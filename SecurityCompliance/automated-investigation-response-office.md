---
title: Recherche et réponse automatisées (AIR) avec Office 365 Threat Intelligence
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/21/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection: M365-security-compliance
description: Découvrez les fonctionnalités d'analyse et de réponse automatisées dans Office 365 Advanced Threat Protection.
ms.openlocfilehash: c2d5acd0bf26dc28b30f26488adf47de2c834fb6
ms.sourcegitcommit: a56128c7be5d59e976851c27301031e19fa1997d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/21/2019
ms.locfileid: "30736301"
---
# <a name="automated-investigation-and-response-air-with-office-365-threat-intelligence"></a><span data-ttu-id="c1189-103">Recherche et réponse automatisées (AIR) avec Office 365 Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="c1189-103">Automated Investigation and Response (AIR) with Office 365 Threat Intelligence</span></span>

<span data-ttu-id="c1189-104">AutoMated Investigation and Response (AIR) (bientôt disponible pour les [fonctionnalités d'enquête et de réponse aux menaces Office 365](office-365-ti.md)) vous permet d'effectuer des recherches et des corrections automatiques sur des menaces connues qui existent aujourd'hui.</span><span class="sxs-lookup"><span data-stu-id="c1189-104">Automated Investigation and Response (AIR) (coming soon to [Office 365 Threat investigation and response capabilities](office-365-ti.md)) enables you to run automated investigation and remediation to well-known threats that exist today.</span></span> <span data-ttu-id="c1189-105">Lisez cet article pour obtenir une vue d'ensemble de l'AIR et la façon dont il peut aider votre organisation à réduire les menaces de manière plus efficace.</span><span class="sxs-lookup"><span data-stu-id="c1189-105">Read this article to get an overview of AIR and how it can help your organization mitigate threats more effectively and efficiently.</span></span> <span data-ttu-id="c1189-106">Tolearn en savoir plus sur la disponibilité de l'AIR, consultez la feuille de [route Microsoft 365](https://www.microsoft.com/microsoft-365/roadmap).</span><span class="sxs-lookup"><span data-stu-id="c1189-106">Tolearn more about when AIR will be available, see the [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap).</span></span>

## <a name="alerts"></a><span data-ttu-id="c1189-107">Alertes</span><span class="sxs-lookup"><span data-stu-id="c1189-107">Alerts</span></span>

<span data-ttu-id="c1189-108">Les [alertes](alert-policies.md#viewing-alerts) représentent des déclencheurs pour les flux de travail d'équipe des opérations de sécurité pour la réponse aux incidents.</span><span class="sxs-lookup"><span data-stu-id="c1189-108">[Alerts](alert-policies.md#viewing-alerts) represent triggers for Security Operations team workflows for incident response.</span></span> <span data-ttu-id="c1189-109">La définition de la priorité des alertes à droite pour l'enquête tout en s'assurant qu'aucune menace n'est sans adresse est complexe.</span><span class="sxs-lookup"><span data-stu-id="c1189-109">Prioritizing the right set of alerts for investigation while making sure no threats are unaddressed is challenging.</span></span> <span data-ttu-id="c1189-110">Lorsque les enquêtes dans les alertes sont effectuées manuellement, les équipes des opérations de sécurité doivent rechercher et corréler les entités (par exemple, le contenu, les appareils et les utilisateurs) menacées.</span><span class="sxs-lookup"><span data-stu-id="c1189-110">When investigations into alerts are performed manually, Security Operations teams must hunt and correlate entities (e.g. content, devices and users) at risk from threats.</span></span> <span data-ttu-id="c1189-111">Ces tâches et les flux de travail sont très longs et impliquent plusieurs outils et systèmes.</span><span class="sxs-lookup"><span data-stu-id="c1189-111">Such tasks and workflows are very time consuming and involve multiple tools and systems.</span></span> <span data-ttu-id="c1189-112">Avec AIR, l'analyse et la réponse sont automatisées dans les alertes de gestion de la sécurité et des menaces clés qui déclenchent automatiquement vos règles de réponse de sécurité.</span><span class="sxs-lookup"><span data-stu-id="c1189-112">With AIR, investigation and response are automated into key security and threat management alerts that trigger your security response playbooks automatically.</span></span> 

<span data-ttu-id="c1189-113">pour afficher les alertes, dans le centre de sécurité & de sécurité Office 365, sélectionnez **alertes** > **afficher les alertes**.</span><span class="sxs-lookup"><span data-stu-id="c1189-113">To view alerts, in the Office 365 Security & Compliance Center, choose **Alerts** > **View alerts**.</span></span>

![Alertes liées à des enquêtes](media/air-alerts-page-details.png) 

<span data-ttu-id="c1189-115">Sélectionnez une alerte pour afficher ses détails, puis, à partir de là, utilisez le lien **consulter l'enquête** pour accéder à l' [enquête](#investigation-graph)correspondante.</span><span class="sxs-lookup"><span data-stu-id="c1189-115">Select an alert to view its details, and from there, use the **View investigation** link to go to the corresponding [investigation](#investigation-graph).</span></span>

## <a name="security-playbooks"></a><span data-ttu-id="c1189-116">Règles de sécurité</span><span class="sxs-lookup"><span data-stu-id="c1189-116">Security playbooks</span></span>

<span data-ttu-id="c1189-117">Les règles de sécurité sont des stratégies principales qui sont au cœur de l'automatisation dans la protection contre les menaces Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c1189-117">Security playbooks are back-end policies that are at the heart of automation in Microsoft Threat Protection.</span></span> <span data-ttu-id="c1189-118">Les règles de sécurité fournies dans AIR sont basées sur des scénarios de sécurité réels courants.</span><span class="sxs-lookup"><span data-stu-id="c1189-118">The security playbooks provided in AIR are based on common real-world security scenarios.</span></span> <span data-ttu-id="c1189-119">Un manuel de sécurité est lancé automatiquement lorsqu'une alerte est déclenchée au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="c1189-119">A security playbook is launched automatically when an alert is triggered within your organization.</span></span> <span data-ttu-id="c1189-120">Une fois que l'alerte est déclenchée, le manuel associé est exécuté automatiquement.</span><span class="sxs-lookup"><span data-stu-id="c1189-120">Once the alert triggers, the associated playbook is run automatically.</span></span> <span data-ttu-id="c1189-121">Le manuel exécute une enquête, en examinant toutes les métadonnées associées (y compris les messages électroniques, les utilisateurs, les objets, les expéditeurs, etc.) et, en fonction de ses conclusions, recommande une série d'actions que l'équipe de sécurité de votre organisation peut prendre pour contrôler et atténuer la menace.</span><span class="sxs-lookup"><span data-stu-id="c1189-121">The playbook runs an investigation, looking at all the associated metadata (including email messages, users, subjects, senders, etc.) and, based on its findings, recommends a set of actions that your organization's security team can take to control and mitigate the threat.</span></span> 

<span data-ttu-id="c1189-122">Les règles de sécurité que vous obtenez avec AIR sont conçues pour aborder les menaces les plus fréquentes auxquelles les entreprises sont confrontés aujourd'hui.</span><span class="sxs-lookup"><span data-stu-id="c1189-122">The security playbooks you'll get with AIR are designed to tackle the most frequent threats that organizations face today.</span></span> <span data-ttu-id="c1189-123">Elles sont basées sur les opérations de sécurité et les équipes de réponse aux incidents, notamment celles qui permettent de défendre les biens Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c1189-123">They're based on input from Security Operations and Incident Response teams, including those who help defend Microsoft assets.</span></span>

### <a name="security-playbooks-are-rolling-out-in-phases"></a><span data-ttu-id="c1189-124">Les règles de sécurité sont déployées en plusieurs phases</span><span class="sxs-lookup"><span data-stu-id="c1189-124">Security playbooks are rolling out in phases</span></span>

<span data-ttu-id="c1189-125">Dans le cadre de l'AIR, les règles de sécurité sont déployées en phases.</span><span class="sxs-lookup"><span data-stu-id="c1189-125">As part of AIR, security playbooks are rolling out in phases</span></span>

- <span data-ttu-id="c1189-126">**Phase 1 (avril 2019)**: les règles incluent des recommandations que les administrateurs de la sécurité examinent et approuvent.</span><span class="sxs-lookup"><span data-stu-id="c1189-126">**Phase 1 (April 2019)**: Playbooks include recommendations that security administrators review and approve.</span></span> 

- <span data-ttu-id="c1189-127">**Phase 2 (juin 2019)**: les administrateurs de la sécurité auront la possibilité d'autoriser les règles de sécurité à agir automatiquement, sans interaction administrative.</span><span class="sxs-lookup"><span data-stu-id="c1189-127">**Phase 2 (June 2019)**: Security administrators will have the option to allow security playbooks to take action automatically, without administrative interaction.</span></span>

<span data-ttu-id="c1189-128">La phase 1 inclut les règles suivantes:</span><span class="sxs-lookup"><span data-stu-id="c1189-128">Phase 1 will include the following playbooks:</span></span>
- <span data-ttu-id="c1189-129">Message hameçon signalé par l'utilisateur</span><span class="sxs-lookup"><span data-stu-id="c1189-129">User-reported phish message</span></span>
- <span data-ttu-id="c1189-130">URL cliquez sur modifier le verdict et remplacer le bloc liens de sécurité ATP</span><span class="sxs-lookup"><span data-stu-id="c1189-130">URL click verdict change and ATP Safe Links block override</span></span>
- <span data-ttu-id="c1189-131">Programme malveillant ZAP</span><span class="sxs-lookup"><span data-stu-id="c1189-131">Malware ZAP</span></span>
- <span data-ttu-id="c1189-132">Hameçon ZAP</span><span class="sxs-lookup"><span data-stu-id="c1189-132">Phish ZAP</span></span>
- <span data-ttu-id="c1189-133">Analyses manuelles (à l'aide de l'Explorateur)</span><span class="sxs-lookup"><span data-stu-id="c1189-133">Manual investigations (using Explorer)</span></span>

<span data-ttu-id="c1189-134">Plusieurs autres règles sont prévues pour la phase 2.</span><span class="sxs-lookup"><span data-stu-id="c1189-134">Several more playbooks are planned for Phase 2.</span></span>

### <a name="playbooks-include-investigation-and-recommendations"></a><span data-ttu-id="c1189-135">Les règles incluent une enquête et des recommandations</span><span class="sxs-lookup"><span data-stu-id="c1189-135">Playbooks include investigation and recommendations</span></span>

<span data-ttu-id="c1189-136">Chaque manuel inclut:</span><span class="sxs-lookup"><span data-stu-id="c1189-136">Each playbook includes:</span></span> 
- <span data-ttu-id="c1189-137">une enquête racine,</span><span class="sxs-lookup"><span data-stu-id="c1189-137">a root investigation,</span></span> 
- <span data-ttu-id="c1189-138">étapes de la recherche d'autres menaces potentielles et</span><span class="sxs-lookup"><span data-stu-id="c1189-138">steps to hunt down other potential threats, and</span></span> 
- <span data-ttu-id="c1189-139">correction des menaces recommandées.</span><span class="sxs-lookup"><span data-stu-id="c1189-139">recommended threat remediation.</span></span>

<span data-ttu-id="c1189-140">Chaque étape de haut niveau inclut de nombreuses sous-étapes qui sont exécutées pour fournir une réponse approfondie, détaillée et exhaustive aux menaces.</span><span class="sxs-lookup"><span data-stu-id="c1189-140">Each high-level step includes many sub-steps that are executed to provide a deep, detailed, and exhaustive response to threats.</span></span>

## <a name="example-user-reported-phish-message"></a><span data-ttu-id="c1189-141">Exemple: message hameçon signalé par l'utilisateur</span><span class="sxs-lookup"><span data-stu-id="c1189-141">Example: User-reported phish message</span></span>

<span data-ttu-id="c1189-142">Lorsqu'un utilisateur de votre organisation soumet un message électronique et le signale à Microsoft à l'aide du [complément de message de rapport pour Outlook ou Outlook Web Access](enable-the-report-message-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="c1189-142">When a user in your organization submits an email message and reports it to Microsoft by using the [Report Message add-in for Outlook or Outlook Web Access](enable-the-report-message-add-in.md).</span></span> <span data-ttu-id="c1189-143">Cela déclenche une alerte d'information basée sur le système qui lance automatiquement le manuel d'enquête.</span><span class="sxs-lookup"><span data-stu-id="c1189-143">This triggers a system-based informational alert that automatically launches the investigation playbook.</span></span>

<span data-ttu-id="c1189-144">Lors de la phase d'enquête de racine, différents aspects du courrier électronique sont évalués.</span><span class="sxs-lookup"><span data-stu-id="c1189-144">During the root investigation phase, various aspects of the email are assessed.</span></span> <span data-ttu-id="c1189-145">Ces situations sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="c1189-145">These include:</span></span>
- <span data-ttu-id="c1189-146">Détermination du type de menace susceptible de se présenter;</span><span class="sxs-lookup"><span data-stu-id="c1189-146">A determination about what type of threat it might be;</span></span>
- <span data-ttu-id="c1189-147">Expéditeur;</span><span class="sxs-lookup"><span data-stu-id="c1189-147">Who sent it;</span></span>
- <span data-ttu-id="c1189-148">Emplacement d'envoi du courrier électronique (infrastructure émettrice);</span><span class="sxs-lookup"><span data-stu-id="c1189-148">Where the email was sent from (sending infrastructure);</span></span>
- <span data-ttu-id="c1189-149">Si d'autres instances du courrier électronique ont été remises ou bloquées;</span><span class="sxs-lookup"><span data-stu-id="c1189-149">Whether other instances of the email were delivered or blocked;</span></span>
- <span data-ttu-id="c1189-150">Une évaluation de nos analystes;</span><span class="sxs-lookup"><span data-stu-id="c1189-150">An assessment from our analysts;</span></span>
- <span data-ttu-id="c1189-151">Si le courrier électronique est associé à des campagnes connues;</span><span class="sxs-lookup"><span data-stu-id="c1189-151">Whether the email is associated with any known campaigns;</span></span>
- <span data-ttu-id="c1189-152">et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="c1189-152">and more.</span></span>

<span data-ttu-id="c1189-153">Une fois l'enquête terminée, le manuel fournit une liste d'actions recommandées à effectuer.</span><span class="sxs-lookup"><span data-stu-id="c1189-153">After the root investigation is complete, the playbook provides a list of recommended actions to take.</span></span>
  
<span data-ttu-id="c1189-154">Ensuite, plusieurs étapes de la chasse sont exécutées:</span><span class="sxs-lookup"><span data-stu-id="c1189-154">Next, several hunting steps are executed:</span></span>

- <span data-ttu-id="c1189-155">Les messages électroniques similaires dans d'autres clusters de messagerie sont recherchés.</span><span class="sxs-lookup"><span data-stu-id="c1189-155">Similar email messages in other email clusters are searched.</span></span>
- <span data-ttu-id="c1189-156">Le signal est partagé avec d'autres plateformes, telles que [Windows Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/windows-defender-advanced-threat-protection).</span><span class="sxs-lookup"><span data-stu-id="c1189-156">The signal is shared with other platforms, such as [Windows Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/windows-defender-advanced-threat-protection).</span></span>
- <span data-ttu-id="c1189-157">Une détermination est effectuée sur le fait que les utilisateurs aient cliqué sur le message suspect.</span><span class="sxs-lookup"><span data-stu-id="c1189-157">A determination is made on whether any users have clicked through on the suspicious email message.</span></span>
- <span data-ttu-id="c1189-158">Une vérification est effectuée dans Office 365 [EOP](eop/exchange-online-protection-eop.md) et [](office-365-atp.md) la protection avancée contre les menaces pour voir s'il existe d'autres messages similaires signalés par les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="c1189-158">A check is done across Office 365 [EOP](eop/exchange-online-protection-eop.md) and [ATP](office-365-atp.md) to see if there are any other similar messages reported by users.</span></span>
- <span data-ttu-id="c1189-159">Une vérification est exécutée pour déterminer si un utilisateur a été compromis.</span><span class="sxs-lookup"><span data-stu-id="c1189-159">A check is done to see if a user has been compromised.</span></span> <span data-ttu-id="c1189-160">Cette vérification s'appuie sur les signaux de la sécurité de l' [application Cloud Microsoft](https://docs.microsoft.com/cloud-app-security) et d' [Azure Active Directory](https://docs.microsoft.com/azure/active-directory), ce qui met en corrélation les événements ou alertes connexes.</span><span class="sxs-lookup"><span data-stu-id="c1189-160">This check leverages signals across [Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security) and [Azure Active Directory](https://docs.microsoft.com/azure/active-directory), correlating any related events or alerts.</span></span> 

<span data-ttu-id="c1189-161">Au cours de la phase de chasse, les risques et les menaces sont affectés à différentes étapes de la chasse.</span><span class="sxs-lookup"><span data-stu-id="c1189-161">During the hunting phase, risks and threats are assigned to various hunting steps.</span></span>  

<span data-ttu-id="c1189-162">La correction est la phase finale du manuel.</span><span class="sxs-lookup"><span data-stu-id="c1189-162">Remediation is the final phase of the playbook.</span></span> <span data-ttu-id="c1189-163">Pendant cette phase, les étapes de correction sont prises, en fonction des phases de theinvestigation et de chasse.</span><span class="sxs-lookup"><span data-stu-id="c1189-163">During this phase, remediation steps are taken, based on theinvestigation and hunting phases.</span></span>  

## <a name="getting-started"></a><span data-ttu-id="c1189-164">Prise en main</span><span class="sxs-lookup"><span data-stu-id="c1189-164">Getting started</span></span>

<span data-ttu-id="c1189-165">Pour accéder à vos enquêtes, en tant qu'administrateur général ou administrateur de sécurité Office 365, accédez au centre de sécurité & conformité[https://protection.office.com](https://protection.office.com)Office 365 () et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="c1189-165">To access your investigations, as an Office 365 global administrator or security administrator, Go to the Office 365 Security & Compliance Center ([https://protection.office.com](https://protection.office.com)) and sign in.</span></span> <span data-ttu-id="c1189-166">Effectuez ensuite l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="c1189-166">Then, do one of the following:</span></span>

- <span data-ttu-id="c1189-167">Dans le volet de navigation de gauche, accédez à**recherches**de **gestion** > des menaces.</span><span class="sxs-lookup"><span data-stu-id="c1189-167">In the left navigation, go to **Threat management** > **Investigations**.</span></span>

    <span data-ttu-id="c1189-168">ou</span><span class="sxs-lookup"><span data-stu-id="c1189-168">or</span></span>

- <span data-ttu-id="c1189-169">Visitez le tableau de bord de gestion des menaces (dans le centre de sécurité & Compliance Center, accédez au**tableau de bord**de **gestion** > des menaces).</span><span class="sxs-lookup"><span data-stu-id="c1189-169">Visit the Threat management dashboard (In the Security & Compliance Center, go to **Threat management** > **Dashboard**).</span></span>

![Widgets d'AIR](media/air-widgets.png)

<span data-ttu-id="c1189-171">Vos widgets d'AIR s'affichent dans la partie supérieure du [tableau de bord de sécurité](security-dashboard.md).</span><span class="sxs-lookup"><span data-stu-id="c1189-171">Your AIR widgets will appear across the top of the [Security Dashboard](security-dashboard.md).</span></span> <span data-ttu-id="c1189-172">Sélectionnez un widget pour commencer.</span><span class="sxs-lookup"><span data-stu-id="c1189-172">Select a widget to get started.</span></span>

### <a name="automated-investigations"></a><span data-ttu-id="c1189-173">Analyses automatisées</span><span class="sxs-lookup"><span data-stu-id="c1189-173">Automated investigations</span></span>

<span data-ttu-id="c1189-174">La page enquêtes automatiques indique les évaluations de votre organisation et leurs États actuels.</span><span class="sxs-lookup"><span data-stu-id="c1189-174">The automated investigations page shows your organization's investigations and their current states.</span></span>

![Page d'enquête principale pour l'AIR](media/air-maininvestigationpage.png) 
  
<span data-ttu-id="c1189-176">Vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="c1189-176">You can:</span></span>
- <span data-ttu-id="c1189-177">Accédez directement à une enquête (sélectionnez un **ID d'enquête**).</span><span class="sxs-lookup"><span data-stu-id="c1189-177">Navigate directly to an investigation (select an **Investigation ID**).</span></span>
- <span data-ttu-id="c1189-178">Appliquer des filtres.</span><span class="sxs-lookup"><span data-stu-id="c1189-178">Apply filters.</span></span> <span data-ttu-id="c1189-179">Choisissez entre **type**d'enquête \*\*\*\*, période, **État**ou une combinaison de ces éléments.</span><span class="sxs-lookup"><span data-stu-id="c1189-179">Choose from **Investigation Type**, **Time range**, **Status**, or a combination of these.</span></span>
- <span data-ttu-id="c1189-180">ExPortez les données dans un fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="c1189-180">Export the data to a CSV file.</span></span>

### <a name="investigation-graph"></a><span data-ttu-id="c1189-181">Graphique d'enquête</span><span class="sxs-lookup"><span data-stu-id="c1189-181">Investigation graph</span></span>

<span data-ttu-id="c1189-182">Lorsque vous ouvrez une enquête spécifique, vous voyez la page Graph de l'enquête.</span><span class="sxs-lookup"><span data-stu-id="c1189-182">When you open a specific investigation, you see the investigation graph page.</span></span> <span data-ttu-id="c1189-183">Cette page affiche toutes les entités différentes: les messages électroniques, les utilisateurs (ainsi que leurs activités) et les appareils qui ont été automatiquement analysés dans le cadre de l'alerte déclenchée.</span><span class="sxs-lookup"><span data-stu-id="c1189-183">This page shows all the different entities: email messages, users (and their activities), and devices that were automatically investigated as part of the alert that was triggered.</span></span>

![Page graphique d'enquête sur l'AIR](media/air-investigationgraphpage.png)

<span data-ttu-id="c1189-185">Vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="c1189-185">You can:</span></span>
- <span data-ttu-id="c1189-186">Obtenir une vue d'ensemble visuelle de l'enquête actuelle.</span><span class="sxs-lookup"><span data-stu-id="c1189-186">Get a visual overview of the current investigation.</span></span>
- <span data-ttu-id="c1189-187">Afficher un résumé du minutage de l'enquête.</span><span class="sxs-lookup"><span data-stu-id="c1189-187">View a summary of the investigation timings.</span></span>
- <span data-ttu-id="c1189-188">Sélectionnez un nœud dans la visualisation pour afficher les détails de ce nœud.</span><span class="sxs-lookup"><span data-stu-id="c1189-188">Select a node in the visualization to view details for that node.</span></span>
- <span data-ttu-id="c1189-189">Sélectionnez un onglet dans la partie supérieure pour afficher les détails de cet onglet.</span><span class="sxs-lookup"><span data-stu-id="c1189-189">Select a tab across the top to view details for that tab.</span></span>

### <a name="alert-investigation"></a><span data-ttu-id="c1189-190">Enquête sur les alertes</span><span class="sxs-lookup"><span data-stu-id="c1189-190">Alert investigation</span></span>

<span data-ttu-id="c1189-191">Dans l'onglet **alertes** pour une enquête, vous pouvez voir toutes les alertes relatives à l'enquête.</span><span class="sxs-lookup"><span data-stu-id="c1189-191">On the **Alerts** tab for an investigation, you can see all of the alerts relevant to the investigation.</span></span> <span data-ttu-id="c1189-192">Les détails incluent l'alerte qui a déclenché l'enquête et d'autres alertes, telles que la connexion à risque, le téléchargement en masse, etc., qui sont corrélées à l'enquête.</span><span class="sxs-lookup"><span data-stu-id="c1189-192">Details include the alert that triggered the investigation and other alerts, such as risky sign-in, mass download, etc., that are correlated to the investigation.</span></span> <span data-ttu-id="c1189-193">À partir de cette page, un analyste de sécurité peut également afficher des détails supplémentaires sur des alertes individuelles.</span><span class="sxs-lookup"><span data-stu-id="c1189-193">From this page, a security analyst can also view additional details on individual alerts.</span></span>

![Page alertes AÉRIENNEs](media/air-investigationalertspage.png)

<span data-ttu-id="c1189-195">Vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="c1189-195">You can:</span></span>
- <span data-ttu-id="c1189-196">Obtenir une vue d'ensemble visuelle de l'alerte de déclenchement actuelle et de toutes les alertes associées.</span><span class="sxs-lookup"><span data-stu-id="c1189-196">Get a visual overview of the current triggering alert and any associated alerts.</span></span>
- <span data-ttu-id="c1189-197">Sélectionnez une alerte dans la liste pour ouvrir une page de survol qui affiche les détails de l'alerte complète.</span><span class="sxs-lookup"><span data-stu-id="c1189-197">Select an alert in the list to open a fly-out page that shows full alert details.</span></span>

### <a name="email-investigation"></a><span data-ttu-id="c1189-198">Enquête par courrier électronique</span><span class="sxs-lookup"><span data-stu-id="c1189-198">Email investigation</span></span>

<span data-ttu-id="c1189-199">Dans l'onglet **e-mail** pour une enquête, vous pouvez voir tous les clusters de messagerie identifiés dans le cadre de l'enquête.</span><span class="sxs-lookup"><span data-stu-id="c1189-199">On the **Email** tab for an investigation, you can see all the email clusters identified as part of the investigation.</span></span> 

<span data-ttu-id="c1189-200">Étant donné le volume de courrier électronique que les utilisateurs d'une organisation envoient et reçoivent, le processus de</span><span class="sxs-lookup"><span data-stu-id="c1189-200">Given the sheer volume of email that users in an organization send and receive, the process of</span></span> 
- <span data-ttu-id="c1189-201">mise en cluster de messages électroniques en fonction d'attributs similaires d'un en-tête, d'un corps, d'une URL et d'une pièce jointe de message;</span><span class="sxs-lookup"><span data-stu-id="c1189-201">clustering email messages based on similar attributes from a message header, body, URL and attachment;</span></span> 
- <span data-ttu-id="c1189-202">séparation du courrier électronique malveillant du courrier électronique approprié; les</span><span class="sxs-lookup"><span data-stu-id="c1189-202">separating malicious email from the good email; and</span></span> 
- <span data-ttu-id="c1189-203">prendre des mesures sur les messages électroniques malveillants</span><span class="sxs-lookup"><span data-stu-id="c1189-203">taking action on malicious email messages</span></span> 

<span data-ttu-id="c1189-204">peut prendre plusieurs heures.</span><span class="sxs-lookup"><span data-stu-id="c1189-204">can take many hours.</span></span> <span data-ttu-id="c1189-205">AIR automatise ce processus en enregistrant le temps et les efforts de l'équipe de sécurité de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="c1189-205">AIR now automates this process, saving your organization's security team time and effort.</span></span> 

<span data-ttu-id="c1189-206">À titre d'exemple, considérez l'image suivante.</span><span class="sxs-lookup"><span data-stu-id="c1189-206">As an example, consider the following image.</span></span> <span data-ttu-id="c1189-207">Le premier cluster de trois messages électroniques était considéré comme un hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="c1189-207">The first cluster of three email messages were deemed to be phish.</span></span> <span data-ttu-id="c1189-208">Un autre cluster de messages similaires avec le même IP et le même objet a été trouvé et considéré comme malveillant, car certains d'entre eux ont été identifiés comme des hameçons lors de la détection initiale.</span><span class="sxs-lookup"><span data-stu-id="c1189-208">Another cluster of similar messages with the same IP and subject was found and is considered to be malicious, as some of them were identified as phish during initial detection.</span></span> 

![Page d'enquête sur le courrier électronique aérien](media/air-investigationemailpage.png)

<span data-ttu-id="c1189-210">Vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="c1189-210">You can:</span></span>
- <span data-ttu-id="c1189-211">Obtenir une vue d'ensemble visuelle des résultats de clustering actuels et des menaces détectées.</span><span class="sxs-lookup"><span data-stu-id="c1189-211">Get a visual overview of the current clustering results and threats found.</span></span>
- <span data-ttu-id="c1189-212">Cliquez sur une entité de cluster ou une liste de menaces pour ouvrir une page de survol qui affiche les détails de l'alerte complète.</span><span class="sxs-lookup"><span data-stu-id="c1189-212">Click a cluster entity or a threat list to open a fly-out page that shows the full alert details.</span></span>

![Courrier électronique d'enquête aérienne avec détails du menu volant](media/air-investigationemailpageflyoutdetails.png)

### <a name="user-investigation"></a><span data-ttu-id="c1189-214">Enquête utilisateur</span><span class="sxs-lookup"><span data-stu-id="c1189-214">User investigation</span></span>

<span data-ttu-id="c1189-215">Sous l'onglet **utilisateurs** , vous pouvez voir tous les utilisateurs identifiés dans le cadre de l'enquête.</span><span class="sxs-lookup"><span data-stu-id="c1189-215">On the **Users** tab, you can see all the users identified as part of the investigation.</span></span> 

<span data-ttu-id="c1189-216">Par exemple, dans l'image suivante, AIR a identifié des indicateurs de compromission et des anomalies en fonction d'une nouvelle règle de boîte de réception créée.</span><span class="sxs-lookup"><span data-stu-id="c1189-216">For example, in the following image, AIR has identified indicators of compromise and anomalies based on a new inbox rule that was created.</span></span> <span data-ttu-id="c1189-217">Des détails supplémentaires (preuve) de l'enquête sont disponibles par le biais d'affichages détaillés au sein de cet onglet.</span><span class="sxs-lookup"><span data-stu-id="c1189-217">Additional details (evidence) of the investigation are available through detailed views within this tab.</span></span>

![Page des utilisateurs de l'enquête aérienne](media/air-investigationuserspage.png)

<span data-ttu-id="c1189-219">Vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="c1189-219">You can:</span></span>
- <span data-ttu-id="c1189-220">Obtenir une vue d'ensemble visuelle des résultats et des risques utilisateur identifiés.</span><span class="sxs-lookup"><span data-stu-id="c1189-220">Get a visual overview of identified user results and risks found.</span></span>
- <span data-ttu-id="c1189-221">Sélectionnez un utilisateur pour ouvrir une page de survol qui affiche les détails de l'alerte complète.</span><span class="sxs-lookup"><span data-stu-id="c1189-221">Select a user to open a fly-out page that shows the full alert details.</span></span>

### <a name="machine-investigation"></a><span data-ttu-id="c1189-222">Enquête sur les machines</span><span class="sxs-lookup"><span data-stu-id="c1189-222">Machine investigation</span></span>

<span data-ttu-id="c1189-223">Sous l'onglet **ordinateurs** , vous pouvez voir tous les ordinateurs identifiés dans le cadre de l'enquête.</span><span class="sxs-lookup"><span data-stu-id="c1189-223">On the **Machines** tab, you can see all the machines identified as part of the investigation.</span></span> 

![Page de l'ordinateur d'enquête aérien](media/air-investigationmachinepage.png)

<span data-ttu-id="c1189-225">Dans le cadre de l'enquête, AIR établit une corrélation entre les menaces de messagerie et les appareils.</span><span class="sxs-lookup"><span data-stu-id="c1189-225">As part of the investigation, AIR correlates email threats to devices.</span></span> <span data-ttu-id="c1189-226">Par exemple, une enquête transmet un hachage de fichier à [Windows Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/windows-defender-advanced-threat-protection) pour enquêter.</span><span class="sxs-lookup"><span data-stu-id="c1189-226">For example, an investigation passes a file hash across to [Windows Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/windows-defender-advanced-threat-protection) to investigate.</span></span> <span data-ttu-id="c1189-227">Cela permet l'analyse automatisée des ordinateurs pertinents pour vos utilisateurs et vous aide à vous assurer que les menaces sont résolues dans le Cloud et sur vos appareils.</span><span class="sxs-lookup"><span data-stu-id="c1189-227">This allows for automated investigation of relevant machines for your users and helps to ensure that threats are addressed both in the cloud and across your devices.</span></span> 

<span data-ttu-id="c1189-228">Vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="c1189-228">You can:</span></span>
- <span data-ttu-id="c1189-229">Obtenir une vue d'ensemble visuelle des ordinateurs et menaces actuels détectés.</span><span class="sxs-lookup"><span data-stu-id="c1189-229">Get a visual overview of the current machines and threats found.</span></span>
- <span data-ttu-id="c1189-230">Sélectionnez un ordinateur pour ouvrir une vue dans les [recherches Windows Defender](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/automated-investigations-windows-defender-advanced-threat-protection)connexes connexes.</span><span class="sxs-lookup"><span data-stu-id="c1189-230">Select a machine to open a view that into the related [Windows Defender ATP investigations](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/automated-investigations-windows-defender-advanced-threat-protection).</span></span>

### <a name="entity-investigation"></a><span data-ttu-id="c1189-231">Enquête d'entité</span><span class="sxs-lookup"><span data-stu-id="c1189-231">Entity investigation</span></span>

<span data-ttu-id="c1189-232">Sous l'onglet **entités** , vous pouvez voir tous les ordinateurs identifiés dans le cadre de l'enquête.</span><span class="sxs-lookup"><span data-stu-id="c1189-232">On the **Entities** tab, you can see all the machines identified as part of the investigation.</span></span> 

<span data-ttu-id="c1189-233">Ici, vous pouvez voir les entités analysées.</span><span class="sxs-lookup"><span data-stu-id="c1189-233">Here, you can see the investigated entities.</span></span> <span data-ttu-id="c1189-234">Vous pouvez afficher les détails des types d'entités, tels que les messages électroniques, les clusters, les adresses IP, les utilisateurs et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="c1189-234">You can see details of the types of entities, such as email messages, clusters, IP addresses, users, and more.</span></span> <span data-ttu-id="c1189-235">Vous pouvez également voir le nombre d'entités analysées et les menaces associées à chacune d'elles.</span><span class="sxs-lookup"><span data-stu-id="c1189-235">You can also see how many entities were analyzed, and the threats that were associated with each.</span></span> 

![Page des entités d'enquête sur l'AIR](media/air-investigationentitiespage.png)

<span data-ttu-id="c1189-237">Vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="c1189-237">You can:</span></span>
- <span data-ttu-id="c1189-238">Obtenir une vue d'ensemble visuelle des entités d'enquête et des menaces détectées.</span><span class="sxs-lookup"><span data-stu-id="c1189-238">Get a visual overview of the investigation entities and threats found.</span></span>
- <span data-ttu-id="c1189-239">Sélectionnez une entité pour ouvrir une page de survol qui affiche le détail de l'entité associée.</span><span class="sxs-lookup"><span data-stu-id="c1189-239">Select an entity to open a fly-out page that shows the related entity detail.</span></span>

![Détails des entités d'enquête aérienne](media/air-investigationsentitiespagedetails.png)

### <a name="playbook-log"></a><span data-ttu-id="c1189-241">Journal des manifestes</span><span class="sxs-lookup"><span data-stu-id="c1189-241">Playbook log</span></span>

<span data-ttu-id="c1189-242">Sous l'onglet **Journal** , vous pouvez voir toutes les étapes du manuel qui ont eu lieu lors de l'enquête.</span><span class="sxs-lookup"><span data-stu-id="c1189-242">On the **Log** tab, you can see all the playbook steps that have occurred during the investigation.</span></span> <span data-ttu-id="c1189-243">Le journal capture un inventaire complet de toutes les actions effectuées par les fonctionnalités d'aide à la décision Office 365 dans le cadre de l'AIR.</span><span class="sxs-lookup"><span data-stu-id="c1189-243">The log captures a complete inventory of all actions completed by Office 365 Threat Intelligence capabilities as part of AIR.</span></span> <span data-ttu-id="c1189-244">Elle fournit une vue claire de toutes les étapes effectuées, y compris l'action elle-même, une description et la durée du début à la fin.</span><span class="sxs-lookup"><span data-stu-id="c1189-244">It provides a clear view of all the steps taken, including the Action itself, a description and the duration of the actual from start to finish.</span></span> 

![Page Journal d'enquête aérienne](media/air-investigationlogpage.png)

<span data-ttu-id="c1189-246">Vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="c1189-246">You can:</span></span>
- <span data-ttu-id="c1189-247">Obtenir une vue d'ensemble visuelle des étapes du manuel.</span><span class="sxs-lookup"><span data-stu-id="c1189-247">Get see a visual overview of the playbook steps taken.</span></span>
- <span data-ttu-id="c1189-248">ExPortez les résultats dans un fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="c1189-248">Export the results to a CSV file.</span></span>
- <span data-ttu-id="c1189-249">Filtrer l'affichage.</span><span class="sxs-lookup"><span data-stu-id="c1189-249">Filter the view.</span></span>

### <a name="recommended-actions"></a><span data-ttu-id="c1189-250">Actions recommandées</span><span class="sxs-lookup"><span data-stu-id="c1189-250">Recommended actions</span></span>

<span data-ttu-id="c1189-251">Sous l'onglet **actions** , vous pouvez voir toutes les actions de recherche qui sont recommandées pour la correction une fois l'enquête terminée.</span><span class="sxs-lookup"><span data-stu-id="c1189-251">On the **Actions** tab, you can see all the playbook actions that are recommended for remediation after the investigation has completed.</span></span> 

<span data-ttu-id="c1189-252">Actions capturez la liste complète de toutes les étapes que Microsoft vous recommande d'effectuer à la fin de l'enquête.</span><span class="sxs-lookup"><span data-stu-id="c1189-252">Actions capture a complete list of all the steps Microsoft recommends you take at the end of a investigation.</span></span> <span data-ttu-id="c1189-253">Vous pouvez prendre des mesures de correction ici en sélectionnant une ou plusieurs actions.</span><span class="sxs-lookup"><span data-stu-id="c1189-253">You can take remediation actions here by selecting one or more actions.</span></span> <span data-ttu-id="c1189-254">Si vous cliquez sur **approuver** , le début de la correction est autorisé.</span><span class="sxs-lookup"><span data-stu-id="c1189-254">Clicking **Approve** will allow remediation to begin.</span></span> <span data-ttu-id="c1189-255">(Des autorisations appropriées peuvent être requises.</span><span class="sxs-lookup"><span data-stu-id="c1189-255">(Appropriate permissions might be required.</span></span> <span data-ttu-id="c1189-256">Par exemple, un lecteur de sécurité peut afficher les actions mais pas les approuver.)</span><span class="sxs-lookup"><span data-stu-id="c1189-256">For example, a Security Reader can view actions but not approve them.)</span></span>  

![Page action de l'enquête par avion](media/air-investigationactionspage.png)

<span data-ttu-id="c1189-258">Vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="c1189-258">You can:</span></span>
- <span data-ttu-id="c1189-259">Obtenir une vue d'ensemble visuelle des actions recommandées.</span><span class="sxs-lookup"><span data-stu-id="c1189-259">Get a visual overview of the playbook-recommended actions.</span></span>
- <span data-ttu-id="c1189-260">Sélectionnez une ou plusieurs actions.</span><span class="sxs-lookup"><span data-stu-id="c1189-260">Select a single action or multiple actions.</span></span>
- <span data-ttu-id="c1189-261">Approuver les actions recommandées.</span><span class="sxs-lookup"><span data-stu-id="c1189-261">Approve recommended actions.</span></span> <span data-ttu-id="c1189-262">(Ceux-ci sont démarrés immédiatement avec les commentaires.)</span><span class="sxs-lookup"><span data-stu-id="c1189-262">(These are started immediately with comments.)</span></span>
- <span data-ttu-id="c1189-263">ExPortez les résultats dans un fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="c1189-263">Export the results to a CSV file.</span></span>
- <span data-ttu-id="c1189-264">Filtrer l'affichage.</span><span class="sxs-lookup"><span data-stu-id="c1189-264">Filter the view.</span></span>

## <a name="how-to-get-air"></a><span data-ttu-id="c1189-265">Comment obtenir de l'AIR</span><span class="sxs-lookup"><span data-stu-id="c1189-265">How to get AIR</span></span>

<span data-ttu-id="c1189-266">Actuellement, AIR est en préversion.</span><span class="sxs-lookup"><span data-stu-id="c1189-266">Currently, AIR is in preview.</span></span> <span data-ttu-id="c1189-267">Une fois diffusé, AIR est inclus dans les abonnements suivants:</span><span class="sxs-lookup"><span data-stu-id="c1189-267">When released, AIR will be included in the following subscriptions:</span></span>

- <span data-ttu-id="c1189-268">Microsoft 365 Entreprise E5</span><span class="sxs-lookup"><span data-stu-id="c1189-268">Microsoft 365 Enterprise E5</span></span>
- <span data-ttu-id="c1189-269">Office 365 Entreprise E5</span><span class="sxs-lookup"><span data-stu-id="c1189-269">Office 365 Enterprise E5</span></span>
- <span data-ttu-id="c1189-270">Protection contre les menaces Microsoft</span><span class="sxs-lookup"><span data-stu-id="c1189-270">Microsoft Threat Protection</span></span>
- <span data-ttu-id="c1189-271">Plan 2 de protection avancée contre les menaces Office 365</span><span class="sxs-lookup"><span data-stu-id="c1189-271">Office 365 Advanced Threat Protection Plan 2</span></span>

<span data-ttu-id="c1189-272">Pour en savoir plus sur la disponibilité des fonctionnalités, consultez la feuille de [route Microsoft 365](https://www.microsoft.com/microsoft-365/roadmap).</span><span class="sxs-lookup"><span data-stu-id="c1189-272">To learn more about feature availability, visit the [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap).</span></span>
