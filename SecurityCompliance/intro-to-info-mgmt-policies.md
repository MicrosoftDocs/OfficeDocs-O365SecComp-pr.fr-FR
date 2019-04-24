---
title: Introduction aux stratégies de gestion des informations
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 5/16/2014
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- WSU150
- SPO160
- OSU150
- MET150
ms.assetid: 63a0b501-ba59-44b7-a35c-999f3be057b2
ms.collection:
- M365-security-compliance
description: Une stratégie de gestion des informations constitue un ensemble de règles pour un type de contenu. Les stratégies de gestion des informations permettent aux organisations de contrôler et de suivre des événements tels que la durée de rétention des contenus ou les actions que les utilisateurs sont autorisés à effectuer sur ces contenus. Les stratégies de gestion des informations peuvent aider les organisations à se conformer aux réglementations légales ou administratives, ou elles peuvent simplement appliquer les processus d’entreprise internes.
ms.openlocfilehash: 23662c555dfc19b2fc83b0364d93724e922c7c97
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32254232"
---
# <a name="introduction-to-information-management-policies"></a>Introduction aux stratégies de gestion des informations

Une stratégie de gestion des informations constitue un ensemble de règles pour un type de contenu. Les stratégies de gestion des informations permettent aux organisations de contrôler et de suivre des événements tels que la durée de rétention des contenus ou les actions que les utilisateurs sont autorisés à effectuer sur ces contenus. Les stratégies de gestion des informations peuvent aider les organisations à se conformer aux réglementations légales ou administratives, ou elles peuvent simplement appliquer les processus d’entreprise internes. 
  
Par exemple, une organisation qui doit suivre des réglementations gouvernementales exigeant qu'elle démontre les «contrôles adéquats» de ses États financiers pourrait créer une ou plusieurs stratégies de gestion des informations qui auditent des actions spécifiques dans la création et processus d'approbation de tous les documents liés aux profils financiers.
  
Pour obtenir des informations sur les procédures, consultez la rubrique [créer et appliquer des stratégies de gestion des informations](create-info-mgmt-policies.md).
  
## <a name="features-of-information-management-policies"></a>Fonctionnalités des stratégies de gestion des informations
<a name="__top"> </a>

Il existe quatre catégories de base de fonctionnalités de stratégie prédéfinies que les organisations peuvent utiliser individuellement ou en combinaison pour gérer le contenu et les processus. 
  
![Types de stratégies de contenu](media/19fcb8a3-974b-40d3-a13f-b76088d122f8.png)
  
La fonctionnalité de stratégie d'audit aide les organisations à analyser le mode d'utilisation de leurs systèmes de gestion de contenu en consignant les événements et les opérations effectuées sur les documents et les éléments de liste. Vous pouvez configurer la fonctionnalité de stratégie d'audit pour enregistrer des événements tels que la modification, l'affichage, l'archivage, la suppression ou la modification des autorisations d'un document ou d'un élément. Toutes les informations d'audit sont stockées dans un journal d'audit unique sur le serveur et les administrateurs de site peuvent y exécuter des rapports. 
  
La fonctionnalité de stratégie d'expiration permet aux organisations de supprimer ou de supprimer du contenu obsolète de leurs sites de façon cohérente et facile à suivre. Cela vous permet de gérer à la fois les coûts et les risques associés à la conservation du contenu obsolète. Vous pouvez configurer une stratégie d'expiration pour spécifier que certains types de contenu expirent à une date donnée ou pendant un laps de temps après la création ou la dernière modification du document.
  
Les organisations peuvent également créer et déployer des fonctionnalités de stratégie personnalisées afin de répondre à des besoins spécifiques. Par exemple, une organisation de fabrication peut souhaiter définir une stratégie de gestion des informations pour tous les projets de spécifications de conception de produits qui empêche les utilisateurs d'imprimer des copies de ces documents sur des imprimantes non sécurisées. Pour définir ce type de stratégie de gestion des informations, vous pouvez créer et déployer une fonctionnalité de stratégie de restriction d'impression pouvant être ajoutée à la stratégie de gestion des informations pertinente pour le type de contenu spécification de conception de produit.
  
## <a name="locations-to-use-an-information-management-policy"></a>Emplacements d'utilisation d'une stratégie de gestion des informations
<a name="__toc340213528"> </a>

Pour implémenter une stratégie de gestion des informations, vous devez l'ajouter à une liste, une bibliothèque ou un type de contenu dans un site. L'emplacement où vous créez ou ajoutez une stratégie de gestion des informations influe sur l'étendue de la stratégie ou sur son utilisation. Vous pouvez :
  
 **Créer une stratégie de collection de sites, puis ajouter cette stratégie à un type de contenu, une liste ou une bibliothèque** Vous pouvez créer une stratégie de collection de sites dans la liste stratégies du site de niveau supérieur d'une collection de sites. Une fois que vous avez créé une stratégie de collection de sites, vous pouvez l'exporter afin que les administrateurs d'autres collections de sites puissent l'importer dans leur liste de stratégies. La création d'une stratégie de collection de sites exportable vous permet de normaliser les stratégies de gestion des informations sur les différents sites de votre organisation. 
  
