---
title: Supprimer des éléments dans le dossier éléments récupérables de nuage des boîtes aux lettres en attente - aide d’administration
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: a85e1c87-a48e-4715-bfa9-d5275cde67b0
description: 'Pour les administrateurs : supprimer des éléments dans le dossier des éléments récupérables d’un utilisateur pour une boîte aux lettres Exchange Online, même si cette boîte aux lettres se trouve en conservation légale. Il s’agit d’un moyen efficace pour supprimer les données sont répandues par inadvertance dans Office 365.'
ms.openlocfilehash: e80f5182bc425d71c6219decd48d41cf3dce6bba
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2019
ms.locfileid: "28009640"
---
# <a name="delete-items-in-the-recoverable-items-folder-of-cloud-based-mailboxes-on-hold---admin-help"></a>Supprimer des éléments dans le dossier éléments récupérables de nuage des boîtes aux lettres en attente - aide d’administration

Le dossier éléments récupérables pour une boîte aux lettres Exchange Online existe pour protéger contre les suppressions accidentelles ou malveillantes. Il est également utilisé pour stocker les éléments qui sont conservés et accessibles par les fonctionnalités de conformité d’Office 365, telles que le blocage et eDiscovery recherches. Toutefois, dans certaines situations, organisations peut-être été involontairement conservées dans le dossier éléments récupérables qui ils doivent supprimer des données. Par exemple, un utilisateur peut envoyer sans le savoir ou transférer un message électronique qui contient des informations sensibles ou qui peut avoir des conséquences graves. Même si le message est définitivement supprimé, il peut être conservée indéfiniment car une conservation légale a été placée dans la boîte aux lettres. Ce scénario est appelé débordements de données, car les données a été involontairement répandues dans Office 365. Dans ce cas, vous pouvez supprimer des éléments dans le dossier des éléments récupérables d’un utilisateur pour une boîte aux lettres Exchange Online, même si cette boîte aux lettres est mis en attente avec l’une des fonctionnalités de blocage différents dans Office 365. Ces types de suspensions comprennent contient des litiges, archives permanentes, suspensions eDiscovery et des stratégies de rétention Office 365 créés de sécurité Office 365 &amp; centre de conformité. 
  
 Cet article explique comment supprimer des éléments dans le dossier éléments récupérables pour les boîtes aux lettres en nuage qui sont en attente. Cette procédure implique la désactivation de l’accès à la boîte aux lettres et de désactivation de récupération d’élément unique, désactivation de l’Assistant dossier géré à partir de la boîte aux lettres de traitement, supprimer temporairement la suspension, supprimer des éléments à partir du dossier éléments récupérables et retour puis la boîte aux lettres à sa configuration précédente. Voici le processus : 
  
