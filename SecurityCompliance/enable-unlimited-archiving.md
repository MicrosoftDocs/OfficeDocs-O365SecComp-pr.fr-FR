---
title: Activer l'archivage illimité dans Office 365-aide de l'administrateur
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: e2a789f2-9962-4960-9fd4-a00aa063559e
description: "Pour les administrateurs: Découvrez comment activer l'archivage à extension automatique dans Office 365, qui permet à vos utilisateurs de disposer d'un espace de stockage illimité pour leurs boîtes aux lettres Exchange Online. Vous pouvez activer l'archivage à extension automatique pour l'ensemble de votre organisation ou uniquement pour des utilisateurs spécifiques."
ms.openlocfilehash: 39098ffc78d0379436cafb20e5a484ec0e7aa283
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215394"
---
# <a name="enable-unlimited-archiving-in-office-365---admin-help"></a>Activer l'archivage illimité dans Office 365-aide de l'administrateur

Vous pouvez utiliser la fonctionnalité d'archivage Exchange Online avec extension automatique dans Office 365 pour activer un espace de stockage illimité pour les boîtes aux lettres d'archivage. Lorsque l'archivage à extension automatique est activé, un espace de stockage supplémentaire est automatiquement ajouté à la boîte aux lettres d'archivage d'un utilisateur lorsqu'il approche de la limite de stockage. Le résultat est une capacité de stockage de boîte aux lettres illimitée. Vous pouvez activer l'archivage à extension automatique pour tous les membres de votre organisation ou uniquement pour des utilisateurs spécifiques. Pour plus d'informations sur l'archivage à extension automatique, consultez la rubrique [vue d'ensemble de l'archivage illimité dans Office 365](unlimited-archiving.md).

## <a name="before-you-begin"></a>Avant de commencer

- Vous devez être un administrateur général dans votre organisation Office 365 ou membre du groupe de rôles gestion de l'organisation dans votre organisation Exchange Online pour activer l'archivage à extension automatique pour l'ensemble de votre organisation ou pour des utilisateurs spécifiques. Vous pouvez également être membre d'un groupe de rôles auquel est affecté le rôle destinataires de messagerie pour activer l'archivage à extension automatique pour des utilisateurs spécifiques.
    
- La boîte aux lettres d'archivage d'un utilisateur doit être activée pour pouvoir activer l'archivage à extension automatique. Un utilisateur doit disposer d'une licence Exchange Online plan 2 pour activer la boîte aux lettres d'archivage. Si un utilisateur se voit attribuer une licence Exchange Online plan 1, vous devez lui attribuer une licence d'archivage Exchange Online distincte pour activer sa boîte aux lettres d'archivage. Consultez [la rubrique activation des boîtes aux lettres d'archivage dans le centre de sécurité &amp; conformité Office 365](enable-archive-mailboxes.md).
    
