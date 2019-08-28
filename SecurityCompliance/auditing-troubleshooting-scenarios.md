---
title: Effectuer des recherches dans le journal d’audit Office 365 pour résoudre les scénarios courants
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
- MET150
- MOE150
description: Vous pouvez utiliser l’outil de recherche de journal d’audit Office 365 pour vous aider à résoudre les problèmes courants, tels que l’enquête sur un compte compromis, la configuration du transfert de courrier pour une boîte aux lettres ou la détermination de la raison pour laquelle un utilisateur externe a réussi à se connecter à votre Département.
ms.openlocfilehash: 255fd323ca08dd4ea759648fbe0673f5e5254c22
ms.sourcegitcommit: 1947ad3c0dde9163ba9b6834d8b38bd04b4264a5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2019
ms.locfileid: "36643282"
---
# <a name="search-the-office-365-audit-log-to-troubleshoot-common-scenarios"></a>Effectuer des recherches dans le journal d’audit Office 365 pour résoudre les scénarios courants

Cet article explique comment utiliser l’outil de recherche de journal d’audit Office 365 pour vous aider à résoudre les scénarios de prise en charge courants. Cela inclut l’utilisation du journal d’audit pour:

- Rechercher l’adresse IP de l’ordinateur utilisé pour accéder à un compte compromis
- Déterminer qui a configuré le transfert de courrier pour une boîte aux lettres
- Déterminer si un utilisateur a supprimé des éléments de courrier électronique dans leur boîte aux lettres
- Déterminer si un utilisateur a créé une règle de boîte de réception
- Identifier la raison pour laquelle un utilisateur a réussi à se connecter à l’extérieur de votre organisation

## <a name="using-the-office-365-audit-log-search-tool"></a>Utilisation de l’outil de recherche de journal d’audit Office 365

Chacun des scénarios de dépannage décrits dans cet article est basé sur l’utilisation de l’outil de recherche de journal d’audit dans le centre de sécurité et conformité Office 365. Cette section répertorie les autorisations requises pour effectuer des recherches dans le journal d’audit et décrit les étapes permettant d’accéder aux recherches dans le journal d’audit et de les exécuter. Chaque section de scénario fournit des instructions spécifiques sur la configuration d’une requête de recherche de journal d’audit et sur ce qu’il faut rechercher dans les informations détaillées des enregistrements d’audit qui correspondent aux critères de recherche.

### <a name="permissions-required-to-use-the-audit-log-search-tool"></a>Autorisations requises pour utiliser l’outil de recherche de journal d’audit

