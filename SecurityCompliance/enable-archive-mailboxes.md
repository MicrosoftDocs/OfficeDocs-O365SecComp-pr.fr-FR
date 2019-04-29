---
title: Activer les boîtes aux lettres d'archivage dans le centre de sécurité & conformité
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.ArchivingHelp
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 268a109e-7843-405b-bb3d-b9393b2342ce
description: Utilisez le centre de sécurité & conformité dans Office 365 pour activer les boîtes aux lettres d'archivage afin de prendre en charge les exigences de rétention, eDiscovery et de conservation des messages de votre organisation.
ms.openlocfilehash: f4f02e5107526f2f45b0a46579e0676b791f0dd1
ms.sourcegitcommit: e23b84ef4eee9cccec7205826b71ddfe9aaac2f8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33402922"
---
# <a name="enable-archive-mailboxes-in-the-security--compliance-center"></a>Activer les boîtes aux lettres d'archivage dans le centre de sécurité & conformité
  
L'archivage dans Office 365 (également appelé archivage inaltérable) fournit aux utilisateurs un espace de stockage de boîte aux lettres supplémentaire. Une fois que vous avez activé les boîtes aux lettres d'archivage, les utilisateurs peuvent accéder aux messages et les stocker dans leurs boîtes aux lettres d'archivage à l'aide de Microsoft Outlook et Outlook sur le Web (anciennement Outlook Web App). Les utilisateurs peuvent également déplacer ou copier des messages entre leur boîte aux lettres principale et leur boîte aux lettres d'archivage. Ils peuvent également récupérer des éléments supprimés du dossier éléments récupérables dans leur boîte aux lettres d'archivage à l'aide de l'outil récupérer les éléments supprimés. 
  
