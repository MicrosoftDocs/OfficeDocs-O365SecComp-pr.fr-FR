---
title: Activer des boîtes aux lettres d’archivage dans le Centre de sécurité et conformité
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
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
description: Utilisez le Centre de sécurité et conformité dans Office 365 pour activer des boîtes aux lettres d’archivage afin de vous conformer aux exigences de votre organisation en matière de rétention, d’eDiscovery et de conservation des messages.
ms.openlocfilehash: 5cf399b311b6c342aff2d84477edaa945f8e0cd4
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34153286"
---
# <a name="enable-archive-mailboxes-in-the-security--compliance-center"></a>Activer des boîtes aux lettres d’archivage dans le Centre de sécurité et conformité
  
L’archivage dans Office 365 (également appelé archivage inaltérable) fournit aux utilisateurs de l’espace de stockage de boîtes aux lettres supplémentaire. Une fois que vous avez activé les boîtes aux lettres d’archivage, les utilisateurs peuvent consulter et stocker des messages dans leurs boîtes aux lettres d’archivage à l’aide de Microsoft Outlook et d’Outlook sur le web (autrefois appelé Outlook Web App). Les utilisateurs peuvent également déplacer ou copier des messages entre leurs boîtes aux lettres principale et d’archivage. Ils peuvent également récupérer les éléments supprimés du dossier Éléments récupérables dans leur boîte aux lettres d’archivage à l’aide de l’outil Récupérer les éléments supprimés. 
  
> [!TIP]
> Office 365 offre une quantité illimitée d’espace de stockage d’archivage avec la fonctionnalité d’archivage à développement automatique. Lorsque l’archivage à développement automatique est activé et que le quota de stockage initial de la boîte aux lettres d’archivage d’un utilisateur est atteint, Office 365 ajoute automatiquement un espace de stockage supplémentaire. Cela signifie que les utilisateurs ne tombent pas à cours d’espace de stockage de boîte aux lettres et que vous n’avez plus besoin de gérer quoi que ce soit après l’activation initiale de la boîte aux lettres d’archivage et de l’archivage à développement automatique pour votre organisation. Pour plus d’informations, voir [Vue d’ensemble d’un archivage illimité dans Office 365](unlimited-archiving.md). 
  
## <a name="before-you-begin"></a>Avant de commencer

Pour activer ou désactiver les boîtes aux lettres d’archivage, vous devez être affecté au rôle Destinataires du courrier dans Exchange Online. Par défaut, ce rôle est attribué aux groupes de rôles Gestion des destinataires et Gestion de l’organisation sur la page **Autorisations** du Centre d’administration Exchange. Si la page **Archive** n’apparaît pas dans le Centre de sécurité et conformité, demandez à votre administrateur de vous attribuer les autorisations nécessaires. 
  
## <a name="enable-an-archive-mailbox"></a>Activer une boîte aux lettres d’archivage
  
