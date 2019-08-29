---
title: Gérer l’audit de boîte aux lettres
ms.author: chrisda
author: chrisda
manager: dansimp
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
ms.assetid: aaca8987-5b62-458b-9882-c28476a66918
description: La journalisation d’audit de boîte aux lettres est activée par défaut dans Office 365 (également appelée audit de boîte aux lettres par défaut ou audit de boîte aux lettres par défaut). En d’autres termes, certaines actions effectuées par les propriétaires de boîtes aux lettres, les délégués et les administrateurs sont automatiquement enregistrées dans un journal d’audit de boîte aux lettres, dans lequel vous pouvez rechercher des activités effectuées sur la boîte aux lettres.
ms.openlocfilehash: 049b9fe79ae3389e09fb07017fd2deb810640f35
ms.sourcegitcommit: 3962de88a143f0eb416b5cfdfd777d731f560ec8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/28/2019
ms.locfileid: "36649909"
---
# <a name="manage-mailbox-auditing"></a>Gérer l’audit de boîte aux lettres

À compter du 1er janvier 2019, Microsoft Active la journalisation d’audit des boîtes aux lettres par défaut pour toutes les organisations Office 365. Cela signifie que certaines actions effectuées par les propriétaires de boîtes aux lettres, les délégués et les administrateurs sont automatiquement journalisées et que les enregistrements d’audit de boîte aux lettres correspondants sont disponibles lorsque vous les recherchez dans le journal d’audit de boîte aux lettres. Avant que l’audit des boîtes aux lettres ait été activé par défaut, vous devez l’activer manuellement pour chaque boîte aux lettres d’utilisateur de votre organisation.

Voici quelques avantages de l’audit des boîtes aux lettres par défaut:

- L’audit est automatiquement activé lorsque vous créez une nouvelle boîte aux lettres. Vous n’avez pas besoin de l’activer manuellement pour les nouveaux utilisateurs.

- Vous n’avez pas besoin de gérer les actions de boîte aux lettres qui sont auditées. Un ensemble prédéfini d’actions de boîte aux lettres est audité par défaut pour chaque type d’ouverture de session (administrateur, délégué et propriétaire).

- Lorsque Microsoft publie une nouvelle action de boîte aux lettres (en particulier les actions qui contribuent à protéger votre organisation et vous aide à effectuer des enquêtes de façon judiciaire), l’action est automatiquement ajoutée à la liste des actions de boîte aux lettres qui sont auditées par défaut. Cela signifie que vous n’avez pas besoin de surveiller ajouter de nouvelles actions sur les boîtes aux lettres.

- Vous disposez d’une stratégie d’audit de boîte aux lettres cohérente au sein de votre organisation (car vous auditez les mêmes actions pour toutes les boîtes aux lettres).

