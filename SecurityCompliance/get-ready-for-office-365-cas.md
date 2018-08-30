---
title: Préparez-vous pour la sécurité d’application Office 365 dans le nuage
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: d9ee4d67-f2b3-42b4-9c9e-c4529904990a
description: Mise en route à l’aide de la sécurité d’application Office 365 dans le nuage
ms.openlocfilehash: 906570c6607c70b63fa9d2059d56b50f7807124a
ms.sourcegitcommit: edf5db9357c0d34573f8cc406314525ef10d1eb9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/28/2018
ms.locfileid: "23229986"
---
# <a name="get-ready-for-office-365-cloud-app-security"></a><span data-ttu-id="65b79-103">Préparez-vous pour la sécurité d’application Office 365 dans le nuage</span><span class="sxs-lookup"><span data-stu-id="65b79-103">Get ready for Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="65b79-104">Évaluation **\>**</span><span class="sxs-lookup"><span data-stu-id="65b79-104">****Evaluation** \>**</span></span>|<span data-ttu-id="65b79-105">Planification **\>**</span><span class="sxs-lookup"><span data-stu-id="65b79-105">****Planning** \>**</span></span>|<span data-ttu-id="65b79-106">Déploiement **\>**</span><span class="sxs-lookup"><span data-stu-id="65b79-106">****Deployment** \>**</span></span>|<span data-ttu-id="65b79-107">Utilisation du \*\*\*</span><span class="sxs-lookup"><span data-stu-id="65b79-107">****Utilization****</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="65b79-108">Commencer à évaluer</span><span class="sxs-lookup"><span data-stu-id="65b79-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |<span data-ttu-id="65b79-109">Vous êtes ici !</span><span class="sxs-lookup"><span data-stu-id="65b79-109">You are here!</span></span>  <br/> [<span data-ttu-id="65b79-110">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="65b79-110">Next step</span></span>](turn-on-office-365-cas.md) <br/> |[<span data-ttu-id="65b79-111">Commencer à déployer</span><span class="sxs-lookup"><span data-stu-id="65b79-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |[<span data-ttu-id="65b79-112">Commencer à utiliser</span><span class="sxs-lookup"><span data-stu-id="65b79-112">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |
   
<span data-ttu-id="65b79-p101">Lorsque vous préparez à activer et à implémenter la sécurité d’application Office 365 dans le nuage (anciennement appelé gestion de la sécurité avancée) pour votre organisation, il existe quelques éléments à prendre en compte. Utilisez cet article comme un guide pour planifier la sécurité d’application Office 365 dans le nuage.</span><span class="sxs-lookup"><span data-stu-id="65b79-p101">As you prepare to turn on and implement Office 365 Cloud App Security (formerly known as Advanced Security Management) for your organization, there are a few things to take into account. Use this article as a guide to plan for Office 365 Cloud App Security.</span></span>
    
## <a name="step-1-identify-and-protect-your-global-and-security-administrator-accounts"></a><span data-ttu-id="65b79-115">Étape 1 : Identifier et protéger vos comptes d’administrateur globales et sécurité</span><span class="sxs-lookup"><span data-stu-id="65b79-115">Step 1: Identify and protect your global and security administrator accounts</span></span>

