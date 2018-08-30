---
title: Contrôles d’accès administratif dans Office 365
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
description: 'Résumé : Vue d’ensemble de la catégorisation d’accéder à des contrôles d’administration et les données d’Office 365.'
ms.openlocfilehash: afa15d37aa8542985c59dbd9e3d82368421530e8
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528109"
---
# <a name="administrative-access-controls-in-office-365"></a>Contrôles d’accès administratif dans Office 365 

## <a name="introduction"></a>Présentation
Microsoft a investi fortement et en conséquence dans des systèmes et des contrôles qui automatisent la plupart des opérations d’Office 365 tout en limitant intentionnellement contenu client access de Microsoft. L’homme régissent le service et logiciel fonctionne le service. Cela permet à Microsoft gérer Office 365 à l’échelle, ainsi que de gérer les risques d’internes contre les menaces envers le contenu client telles que les acteurs malveillants, la sonde-hameçonnage d’un technicien Microsoft et ainsi de suite.

Par défaut, les ingénieurs de Microsoft ont zéro privilèges permanent et zéro permanent un accès au contenu client dans Office 365. Un ingénieur Microsoft ont limité, contrôlée et sécurisée de l’accès à d’un client contenu pour une durée limitée, mais uniquement lorsque cela est nécessaire pour les opérations de service et uniquement lorsque approuvé par un membre de la direction de Microsoft (et pour les clients qui sont une licence de la fonctionnalité de zone de sécurité client, le client).

Microsoft propose des services en ligne, y compris Office 365, à l’aide de plusieurs formulaires de remise dans le nuage :

- **Nuages publics** - inclut les versions de plusieurs clients d’Office 365, Azure et d’autres services qui sont hébergées dans Amérique du Nord, l’Amérique du Sud, Europe, Asie, Australie, etc..
- **Nuages national** - inclut tous les nuages souverains et fonctionnant sur tiers en dehors des États-Unis (à l’exception de celles mentionnées ci-dessus), telles que Office 365 en Chine (qui est géré par 21Vianet) et Office 365 en Allemagne (qui est géré par Microsoft, mais sous un modèle dans lequel un tiers de confiance données allemand, Deutsche Telekom, contrôles et surveille access de Microsoft pour les données du client et les systèmes qui contiennent des données du client).
- **Nuages gouvernement** - inclut les services Office 365 et Azure qui sont disponibles pour les clients pour le gouvernement des États-Unis.

À des fins de cet article, les services Office 365 incluent [Exchange Online](https://docs.microsoft.com/Exchange/exchange-online), [Exchange Online Protection](https://docs.microsoft.com/Office365/SecurityCompliance/eop/exchange-online-protection-overview), [SharePoint Online](https://docs.microsoft.com/sharepoint/sharepoint-online) (y compris [OneDrive entreprise](https://docs.microsoft.com/OneDrive/onedrive)) et [Skype pour les entreprises](https://docs.microsoft.com/SkypeForBusiness/skype-for-business-online), avec des informations supplémentaires sur certains contrôles d’accès [Entreprise Yammer](https://support.office.com/article/yammer-–-admin-help-e1464355-1f97-49ac-b2aa-dd320b179dbe?ui=en-US&rs=en-US&ad=US) . Autres services Office 365 sont hors de portée de cet article.

## <a name="office-365-access-controls"></a>Accéder à des contrôles Office 365
À des fins de contrôle d’accès, les données d’Office 365 sont classées sous forme de données du client ou d’autres types de données. Données du client sont toutes les données fournies par ou au nom d’un client à l’aide du client des services Office 365, tels que le contenu de client (contenu directement créés ou téléchargés par les utilisateurs Office 365, y compris les messages électroniques, contenu, SharePoint Online, les messages instantanés les contacts stockés dans Office 365, les documents et les éléments de calendrier) et les informations d’identification pour l’utilisateur final (EUII) (données qui est unique à un utilisateur ou est identifié par un utilisateur, mais n’inclut pas le contenu de client). 

Autres types de données incluent des données de compte (y compris les données d’administration, c'est-à-dire les informations fournies par les administrateurs lorsqu’ils d’inscription ou services d’achat et les données de paiement, qui est plus d’informations sur les instruments de paiement, tels que crédit détails de la carte), informations d’identification organisationnel (données qui peuvent être utilisées pour identifier un client ; ou utilisation ; il n’est pas identifié à un utilisateur individuel et n’inclut pas le contenu de client) et métadonnées système (inclut les journaux du service qui contiennent des paramètres de configuration, état du système, des adresses IP de Microsoft et des informations techniques sur les abonnements et les clients).

Microsoft a créé les mécanismes de contrôle d’accès pour vous assurer qu’il n’est approuvé d’accès aux données client ou accéder aux données de contrôle (utilisé pour gérer l’accès à d’autres types de données ou des fonctions dans l’environnement, y compris l’accès au contenu client ou EUII ; il inclut les mots de passe, les certificats de sécurité et autres données liées à l’authentification Microsoft) ou un accès à distance, physique ou logique non approuvé à l’environnement de production d’Office 365.

Les contrôles d’accès utilisées par Microsoft pour l’utilisation d’Office 365 peuvent être regroupés en trois catégories :
- Contrôles d’isolation
- Contrôles de personnel
- Contrôles de technologie

Combinées, ces contrôles permettent de prévenir et de détecter des actions malveillantes dans Office 365. Outre l’isolation, le personnel et les contrôles de technologie utilisées par Microsoft, il existe une quatrième catégorie des contrôles : celles implémentées par les clients.

Office 365 vous permet de gérer vos données que beaucoup dans les même façon que les données est géré dans les environnements sur site. La personne qui a inscrit automatiquement une organisation pour Office 365 devient administrateur général (admin). L’administrateur global a accès à toutes les fonctionnalités dans les portails de gestion (par exemple, centres d’administration et PowerShell à distance) et peut créer ou modifier les utilisateurs, assigner des rôles d’administrateur à d’autres personnes, réinitialiser les mots de passe utilisateur, gérer les licences utilisateur, gérer les domaines et approuver la zone de sécurité client demandes, entre autres choses. Il est recommandé que chaque organisation désigner au moins deux comptes d’administration et selon la taille de votre organisation, vous souhaiterez peut-être désigner plusieurs administrateurs qui remplissent différentes fonctions. Pour plus d’informations sur l’attribution d’autorisations et les rôles d’administration, voir [attribution des rôles d’administrateur dans Office 365](https://support.office.com/article/Assigning-admin-roles-in-Office-365-eac4d046-1afd-4f1a-85fc-8219c79e1504) et [rôles d’administrateur sur Office 365](https://support.office.com/article/Permissions-in-Office-365-DA585EEA-F576-4F55-A1E0-87090B6AAA9D).


## <a name="related-links"></a>Liens connexes

- [Contrôles d’isolation](office-365-isolation-controls.md)
- [Contrôles de personnel](office-365-personnel-controls.md)
- [Contrôles de technologie](office-365-technology-controls.md)
- [Surveillance et l’audit des contrôles d’accès](office-365-monitoring-and-auditing-access-controls.md)
- [Contrôles d’accès entreprise Yammer](office-365-yammer-enterprise-access-controls.md)