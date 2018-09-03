---
title: Augmenter le quota des éléments récupérables pour les boîtes aux lettres placées en conservation
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 8/22/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a8bdcbdd-9298-462f-b889-df26037a990c
description: 'Activer la boîte aux lettres d’archive et activer l’archivage pour augmenter la taille du dossier éléments récupérables pour une boîte aux lettres dans Office 365 développer automatiquement. '
ms.openlocfilehash: cd2d07e6ef1637343798ccb71870c8d436f10574
ms.sourcegitcommit: e7b87fae103a858981bdbcdf7ec55afa4751ad05
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2018
ms.locfileid: "23782091"
---
# <a name="increase-the-recoverable-items-quota-for-mailboxes-on-hold"></a>Augmenter le quota des éléments récupérables pour les boîtes aux lettres placées en conservation

La stratégie de rétention par défaut, appelée stratégie MRM par défaut, qui est appliquées automatiquement vers les nouvelles boîtes aux lettres dans Exchange Online contient une balise de rétention nommé récupérables éléments 14 jours déplacement vers l’archive. Cette balise de rétention déplace les éléments à partir du dossier éléments récupérables dans la boîte aux lettres principale de l’utilisateur dans le dossier éléments récupérables dans la boîte aux lettres de l’utilisateur archive l’expiration de la période de rétention de 14 jours pour un élément. Pour ce faire, la boîte aux lettres de l’utilisateur archive doit être activé. Si la boîte aux lettres d’archivage n’est pas activé, aucune action, ce qui signifie que les éléments dans les éléments récupérables blocage du dossier à une boîte aux lettres ne sont pas déplacés vers la boîte aux lettres d’archivage après expiration de la période de rétention de 14 jours. Rien n’est supprimé à partir d’une boîte aux lettres en attente, il est possible que le quota de stockage pour le dossier éléments récupérables peut être dépassé, surtout si la boîte aux lettres de l’utilisateur archive n’est pas activé. 
  
Pour réduire le risque de dépassement de cette limite, le quota de stockage pour le dossier éléments récupérables est automatiquement augmenté de 30 Go à 100 Go lors d’une suspension est placée dans une boîte aux lettres dans Exchange Online. Si la boîte aux lettres d’archive est activé, le quota de stockage pour le dossier éléments récupérables dans la boîte aux lettres d’archive est également passent de 30 Go à 100 Go. Si l’archivage automatique-développement des fonctionnalités dans Exchange Online est activé, le quota de stockage pour le dossier éléments récupérables dans l’archive de l’utilisateur sera illimité.
  
  Le tableau suivant résume le quota de stockage pour le dossier Éléments récupérables. 
  
|**Emplacement du dossier Éléments récupérables**|**Boîtes aux lettres non placées en conservation**|**Boîtes aux lettres placées en conservation**|
|:-----|:-----|:-----|
|Boîte aux lettres principale  <br/> |30 Go  <br/> |100 Go  <br/> |
|Boîte aux lettres d’archive<sup>\*</sup> <br/> |Illimité  <br/> |Illimité  <br/> |
|**Quota de stockage total pour le dossier Éléments récupérables** <br/> |Illimité  <br/> |Illimité  <br/> |
   
> [!NOTE]
> <sup>\*</sup>Quota de stockage initial de la boîte aux lettres d’archive est de 100 Go pour les utilisateurs disposant d’une licence Exchange Online (Plan 2). Toutefois, lorsque développer automatiquement l’archivage est activée pour les boîtes aux lettres en attente, le quota de stockage pour les deux la la boîte aux lettres d’archivage et le dossier éléments récupérables est augmentée à 110 Go. Espace de stockage d’archive supplémentaires système mis en service lorsque cela est nécessaire ce qui génère un nombre illimité de stockage d’archives. Pour plus d’informations sur l’extension automatique d’archivage, consultez la rubrique [vue d’ensemble de l’archivage illimité dans Office 365](unlimited-archiving.md). 
  
Lorsque le quota de stockage pour le dossier Éléments récupérables dans la boîte aux lettres principale d’une boîte aux lettres placée en conservation est proche de sa limite, vous pouvez effectuer les opérations suivantes :
  
