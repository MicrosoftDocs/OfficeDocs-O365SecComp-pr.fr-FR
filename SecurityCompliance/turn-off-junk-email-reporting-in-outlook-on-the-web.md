---
title: Désactiver la création de rapports dans Outlook sur le site web de courrier indésirable
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/9/2015
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 8d57fe9e-57b8-4884-9317-80b380804b4a
description: En tant qu’un administrateur Office 365, vous pouvez désactiver la possibilité pour les personnes à un message électronique de rapport comme courriers indésirables.
ms.openlocfilehash: 8ee5ff87408b80c443e4cf950ce49f624096becb
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272039"
---
# <a name="turn-off-junk-email-reporting-in-outlook-on-the-web"></a>Désactiver la création de rapports dans Outlook sur le site web de courrier indésirable

Vous pouvez envoyer indésirable, l’hameçonnage et les messages légitimes à Microsoft pour analyse à l’aide d’Outlook sur le courrier indésirable web reporting options, comme indiqué dans le [courrier indésirable de rapport et de hameçonnage dans Outlook sur le web ](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md). Si vous ne souhaitez pas utiliser ces options, administrateurs peuvent les désactiver par le biais de l’applet de commande [Set-OwaMailboxPolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx) . 
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>Ce qu’il faut savoir avant de commencer
<a name="sectionSection0"> </a>

- Durée d'exécution estimée : 5 minutes
    
- Vous devez avoir les autorisations avant de pouvoir effectuer cette procédure, ou procédures. Pour voir les autorisations requises, consultez l’entrée « Stratégies de boîte aux lettres Outlook Web App » dans la rubrique [autorisations Outlook Web App](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx#OutlookWebApp) . 
    
- Avant d’exécuter les applets de commande nécessaire pour désactiver le signalement de courrier indésirable, il peut être utile de consulter les informations de référence dans les rubriques [Get-OwaMailboxPolicy](http://technet.microsoft.com/library/bdd580d3-8812-4b4a-93e8-c6401b0d2f0f.aspx) et [Set-OwaMailboxPolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx) . 
    
## <a name="turn-off-junk-phishing-and-not-junk-reporting-to-microsoft"></a>Désactiver le courrier indésirable, hameçonnage et légitime de création de rapports à Microsoft
<a name="sectionSection1"> </a>

Tout d'abord, exécutez la cmdlet suivante pour obtenir les répertoires virtuels pour lesquels vous souhaitez désactiver le signalement :
  
```
Get-OwaMailboxPolicy -Identity <parameter>
```

Ensuite, exécutez la cmdlet suivante pour désactiver le signalement des courriers indésirables et légitimes à Microsoft :
  
```
Set-OwaMailboxPolicy -Identity <parameter> -ReportJunkEmailEnabled $false
```

Par exemple, la cmdlet suivante désactive le signalement pour le répertoire virtuel Contoso\owa :
  
```
Set-OwaMailboxPolicy -Identity Default -ReportJunkEmailEnabled $false
```

## <a name="how-do-you-know-this-worked"></a>Comment savoir si cela a fonctionné ?
<a name="sectionSection2"> </a>

Exécutez Get-OWAMailboxPolicy pour vérifier les valeurs de paramètre et ensuite accéder à Outlook sur le web et vérifiez que les options pour signaler le courrier indésirable, l’hameçonnage et légitime ne sont pas disponibles. Vous serez toujours en mesure de marquer les messages comme courrier indésirable, hameçonnage et légitime, mais vous ne pourrez pas les signaler. 
  

