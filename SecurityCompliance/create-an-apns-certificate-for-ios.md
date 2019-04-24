---
title: Créer un certificat APNs pour les appareils iOS
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: 8/5/2016
ms.audience: Admin
ms.topic: article
f1_keywords:
- O365M_APNCertMDM
- O365E_APNCertMDM
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 522b43f4-a2ff-46f6-962a-dd4f47e546a7
description: Pour gérer les appareils iOS comme iPad et iPhone dans la gestion des appareils mobiles pour Office 365, procédez comme suit pour créer d'abord un certificat APNs.
ms.openlocfilehash: 5f82690f0add5f1aae95a089d9cdfc0b320ae596
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32258618"
---
# <a name="create-an-apns-certificate-for-ios-devices"></a><span data-ttu-id="95fb6-103">Créer un certificat APNs pour les appareils iOS</span><span class="sxs-lookup"><span data-stu-id="95fb6-103">Create an APNs Certificate for iOS devices</span></span>

 <span data-ttu-id="95fb6-104">Pour gérer des appareils iOS comme iPad et iPhone dans la gestion des appareils mobiles pour Office 365, vous devez créer un certificat APNs.</span><span class="sxs-lookup"><span data-stu-id="95fb6-104">To manage iOS devices like iPad and iPhones in Mobile Device Management for Office 365 you must create an APNs certificate.</span></span> 
  
<span data-ttu-id="95fb6-105">Pour ce faire, suivez les étapes indiquées dans le lien **configurer** sur la page du portail.</span><span class="sxs-lookup"><span data-stu-id="95fb6-105">To do this, follow the steps from the **Set up** link on the portal page.</span></span> <span data-ttu-id="95fb6-106">(Accédez à \> **stratégies** \> de sécurité du centre de sécurité \*\* &amp; conformité\*\* **gestion** \> des périphériques **gérer les paramètres**.)</span><span class="sxs-lookup"><span data-stu-id="95fb6-106">(Go to **Security &amp; Compliance Center** \> **Security policies** \> **Device management** \> **Manage settings**.)</span></span>
  
![Configurer la gestion des appareils mobiles requise et les étapes recommandées](media/d71e3c76-b6b9-4549-ade6-cbfab846d908.png)
  
1. <span data-ttu-id="95fb6-108">Next to **Configure a APNs Certificate for iOS devices**, select **Set up**.</span><span class="sxs-lookup"><span data-stu-id="95fb6-108">Next to **Configure a APNs Certificate for iOS devices**, select **Set up**.</span></span>
    
2. <span data-ttu-id="95fb6-109">Select **Download your CSR file** and save the Certificate signing request to a somewhere on your computer that you'll remember.</span><span class="sxs-lookup"><span data-stu-id="95fb6-109">Select **Download your CSR file** and save the Certificate signing request to a somewhere on your computer that you'll remember.</span></span> 
    
    ![Boîte de dialogue installer le certificat APN](media/03aa8a24-e95c-4077-9b6b-ef76a86bafd7.png)
  
3. <span data-ttu-id="95fb6-111"> Select *\*Next*\*. </span><span class="sxs-lookup"><span data-stu-id="95fb6-111">Select **Next**.</span></span>
    
4. <span data-ttu-id="95fb6-112"> Create an APN certificate.</span><span class="sxs-lookup"><span data-stu-id="95fb6-112">Create an APN certificate.</span></span>
    
  - <span data-ttu-id="95fb6-113">Select **Apple APNS Portal** to open the Apple Push Certificates Portal. </span><span class="sxs-lookup"><span data-stu-id="95fb6-113">Select **Apple APNS Portal** to open the Apple Push Certificates Portal.</span></span> 
    
    ![Boîte de dialogue installer le certificat de notification APN avec le portail Apple APNS sélectionné](media/ce19f53c-f44a-470b-baf3-9278dfda2ba5.png)
  
  - <span data-ttu-id="95fb6-115">Sign in with an Apple ID.</span><span class="sxs-lookup"><span data-stu-id="95fb6-115">Sign in with an Apple ID.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="95fb6-p102">Use a company Apple ID associated with an email account that will remain with your organization even if the user who manages the account leaves. Save this ID because you'll need to use the same ID when it's time to renew the certificate.</span><span class="sxs-lookup"><span data-stu-id="95fb6-p102">Use a company Apple ID associated with an email account that will remain with your organization even if the user who manages the account leaves. Save this ID because you'll need to use the same ID when it's time to renew the certificate.</span></span> 
  
  - <span data-ttu-id="95fb6-118">Select **Create a Certificate** and accept the **Terms of Use**.</span><span class="sxs-lookup"><span data-stu-id="95fb6-118">Select **Create a Certificate** and accept the **Terms of Use**.</span></span>
    
  - <span data-ttu-id="95fb6-119">**Browse** to the Certificate signing request you downloaded to your computer from Office 365 and select **Upload**.</span><span class="sxs-lookup"><span data-stu-id="95fb6-119">**Browse** to the Certificate signing request you downloaded to your computer from Office 365 and select **Upload**.</span></span>
    
  - <span data-ttu-id="95fb6-120">**Download** the APN certificate created by the Apple Push Certificate Portal to your computer.</span><span class="sxs-lookup"><span data-stu-id="95fb6-120">**Download** the APN certificate created by the Apple Push Certificate Portal to your computer.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="95fb6-121">If you're having trouble downloading the certificate, refresh your browser.</span><span class="sxs-lookup"><span data-stu-id="95fb6-121">If you're having trouble downloading the certificate, refresh your browser.</span></span> 
  
5. <span data-ttu-id="95fb6-122">Go back to Office 365 and select **Next** to get to the **Upload APNS certificate** page.</span><span class="sxs-lookup"><span data-stu-id="95fb6-122">Go back to Office 365 and select **Next** to get to the **Upload APNS certificate** page.</span></span> 
    
6. <span data-ttu-id="95fb6-123"> Browse to the APN certificate you downloaded from the Apple Push Certificates Portal.</span><span class="sxs-lookup"><span data-stu-id="95fb6-123">Browse to the APN certificate you downloaded from the Apple Push Certificates Portal.</span></span>
    
    ![Cliquez sur le bouton Parcourir pour sélectionner le certificat APNS que vous avez téléchargé depuis Apple.](media/afe2849d-af23-4c55-9009-d8f25edaf6c0.png)
  
7. <span data-ttu-id="95fb6-125">Select **Finish**.</span><span class="sxs-lookup"><span data-stu-id="95fb6-125">Select **Finish**.</span></span>
    
<span data-ttu-id="95fb6-126">Revenez aux \> **stratégies** \> de sécurité du centre de sécurité \*\* &amp; conformité\*\* **gestion** \> des appareils **gérer les paramètres** pour terminer l'installation.</span><span class="sxs-lookup"><span data-stu-id="95fb6-126">Go back to **Security &amp; Compliance Center** \> **Security policies** \> **Device management** \> **Manage settings** to complete setup.</span></span> 
  

