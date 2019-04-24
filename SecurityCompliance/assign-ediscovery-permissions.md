---
title: Attribuer des autorisations eDiscovery dans le centre de sécurité & Compliance Center
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 5b9a067b-9d2e-4aa5-bb33-99d8c0d0b5d7
description: Affecter les autorisations requises pour effectuer des tâches liées à la découverte électronique à l'aide du centre de sécurité & Compliance Center.
ms.openlocfilehash: 958dd3f41bb9e578c80608d738fc735f5063148d
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32250168"
---
# <a name="assign-ediscovery-permissions-in-the-security--compliance-center"></a>Attribuer des autorisations eDiscovery dans le centre de sécurité & Compliance Center

Si vous souhaitez que les utilisateurs puissent utiliser l'un des outils de découverte électronique dans le centre de sécurité & Compliance Center dans Office 365, vous devez leur attribuer les autorisations appropriées. La manière la plus simple de procéder consiste à ajouter la personne au groupe de rôles approprié sur la page des **autorisations** dans le centre de sécurité _AMP_ Compliance Center. Cette rubrique décrit les autorisations requises pour effectuer des tâches de recherche de contenu et de découverte électronique à l'aide du centre de sécurité & Compliance Center. 
  
Le groupe de rôles de découverte électronique principal dans le centre de sécurité & Compliance Center est appelé **Gestionnaire eDiscovery**. Il existe deux sous-groupes dans ce groupe de rôles. 
  
- **gestionnaires eDiscovery** : un gestionnaire eDiscovery peut utiliser l'outil de recherche de contenu dans le centre de sécurité _AMP_ Compliance Center pour rechercher des emplacements de contenu dans l'organisation et effectuer diverses actions liées à la recherche, telles que l'aperçu et l'exportation des résultats de recherche. Les membres peuvent également créer et gérer des cas de découverte électronique, ajouter et supprimer des membres à un cas, créer des suspensions de cas, et exécuter des recherches de contenu associées à un cas, et accéder à des données de cas dans Office 365 Advanced eDiscovery.  Les gestionnaires eDiscovery peuvent uniquement accéder aux incidents qu'ils créent et les gérer. Ils ne peuvent pas accéder aux dossiers créés par d'autres gestionnaires eDiscovery ni les gérer. 
    
