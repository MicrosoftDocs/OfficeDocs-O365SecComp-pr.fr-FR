---
title: Privilèges d’accès gestion dans Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.service: o365-solutions
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Strat_O365_IP
ms.custom: Ent_Solutions
ms.assetid: ''
description: Utilisez cette rubrique pour en savoir plus sur les privilèges accéder à la gestion dans Office 365
ms.openlocfilehash: f3cd5fb263fe3bb83d60a7938f0e22dc38f199e3
ms.sourcegitcommit: b0b0b716718c22779c7c04775b8010d65cd6656b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28723231"
---
# <a name="privileged-access-management-in-office-365"></a>Privilèges d’accès gestion dans Office 365

> [!IMPORTANT]
> Cette rubrique traite des instructions de déploiement et de configuration pour les fonctionnalités uniquement actuellement disponibles dans Office 365 E5 et références de conformité avancées.

Un accès privilégié gestion permet de contrôle d’accès granulaire sur les tâches d’administration privilégié dans Office 365. Il permet de protéger votre organisation contre les violations qui peuvent utiliser des comptes d’administration privilégié existants avec accès permanent à des données sensibles ou l’accès aux paramètres de configuration critique. Après avoir activé la gestion de l’accès privilégié, les utilisateurs devront demander l’accès juste-à-temps pour effectuer des tâches avec des privilèges élevés et privilégiés via un flux de travail d’approbation qui est hautement et de temps. Ainsi, les utilisateurs juste suffisamment-accès pour effectuer la tâche en cours, sans risque d’exposition des données sensibles ou des paramètres de configuration critique. Activation de la gestion des accès privilégié dans Office 365 permettra à votre organisation de fonctionner avec des privilèges zéro permanent et fournir une couche de protection contre les vulnérabilités résultant en raison de cet accès administratif permanent. 

## <a name="layers-of-protection"></a>Couches de protection

