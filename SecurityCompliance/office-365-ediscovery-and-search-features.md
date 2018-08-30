---
title: Vue d’ensemble des fonctionnalités de recherche et de découverte électronique Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: Vue d’ensemble de la fonctionnalité de découverte et d’autres fonctionnalités de recherche dans Office 365 pour auditer l’utilisation et la transparence.
ms.openlocfilehash: 2d5cc2533c195b51f685aebd8da4462518116905
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528134"
---
# <a name="ediscovery-and-search-features"></a>Fonctionnalités de recherche et de découverte électronique 

## <a name="ediscovery"></a>eDiscovery
La fonctionnalité de découverte électronique fournit un emplacement unique pour les administrateurs, les responsables de la conformité, et autres autorisés aux utilisateurs de réaliser une enquête complète sur l’activité utilisateur Office 365. Responsables de la sécurité avec les autorisations appropriées peuvent effectuer des recherches et archives permanentes sur le contenu. Les résultats de recherche sont les mêmes résultats que vous obtenez à partir d’une recherche de contenu, sauf qu’un cas eDiscovery est créé pour les suspensions appliquées. Les résultats de recherches de découverte électronique sont chiffrés de la sécurité et les données exportées peuvent être analysées à l’aide de la [découverte électronique avancée](https://support.office.com/article/office-365-advanced-ediscovery-fd53438a-a760-45f6-9df4-861b50161ae4).

## <a name="content-search"></a>Recherche de contenu
[Recherche de contenu](https://support.office.com/article/Run-a-Content-Search-in-the-Office-365-Security-Compliance-Center-61852fd9-fe8a-4880-a339-cb19ed3bff4a) est un nouvel outil de recherche de découverte électronique dans la sécurité et de centre de conformité qui fournit une montée en charge améliorée et de performances sur les outils de recherche eDiscovery précédents. Vous pouvez utiliser la recherche de contenu pour rechercher les boîtes aux lettres, les dossiers publics, les sites SharePoint Online et OneDrive pour des sites. Recherche de contenu est spécifiquement conçue pour les recherches de très grande taille. Il n’existe aucune limite sur le nombre de boîtes aux lettres et de sites que vous pouvez rechercher. Il n’existe également aucune limite sur le nombre de recherches autorisées à exécuter en même temps. Après avoir exécuté une recherche, le nombre de sources de contenu et un estimation du nombre de recherche résultats sont affichés dans le volet d’informations sur la page de recherche, dans laquelle vous pouvez afficher les résultats ou les exporter vers un ordinateur local. Si votre organisation a un abonnement à Office 365 entreprise E5, vous pouvez également [préparer les résultats](https://support.office.com/article/Run-a-Content-Search-in-the-Office-365-Security-Compliance-Center-61852fd9-fe8a-4880-a339-cb19ed3bff4a#prepare) d’analyse d’utilisation des fonctionnalités puissantes analytique de [eDiscovery Office 365 avancés](http://go.microsoft.com/fwlink/p/?LinkID=620116).

## <a name="audit-log-search"></a>Recherche des journaux d’audit
Outre le suivi des modifications dans leur organisation Office 365, les clients peuvent également afficher les rapports d’audit et exporter des journaux d’audit. Une fois que l’audit est activé pour un client Office 365, utilisateur et l’activité d’administration pour ce client est enregistré dans les journaux des événements et objet d’une recherche. Par exemple, vous pouvez utiliser pour suivre les actions effectuées sur une boîte aux lettres par les utilisateurs autres que le propriétaire de la boîte aux lettres la journalisation d’audit. En outre, aux règlements pouvant utiliser les fonctionnalités de recherche et de filtrage pour voir si un utilisateur a affiché ou télécharger un document spécifique, ou si un administrateur a effectué les activités de gestion des utilisateurs ou apporté des modifications à la configuration du client au cours des 90 derniers jours. Résultats de recherche peuvent contenir des informations légales importantes sur les activités spécifiques qui ont été effectués par un utilisateur ou un administrateur. Pour obtenir une description de l’utilisateur et les activités administratives qui sont consignées dans Office 365, voir [les activités contrôlé dans Office 365](https://support.office.com/article/Search-the-audit-log-in-the-Office-365-Security-Compliance-Center-0d4d0f35-390b-4518-800e-0c7ec95e946c#auditlogevents) .

Événements liés à SharePoint Online et OneDrive entreprise sont affichés dans le journal de 30 minutes de leur occurrence. Événements à partir d’Exchange Online s’affichent dans les journaux d’audit dans les 24 heures d’occurrence. Événements de connexion d’Azure Active Directory sont disponibles dans les minutes d’occurrence et autres événements directory d’Azure Active Directory sont disponibles dans les 24 heures d’occurrence. Événements dans les résultats de recherche du journal d’audit peuvent également être exportés pour une analyse approfondie. (Un maximum de 50 000 entrées peut être exporté à partir d’une recherche de journal d’audit unique. Pour exporter des entrées plus cette limite, réduisez la plage de dates, ou exécuter plusieurs recherches de journal d’audit.)

Le tableau suivant détaille certaines des informations qui s’affiche dans les rapports d’activité. Consultez [journal d’audit de propriétés détaillées dans Office 365](https://support.office.com/article/detailed-properties-in-the-office-365-audit-log-ce004100-9e7f-443e-942b-9b04098fcfc3
) pour plus d’informations sur les propriétés sont collectées par chaque charge de travail d’Office 365.

| Propriété | Description |
|----------------|----------------------------------------------------------------------------------------------------------------------|
| Date | Date et heure de l’événement |
| Utilisateur | Utilisateur qui a effectué l’action |
| ClientIP | Adresse IPv4 ou IPv6 de l’appareil qui a été utilisé lors de l’activité a été enregistrée. |
| CreationTime | Date et heure en temps universel coordonné (UTC) lorsque l’utilisateur a effectué l’activité. |
| Source d’événement | Identifie qu’un événement s’est produite. Les valeurs possibles sont SharePoint et ObjectModel. |
| ID | ID de l’entrée du rapport. L’ID identifie l’entrée du rapport. |
| Opération | Nom de l’utilisateur ou d’une activité, qui correspond à la valeur sélectionnée dans les résultats d’affichage pour l’activité de l’utilisateur. |
| OrganizationId | GUID Office 365 service de l’organisation où l’événement s’est produite. |
| UserAgent | Informations sur le navigateur de l’utilisateur fourni par le navigateur. |
| Nom d’utilisateur | Utilisateur qui a exécuté l’action (spécifiée dans la propriété Operation) qui a provoqué l’enregistrement en cours de journalisation. |
| UserType | Type d’utilisateur qui a effectué l’opération. Les valeurs suivantes indiquent le type d’utilisateur. |
|  | 0 indique qu’un utilisateur standard. |
|  | 2 indique un administrateur de votre organisation Office 365. |
|  | 3 indique un compte de système Microsoft datacenter administrateur ou centre de données. |
| Charge de travail | Service Office 365 dans lequel l’activité s’est produite. Les valeurs possibles pour cette propriété sont : |
|  | Exchange Online |
|  | SharePoint Online |
|  | OneDrive Entreprise |
|  | Rapports d’Azure Active Directory |


Journaux d’audit pour obtenir la procédure détaillée pour la recherche Office 365, consultez les [journaux d’audit de recherche dans la sécurité pour Microsoft Office 365 et le centre de conformité](https://support.office.com/article/Search-the-audit-log-in-the-Office-365-Security-Compliance-Center-0d4d0f35-390b-4518-800e-0c7ec95e946c).

## <a name="search-unified-audit-log"></a>Recherche unifiée journal d’Audit
La fonctionnalité de recherche des journaux d’Audit de la sécurité et le centre de conformité peut servir à rechercher dans le journal d’audit unifiée. Office 365 offre également la possibilité pour rechercher ce journal à l’aide de PowerShell à distance. Spécifiquement, l' [applet de commande Search-UnifiedAuditLog](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/Search-UnifiedAuditLog?view=exchange-ps) dans Exchange Online PowerShell peut être utilisée pour rechercher le journal d’audit unifiée des événements liés aux opérations de l’utilisateur à partir d’Exchange Online, SharePoint Online, OneDrive pour les entreprises et Azure AD. Vous pouvez rechercher tous les événements dans une plage de dates spécifiée, ou vous pouvez filtrer les résultats en fonction des critères spécifiques, comme une action spécifique, l’utilisateur ayant exécuté l’action ou l’objet cible. Les administrateurs peuvent utiliser 3 jusqu'à l’exécution simultanée de sessions Exchange Online PowerShell pour diviser des recherches de plage de date de grande taille.
