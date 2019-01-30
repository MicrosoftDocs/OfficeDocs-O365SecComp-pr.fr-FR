---
title: Afficher l’activité d’audit dépositaire
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 8219ae8a061f6d08dd37da5b7f2974dd86c68f04
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607660"
---
# <a name="viewing-custodian-audit-activity"></a>Affichage de l’activité d’audit de dépositaire

Vous devez trouver si un utilisateur affiché d’un document spécifique ou purgés un élément à partir de leur boîte aux lettres ? Découverte avancée (Preview) est désormais intégré à l’outil de recherche de journal d’audit existant dans le centre de conformité de & sécurité. À l’aide de cette expérience incorporée, vous pouvez utiliser l’outil de gestion de dépositaire eDiscovery avancées (Preview) pour faciliter vos recherches en accédant à facilement et de recherche de l’activité de dépositaires dans votre cas.

## <a name="before-you-begin"></a>Avant de commencer

Vous devez être le rôle journaux d’Audit en affichage seul ou des journaux d’Audit dans Exchange Online à rechercher dans le journal d’audit Office 365. Par défaut, ces rôles sont affectées à la gestion de la conformité et les groupes de rôles de gestion de l’organisation dans la page autorisations, dans le centre d’administration Exchange. Pour accorder à un utilisateur la possibilité de recherche avancée eDiscovery (Preview) dans le journal d’audit avec les privilèges minimaux, vous pouvez créer un groupe de rôles personnalisés dans Exchange Online, ajouter le rôle journaux d’Audit en affichage seul ou des journaux d’Audit et puis ajouter l’utilisateur en tant que membre de la nouvelle gr de rôle groupe. Pour plus d’informations, voir gérer les groupes de rôle dans Exchange Online.

> [!IMPORTANT]
> Si vous affectez à un utilisateur le rôle journaux d’Audit en affichage seul ou des journaux d’Audit dans la page autorisations, dans le centre de conformité de & sécurité, ils ne pourrez pas rechercher dans le journal d’audit Office 365. Vous devez attribuer les autorisations dans Exchange Online. Il s’agit de l’applet de commande sous-jacent utilisé pour la recherche dans le journal d’audit étant une applet de commande Exchange Online.

## <a name="step-1-create-an-advanced-ediscovery-preview-audit-log-search"></a>Étape 1 : Créer une recherche de journal d’audit eDiscovery avancées (Preview)

   1. Sélectionnez un incident existant à partir de **sécurité & centre de conformité > eDiscovery avancées (Preview)**.
   
   2. Accédez à l’onglet **dépositaires** et sélectionnez un dépositaire.
   
   3. Une fois que vous avez sélectionné un dépositaire, cliquez sur **Afficher l’activité dépositaire** à partir du Panneau de détails.
   
   4. Configurer les critères de recherche suivants :
      
      a. **activités** , cliquez sur la liste déroulante pour afficher les activités que vous pouvez rechercher. Après avoir exécuté la recherche, uniquement les enregistrements d’audit pour les activités sélectionnées sont affichées. Sélectionnez **Afficher les résultats pour toutes les activités** affiche les résultats de toutes les activités qui répondent aux critères de recherche.
      
      b. la **date de début et date de fin** - sélectionner une plage de date et heure pour afficher les événements qui se sont produites pendant cette période. Au cours des sept derniers jours sont sélectionnés par défaut. La date et l’heure sont présentées au format de temps universel coordonné (UTC). La plage de dates maximale que vous pouvez spécifier est un an.
      
      c. **dépositaires** - Click dans cette zone puis sélectionnez un dépositaire spécifique pour afficher la recherche pour les résultats. Les enregistrements d’audit pour l’activité sélectionnée effectuées par les utilisateurs que vous sélectionnez dans cette zone sont affichées dans la liste des résultats.
    
    1. Cliquez sur **Rechercher** pour lancer la recherche à l’aide de vos critères de recherche. Les résultats de recherche sont chargés, et après quelques instants, ils sont affichent sous résultats sur la page de recherche dépositaire activités. 

## <a name="step-2-view-the-audit-log-search-results"></a>Étape 2 : Afficher les résultats de recherche de journal d’audit

Les résultats d’une recherche de journal d’audit sont affichés sous résultats dans la page journal d’Audit dépositaire. Un maximum de 5 000 événements (les plus récentes) sont affichés par incréments de 150 événements. Pour afficher davantage d’événements vous pouvez utiliser la barre de défilement dans le volet résultats, ou vous pouvez appuyer sur MAJ + fin pour afficher les événements ensuite 150.

Les résultats contiennent les informations suivantes sur chaque événement renvoyé par la recherche.
- **Date**: la date et l’heure (au format UTC) lorsque l’événement s’est produite.

- **Adresse IP**: adresse IP de l’appareil qui a été utilisé lors de l’activité a été enregistrée. L’adresse IP est affichée dans le format d’adresse IPv4 ou IPv6.

