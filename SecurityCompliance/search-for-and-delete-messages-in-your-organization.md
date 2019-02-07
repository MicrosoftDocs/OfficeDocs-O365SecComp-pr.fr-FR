---
title: Rechercher et supprimer des messages électroniques dans votre organisation Office 365 - aide d’administration
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
ms.assetid: 3526fd06-b45f-445b-aed4-5ebd37b3762a
description: Utiliser la recherche et la purge des fonctionnalités de sécurité Office 365 &amp; centre de conformité pour rechercher et supprimer un message électronique à partir de toutes les boîtes aux lettres dans votre organisation.
ms.openlocfilehash: be83b2e3e765980ae401356b924c26c53386a2b3
ms.sourcegitcommit: d6a28c4f6db6a676ca960173e8ff8f17d4aa1c4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2019
ms.locfileid: "29755255"
---
# <a name="search-for-and-delete-email-messages-in-your-office-365-organization---admin-help"></a>Rechercher et supprimer des messages électroniques dans votre organisation Office 365 - aide d’administration

**Cet article est destiné aux administrateurs. Vous essayez de rechercher des éléments dans votre boîte aux lettres que vous souhaitez supprimer ? Trouver [un message ou un élément avec la recherche instantanée](https://support.office.com/article/69748862-5976-47b9-98e8-ed179f1b9e4d)**|
   
Vous pouvez utiliser la fonctionnalité de recherche de contenu dans Office 365 pour rechercher et supprimer un message électronique à partir de toutes les boîtes aux lettres dans votre organisation. Vous pouvez rechercher et supprimer des e-mails potentiellement dangereux ou à haut risque, tels que :
  
- Messages qui contiennent des pièces jointes dangereuses ou des virus
    
- Messages de hameçonnage
    
- Messages qui contiennent des données sensibles
    
> [!CAUTION]
> Recherche et purge est une puissante fonctionnalité qui permet à toute personne qui reçoit les autorisations nécessaires pour supprimer des messages électroniques à partir des boîtes aux lettres dans votre organisation. 
  
## <a name="before-you-begin"></a>Avant de commencer

- Pour créer et exécuter une recherche de contenu, vous devez être membre du groupe de rôles **gestionnaire eDiscovery** ou attribuer le rôle de gestion de **Recherche de conformité** . Pour supprimer des messages, vous devez être membre du groupe de rôles de **Gestion de l’organisation** ou attribuer le rôle de gestion de **Recherche et de Purge** . Pour plus d’informations sur l’ajout d’utilisateurs à un groupe de rôles, consultez la rubrique [donner aux utilisateurs l’accès à la & Office 365 sécurité Centre de conformité](grant-access-to-the-security-and-compliance-center.md).
    
- Vous devez utiliser sécurité & PowerShell du centre de conformité pour supprimer les messages. Voir [l’étape 2](#step-2-connect-to-security-amp-compliance-center-powershell) pour obtenir des instructions sur la connexion.
    
- Un maximum de 10 éléments par boîte aux lettres peut être supprimé en même temps. Étant donné que la capacité pour rechercher et supprimer des messages est destinée à être un outil de réponse aux incidents, cette limite permet de garantir que les messages sont supprimés rapidement des boîtes aux lettres. Cette fonctionnalité n’est pas destinée à nettoyer les boîtes aux lettres utilisateur. Pour supprimer plus de 10 éléments, vous pouvez utiliser la commande **Search-Mailbox-DeleteContent** dans Exchange Online PowerShell. Voir [Rechercher et supprimer les messages - aide d’administration](search-for-and-delete-messagesadmin-help.md).
    
- Le nombre maximal de boîtes aux lettres dans une recherche de contenu que vous pouvez supprimer des éléments dans en effectuant une recherche et vider action est de 50 000. Si la recherche de contenu (que vous créez à [l’étape 1](#step-1-create-a-content-search-to-find-the-message-to-delete)) comporte plus de 50 000 boîtes aux lettres source, l’action de purge (que vous créez à l’étape 3) échoue. Voir la section [plus d’informations](#more-information) pour une info-bulle sur l’exécution d’une recherche et purge opération sur plus de 50 000 boîtes aux lettres. 
    
- La procédure décrite dans cet article vous permet uniquement de supprimer des éléments dans les dossiers publics et les boîtes aux lettres Exchange Online. Vous ne pouvez pas l’utiliser pour supprimer du contenu à partir de SharePoint ou OneDrive pour les sites de l’entreprise.
    
## <a name="step-1-create-a-content-search-to-find-the-message-to-delete"></a>Étape 1 : créer une recherche de contenu pour rechercher les messages à supprimer

La première étape consiste à créer et exécuter une recherche de contenu pour trouver le message que vous souhaitez supprimer des boîtes aux lettres dans votre organisation. Vous pouvez créer la recherche à l’aide de la sécurité &amp; centre de conformité ou en exécutant les applets de commande **New-ComplianceSearch** et **ComplianceSearch-démarrer** . Les messages qui correspondent à la requête pour cette recherche est supprimée en exécutant la **New-ComplianceSearchAction-purger** commande à [l’étape 3](#step-3-delete-the-message). Pour plus d’informations sur la création d’une recherche de contenu et de configuration des requêtes de recherche, voir les rubriques suivantes : 
  
- [Recherche de contenu dans Office 365](content-search.md)
    
- [Requêtes de mot clé pour la recherche de contenu](keyword-queries-and-search-conditions.md)
    
- [New-ComplianceSearch](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/New-ComplianceSearch)
    
- [Start-ComplianceSearch](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/Start-ComplianceSearch)
    
> [!NOTE]
> Les emplacements de contenu sont recherchées dans la recherche de contenu que vous créez dans cette étape ne peut pas inclure de SharePoint ou OneDrive pour les sites de l’entreprise. Vous pouvez inclure uniquement les boîtes aux lettres et les dossiers publics dans une recherche de contenu qui sera utilisé pour les messages électroniques. Si la recherche de contenu inclut des sites, vous recevrez une erreur à l’étape 3 lorsque vous exécutez l’applet de commande **New-ComplianceSearchAction** . 
  
### <a name="tips-for-finding-messages-to-remove"></a>Conseils pour la recherche de messages à supprimer

L’objectif de la requête de recherche est de concentrer les résultats de la recherche sur les messages que vous voulez supprimer. Voici quelques conseils :
  
- Si vous connaissez le texte exact ou l’expression utilisée dans la ligne objet du message, utilisez la propriété **Subject** dans la requête de recherche. 
    
- Si vous connaissez la date (ou la plage de dates) exacte du message, incluez la propriété **Received** dans la requête de recherche. 
    
- Si vous savez qui a envoyé le message, incluez la propriété **From** dans la requête de recherche. 
    
- Afficher un aperçu des résultats de la recherche pour vérifier que la recherche a renvoyé uniquement le (ou les messages) que vous souhaitez supprimer.
    
- Utilisez les statistiques d’estimation de recherche (affiché dans le volet de détails de la recherche dans la sécurité &amp; centre de conformité ou à l’aide de l’applet de commande [Get-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517934) ) pour obtenir un nombre au nombre total de résultats. 
    
Voici deux exemples de requêtes pour rechercher des messages électroniques suspects.
  
- Cette requête renvoie les messages qui ont été reçus par les utilisateurs entre le 13 et le 14 avril 2016, et qui contiennent les mots « action » et « obligatoire » dans l’objet.
    
    ```
    (Received:4/13/2016..4/14/2016) AND (Subject:'Action required')
    ```
   
- Cette requête renvoie les messages qui ont été envoyés par chatsuwloginsset12345@outlook.com et contenant l’expression exacte « Mettez à jour vos informations de compte » dans l’objet.
    
    ```
    (From:chatsuwloginsset12345@outlook.com) AND (Subject:"Update your account information")
    ```

## <a name="step-2-connect-to-security--compliance-center-powershell"></a>Étape 2 : Se connecter à la sécurité & centre de conformité PowerShell

L’étape suivante consiste à se connecter à la sécurité & PowerShell du centre de conformité pour votre organisation. Pour des instructions détaillées, consultez la rubrique [se connecter à Office 365 sécurité &amp; PowerShell du centre de conformité](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).
  
Si votre compte Office 365 utilise l’authentification multifacteur (MFA) ou fédérés d’authentification, vous ne pouvez pas utiliser les instructions de la rubrique précédente sur la connexion à la sécurité & PowerShell du centre de conformité. Au lieu de cela, consultez les instructions fournies dans la rubrique [se connecter à Office 365 sécurité & PowerShell du centre de conformité à l’aide de l’authentification multifacteur](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/mfa-connect-to-scc-powershell).
  
## <a name="step-3-delete-the-message"></a>Étape 3 : Supprimer le message

Une fois que vous avez créé et affiné une recherche de contenu pour renvoyer le message que vous souhaitez supprimer et sont connectés à la sécurité &amp; PowerShell du centre de conformité, l’étape finale consiste à exécuter la cmdlet **New-ComplianceSearchAction** pour supprimer le message. Vous pouvez récupérable - ou suppression définitive le message. Un message récupérable est déplacé vers le dossier des éléments récupérables d’un utilisateur et conservé avant l’expiration de la période de rétention des éléments supprimés. Messages supprimée sont marquées pour suppression définitive de la boîte aux lettres et seront définitivement supprimées la prochaine fois que la boîte aux lettres est traitée par l’Assistant dossier géré. Si la récupération d’élément unique est activée pour la boîte aux lettres, éléments supprimés définitivement seront définitivement supprimées après expiration de la période de rétention des éléments supprimés. Si une boîte aux lettres est mis en attente, les messages supprimés sont conservés jusqu'à ce que la durée de la suspension de l’élément expire ou jusqu'à ce que le blocage est supprimé de la boîte aux lettres.
  
Dans l’exemple suivant, la commande sera récupérable-supprimer les résultats de recherche renvoyés par une recherche de contenu nommé « Supprimer du Message de Phishing ». 

```
New-ComplianceSearchAction -SearchName "Remove Phishing Message" -Purge -PurgeType SoftDelete
```

Disque dur-supprimer les éléments renvoyés par la recherche de contenu « Supprimer du Message de Phishing », vous exécuterez cette commande :

```
New-ComplianceSearchAction -SearchName "Remove Phishing Message" -Purge -PurgeType HardDelete
```

Notez que lorsque vous exécutez la commande précédente aux messages récupérable - ou suppression définitive, la recherche spécifiée par le paramètre *SearchName* est la recherche de contenu que vous avez créé à l’étape 1. 
  
Pour plus d’informations, voir [New-ComplianceSearchAction](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/New-ComplianceSearchAction).

## <a name="more-information"></a>Plus d’informations

- **Comment obtenir l’état de la recherche et l’opération de suppression ?**

    Exécutez la **Get-ComplianceSearchAction** pour obtenir l’état de l’opération de suppression. Notez que l’objet qui est créé lorsque vous exécutez l’applet de commande **New-ComplianceSearchAction** est nommé à l’aide de ce format : `<name of Content Search>_Purge`. 
    
- **Que se passe-t-il après la suppression d’un message ?**

   Un message est supprimé avec la `New-ComplianceSearchAction -Purge -PurgeType HardDelete` commande est déplacée vers le dossier vide et n’est pas accessible par l’utilisateur. Une fois que le message est déplacé vers le dossier de purge, le message est conservé pendant la durée de la période de rétention des éléments supprimés si la récupération d’élément unique est activée pour la boîte aux lettres. (Dans Office 365, récupération d’élément unique est activée par défaut lors de la création d’une nouvelle boîte aux lettres.) Après l’expiration de la période de rétention des éléments supprimés, le message est marqué pour suppression définitive et la prochaine fois que la boîte aux lettres est traitée par l’assistant dossier géré est purgé à partir d’Office 365. 

   Si vous utilisez la `New-ComplianceSearchAction -Purge -PurgeType SoftDelete` de commande, les messages sont placés dans le dossier de suppressions dans le dossier éléments récupérables de l’utilisateur. Il n’est pas immédiatement purgée à partir d’Office 365. L’utilisateur peut récupérer des messages dans le dossier éléments supprimés pour la durée en fonction de la période de rétention des éléments supprimés configurée pour la boîte aux lettres. Une fois cette période de rétention expire (ou si l’utilisateur supprime définitivement le message avant son expiration), le message est déplacé vers le dossier vide et n’est plus accessible par l’utilisateur. Une fois dans le dossier vide, le message est conservé pendant toute la durée en fonction de la période de rétention des éléments supprimés configurée pour la boîte aux lettres si la récupération d’éléments unique est activée pour la boîte aux lettres. (Dans Office 365, récupération d’élément unique est activée par défaut lors de la création d’une nouvelle boîte aux lettres.) Après l’expiration de la période de rétention des éléments supprimés, le message est marqué pour suppression définitive et la prochaine fois que la boîte aux lettres est traitée par l’assistant dossier géré est purgé à partir d’Office 365. 
    
- **Que se passe-t-il si vous devez supprimer un message de plus de 50 000 boîtes aux lettres ?**

    Comme indiqué précédemment, vous pouvez effectuer une recherche et vider opération sur un maximum de 50 000 boîtes aux lettres. Si vous devez effectuer une recherche et vider opération sur plus de 50 000 boîtes aux lettres, envisagez de créer des filtres d’autorisations recherche temporaire qui réduit le nombre de boîtes aux lettres doit être recherché à moins de 50 000 boîtes aux lettres. Par exemple, si votre organisation comporte des boîtes aux lettres dans les différents départements, États ou pays, vous pouvez créer un filtre d’autorisations de recherche de boîte aux lettres en fonction d’une de ces propriétés de boîte aux lettres pour rechercher un sous-ensemble de boîtes aux lettres dans votre organisation. Après avoir créé le filtre d’autorisations de recherche, vous créez la recherche (décrite à l’étape 1) et ensuite supprimer le message (décrit à l’étape 3). Vous pouvez ensuite modifier le filtre pour rechercher et supprimer définitivement les messages dans un ensemble différent de boîtes aux lettres. Pour plus d’informations sur la création des filtres des autorisations de recherche, voir [configurer les autorisations de filtrage pour la recherche de contenu](permissions-filtering-for-content-search.md).
    
- **Supprimer des éléments non indexés inclus dans les résultats de recherche ?**

    Non, la « New-ComplianceSearchAction-commande Vider ne supprime pas les éléments non indexés. 
    
- **Que se passe-t-il si un message est supprimé d’une boîte aux lettres qui a été placé sur le blocage sur Place ou litige ou est affectée à une stratégie de rétention Office 365 ?**

    Une fois que le message est purgé et déplacé vers le dossier de purge, le message est conservé jusqu'à ce que la durée d’attente expire. Si la durée d’attente est illimitée, les éléments sont conservés jusqu'à ce que le blocage est supprimé ou la durée d’attente est modifiée.
    
- **Pourquoi la recherche et supprimer des flux de travail réparti entre les différents groupes de rôles de centre de conformité sécurité & ?**

    Comme expliqué précédemment, une personne doit être un membre du groupe de rôles de gestionnaire de découverte électronique ou attribuer le rôle de gestion de conformité recherche pour rechercher les boîtes aux lettres. Pour supprimer des messages, une personne doit être un membre du groupe de rôles de gestion de l’organisation ou attribuer le rôle de gestion de recherche et de Purge. Cela permet à un contrôle qui peut rechercher des boîtes aux lettres dans l’organisation et qui peut supprimer des messages. 
