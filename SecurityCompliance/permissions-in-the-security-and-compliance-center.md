---
title: Autorisations dans le centre de sécurité &amp; conformité Office 365
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: overview
f1_keywords:
- ms.o365.cc.AdminRoleGroups
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: d10608af-7934-490a-818e-e68f17d0e9c1
description: Le centre de sécurité &amp; conformité Office 365 vous permet d'accorder des autorisations aux personnes qui effectuent des tâches de conformité telles que la gestion des appareils, la protection contre la perte de données, la découverte électronique, la rétention, etc. Ces personnes peuvent uniquement effectuer les tâches auxquelles vous leur accordez explicitement un accès. Pour accéder au centre &amp; de sécurité conformité, les utilisateurs doivent être un administrateur général Office 365 ou un membre d'un ou plusieurs &amp; groupes de rôles du centre de sécurité de la sécurité.
ms.openlocfilehash: cee6bc64b971ef99343d35df74415e80c087321e
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214914"
---
# <a name="permissions-in-the-office-365-security-amp-compliance-center"></a>Autorisations dans le centre de sécurité &amp; conformité Office 365

Le centre de sécurité &amp; conformité Office 365 vous permet d'accorder des autorisations aux personnes qui effectuent des tâches de conformité telles que la gestion des appareils, la protection contre la perte de données, la découverte électronique, la rétention, etc. Ces personnes peuvent uniquement effectuer les tâches auxquelles vous leur accordez explicitement un accès. Pour accéder au centre &amp; de sécurité conformité, les utilisateurs doivent être un administrateur général Office 365 ou un membre d'un ou plusieurs &amp; groupes de rôles du centre de sécurité de la sécurité.
  
Les autorisations dans le &amp; Centre de sécurité conformité sont basées sur le modèle d'autorisations contrôle d'accès basé sur un rôle (RBAC). Il s'agit du même modèle d'autorisations que celui utilisé par Exchange, par conséquent, si vous êtes familiarisé avec Exchange, l' &amp; octroi d'autorisations dans le centre de sécurité conformité sera très similaire. Toutefois, il est important de ne pas oublier que les groupes de rôles &amp; Exchange et les groupes de rôles du centre de sécurité ne partagent pas d'appartenance ou d'autorisations. Même si les deux ont un groupe de rôles gestion de l'organisation, ils ne sont pas identiques. Les autorisations qu'elles accordent, ainsi que les membres des groupes de rôles, sont différentes. Vous trouverez ci-dessous une &amp; liste des groupes de rôles du centre de sécurité conformité.
  
![Page des autorisations dans le centre de &amp; sécurité conformité Office 365](media/992c20ca-e82e-497c-9c8d-6fab212deb80.png)
  
## <a name="relationship-of-members-roles-and-role-groups"></a>Relation entre les membres, les rôles et les groupes de rôles

Un **rôle** accorde des autorisations pour un ensemble de tâches ; par exemple, le rôle Gestion des cas permet aux personnes d’utiliser des cas de découverte électronique. 
  
