---
title: Configurer les nouvelles fonctionnalités de chiffrement de messages Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/19/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 7ff0c040-b25c-4378-9904-b1b50210d00e
description: Nouvel Office 365 Message Encryption fonctionnalités greffées sur la Protection des informations Azure, votre organisation peuvent utiliser protégé de communication par courrier électronique avec des personnes à l’intérieur et à l’extérieur de votre organisation. Les nouvelles fonctionnalités OME fonctionnent avec d’autres organisations Office 365, Outlook.com, Gmail et autres services de messagerie.
ms.openlocfilehash: e59368f5854c86c04f4f0bdf376537d3f6b02d33
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528681"
---
# <a name="set-up-new-office-365-message-encryption-capabilities"></a>Configurer les nouvelles fonctionnalités de chiffrement de messages Office 365

Avec les nouvelles fonctionnalités d’Office 365 Message Encryption (OME), qui exploitent les fonctionnalités de protection de la Protection des informations Azure, votre organisation peut partager facilement électronique protégé avec tout le monde sur n’importe quel appareil. Les utilisateurs peuvent envoyer et recevoir des messages protégés avec d’autres organisations Office 365, ainsi que les clients Office 365 à l’aide de Outlook.com, Gmail et autres services de messagerie.
  
## <a name="get-started-with-ome-by-activating-azure-rights-management-part-of-azure-information-protection"></a>Mise en route avec OME en activant Azure Rights Management, composant Azure de Protection des informations

