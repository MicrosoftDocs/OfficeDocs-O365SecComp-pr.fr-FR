---
title: Intégrer Office 365 Advanced Threat Protection avec Windows Defender protection avancée contre les menaces
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/22/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 414fa693-d7b7-4a1d-a387-ebc3b6a52889
ms.collection:
- M365-security-compliance
description: Intégrer Office 365 Advanced Threat Protection avec Windows Defender protection avancée contre les menaces pour consulter des informations plus détaillées sur la gestion des menaces.
ms.openlocfilehash: 832b9c6bc600366e1ed6b7c6e60442bec8b5002c
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32254424"
---
# <a name="integrate-office-365-advanced-threat-protection-with-windows-defender-advanced-threat-protection"></a><span data-ttu-id="daee2-103">Intégrer Office 365 Advanced Threat Protection avec Windows Defender protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="daee2-103">Integrate Office 365 Advanced Threat Protection with Windows Defender Advanced Threat Protection</span></span>

<span data-ttu-id="daee2-104">Si vous êtes membre de l'équipe de sécurité de votre organisation, vous pouvez intégrer Office 365 Advanced Threat Protection et les fonctionnalités d'enquête et de réponse associées avec Windows Defender Advanced Threat Protection.</span><span class="sxs-lookup"><span data-stu-id="daee2-104">If you are part of your organization's security team, you can integrate Office 365 Advanced Threat Protection and related investigation and response features with Windows Defender Advanced Threat Protection.</span></span> <span data-ttu-id="daee2-105">Cela peut vous aider à comprendre rapidement si les ordinateurs des utilisateurs sont exposés lorsque vous étudiez les menaces dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="daee2-105">This can help you quickly understand if users' machines are at risk when you are investigating threats in Office 365.</span></span> <span data-ttu-id="daee2-106">Par exemple, une fois que l'intégration est activée, vous pouvez voir la liste des ordinateurs utilisés par les destinataires d'un message électronique détecté, ainsi que le nombre d'alertes récentes de protection avancée contre les menaces Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="daee2-106">For example, once integration is enabled, you will be able to see a list of machines that are used by the recipients of a detected email message, as well as how many recent alerts those machines have in Windows Defender Advanced Threat Protection.</span></span>
  
<span data-ttu-id="daee2-107">L'image suivante montre l'onglet **appareils** qui apparaît lorsque l'intégration de la protection avancée contre les menaces Windows Defender est activée:</span><span class="sxs-lookup"><span data-stu-id="daee2-107">The following image shows the **Devices** tab that you'll see when have Windows Defender Advanced Threat Protection integration enabled:</span></span> 
  
