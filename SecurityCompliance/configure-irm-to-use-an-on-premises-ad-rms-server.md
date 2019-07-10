---
title: Configuration de la Gestion des droits relatifs à l’information (IRM) pour utiliser un serveur AD RMS local
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/13/2017
audience: End User
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 3ecde857-4b7c-451d-b4aa-9eeffc8a8c61
ms.collection:
- M365-security-compliance
description: Cette rubrique décrit la configuration de la gestion des droits relatifs à l'information de manière à utiliser un serveur AD RMS.
ms.openlocfilehash: 6f764ddf3604dcf0d6b28a37b56a498489c0769f
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35600170"
---
# <a name="configure-irm-to-use-an-on-premises-ad-rms-server"></a>Configuration de la Gestion des droits relatifs à l’information (IRM) pour utiliser un serveur AD RMS local
  
Pour une utilisation avec des déploiements locaux, la gestion des droits relatifs à l’information (IRM) dans Exchange Online utilise les services AD RMS (Active Directory Rights Management Services), une technologie de protection des informations dans Windows Server 2008 et versions ultérieures. La protection IRM permet d'appliquer un modèle de stratégie de droits AD RMS à un message électronique. Les droits sont joints au message lui-même pour que la protection s’effectue en ligne et hors connexion, et à l’intérieur et à l’extérieur du pare-feu de votre organisation.
  
Cette rubrique décrit la configuration de la gestion des droits relatifs à l'information de manière à utiliser un serveur AD RMS. Pour plus d’informations sur l’utilisation des nouvelles fonctionnalités pour le chiffrement de messages Office 365 avec Azure Active Directory et Azure Rights Management, consultez le [Forum aux questions sur le chiffrement de messages office 365](https://support.office.com/article/0432dce9-d9b6-4e73-8a13-4a932eb0081e).
  
Pour en savoir plus sur la Gestion des droits relatifs à l'information dans Exchange Online, consultez la rubrique [Gestion des droits relatifs à l'information (IRM) dans Exchange Online](information-rights-management-in-exchange-online.md).
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>Ce qu’il faut savoir avant de commencer
<a name="sectionSection0"> </a>

- Durée d'exécution estimée de cette tâche : 30 minutes
    
- Des autorisations doivent vous être attribuées avant de pouvoir exécuter cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez l'entrée « Gestion des droits relatifs à l'information » dans la rubrique [Messaging policy and compliance permissions](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx). 
    
