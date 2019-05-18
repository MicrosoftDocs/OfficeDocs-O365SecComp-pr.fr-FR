---
title: Déduplication dans les résultats de recherche eDiscovery
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/21/2016
audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid: MOE150
ms.assetid: 5af334b6-a15d-4f73-97f8-1423457d9f6b
description: Vous avez la possibilité de dédupliquer les résultats de recherche de découverte électronique exportés de sorte qu’une seule copie d’un message électronique soit exportée même si plusieurs instances du même message ont pu être trouvées dans des boîtes aux lettres différentes.
ms.openlocfilehash: 98639bd23b3d7c99b91a193c2651ff2fad677eeb
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34150656"
---
# <a name="de-duplication-in-ediscovery-search-results"></a>Déduplication dans les résultats de recherche eDiscovery

Cet article décrit le fonctionnement de la déduplication des résultats de recherche de découverte électronique et explique les limites de l’algorithme de déduplication.
  
Lorsque vous utilisez les outils eDiscovery d’Office 365 pour exporter les résultats d’une recherche de découverte électronique, vous avez la possibilité de dédupliquer les résultats qui sont exportés. Scénario Lorsque vous activez la déduplication (par défaut, la déduplication n’est pas activée), une seule copie d’un message électronique est exportée même si plusieurs instances du même message ont pu être trouvées dans les boîtes aux lettres qui ont été recherchées. La déduplication vous permet de gagner du temps en réduisant le nombre d’éléments que vous devez examiner et analyser après l’exportation des résultats de la recherche. Toutefois, il est important de comprendre le fonctionnement de la déduplication et de savoir qu’il existe des limitations à l’algorithme susceptibles de provoquer la marque d’un élément unique en tant que doublon pendant le processus d’exportation.
  
## <a name="how-duplicate-messages-are-identified"></a>Identification des doublons de messages

Les outils eDiscovery Office 365 utilisent une combinaison des propriétés de messagerie suivantes pour déterminer si un message est un doublon:
  
- **InternetMessageId** -cette propriété spécifie l’identificateur de message Internet d’un message électronique, qui est un identificateur global unique qui fait référence à une version spécifique d’un message spécifique. Cet ID est généré par le programme client de messagerie de l’expéditeur ou par le système de messagerie hôte qui envoie le message. Si une personne envoie un message à plusieurs destinataires, l’ID de message Internet est le même pour chaque instance du message. Les révisions suivantes du message d’origine recevront un identificateur de message différent. 
    
- **ConversationTopic** -sa propriété spécifie l’objet du thème de la conversation d’un message. La valeur de la propriété **ConversationTopic** est la chaîne qui décrit le sujet global de la conversation. Une conservation est constituée d’un message initial et de tous les messages envoyés en réponse au message initial. Les messages dans la même conversation ont la même valeur pour la propriété **ConversationTopic** . La valeur de cette propriété est généralement la ligne d’objet du message initial qui a généré la conversation. 
    
- **BodyTagInfo** -il s’agit d’une propriété de la banque Exchange interne. La valeur de cette propriété est calculée en vérifiant différents attributs dans le corps du message. Cette propriété est utilisée pour identifier les différences dans le corps des messages. 
    
Lors du processus d’exportation de la découverte électronique, ces trois propriétés sont comparées pour chaque message correspondant aux critères de recherche. Si ces propriétés sont identiques pour deux (ou plus) messages, ces messages sont considérés comme des doublons et le résultat est qu’une seule copie du message sera exportée si la déduplication est activée. Le message exporté est appelé «élément source». Les informations sur les messages en double sont incluses dans les rapports **results. csv** et **Manifest. xml** qui sont inclus dans les résultats de recherche exportés. Dans le fichier **results. csv** , un message en double est identifié par une valeur dans la colonne **dupliquer vers l’élément** . La valeur dans cette colonne correspond à la valeur dans la colonne identité de l' **élément** pour le message qui a été exporté. 
  
Les graphiques suivants montrent comment les messages dupliqués sont affichés dans les rapports **results. csv** et **Manifest. xml** qui sont exportés avec les résultats de la recherche. Ces rapports n’incluent pas les propriétés de messagerie précédemment décrites, qui sont utilisées dans l’algorithme de déduplication. Au lieu de cela, les rapports incluent la propriété d’identité de l' **élément** qui est assignée aux éléments par la Banque d’aide Exchange. 
  
 ### <a name="resultscsv-report-viewed-in-excel"></a>Rapport results. csv (affiché dans Excel)
  
