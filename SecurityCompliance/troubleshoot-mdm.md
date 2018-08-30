---
title: Résoudre les problèmes d’inscription de périphérique avec Mobile Device Manager pour Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 11/17/2015
ms.audience: Admin
ms.topic: get-started-article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: c863b2bf-45f3-483a-ba05-29fc7f4d6434
description: Si vous exécutez des problèmes lorsque vous tentez d’inscrire un appareil Mobile Device Management (MDM) pour Office 365, essayez les étapes répertoriées ici pour localiser le problème. Si les étapes générales ne résout pas le problème, voir une des sections ultérieure avec les étapes spécifiques pour votre type de périphérique.
ms.openlocfilehash: 490259fc623b38ab5ad6cf8553c5074c77b77426
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272109"
---
# <a name="troubleshoot-device-enrollment-with-mdm-for-office-365"></a><span data-ttu-id="1840f-104">Résoudre les problèmes d’inscription de périphérique avec Mobile Device Manager pour Office 365</span><span class="sxs-lookup"><span data-stu-id="1840f-104">Troubleshoot device enrollment with MDM for Office 365</span></span>

<span data-ttu-id="1840f-p102">Si vous exécutez des problèmes lorsque vous tentez d’inscrire un appareil Mobile Device Management (MDM) pour Office 365, essayez les étapes répertoriées ici pour localiser le problème. Si les étapes générales ne résout pas le problème, voir une des sections ultérieure avec les étapes spécifiques pour votre type de périphérique.</span><span class="sxs-lookup"><span data-stu-id="1840f-p102">If you're running into issues when you try to enroll a device in Mobile Device Management (MDM) for Office 365, try the steps listed here to track down the problem. If the general steps don't fix the issue, see one of the later sections with specific steps for your device type.</span></span>
  
## <a name="steps-to-try-first"></a><span data-ttu-id="1840f-107">Étapes à essayer en premier</span><span class="sxs-lookup"><span data-stu-id="1840f-107">Steps to try first</span></span>

<span data-ttu-id="1840f-108">Pour commencer, vérifiez les points suivants :</span><span class="sxs-lookup"><span data-stu-id="1840f-108">To start, check the following:</span></span>
  
- <span data-ttu-id="1840f-109">Assurez-vous que le périphérique n’est pas déjà inscrit avec un autre fournisseur de gestion des appareils mobiles, tels que Intune.</span><span class="sxs-lookup"><span data-stu-id="1840f-109">Make sure that the device is not already enrolled with another mobile device management provider, such as Intune.</span></span>
    
- <span data-ttu-id="1840f-110">Assurez-vous que le périphérique est défini sur la date et l’heure.</span><span class="sxs-lookup"><span data-stu-id="1840f-110">Make sure that the device is set to the correct date and time.</span></span>
    
- <span data-ttu-id="1840f-111">Basculer vers un autre Wi-Fi ou le réseau cellulaire sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="1840f-111">Switch to a different Wi-Fi or cellular network on the device.</span></span>
    
- <span data-ttu-id="1840f-112">Pour les appareils Android ou iOS, désinstallez et réinstallez l’application de portail d’entreprise Intune sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="1840f-112">For Android or iOS devices, uninstall and reinstall the Intune Company Portal app on the device.</span></span>
    
## <a name="ios-phone-or-tablet"></a><span data-ttu-id="1840f-113">iOS téléphone ou tablette</span><span class="sxs-lookup"><span data-stu-id="1840f-113">iOS phone or tablet</span></span>

