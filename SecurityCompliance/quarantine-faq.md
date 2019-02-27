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
# <a name="quarantine-faq"></a><span data-ttu-id="b1bc1-103">FAQ sur la mise en quarantaine</span><span class="sxs-lookup"><span data-stu-id="b1bc1-103">Quarantine FAQ</span></span>

<span data-ttu-id="b1bc1-p101">Cette rubrique présente les questions fréquemment posées ainsi que les réponses au sujet de la mise en quarantaine hébergée. Les réponses sont applicables pour les clients Microsoft Exchange Online et Exchange Online Protection.</span><span class="sxs-lookup"><span data-stu-id="b1bc1-p101">This topic provides frequently asked questions and answers about the hosted quarantine. Answers are applicable for Microsoft Exchange Online and Exchange Online Protection customers.</span></span>
  
 <span data-ttu-id="b1bc1-106">**Q. Comment puis-je gérer les messages mis en quarantaine contre les programmes malveillants?**</span><span class="sxs-lookup"><span data-stu-id="b1bc1-106">**Q. How do I manage malware-quarantined messages in quarantine?**</span></span>
  
<span data-ttu-id="b1bc1-p102">Vous devez utiliser le centre de &amp; sécurité conformité afin d'afficher et de manipuler les messages qui ont été envoyés en quarantaine car ils contiennent des programmes malveillants. Pour plus d'informations, consultez la rubrique [mise en quarantaine des messages électroniques dans Office 365](https://support.office.com/article/Quarantine-email-messages-in-Office-365-4c234874-015e-4768-8495-98fcccfc639b).</span><span class="sxs-lookup"><span data-stu-id="b1bc1-p102">You need to use the Security &amp; Compliance Center in order to view and work with messages that were sent to quarantine because they contain malware. For more information, see [Quarantine email messages in Office 365](https://support.office.com/article/Quarantine-email-messages-in-Office-365-4c234874-015e-4768-8495-98fcccfc639b).</span></span>
  
 <span data-ttu-id="b1bc1-109">**Q. Comment puis-je configurer le service pour envoyer des messages de courrier indésirable mis en quarantaine vers la mise en quarantaine ?**</span><span class="sxs-lookup"><span data-stu-id="b1bc1-109">**Q. How do I configure the service to send spam-quarantined messages to the quarantine?**</span></span>
  
<span data-ttu-id="b1bc1-p103">R. Par défaut, les messages dont le contenu est filtré sont envoyés vers le dossier de courrier indésirable des destinataires. Toutefois, les administrateurs peuvent configurer des stratégies de filtrage de contenu pour envoyer le courrier indésirable mis en quarantaine vers la mise en quarantaine. Pour plus d'informations sur les différentes actions qui peuvent être menées sur les messages dont le contenu est filtré, voir [Configuration de vos stratégies de filtrage du courrier indésirable](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="b1bc1-p103">A. By default, content-filtered messages are sent to the recipients Junk Email folder. However, admins can configure content filter policies to send spam-quarantined messages to the quarantine instead. For more information about the different actions that can be performed on content-filtered messages, see [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span>
  
 <span data-ttu-id="b1bc1-114">**Q. Le service permet-il une gestion par un administrateur ou un utilisateur final des messages de courrier indésirable mis en quarantaine ?**</span><span class="sxs-lookup"><span data-stu-id="b1bc1-114">**Q. Does the service have administrator and end user management of spam-quarantined messages?**</span></span>
  
<span data-ttu-id="b1bc1-p104">R. En tant qu'administrateur, vous pouvez rechercher et afficher des détails sur tous les messages électroniques mis en quarantaine dans le Centre d'administration Exchange (CAE). Après avoir localisé un message, vous pouvez le débloquer pour l'envoyer à des utilisateurs spécifiques et, si vous le souhaitez, le signaler comme faux positif (message légitime) à l'équipe d'analyse du courrier indésirable de Microsoft. Pour plus d'informations, voir [Rechercher et débloquer les messages mis en quarantaine en tant qu'administrateur](find-and-release-quarantined-messages-as-an-administrator.md).</span><span class="sxs-lookup"><span data-stu-id="b1bc1-p104">A. As an administrator, you can search for and view details about all quarantined email messages in the Exchange admin center (EAC). After locating the message, you can release it to specific users and optionally report it as a false positive (not junk) to the Microsoft Spam Analysis Team. For more information, see [Find and release quarantined messages as an administrator](find-and-release-quarantined-messages-as-an-administrator.md).</span></span>
  
<span data-ttu-id="b1bc1-119">En tant qu'utilisateur final, vous pouvez gérer vos propres messages mis en quarantaine via :</span><span class="sxs-lookup"><span data-stu-id="b1bc1-119">As an end user, you can manage your own spam-quarantined messages via:</span></span> 
  
- <span data-ttu-id="b1bc1-p105">L'interface utilisateur de mise en quarantaine du courrier électronique. Pour plus d’informations, voir [Find and Release Quarantined Messages (End Users)](http://technet.microsoft.com/library/e439b560-827a-4807-abd3-6b861c1ff786.aspx).</span><span class="sxs-lookup"><span data-stu-id="b1bc1-p105">The spam quarantine user interface. For more information, see [Find and Release Quarantined Messages (End Users)](http://technet.microsoft.com/library/e439b560-827a-4807-abd3-6b861c1ff786.aspx).</span></span>
        
 <span data-ttu-id="b1bc1-122">**Q. Comment accorder l'accès au courrier indésirable mis en quarantaine aux utilisateurs finaux ?**</span><span class="sxs-lookup"><span data-stu-id="b1bc1-122">**Q. How do I grant access to the spam quarantine for my end users?**</span></span>
  
<span data-ttu-id="b1bc1-p106">A. pour accéder à la mise en quarantaine du courrier indésirable de l'utilisateur final, les utilisateurs finaux doivent disposer d'un ID d'utilisateur et d'un mot de passe Office 365 valides. Les clients EOP qui protègent les boîtes aux lettres locales doivent être des utilisateurs de messagerie valides créés via la synchronisation d'annuaires ou le centre d'administration Exchange. Pour plus d'informations sur la gestion des utilisateurs, les administrateurs EOP peuvent se référer à la rubrique [gérer les utilisateurs de messagerie dans EOP](eop/manage-mail-users-in-eop.md). Pour les clients autonomes EOP, nous vous recommandons d'utiliser la synchronisation d'annuaires et d'activer le blocage du périmètre basé sur l'annuaire; Pour plus d'informations, consultez la rubrique [utiliser le blocage du périmètre basé sur l'annuaire pour rejeter les messages envoyés à des destinataires non valides](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx).</span><span class="sxs-lookup"><span data-stu-id="b1bc1-p106">A. In order to access the end user spam quarantine, end users must have a valid Office 365 user ID and password. EOP customers protecting on-premises mailboxes must be valid email users created via directory synchronization or the EAC. For more information about managing users, EOP admins can refer to [Manage mail users in EOP](eop/manage-mail-users-in-eop.md). For EOP standalone customers, we recommend using directory synchronization and enabling Directory Based Edge Blocking; for more information, see [Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx).</span></span>
  
 <span data-ttu-id="b1bc1-128">**Q. Est-ce que du courrier autre que du courrier indésirable peut être envoyé en quarantaine ?**</span><span class="sxs-lookup"><span data-stu-id="b1bc1-128">**Q. Can anything other than spam be sent to the quarantine?**</span></span>
  
<span data-ttu-id="b1bc1-p107">R. Les messages concernés par une règle de transport peuvent également être envoyés dans la boîte de quarantaine de l'administrateur, si cette action est celle qui a été configurée. La boîte de mise en quarantaine de l'utilisateur final est uniquement réservée au courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="b1bc1-p107">A. Messages that match a transport rule can also be sent to the administrator quarantine, if that's the configured action. The end user quarantine is for spam only.</span></span>
  
 <span data-ttu-id="b1bc1-132">**Q. Pendant combien de temps les messages sont-ils mis en quarantaine ?**</span><span class="sxs-lookup"><span data-stu-id="b1bc1-132">**Q. For how long are messages kept in the quarantine?**</span></span>
  
<span data-ttu-id="b1bc1-p108">A. par défaut, les messages de courrier indésirable mis en quarantaine sont conservés en quarantaine pendant 30 jours, tandis que les messages mis en quarantaine qui correspondent à une règle de transport sont maintenus en quarantaine pendant 7 jours. Après cette période de temps, les messages sont supprimés et ne peuvent pas être récupérés. La période de rétention pour les messages en quarantaine qui correspondent à une règle de transport ne peut pas être configurée. Toutefois, la période de rétention des messages indésirables mis en quarantaine peut être abaissée via le paramètre **conserver le courrier indésirable pendant (jours)** dans vos stratégies de filtrage de contenu. Pour plus d'informations, consultez [la rubrique Configuration de vos stratégies de filtrage du courrier](configure-your-spam-filter-policies.md)indésirable.</span><span class="sxs-lookup"><span data-stu-id="b1bc1-p108">A. By default, spam-quarantined messages are kept in the quarantine for 30 days, while quarantined messages that matched a transport rule are kept in the quarantine for 7 days. After this period of time the messages are deleted and are not retrievable. The retention period for quarantined messages that matched a transport rule is not configurable. However, the retention period for spam-quarantined messages can be lowered via the **Retain spam for (days)** setting in your content filter policies. For more information, see [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span>
  
 <span data-ttu-id="b1bc1-139">**Q. Est-ce que je peux libérer ou signaler plusieurs messages mis en quarantaine à la fois ?**</span><span class="sxs-lookup"><span data-stu-id="b1bc1-139">**Q. Can I release or report more than one quarantined message at a time?**</span></span>
  
<span data-ttu-id="b1bc1-p109">R. La fonction de libération ou de signalement de plusieurs messages à la fois n'est pas disponible actuellement dans le CAE ou la mise en quarantaine du courrier indésirable de l'utilisateur final. Toutefois, les administrateurs peuvent créer un script Windows PowerShell à distance pour accomplir cette tâche. Utilisez la cmdlet [Get-QuarantineMessage](http://technet.microsoft.com/library/88026da1-8dbc-49e7-80e8-112a32773c34.aspx) pour rechercher des messages, et la cmdlet [Release-QuarantineMessage](http://technet.microsoft.com/library/4a3aa05c-238f-46f2-b8dd-b0e3c38eab3e.aspx) pour les libérer.</span><span class="sxs-lookup"><span data-stu-id="b1bc1-p109">A. The ability to release or report multiple messages at once is not currently available in the EAC or the end user spam quarantine. However, admins can create a remote Windows PowerShell script to accomplish this task. Use the [Get-QuarantineMessage](http://technet.microsoft.com/library/88026da1-8dbc-49e7-80e8-112a32773c34.aspx) cmdlet to search for messages, and the [Release-QuarantineMessage](http://technet.microsoft.com/library/4a3aa05c-238f-46f2-b8dd-b0e3c38eab3e.aspx) cmdlet to release them.</span></span> 
  
 <span data-ttu-id="b1bc1-144">**Q. les caractères génériques sont-ils pris en charge lors de la recherche de messages mis en quarantaine? Puis-je Rechercher des messages mis en quarantaine pour un domaine spécifique?**</span><span class="sxs-lookup"><span data-stu-id="b1bc1-144">**Q. Are wildcards supported when searching for quarantined messages? Can I search for quarantined messages for a specific domain?**</span></span>
  
<span data-ttu-id="b1bc1-p110">R. Les caractères génériques ne sont pas pris en charge lors de la spécification des critères de recherche dans le Centre d'administration Exchange. Par exemple, si vous recherchez un expéditeur, vous devez indiquer l'adresse électronique complète.</span><span class="sxs-lookup"><span data-stu-id="b1bc1-p110">A. Wildcards are not supported when specifying search criteria in the Exchange admin center. For example, when searching for a sender, you must specify the full email address.</span></span>
  
<span data-ttu-id="b1bc1-148">Le recours à Windows PowerShell à distance permet aux administrateurs d'utiliser la cmdlet [Get-QuarantineMessage](http://technet.microsoft.com/library/88026da1-8dbc-49e7-80e8-112a32773c34.aspx) pour rechercher des messages mis en quarantaine pour un domaine spécifique (par exemple, contoso.com) :</span><span class="sxs-lookup"><span data-stu-id="b1bc1-148">Using remote Windows PowerShell, admins can specify the [Get-QuarantineMessage](http://technet.microsoft.com/library/88026da1-8dbc-49e7-80e8-112a32773c34.aspx) cmdlet to search for quarantined messages for a specific domain (for example, contoso.com):</span></span> 
  
```
Get-QuarantineMessage | ? {$_.Senderaddress -like "*@contoso.com"}
```

<span data-ttu-id="b1bc1-p111">Les résultats peuvent être transmis à la cmdlet [Release-QuarantineMessage](http://technet.microsoft.com/library/4a3aa05c-238f-46f2-b8dd-b0e3c38eab3e.aspx). Incluez le paramètre -ReleaseToAll pour débloquer le message et l'envoyer à tous ses destinataires. Une fois qu'un message est débloqué, il ne peut plus l'être de nouveau.</span><span class="sxs-lookup"><span data-stu-id="b1bc1-p111">The results can be passed to the [Release-QuarantineMessage](http://technet.microsoft.com/library/4a3aa05c-238f-46f2-b8dd-b0e3c38eab3e.aspx) cmdlet. Include the -ReleaseToAll parameter to release the message to all recipients. Once a message is released, it can't be released again.</span></span> 
  
```
Get-QuarantineMessage | ? {$_.Senderaddress -like "*@contoso.com"}
```


