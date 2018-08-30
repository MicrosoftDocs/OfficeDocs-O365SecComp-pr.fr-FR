---
title: Créer un certificat APNs pour les appareils iOS
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: 8/5/2016
ms.audience: Admin
ms.topic: get-started-article
f1_keywords:
- O365M_APNCertMDM
- O365E_APNCertMDM
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 522b43f4-a2ff-46f6-962a-dd4f47e546a7
description: Pour gérer les périphériques iOS comme iPad et l’iPhone dans Gestion des périphériques mobiles pour Office 365, procédez comme suit pour créer un certificat APNs.
ms.openlocfilehash: 28e8888d7dd57c3052cdcb5994725f11a5f0445f
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272049"
---
# <a name="create-an-apns-certificate-for-ios-devices"></a><span data-ttu-id="c7cc3-103">Créer un certificat APNs pour les appareils iOS</span><span class="sxs-lookup"><span data-stu-id="c7cc3-103">Create an APNs Certificate for iOS devices</span></span>

 <span data-ttu-id="c7cc3-104">Pour gérer les périphériques iOS comme iPad et l’iPhone dans Gestion des périphériques mobiles pour Office 365, vous devez créer un certificat APNs.</span><span class="sxs-lookup"><span data-stu-id="c7cc3-104">To manage iOS devices like iPad and iPhones in Mobile Device Management for Office 365 you must create an APNs certificate.</span></span> 
  
<span data-ttu-id="c7cc3-p101">Pour ce faire, suivez les étapes à partir du lien **configurer** sur la page du portail. (Atteindre **sécurité &amp; centre de conformité** \> **stratégies de sécurité** \> **Device management** \> **Gérer les paramètres**.)</span><span class="sxs-lookup"><span data-stu-id="c7cc3-p101">To do this, follow the steps from the **Set up** link on the portal page. (Go to **Security &amp; Compliance Center** \> **Security policies** \> **Device management** \> **Manage settings**.)</span></span>
  
![Configurer la gestion des appareils mobiles requis et les étapes recommandées](media/d71e3c76-b6b9-4549-ade6-cbfab846d908.png)
  
1. <span data-ttu-id="c7cc3-108">En regard de **configurer un certificat APNs pour les appareils iOS**, sélectionnez **configurer**.</span><span class="sxs-lookup"><span data-stu-id="c7cc3-108">Next to **Configure a APNs Certificate for iOS devices**, select **Set up**.</span></span>
    
2. <span data-ttu-id="c7cc3-109">Sélectionnez **télécharger votre fichier CSR** et enregistrez la demande de signature de certificat vers un quelque part sur votre ordinateur que vous allez vous souvenir.</span><span class="sxs-lookup"><span data-stu-id="c7cc3-109">Select **Download your CSR file** and save the Certificate signing request to a somewhere on your computer that you'll remember.</span></span> 
    
    ![Installer la boîte de dialogue certificat point](media/03aa8a24-e95c-4077-9b6b-ef76a86bafd7.png)
  
3. <span data-ttu-id="c7cc3-111">Cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="c7cc3-111">Select **Next**.</span></span>
    
4. <span data-ttu-id="c7cc3-112">Créer un certificat de point.</span><span class="sxs-lookup"><span data-stu-id="c7cc3-112">Create an APN certificate.</span></span>
    
  - <span data-ttu-id="c7cc3-113">Sélectionnez **Apple APNS portail** pour ouvrir le portail de certificats Push Apple.</span><span class="sxs-lookup"><span data-stu-id="c7cc3-113">Select **Apple APNS Portal** to open the Apple Push Certificates Portal.</span></span> 
    
    ![Installer point cert boîte de dialogue avec Apple APNS portail sélectionné](media/ce19f53c-f44a-470b-baf3-9278dfda2ba5.png)
  
  - <span data-ttu-id="c7cc3-115">Connectez-vous à l’aide d’un ID d’Apple.</span><span class="sxs-lookup"><span data-stu-id="c7cc3-115">Sign in with an Apple ID.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="c7cc3-p102">Utilisez une société Qu'apple ID associé à un compte de messagerie qui restera avec votre organisation, même si l’utilisateur qui gère le compte. Enregistrez ce code, car vous devez utiliser le même ID lorsqu’il est temps de renouveler le certificat.</span><span class="sxs-lookup"><span data-stu-id="c7cc3-p102">Use a company Apple ID associated with an email account that will remain with your organization even if the user who manages the account leaves. Save this ID because you'll need to use the same ID when it's time to renew the certificate.</span></span> 
  
  - <span data-ttu-id="c7cc3-118">Sélectionnez **créer un certificat** et accepter les **Conditions d’utilisation**.</span><span class="sxs-lookup"><span data-stu-id="c7cc3-118">Select **Create a Certificate** and accept the **Terms of Use**.</span></span>
    
  - <span data-ttu-id="c7cc3-119">**Accédez** à la demande de signature de certificat vous avez téléchargé sur votre ordinateur à partir d’Office 365 et sélectionnez **Télécharger**.</span><span class="sxs-lookup"><span data-stu-id="c7cc3-119">**Browse** to the Certificate signing request you downloaded to your computer from Office 365 and select **Upload**.</span></span>
    
  - <span data-ttu-id="c7cc3-120">**Télécharger** le certificat point créé par le portail de certificat Push Apple à votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c7cc3-120">**Download** the APN certificate created by the Apple Push Certificate Portal to your computer.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="c7cc3-121">Si vous rencontrez des difficultés à télécharger le certificat, actualisez votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="c7cc3-121">If you're having trouble downloading the certificate, refresh your browser.</span></span> 
  
5. <span data-ttu-id="c7cc3-122">Revenir à Office 365, puis cliquez sur **suivant** pour accéder à la page **APNS télécharger le certificat** .</span><span class="sxs-lookup"><span data-stu-id="c7cc3-122">Go back to Office 365 and select **Next** to get to the **Upload APNS certificate** page.</span></span> 
    
6. <span data-ttu-id="c7cc3-123">Recherchez le certificat point que vous avez téléchargé à partir du portail de certificats Push Apple.</span><span class="sxs-lookup"><span data-stu-id="c7cc3-123">Browse to the APN certificate you downloaded from the Apple Push Certificates Portal.</span></span>
    
    ![Cliquez sur le bouton Parcourir pour sélectionner le certificat APNS que vous avez téléchargé à partir d’Apple](media/afe2849d-af23-4c55-9009-d8f25edaf6c0.png)
  
7. <span data-ttu-id="c7cc3-125">Sélectionnez **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="c7cc3-125">Select **Finish**.</span></span>
    
<span data-ttu-id="c7cc3-126">Revenez à **sécurité &amp; centre de conformité** \> **stratégies de sécurité** \> **Device management** \> **Gérer les paramètres** pour terminer l’installation.</span><span class="sxs-lookup"><span data-stu-id="c7cc3-126">Go back to **Security &amp; Compliance Center** \> **Security policies** \> **Device management** \> **Manage settings** to complete setup.</span></span> 
  

