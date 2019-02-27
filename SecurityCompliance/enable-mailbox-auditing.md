---
title: Activer l’audit de boîte aux lettres dans Office 365
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
ms.assetid: aaca8987-5b62-458b-9882-c28476a66918
description: Dans Office 365, vous pouvez activer la journalisation d'audit des boîtes aux lettres pour enregistrer l'accès aux boîtes aux lettres par les propriétaires des boîtes aux lettres, les délégués et les administrateurs. Par défaut, l'audit des boîtes aux lettres dans Office 365 n'est pas activé. Une fois que vous avez activé l'enregistrement d'audit de boîte aux lettres pour une boîte aux lettres, vous pouvez rechercher dans le journal d'audit Office 365 les activités réalisées sur la boîte aux lettres.
ms.openlocfilehash: a9bc84bad8532dd546d5ce3e2f149151967050d6
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30295917"
---
# <a name="enable-mailbox-auditing-in-office-365"></a>Activer l’audit de boîte aux lettres dans Office 365
  
Dans Office 365, vous pouvez activer la journalisation d'audit des boîtes aux lettres pour enregistrer l'accès aux boîtes aux lettres par les propriétaires des boîtes aux lettres, les délégués et les administrateurs. Par défaut, l'audit des boîtes aux lettres dans Office 365 n'est pas activé. Cela signifie que les événements d'audit de boîte aux lettres n'apparaîtront pas dans les résultats lorsque vous effectuerez une recherche dans le journal d'audit Office 365 pour l'activité des boîtes aux lettres Mais après avoir activé l'enregistrement d'audit de boîte aux lettres pour une boîte aux lettres d'utilisateur, vous pouvez rechercher dans le journal d'audit l'activité des boîtes aux lettres. En outre, lorsque l'enregistrement d'audit de boîte aux lettres est activé, certaines actions effectuées par les administrateurs, délégués et propriétaires sont enregistrées par défaut. Pour enregistrer les actions supplémentaires dans le journal (et les Rechercher), reportez-vous à l'étape 3.

## <a name="before-you-begin"></a>Avant de commencer
  
- Vous devez utiliser Exchange Online PowerShell pour activer la journalisation d'audit des boîtes aux lettres. Vous ne pouvez pas utiliser le centre &amp; de sécurité conformité d'Office 365 ou le centre d'administration Exchange.
    
- Vous ne pouvez pas activer l'enregistrement d'audit pour la boîte aux lettres associée à un groupe Office 365 ou une équipe dans Microsoft Teams.
    
- Un administrateur disposant de l'autorisation Accès complet sur la boîte aux lettres d'un utilisateur est considéré comme un utilisateur délégué.
  
## <a name="step-1-connect-to-exchange-online-powershell"></a>Étape 1: Connectez-vous à Exchange Online PowerShell

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

Une fois que vous vous êtes connecté à votre organisation Exchange Online, utilisez PowerShell pour activer l'enregistrement d'audit de boîte aux lettres pour une boîte aux lettres. Vous pouvez également activer l'audit de boîte aux lettres pour toutes les boîtes aux lettres de votre organisation.
  
Cet exemple active l'enregistrement d'audit de boîte aux lettres pour la boîte aux lettres de Pilar Pinilla.
  
```
Set-Mailbox -Identity "Pilar Pinilla" -AuditEnabled $true
```

Dans cet exemple, la journalisation d'audit est activée pour toutes les boîtes aux lettres d'utilisateur de votre organisation.
  
```
Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | Set-Mailbox -AuditEnabled $true
```
  
## <a name="step-3-specify-owner-actions-to-audit"></a>Étape 3 : indication des actions de propriétaire à auditer

