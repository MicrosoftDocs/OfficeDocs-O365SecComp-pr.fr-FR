---
title: Vue d’ensemble de la gestion des appareils mobiles (Mobile Device Manager) pour Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: overview
f1_keywords:
- O365M_MDMConfigDomains
- O365E_MDMConfigDomains
- ms.o365.cc.DevicePolicy
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: faa7d8e5-645d-4d59-839c-c8d4c1869e4a
description: Vous pouvez gérer et sécuriser les périphériques mobiles s’ils étaient connectés à votre organisation Office 365 à l’aide de la gestion des périphériques mobiles pour Office 365. Les appareils mobiles tels que les smartphones et tablettes qui servent à accéder aux travail courrier, calendrier, contacts et documents lire une grande partie de s’assurer que les employés effectuer leur travail et à tout moment, depuis n’importe où. Il est donc essentiel que vous aider à protéger les informations de votre organisation lorsque des personnes utilisent des périphériques. Vous pouvez utiliser Mobile Device Manager pour Office 365 pour définir des règles d’accès et les stratégies de sécurité des appareils et pour réinitialiser les appareils mobiles s’ils sont perdus ou volés.
ms.openlocfilehash: f06cef11b68ee0673f13c54738f07f4556495fdd
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272489"
---
# <a name="overview-of-mobile-device-management-mdm-for-office-365"></a><span data-ttu-id="defb8-106">Vue d’ensemble de la gestion des appareils mobiles (Mobile Device Manager) pour Office 365</span><span class="sxs-lookup"><span data-stu-id="defb8-106">Overview of Mobile Device Management (MDM) for Office 365</span></span>

<span data-ttu-id="defb8-p102">Vous pouvez gérer et sécuriser les périphériques mobiles s’ils étaient connectés à votre organisation Office 365 à l’aide de la gestion des périphériques mobiles pour Office 365. Les appareils mobiles tels que les smartphones et tablettes qui servent à accéder aux travail courrier, calendrier, contacts et documents lire une grande partie de s’assurer que les employés effectuer leur travail et à tout moment, depuis n’importe où. Il est donc essentiel que vous aider à protéger les informations de votre organisation lorsque des personnes utilisent des périphériques. Vous pouvez utiliser Mobile Device Manager pour Office 365 pour définir des règles d’accès et les stratégies de sécurité des appareils et pour réinitialiser les appareils mobiles s’ils sont perdus ou volés.</span><span class="sxs-lookup"><span data-stu-id="defb8-p102">You can manage and secure mobile devices when they're connected to your Office 365 organization by using Mobile Device Management for Office 365. Mobile devices like smartphones and tablets that are used to access work email, calendar, contacts, and documents play a big part in making sure that employees get their work done anytime, from anywhere. So it's critical that you help protect your organization's information when people use devices. You can use MDM for Office 365 to set device security policies and access rules, and to wipe mobile devices if they're lost or stolen.</span></span>
  
![Mobile Device Manager sur le téléphone Android](media/69b9a9f6-13ac-4e36-99ca-95e82e0375aa.png)
  
## <a name="what-types-of-devices-can-you-manage"></a><span data-ttu-id="defb8-112">Quels types d’appareils pouvez-vous gérer ?</span><span class="sxs-lookup"><span data-stu-id="defb8-112">What types of devices can you manage?</span></span>

<span data-ttu-id="defb8-p103">Vous pouvez utiliser Mobile Device Manager pour Office 365 pour gérer plusieurs types d’appareils mobiles tels que Windows Phone, Android, iPhone et iPad. Pour gérer les appareils mobiles utilisés par des personnes dans votre organisation, chaque personne doit avoir une licence Office 365 applicable et leur appareil doit être inscrit dans Mobile Device Manager pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="defb8-p103">You can use MDM for Office 365 to manage many types of mobile devices like Windows Phone, Android, iPhone, and iPad. To manage mobile devices used by people in your organization, each person must have an applicable Office 365 license and their device must be enrolled in MDM for Office 365.</span></span> 
  
<span data-ttu-id="defb8-115">Pour voir quel Mobile Device Manager pour Office 365 prend en charge pour chaque type de périphérique, voir [Fonctionnalités de gestion des périphériques mobiles pour Office 365](capabilities-of-mobile-device-management.md).</span><span class="sxs-lookup"><span data-stu-id="defb8-115">To see what MDM for Office 365 supports for each type of device, see [Capabilities of Mobile Device Management for Office 365](capabilities-of-mobile-device-management.md).</span></span>
  
## <a name="setup-steps-for-mdm"></a><span data-ttu-id="defb8-116">Étapes de configuration pour Mobile Device Manager</span><span class="sxs-lookup"><span data-stu-id="defb8-116">Setup steps for MDM</span></span>

<span data-ttu-id="defb8-p104">Un administrateur global d’Office 365 doit effectuer les étapes suivantes pour activer et configurer Mobile Device Manager pour Office 365. Suivez les instructions de la rubrique sur [la configuration de Mobile Device Manager pour Office 365](set-up-mobile-device-management.md) pour voir la procédure détaillée. Voici un résumé rapide :</span><span class="sxs-lookup"><span data-stu-id="defb8-p104">An Office 365 global admin must complete the following steps to activate and set up MDM for Office 365. Follow the guidance in the topic on [setting up MDM for Office 365](set-up-mobile-device-management.md) to see detailed steps. Here's a quick summary:</span></span> 
  
