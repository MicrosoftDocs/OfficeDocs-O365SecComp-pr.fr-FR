---
title: Contenu stocké dans les boîtes aux lettres Exchange Online
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: ''
ROBOTS: NOINDEX, NOFOLLOW
description: Les données générées par des applications basées sur le nuage dans Office 365 sont stockées dans la boîte aux lettres Exchange Online d’un utilisateur dans le Cloud Microsoft.
ms.openlocfilehash: d2d126d28a9b92962af7637610282e99e7685594
ms.sourcegitcommit: ecc823c2a4f1465114cf1d3a4630e31c47779ddc
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2019
ms.locfileid: "35079398"
---
# <a name="content-stored-in-exchange-online-mailboxes"></a>Contenu stocké dans les boîtes aux lettres Exchange Online

Une boîte aux lettres dans Exchange Online est principalement utilisée pour stocker des éléments liés au courrier électronique, tels que des messages, des éléments de calendrier, des tâches et des notes. Mais cela devient un plus plus d’applications Office 365 basées sur le Cloud qui stockent également leurs données dans la boîte aux lettres d’un utilisateur. L’un des avantages du stockage de données dans une boîte aux lettres est que vous pouvez utiliser les outils de recherche dans la recherche de contenu, eDiscovery, Advanced eDiscovery et les enquêtes de données pour rechercher, afficher et exporter les données à partir de ces applications basées sur le Cloud. Les données de certaines de ces applications sont stockées dans des dossiers cachés situés dans une sous-arborescence non de message interpersonnel (non-IPM) dans la boîte aux lettres. Cela signifie que les données sont masquées dans l’affichage de l’utilisateur lorsqu’elles utilisent Outlook ou d’autres clients de messagerie pour accéder à leur boîte aux lettres.

Le tableau suivant répertorie les applications Office 365 qui stockent des données dans une boîte aux lettres en nuage. Le tableau décrit également le type de contenu que chaque application stocke.

|Application Office 365  |Description  |
|:---------|:---------|
|Formulaires     <br/> |Les formulaires (stockés sous forme de fichier PDF) et les réponses à un formulaire (stocké dans un fichier CSV) sont joints aux messages électroniques et stockés dans un dossier masqué dans la boîte aux lettres de l’utilisateur qui a créé le formulaire. Lorsque vous exportez du contenu à partir de formulaires dans un fichier PST, ces données se trouvent dans le dossier **ApplicationDataRoot** d’un sous-dossier nommé avec le GUID suivant: **c9a559d2-7aab-4F13-A6ED-e7e9c52aec87**.        <br/> |
|Groupes Office 365    <br/>|  Les messages électroniques, les éléments de calendrier, les contacts (personnes), les notes et les tâches sont stockés dans la boîte aux lettres associée à un groupe Office 365.       <br/> |
|Outlook/Exchange Online<br/>|  Les messages électroniques, les éléments de calendrier, les contacts (personnes), les notes et les tâches sont stockés dans la boîte aux lettres d’un utilisateur.       <br/> |
|Contacts    <br/> |  Les contacts dans l’application contacts (qui sont les mêmes contacts que ceux accessibles dans Outlook) sont stockés dans la boîte aux lettres d’un utilisateur.      <br/> |
|Planification de la classe     <br/> |   Les plans créés au cours de la planification de classe sont stockés dans la boîte aux lettres du groupe Office 365 correspondant qui est mis en service lors de la création d’un plan. L’alias de la boîte aux lettres de groupe est le nom du plan.      <br/> |
|Skype Entreprise    <br/>  | Les conversations dans Skype entreprise sont stockées dans le dossier historique des conversations dans la boîte aux lettres d’un utilisateur. Si la boîte aux lettres d’un participant à une réunion Skype est placée en conservation pour litige ou affectée à une stratégie de rétention, les fichiers joints à une réunion sont conservés dans la boîte aux lettres des participants.         <br/> |
|Sway     <br/> |  Les Sways sont stockés sous forme de fichier HTML joint à un message électronique et stockés dans un dossier masqué dans la boîte aux lettres de l’utilisateur qui a créé le Sway. Lorsque vous exportez du contenu à partir de Sway dans un fichier PST, ces données se trouvent dans le dossier **ApplicationDataRoot** dans un sous-dossier nommé avec le GUID suivant) **905fcf26-4EB7-48A0-9ff0-8dcc7194b5ba**.       <br/> |
|Tâches    <br/> |  Les tâches de l’application tâches (qui sont les mêmes que celles qui sont accessibles dans Outlook) sont stockées dans la boîte aux lettres d’un utilisateur.       <br/> |
|Équipes    <br/>  |Les conversations qui font partie d’un canal teams sont stockées dans la boîte aux lettres associée à l’équipe. Les conversations qui font partie de la liste des conversations dans Teams (également appelées « *conversations 1 x N*)» sont stockées dans la boîte aux lettres des utilisateurs qui participent à la conversation. Par ailleurs, les informations de synthèse pour les réunions et les appels dans une chaîne teams sont stockées dans les boîtes aux lettres des utilisateurs qui composent la réunion ou l’appel. <br/> | 
|To-Do  <br/> | Les tâches (appelées *actions*, qui sont enregistrées dans les listes de tâches) de l’application de la tâche sont stockées dans la boîte aux lettres d’un utilisateur.        <br/> |
||||

> [!NOTE]
> Pour l’instant, si une boîte aux lettres est placée en conservation (en utilisant des suspensions dans la découverte électronique et des cas avancés de découverte électronique), le contenu des formulaires et de Sway ne sera pas préservé par la suspension. 