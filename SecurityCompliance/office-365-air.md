---
title: Examiner et répondre automatiquement aux menaces dans Office 365
keywords: AIR, autoIR, ATP, automatisation, analyse, réponse, correction, menaces, avancé, menace, protection
ms.author: deniseb
author: denisebmsft
manager: dansimp
ms.date: 09/04/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection: M365-security-compliance
description: Prise en main des fonctionnalités d’analyse et de réponse automatisées dans Office 365 Advanced Threat Protection Plan 2.
ms.openlocfilehash: 2c64ea936170524811839db7c593d67bfe11a928
ms.sourcegitcommit: 4a2bde56178609e75c1ad7ecad2db5e049fc0c45
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/05/2019
ms.locfileid: "36762021"
---
# <a name="automatically-investigate-and-respond-to-threats-in-office-365"></a><span data-ttu-id="3ac31-104">Examiner et répondre automatiquement aux menaces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="3ac31-104">Automatically investigate and respond to threats in Office 365</span></span>

## <a name="overview"></a><span data-ttu-id="3ac31-105">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="3ac31-105">Overview</span></span>

<span data-ttu-id="3ac31-106">[Office 365 protection avancée contre les menaces](office-365-atp.md) Le plan 2 inclut des fonctionnalités d’analyse et de réponse automatisées qui permettent d’économiser le temps et les efforts de l’équipe des opérations de sécurité pour traiter les alertes et les menaces.</span><span class="sxs-lookup"><span data-stu-id="3ac31-106">[Office 365 Advanced Threat Protection](office-365-atp.md) Plan 2 includes automated investigation and response (AIR) capabilities that can save your security operations team time and effort in dealing with alerts and threats.</span></span> <span data-ttu-id="3ac31-107">Lisez cet article pour commencer à utiliser les fonctionnalités AIR dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="3ac31-107">Read this article to get started using AIR capabilities in Office 365.</span></span> <span data-ttu-id="3ac31-108">Pour en savoir plus sur le fonctionnement de l’avion, voir [Automated State and Response (air) with Office 365](automated-investigation-response-office.md).</span><span class="sxs-lookup"><span data-stu-id="3ac31-108">To learn more about how AIR works, see [Automated Investigation and Response (AIR) with Office 365](automated-investigation-response-office.md).</span></span>

<span data-ttu-id="3ac31-109">Avec AIR, lorsque certaines alertes sont déclenchées, un ou plusieurs règles de sécurité se déclenchent et une enquête automatisée commence.</span><span class="sxs-lookup"><span data-stu-id="3ac31-109">With AIR, when certain alerts are triggered, one or more security playbooks initiate, and automated investigation begins.</span></span> <span data-ttu-id="3ac31-110">Pendant et après un processus d’enquête automatisé, l’équipe des administrateurs et des opérations de sécurité peut :</span><span class="sxs-lookup"><span data-stu-id="3ac31-110">During and after an automated investigation process, your administrators and security operations team can:</span></span>

