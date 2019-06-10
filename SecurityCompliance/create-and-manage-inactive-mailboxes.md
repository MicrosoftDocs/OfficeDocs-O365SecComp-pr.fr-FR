---
title: Créer et gérer des boîtes aux lettres inactives dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 296a02bd-ebde-4022-900e-547acf38ddd7
description: Vous pouvez créer une boîte aux lettres inactive dans Office 365 en appliquant une stratégie de rétention de blocage ou d’Office 365 à la boîte aux lettres, puis en supprimant le compte d’utilisateur Office 365 correspondant. Les éléments d’une boîte aux lettres inactive sont conservés pendant la durée de la conservation ou de la stratégie de rétention qui lui a été appliquée avant qu’elle ne soit devenue inactive. Pour supprimer définitivement une boîte aux lettres inactive, supprimez simplement la stratégie de conservation ou de rétention.
ms.openlocfilehash: e07b062f6b77f18589334b141e38edddc5ea18c5
ms.sourcegitcommit: f88f14999aeb70ecf265cd98eb09a3304b150be8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/07/2019
ms.locfileid: "34768949"
---
# <a name="create-and-manage-inactive-mailboxes-in-office-365"></a>Créer et gérer des boîtes aux lettres inactives dans Office 365

Office 365 vous permet de conserver le contenu des boîtes aux lettres supprimées. Cette fonctionnalité est appelée [boîtes aux lettres inactives](inactive-mailboxes-in-office-365.md). Inactive mailboxes allow you to retain former employees' email after they leave your organization. Une boîte aux lettres devient inactive lorsqu’une conservation pour litige ou une stratégie de rétention Office 365 (créée dans le centre de sécurité et de conformité dans Office 365 ou Microsoft 365) est appliquée à la boîte aux lettres avant la suppression du compte d’utilisateur Office 365 correspondant. The contents of an inactive mailbox are retained for the duration of the hold that was placed on the mailbox before it was made inactive. Cela permet aux administrateurs, aux responsables de la mise en conformité et aux gestionnaires d’enregistrements d’utiliser la recherche de contenu pour rechercher et exporter le contenu d’une boîte aux lettres inactive. Inactive mailboxes can't receive email and aren't displayed in your organization's shared address book or other lists.
  
> [!NOTE]
> Nous avons reporté l'échéance du 1er juillet 2017 afin de créer des conservations inaltérables pour rendre une boîte aux lettres inactive. Cependant, plus tard cette année ou au début de l'année prochaine, vous ne pourrez plus créer de conservations inaltérables dans Exchange Online. Actuellement, seules les conservations pour litige et les stratégies de rétention Office 365 peuvent être utilisées pour créer une boîte aux lettres inactive. Toutefois, les boîtes aux lettres inactives existantes qui se trouvent en conservation inaltérable seront toujours prises en charge. Vous pouvez continuer à gérer les conservations inaltérables sur les boîtes aux lettres inactives. Cela inclut la modification de la durée d'une conservation inaltérable et la suppression définitive d'une boîte aux lettres inactive en supprimant la conservation inaltérable. 
  
## <a name="before-you-begin"></a>Avant de commencer

- Pour désactiver une boîte aux lettres, vous devez lui avoir affecté une licence Exchange Online plan 2 afin qu’une conservation pour litige ou une stratégie de rétention Office 365 puisse être appliquée à la boîte aux lettres avant d’être supprimée. Les licences Exchange Online plan 2 font partie d’un abonnement Office 365 entreprise E3 et E5. Si une boîte aux lettres est attribuée à une licence Exchange Online plan 1 (qui fait partie d’un abonnement Office 365 Enterprise E1), vous devez lui attribuer une licence d’archivage Exchange Online distincte de sorte qu’une conservation puisse être appliquée à la boîte aux lettres avant d’être supprimée. Pour plus d'informations, consultez la page [Archivage Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=286153).
    
