---
title: Passer en revue et effectuer une action sur les alertes dans la sécurité des applications cloud Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 97e9c3d9-df89-458e-924b-369becee5532
description: Utilisez la page des alertes dans Office 365 Cloud App Security pour afficher les problèmes potentiels et prendre des mesures. Vous pouvez ignorer ou résoudre les alertes et, si nécessaire, suspendre un compte d'utilisateur.
ms.openlocfilehash: 6c2f9788cb238e86abc347a3a118eb08fa84e971
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30213164"
---
# <a name="review-and-take-action-on-alerts-in-office-365-cloud-app-security"></a><span data-ttu-id="60971-104">Passer en revue et effectuer une action sur les alertes dans la sécurité des applications cloud Office 365</span><span class="sxs-lookup"><span data-stu-id="60971-104">Review and take action on alerts in Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="60971-105">Évaluation \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="60971-105">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="60971-106">Planification \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="60971-106">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="60971-107">Déploiement \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="60971-107">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="60971-108">Utilisation \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="60971-108">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="60971-109">Commencer l'évaluation</span><span class="sxs-lookup"><span data-stu-id="60971-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="60971-110">Commencer la planification</span><span class="sxs-lookup"><span data-stu-id="60971-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="60971-111">Démarrer le déploiement</span><span class="sxs-lookup"><span data-stu-id="60971-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="60971-112">Vous êtes là!</span><span class="sxs-lookup"><span data-stu-id="60971-112">You are here!</span></span>  <br/> [<span data-ttu-id="60971-113">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="60971-113">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="60971-114">Vous pouvez utiliser la page des alertes dans Office 365 Cloud App Security pour afficher les problèmes potentiels et, si nécessaire, prendre des mesures.</span><span class="sxs-lookup"><span data-stu-id="60971-114">You can use the Alerts page in Office 365 Cloud App Security to view potential issues and, if needed, take action.</span></span>
  
