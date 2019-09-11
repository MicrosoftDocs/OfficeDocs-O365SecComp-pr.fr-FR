---
title: 'Effectuer des recherches dans le journal d’audit depuis le Centre de sécurité et conformité '
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 0d4d0f35-390b-4518-800e-0c7ec95e946c
description: "Utilisez le Centre de sécurité et conformité pour rechercher dans le journal d’audit unifié les activités des utilisateurs et des administrateurs de votre organisation Office 365.\n "
ms.openlocfilehash: f10c6b488683201a2980702cc83efe97bf54f046
ms.sourcegitcommit: 50a2654d6d56249c3f836607f436446049be7833
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/11/2019
ms.locfileid: "36838164"
---
# <a name="search-the-audit-log-in-the-security--compliance-center"></a>Effectuer des recherches dans le journal d’audit depuis le Centre de sécurité et conformité 

## <a name="introduction"></a>Introduction

Vous avez besoin de déterminer si un utilisateur a consulté un document spécifique ou supprimé définitivement un élément de sa boîte aux lettres ? Si c’est le cas, vous pouvez utiliser le Centre de sécurité &amp; conformité Office 365 pour rechercher dans le journal d’audit unifié les activités des utilisateurs et des administrateurs de votre organisation Office 365.
 Qu’est-ce qu’un journal d’audit unifié ? Un tel journal permet de rechercher les types suivants d’activité des utilisateurs et administrateurs dans Office 365 :

- Activité utilisateur dans SharePoint Online et OneDrive Entreprise

- Activité utilisateur dans Exchange Online (enregistrement d’audit de boîte aux lettres Exchange) 

- Activité des administrateurs dans SharePoint Online

- Activité des administrateurs dans Azure Active Directory (service d’annuaire pour Office 365)

- Activité des administrateurs dans Exchange Online (journalisation d’audit de l’administrateur Exchange)

- Activités utilisateur et administrateur dans Sway

- Activités eDiscovery dans le Centre de conformité et sécurité

- Activités utilisateur et administrateur dans Power BI

- Activités utilisateur et administrateur dans Microsoft Teams

- Activités utilisateur et administrateur dans Dynamics 365

- Activités utilisateur et administrateur dans Yammer

- Activités utilisateur et administrateur dans Microsoft Flow

- Activités utilisateur et administrateur dans Microsoft Stream

- Activité d’analystes et d’administrateurs dans Microsoft Workplace Analytics

- Activités utilisateur et administrateur dans Microsoft PowerApps

## <a name="before-you-begin"></a>Avant de commencer

Avant de commencer à effectuer une recherche dans le journal d’audit d’Office 365, veillez à lire ce qui suit.

- Vous (ou un autre administrateur) devez activer l’enregistrement d’audit avant d’effectuer des recherches dans le journal d’audit Office 365. Pour cela, cliquez sur **Commencer à enregistrer les activités des utilisateurs et des administrateurs** sur la page **Recherche dans le journal d’audit** du Centre de sécurité et de conformité. (Si vous ne voyez pas ce lien, l’audit est déjà activé dans votre organisation.). Une fois l’audit activé, le message qui apparaît indique que le journal d’audit est en cours de préparation et que vous pourrez effectuer une recherche environ deux heures après la fin de la préparation. Vous ne devez effectuer cette opération qu’une seule fois.

  > [!NOTE]
  > Nous effectuons la procédure nécessaire pour activer l’audit par défaut. En attendant, vous pouvez l’activer en suivant la procédure décrite précédemment.

- Vous devez avoir le rôle Journaux d’audit en affichage seul ou Journaux d’audit dans Exchange Online pour pouvoir effectuer des recherches dans le journal d’audit Office 365. Par défaut, ces rôles sont affectés aux groupes de rôles Gestion de la conformité et Gestion de l’organisation sur la page **Autorisations** dans le Centre d’administration Exchange. Notez que les administrateurs globaux dans votre client Office 365 et Microsoft 365 sont automatiquement des membres du groupe de rôle Gestion de l'organisation dans Exchange Online. Pour permettre à un utilisateur d’effectuer des recherches dans le journal d’audit Office 365 avec le niveau minimal de privilèges, vous pouvez créer un groupe de rôles personnalisé dans Exchange Online, ajouter le rôle Journaux d’audit en affichage seul ou Journaux d’audit, puis ajouter l’utilisateur en tant que membre du nouveau groupe de rôles. Pour plus d’informations, voir [Gérer les groupes de rôles dans Exchange Online](https://go.microsoft.com/fwlink/p/?LinkID=730688).

  > [!IMPORTANT]
  > Si vous affectez le rôle Journaux d’audit en affichage seul ou Journaux d’audit à un utilisateur dans la page **Autorisations** dans le Centre de sécurité et conformité, celui-ci ne pourra pas effectuer de recherches dans le journal d’audit Office 365. Vous devez affecter les autorisations dans Exchange Online. En effet, la cmdlet sous-jacente utilisée pour les recherches dans le journal d’audit est une cmdlet Exchange Online.

- Lorsqu’une activité auditée est effectuée par un utilisateur ou un administrateur, un enregistrement d’audit est généré et stocké dans le journal d’audit Office 365 pour votre organisation. La durée pendant laquelle un enregistrement d’audit est conservé (et peut faire l’objet d’une recherche dans le journal d’audit) dépend de votre abonnement Office 365 et du type de licence affecté à un utilisateur spécifique.

  - **Office 365 E3 :** Les dossiers d’audit sont conservés pendant 90 jours. Vous pouvez rechercher les activités effectuées au cours des 90 derniers jours dans le journal d’audit.  

  - **Office 365 E5 :** Les dossiers d’audit sont également conservés pendant 90 jours. La conservation d’enregistrements d’audit pendant un an peut être mise à la disposition des utilisateurs et utilisateurs de E5 et des utilisateurs avec une licence E3 et d’une licence de composant additionnel de conformité avancée Office 365.

    > [!NOTE]
    > Le programme d’aperçu privé pour la période de rétention d’un an pour les enregistrements d’audit pour les organisations E5 (ou pour les utilisateurs de E3 organisations disposant de licences complémentaires de conformité avancées) de prend plus de nouvelle inscription. Cet article sera mis à jour lorsque la période de rétention d’un an sera disponible en version publique ou publiée pour une disponibilité générale.

- Si vous souhaitez désactiver la recherche dans le journal d’audit dans Office 365 pour votre organisation, vous pouvez exécuter la commande suivante dans une session PowerShell distante connectée à votre organisation Exchange Online :

  ```
  Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $false
  ```

    Pour réactiver la recherche d’audit, vous pouvez exécuter la commande suivante dans Exchange Online PowerShell :

  ```
  Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $true
  ```

  Pour plus d’informations, voir [Désactiver la recherche dans le journal d’audit dans Office 365](turn-audit-log-search-on-or-off.md).

