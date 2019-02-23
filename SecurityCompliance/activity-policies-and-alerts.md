---
title: Stratégies d’activité et alertes pour Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/28/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 367f25d3-10a0-4a91-bdae-70ebb7a79c98
description: Définir des stratégies d'activité avec Office 365 Cloud App Security pour configurer des alertes à déclencher lorsque des activités spécifiques se produisent ou se produisent trop fréquemment. En configurant des stratégies pour déclencher des alertes, vous pouvez être informé et surveiller des activités spécifiques.
ms.openlocfilehash: cfa58182ea35551ca3a3807c23e09c9f87c7be82
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219764"
---
# <a name="activity-policies-and-alerts-in-office-365-cloud-app-security"></a><span data-ttu-id="5fe11-104">Stratégies d’activité et alertes pour Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="5fe11-104">Activity policies and alerts in Office 365 Cloud App Security</span></span>

|<span data-ttu-id="5fe11-105">Évaluation \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="5fe11-105">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="5fe11-106">Planification \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="5fe11-106">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="5fe11-107">Déploiement \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="5fe11-107">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="5fe11-108">Utilisation \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="5fe11-108">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="5fe11-109">Commencer l'évaluation</span><span class="sxs-lookup"><span data-stu-id="5fe11-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="5fe11-110">Commencer la planification</span><span class="sxs-lookup"><span data-stu-id="5fe11-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="5fe11-111">Vous êtes là!</span><span class="sxs-lookup"><span data-stu-id="5fe11-111">You are here!</span></span>  <br/> [<span data-ttu-id="5fe11-112">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="5fe11-112">Next step</span></span>](anomaly-detection-policies-in-ocas.md) <br/> |[<span data-ttu-id="5fe11-113">Commencer à utiliser</span><span class="sxs-lookup"><span data-stu-id="5fe11-113">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |
   
<span data-ttu-id="5fe11-p102">Avec la sécurité des applications Cloud d'Office 365, les stratégies de gestion du Cloud avancées déclenchent des alertes pour des activités spécifiques qui se produisent ou se produisent trop fréquemment. Par exemple, supposons qu'un utilisateur tente de se connecter à Office 365 et échoue 70 fois à une minute. Supposons qu'un autre utilisateur télécharge 7 000 fichiers ou qu'il semble être connecté à partir du Canada, lorsque cet utilisateur est censé se trouver dans un autre emplacement. Ou pire, supposons que le compte d'une personne a été compromis, et qu'un agresseur utilise ce compte pour accéder aux applications Cloud et aux données sensibles de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="5fe11-p102">With Office 365 Cloud App Security, advanced cloud management policies trigger alerts for specific activities that happen or happen too frequently. For example, suppose a user tries to sign in to Office 365 and fails 70 times in one minute. Suppose that another user downloads 7,000 files, or appears to be signed in from Canada, when that user is supposed to be in another location. Or worse, suppose that someone's account has been compromised, and an attacker is using that account to access your organization's cloud apps and sensitive data.</span></span>
  
<span data-ttu-id="5fe11-p103">Si vous êtes un administrateur [général ou un administrateur de sécurité](permissions-in-the-security-and-compliance-center.md), les alertes d'activité vous avertissent lorsque des événements semblables à ceux-ci se produisent. Vous pouvez ensuite effectuer des actions spécifiques, telles que la suspension d'un compte d'utilisateur jusqu'à ce que vous puissiez examiner ce qui s'est passé.</span><span class="sxs-lookup"><span data-stu-id="5fe11-p103">If you are a [global administrator or security administrator](permissions-in-the-security-and-compliance-center.md), activity alerts notify you when events like these occur. You can then take specific actions, such as suspending a user account until you can investigate what happened.</span></span>
  
> [!NOTE]
> <span data-ttu-id="5fe11-p104">Les stratégies de sécurité d'application Cloud Office 365 sont différentes des [stratégies d'alerte dans &amp; le centre de sécurité conformité Office 365](alert-policies.md). Les stratégies d'activité décrites dans cet article sont définies dans le portail de sécurité des applications Cloud Office 365 et peuvent vous aider à mieux gérer l'environnement Cloud de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="5fe11-p104">Office 365 Cloud App Security policies are different from [alert policies in the Office 365 Security &amp; Compliance Center](alert-policies.md). The activity policies described in this article are defined in the Office 365 Cloud App Security portal, and can help you better manage your organization's cloud environment.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="5fe11-122">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="5fe11-122">Before you begin</span></span>

