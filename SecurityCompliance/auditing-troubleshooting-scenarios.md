---
title: Recherche dans le journal d’audit Office 365 pour résoudre des scénarios courants
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
description: Vous pouvez utiliser l’outil de recherche de journal d’audit Office 365 pour vous aider à résoudre les problèmes courants tels qu’une analyse d’un compte compromis ou savoir qui a configuré le transfert de messages pour une boîte aux lettres.
ms.openlocfilehash: 930e311712e49214ca2a51e256c29e5f959deab8
ms.sourcegitcommit: c34f1a0d560117153fc9a7b8da8994bc6fc53791
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/30/2018
ms.locfileid: "27123897"
---
# <a name="search-the-office-365-audit-log-to-troubleshoot-common-scenarios"></a>Recherche dans le journal d’audit Office 365 pour résoudre des scénarios courants

Cet article décrit comment utiliser l’outil de recherche de journal d’audit Office 365 pour vous aider à résoudre les problèmes de prise en charge des scénarios courants. Cela inclut l’utilisation du journal d’audit pour :

- Rechercher l’adresse IP de l’ordinateur utilisé pour accéder à un compte compromis
- Déterminer qui a configuré le transfert de messages pour une boîte aux lettres
- Déterminer si un utilisateur a supprimé des éléments de messagerie électronique dans leur boîte aux lettres
- Déterminer si un utilisateur créé une règle de boîte de réception

## <a name="using-the-office-365-audit-log-search-tool"></a>À l’aide de l’outil de recherche de journal d’audit Office 365

Chacun des scénarios de dépannage décrites dans cet article sont basées sur l’utilisation de l’outil de recherche de journal d’audit de la sécurité pour Microsoft Office 365 et le centre de conformité. Cette section répertorie les autorisations requises pour la recherche dans le journal d’audit et décrit les étapes pour accéder et exécuter des recherches de journal d’audit. Chaque section du scénario fournit des instructions spécifiques sur la façon de configurer une requête de recherche du journal d’audit et les éléments à rechercher dans les enregistrements d’audit qui correspondent aux critères de recherche des informations détaillées.

### <a name="permissions-required-to-use-the-audit-log-search-tool"></a>Autorisations requises pour utiliser l’outil de recherche du journal d’audit

