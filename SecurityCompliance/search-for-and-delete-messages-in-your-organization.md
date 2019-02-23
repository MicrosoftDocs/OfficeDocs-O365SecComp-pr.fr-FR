---
title: Rechercher et supprimer des messages électroniques dans votre organisation Office 365-aide de l'administrateur
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 3526fd06-b45f-445b-aed4-5ebd37b3762a
description: Utilisez la fonctionnalité de recherche et de purge dans le centre de &amp; sécurité conformité Office 365 pour rechercher et supprimer un message électronique de toutes les boîtes aux lettres de votre organisation.
ms.openlocfilehash: ecdacd4e484d6de267e029b8e3fcdafc9b1fce4d
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30223613"
---
# <a name="search-for-and-delete-email-messages-in-your-office-365-organization---admin-help"></a>Rechercher et supprimer des messages électroniques dans votre organisation Office 365-aide de l'administrateur

**Cet article est destiné aux administrateurs. Essayez-vous de trouver des éléments dans votre boîte aux lettres que vous souhaitez supprimer? Voir [Rechercher un message ou un élément avec recherche instantanée](https://support.office.com/article/69748862-5976-47b9-98e8-ed179f1b9e4d)**|
   
Vous pouvez utiliser la fonctionnalité de recherche de contenu dans Office 365 pour rechercher et supprimer un message électronique de toutes les boîtes aux lettres de votre organisation. Cela peut vous aider à détecter et supprimer les messages potentiellement dangereux ou à haut risque, tels que:
  
- Messages contenant des pièces jointes ou des virus dangereux
    
- Messages de hameçonnage
    
- Messages qui contiennent des données sensibles
    
> [!CAUTION]
> La fonction de recherche et de purge est une fonctionnalité puissante qui permet à quiconque disposant des autorisations nécessaires de supprimer des messages électroniques de boîtes aux lettres de votre organisation. 
  
## <a name="before-you-begin"></a>Avant de commencer

- Pour créer et exécuter une recherche de contenu, vous devez être membre du groupe de rôles **Gestionnaire eDiscovery** ou être doté du rôle de gestion de la **recherche de conformité** . Pour supprimer des messages, vous devez être membre du groupe de rôles gestion de l' **organisation** ou disposer du rôle de gestion de la **recherche et de la purge** . Pour plus d'informations sur l'ajout d'utilisateurs à un groupe de rôles, consultez [la rubrique accorder aux utilisateurs l'accès au centre de sécurité & de sécurité Office 365](grant-access-to-the-security-and-compliance-center.md).
    
- Vous devez utiliser le centre de sécurité & Compliance Center PowerShell pour supprimer des messages. RePortez-vous à l' [étape 2](#step-2-connect-to-security-amp-compliance-center-powershell) pour obtenir des instructions sur la connexion.
    
- Vous pouvez supprimer un maximum de 10 éléments par boîte aux lettres à la fois. Étant donné que la fonctionnalité de recherche et de suppression des messages est conçue comme un outil de réponse aux incidents, cette limite permet de s'assurer que les messages sont rapidement supprimés des boîtes aux lettres. Cette fonctionnalité n'est pas destinée à nettoyer les boîtes aux lettres utilisateur. Pour supprimer plus de 10 éléments, vous pouvez utiliser la commande **Search-Mailbox-DeleteContent** dans Exchange Online PowerShell. Consultez la rubrique [Rechercher et supprimer des messages-aide de l'administrateur](search-for-and-delete-messagesadmin-help.md).
    
- Le nombre maximal de boîtes aux lettres dans une recherche de contenu que vous pouvez supprimer des éléments dans en effectuant une opération de recherche et de purge est 50 000. Si la recherche de contenu (que vous créez à l' [étape 1](#step-1-create-a-content-search-to-find-the-message-to-delete)) comporte plus de 50 000 boîtes aux lettres source, l'action de vidage (que vous créez à l'étape 3) échouera. Consultez la section [plus d'informations](#more-information) pour obtenir une astuce sur l'exécution d'une opération de recherche et de purge sur plus de 50 000 boîtes aux lettres. 
    
- La procédure décrite dans cet article ne peut être utilisée que pour supprimer des éléments dans les boîtes aux lettres et les dossiers publics Exchange Online. Vous ne pouvez pas l'utiliser pour supprimer du contenu de sites SharePoint ou OneDrive entreprise.
    
## <a name="step-1-create-a-content-search-to-find-the-message-to-delete"></a>Étape 1 : créer une recherche de contenu pour rechercher les messages à supprimer

La première étape consiste à créer et exécuter une recherche de contenu pour rechercher le message que vous souhaitez supprimer des boîtes aux lettres de votre organisation. Vous pouvez créer la recherche à l'aide du &amp; Centre de sécurité conformité ou en exécutant les cmdlets **New-ComplianceSearch** et **Start-ComplianceSearch** . Les messages qui correspondent à la requête pour cette recherche sont supprimés en exécutant la commande **New-ComplianceSearchAction-purger** à l' [étape 3](#step-3-delete-the-message). Pour plus d'informations sur la création d'une recherche de contenu et sur la configuration de requêtes de recherche, consultez les rubriques suivantes: 
  
- [Recherche de contenu dans Office 365](content-search.md)
    
- [Requêtes par Mots clés pour la recherche de contenu](keyword-queries-and-search-conditions.md)
    
- [New-ComplianceSearch](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/New-ComplianceSearch)
    
- [Start-ComplianceSearch](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/Start-ComplianceSearch)
    
> [!NOTE]
> Les emplacements de contenu qui sont recherchés dans la recherche de contenu que vous créez dans cette étape ne peuvent pas inclure de sites SharePoint ou OneDrive entreprise. Vous pouvez inclure uniquement les boîtes aux lettres et les dossiers publics dans une recherche de contenu qui sera utilisée pour les messages électroniques. Si la recherche de contenu inclut des sites, vous recevrez une erreur à l'étape 3 lors de l'exécution de la cmdlet **New-ComplianceSearchAction** . 
  
### <a name="tips-for-finding-messages-to-remove"></a>Conseils pour la recherche de messages à supprimer

L’objectif de la requête de recherche est de concentrer les résultats de la recherche sur les messages que vous voulez supprimer. Voici quelques conseils :
  
- Si vous êtes informé du texte ou de l'expression exact utilisés dans la ligne d'objet du message, utilisez la propriété **Subject** dans la requête de recherche. 
    
- Si vous connaissez la date (ou la plage de dates) exacte du message, incluez la propriété **Received** dans la requête de recherche. 
    
- Si vous savez qui a envoyé le message, incluez la propriété **From** dans la requête de recherche. 
    
- Affichez un aperçu des résultats de la recherche pour vérifier que la recherche renvoie uniquement les messages (ou messages) que vous souhaitez supprimer.
    
- Utilisez les statistiques d'estimation de recherche (affichées dans le volet d'informations de la recherche &amp; dans le centre de sécurité conformité ou à l'aide de la cmdlet [Get-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517934) ) pour obtenir le nombre total de résultats. 
    
Voici deux exemples de requêtes pour rechercher des messages électroniques suspects.
  
- Cette requête renvoie les messages qui ont été reçus par les utilisateurs entre le 13 et le 14 avril 2016, et qui contiennent les mots « action » et « obligatoire » dans l’objet.
    
    ```
    (Received:4/13/2016..4/14/2016) AND (Subject:'Action required')
    ```
   
- Cette requête renvoie les messages qui ont été envoyés par chatsuwloginsset12345@outlook.com et contenant l’expression exacte « Mettez à jour vos informations de compte » dans l’objet.
    
    ```
    (From:chatsuwloginsset12345@outlook.com) AND (Subject:"Update your account information")
    ```

## <a name="step-2-connect-to-security--compliance-center-powershell"></a>Étape 2: Connectez-vous au centre de sécurité & Compliance Center PowerShell

L'étape suivante consiste à vous connecter au centre de sécurité & Compliance Center PowerShell pour votre organisation. Pour obtenir des instructions pas à pas, consultez [la rubrique Connect to Office &amp; 365 Security Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).
  
Si votre compte Office 365 utilise l'authentification multifacteur (MFA) ou l'authentification fédérée, vous ne pouvez pas utiliser les instructions de la rubrique précédente sur la connexion au centre de sécurité & Compliance Center PowerShell. Au lieu de cela, consultez les instructions de la rubrique [se connecter au centre de sécurité Office 365 Security _AMP_ PowerShell using Multi-Factor Authentication](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/mfa-connect-to-scc-powershell).
  
## <a name="step-3-delete-the-message"></a>Étape 3: supprimer le message

Une fois que vous avez créé et affiné une recherche de contenu pour renvoyer le message que vous souhaitez supprimer et que vous &amp; êtes connecté au centre de sécurité, la dernière étape consiste à exécuter la cmdlet **New-ComplianceSearchAction** pour supprimer le message. Vous pouvez supprimer le message de manière irréversible ou irréversible. Un message supprimé (récupérable) est déplacé vers le dossier éléments récupérables d'un utilisateur et conservé jusqu'à l'expiration de la période de rétention des éléments supprimés. Les messages supprimés définitivement sont marqués pour suppression définitive de la boîte aux lettres et seront définitivement supprimés la prochaine fois que la boîte aux lettres sera traitée par l'Assistant dossier géré. Si la récupération d'élément unique est activée pour la boîte aux lettres, les éléments supprimés définitivement seront définitivement supprimés après l'expiration de la période de rétention des éléments supprimés. Si une boîte aux lettres est placée en conservation, les messages supprimés sont conservés jusqu'à ce que la durée de la conservation de l'élément expire ou jusqu'à ce que la conservation soit supprimée de la boîte aux lettres.
  
Dans l'exemple suivant, la commande supprime de manière récupérable les résultats de la recherche renvoyés par une recherche de contenu nommée «Remove phishing message». 

```
New-ComplianceSearchAction -SearchName "Remove Phishing Message" -Purge -PurgeType SoftDelete
```

Pour supprimer définitivement les éléments renvoyés par la recherche de contenu «supprimer le message d'hameçonnage», exécutez la commande suivante:

```
New-ComplianceSearchAction -SearchName "Remove Phishing Message" -Purge -PurgeType HardDelete
```

Notez que lorsque vous exécutez la commande précédente pour les messages de suppression logicielle ou matérielle, la recherche spécifiée par le paramètre *SearchName* est la recherche de contenu que vous avez créée à l'étape 1. 
  
Pour plus d'informations, consultez la rubrique [New-ComplianceSearchAction](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/New-ComplianceSearchAction).

## <a name="more-information"></a>Plus d’informations

- **Comment obtenir l'état de l'opération de recherche et de suppression?**

    Exécutez la commande **Get-ComplianceSearchAction** pour obtenir l'état de l'opération de suppression. Notez que l'objet qui est créé lors de l'exécution de la cmdlet **New-ComplianceSearchAction** est nommé à l' `<name of Content Search>_Purge`aide de ce format:. 
    
- **Que se passe-t-il une fois que vous avez supprimé un message?**

   Un message qui a été supprimé avec `New-ComplianceSearchAction -Purge -PurgeType HardDelete` la commande est déplacé vers le dossier purges et n'est pas accessible par l'utilisateur. Une fois le message déplacé dans le dossier purges, le message est conservé pendant la durée de la période de rétention des éléments supprimés si la récupération d'élément unique est activée pour la boîte aux lettres. (Dans Office 365, la récupération d'élément unique est activée par défaut lors de la création d'une nouvelle boîte aux lettres.) Une fois la période de rétention des éléments supprimés expirée, le message est marqué pour suppression définitive et sera purgé à partir d'Office 365 la prochaine fois que la boîte aux lettres sera traitée par l'Assistant dossier géré. 

   Si vous utilisez la `New-ComplianceSearchAction -Purge -PurgeType SoftDelete` commande, les messages sont déplacés vers le dossier des suppressions dans le dossier éléments récupérables de l'utilisateur. Il n'est pas supprimé immédiatement d'Office 365. L'utilisateur peut récupérer les messages dans le dossier éléments supprimés pendant la durée en fonction de la période de rétention des éléments supprimés configurée pour la boîte aux lettres. Une fois cette période de rétention expirée (ou si l'utilisateur purge le message avant son expiration), le message est déplacé vers le dossier purges et l'utilisateur ne peut plus y accéder. Une fois dans le dossier purges, le message est conservé pendant la durée en fonction de la période de rétention des éléments supprimés configurée pour la boîte aux lettres si la récupération d'éléments uniques est activée pour la boîte aux lettres. (Dans Office 365, la récupération d'élément unique est activée par défaut lors de la création d'une nouvelle boîte aux lettres.) Une fois la période de rétention des éléments supprimés expirée, le message est marqué pour suppression définitive et sera vidé de Office 365 la prochaine fois que la boîte aux lettres sera traitée par l'Assistant dossier géré. 
    
- **Que se passe-t-il si vous devez supprimer un message de plus de 50 000 boîtes aux lettres?**

    Comme indiqué précédemment, vous pouvez effectuer une opération de recherche et de purge sur un maximum de 50 000 boîtes aux lettres. Si vous devez effectuer une opération de recherche et de purge sur plus de 50 000 boîtes aux lettres, envisagez de créer des filtres d'autorisations de recherche temporaires qui réduiraient le nombre de boîtes aux lettres qui seraient recherchées avec moins de 50 000 boîtes aux lettres. Par exemple, si votre organisation contient des boîtes aux lettres dans différents services, États ou pays, vous pouvez créer un filtre d'autorisations de recherche de boîte aux lettres basé sur l'une de ces propriétés de boîte aux lettres pour rechercher un sous-ensemble de boîtes aux lettres dans votre organisation. Après avoir créé le filtre d'autorisations de recherche, vous devez créer la recherche (décrite à l'étape 1), puis supprimer le message (décrit à l'étape 3). Vous pouvez ensuite modifier le filtre pour rechercher et purger les messages dans un autre ensemble de boîtes aux lettres. Pour plus d'informations sur la création de filtres d'autorisations de recherche, voir [configurer le filtrage des autorisations pour la recherche de contenu](permissions-filtering-for-content-search.md).
    
- **Les éléments non indexés inclus dans les résultats de la recherche seront-ils supprimés?**

    Non, la commande «New-ComplianceSearchAction-purge ne supprime pas les éléments non indexés. 
    
- **Que se passe-t-il si un message est supprimé d'une boîte aux lettres qui a été placée en conservation inaltérable ou en conservation pour litige ou est affecté à une stratégie de rétention Office 365?**

    Une fois que le message a été purgé et déplacé vers le dossier purges, le message est conservé jusqu'à l'expiration de la durée de la conservation. Si la durée de la conservation est illimitée, les éléments sont conservés jusqu'à ce que la conservation soit supprimée ou que la durée de la conservation soit modifiée.
    
- **Pourquoi les flux de travail de recherche et de suppression sont-ils divisés en différents groupes de rôles de centre de sécurité & de conformité?**

    Comme expliqué précédemment, une personne doit être membre du groupe de rôles gestionnaire eDiscovery ou se voir attribuer le rôle de gestion de la recherche de conformité pour effectuer des recherches dans des boîtes aux lettres. Pour supprimer des messages, une personne doit être membre du groupe de rôles gestion de l'organisation ou se voir attribuer le rôle de gestion recherche et purge. Cela permet de contrôler qui peut effectuer des recherches dans les boîtes aux lettres de l'organisation et qui peut supprimer des messages. 
