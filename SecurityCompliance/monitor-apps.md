---
title: Surveiller et signaler l'état de l'application dans la sécurité Microsoft 365
description: Décrit comment obtenir plus d'informations sur l'utilisation des applications Cloud dans votre organisation
keywords: sécurité, programmes malveillants, Microsoft 365, M365, centre de sécurité, moniteur, rapport, applications
ms.prod: w10
ms.mktglfcycl: deploy
ms.localizationpriority: medium
ms.author: ellevin
author: levinec
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.openlocfilehash: 02cc511532f65172aba2c0f98cdf594776f586a5
ms.sourcegitcommit: ef27da3ea5340d6e7a2eaa1288e2e005ef8e4788
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2019
ms.locfileid: "30791664"
---
# <a name="monitor-and-report-app-status-in-microsoft-365-security"></a><span data-ttu-id="44a5f-104">Surveiller et signaler l'état de l'application dans la sécurité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="44a5f-104">Monitor and report app status in Microsoft 365 security</span></span>

[!include[Prerelease�information](prerelease.md)]

<span data-ttu-id="44a5f-105">Ces rapports fournissent plus d'informations sur la façon dont les applications Cloud sont utilisées dans votre organisation, notamment les types d'applications, leur niveau de risque et les alertes.</span><span class="sxs-lookup"><span data-stu-id="44a5f-105">These reports provide more insight into how cloud apps are being used in your organization, including what kinds of apps, their level of risk, and alerts.</span></span>

## <a name="monitor-email-accounts-at-risk"></a><span data-ttu-id="44a5f-106">Surveiller les comptes de messagerie à risque</span><span class="sxs-lookup"><span data-stu-id="44a5f-106">Monitor email accounts at risk</span></span>

<span data-ttu-id="44a5f-107">La protection de la **messagerie** affiche les comptes de messagerie à risque.</span><span class="sxs-lookup"><span data-stu-id="44a5f-107">**Email protection** shows email accounts at risk.</span></span> <span data-ttu-id="44a5f-108">Vous pouvez cliquer sur un compte pour approfondir vos recherches dans le centre de sécurité Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="44a5f-108">You can click an account to investigate further in Windows Defender Security Center.</span></span>

![Carte de protection de la messagerie](./media/security-docs/email-protection.png)

## <a name="monitor-app-permissions-granted-by-users"></a><span data-ttu-id="44a5f-110">Surveiller les autorisations d'application accordées par les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="44a5f-110">Monitor app permissions granted by users</span></span>

<span data-ttu-id="44a5f-111">**Sécurité des applications Cloud: applications OAuth** répertorie les applications découvertes par la sécurité des applications Cloud auxquelles des autorisations ont été accordées par les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="44a5f-111">**Cloud App Security - OAuth apps** lists apps discovered by Cloud App Security that have been granted permissions by users.</span></span> <span data-ttu-id="44a5f-112">Le catalogue des risques de la sécurité des applications Cloud inclut plus de 16 000 applications évaluées à l'aide de plus de 70 facteurs de risque.</span><span class="sxs-lookup"><span data-stu-id="44a5f-112">Cloud App Security's risk catalog includes over 16,000 apps that are assessed using over 70 risk factors.</span></span>

<span data-ttu-id="44a5f-113">Les facteurs de risque commencent à partir d'informations générales, telles que l'éditeur de l'application, vers des mesures et des contrôles de sécurité, par exemple si l'application prend en charge le chiffrement au repos ou fournit un journal d'audit de l'activité de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="44a5f-113">The risk factors start from general information, such as the app publisher, to security measures and controls, such as whether the app supports for encryption at rest or provides an audit log of user activity.</span></span>

![Carte d'applications OAuth de sécurité d'application Cloud](./media/security-docs/cloud-app-security-oauth-apps.png)

## <a name="monitor-cloud-app-user-accounts"></a><span data-ttu-id="44a5f-115">Surveiller les comptes d'utilisateur d'application Cloud</span><span class="sxs-lookup"><span data-stu-id="44a5f-115">Monitor cloud app user accounts</span></span>

