---
title: Recherche et suppression de messages - Aide de l’administrateur
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/20/2017
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 8c36bb03-e716-4fdd-9958-4aa7a2a1db42
description: Les administrateurs peuvent utiliser la cmdlet Search-Mailbox pour faire une recherche dans des boîtes aux lettres utilisateur, puis supprimer des messages d'une boîte aux lettres.
ms.openlocfilehash: a097b39aa179ed18c3d5426eeeacff204d48ee9b
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34158486"
---
# <a name="search-for-and-delete-messages---admin-help"></a>Recherche et suppression de messages - Aide de l’administrateur
  
Les administrateurs peuvent utiliser la cmdlet **Search-Mailbox** pour faire une recherche dans des boîtes aux lettres utilisateur, puis supprimer des messages d'une boîte aux lettres. 
  
Pour rechercher et supprimer des messages en une seule étape, exécutez la cmdlet **Search-Mailbox** avec le commutateur  _DeleteContent_. Cependant, quand vous effectuez cette opération, vous ne pouvez ni afficher un aperçu des résultats ni générer un journal des messages qui seront renvoyés par la recherche, et vous pourriez supprimer des messages par inadvertance. Pour afficher un aperçu du journal des messages identifiés par la recherche avant qu'ils ne soient supprimés, exécutez la cmdlet **Search-Mailbox** avec le commutateur  _LogOnly_. 
  
Pour plus de sécurité, vous pouvez d'abord copier les messages vers une autre boîte aux lettres à l'aide des paramètres  _TargetMailbox_ et  _TargetFolder_. De cette manière, vous êtes assuré de conserver une copie des messages supprimés pour pouvoir y accéder ultérieurement. 
  
## <a name="before-you-begin"></a>Avant de commencer

- Durée d'exécution estimée : 10 minutes. La durée réelle dépend de la taille de la boîte aux lettres et de la requête de recherche.
    
- Vous ne pouvez pas utiliser le Centre d'administration Exchange (CAE) pour effectuer ces procédures. Vous devez utiliser l'environnement de ligne de commande Exchange Management Shell.
    
