---
title: Placement d'une boîte aux lettres en conservation pour litige
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/18/2016
ms.audience: End User
ms.topic: article
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid: ''
ms.assetid: adee4621-3626-4aec-aa53-00b35ff0d0b0
description: 'Vous pouvez placer une boîte aux lettres en conservation pour litige pour conserver tout le contenu de la boîte aux lettres, y compris les éléments supprimés et les versions originales des éléments modifiés. '
ms.openlocfilehash: a4d0939ffed32a8442b4b705bd15804b9f3eb7ea
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693123"
---
# <a name="place-a-mailbox-on-litigation-hold"></a>Placement d'une boîte aux lettres en conservation pour litige
 
Vous pouvez placer une boîte aux lettres en conservation pour litige pour conserver tout le contenu de la boîte aux lettres, y compris les éléments supprimés et les versions originales des éléments modifiés. Lorsque vous placez la boîte aux lettres d'un utilisateur en conservation pour litige, le contenu de la boîte aux lettres d'archivage de l'utilisateur (si elle est activée) est également placé en conservation. Les éléments supprimés et modifiés sont conservés pendant une période spécifiée, ou jusqu'à ce que vous supprimiez la boîte aux lettres de la conservation pour litige. Tous ces éléments de boîte aux lettres sont renvoyés dans une recherche de [Découverte électronique locale](http://technet.microsoft.com/library/6377cb7a-3416-4e15-8571-c45d2160fc6f.aspx). 
  
> [!IMPORTANT]
> La conservation pour litige conserve les éléments dans le dossier Éléments récupérables de la boîte aux lettres de l'utilisateur. En fonction du nombre et de la taille des éléments supprimés ou modifiés, la taille du dossier Éléments récupérables de la boîte aux lettres peut augmenter rapidement. Le dossier Éléments récupérables est configuré avec un quota élevé par défaut. Dans Exchange Online, ce quota augmente automatiquement lorsque vous placez une boîte aux lettres en conservation pour litige. Dans Exchange Server 2013, nous vous recommandons de surveiller les boîtes aux lettres placées en conservation pour litige sur une base hebdomadaire afin de s'assurer qu'elles n'atteignent pas les limites des quotas d'éléments récupérables. 
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>Ce qu’il faut savoir avant de commencer
<a name="sectionSection0"> </a>

- Durée d'exécution estimée : 5 minutes
    
- Il se peut que vous deviez attendre 60 minutes avant que le paramètre Conservation pour litige ne soit actif.
    
- Des autorisations doivent vous être attribuées avant de pouvoir exécuter cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez l'entrée « Conservation inaltérable » dans la rubrique [Stratégie de messagerie et autorisations de conformité](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx). 
    
- Pour placer une boîte aux lettres Exchange Online en conservation pour litige, une licence Exchange Online (plan 2) doit lui être attribuée. Si une boîte aux lettres dispose d’une licence Exchange Online (Plan 1), vous devez lui attribuer une licence Archivage Exchange Online distincte pour la placer en conservation inaltérable.
    
- Comme expliqué précédemment, lorsque vous placez une conservation pour litige dans la boîte aux lettres d'un utilisateur, le contenu de la boîte aux lettres d'archivage de l'utilisateur est également placé en conservation. Si vous placez une conservation pour litige sur une boîte aux lettres principale locale dans un déploiement hybride Exchange, la boîte aux lettres d'archivage informatique (si elle est activée) est également mise en attente.
    
- Dans Exchange Online, le quota pour le dossier éléments récupérables est automatiquement augmenté à 100 Go lorsque vous placez une boîte aux lettres en conservation pour litige. La taille par défaut de ce dossier est de 30 Go.
    
- La conservation pour litige conserve les éléments supprimés, ainsi que les versions originales des éléments modifiés jusqu'à ce que la conservation soit supprimée. Vous pouvez éventuellement spécifier une durée d'attente, ce qui permet de conserver un élément de boîte aux lettres pendant la durée spécifiée. Si vous spécifiez une durée d'attente, cette dernière débute à partir de la date de réception d'un message ou de la date de création d'un élément de boîte aux lettres. Pour conserver les éléments qui répondent aux critères spécifiés, utilisez une conservation inaltérable pour créer une conservation basée sur une requête. Pour plus d'informations, consultez la rubrique [créer ou supprimer une conservation](http://technet.microsoft.com/library/9d5d8d37-a053-4830-9cb1-6e1ede25e963.aspx)inaltérable.
    
- Pour utiliser l'environnement de ligne de commande Exchange Management Shell pour mettre en attente une boîte aux lettres Exchange Online, vous devez utiliser Exchange Online PowerShell. Pour plus d'informations, voir [Connexion à Exchange Online à l'aide de Remote PowerShell](http://technet.microsoft.com/library/c8bea338-6c1a-4bdf-8de0-7895d427ee5b.aspx).
    
- La mise en attente pour litige dans une boîte aux lettres de dossiers publics n'est pas prise en charge. Vous devez utiliser la conservation inaltérable pour placer une conservation sur des dossiers publics.
    
## <a name="use-the-eac-to-place-a-mailbox-on-litigation-hold"></a>Utilisation du Centre d’administration Exchange pour mettre une boîte aux lettres en conservation pour litige
<a name="sectionSection1"> </a>

1. Accédez à **Destinataires** \> **Boîtes aux lettres**.
    
2. Dans la liste des boîtes aux lettres utilisateur, cliquez sur la boîte aux lettres que vous souhaitez placer en conservation pour litige **** ![, puis cliquez](media/ITPro-EAC-EditIcon.gif)sur modifier l'icône modifier.
    
3. Dans la page Propriétés de boîte aux lettres, cliquez sur **fonctionnalités de boîte aux lettres.**
    
4. Sous **Conservation pour litige : désactivée**, cliquez sur **Activer** pour mettre la boîte aux lettres en conservation pour litige. 
    
5. Sur la page **Conservation pour litige**, entrez les informations facultatives suivantes : 
    
  - **Durée de conservation pour litige (en nombre de jours)** Cette zone permet de spécifier la durée de conservation des éléments de boîte aux lettres lorsque la boîte aux lettres est conservée pour litige. La durée est calculée à compter de la date de réception ou de création de l'élément de boîte aux lettres. Si vous laissez cette zone vide, les éléments sont conservés indéfiniment ou jusqu'à ce que la conservation soit annulée. Indiquez la période en nombre de jours. 
    
  - **Remarque** Cette zone permet d'informer l'utilisateur de la conservation pour litige de sa boîte aux lettres. La note apparaît dans la boîte aux lettres de l'utilisateur si elle utilise Outlook 2010 ou une version ultérieure. 
    
  - **URL** Cette zone permet de diriger l'utilisateur vers un site web pour plus d'informations sur la conservation pour litige. Cette URL apparaît dans la boîte aux lettres de l'utilisateur si elle utilise Outlook 2010 ou une version ultérieure. 
    
6. Cliquez sur **Enregistrer** sur la page **Conservation pour litige**, puis cliquez sur **Enregistrer** sur la page des propriétés de boîte aux lettres. 
  
## <a name="use-the-shell-to-place-a-mailbox-on-litigation-hold-indefinitely"></a>Utiliser l'environnement Shell pour placer une boîte aux lettres en conservation pour litige indéfiniment
<a name="sectionSection2"> </a>

Dans cet exemple, la boîte aux lettres bsuneja@contoso.com est placée en conservation pour litige. Les éléments de la boîte aux lettres sont conservés indéfiniment ou jusqu'à ce que la conservation soit supprimée.
  
```
Set-Mailbox bsuneja@contoso.com -LitigationHoldEnabled $true
```

> [!NOTE]
> Lorsque vous placez une boîte aux lettres en conservation pour litige indéfiniment (en ne spécifiant aucune durée), la valeur de la propriété de boîte aux lettres  _LitigationHoldDuration_ est définie sur  `Unlimited`. 
  
## <a name="use-the-shell-to-place-a-mailbox-on-litigation-hold-and-preserve-items-for-a-specified-duration"></a>Utiliser l'environnement de lignes de commande Exchange Management Shell pour mettre une boîte aux lettres en conservation pour litige et conserver des éléments pendant une durée spécifiée
<a name="sectionSection3"> </a>

Dans cet exemple, la boîte aux lettres bsuneja@contoso.com est placée en conservation pour litige et les éléments sont conservés pendant 2 555 jours (environ 7 ans). 
  
```
Set-Mailbox bsuneja@contoso.com -LitigationHoldEnabled $true -LitigationHoldDuration 2555
```

## <a name="use-the-shell-to-place-all-mailboxes-on-litigation-hold-for-a-specified-duration"></a>Utiliser l'environnement Shell pour placer toutes les boîtes aux lettres en conservation pour litige pendant une durée spécifiée
<a name="sectionSection4"> </a>

Votre organisation peut exiger que toutes les données de boîte aux lettres soient conservées pendant une période de temps spécifique. Avant de placer toutes les boîtes aux lettres d'une organisation en conservation pour litige, prenez en compte les points suivants:
  
Dans cet exemple, toutes les boîtes aux lettres utilisateur de l'organisation sont placées en conservation pour litige pendant un an (365 jours).
  
```
Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | Set-Mailbox -LitigationHoldEnabled $true -LitigationHoldDuration 365
```

Cet exemple utilise la cmdlet [Get-Mailbox](http://technet.microsoft.com/library/8a5a6eb9-4a75-47f9-ae3b-a3ba251cf9a8.aspx) pour récupérer toutes les boîtes aux lettres de l'organisation, spécifie un filtre de destinataires pour inclure toutes les boîtes aux lettres utilisateur, puis canalise la liste des boîtes aux lettres vers la cmdlet [Set-Mailbox](http://technet.microsoft.com/library/a0d413b9-d949-4df6-ba96-ac0906dedae2.aspx) pour activer la conservation pour litige et durée de la conservation. 
  
Pour conserver toutes les boîtes aux lettres d'utilisateurs pour une durée indéterminée, exécutez la commande précédente, mais n'incluez pas le paramètre  _LitigationHoldDuration_. 
  
Consultez la section [Plus d'informations](#moreinfo.md) pour obtenir des exemples d'utilisation d'autres propriétés de destinataire dans un filtre pour inclure ou exclure une ou plusieurs boîtes aux lettres. 
  
## <a name="use-the-shell-to-remove-a-mailbox-from-litigation-hold"></a>Utiliser l'environnement de commande Exchange Management Shell pour supprimer une boîte aux lettres en conservation pour litige
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
    
2. Dans la liste des boîtes aux lettres utilisateur, cliquez sur la boîte aux lettres pour laquelle vous souhaitez vérifier les paramètres de conservation **** ![pour litige,](media/ITPro-EAC-EditIcon.gif)puis cliquez sur modifier l'icône de modification.
    
3. Dans la page Propriétés de boîte aux lettres, cliquez sur **fonctionnalités de boîte aux lettres.**
    
4. Sous **Conservation pour litige**, vérifiez que la conservation est activée.
    
5. Cliquez sur **Afficher les détails** pour vérifier la date et l'auteur de la conservation pour litige de la boîte aux lettres. Vous pouvez également vérifier ou modifier les valeurs dans les zones facultatives **Durée de conservation pour litige (en nombre de jours)**, **Remarque** et **URL**. 
    
- Dans l'environnement de commande Exchange Management Shell, exécutez l'une des commandes suivantes:
    
  ```
  Get-Mailbox <name of mailbox> | FL LitigationHold*
  ```

    ou
    
  ```
  Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | FL Name,LitigationHold*
  ```

    Si une boîte aux lettres est placée en conservation pour litige indéfiniment, la valeur de la propriété de boîte aux lettres  _LitigationHoldDuration_ est définie sur  `Unlimited`.
    
## <a name="more-information"></a>Plus d’informations
<a name="moreinfo"> </a>

- Si votre organisation exige la conservation de toutes les données de boîtes aux lettres pendant une période spécifique, réfléchissez aux éléments suivants avant de placer toutes les boîtes aux lettres de l'organisation en conservation pour litige.
    
  - Lorsque vous utilisez la commande précédente pour mettre en conservation toutes les boîtes aux lettres d'une organisation (ou un sous-ensemble de boîtes aux lettres correspondant à un filtre de destinataire spécifié), seules les boîtes aux lettres existantes au moment de l'exécution de la commande sont placées en conservation. Si vous créez des boîtes aux lettres par la suite, vous devrez exécuter à nouveau la commande pour les placer en conservation. Si vous créez fréquemment des boîtes aux lettres, vous pouvez exécuter la commande en tant que tâche planifiée aussi souvent que nécessaire.
    
  - Le placement de toutes les boîtes aux lettres en conservation pour litige peut avoir une incidence considérable sur la taille des boîtes aux lettres. Dans une organisation Exchange Server 2013, planifiez un stockage adéquat pour répondre aux exigences de conservation de votre organisation.
    
  - Le dossier éléments récupérables a sa propre limite de stockage, de sorte que les éléments dans le dossier ne sont pas pris en compte dans la limite de stockage de boîte aux lettres. Comme expliqué précédemment, la conservation des données de boîte aux lettres pendant une longue période entraînera la croissance du dossier éléments récupérables dans la boîte aux lettres et l'archive d'un utilisateur. Pour tenir compte de cette augmentation dans Exchange Online, le quota pour le dossier éléments récupérables est automatiquement augmenté de 30 Go à 100 Go lorsque vous placez une boîte aux lettres en conservation pour litige. 
    
    Dans Exchange Server 2013, la limite de stockage par défaut pour le dossier éléments récupérables est également de 30 Go. Nous vous recommandons de surveiller régulièrement la taille de ce dossier pour vous assurer qu'il n'atteint pas la limite. Pour plus d'informations, consultez la rubrique [dossier éléments récupérables](http://technet.microsoft.com/library/efc48fb4-2ed8-4d05-93af-f3505fbc389d.aspx).
    
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
    

