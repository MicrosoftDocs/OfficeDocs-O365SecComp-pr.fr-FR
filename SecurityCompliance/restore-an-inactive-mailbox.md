---
title: Restaurer une boîte aux lettres inactive dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 8/28/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 97e06a7a-ef9a-4ce8-baea-18b9e20449a3
description: Si un nouvel employé ou un autre utilisateur a besoin d’accéder au contenu d’une boîte aux lettres inactive dans Office 365, vous pouvez restaurer (ou fusionner) le contenu de la boîte aux lettres inactive dans une boîte aux lettres existante.
ms.openlocfilehash: e0add2b63a48edc27795143324c83153b15dcf8c
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527577"
---
# <a name="restore-an-inactive-mailbox-in-office-365"></a>Restaurer une boîte aux lettres inactive dans Office 365

Une boîte aux lettres inactive (qui est un type de boîte aux lettres supprimée) est utilisée pour conserver le courrier électronique d’un ancien employé une fois qu’il quitte l’organisation. Si un autre employé prend en charge les responsabilités de l’employé quittée ou si celui-ci renvoie à votre organisation, il existe deux méthodes que vous pouvez apporter le contenu de la boîte aux lettres inactive disponibles à un utilisateur : 
  
- **Restaurer une boîte aux lettres inactive** Si un autre employé assume les responsabilités de l'employé qui est parti, ou si un autre utilisateur doit accéder au contenu de la boîte aux lettres inactive, vous pouvez restaurer (ou fusionner) le contenu de la boîte aux lettres inactive vers une boîte aux lettres existante. Vous pouvez également restaurer l'archive d'une boîte aux lettres inactive. Une fois restaurée, la boîte aux lettres inactive est conservée sous la forme d'une boîte aux lettres inactive. Cette rubrique décrit les procédures de restauration d'une boîte aux lettres inactive. 
    
- **Récupérer une boîte aux lettres inactive** Si l’employé quittée renvoie à votre organisation, ou si un nouvel employé à effectuer sur les responsabilités de l’employé quittée, vous pouvez récupérer le contenu de la boîte aux lettres inactive. Cette méthode convertit la boîte aux lettres inactive dans une nouvelle boîte aux lettres qui contient le contenu de la boîte aux lettres inactive. Une fois qu’il est récupéré, la boîte aux lettres inactive n’existe plus. Pour les procédures pas à pas, consultez la rubrique [récupérer une boîte aux lettres inactive dans Office 365](recover-an-inactive-mailbox.md).
    
Voir la section **plus d’informations** dans cet article pour plus d’informations sur les différences entre la restauration et récupération d’une boîte aux lettres inactive. 
  
## <a name="before-you-begin"></a>Avant de commencer

- Vous devez utiliser Exchange Online PowerShell pour restaurer une boîte aux lettres inactive. Vous ne pouvez pas utiliser le centre d’administration Exchange (CAE). Pour obtenir des instructions détaillées, voir [se connecter à Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=396554).
    
- Exécutez la commande suivante dans Exchange Online PowerShell pour obtenir des informations d’identité pour les boîtes aux lettres inactives dans votre organisation. 
    
    ```
    Get-Mailbox -InactiveMailboxOnly | FL Name,DistinguishedName,ExchangeGuid,PrimarySmtpAddress
    ```

     Utilisez les informations renvoyées par cette commande pour restaurer une boîte aux lettres inactive spécifique.
    
- Pour plus d’informations sur les boîtes aux lettres inactives, voir [boîtes aux lettres inactives dans Office 365](inactive-mailboxes-in-office-365.md).
    
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

  
## <a name="more-information"></a>Plus d'informations

