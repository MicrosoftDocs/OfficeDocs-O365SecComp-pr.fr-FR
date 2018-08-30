---
title: Recherche de contenu permet de rechercher des données tiers qui a été importées dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/27/2017
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: ec2677ff-c4d7-4363-a9e7-22c80e015688
description: Utiliser l’outil de découverte électronique de recherche de contenu pour rechercher des éléments qui ont été importés pour les boîtes aux lettres dans Office 365 à partir d’une source de données tierce. Vous pouvez créer une requête pour rechercher tous les éléments importés ou pour créer une requête pour rechercher des types de données tiers spécifiques. Cet article répertorie les valeurs que vous pouvez utiliser dans une requête de mot clé pour rechercher les types de données de tiers qui peuvent être importés dans Office 365.
ms.openlocfilehash: 90d9dc52dcd9dba9bc273dfcf1c5f22e3913d6ba
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528350"
---
# <a name="use-content-search-to-search-third-party-data-that-was-imported-to-office-365"></a>Recherche de contenu permet de rechercher des données tiers qui a été importées dans Office 365

Vous pouvez utiliser l' [outil de découverte électronique de recherche de contenu](content-search.md) de sécurité Office 365 &amp; centre de conformité pour rechercher des éléments qui ont été importés pour les boîtes aux lettres dans Office 365 à partir d’une source de données tierce. Vous pouvez créer une requête pour rechercher importé tous les éléments de données de tiers ou vous pouvez créer une requête de recherche uniquement les éléments de données tiers spécifiques. En outre, vous pouvez également créer une stratégie de conservation basée sur une requête ou une découverte basée sur une requête attente permettant de conserver des données tierces dans Office 365. 
  
Pour plus d’informations sur l’importation des données tierces et une liste des types de données de tiers qui peuvent être importés dans Office 365, voir [l’archivage des données tierces dans Office 365](archiving-third-party-data.md). 
  
## <a name="creating-a-query-to-search-all-third-party-data"></a>Création d’une requête pour rechercher toutes les données de tiers

Recherche (ou mise en attente) n’importe quel type de données de tiers que vous avez importés vers Office 365, vous pouvez vous permet de la `kind:externaldata` paire de messages valeur de la propriété dans la zone mots clés pour une recherche de contenu ou lors de la création d’une suspension basée sur une requête. Par exemple, pour rechercher des éléments qui ont été importés à partir d’une source de données tierce et contiennent le mot « contoso » dans la propriété Subject de l’élément importé, vous utiliseriez la requête suivante : 
  
```
kind:externaldata AND subject:contoso
```

