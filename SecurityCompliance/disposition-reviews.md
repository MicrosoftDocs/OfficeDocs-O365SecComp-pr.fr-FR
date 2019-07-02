---
title: Vue d’ensemble des révisions de destruction
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Lorsque vous créez une étiquette de rétention qui conserve le contenu dans Microsoft 365, vous pouvez choisir de déclencher une révision de disposition à la fin de la période de rétention.
ms.openlocfilehash: 06b85d1ac4c8ed0527a8018129e146fee074d942
ms.sourcegitcommit: 044003455eb36071806c9f008ac631d54c64dde6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/24/2019
ms.locfileid: "35199683"
---
# <a name="overview-of-disposition-reviews"></a>Vue d’ensemble des révisions de destruction

Lorsque le contenu atteint la fin de sa période de rétention, il existe plusieurs raisons pour lesquelles vous pouvez souhaiter examiner ce contenu pour décider s’il peut être supprimé en toute sécurité («supprimé»). Par exemple, vous devrez peut-être:
  
- Suspendre la suppression («disposition») du contenu pertinent en cas de litige ou d’audit.
    
- Supprimer le contenu de la liste de disposition pour le stocker dans une archive, si ce contenu a une recherche ou une valeur historique.
    
- Affecter une période de rétention différente au contenu, si la stratégie d’origine était une solution temporaire ou provisoire.
    
- Renvoyer le contenu aux clients ou le transférer vers une autre organisation.
    
Lorsque vous créez une étiquette de rétention dans le centre de conformité Microsoft 365, le centre de sécurité Microsoft 365 ou le centre de sécurité & conformité Office 365, vous pouvez choisir de déclencher une révision de destruction à la fin de la période de rétention. Dans une révision de disposition:
  
- Les personnes que vous choisissez reçoivent une notification par courrier électronique dont le contenu doit être révisé. Ces relecteurs peuvent être des utilisateurs individuels, des groupes de distribution ou des groupes de sécurité ou des groupes Office 365. Notez que les notifications sont envoyées chaque semaine.
    
- Les réviseurs accèdent à la page de **disposition** dans &amp; le centre de conformité et de sécurité pour examiner le contenu. Les relecteurs peuvent voir le nombre d’éléments pour chaque étiquette de rétention en attente de destruction, puis sélectionner une étiquette de rétention pour afficher l’ensemble du contenu portant cette étiquette.
    
- Pour chaque document ou courrier électronique, le réviseur peut:
    
  - Appliquer une étiquette de rétention différente.
    
  - Prolonger sa période de rétention.
    
  - Supprimez-la définitivement.
    
- Les relecteurs peuvent afficher les suppressions en attente ou terminées, puis les exporter sous forme de fichier. csv.

> [!NOTE]
> Les révisions de destruction nécessitent un abonnement Office 365 entreprise E5.
  
Une révision de disposition peut inclure du contenu dans des boîtes aux lettres Exchange, des sites SharePoint, des comptes OneDrive et des groupes Office 365. Le contenu en attente d’une révision de disposition dans ces emplacements est supprimé uniquement lorsqu’un relecteur choisit de supprimer définitivement le contenu.
  
![Page des dispositions dans le centre de sécurité et conformité](media/Retention-Dispositions-v2-page.png)

## <a name="setting-up-the-disposition-review-by-creating-a-retention-label"></a>Configuration de la révision de la disposition en créant une étiquette de rétention

Il s’agit du flux de travail de base pour la configuration d’une révision de la disposition. Notez que ce flux affiche une étiquette de rétention publiée, puis appliquée manuellement par un utilisateur; une étiquette de rétention déclenchant une révision de disposition peut également être appliquée automatiquement au contenu.
  
![Graphique illustrant le flux de fonctionnement de la disposition](media/5fb3f33a-cb53-468c-becc-6dda0ec52778.png)
  
Une révision de disposition est une option lorsque vous créez une étiquette de rétention dans Office 365. Notez que cette option n’est pas disponible dans une stratégie de rétention, mais uniquement dans une étiquette de rétention configurée pour conserver le contenu.
  
Pour plus d’informations sur les étiquettes de rétention, voir [vue d’ensemble des étiquettes de](labels.md)rétention.
  
![Paramètres de rétention d’une étiquette](media/a16dd202-8862-40ac-80ff-6fee974de5da.png)
  
## <a name="disposing-content"></a>Suppression du contenu

Lorsqu’un réviseur est averti par courrier électronique que le contenu est prêt à être révisé, il peut **** accéder à la page de disposition &amp; dans le centre de sécurité et de conformité. Les relecteurs peuvent voir le nombre d’éléments pour chaque étiquette de rétention en attente de destruction, puis sélectionner une étiquette de rétention pour afficher l’ensemble du contenu portant cette étiquette.

Une fois que vous avez sélectionné une étiquette de rétention, la page suivante affiche toutes les impositions en attente pour cette étiquette.

