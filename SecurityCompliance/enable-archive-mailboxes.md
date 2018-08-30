---
title: Activer des boîtes aux lettres d’archive de sécurité Office 365 &amp; centre de conformité
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.ArchivingHelp
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 268a109e-7843-405b-bb3d-b9393b2342ce
description: Utilisez le Office 365 Security &amp; centre de conformité pour activer des boîtes aux lettres d’archive de prise en charge de la rétention des messages de votre organisation, eDiscovery, maintenir des exigences.
ms.openlocfilehash: 5ba578ba611f619194ac4f475121bd485b75f9e0
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528193"
---
# <a name="enable-archive-mailboxes-in-the-office-365-security-amp-compliance-center"></a>Activer des boîtes aux lettres d’archive de sécurité Office 365 &amp; centre de conformité
  
L’archivage dans Office 365 (également appelée In-Place Archiving) fournit aux utilisateurs d’espace de stockage des boîtes aux lettres supplémentaires. Une fois que vous allumez boîtes aux lettres d’archivage, les utilisateurs peuvent accéder et stocker des messages dans leurs boîtes aux lettres d’archivage à l’aide de Microsoft Outlook et les utilisateurs d’Outlook Web App peut également déplacer ou copier des messages entre leur boîte aux lettres principale et leur boîte aux lettres d’archive. Ils peuvent également récupérer des éléments supprimés à partir du dossier éléments récupérables dans leur boîte aux lettres d’archivage à l’aide de l’outil de récupérer les éléments supprimés. 
  
> [!TIP]
> Office 365 propose un nombre illimité de stockage d’archives avec la fonctionnalité d’archivage automatique en expansion. Lorsque développer automatiquement l’archivage est activé, puis le quota de stockage initiale dans la boîte aux lettres de l’utilisateur archive est atteint, Office 365 ajoute automatiquement espace de stockage supplémentaire. Cela signifie que les utilisateurs ne seront pas exécutés en dehors de l’espace de stockage de boîtes aux lettres et vous n’aurez pas à gérer les rien après avoir initialement activer la boîte aux lettres d’archive et activer l’archivage pour votre organisation développer automatiquement. Pour plus d’informations, voir [vue d’ensemble de l’archivage illimité dans Office 365](unlimited-archiving.md). 
  
## <a name="before-you-begin"></a>Avant de commencer

Vous devez être affecté le rôle destinataires de messagerie dans Exchange Online pour activer ou désactiver des boîtes aux lettres d’archive. Par défaut, ce rôle est attribué aux groupes de rôles gestion des destinataires et la gestion de l’organisation dans la page **autorisations** , dans le centre d’administration Exchange. Si vous ne voyez pas la page **d’Archive** dans la sécurité &amp; du centre de conformité, demandez à votre administrateur vous assignez les autorisations nécessaires. 
  
## <a name="enable-an-archive-mailbox"></a>Activation d'une boîte aux lettres d'archivage
  
