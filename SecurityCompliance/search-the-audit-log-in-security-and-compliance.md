---
title: Rechercher dans le journal d’audit dans le centre de sécurité & conformité
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
description: 'Utilisez le centre de sécurité & conformité pour rechercher le journal d’audit unifié afin d’afficher l’activité des utilisateurs et des administrateurs dans votre organisation Office 365. '
ms.openlocfilehash: f2ac7e39f4bb94b516ff64323179e8107a179906
ms.sourcegitcommit: eda5fdbefdd1d9188375f83868c07bc075841c41
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/23/2019
ms.locfileid: "35820497"
---
# <a name="search-the-audit-log-in-the-security--compliance-center"></a>Rechercher dans le journal d’audit dans le centre de sécurité & conformité

## <a name="introduction"></a>Introduction

Vous avez besoin de savoir si un utilisateur a affiché un document spécifique ou s’il a purgé un élément de sa boîte aux lettres? Si c’est le cas, vous pouvez utiliser le &amp; Centre de sécurité conformité d’Office 365 pour rechercher le journal d’audit unifié afin d’afficher l’activité des utilisateurs et des administrateurs dans votre organisation Office 365. Pourquoi un journal d’audit unifié? Étant donné que vous pouvez rechercher les types d’activité d’utilisateur et d’administrateur suivants dans Office 365:
  
- Activité des utilisateurs dans SharePoint Online et OneDrive entreprise
    
- Activité de l’utilisateur dans Exchange Online (journalisation d’audit de boîte aux lettres Exchange)
  
- Activité d’administration dans SharePoint Online
    
- Activité d’administration dans Azure Active Directory (le service d’annuaire pour Office 365)
    
- Activité d’administration dans Exchange Online (journalisation d’audit de l’administrateur Exchange)
    
- Activité de l’utilisateur et de l’administrateur dans Sway
    
- activités eDiscovery dans le centre de sécurité et conformité
    
- Activité de l’utilisateur et de l’administrateur dans Power BI
    
- Activité de l’utilisateur et de l’administrateur dans Microsoft teams

- Activité de l’utilisateur et de l’administrateur dans Dynamics 365
    
- Activité de l’utilisateur et de l’administrateur dans Yammer
 
- Activité de l’utilisateur et de l’administrateur dans Microsoft Flow
    
- Activité de l’utilisateur et de l’administrateur dans Microsoft Stream

- Activité des analystes et des administrateurs dans Microsoft Workplace Analytics

- Activité des utilisateurs et des administrateurs dans les Microsoft PowerApp
    
   
## <a name="before-you-begin"></a>Avant de commencer

Veillez à lire les éléments suivants avant de commencer à rechercher dans le journal d’audit Office 365.
  
- Vous (ou un autre administrateur) devez d’abord activer la journalisation d’audit avant de pouvoir commencer à rechercher dans le journal d’audit Office 365. Pour l’activer, cliquez sur **Démarrer l’enregistrement des activités de l’utilisateur et** de l’administrateur sur la page de **recherche du journal d’audit** dans le centre de sécurité & conformité. (Si vous ne voyez pas ce lien, l’audit a déjà été activé pour votre organisation.) Une fois que vous l’activez, un message s’affiche indiquant que le journal d’audit est prêt et que vous pouvez exécuter une recherche dans quelques heures après la fin de la préparation. Vous ne devez effectuer cette opération qu’une seule fois. 
    
    > [!NOTE]
    > Nous allons activer l’audit par défaut. En attendant, vous pouvez l’activer comme décrit précédemment. 
  