Vous devez disposer du rôle journaux d’audit en affichage seul ou journaux d’audit dans Exchange Online pour effectuer des recherches dans le journal d’audit Office 365. Par défaut, ces rôles sont attribués aux groupes de rôles gestion de la conformité et gestion de l’organisation dans la page **autorisations** du centre d’administration Exchange. Les administrateurs globaux dans Office 365 et Microsoft 365 sont automatiquement ajoutés en tant que membres du groupe de rôles gestion de l’organisation dans Exchange Online. Pour plus d’informations, consultez la rubrique [gérer des groupes de rôles dans Exchange Online](https://go.microsoft.com/fwlink/p/?LinkID=730688).

### <a name="running-audit-log-searches"></a>Exécution de recherches dans le journal d’audit

Cette section décrit les notions de base pour la création et l’exécution de recherches dans le journal d’audit. Utilisez ces instructions comme point de départ pour chaque scénario de dépannage dans cet article. Pour obtenir des instructions détaillées détaillées, consultez [la rubrique Search the audit log](search-the-audit-log-in-security-and-compliance.md#step-1-run-an-audit-log-search).

1. Accédez à [https://protection.office.com/unifiedauditlog](https://protection.office.com/unifiedauditlog) et connectez-vous à l’aide de votre compte professionnel ou scolaire.
    
    La page **recherche du journal d’audit** s’affiche. 
    
    ![Configurez les critères, puis cliquez sur Rechercher pour exécuter la recherche.](media/8639d09c-2843-44e4-8b4b-9f45974ff7f1.png)
  
4. Vous pouvez configurer les critères de recherche suivants. Chaque scénario de dépannage de cet article recommande des instructions spécifiques pour la configuration de ces champs.
    
    a. **Activités:** Cliquez sur la liste déroulante pour afficher les activités que vous pouvez rechercher. Après l’exécution de la recherche, seuls les enregistrements d’audit des activités sélectionnées sont affichés. La sélection de l’option **afficher les résultats pour toutes les activités** affiche les résultats de toutes les activités qui répondent aux autres critères de recherche. Vous devrez également laisser ce champ vide dans certains scénarios de dépannage.
    
    b. **Date de début** et **Date de fin:** sélectionnez une date et une plage horaire pour afficher les événements qui se sont produits au cours de cette période. Les sept derniers jours sont sélectionnés par défaut. La date et l’heure sont présentées au format UTC (Coordinated Universal Time). La plage de dates maximale que vous pouvez spécifier est de 90 jours.

    c. **Utilisateurs:** Cliquez dans cette zone, puis sélectionnez un ou plusieurs utilisateurs pour lesquels vous souhaitez afficher les résultats de la recherche. Les enregistrements d’audit de l’activité sélectionnée effectuée par les utilisateurs que vous sélectionnez dans cette zone sont affichés dans la liste des résultats. Laissez cette zone vide pour renvoyer les entrées de tous les utilisateurs (et comptes de service) de votre organisation.
    
    d. **Fichier, dossier ou site:** Tapez une partie ou la totalité d’un nom de fichier ou de dossier pour Rechercher l’activité liée au fichier du dossier qui contient le mot clé spécifié. Vous pouvez également spécifier l’URL d’un fichier ou d’un dossier. Si vous utilisez une URL, vérifiez que vous tapez le chemin d’URL complet ou, si vous ne tapez qu’une partie de l’URL, n’incluez pas de caractères spéciaux ou d’espaces. Laissez cette zone vide pour renvoyer les entrées de tous les fichiers et dossiers de votre organisation. Ce champ est vide dans tous les scénarios de dépannage décrits dans cet article.
    
5. Cliquez sur **Rechercher** pour exécuter la recherche à l’aide de vos critères de recherche. 
    
    Les résultats de la recherche sont chargés et, après quelques instants, s’affichent sous **résultats** dans la page **recherche du journal d’audit** . Chacune des sections de cet article fournit des instructions sur les éléments à rechercher dans le contexte du scénario de dépannage spécifique.

    Pour plus d’informations sur l’affichage, le filtrage ou l’exportation des résultats de la recherche du journal d’audit, voir:

    - [Afficher les résultats de la recherche](search-the-audit-log-in-security-and-compliance.md#step-2-view-the-search-results)
    - [Filtrer les résultats de la recherche](search-the-audit-log-in-security-and-compliance.md#step-3-filter-the-search-results)
    - [Exporter les résultats de la recherche](search-the-audit-log-in-security-and-compliance.md#step-4-export-the-search-results-to-a-file)

## <a name="find-the-ip-address-of-the-computer-used-to-access-a-compromised-account"></a>Rechercher l’adresse IP de l’ordinateur utilisé pour accéder à un compte compromis

L’adresse IP correspondant à une activité effectuée par un utilisateur est incluse dans la plupart des enregistrements d’audit. Les informations sur le client utilisé sont également incluses dans l’enregistrement d’audit.

Voici comment configurer une requête de recherche de journal d’audit pour ce scénario:

**Activités:** Si cela s’applique à votre cas, sélectionnez une activité spécifique à rechercher. Pour résoudre les problèmes de comptes compromis, sélectionnez l’activité **connexion à la boîte aux lettres** sous **activités des boîtes aux lettres Exchange**. Renvoie les enregistrements d’audit indiquant l’adresse IP utilisée lors de la connexion à la boîte aux lettres. Dans le cas contraire, laissez ce champ vide pour renvoyer les enregistrements d’audit de toutes les activités. 

> [!TIP]
> Le fait de laisser ce champ vide renverra les activités **UserLoggedIn** , qui est une activité Azure Active Directory indiquant qu’une personne s’est connectée à un compte d’utilisateur Office 365. Utilisez le filtrage dans les résultats de la recherche pour afficher les enregistrements d’audit **UserLoggedIn** .

**Date de début** et **Date de fin:** sélectionnez une plage de dates applicable à votre enquête.

**Utilisateurs:** Si vous recherchez un compte compromis, sélectionnez l’utilisateur dont le compte a été compromis. Cette opération renvoie les enregistrements d’audit pour les activités effectuées par ce compte d’utilisateur.

**Fichier, dossier ou site:** Laissez ce champ vide.

Après avoir exécuté la recherche, l’adresse IP de chaque activité est affichée dans la colonne **adresse IP** dans les résultats de la recherche. Cliquez sur l’enregistrement dans les résultats de la recherche pour afficher des informations plus détaillées sur la page de menu volant.

## <a name="determine-who-set-up-email-forwarding-for-a-mailbox"></a>Déterminer qui a configuré le transfert de courrier pour une boîte aux lettres

Lorsque le transfert de courrier est configuré pour une boîte aux lettres, les messages électroniques envoyés à la boîte aux lettres sont transférés vers une autre boîte aux lettres. Les messages peuvent être transférés à des utilisateurs à l’intérieur ou à l’extérieur de votre organisation. Lorsque le transfert de courrier est configuré sur une boîte aux lettres, l’applet de commande Exchange Online sous-jacente utilisée est **Set-Mailbox**.

Voici comment configurer une requête de recherche de journal d’audit pour ce scénario:

**Activités:** Laissez ce champ vide afin que la recherche renvoie les enregistrements d’audit pour toutes les activités. Cela est nécessaire pour renvoyer les enregistrements d’audit liés à la cmdlet **Set-Mailbox** .

**Date de début** et **Date de fin:** sélectionnez une plage de dates applicable à votre enquête.

**Utilisateurs:** Sauf si vous recherchez un problème de transfert de courrier pour un utilisateur spécifique, laissez ce champ vide. Cela vous permet d’identifier si le transfert des messages a été configuré pour n’importe quel utilisateur.

**Fichier, dossier ou site:** Laissez ce champ vide.

Après avoir exécuté la recherche, cliquez sur **Filtrer les résultats** sur la page des résultats de la recherche. Dans la zone située sous en-tête de colonne **activité** , tapez **Set-Mailbox** afin que seuls les enregistrements d’audit liés à la cmdlet **Set-Mailbox** s’affichent.

![Filtrage des résultats d’une recherche de journal d’audit](media/emailforwarding1.png)

À ce stade, vous devez examiner les détails de chaque enregistrement d’audit pour déterminer si l’activité est liée au transfert du courrier. Cliquez sur l’enregistrement d’audit pour afficher la page de menu volant **Détails** , puis cliquez sur **informations supplémentaires**. La capture d’écran et les descriptions suivantes mettent en évidence les informations indiquant que le transfert de courrier a été défini sur la boîte aux lettres.

![Informations détaillées à partir de l’enregistrement d’audit](media/emailforwarding2.png)

a. Dans le champ **ObjectID** , l’alias de la boîte aux lettres sur lequel le transfert de courrier a été activé est affiché. Cette boîte aux lettres est également affichée dans la colonne **élément** de la page des résultats de la recherche.

b. Dans le **** champ Parameters, la valeur *ForwardingSmtpAddress* indique que le transfert de courrier électronique a été défini sur la boîte aux lettres. Dans cet exemple, le courrier est transmis à l’adresse de messagerie mike@contoso.com, qui se trouve en dehors de l’organisation alpinehouse.onmicrosoft.com.

c. La valeur *true* pour le paramètre *DeliverToMailboxAndForward* indique qu’une copie du message remis à Sarad@alpinehouse.onmicrosoft.com ** est transférée à l’adresse de messagerie spécifiée par l' *ForwardingSmtpAddress *, qui dans cet exemple est Mike@contoso.com. Si la valeur du paramètre *DeliverToMailboxAndForward* est définie sur *false*, le courrier électronique est uniquement transféré à l’adresse spécifiée par le paramètre *ForwardingSmtpAddress* . Il n’est pas remis à la boîte aux lettres spécifiée dans le champ **ObjectID** .

d. Le champ **userid** indique l’utilisateur qui définit le transfert du courrier électronique sur la boîte aux lettres spécifiée dans le champ **ObjectID** . Cet utilisateur est également affiché dans la colonne **utilisateur** de la page des résultats de la recherche. Dans ce cas, il semble que le propriétaire de la boîte aux lettres définisse le transfert du courrier sur sa boîte aux lettres.

Si vous déterminez que le transfert du courrier ne doit pas être défini sur la boîte aux lettres, vous pouvez le supprimer en exécutant la commande suivante dans Exchange Online PowerShell:

```
Set-Mailbox <mailbox alias> -ForwardingSmtpAddress $null 
```

Pour plus d’informations sur les paramètres liés au transfert de messages, voir l’article [Set-Mailbox](https://docs.microsoft.com/powershell/module/exchange/mailboxes/set-mailbox) .

## <a name="determine-if-a-user-deleted-email-items"></a>Déterminer si un utilisateur a supprimé des éléments de courrier électronique

À compter du 1er janvier 2019, Microsoft Active la journalisation d’audit des boîtes aux lettres par défaut pour toutes les organisations Office 365 et Microsoft. Cela signifie que certaines actions effectuées par les propriétaires de boîtes aux lettres sont automatiquement journalisées et que les enregistrements d’audit de boîte aux lettres correspondants sont disponibles lorsque vous les recherchez dans le journal d’audit de boîte aux lettres. Avant que l’audit des boîtes aux lettres ait été activé par défaut, vous devez l’activer manuellement pour chaque boîte aux lettres d’utilisateur de votre organisation. 

Les actions de boîte aux lettres enregistrées par défaut incluent les actions de boîte aux lettres SoftDelete et HardDelete effectuées par les propriétaires de boîtes aux lettres. Cela signifie que vous pouvez utiliser les étapes suivantes pour rechercher dans le journal d’audit des événements liés aux éléments de messagerie supprimés. Pour plus d’informations sur l’audit des boîtes aux lettres par défaut, consultez la rubrique [Manage Mailbox Auditing](enable-mailbox-auditing.md).

Voici comment configurer une requête de recherche de journal d’audit pour ce scénario:

**Activités:** Sous **activités de boîte aux lettres Exchange**, sélectionnez l’une des activités suivantes ou les deux:

- **Messages supprimés du dossier éléments supprimés:** Cette activité correspond à l’action d’audit de boîte aux lettres **SoftDelete** . Cette activité est également consignée lorsqu’un utilisateur supprime définitivement un élément en le sélectionnant et en appuyant sur **MAJ + SUPPR**. Une fois qu’un élément est supprimé définitivement, l’utilisateur peut le récupérer jusqu’à ce que la période de rétention des éléments supprimés expire.

- **Messages supprimés de la boîte aux lettres:** Cette activité correspond à l’action d’audit de boîte aux lettres **HardDelete** . Cette option est enregistrée lorsqu’un utilisateur supprime un élément du dossier éléments récupérables. Les administrateurs peuvent utiliser l’outil de recherche de contenu dans le centre de sécurité et de conformité pour rechercher et récupérer les éléments purgés jusqu’à ce que la période de rétention des éléments supprimés expire ou plus si la boîte aux lettres de l’utilisateur est en conservation.

**Date de début** et **Date de fin:** sélectionnez une plage de dates applicable à votre enquête.

**Utilisateurs:** Si vous sélectionnez un utilisateur dans ce champ, l’outil de recherche de journal d’audit renvoie les enregistrements d’audit pour les éléments de courrier électronique qui ont été supprimés (SoftDeleted ou HardDeleted) par l’utilisateur que vous spécifiez. Parfois, l’utilisateur qui supprime un courrier électronique n’est peut-être pas le propriétaire de la boîte aux lettres.

**Fichier, dossier ou site:** Laissez ce champ vide.

Après avoir exécuté la recherche, vous pouvez filtrer les résultats de la recherche pour afficher les enregistrements d’audit pour les éléments supprimés de manière récupérable ou pour les éléments supprimés définitivement. Cliquez sur l’enregistrement d’audit pour afficher la page de menu volant **Détails** , puis cliquez sur **informations supplémentaires**. Des informations supplémentaires sur l’élément supprimé, telles que la ligne d’objet et l’emplacement de l’élément lors de sa suppression, sont affichées dans le champ **AffectedItems** . Les captures d’écran suivantes illustrent un exemple de champ **AffectedItems** provenant d’un élément supprimé (récupérable) et d’un élément supprimé de manière irréversible.

**Exemple de champ AffectedItems pour un élément supprimé (récupérable)**

![Enregistrement d’audit pour l’élément supprimé (récupérable)](media/softdeleteditem.png)

**Exemple de champ AffectedItems pour un élément supprimé de manière irréversible**

![Enregistrement d’audit pour un élément de courrier supprimé de manière irréversible](media/harddeleteditem.png)

### <a name="recover-deleted-email-items"></a>Récupérer des éléments de courrier électronique supprimés

Les utilisateurs peuvent récupérer des éléments supprimés de manière récupérable si la période de rétention des éléments supprimés n’a pas expiré. Dans Exchange Online, la période de rétention des éléments supprimés par défaut est de 14 jours, mais les administrateurs peuvent augmenter ce paramètre à un maximum de 30 jours. Pointez les utilisateurs vers l’article [récupérer les éléments supprimés ou le courrier électronique dans Outlook sur le Web](https://support.office.com/article/Recover-deleted-items-or-email-in-Outlook-Web-App-C3D8FC15-EEEF-4F1C-81DF-E27964B7EDD4) pour obtenir des instructions sur la récupération des éléments supprimés.

Comme expliqué précédemment, les administrateurs peuvent être en mesure de récupérer des éléments supprimés définitivement si la période de rétention des éléments supprimés n’a pas expiré ou si la boîte aux lettres est en conservation, auquel cas les éléments sont conservés jusqu’à l’expiration de la durée de la conservation. Lorsque vous exécutez une recherche de contenu, les éléments supprimés et supprimés définitivement dans le dossier éléments récupérables sont renvoyés dans les résultats de la recherche s’ils correspondent à la requête de recherche. Pour plus d’informations sur l’exécution des recherches de contenu, consultez la rubrique [recherche de contenu dans Office 365](content-search.md).

> [!TIP]
> Pour rechercher des éléments de courrier électronique supprimés, recherchez tout ou partie de la ligne d’objet qui s’affiche dans le champ **AffectedItems** de l’enregistrement d’audit.

## <a name="determine-if-a-user-created-an-inbox-rule"></a>Déterminer si un utilisateur a créé une règle de boîte de réception

Lorsque les utilisateurs créent une règle de boîte de réception pour leur boîte aux lettres Exchange Online, un enregistrement d’audit correspondant est enregistré dans le journal d’audit. Pour plus d’informations sur les règles de boîte de réception, voir:

- [Utiliser des règles de boîte de réception dans Outlook sur le Web](https://support.office.com/article/use-inbox-rules-in-outlook-on-the-web-8400435c-f14e-4272-9004-1548bb1848f2)
- [Gérer les messages électroniques dans Outlook à l’aide de règles](https://support.office.com/article/Manage-email-messages-by-using-rules-C24F5DEA-9465-4DF4-AD17-A50704D66C59)

Voici comment configurer une requête de recherche de journal d’audit pour ce scénario:

**Activités:** Sous **activités de boîte aux lettres Exchange**, sélectionnez **nouveau-InboxRule créer/modifier/activer/désactiver la règle de boîte de réception**.

**Date de début** et **Date de fin:** sélectionnez une plage de dates applicable à votre enquête.

**Utilisateurs:** Sauf si vous recherchez un utilisateur spécifique, laissez ce champ vide. Cela vous permet d’identifier les nouvelles règles de boîte de réception configurées par un utilisateur.

**Fichier, dossier ou site:** Laissez ce champ vide.

Après avoir exécuté la recherche, tous les enregistrements d’audit de cette activité sont affichés dans les résultats de la recherche. Cliquez sur un enregistrement d’audit pour afficher la page de menu volant **Détails** , puis cliquez sur **informations supplémentaires**. Les informations sur les paramètres des règles de boîte de réception sont affichées dans le champ **paramètres** . La capture d’écran et les descriptions suivantes mettent en évidence les informations relatives aux règles de boîte de réception.

![Enregistrement d’audit pour la nouvelle règle de boîte de réception](media/NewInboxRuleRecord.png)

a. Dans le champ **ObjectID** , le nom complet de la règle de boîte de réception est affiché. Ce nom inclut l’alias de la boîte aux lettres de l’utilisateur (par exemple, Sarad) et le nom de la règle de boîte de réception (par exemple, «Move messages from admin»).

b. Dans le champ **paramètres** , la condition de la règle de boîte de réception est affichée. Dans cet exemple, la condition est spécifiée par le paramètre *from* . La valeur définie pour le paramètre *from* indique que la règle de boîte de réception agit sur les messages envoyés par admin@alpinehouse.onmicrosoft.com. Pour obtenir la liste complète des paramètres qui peuvent être utilisés pour définir les conditions des règles de boîte de réception, consultez l’article [New-InboxRule](https://docs.microsoft.com/powershell/module/exchange/mailboxes/new-inboxrule) .

c. Le paramètre *MoveToFolder* spécifie l’action pour la règle de boîte de réception. Dans cet exemple, les messages reçus à partir de admin@alpinehouse.onmicrosoft.com sont déplacés vers le dossier nommé *AdminSearch*. Consultez également l’article [New-InboxRule](https://docs.microsoft.com/powershell/module/exchange/mailboxes/new-inboxrule) pour obtenir la liste complète des paramètres permettant de définir l’action d’une règle de boîte de réception.

d. Le champ **userid** indique l’utilisateur qui a créé la règle de boîte de réception spécifiée dans le champ **ObjectID** . Cet utilisateur est également affiché dans la colonne **utilisateur** de la page des résultats de la recherche.

## <a name="investigate-why-there-was-a-successful-login-by-a-user-outside-your-organization"></a>Identifier la raison pour laquelle un utilisateur a réussi à se connecter à l’extérieur de votre organisation

Lors de l’examen des enregistrements d’audit dans le journal d’audit Office 365, vous pouvez voir des enregistrements indiquant qu’un utilisateur externe a été authentifié par Azure Active Directory et a réussi à se connecter à votre organisation. Par exemple, un administrateur dans contoso.onmicrosoft.com peut voir un enregistrement d’audit indiquant qu’un utilisateur d’une autre organisation Office 365 (par exemple, fabrikam.onmicrosoft.com) a réussi à se connecter à contoso.onmicrosoft.com. De même, vous pouvez voir des enregistrements d’audit qui indiquent que les utilisateurs disposant d’un compte Microsoft (MSA), tels qu’un Outlook.com ou Live.com, ont réussi à se connecter à votre organisation. Dans ce cas, l’activité auditée est l' **utilisateur connecté**. 

Ce comportement est par conception. Azure Active Directory (Azure AD), le service d’annuaire dans Office 365, autorise une *authentification directe* lorsqu’un utilisateur externe tente d’accéder à un site SharePoint ou à un emplacement OneDrive de votre organisation. Lorsque l’utilisateur externe tente de le faire, il est invité à entrer ses informations d’identification Office 365. Azure AD utilise les informations d’identification pour authentifier l’utilisateur, ce qui signifie qu’Azure AD vérifie que l’utilisateur est bien ce qu’il dit. L’indication de la connexion réussie dans l’enregistrement d’audit est le résultat de l’authentification de l’utilisateur par Azure AD. La connexion réussie ne signifie pas que l’utilisateur a pu accéder à des ressources ou effectuer d’autres actions dans votre organisation. Il indique uniquement que l’utilisateur a été authentifié par Azure AD. Pour que l’utilisateur direct puisse accéder aux ressources SharePoint ou OneDrive, un utilisateur de votre organisation doit partager explicitement une ressource avec l’utilisateur externe en lui envoyant une invitation de partage ou un lien de partage anonyme. 

> [!NOTE]
> Azure AD autorise l’authentification directe uniquement pour les *applications tierces*, telles que SharePoint Online et OneDrive entreprise. Il n’est pas autorisé pour d’autres applications tierces.

Voici un exemple et des descriptions de propriétés pertinentes dans un enregistrement d’audit pour un événement connecté à un **utilisateur** qui est le résultat de l’authentification directe. Cliquez sur l’enregistrement d’audit pour afficher la page de menu volant **Détails** , puis cliquez sur **informations supplémentaires**.

![Exemple d’enregistrement d’audit pour une authentification relais réussie](media/PassThroughAuth1.png)

   a. Ce champ indique que l’utilisateur qui a tenté d’accéder à une ressource de votre organisation n’a pas été trouvé dans Azure AD de votre organisation.

   b. Ce champ affiche le nom d’utilisateur principal de l’utilisateur externe qui a tenté d’accéder à une ressource de votre organisation. Cet ID d’utilisateur est également identifié dans les propriétés **User** et **userid** de l’enregistrement d’audit.

   c. La propriété **ApplicationID** identifie l’application qui a déclenché la demande d’ouverture de session. La valeur de 00000003-0000-0ff1-CE00-000000000000 affichée dans la propriété ApplicationId de cet enregistrement d’audit indique SharePoint Online. OneDrive entreprise est également associé à ce même ApplicationId.

   d. Cela indique que l’authentification directe a réussi. En d’autres termes, l’utilisateur a été authentifié avec succès par Azure AD. 

   e. La valeur **RecordType** de **15** indique que l’activité auditée (UserLoggedIn) est un événement d’ouverture de session STS (Secure Token Service) dans Azure ad.

Pour plus d’informations sur les autres propriétés affichées dans un enregistrement d’audit UserLoggedIn, voir les informations de schéma liées à Azure AD dans le schéma de l' [API activité de gestion Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#azure-active-directory-base-schema).

Voici deux exemples de scénarios permettant à un utilisateur de se **connecter à** l’aide de l’audit en raison de l’authentification directe: 

  - Un utilisateur disposant d’un compte Microsoft (tel que SaraD@outlook.com) a tenté d’accéder à un document dans un compte OneDrive entreprise dans fourthcoffee.onmicrosoft.com et son n’est pas un compte d’utilisateur invité correspondant pour SaraD@outlook.com dans fourthcoffee.onmicrosoft.com.

  - Un utilisateur disposant d’un compte professionnel ou scolaire dans une organisation Office 365 (par exemple pilarp@fabrikam.onmicrosoft.com) a tenté d’accéder à un site SharePoint dans contoso.onmicrosoft.com et son n’est pas un compte d’utilisateur invité correspondant pour pilarp@fabrikam.com dans contoso.onmicrosoft.com.


### <a name="tips-for-investigating-successful-logins-resulting-from-pass-through-authentication"></a>Conseils pour l’étude des connexions réussies résultant de l’authentification directe

- Recherchez dans le journal d’audit les activités effectuées par l’utilisateur externe identifié dans l’enregistrement d’audit de l' **utilisateur connecté** . Tapez le nom d’utilisateur principal de l’utilisateur externe dans la zone **utilisateurs** et utilisez une plage de dates si cela est approprié à votre scénario. Par exemple, vous pouvez créer une recherche à l’aide des critères de recherche suivants:

   ![Rechercher toutes les activités effectuées par l’utilisateur externe](media/PassThroughAuth2.png)

    En plus des activités de l' **utilisateur connecté** , d’autres enregistrements d’audit peuvent être renvoyés, par exemple ceux qui indiquent qu’un utilisateur de votre organisation a partagé des ressources avec l’utilisateur externe et si l’utilisateur externe a accédé à, modifié ou téléchargé un document qui a été partagé avec eux.

- Recherchez les activités de partage SharePoint qui indiquent qu’un fichier a été partagé avec l’utilisateur externe identifié par un **utilisateur connecté à** un enregistrement d’audit. Pour plus d’informations, reportez-vous à [la rubrique utiliser l’audit de partage dans le journal d’audit Office 365](use-sharing-auditing.md).

- Exportez les résultats de recherche du journal d’audit qui contiennent des enregistrements pertinents pour votre enquête afin que vous puissiez utiliser Excel pour rechercher d’autres activités liées à l’utilisateur externe. Pour plus d’informations, consultez la rubrique [Exporter, configurer et afficher les enregistrements du journal d’audit](export-view-audit-log-records.md).
