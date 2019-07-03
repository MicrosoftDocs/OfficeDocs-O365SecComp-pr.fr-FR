---
title: Exporter, configurer et afficher les enregistrements du journal d’audit
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 0d4d0f35-390b-4518-800e-0c7ec95e946c
description: Après avoir exporté et téléchargé les résultats d’une recherche de journal d’audit Office 365 dans un fichier CSV, vous pouvez utiliser la fonctionnalité transformation JSON de l’éditeur de la requête Power dans Excel pour fractionner chaque propriété de l’objet JSON dans la colonne AuditData en sa propre colonne. Cela peut vous aider à localiser rapidement les données d’audit spécifiques que vous recherchez.
ms.openlocfilehash: 7dac373e8f25ead38dddbe2663e521b35b3153ef
ms.sourcegitcommit: b262d40f6daf06be26e7586f37b736e09f8a4511
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/02/2019
ms.locfileid: "35462903"
---
# <a name="export-configure-and-view-audit-log-records"></a>Exporter, configurer et afficher les enregistrements du journal d’audit

Une fois que vous avez effectué une recherche dans le journal d’audit Office 365 et que vous avez téléchargé les résultats de la recherche dans un fichier CSV, le fichier contient une colonne nommée **AuditData**, qui contient des informations supplémentaires sur chaque événement. Les données de cette colonne sont mises en forme comme un objet JSON, qui contient plusieurs propriétés configurées en tant que paires *propriété: valeur* séparées par des virgules. Vous pouvez utiliser la fonctionnalité transformation JSON de l’éditeur Power Query dans Excel pour fractionner chaque propriété de l’objet JSON dans la colonne **AuditData** en plusieurs colonnes afin que chaque propriété dispose de sa propre colonne. Cela vous permet de trier et de filtrer sur une ou plusieurs de ces propriétés, qui peuvent vous aider à localiser rapidement les données d’audit spécifiques que vous recherchez.

## <a name="step-1-export-audit-log-search-results"></a>Étape 1: exporter les résultats de la recherche du journal d’audit

La première étape consiste à rechercher dans le journal d’audit, puis à exporter les résultats dans un fichier de valeurs séparées par des virgules (CSV) sur votre ordinateur local.
  
