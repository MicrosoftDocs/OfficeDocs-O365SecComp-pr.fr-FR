---
title: Effectuer des recherches dans le journal d’audit dans le Centre de sécurité et de conformité Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
f1_keywords:
- O365AC_AlternativeEmailAddress
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 0d4d0f35-390b-4518-800e-0c7ec95e946c
description: 'Utilisez le Office 365 Security &amp; centre de conformité pour la recherche dans le journal d’audit unifiée pour afficher l’activité utilisateur et l’administrateur de votre organisation Office 365. '
ms.openlocfilehash: dc673b8f52bacccfa746ad258ea91d8dd2074eeb
ms.sourcegitcommit: bf70ec8e11b3f75bf45cd4f760cd1a982593dbad
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/22/2018
ms.locfileid: "24962970"
---
# <a name="search-the-audit-log-in-the-office-365-security-amp-compliance-center"></a>Effectuer des recherches dans le journal d’audit dans le Centre de sécurité et de conformité Office 365

Vous devez trouver si un utilisateur affiché d’un document spécifique ou purgés un élément à partir de leur boîte aux lettres ? Si ce cas, vous pouvez utiliser la sécurité de 365 Office &amp; centre de conformité pour la recherche dans le journal d’audit unifiée pour afficher l’activité utilisateur et l’administrateur de votre organisation Office 365. Pourquoi un audit unifié se connecter ? Étant donné que vous pouvez rechercher les types suivants de l’activité utilisateur et d’administration d’Office 365 :
  
- Activité de l’utilisateur dans SharePoint Online et OneDrive entreprise
    
- Activité de l’utilisateur dans Exchange Online (enregistrement d’audit des boîtes aux lettres Exchange)
    
    > [!IMPORTANT]
    > Audit de boîte aux lettres la journalisation doit être activée pour chaque boîte aux lettres de l’utilisateur avant d’activité de l’utilisateur dans Exchange Online est enregistrée. Pour plus d’informations, voir [Activer la boîte aux lettres de l’audit dans Office 365](enable-mailbox-auditing.md).
  
- Activité d’administration dans SharePoint Online
    
- Activité d’administration dans Azure Active Directory (service d’annuaire pour Office 365)
    
- Activité d’administration dans Exchange Online (enregistrement d’audit d’administration Exchange)
    
- Activité utilisateur et d’administration dans balancement
    
- activités de découverte de sécurité Office 365 &amp; centre de conformité
    
- Activité utilisateur et d’administration dans Power BI pour Office 365
    
- Activité utilisateur et d’administration dans Microsoft Teams
    
- Activité utilisateur et d’administration dans Yammer
    
- Activité utilisateur et d’administration dans Microsoft Stream
    
   
## <a name="before-you-begin"></a>Avant de commencer

Veillez à lire le journal d’audit des éléments suivants avant de commencer la recherche dans Office 365.
  
- Vous (ou un autre administrateur) devez d’abord activer sur l’enregistrement d’audit avant de commencer la recherche dans le journal d’audit de Office 365. Pour l’activer, cliquez simplement sur ** lancer l’enregistrement d’activité de l’utilisateur et d’administration ** dans la page de **recherche des journaux d’Audit** de sécurité &amp; centre de conformité. (Si vous ne voyez pas ce lien, l’audit a déjà été activé pour votre organisation.) Une fois que vous l’activer, un message s’affiche indiquant que le journal d’audit est préparé et que vous pouvez exécuter une recherche en quelques heures après que la préparation est terminée. Vous ne devez cela qu’une seule fois. 
    
    > [!NOTE]
    > Nous sommes en cours de l’activation de l’audit par défaut. En attendant, vous pouvez l’activer comme décrit précédemment. 
  
