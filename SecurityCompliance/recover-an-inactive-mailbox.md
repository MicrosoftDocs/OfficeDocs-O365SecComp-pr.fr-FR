---
title: Récupérer une boîte aux lettres inactive dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/21/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 35d0ecdb-7cb0-44be-ad5c-69df2f8f8b25
description: 'Si un ancien employé renvoie à votre organisation, ou si un nouvel employé à effectuer sur les responsabilités d’un employé quittée, vous pouvez récupérer le contenu de la boîte aux lettres inactive dans Office 365. Lorsque vous récupérez une boîte aux lettres inactive, il est converti en une nouvelle boîte aux lettres qui contient le contenu de la boîte aux lettres inactive. '
ms.openlocfilehash: dcc84e44454a75f8b4dac953599632d632f340b9
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528660"
---
# <a name="recover-an-inactive-mailbox-in-office-365"></a>Récupérer une boîte aux lettres inactive dans Office 365

Une boîte aux lettres inactive (qui est un type de boîte aux lettres supprimée) est utilisée pour conserver le courrier électronique d’un ancien employé une fois qu’il quitte l’organisation. Si cet employé renvoie à votre organisation ou un autre employé prend en charge les responsabilités de l’ancien employé, il existe deux méthodes que vous pouvez apporter le contenu de la boîte aux lettres inactive disponibles à un utilisateur : 
  
- **Récupérer une boîte aux lettres inactive** Si l’ancien employé renvoie à votre organisation, ou si un nouvel employé à effectuer sur les responsabilités de l’ancien employé, vous pouvez récupérer le contenu de la boîte aux lettres inactive. Cette méthode convertit la boîte aux lettres inactive dans une nouvelle boîte aux lettres active qui contient le contenu de la boîte aux lettres inactive. Une fois qu’il est récupéré, la boîte aux lettres inactive n’existe plus. Les procédures décrites dans cette rubrique décrivent cette méthode. 
    
- **Restaurer une boîte aux lettres inactive** Si un autre employé prend en charge les responsabilités de l’ancien employé, ou si un autre utilisateur a besoin d’accéder au contenu de la boîte aux lettres inactive, vous pouvez restaurer (ou fusionner) le contenu de la boîte aux lettres inactive dans une boîte aux lettres existante. Vous pouvez également restaurer l’archive à partir d’une boîte aux lettres inactive. Pour les procédures de cette méthode, voir [restaurer une boîte aux lettres inactive dans Office 365](restore-an-inactive-mailbox.md).
    
