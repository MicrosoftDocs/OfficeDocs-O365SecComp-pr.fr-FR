---
title: Restaurer une boîte aux lettres inactive dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 8/28/2017
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 97e06a7a-ef9a-4ce8-baea-18b9e20449a3
description: Si un nouvel employé ou un autre utilisateur a besoin d’accéder au contenu d’une boîte aux lettres inactive dans Office 365, vous pouvez restaurer (ou fusionner) le contenu de la boîte aux lettres inactive dans une boîte aux lettres existante.
ms.openlocfilehash: 6bd147296e4324c5f75ff808768f8899cf9b59fd
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34157306"
---
# <a name="restore-an-inactive-mailbox-in-office-365"></a>Restaurer une boîte aux lettres inactive dans Office 365

Une boîte aux lettres inactive (qui est un type de boîte aux lettres supprimée (récupérable)) est utilisée pour conserver le courrier électronique d’un ancien employé une fois qu’il quitte votre organisation. Si un autre employé assume les responsabilités de l'employé qui est parti ou si ce dernier réintègre votre organisation, deux méthodes vous permettent de mettre à disposition le contenu de la boîte aux lettres inactive : 
  
- **Restaurer une boîte aux lettres inactive** Si un autre employé assume les responsabilités de l'employé qui est parti, ou si un autre utilisateur doit accéder au contenu de la boîte aux lettres inactive, vous pouvez restaurer (ou fusionner) le contenu de la boîte aux lettres inactive vers une boîte aux lettres existante. Vous pouvez également restaurer l'archive d'une boîte aux lettres inactive. Une fois restaurée, la boîte aux lettres inactive est conservée sous la forme d'une boîte aux lettres inactive. Cette rubrique décrit les procédures de restauration d'une boîte aux lettres inactive. 
    
- **Récupérer une boîte aux lettres inactive** Si l'employé qui est parti réintègre votre organisation, ou si un nouvel employé est embauché pour assumer les responsabilités de l'employé parti, vous pouvez récupérer le contenu de la boîte aux lettres inactive. Cette méthode convertit la boîte aux lettres inactive en une nouvelle boîte aux lettres qui renferme le contenu de la boîte aux lettres inactive. Une fois récupérée, la boîte aux lettres inactive n'existe plus. Pour connaître les procédures pas à pas, reportez-vous à la rubrique [récupérer une boîte aux lettres inactive dans Office 365](recover-an-inactive-mailbox.md).
    
Pour plus d’informations sur les différences entre la restauration et la récupération d’une boîte aux lettres inactive, reportez-vous à la section **plus d’informations** de cet article. 
  
## <a name="before-you-begin"></a>Avant de commencer

- Vous devez utiliser Exchange Online PowerShell pour restaurer une boîte aux lettres inactive. Vous ne pouvez pas utiliser le Centre d'administration Exchange (CAE). Pour obtenir des instructions détaillées, consultez la rubrique [connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=396554).
    
- Exécutez la commande suivante dans Exchange Online PowerShell pour obtenir des informations d’identité pour les boîtes aux lettres inactives dans votre organisation. 
    
    ```
    Get-Mailbox -InactiveMailboxOnly | FL Name,DistinguishedName,ExchangeGuid,PrimarySmtpAddress
    ```

     Utilisez les informations renvoyées par cette commande pour restaurer une boîte aux lettres inactive spécifique.
    
- Pour plus d’informations sur les boîtes aux lettres inactives, consultez la rubrique [inactive mailboxes in Office 365](inactive-mailboxes-in-office-365.md).
    
## <a name="restore-an-inactive-mailbox"></a>Restaurer une boîte aux lettres inactive

Utilisez la cmdlet **New-MailboxRestoreRequest** avec les paramètres  _SourceMailbox_ et  _TargetMailbox_ pour restaurer le contenu d'une boîte aux lettres inactive vers une boîte aux lettres existante. Pour plus d'informations sur l'utilisation de cette cmdlet, consultez la rubrique [New-MailboxRestoreRequest](https://go.microsoft.com/fwlink/?linkid=856298).
  
1. Créez une variable contenant les propriétés de la boîte aux lettres inactive. 
    
    ```
    $InactiveMailbox = Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox>
    ```

    > [!IMPORTANT]
    > Dans la commande précédente, utilisez la valeur de la propriété **DistinguishedName** ou **ExchangeGUID** pour identifier la boîte aux lettres inactive. Ces propriétés sont uniques pour chaque boîte aux lettres de votre organisation, alors qu'une boîte aux lettres active et une boîte aux lettres inactive peuvent avoir la même adresse SMTP principale. 
  
