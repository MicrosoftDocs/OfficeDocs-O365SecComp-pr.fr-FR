---
title: Activer l’archivage illimité dans Office 365 - aide d’administration
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
ms.assetid: e2a789f2-9962-4960-9fd4-a00aa063559e
description: 'Pour les administrateurs : Découvrez comment activer développer automatiquement l’archivage dans Office 365, qui propose aux utilisateurs du stockage illimité pour leurs boîtes aux lettres Exchange Online. Vous pouvez activer l’extension automatique d’archivage pour votre organisation ou juste pour des utilisateurs spécifiques.'
ms.openlocfilehash: 823e4ed0049e7a28a6c97c4045fb75987f43db5f
ms.sourcegitcommit: e7b87fae103a858981bdbcdf7ec55afa4751ad05
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2018
ms.locfileid: "23782151"
---
# <a name="enable-unlimited-archiving-in-office-365---admin-help"></a>Activer l’archivage illimité dans Office 365 - aide d’administration

Vous pouvez utiliser la fonctionnalité d’archivage automatique-développement Exchange Online dans Office 365 pour activer l’espace de stockage illimité pour les boîtes aux lettres d’archive. Lors de l’extension automatique d’archivage est activé, espace de stockage supplémentaire est ajouté automatiquement aux lettres d’archivage d’un utilisateur lorsqu’elle est proche de la limite de stockage. Le résultat est la capacité de stockage de boîte aux lettres illimitée. Vous pouvez activer l’archivage pour tout le monde dans votre organisation ou juste pour des utilisateurs spécifiques développer automatiquement. Pour plus d’informations sur l’extension automatique d’archivage, consultez la rubrique [vue d’ensemble de l’archivage illimité dans Office 365](unlimited-archiving.md).

## <a name="before-you-begin"></a>Avant de commencer

- Vous devez être un administrateur global dans votre organisation Office 365 ou un membre du groupe de rôles gestion de l’organisation au sein de votre organisation Exchange Online pour activer développer automatiquement l’archivage pour votre organisation ou des utilisateurs spécifiques. Sinon, vous devez être un membre d’un groupe de rôles qui a attribué le rôle destinataires de messagerie à activer développer automatiquement l’archivage pour des utilisateurs spécifiques.
    
- Lettres d’archivage d’un utilisateur doit être activé avant de pouvoir activer développer automatiquement l’archivage. Un utilisateur doit être attribué une licence Exchange Online Plan 2 pour activer la boîte aux lettres d’archive. Si un utilisateur est attribué une licence Exchange Online Plan 1, vous devrez affecter une licence séparée de l’archivage Exchange Online pour activer leur boîte aux lettres d’archive. Voir [Activer les boîtes aux lettres archive de sécurité Office 365 &amp; centre de conformité](enable-archive-mailboxes.md).
    
