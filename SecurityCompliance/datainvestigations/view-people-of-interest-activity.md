---
title: Afficher l'activité d'audit des personnes concernées
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 82c6cb419ce00aca0d636083aa41a3384cb6bb01
ms.sourcegitcommit: 2c5834235c32b2616e1813ce24eeb3419a09629f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "31030076"
---
# <a name="view-the-audit-activity-of-people-of-interest"></a>Afficher l'activité d'audit des personnes concernées

Vous avez besoin de savoir si un utilisateur a affiché un document spécifique ou s'il a purgé un élément de sa boîte aux lettres? Les enquêtes de données (préversion) sont désormais intégrées à l'outil de recherche de journal d'audit existant dans le centre de sécurité & Compliance Center. À l'aide de cette expérience intégrée, vous pouvez utiliser l'outil de gestion des données (préversion) personnes d'un outil de gestion des intérêts pour faciliter votre enquête en accédant facilement à l'activité des personnes intéressantes et en les recherchant dans votre enquête.

## <a name="before-you-begin"></a>Avant de commencer

Vous devez disposer du rôle journaux d'audit en affichage seul ou journaux d'audit dans Exchange Online pour effectuer des recherches dans le journal d'audit Office 365. Par défaut, ces rôles sont attribués aux groupes de rôles gestion de la conformité et gestion de l'organisation dans la page autorisations du centre d'administration Exchange. Pour permettre à un utilisateur d'effectuer des recherches dans le journal d'audit des enquêtes de données (aperçu) avec le niveau minimal de privilèges, vous pouvez créer un groupe de rôles personnalisé dans Exchange Online, ajouter les journaux d'audit en affichage seul ou les journaux d'audit, puis ajouter l'utilisateur en tant que membre du nouveau groupe de rôles. OUP. Pour plus d'informations, consultez la rubrique gérer des groupes de rôles dans Exchange Online.

> [!IMPORTANT]
> Si vous attribuez à un utilisateur le rôle journaux d'audit en affichage seul ou journaux d'audit sur la page des autorisations dans le centre de sécurité & Compliance Center, il ne pourra pas effectuer de recherche dans le journal d'audit Office 365. Vous devez attribuer les autorisations dans Exchange Online. Cela est dû au fait que la cmdlet sous-jacente utilisée pour effectuer des recherches dans le journal d'audit est une applet de commande Exchange Online.

## <a name="step-1-create-an-data-investigations-preview-audit-log-search"></a>Étape 1: créer une recherche de journaux d'audit (aperçu)

   1. Sélectionnez une enquête existante dans le **Centre de sécurité _AMP_ Compliance Center (en anglais) _GT_ Data investigations (Preview)**.
   
   2. Accédez à l'onglet **personnes d'intérêt** et sélectionnez une personne.
   
   3. Une fois que vous avez sélectionné une personne, cliquez sur **afficher l'activité** dans le panneau de détails.
   
   4. ConFigurez les critères de recherche suivants:
      
      a. **Activités** : cliquez sur la liste déroulante pour afficher les activités que vous pouvez rechercher. Après l'exécution de la recherche, seuls les enregistrements d'audit des activités sélectionnées sont affichés. Sélectionnez **afficher les résultats pour toutes les activités** pour afficher les résultats de toutes les activités qui répondent aux autres critères de recherche.
      
      b. **Date de début et date de fin** : sélectionnez une date et une plage horaire pour afficher les événements qui se sont produits au cours de cette période. Les sept derniers jours sont sélectionnés par défaut. La date et l'heure sont présentées au format UTC (Coordinated Universal Time). La plage de dates maximale que vous pouvez spécifier est d'un an.
      
      c. **Personnes concernées** : cliquez dans cette zone, puis sélectionnez un dépositaire spécifique pour lequel afficher les résultats de la recherche. Les enregistrements d'audit de l'activité sélectionnée effectuée par les utilisateurs que vous sélectionnez dans cette zone sont affichés dans la liste des résultats.
    
    1. Cliquez sur **Rechercher** pour exécuter la recherche à l'aide de vos critères de recherche. Les résultats de la recherche sont chargés et après quelques instants, ils s'affichent sous résultats sur la page de recherche des personnes d'intérêt. 

## <a name="step-2-view-the-audit-log-search-results"></a>Étape 2: afficher les résultats de la recherche du journal d'audit

Les résultats d'une recherche dans le journal d'audit sont affichés sous résultats dans la page du journal d'audit des personnes concernées. Un maximum de 5 000 (plus récent) événements sont affichés par incréments de 150 événements. Pour afficher d'autres événements, vous pouvez utiliser la barre de défilement dans le volet de résultats ou appuyer sur Maj + fin pour afficher les événements suivants 150.

Les résultats contiennent les informations suivantes sur chaque événement renvoyé par la recherche.
- **Date**: date et heure (au format UTC) lorsque l'événement s'est produit.

- **Adresse IP**: adresse IP du périphérique qui a été utilisé lors de l'enregistrement de l'activité. L’adresse IP apparaît au format d’adresse IPv4 ou IPv6.