![Options de disposition](media/Retention-Disposition-options-v2.png)

Le réviseur peut ensuite: 
  
- Appliquer une étiquette de rétention différente.
    
- Prolonger la période de rétention.
    
- Supprimez définitivement l’élément.

Notez qu’un réviseur peut sélectionner plusieurs éléments et les supprimer en même temps.
    
Un réviseur peut également utiliser le lien pour afficher le document à son emplacement d’origine, si le réviseur dispose des autorisations pour cet emplacement. Lors d’une révision de destruction, le contenu ne se déplace jamais à partir de son emplacement d’origine et n’est jamais supprimé tant que le relecteur n’a pas choisi de le faire.
  
Notez que les notifications par courrier électronique sont envoyées automatiquement aux relecteurs chaque semaine. Par conséquent, lorsque le contenu atteint la fin de sa période de rétention, il peut falloir jusqu’à sept jours pour que les relecteurs reçoivent la notification par courrier électronique que le contenu attend.
  
Notez également que toutes les actions de disposition sont auditées. Pour ce faire, vous devez activer l’audit au moins un jour avant la première action de disposition-pour plus d’informations, consultez [la rubrique Search the audit log dans le centre de &amp; sécurité conformité Office 365](search-the-audit-log-in-security-and-compliance.md). 
  
## <a name="permissions-for-disposition"></a>Autorisations pour la disposition

Pour accéder à la page de **disposition** , les relecteurs doivent être membres du rôle de **gestion disposition** et du rôle **journaux d’audit en affichage seul** . Nous vous recommandons de créer un nouveau groupe de rôles appelé réviseurs de disposition, d’ajouter ces deux rôles à ce groupe de rôles, puis d’ajouter des membres au groupe de rôles. 
  
Pour plus d’informations, consultez [la rubrique accorder aux utilisateurs l’accès &amp; au centre de sécurité conformité Office 365](grant-access-to-the-security-and-compliance-center.md)
  
## <a name="how-long-until-disposed-content-is-permanently-deleted"></a>Durée jusqu’à la suppression définitive du contenu supprimé

Le contenu en attente d’une révision de disposition est supprimé uniquement lorsqu’un relecteur choisit de supprimer définitivement le contenu. Lorsque le relecteur choisit cette option, le contenu du site SharePoint ou du compte OneDrive devient éligible pour le processus de nettoyage standard décrit dans cette section: fonctionnement d' [une stratégie de rétention avec le contenu en place](retention-policies.md#how-a-retention-policy-works-with-content-in-place).
  
Cela signifie que:
  
- Le contenu d’une bibliothèque de documents est déplacé vers la corbeille de première étape **dans les 7 jours suivant** la disposition, puis supprimé définitivement **93 jours** après cela. La Corbeille n’est pas indexée par la recherche et, par conséquent, son contenu n’est pas disponible pour une conservation eDiscovery.

- Le contenu de la bibliothèque de conservation sera définitivement supprimé **dans les 7 jours suivant** la disposition.

- Les éléments d’une boîte aux lettres Exchange seront définitivement supprimés **dans les 14 jours suivant** leur destruction. (Notez que 14 jours est le paramètre par défaut, mais il peut être configuré jusqu’à 30 jours.)
    
## <a name="view-pending-dispositions-and-disposed-items"></a>Afficher les éléments de disposition et de suppression en attente

Sur la page **destruction en attente** , vous pouvez afficher les impositions en attente et terminées pour une étiquette de rétention spécifique: 
  
- La **disposition en attente** indique les éléments qui ont atteint la fin de leur période de rétention et nécessitent une révision de la disposition. Après avoir vérifié chaque élément, déterminez si vous voulez appliquer une étiquette de rétention différente, étendez sa période de rétention ou supprimez-la définitivement. Vous pouvez sélectionner plusieurs éléments.
    
- L’onglet **éléments supprimés** indique que les éléments ont été approuvés pour suppression lors d’une révision de destruction et qu’ils sont désormais supprimés définitivement. Les éléments auxquels une étiquette de rétention différente a été appliquée ou leur période de rétention étendue dans le cadre d’une révision ne s’affichent pas ici.

![Onglets de disposition](media/Retention-Disposition-tabs.png)
    
### <a name="filter-the-disposition-views"></a>Filtrer les vues de disposition

Vous pouvez filtrer ces affichages par étiquette de rétention ou plage horaire. Pour les impositions en attente, la plage horaire est basée sur la date d’expiration. Pour les éléments supprimés, la plage horaire est basée sur la date de suppression.
  
![Options de filtre de disposition](media/Retention-filter-options.png)

### <a name="export-the-disposition-items"></a>Exportation des éléments de disposition

En outre, vous pouvez exporter les éléments de l’affichage en tant que fichier. csv que vous pouvez ouvrir dans Excel.
  
![Données de disposition exportées dans Excel](media/08e3bc09-b132-47b4-a051-a590b697e725.png)
  

