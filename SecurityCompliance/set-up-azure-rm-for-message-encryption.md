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
# <a name="set-up-azure-rights-management-for-office-365-message-encryption"></a><span data-ttu-id="9a7e7-103">Configurer Azure Rights Management pour le chiffrement de messages Office 365</span><span class="sxs-lookup"><span data-stu-id="9a7e7-103">Set up Azure Rights Management for Office 365 Message Encryption</span></span>

<span data-ttu-id="9a7e7-104">Cette rubrique décrit les étapes à suivre afin d’activer, puis définissez les Azure RMS (Rights Management), partie de la Protection des informations Azure, pour une utilisation avec Office 365 Message Encryption (OME).</span><span class="sxs-lookup"><span data-stu-id="9a7e7-104">This topic describes the steps you need to follow in order to activate and then set up Azure Rights Management (RMS), part of Azure Information Protection, for use with Office 365 Message Encryption (OME).</span></span>
  
## <a name="prerequisites-for-using-office-365-message-encryption"></a><span data-ttu-id="9a7e7-105">Les conditions préalables à l’utilisation du chiffrement des messages Office 365</span><span class="sxs-lookup"><span data-stu-id="9a7e7-105">Prerequisites for using Office 365 Message Encryption</span></span>
<span data-ttu-id="9a7e7-106"><a name="warmprereqs"> </a></span><span class="sxs-lookup"><span data-stu-id="9a7e7-106"></span></span>

<span data-ttu-id="9a7e7-p101">Office 365 Message Encryption (OME), y compris IRM, dépend Azure Rights Management (Services RMS Azure). RMS Azure est la technologie de protection utilisée par la Protection des informations Azure. Pour utiliser OME, votre organisation Office 365 doit inclure un abonnement Exchange Online ou Exchange Online Protection qui, à son tour, inclut un abonnement Azure Rights Management.</span><span class="sxs-lookup"><span data-stu-id="9a7e7-p101">Office 365 Message Encryption (OME), including IRM, depends on Azure Rights Management (Azure RMS). Azure RMS is the protection technology used by Azure Information Protection. To use OME, your Office 365 organization must include an Exchange Online or Exchange Online Protection subscription that, in turn, includes an Azure Rights Management subscription.</span></span>
  
