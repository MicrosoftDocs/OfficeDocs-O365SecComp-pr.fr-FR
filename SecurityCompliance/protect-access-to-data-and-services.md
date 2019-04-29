---
title: Protéger l’accès aux appareils et l’accès des utilisateurs
ms.author: bcarter
author: brendacarter
manager: laurawi
ms.date: 4/17/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a6ef28a4-2447-4b43-aae2-f5af6d53c68e
description: Page d'accueil pour la protection de l'accès aux données et services O365
ms.openlocfilehash: e1b529a641d25f82521c40d0df9d091e0ebb5d90
ms.sourcegitcommit: e23b84ef4eee9cccec7205826b71ddfe9aaac2f8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33403002"
---
# <a name="protect-user-and-device-access"></a>Protéger l’accès aux appareils et l’accès des utilisateurs

La protection de l'accès à vos données et services Office 365 est cruciale pour la défense contre les attaques informatiques et la protection contre la perte de données. Les mêmes protections peuvent être appliquées à d'autres applications SaaS dans votre environnement et même aux applications locales publiées avec le proxy d'application Azure Active Directory.
  
## <a name="step-1-review-recommendations"></a>Étape 1: passer en revue les recommandations

Découvrez les fonctionnalités recommandées relatives à la protection des identités et des appareils qui accèdent à Office 365, aux autres services SaaS et applications locales publiées avec le proxy d’application Azure AD.
  
[PDF](https://go.microsoft.com/fwlink/p/?linkid=841656) | [Visio](https://go.microsoft.com/fwlink/p/?linkid=841657) | [Plus de langues](https://www.microsoft.com/download/details.aspx?id=55032)
  
## <a name="step-2-protect-administrator-accounts-and-access"></a>Étape 2: Protégez les comptes d'administrateur et l'accès
Les comptes d'administration que vous utilisez pour administrer votre environnement Office 365 incluent des privilèges élevés. Il s'agit de cibles précieuses pour les pirates et les cybercriminels. 

Commencez par utiliser les comptes d'administrateur uniquement pour l'administration. Les administrateurs doivent disposer d'un compte d'utilisateur distinct pour une utilisation normale et non administrative et n'utiliser leur compte d'administrateur que si nécessaire pour effectuer une tâche associée à leur fonction.

Protégez vos comptes d'administrateur à l'aide de l'authentification multifacteur et de l'accès conditionnel. Pour plus d'informations, consultez la rubrique [protection des comptes administrateurs](https://docs.microsoft.com/en-us/microsoft-365/enterprise/identity-access-prerequisites#protecting-administrator-accounts). 

Ensuite, configurez la gestion des accès privilégiés dans Office 365. La gestion des accès privilégiés permet le contrôle d'accès granulaire sur les tâches d'administration privilégiée dans Office 365. Elle peut aider à protéger votre organisation contre les violations susceptibles d'utiliser des comptes d'administrateur privilégié existants avec un accès permanent aux données sensibles ou un accès aux paramètres de configuration critiques.

- [Vue d'ensemble de la gestion des accès privilégiés](privileged-access-management-overview.md)
- [Configurer la gestion des accès privilégiés](privileged-access-management-configuration.md)

Il est également recommandé d'utiliser des stations de travail spécifiquement configurées pour le travail administratif. Il s'agit d'appareils dédiés qui sont utilisés uniquement pour les tâches d'administration. Consultez la rubrique Sécurisation de [l'accès privilégié](https://docs.microsoft.com/en-us/windows-server/identity/securing-privileged-access/securing-privileged-access).

Enfin, vous pouvez limiter l'impact d'un manque d'accès administratif par inadvertance en créant au moins deux comptes d'accès d'urgence dans votre client. Consultez la rubrique [Manage Emergency Access Accounts in Azure ad](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/directory-emergency-access). 

## <a name="step-3-configure-recommended-identity-and-device-access-policies"></a>Étape 3: configurer les stratégies d'identité et d'accès aux appareils recommandées
L'authentification multifacteur (MFA) et les stratégies d'accès conditionnel sont des outils puissants pour atténuer les comptes compromis et les accès non autorisés. Nous vous recommandons d'implémenter un ensemble de stratégies qui ont été testées ensemble. Pour plus d'informations, y compris sur les étapes de déploiement, voir [configurations d'identité et d'accès aux appareils](https://docs.microsoft.com/en-us/microsoft-365/enterprise/microsoft-365-policies-configurations).

 Ces stratégies implémentent les fonctionnalités suivantes:
- Authentification multifacteur
- Accès conditionnel
- Protection des applications Intune (application et protection des données pour les appareils)
- Conformité des appareils Intune
- Azure AD Identity Protection

La conformité des appareils Implemetning Intune nécessite l'enregistrement de l'appareil. La gestion des appareils vous permet de vous assurer qu'ils sont intègres et conformes avant de leur accorder l'accès à des ressources dans votre environnement. Voir [inscrire des appareils pour la gestion dans Intune](https://docs.microsoft.com/intune-classic/deploy-use/enroll-devices-in-microsoft-intune)

## <a name="step-4-configure-sharepoint-device-access-policies"></a>Étape 4: configurer les stratégies d'accès aux appareils SharePoint

Microsoft vous recommande de protéger le contenu des sites SharePoint avec du contenu sensible et hautement réglementé avec des contrôles d'accès aux appareils. Pour plus d'informations, reportez-vous à [stratégies recommandées pour la sécurisation des sites et des fichiers SharePoint](https://docs.microsoft.com/en-us/microsoft-365/enterprise/sharepoint-file-access-policies).



    