1. Accédez à [https://protection.office.com](https://protection.office.com).
    
2. Ouvrez une session Office 365 en utilisant votre compte scolaire ou professionnel.
    
3. Dans le volet gauche du Centre de sécurité et conformité, cliquez sur **Gouvernance des données** \> **Archive**.
    
    La **page** Archive s’affiche. La colonne **Boîte aux lettres d’archivage** indique si une boîte aux lettres d’archivage est activée ou désactivée pour chaque utilisateur. 
    
4. Dans la liste des boîtes aux lettres, sélectionnez l’utilisateur pour lequel vous voulez activer la boîte aux lettres d’archivage.
    
    ![Cliquer sur Activer dans le volet d’informations de l’utilisateur sélectionné pour activer la boîte aux lettres d’archivage](media/8b53cdec-d5c9-4c28-af11-611f95c37b34.png)
  
5. Dans le volet d’informations de l’utilisateur sélectionné, cliquez sur **Activer**. 
    
    Un avertissement s’affiche, qui vous signale que, si vous activez la boîte aux lettres d’archivage, les éléments de la boîte aux lettres de l’utilisateur plus anciens que la stratégie d’archivage affectée à la boîte aux lettres seront déplacés vers la nouvelle boîte aux lettres d’archivage. La stratégie d’archivage par défaut qui fait partie de la stratégie de rétention affectée aux boîtes aux lettres Online déplace les éléments vers la boîte aux lettres d’archivage deux ans après la date à laquelle ils ont été remis à la boîte aux lettres ou créés par l’utilisateur. Pour plus d’informations, voir la section **Plus d’informations** de cet article. 
    
6. Cliquez sur **Oui** pour activer la boîte aux lettres d’archivage. 
    
    La création de la boîte aux lettres d’archivage peut prendre un certain temps. Une fois la boîte aux lettres d’archivage créée, l’indication **Boîte aux lettres d’archivage : Activée** s’affiche dans le volet d’informations pour l’utilisateur sélectionné. Il sera peut-être nécessaire de cliquer sur **Actualiser** ![icône Actualiser](media/O365-MDM-Policy-RefreshIcon.gif) pour mettre à jour les informations dans le volet d’informations. 
    
> [!TIP]
> Vous pouvez également activer des boîtes aux lettres d’archivage en bloc en sélectionnant plusieurs utilisateurs dont les boîtes aux lettres sont désactivées (à l’aide de la touche Maj ou Ctrl). Une fois les boîtes aux lettres sélectionnées, cliquez sur **Activer** dans le volet des détails. 
  
## <a name="disable-an-archive-mailbox"></a>Désactiver une boîte aux lettres d’archivage
  
Vous pouvez également utiliser la page **Archive** dans le Centre de sécurité et conformité pour désactiver la boîte aux lettres d’archivage d’un utilisateur. Si vous désactivez la boîte aux lettres d’un utilisateur, vous pouvez la reconnecter à la boîte aux lettres principale de l’utilisateur dans les 30 jours qui suivent sa désactivation. Dans ce cas, le contenu d’origine de la boîte aux lettres d’archivage est restauré. Au bout de 30 jours, le contenu de la boîte aux lettres d’archivage d’origine est supprimé définitivement et ne peut pas être récupéré. Par conséquent, si vous réactivez l’archive plus de 30 jours après l’avoir désactivée, une nouvelle boîte aux lettres d’archivage est créée. 
  
Notez que la stratégie d’archivage par défaut affectée aux boîtes aux lettres des utilisateurs déplace les éléments vers la boîte aux lettres d’archivage deux ans après leur date de remise. Si vous désactivez la boîte aux lettres d’archivage d’un utilisateur, aucune action n’est effectuée sur les éléments de boîte aux lettres et ceux-ci restent dans la boîte aux lettres principale de l’utilisateur.
  
Pour désactiver une boîte aux lettres d’archivage :
  
1. Accédez à [https://protection.office.com](https://protection.office.com).
    
2. Ouvrez une session Office 365 en utilisant votre compte scolaire ou professionnel.
    
3. Dans le volet gauche du Centre de sécurité et conformité, cliquez sur **Gouvernance des données** \> **Archive**.
    
    La page **Archive** s’affiche. La colonne **Boîte aux lettres d’archivage** indique si une boîte aux lettres d’archivage est activée ou désactivée pour chaque utilisateur. 
    
4. Dans la liste des boîtes aux lettres, sélectionnez l’utilisateur pour lequel vous voulez désactiver la boîte aux lettres d’archivage.
    
5. Dans le volet des détails, cliquez sur **Désactiver**. 
    
    Un message d’avertissement s’affiche, indiquant que vous avez 30 jours pour réactiver la boîte aux lettres d’archivage et qu’à l’issue de ce délai, toutes les informations contenues dans l’archive seront définitivement supprimées. 
    
6. Cliquez sur **Oui** pour désactiver la boîte aux lettres d’archivage. 
    
    La désactivation de la boîte aux lettres d’archivage peut prendre un certain temps. Une fois la boîte aux lettres d’archivage désactivée, l’indication **Boîte aux lettres d’archivage : Désactivée** s’affiche dans le volet d’informations pour l’utilisateur sélectionné. Il sera peut-être nécessaire de cliquer sur **Actualiser** ![icône Actualiser](media/O365-MDM-Policy-RefreshIcon.gif) pour mettre à jour les informations dans le volet d’informations. 
    
> [!TIP]
> Vous pouvez également désactiver des boîtes aux lettres d’archivage en bloc en sélectionnant plusieurs utilisateurs dont les boîtes aux lettres sont activées (à l’aide de la touche Maj ou Ctrl). Une fois les boîtes aux lettres sélectionnées, cliquez sur **Désactiver** dans le volet des détails. 
  
## <a name="use-exchange-online-powershell-to-enable-or-disable-archive-mailboxes"></a>Utiliser Exchange Online PowerShell pour activer ou désactiver les boîtes aux lettres d’archivage

Vous pouvez également utiliser Exchange Online PowerShell pour activer les boîtes aux lettres d’archivage. La principale raison d’utiliser PowerShell est que vous pouvez activer rapidement la boîte aux lettres d’archivage pour tous les utilisateurs au sein de votre organisation.

La première étape consiste à se connecter à Exchange Online PowerShell. Pour obtenir des instructions, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).

Une fois que vous êtes connecté à Exchange Online, vous pouvez exécuter les commandes décrites dans les sections suivantes pour activer ou désactiver les boîtes aux lettres d’archivage.

### <a name="enable-archive-mailboxes"></a>Activer les boîtes aux lettres d’archivage

Pour activer la boîte aux lettres d’archivage pour un seul utilisateur, exécutez la commande suivante.
    
  ```
  Enable-Mailbox -Identity <username> -Archive
  ```

Pour activer la boîte aux lettres d’archivage pour tous les utilisateurs au sein de votre organisation (dont la boîte aux lettres d’archivage n’est pas activée), exécutez la commande suivante.
    
  ```
  Get-Mailbox -Filter {ArchiveStatus -Eq "None" -AND RecipientTypeDetails -eq "UserMailbox"} | Enable-Mailbox -Archive
  ```
  
### <a name="disable-archive-mailboxes"></a>Désactiver les boîtes aux lettres d’archivage

Pour désactiver la boîte aux lettres d’archivage pour un seul utilisateur, exécutez la commande suivante.
    
  ```
  Disable-Mailbox -Identity <username> -Archive
  ```

Pour désactiver la boîte aux lettres d’archivage pour tous les utilisateurs au sein de votre organisation (dont la boîte aux lettres d’archivage est activée), exécutez la commande suivante.
    
  ```
  Get-Mailbox -Filter {ArchiveStatus -Eq "Active" -AND RecipientTypeDetails -eq "UserMailbox"} | Disable-Mailbox -Archive
  ```

## <a name="more-information"></a>Plus d’informations
  
- Quand une boîte aux lettres d’archivage est activé, les utilisateurs peuvent y stocker des messages. Les utilisateurs peuvent accéder à leur boîte aux lettres d’archivage à l’aide de Microsoft Outlook et d’Outlook sur le web. À l’aide de l’une de ces applications clientes, les utilisateurs peuvent afficher les messages dans leur boîte aux lettres d’archivage et déplacer ou copier des messages entre leur boîte aux lettres principale et la boîte aux lettres d’archivage. Les utilisateurs peuvent également récupérer les éléments supprimés du dossier Éléments récupérables dans leur boîte aux lettres d’archivage à l’aide de l’outil de récupération des éléments supprimés.

   Pour obtenir la liste des licences Outlook qui prennent en charge l’archivage inaltérable, voir [Conditions de licence Outlook requises pour les fonctionnalités Exchange](https://support.office.com/article/outlook-license-requirements-for-exchange-features-46b6b7c5-c3ca-43e5-8424-1e2807917c99).

- Les boîtes aux lettres d’archivage vous aident à répondre aux exigences de rétention, d’eDiscovery et de conservation des messages de votre organisation. Par exemple, vous pouvez utiliser la stratégie de rétention Exchange de votre organisation pour déplacer le contenu de boîtes aux lettres vers la boîte aux lettres d’archivage des utilisateurs. Lorsque vous utilisez l’outil Recherche de contenu dans le Centre de sécurité et conformité pour effectuer rechercher un contenu spécifique dans la boîte aux lettres d’un utilisateur, la boîte aux lettres d’archivage de celui-ci est également incluse dans le processus. Lorsque vous définissez une Conservation pour litige ou appliquez une stratégie de rétention Office 365 à la boîte aux lettres d’un utilisateur, les éléments contenus dans la boîte aux lettres d’archivage sont également conservés.
  
- Lorsque les boîtes aux lettres d’archivage sont activées, votre organisation peut tirer parti de la stratégie de rétention par défaut Exchange (également appelée stratégie de Gestion des enregistrements de messagerie ou MRM) automatiquement affectée à chaque boîte aux lettres. Quand une boîte aux lettres d’archivage est activée, la stratégie de rétention par défaut Exchange effectue automatiquement les opérations suivantes : 
  
    - Elle déplace les éléments datant de deux ans ou plus de la boîte aux lettres principale d’un utilisateur à sa boîte aux lettres d’archivage. 
    
    - Elle déplace les éléments datant de 14 jours ou plus du dossier Éléments récupérables dans la boîte aux lettres principale de l’utilisateur vers le dossier Éléments récupérables dans la boîte aux lettres d’archivage.
    
- Pour plus d’informations sur les boîtes aux lettres d’archivage et les stratégies de rétention Exchange, voir:
    
  - [Balises et stratégies de rétention](https://go.microsoft.com/fwlink/?LinkId=404424)
    
  - [Stratégie de rétention par défaut dans Exchange Online](https://go.microsoft.com/fwlink/?linkid=839418)
    
  - [Configurer une stratégie d’archivage et de suppression pour les boîtes aux lettres de votre organisation Office 365](set-up-an-archive-and-deletion-policy-for-mailboxes.md)