Lorsque vous activez l'audit pour une boîte aux lettres, certaines actions effectuées par le propriétaire de la boîte aux lettres sont auditées par défaut. Vous devez spécifier d'autres actions de propriétaire à auditer. Consultez le tableau de la section [actions d'audit de boîte aux lettres](#mailbox-auditing-actions) pour obtenir une liste et une description des actions de propriétaire qui sont enregistrées par défaut et les autres actions pouvant être auditées. 
  
Cet exemple ajoute les actions du propriétaire **MailboxLogin** et **HardDelete** à l'audit de boîte aux lettres pour la boîte aux lettres de Pilar Pinilla. Cet exemple part du principe que l'audit des boîtes aux lettres a déjà été activé pour cette boîte aux lettres. 

```
Set-Mailbox "Pilar Pinilla" -AuditOwner @{Add="MailboxLogin","HardDelete"}
```

Cet exemple active l'enregistrement d'audit de la boîte aux lettres de Don Hall et spécifie que seule l'action **MailboxLogin** effectuée par le propriétaire de la boîte aux lettres sera enregistrée. Notez que cet exemple remplace l'action UpdateFolderPermissions par défaut. 
  
```
Set-Mailbox "Don Hall" -AuditEnabled $true -AuditOwner MailboxLogin
```
   
Cet exemple ajoute les actions **MailboxLogin**, **HardDelete**et **SoftDelete** owner à toutes les boîtes aux lettres de l'organisation. Cet exemple suppose que l'audit des boîtes aux lettres a déjà été activé pour toutes les boîtes aux lettres. 
  
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
   
La valeur **true** pour la propriété **AuditEnabled** vérifie que la journalisation d'audit des boîtes aux lettres est activée. 
    
## <a name="mailbox-auditing-actions"></a>Actions d'audit de boîte aux lettres
  
Le tableau suivant répertorie les actions qui peuvent être consignées par l'enregistrement d'audit de boîte aux lettres. Le tableau indique quelle action peut être consignée pour les différents types d'ouverture de session de l'utilisateur. Dans le tableau, un **non** indique qu'une action ne peut pas être enregistrée pour ce type d'ouverture de session. Un astérisque ( **\*** ) indique que l'action est enregistrée par défaut lorsque l'enregistrement d'audit de boîte aux lettres est activé pour la boîte aux lettres. 
  
|**Action**|**Description**|**Administrateur**|**Délégué\*\*\***|**Propriétaire**|
|:-----|:-----|:-----|:-----|:-----|
|**Copier** <br/> |Un message a été copié dans un autre dossier.  <br/> |Oui  <br/> |Non  <br/> |Non  <br/> |
|**Create** <br/> |Un élément est créé dans le dossier calendrier, contacts, notes ou tâches de la boîte aux lettres; par exemple, une nouvelle demande de réunion est créée. Notez que la création, l'envoi ou la réception d'un message n'est pas audité. En outre, la création d'un dossier de boîte aux lettres n'est pas auditée.  <br/> |Oui\*  <br/> |Oui\*  <br/> |Oui  <br/> |
|**FolderBind** <br/> |Un utilisateur a accédé au dossier de boîte aux lettres. Cette action est également enregistrée lorsque l’administrateur ou un délégué ouvre la boîte aux lettres.  <br/> |Oui  <br/> |Oui\*\*  <br/> |Non  <br/> |
|**HardDelete** <br/> |Un message a été purgé du dossier Éléments récupérables.  <br/> |Oui\*  <br/> |Oui\*  <br/> |Oui  <br/> |
|**MailboxLogin** <br/> |L'utilisateur s'est connecté à sa boîte aux lettres.  <br/> |Non  <br/> |Non  <br/> |Oui  <br/> |
|**MessageBind** <br/> |Un message a été affiché dans le volet de visualisation ou ouvert.  <br/> |Oui  <br/> |Non  <br/> |Non  <br/> |
|**Déplacer** <br/> |Un message a été déplacé vers un autre dossier.  <br/> |Oui  <br/> |Oui   <br/> |Non  <br/> |
|**MoveToDeletedItems** <br/> |Un message a été supprimé et déplacé vers le dossier Éléments supprimés.  <br/> |Oui\*  <br/> |Oui\*  <br/> |Oui  <br/> |
|**SendAs** <br/> |Un message a été envoyé à l’aide de l’autorisation SendAs. Cela signifie qu’un autre utilisateur a envoyé le message comme s’il provenait du propriétaire de la boîte aux lettres.  <br/> |Oui\*  <br/> |Oui\*  <br/> |Non  <br/> |
|**SendOnBehalf** <br/> |Un message a été envoyé à l’aide de l’autorisation SendOnBehalf. Cela signifie qu’un autre utilisateur a envoyé le message de la part du propriétaire de la boîte aux lettres. Le message indique au destinataire de la part de qui le message a été envoyé et qui a envoyé réellement le message.  <br/> |Oui\*  <br/> |Oui\*  <br/> |Non  <br/> |
|**SoftDelete** <br/> |Un message a été définitivement supprimé ou supprimé (récupérable) du dossier Éléments supprimés. Les éléments supprimés récupérables sont déplacés vers le dossier Éléments récupérables.  <br/> |Oui\*  <br/> |Oui\*  <br/> |Oui  <br/> |
|**Mettre à jour** <br/> |Un message ou ses propriétés ont été modifiés.  <br/> |Oui\*  <br/> |Oui\*  <br/> |Oui  <br/> |
|**UpdateCalendarDelegation** <br/> |Une délégation de calendrier a été affectée à une boîte aux lettres. La délégation de calendrier donne à une autre personne de la même organisation des autorisations pour gérer le calendrier du propriétaire de la boîte aux lettres.  <br/> |Oui\*  <br/> |Non  <br/> |Oui\*  <br/> |
|**UpdateFolderPermissions** <br/> |Une autorisation de dossier a été modifiée. Les autorisations de dossier contrôlent les utilisateurs de votre organisation qui peuvent accéder aux dossiers d'une boîte aux lettres et aux messages qu'ils hébergent.  <br/> |Oui\*  <br/> |Oui\*  <br/> |Oui\*  <br/> |
|**UpdateInboxRules** <br/> |Une règle de boîte de réception a été ajoutée, supprimée ou modifiée. Les règles de boîte de réception sont utilisées pour traiter les messages dans la boîte de réception de l'utilisateur en fonction des conditions spécifiées et prendre des mesures lorsque les conditions d'une règle sont remplies, telles que le transfert d'un message vers un dossier spécifié ou la suppression d'un message.  <br/> |Oui\*  <br/> |Oui\*  <br/> |Oui\*  <br/> |
   
> [!NOTE]
> <sup>\*</sup>Auditée par défaut si l'audit est activé pour une boîte aux lettres.<br/><br/>  <sup>\*\*</sup>Les entrées pour les actions de liaison de dossiers effectuées par des délégués sont consolidées. Une entrée de journal est générée pour l'accès à un dossier individuel dans un intervalle de temps de 24 heures.<br/><br/><sup>\*\*\*</sup>Un administrateur disposant de l'autorisation accès total à la boîte aux lettres d'un utilisateur est considéré comme un utilisateur délégué. 
  
Si vous n'avez plus besoin d'auditer certains types d'actions de boîte aux lettres, vous devez modifier la configuration de journalisation d'audit de la boîte aux lettres pour désactiver ces actions. Les entrées de journal existantes ne sont pas purgées tant que la limite d'âge de rétention des entrées du journal d'audit n'est pas atteinte. Pour plus d'informations sur l'âge de rétention pour les entrées du journal d'audit, voir la section «avant de commencer» dans [Search the Audit Log in the Office 365 Security _AMP_ Compliance Center](search-the-audit-log-in-security-and-compliance.md#before-you-begin).
  
## <a name="more-infotab"></a>[Informations supplémentaires](#tab/)
  
- Utilisez le journal d'audit Office 365 pour Rechercher l'activité de boîte aux lettres qui a été enregistrée. Vous pouvez rechercher une activité pour une boîte aux lettres d'utilisateur spécifique. La capture d'écran suivante montre une liste des activités de boîte aux lettres que vous pouvez rechercher dans le journal d'audit Office 365. Notez que ces activités sont les mêmes que celles décrites dans la section «actions d'audit de boîte aux lettres» de cette rubrique.
    
    ![Vous pouvez rechercher le journal d'audit Office 365 pour les actions d'audit de boîte aux lettres en sélectionnant «activités de boîte aux lettres Exchange» dans la liste déroulante activités.](media/fadc34f8-9de2-4688-8b1a-bc5540e69a23.png)
  
    Le tableau suivant décrit chaque activité de boîte aux lettres que vous pouvez rechercher et indique l'action d'audit de boîte aux lettres correspondante.
    
    |**Activité dans le journal d'audit**|**Action d'audit de boîte aux lettres**|
    |:-----|:-----|
    |Élément de boîte aux lettres créé  <br/> |Create  <br/> |
    |Messages copiés dans un autre dossier  <br/> |Copy  <br/> |
    |L'utilisateur s'est connecté à la boîte aux lettres  <br/> |MailboxLogin  <br/> |
    |Message envoyé à l'aide des autorisations Envoyer de la part de  <br/> |SendOnBehalf  <br/> |
    |Messages purgés de la boîte aux lettres  <br/> |HardDelete  <br/> |
    |Messages déPlacés vers le dossier éléments supprimés  <br/> |MoveToDeletedItems  <br/> |
    |Messages déPlacés dans un autre dossier  <br/> |Move  <br/> |
    |Message envoyé à l'aide des autorisations Envoyer en tant que  <br/> |SendAs  <br/> |
    |Message mis à jour  <br/> |Update  <br/> |
    |Messages supprimés du dossier éléments supprimés  <br/> |SoftDelete  <br/> |
    |Ajout d'autorisations au dossier  <br/> |UpdateFolderPermissions  <br/> |
    |Autorisations modifiées du dossier  <br/> |UpdateFolderPermissions  <br/> |
    |Autorisations supprimées du dossier  <br/> |UpdateFolderPermissions  <br/> |
    |Ajout ou suppression d'un utilisateur avec un accès délégué au dossier de calendrier  <br/> |UpdateCalendarDelegation  <br/> |
   
    Notez que les activités de **boîte aux lettres déléguée ajoutées** et **suppression des autorisations de boîte aux lettres déléguée** indiquées dans la capture d'écran précédente ne sont pas liées aux actions d'audit de boîte aux lettres. Elles indiquent si un administrateur a affecté ou supprimé l'autorisation de boîte aux lettres FullAccess. 
    
    Pour plus d'informations sur le journal d'audit Office 365, voir [Search the audit log dans le &amp; Centre de sécurité conformité Office 365](search-the-audit-log-in-security-and-compliance.md).
    
- On considère qu'un administrateur accède aux boîtes aux lettres uniquement dans les cas suivants :
    
  - La découverte électronique inaltérable dans Exchange Online ou la recherche de contenu dans Office 365 est utilisée pour effectuer une recherche dans une boîte aux lettres.
    
  - [Éditeur MAPI Microsoft Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=204086) sert à accéder à la boîte aux lettres. 
    
- Lorsque vous activez l’enregistrement d’audit pour une boîte aux lettres, vous pouvez également indiquer quelles actions de l’utilisateur (par exemple l’accès, le déplacement ou la suppression d’un message) doivent être enregistrées pour chaque type de connexion (administrateur, délégué ou propriétaire). 
    
- Pour désactiver la journalisation d’audit de boîte aux lettres, exécutez la commande suivante :

  ```
  Set-Mailbox -Identity <identity of mailbox> -AuditEnabled $false
   ```

- Les actions qui sont auditées pour chaque type d'utilisateur ne s'affichent pas lorsque vous exécutez la cmdlet **Get-Mailbox** . Toutefois, vous pouvez exécuter les commandes suivantes pour afficher toutes les actions auditées pour un type d'ouverture de session d'utilisateur spécifique. 

    ```
    Get-Mailbox <identity of mailbox> | Select-Object -ExpandProperty AuditAdmin
    ```

    ```
    Get-Mailbox <identity of mailbox> | Select-Object -ExpandProperty AuditDelegate
    ```

    ```
    Get-Mailbox <identity of mailbox> | Select-Object -ExpandProperty AuditOwner
    ```

- Vous pouvez également exporter un journal d'audit de boîte aux lettres et spécifier les entrées à inclure pour un ou plusieurs utilisateurs. Chaque entrée du rapport et du journal d'audit comprend des informations sur la personne qui a effectué l'action et le moment où l'action a été effectuée, et indique si l'action a réussi. Pour plus d'informations, consultez la rubrique [exporter des journaux d'audit de boîte aux lettres](https://go.microsoft.com/fwlink/p/?LinkID=404104).