- <span data-ttu-id="1840f-114">Assurez-vous que vous avez [configurer un certificat APNs](https://support.office.com/article/522b43f4-a2ff-46f6-962a-dd4f47e546a7).</span><span class="sxs-lookup"><span data-stu-id="1840f-114">Make sure that you've [set up an APNs certificate](https://support.office.com/article/522b43f4-a2ff-46f6-962a-dd4f47e546a7).</span></span>
    
- <span data-ttu-id="1840f-p103">Dans **paramètres** \> **Général** \> **profil** (ou la **Gestion des périphériques**), assurez-vous qu’un **Profil de gestion** n’est pas déjà installé. S’il s’agit, supprimez-le.</span><span class="sxs-lookup"><span data-stu-id="1840f-p103">In **Settings** \> **General** \> **Profile** (or **Device Management**), make sure that a **Management Profile** is not already installed. If it is, remove it.</span></span> 
    
- <span data-ttu-id="1840f-117">Si vous voyez le message d’erreur « Échec du périphérique inscrire, » se connecter à Office 365 et assurez-vous qu’une licence qui inclut Exchange Online a été attribuée à l’utilisateur qui est connecté au périphérique.</span><span class="sxs-lookup"><span data-stu-id="1840f-117">If you see the error message, "Device failed to enroll," sign in to Office 365 and make sure that a license that includes Exchange Online has been assigned to the user who is signed in to the device.</span></span>
    
- <span data-ttu-id="1840f-118">Si vous voyez le message d’erreur « Échec de profil à installer, », essayez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="1840f-118">If you see the error message, "Profile failed to install," try one of the following:</span></span>
    
  - <span data-ttu-id="1840f-119">Assurez-vous que Safari est le navigateur par défaut sur l’appareil et que les cookies ne sont pas désactivés.</span><span class="sxs-lookup"><span data-stu-id="1840f-119">Make sure that Safari is the default browser on the device, and that cookies are not disabled.</span></span>
    
  - <span data-ttu-id="1840f-120">Redémarrer le périphérique, puis accédez à portal.manage.microsoft.com, connectez-vous avec votre ID d’utilisateur Office 365 et le mot de passe et essayer d’installer le profil manuellement.</span><span class="sxs-lookup"><span data-stu-id="1840f-120">Reboot the device, then navigate to portal.manage.microsoft.com, sign in with your Office 365 user ID and password, and attempt to install the profile manually.</span></span>
    
## <a name="windows-rt-tablet"></a><span data-ttu-id="1840f-121">Tablette Windows RT</span><span class="sxs-lookup"><span data-stu-id="1840f-121">Windows RT tablet</span></span>

- <span data-ttu-id="1840f-122">Assurez-vous que votre domaine est [configuré dans Office 365 pour fonctionner avec Mobile Device Manager](set-up-mobile-device-management.md).</span><span class="sxs-lookup"><span data-stu-id="1840f-122">Make sure that your domain is [set up in Office 365 to work with MDM](set-up-mobile-device-management.md).</span></span>
    
- <span data-ttu-id="1840f-123">Assurez-vous que l’utilisateur est choix **Activer** plutôt que de choisir **joindre**.</span><span class="sxs-lookup"><span data-stu-id="1840f-123">Make sure that the user is choosing **Turn On** rather than choosing **Join**.</span></span>
    
## <a name="windows-phone"></a><span data-ttu-id="1840f-124">Windows Phone</span><span class="sxs-lookup"><span data-stu-id="1840f-124">Windows Phone</span></span>

- <span data-ttu-id="1840f-125">Assurez-vous que votre domaine est [configuré dans Office 365 pour fonctionner avec Mobile Device Manager](set-up-mobile-device-management.md).</span><span class="sxs-lookup"><span data-stu-id="1840f-125">Make sure that your domain is [set up in Office 365 to work with MDM](set-up-mobile-device-management.md).</span></span>
    
- <span data-ttu-id="1840f-126">Assurez-vous que le périphérique est en cours d’exécution Windows 8.1 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="1840f-126">Make sure the device is running Windows 8.1 or later.</span></span>
    
## <a name="android-phone-or-tablet"></a><span data-ttu-id="1840f-127">Téléphone Android ou tablette</span><span class="sxs-lookup"><span data-stu-id="1840f-127">Android phone or tablet</span></span>

- <span data-ttu-id="1840f-128">Assurez-vous que le périphérique est en cours d’exécution Android 4.0 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="1840f-128">Make sure the device is running Android 4.0 or later.</span></span>
    
- <span data-ttu-id="1840f-129">Si vous voyez le message d’erreur « Nous n’inscrire ce périphérique, » se connecter à Office 365 et assurez-vous qu’une licence qui inclut Exchange Online a été attribuée à l’utilisateur qui est connecté au périphérique.</span><span class="sxs-lookup"><span data-stu-id="1840f-129">If you see the error message, "We couldn't enroll this device," sign in to Office 365 and make sure that a license that includes Exchange Online has been assigned to the user who is signed in to the device.</span></span>
    
- <span data-ttu-id="1840f-130">Vérifiez la **Zone de Notification** sur le périphérique pour voir si toutes les actions de l’utilisateur final sont en attente et si elles sont, effectuez les actions.</span><span class="sxs-lookup"><span data-stu-id="1840f-130">Check the **Notification Area** on the device to see if any required end-user actions are pending, and if they are, complete the actions.</span></span> 
    