Consultez la section [Plus d'informations](recover-an-inactive-mailbox.md#moreinfo) pour obtenir d'autres détails concernant les différences entre la restauration et la récupération d'une boîte aux lettres inactive et une description de la récupération d'une boîte aux lettres inactive.
  
> [!NOTE]
> Nous avons différée le délai de création des archives permanentes pour désactiver une boîte aux lettres. Mais à un moment donné à l’avenir, vous ne pourrez créer des archives permanentes dans Exchange Online. À ce moment, stratégies de rétention pour litige contient et Office 365 peuvent servir à créer une boîte aux lettres inactive. Cependant, les boîtes aux lettres inactives existants qui se trouvent sur In-Place Hold seront toujours être prise en charge et vous pouvez continuer à gérer les boîtes aux lettres inactives conserve In-Place. Cela inclut la modification de la durée d’an In-Place Hold et supprimer définitivement une boîte aux lettres inactive en supprimant la In-Place Hold. 
  
## <a name="before-you-begin"></a>Avant de commencer

- Vous devez utiliser Exchange Online PowerShell pour restaurer une boîte aux lettres inactive. Vous ne pouvez pas utiliser le centre d’administration Exchange (CAE). Pour obtenir des instructions détaillées, voir [se connecter à Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=396554).
    
- Exécutez la commande suivante pour obtenir les informations d'identité pour les boîtes aux lettres inactives de votre organisation. 

    ```
    Get-Mailbox -InactiveMailboxOnly | FL Name,DistinguishedName,ExchangeGuid,PrimarySmtpAddress
    ```

    Utilisez les informations renvoyées par cette commande pour récupérer une boîte aux lettres inactive spécifique.
    
- Pour plus d’informations sur les boîtes aux lettres inactives, voir [boîtes aux lettres inactives dans Office 365](inactive-mailboxes-in-office-365.md).
    
## <a name="recover-an-inactive-mailbox"></a>Récupérer une boîte aux lettres inactive

Utilisez l’applet de commande **New-Mailbox** avec le paramètre *InactiveMailbox* pour récupérer une boîte aux lettres inactive. 
  
1. Créez une variable contenant les propriétés de la boîte aux lettres inactive. 
    
    ```
    $InactiveMailbox = Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox>
    ```
   
    > [!IMPORTANT]
    > Dans la commande précédente, utilisez la valeur de la propriété **DistinguishedName** ou **ExchangeGUID** pour identifier la boîte aux lettres inactive. Ces propriétés sont uniques pour chaque boîte aux lettres de votre organisation, alors qu'une boîte aux lettres active et une boîte aux lettres inactive peuvent avoir la même adresse SMTP principale. 
  
2. Cet exemple utilise les propriétés obtenues dans la commande précédente et récupère la boîte aux lettres inactive dans une boîte aux lettres active pour l’utilisateur de Ann Beebe. N’oubliez pas que les valeurs spécifiées pour les paramètres *nom* et *MicrosoftOnlineServicesID* sont uniques au sein de votre organisation. 

    ```
    New-Mailbox -InactiveMailbox $InactiveMailbox.DistinguishedName -Name annbeebe -FirstName Ann -LastName Beebe -DisplayName "Ann Beebe" -MicrosoftOnlineServicesID Ann.Beebe@contoso.com -Password (ConvertTo-SecureString -String 'P@ssw0rd' -AsPlainText -Force) -ResetPasswordOnNextLogon $true
    ```

    L’adresse SMTP principale pour la boîte aux lettres inactive récupérée aura la même valeur que celle spécifiée par le paramètre *MicrosoftOnlineServicesID* . 
    
Après la récupération d'une boîte aux lettres inactive, un compte d'utilisateur Office 365 est également créé. Vous devez activer ce compte d'utilisateur en lui attribuant une licence. Pour savoir comment attribuer une licence dans le centre d'administration Office 365, consultez la rubrique [Attribuer ou retirer des licences pour Office 365 pour les entreprises](https://go.microsoft.com/fwlink/p/?LinkId=276798).
  
## <a name="more-information"></a>Plus d'informations

- **Quelle est la principale différence entre la récupération et la restauration d'une boîte aux lettres inactive ?** Lorsque vous récupérez une boîte aux lettres inactive, la boîte aux lettres est généralement convertie en une nouvelle boîte aux lettres, le contenu et la structure de dossiers de la boîte aux lettres inactive sont conservés et la boîte aux lettres est liée à un nouveau compte d'utilisateur. Une fois récupérée, la boîte aux lettres inactive n'existe plus et les modifications apportées au contenu dans la nouvelle boîte aux lettres affectent le contenu placé en attente dans la boîte aux lettres inactive. À l'inverse, lorsque vous restaurez une boîte aux lettres inactive, le contenu est simplement copié vers une autre boîte aux lettres. La boîte aux lettres inactive est conservée et reste une boîte aux lettres inactive. Toute modification apportée au contenu de la boîte aux lettres cible n'affecte pas le contenu d'origine conservé dans la boîte aux lettres inactive. La boîte aux lettres inactive peut toujours faire l'objet d'une recherche à l'aide de la découverte électronique inaltérable, son contenu peut être restauré vers une autre boîte aux lettres ou il peut être récupéré ou supprimé ultérieurement. 
    
- **Que se passe-t-il lorsque vous récupérez une boîte aux lettres inactive ?** La récupération d'une boîte aux lettres inactive entraîne les événements suivants : 
    
  - La conservation pour litige (si elle a été activée pour la boîte aux lettres inactive) est désactivée.
    
  - Les conservations inaltérables sont désactivées. Cela signifie que la boîte aux lettres inactive est supprimée comme boîte aux lettres source de toutes les recherches de conservation inaltérable ou de la découverte électronique inaltérable. 
    
  - La boîte aux lettres inactive est supprimé à partir des stratégies de rétention Office 365 dont appliqué.
    
  - La période de récupération d'élément unique (définie par la propriété de boîte aux lettres **RetainDeletedItemsFor** ) est paramétrée sur 30 jours. En général, lorsqu'une boîte aux lettres est créée dans Exchange Online, cette période de rétention est définie sur 14 jours. En définissant ce paramètre sur la valeur maximale de 30 jours, vous gagnez du temps pour récupérer toutes les données définitivement supprimées (ou purgées) de la boîte aux lettres inactive. Vous pouvez également désactiver la récupération d'élément unique ou redéfinir la période de récupération d'élément unique sur la valeur par défaut de 14 jours. Pour plus d'informations, consultez la rubrique [Enable or disable single item recovery for a mailbox](https://go.microsoft.com/fwlink/?linkid=856769).
    
  - Blocage de rétention est activée, et la durée de blocage de rétention est définie sur 30 jours. Cela signifie que la stratégie de rétention par défaut Exchange et tout Office 365-l’échelle de l’organisation ou Exchange, les stratégies de rétention sont affectés à la nouvelle boîte aux lettres ne sera pas traités pendant 30 jours. Cela donne l’employé retour ou le nouveau propriétaire de l’heure de la boîte aux lettres inactive récupérée pour gérer les anciens messages. Dans le cas contraire, la stratégie de rétention Exchange ou Office 365 peut supprimer les anciens éléments de boîte aux lettres (ou déplacer les éléments vers la boîte aux lettres d’archive, s’il est activé) qui ont expiré selon les paramètres configurés pour les stratégies de rétention Exchange ou Office 365. Après 30 jours, le blocage de rétention arrive à expiration, la propriété de la boîte aux lettres **RetentionHoldEnabled** est définie sur **False**, et démarre l’Assistant dossier géré traitement les stratégies affectées à la boîte aux lettres. Si vous n’avez pas besoin cette fois supplémentaire, vous pouvez seulement supprimer le blocage de rétention. Sinon, vous pouvez augmenter la durée de la période de rétention à l’aide de la commande **Set-Mailbox-EndDateForRetentionHold** . Pour plus d’informations, voir [archive une boîte aux lettres sur la rétention](https://go.microsoft.com/fwlink/?linkid=856300).
    
- **Placer une suspension sur la boîte aux lettres récupérée si vous devez conserver l’état d’origine de la boîte aux lettres inactive.** Pour empêcher le nouveau propriétaire de boîte aux lettres ou de la stratégie de rétention de suppression définitive de tous les messages à partir de la boîte aux lettres inactive récupérée, vous pouvez placer la boîte aux lettres pour litige maintenez pour plus d’informations, consultez la rubrique [Place une boîte aux lettres en conservation pour litige](https://go.microsoft.com/fwlink/?linkid=856286).
    
- **ID utilisateur pouvez-vous utiliser lorsque vous récupérez une boîte aux lettres inactive ?** Lorsque vous récupérez une boîte aux lettres inactive, la valeur que vous spécifiez pour le paramètre *MicrosoftOnlineServicesID* peut être différente de celle d’origine qui était associé à la boîte aux lettres inactive. Vous pouvez également utiliser l’ID d’utilisateur d’origine. Mais, comme indiqué précédemment, assurez-vous que les valeurs utilisées pour le *nom* et *MicrosoftOnlineServicesID* sont uniques au sein de votre organisation lors de la récupération de la boîte aux lettres inactive. 
    
- **Que faire si la période de rétention de la boîte aux lettres inactive n'a pas expiré ?** Si une boîte aux lettres inactive a été supprimée (récupérable) il y a moins de 30 jours, vous ne pouvez pas utiliser la commande **New-Mailbox -InactiveMailbox** pour la récupérer. Vous devez la récupérer en restaurant le compte d'utilisateur Office 365 correspondant. Pour plus d'informations, consultez la rubrique [Supprimer ou restaurer des utilisateurs](https://go.microsoft.com/fwlink/p/?LinkId=279162).
    
- **Comment savoir si la période de rétention de boîte aux lettres supprimée (récupérable) pour une boîte aux lettres inactive a expiré ?** Exécutez la commande suivante. 
    
    ```
    Get-Mailbox -InactiveMailboxOnly <identity of inactive mailbox> | FL ExternalDirectoryObjectId
  ```

    Si la propriété **ExternalDirectoryObjectId** n'a pas de valeur, la période de rétention de boîte aux lettres a expiré et vous pouvez récupérer la boîte aux lettres inactive en exécutant la commande **New-Mailbox -InactiveMailbox**. Si la propriété **ExternalDirectoryObjectId** affiche une valeur, la période de rétention de boîte aux lettres supprimée (récupérable) n'a pas expiré et vous devez récupérer la boîte aux lettres en restaurant le compte d'utilisateur Office 365. Consultez la rubrique [Supprimer ou restaurer des utilisateurs](https://go.microsoft.com/fwlink/p/?LinkId=279162)
    
- **Envisagez l’activation de la boîte aux lettres d’archivage après avoir récupéré une boîte aux lettres inactive.** Cela permet le renvoi d’utilisateur ou un nouvel employé déplacer les anciens messages vers la boîte aux lettres d’archive. Et lorsque le blocage de rétention arrive à expiration, la stratégie d’archivage qui fait partie de la stratégie de rétention par défaut Exchange affectée à Exchange Online, les boîtes aux lettres seront déplace les éléments qui sont les deux ans ou antérieure à la boîte aux lettres d’archive. Si vous n’activez pas la boîte aux lettres d’archivage, les éléments antérieurs à deux ans restent dans la boîte aux lettres principale de l’utilisateur. Pour plus d’informations, voir [Activer les boîtes aux lettres archive de sécurité Office 365 &amp; centre de conformité](enable-archive-mailboxes.md).
 