2. Restaurez le contenu de la boîte aux lettres inactive vers une boîte aux lettres existante. Le contenu de la boîte aux lettres inactive (boîte aux lettres source) sera fusionné dans les dossiers correspondants de la boîte aux lettres existante (boîte aux lettres cible).
    
    ```
    New-MailboxRestoreRequest -SourceMailbox $InactiveMailbox.DistinguishedName -TargetMailbox newemployee@contoso.com -AllowLegacyDNMismatch
    ```
   
   Vous pouvez également indiquer un dossier de premier niveau dans la boîte aux lettres cible, dans lequel restaurer le contenu de la boîte aux lettres inactive. Si le dossier cible spécifié ou la structure de dossiers cible n'existe pas encore dans la boîte aux lettres cible, il/elle est créé(e) pendant le processus de restauration. 
    
    Cet exemple copie les éléments et sous-dossiers depuis une boîte aux lettres inactive vers un dossier intitulé « Boîte aux lettres inactive » dans la structure de dossiers de premier niveau de la boîte aux lettres cible.
    
   ```
   New-MailboxRestoreRequest -SourceMailbox $InactiveMailbox.DistinguishedName -TargetMailbox newemployee@contoso.com -TargetRootFolder "Inactive Mailbox" -AllowLegacyDNMismatch
   ```
  
## <a name="restore-the-archive-from-an-inactive-mailbox"></a>Restaurer l'archive d'une boîte aux lettres inactive

Si une boîte aux lettres inactive possède une boîte aux lettres d'archivage, vous pouvez également la restaurer vers la boîte aux lettres d'archivage d'une boîte aux lettres existante. Pour restaurer l'archive d'une boîte aux lettres inactive, vous devez ajouter les commutateurs  _SourceIsArchive_ et  _TargetIsAchive_ à la commande utilisée pour restaurer une boîte aux lettres inactive. 
  
1. Créez une variable contenant les propriétés de la boîte aux lettres inactive. 
    
    ```
    $InactiveMailbox = Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox>
    ```

    > [!IMPORTANT]
    > Dans la commande précédente, utilisez la valeur de la propriété **DistinguishedName** ou **ExchangeGUID** pour identifier la boîte aux lettres inactive. Ces propriétés sont uniques pour chaque boîte aux lettres de votre organisation, alors qu'une boîte aux lettres active et une boîte aux lettres inactive peuvent avoir la même adresse SMTP principale. 
  
2. Restaurez le contenu de l'archive de la boîte aux lettres inactive (archive source) vers l'archive d'une boîte aux lettres existante (archive cible). Dans cet exemple, le contenu de l'archive source est copié dans un dossier intitulé « Archive de boîte aux lettres inactive » dans l'archive de la boîte aux lettres cible.

    ```
    New-MailboxRestoreRequest -SourceMailbox $InactiveMailbox.DistinguishedName -SourceIsArchive -TargetMailbox newemployee@contoso.com -TargetIsArchive -TargetRootFolder "Inactive Mailbox Archive" -AllowLegacyDNMismatch
    ```

  
## <a name="more-information"></a>Plus d’informations

- **Quelle est la principale différence entre la récupération et la restauration d'une boîte aux lettres inactive ?** Lorsque vous récupérez une boîte aux lettres inactive, la boîte aux lettres est généralement convertie en une nouvelle boîte aux lettres, le contenu et la structure de dossiers de la boîte aux lettres inactive sont conservés et la boîte aux lettres est liée à un nouveau compte d'utilisateur. Une fois récupérée, la boîte aux lettres inactive n'existe plus et les modifications apportées au contenu dans la nouvelle boîte aux lettres affectent le contenu placé en attente dans la boîte aux lettres inactive. À l'inverse, lorsque vous restaurez une boîte aux lettres inactive, le contenu est simplement copié vers une autre boîte aux lettres. La boîte aux lettres inactive est conservée et reste une boîte aux lettres inactive. Toute modification apportée au contenu de la boîte aux lettres cible n'affecte pas le contenu d'origine conservé dans la boîte aux lettres inactive. La boîte aux lettres inactive peut toujours faire l’objet d’une recherche à l’aide de l' [outil de recherche de contenu](run-a-content-search-in-the-security-and-compliance-center.md) dans le centre de sécurité _AMP_ Compliance Center, son contenu peut être restauré vers une autre boîte aux lettres ou il peut être récupéré ou supprimé ultérieurement. 
    
- **Comment rechercher des boîtes aux lettres inactives ?** Pour obtenir la liste des boîtes aux lettres inactives au sein de votre organisation et afficher les informations utiles à la restauration d'une boîte aux lettres inactive, vous pouvez exécuter cette commande. 

  ```
  Get-Mailbox -InactiveMailboxOnly | FL Name,PrimarySMTPAddress,DistinguishedName,ExchangeGUID,LegacyExchangeDN,ArchiveStatus
  ```