Vous devez être le rôle journaux d’Audit en affichage seul ou des journaux d’Audit dans Exchange Online à rechercher dans le journal d’audit Office 365. Par défaut, ces rôles sont affectés aux groupes de rôle de gestion de la conformité et de gestion de l’organisation dans la page **autorisations** , dans le centre d’administration Exchange. Pour plus d’informations, voir [rôles de gérer les groupes dans Exchange Online](https://go.microsoft.com/fwlink/p/?LinkID=730688).

### <a name="running-audit-log-searches"></a>Recherches de journal d’audit en cours d’exécution

Cette section décrit les notions de base pour créer et exécuter des recherches de journal d’audit. Utilisez ces instructions comme point de départ pour chaque scénario de dépannage dans cet article. Pour des instructions plus détaillées, voir [recherche d’audit de l’ouvrir une session dans la sécurité pour Microsoft Office 365 et le centre de conformité ](search-the-audit-log-in-security-and-compliance.md#step-1-run-an-audit-log-search).

1. Accédez à la page [https://protection.office.com](https://protection.office.com).
  
2. Connectez-vous à Office 365 à l'aide de votre compte scolaire ou professionnel.

3. Dans le volet gauche de la sécurité et le centre de conformité, cliquez sur **recherche et enquête** > **recherche des journaux d’Audit**.
    
    La page de **recherche des journaux d’Audit** s’affiche. 
    
    ![Configurer les critères, puis cliquez sur Rechercher pour lancer la recherche](media/8639d09c-2843-44e4-8b4b-9f45974ff7f1.png)
  
4. Vous pouvez configurer les critères de recherche suivants. Notez que chaque scénario de dépannage dans cet article ne recommande des instructions spécifiques à la configuration de ces champs.
    
    a. **activités** , cliquez sur la liste déroulante pour afficher les activités que vous pouvez rechercher. Après avoir exécuté la recherche, uniquement les enregistrements d’audit pour les activités sélectionnées sont affichées. Sélectionnez **Afficher les résultats pour toutes les activités** affiche les résultats de toutes les activités qui répondent aux critères de recherche. Vous devrez également laissez ce champ vide dans certains des scénarios de dépannage.
    
    b. **date de début** et **date de fin** - sélectionner une plage de date et heure pour afficher les événements qui se sont produites pendant cette période. Au cours des sept derniers jours sont sélectionnés par défaut. La date et l’heure sont présentées au format de temps universel coordonné (UTC). La plage de dates maximale que vous pouvez spécifier est 90 jours.

    les résultats pour c **utilisateurs** - cliquez dans cette zone et sélectionnez un ou plusieurs utilisateurs pour afficher la recherche. Les enregistrements d’audit pour l’activité sélectionnée effectuées par les utilisateurs que vous sélectionnez dans cette zone sont affichées dans la liste des résultats. Laissez cette zone vide de renvoi des entrées pour tous les utilisateurs (et les comptes de service) dans votre organisation.
    
    d. le **fichier, dossier ou site** - tapez tout ou partie d’un nom de fichier ou un dossier pour rechercher des activités liées au fichier du dossier qui contient le mot clé spécifié. Vous pouvez également spécifier une URL d’un fichier ou un dossier. Si vous utilisez une URL, assurez-vous que le type le chemin d’URL complète ou si vous tapez uniquement une partie de l’URL, n’incluez pas des caractères spéciaux ou des espaces. Laissez cette zone vide de renvoi des entrées pour tous les fichiers et dossiers dans votre organisation. Notez que ce champ est vide dans tous les scénarios de dépannage dans cet article.
    
5. Cliquez sur **Rechercher** pour lancer la recherche à l’aide de vos critères de recherche. 
    
    Les résultats de recherche sont chargés, et après quelques instants, ils sont affichent sous **résultats** sur la page de **recherche du journal d’Audit** . Pour les sections suivantes fournit des instructions sur les éléments à rechercher pour le scénario de résolution des problèmes spécifique.

    Pour plus d’informations sur l’affichage, le filtrage ou l’exportation des résultats de recherche du journal d’audit, voir :

    - [Afficher les résultats de recherche](search-the-audit-log-in-security-and-compliance.md#step-2-view-the-search-results)
    - [Filtrer les résultats de recherche](search-the-audit-log-in-security-and-compliance.md#step-3-filter-the-search-results)
    - [Exporter les résultats de la recherche](search-the-audit-log-in-security-and-compliance.md#step-4-export-the-search-results-to-a-file)

## <a name="finding-the-ip-address-of-the-computer-used-to-access-a-compromised-account"></a>Recherche de l’adresse IP de l’ordinateur utilisé pour accéder à un compte compromis

L’adresse IP correspondant à une activité exécutée par n’importe quel utilisateur est inclus dans la plupart des enregistrements d’audit. Informations sur le client utilisé sont également incluses dans l’enregistrement d’audit.

Voici comment configurer une requête de recherche du journal d’audit pour ce scénario :

**Activités** - si appropriée à votre cas, sélectionnez une activité spécifique à rechercher. Pour la résolution des problèmes des comptes compromis, envisagez de sélection de l’activité **utilisateur connecté à la boîte aux lettres** sous les **activités de boîte aux lettres Exchange**. Cela retourne les enregistrements d’audit affichant l’adresse IP qui a été utilisée lors de la signature la boîte aux lettres. Sinon, laissez ce champ vide pour renvoyer les enregistrements d’audit pour toutes les activités. 

> [!TIP]
> Si vous laissez ce champ vide retourne les activités **UserLoggedIn** , qui est une activité Azure Active Directory qui indique qu’une personne est connectée à un compte d’utilisateur Office 365. Pour afficher les enregistrements d’audit de **UserLoggedIn** , utilisez le filtrage dans les résultats de recherche.

**Date de début** et **date de fin** - sélectionnez une plage de dates qui s’applique à votre investigation.

**Utilisateurs** : Si vous utilisez des recherches sur un compte compromis, sélectionnez l’utilisateur dont le compte a été compromis. Cela renvoie des enregistrements d’audit pour les opérations effectuées par ce compte d’utilisateur.

**Fichier, dossier ou site** - laissez ce champ vide.

Après avoir exécuté la recherche, l’adresse IP pour chaque activité s’affiche dans la colonne **adresse IP** dans les résultats de recherche. Cliquez sur l’enregistrement dans les résultats de recherche pour afficher des informations plus détaillées sur la page flottant.

## <a name="determining-who-set-up-email-forwarding-for-a-mailbox"></a>Déterminer qui a configuré le transfert de messages pour une boîte aux lettres

Lorsque le transfert de messages est configuré pour une boîte aux lettres, les messages électroniques qui sont envoyés à la boîte aux lettres sont transférés vers une autre boîte aux lettres. Les messages peuvent être transférés vers les utilisateurs à l’intérieur ou à l’extérieur de votre organisation. Lorsque le transfert de messages est défini sur une boîte aux lettres, l’applet de commande Exchange Online sous-jacent utilisé est **Set-Mailbox**.

Voici comment configurer une requête de recherche du journal d’audit pour ce scénario :

**Activités** - laissez ce champ vide afin que la recherche renvoie des enregistrements d’audit pour toutes les activités. Cela est nécessaire pour retourner les enregistrements liés à l’applet de commande **Set-Mailbox** d’audit.

**Date de début** et **date de fin** - sélectionnez une plage de dates qui s’applique à votre investigation.

**Les utilisateurs** - sauf si vous utilisez des recherches sur un message électronique de transférer le problème pour un utilisateur spécifique, laissez ce champ vide. Cela vous permet d’identifier si le transfert de messages a été configuré pour n’importe quel utilisateur.

**Fichier, dossier ou site** - laissez ce champ vide.

Après avoir exécuté la recherche, cliquez sur **filtrer les résultats** dans la page de résultats de recherche. Dans la zone sous l’en-tête de colonne **activité** , tapez **Set-Mailbox** afin que seuls les enregistrements d’audit liées à l’applet de commande **Set-Mailbox** soient affichées.

![Filtrage des résultats d’une recherche de journal d’audit](media/emailforwarding1.png)

À ce stade, vous devez examiner les détails de chaque enregistrement d’audit pour déterminer si l’activité est liée par courrier électronique de transfert. Cliquez sur l’enregistrement d’audit pour afficher la page des **Détails** flottant, puis cliquez sur **plus d’informations**. Les capture d’écran et descriptions des caractéristiques suivantes les informations qui indique le transfert de messages a été définies sur la boîte aux lettres.

![Informations détaillées de l’enregistrement d’audit](media/emailforwarding2.png)

a dans le champ **ObjectId** , l’alias de la boîte aux lettres de transfert de messagerie a été définie sur s’affiche. Cette boîte aux lettres est également affiché dans la colonne de **l’élément** dans la page de résultats de recherche.

b. dans le champ de **paramètre** , la valeur *ForwardingSmtpAddress* indique que transférer électronique a été défini sur la boîte aux lettres. Dans cet exemple, la messagerie est transmise à la messagerie adresse mike@contoso.com, qui est en dehors de l’organisation alpinehouse.onmicrosoft.com.

c. la valeur *True* pour le paramètre *DeliverToMailboxAndForward* indique qu’une copie du message envoyé à sarad@alpinehouse.onmicrosoft.com *et* est transférée à l’adresse de messagerie spécifiée par la *ForwardingSmtpAddress *paramètre, qui est mike@contoso.com dans cet exemple. Si la valeur pour le paramètre *DeliverToMailboxAndForward* est définie sur *False*, courrier électronique est transféré uniquement à l’adresse spécifiée par le paramètre *ForwardingSmtpAddress* . Il n’est pas remis à la boîte aux lettres spécifiée dans le champ **ObjectId** .

d. le champ **UserId** indique l’utilisateur qui a défini le transfert de messages dans la boîte aux lettres spécifiée dans le champ **ObjectId** . Cet utilisateur est également affiché dans la colonne de **l’utilisateur** dans la page de résultats de recherche. Dans ce cas, il semble que le propriétaire de la boîte aux lettres définie le transfert de messages dans sa boîte aux lettres.

Si vous avez déterminé que le transfert de messages ne doit pas être défini sur la boîte aux lettres, vous pouvez la supprimer en exécutant la commande suivante dans Exchange Online PowerShell :

```
Set-Mailbox <mailbox alias> -ForwardingSmtpAddress $null 
```

Consultez l’article [Set-Mailbox](https://docs.microsoft.com/powershell/module/exchange/mailboxes/set-mailbox) pour plus d’informations sur les paramètres relatifs à la messagerie de transfert.

## <a name="determining-if-a-user-deleted-email-items"></a>Déterminer si un utilisateur a supprimé des éléments de messagerie électronique

Avant la suppression d’enregistrements du journal d’audit sur les éléments de messagerie électronique sont enregistrés dans le journal d’audit d’Office 365, l’audit de boîte aux lettres doit être activé pour chaque boîte aux lettres de l’utilisateur dans votre organisation. En outre, les actions de boîte aux lettres SoftDelete et HardDelete doivent être activées pour l’audit. Pour obtenir des instructions, consultez la rubrique [Activer la boîte aux lettres de l’audit dans Office 365](enable-mailbox-auditing.md). Si l’audit de boîte aux lettres est déjà activé pour les utilisateurs, utilisez les étapes suivantes pour rechercher le journal d’audit pour les événements liés aux éléments de messagerie supprimé.

Voici comment configurer une requête de recherche du journal d’audit pour ce scénario :

**Activités** - sous **activités de boîte aux lettres Exchange**, sélectionnez une ou les deux activités suivantes :

- **Messages supprimés du dossier éléments supprimés** - cette activité correspond à la boîte aux lettres **SoftDelete** action d’audit. Cette activité est également connectée lorsqu’un utilisateur supprime définitivement un élément en le sélectionnant et en appuyant sur **MAJ + SUPPR**. Une fois un élément est définitivement supprimé, l’utilisateur peut récupérer jusqu'à expiration de la période de rétention des éléments supprimés.

- **Messages Purged de boîte aux lettres** - cette activité correspond à la boîte aux lettres **HardDelete** action d’audit. Cette opération est enregistrée lorsqu’un utilisateur supprime un élément à partir du dossier éléments récupérables. Administrateurs peuvent utiliser l’outil de recherche de contenu de la sécurité pour Microsoft Office 365 et le centre de conformité pour rechercher et récupérer purgé éléments avant l’expiration de la période de rétention des éléments supprimés ou plus longtemps si boîte aux lettres de l’utilisateur est en attente.

**Date de début** et **date de fin** - sélectionnez une plage de dates qui s’applique à votre investigation.

L’outil de recherche du journal d’audit renverra **les utilisateurs** - si vous sélectionnez un utilisateur dans ce champ, les enregistrements d’audit des éléments de messagerie qui ont été supprimés (SoftDeleted ou HardDeleted) par l’utilisateur que vous spécifiez. Dans certains cas, l’utilisateur qui supprime un message électronique ne peut pas être le propriétaire de la boîte aux lettres.

**Fichier, dossier ou site** - laissez ce champ vide.

Après avoir exécuté la recherche, vous pouvez filtrer les résultats de recherche pour afficher les enregistrements d’audit des éléments supprimés, ou pour les éléments supprimés définitivement. Cliquez sur l’enregistrement d’audit pour afficher la page des **Détails** flottant, puis cliquez sur **plus d’informations**. Plus d’informations sur les éléments supprimés, tels que la ligne d’objet et l’emplacement de l’élément lorsqu’il a été supprimé, sont affichés dans le champ **AffectedItems** . Les captures d’écran suivantes affichent un exemple du champ **AffectedItems** à partir d’un élément récupérable et un élément supprimée.

**Exemple de champ AffectedItems pour élément récupérable**

![Enregistrement d’audit pour l’élément récupérable](media/softdeleteditem.png)

**Exemple de champ AffectedItems pour élément supprimée**

![Enregistrement d’audit pour l’élément de courrier supprimée](media/harddeleteditem.png)

### <a name="recovering-deleted-email-items"></a>Récupération des éléments de courrier électronique supprimés

Les utilisateurs peuvent récupérer des éléments supprimés si la période de rétention des éléments supprimés n’a pas expiré. Dans Exchange Online, la période de rétention par défaut supprimé éléments est de 14 jours, mais les administrateurs peuvent augmenter ce paramètre pour un maximum de 30 jours. Les utilisateurs de point à l’article de [récupérer des éléments supprimés ou courrier dans Outlook Web App](https://support.office.com/article/Recover-deleted-items-or-email-in-Outlook-Web-App-C3D8FC15-EEEF-4F1C-81DF-E27964B7EDD4) pour obtenir des instructions sur la récupération des éléments supprimés.

Comme expliqué précédemment, administrateurs peuvent être en mesure de récupérer les éléments supprimés définitivement si la période de rétention des éléments supprimés n’a pas expiré ou si la boîte aux lettres est sur mise en suspens, auquel cas les éléments sont conservés jusqu'à ce que la durée d’attente expire. Lorsque vous exécutez une recherche de contenu, les éléments supprimés et supprimée dans le dossier éléments récupérables sont renvoyés dans les résultats de recherche s’ils correspondent à la requête de recherche. Pour plus d’informations sur l’exécution de recherches de contenu, voir [Recherche de contenu dans Office 365](content-search.md).

> [!TIP]
> Pour rechercher des éléments de messagerie électronique supprimée, recherchez tout ou partie de la ligne d’objet qui est affichée dans le champ **AffectedItems** dans l’enregistrement d’audit.

## <a name="determining-if-a-user-created-an-inbox-rule"></a>Déterminer si un utilisateur créé une règle de boîte de réception

Lorsque les utilisateurs créent une règle de boîte de réception pour leur boîte aux lettres Exchange Online, un enregistrement d’audit correspondant est enregistré dans le journal d’audit. Pour plus d’informations sur les règles de boîte de réception, voir :

- [Utiliser les règles de boîte de réception dans Outlook sur le web](https://support.office.com/article/use-inbox-rules-in-outlook-on-the-web-8400435c-f14e-4272-9004-1548bb1848f2)
- [Gérer les messages électroniques dans Outlook à l’aide de règles](https://support.office.com/article/Manage-email-messages-by-using-rules-C24F5DEA-9465-4DF4-AD17-A50704D66C59)

Voici comment configurer une requête de recherche du journal d’audit pour ce scénario :

**Activités** - sous **activités de boîte aux lettres Exchange**, sélectionnez **New-InboxRule créer/modifier/activer/désactiver la règle de boîte de réception**.

**Date de début** et **date de fin** - sélectionnez une plage de dates qui s’applique à votre investigation.

**Les utilisateurs** - sauf si vous utilisez des recherches sur un utilisateur spécifique, laissez ce champ vide. Cela permet d’identifier les nouvelles règles de boîte de réception configurées par n’importe quel utilisateur.

**Fichier, dossier ou site** - laissez ce champ vide.

Après avoir exécuté la recherche, les enregistrements d’audit pour cette activité sont affichés dans les résultats de recherche. Cliquez sur un enregistrement d’audit pour afficher la page des **Détails** flottant, puis cliquez sur **plus d’informations**. Informations sur les paramètres de règle de boîte de réception sont affichées dans le champ **paramètres** . La capture d’écran et les descriptions suivant met en évidence les informations sur les règles de boîte de réception.

![Enregistrement d’audit pour la nouvelle règle de boîte de réception](media/NewInboxRuleRecord.png)

a dans le champ **ObjectId** , le nom complet de la règle de boîte de réception est affiché. Ce nom inclut l’alias de boîte aux lettres de l’utilisateur (par exemple, SaraD) et le nom de la règle de boîte de réception (par exemple, « déplacer les messages de l’administrateur »).

b. dans le champ de **paramètre** , la condition de la règle de boîte de réception est affichée. Dans cet exemple, la condition est spécifiée par le paramètre *From* . La valeur définie pour le paramètre *From* indique que la règle de boîte de réception agit sur le courrier envoyé par admin@alpinehouse.onmicrosoft.com. Pour obtenir une liste complète des paramètres qui peut être utilisé pour définir les conditions de règles de boîte de réception, consultez l’article [New-InboxRule](https://docs.microsoft.com/powershell/module/exchange/mailboxes/new-inboxrule) .

c. le paramètre *MoveToFolder* Spécifie l’action de la règle de boîte de réception ; Dans cet exemple, les messages provenant de admin@alpinehouse.onmicrosoft.com sont déplacés vers le dossier nommé *AdminSearch*. Voir aussi l’article [New-InboxRule](https://docs.microsoft.com/powershell/module/exchange/mailboxes/new-inboxrule) pour une liste complète des paramètres qui peuvent être utilisés pour définir l’action d’une règle de boîte de réception.

d. le champ **UserId** indiquer que l’utilisateur qui a créé la règle de boîte de réception spécifiée dans le champ **ObjectId** . Cet utilisateur est également affiché dans la colonne de **l’utilisateur** dans la page de résultats de recherche.