- Vous devez être le rôle journaux d’Audit en affichage seul ou des journaux d’Audit dans Exchange Online à rechercher dans le journal d’audit Office 365. Par défaut, ces rôles sont affectés aux groupes de rôle de gestion de la conformité et de gestion de l’organisation dans la page **autorisations** , dans le centre d’administration Exchange. Pour permettre à un utilisateur pour la recherche dans le journal d’audit Office 365 avec le niveau minimal de privilèges, vous pouvez créer un groupe de rôles personnalisés dans Exchange en ligne, ajouter le rôle journaux d’Audit en affichage seul ou des journaux d’Audit et puis ajouter l’utilisateur en tant que membre du nouveau groupe de rôles. Pour plus d’informations, voir [rôles de gérer les groupes dans Exchange Online](https://go.microsoft.com/fwlink/p/?LinkID=730688).
    
    > [!IMPORTANT]
    > Si vous attribuez à un utilisateur le rôle journaux d’Audit en affichage seul ou des journaux d’Audit dans la page **autorisations** de sécurité &amp; centre de conformité, ils ne pourront recherche Office 365 dans le journal d’audit. Vous devez attribuer les autorisations dans Exchange Online. Il s’agit de l’applet de commande sous-jacent utilisé pour la recherche dans le journal d’audit étant une applet de commande Exchange Online. 
  
- Si vous souhaitez désactiver la recherche du journal d’audit dans Office 365 pour votre organisation, vous pouvez exécuter la commande suivante dans PowerShell distant connecté à votre organisation Exchange Online :
    
  ```
  Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $false
  ```

    Pour réactiver la recherche d’audit, vous pouvez exécuter la commande suivante dans Exchange Online PowerShell :
    
  ```
  Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $true
  ```

    Pour plus d’informations, voir [désactiver la recherche du journal d’audit dans Office 365](turn-audit-log-search-on-or-off.md).
    
- Comme indiqué précédemment, l’applet de commande sous-jacent utilisé pour la recherche dans le journal d’audit est une applet de commande Exchange Online, **UnifiedAuditLog de la recherche**. Cela signifie que vous pouvez utiliser cette applet de commande pour rechercher dans le journal d’audit Office 365 au lieu d’utiliser la page de **recherche des journaux d’Audit de** la sécurité &amp; centre de conformité. Vous devez exécuter cette applet de commande dans PowerShell distant connecté à votre organisation Exchange Online. Pour plus d’informations, voir [UnifiedAuditLog à la recherche](https://go.microsoft.com/fwlink/p/?linkid=834776).
    
- Si vous souhaitez télécharger par programme des données à partir du journal d’audit de Office 365, nous recommandons d’utiliser l’API d’activité de gestion Office 365 au lieu d’utiliser un script PowerShell. L’API d’activité de gestion Office 365 est un service web REST que vous pouvez utiliser pour développer des solutions de surveillance de la conformité pour votre organisation, la sécurité et opérations. Pour plus d’informations, voir [référence des API d’activité de gestion Office 365](https://go.microsoft.com/fwlink/?linkid=852309).
    
- Vous pouvez rechercher le journal d’audit de Office 365 pour les activités qui ont été effectuées au cours des 90 derniers jours.
    
- Il peut prendre jusqu'à 30 minutes ou les 24 heures après un événement se produit pour l’entrée du journal d’audit correspondant à afficher dans les résultats de recherche. Le tableau suivant indique le temps que nécessaire pour les différents services dans Office 365.
    
|**Service Office 365**|**30 minutes**|**24 heures**|
|:-----|:-----|:-----|
|Azure Active Directory (événements d’administration)  <br/> ||![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> |
|Azure Active Directory (événements d’ouverture de session utilisateur)  <br/> ||![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> |
|Exchange Online  <br/> |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> ||
|Microsoft Teams  <br/> |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> ||
|Power BI  <br/> ||![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> |
|Sécurité &amp; centre de conformité  <br/> |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> ||
|Sharepoint Online et OneDrive Entreprise  <br/> |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> ||
|Sway  <br/> ||![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> |
|Yammer  <br/> ||![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> |
   
- Azure Active Directory (AD Azure) est le service d’annuaire pour Office 365. Le journal d’audit unifiée contient l’utilisateur, groupe, application, domaine et activités directory effectuées dans le centre d’administration d’Office 365 ou dans le dans Azure portail de gestion. Pour obtenir une liste complète des événements Azure AD, voir [Événements du rapport d’Audit Azure Active Directory](https://go.microsoft.com/fwlink/p/?LinkID=616549).
    
- Les journaux d’audit Exchange Online se composent de deux types d’événements : les événements d’administration (actions effectuées par les administrateurs) et événements (actions effectuées par les utilisateurs de boîtes aux lettres) de la boîte aux lettres Exchange. Notez que l’audit de boîte aux lettres n’est pas activé par défaut. Il doit être activer pour chaque boîte aux lettres de l’utilisateur avant que les événements de boîte aux lettres peuvent être recherchées dans le journal d’audit d’Office 365. Pour plus d’informations sur l’audit des boîtes aux lettres et de la boîte aux lettres de l’audit des actions que vous avez ouvert une session, voir [Activer la boîte aux lettres de l’audit dans Office 365](enable-mailbox-auditing.md).
    
- Enregistrement d’audit pour Power BI n’est pas activée par défaut. Pour rechercher des activités de Power BI dans le journal d’audit d’Office 365, vous devez activer l’audit dans le portail d’administration Power BI. Pour plus d’informations, voir [L’audit Power BI](https://docs.microsoft.com/power-bi/service-admin-auditing#enabling-auditing-functionality-in-the-power-bi-admin-portal).
    
    
## <a name="search-the-audit-log"></a>Rechercher le journal d’audit

Voici le processus de recherche dans le journal d’audit dans Office 365.
  
[Étape 1 : Exécuter une recherche de journal d’audit](#step-1-run-an-audit-log-search)
  
[Étape 2 : Afficher les résultats de recherche](#step-2-view-the-search-results)

[Étape 3 : Filtrer les résultats de recherche](#step-3-filter-the-search-results)

[Étape 4 : Exporter les résultats de recherche vers un fichier](#step-4-export-the-search-results-to-a-file)
  
### <a name="step-1-run-an-audit-log-search"></a>Étape 1 : Exécuter une recherche de journal d’audit

1. Accédez à [https://protection.office.com](https://protection.office.com).
    
    > [!TIP]
    > Utiliser une session de navigation privée (pas une session standard) pour accéder à la sécurité du Office 365 &amp; , car cela empêche les informations d’identification que vous êtes actuellement connecté avec utilisation du centre de conformité. Pour ouvrir une session de navigation InPrivate dans Internet Explorer ou Microsoft Edge, appuyez sur CTRL + MAJ + P. Pour ouvrir une session de navigation privée dans Google Chrome (appelé une fenêtre incognito), appuyez sur CTRL + MAJ + N. 
  
2. Connectez-vous à Office 365 à l’aide de votre compte professionnel ou de l’école.
    
3. Dans le volet gauche de la sécurité &amp; centre de conformité, cliquez sur **recherche &amp; enquête**, puis cliquez sur **Rechercher des journaux d’Audit**.
    
    La page de **recherche des journaux d’Audit** s’affiche. 
    
    ![Configurer les critères, puis cliquez sur Rechercher pour exécuter des rapports](media/8639d09c-2843-44e4-8b4b-9f45974ff7f1.png)
  
    > [!NOTE]
    > Vous devez activer le premier enregistrement d’audit avant de pouvoir exécuter une recherche de journal d’audit. Si le lien **Démarrer l’enregistrement d’utilisateur et administration activité** s’affiche, cliquez dessus pour activer l’audit. Si vous ne voyez pas ce lien, l’audit a déjà été activé pour votre organisation. 
  
4. Configurer les critères de recherche suivants :
    
1. **Activités** Cliquez sur la liste déroulante pour afficher les activités que vous pouvez rechercher. Activités des utilisateurs et d’administration sont organisées dans vers des groupes d’activités associées. Vous pouvez sélectionner des activités spécifiques ou vous pouvez cliquer sur le nom du groupe activité à sélectionner toutes les activités dans le groupe. Vous pouvez également cliquer sur une activité sélectionnée pour effacer la sélection. Après avoir exécuté la recherche, uniquement les entrées du journal d’audit pour les activités sélectionnées sont affichées. Sélectionnez **Afficher les résultats pour toutes les activités** affiche les résultats de toutes les activités effectuées par l’utilisateur sélectionné ou un groupe d’utilisateurs. 
    
    Plus de 100 activités d’utilisateur et d’administration sont consignées dans le journal d’audit d’Office 365. Cliquez sur l’onglet **activités contrôlé** le sujet de cet article pour consulter les descriptions de chaque activité dans chacun des différents services Office 365. 
    
2. **Date de début** et **date de fin** au cours des sept derniers jours sont sélectionnés par défaut. Sélectionnez une plage de date et heure pour afficher les événements qui se sont produites pendant cette période. La date et l’heure sont présentées au format de temps universel coordonné (UTC). La plage de dates maximale que vous pouvez spécifier est 90 jours. Une erreur s’affiche si la plage de dates sélectionnée est supérieure à 90 jours. 
    
    > [!TIP]
    > Si vous utilisez la plage de dates maximale de 90 jours, sélectionnez l’heure actuelle à la **date de début**. Sinon, vous recevrez une erreur indiquant que la date de début est antérieure à la date de fin. Si vous avez activé l’audit dans les 90 derniers jours, la plage de dates maximale ne peut pas démarrer avant la date à laquelle l’audit a été activé. 
  
3. **Utilisateurs** Cliquez dans cette zone, puis sélectionnez un ou plusieurs utilisateurs pour afficher les résultats de recherche. Les entrées du journal d’audit pour l’activité sélectionnée effectuées par les utilisateurs que vous sélectionnez dans cette zone sont affichées dans la liste des résultats. Laissez cette zone vide de renvoi des entrées pour tous les utilisateurs (et les comptes de service) dans votre organisation. 
    
4. **Fichier ou dossier** Tapez une partie ou la totalité d’un nom de fichier ou un dossier pour rechercher des activités liées au fichier du dossier qui contient le mot clé spécifié. Vous pouvez également spécifier une URL d’un fichier ou un dossier. Si vous utilisez une URL, assurez-vous que le type le chemin d’URL complète ou si vous tapez uniquement une partie de l’URL, n’incluez pas des caractères spéciaux ou des espaces. 
    
    Laissez cette zone vide de renvoi des entrées pour tous les fichiers et dossiers dans votre organisation.
    
5. Cliquez sur **Rechercher** pour lancer la recherche à l’aide de vos critères de recherche. 
    
    Les résultats de recherche sont chargés, et après quelques instants, ils sont affichent sous **résultats**. Lors de la recherche est terminée, le nombre de résultats de la recherche s’affiche. Notez qu’un maximum de 5 000 événements s’affichera dans le volet **résultats** , par incréments de 150 événements ; Si plus de 5 000 événements répondent aux critères de recherche, les événements de 5 000 plus récents sont affichés. 
    
    ![Le nombre de résultats s’affichent une fois que la recherche est terminée.](media/986216f1-ca2f-4747-9480-e232b5bf094c.png)
  
  
#### <a name="tips-for-searching-the-audit-log"></a>Conseils pour la recherche dans le journal d’audit

- Vous pouvez sélectionner les activités spécifiques à rechercher en cliquant sur le nom de l’activité. Ou vous pouvez rechercher toutes les activités dans un groupe (par exemple, les **activités de fichiers et de dossiers**) en cliquant sur le nom du groupe. Si une activité est sélectionnée, vous pouvez cliquer dessus pour annuler la sélection. Vous pouvez également utiliser la zone de recherche pour afficher les activités qui contiennent le mot clé que vous tapez.
    
    ![Cliquez sur le nom du groupe activité à sélectionner toutes les activités](media/3cde97cb-6f35-47c0-8612-ecd9c6ac36a3.png)
  
- Vous devez sélectionner **Afficher les résultats pour toutes les activités** dans la liste des **activités** pour afficher les événements dans le journal d’audit d’administration Exchange. Événements ce journal d’audit d’affichent un nom de l’applet de commande (par exemple, **Set-Mailbox** ) dans la colonne de **l’activité** dans les résultats. Pour plus d’informations, cliquez sur l’onglet **activités contrôlé** dans cette rubrique, puis sur **les activités d’administration Exchange**.
    
    De même, il existe des activités d’audit qui n’ont pas un élément correspondant dans la liste des **activités** . Si vous connaissez le nom de l’opération pour ces activités, vous pouvez rechercher toutes les activités, puis filtrer les résultats en tapant le nom de l’opération dans la zone de la colonne de **l’activité** . Voir [étape 3 : filtrer les résultats de recherche](#step-3-filter-the-search-results) pour plus d’informations sur le filtrage des résultats. 
    
- Cliquez sur **Effacer** pour effacer les critères de recherche en cours. La plage de dates renvoie la valeur par défaut au cours des sept derniers jours. Vous pouvez également cliquer sur **Effacer tout pour afficher les résultats pour toutes les activités** pour annuler toutes les activités sélectionnées. 
    
- Si 5 000 résultats sont détectés, vous pouvez supposer que plus de 5 000 événements qui répondent aux critères de recherche. Vous pouvez affiner les critères de recherche et relancez la recherche pour renvoyer le nombre de résultats, ou vous pouvez exporter tous les résultats de recherche en sélectionnant **Exporter les résultats de** \> **Téléchargez tous les résultats**.

  
### <a name="step-2-view-the-search-results"></a>Étape 2 : Afficher les résultats de recherche

Les résultats d’une recherche de journal d’audit sont affichés sous **résultats** sur la page de **recherche des journaux d’Audit de** . Comme indiqué plus haut un maximum de 5 000 événements (les plus récentes) sont affichés par incréments de 150 événements. Pour afficher davantage d’événements vous pouvez utiliser la barre de défilement dans le volet **résultats** , ou vous pouvez appuyer sur **MAJ + fin** pour afficher les événements ensuite 150. 
  
Les résultats contiennent les informations suivantes sur chaque événement renvoyé par la recherche.
  
- **Date :** La date et l’heure (au format UTC) lorsque l’événement s’est produite. 
    
- **Adresse IP :** L’adresse IP du périphérique qui a été utilisé lors de l’activité a été enregistrée. L’adresse IP est affichée dans le format d’adresse IPv4 ou IPv6. 
    
- **Utilisateur :** Le compte d’utilisateur (ou service) qui a effectué l’action qui a déclenché l’événement. 
    
- **Activité :** L’activité effectuée par l’utilisateur. Cette valeur correspond aux activités que vous avez sélectionné dans la liste déroulante **activités** . Pour un événement dans le journal d’audit d’administration Exchange, la valeur dans cette colonne est une cmdlet Exchange. 
    
- **Élément :** L’objet qui a été créé ou modifié à la suite de l’activité correspondante. Par exemple, le fichier qui a été vus ou modifié ou le compte d’utilisateur qui a été mis à jour. Pas toutes les activités ont une valeur dans cette colonne. 
    
- **Détails :** Plus de détails sur une activité. Là encore, pas toutes les activités aura une valeur. 
    
> [!TIP]
> Sous **résultats** pour trier les résultats, cliquez sur un en-tête de colonne. Vous pouvez trier les résultats de A à Z ou de Z à A. Cliquez sur l’en-tête de **Date** pour trier les résultats de la plus ancienne plus récent au plus ancien ou plus récent. 
  
#### <a name="view-the-details-for-a-specific-event"></a>Afficher les détails d’un événement spécifique

Vous pouvez afficher plus d’informations sur un événement en cliquant sur l’enregistrement des événements dans la liste des résultats de recherche. Une page de **Détails** s’affiche qui contient les propriétés détaillées de l’enregistrement de l’événement. Les propriétés qui sont affichées dépendent du service Office 365 dans lequel l’événement se produit. Pour afficher les détails, cliquez sur **plus d’informations**. Pour obtenir des descriptions, voir le [journal d’audit de propriétés détaillées dans Office 365](detailed-properties-in-the-office-365-audit-log.md).
  
![Cliquez sur plus d’informations pour afficher les propriétés détaillées de l’enregistrement du journal d’événements d’audit](media/6df582ae-d339-4735-b1a6-80914fb77a08.png)

  
### <a name="step-3-filter-the-search-results"></a>Étape 3 : Filtrer les résultats de recherche

En plus de tri, vous pouvez également filtrer les résultats d’une recherche de journal d’audit. Il s’agit d’une fonctionnalité très qui peut vous aider à rapidement filtrer les résultats pour un utilisateur spécifique ou une activité. Vous pouvez créer à l’origine une recherche à l’échelle et puis rapidement filtrer les résultats pour voir les événements spécifiques. Ensuite, vous pouvez limiter les critères de recherche et réexécuter la recherche pour renvoyer un ensemble de résultats plus petit, plus court.
  
Pour filtrer les résultats :
  
1. Exécuter une recherche de journal d’audit.
    
2. Lorsque les résultats sont affichés, cliquez sur **filtrer les résultats**.
    
    Zones de mot clé sont affichés sous chaque en-tête de colonne.
    
3. Cliquez sur l’une des cases sous un en-tête de colonne, tapez un mot ou une phrase, en fonction de la colonne que vous filtrez sur. Les résultats seront dynamiquement Ajustez à nouveau pour afficher les événements qui correspondent à votre filtre.
    
    ![Tapez un mot dans le filtre pour afficher les événements qui correspondent au filtre](media/542dc323-a997-402c-934b-cc5e218e50bc.png)
  
4. Pour effacer un filtre, cliquez sur le **X** dans la zone Filtre ou cliquer sur **Masquer le filtrage**.
    
> [!TIP]
> Pour afficher les événements dans le journal d’audit d’administration Exchange, tapez un **-** (tiret) dans la zone de filtre **d’activité** . Noms d’applet de commande, qui sont affichés dans la colonne **d’activité** pour les événements d’administration Exchange s’affiche. Vous pouvez ensuite trier les noms d’applet de commande dans l’ordre alphabétique. 

### <a name="step-4-export-the-search-results-to-a-file"></a>Étape 4 : Exporter les résultats de recherche vers un fichier

Vous pouvez exporter les résultats d’une recherche de journal d’audit pour un fichier de valeurs séparées (CSV) sur votre ordinateur local. Vous pouvez ouvrir ce fichier dans Microsoft Excel et utiliser des fonctionnalités telles que la recherche, tri, filtrage et fractionnement d’une seule colonne (qui contient les cellules de valeurs multiples) dans plusieurs colonnes.
  
1. Exécuter une recherche de journal d’audit, puis modifier les critères de recherche jusqu'à ce que vous ayez les résultats souhaités.
    
2. Cliquez sur **Exporter les résultats** , sélectionnez une des options suivantes : 
    
  - **Enregistrer les résultats chargés** Choisissez cette option pour exporter uniquement les entrées qui sont affichent sous **résultats** sur la ** recherche des journaux d’Audit ** page. Le fichier CSV qui est téléchargé contient les mêmes colonnes (et données) affiché dans la page (Date, utilisateur, les activités, élément et plus d’informations). Une colonne supplémentaire (appelée **plus**) est incluse dans le fichier CSV qui contient plus d’informations à partir de l’entrée du journal d’audit. Étant donné que vous exportez les mêmes résultats qui sont chargés (et visible) dans la page de **recherche des journaux d’Audit** , un maximum de 5 000 entrées sont exportées. 
    
  - **Téléchargez tous les résultats** Choisissez cette option pour exporter toutes les entrées du journal d’audit de Office 365 qui répondent aux critères de recherche. Pour un grand ensemble de résultats de la recherche, choisissez cette option pour télécharger toutes les entrées du journal d’audit en plus de 5 000 résultats peuvent être affichés sur la page de **recherche des journaux d’Audit de** . Cette option télécharge les données brutes du journal d’audit dans un fichier CSV et contient des informations supplémentaires à partir de l’entrée du journal d’audit dans une colonne nommée **AuditData**. Elle peut prendre plus de temps pour télécharger le fichier si vous choisissez cette option Exporter, car le fichier peut être beaucoup plus volumineux que celui qui est téléchargé si vous choisissez l’option autres.
    
    > [!IMPORTANT]
    > Vous pouvez télécharger un maximum de 50 000 entrées dans un fichier CSV à partir d’une recherche de journal d’audit unique. Si 50 000 entrées sont téléchargées vers le fichier CSV, vous pouvez supposer que plus de 50 000 événements qui répondent aux critères de recherche. Pour exporter le plus de cette limite, essayez d’utiliser une plage de dates pour réduire le nombre d’entrées du journal d’audit. Vous devrez peut-être effectuer plusieurs recherches plus petite plage de dates pour exporter des entrées de plus de 50 000. 
  
3. Après avoir sélectionné une option d’exportation, un message s’affiche en bas de la fenêtre qui vous invite à ouvrir le fichier CSV, enregistrez-le dans le dossier téléchargements ou enregistrez-le dans un dossier spécifique.

  
#### <a name="more-information-about-exporting-audit-log-search-results"></a>Plus d’informations sur l’exportation de résultats de recherche du journal d’audit

- L’option de **téléchargement de tous les résultats** télécharge les données brutes à partir du journal d’audit de Office 365 dans un fichier CSV. Ce fichier contient les noms de colonne différents (CreationDate, UserIds, opération, AuditData) que le fichier est téléchargé si vous sélectionnez l’option **Enregistrer les résultats chargés** . Les valeurs dans les deux fichiers CSV différents pour la même activité peuvent également être différentes. Par exemple, l’activité dans la colonne **Action** du CSV du fichier et peut avoir une valeur autre que la version « conviviale » qui s’affiche dans la colonne de **l’activité** sur la page de **recherche des journaux d’Audit** ; par exemple, MailboxLogin et utilisateur connecté à la boîte aux lettres.
    
- Si vous téléchargez tous les résultats, le fichier CSV contient une colonne nommée **AuditData**, qui contient des informations supplémentaires sur chaque événement. Comme indiqué précédemment, cette colonne contient une propriété à valeurs multiples pour plusieurs propriétés de l’enregistrement du journal d’audit. Chacune des paires **: valeur de la propriété** dans cette propriété à valeurs multiples sont séparés par une virgule. Vous pouvez utiliser la requête d’alimentation dans Excel pour fractionner cette colonne sur plusieurs colonnes afin que chaque propriété possède sa propre colonne. Cela vous permet de trier et filtrer sur un ou plusieurs de ces propriétés. Pour savoir comment procéder, voir la section « Fractionner une colonne par délimiteur » dans [une colonne de texte (requête Power) de fractionnement](https://support.office.com/article/5282d425-6dd0-46ca-95bf-8e0da9539662).
    
    Une fois que vous avez séparé la colonne **AuditData** , vous pouvez filtrer la colonne **opérations** pour afficher les propriétés détaillées d’un type spécifique d’activité. 
    
- Il existe une limite de caractères 3,060 pour les données qui s’affiche dans le champ **AuditData** pour un enregistrement d’audit. Si la limite de caractères 3,060 est dépassée, les données dans ce champ sont tronquées. 
    
- Lorsque vous téléchargez tous les résultats d’une requête de recherche qui contient les événements à partir de différents services Office 365, la colonne **AuditData** dans le fichier CSV contient des propriétés différentes selon ce service l’action a été effectuée dans. Par exemple, les entrées de journaux d’audit Exchange et Azure AD incluent une propriété nommée **ResultStatus** qui indique si l’action a réussi ou non. Cette propriété n’est pas incluse pour les événements dans SharePoint. De même, les événements SharePoint ont une propriété qui identifie le site activités liées à l’URL pour les fichiers et dossiers. Pour modifier ce comportement, envisagez d’utiliser des recherches différentes pour exporter les résultats des activités d’un seul service. 
    
    Pour obtenir une description des propriétés qui sont répertoriés dans la colonne **AuditData** dans le fichier CSV lorsque vous téléchargez tous les résultats et le service de chaque 1 s’applique à, consultez le [journal d’audit de propriétés détaillées dans Office 365](detailed-properties-in-the-office-365-audit-log.md).

  
## <a name="audited-activities"></a>Audit des activités

Les tableaux de cette section décrivent les activités audités dans Office 365. Vous pouvez rechercher ces événements en recherchant l’audit journal de la sécurité &amp; centre de conformité. Cliquez sur l’onglet **recherche le journal d’audit** pour obtenir des instructions pas à pas. 
  
Ces tables groupe activités associées ou les activités d’un service spécifique d’Office 365. Les tableaux incluent le nom convivial qui s’affiche dans la liste déroulante des **activités** et le nom de l’opération correspondante qui s’affiche dans les informations détaillées d’un enregistrement d’audit, dans le fichier CSV lorsque vous exportez les résultats de recherche. Pour obtenir des descriptions des informations détaillées, consultez le [journal d’audit de propriétés détaillées dans Office 365](detailed-properties-in-the-office-365-audit-log.md).
  
Cliquez sur un des liens suivants pour accéder à une table spécifique.
  
||||
|:-----|:-----|:-----|
|[Activités de fichier et de page](#file-and-page-activities)<br/> |[Activités de dossier](#folder-activities)<br/> |[Activités de demande de partage et d’accès](#sharing-and-access-request-activities)<br/> |
|[Activités de synchronisation](#synchronization-activities)<br/> |[Activités de l’administration de site](#site-administration-activities)<br/> |[Activités de boîte aux lettres Exchange](#exchange-mailbox-activities)<br/> |
|[Balancement des activités](#sway-activities) <br/> |[Activités de l’administration des utilisateurs](#user-administration-activities) <br/> |[Activités de l’administration du groupe AD Azure](#azure-ad-group-administration-activities) <br/> |
|[Activités de l’administration d’applications](#application-administration-activities) <br/> |[Activités de l’administration des rôles](#role-administration-activities) <br/> |[Opérations de l’administration d’annuaire](#directory-administration-activities) <br/> |
|[activités de découverte électronique](#ediscovery-activities) <br/> |[Activités de Power BI](#power-bi-activities) <br/> |[Activités Microsoft Teams](#microsoft-teams-activities) <br/> |
|[Activités de Yammer](#yammer-activities) <br/> |[Microsoft Stream](#microsoft-stream) <br/> |[Journal d’audit de l’administrateur Exchange](#exchange-admin-audit-log) <br/> |
   
  
### <a name="file-and-page-activities"></a>Activités de fichier et de page
  
Le tableau suivant décrit les activités de fichier et de page dans SharePoint Online et OneDrive for Business.
  
|**Nom convivial**|**Operation**|**Description**|
|:-----|:-----|:-----|
|Accès aux fichiers  <br/> |FileAccessed  <br/> |Compte d’utilisateur ou le système accède à un fichier.  <br/> |
|(aucun)  <br/> |FileAccessedExtended  <br/> |Cela est liée dans le fichier « accès » activité (FileAccessed). Un événement FileAccessedExtended est enregistré lors de la même personne en permanence accède à un fichier pour une longue période de temps (jusqu'à 3 heures). L’objectif de la journalisation des événements FileAccessedExtended consiste à réduire le nombre d’événements FileAccessed enregistrés lorsqu’un fichier est accessible en permanence. Cela permet de réduire le bruit de plusieurs enregistrements FileAccessed pour ce qui est identique à celui de l’activité des utilisateurs et vous pouvez vous concentrer sur l’événement FileAccessed initiale (et plus important).  <br/> |
|Fichier d’archivage  <br/> |FileCheckedIn  <br/> |L’utilisateur archive un document qui ils extrait à partir d’une bibliothèque de documents.  <br/> |
|Extrait le fichier  <br/> |FileCheckedOut  <br/> |Utilisateur extrait un document situé dans une bibliothèque de documents. Les utilisateurs peuvent extraire et apporter des modifications à des documents qui ont été partagés avec eux.  <br/> |
|Fichier copié  <br/> |FileCopied  <br/> |Utilisateur copie un document à partir d’un site. Le fichier copié peut être enregistré dans un autre dossier sur le site.  <br/> |
|Fichier supprimé  <br/> |FileDeleted  <br/> |Utilisateur supprime un document d’un site.  <br/> |
|Fichier supprimé à partir de la Corbeille  <br/> |FileDeletedFirstStageRecycleBin  <br/> |Utilisateur supprime un fichier à partir de la Corbeille d’un site.  <br/> |
|Fichier supprimé à partir de la Corbeille secondaire  <br/> |FileDeletedSecondStageRecycleBin  <br/> |Utilisateur supprime un fichier de la Corbeille de deuxième niveau d’un site.  <br/> |
|Programme malveillant détecté dans le fichier  <br/> |FileMalwareDetected  <br/> |Moteur d’antivirus SharePoint détecte les logiciels malveillants dans un fichier.  <br/> |
|Extraction du fichier ignoré  <br/> |FileCheckOutDiscarded  <br/> |L’utilisateur ignore (ou annule) un fichier extrait. Cela signifie que toutes les modifications apportées au fichier alors qu’il était extrait sont ignorées et ne sont pas enregistrées dans la version du document qui se trouve dans la bibliothèque de documents.  <br/> |
|Fichier téléchargé  <br/> |FileDownloaded  <br/> |Utilisateur télécharge un document à partir d’un site.  <br/> |
|Fichier modifié  <br/> |FileModified  <br/> |Compte d’utilisateur ou système modifie le contenu ou les propriétés d’un document situé sur un site.  <br/> |
|(aucun)  <br/> |FileModifiedExtended  <br/> |Ceci est lié à « le fichier modifié » activité (FileModified). Un événement FileModifiedExtended est enregistré lors de la même personne modifie régulièrement un fichier pour une longue période de temps (jusqu'à 3 heures). L’objectif de la journalisation des événements FileModifiedExtended consiste à réduire le nombre d’événements FileModified qui sont enregistrés lorsqu’un fichier est modifié en permanence. Cela permet de réduire le bruit de plusieurs enregistrements FileModified pour ce qui est identique à celui de l’activité des utilisateurs et vous pouvez vous concentrer sur l’événement FileModified initiale (et plus important).  <br/> |
|Fichier déplacé  <br/> |Fichier déplacé  <br/> |Utilisateur déplace un document à partir de son emplacement actuel sur un site vers un nouvel emplacement.  <br/> |
|Recyclés toutes les versions secondaires du fichier  <br/> |FileVersionsAllMinorsRecycled  <br/> |Utilisateur supprime toutes les versions secondaires de l’historique des versions d’un fichier. Les versions supprimées sont déplacées vers la Corbeille du site.  <br/> |
|Recyclés toutes les versions de fichier  <br/> |FileVersionsAllRecycled  <br/> |Utilisateur supprime toutes les versions de l’historique des versions d’un fichier. Les versions supprimées sont déplacées vers la Corbeille du site.  <br/> |
|Version recyclée du fichier  <br/> |FileVersionRecycled  <br/> |Utilisateur supprime une version de l’historique des versions d’un fichier. La version supprimée est déplacée vers la Corbeille du site.  <br/> |
|Fichier renommé  <br/> |FileRenamed  <br/> |Utilisateur renomme un document sur un site.  <br/> |
|Fichier restauré  <br/> |FileRestored  <br/> |Utilisateur restaure un document à partir de la Corbeille d’un site.  <br/> |
|Fichier téléchargé  <br/> |FileUploaded  <br/> |Utilisateur télécharge un document dans un dossier sur un site.  <br/> |
|Page affichée  <br/> |PageViewed  <br/> |Utilisateur visualise une page sur un site. Cela n’inclut pas à l’aide d’un navigateur Web pour afficher les fichiers situés dans une bibliothèque de documents.  <br/> |
|(aucun)  <br/> |PageViewedExtended  <br/> |Ceci est lié à la page « Affichage » activité (PageViewed). Un événement PageViewedExtended est enregistré lors de la même personne affiche en permanence une page web pour une longue période de temps (jusqu'à 3 heures). L’objectif de la journalisation des événements PageViewedExtended consiste à réduire le nombre d’événements PageViewed qui sont enregistrés lorsqu’une page est affichée en permanence. Cela permet de réduire le bruit de plusieurs enregistrements PageViewed pour ce qui est identique à celui de l’activité des utilisateurs et vous pouvez vous concentrer sur l’événement PageViewed initiale (et plus important).  <br/> |
  
### <a name="folder-activities"></a>Activités de dossier
  
Le tableau suivant décrit les activités de dossier dans SharePoint Online et OneDrive for Business.
  
|**Nom convivial**|**Operation**|**Description**|
|:-----|:-----|:-----|
|Dossier copié  <br/> |FolderCopied  <br/> |Utilisateur copie un dossier d’un site vers un autre emplacement dans SharePoint ou OneDrive for Business.  <br/> |
|Dossier créé  <br/> |FolderCreated  <br/> |Utilisateur crée un dossier sur un site.  <br/> |
|Dossier supprimé  <br/> |FolderDeleted  <br/> |Utilisateur supprime un dossier d’un site.  <br/> |
|Dossier supprimé à partir de la Corbeille  <br/> |FolderDeletedFirstStageRecycleBin  <br/> |Utilisateur supprime un dossier de la Corbeille sur un site.  <br/> |
|Dossier supprimé à partir de la Corbeille secondaire  <br/> |FolderDeletedSecondStageRecycleBin  <br/> |Utilisateur supprime un dossier de la Corbeille secondaire sur un site.  <br/> |
|Dossier modifié  <br/> |FolderModified  <br/> |Utilisateur modifie un dossier sur un site. Cela implique de changer les métadonnées de dossier, telle que la modification des balises et des propriétés.  <br/> |
|Dossier déplacé  <br/> |FolderMoved  <br/> |Utilisateur déplace un dossier à un autre emplacement sur un site.  <br/> |
|Dossier renommé  <br/> |FolderRenamed  <br/> |Utilisateur renomme un dossier sur un site.  <br/> |
|Dossier restauré  <br/> |FolderRestored  <br/> |Utilisateur restaure un dossier supprimé à partir de la Corbeille sur un site.  <br/> |
  
### <a name="sharing-and-access-request-activities"></a>Activités de demande de partage et d’accès
  
Le tableau suivant décrit les activités utilisateur de demande de partage et d’accès dans SharePoint Online et OneDrive for Business. Pour partager des événements, la colonne **Détail** sous **résultats** identifie le nom de l’utilisateur ou le groupe d’avec que l’élément a été partagé, et si cet utilisateur ou ce groupe est un membre ou les invités dans votre organisation. Pour plus d’informations, voir [utiliser le partage d’audit dans le journal d’audit d’Office 365](use-sharing-auditing.md).
  
> [!NOTE]
> Les utilisateurs peuvent être *membres* ou *invités* , en fonction de la propriété UserType de l’objet utilisateur. Un membre est généralement un employé et invité est généralement un collaborateur à l’extérieur de votre organisation. Lorsqu’un utilisateur accepte une invitation de partage (et n’est pas déjà partie de votre organisation), un compte invité est créé pour eux dans l’annuaire de votre organisation. Une fois que l’utilisateur invité dispose d’un compte dans votre répertoire, ressources peuvent être partagées directement avec eux (sans nécessiter une invitation). 
  
|**Nom convivial**|**Operation**|**Description**|
|:-----|:-----|:-----|
|Acceptation des demandes d’accès  <br/> |AccessRequestAccepted  <br/> |Une demande d’accès à un site, le dossier ou le document a été acceptée et l’utilisateur a accès.  <br/> |
|Accepté l’invitation de partage  <br/> |SharingInvitationAccepted  <br/> |Utilisateur (membre ou invité) accepté une invitation de partage et a été accordé l’accès à une ressource. Cet événement consacrée des informations sur l’utilisateur qui a été invité et l’adresse de messagerie qui a été utilisé pour accepter l’invitation (il peuvent être différents). Cette activité est souvent accompagnée d’un second événement qui décrit comment l’utilisateur a accès à la ressource, par exemple, les utilisateurs ajoutés à un groupe qui a accès à la ressource.  <br/> |
|Niveau d’autorisation ajouté à la collection de sites  <br/> |PermissionLevelAdded  <br/> |Un niveau d’autorisation a été ajouté à une collection de sites.  <br/> |
|Utilisateur ajouté à un lien sécurisé  <br/> |AddedToSecureLink  <br/> |Un utilisateur a été ajouté à la liste des entités qui peuvent utiliser ce lien de partage d’informations sécurisé.  <br/> |
|Bloqué l’invitation de partage  <br/> |SharingInvitationBlocked  <br/> | Une invitation de partage envoyée par un utilisateur dans votre organisation est bloquée en raison d’une stratégie de partage externe qui autorise ou refuse partage externe basés sur le domaine de l’utilisateur cible. Dans ce cas, l’invitation de partage a été bloquée car :<br/>  Domaine de l’utilisateur cible n’est pas inclus dans la liste des domaines autorisés.  <br/>  Ou  <br/>  Domaine de l’utilisateur cible est inclus dans la liste des domaines bloqués.  <br/>  Pour plus d’informations sur Autoriser ou bloquer un partage externe basée sur les domaines, voir [domaines restreints partage dans SharePoint Online et OneDrive for Business](https://support.office.com/article/5d7589cd-0997-4a00-a2ba-2320ec49c4e9).  <br/> |
|L’héritage des autorisations au niveau de s’est arrêtée  <br/> |PermissionLevelsInheritanceBroken  <br/> |Un élément a été modifié de sorte qu’il n’est plus hérite des niveaux d’autorisation à partir de son parent.  <br/> |
|A interrompu l’héritage des autorisations de partage  <br/> |SharingInheritanceBroken  <br/> |Un élément a été modifié de sorte qu’il n’est plus hérite les autorisations de partage à partir de son parent.  <br/> |
|Création d’un lien partageables société  <br/> |CompanyLinkCreated  <br/> |Utilisateur créé un lien de l’entreprise à une ressource. échelle de la société liens peut uniquement être utilisés par les membres de votre organisation. Ils ne peuvent pas être utilisés par les invités.  <br/> |
|Création de demandes d’accès  <br/> |AccessRequestCreated  <br/> |Utilisateur demande l’accès à un site, dossier, document ou à qu'ils ne disposent d’autorisations d’accès.  <br/> |
|Création d’un lien anonyme  <br/> |AnonymousLinkCreated  <br/> |Créé un lien vers une ressource anonyme par l’utilisateur. Toute personne possédant ce lien peut accéder à la ressource sans avoir à être authentifiés.  <br/> |
|Lien d’informations sécurisé  <br/> |SecureLinkCreated  <br/> |Un lien sécurisé de partage a été créé pour cet élément.  <br/> |
|Invitation de partage créée  <br/> |SharingInvitationCreated  <br/> |Utilisateur partagé une ressource dans SharePoint Online ou OneDrive entreprise avec un utilisateur qui ne figure pas dans l’annuaire de votre organisation.  <br/> |
|Lien sécurisé supprimée  <br/> |SecureLinkDeleted  <br/> |Un lien sécurisé de partage a été supprimé.  <br/> |
|Refus des demandes d’accès  <br/> |AccessRequestDenied  <br/> |Une demande d’accès à un site, le dossier ou le document a été refusée.  <br/> |
|Niveau d’autorisation modification sur la collection de sites  <br/> |PermissionLevelModified  <br/> |Un niveau d’autorisation a été modifié sur une collection de sites.  <br/> |
|Supprimer un lien partageables société  <br/> |CompanyLinkRemoved  <br/> |Utilisateur supprimé un lien de l’entreprise à une ressource. Le lien ne puisse plus être utilisé pour accéder à la ressource.  <br/> |
|Supprimer un lien anonyme  <br/> |AnonymousLinkRemoved  <br/> |Utilisateur supprimé un lien vers une ressource anonyme. Le lien ne puisse plus être utilisé pour accéder à la ressource.  <br/> |
|Supprimer un niveau d’autorisation à partir de la collection de sites  <br/> |PermissionLevelRemoved  <br/> |Un niveau d’autorisation a été supprimé à partir d’une collection de sites.  <br/> |
|Restaurer l’héritage des autorisations de partage  <br/> |SharingInheritanceReset  <br/> |Une modification a été apportée afin qu’un élément hérite des autorisations de partage de son parent.  <br/> |
|Fichier partagé, dossier ou site  <br/> |SharingSet  <br/> |Utilisateur (membre ou invité) partagé un fichier, un dossier ou un site SharePoint ou OneDrive entreprise avec un utilisateur dans l’annuaire de votre organisation. La valeur dans la colonne de **Détails** pour cette activité identifie le nom de l’utilisateur d’avec que la ressource a été partagée et si cet utilisateur est membre ou invité. Cette activité est souvent accompagnée d’un second événement qui décrit la façon dont l’utilisateur a été accordé l’accès à la ressource ; par exemple, ajout de l’utilisateur à un groupe qui a accès à la ressource.<br/> |
|Demande d’accès mis à jour  <br/> |AccessRequestUpdated  <br/> |Une demande d’accès à un élément a été mis à jour.  <br/> |
|Mise à jour d’une liaison anonyme  <br/> |AnonymousLinkUpdated  <br/> |Utilisateur mis à jour une liaison anonyme pour une ressource. Le champ mise à jour est inclus dans la propriété EventData lorsque vous exportez les résultats de recherche.  <br/> |
|Mise à jour d’invitation de partage  <br/> |SharingInvitationUpdated  <br/> |Une invitation de partage externe a été mis à jour.  <br/> |
|Cliquez sur un lien anonyme  <br/> |AnonymousLinkUsed  <br/> |Un utilisateur anonyme accéder à une ressource à l’aide d’une liaison anonyme. Identité de l’utilisateur peut être inconnue, mais vous pouvez obtenir d’autres détails tels que les adresses IP de l’utilisateur.  <br/> |
|Fichier partagé, dossier ou site  <br/> |SharingRevoked  <br/> |Utilisateur (membre ou invité) non partagé un fichier, un dossier ou un site qui a été précédemment partagée avec un autre utilisateur.  <br/> |
|Utiliser un lien partageables société  <br/> |CompanyLinkUsed  <br/> |Utilisateur accéder à une ressource à l’aide d’un lien de l’entreprise.  <br/> |
|Cliquez sur lien sécurisé  <br/> |SecureLinkUsed  <br/> |Un utilisateur utilisé un lien sécurisé.  <br/> |
|Utilisateur ajouté à un lien sécurisé  <br/> |AddedToSecureLink  <br/> |Un utilisateur a été ajouté à la liste des entités qui peuvent utiliser un lien de partage d’informations sécurisé.  <br/> |
|Utilisateur supprimé de lien sécurisé  <br/> |RemovedFromSecureLink  <br/> |Un utilisateur a été supprimé de la liste des entités qui peuvent utiliser un lien de partage d’informations sécurisé.  <br/> |
|Retirée d’invitation de partage  <br/> |SharingInvitationRevoked  <br/> |Utilisateur utilisés à une invitation de partage à une ressource.  <br/> |
  
### <a name="synchronization-activities"></a>Activités de synchronisation
  
Le tableau suivant répertorie les activités de la synchronisation de fichier dans SharePoint Online et OneDrive for Business.
  
|**Nom convivial**|**Operation**|**Description**|
|:-----|:-----|:-----|
|Autorisé d’ordinateur pour synchroniser des fichiers  <br/> |ManagedSyncClientAllowed  <br/> |Utilisateur a réussi à établir une relation de synchronisation avec un site. La relation de synchronisation réussit, car l’ordinateur de l’utilisateur est un membre d’un domaine qui a été ajouté à la liste des domaines (appelée la *liste des destinataires approuvés* ) qui peut accéder aux bibliothèques de documents dans votre organisation.<br/> Pour plus d’informations sur cette fonctionnalité, voir [Use Windows PowerShell cmdlets pour activer la synchronisation de OneDrive pour les domaines qui figurent sur la liste des destinataires approuvés](https://go.microsoft.com/fwlink/p/?LinkID=534609).  <br/> |
|Bloquer la synchronisation des fichiers de l’ordinateur  <br/> |UnmanagedSyncClientBlocked  <br/> |Utilisateur tente d’établir une relation de synchronisation avec un site à partir d’un ordinateur qui n’est pas un membre du domaine de votre organisation ou est un membre d’un domaine qui n’a pas été ajouté à la liste des domaines (appelé le *liste des destinataires approuvés)* qui peut accéder aux documents bibliothèques dans votre organisation. La relation de synchronisation n’est pas autorisée et ordinateur de l’utilisateur est bloqué à partir de la synchronisation, le téléchargement ou téléchargement de fichiers dans une bibliothèque de documents.<br/> Pour plus d’informations sur cette fonctionnalité, voir [Use Windows PowerShell cmdlets pour activer la synchronisation de OneDrive pour les domaines qui figurent sur la liste des destinataires approuvés](https://go.microsoft.com/fwlink/p/?LinkID=534609).  <br/> |
|Fichiers téléchargés vers l’ordinateur  <br/> |FileSyncDownloadedFull  <br/> |Utilisateur établit une relation de synchronisation et télécharge correctement des fichiers pour la première fois sur leur ordinateur à partir d’une bibliothèque de documents.  <br/> |
|Modifications du fichier téléchargé sur ordinateur  <br/> |FileSyncDownloadedPartial  <br/> |Utilisateur télécharge correctement les modifications aux fichiers à partir d’une bibliothèque de documents. Cette activité indique que les modifications qui ont été apportées aux fichiers dans la bibliothèque de documents ont été téléchargées vers l’ordinateur de l’utilisateur. Seules les modifications ont été téléchargées, car la bibliothèque de documents a été préalablement téléchargée par l’utilisateur (comme indiqué par l’activité **téléchargé les fichiers de l’ordinateur** ).<br/> |
|Fichiers téléchargés vers la bibliothèque de documents  <br/> |FileSyncUploadedFull  <br/> |Utilisateur distant établit une relation de synchronisation et télécharge correctement les fichiers pour la première fois à partir de leur ordinateur à une bibliothèque de documents.  <br/> |
|Modifications du fichier téléchargé vers la bibliothèque de documents  <br/> |FileSyncUploadedPartial  <br/> |Utilisateur télécharge correctement les modifications aux fichiers dans une bibliothèque de documents. Cet événement indique que les modifications apportées à la version locale d’un fichier à partir d’une bibliothèque de documents sont correctement téléchargées vers la bibliothèque de documents. Seules les modifications sont déchargées parce que ces fichiers ont été précédemment téléchargés par l’utilisateur (comme indiqué par le ** les fichiers téléchargés vers la bibliothèque de documents ** activité).  <br/> |
  
### <a name="site-administration-activities"></a>Activités de l’administration de site
  
Le tableau suivant répertorie les événements qui résultent de tâches d’administration de site dans SharePoint Online.
  
|**Nom convivial**|**Operation**|**Description**|
|:-----|:-----|:-----|
|Ajout des agents utilisateurs exemptés  <br/> |ExemptUserAgentSet  <br/> |Un administrateur global ou SharePoint ajoute un agent utilisateur à la liste des agents utilisateurs exemptés dans le centre d’administration de SharePoint.  <br/> |
|Administrateur de collection de site ajouté  <br/> |SiteCollectionAdminAdded  <br/> |Administrateur de collection de sites ou propriétaire ajoute une personne comme un administrateur de collection de sites pour un site. Administrateurs de collection de sites ont des autorisations Contrôle total pour la collection de sites et tous ses sous-sites.  <br/> |
|Ajout d’utilisateur ou un groupe au groupe SharePoint  <br/> |AddedToGroup  <br/> |Utilisateur ajouté un membre ou un invité à un groupe SharePoint. Cela a peut-être été une action intentionnelle ou le résultat d’une autre activité, par exemple un événement de partage.  <br/> |
|Autorisé l’utilisateur à créer des groupes  <br/> |AllowGroupCreationSet  <br/> |Administrateur de site ou propriétaire ajoute un niveau d’autorisation à un site qui permet à un utilisateur affecté à cette autorisation pour créer un groupe de ce site.  <br/> |
|Site annulé geo déplacer  <br/> |SiteGeoMoveCancelled  <br/> |Un administrateur global ou SharePoint avec succès annule SharePoint ou déplacer OneDrive site géographique. La fonctionnalité Multi-Geo permet à une organisation Office 365 englober plusieurs régions de centre de données Office 365, qui sont appelées zones géographiques. Pour plus d’informations, voir [Fonctionnalités Multi-localisés dans OneDrive et SharePoint Online dans Office 365](https://go.microsoft.com/fwlink/?linkid=860840).<br/> |
|Modification d’une stratégie de partage  <br/> |SharingPolicyChanged  <br/> |Un administrateur global ou SharePoint modifié SharePoint stratégie de partage à l’aide du portail d’administration d’Office 365, portail d’administration de SharePoint ou SharePoint Online Management Shell. Toute modification apportée aux paramètres de la stratégie de partage de votre organisation est enregistrée. La stratégie qui a été modifiée est identifiée dans le champ **ModifiedProperties** dans les propriétés détaillées de l’enregistrement de l’événement.<br/> |
|Modifié la stratégie d’accès de périphérique  <br/> |DeviceAccessPolicyChanged  <br/> |Un SharePoint ou un administrateur global modifié la stratégie de périphériques non gérés pour votre organisation. Cette stratégie contrôle l’accès à SharePoint, OneDrive et Office 365 à partir des périphériques qui ne sont pas joints à votre organisation. La configuration de cette stratégie nécessite une mobilité d’entreprise + l’abonnement de sécurité. Pour plus d’informations, consultez [contrôler l’accès à partir des périphériques non gérés](https://support.office.com/article/5ae550c4-bd20-4257-847b-5c20fb053622).<br/> |
|Modification des agents utilisateurs exemptés  <br/> |CustomizeExemptUsers  <br/> |Un administrateur global ou SharePoint personnalisés à la liste des agents utilisateurs exemptés dans le centre d’administration de SharePoint. Vous pouvez spécifier les agents utilisateurs exemptés de recevoir une page web entière à l’index. Cela signifie lorsqu’un agent utilisateur que vous avez spécifiés en tant qu’identifiant rencontre un formulaire InfoPath, le formulaire est renvoyé comme un fichier XML, au lieu d’une page web entière. Cela accélère l’indexation des formulaires InfoPath.  <br/> |
|Modifié la stratégie d’accès réseau  <br/> |NetworkAccessPolicyChanged  <br/> |Un SharePoint ou un administrateur global modifié la stratégie d’accès basé sur l’emplacement (également appelée une limite réseau approuvé) dans le centre d’administration de SharePoint ou à l’aide de SharePoint Online PowerShell. Ce type de contrôle de stratégie qui peut accéder aux ressources SharePoint et OneDrive dans votre organisation basée sur les plages d’adresses IP autorisées que vous spécifiez. Pour plus d’informations, consultez [contrôler l’accès à SharePoint Online et données OneDrive basées sur l’emplacement réseau](https://support.office.com/article/b5a5f1f1-1174-4c6b-91d0-9273a6b6971f).<br/> |
|Déplacer de site terminés localisés  <br/> |SiteGeoMoveCompleted  <br/> |Un déplacement localisés de site qui a été planifié par un administrateur global dans votre organisation a réussi. La fonctionnalité Multi-Geo permet à une organisation Office 365 englober plusieurs régions de centre de données Office 365, qui sont appelées zones géographiques. Pour plus d’informations, voir [Fonctionnalités Multi-localisés dans OneDrive et SharePoint Online dans Office 365](https://go.microsoft.com/fwlink/?linkid=860840).<br/> |
|Groupe créé  <br/> |GroupAdded  <br/> |Administrateur de site ou propriétaire crée un groupe pour un site ou effectue une tâche qui se traduit un groupe en cours de création. Par exemple, la première fois un utilisateur crée un lien pour partager un fichier, un groupe système est ajouté à OneDrive l’utilisateur pour le site de l’entreprise. Cet événement peut également être un utilisateur qui crée une liaison avec résultat modifier les autorisations à un fichier partagé.  <br/> |
|Connexion créée envoyés à  <br/> |SendToConnectionAdded  <br/> |Un administrateur global ou SharePoint crée une connexion à envoyer dans la page de gestion des enregistrements dans le centre d’administration de SharePoint. Une connexion d’envoi spécifie les paramètres pour un référentiel de documents ou un centre des enregistrements. Lorsque vous créez une connexion envoyer vers, un organisateur de contenu peuvent envoyer des documents à l’emplacement spécifié.  <br/> |
|Collection de sites créée  <br/> |SiteCollectionCreated  <br/> |Un administrateur global ou SharePoint crée une nouvelle collection de sites dans votre organisation SharePoint Online ou un utilisateur a déployé leur OneDrive pour le site de l’entreprise.  <br/> |
|Groupe supprimé  <br/> |GroupRemoved  <br/> |Utilisateur supprime un groupe d’un site.  <br/> |
|Envoyé à connexion supprimée  <br/> |SendToConnectionRemoved  <br/> |Un administrateur global ou SharePoint supprime une connexion à envoyer dans la page de gestion des enregistrements dans le centre d’administration de SharePoint.  <br/> |
|Site supprimé  <br/> |SiteDeleted  <br/> |Administrateur de site supprime un site.  <br/> |
|Extension d’aperçu des documents  <br/> |PreviewModeEnabledSet  <br/> |Administrateur du site permet d’aperçu de documents à un site.  <br/> |
|Flux de travail activé hérité  <br/> |LegacyWorkflowEnabledSet  <br/> |L’administrateur de site ou le propriétaire ajoute le type de contenu Tâche de flux de travail SharePoint 2013 au site. Les administrateurs globaux peuvent également activer des flux de travail pour l’organisation entière dans le Centre d’administration SharePoint.  <br/> |
|Office activé à la demande  <br/> |OfficeOnDemandSet  <br/> |Administrateur du site permet à Office à la demande, ce qui permet aux utilisateurs d’accéder à la version la plus récente des applications bureautiques Office. Office à la demande est activée dans le centre d’administration SharePoint et requiert un abonnement à Office 365 qui inclut complètes, toutes les applications Office.  <br/> |
|Flux RSS activés  <br/> |NewsFeedEnabledSet  <br/> |Administrateur de site ou propriétaire permet de flux RSS pour un site. Les administrateurs globaux peuvent activer les flux RSS pour toute l’organisation dans le centre d’administration de SharePoint.  <br/> |
|Demande d’accès modifiés définition  <br/> |WebRequestAccessModified  <br/> |Les paramètres de demande d’accès ont été modifiés sur un site.  <br/> |
|Paramètre de membres peuvent partager modifié  <br/> |WebMembersCanShareModified  <br/> |Le **Membres peuvent partager** un paramètre a été modifié sur un site.  <br/> |
|Autorisations de site modifié  <br/> |SitePermissionsModified  <br/> |Administrateur de site ou propriétaire (ou compte système) modifie le niveau d’autorisation qui sont assignés à un groupe sur un site. Cette activité est également connectée si toutes les autorisations sont supprimées d’un groupe.<br/> > [!NOTE]> Cette opération a été désapprouvée dans SharePoint Online. Pour rechercher les événements associés, vous pouvez rechercher pour d’autres activités liées aux autorisations, comme **administrateur de collection de sites Ajout**, **Ajout d’utilisateur ou un groupe SharePoint groupe**, **utilisateur autorisé à créer des groupes**, **groupe créé**et **Deleted groupe.**         |
|Supprimé utilisateur ou du groupe SharePoint groupe  <br/> |RemovedFromGroup  <br/> |Utilisateur supprimé un invité ou un membre d’un groupe SharePoint. Cela a peut-être été une action intentionnelle ou le résultat d’une autre activité, comme un événement d’annulation du partage.  <br/> |
|Site renommée  <br/> |SiteRenamed  <br/> |Administrateur de site ou propriétaire renomme un site  <br/> |
|Autorisations d’administrateur de site demandé  <br/> |SiteAdminChangeRequest  <br/> |Demandes de l’utilisateur à ajouter comme administrateur de collection de sites pour une collection de sites. Administrateurs de collection de sites ont des autorisations Contrôle total pour la collection de sites et tous ses sous-sites.  <br/> |
|Déplacer de site planifiée localisés  <br/> |SiteGeoMoveScheduled  <br/> |Un administrateur global ou SharePoint avec succès planifie SharePoint ou déplacer OneDrive site géographique. La fonctionnalité Multi-Geo permet à une organisation Office 365 englober plusieurs régions de centre de données Office 365, qui sont appelées zones géographiques. Pour plus d’informations, voir [Fonctionnalités Multi-localisés dans OneDrive et SharePoint Online dans Office 365](https://go.microsoft.com/fwlink/?linkid=860840).<br/> |
|Site hôte de jeu  <br/> |HostSiteSet  <br/> |Un administrateur global ou SharePoint modifie le site désigné pour héberger personnel ou OneDrive pour les sites.  <br/> |
|Groupe mis à jour  <br/> |GroupUpdated  <br/> |Administrateur de site ou propriétaire modifie les paramètres d’un groupe pour un site. Cela peut inclure la modification du nom du groupe, qui peut afficher ou modifier l’appartenance au groupe et la gestion des demandes d’appartenance.  <br/> |
  
### <a name="exchange-mailbox-activities"></a>Activités de boîte aux lettres Exchange
  
Le tableau suivant répertorie les activités qui peuvent être enregistrées par boîte aux lettres de journal d’audit. Activités de boîte aux lettres effectuées par le propriétaire de la boîte aux lettres, un utilisateur délégué ou un administrateur sont enregistrées. Par défaut, l’audit de boîte aux lettres dans Office 365 n’est pas activé. Audit de boîte aux lettres la journalisation doit être activée pour chaque boîte aux lettres avant d’activité de la boîte aux lettres sera considérée. Pour plus d’informations, voir [Activer la boîte aux lettres de l’audit dans Office 365](https://go.microsoft.com/fwlink/p/?LinkID=626109).
  
|**Nom convivial**|**Operation**|**Description**|
|:-----|:-----|:-----|
|Ajout de déléguer des autorisations de boîte aux lettres  <br/> |Ajouter-MailboxPermission  <br/> |Un administrateur a attribué l’autorisation de boîte aux lettres FullAccess à un utilisateur (appelé délégué) boîte aux lettres d’une autre personne. L’autorisation FullAccess permet au délégué d’ouvrir la boîte aux lettres de l’autre personne et de lire et de gérer le contenu de la boîte aux lettres.  <br/> |
|Messages copiés dans un autre dossier  <br/> |Copy  <br/> |Un message a été copié dans un autre dossier.  <br/> |
|Élément de boîte aux lettres créée  <br/> |Create  <br/> |Un élément est créé dans le dossier calendrier, Contacts, Notes ou les tâches dans la boîte aux lettres ; par exemple, une demande de réunion est créée. Notez que la création, l’envoi ou la réception d’un message n’est pas audités. En outre, la création d’un dossier de boîte aux lettres n’est pas analysé.  <br/> |
|Messages supprimés du dossier éléments supprimés  <br/> |SoftDelete  <br/> |Un message a été définitivement supprimé ou supprimé du dossier éléments supprimés. Ces éléments sont déplacés vers le dossier éléments récupérables. Les messages sont également placés dans le dossier éléments récupérables lorsqu’un utilisateur sélectionne et appuie sur **MAJ + SUPPR**.<br/> |
|Déplacer des messages vers un autre dossier  <br/> |Move  <br/> |Un message a été déplacé vers un autre dossier.  <br/> |
|Déplacer des messages vers le dossier éléments supprimés  <br/> |MoveToDeletedItems  <br/> |Un message a été supprimé et déplacé vers le dossier Éléments supprimés.  <br/> |
|Autorisation de dossier modifié  <br/> |UpdateFolderPermissions  <br/> |Une autorisation de dossier a été modifiée. Contrôle des autorisations du dossier les utilisateurs de votre organisation peuvent accéder aux dossiers de boîte aux lettres et les messages dans le dossier.  <br/> |
|Messages purgés à partir de la boîte aux lettres  <br/> |HardDelete  <br/> |Un message a été purgé à partir du dossier éléments récupérables (définitivement supprimé de la boîte aux lettres).  <br/> |
|Autorisations de boîte aux lettres de délégué supprimé  <br/> |Remove-MailboxPermission  <br/> |Un administrateur a supprimé l’autorisation FullAccess (qui a été assignée à un délégué) à partir de la boîte aux lettres d’une personne. Une fois que l’autorisation FullAccess est supprimée, le délégué ne peut pas ouvrir les boîtes aux lettres de l’autre personne ou accéder au contenu de celui-ci.  <br/> |
|Envoyé le message à l’aide des autorisations Envoyer en tant que  <br/> |SendAs  <br/> |Un message a été envoyé à l’aide de l’autorisation SendAs. Cela signifie qu’un autre utilisateur a envoyé le message comme s’il provenait du propriétaire de la boîte aux lettres.  <br/> |
|Envoyé à l’aide des autorisations Envoyer de la part de message  <br/> |SendOnBehalf  <br/> |Un message a été envoyé à l’aide de l’autorisation SendOnBehalf. Cela signifie qu’un autre utilisateur a envoyé le message de la part du propriétaire de la boîte aux lettres. Le message indique au destinataire de la part de qui le message a été envoyé et qui a envoyé réellement le message.  <br/> |
|Accès délégué mis à jour au dossier calendrier  <br/> |UpdateCalendarDelegation  <br/> |Une délégation de calendrier a été affectée à une boîte aux lettres. La délégation de calendrier donne à quelqu'un d’autre dans les mêmes autorisations d’organisation pour gérer le calendrier du propriétaire de la boîte aux lettres.  <br/> |
|Message mis à jour  <br/> |Update  <br/> |Un message ou ses propriétés ont été modifiés.  <br/> |
|Utilisateur connecté à la boîte aux lettres  <br/> |MailboxLogin  <br/> |L'utilisateur s'est connecté à sa boîte aux lettres.  <br/> |
|(aucun)  <br/> |UpdateInboxRules  <br/> |Une règle de boîte de réception a été ajoutée, supprimée ou modifiée. Règles de boîte de réception sont utilisés pour traiter les messages dans la boîte de réception en fonction de conditions spécifiées et prennent les mesures lorsque les conditions d’une règle sont remplies, telles que le déplacement d’un message dans un dossier spécifié ou suppression d’un message.<br/> Pour renvoyer les entrées pour les activités de règle de boîte de réception, vous devez sélectionner **Afficher les résultats pour toutes les activités** dans la liste des **activités** . Utilisez les zones plage de dates et la liste des **utilisateurs** pour affiner les résultats de recherche.<br/> |
  
### <a name="sway-activities"></a>Balancement des activités
  
Le tableau suivant répertorie les activités des utilisateurs et d’administration de balancement. Balancement est une application Office 365 qui permet aux utilisateurs de collecter, mettre en forme et partager des idées, articles et des présentations sur une zone de dessin interactive, basée sur le web. Pour plus d’informations, voir le [Forum aux questions sur balancement - aide d’administration](https://support.office.com/article/446380fa-25bf-47b2-996c-e12cb2f9d075).
  
|**Nom convivial**|**Operation**|**Description**|
|:-----|:-----|:-----|
|Niveau de partage balancement modifié  <br/> |SwayChangeShareLevel  <br/> |Utilisateur modifie le niveau de partage d’un balancement. Cet événement capture de l’utilisateur de modifier l’étendue du partage associé à un balancement ; par exemple, public par rapport à l’intérieur de l’organisation.  <br/> |
|Balancement créée  <br/> |SwayCreate  <br/> |L’utilisateur crée un balancement.  <br/> |
|Balancement supprimée  <br/> |SwayDelete  <br/> |Utilisateur supprime un balancement.  <br/> |
|Duplication de balancement désactivée  <br/> |SwayDisableDuplication  <br/> |Utilisateur désactive la duplication d’un balancement.  <br/> |
|Balancement dupliqué  <br/> |SwayDuplicate  <br/> |Utilisateur un balancement les doublons.  <br/> |
|Balancement modifiée  <br/> |SwayEdit  <br/> |L’utilisateur modifie un balancement.  <br/> |
|Duplication de balancement activée  <br/> |EnableDuplication  <br/> |Utilisateur permet la duplication d’un balancement ; la possibilité pour un utilisateur d’activer la duplication d’un balancement est activée par défaut.  <br/> |
|Partage de balancement révoquées  <br/> |SwayRevokeShare  <br/> |Utilisateur arrête le partage un balancement par l’annulation de l’accès à celui-ci. Annulation de l’accès modifie les liens associés à un balancement.  <br/> |
|Balancement partagé  <br/> |SwayShare  <br/> |Utilisateur a l’intention de partager un balancement. Cet événement capture l’action de l’utilisateur de cliquer sur une destination spécifiques de partage dans le menu partager de balancement. L’événement n’indique pas si l’utilisateur s’est terminé l’action de partage.  <br/> |
|Désactivé le partage externe de balancement  <br/> |SwayExternalSharingOff  <br/> |Administrateur désactive balancement partage externe pour toute l’organisation à l’aide du centre d’administration Office 365.  <br/> |
|Partage externe de balancement activée  <br/> |SwayExternalSharingOn  <br/> |Administrateur Active balancement partage externe pour toute l’organisation à l’aide du centre d’administration Office 365.  <br/> |
|Désactivé le service balancement  <br/> |SwayServiceOff  <br/> |Administrateur désactive balancement pour toute l’organisation à l’aide du centre d’administration Office 365.  <br/> |
|Service balancement activée  <br/> |SwayServiceOn  <br/> |Administrateur Active balancement pour toute l’organisation en utilisant le centre d’administration Office 365 (balancement service est activé par défaut).  <br/> |
|Balancement affichée  <br/> |SwayView  <br/> |Utilisateur visualise un balancement.  <br/> |

  
### <a name="user-administration-activities"></a>Activités de l’administration des utilisateurs
  
Le tableau suivant répertorie les activités de l’administration utilisateur enregistrés lorsqu’un administrateur ajoute ou modifie un compte d’utilisateur à l’aide du centre d’administration Office 365 ou le portail de gestion Azure.
  
|**Activité**|**Operation**|**Description**|
|:-----|:-----|:-----|
|Ajout d’utilisateur  <br/> |Ajouter un utilisateur  <br/> |Un compte d’utilisateur Office 365 a été créé.  <br/> |
|Licence utilisateur modifié  <br/> |Licence utilisateur de modification  <br/> |La licence est attribuée à un utilisateur, ce qui a changé. Pour voir quelles licences ont été modifications, voir l’activité de **mise à jour utilisateur** correspondante.<br/> |
|Mot de passe utilisateur modifié  <br/> |Modification mot de passe utilisateur  <br/> |Administrateur a modifié le mot de passe le mot de passe pour un utilisateur.  <br/> |
|Utilisateur supprimé  <br/> |Supprimer l’utilisateur  <br/> |Un compte d’utilisateur Office 365 a été supprimé.  <br/> |
|Réinitialiser le mot de passe utilisateur  <br/> |Réinitialiser le mot de passe utilisateur  <br/> |Administrateur de réinitialiser le mot de passe pour un utilisateur.  <br/> |
|Définir la propriété qui oblige l’utilisateur à modifier le mot de passe  <br/> |Jeu de force modification utilisateur mot de passe  <br/> |Administrateur de définie la propriété qui oblige un utilisateur à modifier leur mot de passe la prochaine fois que la connexion utilisateur vers Office 365.  <br/> |
|Définition des propriétés de licence  <br/> |Définition des propriétés de licence  <br/> |Administrateur modifie les propriétés d’une licence attribuée à un utilisateur.  <br/> |
|Utilisateur mis à jour  <br/> |Utilisateur de la mise à jour  <br/> |Administrateur modifie une ou plusieurs propriétés d’un compte d’utilisateur. Pour obtenir la liste des propriétés utilisateur pouvant être mis à jour, consultez la section « Mise à jour des attributs utilisateur » dans les [Événements du rapport d’Audit Azure Active Directory](https://go.microsoft.com/fwlink/p/?LinkID=616549).<br/> |
  
### <a name="azure-ad-group-administration-activities"></a>Activités de l’administration du groupe AD Azure
  
Le tableau suivant répertorie les activités de l’administration de groupe qui sont enregistrées lorsqu’un administrateur ou un utilisateur crée ou modifie un groupe d’Office 365 ou lorsqu’un administrateur crée un groupe de sécurité à l’aide du centre d’administration Office 365 ou le portail de gestion Azure. Pour plus d’informations sur les groupes dans Office 365, voir [Afficher, créer et supprimer des groupes dans le centre d’administration d’Office 365](https://support.office.com/article/a6360120-2fc4-46af-b105-6a04dc5461c7).
  
|**Nom convivial**|**Operation**|**Description**|
|:-----|:-----|:-----|
|Ajout de groupe  <br/> |Ajouter un groupe  <br/> |Un groupe a été créé.  <br/> |
|Ajout de membres au groupe  <br/> |Ajouter un membre au groupe  <br/> |Un membre a été ajouté à un groupe.  <br/> |
|Groupe supprimé  <br/> |Supprimer le groupe  <br/> |Un groupe a été supprimé.  <br/> |
|Supprimé le membre du groupe  <br/> |Supprimer des membres du groupe  <br/> |Un membre a été supprimé d’un groupe.  <br/> |
|Groupe mis à jour  <br/> |Groupe de mise à jour  <br/> |Une propriété d’un groupe a été modifiée.  <br/> |
   
### <a name="application-administration-activities"></a>Activités de l’administration d’applications
  
Le tableau suivant répertorie les activités d’administration d’applications qui sont enregistrées lorsqu’un administrateur ajoute ou modifie une application qui est enregistrée dans Azure AD. N’importe quelle application qui s’appuie sur Azure AD pour l’authentification doit être enregistrée dans le répertoire.
  
|**Nom convivial**|**Operation**|**Description**|
|:-----|:-----|:-----|
|Entrée de délégation Ajout  <br/> |Ajoutez l’entrée de délégation  <br/> |Une autorisation d’authentification a été créé/accordées à une application dans Azure AD.  <br/> |
|Principaux de service supplémentaire  <br/> |Ajouter des principaux de service  <br/> |Une application a été enregistrée dans Azure AD. Une application est représentée par un principal de service dans le répertoire.  <br/> |
|Informations d’identification ajoutées à une entité de service  <br/> |Ajouter des informations d’identification principal de service  <br/> |Informations d’identification ont été ajoutées à un service principal dans Azure AD. Un principe service représente une application dans le répertoire.  <br/> |
|Entrée de délégation supprimées  <br/> |Supprimer l’entrée de délégation  <br/> |Une autorisation d’authentification a été supprimée d’une application dans Azure AD.  <br/> |
|Supprimer un principal de service à partir du répertoire  <br/> |Supprimer les principaux de service  <br/> |Une application a été supprimée / n’est pas inscrite dans Azure AD. Une application est représentée par un principal de service dans le répertoire.  <br/> |
|Informations d’identification supprimées à partir d’un service principal  <br/> |Supprimer les informations d’identification principal de service  <br/> |Informations d’identification ont été supprimées à partir d’un service principal dans Azure AD. Un principe service représente une application dans le répertoire.  <br/> |
|Entrée de délégation Set  <br/> |Entrée de délégation Set  <br/> |Une autorisation d’authentification a été mis à jour pour une application dans Azure AD.  <br/> |

### <a name="role-administration-activities"></a>Activités de l’administration des rôles
  
Le tableau suivant répertorie les activités de l’administration de rôle Azure AD qui sont enregistrées lorsqu’un administrateur gère les rôles d’administrateur dans le centre d’administration Office 365 ou dans le portail de gestion Azure.
  
|**Nom convivial**|**Operation**|**Description**|
|:-----|:-----|:-----|
|Ajouter des membres au rôle  <br/> |Ajouter un membre de rôle au rôle  <br/> |Ajouter un utilisateur à un rôle d’administrateur dans Office 365.  <br/> |
|Supprimer un utilisateur d’un rôle de répertoire  <br/> |Supprimer des membres du rôle de rôle  <br/> |Supprimer un utilisateur à un rôle d’administration dans Office 365.  <br/> |
|Définir les informations de contact d’entreprise  <br/> |Définir les informations de contact d’entreprise  <br/> |Mise à jour les préférences de contacts de votre organisation Office 365 au niveau de la société. Cela inclut les adresses de messagerie pour la messagerie associés aux abonnements envoyés par Office 365, ainsi que des notifications techniques sur les services Office 365.  <br/> |
   
### <a name="directory-administration-activities"></a>Opérations de l’administration d’annuaire
  
Le tableau suivant répertorie Azure AD directory et le domaine des activités qui sont enregistrées lorsqu’un administrateur gère leur organisation Office 365 dans le centre d’administration Office 365 ou dans le portail de gestion Azure liées.
  
|**Nom convivial**|**Operation**|**Description**|
|:-----|:-----|:-----|
|Domaine ajouté à la société  <br/> |Ajouter un domaine à la société  <br/> |Ajout d’un domaine à votre organisation Office 365.  <br/> |
|Ajout d’un partenaire dans le répertoire  <br/> |Ajouter un partenaire de société  <br/> |Ajout d’un partenaire (administrateur délégué) à votre organisation Office 365.  <br/> |
|Domaine supprimé de la société  <br/> |Supprimer le domaine de la société  <br/> |Supprimer un domaine de votre organisation Office 365.  <br/> |
|Supprimer un partenaire à partir du répertoire  <br/> |Supprimer un partenaire de la société  <br/> |Supprimer un partenaire (administrateur délégué) à partir de votre organisation Office 365.  <br/> |
|Obtenir des informations société  <br/> |Obtenir des informations société  <br/> |Mise à jour les informations de société pour votre organisation Office 365. Cela inclut les adresses de messagerie pour la messagerie associés aux abonnements envoyés par Office 365, ainsi que des notifications techniques sur les services Office 365.  <br/> |
|Définir l’authentification de domaine  <br/> |Définir l’authentification de domaine  <br/> |Modification du paramètre d’authentification de domaine de votre organisation Office 365.  <br/> |
|Mise à jour les paramètres de fédération pour un domaine  <br/> |Définir les paramètres de fédération de domaine  <br/> |Modifier les paramètres de fédération (partage externe) pour votre organisation Office 365.  <br/> |
|Définir la stratégie de mot de passe  <br/> |Définir la stratégie de mot de passe  <br/> |Modifier les contraintes de longueur et de caractères pour les mots de passe utilisateur dans votre organisation Office 365.  <br/> |
|Activé la synchronisation Azure AD  <br/> |Définir l’indicateur DirSyncEnabled société  <br/> |Définissez la propriété qui permet à un répertoire pour la synchronisation Azure AD.  <br/> |
|Domaine mis à jour  <br/> |Domaine de mise à jour  <br/> |Mise à jour les paramètres d’un domaine dans votre organisation Office 365.  <br/> |
|Domaine vérifié  <br/> |Vérifier le domaine  <br/> |Vérifiez que votre organisation est le propriétaire d’un domaine.  <br/> |
|Domaine vérifié messagerie vérifié  <br/> |Vérifier le domaine vérifié de messagerie  <br/> |Vérification de messagerie permet de vérifier que votre organisation est le propriétaire d’un domaine.  <br/> |
   
### <a name="ediscovery-activities"></a>activités de découverte électronique
  
Activités de découverte électronique qui sont effectuées lors de la sécurité Office 365 et recherche de contenu &amp; centre de conformité ou en exécutant Windows PowerShell correspondant applets de commande sont consignés dans le journal d’audit de Office 365. Cela inclut les activités suivantes :
  
- Créer et gérer des affaires eDiscovery
    
- Création, de démarrage et de modification des recherches de contenu
    
- Effectuer les opérations de recherche de contenu, tels que l’aperçu, des résultats de recherche, suppression et exportation
    
- Configuration des autorisations de filtrage pour la recherche de contenu
    
- La gestion du rôle d’administrateur de découverte électronique
    
Pour une liste et une description détaillée des activités de découverte électronique qui sont enregistrés, voir [recherche d’activités de découverte électronique dans Office 365 journal d’audit](search-for-ediscovery-activities-in-the-audit-log.md).
  
> [!NOTE]
> Elle accepte jusqu'à 30 minutes pour les événements qui résultent des activités énumérées aux **activités de découverte électronique** dans la liste déroulante **activités** à afficher dans les résultats de recherche. Inversement, nécessaire dans les 24 heures pour les événements correspondants à partir de la découverte électronique activités d’applet de commande apparaissent dans les résultats de recherche. 
  
### <a name="power-bi-activities"></a>Activités de Power BI
  
Le tableau suivant répertorie l’utilisateur et les activités d’administration dans Power BI qui sont enregistrées dans le journal d’audit Office 365.
  
 **Important :** Enregistrement d’audit pour Power BI n’est pas activée par défaut. Pour rechercher des activités de Power BI dans le journal d’audit de theOffice 365, vous devez activer l’audit dans le portail d’administration Power BI. Pour plus d’informations, voir [L’audit Power BI](https://docs.microsoft.com/power-bi/service-admin-auditing#enabling-auditing-functionality-in-the-power-bi-admin-portal).
  
|**Nom convivial**|**Operation**|**Description**|
|:-----|:-----|:-----|
|Membres du groupe ajoutés Power BI  <br/> |AddGroupMembers  <br/> |Un membre est ajouté à un espace de travail de groupe Power BI.  <br/> |
|Jeu de données analysée Power BI  <br/> |AnalyzedByExternalApplication  <br/> |Un ensemble de données est analysé par une application externe.  <br/> |
|Tableau de bord créé Power BI  <br/> |CreateDashboard  <br/> |Un tableau de bord est créé.  <br/> |
|Groupe Power BI  <br/> |CreateGroup  <br/> |Un groupe est créé.  <br/> |
|Création d’organisation pack contenu Power BI  <br/> |CreateOrgApp  <br/> |Un module d’organisation de contenu est créé.  <br/> |
|Tableau de bord supprimé Power BI  <br/> |DeleteDashboard  <br/> |Un tableau de bord est supprimé.  <br/> |
|Jeu de données supprimé Power BI  <br/> |DeleteDataset  <br/> |Un ensemble de données est supprimé.  <br/> |
|Rapport Power BI supprimé  <br/> |DeleteReport  <br/> |Un rapport est supprimé.  <br/> |
|Rapport Power BI téléchargé  <br/> |DownloadReport  <br/> |Un utilisateur télécharge un rapport Power BI depuis le service sur leur ordinateur.  <br/> |
|Tableau de bord modifiée Power BI  <br/> |EditDashboard  <br/> |Un tableau de bord est renommé.  <br/> |
|Données de visual exportées des rapports Power BI  <br/> |ExportReport  <br/> |Données sont exportées depuis une mosaïque de rapport.  <br/> |
|Données de mosaïque exportées Power BI  <br/> |ExportTile  <br/> |Données sont exportées depuis une mosaïque de tableau de bord.  <br/> |
|Tableau de bord imprimé Power BI  <br/> |PrintDashboard  <br/> |Un tableau de bord est imprimée.  <br/> |
|Page de rapport imprimé Power BI  <br/> |PrintReport  <br/> |Un état est imprimé.  <br/> |
|Publication web rapport Power BI  <br/> |PublishToWebReport  <br/> |Un rapport est publié sur le web.  <br/> |
|Tableau de bord de Power BI partagé  <br/> |ShareDashboard  <br/> |Un tableau de bord est partagé.  <br/> |
|Version d’évaluation de prise en main Power BI  <br/> |OptInForProTrial  <br/> |Un utilisateur démarre une inscription d’essai Power BI Pro.  <br/> |
|Paramètres de mise à jour de l’organisation Power BI  <br/> |UpdatedAdminFeatureSwitch  <br/> |Un administrateur modifié un paramètre d’organisation dans le portail d’administration Power BI.  <br/> |
|Tableau de bord affiché Power BI  <br/> |ViewDashboard  <br/> |Un tableau de bord est affiché.  <br/> |
|Visualisé rapport Power BI  <br/> |ViewReport  <br/> |Un rapport est affiché.  <br/> |
  
### <a name="microsoft-teams-activities"></a>Activités Microsoft Teams
  
Le tableau suivant répertorie l’utilisateur et le journal d’audit des activités d’administration dans Microsoft Teams qui sont consignés dans Office 365. Microsoft Teams est un espace de travail centrée conversation dans Office 365. Il affiche les conversations, réunions, fichiers et notes d’une équipe en un seul emplacement. Pour plus d’informations et des liens vers les rubriques d’aide, voir :
  
- [Forum aux questions sur Microsoft Teams - aide d’administration](https://support.office.com/article/05cbe533-2181-4e95-a4b0-52cd7695fafc)
    
- [Aide Microsoft Teams](https://support.office.com/article/23156c0c-2c6e-49dd-8b7b-7c564b76508c)
    
|**Nom convivial**|**Operation**|**Description**|
|:-----|:-----|:-----|
|Ajout de robot à l’équipe  <br/> |BotAddedToTeam  <br/> |Un utilisateur ajoute un robot à une équipe.  <br/> |
|Ajout de canal  <br/> |ChannelAdded  <br/> |Un utilisateur ajoute un canal à une équipe.  <br/> |
|Ajout de connecteur  <br/> |ConnectorAdded  <br/> |Un utilisateur ajoute un connecteur à un canal.  <br/> |
|Ajout de membres à l’équipe  <br/> |MemberAdded  <br/> |Un propriétaire de l’équipe ajoute des membres à une équipe.  <br/> |
|Onglet ajouté  <br/> |TabAdded  <br/> |Un utilisateur ajoute un onglet à un canal.  <br/> |
|Modifié le paramètre de canal  <br/> |ChannelSettingChanged  <br/> | L’opération ChannelSettingChanged est enregistrée lorsque les activités suivantes sont effectuées par un membre d’équipe. Pour chacune de ces activités, une description du paramètre qui a été modifié (indiqué entre parenthèses ci-dessous) s’affiche dans la colonne de **l’élément** dans les résultats de recherche du journal d’audit.<br/> <br/>-Modifie le nom d’un canal d’équipe ( **nom de la chaîne**).  <br/>  <br/>-Modifie la description d’un canal d’équipe ( **description de la chaîne**).  <br/> |
|Modifié le paramètre de l’organisation  <br/> |TeamsTenantSettingChanged  <br/> | L’opération TeamsTenantSettingChanged est enregistrée lorsque les activités suivantes sont effectuées par un administrateur global (à l’aide du centre d’administration Office 365) ; Notez que ces activités affectent les paramètres Microsoft Teams à l’échelle de l’organisation. Pour plus d’informations, voir [les paramètres administrateur pour les équipes Microsoft](https://support.office.com/article/3966a3f5-7e0f-4ea9-a402-41888f455ba2).<br/>  Pour chacune de ces activités, une description du paramètre qui a été modifié (indiqué entre parenthèses ci-dessous) s’affiche dans la colonne de **l’élément** dans les résultats de recherche du journal d’audit.  <br/><br/>-Active ou désactive Teams Microsoft pour l’organisation ( **Les équipes Microsoft**).  <br/><br/>-Active ou désactive l’interopérabilité entre Microsoft Teams et Skype pour les professionnels de l’organisation ( **Skype pour l’interopérabilité de l’entreprise**).<br/><br/>-Active ou désactive l’affichage de l’organigramme dans les clients Microsoft Teams ( **affichage graphique de l’organisation**).  <br/><br/>-Active ou désactive la possibilité pour les membres de l’équipe organiser des réunions privées ( **planification de la réunion privée**).  <br/><br/>-Active ou désactive la possibilité pour les membres de l’équipe organiser des réunions de canal ( **Channel planifier des réunions**).  <br/><br/>-Active ou désactive l’appel vidéo dans des équipes de réunions ( **vidéo pour les réunions Skype**).  <br/><br/>-Active ou désactive le partage dans Microsoft Teams meetups pour l’organisation ( **partage d’écran pour les réunions Skype**) de l’écran.  <br/><br/>-Active ou désactive cette possibilité d’ajouter des images animées (appelés Giphys) à des conversations équipes ( **images animés**).  <br/><br/>-Modifier le paramètre pour l’organisation ( **évaluation du contenu**) de classification de contenu. L’évaluation du contenu restreint les types d’image animée qui peut être affiché dans les conversations.<br/><br/>-Active ou désactive la possibilité pour les membres de l’équipe ajouter des images personnalisables (appelés memes personnalisé) à partir d’Internet à des conversations d’équipe ( **images personnalisables à partir d’Internet**).  <br/><br/>-Active ou désactive la possibilité pour les membres de l’équipe ajouter des images modifiables (appelés autocollants) à des conversations d’équipe ( **images modifiables**).<br/><br/>-Active ou désactive la possibilité pour les membres d’équipe utilisent des robots dans Microsoft Teams conversations et les canaux ( **robots de l’échelle de l’organisation**).<br/><br/>-Permet de robots spécifiques pour Microsoft Teams ; Cela n’inclut pas le robot T est bot aide les équipes qui est disponible lorsque des robots sont activés pour l’organisation ( **robots individuels**).  <br/><br/>-Active ou désactive la possibilité pour les membres de l’équipe ajouter des extensions ou des onglets ( **Extensions ou onglets**).  <br/><br/>-Active ou désactive le chargement à côté de propriétaires robots pour Microsoft Teams ( **chargement de côté des robots**).  <br/><br/>-Active ou désactive la possibilité pour les utilisateurs à envoyer des messages électroniques à un canal Teams Microsoft ( **messagerie canal**).  <br/> |
|Rôle modifiée de membres de l’équipe  <br/> |MemberRoleChanged  <br/> |Un propriétaire de l’équipe change le rôle de membres dans une équipe. Les valeurs suivantes indiquent le type de rôle affecté à l’utilisateur.<br/><br/><br/> **1** - indique le rôle de propriétaire.<br/>**2** - indique le rôle de membre. <br/>**3** - indique que le rôle invité. <br/>La propriété Members inclut également le nom de votre organisation et l’adresse de messagerie.  <br/> |
|Modifié le paramètre de l’équipe  <br/> |TeamSettingChanged  <br/> | L’opération TeamSettingChanged est enregistrée lorsque les activités suivantes sont effectuées par un propriétaire de l’équipe. Pour chacune de ces activités, une description du paramètre qui a été modifié (indiqué entre parenthèses ci-dessous) s’affiche dans la colonne de **l’élément** dans les résultats de recherche du journal d’audit.<br/><br/>-Modifie le type d’accès pour une équipe. Les équipes peuvent être défini comme privée ou publique ( **type d’accès équipe**). Lorsqu’une équipe est privée (paramètre par défaut), les utilisateurs peuvent accéder à l’équipe uniquement par l’invitation. Lorsqu’une équipe est publique, il est accessible par tout le monde.<br/><br/>-Modification de la classification des informations d’une équipe ( **classification de l’équipe**).  <br/>  Par exemple, les données de l’équipe peuvent être classées en tant que haute, moyenne entreprise ou faible impact.<br/><br/>-Modifie le nom d’une équipe ( **nom de l’équipe**).  <br/><br/>-Modifie la description de l’équipe ( **description de l’équipe**). <br/><br/>-Les modifications apportées à un des paramètres de l’équipe. Un propriétaire de l’équipe permettre accéder à ces paramètres dans un client d’équipes en cliquant une équipe, cliquez sur **l’équipe de gestion**, puis en cliquant sur l’onglet **paramètres** . Pour ces activités, le nom du paramètre qui a été modifié s’affiche dans la colonne de **l’élément** dans les résultats de recherche du journal d’audit.<br/> |
|Équipe créé  <br/> |TeamCreated  <br/> |Un utilisateur crée une nouvelle équipe.  <br/> |
|Canal supprimé  <br/> |ChannelDeleted  <br/> |Un utilisateur supprime un canal d’une équipe.  <br/> |
|Équipe supprimé  <br/> |TeamDeleted  <br/> |Un propriétaire de l’équipe supprime une équipe.  <br/> |
|ROBOT supprimé de l’équipe  <br/> |BotRemovedFromTeam  <br/> |Un utilisateur supprime un robot d’une équipe.  <br/> |
|Connecteur supprimée  <br/> |ConnectorRemoved  <br/> |Un utilisateur supprime un canal de connecteur.  <br/> |
|Membres supprimés de l’équipe  <br/> |MemberRemoved  <br/> |Un propriétaire de l’équipe supprime des membres d’une équipe.  <br/> |
|Onglet supprimée  <br/> |TabRemoved  <br/> |Un utilisateur supprime un onglet d’un canal.  <br/> |
|Connecteur mis à jour  <br/> |ConnectorUpdated  <br/> |Un utilisateur a modifié un connecteur dans un canal.  <br/> |
|Onglet mis à jour  <br/> |TabUpdated  <br/> |Un utilisateur a modifié un onglet dans un canal.  <br/> |
|Utilisateur connecté à des équipes  <br/> |TeamsSessionStarted  <br/> |Un utilisateur se connecte à un client Microsoft Teams.  <br/> |

### <a name="yammer-activities"></a>Activités de Yammer
  
Le tableau suivant répertorie l’utilisateur et le journal d’audit des activités d’administration dans Yammer et qui sont consignées dans Office 365. Pour renvoyer le journal d’audit des activités liées aux Yammer à partir d’Office 365, vous devez sélectionner **Afficher les résultats pour toutes les activités** dans la liste des **activités** . Utilisez les zones plage de dates et la liste des **utilisateurs** pour affiner les résultats de recherche. 
  
|**Nom convivial**|**Operation**|**Description**|
|:-----|:-----|:-----|
|Stratégie de rétention des données modifiées  <br/> |SoftDeleteSettingsUpdated  <br/> |Admin vérifié met à jour le paramètre de la stratégie de rétention des données de réseau dur supprimez ou logicielle supprimer. Seuls les administrateurs vérifiés peuvent effectuer cette opération.  <br/> |
|Configuration réseau modifiée  <br/> |NetworkConfigurationUpdated  <br/> |Réseau ou un administrateur vérifié modifie la configuration du réseau Yammer. Cela inclut la définition de l’intervalle pour l’exportation des données et l’activation de conversation.  <br/> |
|Paramètres du profil modifié  <br/> |ProcessProfileFields  <br/> |Réseau ou un administrateur vérifié modifie les informations qui s’affiche sur les profils d’utilisateur pour le réseau d’utilisateurs.  <br/> |
|Modification du mode contenu privé  <br/> |SupervisorAdminToggled  <br/> |Admin vérifié Active ou désactive la *Mode de contenu privé* . Ce mode vous permet un affichage admin publie dans les groupes privés et affichage des messages privés entre les utilisateurs individuels (ou groupes d’utilisateurs). Seuls les administrateurs vérifiés peuvent uniquement effectuer cette opération.<br/> |
|Configuration de la sécurité modifié  <br/> |NetworkSecurityConfigurationUpdated  <br/> |Admin vérifié met à jour la configuration de la sécurité du réseau Yammer. Cela inclut la définition des stratégies d’expiration de mot de passe et les restrictions sur les adresses IP. Seuls les administrateurs vérifiés peuvent effectuer cette opération.  <br/> |
|Fichier créé  <br/> |FileCreated  <br/> |Utilisateur télécharge un fichier.  <br/> |
|Groupe créé  <br/> |GroupCreation  <br/> |Utilisateur crée un nouveau groupe.  <br/> |
|Groupe supprimé  <br/> |GroupDeletion  <br/> |Un groupe est supprimé de Yammer.  <br/> |
|Message supprimé  <br/> |MessageDeleted  <br/> |Utilisateur supprime un message.  <br/> |
|Fichier téléchargé  <br/> |FileDownloaded  <br/> |Utilisateur télécharge un fichier.  <br/> |
|Données exportées  <br/> |DonnéesExporter  <br/> |Admin vérifié exporte les données du réseau Yammer. Seuls les administrateurs vérifiés peuvent effectuer cette opération.  <br/> |
|Fichier partagé  <br/> |FileShared  <br/> |Utilisateur partage un fichier avec un autre utilisateur.  <br/> |
|Utilisateur suspendu réseau  <br/> |NetworkUserSuspended  <br/> |Interrompt le réseau ou un administrateur vérifié (désactive) un utilisateur de Yammer.  <br/> |
|Utilisateur suspendu  <br/> |UserSuspension  <br/> |Compte d’utilisateur est suspendu (désactivé).  <br/> |
|Description du fichier mis à jour  <br/> |FileUpdateDescription  <br/> |Utilisateur modifie la description d’un fichier.  <br/> |
|Nom du fichier mis à jour  <br/> |FileUpdateName  <br/> |Utilisateur modifie le nom d’un fichier.  <br/> |
|Fichier visualisé  <br/> |FileVisited  <br/> |Utilisateur visualise un fichier.  <br/> |
   
### <a name="microsoft-stream"></a>Microsoft Stream
  
Vous pouvez rechercher le journal d’audit pour les activités dans Microsoft Stream. Ces activités incluent vidéo activités effectuées par les utilisateurs, les activités de canal de groupe et activités telles que la gestion des utilisateurs, la gestion des paramètres de l’organisation et l’exportation des rapports d’administration. Pour obtenir une description de ces activités, consultez la section « Activités enregistrées dans Microsoft Stream » dans [Les journaux d’Audit dans le flux de Microsoft](https://docs.microsoft.com/stream/audit-logs).
  
### <a name="exchange-admin-audit-log"></a>Journal d’audit de l’administrateur Exchange
  
Enregistrement d’audit administrateur Exchange, qui est activé par défaut dans Office 365 : consigne un événement dans le journal d’audit Office 365 lorsqu’un administrateur (ou un utilisateur qui a été attribué des autorisations d’administration) apporte une modification au sein de votre organisation Exchange Online. Modifications apportées à l’aide du centre d’administration Exchange ou en exécutant une applet de commande de Windows PowerShell sont consignées dans le journal d’audit d’administration Exchange. Pour plus d’informations sur l’administration d’Exchange l’enregistrement d’audit, voir [enregistrement d’audit administrateur](https://go.microsoft.com/fwlink/p/?LinkID=619225).
  
Voici quelques conseils pour la recherche d’activité dans le journal d’audit d’administration Exchange :
  
- Pour renvoyer les entrées dans le journal d’audit d’administration Exchange, vous devez sélectionner **Afficher les résultats pour toutes les activités** dans la liste des **activités** . Utilisez les zones plage de dates et la liste des **utilisateurs** pour affiner les résultats de recherche pour les applets de commande exécutées par un administrateur Exchange spécifique au sein d’une plage de dates spécifique. 
    
- Pour afficher les événements dans le journal d’audit d’administration Exchange, filtrer les résultats de la recherche et le type un **-** (tiret) dans la zone de filtre **d’activité** . Noms d’applet de commande, qui sont affichés dans la colonne **d’activité** pour les événements d’administration Exchange s’affiche. Vous pouvez ensuite trier les noms d’applet de commande dans l’ordre alphabétique. 
    
    ![Tapez un tiret dans la zone activités pour filtrer les événements d’administration Exchange](media/7628e7aa-6263-474a-a28b-2dcf5694bb27.png)
  
- Pour obtenir plus d’informations sur les applets de commande a été exécutée, les paramètres et les valeurs de paramètre ont été utilisés et les objets qui ont été affectées, vous devez exporter les résultats de recherche et sélectionnez l’option **télécharger tous les résultats** . 
    
- Vous pouvez également afficher les événements dans le journal d’audit d’administration Exchange à l’aide du centre d’administration Exchange. Pour obtenir des instructions, consultez la rubrique [Afficher journal d’audit de l’administrateur](https://technet.microsoft.com/library/dn342832%28v=exchg.150%29.aspx).
  
## <a name="frequently-asked-questions"></a>Questions fréquemment posées

**Où puis-je trouver sur les fonctionnalités offertes par le service d’audit dans Office 365 ?**

Pour plus d’informations sur les fonctionnalités d’audit et création de rapports disponibles dans Office 365, voir [l’audit et la création de rapports dans Office 365](office-365-auditing-and-reporting-overview.md). 

**Quels sont les différents Services Office 365 actuellement audités ?**

Services Office 365 plus utilisés comme Exchange Online, SharePoint, OneDrive, Azure Active Directory, Microsoft Teams, CRM, protection contre les menaces avancées et Data Loss Prevention audités. Voir la section [Introduction](#search-the-audit-log-in-the-office-365-security-amp-compliance-center) de cet article pour obtenir la liste complète.

**Quelles activités sont contrôlées par l’audit service dans Office 365 ?**

Consultez la section [activités contrôlé](#audited-activities) dans cet article pour obtenir une liste et une description des activités audités dans Office 365.

**Combien de temps faut-il pour un enregistrement d’audit après un événement s’est produit ?**

La plupart des données d’audit sont disponibles dans les 30 minutes, mais elle peut prendre jusqu'à 24 heures après qu’un événement se produit pour l’entrée du journal d’audit correspondant à afficher dans les résultats de recherche. Consultez le tableau dans la section [avant de commencer](#before-you-begin) de cet article qui indique le temps que nécessaire pour les événements dans les différents services Office 365 soit disponible.

**Combien de temps sont les enregistrements d’audit conservés pour ?**

Enregistrements du journal d’audit sont actuellement conservées pendant 90 jours. Microsoft travaille activement sur un plan pour augmenter la taille limite. 

**Puis-je accéder par programme les données d’audit ?**

Oui. L’API d’activité de gestion Office 365 est utilisé pour extraire les journaux d’audit par programme.  Pour commencer, consultez la rubrique [en route avec l’API de gestion d’Office 365](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).

**Existe-t-il d’autres façons d’obtenir l’audit des journaux qu’exploiteront la Office 365 Security & centre de conformité ou de l’API d’activité de gestion Office 365 ?**

Non. Voici les uniquement deux façons d’obtenir des données à partir du service d’audit Office 365. 

**Dois-je individuellement activer l’audit dans chaque service à capturer des journaux d’audit pour ?**

Dans la plupart des services Office 365, l’audit est activé par défaut après l’activation à l’origine de l’audit pour votre organisation Office 365 (comme décrit dans la section [avant de commencer](#before-you-begin) dans cet article). Toutefois, vous devez activer la boîte aux lettres de l’audit dans Exchange Online pour chaque boîte aux lettres que vous souhaitez auditer.   Nous cherchons sur l’activation de l’audit des boîtes aux lettres par défaut pour toutes les boîtes aux lettres dans une organisation Office 365. Pour plus d’informations, voir « audit de boîte aux lettres Exchange sera activé par défaut » dans le [blog de sécurité de Microsoft, de confidentialité et de conformité](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Exchange-Mailbox-Auditing-will-be-enabled-by-default/ba-p/215171).

**Supprime la prise en charge de service audit Office 365 les doublons d’enregistrements ?**

Non. Le pipeline de service d’audit est quasiment en temps réel et par conséquent ne prennent en charge la déduplication.
 
**Données d’audit Office 365 ne sont transmis dans le monde entier ?**

Non. Nous disposons d’audit des déploiements de pipeline NA (Amérique du Nord), EMEA (Europe, Moyen-Orient et Afrique) et régions APAC (Asie-Pacifique). Toutefois, nous pouvons le débit entre ces régions pour l’équilibrage de charge et uniquement pendant les problèmes live. Lorsque nous effectuer ces activités, les données en transit sont chiffrées.   
 
**Est l’audit des données chiffrées ?**

Données d’audit sont stockée dans des boîtes aux lettres Exchange (données au repos) dans la même région dans lequel le pipeline de l’audit est déployé. Ces données ne sont pas chiffrées. Toutefois, les données en transit sont toujours chiffrées. 