- **Utilisez une conservation pour litige ou une stratégie de rétention Office 365 pour conserver le contenu de boîte aux lettres inactive.** Si vous souhaitez conserver l’état d’une boîte aux lettres inactive après sa restauration, vous pouvez placer la boîte aux lettres cible en [conservation pour litige](https://go.microsoft.com/fwlink/?linkid=856286) ou appliquer une stratégie de rétention [Office 365](retention-policies.md) avant de restaurer la boîte aux lettres inactive. Cela empêche la suppression définitive des éléments provenant de la boîte aux lettres inactive après leur restauration dans la boîte aux lettres cible. 
    
- **Activez le blocage de rétention pour la boîte aux lettres cible avant de restaurer une boîte aux lettres inactive.** Comme les éléments provenant d'une boîte aux lettres inactive peuvent être anciens, vous pouvez envisager d'activer le blocage de rétention pour la boîte aux lettres cible avant de restaurer une boîte aux lettres inactive. Lorsque vous placez une boîte aux lettres en blocage de rétention, la stratégie de rétention qui lui est affectée n'est pas traitée jusqu'à ce que le blocage de rétention soit supprimé ou jusqu'à ce que la période de blocage de rétention soit écoulée. Ainsi, le propriétaire de la boîte aux lettres cible dispose d'un certain temps pour gérer les anciens messages de la boîte aux lettres inactive. Sinon, la stratégie de rétention risque de supprimer d'anciens éléments (ou de déplacer des éléments vers la boîte aux lettres d'archivage, si elle est activée) qui ont expiré d'après les paramètres de rétention configurés pour la boîte aux lettres cible. Pour plus d’informations, consultez [la rubrique placer une boîte aux lettres sur le blocage de rétention dans Exchange Online](https://go.microsoft.com/fwlink/?linkid=856300).
    
- **Que fait le commutateur AllowLegacyDNMismatch ?** Dans les précédents exemples pour restaurer une boîte aux lettres inactive, le commutateur **AllowLegacyDNMismatch** sert à autoriser la restauration de la boîte aux lettres inactive vers une boîte aux lettres cible différente. Dans un scénario de restauration classique, l'objectif consiste à restaurer du contenu pour lequel les boîtes aux lettres source et cible sont la même boîte aux lettres. Par défaut, l’applet **de commande New-MailboxRestoreRequest** vérifie que la valeur de la propriété **legacyExchangeDN** des boîtes aux lettres source et cible est identique. Cette vérification vous empêche de restaurer accidentellement une boîte aux lettres source vers la mauvaise boîte aux lettres cible. Si vous essayez de restaurer une boîte aux lettres inactive sans utiliser le commutateur **AllowLegacyDNMismatch**, la commande peut échouer si les boîtes aux lettres source et cible ont des valeurs différentes pour la propriété **LegacyExchangeDN**. 
    
- **Vous pouvez utiliser d'autres paramètres avec la cmdlet New-MailboxRestoreRequest pour implémenter différents scénarios de restauration pour les boîtes aux lettres inactives.** Par exemple, vous pouvez exécuter cette commande pour restaurer l'archive à partir de la boîte aux lettres inactive vers la boîte aux lettres principale de la boîte aux lettres cible. 
    
  ```
  New-MailboxRestoreRequest -SourceMailbox <inactive mailbox> -SourceIsArchive -TargetMailbox <target mailbox> -TargetRootFolder "Inactive Mailbox Archive" -AllowLegacyDNMismatch
  ```

  Vous pouvez également restaurer la boîte aux lettres principale inactive vers l'archive de la boîte aux lettres cible en exécutant cette commande.

  ```
  New-MailboxRestoreRequest -SourceMailbox <inactive mailbox> -TargetMailbox <target mailbox> -TargetIsArchive -TargetRootFolder "Inactive Mailbox" -AllowLegacyDNMismatch
  ```

- **Que fait le paramètre TargetRootFolder ?** Comme indiqué précédemment, vous pouvez utiliser le paramètre **TargetRootFolder** pour spécifier un dossier dans la partie supérieure de la structure de dossiers (également appelée racine) de la boîte aux lettres cible vers laquelle restaurer le contenu de la boîte aux lettres inactive. Si vous n'utilisez pas ce paramètre, les éléments de la boîte aux lettres inactive sont fusionnés dans les dossiers par défaut correspondants de la boîte aux lettres cible et les dossiers personnalisés sont recréés à la racine de la boîte aux lettres cible. Les illustrations suivantes soulignent ces différences entre la non-utilisation et l'utilisation du paramètre **TargetRootFolder**. 
    
    **Hiérarchie des dossiers dans la boîte aux lettres cible lorsque le paramètre TargetRootFolder n'est pas utilisé**
    
    ![Capture d'écran lorsque le paramètre TargetRootFolder n'est pas utilisé](media/76a759af-f483-4d1c-8cc7-243435b5562e.png)
  
    **Hiérarchie des dossiers dans la boîte aux lettres cible lorsque le paramètre TargetRootFolder est utilisé**
    
    ![Capture d'écran lorsque le paramètre TargetRootFolder est utilisé](media/300da592-7323-48db-b8a4-07012259d113.png)

  

