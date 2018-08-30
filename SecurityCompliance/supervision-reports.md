---
title: Rapports de surveillance
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: 5/12/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 2a762db5-e1c9-4c09-aa8e-bef49ce97209
description: Utiliser des rapports de surveillance pour voir de messages électroniques qui doivent conformité et qui doit exécuter.
ms.openlocfilehash: e18d083c0aad8be945c628516e593462da8e3898
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527700"
---
# <a name="supervision-reports"></a><span data-ttu-id="640bd-103">Rapports de surveillance</span><span class="sxs-lookup"><span data-stu-id="640bd-103">Supervision reports</span></span>

<span data-ttu-id="640bd-p101">Définissent des stratégies de surveillance communications dans votre organisation doivent passer en revue les pour la conformité et qui effectue les révisions. Utilisez les rapports de surveillance pour afficher l’activité de révision au niveau de la stratégie et de réviseur. Pour chaque stratégie, vous pouvez également afficher les statistiques live sur l’état actuel de l’activité de révision. [En savoir plus sur les stratégies de surveillance](configure-supervision-policies.md) .</span><span class="sxs-lookup"><span data-stu-id="640bd-p101">Supervision policies define which communications in your organization need review for compliance, and who will perform those reviews. Use the supervision reports to see the review activity at the policy and reviewer level. For each policy, you can also view live statistics on the current state of review activity. [Learn more about supervision policies ](configure-supervision-policies.md) .</span></span> 
  
> [!NOTE]
> <span data-ttu-id="640bd-p102">À l’aide de stratégies de surveillance requiert un abonnement à Office 365 E5 pour votre organisation. Si vous n’avez qu’un plan et essayer de surveillance, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="640bd-p102">Using supervision policies requires an Office 365 E5 subscription for your organization. If you don't have that plan and want to try supervision, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="640bd-110">Vous pouvez utiliser les rapports de surveillance :</span><span class="sxs-lookup"><span data-stu-id="640bd-110">You can use the supervision reports to:</span></span>
  
- <span data-ttu-id="640bd-111">Vérifiez que vos stratégies fonctionnent comme prévu.</span><span class="sxs-lookup"><span data-stu-id="640bd-111">Verify that your policies are working as you intended.</span></span> 
    
- <span data-ttu-id="640bd-112">Découvrez combien de messages est identifiés pour révision.</span><span class="sxs-lookup"><span data-stu-id="640bd-112">Find out how many emails are being identified for review.</span></span>
    
- <span data-ttu-id="640bd-p103">Découvrez combien de messages ne sont pas conformes et ceux qui est en passant révision. Ces informations peuvent vous aider à décider s’il faut affiner vos stratégies ou modifier le nombre de relecteurs.</span><span class="sxs-lookup"><span data-stu-id="640bd-p103">Find out how many emails aren't compliant and which ones are passing review. This information can help you decide whether to fine-tune your policies or change the number of reviewers.</span></span>
    
## <a name="view-the-supervision-report"></a><span data-ttu-id="640bd-115">Afficher le rapport de surveillance</span><span class="sxs-lookup"><span data-stu-id="640bd-115">View the Supervision report</span></span>