- Vous pouvez également utiliser PowerShell pour activer des boîtes aux lettres d’archive. Voir la section [plus d’informations](#more-information) pour obtenir un exemple de la commande PowerShell que vous pouvez utiliser pour activer des boîtes aux lettres d’archive pour tous les utilisateurs de votre organisation. 
    
- Développer automatiquement l’archivage également prend en charge les boîtes aux lettres partagées. Pour activer l’archivage pour une boîte aux lettres partagée, une licence Exchange Online Plan 2 ou une licence Exchange Online Plan 1 avec une licence de l’archivage Exchange Online est nécessaire.
    
- Vous ne pouvez pas utiliser le centre d’administration Exchange ou la sécurité &amp; centre de conformité permettant de développer automatiquement l’archivage. Vous devez utiliser Exchange Online PowerShell. Pour vous connecter à votre organisation Exchange Online PowerShell à distance, voir [se connecter à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).
    
  
## <a name="enable-auto-expanding-archiving-for-your-entire-organization"></a>Activer l’extension automatique de l’archivage pour votre organisation

Vous pouvez activer l’extension automatique de l’archivage pour votre organisation. Une fois que vous l’activer, développer automatiquement l’archivage sera activé pour les boîtes aux lettres utilisateur existantes et nouvelles boîtes aux lettres utilisateur sont créés. Lorsque vous créez de nouvelles boîtes aux lettres utilisateur, veillez à activer la boîte aux lettres principale d’archivage afin que la fonctionnalité d’archivage automatique-développement fonctionnera pour la nouvelle boîte aux lettres utilisateur.
  
1. [Connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554)
    
2. Exécutez la commande suivante dans Exchange Online PowerShell pour activer l’extension automatique de l’archivage pour votre organisation.

    ```
    Set-OrganizationConfig -AutoExpandingArchive
    ```
  
## <a name="enable-auto-expanding-archiving-for-specific-users"></a>Activer développer automatiquement l’archivage pour des utilisateurs spécifiques

Au lieu d’activer l’extension automatique de l’archivage pour tous les utilisateurs de votre organisation, vous pouvez activer simplement pour des utilisateurs spécifiques. Vous pouvez procéder parce uniquement certains utilisateurs peuvent avoir besoin d’un stockage d’archives de très grande taille.
  
Lorsque vous activez l’extension automatique de l’archivage pour un utilisateur spécifique, les modifications de deux configurations suivantes sont également apportées :
  
- Le quota de stockage de boîte aux lettres de l’utilisateur principal d’archivage est augmenté de 10 Go (de 100 à 110 Go). Le quota d’avertissement d’archivage est également augmenté de 10 Go (de 90 à 100 Go).
    
- Le quota de stockage pour le dossier éléments récupérables dans la boîte aux lettres principale de l’utilisateur est augmenté de 10 Go (également de 100 à 110 Go). Le quota d’avertissement éléments récupérables est également augmenté de 10 Go (de 90 à 100 Go). Ces modifications sont applicables uniquement si la boîte aux lettres en blocage ou affectés à une stratégie de rétention d’Office 365.
    
Cet espace supplémentaire est ajouté pour éviter les problèmes de stockage qui peuvent se produire avant l’archive de l’extension automatique est mis en service. Notez que stockage supplémentaire espace *n’est pas* ajouté lorsque vous activez l’extension automatique de l’archivage pour votre organisation, comme décrit dans la section précédente. 
  
1. [Connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554)
    
2. Exécutez la commande suivante dans Exchange Online PowerShell permettant de développer automatiquement l’archivage pour un utilisateur spécifique. Comme expliqué précédemment, la boîte aux lettres de l’utilisateur archive (archive principale) doit être activé avant que vous pouvez activer l’archivage pour cet utilisateur Développer automatiquement.
    
    ```
    Enable-Mailbox <user mailbox> -AutoExpandingArchive
    ```


> [!IMPORTANT]
> Dans un déploiement Exchange hybride, vous ne pouvez pas utiliser la commande **Enable-Mailbox-AutoExpandingArchive** pour activer l’archivage pour spécifiques à un utilisateur de boîte aux lettres principale est localement développer automatiquement et leur boîte aux lettres d’archive est basée sur le cloud. Pour activer l’extension automatique de l’archivage pour les boîtes aux lettres d’archive en nuage dans un déploiement Exchange hybride, vous devez exécutez la commande **Set-OrganizationConfig-AutoExpandingArchive** dans Exchange Online PowerShell permettant de développer automatiquement l’archivage pour l’organisation toute entière. Si l’utilisateur principal et boîtes aux lettres d’archivage sont basées sur le nuage, vous pouvez utiliser la commande **Enable-Mailbox-AutoExpandingArchive** permettant de développer automatiquement l’archivage pour un utilisateur spécifique. 
  
## <a name="verify-that-auto-expanding-archiving-is-enabled"></a>Vérifiez que développer automatiquement l’archivage est activé.

Pour vérifier que l’extension automatique d’archivage est activé pour votre organisation, exécutez la commande suivante dans Exchange Online PowerShell.

```
Get-OrganizationConfig | FL AutoExpandingArchiveEnabled
```

La valeur `True` développer automatiquement l’archivage est activé pour l’organisation. 
  
Pour vérifier que l’extension automatique d’archivage est activer pour un utilisateur spécifique, exécutez la commande suivante dans Exchange Online PowerShell.
  
```
Get-Mailbox <user mailbox> | FL AutoExpandingArchiveEnabled
```
La valeur `True` développer automatiquement l’archivage est activé pour l’utilisateur. 
  
Gardez les éléments suivants à l’esprit une fois que vous activez développer automatiquement l’archivage :
  
- Si vous exécutez la commande **Set-OrganizationConfig-AutoExpandingArchive** permettant de développer automatiquement l’archivage pour votre organisation, vous n’êtes pas obligé d’exécuter **Enable-Mailbox-AutoExpandingArchive** sur des boîtes aux lettres. Notez ce qui exécute l’applet de commande **Set-OrganizationConfig** permettant de développer automatiquement l’archivage pour votre organisation ne change pas la propriété *AutoExpandingArchiveEnabled* sur les boîtes aux lettres utilisateur vers `True`.
    
- De même, les valeurs pour les propriétés de boîte aux lettres *ArchiveQuota* et *ArchiveWarningQuota* ne sont pas modifiées lorsque vous activez développer automatiquement l’archivage. En fait, lorsque vous activez développer automatiquement l’archivage pour une boîte aux lettres utilisateur et la propriété *AutoExpandingArchiveEnabled* est définie sur `True`, les propriétés *ArchiveQuota* et *ArchiveWarningQuota* sont simplement ignorées. Voici un exemple de ces propriétés de boîte aux lettres après que développer automatiquement l’archivage est activé pour la boîte aux lettres d’un utilisateur. 
    
    ![Propriétés ArchiveQuota et ArchiveWarningQuota sont ignorées une fois que vous activez développer automatiquement l’archivage](media/6a1c1b69-5c4c-4267-aac8-53577667f03e.png)

  
## <a name="more-information"></a>Plus d'informations

- Vous pouvez également utiliser PowerShell pour activer des boîtes aux lettres d’archive. Par exemple, vous pouvez exécuter la commande suivante dans Exchange Online PowerShell pour activer des boîtes aux lettres d’archive pour tous les utilisateurs dont boîte aux lettres d’archivage n’est pas déjà activé.

    ```
    Get-Mailbox -Filter {ArchiveStatus -Eq "None" -AND RecipientTypeDetails -eq "UserMailbox"} | Enable-Mailbox -Archive
    ```

- Une fois que vous activez l’archivage pour votre organisation ou pour un utilisateur spécifique développer automatiquement, une boîte aux lettres d’archive est convertie en une archive développer automatiquement lorsque la boîte aux lettres d’archivage (y compris le dossier éléments récupérables) atteint 90 Go. Cela peut prendre jusqu'à 30 jours pour l’espace de stockage supplémentaire être mis en service.
    
- Après avoir activé l’archivage automatique en expansion, elle ne peut pas être désactivée.
    
- Développer automatiquement l’archivage est pris en charge pour les boîtes aux lettres d’archive en nuage dans un déploiement Exchange hybride pour les utilisateurs qui disposent d’une boîte aux lettres principale locale. Toutefois, après que l’extension automatique d’archivage est activé pour une boîte aux lettres d’archive en nuage, vous ne pouvez pas bord cette boîte aux lettres d’archivage à l’organisation Exchange locale.
    
- Pour obtenir la liste des clients Outlook qui permettent aux utilisateurs d’accéder aux éléments dans la zone de stockage supplémentaire dans leur boîte aux lettres d’archivage, consultez la section « Critères d’Outlook pour accéder aux éléments dans une archive développé automatique » dans la [vue d’ensemble d’un nombre illimité d’archivage dans Office 365](unlimited-archiving.md#outlook-requirements-for-accessing-items-in-an-auto-expanded-archive) .
    
- Comme expliqué précédemment, 10 Go est ajouté au quota de stockage de boîte aux lettres de l’utilisateur principal d’archivage (et dans le dossier éléments récupérables si la boîte aux lettres est sur Maintenez) lorsque vous exécutez la commande **Enable-Mailbox-AutoExpandingArchive** . Cela offre un stockage supplémentaire jusqu'à ce que l’espace de stockage étendu automatique est mis en service (qui peut prendre jusqu'à 30 jours). Cet espace de stockage supplémentaire n’est pas ajouté lorsque vous exécutez **AutoExpandingArchive-Set-OrganizationConfig** activer développer automatiquement l’archivage pour toutes les boîtes aux lettres dans votre organisation. Si vous activé développer automatiquement l’archivage pour toute l’organisation, mais vous devez ajouter le plus 10 Go d’espace de stockage pour un utilisateur spécifique, vous pouvez exécuter la commande **Enable-Mailbox-AutoExpandingArchive** sur cette boîte aux lettres. Notez que vous recevez une erreur indiquant que développer automatiquement l’archivage a déjà été activée, mais l’espace de stockage supplémentaire est ajouté à la boîte aux lettres. 
