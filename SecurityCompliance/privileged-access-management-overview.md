---
title: Gestion des accès privilégiés dans Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
ms.custom: Ent_Solutions
ms.assetid: ''
description: Utilisez cette rubrique pour en savoir plus sur la gestion des accès privilégiés dans Office 365
ms.openlocfilehash: 2a464bacaa568515e470e29a0c9c45a91a79cf8e
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2019
ms.locfileid: "31001247"
---
# <a name="privileged-access-management-in-office-365"></a>Gestion des accès privilégiés dans Office 365

> [!IMPORTANT]
> Cette rubrique traite des conseils de déploiement et de configuration pour les fonctionnalités uniquement disponibles dans Office 365 E5 et les SKU de conformité avancée.

La gestion des accès privilégiés permet le contrôle d'accès granulaire sur les tâches d'administration privilégiée dans Office 365. Elle peut aider à protéger votre organisation contre les violations susceptibles d'utiliser des comptes d'administrateur privilégié existants avec un accès permanent aux données sensibles ou un accès aux paramètres de configuration critiques. Une fois que vous avez activé la gestion des accès privilégiés, les utilisateurs doivent demander un accès juste-à-temps pour effectuer des tâches élevées et privilégiées via un flux de travail d'approbation hautement étendu et lié au temps. Cela permet aux utilisateurs d'effectuer la tâche à tout moment, sans risquer d'exposer les données sensibles ou les paramètres de configuration critiques. L'activation de la gestion des accès privilégiés dans Office 365 permettra à votre organisation de fonctionner avec des privilèges permanents et de fournir une couche de défense contre les vulnérabilités dues à ce type d'accès administratif permanent.

