---
title: Activer l’audit de boîte aux lettres dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/19/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: aaca8987-5b62-458b-9882-c28476a66918
description: Dans Office 365, vous pouvez activer l’enregistrement d’audit boîte aux lettres pour enregistrer l’accès des boîtes aux lettres par les propriétaires de boîte aux lettres, les délégués et les administrateurs. Par défaut, l’audit de boîte aux lettres dans Office 365 n’est pas activé. Une fois que la boîte aux lettres enregistrement d’audit pour une boîte aux lettres, vous pouvez rechercher le journal d’audit de Office 365 pour les activités effectuées sur la boîte aux lettres.
ms.openlocfilehash: a31a96c8c5c65965746a3a31bc924731289795f0
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527928"
---
# <a name="enable-mailbox-auditing-in-office-365"></a>Activer l’audit de boîte aux lettres dans Office 365
  
Dans Office 365, vous pouvez activer l’enregistrement d’audit boîte aux lettres pour enregistrer l’accès des boîtes aux lettres par les propriétaires de boîte aux lettres, les délégués et les administrateurs. Par défaut, l’audit de boîte aux lettres dans Office 365 n’est pas activé. Cela signifie que la boîte aux lettres de l’audit des événements n’apparaisse pas dans les résultats lorsque vous recherchez le journal d’audit de Office 365 pour l’activité de la boîte aux lettres. Mais après l’activation de la boîte aux lettres enregistrement d’audit pour une boîte aux lettres utilisateur, vous pouvez rechercher le journal d’audit pour l’activité de la boîte aux lettres. En outre, lors de l’audit de boîte aux lettres de journalisation est activée, certaines actions effectuées par les administrateurs, les délégués, et propriétaires sont consignées par défaut. Pour ouvrir une session (et recherchez) actions supplémentaires, consultez l’étape 3.

## <a name="before-you-begin"></a>Avant de commencer
  
- Vous devez utiliser Exchange Online PowerShell pour activer la boîte aux lettres de journal d’audit. Vous ne pouvez pas utiliser le Office 365 Security &amp; centre de conformité ou le centre d’administration Exchange.
    
- Une fois que la boîte aux lettres enregistrement d’audit pour une boîte aux lettres, accès aux boîtes aux lettres et certains admin et délégué actions sont enregistrés par défaut. Pour enregistrer les actions effectuées par le propriétaire de boîte aux lettres, vous devez spécifier les actions de propriétaire à auditer. Consultez la section « Informations supplémentaires » pour voir une liste des actions qui sont enregistrés après l’enregistrement d’audit de boîte aux lettres est activée, et les actions qui sont disponibles pour chaque type d’ouverture de session utilisateur.
    
- Vous ne pouvez pas activer la boîte aux lettres enregistrement d’audit pour la boîte aux lettres qui est associé à un groupe d’Office 365 ou d’une équipe dans Microsoft Teams.
    
- Un administrateur disposant de l'autorisation Accès complet sur la boîte aux lettres d'un utilisateur est considéré comme un utilisateur délégué.
  
## <a name="step-1-connect-to-exchange-online-powershell"></a>Étape 1 : Connexion à Exchange Online PowerShell

1. Sur votre ordinateur local, ouvrez Windows PowerShell et exécutez la commande suivante.
   
    ```
    $UserCredential = Get-Credential
    ```

2. Dans la boîte de dialogue **Demande d'informations d'identification Windows PowerShell**, saisissez le nom d'utilisateur et le mot de passe d'un compte d'administrateur global Office 365, puis cliquez sur **OK**.
    
3. Exécutez la commande suivante :
    
    ```
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://outlook.office365.com/powershell-liveid/ -Credential $UserCredential -Authentication Basic -AllowRedirection
    ```

3. Exécutez la commande suivante.

    ```
    Import-PSSession $Session
    ```
   
4. Pour vérifier que vous êtes connecté à votre organisation Exchange Online, exécutez la commande suivante pour obtenir la liste de toutes les boîtes aux lettres de votre organisation.
    
    ```
    Get-Mailbox
    ```
  
Pour plus d'informations ou si vous rencontrez des problèmes pour vous connecter à votre organisation Exchange Online, consultez la rubrique [Connexion à Exchange Online à l'aide de Remote PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=517283).
  
## <a name="step-2-enable-mailbox-audit-logging"></a>Étape 2 : activation de la journalisation d’audit de boîte aux lettres

Une fois que vous vous connectez à votre organisation Exchange Online, utiliser PowerShell pour activer la boîte aux lettres enregistrement d’audit pour une boîte aux lettres. Vous pouvez également activer l’audit de boîte aux lettres pour toutes les boîtes aux lettres dans votre organisation.
  
Cet exemple active l’enregistrement de boîte aux lettres de Pilar Pinilla d’audit des boîtes aux lettres.
  