- La licence associée à la boîte aux lettres Exchange Online supprimée sera disponible une fois que vous aurez supprimé la boîte aux lettres Office 365 correspondante. Vous pouvez ensuite [attribuer des licences aux utilisateurs dans Office 365 pour les entreprises](https://support.office.com/article/997596b5-4173-4627-b915-36abac6786dc) à un autre utilisateur. 
    
- Si une conservation pour litige ou une stratégie de rétention Office 365 (configurée pour conserver ou conserver et supprimer du contenu) n’est pas appliquée à une boîte aux lettres avant sa suppression, le contenu de la boîte aux lettres n’est pas conservé ni découvrable. Cependant, la boîte aux lettres peut être récupérée dans les 30 jours suivant sa suppression, mais, à défaut de récupération, elle est définitivement supprimée avec son contenu à l'issue de cette période.
    
- For more information about Litigation Hold, see [In-Place Hold and Litigation Hold](https://go.microsoft.com/fwlink/p/?LinkId=846124). Pour en savoir plus sur les stratégies de rétention Office 365, consultez la rubrique [Vue d'ensemble des stratégies de rétention dans Office 365](retention-policies.md).
  
## <a name="create-an-inactive-mailbox"></a>Créer une boîte aux lettres inactive

La création d’une boîte aux lettres inactive implique deux étapes: 1) en plaçant la boîte aux lettres en conservation pour litige ou en y appliquant une stratégie de rétention Office 365, et 2) en supprimant la boîte aux lettres ou le compte d’utilisateur Office 365 correspondant. Une fois la boîte aux lettres inactive, son contenu est conservé jusqu'au retrait de la conservation ou de la stratégie de rétention.
  
### <a name="step-1-place-a-mailbox-on-litigation-hold-or-apply-an-office-365-retention-policy"></a>Étape 1 : Placement d'une boîte aux lettres en conservation pour litige ou application d'une stratégie de rétention Office 365

Placer une boîte aux lettres en conservation pour litige ou appliquer une stratégie de rétention Office 365 (configurée pour conserver ou conserver et supprimer du contenu) conserve le contenu de la boîte aux lettres avant qu’elle ne soit supprimée. Ces deux types de conservation conservent l'ensemble du contenu de la boîte aux lettres, notamment les éléments supprimés et les versions d'origine des éléments modifiés. Les éléments supprimés et modifiés sont conservés dans la boîte aux lettres inactive pendant une période spécifiée, jusqu'à la suppression définitive de la boîte aux lettres inactive en supprimant la conservation ou la stratégie de rétention appliquée.
  
Si une boîte aux lettres est déjà placée en conservation, ou si une stratégie de rétention Office 365 est déjà appliquée à une boîte aux lettres, il vous suffit de supprimer le compte d'utilisateur Office 365 correspondant, comme expliqué à l'étape 2.
  
Pour savoir comment placer une boîte aux lettres en conservation pour litige ou appliquer une stratégie de rétention Office 365, consultez les rubriques suivantes :
  
