---
title: Désactiver la création de rapports dans Outlook sur le site web de courrier indésirable
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/9/2015
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 8d57fe9e-57b8-4884-9317-80b380804b4a
description: En tant qu’un administrateur Office 365, vous pouvez désactiver la possibilité pour les personnes à un message électronique de rapport comme courriers indésirables.
ms.openlocfilehash: 8ee5ff87408b80c443e4cf950ce49f624096becb
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272039"
---
# <a name="turn-off-junk-email-reporting-in-outlook-on-the-web"></a><span data-ttu-id="d5ce6-103">Désactiver la création de rapports dans Outlook sur le site web de courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="d5ce6-103">Turn off junk email reporting in Outlook on the web</span></span>

<span data-ttu-id="d5ce6-p101">Vous pouvez envoyer indésirable, l’hameçonnage et les messages légitimes à Microsoft pour analyse à l’aide d’Outlook sur le courrier indésirable web reporting options, comme indiqué dans le [courrier indésirable de rapport et de hameçonnage dans Outlook sur le web ](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md). Si vous ne souhaitez pas utiliser ces options, administrateurs peuvent les désactiver par le biais de l’applet de commande [Set-OwaMailboxPolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx) .</span><span class="sxs-lookup"><span data-stu-id="d5ce6-p101">You can send junk, phishing, and not junk messages to Microsoft for analysis using the Outlook on the web junk email reporting options, as described in [Report junk email and phishing scams in Outlook on the web ](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md). If you don't want to use these options,admins can turn them off via the [Set-OwaMailboxPolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx) cmdlet.</span></span> 
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="d5ce6-106">Ce qu’il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="d5ce6-106">What do you need to know before you begin?</span></span>
<span data-ttu-id="d5ce6-107"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="d5ce6-107"></span></span>

- <span data-ttu-id="d5ce6-108">Durée d'exécution estimée : 5 minutes</span><span class="sxs-lookup"><span data-stu-id="d5ce6-108">Estimated time to complete: 5 minutes</span></span>
    
- <span data-ttu-id="d5ce6-p102">Vous devez avoir les autorisations avant de pouvoir effectuer cette procédure, ou procédures. Pour voir les autorisations requises, consultez l’entrée « Stratégies de boîte aux lettres Outlook Web App » dans la rubrique [autorisations Outlook Web App](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx#OutlookWebApp) .</span><span class="sxs-lookup"><span data-stu-id="d5ce6-p102">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Outlook Web App mailbox policies" entry in the [Outlook Web App permissions](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx#OutlookWebApp) topic.</span></span> 
    
- <span data-ttu-id="d5ce6-111">Avant d’exécuter les applets de commande nécessaire pour désactiver le signalement de courrier indésirable, il peut être utile de consulter les informations de référence dans les rubriques [Get-OwaMailboxPolicy](http://technet.microsoft.com/library/bdd580d3-8812-4b4a-93e8-c6401b0d2f0f.aspx) et [Set-OwaMailboxPolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx) .</span><span class="sxs-lookup"><span data-stu-id="d5ce6-111">Before you run the cmdlets required to turn off junk email reporting, it might be helpful to review the reference information in the [Get-OwaMailboxPolicy](http://technet.microsoft.com/library/bdd580d3-8812-4b4a-93e8-c6401b0d2f0f.aspx) and [Set-OwaMailboxPolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx) topics.</span></span> 
    
## <a name="turn-off-junk-phishing-and-not-junk-reporting-to-microsoft"></a><span data-ttu-id="d5ce6-112">Désactiver le courrier indésirable, hameçonnage et légitime de création de rapports à Microsoft</span><span class="sxs-lookup"><span data-stu-id="d5ce6-112">Turn off junk, phishing, and not junk reporting to Microsoft</span></span>
<span data-ttu-id="d5ce6-113"><a name="sectionSection1"> </a></span><span class="sxs-lookup"><span data-stu-id="d5ce6-113"></span></span>

<span data-ttu-id="d5ce6-114">Tout d'abord, exécutez la cmdlet suivante pour obtenir les répertoires virtuels pour lesquels vous souhaitez désactiver le signalement :</span><span class="sxs-lookup"><span data-stu-id="d5ce6-114">First, run the following cmdlet to get the virtual directories for which you want to turn off reporting:</span></span>
  
```
Get-OwaMailboxPolicy -Identity <parameter>
```

<span data-ttu-id="d5ce6-115">Ensuite, exécutez la cmdlet suivante pour désactiver le signalement des courriers indésirables et légitimes à Microsoft :</span><span class="sxs-lookup"><span data-stu-id="d5ce6-115">Next, run the following cmdlet to turn off junk and not junk reporting to Microsoft:</span></span>
  
```
Set-OwaMailboxPolicy -Identity <parameter> -ReportJunkEmailEnabled $false
```

<span data-ttu-id="d5ce6-116">Par exemple, la cmdlet suivante désactive le signalement pour le répertoire virtuel Contoso\owa :</span><span class="sxs-lookup"><span data-stu-id="d5ce6-116">For example, the following cmdlet turns off reporting for virtual directory Contoso\owa:</span></span>
  
```
Set-OwaMailboxPolicy -Identity Default -ReportJunkEmailEnabled $false
```

## <a name="how-do-you-know-this-worked"></a><span data-ttu-id="d5ce6-117">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="d5ce6-117">How do you know this worked?</span></span>
<span data-ttu-id="d5ce6-118"><a name="sectionSection2"> </a></span><span class="sxs-lookup"><span data-stu-id="d5ce6-118"></span></span>

<span data-ttu-id="d5ce6-p103">Exécutez Get-OWAMailboxPolicy pour vérifier les valeurs de paramètre et ensuite accéder à Outlook sur le web et vérifiez que les options pour signaler le courrier indésirable, l’hameçonnage et légitime ne sont pas disponibles. Vous serez toujours en mesure de marquer les messages comme courrier indésirable, hameçonnage et légitime, mais vous ne pourrez pas les signaler.</span><span class="sxs-lookup"><span data-stu-id="d5ce6-p103">Run Get-OWAMailboxPolicy to check the parameter values, and then access Outlook on the web and verify that the options to report junk, phishing, and not junk are not available. You'll still be able to mark messages as junk, phishing, and not junk, but you won't be able to report them.</span></span> 
  

