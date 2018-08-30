---
title: Utiliser des notifications de courrier indésirable d’utilisateur et signalement des messages mis en quarantaine dans Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/12/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 56de4ed5-b0aa-4195-9f46-033d7cc086bc
description: Si votre administrateur Active les notifications pour les utilisateurs, vous recevrez un message de notification qui répertorie les messages envoyés à votre boîte aux lettres qui ont été identifiés comme du courrier indésirable ou hameçonnage en bloc. Vous pouvez libérer ou signaler qu’après la notification.
ms.openlocfilehash: e355a94af5ac295503a8e205b1a896afc1c54fb6
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527848"
---
# <a name="use-user-spam-notifications-to-release-and-report-quarantined-messages-in-office-365"></a><span data-ttu-id="e0e03-104">Utiliser des notifications de courrier indésirable d’utilisateur et signalement des messages mis en quarantaine dans Office 365</span><span class="sxs-lookup"><span data-stu-id="e0e03-104">Use user spam notifications to release and report quarantined messages in Office 365</span></span>

<span data-ttu-id="e0e03-105">Si votre administrateur Active les notifications de courrier indésirable pour les utilisateurs, vous recevrez un message de notification qui répertorie les messages adressés à votre boîte aux lettres qui n’ont été identifiés comme courrier indésirable mis en quarantaine à la place.</span><span class="sxs-lookup"><span data-stu-id="e0e03-105">If your admin enables spam notifications for users, you'll receive a notification message that lists messages addressed to your mailbox that were identified as spam and quarantined instead.</span></span>
  
> [!TIP]
> <span data-ttu-id="e0e03-106">Si vous êtes administrateur et que vous souhaitez activer cette fonctionnalité, vous pouvez choisir l’option lorsque vous [modifiez une stratégie de blocage du courrier indésirable par défaut](https://go.microsoft.com/fwlink/?LinkId=800313).</span><span class="sxs-lookup"><span data-stu-id="e0e03-106">If you're an administrator and want to enable this feature, you can choose the option when you [modify a default anti-spam policy](https://go.microsoft.com/fwlink/?LinkId=800313).</span></span> 
  
<span data-ttu-id="e0e03-p102">Le message que vous recevez inclut le nombre de messages mis en quarantaine du courrier indésirable qu'avoir, la date et l’heure (en temps universel coordonné ou UTC) du dernier message dans la liste. La liste inclut les informations suivantes pour chaque message :</span><span class="sxs-lookup"><span data-stu-id="e0e03-p102">The message you receive includes the number of spam-quarantined messages you have, and the date and time (in Universal Coordinated Time or UTC) of the last message in the list. The list includes the following for each message:</span></span>
  
- <span data-ttu-id="e0e03-109">**Expéditeur** L’envoi nom et adresse électronique du message en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="e0e03-109">**Sender** The send name and email address of the quarantined message.</span></span> 
    
- <span data-ttu-id="e0e03-110">**Objet** Texte de l'objet du message en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="e0e03-110">**Subject** The subject line text of the quarantined message.</span></span> 
    
- <span data-ttu-id="e0e03-111">**Date** Date et heure (UTC) auxquelles le message a été mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="e0e03-111">**Date** The date and time (in UTC) that the message was quarantined.</span></span> 
    
- <span data-ttu-id="e0e03-112">**Taille** La taille du message, en kilo-octets (Ko).</span><span class="sxs-lookup"><span data-stu-id="e0e03-112">**Size** The size of the message, in kilobytes (KBs).</span></span> 
    
<span data-ttu-id="e0e03-113">Actuellement, il existe deux actions que vous pouvez entreprendre avec un message en quarantaine :</span><span class="sxs-lookup"><span data-stu-id="e0e03-113">Currently, there are two actions you can take with a quarantined message:</span></span>
  
- <span data-ttu-id="e0e03-114">**Version de la boîte de réception** Choisissez cette option pour envoyer le message vers votre boîte de réception, où vous pouvez l’afficher.</span><span class="sxs-lookup"><span data-stu-id="e0e03-114">**Release to Inbox** Choose this to send the message to your inbox, where you can view it.</span></span> 
    
- <span data-ttu-id="e0e03-p103">**Signaler comme légitime** Choisissez cette option pour envoyer une copie du message à Microsoft pour analyse. L’équipe du courrier indésirable évalue et analyse le message et, en fonction des résultats de l’analyse, ajuste les règles de filtrage de blocage du courrier indésirable pour autoriser le message.</span><span class="sxs-lookup"><span data-stu-id="e0e03-p103">**Report as Not Junk** Choose this to send a copy of the message to Microsoft for analysis. The spam team evaluates and analyzes the message, and, depending on the results of the analysis, adjusts the anti-spam filter rules to allow the message through.</span></span> 
    
<span data-ttu-id="e0e03-117">Prenez note des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="e0e03-117">Be aware of the following:</span></span>
  
- <span data-ttu-id="e0e03-p104">Messages mis en quarantaine car ils correspondant à une règle de flux de messagerie ne sont pas inclus dans les messages utilisateur mis en quarantaine. Seuls les messages mis en quarantaine du courrier indésirable sont répertoriés.</span><span class="sxs-lookup"><span data-stu-id="e0e03-p104">Messages that are quarantined because they matched a mail flow rule are not included in user quarantined messages. Only spam-quarantined messages are listed.</span></span>
    
- <span data-ttu-id="e0e03-120">Vous ne pouvez libérer un message et le signaler comme faux positif (légitime) qu'une fois.</span><span class="sxs-lookup"><span data-stu-id="e0e03-120">You can only release a message and report it as a false positive (not junk) once.</span></span>
    

