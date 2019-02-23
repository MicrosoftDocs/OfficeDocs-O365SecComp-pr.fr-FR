---
title: Contrôles d’accès des administrateurs dans Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: "Résumé: vue d'ensemble des contrôles d'accès administratif et de la catégorisation des données d'Office 365."
ms.openlocfilehash: b23fcdcb6c790b3860a24a555424beb3bb99e4f4
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216024"
---
# <a name="administrative-access-controls-in-office-365"></a>Contrôles d’accès des administrateurs dans Office 365 

## <a name="introduction"></a>Introduction
Microsoft a investi largement et en conséquence sur les systèmes et les contrôles qui automatisent la plupart des opérations Office 365 tout en limitant intentionnellement l'accès de Microsoft au contenu client. Les êtres humains gouvernent le service et le logiciel fonctionne avec le service. Cela permet à Microsoft de gérer Office 365 à l'horizontale, ainsi que de gérer les risques de menaces internes pour le contenu du client, comme les acteurs malveillants, le Spear Phishing d'un ingénieur Microsoft, et ainsi de suite.

Par défaut, les ingénieurs Microsoft disposent de zéro privilège administratif permanent et d'un accès permanent au contenu client dans Office 365. Un ingénieur Microsoft peut disposer d'un accès limité, audité et sécurisé au contenu d'un client pendant une durée limitée, mais uniquement en cas de nécessité pour les opérations de service, et uniquement lorsqu'il est approuvé par un membre de la gestion des cadres dirigeants de Microsoft (et pour les clients qui sont licence pour la fonctionnalité de référentiel sécurisé du client, le client).

Microsoft fournit des services en ligne, y compris Office 365, à l'aide de plusieurs formes de remise en nuage:

- **Nuages publics** : inclut des versions mutualisées d'Office 365, Azure et d'autres services hébergés en Amérique du Nord, Amérique du Sud, Europe, Asie, Australie, etc.
- **Clouds nationaux** : inclut tous les nuages souverains et tiers à l'extérieur des États-Unis (à l'exception de ceux mentionnés ci-dessus), tels que Office 365 en Chine (qui est géré par 21ViaNet) et Office 365 en Allemagne (qui est géré par Microsoft mais sous un modèle dans lequel un tiers de confiance de données allemand, Deutsche Telekom, contrôle et surveille l'accès de Microsoft aux données client et aux systèmes contenant des données client).
- **Clouds gouvernementaux** : inclut Office 365 et Azure services qui sont disponibles pour les clients gouvernementaux des États-Unis.

Pour les besoins de cet article, les services Office 365 incluent [Exchange Online](https://docs.microsoft.com/Exchange/exchange-online), [Exchange Online Protection](https://docs.microsoft.com/Office365/SecurityCompliance/eop/exchange-online-protection-overview), [SharePoint Online](https://docs.microsoft.com/sharepoint/sharepoint-online) (y compris [OneDrive entreprise](https://docs.microsoft.com/OneDrive/onedrive)) et [Skype entreprise](https://docs.microsoft.com/SkypeForBusiness/skype-for-business-online), avec des informations supplémentaires à propos de certains contrôles d'accès aux [entreprises Yammer](https://support.office.com/article/yammer-–-admin-help-e1464355-1f97-49ac-b2aa-dd320b179dbe?ui=en-US&rs=en-US&ad=US) . Les autres services Office 365 sont hors de portée pour cet article.

## <a name="office-365-access-controls"></a>Contrôles d'accès Office 365
Pour des raisons de contrôle d'accès, les données Office 365 sont classées en tant que données client ou d'autres types de données. Les données client sont toutes les données fournies par ou pour le compte d'un client par le biais de l'utilisation des services Office 365 par le client (contenu directement créé ou téléchargé par les utilisateurs d'Office 365, y compris les courriers électroniques, le contenu SharePoint Online, les messages instantanés, les éléments de calendrier, les documents et les contacts stockés dans Office 365) et les informations d'identification de l'utilisateur final (EUII) (données propres à un utilisateur ou pouvant être liées à un utilisateur individuel, mais qui n'incluent pas de contenu client). 

Les autres types de données incluent les données de compte (y compris les données administratives, qui sont les informations fournies par les administrateurs lorsqu'ils se connectent ou achètent des services, ainsi que les données de paiement, qui sont des informations sur les instruments de paiement, tels que les informations de carte de crédit), informations identifiables au sein de l'organisation (données qui peuvent être utilisées pour identifier un locataire ou des données d'utilisation; il ne peut pas être lié à un utilisateur individuel et n'inclut pas le contenu du client), ainsi que les métadonnées système (y compris les journaux de service qui contiennent des paramètres de configuration, État du système, adresses IP Microsoft et informations techniques sur les abonnements et les clients).

Microsoft a établi des mécanismes de contrôle d'accès pour s'assurer que personne ne dispose d'un accès non approuvé aux données du client ou aux données de contrôle d'accès (utilisé pour gérer l'accès à d'autres types de données ou fonctions au sein de l'environnement, y compris l'accès au contenu du client ou à EUII; IT inclut les mots de passe Microsoft, les certificats de sécurité et d'autres données liées à l'authentification) ou un accès physique, logique ou distant non approuvé à l'environnement de production Office 365.

Les contrôles d'accès utilisés par Microsoft pour Office 365 peuvent être regroupés en trois catégories:
- Contrôles d'isolation
- Contrôles du personnel
- Contrôles technologiques

Lorsqu'ils sont combinés, ces contrôles aident à empêcher et à détecter les actions malveillantes dans Office 365. Outre les contrôles d'isolation, de personnel et de technologie utilisés par Microsoft, il existe une quatrième catégorie de contrôles: ceux mis en œuvre par les clients.

Office 365 vous permet de gérer vos données de la même façon que les données sont gérées dans des environnements locaux. La personne qui s'inscrit à une organisation pour Office 365 devient automatiquement administrateur général (administrateur). L'administrateur global a accès à toutes les fonctionnalités des portails de gestion (par exemple, les centres d'administration et PowerShell à distance), et peut créer ou modifier des utilisateurs, attribuer des rôles d'administrateur à d'autres utilisateurs, réinitialiser des mots de passe utilisateur, gérer des licences utilisateur, gérer des domaines et approuver le référentiel sécurisé du client. demandes, entre autres. Il est recommandé que chaque organisation désigne au moins deux comptes administrateur, et selon la taille de votre organisation, vous pouvez désigner plusieurs administrateurs qui utilisent différentes fonctions. Pour plus d'informations sur l'attribution des rôles et des autorisations d'administrateur, consultez la rubrique [attribution de rôles d'administrateur dans office 365](https://support.office.com/article/Assigning-admin-roles-in-Office-365-eac4d046-1afd-4f1a-85fc-8219c79e1504) et [à propos des rôles d'administrateur Office 365](https://support.office.com/article/Permissions-in-Office-365-DA585EEA-F576-4F55-A1E0-87090B6AAA9D).


## <a name="related-links"></a>Liens connexes

- [Contrôles d'isolation](office-365-isolation-controls.md)
- [Contrôles du personnel](office-365-personnel-controls.md)
- [Contrôles technologiques](office-365-technology-controls.md)
- [Surveillance et audit des contrôles d’accès](office-365-monitoring-and-auditing-access-controls.md)
- [Contrôles d’accès Yammer Entreprise](office-365-yammer-enterprise-access-controls.md)