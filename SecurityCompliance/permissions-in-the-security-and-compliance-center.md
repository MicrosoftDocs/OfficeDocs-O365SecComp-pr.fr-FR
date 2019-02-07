---
title: Autorisations de sécurité Office 365 &amp; centre de conformité
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: overview
f1_keywords:
- ms.o365.cc.AdminRoleGroups
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: d10608af-7934-490a-818e-e68f17d0e9c1
description: L’Office 365 Security &amp; centre de conformité permet d’octroyer des autorisations à des personnes qui effectuent des tâches de conformité telles que la gestion des périphériques, data loss prevention, eDiscovery, rétention et ainsi de suite. Ces personnes peuvent effectuer uniquement les tâches que vous leur accordez explicitement l’accès à. Pour accéder à la sécurité &amp; centre de conformité, les utilisateurs doivent être un administrateur global d’Office 365 ou un membre de la sécurité d’un ou plusieurs &amp; groupes de rôles de centre de conformité.
ms.openlocfilehash: ef281ca7cda706ff78fbf1a5584674cdf41e9025
ms.sourcegitcommit: a64af0ebd0b03e4a5e60a33e9108c44c7d74f356
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2019
ms.locfileid: "29741057"
---
# <a name="permissions-in-the-office-365-security-amp-compliance-center"></a>Autorisations de sécurité Office 365 &amp; centre de conformité

L’Office 365 Security &amp; centre de conformité permet d’octroyer des autorisations à des personnes qui effectuent des tâches de conformité telles que la gestion des périphériques, data loss prevention, eDiscovery, rétention et ainsi de suite. Ces personnes peuvent effectuer uniquement les tâches que vous leur accordez explicitement l’accès à. Pour accéder à la sécurité &amp; centre de conformité, les utilisateurs doivent être un administrateur global d’Office 365 ou un membre de la sécurité d’un ou plusieurs &amp; groupes de rôles de centre de conformité.
  
Autorisations de sécurité &amp; centre de conformité basés sur le modèle d’autorisations de contrôle d’accès en fonction de rôle (RBAC). Voici le même modèle d’autorisations qui est utilisé par Exchange, donc si vous êtes familiarisé avec Exchange, accordez des autorisations de sécurité &amp; centre de conformité sera très similaire. Il est important de noter, toutefois, ce rôle Exchange groupes et sécurité &amp; ne partagent pas les groupes de rôles de centre de conformité appartenance ou des autorisations. Alors que les deux ont un groupe de rôles de gestion de l’organisation, ils ne sont pas identiques. Leur accordent des autorisations, ainsi que les membres des groupes de rôles, sont différentes. Il existe une liste de sécurité &amp; groupes de rôles de centre de conformité ci-dessous.
  
![Page des autorisations de sécurité Office 365 &amp; centre de conformité](media/992c20ca-e82e-497c-9c8d-6fab212deb80.png)
  
## <a name="relationship-of-members-roles-and-role-groups"></a>Relation entre les membres, les rôles et les groupes de rôles

Un **rôle** accorde des autorisations pour un ensemble de tâches ; par exemple, le rôle Gestion des cas permet aux personnes d’utiliser des cas de découverte électronique. 
  
Un **groupe de rôles** est un ensemble de rôles qui permet aux utilisateurs d’effectuer leur travail sur la sécurité &amp; centre de conformité ; par exemple, le groupe de rôles d’administrateur de conformité inclut les rôles de gestion des cas, recherche de contenu et Configuration de l’organisation (ainsi que d’autres personnes), car une personne qui est un administrateur de la conformité devra les autorisations pour les tâches à effectuer leur travail. 
  
La sécurité &amp; centre de conformité inclut les groupes de rôles par défaut pour les tâches les plus courantes et les fonctions que vous aurez besoin pour affecter des personnes à. Nous vous recommandons d’ajouter simplement des utilisateurs individuels en tant que **membres** pour les groupes de rôles par défaut. 
  
![Diagramme montrant la relation des groupes de rôles avec les rôles et les membres](media/2a16d200-968c-4755-98ec-f1862d58cb8b.png)
  
Vous pouvez modifier ou supprimer les groupes de rôles existant, mais nous ne recommandons pas cette. Plutôt qu’une modification d’un groupe de rôles par défaut, vous pourrez copier, modifier, puis l’enregistrer avec un nom différent.
  
