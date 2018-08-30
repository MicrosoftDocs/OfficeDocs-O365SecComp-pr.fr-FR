---
title: Affichage des rapports de protection contre la perte de données
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/7/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 41eb4324-c513-4fa5-91c8-8fbd8aaba83b
description: Les rapports DLP dans Office 365, vous pouvez rapidement afficher le nombre de correspondances de stratégies DLP, substitutions ou faux positifs ; voir si elles sont tendances monter ou Descendre dans le temps ; filtrer le rapport de différentes façons ; et afficher des détails supplémentaires en sélectionnant un point sur une ligne dans le graphique.
ms.openlocfilehash: 379e66fc3f2611cf338739d030c2b1d48e7416d8
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "23013908"
---
# <a name="view-the-reports-for-data-loss-prevention"></a><span data-ttu-id="ff64f-103">Affichage des rapports de protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="ff64f-103">View the reports for data loss prevention</span></span>

<span data-ttu-id="ff64f-p101">Après avoir créé des stratégies de protection contre la perte de données, vous souhaiterez vérifier qu’elles fonctionnent que vous destiné et en vous aidant à la conformité. Les rapports de sécurité Office 365 avec la DLP &amp; centre de conformité, vous pouvez rapidement afficher :</span><span class="sxs-lookup"><span data-stu-id="ff64f-p101">After you create your data loss prevention (DLP) policies, you'll want to verify that they're working as you intended and helping you to stay compliant. With the DLP reports in the Office 365 Security &amp; Compliance Center, you can quickly view:</span></span>
  
- <span data-ttu-id="ff64f-p102">**Correspondances de stratégies DLP** Ce rapport affiche le nombre de correspondances de stratégies DLP au fil du temps. Vous pouvez filtrer le rapport par date, l’emplacement, stratégie ou action. Vous pouvez utiliser ce rapport pour :</span><span class="sxs-lookup"><span data-stu-id="ff64f-p102">**DLP policy matches** This report shows the count of DLP policy matches over time. You can filter the report by date, location, policy, or action. You can use this report to:</span></span> 
    
  - <span data-ttu-id="ff64f-p103">Paramétrer ou d’affiner vos stratégies DLP comme les exécuter en mode test. Vous pouvez afficher la règle spécifique qui correspondent à du contenu.</span><span class="sxs-lookup"><span data-stu-id="ff64f-p103">Tune or refine your DLP policies as you run them in test mode. You can view the specific rule that matched the content.</span></span>
    
  - <span data-ttu-id="ff64f-111">Vous concentrer sur des périodes de temps spécifiques et comprendre les raisons des pics et des tendances.</span><span class="sxs-lookup"><span data-stu-id="ff64f-111">Focus on specific time periods and understand the reasons for spikes and trends.</span></span>
    
  - <span data-ttu-id="ff64f-112">Découvrez les processus métiers enfreignant les stratégies DLP de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ff64f-112">Discover business processes that violate your organization's DLP policies.</span></span>
    
  - <span data-ttu-id="ff64f-113">Comprendre n’importe quel impact sur l’activité de stratégies DLP en consultant la rubrique les actions sont appliquées au contenu.</span><span class="sxs-lookup"><span data-stu-id="ff64f-113">Understand any business impact of the DLP policies by seeing what actions are being applied to content.</span></span>
    
  - <span data-ttu-id="ff64f-114">Vérifier la conformité avec une stratégie DLP spécifique en affichant les correspondances pour cette stratégie.</span><span class="sxs-lookup"><span data-stu-id="ff64f-114">Verify compliance with a specific DLP policy by showing any matches for that policy.</span></span>
    
  - <span data-ttu-id="ff64f-115">Afficher la liste des utilisateurs les plus fréquents, recommencez les utilisateurs qui travaillent aux incidents dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ff64f-115">View a list of top users and repeat users who are contributing to incidents in your organization.</span></span>
    
  - <span data-ttu-id="ff64f-116">Afficher une liste des principaux types d’informations sensibles dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ff64f-116">View a list of the top types of sensitive information in your organization.</span></span>
    