Lorsque vous ajoutez une stratégie de collection de sites à un type de contenu de site et qu'une instance de ce type de contenu de site est ajoutée à une liste ou une bibliothèque, le propriétaire de cette liste ou bibliothèque ne peut pas modifier la stratégie de collection de sites pour la liste ou la bibliothèque. L'ajout d'une stratégie de collection de sites à un type de contenu de site constitue un moyen efficace pour s'assurer que les stratégies de collection de sites sont appliquées à chaque niveau de la hiérarchie de votre site.
  
![Lien de modèle de stratégie de type de contenu sur la page Paramètres du site](media/26d3466a-23ec-443f-88f0-2aaff38e992b.png)
  
 **Créer une stratégie de gestion des informations pour un type de contenu de site dans la Galerie de types de contenu de site du site de niveau supérieur, puis ajouter ce type de contenu à une ou plusieurs listes ou bibliothèques** Vous pouvez également créer une stratégie de gestion des informations directement pour un type de contenu de site, puis associer une instance de ce type de contenu de site à plusieurs listes ou bibliothèques. Si vous créez une stratégie de gestion des informations de cette façon, chaque élément de la collection de sites de ce type de contenu ou d'un type de contenu qui hérite de ce type de contenu est associé à la stratégie. Toutefois, si vous créez directement une stratégie de gestion des informations pour un type de contenu de site, il est plus difficile de réutiliser cette stratégie de gestion des informations dans d'autres collections de sites, car les stratégies créées de cette manière ne peuvent pas être exportées. 
  
![Lien de types de contenu de site sur la page Paramètres du site](media/6f6fa51f-15d7-4782-b06f-a7b36e874cd3.png)
  
![Lien de stratégie de gestion des informations sur la page des paramètres d'un type de contenu de site](media/15d83a34-6c8f-4b6e-b6ee-e9b0a70cbb4b.png)
  
Remarque pour contrôler les stratégies utilisées dans une collection de sites, les administrateurs de collections de sites peuvent désactiver la possibilité de définir des fonctionnalités de stratégie directement sur un type de contenu. Lorsque cette restriction est appliquée, les utilisateurs qui créent des types de contenu sont limités à la sélection de stratégies dans la liste stratégies de collection de sites.
  
 **Créer une stratégie de gestion des informations pour une liste ou une bibliothèque** Si votre organisation a besoin d'appliquer une stratégie de gestion des informations spécifique à un ensemble très limité de contenu, vous pouvez créer une stratégie de gestion des informations qui s'applique uniquement à une liste ou une bibliothèque individuelle. Cette méthode de création d'une stratégie de gestion des informations est la moins flexible, car la stratégie s'applique uniquement à un seul emplacement, et elle ne peut pas être exportée ou réutilisée pour d'autres emplacements. Toutefois, il se peut que vous deviez parfois créer des stratégies de gestion des informations uniques avec une applicabilité limitée pour résoudre des situations spécifiques. 
  
![Lien stratégies de gestion des informations sur la page Paramètres de la bibliothèque de documents](media/9fa6d366-6aab-49e1-a05c-898ac6f536e6.png)
  
Notes 
  
Vous pouvez créer une stratégie de gestion des informations pour une liste ou une bibliothèque uniquement si cette liste ou bibliothèque ne prend pas en charge plusieurs types de contenu. Si une liste ou une bibliothèque prend en charge plusieurs types de contenu, vous devez définir une stratégie de gestion des informations pour chaque type de contenu de liste individuel associé à cette liste ou bibliothèque. (Les instances d'un type de contenu de site qui sont associées à une liste ou une bibliothèque spécifique sont connues sous le nom de types de contenu de liste.)
  
Pour contrôler les stratégies utilisées dans une collection de sites, les administrateurs de collections de sites peuvent désactiver la possibilité de définir des fonctionnalités de stratégie directement sur une liste ou une bibliothèque. Lorsque cette restriction est appliquée, les utilisateurs qui gèrent des listes ou des bibliothèques se limitent à sélectionner des stratégies dans la liste stratégies de collection de sites.
  
[Une stratégie de gestion des informations est un ensemble de règles pour un type de contenu. Les stratégies de gestion des informations permettent aux organisations de contrôler et de suivre des éléments tels que la durée de conservation du contenu ou les actions que les utilisateurs peuvent effectuer avec ce contenu. Les stratégies de gestion des informations peuvent aider les organisations à se conformer aux réglementations juridiques ou gouvernementales, ou elles peuvent simplement appliquer les processus d'entreprise internes. Par exemple, une organisation qui doit suivre des réglementations gouvernementales exigeant qu'elle démontre les «contrôles adéquats» de ses États financiers pourrait créer une ou plusieurs stratégies de gestion des informations qui auditent des actions spécifiques dans la création et processus d'approbation de tous les documents liés aux profils financiers. Pour obtenir des informations sur les procédures, consultez la rubrique créer et appliquer des stratégies de gestion des informations.](intro-to-info-mgmt-policies.md#__top)
  

