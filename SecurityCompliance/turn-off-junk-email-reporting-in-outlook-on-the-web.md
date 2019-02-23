---
title: Désactiver la création de rapports de courrier indésirable dans Outlook sur le Web
ms.author: krowley
author: kccross
manager: laurawi
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 8d57fe9e-57b8-4884-9317-80b380804b4a
description: En tant qu'administrateur Office 365, vous pouvez désactiver la possibilité pour les utilisateurs de signaler le courrier indésirable.
ms.openlocfilehash: 4c84ae6b92658d045675fd8e8ffe6a6cff516886
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30213914"
---
# <a name="turn-off-junk-email-reporting-in-outlook-on-the-web"></a>Désactiver la création de rapports de courrier indésirable dans Outlook sur le Web

Vous pouvez envoyer des messages indésirables, de hameçonnage et non de courrier indésirable à Microsoft à des fins d'analyse à l'aide des options de création de rapports de courrier indésirable Outlook sur le Web (anciennement appelé Outlook Web App), comme décrit dans le rapport de courrier indésirable [et les escroqueries par hameçonnage dans Outlook sur le Web ](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md). Si vous ne souhaitez pas utiliser ces options, les administrateurs peuvent les désactiver via la cmdlet [Set-OwaMailboxPolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx) . 
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>Ce qu'il faut savoir avant de commencer
<a name="sectionSection0"> </a>

- Durée d’exécution estimée : 5 minutes
    
- Des autorisations doivent vous être attribuées avant de pouvoir effectuer cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez entrée «stratégies de boîte aux lettres Outlook sur le Web» dans la rubrique [autorisations Outlook sur le Web](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx#OutlookWebApp) . 

- Pour vous connecter à Exchange Online PowerShell, consultez la rubrique [connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).

## <a name="turn-off-junk-phishing-and-not-junk-reporting-to-microsoft"></a>Désactiver le courrier indésirable, le hameçonnage et les notifications de courrier indésirable à Microsoft
<a name="sectionSection1"> </a>

Tout d'abord, exécutez la commande suivante pour obtenir les noms de vos stratégies de boîte aux lettres Outlook sur le Web disponibles:
  
```
Get-OwaMailboxPolicy | Format-Table Name
```

Ensuite, utilisez la syntaxe suivante pour activer ou désactiver le signalement de courrier indésirable à Microsoft dans Outlook sur le Web:
  
```
Set-OwaMailboxPolicy -Identity "<OWAMailboxPolicyName>" -ReportJunkEmailEnabled <$true | $false>
```

Cet exemple montre comment désactiver la création de rapports dans la stratégie de boîte aux lettres Outlook Web App par défaut:
  
```
Set-OwaMailboxPolicy -Identity "OwaMailboxPolicy-Default" -ReportJunkEmailEnabled $false
```

Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Get-OwaMailboxPolicy](http://technet.microsoft.com/library/bdd580d3-8812-4b4a-93e8-c6401b0d2f0f.aspx) et [Set-OwaMailboxPolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx).

## <a name="how-do-you-know-this-worked"></a>Comment savoir si cela a fonctionné ?
<a name="sectionSection2"> </a>

Exécutez **Get-OwaMailboxPolicy** pour vérifier les valeurs des paramètres, puis ouvrez Outlook sur le Web pour un utilisateur affecté (auquel la stratégie de boîte aux lettres Outlook sur le Web est appliquée) et vérifiez que les options de signalement de courrier indésirable, de hameçonnage et non de courrier indésirable ne sont pas disponibles. Vous serez toujours en mesure de marquer les messages comme courriers indésirables, de hameçonnage et non comme courriers indésirables, mais vous ne pourrez pas les signaler. 