- **Utilisateur**: l’utilisateur (ou le compte de service) qui a effectué l’action qui a déclenché l’événement.

- **Activité**: l’activité effectuée par l’utilisateur. Cette valeur correspond aux activités que vous avez sélectionné dans la liste déroulante activités. Pour un événement dans le journal d’audit d’administration Exchange, la valeur dans cette colonne est une cmdlet Exchange.

- **Élément**: l’objet qui a été créé ou modifié à la suite de l’activité correspondante. Par exemple, le fichier qui a été vus ou modifié ou le compte d’utilisateur qui a été mis à jour. Pas toutes les activités ont une valeur dans cette colonne.

- **Détails**: plus de détails sur une activité. Là encore, pas toutes les activités aura une valeur.

## <a name="step-3-filter-the-search-results"></a>Étape 3 : Filtrer les résultats de recherche

En plus de tri, vous pouvez également filtrer les résultats d’une recherche de journal d’audit. Vous pouvez rapidement filtrer les résultats pour un utilisateur spécifique ou une activité. 

Pour filtrer les résultats :

 1. Créer et exécuter une recherche de journal d’audit.
  
2. Lorsque les résultats sont affichés, cliquez sur **filtrer les résultats**.
 
3. Zones de mot clé sont affichés sous chaque en-tête de colonne.
  
4. Cliquez sur l’une des cases sous un en-tête de colonne, tapez un mot ou une phrase, en fonction de la colonne que vous filtrez sur. Les résultats seront dynamiquement Ajustez à nouveau pour afficher les événements qui correspondent à votre filtre.
  
5. Pour effacer un filtre, cliquez sur le **X** dans la zone Filtre ou cliquer sur **Masquer le filtrage**.

## <a name="export-the-search-results-to-a-file"></a>Exporter les résultats de recherche vers un fichier

Vous pouvez exporter les résultats d’une recherche de journal d’audit pour un fichier de valeurs séparées (CSV) sur votre ordinateur local. Vous pouvez ouvrir ce fichier dans Microsoft Excel et utiliser des fonctionnalités telles que la recherche, tri, filtrage et fractionnement d’une seule colonne (qui contient les cellules de valeurs multiples) dans plusieurs colonnes.

1. Exécuter une recherche de journal d’audit, puis modifier les critères de recherche jusqu'à ce que vous ayez les résultats souhaités.
  
2. Cliquez sur Exporter les résultats, sélectionnez une des options suivantes :

    - **Save chargé de résultats :** Choisissez cette option pour exporter uniquement les entrées qui sont affichent sous **résultats** sur la page de **recherche du journal d’Audit dépositaire** . Le fichier CSV qui est téléchargé contient les mêmes colonnes (et données) affiché dans la page (Date, utilisateur, les activités, élément et plus d’informations). Une colonne supplémentaire (intitulée **plus**) est incluse dans le fichier CSV qui contient plus d’informations à partir de l’entrée du journal d’audit. Étant donné que vous exportez les mêmes résultats qui sont chargés (et visible) dans la page de recherche du journal d’Audit, un maximum de 5 000 entrées sont exportées.
        
    - **Téléchargez tous les résultats :** Choisissez cette option pour exporter toutes les entrées du journal d’audit de Office 365 qui répondent aux critères de recherche. Pour un grand ensemble de résultats de la recherche, choisissez cette option pour télécharger toutes les entrées du journal d’audit en plus des 5 000 résultats peuvent être affichés sur la page de recherche du **journal d’Audit dépositaire** . Cette option télécharge les données brutes du journal d’audit dans un fichier CSV et contient des informations supplémentaires à partir de l’entrée du journal d’audit dans une colonne nommée AuditData. Elle peut prendre plus de temps pour télécharger le fichier si vous choisissez cette option Exporter, car le fichier peut être beaucoup plus volumineux que celui qui est téléchargé si vous choisissez l’option autres.
    
      > [!IMPORTANT]
      > Vous pouvez télécharger un maximum de 50 000 entrées dans un fichier CSV à partir d’une recherche de journal d’audit unique. Si 50 000 entrées sont téléchargées vers le fichier CSV, vous pouvez supposer que plus de 50 000 événements qui répondent aux critères de recherche. Pour exporter le plus de cette limite, essayez d’utiliser une plage de dates pour réduire le nombre d’entrées du journal d’audit. Vous devrez peut-être effectuer plusieurs recherches plus petite plage de dates pour exporter des entrées de plus de 50 000.
        

3. Après avoir sélectionné une option d’exportation, un message s’affiche en bas de la fenêtre qui vous invite à ouvrir le fichier CSV, enregistrez-le dans le dossier téléchargements ou enregistrez-le dans un dossier spécifique

[!NOTE] 
 Pour plus d’informations sur l’affichage, le filtrage ou l’exportation des résultats de recherche du journal d’audit, voir :
   - Afficher la liste des activités d’auditées 
   - Avant de commencer : Les journaux d’Audit unifiée
 