- [Place a mailbox on Litigation Hold](https://go.microsoft.com/fwlink/?linkid=856286)
    
- [Vue d'ensemble des stratégies de rétention](retention-policies.md)
    
> [!NOTE]
> Pour les conservations pour litige et les stratégies de rétention Office 365, vous pouvez créer une conservation indéfinie ou temporaire. En cas de conservation indéfinie, le contenu de la boîte aux lettres inactive est conservé pour une durée illimitée, ou jusqu'à la suppression de la conservation ou jusqu'à la modification de la durée de conservation. Une fois la conservation ou la stratégie de rétention supprimée (en supposant que la boîte aux lettres a été supprimée depuis plus de 30 jours), la boîte aux lettres inactive est définitivement supprimée et son contenu n'est plus conservé ni détectable. En cas de conservation ou de stratégie de rétention Office 365 temporaire, vous en spécifiez la durée. Cette durée s'applique à un élément et est calculée à partir de la date de réception ou de création de ce dernier. Après l'expiration de la conservation d'un élément de boîte aux lettres, si cet élément est déplacé vers, ou se trouve dans le dossier Éléments récupérables de la boîte aux lettres inactive, l'élément est supprimé définitivement (purgé) de la boîte aux lettres inactive après l'expiration de la période de rétention de l'élément supprimé. 
  
### <a name="step-2-delete-the-mailbox"></a>Étape 2 : Suppression de la boîte aux lettres

Lorsqu'une conservation ou une stratégie de rétention Office 365 est appliquée à la boîte aux lettres, vous pouvez la supprimer. La meilleure façon de supprimer une boîte aux lettres est de supprimer le compte d’utilisateur Office 365 correspondant dans le centre d’administration Microsoft 365. Pour plus d’informations sur la suppression des comptes d’utilisateur Office 365, consultez la rubrique [supprimer un utilisateur de votre organisation](https://support.office.com/article/d5155593-3bac-4d8d-9d8b-f4513a81479e).
  
> [!NOTE]
> Vous pouvez également supprimer la boîte aux lettres en utilisant la cmdlet **Remove-Mailbox** dans Exchange Online PowerShell. Pour plus d’informations, consultez la rubrique [supprimer ou restaurer des boîtes aux lettres utilisateur dans Exchange Online](https://go.microsoft.com/fwlink/?linkid=856287). 
  

## <a name="view-a-list-of-inactive-mailboxes"></a>Afficher la liste des boîtes aux lettres inactives

Pour afficher la liste des boîtes aux lettres inactives dans votre organisation, procédez comme suit:
  
1. Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous à l’aide des informations d’identification d’un compte administrateur de votre organisation Office 365. 
    
2. Cliquez sur rétention de la **gouvernance** > **** des données.
    
3. Sur la **** page rétention, cliquez sur **autres**![barres](media/9723029d-e5cd-4740-b5b1-2806e4f28208.gif)d’ellipse de la barre de navigation, puis cliquez sur **boîtes aux lettres**inactives.
    
    ![Sur la page rétention, cliquez sur autres, puis cliquez sur boîtes aux lettres inactives pour afficher la liste des boîtes aux lettres inactives.](media/761bd90c-3e37-48f9-b1b9-479e90fea267.png)
  
    La page **boîtes aux lettres** inactives s’affiche. Remarque le nombre total de boîtes aux lettres inactives dans votre organisation est affiché. 
    
    ![Une liste de toutes les boîtes aux lettres inactives de votre organisation s’affiche.](media/57d9d183-0c6c-4bd8-82e7-115f7b7b6de7.png)
  
Vous pouvez également exécuter la commande suivante dans Exchange Online PowerShell pour afficher la liste des boîtes aux lettres inactives.

```
 Get-Mailbox -InactiveMailboxOnly | FT DisplayName,PrimarySMTPAddress,WhenSoftDeleted
```

Vous pouvez cliquer ![sur Exporter les résultats](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) de la recherche **Exporter** pour afficher ou télécharger un fichier csv contenant des informations supplémentaires sur les boîtes aux lettres inactives dans votre organisation. 
  
Vous pouvez également exécuter la commande suivante pour exporter la liste des boîtes aux lettres inactives et d’autres informations dans un fichier CSV. Dans cet exemple, le fichier CSV est créé dans le répertoire actif.

```
Get-Mailbox -InactiveMailboxOnly | Select Displayname,PrimarySMTPAddress,DistinguishedName,ExchangeGuid,WhenSoftDeleted | Export-Csv InactiveMailboxes.csv -NoType
```
   
> [!NOTE]
> Il est possible qu’une boîte aux lettres inactive ait la même adresse SMTP qu’une boîte aux lettres utilisateur active. Dans ce cas, la valeur de la propriété **distinguishedName** ou **ExchangeGuid** peut être utilisée pour identifier une boîte aux lettres inactive de manière unique. 
  
## <a name="search-and-export-the-contents-of-an-inactive-mailbox"></a>Recherche et exportation du contenu d'une boîte aux lettres inactive

Vous pouvez accéder au contenu de la boîte aux lettres inactive à l’aide de l’outil de recherche de contenu dans le centre de sécurité & conformité. When you search an inactive mailbox, you can create a keyword search query to search for specific items or you can return the entire contents of the inactive mailbox. You can preview the search results or export the search results to an Outlook Data (PST) file or as individual email messages. For step-by-step procedures for searching mailboxes and exporting search results, see the following topics:
  
- [Recherche de contenu dans Office 365](content-search.md)
    
- [Exporter les résultats de la recherche de contenu](export-search-results.md)
    
Voici quelques éléments à garder à l’esprit lors de la recherche de boîtes aux lettres inactives.
  
- Si une recherche de contenu inclut une boîte aux lettres utilisateur et que celle-ci est devenue inactive, la recherche de contenu continue à rechercher dans la boîte aux lettres inactive lorsque vous relancez la recherche après qu’elle a été inactive.
    
- Dans certains cas, un utilisateur peut avoir une boîte aux lettres active et une boîte aux lettres inactive possédant la même adresse SMTP. Dans ce cas, seule la boîte aux lettres spécifique que vous sélectionnez comme emplacement pour une recherche de contenu fera l’objet d’une recherche. En d’autres termes, si vous ajoutez la boîte aux lettres d’un utilisateur à une recherche, vous ne pouvez pas supposer que leurs boîtes aux lettres actives et inactives seront recherchées; seule la boîte aux lettres que vous ajoutez explicitement à la recherche sera recherchée.
    
- Nous vous recommandons vivement d’éviter d’avoir une boîte aux lettres active et une boîte aux lettres inactive avec la même adresse SMTP. Si vous devez réutiliser l’adresse SMTP actuellement attribuée à une boîte aux lettres inactive, nous vous recommandons de récupérer la boîte aux lettres inactive ou de restaurer le contenu d’une boîte aux lettres inactive vers une boîte aux lettres active (ou l’archive d’une boîte aux lettres active), puis de supprimer le boîte aux lettres inactive.
    
## <a name="change-the-hold-duration-for-an-inactive-mailbox"></a>Modifier la durée de la conservation pour une boîte aux lettres inactive

Une fois qu’une boîte aux lettres est devenue inactive, vous pouvez modifier la durée de la conservation ou de la stratégie de rétention Office 365 appliquée à la boîte aux lettres inactive. Pour obtenir des procédures pas à pas, consultez [la rubrique modifier la durée de la conservation pour une boîte aux lettres inactive dans Office 365](change-the-hold-duration-for-an-inactive-mailbox.md).
  
## <a name="recover-an-inactive-mailbox"></a>Récupérer une boîte aux lettres inactive

Si un ancien employé réintègre votre organisation, ou si un nouvel employé est embauché pour assumer les responsabilités d'un employé qui a quitté l'organisation, vous pouvez récupérer le contenu de la boîte aux lettres inactive. Lorsque vous récupérez une boîte aux lettres inactive, la boîte aux lettres est convertie en une nouvelle boîte aux lettres, le contenu et la structure de dossiers de la boîte aux lettres inactive sont conservés et la boîte aux lettres est liée à un nouveau compte d'utilisateur. Une fois récupérée, la boîte aux lettres inactive n'existe plus. Pour obtenir des procédures pas à pas et des informations supplémentaires sur le déroulement de la récupération d’une boîte aux lettres inactive, consultez la rubrique [récupérer une boîte aux lettres inactive dans Office 365](recover-an-inactive-mailbox.md).
  
## <a name="restore-the-contents-of-an-inactive-mailbox-to-another-mailbox"></a>Restaurer le contenu d'une boîte aux lettres inactive vers une autre boîte aux lettres

Si un autre employé assume les responsabilités de l'ancien employé, ou si un autre utilisateur doit accéder au contenu de la boîte aux lettres inactive, vous pouvez restaurer (ou fusionner) le contenu de la boîte aux lettres inactive vers une boîte aux lettres existante. Lorsque vous restaurez une boîte aux lettres inactive, le contenu est copié vers une autre boîte aux lettres. La boîte aux lettres inactive est conservée et reste une boîte aux lettres inactive. La boîte aux lettres inactive peut toujours faire l'objet d'une recherche à l'aide d'eDiscovery, son contenu peut être restauré vers une autre boîte aux lettres, ou il peut être récupéré ou supprimé ultérieurement. Pour obtenir des procédures pas à pas, reportez-vous à la rubrique [restaurer une boîte aux lettres inactive dans Office 365](restore-an-inactive-mailbox.md).
  
## <a name="delete-an-inactive-mailbox"></a>Suppression d’une boîte aux lettres inactive

Si vous n’avez plus besoin de conserver le contenu d’une boîte aux lettres inactive, vous pouvez supprimer définitivement la boîte aux lettres inactive en supprimant la conservation ou en supprimant la stratégie de rétention Office 365 appliquée à la boîte aux lettres inactive. Si la boîte aux lettres a été supprimée depuis plus de 30 jours, la boîte aux lettres est marquée pour suppression définitive après la suppression de la conservation, et la boîte aux lettres devient non récupérable. Si la boîte aux lettres a été supprimée au cours des 30 derniers jours, vous pouvez toujours récupérer la boîte aux lettres après avoir supprimé la conservation ou la stratégie de rétention. Pour obtenir des procédures pas à pas pour supprimer une stratégie de rétention ou une stratégie de rétention Office 365 afin de supprimer définitivement une boîte aux lettres inactive, consultez la rubrique [supprimer une boîte aux lettres inactive dans Office 365](delete-an-inactive-mailbox.md).