- <span data-ttu-id="9a7e7-110">Si vous n’êtes pas sûr de ce que comprend votre abonnement, consultez les descriptions de service Exchange Online de [Message, de récupération et de conformité](https://technet.microsoft.com/library/exchange-online-message-policy-recovery-and-compliance.aspx).</span><span class="sxs-lookup"><span data-stu-id="9a7e7-110">If you're not sure of what your subscription includes, see the Exchange Online service descriptions for [Message Policy, Recovery, and Compliance](https://technet.microsoft.com/library/exchange-online-message-policy-recovery-and-compliance.aspx).</span></span>
    
- <span data-ttu-id="9a7e7-111">Si vous ne disposez pas un abonnement Azure RMS pour Exchange Online ou Exchange Online Protection, vous devez acheter un abonnement et tout d’abord l’activer.</span><span class="sxs-lookup"><span data-stu-id="9a7e7-111">If you don't have an Azure RMS subscription for Exchange Online or Exchange Online Protection, you must purchase a subscription and activate it first.</span></span>
    
    <span data-ttu-id="9a7e7-p102">Pour plus d’informations sur l’achat d’un abonnement Azure Rights Management, consultez [Azure Rights Management](https://portal.office.com/Signup/MainSignUp15.aspx?&amp;OfferId=9DF77AF9-DAAE-4d51-8E0E-EEEADD4866B8&amp;dl=RIGHTSMANAGEMENT). La section suivante fournit des informations sur l’activation d’Azure Rights Management.</span><span class="sxs-lookup"><span data-stu-id="9a7e7-p102">For information about purchasing a subscription to Azure Rights Management, see [Azure Rights Management](https://portal.office.com/Signup/MainSignUp15.aspx?&amp;OfferId=9DF77AF9-DAAE-4d51-8E0E-EEEADD4866B8&amp;dl=RIGHTSMANAGEMENT). The next section gives you information about activating Azure Rights Management.</span></span>
    
- <span data-ttu-id="9a7e7-114">Si vous avez Azure Rights Management, mais il n’est pas configuré pour Exchange Online ou Exchange Online Protection, cet article explique comment activer Azure Rights Management, puis le décrit la meilleure façon de configurer OME pour fonctionner avec Azure Rights Management.</span><span class="sxs-lookup"><span data-stu-id="9a7e7-114">If you have Azure Rights Management but it's not set up for Exchange Online or Exchange Online Protection, this article explains how to activate Azure Rights Management and then the describes the best way to set up OME to work with Azure Rights Management.</span></span>
    
- <span data-ttu-id="9a7e7-p103">Si vous avez déjà configuré OME pour fonctionner avec Azure Rights Management pour Exchange Online ou Exchange Online Protection, en fonction de la façon dont vous l’avez configuré, il se peut que vous ne soyez prêt à commencer à utiliser immédiatement de OME et ses nouvelles fonctionnalités. Cet article explique comment déterminer si vous avez configuré OME correctement, que faire si vous devez modifier votre configuration et que se passe-t-il si vous choisissez de ne pas modifier votre configuration. Par exemple, pour pouvoir utiliser les nouvelles fonctionnalités, vous devez utiliser RMS Azure avec OME. Vous ne pouvez pas utiliser les nouvelles fonctionnalités avec un Active Directory RMS du local.</span><span class="sxs-lookup"><span data-stu-id="9a7e7-p103">If you've already set up OME to work with Azure Rights Management for Exchange Online or Exchange Online Protection, depending on how you set it up, you may be ready to start using OME and its new capabilities right away. This article explains how to determine if you've set OME up correctly, what to do if you need to change your setup, and what happens if you choose not to change your setup. For example, in order to use the new capabilities, you must use Azure RMS with OME. You can't use the new capabilities with an on-premises Active Directory RMS.</span></span>
    
## <a name="activate-azure-rights-management-for-ome-in-office-365"></a><span data-ttu-id="9a7e7-119">Activer Azure Rights Management pour OME dans Office 365</span><span class="sxs-lookup"><span data-stu-id="9a7e7-119">Activate Azure Rights Management for OME in Office 365</span></span>
<span data-ttu-id="9a7e7-120"><a name="activatewarm"> </a></span><span class="sxs-lookup"><span data-stu-id="9a7e7-120"></span></span>

<span data-ttu-id="9a7e7-p104">Vous devez activer Azure Rights Management afin que les utilisateurs de votre organisation peuvent appliquer la protection des informations aux messages qu’ils envoient et ouvrir des fichiers qui ont été protégés par le service Azure Rights Management et des messages. Pour plus d’informations, voir [Activation Azure Rights Management](https://go.microsoft.com/fwlink/p/?LinkId=525775). Une fois que vous avez terminé l’activation, revenez ici et continuez avec les tâches dans cet article.</span><span class="sxs-lookup"><span data-stu-id="9a7e7-p104">You need to activate Azure Rights Management so that the users in your organization can apply information protection to messages that they send, and open messages and files that have been protected by the Azure Rights Management service. For instructions, see [Activating Azure Rights Management](https://go.microsoft.com/fwlink/p/?LinkId=525775). Once you've completed the activation, return here and continue with the tasks in this article.</span></span>
  
## <a name="set-up-ome-to-use-azure-rms-by-importing-trusted-publishing-domains-tpds"></a><span data-ttu-id="9a7e7-124">Configurer les OME à utiliser RMS Azure en important des domaines de publication approuvés (TPD)</span><span class="sxs-lookup"><span data-stu-id="9a7e7-124">Set up OME to use Azure RMS by importing trusted publishing domains (TPDs)</span></span>
<span data-ttu-id="9a7e7-125"><a name="importTPDs"> </a></span><span class="sxs-lookup"><span data-stu-id="9a7e7-125"></span></span>

<span data-ttu-id="9a7e7-p105">Un domaine de publication approuvé est un fichier XML qui contient des informations sur les paramètres de gestion des droits de votre organisation. Par exemple, le domaine de publication approuvé contient des informations sur le certificat de licence serveur (SLC) utilisé pour signer et chiffrer les certificats et les licences, l’URL utilisée pour la gestion des licences et de publication et ainsi de suite. Vous importez le domaine de publication approuvé dans votre organisation Office 365 à l’aide de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9a7e7-p105">A TPD is an XML file that contains information about your organization's rights management settings. For example, the TPD contains information about the server licensor certificate (SLC) used for signing and encrypting certificates and licenses, the URLs used for licensing and publishing, and so on. You import the TPD into your Office 365 organization by using Windows PowerShell.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="9a7e7-p106">Auparavant, vous pouvez choisir Importer TPD à partir du service Active Directory Rights Management (Services AD RMS) dans votre organisation Office 365. Toutefois, cela vous empêche d’utiliser les nouvelles fonctionnalités OME et n’est pas recommandée. Si Office 365 entreprise est actuellement configuré de cette manière, Microsoft recommande que vous créez un plan de migration à partir de votre Active Directory RMS du local à la Protection des informations Azure basées sur le nuage. Pour plus d’informations, voir [migration à partir d’AD RMS pour la Protection des informations Azure](https://docs.microsoft.com/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms). Vous ne serez pas en mesure d’utiliser les nouvelles fonctionnalités OME jusqu'à ce que vous avez terminé la migration vers Azure la Protection des informations.</span><span class="sxs-lookup"><span data-stu-id="9a7e7-p106">Previously, you could choose to import TPDs from the Active Directory Rights Management service (AD RMS) into your Office 365 organization. However, doing so will prevent you from using the new OME capabilities and is not recommended. If your Office 365 organization is currently configured this way, Microsoft recommends that you create a plan to migrate from your on-premises Active Directory RMS to cloud-based Azure Information Protection. For more information, see [Migrating from AD RMS to Azure Information Protection](https://docs.microsoft.com/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms). You will not be able to use the new OME capabilities until you have completed the migration to Azure Information Protection.</span></span> 
  
 <span data-ttu-id="9a7e7-134">**Pour importer le TPD de RMS Azure**</span><span class="sxs-lookup"><span data-stu-id="9a7e7-134">**To import TPDs from Azure RMS**</span></span>
  
1. <span data-ttu-id="9a7e7-135">[Se connecter à Exchange Online à l’aide de PowerShell à distance](https://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="9a7e7-135">[Connect to Exchange Online Using Remote PowerShell](https://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span></span>
    
2. <span data-ttu-id="9a7e7-136">Choisissez l’URL de partage de clé qui correspond à l’emplacement géographique de votre organisation Office 365 :</span><span class="sxs-lookup"><span data-stu-id="9a7e7-136">Choose the key-sharing URL that corresponds to your Office 365 organization's geographic location:</span></span>
    
|<span data-ttu-id="9a7e7-137">**Emplacement**</span><span class="sxs-lookup"><span data-stu-id="9a7e7-137">**Location**</span></span>|<span data-ttu-id="9a7e7-138">**URL de l’emplacement de partage de clé**</span><span class="sxs-lookup"><span data-stu-id="9a7e7-138">**Key sharing location URL**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9a7e7-139">Amérique du Nord</span><span class="sxs-lookup"><span data-stu-id="9a7e7-139">North America</span></span>  <br/> |https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|<span data-ttu-id="9a7e7-140">Union européenne</span><span class="sxs-lookup"><span data-stu-id="9a7e7-140">European Union</span></span>  <br/> |https://sp-rms.eu.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|<span data-ttu-id="9a7e7-141">Asie</span><span class="sxs-lookup"><span data-stu-id="9a7e7-141">Asia</span></span>  <br/> |https://sp-rms.ap.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|<span data-ttu-id="9a7e7-142">Amérique du Sud</span><span class="sxs-lookup"><span data-stu-id="9a7e7-142">South America</span></span>  <br/> |https://sp-rms.sa.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|<span data-ttu-id="9a7e7-143">Office 365 pour le gouvernement (nuage communautaire propre aux gouvernements)</span><span class="sxs-lookup"><span data-stu-id="9a7e7-143">Office 365 for Government (Government Community Cloud)</span></span>  <br/> <span data-ttu-id="9a7e7-144">Cet emplacement de partage de clé RMS est réservé pour les clients ayant acheté Office 365 pour le gouvernement SKU.</span><span class="sxs-lookup"><span data-stu-id="9a7e7-144">This RMS key-sharing location is reserved for customers who have purchased Office 365 for Government SKUs.</span></span>  <br/> |https://sp-rms.govus.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
   
3. <span data-ttu-id="9a7e7-145">Configurer l’emplacement de partage de clé en exécutant l’applet de commande [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.160%29.aspx) comme suit :</span><span class="sxs-lookup"><span data-stu-id="9a7e7-145">Configure the key-sharing location by running the [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.160%29.aspx) cmdlet as follows:</span></span> 
    
  ```
  Set-IRMConfiguration -RMSOnlineKeySharingLocation "<RMSKeySharingURL >"
  ```

    <span data-ttu-id="9a7e7-146">Par exemple, pour configurer la clé emplacement de partage si votre organisation est située en Amérique du Nord :</span><span class="sxs-lookup"><span data-stu-id="9a7e7-146">For example, to configure the key sharing location if your organization is located in North America:</span></span>
    
  ```
  Set-IRMConfiguration -RMSOnlineKeySharingLocation "https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc"
  ```

4. <span data-ttu-id="9a7e7-147">Exécutez la cmdlet [Import-RMSTrustedPublishingDomain](https://technet.microsoft.com/library/jj200724%28v=exchg.150%29.aspx) avec le commutateur RMSOnline - pour importer le domaine de publication approuvé d’Azure Rights Management :</span><span class="sxs-lookup"><span data-stu-id="9a7e7-147">Run the [Import-RMSTrustedPublishingDomain](https://technet.microsoft.com/library/jj200724%28v=exchg.150%29.aspx) cmdlet with the -RMSOnline switch to import the TPD from Azure Rights Management:</span></span> 
    
  ```
  Import-RMSTrustedPublishingDomain -RMSOnline -Name "<TPDName> "
  ```

    <span data-ttu-id="9a7e7-p107">Où *TPDName* est le nom que vous souhaitez utiliser pour le domaine de publication approuvé. Par exemple, « Contoso Amérique du Nord TPD ».</span><span class="sxs-lookup"><span data-stu-id="9a7e7-p107">Where  *TPDName*  is the name you want to use for the TPD. For example, "Contoso North American TPD".</span></span> 
    
5. <span data-ttu-id="9a7e7-150">Pour vérifier que vous avez configuré correctement votre organisation Office 365 pour utiliser le service Azure Rights Management, exécutez l’applet de commande [Test-IRMConfiguration](https://technet.microsoft.com/library/dd979798%28v=exchg.160%29.aspx) avec le commutateur RMSOnline - comme suit :</span><span class="sxs-lookup"><span data-stu-id="9a7e7-150">To verify that you successfully configured your Office 365 organization to use the Azure Rights Management service, run the [Test-IRMConfiguration](https://technet.microsoft.com/library/dd979798%28v=exchg.160%29.aspx) cmdlet with the -RMSOnline switch as follows:</span></span> 
    
  ```
  Test-IRMConfiguration -RMSOnline
  ```

    <span data-ttu-id="9a7e7-151">Entre autres choses, cette applet de commande vérifie la connectivité avec le service Azure Rights Management, télécharge le domaine de publication approuvé et vérifie sa validité.</span><span class="sxs-lookup"><span data-stu-id="9a7e7-151">Among other things, this cmdlet checks connectivity with the Azure Rights Management service, downloads the TPD, and checks its validity.</span></span>
    
6. <span data-ttu-id="9a7e7-152">Exécutez l’applet de commande [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.150%29.aspx) comme suit pour désactiver des modèles Azure Rights Management soient disponibles dans Outlook sur le web et Outlook :</span><span class="sxs-lookup"><span data-stu-id="9a7e7-152">Run the [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.150%29.aspx) cmdlet as follows to disable Azure Rights Management templates from being available in Outlook on the web and Outlook:</span></span> 
    
  ```
  Set-IRMConfiguration -ClientAccessServerEnabled $false
  ```

7. <span data-ttu-id="9a7e7-153">Exécutez l’applet de commande [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.150%29.aspx) comme suit pour activer Azure Rights Management pour votre organisation de messagerie en nuage et le configurer pour utiliser Azure Rights Management pour le chiffrement de messages Office 365 :</span><span class="sxs-lookup"><span data-stu-id="9a7e7-153">Run the [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.150%29.aspx) cmdlet as follows to enable Azure Rights Management for your cloud-based email organization and configure it to use Azure Rights Management for Office 365 Message Encryption:</span></span> 
    
  ```
  Set-IRMConfiguration -InternalLicensingEnabled $true
  ```

8. <span data-ttu-id="9a7e7-p108">Pour vérifier que vous avez correctement importé le domaine de publication approuvé et activé Azure Rights Management, utilisez l’applet de commande Test-IRMConfiguration pour tester la fonctionnalité Azure Rights Management. Pour plus d’informations, voir « Exemple 1 » dans le [Test-IRMConfiguration](https://technet.microsoft.com/library/dd979798%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="9a7e7-p108">To verify that you have successfully imported the TPD and enabled Azure Rights Management, use the Test-IRMConfiguration cmdlet to test Azure Rights Management functionality. For details, see "Example 1" in [Test-IRMConfiguration](https://technet.microsoft.com/library/dd979798%28v=exchg.150%29.aspx).</span></span>
    
## <a name="i-have-ome-set-up-with-active-directory-rights-management-not-azure-information-protection-what-do-i-do"></a><span data-ttu-id="9a7e7-156">Vous avez OME configurée avec Azure pas la Protection des informations Active Directory Rights Management, que dois-je faire ?</span><span class="sxs-lookup"><span data-stu-id="9a7e7-156">I have OME set up with Active Directory Rights Management not Azure Information Protection, what do I do?</span></span>
<span data-ttu-id="9a7e7-157"><a name="importTPDs"> </a></span><span class="sxs-lookup"><span data-stu-id="9a7e7-157"></span></span>

<span data-ttu-id="9a7e7-p109">Vous pouvez continuer à utiliser vos règles de flux de messagerie Office 365 Message Encryption existantes avec Active Directory Rights Management, mais vous ne pouvez pas configurer ou utiliser les nouvelles fonctionnalités d’OME. Au lieu de cela, vous devez effectuer la migration vers Azure la Protection des informations. Pour plus d’informations sur la migration et ce que cela signifie pour votre organisation, voir [migration à partir d’AD RMS pour la Protection des informations Azure](https://docs.microsoft.com/information-protection/deploy-use/prepare-environment-adrms).</span><span class="sxs-lookup"><span data-stu-id="9a7e7-p109">You can continue to use your existing Office 365 Message Encryption mail flow rules with Active Directory Rights Management, but you can't configure or use the new OME capabilities. Instead, you need to migrate to Azure Information Protection. For information about migration and what this means for your organization, see [Migrating from AD RMS to Azure Information Protection](https://docs.microsoft.com/information-protection/deploy-use/prepare-environment-adrms).</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="9a7e7-161">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="9a7e7-161">Next steps</span></span>
<span data-ttu-id="9a7e7-162"><a name="importTPDs"> </a></span><span class="sxs-lookup"><span data-stu-id="9a7e7-162"></span></span>

<span data-ttu-id="9a7e7-163">Une fois que vous avez terminé le programme d’installation Azure Rights Management, si vous souhaitez activer les nouvelles fonctionnalités OME, consultez la rubrique [configurer de nouvelles fonctionnalités d’Office 365 Message Encryption greffées Azure la Protection des informations.](https://support.office.com/article/7ff0c040-b25c-4378-9904-b1b50210d00e)</span><span class="sxs-lookup"><span data-stu-id="9a7e7-163">Once you've completed Azure Rights Management setup, if you want to enable the new OME capabilities, see [Set up new Office 365 Message Encryption capabilities built on top of Azure Information Protection.](https://support.office.com/article/7ff0c040-b25c-4378-9904-b1b50210d00e)</span></span>
  
<span data-ttu-id="9a7e7-164">Une fois que vous avez configuré votre organisation pour utiliser les nouvelles fonctionnalités OME, vous êtes prêt à des [règles de flux de messagerie définir pour protéger les messages électroniques avec les nouvelles fonctionnalités d’OME](define-mail-flow-rules-to-encrypt-email.md).</span><span class="sxs-lookup"><span data-stu-id="9a7e7-164">After you've set up your organization to use the new OME capabilities, you're ready to [Define mail flow rules to protect email messages with new OME capabilities](define-mail-flow-rules-to-encrypt-email.md).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="9a7e7-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a7e7-165">Related topics</span></span>
<span data-ttu-id="9a7e7-166"><a name="importTPDs"> </a></span><span class="sxs-lookup"><span data-stu-id="9a7e7-166"></span></span>

[<span data-ttu-id="9a7e7-167">Chiffrement dans Office 365</span><span class="sxs-lookup"><span data-stu-id="9a7e7-167">Encryption in Office 365</span></span>](encryption.md)
  
[<span data-ttu-id="9a7e7-168">Informations de référence technique de chiffrement dans Office 365</span><span class="sxs-lookup"><span data-stu-id="9a7e7-168">Technical reference details about encryption in Office 365</span></span>](technical-reference-details-about-encryption.md)
  
[<span data-ttu-id="9a7e7-169">What ' s Azure Rights Management ?</span><span class="sxs-lookup"><span data-stu-id="9a7e7-169">What is Azure Rights Management?</span></span>](https://docs.microsoft.com/information-protection/understand-explore/what-is-azure-rms)
  

