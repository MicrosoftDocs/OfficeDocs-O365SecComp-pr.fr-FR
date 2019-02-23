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
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220454"
---
# <a name="create-an-apns-certificate-for-ios-devices"></a><span data-ttu-id="37979-103">Créer un certificat APNs pour les appareils iOS</span><span class="sxs-lookup"><span data-stu-id="37979-103">Create an APNs Certificate for iOS devices</span></span>

 <span data-ttu-id="37979-104">Pour gérer des appareils iOS comme iPad et iPhone dans la gestion des appareils mobiles pour Office 365, vous devez créer un certificat APNs.</span><span class="sxs-lookup"><span data-stu-id="37979-104">To manage iOS devices like iPad and iPhones in Mobile Device Management for Office 365 you must create an APNs certificate.</span></span> 
  
<span data-ttu-id="37979-p101">Pour ce faire, suivez les étapes indiquées dans le lien **configurer** sur la page du portail. (Accédez à \> **stratégies** \> de sécurité du centre de sécurité \*\* &amp; conformité\*\* **gestion** \> des périphériques **gérer les paramètres**.)</span><span class="sxs-lookup"><span data-stu-id="37979-p101">To do this, follow the steps from the **Set up** link on the portal page. (Go to **Security &amp; Compliance Center** \> **Security policies** \> **Device management** \> **Manage settings**.)</span></span>
  
![Configurer la gestion des appareils mobiles requise et les étapes recommandées](media/d71e3c76-b6b9-4549-ade6-cbfab846d908.png)
  
1. <span data-ttu-id="37979-108">En regard de **configurer un certificat APNs pour les appareils iOS**, sélectionnez **configurer**.</span><span class="sxs-lookup"><span data-stu-id="37979-108">Next to **Configure a APNs Certificate for iOS devices**, select **Set up**.</span></span>
    
2. <span data-ttu-id="37979-109">Sélectionnez **Télécharger votre fichier CSR** et enregistrez la demande de signature de certificat à un endroit de votre ordinateur dont vous vous souviendrez.</span><span class="sxs-lookup"><span data-stu-id="37979-109">Select **Download your CSR file** and save the Certificate signing request to a somewhere on your computer that you'll remember.</span></span> 
    
    ![Boîte de dialogue installer le certificat APN](media/03aa8a24-e95c-4077-9b6b-ef76a86bafd7.png)
  
3. <span data-ttu-id="37979-111">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="37979-111">Select **Next**.</span></span>
    
4. <span data-ttu-id="37979-112">Créez un certificat APN.</span><span class="sxs-lookup"><span data-stu-id="37979-112">Create an APN certificate.</span></span>
    
  - <span data-ttu-id="37979-113">Sélectionnez **Apple APNs Portal** pour ouvrir le portail Appled Certificates.</span><span class="sxs-lookup"><span data-stu-id="37979-113">Select **Apple APNS Portal** to open the Apple Push Certificates Portal.</span></span> 
    
    ![Boîte de dialogue installer le certificat de notification APN avec le portail Apple APNS sélectionné](media/ce19f53c-f44a-470b-baf3-9278dfda2ba5.png)
  
  - <span data-ttu-id="37979-115">Connectez-vous avec un ID Apple.</span><span class="sxs-lookup"><span data-stu-id="37979-115">Sign in with an Apple ID.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="37979-p102">Utilisez l'ID d'une société associée à un compte de messagerie qui restera avec votre organisation, même si l'utilisateur qui gère le compte le quitte. Enregistrez cet ID car vous devrez utiliser le même ID lorsqu'il est temps de renouveler le certificat.</span><span class="sxs-lookup"><span data-stu-id="37979-p102">Use a company Apple ID associated with an email account that will remain with your organization even if the user who manages the account leaves. Save this ID because you'll need to use the same ID when it's time to renew the certificate.</span></span> 
  
  - <span data-ttu-id="37979-118">Sélectionnez **créer un certificat** et accepter les **conditions d'utilisation**.</span><span class="sxs-lookup"><span data-stu-id="37979-118">Select **Create a Certificate** and accept the **Terms of Use**.</span></span>
    
  - <span data-ttu-id="37979-119">**Accédez** à la demande de signature de certificat que vous avez téléchargée sur votre ordinateur à partir d'Office 365 et sélectionnez **Télécharger**.</span><span class="sxs-lookup"><span data-stu-id="37979-119">**Browse** to the Certificate signing request you downloaded to your computer from Office 365 and select **Upload**.</span></span>
    
  - <span data-ttu-id="37979-120">**Téléchargez** le certificat APN créé par le portail de certificats poussés Apple sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="37979-120">**Download** the APN certificate created by the Apple Push Certificate Portal to your computer.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="37979-121">Si vous ne parvenez pas à télécharger le certificat, actualisez votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="37979-121">If you're having trouble downloading the certificate, refresh your browser.</span></span> 
  
5. <span data-ttu-id="37979-122">ReVenez à Office 365 et sélectionnez **suivant** pour accéder à la page **Télécharger le certificat APNs** .</span><span class="sxs-lookup"><span data-stu-id="37979-122">Go back to Office 365 and select **Next** to get to the **Upload APNS certificate** page.</span></span> 
    
6. <span data-ttu-id="37979-123">Accédez au certificat APN que vous avez téléchargé à partir du portail Apple des certificats poussés.</span><span class="sxs-lookup"><span data-stu-id="37979-123">Browse to the APN certificate you downloaded from the Apple Push Certificates Portal.</span></span>
    
    ![Cliquez sur le bouton Parcourir pour sélectionner le certificat APNS que vous avez téléchargé depuis Apple.](media/afe2849d-af23-4c55-9009-d8f25edaf6c0.png)
  
7. <span data-ttu-id="37979-125">Sélectionnez **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="37979-125">Select **Finish**.</span></span>
    
<span data-ttu-id="37979-126">Revenez aux \> **stratégies** \> de sécurité du centre de sécurité \*\* &amp; conformité\*\* **gestion** \> des appareils **gérer les paramètres** pour terminer l'installation.</span><span class="sxs-lookup"><span data-stu-id="37979-126">Go back to **Security &amp; Compliance Center** \> **Security policies** \> **Device management** \> **Manage settings** to complete setup.</span></span> 
  

