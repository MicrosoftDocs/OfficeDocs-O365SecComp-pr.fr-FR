---
title: Attribuer des autorisations de sécurité Office 365 eDiscovery &amp; centre de conformité
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 5b9a067b-9d2e-4aa5-bb33-99d8c0d0b5d7
description: Assignez les autorisations requises pour effectuer les tâches liées à la découverte électronique à l’aide de la sécurité &amp; centre de conformité.
ms.openlocfilehash: 95f0ed171c37ec84ca8bb8f00e69ab0318cd31cd
ms.sourcegitcommit: a64af0ebd0b03e4a5e60a33e9108c44c7d74f356
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2019
ms.locfileid: "29741157"
---
# <a name="assign-ediscovery-permissions-in-the-office-365-security-amp-compliance-center"></a>Attribuer des autorisations de sécurité Office 365 eDiscovery &amp; centre de conformité

Si vous souhaitez que les personnes susceptibles d’utiliser les outils liés à la découverte de sécurité Office 365 &amp; centre de conformité, vous devez attribuer les autorisations appropriées. Le moyen le plus simple consiste à ajouter cette personne le groupe de rôles appropriée dans la page **autorisations** de sécurité Office 365 &amp; centre de conformité. Cette rubrique décrit les autorisations requises pour effectuer des tâches liées à la découverte électronique à l’aide de la sécurité &amp; centre de conformité. 
  
Le groupe de rôles de liés à la découverte électronique principale de la sécurité &amp; centre de conformité est appelé **gestionnaire eDiscovery**. Il existe deux sous-groupes de ce groupe de rôles. 
  
- **gestionnaires de découverte électronique** - un gestionnaire eDiscovery permet l’outil de recherche de contenu dans la sécurité &amp; centre de conformité pour rechercher les emplacements de contenu dans l’organisation et d’effectuer diverses actions liées à la recherche comme aperçu et d’exportation de recherche résultats. Membres peuvent également créer et gérer des affaires eDiscovery, ajouter et supprimer des membres à un cas, créer des suspensions cas et exécuter des recherches de contenu associés à un cas et accès aux données cas eDiscovery Office 365 avancés.  Une gestionnaires de découverte électronique peut accéder uniquement au et gérer les cas qu’ils créent. Ils ne peuvent pas accéder ou gérer les dossiers créés par les autres gestionnaires de découverte électronique. 
    
