---
title: Vue d’ensemble des révisions de destruction
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: d0c6095b-bfee-4906-a2c7-89c2d7f411c1
description: Lorsque vous créez une étiquette qui conserve le contenu dans Office 365, vous pouvez choisir de déclencher une révision destruction à la fin de la période de rétention.
ms.openlocfilehash: c0a2933f597c9b314ac4ce2e72de9619fac90082
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "23013718"
---
# <a name="overview-of-disposition-reviews"></a>Vue d’ensemble des révisions de destruction

Lorsque le contenu atteint la fin de sa période de rétention, il existe plusieurs raisons pourquoi vous souhaiterez peut-être réviser ce contenu pour déterminer si elle peut être supprimé en toute sécurité (« supprimée »). Par exemple, vous devrez peut-être :
  
- Suspendre la suppression (« disposition ») du contenu pertinent en cas de litige ou d’audit.
    
- Supprimer le contenu de la liste de destruction à stocker dans une archive, si ce contenu a la recherche ou la valeur historique.
    
- Affecter une période de rétention différentes au contenu, si la stratégie d’origine était une solution temporaire ou provisoire.
    
- Renvoyer le contenu à des clients ou transférer vers une autre organisation.
    
Lorsque vous créez une étiquette qui conserve le contenu dans Office 365, vous pouvez choisir de déclencher une révision destruction à la fin de la période de rétention. Dans un examen de la disposition :
  
- Les personnes que vous choisissez recevoir une notification par courrier électronique qu’ils possèdent pour passer en revue le contenu. Ces relecteurs peuvent être des utilisateurs individuels, de distribution ou de groupes de sécurité ou de groupes d’Office 365. Notez que les notifications sont envoyées une fois par semaine.
    
- Relecteurs accédez à la page de **Disposition** de la sécurité &amp; centre de conformité pour consulter le contenu. 
    
- Pour chaque document, le réviseur peut :
    
  - Appliquer une étiquette différente.
    
  - Étendre sa période de rétention.
    
  - Supprimer définitivement.
    
- Relecteurs peuvent afficher les problèmes en attente ou historiques et exporter la liste dans un fichier .csv.
    
Notez que le destruction avis nécessitent un abonnement à Office 365 entreprise E5.
  
Un examen de disposition peut inclure le contenu dans les boîtes aux lettres Exchange, les sites SharePoint, OneDrive comptes et groupes d’Office 365. En attente d’un examen de destruction dans les emplacements de contenu est supprimé uniquement après qu’un réviseur choisit de supprimer définitivement le contenu.
  
![Page de disposition](media/b7436fb2-1f35-4146-8ca2-32c9d10f7e09.png)
  
## <a name="setting-up-the-disposition-review-by-creating-a-label"></a>La configuration de la révision de disposition en créant une étiquette

Il s’agit du flux de travail pour configurer un examen de la disposition. Notez que ce flux présente une étiquette publié et appliquée manuellement par un utilisateur ; une étiquette qui déclenche un examen de disposition peut également être appliquée automatiquement au contenu.
  
![Graphique montrant le flux du fonctionne de destruction](media/5fb3f33a-cb53-468c-becc-6dda0ec52778.png)
  
Un examen de la disposition est une option lorsque vous créez une étiquette dans Office 365. Notez que cette option n’est pas disponible dans une stratégie de rétention, mais uniquement dans une étiquette avec les paramètres de rétention.
  
Pour plus d’informations sur les étiquettes, voir [vue d’ensemble des étiquettes](labels.md).
  
![Paramètres de rétention pour une étiquette](media/a16dd202-8862-40ac-80ff-6fee974de5da.png)
  
## <a name="disposing-content"></a>Suppression du contenu

Lorsqu’un réviseur est averti par courrier électronique que le contenu est prêt passer en revue, ils peuvent accéder à la page de **Disposition** dans la sécurité &amp; centre de conformité et sélectionnez un ou plusieurs éléments. Le réviseur peut ensuite : 
  
- Appliquer une étiquette différente.
    
- Étendre la période de rétention.
    
- Supprimer définitivement l’élément.
    
