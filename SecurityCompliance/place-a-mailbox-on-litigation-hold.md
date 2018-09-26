---
title: Placement d'une boîte aux lettres en conservation pour litige
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/18/2016
ms.audience: End User
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid: ''
ms.assetid: adee4621-3626-4aec-aa53-00b35ff0d0b0
description: 'Vous pouvez placer une boîte aux lettres en conservation pour litige pour conserver tout le contenu de la boîte aux lettres, y compris les éléments supprimés et les versions originales des éléments modifiés. '
ms.openlocfilehash: 00f83d69d90f10659427986ffcb16f9e5358c054
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038037"
---
# <a name="place-a-mailbox-on-litigation-hold"></a>Placement d'une boîte aux lettres en conservation pour litige
 
Vous pouvez placer une boîte aux lettres en conservation pour litige pour conserver tout le contenu de la boîte aux lettres, y compris les éléments supprimés et les versions originales des éléments modifiés. Lorsque vous placez une conservation pour litige sur la boîte aux lettres d’un utilisateur, le contenu de la boîte aux lettres d’archivage de l’utilisateur (si elle est activée) est également placé en conservation. Les éléments supprimés et modifiés sont conservés pendant une période déterminée, ou jusqu’à ce que vous supprimiez la boîte aux lettres de la conservation pour litige. Tous ces éléments de boîte aux lettres sont renvoyés dans une recherche de [In-Place eDiscovery](http://technet.microsoft.com/library/6377cb7a-3416-4e15-8571-c45d2160fc6f.aspx). 
  
> [!IMPORTANT]
> Blocage pour litige conserve les éléments du dossier éléments récupérables dans la boîte aux lettres de l’utilisateur. Selon le nombre et la taille des éléments supprimés ou modifiés, la taille du dossier éléments récupérables de la boîte aux lettres peut augmenter rapidement. Le dossier éléments récupérables est configuré avec un haute quota par défaut. Dans Exchange Online, ce quota est augmenté automatiquement lorsque vous placez une boîte aux lettres en conservation pour litige. Dans Exchange Server 2013, nous vous recommandons d’analyser les boîtes aux lettres qui sont mis en attente pour litige hebdomadaires pour s’assurer qu’ils n’atteignent les limites des quotas éléments récupérables. 
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>Ce qu'il faut savoir avant de commencer
<a name="sectionSection0"> </a>

- Durée d’exécution estimée : 5 minutes
    
- Il se peut que vous deviez attendre 60 minutes avant que le paramètre Conservation pour litige ne soit actif.
    
- Des autorisations doivent vous être attribuées avant de pouvoir exécuter cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez l'entrée « Conservation inaltérable » dans la rubrique [Stratégie de messagerie et autorisations de conformité](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx). 
    
- Pour placer une boîte aux lettres Exchange Online litige, il doit être attribué une licence Exchange Online (Plan 2). Si une boîte aux lettres est attribué une licence Exchange Online (Plan 1), vous devrez affecter maintenez une licence séparée de l’archivage Exchange Online à placer dans.
    
- Comme expliqué précédemment, lorsque vous placez un litige sur boîte aux lettres d’un utilisateur, le contenu de la boîte aux lettres de l’utilisateur archive est également mis en attente. Si vous placez un litige sur une boîte aux lettres principale locale dans un déploiement Exchange hybride, la boîte aux lettres de l’archive en nuage (si activée) est également mis en attente.
    
- Dans Exchange Online, le quota du dossier éléments récupérables est augmenté à 100 Go lorsque vous placez une boîte aux lettres en conservation pour litige. La taille par défaut de ce dossier est de 30 Go.
    
- Blocage pour litige conserve les éléments supprimés et conserve également les versions originales d’éléments modifiés jusqu'à ce que le blocage est supprimé. Vous pouvez éventuellement spécifier une durée de la suspension, qui conserve un élément de boîte aux lettres pendant la durée spécifiée. Si vous spécifiez une durée d’attente, elle est calculée à partir de la date de réception d’un message ou un élément de boîte aux lettres est créé. Pour conserver les éléments qui répondent aux critères spécifiés, utilisez an In-Place Hold pour créer une suspension basée sur une requête. Pour plus d’informations, voir [créer ou supprimer un In-Place Hold](http://technet.microsoft.com/library/9d5d8d37-a053-4830-9cb1-6e1ede25e963.aspx).
    
- Pour utiliser le Shell pour placer une boîte aux lettres Exchange Online en attente, vous devez utiliser Exchange Online PowerShell. Pour plus d’informations, voir [se connecter à Exchange Online à l’aide de Remote PowerShell](http://technet.microsoft.com/library/c8bea338-6c1a-4bdf-8de0-7895d427ee5b.aspx).
    
- Le placement d’une boîte aux lettres de dossier public en conservation pour litige n’est pas pris en charge. Vous devez utiliser la conservation inaltérable pour placer des dossiers publics en conservation.
    
## <a name="use-the-eac-to-place-a-mailbox-on-litigation-hold"></a>Utilisation du Centre d'administration Exchange pour mettre une boîte aux lettres en conservation pour litige
<a name="sectionSection1"> </a>

1. Accédez à **Destinataires**\> **Boîtes aux lettres**.
    
2. Dans la liste des boîtes aux lettres utilisateur, cliquez sur la boîte aux lettres que vous souhaitez mettre en attente pour litige, puis cliquez sur **Modifier** ![icône Modifier](media/ITPro-EAC-EditIcon.gif).
    
3. Dans la page Propriétés de boîte aux lettres, cliquez sur **les fonctionnalités de boîte aux lettres.**
    
4. Sous **Conservation pour litige : désactivée**, cliquez sur **Activer** pour mettre la boîte aux lettres en conservation pour litige. 
    
5. Sur la page **Conservation pour litige**, entrez les informations facultatives suivantes : 
    
  - **Durée de conservation pour litige (en nombre de jours)** Cette zone permet de spécifier la durée de conservation des éléments de boîte aux lettres lorsque la boîte aux lettres est conservée pour litige. La durée est calculée à compter de la date de réception ou de création de l'élément de boîte aux lettres. Si vous laissez cette zone vide, les éléments sont conservés indéfiniment ou jusqu'à ce que la conservation soit annulée. Indiquez la période en nombre de jours. 
    
  - **Remarque** Utilisez cette boîte pour informer l’utilisateur à que leur boîte aux lettres est litige. La note apparaît dans la boîte aux lettres de l’utilisateur si ils utilisent Outlook 2010 ou version ultérieure. 
    
  - **URL** Utilisez cette boîte pour diriger l’utilisateur vers un site Web pour plus d’informations sur le litige. Cette URL apparaît dans la boîte aux lettres de l’utilisateur s’ils utilisent Outlook 2010 ou version ultérieure. 
    
6. Cliquez sur **Enregistrer** sur la page **Conservation pour litige**, puis cliquez sur **Enregistrer** sur la page des propriétés de boîte aux lettres. 
  
## <a name="use-the-shell-to-place-a-mailbox-on-litigation-hold-indefinitely"></a>Utilisation de l’environnement de ligne de commande Exchange Management Shell pour mettre une boîte aux lettres en conservation pour litige indéfiniment
<a name="sectionSection2"> </a>

Dans cet exemple, la boîte aux lettres bsuneja@contoso.com est placée en conservation pour litige. Les éléments de la boîte aux lettres sont conservés indéfiniment ou jusqu'à ce que la conservation soit supprimée.
  
```
Set-Mailbox bsuneja@contoso.com -LitigationHoldEnabled $true
```

> [!NOTE]
> Lorsque vous placez une boîte aux lettres en conservation pour litige indéfiniment (en ne spécifiant aucune durée), la valeur de la propriété de boîte aux lettres  _LitigationHoldDuration_ est définie sur  `Unlimited`. 
  
## <a name="use-the-shell-to-place-a-mailbox-on-litigation-hold-and-preserve-items-for-a-specified-duration"></a>Utilisation de l’environnement de ligne de commande Exchange Management Shell pour placer une boîte aux lettres en conservation pour litige et conserver les éléments pour une durée spécifiée
<a name="sectionSection3"> </a>

Dans cet exemple, la boîte aux lettres bsuneja@contoso.com est placée en conservation pour litige et les éléments sont conservés pendant 2 555 jours (environ 7 ans). 
  
```
Set-Mailbox bsuneja@contoso.com -LitigationHoldEnabled $true -LitigationHoldDuration 2555
```

## <a name="use-the-shell-to-place-all-mailboxes-on-litigation-hold-for-a-specified-duration"></a>Utilisation de l’environnement de ligne de commande Exchange Management Shell pour placer toutes les boîtes aux lettres en conservation pour litige pour une durée spécifiée
<a name="sectionSection4"> </a>

Votre organisation peut exiger que toutes les données de boîtes aux lettres soient conservées pendant une période spécifique. Avant de placer toutes les boîtes aux lettres d’une organisation en conservation pour litige, prenez en considération les points suivants :
  
Dans cet exemple, toutes les boîtes aux lettres d’utilisateurs de l’organisation sont placées en conservation pour litige pendant un an (365 jours).
  
```
Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | Set-Mailbox -LitigationHoldEnabled $true -LitigationHoldDuration 365
```

Dans cet exemple, la cmdlet [Get-Mailbox](http://technet.microsoft.com/library/8a5a6eb9-4a75-47f9-ae3b-a3ba251cf9a8.aspx) est utilisée pour récupérer toutes les boîtes aux lettres de l’organisation, un filtre de destinataire est spécifié pour inclure toutes les boîtes aux lettres d’utilisateurs, puis la liste des boîtes aux lettres est dirigée vers la cmdlet [Set-Mailbox](http://technet.microsoft.com/library/a0d413b9-d949-4df6-ba96-ac0906dedae2.aspx) pour activer la conservation pour litige et la durée de conservation. 
  
Pour conserver toutes les boîtes aux lettres d'utilisateurs pour une durée indéterminée, exécutez la commande précédente, mais n'incluez pas le paramètre  _LitigationHoldDuration_. 
  
Consultez la section [Plus d'informations](#moreinfo.md) pour obtenir des exemples d'utilisation d'autres propriétés de destinataire dans un filtre pour inclure ou exclure une ou plusieurs boîtes aux lettres. 
  
## <a name="use-the-shell-to-remove-a-mailbox-from-litigation-hold"></a>Utilisation de l’environnement de ligne de commande Exchange Management Shell pour supprimer la conservation pour litige d’une boîte aux lettres
<a name="sectionSection5"> </a>

Dans cet exemple, la conservation pour litige de la boîte aux lettres bsuneja@contoso.com est supprimée.
  
```
Set-Mailbox bsuneja@contoso.com -LitigationHoldEnabled $false
```

P
## <a name="how-do-you-know-this-worked"></a>Comment savoir si cela a fonctionné ?
<a name="sectionSection6"> </a>

Pour vérifier que vous avez correctement placé une boîte aux lettres en conservation pour litige, effectuez l'une des opérations suivantes :
  
- Dans le CAE, procédez comme suit :
    
1. Accédez à **Destinataires**\> **Boîtes aux lettres**.
    
2. Dans la liste des boîtes aux lettres utilisateur, cliquez sur la boîte aux lettres que vous souhaitez vérifier les paramètres de blocage pour litige pour, puis cliquez sur **Modifier** ![icône Modifier](media/ITPro-EAC-EditIcon.gif).
    
3. Dans la page Propriétés de boîte aux lettres, cliquez sur **les fonctionnalités de boîte aux lettres.**
    
4. Sous **Conservation pour litige**, vérifiez que la conservation est activée.
    
5. Cliquez sur **Afficher les détails** pour vérifier la date et l'auteur de la conservation pour litige de la boîte aux lettres. Vous pouvez également vérifier ou modifier les valeurs dans les zones facultatives **Durée de conservation pour litige (en nombre de jours)**, **Remarque** et **URL**. 
    
- Dans l’environnement de ligne de commande Exchange Management Shell, exécutez l’une des commandes suivantes :
    
  ```
  Get-Mailbox <name of mailbox> | FL LitigationHold*
  ```

    ou
    
  ```
  Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | FL Name,LitigationHold*
  ```

    Si une boîte aux lettres est placée en conservation pour litige indéfiniment, la valeur de la propriété de boîte aux lettres  _LitigationHoldDuration_ est définie sur  `Unlimited`.
    
## <a name="more-information"></a>Plus d'informations
<a name="moreinfo"> </a>

- Si votre organisation exige la conservation de toutes les données de boîtes aux lettres pendant une période spécifique, réfléchissez aux éléments suivants avant de placer toutes les boîtes aux lettres de l'organisation en conservation pour litige.
    
  - Lorsque vous utilisez la commande précédente pour mettre en conservation toutes les boîtes aux lettres d'une organisation (ou un sous-ensemble de boîtes aux lettres correspondant à un filtre de destinataire spécifié), seules les boîtes aux lettres existantes au moment de l'exécution de la commande sont placées en conservation. Si vous créez des boîtes aux lettres par la suite, vous devrez exécuter à nouveau la commande pour les placer en conservation. Si vous créez fréquemment des boîtes aux lettres, vous pouvez exécuter la commande en tant que tâche planifiée aussi souvent que nécessaire.
    
  - Placer toutes les boîtes aux lettres en conservation pour litige peut avoir un impact significatif sur les tailles de boîte aux lettres. Dans une organisation Exchange Server 2013, planifier le stockage approprié répondre aux exigences de conservation de votre organisation.
    
  - Le dossier éléments récupérables possède son propre limite de stockage, afin que les éléments dans le dossier ne rentrent dans la limite de stockage de boîtes aux lettres. Comme expliqué précédemment, en conservant les données de boîtes aux lettres pour une longue période sont alors entraîner la croissance du dossier éléments récupérables de boîte aux lettres d’un utilisateur et archiver. Pour prendre en compte pour cette augmentation dans Exchange Online, le quota du dossier éléments récupérables est automatiquement augmenté de 30 Go à 100 Go lorsque vous placez une boîte aux lettres en conservation pour litige. 
    
    Dans Exchange Server 2013, la limite de stockage par défaut pour le dossier éléments récupérables est également 30 Go. Nous vous recommandons de surveiller régulièrement la taille de ce dossier pour vous assurer qu’il n’atteint la limite. Pour plus d’informations, consultez le [Dossier éléments récupérables](http://technet.microsoft.com/library/efc48fb4-2ed8-4d05-93af-f3505fbc389d.aspx).
    
- La commande précédente permettant de placer en conservation toutes les boîtes aux lettres utilise un filtre de destinataire qui renvoie toutes les boîtes aux lettres d'utilisateurs. Vous pouvez utiliser d'autres propriétés de destinataire pour renvoyer une liste de boîtes aux lettres spécifiques que vous pouvez ensuite rediriger vers la cmdlet **Set-Mailbox** pour placer une conservation pour litige sur ces boîtes aux lettres. 
    
    Voici quelques exemples d'utilisation des cmdlets **Get-Mailbox** et **Get-Recipient** pour renvoyer un sous-ensemble de boîtes aux lettres sur la base de propriétés de boîte aux lettres ou d'utilisateur courantes. Ces exemples supposent que les propriétés de boîte aux lettres appropriées (telles que  _CustomAttributeN_ ou  _Department_) aient été renseignées.
    
  ```
  Get-Mailbox -RecipientTypeDetails UserMailbox -ResultSize unlimited -Filter 'CustomAttribute15 -eq "OneYearLitigationHold"'
  ```

  ```
  Get-Recipient -RecipientTypeDetails UserMailbox -ResultSize unlimited -Filter 'Department -eq "HR"'
  ```

  ```
  Get-Recipient -RecipientTypeDetails UserMailbox -ResultSize unlimited -Filter 'PostalCode -eq "98052"'
  ```

  ```
  Get-Recipient -RecipientTypeDetails UserMailbox -ResultSize unlimited -Filter 'StateOrProvince -eq "WA"'
  ```

  ```
  Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -ne "DiscoveryMailbox"}
  ```

    Vous pouvez utiliser d'autres propriétés de boîte aux lettres utilisateur dans un filtre pour inclure ou exclure des boîtes aux lettres. Pour plus d'informations, voir [Filterable Properties for the -Filter Parameter](http://technet.microsoft.com/library/b02b0005-2fb6-4bc2-8815-305259fa5432.aspx).
    