- [<span data-ttu-id="3ac31-111">Afficher les détails d’une enquête</span><span class="sxs-lookup"><span data-stu-id="3ac31-111">View the details of an investigation</span></span>](#view-details-of-an-investigation)

- [<span data-ttu-id="3ac31-112">Passer en revue et approuver les actions à la suite d’une enquête</span><span class="sxs-lookup"><span data-stu-id="3ac31-112">Review and approve actions as a result of an investigation</span></span>](#review-and-approve-actions) 

- [<span data-ttu-id="3ac31-113">Afficher les détails d’une alerte liée à une enquête</span><span class="sxs-lookup"><span data-stu-id="3ac31-113">View details about an alert related to an investigation</span></span>](#view-details-about-an-alert-related-to-an-investigation)

> [!NOTE]
> <span data-ttu-id="3ac31-114">Vous devez être un administrateur général, un administrateur de sécurité, un opérateur de sécurité ou un lecteur de sécurité pour effectuer les tâches décrites dans cet article.</span><span class="sxs-lookup"><span data-stu-id="3ac31-114">You must be a global administrator, security administrator, security operator, or security reader to perform the tasks described in this article.</span></span> <span data-ttu-id="3ac31-115">Pour plus d’informations, consultez la rubrique [Microsoft 365 Security Center : Roles and Permissions](https://docs.microsoft.com/office365/securitycompliance/microsoft-security-and-compliance#required-licenses-and-permissions).</span><span class="sxs-lookup"><span data-stu-id="3ac31-115">To learn more, see [Microsoft 365 security center: roles and permissions](https://docs.microsoft.com/office365/securitycompliance/microsoft-security-and-compliance#required-licenses-and-permissions).</span></span>

## <a name="view-details-of-an-investigation"></a><span data-ttu-id="3ac31-116">Afficher les détails d’une enquête</span><span class="sxs-lookup"><span data-stu-id="3ac31-116">View details of an investigation</span></span>

1. <span data-ttu-id="3ac31-117">En tant qu’administrateur général Office 365, administrateur de sécurité ou lecteur de sécurité, [https://protection.office.com](https://protection.office.com) accédez à et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="3ac31-117">As an Office 365 global administrator, security administrator, or security reader, go to [https://protection.office.com](https://protection.office.com) and sign in.</span></span> <span data-ttu-id="3ac31-118">Cette opération vous permet d’accéder au centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="3ac31-118">This takes you to the the Security & Compliance Center.</span></span>

2. <span data-ttu-id="3ac31-119">Effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="3ac31-119">Do one of the following:</span></span>

    - <span data-ttu-id="3ac31-120">Accédez au \*\*\*\* > **tableau de bord**gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="3ac31-120">Go to **Threat management** > **Dashboard**.</span></span> <span data-ttu-id="3ac31-121">Cela vous amène au [tableau de bord de sécurité](security-dashboard.md).</span><span class="sxs-lookup"><span data-stu-id="3ac31-121">This takes you to the [Security Dashboard](security-dashboard.md).</span></span> <span data-ttu-id="3ac31-122">Vos widgets d’AIR s’affichent dans la partie supérieure du [tableau de bord de sécurité](security-dashboard.md).</span><span class="sxs-lookup"><span data-stu-id="3ac31-122">Your AIR widgets appear across the top of the [Security Dashboard](security-dashboard.md).</span></span> <span data-ttu-id="3ac31-123">Sélectionnez un widget, par exemple, **Résumé des enquêtes**.</span><span class="sxs-lookup"><span data-stu-id="3ac31-123">Select a widget, such as **Investigations summary**.</span></span>

    - <span data-ttu-id="3ac31-124">Accédez aux \*\*\*\* > **enquêtes**de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="3ac31-124">Go to **Threat management** > **Investigations**.</span></span> 

    <span data-ttu-id="3ac31-125">L’une ou l’autre de ces méthodes vous permet d’accéder à une liste d’investigations.</span><span class="sxs-lookup"><span data-stu-id="3ac31-125">Either method takes you to a list of investigations.</span></span>

    ![Page d’enquête principale pour l’AIR](media/air-maininvestigationpage.png) 

3. <span data-ttu-id="3ac31-127">Dans la liste des enquêtes, sélectionnez un élément dans la colonne **ID** .</span><span class="sxs-lookup"><span data-stu-id="3ac31-127">In the list of investigations, select an item in the **ID** column.</span></span> <span data-ttu-id="3ac31-128">Cette action ouvre la page des détails de l’enquête, en commençant par le graphique d’enquête.</span><span class="sxs-lookup"><span data-stu-id="3ac31-128">This opens investigation details page, starting with the investigation graph.</span></span>

    ![Page graphique d’enquête sur l’AIR](media/air-investigationgraphpage.png)

4. <span data-ttu-id="3ac31-130">Utilisez les différents onglets pour en savoir plus sur l’enquête.</span><span class="sxs-lookup"><span data-stu-id="3ac31-130">Use the various tabs to learn more about the investigation.</span></span>

## <a name="review-and-approve-actions"></a><span data-ttu-id="3ac31-131">Vérifier et approuver des actions</span><span class="sxs-lookup"><span data-stu-id="3ac31-131">Review and approve actions</span></span>

<span data-ttu-id="3ac31-132">Dans Office 365, les analyses automatiques entraînent généralement une ou plusieurs actions recommandées.</span><span class="sxs-lookup"><span data-stu-id="3ac31-132">In Office 365, automated investigations typically result in one or more recommended actions.</span></span> <span data-ttu-id="3ac31-133">Toutefois, aucune action n’est effectuée tant qu’elles n’ont pas été approuvées par votre équipe des opérations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="3ac31-133">However, no actions are taken until they are approved by your security operations team.</span></span> <span data-ttu-id="3ac31-134">Utilisez la procédure suivante pour passer en revue et approuver les actions.</span><span class="sxs-lookup"><span data-stu-id="3ac31-134">Use the following procedure to review and approve actions.</span></span>

1. <span data-ttu-id="3ac31-135">En tant qu’administrateur général Office 365, administrateur de sécurité ou lecteur de sécurité, [https://protection.office.com](https://protection.office.com) accédez à et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="3ac31-135">As an Office 365 global administrator, security administrator, or security reader, go to [https://protection.office.com](https://protection.office.com) and sign in.</span></span> 

2. <span data-ttu-id="3ac31-136">Accédez aux \*\*\*\* > **enquêtes**de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="3ac31-136">Go to **Threat management** > **Investigations**.</span></span>

3. <span data-ttu-id="3ac31-137">Dans la liste des enquêtes, sélectionnez un élément dans la colonne **ID** .</span><span class="sxs-lookup"><span data-stu-id="3ac31-137">In the list of investigations, select an item in the **ID** column.</span></span> 

3. <span data-ttu-id="3ac31-138">Dans l’affichage Détails de l’enquête, sélectionnez l’onglet **actions** . Toutes les actions en attente d’approbation sont répertoriées ici.</span><span class="sxs-lookup"><span data-stu-id="3ac31-138">On the investigation details view, select the **Actions** tab. Any actions that are pending approval are listed here.</span></span>

4. <span data-ttu-id="3ac31-139">Sélectionnez un élément dans la liste.</span><span class="sxs-lookup"><span data-stu-id="3ac31-139">Select an item in the list.</span></span>

5. <span data-ttu-id="3ac31-140">Sélectionnez **approuver** pour prendre l’action recommandée (ou **rejeter** pour fermer l’enquête sans entreprendre d’action).</span><span class="sxs-lookup"><span data-stu-id="3ac31-140">Select **Approve** to take the recommended action (or **Reject** to close the investigation without taking action).</span></span>

## <a name="view-details-about-an-alert-related-to-an-investigation"></a><span data-ttu-id="3ac31-141">Afficher les détails d’une alerte liée à une enquête</span><span class="sxs-lookup"><span data-stu-id="3ac31-141">View details about an alert related to an investigation</span></span>

<span data-ttu-id="3ac31-142">Certains types d’alertes déclenchent une enquête automatisée dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="3ac31-142">Certain kinds of alerts trigger automated investigation in Office 365.</span></span> <span data-ttu-id="3ac31-143">Pour en savoir plus, consultez la rubrique [alertes](automated-investigation-response-office.md#alerts).</span><span class="sxs-lookup"><span data-stu-id="3ac31-143">To learn more, see [Alerts](automated-investigation-response-office.md#alerts).</span></span> <span data-ttu-id="3ac31-144">Utilisez la procédure suivante pour afficher les détails d’une alerte associée à une enquête automatisée.</span><span class="sxs-lookup"><span data-stu-id="3ac31-144">Use the following procedure to view details about an alert that is associated with an automated investigation.</span></span>

1. <span data-ttu-id="3ac31-145">En tant qu’administrateur général Office 365, administrateur de sécurité ou lecteur de sécurité, [https://protection.office.com](https://protection.office.com) accédez à et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="3ac31-145">As an Office 365 global administrator, security administrator, or security reader, go to [https://protection.office.com](https://protection.office.com) and sign in.</span></span> <span data-ttu-id="3ac31-146">Cette opération vous permet d’accéder au centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="3ac31-146">This takes you to the the Security & Compliance Center.</span></span>

2. <span data-ttu-id="3ac31-147">Accédez aux \*\*\*\* > **enquêtes**de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="3ac31-147">Go to **Threat management** > **Investigations**.</span></span>

3. <span data-ttu-id="3ac31-148">Dans la liste des enquêtes, sélectionnez un élément dans la colonne **ID** .</span><span class="sxs-lookup"><span data-stu-id="3ac31-148">In the list of investigations, select an item in the **ID** column.</span></span> 

4. <span data-ttu-id="3ac31-149">Les détails d’une enquête étant ouverts, sélectionnez l’onglet **alertes** . Les alertes qui ont déclenché l’enquête sont répertoriées ici.</span><span class="sxs-lookup"><span data-stu-id="3ac31-149">With details of an investigation open, select the **Alerts** tab. Any alerts that triggered the investigation are listed here.</span></span>

5. <span data-ttu-id="3ac31-150">Sélectionnez un élément dans la liste.</span><span class="sxs-lookup"><span data-stu-id="3ac31-150">Select an item in the list.</span></span> <span data-ttu-id="3ac31-151">Un menu volant s’ouvre, avec des détails sur l’alerte et des liens vers des informations et des actions supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="3ac31-151">A flyout opens, with details about the alert and links to additional information and actions.</span></span>

6. <span data-ttu-id="3ac31-152">Passez en revue les informations de la fenêtre mobile et, en fonction de l’alerte en particulier, effectuez une action, telle que **résoudre**, **supprimer**ou **avertir les utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="3ac31-152">Review the information on the flyout, and, depending on the particular alert, take an action, such as **Resolve**, **Suppress**, or **Notify users**.</span></span> 

## <a name="use-the-office-365-management-activity-api-for-custom-or-third-party-reporting-solutions"></a><span data-ttu-id="3ac31-153">Utiliser l’API activité de gestion d’Office 365 pour des solutions de création de rapports personnalisées ou tierces</span><span class="sxs-lookup"><span data-stu-id="3ac31-153">Use the Office 365 Management Activity API for custom or third-party reporting solutions</span></span>

<span data-ttu-id="3ac31-154">Si votre organisation utilise une solution de création de rapports personnalisée ou une solution de création de rapports tierce, vous pouvez afficher des informations sur les analyses automatisées dans cette solution à l’aide de l’API activité de gestion d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="3ac31-154">If your organization is using a custom reporting solution, or a third-party reporting solution, you can view information about automated investigations in that solution by using the Office 365 Management Activity API.</span></span>

<span data-ttu-id="3ac31-155">Pour ce faire, utilisez les ressources suivantes :</span><span class="sxs-lookup"><span data-stu-id="3ac31-155">Use the following resources to set this up:</span></span>

|<span data-ttu-id="3ac31-156">Ressource</span><span class="sxs-lookup"><span data-stu-id="3ac31-156">Resource</span></span>  |<span data-ttu-id="3ac31-157">Description</span><span class="sxs-lookup"><span data-stu-id="3ac31-157">Description</span></span>  |
|---------|---------|
|[<span data-ttu-id="3ac31-158">Vue d’ensemble des API de gestion d’Office 365</span><span class="sxs-lookup"><span data-stu-id="3ac31-158">Office 365 Management APIs overview</span></span>](https://docs.microsoft.com/office/office-365-management-api/office-365-management-apis-overview)     |<span data-ttu-id="3ac31-159">L’API Activité de gestion Office 365 fournit des informations sur diverses actions et événements d’utilisateur, d’administrateur, de système et de stratégie à partir des journaux d’activité Office 365 et Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3ac31-159">The Office 365 Management Activity API provides information about various user, admin, system, and policy actions and events from Office 365 and Azure Active Directory activity logs.</span></span>         |
|[<span data-ttu-id="3ac31-160">Prise en main des API de gestion d’Office 365</span><span class="sxs-lookup"><span data-stu-id="3ac31-160">Get started with Office 365 Management APIs</span></span>](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis)     |<span data-ttu-id="3ac31-161">L’API de gestion d’Office 365 utilise Azure AD pour fournir des services d’authentification à votre application pour accéder aux données d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="3ac31-161">The Office 365 Management API uses Azure AD to provide authentication services for your application to access Office 365 data.</span></span> <span data-ttu-id="3ac31-162">Suivez les étapes décrites dans cet article pour le configurer.</span><span class="sxs-lookup"><span data-stu-id="3ac31-162">Follow the steps in this article to set this up.</span></span>          |
|[<span data-ttu-id="3ac31-163">Référence de l’API Activité de gestion Office 365</span><span class="sxs-lookup"><span data-stu-id="3ac31-163">Office 365 Management Activity API reference</span></span>](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference)     |<span data-ttu-id="3ac31-164">Vous pouvez utiliser l’API activité de gestion d’Office 365 pour récupérer des informations sur les actions et événements d’utilisateur, d’administrateur, de système et de stratégie à partir des journaux d’activité Office 365 et Azure AD.</span><span class="sxs-lookup"><span data-stu-id="3ac31-164">You can use the Office 365 Management Activity API to retrieve information about user, admin, system, and policy actions and events from Office 365 and Azure AD activity logs.</span></span> <span data-ttu-id="3ac31-165">Lisez cet article pour en savoir plus sur le fonctionnement de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="3ac31-165">Read this article to learn more about how this works.</span></span>        |
|[<span data-ttu-id="3ac31-166">Schéma de l’API Activité de gestion Office 365</span><span class="sxs-lookup"><span data-stu-id="3ac31-166">Office 365 Management Activity API schema</span></span>](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema)     |<span data-ttu-id="3ac31-167">Pour en savoir plus sur des types de données spécifiques disponibles via l’API activité de gestion Office 365, consultez le schéma [commun](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#common-schema) et le schéma d’enquête et de [réponse aux menaces Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-investigation-and-response-schema) .</span><span class="sxs-lookup"><span data-stu-id="3ac31-167">Get an overview of the [Common schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#common-schema) and the [Office 365 ATP and threat investigation and response schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-investigation-and-response-schema) to learn about specific kinds of data available through the Office 365 Management Activity API.</span></span>         |

## <a name="next-steps"></a><span data-ttu-id="3ac31-168">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="3ac31-168">Next steps</span></span>

[<span data-ttu-id="3ac31-169">En savoir plus sur les alertes</span><span class="sxs-lookup"><span data-stu-id="3ac31-169">Learn more about alerts</span></span>](alert-policies.md)

[<span data-ttu-id="3ac31-170">Rechercher et identifier manuellement les messages électroniques malveillants remis dans Office 365</span><span class="sxs-lookup"><span data-stu-id="3ac31-170">Manually find and investigate malicious email that was delivered in Office 365</span></span>](investigate-malicious-email-that-was-delivered.md)

[<span data-ttu-id="3ac31-171">En savoir plus sur AIR dans Microsoft Defender ATP</span><span class="sxs-lookup"><span data-stu-id="3ac31-171">Learn about AIR in Microsoft Defender ATP</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/automated-investigations)

[<span data-ttu-id="3ac31-172">Consultez la feuille de route Microsoft 365 pour découvrir les éléments bientôt disponibles et à déployer</span><span class="sxs-lookup"><span data-stu-id="3ac31-172">Visit the Microsoft 365 Roadmap to see what's coming soon and rolling out</span></span>](https://www.microsoft.com/microsoft-365/roadmap?filters=)