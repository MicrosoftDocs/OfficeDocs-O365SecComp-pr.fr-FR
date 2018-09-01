---
title: Configurer Azure Rights Management pour le chiffrement de messages Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/3/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 2cba47b3-f09e-4911-9207-ac056fcb9db7
description: 'Chiffrement de messages Office 365 dépend de Microsoft Azure Rights Management (anciennement appelé Windows Azure Active Directory Rights Management). '
ms.openlocfilehash: 99c8de49330cf99545d28d81e0c99c2138797356
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528152"
---
# <a name="set-up-azure-rights-management-for-office-365-message-encryption"></a>Configurer Azure Rights Management pour le chiffrement de messages Office 365

Cette rubrique décrit les étapes à suivre afin d’activer, puis définissez les Azure RMS (Rights Management), partie de la Protection des informations Azure, pour une utilisation avec Office 365 Message Encryption (OME).
  
## <a name="prerequisites-for-using-office-365-message-encryption"></a>Les conditions préalables à l’utilisation du chiffrement des messages Office 365
<a name="warmprereqs"> </a>

Office 365 Message Encryption (OME), y compris IRM, dépend Azure Rights Management (Services RMS Azure). RMS Azure est la technologie de protection utilisée par la Protection des informations Azure. Pour utiliser OME, votre organisation Office 365 doit inclure un abonnement Exchange Online ou Exchange Online Protection qui, à son tour, inclut un abonnement Azure Rights Management.
  
