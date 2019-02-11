---
title: Créer et gérer des boîtes aux lettres inactives dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 296a02bd-ebde-4022-900e-547acf38ddd7
description: Vous pouvez créer une boîte aux lettres inactive dans Office 365 par application d’une suspension ou une stratégie de rétention d’Office 365 à la boîte aux lettres et ensuite supprimer le compte d’utilisateur Office 365 correspondant. Éléments d’une boîte aux lettres inactive sont conservés pendant la durée de la stratégie de blocage ou de rétention qui a été appliquée avant qu’il a été inactif. Pour supprimer définitivement une boîte aux lettres inactive, simplement supprimer la stratégie de blocage ou de rétention.
ms.openlocfilehash: de67068ded30f63e46a8a94c1030d45a12b56a2e
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29740836"
---
# <a name="create-and-manage-inactive-mailboxes-in-office-365"></a>Créer et gérer des boîtes aux lettres inactives dans Office 365

Office 365 permet de conserver le contenu des boîtes aux lettres supprimées. Cette fonctionnalité est appelée [boîtes aux lettres inactives](inactive-mailboxes-in-office-365.md). Boîtes aux lettres inactives permettent de conserver e-mail de vos employés ancien avoir quitté votre organisation. Une boîte aux lettres devienne inactive lorsqu’un litige ou une stratégie de rétention Office 365 (créé de sécurité Office 365 &amp; centre de conformité) est appliqué à la boîte aux lettres avant la suppression du compte d’utilisateur Office 365 correspondant. Le contenu d’une boîte aux lettres inactive est conservé pendant la durée de la suspension a été placée dans la boîte aux lettres avant qu’il a été inactif. Cela permet aux administrateurs, responsables de la conformité et des enregistrements responsables à utiliser la recherche de contenu dans la sécurité &amp; centre de conformité pour rechercher et exporter le contenu d’une boîte aux lettres inactive. Boîtes aux lettres inactives ne peut pas recevoir du courrier électronique et ne sont pas affichés dans le carnet d’adresses partagé de votre organisation ou d’autres listes.
  
> [!NOTE]
> Nous avons reporté l'échéance du 1er juillet 2017 afin de créer des conservations inaltérables pour rendre une boîte aux lettres inactive. Cependant, plus tard cette année ou au début de l'année prochaine, vous ne pourrez plus créer de conservations inaltérables dans Exchange Online. Actuellement, seules les conservations pour litige et les stratégies de rétention Office 365 peuvent être utilisées pour créer une boîte aux lettres inactive. Toutefois, les boîtes aux lettres inactives existantes qui se trouvent en conservation inaltérable seront toujours prises en charge. Vous pouvez continuer à gérer les conservations inaltérables sur les boîtes aux lettres inactives. Cela inclut la modification de la durée d'une conservation inaltérable et la suppression définitive d'une boîte aux lettres inactive en supprimant la conservation inaltérable. 
  
## <a name="before-you-begin"></a>Avant de commencer

- Pour désactiver une boîte aux lettres, il doit être attribué une licence Exchange Online Plan 2 afin qu’un litige ou une stratégie de rétention Office 365 peut être appliquée à la boîte aux lettres avant d’être supprimé. Licences Exchange Online Plan 2 font partie d’un abonnement Office 365 entreprise E3 et E5. Si une boîte aux lettres est attribué une licence Exchange Online Plan 1 (qui fait partie d’un abonnement à Office 365 entreprise E1), vous devez attribuer une licence séparée de l’archivage Exchange Online afin qu’une suspension peut être appliquée à la boîte aux lettres avant d’être supprimé. Pour plus d’informations, voir [L’archivage Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=286153).
    