```
Set-Mailbox -Identity "Pilar Pinilla" -AuditEnabled $true
```

Dans cet exemple, la journalisation d'audit est activée pour toutes les boîtes aux lettres d'utilisateur de votre organisation.
  
```
Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | Set-Mailbox -AuditEnabled $true
```
  
## <a name="step-3-specify-owner-actions-to-audit"></a>Étape 3 : indication des actions de propriétaire à auditer

Lorsque vous activez l’audit pour une boîte aux lettres, une seule action ( **UpdateFolderPermissions** ) effectuée par le propriétaire de boîte aux lettres est enregistrée par défaut. Vous devez spécifier d’autres actions propriétaire à auditer. Consultez le tableau dans la section « Actions de boîte aux lettres » pour une liste et une description des actions propriétaire pouvant être audités. 
  
Cet exemple ajoute les actions de propriétaire **MailboxLogin** et **HardDelete** à la boîte aux lettres de l’audit de boîte aux lettres de Pilar Pinilla. Cet exemple suppose que l’audit de boîte aux lettres a déjà été activé pour cette boîte aux lettres. 

```
Set-Mailbox "Pilar Pinilla" -AuditOwner @{Add="MailboxLogin","HardDelete"}
```

Cet exemple permet d’audit de boîte aux lettres enregistrement de boîte aux lettres de Don Hall et spécifie que seule l’action **MailboxLogin** effectuée par le propriétaire de boîte aux lettres sera consignée. Notez que cet exemple remplace l’action de UpdateFolderPermissions par défaut. 
  
```
Set-Mailbox "Don Hall" -AuditEnabled $true -AuditOwner MailboxLogin
```
   
Cet exemple ajoute les actions de propriétaire **SoftDelete** , **HardDelete**et **MailboxLogin**à toutes les boîtes aux lettres dans l’organisation. Cet exemple suppose que l’audit de boîte aux lettres a déjà été activé pour toutes les boîtes aux lettres. 
  
```
Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | Set-Mailbox -AuditOwner @{Add="MailboxLogin","HardDelete","SoftDelete"}
```
  
## <a name="how-do-you-know-this-worked"></a>Comment savoir si cela a fonctionné ?

Pour vérifier que vous avez activé la journalisation d’audit de boîte aux lettres pour une boîte aux lettres donnée, utilisez la cmdlet **Get-Mailbox** pour récupérer les paramètres d’audit de cette boîte aux lettres. 
  
Dans cet exemple, les paramètres d’audit sont récupérés pour Pilar Pinilla.

```
Get-Mailbox "Pilar Pinilla"| FL Audit*
```
   
Dans cet exemple, les paramètres d’audit sont récupérés pour toutes les boîtes aux lettres d’utilisateur de votre organisation.

```
Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | FL Name,Audit*
```
   
Une valeur **true** pour la propriété **AuditEnabled** vérifie que d’audit de boîte aux lettres la journalisation est activée. 
    
## <a name="mailbox-auditing-actions"></a>Actions d’audit de boîte aux lettres
  