## <a name="permissions-needed-to-use-features-in-the-security-amp-compliance-center"></a>Autorisations requises pour utiliser les fonctionnalités de la sécurité &amp; centre de conformité

Le tableau suivant répertorie les groupes de rôles par défaut qui sont disponibles dans la sécurité &amp; centre de conformité. Pour accorder des autorisations à un utilisateur pour effectuer une tâche de conformité, les ajouter à la sécurité appropriée &amp; groupe de rôles de centre de conformité.
  
Gestion des autorisations de sécurité &amp; centre de conformité uniquement offre aux utilisateurs l’accès aux fonctionnalités de conformité qui sont disponibles au sein de la sécurité &amp; centre de conformité proprement dit. Si vous souhaitez accorder des autorisations à d’autres fonctionnalités de conformité qui ne figurent pas dans la sécurité &amp; centre de conformité, tels que les règles de transport Exchange, vous devez utiliser le centre d’administration Exchange.
  
Pour savoir comment accorder l’accès à la sécurité &amp; centre de conformité, extraction de [donner aux utilisateurs l’accès au centre d’administration d’Office 365 conformité](grant-access-to-the-security-and-compliance-center.md).
  
|**Groupe de rôles**|**Description**|
|:-----|:-----|
|**Administrateur de conformité** <sup>1</sup> <br/> |Les membres peuvent gérer les paramètres de gestion des périphériques, prévention des pertes de données, des rapports et des archives.  <br/> |
|**Gestionnaire eDiscovery** <br/> | Les membres peuvent effectuer des recherches et archives permanentes dans les boîtes aux lettres, les sites SharePoint Online et OneDrive pour des sites. Membres peuvent également créer et gérer des affaires eDiscovery, ajouter et supprimer des membres à un incident, créer et modifier les recherches de contenu associés à un cas et accès aux données cas eDiscovery Office 365 avancés.<br/><br/>Une découverte électronique administrateur est un membre du groupe de rôles de gestionnaire de découverte électronique qui a été attribué des autorisations supplémentaires. Outre les tâches capable d’effectuer un gestionnaire eDiscovery, une administrateur de découverte électronique peut :<br/><br/>  • Afficher tous les cas de découverte électronique dans l’organisation.  <br/>  • Gérer tous les cas eDiscovery après l’ajout eux-mêmes en tant que membre de la casse.  <br/><br/>La principale différence entre un gestionnaire eDiscovery et une administrateur eDiscovery est qu’une découverte électronique par l’administrateur peut accéder à tous les cas qui sont répertoriés dans la page **cas eDiscovery** dans la sécurité &amp; centre de conformité. Un gestionnaire de découverte électronique peut accéder uniquement au cas, qu'ils ont créés ou qu’ils sont membres de.  Pour plus d’informations sur la définition d’un utilisateur une découverte électronique administrateur, voir [attribuer des autorisations de sécurité Office 365 eDiscovery &amp; centre de conformité](assign-ediscovery-permissions.md).<br/>           |
|**Gestion de l’organisation** <sup>1</sup> <br/> |Les membres peuvent contrôler les autorisations pour accéder aux fonctionnalités de sécurité &amp; centre de conformité et également gérer les paramètres pour la gestion des périphériques, prévention des pertes de données, des rapports et des archives.  <br/> Notez que pour un utilisateur qui n’est pas un administrateur global pour afficher la liste des périphériques gérés par Mobile Device Manager pour Office 365 et effectuer des actions sur ces périphériques, telles que le retrait d’un périphérique à partir de Mobile Device Manager pour Office 365, l’utilisateur doit être un administrateur Exchange.  <br/> Office 365 les administrateurs globaux sont automatiquement ajoutés en tant que membres de ce groupe de rôles.           |
|**Gestion des enregistrements** <br/> |Les membres peuvent gérer et supprimer le contenu de l’enregistrement.  <br/> |
|**Relecteur** <br/> |Les membres peuvent afficher uniquement la liste des incidents dans la page de cas eDiscovery dans la sécurité &amp; centre de conformité. Ils ne peuvent pas créer, ouvrir ou gérer une affaire eDiscovery. Le principal objectif de ce groupe de rôles consiste à permettre aux membres de l’affichage et l’accès cas les données d’eDiscovery avancée.  <br/> Ce groupe de rôles dispose des autorisations les plus restrictives liées à la découverte électronique.  <br/> |
|**Administrateur de sécurité** <br/> |Les membres de ce groupe de rôles peuvent inclure les administrateurs cross-service, ainsi que les groupes de partenaires externes et Support Microsoft. Par défaut, ce groupe ne peut être défini des rôles. Toutefois, elle sera membre du rôle Administrateurs de la sécurité dans Azure Active Directory et hérite les fonctionnalités de ce rôle. Pour gérer les autorisations de façon centralisée, apporter des modifications à ce rôle dans le centre d’administration Azure Active Directory - pour plus d’informations, consultez la rubrique [autorisations de rôle administrateur dans Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/directory-assign-admin-roles). Si vous modifiez ce groupe de rôles dans le centre de conformité de & sécurité, ces modifications s’appliquent uniquement au centre de conformité de sécurité & et pas d’autres services, tandis que les modifications apportées dans le centre d’administration Azure Active Directory affectent tous les services.<br/> Toutes les autorisations en lecture seule au rôle de sécurité de lecteur, plus un nombre d’autorisations d’administration supplémentaires pour les mêmes services : Azure Information Protection, centre de Protection d’identité, la gestion des identités privilégié, Service de surveillance Office 365 L’intégrité et la sécurité Office 365 &amp; centre de conformité.  <br/> |
|**Lecteur de sécurité** <br/> |Les membres ont accès en lecture seule à un nombre de fonctionnalités de sécurité du centre de Protection d’identité, la gestion des identités privilégié, intégrité du Service Moniteur Office 365 et Office 365 sécurité &amp; centre de conformité.  <br/> L’appartenance à ce groupe de rôles est synchronisé dans les services et gérée de manière centralisée. Les membres de ce groupe de rôles peuvent inclure les administrateurs cross-service, ainsi que les groupes de partenaires externes et Support Microsoft. Par défaut, ce groupe ne peut être défini des rôles. Toutefois, elle sera membre du rôle Administrateurs de la sécurité dans Azure Active Directory et hérite les fonctionnalités de ce rôle. Pour gérer les autorisations de façon centralisée, apporter des modifications à ce rôle dans le centre d’administration Azure Active Directory - pour plus d’informations, consultez la rubrique [autorisations de rôle administrateur dans Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/directory-assign-admin-roles). Si vous modifiez ce groupe de rôles dans le centre de conformité de & sécurité, ces modifications s’appliquent uniquement au centre de conformité de sécurité & et pas d’autres services, tandis que les modifications apportées dans le centre d’administration Azure Active Directory affectent tous les services.<br/> |
|**Utilisateur de la certification de service** <br/> |Les membres peuvent accéder à la section assurance de Service de sécurité Office 365 &amp; centre de conformité. Assurance de service fournit des rapports et des documents qui décrivent les pratiques de sécurité de Microsoft pour les données du client qui sont stockées dans Office 365. Il fournit également les rapports d’audit tiers indépendant sur Office 365. Pour plus d’informations, voir [de Service pour l’assurance de sécurité Office 365 &amp; centre de conformité](http://go.microsoft.com/fwlink/p/?LinkID=717765).<br/> |
|**Révision de surveillance** <br/> |Les membres peuvent créer et gérer les stratégies de définition des communications sont soumis à la révision d’une organisation. Pour plus d’informations, voir [Configure surveillance passez en revue les stratégies pour votre organisation](configure-supervision-policies.md).<br/> |
   
> [!NOTE]
> <sup>1</sup> ce groupe de rôles n’assignez membres les autorisations nécessaires à la recherche dans le journal d’audit Office 365 ou d’utiliser les rapports qui peuvent inclure des données Exchange, telles que les rapports DLP ou DAV. Pour rechercher le journal d’audit ou pour afficher tous les rapports, un utilisateur doit être affectées des autorisations dans Exchange Online. Il s’agit de l’applet de commande sous-jacent utilisé pour la recherche dans le journal d’audit étant une applet de commande Exchange Online. Office 365 les administrateurs globaux peuvent rechercher le journal d’audit et afficher tous les rapports, car ils sont automatiquement ajoutées en tant que membres du groupe de rôles de gestion de l’organisation dans Exchange Online. Pour plus d’informations, voir [recherche dans le journal d’audit de sécurité Office 365 &amp; centre de conformité](https://go.microsoft.com/fwlink/p/?LinkID=708432). 
  

