---
title: Créer une suspension pour litige dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 3/13/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: MET150
ms.assetid: 39db1659-0b12-4243-a21c-2614512dcb44
ms.openlocfilehash: f2d3793eac84e8f80158842c833c30986b0549c5
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218654"
---
# <a name="create-a-litigation-hold-in-office-365"></a>Créer une suspension pour litige dans Office 365

Vous pouvez placer une boîte aux lettres en conservation pour litige pour conserver tout le contenu des boîtes aux lettres, y compris les éléments supprimés et les versions d'origine des éléments modifiés. Lorsque vous placez une boîte aux lettres utilisateur en conservation pour litige, le contenu de la boîte aux lettres d'archivage de l'utilisateur (si elle est activée) est également conservé. Lorsque vous créez une suspension, vous pouvez spécifier une durée de conservation (également appelée *conservation basée sur l'heure*) afin que les éléments supprimés et modifiés soient conservés pendant une période spécifiée, puis supprimés définitivement de la boîte aux lettres. Vous pouvez également conserver indéfiniment le contenu (appelé *conservation*infinie) ou jusqu'à ce que la conservation pour litige ne soit supprimée. Si vous spécifiez une période de durée de blocage, elle est calculée à partir de la date de réception d'un message ou de la création d'un élément de boîte aux lettres. 
  
Voici ce qui se passe lorsque vous créez une suspension pour litige.
  
- Les éléments définitivement supprimés par l'utilisateur sont conservés dans le dossier éléments récupérables de la boîte aux lettres de l'utilisateur pendant la durée de la conservation.
    
- Les éléments purgés du dossier éléments récupérables par l'utilisateur sont conservés pendant la durée de la conservation.
    
- Le quota de stockage pour le dossier éléments récupérables est passé de 30 Go à 110 Go.
    
- Les éléments dans les boîtes aux lettres principale et d'archivage de l'utilisateur sont conservés
    
## <a name="before-you-begin"></a>Avant de commencer

- Pour placer une boîte aux lettres Exchange Online en conservation pour litige, une licence Exchange Online plan 2 doit lui être attribuée. Si une licence Exchange Online plan 1 est attribuée à une boîte aux lettres, vous devez lui attribuer une licence d'archivage Exchange Online distincte pour la mettre en attente.
    

## <a name="place-a-mailbox-on-litigation-hold-in-the-office-365-admin-center"></a>Placer une boîte aux lettres en conservation pour litige dans le centre d'administration Office 365

Voici les étapes à suivre pour placer un maibox en conservation pour litige à l'aide du centre d'administration Office 365.

1. Accédez à https://portal.office.com/adminportal/home et connectez-vous à l'aide de votre compte d'administrateur général.
2. Cliquez sur utilisateurs**actifs** dans le volet de navigation de gauche. **** > 
3. Sélectionnez l'utilisateur dont vous souhaitez placer la boîte aux lettres en conservation pour litige.
4. Sur la page de survol, cliquez sur **paramètres de messagerie**, puis cliquez sur **modifier** en regard de **conservation pour litige**.
5. Sur la page **conservation pour litige** , cliquez sur le bouton bascule pour activer la conservation pour litige et renseignez les paramètres facultatifs suivants qui sont affichés:
 
    ![O365_LitigationHold1. png](media/O365-LitigationHold1.png)

    a. **Hold durée (jours)** : cette zone permet de créer une conservation basée sur le temps et de spécifier la durée pendant laquelle les éléments de boîte aux lettres sont conservés lorsque la boîte aux lettres est placée en conservation pour litige. La durée est calculée à partir de la date de réception ou de création d'un élément de boîte aux lettres. Si vous laissez cette zone vide, les éléments sont conservés indéfiniment ou jusqu'à ce que la conservation soit supprimée. Utilisez l'intervalle jours pour spécifier la durée.
    
    b. **note** : cette zone permet d'informer l'utilisateur que sa boîte aux lettres est en conservation pour litige. La note apparaît sur la page informations sur le compte dans la boîte aux lettres de l'utilisateur si elle utilise Outlook 2010 ou une version ultérieure. Pour accéder à cette page, les utilisateurs peuvent cliquer sur **fichier** dans Outlook.
     
    c. **page Web** : utilisez cette zone pour diriger l'utilisateur vers un site Web pour obtenir plus d'informations sur la conservation pour litige. Cette URL apparaît sur la page informations sur le compte dans la boîte aux lettres de l'utilisateur, si elle utilise Outlook 2010 ou une version ultérieure. Pour accéder à cette page, les utilisateurs peuvent cliquer sur **fichier** dans Outlook.
 
6. Cliquez sur **Enregistrer** pour créer la conservation pour litige.

Une fois la conservation créée, les paramètres de messagerie de la page de survol indiquent que la conservation pour litige est activée pour l'utilisateur sélectionné.

![O365_LitigationHold2. png](media/O365-LitigationHold2.png)

Pour plus d'informations sur la création et la gestion des conservations pour litige et sur l'utilisation d'Exchange Online PowerShell pour créer en bloc des conservations pour litige, consultez [la rubrique placer une boîte aux lettres en conservation pour litige](https://docs.microsoft.com/office365/SecurityCompliance/place-a-mailbox-on-litigation-hold).
