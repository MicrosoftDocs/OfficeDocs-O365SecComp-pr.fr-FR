---
title: Stratégies d’activité et alertes pour Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/26/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 367f25d3-10a0-4a91-bdae-70ebb7a79c98
description: Définir des stratégies d’activité avec Office 365 Cloud application sécurité pour définir des alertes se déclenche lorsque des activités spécifiques se produire ou se produire trop souvent. En définissant des stratégies pour déclencher les alertes, vous pourrez être averti et surveiller les activités spécifiques.
ms.openlocfilehash: 6f5039d09dea98de970ab4bd28e95a6cfad73db4
ms.sourcegitcommit: 9034809b6f308bedc3b8ddcca8242586b5c30f94
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/15/2019
ms.locfileid: "28015006"
---
# <a name="activity-policies-and-alerts-in-office-365-cloud-app-security"></a><span data-ttu-id="59f13-104">Stratégies d’activité et alertes pour Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="59f13-104">Activity policies and alerts in Office 365 Cloud App Security</span></span>

<span data-ttu-id="59f13-105">Gestion de la sécurité Office 365 avancée est désormais sécurité d’application Office 365 dans le nuage.</span><span class="sxs-lookup"><span data-stu-id="59f13-105">Office 365 Advanced Security Management is now Office 365 Cloud App Security.</span></span>
  