> <span data-ttu-id="defb8-120">Étape 1 : Activer Mobile Device Manager pour Office 365 en suivant les étapes de la [valeur up Mobile Device Management (MDM) dans Office 365](set-up-mobile-device-management.md).</span><span class="sxs-lookup"><span data-stu-id="defb8-120">Step 1: Activate MDM for Office 365 by following steps in the [Set up Mobile Device Management (MDM) in Office 365](set-up-mobile-device-management.md).</span></span>
    
> <span data-ttu-id="defb8-121">Étape 2 : Configurer Mobile Device Manager pour Office 365, par exemple, création d’un certificat APNs pour gérer les appareils iOS et ajout d’un enregistrement de nom de domaine DNS (Domain Name System) pour votre domaine prendre en charge Windows Phone.</span><span class="sxs-lookup"><span data-stu-id="defb8-121">Step 2: Set up MDM for Office 365 by, for example, creating an APNs certificate to manage iOS devices and adding a Domain Name System (DNS) record for your domain to support Windows phones.</span></span>
    
> <span data-ttu-id="defb8-p105">Étape 3 : Créer des stratégies d’appareil et les appliquer à des groupes d’utilisateurs. Lorsque vous effectuez cette opération, vos utilisateurs obtiendrez un [message d’inscription sur leur appareil](enroll-your-mobile-device.md). Et lorsqu’ils réalisé l’inscription, leurs appareils seront limitées par les stratégies que vous avez configuré les.</span><span class="sxs-lookup"><span data-stu-id="defb8-p105">Step 3: Create device policies and apply them to groups of users. When you do this, your users will get an [enrollment message on their device](enroll-your-mobile-device.md). And when they've completed enrollment, their devices will be restricted by the policies you've set up for them.</span></span>
    
    ![Creating an MDN device policy under Device security policies](media/fbcdbecd-0016-42f1-81a9-9fbad610da90.png)
  
## <a name="device-management-tasks"></a><span data-ttu-id="defb8-125">Tâches de gestion des périphériques</span><span class="sxs-lookup"><span data-stu-id="defb8-125">Device management tasks</span></span>

<span data-ttu-id="defb8-p106">Une fois que vous avez Mobile Device Manager pour Office 365, configurer et vos utilisateurs ont inscrit leurs périphériques, vous pouvez gérer les périphériques, bloquez l’accès ou réinitialiser un appareil, si nécessaire. Pour plus d’informations sur [certaines tâches courantes de gestion des périphériques](manage-devices-in-mdm.md), y compris where effectuer les tâches.</span><span class="sxs-lookup"><span data-stu-id="defb8-p106">After you've got MDM for Office 365 set up and your users have enrolled their devices, you can manage the devices, block access, or wipe a device, if needed. Learn more about [some common device management tasks](manage-devices-in-mdm.md), including where to complete the tasks.</span></span>
  
## <a name="other-ways-to-manage-devices-and-apps"></a><span data-ttu-id="defb8-128">Autres méthodes de gestion des applications et des périphériques</span><span class="sxs-lookup"><span data-stu-id="defb8-128">Other ways to manage devices and apps</span></span>

<span data-ttu-id="defb8-129">Si vous avez besoin de plus de fonctionnalités Mobile Device Manager pour Office 365 inclut, extraire cette [comparaison des fonctionnalités de Mobile Device Manager et Microsoft Intune](choose-between-mdm-and-intune.md) pour voir si un abonnement Intune doit répondre aux besoins de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="defb8-129">If you need more functionality than MDM for Office 365 includes, check out this [comparison of MDM and Microsoft Intune features](choose-between-mdm-and-intune.md) to see if an Intune subscription would meet your organization's needs.</span></span> 
  
<span data-ttu-id="defb8-p107">Si vous devez simplement la gestion des applications mobiles (MAM), par exemple des personnes de mise à jour des projets de travail sur leurs appareils, Intune fournit une autre option outre l’inscription et la gestion des périphériques. Un abonnement Intune vous permet de configurer les stratégies MAM à l’aide du portail Azure, même si les périphériques de personnes ne sont pas inscrits dans Intune. Voir [protéger les données d’application à l’aide de stratégies MAM](https://go.microsoft.com/fwlink/?LinkId=825439).</span><span class="sxs-lookup"><span data-stu-id="defb8-p107">If you just need mobile app management (MAM), perhaps for people updating work projects on their own devices, Intune provides another option besides enrolling and managing devices. An Intune subscription allows you to set up MAM policies by using the Azure portal, even if people's devices aren't enrolled in Intune. See [Protect app data using MAM policies](https://go.microsoft.com/fwlink/?LinkId=825439).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="defb8-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="defb8-133">See also</span></span>

[<span data-ttu-id="defb8-134">Obtenir plus d’informations sur les périphériques gérés par Mobile Device Manager</span><span class="sxs-lookup"><span data-stu-id="defb8-134">Get details about devices managed by MDM</span></span>](get-details-about-mdm-managed-devices.md)

[<span data-ttu-id="defb8-135">Configurer Mobile Device Manager pour Office 365</span><span class="sxs-lookup"><span data-stu-id="defb8-135">Set up MDM for Office 365</span></span>](set-up-mobile-device-management.md)
  
[<span data-ttu-id="defb8-136">Inscrire les appareils mobiles dans Mobile Device Manager</span><span class="sxs-lookup"><span data-stu-id="defb8-136">Enroll mobile devices in MDM</span></span>](enroll-your-mobile-device.md)
  
[<span data-ttu-id="defb8-137">Gérer les périphériques inscrits dans Mobile Device Manager</span><span class="sxs-lookup"><span data-stu-id="defb8-137">Manage devices enrolled in MDM</span></span>](manage-devices-in-mdm.md)