> [!NOTE]
>• Il est important de garder à l’esprit la publication de l’audit des boîtes aux lettres sur par défaut: vous n’avez rien à faire pour gérer l’audit des boîtes aux lettres. Toutefois, pour en savoir plus, personnaliser l’audit des boîtes aux lettres à partir des paramètres par défaut ou le désactiver, cette rubrique peut vous aider. <br><br>• Même lorsque l’audit de boîte aux lettres activé est activé par défaut, vous pouvez remarquer que des événements d’audit de boîte aux lettres pour certains utilisateurs ne sont pas détectés dans les recherches dans le journal d’audit dans le centre de sécurité & ou via l’API activité de gestion d’Office 365. Pour plus d’informations, reportez-vous à la section [plus d’informations](#more-information) de cette rubrique.

## <a name="verify-mailbox-auditing-on-by-default-is-turned-on"></a>Vérifier que l’audit de boîte aux lettres activé est activé par défaut

Pour vérifier que l’audit de boîte aux lettres activé par défaut est activé pour votre organisation, exécutez la commande suivante dans [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell):

```
Get-OrganizationConfig | Format-List AuditDisabled
```

La valeur **false** indique que l’audit de boîte aux lettres activé par défaut est activé pour l’organisation. Cette valeur de l’organisation par défaut remplace le paramètre d’audit de boîte aux lettres sur des boîtes aux lettres spécifiques. Par exemple, si l’audit de boîte aux lettres est désactivé pour une boîte aux lettres (la propriété *AuditEnabled* a la **valeur false** sur la boîte aux lettres), les actions de boîte aux lettres par défaut seront toujours auditées pour la boîte aux lettres, car l’audit de boîte aux lettres activé par défaut est activé pour le Département.

Pour conserver l’audit de boîte aux lettres désactivé pour des boîtes aux lettres spécifiques, vous devez configurer le contournement d’audit de boîte aux lettres pour le propriétaire de la boîte aux lettres et d’autres utilisateurs auxquels l’accès à la boîte aux lettres a été délégué. Pour plus d’informations, reportez-vous à la section Contournement de l' [enregistrement d’audit des boîtes aux lettres](#bypass-mailbox-audit-logging) de cette rubrique.

> [!NOTE]
> Lorsque l’audit de boîte aux lettres activé par défaut est activé pour l’organisation, la propriété *AuditEnabled* des boîtes aux lettres affectées ne passe pas de **false** à **true**. En d’autres termes, l’audit de boîte aux lettres sur par défaut ignore la propriété *AuditEnabled* sur les boîtes aux lettres.

## <a name="supported-mailbox-types"></a>Types de boîtes aux lettres pris en charge

Le tableau suivant indique les types de boîtes aux lettres actuellement pris en charge par l’audit des boîtes aux lettres par défaut:

|**Type de boîte aux lettres**|**Pris en charge**|**Non pris en charge**|
|:---------|:---------:|:---------:|
|Boîtes aux lettres utilisateur|![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||
|Boîtes aux lettres partagées|![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||
|Boîtes aux lettres de groupe Office 365|![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||
|Boîtes aux lettres de ressources||![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|Boîtes aux lettres de dossiers publics||![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|

## <a name="logon-types-and-mailbox-actions"></a>Types d’ouverture de session et actions de boîte aux lettres

Les types d’ouverture de session classent l’utilisateur qui a effectué les actions auditées sur la boîte aux lettres. La liste suivante décrit les types d’ouverture de session utilisés lors de l’enregistrement d’audit de boîte aux lettres:

- **Propriétaire**: le propriétaire de la boîte aux lettres (le compte associé à la boîte aux lettres).

- **Délégué**:

  - Un utilisateur auquel l’autorisation SendAs, SendOnBehalf ou FullAccess a été attribuée à une autre boîte aux lettres.

  - Administrateur auquel l’autorisation FullAccess a été attribuée à la boîte aux lettres d’un utilisateur.

- **Administrateur**:

  - La boîte aux lettres est recherchée avec l’un des outils Microsoft eDiscovery suivants:

    - Recherche de contenu dans le centre de conformité.

    - eDiscovery ou Advanced eDiscovery dans le centre de conformité.

    - Découverte électronique inaltérable dans Exchange Online.

  - La boîte aux lettres est accessible à l’aide de l' [Éditeur MAPI Microsoft Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=204086).

### <a name="mailbox-actions-for-user-mailboxes-and-shared-mailboxes"></a>Actions de boîte aux lettres pour les boîtes aux lettres utilisateur et les boîtes aux lettres partagées

Le tableau suivant décrit les actions de boîte aux lettres disponibles dans l’enregistrement d’audit de boîte aux lettres pour les boîtes aux lettres d’utilisateur et les boîtes aux lettres partagées.

- Une coche ( ![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)) indique que l’action de boîte aux lettres peut être enregistrée pour le type d’ouverture de session (toutes les actions ne sont pas disponibles pour tous les types d’ouverture de session).

- Un astérisque ( <sup>\*</sup> ) après la coche indique que l’action de boîte aux lettres est enregistrée par défaut pour le type d’ouverture de session.

- N’oubliez pas qu’un administrateur disposant d’une autorisation d’accès total à une boîte aux lettres est considéré comme un délégué.

|**Action de boîte aux lettres**|**Description**|**Administrateur**|**Délégué**|**Owner**|
|:---------|:---------|:---------:|:---------:|:---------:|
|**AddFolderPermissions**|**Remarque**: bien que cette valeur soit acceptée en tant qu’action de boîte aux lettres, elle est déjà incluse dans l’action **UpdateFolderPermissions** et n’est pas auditée séparément. En d’autres termes, n’utilisez pas cette valeur.||||
|**ApplyRecord**|Un élément est étiqueté en tant qu’enregistrement.|![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|**Copier**|Un message a été copié dans un autre dossier.|![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|||
|**Create**|Un élément a été créé dans le dossier calendrier, contacts, notes ou tâches dans la boîte aux lettres (par exemple, une nouvelle demande de réunion est créée). Notez que la création, l’envoi ou la réception d’un message n’est pas audité. En outre, la création d’un dossier de boîte aux lettres n’est pas auditée.|![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|**FolderBind**|Un utilisateur a accédé au dossier de boîte aux lettres. Cette action est également enregistrée lorsque l’administrateur ou un délégué ouvre la boîte aux lettres.<br/><br/> **Remarque**: les enregistrements d’audit pour les actions de liaison de dossiers effectuées par des délégués sont consolidés. Un enregistrement d’audit est généré pour l’accès à un dossier individuel dans les 24 heures.|![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||
|**HardDelete**|Un message a été purgé du dossier Éléments récupérables.|![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|
|**MailboxLogin**|L’utilisateur est connecté à sa boîte aux lettres. |||![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|**MessageBind**|Un message a été affiché dans le volet de visualisation ou ouvert.|![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|||
|**ModifyFolderPermissions**|**Remarque**: bien que cette valeur soit acceptée en tant qu’action de boîte aux lettres, elle est déjà incluse dans l’action **UpdateFolderPermissions** et n’est pas auditée séparément. En d’autres termes, n’utilisez pas cette valeur.||||
|**Déplacer**|Un message a été déplacé vers un autre dossier.|![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|**MoveToDeletedItems**|Un message a été supprimé et déplacé vers le dossier Éléments supprimés.|![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|
|**RecordDelete**|Un élément étiqueté comme enregistrement a été supprimé de manière récupérable (déplacé vers le dossier éléments récupérables). Les éléments étiquetés comme enregistrements ne peuvent pas être supprimés définitivement (purgés du dossier éléments récupérables).|![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|**RemoveFolderPermissions**|**Remarque**: bien que cette valeur soit acceptée en tant qu’action de boîte aux lettres, elle est déjà incluse dans l’action **UpdateFolderPermissions** et n’est pas auditée séparément. En d’autres termes, n’utilisez pas cette valeur.||||
|**SendAs**|Un message a été envoyé à l’aide de l’autorisation SendAs. Cela signifie qu’un autre utilisateur a envoyé le message comme s’il provenait du propriétaire de la boîte aux lettres.|![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>||
|**SendOnBehalf**|Un message a été envoyé à l’aide de l’autorisation SendOnBehalf. Cela signifie qu’un autre utilisateur a envoyé le message de la part du propriétaire de la boîte aux lettres. Le message indique au destinataire de la part de qui le message a été envoyé et qui a envoyé réellement le message.|![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>||
|**SoftDelete**|Un message a été définitivement supprimé ou supprimé (récupérable) du dossier Éléments supprimés. Les éléments supprimés récupérables sont déplacés vers le dossier Éléments récupérables.|![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|
|**Update**|Un message ou ses propriétés ont été modifiés.|![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|
|**UpdateCalendarDelegation**|Une délégation de calendrier a été affectée à une boîte aux lettres. La délégation de calendrier donne à une autre personne de la même organisation des autorisations pour gérer le calendrier du propriétaire de la boîte aux lettres.|![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>||![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|
|**UpdateFolderPermissions**|Une autorisation de dossier a été modifiée. Les autorisations de dossier contrôlent les utilisateurs de votre organisation qui peuvent accéder aux dossiers d’une boîte aux lettres et aux messages qu’ils hébergent.|![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|
|**UpdateInboxRules**|Une règle de boîte de réception a été ajoutée, supprimée ou modifiée. Les règles de boîte de réception sont utilisées pour traiter les messages dans la boîte de réception de l’utilisateur en fonction des conditions spécifiées et prendre des mesures lorsque les conditions d’une règle sont remplies, telles que le transfert d’un message vers un dossier spécifié ou la suppression d’un message.|![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|

> [!IMPORTANT]
> Si vous avez personnalisé les actions de boîte aux lettres à auditer pour tout type d’ouverture de session *avant* l’activation de l’audit de boîte aux lettres par défaut dans votre organisation, les paramètres personnalisés sont conservés dans la boîte aux lettres et ne sont pas remplacés par les actions de boîte aux lettres par défaut comme décrit dans cette section. Pour rétablir les valeurs par défaut des actions de boîte aux lettres d’audit (que vous pouvez effectuer à tout moment), consultez la section [restaurer les actions de boîte aux lettres par défaut](#restore-the-default-mailbox-actions) plus loin dans cette rubrique.

### <a name="mailbox-actions-for-office-365-group-mailboxes"></a>Actions de boîte aux lettres pour les boîtes aux lettres de groupe Office 365

La fonction d’audit de boîte aux lettres activée par défaut permet la journalisation d’audit des boîtes aux lettres de groupe Office 365, mais vous ne pouvez pas personnaliser le contenu journalisé (vous ne pouvez pas ajouter ou supprimer des actions de boîte aux lettres qui sont consignées pour un type d’ouverture de session).

Le tableau suivant décrit les actions de boîte aux lettres qui sont enregistrées par défaut sur les boîtes aux lettres de groupe Office 365 pour chaque type d’ouverture de session.

N’oubliez pas qu’un administrateur disposant d’une autorisation d’accès total à une boîte aux lettres de groupe Office 365 est considéré comme un délégué.

|**Action de boîte aux lettres**|**Description**|**Administrateur**|**Délégué**|**Owner**|
|:---------|:---------|:---------:|:---------:|:---------:|
|**Create**|Création d’un élément de calendrier. Notez que la création, l’envoi ou la réception d’un message n’est pas audité.|![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>||
|**HardDelete**|Un message a été purgé du dossier Éléments récupérables.|![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|
|**MoveToDeletedItems**|Un message a été supprimé et déplacé vers le dossier Éléments supprimés.|![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|
|**SendAs**|Un message a été envoyé à l’aide de l’autorisation SendAs.|![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>||
|**SendOnBehalf**|Un message a été envoyé à l’aide de l’autorisation SendOnBehalf. |![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>||
|**SoftDelete**|Un message a été définitivement supprimé ou supprimé (récupérable) du dossier Éléments supprimés. Les éléments supprimés récupérables sont déplacés vers le dossier Éléments récupérables.|![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|
|**Update**|Un message ou ses propriétés ont été modifiés.|![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![Case à cocher](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|

### <a name="verify-that-default-mailbox-actions-are-being-logged-for-each-logon-type"></a>Vérifier que les actions de boîte aux lettres par défaut sont journalisées pour chaque type d’ouverture de session

L’audit de boîte aux lettres activé par défaut ajoute une nouvelle propriété *DefaultAuditSet* à toutes les boîtes aux lettres. La valeur de cette propriété indique si les actions de boîte aux lettres par défaut (gérées par Microsoft) sont auditées sur la boîte aux lettres.

Pour afficher la valeur sur les boîtes aux lettres utilisateur ou les boîtes aux \<lettres\> partagées, remplacez MailboxIdentity par le nom, l’alias, l’adresse de messagerie ou le nom d’utilisateur principal (username) de la boîte aux lettres, puis exécutez la commande suivante dans Exchange Online PowerShell:

```
Get-Mailbox -Identity <MailboxIdentity> | Format-List DefaultAuditSet
```

Pour afficher la valeur sur les boîtes aux lettres de groupe Office \<365\> , remplacez MailboxIdentity par le nom, l’alias ou l’adresse de messagerie de la boîte aux lettres partagée, puis exécutez la commande suivante dans Exchange Online PowerShell:

```
Get-Mailbox -Identity <MailboxIdentity> -GroupMailbox | Format-List DefaultAuditSet
```

La valeur `Admin, Delegate, Owner` indique:

- Les actions de boîte aux lettres par défaut pour les trois types d’ouverture de session sont auditées. Notez qu’il s’agit de la seule valeur que vous verrez sur les boîtes aux lettres de groupe Office 365.

- Un administrateur n' *a pas* modifié les actions de boîte aux lettres auditées pour tout type d’ouverture de session sur une boîte aux lettres d’utilisateur ou une boîte aux lettres partagée. Remarque Il s’agit de l’État par défaut après activation initiale de l’audit des boîtes aux lettres dans votre organisation.

Si un administrateur a déjà modifié les actions de boîte aux lettres qui sont auditées pour un type d’ouverture de session (à l’aide des paramètres *AuditAdmin*, *AuditDelegate*ou *AuditOwner* sur la cmdlet **Set-Mailbox** ), la valeur de la propriété sera différente.

Par exemple, la valeur `Owner` de la propriété *DefaultAuditSet* sur une boîte aux lettres d’utilisateur ou une boîte aux lettres partagée indique:

- Les actions de boîte aux lettres par défaut pour le propriétaire de la boîte aux lettres sont auditées.

- Les actions de boîte aux lettres auditées pour les `Delegate` types d’ouverture de session et `Admin` de connexion ont été modifiées par rapport aux actions par défaut.

Une valeur vide pour la propriété *DefaultAuditSet* indique que les actions de boîte aux lettres pour les trois types d’ouverture de session ont été modifiées dans la boîte aux lettres utilisateur ou dans une boîte aux lettres partagée.

Pour plus d’informations, consultez la section [modifier ou restaurer les actions de boîte aux lettres enregistrées par défaut](#change-or-restore-mailbox-actions-logged-by-default) de cette rubrique.

### <a name="display-the-mailbox-actions-that-are-being-logged-on-mailboxes"></a>Afficher les actions de boîte aux lettres qui sont consignées sur des boîtes aux lettres

Pour afficher les actions de boîte aux lettres actuellement enregistrées sur des boîtes aux lettres d’utilisateurs ou des boîtes \<aux\> lettres partagées, remplacez MailboxIdentity par le nom, l’alias, l’adresse de messagerie ou le nom d’utilisateur principal (username) de la boîte aux lettres, puis exécutez une ou plusieurs des opérations suivantes: commandes dans Exchange Online PowerShell.

> [!NOTE]
> Bien que vous puissiez ajouter `-GroupMailbox` le commutateur aux commandes **Get-Mailbox** suivantes pour les boîtes aux lettres de groupe Office 365, ne croyez pas les valeurs que vous voyez. Les actions de boîte aux lettres par défaut et statiques qui sont auditées pour les boîtes aux lettres de groupe Office 365 sont décrites dans la section [actions de boîte aux lettres pour les boîtes aux lettres de groupe office 365](#mailbox-actions-for-office-365-group-mailboxes) plus haut dans cette rubrique.

#### <a name="owner-actions"></a>Actions du propriétaire

```
Get-Mailbox -Identity <MailboxIdentity> | Select-Object -ExpandProperty AuditOwner
```

#### <a name="delegate-actions"></a>Actions de délégué

```
Get-Mailbox -Identity <MailboxIdentity> | Select-Object -ExpandProperty AuditDelegate
```

#### <a name="admin-actions"></a>Actions d’administration

```
Get-Mailbox -Identity <MailboxIdentity> | Select-Object -ExpandProperty AuditAdmin
```

## <a name="change-or-restore-mailbox-actions-logged-by-default"></a>Modifier ou restaurer les actions de boîte aux lettres enregistrées par défaut

Comme expliqué précédemment, l’un des principaux avantages de l’audit de boîte aux lettres par défaut est le suivant: vous n’avez pas besoin de gérer les actions des boîtes aux lettres qui sont auditées. Microsoft le procède pour vous et ajoute automatiquement de nouvelles actions de boîte aux lettres à auditer par défaut lorsqu’elles sont publiées.

Toutefois, votre organisation peut être amenée à auditer un autre ensemble d’actions de boîte aux lettres pour les boîtes aux lettres d’utilisateur et les boîtes aux lettres partagées. Les procédures décrites dans cette section expliquent comment modifier les actions de boîte aux lettres qui sont auditées pour chaque type d’ouverture de session et comment rétablir les actions par défaut gérées par Microsoft.

> [!IMPORTANT]
> Si vous utilisez les procédures suivantes pour personnaliser les actions de boîte aux lettres qui sont consignées sur des boîtes aux lettres d’utilisateurs ou des boîtes aux lettres partagées, les nouvelles actions de boîte aux lettres par défaut libérées par Microsoft ne seront pas automatiquement auditées sur ces boîtes aux lettres. Vous devez ajouter manuellement les nouvelles actions de boîte aux lettres à votre liste personnalisée d’actions.

### <a name="change-the-mailbox-actions-to-audit"></a>Modifier les actions de boîte aux lettres en audit

Vous pouvez utiliser les paramètres *AuditAdmin*, *AuditDelegate*ou *AuditOwner* sur la cmdlet **Set-Mailbox** pour modifier les actions de boîte aux lettres qui sont auditées pour les boîtes aux lettres d’utilisateur et les boîtes aux lettres partagées (actions auditées pour le groupe Office 365 les boîtes aux lettres ne peuvent pas être personnalisées.

Vous pouvez utiliser deux méthodes différentes pour spécifier les actions de boîte aux lettres:

- *Remplacer* (remplacer) les actions de boîte aux lettres existantes à l’aide `action1,action2,...actionN`de la syntaxe suivante:.

- *Ajouter ou supprimer* des actions de boîte aux lettres sans affecter les autres valeurs existantes `@{Add="action1","action2",..."actionN"}` à `@{Remove="action1","action2",..."actionN"}`l’aide de la syntaxe suivante: ou.

Cet exemple modifie les actions de boîte aux lettres d’administration pour la boîte aux lettres nommée «Gabriela Laureano» en écrasant les actions par défaut avec SoftDelete et HardDelete.

```
Set-Mailbox -Identity "Gabriela Laureano" -AuditAdmin HardDelete,SoftDelete
```

Cet exemple montre comment ajouter l’action de propriétaire MailboxLogin à la boîte aux lettres laura@contoso.onmicrosoft.com.

```
Set-Mailbox -Identity laura@contoso.onmicrosoft.com -AuditOwner @{Add="MailboxLogin"}
```

Cet exemple supprime l’action de délégué MoveToDeletedItems pour la boîte aux lettres de discussion d’équipe.

```
Set-Mailbox -Identity "Team Discussion" -AuditDelegate @{Remove="MoveToDeletedItems"}
```

Quelle que soit la méthode que vous utilisez, la personnalisation des actions de boîte aux lettres auditées sur les boîtes aux lettres des utilisateurs ou les boîtes aux lettres partagées a les résultats suivants:

- Pour le type de connexion que vous avez personnalisé, les actions de boîte aux lettres auditées ne sont plus gérées par Microsoft.

- Le type de connexion que vous avez personnalisé n’est plus affiché dans la valeur de la propriété *DefaultAuditSet* de la boîte aux lettres, comme [décrit précédemment](#verify-that-default-mailbox-actions-are-being-logged-for-each-logon-type).

### <a name="restore-the-default-mailbox-actions"></a>Restaurer les actions de boîte aux lettres par défaut

Si vous avez personnalisé les actions de boîte aux lettres qui sont auditées sur une boîte aux lettres utilisateur ou une boîte aux lettres partagée, vous pouvez restaurer les actions de boîte aux lettres par défaut pour un ou tous les types d’ouverture de session à l’aide de la syntaxe suivante:

```
Set-Mailbox -Identity <MailboxIdentity> -DefaultAuditSet <Admin | Delegate | Owner>
```

Vous pouvez spécifier plusieurs valeurs *DefaultAuditSet* séparées par des virgules

**Remarque**: les procédures suivantes ne s’appliquent pas aux boîtes aux lettres de groupe Office 365 (elles sont limitées aux actions par défaut comme décrit [ici](#mailbox-actions-for-office-365-group-mailboxes)).

Cet exemple restaure les actions de boîte aux lettres auditées par défaut pour tous les types d’ouverture de session dans la boîte aux lettres mark@contoso.onmicrosoft.com.

```
Set-Mailbox -Identity mark@contoso.onmicrosoft.com -DefaultAuditSet Admin,Delegate,Owner
```

Cet exemple restaure les actions de boîte aux lettres auditées par défaut pour le type d’ouverture de session administrateur sur la boîte aux lettres chris@contoso.onmicrosoft.com, mais laisse les actions de boîte aux lettres auditées personnalisées pour les types de connexion de délégué et de propriétaire.

```
Set-Mailbox -Identity chris@contoso.onmicrosoft.com -DefaultAuditSet Admin
```

La restauration des actions de boîte aux lettres auditées par défaut pour un type d’ouverture de session a les conséquences suivantes:

- La liste actuelle des actions de boîte aux lettres est remplacée par les actions de boîte aux lettres par défaut pour le type d’ouverture de session.

- Toutes les nouvelles actions de boîte aux lettres publiées par Microsoft sont automatiquement ajoutées à la liste des actions auditées pour le type d’ouverture de session.

- La valeur de la propriété *DefaultAuditSet* de la boîte aux lettres est mise à jour pour inclure le type d’ouverture de session restaurée.

## <a name="turn-off-mailbox-auditing-on-by-default-for-your-organization"></a>Désactiver l’audit des boîtes aux lettres par défaut pour votre organisation

Vous pouvez désactiver l’audit des boîtes aux lettres par défaut pour l’ensemble de votre organisation en exécutant la commande suivante dans Exchange Online PowerShell:

```
Set-OrganizationConfig -AuditDisabled $true
```

La désactivation de l’audit des boîtes aux lettres par défaut a les résultats suivants:

- L’audit des boîtes aux lettres est désactivé pour votre organisation.

- À partir du moment où vous désactivez l’audit des boîtes aux lettres activé par défaut, aucune action de boîte aux lettres n’est auditée, même si l’audit est activé sur une boîte aux lettres (la propriété *AuditEnabled* de la boîte aux lettres est **true**).

- L’audit des boîtes aux lettres n’est pas activé pour les nouvelles boîtes aux lettres et la définition de la propriété *AuditEnabled* sur une boîte aux lettres nouvelle ou existante sur **true** sera ignorée.

- Tout paramètre d’association de contournement d’audit de boîte aux lettres (configuré à l’aide de l’applet de commande **Set-MailboxAuditBypassAssociation** ) est ignoré.

- Les enregistrements d’audit de boîte aux lettres existants sont conservés jusqu’à l’expiration de la limite d’âge du journal d’audit de l’enregistrement.

### <a name="turn-on-mailbox-auditing-on-by-default"></a>Activer l’audit de boîte aux lettres par défaut

Pour réactiver l’audit des boîtes aux lettres pour votre organisation, exécutez la commande suivante dans Exchange Online PowerShell:

```
Set-OrganizationConfig -AuditDisabled $false
```

## <a name="bypass-mailbox-audit-logging"></a>Contournement de l’enregistrement d’audit de boîte aux lettres

Actuellement, vous ne pouvez pas désactiver l’audit de boîte aux lettres pour des boîtes aux lettres spécifiques lorsque l’audit de boîte aux lettres activé par défaut est activé dans votre organisation. Par exemple, la définition de la propriété de boîte aux lettres *AuditEnabled* sur **false** est ignorée.

Toutefois, vous pouvez toujours utiliser la cmdlet **Set-MailboxAuditBypassAssociation** dans Exchange Online PowerShell pour empêcher la journalisation des actions de boîte aux lettres *et de toutes les* boîtes aux lettres par les utilisateurs spécifiés, quel que soit l’endroit où les actions se produisent. Par exemple :

- Les actions du propriétaire de la boîte aux lettres effectuées par les utilisateurs ignorés ne sont pas enregistrées.

- Les actions de délégation effectuées par les utilisateurs ignorés sur les boîtes aux lettres d’autres utilisateurs (y compris les boîtes aux lettres partagées) ne sont pas enregistrées.

- Les actions d’administration effectuées par les utilisateurs ignorés ne sont pas enregistrées.

Pour contourner la journalisation d’audit de boîte aux \<lettres\> pour un utilisateur spécifique, remplacez MailboxIdentity par le nom, l’adresse de messagerie, l’alias ou le nom d’utilisateur principal (username) de l’utilisateur, puis exécutez la commande suivante:

```
Set-MailboxAuditBypassAssociation -Identity <MailboxIdentity> -AuditByPassEnabled $true
```

Pour vérifier que l’audit est contourné pour l’utilisateur spécifié, exécutez la commande suivante:

```
Get-MailboxAuditBypassAssociation -Identity <MailboxIdentity> | Format-List AuditByPassEnabled
```

La valeur **true** indique que l’enregistrement d’audit de boîte aux lettres est contourné pour l’utilisateur.

## <a name="more-information"></a>Plus d’informations

- Seuls les utilisateurs disposant de licences E5 ou de boîtes aux lettres pour lesquelles l’enregistrement d’audit de boîte aux lettres a été activé manuellement par un administrateur renvoient des événements de journal d’audit de boîte aux lettres dans le centre de sécurité & Compliance Center ou via l’API d’activité de gestion d’Office 365.

  Pour récupérer les entrées du journal d’audit de boîte aux lettres pour les utilisateurs sans licence E5, vous pouvez:

  - Utilisez les applets de commande suivantes dans Exchange Online PowerShell:

    - [Search-MailboxAuditLog](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/search-mailboxauditlog) pour rechercher des utilisateurs spécifiques dans le journal d’audit de boîte aux lettres.

    - [New-MailboxAuditLogSearch](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/new-mailboxauditlogsearch) pour rechercher des utilisateurs spécifiques dans le journal d’audit de boîte aux lettres et pour que les résultats soient envoyés par courrier électronique à des destinataires spécifiés.

  - Utilisez le centre d’administration Exchange dans Exchange Online pour effectuer les opérations suivantes:

    - [Exporter les journaux d’audit de boîte aux lettres](https://docs.microsoft.com/Exchange/security-and-compliance/exchange-auditing-reports/export-mailbox-audit-logs)

    - [Exécuter un rapport d'accès aux boîtes aux lettres par des non-propriétaires](https://docs.microsoft.com/Exchange/security-and-compliance/exchange-auditing-reports/non-owner-mailbox-access-report)

- Par défaut, les enregistrements du journal d’audit de boîte aux lettres sont conservés pendant 90 jours avant d’être supprimés. Vous pouvez modifier la limite d’âge pour les enregistrements du journal d’audit à l’aide du paramètre *AuditLogAgeLimit* sur la cmdlet **Set-Mailbox** dans Exchange Online PowerShell. Toutefois, l’augmentation de cette valeur ne vous permet pas de rechercher des événements datant de plus de 90 jours dans le journal d’audit Office 365.

  Si vous augmentez la limite d’âge, vous devez utiliser la cmdlet [Search-MailboxAuditLog](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/search-mailboxauditlog) dans Exchange Online PowerShell pour rechercher dans le journal d’audit de la boîte aux lettres de l’utilisateur des enregistrements datant de plus de 90 jours.

- Si vous avez modifié la propriété *AuditLogAgeLimit* d’une boîte aux lettres avant que l’audit des boîtes aux lettres soit activé par défaut pour l’organisation, la limite d’âge de journal d’audit existante de la boîte aux lettres n’est pas modifiée. En d’autres termes, l’audit de boîte aux lettres sur par défaut n’a pas d’effet sur la limite d’âge actuelle pour les enregistrements d’audit de boîte aux lettres.

- Pour modifier la valeur *AuditLogAgeLimit* sur une boîte aux lettres de groupe Office 365, vous devez `-GroupMailbox` inclure le commutateur dans la commande **Set-Mailbox** .

- Les enregistrements du journal d’audit de boîte aux lettres sont stockés ** dans un sous-dossier (nommé audits) dans le dossier éléments récupérables de la boîte aux lettres de chaque utilisateur. Gardez les points suivants à l’esprit concernant les enregistrements d’audit de boîte aux lettres et le dossier éléments récupérables:

  - Les enregistrements d’audit de boîte aux lettres comptent sur le quota de stockage du dossier éléments récupérables, qui est de 30 Go par défaut (le quota d’avertissement est de 20 Go). Le quota de stockage est automatiquement augmenté jusqu’à 100 Go (avec un quota d’avertissement de 90 Go) dans les cas suivants:

    - Une boîte aux lettres est placée en conservation.

    - La boîte aux lettres est affectée à une stratégie de rétention dans le centre de conformité.

  - Les enregistrements d’audit de boîte aux lettres sont également décomptés par rapport à la [limite de dossiers pour le dossier éléments récupérables](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#mailbox-folder-limits). Un nombre maximal de 3 millions éléments (enregistrements d’audit) peut être stocké dans le sous-dossier audits.

    > [!NOTE]
    > Il est peu probable que l’audit de boîte aux lettres par défaut ait un impact sur le quota de stockage ou le nombre maximal de dossiers pour le dossier éléments récupérables.

    - Vous pouvez exécuter la commande suivante dans Exchange Online PowerShell pour afficher la taille et le nombre d’éléments dans le sous-dossier audits du dossier éléments récupérables:

      ```
      Get-MailboxFolderStatistics -Identity <MailboxIdentity> -FolderScope RecoverableItems | Where-Object {$_.Name -eq 'Audits'} | Format-List FolderPath,FolderSize,ItemsInFolder
      ```

    - Vous ne pouvez pas accéder directement à un enregistrement de journal d’audit dans le dossier éléments récupérables; à la place, vous utilisez la cmdlet **Search-MailboxAuditLog** ou recherchez dans le journal d’audit Office 365 pour rechercher et afficher des enregistrements d’audit de boîte aux lettres.

- Si une boîte aux lettres est placée en conservation ou affectée à une stratégie de rétention dans le centre de conformité, les enregistrements du journal d’audit sont toujours conservés pendant la durée définie par la propriété *AuditLogAgeLimit* de la boîte aux lettres (90 jours par défaut). Pour conserver les enregistrements du journal d’audit plus longtemps pour les boîtes aux lettres en attente, vous devez augmenter la valeur *AuditLogAgeLimit* de la boîte aux lettres.
