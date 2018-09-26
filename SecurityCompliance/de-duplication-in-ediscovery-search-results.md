---
title: Déduplication dans les résultats de recherche eDiscovery
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/21/2016
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid: MOE150
ms.assetid: 5af334b6-a15d-4f73-97f8-1423457d9f6b
description: Vous avez la possibilité de suppression des doublons des résultats de recherche de découverte électronique qui sont exportés afin qu’une seule copie d’un message électronique est exportée, même si plusieurs instances du même message a été trouvés dans différentes boîtes aux lettres.
ms.openlocfilehash: 5e54f0e5841fdbd29d1ab8b6b9509ff06e827920
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038007"
---
# <a name="de-duplication-in-ediscovery-search-results"></a>Déduplication dans les résultats de recherche eDiscovery

Cet article décrit le fonctionnement de la déduplication des résultats de recherche eDiscovery et explique les limitations de l’algorithme de la déduplication.
  
Lorsque vous utilisez les outils de découverte électronique Office 365 pour exporter les résultats d’une recherche eDiscovery, vous avez la possibilité de suppression des doublons les résultats qui sont exportés. Que cela signifie ? Lorsque vous activez la déduplication (par défaut, la déduplication n’est pas activée), une seule copie d’un message électronique est exportée, même si plusieurs instances du même message ont été trouvées dans les boîtes aux lettres qui ont été exclus. La déduplication permet de gagner du temps en réduisant le nombre d’éléments que vous devez passer en revue et analyser une fois les résultats de recherche sont exportées. Mais il est important de comprendre le fonctionne de la déduplication et à l’esprit qu’il existe des limitations de l’algorithme qui peut provoquer un élément unique doit être marqué comme étant un doublon pendant le processus d’exportation.
  
## <a name="how-duplicate-messages-are-identified"></a>Comment les messages en double sont identifiés

Les outils Office 365 eDiscovery utilisent une combinaison des propriétés de messagerie suivantes pour déterminer si un message est un doublon :
  
- **InternetMessageId** - cette propriété spécifie l’identificateur de message Internet d’un message électronique, qui est un identificateur global unique qui fait référence à une version spécifique d’un message spécifique. Cet ID est généré par le programme de client de messagerie de l’expéditeur ou le système de messagerie hôte qui envoie le message. Si une personne envoie un message à plusieurs destinataires, l’ID de message Internet sera la même pour chaque instance du message. Les versions ultérieures au message d’origine reçoit un identificateur de message différent. 
    
- **ConversationTopic** - sa propriété spécifie le sujet de la conversation d’un message. La valeur de la propriété **ConversationTopic** est la chaîne qui décrit la rubrique générale de la conversation. Une conservation se compose d’un message initial et tous les messages envoyés dans la réponse au message. Messages de la même conversation ont la même valeur de la propriété **ConversationTopic** . La valeur de cette propriété est généralement la ligne objet du message initial qui a généré la conversation. 
    
- **BodyTagInfo** - il s’agit d’une propriété de banque Exchange interne. La valeur de cette propriété est calculée en vérifiant les divers attributs dans le corps du message. Cette propriété est utilisée pour identifier les différences dans le corps des messages. 
    
Pendant le processus d’exportation eDiscovery, ces trois propriétés sont comparées pour chaque message correspond aux critères de recherche. Si ces propriétés sont identiques pour les deux (ou plusieurs) des messages, ces messages sont déterminés à des doublons et le résultat est qu’une seule copie du message doit être exportée si la déduplication est activée. Le message est exporté est appelé le « élément source ». Informations sur les messages en double sont incluses dans les rapports **Results.csv** et **Manifest.xml** qui sont inclus dans les résultats de recherche exportés. Dans le fichier **Results.csv** , un message en double est identifié par ayant une valeur dans la colonne **en double pour l’élément** . La valeur dans cette colonne correspond à la valeur dans la colonne **Identité d’un article** pour le message qui a été exporté. 
  
Les graphiques suivants illustrent la façon dont les doublons s’affichent dans les rapports **Results.csv** et **Manifest.xml** qui sont exportés avec les résultats de recherche. Ces rapports ne pas inclure les propriétés de messagerie décrites précédemment, qui sont utilisées dans l’algorithme de suppression des doublons. Au lieu de cela, les rapports comprennent la propriété **Identity de l’élément** qui est affectée aux éléments de la banque d’informations Exchange. 
  
 ### <a name="resultscsv-report-viewed-in-excel"></a>Rapport Results.csv (affiché dans Excel)
  
