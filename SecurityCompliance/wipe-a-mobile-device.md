---
title: Réinitialiser un appareil mobile dans Office 365
ms.author: dianef
author: dianef77
manager: scotv
ms.date: 6/11/2018
ms.audience: Admin
ms.topic: get-started-article
f1_keywords:
- O365M_WipeDevice
- O365E_WipeDevice
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 9d727c7d-8b47-4499-bf24-d046b449214c
description: Vous pouvez utiliser la gestion intégrée des périphériques mobiles pour Office 365 pour effectuer une réinitialisation à sélective pour supprimer uniquement les informations d’organisation, ou une réinitialisation à distance complet pour supprimer toutes les informations à partir d’un appareil mobile et la restaurer dans ses paramètres d’usine.
ms.openlocfilehash: d3eb28575924ca3bb4a647ae9af2f96b55116a53
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272499"
---
# <a name="wipe-a-mobile-device-in-office-365"></a><span data-ttu-id="65c51-103">Réinitialiser un appareil mobile dans Office 365</span><span class="sxs-lookup"><span data-stu-id="65c51-103">Wipe a mobile device in Office 365</span></span>
  
<span data-ttu-id="65c51-104">Vous pouvez utiliser la gestion intégrée des périphériques mobiles pour Office 365 pour effectuer une réinitialisation à sélective pour supprimer uniquement les informations d’organisation, ou une réinitialisation à distance complet pour supprimer toutes les informations à partir d’un appareil mobile et la restaurer dans ses paramètres d’usine.</span><span class="sxs-lookup"><span data-stu-id="65c51-104">You can use built-in mobile device management for Office 365 to do a selective wipe to remove only organizational information, or a full wipe to delete all information from a mobile device and restore it to its factory settings.</span></span>
  
## <a name="what-to-know-before-you-begin"></a><span data-ttu-id="65c51-105">Éléments à connaître avant de commencer</span><span class="sxs-lookup"><span data-stu-id="65c51-105">What to know before you begin</span></span>

- <span data-ttu-id="65c51-p101">Appareils mobiles peuvent stocker des informations sensibles d’organisation et de fournir un accès aux ressources de votre organisation Office 365. Pour protéger les informations de votre organisation, vous pouvez effectuer une réinitialisation à distance complet ou une réinitialisation sélective à :</span><span class="sxs-lookup"><span data-stu-id="65c51-p101">Mobile devices can store sensitive organizational information and provide access to your organization's Office 365 resources. To help protect your organization's information, you can do a full wipe or a selective wipe:</span></span>
    
  - <span data-ttu-id="65c51-p102">**Réinitialisation à distance complet**: supprime toutes les données sur l’appareil mobile d’un utilisateur, y compris les applications installées, des photos et des informations personnelles. Lors de la transition est terminée, le périphérique est restauré à ses paramètres par défaut.</span><span class="sxs-lookup"><span data-stu-id="65c51-p102">**Full wipe**: Deletes all data on a user's mobile device, including installed applications, photos, and personal information. When the wipe is complete, the device is restored to its factory settings.</span></span> 
    
  - <span data-ttu-id="65c51-110">**Balayage sélective**: supprime uniquement les données d’entreprise et applications laisse installé, photos et des informations personnelles sur l’appareil mobile d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="65c51-110">**Selective wipe**: Removes only organization data and leaves installed applications, photos, and personal information on a user's mobile device.</span></span> 
    
- <span data-ttu-id="65c51-111">Lorsqu’un périphérique est effacé (réinitialisation à distance complète ou sélective réinitialisation à distance), le périphérique est supprimé de la liste des périphériques gérés.</span><span class="sxs-lookup"><span data-stu-id="65c51-111">When a device is wiped (full wipe or selective wipe), the device is removed from the list of managed devices.</span></span>
    
- <span data-ttu-id="65c51-p103">Vous pouvez configurer une stratégie de gestion des appareils mobiles qui efface automatiquement (réinitialisation à distance complet) un périphérique une fois que l’utilisateur ne parvient pas à entrer le mot de passe du périphérique un certain nombre de fois. Suivez les étapes de [créer et déployer des stratégies de sécurité des périphériques](create-device-security-policies.md).</span><span class="sxs-lookup"><span data-stu-id="65c51-p103">You can set up a mobile device management policy that automatically wipes (full wipe) a device after the user unsuccessfully tries to enter the device's password a specific number of times. Follow the steps in [Create and deploy device security policies](create-device-security-policies.md).</span></span>
    