- La licence associée à la boîte aux lettres Exchange Online supprimée sera disponible après la suppression du compte d’utilisateur Office 365 correspondant. Vous pouvez ensuite [affecter des licences aux utilisateurs dans Office 365 pour les entreprises](https://support.office.com/article/997596b5-4173-4627-b915-36abac6786dc) à un autre utilisateur. 
    
- Si une conservation pour litige ou une stratégie de rétention Office 365 n'est pas appliquée à une boîte aux lettres avant sa suppression, son contenu n'est ni conservé ni détectable. Cependant, la boîte aux lettres peut être récupérée dans les 30 jours suivant sa suppression, mais, à défaut de récupération, elle est définitivement supprimée avec son contenu à l'issue de cette période.
    
- Pour plus d’informations sur le litige, voir [In-Place Hold et litige](https://go.microsoft.com/fwlink/p/?LinkId=846124). Pour plus d’informations sur les stratégies de rétention d’Office 365 dans la sécurité &amp; centre de conformité, voir [vue d’ensemble des stratégies de rétention dans Office 365](retention-policies.md).
  
## <a name="create-an-inactive-mailbox"></a>Créer une boîte aux lettres inactive

Définition d’une boîte aux lettres inactive comprend deux étapes : 1) placer la boîte aux lettres sur litige ou de lui appliquer une stratégie de rétention d’Office 365 et de suppression de la boîte aux lettres 2) ou le compte d’utilisateur Office 365 correspondant. Une fois que la boîte aux lettres est inactive, son contenu est conservé jusqu'à ce que la stratégie de blocage ou de rétention est supprimée.
  
### <a name="step-1-place-a-mailbox-on-litigation-hold-or-apply-an-office-365-retention-policy"></a>Étape 1 : Placement d'une boîte aux lettres en conservation pour litige ou application d'une stratégie de rétention Office 365

Le placement d'une boîte aux lettres en conservation pour litige ou l'application d'une stratégie de rétention Office 365 permet de conserver le contenu de la boîte aux lettres avant sa suppression. Ces deux types de conservation conservent l'ensemble du contenu de la boîte aux lettres, notamment les éléments supprimés et les versions d'origine des éléments modifiés. Les éléments supprimés et modifiés sont conservés dans la boîte aux lettres inactive pendant une période spécifiée, jusqu'à la suppression définitive de la boîte aux lettres inactive en supprimant la conservation ou la stratégie de rétention appliquée.
  
Si une boîte aux lettres est déjà placée en conservation, ou si une stratégie de rétention Office 365 est déjà appliquée à une boîte aux lettres, il vous suffit de supprimer le compte d'utilisateur Office 365 correspondant, comme expliqué à l'étape 2.
  
Pour savoir comment placer une boîte aux lettres en conservation pour litige ou appliquer une stratégie de rétention Office 365, consultez les rubriques suivantes :
  
