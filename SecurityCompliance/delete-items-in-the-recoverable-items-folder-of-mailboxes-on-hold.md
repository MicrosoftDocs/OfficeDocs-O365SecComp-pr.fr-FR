---
title: Supprimer des éléments dans le dossier éléments récupérables des boîtes aux lettres en nuage en attente-aide de l'administrateur
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: a85e1c87-a48e-4715-bfa9-d5275cde67b0
description: "Pour les administrateurs: supprimez les éléments du dossier éléments récupérables d'un utilisateur pour une boîte aux lettres Exchange Online, même si cette boîte aux lettres est placée en conservation légale. Il s'agit d'un moyen efficace de supprimer des données accidentellement propagées dans Office 365."
ms.openlocfilehash: 7badd45f582e4d5fef4cb5708c504573da0aba50
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2019
ms.locfileid: "31000077"
---
# <a name="delete-items-in-the-recoverable-items-folder-of-cloud-based-mailboxes-on-hold---admin-help"></a>Supprimer des éléments dans le dossier éléments récupérables des boîtes aux lettres en nuage en attente-aide de l'administrateur

Le dossier éléments récupérables d'une boîte aux lettres Exchange Online existe pour une protection contre les suppressions accidentelles ou malveillantes. Il est également utilisé pour stocker les éléments conservés et accessibles par les fonctionnalités de conformité d'Office 365, telles que les suspensions et les recherches de découverte électronique. Toutefois, dans certains cas, les organisations peuvent avoir des données qui ont été involontairement conservées dans le dossier éléments récupérables qu'elles doivent supprimer. Par exemple, un utilisateur peut envoyer ou transférer sans le savoir un message électronique contenant des informations sensibles ou des informations susceptibles d'avoir des répercussions importantes. Même si le message est supprimé définitivement, il peut être conservé indéfiniment, car une conservation légale a été placée sur la boîte aux lettres. Ce scénario est appelé fuite de données, car les données ont été involontairement propagées dans Office 365. Dans ce cas, vous pouvez supprimer des éléments du dossier éléments récupérables d'un utilisateur pour une boîte aux lettres Exchange Online, même si cette boîte aux lettres est placée en conservation avec l'une des autres fonctionnalités de blocage dans Office 365. Ces types de conservation incluent les conservations pour litige, les conservations inaltérables, les conservations de découverte électronique et les stratégies de rétention Office 365 créées dans le centre de sécurité et conformité dans Office 365 ou Microsoft 365.
  
 Cet article explique comment supprimer des éléments du dossier éléments récupérables pour les boîtes aux lettres en nuage qui sont en conservation. Cette procédure implique la désactivation de l'accès à la boîte aux lettres et la désactivation de la récupération d'élément unique, la désactivation de l'Assistant dossier géré pour le traitement de la boîte aux lettres, la suppression temporaire du blocage, la suppression des éléments du dossier éléments récupérables, puis la restauration la boîte aux lettres à sa configuration précédente. Voici le processus: 
  