|<span data-ttu-id="59f13-106">Évaluation **\>**</span><span class="sxs-lookup"><span data-stu-id="59f13-106">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="59f13-107">Planification **\>**</span><span class="sxs-lookup"><span data-stu-id="59f13-107">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="59f13-108">Déploiement **\>**</span><span class="sxs-lookup"><span data-stu-id="59f13-108">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="59f13-109">Utilisation du \*\*\*</span><span class="sxs-lookup"><span data-stu-id="59f13-109">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="59f13-110">Commencer à évaluer</span><span class="sxs-lookup"><span data-stu-id="59f13-110">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="59f13-111">Commencer à planifier</span><span class="sxs-lookup"><span data-stu-id="59f13-111">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="59f13-112">Vous êtes ici !</span><span class="sxs-lookup"><span data-stu-id="59f13-112">You are here!</span></span>  <br/> [<span data-ttu-id="59f13-113">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="59f13-113">Next step</span></span>](anomaly-detection-policies-in-ocas.md) <br/> |[<span data-ttu-id="59f13-114">Commencer à utiliser</span><span class="sxs-lookup"><span data-stu-id="59f13-114">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |
   
<span data-ttu-id="59f13-p102">Avec Office 365 Cloud application sécurité, des stratégies de gestion avancée sur le nuage déclenchent des alertes pour des actions spécifiques se produire ou se produire trop souvent. Par exemple, supposons qu’un utilisateur tente de se connecter à Office 365 et échoue 70 heures dans une minute. Supposons qu’un autre utilisateur télécharge 7 000 fichiers ou semble être connecté à partir du Canada, lorsque cet utilisateur est supposé pour être dans un autre emplacement. Ou pire, supposons que le compte d’une personne a été compromis et une personne malveillante utilise ce compte pour accéder aux applications de cloud de votre organisation et les données sensibles.</span><span class="sxs-lookup"><span data-stu-id="59f13-p102">With Office 365 Cloud App Security, advanced cloud management policies trigger alerts for specific activities that happen or happen too frequently. For example, suppose a user tries to sign in to Office 365 and fails 70 times in one minute. Suppose that another user downloads 7,000 files, or appears to be signed in from Canada, when that user is supposed to be in another location. Or worse, suppose that someone's account has been compromised, and an attacker is using that account to access your organization's cloud apps and sensitive data.</span></span>
  
<span data-ttu-id="59f13-p103">Si vous êtes un [administrateur global ou administrateur de la sécurité](permissions-in-the-security-and-compliance-center.md), activité alertes lorsque les événements tels que ceux-ci se produisent. Vous pouvez ensuite effectuer des actions spécifiques, telles que la suspension d’un compte d’utilisateur jusqu'à ce que vous pouvez vérifier qu’en est-il de.</span><span class="sxs-lookup"><span data-stu-id="59f13-p103">If you are a [global administrator or security administrator](permissions-in-the-security-and-compliance-center.md), activity alerts notify you when events like these occur. You can then take specific actions, such as suspending a user account until you can investigate what happened.</span></span>
  
> [!NOTE]
> <span data-ttu-id="59f13-p104">Stratégies de sécurité des applications dans le nuage Office 365 sont différents de [stratégies de sécurité Office 365 d’alerte &amp; centre de conformité](alert-policies.md). L’activité politiques décrites dans cet article sont définis dans le portail Office 365 Cloud Application Security et peuvent vous aider à mieux gérer l’environnement de votre organisation en nuage.</span><span class="sxs-lookup"><span data-stu-id="59f13-p104">Office 365 Cloud App Security policies are different from [alert policies in the Office 365 Security &amp; Compliance Center](alert-policies.md). The activity policies described in this article are defined in the Office 365 Cloud App Security portal, and can help you better manage your organization's cloud environment.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="59f13-123">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="59f13-123">Before you begin</span></span>

<span data-ttu-id="59f13-124">Vérifiez que :</span><span class="sxs-lookup"><span data-stu-id="59f13-124">Make sure that:</span></span>
  
- <span data-ttu-id="59f13-125">Votre organisation dispose de [Sécurité d’application Office 365 dans le nuage](office-365-cas-overview.md)et le service est [activé](turn-on-office-365-cas.md).</span><span class="sxs-lookup"><span data-stu-id="59f13-125">Your organization has [Office 365 Cloud App Security](office-365-cas-overview.md), and the service is [turned on](turn-on-office-365-cas.md).</span></span>
    
- <span data-ttu-id="59f13-126">[L’enregistrement d’audit](turn-audit-log-search-on-or-off.md) est activé pour votre environnement Office 365.</span><span class="sxs-lookup"><span data-stu-id="59f13-126">[Audit logging](turn-audit-log-search-on-or-off.md) is turned on for your Office 365 environment.</span></span> 
    
- <span data-ttu-id="59f13-127">Vous êtes un administrateur global ou un administrateur de sécurité pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="59f13-127">You are a global administrator or security administrator for Office 365.</span></span>
    
## <a name="create-a-new-activity-policy"></a><span data-ttu-id="59f13-128">Créer une nouvelle stratégie d’activité</span><span class="sxs-lookup"><span data-stu-id="59f13-128">Create a new activity policy</span></span>

1. <span data-ttu-id="59f13-129">En tant qu’un administrateur global ou administrateur de sécurité, accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous à l’aide de votre compte professionnel ou de l’école.</span><span class="sxs-lookup"><span data-stu-id="59f13-129">As a global administrator or security administrator, go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account.</span></span> 
    
2. <span data-ttu-id="59f13-130">Dans la sécurité &amp; centre de conformité, sélectionnez **alertes** \> **Gestion avancée des alertes**.</span><span class="sxs-lookup"><span data-stu-id="59f13-130">In the Security &amp; Compliance Center, choose **Alerts** \> **Manage advanced alerts**.</span></span>
    
3. <span data-ttu-id="59f13-131">Cliquez sur **Aller à la sécurité d’application Office 365 dans le nuage**.</span><span class="sxs-lookup"><span data-stu-id="59f13-131">Choose **Go to Office 365 Cloud App Security**.</span></span>
    
    <span data-ttu-id="59f13-132">Vous accédez à la page de stratégies de sécurité des applications Office 365 dans le nuage.</span><span class="sxs-lookup"><span data-stu-id="59f13-132">This takes you to the Office 365 Cloud App Security Policies page.</span></span>
    
    ![Lorsque vous accédez au portail Office 365 Cloud Application Security, vous démarrez avec la page de stratégies](media/5cb8833c-4e08-438c-bab3-91b5106f6f3f.png)
  
4. <span data-ttu-id="59f13-134">Cliquez sur **créer une stratégie**, puis sélectionnez la **stratégie de l’activité**.</span><span class="sxs-lookup"><span data-stu-id="59f13-134">Click **Create policy**, and then select **Activity policy**.</span></span>
    
    ![Lorsque vous créez une stratégie dans O365 autorités de certification, vous pouvez choisir entre les stratégies de l’activité et de détection des anomalies.](media/79f34535-ddf9-4a5b-a0a3-8766bf9c174c.png)
  
5. <span data-ttu-id="59f13-p105">Dans la page **créer une stratégie activité** , spécifiez le **nom de la stratégie** et la **Description**. Pour baser votre stratégie sur un modèle par défaut, choisissez dans la liste **modèle de stratégie** , ou créer votre propre stratégie sans utiliser de modèle.</span><span class="sxs-lookup"><span data-stu-id="59f13-p105">On the **Create activity policy** page, specify the **Policy name** and **Description**. To base your policy on a default template, choose one in the **Policy template** list, or create your own policy without using a template.</span></span> 
    
    ![Vous pouvez créer des stratégies de l’activité avec Office 365 Cloud Application Security.](media/4083a76f-7074-4d6a-8200-6d76d49259d7.png)
  
6. <span data-ttu-id="59f13-p106">Choisissez une **gravité stratégie** (faible, moyen ou élevé) qui mesure grave comment il doit vous si cette stratégie déclenche une alerte. Cela vous permettra de filtrer les alertes lorsque vous êtes de les consulter ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="59f13-p106">Choose a **Policy severity** (Low, Medium, or High) that measures how serious it is to you if this policy triggers an alert. This will help you filter alerts when you're reviewing them later.</span></span> 
    
7. <span data-ttu-id="59f13-p107">Choisissez une **catégorie** pour cette stratégie. Cela vous permettra de filtrer et trier les alertes qui ont été déclenchés, ou aux stratégies de groupe, lorsque vous êtes en examinant les apporter des modifications.</span><span class="sxs-lookup"><span data-stu-id="59f13-p107">Choose a **Category** for this policy. This will help you filter and sort alerts that have been triggered, or to group policies when you're reviewing them to make changes.</span></span> 
    
8. <span data-ttu-id="59f13-143">Choisissez **filtres d’activité** pour configurer d’autres actions ou les mesures qui déclenchent une alerte basée sur cette stratégie.</span><span class="sxs-lookup"><span data-stu-id="59f13-143">Choose **Activity filters** to set up other actions or metrics that will trigger an alert based on this policy.</span></span> 
    
9. <span data-ttu-id="59f13-144">Sous l' **activité correspondent aux paramètres**, spécifiez si une violation de stratégie sera déclenchée lorsqu’une activité unique établit une correspondance avec les filtres, ou si un nombre spécifié d’activités est requise avant les déclencheurs de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="59f13-144">Under **Activity match parameters**, specify whether a policy violation will be triggered when a single activity matches the filters, or if a specified number of repeated activities is required before the alert triggers.</span></span>
    
    <span data-ttu-id="59f13-145">Si vous sélectionnez **activité répétée**, spécifiez le nombre d’activités, le critère de temps, et si une violation de compte pour un utilisateur au sein d’une application spécifique ou pour le même utilisateur avec n’importe quelle application.</span><span class="sxs-lookup"><span data-stu-id="59f13-145">If you select **Repeated activity**, specify the number of activities, the time frame, and whether a violation will count for a user within a specific app or for the same user with any app.</span></span>
    
10. <span data-ttu-id="59f13-146">Si vous le souhaitez, vous pouvez sélectionner **alerte créer** pour créer des alertes supplémentaires pour recevoir des notifications de cette stratégie (via le courrier électronique, message texte ou les deux).</span><span class="sxs-lookup"><span data-stu-id="59f13-146">Optionally, you can select **Create alert** to create additional alerts to receive notifications from this policy (via email, text message, or both).</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="59f13-147">Assurez-vous que votre fournisseur de messagerie électronique ne bloque pas les messages électroniques envoyés à partir de no-reply@cloudappsecurity.com.</span><span class="sxs-lookup"><span data-stu-id="59f13-147">Make sure that your email provider doesn't block emails sent from no-reply@cloudappsecurity.com.</span></span> 
  
11. <span data-ttu-id="59f13-148">Choisissez les **Actions** à entreprendre lors du déclenche d’une alerte de suspendre l’utilisateur ou de l’utilisateur doit se reconnecter pour que les applications Office 365.</span><span class="sxs-lookup"><span data-stu-id="59f13-148">Choose the **Actions** that should be taken when an alert is triggered to suspend the user or require the user to sign in again to Office 365 apps.</span></span> 
    
12. <span data-ttu-id="59f13-149">Cliquez sur **créer** pour terminer la création de votre stratégie.</span><span class="sxs-lookup"><span data-stu-id="59f13-149">Choose **Create** to finish creating your policy.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="59f13-150">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="59f13-150">Next steps</span></span>

- [<span data-ttu-id="59f13-151">Stratégies de détection des anomalies</span><span class="sxs-lookup"><span data-stu-id="59f13-151">Anomaly detection policies</span></span>](anomaly-detection-policies-in-ocas.md)
    
- [<span data-ttu-id="59f13-152">Intégrer votre serveur SIEM</span><span class="sxs-lookup"><span data-stu-id="59f13-152">Integrate your SIEM server</span></span>](integrate-your-siem-server-with-office-365-cas.md)
    
- [<span data-ttu-id="59f13-153">Passez en revue et effectuer une action sur les alertes</span><span class="sxs-lookup"><span data-stu-id="59f13-153">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="59f13-154">Vos adresses IP pour simplifier la gestion de groupe</span><span class="sxs-lookup"><span data-stu-id="59f13-154">Group your IP addresses to simplify management</span></span>](group-your-ip-addresses-in-ocas.md)
    