1. Effectuez une [recherche dans le journal d’audit](search-the-audit-log-in-security-and-compliance.md#search-the-audit-log) et révisez les critères de recherche si nécessaire jusqu’à ce que vous ayez les résultats souhaités.
    
2. Cliquez sur **Exporter les résultats** , puis sélectionnez **Télécharger tous les résultats**. 
    
   ![Cliquez sur Télécharger tous les résultats](media/ExportAuditSearchResults.png)

   Cette option permet d’exporter tous les enregistrements d’audit à partir de la recherche de journal d’audit que vous avez exécutée à l’étape 1, et de télécharger les données brutes du journal d’audit dans un fichier CSV. 

   Un message s’affiche en bas de la fenêtre qui vous invite à ouvrir ou à enregistrer le fichier CSV. 

3. Cliquez sur **enregistrer > enregistrer sous** et enregistrez le fichier CSV sur votre ordinateur local. Le téléchargement de nombreux résultats de recherche prend un certain temps. C’est généralement le cas lors de la recherche de toutes les activités ou d’une plage de dates étendue. Un message en bas des fenêtres s’affiche lorsque le téléchargement du fichier CSV est terminé.
 
   ![Message affiché lorsque le téléchargement du fichier CSV est terminé](media/ExportAuditSearchResultsFinish.png)

> [!NOTE]
  > Vous pouvez télécharger un maximum de 50 000 entrées dans un fichier CSV à partir d’une seule recherche de journal d’audit. Si 50 000 entrées sont téléchargées dans le fichier CSV, vous pouvez probablement supposer qu’il y a plus de 50 000 événements correspondant aux critères de recherche. Pour exporter plus de cette limite, essayez d’utiliser une plage de dates pour réduire le nombre d’enregistrements du journal d’audit. Il se peut que vous deviez exécuter plusieurs recherches avec des plages de dates plus petites pour exporter plus de 50 000 entrées.

## <a name="step-2-format-the-exported-audit-log-using-the-power-query-editor"></a>Étape 2: mettre en forme le journal d’audit exporté à l’aide de l’éditeur de requête Power

L’étape suivante consiste à utiliser la fonctionnalité transformation JSON de l’éditeur Power Query dans Excel pour fractionner chaque propriété de l’objet JSON dans la colonne **AuditData** en sa propre colonne. Ensuite, filtrez les colonnes pour afficher les enregistrements en fonction des valeurs de propriétés spécifiques. Cela peut vous aider à localiser rapidement les données d’audit spécifiques que vous recherchez.

1. Ouvrez un classeur vierge dans Excel pour Office 365, Excel 2019 ou Excel 2016.
    
2.  Sous l’onglet **données** , dans le groupe de rubans **obtenir des données de transformation de &** , cliquez sur **de texte/CSV**.

    ![Sous l’onglet données, cliquez sur de texte/CSV](media/JSONTransformOpenCSVFile.png)

3. Ouvrez le fichier CSV que vous avez téléchargé à l’étape 1.
    
4. Dans la fenêtre affichée, cliquez sur **transformer les données**.

   ![Cliquez sur transformer les données](media/JSONOpenPowerQuery.png)

Le fichier CSV s’ouvre dans l' **éditeur de requête**. Il existe quatre colonnes: **CreationDate**, **userids**, **Operations**et **AuditData**. La colonne **AuditData** est un objet JSON qui contient plusieurs propriétés. L’étape suivante consiste à créer une colonne pour chaque propriété de l’objet JSON.
    
5. Cliquez avec le bouton droit sur le titre dans la colonne **AuditData** , cliquez sur **transformer**, puis sur **JSON**. 
 
   ![Cliquez avec le bouton droit sur la colonne AuditData, cliquez sur transformer, puis sélectionnez JSON](media/JSONTransform.png)

6. Dans le coin supérieur droit de la colonne **AuditData** , cliquez sur l’icône développer.
    
   ![Dans la colonne AuditData, cliquez sur l’icône développer.](media/JSONTransformExpandIcon.png)

   Une liste partielle des propriétés dans les objets JSON dans la colonne **AuditData** s’affiche.

7. Cliquez sur **charger plus** pour afficher toutes les propriétés dans les objets JSON dans la colonne **AuditData** .

   ![Cliquez sur charger plus pour afficher toutes les propriétés dans l’objet JSON.](media/JSONTransformLoadJSONProperties.png)

   Vous pouvez désélectionner la case à cocher en regard d’une propriété que vous ne voulez pas inclure. La suppression des colonnes qui ne sont pas utiles pour votre enquête est un bon moyen de réduire la quantité de données affichées dans le journal d’audit. 

   > [!NOTE]
   > Les propriétés JSON affichées dans la capture d’écran précédente (après avoir cliqué sur **charger plus**) sont basées sur les propriétés figurant dans la colonne **AuditData** des premières lignes 1 000 du fichier CSV. S’il existe des propriétés JSON différentes dans les enregistrements après les 1 000 premières lignes, ces propriétés (et une colonne correspondante) ne sont pas incluses lorsque la colonne **AuditData** est fractionnée en plusieurs colonnes. Pour éviter cela, envisagez de réexécuter la recherche du journal d’audit et de limiter les critères de recherche afin d’obtenir des résultats moins nombreux. Une autre solution consiste à filtrer les éléments dans la colonne **opérations** afin de réduire le nombre de lignes (avant d’effectuer l’étape 5 ci-dessus) avant de transformer l’objet JSON dans la colonne **AuditData** .

8. Effectuez l’une des opérations suivantes pour mettre en forme le titre des colonnes qui sont ajoutées pour chaque propriété JSON sélectionnée.

    - Désélectionnez la case à cocher utiliser le nom de la **colonne d’origine comme préfixe** pour utiliser le nom de la propriété JSON comme nom de colonne; par exemple, **RecordType** ou **sourceFileName**.
    
   - Laissez la case à cocher **utiliser le nom de la colonne d’origine comme préfixe** sélectionnée pour ajouter le préfixe AuditData aux noms de colonne; par exemple, **AuditData. RecordType** ou **AuditData. sourceFileName**.

9. Cliquez sur **OK**.
    
    La colonne **AuditData** est divisée en plusieurs colonnes. Chaque nouvelle colonne correspond à une propriété dans l’objet JSON AuditData. Chaque ligne de la colonne contient la valeur de la propriété. Si la propriété ne contient pas de valeur, la valeur *null* est affichée. Dans Excel, les cellules contenant des valeurs NULL sont vides.
  
10. Sous l’onglet **Accueil** , cliquez sur **Fermer & charger** pour fermer l’éditeur de requête Power et ouvrez le fichier CSV transformé dans un classeur Excel. 

## <a name="tips-for-exporting-and-viewing-the-audit-log"></a>Conseils pour l’exportation et l’affichage du journal d’audit

Voici quelques conseils et exemples d’exportation et d’affichage du journal d’audit avant et après l’utilisation de la fonctionnalité transformation JSON pour fractionner la colonne **AuditData** en plusieurs colonnes.

- Filtrer la colonne **RecordType** pour afficher uniquement les enregistrements d’un service ou d’un domaine fonctionnel Office 365 spécifique. Par exemple, pour afficher les événements liés au partage SharePoint, sélectionnez **14** (valeur d’énumération pour les enregistrements déclenchés par les activités de partage SharePoint). Pour obtenir la liste des services Office 365 qui correspondent aux valeurs d’énumération affichées dans la colonne **RecordType** , voir [Propriétés détaillées dans le journal d’audit Office 365](detailed-properties-in-the-office-365-audit-log.md).

- Filtrez la colonne **opérations** pour afficher les enregistrements pour des activités spécifiques. Pour obtenir la liste de la plupart des opérations qui correspondent à une activité pouvant faire l’objet d’une recherche dans l’outil de recherche de journal d’audit dans le centre de sécurité & conformité, consultez la section «activités auditées» dans [Rechercher le journal d’audit dans le centre de conformité & de sécurité](search-the-audit-log-in-security-and-compliance.md#audited-activities).

- Au lieu d’utiliser l’outil de recherche de journal d’audit dans le centre de sécurité & conformité, vous pouvez utiliser la cmdlet [Search-UnifiedAuditLog](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/search-unifiedauditlog) dans Exchange Online PowerShell pour exporter les résultats d’une recherche de journal d’audit Office 365 vers un fichier CSV. Vous pouvez ensuite suivre la même procédure que celle décrite à l’étape 2 pour mettre en forme le journal d’audit à l’aide de l’éditeur de requête Power. L’un des avantages de l’utilisation de l’applet de commande PowerShell est que vous pouvez rechercher des événements à partir d’un service Office 365 spécifique à l’aide du paramètre *RecordType* . Voici quelques exemples d’utilisation de PowerShell pour exporter des enregistrements d’audit dans un fichier CSV afin que vous puissiez utiliser l’éditeur de requête Power pour transformer l’objet JSON dans la colonne **AuditData** , comme décrit à l’étape 2.

   Dans cet exemple, exécutez les commandes suivantes pour renvoyer tous les enregistrements liés aux opérations de partage SharePoint. 
   
   ```
   $auditlog = Search-UnifiedAuditLog -StartDate 06/01/2019 -EndDate 06/30/2019 -RecordType SharePointSharingOperation
   ```

   ```
   $auditlog | Select-Object -Property CreationDate,UserIds,RecordType,AuditData | Export-Csv -Path c:\AuditLogs\PowerShellAuditlog.csv -NoTypeInformation
   ```

   - Les résultats de la recherche sont exportés dans un fichier CSV nommé *PowerShellAuditlog* qui contient quatre colonnes: CreationDate, userids, RecordType, AuditData).

   - Vous pouvez utiliser le nom ou la valeur d’énumération du type d’enregistrement comme valeur du paramètre *RecordType* . Pour obtenir la liste des noms de types d’enregistrements et leurs valeurs enum correspondantes, consultez la table *AuditLogRecordType* dans le schéma de l' [API activité de gestion d’Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#enum-auditlogrecordtype---type-edmint32).
   
   - Vous ne pouvez inclure qu’une seule valeur pour ce paramètre. Pour rechercher des enregistrements d’audit pour d’autres types d’enregistrements, vous devez réexécuter les deux commandes précédentes pour spécifier un autre type d’enregistrement et ajouter ces résultats au fichier CSV d’origine. Par exemple, vous pouvez exécuter ces deux commandes pour ajouter des activités de fichiers SharePoint à partir de la même plage de dates dans le fichier PowerShellAuditlog. csv.

       ```
      $auditlog = Search-UnifiedAuditLog -StartDate 06/01/2019 -EndDate 06/30/2019 -RecordType SharePointFileOperation
      ```

      ```
      $auditlog | Select-Object -Property CreationDate,UserIds,RecordType,AuditData | Export-Csv -Append -Path c:\AuditLogs\PowerShellAuditlog.csv -NoTypeInformation
      ```