- Comme indiqué précédemment, la cmdlet sous-jacente utilisée pour effectuer une recherche dans le journal d’audit est une cmdlet Exchange Online, à savoir **Search-UnifiedAuditLog**. Cela signifie que vous pouvez utiliser cette cmdlet pour effectuer une recherche dans le journal d’audit Office 365 au lieu d’utiliser la page **Recherche dans le journal d’audit** du Centre de sécurité et conformité. Vous devez exécuter cette cmdlet dans PowerShell distant connecté à votre organisation Exchange Online. Pour plus d’informations, voir [Search-UnifiedAuditLog](https://go.microsoft.com/fwlink/p/?linkid=834776).

  Pour plus d’informations sur l’exportation des résultats de recherche renvoyés par l’applet de commande **Search-UnifiedAuditLog** vers un fichier CSV, voir la section «conseils pour l'exportation et l’affichage du journal d’audit» dans [exporter, configurer et afficher les enregistrements du journal d’audit.](export-view-audit-log-records.md#tips-for-exporting-and-viewing-the-audit-log).

- Si vous voulez télécharger par programme les données du journal d’audit Office 365, nous recommandons d’utiliser l’API Activité de gestion Office 365 au lieu d’utiliser un script PowerShell. L’API Activité de gestion Office 365 est un service web REST que vous pouvez utiliser pour développer des solutions de surveillance des opérations, de la sécurité et de la conformité pour votre organisation. Pour plus d’informations, consultez [Référence de l’API d’activité de gestion d’Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).

- Après la survenue d’un événement, l’apparition de l’entrée de journal d’audit correspondante dans les résultats de la recherche peut prendre jusqu’à 30 minutes, voir 24 heures. Le tableau suivant répertorie les délais en fonction des services dans Office 365.

  |**Service Office 365**|**30 minutes**|**24 heures**|
  |:-----|:-----:|:-----:|
  |Schéma Threat Intelligence et Protection avancée contre les menaces|![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||
  |Azure Active Directory (événements de connexion utilisateur)||![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
  |Azure Active Directory (événements administrateur)||![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
  |Protection contre la perte de données|![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||
  |Dynamics 365 CRM|![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||
  |eDiscovery|![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||
  |Exchange Online|![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||
  |Microsoft Flow|![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||
  |Microsoft Project|![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||
  |Microsoft Stream|![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||
  |Microsoft Teams|![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||
  |Power BI|![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||
  |Centre de sécurité et conformité|![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||
  |Sharepoint Online et OneDrive Entreprise|![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||
  |Sway||![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
  |Workplace Analytics|![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||
  |Yammer||![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|

- Azure Active Directory (Azure AD) est le service d’annuaire pour Office 365. Le journal d’audit unifié contient les activités des utilisateurs, des groupes, des applications, des domaines et des annuaires effectuées dans le centre d’administration Microsoft 365 ou le portail de gestion Azure. Pour consulter la liste complète des événements Azure AD, voir [Événements de rapport d’audit d’Azure Active Directory](https://go.microsoft.com/fwlink/p/?LinkID=616549).

- L’enregistrement d’audit pour Power BI n’est pas activé par défaut. Pour rechercher des activités Power BI dans le journal d’audit Office 365, vous devez activer l’audit dans le portail d’administration Power BI. Pour consulter des instructions, voir la section «journaux d’audit» du [portail d’administration Power BI](https://docs.microsoft.com/power-bi/service-admin-portal#audit-logs).

## <a name="search-the-audit-log"></a>Effectuer une recherche dans le journal d’audit

Pour effectuer une recherche dans le journal d’audit dans Office 365, vous devez procéder comme suit. 

[Étape 1 : effectuer une recherche dans le journal d’audit](#step-1-run-an-audit-log-search)

[Étape 2 : consulter les résultats de la recherche](#step-2-view-the-search-results)

[Étape 3 : filtrer les résultats de la recherche](#step-3-filter-the-search-results)

[Étape 4 : exporter les résultats de la recherche dans un fichier](#step-4-export-the-search-results-to-a-file)

### <a name="step-1-run-an-audit-log-search"></a>Étape 1 : effectuer une recherche dans le journal d’audit

1. Accédez à [https://protection.office.com](https://protection.office.com).

    > [!TIP]
    > Pour accéder au centre de sécurité et conformité, utilisez une session de navigation privée (par opposition à standard), car cela permet d’éviter que les informations d’identification à l’aide desquelles vous êtes actuellement connecté ne soient utilisées. Pour ouvrir une fenêtre de navigation InPrivate dans Internet Explorer ou Microsoft Edge, appuyez sur Ctrl+Maj+P. Pour ouvrir une session de navigation privée dans Google Chrome (appelée fenêtre Incognito), appuyez sur CTRL + MAJ + N.

2. Ouvrez une session Office 365 en utilisant votre compte scolaire ou professionnel.

3. Dans le volet gauche du Centre de sécurité et de conformité, cliquez sur **Recherche** puis sur **Recherche du journal d’audit**.

    La page **Recherche dans le journal d’audit** s’affiche.

    ![Configurez des critères, puis cliquez sur Rechercher pour générer un rapport](media/8639d09c-2843-44e4-8b4b-9f45974ff7f1.png)

    > [!NOTE]
    > Vous devez activer la journalisation d’audit avant d’effectuer une recherche dans le journal d’audit. Si le lien **Commencer à enregistrer les activités des utilisateurs et des administrateurs** apparaît, cliquez dessus pour activer l’audit. Si ce lien n’apparaît pas, l’audit est déjà été activé pour votre organisation.

4. Configurez les critères de recherche suivants : 

    a. **Activités** : Cliquez sur la liste déroulante pour afficher les activités que vous pouvez rechercher. Les activités des utilisateurs et des administrateurs sont organisées au sein de groupes d’activités liées. Vous pouvez sélectionner des activités spécifiques ou cliquer sur le nom d’un groupe d’activités pour sélectionner toutes les activités du groupe. Vous pouvez également cliquer sur une activité sélectionnée pour effacer la sélection. Une fois la recherche terminée, seules les entrées du journal d’audit correspondant aux activités sélectionnées apparaissent. La sélection de l’option **Afficher les résultats pour toutes les activités** affiche les résultats de toutes les activités effectuées par l’utilisateur ou le groupe d’utilisateurs sélectionné.

    Plus de 100 activités utilisateur et administrateur sont enregistrées dans le journal d’audit d’Office 365. Cliquez sur l’onglet **Activités auditées** pour consulter les descriptions de chaque activité pour les différents services Office 365.

    b. **Date de début** et **Date de fin** : Les sept derniers jours sont sélectionnés par défaut. Sélectionnez une plage de dates et d’heures pour afficher les événements survenus pendant cette période. Les date et heure sont présentées au format UTC (temps universel coordonné). La plage de dates maximale que vous pouvez spécifier est de 90 jours. Une erreur s’affiche si la plage de dates sélectionnée est supérieure à 90 jours.

    > [!TIP]
    > Si vous utilisez la plage de dates maximale de 90 jours, sélectionnez l’heure actuelle pour l’option **Date de début**. Dans le cas contraire, un message d’erreur indiquant que la date de début est antérieure à la date de fin apparaît. Si vous avez activé l’audit au cours des 90 derniers jours, la plage de dates maximale ne peut pas commencer avant la date à laquelle l’audit a été activé.

    c. **Utilisateurs** : Cliquez dans cette zone, puis sélectionnez un ou plusieurs utilisateurs pour lesquels afficher les résultats. Les entrées du journal d’audit pour l’activité sélectionnée effectuée par les utilisateurs que vous sélectionnez dans cette zone apparaissent dans la liste des résultats. Laissez cette zone vide pour renvoyer les entrées pour tous les utilisateurs (et les comptes de service) dans votre organisation.

    d. **Fichier, dossier ou site** : Tapez l’entièreté ou une partie du nom d’un fichier ou d’un dossier pour rechercher les activités liées au fichier ou au dossier qui contient le mot clé spécifié. Vous pouvez également spécifier l’URL d’un fichier ou d’un dossier. Si vous utilisez une URL, veillez à entre l’URL complète. Si vous ne tapez qu’une partie de l’URL, n’incluez aucun caractère spécial ou espace.

    Laissez cette zone vide pour renvoyer les entrées correspondant à tous les fichiers et dossiers dans votre organisation.

   **Conseils**

   - Si vous recherchez toutes les activités associées à un **site**, ajoutez le symbole générique (\*) après l’URL pour renvoyer toutes les entrées de ce site, par exemple, **«https://contoso-my.sharepoint.com/personal/*»**.

   - Si vous recherchez toutes les activités associées à **un fichier**, ajoutez le symbole générique (\*) avant le nom de fichier pour renvoyer toutes les entrées de ce fichier, par exemple, **«*Customer_Profitability_Sample. csv».**.

5. Cliquez sur **Rechercher** pour effectuer la recherche à l’aide de vos critères de recherche. 

   Les résultats de recherche sont chargés, puis affichés sous **Résultats** après un moment. Une fois la recherche terminée, le nombre de résultats détectés est affiché. Un maximum de 5 000 événements s’affichent dans le volet**résultats** par incréments de 150 événements. Si plus de 5 000 événements correspondent aux critères de recherche, les 5 000 événements les plus récents sont affichés.

   ![Le nombre de résultats affichés une fois la recherche terminée](media/986216f1-ca2f-4747-9480-e232b5bf094c.png)

#### <a name="tips-for-searching-the-audit-log"></a>Conseils pour effectuer une recherche dans le journal d’audit

- Vous pouvez sélectionner des activités spécifiques à rechercher en cliquant sur le nom des activités. Vous pouvez également rechercher toutes les activités dans un groupe (par exemple, **Activités des fichiers et des dossiers**) en cliquant sur le nom du groupe. Si une activité est sélectionnée, vous pouvez cliquer dessus pour annuler la sélection. Vous pouvez également utiliser la zone de recherche pour afficher les activités qui contiennent le mot clé que vous tapez.

  ![Cliquez sur le nom d’un groupe d’activités pour sélectionner toutes les activités](media/3cde97cb-6f35-47c0-8612-ecd9c6ac36a3.png)

- Vous devez sélectionner **Afficher les résultats pour toutes les activités** dans la liste **Activités** pour afficher les entrées du journal d’audit de l’administrateur Exchange. Les événements dans ce journal d’audit affichent un nom de cmdlet (par exemple, **Set-Mailbox**) dans la colonne **Activité** des résultats. Pour plus d’informations, cliquez sur l’onglet**activités auditées** dans cette rubrique, puis sur **activités de l’administrateur Exchange**.

  De même, certaines activités d’audit n’ont pas d’élément correspondant dans la liste **Activités**. Si vous connaissez le nom de l’opération correspondant à ces activités, vous pouvez effectuer une recherche sur toutes les activités, puis filtrer les résultats en entrant le nom de l’opération dans la zone pour la colonne **Activité**. Voir [Étape 3 : filtrer les résultats de recherche](#step-3-filter-the-search-results) pour plus d’informations sur le filtrage des résultats.

- Cliquez sur **Effacer** pour effacer les critères de recherche actuels. La plage de dates reprend la valeur par défaut des sept derniers jours. Vous pouvez également cliquer sur **Effacer tout pour afficher les résultats correspondant à toutes les activités** pour annuler toutes les activités sélectionnées.

- Si 5 000 résultats sont détectés, vous pouvez partir du principe que plus de 5 000 événements correspondent aux critères de recherche. Vous pouvez affiner les critères de recherche et relancer la recherche pour renvoyer moins de résultats. Vous pouvez également exporter tous les résultats de recherche en sélectionnant **Exporter les résultats** > \> **Télécharger tous les résultats**.

### <a name="step-2-view-the-search-results"></a>Étape 2 : consulter les résultats de la recherche

Les résultats d’une recherche dans le journal d’audit apparaissent sous **Résultats** sur la page **Recherche dans le journal d’audit**. Comme indiqué précédemment, un maximum de 5 000 événements (les plus récents) peut s’afficher, par incréments de 150. Pour afficher davantage d’événements, vous pouvez utiliser la barre de défilement du volet **Résultats** ou appuyer sur **Maj+Fin** afin d’afficher les 150 événements suivants.

Les résultats contiennent les informations suivantes sur chaque événement renvoyé par la recherche :

- **Date :** Date et heure (au format UTC) auxquelles l’événement s’est produit.

- **Adresse IP :** Adresse IP de l’appareil utilisé lors de l’enregistrement de l’activité. L’adresse IP apparaît au format d’adresse IPv4 ou IPv6.

- **Utilisateur :** Utilisateur (ou compte de service) qui a effectué l’action ayant déclenché l’événement.

- **Activité :** Activité effectuée par l’utilisateur. Cette valeur correspond aux activités que vous avez sélectionnées dans la liste déroulante **Activités**. Pour un événement figurant dans le journal d’audit de l’administrateur Exchange, la valeur dans cette colonne est une cmdlet Exchange.

- **Élément :** Objet qui a été créé ou modifié suite à l’activité correspondante. Par exemple, fichier consulté ou modifié, ou compte d’utilisateur mis à jour. Certaines activités n’ont pas de valeur dans cette colonne.

- **Détails :** Détails supplémentaires sur une activité. Là encore, toutes les activités n’ont pas de valeur.

> [!TIP]
> Cliquez sur un en-tête de colonne sous **Résultats** pour trier les résultats. Vous pouvez trier les résultats par ordre croissant ou décroissant. Cliquez sur l’en-tête **Date** pour trier les résultats du plus ancien au plus récent, ou du plus récent au plus ancien.

#### <a name="view-the-details-for-a-specific-event"></a>Afficher les détails d’un événement spécifique

Vous pouvez afficher davantage d’informations sur un événement en cliquant sur l’enregistrement d’événement dans la liste des résultats de recherche. La page **Détails** qui s’affiche contient les propriétés détaillées de l’enregistrement d’événement. Les propriétés affichées dépendent du service Office 365 dans lequel l’événement se produit. Pour afficher des détails supplémentaires, cliquez sur **Plus d’informations**. Pour obtenir des descriptions, voir [Propriétés détaillées dans le journal d’audit Office 365](detailed-properties-in-the-office-365-audit-log.md).

![Cliquez sur Informations supplémentaires pour afficher les propriétés détaillées de l’enregistrement d’événement du journal d’audit](media/6df582ae-d339-4735-b1a6-80914fb77a08.png)

### <a name="step-3-filter-the-search-results"></a>Étape 3 : filtrer les résultats de la recherche

Vous pouvez également filtrer les résultats d’une recherche dans le journal d’audit. Cette fonctionnalité permet de filtrer rapidement les résultats pour un utilisateur ou une activité spécifique. Vous pouvez créer une recherche large au départ, puis filtrer rapidement les résultats pour afficher des événements spécifiques. Vous pouvez ensuite affiner les critères de recherche, puis relancer la recherche pour renvoyer un jeu de résultats plus petit et concis.

Pour filtrer les résultats :

1. Effectuez une recherche dans le journal d’audit.

2. Lorsque les résultats sont affichés, cliquez sur **Filtrer les résultats**.

   Les zones de mot clé apparaissent sous chaque en-tête de colonne.

3. Cliquez sur une des zones sous un en-tête de colonne et tapez un mot ou une expression, en fonction de la colonne qui fait l’objet du filtrage. Les résultats sont réajustés dynamiquement pour afficher les événements qui correspondent à votre filtre.

   ![Tapez un mot dans le filtre pour afficher les événements correspondant au filtre](media/542dc323-a997-402c-934b-cc5e218e50bc.png)

4. Pour effacer un filtre, cliquez sur le **X** dans la zone de filtre, ou cliquez sur **Masquer le filtrage**.

> [!TIP]
> Pour afficher des événements dans le journal d’audit de l’administrateur Exchange, tapez un **-** (tiret) dans la zone de filtre **Activité**. Cela permet d’afficher le nom des cmdlets qui figurent dans la colonne **Activité** des événements d’administrateur Exchange. Vous pouvez ensuite trier les noms de cmdlet par ordre alphabétique.

### <a name="step-4-export-the-search-results-to-a-file"></a>Étape 4 : exporter les résultats de la recherche dans un fichier

Vous pouvez exporter les résultats d’une recherche dans le journal d’audit dans un fichier de valeurs séparées par des virgules (.csv) sur votre ordinateur local. Vous pouvez ouvrir ce fichier dans Microsoft Excel et utiliser des fonctionnalités telles que la recherche, le tri, le filtrage et le fractionnement d’une colonne (dont les cellules contiennent plusieurs propriétés) en plusieurs colonnes.

1. Effectuez une recherche dans le journal d’audit, puis modifiez les critères de recherche jusqu’à obtenir les résultats souhaités.

2. Cliquez sur **Exporter les résultats**, puis sélectionnez l’une des options suivantes :

   - **Enregistrer les résultats chargés :** Choisissez cette option pour exporter uniquement les entrées affichées sous **Résultats** sur la page **Recherche dans le journal d’audit**. Le fichier .csv téléchargé contient les mêmes colonnes (et données) que celles affichées sur la page (Date, Utilisateur, Activité, Élément et Détails). Une colonne supplémentaire (nommée **Plus**) est incluse dans le fichier .csv qui contient davantage d’informations de l’entrée du journal d’audit. Comme vous exportez les mêmes résultats que ceux chargés (et visibles) sur la page **Recherche dans le journal d’audit**, 5 000 entrées au maximum sont exportées.

   - **Télécharger tous les résultats :** Choisissez cette option pour exporter toutes les entrées du journal d’audit Office 365 qui correspondent aux critères de recherche. Pour un ensemble plus vaste de résultats de recherche, choisissez cette option pour télécharger toutes les entrées du journal d’audit en plus des 5 000 résultats d’audit qui apparaissent sur la page **Recherche dans le journal d’audit**. Cette option permet de télécharger les données brutes du journal d’audit dans un fichier .csv et contient des informations supplémentaires de l’entrée du journal d’audit dans la colonne **AuditData**. Le téléchargement du fichier peut prendre plus de temps si vous choisissez cette option d’exportation, car le fichier peut-être plus volumineux que celui téléchargé à l’aide de l’autre option.

     > [!IMPORTANT]
     > Vous pouvez télécharger un maximum de 50 000 entrées dans un fichier .csv à partir d’une seule recherche dans le journal d’audit. Si 50 000 résultats sont téléchargés dans le fichier .csv, vous pouvez partir du principe que plus de 50 000 événements remplissent les critères de recherche. Pour exporter davantage de résultats, essayez d’utiliser une plage de dates pour réduire le nombre d’entrées du journal d’audit. Vous devrez peut-être effectuer plusieurs recherches avec des plages de dates plus réduites pour exporter plus de 50 000 entrées.

3. Une fois que vous avez sélectionné une option d’exportation, un message apparaît en bas de la fenêtre. Il vous invite à ouvrir le fichier .csv, à l’enregistrer dans le dossier Téléchargements ou à l’enregistrer dans un dossier spécifique.



#### <a name="more-information-about-exporting-and-viewing-audit-log-search-results"></a>Informations supplémentaires sur l’exportation et l’affichage des résultats de recherche dans le journal d’audit

- Si vous téléchargez tous les résultats de recherche, le fichier .csv contient une colonne nommée **AuditData**, qui inclut des informations supplémentaires sur chaque événement. Les données de cette colonne se composent d’un objet JSON qui contient plusieurs propriétés de l’enregistrement du journal d’audit. Chaque pair*property:value* dans l’objet JSON est séparée par une virgule. Vous pouvez utiliser l’outil transformation JSON de l’éditeur Power Query dans Excel pour fractionner la colonne **AuditData** en plusieurs colonnes de sorte que chaque propriété dans l’objet JSON ait sa propre colonne. Cela vous permettra d’utiliser une ou plusieurs de ces propriétés pour trier et filtrer les valeurs. Pour obtenir des instructions pas à pas à l’aide de l’éditeur Power Query pour transformer l’objet JSON, voir [exporter, configurer et afficher des enregistrements de journal d’audit](export-view-audit-log-records.md).

  Après avoir fractionné la colonne **AuditData**, vous pouvez filtrer sur la colonne **Opérations** pour afficher les propriétés détaillées pour un type d’activité spécifique.

- L’option **Télécharger tous les résultats** télécharge les données brutes du journal d’audit Office 365 dans un fichier .csv. Les noms de colonne qui apparaissent dans ce fichier (CreationDate, UserIds, Operation, AuditData) sont différents de ceux figurant dans le fichier téléchargé si vous sélectionnez l’option **Enregistrer les résultats chargés**. Les valeurs dans les deux fichiers .csv peuvent également différer pour la même activité. Par exemple, l’activité dans la colonne **Action** du fichier .csv peut avoir une valeur différente de la version « conviviale » qui apparaît dans la colonne **Activité** sur la page Recherche dans le **journal d’audit**. Par exemple, MailboxLogin et Utilisateur connecté à la boîte aux lettres.

- Lorsque vous téléchargez tous les résultats d’une requête de recherche qui contient les événements de différents services Office 365, la colonne **AuditData** du fichier .csv contient différentes propriétés selon le service dans lequel l’action a été effectuée. Par exemple, les entrées des journaux d’audit Exchange et Azure AD incluent une propriété nommée **ResultStatus** qui indique si l’action a réussi ou non. Cette propriété n’est pas incluse pour les événements dans SharePoint. De même, les événements SharePoint ont une propriété qui identifie l’URL de site pour les activités liées aux fichiers et dossiers. Pour modifier ce comportement, vous pouvez utiliser des recherches différentes pour exporter les résultats des activités d’un service.

  Pour obtenir une description des propriétés répertoriées dans la colonne**AuditData** du fichier .csv lorsque vous téléchargez tous les résultats, et du service auquel s’applique chacune d’elles, voir [Propriétés détaillées dans le journal d’audit Office 365](detailed-properties-in-the-office-365-audit-log.md).

## <a name="audited-activities"></a>Activités auditées

Les tableaux de cette section décrivent les activités auditées dans Office 365. Vous pouvez rechercher ces événements dans le journal d’audit dans le Centre de sécurité et conformité.

Ces tableaux regroupent des activités connexes ou les activités d’un service Office 365 spécifique. Les tableaux incluent le nom convivial affiché dans la liste déroulante **Activités** et le nom de l’opération correspondante qui apparaît dans les informations détaillées d’un enregistrement d’audit et le fichier .csv lorsque vous exportez les résultats de recherche. Pour obtenir des descriptions des informations détaillées, voir [Propriétés détaillées dans le journal d’audit Office 365](detailed-properties-in-the-office-365-audit-log.md).

Pour accéder à un tableau spécifique, cliquez sur l’un des liens suivants.

||||
|:-----|:-----|:-----|
|[Activités des fichiers et pages](#file-and-page-activities)|[Activités des dossiers](#folder-activities)|[Activités de liste SharePoint](#sharepoint-list-activities)|
|[Activités de demande d’accès et de partage](#sharing-and-access-request-activities)|[Activités de synchronisation](#synchronization-activities)|[Activités d’autorisations de site](#site-permissions-activities)|
|[Activités d’administration des sites](#site-administration-activities)|[Activités de la boîte aux lettres Exchange](#exchange-mailbox-activities)|[Activités liées au Sway](#sway-activities)|
|[Activités d’administration des utilisateurs](#user-administration-activities)|[Activités d’administration des groupes Azure AD](#azure-ad-group-administration-activities)|[Activités d’administration des applications](#application-administration-activities)|
|[Activités d’administration des rôles](#role-administration-activities)|[Activités d’administration de l’annuaire](#directory-administration-activities)|[Activités de découverte électronique](#ediscovery-activities)|
|[Activités avancées eDiscovery](#advanced-ediscovery-activities)|[Activités dans Power BI](#power-bi-activities)|[Microsoft Workplace Analytics](#microsoft-workplace-analytics-activities)|
|[Activités dans Microsoft Teams](#microsoft-teams-activities)|[Activités dans Yammer](#yammer-activities)|[Activités Microsoft Flow](#microsoft-flow-activities)|
|[Activités Microsoft PowerApps](#microsoft-powerapps)|[Activités de Microsoft Stream](#microsoft-stream-activities)|[Activités administrateur Exchange](#exchange-admin-audit-log)|
||||

### <a name="file-and-page-activities"></a>Activités des fichiers et pages

Le tableau suivant décrit les activités des fichiers et pages dans SharePoint Online et OneDrive Entreprise.

|**Nom convivial**|**Opération**|**Description**|
|:-----|:-----|:-----|
|Fichier consulté|FileAccessed|Le compte d’utilisateur ou système consulte un fichier.|
|(aucun)|FileAccessedExtended|Cet événement est lié à l’activité « Fichier consulté » (FileAccessed). Un événement FileAccessedExtended est consigné lorsque la même personne accède à un fichier pendant une période prolongée (jusqu'à 3 heures). <br/><br/> L’objectif de la journalisation des événements FileAccessedExtended consiste à réduire le nombre d’événements FileAccessed enregistrés lorsqu’un fichier est consulté de manière continue. Cela permet de réduire le bruit généré par l’enregistrement de plusieurs événements FileAccessed pour ce qui est en fait l’activité d’un seul et même utilisateur et vous permettre de vous concentrer sur l’événement FileAccessed initial (plus important).|
|Étiquette stratégie de conformité modifiée|ComplianceSettingChanged|Une étiquette de rétention a été appliquée à un document ou supprimée de celui-ci. Cet événement est déclenché lorsqu’une étiquette de rétention est appliquée manuellement ou automatiquement à un message.|
|État de l’enregistrement modifié sur verrouillé|LockRecord|État de l’enregistrement d’une étiquette de rétention qui classifie un document en tant qu’enregistrement verrouillé. Cela signifie que le document ne peut pas être modifié ou supprimé. Seuls les utilisateurs ayant au moins l’autorisation de collaborateur pour un site peuvent changer le statut d’enregistrement d’un document.|
|Modifier l’état de l’enregistrement sur verrouillé|UnlockRecord|État de l’enregistrement d’une étiquette de rétention qui classifie un document en tant qu’enregistrement déverrouillé. Cela signifie que le document peut être modifié ou supprimé. Seuls les utilisateurs ayant au moins l’autorisation de collaborateur pour un site peuvent changer le statut d’enregistrement d’un document.|
|Fichier archivé|FileCheckedIn|Un utilisateur archive un document qu’il a extrait d’une bibliothèque de documents.|
|Fichier extrait|FileCheckedOut|L’utilisateur extrait un document situé dans une bibliothèque de documents. Les utilisateurs peuvent extraire et apporter des modifications aux documents partagés avec eux.|
|Fichier copié|FileCopied|L’utilisateur copie un document à partir d’un site. Le fichier copié peut être enregistré dans un autre dossier sur le site.|
|Fichier supprimé|FileDeleted|Un utilisateur supprime un document d’un site.|
|Fichier supprimé de la Corbeille|FileDeletedFirstStageRecycleBin|Un utilisateur supprime un fichier de la Corbeille d’un site.|
|Fichier supprimé de la Corbeille second niveau|FileDeletedSecondStageRecycleBin|Un utilisateur supprime un fichier de la Corbeille second niveau d’un site.|
|Supprimer l’enregistrement de l’étiquette stratégie de conformité|ComplianceRecordDelete|Un document classifié en tant qu’enregistrement a été supprimé. Un document est considéré comme un enregistrement lorsqu’une étiquette de rétention qui classifie le contenu en tant qu’enregistrement est appliqué au document.|
|Détection de correspondance incorrecte des documents|DocumentSensitivityMismatchDetected|L’utilisateur charge un document classifié avec une étiquette de confidentialité ayant une priorité plus élevée que l’étiquette de confidentialité appliquée au site sur lequel le document est téléchargé. <br/><br/> Cet événement n’est pas déclenché si l’étiquette de confidentialité appliquée à un site a une priorité plus élevée que l’étiquette de confidentialité appliquée à un document téléchargé sur le site. Pour plus d’informations sur la priorité de l’étiquette de confidentialité, voir la section «priorité des étiquettes» dans [vue d’ensemble des étiquettes de confidentialité](sensitivity-labels.md#label-priority-order-matters).|
|Détection d’un programme malveillant dans le fichier|FileMalwareDetected|Le moteur antivirus de SharePoint détecte un programme malveillant dans un fichier.|
|Extraction de fichier ignorée|FileCheckOutDiscarded|Un utilisateur ignore (ou annule) un fichier extrait. Les modifications qu’il a apportées au fichier le temps de son extraction sont ignorées et ne sont pas enregistrées dans la version du document dans la bibliothèque de documents.|
|Fichier téléchargé|FileDownloaded|Un utilisateur télécharge un document à partir d’un site.|
|Fichier modifié|FileModified|Le compte d’utilisateur ou système modifie le contenu ou les propriétés d’un document sur un site.|
|(aucun)|FileModifiedExtended|Cet événement est lié à l’activité « Fichier modifié » (FileModified). Un événement FileModifiedExtended est consigné lorsque la même personne modifie un fichier pendant une période prolongée (jusqu'à 3 heures). <br/><br/> L’objectif de la journalisation des événements FileModifiedExtended consiste à réduire le nombre d’événements FileModified enregistrés lorsqu’un fichier est modifié de manière continue. Cela permet de réduire le bruit généré par l’enregistrement de plusieurs événements FileModified pour ce qui est en fait l’activité d’un seul et même utilisateur et vous permettre de vous concentrer sur l’événement FileModified initial (plus important).|
|Fichier déplacé|FileMoved|Un utilisateur déplace un document de son emplacement actuel sur un site vers un nouvel emplacement.|
|(aucun)|FilePreviewed|Un utilisateur affiche l’aperçu de fichiers sur un site SharePoint ou OneDrive Entreprise. Ces événements se produisent généralement dans des volumes élevés basés sur une activité unique, comme l’affichage d’une galerie d’images.|
|Recyclage de toutes les versions mineures du fichier|FileVersionsAllMinorsRecycled|L’utilisateur supprime toutes les versions mineures de l’historique des versions d’un fichier. Les versions supprimées sont déplacées vers la Corbeille du site.|
|Recyclage de toutes les versions du fichier|FileVersionsAllRecycled|L’utilisateur supprime toutes les versions de l’historique des versions d’un fichier. Les versions supprimées sont déplacées vers la Corbeille du site.|
|Recyclage d’une version du fichier|FileVersionRecycled|L’utilisateur supprime une version de l’historique des versions d’un fichier. La version supprimée est déplacée vers la Corbeille du site.|
|Fichier renommé|FileRenamed|Un utilisateur renomme un document sur un site.|
|Fichier restauré|FileRestored|Un utilisateur restaure un document à partir de la Corbeille d’un site.|
|Fichier téléchargé|FileUploaded|Un utilisateur charge un document vers un dossier sur un site.|
|Page affichée|PageViewed|Un utilisateur affiche une page sur un site. Ceci n’inclut pas l’utilisation d’un navigateur web pour afficher les fichiers dans une bibliothèque de documents.|
|(aucun)|PageViewedExtended|Cet événement est lié à l’activité « Page affichée » (PageViewed). Un événement PageViewedExtended est consigné lorsque la même personne affiche une page web pendant une période prolongée (jusqu'à 3 heures). <br/><br/> L’objectif de la journalisation des événements PageViewedExtended consiste à réduire le nombre d’événements PageViewed enregistrés lorsqu’une page est affichée de manière continue. Cela permet de réduire le bruit généré par l’enregistrement de plusieurs événements PageViewed pour ce qui est en fait l’activité d’un seul et même utilisateur et vous permettre de vous concentrer sur l’événement PageViewed initial (plus important).|
|Affichage signalé par le client|ClientViewSignaled|Le client d’un utilisateur (tel qu’un site Web ou une application mobile) a signalé que la page indiquée a été consultée par l’utilisateur. Cette activité est souvent journalisée à la suite d’un événement PagePrefetched pour une page. <br/><br/>**Remarque**: les événements ClientViewSignaled étant signalés par le client, plutôt que le serveur, il est possible que l’événement ne soit pas consigné par le serveur et, par conséquent, qu’il n’apparaisse pas dans le journal d’audit. Il est également possible que les informations dans l’enregistrement d’audit ne soient pas dignes de confiance. Toutefois, étant donné que l’identité de l’utilisateur est validée par le jeton utilisé pour créer le signal, l’identité de l’utilisateur répertoriée dans l’enregistrement d’audit correspondant est exacte. |
|(aucun)|PagePrefetched|Le client d’un utilisateur (tel qu’un site Web ou une application mobile) a demandé la page indiquée afin de vous aider à améliorer les performances si l’utilisateur accède à celui-ci. Cet événement est enregistré pour indiquer que le contenu de la page a été servi au client de l’utilisateur. Cet événement n’indique pas si l’utilisateur a accédé à la page. <br/><br/> Lorsque le contenu de la page est affiché par le client (conformément à la demande de l’utilisateur), un événement ClientViewSignaled doit être généré. Tous les clients ne prennent pas en charge l’indication d’une pré-récupération ; par conséquent, certaines activités préalablement récupérées peuvent être enregistrées en tant qu’événements PageViewed.|
||||

### <a name="folder-activities"></a>Activités des dossiers

Le tableau suivant décrit les activités des fichiers dans SharePoint Online et OneDrive Entreprise.

|**Nom convivial**|**Opération**|**Description**|
|:-----|:-----|:-----|
|Dossier copié|FolderCopied|Un utilisateur copie un dossier à partir d’un site vers un autre emplacement dans SharePoint ou OneDrive Entreprise.|
|Dossier créé|FolderCreated|Un utilisateur crée un dossier sur un site.|
|Dossier supprimé|FolderDeleted|Un utilisateur supprime un dossier d’un site.|
|Dossier supprimé de la Corbeille|FolderDeletedFirstStageRecycleBin|Un utilisateur supprime un dossier de la Corbeille sur un site.|
|Dossier supprimé de la Corbeille second niveau|FolderDeletedSecondStageRecycleBin|Un utilisateur supprime un dossier de la Corbeille second niveau sur un site.|
|Dossier modifié|FolderModified|Un utilisateur modifie un dossier sur un site. Cela inclut la modification des métadonnées du dossier (par exemple, modification des balises et propriétés).|
|Dossier déplacé|FolderMoved|Un utilisateur déplace un dossier vers un autre emplacement sur un site.|
|Dossier renommé|FolderRenamed|Un utilisateur renomme un dossier sur un site.|
|Dossier restauré|FolderRestored|Un utilisateur restaure un dossier supprimé de la Corbeille sur un site.|
||||

### <a name="sharepoint-list-activities"></a>Activités de liste SharePoint

Le tableau suivant décrit les activités liées à la façon dont les utilisateurs interagissent avec les listes et les éléments de liste dans SharePoint Online.

|**Nom convivial**|**Opération**|**Description**|
|:-----|:-----|:-----|
|Liste créée|ListCreated|Un utilisateur a créé une liste SharePoint.|
|Colonne de liste créée|ListColumnCreated|Un utilisateur a créé une colonne de liste SharePoint. Une colonne de liste est une colonne jointe à une ou plusieurs listes SharePoint.|
|Type de contenu de liste créé|ListContentTypeCreated|Un utilisateur a créé un type de contenu de liste. Un type de contenu de liste est un type de contenu attaché à une ou plusieurs listes SharePoint.|
|Élément de liste créé|ListItemCreated|Un utilisateur a créé un élément dans une liste SharePoint existante.|
|Colonne de site créée|SiteColumnCreated|Un utilisateur a créé une colonne de site SharePoint. Une colonne de site est une colonne qui n’est pas jointe à une liste. Une colonne de site est également une structure de métadonnées pouvant être utilisée par n’importe quelle liste d’un site Web donné.|
|Type de contenu de site créé|ContentType du site créé|Un utilisateur a créé un type de contenu de site. Un type de contenu de site est un type de contenu attaché au site parent.|
|Liste supprimée|ListDeleted|Un utilisateur a supprimé une liste SharePoint.|
|Colonne de liste supprimée|Colonne de liste supprimée|Un utilisateur a supprimé une colonne de liste SharePoint.|
|Type de contenu de liste supprimé|ListContentTypeDeleted|Un utilisateur a supprimé un type de contenu de liste.|
|Élément de liste supprimé|Élément de liste supprimé|Un utilisateur a supprimé un élément de liste SharePoint.|
|Colonne de site supprimée|SiteColumnDeleted|Un utilisateur a supprimé une colonne de site SharePoint.|
|Type de contenu de site supprimé|SiteContentTypeDeleted|Un utilisateur a supprimé un type de contenu de site.|
|Élément de liste recyclé|ListItemRecycled|Un utilisateur a déplacé un élément de liste SharePoint dans la corbeille.|
|Liste restaurée|ListRestored|Un utilisateur a restauré un élément de liste SharePoint depuis la corbeille.|
|Élément de liste restauré|ListItemRestored|Un utilisateur a restauré un élément de liste SharePoint depuis la corbeille.|
|Liste mise à jour|ListUpdated|Un utilisateur a mis à jour une liste SharePoint en modifiant une ou plusieurs propriétés.|
|Colonne de liste mise à jour|ListColumnUpdated|Un utilisateur a mis à jour une colonne de liste SharePoint en modifiant une ou plusieurs propriétés.|
|Type de contenu de liste mis à jour|ListContentTypeUpdated|Un utilisateur a mis à jour un type de contenu de liste en modifiant une ou plusieurs propriétés.|
|Élément de liste mis à jour|ListItemUpdated|Un utilisateur a mis à jour un élément de liste SharePoint en modifiant une ou plusieurs propriétés.|
|Colonne de site mise à jour|SiteColumnUpdated|Un utilisateur a mis à jour une colonne de site SharePoint en modifiant une ou plusieurs propriétés.|
|Type de contenu de site mis à jour|SiteContentTypeUpdated|Un utilisateur a mis à jour un type de contenu de site en modifiant une ou plusieurs propriétés.|
||||

### <a name="sharing-and-access-request-activities"></a>Activités de demande d’accès et de partage

Le tableau suivant décrit les activités de demande d’accès et de partage d’utilisateurs dans SharePoint Online et OneDrive Entreprise. Pour les événements de partage, la colonne **Détails** sous **Résultats** identifie le nom de l’utilisateur ou du groupe avec lequel l’élément était partagé et si cet utilisateur ou groupe est un membre de votre organisation ou un invité. Pour plus d’informations, voir [Utiliser l’audit du partage dans le journal d’audit d’Office 365](use-sharing-auditing.md).

> [!NOTE]
> Les utilisateurs peuvent être des *membres* ou des *invités* en fonction de la propriété UserType de l’objet utilisateur. Un membre est généralement un employé, tandis qu’un invité est généralement un collaborateur externe à votre organisation. Lorsqu’un utilisateur accepte une invitation de partage (et ne fait pas déjà partie de votre organisation), un compte invité est créé pour lui dans l’annuaire de votre organisation. Dès lors que l’utilisateur invité a un compte dans votre annuaire, des ressources peuvent être partagées directement avec lui (sans invitation).

|**Nom convivial**|**Opération**|**Description**|
|:-----|:-----|:-----|
|Ajout d’un niveau d’autorisation à la collection de sites|PermissionLevelAdded|Un niveau d’autorisation a été ajouté à une collection de sites.|
|Demande d’accès acceptée|AccessRequestAccepted|Une demande d’accès à un site, un dossier ou un document a été acceptée et l’utilisateur à l’origine de la demande s’est vu octroyé l’accès.|
|Invitation de partage acceptée|SharingInvitationAccepted|L’utilisateur (membre ou invité) a accepté une invitation de partage et s’est vu octroyer l’accès à une ressource. Cet événement inclut des informations sur l’utilisateur invité et l’adresse de messagerie utilisée pour accepter l’invitation (ils peuvent être différents). Cette activité est souvent accompagnée d’un deuxième événement qui décrit la manière dont l’utilisateur s’est vu octroyer l’accès à la ressource (par exemple, en ajoutant l’utilisateur à un groupe ayant accès à la ressource).|
|Invitation de partage bloquée|SharingInvitationBlocked|Une invitation de partage envoyée par un utilisateur de votre organisation est bloquée par une stratégie de partage externe qui autorise ou refuse le partage externe en fonction du domaine de l’utilisateur cible. Dans ce cas, l’invitation de partage a été bloquée car : <br/> Le domaine de l’utilisateur cible n’est pas inclus dans la liste des domaines autorisés. <br/> Ou <br/> Le domaine de l’utilisateur cible est inclus dans la liste des domaines bloqués. <br/> Pour plus d’informations sur l’autorisation ou le blocage du partage externe en fonction des domaines, voir [Restreindre le partage des domaines dans SharePoint Online et OneDrive Entreprise](https://support.office.com/article/5d7589cd-0997-4a00-a2ba-2320ec49c4e9).|
|Demande d’accès créée|AccessRequestCreated|Un utilisateur demande l’accès à un site, un dossier ou un document auquel il n’est pas autorisé à accéder.|
|Création d’un lien d’entreprise partageable |CompanyLinkCreated|L’utilisateur a créé un lien à l’échelle de l’entreprise vers une ressource. Les liens à l’échelle de l’entreprise ne peuvent être utilisés que par les membres de votre organisation. Ils ne peuvent pas être utilisés par les invités.|
|Création d’un lien anonyme|AnonymousLinkCreated|L’utilisateur a créé un lien anonyme vers une ressource. Toute personne disposant de ce lien peut accéder à la ressource sans être authentifiée.|
|Lien sécurisé créé|SecureLinkCreated|Un lien de partage sécurisé a été créé sur cet élément.|
|Invitation de partage créée|SharingInvitationCreated|Un utilisateur a partagé une ressource dans SharePoint Online ou OneDrive Entreprise avec un utilisateur qui ne figure pas dans l’annuaire de votre organisation.|
|Lien sécurisé supprimé|SecureLinkDeleted|Un lien de partage sécurisé a été supprimé.|
|Demande d’accès refusée |AccessRequestDenied|Une demande d’accès à un site, un dossier ou un document a été refusée.|
|Suppression d’un lien d’entreprise partageable|CompanyLinkRemoved|L’utilisateur a supprimé un lien à l’échelle de l’entreprise vers une ressource. Le lien ne peut plus être utilisé pour accéder à la ressource.|
|Suppression d’un lien anonyme|AnonymousLinkRemoved|L’utilisateur a supprimé un lien anonyme vers une ressource. Le lien ne peut plus être utilisé pour accéder à la ressource.|
|Fichier, dossier ou site partagé|SharingSet|L’utilisateur (membre ou invité) a partagé un fichier, un dossier ou un site dans SharePoint ou OneDrive Entreprise avec un utilisateur dans l’annuaire de votre organisation. La valeur dans la colonne **Détails** pour cette activité identifie le nom de l’utilisateur avec lequel la ressource a été partagée et si cet utilisateur est un membre ou un invité. <br/><br/> Cette activité est souvent accompagnée d’un deuxième événement qui décrit la manière dont l’utilisateur s’est vu octroyer l’accès à la ressource. Par exemple, en ajoutant l’utilisateur à un groupe ayant accès à la ressource.|
|Demande d’accès mise à jour|AccessRequestUpdated|Une demande d’accès à un élément a été mise à jour.|
|Mise à jour d’un lien anonyme |AnonymousLinkUpdated|L’utilisateur a mis à jour un lien anonyme vers une ressource. Le champ mise à jour est inclus dans la propriété EventData lorsque vous exportez les résultats de recherche.|
|Invitation de partage mise à jour|SharingInvitationUpdated|Une invitation de partage externe a été mise à jour.|
|Utilisation d’un lien anonyme |AnonymousLinkUsed|Un utilisateur anonyme a consulté une ressource à l’aide d’un lien anonyme. L’identité de l’utilisateur peut être inconnue, mais vous pouvez obtenir d’autres informations telles que l’adresse IP de l’utilisateur.|
|Fichier, dossier ou site non partagé|SharingRevoked|Un utilisateur (membre ou invité) a cessé de partager un fichier, un dossier ou un site précédemment partagé avec un autre utilisateur.|
|Utilisation d’un lien d’entreprise partageable|CompanyLinkUsed|Un utilisateur a consulté une ressource à l’aide d’un lien à l’échelle de l’entreprise.|
|Lien sécurisé utilisé|SecureLinkUsed|Un utilisateur a utilisé un lien sécurisé.|
|Utilisateur ajouté à un lien sécurisé.|AddedToSecureLink|Un utilisateur a été ajouté à la liste des entités pouvant utiliser un lien de partage sécurisé.|
|Utilisateur supprimé d’un lien sécurisé.|RemovedFromSecureLink|Un utilisateur a été supprimé de la liste des entités pouvant utiliser un lien de partage sécurisé.|
|Invitation de partage retirée|SharingInvitationRevoked|Un utilisateur a retiré une invitation de partage à une ressource. |
||||

### <a name="synchronization-activities"></a>Activités de synchronisation

Le tableau suivant décrit les activités de synchronisation dans SharePoint Online et OneDrive Entreprise.

|**Nom convivial**|**Opération**|**Description**|
|:-----|:-----|:-----|
|Ordinateur autorisé à synchroniser des fichiers|ManagedSyncClientAllowed|L’utilisateur a réussi à établir une relation de synchronisation avec un site. La relation de synchronisation est établie, car l’ordinateur de l’utilisateur est membre d’un domaine qui a été ajouté à la liste de domaines (*liste des destinataires approuvés*) qui peuvent accéder aux bibliothèques de documents dans votre organisation. <br/><br/> Pour plus d’informations sur cette fonctionnalité, reportez-vous à l’article [Utilisation des cmdlet Windows PowerShell pour activer la synchronisation de OneDrive pour les domaines figurant dans la liste des destinataires approuvés](https://go.microsoft.com/fwlink/p/?LinkID=534609).|
|Ordinateur non autorisé à synchroniser des fichiers|UnmanagedSyncClientBlocked|L’utilisateur tente d’établir une relation de synchronisation avec un site à partir d’un ordinateur qui n’est pas membre du domaine de votre organisation ou qui est membre d’un domaine qui n’a pas été ajouté à la liste de domaines (*liste des destinataires approuvés)* qui peut accéder aux bibliothèques de documents dans votre organisation. La relation de synchronisation n’est pas autorisée et l’ordinateur de l’utilisateur est bloqué en matière de synchronisation, de téléchargement ou de chargement de fichiers dans une bibliothèque de documents. <br/><br/> Pour plus d’informations sur cette fonctionnalité, reportez-vous à l’article [Utilisation des cmdlet Windows PowerShell pour activer la synchronisation de OneDrive pour les domaines figurant dans la liste des destinataires approuvés](https://go.microsoft.com/fwlink/p/?LinkID=534609).|
|Fichiers téléchargés sur l’ordinateur|FileSyncDownloadedFull|Un utilisateur établit une relation de synchronisation et télécharge des fichiers pour la première fois sur son ordinateur à partir d’une bibliothèque de documents.|
|Modifications du fichier téléchargées sur l’ordinateur|FileSyncDownloadedPartial|L’utilisateur télécharge les modifications apportées aux fichiers à partir d’une bibliothèque de documents. Cette activité indique que les modifications apportées à des fichiers dans la bibliothèque de documents ont été téléchargées sur l’ordinateur de l’utilisateur. Seules les modifications ont été téléchargées, car la bibliothèque de documents a été téléchargée précédemment par l’utilisateur (comme indiqué par l’activité **Fichiers téléchargés sur l’ordinateur**).|
|Fichiers téléchargés dans la bibliothèque de documents|FileSyncUploadedFull|Un utilisateur établit une relation de synchronisation et charge des fichiers pour la première fois à partir de son ordinateur dans une bibliothèque de documents.|
|Modifications du fichier téléchargées dans la bibliothèque de documents|FileSyncUploadedPartial|L’utilisateur charge les modifications apportées aux fichiers dans une bibliothèque de documents. Cet événement indique que les modifications apportées à la version locale d’un fichier dans une bibliothèque de documents sont correctement chargées dans la bibliothèque de documents. Seules les modifications sont chargées, car ces fichiers ont été précédemment chargés par l’utilisateur (comme indiqué par l’activité **Fichiers téléchargés dans la bibliothèque de documents**).|
||||

### <a name="site-permissions-activities"></a>Activités d’autorisations de site

Le tableau suivant répertorie les événements liés à l’attribution d’autorisations dans SharePoint et l’utilisation des groupes pour accorder (et révoquer) l’accès aux sites.

|**Nom convivial**|**Opération**|**Description**|
|:-----|:-----|:-----|
|Administrateur de collection de site ajouté|SiteCollectionAdminAdded|L’administrateur de collection de sites ou le propriétaire ajoute une personne en tant qu’administrateur de collection de sites pour un site. Les administrateurs de collection de sites disposent du niveau d’autorisation Contrôle total sur la collection de sites et tous les sous-sites. Cette activité est également enregistrée lorsqu’un administrateur donne son accès au compte OneDrive d’un utilisateur (en modifiant le profil utilisateur dans le centre d’administration SharePoint ou à l’aide du [centre d’administration Microsoft 365](https://docs.microsoft.com/office365/admin/add-users/get-access-to-and-back-up-a-former-user-s-data#part-1---get-access-to-the-former-employees-onedrive-for-business-documents)).|
|Utilisateur ou groupe ajouté au groupe SharePoint|AddedToGroup|L’utilisateur a ajouté un membre ou un invité à un groupe SharePoint. Il s’agit peut-être d’une action intentionnelle ou du résultat d’une autre activité (par exemple, événement de partage).|
|Fin de l’héritage des niveaux d’autorisation|PermissionLevelsInheritanceBroken|Un élément a été modifié afin qu’il n’hérite plus des niveaux d’autorisation de son parent.|
|Fin de l’héritage de partage|SharingInheritanceBroken|Un élément a été modifié afin qu’il n’hérite plus des autorisations de partage de son parent.|
|Groupe créé|GroupAdded|L’administrateur ou le propriétaire du site crée un groupe pour un site ou effectue une tâche à l’origine de la création d’un groupe. Par exemple, la première fois qu’un utilisateur crée un lien pour partager un fichier, un groupe système est ajouté au site OneDrive Entreprise de l’utilisateur. Cet événement peut également être le résultat de la création d’un lien par un utilisateur avec autorisation de modification sur un fichier partagé.|
|Groupe supprimé|GroupRemoved|Un utilisateur supprime un groupe d’un site.|
|Paramètre de demande d’accès modifié|WebRequestAccessModified|Les paramètres de demande d’accès ont été modifiés sur un site.|
|Paramètre «les membres peuvent partagés» modifié|WebMembersCanShareModified|Le paramètre **les membres peuvent partager** a été modifié sur un site.|
|Modification du niveau d’autorisation sur la collection de sites|PermissionLevelModified|Un niveau d’autorisation a été modifié sur une collection de sites.|
|Autorisations de site modifiées|SitePermissionsModified|L’administrateur ou le propriétaire du site (ou compte système) modifie le niveau d’autorisation affecté à un groupe sur un site. Cette activité est également enregistrée si toutes les autorisations sont supprimées d’un groupe. <br/><br/> **Remarque**: cette opération est déconseillée dans SharePoint Online. Pour rechercher des événements connexes, vous pouvez rechercher d’autres activités liées à une autorisation, telles que **Administrateur de collection de sites ajoutée**, **Utilisateur ou groupe ajouté à un groupe SharePoint**, **Utilisateur autorisé à créer des groupes**, **Groupe créé** et **Groupe supprimé**.|
|Suppression d’un niveau d’autorisation dans une collection de sites|PermissionLevelRemoved|Un niveau d’autorisation a été supprimé d’une collection de sites.|
|Administrateur de collection de site supprimé|SiteCollectionAdminRemoved|L’administrateur de collection de sites ou le propriétaire supprime une personne en tant qu’administrateur de collection de sites pour un site. Cette activité est également enregistrée lorsqu’un administrateur se supprime de la liste des administrateurs de collections de sites pour le compte OneDrive d’un utilisateur (en modifiant le profil utilisateur dans le centre d’administration SharePoint).  Pour renvoyer cette activité dans les résultats de la recherche dans le journal d’audit, vous devez rechercher toutes les activités.|
|Utilisateur ou groupe supprimé au groupe SharePoint|RemovedFromGroup|L’utilisateur a supprimé un membre ou un invité d’un groupe SharePoint. Il s’agit peut-être d’une action intentionnelle ou du résultat d’une autre activité (par exemple, événement d’annulation de partage).|
|Autorisations d’administrateur de site demandées|SiteAdminChangeRequest|L’utilisateur demande à être ajouté en tant qu’administrateur de collection de sites pour une collection de sites. Les administrateurs de collection de sites disposent du niveau d’autorisation Contrôle total sur la collection de sites et tous les sous-sites.|
|Restauration de l’héritage de partage|SharingInheritanceReset|Une modification a été apportée afin qu’un élément hérite des autorisations de partage de son parent.|
|Groupe mis à jour|GroupUpdated|L’administrateur ou le propriétaire du site modifie les paramètres d’un groupe pour un site. Cela peut inclure la modification du nom du groupe, qui peut consulter ou modifier l’appartenance au groupe et la gestion des demandes d’appartenance.|
||||

### <a name="site-administration-activities"></a>Activités d’administration des sites

Le tableau suivant répertorie les événements qui résultent de tâches d’administration de site dans SharePoint Online.

|**Nom convivial**|**Opération**|**Description**|
|:-----|:-----|:-----|
|Ajout de l’emplacement de données autorisé|AllowedDataLocationAdded|Un administrateur SharePoint ou général a ajouté un emplacement de données autorisé dans un environnement à plusieurs emplacements géographiques.|
|Agent utilisateur exempté ajouté|ExemptUserAgentSet|Un administrateur SharePoint ou général a ajouté un agent utilisateur à la liste des agents utilisateurs exemptés dans le centre d’administration SharePoint.|
|Ajout d’un administrateur d’emplacement géographique|GeoAdminAdded|Un administrateur SharePoint ou général a ajouté un utilisateur en tant qu’administrateur géo d’un emplacement.|
|Utilisateur autorisé à créer des groupes|AllowGroupCreationSet|Un administrateur ou propriétaire de site ajoute un niveau d’autorisation à un site qui permet à un utilisateur auquel cette autorisation est octroyée de créer un groupe pour ce site.|
|Annulation du géodéplacement d’un site|SiteGeoMoveCancelled|Un administrateur SharePoint ou global annule correctement un déplacement géospatial de site SharePoint ou OneDrive. La fonctionnalité multigéographique permet à une organisation Office 365 de couvrir plusieurs zones géographiques de centre de données Office 365, que l’on appelle géos. Pour plus d’informations, voir [Fonctionnalités multigéographiques de OneDrive et SharePoint Online dans Office 365](https://go.microsoft.com/fwlink/?linkid=860840).|
|Modification d’une stratégie de partage|SharingPolicyChanged|Un administrateur SharePoint ou général a modifié une stratégie de partage SharePoint à l’aide du portail d’administration 365 d’Office, du portail d’administration SharePoint ou de SharePoint Online Management Shell. Les modifications apportées aux paramètres de la stratégie de partage de votre organisation sont enregistrées. La stratégie modifiée est identifiée dans le champ **ModifiedProperties** des propriétés détaillées de l’enregistrement d’événement.|
|Modification de la stratégie d’accès aux appareils|DeviceAccessPolicyChanged|Un administrateur SharePoint ou général a modifié la stratégie relative aux appareils non gérés de votre organisation. Cette stratégie contrôle l’accès à SharePoint, OneDrive, et Office 365 sur les appareils qui ne sont pas associés à votre organisation. La configuration de cette stratégie nécessite un abonnement Enterprise Mobility + Security. Pour plus d’informations, voir [Contrôler l’accès à partir des appareils non gérés](https://support.office.com/article/5ae550c4-bd20-4257-847b-5c20fb053622).|
|Agents utilisateurs exemptés modifiés|CustomizeExemptUsers|L’administrateur SharePoint ou général a personnalisé la liste des agents utilisateurs exemptés dans le Centre d’administration SharePoint. Vous pouvez spécifier les agents utilisateurs que vous voulez exempter de la réception d’une page web entière à indexer. Cela signifie que lorsqu’un agent utilisateur que vous avez spécifié comme exempté rencontre un formulaire InfoPath, le formulaire est renvoyé sous la forme d’un fichier XML au lieu d’une page web entière. Cela permet d’accélérer l’indexation des formulaires InfoPath.|
|Modification de la stratégie d’accès au réseau|NetworkAccessPolicyChanged|Un administrateur SharePoint ou général a modifié la stratégie d’accès basée sur l’emplacement (également appelée limite réseau approuvée) dans le Centre d’administration SharePoint ou à l’aide de SharePoint Online PowerShell. Ce type de stratégie détermine qui peut accéder aux ressources SharePoint et OneDrive de votre organisation en fonction des plages d’adresses IP autorisées que vous spécifiez. Pour plus d’informations, voir [Contrôler l’accès aux données SharePoint Online et OneDrive en fonction d’emplacements réseau définis](https://support.office.com/article/b5a5f1f1-1174-4c6b-91d0-9273a6b6971f).|
|Géodéplacement de site effectué|SiteGeoMoveCompleted|Un géodéplacement planifié par un administrateur général de votre organisation a été effectué avec succès. La fonctionnalité multigéographique permet à une organisation Office 365 de couvrir plusieurs zones géographiques de centre de données Office 365, que l’on appelle géos. Pour plus d’informations, voir [Fonctionnalités multigéographiques de OneDrive et SharePoint Online dans Office 365](https://go.microsoft.com/fwlink/?linkid=860840).|
|Connexion Envoyé à créée|SendToConnectionAdded|L’administrateur SharePoint ou général crée une nouvelle connexion Envoyer à sur la page de gestion des enregistrements dans le Centre d’administration SharePoint. Une connexion Envoyer à spécifie les paramètres pour un référentiel de documents ou un centre des enregistrements. Lorsque vous créez une connexion Envoyé à, un organisateur de contenu peut soumettre des documents à l’emplacement spécifié.|
|Collection de sites créée|SiteCollectionCreated|Un administrateur SharePoint ou global crée une collection de sites dans votre organisation SharePoint Online ou un utilisateur configure son site OneDrive Entreprise.|
|Site hub orphelin supprimé|HubSiteOrphanHubDeleted|Un administrateur SharePoint ou général a supprimé un site hub orphelin, qui est un site concentrateur qui n’a pas de sites associé. Un concentrateur orphelin est probablement dû à la suppression du site concentrateur d’origine.|
|Connexion Envoyé à supprimée|SendToConnectionRemoved|L’administrateur SharePoint ou général supprime une connexion Envoyer à sur la page de gestion des enregistrements dans le Centre d’administration SharePoint.|
|Site supprimé|SiteDeleted|L’administrateur de site supprime un site.|
|Aperçu du document activé|PreviewModeEnabledSet|Un administrateur de site active l’aperçu des documents pour un site.|
|Flux de travail hérité activé|LegacyWorkflowEnabledSet|Le propriétaire ou l’administrateur du site ajoute le type de contenu de tâche de flux de travail SharePoint 2013 au site. Les administrateurs généraux peuvent également activer les workflows pour l’ensemble de l’organisation dans le Centre d’administration SharePoint.|
|Office à la demande activé|OfficeOnDemandSet|L’administrateur de site active Office à la demande, qui permet aux utilisateurs d’accéder à la dernière version des applications de bureau Office. « Office à la demande » est activé dans le Centre d’administration SharePoint et nécessite un abonnement Office 365 qui inclut l’installation de l’ensemble des applications Office.|
|Source de résultats activée pour les recherches de personnes|PeopleResultsScopeSet|Un administrateur de site crée l’origine des résultats pour les recherches de personnes pour un site.|
|Flux RSS activés|NewsFeedEnabledSet|L’administrateur ou le propriétaire du site active les flux RSS pour un site. Les administrateurs généraux peuvent activer les flux RSS pour l’ensemble de l’organisation dans le Centre d’administration SharePoint.|
|Site joint au site concentrateur|HubSiteJoined|Un propriétaire de site associe son site à un site concentrateur.|
|Site hub inscrit|HubSiteRegistered|Un administrateur SharePoint ou global crée un site concentrateur. Le résultat est que le site est inscrit pour être un site concentrateur.|
|Emplacement des données autorisées supprimé|AllowedDataLocationDeleted|Un administrateur SharePoint ou général a supprimé un emplacement de données autorisé dans un environnement à plusieurs emplacements géographiques.|
|Administrateur d’emplacement géographique supprimé|GeoAdminDeleted|Un administrateur SharePoint ou général a supprimé un utilisateur en tant qu’administrateur géo d’un emplacement.|
|Site renommé|SiteRenamed|Un administrateur ou propriétaire de site renomme un site.|
|Planification du géodéplacement d’un site|SiteGeoMoveScheduled|Un administrateur SharePoint ou global planifie correctement un déplacement géospatial de site SharePoint ou OneDrive. La fonctionnalité multigéographique permet à une organisation Office 365 de couvrir plusieurs zones géographiques de centre de données Office 365, que l’on appelle géos. Pour plus d’informations, voir [Fonctionnalités multigéographiques de OneDrive et SharePoint Online dans Office 365](https://go.microsoft.com/fwlink/?linkid=860840).|
|Site hôte défini|HostSiteSet|Un administrateur SharePoint ou général modifie le site désigné pour l’hébergement de sites personnels ou OneDrive Entreprise.|
|Définir un quota de stockage pour un emplacement géographique|GeoQuotaAllocated|Un administrateur SharePoint ou général a configuré un quota de stockage pour un environnement à plusieurs emplacements géographiques.|
|Site disjoint d’un site concentrateur|HubSiteUnjoined|Un propriétaire de site dissocie son site d’un site concentrateur.|
|Site concentrateur non enregistré|HubSiteUnregistered|Un administrateur SharePoint ou global annule l’enregistrement d’un site concentrateur. Lorsqu’un site concentrateur est supprimé, il ne fonctionne plus en tant que site concentrateur.|
||||

### <a name="exchange-mailbox-activities"></a>Activités de la boîte aux lettres Exchange

Le tableau suivant répertorie les activités qui peuvent être enregistrées par la journalisation d’audit de la boîte aux lettres. Les activités de boîte aux lettres effectuées par le propriétaire de la boîte aux lettres, un utilisateur délégué ou un administrateur sont enregistrées automatiquement dans le journal d’audit Office 365 pour jusqu’à 90 jours. Un administrateur peut désactiver la journalisation d’audit des boîtes aux lettres pour tous les utilisateurs de votre organisation. Dans ce cas, aucune action de boîte aux lettres pour un utilisateur n’est enregistrée. Pour plus d’informations, voir [Gérer l’audit de boîte aux lettres](enable-mailbox-auditing.md).

 Vous pouvez également rechercher des activités de boîte aux lettres à l’aide de l’applet de commande [Search-MailboxAuditLog](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/search-mailboxauditlog) dans Exchange Online PowerShell.

|**Nom convivial**|**Opération**|**Description**|
|:-----|:-----|:-----|
|Autorisations de boîtes aux lettres de délégué ajoutées|AddMailboxPermissions|Un administrateur a attribué l’autorisation de boîte aux lettres FullAccess à un utilisateur (appelé délégué) à la boîte aux lettres d’une autre personne. L’autorisation FullAccess permet au délégué d’ouvrir la boîte aux lettres d’un autre utilisateur ainsi que de lire et de gérer le contenu de la boîte aux lettres.|
|Utilisateur ajouté ou supprimé avec accès délégué au dossier calendrier|UpdateCalendarDelegation|Un utilisateur a été ajouté ou supprimé en tant que délégué au calendrier de la boîte aux lettres d’un autre utilisateur. La délégation de calendrier donne à une autre personne les mêmes autorisations d’organisation pour gérer le calendrier du propriétaire de la boîte aux lettres.|
|Autorisations ajoutées au dossier|AddFolderPermissions|Une autorisation de dossier a été ajoutée. Les autorisations de dossier contrôlent quels utilisateurs de votre organisation peuvent accéder aux dossiers dans une boîte aux lettres et aux messages situés dans ces dossiers.|
|Messages copiés vers un autre dossier|Copy|Un message a été copié vers un autre dossier.|
|Élément de boîte aux lettres créé|Créer|Un élément est créé dans le dossier Calendrier, Contacts, Notes ou Tâches de la boîte aux lettres.  Par exemple, une nouvelle demande de réunion est créée. Notez que la création, l’envoi ou la réception d’un message ne sont pas audités. De même, la création d’un dossier de boîte aux lettres n’est pas auditée.|
|Nouvelle règle de boîte de réception créée dans Outlook Web App|New-InboxRule|Un propriétaire de boîte aux lettres ou un autre utilisateur ayant accès à la boîte aux lettres a créé une règle de boîte de réception dans Outlook Web App.|
|Messages supprimés du dossier Éléments supprimés|SoftDelete|Un message a été supprimé définitivement ou non du dossier Éléments supprimés. Ces éléments sont déplacés vers le dossier Éléments récupérables. Les messages sont également déplacés vers le dossier Éléments récupérables lorsqu’un utilisateur les sélectionne et appuie sur **Maj+Suppr**.|
|Message étiqueté en tant qu’enregistrement|ApplyRecordLabel|Un message a été classifié en tant qu’enregistrement. Ceci se produit lorsqu’une étiquette de rétention qui classifie le contenu en tant qu’enregistrement est manuellement ou automatiquement appliquée à un message.|
|Messages déplacés vers un autre dossier|Move|Un message a été déplacé vers un autre dossier.|
|Messages déplacés vers le dossier Éléments supprimés|MoveToDeletedItems|Un message a été supprimé et déplacé vers le dossier Éléments supprimés.|
|Autorisation de dossier modifiée|UpdateFolderPermissions|Une autorisation de dossier a été modifiée. Les autorisations de dossier contrôlent quels utilisateurs de votre organisation peuvent accéder aux dossiers de boîte aux lettres et aux messages du dossier.|
|Règle de boîte de réception modifiée à partir d’Outlook Web App|Set-InboxRule|Un propriétaire de boîte aux lettres ou un autre utilisateur ayant accès à la boîte aux lettres a modifié une règle de boîte de réception dans Outlook Web App.|
|Messages supprimés définitivement de la boîte aux lettres|HardDelete|Un courrier a été supprimé définitivement du dossier Éléments récupérables (supprimé définitivement de la boîte aux lettres).|
|Autorisations de boîtes aux lettres de délégué supprimées|Remove-MailboxPermission|Un administrateur a supprimé l’autorisation FullAccess (qui était attribuée à un délégué) à partir de la boîte lettres d’un autre utilisateur. Une fois l’autorisation FullAccess supprimée, le délégué ne peut pas ouvrir l’autre boîte aux lettres ni accéder au contenu.|
|Autorisations supprimées du dossier|RemoveFolderPermissions|Une autorisation de dossier a été supprimée. Les autorisations de dossier contrôlent quels utilisateurs de votre organisation peuvent accéder aux dossiers dans une boîte aux lettres et aux messages situés dans ces dossiers.|
|Message envoyé à l’aide d’autorisations Envoyer en tant que|SendAs|Un message a été envoyé à l’aide de l’autorisation Envoyer en tant que. Cela signifie qu’un autre utilisateur a envoyé le message comme s’il provenait du propriétaire de la boîte aux lettres.|
|Message envoyé à l’aide d’autorisations Envoyer de la part de|SendOnBehalf|Un message a été envoyé à l’aide de l’autorisation Envoyer de la part de. Cela signifie qu’un autre utilisateur a envoyé le message de la part du propriétaire de la boîte aux lettres. Le message indique au destinataire de la part de qui le message a été envoyé et qui a réellement envoyé le message.|
|Règles de boîte de réception mises à jour à partir du client Outlook|UpdateInboxRules|Un propriétaire de boîte aux lettres ou un autre utilisateur ayant accès à la boîte aux lettres a modifié une règle de boîte de réception dans le client Outlook.|
|Message mis à jour|Update|Un message (ou ses propriétés) a été modifié.|
|Utilisateur connecté à la boîte aux lettres|MailboxLogin|L’utilisateur s’est connecté à sa boîte aux lettres.|
||||

### <a name="sway-activities"></a>Activités liées au Sway

Le tableau suivant répertorie les activités des utilisateurs et des administrateurs dans Sway. Sway est une application Office 365 qui permet aux utilisateurs de collecter, de mettre en forme et de partager des idées, des récits et des présentations dans un panneau web interactif. Pour plus d’informations, voir [Forum aux questions sur Sway – Aide pour l’administrateur](https://support.office.com/article/446380fa-25bf-47b2-996c-e12cb2f9d075).

|**Nom convivial**|**Opération**|**Description**|
|:-----|:-----|:-----|
|Niveau de partage Sway modifié|SwayChangeShareLevel|L’utilisateur modifie le niveau de partage d’une instance Sway. Cet événement capture la modification par l’utilisateur de l’étendue du partage associé à un Sway (par exemple, public ou à l’intérieur de l’organisation).|
|Sway créé|SwayCreate|L’utilisateur crée une instance Sway.|
|Sway supprimé|SwayDelete|L’utilisateur supprime une instance Sway.|
|Duplication Sway désactivée|SwayDisableDuplication|L’utilisateur désactive la duplication d’un Sway.|
|Sway dupliqué|SwayDuplicate|L’utilisateur duplique une instance Sway.|
|Sway modifié|SwayEdit|L’utilisateur modifie une instance Sway.|
|Duplication de Sway activée|EnableDuplication|L’utilisateur permet de dupliquer un Sway. La possibilité pour un utilisateur d’autoriser la duplication d’un Sway est activée par défaut.|
|Partage Sway révoqué|SwayRevokeShare|L’utilisateur cesse de partager une instance Sway en révoquant l’accès. Révoquer l’accès modifie les liens associés à une instance Sway.|
|Sway partagé|SwayShare|L’utilisateur a l’intention de partager un Sway. Cet événement capture l’action de l’utilisateur cliquant sur une destination de partage spécifique dans le menu de partage de Sway. L’événement n’indique pas si l’utilisateur a terminé l’action de partage.|
|Désactivation du partage externe de Sway|SwayExternalSharingOff|Un administrateur désactive le partage de Sway externes pour l’ensemble de votre organisation à l’aide du centre d’administration Microsoft 365.|
|Partage externe de Sway activé|SwayExternalSharingOn|Un administrateur active le partage de Sway externes pour l’ensemble de votre organisation à l’aide du centre d’administration Microsoft 365.|
|Service Sway désactivé|SwayServiceOff|Un administrateur désactive Sway pour l’ensemble de votre organisation à l’aide du centre d’administration Microsoft 365.|
|Service Sway activé|SwayServiceOn|L’administrateur active Sway pour l’ensemble de l’organisation à l’aide du centre d’administration Microsoft 365 (le service Sway est activé par défaut).|
|Sway consulté|SwayView|L’utilisateur affiche une instance Sway.|
||||

### <a name="user-administration-activities"></a>Activités d’administration des utilisateurs

Le tableau suivant répertorie les activités d’administration des utilisateurs enregistrées quand un administrateur ajoute ou modifie un compte d’utilisateur via le Centre d’administration Microsoft 365 ou le portail de gestion Azure.

|**Activité**|**Opération**|**Description**|
|:-----|:-----|:-----|
|Utilisateur ajouté|Ajouter un utilisateur|Un compte d’utilisateur Office 365 a été créé.|
|Licence utilisateur modifiée|Change user license|La licence attribuée à un utilisateur a été modifiée. Pour identifier les licences modifiées, voir l’activité **Utilisateur mis à jour** correspondante.|
|Mot de passe utilisateur modifié|Modifier le mot de passe de l’utilisateur|Un administrateur a modifié le mot de passe d’un utilisateur.|
|Utilisateur supprimé|Supprimer un utilisateur|Un compte d’utilisateur Office 365 a été supprimé.|
|Réinitialiser le mot de passe de l’utilisateur|Reset user password|Un administrateur a réinitialisé le mot de passe d’un utilisateur.|
|Propriété définie qui force l’utilisateur à changer de mot de passe.|Forcer la réinitialisation du mot de passe de l'utilisateur|Un administrateur a défini la propriété qui force un utilisateur à modifier son mot de passe lors de sa prochaine connexion à Office 365.|
|Propriétés de licence définies|Propriétés de licence définies|Un administrateur modifie les propriétés d’une licence attribuée à un utilisateur.|
|Utilisateur mis à jour|Mettre à jour un utilisateur|Un administrateur modifie une ou plusieurs propriétés d’un compte d’utilisateur. Pour obtenir la liste des propriétés utilisateur qui peuvent être mises à jour, voir la section « Attributs de "Mettre à jour l’utilisateur" » dans [Événements de rapport d’audit d’Azure Active Directory](https://go.microsoft.com/fwlink/p/?LinkID=616549).|
||||

### <a name="azure-ad-group-administration-activities"></a>Activités d’administration des groupes Azure AD

Le tableau suivant répertorie les activités d’administration des groupes enregistrées lorsqu’un administrateur ou un utilisateur crée ou modifie un groupe Office 365 ou lorsqu’un administrateur crée ou modifie un groupe à l’aide du Centre d’administration Microsoft 365 ou du portail de gestion Azure. Pour plus d’informations sur les groupes dans Office 365, voir [afficher, créer et supprimer des groupes dans le centre d’administration Microsoft 365](https://support.office.com/article/a6360120-2fc4-46af-b105-6a04dc5461c7).

|**Nom convivial**|**Opération**|**Description**|
|:-----|:-----|:-----|
|Groupe ajouté|Add group|Un groupe a été créé.|
|Membre ajouté au groupe|Add member to group|Un membre a été ajouté à un groupe.|
|Groupe supprimé|Delete group|Un groupe a été supprimé.|
|Membre supprimé du groupe|Remove member from group|Un membre a été supprimé d’un groupe.|
|Groupe mis à jour|Update group|Une propriété d’un groupe a été modifiée.|
||||

### <a name="application-administration-activities"></a>Activités d’administration des applications

Le tableau suivant répertorie les activités d’administration des applications enregistrés lorsqu’un administrateur ajoute ou modifie une application enregistrée dans Azure AD. Les applications qui utilisent Azure AD pour l’authentification doivent être enregistrées dans l’annuaire.

|**Nom convivial**|**Opération**|**Description**|
|:-----|:-----|:-----|
|Entrée de délégation ajoutée|Ajouter Entrée de délégation|Une autorisation d’authentification a été créée/accordée à une application dans Azure AD.|
|Principal de service ajouté|Ajouter principal de service|Une application a été enregistrée dans Azure AD. Une application est représentée par un principal de service dans l’annuaire.|
|Informations d’identification ajoutées à un principal de service |Ajouter Informations d’identification à un principal de service|Des informations d’identification ont été ajoutées à un principal de service dans Azure AD. Un principal de service représente une application dans l’annuaire.|
|Entrée de délégation supprimée|Supprimer une entrée de délégation |Une autorisation d’authentification a été supprimée d’une application dans Azure AD.|
|Principal de service supprimé de l’annuaire|Supprimer le principal de service|Une application a été supprimée ou désinscrite de Azure AD. Une application est représentée par un principal de service dans l’annuaire.|
|Les informations d’identification ont été supprimées du principal de service |Supprimer les informations d’identification du principal de service|Des informations d’identification ont été supprimées d’un principal de service dans Azure AD. Un principal de service représente une application dans l’annuaire.|
|Entrée de délégation définie|Définition de l’entrée de délégation|Une autorisation d’authentification a été mise à jour pour une application dans Azure AD.|
||||

### <a name="role-administration-activities"></a>Activités d’administration des rôles

Le tableau suivant répertorie les activités d’administration des rôles Azure AD journalisées quand un administrateur gère les rôles d’administrateur via le Centre d’administration Microsoft 365 ou le portail de gestion Azure.

|**Nom convivial**|**Opération**|**Description**|
|:-----|:-----|:-----|
|Membre ajouté au rôle|Ajouter un membre de rôle au rôle|Un utilisateur a été ajouté à un rôle d’administrateur dans Office 365.|
|Utilisateur supprimé d’un rôle d’annuaire|Supprimer un membre de rôle d’un rôle|Un utilisateur a été supprimé d’un rôle d’administrateur dans Office 365.|
|Définition des informations de contact d’une entreprise|Définition des informations de contact d’une entreprise|Les préférences de contact au niveau de l’entreprise ont été mises à jour pour votre organisation Office 365. Cela inclut les adresses de messagerie pour les messages liés à un abonnement envoyés par Office 365, ainsi que les notifications techniques relatives aux services Office 365.|
||||

### <a name="directory-administration-activities"></a>Activités d’administration de l’annuaire

Le tableau suivant répertorie les activités liées à l’annuaire et au domaine Azure AD journalisées quand un administrateur gère son organisation Office 365 via le Centre d’administration Microsoft 365 ou le portail de gestion Azure.

|**Nom convivial**|**Opération**|**Description**|
|:-----|:-----|:-----|
|Domaine ajouté à l’entreprise|Ajouter un domaine à l’entreprise|Ajoutez un domaine à votre organisation Office 365.|
|Partenaire ajouté à l’annuaire|Ajouter un partenaire à l’entreprise|Un partenaire (administrateur délégué) a été ajouté à votre organisation Office 365.|
|Domaine supprimé de l’entreprise|Supprimer le domaine de l’entreprise|Supprimer un domaine à votre organisation Office 365.|
|Partenaire supprimé de l’annuaire|Supprimer un partenaire de l’entreprise|Un partenaire (administrateur délégué) a été supprimé de votre organisation Office 365.|
|Définition des informations sur la société|Définition des informations sur la société|Les informations de l’entreprise ont été mises à jour pour votre organisation Office 365. Cela inclut les adresses de messagerie pour les messages liés à un abonnement envoyés par Office 365, ainsi que les notifications techniques relatives aux services Office 365.|
|Définition de l’authentification de domaine|Définition de l’authentification de domaine|Le paramètre d’authentification de domaine a été modifié pour votre organisation Office 365.|
|Paramètres de fédération mis à jour pour un domaine|Définir les paramètres de fédération du domaine|Les paramètres de la fédération (partage externe) ont été modifiés pour votre organisation Office 365.|
|Stratégie de mot de passe définie|Stratégie de mot de passe définie|Les contraintes de longueur et de caractères applicables aux mots de passe utilisateur ont été modifiées dans votre organisation Office 365.|
|Activation de la synchronisation Azure AD|Définir l’indicateur DirSyncEnabled à l’entreprise|La propriété qui active un annuaire pour la synchronisation Azure AD a été définie.|
|Domaine mis à jour|Mettre à jour le domaine|Les paramètres d’un domaine dans votre organisation Office 365 ont été mis à jour.|
|Domaine vérifié|Verify domain|La propriété d’un domaine par votre organisation a été vérifiée.|
|Domaine de courrier vérifié par courrier électronique|Verify email verified domain|Une vérification de courrier électronique a été effectuée pour vérifier que votre organisation est propriétaire d’un domaine.|
||||

### <a name="ediscovery-activities"></a>Activités de découverte électronique

Les activités liées à la recherche de contenu et la découverte électronique effectuées dans le centre de sécurité et conformité ou via l’exécution des cmdlets PowerShell correspondantes sont enregistrées dans le journal d’audit. Cela inclut les activités suivantes :

- création et gestion des cas de découverte électronique ;

- création, démarrage et modification des recherches de contenu ;

- exécution des actions de recherche de contenu, telles que l’aperçu, l’exportation et la suppression des résultats de recherche ;

- configuration des autorisations de filtrage de la recherche de contenu ;

- gestion du rôle d’administrateur eDiscovery.

Pour consulter la liste et une description détaillée des activités de découverte électronique enregistrées, voir [Rechercher les activités de découverte électronique dans le journal d’audit Office 365](search-for-ediscovery-activities-in-the-audit-log.md).

> [!NOTE]
> Une trentaine de minutes peut être nécessaire avant que les événements résultant des activités répertoriées sous l’élément **Activités de découverte électronique** de la liste déroulante **Activités** s’affichent dans les résultats de la recherche. Inversement, 24 heures peuvent être nécessaires avant que les événements correspondant aux activités de l’applet de commande eDiscovery s’affichent dans les résultats de la recherche.

### <a name="advanced-ediscovery-activities"></a>Activités avancées eDiscovery

Le tableau suivant répertorie les activités qui résultent des professionnels de l’informatique et du service juridique qui effectuent des tâches dans Advanced eDiscovery dans Microsoft 365. Pour plus d’informations, voir [vue d’ensemble de la solution avancée d'eDiscovery dans Microsoft 365](compliance20/overview-ediscovery-20.md).

|**Nom convivial**|**Opération**|**Description**|
|:-----|:-----|:-----|
|Ajouter des données dans un autre ensemble à réviser|AddWorkingSetQueryToWorkingSet|L’utilisateur a ajouté des documents d’un ensemble à réviser à un autre.|
|Données ajoutées au groupe à réviser|AddQueryToWorkingSet|Un utilisateur a ajouté les résultats de la recherche à partir d’une recherche de contenu associée à un cas avancé d’eDiscovery dans un groupe de révision.|
|Charger des données autres qu’Office 365 dans un ensemble à réviser|AddNonOffice365DataToWorkingSet|L’utilisateur a ajouté des données non-Office 365 à un groupe de révision.|
|Ajout de documents corrigés au groupe révision|AddRemediatedData|L’utilisateur charge les documents qui comportent des erreurs d’indexation qui ont été corrigées dans un groupe de révision.|
|Données analysées dans le groupe révision|RunAlgo|L’utilisateur a exécuté Analytics sur les documents d’un groupe de révision.|
|Document annoté dans le groupe révision|AnnotateDocument|L’utilisateur a annoté un document dans un groupe de révision. L’annotation inclut rédiger du contenu dans un document.|
|Ensembles chargés comparés|LoadComparisonJob|Un utilisateur a comparé deux ensembles chargés différents dans un groupe de révision. Un ensemble chargé est activé lorsque les données d’une recherche de contenu associées au cas sont ajoutées à un groupe de révision.|
|Documents rédigés convertis au format PDF|BurnJob|L’utilisateur a converti tous les documents rédigés dans un ensemble de révision en fichiers PDF.|
|Ensemble de révision créée|CreateWorkingSet|L’utilisateur a créé un groupe de révision.|
|Configuration de la recherche de révision créée|CreateWorkingSetSearch|L’utilisateur a créé une requête de recherche qui effectue une recherche dans les documents d’un groupe de révision.|
|Balise créée|CreateTag|Un utilisateur a créé un groupe de balises dans un ensemble de révision. Un groupe de balises peut contenir une ou plusieurs balises enfant. Ces balises sont ensuite utilisées pour baliser des documents dans le groupe révision.|
|Recherche de la révision supprimée|DeleteWorkingSetSearch|Un utilisateur a supprimé une requête de recherche dans un groupe de révision.|
|Balise supprimée|DeleteTag|Un utilisateur a supprimé une balise ou une balise de groupe dans un groupe de révision.|
|Document téléchargé|DownloadDocument|Un utilisateur a téléchargé un document à partir d’un groupe de révision.|
|Balise modifiée|DownloadDocument|Un utilisateur a modifié une balise dans un groupe de révision.|
|Exporter des documents d’un groupe de révision|ExportJob|L’utilisateur a exporté les documents à partir d’un groupe de révision.|
|Paramètre de casse modifié|UpdateCaseSettings|L’utilisateur a modifié les paramètres de casse. Les paramètres de casse incluent les informations de casse, les autorisations d’accès et les paramètres qui contrôlent le comportement des recherches et analyses.|
|Configuration de la recherche de révision modifiée|UpdateWorkingSetSearch|Un utilisateur a modifié une requête de recherche dans un groupe de révision.|
|Aperçu de configuration de la recherche de révision|PreviewWorkingSetSearch|Un utilisateur a visualisé les résultats d’une requête de recherche dans un ensemble de révision.|
|Documents d’erreur rectifiés|ErrorRemediationJob|L’utilisateur corrige les fichiers qui contiennent des erreurs d’indexation.|
|Document balisé|TagFiles|L’utilisateur a balisé un document dans un groupe de révision.|
|Résultats avec indicateur d’une requête|TagJob|L’utilisateur balise tous les documents qui correspondent aux critères de la requête de recherche dans un ensemble de révision.|
|Document visualisé dans le groupe révision|ViewDocument|Un utilisateur a consulté un document dans un groupe de révision.|
|||

### <a name="power-bi-activities"></a>Activités dans Power BI

Vous pouvez effectuer une recherche dans le journal d’audit des activités dans Power BI. Pour plus d’informations sur les activités Power BI, voir la section «activités vérifiées par Power BI» dans [utilisation de l'audit au sein de votre organisation](https://docs.microsoft.com/power-bi/service-admin-auditing#activities-audited-by-power-bi).

L’enregistrement d’audit pour Power BI n’est pas activé par défaut. Pour rechercher des activités Power BI dans le journal d’audit Office 365, vous devez activer l’audit dans le portail d’administration Power BI. Pour consulter des instructions, voir la section «journaux d’audit» du [portail d’administration Power BI](https://docs.microsoft.com/power-bi/service-admin-portal#audit-logs).

### <a name="microsoft-workplace-analytics-activities"></a>Activités de Microsoft Workplace Analytics

Workplace Analytics explique comment les groupes collaborent au sein de votre organisation Office 365. Le tableau suivant répertorie les activités effectuées par les utilisateurs auxquels est attribué le rôle d’administrateur ou les rôles d’analyste dans Workplace Analytics. Les utilisateurs dotés du rôle d’analyste ont un accès total à toutes les fonctionnalités du service et utilisent le produit pour effectuer l’analyse. Les utilisateurs dotés du rôle d’administrateur peuvent configurer les paramètres de confidentialité et les valeurs par défaut du système, et peuvent préparer, charger et vérifier les données organisationnelles dans Workplace Analytics. Pour plus d'informations, voir [Workplace Analytics](https://docs.microsoft.com/fr-FR/workplace-analytics/index-orig).

|**Nom convivial**|**Opération**|**Description**|
|:-----|:-----|:-----|
|Lien OData consulté|AccessedOdataLink|Les analystes ont accédé au lien OData pour une requête.|
|Requête annulée|CanceledQuery|Un analyste a annulé une requête en cours d’exécution.|
|Exclusion de réunion créée|MeetingExclusionCreated|Un analyste a créé une règle d’exclusion de réunion.|
|Résultat supprimé|DeletedResult|Un analyste a supprimé un résultat de requête.|
|Fichier téléchargé|DownloadedReport|Un analyste a téléchargé un résultat de requête.|
|Requête exécutée|ExecutedQuery|Un analyste a exécuté une requête.|
|Paramètres d’accès aux données mis à jour|UpdatedDataAccessSetting|Un administrateur a mis à jour les paramètres d’accès aux données.|
|Paramètre de confidentialité mis à jour|UpdatedPrivacySetting|Paramètres de confidentialité mis à jour par l’administrateur; par exemple, taille de groupe minimale.|
|Données d’organisation téléchargées|UploadedOrgData|Fichier de données d’organisation téléchargé par l’administrateur.|
|Exploration de la consultation|ViewedExplore|Un analyste a consulté les visualisations dans un ou plusieurs onglets de page exploration.|
||||

### <a name="microsoft-teams-activities"></a>Activités dans Microsoft Teams 

Le tableau suivant répertorie les activités des utilisateurs et des administrateurs dans Microsoft Teams qui sont enregistrées dans le journal d’audit Office 365. Microsoft Teams est un espace de travail centré sur la conversation dans Office 365. Il rassemble les conversations, réunions, fichiers et notes d’une équipe dans un emplacement unique. Pour plus d’informations et des liens vers des rubriques d’aide, voir :

- [Forum aux questions sur Microsoft Teams – Aide de l’administrateur](https://support.office.com/article/05cbe533-2181-4e95-a4b0-52cd7695fafc)

- [Aide de Microsoft Teams](https://support.office.com/article/23156c0c-2c6e-49dd-8b7b-7c564b76508c)

|**Nom convivial**|**Opération**|**Description**|
|:-----|:-----|:-----|
|Robot ajouté à une équipe|BotAddedToTeam|Un utilisateur ajoute un robot à une équipe.|
|Canal ajouté|ChannelAdded|Un utilisateur ajoute un canal à une équipe.|
|Connecteur ajouté|ConnectorAdded|Un utilisateur ajoute un connecteur à un canal.|
|Membres ajoutés à l’équipe|MemberAdded|Un propriétaire d’équipe ajoute des membres à une équipe.|
|Onglet ajouté|TabAdded|Un utilisateur ajoute un onglet à un canal.|
|Paramètre de canal modifié|ChannelSettingChanged|L’opération ChannelSettingChanged est consignée lorsque les activités suivantes sont effectuées par un membre de l’équipe. Pour chacune de ces activités, une description du paramètre modifié (entre parenthèses ci-dessous) s’affiche dans la colonne **Élément (Item)** des résultats de la recherche dans le journal d’audit. <br/><br/>• Modifie le nom d’un canal d’équipe (**Nom de canal**). <br/><br/>• Modifie la description d’un canal d’équipe (**Description de canal**).|
|Paramètre d’organisation modifié|TeamsTenantSettingChanged|L’opération TeamsTenantSettingChanged est consignée lorsque les activités suivantes sont effectuées par un administrateur général (à l’aide du centre d’administration Microsoft 365). Notez que ces activités affectent les paramètres de Microsoft Teams à l’échelle de l’organisation. Pour plus d’informations, voir [Paramètres de l’administrateur de Microsoft Teams](https://support.office.com/article/3966a3f5-7e0f-4ea9-a402-41888f455ba2). <br/> Pour chacune de ces activités, une description du paramètre modifié (entre parenthèses ci-dessous) s’affiche dans la colonne **Élément (Item)** des résultats de la recherche dans le journal d’audit. <br/><br/>• Active ou désactive Microsoft Teams pour l’organisation (**Microsoft Teams**). <br/><br/>• Active ou désactive l’interopérabilité entre Microsoft Teams et Skype Entreprise pour l’organisation (**interopérabilité de Skype Entreprise**). <br/><br/>• Active ou désactive l’affichage de l’organigramme dans les clients Microsoft Teams (**organigramme hiérarchique). <br/> <br/>• Active ou désactive la possibilité pour les membres de l’équipe de planifier des réunions privées (** planification privée des réunions **). <br/><br/>• Active ou désactive la possibilité pour les membres de l’équipe de planifier des réunions de canal (planification des réunions de canal**). <br/><br/>• Active ou désactive les appels vidéo pendant les réunions Teams (Vidéo pour réunions Skype **). <br/><br/>• Active ou désactive le partage d’écran dans les rencontres Microsoft Teams pour l’organisation (** partage d’écran pour les réunions Skype **). <br/> <br/>• Active ou désactive la possibilité d’ajouter des images animées (appelées Giphys) aux conversations Teams (images animées**). <br/><br/>• Modifie le paramètre d’évaluation du contenu pour l’organisation (**Évaluation du contenu**). L’évaluation du contenu restreint les types d’images animées qui peuvent être affichées dans les conversations. <br/><br/>• Active ou désactive la possibilité pour les membres de l’équipe d’ajouter des images personnalisables (appelées mèmes personnalisés) à partir d’Internet aux conversations d’équipe (personnalisation d’images à partir d’Internet **). <br/> <br/>• Active ou désactive la possibilité pour les membres de l’équipe d’ajouter des images modifiables (appelées autocollants) aux conversations d’équipe (** images modifiables **).<br/><br/>• Active ou désactive la possibilité pour les membres de l’équipe d’utiliser des robots dans les conversations et canaux Microsoft Teams (robots à l’échelle de l’organisation**). <br/><br/>• Active les robots spécifiques pour Microsoft Teams. Cela n’inclut pas T-Bot qui est le robot d’assistance de Teams disponible lorsque les robots sont activés pour l’organisation (**Robots individuels**). <br/><br/>• Active ou désactive la possibilité pour les membres de l’équipe d’ajouter des extensions ou des onglets (**Extensions ou onglets**). <br/><br/>• Active ou désactive le chargement latéral des robots propriétaires pour Microsoft Teams (**Chargement latéral des robots**). <br/><br/>• Active ou désactive la possibilité pour les utilisateurs d’envoyer des messages électronique à un canal Microsoft Teams (**E-mail du canal**).|
|Rôle modifié des membres de l’équipe|MemberRoleChanged|Un propriétaire d’équipe modifie le rôle de membres d’une équipe. Les valeurs suivantes indiquent le type de rôles attribué à l’utilisateur. <br/><br/> **1** indique le rôle Propriétaire.<br/>**2** indique le rôle Membre. <br/>**3** indique le rôle Invité. <br/><br/> La propriété Members comprend également le nom de votre organisation et l’adresse e-mail du membre.|
|Paramètre d’équipe modifié|TeamSettingChanged|L’opération TeamSettingChanged est consignée lorsque les activités suivantes sont effectuées par un membre de l’équipe. Pour chacune de ces activités, une description du paramètre modifié (entre parenthèses ci-dessous) s’affiche dans la colonne **Élément (Item)** des résultats de la recherche dans le journal d’audit. <br/><br/>• Modifie le type d’accès d’une équipe. Teams peut être défini comme public ou privé (**Type d’accès à Team**). Quand une équipe est privée (paramètre par défaut), les utilisateurs ne peuvent ne peuvent y accéder que sur invitation. Quand une équipe est publique, n’importe qui peut la trouver. <br/><br/>• Modifie la classification des informations d’une équipe (**Classification d’une équipe **). <br/> Par exemple, les données d’une équipe peuvent être classifiées comme ayant un impact élevé, moyen ou faible sur l’activité.<br/><br/>• Modifie le nom d’une équipe (**Nom de l’équipe**). <br/><br/>• Modifie la description de l’équipe (Description de l’équipe**). <br/><br/>• Modifications apportées aux paramètres de l’équipe. Un propriétaire de l’équipe peut accéder à ces paramètres dans un client Microsoft Teams en cliquant avec le bouton droit sur une équipe, en cliquant sur **Gérer l’équipe**, puis sur l’onglet **Paramètres**. Pour ces activités, le nom du paramètre modifié s’affiche dans la colonne **Élément (Item)** des résultats de la recherche dans le journal d’audit.|
|Équipe créée|TeamCreated|L’utilisateur crée une équipe.|
|Canal supprimé|ChannelDeleted|Un utilisateur supprime un canal d’une équipe.|
|Équipe supprimée|TeamDeleted|Un propriétaire d’équipe supprime une équipe.|
|Robot supprimé l’équipe|BotRemovedFromTeam|Un utilisateur supprime un robot d’une d’une équipe.|
|Connecteur supprimé|ConnectorRemoved|Un utilisateur supprime un connecteur d’un canal.|
|Membres supprimés de l’équipe|MemberRemoved|Un propriétaire d’équipe supprime des membres d’une équipe.|
|Onglet supprimé|TabRemoved|Un utilisateur supprime un onglet d’un canal.|
|Connecteur mis à jour|ConnectorUpdated|Un utilisateur a modifié un connecteur dans un canal.|
|Onglet mis à jour|TabUpdated|Un utilisateur a modifié un onglet dans un canal.|
|Utilisateur connecté à Teams|TeamsSessionStarted|Un utilisateur se connecte à un client Microsoft Teams.|
||||

### <a name="yammer-activities"></a>Activités dans Yammer

Le tableau suivant répertorie les activités des utilisateurs et des administrateurs dans Yammer qui sont enregistrées dans le journal d’audit Office 365. Pour renvoyer des activités Yammer du journal d’audit Office 365, vous devez sélectionner **Afficher les résultats pour toutes les activités** dans la liste**Activités**. Utilisez les zones des plages de dates et la liste **Utilisateurs** pour limiter les résultats de la recherche.

|**Nom convivial**|**Opération**|**Description**|
|:-----|:-----|:-----|
|Modification d’une stratégie de rétention des données|SoftDeleteSettingsUpdated|Un administrateur vérifié met à jour le paramètre de stratégie de rétention des données de réseau en vue d’une suppression définitive ou réversible. Seuls les administrateurs vérifiés peuvent effectuer cette opération.|
|Modification de configuration réseau|NetworkConfigurationUpdated|Un administrateur réseau ou vérifié modifie la configuration du réseau Yammer. Cela inclut la définition d’un intervalle pour l’exportation de données et l’activation de la conversation instantanée.|
|Modification des paramètres de profil réseau|ProcessProfileFields|Un administrateur réseau ou vérifié modifie les informations qui apparaissent sur les profils de membre des utilisateurs du réseau.|
|Modification du mode Contenu privé|SupervisorAdminToggled|Un administrateur vérifié active ou désactive le *mode contenu privé*. Ce mode permet à un administrateur d’afficher les publications dans des groupes privés et les messages privés entre utilisateurs individuels (ou groupes d’utilisateurs). Seuls les administrateurs vérifiés peuvent effectuer cette opération.|
|Modification de la configuration de la sécurité|NetworkSecurityConfigurationUpdated|Un administrateur vérifié met à jour la configuration de sécurité du réseau Yammer. Cela inclut la définition des stratégies d’expiration de mot de passe et les restrictions d’adresses IP. Seuls les administrateurs vérifiés peuvent effectuer cette opération.|
|Création de fichier|FileCreated|Un utilisateur charge un fichier.|
|Groupe créé|GroupCreation|L’utilisateur crée un groupe.|
|Groupe supprimé|GroupDeletion|Un groupe est supprimé de Yammer.|
|Message supprimé|MessageDeleted|Un utilisateur supprime un message.|
|Fichier téléchargé|FileDownloaded|Un utilisateur télécharge un fichier.|
|Données exportées|DataExport|Un administrateur vérifié exporte des données de réseau Yammer. Seuls les administrateurs vérifiés peuvent effectuer cette opération.|
|Partage de fichier|FileShared|Un utilisateur partage un fichier avec un autre utilisateur.|
|Suspension d’un utilisateur du réseau|NetworkUserSuspended|Un administrateur réseau ou vérifié suspend (désactive) un utilisateur de Yammer.|
|Utilisateur suspendu|UserSuspension|Un compte d’utilisateur est suspendu (désactivé).|
|Mise à jour de la description d’un fichier|FileUpdateDescription|Un utilisateur modifie la description d’un fichier.|
|Mise à jour d’un nom de fichier|FileUpdateName|Un utilisateur modifie le nom d’un fichier.|
|Affichage d’un fichier|FileVisited|Un utilisateur affiche un fichier.|
||||

### <a name="microsoft-flow-activities"></a>Activités Microsoft Flow

Vous pouvez effectuer une recherche dans le journal d’audit des activités dans Microsoft Flow. Ces activités incluent la création, la modification et la suppression de flux, et la modification des autorisations de flux. Pour plus d’informations sur l’audit des activités de Flow, voir le blog [événements d’audit de Microsoft Flow désormais disponible dans le centre de sécurité & conformité](https://flow.microsoft.com/blog/security-and-compliance-center).

### <a name="microsoft-powerapps"></a>Microsoft PowerApps

Vous pouvez effectuer une recherche dans le journal d’audit pour consulter les activités liées aux applications dans PowerApps. Ces activités incluent la création, le lancement et la publication d’une application. L’attribution d’autorisations à des applications est également auditée. Pour obtenir une description de toutes les activités PowerApp, voir [journalisation des activités pour PowerApps](https://docs.microsoft.com/fr-FR/power-platform/admin/logging-powerapps#what-events-are-audited).

### <a name="microsoft-stream-activities"></a>Activités de Microsoft Stream

Vous pouvez effectuer une recherche dans le journal d’audit des activités dans Microsoft Stream. Ces activités incluent les activités de vidéo effectuées par les utilisateurs, les activités de canal de groupe et les activités d’administrateur telles que la gestion des utilisateurs, la gestion des paramètres d’organisation et l’exportation de rapports. Pour obtenir une description de ces activités, voir la section «activités enregistrées dans Microsoft Stream» dans [journaux d’audit dans Microsoft Stream](https://docs.microsoft.com/stream/audit-logs).

### <a name="exchange-admin-audit-log"></a>Journal d’audit de l’administrateur Exchange

La journalisation d’audit de l’administrateur Exchange (activée par défaut dans Office 365) enregistre un événement dans le journal d’audit Office 365 lorsqu’un administrateur (ou un utilisateur auquel des autorisations d’administration ont été attribuées) apporte une modification dans votre organisation Exchange. Les modifications apportées à l’aide du Centre d’administration Exchange ou en exécutant une cmdlet dans Exchange Online PowerShell sont enregistrées dans le journal d’audit de l’administrateur Exchange. Les applets de commande qui commencent par les verbes **obtenir**, **rechercher** ou **tester** ne sont pas enregistrées dans le journal d’audit Office 365. Pour plus d’informations sur la journalisation d’audit de l’administrateur dans Exchange, voir [Journalisation d’audit de l’administrateur](https://go.microsoft.com/fwlink/p/?LinkID=619225).

> [!IMPORTANT]
> Certaines applets de commande Exchange Online qui ne sont pas enregistrées dans le journal d’audit de l’administrateur Exchange (ou dans le journal d’audit Office 365). Bon nombre de ces applets de commande sont liées à la maintenance du service Exchange Online et sont exécutées par le personnel du centre de données Microsoft ou les comptes de service. Ces applets de commande ne sont pas enregistrées, car elles génèrent un grand nombre d’événements d’audit «bruyants». Si une applet de commande Exchange Online ne fait pas l’objet d’un audit, envoyez une suggestion [au forum Microsoft Office 365 sécurité & conformité](https://office365.uservoice.com/forums/289138-office-365-security-compliance) et demandez de l’activer pour l’audit. Vous pouvez également envoyer une demande de modification de conception (DCR) au support Microsoft.

Voici quelques conseils pour rechercher des activités d’administrateur Exchange lors de la recherche dans le journal d’audit d’Office 365 :

- Pour renvoyer des entrées du journal d’audit de l’administrateur Exchange, vous devez sélectionner **Afficher les résultats pour toutes les activités** dans la liste **Activités**. Utiliser les zones des plages de dates et la liste **Utilisateurs** pour limiter les résultats de recherche des cmdlets exécutées par un administrateur Exchange spécifique à une plage de dates donnée.

- Pour afficher des événements du journal d’audit de l’administrateur Exchange, filtrez les résultats de la recherche, puis tapez **-** (tiret) dans la zone de filtre **activité**. Cela permet d’afficher le nom des cmdlets qui figurent dans la colonne **Activité** des événements d’administrateur Exchange. Vous pouvez ensuite trier les noms de cmdlet par ordre alphabétique.

  ![Tapez un tiret dans le champ Activités pour filtrer les événements Admin d’Exchange](media/7628e7aa-6263-474a-a28b-2dcf5694bb27.png)

- Pour obtenir des informations sur les cmdlets exécutées, les paramètres et valeurs de paramètres utilisés et les objets affectés, vous devez exporter les résultats de recherche et sélectionner l’option **Télécharger tous les résultats**. Pour plus d’informations, voir [Exporter, configurer et afficher des enregistrements du journal d’audit](export-view-audit-log-records.md).

- Vous pouvez également utiliser la `Search-UnifiedAuditLog -RecordType ExchangeAdmin` commande dans Exchange Online PowerShell pour renvoyer uniquement les enregistrements d’audit du journal d’audit de l’administrateur Exchange. L’exécution de l’entrée de journal d’audit correspondante dans les résultats de la recherche peut prendre jusqu’à 30 minutes après l’exécution d’une applet de commande Exchange. Pour plus d’informations, voir [Search-UnifiedAuditLog](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/search-unifiedauditlog). Pour plus d’informations sur l’exportation des résultats de recherche renvoyés par l’applet de commande **Search-UnifiedAuditLog** vers un fichier CSV, voir la section «conseils pour l'exportation et l’affichage du journal d’audit» dans [exporter, configurer et afficher les enregistrements du journal d’audit.](export-view-audit-log-records.md#tips-for-exporting-and-viewing-the-audit-log).

- Vous pouvez également afficher les événements dans le journal d’audit de l’administrateur Exchange à l’aide du centre d’administration Exchange ou à l’aide de la fonction **Search-AdminAuditLog** dans Exchange Online PowerShell. Il s’agit d’un bon moyen de rechercher spécifiquement les activités effectuées par les administrateurs Exchange Online. Pour plus d’informations, voir :

  - [Consulter le journal d’audit de l’administrateur](https://technet.microsoft.com/library/dn342832%28v=exchg.150%29.aspx)

  - [Search-AdminAuditLog](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/search-adminauditlog)

   Gardez à l’esprit que les mêmes activités d’administrateur Exchange sont enregistrées dans le journal d’audit de l’administrateur Exchange et dans le journal d’audit d’Office 365.

## <a name="frequently-asked-questions"></a>Questions fréquemment posées

**Où puis-je trouver des informations sur les fonctionnalités offertes par le service d’audit dans Office 365 ?**

Pour plus d’informations sur les fonctionnalités d’audit et de création de rapports disponibles dans Office 365, voir [audit et création de rapports dans Office 365](office-365-auditing-and-reporting-overview.md).

**Quels sont les différents services Office 365 actuellement audités ?**

Les services Office 365 les plus utilisés tels qu’Exchange Online, SharePoint Online, OneDrive Entreprise, Azure Active Directory, Microsoft Teams, Dynamics 365, Advanced Threat Protection et Power BI sont audités. Pour obtenir la liste des services audités, voir le [ldébut de cet article](search-the-audit-log-in-security-and-compliance.md).

**Quelles activités sont auditées par le service d’audit dans Office 365 ?**

Consultez la section [activités auditées](#audited-activities) dans cet article pour obtenir la liste et la description des activités auditées dans Office 365.

**Combien de temps faut-il pour que l’enregistrement d’audit soit disponible une fois qu’un événement s’est produit ?**

Après la survenue d’un événement, l’apparition de l’entrée de journal d’audit correspondante dans les résultats de la recherche peut prendre entre 30 minutes et 24 heures. Consultez le tableau de la section [avant de commencer](#before-you-begin) de cet article qui indique le temps nécessaire pour que les événements dans les différents services Office 365 soient disponibles.

**Pendant combien de temps les enregistrements d’audit sont-ils conservés ?**

Comme indiqué précédemment, la période de rétention pour les enregistrements d’audit dépend de l’abonnement Office 365 de votre organisation.

- **Office 365 E3 :** Les dossiers d’audit sont conservés pendant 90 jours.

- **Office 365 E5 :** Les dossiers d’audit sont également conservés pendant 90 jours. La conservation d’enregistrements d’audit pendant un an peut être mise à la disposition des utilisateurs et utilisateurs de E5 et des utilisateurs avec une licence E3 et d’une licence de composant additionnel de conformité avancée Office 365.

  > [!NOTE]
  > Comme indiqué précédemment, le programme d’aperçu privé pour la période de rétention d’un an pour les enregistrements d’audit pour les organisations E5 (ou pour les utilisateurs de E3 organisations disposant de licences complémentaires de conformité avancées) ne prend plus de nouvelle inscription. Cet article sera mis à jour lorsque la période de rétention d’un an sera disponible en version publique ou publiée pour une disponibilité générale.

Notez également que la durée de la période de rétention pour les enregistrements d’audit est basée sur la gestion des licences par utilisateur. Par exemple, si un utilisateur de votre organisation se voit attribuer une licence Office 365 E3 ou E5, les enregistrements d’audit des activités effectuées par cet utilisateur sont conservés pendant 90 jours.

**Puis-je accéder aux données d’audit par programme ?**

Oui. L’API d’activité de gestion d’Office 365 est utilisée pour extraire les journaux d’audit par programme.  Pour commencer, consultez l’article relatif à la [prise en main des API de gestion Office 365](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).

**Existe-t-il d’autres méthodes pour obtenir des journaux d’audit autres que l’utilisation du centre de sécurité et conformité ou de l’API d’activité de gestion d’Office 365 ?**

Non. Il s’agit des deux méthodes permettant d’obtenir des données à partir du service d’audit Office 365.

**Est-ce que je dois activer l’audit de chaque service pour lequel je souhaite capturer les journaux d’audit ?**

Dans la plupart des services Office 365, l’audit est activé par défaut une fois que vous avez activé l’audit pour votre organisation Office 365, comme décrit dans la section [avant de commencer](#before-you-begin) dans cet article.

**Le service d’audit Office 365 prend-il en charge la suppression de doublons d’enregistrements ?**

Non. Le pipeline de service d’audit est presque en temps réel et ne peut donc pas prendre en charge la déduplication.

**Office 365 audite-t-il le flux de données dans les zones géographiques ?**

Non. Nous avons actuellement des déploiements de pipeline d’audit dans les régions NA (Amérique du Nord), EMEA (Europe, Moyen-Orient et Afrique) et APAC (Asie-Pacifique). Toutefois, nous pouvons faire circuler les données entre ces régions pour l’équilibrage de la charge et uniquement lors des problèmes liés aux sites dynamiques. Lorsque nous effectuons ces activités, les données en transit sont chiffrées.

**Les données d’audit sont-elles chiffrées ?**

Les données d’audit sont stockées dans les boîtes aux lettres Exchange (données au repos) situées dans la même région où le pipeline d’audit est déployé. Ces données ne sont pas chiffrées. Toutefois, les données en transit sont toujours chiffrées.