- <span data-ttu-id="ff64f-p104">**Incidents DLP** Ce rapport indique également les correspondances de stratégies au fil du temps, comme la stratégie correspond à l’état. Toutefois, la stratégie établit une correspondance avec rapport montre correspond au niveau de la règle ; par exemple, si un message électronique mis en correspondance les trois règles différentes, la stratégie établit une correspondance avec rapport affiche trois différents éléments de ligne. En revanche, le rapport d’incidents montre correspond au niveau élément ; par exemple, si un message électronique mis en correspondance les trois règles différentes, le rapport d’incidents montre un élément de ligne de ce type de contenu.</span><span class="sxs-lookup"><span data-stu-id="ff64f-p104">**DLP incidents** This report also shows policy matches over time, like the policy matches report. However, the policy matches report shows matches at a rule level; for example, if an email matched three different rules, the policy matches report shows three different line items. By contrast, the incidents report shows matches at an item level; for example, if an email matched three different rules, the incidents report shows a single line item for that piece of content.</span></span> 
    
  <span data-ttu-id="ff64f-p105">Étant donné que le nombre de rapport est regroupée différemment, le rapport de correspondances de stratégie est préférable d’identification des correspondances avec des règles spécifiques et réglage de stratégies DLP. Le rapport d’incidents est préférable de l’identification des éléments de contenu spécifiques qui sont problématiques pour vos stratégies DLP.</span><span class="sxs-lookup"><span data-stu-id="ff64f-p105">Because the report counts are aggregated differently, the policy matches report is better for identifying matches with specific rules and fine tuning DLP policies. The incidents report is better for identifying specific pieces of content that are problematic for your DLP policies.</span></span>
    
- <span data-ttu-id="ff64f-p106">**Les substitutions et DLP faux positifs** Si votre stratégie DLP permet aux utilisateurs de remplacer ou signaler un faux positif, ce rapport affiche le nombre de ces instances au fil du temps. Vous pouvez filtrer le rapport par date, emplacement ou la stratégie. Vous pouvez utiliser ce rapport pour :</span><span class="sxs-lookup"><span data-stu-id="ff64f-p106">**DLP false positives and overrides** If your DLP policy allows users to override it or report a false positive, this report shows a count of such instances over time. You can filter the report by date, location, or policy. You can use this report to:</span></span> 
    
  - <span data-ttu-id="ff64f-125">Paramétrer ou d’affiner vos stratégies DLP en consultant la rubrique les stratégies provoquer un nombre élevé de faux positifs.</span><span class="sxs-lookup"><span data-stu-id="ff64f-125">Tune or refine your DLP policies by seeing which policies incur a high number of false positives.</span></span>
    
  - <span data-ttu-id="ff64f-126">Afficher les justificatifs présentés par les utilisateurs lorsqu’ils résolvent un Conseil de stratégie en remplacement de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="ff64f-126">View the justifications submitted by users when they resolve a policy tip by overriding the policy.</span></span>
    
  - <span data-ttu-id="ff64f-127">Découvrir où se substitue à conflit de stratégies DLP à des processus métiers valide par entraîner un nombre élevé de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ff64f-127">Discover where DLP policies conflict with valid business processes by incurring a high number of user overrides.</span></span>
    
<span data-ttu-id="ff64f-p107">Tous les rapports DLP peuvent afficher les données de la période de quatre mois plus récente. Les données les plus récentes peuvent prendre jusqu'à 24 heures pour apparaître dans les rapports.</span><span class="sxs-lookup"><span data-stu-id="ff64f-p107">All DLP reports can show data from the most recent four-month time period. The most recent data can take up to 24 hours to appear in the reports.</span></span>
  
<span data-ttu-id="ff64f-130">Vous trouverez ces rapports à la sécurité &amp; centre de conformité \> **rapports** \> **tableau de bord**.</span><span class="sxs-lookup"><span data-stu-id="ff64f-130">You can find these reports in the Security &amp; Compliance Center \> **Reports** \> **Dashboard**.</span></span>
  
![Rapport des correspondances de stratégies DLP](media/117d20c9-d379-403f-ad68-1f5cd6c4e5cf.png)
  
## <a name="view-the-justification-submitted-by-a-user-for-an-override"></a><span data-ttu-id="ff64f-132">Affichez la justification envoyée par un utilisateur pour une substitution</span><span class="sxs-lookup"><span data-stu-id="ff64f-132">View the justification submitted by a user for an override</span></span>

<span data-ttu-id="ff64f-133">Si votre stratégie DLP permet aux utilisateurs de remplacer, vous pouvez utiliser le faux positif et remplacer le rapport à afficher le texte envoyé par des utilisateurs dans le Conseil de stratégie.</span><span class="sxs-lookup"><span data-stu-id="ff64f-133">If your DLP policy allows users to override it, you can use the false positive and override report to view the text submitted by users in the policy tip.</span></span>
  