Il est désormais facile à prendre en main les nouvelles fonctionnalités d’OME. À compter de février 2018, Office 365 active automatiquement les nouvelles fonctionnalités OME pour les organisations éligibles dans nos centres de données. Votre organisation est éligible s’il est un nouveau client Office 365 et votre organisation a les abonnements appropriés. ** If ** ** vous avez activé Azure Rights Management Services (RMS Azure), partie Azure de Protection des informations, puis nous activer automatiquement Office 365 Message Encryption pour vous. ** Vous n’êtes pas obligé de faire quoi pour activer OME. Pour activer Azure Rights Management, consultez la rubrique [Activer Azure Rights Management](https://docs.microsoft.com/azure/information-protection/deploy-use/activate-service). Pour plus d’informations sur les abonnements, voir « les abonnements ai-je besoin pour utiliser le nouveau capabilities? OME » dans le [Forum aux questions sur le chiffrement de Message Office 365](ome-faq.md). Pour plus d’informations sur l’achat d’un abonnement Azure protection des informations, voir [La Protection des informations Azure](https://azure.microsoft.com/services/information-protection/).
  
Si vous utilisez Exchange Online avec Active Directory Rights Management Services AD RMS, vous ne pouvez pas activer ces nouvelles fonctionnalités immédiatement. Au lieu de cela, vous devez migrer à partir d’AD RMS pour la Protection des informations Azure tout d’abord. Lorsque vous avez terminé la migration, vous pouvez appliquer la procédure suivante.
  
Si vous choisissez de continuer à utiliser sur site AD RMS avec Exchange Online au lieu de la migration vers Azure la Protection des informations, vous ne pourrez pas utiliser ces nouvelles fonctionnalités.
  
## <a name="how-the-new-capabilities-for-ome-work"></a>Comment fonctionnent les nouvelles fonctionnalités pour OME

Les nouvelles fonctionnalités d’Office 365 Message Encryption utilisent les fonctionnalités de protection, également appelées Azure Rights Management Services (RMS Azure), à partir de la Protection des informations Azure. Cela inclut les stratégies de chiffrement, d’identité et d’autorisation pour sécuriser votre courrier électronique. Vous pouvez chiffrer les messages à l’aide de l' [option chiffrer uniquement](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails), l' [option ne pas transférer](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails)et modèles de gestion des droits. Les utilisateurs peuvent ensuite crypter les messages électroniques et un ensemble de pièces jointes Office 365 à l’aide de ces options. Pour obtenir une liste complète des types de pièce jointe pris en charge, voir [« types de fichiers couverts par les stratégies IRM lorsqu’ils sont joints aux messages » dans présentation IRM pour les messages électroniques](https://support.office.com/article/bb643d33-4a3f-4ac7-9770-fd50d95f58dc#FileTypesforIRM). En tant qu’administrateur, vous pouvez également définir des règles de flux de messagerie pour appliquer cette protection. Par exemple, vous pouvez définir une règle où tous les messages non protégés qui sont adressés à un destinataire spécifique ou qui contiennent des mots spécifiques dans la ligne objet sont protégés contre les accès et les destinataires ne peut pas copier ou imprimer le contenu du message.
  
Contrairement à la version précédente d’OME, ces nouvelles fonctionnalités fournissent une expérience unifiée expéditeur si vous envoyez un courrier à l’intérieur de votre organisation ou à des destinataires en dehors d’Office 365. En outre, les destinataires qui reçoivent un message protégé envoyé à un compte Office 365 dans 2016 Outlook ou Outlook sur le web, inutile d’aucune action supplémentaire pour afficher le message. Il fonctionne de façon transparente. Destinataires à l’aide d’autres clients de messagerie et les fournisseurs de services de messagerie également auront une expérience améliorée. Pour plus d’informations, voir [Découvrez les messages protégés dans Office 365](https://support.office.com/article/Learn-about-protected-messages-in-Office-365-2baf3ac7-12db-40a4-8af7-1852204b4b67) et [comment ouvrir un message protégé](https://support.office.com/article/How-do-I-open-a-protected-message-1157a286-8ecc-4b1e-ac43-2a608fbf3098).
  
## <a name="steps-to-manually-set-up-the-new-capabilities-for-ome"></a>Étapes pour configurer manuellement les nouvelles fonctionnalités pour OME

Si votre organisation ne possède pas automatiquement OME activé, ou si vous avez activé OME désactivé, procédez comme suit pour configurer manuellement les nouvelles fonctionnalités pour OME.
  
### <a name="to-manually-set-up-the-new-capabilities-for-ome"></a>Pour configurer manuellement les nouvelles fonctionnalités pour OME

1. Vérifiez que vous avez l’abonnement pour votre organisation. Pour plus d’informations sur les abonnements, voir « les abonnements ai-je besoin pour utiliser le nouveau capabilities? OME » dans la [Office 365 Message Encryption FAQ.](ome-faq.md) Pour plus d’informations sur l’achat d’un abonnement Azure protection des informations, voir [La Protection des informations Azure](https://azure.microsoft.com/services/information-protection/).
    
2. Décider si vous souhaitez que Microsoft pour gérer la clé de la racine pour la Protection des informations Azure (par défaut), ou générer et gérer cette clé vous-même (également appelés mettre votre propre clé ou BYOK). Si vous souhaitez générer et gérer cette clé vous-même, vous devez effectuer certaines étapes avant de configurer les nouvelles fonctionnalités pour OME. Pour plus d’informations, voir [planification et l’implémentation de votre clé de client Azure la Protection des informations](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key). Microsoft recommande que vous effectuez ces étapes avant de configurer OME.
    
3. Activer les nouvelles fonctionnalités pour OME en activant Azure Rights Management. Pour plus d’informations, voir [Activation Azure Rights Management](https://docs.microsoft.com/azure/information-protection/deploy-use/activate-service). Lorsque vous effectuez cette opération, Office 365 active automatiquement les nouvelles fonctionnalités OME pour vous.
    
    > [!TIP]
    > Outlook sur le Web met en cache son interface utilisateur, il est conseillé d’attendre un jour avant que vous essayez d’appliquer les nouvelles fonctionnalités pour OME pour les messages électroniques à l’aide de ce client. Avant de l’interface utilisateur met à jour pour refléter la nouvelle configuration, les nouvelles fonctionnalités pour OME ne sont pas disponibles. Après mise à jour de l’interface utilisateur, les utilisateurs peuvent protéger les messages électroniques à l’aide des nouvelles fonctionnalités pour OME. 
  
4. (Facultatif) Définir de nouvelles règles de flux de messagerie ou mettre à jour les règles de flux messagerie existante qui définissent comment et quand vous souhaitez qu’Office 365 pour chiffrer les messages envoyés à partir de votre organisation.
    
## <a name="verify-that-the-new-capabilities-for-ome-are-configured-properly-by-using-windows-powershell"></a>Vérifiez que les nouvelles fonctionnalités pour OME sont correctement configurées à l’aide de Windows PowerShell

Procédez comme suit pour vérifier que votre client est correctement configuré pour utiliser les nouvelles fonctionnalités pour OME via Exchange Online PowerShell.
  
1. À l’aide d’un compte qui dispose des autorisations d’administrateur global dans votre organisation Office 365 Professionnel ou de l’école, démarrer une session Windows PowerShell et se connecter à Exchange Online. Pour plus d’informations, voir [se connecter à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).
    
2. Exécutez l’applet de commande Test-IRMConfiguration à l’aide de la syntaxe suivante :
    
  ```
  Test-IRMConfiguration [-Sender <email address >]
  ```

    Par exemple :
    
  ```
  Test-IRMConfiguration -Sender securityadmin@contoso.com
  ```

    Où l’adresse est l’adresse de messagerie d’un utilisateur dans votre organisation Office 365. Facultatif, qui fournit une adresse de messagerie de l’expéditeur force le système à effectuer des contrôles supplémentaires.
    
    Vos résultats doivent se présenter comme celles-ci :
    
  ```
  Results : Acquiring RMS Templates ...
                - PASS: RMS Templates acquired.  Templates available: Contoso  - Confidential View Only, Contoso  - Confidential, Do Not 
            Forward.
            Verifying encryption ...
                - PASS: Encryption verified successfully.
            Verifying decryption ...
                - PASS: Decryption verified successfully.
            Verifying IRM is enabled ...
                - PASS: IRM verified successfully.
            
            OVERALL RESULT: PASS
  ```

    Où *Contoso* est remplacée par le nom de votre organisation Office 365. 
    
    Les noms des modèles par défaut renvoyés dans les résultats peuvent être différentes de celles affichées dans les résultats ci-dessus.
    
    Pour obtenir une introduction aux modèles et des informations sur les modèles par défaut, voir [configuration et gestion des modèles pour la Protection des informations Azure](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates). Pour plus d’informations sur ne pas transférer option, l’option chiffrer uniquement et comment créer des modèles supplémentaires, ou Découvrez quels droits sont inclus dans un modèle existant, consultez la rubrique [Configuration des droits d’utilisation pour Azure Rights Management](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights).
    
3. Exécutez l’applet de commande Remove-PSSession pour déconnecter la session à partir du service de gestion des droits.
    
  ```
  Remove-PSSession $session
  ```

## <a name="next-steps-define-new-mail-flow-rules-that-use-the-new-ome-capabilities"></a>Étapes suivantes : définir de nouvelles règles de flux de messagerie qui utilisent les nouvelles fonctionnalités OME
<a name="Rules_1"> </a>

Cette étape est facultative pour les nouveaux déploiements OME, toutefois, cette étape est requise pour les déploiements OME existants qui ont déjà des règles de flux de messagerie configuré pour chiffrer les messages sortants. Si vous souhaitez tirer parti des nouvelles fonctionnalités OME, vous devez mettre à jour vos règles de flux de messagerie existante. Dans le cas contraire, vos utilisateurs continueront à recevoir des messages chiffrés qui utilise le format de pièce jointe HTML précédent au lieu de la nouvelle expérience OME transparent.
  
Règles de flux de messagerie déterminent dans un message quelles conditions les messages doivent être chiffrées, ainsi que les conditions de suppression que le chiffrement. Lorsque vous définissez une action d’une règle, tous les messages qui correspondent aux conditions de règle sont chiffrées lorsqu’ils sont envoyés.
  
Pour plus d’informations sur les règles de flux de messagerie, voir [définir les règles de flux des messages pour chiffrer les messages électroniques dans Office 365](define-mail-flow-rules-to-encrypt-email.md).
  
## <a name="related-topics"></a>Voir aussi
<a name="Rules_1"> </a>

[Envoyer, consulter et répondre aux messages chiffrés dans Outlook](https://support.office.com/article/eaa43495-9bbb-4fca-922a-df90dee51980.aspx)
  
[Enable-Aadrm](https://docs.microsoft.com/powershell/module/aadrm/enable-aadrm?view=azureipps)
  
[Connexion à Exchange Online PowerShell](https://technet.microsoft.com/library/jj984289%28v=exchg.160%29.aspx)
  
[Définir des règles de flux de messagerie pour chiffrer les messages électroniques dans Office 365](define-mail-flow-rules-to-encrypt-email.md)
  