- Le serveur AD RMS doit exécuter Windows Server 2008 ou une version ultérieure. Pour plus d'informations sur le déploiement d'AD RMS, consultez [Installation d'un cluster AD RMS](https://go.microsoft.com/fwlink/?LinkId=210873).
    
- Pour plus d'informations sur l'installation et la configuration de Windows PowerShell et la connexion au service, consultez la rubrique [Connexion à Exchange Online à l'aide de Remote PowerShell](http://technet.microsoft.com/library/c8bea338-6c1a-4bdf-8de0-7895d427ee5b.aspx).
    
- Pour des informations sur les raccourcis clavier applicables aux procédures de cette rubrique, voir Raccourcis clavier dans Exchange 2013 **Keyboard shortcuts in Exchange 2013**.
    
> [!TIP]
> Vous rencontrez des difficultés ? Demandez de l'aide en participant aux forums Exchange. Visitez les forums sur les pages [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), et [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351). 
  
## <a name="how-do-you-do-this"></a>Comment procéder ?
<a name="sectionSection1"> </a>

### <a name="step-1-use-the-ad-rms-console-to-export-a-trusted-publishing-domain-tpd-from-an-ad-rms-server"></a>Étape 1 : utiliser la console AD RMS pour exporter un domaine de publication approuvé (TPD) à partir d'un serveur AD RMS

La première étape consiste à exporter un domaine de publication approuvé vers un fichier XML local à partir du serveur AD RMS local. Le domaine de publication approuvé contient les paramètres suivants requis pour utiliser les fonctionnalités RMS : 
  
- le certificat de licence serveur (SLC) utilisé pour signer et chiffrer les certificats et licences ;
    
- les URL utilisées pour les licences et les publications ;
    
- les modèles de stratégie de droits AD RMS créés avec le SLC spécifique au domaine de publication approuvé.
    
Quand vous importez le domaine de publication approuvé, il est stocké et protégé dans Exchange Online.
  
1. Ouvrez la console Active Directory Rights Management Services et développez le cluster AD RMS.
    
2. Dans l'arborescence de la console, développez **Stratégies d'approbation**, puis cliquez sur **Domaines de publication approuvés**.
    
3. Dans le volet des résultats, sélectionnez le certificat du domaine à exporter.
    
4. Dans le volet **Actions**, cliquez sur **Exporter le domaine de publication approuvé**.
    
5. Dans la zone **Fichier de domaine de publication**, cliquez sur **Enregistrer sous** pour enregistrer le fichier dans un emplacement spécifique sur l'ordinateur local. Entrez un nom de fichier et assurez-vous de spécifier l'extension de fichier  `.xml`, puis cliquez sur **Enregistrer**.
    
6. Dans les zones **Mot de passe** et **Confirmer le mot de passe**, entrez un mot de passe fort qui sera utilisé pour chiffrer le fichier de domaine de publication approuvé. Vous devrez spécifier ce mot de passe lors de l'importation du domaine de publication approuvé vers votre système de messagerie en nuage. 
    
### <a name="step-2-use-the-exchange-management-shell-to-import-the-tpd-to-exchange-online"></a>Étape 2 : utiliser l'Environnement de ligne de commande Exchange Management Shell pour importer le domaine de publication approuvé dans Exchange Online

Après avoir exporté le domaine de publication approuvé vers un fichier XML, vous devez l'importer dans Exchange Online. Quand un domaine de publication approuvé est importé, les modèles AD RMS de votre organisation sont également importés. Quand le premier domaine de publication approuvé est importé, il devient le domaine de publication approuvé par défaut de votre organisation en nuage. Si vous importez un autre domaine de publication approuvé, vous pouvez utiliser le commutateur **Par défaut** pour le définir en tant que domaine de publication approuvé par défaut disponible aux utilisateurs. 
  
Pour importer le domaine de publication approuvé, exécutez la commande suivante dans Windows PowerShell :
  
```
Import-RMSTrustedPublishingDomain -FileData $([byte[]](Get-Content -Encoding byte -Path <path to exported TPD file> -ReadCount 0)) -Name "<name of TPD>" -ExtranetLicensingUrl <URL> -IntranetLicensingUrl <URL>
```

Vous pouvez obtenir les valeurs des paramètres  _ExtranetLicensingUrl_ et  _IntranetLicensingUrl_ dans la console Active Directory Rights Management Services. Sélectionnez le cluster AD RMS dans l'arborescence de la console. Les URL des licences s'affichent dans le volet des résultats. Ces URL sont utilisées par les clients de messagerie quand le contenu doit être déchiffré et quand Exchange Online doit déterminer quel domaine de publication approuvé il convient d'utiliser. 
  
Quand vous utilisez cette commande, vous êtes invité à saisir un mot de passe. Entrez le mot de passe que vous avez spécifié lors de l'exportation du domaine de publication approuvé à partir de votre serveur AD RMS.
  
Par exemple; la commande suivante importe le domaine de publication approuvé appelé « Exported TPD », à l'aide du fichier XML exporté à partir de votre serveur AD RMS et enregistré sur l'ordinateur de votre compte d'administrateur. Le paramètre Nom est utilisé pour spécifier un nom pour le domaine de publication approuvé.
  
```
Import-RMSTrustedPublishingDomain -FileData $([byte[]](Get-Content -Encoding byte -Path C:\Users\Administrator\Desktop\ExportTPD.xml -ReadCount 0)) -Name "Exported TPD" -ExtranetLicensingUrl https://corp.contoso.com/_wmcs/licensing -IntranetLicensingUrl https://rmsserver/_wmcs/licensing
```

Pour plus d'informations sur la syntaxe et les paramètres, consultez la rubrique [Import-RMSTrustedPublishingDomain](http://technet.microsoft.com/library/7c5e7a0f-9c9d-4863-bab8-bcc729cc16a6.aspx).
  
#### <a name="how-do-you-know-this-step-worked"></a>Comment savoir si cette étape a fonctionné ?

Pour vérifier que le domaine de publication a bien été importé, exécutez la cmdlet **Get-RMSTrustedPublishingDomain** pour récupérer les domaines de publication approuvés dans votre organisation Exchange Online. Pour plus de détails, consultez les exemples de la rubrique [Get-RMSTrustedPublishingDomain](http://technet.microsoft.com/library/69499195-f08f-41bd-b0ed-443688410b12.aspx).
  
### <a name="step-3-use-the-exchange-management-shell-to-distribute-an-ad-rms-rights-policy-template"></a>Étape 3 : utiliser l'Environnement de ligne de commande Exchange Management Shell pour distribuer un modèle de stratégie de droits AD RMS

Après avoir importé le domaine de publication approuvé, vous devez vous assurer qu'un modèle de stratégie de droits AD RMS est distribué. Un modèle distribué est visible par les utilisateurs d’Outlook sur le Web (anciennement appelé Outlook Web App), qui peuvent ensuite appliquer les modèles à un message électronique.
  
Pour renvoyer une liste de tous les modèles du domaine de publication approuvé par défaut, exécutez la commande suivante :
  
```
Get-RMSTemplate -Type All | fl
```

Si la valeur du paramètre  _Type_ est  `Archived`, le modèle n'est pas visible aux utilisateurs. Seuls les modèles distribués dans le publication approuvé par défaut sont disponibles dans Outlook sur le Web.
  
Pour distribuer un modèle, exécutez la commande suivante :
  
```
Set-RMSTemplate -Identity "<name of the template>" -Type Distributed
```

Par exemple, la commande suivante importe le modèle « Propriétaire ».
  
```
Set-RMSTemplate -Identity "Company Confidential" -Type Distributed
```

Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez les rubriques [Get-RMSTemplate](http://technet.microsoft.com/library/4a5066e8-b770-4aa2-b464-0d2190914f71.aspx) et [Set-RMSTemplate](http://technet.microsoft.com/library/4637f6b8-751a-4f5e-8869-428250230382.aspx).
  
 **Modèle Ne pas transférer**
  
Quand vous importez le domaine de publication approuvé par défaut de votre organisation locale dans Exchange Online, un modèle de stratégie de droits AD RMS nommé **Ne pas transférer** est importé. C'est le modèle distribué par défaut quand vous importez le domaine de publication approuvé par défaut. Vous ne pouvez pas utiliser la cmdlet **Set-RMSTemplate** pour modifier le modèle **Ne pas transférer**. 
  
When the **Do Not Forward** template is applied to a message, only the recipients addressed in the message can read the message. Additionally, recipients can't do the following: 
  
- transférer le message à une autre personne ;
    
- copier le contenu du message ;
    
- imprimer le message.
    
> [!IMPORTANT]
> Le modèle **Ne pas transférer** ne peut pas empêcher qu'un message soit copié avec un programme de capture d'écran tiers, pris en photo, ou simplement copié à la main par les utilisateurs. 
  
Vous pouvez créer des modèles de stratégie de droits AD RMS supplémentaires sur le serveur AD RMS de votre organisation locale pour répondre aux exigences de protection IRM. Si vous créez des modèles de stratégie de droits AD RMS supplémentaires, vous devez de nouveau exporter le domaine de publication approuvé à partir du serveur AD RMS local et l'actualiser dans l'organisation de messagerie en nuage. 
  
#### <a name="how-do-you-know-this-step-worked"></a>Comment savoir si cette étape a fonctionné ?

Pour vérifier qu'un modèle de stratégie de droits AD RMS a été distribué correctement, exécutez la cmdlet **Get-RMSTemplate** pour vérifier les propriétés du modèle. Pour plus de détails, consultez les exemples de la rubrique [Get-RMSTemplate](http://technet.microsoft.com/library/4a5066e8-b770-4aa2-b464-0d2190914f71.aspx).
  
### <a name="step-4-use-the-exchange-management-shell-to-enable-irm"></a>Étape 4: utiliser l'Environnement de ligne de commande Exchange Management Shell pour activer la Gestion des droits relatifs à l'information

Après avoir importé le domaine de publication approuvé et distribué un modèle de stratégie de droits AD RMS, exécutez la commande suivante pour activer la Gestion des droits relatifs à l'information dans votre organisation de messagerie en nuage.
  
```
Set-IRMConfiguration -InternalLicensingEnabled $true
```

Pour plus d'informations sur la syntaxe et les paramètres, consultez la rubrique [Set-IRMConfiguration](http://technet.microsoft.com/library/5df0b56a-7bcc-4be2-b4b8-4de16720476c.aspx).
  
#### <a name="how-do-you-know-this-step-worked"></a>Comment savoir si cette étape a fonctionné ?

Pour vérifier que l'IRM a bien été activée, exécutez la cmdlet [Get-IRMConfiguration](http://technet.microsoft.com/library/e1821219-fe18-4642-a9c2-58eb0aadd61a.aspx) pour vérifier la configuration IRM dans l'organisation Exchange Online. 
  
## <a name="how-do-you-know-this-task-worked"></a>Comment savoir si cette tâche a fonctionné ?
<a name="sectionSection2"> </a>

Pour vérifier que vous avez correctement importé le domaine de publication approuvé et activé la fonctionnalité IRM, procédez comme suit :
  
- Exécutez la cmdlet **Test-IRMConfiguration** pour tester la fonctionnalité IRM. Pour plus d'informations, consultez « Exemple 1 » dans la rubrique [Test-IRMConfiguration](http://technet.microsoft.com/library/a730e7ff-a67f-4360-b5ff-70d171bb5e1d.aspx).
    
- Rédigez un nouveau message dans Outlook sur le Web et protégez l’IRM en sélectionnant l’option **définir les autorisations** dans le ![menu étendu (](media/ITPro-EAC-MoreOptionsIcon.gif)icône Options supplémentaires).
    