1. Accédez à [https://protection.office.com](https://protection.office.com).
    
2. Connectez-vous à Office 365 à l’aide de votre compte professionnel ou de l’école.
    
3. Dans le volet gauche de la sécurité &amp; centre de conformité, cliquez sur **la gouvernance des données** \> **Archive**.
    
    La page **Archive** s’affiche. La colonne **Boîte aux lettres d’archivage** indique si une boîte aux lettres d’archivage est activée ou désactivée pour chaque utilisateur. 
    
4. Dans la liste des boîtes aux lettres, sélectionnez l’utilisateur pour lequel vous voulez activer la boîte aux lettres d’archivage.
    
    ![Cliquez sur Activer dans le volet de détails de l’utilisateur sélectionné pour activer la boîte aux lettres d’archive](media/8b53cdec-d5c9-4c28-af11-611f95c37b34.png)
  
5. Dans le volet de détails de l’utilisateur sélectionné, cliquez sur **Activer**. 
    
    Un avertissement s’affiche indiquant que si vous activez la boîte aux lettres d’archivage, les éléments de boîte aux lettres de l’utilisateur qui sont antérieurs à la stratégie d’archivage attribuée à la boîte aux lettres seront déplacées vers la nouvelle boîte aux lettres d’archive. La stratégie d’archivage par défaut qui fait partie de la stratégie de rétention affectée à des boîtes aux lettres Exchange Online déplace des éléments vers la boîte aux lettres d’archive deux ans après la date de l’élément a été remis à la boîte aux lettres ou créé par l’utilisateur. Pour plus d’informations, consultez la section **informations supplémentaires** dans cet article. 
    
6. Cliquez sur **Oui** pour activer la boîte aux lettres d’archivage. 
    
    Elle peut prendre quelques instants pour créer la boîte aux lettres d’archive. Lors de sa création, **boîte aux lettres d’Archive : activé** s’affiche dans le volet de détails de l’utilisateur sélectionné. Vous devrez peut-être cliquer sur **Actualiser** ![icône Actualiser](media/O365-MDM-Policy-RefreshIcon.gif) pour mettre à jour les informations contenues dans le volet de détails. 
    
> [!TIP]
> Vous pouvez également activer des boîtes aux lettres d’archivage en bloc en sélectionnant plusieurs utilisateurs dont les boîtes aux lettres sont désactivées (à l’aide de la touche Maj ou Ctrl). Une fois les boîtes aux lettres sélectionnées, cliquez sur **Activer** dans le volet des détails.  
  
## <a name="disable-an-archive-mailbox"></a>Désactiver une boîte aux lettres d'archivage
  
Vous pouvez également utiliser la page **Archive** dans la sécurité &amp; centre de conformité pour désactiver la boîte aux lettres de l’utilisateur archive. Une fois que vous avez désactivé une boîte aux lettres d’archivage, vous pouvez vous reconnecter à la boîte aux lettres principale de l’utilisateur dans les 30 jours de le désactiver. Dans ce cas, le contenu d’origine de la boîte aux lettres d’archivage est restauré. Après 30 jours, le contenu de la boîte aux lettres d’archive d’origine est supprimé définitivement et ne peuvent pas être récupéré. Si vous réactivez l’archive plus de 30 jours après l’avoir désactivé, une nouvelle boîte aux lettres d’archive est créé. 
  
Notez que la stratégie d’archivage par défaut attribué aux boîtes aux lettres des utilisateurs déplace les éléments dans la boîte aux lettres d’archive deux ans après la date de l’élément est remis. Si vous désactivez les boîtes aux lettres de l’utilisateur archive, aucune action ne sera entreprise sur les éléments de boîte aux lettres et qu’ils restent dans la boîte aux lettres principale de l’utilisateur.
  
Pour désactiver une boîte aux lettres d’archivage :
  
1. Accédez à [https://protection.office.com](https://protection.office.com).
    
2. Connectez-vous à Office 365 à l’aide de votre compte professionnel ou de l’école.
    
3. Dans le volet gauche de la sécurité &amp; centre de conformité, cliquez sur **la gouvernance des données** \> **Archive**.
    
    La page **Archive** s’affiche. La colonne **Boîte aux lettres d’archivage** indique si une boîte aux lettres d’archivage est activée ou désactivée pour chaque utilisateur. 
    
4. Dans la liste des boîtes aux lettres, sélectionnez l’utilisateur pour lequel vous voulez désactiver la boîte aux lettres d’archivage.
    
5. Dans le volet des détails, cliquez sur **Désactiver**. 
    
    Un message d’avertissement s’affiche indiquant que vous aurez 30 jours pour réactiver la boîte aux lettres d’archivage et qu’après 30 jours, toutes les informations dans l’archive seront définitivement supprimées. 
    
6. Cliquez sur **Oui** pour désactiver la boîte aux lettres d’archivage. 
    
    Elle peut prendre quelques instants pour désactiver la boîte aux lettres d’archive. Lorsqu’il est désactivé, **boîte aux lettres d’Archive : désactivé** s’affiche dans le volet de détails de l’utilisateur sélectionné. Vous devrez peut-être cliquer sur **Actualiser** ![icône Actualiser](media/O365-MDM-Policy-RefreshIcon.gif) pour mettre à jour les informations contenues dans le volet de détails. 
    
> [!TIP]
> Vous pouvez également désactiver des boîtes aux lettres d’archivage en bloc en sélectionnant plusieurs utilisateurs dont les boîtes aux lettres sont activées (à l’aide de la touche Maj ou Ctrl). Une fois les boîtes aux lettres sélectionnées, cliquez sur **Désactiver** dans le volet des détails.  
  
## <a name="more-information"></a>Plus d'informations
  
- Boîtes aux lettres d’archive aider à vous et vos utilisateurs pour répondre à la rétention de votre organisation, eDiscovery et maintenez la configuration requise. Par exemple, vous pouvez utiliser la stratégie de rétention de votre organisation Exchange pour déplacer le contenu de la boîte aux lettres boîte aux lettres d’archivage des utilisateurs. Lorsque vous utilisez l’outil de recherche de contenu dans la sécurité &amp; centre de conformité pour rechercher les boîtes aux lettres d’un utilisateur pour un contenu spécifique, boîte aux lettres de l’utilisateur archive sera également recherché. Et, lorsque vous placez un litige ou appliquez une stratégie de rétention Office 365 pour les boîtes aux lettres d’un utilisateur, les éléments dans la boîte aux lettres d’archivage sont également conservées.
  
- Lorsqu’une boîte aux lettres d’archive est activé, les utilisateurs peuvent stocker des messages dans leur boîte aux lettres d’archive. Les utilisateurs peuvent accéder leurs boîtes aux lettres d’archivage à l’aide de Microsoft Outlook et Outlook Web App en utilisant une de ces applications clientes, les utilisateurs peuvent afficher les messages dans leur boîte aux lettres d’archivage et de déplacer ou copier des messages entre leur boîte aux lettres principale et leur boîte aux lettres d’archive. Les utilisateurs peuvent également récupérer les éléments supprimés du dossier éléments récupérables dans leur boîte aux lettres d’archive à l’aide de l’outil de récupérer les éléments supprimés. 
  
- Une fois l’archivage de boîtes aux lettres sont activées, votre organisation peut tirer parti de la stratégie par défaut Exchange rétention (également appelée stratégie de gestion des enregistrements de messagerie ou MRM) qui est automatiquement attribuée à chaque boîte aux lettres. Lorsqu’une boîte aux lettres d’archive est activé, la stratégie de rétention par défaut Exchange automatiquement les opérations suivantes : 
  
    - Elle déplace les éléments datant de deux ans ou plus de la boîte aux lettres principale d'un utilisateur à sa boîte aux lettres d'archivage. 
    
    - Elle déplace les éléments datant de 14 jours ou plus du dossier Éléments récupérables dans la boîte aux lettres principale de l'utilisateur vers le dossier Éléments récupérables dans la boîte aux lettres d'archivage.
    
- Pour plus d’informations sur les boîtes aux lettres d’archive et des stratégies de rétention d’Exchange, voir :
  
  - [Boîtes aux lettres d'archivage dans Exchange Online](https://go.microsoft.com/fwlink/?LinkId=404421)
    
  - [Balises et stratégies de rétention](https://go.microsoft.com/fwlink/?LinkId=404424)
    
  - [Valeur par défaut de la stratégie de rétention dans Exchange Online](https://go.microsoft.com/fwlink/?linkid=839418)
    
  - [Configurer une stratégie d’archivage et de suppression des boîtes aux lettres dans votre organisation Office 365](set-up-an-archive-and-deletion-policy-for-mailboxes.md)
