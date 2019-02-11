---
title: Intégrer Office 365 Threat Intelligence à Windows Defender - Protection avancée contre les menaces
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/22/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 414fa693-d7b7-4a1d-a387-ebc3b6a52889
description: Intégrer contre les menaces avancées Office 365 avec Windows Defender avancée protection contre les menaces pour afficher des informations plus détaillées sur la gestion menace.
ms.openlocfilehash: e5070e003972ae5308415dcdcca85b069d1163ac
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29382537"
---
# <a name="integrate-office-365-threat-intelligence-with-windows-defender-advanced-threat-protection"></a><span data-ttu-id="38fa4-103">Intégrer Office 365 Threat Intelligence à Windows Defender - Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="38fa4-103">Integrate Office 365 Threat Intelligence with Windows Defender Advanced Threat Protection</span></span>

<span data-ttu-id="38fa4-p101">Si vous faites partie de l’équipe de sécurité de votre organisation, vous pouvez intégrer les fonctionnalités Office 365 avancée protection contre les menaces et les menaces contre les menaces avancées Windows Defender. Cela peut vous aider à comprendre rapidement si les ordinateurs des utilisateurs sont exposés lorsque vous effectuez des recherches sur les menaces dans Office 365. Par exemple, une fois que l’intégration est activée, vous serez en mesure de voir une liste des ordinateurs qui sont utilisés par les destinataires d’un message électronique détecté, ainsi que la manière dont les alertes récentes de ces ordinateurs ont dans Windows Defender avancée protection contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="38fa4-p101">If you are part of your organization's security team, you can integrate Office 365 Advanced Threat Protection and Threat Intelligence features with Windows Defender Advanced Threat Protection. This can help you quickly understand if users' machines are at risk when you are investigating threats in Office 365. For example, once integration is enabled, you will be able to see a list of machines that are used by the recipients of a detected email message, as well as how many recent alerts those machines have in Windows Defender Advanced Threat Protection.</span></span>
  
<span data-ttu-id="38fa4-107">L’image suivante montre l’onglet **périphériques** qui apparaît lorsque l’intégration Windows Defender avancée protection contre les menaces activée a été :</span><span class="sxs-lookup"><span data-stu-id="38fa4-107">The following image shows the **Devices** tab that you'll see when have Windows Defender Advanced Threat Protection integration enabled:</span></span> 
  
![Lorsque Windows Defender DAV est activé, vous pouvez voir une liste des ordinateurs sur lesquels les alertes.](media/fec928ea-8f0c-44d7-80b9-a2e0a8cd4e89.PNG)
  
<span data-ttu-id="38fa4-p102">Dans cet exemple, vous pouvez voir que les destinataires du message électronique ont quatre périphériques et a une alerte. En cliquant sur le lien pour un périphérique, la page s’ouvre dans le portail Windows Defender avancée protection contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="38fa4-p102">In this example, you can see that the recipients of the email message have four devices and one has an alert. Clicking the link for a device opens its page in the Windows Defender Advanced Threat Protection portal.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="38fa4-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="38fa4-111">Requirements</span></span>

- <span data-ttu-id="38fa4-112">Votre organisation doit avoir des informations sur les menaces Office 365 et Windows Defender DAV.</span><span class="sxs-lookup"><span data-stu-id="38fa4-112">Your organization must have Office 365 Threat Intelligence and Windows Defender ATP.</span></span>
    
- <span data-ttu-id="38fa4-p103">Vous devez être administrateur Global Office 365 ou avoir un rôle d’administrateur de sécurité (comme administrateur de sécurité) affecté dans le [sécurité &amp; centre de conformité](https://protection.office.com). (Voir [les autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md))</span><span class="sxs-lookup"><span data-stu-id="38fa4-p103">You must be an Office 365 Global Administrator or have a security administrator role (such as Security Administrator) assigned in the [Security &amp; Compliance Center](https://protection.office.com). (See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md))</span></span>
    
- <span data-ttu-id="38fa4-115">Vous devez avoir accès à Office 365 menaces et le portail Windows Defender avancée protection contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="38fa4-115">You must have access to both Office 365 Threat Intelligence and the Windows Defender Advanced Threat Protection portal.</span></span>
    
## <a name="to-integrate-office-365-threat-intelligence-with-windows-defender-atp"></a><span data-ttu-id="38fa4-116">Pour intégrer des menaces Office 365 avec Windows Defender DAV</span><span class="sxs-lookup"><span data-stu-id="38fa4-116">To integrate Office 365 Threat Intelligence with Windows Defender ATP</span></span>

<span data-ttu-id="38fa4-117">Intégrer Office 365 menaces contre les menaces avancées Windows Defender est définie à l’aide de deux & Office 365 sécurité Centre de conformité et le portail Windows Defender avancée protection contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="38fa4-117">Integrating Office 365 Threat Intelligence with Windows Defender Advanced Threat Protection is set up by using both the Office 365 Security & Compliance Center AND the Windows Defender Advanced Threat Protection portal.</span></span>
  
1. <span data-ttu-id="38fa4-118">En tant qu’administrateur global Office 365 ou un administrateur de sécurité, accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous avec votre compte professionnel ou de l’école pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="38fa4-118">As an Office 365 global administrator or a security administrator, go to [https://protection.office.com](https://protection.office.com) and sign in with your work or school account for Office 365.</span></span> 
    
2. <span data-ttu-id="38fa4-119">Cliquez sur **Gestion des menaces** \> **Explorer**.</span><span class="sxs-lookup"><span data-stu-id="38fa4-119">Choose **Threat management** \> **Explorer**.</span></span><br><span data-ttu-id="38fa4-120">![Explorateur de solutions dans le menu Gestion des menaces](media/ThreatMgmt-Explorer-nav.png)</span><span class="sxs-lookup"><span data-stu-id="38fa4-120">![Explorer in Threat Management menu](media/ThreatMgmt-Explorer-nav.png)</span></span><br>
    
3. <span data-ttu-id="38fa4-121">Dans le coin supérieur droit de l’écran, choisissez **Paramètres WDATP**.</span><span class="sxs-lookup"><span data-stu-id="38fa4-121">In the upper right corner of the screen, choose **WDATP Settings**.</span></span>
    
4. <span data-ttu-id="38fa4-122">Dans la boîte de dialogue connexion Windows Defender DAV activer sur se connecter à Windows DAV.</span><span class="sxs-lookup"><span data-stu-id="38fa4-122">In the Windows Defender ATP connection dialog box, turn on Connect to Windows ATP.</span></span><br>![Connexion Windows Defender DAV](media/Explorer-WDATPConnection-dialog.png)<br>
    
5. <span data-ttu-id="38fa4-p104">Activer la connexion dans Windows Defender avancée protection contre les menaces. Voir [utilisation du portail Windows Defender avancée protection contre les menaces](https://go.microsoft.com/fwlink/?linkid=859690).</span><span class="sxs-lookup"><span data-stu-id="38fa4-p104">Enable the connection in Windows Defender Advanced Threat Protection. See [Use the Windows Defender Advanced Threat Protection portal](https://go.microsoft.com/fwlink/?linkid=859690).</span></span>

  
## <a name="related-topics"></a><span data-ttu-id="38fa4-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38fa4-126">Related topics</span></span>

[<span data-ttu-id="38fa4-127">Intelligence des menaces d’Office 365</span><span class="sxs-lookup"><span data-stu-id="38fa4-127">Office 365 Threat Intelligence</span></span>](office-365-ti.md)
  
[<span data-ttu-id="38fa4-128">Protection avancée contre les menaces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="38fa4-128">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  

