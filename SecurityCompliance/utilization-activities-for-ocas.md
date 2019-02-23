---
title: Activités d’utilisation après avoir déployé la sécurité des applications cloud Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/28/2019
ms.audience: ITPro
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 86f414ad-81de-4703-b40a-c6615bbe9108
description: Une fois que vous avez configuré et déployé Office 365 Cloud App Security, vous devez effectuer certaines tâches pour vous assurer que votre configuration est correcte et que vous êtes prêt à effectuer des révisions régulières.
ms.openlocfilehash: 3afcfc307ea4a587287f3b71080bba89c715c908
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215944"
---
# <a name="utilization-activities-after-rolling-out-office-365-cloud-app-security"></a><span data-ttu-id="6b5a8-103">Activités d’utilisation après avoir déployé la sécurité des applications cloud Office 365</span><span class="sxs-lookup"><span data-stu-id="6b5a8-103">Utilization activities after rolling out Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="6b5a8-104">Évaluation \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="6b5a8-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="6b5a8-105">Planification \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="6b5a8-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="6b5a8-106">Déploiement \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="6b5a8-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="6b5a8-107">Utilisation \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="6b5a8-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="6b5a8-108">Commencer l'évaluation</span><span class="sxs-lookup"><span data-stu-id="6b5a8-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="6b5a8-109">Commencer la planification</span><span class="sxs-lookup"><span data-stu-id="6b5a8-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="6b5a8-110">Démarrer le déploiement</span><span class="sxs-lookup"><span data-stu-id="6b5a8-110">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="6b5a8-111">Vous êtes là!</span><span class="sxs-lookup"><span data-stu-id="6b5a8-111">You are here!</span></span>  <br/> [<span data-ttu-id="6b5a8-112">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="6b5a8-112">Next step</span></span>](review-office-365-cas-alerts.md) <br/> |
   
> [!NOTE]
> <span data-ttu-id="6b5a8-p101">Office 365 Cloud App Security est disponible dans Office 365 entreprise E5. Si votre organisation utilise un autre abonnement entreprise 365 Enterprise, Office 365 Cloud App Security peut être acheté en tant que module complémentaire. (en tant qu'administrateur général, dans le centre d'administration Office 365, sélectionnez **facturation** \> : **ajouter**des abonnements.) Pour plus d'informations, reportez-vous à [la rubrique office &amp; 365 Platform Service Description: Office 365 Security Compliance Center](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center) et [acheter ou modifier un composant additionnel pour Office 365 pour les entreprises](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).</span><span class="sxs-lookup"><span data-stu-id="6b5a8-p101">Office 365 Cloud App Security is available in Office 365 Enterprise E5. If your organization is using another Office 365 Enterprise subscription, Office 365 Cloud App Security can be purchased as an add-on. (As a global administrator, in the Office 365 admin center, choose **Billing** \> **Add subscriptions**.) For more information, see [Office 365 Platform Service Description: Office 365 Security &amp; Compliance Center](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center) and [Buy or edit an add-on for Office 365 for business](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).</span></span> 
  
<span data-ttu-id="6b5a8-116">Une fois que vous avez configuré et configuré Office 365 Cloud App Security, vous pouvez effectuer certaines tâches d'utilisation en tant qu'administrateur général ou administrateur de sécurité Office 365 pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="6b5a8-116">After you have set up and configured Office 365 Cloud App Security, you'll want to perform certain utilization tasks as an Office 365 global administrator or security administrator for your organization.</span></span> 

<span data-ttu-id="6b5a8-p102">En effectuant ces tâches, vous vous assurerez que la sécurité des applications Cloud d'Office 365 est correctement configurée, que vos stratégies sont à jour, et que votre organisation réalise la valeur à partir d'Office 365. Utilisez cet article pour vous aider à planifier ces tâches.</span><span class="sxs-lookup"><span data-stu-id="6b5a8-p102">By performing these tasks, you'll help ensure that Office 365 Cloud App Security is configured correctly, your policies are up to date, and your organization realizes value from Office 365. Use this article as a guide to help you plan for these tasks.</span></span>
  