- Vous pouvez également utiliser PowerShell pour activer les boîtes aux lettres d'archivage. Consultez la section [plus d'informations](#more-information) pour obtenir un exemple de la commande PowerShell que vous pouvez utiliser pour activer des boîtes aux lettres d'archivage pour tous les utilisateurs de votre organisation. 
    
- L'archivage à extension automatique prend également en charge les boîtes aux lettres partagées. Pour activer l'archivage pour une boîte aux lettres partagée, une licence Exchange Online plan 2 ou une licence Exchange Online plan 1 avec une licence d'archivage Exchange Online est requise.
    
- Vous ne pouvez pas utiliser le centre d'administration Exchange &amp; ou le centre de sécurité conformité pour activer l'archivage à extension automatique. Vous devez utiliser Exchange Online PowerShell. Pour vous connecter à votre organisation Exchange Online à l'aide de Remote PowerShell, consultez la rubrique [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).
    
  
## <a name="enable-auto-expanding-archiving-for-your-entire-organization"></a>Activer l'archivage à extension automatique pour l'ensemble de votre organisation

Vous pouvez activer l'archivage à extension automatique pour l'ensemble de votre organisation. Une fois que vous l'activez, l'archivage à extension automatique est activé pour les boîtes aux lettres utilisateur existantes et pour les nouvelles boîtes aux lettres utilisateur qui sont créées. Lorsque vous créez des boîtes aux lettres utilisateur, veillez à activer la boîte aux lettres d'archivage principale de l'utilisateur de sorte que la fonctionnalité d'archivage à extension automatique fonctionne pour la nouvelle boîte aux lettres utilisateur.
  
1. [Connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554)
    
2. Exécutez la commande suivante dans Exchange Online PowerShell pour activer l'archivage à extension automatique pour l'ensemble de votre organisation.

    ```
    Set-OrganizationConfig -AutoExpandingArchive
    ```
  
## <a name="enable-auto-expanding-archiving-for-specific-users"></a>Activer l'archivage à extension automatique pour des utilisateurs spécifiques

Au lieu d'activer l'archivage à extension automatique pour chaque utilisateur de votre organisation, vous pouvez simplement l'activer pour des utilisateurs spécifiques. Vous pouvez effectuer cette opération, car seuls certains utilisateurs peuvent avoir besoin d'un stockage d'archive très volumineux.
  
Lorsque vous activez l'archivage à extension automatique pour un utilisateur spécifique et que la boîte aux lettres de l'utilisateur est en conservation ou affectée à une stratégie de rétention Office 365, les deux modifications de configuration suivantes sont apportées:
  
- Le quota de stockage de la boîte aux lettres d'archivage principale de l'utilisateur est augmenté de 10 Go (de 100 Go à 110 Go). Le quota d'avertissement d'archivage augmente de 10 Go (de 90 Go à 100 Go).
    
- Le quota de stockage pour le dossier éléments récupérables dans la boîte aux lettres principale de l'utilisateur est augmenté de 10 Go (également de 100 Go à 110 Go). Le quota d'avertissement des éléments récupérables augmente de 10 Go (de 90 Go à 100 Go). Ces modifications ne s'appliquent que si la boîte aux lettres est en conservation ou affectée à une stratégie de rétention Office 365.
    
Cet espace supplémentaire est ajouté pour éviter tout problème de stockage pouvant survenir avant la mise en service de l'archive à extension automatique. Notez que l'espace de stockage supplémentaire *n'est pas* ajouté lorsque vous activez l'archivage à extension automatique pour l'ensemble de votre organisation, comme décrit dans la section précédente. 
  
1. [Connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554)
    
2. Exécutez la commande suivante dans Exchange Online PowerShell pour activer l'archivage à extension automatique pour un utilisateur spécifique. Comme expliqué précédemment, la boîte aux lettres d'archivage de l'utilisateur (Archive principale) doit être activée pour pouvoir activer l'archivage à extension automatique pour cet utilisateur.
    
    ```
    Enable-Mailbox <user mailbox> -AutoExpandingArchive
    ```


> [!IMPORTANT]
> Dans un déploiement hybride Exchange, vous ne pouvez pas utiliser la commande **Enable-Mailbox-AutoExpandingArchive** pour activer l'archivage à extension automatique pour un utilisateur dont la boîte aux lettres principale est locale et dont la boîte aux lettres d'archivage est basée sur le Cloud. Pour activer l'archivage en développement automatique pour les boîtes aux lettres d'archivage informatique dans un déploiement hybride Exchange, vous devez exécuter la commande **Set-OrganizationConfig-AutoExpandingArchive** dans Exchange Online PowerShell pour activer l'archivage à extension automatique pour l'ensemble de l'organisation. Si les boîtes aux lettres principales et d'archivage d'un utilisateur sont à la fois basées sur le Cloud, vous pouvez utiliser la commande **Enable-Mailbox-AutoExpandingArchive** pour activer l'archivage à extension automatique pour cet utilisateur spécifique. 
  
## <a name="verify-that-auto-expanding-archiving-is-enabled"></a>Vérifier que l'archivage à extension automatique est activé

Pour vérifier que l'archivage à extension automatique est activé pour votre organisation, exécutez la commande suivante dans Exchange Online PowerShell.

```
Get-OrganizationConfig | FL AutoExpandingArchiveEnabled
```

La valeur `True` indique que l'archivage à extension automatique est activé pour l'organisation. 
  
Pour vérifier que l'archivage à extension automatique est activé pour un utilisateur spécifique, exécutez la commande suivante dans Exchange Online PowerShell.
  
```
Get-Mailbox <user mailbox> | FL AutoExpandingArchiveEnabled
```
La valeur `True` indique que l'archivage à extension automatique est activé pour l'utilisateur. 
  
Gardez les points suivants à l'esprit après avoir activé l'archivage à extension automatique:
  
- Si vous exécutez la commande **Set-OrganizationConfig-AutoExpandingArchive** pour activer l'archivage à extension automatique pour votre organisation, il n'est pas nécessaire d'exécuter la commande **Enable-Mailbox-AutoExpandingArchive** sur des boîtes aux lettres individuelles. Notez que l'exécution de l'applet de commande **Set-OrganizationConfig** pour activer l'archivage à extension automatique pour ** votre organisation ne modifie pas la propriété `True`AutoExpandingArchiveEnabled sur les boîtes aux lettres des utilisateurs.
    
- De même, les valeurs des propriétés de boîte aux lettres *ArchiveQuota* et *ArchiveWarningQuota* ne sont pas modifiées lorsque vous activez l'archivage à extension automatique. En fait, lorsque vous activez l'archivage à extension automatique pour une boîte aux lettres ** utilisateur et que la propriété `True`AutoExpandingArchiveEnabled est définie sur, les propriétés *ArchiveQuota* et *ArchiveWarningQuota* sont simplement ignorées. Voici un exemple de ces propriétés de boîte aux lettres après que l'archivage en développement automatique est activé pour la boîte aux lettres d'un utilisateur. 
    
    ![Les propriétés ArchiveQuota et ArchiveWarningQuota sont ignorées après l'activation de l'archivage à extension automatique](media/6a1c1b69-5c4c-4267-aac8-53577667f03e.png)

  
## <a name="more-information"></a>Plus d’informations

- Vous pouvez également utiliser PowerShell pour activer les boîtes aux lettres d'archivage. Par exemple, vous pouvez exécuter la commande suivante dans Exchange Online PowerShell pour activer les boîtes aux lettres d'archivage pour tous les utilisateurs dont la boîte aux lettres d'archivage n'est pas déjà activée.

    ```
    Get-Mailbox -Filter {ArchiveStatus -Eq "None" -AND RecipientTypeDetails -eq "UserMailbox"} | Enable-Mailbox -Archive
    ```

- Après l'activation de l'archivage à extension automatique pour votre organisation ou pour un utilisateur spécifique, une boîte aux lettres d'archivage est convertie en archive de développement automatique lorsque la boîte aux lettres d'archivage (y compris le dossier éléments récupérables) atteint 90 Go. La mise en service de l'espace de stockage supplémentaire peut prendre jusqu'à 30 jours.
    
- Une fois l'archivage à extension automatique activé, il est impossible de l'activer.
    
- L'archivage à extension automatique est pris en charge pour les boîtes aux lettres d'archivage en nuage dans un déploiement hybride Exchange pour les utilisateurs disposant d'une boîte aux lettres principale locale. Toutefois, une fois que l'archivage en développement automatique est activé pour une boîte aux lettres d'archivage informatique, vous ne pouvez pas désactiver l'archivage de la boîte aux lettres dans l'organisation Exchange locale.
    
- Pour obtenir la liste des clients Outlook que les utilisateurs peuvent utiliser pour accéder aux éléments de la zone de stockage supplémentaire dans leur boîte aux lettres d'archivage, consultez la section «Configuration requise par Outlook pour accéder aux éléments dans une archive étendue automatiquement» dans [vue d'ensemble d'un archivage illimité dans Office 365](unlimited-archiving.md#outlook-requirements-for-accessing-items-in-an-auto-expanded-archive) .
    
- Comme indiqué précédemment, 10 Go est ajouté au quota de stockage de la boîte aux lettres d'archivage principale de l'utilisateur (et au dossier éléments récupérables si la boîte aux lettres est en conservation) lorsque vous exécutez la commande **Enable-Mailbox-AutoExpandingArchive** . Cela permet un stockage supplémentaire jusqu'à ce que l'espace de stockage étendu automatiquement soit mis en service (ce qui peut prendre jusqu'à 30 jours). Cet espace de stockage supplémentaire n'est pas ajouté lorsque vous exécutez le **Set-OrganizationConfig-AutoExpandingArchive** pour activer l'archivage à extension automatique pour toutes les boîtes aux lettres de votre organisation. Si vous avez activé l'archivage à extension automatique pour l'ensemble de l'organisation, mais que vous avez besoin d'ajouter 10 Go d'espace de stockage supplémentaire pour un utilisateur spécifique, vous pouvez exécuter la commande **Enable-Mailbox-AutoExpandingArchive** sur cette boîte aux lettres. Notez que vous recevrez une erreur indiquant que l'archivage à extension automatique a déjà été activé, mais que l'espace de stockage supplémentaire sera ajouté à la boîte aux lettres. 
