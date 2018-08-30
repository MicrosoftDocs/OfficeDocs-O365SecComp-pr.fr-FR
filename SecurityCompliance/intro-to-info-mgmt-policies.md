---
title: Introduction aux stratégies de gestion des informations
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/16/2014
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- WSU150
- SPO160
- OSU150
- MET150
ms.assetid: 63a0b501-ba59-44b7-a35c-999f3be057b2
description: Une stratégie de gestion des informations est un ensemble de règles pour un type de contenu. Informations permettent aux organisations de contrôle de stratégies de gestion et suivi des éléments tels que la durée de conservation de contenu ou les actions que les utilisateurs peuvent prendre avec ce contenu. Stratégies de gestion des informations peuvent aider les organisations à se conformer aux réglementations légales ou gouvernementales, ou ils peuvent appliquer simplement des processus d’entreprise interne.
ms.openlocfilehash: 9ec64cd7e015acc6a7d8da324ba18cf74405cc71
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527998"
---
# <a name="introduction-to-information-management-policies"></a>Introduction aux stratégies de gestion des informations

Une stratégie de gestion des informations est un ensemble de règles pour un type de contenu. Informations permettent aux organisations de contrôle de stratégies de gestion et suivi des éléments tels que la durée de conservation de contenu ou les actions que les utilisateurs peuvent prendre avec ce contenu. Stratégies de gestion des informations peuvent aider les organisations à se conformer aux réglementations légales ou gouvernementales, ou ils peuvent appliquer simplement des processus d’entreprise interne. 
  
Par exemple, une organisation qui doit respecter les réglementations gouvernementales exigeant qu’elle démontre « maîtrise » ses rapports financiers peut créer une ou plusieurs informations stratégies de gestion d’audit des actions spécifiques dans la création et processus d’approbation pour tous les documents liés aux archivages financiers.
  
Pour obtenir des informations, voir [créer et appliquer des stratégies de gestion des informations](create-info-mgmt-policies.md).
  
## <a name="features-of-information-management-policies"></a>Fonctionnalités des stratégies de gestion des informations
<a name="__top"> </a>

Il existe quatre catégories principales de fonctionnalités de stratégie prédéfinies que les organisations peuvent utiliser individuellement ou conjointement pour gérer le contenu et les processus. 
  
![Types de stratégies de contenu](media/19fcb8a3-974b-40d3-a13f-b76088d122f8.png)
  
La fonctionnalité de stratégie audit aide les organisations à analyser l’utilisation de leurs systèmes de gestion de contenu à l’enregistrement des événements et les opérations sont effectuées sur des documents et éléments de liste. Vous pouvez configurer la fonctionnalité de stratégie audit pour enregistrer des événements tels que lorsqu’un document ou un élément est modifié, affiché, archivé, extrait, supprimés, ou a la modification des autorisations. Toutes les informations d’audit sont stockées dans un journal d’audit unique sur le serveur et les administrateurs de site peuvent exécuter des rapports sur celui-ci. 
  
La fonctionnalité de stratégie Expiration aide les organisations à supprimer les contenus obsolètes de leurs sites d’une manière cohérente et vérifiable. Cela vous permet de gérer les coûts et les risques liés à la conservation de contenus obsolètes. Vous pouvez configurer une stratégie d’Expiration pour spécifier que certains types de contenus expirent à une date spécifique ou au sein d’un certain temps après que le document a été créé ou modifié.
  
Les organisations peuvent également créer et déployer des fonctionnalités de stratégie personnalisée pour répondre aux besoins spécifiques. Par exemple, une organisation de fabrication souhaiterez définir une stratégie de gestion des informations pour tous les documents de spécification de conception du produit provisoire qui empêche les utilisateurs de l’impression de copies de ces documents sur des imprimantes. Pour définir ce type de stratégie de gestion des informations, vous pouvez créer et déployer une fonctionnalité de stratégie de Restriction d’impression qui peut être ajoutée à la stratégie de gestion des informations pertinentes pour le type de contenu spécification de conception du produit.
  
## <a name="locations-to-use-an-information-management-policy"></a>Emplacements pour utiliser une stratégie de gestion des informations
<a name="__toc340213528"> </a>

Pour implémenter une stratégie de gestion des informations, vous devez l’ajouter à une liste, une bibliothèque ou un type de contenu dans un site. L’emplacement où vous créez ou ajoutez une stratégie de gestion des informations affecte façon générale s’applique la stratégie ou façon générale dont il peut être utilisé. Vous pouvez :
  
 **Créer une stratégie de collection de sites, puis ajoutez cette stratégie à un type de contenu, liste ou une bibliothèque** Vous pouvez créer une stratégie de collection de sites dans la liste de stratégies dans le site de niveau supérieur d’une collection de sites. Après avoir créé une stratégie de collection de sites, vous pouvez l’exporter afin que les administrateurs d’autres collections de sites peuvent importer dans leur liste des stratégies. Création d’une stratégie de collection de sites exportable vous permet de normaliser les stratégies de gestion des informations sur les sites de votre organisation. 
  