- [Place a mailbox on Litigation Hold](https://go.microsoft.com/fwlink/?linkid=856286)
    
- [Vue d'ensemble des stratégies de rétention](retention-policies.md)
    
> [!NOTE]
> Pour les conservations pour litige et les stratégies de rétention Office 365, vous pouvez créer une conservation indéfinie ou temporaire. En cas de conservation indéfinie, le contenu de la boîte aux lettres inactive est conservé pour une durée illimitée, ou jusqu'à la suppression de la conservation ou jusqu'à la modification de la durée de conservation. Une fois la conservation ou la stratégie de rétention supprimée (en supposant que la boîte aux lettres a été supprimée depuis plus de 30 jours), la boîte aux lettres inactive est définitivement supprimée et son contenu n'est plus conservé ni détectable. En cas de conservation ou de stratégie de rétention Office 365 temporaire, vous en spécifiez la durée. Cette durée s'applique à un élément et est calculée à partir de la date de réception ou de création de ce dernier. Après l'expiration de la conservation d'un élément de boîte aux lettres, si cet élément est déplacé vers, ou se trouve dans le dossier Éléments récupérables de la boîte aux lettres inactive, l'élément est supprimé définitivement (purgé) de la boîte aux lettres inactive après l'expiration de la période de rétention de l'élément supprimé. 
  
### <a name="step-2-delete-the-mailbox"></a>Étape 2 : Suppression de la boîte aux lettres

Une fois que la boîte aux lettres est mis en attente ou une stratégie de rétention Office 365 est appliquée, l’étape suivante consiste à supprimer la boîte aux lettres. La meilleure façon de supprimer une boîte aux lettres consiste à supprimer le compte d’utilisateur Office 365 correspondant dans le centre d’administration d’Office 365. Pour plus d’informations sur la suppression des comptes d’utilisateurs Office 365, voir [Supprimer un utilisateur à partir de votre organisation](https://support.office.com/article/d5155593-3bac-4d8d-9d8b-f4513a81479e).
  
> [!NOTE]
> Vous pouvez également supprimer la boîte aux lettres à l’aide de l’applet de commande **Remove-Mailbox** dans Exchange Online PowerShell. Pour plus d’informations, voir [Supprimer ou restaurer les boîtes aux lettres dans Exchange Online](https://go.microsoft.com/fwlink/?linkid=856287). 
  

## <a name="view-a-list-of-inactive-mailboxes"></a>Afficher la liste des boîtes aux lettres inactives


Pour afficher une liste des boîtes aux lettres inactives dans votre organisation :
  
1. Accédez à [https://protection.office.com/](https://protection.office.com/) et connectez-vous en utilisant les informations d’identification pour un compte d’administrateur de votre organisation Office 365. 
    
2. Dans le volet gauche de la sécurité &amp; centre de conformité, cliquez sur **la gouvernance des données** \> ** rétention **.
    
3. Dans la page de **rétention** , cliquez sur **plus de**![ellipses barre de Navigation](media/9723029d-e5cd-4740-b5b1-2806e4f28208.gif), puis cliquez sur **boîtes aux lettres inactives**.
    
    ![Dans la page de rétention, cliquez sur plus, puis cliquez sur boîtes aux lettres inactives pour afficher la liste des boîtes aux lettres inactives](media/761bd90c-3e37-48f9-b1b9-479e90fea267.png)
  
    La page **boîtes aux lettres inactives** s’affiche. Notez que le nombre total de boîtes aux lettres inactives dans votre organisation est affiché. 
    
    ![Une liste de toutes les boîtes aux lettres inactives dans votre organisation est affichée.](media/57d9d183-0c6c-4bd8-82e7-115f7b7b6de7.png)
  
Sinon, vous pouvez exécuter la commande suivante dans Exchange Online PowerShell pour afficher la liste des boîtes aux lettres inactives.

```
 Get-Mailbox -InactiveMailboxOnly | FT DisplayName,PrimarySMTPAddress,WhenSoftDeleted
```

Vous pouvez cliquer sur ![icône de résultats de recherche d’exportation](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **Exporter** pour afficher ou télécharger un fichier CSV qui contient des informations supplémentaires sur les boîtes aux lettres inactives dans votre organisation. 
  
Vous pouvez également exécuter la commande suivante pour exporter la liste des boîtes aux lettres inactives et autres informations dans un fichier CSV. Dans cet exemple, le fichier CSV est créé dans le répertoire actif.

```
Get-Mailbox -InactiveMailboxOnly | Select Displayname,PrimarySMTPAddress,DistinguishedName,ExchangeGuid,WhenSoftDeleted | Export-Csv InactiveMailboxes.csv -NoType
```
   
> [!NOTE]
> Il est possible qu’une boîte aux lettres inactive aient la même adresse SMTP en tant qu’une boîte aux lettres de l’utilisateur actif. Dans ce cas, la valeur de la propriété **DistinguishedName** ou **ExchangeGuid** peut servir à identifier de manière unique une boîte aux lettres inactive. 
  
## <a name="search-and-export-the-contents-of-an-inactive-mailbox"></a>Recherche et exportation du contenu d'une boîte aux lettres inactive

Vous pouvez accéder au contenu de la boîte aux lettres inactive à l’aide de l’outil de recherche de contenu dans la sécurité &amp; centre de conformité. Lorsque vous recherchez une boîte aux lettres inactive, vous pouvez créer une requête de recherche de mot clé pour rechercher des éléments spécifiques ou vous pouvez retourner tout le contenu de la boîte aux lettres inactive. Vous pouvez afficher un aperçu des résultats de la recherche ou exporter les résultats de recherche dans un fichier de données Outlook (PST) ou en tant que messages électroniques individuels. Pour obtenir des procédures détaillées pour la recherche de boîtes aux lettres et l’exportation de résultats de recherche, voir les rubriques suivantes :
  
- [Recherche de contenu dans Office 365](content-search.md)
    
- [Exporter les résultats de recherche de contenu à partir de la sécurité de 365 Office &amp; centre de conformité](export-search-results.md)
    
Voici quelques points à prendre en compte lors de la recherche de boîtes aux lettres inactives.
  
- Si une recherche de contenu inclut une boîte aux lettres utilisateur et que cette boîte aux lettres est ensuite effectuée inactive, la recherche de contenu continuera à rechercher la boîte aux lettres inactive lorsque vous exécutez de nouveau la recherche dès que celui-ci est inactif.
    
- Dans certains cas, un utilisateur peut avoir une boîte aux lettres active et une boîte aux lettres inactive qui ont la même adresse SMTP. Dans ce cas, recherche portera uniquement la boîte aux lettres spécifique que vous sélectionnez un emplacement pour une recherche de contenu. En d’autres termes, si vous ajoutez des boîtes aux lettres d’un utilisateur à une recherche, vous ne pouvez pas supposer que les deux actives et inactives boîtes aux lettres portera ; recherche portera uniquement à la boîte aux lettres que vous ajoutez explicitement à la recherche.
    
- Il est vivement recommandé de ne pas avoir une boîte aux lettres active et la boîte aux lettres inactive avec la même adresse SMTP. Si vous avez besoin de réutiliser l’adresse SMTP qui est actuellement attribué à une boîte aux lettres inactive, nous vous recommandons de récupérer la boîte aux lettres inactive ou restaurer le contenu d’une boîte aux lettres inactive dans une boîte aux lettres active (ou l’archivage d’une boîte aux lettres active) et supprimez le boîte aux lettres inactive.
    
## <a name="change-the-hold-duration-for-an-inactive-mailbox"></a>Modifier la durée de la conservation pour une boîte aux lettres inactive

Après une boîte aux lettres inactive, vous pouvez modifier la durée de la suspension ou la stratégie de rétention pour la boîte aux lettres inactive Office 365. Pour connaître les procédures, voir [Modifier la durée d’attente pour une boîte aux lettres inactive dans Office 365](change-the-hold-duration-for-an-inactive-mailbox.md).
  
## <a name="recover-an-inactive-mailbox"></a>Récupérer une boîte aux lettres inactive

Si un ancien employé renvoie à votre organisation, ou si un nouvel employé à effectuer sur les responsabilités de l’employé quittée, vous pouvez récupérer le contenu de la boîte aux lettres inactive. Lorsque vous récupérez une boîte aux lettres inactive, la boîte aux lettres est converti en une nouvelle boîte aux lettres, le contenu et la structure de dossiers de la boîte aux lettres inactive sont conservés, et la boîte aux lettres est liée à un nouveau compte d’utilisateur. Une fois qu’il est récupéré, la boîte aux lettres inactive n’existe plus. Pour connaître les procédures et plus d’informations sur qui se produit lorsque vous récupérez une boîte aux lettres inactive, consultez la rubrique [récupérer une boîte aux lettres inactive dans Office 365](recover-an-inactive-mailbox.md).
  
## <a name="restore-the-contents-of-an-inactive-mailbox-to-another-mailbox"></a>Restaurer le contenu d'une boîte aux lettres inactive vers une autre boîte aux lettres

Si un autre employé prend en charge les responsabilités d’un ancien employé, ou si une autre personne doit avoir accès au contenu de la boîte aux lettres inactive, vous pouvez restaurer (ou fusionner) le contenu de la boîte aux lettres inactive dans une boîte aux lettres existante. Lorsque vous restaurez une boîte aux lettres inactive, le contenu est copié dans une autre boîte aux lettres. La boîte aux lettres inactive est conservée et reste une boîte aux lettres inactive. La boîte aux lettres inactive peut toujours être recherché à l’aide de la découverte électronique, son contenu peut être restauré à une autre boîte aux lettres, ou peut être récupéré ou supprimé à une date ultérieure. Pour connaître les procédures, voir [restaurer une boîte aux lettres inactive dans Office 365](restore-an-inactive-mailbox.md).
  
## <a name="delete-an-inactive-mailbox"></a>Suppression d'une boîte aux lettres inactive

Si vous n’avez plus besoin de conserver le contenu d’une boîte aux lettres inactive, vous pouvez supprimer définitivement la boîte aux lettres inactive en supprimant la suspension ou de suppression de la stratégie de rétention pour la boîte aux lettres inactive Office 365. Si la boîte aux lettres a été supprimé remonte à plus de 30 jours, la boîte aux lettres est marqué pour suppression définitive une fois que vous supprimez la suspension, et devient la boîte aux lettres non récupérables. Si la boîte aux lettres a été supprimée au cours des 30 derniers jours, vous pouvez récupérer la boîte aux lettres après la suppression de la stratégie de blocage ou de rétention. Pour connaître les procédures de suppression d’une suspension ou une stratégie de rétention à supprimer définitivement une boîte aux lettres inactive Office 365, voir [suppression d’une boîte aux lettres inactive dans Office 365](delete-an-inactive-mailbox.md).