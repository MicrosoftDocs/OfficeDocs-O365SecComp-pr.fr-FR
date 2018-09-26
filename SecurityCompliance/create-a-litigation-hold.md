---
title: Créer un litige dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 3/13/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MET150
ms.assetid: 39db1659-0b12-4243-a21c-2614512dcb44
ms.openlocfilehash: aa78d12046108aa1f1b974f01c02ff923b99b97b
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25037957"
---
# <a name="create-a-litigation-hold-in-office-365"></a>Créer un litige dans Office 365

Vous pouvez placer une boîte aux lettres en conservation pour litige à conserver tous les contenus de boîte aux lettres, notamment les éléments supprimés et les versions d’origine d’éléments modifiés. Lorsque vous placez une boîte aux lettres utilisateur litige, contenu dans la boîte aux lettres de l’utilisateur archive (si elle est activée) est également conservé. Lorsque vous créez une suspension, vous pouvez spécifier une durée d’attente (également appelée une *archive temporaire*) afin que supprimés et les éléments modifiés sont conservés pendant une période spécifiée et suppression définitive de la boîte aux lettres. Ou vous pouvez simplement conserver le contenu indéfiniment (appelé une *attente infinie*) ou jusqu'à ce que le litige est supprimé. Si vous ne spécifiez pas une durée de suspension, il est calculée à partir de la date de réception d’un message ou un élément de boîte aux lettres est créé. 
  
C’est ici que se passe-t-il lorsque vous créez un litige.
  
- Éléments sont définitivement supprimés par l’utilisateur sont conservées dans le dossier éléments récupérables de boîte aux lettres de l’utilisateur pendant la durée de la suspension.
    
- Les éléments qui sont supprimés du dossier éléments récupérables par l’utilisateur sont conservés pendant la durée de la suspension.
    
- Le quota de stockage pour le dossier éléments récupérables est passent de 30 Go à 110 Go.
    
- Éléments de principal de l’utilisateur et les boîtes aux lettres d’archivage sont conservés.
    
## <a name="before-you-begin"></a>Avant de commencer

- Pour placer une boîte aux lettres Exchange Online litige, il doit être attribué une licence Exchange Online Plan 2. Si une boîte aux lettres est attribué une licence Exchange Online Plan 1, vous devrez affecter maintenez une licence séparée de l’archivage Exchange Online à placer dans.
    

## <a name="place-a-mailbox-on-litigation-hold-in-the-office-365-admin-center"></a>Placer une boîte aux lettres en conservation pour litige dans le centre d’administration d’Office 365

Voici les étapes pour placer une boîtes aux lettres en conservation pour litige utilisant le centre d’administration Office 365.

1. Accédez à https://portal.office.com/adminportal/home et connectez-vous à l’aide de votre compte d’administrateur global.
2. Cliquez sur **utilisateurs** > **utilisateurs actifs** dans le volet de navigation de gauche.
3. Sélectionnez l’utilisateur de boîte aux lettres que vous souhaitez mettre en attente pour litige.
4. Dans la page volants, cliquez sur **paramètres de messagerie**, puis cliquez sur **Modifier** en regard de **litige**.
5. Dans la page **litige** , cliquez sur le bouton pour activer litige et effectuer les paramètres facultatifs suivants qui sont affichent :
 
    ![O365_LitigationHold1.png](media/O365-LitigationHold1.png)

    a **durée de suspension (jours)** -Utilisez cette boîte pour créer une suspension basé sur le temps et spécifier la durée de conservation des éléments de boîte aux lettres lors de la boîte aux lettres est mis en attente pour litige. La durée est calculée à partir de la date d’un élément de boîte aux lettres est reçu ou créé. Si vous laissez ce champ vide, les éléments sont conservés indéfiniment ou jusqu'à ce que le blocage est supprimé. Jours permet de spécifier la durée.
    
    b. **Remarque** - Utilisez cette boîte pour informer l’utilisateur à leur boîte aux lettres est litige. La note apparaît dans la page informations de compte dans la boîte aux lettres de l’utilisateur s’il utilise Outlook 2010 ou version ultérieure. Pour accéder à cette page, les utilisateurs peuvent cliquer sur le **fichier** dans Outlook.
     
    c. **page Web** - Utilisez cette boîte pour diriger l’utilisateur vers un site Web pour plus d’informations sur le litige. Cette URL apparaît dans la page informations de compte dans la boîte aux lettres de l’utilisateur s’ils utilisent Outlook 2010 ou version ultérieure. Pour accéder à cette page, les utilisateurs peuvent cliquer sur le **fichier** dans Outlook.
 
6. Cliquez sur **Enregistrer** pour créer le litige.

Après avoir créé la suspension, les paramètres de messagerie dans la page volants montre que litige est activé pour l’utilisateur sélectionné.

![O365_LitigationHold2.png](media/O365-LitigationHold2.png)

Pour plus d’informations sur la création et la gestion des suspensions en cas de litige et à l’aide d’Exchange Online PowerShell pour litige contient création en bloc, voir [archive une boîte aux lettres en conservation pour litige](https://docs.microsoft.com/office365/SecurityCompliance/place-a-mailbox-on-litigation-hold).