- Vous devez disposer du rôle journaux d’audit en affichage seul ou journaux d’audit dans Exchange Online pour effectuer des recherches dans le journal d’audit Office 365. Par défaut, ces rôles sont attribués aux groupes de rôles gestion de la conformité et gestion de l’organisation dans la page **autorisations** du centre d’administration Exchange. Remarque les administrateurs globaux dans Office 365 et Microsoft 365 sont automatiquement ajoutés en tant que membres du groupe de rôles gestion de l’organisation dans Exchange Online. Pour permettre à un utilisateur d’effectuer des recherches dans le journal d’audit Office 365 avec le niveau de privilèges minimum, vous pouvez créer un groupe de rôles personnalisé dans Exchange Online, ajouter les journaux d’audit en affichage seul ou les journaux d’audit, puis ajouter l’utilisateur en tant que membre du nouveau groupe de rôles. Pour plus d’informations, consultez la rubrique [gérer des groupes de rôles dans Exchange Online](https://go.microsoft.com/fwlink/p/?LinkID=730688).
    
    > [!IMPORTANT]
    > Si vous attribuez à un utilisateur le rôle journaux d’audit en affichage seul ou journaux d’audit sur la page **autorisations** dans le centre de sécurité & conformité, il ne pourra pas effectuer de recherche dans le journal d’audit Office 365. Vous devez attribuer les autorisations dans Exchange Online. Cela est dû au fait que la cmdlet sous-jacente utilisée pour effectuer des recherches dans le journal d’audit est une applet de commande Exchange Online. 
  
- Lorsqu’une activité auditée est effectuée par un utilisateur ou un administrateur, un enregistrement d’audit est généré et stocké dans le journal d’audit Office 365 de votre organisation. La durée pendant laquelle un enregistrement d’audit est conservé (et pouvant faire l’objet d’une recherche dans le journal d’audit) dépend de votre abonnement Office 365, ainsi que du type de licence affecté à un utilisateur spécifique.

     - **Office 365 E3:** Les enregistrements d’audit sont conservés pendant 90 jours. Cela signifie que vous pouvez rechercher dans le journal d’audit les activités qui ont eu lieu au cours des 90 derniers jours.

     - **Office 365 E5:** Les enregistrements d’audit sont également conservés pendant 90 jours. La conservation des enregistrements d’audit pendant un an peut être finalement disponible pour les utilisateurs et utilisateurs E5 avec une licence E3 et une licence de complément Office 365 Advanced Compliance.

        > [!NOTE]
        > Le programme d’aperçu privé pour la période de rétention d’un an pour les enregistrements d’audit pour E5 organisations (ou pour les utilisateurs de E3 organisations qui ont des licences de complément de conformité avancées) est fermé à nouveau. Cet article sera mis à jour lorsque la période de rétention d’un an est disponible en préversion publique ou publiée pour une disponibilité générale.

- Si vous souhaitez désactiver la recherche dans le journal d’audit dans Office 365 pour votre organisation, vous pouvez exécuter la commande suivante dans PowerShell distant connecté à votre organisation Exchange Online:
    
  ```
  Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $false
  ```

    Pour réactiver la recherche d’audit, vous pouvez exécuter la commande suivante dans Exchange Online PowerShell:
    
  ```
  Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $true
  ```

    Pour plus d’informations, consultez la rubrique [désactiver la recherche de journal d’audit dans Office 365](turn-audit-log-search-on-or-off.md).
    
- Comme indiqué précédemment, la cmdlet sous-jacente utilisée pour effectuer des recherches dans le journal d’audit est une applet de commande Exchange Online, qui est **Search-UnifiedAuditLog**. Cela signifie que vous pouvez utiliser cette applet de commande pour rechercher dans le journal d’audit Office 365 au lieu d’utiliser la page de **recherche de journal d’audit** dans le centre de sécurité & conformité. Vous devez exécuter cette applet de commande dans PowerShell à distance connecté à votre organisation Exchange Online. Pour plus d’informations, consultez la rubrique [Search-UnifiedAuditLog](https://go.microsoft.com/fwlink/p/?linkid=834776). 

    Pour plus d’informations sur l’exportation des résultats de la recherche renvoyés par la cmdlet **Search-UnifiedAuditLog** dans un fichier CSV, consultez la section «conseils pour l’exportation et l’affichage du journal d’audit» dans [Exporter, configurer et afficher les enregistrements du journal d’audit](export-view-audit-log-records.md#tips-for-exporting-and-viewing-the-audit-log).  

- Si vous souhaitez télécharger par programme des données à partir du journal d’audit Office 365, nous vous recommandons d’utiliser l’API d’activité de gestion d’Office 365 au lieu d’utiliser un script PowerShell. L’API d’activité de gestion Office 365 est un service REST qui vous permet de développer des solutions d’opérations, de sécurité et de surveillance de la conformité pour votre organisation. Pour plus d’informations, voir référence de l' [API activité de gestion Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).
    
- L’affichage de l’entrée de journal d’audit correspondante dans les résultats de la recherche peut prendre jusqu’à 30 minutes ou jusqu’à 24 heures. Le tableau suivant indique le temps nécessaire pour les différents services dans Office 365.
    
    |**Service Office 365**|**30 minutes**|**24 heures**|
    |:-----|:-----|:-----|
    |Protection avancée contre les menaces et intelligence des menaces  <br/> |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)| |
    |Azure Active Directory (événements de connexion de l’utilisateur)  <br/> ||![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> |
    |Azure Active Directory (événements d’administration)  <br/> ||![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) |
    |Prévention contre la perte de données  <br/> |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)       <br/>| |
    |Dynamics 365 CRM <br/> |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/>| |
    |eDiscovery  <br/> |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/>| |
    |Exchange Online  <br/> |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> ||
    |Microsoft Flow  <br/> |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/>| |
    |Microsoft Project  <br/> |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/>| |
    |Microsoft Stream  <br/> |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/>| |
    |Microsoft Teams  <br/> |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> ||
    |Power BI  <br/> |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/>| |
    |Centre de conformité et sécurité  <br/> |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> ||
    |Sharepoint Online et OneDrive Entreprise  <br/> |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> ||
    |Sway  <br/> ||![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> |
    |Workplace Analytics<br/> |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> || 
    |Yammer  <br/> ||![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> |
   
- Azure Active Directory (Azure AD) est le service d’annuaire pour Office 365. Le journal d’audit unifié contient les activités des utilisateurs, des groupes, des applications, des domaines et des annuaires effectuées dans le centre d’administration 365 de Microsoft ou dans le portail de gestion Azure. Pour obtenir la liste complète des événements Azure AD, reportez-vous à [Azure Active Directory audit report Events](https://go.microsoft.com/fwlink/p/?LinkID=616549).
    
- L’enregistrement d’audit pour Power BI n’est pas activé par défaut. Pour rechercher des activités Power BI dans le journal d’audit Office 365, vous devez activer l’audit dans le portail d’administration de Power BI. Pour obtenir des instructions, consultez la section «journaux d’audit» dans le [portail d’administration Power bi](https://docs.microsoft.com/power-bi/service-admin-portal#audit-logs).
    
    
## <a name="search-the-audit-log"></a>Effectuer une recherche dans le journal d’audit

Voici le processus de recherche dans le journal d’audit dans Office 365.
  
[Étape 1: exécuter une recherche de journal d’audit](#step-1-run-an-audit-log-search)
  
[Étape 2: afficher les résultats de la recherche](#step-2-view-the-search-results)

[Étape 3: filtrer les résultats de la recherche](#step-3-filter-the-search-results)

[Étape 4: exporter les résultats de la recherche dans un fichier](#step-4-export-the-search-results-to-a-file)
  
### <a name="step-1-run-an-audit-log-search"></a>Étape 1: exécuter une recherche de journal d’audit

1. Accédez à [https://protection.office.com](https://protection.office.com).
    
    > [!TIP]
    > Utilisez une session de navigation privée (pas une session normale) pour accéder au centre de sécurité & conformité, car cela empêchera les informations d’identification avec lesquelles vous avez ouvert une session. Pour ouvrir une session de navigation InPrivate dans Internet Explorer ou Microsoft Edge, appuyez simplement sur CTRL + MAJ + P. Pour ouvrir une session de navigation privée dans Google Chrome (appelée fenêtre Incognito), appuyez sur CTRL + MAJ + N. 
  
2. Connectez-vous à Office 365 à l'aide de votre compte scolaire ou professionnel.
    
3. Dans le volet gauche du centre de sécurité & conformité, cliquez sur **Rechercher**, puis sur **recherche de journal d’audit**.
    
    La page **recherche du journal d’audit** s’affiche. 
    
    ![Configurez les critères, puis cliquez sur Rechercher pour exécuter le rapport.](media/8639d09c-2843-44e4-8b4b-9f45974ff7f1.png)
  
    > [!NOTE]
    > Vous devez d’abord activer la journalisation d’audit avant de pouvoir exécuter une recherche de journal d’audit. Si le lien **Démarrer l’utilisateur et l’activité** de l’administrateur s’affiche, cliquez dessus pour activer l’audit. Si vous ne voyez pas ce lien, l’audit a déjà été activé pour votre organisation. 
  
4. Configurez les critères de recherche suivants:
    
    a. **Activités** Cliquez sur la liste déroulante pour afficher les activités que vous pouvez rechercher. Les activités de l’utilisateur et de l’administrateur sont organisées en groupes d’activités associées. Vous pouvez sélectionner des activités spécifiques ou cliquer sur le nom du groupe d’activités pour sélectionner toutes les activités du groupe. Vous pouvez également cliquer sur une activité sélectionnée pour effacer la sélection. Une fois la recherche exécutée, seules les entrées du journal d’audit des activités sélectionnées sont affichées. La sélection de l’option **afficher les résultats pour toutes les activités** affiche les résultats de toutes les activités effectuées par l’utilisateur ou le groupe d’utilisateurs sélectionné. 
    
    Plus de 100 les activités de l’utilisateur et de l’administrateur sont consignées dans le journal d’audit Office 365. Cliquez sur l’onglet **activités auditées** dans la rubrique de cet article pour afficher les descriptions de chaque activité de chacun des différents services Office 365. 
    
    b. **Date de début** et **Date de fin** les 7 derniers jours sont sélectionnés par défaut. Sélectionnez une date et une plage horaire pour afficher les événements survenus au cours de cette période. La date et l’heure sont présentées au format UTC (Coordinated Universal Time). La plage de dates maximale que vous pouvez spécifier est de 90 jours. Une erreur s’affiche si la plage de dates sélectionnée est supérieure à 90 jours. 
    
    > [!TIP]
    > Si vous utilisez la plage de dates maximale de 90 jours, sélectionnez l’heure actuelle de la **Date de début**. Dans le cas contraire, vous recevrez une erreur indiquant que la date de début est antérieure à la date de fin. Si vous avez activé l’audit au cours des 90 derniers jours, la plage de dates maximale ne peut pas démarrer avant la date à laquelle l’audit a été activé. 
  
    c. **Les utilisateurs** Cliquez dans cette zone, puis sélectionnez un ou plusieurs utilisateurs pour lesquels vous souhaitez afficher les résultats de la recherche. Les entrées du journal d’audit de l’activité sélectionnée effectuées par les utilisateurs que vous sélectionnez dans cette zone sont affichées dans la liste des résultats. Laissez cette zone vide pour renvoyer les entrées de tous les utilisateurs (et comptes de service) de votre organisation. 
    
    d. **Fichier, dossier ou site** Tapez une partie ou la totalité d’un nom de fichier ou de dossier pour Rechercher l’activité liée au fichier du dossier qui contient le mot clé spécifié. Vous pouvez également spécifier l’URL d’un fichier ou d’un dossier. Si vous utilisez une URL, vérifiez que vous tapez le chemin d’URL complet ou que vous tapez une partie de l’URL, n’incluez pas de caractères spéciaux ou d’espaces. 
    
    Laissez cette zone vide pour renvoyer les entrées de tous les fichiers et dossiers de votre organisation.
    
   **BOURGEON**

   - Si vous recherchez toutes les activités liées à un **site**, ajoutez le symbole générique (\*) après l’URL pour renvoyer toutes les entrées de ce site; par exemple, **«https://contoso-my.sharepoint.com/personal/*»**.

   - Si vous recherchez toutes les activités liées à un **fichier**, ajoutez le symbole générique (\*) avant le nom de fichier pour renvoyer toutes les entrées de ce fichier; par exemple, **«* Customer_Profitability_Sample. csv»**.
    

    
5. Cliquez sur **Rechercher** pour exécuter la recherche à l’aide de vos critères de recherche. 
    
    Les résultats de la recherche sont chargés et après quelques instants, ils s’affichent sous **résultats**. Lorsque la recherche est terminée, le nombre de résultats trouvés est affiché. Un nombre maximal de 5 000 événements s’affichent dans le volet **résultats** par incréments de 150 événements. Si plus de 5 000 événements répondent aux critères de recherche, les événements 5 000 les plus récents sont affichés. 
    
    ![Le nombre de résultats s’affiche une fois la recherche terminée.](media/986216f1-ca2f-4747-9480-e232b5bf094c.png)
  
  
#### <a name="tips-for-searching-the-audit-log"></a>Conseils pour la recherche dans le journal d’audit

- Vous pouvez sélectionner des activités spécifiques à rechercher en cliquant sur le nom de l’activité. Vous pouvez aussi rechercher toutes les activités d’un groupe (telles que les **activités de fichiers et de dossiers**) en cliquant sur le nom du groupe. Si une activité est sélectionnée, vous pouvez cliquer dessus pour annuler la sélection. Vous pouvez également utiliser la zone de recherche pour afficher les activités qui contiennent le mot clé que vous tapez.
    
    ![Cliquez sur nom du groupe d’activité pour sélectionner toutes les activités.](media/3cde97cb-6f35-47c0-8612-ecd9c6ac36a3.png)
  
- Vous devez sélectionner **afficher les résultats pour toutes les activités** de la liste **activités** pour afficher les événements du journal d’audit de l’administrateur Exchange. Les événements de ce journal d’audit affichent un nom de cmdlet (par exemple, **Set-Mailbox**) dans la colonne **activité** des résultats. Pour plus d’informations, cliquez sur l’onglet **activités auditées** dans cette rubrique, puis cliquez sur **activités d’administration Exchange**.
    
    De même, il existe des activités d’audit qui n’ont pas d’élément correspondant dans la liste des **activités** . Si vous connaissiez le nom de l’opération pour ces activités, vous pouvez rechercher toutes les activités, puis filtrer les résultats en tapant le nom de l’opération dans la zone de la colonne **activité** . Pour plus d’informations sur le filtrage des résultats, voir [étape 3: filtrer les résultats](#step-3-filter-the-search-results) de la recherche. 
    
- Cliquez sur **Effacer** pour effacer les critères de recherche actuels. La plage de dates est renvoyée à la valeur par défaut des sept derniers jours. Vous pouvez également cliquer sur **Effacer tout pour afficher les résultats de toutes les activités** afin d’annuler toutes les activités sélectionnées. 
    
- Si 5 000 résultats sont trouvés, vous pouvez probablement supposer qu’il y a plus de 5 000 événements qui satisfont aux critères de recherche. Vous pouvez affiner les critères de recherche et relancer la recherche pour renvoyer moins de résultats, ou vous pouvez exporter tous les résultats de la recherche en sélectionnant **Exporter les résultats** \> **Télécharger tous les résultats**.

  
### <a name="step-2-view-the-search-results"></a>Étape 2: afficher les résultats de la recherche

Les résultats d’une recherche dans le journal d’audit sont affichés sous **résultats** dans la page **recherche du journal d’audit** . Comme indiqué précédemment, un maximum de 5 000 (plus récent) événements est affiché par incréments de 150 événements. Pour afficher d’autres événements, vous pouvez utiliser la barre de défilement dans le volet de **résultats** ou appuyer sur **MAJ + fin** pour afficher les événements suivants 150. 
  
Les résultats contiennent les informations suivantes sur chaque événement renvoyé par la recherche.
  
- **Date:** La date et l’heure (au format UTC) lorsque l’événement s’est produit. 
    
- **Adresse IP:** Adresse IP du périphérique qui a été utilisé lors de l’enregistrement de l’activité. L’adresse IP apparaît au format d’adresse IPv4 ou IPv6. 
    
- **Utilisateur:** Utilisateur (ou compte de service) ayant effectué l’action qui a déclenché l’événement. 
    
- **Activité:** Activité effectuée par l’utilisateur. Cette valeur correspond aux activités sélectionnées dans la liste déroulante **activités** . Pour un événement du journal d’audit de l’administrateur Exchange, la valeur dans cette colonne est une applet de commande Exchange. 
    
- **Élément:** Objet créé ou modifié à la suite de l’activité correspondante. Par exemple, le fichier qui a été affiché ou modifié ou le compte d’utilisateur qui a été mis à jour. Toutes les activités ne disposent pas d’une valeur dans cette colonne. 
    
- **Détail:** Informations supplémentaires sur une activité. Une fois encore, toutes les activités n’ont pas de valeur. 
    
> [!TIP]
> Cliquez sur un en-tête de colonne sous **résultats** pour trier les résultats. Vous pouvez trier les résultats de A à Z ou de Z à A. cliquez sur l’en-tête de **Date** pour trier les résultats du plus ancien au plus récent ou du plus récent au plus ancien. 
  
#### <a name="view-the-details-for-a-specific-event"></a>Afficher les détails d’un événement spécifique

Vous pouvez afficher plus de détails sur un événement en cliquant sur l’enregistrement d’événement dans la liste des résultats de la recherche. Une page de **Détails** contenant les propriétés détaillées de l’enregistrement d’événement s’affiche. Les propriétés affichées dépendent du service Office 365 dans lequel l’événement se produit. Pour afficher ces détails, cliquez sur **informations supplémentaires**. Pour obtenir des descriptions, consultez [la rubrique Propriétés détaillées dans le journal d’audit Office 365](detailed-properties-in-the-office-365-audit-log.md).
  
![Cliquez sur informations supplémentaires pour afficher les propriétés détaillées de l’enregistrement d’événement du journal d’audit.](media/6df582ae-d339-4735-b1a6-80914fb77a08.png)

  
### <a name="step-3-filter-the-search-results"></a>Étape 3: filtrer les résultats de la recherche

Outre le tri, vous pouvez également filtrer les résultats d’une recherche de journal d’audit. Il s’agit d’une fonctionnalité intéressante qui vous permet de filtrer rapidement les résultats d’une activité ou d’un utilisateur spécifique. Vous pouvez initialement créer une recherche étendue, puis filtrer rapidement les résultats pour afficher des événements spécifiques. Vous pouvez ensuite affiner les critères de recherche et relancer la recherche pour obtenir un jeu de résultats plus petit et concis.
  
Pour filtrer les résultats:
  
1. Exécutez une recherche de journal d’audit.
    
2. Lorsque les résultats sont affichés, cliquez sur **Filtrer les résultats**.
    
    Les zones de mots clés s’affichent sous chaque en-tête de colonne.
    
3. Cliquez sur l’une des cases sous un en-tête de colonne et tapez un mot ou une expression, en fonction de la colonne sur laquelle vous filtrez. Les résultats sont réajustés dynamiquement pour afficher les événements qui correspondent à votre filtre.
    
    ![Saisie d’un mot dans un filtre pour afficher les événements correspondant au filtre](media/542dc323-a997-402c-934b-cc5e218e50bc.png)
  
4. Pour effacer un filtre, cliquez sur **X** dans la zone filtre ou cliquez sur **masquer le filtrage**.
    
> [!TIP]
> Pour afficher les événements à partir du journal d’audit de l' **-** administrateur Exchange, tapez un tiret dans la zone filtre d' **activité** . Cela permet d’afficher les noms des cmdlets, qui s’affichent dans la colonne **activité** pour les événements d’administration Exchange. Vous pouvez ensuite trier les noms des applets de commande par ordre alphabétique. 

### <a name="step-4-export-the-search-results-to-a-file"></a>Étape 4: exporter les résultats de la recherche dans un fichier

Vous pouvez exporter les résultats d’une recherche de journal d’audit dans un fichier de valeurs séparées par des virgules (CSV) sur votre ordinateur local. Vous pouvez ouvrir ce fichier dans Microsoft Excel et utiliser des fonctionnalités telles que la recherche, le tri, le filtrage et le fractionnement d’une seule colonne (qui contient plusieurs propriétés) en plusieurs colonnes.
  
1. Exécutez une recherche dans le journal d’audit, puis modifiez les critères de recherche jusqu’à ce que vous ayez les résultats souhaités.
    
2. Cliquez sur **Exporter les résultats** , puis sélectionnez l’une des options suivantes: 
    
     - **Enregistrer les résultats chargés:** Choisissez cette option pour exporter uniquement les entrées affichées sous **résultats** dans la page de **recherche du journal d’audit** . Le fichier CSV téléchargé contient les mêmes colonnes (et données) que celles affichées sur la page (date, utilisateur, activité, élément et détails). Une colonne supplémentaire (nommée **More**) est incluse dans le fichier CSV qui contient plus d’informations à partir de l’entrée du journal d’audit. Étant donné que vous exportez les mêmes résultats qui sont chargés (et affichables) sur la page de **recherche du journal d’audit** , un maximum de 5 000 entrées sont exportées. 
    
     - **Télécharger tous les résultats:** Choisissez cette option pour exporter toutes les entrées du journal d’audit Office 365 correspondant aux critères de recherche. Pour un grand ensemble de résultats de recherche, choisissez cette option pour télécharger toutes les entrées à partir du journal d’audit en plus des enregistrements d’audit 5 000 qui peuvent être affichés sur la page de **recherche du journal d’audit** . Cette option télécharge les données brutes à partir du journal d’audit vers un fichier CSV, et contient des informations supplémentaires provenant de l’entrée du journal d’audit dans une colonne nommée **AuditData**. Le téléchargement du fichier peut prendre plus de temps si vous choisissez cette option d’exportation, car le fichier peut être plus volumineux que celui téléchargé si vous choisissez l’autre option.
    
       > [!IMPORTANT]
       > Vous pouvez télécharger un maximum de 50 000 entrées dans un fichier CSV à partir d’une seule recherche de journal d’audit. Si 50 000 entrées sont téléchargées dans le fichier CSV, vous pouvez probablement supposer qu’il y a plus de 50 000 événements correspondant aux critères de recherche. Pour exporter plus de cette limite, essayez d’utiliser une plage de dates pour réduire le nombre d’entrées du journal d’audit. Il se peut que vous deviez exécuter plusieurs recherches avec des plages de dates plus petites pour exporter plus de 50 000 entrées. 
  
3. Une fois que vous avez sélectionné une option d’exportation, un message s’affiche en bas de la fenêtre qui vous invite à ouvrir le fichier CSV, à l’enregistrer dans le dossier téléchargements, ou à l’enregistrer dans un dossier spécifique.
 
#### <a name="more-information-about-exporting-and-viewing-audit-log-search-results"></a>Plus d’informations sur l’exportation et l’affichage des résultats de la recherche du journal d’audit

- Si vous téléchargez tous les résultats de la recherche, le fichier CSV contient une colonne nommée **AuditData**, qui contient des informations supplémentaires sur chaque événement. Les données de cette colonne se composent d’un objet JSON qui contient plusieurs propriétés de l’enregistrement du journal d’audit. Chaque paire *propriété: valeur* dans l’objet JSON est séparée par une virgule. Vous pouvez utiliser l’outil transformation JSON de l’éditeur Power Query dans Excel pour fractionner une colonne **AuditData** en plusieurs colonnes, de sorte que chaque propriété de l’objet JSON ait sa propre colonne. Cela vous permet de trier et de filtrer sur une ou plusieurs de ces propriétés. Pour obtenir des instructions pas à pas à l’aide de l’éditeur de la requête Power pour transformer l’objet JSON, voir [Exporter, configurer et afficher les enregistrements du journal d’audit](export-view-audit-log-records.md).
    
    Une fois que vous avez séparé la colonne **AuditData** , vous pouvez filtrer sur la colonne **opérations** pour afficher les propriétés détaillées d’un type spécifique d’activité. 
    
- L’option **Télécharger tous les résultats** transfère les données brutes à partir du journal d’audit Office 365 vers un fichier CSV. Ce fichier contient différents noms de colonne (CreationDate, UserIds, Operation, AuditData) que le fichier téléchargé si vous sélectionnez l’option **enregistrer les résultats chargés** . Les valeurs des deux fichiers CSV différents pour la même activité peuvent également être différentes. Par exemple, l’activité dans la colonne **action** du fichier CSV et peut avoir une valeur différente de celle qui est affichée dans la colonne **activité** de la page de **recherche du journal d’audit** . Par exemple, MailboxLogin vs. User s’est connecté à la boîte aux lettres.

- Lorsque vous téléchargez tous les résultats à partir d’une requête de recherche qui contient des événements provenant de différents services Office 365, la colonne **AuditData** du fichier CSV contient différentes propriétés en fonction du service dans lequel l’action a été exécutée. Par exemple, les entrées des journaux d’audit Exchange et Azure AD incluent une propriété nommée **ResultStatus** qui indique si l’action a réussi ou non. Cette propriété n’est pas incluse pour les événements dans SharePoint. De même, les événements SharePoint ont une propriété qui identifie l’URL du site pour les activités liées aux fichiers et aux dossiers. Pour atténuer ce comportement, envisagez d’utiliser des recherches différentes pour exporter les résultats des activités à partir d’un seul service. 
    
    Pour obtenir une description de la plupart des propriétés répertoriées dans la colonne **AuditData** du fichier CSV lorsque vous téléchargez tous les résultats, et que le service auquel chacune d’entre elles s’applique, reportez-vous à la rubrique [Propriétés détaillées dans le journal d’audit Office 365](detailed-properties-in-the-office-365-audit-log.md).

## <a name="audited-activities"></a>Activités vérifiées

Les tableaux de cette section décrivent les activités auditées dans Office 365. Vous pouvez rechercher ces événements en effectuant une recherche dans le journal d’audit dans le centre de sécurité et de conformité.
  
Ces tableaux regroupent les activités associées ou les activités d’un service Office 365 spécifique. Les tables incluent le nom convivial qui s’affiche dans la liste déroulante **activités** et le nom de l’opération correspondante qui apparaît dans les informations détaillées d’un enregistrement d’audit et dans le fichier CSV lorsque vous exportez les résultats de la recherche. Pour obtenir des descriptions des informations détaillées, consultez [la rubrique Propriétés détaillées dans le journal d’audit Office 365](detailed-properties-in-the-office-365-audit-log.md).
  
Cliquez sur l’un des liens suivants pour accéder à une table spécifique.
  
||||
|:-----|:-----|:-----|
|[Activités de fichier et de page](#file-and-page-activities)<br/> |[Activités de dossier](#folder-activities)<br/> |[Activités de liste SharePoint](#sharepoint-list-activities)<br/>|
|[Activités de partage et d’accès aux demandes](#sharing-and-access-request-activities)<br/> |[Activités de synchronisation](#synchronization-activities)<br/> |[Activités des autorisations de site](#site-permissions-activities)<br/> |
|[Activités d’administration de site](#site-administration-activities)<br/> |[Activités de boîte aux lettres Exchange](#exchange-mailbox-activities)<br/> |[Activités Sway](#sway-activities) <br/> |
|[Activités d’administration des utilisateurs](#user-administration-activities) <br/> |[Activités d’administration du groupe Azure AD](#azure-ad-group-administration-activities) <br/> |[Activités d’administration des applications](#application-administration-activities) <br/> |
|[Activités d’administration des rôles](#role-administration-activities) <br/> |[Activités d’administration d’annuaire](#directory-administration-activities) <br/>|[activités eDiscovery](#ediscovery-activities) <br/> |
|[Activités eDiscovery avancées](#advanced-ediscovery-activities)<br/> |[Activités Power BI](#power-bi-activities) <br/> |[Microsoft Workplace Analytics](#microsoft-workplace-analytics-activities)<br/>|
|[Activités de Microsoft teams](#microsoft-teams-activities) <br/> |[Activités Yammer](#yammer-activities) <br/> |[Activités de flux Microsoft](#microsoft-flow-activities) <br/>|
|[Activités Microsoft PowerApp](#microsoft-powerapps)<br/>|[Activités de Microsoft Stream](#microsoft-stream-activities) <br/>|[Activités d’administration d’Exchange](#exchange-admin-audit-log)<br/>|
||||
  
### <a name="file-and-page-activities"></a>Activités de fichier et de page
  
Le tableau suivant décrit les activités de fichier et de page dans SharePoint Online et OneDrive entreprise.
  
|**Nom convivial**|**Opération**|**Description**|
|:-----|:-----|:-----|
|Fichier accédé  <br/> |FileAccessed  <br/> |Un compte d’utilisateur ou système accède à un fichier.  <br/> |
|(aucun)  <br/> |FileAccessedExtended  <br/> |Ceci est lié à l’activité «accès au fichier» (FileAccessed). Un événement FileAccessedExtended est enregistré lorsque la même personne accède en permanence à un fichier pendant une période prolongée (jusqu’à 3 heures). L’objectif de la journalisation des événements FileAccessedExtended est de réduire le nombre d’événements FileAccessed enregistrés lors d’un accès permanent à un fichier. Cela permet de réduire le bruit de plusieurs enregistrements FileAccessed pour ce qui est essentiellement la même activité utilisateur et vous permet de vous concentrer sur l’événement initial (et plus important) FileAccessed.  <br/> |
|Étiquette de stratégie de conformité modifiée<br/> |ComplianceSettingChanged<br/> |Une étiquette de rétention a été appliquée à un document ou supprimée de celui-ci. Cet événement est déclenché lorsqu’une étiquette de rétention est appliquée manuellement ou automatiquement à un message.<br/> |
|État de l’enregistrement modifié sur verrouillé<br/> |LockRecord<br/> |État de l’enregistrement d’une étiquette de rétention qui classifie un document en tant qu’enregistrement verrouillé. Cela signifie que le document ne peut pas être modifié ou supprimé. Seuls les utilisateurs qui disposent au moins de l’autorisation de collaborateur pour un site peuvent modifier l’état de l’enregistrement d’un document.<br/> |
|État de l’enregistrement modifié sur déverrouillé<br/> |UnlockRecord<br/> |État de l’enregistrement d’une étiquette de rétention qui classifie un document en tant qu’enregistrement déverrouillé. Cela signifie que le document peut être modifié ou supprimé. Seuls les utilisateurs qui disposent au moins de l’autorisation de collaborateur pour un site peuvent modifier l’état de l’enregistrement d’un document.<br/><br/> |
|Fichier archivé  <br/> |FileCheckedIn  <br/> |Un utilisateur archive un document qu’il a extrait d’une bibliothèque de documents.  <br/> |
|Fichier extrait  <br/> |FileCheckedOut  <br/> |Un utilisateur extrait un document situé dans une bibliothèque de documents. Les utilisateurs peuvent extraire et apporter des modifications aux documents partagés avec eux.  <br/> |
|Fichier copié  <br/> |FileCopied  <br/> |Un utilisateur copie un document à partir d’un site. Le fichier copié peut être enregistré dans un autre dossier sur le site.  <br/> |
|Fichier supprimé  <br/> |FileDeleted  <br/> |Un utilisateur supprime un document d’un site.  <br/> |
|Fichier supprimé de la corbeille  <br/> |FileDeletedFirstStageRecycleBin  <br/> |Un utilisateur supprime un fichier de la corbeille d’un site.  <br/> |
|Fichier supprimé de la Corbeille secondaire  <br/> |FileDeletedSecondStageRecycleBin  <br/> |Un utilisateur supprime un fichier de la Corbeille secondaire d’un site.  <br/> |
|Étiquette de stratégie de conformité des enregistrements supprimés<br/> |ComplianceRecordDelete<br/> |Un document qui a été classé comme enregistrement a été supprimé. Un document est considéré comme un enregistrement lorsqu’une étiquette de rétention qui classifie le contenu en tant qu’enregistrement est appliquée au document. <br/> |
|Incompatibilité de la sensibilité des documents détectés <br/>|DocumentSensitivityMismatchDetected<br/>|Un utilisateur charge un document classé avec une étiquette de sensibilité dont la priorité est supérieure à l’étiquette de sensibilité appliquée au site vers lequel le document est chargé. Cet événement n’est pas déclenché si l’étiquette de sensibilité appliquée à un site a une priorité plus élevée que l’étiquette de sensibilité appliquée à un document chargé sur le site. Pour plus d’informations sur la priorité de l’étiquette de sensibilité, consultez la section «priorité des étiquettes» dans [vue d’ensemble des étiquettes de sensibilité](sensitivity-labels.md#label-priority-order-matters).<br/>|
|Programmes malveillants détectés dans le fichier  <br/> |FileMalwareDetected  <br/> |Le moteur de protection antivirus SharePoint détecte un programme malveillant dans un fichier.  <br/> |
|Extraction des fichiers ignorés  <br/> |FileCheckOutDiscarded  <br/> |Un utilisateur ignore (ou annule) un fichier extrait. Les modifications qu’il a apportées au fichier le temps de son extraction sont ignorées et ne sont pas enregistrées dans la version du document dans la bibliothèque de documents.  <br/> |
|Fichier téléchargé  <br/> |FileDownloaded  <br/> |Un utilisateur télécharge un document à partir d’un site.  <br/> |
|Fichier modifié  <br/> |FileModified  <br/> |Le compte d’utilisateur ou système modifie le contenu ou les propriétés d’un document sur un site.  <br/> |
|(aucun)  <br/> |FileModifiedExtended  <br/> |Cela est lié à l’activité «fichier modifié» (FileModified). Un événement FileModifiedExtended est enregistré lorsque la même personne modifie continuellement un fichier pendant une période prolongée (jusqu’à 3 heures). L’objectif de la journalisation des événements FileModifiedExtended est de réduire le nombre d’événements FileModified enregistrés quand un fichier est continuellement modifié. Cela permet de réduire le bruit de plusieurs enregistrements FileModified pour ce qui est essentiellement la même activité utilisateur et vous permet de vous concentrer sur l’événement initial (et plus important) FileModified.  <br/> |
|Fichier déplacé  <br/> |FileMoved  <br/> |Un utilisateur déplace un document de son emplacement actuel sur un site vers un nouvel emplacement.  <br/> |
|(aucun)  <br/> |FilePreviewed  <br/> |L’utilisateur affiche un aperçu des fichiers sur un site SharePoint ou OneDrive entreprise. Ces événements se produisent généralement dans des volumes élevés sur la base d’une activité unique, telle que l’affichage d’une galerie d’images.  <br/> |
|Recyclage de toutes les versions mineures du fichier  <br/> |FileVersionsAllMinorsRecycled  <br/> |L’utilisateur supprime toutes les versions secondaires de l’historique des versions d’un fichier. Les versions supprimées sont déplacées vers la corbeille du site.  <br/> |
|Recyclage de toutes les versions du fichier  <br/> |FileVersionsAllRecycled  <br/> |Un utilisateur supprime toutes les versions de l’historique des versions d’un fichier. Les versions supprimées sont déplacées vers la corbeille du site.  <br/> |
|Version recyclée du fichier  <br/> |FileVersionRecycled  <br/> |Un utilisateur supprime une version de l’historique des versions d’un fichier. La version supprimée est déplacée vers la corbeille du site.  <br/> |
|Fichier renommé  <br/> |FileRenamed  <br/> |Un utilisateur renomme un document sur un site.  <br/> |
|Fichier restauré  <br/> |FileRestored  <br/> |Un utilisateur restaure un document à partir de la corbeille d’un site.  <br/> |
|Fichier téléchargé  <br/> |FileUploaded  <br/> |Un utilisateur charge un document dans un dossier sur un site.  <br/> |
|Page affichée  <br/> |PageViewed  <br/> |Un utilisateur affiche une page sur un site. Cela n’inclut pas l’utilisation d’un navigateur Web pour afficher les fichiers situés dans une bibliothèque de documents.  <br/> |
|(aucun)  <br/> |PageViewedExtended  <br/> |Ceci est lié à l’activité «page affichée» (PageViewed). Un événement PageViewedExtended est enregistré lorsque la même personne affiche de façon continue une page Web pendant une période prolongée (jusqu’à 3 heures). L’objectif de la journalisation des événements PageViewedExtended est de réduire le nombre d’événements PageViewed enregistrés lorsqu’une page est affichée en continu. Cela permet de réduire le bruit de plusieurs enregistrements PageViewed pour ce qui est essentiellement la même activité utilisateur et vous permet de vous concentrer sur l’événement initial (et plus important) PageViewed.  <br/> |
|Affichage signalé par le client <br/>|ClientViewSignaled<br/>|Le client d’un utilisateur (tel qu’un site Web ou une application mobile) a signalé que la page indiquée a été affichée par l’utilisateur. Cette activité est souvent journalisée à la suite d’un événement PagePrefetched pour une page. <br/><br/>**Remarque**: étant donné que les événements ClientViewSignaled sont signalés par le client, et non par le serveur, il est possible que l’événement ne soit pas enregistré par le serveur et, par conséquent, qu’il n’apparaisse pas dans le journal d’audit. Il est également possible que les informations contenues dans l’enregistrement d’audit ne soient pas dignes de confiance. Toutefois, étant donné que l’identité de l’utilisateur est validée par le jeton utilisé pour créer le signal, l’identité de l’utilisateur figurant dans l’enregistrement d’audit correspondant est précise. |
|(aucun) <br/>|PagePrefetched<br/>|Le client d’un utilisateur (tel qu’un site Web ou une application mobile) a demandé la page indiquée afin d’améliorer les performances si l’utilisateur y accède. Cet événement est enregistré pour indiquer que le contenu de la page a été traité sur le client de l’utilisateur. Cet événement n’indique pas clairement que l’utilisateur a accédé à la page. Lorsque le contenu de la page est affiché par le client (conformément à la demande de l’utilisateur), un événement ClientViewSignaled doit être généré. Tous les clients ne prennent pas en charge l’indication d’une pré-extraction et, par conséquent, certaines activités préalablement lues peuvent être enregistrées en tant qu’événements PageViewed.<br/>|
||||
  
### <a name="folder-activities"></a>Activités de dossier
  
Le tableau suivant décrit les activités de dossier dans SharePoint Online et OneDrive entreprise.
  
|**Nom convivial**|**Opération**|**Description**|
|:-----|:-----|:-----|
|Dossier copié  <br/> |FolderCopied  <br/> |Un utilisateur copie un dossier à partir d’un site vers un autre emplacement dans SharePoint ou OneDrive entreprise.  <br/> |
|Dossier créé  <br/> |FolderCreated  <br/> |Un utilisateur crée un dossier sur un site.  <br/> |
|Dossier supprimé  <br/> |FolderDeleted  <br/> |Un utilisateur supprime un dossier d’un site.  <br/> |
|Dossier supprimé de la corbeille  <br/> |FolderDeletedFirstStageRecycleBin  <br/> |Un utilisateur supprime un dossier de la corbeille sur un site.  <br/> |
|Dossier supprimé de la Corbeille secondaire  <br/> |FolderDeletedSecondStageRecycleBin  <br/> |Un utilisateur supprime un dossier de la Corbeille secondaire sur un site.  <br/> |
|Dossier modifié  <br/> |FolderModified  <br/> |Un utilisateur modifie un dossier sur un site. Cela inclut la modification des métadonnées de dossier, telles que la modification des balises et des propriétés.  <br/> |
|Dossier déplacé  <br/> |FolderMoved  <br/> |Un utilisateur déplace un dossier vers un autre emplacement sur un site.  <br/> |
|Dossier renommé  <br/> |FolderRenamed  <br/> |Un utilisateur renomme un dossier sur un site.  <br/> |
|Dossier restauré  <br/> |FolderRestored  <br/> |Un utilisateur restaure un dossier supprimé à partir de la corbeille sur un site.  <br/> |
||||
  
### <a name="sharepoint-list-activities"></a>Activités de liste SharePoint
  
Le tableau suivant décrit les activités liées à la façon dont les utilisateurs interagissent avec les listes et les éléments de liste dans SharePoint Online.

|**Nom convivial**|**Opération**|**Description**|
|:-----|:-----|:-----|
| Liste créée              | ListCreated              | Un utilisateur a créé une liste SharePoint.|
| Colonne de liste créée       | ListColumnCreated        | Un utilisateur a créé une colonne de liste SharePoint. Une colonne de liste est une colonne attachée à une ou plusieurs listes SharePoint. |
| Type de contenu de liste créé | ListContentTypeCreated   | Un utilisateur a créé un type de contenu de liste. Un type de contenu de liste est un type de contenu qui est associé à une ou plusieurs listes SharePoint.|
| Élément de liste créé         | ListItemCreated          | Un utilisateur A créé un élément dans une liste SharePoint existante.|
| Colonne de site créée       | SiteColumnCreated        | Un utilisateur a créé une colonne de site SharePoint. Une colonne de site est une colonne qui n’est pas attachée à une liste. Une colonne de site est également une structure de métadonnées qui peut être utilisée par n’importe quelle liste d’un site Web donné.|
| Type de contenu de site créé | ContentType de site créé | Un utilisateur a créé un type de contenu de site. Un type de contenu de site est un type de contenu qui est attaché au site parent.|
| Liste supprimée              | ListDeleted              | Un utilisateur a supprimé une liste SharePoint.|
| Colonne de liste supprimée       | Colonne de liste supprimée      | Un utilisateur a supprimé une colonne de liste SharePoint.|
| Type de contenu de liste supprimé | ListContentTypeDeleted   | Un utilisateur a supprimé un type de contenu de liste. |
| Élément de liste supprimé         | Élément de liste supprimé        | Un utilisateur a supprimé un élément de liste SharePoint.|
| Colonne de site supprimée       | SiteColumnDeleted        | Un utilisateur a supprimé une colonne de site SharePoint. |
| Type de contenu de site supprimé | SiteContentTypeDeleted   | Un utilisateur a supprimé un type de contenu de site.|
| Élément de liste recyclé        | ListItemRecycled         | Un utilisateur a déplacé un élément de liste SharePoint vers la corbeille.|
| Liste restaurée             | ListRestored             | Un utilisateur a restauré une liste SharePoint à partir de la corbeille.|
| Élément de liste restauré        | ListItemRestored         | Un utilisateur a restauré un élément de liste SharePoint à partir de la corbeille.|
| Liste mise à jour              | ListUpdated              | Un utilisateur a mis à jour une liste SharePoint en modifiant une ou plusieurs propriétés.|
| Colonne de liste mise à jour       | ListColumnUpdated        | Un utilisateur a mis à jour une colonne de liste SharePoint en modifiant une ou plusieurs propriétés.|
| Type de contenu de liste mis à jour | ListContentTypeUpdated   | Un utilisateur a mis à jour un type de contenu de liste en modifiant une ou plusieurs propriétés.|
| Élément de liste mis à jour         | ListItemUpdated          | Un utilisateur a mis à jour un élément de liste SharePoint en modifiant une ou plusieurs propriétés.|  
| Colonne de site mise à jour       | SiteColumnUpdated        | Un utilisateur a mis à jour une colonne de site SharePoint en modifiant une ou plusieurs propriétés.|
| Type de contenu de site mis à jour | SiteContentTypeUpdated   | Un utilisateur a mis à jour un type de contenu de site en modifiant une ou plusieurs propriétés.|
||||

### <a name="sharing-and-access-request-activities"></a>Activités de partage et d’accès aux demandes
  
Le tableau suivant décrit les activités de partage d’utilisateurs et de demande d’accès dans SharePoint Online et OneDrive entreprise. Pour les événements de partage, la colonne de **détail** sous **résultats** identifie le nom de l’utilisateur ou du groupe avec lequel l’élément a été partagé, et indique si cet utilisateur ou ce groupe est membre ou invité dans votre organisation. Pour plus d’informations, reportez-vous à [la rubrique utiliser l’audit de partage dans le journal d’audit Office 365](use-sharing-auditing.md).
  
> [!NOTE]
> Les utilisateurs peuvent être *membres* ou *invités* en fonction de la propriété usertype de l’objet User. Un membre est généralement un employé et un invité est généralement un collaborateur en dehors de votre organisation. Lorsqu’un utilisateur accepte une invitation de partage (et ne fait pas déjà partie de votre organisation), un compte invité est créé pour eux dans l’annuaire de votre organisation. Une fois que l’utilisateur invité dispose d’un compte dans votre répertoire, les ressources peuvent être partagées directement avec elles (sans avoir besoin d’invitation). 
  
|**Nom convivial**|**Opération**|**Description**|
|:-----|:-----|:-----|
|Niveau d’autorisation ajouté à la collection de sites  <br/> |PermissionLevelAdded  <br/> |Un niveau d’autorisation a été ajouté à une collection de sites.  <br/> |
|Demande d’accès acceptée  <br/> |AccessRequestAccepted  <br/> |Une demande d’accès à un site, un dossier ou un document a été acceptée et l’utilisateur à l’origine de la demande a reçu l’autorisation d’accès.  <br/> |
|Invitation de partage acceptée  <br/> |SharingInvitationAccepted  <br/> |Un utilisateur (membre ou invité) a accepté une invitation de partage et a reçu l’autorisation d’accéder à une ressource. Cet événement inclut des informations sur l’utilisateur qui a été invité et l’adresse de messagerie utilisée pour accepter l’invitation (elles peuvent être différentes). Cette activité est souvent accompagnée d’un deuxième événement qui décrit le mode d’accès à la ressource accordé à l’utilisateur, par exemple, l’ajout de l’utilisateur à un groupe ayant accès à la ressource.  <br/> |
|Invitation de partage bloquée  <br/> |SharingInvitationBlocked  <br/> | Une invitation de partage envoyée par un utilisateur de votre organisation est bloquée en raison d’une stratégie de partage externe qui autorise ou refuse le partage externe en fonction du domaine de l’utilisateur cible. Dans ce cas, l’invitation de partage a été bloquée pour les raisons suivantes:  <br/>  Le domaine de l’utilisateur cible n’est pas inclus dans la liste des domaines autorisés.  <br/>  Ou  <br/>  Le domaine de l’utilisateur cible est inclus dans la liste des domaines bloqués.  <br/>  Pour plus d’informations sur l’autorisation ou le blocage du partage externe basé sur des domaines, voir [Restricted Domains sharing in SharePoint Online et OneDrive entreprise](https://support.office.com/article/5d7589cd-0997-4a00-a2ba-2320ec49c4e9).  <br/> |
|Demande d’accès créée  <br/> |AccessRequestCreated  <br/> |Un utilisateur demande l’accès à un site, un dossier ou un document auquel il n’est pas autorisé à accéder.  <br/> |
|Création d’un lien partageant une société  <br/> |CompanyLinkCreated  <br/> |Un utilisateur a créé un lien à l’échelle de l’entreprise vers une ressource. les liens à l’échelle de l’entreprise ne peuvent être utilisés que par les membres de votre organisation. Ils ne peuvent pas être utilisés par les invités.  <br/> |
|Création d’un lien anonyme  <br/> |AnonymousLinkCreated  <br/> |Un utilisateur a créé un lien anonyme vers une ressource. Toute personne disposant de ce lien peut accéder à la ressource sans avoir à être authentifiée.  <br/> |
|Lien sécurisé créé  <br/> |SecureLinkCreated  <br/> |Un lien de partage sécurisé a été créé sur cet élément.  <br/> |
|Invitation de partage créée  <br/> |SharingInvitationCreated  <br/> |Un utilisateur a partagé une ressource dans SharePoint Online ou OneDrive entreprise avec un utilisateur qui n’est pas dans l’annuaire de votre organisation.  <br/> |
|Lien sécurisé supprimé  <br/> |SecureLinkDeleted  <br/> |Un lien de partage sécurisé a été supprimé.  <br/> |
|Demande d’accès refusée  <br/> |AccessRequestDenied  <br/> |Une demande d’accès à un site, un dossier ou un document a été refusée.  <br/> |
|Suppression d’un lien partageant une société  <br/> |CompanyLinkRemoved  <br/> |Un utilisateur a supprimé un lien à l’échelle de l’entreprise vers une ressource. Le lien ne peut plus être utilisé pour accéder à la ressource.  <br/> |
|Suppression d’un lien anonyme  <br/> |AnonymousLinkRemoved  <br/> |Un utilisateur a supprimé un lien anonyme vers une ressource. Le lien ne peut plus être utilisé pour accéder à la ressource.  <br/> |
|Fichier, dossier ou site partagé  <br/> |SharingSet  <br/> |Utilisateur (membre ou invité) partage d’un fichier, d’un dossier ou d’un site dans SharePoint ou OneDrive entreprise avec un utilisateur dans l’annuaire de votre organisation. La valeur dans la colonne **détail** de cette activité Identifie le nom de l’utilisateur avec lequel la ressource a été partagée et indique si cet utilisateur est membre ou invité. Cette activité est souvent accompagnée d’un deuxième événement qui décrit comment l’utilisateur a été autorisé à accéder à la ressource. Par exemple, l’ajout de l’utilisateur à un groupe qui a accès à la ressource.  <br/> |
|Demande d’accès mise à jour  <br/> |AccessRequestUpdated  <br/> |Une demande d’accès à un élément a été mise à jour.  <br/> |
|Mise à jour d’un lien anonyme  <br/> |AnonymousLinkUpdated  <br/> |Un utilisateur a mis à jour un lien anonyme vers une ressource. Le champ mis à jour est inclus dans la propriété EventData lorsque vous exportez les résultats de la recherche.  <br/> |
|Invitation de partage mise à jour  <br/> |SharingInvitationUpdated  <br/> |Une invitation de partage externe a été mise à jour.  <br/> |
|Utilisation d’un lien anonyme  <br/> |AnonymousLinkUsed  <br/> |Un utilisateur anonyme a accédé à une ressource à l’aide d’un lien anonyme. L’identité de l’utilisateur peut être inconnue, mais vous pouvez obtenir d’autres détails, tels que l’adresse IP de l’utilisateur.  <br/> |
|Fichier, dossier ou site non partagé  <br/> |SharingRevoked  <br/> |Utilisateur (membre ou invité) non partagé d’un fichier, d’un dossier ou d’un site qui a été précédemment partagé avec un autre utilisateur.  <br/> |
|Utilisation d’un lien partageable avec une société  <br/> |CompanyLinkUsed  <br/> |Un utilisateur a accédé à une ressource à l’aide d’un lien à l’échelle de l’entreprise.  <br/> |
|Lien sécurisé utilisé  <br/> |SecureLinkUsed  <br/> |Un utilisateur a utilisé un lien sécurisé.  <br/> |
|Utilisateur ajouté à la liaison sécurisée  <br/> |AddedToSecureLink  <br/> |Un utilisateur a été ajouté à la liste des entités pouvant utiliser un lien de partage sécurisé.  <br/> |
|Utilisateur supprimé de la liaison sécurisée  <br/> |RemovedFromSecureLink  <br/> |Un utilisateur a été supprimé de la liste des entités pouvant utiliser un lien de partage sécurisé.  <br/> |
|Invitation de partage withdrew  <br/> |SharingInvitationRevoked  <br/> |Utilisateur withdrew une invitation de partage à une ressource.  <br/> |
||||
  
### <a name="synchronization-activities"></a>Activités de synchronisation
  
Le tableau suivant répertorie les activités de synchronisation de fichiers dans SharePoint Online et OneDrive entreprise.
  
|**Nom convivial**|**Opération**|**Description**|
|:-----|:-----|:-----|
|Ordinateur autorisé à synchroniser des fichiers  <br/> |ManagedSyncClientAllowed  <br/> |Un utilisateur établit une relation de synchronisation avec un site. La relation de synchronisation est établie car l’ordinateur de l’utilisateur est membre d’un domaine qui a été ajouté à la liste des domaines (appelé *liste des destinataires fiables*) qui peut accéder aux bibliothèques de documents de votre organisation.  <br/> Pour plus d’informations sur cette fonctionnalité, reportez-vous à l’article [Utilisation des cmdlet Windows PowerShell pour activer la synchronisation de OneDrive pour les domaines figurant dans la liste des destinataires approuvés](https://go.microsoft.com/fwlink/p/?LinkID=534609).  <br/> |
|Ordinateur bloqué de la synchronisation des fichiers  <br/> |UnmanagedSyncClientBlocked  <br/> |Un utilisateur tente d’établir une relation de synchronisation avec un site à partir d’un ordinateur qui n’est pas membre du domaine de votre organisation ou membre d’un domaine qui n’a pas été ajouté à la liste des domaines (appelé *liste des destinataires fiables)* pouvant accéder au document bibliothèques de votre organisation. La relation de synchronisation n’est pas autorisée et l’ordinateur de l’utilisateur est bloqué en matière de synchronisation, de téléchargement ou de chargement de fichiers dans une bibliothèque de documents.  <br/> Pour plus d’informations sur cette fonctionnalité, reportez-vous à l’article [Utilisation des cmdlet Windows PowerShell pour activer la synchronisation de OneDrive pour les domaines figurant dans la liste des destinataires approuvés](https://go.microsoft.com/fwlink/p/?LinkID=534609).  <br/> |
|Fichiers téléchargés sur l’ordinateur  <br/> |FileSyncDownloadedFull  <br/> |Un utilisateur établit une relation de synchronisation et télécharge des fichiers pour la première fois sur son ordinateur à partir d’une bibliothèque de documents.  <br/> |
|Modifications apportées au fichier téléchargé sur l’ordinateur  <br/> |FileSyncDownloadedPartial  <br/> |Un utilisateur télécharge correctement les modifications apportées aux fichiers à partir d’une bibliothèque de documents. Cette activité indique que les modifications apportées aux fichiers dans la bibliothèque de documents ont été téléchargées sur l’ordinateur de l’utilisateur. Seules les modifications ont été téléchargées, car la bibliothèque de documents a été téléchargée précédemment par l’utilisateur (comme indiqué par l’activité **fichiers téléchargés vers l’ordinateur** ).  <br/> |
|Fichiers téléchargés dans la bibliothèque de documents  <br/> |FileSyncUploadedFull  <br/> |Un utilisateur établit une relation de synchronisation et télécharge des fichiers pour la première fois à partir de son ordinateur vers une bibliothèque de documents.  <br/> |
|Modifications de fichiers téléchargées dans la bibliothèque de documents  <br/> |FileSyncUploadedPartial  <br/> |L’utilisateur télécharge les modifications apportées aux fichiers dans une bibliothèque de documents. Cet événement indique que les modifications apportées à la version locale d’un fichier dans une bibliothèque de documents sont correctement chargées dans la bibliothèque de documents. Seules les modifications sont téléchargées, car ces fichiers ont été précédemment téléchargés par l’utilisateur (comme indiqué par l’activité des **fichiers téléchargés vers la bibliothèque de documents** ).  <br/> |
||||

### <a name="site-permissions-activities"></a>Activités des autorisations de site

Le tableau suivant répertorie les événements liés à l’attribution d’autorisations dans SharePoint et l’utilisation de groupes pour accorder (et révoquer) l’accès aux sites.

|**Nom convivial**|**Opération**|**Description**|
|:-----|:-----|:-----|
|Ajout de l’administrateur de collection de sites  <br/> |SiteCollectionAdminAdded  <br/> |L’administrateur ou le propriétaire de la collection de sites ajoute une personne en tant qu’administrateur de collection de sites pour un site. Les administrateurs de collection de sites disposent du niveau d’autorisation Contrôle total sur la collection de sites et tous les sous-sites. Cette activité est également consignée lorsqu’un administrateur a lui-même accès au compte OneDrive d’un utilisateur (en modifiant le profil utilisateur dans le centre d’administration SharePoint ou [en utilisant le centre d’administration Microsoft 365](https://docs.microsoft.com/office365/admin/add-users/get-access-to-and-back-up-a-former-user-s-data#part-1---get-access-to-the-former-employees-onedrive-for-business-documents)). <br/> |
|Ajout d’un utilisateur ou d’un groupe à un groupe SharePoint  <br/> |AddedToGroup  <br/> |Un utilisateur a ajouté un membre ou un invité à un groupe SharePoint. Il peut s’agir d’une action intentionnelle ou du résultat d’une autre activité, telle qu’un événement de partage.  <br/> |
|L’héritage du niveau d’autorisation a été interrompu  <br/> |PermissionLevelsInheritanceBroken  <br/> |Un élément a été modifié de sorte qu’il n’hérite plus des niveaux d’autorisation de son parent.  <br/> |
|Héritage de partage rompu  <br/> |SharingInheritanceBroken  <br/> |Un élément a été modifié de sorte qu’il n’hérite plus des autorisations de partage de son parent.  <br/> |
|Groupe créé  <br/> |GroupAdded  <br/> |L’administrateur de site ou le propriétaire crée un groupe pour un site ou effectue une tâche qui entraîne la création d’un groupe. Par exemple, la première fois qu’un utilisateur crée un lien pour partager un fichier, un groupe système est ajouté au site OneDrive Entreprise de l’utilisateur. Cet événement peut également être le résultat de la création d’un lien par un utilisateur avec autorisation de modification sur un fichier partagé.  <br/> |
|Groupe supprimé  <br/> |GroupRemoved  <br/> |Un utilisateur supprime un groupe d’un site.  <br/> |
|Paramètre de demande d’accès modifié  <br/> |WebRequestAccessModified  <br/> |Les paramètres de demande d’accès ont été modifiés sur un site.  <br/> |
|Paramètre «les membres peuvent être partagés» modifiés  <br/> |WebMembersCanShareModified  <br/> |Le paramètre les **membres peuvent partager** a été modifié sur un site.  <br/> |
|Niveau d’autorisation modifié sur la collection de sites  <br/> |PermissionLevelModified  <br/> |Un niveau d’autorisation a été modifié sur une collection de sites.  <br/> |
|Autorisations de site modifiées  <br/> |SitePermissionsModified  <br/> |L’administrateur de site ou le propriétaire (ou compte système) modifie le niveau d’autorisation affecté à un groupe sur un site. Cette activité est également consignée si toutes les autorisations sont supprimées d’un groupe.  <br/><br/> **Remarque**: cette opération a été déconseillée dans SharePoint Online. Pour rechercher des événements connexes, vous pouvez rechercher d’autres activités liées aux autorisations, telles que l’ajout d’un **administrateur de collection de sites**, l' **Ajout d’un utilisateur ou d’un groupe à un groupe SharePoint**, un **utilisateur autorisé à créer des groupes**, créé un **groupe**et **supprimé groupe.**|
|Niveau d’autorisation supprimé de la collection de sites  <br/> |PermissionLevelRemoved  <br/> |Un niveau d’autorisation a été supprimé d’une collection de sites.  <br/> |
|Administrateur de collection de sites supprimé  <br/> |SiteCollectionAdminRemoved <br/> |Le propriétaire ou l’administrateur de la collection de sites supprime une personne en tant qu’administrateur de collection de sites pour un site. Cette activité est également consignée lorsqu’un administrateur se retire de la liste des administrateurs de collection de sites pour le compte OneDrive d’un utilisateur (en modifiant le profil utilisateur dans le centre d’administration SharePoint).  Pour renvoyer cette activité dans les résultats de la recherche du journal d’audit, vous devez rechercher toutes les activités. <br/> |
|Suppression d’un utilisateur ou d’un groupe dans un groupe SharePoint  <br/> |RemovedFromGroup  <br/> |Un utilisateur a supprimé un membre ou un invité d’un groupe SharePoint. Il peut s’agir d’une action intentionnelle ou du résultat d’une autre activité, telle qu’un événement d’annulation de partage.  <br/> |
|Autorisations d’administrateur de site demandées  <br/> |SiteAdminChangeRequest  <br/> |Les demandes de l’utilisateur à ajouter en tant qu’administrateur de collection de sites pour une collection de sites. Les administrateurs de collection de sites disposent du niveau d’autorisation Contrôle total sur la collection de sites et tous les sous-sites.  <br/> |
|Héritage de partage restauré  <br/> |SharingInheritanceReset  <br/> |Une modification a été apportée afin qu’un élément hérite des autorisations de partage de son parent.  <br/> |
|Groupe mis à jour  <br/> |GroupUpdated  <br/> |L’administrateur de site ou le propriétaire modifie les paramètres d’un groupe pour un site. Cela peut inclure la modification du nom du groupe, qui peut consulter ou modifier l’appartenance au groupe et la gestion des demandes d’appartenance.  <br/> |
||||

  
### <a name="site-administration-activities"></a>Activités d’administration de site
  
Le tableau suivant répertorie les événements qui résultent de tâches d’administration de site dans SharePoint Online.
  
|**Nom convivial**|**Opération**|**Description**|
|:-----|:-----|:-----|
|Ajout de l’emplacement des données autorisées<br/>|AllowedDataLocationAdded|Un administrateur SharePoint ou global a ajouté un emplacement de données autorisé dans un environnement multi-géo. <br/>|
|Agent utilisateur exempté ajouté  <br/> |ExemptUserAgentSet  <br/> |Un administrateur SharePoint ou global a ajouté un agent utilisateur à la liste des agents utilisateurs exemptés dans le centre d’administration SharePoint.  <br/> |
|Ajout de l’administrateur de l’emplacement géographique<br/>|GeoAdminAdded<br/>|Un administrateur SharePoint ou global a ajouté un utilisateur en tant qu’administrateur géo d’un emplacement. <br/>|
|Utilisateur autorisé à créer des groupes  <br/> |AllowGroupCreationSet  <br/> |L’administrateur de site ou le propriétaire ajoute un niveau d’autorisation à un site qui lui permet de créer un groupe pour ce site.  <br/> |
|Déplacement géographique de site annulé  <br/> |SiteGeoMoveCancelled  <br/> |Un administrateur SharePoint ou global annule un déplacement géographique de site SharePoint ou OneDrive. La capacité multi-géo permet à une organisation Office 365 d’occuper plusieurs zones géographiques de centre de régions centres Office 365, appelées. Pour plus d’informations, reportez-vous à [capacités Multigéographiques dans OneDrive et SharePoint Online dans Office 365](https://go.microsoft.com/fwlink/?linkid=860840).  <br/> |
|Modification d’une stratégie de partage  <br/> |SharingPolicyChanged  <br/> |Un administrateur SharePoint ou global a modifié une stratégie de partage SharePoint à l’aide du portail d’administration d’Office 365, du portail d’administration SharePoint ou de SharePoint Online Management Shell. Toutes les modifications apportées aux paramètres de la stratégie de partage dans votre organisation seront consignées. La stratégie qui a été modifiée est identifiée dans le champ **ModifiedProperties** dans les propriétés détaillées de l’enregistrement d’événement.  <br/> |
|Stratégie d’accès aux appareils modifiée  <br/> |DeviceAccessPolicyChanged  <br/> |Un administrateur SharePoint ou global a modifié la stratégie périphériques non gérés pour votre organisation. Cette stratégie contrôle l’accès à SharePoint, OneDrive et Office 365 à partir d’appareils qui ne sont pas joints à votre organisation. La configuration de cette stratégie nécessite un abonnement Enterprise Mobility + Security. Pour plus d’informations, voir [Contrôler l’accès à partir des appareils non gérés](https://support.office.com/article/5ae550c4-bd20-4257-847b-5c20fb053622).  <br/> |
|Agents utilisateurs exemptés modifiés  <br/> |CustomizeExemptUsers  <br/> |Un administrateur SharePoint ou global A personnalisé la liste des agents utilisateurs exemptés dans le centre d’administration SharePoint. Vous pouvez spécifier les agents utilisateurs à exempter de la réception d’une page web entière à indexer. Cela signifie qu’un agent utilisateur que vous avez spécifié comme étant exempté rencontre un formulaire InfoPath, le formulaire est renvoyé sous la forme d’un fichier XML au lieu d’une page Web entière. Cela permet d’accélérer l’indexation des formulaires InfoPath.  <br/> |
|Stratégie d’accès réseau modifiée  <br/> |NetworkAccessPolicyChanged  <br/> |Un administrateur SharePoint ou global a modifié la stratégie d’accès basé sur l’emplacement (également appelée limite de réseau approuvée) dans le centre d’administration SharePoint ou à l’aide de SharePoint Online PowerShell. Ce type de stratégie permet aux utilisateurs d’accéder aux ressources SharePoint et OneDrive de votre organisation en fonction des plages d’adresses IP autorisées que vous spécifiez. Pour plus d’informations, reportez-vous à la rubrique [contrôler l’accès à SharePoint Online et aux données OneDrive en fonction de l’emplacement réseau](https://support.office.com/article/b5a5f1f1-1174-4c6b-91d0-9273a6b6971f).  <br/> |
|Déplacement géographique de site terminé  <br/> |SiteGeoMoveCompleted  <br/> |Un déplacement géographique de site qui a été planifié par un administrateur global dans votre organisation a été correctement effectué. La capacité multi-géo permet à une organisation Office 365 d’occuper plusieurs zones géographiques de centre de régions centres Office 365, appelées. Pour plus d’informations, reportez-vous à [capacités Multigéographiques dans OneDrive et SharePoint Online dans Office 365](https://go.microsoft.com/fwlink/?linkid=860840).  <br/> |
|Créé à la connexion  <br/> |SendToConnectionAdded  <br/> |Un administrateur SharePoint ou global crée une connexion envoyer à sur la page de gestion des enregistrements dans le centre d’administration SharePoint. Une connexion Envoyer à spécifie les paramètres pour un référentiel de documents ou un centre des enregistrements. Lorsque vous créez une connexion Envoyer à, un organisateur de contenu peut soumettre des documents à l’emplacement spécifié.  <br/> |
|Collection de sites créée  <br/> |SiteCollectionCreated  <br/> |Un administrateur SharePoint ou global crée une collection de sites dans votre organisation SharePoint Online ou un utilisateur met en service son site OneDrive entreprise.  <br/> |
|Site hub orphelin supprimé<br/>|HubSiteOrphanHubDeleted<br/>|Un administrateur SharePoint ou global a supprimé un site hub orphelin, qui est un site hub qui n’a aucun site associé. Un concentrateur orphelin est probablement dû à la suppression du site hub d’origine. <br/>|
|Suppression envoyée à la connexion  <br/> |SendToConnectionRemoved  <br/> |Un administrateur SharePoint ou global supprime une connexion envoyer à sur la page de gestion des enregistrements dans le centre d’administration SharePoint.  <br/> |
|Site supprimé  <br/> |SiteDeleted  <br/> |L’administrateur de site supprime un site.  <br/> |
|Aperçu du document activé  <br/> |PreviewModeEnabledSet  <br/> |L’administrateur de site Active l’aperçu de document pour un site.  <br/> |
|Flux de travail hérité activé  <br/> |LegacyWorkflowEnabledSet  <br/> |L’administrateur de site ou le propriétaire ajoute le type de contenu Tâche de flux de travail SharePoint 2013 au site. Les administrateurs globaux peuvent également activer des flux de travail pour l’organisation entière dans le Centre d’administration SharePoint.  <br/> |
|Office à la demande activé  <br/> |OfficeOnDemandSet  <br/> |L’administrateur de site active Office à la demande, qui permet aux utilisateurs d’accéder à la dernière version des applications de bureau Office. « Office à la demande » est activé dans le Centre d’administration SharePoint et nécessite un abonnement Office 365 qui inclut l’installation de l’ensemble des applications Office.  <br/> |
|Origine des résultats activée pour les recherches de personnes<br/>|PeopleResultsScopeSet<br/>|L’administrateur de site crée l’origine des résultats pour les recherches de personnes pour un site.<br/>|
|Flux RSS activés  <br/> |NewsFeedEnabledSet  <br/> |L’administrateur de site ou le propriétaire active les flux RSS pour un site. Les administrateurs généraux peuvent activer les flux RSS pour l’ensemble de l’organisation dans le Centre d’administration SharePoint.  <br/> |
|Site joint au site hub<br/>|HubSiteJoined<br/>|Un propriétaire de site associe son site à un site hub.<br/>|
|Site hub inscrit<br/>|HubSiteRegistered<br/>|Un administrateur SharePoint ou global crée un site hub. Les résultats sont que le site est inscrit en tant que site hub. <br/>|
|Suppression de l’emplacement des données autorisées<br/>|AllowedDataLocationDeleted<br/>|Un administrateur SharePoint ou global a supprimé un emplacement de données autorisé dans un environnement multi-géo.<br/>|
|Administrateur de l’emplacement géographique supprimé<br/>|GeoAdminDeleted<br/>|Un administrateur SharePoint ou global a supprimé un utilisateur en tant qu’administrateur géo d’un emplacement.<br/>|
|Site renommé  <br/> |SiteRenamed  <br/> |L’administrateur de site ou le propriétaire renomme un site  <br/> |
|Déplacement géographique de site planifié  <br/> |SiteGeoMoveScheduled  <br/> |Un administrateur SharePoint ou global planifie un déplacement géographique de site SharePoint ou OneDrive. La capacité multi-géo permet à une organisation Office 365 d’occuper plusieurs zones géographiques de centre de régions centres Office 365, appelées. Pour plus d’informations, reportez-vous à [capacités Multigéographiques dans OneDrive et SharePoint Online dans Office 365](https://go.microsoft.com/fwlink/?linkid=860840).  <br/> |
|Définir le site hôte  <br/> |HostSiteSet  <br/> |Un administrateur SharePoint ou global modifie le site désigné pour héberger les sites personnels ou OneDrive entreprise.  <br/> |
|Définir le quota de stockage pour l’emplacement géographique  <br/> |GeoQuotaAllocated<br/> |Un administrateur SharePoint ou global a configuré le quota de stockage pour un emplacement géographique dans un environnement multi-géo.<br/> |
|Site à partir d’un site hub<br/>|HubSiteUnjoined<br/>|Un propriétaire de site dissocie son site d’un site hub.<br/>|
|Site hub non enregistré<br/>|HubSiteUnregistered<br/>|Un administrateur SharePoint ou global annule l’inscription d’un site en tant que site hub. Lorsqu’un site Hub n’est pas enregistré, il ne fonctionne plus comme un site hub. <br/>|
||||
  
### <a name="exchange-mailbox-activities"></a>Activités de boîte aux lettres Exchange
  
Le tableau suivant répertorie les activités qui peuvent être consignées par l’enregistrement d’audit de boîte aux lettres. Les activités de boîte aux lettres effectuées par le propriétaire de la boîte aux lettres, un utilisateur délégué ou un administrateur sont automatiquement consignées dans le journal d’audit Office 365 pendant 90 jours. Un administrateur peut désactiver l’enregistrement d’audit des boîtes aux lettres pour tous les utilisateurs de votre organisation. Dans ce cas, aucune action de boîte aux lettres n’est enregistrée pour les utilisateurs. Pour plus d’informations, consultez la rubrique [Manage Mailbox Auditing](enable-mailbox-auditing.md).

 Vous pouvez également rechercher des activités de boîte aux lettres à l’aide de la cmdlet [Search-MailboxAuditLog](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/search-mailboxauditlog) dans Exchange Online PowerShell. 
  
|**Nom convivial**|**Opération**|**Description**|
|:-----|:-----|:-----|
|Ajout des autorisations de boîte aux lettres déléguée  <br/> |AddMailboxPermissions  <br/> |Un administrateur a attribué l’autorisation de boîte aux lettres FullAccess à un utilisateur (appelé délégué) à la boîte aux lettres d’une autre personne. L’autorisation FullAccess permet au délégué d’ouvrir la boîte aux lettres de l’autre personne, de lire et de gérer le contenu de la boîte aux lettres.  <br/> |
|Ajout ou suppression d’un utilisateur avec un accès délégué au dossier de calendrier<br/> |UpdateCalendarDelegation<br/> |Un utilisateur a été ajouté ou supprimé en tant que délégué du calendrier de la boîte aux lettres d’un autre utilisateur. La délégation de calendrier donne à une autre personne de la même organisation des autorisations pour gérer le calendrier du propriétaire de la boîte aux lettres. <br/> |
|Ajout d’autorisations au dossier<br/> |AddFolderPermissions<br/> |Une autorisation de dossier a été ajoutée. Les autorisations de dossier contrôlent les utilisateurs de votre organisation qui peuvent accéder aux dossiers d’une boîte aux lettres et aux messages qu’ils hébergent.<br/> |
|Messages copiés dans un autre dossier  <br/> |Copier  <br/> |Un message a été copié dans un autre dossier.  <br/> |
|Élément de boîte aux lettres créé  <br/> |Create  <br/> |Un élément est créé dans le dossier calendrier, contacts, notes ou tâches de la boîte aux lettres. Par exemple, une nouvelle demande de réunion est créée. La création, l’envoi ou la réception d’un message n’est pas audité. En outre, la création d’un dossier de boîte aux lettres n’est pas auditée.  <br/> |
|Création d’une nouvelle règle de boîte de réception dans Outlook Web App  <br/> |NewInboxRule<br/> |Un propriétaire de boîte aux lettres ou un autre utilisateur ayant accès à la boîte aux lettres A créé une règle de boîte de réception dans Outlook Web App.<br/> |
|Messages supprimés du dossier éléments supprimés  <br/> |SoftDelete  <br/> |Un message a été définitivement supprimé ou supprimé (récupérable) du dossier Éléments supprimés. Ces éléments sont déplacés vers le dossier éléments récupérables. Les messages sont également déplacés vers le dossier éléments récupérables lorsqu’un utilisateur le sélectionne et appuie sur **MAJ + SUPPR**.  <br/> |
|Message étiqueté en tant qu’enregistrement  <br/> |ApplyRecordLabel<br/> |Un message a été classé comme un enregistrement. Cela se produit lorsqu’une étiquette de rétention qui classifie le contenu en tant qu’enregistrement est manuellement ou automatiquement appliquée à un message.<br/> |
|Messages déplacés dans un autre dossier  <br/> |Déplacer  <br/> |Un message a été déplacé vers un autre dossier.  <br/> |
|Messages déplacés vers le dossier éléments supprimés  <br/> |MoveToDeletedItems  <br/> |Un message a été supprimé et déplacé vers le dossier Éléments supprimés.  <br/> |
|Autorisation de dossier modifiée  <br/> |UpdateFolderPermissions  <br/> |Une autorisation de dossier a été modifiée. Les autorisations de dossier contrôlent les utilisateurs de votre organisation qui peuvent accéder aux dossiers de boîte aux lettres et aux messages dans le dossier.  <br/> |
|Règle de boîte de réception modifiée à partir d’Outlook Web App<br/> |SetInboxRule<br/> |Un propriétaire de boîte aux lettres ou un autre utilisateur ayant accès à la boîte aux lettres A modifié une règle de boîte de réception à l’aide d’Outlook Web App.<br/> |
|Messages purgés de la boîte aux lettres  <br/> |HardDelete  <br/> |Un message a été purgé du dossier éléments récupérables (supprimé définitivement de la boîte aux lettres).  <br/> |
|Suppression des autorisations de boîte aux lettres déléguée  <br/> |Remove-MailboxPermission  <br/> |Un administrateur a supprimé l’autorisation FullAccess (qui a été affectée à un délégué) de la boîte aux lettres d’une personne. Après la suppression de l’autorisation FullAccess, le délégué ne peut pas ouvrir la boîte aux lettres de l’autre personne ou accéder à son contenu.  <br/> |
|Autorisations supprimées du dossier<br/> |RemoveFolderPermissions<br/> |Une autorisation de dossier a été supprimée. Les autorisations de dossier contrôlent les utilisateurs de votre organisation qui peuvent accéder aux dossiers d’une boîte aux lettres et aux messages qu’ils hébergent.<br/> |
|Message envoyé à l’aide des autorisations Envoyer en tant que  <br/> |SendAs  <br/> |Un message a été envoyé à l’aide de l’autorisation SendAs. Cela signifie qu’un autre utilisateur a envoyé le message comme s’il provenait du propriétaire de la boîte aux lettres.  <br/> |
|Message envoyé à l’aide des autorisations Envoyer de la part de  <br/> |SendOnBehalf  <br/> |Un message a été envoyé à l’aide de l’autorisation SendOnBehalf. Cela signifie qu’un autre utilisateur a envoyé le message au nom du propriétaire de la boîte aux lettres. Le message indique au destinataire de la part de qui le message a été envoyé et qui a envoyé réellement le message.  <br/> |
|Règles de boîte de réception mises à jour à partir du client Outlook<br/> |UpdateInboxRules<br/> |Un propriétaire de boîte aux lettres ou un autre utilisateur ayant accès à la boîte aux lettres A modifié une règle de boîte de réception dans le client Outlook.<br/> |
|Message mis à jour  <br/> |Update  <br/> |Un message ou ses propriétés ont été modifiés.  <br/> |
|L’utilisateur s’est connecté à la boîte aux lettres  <br/> |MailboxLogin  <br/> |L'utilisateur s'est connecté à sa boîte aux lettres.  <br/> |
||||

### <a name="sway-activities"></a>Activités Sway
  
Le tableau suivant répertorie les activités de l’utilisateur et de l’administrateur dans Sway. Sway est une application Office 365 qui permet aux utilisateurs de recueillir, de mettre en forme et de partager des idées, des histoires et des présentations sur un canevas interactif basé sur le Web. Pour plus d’informations, reportez-vous [aux questions fréquemment posées sur Sway-administrateur de l’aide](https://support.office.com/article/446380fa-25bf-47b2-996c-e12cb2f9d075).
  
|**Nom convivial**|**Opération**|**Description**|
|:-----|:-----|:-----|
|Niveau de partage Sway modifié  <br/> |SwayChangeShareLevel  <br/> |Un utilisateur modifie le niveau de partage d’un Sway. Cet événement capture l’utilisateur qui modifie l’étendue du partage associé à un Sway; par exemple, public par rapport à l’organisation.  <br/> |
|Sway créé  <br/> |SwayCreate  <br/> |Un utilisateur crée un Sway.  <br/> |
|Sway supprimé  <br/> |SwayDelete  <br/> |Un utilisateur supprime un Sway.  <br/> |
|Duplication Sway désactivée  <br/> |SwayDisableDuplication  <br/> |L’utilisateur désactive la duplication d’une instance Sway.  <br/> |
|Sway en double  <br/> |SwayDuplicate  <br/> |Un utilisateur duplique un Sway.  <br/> |
|Sway modifié  <br/> |SwayEdit  <br/> |Un utilisateur modifie un Sway.  <br/> |
|Duplication Sway activée  <br/> |EnableDuplication  <br/> |L’utilisateur active la duplication d’un Sway. La capacité d’un utilisateur à activer la duplication d’un Sway est activée par défaut.  <br/> |
|Partage Sway révoqué  <br/> |SwayRevokeShare  <br/> |Un utilisateur cesse de partager un Sway en révoquant l’accès à celui-ci. Révoquer l’accès modifie les liens associés à une instance Sway.  <br/> |
|Sway partagé  <br/> |SwayShare  <br/> |L’utilisateur a l’intention de partager un Sway. Cet événement capture l’action de l’utilisateur en cliquant sur une destination de partage spécifique dans le menu du partage Sway. L’événement n’indique pas si l’utilisateur a effectué l’action de partage.  <br/> |
|Désactivation du partage externe de Sway  <br/> |SwayExternalSharingOff  <br/> |L’administrateur désactive le partage d’Sway externe pour l’ensemble de l’organisation à l’aide du centre d’administration Microsoft 365.  <br/> |
|Partage externe de Sway activé  <br/> |SwayExternalSharingOn  <br/> |L’administrateur Active le partage d’Sway externe pour l’ensemble de l’organisation à l’aide du centre d’administration Microsoft 365.  <br/> |
|Service Sway désactivé  <br/> |SwayServiceOff  <br/> |L’administrateur désactive Sway pour l’ensemble de l’organisation à l’aide du centre d’administration Microsoft 365.  <br/> |
|Activé le service Sway  <br/> |SwayServiceOn  <br/> |L’administrateur Active Sway pour l’ensemble de l’organisation à l’aide du centre d’administration Microsoft 365 (le service Sway est activé par défaut).  <br/> |
|Sway visionné  <br/> |SwayView  <br/> |Un utilisateur visualise un Sway.  <br/> |
||||

  
### <a name="user-administration-activities"></a>Activités d’administration des utilisateurs
  
Le tableau suivant répertorie les activités d’administration des utilisateurs qui sont consignées lorsqu’un administrateur ajoute ou modifie un compte d’utilisateur à l’aide du centre d’administration Microsoft 365 ou du portail de gestion Azure.
  
|**Activité**|**Opération**|**Description**|
|:-----|:-----|:-----|
|Ajout de l’utilisateur  <br/> |Ajouter un utilisateur  <br/> |Un compte d’utilisateur Office 365 a été créé.  <br/> |
|Licence utilisateur modifiée  <br/> |Modifier la licence utilisateur  <br/> |La licence affectée à un utilisateur qui a changé. Pour voir les licences qui ont été modifiées, consultez l’activité **utilisateur mise à jour** correspondante.  <br/> |
|Mot de passe utilisateur modifié  <br/> |Modification mot de passe utilisateur  <br/> |Un administrateur a modifié le mot de passe d’un utilisateur.  <br/> |
|Utilisateur supprimé  <br/> |Supprimer un utilisateur  <br/> |Un compte d’utilisateur Office 365 a été supprimé.  <br/> |
|Réinitialiser le mot de passe utilisateur  <br/> |Réinitialiser le mot de passe utilisateur  <br/> |Administrateur réinitialisez le mot de passe d’un utilisateur.  <br/> |
|Propriété Set qui force l’utilisateur à modifier le mot de passe  <br/> |Définir le mot de passe utilisateur forcé  <br/> |Un administrateur définit la propriété qui force un utilisateur à modifier son mot de passe la prochaine fois qu’il se connecte à Office 365.  <br/> |
|Définir les propriétés de la licence  <br/> |Définir les propriétés de la licence  <br/> |L’administrateur modifie les propriétés d’une licence attribuée à un utilisateur.  <br/> |
|Utilisateur mis à jour  <br/> |Mettre à jour un utilisateur  <br/> |L’administrateur modifie une ou plusieurs propriétés d’un compte d’utilisateur. Pour obtenir la liste des propriétés de l’utilisateur qui peuvent être mises à jour, consultez la section «mettre à jour les attributs utilisateur» dans [Azure Active Directory audit report Events](https://go.microsoft.com/fwlink/p/?LinkID=616549).  <br/> |
||||
  
### <a name="azure-ad-group-administration-activities"></a>Activités d’administration du groupe Azure AD
  
Le tableau suivant répertorie les activités d’administration de groupe enregistrées lorsqu’un administrateur ou un utilisateur crée ou modifie un groupe Office 365 ou lorsqu’un administrateur crée un groupe de sécurité à l’aide du centre d’administration Microsoft 365 ou du portail de gestion Azure. Pour plus d’informations sur les groupes dans Office 365, reportez-vous à [la rubrique afficher, créer et supprimer des groupes dans le centre d’administration Microsoft 365](https://support.office.com/article/a6360120-2fc4-46af-b105-6a04dc5461c7).
  
|**Nom convivial**|**Opération**|**Description**|
|:-----|:-----|:-----|
|Ajout d’un groupe  <br/> |Ajouter un groupe  <br/> |Un groupe a été créé.  <br/> |
|Membre ajouté au groupe  <br/> |Ajouter un membre au groupe  <br/> |Un membre a été ajouté à un groupe.  <br/> |
|Groupe supprimé  <br/> |Supprimer un groupe  <br/> |Un groupe a été supprimé.  <br/> |
|Membre supprimé du groupe  <br/> |Supprimer un membre du groupe  <br/> |Un membre a été supprimé d’un groupe.  <br/> |
|Groupe mis à jour  <br/> |Mettre à jour un groupe  <br/> |Une propriété d’un groupe a été modifiée.  <br/> |
||||
   
### <a name="application-administration-activities"></a>Activités d’administration des applications
  
Le tableau suivant répertorie les activités d’administration des applications qui sont consignées lorsqu’un administrateur ajoute ou modifie une application inscrite dans Azure AD. Toutes les applications qui s’appuient sur Azure AD pour l’authentification doivent être enregistrées dans l’annuaire.
  
|**Nom convivial**|**Opération**|**Description**|
|:-----|:-----|:-----|
|Ajout de l’entrée de délégation  <br/> |Ajouter une entrée de délégation  <br/> |Une autorisation d’authentification a été créée/accordée à une application dans Azure AD.  <br/> |
|Ajout du principal de service  <br/> |Ajouter un principal de service  <br/> |Une application a été inscrite dans Azure AD. Une application est représentée par un principal de service dans l’annuaire.  <br/> |
|Ajout d’informations d’identification à un principal de service  <br/> |Ajouter des informations d’identification de principal de service  <br/> |Les informations d’identification ont été ajoutées à un principal de service dans Azure AD. Un principe de service représente une application dans l’annuaire.  <br/> |
|Entrée de délégation supprimée  <br/> |Supprimer une entrée de délégation  <br/> |Une autorisation d’authentification a été supprimée d’une application dans Azure AD.  <br/> |
|Suppression d’un principal de service du répertoire  <br/> |Supprimer le principal de service  <br/> |Une application a été supprimée/désinscrite d’Azure AD. Une application est représentée par un principal de service dans l’annuaire.  <br/> |
|Suppression des informations d’identification d’une entité de service  <br/> |Supprimer les informations d’identification du principal de service  <br/> |Les informations d’identification ont été supprimées d’une entité de service dans Azure AD. Un principe de service représente une application dans l’annuaire.  <br/> |
|Définir l’entrée de délégation  <br/> |Définir l’entrée de délégation  <br/> |Une autorisation d’authentification a été mise à jour pour une application dans Azure AD.  <br/> |
||||

### <a name="role-administration-activities"></a>Activités d’administration des rôles
  
Le tableau suivant répertorie les activités d’administration des rôles Azure AD qui sont consignées lorsqu’un administrateur gère les rôles d’administrateur dans le centre d’administration 365 de Microsoft ou dans le portail de gestion Azure.
  
|**Nom convivial**|**Opération**|**Description**|
|:-----|:-----|:-----|
|Ajouter un membre au rôle  <br/> |Ajouter un membre de rôle à un rôle  <br/> |Ajout d’un utilisateur à un rôle d’administrateur dans Office 365.  <br/> |
|Suppression d’un utilisateur d’un rôle d’annuaire  <br/> |Supprimer un membre de rôle d’un rôle  <br/> |Suppression d’un utilisateur d’un rôle d’administrateur dans Office 365.  <br/> |
|Définir les informations de contact de la société  <br/> |Définir les informations de contact de la société  <br/> |Mise à jour des préférences de contact au niveau de l’entreprise pour votre organisation Office 365. Cela inclut les adresses de messagerie pour les messages électroniques liés aux abonnements envoyés par Office 365, ainsi que les notifications techniques concernant les services 365 Office.  <br/> |
||||
   
### <a name="directory-administration-activities"></a>Activités d’administration d’annuaire
  
Le tableau suivant répertorie les activités de domaine et d’annuaire Azure AD qui sont consignées lorsqu’un administrateur gère son organisation Office 365 dans le centre d’administration Microsoft 365 ou dans le portail de gestion Azure.
  
|**Nom convivial**|**Opération**|**Description**|
|:-----|:-----|:-----|
|Ajout d’un domaine à la société  <br/> |Ajouter un domaine à la société  <br/> |Ajout d’un domaine à votre organisation Office 365.  <br/> |
|Ajout d’un partenaire au répertoire  <br/> |Ajouter un partenaire à la société  <br/> |Ajout d’un partenaire (administrateur délégué) à votre organisation Office 365.  <br/> |
|Domaine supprimé de la société  <br/> |Supprimer le domaine de la société  <br/> |Suppression d’un domaine de votre organisation Office 365.  <br/> |
|Suppression d’un partenaire du répertoire  <br/> |Supprimer le partenaire de la société  <br/> |Suppression d’un partenaire (administrateur délégué) de votre organisation Office 365.  <br/> |
|Définir les informations sur la société  <br/> |Définir les informations sur la société  <br/> |Mise à jour des informations relatives à la société de votre organisation Office 365. Cela inclut les adresses de messagerie pour les messages électroniques liés aux abonnements envoyés par Office 365, ainsi que les notifications techniques concernant les services 365 Office.  <br/> |
|Définir l’authentification de domaine  <br/> |Définir l’authentification de domaine  <br/> |Modification du paramètre d’authentification de domaine pour votre organisation Office 365.  <br/> |
|Mise à jour des paramètres de Fédération pour un domaine  <br/> |Définir les paramètres de Fédération sur le domaine  <br/> |Modification des paramètres de Fédération (partage externe) de votre organisation Office 365.  <br/> |
|Définir une stratégie de mot de passe  <br/> |Définir une stratégie de mot de passe  <br/> |Modification des contraintes de longueur et de caractère pour les mots de passe des utilisateurs dans votre organisation Office 365.  <br/> |
|Activation de la synchronisation Azure AD  <br/> |Définir l’indicateur DirSyncEnabled sur la société  <br/> |Définissez la propriété qui active un répertoire pour la synchronisation Azure AD.  <br/> |
|Domaine mis à jour  <br/> |Mettre à jour le domaine  <br/> |Mise à jour des paramètres d’un domaine dans votre organisation Office 365.  <br/> |
|Domaine vérifié  <br/> |Vérifier le domaine  <br/> |Vérifiez que votre organisation est le propriétaire d’un domaine-effectué.  <br/> |
|Domaine vérifié par courrier électronique vérifié  <br/> |Vérifier le domaine vérifié par courrier électronique  <br/> |Utilisation de la vérification du courrier électronique pour vérifier que votre organisation est le propriétaire d’un domaine.  <br/> |
||||
   
### <a name="ediscovery-activities"></a>activités eDiscovery
  
La recherche de contenu et les activités de découverte électronique effectuées dans le centre de sécurité et de conformité ou en exécutant les cmdlets PowerShell correspondantes sont consignées dans le journal d’audit. Cela inclut les activités suivantes:
  
- Création et gestion de cas eDiscovery
    
- Création, démarrage et modification de recherches de contenu
    
- Exécution d’actions de recherche de contenu, telles que l’aperçu, l’exportation et la suppression des résultats de recherche
    
- Configuration du filtrage des autorisations pour la recherche de contenu
    
- Gestion du rôle d’administrateur eDiscovery
    
Pour obtenir une liste et une description détaillée des activités eDiscovery journalisées, voir [Search for eDiscovery Activities dans le journal d’audit Office 365](search-for-ediscovery-activities-in-the-audit-log.md).
  
> [!NOTE]
> Les événements résultant des activités répertoriées sous **activités de découverte électronique** dans la liste déroulante **activités** doivent prendre jusqu’à 30 minutes pour être affichés dans les résultats de la recherche. À l’inverse, il faut 24 heures pour que les événements correspondants des activités de l’applet de commande eDiscovery apparaissent dans les résultats de la recherche. 
  
### <a name="advanced-ediscovery-activities"></a>Activités eDiscovery avancées

Le tableau suivant répertorie les activités qui résultent de l’informatique et des professionnels juridiques qui exécutent des tâches dans Advanced eDiscovery dans Microsoft 365. Pour plus d’informations, reportez-vous à [la rubrique vue d’ensemble de la solution EDiscovery avancée dans Microsoft 365](compliance20/overview-ediscovery-20.md).

|**Nom convivial**|**Opération**|**Description**|
|:-----|:-----|:-----|
| Ajout de données à un autre ensemble de vérification<br/>         | AddWorkingSetQueryToWorkingSet<br/>  |  L’utilisateur a ajouté des documents à partir d’un ensemble de réexamen à un autre ensemble de révision.<br/>|
| Ajout de données à l’ensemble de vérification <br/>                | AddQueryToWorkingSet<br/>            |  Un utilisateur a ajouté les résultats de la recherche d’une recherche de contenu associée à un cas avancé eDiscovery à un jeu de révision.<br/>|
| Ajout de données non Office 365 à l’ensemble de vérification<br/>  | AddNonOffice365DataToWorkingSet<br/> |  Un utilisateur a ajouté des données non Office 365 à un jeu de révision.<br/>|
| Ajout des documents corrigés à l’ensemble de la révision<br/> | AddRemediatedData<br/>               |  Un utilisateur télécharge des documents qui avaient des erreurs d’indexation qui ont été résolues en un jeu de révision.<br/>|
| Données analysées dans l’ensemble de révision <br/>             | RunAlgo<br/>                         |  L’utilisateur a exécuté l’analyse sur les documents dans un jeu de révision. <br/>|
| Document annoté dans l’ensemble de validation <br/>        | AnnotateDocument<br/>                |  L’utilisateur a annoté un document dans un jeu de révision. Annotation inclut le contenu redacting d’un document. <br/>|
| Jeux de charges comparés <br/>                      | LoadComparisonJob<br/>               |L’utilisateur compare deux jeux de charges différents dans un jeu de révision. Un jeu de charges est utilisé lorsque les données d’une recherche de contenu associées à la casse sont ajoutées à un jeu de révision.  <br/>|
| Documents biffés convertis au format PDF<br/>      | BurnJob<br/>                         |Un utilisateur a converti tous les documents biffés d’un jeu de réexamen en fichiers PDF.<br/>|
| Jeu de révision créé<br/>                       | CreateWorkingSet<br/>                |L’utilisateur a créé un jeu de révision.<br/>|
| Création de la recherche de jeu de révision<br/>                | CreateWorkingSetSearch<br/>          |Un utilisateur a créé une requête de recherche qui recherche les documents dans un jeu de révision. <br/>|
| Balise créée<br/>                              | CreateTag<br/>                       |Un utilisateur a créé un groupe de balises dans un jeu de révision. Un groupe de balises peut contenir une ou plusieurs balises enfants. Ces balises sont ensuite utilisées pour marquer des documents dans l’ensemble de révision.<br/>|
| Recherche de jeu de réexamens supprimée <br/>               | DeleteWorkingSetSearch<br/>          |Un utilisateur a supprimé une requête de recherche dans un jeu de révision.<br/>|
| Balise supprimée<br/>                              | DeleteTag<br/>                       |Un utilisateur a supprimé une balise ou un groupe de balises dans un jeu de révision.<br/>|
| Document téléchargé<br/>                      | DownloadDocument<br/>                |Un utilisateur a téléchargé un document à partir d’un jeu de révision.<br/>|
| Balise modifiée <br/>                              | DownloadDocument<br/>                |Un utilisateur a modifié une balise dans un jeu de révision.<br/>|
| Documents exportés à partir de l’ensemble de révision <br/>      | ExportJob<br/>                       |Les documents exportés par l’utilisateur à partir d’un ensemble de révision.<br/>|
| Paramètre case modifié <br/>                   | UpdateCaseSettings<br/>              | Un utilisateur a modifié les paramètres d’un cas. Les paramètres de cas incluent les informations de cas, les autorisations d’accès et les paramètres qui contrôlent le comportement de recherche et d’analyse.<br/>|
| Recherche de jeu de réexamen modifié<br/>               | UpdateWorkingSetSearch<br/>          |  Un utilisateur a modifié une requête de recherche dans un jeu de révision.<br/>|
| Recherche de jeu d’aperçu prévisualisée <br/>             | PreviewWorkingSetSearch<br/>         |  Un utilisateur a affiché un aperçu des résultats d’une requête de recherche dans un jeu de révision.<br/>|
| Documents d’erreur résolus <br/>              | ErrorRemediationJob<br/>             |  L’utilisateur corrige les fichiers contenant des erreurs d’indexation. <br/>|
| Document balisé<br/>                          | TagFiles<br/>                        |  Un utilisateur balise un document dans un ensemble de révision.<br/>|
| Résultats balisés d’une requête<br/>                | TagJob<br/>                          |  L’utilisateur balise tous les documents qui correspondent aux critères de la requête de recherche dans un jeu de révision.<br/>|
| Document affiché dans l’ensemble de validation<br/>            | ViewDocument<br/>                    |  Un utilisateur a affiché un document dans un jeu de révision.<br/>|
|||

### <a name="power-bi-activities"></a>Activités Power BI
  
Vous pouvez rechercher des activités dans Power BI dans le journal d’audit. Pour plus d’informations sur les activités Power BI, voir la section «activités auditées par Power BI» dans utilisation de l' [audit au sein de votre organisation](https://docs.microsoft.com/power-bi/service-admin-auditing#activities-audited-by-power-bi).
  
L’enregistrement d’audit pour Power BI n’est pas activé par défaut. Pour rechercher des activités Power BI dans le journal d’audit Office 365, vous devez activer l’audit dans le portail d’administration de Power BI. Pour obtenir des instructions, consultez la section «journaux d’audit» dans le [portail d’administration Power bi](https://docs.microsoft.com/power-bi/service-admin-portal#audit-logs).
  
### <a name="microsoft-workplace-analytics-activities"></a>Activités de Microsoft Workplace Analytics

Workplace Analytics explique comment les groupes collaborent dans votre organisation Office 365. Le tableau suivant répertorie les activités effectuées par les utilisateurs auxquels sont attribués le rôle d’administrateur ou les rôles d’analyste dans Workplace Analytics. Les utilisateurs auxquels le rôle d’analyste a été attribué ont un accès total à toutes les fonctionnalités de service et utilisent le produit pour effectuer l’analyse. Les utilisateurs auxquels le rôle administrateur est affecté peuvent configurer les paramètres de confidentialité et les valeurs par défaut du système, et peuvent préparer, télécharger et vérifier les données organisationnelles dans Workplace Analytics. Pour plus d'informations, consultez l'article [Workplace Analytics](https://docs.microsoft.com/en-us/workplace-analytics/index-orig).

|**Nom convivial**|**Opération**|**Description**|
|:-----|:-----|:-----|
|Lien OData accédé <br/> |AccessedOdataLink <br/> |Les analystes ont accédé au lien OData pour une requête.|
|Requête annulée <br/> |CanceledQuery <br/> |Un analyste a annulé une requête en cours d’exécution.|
|Exclusion de la réunion créée <br/> |MeetingExclusionCreated <br/> |Un analyste a créé une règle d’exclusion de réunion.|
|Résultat supprimé <br/> |DeletedResult <br/> |Un analyste a supprimé un résultat de requête.|
|Rapport téléchargé <br/> |DownloadedReport <br/> |Un analyste a téléchargé un fichier de résultats de requête.|
|Requête exécutée <br/> |ExecutedQuery <br/> |Un analyste a exécuté une requête.|
|Paramètre d’accès aux données mis à jour <br/> |UpdatedDataAccessSetting <br/> |Paramètres d’accès aux données mis à jour par l’administrateur.|
|Paramètre de confidentialité mis à jour <br/> |UpdatedPrivacySetting <br/> |Paramètres de confidentialité mis à jour par l’administrateur; par exemple, taille de groupe minimale.|
|Données d’organisation téléchargées <br/> |UploadedOrgData <br/> |Administrateur chargé le fichier de données de l’organisation.|
|Exploration affichée <br/> |ViewedExplore <br/> |Analyst a consulté les visualisations dans un ou plusieurs onglets de page Explorer.|
||||

### <a name="microsoft-teams-activities"></a>Activités de Microsoft teams
  
Le tableau suivant répertorie les activités de l’utilisateur et de l’administrateur dans Microsoft teams qui sont consignées dans le journal d’audit Office 365. Microsoft teams est un espace de travail centré sur la conversation dans Office 365. Il permet d’associer des conversations, des réunions, des fichiers et des notes d’une équipe à un seul endroit. Pour plus d’informations et des liens vers des rubriques d’aide, voir:
  
- [Forum aux questions sur Microsoft teams-aide de l’administrateur](https://support.office.com/article/05cbe533-2181-4e95-a4b0-52cd7695fafc)
    
- [Aide de Microsoft teams](https://support.office.com/article/23156c0c-2c6e-49dd-8b7b-7c564b76508c)
    
|**Nom convivial**|**Opération**|**Description**|
|:-----|:-----|:-----|
|Ajout de bot à Team  <br/> |BotAddedToTeam  <br/> |Un utilisateur ajoute un bot à une équipe.  <br/> |
|Canal ajouté  <br/> |ChannelAdded  <br/> |Un utilisateur ajoute un canal à une équipe.  <br/> |
|Connecteur ajouté  <br/> |ConnectorAdded  <br/> |Un utilisateur ajoute un connecteur à un canal.  <br/> |
|Ajouté des membres à l’équipe  <br/> |MemberAdded  <br/> |Un propriétaire d’équipe ajoute des membres à une équipe.  <br/> |
|Onglet ajouté  <br/> |TabAdded  <br/> |Un utilisateur ajoute un onglet à un canal.  <br/> |
|Paramètre de canal modifié  <br/> |ChannelSettingChanged  <br/> | L’opération ChannelSettingChanged est enregistrée lorsque les activités suivantes sont effectuées par un membre de l’équipe. Pour chacune de ces activités, une description du paramètre modifié (indiqué entre parenthèses ci-dessous) s’affiche dans la colonne **élément** des résultats de la recherche du journal d’audit.  <br/> <br/>-Modifie le nom d’un canal d’équipe (**nom de canal**).  <br/>  <br/>-Modifie la description d’un canal d’équipe (**Description de canal**).  <br/> |
|Paramètres de l’organisation modifiés  <br/> |TeamsTenantSettingChanged  <br/> | L’opération TeamsTenantSettingChanged est enregistrée lorsque les activités suivantes sont effectuées par un administrateur global (à l’aide du centre d’administration Microsoft 365); Notez que ces activités affectent les paramètres de Microsoft teams à l’échelle de l’organisation. Pour plus d’informations, consultez la rubrique [paramètres d’administration de Microsoft teams](https://support.office.com/article/3966a3f5-7e0f-4ea9-a402-41888f455ba2).  <br/>  Pour chacune de ces activités, une description du paramètre modifié (indiqué entre parenthèses ci-dessous) s’affiche dans la colonne **élément** des résultats de la recherche du journal d’audit.  <br/><br/>-Active ou désactive Microsoft teams pour l’organisation (**Microsoft teams**).  <br/><br/>-Active ou désactive l’interopérabilité entre Microsoft teams et Skype entreprise pour l’organisation (interopérabilité de**Skype entreprise**).<br/><br/>-Active ou désactive l’affichage graphique de l’organisation dans les clients Microsoft Teams (affichage Organigramme hiérarchique **).  - <br/>ou désactive la possibilité pour les membres de l’équipe de planifier des réunions privées (planification des réunions privées <br/>****).  - <br/>ou désactive la possibilité pour les membres de l’équipe de planifier des réunions de canal (planification des réunions de canal <br/>**).  <br/><br/>-Active ou désactive les appels vidéo dans les réunions Teams (vidéo pour les réunions Skype **).  - <br/>ou désactive le partage d’écran dans Microsoft teams meetups pour l’organisation (partage d’écran pour les réunions Skype <br/>****).  - <br/>ou désactive la possibilité d’ajouter des images animées (appelées images giphy) aux conversations en équipe (images animées <br/>**).  <br/><br/>-Modifie le paramètre de contrôle d’accès au contenu de l’organisation (**contrôle d’accès au contenu**). La notation de contenu limite le type d’image animée qui peut être affichée dans les conversations.  <br/><br/>-Active ou désactive la possibilité pour les membres de l’équipe d’ajouter des images personnalisables (appelées mèmes pour personnalisées) à partir d’Internet vers des conversations d’équipe (images personnalisables à partir d’Internet **).  - <br/>ou désactive la possibilité pour les membres de l’équipe d’ajouter des images modifiables (appelées autocollants) à des conversations d’équipe (images modifiables <br/>****). - <br/>ou désactive la possibilité pour les membres de l’équipe d’utiliser des robots dans les conversations et les canaux de Microsoft Teams (bots à l’échelle de l’organisation <br/>**).<br/><br/>-Active des robots spécifiques pour Microsoft Teams. Cela n’inclut pas le T-bot, qui est le robot d’aide de teams, disponible lorsque les robots sont activés pour l’organisation (**robots individuels**).  <br/><br/>-Active ou désactive la possibilité pour les membres de l’équipe d’ajouter des extensions ou des onglets (**extensions ou tabulations**).  <br/><br/>-Active ou désactive le chargement de partie des robots propriétaires pour Microsoft Teams (**chargement latéral des robots**).  <br/><br/>-Active ou désactive la possibilité pour les utilisateurs d’envoyer des messages électroniques à un canal Microsoft Teams (**courrier électronique de canal**).  <br/> |
|Modification du rôle des membres dans l’équipe  <br/> |MemberRoleChanged  <br/> |Un propriétaire d’équipe modifie le rôle des membres d’une équipe. Les valeurs suivantes indiquent le type de rôle affecté à l’utilisateur.  <br/><br/><br/> **1** -indique le rôle de propriétaire.<br/>**2** -indique le rôle de membre. <br/>**3** -indique le rôle invité. <br/>La propriété Members inclut également le nom de votre organisation et l’adresse de messagerie du membre.  <br/> |
|Modification du paramètre d’équipe  <br/> |TeamSettingChanged  <br/> | L’opération TeamSettingChanged est enregistrée lorsque les activités suivantes sont effectuées par un propriétaire d’équipe. Pour chacune de ces activités, une description du paramètre modifié (indiqué entre parenthèses ci-dessous) s’affiche dans la colonne **élément** des résultats de la recherche du journal d’audit.  <br/><br/>-Modifie le type d’accès d’une équipe. Les équipes peuvent être définies comme étant privées ou publiques (**type d’accès à l’équipe**). Lorsqu’une équipe est privée (paramètre par défaut), les utilisateurs peuvent accéder à l’équipe uniquement par invitation. Lorsqu’une équipe est publique, elle est découvrable par tout le monde.  <br/><br/>-Modifie la classification des informations d’une équipe (**classification d’équipe**).  <br/>  Par exemple, les données d’équipe peuvent être classées comme un impact élevé sur l’entreprise, une incidence moyenne entreprise ou un faible impact sur l’activité.<br/><br/>-Modifie le nom d’une équipe (**nom**de l’équipe).  <br/><br/>-Modifie la description de l’équipe (description de l’équipe * *). <br/><br/>-Modifications apportées à l’un des paramètres d’équipe. Un propriétaire d’équipe peut accéder à ces paramètres dans un client teams en cliquant avec le bouton droit sur une équipe, en cliquant sur **gérer l’équipe**, puis en cliquant sur l’onglet **paramètres** . Pour ces activités, le nom du paramètre modifié est affiché dans la colonne **élément** dans les résultats de la recherche du journal d’audit.  <br/> |
|Équipe créée  <br/> |TeamCreated  <br/> |Un utilisateur crée une équipe.  <br/> |
|Canal supprimé  <br/> |ChannelDeleted  <br/> |Un utilisateur supprime un canal d’une équipe.  <br/> |
|Équipe supprimée  <br/> |TeamDeleted  <br/> |Un propriétaire d’équipe supprime une équipe.  <br/> |
|Robot supprimé de Team  <br/> |BotRemovedFromTeam  <br/> |Un utilisateur supprime un bot d’une équipe.  <br/> |
|Connecteur supprimé  <br/> |ConnectorRemoved  <br/> |Un utilisateur supprime le connecteur d’un canal.  <br/> |
|Suppression des membres de l’équipe  <br/> |MemberRemoved  <br/> |Un propriétaire d’équipe supprime les membres d’une équipe.  <br/> |
|Onglet supprimé  <br/> |TabRemoved  <br/> |Un utilisateur supprime un onglet d’un canal.  <br/> |
|Connecteur mis à jour  <br/> |ConnectorUpdated  <br/> |Un utilisateur a modifié un connecteur dans un canal.  <br/> |
|Onglet mis à jour  <br/> |TabUpdated  <br/> |Un utilisateur a modifié un onglet dans un canal.  <br/> |
|L’utilisateur s’est connecté à teams  <br/> |TeamsSessionStarted  <br/> |Un utilisateur se connecte à un client Microsoft Teams.  <br/> |
||||

### <a name="yammer-activities"></a>Activités Yammer
  
Le tableau suivant répertorie les activités de l’utilisateur et de l’administrateur dans Yammer qui sont consignées dans le journal d’audit Office 365. Pour renvoyer des activités liées à Yammer à partir du journal d’audit Office 365, vous devez sélectionner **afficher les résultats pour toutes les activités** dans la liste **activités** . Utilisez les zones plage de dates et la liste **utilisateurs** pour affiner les résultats de la recherche. 
  
|**Nom convivial**|**Opération**|**Description**|
|:-----|:-----|:-----|
|Stratégie de rétention des données modifiée  <br/> |SoftDeleteSettingsUpdated  <br/> |Le paramètre administrateur vérifié met à jour les paramètres de la stratégie de rétention des données réseau sur suppression matérielle ou suppression logicielle. Seuls les administrateurs vérifiés peuvent effectuer cette opération.  <br/> |
|Modification de la configuration réseau  <br/> |NetworkConfigurationUpdated  <br/> |Le réseau ou l’administrateur vérifié modifie la configuration du réseau Yammer. Cela inclut la définition de l’intervalle pour l’exportation des données et l’activation de la conversation.  <br/> |
|Modification des paramètres de profil réseau  <br/> |ProcessProfileFields  <br/> |Le réseau ou l’administrateur vérifié modifie les informations qui apparaissent sur les profils des membres pour le réseau des utilisateurs réseau.  <br/> |
|Mode de contenu privé modifié  <br/> |SupervisorAdminToggled  <br/> |L’administrateur a vérifié qu’il active ou désactive le *mode de contenu privé* . Ce mode permet à un administrateur d’afficher les publications dans les groupes privés et d’afficher les messages privés entre des utilisateurs individuels (ou des groupes d’utilisateurs). Seuls les administrateurs vérifiés peuvent effectuer cette opération.  <br/> |
|Configuration de la sécurité modifiée  <br/> |NetworkSecurityConfigurationUpdated  <br/> |L’administrateur a vérifié la mise à jour de la configuration de sécurité du réseau Yammer. Cela inclut la définition des stratégies d’expiration de mot de passe et des restrictions sur les adresses IP. Seuls les administrateurs vérifiés peuvent effectuer cette opération.  <br/> |
|Fichier créé  <br/> |FileCreated  <br/> |Un utilisateur télécharge un fichier.  <br/> |
|Groupe créé  <br/> |GroupCreation  <br/> |Un utilisateur crée un groupe.  <br/> |
|Groupe supprimé  <br/> |GroupDeletion  <br/> |Un groupe est supprimé de Yammer.  <br/> |
|Message supprimé  <br/> |MessageDeleted  <br/> |Un utilisateur supprime un message.  <br/> |
|Fichier téléchargé  <br/> |FileDownloaded  <br/> |Un utilisateur télécharge un fichier.  <br/> |
|Données exportées  <br/> |DataExport  <br/> |L’administrateur vérifié exporte les données réseau Yammer. Seuls les administrateurs vérifiés peuvent effectuer cette opération.  <br/> |
|Fichier partagé  <br/> |FileShared  <br/> |Un utilisateur partage un fichier avec un autre utilisateur.  <br/> |
|Utilisateur réseau suspendu  <br/> |NetworkUserSuspended  <br/> |Le réseau ou l’administrateur vérifié suspend (désactive) un utilisateur à partir de Yammer.  <br/> |
|Utilisateur suspendu  <br/> |UserSuspension  <br/> |Le compte d’utilisateur est suspendu (désactivé).  <br/> |
|Description du fichier mis à jour  <br/> |FileUpdateDescription  <br/> |Un utilisateur modifie la description d’un fichier.  <br/> |
|Nom de fichier mis à jour  <br/> |FileUpdateName  <br/> |Un utilisateur modifie le nom d’un fichier.  <br/> |
|Fichier affiché  <br/> |FileVisited  <br/> |Un utilisateur visualise un fichier.  <br/> |
||||
   
### <a name="microsoft-flow-activities"></a>Activités de flux Microsoft

Vous pouvez rechercher des activités dans le journal d’audit dans Microsoft Flow. Ces activités incluent la création, la modification et la suppression de flux, ainsi que la modification des autorisations de flux. Pour plus d’informations sur l’audit des activités de flux, reportez-vous au blog [Microsoft Flow audit Events now available in Security & Compliance Center](https://flow.microsoft.com/blog/security-and-compliance-center).

### <a name="microsoft-powerapps"></a>Microsoft PowerApps

Vous pouvez rechercher dans le journal d’audit les activités liées à l’application dans les PowerApp. Ces activités incluent la création, le lancement et la publication d’une application. L’attribution d’autorisations aux applications est également auditée. Pour obtenir une description de toutes les activités PowerApp, consultez la rubrique [journalisation des activités pour les PowerApp](https://docs.microsoft.com/en-us/power-platform/admin/logging-powerapps#what-events-are-audited).

### <a name="microsoft-stream-activities"></a>Activités de Microsoft Stream
  
Vous pouvez rechercher des activités dans le journal d’audit dans Microsoft Stream. Ces activités incluent les activités vidéo effectuées par les utilisateurs, les activités de canal de groupe et les activités d’administration telles que la gestion des utilisateurs, la gestion des paramètres de l’organisation et l’exportation des rapports. Pour obtenir une description de ces activités, reportez-vous à la section «activités enregistrées dans Microsoft Stream» dans [journaux d’audit dans Microsoft Stream](https://docs.microsoft.com/stream/audit-logs).

### <a name="exchange-admin-audit-log"></a>Journal d’audit de l’administrateur Exchange
  
La journalisation d’audit de l’administrateur Exchange (activée par défaut dans Office 365) consigne un événement dans le journal d’audit d’Office 365 lorsqu’un administrateur (ou un utilisateur auquel des autorisations d’administration ont été affectées) apporte une modification dans votre organisation Exchange Online. Les modifications apportées à l’aide du centre d’administration Exchange ou de l’exécution d’une cmdlet dans Exchange Online PowerShell sont consignées dans le journal d’audit de l’administrateur Exchange. Les cmdlets qui commencent par les verbes **Get**, **Search-** ou **test-** ne sont pas enregistrées dans le journal d’audit Office 365. Pour plus d’informations sur la journalisation d’audit de l’administrateur dans Exchange, consultez la rubrique [enregistrement d’audit de l’administrateur](https://go.microsoft.com/fwlink/p/?LinkID=619225).

> [!IMPORTANT]
> Certaines cmdlets Exchange Online qui ne sont pas consignées dans le journal d’audit de l’administrateur Exchange (ou dans le journal d’audit Office 365). Un grand nombre de ces cmdlets sont liées à la maintenance du service Exchange Online et sont exécutées par le personnel du centre de gestion de Microsoft ou des comptes de service. Ces applets de commande ne sont pas enregistrées, car elles entraîneraient un grand nombre d’événements d’audit «bruyants». S’il existe une applet de commande Exchange Online qui n’est pas auditée, soumettez une suggestion au Forum de la voix de l’utilisateur de la [& sécurité d’Office 365](https://office365.uservoice.com/forums/289138-office-365-security-compliance) et demandez-lui d’activer l’audit. Vous pouvez également soumettre une demande de modification de conception (DCR) au support Microsoft.
  
Voici quelques conseils pour rechercher des activités d’administration d’Exchange lors de la recherche dans le journal d’audit Office 365:
  
- Pour renvoyer des entrées à partir du journal d’audit de l’administrateur Exchange, vous devez sélectionner **afficher les résultats pour toutes les activités** dans la liste **activités** . Utilisez les zones plage de dates et la liste **utilisateurs** pour affiner les résultats de recherche pour les cmdlets exécutées par un administrateur Exchange spécifique dans une plage de dates spécifique. 
    
- Pour afficher les événements du journal d’audit de l’administrateur Exchange, filtrez les résultats **-** de la recherche et tapez a (tiret) dans la zone filtre d' **activité** . Cette opération affiche les noms des cmdlets, qui s’affichent dans la colonne **activité** pour les événements d’administration Exchange. Vous pouvez ensuite trier les noms des applets de commande par ordre alphabétique. 
    
    ![Tapez un tiret dans la zone activités pour filtrer les événements d’administration Exchange.](media/7628e7aa-6263-474a-a28b-2dcf5694bb27.png)
  
- Pour obtenir des informations sur la cmdlet qui a été exécutée, les paramètres et les valeurs des paramètres qui ont été utilisés, ainsi que les objets affectés, vous pouvez exporter les résultats de la recherche en sélectionnant l’option **Télécharger tous les résultats** . Pour plus d’informations, consultez la rubrique [Exporter, configurer et afficher les enregistrements du journal d’audit](export-view-audit-log-records.md). 
    
- Vous pouvez également utiliser la `Search-UnifiedAuditLog -RecordType ExchangeAdmin` commande dans Exchange Online PowerShell pour renvoyer uniquement des enregistrements d’audit à partir du journal d’audit de l’administrateur Exchange. Une applet de commande Exchange est exécutée pour que l’entrée du journal d’audit correspondante soit renvoyée dans les résultats de la recherche. Pour plus d’informations, consultez la rubrique [Search-UnifiedAuditLog](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/search-unifiedauditlog). Pour plus d’informations sur l’exportation des résultats de la recherche renvoyés par la cmdlet **Search-UnifiedAuditLog** dans un fichier CSV, consultez la section «conseils pour l’exportation et l’affichage du journal d’audit» dans [Exporter, configurer et afficher les enregistrements du journal d’audit](export-view-audit-log-records.md#tips-for-exporting-and-viewing-the-audit-log).

- Vous pouvez également afficher les événements dans le journal d’audit de l’administrateur Exchange à l’aide du centre d’administration Exchange ou en exécutant la commande **Search-AdminAuditLog** dans Exchange Online PowerShell. Pour obtenir des instructions, voir :
   - [Affichez le journal d’audit de l’administrateur](https://technet.microsoft.com/library/dn342832%28v=exchg.150%29.aspx). 
   
   -  [Search-AdminAuditLog](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/search-adminauditlog)
   
   N’oubliez pas que les mêmes activités d’administration Exchange sont consignées dans le journal d’audit de l’administrateur Exchange et dans le journal d’audit Office 365.
  
## <a name="frequently-asked-questions"></a>Questions fréquemment posées

**Où puis-je trouver des informations sur les fonctionnalités offertes par le service d’audit dans Office 365?**

Pour plus d’informations sur les fonctionnalités d’audit et de création de rapports disponibles dans Office 365, consultez la rubrique [Auditing and Reporting in office 365](office-365-auditing-and-reporting-overview.md). 

**Quels sont les différents services Office 365 actuellement audités?**

Les services Office 365 les plus utilisés tels qu’Exchange Online, SharePoint Online, OneDrive entreprise, Azure Active Directory, Microsoft Teams, Dynamics 365, Advanced Threat Protection et Power BI sont audités. Consultez le [début de cet article](search-the-audit-log-in-security-and-compliance.md) pour obtenir la liste des services qui sont audités.

**Quelles sont les activités auditées par le service d’audit dans Office 365?**

Consultez la section [activités auditées](#audited-activities) de cet article pour obtenir la liste et la description des activités auditées dans Office 365.

**Combien de temps faut-il pour qu’un enregistrement d’audit soit disponible après la survenue d’un événement?**

La plupart des données d’audit sont disponibles dans les 30 minutes, mais cela peut prendre jusqu’à 24 heures après l’affichage d’un événement pour que l’entrée du journal d’audit correspondante s’affiche dans les résultats de la recherche. Reportez-vous au tableau de la section [avant de commencer](#before-you-begin) de cet article pour afficher le temps nécessaire pour que les événements dans les différents services Office 365 soient disponibles.

**Pendant combien de temps les enregistrements d’audit sont-ils conservés?**

Comme indiqué précédemment, la période de rétention des enregistrements d’audit dépend de l’abonnement Office 365 de votre organisation.  

- **Office 365 E3:** Les enregistrements d’audit sont conservés pendant 90 jours.

- **Office 365 E5:** Les enregistrements d’audit sont également conservés pendant 90 jours. La conservation des enregistrements d’audit pendant un an peut être finalement disponible pour les utilisateurs et utilisateurs E5 avec une licence E3 et une licence de complément Office 365 Advanced Compliance.

     > [!NOTE]
     > Comme expliqué précédemment, le programme d’aperçu privé de la période de rétention d’un an pour les enregistrements d’audit pour E5 organisations (ou les organisations E3 avec des licences de complément de conformité avancées) est fermé à nouveau. Cet article sera mis à jour lorsque la période de rétention d’un an est disponible en préversion publique ou publiée pour une disponibilité générale.

Notez également que la durée de la période de rétention des enregistrements d’audit est basée sur une licence par utilisateur. Par exemple, si un utilisateur de votre organisation reçoit une licence Office 365 E3 ou E5, les enregistrements d’audit pour les activités effectuées par cet utilisateur sont conservés pendant 90 jours.

**Puis-je accéder aux données d’audit par programmation?**

Oui. L’API activité de gestion d’Office 365 est utilisée pour extraire les journaux d’audit par programme.  Pour commencer, consultez la rubrique [prise en main des API de gestion d’Office 365](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).

**Existe-t-il d’autres méthodes pour obtenir des journaux d’audit autres que l’utilisation du centre de sécurité et de conformité ou l’API activité de gestion d’Office 365?**

Non. Il s’agit des deux méthodes permettant d’obtenir des données à partir du service d’audit Office 365. 

**Dois-je activer individuellement l’audit dans chaque service pour lequel je souhaite capturer les journaux d’audit?**

Dans la plupart des services Office 365, l’audit est activé par défaut après l’activation initiale de l’audit de votre organisation Office 365 (comme décrit dans la section [avant de commencer](#before-you-begin) , dans cet article).

**Le service d’audit Office 365 prend-il en charge la déduplication des enregistrements?**

Non. Le pipeline service d’audit est quasiment en temps réel et ne peut donc pas prendre en charge la déduplication.
 
**Est-ce que le flux de données d’audit Office 365 entre les régions géographiques?**

Non. Nous disposons actuellement de déploiements de pipeline d’audit dans les régions NA (Amérique du Nord), EMEA (Europe, Moyen-Orient et Afrique) et APAC (Asie Pacifique). Toutefois, nous pouvons transmettre les données dans ces régions pour l’équilibrage de charge et uniquement lors des problèmes de site réel. Lorsque nous effectuons ces activités, les données en transit sont chiffrées.   
 
**Les données d’audit sont-elles chiffrées?**

Les données d’audit sont stockées dans les boîtes aux lettres Exchange (données au repos) dans la région où le pipeline d’audit est déployé. Ces données ne sont pas chiffrées. Toutefois, les données en transit sont toujours chiffrées. 
