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
# <a name="monitor-and-report-app-status-in-microsoft-365-security"></a>Surveiller et signaler l'état de l'application dans la sécurité Microsoft 365

[!include[Prerelease�information](prerelease.md)]

Ces rapports fournissent plus d'informations sur la façon dont les applications Cloud sont utilisées dans votre organisation, notamment les types d'applications, leur niveau de risque et les alertes.

## <a name="monitor-email-accounts-at-risk"></a>Surveiller les comptes de messagerie à risque

La protection de la **messagerie** affiche les comptes de messagerie à risque. Vous pouvez cliquer sur un compte pour approfondir vos recherches dans le centre de sécurité Windows Defender.

![Carte de protection de la messagerie](./media/security-docs/email-protection.png)

## <a name="monitor-app-permissions-granted-by-users"></a>Surveiller les autorisations d'application accordées par les utilisateurs

**Sécurité des applications Cloud: applications OAuth** répertorie les applications découvertes par la sécurité des applications Cloud auxquelles des autorisations ont été accordées par les utilisateurs. Le catalogue des risques de la sécurité des applications Cloud inclut plus de 16 000 applications évaluées à l'aide de plus de 70 facteurs de risque.

Les facteurs de risque commencent à partir d'informations générales, telles que l'éditeur de l'application, vers des mesures et des contrôles de sécurité, par exemple si l'application prend en charge le chiffrement au repos ou fournit un journal d'audit de l'activité de l'utilisateur.

![Carte d'applications OAuth de sécurité d'application Cloud](./media/security-docs/cloud-app-security-oauth-apps.png)

## <a name="monitor-cloud-app-user-accounts"></a>Surveiller les comptes d'utilisateur d'application Cloud

**Comptes d'application Cloud pour vérifier les** comptes qui peuvent nécessiter votre attention.

![Carte de révision des comptes d'application Cloud](./media/security-docs/cloud-app-accounts-for-review.png)

## <a name="understand-which-cloud-apps-are-used"></a>Comprendre les applications Cloud utilisées

**Applications Cloud découvertes (catégories)** Affichez les types d'applications qui sont utilisées dans votre organisation et les liens vers le tableau de bord de découverte dans le Cloud dans la sécurité des applications Cloud. Pour plus d'informations, consultez la rubrique [QuickStart: utiliser des applications découvertes](https://docs.microsoft.com/cloud-app-security/discovered-apps).  

![Carte des catégories d'applications Cloud découvertes](./media/security-docs/discovered-cloud-apps-categories.png)

## <a name="monitor-where-users-access-cloud-apps"></a>Surveiller l'emplacement où les utilisateurs accèdent aux applications Cloud

Les emplacements des activités de l' **application Cloud** indiquent où les utilisateurs accèdent aux applications Cloud.

![Fiche des emplacements des activités de l'application Cloud](./media/security-docs/cloud-app-activity-locations.png)

## <a name="monitor-health-for-infrastructure-workloads"></a>Surveiller l'intégrité des charges de travail d'infrastructure

L'intégrité de l' **infrastructure** indique des alertes d'état d'intégrité pour les charges de travail d'infrastructure dans Azure Security Center.

Azure Security Center offre une gestion de sécurité unifiée et une protection avancée contre les menaces entre les charges de travail locales et de Cloud. Vous pouvez collecter, Rechercher et analyser des données de sécurité à partir d'une variété de sources, notamment des pare-feu et d'autres solutions partenaires.

Pour plus d'informations, reportez-vous à [Azure Security Center documentation](https://docs.microsoft.com/azure/security-center/).

![Carte d'intégrité de l'infrastructure](./media/security-docs/infrastructure-health.png)