- **administrateurs eDiscovery** : un administrateur eDiscovery est membre du groupe de rôles gestionnaire eDiscovery et peut effectuer la même recherche de contenu et les mêmes tâches liées à la gestion des cas qu'un gestionnaire eDiscovery peut effectuer. De plus, un administrateur de découverte électronique peut : 
    
  - Accédez à tous les cas répertoriés sur la page **cas eDiscovery** dans le centre de sécurité _AMP_ Compliance Center. 

  - Accéder aux données de cas dans Advanced eDiscovery pour tous les cas de l'organisation.
    
  - Gérer les cas de découverte électronique après s’être ajouté en tant que membre du cas.
  
  Consultez la section [plus d'informations](#more-information) pour connaître les raisons pour lesquelles vous pouvez souhaiter des administrateurs de découverte électronique dans votre organisation. 

> [!NOTE]
> Pour analyser les données d'un utilisateur à l'aide de Advanced eDiscovery, l'utilisateur (le dépositaire des données) doit disposer d'une licence Office 365 E5. Par ailleurs, les utilisateurs disposant d'une licence Office 365 E1 ou E3 peuvent se voir attribuer une licence avancée eDiscovery autonome. Les administrateurs et les responsables de la mise en conformité qui sont affectés à des cas et utilisent Advanced eDiscovery pour analyser les données n'ont pas besoin d'une licence E5.  
  
## <a name="before-you-begin"></a>Avant de commencer

- Vous devez être membre du groupe de rôles gestion de l'organisation (ou disposer du rôle de gestion des rôles) pour attribuer des autorisations eDiscovery dans le centre de sécurité & Compliance Center.
    
- Vous pouvez utiliser l'applet de commande [Add-RoleGroupMember](https://technet.microsoft.com/en-us/library/dd638207%28v=exchg.160%29.aspx) dans le centre de sécurité _AMP_ Compliance Center PowerShell pour ajouter un groupe de sécurité à extension messagerie en tant que membre du sous-groupe gestionnaires eDiscovery dans le groupe de rôles gestionnaire de découverte électronique. Toutefois, vous ne pouvez pas ajouter un groupe de sécurité à extension messagerie au sous-groupe administrateurs eDiscovery. Pour plus d'informations, rePortez-vous à la section [more information](#more-information) . 
    
## <a name="assign-ediscovery-permissions-in-the-security--compliance-center"></a>Attribuer des autorisations eDiscovery dans le centre de sécurité & Compliance Center

1. Accédez à la page [https://protection.office.com](https://protection.office.com).
    
2. Connectez-vous à Office 365 à l'aide de votre compte scolaire ou professionnel.
    
3. Dans le volet gauche du centre de sécurité et conformité, cliquez sur **autorisations**, puis cliquez sur la case à cocher en regard de **Gestionnaire eDiscovery**.
    
4. Sur la page de menu volant du **Gestionnaire eDiscovery** , effectuez l'une des opérations suivantes en fonction des autorisations de découverte électronique que vous souhaitez attribuer. 
    
  - **Pour faire d'un utilisateur un gestionnaire eDiscovery** En regard de **Gestionnaire eDiscovery**, cliquez sur **modifier**. Sous **gestionnaires eDiscovery sélectionnés**, cliquez sur **modifier**, puis sur ![ajouter une](media/ITPro-EAC-AddIcon.gif) icône **Ajouter**. Sélectionnez l'utilisateur (ou les utilisateurs) que vous souhaitez ajouter en tant que gestionnaire eDiscovery, puis cliquez sur **Ajouter**. Lorsque vous avez terminé d'ajouter des utilisateurs, cliquez sur **terminé**. Ensuite, dans la page d'édition choisir le menu volant du **Gestionnaire eDiscovery** , cliquez sur **Enregistrer** pour enregistrer les modifications apportées à l'appartenance au gestionnaire eDiscovery. 
    
  - **Pour faire d'un utilisateur un administrateur de découverte électronique** En regard de l' **administrateur de découverte électronique**, cliquez sur **modifier**. Sous **administrateurs eDiscovery sélectionnés**, cliquez sur **modifier**, puis sur ![ajouter une](media/ITPro-EAC-AddIcon.gif) icône **Ajouter**. Sélectionnez l'utilisateur (ou les utilisateurs) que vous souhaitez ajouter en tant qu'administrateur de découverte électronique, puis cliquez sur **Ajouter**. Lorsque vous avez terminé d'ajouter des utilisateurs, cliquez sur **terminé**. Ensuite, dans la page d'édition choisir le menu volant **administrateur eDiscovery** , cliquez sur **Enregistrer** pour enregistrer les modifications apportées à l'appartenance de l'administrateur de découverte électronique. 
    
> [!NOTE]
> Vous pouvez également utiliser l'applet de commande **Add-eDiscoveryCaseAdmin** pour faire d'un utilisateur un administrateur de découverte électronique. Toutefois, l'utilisateur doit se voir attribuer le rôle de gestion des cas avant de pouvoir utiliser cette applet de commande pour en faire un administrateur eDiscovery. Pour plus d'informations, voir [Add-eDiscoveryCaseAdmin](https://go.microsoft.com/fwlink/p/?LinkID=798217). 
  
Sur la page **autorisations** du centre de sécurité et de conformité &, vous pouvez également attribuer des autorisations liées à la découverte électronique aux utilisateurs en les ajoutant aux groupes de rôles Administrateur de conformité, gestion de l'organisation et réviseur. Pour obtenir une description des rôles RBAC liés à la découverte électronique affectés à chacun de ces groupes de rôles, consultez la section [rôles RBAC liés à eDiscovery](#rbac-roles-related-to-ediscovery) . 

## <a name="rbac-roles-related-to-ediscovery"></a>Rôles RBAC liés à eDiscovery

Le tableau suivant répertorie les rôles RBAC liés à la découverte électronique dans le centre de sécurité & Compliance Center et indique les groupes de rôles intégrés auxquels chaque rôle est affecté par défaut. 
    
|**Role**|**Administrateur de conformité**|**Administrateur & du gestionnaire eDiscovery**|**Gestion de l'organisation**|**Relecteur**|
|:-----|:-----:|:-----:|:-----:|:-----:|
|Gestion des cas <br/> |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> |
|Recherche de conformité <br/> |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> |
|Exporter <br/> | <br/> |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> | <br/> |
|Placer <br/>  |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> |
|Aperçu <br/>  | <br/> |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> | <br/> |
|Révision <br/>  | <br/> |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |
|DéChiffrement RMS <br/>  ||![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |||
|Recherche et purge <br/> | <br/> | <br/> |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> | <br/> | 
||||
  
Les sections suivantes décrivent chacun des rôles RBAC liés à la découverte électronique figurant dans le tableau précédent.

### <a name="case-management"></a>Gestion des cas

Ce rôle permet aux utilisateurs de créer, de modifier, de supprimer et de contrôler l'accès aux cas eDiscovery dans le centre de sécurité & Compliance Center. Pour plus d'informations, consultez [la rubrique Manage eDiscovery cases dans le centre de sécurité _AMP_ Compliance Center](manage-ediscovery-cases.md). Comme expliqué précédemment, un utilisateur doit se voir attribuer le rôle de gestion des cas avant de pouvoir utiliser l'applet de commande **Add-eDiscoveryCaseAdmin** pour en faire un administrateur eDiscovery. 

### <a name="compliance-search"></a>Recherche de conformité

Ce rôle permet aux utilisateurs d'exécuter l'outil de recherche de contenu dans le centre de sécurité & Compliance Center pour rechercher des boîtes aux lettres et des dossiers publics, des sites SharePoint Online, des sites OneDrive entreprise, des conversations Skype entreprise, des groupes Office 365 et Microsoft Teams. Ce rôle permet à un utilisateur d'obtenir une estimation des résultats de la recherche et de créer des rapports d'exportation, mais des rôles supplémentaires sont nécessaires pour lancer des actions de recherche de contenu telles que l'aperçu, l'exportation ou la suppression de résultats de recherche.

Notez que les utilisateurs qui ont attribué le rôle de recherche de conformité mais n'ont pas le rôle Aperçu peuvent prévisualiser les résultats d'une recherche dans laquelle l'action d'aperçu a été initiée par un utilisateur auquel le rôle aperçu a été attribué. L'utilisateur sans rôle d'aperçu peut prévisualiser les résultats pendant 2 semaines au maximum après la création de l'action d'évaluation initiale.

De même, les utilisateurs ayant attribué le rôle de recherche de conformité mais ne disposent pas du rôle d'exportation peuvent télécharger les résultats d'une recherche dans laquelle l'action d'exportation a commencé par un utilisateur auquel le rôle d'exportation est attribué. L'utilisateur sans rôle d'exportation peut télécharger les résultats d'une recherche pendant 2 semaines au maximum après la création de l'action d'exportation initiale. Après qu'ils ne pourront pas télécharger les résultats, sauf si une personne disposant du rôle d'exportation redémarre l'exportation.

Pour plus d'informations, consultez la rubrique [recherche de contenu dans Office 365](content-search.md). 

### <a name="export"></a>Exporter

Le rôle permet aux utilisateurs d'exporter les résultats d'une recherche de contenu sur un ordinateur local. Elle leur permet également de préparer des résultats de recherche pour analyse dans Advanced eDiscovery. 

Pour plus d'informations sur l'exportation des résultats de recherche, voir [Export Search Results from Security _AMP_ Compliance Center](export-search-results.md).

### <a name="hold"></a>Placer

Ce rôle permet aux utilisateurs de placer du contenu dans des boîtes aux lettres, des dossiers publics, des sites, des conversations Skype entreprise et des groupes Office 365 en conservation. Lorsque le contenu est en conservation, les propriétaires de contenu peuvent toujours modifier ou supprimer le contenu d'origine, mais le contenu est conservé jusqu'à ce que la conservation soit supprimée ou jusqu'à l'expiration de la durée de la conservation. 

Pour plus d'informations sur les suspensions, voir:

- [cas eDiscovery](ediscovery-cases.md) 
- [Vue d’ensemble des stratégies de rétention](retention-policies.md)

### <a name="preview"></a>Aperçu

Ce rôle permet aux utilisateurs d'afficher la liste des éléments renvoyés à partir d'une recherche de contenu. Ils peuvent également ouvrir et afficher chaque élément de la liste pour afficher son contenu.

### <a name="review"></a>Révision

Ce rôle permet aux utilisateurs d'accéder aux données de cas dans Office 365 Advanced eDiscovery. L'objectif principal de ce rôle est de permettre aux utilisateurs d'accéder à la découverte électronique avancée. Les utilisateurs auxquels ce rôle est attribué peuvent afficher et ouvrir la liste des incidents sur la page de découverte électronique dans le centre de sécurité & conformité dont ils sont membres. Une fois que l'utilisateur accède à un cas dans le centre de sécurité & Compliance Center, il peut cliquer sur **basculer vers Advanced eDiscovery** pour accéder aux données de cas et les analyser dans Advanced eDiscovery. Ce rôle ne permet pas à l'utilisateur d'afficher un aperçu des résultats d'une recherche de contenu associée à l'incident ou d'effectuer d'autres tâches de recherche de contenu ou de gestion des dossiers.

### <a name="rms-decrypt"></a>DéChiffrement RMS

Ce rôle permet aux utilisateurs de déchiffrer des messages électroniques chiffrés RMS lors de l'exportation des résultats de recherche ou de la préparation des résultats de recherche pour analyse dans Advanced eDiscovery. Pour plus d'informations sur le déchiffrement des résultats de recherche lors de l'exportation, voir [Export content Search Results](export-search-results.md).

### <a name="search-and-purge"></a>Recherche et purge

Ce rôle permet aux utilisateurs de procéder à la suppression en bloc des données correspondant aux critères d'une recherche de contenu. Pour plus d'informations, consultez [la rubrique Rechercher et supprimer des messages électroniques dans votre organisation Office 365](search-for-and-delete-messages-in-your-organization.md). 


## <a name="more-information"></a>Plus d’informations

- **Pourquoi créer un administrateur de découverte électronique ?** Comme indiqué précédemment, un administrateur de découverte électronique est membre du groupe de rôles de gestionnaire de découverte électronique, qui peut afficher tous les cas de découverte électronique, et y accéder, de votre organisation. Cette capacité d’accès à tous les cas de découverte électronique a deux objectifs importants : 
    
  - Si une personne qui est le seul membre d’un cas de découverte électronique quitte votre organisation, personne (y compris les membres du groupe de rôles de gestion de l’organisation ou un autre membre du groupe de rôles de gestionnaire de découverte électronique) ne peut accéder à ce cas, car personne n’en est alors membre. Dans ce cas, il n’y aurait aucun moyen d’accéder aux données dans le cas. Toutefois, étant donné qu'un administrateur de découverte électronique peut accéder à tous les cas eDiscovery au sein de l'organisation, il peut afficher le cas et s'ajouter eux-mêmes ou un autre gestionnaire eDiscovery en tant que membre du cas.
    
  - Étant donné qu'un administrateur de découverte électronique peut afficher et accéder à tous les cas eDiscovery, ils peuvent auditer et superviser tous les cas et les recherches de conformité associées. Cela peut vous aider à éviter toute utilisation abusive de recherches de conformité ou de cas de découverte électronique. Étant donné que les administrateurs eDiscovery peuvent accéder à des informations potentiellement sensibles dans les résultats d'une recherche de conformité, vous devez limiter le nombre de personnes qui sont des administrateurs eDiscovery.
    
    En outre, les administrateurs eDiscovery sont automatiquement ajoutés en tant qu'administrateurs dans Advanced eDiscovery. Cela signifie qu'une personne doit être un administrateur eDiscovery pour effectuer des tâches administratives dans Advanced eDiscovery, telles que la configuration des utilisateurs, la création de cas et l'importation de données dans un cas.
    
- **Puis-je ajouter un groupe en tant que membre du groupe de rôles gestionnaire eDiscovery?** Comme expliqué précédemment, vous pouvez ajouter un groupe de sécurité à extension messagerie en tant que membre du sous-groupe gestionnaires eDiscovery dans le groupe de rôles gestionnaire de découverte électronique à l'aide de la cmdlet **Add-RoleGroupMember** dans le centre de sécurité _AMP_ Compliance Center PowerShell. Par exemple, vous pouvez exécuter la commande suivante pour ajouter un groupe de sécurité à extension messagerie au groupe de rôles gestionnaire eDiscovery. 
    
  ```
  Add-RoleGroupMember "eDiscovery Manager" -Member <name of security group>
  ```

    Notez qu'un groupe de distribution Exchange ou un groupe Office 365 ne sont pas pris en charge. Vous devez utiliser un groupe de sécurité à extension messagerie, que vous pouvez créer dans Exchange Online PowerShell à l' ` New-DistributionGroup -Type Security ` aide de la commande. Vous pouvez également créer un groupe de sécurité à extension messagerie (et ajouter des membres) dans le centre d'administration Exchange ou dans le centre d'administration Microsoft 365. Notez que vous pouvez prendre jusqu'à 60 minutes après sa création pour qu'une nouvelle sécurité à extension messagerie soit disponible pour l'ajouter au groupe de rôles gestionnaires eDiscovery. 
    
    Comme indiqué précédemment, vous ne pouvez pas faire d'un groupe de sécurité à extension messagerie un administrateur de découverte électronique à l'aide de la cmdlet **Add-eDiscoveryCaseAdmin** dans le centre de sécurité _AMP_ Compliance Center PowerShell. Vous pouvez uniquement ajouter des utilisateurs individuels en tant qu'administrateurs eDiscovery. 
    
    Notez que vous ne pouvez pas non plus ajouter un groupe de sécurité à extension messagerie en tant que membre d'un cas.
