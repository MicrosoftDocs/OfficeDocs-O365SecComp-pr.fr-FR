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
description: Vous pouvez utiliser l’outil de recherche de journal d’audit Office 365 pour vous aider à résoudre les problèmes courants, tels que l’étude d’un compte compromis ou la définition du transfert de courrier pour une boîte aux lettres.
ms.openlocfilehash: e5c043668d73bdff30dfce962962a015a6748949
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155676"
---
# <a name="search-the-office-365-audit-log-to-troubleshoot-common-scenarios"></a>Effectuer des recherches dans le journal d’audit Office 365 pour résoudre les scénarios courants

Cet article explique comment utiliser l’outil de recherche de journal d’audit Office 365 pour vous aider à résoudre les scénarios de prise en charge courants. Cela inclut l’utilisation du journal d’audit pour:

- Rechercher l’adresse IP de l’ordinateur utilisé pour accéder à un compte compromis
- Déterminer qui a configuré le transfert de courrier pour une boîte aux lettres
- Déterminer si un utilisateur a supprimé des éléments de courrier électronique dans leur boîte aux lettres
- Déterminer si un utilisateur a créé une règle de boîte de réception

## <a name="using-the-office-365-audit-log-search-tool"></a>Utilisation de l’outil de recherche de journal d’audit Office 365

Chacun des scénarios de dépannage décrits dans cet article est basé sur l’utilisation de l’outil de recherche de journal d’audit dans le centre de sécurité et conformité Office 365. Cette section répertorie les autorisations requises pour effectuer des recherches dans le journal d’audit et décrit les étapes permettant d’accéder aux recherches dans le journal d’audit et de les exécuter. Chaque section de scénario fournit des instructions spécifiques sur la configuration d’une requête de recherche de journal d’audit et sur ce qu’il faut rechercher dans les informations détaillées des enregistrements d’audit qui correspondent aux critères de recherche.

### <a name="permissions-required-to-use-the-audit-log-search-tool"></a>Autorisations requises pour utiliser l’outil de recherche de journal d’audit

