---
title: Intégrer Office 365 Threat Intelligence à Windows Defender - Protection avancée contre les menaces
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
ms.openlocfilehash: 892d04152d6029c48a52d37c6235d45a8ba67b81
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30222813"
---
# <a name="integrate-office-365-threat-intelligence-with-windows-defender-advanced-threat-protection"></a><span data-ttu-id="6cae4-103">Intégrer Office 365 Threat Intelligence à Windows Defender - Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="6cae4-103">Integrate Office 365 Threat Intelligence with Windows Defender Advanced Threat Protection</span></span>

<span data-ttu-id="6cae4-p101">Si vous êtes membre de l'équipe de sécurité de votre organisation, vous pouvez intégrer les fonctionnalités de protection avancée contre les menaces et d'aide à la décision d'Office 365 avec Windows Defender Advanced Threat Protection. Cela peut vous aider à comprendre rapidement si les ordinateurs des utilisateurs sont exposés lorsque vous étudiez les menaces dans Office 365. Par exemple, une fois que l'intégration est activée, vous pouvez voir la liste des ordinateurs utilisés par les destinataires d'un message électronique détecté, ainsi que le nombre d'alertes récentes de protection avancée contre les menaces Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="6cae4-p101">If you are part of your organization's security team, you can integrate Office 365 Advanced Threat Protection and Threat Intelligence features with Windows Defender Advanced Threat Protection. This can help you quickly understand if users' machines are at risk when you are investigating threats in Office 365. For example, once integration is enabled, you will be able to see a list of machines that are used by the recipients of a detected email message, as well as how many recent alerts those machines have in Windows Defender Advanced Threat Protection.</span></span>
  
<span data-ttu-id="6cae4-107">L'image suivante montre l'onglet **appareils** qui apparaît lorsque l'intégration de la protection avancée contre les menaces Windows Defender est activée:</span><span class="sxs-lookup"><span data-stu-id="6cae4-107">The following image shows the **Devices** tab that you'll see when have Windows Defender Advanced Threat Protection integration enabled:</span></span> 
  
![Lorsque l'ATP Windows Defender est activé, vous pouvez voir une liste des ordinateurs avec des alertes.](media/fec928ea-8f0c-44d7-80b9-a2e0a8cd4e89.PNG)
  
<span data-ttu-id="6cae4-p102">Dans cet exemple, vous pouvez voir que les destinataires du message électronique ont quatre appareils et que l'un d'entre eux comporte une alerte. Cliquer sur le lien d'un appareil ouvre sa page dans le portail protection avancée contre les menaces Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="6cae4-p102">In this example, you can see that the recipients of the email message have four devices and one has an alert. Clicking the link for a device opens its page in the Windows Defender Advanced Threat Protection portal.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="6cae4-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6cae4-111">Requirements</span></span>

- <span data-ttu-id="6cae4-112">Votre organisation doit disposer d'Office 365 Threat Intelligence et de Windows Defender ATP.</span><span class="sxs-lookup"><span data-stu-id="6cae4-112">Your organization must have Office 365 Threat Intelligence and Windows Defender ATP.</span></span>
    
- <span data-ttu-id="6cae4-p103">Vous devez être un administrateur général Office 365 ou disposer d'un rôle d'administrateur de sécurité (tel que administrateur de sécurité) affecté dans le [Centre de sécurité &amp; conformité](https://protection.office.com). (Consultez [la rubrique autorisations dans le centre &amp; de sécurité conformité Office 365](permissions-in-the-security-and-compliance-center.md))</span><span class="sxs-lookup"><span data-stu-id="6cae4-p103">You must be an Office 365 Global Administrator or have a security administrator role (such as Security Administrator) assigned in the [Security &amp; Compliance Center](https://protection.office.com). (See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md))</span></span>
    
- <span data-ttu-id="6cae4-115">Vous devez avoir accès à Office 365 Threat Intelligence et au portail protection avancée contre les menaces Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="6cae4-115">You must have access to both Office 365 Threat Intelligence and the Windows Defender Advanced Threat Protection portal.</span></span>
    
## <a name="to-integrate-office-365-threat-intelligence-with-windows-defender-atp"></a><span data-ttu-id="6cae4-116">Pour intégrer Office 365 Threat Intelligence avec Windows Defender ATP</span><span class="sxs-lookup"><span data-stu-id="6cae4-116">To integrate Office 365 Threat Intelligence with Windows Defender ATP</span></span>

<span data-ttu-id="6cae4-117">L'intégration d'Office 365 Threat Intelligence avec Windows Defender Advanced Threat Protection est configurée à l'aide du centre de sécurité & de sécurité d'Office 365 et du portail protection avancée contre les menaces Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="6cae4-117">Integrating Office 365 Threat Intelligence with Windows Defender Advanced Threat Protection is set up by using both the Office 365 Security & Compliance Center AND the Windows Defender Advanced Threat Protection portal.</span></span>
  
1. <span data-ttu-id="6cae4-118">En tant qu'administrateur général Office 365 ou administrateur de sécurité, accédez [https://protection.office.com](https://protection.office.com) à et connectez-vous avec votre compte professionnel ou scolaire pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="6cae4-118">As an Office 365 global administrator or a security administrator, go to [https://protection.office.com](https://protection.office.com) and sign in with your work or school account for Office 365.</span></span> 
    
2. <span data-ttu-id="6cae4-119">Choisissez \*\*\*\* \> **Explorateur**de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="6cae4-119">Choose **Threat management** \> **Explorer**.</span></span><br><span data-ttu-id="6cae4-120">![Explorateur dans le menu gestion des menaces](media/ThreatMgmt-Explorer-nav.png)</span><span class="sxs-lookup"><span data-stu-id="6cae4-120">![Explorer in Threat Management menu](media/ThreatMgmt-Explorer-nav.png)</span></span><br>
    
3. <span data-ttu-id="6cae4-121">Dans le coin supérieur droit de l'écran, sélectionnez **paramètres WDATP**.</span><span class="sxs-lookup"><span data-stu-id="6cae4-121">In the upper right corner of the screen, choose **WDATP Settings**.</span></span>
    
4. <span data-ttu-id="6cae4-122">Dans la boîte de dialogue connexion Windows Defender ATP, activez connexion à Windows ATP.</span><span class="sxs-lookup"><span data-stu-id="6cae4-122">In the Windows Defender ATP connection dialog box, turn on Connect to Windows ATP.</span></span><br>![Connexion ATP Windows Defender](media/Explorer-WDATPConnection-dialog.png)<br>
    
5. <span data-ttu-id="6cae4-p104">Activez la connexion dans Windows Defender protection avancée contre les menaces. Voir [utiliser le portail protection avancée contre les menaces Windows Defender](https://go.microsoft.com/fwlink/?linkid=859690).</span><span class="sxs-lookup"><span data-stu-id="6cae4-p104">Enable the connection in Windows Defender Advanced Threat Protection. See [Use the Windows Defender Advanced Threat Protection portal](https://go.microsoft.com/fwlink/?linkid=859690).</span></span>

  
## <a name="related-topics"></a><span data-ttu-id="6cae4-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6cae4-126">Related topics</span></span>

[<span data-ttu-id="6cae4-127">Intelligence des menaces d’Office 365</span><span class="sxs-lookup"><span data-stu-id="6cae4-127">Office 365 Threat Intelligence</span></span>](office-365-ti.md)
  
[<span data-ttu-id="6cae4-128">Protection avancée contre les menaces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="6cae4-128">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  