Pour obtenir une vue d'ensemble rapide du flux de travail intégré du client et de la gestion de l'accès privilégié, reportez-vous à cette rubrique [customEr Lockbox and Privileged Access Management in Office 365 Video](https://go.microsoft.com/fwlink/?linkid=2066800).

## <a name="layers-of-protection"></a>Couches de protection

La gestion des accès privilégiés complète les autres protections des données et des fonctionnalités d'accès dans l'architecture de sécurité Office 365. En activant la gestion des accès privilégiés dans le cadre d'une approche intégrée de la sécurité et de la protection de votre organisation, un modèle de sécurité en couche peut être utilisé pour optimiser la protection des informations sensibles et des paramètres de configuration d'Office 365. Comme indiqué dans le diagramme ci-dessous, l'activation de la gestion des accès privilégiés permet de créer des versions de protection fournies avec le chiffrement natif des données Office 365 et le modèle de sécurité de contrôle d'accès basé sur un rôle des services Office 365. Lorsqu'elles sont utilisées conjointement avec [Azure ad Privileged identIty Management](https://docs.microsoft.com/azure/active-directory/active-directory-privileged-identity-management-configure), ces deux fonctionnalités fournissent un contrôle d'accès avec un accès juste-à-temps à différentes étendues.

![Protection multiNiveau dans Office 365](media/pam-layered-protection.png)

La gestion des accès privilégiés dans Office 365 peut être définie et étendue au niveau de la **tâche** , tandis que Azure ad Privileged Identity Management applique la protection au niveau du **rôle** avec la possibilité d'exécuter plusieurs tâches.  Azure AD Privileged Identity Management principalement permet de gérer les accès aux rôles AD et aux groupes de rôles, tandis que la gestion des accès privilégiés dans Office 365 est appliquée uniquement au niveau de la tâche.

- **Activation de la gestion des accès privilégiés dans Office 365 tout en utilisant Azure ad Privileged identIty Management:** L'ajout de la gestion des accès privilégiés dans Office 365 fournit une autre couche granulaire de fonctionnalités de protection et d'audit pour l'accès privilégié aux données Office 365.

- **Activation de la gestion des identités Azure ad privilégiée tout en utilisant déjà la gestion des accès privilégiés dans Office 365:**  L'ajout de la gestion des identités Azure AD privilégiées à la gestion des accès privilégiés dans Office 365 peut étendre l'accès privilégié aux données en dehors d'Office 365, qui est principalement défini par le rôle ou l'identité d'un utilisateur.  

## <a name="privileged-access-management-architecture-and-process-flow"></a>Architecture et flux de processus de gestion des accès privilégiés

Chacun des flux de processus suivants décrit l'architecture de l'accès privilégié et son interaction avec le substrat Office 365, l'audit Office 365 et l'instance d'exécution de la gestion d'Exchange.

### <a name="step-1-configuring-a-privileged-access-policy"></a>Étape 1: configuration d'une stratégie d'accès privilégié

Lors de la configuration d'une stratégie d'accès privilégié en utilisant le [Centre d'administration Microsoft 365](https://admin.microsoft.com) ou Exchange Management PowerShell, vous créez et définissez la stratégie et la fonctionnalité accès privilégié traite les attributs de stratégie dans le substrat Office 365 et enregistre l'activité dans le centre de sécurité et conformité Office 365. La stratégie est désormais activée et prête à gérer les demandes d'approbations entrantes.

![Étape 1: création de stratégies](media/pam-step1-policy-creation.jpg)

### <a name="step-2-access-request"></a>Étape 2: demande d'accès

À l'aide du [Centre d'administration Microsoft 365](https://admin.microsoft.com) ou de PowerShell de gestion Exchange, les utilisateurs peuvent demander l'accès à des tâches élevées ou privilégiées. La fonctionnalité accès privilégié envoie la demande au substrat Office 365 pour traitement sur la stratégie d'accès aux privilèges configurée et enregistre l'activité dans les journaux du centre de sécurité et de conformité d'Office 365.

![Étape 2: demande d'accès](media/pam-step2-access-request.jpg)

### <a name="step-3-access-approval"></a>Étape 3: approbation d'accès

Une demande d'approbation est générée et le groupe d'approbation est averti par courrier électronique de la demande en attente. Si l'approbation est accordée, la demande d'accès privilégié est traitée comme une approbation et la tâche est prête à être terminée. Si la demande est refusée, la tâche est bloquée et aucun accès n'est accordé au demandeur. Le demandeur est informé de l'approbation ou du refus de la demande via un message électronique.

![Étape 3: approbation de l'accès](media/pam-step3-access-approval.jpg)

### <a name="step-4-access-processing"></a>Étape 4: traitement de l'accès

Pour les demandes approuvées, la tâche est traitée par l'instance d'exécution de la gestion d'Exchange. L'approbation est vérifiée par rapport à la stratégie d'accès privilégié et traitée par le substrat Office 365. Toutes les activités de la tâche sont consignées dans le centre de sécurité et de conformité Office 365.

![Étape 4: traitement de l'accès](media/pam-step4-access-processing.jpg)

## <a name="frequently-asked-questions"></a>Questions fréquemment posées

### <a name="what-skus-do-i-need-to-use-privileged-access-in-office-365"></a>Quels sont les UGS dont j'ai besoin pour utiliser l'accès privilégié dans Office 365?
La gestion des accès privilégiés est actuellement disponible uniquement pour les clients disposant d'Office 365 E5 et de SKU de conformité avancée.

### <a name="when-will-privileged-access-be-available-for-office-365-workloads-beyond-exchange"></a>Quand l'accès privilégié sera-t-il disponible pour les charges de travail Office 365 au-delà d'Exchange?
Nous prévoyons de proposer cette fonctionnalité dans les autres charges de travail Office 365. Lorsque nous sommes prêts à partager une chronologie, celle-ci sera disponible via la feuille de [route Microsoft 365](https://www.microsoft.com/microsoft-365/roadmap).

### <a name="my-organization-needs-more-than-30-privileged-access-polices-will-this-limit-be-increased"></a>Mon organisation a besoin de plus de 30 stratégies d'accès privilégié, cette limite sera-t-elle augmentée?

Nous préVoyons d'augmenter rapidement la limite actuelle de 30 stratégies d'accès privilégié par organisation Office 365.

### <a name="do-i-need-to-be-a-global-admin-to-manage-privileged-access-in-office-365"></a>Ai-je besoin d'être un administrateur général pour gérer l'accès privilégié dans Office 365?
Non, le rôle de gestion des rôles Exchange doit être attribué aux comptes qui géreront l'accès privilégié dans Office 365. Toutefois, le rôle administrateur général inclut ce rôle par défaut et peut être utilisé pour gérer l'accès privilégié si vous ne souhaitez pas configurer le rôle de gestion de rôle en tant qu'autorisation de compte autonome. Les utilisateurs qui sont inclus dans un groupe d'approbateurs n'ont pas besoin d'être un administrateur général ou ont le rôle de gestion de rôle affecté à la révision et l'approbation des demandes.

### <a name="how-is-privileged-access-management-in-office-365-related-to-customer-lockbox"></a>Comment la gestion des accès privilégiés dans Office 365 est-elle liée au référentiel sécurisé du client?
Le [référentiel sécurisé du client](https://docs.microsoft.com/office365/admin/manage/customer-lockbox-requests) autorise un niveau de contrôle d'accès pour les organisations à accéder aux données par leur fournisseur de services, c'est-à-dire Microsoft. La gestion des accès privilégiés dans Office 365 autorise un contrôle d'accès granulaire au sein d'une organisation pour toutes les tâches privilégiées d'Office 365.