[Étape 1 : Collecter des informations sur la boîte aux lettres](#step-1-collect-information-about-the-mailbox)

[Étape 2 : Préparation de la boîte aux lettres](#step-2-prepare-the-mailbox)

[Étape 3 : Suppression de toutes les suspensions à partir de la boîte aux lettres](#step-3-remove-all-holds-from-the-mailbox)

[Étape 4 : Supprimer la suspension de délai d’attente de la boîte aux lettres](#step-4-remove-the-delay-hold-from-the-mailbox)

[Étape 5 : Supprimer des éléments dans le dossier éléments récupérables](#step-5-delete-items-in-the-recoverable-items-folder)

[Étape 6 : Rétablir la boîte aux lettres à son état précédent](#step-6-revert-the-mailbox-to-its-previous-state)
  
> [!CAUTION]
> Les procédures décrites dans cet article entraînera données définitivement supprimés (définitivement) à partir d’une boîte aux lettres Exchange Online. Cela signifie que les messages que vous supprimez à partir du dossier éléments récupérables ne peuvent pas être récupérés et ne sont pas disponibles pour la récupération sur demande juridique ou autres à des fins de conformité. Si vous souhaitez supprimer des messages à partir d’une boîte aux lettres qui est mis en attente dans le cadre d’un litige, blocage sur Place, maintenez la touche e-Discovery, ou stratégie de rétention Office 365 créée de sécurité Office 365 &amp; centre de conformité, vérifiez auprès de votre gestion des enregistrements ou le département juridique Services avant la suppression de la suspension. Votre organisation peut avoir une stratégie qui définit si une boîte aux lettres sur blocage ou un incident débordements de données est prioritaire. 
  
## <a name="before-you-begin"></a>Avant de commencer

- Vous devez être affectées à la fois des rôles de gestion suivants dans Exchange Online pour rechercher et supprimer des messages à partir du dossier éléments récupérables à l’étape 5.
    
  - **Recherche de boîte aux lettres** - ce rôle permet pour rechercher les boîtes aux lettres dans votre organisation. Les administrateurs Exchange ne sont pas affectés à ce rôle par défaut. Pour assigner vous-même ce rôle, ajoutez-vous en tant que membre du groupe de rôles de gestion de la découverte dans Exchange Online. 
    
  - **Boîte aux lettres importer exporter** : ce rôle permet à pour supprimer des messages de boîte aux lettres d’un utilisateur. Par défaut, ce rôle n’est pas affecté à un groupe de rôles. Pour supprimer les messages des boîtes aux lettres des utilisateurs, vous pouvez ajouter le rôle de boîte aux lettres importer exporter au groupe de rôles de gestion de l’organisation dans Exchange Online. 
    
- La procédure décrite dans cet article n’est pas pris en charge pour les boîtes aux lettres inactives. C'est-à-dire, car vous ne pouvez pas réappliquer une attente (ou la stratégie de rétention Office 365) à une boîte aux lettres inactive après que l’avoir supprimé. Lorsque vous supprimez une suspension à partir d’une boîte aux lettres inactive, elle est remplacée par une boîte aux lettres supprimée normal et est définitivement supprimé de votre organisation après son traitement par l’Assistant dossier géré.
    
- Vous ne pouvez pas effectuer cette procédure pour une boîte aux lettres qui a été affecté à une stratégie de rétention d’Office 365 verrouillée avec un verrou de conservation. C’est parce qu’un verrou de conservation vous empêche de suppression ou à l’exception de la boîte aux lettres à partir de la stratégie de rétention Office 365 et de désactiver l’Assistant dossier géré sur la boîte aux lettres. Pour plus d’informations sur le verrouillage des stratégies de rétention, voir [verrouillage d’une stratégie de rétention](retention-policies.md#locking-a-retention-policy).
    
- Si une boîte aux lettres n’est pas mis en attente (ou ne possède pas de récupération d’élément unique), vous pouvez simplement supprimer les éléments du dossier éléments récupérables. Pour plus d’informations, voir [Rechercher et supprimer les messages ](https://go.microsoft.com/fwlink/?linkid=852453).
  
## <a name="step-1-collect-information-about-the-mailbox"></a>Étape 1 : Collecter des informations sur la boîte aux lettres

Cette première étape consiste à collecter les propriétés sélectionnées à partir de la boîte aux lettres cible auront une incidence sur cette procédure. Veillez à noter ces paramètres ou de les enregistrer dans un fichier texte, car vous allez modifier certaines de ces propriétés et puis rétablir les valeurs d’origine à l’étape 6, après la suppression d’éléments à partir du dossier éléments récupérables. Voici une liste des propriétés de boîte aux lettres que vous devez recueillir.
  
-  *SingleItemRecoveryEnabled* et *RetainDeletedItemsFor* ; Si nécessaire, vous devez désactiver la récupération unique et augmenter la période de rétention des éléments supprimés à l’étape 3. 
    
-  *LitigationHoldEnabled* et *InPlaceHolds* ; Vous devez identifier toutes les suspensions placées sur la boîte aux lettres afin que vous pouvez les supprimer temporairement à l’étape 3. Voir la section [plus d’informations](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#moreinfo) pour obtenir des conseils sur la façon d’identifier la suspension de type qui peut-être être placée sur une boîte aux lettres. 
    
En outre, vous devez obtenir les paramètres d’accès client de la boîte aux lettres afin que vous pouvez temporairement désactiver afin que le propriétaire (ou autres utilisateurs) ne peut pas accéder à la boîte aux lettres au cours de cette procédure. Enfin, vous pouvez obtenir la taille actuelle et le nombre d’éléments dans le dossier éléments récupérables. Après la suppression d’éléments dans le dossier éléments récupérables à l’étape 5, vous allez utiliser ces informations pour vérifier que les éléments ont été supprimées réellement.
  
1. [Connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=396554). Veillez à utiliser un nom d’utilisateur et le mot de passe pour un compte d’administrateur qui a été affecté les rôles de gestion dans Exchange Online. 
    
2. Exécutez la commande suivante pour obtenir des informations sur la récupération d’élément unique et la période de rétention des éléments supprimés.

    ```
    Get-Mailbox <username> | FL SingleItemRecoveryEnabled,RetainDeletedItemsFor
    ```

   Si la récupération d’élément unique est activée, vous devrez désactiver à l’étape 2. Si la période de rétention des éléments supprimés n’est pas définie pour des 30 derniers jours (la valeur maximale dans Exchange Online), puis vous pouvez augmenter à l’étape 2. 
    
3. Exécutez la commande suivante pour obtenir des paramètres d’accès pour la boîte aux lettres de la boîte aux lettres. 
    
    ```
    Get-CASMailbox <username> | FL EwsEnabled,ActiveSyncEnabled,MAPIEnabled,OWAEnabled,ImapEnabled,PopEnabled
    ```

   Vous allez désactiver toutes ces méthodes d’accès à l’étape 2.
    
4. Exécutez la commande suivante pour obtenir des informations sur les suspensions appliquées à la boîte aux lettres de stratégies de rétention Office 365.
    
    ```
    Get-Mailbox <username> | FL LitigationHoldEnabled,InPlaceHolds
    ```


   > [!TIP]
    > S’il existe trop grand nombre de valeurs dans la propriété *InPlaceHolds* et tous les s’affichent, vous pouvez exécuter la `Get-Mailbox <username> | Select-Object -ExpandProperty InPlaceHolds` commande pour afficher chaque valeur sur une ligne distincte. 
  
5. Exécutez la commande suivante pour obtenir des informations sur les stratégies de rétention d’Office 365 à l’échelle de l’organisation. 

    ```
    Get-OrganizationConfig | FL InPlaceHolds
    ```
   Si votre organisation dispose des stratégies de rétention à l’échelle de l’organisation Office 365, vous devrez exclure la boîte aux lettres de ces stratégies à l’étape 3.

   > [!TIP]
    > S’il existe trop grand nombre de valeurs dans la propriété *InPlaceHolds* et tous les s’affichent, vous pouvez exécuter la `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` commande pour afficher chaque valeur sur une ligne distincte. 
  
6. Exécutez la commande suivante pour obtenir la taille actuelle et le nombre total d’éléments dans des dossiers et les sous-dossiers du dossier éléments récupérables dans la boîte aux lettres principale de l’utilisateur. 

    ```
    Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
    ```

   Si la boîte aux lettres de l’utilisateur archive est activé, exécutez la commande suivante pour obtenir la taille et le nombre total d’éléments dans des dossiers et les sous-dossiers du dossier éléments récupérables dans leur boîte aux lettres d’archive. 

    ```s
    Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems -Archive | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
    ```

   Lorsque vous supprimez des éléments à l’étape 5, vous pouvez choisir de supprimer ou pas supprimer des éléments dans le dossier éléments récupérables de boîte aux lettres de l’utilisateur principal d’archivage. Notez que si l’extension automatique d’archivage est activé pour la boîte aux lettres, les éléments dans une boîte aux lettres d’archive auxiliaire ne sont pas supprimés.
  
## <a name="step-2-prepare-the-mailbox"></a>Étape 2 : Préparation de la boîte aux lettres

Après la collecte et l’enregistrement des informations sur la boîte aux lettres, l’étape suivante consiste à préparer la boîte aux lettres en effectuant les tâches suivantes : 
  
- **Désactiver l’accès client aux boîtes aux lettres** afin que le propriétaire de la boîte aux lettres ne peut pas accéder à leur boîte aux lettres et apportez des modifications aux données de boîte aux lettres au cours de cette procédure. 
    
- **Augmenter la période de rétention des éléments supprimés** de 30 jours (la valeur maximale dans Exchange Online) afin que les éléments ne sont pas supprimés du dossier éléments récupérables avant de les supprimer à l’étape 5. 
    
- **Désactiver la récupération d’élément unique** afin que les articles ne seront pas conservées (pendant la durée de la période de rétention des éléments supprimés) après leur suppression à partir du dossier éléments récupérables à l’étape 5. 
    
- **Désactiver l’Assistant dossier géré** afin qu’elle ne traiter la boîte aux lettres et conserver les éléments supprimés à l’étape 5. 
    
Dans Exchange Online PowerShell, procédez comme suit.
  
1. Exécutez la commande suivante pour désactiver tous les accès au client à la boîte aux lettres. La syntaxe de la commande suppose que toutes les méthodes d’accès client ont été activés dans la boîte aux lettres.

    ```   
    Set-CASMailbox <username> -EwsEnabled $false -ActiveSyncEnabled $false -MAPIEnabled $false -OWAEnabled $false -ImapEnabled $false -PopEnabled $false
    ```
   
   > [!NOTE]
    > Cela peut prendre jusqu'à 60 minutes pour désactiver toutes les méthodes d’accès client pour la boîte aux lettres. Notez que la désactivation de ces méthodes d’accès ne déconnecter le propriétaire de boîte aux lettres qu'ils êtes actuellement connectés. Si le propriétaire n’est pas connecté, puis ils ne pourront accéder à leur boîte aux lettres après que ces méthodes d’accès sont désactivées. 
  
2. Exécutez la commande suivante pour augmenter la période de rétention des éléments supprimés de la valeur maximale de 30 jours. Cela suppose que la valeur actuelle est inférieure à 30 jours. 

    ```
    Set-Mailbox <username> -RetainDeletedItemsFor 30
    ```

3. Exécutez la commande suivante pour désactiver la récupération d’élément unique.
    
    ```
    Set-Mailbox <username> -SingleItemRecoveryEnabled $false
    ```

   > [!NOTE]
    > Cela peut prendre jusqu'à 60 minutes pour désactiver la récupération d’élément unique. Ne pas supprimer des éléments dans le dossier éléments récupérables jusqu'à ce que cette période écoulée. 
  
4. Exécutez la commande suivante pour empêcher l’Assistant dossier géré de traiter la boîte aux lettres. Comme expliqué précédemment, vous pouvez désactiver l’Assistant dossier géré uniquement si une stratégie de rétention d’Office 365 avec un verrou de conservation n’est pas appliquée à la boîte aux lettres. 

    ```
    Set-Mailbox <username> -ElcProcessingDisabled $true
    ```

## <a name="step-3-remove-all-holds-from-the-mailbox"></a>Étape 3 : Suppression de toutes les suspensions à partir de la boîte aux lettres

Avant de pouvoir supprimer des éléments à partir du dossier éléments récupérables de la dernière étape consiste à supprimer toutes les suspensions (que vous avez identifié à l’étape 1) placées sur la boîte aux lettres. Toutes les suspensions doivent être supprimées afin que les éléments ne seront pas conservées après leur suppression à partir du dossier éléments récupérables. Les sections suivantes contiennent des informations sur la suppression de différents types de suspensions sur une boîte aux lettres. Voir la section [plus d’informations](#more-information) pour obtenir des conseils sur la façon d’identifier la suspension de type qui peut-être être placée sur une boîte aux lettres. Pour plus d’informations, voir [Comment faire pour identifier le type de blocage placé dans une boîte aux lettres Exchange Online](identify-a-hold-on-an-exchange-online-mailbox.md).
  
> [!CAUTION]
> Comme indiqué précédemment, vérifiez auprès de votre gestion des enregistrements ou les services juridiques avant la suppression d’une suspension à partir d’une boîte aux lettres. 
  
 ### <a name="litigation-hold"></a>Conservation pour litige
  
Exécutez la commande suivante dans Exchange Online PowerShell pour supprimer un litige à partir de la boîte aux lettres.

```
Set-Mailbox <username> -LitigationHoldEnabled $false
```

   
> [!NOTE]
> Semblable à la désactivation de la récupération d’élément unique et les méthodes d’accès client, il peut prendre jusqu'à 60 minutes pour supprimer le litige. Ne pas supprimer des éléments à partir du dossier éléments récupérables jusqu'à ce que cette période écoulée. 
  
 ### <a name="in-place-hold"></a>Blocage local
  
Exécutez la commande suivante dans Exchange Online PowerShell pour identifier la In-Place Hold qui est placé sur la boîte aux lettres. Utilisez le GUID pour la conservation inaltérable que vous avez identifié à l’étape 1. 

```
Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL Name
```
   
Après avoir identifié la conservation inaltérable, vous pouvez utiliser le centre d’administration Exchange (EAC) ou Exchange Online PowerShell pour supprimer la boîte aux lettres de la suspension. Pour plus d’informations, voir [Create or remove an In-Place Hold](https://go.microsoft.com/fwlink/?linkid=852668).
  
 ### <a name="office-365-retention-policies-applied-to-specific-mailboxes"></a>Office 365 de rétention appliquée à des boîtes aux lettres spécifiques
  
Exécutez la commande suivante [Office 365 sécurité &amp; PowerShell du centre de conformité](https://go.microsoft.com/fwlink/?linkid=627084) pour identifier la stratégie de rétention d’Office 365 est appliquée à la boîte aux lettres. Utilisez le GUID (non compris le `mbx` ou `skp` préfixe) pour la stratégie de rétention que vous avez identifié à l’étape 1. 

```
Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name
```
   
Après avoir identifié la stratégie de rétention, accédez à la **gouvernance de Date** \> page de **rétention** dans la sécurité &amp; centre de conformité, modifiez la stratégie de rétention que vous avez identifié à l’étape précédente et supprimer la boîte aux lettres à partir de la liste des destinataires qui sont inclus dans la stratégie de rétention. 
  
 ### <a name="organization-wide-office-365-retention-policies"></a>Stratégies de rétention de l’organisation Office 365
  
Échelle de l’organisation et les stratégies de rétention à l’échelle Exchange Office 365 sont appliquées à chaque boîte aux lettres dans l’organisation. Ils sont appliqués au niveau de l’organisation (et non le niveau de boîte aux lettres) et sont renvoyées lorsque vous exécutez l’applet de commande **Get-OrganizationConfig** à l’étape 1. Exécutez la commande suivante [sécurité &amp; PowerShell du centre de conformité](https://go.microsoft.com/fwlink/?linkid=627084) pour identifier les stratégies de rétention d’Office 365 à l’échelle de l’organisation. Utilisez le GUID (non compris le `mbx` préfixe) pour les stratégies de rétention de l’organisation que vous avez identifié à l’étape 1. 

```
Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name
```

Après avoir identifié les stratégies de rétention de l’organisation Office 365, accédez à la **gouvernance de Date** \> page de **rétention** dans la sécurité &amp; centre de conformité, modifier chaque stratégie de rétention de l’organisation que vous avez identifié dans la précédente étape, puis ajoutez la boîte aux lettres à la liste des destinataires exclus. Cette opération supprimera boîte aux lettres de l’utilisateur de la stratégie de rétention. 

### <a name="office-365-retention-labels"></a>Étiquettes de rétention d’Office 365

Chaque fois qu’un utilisateur s’applique une étiquette qui est configurée pour conserver le contenu ou conserver et puis supprimer le contenu à un dossier ou un élément dans leur boîte aux lettres, la propriété de la boîte aux lettres *ComplianceTagHoldApplied* est définie sur **True**. Dans ce cas, la boîte aux lettres est considéré comme être mise en attente, comme s’il a été mis en attente pour litige ou affecté à une stratégie de rétention d’Office 365.

Pour afficher la valeur de la propriété *ComplianceTagHoldApplied* , exécutez la commande suivante dans Exchange Online PowerShell :

```
Get-Mailbox <username> |FL ComplianceTagHoldApplied
```

Une fois que vous avez identifié qu’une boîte aux lettres est en attente car une étiquette de rétention est appliquée à un dossier ou un élément, vous pouvez utiliser l’outil de recherche de contenu dans le centre de conformité de & sécurité pour rechercher des éléments étiquetés à l’aide de la condition de recherche ComplianceTag. Pour plus d’informations, consultez la section « Conditions de recherche » dans les [requêtes de mot clé et les conditions de recherche pour la recherche de contenu](keyword-queries-and-search-conditions.md#conditions-for-common-properties).

Pour plus d’informations sur les étiquettes, voir [vue d’ensemble d’Office 365 étiquettes](labels.md).

 ### <a name="ediscovery-case-holds"></a>contient des cas de découverte électronique
  
Exécutez les commandes suivantes [sécurité &amp; PowerShell du centre de conformité](https://go.microsoft.com/fwlink/?linkid=627084) pour identifier la suspension associée à un cas de découverte électronique qui est appliqué à la boîte aux lettres. Utilisez le GUID (non compris le `UniH` préfixe) pour la découverte électronique maintenez que vous avez identifié à l’étape 1. Notez que la deuxième commande affiche le nom du cas eDiscovery que la suspension associée ; la troisième commande affiche le nom de la suspension. 
  
```
$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>
```

```
Get-ComplianceCase $CaseHold.CaseId | FL Name
```

```
$CaseHold.Name
```

Une fois que vous avez identifié le nom de la casse eDiscovery et la suspension, accédez à la **recherche &amp; enquête** \> page de **découverte électronique** dans la sécurité &amp; centre de conformité, ouvrez le cas et supprimer la boîte aux lettres de la suspension. Pour plus d’informations, voir [gérer des affaires eDiscovery de sécurité Office 365 &amp; centre de conformité](manage-ediscovery-cases.md).
  
## <a name="step-4-remove-the-delay-hold-from-the-mailbox"></a>Étape 4 : Supprimer la suspension de délai d’attente de la boîte aux lettres

Une fois que n’importe quel type de suspension est supprimé d’une boîte aux lettres, la valeur de la propriété de la boîte aux lettres *DelayHoldApplied* est définie sur **True**. Cela se produit la prochaine fois que l’Assistant dossier géré traite la boîte aux lettres et détecte qu’une suspension a été supprimée. Cela est appelé un *délai de blocage* et signifie que la suppression effective de la suspension est retardée de 30 jours pour empêcher les données définitivement supprimées de la boîte aux lettres. (L’objectif d’une suspension du délai d’attente est Administrateurs de donner la possibilité permet de rechercher ou de récupérer des éléments de boîte aux lettres qui seront purgés après la suppression d’une suspension.)  Lorsque le délai est suspendu sur la boîte aux lettres, la boîte aux lettres est considérée en attente pour une durée illimitée, en tant que si la boîte aux lettres a été litige. Après 30 jours, la suspension de délai d’attente expire et Office 365 tente automatiquement de supprimer la suspension de délai d’attente (en définissant la propriété *DelayHoldApplied* sur **False**) afin que la suspension est réellement supprimée. 

Avant de pouvoir supprimer des éléments à l’étape 5, vous devez supprimer la suspension de délai d’attente de la boîte aux lettres. Commencez par déterminer si la suspension du délai d’attente est appliquée à la boîte aux lettres en exécutant la commande suivante dans Exchange Online PowerShell :

```
Get-Mailbox <username> | FL DelayHoldApplied
```

Si la valeur de la propriété *DelayHoldApplied* est définie sur **False**, une suspension du délai d’attente n’a pas été placée dans la boîte aux lettres. Vous pouvez accéder à l’étape 5 et supprimer des éléments dans le dossier éléments récupérables.

Si la valeur de la propriété *DelayHoldApplied* est définie sur **True**, exécutez la commande suivante pour supprimer la suspension de délai d’attente :

```
Set-Mailbox <username> -RemoveDelayHoldApplied
```
Notez que vous devez être affecté au rôle suspens pour raisons juridiques dans Exchange Online à utiliser le paramètre *RemoveDelayHoldApplied* .

## <a name="step-5-delete-items-in-the-recoverable-items-folder"></a>Étape 5 : Supprimer des éléments dans le dossier éléments récupérables

Vous êtes maintenant prêt à supprimer les éléments dans le dossier éléments récupérables à l’aide de l’applet de commande [Search-Mailbox](https://go.microsoft.com/fwlink/?linkid=852595) dans Exchange Online PowerShell. Vous disposez de trois options lors de l’exécution de l’applet de commande **Search-Mailbox** . 
  
- Copier des éléments dans une boîte aux lettres cible avant de les supprimer afin que vous pouvez consulter les articles, si nécessaire, avant de les supprimer.
    
- Copier des éléments dans une boîte aux lettres cible et les supprimer dans la même commande.
    
- Supprimer des éléments sans les copier dans une boîte aux lettres cible. 
    
Notez que les éléments dans le dossier éléments récupérables dans la boîte aux lettres de l’utilisateur principal d’archivage seront également supprimés lorsque vous exécutez l’applet de commande **Search-Mailbox** . Pour éviter ce problème, vous pouvez inclure le commutateur *DoNotIncludeArchive* . Et comme indiqué précédemment, si l’extension automatique d’archivage est activé pour la boîte aux lettres, les ** Search-Mailbox ** applet de commande ne les éléments supprimés dans une boîte aux lettres d’archive auxiliaire. Pour plus d’informations sur l’extension automatique d’archivage, consultez la rubrique [vue d’ensemble de l’archivage illimité dans Office 365](unlimited-archiving.md).
  
> [!NOTE]
> Si vous incluez une requête de recherche (à l'aide du paramètre  *SearchQuery*  ), la cmdlet **Search-Mailbox** renverra au maximum 10 000 éléments dans les résultats de recherche. Ainsi, si vous incluez une requête de recherche, vous devrez peut-être exécuter la commande **Search-Mailbox** plusieurs fois pour supprimer plus de 10 000 éléments. 
  
Les exemples suivants montrent la syntaxe de commande pour chacune de ces options. Ces exemples utilisent le `-SearchQuery size>0` valeur de paramètre, qui supprime tous les éléments de tous les sous-dossiers du dossier éléments récupérables. Si vous devez supprimer uniquement les éléments qui correspondent aux conditions spécifiques, vous pouvez également utiliser le paramètre *SearchQuery* pour spécifier d’autres conditions, telles que l’objet d’un message ou une plage de dates. Consultez les [autres exemples d’utilisation le paramètre SearchQuery](#other-examples-of-using-the-searchquery-parameter) ci-dessous. 
  
### <a name="example-1"></a>Exemple 1

Cet exemple copie tous les éléments dans le dossier éléments récupérables de l’utilisateur dans un dossier de boîte aux lettres de découverte de votre organisation. Cela vous permet de passer en revue les avant de vous les supprimez définitivement.

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -TargetMailbox "Discovery Search Mailbox" -TargetFolder "<foldername>"
```

Dans l’exemple précédent, il n’est pas nécessaire de copier des éléments dans la boîte aux lettres de découverte. Vous pouvez copier des messages dans une boîte aux lettres cible. Toutefois, pour empêcher l’accès aux données de boîte aux lettres potentiellement sensibles, il est recommandé de copier des messages dans une boîte aux lettres qui dispose d’un accès limité au personnel autorisé. Par défaut, l’accès à la boîte aux lettres de découverte par défaut est limité aux membres du groupe de rôles de gestion de la découverte dans Exchange Online. 
  
### <a name="example-2"></a>Exemple 2

Cet exemple copie tous les éléments dans le dossier éléments récupérables de l’utilisateur dans un dossier de boîte aux lettres de découverte de votre organisation, puis supprime les éléments du dossier éléments récupérables de l’utilisateur.

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -TargetMailbox "Discovery Search Mailbox" -TargetFolder "<foldername>" -DeleteContent
```
 
### <a name="example-3"></a>Exemple 3

Cet exemple supprime tous les éléments dans le dossier éléments récupérables de l’utilisateur, sans les copier dans une boîte aux lettres cible. 

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -DeleteContent
```

### <a name="other-examples-of-using-the-searchquery-parameter"></a>Autres exemples d’utilisation le paramètre SearchQuery

Voici quelques exemples d’utilisation le paramètre *SearchQuery* pour rechercher des messages spécifiques. Si vous utilisez le paramètre *SearchQuery* pour rechercher des éléments spécifiques, envisagez de copier les résultats de recherche dans une boîte aux lettres cible afin que vous pouvez examiner les résultats de recherche et ensuite modifier la requête si nécessaire avant de supprimer les résultats d’une recherche. 
  
Cet exemple renvoie des messages qui contiennent une expression spécifique dans le champ objet.
  
```
SearchQuery 'subject:"MAIL_BOX VALIDATION/UPGRADE!!!"' 
```

Cet exemple renvoie des messages qui ont été envoyés au sein de la plage de dates spécifiée.
  
```
SearchQuery 'sent>=06/01/2016 AND sent<=09/01/2016'
```
 
Cet exemple renvoie des messages qui ont été envoyés à la personne spécifiée.

```
SearchQuery 'to:garthf@alpinehouse.com'
```
   
### <a name="verify-that-items-were-deleted"></a>Vérifiez que les éléments ont été supprimés

Pour vérifier que vous avez bien supprimé des éléments à partir du dossier éléments récupérables d’une boîte aux lettres, la cmdlet **Get-MailboxFolderStatistics** dans Exchange Online PowerShell pour vérifier la taille et le nombre d’éléments dans le dossier éléments récupérables. Vous pouvez comparer ces statistiques avec celles que vous avez collectées à l’étape 1. 
  
Pour obtenir la taille actuelle et le nombre total d’éléments dans des dossiers et les sous-dossiers du dossier éléments récupérables dans la boîte aux lettres principale de l’utilisateur, exécutez la commande suivante dans. 
  
```
Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
```
   
Exécutez la commande suivante pour obtenir la taille et le nombre total d’éléments dans des dossiers et les sous-dossiers du dossier éléments récupérables dans la boîte aux lettres de l’utilisateur archive. 

```
Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems -Archive | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
```
  
## <a name="step-6-revert-the-mailbox-to-its-previous-state"></a>Étape 6 : Rétablir la boîte aux lettres à son état précédent

L’étape finale consiste à rétablir la boîte aux lettres à sa configuration précédente. Cela signifie réinitialiser les propriétés que vous avez modifié à l’étape 2 et réappliquer la suspension que vous avez supprimé à l’étape 3. Cela inclut :
  
- Modification de la période de rétention des éléments supprimés retour à sa valeur précédente. Autrement, vous pouvez laissez ce définie sur 30 jours, la valeur maximale dans Exchange Online.
    
- Réactivation de récupération d’élément unique.
    
- Réactivation les méthodes d’accès client afin que le propriétaire peut accéder à leur boîte aux lettres.
    
- Réappliquer les suspensions et les stratégies de rétention Office 365 que vous avez supprimé.
    
- Réactivation de l’Assistant dossier géré pour traiter la boîte aux lettres.
    
> [!IMPORTANT]
> Nous vous conseillons d’attendre 24 heures après l’application réutilisation d’une suspension ou un Office 365 rétention stratégie (et vérifier qu’il est en place) avant de vous réactivez l’Assistant dossier géré pour traiter la boîte aux lettres. 
  
Dans Exchange Online PowerShell, procédez comme suit (dans l’ordre spécifié).
  
1. Exécuter la commande suivante pour modifier la période de rétention des éléments supprimés retour à sa valeur d’origine. Cela suppose que le paramètre précédent est inférieure à 30 jours ; par exemple 14 jours. 
    
    ```
    Set-Mailbox <username> -RetainDeletedItemsFor 14
    ```
   
2. Exécutez la commande suivante pour réactiver récupération d’élément unique.
   
    ```
    Set-Mailbox <username> -SingleItemRecoveryEnabled $true
    ```

3. Exécutez la commande suivante pour réactiver toutes les méthodes d’accès client pour la boîte aux lettres.
    
    ```
    Set-CASMailbox <username> -EwsEnabled $true -ActiveSyncEnabled $true -MAPIEnabled $true -OWAEnabled $true -ImapEnabled $true -PopEnabled $true
    ```
   
4. Réappliquer la suspension que vous avez supprimé à l’étape 3. Selon le type d’attente, utilisez une des procédures suivantes.
    
    **Conservation pour litige**
    
    Exécutez la commande suivante pour réactiver un litige pour la boîte aux lettres.
    
    ```
    Set-Mailbox <username> -LitigationHoldEnabled $true
    ```

    **In-Place Hold**
    
    Utiliser le centre d’administration Exchange (ou Exchange Online PowerShell) pour ajouter la boîte aux lettres à la In-Place Hold. 
    
    **Office 365 de rétention appliquée à des boîtes aux lettres spécifiques**
    
    Utilisez la sécurité &amp; centre de conformité pour ajouter la boîte aux lettres à la stratégie de rétention d’Office 365. Accédez à la **gouvernance de Date** \> page de **rétention** dans la sécurité &amp; centre de conformité, modifiez la stratégie de rétention et ajoutez la boîte aux lettres à la liste de destinataires auxquels la stratégie de rétention est appliquée à. 
    
    **Stratégies de rétention de l’organisation Office 365**
    
    Si vous avez supprimé une échelle de l’organisation ou de la stratégie de rétention Exchange à l’échelle par l’exclusion de la stratégie, puis utiliser la sécurité &amp; centre de conformité pour supprimer la boîte aux lettres à partir de la liste d’exclure les utilisateurs. Accédez à la **gouvernance de Date** \> page de **rétention** dans la sécurité &amp; centre de conformité, modifier la stratégie de rétention de l’entreprise et supprimer la boîte aux lettres à partir de la liste des destinataires exclus. Cette opération sera réappliquer la stratégie de rétention aux boîtes aux lettres de l’utilisateur. 
    
    **contient des cas de découverte électronique**
    
    Utilisez la sécurité &amp; centre de conformité pour ajouter la boîte aux lettres sauvegarder la suspension associé à une affaire eDiscovery. Accédez à la **recherche &amp; enquête** \> page de **découverte électronique** dans la sécurité &amp; centre de conformité, ouvrez le cas et ajoutez la boîte aux lettres à la suspension. 
    
5. Exécutez la commande suivante pour autoriser l’Assistant dossier géré à traiter à nouveau de la boîte aux lettres. Comme indiqué plus haut, nous vous conseillons d’attendre 24 heures après l’application réutilisation d’une suspension ou un Office 365 rétention stratégie (et vérifier qu’il est en place) avant de vous réactivez l’Assistant dossier géré. 

    ```
    Set-Mailbox <username> -ElcProcessingDisabled $false
    ```
   
6. Pour vérifier que la boîte aux lettres a été rétablie à sa configuration précédente, vous pouvez exécuter les commandes suivantes et comparez les paramètres à celles que vous avez collectées à l’étape 1.

    ```
    Get-Mailbox <username> | FL ElcProcessingDisabled,InPlaceHolds,LitigationHoldEnabled,RetainDeletedItemsFor,SingleItemRecoveryEnabled
    ```

    ```
    Get-CASMailbox <username> | FL EwsEnabled,ActiveSyncEnabled,MAPIEnabled,OWAEnabled,ImapEnabled,PopEnabled
    ```
  
## <a name="more-information"></a>Plus d’informations

Voici un tableau qui décrit comment identifier les différents types de suspensions en fonction des valeurs dans la propriété *InPlaceHolds* lorsque vous exécutez les applets de commande **Get-Mailbox** ou **Get-OrganizationConfig** . Pour plus d’informations, voir [Comment faire pour identifier le type de blocage placé dans une boîte aux lettres Exchange Online](identify-a-hold-on-an-exchange-online-mailbox.md).

Comme indiqué, vous devez supprimer toutes les suspensions et stratégies de rétention d’Office 365 à partir d’une boîte aux lettres avant de supprimer les éléments dans le dossier éléments récupérables. 
  
|**Type de conservation**|**Exemple de valeur**|**Comment identifier la suspension**|
|:-----|:-----|:-----|
|Conservation pour litige  <br/> | `True` <br/> |La propriété  *LitigationHoldEnabled*  est définie sur  `True`.  <br/> |
|Blocage local  <br/> | `c0ba3ce811b6432a8751430937152491` <br/> |La propriété *InPlaceHolds* contient le GUID de la conservation inaltérable qui est placé sur la boîte aux lettres. Vous pouvez indiquer qu'il s’agit d’une conservation inaltérable, car le GUID ne commence pas par un préfixe.<br/> Vous pouvez utiliser la `Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL` command dans Exchange Online PowerShell pour obtenir des informations sur la conservation inaltérable dans la boîte aux lettres.  <br/> |
| Stratégies de rétention Office 365 dans la sécurité &amp; centre de conformité appliquée aux boîtes aux lettres spécifiques  <br/> | `mbxcdbbb86ce60342489bff371876e7f224` <br/> ou  <br/>  `skp127d7cf1076947929bf136b7a2a8c36f` <br/> |Lorsque vous exécutez l’applet de commande **Get-Mailbox** , la propriété *InPlaceHolds* contient également les GUID d’Office 365 les stratégies de rétention appliquées à la boîte aux lettres. Vous pouvez identifier les stratégies de rétention, car le GUID commence par la `mbx` préfixe. Notez que si le GUID de la stratégie de rétention commence par la `skp` préfixe, ce qui indique que la stratégie de rétention est appliquée aux Skype pour des conversations.<br/> Pour la stratégie de rétention identité Office 365 qui est appliqué à la boîte aux lettres, exécutez la commande suivante dans la sécurité &amp; PowerShell du centre de conformité : <br/> <br/>`Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name`<br/><br/>N’oubliez pas de supprimer le `mbx` ou `skp` préfixe lorsque vous exécutez cette commande.  <br/> |
|Stratégies de rétention d’Office 365 à l’échelle de l’organisation de la sécurité &amp; centre de conformité  <br/> |Aucune valeur  <br/> ou  <br/>  `-mbxe9b52bf7ab3b46a286308ecb29624696`(indique que la boîte aux lettres est exclu d’une stratégie de l’entreprise)  <br/> |Même si la propriété *InPlaceHolds* est vide lorsque vous exécutez l’applet de commande **Get-Mailbox** , toujours il peut y avoir au moins une échelle de l’organisation Office 365 de rétention appliquée à la boîte aux lettres.  <br/> Pour vérifier cela, vous pouvez exécuter la `Get-OrganizationConfig | FL InPlaceHolds` command dans Exchange Online PowerShell pour obtenir une liste de GUID pour les stratégies de rétention d’Office 365 à l’échelle de l’organisation. Le GUID de l’organisation de rétention appliquée au démarrage de boîtes aux lettres Exchange avec la `mbx` préfixe ; par exemple `mbxa3056bb15562480fadb46ce523ff7b02`.<br/> Identité de la stratégie de rétention d’Office 365 à l’échelle de l’organisation qui est appliquée à la boîte aux lettres, exécutez la commande suivante dans la sécurité &amp; PowerShell du centre de conformité : <br/><br/> `Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name`<br/><br/>Notez que si une boîte aux lettres est exclu d’une stratégie de rétention à l’échelle de l’organisation Office 365, le GUID de la stratégie de rétention est affiché dans la propriété *InPlaceHolds* de boîte aux lettres de l’utilisateur lorsque vous exécutez l’applet de commande **Get-Mailbox** ; Il est identifié par le préfixe `-mbx`; par exemple,`-mbxe9b52bf7ab3b46a286308ecb29624696` <br/> |
|blocage de cas de découverte électronique dans la sécurité &amp; centre de conformité  <br/> | `UniH7d895d48-7e23-4a8d-8346-533c3beac15d` <br/> |La propriété *InPlaceHolds* contient également le GUID de n’importe quel suspension associé à un cas de découverte électronique dans la sécurité &amp; centre de conformité peuvent être placées sur la boîte aux lettres. Vous pouvez indiquer il s’agit d’un blocage cas eDiscovery, car le GUID commence par la `UniH` préfixe.<br/> Vous pouvez utiliser la `Get-CaseHoldPolicy` applet de commande de la sécurité &amp; PowerShell du centre de conformité pour obtenir des informations sur le cas de découverte électronique qui est associée à la suspension de la boîte aux lettres. Par exemple, vous pouvez exécuter la commande `Get-CaseHoldPolicy <hold GUID without prefix> | FL Name` pour afficher le nom de la suspension de cas qui se trouve sur la boîte aux lettres. N’oubliez pas de supprimer le `UniH` préfixe lorsque vous exécutez cette commande.<br/><br/> Pour identifier le cas de découverte électronique qui est associée à la suspension de la boîte aux lettres, exécutez les commandes suivantes :<br/><br/>`$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>`<br/><br/>`Get-ComplianceCase $CaseHold.CaseId | FL Name`