- Vous devez disposer des deux rôles de gestion suivants pour rechercher et supprimer des messages dans les boîtes aux lettres des utilisateurs :
    
  - **Recherche de boîte aux lettres**-ce rôle vous permet de rechercher des messages dans plusieurs boîtes aux lettres de votre organisation. Ce rôle n'est pas attribué par défaut aux administrateurs. Pour vous attribuer vous-même ce rôle afin de pouvoir rechercher les boîtes aux lettres, ajoutez-vous en tant que membre du groupe de rôles Gestion de la découverte. Voir [Ajouter un utilisateur au groupe de rôles gestion de la découverte](http://technet.microsoft.com/library/729e09d8-614b-431f-ae04-ae41fb4c628e.aspx).
    
  - **Importation de boîte aux lettres** -ce rôle vous permet de supprimer des messages de la boîte aux lettres d’un utilisateur. Par défaut, ce rôle n'est attribué à aucun groupe de rôles. Pour supprimer des messages des boîtes aux lettres des utilisateurs, vous pouvez ajouter le rôle Importation/Exportation de boîte aux lettres au groupe de rôles Gestion de l'organisation. Pour plus d’informations, consultez la section «Ajouter un rôle à un groupe de rôles» dans [gérer des groupes de rôles](http://technet.microsoft.com/library/ab9b7a3b-bf67-4ba1-bde5-8e6ac174b82c.aspx) . 
    
- Si la fonctionnalité de récupération d'élément unique est activée pour la boîte aux lettres dont vous souhaitez supprimer des messages, vous devez d'abord la désactiver. Pour plus d'informations, voir [Activation de la récupération d'élément unique pour une boîte aux lettres](http://technet.microsoft.com/library/2e7f1bcd-8395-45ad-86ce-22868bd46af0.aspx).
    
- Si la boîte aux lettres dont vous souhaitez supprimer des messages est mise en conservation, nous vous recommandons de vous informer préalablement auprès du service de gestion des enregistrements ou juridique avant de désactiver la mise en attente et de supprimer le contenu de la boîte aux lettres. Une fois l’approbation obtenue, suivez les étapes décrites dans la rubrique [nettoyer le dossier éléments récupérables](http://technet.microsoft.com/library/82c310f8-de2f-46f2-8e1a-edb6055d6e69.aspx).
    
- Vous pouvez faire une recherche dans 10 000 boîtes aux lettres au maximum à l'aide de la cmdlet **Search-Mailbox**. Si vous êtes une organisation Exchange Online et que vous disposez de plus de 10 000 boîtes aux lettres, vous pouvez utiliser la fonctionnalité de recherche de conformité (ou la cmdlet **New-ComplianceSearch** correspondante) pour réaliser une recherche dans un nombre illimité de boîtes aux lettres. Vous pouvez ensuite utiliser la cmdlet **New-ComplianceSearchAction** pour supprimer les messages renvoyés par la recherche de conformité. Pour plus d'informations, reportez-vous à la rubrique [Recherche et suppression de messages électroniques dans votre organisation Office 365](https://go.microsoft.com/fwlink/p/?LinkId=786856).
    
- Si vous incluez une requête de recherche (à l'aide du paramètre  *SearchQuery*  ), la cmdlet **Search-Mailbox** renverra au maximum 10 000 éléments dans les résultats de recherche. Ainsi, si vous incluez une requête de recherche, vous devrez peut-être exécuter la commande **Search-Mailbox** plusieurs fois pour supprimer plus de 10 000 éléments. 
    
- La boîte aux lettres d'archivage de l'utilisateur est également incluse dans la recherche quand vous exécutez la cmdlet **Search-Mailbox**. De même, les éléments de la boîte aux lettres d'archivage principale sont supprimés quand vous utilisez la cmdlet **Search-Mailbox** avec le commutateur  _DeleteContent_. Pour éviter cela, vous pouvez inclure le commutateur  *DoNotIncludeArchive*  . Par ailleurs, nous vous recommandons de ne pas utiliser le commutateur _DeleteContent_ pour supprimer les messages dans les boîtes aux lettres Exchange Online dont l’archivage est automatiquement étendu, car une perte de données inattendue peut se produire. 
    
## <a name="search-messages-and-log-the-search-results"></a>Rechercher des messages et enregistrer les résultats de la recherche

Cet exemple permet d'effectuer une recherche dans la boîte aux lettres d'April Stewart au niveau des messages dont le champ Objet contient l'expression « Your bank statement » (Votre relevé de compte) et de consigner les résultats de la recherche dans le dossier SearchAndDeleteLog de la boîte aux lettres de l'administrateur. Les messages ne sont ni copiés ni supprimés de la boîte aux lettres cible.
  
```
Search-Mailbox -Identity "April Stewart" -SearchQuery 'Subject:"Your bank statement"' -TargetMailbox administrator -TargetFolder "SearchAndDeleteLog" -LogOnly -LogLevel Full
```

Cet exemple permet d'effectuer une recherche dans toutes les boîtes aux lettres de l'organisation au niveau des messages comprenant n'importe quel type de fichier joint qui contient le mot « Trojan » dans le nom de fichier et envoie un message de journal à la boîte aux lettres de l'administrateur.
  
```
Get-Mailbox -ResultSize unlimited | Search-Mailbox -SearchQuery attachment:trojan* -TargetMailbox administrator -TargetFolder "SearchAndDeleteLog" -LogOnly -LogLevel Full
```

Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Search-Mailbox](http://technet.microsoft.com/library/9ee3b02c-d343-4816-a583-a90b1fad4b26.aspx).
  
 
## <a name="search-and-delete-messages"></a>Rechercher et supprimer des messages

Cet exemple permet d'effectuer une recherche dans la boîte aux lettres d'April Stewart au niveau des messages dont le champ Objet contient l'expression « Your bank statement » et de supprimer les messages de la boîte aux lettres source sans copier les résultats de la recherche dans un autre dossier. Comme expliqué précédemment, le rôle de gestion Importation/Exportation de boîte aux lettres doit vous avoir été attribué pour que vous puissiez supprimer des messages de la boîte aux lettres d'un utilisateur.
  
> [!IMPORTANT]
> Quand vous utilisez la cmdlet **Search-Mailbox** avec le commutateur  _DeleteContent_, les messages sont définitivement supprimés de la boîte aux lettres source. Avant de supprimer définitivement des messages, nous vous conseillons d'utiliser le commutateur  _LogOnly_ pour générer un journal des messages identifiés lors de la recherche avant qu'ils ne soient supprimés ou de copier les messages vers une autre boîte aux lettres avant leur suppression de la boîte aux lettres source. 
  
```
Search-Mailbox -Identity "April Stewart" -SearchQuery 'Subject:"Your bank statement"' -DeleteContent
```

Cet exemple permet d'effectuer une recherche dans la boîte aux lettres d'April Stewart au niveau des messages dont le champ Objet contient l'expression « Your bank statement », de copier les résultats de la recherche dans le dossier AprilStewart-DeletedMessages de la boîte aux lettres BackupMailbox et de supprimer les messages de la boîte aux lettres d'April.
  
```
Search-Mailbox -Identity "April Stewart" -SearchQuery 'Subject:"Your bank statement"' -TargetMailbox "BackupMailbox" -TargetFolder "AprilStewart-DeletedMessages" -LogLevel Full -DeleteContent
```

Cet exemple permet d'effectuer une recherche dans toutes les boîtes aux lettres de l'organisation au niveau des messages ayant pour objet « Download this file » et les supprime définitivement. 
  
```
Get-Mailbox -ResultSize unlimited | Search-Mailbox -SearchQuery 'Subject:"Download this file"' -DeleteContent
```

Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Search-Mailbox](http://technet.microsoft.com/library/9ee3b02c-d343-4816-a583-a90b1fad4b26.aspx).

## <a name="using-the--loglevel-full-parameter"></a>Utilisation du paramètre -LogLevel Full

Dans certains des exemples ci-dessus, le paramètre  _LogLevel_ avec la valeur  `Full` est utilisé pour consigner des informations détaillées concernant les résultats renvoyés par la cmdlet **Search-Mailbox**. Lorsque vous incluez ce paramètre, un courrier électronique est créé et envoyé à la boîte aux lettres spécifiée par le paramètre  _TargetMailbox_. Le fichier journal (au format CSV nommé Résultats recherche.csv) est joint au courrier électronique et est disponible dans le dossier indiqué par le paramètre  _TargetFolder_. Le fichier journal comporte une ligne par message inclus dans les résultats de la recherche lorsque vous exécutez la cmdlet **Search-Mailbox**. 