![Champ justification dans les détails de l’état de substitution et un faux positif DLP](media/e11e3126-026d-4e77-a16d-74a0686d1fa3.png)
  
## <a name="take-action-on-insights-and-recommendations"></a><span data-ttu-id="ff64f-135">Effectuer une action sur les conseils et recommandations</span><span class="sxs-lookup"><span data-stu-id="ff64f-135">Take action on insights and recommendations</span></span>

<span data-ttu-id="ff64f-136">États peuvent afficher des conseils et recommandations où vous pouvez cliquer sur l’icône d’avertissement rouge pour afficher des informations sur les problèmes potentiels et mesures correctives possibles.</span><span class="sxs-lookup"><span data-stu-id="ff64f-136">Reports can show insights and recommendations where you can click the red warning icon to see details about potential issues and take possible remedial action.</span></span>
  
![En cliquant sur une icône de détails pour afficher les détails et les actions à entreprendre](media/51782036-7299-4960-8175-75c2b1637159.png)
  
## <a name="find-the-cmdlets-for-the-dlp-reports"></a><span data-ttu-id="ff64f-138">Recherchez les applets de commande pour les rapports DLP</span><span class="sxs-lookup"><span data-stu-id="ff64f-138">Find the cmdlets for the DLP reports</span></span>

<span data-ttu-id="ff64f-139">Pour utiliser la plupart des applets de commande pour la sécurité &amp; centre de conformité, vous devez :</span><span class="sxs-lookup"><span data-stu-id="ff64f-139">To use most of the cmdlets for the Security &amp; Compliance Center, you need to:</span></span>
  
1. [<span data-ttu-id="ff64f-140">Se connecter à l’Office 365 Security &amp; centre de conformité à l’aide de PowerShell à distance</span><span class="sxs-lookup"><span data-stu-id="ff64f-140">Connect to the Office 365 Security &amp; Compliance Center using remote PowerShell</span></span>](http://go.microsoft.com/fwlink/?LinkID=799771&amp;clcid=0x409)
    
2. <span data-ttu-id="ff64f-141">Utilisez une de ces [Office 365 sécurité &amp; centre de conformité des applets de commande](http://go.microsoft.com/fwlink/?LinkID=799772&amp;clcid=0x409)</span><span class="sxs-lookup"><span data-stu-id="ff64f-141">Use any of these [Office 365 Security &amp; Compliance Center cmdlets](http://go.microsoft.com/fwlink/?LinkID=799772&amp;clcid=0x409)</span></span>
    
<span data-ttu-id="ff64f-p108">Toutefois, les rapports DLP doivent extraire des données dans Office 365, notamment Exchange Online. Pour cette raison, les applets de commande pour les rapports DLP sont disponibles dans Exchange Online Powershell — pas de sécurité &amp; Powershell du centre de conformité. Par conséquent, pour utiliser les applets de commande pour les rapports DLP, vous devez :</span><span class="sxs-lookup"><span data-stu-id="ff64f-p108">However, DLP reports need pull data from across Office 365, including Exchange Online. For this reason, the cmdlets for the DLP reports are available in Exchange Online Powershell—not in Security &amp; Compliance Center Powershell. Therefore, to use the cmdlets for the DLP reports, you need to:</span></span>
  
1. [<span data-ttu-id="ff64f-145">Connect to Exchange Online using remote PowerShell</span><span class="sxs-lookup"><span data-stu-id="ff64f-145">Connect to Exchange Online using remote PowerShell</span></span>](http://go.microsoft.com/fwlink/?LinkID=799773&amp;clcid=0x409)
    
2. <span data-ttu-id="ff64f-146">Utilisez une de ces applets de commande pour les rapports DLP :</span><span class="sxs-lookup"><span data-stu-id="ff64f-146">Use any of these cmdlets for the DLP reports:</span></span>
    
      - [<span data-ttu-id="ff64f-147">Get-DlpDetectionsReport</span><span class="sxs-lookup"><span data-stu-id="ff64f-147">Get-DlpDetectionsReport</span></span>](http://go.microsoft.com/fwlink/?LinkID=799774&amp;clcid=0x409)
    
      - [<span data-ttu-id="ff64f-148">Get-DlpDetailReport</span><span class="sxs-lookup"><span data-stu-id="ff64f-148">Get-DlpDetailReport</span></span>](http://go.microsoft.com/fwlink/?LinkID=799775&amp;clcid=0x409)
    