Lorsque vous ajoutez une stratégie de collection de sites à un type de contenu de site, et une instance de ce type de contenu de site est ajoutée à une liste ou une bibliothèque, le propriétaire de cette liste ou bibliothèque ne peut pas modifier la stratégie de collection de sites pour la liste ou bibliothèque. Ajout d’une stratégie de collection de sites à un type de contenu de site est un excellent moyen de garantir des stratégies de collections de ce site sont appliquées à chaque niveau de votre hiérarchie de site.
  
![Lien de modèle de stratégie de Type contenu dans la page Paramètres du Site](media/26d3466a-23ec-443f-88f0-2aaff38e992b.png)
  
 **Créer une stratégie de gestion des informations pour un type de contenu de site dans la galerie des types de contenu de Site du site de niveau supérieur et d’ajouter ce type de contenu à une ou plusieurs listes ou bibliothèques** Vous pouvez également créer une stratégie de gestion des informations directement pour un type de contenu de site et puis associer une instance de ce type de contenu de site à plusieurs listes ou bibliothèques. Si vous créez une stratégie de gestion des informations de cette manière, chaque élément dans la collection de sites de ce type de contenu ou un type de contenu qui hérite de ce type de contenu est la stratégie. Toutefois, si vous créez une stratégie de gestion des informations directement pour un type de contenu de site, il est plus difficile à réutiliser cette stratégie de gestion des informations dans d’autres collections de sites, car les stratégies créées de cette manière ne peut pas être exportés. 
  
![Lien de types de contenu de site sur la page Paramètres du Site](media/6f6fa51f-15d7-4782-b06f-a7b36e874cd3.png)
  
![Lien de stratégie de gestion des informations sur la page des paramètres pour un type de contenu de site](media/15d83a34-6c8f-4b6e-b6ee-e9b0a70cbb4b.png)
  
Remarque : pour contrôler les stratégies sont utilisées dans une collection de sites, les administrateurs de collection de sites peuvent désactiver la possibilité de définir des fonctionnalités de stratégie directement sur un type de contenu. Lorsque cette restriction est en vigueur, les utilisateurs qui créent des types de contenu sont limités à sélectionner des stratégies dans la liste de stratégies de collection de sites.
  
 **Créer une stratégie de gestion des informations pour une liste ou une bibliothèque** Si votre organisation a besoin appliquer une stratégie de gestion des informations spécifiques à un ensemble très limité de contenu, vous pouvez créer une stratégie de gestion des informations qui s’applique uniquement à une liste ou bibliothèque particulière. Cette méthode de création d’une stratégie de gestion des informations est la moins flexible, étant donné que la stratégie s’applique uniquement à un seul emplacement et ne peut pas être exportée ou réutilisée pour d’autres emplacements. Toutefois, parfois vous devrez peut-être créer des stratégies de gestion des informations uniques avec application limitée pour traiter les situations spécifiques. 
  
![Lien de stratégies de gestion des informations sur la page Paramètres de la bibliothèque de documents](media/9fa6d366-6aab-49e1-a05c-898ac6f536e6.png)
  
Notes 
  
Vous pouvez créer une stratégie de gestion des informations pour une liste ou une bibliothèque uniquement si cette liste ou bibliothèque ne prend pas en charge plusieurs types de contenu. Si une liste ou une bibliothèque prend en charge plusieurs types de contenu, vous devez définir une stratégie de gestion des informations pour chaque type de contenu de liste qui est associé à cette liste ou bibliothèque. (Les instances d’un type de contenu de site qui sont associés à une liste ou bibliothèque spécifique sont appelées types de contenu de liste.)
  
Pour contrôler les stratégies qui sont utilisées dans une collection de sites, les administrateurs de collection de sites peuvent désactiver la capacité de définir des fonctionnalités de stratégie directement sur une liste ou une bibliothèque. Lorsque cette restriction est en vigueur, les utilisateurs qui gèrent des listes ou bibliothèques sont limitées à sélectionner des stratégies dans la liste de stratégies de collection de sites.
  
[Une stratégie de gestion des informations est un ensemble de règles pour un type de contenu. Informations permettent aux organisations de contrôle de stratégies de gestion et suivi des éléments tels que la durée de conservation de contenu ou les actions que les utilisateurs peuvent prendre avec ce contenu. Stratégies de gestion des informations peuvent aider les organisations à se conformer aux réglementations légales ou gouvernementales, ou ils peuvent appliquer simplement des processus d’entreprise interne. Par exemple, une organisation qui doit respecter les réglementations gouvernementales exigeant qu’elle démontre « maîtrise » ses rapports financiers peut créer une ou plusieurs informations stratégies de gestion d’audit des actions spécifiques dans la création et processus d’approbation pour tous les documents liés aux archivages financiers. Pour obtenir des informations, voir créer et appliquer des stratégies de gestion des informations.](intro-to-info-mgmt-policies.md#__top)
  