> [!NOTE]
> <span data-ttu-id="6b5a8-p103">Vous devez être un administrateur général ou un administrateur de sécurité pour effectuer les tâches décrites dans cet article. Pour en savoir plus, consultez [la rubrique autorisations dans le &amp; Centre de sécurité conformité Office 365](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="6b5a8-p103">You must be a global administrator or security administrator to perform the tasks described in this article. To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
    
## <a name="activities-after-the-initial-configuration-and-rollout-of-office-365-cloud-app-security"></a><span data-ttu-id="6b5a8-121">Activités après la configuration initiale et le déploiement de la sécurité des applications Cloud Office 365</span><span class="sxs-lookup"><span data-stu-id="6b5a8-121">Activities after the initial configuration and rollout of Office 365 Cloud App Security</span></span>

<span data-ttu-id="6b5a8-122">Une fois que la sécurité des applications Cloud d'Office 365 est configurée et déployée, en tant qu'administrateur général ou administrateur de sécurité, vous devez prendre en compte les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="6b5a8-122">After Office 365 Cloud App Security is configured and rolled out, as a global administrator or security administrators, you have several things to consider:</span></span>
  
- <span data-ttu-id="6b5a8-123">Quelles tâches doivent être ajoutées au calendrier du service informatique?</span><span class="sxs-lookup"><span data-stu-id="6b5a8-123">What tasks need to be added to the IT department calendar?</span></span>
    
- <span data-ttu-id="6b5a8-124">Comment vous assurer que la sécurité des applications Cloud d'Office 365 est configurée pour utiliser le bon ensemble de stratégies au fil du temps?</span><span class="sxs-lookup"><span data-stu-id="6b5a8-124">How can you make sure Office 365 Cloud App Security is configured to use the right set of policies over time?</span></span>
    
- <span data-ttu-id="6b5a8-125">Quels types d'informations récapitulatives devez-vous envoyer à la chaîne de gestion informatique?</span><span class="sxs-lookup"><span data-stu-id="6b5a8-125">What kinds of summary information should you send up the IT management chain?</span></span>
    
<span data-ttu-id="6b5a8-126">Le tableau suivant résume brièvement les tâches en cours à effectuer et les tâches périodiques que vous devez envisager d'ajouter au calendrier de votre service informatique.</span><span class="sxs-lookup"><span data-stu-id="6b5a8-126">The following table briefly summarizes the ongoing tasks you'll want to perform and periodic tasks you should consider adding to your IT department's calendar.</span></span>
  
|<span data-ttu-id="6b5a8-127">**Tâches en cours**</span><span class="sxs-lookup"><span data-stu-id="6b5a8-127">**Ongoing tasks**</span></span>|<span data-ttu-id="6b5a8-128">**Tâches périodiques**</span><span class="sxs-lookup"><span data-stu-id="6b5a8-128">**Periodic tasks**</span></span>|
|:-----|:-----|
| <span data-ttu-id="6b5a8-129">SurVeillez les comptes de messagerie vers lesquels vous envoyez des messages d'alerte.</span><span class="sxs-lookup"><span data-stu-id="6b5a8-129">Monitor the email accounts to which you are sending alert messages</span></span>  <br/>  <span data-ttu-id="6b5a8-130">SurVeillez les flux d'actualités Cybersecurity pour les informations les plus récentes sur les nouvelles attaques informatiques</span><span class="sxs-lookup"><span data-stu-id="6b5a8-130">Monitor industry cybersecurity news feeds for the latest information about new cyber attacks</span></span>  <br/>  <span data-ttu-id="6b5a8-131">Agir sur les alertes de sécurité pour identifier et résoudre les incidents et les risques liés à la sécurité</span><span class="sxs-lookup"><span data-stu-id="6b5a8-131">Act on security alerts to identify and address security incidents and risks</span></span>  <br/>  <span data-ttu-id="6b5a8-132">Résumer chaque incident et résolution de sécurité dans un journal central</span><span class="sxs-lookup"><span data-stu-id="6b5a8-132">Summarize each security incident and resolution in a central log</span></span>  <br/> | <span data-ttu-id="6b5a8-133">Effectuer des révisions mensuelles ou trimestrielles des alertes de sécurité Office 365 Cloud App pour détecter les anomalies et analyser les tendances</span><span class="sxs-lookup"><span data-stu-id="6b5a8-133">Perform monthly or quarterly reviews of Office 365 Cloud App Security alerts to spot anomalies and analyze trends</span></span>  <br/>  <span data-ttu-id="6b5a8-134">Effectuer des révisions mensuelles ou trimestrielles de vos stratégies de sécurité Office 365 Cloud App existantes afin d'inclure des améliorations dans Office 365 Cloud App Security et de résoudre les nouvelles cyberattaques et tendances dans Cybersecurity</span><span class="sxs-lookup"><span data-stu-id="6b5a8-134">Perform monthly or quarterly reviews of your existing Office 365 Cloud App Security policies to include enhancements in Office 365 Cloud App Security and address new cyberattacks and trends in cybersecurity</span></span>  <br/> |
   
<span data-ttu-id="6b5a8-135">En fonction de la taille et de l'intérêt de votre organisation en matière de surveillance et de maintenance d'un groupe de sécurité stature, vous pouvez compiler un résumé mensuel pour votre chaîne de gestion informatique, notamment:</span><span class="sxs-lookup"><span data-stu-id="6b5a8-135">Depending on your organization's size and interest in monitoring and maintaining a security stature, you can compile a monthly summary for your IT management chain that includes:</span></span>
  
- <span data-ttu-id="6b5a8-136">Les différents types d'incidents de sécurité identifiés avec Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="6b5a8-136">The different types of security incidents identified with Office 365 Cloud App Security</span></span>
    
- <span data-ttu-id="6b5a8-137">Informations récapitulatives de votre journal central des incidents de sécurité, telles que le nombre d'incidents détectés</span><span class="sxs-lookup"><span data-stu-id="6b5a8-137">Summary information from your central log of the security incidents, such as number of incidents detected</span></span>
    
- <span data-ttu-id="6b5a8-138">Tendances des alertes et de la manière dont elles ont été traitées</span><span class="sxs-lookup"><span data-stu-id="6b5a8-138">Alert trends and how they were addressed</span></span>
    
- <span data-ttu-id="6b5a8-139">Les dernières tendances Cybersecurity</span><span class="sxs-lookup"><span data-stu-id="6b5a8-139">The latest cybersecurity trends</span></span>
    
- <span data-ttu-id="6b5a8-140">Recommandations concernant les modifications apportées à la stratégie de sécurité des applications Cloud Office 365 et leur impact sur les utilisateurs finaux</span><span class="sxs-lookup"><span data-stu-id="6b5a8-140">Recommendations for Office 365 Cloud App Security policy changes and their impact on end users</span></span>
    
## <a name="activities-after-time-has-passed-since-rolling-out-office-365-cloud-app-security"></a><span data-ttu-id="6b5a8-141">Activités une fois le temps écoulé depuis le déploiement de la sécurité des applications Cloud Office 365</span><span class="sxs-lookup"><span data-stu-id="6b5a8-141">Activities after time has passed since rolling out Office 365 Cloud App Security</span></span>

<span data-ttu-id="6b5a8-142">Si une durée prolongée a expiré depuis que vous avez initialement configuré ou géré vos stratégies de sécurité d'application Cloud Office 365, procédez comme suit pour revenir à une configuration reflétant les objectifs de sécurité de votre organisation et les fonctionnalités actuelles sur la sécurité des applications Cloud Office 365:</span><span class="sxs-lookup"><span data-stu-id="6b5a8-142">If a protracted amount of time has passed since you initially configured or maintained your Office 365 Cloud App Security policies, take the following steps to get back to a configuration that reflects your organization's security goals and the current capabilities of Office 365 Cloud App Security:</span></span>
  
1. <span data-ttu-id="6b5a8-143">Déterminez la date de la dernière modification de configuration pour la sécurité des applications Cloud Office 365.</span><span class="sxs-lookup"><span data-stu-id="6b5a8-143">Determine the date of the last configuration change for Office 365 Cloud App Security.</span></span>
    
2. <span data-ttu-id="6b5a8-p104">Comprenez votre configuration actuelle de la sécurité des applications Cloud d'Office 365 et ajustez ces stratégies selon vos besoins. Par exemple, assurez-vous que vous connaissez l'emplacement d'envoi des alertes par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="6b5a8-p104">Understand your current Office 365 Cloud App Security configuration and adjust those policies as needed. For example, make sure you know where alerts are being sent via email.</span></span>
    
3. <span data-ttu-id="6b5a8-146">Découvrez [les nouveautés d'office 365 Cloud App Security](new-in-office-365-cas.md) pour les modifications de produit depuis la dernière configuration de la sécurité des applications cloud Office 365.</span><span class="sxs-lookup"><span data-stu-id="6b5a8-146">See [what's new in Office 365 Cloud App Security](new-in-office-365-cas.md) for product changes since you last configured Office 365 Cloud App Security.</span></span> 
    
4. <span data-ttu-id="6b5a8-147">Effectuez une analyse des alertes et des journaux d'application Cloud App pour Office 365 pour repérer les anomalies et analyser les tendances.</span><span class="sxs-lookup"><span data-stu-id="6b5a8-147">Perform an analysis of Office 365 Cloud App Security alerts and logs to spot anomalies and analyze trends.</span></span>
    
5. <span data-ttu-id="6b5a8-148">Consultez les tendances du secteur industriel Cybersecurity pour connaître les menaces de sécurité les plus récentes.</span><span class="sxs-lookup"><span data-stu-id="6b5a8-148">Check industry cybersecurity trends to become aware of the latest security threats.</span></span>
    
6. <span data-ttu-id="6b5a8-p105">Effectuez une analyse des modifications qui doivent être apportées à l'ensemble actuel des stratégies de sécurité des applications Cloud Office 365. Incorporer les modifications des fonctionnalités de sécurité de l'application Cloud Office 365, les anomalies actuelles et les tendances Cybersecurity. ReCommandez les modifications apportées aux stratégies existantes ou à la création de nouvelles stratégies.</span><span class="sxs-lookup"><span data-stu-id="6b5a8-p105">Perform an analysis of the changes that need to be made to the current set of Office 365 Cloud App Security policies. Incorporate Office 365 Cloud App Security feature changes, current anomalies, and cybersecurity trends. Recommend changes to existing policies or the creation of new policies.</span></span>
    
7. <span data-ttu-id="6b5a8-p106">Planifiez l'implémentation des modifications de stratégie. Communiquez (socialiser) les conséquences des modifications proposées avec vos utilisateurs finaux, selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="6b5a8-p106">Make a plan for implementing the policy changes. Communicate (socialize) the consequences of the proposed changes with your end users as needed.</span></span>
    
8. <span data-ttu-id="6b5a8-154">Implémentez les modifications apportées à la stratégie de sécurité des applications Cloud Office 365.</span><span class="sxs-lookup"><span data-stu-id="6b5a8-154">Implement the Office 365 Cloud App Security policy changes.</span></span>
    
9. <span data-ttu-id="6b5a8-155">SurVeillez les commentaires des utilisateurs finaux et les alertes de sécurité Office 365 Cloud App et ajustez les stratégies au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="6b5a8-155">Monitor end user feedback and Office 365 Cloud App Security alerts and adjust policies over time.</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="6b5a8-156">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="6b5a8-156">Next steps</span></span>

- [<span data-ttu-id="6b5a8-157">Examiner une activité</span><span class="sxs-lookup"><span data-stu-id="6b5a8-157">Investigate an activity</span></span>](investigate-an-activity-in-office-365-cas.md)
    
- [<span data-ttu-id="6b5a8-158">Suspendre ou restaurer un compte d'utilisateur</span><span class="sxs-lookup"><span data-stu-id="6b5a8-158">Suspend or restore a user account</span></span>](suspend-or-restore-an-account-in-ocas.md)
    
- [<span data-ttu-id="6b5a8-159">Gérer les applications OAuth</span><span class="sxs-lookup"><span data-stu-id="6b5a8-159">Manage OAuth apps</span></span>](manage-app-permissions-in-ocas.md)
    
- [<span data-ttu-id="6b5a8-160">Passer en revue les détections d'applications dans la sécurité des applications cloud Office 365</span><span class="sxs-lookup"><span data-stu-id="6b5a8-160">Review app discovery findings in Office 365 Cloud App Security</span></span>](review-app-discovery-findings-in-ocas.md)
    
- <span data-ttu-id="6b5a8-161">Afficher la liste des [journaux de trafic Web et des sources de données](web-traffic-logs-and-data-sources-for-ocas.md) pris en charge</span><span class="sxs-lookup"><span data-stu-id="6b5a8-161">View a list of supported [Web traffic logs and data sources](web-traffic-logs-and-data-sources-for-ocas.md)</span></span>
    