- **Activer la boîte aux lettres d’archivage et d’activer l’archivage automatique-développement** - vous pouvez activer une capacité de stockage illimitée pour le dossier éléments récupérables simplement par l’activation de la boîte aux lettres d’archive et puis activer la fonctionnalité d’archivage automatique-développement dans Exchange En ligne. Le résultat 110 Go pour le dossier éléments récupérables dans la boîte aux lettres principale et un nombre illimité de capacité de stockage pour le dossier éléments récupérables dans l’archive de l’utilisateur. Voir comment : [Activer les boîtes aux lettres archive de sécurité Office 365 &amp; centre de conformité](enable-archive-mailboxes.md) et [Activer l’archivage illimité dans Office 365](enable-unlimited-archiving.md).
    
    > [!NOTE]
    > Après avoir activé l’archivage pour une boîte aux lettres qui est proche dépassant le quota de stockage pour le dossier éléments récupérables, vous voudrez peut-être exécuter l’Assistant dossier géré pour déclencher manuellement l’assistant pour traiter la boîte aux lettres afin que les éléments arrivés à expiration sont déplacés le Dossier éléments récupérables dans la boîte aux lettres d’archive. Pour plus d’informations, voir [l’étape 4](#optional-step-4-run-the-managed-folder-assistant-to-apply-the-new-retention-settings) . Notez que les autres éléments de boîte aux lettres de l’utilisateur peuvent être déplacés vers la nouvelle boîte aux lettres d’archive. Prendre en compte pour présenter à l’utilisateur que cela peut se produire après l’activation de la boîte aux lettres d’archive. 
  
- **Créer une stratégie de rétention personnalisée pour les boîtes aux lettres sur Maintenez** - outre l’activation de la boîte aux lettres d’archive et développer automatiquement l’archivage pour les boîtes aux lettres sur un litige ou blocage sur Place, vous pourriez également créer une stratégie de rétention personnalisée pour les boîtes aux lettres sur mettre en attente. Cela nous allons vous appliquer une stratégie de rétention aux boîtes aux lettres en attente qui diffère de la stratégie MRM par défaut qui est appliqué aux boîtes aux lettres qui ne sont pas en attente. Cela vous permet pour appliquer des balises de rétention sont spécialement conçues pour les boîtes aux lettres en attente. Cela comprend la création d’une nouvelle balise de rétention du dossier éléments récupérables. 
    
Le reste de cette rubrique décrit les procédures détaillées de création d’une stratégie de rétention personnalisée pour les boîtes aux lettres placées en conservation.
  
[Étape 1 : Création d’une balise de rétention pour le dossier Éléments récupérables](#step-1-create-a-custom-retention-tag-for-the-recoverable-items-folder)

[[Étape 2 : créer une nouvelle stratégie de rétention des boîtes aux lettres en attente](#step-2-create-a-new-retention-policy-for-mailboxes-on-hold)

[Étape 3 : Application de la nouvelle stratégie de rétention aux boîtes aux lettres placées en conservation](#step-3-apply-the-new-retention-policy-to-mailboxes-on-hold)

[(Facultatif) Étape 4 : Exécution de l’Assistant Dossier géré pour appliquer les nouveaux paramètres de rétention](#optional-step-4-run-the-managed-folder-assistant-to-apply-the-new-retention-settings)
  
## <a name="step-1-create-a-custom-retention-tag-for-the-recoverable-items-folder"></a>Étape 1 : Création d’une balise de rétention personnalisée pour le dossier Éléments récupérables

La première étape consiste à créer une balise de rétention personnalisée (appelée balise de stratégie de rétention ou RPT) pour le dossier éléments récupérables. Comme expliqué précédemment, ce rapport déplace les éléments à partir du dossier éléments récupérables dans la boîte aux lettres principale de l’utilisateur dans le dossier éléments récupérables dans la boîte aux lettres de l’utilisateur archive. Vous devez utiliser PowerShell pour créer un rapport pour le dossier éléments récupérables. Vous ne pouvez pas utiliser le centre d’administration Exchange (CAE). 
  
1. [Connect to Exchange Online using remote PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=517283)
    
2. Exécutez la commande suivante pour créer une balise de stratégie de rétention pour le dossier Éléments récupérables :  
    
    ```
    New-RetentionPolicyTag -Name <Name of RPT> -Type RecoverableItems -AgeLimitForRetention <Number of days> -RetentionAction MoveToArchive
    ```

    Par exemple, la commande suivante crée une balise de stratégie de rétention pour le dossier Éléments récupérables nommée « Éléments récupérables 30 jours pour les boîtes aux lettres en conservation », avec une période de rétention de 30 jours. Cela signifie que 30 jours après qu’un élément a été placé dans le dossier Éléments récupérables, il est déplacé vers le dossier Éléments récupérables de la boîte aux lettres d’archivage de l’utilisateur.
    
    ```
    New-RetentionPolicyTag -Name "Recoverable Items 30 days for mailboxes on hold" -Type RecoverableItems -AgeLimitForRetention 30 -RetentionAction MoveToArchive
    ```

    > [!TIP]
    > Il est recommandé que la période de rétention (définie par le paramètre _AgeLimitForRetention_ ) pour le rapport éléments récupérables est la même que la période de rétention des éléments supprimés pour les boîtes aux lettres qui est appliquée à l’arborescence RPT. Cela permet à un utilisateur la période de rétention des éléments supprimés ensemble pour récupérer des éléments supprimés avant qu’ils sont déplacés vers la boîte aux lettres d’archive. Dans l’exemple précédent, la période de rétention a été définie sur 30 jours basés sur l’hypothèse que la période de rétention des éléments supprimés pour les boîtes aux lettres est également de 30 jours. Une boîte aux lettres Exchange Online est configuré pour conserver les éléments supprimés pendant 14 jours par défaut. Mais vous pouvez modifier ce paramètre pour un maximum de 30 jours. Pour plus d’informations, voir [Modifier la période de rétention des éléments supprimés pour une boîte aux lettres dans Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=286940). 
  
## <a name="step-2-create-a-new-retention-policy-for-mailboxes-on-hold"></a>Étape 2 : Création d’une stratégie de rétention pour les boîtes aux lettres placées en conservation

L’étape suivante consiste à créer une stratégie de rétention et à lui ajouter des balises de rétention, y compris la balise de stratégie de rétention des éléments récupérables que vous avez créée à l’étape 1. Cette nouvelle stratégie sera appliquée aux boîtes aux lettres placées en conservation dans l’étape suivante.  
  
Avant de créer la stratégie de rétention, déterminez les balises de rétention supplémentaires que vous souhaitez ajouter. Pour obtenir une liste des balises de rétention qui sont ajoutées à la stratégie MRM par défaut et pour plus d’informations sur la création des balises de rétention, voir les rubriques suivantes :
  
- [Valeur par défaut de la stratégie de rétention dans Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=746954)
    
- [Dossiers par défaut prenant en charge les balises de stratégie de rétention](https://go.microsoft.com/fwlink/p/?LinkId=746957)
    
- La section « Créer une balise de rétention » dans la rubrique [créer une stratégie de rétention](https://go.microsoft.com/fwlink/p/?LinkId=404422) .
    
Vous pouvez utiliser le centre d’administration Exchange ou Exchange Online PowerShell pour créer une stratégie de rétention.
  
### <a name="use-the-eac-to-create-a-retention-policy"></a>Utilisation du Centre d'administration Exchange pour créer une stratégie de rétention
  
1. Dans le CAE, accédez à **gestion de la conformité** \> de **stratégies de rétention**, puis cliquez sur **Ajouter** ![ajouter une icône](media/ITPro-EAC-AddIcon.gif).
    
2. Sur la page **Nouvelle stratégie de rétention**, sous **Nom**, saisissez un nom qui décrit l’objectif de la stratégie de rétention ; par exemple, **MRM Policy for Mailboxes on Hold**.  
    
3. Sous **les balises de rétention**, cliquez sur **Ajouter** ![ajouter une icône](media/ITPro-EAC-AddIcon.gif).
    
4. Dans la liste des balises de rétention, sélectionnez la balise de stratégie de rétention des éléments récupérables que vous avez créée à l’étape 1, puis cliquez sur **Ajouter**.
    
    ![Sélectionnez la balise de rétention Éléments récupérables personnalisée](media/eb49866b-bdef-4fcd-a6d9-01607c01249b.png)
  
5. Sélectionnez des balises de rétention supplémentaires à ajouter à la stratégie de rétention. Par exemple, vous pouvez ajouter les mêmes balises qui sont incluses dans la stratégie MRM par défaut.
    
6. Lorsque vous avez fini d’ajouter les balises de rétention, cliquez sur **OK**.
    
7. Cliquez sur **Enregistrer** pour créer la stratégie de rétention. 
    
    Les balises de rétention liées à la stratégie de rétention sont affichées dans le volet de détails.
    
    ![Des balises de conservation liées à la stratégie de rétention sont affichées dans le volet de détails](media/dad1c8f4-9928-4d6d-991a-6f6c5194eceb.png)
  
### <a name="use-exchange-online-powershell-to-create-a-retention-policy"></a>Utiliser Exchange Online PowerShell pour créer une stratégie de rétention
  
Exécutez la commande suivante pour créer une stratégie de rétention pour les boîtes aux lettres placées en conservation.  
  
```
New-RetentionPolicy <Name of retention policy>  -RetentionPolicyTagLinks <list of retention tags>

```

Par exemple, la commande suivante crée la stratégie de rétention et les balises de rétention liées qui sont présentées dans l’illustration précédente.
  
```
New-RetentionPolicy "MRM Policy for Mailboxes on Hold"  -RetentionPolicyTagLinks "Recoverable Items 30 days for mailboxes on hold","1 Month Delete","1 Week Delete","1 Year Delete","5 Year Delete","6 Month Delete","Default 2 year move to archive","Junk Email","Never Delete","Personal 1 year move to archive","Personal 5 year move to archive"
```
  
## <a name="step-3-apply-the-new-retention-policy-to-mailboxes-on-hold"></a>Étape 3 : Application de la nouvelle stratégie de rétention aux boîtes aux lettres placées en conservation

La dernière étape consiste à appliquer la nouvelle stratégie de rétention que vous avez créé à l’étape 2 pour les boîtes aux lettres en attente dans votre organisation. Vous pouvez utiliser le centre d’administration Exchange ou Exchange Online PowerShell pour appliquer la stratégie de rétention à une boîte aux lettres unique ou à plusieurs boîtes aux lettres. 
  
### <a name="use-the-eac-to-apply-the-new-retention-policy"></a>Utilisation du Centre d’administration Exchange pour appliquer la nouvelle stratégie de rétention
  
1. Accédez à **Destinataires**\> **Boîtes aux lettres**.
    
2. Dans la liste affichée, sélectionnez la boîte aux lettres que vous voulez appliquer la stratégie de rétention à, puis cliquez sur **Modifier** ![icône Modifier](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).
    
3. Sur la page **Boîte aux lettres de l’utilisateur**, cliquez sur **Fonctionnalités de boîte aux lettres**.
    
4. Sous **Stratégie de rétention**, sélectionnez la stratégie de rétention que vous avez créée à l’étape 2, puis cliquez sur **Enregistrer**.
    
Vous pouvez aussi utiliser le Centre d’administration Exchange pour appliquer la stratégie de rétention à plusieurs boîtes aux lettres.
  
1. Accédez à **Destinataires**\> **Boîtes aux lettres**.
    
2. Dans la liste affichée, utilisez les touches Maj ou Ctrl pour sélectionner plusieurs boîtes aux lettres.
    
3. Dans le volet d'informations, cliquez sur **Plus d'options**.
    
4. Sous **Stratégie de rétention**, cliquez sur **Mettre à jour**.
    
5. Sur la page **Attribuer la stratégie de rétention en bloc**, sélectionnez la stratégie de rétention que vous avez créée à l’étape 2, puis cliquez sur **Enregistrer**.  
    
### <a name="use-exchange-online-powershell-to-apply-the-new-retention-policy"></a>Utiliser Exchange Online PowerShell pour appliquer la nouvelle stratégie de rétention
  
Vous pouvez utiliser Exchange Online PowerShell pour appliquer une nouvelle stratégie de rétention à une seule boîte aux lettres. Mais la puissance de PowerShell est que vous pouvez l’utiliser pour identifier rapidement toutes les boîtes aux lettres dans votre organisation qui sont en attente pour litige ou blocage sur Place, puis appliquent la nouvelle stratégie de rétention à toutes les boîtes aux lettres sur blocage dans une seule commande. Voici quelques exemples d’utilisation de PowerShell Exchange pour appliquer une stratégie de rétention à une ou plusieurs boîtes aux lettres. Tous les exemples appliquent la stratégie de rétention qui a été créée à l’étape 2.
  
Cet exemple applique la nouvelle stratégie de rétention à la boîte aux lettres de Pilar Pinilla.
  
```
Set-Mailbox "Pilar Pinilla" -RetentionPolicy "MRM Policy for Mailboxes on Hold"
```

Cet exemple applique la nouvelle stratégie de rétention à toutes les boîtes aux lettres de l’organisation qui sont placées en conservation pour litige.
  
```
$LitigationHolds = Get-Mailbox -ResultSize unlimited | Where-Object {$_.LitigationHoldEnabled -eq 'True'}
```

```
$LitigationHolds.DistinguishedName | Set-Mailbox -RetentionPolicy "MRM Policy for Mailboxes on Hold"
```

Cet exemple applique la nouvelle stratégie de rétention à toutes les boîtes aux lettres de l’organisation qui sont placées en conservation inaltérable.
  
```
$InPlaceHolds = Get-Mailbox -ResultSize unlimited | Where-Object {$_.InPlaceHolds -ne $null}
```

```
$InPlaceHolds.DistinguishedName | Set-Mailbox -RetentionPolicy "MRM Policy for Mailboxes on Hold"
```

Vous pouvez utiliser la cmdlet **Get-Mailbox** pour vérifier que la nouvelle stratégie de rétention a été appliquée. 
  
Voici quelques exemples pour vérifier que les commandes des exemples précédents appliquent la stratégie de rétention « stratégie MRM pour les boîtes aux lettres en conservation » aux boîtes aux lettres placées en conservation sur litige et aux boîtes aux lettres en conservation inaltérable.
  
```
Get-Mailbox "Pilar Pinilla" | Select RetentionPolicy
```

```
Get-Mailbox -ResultSize unlimited | Where-Object {$_.LitigationHoldEnabled -eq 'True'} | FT DisplayName,RetentionPolicy -Auto
```

```
Get-Mailbox -ResultSize unlimited | Where-Object {$_.InPlaceHolds -ne $null} | FT DisplayName,RetentionPolicy -Auto
```
  
## <a name="optional-step-4-run-the-managed-folder-assistant-to-apply-the-new-retention-settings"></a>(Facultatif) Étape 4 : Exécution de l’Assistant Dossier géré pour appliquer les nouveaux paramètres de rétention

Après avoir appliqué la nouvelle stratégie de rétention aux boîtes aux lettres en attente, il peut prendre jusqu'à sept jours dans Exchange Online pour l’Assistant dossier géré à traiter ces boîtes aux lettres en utilisant les paramètres de la nouvelle stratégie de rétention. Au lieu d’attendre exécuter l’Assistant dossier géré, vous pouvez utiliser l’applet de commande **Start-ManagedFolderAssistant** pour déclencher manuellement l’assistant pour traiter les boîtes aux lettres que vous avez appliqué à la nouvelle stratégie de rétention. 
  
Exécutez la commande suivante pour démarrer l’Assistant Dossier géré pour la boîte aux lettres de Pilar Pinilla.
  
```
Start-ManagedFolderAssistant "Pilar Pinilla"
```

Exécutez les commandes suivantes pour démarrer l’Assistant Dossier géré pour toutes les boîtes aux lettres placées en conservation.
  
```
$MailboxesOnHold = Get-Mailbox -ResultSize unlimited | Where-Object {($_.InPlaceHolds -ne $null) -or ($_.LitigationHoldEnabled -eq "True")}
```

```
$MailboxesOnHold.DistinguishedName | Start-ManagedFolderAssistant
```

## <a name="more-information"></a>Plus d'informations

- Une fois que la boîte aux lettres de l’utilisateur archive, prenez en compte pour présenter à l’utilisateur que les autres éléments dans leur boîte aux lettres (pas seulement les éléments dans le dossier éléments récupérables) peuvent être déplacés vers la boîte aux lettres d’archive. Il s’agit, car la stratégie MRM par défaut qui est affecté à des boîtes aux lettres Exchange Online contient une balise de rétention (nommé par défaut de 2 ans à déplacer vers l’archive) qui déplace les éléments dans la boîte aux lettres d’archive deux ans après la date de l’élément a été remis à la boîte aux lettres ou créé par le utilisateur. Pour plus d’informations, voir [Stratégie de rétention par défaut dans Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=746954)
    
- Une fois que la boîte aux lettres de l’utilisateur archive, vous pourrez également indiquer à l’utilisateur qu’ils peuvent récupérer les éléments supprimés dans le dossier éléments récupérables dans leur boîte aux lettres d’archive. Cela dans Outlook en sélectionnant le dossier **Éléments supprimés** dans la boîte aux lettres d’archivage, puis en cliquant sur **Récupérer les éléments supprimés de serveur** sous l’onglet **accueil** . Pour plus d’informations sur la récupération des éléments supprimés, consultez la rubrique [récupérer les éléments supprimés dans Outlook pour Windows](https://go.microsoft.com/fwlink/p/?LinkId=624829). 