[Étape 1: collecter des informations sur la boîte aux lettres](#step-1-collect-information-about-the-mailbox)

[Étape 2: préparer la boîte aux lettres](#step-2-prepare-the-mailbox)

[Étape 3: supprimer toutes les suspensions de la boîte aux lettres](#step-3-remove-all-holds-from-the-mailbox)

[Étape 4: supprimer le délai de conservation de la boîte aux lettres](#step-4-remove-the-delay-hold-from-the-mailbox)

[Étape 5: supprimer des éléments dans le dossier éléments récupérables](#step-5-delete-items-in-the-recoverable-items-folder)

[Étape 6: rétablir l'état précédent de la boîte aux lettres](#step-6-revert-the-mailbox-to-its-previous-state)
  
> [!CAUTION]
> Les procédures décrites dans cet article entraînent la suppression définitive des données (purgées) d'une boîte aux lettres Exchange Online. Cela signifie que les messages que vous supprimez du dossier éléments récupérables ne peuvent pas être récupérés et ne sont pas disponibles pour la découverte légale ou d'autres objectifs de conformité. Si vous souhaitez supprimer des messages d'une boîte aux lettres bloquée dans le cadre d'une conservation pour litige, d'une conservation inaltérable, d'une conservation eDiscovery ou d'une stratégie de rétention Office 365 créée dans le centre de sécurité et de conformité, vérifiez auprès de votre gestion des enregistrements ou de vos services juridiques. avant de supprimer le blocage. Votre organisation peut avoir une stratégie qui détermine si une boîte aux lettres en attente ou un incident de débordement de données est prioritaire. 
  
## <a name="before-you-begin"></a>Avant de commencer

- Vous devez disposer des deux rôles de gestion suivants dans Exchange Online pour rechercher et supprimer des messages dans le dossier éléments récupérables à l'étape 5.
    
  - **Recherche de boîte aux lettres** -ce rôle vous permet de rechercher des boîtes aux lettres dans votre organisation. Ce rôle n'est pas attribué par défaut aux administrateurs Exchange. Pour vous attribuer ce rôle, ajoutez-vous en tant que membre du groupe de rôles gestion de la découverte dans Exchange Online. 
    
  - **Importation de boîte aux lettres** -ce rôle vous permet de supprimer des messages de la boîte aux lettres d'un utilisateur. Par défaut, ce rôle n'est attribué à aucun groupe de rôles. Pour supprimer des messages des boîtes aux lettres des utilisateurs, vous pouvez ajouter le rôle exportation d'importation de boîte aux lettres au groupe de rôles gestion de l'organisation dans Exchange Online. 
    
- La procédure décrite dans cet article n'est pas prise en charge pour les boîtes aux lettres inactives. Cela est dû au fait que vous ne pouvez pas réappliquer une stratégie de rétention (ou une stratégie de rétention Office 365) à une boîte aux lettres inactive après l'avoir supprimée. Lorsque vous supprimez une conservation d'une boîte aux lettres inactive, celle-ci est remplacée par une boîte aux lettres normale et supprimée définitivement de votre organisation après avoir été traitée par l'Assistant dossier géré.
    
- Vous ne pouvez pas effectuer cette procédure pour une boîte aux lettres affectée à une stratégie de rétention Office 365 qui a été verrouillée avec un verrou de conservation. Cela est dû au fait qu'un verrouillage de conservation vous empêche de supprimer ou d'exclure la boîte aux lettres de la stratégie de rétention Office 365 et de désactiver l'Assistant dossier géré sur la boîte aux lettres. Pour plus d'informations sur le verrouillage des stratégies de rétention, voir [verrouillage d'une stratégie de](retention-policies.md#locking-a-retention-policy)rétention.
    
- Si une boîte aux lettres n'est pas placée en conservation (ou si la récupération d'élément unique n'est pas activée), vous pouvez simplement supprimer les éléments du dossier éléments récupérables. Pour plus d'informations sur la procédure à suivre, consultez la rubrique [Rechercher et supprimer des messages ](https://go.microsoft.com/fwlink/?linkid=852453).
  
## <a name="step-1-collect-information-about-the-mailbox"></a>Étape 1: collecter des informations sur la boîte aux lettres

Cette première étape consiste à collecter les propriétés sélectionnées à partir de la boîte aux lettres cible qui affecteront cette procédure. N'oubliez pas de noter ces paramètres ou de les enregistrer dans un fichier texte, car vous modifierez certaines de ces propriétés, puis revenir aux valeurs d'origine à l'étape 6, après avoir supprimé des éléments du dossier éléments récupérables. Voici une liste des propriétés de boîte aux lettres que vous devez collecter.
  
-  *SingleItemRecoveryEnabled* et *RetainDeletedItemsFor* ; Si nécessaire, vous allez désactiver la récupération simple et augmenter la période de rétention des éléments supprimés à l'étape 3. 
    
-  *LitigationHoldEnabled* et *InPlaceHolds* ; vous devez identifier toutes les suspensions placées sur la boîte aux lettres pour pouvoir les supprimer temporairement à l'étape 3. Consultez la section [plus d'informations](#more-information) pour obtenir des conseils sur la façon d'identifier la conservation de type qui peut être placée sur une boîte aux lettres. 
    
En outre, vous devez obtenir les paramètres d'accès au client de boîte aux lettres afin de les désactiver temporairement afin que le propriétaire (ou les autres utilisateurs) ne puissent pas accéder à la boîte aux lettres au cours de cette procédure. Enfin, vous pouvez obtenir la taille et le nombre d'éléments actuels dans le dossier éléments récupérables. Une fois que vous avez supprimé des éléments dans le dossier éléments récupérables à l'étape 5, vous utiliserez ces informations pour vérifier que les éléments ont été supprimés.
  
1. [Connectez-vous à Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=396554). Veillez à utiliser un nom d'utilisateur et un mot de passe pour un compte administrateur auquel des rôles de gestion appropriés ont été attribués dans Exchange Online. 
    
2. Exécutez la commande suivante pour obtenir des informations sur la récupération d'élément unique et la période de rétention des éléments supprimés.

    ```
    Get-Mailbox <username> | FL SingleItemRecoveryEnabled,RetainDeletedItemsFor
    ```

   Si la récupération d'élément unique est activée, vous devez la désactiver à l'étape 2. Si la période de rétention des éléments supprimés n'est pas définie sur 30 jours (la valeur maximale dans Exchange Online), vous pouvez l'augmenter à l'étape 2. 
    
3. Exécutez la commande suivante pour obtenir les paramètres d'accès aux boîtes aux lettres de la boîte aux lettres. 
    
    ```
    Get-CASMailbox <username> | FL EwsEnabled,ActiveSyncEnabled,MAPIEnabled,OWAEnabled,ImapEnabled,PopEnabled
    ```

   Vous allez désactiver toutes ces méthodes d'accès à l'étape 2.
    
4. Exécutez la commande suivante pour obtenir des informations sur les conservations et les stratégies de rétention Office 365 appliquées à la boîte aux lettres.
    
    ```
    Get-Mailbox <username> | FL LitigationHoldEnabled,InPlaceHolds
    ```


   > [!TIP]
    > S'il y a trop de valeurs dans la propriété *InPlaceHolds* et qu'elles ne sont pas toutes affichées, vous pouvez `Get-Mailbox <username> | Select-Object -ExpandProperty InPlaceHolds` exécuter la commande pour afficher chaque valeur sur une ligne distincte. 
  
5. Exécutez la commande suivante pour obtenir des informations sur les stratégies de rétention Office 365 à l'échelle de l'organisation. 

    ```
    Get-OrganizationConfig | FL InPlaceHolds
    ```
   Si votre organisation possède des stratégies de rétention Office 365 à l'échelle de l'organisation, vous devez exclure la boîte aux lettres de ces stratégies à l'étape 3.

   > [!TIP]
    > S'il y a trop de valeurs dans la propriété *InPlaceHolds* et qu'elles ne sont pas toutes affichées, vous pouvez `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` exécuter la commande pour afficher chaque valeur sur une ligne distincte. 
  
6. Exécutez la commande suivante pour obtenir la taille actuelle et le nombre total d'éléments dans les dossiers et sous-dossiers du dossier éléments récupérables dans la boîte aux lettres principale de l'utilisateur. 

    ```
    Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
    ```

   Si la boîte aux lettres d'archivage de l'utilisateur est activée, exécutez la commande suivante pour obtenir la taille et le nombre total d'éléments dans les dossiers et sous-dossiers du dossier éléments récupérables de leur boîte aux lettres d'archivage. 

    ```s
    Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems -Archive | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
    ```

   Lorsque vous supprimez des éléments à l'étape 5, vous pouvez choisir de supprimer ou de ne pas supprimer les éléments du dossier éléments récupérables dans la boîte aux lettres d'archivage principale de l'utilisateur. Notez que si l'archivage à extension automatique est activé pour la boîte aux lettres, les éléments d'une boîte aux lettres d'archivage auxiliaire ne seront pas supprimés.
  
## <a name="step-2-prepare-the-mailbox"></a>Étape 2: préparer la boîte aux lettres

Après avoir collecté et enregistré les informations relatives à la boîte aux lettres, l'étape suivante consiste à préparer la boîte aux lettres en effectuant les tâches suivantes: 
  
- DésActivez l' **accès client à la boîte aux lettres de** sorte que le propriétaire de la boîte aux lettres ne puisse pas accéder à sa boîte aux lettres et modifier les données de la boîte aux lettres pendant cette procédure. 
    
- **Augmentez la période** de rétention des éléments supprimés à 30 jours (la valeur maximale dans Exchange Online) de sorte que les éléments ne soient pas supprimés du dossier éléments récupérables avant de pouvoir les supprimer à l'étape 5. 
    
- DésActivez la **récupération d'élément unique** de sorte que les éléments ne soient pas conservés (pendant la durée de la période de rétention des éléments supprimés) après les avoir supprimés du dossier éléments récupérables à l'étape 5. 
    
- **Désactivez l'Assistant dossier géré** afin qu'il ne traite pas la boîte aux lettres et conserve les éléments que vous supprimez à l'étape 5. 
    
Effectuez les étapes suivantes dans Exchange Online PowerShell.
  
1. Exécutez la commande suivante pour désactiver tous les accès client à la boîte aux lettres. La syntaxe de commande suppose que toutes les méthodes d'accès au client étaient activées sur la boîte aux lettres.

    ```   
    Set-CASMailbox <username> -EwsEnabled $false -ActiveSyncEnabled $false -MAPIEnabled $false -OWAEnabled $false -ImapEnabled $false -PopEnabled $false
    ```
   
   > [!NOTE]
    > La désactivation de toutes les méthodes d'accès client à la boîte aux lettres peut prendre jusqu'à 60 minutes. Notez que la désactivation de ces méthodes d'accès ne déconnectera pas le propriétaire de la boîte aux lettres dans laquelle ils sont actuellement connectés. Si le propriétaire n'est pas connecté, il ne pourra pas accéder à sa boîte aux lettres après la désactivation de ces méthodes d'accès. 
  
2. Exécutez la commande suivante pour augmenter la période de rétention des éléments supprimés le maximum de 30 jours. Cela suppose que le paramètre actuel est inférieur à 30 jours. 

    ```
    Set-Mailbox <username> -RetainDeletedItemsFor 30
    ```

3. Exécutez la commande suivante pour désactiver la récupération d'élément unique.
    
    ```
    Set-Mailbox <username> -SingleItemRecoveryEnabled $false
    ```

   > [!NOTE]
    > La désactivation de la récupération d'élément unique peut prendre jusqu'à 60 minutes. Ne supprimez pas les éléments dans le dossier éléments récupérables tant que cette période n'est pas écoulée. 
  
4. Exécutez la commande suivante pour empêcher l'Assistant dossier géré de traiter la boîte aux lettres. Comme expliqué précédemment, vous pouvez désactiver l'Assistant dossier géré uniquement si une stratégie de rétention Office 365 avec un verrou de conservation n'est pas appliquée à la boîte aux lettres. 

    ```
    Set-Mailbox <username> -ElcProcessingDisabled $true
    ```

## <a name="step-3-remove-all-holds-from-the-mailbox"></a>Étape 3: supprimer toutes les suspensions de la boîte aux lettres

La dernière étape avant que vous ne puissiez supprimer des éléments du dossier éléments récupérables consiste à supprimer toutes les suspensions (que vous avez identifiées à l'étape 1) placées dans la boîte aux lettres. Toutes les conservations doivent être supprimées afin que les éléments ne soient pas conservés après leur suppression du dossier éléments récupérables. Les sections suivantes contiennent des informations sur la suppression des différents types de suspensions sur une boîte aux lettres. Consultez la section [plus d'informations](#more-information) pour obtenir des conseils sur la façon d'identifier la conservation de type qui peut être placée sur une boîte aux lettres. Pour plus d'informations, voir [Comment identifier le type de suspension placé sur une boîte aux lettres Exchange Online](identify-a-hold-on-an-exchange-online-mailbox.md).
  
> [!CAUTION]
> Comme indiqué précédemment, vérifiez auprès de votre gestion des enregistrements ou des services juridiques avant de supprimer un blocage d'une boîte aux lettres. 
  
 ### <a name="litigation-hold"></a>Conservation pour litige
  
Exécutez la commande suivante dans Exchange Online PowerShell pour supprimer une suspension pour litige de la boîte aux lettres.

```
Set-Mailbox <username> -LitigationHoldEnabled $false
```

   
> [!NOTE]
> À l'inStar de la désactivation des méthodes d'accès au client et de la récupération d'élément unique, la suppression de la conservation pour litige peut prendre jusqu'à 60 minutes. Ne supprimez pas les éléments du dossier éléments récupérables tant que cette période n'est pas écoulée. 
  
 ### <a name="in-place-hold"></a>Blocage local
  
Exécutez la commande suivante dans Exchange Online PowerShell pour identifier la conservation inaltérable qui est placée sur la boîte aux lettres. Utilisez le GUID pour le blocage sur place que vous avez identifié à l'étape 1. 

```
Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL Name
```
   
Après avoir identifié le blocage sur place, vous pouvez utiliser le centre d'administration Exchange ou Exchange Online PowerShell pour supprimer la boîte aux lettres de la suspension. Pour plus d'informations, voir [Créer ou supprimer une conservation inaltérable](https://go.microsoft.com/fwlink/?linkid=852668).
  
 ### <a name="office-365-retention-policies-applied-to-specific-mailboxes"></a>Stratégies de rétention Office 365 appliquées à des boîtes aux lettres spécifiques
  
Exécutez la commande suivante dans le [Centre de sécurité _AMP_ Compliance Center PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) pour identifier la stratégie de rétention Office 365 qui est appliquée à la boîte aux lettres. Utilisez le GUID (sans le `mbx` préfixe `skp` ou) pour la stratégie de rétention que vous avez identifiée à l'étape 1. 

```
Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name
```
   
Après avoir identifié la stratégie de rétention, accédez à la page rétention de la **gouvernance** \> **** de sécurité dans le centre de sécurité & conformité, modifiez la stratégie de rétention que vous avez identifiée à l'étape précédente et supprimez la boîte aux lettres de la liste des destinataires inclus dans la stratégie de rétention. 
  
 ### <a name="organization-wide-office-365-retention-policies"></a>Stratégies de rétention Office 365 à l'échelle de l'Organisation
  
Les stratégies de rétention Office 365 à l'échelle de l'organisation et d'Exchange à l'échelle de l'organisation sont appliquées à chaque boîte aux lettres dans l'organisation. Elles sont appliquées au niveau de l'organisation (et non au niveau de la boîte aux lettres) et sont renvoyées lorsque vous exécutez la cmdlet **Get-OrganizationConfig** à l'étape 1. Exécutez la commande suivante dans [Security _AMP_ Compliance Center PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) pour identifier les stratégies de rétention Office 365 à l'échelle de l'organisation. Utilisez le GUID (sans le `mbx` préfixe) pour les stratégies de rétention à l'échelle de l'organisation que vous avez identifiées à l'étape 1. 

```
Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name
```

après avoir identifié les stratégies de rétention Office 365 à l'échelle de l'organisation, accédez à la page rétention de la gestion des **dates** \> **** dans le centre de sécurité & Compliance Center, modifiez chaque stratégie de rétention à l'échelle de l'organisation que vous avez identifiée dans le étape précédente, puis ajoutez la boîte aux lettres à la liste des destinataires exclus. Cette opération supprimera la boîte aux lettres de l'utilisateur de la stratégie de rétention. 

### <a name="office-365-retention-labels"></a>Étiquettes de rétention Office 365

Chaque fois qu'un utilisateur applique une étiquette configurée pour conserver le contenu ou conserver, puis supprimer le contenu d'un dossier ou d'un élément de sa boîte aux lettres, la propriété de boîte aux lettres *ComplianceTagHoldApplied* est définie sur **true**. Dans ce cas, la boîte aux lettres est considérée comme étant en attente, comme si elle était placée en conservation pour litige ou affectée à une stratégie de rétention Office 365.

Pour afficher la valeur de la propriété *ComplianceTagHoldApplied* , exécutez la commande suivante dans Exchange Online PowerShell:

```
Get-Mailbox <username> |FL ComplianceTagHoldApplied
```

Une fois que vous avez identifié qu'une boîte aux lettres est en attente, car une étiquette de rétention est appliquée à un dossier ou un élément, vous pouvez utiliser l'outil de recherche de contenu dans le centre de sécurité et de conformité pour rechercher des éléments étiquetés à l'aide de la condition de recherche ComplianceTag. Pour plus d'informations, consultez la section «conditions de recherche» dans la rubrique [requêtes de mots clés et conditions de recherche pour la recherche de contenu](keyword-queries-and-search-conditions.md#conditions-for-common-properties).

Pour plus d'informations sur les étiquettes, consultez la rubrique [vue d'ensemble des étiquettes Office 365](labels.md).

 ### <a name="ediscovery-case-holds"></a>conservations de cas eDiscovery
  
Exécutez les commandes suivantes dans [Security _AMP_ Compliance Center PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) pour identifier la conservation associée à un cas eDiscovery qui est appliqué à la boîte aux lettres. Utilisez le GUID (sans le `UniH` préfixe) pour le blocage eDiscovery que vous avez identifié à l'étape 1. Notez que la deuxième commande affiche le nom du cas eDiscovery auquel la conservation est associée; la troisième commande affiche le nom de la suspension. 
  
```
$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>
```

```
Get-ComplianceCase $CaseHold.CaseId | FL Name
```

```
$CaseHold.Name
```

Une fois que vous avez identifié le nom du cas eDiscovery et le blocage, accédez à la page **découverte** électronique **eDiscovery** \> dans le centre de conformité, ouvrez le cas, puis supprimez la boîte aux lettres de la suspension. Pour plus d'informations, consultez la rubrique [cas eDiscovery](ediscovery-cases.md).
  
## <a name="step-4-remove-the-delay-hold-from-the-mailbox"></a>Étape 4: supprimer le délai de conservation de la boîte aux lettres

Après la suppression d'un type de conservation d'une boîte aux lettres, la valeur de la propriété de boîte aux lettres *DelayHoldApplied* est définie sur **true**. Cela se produit la prochaine fois que l'Assistant dossier géré traite la boîte aux lettres et détecte qu'une conservation a été supprimée. Il s'agit d'une *attente de retard* qui signifie que la suppression effective de la conservation est retardée de 30 jours pour empêcher la suppression définitive des données de la boîte aux lettres. (L'objectif d'un délai de blocage est de permettre aux administrateurs de rechercher ou de récupérer des éléments de boîte aux lettres qui seront purgés après la suppression d'une conservation).  Lorsqu'une boîte aux lettres est suspendue, la boîte aux lettres est toujours considérée comme suspendue pendant une durée illimitée, comme si la boîte aux lettres était en conservation pour litige. Au bout de 30 jours, le délai d'attente expire et Office 365 tente automatiquement de supprimer le blocage de délai (en définissant la propriété *DelayHoldApplied* sur **false**) de sorte que la conservation soit effectivement supprimée. 

Avant de pouvoir supprimer des éléments à l'étape 5, vous devez supprimer le délai de conservation de la boîte aux lettres. Tout d'abord, déterminez si la conservation du retard est appliquée à la boîte aux lettres en exécutant la commande suivante dans Exchange Online PowerShell:

```
Get-Mailbox <username> | FL DelayHoldApplied
```

Si la valeur de la propriété *DelayHoldApplied* est définie sur **false**, aucune temporisation n'a été placée sur la boîte aux lettres. Vous pouvez passer à l'étape 5 et supprimer des éléments dans le dossier éléments récupérables.

Si la valeur de la propriété *DelayHoldApplied* est définie sur **true**, exécutez la commande suivante pour supprimer la suspension de délai:

```
Set-Mailbox <username> -RemoveDelayHoldApplied
```
Notez que vous devez disposer du rôle conservation légal dans Exchange Online pour utiliser le paramètre *RemoveDelayHoldApplied* .

## <a name="step-5-delete-items-in-the-recoverable-items-folder"></a>Étape 5: supprimer des éléments dans le dossier éléments récupérables

Vous êtes maintenant prêt à supprimer des éléments dans le dossier éléments récupérables à l'aide de la cmdlet [Search-Mailbox](https://go.microsoft.com/fwlink/?linkid=852595) dans Exchange Online PowerShell. Vous disposez de trois options lors de l'exécution de la cmdlet **Search-Mailbox** . 
  
- Copiez les éléments vers une boîte aux lettres cible avant de les supprimer afin de pouvoir vérifier les éléments, le cas échéant, avant de les supprimer.
    
- Copiez les éléments dans une boîte aux lettres cible et supprimez-les dans la même commande.
    
- Supprimer des éléments sans les copier dans une boîte aux lettres cible. 
    
Notez que les éléments du dossier éléments récupérables de la boîte aux lettres d'archivage principale de l'utilisateur sont également supprimés lorsque vous exécutez la cmdlet **Search-Mailbox** . Pour éviter cela, vous pouvez inclure le commutateur  *DoNotIncludeArchive*  . Comme indiqué précédemment, si l'archivage à extension automatique est activé pour la boîte aux lettres, la cmdlet * * Search-Mailbox * * n'a pas de suppression des éléments dans une boîte aux lettres d'archivage auxiliaire. Pour plus d'informations sur l'archivage à extension automatique, consultez la rubrique [vue d'ensemble de l'archivage illimité dans Office 365](unlimited-archiving.md).
  
> [!NOTE]
> Si vous incluez une requête de recherche (à l'aide du paramètre  *SearchQuery*  ), la cmdlet **Search-Mailbox** renverra au maximum 10 000 éléments dans les résultats de recherche. Ainsi, si vous incluez une requête de recherche, vous devrez peut-être exécuter la commande **Search-Mailbox** plusieurs fois pour supprimer plus de 10 000 éléments. 
  
Les exemples suivants illustrent la syntaxe de commande pour chacune de ces options. Ces exemples utilisent la `-SearchQuery size>0` valeur de paramètre, qui supprime tous les éléments de tous les sous-dossiers dans le dossier éléments récupérables. Si vous devez supprimer uniquement les éléments qui correspondent à des conditions spécifiques, vous pouvez également utiliser le paramètre *SearchQuery* pour spécifier d'autres conditions, telles que l'objet d'un message ou une plage de dates. Consultez les [autres exemples de l'utilisation du paramètre SearchQuery](#other-examples-of-using-the-searchquery-parameter) ci-dessous. 
  
### <a name="example-1"></a>Exemple 1

Cet exemple copie tous les éléments du dossier éléments récupérables de l'utilisateur dans un dossier de la boîte aux lettres de découverte de votre organisation. Cela vous permet de vérifier les éléments avant de les supprimer définitivement.

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -TargetMailbox "Discovery Search Mailbox" -TargetFolder "<foldername>"
```

Dans l'exemple précédent, il n'est pas nécessaire de copier des éléments dans la boîte aux lettres de découverte. Vous pouvez copier des messages vers n'importe quelle boîte aux lettres cible. Toutefois, pour empêcher l'accès aux données de boîte aux lettres potentiellement sensibles, nous vous recommandons de copier les messages dans une boîte aux lettres dont l'accès est limité au personnel autorisé. Par défaut, l'accès à la boîte aux lettres de découverte par défaut est limité aux membres du groupe de rôles gestion de la découverte dans Exchange Online. 
  
### <a name="example-2"></a>Exemple 2

Cet exemple copie tous les éléments du dossier éléments récupérables de l'utilisateur dans un dossier de la boîte aux lettres de découverte de votre organisation, puis supprime les éléments du dossier éléments récupérables de l'utilisateur.

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -TargetMailbox "Discovery Search Mailbox" -TargetFolder "<foldername>" -DeleteContent
```
 
### <a name="example-3"></a>Exemple 3

Cet exemple supprime tous les éléments du dossier éléments récupérables de l'utilisateur, sans les copier dans une boîte aux lettres cible. 

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -DeleteContent
```

### <a name="other-examples-of-using-the-searchquery-parameter"></a>Autres exemples d'utilisation du paramètre SearchQuery

Voici quelques exemples d'utilisation du paramètre *SearchQuery* pour rechercher des messages spécifiques. Si vous utilisez le paramètre *SearchQuery* pour rechercher des éléments spécifiques, envisagez de copier les résultats de la recherche dans une boîte aux lettres cible afin de pouvoir examiner les résultats de la recherche, puis de modifier la requête si nécessaire avant de supprimer les résultats d'une recherche. 
  
Cet exemple renvoie les messages qui contiennent une phrase spécifique dans le champ Subject.
  
```
SearchQuery 'subject:"MAIL_BOX VALIDATION/UPGRADE!!!"' 
```

Cet exemple renvoie les messages qui ont été envoyés dans la plage de dates spécifiée.
  
```
SearchQuery 'sent>=06/01/2016 AND sent<=09/01/2016'
```
 
Cet exemple renvoie les messages qui ont été envoyés à la personne spécifiée.

```
SearchQuery 'to:garthf@alpinehouse.com'
```
   
### <a name="verify-that-items-were-deleted"></a>Vérifier que les éléments ont été supprimés

Pour vérifier que vous avez bien supprimé des éléments du dossier éléments récupérables d'une boîte aux lettres, utilisez la cmdlet **Get-MailboxFolderStatistics** dans Exchange Online PowerShell pour vérifier la taille et le nombre d'éléments dans le dossier éléments récupérables. Vous pouvez comparer ces statistiques avec celles que vous avez collectées à l'étape 1. 
  
Exécutez la commande suivante dans pour obtenir la taille actuelle et le nombre total d'éléments dans les dossiers et sous-dossiers du dossier éléments récupérables dans la boîte aux lettres principale de l'utilisateur. 
  
```
Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
```
   
Exécutez la commande suivante pour obtenir la taille et le nombre total d'éléments dans les dossiers et sous-dossiers du dossier éléments récupérables dans la boîte aux lettres d'archivage de l'utilisateur. 

```
Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems -Archive | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
```
  
## <a name="step-6-revert-the-mailbox-to-its-previous-state"></a>Étape 6: rétablir l'état précédent de la boîte aux lettres

La dernière étape consiste à rétablir la configuration précédente de la boîte aux lettres. Cela signifie que vous devez réinitialiser les propriétés modifiées à l'étape 2 et appliquer de nouveau les conservations que vous avez supprimées à l'étape 3. Celles-ci incluent les valeurs suivantes :
  
- Modification de la période de rétention des éléments supprimés à sa valeur précédente. Vous pouvez également laisser cette valeur sur 30 jours, la valeur maximale dans Exchange Online.
    
- Réactivation de la récupération d'élément unique.
    
- Réactivation des méthodes d'accès client de sorte que le propriétaire puisse accéder à sa boîte aux lettres.
    
- Réapplication des suspensions et des stratégies de rétention Office 365 que vous avez supprimées.
    
- Réactivation de l'Assistant dossier géré pour traiter la boîte aux lettres.
    
> [!IMPORTANT]
> Nous vous recommandons d'attendre 24 heures après avoir appliqué une nouvelle stratégie de rétention ou une stratégie de rétention Office 365 (et de vérifier qu'elle est en place) avant de réactiver l'Assistant dossier géré pour traiter la boîte aux lettres. 
  
Effectuez les étapes suivantes (dans la séquence spécifiée) dans Exchange Online PowerShell.
  
1. Exécutez la commande suivante pour rétablir la valeur d'origine de la période de rétention des éléments supprimés. Cela suppose que le paramètre précédent soit inférieur à 30 jours; par exemple, 14 jours. 
    
    ```
    Set-Mailbox <username> -RetainDeletedItemsFor 14
    ```
   
2. Exécutez la commande suivante pour réactiver la récupération d'élément unique.
   
    ```
    Set-Mailbox <username> -SingleItemRecoveryEnabled $true
    ```

3. Exécutez la commande suivante pour réactiver toutes les méthodes d'accès client à la boîte aux lettres.
    
    ```
    Set-CASMailbox <username> -EwsEnabled $true -ActiveSyncEnabled $true -MAPIEnabled $true -OWAEnabled $true -ImapEnabled $true -PopEnabled $true
    ```
   
4. Réappliquez les suspensions que vous avez supprimées à l'étape 3. Selon le type de blocage, utilisez l'une des procédures suivantes.
    
    **Conservation pour litige**
    
    Exécutez la commande suivante pour réactiver une conservation pour litige pour la boîte aux lettres.
    
    ```
    Set-Mailbox <username> -LitigationHoldEnabled $true
    ```

    **In-Place Hold**
    
    Utilisez le centre d'administration Exchange (ou Exchange Online PowerShell) pour rajouter la boîte aux lettres à la conservation inaltérable. 
    
    **Stratégies de rétention Office 365 appliquées à des boîtes aux lettres spécifiques**
    
    Utilisez le centre de sécurité & Compliance Center pour rajouter la boîte aux lettres à la stratégie de rétention. Accédez à la page rétention de la **gouvernance** \> **** des dates dans le centre de sécurité & conformité, modifiez la stratégie de rétention, puis rajoutez la boîte aux lettres à la liste des destinataires auxquels la stratégie de rétention est appliquée. 
    
    **Stratégies de rétention Office 365 à l'échelle de l'Organisation**
    
    Si vous avez supprimé une stratégie de rétention à l'échelle de l'organisation ou de l'entreprise en l'excluant de la stratégie, utilisez le centre de sécurité & Compliance Center pour supprimer la boîte aux lettres de la liste des utilisateurs exclus. Accédez à la page rétention de la **gouvernance** \> **** des dates dans le centre de sécurité & conformité, modifiez la stratégie de rétention à l'échelle de l'organisation, puis supprimez la boîte aux lettres de la liste des destinataires exclus. Cette opération va réappliquer la stratégie de rétention à la boîte aux lettres de l'utilisateur. 
    
    **conservations de cas eDiscovery**
    
    Utilisez le centre de sécurité & Compliance Center pour rajouter à la boîte aux lettres le blocage associé à un cas de découverte électronique. Accédez à la **** \> page **découverte** électronique eDiscovery, ouvrez le cas et rajoutez la boîte aux lettres à la suspension. 
    
5. Exécutez la commande suivante pour permettre à l'Assistant dossier géré de traiter à nouveau la boîte aux lettres. Comme indiqué précédemment, nous vous recommandons d'attendre 24 heures après avoir appliqué une nouvelle stratégie de rétention ou une stratégie de rétention Office 365 (et de vérifier qu'elle est en place) avant de réactiver l'Assistant dossier géré. 

    ```
    Set-Mailbox <username> -ElcProcessingDisabled $false
    ```
   
6. Pour vérifier que la boîte aux lettres a été restaurée à sa configuration précédente, vous pouvez exécuter les commandes suivantes, puis comparer les paramètres à ceux que vous avez collectés à l'étape 1.

    ```
    Get-Mailbox <username> | FL ElcProcessingDisabled,InPlaceHolds,LitigationHoldEnabled,RetainDeletedItemsFor,SingleItemRecoveryEnabled
    ```

    ```
    Get-CASMailbox <username> | FL EwsEnabled,ActiveSyncEnabled,MAPIEnabled,OWAEnabled,ImapEnabled,PopEnabled
    ```
  
## <a name="more-information"></a>Plus d’informations

Voici un tableau qui décrit comment identifier différents types de suspensions en fonction des valeurs de la propriété *InPlaceHolds* lorsque vous exécutez les cmdlets **Get-Mailbox** ou **Get-OrganizationConfig** . Pour plus d'informations, voir [Comment identifier le type de suspension placé sur une boîte aux lettres Exchange Online](identify-a-hold-on-an-exchange-online-mailbox.md).

Comme expliqué précédemment, vous devez supprimer toutes les conservations et les stratégies de rétention d'Office 365 d'une boîte aux lettres avant de pouvoir supprimer des éléments dans le dossier éléments récupérables. 
  
|**Type de conservation**|**Exemple de valeur**|**Comment identifier la conservation**|
|:-----|:-----|:-----|
|Conservation pour litige  <br/> | `True` <br/> |La propriété  *LitigationHoldEnabled*  est définie sur  `True`.  <br/> |
|Blocage local  <br/> | `c0ba3ce811b6432a8751430937152491` <br/> |La propriété *InPlaceHolds* contient le GUID de la conservation inaltérable qui est placée sur la boîte aux lettres. Vous pouvez indiquer qu'il s'agit d'une conservation inaltérable, car le GUID ne commence pas par un préfixe.  <br/> Vous pouvez utiliser la `Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL` commande dans Exchange Online PowerShell pour obtenir des informations sur la conservation inaltérable sur la boîte aux lettres.  <br/> |
| Stratégies de rétention Office 365 dans le centre de sécurité & conformité appliquées à des boîtes aux lettres spécifiques  <br/> | `mbxcdbbb86ce60342489bff371876e7f224` <br/> ou  <br/>  `skp127d7cf1076947929bf136b7a2a8c36f` <br/> |Lorsque vous exécutez la cmdlet **Get-Mailbox** , la propriété *InPlaceHolds* contient également les GUID des stratégies de rétention d'Office 365 appliquées à la boîte aux lettres. Vous pouvez identifier les stratégies de rétention, car `mbx` le GUID commence par le préfixe. Notez que si le GUID de la stratégie de rétention `skp` commence par le préfixe, cela indique que la stratégie de rétention est appliquée aux conversations Skype entreprise.  <br/> Pour identifier la stratégie de rétention Office 365 qui est appliquée à la boîte aux lettres, exécutez la commande suivante dans Security & Compliance Center PowerShell: <br/> <br/>`Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name`<br/><br/>N'oubliez pas de supprimer le préfixe  `mbx` ou  `skp` lorsque vous exécutez cette commande.  <br/> |
|Stratégies de rétention Office 365 à l'échelle de l'organisation dans le centre de sécurité & Compliance Center  <br/> |Aucune valeur  <br/> ou  <br/>  `-mbxe9b52bf7ab3b46a286308ecb29624696`(indique que la boîte aux lettres est exclue d'une stratégie à l'échelle de l'organisation)  <br/> |Même si la propriété *InPlaceHolds* est vide lorsque vous exécutez la cmdlet **Get-Mailbox** , il peut y avoir une ou plusieurs stratégies de rétention Office 365 à l'échelle de l'organisation appliquées à la boîte aux lettres.  <br/> Pour ce faire, vous pouvez exécuter la `Get-OrganizationConfig | FL InPlaceHolds` commande dans Exchange Online PowerShell pour obtenir la liste des GUID pour les stratégies de rétention Office 365 à l'échelle de l'organisation. Le GUID des stratégies de rétention à l'échelle de l'organisation appliquées aux `mbx` boîtes aux lettres Exchange commence par le préfixe; par exemple `mbxa3056bb15562480fadb46ce523ff7b02`.  <br/> Pour identifier la stratégie de rétention Office 365 à l'échelle de l'organisation qui est appliquée à la boîte aux lettres, exécutez la commande suivante dans Security & Compliance Center PowerShell: <br/><br/> `Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name`<br/><br/>Notez que si une boîte aux lettres est exclue d'une stratégie de rétention Office 365 à l'échelle de l'organisation, le GUID de la stratégie de rétention est affiché dans la propriété *InPlaceHolds* de la boîte aux lettres de l'utilisateur lorsque vous exécutez la cmdlet **Get-Mailbox** ; elle est identifiée par le `-mbx`préfixe; par exemple,`-mbxe9b52bf7ab3b46a286308ecb29624696` <br/> |
|conservation des cas eDiscovery dans le centre de sécurité & Compliance Center  <br/> | `UniH7d895d48-7e23-4a8d-8346-533c3beac15d` <br/> |La propriété *InPlaceHolds* contient également le GUID de n'importe quelle conservation associée à un cas eDiscovery dans le centre de sécurité _AMP_ Compliance Center pouvant être placé sur la boîte aux lettres. Vous pouvez déterminer qu'il s'agit d'une mise en conservation de cas eDiscovery, car le GUID commence par le préfixe  `UniH`.  <br/> Vous pouvez utiliser l' `Get-CaseHoldPolicy` applet de commande dans Security _AMP_ Compliance Center PowerShell pour obtenir des informations sur le cas eDiscovery auquel est associée la conservation de la boîte aux lettres. Par exemple, vous pouvez exécuter la commande `Get-CaseHoldPolicy <hold GUID without prefix> | FL Name` pour afficher le nom du blocage de la boîte aux lettres qui se trouve sur la boîte aux lettres. Be sure to remove the  `UniH` lorsque vous exécutez cette commande.  <br/><br/> Pour identifier le cas eDiscovery auquel est associée la conservation de la boîte aux lettres, exécutez les commandes suivantes:<br/><br/>`$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>`<br/><br/>`Get-ComplianceCase $CaseHold.CaseId | FL Name`