<span data-ttu-id="44a5f-116">**Comptes d'application Cloud pour vérifier les** comptes qui peuvent nécessiter votre attention.</span><span class="sxs-lookup"><span data-stu-id="44a5f-116">**Cloud app accounts for review** lists accounts that may require attention.</span></span>

![Carte de révision des comptes d'application Cloud](./media/security-docs/cloud-app-accounts-for-review.png)

## <a name="understand-which-cloud-apps-are-used"></a><span data-ttu-id="44a5f-118">Comprendre les applications Cloud utilisées</span><span class="sxs-lookup"><span data-stu-id="44a5f-118">Understand which cloud apps are used</span></span>

<span data-ttu-id="44a5f-119">**Applications Cloud découvertes (catégories)** Affichez les types d'applications qui sont utilisées dans votre organisation et les liens vers le tableau de bord de découverte dans le Cloud dans la sécurité des applications Cloud.</span><span class="sxs-lookup"><span data-stu-id="44a5f-119">**Discovered cloud apps (categories)** show what kinds of apps are being used in your organization and links to the Cloud Discovery dashboard in Cloud App Security.</span></span> <span data-ttu-id="44a5f-120">Pour plus d'informations, consultez la rubrique [QuickStart: utiliser des applications découvertes](https://docs.microsoft.com/cloud-app-security/discovered-apps).</span><span class="sxs-lookup"><span data-stu-id="44a5f-120">For more information, see [Quickstart: Work with discovered apps](https://docs.microsoft.com/cloud-app-security/discovered-apps).</span></span>  

![Carte des catégories d'applications Cloud découvertes](./media/security-docs/discovered-cloud-apps-categories.png)

## <a name="monitor-where-users-access-cloud-apps"></a><span data-ttu-id="44a5f-122">Surveiller l'emplacement où les utilisateurs accèdent aux applications Cloud</span><span class="sxs-lookup"><span data-stu-id="44a5f-122">Monitor where users access cloud apps</span></span>

<span data-ttu-id="44a5f-123">Les emplacements des activités de l' **application Cloud** indiquent où les utilisateurs accèdent aux applications Cloud.</span><span class="sxs-lookup"><span data-stu-id="44a5f-123">**Cloud app activity locations** show where users are accessing cloud apps.</span></span>

![Fiche des emplacements des activités de l'application Cloud](./media/security-docs/cloud-app-activity-locations.png)

## <a name="monitor-health-for-infrastructure-workloads"></a><span data-ttu-id="44a5f-125">Surveiller l'intégrité des charges de travail d'infrastructure</span><span class="sxs-lookup"><span data-stu-id="44a5f-125">Monitor health for infrastructure workloads</span></span>

<span data-ttu-id="44a5f-126">L'intégrité de l' **infrastructure** indique des alertes d'état d'intégrité pour les charges de travail d'infrastructure dans Azure Security Center.</span><span class="sxs-lookup"><span data-stu-id="44a5f-126">**Infrastructure health** shows health status alerts for infrastructure workloads in Azure Security Center.</span></span>

<span data-ttu-id="44a5f-127">Azure Security Center offre une gestion de sécurité unifiée et une protection avancée contre les menaces entre les charges de travail locales et de Cloud.</span><span class="sxs-lookup"><span data-stu-id="44a5f-127">Azure Security Center provides unified security management and advanced threat protection across on-premises and cloud workloads.</span></span> <span data-ttu-id="44a5f-128">Vous pouvez collecter, Rechercher et analyser des données de sécurité à partir d'une variété de sources, notamment des pare-feu et d'autres solutions partenaires.</span><span class="sxs-lookup"><span data-stu-id="44a5f-128">You can collect, search, and analyze security data from a variety of sources, including firewalls and other partner solutions.</span></span>

<span data-ttu-id="44a5f-129">Pour plus d'informations, reportez-vous à [Azure Security Center documentation](https://docs.microsoft.com/azure/security-center/).</span><span class="sxs-lookup"><span data-stu-id="44a5f-129">For more information, see [Azure Security Center Documentation](https://docs.microsoft.com/azure/security-center/).</span></span>

![Carte d'intégrité de l'infrastructure](./media/security-docs/infrastructure-health.png)