- Si vous n’êtes pas sûr de ce que comprend votre abonnement, consultez les descriptions de service Exchange Online de [Message, de récupération et de conformité](https://technet.microsoft.com/library/exchange-online-message-policy-recovery-and-compliance.aspx).
    
- Si vous ne disposez pas un abonnement Azure RMS pour Exchange Online ou Exchange Online Protection, vous devez acheter un abonnement et tout d’abord l’activer.
    
    Pour plus d’informations sur l’achat d’un abonnement Azure Rights Management, consultez [Azure Rights Management](https://portal.office.com/Signup/MainSignUp15.aspx?&amp;OfferId=9DF77AF9-DAAE-4d51-8E0E-EEEADD4866B8&amp;dl=RIGHTSMANAGEMENT). La section suivante fournit des informations sur l’activation d’Azure Rights Management.
    
- Si vous avez Azure Rights Management, mais il n’est pas configuré pour Exchange Online ou Exchange Online Protection, cet article explique comment activer Azure Rights Management, puis le décrit la meilleure façon de configurer OME pour fonctionner avec Azure Rights Management.
    
- Si vous avez déjà configuré OME pour fonctionner avec Azure Rights Management pour Exchange Online ou Exchange Online Protection, en fonction de la façon dont vous l’avez configuré, il se peut que vous ne soyez prêt à commencer à utiliser immédiatement de OME et ses nouvelles fonctionnalités. Cet article explique comment déterminer si vous avez configuré OME correctement, que faire si vous devez modifier votre configuration et que se passe-t-il si vous choisissez de ne pas modifier votre configuration. Par exemple, pour pouvoir utiliser les nouvelles fonctionnalités, vous devez utiliser RMS Azure avec OME. Vous ne pouvez pas utiliser les nouvelles fonctionnalités avec un Active Directory RMS du local.
    
## <a name="activate-azure-rights-management-for-ome-in-office-365"></a>Activer Azure Rights Management pour OME dans Office 365
<a name="activatewarm"> </a>

Vous devez activer Azure Rights Management afin que les utilisateurs de votre organisation peuvent appliquer la protection des informations aux messages qu’ils envoient et ouvrir des fichiers qui ont été protégés par le service Azure Rights Management et des messages. Pour plus d’informations, voir [Activation Azure Rights Management](https://go.microsoft.com/fwlink/p/?LinkId=525775). Une fois que vous avez terminé l’activation, revenez ici et continuez avec les tâches dans cet article.
  
## <a name="set-up-ome-to-use-azure-rms-by-importing-trusted-publishing-domains-tpds"></a>Configurer les OME à utiliser RMS Azure en important des domaines de publication approuvés (TPD)
<a name="importTPDs"> </a>

Un domaine de publication approuvé est un fichier XML qui contient des informations sur les paramètres de gestion des droits de votre organisation. Par exemple, le domaine de publication approuvé contient des informations sur le certificat de licence serveur (SLC) utilisé pour signer et chiffrer les certificats et les licences, l’URL utilisée pour la gestion des licences et de publication et ainsi de suite. Vous importez le domaine de publication approuvé dans votre organisation Office 365 à l’aide de Windows PowerShell.
  
> [!IMPORTANT]
> Auparavant, vous pouvez choisir Importer TPD à partir du service Active Directory Rights Management (Services AD RMS) dans votre organisation Office 365. Toutefois, cela vous empêche d’utiliser les nouvelles fonctionnalités OME et n’est pas recommandée. Si Office 365 entreprise est actuellement configuré de cette manière, Microsoft recommande que vous créez un plan de migration à partir de votre Active Directory RMS du local à la Protection des informations Azure basées sur le nuage. Pour plus d’informations, voir [migration à partir d’AD RMS pour la Protection des informations Azure](https://docs.microsoft.com/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms). Vous ne serez pas en mesure d’utiliser les nouvelles fonctionnalités OME jusqu'à ce que vous avez terminé la migration vers Azure la Protection des informations. 
  
 **Pour importer le TPD de RMS Azure**
  
1. [Se connecter à Exchange Online à l’aide de PowerShell à distance](https://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).
    
2. Choisissez l’URL de partage de clé qui correspond à l’emplacement géographique de votre organisation Office 365 :
    
|**Emplacement**|**URL de l’emplacement de partage de clé**|
|:-----|:-----|
|Amérique du Nord  <br/> |https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|Union européenne  <br/> |https://sp-rms.eu.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|Asie  <br/> |https://sp-rms.ap.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|Amérique du Sud  <br/> |https://sp-rms.sa.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|Office 365 pour le gouvernement (nuage communautaire propre aux gouvernements)  <br/> Cet emplacement de partage de clé RMS est réservé pour les clients ayant acheté Office 365 pour le gouvernement SKU.  <br/> |https://sp-rms.govus.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
   
3. Configurer l’emplacement de partage de clé en exécutant l’applet de commande [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.160%29.aspx) comme suit : 
    
  ```
  Set-IRMConfiguration -RMSOnlineKeySharingLocation "<RMSKeySharingURL >"
  ```

    Par exemple, pour configurer la clé emplacement de partage si votre organisation est située en Amérique du Nord :
    
  ```
  Set-IRMConfiguration -RMSOnlineKeySharingLocation "https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc"
  ```

4. Exécutez la cmdlet [Import-RMSTrustedPublishingDomain](https://technet.microsoft.com/library/jj200724%28v=exchg.150%29.aspx) avec le commutateur RMSOnline - pour importer le domaine de publication approuvé d’Azure Rights Management : 
    
  ```
  Import-RMSTrustedPublishingDomain -RMSOnline -Name "<TPDName> "
  ```

    Où *TPDName* est le nom que vous souhaitez utiliser pour le domaine de publication approuvé. Par exemple, « Contoso Amérique du Nord TPD ». 
    
5. Pour vérifier que vous avez configuré correctement votre organisation Office 365 pour utiliser le service Azure Rights Management, exécutez l’applet de commande [Test-IRMConfiguration](https://technet.microsoft.com/library/dd979798%28v=exchg.160%29.aspx) avec le commutateur RMSOnline - comme suit : 
    
  ```
  Test-IRMConfiguration -RMSOnline
  ```

    Entre autres choses, cette applet de commande vérifie la connectivité avec le service Azure Rights Management, télécharge le domaine de publication approuvé et vérifie sa validité.
    
6. Exécutez l’applet de commande [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.150%29.aspx) comme suit pour désactiver des modèles Azure Rights Management soient disponibles dans Outlook sur le web et Outlook : 
    
  ```
  Set-IRMConfiguration -ClientAccessServerEnabled $false
  ```

7. Exécutez l’applet de commande [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.150%29.aspx) comme suit pour activer Azure Rights Management pour votre organisation de messagerie en nuage et le configurer pour utiliser Azure Rights Management pour le chiffrement de messages Office 365 : 
    
  ```
  Set-IRMConfiguration -InternalLicensingEnabled $true
  ```

8. Pour vérifier que vous avez correctement importé le domaine de publication approuvé et activé Azure Rights Management, utilisez l’applet de commande Test-IRMConfiguration pour tester la fonctionnalité Azure Rights Management. Pour plus d’informations, voir « Exemple 1 » dans le [Test-IRMConfiguration](https://technet.microsoft.com/library/dd979798%28v=exchg.150%29.aspx).
    
## <a name="i-have-ome-set-up-with-active-directory-rights-management-not-azure-information-protection-what-do-i-do"></a>Vous avez OME configurée avec Azure pas la Protection des informations Active Directory Rights Management, que dois-je faire ?
<a name="importTPDs"> </a>

Vous pouvez continuer à utiliser vos règles de flux de messagerie Office 365 Message Encryption existantes avec Active Directory Rights Management, mais vous ne pouvez pas configurer ou utiliser les nouvelles fonctionnalités d’OME. Au lieu de cela, vous devez effectuer la migration vers Azure la Protection des informations. Pour plus d’informations sur la migration et ce que cela signifie pour votre organisation, voir [migration à partir d’AD RMS pour la Protection des informations Azure](https://docs.microsoft.com/information-protection/deploy-use/prepare-environment-adrms).
  
## <a name="next-steps"></a>Étapes suivantes
<a name="importTPDs"> </a>

Une fois que vous avez terminé le programme d’installation Azure Rights Management, si vous souhaitez activer les nouvelles fonctionnalités OME, consultez la rubrique [configurer de nouvelles fonctionnalités d’Office 365 Message Encryption greffées Azure la Protection des informations.](https://support.office.com/article/7ff0c040-b25c-4378-9904-b1b50210d00e)
  
Une fois que vous avez configuré votre organisation pour utiliser les nouvelles fonctionnalités OME, vous êtes prêt à des [règles de flux de messagerie définir pour protéger les messages électroniques avec les nouvelles fonctionnalités d’OME](define-mail-flow-rules-to-encrypt-email.md).
  
## <a name="related-topics"></a>Voir aussi
<a name="importTPDs"> </a>

[Chiffrement dans Office 365](encryption.md)
  
[Informations de référence technique de chiffrement dans Office 365](technical-reference-details-about-encryption.md)
  
[What ' s Azure Rights Management ?](https://docs.microsoft.com/information-protection/understand-explore/what-is-azure-rms)
  
