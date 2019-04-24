---
title: Récupérer une boîte aux lettres inactive dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/21/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 35d0ecdb-7cb0-44be-ad5c-69df2f8f8b25
description: "Si un ancien employé revient à votre organisation, ou si un nouvel employé est embauché pour prendre en charge les responsabilités d'un employé à l'origine de la demande, vous pouvez récupérer le contenu de la boîte aux lettres inactive dans Office 365. Lorsque vous récupérez une boîte aux lettres inactive, elle est convertie en une nouvelle boîte aux lettres qui contient le contenu de la boîte aux lettres inactive. "
ms.openlocfilehash: c7f942c518dcc74a4bdb37d67e27e8a63879ab46
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32261542"
---
# <a name="recover-an-inactive-mailbox-in-office-365"></a>Récupérer une boîte aux lettres inactive dans Office 365

Une boîte aux lettres inactive (c'est-à-dire un type de boîte aux lettres supprimée (récupérable)) sert à conserver les courriers électroniques d'un ancien employé après qu'il a quitté votre organisation. Si cet employé revient à votre organisation ou si un autre employé assume les responsabilités de l'ancien employé, il existe deux façons de mettre le contenu de la boîte aux lettres inactive à la disposition de l'utilisateur: 
  
- **Récupérer une boîte aux lettres inactive** Si l'ancien employé revient à votre organisation ou si un nouvel employé est embauché pour prendre les responsabilités de l'ancien employé, vous pouvez récupérer le contenu de la boîte aux lettres inactive. Cette méthode convertit la boîte aux lettres inactive en une nouvelle boîte aux lettres active qui contient le contenu de la boîte aux lettres inactive. Une fois récupérée, la boîte aux lettres inactive n'existe plus. Les procédures présentées dans cette rubrique décrivent cette méthode. 
    
- **Restaurer une boîte aux lettres inactive** Si un autre employé assume les responsabilités de l'ancien employé ou si un autre utilisateur a besoin d'accéder au contenu de la boîte aux lettres inactive, vous pouvez restaurer (ou fusionner) le contenu de la boîte aux lettres inactive vers une boîte aux lettres existante. Vous pouvez également restaurer l'archive d'une boîte aux lettres inactive. Pour connaître les procédures de cette méthode, consultez la rubrique [restaurer une boîte aux lettres inactive dans Office 365](restore-an-inactive-mailbox.md).
    
Consultez la section [Plus d'informations](#more-information) pour obtenir d'autres détails concernant les différences entre la restauration et la récupération d'une boîte aux lettres inactive et une description de la récupération d'une boîte aux lettres inactive.
  
> [!NOTE]
> Nous avons repoussé l'échéance de création de nouvelles conservations inactives pour désactiver une boîte aux lettres. Toutefois, à l'avenir, vous ne pourrez pas créer de nouvelles conservations inaltérables dans Exchange Online. À ce stade, seuls les stratégies de conservation pour litige et Office 365 peuvent être utilisées pour créer une boîte aux lettres inactive. Toutefois, les boîtes aux lettres inactives existantes qui sont en conservation inaltérable sont toujours prises en charge, et vous pouvez continuer à gérer les conservations inactives sur les boîtes aux lettres inactives. Cela inclut le changement de la durée d'une conservation inaltérable et la suppression définitive d'une boîte aux lettres inactive en supprimant la conservation inaltérable. 
  
## <a name="before-you-begin"></a>Avant de commencer

- Vous devez utiliser Exchange Online PowerShell pour restaurer une boîte aux lettres inactive. Vous ne pouvez pas utiliser le Centre d'administration Exchange (CAE). Pour obtenir des instructions détaillées, consultez la rubrique [connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=396554).
    
- Exécutez la commande suivante pour obtenir les informations d'identité pour les boîtes aux lettres inactives de votre organisation. 

    ```
    Get-Mailbox -InactiveMailboxOnly | FL Name,DistinguishedName,ExchangeGuid,PrimarySmtpAddress
    ```

    Utilisez les informations renvoyées par cette commande pour récupérer une boîte aux lettres inactive spécifique.
    
- Pour plus d'informations sur les boîtes aux lettres inactives, consultez la rubrique [inactive mailboxes in Office 365](inactive-mailboxes-in-office-365.md).
    
## <a name="recover-an-inactive-mailbox"></a>Récupérer une boîte aux lettres inactive

Utilisez la cmdlet **New-Mailbox** avec le paramètre *InactiveMailbox* pour récupérer une boîte aux lettres inactive. 
  
1. Créez une variable contenant les propriétés de la boîte aux lettres inactive. 
    
    ```
    $InactiveMailbox = Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox>
    ```
   
    > [!IMPORTANT]
    > Dans la commande précédente, utilisez la valeur de la propriété **DistinguishedName** ou **ExchangeGUID** pour identifier la boîte aux lettres inactive. Ces propriétés sont uniques pour chaque boîte aux lettres de votre organisation, alors qu'une boîte aux lettres active et une boîte aux lettres inactive peuvent avoir la même adresse SMTP principale. 
  
2. Cet exemple utilise les propriétés obtenues grâce à la commande précédente et récupère la boîte aux lettres inactive dans une boîte aux lettres active pour l'utilisateur Ann Beebe. Assurez-vous que les valeurs spécifiées pour les paramètres *Name* et *MicrosoftOnlineServicesID* sont uniques au sein de votre organisation. 

    ```
    New-Mailbox -InactiveMailbox $InactiveMailbox.DistinguishedName -Name annbeebe -FirstName Ann -LastName Beebe -DisplayName "Ann Beebe" -MicrosoftOnlineServicesID Ann.Beebe@contoso.com -Password (ConvertTo-SecureString -String 'P@ssw0rd' -AsPlainText -Force) -ResetPasswordOnNextLogon $true
    ```

    L'adresse SMTP principale de la boîte aux lettres inactive Récupérée aura la même valeur que celle spécifiée par le paramètre *MicrosoftOnlineServicesID* . 
    
Après la récupération d'une boîte aux lettres inactive, un compte d'utilisateur Office 365 est également créé. Vous devez activer ce compte d'utilisateur en lui attribuant une licence. Pour savoir comment attribuer une licence dans le Centre d'administration Microsoft 365, voir [Attribuer ou retirer des licences pour Office 365 pour les entreprises](https://go.microsoft.com/fwlink/p/?LinkId=276798).
  
## <a name="more-information"></a>Plus d’informations

- **Quelle est la principale différence entre la récupération et la restauration d'une boîte aux lettres inactive ?** Lorsque vous récupérez une boîte aux lettres inactive, la boîte aux lettres est généralement convertie en une nouvelle boîte aux lettres, le contenu et la structure de dossiers de la boîte aux lettres inactive sont conservés et la boîte aux lettres est liée à un nouveau compte d'utilisateur. Une fois récupérée, la boîte aux lettres inactive n'existe plus et les modifications apportées au contenu dans la nouvelle boîte aux lettres affectent le contenu placé en attente dans la boîte aux lettres inactive. À l'inverse, lorsque vous restaurez une boîte aux lettres inactive, le contenu est simplement copié vers une autre boîte aux lettres. La boîte aux lettres inactive est conservée et reste une boîte aux lettres inactive. Toute modification apportée au contenu de la boîte aux lettres cible n'affecte pas le contenu d'origine conservé dans la boîte aux lettres inactive. La boîte aux lettres inactive peut toujours faire l'objet d'une recherche à l'aide de la découverte électronique inaltérable, son contenu peut être restauré vers une autre boîte aux lettres ou il peut être récupéré ou supprimé ultérieurement. 
    
- **Que se passe-t-il lorsque vous récupérez une boîte aux lettres inactive ?** La récupération d'une boîte aux lettres inactive entraîne les événements suivants : 
    
  - La conservation pour litige (si elle a été activée pour la boîte aux lettres inactive) est désactivée.
    
  - Les conservations inaltérables sont désactivées. Cela signifie que la boîte aux lettres inactive est supprimée comme boîte aux lettres source de toutes les recherches de conservation inaltérable ou de la découverte électronique inaltérable. 
    
  - La boîte aux lettres inactive est supprimée des stratégies de rétention Office 365 auxquelles elle est appliquée.
    
  - La période de récupération d'élément unique (définie par la propriété de boîte aux lettres **RetainDeletedItemsFor** ) est paramétrée sur 30 jours. En général, lorsqu'une boîte aux lettres est créée dans Exchange Online, cette période de rétention est définie sur 14 jours. En définissant ce paramètre sur la valeur maximale de 30 jours, vous gagnez du temps pour récupérer toutes les données définitivement supprimées (ou purgées) de la boîte aux lettres inactive. Vous pouvez également désactiver la récupération d'élément unique ou redéfinir la période de récupération d'élément unique sur la valeur par défaut de 14 jours. Pour plus d'informations, consultez la rubrique [Enable or disable single item recovery for a mailbox](https://go.microsoft.com/fwlink/?linkid=856769).
    
  - Le blocage de rétention est activé et la durée du blocage de rétention est définie sur 30 jours. Cela signifie que la stratégie de rétention Exchange par défaut, ainsi que toutes les stratégies de rétention Office 365 à l'échelle de l'organisation ou à l'échelle de l'organisation qui sont affectées à la nouvelle boîte aux lettres ne seront pas traitées pendant 30 jours. L'employé de retour ou le nouveau propriétaire de la boîte aux lettres inactive récupérée a ainsi le temps de gérer les anciens messages. Dans le cas contraire, la stratégie de rétention Exchange ou Office 365 peut supprimer les anciens éléments de boîte aux lettres (ou déplacer les éléments vers la boîte aux lettres d'archivage si elle est activée) qui ont expiré en fonction des paramètres configurés pour les stratégies de rétention Exchange ou Office 365. Après 30 jours, le blocage de rétention expire, la propriété de boîte aux lettres **RetentionHoldEnabled** est définie sur **false**et l'Assistant dossier géré commence à traiter les stratégies attribuées à la boîte aux lettres. Si vous n'avez pas besoin de ce temps supplémentaire, il vous suffit de supprimer le blocage de rétention. Vous pouvez également augmenter la durée du blocage de rétention à l'aide de la commande **Set-Mailbox -EndDateForRetentionHold**. Pour plus d'informations, consultez la rubrique [Place a mailbox on retention hold](https://go.microsoft.com/fwlink/?linkid=856300).
    
- **Placez une conservation sur la boîte aux lettres récupérée si vous devez conserver l'état d'origine de la boîte aux lettres inactive.** Pour empêcher le nouveau propriétaire de la boîte aux lettres ou la stratégie de rétention de supprimer définitivement les messages de la boîte aux lettres inactive Récupérée, vous pouvez placer la boîte aux lettres en conservation pour litige pour plus d'informations, consultez la rubrique [placer une boîte aux lettres en conservation pour litige](https://go.microsoft.com/fwlink/?linkid=856286).
    
- **Quel identifiant utilisateur pouvez-vous utiliser pour récupérer une boîte aux lettres inactive ?** Lorsque vous récupérez une boîte aux lettres inactive, la valeur que vous spécifiez pour le paramètre *MicrosoftOnlineServicesID* peut être différente de l'image d'origine associée à la boîte aux lettres inactive. Vous pouvez également utiliser l'identifiant utilisateur d'origine. Toutefois, comme indiqué précédemment, assurez-vous que les valeurs utilisées pour *Name* et *MicrosoftOnlineServicesID* sont uniques au sein de votre organisation lorsque vous récupérez la boîte aux lettres inactive. 
    
- **Que faire si la période de rétention de la boîte aux lettres inactive n'a pas expiré ?** Si une boîte aux lettres inactive a été supprimée (récupérable) il y a moins de 30 jours, vous ne pouvez pas utiliser la commande **New-Mailbox -InactiveMailbox** pour la récupérer. Vous devez la récupérer en restaurant le compte d'utilisateur Office 365 correspondant. Pour plus d'informations, consultez la rubrique [Supprimer ou restaurer des utilisateurs](https://go.microsoft.com/fwlink/p/?LinkId=279162).
    
- **Comment savoir si la période de rétention de boîte aux lettres supprimée (récupérable) pour une boîte aux lettres inactive a expiré ?** Exécutez la commande suivante. 
    
    ```
    Get-Mailbox -InactiveMailboxOnly <identity of inactive mailbox> | FL ExternalDirectoryObjectId
  ```

    Si la propriété **ExternalDirectoryObjectId** n'a pas de valeur, la période de rétention de boîte aux lettres a expiré et vous pouvez récupérer la boîte aux lettres inactive en exécutant la commande **New-Mailbox -InactiveMailbox**. Si la propriété **ExternalDirectoryObjectId** affiche une valeur, la période de rétention de boîte aux lettres supprimée (récupérable) n'a pas expiré et vous devez récupérer la boîte aux lettres en restaurant le compte d'utilisateur Office 365. Consultez la rubrique [Supprimer ou restaurer des utilisateurs](https://go.microsoft.com/fwlink/p/?LinkId=279162)
    
- **Pensez à activer la boîte aux lettres d'archivage après avoir récupéré une boîte aux lettres inactive.** Ainsi, l'utilisateur qui revient ou le nouvel employé peut déplacer les anciens messages vers la boîte aux lettres d'archivage. Lorsque le blocage de rétention expire, la stratégie d'archivage qui fait partie de la stratégie de rétention Exchange par défaut affectée aux boîtes aux lettres Exchange Online déplace les éléments datant de deux ans ou plus dans la boîte aux lettres d'archivage. Si vous n'activez pas la boîte aux lettres d'archivage, les éléments antérieurs à deux ans restent dans la boîte aux lettres principale de l'utilisateur. Pour plus d'informations, consultez [la rubrique activation des boîtes aux lettres d' &amp; archivage dans le centre de sécurité conformité Office 365](enable-archive-mailboxes.md).
 