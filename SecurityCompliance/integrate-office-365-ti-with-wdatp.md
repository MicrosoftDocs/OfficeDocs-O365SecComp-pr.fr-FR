---
title: Intégrer Office 365 Threat Intelligence à Windows Defender - Protection avancée contre les menaces
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 3/21/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 414fa693-d7b7-4a1d-a387-ebc3b6a52889
description: Intégrer contre les menaces avancées Office 365 avec Windows Defender avancée protection contre les menaces pour afficher des informations plus détaillées sur la gestion menace.
ms.openlocfilehash: 1198f53c47811d69b93106c413e3d3a09d83e736
ms.sourcegitcommit: 2cf7f5bb282c971d33e00f65d9982a3f14aec74e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/27/2018
ms.locfileid: "26706138"
---
# <a name="integrate-office-365-threat-intelligence-with-windows-defender-advanced-threat-protection"></a><span data-ttu-id="843e2-103">Intégrer Office 365 Threat Intelligence à Windows Defender - Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="843e2-103">Integrate Office 365 Threat Intelligence with Windows Defender Advanced Threat Protection</span></span>

<span data-ttu-id="843e2-p101">Si vous faites partie de l’équipe de sécurité de votre organisation, vous pouvez intégrer Office 365 avec le module Windows Defender Advanced Threat Protection (DAV). Cela peut vous aider à comprendre rapidement si les ordinateurs des utilisateurs sont exposés lorsque vous effectuez des recherches sur les menaces dans Office 365. Par exemple, une fois que l’intégration est activée, vous serez en mesure de voir une liste des ordinateurs qui sont utilisés par les destinataires d’un message électronique détecté, ainsi que la manière dont les alertes récentes de ces ordinateurs ont dans Windows Defender DAV.</span><span class="sxs-lookup"><span data-stu-id="843e2-p101">If you are part of your organization's security team, you can integrate Office 365 with Windows Defender Advanced Threat Protection (ATP). This can help you quickly understand if users' machines are at risk when you are investigating threats in Office 365. For example, once integration is enabled, you will be able to see a list of machines that are used by the recipients of a detected email message, as well as how many recent alerts those machines have in Windows Defender ATP.</span></span>
  
<span data-ttu-id="843e2-107">L’image suivante montre l’onglet **périphériques** qui apparaît lorsque l’intégration Windows Defender DAV activée a été :</span><span class="sxs-lookup"><span data-stu-id="843e2-107">The following image shows the **Devices** tab that you'll see when have Windows Defender ATP integration enabled:</span></span> 
  
![Lorsque Windows Defender DAV est activé, vous pouvez voir une liste des ordinateurs sur lesquels les alertes.](media/fec928ea-8f0c-44d7-80b9-a2e0a8cd4e89.PNG)
  
<span data-ttu-id="843e2-p102">Dans cet exemple, vous pouvez voir que les destinataires du message électronique ont quatre ordinateurs et une a une alerte dans Windows Defender DAV. En cliquant sur le lien vers un ordinateur ouvre la page de l’ordinateur dans Windows Defender DAV dans un nouvel onglet.</span><span class="sxs-lookup"><span data-stu-id="843e2-p102">In this example, you can see that the recipients of the email message have four machines and one has an alert in Windows Defender ATP. Clicking the link to a machine opens the machine page in Windows Defender ATP in a new tab.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="843e2-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="843e2-111">Requirements</span></span>

- <span data-ttu-id="843e2-112">Votre organisation doit avoir des informations sur les menaces Office 365 et Windows Defender DAV.</span><span class="sxs-lookup"><span data-stu-id="843e2-112">Your organization must have Office 365 Threat Intelligence and Windows Defender ATP.</span></span>
    
- <span data-ttu-id="843e2-p103">Vous devez être un administrateur global d’Office 365 ou avoir un rôle d’administrateur de sécurité affecté dans le [sécurité &amp; centre de conformité](https://security.microsoft.com). (Voir [les autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md))</span><span class="sxs-lookup"><span data-stu-id="843e2-p103">You must be an Office 365 global administrator or have a security administrator role assigned in the [Security &amp; Compliance Center](https://security.microsoft.com). (See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md))</span></span>
    
- <span data-ttu-id="843e2-115">Vous devez avoir accès à Office 365 menaces et le portail Windows Defender DAV.</span><span class="sxs-lookup"><span data-stu-id="843e2-115">You must have access to both Office 365 Threat Intelligence and the Windows Defender ATP portal.</span></span>
    
## <a name="to-integrate-office-365-threat-intelligence-with-windows-defender-atp"></a><span data-ttu-id="843e2-116">Pour intégrer des menaces Office 365 avec Windows Defender DAV</span><span class="sxs-lookup"><span data-stu-id="843e2-116">To integrate Office 365 Threat Intelligence with Windows Defender ATP</span></span>

<span data-ttu-id="843e2-117">Intégration des menaces Office 365 avec Windows Defender DAV est configuré dans Office 365 et dans le portail Windows Defender DAV.</span><span class="sxs-lookup"><span data-stu-id="843e2-117">Integrating Office 365 Threat Intelligence with Windows Defender ATP is set up both in Office 365 and in the Windows Defender ATP portal.</span></span>
  
1. <span data-ttu-id="843e2-118">En tant qu’un global Office 365 ou un administrateur de sécurité, accédez à [https://security.microsoft.com](https://security.microsoft.com) et connectez-vous avec votre compte professionnel ou de l’école pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="843e2-118">As an Office 365 global or a security administrator, go to [https://security.microsoft.com](https://security.microsoft.com) and sign in with your work or school account for Office 365.</span></span> 
    
2. <span data-ttu-id="843e2-119">Cliquez sur **Gestion des menaces** \> **explorer menace**.</span><span class="sxs-lookup"><span data-stu-id="843e2-119">Choose **Threat management** \> **Threat explorer**.</span></span>
    
3. <span data-ttu-id="843e2-120">Dans le menu de **plus** , choisissez **Paramètres WDATP**.</span><span class="sxs-lookup"><span data-stu-id="843e2-120">On the **More** menu, choose **WDATP Settings**.</span></span>
    
4. <span data-ttu-id="843e2-121">Sélectionnez **se connecter à Windows DAV**.</span><span class="sxs-lookup"><span data-stu-id="843e2-121">Select **Connect to Windows ATP**.</span></span>
    
<span data-ttu-id="843e2-p104">Une fois que vous avez modifié les paramètres dans Office 365, vous devez activer la connexion à partir de Windows Defender DAV. Pour ce faire, voir [utilisation du portail Windows Defender avancée protection contre les menaces](https://go.microsoft.com/fwlink/?linkid=859690).</span><span class="sxs-lookup"><span data-stu-id="843e2-p104">After you have changed the settings in Office 365, you must enable the connection from Windows Defender ATP. To do that, see [Use the Windows Defender Advanced Threat Protection portal](https://go.microsoft.com/fwlink/?linkid=859690).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="843e2-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="843e2-124">Related topics</span></span>

[<span data-ttu-id="843e2-125">Intelligence des menaces d’Office 365</span><span class="sxs-lookup"><span data-stu-id="843e2-125">Office 365 Threat Intelligence</span></span>](office-365-ti.md)
  
[<span data-ttu-id="843e2-126">Protection avancée contre les menaces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="843e2-126">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  