Le tableau suivant répertorie les actions qui peuvent être enregistrées par boîte aux lettres de journal d’audit. Le tableau inclut l’action qui peut être enregistrée pour les types d’ouverture de session utilisateur différent. Dans le tableau, un **No** indique qu’une action ne peut pas être enregistrée pour ce type d’ouverture de session. Un astérisque ( **\*** ) indique que l’action est consignée par défaut lors de l’enregistrement d’audit de boîte aux lettres est activée pour la boîte aux lettres. Comme indiqué précédemment, l’action seuls le propriétaire enregistrée par défaut lorsque vous activez l’audit de boîte aux lettres est UpdateFolderPermissions. Pour enregistrer les autres actions effectuées par le propriétaire de boîte aux lettres, vous devez spécifier les actions supplémentaires propriétaire à auditer. Pour ce faire, consultez [l’étape 3](#step-3-specify-owner-actions-to-audit) dans cette rubrique. 
  
|**Action**|**Description**|**Administrateur**|**Délégué\*\*\***|**Propriétaire**|
|:-----|:-----|:-----|:-----|:-----|
|**Copier** <br/> |Un message a été copié dans un autre dossier.  <br/> |Oui  <br/> |Non  <br/> |Non  <br/> |
|**Create** <br/> |Un élément est créé dans le dossier calendrier, Contacts, Notes ou les tâches dans la boîte aux lettres ; par exemple, une demande de réunion est créée. Notez que la création, l’envoi ou la réception d’un message n’est pas audités. En outre, la création d’un dossier de boîte aux lettres n’est pas analysé.  <br/> |Oui\*  <br/> |Oui\*  <br/> |Oui  <br/> |
|**FolderBind** <br/> |Un utilisateur a accédé au dossier de boîte aux lettres. Cette action est également enregistrée lorsque l’administrateur ou un délégué ouvre la boîte aux lettres.  <br/> |Oui\*  <br/> |Oui\*\*  <br/> |Non  <br/> |
|**HardDelete** <br/> |Un message a été purgé du dossier Éléments récupérables.  <br/> |Oui\*  <br/> |Oui\*  <br/> |Oui  <br/> |
|**MailboxLogin** <br/> |L'utilisateur s'est connecté à sa boîte aux lettres.  <br/> |Non  <br/> |Non  <br/> |Oui  <br/> |
|**Messagebind ne** <br/> |Un message a été affiché dans le volet de visualisation ou ouvert.  <br/> |Oui  <br/> |Non  <br/> |Non  <br/> |
|**Déplacer** <br/> |Un message a été déplacé vers un autre dossier.  <br/> |Oui\*  <br/> |Oui  <br/> |Oui  <br/> |
|**MoveToDeletedItems** <br/> |Un message a été supprimé et déplacé vers le dossier Éléments supprimés.  <br/> |Oui\*  <br/> |Oui  <br/> |Oui  <br/> |
|**SendAs** <br/> |Un message a été envoyé à l’aide de l’autorisation SendAs. Cela signifie qu’un autre utilisateur a envoyé le message comme s’il provenait du propriétaire de la boîte aux lettres.  <br/> |Oui\*  <br/> |Oui\*  <br/> |Non  <br/> |
|**SendOnBehalf** <br/> |Un message a été envoyé à l’aide de l’autorisation SendOnBehalf. Cela signifie qu’un autre utilisateur a envoyé le message de la part du propriétaire de la boîte aux lettres. Le message indique au destinataire de la part de qui le message a été envoyé et qui a envoyé réellement le message.  <br/> |Oui\*  <br/> |Oui  <br/> |Non  <br/> |
|**SoftDelete** <br/> |Un message a été définitivement supprimé ou supprimé (récupérable) du dossier Éléments supprimés. Les éléments supprimés récupérables sont déplacés vers le dossier Éléments récupérables.  <br/> |Oui\*  <br/> |Oui\*  <br/> |Oui  <br/> |
|**Mettre à jour** <br/> |Un message ou ses propriétés ont été modifiés.  <br/> |Oui\*  <br/> |Oui\*  <br/> |Oui  <br/> |
|**UpdateCalendarDelegation** <br/> |Une délégation de calendrier a été affectée à une boîte aux lettres. La délégation de calendrier donne à quelqu'un d’autre dans les mêmes autorisations d’organisation pour gérer le calendrier du propriétaire de la boîte aux lettres.  <br/> |Oui\*  <br/> |Non  <br/> |Oui\*  <br/> |
|**UpdateFolderPermissions** <br/> |Une autorisation de dossier a été modifiée. Contrôle des autorisations dossier les utilisateurs de votre organisation peuvent accéder aux dossiers dans une boîte aux lettres et les messages situés dans les dossiers.  <br/> |Oui\*  <br/> |Oui\*  <br/> |Oui\*  <br/> |
|**UpdateInboxRules** <br/> |Une règle de boîte de réception a été ajoutée, supprimée ou modifiée. Règles de boîte de réception sont utilisés pour traiter les messages dans la boîte de réception en fonction de conditions spécifiées et prennent les mesures lorsque les conditions d’une règle sont remplies, telles que le déplacement d’un message dans un dossier spécifié ou suppression d’un message.  <br/> |Oui\*  <br/> |Oui\*  <br/> |Oui\*  <br/> |
   
> [!NOTE]
> <sup>\*</sup>Enregistré par défaut si l’audit est activé pour une boîte aux lettres. > <sup> \* </sup> Entrées pour les actions de lier dossier effectuées par les délégués sont consolidées. Une entrée de journal est générée pour l’accès à un dossier spécifique dans une période de 24 heures. > <sup> \* \* </sup> Un administrateur qui a été attribué l’autorisation accès total aux boîtes aux lettres d’un utilisateur est considéré comme un utilisateur délégué. 
  
Si vous avez besoin n’est plus certains types d’actions de boîte aux lettres à auditer, vous devez modifier la configuration de journalisation d’audit de la boîte aux lettres pour désactiver ces actions. Les entrées existantes ne sont pas supprimées jusqu'à ce que la limite d’âge de 90 jours pour les entrées du journal d’audit est atteint.
  
## <a name="more-infotab"></a>[Informations supplémentaires](#tab/)
  
- Utilisez le journal d’audit de Office 365 pour rechercher des activités de boîte aux lettres qui ont été enregistrés. Vous pouvez rechercher activité pour une boîte aux lettres d’utilisateur spécifique. La capture d’écran suivante affiche la liste des activités de boîte aux lettres que vous pouvez rechercher dans le journal d’audit d’Office 365. Notez que ces activités sont les mêmes actions qui sont décrites dans la section « Actions l’audit des boîtes aux lettres » dans cette rubrique.
    
    ![Vous pouvez rechercher le journal d’audit de Office 365 pour les actions d’audit de boîte aux lettres en sélectionnant « Échanger des activités de la boîte aux lettres » dans la liste déroulante des activités](media/fadc34f8-9de2-4688-8b1a-bc5540e69a23.png)
  
    Le tableau suivant décrit chaque activité de boîte aux lettres que vous pouvez rechercher et indique l’action d’audit de boîte aux lettres correspondante.
    
    |**Activités dans le journal d’audit**|**Action d’audit de boîte aux lettres**|
    |:-----|:-----|
    |Élément de boîte aux lettres créée  <br/> |Create  <br/> |
    |Messages copiés dans un autre dossier  <br/> |Copy  <br/> |
    |Utilisateur connecté à la boîte aux lettres  <br/> |MailboxLogin  <br/> |
    |Envoyé à l’aide des autorisations Envoyer de la part de message  <br/> |SendOnBehalf  <br/> |
    |Messages purgés à partir de la boîte aux lettres  <br/> |HardDelete  <br/> |
    |Déplacer des messages vers le dossier éléments supprimés  <br/> |MoveToDeletedItems  <br/> |
    |Déplacer des messages vers un autre dossier  <br/> |Move  <br/> |
    |Envoyé le message à l’aide des autorisations Envoyer en tant que  <br/> |SendAs  <br/> |
    |Message mis à jour  <br/> |Update  <br/> |
    |Messages supprimés du dossier éléments supprimés  <br/> |SoftDelete  <br/> |
    |Ajout d’autorisations au dossier  <br/> |UpdateFolderPermissions  <br/> |
    |Modification des autorisations du dossier  <br/> |UpdateFolderPermissions  <br/> |
    |Autorisations supprimées du dossier  <br/> |UpdateFolderPermissions  <br/> |
    |Utilisateur ajouté ou supprimé avec l’accès délégué au dossier de calendrier  <br/> |UpdateCalendarDelegation  <br/> |
   
    Notez que les activités de **déléguer des autorisations de boîte aux lettres Ajout** et **suppression déléguer des autorisations de boîte aux lettres** indiquées dans la capture d’écran précédente ne sont pas liées à la boîte aux lettres de l’audit des actions. Ils indiquent si un administrateur affecté ou supprimé de l’autorisation de boîte aux lettres FullAccess. 
    
    Pour plus d’informations sur le journal d’audit de Office 365, voir [recherche dans le journal d’audit de sécurité Office 365 &amp; centre de conformité](search-the-audit-log-in-security-and-compliance.md).
    
- On considère qu'un administrateur accède aux boîtes aux lettres uniquement dans les cas suivants :
    
  - Découverte électronique inaltérable dans Exchange Online ou de recherche de contenu dans Office 365 est utilisée pour rechercher une boîte aux lettres.
    
  - [Éditeur MAPI Microsoft Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=204086) sert à accéder à la boîte aux lettres. 
    
- Lorsque vous activez l’enregistrement d’audit pour une boîte aux lettres, vous pouvez également indiquer quelles actions de l’utilisateur (par exemple l’accès, le déplacement ou la suppression d’un message) doivent être enregistrées pour chaque type de connexion (administrateur, délégué ou propriétaire). 
    
- Pour désactiver la journalisation d’audit de boîte aux lettres, exécutez la commande suivante :

  ```
  Set-Mailbox -Identity <identity of mailbox> -AuditEnabled $false
   ```

- Les actions qui sont vérifiées pour chaque type d’utilisateur ne sont pas affichées lorsque vous exécutez l’applet de commande **Get-Mailbox** . Mais vous pouvez exécuter les commandes suivantes pour afficher toutes les actions d’auditées pour un type d’ouverture de session utilisateur spécifique. 

    ```
    Get-Mailbox <identity of mailbox> | Select-Object -ExpandProperty AuditAdmin
    ```

    ```
    Get-Mailbox <identity of mailbox> | Select-Object -ExpandProperty AuditDelegate
    ```

    ```
    Get-Mailbox <identity of mailbox> | Select-Object -ExpandProperty AuditOwner
    ```

- Vous pouvez également exporter un journal d’audit de boîte aux lettres et spécifier les entrées à inclure pour un ou plusieurs utilisateurs. Chaque entrée dans le rapport et le journal d’audit inclut des informations sur qui a effectué l’action et, lors de l’action effectuée, et si l’action a réussi. Pour plus d’informations, voir [exporter des journaux d’audit de boîte aux lettres](https://go.microsoft.com/fwlink/p/?LinkID=404104).