> [!NOTE]
> <span data-ttu-id="60971-p102">Vous devez être un administrateur général ou un administrateur de sécurité pour effectuer les tâches décrites dans cet article. Consultez [la rubrique autorisations dans le centre &amp; de sécurité conformité Office 365](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="60971-p102">You must be a global administrator or security administrator to perform the tasks in this article. See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
## <a name="how-to-get-to-the-alerts-page"></a><span data-ttu-id="60971-117">Comment accéder à la page des alertes?</span><span class="sxs-lookup"><span data-stu-id="60971-117">How to get to the Alerts page</span></span>

1. <span data-ttu-id="60971-118">Accédez au portail de sécurité des applications Cloud[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)() et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="60971-118">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span>
  
2. <span data-ttu-id="60971-119">Dans la barre de navigation en haut de l'écran, sélectionnez **alertes**.</span><span class="sxs-lookup"><span data-stu-id="60971-119">In the navigation bar across the top of the screen, choose **Alerts**.</span></span><br/><span data-ttu-id="60971-120">![Sur la page alertes, vous pouvez voir les alertes déclenchées et toutes les actions entreprises.](media/3b53d4c9-4b13-435d-8547-8c0f9ae6b914.png)</span><span class="sxs-lookup"><span data-stu-id="60971-120">![On the Alerts page, you can see alerts that were triggered and any actions taken.](media/3b53d4c9-4b13-435d-8547-8c0f9ae6b914.png)</span></span>
  
## <a name="review-and-handle-alerts"></a><span data-ttu-id="60971-121">Examiner et gérer les alertes</span><span class="sxs-lookup"><span data-stu-id="60971-121">Review and handle alerts</span></span>

<span data-ttu-id="60971-p103">Les alertes vous aident à identifier les activités dans votre environnement Cloud Office 365 que vous souhaiterez peut-être approfondir. Vous pouvez également décider de créer de nouvelles stratégies ou de modifier des stratégies existantes en fonction des alertes que vous voyez. Par exemple, si vous voyez un administrateur qui se connecte à partir d'un emplacement étrange, vous pouvez décider de configurer une stratégie qui empêche les administrateurs de se connecter à Office 365 à partir de certains emplacements.</span><span class="sxs-lookup"><span data-stu-id="60971-p103">Alerts help you identify activities in your Office 365 cloud environment that you might want to investigate further. You might also decide to create new policies or edit existing policies based on the alerts you see. For example, if you see an administrator logging on from a strange location, you may decide to set up a policy that prevents administrators from signing in to Office 365 from certain locations.</span></span>
  
> [!TIP]
> <span data-ttu-id="60971-125">Vous pouvez filtrer les alertes par **catégorie** ou par **gravité** afin de gérer les plus importantes en premier.</span><span class="sxs-lookup"><span data-stu-id="60971-125">You can filter the alerts by **Category** or by **Severity** so you can manage the most important ones first.</span></span> 
  
<span data-ttu-id="60971-p104">Pour chaque alerte, examinez ce qui a provoqué cette action afin de décider de l'action à effectuer. Pour afficher plus de détails sur une alerte et agir comme la résolution de l'alerte ou la suspension d'un compte d'utilisateur, choisissez l'alerte pour ouvrir une page de détails. Sur la page détails, vous pouvez consulter le journal d'activité, les comptes et les utilisateurs qui sont associés à l'alerte, et effectuer des actions telles que les suivantes:</span><span class="sxs-lookup"><span data-stu-id="60971-p104">For each alert, look into what caused it so you can decide what action to take. To see more details about an alert and to take action, such as resolving the alert or suspending a users account, choose the alert to open a details page. On the details page, you can review the activity log, accounts, and users that are related to the alert, and take actions such as the following:</span></span>
  
- <span data-ttu-id="60971-p105">**Faire disparaître** Si l'alerte était un faux positif, faites-la disparaître. Vous pouvez éventuellement ajouter un commentaire expliquant la raison pour laquelle vous l'avez rejetée.</span><span class="sxs-lookup"><span data-stu-id="60971-p105">**Dismiss** If the alert was a false positive, dismiss it. You can optionally add a comment explaining why you dismissed it.</span></span> 
    
- <span data-ttu-id="60971-p106">**Résoudre l'alerte** Si l'alerte a été déclenchée par une activité qui n'est pas une menace, résolvez-la. Vous pouvez éventuellement ajouter un commentaire expliquant la raison pour laquelle vous l'avez résolue.</span><span class="sxs-lookup"><span data-stu-id="60971-p106">**Resolve alert** If the alert was triggered by an activity that you know isn't a threat, resolve it. You can optionally add a comment explaining why you resolved it.</span></span> 
    
- <span data-ttu-id="60971-133">**Suspendre** Si vous suspectez des signes non autorisés sur un compte, par exemple, une personne se connectant à partir d'un autre pays lorsque vous avez la certitude qu'il s'agit physiquement d'un bureau local, vous pouvez [suspendre le compte](suspend-or-restore-an-account-in-ocas.md) pendant que vous examinez ce qui se passe.</span><span class="sxs-lookup"><span data-stu-id="60971-133">**Suspend** If you suspect unauthorized sign ins on an account, for example, someone signing in from another country when you know that person is physically at a local office, you can [suspend the account](suspend-or-restore-an-account-in-ocas.md) while you investigate what's going on.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="60971-134">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="60971-134">Next steps</span></span>

- [<span data-ttu-id="60971-135">Examiner une activité</span><span class="sxs-lookup"><span data-stu-id="60971-135">Investigate an activity</span></span>](investigate-an-activity-in-office-365-cas.md)
    
- [<span data-ttu-id="60971-136">Suspendre ou restaurer un compte d'utilisateur</span><span class="sxs-lookup"><span data-stu-id="60971-136">Suspend or restore a user account</span></span>](suspend-or-restore-an-account-in-ocas.md)
    
- <span data-ttu-id="60971-137">Afficher la liste des [journaux de trafic Web et des sources de données](web-traffic-logs-and-data-sources-for-ocas.md) pris en charge</span><span class="sxs-lookup"><span data-stu-id="60971-137">View a list of supported [Web traffic logs and data sources](web-traffic-logs-and-data-sources-for-ocas.md)</span></span>
    
- <span data-ttu-id="60971-138">Examiner vos [activités d'utilisation pour Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="60971-138">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

