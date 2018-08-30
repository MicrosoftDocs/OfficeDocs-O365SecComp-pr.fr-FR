---
title: Comment faire pour désactiver la gestion des périphériques mobiles dans Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/12/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- GPA150
- MET150
ms.assetid: 2709cafb-0a8b-44bc-8494-7e2fccfa2b19
description: Suivez ces étapes pour arrêter les stratégies de Mobile Device Manager à partir de la mise en œuvre pour les appareils mobiles dans votre organisation Office 365.
ms.openlocfilehash: 6b8f0036ed999b10263f5cc074df27175769e604
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272219"
---
# <a name="how-to-turn-off-mobile-device-management-in-office-365"></a><span data-ttu-id="5dc7b-103">Comment faire pour désactiver la gestion des périphériques mobiles dans Office 365</span><span class="sxs-lookup"><span data-stu-id="5dc7b-103">How to turn off Mobile Device Management in Office 365</span></span>

<span data-ttu-id="5dc7b-104">Pour désactiver efficacement Mobile Device Manager pour Office 365, vous supprimez des groupes de personnes (défini par les groupes de sécurité) les stratégies de gestion de périphériques, ou supprimez les stratégies eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="5dc7b-104">To effectively turn off MDM for Office 365, you remove groups of people (defined by security groups) from the device management policies, or remove the policies themselves.</span></span> 
  
- <span data-ttu-id="5dc7b-105">Supprimer des groupes d’utilisateurs en supprimant les groupes de sécurité utilisateur à partir des stratégies d’appareil que vous avez créé.</span><span class="sxs-lookup"><span data-stu-id="5dc7b-105">Remove groups of users by removing user security groups from the device policies you've created.</span></span> 
    
- <span data-ttu-id="5dc7b-106">Désactiver Mobile Device Manager pour tout le monde en supprimant toutes les stratégies d’appareil mobile Device Manager.</span><span class="sxs-lookup"><span data-stu-id="5dc7b-106">Disable MDM for everyone by removing all MDM device policies.</span></span> 
    
<span data-ttu-id="5dc7b-p101">Ces options supprimera l’application Mobile Device Manager pour les périphériques de votre organisation. Malheureusement, vous ne pouvez pas simplement « mise hors service « Mobile Device Manager pour Office 365 après que vous l’avez configuré.</span><span class="sxs-lookup"><span data-stu-id="5dc7b-p101">These options will remove MDM enforcement for devices in your organization. Unfortunately, you can't simply "unprovision" MDM for Office 365 after you've set it up.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="5dc7b-p102">N’oubliez pas de l’impact sur les périphériques des utilisateurs lorsque vous supprimez des groupes de sécurité utilisateur de stratégies ou supprimez les stratégies eux-mêmes. Par exemple, les profils de messagerie et les messages électroniques mis en cache peuvent être supprimés, en fonction de l’appareil. Voir : [Quel est l’impact des stratégies de sécurité sur les différents types d’appareils ?](create-device-security-policies.md#what-is-the-impact-of-security-policies-on-different-device-types)</span><span class="sxs-lookup"><span data-stu-id="5dc7b-p102">Be aware of the impact on users' devices when you remove user security groups from policies or remove the policies themselves. For example, email profiles and cached emails may be removed, depending on the device. See: [What is the impact of security policies on different device types?](create-device-security-policies.md#what-is-the-impact-of-security-policies-on-different-device-types)</span></span>
  
## <a name="remove-user-security-groups-from-mdm-device-policies"></a><span data-ttu-id="5dc7b-112">Supprimer des groupes de sécurité utilisateur de stratégies d’appareil mobile Device Manager</span><span class="sxs-lookup"><span data-stu-id="5dc7b-112">Remove user security groups from MDM device policies</span></span>

1. <span data-ttu-id="5dc7b-113">Accédez à **sécurité &amp; centre de conformité** \> **prévention des pertes de données** \> **stratégies de sécurité de l’appareil**.</span><span class="sxs-lookup"><span data-stu-id="5dc7b-113">Go to **Security &amp; Compliance Center**\> **Data loss prevention** \> **Device security polices**.</span></span>
    
2. <span data-ttu-id="5dc7b-114">Sélectionnez une stratégie de périphérique, puis cliquez sur ![icône Modifier](media/O365-MDM-CreatePolicy-EditIcon.gif) **Modifier la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="5dc7b-114">Select a device policy, and click ![Edit icon](media/O365-MDM-CreatePolicy-EditIcon.gif) **Edit policy**.</span></span>
    
3. <span data-ttu-id="5dc7b-115">Sous **déploiement**, cliquez sur **: supprimer**.</span><span class="sxs-lookup"><span data-stu-id="5dc7b-115">Under **Deployment**, click **- Remove**.</span></span>
    
    <span data-ttu-id="5dc7b-116">Sous **groupes**, sélectionnez un groupe de sécurité.</span><span class="sxs-lookup"><span data-stu-id="5dc7b-116">Under **Groups**, select a security group.</span></span>
    
4.  <span data-ttu-id="5dc7b-117">Cliquez sur **Supprimer**.</span><span class="sxs-lookup"><span data-stu-id="5dc7b-117">Click **Remove**.</span></span>
    
5. <span data-ttu-id="5dc7b-118">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="5dc7b-118">Click **Save**.</span></span>
    
## <a name="remove-mdm-device-policies"></a><span data-ttu-id="5dc7b-119">Supprimer des stratégies d’appareil mobile Device Manager</span><span class="sxs-lookup"><span data-stu-id="5dc7b-119">Remove MDM device policies</span></span>

1. <span data-ttu-id="5dc7b-120">Accédez à **sécurité &amp; centre de conformité** \> **stratégies de sécurité** \> **stratégies de sécurité des périphériques**.</span><span class="sxs-lookup"><span data-stu-id="5dc7b-120">Go to **Security &amp; Compliance Center**\> **Security policies** \> **Device security policies**.</span></span>
    
2. <span data-ttu-id="5dc7b-p103">Sélectionnez une stratégie de périphérique, puis cliquez sur ![Image de la Corbeille peut icône. ](media/b8bfa783-c0b5-46d9-9570-8a385088e8fe.png) **Supprimer la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="5dc7b-p103">Select a device policy, and then click ![Image of the trash can icon.](media/b8bfa783-c0b5-46d9-9570-8a385088e8fe.png) **Delete policy**.</span></span>
    
3. <span data-ttu-id="5dc7b-123">Dans la boîte de dialogue **Avertissement** , cliquez sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="5dc7b-123">In the **Warning** dialog, click **Yes**.</span></span> 
    