<span data-ttu-id="5fe11-123">Vérifiez que :</span><span class="sxs-lookup"><span data-stu-id="5fe11-123">Make sure that:</span></span>
  
- <span data-ttu-id="5fe11-124">Votre organisation dispose de la [sécurité des applications Cloud Office 365](office-365-cas-overview.md)et le service est [activé](turn-on-office-365-cas.md).</span><span class="sxs-lookup"><span data-stu-id="5fe11-124">Your organization has [Office 365 Cloud App Security](office-365-cas-overview.md), and the service is [turned on](turn-on-office-365-cas.md).</span></span>
    
- <span data-ttu-id="5fe11-125">La [journalIsation d'audit](turn-audit-log-search-on-or-off.md) est activée pour votre environnement Office 365.</span><span class="sxs-lookup"><span data-stu-id="5fe11-125">[Audit logging](turn-audit-log-search-on-or-off.md) is turned on for your Office 365 environment.</span></span> 
    
- <span data-ttu-id="5fe11-126">Vous êtes un administrateur général ou un administrateur de sécurité pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="5fe11-126">You are a global administrator or security administrator for Office 365.</span></span>
    
## <a name="create-a-new-activity-policy"></a><span data-ttu-id="5fe11-127">Créer une stratégie d'activité</span><span class="sxs-lookup"><span data-stu-id="5fe11-127">Create a new activity policy</span></span>

1. <span data-ttu-id="5fe11-128">En tant qu'administrateur général ou administrateur de sécurité, accédez au portail de sécurité des[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)applications Cloud () et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="5fe11-128">As a global administrator or security administrator, go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span> <br><span data-ttu-id="5fe11-129">Cette opération vous amène à la page stratégies de sécurité des applications Cloud Office 365.</span><span class="sxs-lookup"><span data-stu-id="5fe11-129">This takes you to the Office 365 Cloud App Security Policies page.</span></span><br><span data-ttu-id="5fe11-130">![Lorsque vous accédez au portail de sécurité des applications Cloud Office 365, vous commencez par la page stratégies.](media/5cb8833c-4e08-438c-bab3-91b5106f6f3f.png)</span><span class="sxs-lookup"><span data-stu-id="5fe11-130">![When you go to the Office 365 Cloud App Security portal, you start with the Policies page](media/5cb8833c-4e08-438c-bab3-91b5106f6f3f.png)</span></span>
  
2. <span data-ttu-id="5fe11-131">Cliquez sur **créer une stratégie**, puis sélectionnez stratégie d' **activité**.</span><span class="sxs-lookup"><span data-stu-id="5fe11-131">Click **Create policy**, and then select **Activity policy**.</span></span><br><span data-ttu-id="5fe11-132">![Lorsque vous créez une stratégie dans les autorités de certification O365, vous pouvez choisir entre les stratégies d'activité et les stratégies de détection des anomalies.](media/79f34535-ddf9-4a5b-a0a3-8766bf9c174c.png)</span><span class="sxs-lookup"><span data-stu-id="5fe11-132">![When you create a policy in O365 CAS, you can choose between Activity policies and Anomaly Detection policies.](media/79f34535-ddf9-4a5b-a0a3-8766bf9c174c.png)</span></span>
  
3. <span data-ttu-id="5fe11-p105">Sur la page **créer une stratégie d'activité** , spécifiez le nom et la **Description**de la **stratégie** . Pour baser votre stratégie sur un modèle par défaut, sélectionnez-en un dans la liste **modèle de stratégie** ou créez votre propre stratégie sans utiliser de modèle.</span><span class="sxs-lookup"><span data-stu-id="5fe11-p105">On the **Create activity policy** page, specify the **Policy name** and **Description**. To base your policy on a default template, choose one in the **Policy template** list, or create your own policy without using a template.</span></span><br><span data-ttu-id="5fe11-135">![Vous pouvez créer des stratégies d'activité avec Office 365 Cloud App Security.](media/4083a76f-7074-4d6a-8200-6d76d49259d7.png)</span><span class="sxs-lookup"><span data-stu-id="5fe11-135">![You can create activity policies with Office 365 Cloud App Security.](media/4083a76f-7074-4d6a-8200-6d76d49259d7.png)</span></span>
  
4. <span data-ttu-id="5fe11-p106">Choisissez une **gravité de stratégie** (faible, moyenne ou élevée) qui mesure son sérieux si cette stratégie déclenche une alerte. Cela vous permettra de filtrer les alertes lorsque vous les consulterez plus tard.</span><span class="sxs-lookup"><span data-stu-id="5fe11-p106">Choose a **Policy severity** (Low, Medium, or High) that measures how serious it is to you if this policy triggers an alert. This will help you filter alerts when you're reviewing them later.</span></span> 
    
