---
title: Vue d'ensemble des révisions de destruction
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Lorsque vous créez une étiquette qui conserve du contenu dans Office 365, vous pouvez choisir de déclencher une révision de disposition à la fin de la période de rétention.
ms.openlocfilehash: 5dac91368ff2aff6ca7e1a2c3591b50466b869ac
ms.sourcegitcommit: 6aa82374eef09d2c1921f93bda3eabeeb28aadeb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "30455036"
---
# <a name="overview-of-disposition-reviews"></a>Vue d'ensemble des révisions de destruction

Lorsque le contenu atteint la fin de sa période de rétention, il existe plusieurs raisons pour lesquelles vous pouvez souhaiter examiner ce contenu pour décider s'il peut être supprimé en toute sécurité («supprimé»). Par exemple, vous devrez peut-être:
  
- Suspendre la suppression («disposition») du contenu pertinent en cas de litige ou d'audit.
    
- Supprimer le contenu de la liste de disposition pour le stocker dans une archive, si ce contenu a une recherche ou une valeur historique.
    
- Affecter une période de rétention différente au contenu, si la stratégie d'origine était une solution temporaire ou provisoire.
    
- Renvoyer le contenu aux clients ou le transférer vers une autre organisation.
    
Lorsque vous créez une étiquette qui conserve du contenu dans Office 365, vous pouvez choisir de déclencher une révision de disposition à la fin de la période de rétention. Dans une révision de disposition:
  
- Les personnes que vous choisissez reçoivent une notification par courrier électronique dont le contenu doit être révisé. Ces relecteurs peuvent être des utilisateurs individuels, des groupes de distribution ou des groupes de sécurité ou des groupes Office 365. Notez que les notifications sont envoyées chaque semaine.
    
- Les réviseurs accèdent à la page de **disposition** dans &amp; le centre de conformité et de sécurité pour examiner le contenu. 
    
- Pour chaque document, le réviseur peut:
    
  - Appliquer une étiquette différente.
    
  - Prolonger sa période de rétention.
    
  - Supprimez-la définitivement.
    
- Les relecteurs peuvent afficher les dépôts en attente ou historiques, et exporter cette liste sous la forme d'un fichier. csv.
    
Notez que les révisions de disposition nécessitent un abonnement Office 365 entreprise E5.
  
Une révision de disposition peut inclure du contenu dans des boîtes aux lettres Exchange, des sites SharePoint, des comptes OneDrive et des groupes Office 365. Le contenu en attente d'une révision de disposition dans ces emplacements est supprimé uniquement lorsqu'un relecteur choisit de supprimer définitivement le contenu.
  
![Page de disposition](media/b7436fb2-1f35-4146-8ca2-32c9d10f7e09.png)
  
## <a name="setting-up-the-disposition-review-by-creating-a-label"></a>Configuration de la révision de la disposition en créant une étiquette

Il s'agit du flux de travail de base pour la configuration d'une révision de la disposition. Notez que ce flux affiche une étiquette publiée, puis appliquée manuellement par un utilisateur; par ailleurs, une étiquette qui déclenche une révision de disposition peut être appliquée automatiquement au contenu.
  
![Graphique illustrant le flux de fonctionnement de la disposition](media/5fb3f33a-cb53-468c-becc-6dda0ec52778.png)
  
Une révision de disposition est une option lorsque vous créez une étiquette dans Office 365. Notez que cette option n'est pas disponible dans une stratégie de rétention, mais uniquement dans une étiquette avec des paramètres de rétention.
  
Pour en savoir plus sur les étiquettes, consultez l’article [Vue d’ensemble des étiquettes](labels.md).
  
