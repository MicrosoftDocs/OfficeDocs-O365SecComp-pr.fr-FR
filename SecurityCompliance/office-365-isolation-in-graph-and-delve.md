---
title: Isolation du locataire Office 365 dans le bureau du graphique et étudier
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
description: 'Résumé : Une explication de l’isolation du locataire dans le graphique Office et dans Delve.'
ms.openlocfilehash: bdc0f34d558f25ec139861c9a91261a72418f18a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527940"
---
# <a name="tenant-isolation-in-the-office-graph-and-delve"></a>Isolation du bureau des clients du graphique et étudier

## <a name="tenant-isolation-in-the-office-graph"></a>Isolation du locataire dans le graphique Office
L’activité de modèles de [Graphique Office](https://dev.office.com/officegraph) dans les services Office 365, notamment Exchange Online, SharePoint Online, Yammer, Skype pour entreprises, Azure Active Directory et plus d’informations et des services externes, tels que les autres services Microsoft ou les services tiers. Composants de graphique d’Office sont utilisés dans Office 365. Le graphique Office représente une collection de contenu et les activités et les relations entre eux qui se produisent dans l’ensemble d’Office. Il utilise machine sophistiquée techniques d’apprentissage pour connecter les personnes pour le contenu pertinent, les conversations et les personnes qui les entoure. Par exemple, l’index du client dans SharePoint Online a un index de graphique Office qui est utilisé pour traiter les requêtes Delve, le moteur de traitement Analytique dans SharePoint Online est utilisé pour stocker des signaux et calculer insights et Exchange Online calcule de chaque utilisateur cache de destinataires comme entrée en analytique du client.

Le graphique Office contient des informations sur les objets d’entreprise, telles que des personnes et des documents, ainsi que les relations et les interactions entre ces objets. Les relations et les interactions sont représentées comme *bords*. Le graphique Office est segmenté par client telles que les bords ne peuvent exister entre les *nœuds* dans la même Location. Un *nœud* est une entité avec un identificateur URI (Uniform Resource), type de nœud, liste de contrôle d’accès et un ensemble de facettes contenant les *métadonnées* et les côtés. Chaque nœud est associé aux métadonnées et bords, organisés en *facettes* comme dans le modèle commun de la base de connaissances. *Métadonnées* sont nommées propriétés stockées sur un nœud qui peut être utilisé pour la recherche, le filtrage, ou l’analyse dans le graphique office. Une *facettes* est une collection logique de métadonnées et les bords sur un nœud. Chaque facettes décrit un aspect d’un nœud. 

Le graphique Office ne met pas toutes les données dans un référentiel unique ; au lieu de cela, il stocke des métadonnées et des relations de données se trouve ailleurs. Le graphique Office se compose de plusieurs magasins de données et les composants de traitement :
- Le magasin de graphique client fournit un stockage en bloc optimisé pour analytique efficace.
- Le Cache de contenu actif fournit un accès aléatoire rapide pour le nœud actif et des bords pour une expérience utilisateur de lecteur.
- Le routeur d’entrée avertit les composants internes et externes des modifications apportées au graphique client.

Analytique au sein de chaque charge de travail déduire insights pertinents pour les calculs de client à l’échelle et les dirige vers le graphique de client. Client analytique raisons sur toutes les activités dans une location pour générer des informations sur les modèles de comportement. Par exemple, Exchange Online calcule le cache de destinataires pour chaque utilisateur avec analytique efficacement raison sur boîte aux lettres de chaque utilisateur. Ces analytique par utilisateur produire un ensemble de *Bords RecipientCache* sur chaque personne, qui à son tour envoyée vers le graphique de client. Cela permet de conserver la quantité de traitement analytique comme près les données sources que possible.

## <a name="tenant-isolation-in-delve"></a>Isolation du locataire dans étudier
Comme mentionné précédemment, le graphique Office démarre une expérience qui aident les personnes découvrir et collaborer sur des activités en cours dans leur entreprise et fournit une plateforme de centrées sur l’entité pour analytique à raison sur l’activité et de contenu entre les charges de travail et au-delà d’Office 365. Étudier est le premier telle expérience par le graphique Office. Entrez est une expérience web Office 365 qui couvre le contenu d’entreprise Yammer et Office 365 pour les utilisateurs d’Office 365 via le graphique Office. L’expérience web affiche les données en tant que cartes différentes, chacune avec un même thème, tel que *Trending proches de moi* ou *modifiés par moi*. Chaque carte se compose de plusieurs cartes de document affichant le texte de la synthèse et une image à partir du document. La carte permet aux utilisateurs de faire ouvrir le document ou une page de Yammer pour le document. Il existe une page pour chaque personne dans un client Office 365 qui affiche les documents les plus pertinents pour cette personne et les icônes qui peuvent appeler Exchange Online ou Skype pour les entreprises pour interagir avec cette personne. Étant donné que Delve est basé sur l’API de graphique Office, il est lié par l’isolement basée sur le client de cette API.