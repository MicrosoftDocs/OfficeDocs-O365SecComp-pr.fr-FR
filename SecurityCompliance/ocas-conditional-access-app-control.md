---
title: Protéger les applications avec Office 365 Cloud App Security App contrôle d'application d'accès conditionnel
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.reviewer: alesibov
ms.audience: Admin
ms.topic: reference
ms.date: 02/14/2019
ms.service: o365-administration
localization_priority: Normal
description: Arrêter les violations et les fuites en temps réel avec le contrôle d'application d'accès conditionnel à Office 365 Cloud App Security.
ms.openlocfilehash: 8656bf9d3e028bf6b44731c397b74d9c883db707
ms.sourcegitcommit: 8679937354c1d8870ecd41519a59d2d7468c23c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2019
ms.locfileid: "30103359"
---
# <a name="protect-apps-with-office-365-cloud-app-security-conditional-access-app-control"></a>Protéger les applications avec Office 365 Cloud App Security App contrôle d'application d'accès conditionnel

|Évaluation * *\>**|Planification * *\>**|Déploiement * *\>**|Utilisation * * * *|
|:-----|:-----|:-----|:-----|
|[Commencer l'évaluation](office-365-cas-overview.md) <br/> |[Commencer la planification](get-ready-for-office-365-cas.md) <br/> |Vous êtes là!  <br/> [Étape suivante](ocas-deploy-conditional-access-app-control.md) <br/> |[Commencer à utiliser](utilization-activities-for-ocas.md) <br/> |

Dans l'espace de travail d'aujourd'hui, il est souvent insuffisant de savoir ce qui se passe dans votre environnement Cloud après le fait. Vous souhaitez arrêter les violations et les fuites en temps réel, avant que les employés déposent intentionnellement ou involontairement vos données et votre organisation en péril. Il est important de permettre aux utilisateurs de votre organisation de tirer le meilleur parti des services et outils disponibles dans les applications Cloud, et de leur permettre de faire fonctionner leurs propres appareils. En même temps, vous avez besoin d'outils pour vous aider à protéger votre organisation contre les fuites de données et le vol de données en temps réel. Avec Azure Active Directory, la sécurité des applications Cloud Office 365 offre ces fonctionnalités dans une expérience holistique et intégrée avec un contrôle d'application d'accès conditionnel.

> [!IMPORTANT]
> pour utiliser le contrôle d'application d'accès conditionnel sécurité des applications cloud, vous avez besoin d'une  [licence Azure active Directory P1](https://azure.microsoft.com/pricing/details/active-directory/)et d'un abonnement [Office 365 Cloud app security](office-365-cas-overview.md) .

## <a name="how-it-works"></a>Fonctionnement

Le contrôle d'application d'accès conditionnel utilise une architecture de proxy inverse et est intégré de manière unique à l'accès conditionnel Azure AD. L'accès conditionnel Azure AD vous permet d'appliquer des contrôles d'accès aux applications de votre organisation en fonction de certaines conditions. Les conditions définissent l' *identité* de l'utilisateur ou du groupe d'utilisateurs, ainsi *que* les ** applications Cloud auxquelles une stratégie d'accès conditionnel est appliquée. Une fois que vous avez déterminé les conditions, vous pouvez acheminer les utilisateurs vers la sécurité des applications Cloud Office 365 où vous pouvez protéger les données avec le contrôle d'application d'accès conditionnel en appliquant les contrôles d'accès et de session.

Le contrôle d'application d'accès conditionnel permet de surveiller et de contrôler en temps réel les sessions et l'accès aux applications utilisateur en fonction des stratégies d'accès et de session. Les stratégies d'accès et de session sont utilisées dans le portail de sécurité des applications Cloud pour affiner les filtres et définir les actions à effectuer sur un utilisateur. Avec les stratégies d'accès et de session, vous pouvez:

- **Bloquer au téléchargement**: vous pouvez bloquer le téléchargement de documents sensibles. Par exemple, sur des appareils non gérés.

- **Protéger au téléchargement**: au lieu de bloquer le téléchargement de documents sensibles, vous pouvez exiger la protection des documents via le chiffrement au téléchargement. Ce chiffrement permet de s'assurer que le document est protégé et que l'accès des utilisateurs est authentifié si les données sont téléchargées sur un appareil non approuvé.

- **Surveiller les sessions utilisateur à faible niveau de fiabilité**: les utilisateurs à risque sont surveillés lorsqu'ils se connectent à des applications et que leurs actions sont consignées dans la session. Vous pouvez examiner et analyser le comportement de l'utilisateur pour comprendre où et dans quelles conditions les stratégies de session doivent être appliquées à l'avenir.

- **Bloquer l'accès**: vous pouvez bloquer totalement l'accès à des applications spécifiques pour les utilisateurs provenant d'appareils non gérés ou de réseaux non d'entreprise.

- **Créer un mode lecture seule**: en surveillant et en bloquant les activités personnalisées dans l'application, vous pouvez créer un mode en lecture seule pour des applications spécifiques pour des utilisateurs spécifiques.

- **Limiter les sessions utilisateur de réseaux non d'entreprise**: les utilisateurs qui accèdent à une application protégée à partir d'un emplacement qui ne fait pas partie de votre réseau d'entreprise bénéficient d'un accès restreint. Le téléchargement de documents sensibles est bloqué ou protégé.

### <a name="how-session-control-works"></a>Fonctionnement du contrôle de session

La création d'une stratégie de session avec un contrôle d'application d'accès conditionnel vous permet de contrôler les sessions utilisateur en redirigeant l'utilisateur par le biais d'un proxy inverse au lieu de l'application directement. À partir de là, les demandes et les réponses des utilisateurs passent par la sécurité des applications Cloud d'Office 365 plutôt que directement par l'application.

Pour conserver l'utilisateur au sein de la session, toutes les URL appropriées, tous les scripts Java et tous les cookies de la session de l'application sont remplacés par les URL de sécurité de l'application Cloud d'Office 365. Par exemple, si l'application renvoie une page avec des liens dont les domaines se terminent par myapp.com, le lien est remplacé par des domaines se terminant par une valeur semblable à la suivante: myapp.com.us.cas.ms

Cette méthode ne nécessite aucune installation sur l'appareil. Cette méthode est idéale lors de la surveillance de sessions à partir d'appareils non gérés.

Une fois qu'une session est dirigée par le biais de la sécurité des applications Cloud d'Office 365, les actions suivantes peuvent être effectuées:

1. Inspecter le trafic pour les activités de l'utilisateur

2. Afficher les activités identifiées dans le journal d'activité de sécurité des applications Cloud Office 365

3. Enregistrer les journaux de trafic et les analyser

4. Autoriser l'administrateur à exporter les journaux de trafic

5. Appliquer des stratégies sur la session

## <a name="managed-device-identification"></a>Identification des appareils gérés

Le contrôle d'application d'accès conditionnel vous permet de créer des stratégies qui prennent en compte si un appareil est géré ou non. Pour déterminer si un périphérique est géré ou non, la fonctionnalité utilise les éléments suivants:

- Appareils conformes

- Appareils joints à un domaine

- Déploiement de certificats clients

### <a name="compliant-and-domain-joined-devices"></a>Appareils conformes et joints à un domaine

L'accès conditionnel Azure AD permet de transmettre directement des informations de périphériques conformes et joints à un domaine à la sécurité des applications Cloud Office 365. À partir de là, il est possible de développer une stratégie d'accès ou une stratégie de session qui utilise l'état de l'appareil en tant que filtre. Pour plus d'informations, consultez la rubrique [Présentation de la gestion des appareils dans Azure Active Directory](https://docs.microsoft.com/azure/active-directory/device-management-introduction).

### <a name="client-certificate-authenticated-devices"></a>Appareils authentifiés par le certificat client

Le mécanisme d'identification des périphériques peut demander l'authentification à partir d'appareils appropriés à l'aide de certificats clients. Vous pouvez utiliser des certificats clients existants déjà déployés dans votre organisation ou déployer de nouveaux certificats clients sur des appareils gérés. Vous utilisez ensuite la présence de ces certificats pour définir les stratégies d'accès et de session. Pour plus d'informations sur le déploiement des certificats clients, voir [Deploy ConditionalAttribute Access App Control for Office 365 Apps](ocas-deploy-conditional-access-app-control.md).

## <a name="supported-apps-and-clients"></a>Applications et clients pris en charge

Le contrôle d'application d'accès conditionnel pour Office 365 prend en charge les applications proposées suivantes:

- Exchange Online (aperçu)

- OneDrive entreprise (aperçu)

- Power BI (aperçu)

- SharePoint Online (aperçu)

- Microsoft Teams (aperçu)

- Yammer (aperçu)

Les applications supplémentaires sont constamment intégrées au contrôle de session.

## <a name="next-steps"></a>Étapes suivantes

- [Déployer le contrôle d'application d'accès conditionnel pour les applications Office 365](ocas-deploy-conditional-access-app-control.md)

- [En savoir plus sur les stratégies de session dans Office 365 Cloud App Security](ocas-session-policies.md)

- [En savoir plus sur les stratégies d'accès dans Office 365 Cloud App Security](ocas-access-policies.md) 