- **Quelle est la différence principale entre la récupération et la restauration d’une boîte aux lettres inactive ?** Lorsque vous récupérez une boîte aux lettres inactive, la boîte aux lettres est converti en fait une nouvelle boîte aux lettres, le contenu et la structure de dossiers de la boîte aux lettres inactive sont conservés, et la boîte aux lettres est liée à un nouveau compte d’utilisateur. Une fois qu’il est récupéré, la boîte aux lettres inactive n’existe plus, et toutes les modifications apportées au contenu dans la nouvelle boîte aux lettres déterminent le contenu qui a été initialement sur permanente dans la boîte aux lettres inactive. Inversement, lorsque vous restaurez une boîte aux lettres inactive, le contenu est simplement copié à une autre boîte aux lettres. La boîte aux lettres inactive est conservée et reste une boîte aux lettres inactive. Toutes les modifications apportées au contenu dans la boîte aux lettres cible n’affectent pas le contenu d’origine est conservé dans la boîte aux lettres inactive. La boîte aux lettres inactive peut toujours être recherché à l’aide de l' [outil de recherche de contenu](run-a-content-search-in-the-security-and-compliance-center.md) de sécurité Office 365 &amp; centre de conformité, son contenu peut être restauré à une autre boîte aux lettres, ou peut être récupéré ou supprimé à une date ultérieure. 
    
- **Comment rechercher des boîtes aux lettres inactives ?** Pour obtenir la liste des boîtes aux lettres inactives au sein de votre organisation et afficher les informations utiles à la restauration d'une boîte aux lettres inactive, vous pouvez exécuter cette commande. 

  ```
  Get-Mailbox -InactiveMailboxOnly | FL Name,PrimarySMTPAddress,DistinguishedName,ExchangeGUID,LegacyExchangeDN,ArchiveStatus
  ```

- **Utiliser une stratégie de rétention litige ou Office 365 pour conserver le contenu de la boîte aux lettres inactive.** Si vous souhaitez conserver l’état d’une boîte aux lettres inactive après que l’avoir restauré, vous pouvez placer la boîte aux lettres cible [litige](https://go.microsoft.com/fwlink/?linkid=856286) ou appliquer une [stratégie de rétention Office 365](retention-policies.md) avant de restaurer la boîte aux lettres inactive. Cela empêche la suppression définitive de tous les éléments de la boîte aux lettres inactive une fois qu’ils sont restaurés à la boîte aux lettres cible. 
    
- **Blocage de rétention activer dans la boîte aux lettres cible avant de restaurer une boîte aux lettres inactive.** Étant donné que les éléments de boîte aux lettres à partir d’une boîte aux lettres inactive peuvent être anciennes, pensez à activer le blocage de rétention sur la boîte aux lettres cible avant de restaurer une boîte aux lettres inactive. Lorsque vous placez une boîte aux lettres sur la rétention attente, la stratégie de rétention qui lui est affectée ne sera pas traitée jusqu'à ce que le blocage de rétention est supprimé ou l’expiration de la période jusqu'à ce que le blocage de la rétention. Ainsi, le propriétaire de l’heure de la boîte aux lettres cible pour gérer les anciens messages à partir de la boîte aux lettres inactive. Dans le cas contraire, la stratégie de rétention peut supprimer les anciens éléments (ou déplacer les éléments vers la boîte aux lettres d’archive, s’il est activé) qui ont expiré selon les paramètres de rétention configurés pour la boîte aux lettres cible. Pour plus d’informations, voir [une boîte aux lettres sur la rétention archive dans Exchange Online](https://go.microsoft.com/fwlink/?linkid=856300).
    
- **Que faire le commutateur AllowLegacyDNMismatch ?** Dans les exemples précédents, pour restaurer une boîte aux lettres inactive, le commutateur **AllowLegacyDNMismatch** est utilisé pour permettre la restauration de la boîte aux lettres inactive à une boîte aux lettres cible différent. Dans un scénario de restauration par défaut, l’objectif est de restaurer le contenu où les boîtes aux lettres source et cible sont la même boîte aux lettres. Ainsi, par défaut, l’applet de commande **New-MailboxRestoreRequest** vérifie pour s’assurer que la valeur de la propriété **LegacyExchangeDN** sur les boîtes aux lettres source et cible est les mêmes. Ainsi, vous vous empêche de restauration par inadvertance une boîte aux lettres source dans la boîte aux lettres cible incorrecte. Si vous essayez de restaurer une boîte aux lettres inactive sans utiliser le commutateur **AllowLegacyDNMismatch** , la commande peut échouer si les boîtes aux lettres source et cible ont des valeurs différentes pour la propriété **LegacyExchangeDN** . 
    
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

  