<span data-ttu-id="65b79-p102">Les administrateurs globaux, les administrateurs de sécurité et les lecteurs de sécurité peuvent accéder au portail de sécurité d’application Office 365 dans le nuage pour afficher les stratégies, passez en revue les alertes et utiliser les rapports. Les administrateurs globaux et les administrateurs de sécurité peuvent définir des stratégies et exécuter d’autres actions pour protéger votre organisation. (Pour plus d’informations, voir [des autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md).) Passez en revue les comptes d’utilisateurs de votre organisation qui ont des autorisations élevées par mesure de précaution.</span><span class="sxs-lookup"><span data-stu-id="65b79-p102">Global administrators, security administrators, and security readers can access the Office 365 Cloud App Security portal to view policies, review alerts, and use reports. Global administrators and security administrators can define policies and take other actions to protect your organization. (For more information, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).) Review your organization's user accounts that have elevated permissions as a precaution.</span></span> 
  
 <span data-ttu-id="65b79-119">**[Comptes d’administrateur global Protect Office 365](https://docs.microsoft.com/office365/enterprise/protect-your-global-administrator-accounts)**.</span><span class="sxs-lookup"><span data-stu-id="65b79-119">**[Protect your Office 365 global administrator accounts](https://docs.microsoft.com/office365/enterprise/protect-your-global-administrator-accounts)**.</span></span> 
  
## <a name="step-2-turn-on-audit-logging-for-your-organization"></a><span data-ttu-id="65b79-120">Étape 2 : Activer l’enregistrement d’audit pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="65b79-120">Step 2: Turn on audit logging for your organization</span></span>

<span data-ttu-id="65b79-p103">Dans l’ordre Office 365 nuage sécurité des applications fonctionnent correcte, l’enregistrement d’audit doit être activée. Cela est généralement effectuée par un administrateur Exchange Online ou un administrateur global.</span><span class="sxs-lookup"><span data-stu-id="65b79-p103">In order for Office 365 Cloud App Security to work correct, audit logging must be turned on. This is typically done by an Exchange Online administrator or a global administrator.</span></span>
  
 <span data-ttu-id="65b79-123">**[Recherche des journaux d’audit d’activer Office 365 activé ou désactivé](turn-audit-log-search-on-or-off.md)**.</span><span class="sxs-lookup"><span data-stu-id="65b79-123">**[Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md)**.</span></span> 
  
## <a name="step-3-go-to-the-office-365-cloud-app-security-portal"></a><span data-ttu-id="65b79-124">Étape 3 : Accéder au portail Office 365 Cloud Application Security</span><span class="sxs-lookup"><span data-stu-id="65b79-124">Step 3: Go to the Office 365 Cloud App Security portal</span></span>

1. <span data-ttu-id="65b79-p104">Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous à l’aide de votre compte professionnel ou de l’école pour Office 365. (Cela vous amène à la sécurité &amp; centre de conformité.)</span><span class="sxs-lookup"><span data-stu-id="65b79-p104">Go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account for Office 365. (This takes you to the Security &amp; Compliance Center.)</span></span> 
    
2. <span data-ttu-id="65b79-127">Accédez à des **alertes** \> **Gestion avancée des alertes**.</span><span class="sxs-lookup"><span data-stu-id="65b79-127">Go to **Alerts** \> **Manage advanced alerts**.</span></span>
    
3. <span data-ttu-id="65b79-128">Cliquez sur **Aller à la sécurité d’application Office 365 dans le nuage** pour accéder au portail Office 365 Cloud Application Security.</span><span class="sxs-lookup"><span data-stu-id="65b79-128">Choose **Go to Office 365 Cloud App Security** to go to the Office 365 Cloud App Security portal.</span></span> 
    
    ![Dans la sécurité &amp; centre de conformité, cliquez sur Gérer les alertes avancées pour accéder à la sécurité d’application dans le nuage Office 365](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)
  
    <span data-ttu-id="65b79-130">Lorsque vous accédez au portail Office 365 Cloud Application Security, la première page que vous voyez est la page de stratégies, qui ressemble à l’image suivante :</span><span class="sxs-lookup"><span data-stu-id="65b79-130">When you go to the Office 365 Cloud App Security portal, the first page you see is the Policies page, which resembles the following image:</span></span>
    
    ![Lorsque vous accédez au portail Office 365 Cloud Application Security, vous démarrez avec la page de stratégies](media/5cb8833c-4e08-438c-bab3-91b5106f6f3f.png)
  
## <a name="step-4-define-policies-and-set-up-alerts-amp-actions"></a><span data-ttu-id="65b79-132">Étape 4 : Définir des stratégies et définir des alertes &amp; actions</span><span class="sxs-lookup"><span data-stu-id="65b79-132">Step 4: Define policies and set up alerts &amp; actions</span></span>

<span data-ttu-id="65b79-p105">Les administrateurs globaux et les administrateurs de sécurité définissent des stratégies de sécurité d’application Office 365 dans le nuage. Au cours du processus de définition de stratégies, alertes et des actions sont également définies. Une alerte est une notification basée sur les critères qui s’affiche dans une vue ou est envoyée par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="65b79-p105">Global administrators and security administrators define policies in Office 365 Cloud App Security. During the process of defining policies, alerts and actions are also set. An alert is a criteria-based notification that appears in a view or is sent via email.</span></span> 
  
<span data-ttu-id="65b79-p106">Il existe deux types d’alertes de sécurité d’application Office 365 dans le nuage : les alertes de détection des anomalies que détectent les activités suspectes et alertes d’activité, qui sont définies pour les activités qui peuvent être atypiques pour votre organisation. Les alertes avertissent les administrateurs globaux et les administrateurs de sécurité lorsqu’il existe une activité dans votre environnement Office 365 est inhabituelle pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="65b79-p106">There are two types of alerts in Office 365 Cloud App Security: anomaly detection alerts that detect suspicious activity, and activity alerts, which are defined for activities that might be atypical for your organization. Alerts notify global administrators and security administrators when there's an activity in your Office 365 environment that's unusual for your organization.</span></span>
  
<span data-ttu-id="65b79-138">Voir les ressources suivantes pour en savoir plus :</span><span class="sxs-lookup"><span data-stu-id="65b79-138">See the following resources to learn more:</span></span>
  
- [<span data-ttu-id="65b79-139">Stratégies d’activité et les alertes de sécurité pour application Cloud Microsoft Office 365</span><span class="sxs-lookup"><span data-stu-id="65b79-139">Activity policies and alerts in Office 365 Cloud App Security</span></span>](activity-policies-and-alerts.md)
    
- [<span data-ttu-id="65b79-140">Stratégies de détection des anomalies dans Office 365 Cloud Application Security</span><span class="sxs-lookup"><span data-stu-id="65b79-140">Anomaly detection policies in Office 365 Cloud App Security</span></span>](anomaly-detection-policies-in-ocas.md)
    
- [<span data-ttu-id="65b79-141">Passez en revue et effectuer une action sur les alertes de sécurité pour application Cloud Microsoft Office 365</span><span class="sxs-lookup"><span data-stu-id="65b79-141">Review and take action on Office 365 Cloud App Security alerts</span></span>](review-office-365-cas-alerts.md)
    
## <a name="step-5-learn-about-your-organizations-cloud-usage"></a><span data-ttu-id="65b79-142">Étape 5 : En savoir plus sur l’utilisation du cloud de votre organisation</span><span class="sxs-lookup"><span data-stu-id="65b79-142">Step 5: Learn about your organization's cloud usage</span></span>

<span data-ttu-id="65b79-p107">En tant qu’un administrateur global, un administrateur de sécurité ou un lecteur de sécurité, vous pouvez découvrir l’utilisation du cloud de votre organisation par le biais de rapports et un tableau de bord de découverte dans le nuage (également appelée détection d’application de la productivité). Ce tableau de bord présente des informations sur les utilisateurs, les applications, le trafic web et des niveaux de risques.</span><span class="sxs-lookup"><span data-stu-id="65b79-p107">As a global administrator, security administrator, or security reader, you can learn about your organization's cloud usage through reports and a Cloud Discovery dashboard (also called Productivity App Discovery). This dashboard shows information about users, apps, web traffic, and risk levels.</span></span>
  
![Dans le portail Office 365 autorités de certification, cliquez sur découvrir \> tableau de bord de découverte dans le nuage](media/61269290-fd82-4d4b-8045-aea1ebc82287.png)
  
<span data-ttu-id="65b79-146">Pour accéder au tableau de bord de détection d’application de la productivité, dans le portail Office 365 Cloud application sécurité, choisissez **découvrir** \> **tableau de bord de découverte dans le nuage**.</span><span class="sxs-lookup"><span data-stu-id="65b79-146">To go to the Productivity App Discovery dashboard, in the Office 365 Cloud App Security portal, choose **Discover** \> **Cloud Discovery dashboard**.</span></span>
  
![Dans le portail Office 365 autorités de certification, cliquez sur découvrir](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)
  
<span data-ttu-id="65b79-p108">Pour remplir des rapports avec les informations que nécessaires, télécharger vos fichiers journaux de pare-feu et des proxys de votre organisation. Pour plus d’informations, voir les ressources suivantes :</span><span class="sxs-lookup"><span data-stu-id="65b79-p108">To populate reports with the information you need, upload your log files from your organization's firewalls and proxies. To learn more, see the following resources:</span></span>
  
- [<span data-ttu-id="65b79-150">Créer des rapports de détection d’application dans Office 365 Cloud Application Security</span><span class="sxs-lookup"><span data-stu-id="65b79-150">Create app discovery reports in Office 365 Cloud App Security</span></span>](create-app-discovery-reports-in-ocas.md)
    
- [<span data-ttu-id="65b79-151">Passez en revue les conclusions de découverte d’application dans Office 365 Cloud application sécurité</span><span class="sxs-lookup"><span data-stu-id="65b79-151">Review app discovery findings in Office 365 Cloud App Security</span></span>](review-app-discovery-findings-in-ocas.md)
    
## <a name="step-6-manage-apps-that-your-organization-is-using-to-access-office-365"></a><span data-ttu-id="65b79-152">Étape 6 : Gérer les applications à l’aide de votre organisation à access Office 365</span><span class="sxs-lookup"><span data-stu-id="65b79-152">Step 6: Manage apps that your organization is using to access Office 365</span></span>

<span data-ttu-id="65b79-p109">En tant qu’un administrateur global ou administrateur de sécurité, vous pouvez gérer les applications, telles que les applications personnalisées ou les applications de tiers, utilisant des personnes dans votre organisation sur leurs appareils avec Office 365. Par exemple, supposons que quelqu'un a téléchargé une application personnalisée à utiliser avec Office 365. Vous pouvez consulter les applications à l’aide de personnes, interdire les applications non fiables ou marquer les applications approuvées à vos besoins de suivi. [Gérer les autorisations d’application à l’aide de la sécurité d’application Office 365 dans le nuage](manage-app-permissions-in-ocas.md).</span><span class="sxs-lookup"><span data-stu-id="65b79-p109">As a global administrator or security administrator, you can manage apps, such as custom apps or third-party apps, that people in your organization are using on their devices with Office 365. For example, suppose that someone has downloaded a custom app they want to use with Office 365. You can review the apps people are using, ban untrusted apps, or mark apps as approved for your tracking purposes. [Manage app permissions using Office 365 Cloud App Security](manage-app-permissions-in-ocas.md).</span></span>
  
## <a name="step-7-use-your-siem-server-with-office-365-cloud-app-security"></a><span data-ttu-id="65b79-157">Étape 7 : Utiliser votre serveur SIEM avec Office 365 Cloud application sécurité</span><span class="sxs-lookup"><span data-stu-id="65b79-157">Step 7: Use your SIEM server with Office 365 Cloud App Security</span></span>

<span data-ttu-id="65b79-p110">Votre organisation utilise un serveur de gestion (SIEM) des informations et des événements de sécurité ? Office 365 Cloud application sécurité peut maintenant intégrer à votre serveur SIEM pour activer la surveillance centralisée des alertes. Intégration avec un service SIEM vous permet de mieux protéger vos applications en nuage lors de la maintenance de votre flux de travail habituelles de sécurité, l’automatisation des procédures de sécurité et corrélation entre en nuage et événements locale. L’agent SIEM s’exécute sur votre serveur extrait les alertes de sécurité d’application Office 365 dans le nuage et transmet les alertes dans votre serveur SIEM. Consultez [l’intégration avec Office 365 Cloud application sécurité SIEM](integrate-your-siem-server-with-office-365-cas.md).</span><span class="sxs-lookup"><span data-stu-id="65b79-p110">Is your organization using a security information and event management (SIEM) server? Office 365 Cloud App Security can now integrate with your SIEM server to enable centralized monitoring of alerts. Integrating with a SIEM service allows you to better protect your cloud applications while maintaining your usual security workflow, automating security procedures and correlating between cloud-based and on-premises events. The SIEM agent runs on your server, pulls alerts from Office 365 Cloud App Security, and streams those alerts into your SIEM server. See [SIEM integration with Office 365 Cloud App Security](integrate-your-siem-server-with-office-365-cas.md).</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="65b79-163">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="65b79-163">Next steps</span></span>

- [<span data-ttu-id="65b79-164">Activer la sécurité d’application Office 365 dans le nuage</span><span class="sxs-lookup"><span data-stu-id="65b79-164">Turn on Office 365 Cloud App Security</span></span>](turn-on-office-365-cas.md)
    
- <span data-ttu-id="65b79-165">Essayez notre [Guide de laboratoire de Test](https://docs.microsoft.com/office365/enterprise/cloud-app-security-for-your-office-365-dev-test-environment) pour une expérience pratique qui illustrent les puissantes fonctionnalités de sécurité d’application Office 365 dans le nuage et créer une preuve de concept.</span><span class="sxs-lookup"><span data-stu-id="65b79-165">Try our [Test Lab Guide](https://docs.microsoft.com/office365/enterprise/cloud-app-security-for-your-office-365-dev-test-environment) for a hands-on experience where you can demonstrate the powerful features of Office 365 Cloud App Security and create a proof of concept.</span></span> 
    

