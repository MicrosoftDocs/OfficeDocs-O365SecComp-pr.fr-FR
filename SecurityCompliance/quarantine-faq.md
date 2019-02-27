---
title: FAQ sur la mise en quarantaine
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 6/16/2017
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c440b2ac-cafa-4be5-ba4c-14278a7990ae
ms.collection:
- M365-security-compliance
description: Cette rubrique présente les questions fréquemment posées ainsi que les réponses au sujet de la mise en quarantaine hébergée.
ms.openlocfilehash: 381eb0aba25d7149c2f164f9e0173034568d5eff
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30276024"
---
# <a name="quarantine-faq"></a>FAQ sur la mise en quarantaine

Cette rubrique présente les questions fréquemment posées ainsi que les réponses au sujet de la mise en quarantaine hébergée. Les réponses sont applicables pour les clients Microsoft Exchange Online et Exchange Online Protection.
  
 **Q. Comment puis-je gérer les messages mis en quarantaine contre les programmes malveillants?**
  
Vous devez utiliser le centre de &amp; sécurité conformité afin d'afficher et de manipuler les messages qui ont été envoyés en quarantaine car ils contiennent des programmes malveillants. Pour plus d'informations, consultez la rubrique [mise en quarantaine des messages électroniques dans Office 365](https://support.office.com/article/Quarantine-email-messages-in-Office-365-4c234874-015e-4768-8495-98fcccfc639b).
  
 **Q. Comment puis-je configurer le service pour envoyer des messages de courrier indésirable mis en quarantaine vers la mise en quarantaine ?**
  
R. Par défaut, les messages dont le contenu est filtré sont envoyés vers le dossier de courrier indésirable des destinataires. Toutefois, les administrateurs peuvent configurer des stratégies de filtrage de contenu pour envoyer le courrier indésirable mis en quarantaine vers la mise en quarantaine. Pour plus d'informations sur les différentes actions qui peuvent être menées sur les messages dont le contenu est filtré, voir [Configuration de vos stratégies de filtrage du courrier indésirable](configure-your-spam-filter-policies.md).
  
 **Q. Le service permet-il une gestion par un administrateur ou un utilisateur final des messages de courrier indésirable mis en quarantaine ?**
  
R. En tant qu'administrateur, vous pouvez rechercher et afficher des détails sur tous les messages électroniques mis en quarantaine dans le Centre d'administration Exchange (CAE). Après avoir localisé un message, vous pouvez le débloquer pour l'envoyer à des utilisateurs spécifiques et, si vous le souhaitez, le signaler comme faux positif (message légitime) à l'équipe d'analyse du courrier indésirable de Microsoft. Pour plus d'informations, voir [Rechercher et débloquer les messages mis en quarantaine en tant qu'administrateur](find-and-release-quarantined-messages-as-an-administrator.md).
  
En tant qu'utilisateur final, vous pouvez gérer vos propres messages mis en quarantaine via : 
  
- L'interface utilisateur de mise en quarantaine du courrier électronique. Pour plus d’informations, voir [Find and Release Quarantined Messages (End Users)](http://technet.microsoft.com/library/e439b560-827a-4807-abd3-6b861c1ff786.aspx).
        
 **Q. Comment accorder l'accès au courrier indésirable mis en quarantaine aux utilisateurs finaux ?**
  
A. pour accéder à la mise en quarantaine du courrier indésirable de l'utilisateur final, les utilisateurs finaux doivent disposer d'un ID d'utilisateur et d'un mot de passe Office 365 valides. Les clients EOP qui protègent les boîtes aux lettres locales doivent être des utilisateurs de messagerie valides créés via la synchronisation d'annuaires ou le centre d'administration Exchange. Pour plus d'informations sur la gestion des utilisateurs, les administrateurs EOP peuvent se référer à la rubrique [gérer les utilisateurs de messagerie dans EOP](eop/manage-mail-users-in-eop.md). Pour les clients autonomes EOP, nous vous recommandons d'utiliser la synchronisation d'annuaires et d'activer le blocage du périmètre basé sur l'annuaire; Pour plus d'informations, consultez la rubrique [utiliser le blocage du périmètre basé sur l'annuaire pour rejeter les messages envoyés à des destinataires non valides](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx).
  
 **Q. Est-ce que du courrier autre que du courrier indésirable peut être envoyé en quarantaine ?**
  
R. Les messages concernés par une règle de transport peuvent également être envoyés dans la boîte de quarantaine de l'administrateur, si cette action est celle qui a été configurée. La boîte de mise en quarantaine de l'utilisateur final est uniquement réservée au courrier indésirable.
  
 **Q. Pendant combien de temps les messages sont-ils mis en quarantaine ?**
  
A. par défaut, les messages de courrier indésirable mis en quarantaine sont conservés en quarantaine pendant 30 jours, tandis que les messages mis en quarantaine qui correspondent à une règle de transport sont maintenus en quarantaine pendant 7 jours. Après cette période de temps, les messages sont supprimés et ne peuvent pas être récupérés. La période de rétention pour les messages en quarantaine qui correspondent à une règle de transport ne peut pas être configurée. Toutefois, la période de rétention des messages indésirables mis en quarantaine peut être abaissée via le paramètre **conserver le courrier indésirable pendant (jours)** dans vos stratégies de filtrage de contenu. Pour plus d'informations, consultez [la rubrique Configuration de vos stratégies de filtrage du courrier](configure-your-spam-filter-policies.md)indésirable.
  
 **Q. Est-ce que je peux libérer ou signaler plusieurs messages mis en quarantaine à la fois ?**
  
R. La fonction de libération ou de signalement de plusieurs messages à la fois n'est pas disponible actuellement dans le CAE ou la mise en quarantaine du courrier indésirable de l'utilisateur final. Toutefois, les administrateurs peuvent créer un script Windows PowerShell à distance pour accomplir cette tâche. Utilisez la cmdlet [Get-QuarantineMessage](http://technet.microsoft.com/library/88026da1-8dbc-49e7-80e8-112a32773c34.aspx) pour rechercher des messages, et la cmdlet [Release-QuarantineMessage](http://technet.microsoft.com/library/4a3aa05c-238f-46f2-b8dd-b0e3c38eab3e.aspx) pour les libérer. 
  
 **Q. les caractères génériques sont-ils pris en charge lors de la recherche de messages mis en quarantaine? Puis-je Rechercher des messages mis en quarantaine pour un domaine spécifique?**
  
R. Les caractères génériques ne sont pas pris en charge lors de la spécification des critères de recherche dans le Centre d'administration Exchange. Par exemple, si vous recherchez un expéditeur, vous devez indiquer l'adresse électronique complète.
  
Le recours à Windows PowerShell à distance permet aux administrateurs d'utiliser la cmdlet [Get-QuarantineMessage](http://technet.microsoft.com/library/88026da1-8dbc-49e7-80e8-112a32773c34.aspx) pour rechercher des messages mis en quarantaine pour un domaine spécifique (par exemple, contoso.com) : 
  
```
Get-QuarantineMessage | ? {$_.Senderaddress -like "*@contoso.com"}
```

Les résultats peuvent être transmis à la cmdlet [Release-QuarantineMessage](http://technet.microsoft.com/library/4a3aa05c-238f-46f2-b8dd-b0e3c38eab3e.aspx). Incluez le paramètre -ReleaseToAll pour débloquer le message et l'envoyer à tous ses destinataires. Une fois qu'un message est débloqué, il ne peut plus l'être de nouveau. 
  
```
Get-QuarantineMessage | ? {$_.Senderaddress -like "*@contoso.com"}
```


