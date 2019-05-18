---
title: Configurer Azure Rights Management pour la version précédente de chiffrement de messages Office 365.
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/30/2018
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 2cba47b3-f09e-4911-9207-ac056fcb9db7
description: La version précédente d’Office 365 le chiffrement de messages dépend de Microsoft Azure Rights Management (anciennement appelé Windows Azure Active Directory Rights Management).
ms.openlocfilehash: 84922a57c6245cf3214f17ba922417b5e025b796
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34158496"
---
# <a name="set-up-azure-rights-management-for-the-previous-version-of-office-365-message-encryption"></a>Configurer Azure Rights Management pour la version précédente de chiffrement de messages Office 365.

Cette rubrique décrit les étapes à suivre pour activer, puis configurer Azure Rights Management (RMS), qui fait partie d’Azure information protection, pour une utilisation avec la version précédente d’Office 365 le chiffrement de messages (OME).

## <a name="this-article-only-applies-to-the-previous-version-of-ome"></a>Cet article s’applique uniquement à la version précédente de OME
Si vous n’avez pas encore déplacé votre organisation Office 365 vers les nouvelles fonctionnalités OME, mais que vous avez déjà déployé OME, les informations contenues dans cet article s’appliquent à votre organisation. Microsoft vous recommande de planifier la migration vers les nouvelles fonctionnalités de OME dès que cela est raisonnable pour votre organisation. Pour obtenir des instructions, consultez la rubrique [set up New Office 365 message Encryption Capabilities](set-up-new-message-encryption-capabilities.md). Si vous souhaitez en savoir plus sur la façon dont les nouvelles fonctionnalités fonctionnent en premier, consultez la rubrique [Office 365 message](ome.md)Encryption. Le reste de cet article fait référence au comportement d’OME avant la publication des nouvelles fonctionnalités OME.

## <a name="prerequisites-for-using-the-previous-version-of-office-365-message-encryption"></a>Conditions préalables à l’utilisation de la version précédente d’Office 365 le chiffrement de messages
<a name="warmprereqs"> </a>

Office 365 message Encryption (OME), y compris la gestion des droits relatifs à l’information (IRM), dépend d’Azure Rights Management (Azure RMS). Azure RMS est la technologie de protection utilisée par Azure information protection. Pour utiliser OME, votre organisation Office 365 doit inclure un abonnement Exchange Online ou Exchange Online protection qui, à son tour, inclut un abonnement Azure Rights Management.
  