Vous devez disposer du rôle journaux d’audit en affichage seul ou journaux d’audit dans Exchange Online pour effectuer des recherches dans le journal d’audit Office 365. Par défaut, ces rôles sont attribués aux groupes de rôles gestion de la conformité et gestion de l’organisation dans la page **autorisations** du centre d’administration Exchange. Notez que les administrateurs globaux dans Office 365 et Microsoft 365 sont automatiquement ajoutés en tant que membres du groupe de rôles gestion de l’organisation dans Exchange Online. Pour plus d’informations, consultez la rubrique [gérer des groupes de rôles dans Exchange Online](https://go.microsoft.com/fwlink/p/?LinkID=730688).

### <a name="running-audit-log-searches"></a>Exécution de recherches dans le journal d’audit

Cette section décrit les notions de base pour la création et l’exécution de recherches dans le journal d’audit. Utilisez ces instructions comme point de départ pour chaque scénario de dépannage dans cet article. Pour obtenir des instructions détaillées détaillées, consultez [la rubrique Search the audit log](search-the-audit-log-in-security-and-compliance.md#step-1-run-an-audit-log-search).

1. Accédez à [https://protection.office.com/unifiedauditlog](https://protection.office.com/unifiedauditlog) et connectez-vous à l’aide de votre compte professionnel ou scolaire.
    
    La page **recherche du journal d’audit** s’affiche. 
    
    ![Configurez les critères, puis cliquez sur Rechercher pour exécuter la recherche.](media/8639d09c-2843-44e4-8b4b-9f45974ff7f1.png)
  
4. Vous pouvez configurer les critères de recherche suivants. Notez que chaque scénario de dépannage dans cet article recommande des instructions spécifiques pour la configuration de ces champs.
    
    a. **Activités** : cliquez sur la liste déroulante pour afficher les activités que vous pouvez rechercher. Après l’exécution de la recherche, seuls les enregistrements d’audit des activités sélectionnées sont affichés. Sélectionnez **afficher les résultats pour toutes les activités** pour afficher les résultats de toutes les activités qui répondent aux autres critères de recherche. Vous devrez également laisser ce champ vide dans certains scénarios de dépannage.
    
    b. **Date de début** et **Date de fin** : sélectionnez une date et une plage horaire pour afficher les événements qui se sont produits au cours de cette période. Les sept derniers jours sont sélectionnés par défaut. La date et l’heure sont présentées au format UTC (Coordinated Universal Time). La plage de dates maximale que vous pouvez spécifier est de 90 jours.

    c. **Utilisateurs** : cliquez dans cette zone, puis sélectionnez un ou plusieurs utilisateurs pour lesquels afficher les résultats de la recherche. Les enregistrements d’audit de l’activité sélectionnée effectuée par les utilisateurs que vous sélectionnez dans cette zone sont affichés dans la liste des résultats. Laissez cette zone vide pour renvoyer les entrées de tous les utilisateurs (et comptes de service) de votre organisation.
    
    d. **Fichier, dossier ou site** : entrez une partie ou la totalité d’un nom de fichier ou de dossier pour Rechercher l’activité liée au fichier de dossier qui contient le mot clé spécifié. Vous pouvez également spécifier l’URL d’un fichier ou d’un dossier. Si vous utilisez une URL, vérifiez que vous tapez le chemin d’URL complet ou si vous tapez simplement une partie de l’URL, n’incluez pas de caractères spéciaux ou d’espaces. Laissez cette zone vide pour renvoyer les entrées de tous les fichiers et dossiers de votre organisation. Notez que ce champ est vide dans tous les scénarios de dépannage décrits dans cet article.
    
5. Cliquez sur **Rechercher** pour exécuter la recherche à l’aide de vos critères de recherche. 
    
    Les résultats de la recherche sont chargés et, après quelques instants, s’affichent sous **résultats** dans la page **recherche du journal d’audit** . Chacune des sections suivantes fournit des instructions sur les éléments à rechercher pour le scénario de dépannage spécifique.

    Pour plus d’informations sur l’affichage, le filtrage ou l’exportation des résultats de la recherche du journal d’audit, voir:

    - [Afficher les résultats de la recherche](search-the-audit-log-in-security-and-compliance.md#step-2-view-the-search-results)
    - [Filtrer les résultats de la recherche](search-the-audit-log-in-security-and-compliance.md#step-3-filter-the-search-results)
    - [Exporter les résultats de la recherche](search-the-audit-log-in-security-and-compliance.md#step-4-export-the-search-results-to-a-file)

## <a name="finding-the-ip-address-of-the-computer-used-to-access-a-compromised-account"></a>Recherche de l’adresse IP de l’ordinateur utilisé pour accéder à un compte compromis

L’adresse IP correspondant à une activité effectuée par un utilisateur est incluse dans la plupart des enregistrements d’audit. Les informations sur le client utilisé sont également incluses dans l’enregistrement d’audit.

Voici comment configurer une requête de recherche de journal d’audit pour ce scénario:

**Activités** : si cela s’applique à votre cas, sélectionnez une activité spécifique à rechercher. Pour résoudre les problèmes de comptes compromis, sélectionnez l’activité **connexion à la boîte aux lettres** sous **activités des boîtes aux lettres Exchange**. Cette opération renverra des enregistrements d’audit indiquant l’adresse IP utilisée lors de la connexion à la boîte aux lettres. Dans le cas contraire, laissez ce champ vide pour renvoyer les enregistrements d’audit de toutes les activités. 

> [!TIP]
> Le fait de laisser ce champ vide renverra les activités **UserLoggedIn** , qui est une activité Azure Active Directory indiquant qu’une personne s’est connectée à un compte d’utilisateur Office 365. Utilisez le filtrage dans les résultats de la recherche pour afficher les enregistrements d’audit **UserLoggedIn** .

**Date de début** et **Date de fin** : sélectionnez une plage de dates applicable à votre enquête.

**Utilisateurs** : Si vous recherchez un compte compromis, sélectionnez l’utilisateur dont le compte a été compromis. Cette opération renvoie les enregistrements d’audit pour les activités effectuées par ce compte d’utilisateur.

**Fichier, dossier ou site** : laissez ce champ vide.

Après avoir exécuté la recherche, l’adresse IP de chaque activité est affichée dans la colonne **adresse IP** dans les résultats de la recherche. Cliquez sur l’enregistrement dans les résultats de la recherche pour afficher des informations plus détaillées sur la page de menu volant.

## <a name="determining-who-set-up-email-forwarding-for-a-mailbox"></a>Déterminer qui a configuré le transfert de courrier pour une boîte aux lettres

Lorsque le transfert de courrier est configuré pour une boîte aux lettres, les messages électroniques envoyés à la boîte aux lettres sont transférés vers une autre boîte aux lettres. Les messages peuvent être transférés à des utilisateurs à l’intérieur ou à l’extérieur de votre organisation. Lorsque le transfert de courrier est configuré sur une boîte aux lettres, l’applet de commande Exchange Online sous-jacente utilisée est **Set-Mailbox**.

Voici comment configurer une requête de recherche de journal d’audit pour ce scénario:

**Activités** : laissez ce champ vide afin que la recherche renvoie les enregistrements d’audit pour toutes les activités. Cela est nécessaire pour renvoyer les enregistrements d’audit liés à la cmdlet **Set-Mailbox** .

**Date de début** et **Date de fin** : sélectionnez une plage de dates applicable à votre enquête.

**Utilisateurs** -sauf si vous recherchez un problème de transfert de courrier pour un utilisateur spécifique, laissez ce champ vide. Cela vous permettra d’identifier si le transfert des messages a été configuré pour n’importe quel utilisateur.

**Fichier, dossier ou site** : laissez ce champ vide.

Après avoir exécuté la recherche, cliquez sur **Filtrer les résultats** sur la page des résultats de la recherche. Dans la zone située sous en-tête de colonne **activité** , tapez **Set-Mailbox** afin que seuls les enregistrements d’audit liés à la cmdlet **Set-Mailbox** s’affichent.

![Filtrage des résultats d’une recherche de journal d’audit](media/emailforwarding1.png)

À ce stade, vous devez examiner les détails de chaque enregistrement d’audit pour déterminer si l’activité est liée au transfert du courrier. Cliquez sur l’enregistrement d’audit pour afficher la page de menu volant **Détails** , puis cliquez sur **informations supplémentaires**. La capture d’écran et les descriptions suivantes mettent en évidence les informations indiquant que le transfert de courrier a été défini sur la boîte aux lettres.

![Informations détaillées à partir de l’enregistrement d’audit](media/emailforwarding2.png)

a. Dans le champ **ObjectID** , l’alias de la boîte aux lettres sur lequel le transfert de courrier a été activé est affiché. Cette boîte aux lettres est également affichée dans la colonne **élément** de la page des résultats de la recherche.

b. Dans le **** champ Parameters, la valeur *ForwardingSmtpAddress* indique que le transfert de messages a été défini sur la boîte aux lettres. Dans cet exemple, le courrier est transmis à l’adresse de messagerie mike@contoso.com, qui se trouve en dehors de l’organisation alpinehouse.onmicrosoft.com.

c. La valeur *true* pour le paramètre *DeliverToMailboxAndForward* indique qu’une copie du message remis à Sarad@alpinehouse.onmicrosoft.com ** est transférée à l’adresse de messagerie spécifiée par l' *ForwardingSmtpAddress *, qui dans cet exemple est Mike@contoso.com. Si la valeur du paramètre *DeliverToMailboxAndForward* est définie sur *false*, le courrier électronique est uniquement transféré à l’adresse spécifiée par le paramètre *ForwardingSmtpAddress* . Il n’est pas remis à la boîte aux lettres spécifiée dans le champ **ObjectID** .

d. Le champ **userid** indique l’utilisateur qui définit le transfert du courrier électronique sur la boîte aux lettres spécifiée dans le champ de champ **ObjectID** . Cet utilisateur est également affiché dans la colonne **utilisateur** de la page des résultats de la recherche. Dans ce cas, il semble que le propriétaire de la boîte aux lettres définisse le transfert du courrier sur sa boîte aux lettres.

Si vous déterminez que le transfert du courrier ne doit pas être défini sur la boîte aux lettres, vous pouvez le supprimer en exécutant la commande suivante dans Exchange Online PowerShell:

```
Set-Mailbox <mailbox alias> -ForwardingSmtpAddress $null 
```

Pour plus d’informations sur les paramètres liés au transfert de messages, voir l’article [Set-Mailbox](https://docs.microsoft.com/powershell/module/exchange/mailboxes/set-mailbox) .

## <a name="determining-if-a-user-deleted-email-items"></a>Déterminer si un utilisateur a supprimé des éléments de courrier électronique

À compter du 1er janvier 2019, Microsoft Active la journalisation d’audit des boîtes aux lettres par défaut pour toutes les organisations Office 365 et Microsoft. Cela signifie que certaines actions effectuées par les propriétaires de boîtes aux lettres sont automatiquement journalisées et que les enregistrements d’audit de boîte aux lettres correspondants sont disponibles lorsque vous les recherchez dans le journal d’audit de boîte aux lettres. Avant que l’audit des boîtes aux lettres ait été activé par défaut, vous devez l’activer manuellement pour chaque boîte aux lettres d’utilisateur de votre organisation. 

Les actions de boîte aux lettres enregistrées par défaut incluent les actions de boîte aux lettres SoftDelete et HardDelete effectuées par les propriétaires de boîtes aux lettres. Cela signifie que vous pouvez utiliser la procédure suivante pour rechercher dans le journal d’audit des événements liés aux éléments de messagerie supprimés. Pour plus d’informations sur l’audit des boîtes aux lettres par défaut, consultez la rubrique [Manage Mailbox Auditing](enable-mailbox-auditing.md).

Voici comment configurer une requête de recherche de journal d’audit pour ce scénario:

**Activités** -sous **activités de boîte aux lettres Exchange**, sélectionnez l’une des activités suivantes ou les deux:

- **Messages supprimés du dossier éléments supprimés** : cette activité correspond à l’action d’audit de boîte aux lettres **SoftDelete** . Cette activité est également consignée lorsqu’un utilisateur supprime définitivement un élément en le sélectionnant et en appuyant sur **MAJ + SUPPR**. Une fois qu’un élément est supprimé définitivement, l’utilisateur peut le récupérer jusqu’à ce que la période de rétention des éléments supprimés expire.

- **Messages purgés de la boîte aux lettres** : cette activité correspond à l’action d’audit de boîte aux lettres **HardDelete** . Cette option est enregistrée lorsqu’un utilisateur supprime un élément du dossier éléments récupérables. Les administrateurs peuvent utiliser l’outil de recherche de contenu dans le centre de sécurité et de conformité pour rechercher et récupérer les éléments purgés jusqu’à ce que la période de rétention des éléments supprimés expire ou plus si la boîte aux lettres de l’utilisateur est en conservation.

**Date de début** et **Date de fin** : sélectionnez une plage de dates applicable à votre enquête.

**Utilisateurs** : Si vous sélectionnez un utilisateur dans ce champ, l’outil de recherche de journal d’audit renverra des enregistrements d’audit pour les éléments de courrier électronique qui ont été supprimés (SoftDeleted ou HardDeleted) par l’utilisateur que vous spécifiez. Dans certains cas, l’utilisateur qui supprime un courrier électronique n’est peut-être pas le propriétaire de la boîte aux lettres.

**Fichier, dossier ou site** : laissez ce champ vide.

Après avoir exécuté la recherche, vous pouvez filtrer les résultats de la recherche pour afficher les enregistrements d’audit pour les éléments supprimés de manière récupérable ou pour les éléments supprimés définitivement. Cliquez sur l’enregistrement d’audit pour afficher la page de menu volant **Détails** , puis cliquez sur **informations supplémentaires**. Des informations supplémentaires sur l’élément supprimé, telles que la ligne d’objet et l’emplacement de l’élément lors de sa suppression, sont affichées dans le champ **AffectedItems** . Les captures d’écran suivantes illustrent un exemple de champ **AffectedItems** provenant d’un élément supprimé (récupérable) et d’un élément supprimé de manière irréversible.

**Exemple de champ AffectedItems pour un élément supprimé (récupérable)**

![Enregistrement d’audit pour l’élément supprimé (récupérable)](media/softdeleteditem.png)

**Exemple de champ AffectedItems pour un élément supprimé de manière irréversible**

![Enregistrement d’audit pour un élément de courrier supprimé de manière irréversible](media/harddeleteditem.png)

### <a name="recovering-deleted-email-items"></a>Restaurer des éléments de courrier électronique supprimés

Les utilisateurs peuvent récupérer des éléments supprimés de manière récupérable si la période de rétention des éléments supprimés n’a pas expiré. Dans Exchange Online, la période de rétention des éléments supprimés par défaut est de 14 jours, mais les administrateurs peuvent augmenter ce paramètre à un maximum de 30 jours. Pointez les utilisateurs vers l’article [récupérer les éléments supprimés ou le courrier électronique dans Outlook sur le Web](https://support.office.com/article/Recover-deleted-items-or-email-in-Outlook-Web-App-C3D8FC15-EEEF-4F1C-81DF-E27964B7EDD4) pour obtenir des instructions sur la récupération des éléments supprimés.

Comme expliqué précédemment, les administrateurs peuvent être en mesure de récupérer des éléments supprimés définitivement si la période de rétention des éléments supprimés n’a pas expiré ou si la boîte aux lettres est en conservation, auquel cas les éléments sont conservés jusqu’à l’expiration de la durée de la conservation. Lorsque vous exécutez une recherche de contenu, les éléments supprimés et supprimés définitivement dans le dossier éléments récupérables sont renvoyés dans les résultats de la recherche s’ils correspondent à la requête de recherche. Pour plus d’informations sur l’exécution des recherches de contenu, consultez la rubrique [recherche de contenu dans Office 365](content-search.md).

> [!TIP]
> Pour rechercher des éléments de courrier électronique supprimés, recherchez tout ou partie de la ligne d’objet qui s’affiche dans le champ **AffectedItems** de l’enregistrement d’audit.

## <a name="determining-if-a-user-created-an-inbox-rule"></a>Déterminer si un utilisateur a créé une règle de boîte de réception

Lorsque les utilisateurs créent une règle de boîte de réception pour leur boîte aux lettres Exchange Online, un enregistrement d’audit correspondant est enregistré dans le journal d’audit. Pour plus d’informations sur les règles de boîte de réception, voir:

- [Utiliser des règles de boîte de réception dans Outlook sur le Web](https://support.office.com/article/use-inbox-rules-in-outlook-on-the-web-8400435c-f14e-4272-9004-1548bb1848f2)
- [Gérer les messages électroniques dans Outlook à l’aide de règles](https://support.office.com/article/Manage-email-messages-by-using-rules-C24F5DEA-9465-4DF4-AD17-A50704D66C59)

Voici comment configurer une requête de recherche de journal d’audit pour ce scénario:

**Activités** -sous **activités de boîte aux lettres Exchange**, sélectionnez **nouveau-InboxRule créer/modifier/activer/désactiver la règle de boîte de réception**.

**Date de début** et **Date de fin** : sélectionnez une plage de dates applicable à votre enquête.

**Utilisateurs** : sauf si vous recherchez un utilisateur spécifique, laissez ce champ vide. Cela vous permettra d’identifier les nouvelles règles de boîte de réception configurées par un utilisateur.

**Fichier, dossier ou site** : laissez ce champ vide.

Après avoir exécuté la recherche, tous les enregistrements d’audit de cette activité sont affichés dans les résultats de la recherche. Cliquez sur un enregistrement d’audit pour afficher la page de menu volant **Détails** , puis cliquez sur **informations supplémentaires**. Les informations sur les paramètres des règles de boîte de réception sont affichées dans le champ **paramètres** . La capture d’écran et les descriptions suivantes mettent en évidence les informations relatives aux règles de boîte de réception.

![Enregistrement d’audit pour la nouvelle règle de boîte de réception](media/NewInboxRuleRecord.png)

a. Dans le champ **ObjectID** , le nom complet de la règle de boîte de réception est affiché. Ce nom inclut l’alias de la boîte aux lettres de l’utilisateur (par exemple, Sarad) et le nom de la règle de boîte de réception (par exemple, «Move messages from admin»).

b. Dans le champ **paramètres** , la condition de la règle de boîte de réception est affichée. Dans cet exemple, la condition est spécifiée par le paramètre *from* . La valeur définie pour le paramètre *from* indique que la règle de boîte de réception agit sur les messages envoyés par admin@alpinehouse.onmicrosoft.com. Pour obtenir la liste complète des paramètres qui peuvent être utilisés pour définir les conditions des règles de boîte de réception, consultez l’article [New-InboxRule](https://docs.microsoft.com/powershell/module/exchange/mailboxes/new-inboxrule) .

c. Le paramètre *MoveToFolder* spécifie l’action pour la règle de boîte de réception; dans cet exemple, les messages reçus à partir de admin@alpinehouse.onmicrosoft.com sont déplacés vers le dossier nommé *AdminSearch*. Consultez également l’article [New-InboxRule](https://docs.microsoft.com/powershell/module/exchange/mailboxes/new-inboxrule) pour obtenir la liste complète des paramètres permettant de définir l’action d’une règle de boîte de réception.

d. Le champ **userid** indique l’utilisateur qui a créé la règle de boîte de réception spécifiée dans le champ **ObjectID** . Cet utilisateur est également affiché dans la colonne **utilisateur** de la page des résultats de la recherche.