- **eDiscovery administrateurs** - une administrateur eDiscovery est un membre du groupe de rôles gestionnaire eDiscovery et peut effectuer la même recherche de contenu et tâches associées à la gestion cas capable d’effectuer un gestionnaire eDiscovery. En outre, une administrateur de découverte électronique peut : 
    
  - Accéder à tous les cas qui sont répertoriés dans la page **cas eDiscovery** dans la sécurité &amp; centre de conformité. 

  - Accédez aux données cas d’eDiscovery avancée pour tous les cas dans l’organisation.
    
  - Gérer les cas de découverte électronique après s’être ajouté en tant que membre du cas.
  
  Pour des raisons de pourquoi vous souhaiterez administrateurs eDiscovery dans votre organisation, voir la section [plus d’informations](#more-information) . 

> [!NOTE]
> Pour analyser les données d’un utilisateur à l’aide de la découverte électronique avancée, l’utilisateur (le dépositaire des données) doit être affecté à une licence Office 365 E5. Autrement, les utilisateurs possédant une licence Office 365 E1 ou E3 peuvent être affectés à une licence autonome de découverte avancée. Les administrateurs et des agents de conformité qui sont affectées à des cas et utilisent eDiscovery avancée pour analyser des données inutile d’une licence E5.  
  
## <a name="before-you-begin"></a>Avant de commencer

- Vous devez être membre du groupe de rôles de gestion de l’organisation (ou attribuer le rôle de gestion des rôles) pour attribuer des autorisations de découverte électronique dans la sécurité &amp; centre de conformité.
    
- Vous pouvez utiliser l’applet de commande [Add-RoleGroupMember](https://technet.microsoft.com/en-us/library/dd638207%28v=exchg.160%29.aspx) de la sécurité &amp; PowerShell du centre de conformité pour ajouter un groupe de sécurité à extension messagerie en tant que membre de la sous-groupes de responsables de découverte électronique dans le groupe de rôles de gestionnaire de découverte électronique. Toutefois, vous ne pouvez pas ajouter un groupe de sécurité à extension messagerie au sous-groupe Administrateurs eDiscovery. Voir la section [plus d’informations](#more-information) pour plus d’informations. 
    
## <a name="assign-ediscovery-permissions-in-the-security-amp-compliance-center"></a>Attribution d’autorisations de découverte électronique dans la sécurité &amp; centre de conformité

1. Accédez à la page [https://protection.office.com](https://protection.office.com).
    
2. Connectez-vous à Office 365 à l'aide de votre compte scolaire ou professionnel.
    
3. Dans le volet gauche de la sécurité &amp; centre de conformité, cliquez sur **autorisations**, puis cliquez sur la case à cocher en regard de **gestionnaire eDiscovery**.
    
4. Dans la page flottant **gestionnaire eDiscovery** , effectuez l’une des opérations suivantes en fonction des autorisations de découverte électronique que vous souhaitez affecter. 
    
  - **Pour rendre un utilisateur un gestionnaire eDiscovery** En regard **Gestionnaire de découverte électronique**, cliquez sur **Modifier**. Sous **Selected eDiscovery responsables**, cliquez sur **Modifier**, puis cliquez sur ![ajouter une icône](media/ITPro-EAC-AddIcon.gif) **Ajouter**. Sélectionnez l’utilisateur (ou utilisateurs) vous souhaitez ajouter un administrateur de découverte électronique, puis cliquez sur **Ajouter**. Lorsque vous avez terminé d’ajouter des utilisateurs, cliquez sur **terminé**. Dans la page flottant **gestionnaire eDiscovery Choisissez Modification** , cliquez sur **Enregistrer** pour enregistrer les modifications apportées à l’appartenance au gestionnaire eDiscovery. 
    
  - **Pour rendre un utilisateur à une administrateur d’eDiscovery** En regard **découverte électronique administrateur**, cliquez sur **Modifier**. Sous **Selected eDiscovery administrateurs**, cliquez sur **Modifier**, puis cliquez sur ![ajouter une icône](media/ITPro-EAC-AddIcon.gif) **Ajouter**. Sélectionnez l’utilisateur (ou utilisateurs) vous souhaitez ajouter en tant qu’une administrateur de découverte électronique, puis cliquez sur **Ajouter**. Lorsque vous avez terminé d’ajouter des utilisateurs, cliquez sur **terminé**. Dans la page flottant **eDiscovery modification Sélectionnez Administrateur** , cliquez sur **Enregistrer** pour enregistrer les modifications apportées à l’appartenance au groupe Administrateurs de découverte électronique. 
    
> [!NOTE]
> Vous pouvez également utiliser l’applet de commande **Add-eDiscoveryCaseAdmin** pour rendre un utilisateur à une administrateur de découverte électronique. Toutefois, l’utilisateur doit être affecté le rôle de gestion des cas avant de pouvoir utiliser cette applet de commande pour les rendre une administrateur eDiscovery. Pour plus d’informations, voir [Add-eDiscoveryCaseAdmin](https://go.microsoft.com/fwlink/p/?LinkID=798217). 
  
Dans la page **autorisations** de sécurité &amp; centre de conformité, vous pouvez également affecter les utilisateurs aux autorisations liées à la découverte électronique, en les ajoutant aux groupes de rôles d’administrateur de conformité, gestion de l’organisation et réviseur. Pour obtenir une description des liés à la découverte électronique rôles RBAC assignés à chacun de ces groupes de rôles, consultez la section [rôles RBAC liées à la découverte électronique](#rbac-roles-related-to-ediscovery) . 

## <a name="rbac-roles-related-to-ediscovery"></a>Rôles RBAC associés à la découverte électronique

Le tableau suivant répertorie les rôles RBAC liés à la découverte électronique dans le centre de conformité de & sécurité et indique les groupes de rôles intégrés affecté à chaque rôle par défaut. 
    
|**Rôle**|**Administrateur de conformité**|**Administrateur & Gestionnaire de découverte électronique**|**Gestion de l'organisation**|**Relecteur**|
|:-----|:-----:|:-----:|:-----:|:-----:|
|Gestion des incidents <br/> |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> |
|Recherche de conformité <br/> |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> |
|Exporter <br/> | <br/> |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> | <br/> |
|Conservation <br/>  |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> |
|Aperçu <br/>  | <br/> |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> | <br/> |
|Révision  <br/>  | <br/> |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |
|Déchiffrement RMS <br/>  ||![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |||
|Recherche et Purge <br/> | <br/> | <br/> |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> | <br/> | 
||||
  
Les sections suivantes décrivent chacune des rôles RBAC liés à la découverte électronique répertoriés dans le tableau précédent.

### <a name="case-management"></a>Gestion des incidents

Ce rôle permet aux utilisateurs de créer, modifier, supprimer et contrôler l’accès aux cas eDiscovery dans le centre de conformité de & sécurité. Pour plus d’informations, voir [gérer des affaires eDiscovery de sécurité Office 365 &amp; centre de conformité](manage-ediscovery-cases.md). Comme expliqué précédemment, un utilisateur doit être affecté le rôle de gestion des cas avant de pouvoir utiliser l’applet de commande **Add-eDiscoveryCaseAdmin** pour les rendre une administrateur eDiscovery. 

### <a name="compliance-search"></a>Recherche de conformité

Ce rôle permet aux utilisateurs d’exécuter l’outil de recherche de contenu dans le centre de conformité pour rechercher les boîtes aux lettres et de dossiers publics, des sites SharePoint Online, OneDrive pour les sites de l’entreprise, Skype pour Business conversations Office 365 et groupes Microsoft Teams de & sécurité. Ce rôle permet à un utilisateur obtenir une estimation des résultats de recherche et de création de rapports d’exportation, mais des rôles supplémentaires sont nécessaires pour lancer des opérations de recherche de contenu telles que l’aperçu, l’exportation ou la suppression des résultats de la recherche.

Notez que les utilisateurs d’attribuer le rôle de recherche de la conformité, mais n’ont pas le rôle de l’aperçu peut afficher un aperçu les résultats d’une recherche dans laquelle l’action d’aperçu a été initiée par un utilisateur qui dispose du rôle d’aperçu. L’utilisateur sans le rôle Preview pouvez afficher un aperçu des résultats pour jusqu'à 2 semaines après que l’action d’aperçu initiale a été créée.

De même, les utilisateurs d’attribuer le rôle de recherche de la conformité, mais n’avez pas l’exportation de rôle peut télécharger les résultats d’une recherche dans laquelle l’action de l’exportation a lancé par un utilisateur qui dispose du rôle d’exportation. L’utilisateur sans le rôle d’exportation peut télécharger les résultats d’une recherche de deux semaines après que l’action d’exportation initiale a été créée. Après cela, ils ne pourront pas télécharger les résultats à moins que toute personne disposant du rôle d’exportation redémarre l’exportation.

Pour plus d’informations, voir [Recherche de contenu dans Office 365](content-search.md). 

### <a name="export"></a>Exporter

Le rôle permet aux utilisateurs d’exporter les résultats d’une recherche de contenu sur un ordinateur local. Elle leur permet également de préparer les résultats de la recherche pour l’analyse d’eDiscovery avancée. 

Pour plus d’informations sur l’exportation de résultats de recherche, voir [exportation de résultats de recherche provenant du & Office 365 sécurité Centre de conformité](export-search-results.md).

### <a name="hold"></a>Conservation

Ce rôle permet aux utilisateurs de placer le contenu dans les boîtes aux lettres, les dossiers publics, les sites, Skype pour des conversations, et maintenez les groupes dans Office 365. Lorsque le contenu est en attente, les propriétaires de contenu sera en mesure de modifier ou supprimer le contenu d’origine, mais le contenu sera conservé jusqu'à ce que le blocage est supprimé ou jusqu'à ce que la durée d’attente expire. 

Pour plus d’informations sur les blocages, voir :

- [cas eDiscovery dans le centre de conformité de & sécurité pour Microsoft Office 365](ediscovery-cases.md) 
- [Vue d’ensemble des stratégies de rétention](retention-policies.md)

### <a name="preview"></a>Aperçu

Ce rôle permet aux utilisateurs d’afficher une liste d’éléments qui ont été retournés à partir d’une recherche de contenu. Ils pourrez également ouvrir et afficher chaque élément dans la liste pour afficher son contenu.

### <a name="review"></a>Révision 

Ce rôle permet aux utilisateurs d’accéder aux données cas dans Office 365 avancée de découverte électronique. Le principal objectif de ce rôle consiste à donner aux utilisateurs l’accès à la découverte électronique avancée. Les utilisateurs qui sont affectés à ce rôle peuvent voir et ouvrir la liste des incidents dans la page de découverte électronique dans le & de sécurité Centre de conformité qui ils sont membres de. Une fois que l’utilisateur accède à un cas dans le centre de conformité de & sécurité, ils peuvent cliquer sur **commutateur eDiscovery avancé** pour accéder et analyser les données de cas de découverte avancée. Ce rôle n’autorise l’utilisateur à afficher les résultats d’une recherche de contenu associé à la casse ou effectuer d’autres recherche de contenu ou des tâches de gestion.

### <a name="rms-decrypt"></a>Déchiffrement RMS

Ce rôle permet d’utilisateurs decrypt chiffrés RMS des messages électroniques lors de l’exportation de recherche résultats ou la préparation des résultats de recherche pour l’analyse d’eDiscovery avancée. Pour plus d’informations sur le déchiffrement pendant l’exportation des résultats de recherche, voir [exportation de résultats de recherche provenant du & Office 365 sécurité Centre de conformité](export-search-results.md).

### <a name="search-and-purge"></a>Recherche et Purge

Ce rôle permet aux utilisateurs d’effectuer suppression en bloc de données répondant aux critères d’une recherche de contenu. Pour plus d’informations, voir [Rechercher et supprimer des messages électroniques dans votre organisation Office 365](search-for-and-delete-messages-in-your-organization.md). 


## <a name="more-information"></a>Plus d’informations

- **Pourquoi créer une administrateur de découverte électronique ?** Comme expliqué, une découverte électronique que l’administrateur est membre du groupe de rôles gestionnaire eDiscovery qui peut afficher et accéder à tous les cas de découverte électronique dans votre organisation. Cette capacité à accéder à tous les cas eDiscovery a deux fonctions importantes : 
    
  - Si une personne qui est le seul membre d’un cas eDiscovery quitte l’organisation, personne (y compris les membres du groupe de rôles de gestion de l’organisation ou un autre membre du groupe de rôles de gestionnaire de découverte électronique) peuvent accéder à ce cas de découverte électronique car ils ne sont pas un membre d’un cas. Dans ce cas, il n’y aura aucun moyen d’accéder aux données dans le cas. Mais comme une administrateur de découverte électronique peut accéder à tous les cas de découverte électronique dans l’organisation, ils peuvent afficher le cas dans la sécurité &amp; centre de conformité et l’ajouter eux-mêmes ou un autre gestionnaire de découverte électronique en tant que membre de la casse.
    
  - Car une administrateur de découverte électronique peut afficher et accéder à tous les cas eDiscovery, qu’ils puissent d’audit et surveiller tous les cas et les recherches de conformité. Cela peut aider à empêcher toute utilisation incorrecte de recherches de conformité ou cas eDiscovery. Et car eDiscovery, les administrateurs permettre accéder à des informations sensibles dans les résultats d’une recherche de conformité, vous devez limiter le nombre de personnes qui sont des administrateurs de découverte électronique.
    
    En outre, eDiscovery les administrateurs de la sécurité &amp; centre de conformité sont automatiquement ajoutés en tant qu’administrateurs d’eDiscovery avancée. Cela signifie qu'une personne doit être une administrateur pour effectuer des tâches administratives dans eDiscovery avancée, telles que la configuration des utilisateurs, la création des cas et importation de données dans un cas eDiscovery.
    
- **Puis-je ajouter un groupe en tant que membre du groupe de rôles eDiscovery responsable de la sécurité &amp; centre de conformité ?** Expliqué précédemment, vous pouvez ajouter un groupe de sécurité à extension messagerie en tant que membre de la sous-groupes de responsables de découverte électronique dans le groupe de rôles de gestionnaire de découverte électronique à l’aide de la sécurité de l’applet de commande **Add-RoleGroupMember** &amp; PowerShell du centre de conformité. Par exemple, vous pouvez exécuter la commande suivante pour ajouter un groupe de sécurité à extension messagerie pour le groupe de rôles de gestionnaire de découverte électronique. 
    
  ```
  Add-RoleGroupMember "eDiscovery Manager" -Member <name of security group>
  ```

    Notez qu’un groupe de distribution Exchange ou un groupe d’Office 365 ne sont pas pris en charge. Vous devez utiliser un groupe de sécurité à extension messagerie, vous pouvez créer dans Exchange Online PowerShell à l’aide de la ` New-DistributionGroup -Type Security ` commande. Vous pouvez également créer un groupe de sécurité à extension messagerie (et ajouter des membres) dans le centre d’administration Exchange ou dans le centre d’administration d’Office 365. Notez qu’il peut prendre jusqu'à 60 minutes après que l’avoir créé pour une nouvelle sécurité à extension messagerie être ajoutés au groupe de rôles responsables eDiscovery. 
    
    Également comme indiqué plus haut, vous ne pouvez apporter une sécurité à extension messagerie une administrateur de la découverte de groupe à l’aide de la sécurité de l’applet de commande **Add-eDiscoveryCaseAdmin** &amp; PowerShell du centre de conformité. Vous ne pouvez ajouter des utilisateurs individuels en tant qu’administrateurs de découverte électronique. 
    
    Notez que vous également ne peut pas ajouter un groupe de sécurité à extension messagerie en tant que membre d’un cas.