- **User**: l'utilisateur (ou le compte de service) qui a effectué l'action qui a déclenché l'événement.

- **Activité**: activité effectuée par l'utilisateur. Cette valeur correspond aux activités sélectionnées dans la liste déroulante activités. Pour un événement du journal d'audit de l'administrateur Exchange, la valeur dans cette colonne est une applet de commande Exchange.

- **Élément**: objet qui a été créé ou modifié à la suite de l'activité correspondante. Par exemple, le fichier qui a été affiché ou modifié ou le compte d'utilisateur qui a été mis à jour. Toutes les activités ne disposent pas d'une valeur dans cette colonne.

- **Détail**: détails supplémentaires sur une activité. Une fois encore, toutes les activités n'auront pas de valeur.

## <a name="step-3-filter-the-search-results"></a>Étape 3: filtrer les résultats de la recherche

Outre le tri, vous pouvez également filtrer les résultats d'une recherche de journal d'audit. Cela peut vous aider à filtrer rapidement les résultats d'une activité ou d'un utilisateur spécifique. 

Pour filtrer les résultats:

 1. Créez et exécutez une recherche de journal d'audit.
  
2. Lorsque les résultats sont affichés, cliquez sur **Filtrer les résultats**.
 
3. Les zones de mots clés s'affichent sous chaque en-tête de colonne.
  
4. Cliquez sur l'une des cases sous un en-tête de colonne et tapez un mot ou une expression, en fonction de la colonne sur laquelle vous filtrez. Les résultats sont réajustés dynamiquement pour afficher les événements qui correspondent à votre filtre.
  
5. Pour effacer un filtre, cliquez sur **X** dans la zone filtre ou cliquez simplement sur **masquer le filtrage**.

## <a name="export-the-search-results-to-a-file"></a>Exporter les résultats de la recherche dans un fichier

Vous pouvez exporter les résultats d'une recherche de journal d'audit dans un fichier de valeurs séparées par des virgules (CSV) sur votre ordinateur local. Vous pouvez ouvrir ce fichier dans Microsoft Excel et utiliser des fonctionnalités telles que la recherche, le tri, le filtrage et le fractionnement d'une seule colonne (contenant des cellules à plusieurs valeurs) en plusieurs colonnes.

1. Exécutez une recherche dans le journal d'audit, puis modifiez les critères de recherche jusqu'à ce que vous ayez les résultats souhaités.
  
2. Cliquez sur Exporter les résultats, puis sélectionnez l'une des options suivantes:

    - **Enregistrer les résultats chargés:** Choisissez cette option pour exporter uniquement les entrées affichées sous **résultats** sur la page **de recherche du journal d'audit des personnes concernées** . Le fichier CSV téléchargé contient les mêmes colonnes (et données) que celles affichées sur la page (date, utilisateur, activité, élément et détails). Une colonne supplémentaire (intitulée **More**) est incluse dans le fichier CSV qui contient plus d'informations à partir de l'entrée du journal d'audit. Étant donné que vous exportez les mêmes résultats qui sont chargés (et affichables) sur la page de recherche du journal d'audit, un maximum de 5 000 entrées sont exportées.
        
    - **Télécharger tous les résultats:** Choisissez cette option pour exporter toutes les entrées du journal d'audit Office 365 correspondant aux critères de recherche. Pour un grand ensemble de résultats de recherche, choisissez cette option pour télécharger toutes les entrées à partir du journal d'audit en plus des résultats 5 000 qui peuvent être affichés sur la page **de recherche des personnes concernées** . Cette option télécharge les données brutes à partir du journal d'audit vers un fichier CSV, et contient des informations supplémentaires provenant de l'entrée du journal d'audit dans une colonne nommée AuditData. Le téléchargement du fichier peut prendre plus de temps si vous choisissez cette option d'exportation, car le fichier peut être plus volumineux que celui téléchargé si vous choisissez l'autre option.
    
      > [!IMPORTANT]
      > Vous pouvez télécharger un maximum de 50 000 entrées dans un fichier CSV à partir d'une seule recherche de journal d'audit. Si 50 000 entrées sont téléchargées dans le fichier CSV, vous pouvez probablement supposer qu'il y a plus de 50 000 événements correspondant aux critères de recherche. Pour exporter plus de cette limite, essayez d'utiliser une plage de dates pour réduire le nombre d'entrées du journal d'audit. Il se peut que vous deviez exécuter plusieurs recherches avec des plages de dates plus petites pour exporter plus de 50 000 entrées.
        

3. Une fois que vous avez sélectionné une option d'exportation, un message s'affiche en bas de la fenêtre qui vous invite à ouvrir le fichier CSV, à l'enregistrer dans le dossier téléchargements, ou à l'enregistrer dans un dossier spécifique.

Pour plus d'informations sur l'affichage, le filtrage ou l'exportation des résultats de la recherche du journal d'audit, consultez [la rubrique Search the Audit Log in the Office 365](../search-the-audit-log-in-security-and-compliance.md).