Un réviseur peut utiliser le lien pour afficher le document dans son emplacement d’origine, si le réviseur dispose des autorisations à cet emplacement. Lors d’une révision de destruction, le contenu déplace jamais à partir de son emplacement d’origine, et il n’est jamais supprimé jusqu'à ce que le réviseur choisit de le faire.
  
Notez que les notifications par courrier électronique sont automatiquement envoyées aux réviseurs une fois par semaine. Par conséquent, lorsque le contenu atteint la fin de sa période de rétention, il peut prendre jusqu'à sept jours pour les réviseurs recevoir la notification par courrier électronique que le contenu est en attente de destruction.
  
Notez également que toutes les actions de destruction auditées. Pour ce faire, vous devez activer l’audit au moins un jour avant la première action de destruction - pour plus d’informations, voir [recherche dans le journal d’audit de sécurité Office 365 &amp; centre de conformité](search-the-audit-log-in-security-and-compliance.md). 
  
![Options de disposition d’un document](media/771630fd-a9b0-47cf-983b-fe85eb4cdafd.png)
  
## <a name="permissions-for-disposition"></a>Autorisations pour la disposition

Pour accéder à la page de **Disposition** , relecteurs doivent être membres du rôle **Gestion de la Disposition** et le rôle **Journaux d’Audit en affichage seul** . Nous vous recommandons de créer un nouveau groupe de rôle appelé relecteurs de destruction, en ajoutant ces deux rôles à ce groupe de rôles et puis ajouter des membres au groupe de rôles. 
  
Pour plus d’informations, voir [donner aux utilisateurs l’accès à l’Office 365 Security &amp; centre de conformité](grant-access-to-the-security-and-compliance-center.md)
  
## <a name="how-long-until-disposed-content-is-permanently-deleted"></a>Combien de temps jusqu'à ce que le contenu supprimé est définitivement supprimé.

En attente d’un examen de la disposition de contenu est supprimé uniquement après qu’un réviseur choisit de supprimer définitivement le contenu. Lorsque le réviseur choisit cette option, le contenu dans le site SharePoint ou le compte de OneDrive devient éligible pour le processus de nettoyage standard décrit dans cette section : [fonctionne d’une stratégie de rétention avec contenu sur place](retention-policies.md#how-a-retention-policy-works-with-content-in-place).
  
Cela signifie que :
  
- Le contenu dans une bibliothèque de documents sera déplacé vers la première phase Corbeille **dans les 7 jours** de destruction et puis définitivement supprimés **93 jours** après. La Corbeille n’est pas indexée par la recherche et par conséquent, son contenu n’est pas disponible pour un blocage eDiscovery. 
    
- Le contenu de la conservation permanente bibliothèque seront définitivement supprimés **dans les 7 jours** de disposition. 
    
## <a name="view-pending-and-completed-dispositions"></a>Afficher en attente et dispositions terminées

Dans la page de **Disposition** de la sécurité &amp; centre de conformité, vous pouvez afficher les problèmes en attente et terminées : 
  
- Dispositions **en attente** ont atteint la fin de leur période de rétention et nécessitent un examen de la disposition. Après avoir examiné chaque élément, décidez si vous voulez lui appliquer une étiquette différente, d’étendre sa période de rétention ou le supprimer définitivement. 
    
- Dispositions **terminé** ont été approuvées pour la suppression au cours d’un examen de la disposition et sont en cours de suppression définitive. Éléments qui avaient un libellé différent appliqué ou leur période de rétention étendue comme partie d’un examen ne s’affiche ici. 
    
### <a name="filter-the-disposition-views"></a>Filtrer les affichages de destruction

Vous pouvez filtrer ces affichages par étiquette ou la plage horaire. Pour en attente de dispositions, la plage de temps est basée sur la date d’expiration. Pour les problèmes historiques, la plage de temps est basée sur la date de suppression.
  
![Options de filtre sur la page de Disposition](media/8682a9f5-a77d-45ae-b902-8418a3ebbea1.png)
  
### <a name="export-the-disposition-items"></a>Exporter les éléments de disposition

En outre, vous pouvez exporter les éléments de l’affichage dans un fichier .csv que vous pouvez ouvrir dans Excel.
  
![Destruction exporté les données dans Excel](media/08e3bc09-b132-47b4-a051-a590b697e725.png)
  