> [!TIP]
> Office 365 offre une quantité illimitée de stockage d'archives grâce à la fonctionnalité d'archivage à extension automatique. Lorsque l'archivage à extension automatique est activé, puis que le quota de stockage initial dans la boîte aux lettres d'archivage d'un utilisateur est atteint, Office 365 ajoute automatiquement de l'espace de stockage supplémentaire. Cela signifie que les utilisateurs ne manqueront pas d'espace de stockage de boîte aux lettres et que vous n'aurez pas à gérer les éléments après l'activation initiale de la boîte aux lettres d'archivage et activez l'archivage à extension automatique pour votre organisation. Pour plus d'informations, reportez-vous à la rubrique relative à la [présentation de l'archivage illimité dans Office 365](unlimited-archiving.md). 
  
## <a name="before-you-begin"></a>Avant de commencer

Vous devez disposer du rôle destinataires de messagerie dans Exchange Online pour activer ou désactiver les boîtes aux lettres d'archivage. Par défaut, ce rôle est affecté aux groupes de rôles Gestion des destinataires et gestion de l'organisation dans la page **autorisations** du centre d'administration Exchange. Si vous ne voyez pas la page d' **Archive** dans le centre de sécurité _AMP_ Compliance Center, demandez à votre administrateur de vous accorder les autorisations nécessaires. 
  
## <a name="enable-an-archive-mailbox"></a>Activation d’une boîte aux lettres d’archivage
  
1. Accédez à la page [https://protection.office.com](https://protection.office.com).
    
2. Connectez-vous à Office 365 à l'aide de votre compte scolaire ou professionnel.
    
3. Dans le volet gauche du centre de sécurité & conformité, cliquez sur **Archives**de **gouvernance** \> des données.
    
    La page **Archive** s’affiche. La colonne **Boîte aux lettres d’archivage** indique si une boîte aux lettres d’archivage est activée ou désactivée pour chaque utilisateur. 
    
4. Dans la liste des boîtes aux lettres, sélectionnez l’utilisateur pour lequel vous voulez activer la boîte aux lettres d’archivage.
    
    ![Cliquez sur activer dans le volet d'informations de l'utilisateur sélectionné pour activer la boîte aux lettres d'archivage.](media/8b53cdec-d5c9-4c28-af11-611f95c37b34.png)
  
5. Dans le volet d'informations de l'utilisateur sélectionné, cliquez sur **activer**. 
    
    Un avertissement s'affiche indiquant que si vous activez la boîte aux lettres d'archivage, les éléments de la boîte aux lettres de l'utilisateur qui sont antérieurs à la stratégie d'archivage affectée à la boîte aux lettres seront déplacés vers la nouvelle boîte aux lettres d'archivage. La stratégie d'archivage par défaut qui fait partie de la stratégie de rétention attribuée aux boîtes aux lettres Exchange Online déplace des éléments vers la boîte aux lettres d'archivage deux ans après la date à laquelle l'élément a été remis à la boîte aux lettres ou créé par l'utilisateur. Pour plus d'informations, reportez-vous à la section **plus** d'informations de cet article. 
    
6. Cliquez sur **Oui** pour activer la boîte aux lettres d’archivage. 
    
    La création de la boîte aux lettres d’archivage peut prendre un certain temps. Lors de sa création, la **boîte aux lettres d'archivage: activée** s'affiche dans le volet d'informations de l'utilisateur sélectionné. Vous devrez peut-être **** ![cliquer sur Actualiser l'icône](media/O365-MDM-Policy-RefreshIcon.gif) actualiser pour mettre à jour les informations dans le volet d'informations. 
    
> [!TIP]
> Vous pouvez également activer des boîtes aux lettres d’archivage en bloc en sélectionnant plusieurs utilisateurs dont les boîtes aux lettres sont désactivées (à l’aide de la touche Maj ou Ctrl). Une fois les boîtes aux lettres sélectionnées, cliquez sur **Activer** dans le volet des détails.  
  
## <a name="disable-an-archive-mailbox"></a>Désactiver une boîte aux lettres d’archivage
  
Vous pouvez également utiliser la page d' **Archive** dans le centre de sécurité _AMP_ Compliance Center pour désactiver la boîte aux lettres d'archivage d'un utilisateur. Après avoir désactivé une boîte aux lettres d’archivage, vous pouvez la reconnecter à la boîte aux lettres principale de l’utilisateur dans les 30 jours qui suivent sa désactivation. Dans ce cas, le contenu d’origine de la boîte aux lettres d’archivage est restauré. Au bout de 30 jours, le contenu de la boîte aux lettres d’archivage d’origine est définitivement supprimé et ne peut pas être récupéré. Par conséquent, si vous réactivez l’archive plus de 30 jours après l’avoir désactivée, une nouvelle boîte aux lettres d’archivage est créée. 
  
Notez que la stratégie d'archivage par défaut affectée aux boîtes aux lettres des utilisateurs déplace les éléments vers la boîte aux lettres d'archivage deux ans après la date de remise de l'élément. Si vous désactivez la boîte aux lettres d'archivage d'un utilisateur, aucune action n'est effectuée sur les éléments de boîte aux lettres et ils resteront dans la boîte aux lettres principale de l'utilisateur.
  
Pour désactiver une boîte aux lettres d'archivage:
  
1. Accédez à la page [https://protection.office.com](https://protection.office.com).
    
2. Connectez-vous à Office 365 à l'aide de votre compte scolaire ou professionnel.
    
3. Dans le volet gauche du centre de sécurité & conformité, cliquez sur **Archives**de **gouvernance** \> des données.
    
    La page **Archive** s’affiche. La colonne **Boîte aux lettres d’archivage** indique si une boîte aux lettres d’archivage est activée ou désactivée pour chaque utilisateur. 
    
4. Dans la liste des boîtes aux lettres, sélectionnez l’utilisateur pour lequel vous voulez désactiver la boîte aux lettres d’archivage.
    
5. Dans le volet des détails, cliquez sur **Désactiver**. 
    
    Un message d'avertissement s'affiche indiquant que vous aurez 30 jours pour réactiver la boîte aux lettres d'archivage et qu'après 30 jours, toutes les informations dans l'archive seront définitivement supprimées. 
    
6. Cliquez sur **Oui** pour désactiver la boîte aux lettres d’archivage. 
    
    La désactivation de la boîte aux lettres d’archivage peut prendre un certain temps. Lorsqu'elle est désactivée, la **boîte aux lettres** d'archivage est affichée dans le volet d'informations de l'utilisateur sélectionné. Vous devrez peut-être **** ![cliquer sur Actualiser l'icône](media/O365-MDM-Policy-RefreshIcon.gif) actualiser pour mettre à jour les informations dans le volet d'informations. 
    
> [!TIP]
> Vous pouvez également désactiver des boîtes aux lettres d’archivage en bloc en sélectionnant plusieurs utilisateurs dont les boîtes aux lettres sont activées (à l’aide de la touche Maj ou Ctrl). Une fois les boîtes aux lettres sélectionnées, cliquez sur **Désactiver** dans le volet des détails.  
  
## <a name="use-exchange-online-powershell-to-enable-or-disable-archive-mailboxes"></a>Utiliser Exchange Online PowerShell pour activer ou désactiver les boîtes aux lettres d'archivage

Vous pouvez également utiliser Exchange Online PowerShell pour activer les boîtes aux lettres d'archivage. La principale raison d'utiliser PowerShell est que vous pouvez rapidement activer la boîte aux lettres d'archivage pour tous les utilisateurs de votre organisation.

La première étape consiste à vous connecter à Exchange Online PowerShell. Pour obtenir des instructions, consultez la rubrique [connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).

Une fois que vous êtes connecté à Exchange Online, vous pouvez exécuter les commandes des sections suivantes pour activer ou désactiver les boîtes aux lettres d'archivage.

### <a name="enable-archive-mailboxes"></a>Activation des boîtes aux lettres d’archivage

Exécutez la commande suivante pour activer la boîte aux lettres d'archivage pour un seul utilisateur.
    
  ```
  Enable-Mailbox -Identity <username> -Archive
  ```

Exécutez la commande suivante pour activer la boîte aux lettres d'archivage pour tous les utilisateurs de votre organisation (dont la boîte aux lettres d'archivage n'est pas activée actuellement).
    
  ```
  Get-Mailbox -Filter {ArchiveStatus -Eq "None" -AND RecipientTypeDetails -eq "UserMailbox"} | Enable-Mailbox -Archive
  ```
  
### <a name="disable-archive-mailboxes"></a>Désactiver les boîtes aux lettres d'archivage

Exécutez la commande suivante pour désactiver la boîte aux lettres d'archivage pour un seul utilisateur.
    
  ```
  Disable-Mailbox -Identity <username> -Archive
  ```

Exécutez la commande suivante pour désactiver la boîte aux lettres d'archivage pour tous les utilisateurs de votre organisation (dont la boîte aux lettres d'archivage est activée).
    
  ```
  Get-Mailbox -Filter {ArchiveStatus -Eq "Active" -AND RecipientTypeDetails -eq "UserMailbox"} | Disable-Mailbox -Archive
  ```

## <a name="more-information"></a>Plus d’informations
  
- Lorsqu'une boîte aux lettres d'archivage est activée, les utilisateurs peuvent stocker des messages dans leur boîte aux lettres d'archivage. Les utilisateurs peuvent accéder à leurs boîtes aux lettres d'archivage à l'aide de Microsoft Outlook et d'Outlook sur le Web. À l’aide de l’une de ces applications clientes, les utilisateurs peuvent afficher les messages dans leur boîte aux lettres d’archivage et déplacer ou copier des messages entre leur boîte aux lettres principale et la boîte aux lettres d’archivage. Les utilisateurs peuvent également récupérer les éléments supprimés du dossier Éléments récupérables dans leur boîte aux lettres d’archivage à l’aide de l’outil de récupération des éléments supprimés.

   Pour obtenir la liste des licences Outlook qui prennent en charge l'archivage inaltérable, consultez la rubrique [relative aux licences Outlook requises pour les fonctionnalités Exchange](https://support.office.com/article/outlook-license-requirements-for-exchange-features-46b6b7c5-c3ca-43e5-8424-1e2807917c99).

- Les boîtes aux lettres d'archivage vous permettent, ainsi qu'à vos utilisateurs, de répondre aux exigences de rétention, de découverte électronique et de conservation de votre organisation. Par exemple, vous pouvez utiliser la stratégie de rétention Exchange de votre organisation pour déplacer le contenu de boîte aux lettres vers la boîte aux lettres d'archivage des utilisateurs. Lorsque vous utilisez l'outil de recherche de contenu dans le centre de sécurité & Compliance Center pour rechercher du contenu spécifique dans la boîte aux lettres d'un utilisateur, la boîte aux lettres d'archivage de l'utilisateur est également recherchée. En outre, lorsque vous placez une conservation pour litige ou que vous appliquez une stratégie de rétention Office 365 à la boîte aux lettres d'un utilisateur, les éléments de la boîte aux lettres d'archivage sont également conservés.
  
- Une fois les boîtes aux lettres d'archivage activées, votre organisation peut tirer parti de la stratégie de rétention Exchange par défaut (également appelée gestion des enregistrements de messagerie ou stratégie MRM) qui est automatiquement affectée à chaque boîte aux lettres. Lorsqu'une boîte aux lettres d'archivage est activée, la stratégie de rétention Exchange par défaut effectue automatiquement les opérations suivantes: 
  
    - Elle déplace les éléments datant de deux ans ou plus de la boîte aux lettres principale d'un utilisateur à sa boîte aux lettres d'archivage. 
    
    - Elle déplace les éléments datant de 14 jours ou plus du dossier Éléments récupérables dans la boîte aux lettres principale de l'utilisateur vers le dossier Éléments récupérables dans la boîte aux lettres d'archivage.
    
- Pour plus d'informations sur les boîtes aux lettres d'archivage et les stratégies de rétention Exchange, voir:
    
  - [Balises et stratégies de rétention](https://go.microsoft.com/fwlink/?LinkId=404424)
    
  - [Stratégie de réTention par défaut dans Exchange Online](https://go.microsoft.com/fwlink/?linkid=839418)
    
  - [Configurer une stratégie d'archivage et de suppression pour les boîtes aux lettres de votre organisation Office 365](set-up-an-archive-and-deletion-policy-for-mailboxes.md)
