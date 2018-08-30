---
title: Activités de l’utilisation après le déploiement d’Office 365 Cloud Application Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/26/2018
ms.audience: ITPro
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 86f414ad-81de-4703-b40a-c6615bbe9108
description: Une fois que vous avez configuré et déployé Office 365 Cloud application sécurité, vous souhaiterez effectuer certaines tâches pour vous assurer que votre configuration est correcte et que vous êtes prêt pour révision régulière.
ms.openlocfilehash: bc8cfad8eb9d9444066c3193ec2978e9ffd9f56a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527871"
---
# <a name="utilization-activities-after-rolling-out-office-365-cloud-app-security"></a><span data-ttu-id="fd583-103">Activités de l’utilisation après le déploiement d’Office 365 Cloud Application Security</span><span class="sxs-lookup"><span data-stu-id="fd583-103">Utilization activities after rolling out Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="fd583-104">Évaluation **\>**</span><span class="sxs-lookup"><span data-stu-id="fd583-104">****Evaluation** \>**</span></span>|<span data-ttu-id="fd583-105">Planification **\>**</span><span class="sxs-lookup"><span data-stu-id="fd583-105">****Planning** \>**</span></span>|<span data-ttu-id="fd583-106">Déploiement **\>**</span><span class="sxs-lookup"><span data-stu-id="fd583-106">****Deployment** \>**</span></span>|<span data-ttu-id="fd583-107">Utilisation du \*\*\*</span><span class="sxs-lookup"><span data-stu-id="fd583-107">****Utilization****</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="fd583-108">Commencer à évaluer</span><span class="sxs-lookup"><span data-stu-id="fd583-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="fd583-109">Commencer à planifier</span><span class="sxs-lookup"><span data-stu-id="fd583-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="fd583-110">Commencer à déployer</span><span class="sxs-lookup"><span data-stu-id="fd583-110">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="fd583-111">Vous êtes ici !</span><span class="sxs-lookup"><span data-stu-id="fd583-111">You are here!</span></span>  <br/> [<span data-ttu-id="fd583-112">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="fd583-112">Next step</span></span>](review-office-365-cas-alerts.md) <br/> |
   