- Si vous n’êtes pas sûr de ce que comprend votre abonnement, consultez les descriptions de service Exchange Online pour la [stratégie de message, la récupération et la conformité](https://technet.microsoft.com/library/exchange-online-message-policy-recovery-and-compliance.aspx).

- Si vous n’avez pas d’abonnement Azure RMS pour Exchange Online ou Exchange Online Protection, vous devez tout d’abord acheter un abonnement et l’activer.

    Pour plus d’informations sur l’achat d’un abonnement à Azure Rights Management, consultez la rubrique [Azure Rights Management](https://portal.office.com/Signup/MainSignUp15.aspx?&amp;OfferId=9DF77AF9-DAAE-4d51-8E0E-EEEADD4866B8&amp;dl=RIGHTSMANAGEMENT). La section suivante fournit des informations sur l’activation d’Azure Rights Management.

- Si vous disposez d’Azure Rights Management, mais qu’il n’est pas configuré pour Exchange Online ou Exchange Online Protection, cet article explique comment activer Azure Rights Management, puis décrit la meilleure façon de configurer OME pour qu’il fonctionne avec Azure Rights Management.

- Si vous avez déjà configuré OME pour qu’il fonctionne avec Azure Rights Management pour Exchange Online ou Exchange Online Protection, en fonction de sa configuration, vous pouvez commencer à utiliser OME et ses nouvelles fonctionnalités immédiatement. Cet article explique comment déterminer si vous avez configuré OME correctement, ce que vous devez faire si vous avez besoin de modifier votre configuration, et ce qui se passe si vous choisissez de ne pas modifier votre configuration. Par exemple, pour utiliser les nouvelles fonctionnalités, vous devez utiliser Azure RMS avec OME. Vous ne pouvez pas utiliser les nouvelles fonctionnalités avec un RMS Active Directory local.

## <a name="activate-azure-rights-management-for--the-previous-version-of-ome-in-office-365"></a>Activation de la gestion des droits Azure pour la version précédente de OME dans Office 365

Vous devez activer Azure Rights Management afin que les utilisateurs de votre organisation puissent appliquer la protection des informations aux messages qu’ils envoient et ouvrir les messages et fichiers qui ont été protégés par le service Azure Rights Management. Pour obtenir des instructions, consultez la rubrique activation de la [gestion des droits Azure](https://go.microsoft.com/fwlink/p/?LinkId=525775). Une fois que vous avez terminé l’activation, revenez à cet article et poursuivez les tâches décrites dans cet article.
  
## <a name="set-up-the-previous-version-of-ome-to-use-azure-rms-by-importing-trusted-publishing-domains-tpds"></a>Configuration de la version précédente de OME pour utiliser Azure RMS en important des domaines de publication approuvés (domaines)

Un publication approuvé est un fichier XML qui contient des informations sur les paramètres de gestion des droits de votre organisation. Par exemple, le publication approuvé contient des informations sur le certificat de concession de licences serveur utilisé pour la signature et le chiffrement des certificats et des licences, les URL utilisées pour la gestion des licences et la publication, etc. Vous importez le publication approuvé dans votre organisation Office 365 à l’aide de Windows PowerShell.
  
> [!IMPORTANT]
> Auparavant, vous pouviez importer domaines à partir du service AD RMS (Active Directory Rights Management) dans votre organisation Office 365. Toutefois, cette opération vous empêchera d’utiliser les nouvelles fonctionnalités de OME et n’est pas recommandée. Si votre organisation Office 365 est actuellement configurée de cette façon, Microsoft vous recommande de créer un plan de migration de votre compte Active Directory RMS local vers la protection des informations Azure basée sur le Cloud. Pour plus d’informations, reportez-vous à la rubrique [migration d’AD RMS vers Azure information protection](https://docs.microsoft.com/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms). Vous ne pourrez pas utiliser les nouvelles fonctionnalités de OME tant que vous n’aurez pas terminé la migration vers Azure information protection.
  
 **Pour importer domaines à partir d’Azure RMS**
  
1. [Connectez-vous à Exchange Online à l’aide de Remote PowerShell](https://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).

2. Choisissez l’URL de partage de clés correspondant à l’emplacement géographique de votre organisation Office 365:

|**Emplacement**|**URL d’emplacement de partage de clé**|
|:-----|:-----|
|Amérique du Nord  <br/> |https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|Union européenne  <br/> |https://sp-rms.eu.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|Région  <br/> |https://sp-rms.ap.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|Amérique du Sud  <br/> |https://sp-rms.sa.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|Office 365 Secteur Public (nuage communautaire propre aux gouvernements)  <br/> Cet emplacement de partage de clé RMS est réservé aux clients qui ont acheté des SKU Office 365 pour le gouvernement.  <br/> |https://sp-rms.govus.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
   
3. Configurez l’emplacement de partage de clés en exécutant la cmdlet [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.160%29.aspx) comme suit: 
    
  ```
  Set-IRMConfiguration -RMSOnlineKeySharingLocation "<RMSKeySharingURL >"
  ```

    Par exemple, pour configurer l’emplacement de partage de clé si votre organisation est située en Amérique du Nord:
    
  ```
  Set-IRMConfiguration -RMSOnlineKeySharingLocation "https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc"
  ```

4. Exécutez l’applet de commande [Import-RMSTrustedPublishingDomain](https://technet.microsoft.com/library/jj200724%28v=exchg.150%29.aspx) avec le commutateur-RMSOnline pour importer les publication approuvé à partir d’Azure Rights Management: 
    
  ```
  Import-RMSTrustedPublishingDomain -RMSOnline -Name "<TPDName> "
  ```

    Où *TPDName* est le nom que vous souhaitez utiliser pour le publication approuvé. Par exemple, «contoso North American publication approuvé». 
    
5. Pour vérifier que vous avez bien configuré votre organisation Office 365 afin qu’elle utilise le service Azure Rights Management, exécutez la cmdlet [test-IRMConfiguration](https://technet.microsoft.com/library/dd979798%28v=exchg.160%29.aspx) avec le commutateur-RMSOnline comme suit: 
    
  ```
  Test-IRMConfiguration -RMSOnline
  ```

    Entre autres choses, cette applet de commande vérifie la connectivité avec le service Azure Rights Management, télécharge le publication approuvé et vérifie sa validité.
    
6. Exécutez la cmdlet [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.150%29.aspx) comme suit pour désactiver les modèles Azure Rights Management d’être disponibles dans Outlook sur le Web et Outlook: 
    
  ```
  Set-IRMConfiguration -ClientAccessServerEnabled $false
  ```

7. Exécutez la cmdlet [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.150%29.aspx) comme suit pour activer Azure Rights Management pour votre organisation de messagerie en nuage et configurez-le pour utiliser le chiffrement de messages Azure Rights Management pour Office 365: 
    
  ```
  Set-IRMConfiguration -InternalLicensingEnabled $true
  ```

8. Pour vérifier que vous avez correctement importé le publication approuvé et activé Azure Rights Management, utilisez l’applet de commande test-IRMConfiguration pour tester la fonctionnalité de gestion des droits Azure. Pour plus d'informations, consultez « Exemple 1 » dans la rubrique [Test-IRMConfiguration](https://technet.microsoft.com/library/dd979798%28v=exchg.150%29.aspx).
    
## <a name="i-have-the-previous-version-of-ome-set-up-with-active-directory-rights-management-not-azure-information-protection-what-do-i-do"></a>J’ai la version précédente de OME configurée avec Active Directory Rights Management not Azure information protection, que dois-je faire?
<a name="importTPDs"> </a>

Vous pouvez continuer à utiliser les règles de flux de messagerie de chiffrement de messages Office 365 existantes avec la gestion des droits Active Directory, mais vous ne pouvez pas configurer ou utiliser les nouvelles fonctionnalités de OME. Au lieu de cela, vous devez migrer vers Azure information protection. Pour plus d’informations sur la migration et ce que cela signifie pour votre organisation, consultez la rubrique [migration d’AD RMS vers Azure information protection](https://docs.microsoft.com/information-protection/deploy-use/prepare-environment-adrms).
  
## <a name="next-steps"></a>Étapes suivantes
<a name="importTPDs"> </a>

Une fois que vous avez terminé l’installation d’Azure Rights Management, si vous souhaitez activer les nouvelles fonctionnalités de OME, consultez la rubrique [set up New Office 365 message Encryption Capabilities Built-Top of Azure information protection.](https://support.office.com/article/7ff0c040-b25c-4378-9904-b1b50210d00e)
  
Une fois que vous avez configuré votre organisation pour utiliser les nouvelles fonctionnalités de OME, vous êtes prêt à [définir des règles de flux de messagerie pour protéger les messages électroniques avec les nouvelles fonctionnalités de OME](define-mail-flow-rules-to-encrypt-email.md).
  
## <a name="related-topics"></a>Voir aussi
<a name="importTPDs"> </a>

[Chiffrement dans Office 365](encryption.md)
  
[Détails techniques de référence sur le chiffrement dans Office 365](technical-reference-details-about-encryption.md)
  
[Qu’est-ce que Azure Rights Management?](https://docs.microsoft.com/information-protection/understand-explore/what-is-azure-rms)
  