- <span data-ttu-id="65c51-114">Si vous souhaitez en savoir qu’un utilisateur fera l’expérience lorsque vous réinitialiser leur appareil, voir [Quel est l’impact des utilisateurs et des périphériques ?](wipe-a-mobile-device.md#BKMK_Impact).</span><span class="sxs-lookup"><span data-stu-id="65c51-114">If you want to know what a user will experience when you wipe their device, see [What's the user and device impact?](wipe-a-mobile-device.md#BKMK_Impact).</span></span>
    
## <a name="wipe-a-mobile-device"></a><span data-ttu-id="65c51-115">Réinitialiser un appareil mobile</span><span class="sxs-lookup"><span data-stu-id="65c51-115">Wipe a mobile device</span></span>

1. <span data-ttu-id="65c51-116">Accédez à la [ ![cliquez ici pour accéder au centre d’administration Office 365.](media/e00ba917-c3fb-4173-b344-43eb5c7eeb15.png)](https://portal.office.com/adminportal/home).</span><span class="sxs-lookup"><span data-stu-id="65c51-116">Go to the [![Click here to go to the Office 365 admin center.](media/e00ba917-c3fb-4173-b344-43eb5c7eeb15.png)](https://portal.office.com/adminportal/home).</span></span>

2. <span data-ttu-id="65c51-117">Accédez à [accédez à l’Office 365 Security &amp; centre de conformité](https://support.office.com/article/7e696a40-b86b-4a20-afcc-559218b7b1b8) \> **prévention des pertes de données** \> **Gestion des périphériques**.</span><span class="sxs-lookup"><span data-stu-id="65c51-117">Go to [Go to the Office 365 Security &amp; Compliance Center](https://support.office.com/article/7e696a40-b86b-4a20-afcc-559218b7b1b8)\> **Data loss prevention** \> **Device management**.</span></span>
    
3. <span data-ttu-id="65c51-118">Sélectionnez le périphérique que vous souhaitez effacer.</span><span class="sxs-lookup"><span data-stu-id="65c51-118">Select the device you want to wipe.</span></span>
    
4. <span data-ttu-id="65c51-119">Sélectionnez le type de réinitialisation à distance, que vous souhaitez effectuer.</span><span class="sxs-lookup"><span data-stu-id="65c51-119">Select the type of remote wipe you want to do.</span></span>
    
  - <span data-ttu-id="65c51-120">Pour effectuer une réinitialisation à sélective et de supprimer uniquement Office 365 informations sur l’organisation, dans le volet droit, sélectionnez **balayage sélective**.</span><span class="sxs-lookup"><span data-stu-id="65c51-120">To do a selective wipe and delete only Office 365 organization information, in the right pane, select **Selective wipe**.</span></span>
    
  - <span data-ttu-id="65c51-121">Pour effectuer une réinitialisation à distance complet et restaurer le périphérique ses paramètres, dans le volet droit, sélectionnez **complète réinitialisation à distance**.</span><span class="sxs-lookup"><span data-stu-id="65c51-121">To do a full wipe and restore the device to its factory settings, in the right pane, select **Full wipe**.</span></span>
    
![Sélectionnez un périphérique, puis choisissez le type de réinitialisation à faire.](media/ac940abe-0c4a-404e-a842-a1ad2af13ce3.png)
  
5. <span data-ttu-id="65c51-123">Sélectionnez **Oui** pour confirmer.</span><span class="sxs-lookup"><span data-stu-id="65c51-123">Select **Yes** to confirm.</span></span> 
    
<span data-ttu-id="65c51-124">Avant la fin de la transition, l' **état du périphérique** affiche **RetirePending** ou **RetireIssued**.</span><span class="sxs-lookup"><span data-stu-id="65c51-124">Until the wipe finishes, the **Device status** will show as **RetirePending** or **RetireIssued**.</span></span>
  
### <a name="how-do-i-know-it-worked"></a><span data-ttu-id="65c51-125">Comment savoir si qu'elle a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="65c51-125">How do I know it worked?</span></span>

<span data-ttu-id="65c51-126">Vous verrez n’est plus l’appareil mobile dans la liste des périphériques gérés.</span><span class="sxs-lookup"><span data-stu-id="65c51-126">You'll no longer see the mobile device in the list of managed devices.</span></span>
  
## <a name="why-would-you-want-to-wipe-a-device"></a><span data-ttu-id="65c51-127">Pourquoi vous souhaitez réinitialiser un appareil ?</span><span class="sxs-lookup"><span data-stu-id="65c51-127">Why would you want to wipe a device?</span></span>

<span data-ttu-id="65c51-128">Il existe plusieurs raisons pour le nettoyage des périphériques :</span><span class="sxs-lookup"><span data-stu-id="65c51-128">There are several reasons for wiping devices:</span></span>
  
- <span data-ttu-id="65c51-p104">Les appareils mobiles tels que les smartphones et tablettes sont de plus en plus complètes tout le temps. Cela signifie qu’il est plus facile pour vos utilisateurs de stocker des informations sensibles d’entreprise (tels que les données d’identification personnelle ou communications confidentielles) et y accéder en déplacement. Si une de ces appareils mobiles est perdue ou volée, effacement le périphérique immédiatement permet d’éviter les informations de votre organisation à partir de la fin de compte les mains.</span><span class="sxs-lookup"><span data-stu-id="65c51-p104">Mobile devices like smartphones and tablets are becoming more full-featured all the time. This means it's easier for your users to store sensitive corporate information (such as personal identification or confidential communications) and access it on the go. If one of these mobile devices is lost or stolen, wiping the device immediately can help prevent your organization's information from ending up in the wrong hands.</span></span>
    
- <span data-ttu-id="65c51-132">Lorsqu’un utilisateur quitte l’organisation avec un périphérique personnel qui est inscrit dans Mobile Device Manager pour Office 365, vous pouvez empêcher d’organisation des informations avec les utilisateurs en effectuant une réinitialisation à sélective.</span><span class="sxs-lookup"><span data-stu-id="65c51-132">When a user leaves the organization with a personal device that is enrolled in MDM for Office 365, you can help prevent organizational information from going with that user by doing a selective wipe.</span></span>
    
- <span data-ttu-id="65c51-p105">Si votre organisation fournit les appareils mobiles pour les utilisateurs, vous devrez peut-être réaffecter des périphériques à tout moment. Une réinitialisation à distance complet sur un appareil avant de l’assigner à un nouveau permet d’utilisateur ainsi que des informations sensibles à partir du propriétaire précédent sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="65c51-p105">If your organization provides mobile devices to users, you might need to reassign devices from time to time. Doing a full wipe on a device before assigning it to a new user helps ensures that any sensitive information from the previous owner is deleted.</span></span>
    
## <a name="whats-the-user-and-device-impact"></a><span data-ttu-id="65c51-135">Quel est l’utilisateur et l’impact de l’appareil ?</span><span class="sxs-lookup"><span data-stu-id="65c51-135">What's the user and device impact?</span></span>

<span data-ttu-id="65c51-p106">La réinitialisation à distance est immédiatement envoyée à l’appareil mobile. Le périphérique est également marqué comme n’est pas compatible dans DAS.</span><span class="sxs-lookup"><span data-stu-id="65c51-p106">The wipe is sent immediately to the mobile device. The device is also marked as not compliant in AAD.</span></span>
  
<span data-ttu-id="65c51-138">Le tableau suivant décrit le contenu est supprimé pour chaque type de périphérique lorsqu’un périphérique est effacé de manière sélective.</span><span class="sxs-lookup"><span data-stu-id="65c51-138">The following table describes what content is removed for each device type when a device is selectively wiped.</span></span>
  
|<span data-ttu-id="65c51-139">**Impact de contenu**</span><span class="sxs-lookup"><span data-stu-id="65c51-139">**Content impact**</span></span>|<span data-ttu-id="65c51-140">**Windows Phone 8.1**</span><span class="sxs-lookup"><span data-stu-id="65c51-140">**Windows Phone 8.1**</span></span>|<span data-ttu-id="65c51-141">**iOS 7.1+**</span><span class="sxs-lookup"><span data-stu-id="65c51-141">**iOS 7.1+**</span></span>|<span data-ttu-id="65c51-142">**Android 4+**</span><span class="sxs-lookup"><span data-stu-id="65c51-142">**Android 4+**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="65c51-143">Application de portail d’entreprise\* est désinstallé.</span><span class="sxs-lookup"><span data-stu-id="65c51-143">Company Portal app\* is uninstalled.</span></span>  <br/> |<span data-ttu-id="65c51-144">S/O</span><span class="sxs-lookup"><span data-stu-id="65c51-144">N/A</span></span>  <br/> |<span data-ttu-id="65c51-145">✔</span><span class="sxs-lookup"><span data-stu-id="65c51-145">✔</span></span>  <br/> |<span data-ttu-id="65c51-146">S/O</span><span class="sxs-lookup"><span data-stu-id="65c51-146">N/A</span></span>  <br/> |
|<span data-ttu-id="65c51-p107">Données d’application Office 365 hébergées par les applications où le contrôle d’accès est pris en charge par Mobile Device Manager pour Office 365 sont supprimé (actuellement Outlook et OneDrive entreprise). Les applications ne sont pas supprimées.</span><span class="sxs-lookup"><span data-stu-id="65c51-p107">Office 365 app data hosted by apps where access control is supported by MDM for Office 365 is removed (currently Outlook and OneDrive for Business). The apps are not removed.</span></span>  <br/> <span data-ttu-id="65c51-149">Outlook pour Android ne supprime pas les messages électroniques mis en cache.</span><span class="sxs-lookup"><span data-stu-id="65c51-149">Outlook for Android does not remove cached emails.</span></span>  <br/> |<span data-ttu-id="65c51-150">✔</span><span class="sxs-lookup"><span data-stu-id="65c51-150">✔</span></span>  <br/> |<span data-ttu-id="65c51-151">✔</span><span class="sxs-lookup"><span data-stu-id="65c51-151">✔</span></span>  <br/> |<span data-ttu-id="65c51-152">✔</span><span class="sxs-lookup"><span data-stu-id="65c51-152">✔</span></span>  <br/> |
|<span data-ttu-id="65c51-153">Paramètres de stratégie qui ont été appliquées par Mobile Device Manager pour Office 365 pour les périphériques ne s’appliquent plus sur l’appareil et que les utilisateurs peuvent modifier les paramètres.</span><span class="sxs-lookup"><span data-stu-id="65c51-153">Policy settings that were applied by MDM for Office 365 to devices are no longer enforced on the device and users can change the settings.</span></span>  <br/> |<span data-ttu-id="65c51-154">✔</span><span class="sxs-lookup"><span data-stu-id="65c51-154">✔</span></span>  <br/> |<span data-ttu-id="65c51-155">✔</span><span class="sxs-lookup"><span data-stu-id="65c51-155">✔</span></span>  <br/> |<span data-ttu-id="65c51-156">✔</span><span class="sxs-lookup"><span data-stu-id="65c51-156">✔</span></span>  <br/> |
|<span data-ttu-id="65c51-157">Profils de messagerie créés par Mobile Device Manager pour Office 365 sont supprimés et messagerie mis en cache sur le périphérique est supprimé.</span><span class="sxs-lookup"><span data-stu-id="65c51-157">Email profiles created by MDM for Office 365 are removed and cached email on the device is deleted.</span></span>  <br/> |<span data-ttu-id="65c51-158">S/O</span><span class="sxs-lookup"><span data-stu-id="65c51-158">N/A</span></span>  <br/> |<span data-ttu-id="65c51-159">✔</span><span class="sxs-lookup"><span data-stu-id="65c51-159">✔</span></span>  <br/> |<span data-ttu-id="65c51-160">S/O</span><span class="sxs-lookup"><span data-stu-id="65c51-160">N/A</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="65c51-161">\*Application de portail d’entreprise est disponible au niveau de l’App Store pour iOS et le magasin de lecture pour les appareils Android.</span><span class="sxs-lookup"><span data-stu-id="65c51-161">\* Company Portal app is available at the App Store for iOS and the Play Store for Android devices.</span></span> 
  
## <a name="related-content"></a><span data-ttu-id="65c51-162">Contenu connexe</span><span class="sxs-lookup"><span data-stu-id="65c51-162">Related content</span></span>

[<span data-ttu-id="65c51-163">Gérer les appareils mobiles dans Office 365</span><span class="sxs-lookup"><span data-stu-id="65c51-163">Manage mobile devices in Office 365</span></span>](set-up-mobile-device-management.md)
  