> [!NOTE]
> <span data-ttu-id="fd583-p101">Sécurité d’application Office 365 dans le nuage est disponible dans Office 365 entreprise E5. Si votre organisation utilise un autre abonnement Office 365 pour entreprises, Office 365 Cloud application sécurité peut être achetée comme module complémentaire. (En tant qu’administrateur global, dans le centre d’administration Office 365, choisissez **facturation** \> **abonnements Add**.) Pour plus d’informations, voir [Office 365 Platform Service Description : Office 365 sécurité &amp; centre de conformité](https://technet.microsoft.com/en-us/library/dn933793.aspx) et [acheter ou modifier un module complémentaire pour Office 365 pour entreprises](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).</span><span class="sxs-lookup"><span data-stu-id="fd583-p101">Office 365 Cloud App Security is available in Office 365 Enterprise E5. If your organization is using another Office 365 Enterprise subscription, Office 365 Cloud App Security can be purchased as an add-on. (As a global administrator, in the Office 365 admin center, choose **Billing** \> **Add subscriptions**.) For more information, see [Office 365 Platform Service Description: Office 365 Security &amp; Compliance Center](https://technet.microsoft.com/en-us/library/dn933793.aspx) and [Buy or edit an add-on for Office 365 for business](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).</span></span> 
  
<span data-ttu-id="fd583-116">Après avoir configuré et configuré la sécurité d’application Office 365 dans le nuage, vous souhaiterez effectuer certaines tâches de l’utilisation en tant qu’administrateur général Office 365 ou administrateur de sécurité de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="fd583-116">After you have set up and configured Office 365 Cloud App Security, you'll want to perform certain utilization tasks as an Office 365 global administrator or security administrator for your organization.</span></span> 

<span data-ttu-id="fd583-p102">En effectuant ces tâches, vous devez garantir que Office 365 Cloud Application Security est configuré correctement vos stratégies sont à jour et votre organisation réalise la valeur à partir d’Office 365. Utilisez cet article comme un guide pour vous aider à planifier ces tâches.</span><span class="sxs-lookup"><span data-stu-id="fd583-p102">By performing these tasks, you'll help ensure that Office 365 Cloud App Security is configured correctly, your policies are up to date, and your organization realizes value from Office 365. Use this article as a guide to help you plan for these tasks.</span></span>
  
> [!NOTE]
> <span data-ttu-id="fd583-p103">Vous devez être un administrateur global ou un administrateur de sécurité pour effectuer les tâches décrites dans cet article. Pour plus d’informations, voir [des autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="fd583-p103">You must be a global administrator or security administrator to perform the tasks described in this article. To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
    
## <a name="activities-after-the-initial-configuration-and-rollout-of-office-365-cloud-app-security"></a><span data-ttu-id="fd583-121">Activités après la configuration initiale et le déploiement de la sécurité d’application Office 365 dans le nuage</span><span class="sxs-lookup"><span data-stu-id="fd583-121">Activities after the initial configuration and rollout of Office 365 Cloud App Security</span></span>

<span data-ttu-id="fd583-122">Une fois que la sécurité d’application Office 365 dans le nuage est configurée et déployée en tant qu’administrateur général ou administrateurs de sécurité, vous avez plusieurs éléments à prendre en compte :</span><span class="sxs-lookup"><span data-stu-id="fd583-122">After Office 365 Cloud App Security is configured and rolled out, as a global administrator or security administrators, you have several things to consider:</span></span>
  
- <span data-ttu-id="fd583-123">Les tâches qui doivent être ajoutés au calendrier département informatique ?</span><span class="sxs-lookup"><span data-stu-id="fd583-123">What tasks need to be added to the IT department calendar?</span></span>
    
- <span data-ttu-id="fd583-124">Comment vous assurer que Office 365 Cloud Application Security est configuré pour utiliser le jeu de stratégies au fil du temps ?</span><span class="sxs-lookup"><span data-stu-id="fd583-124">How can you make sure Office 365 Cloud App Security is configured to use the right set of policies over time?</span></span>
    
- <span data-ttu-id="fd583-125">Quels types d’informations récapitulatives doit envoyer la chaîne de gestion informatique ?</span><span class="sxs-lookup"><span data-stu-id="fd583-125">What kinds of summary information should you send up the IT management chain?</span></span>
    
<span data-ttu-id="fd583-126">Le tableau suivant résume brièvement les tâches en cours, que vous souhaiterez pour effectuer des tâches périodiques, que vous devez envisager d’ajouter au calendrier de votre service informatique.</span><span class="sxs-lookup"><span data-stu-id="fd583-126">The following table briefly summarizes the ongoing tasks you'll want to perform and periodic tasks you should consider adding to your IT department's calendar.</span></span>
  
|<span data-ttu-id="fd583-127">**Tâches en cours**</span><span class="sxs-lookup"><span data-stu-id="fd583-127">**Ongoing tasks**</span></span>|<span data-ttu-id="fd583-128">**Tâches périodiques**</span><span class="sxs-lookup"><span data-stu-id="fd583-128">**Periodic tasks**</span></span>|
|:-----|:-----|
| <span data-ttu-id="fd583-129">Surveiller les comptes de messagerie à laquelle vous envoyez des messages d’alerte</span><span class="sxs-lookup"><span data-stu-id="fd583-129">Monitor the email accounts to which you are sending alert messages</span></span>  <br/>  <span data-ttu-id="fd583-130">Sécurité des échanges de news pour obtenir les dernières informations sur les nouvelles attaques informatiques Moniteur du secteur</span><span class="sxs-lookup"><span data-stu-id="fd583-130">Monitor industry cybersecurity news feeds for the latest information about new cyber attacks</span></span>  <br/>  <span data-ttu-id="fd583-131">Agir sur les alertes de sécurité pour identifier et résoudre les incidents de sécurité et les risques</span><span class="sxs-lookup"><span data-stu-id="fd583-131">Act on security alerts to identify and address security incidents and risks</span></span>  <br/>  <span data-ttu-id="fd583-132">Résumer chaque incident de sécurité et de la solution dans un journal central</span><span class="sxs-lookup"><span data-stu-id="fd583-132">Summarize each security incident and resolution in a central log</span></span>  <br/> | <span data-ttu-id="fd583-133">Effectuer des analyses mensuelles ou trimestrielles d’alertes de sécurité d’application Office 365 Cloud anomalies tons directs et l’analyse des tendances</span><span class="sxs-lookup"><span data-stu-id="fd583-133">Perform monthly or quarterly reviews of Office 365 Cloud App Security alerts to spot anomalies and analyze trends</span></span>  <br/>  <span data-ttu-id="fd583-134">Effectuer des analyses mensuelles ou trimestrielles de vos stratégies de sécurité pour application Cloud Microsoft Office 365 existants à inclure des améliorations dans cyberattaques nouvelle sécurité d’application Office 365 dans le nuage et l’adresse et les tendances de sécurité</span><span class="sxs-lookup"><span data-stu-id="fd583-134">Perform monthly or quarterly reviews of your existing Office 365 Cloud App Security policies to include enhancements in Office 365 Cloud App Security and address new cyberattacks and trends in cybersecurity</span></span>  <br/> |
   
<span data-ttu-id="fd583-135">Selon la taille et l’intérêt de surveillance et maintenance un malgré sa taille de la sécurité de votre organisation, vous pouvez compiler un résumé mensuel pour votre chaîne de gestion informatique qui inclut :</span><span class="sxs-lookup"><span data-stu-id="fd583-135">Depending on your organization's size and interest in monitoring and maintaining a security stature, you can compile a monthly summary for your IT management chain that includes:</span></span>
  
- <span data-ttu-id="fd583-136">Les différents types d’incidents de sécurité identifiés avec Office 365 Cloud application sécurité</span><span class="sxs-lookup"><span data-stu-id="fd583-136">The different types of security incidents identified with Office 365 Cloud App Security</span></span>
    
- <span data-ttu-id="fd583-137">Informations récapitulatives dans votre journal centrale des incidents de sécurité, telles que le nombre d’incidents détecté</span><span class="sxs-lookup"><span data-stu-id="fd583-137">Summary information from your central log of the security incidents, such as number of incidents detected</span></span>
    
- <span data-ttu-id="fd583-138">Tendances de l’alerte et la façon dont ils ont été traités</span><span class="sxs-lookup"><span data-stu-id="fd583-138">Alert trends and how they were addressed</span></span>
    
- <span data-ttu-id="fd583-139">Identifiez les tendances de sécurité le plus récent</span><span class="sxs-lookup"><span data-stu-id="fd583-139">The latest cybersecurity trends</span></span>
    
- <span data-ttu-id="fd583-140">Recommandations pour les modifications de stratégie de sécurité d’application Office 365 dans le nuage et leur impact sur les utilisateurs finaux</span><span class="sxs-lookup"><span data-stu-id="fd583-140">Recommendations for Office 365 Cloud App Security policy changes and their impact on end users</span></span>
    
## <a name="activities-after-time-has-passed-since-rolling-out-office-365-cloud-app-security"></a><span data-ttu-id="fd583-141">Une fois le temps écoulé depuis le déploiement d’Office 365 Cloud application sécurité les activités</span><span class="sxs-lookup"><span data-stu-id="fd583-141">Activities after time has passed since rolling out Office 365 Cloud App Security</span></span>

<span data-ttu-id="fd583-142">Si une durée prolongée s’est écoulé depuis vous initialement configuré ou conservé vos stratégies de sécurité d’application Office 365 dans le nuage, procédez comme suit pour revenir à une configuration qui reflète les objectifs de sécurité de votre organisation et les fonctionnalités actuelles de la sécurité des applications Office 365 nuage :</span><span class="sxs-lookup"><span data-stu-id="fd583-142">If a protracted amount of time has passed since you initially configured or maintained your Office 365 Cloud App Security policies, take the following steps to get back to a configuration that reflects your organization's security goals and the current capabilities of Office 365 Cloud App Security:</span></span>
  
1. <span data-ttu-id="fd583-143">Déterminer la date de la dernière modification de la configuration Office 365 nuage sécurité des applications.</span><span class="sxs-lookup"><span data-stu-id="fd583-143">Determine the date of the last configuration change for Office 365 Cloud App Security.</span></span>
    
2. <span data-ttu-id="fd583-p104">Comprendre votre configuration actuelle de la sécurité d’application Office 365 dans le nuage et ajuster les stratégies selon vos besoins. Par exemple, assurez-vous que vous savez où les alertes sont envoyées par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="fd583-p104">Understand your current Office 365 Cloud App Security configuration and adjust those policies as needed. For example, make sure you know where alerts are being sent via email.</span></span>
    
3. <span data-ttu-id="fd583-146">Dans la mesure où vous avez configuré dernière sécurité d’application Office 365 dans le nuage, voir [Nouveautés de la sécurité pour application Cloud Microsoft Office 365](new-in-office-365-cas.md) pour les modifications apportées au produit.</span><span class="sxs-lookup"><span data-stu-id="fd583-146">See [what's new in Office 365 Cloud App Security](new-in-office-365-cas.md) for product changes since you last configured Office 365 Cloud App Security.</span></span> 
    
4. <span data-ttu-id="fd583-147">Effectuer une analyse des alertes de sécurité d’application Office 365 dans le nuage et journaux anomalies tons directs et analyser des tendances.</span><span class="sxs-lookup"><span data-stu-id="fd583-147">Perform an analysis of Office 365 Cloud App Security alerts and logs to spot anomalies and analyze trends.</span></span>
    
5. <span data-ttu-id="fd583-148">Vérifiez les tendances de sécurité pris connaissance des menaces de sécurité le plus récent.</span><span class="sxs-lookup"><span data-stu-id="fd583-148">Check industry cybersecurity trends to become aware of the latest security threats.</span></span>
    
6. <span data-ttu-id="fd583-p105">Effectuer une analyse des modifications qui doivent être effectuées à l’ensemble actuel des stratégies de sécurité d’application Office 365 dans le nuage. Intégrer Office 365 Cloud application sécurité modifications apportées aux fonctionnalités, anomalies actuels et tendances de sécurité. Recommander des modifications à des stratégies existantes ou la création de nouvelles stratégies.</span><span class="sxs-lookup"><span data-stu-id="fd583-p105">Perform an analysis of the changes that need to be made to the current set of Office 365 Cloud App Security policies. Incorporate Office 365 Cloud App Security feature changes, current anomalies, and cybersecurity trends. Recommend changes to existing policies or the creation of new policies.</span></span>
    
7. <span data-ttu-id="fd583-p106">Créer un plan pour implémenter les modifications de stratégie. Communiquer (communiquent) les conséquences des modifications proposées avec vos utilisateurs finaux selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="fd583-p106">Make a plan for implementing the policy changes. Communicate (socialize) the consequences of the proposed changes with your end users as needed.</span></span>
    
8. <span data-ttu-id="fd583-154">Implémenter les modifications de stratégie de sécurité d’application Office 365 dans le nuage.</span><span class="sxs-lookup"><span data-stu-id="fd583-154">Implement the Office 365 Cloud App Security policy changes.</span></span>
    
9. <span data-ttu-id="fd583-155">Surveiller les commentaires des utilisateurs finaux et les alertes de sécurité d’application Office 365 dans le nuage et ajuster les stratégies au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="fd583-155">Monitor end user feedback and Office 365 Cloud App Security alerts and adjust policies over time.</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="fd583-156">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="fd583-156">Next steps</span></span>

- [<span data-ttu-id="fd583-157">Rechercher une activité</span><span class="sxs-lookup"><span data-stu-id="fd583-157">Investigate an activity</span></span>](investigate-an-activity-in-office-365-cas.md)
    
- [<span data-ttu-id="fd583-158">Suspendre ou restaurer un compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="fd583-158">Suspend or restore a user account</span></span>](suspend-or-restore-an-account-in-ocas.md)
    
- [<span data-ttu-id="fd583-159">Gérer les autorisations d’application</span><span class="sxs-lookup"><span data-stu-id="fd583-159">Manage app permissions</span></span>](manage-app-permissions-in-ocas.md)
    
- [<span data-ttu-id="fd583-160">Passez en revue les conclusions de découverte d’application dans Office 365 Cloud application sécurité</span><span class="sxs-lookup"><span data-stu-id="fd583-160">Review app discovery findings in Office 365 Cloud App Security</span></span>](review-app-discovery-findings-in-ocas.md)
    
- <span data-ttu-id="fd583-161">Afficher la liste des [sources de données et journaux de trafic Web](web-traffic-logs-and-data-sources-for-ocas.md) pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd583-161">View a list of supported [Web traffic logs and data sources](web-traffic-logs-and-data-sources-for-ocas.md)</span></span>
    