![Lorsque l'ATP Windows Defender est activé, vous pouvez voir une liste des ordinateurs avec des alertes.](media/fec928ea-8f0c-44d7-80b9-a2e0a8cd4e89.PNG)
  
<span data-ttu-id="daee2-109">Dans cet exemple, vous pouvez voir que les destinataires du message électronique ont quatre appareils et que l'un d'entre eux comporte une alerte.</span><span class="sxs-lookup"><span data-stu-id="daee2-109">In this example, you can see that the recipients of the email message have four devices and one has an alert.</span></span> <span data-ttu-id="daee2-110">Cliquer sur le lien d'un appareil ouvre sa page dans le portail protection avancée contre les menaces Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="daee2-110">Clicking the link for a device opens its page in the Windows Defender Advanced Threat Protection portal.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="daee2-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="daee2-111">Requirements</span></span>

- <span data-ttu-id="daee2-112">Votre organisation doit avoir Office 365 Advanced Threat Protection Plan 2 (ou Office 365 E5) et Windows Defender ATP.</span><span class="sxs-lookup"><span data-stu-id="daee2-112">Your organization must have Office 365 Advanced Threat Protection Plan 2 (or Office 365 E5) and Windows Defender ATP.</span></span>
    
- <span data-ttu-id="daee2-113">Vous devez être un administrateur général Office 365 ou disposer d'un rôle d'administrateur de sécurité (tel que administrateur de sécurité) affecté dans le [Centre de sécurité &amp; conformité](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="daee2-113">You must be an Office 365 Global Administrator or have a security administrator role (such as Security Administrator) assigned in the [Security &amp; Compliance Center](https://protection.office.com).</span></span> <span data-ttu-id="daee2-114">(Consultez [la rubrique autorisations dans le centre &amp; de sécurité conformité Office 365](permissions-in-the-security-and-compliance-center.md))</span><span class="sxs-lookup"><span data-stu-id="daee2-114">(See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md))</span></span>
    
- <span data-ttu-id="daee2-115">Vous devez avoir accès à Office 365 Threat Explorer dans le centre de sécurité & Compliance Center et au portail protection avancée contre les menaces Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="daee2-115">You must have access to both Office 365 Threat Explorer in the Security & Compliance Center and the Windows Defender Advanced Threat Protection portal.</span></span>
    
## <a name="to-integrate-office-365-advanced-threat-protection-with-windows-defender-atp"></a><span data-ttu-id="daee2-116">Pour intégrer Office 365 Advanced Threat Protection avec Windows Defender ATP</span><span class="sxs-lookup"><span data-stu-id="daee2-116">To integrate Office 365 Advanced Threat Protection with Windows Defender ATP</span></span>

<span data-ttu-id="daee2-117">L'intégration de la protection avancée contre les menaces Office 365 avec Windows Defender Advanced Threat Protection est configurée à l'aide du centre de sécurité & Compliance Center et du portail de protection avancée contre les menaces Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="daee2-117">Integrating Office 365 Advanced Threat Protection with Windows Defender Advanced Threat Protection is set up by using both the Security & Compliance Center AND the Windows Defender Advanced Threat Protection portal.</span></span>
  
1. <span data-ttu-id="daee2-118">En tant qu'administrateur général Office 365 ou administrateur de sécurité, accédez [https://protection.office.com](https://protection.office.com) à et connectez-vous avec votre compte professionnel ou scolaire pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="daee2-118">As an Office 365 global administrator or a security administrator, go to [https://protection.office.com](https://protection.office.com) and sign in with your work or school account for Office 365.</span></span> 
    
2. <span data-ttu-id="daee2-119">Choisissez \*\*\*\* \> **Explorateur**de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="daee2-119">Choose **Threat management** \> **Explorer**.</span></span><br><span data-ttu-id="daee2-120">![Explorateur dans le menu gestion des menaces](media/ThreatMgmt-Explorer-nav.png)</span><span class="sxs-lookup"><span data-stu-id="daee2-120">![Explorer in Threat Management menu](media/ThreatMgmt-Explorer-nav.png)</span></span><br>
    
3. <span data-ttu-id="daee2-121">Dans le coin supérieur droit de l'écran, sélectionnez **paramètres WDATP**.</span><span class="sxs-lookup"><span data-stu-id="daee2-121">In the upper right corner of the screen, choose **WDATP Settings**.</span></span>
    
4. <span data-ttu-id="daee2-122">Dans la boîte de dialogue connexion Windows Defender ATP, activez connexion à Windows ATP.</span><span class="sxs-lookup"><span data-stu-id="daee2-122">In the Windows Defender ATP connection dialog box, turn on Connect to Windows ATP.</span></span><br>![Connexion ATP Windows Defender](media/Explorer-WDATPConnection-dialog.png)<br>
    
5. <span data-ttu-id="daee2-124">Activez la connexion dans Windows Defender protection avancée contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="daee2-124">Enable the connection in Windows Defender Advanced Threat Protection.</span></span> <span data-ttu-id="daee2-125">Voir [utiliser le portail protection avancée contre les menaces Windows Defender](https://go.microsoft.com/fwlink/?linkid=859690).</span><span class="sxs-lookup"><span data-stu-id="daee2-125">See [Use the Windows Defender Advanced Threat Protection portal](https://go.microsoft.com/fwlink/?linkid=859690).</span></span>

  
## <a name="related-topics"></a><span data-ttu-id="daee2-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="daee2-126">Related topics</span></span>

[<span data-ttu-id="daee2-127">Enquête et réponse aux menaces Office 365</span><span class="sxs-lookup"><span data-stu-id="daee2-127">Office 365 Threat Investigation and Response</span></span>](office-365-ti.md)
  
[<span data-ttu-id="daee2-128">Office 365-Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="daee2-128">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  