1. <span data-ttu-id="640bd-116">Se connecter à la [sécurité &amp; centre de conformité](https://protection.office.com/) à l’aide des informations d’identification pour un compte d’administrateur de votre organisation Office 365 qui dispose d’autorisations pour afficher les rapports de surveillance...</span><span class="sxs-lookup"><span data-stu-id="640bd-116">Sign into the [Security &amp; Compliance Center](https://protection.office.com/) using the credentials for an admin account in your Office 365 organization that has permissions to view supervision reports..</span></span> 
    
2. <span data-ttu-id="640bd-p104">Accédez aux **rapports** \> **tableau de bord**. Vous verrez un widget de création de rapports de surveillance et d’autres rapports que vous avez accès à.</span><span class="sxs-lookup"><span data-stu-id="640bd-p104">Go to **Reports** \> **Dashboard**. You'll see a reporting widget for supervision and other reports you have access to.</span></span>
    
3. <span data-ttu-id="640bd-119">Cliquez sur le widget de **surveillance** pour ouvrir la page rapport détaillé.</span><span class="sxs-lookup"><span data-stu-id="640bd-119">Click the **Supervision** widget to open the detailed report page.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="640bd-p105">Si vous n’êtes pas en mesure d’accéder à la page **rapports** , vérifiez que vous êtes membre du groupe de rôles de supervision, comme indiqué dans [rendre disponibles dans votre organisation de surveillance](configure-supervision-policies.md#SRavailable). Soient inclus dans cette permet de groupe de rôle pour créer et gérer le contrôle des stratégies et exécutez le rapport.</span><span class="sxs-lookup"><span data-stu-id="640bd-p105">If you aren't able to access the **Reports** page, check that you're a member of the Supervisory Review role group, as described in [Make supervision available in your organization](configure-supervision-policies.md#SRavailable). Being included in this role group lets you create and manage supervision polices and run the report.</span></span> 
  
## <a name="how-to-use-the-report"></a><span data-ttu-id="640bd-122">Comment utiliser le rapport</span><span class="sxs-lookup"><span data-stu-id="640bd-122">How to use the report</span></span>

<span data-ttu-id="640bd-p106">Lorsqu’une stratégie de surveillance identifie un message électronique pour révision, le courrier électronique est remis au dossier de surveillance du réviseur dans Outlook et Outlook web app. Ce rapport répertorie le nom de chaque stratégie et le nombre de communications à chaque étape du processus de révision.</span><span class="sxs-lookup"><span data-stu-id="640bd-p106">When a supervision policy identifies an email for review, the email is delivered to the reviewer's Supervision folder in Outlook and Outlook web app. This report lists each policy's name and the number of communications at each stage in the review process.</span></span>
  
<span data-ttu-id="640bd-125">Utilisez l’état :</span><span class="sxs-lookup"><span data-stu-id="640bd-125">Use the report to:</span></span>
  
- <span data-ttu-id="640bd-126">Afficher les données pour toutes les stratégies spécifiques ou.</span><span class="sxs-lookup"><span data-stu-id="640bd-126">View data for all or specific policies.</span></span>
    
- <span data-ttu-id="640bd-127">Afficher les données regroupement par type de balise (par exemple, conforme, Questionable, etc.), réviseur ou type de message.</span><span class="sxs-lookup"><span data-stu-id="640bd-127">View data grouped by tag type (such as Compliant, Questionable, etc.), reviewer, or message type.</span></span>
    
- <span data-ttu-id="640bd-128">Exporter des données vers un fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="640bd-128">Export data to a CSV file.</span></span>
    
- <span data-ttu-id="640bd-129">Filtrer les données en fonction de la date d’activité la révision, type de balise, réviseur, type de message.</span><span class="sxs-lookup"><span data-stu-id="640bd-129">Filter data based on review activity date, tag type, reviewer, message type.</span></span>
    
<span data-ttu-id="640bd-130">Voici une répartition des valeurs que vous pouvez voir dans la colonne **type de balise** .</span><span class="sxs-lookup"><span data-stu-id="640bd-130">Here's a breakdown of the values you might see in the **Tag type** column.</span></span> 
  
|<span data-ttu-id="640bd-131">**Type de balise**</span><span class="sxs-lookup"><span data-stu-id="640bd-131">**Tag type**</span></span>|<span data-ttu-id="640bd-132">**Cela signifie**</span><span class="sxs-lookup"><span data-stu-id="640bd-132">**What it means**</span></span>|
|:-----|:-----|
|<span data-ttu-id="640bd-133">Pas de révision</span><span class="sxs-lookup"><span data-stu-id="640bd-133">Not Reviewed</span></span>  <br/> |<span data-ttu-id="640bd-p107">Le nombre de messages électroniques qui n’ont pas encore été révisées. Ces e-mails sont en attente de révision dans le dossier de contrôle du réviseur dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="640bd-p107">The number of emails that have not been reviewed yet. These emails are awaiting review in the reviewer's supervision folder in Outlook.</span></span>  <br/> |
|<span data-ttu-id="640bd-136">Compatible</span><span class="sxs-lookup"><span data-stu-id="640bd-136">Compliant</span></span>  <br/> |<span data-ttu-id="640bd-p108">Le nombre de messages électroniques révisé et marqué comme conforme. Aucune action supplémentaire n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="640bd-p108">The number of emails reviewed and marked as compliant. No further action is needed.</span></span>  <br/> |
|<span data-ttu-id="640bd-139">Suspects</span><span class="sxs-lookup"><span data-stu-id="640bd-139">Questionable</span></span>  <br/> |<span data-ttu-id="640bd-p109">Le nombre de messages électroniques révisé et marqués suspect. Sous la forme d’un indicateur ; autres réviseurs peuvent aider à vérifier si un message électronique doit être une enquête de la conformité.</span><span class="sxs-lookup"><span data-stu-id="640bd-p109">The number of emails reviewed and marked questionable. This acts as a flag; other reviewers can help check whether an email needs investigation for compliance.</span></span>  <br/> |
|<span data-ttu-id="640bd-142">Non compatibles (actif)</span><span class="sxs-lookup"><span data-stu-id="640bd-142">Non-Compliant (Active)</span></span>  <br/> |<span data-ttu-id="640bd-143">Le nombre d’e-mails non conformes qui étudie relecteurs.</span><span class="sxs-lookup"><span data-stu-id="640bd-143">The number of non-compliant emails that reviewers are currently investigating.</span></span>  <br/> |
|<span data-ttu-id="640bd-144">Non compatibles (résolu)</span><span class="sxs-lookup"><span data-stu-id="640bd-144">Non-Compliant (Resolved)</span></span>  <br/> |<span data-ttu-id="640bd-145">Le nombre de messages électroniques non conformes qui relecteurs étudier et de résoudre.</span><span class="sxs-lookup"><span data-stu-id="640bd-145">The number of non-compliant emails that reviewers investigated and resolved.</span></span>  <br/> |
   
## <a name="more-details"></a><span data-ttu-id="640bd-146">Plus de détails</span><span class="sxs-lookup"><span data-stu-id="640bd-146">More details</span></span>

- <span data-ttu-id="640bd-147">Stratégies de surveillance doivent tout d’abord être mis en service avant qu’ils n’apparaissent pas dans ce rapport.</span><span class="sxs-lookup"><span data-stu-id="640bd-147">Supervision policies must first be provisioned before they will appear in this report.</span></span>
    
- <span data-ttu-id="640bd-p110">Si les stratégies sont supprimés, les données d’historique sont toujours affichées. Cependant, ils sont indiqués comme une stratégie « inexistant » et la fonction **Exporter** n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="640bd-p110">If policies are deleted, historical data is still shown. However, they're indicated as a "Non-existent policy", and the **Export** function isn't available.</span></span> 
    
- <span data-ttu-id="640bd-p111">Si le rapport n’affiche toutes les données par défaut, il peut être car la plage de dates actuel n’a aucune donnée à afficher. Dans ces cas-là, utilisez le contrôle de **filtres** pour modifier la plage de dates.</span><span class="sxs-lookup"><span data-stu-id="640bd-p111">If the report doesn't show any data by default, it might be because the current date range doesn't have any data to show. In these cases, use the **Filters** control to change the date range.</span></span> 
    

