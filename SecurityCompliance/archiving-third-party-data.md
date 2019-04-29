---
title: Archiver des données tierces dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid: MOE150
ms.assetid: 0ce338d5-3666-4a18-86ab-c6910ff408cc
description: Les administrateurs peuvent importer des données tierces à partir de plateformes de réseaux sociaux, de plateformes de messagerie instantanée et de documents de collaboration vers des boîtes aux lettres de votre organisation Office 365. Cela vous permet d'archiver des données à partir de Facebook, de Twitter et d'autres sources de données tierces dans Office 365. Vous pouvez ensuite utiliser et appliquer les fonctionnalités de conformité d'Office 365 (telles que la conservation légale, la découverte électronique, l'archivage inaltérable et les stratégies de rétention) pour les données tierces.
ms.openlocfilehash: b96c4852c3c9226219120a1be014ea3988cf91a2
ms.sourcegitcommit: e23b84ef4eee9cccec7205826b71ddfe9aaac2f8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33402912"
---
# <a name="archive-third-party-data-in-office-365"></a>Archiver des données tierces dans Office 365

Office 365 permet aux administrateurs d'importer et d'archiver des données tierces à partir de plateformes de médias sociaux, de plateformes de messagerie instantanée et de plateformes de collaboration sur des documents, vers des boîtes aux lettres de votre organisation Office 365. Voici des exemples de sources de données tierces que vous pouvez importer dans Office 365: 
  
- **Social** -Twitter, Facebook, Yammer et LinkedIn 
    
- **Messagerie instantanée** -Yahoo Messenger, GoogleTalk et Cisco Jabber 
    
- **Collaboration** sur les documents-zone et boîte de dépôt 
    
- **Industries verticales** -gestion de la relation client (par exemple, Salesforce chatter) et services financiers (par exemple, Bloomberg et Thomson Reuters) 
    
- **SMS/Text Messaging** -BlackBerry 
    
Une fois les données tierces importées, vous pouvez appliquer les fonctionnalités de conformité d'Office 365 (telles que la conservation pour litige, la découverte électronique, l'archivage inaltérable, l'audit, la surveillance et les stratégies de rétention d'Office 365) à ces données. Par exemple, lorsqu’une boîte aux lettres est placée en conservation pour litige, les données tierces sont conservées. Vous pouvez effectuer des recherches dans des données tierces à l'aide des outils eDiscovery de Microsoft. Vous pouvez également appliquer des stratégies d’archivage et de rétention aux données tierces, de la même manière que pour les données Microsoft. En bref, l'archivage des données tierces dans Office 365 peut aider votre organisation à respecter les stratégies gouvernementales et réglementaires.

Il existe deux façons d'importer et d'archiver des données tierces dans Office 365:

- **Utiliser un connecteur de données tiers dans le centre de sécurité _AMP_ Compliance Center** -utilisez un connecteur de données personnalisé disponible dans le centre de sécurité _AMP_ Compliance Center dans Office 365. Une fois que vous avez configuré et configuré le connecteur, il se connecte à la source de données tierce, convertit le contenu d'un élément en format de message électronique, puis importe l'élément dans une boîte aux lettres dans Office 365. Pour les sources de données tierces prises en charge par ces connecteurs et le processus pas à pas de configuration d'un connecteur, voir [utiliser des connecteurs d'exemple pour archiver des données tierces dans Office 365 (version d'évaluation)](archive-third-party-data-with-sample-connector.md).

- **Collaborez avec un partenaire Microsoft** -votre organisation travaille avec un partenaire Microsoft qui fournira un connecteur personnalisé qui sera configuré pour extraire des éléments de la source de données tierce (régulièrement), puis se connecter au Cloud Microsoft par un API tierce et importation de ces éléments dans Office 365. Le connecteur partenaire convertit également le contenu d'un élément de la source de données tierce en message électronique, puis les importe dans une boîte aux lettres dans Office 365. Pour obtenir la liste des partenaires avec lesquels vous pouvez travailler et le processus pas à pas pour cette méthode, consultez [collaborer avec un partenaire pour archiver des données tierces dans Office 365](work-with-partner-to-archive-third-party-data.md).