Un **groupe** de rôles est un ensemble de rôles qui permet aux utilisateurs d'effectuer leur travail &amp; dans le centre de sécurité conformité; par exemple, le groupe de rôles Administrateur de conformité inclut les rôles de gestion des dossiers, de recherche de contenu et de configuration de l'organisation (en plus d'autres), car une personne qui est un administrateur de conformité aura besoin des autorisations pour ces tâches pour effectuer leur travail. 
  
Le centre &amp; de sécurité conformité inclut les groupes de rôles par défaut pour les tâches et les fonctions les plus courantes auxquelles vous devrez attribuer des personnes. Nous vous recommandons d'ajouter simplement des utilisateurs individuels en tant que **membres** aux groupes de rôles par défaut. 
  
![Diagramme montrant la relation des groupes de rôles avec les rôles et les membres](media/2a16d200-968c-4755-98ec-f1862d58cb8b.png)
  
Vous pouvez modifier ou supprimer les groupes de rôles existants, mais nous vous déconseillons de le faire. Au lieu de modifier un groupe de rôles par défaut, vous pouvez le copier, le modifier, puis l'enregistrer sous un autre nom.
  
## <a name="permissions-needed-to-use-features-in-the-security-amp-compliance-center"></a>Autorisations nécessaires pour utiliser les fonctionnalités dans le &amp; Centre de sécurité conformité

Le tableau suivant répertorie les groupes de rôles par défaut disponibles dans le &amp; Centre de sécurité et de conformité. Pour accorder des autorisations à un utilisateur afin d'effectuer une tâche de conformité, ajoutez-les &amp; au groupe de rôles approprié Security Compliance Center.
  
La gestion des autorisations dans &amp; le centre de sécurité conformité offre uniquement aux utilisateurs l'accès aux fonctionnalités de conformité disponibles &amp; dans le centre de sécurité conformité lui-même. Si vous souhaitez accorder des autorisations à d'autres fonctionnalités de conformité qui ne se &amp; trouvent pas dans le centre de sécurité conformité, comme les règles de transport Exchange, vous devez utiliser le centre d'administration Exchange.
  
Pour savoir comment accorder l'accès au centre de &amp; sécurité conformité, consultez la rubrique [accorder aux utilisateurs l'accès au centre d'administration de conformité Office 365](grant-access-to-the-security-and-compliance-center.md).
  
|**Groupe de rôles**|**Description**|
|:-----|:-----|
|**Administrateur de conformité** <sup>1</sup> <br/> |Les membres peuvent gérer les paramètres de gestion des périphériques, de protection contre la perte de données, des rapports et de conservation.  <br/> |
|**Gestionnaire eDiscovery** <br/> | Les membres peuvent effectuer des recherches et placer des suspensions sur des boîtes aux lettres, des sites SharePoint Online et des emplacements OneDrive entreprise. Les membres peuvent également créer et gérer des cas de découverte électronique, ajouter et supprimer des membres à un cas, créer et modifier des recherches de contenu associées à un cas, et accéder à des données de cas dans Office 365 Advanced eDiscovery.<br/><br/>Un administrateur eDiscovery est membre du groupe de rôles gestionnaire eDiscovery auquel des autorisations supplémentaires ont été affectées. Outre les tâches qu'un gestionnaire eDiscovery peut effectuer, un administrateur eDiscovery peut:<br/><br/>  • Afficher tous les cas eDiscovery au sein de l'organisation.  <br/>  • Gérez les cas eDiscovery après les avoir ajoutés en tant que membres du cas.  <br/><br/>La principale différence entre un gestionnaire eDiscovery et un administrateur eDiscovery est qu'un administrateur eDiscovery peut accéder à tous les cas répertoriés sur la page **cas eDiscovery** dans le &amp; Centre de sécurité et de conformité. Un gestionnaire eDiscovery ne peut accéder qu'aux incidents qu'il a créés ou dont il est membre.  Pour plus d'informations sur la façon de faire d'un utilisateur un administrateur de découverte électronique, consultez [la &amp; rubrique attribution d'autorisations eDiscovery dans le centre de sécurité conformité Office 365](assign-ediscovery-permissions.md).<br/>           |
|**Gestion** de l'Organisation <sup>1</sup> <br/> |Les membres peuvent contrôler les autorisations d'accès aux fonctionnalités dans &amp; le centre de sécurité et gérer les paramètres de gestion des périphériques, de protection contre la perte de données, de rapports et de conservation.  <br/> Notez que, pour qu'un utilisateur qui n'est pas administrateur général puisse voir la liste des appareils gérés par MDM pour Office 365 et effectuer des actions sur ces appareils, comme la suppression d'un appareil de MDM pour Office 365, l'utilisateur doit être un administrateur Exchange.  <br/> Les administrateurs globaux Office 365 sont automatiquement ajoutés en tant que membres de ce groupe de rôles.           |
|**Gestion des enregistrements** <br/> |Les membres peuvent gérer et supprimer le contenu des enregistrements.  <br/> |
|**Relecteur** <br/> |Les membres peuvent uniquement afficher la liste des incidents dans la page cas de découverte électronique &amp; dans le centre de sécurité conformité. Ils ne peuvent pas créer, ouvrir ou gérer un cas de découverte électronique. Le principal objectif de ce groupe de rôles est de permettre aux membres d'afficher et d'accéder aux données de cas dans Advanced eDiscovery.  <br/> Ce groupe de rôles dispose des autorisations les plus restrictives liées à la découverte électronique.  <br/> |
|**Administrateur de sécurité** <br/> |Les membres de ce groupe de rôles peuvent inclure des administrateurs interservice, ainsi que des groupes de partenaires externes et le support Microsoft. Par défaut, aucun rôle ne peut être attribué à ce groupe. Toutefois, il sera membre du rôle Administrateurs de la sécurité dans Azure Active Directory et héritera des fonctionnalités de ce rôle. Pour gérer les autorisations de façon centralisée, modifiez ce rôle dans le centre d'administration Azure Active Directory: pour plus d'informations, consultez la rubrique [autorisations de rôle d'administrateur dans Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/directory-assign-admin-roles). Si vous modifiez ce groupe de rôles dans le centre de sécurité & Compliance Center, ces modifications s'appliquent uniquement au centre de sécurité & Compliance Center et non à d'autres services, tandis que les modifications apportées dans le centre d'administration Azure Active Directory affectent tous les services.<br/> Toutes les autorisations en lecture seule du rôle lecteur de sécurité, plus un certain nombre d'autorisations administratives supplémentaires pour les mêmes services: Azure information protection, Identity Protection Center, Privileged Identity Management, Monitor Office 365 service Intégrité et centre de sécurité &amp; conformité Office 365.  <br/> |
|**Lecteur de sécurité** <br/> |Les membres disposent d'un accès en lecture seule à un certain nombre de fonctionnalités de sécurité du centre de protection des identités, de la gestion des identités &amp; privilégiées, de l'état du Service Office 365 et du centre de sécurité conformité Office 365.  <br/> L'appartenance à ce groupe de rôles est synchronisée entre les services et gérés de manière centralisée. Les membres de ce groupe de rôles peuvent inclure des administrateurs interservice, ainsi que des groupes de partenaires externes et le support Microsoft. Par défaut, aucun rôle ne peut être attribué à ce groupe. Toutefois, il sera membre du rôle des lecteurs de sécurité dans Azure Active Directory et héritera des fonctionnalités de ce rôle. Pour gérer les autorisations de façon centralisée, modifiez ce rôle dans le centre d'administration Azure Active Directory: pour plus d'informations, consultez la rubrique [autorisations de rôle d'administrateur dans Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/directory-assign-admin-roles). Si vous modifiez ce groupe de rôles dans le centre de sécurité & Compliance Center, ces modifications s'appliquent uniquement au centre de sécurité & Compliance Center et non à d'autres services, tandis que les modifications apportées dans le centre d'administration Azure Active Directory affectent tous les services.<br/> |
|**Utilisateur de la certification de service** <br/> |Les membres peuvent accéder à la section assurance de service dans le &amp; Centre de sécurité conformité Office 365. Service assurance fournit des rapports et des documents qui décrivent les pratiques de sécurité Microsoft pour les données client stockées dans Office 365. Il fournit également des rapports d'audit tiers indépendants sur Office 365. Pour plus d'informations, consultez [la rubrique Service assurance dans le &amp; Centre de sécurité conformité Office 365](http://go.microsoft.com/fwlink/p/?LinkID=717765).<br/> |
|**Examen de surveillance** <br/> |Les membres peuvent créer et gérer les stratégies qui définissent les communications susceptibles d'être réexaminées au sein d'une organisation. Pour plus d'informations, consultez [la rubrique Configurer des stratégies de vérification de surveillance pour votre organisation](configure-supervision-policies.md).<br/> |
   
> [!NOTE]
> <sup>1</sup> ce groupe de rôles n'affecte pas de membres les autorisations nécessaires pour effectuer une recherche dans le journal d'audit Office 365 ou utiliser des rapports susceptibles de contenir des données Exchange, telles que les rapports DLP ou ATP. Pour effectuer une recherche dans le journal d'audit ou pour afficher tous les rapports, l'utilisateur doit disposer d'autorisations dans Exchange Online. Cela est dû au fait que la cmdlet sous-jacente utilisée pour effectuer des recherches dans le journal d'audit est une applet de commande Exchange Online. Les administrateurs globaux d'Office 365 peuvent effectuer des recherches dans le journal d'audit et afficher tous les rapports, car ils sont automatiquement ajoutés en tant que membres du groupe de rôles gestion de l'organisation dans Exchange Online. Pour plus d'informations, consultez la rubrique relative [à la recherche dans le &amp; journal d'audit dans le centre de sécurité conformité Office 365](https://go.microsoft.com/fwlink/p/?LinkID=708432). 
  