![Paramètres de réTention d'une étiquette](media/a16dd202-8862-40ac-80ff-6fee974de5da.png)
  
## <a name="disposing-content"></a>Suppression du contenu

Lorsqu'un réviseur est averti par courrier électronique que le contenu est prêt à être révisé, il peut **** accéder à la page de disposition &amp; dans le centre de sécurité conformité et sélectionner un ou plusieurs éléments. Le réviseur peut ensuite: 
  
- Appliquer une étiquette différente.
    
- Prolonger la période de rétention.
    
- Supprimez définitivement l'élément.
    
Un réviseur peut utiliser le lien pour afficher le document à son emplacement d'origine, si le réviseur dispose des autorisations pour cet emplacement. Lors d'une révision de destruction, le contenu ne se déplace jamais à partir de son emplacement d'origine et n'est jamais supprimé tant que le relecteur n'a pas choisi de le faire.
  
Notez que les notifications par courrier électronique sont envoyées automatiquement aux relecteurs chaque semaine. Par conséquent, lorsque le contenu atteint la fin de sa période de rétention, il peut falloir jusqu'à sept jours pour que les relecteurs reçoivent la notification par courrier électronique que le contenu attend.
  
Notez également que toutes les actions de disposition sont auditées. Pour ce faire, vous devez activer l'audit au moins un jour avant la première action de disposition-pour plus d'informations, consultez [la rubrique Search the audit log dans le centre de &amp; sécurité conformité Office 365](search-the-audit-log-in-security-and-compliance.md). 
  
![Options de disposition pour un document](media/771630fd-a9b0-47cf-983b-fe85eb4cdafd.png)
  
## <a name="permissions-for-disposition"></a>Autorisations pour la disposition

Pour accéder à la page de **disposition** , les relecteurs doivent être membres du rôle de **gestion disposition** et du rôle **journaux d'audit en affichage seul** . Nous vous recommandons de créer un nouveau groupe de rôles appelé réviseurs de disposition, d'ajouter ces deux rôles à ce groupe de rôles, puis d'ajouter des membres au groupe de rôles. 
  
Pour plus d'informations, consultez [la rubrique accorder aux utilisateurs l'accès &amp; au centre de sécurité conformité Office 365](grant-access-to-the-security-and-compliance-center.md)
  
## <a name="how-long-until-disposed-content-is-permanently-deleted"></a>Durée jusqu'à la suppression définitive du contenu supprimé

Le contenu en attente d'une révision de disposition est supprimé uniquement lorsqu'un relecteur choisit de supprimer définitivement le contenu. Lorsque le relecteur choisit cette option, le contenu du site SharePoint ou du compte OneDrive devient éligible pour le processus de nettoyage standard décrit dans cette section: fonctionnement d' [une stratégie de rétention avec le contenu en place](retention-policies.md#how-a-retention-policy-works-with-content-in-place).
  
Cela signifie que:
  
- Le contenu d'une bibliothèque de documents est déplacé vers la corbeille de première étape **dans les 7 jours suivant** la disposition, puis supprimé définitivement **93 jours** après cela. La Corbeille n'est pas indexée par la recherche et, par conséquent, son contenu n'est pas disponible pour une conservation eDiscovery. 
    
- Le contenu de la bibliothèque de conservation sera définitivement supprimé **dans les 7 jours suivant** la disposition. 
    
## <a name="view-pending-and-completed-dispositions"></a>Afficher les destructions en attente et terminées

Sur la page de **disposition** du centre de &amp; sécurité et de conformité, vous pouvez afficher les dispositions en attente et terminées: 
  
- Les impositions **en attente** ont atteint la fin de leur période de rétention et nécessitent une révision de la disposition. Après avoir vérifié chaque élément, déterminez si vous voulez lui appliquer une étiquette différente, prolonger sa période de rétention ou le supprimer définitivement. 
    
- **** Les imPositions terminées ont été approuvées pour suppression lors d'une révision de destruction et sont maintenant en cours de suppression définitive. Les éléments ayant une étiquette différente appliquée ou leur période de rétention étendue dans le cadre d'une révision ne s'afficheront pas ici. 
    
### <a name="filter-the-disposition-views"></a>Filtrer les vues de disposition

Vous pouvez filtrer ces affichages par étiquette ou plage de temps. Pour les impositions en attente, la plage horaire est basée sur la date d'expiration. Pour les dépôts historiques, la plage horaire est basée sur la date de suppression.
  
![Options de filtrage sur la page de disposition](media/8682a9f5-a77d-45ae-b902-8418a3ebbea1.png)
  
### <a name="export-the-disposition-items"></a>Exportation des éléments de disposition

En outre, vous pouvez exporter les éléments de l'affichage en tant que fichier. csv que vous pouvez ouvrir dans Excel.
  
![Données de disposition exPortées dans Excel](media/08e3bc09-b132-47b4-a051-a590b697e725.png)
  