Un accès privilégié gestion complète autres protections de fonctionnalité de données et l’accès au sein de l’architecture de sécurité d’Office 365. À l’activation de la gestion des accès privilégié dans le cadre d’une approche intégrée à la sécurité et protection de votre organisation, un modèle de sécurité permet d’optimiser la protection des informations sensibles et les paramètres de configuration d’Office 365. Comme indiqué dans le schéma ci-dessous, l’activation de privilèges permet de gestion d’access s’appuie sur la protection fournie avec le chiffrement de données Office 365 natif et le modèle de sécurité de contrôle d’accès basé sur un rôle des services Office 365. Lorsqu’elle est utilisée conjointement avec [la gestion des identités Azure AD privilégié](https://docs.microsoft.com/azure/active-directory/active-directory-privileged-identity-management-configure), ces deux fonctionnalités fournissent le contrôle d’accès avec un accès à différentes étendues juste-à-temps.

![Protection multiniveau dans Office 365](media/pam-layered-protection.png)

Un accès privilégié gestion dans Office 365 peut être définie et étendue au niveau de la **tâche** , de gestion des identités Azure AD privilégié s’applique la protection au niveau du **rôle** avec la possibilité d’exécuter plusieurs tâches.  Gestion des identités Azure AD privilégié permet principalement d’accès aux rôles AD et des groupes de rôles de gestion, tandis que les privilèges d’accès gestion dans Office 365 s’applique uniquement au niveau de la tâche.

- **Gestion dans Office 365 de privilèges d’activation d’accès lorsque vous utilisez déjà la gestion des identités Azure AD privilégié :** Ajout de gestion de l’accès privilégié dans Office 365 fournit une autre couche précise des fonctionnalités de protection et d’audit pour l’accès aux données d’Office 365 privilégié.

- **Activation Azure AD privilégié déjà à l’aide de la gestion des identités privilégié gestion des accès dans Office 365 :**  Ajout de la gestion des identités Azure AD privilégié avec privilèges gestion des accès dans Office 365 peut étendre les privilèges d’accès aux données en dehors d’Office 365 principalement défini par rôle ou l’identité d’un utilisateur.  

## <a name="privileged-access-management-architecture-and-process-flow"></a>Accès privilégié management architecture et flux du processus

Chacun des flux de processus suivant décrivent l’architecture de détient l’accès et la façon dont il interagit avec le Network substrate Office 365, Office 365 l’audit et l’instance d’exécution Exchange Management.

### <a name="step-1-configuring-a-privileged-access-policy"></a>Étape 1 : Configuration d’une stratégie d’accès privilégié

Lorsque vous configurez une stratégie d’accès privilégié via le centre d’administration d’Office 365 ou Exchange Management PowerShell, vous créez et que vous définissez la stratégie et la fonctionnalité d’accès privilégié traite les attributs de stratégie dans le Network substrate Office 365 et les journaux du activités dans le centre de conformité et de sécurité pour Microsoft Office 365. La stratégie est maintenant activé et prêt à traiter les demandes entrantes pour les approbations.

![Étape 1 : création d’une stratégie](media/pam-step1-policy-creation.jpg)

### <a name="step-2-access-request"></a>Étape 2 : Demande d’accès

À l’aide du centre d’administration d’Office 365 ou Exchange Management PowerShell, les utilisateurs peuvent demander l’accès à des tâches avec des privilèges élevés ou privilégiés. La fonctionnalité d’accès privilégié envoie la demande à la Network substrate Office 365 pour le traitement par rapport à la stratégie d’accès configurés avec des privilèges et enregistre le sctivity de sécurité Office 365 et les journaux de centre de conformité.

![Étape 2 : demande d’accès](media/pam-step2-access-request.jpg)

### <a name="step-3-access-approval"></a>Étape 3 : Approbation d’accès

Une demande d’approbation est générée et le groupe d’approbation est averti par courrier électronique de la demande en attente. Si l’approbation est accordée, la demande d’accès privilégié est traitée comme une approbation et la tâche est prête à être terminé. Si la demande est refusée, tâche est bloquée et aucun accès n’est accordé à la reqeustor. Le demandeur sera averti de l’approbation de la demande ou de refus via le message électronique.

![Étape 3 : approbation d’accès](media/pam-step3-access-approval.jpg)

### <a name="step-4-access-processing"></a>Étape 4 : Traitement de l’accès

Pour les demandes approuvées, la tâche est traitée par l’instance d’exécution Exchange Management. L’approbation est vérifiée par rapport à la stratégie d’accès privilégié et traitée par la Network substrate Office 365. Toutes les activités de la tâche sont enregistrée dans le centre de conformité et de sécurité pour Microsoft Office 365.

![Étape 4 : traitement de l’accès](media/pam-step4-access-processing.jpg)

## <a name="frequently-asked-questions"></a>Questions fréquemment posées

### <a name="what-skus-do-i-need-to-use-privileged-access-in-office-365"></a>Quelles versions clientes ai-je besoin pour utiliser un accès privilégié dans Office 365 ?
Un accès privilégié gestion n’est actuellement disponible pour les clients avec Office 365 E5 et références de conformité avancées.

### <a name="when-will-privileged-access-be-available-for-office-365-workloads-beyond-exchange"></a>Lorsqu’un accès privilégié sera disponible pour des charges de travail Office 365 au-delà Exchange ?
Nous prévoyons de proposer cette fonctionnalité dans les autres charges de travail Office 365 bientôt. Lorsque nous sommes prêts à partager une chronologie, il sera disponible par le biais de la [Feuille de route Microsoft 365](https://www.microsoft.com/microsoft-365/roadmap).

### <a name="my-organization-needs-more-than-30-privileged-access-polices-will-this-limit-be-increased"></a>Stratégies de besoins de mon organisation plus de 30 accès privilégié, cette limite augmentera ?

Nous comptons augmenter la limite actuelle de 30 stratégies d’accès privilégié par l’organisation Office 365 bientôt.

### <a name="do-i-need-to-be-a-global-admin-to-manage-privileged-access-in-office-365"></a>Je dois être un administrateur Global pour gérer l’accès privilégié dans Office 365
Non, vous devez disposer du rôle de gestion des rôles Exchange attribué à des comptes de gérer un accès privilégié dans Office 365. Toutefois, le rôle d’administrateur Global inclut ce rôle par défaut et peut être utilisé pour gérer un accès privilégié si vous ne souhaitez pas configurer le rôle de gestion de rôle comme une autorisation compte autonome. Les utilisateurs qui sont inclus dans le groupe d’un approbateurs n’avez pas besoin être un administrateur Global ou avoir le rôle de gestion des rôles affecté à examiner et approuver les demandes. 

### <a name="how-is-privileged-access-management-in-office-365-related-to-customer-lockbox"></a>Quelle est la gestion des accès privilégié dans Office 365 liés à la zone de sécurité client ?
[Zone de sécurité client](https://docs.microsoft.com/office365/admin/manage/customer-lockbox-requests) permet à un niveau de contrôle d’accès pour les organisations pour l’accès aux données par leur fournisseur de services, par exemple, Microsoft. Un accès privilégié gestion dans Office 365 permet de contrôle d’accès granulaire au sein d’une organisation pour toutes les tâches Office 365 privilégié.