![Affichage des informations sur les éléments en double dans le rapport Results.csv](media/e3d64004-3b91-4cba-b6f3-934b46cbdcdb.png)
  
 ### <a name="manifestxml-report-viewed-in-excel"></a>Rapport manifest.XML (affiché dans Excel)
  
![Affichage des informations sur les éléments en double dans le rapport Manifest.xml](media/69aa4786-9883-46ff-bcae-b35e0daf4a6d.png)
  
En outre, les autres propriétés des messages en double sont incluses dans les rapports d’exportation. Cela inclut la boîte aux lettres que se trouve le message en double, si le message a été envoyé à un groupe de distribution et, si le message a été serait Cc ou Cci séparées par un autre utilisateur.
  
## <a name="limitations-of-the-de-duplication-algorithm"></a>Limitations de l’algorithme de suppression des doublons

Il existe certaines limitations connues de l’algorithme de suppression des doublons risquent d’éléments uniques à obtenir marqués comme étant des doublons. Il est important de comprendre ces limitations afin de décider s’il faut utiliser la fonctionnalité de la déduplication facultatif.
  
Il existe une situation où la fonctionnalité de la déduplication peut identifier par erreur un message comme un double et exporte pas (mais toujours le citer un doublon dans les rapports d’exportation). Il s’agit de messages d’un utilisateur modifie, mais n’envoie pas. Supposons, par exemple, un utilisateur sélectionne un message dans Outlook, copie le contenu du message, puis il la colle dans un nouveau message. L’utilisateur modifie ensuite l’une des copies en supprimant ou ajouter une pièce jointe ou modification de la ligne d’objet ou le corps de lui-même. Si ces deux messages correspond à la requête d’une recherche eDiscovery, seul des messages est exporté si la déduplication est activée lorsque les résultats de recherche sont exportées. Ainsi, même si le message d’origine ou copiée a été modifiée, aucun des messages révisés ont été envoyés et par conséquent, les valeurs des propriétés **InternetMessageId**, **ConversationTopic** et **BodyTagInfo** n’ont pas été mis à jour. Mais comme expliqué précédemment, les messages sont répertoriés dans les rapports d’exportation 
  
Notez que des messages uniques peuvent également être marqués comme doublons lorsque la fonctionnalité de protection de page copie sur écriture est activée, comme dans le cas d’une boîte aux lettres en cours sur litige ou blocage sur Place. La fonctionnalité de copie sur écriture copie le message d’origine (et l’enregistre dans le dossier de Versions du dossier éléments récupérables de l’utilisateur) avant l’enregistrement de la révision de l’élément d’origine. Dans ce cas, la copie révisée et le message d’origine (dans le dossier éléments récupérables) peuvent être considérés comme des messages en double et par conséquent uniquement un d'entre eux doit être exporté.
  
> [!IMPORTANT]
> Si les limitations de l’algorithme de la déduplication peuvent avoir un impact sur la qualité de vos résultats de recherche, vous ne doivent pas activer la déduplication lorsque vous exportez des éléments. Si les situations décrites dans cette section sont peu de chances d’être un facteur dans vos résultats de recherche, et que vous souhaitez réduire le nombre d’éléments susceptibles d’être des doublons, vous devez envisager l’activation de la déduplication. 
  
## <a name="more-information"></a>Plus d’informations

- Les informations de cet article s’appliquent lors de l’exportation des résultats de recherche à l’aide d’un des outils de découverte électronique suivants :
    
  - Recherche de contenu de sécurité Office 365 &amp; centre de conformité
    
  - Découverte électronique inaltérable dans Exchange Online
    
  - Le centre eDiscovery dans SharePoint Online
    
- Pour plus d’informations sur l’exportation de résultats de recherche, voir :
    
  - [Exporter les résultats de recherche à partir de la sécurité de 365 Office &amp; centre de conformité](export-search-results.md)
    
  - [Exporter un rapport de recherche de contenu à partir de la sécurité de 365 Office &amp; centre de conformité](export-a-content-search-report.md)
    
  - [Résultats de la recherche exporter In-Place eDiscovery vers un fichier PST](https://go.microsoft.com/fwlink/p/?linkid=832671)
    
  - [Exporter du contenu et créer des rapports dans le centre de découverte électronique](https://support.office.com/article/7b2ea190-5f9b-4876-86e5-4440354c381a)