L’exemple de requête de mot clé précédent inclut la propriété subject. Pour obtenir la liste des autres propriétés d’éléments de données tiers peuvent inclus dans une requête de mot clé, voir la section « Plus d’informations » dans [l’archivage des données tierces dans Office 365](archiving-third-party-data.md#more-information).
  
Lorsque vous créez des requêtes pour rechercher et bloquer les données tiers, vous pouvez également utiliser des conditions pour affiner les résultats de recherche. Pour plus d’informations sur la création de requêtes de recherche de contenu, voir [conditions de recherche pour la recherche de contenu et les requêtes de mot clé](keyword-queries-and-search-conditions.md).
  
## <a name="creating-a-query-to-search-specific-types-of-third-party-data"></a>Création d’une requête pour rechercher des types spécifiques de données de tiers

Au lieu de la recherche dans tous les types de données tiers, vous pouvez créer de requêtes que seule la recherche pour un type de spécifier des données tiers à l’aide de la paire de valeur de la propriété message suivante dans la zone mots clés pour une recherche de contenu :
  
```
itemclass:ipm.externaldata.<third-party data type>* 
```

Par exemple, pour rechercher uniquement les données Facebook qui contient le mot « contoso » dans la propriété Subject, vous utiliseriez la requête suivante :
  
```
itemclass:ipm.externaldata.Facebook* AND subject:contoso
```

Le tableau suivant répertorie les types de données de tiers que vous pouvez rechercher et la valeur à utiliser pour le `itemclass:` message, propriété au service de recherche spécifiquement pour ce type de données de tiers. Notez que la syntaxe de requête n’est pas respectant la casse. 
  
|**Type de données de tiers**|**Valeur `itemclass:` propriété**|
|:-----|:-----|
|AIM  <br/> | `ipm.externaldata.AIM*` <br/> |
|American Idol  <br/> | `ipm.externaldata.AmericanIdol*` <br/> |
|AOL avec client Pivot   <br/> | `ipm.externaldata.Pivot.IM` <br/> |
|Apple Juice  <br/> | `ipm.externaldata.AppleJuice*` <br/> |
|Ares  <br/> | `ipm.externaldata.Ares*` <br/> |
|Axs Encrypted  <br/> | `ipm.externaldata.AxsEncrypted*` <br/> |
|Axs Exchange  <br/> | `ipm.externaldata.AxsExchange*` <br/> |
|Axs Local Archive  <br/> | `ipm.externaldata.AxsLocalArchive*` <br/> |
|Espace réservé AX  <br/> | `ipm.externaldata.AxsPlaceHolder*` <br/> |
|Axs Signed  <br/> | `ipm.externaldata.AxsSigned*` <br/> |
|Bazaarvoice  <br/> | `ipm.externaldata.Bazaarvoice*` <br/> |
|BearShare  <br/> | `ipm.externaldata.Bearshare*` <br/> |
|BitTorrent  <br/> | `ipm.externaldata.BitTorrent*` <br/> |
|BlackBerry  <br/> | `ipm.externaldata.Blackberry*` <br/> |
|Journaux d’appels blackBerry  <br/> | `ipm.externaldata.BlackBerryCall*` <br/> |
|Messenger blackBerry  <br/> | `ipm.externaldata.BlackBerryMessenger*` <br/> |
|BlackBerry code confidentiel  <br/> | `ipm.externaldata.BlackBerryPIN*` <br/> |
|BlackBerry SMS  <br/> | `ipm.externaldata.BlackBerrySMS*` <br/> |
|Bloomberg  <br/> | `ipm.externaldata.Bloomberg*` <br/> |
|Bloomberg Mail
  <br/> | `ipm.externaldata.BloombergMail*` <br/> |
|Messagerie Bloomberg  <br/> | `ipm.externaldata.BloombergMessaging*` <br/> |
|Box
  <br/> | `ipm.externaldata.Box*` <br/> |
|Messagerie instantanée de Cisco &amp; serveur de présence  <br/> | `ipm.externaldata.Jabber.IM` <br/> |
|Cisco Jabber  <br/> | `ipm.externaldata.Jabber*` <br/> |
|CipherCloud for Salesforce Chatter  <br/> | `ipm.externaldata.Chatter.Post` <br/>  `ipm.externaldata.Chatter.Comment` <br/> |
|Direct Connect  <br/> | `ipm.externaldata.DirectConnect*` <br/> |
|Facebook  <br/> | `ipm.externaldata.Facebook*` <br/> |
|FastTrack  <br/> | `ipm.externaldata.FastTrack*` <br/> |
|FXConnect  <br/> | `ipm.externaldata.FXConnect.chat` <br/> |
|Flickr
  <br/> | `ipm.externaldata.Flickr*` <br/> |
|Gnutella  <br/> | `ipm.externaldata.Gnutella*` <br/> |
|Google+
  <br/> | `ipm.externaldata.GooglePlus*` <br/> |
|Google Talk  <br/> | `ipm.externaldata.GoogleTalk*` <br/> |
|GoToMyPC  <br/> | `ipm.externaldata.GoToMyPC*` <br/> |
|HipChat  <br/> | `ipm.externaldata.HipChat*` <br/> |
|Hopster  <br/> | `ipm.externaldata.Hopster*` <br/> |
|HubConnex  <br/> | `ipm.externaldata.HubConnex*` <br/> |
|Connexions IBM  <br/> | `ipm.externaldata.Connections*` <br/> |
|IBM SameTime  <br/> | `ipm.externaldata.Sametime*` <br/> |
|Conversation ICE  <br/> | `ipm.externaldata.ICEChat.Chat` <br/> |
|Indii Messenger
  <br/> | `ipm.externaldata.Indii*` <br/> |
|Instagram
  <br/> | `ipm.externaldata.Instagram*` <br/> |
|Instant Bloomberg
  <br/> | `ipm.externaldata.InstantBloomberg*` <br/> |
|InvestEdge  <br/> | `ipm.externaldata.InvestEdge*` <br/> |
|IRC  <br/> | `ipm.externaldata.IRC*` <br/> |
|Jive
  <br/> | `ipm.externaldata.Jive*` <br/> |
|JiveApiRetention  <br/> | `ipm.externaldata.JiveApiRetention*` <br/> |
|JXTA  <br/> | `ipm.externaldata.JXTA*` <br/> |
|LinkedIn  <br/> | `ipm.externaldata.LinkedIn*` <br/> |
|MFTP  <br/> | `ipm.externaldata.MFTP*` <br/> |
|Communications unifiées de Microsoft  <br/> | `ipm.externaldata.MicrosoftUC*` <br/> |
|Aligner l’esprit  <br/> | `ipm.externaldata.MindAlign*` <br/> |
|Mobile Guard  <br/> | `ipm.externaldata.MobileGuard*` <br/> |
|MSN  <br/> | `ipm.externaldata.MSN*` <br/> |
|MySpace  <br/> | `ipm.externaldata.MySpace*` <br/> |
|NEONetwork  <br/> | `ipm.externaldata.NEONetwork*` <br/> |
|OpenNap  <br/> | `ipm.externaldata.OpenNap*` <br/> |
|Pinterest  <br/> | `ipm.externaldata.Pinterest*` <br/> |
|Pivot  <br/> | `ipm.externaldata.Pivot*` <br/> |
|QQ  <br/> | `ipm.externaldata.QQ*` <br/> |
|Microsoft SharePoint  <br/> | `ipm.externaldata.SharePoint*` <br/> |
|Salesforce Chatter  <br/> | `ipm.externaldata.Chatter*` <br/> |
|Skype Entreprise  <br/> | `ipm.externaldata.Skype*` <br/> |
|Slack Enterprise Grid  <br/> | `ipm.externaldata.Slack.IM` <br/> |
|SoftEther  <br/> | `ipm.externaldata.SoftEther*` <br/> |
|
Squawker
  <br/> | `ipm.externaldata.Squawker*` <br/> |
|Symphony
  <br/> | `ipm.externaldata.Symphony*` <br/> |
|Thomson Reuters  <br/> | `ipm.externaldata.Reuters*` <br/> |
| Thomson Reuters Eikon Messenger
  <br/> | `ipm.externaldata.ReutersEikon*` <br/> |
|Tor  <br/> | `ipm.externaldata.Tor*` <br/> |
|TTT  <br/> | `ipm.externaldata.TTT*` <br/> |
|Twitter  <br/> | `ipm.externaldata.Twitter*` <br/> |
|UBS Chat
  <br/> | `ipm.externaldata.UBS*` <br/> |
|Vimeo  <br/> | `ipm.externaldata.Vimeo*` <br/> |
|WinMX  <br/> | `ipm.externaldata.WinMX*` <br/> |
|Winny  <br/> | `ipm.externaldata.Winny*` <br/> |
|Yahoo!  <br/> | `ipm.externaldata.Yahoo!*` <br/> |
|Yammer  <br/> | `ipm.externaldata.Yammer*` <br/> |
|YellowJacket  <br/> | `ipm.externaldata.YellowJacket*` <br/> |
|YouTube  <br/> | `ipm.externaldata.YouTube*` <br/> |