![Affichage des informations sur les éléments en double dans le rapport results. csv](media/e3d64004-3b91-4cba-b6f3-934b46cbdcdb.png)
  
 ### <a name="manifestxml-report-viewed-in-excel"></a>Rapport manifest. XML (affiché dans Excel)
  
![Affichage des informations sur les éléments en double dans le rapport manifest. Xml](media/69aa4786-9883-46ff-bcae-b35e0daf4a6d.png)
  
En outre, les autres propriétés des messages en double sont incluses dans les rapports d’exportation. Cela inclut la boîte aux lettres dans laquelle se trouve le doublon du message, si le message a été envoyé à un groupe de distribution et si le message a été envoyé à un autre utilisateur (CC) ou CCI.
  
## <a name="limitations-of-the-de-duplication-algorithm"></a>Limites de l’algorithme de déduplication

Il existe certaines limitations connues de l’algorithme de déduplication qui peuvent entraîner la présence d’éléments uniques marqués comme étant des doublons. Il est important de comprendre ces limitations afin de décider si vous pouvez utiliser la fonctionnalité facultative de déduplication.
  
Il existe une situation dans laquelle la fonctionnalité de déduplication peut identifier par erreur un message comme étant un doublon et ne pas l’exporter (tout en le citation en tant que doublon dans les rapports d’exportation). Il s’agit des messages qu’un utilisateur modifie mais n’envoie pas. Par exemple, supposons qu’un utilisateur sélectionne un message dans Outlook, copie le contenu du message, puis le colle dans un nouveau message. Ensuite, l’utilisateur modifie l’une des copies en supprimant ou en ajoutant une pièce jointe, ou en modifiant la ligne d’objet ou le corps lui-même. Si ces deux messages correspondent à la requête d’une recherche de découverte électronique, seul l’un des messages sera exporté si la déduplication est activée lors de l’exportation des résultats de la recherche. Ainsi, même si le message d’origine ou le message copié a été modifié, aucun des messages révisés n’a été envoyé et, par conséquent, les valeurs des propriétés **InternetMessageId**, **ConversationTopic** et **BodyTagInfo** n’ont pas été mises à jour. Mais comme expliqué précédemment, les deux messages seront affichés dans les rapports d’exportation 
  
Notez que les messages uniques peuvent également être marqués comme étant des doublons lorsque la fonctionnalité de protection de page de copie sur écriture est activée, comme dans le cas d’une boîte aux lettres en conservation pour litige ou en conservation inaltérable. La fonctionnalité de copie sur écriture copie le message d’origine (et l’enregistre dans le dossier des versions du dossier éléments récupérables de l’utilisateur) avant l’enregistrement de la révision de l’élément d’origine. Dans ce cas, la copie révisée et le message d’origine (dans le dossier éléments récupérables) peuvent être considérés comme des messages en double et, par conséquent, un seul d’entre eux serait exporté.
  
> [!IMPORTANT]
> Si les limitations de l’algorithme de déduplication peuvent avoir un impact sur la qualité de vos résultats de recherche, vous ne devez pas activer la déduplication lorsque vous exportez des éléments. Si les situations décrites dans cette section ne sont probablement pas un facteur dans vos résultats de recherche et que vous souhaitez réduire le nombre d’éléments les plus susceptibles d’être dupliqués, vous devez envisager d’activer la déduplication. 
  
## <a name="more-information"></a>Plus d’informations

- Les informations contenues dans cet article s’appliquent lors de l’exportation des résultats de recherche à l’aide de l’un des outils eDiscovery suivants:
    
  - Recherche de contenu dans le centre de conformité dans Office 365
    
  - Découverte électronique inaltérable dans Exchange Online
    
  - Le centre eDiscovery dans SharePoint Online
    
- Pour plus d’informations sur l’exportation des résultats de la recherche, voir:
    
  - [Exporter la recherche de contenu](export-search-results.md)
    
  - [Exporter un rapport de recherche de contenu](export-a-content-search-report.md)
    
  - [Exporter les résultats de recherche de découverte électronique inaltérable vers un fichier PST](https://go.microsoft.com/fwlink/p/?linkid=832671)
    
  - [Exporter du contenu et créer des rapports dans le centre eDiscovery](https://support.office.com/article/7b2ea190-5f9b-4876-86e5-4440354c381a)