5. <span data-ttu-id="5fe11-p107">Choisissez une **catégorie** pour cette stratégie. Cela vous permettra de filtrer et de trier les alertes qui ont été déclenchées, ou de regrouper les stratégies lorsque vous les consultez pour les modifier.</span><span class="sxs-lookup"><span data-stu-id="5fe11-p107">Choose a **Category** for this policy. This will help you filter and sort alerts that have been triggered, or to group policies when you're reviewing them to make changes.</span></span> 
    
6. <span data-ttu-id="5fe11-140">Choisissez **filtres d'activité** pour configurer d'autres actions ou mesures qui déclencheront une alerte en fonction de cette stratégie.</span><span class="sxs-lookup"><span data-stu-id="5fe11-140">Choose **Activity filters** to set up other actions or metrics that will trigger an alert based on this policy.</span></span> 
    
7. <span data-ttu-id="5fe11-141">Sous **paramètres de correspondance des activités**, indiquez si une violation de stratégie est déclenchée lorsqu'une seule activité correspond aux filtres ou si un nombre spécifié d'activités répétées est requis avant l'alerte.</span><span class="sxs-lookup"><span data-stu-id="5fe11-141">Under **Activity match parameters**, specify whether a policy violation will be triggered when a single activity matches the filters, or if a specified number of repeated activities is required before the alert triggers.</span></span><br><span data-ttu-id="5fe11-142">Si vous sélectionnez **activité répétée**, spécifiez le nombre d'activités, le délai et le nombre de fois qu'une violation doit être prise en compte pour un utilisateur au sein d'une application spécifique ou pour le même utilisateur avec n'importe quelle application.</span><span class="sxs-lookup"><span data-stu-id="5fe11-142">If you select **Repeated activity**, specify the number of activities, the time frame, and whether a violation will count for a user within a specific app or for the same user with any app.</span></span>
    
8. <span data-ttu-id="5fe11-143">Vous pouvez également sélectionner créer une **alerte** pour créer des alertes supplémentaires pour recevoir des notifications de cette stratégie (par courrier électronique, SMS ou les deux).</span><span class="sxs-lookup"><span data-stu-id="5fe11-143">Optionally, you can select **Create alert** to create additional alerts to receive notifications from this policy (via email, text message, or both).</span></span><br><span data-ttu-id="5fe11-144">Assurez-vous \*\*que votre fournisseur de courrier ne bloque pas les courriers électroniques envoyés à partir de `no-reply@cloudappsecurity.com` \*\*.</span><span class="sxs-lookup"><span data-stu-id="5fe11-144">**Make sure that your email provider doesn't block emails sent from `no-reply@cloudappsecurity.com`**.</span></span> 
  
9. <span data-ttu-id="5fe11-145">Choisissez les **actions** à effectuer lorsqu'une alerte est déclenchée pour suspendre l'utilisateur ou demander à l'utilisateur de se reconnecter aux applications Office 365.</span><span class="sxs-lookup"><span data-stu-id="5fe11-145">Choose the **Actions** that should be taken when an alert is triggered to suspend the user or require the user to sign in again to Office 365 apps.</span></span> 
    
10. <span data-ttu-id="5fe11-146">Sélectionnez **créer** pour terminer la création de votre stratégie.</span><span class="sxs-lookup"><span data-stu-id="5fe11-146">Choose **Create** to finish creating your policy.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="5fe11-147">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="5fe11-147">Next steps</span></span>

- [<span data-ttu-id="5fe11-148">Stratégies de détection des anomalies</span><span class="sxs-lookup"><span data-stu-id="5fe11-148">Anomaly detection policies</span></span>](anomaly-detection-policies-in-ocas.md)
    
- [<span data-ttu-id="5fe11-149">Intégration de votre serveur SIEM</span><span class="sxs-lookup"><span data-stu-id="5fe11-149">Integrate your SIEM server</span></span>](integrate-your-siem-server-with-office-365-cas.md)
    
- [<span data-ttu-id="5fe11-150">Passer en revue et effectuer une action sur les alertes</span><span class="sxs-lookup"><span data-stu-id="5fe11-150">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="5fe11-151">ReGroupez vos adresses IP pour simplifier la gestion</span><span class="sxs-lookup"><span data-stu-id="5fe11-151">Group your IP addresses to simplify management</span></span>](group-your-ip-addresses-in-ocas.md)
    

