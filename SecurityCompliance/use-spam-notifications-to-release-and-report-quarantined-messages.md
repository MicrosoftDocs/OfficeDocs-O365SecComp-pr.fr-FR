---
title: Utilisation des notifications de courrier indésirable de l’utilisateur pour le déblocage et le signalement des messages de courrier indésirable mis en quarantaine dans Office 365
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 5/12/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 56de4ed5-b0aa-4195-9f46-033d7cc086bc
ms.collection:
- M365-security-compliance
description: Si votre administrateur Active les notifications pour les utilisateurs, vous recevrez un message de notification répertoriant les messages envoyés à votre boîte aux lettres identifiés comme courriers indésirables, en masse ou par hameçonnage. Vous pouvez publier ou signaler des messages après leur notification.
ms.openlocfilehash: 7f68b70298fca7d8ed5f5e5b8dc9c727c3a6a6c1
ms.sourcegitcommit: 5eb664b6ecef94aef4018a75684ee4ae66c486bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2019
ms.locfileid: "30492723"
---
# <a name="use-user-spam-notifications-to-release-and-report-quarantined-messages-in-office-365"></a><span data-ttu-id="7fcae-104">Utilisation des notifications de courrier indésirable de l’utilisateur pour le déblocage et le signalement des messages de courrier indésirable mis en quarantaine dans Office 365</span><span class="sxs-lookup"><span data-stu-id="7fcae-104">Use user spam notifications to release and report quarantined messages in Office 365</span></span>

<span data-ttu-id="7fcae-105">Si votre administrateur active des notifications de courrier indésirable pour les utilisateurs, vous recevrez un message de notification répertoriant les messages adressés à votre boîte aux lettres identifiés comme courrier indésirable et mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="7fcae-105">If your admin enables spam notifications for users, you'll receive a notification message that lists messages addressed to your mailbox that were identified as spam and quarantined instead.</span></span>
  
> [!TIP]
> <span data-ttu-id="7fcae-106">Si vous êtes administrateur et que vous souhaitez activer cette fonctionnalité, vous pouvez choisir l'option lorsque vous [modifiez une stratégie de blocage du courrier indésirable par défaut](https://go.microsoft.com/fwlink/?LinkId=800313).</span><span class="sxs-lookup"><span data-stu-id="7fcae-106">If you're an administrator and want to enable this feature, you can choose the option when you [modify a default anti-spam policy](https://go.microsoft.com/fwlink/?LinkId=800313).</span></span> 
  
<span data-ttu-id="7fcae-107">Le message que vous recevez inclut le nombre de messages indésirables mis en quarantaine que vous avez, ainsi que la date et l'heure (au format UTC ou UTC) du dernier message de la liste.</span><span class="sxs-lookup"><span data-stu-id="7fcae-107">The message you receive includes the number of spam-quarantined messages you have, and the date and time (in Universal Coordinated Time or UTC) of the last message in the list.</span></span> <span data-ttu-id="7fcae-108">La liste inclut les éléments suivants pour chaque message:</span><span class="sxs-lookup"><span data-stu-id="7fcae-108">The list includes the following for each message:</span></span>
  
- <span data-ttu-id="7fcae-109">**Expéditeur** Nom d'envoi et adresse de messagerie du message en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="7fcae-109">**Sender** The send name and email address of the quarantined message.</span></span> 
    
- <span data-ttu-id="7fcae-110">**Objet** Texte de l'objet du message en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="7fcae-110">**Subject** The subject line text of the quarantined message.</span></span> 
    
- <span data-ttu-id="7fcae-111">**Date** Date et heure (UTC) auxquelles le message a été mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="7fcae-111">**Date** The date and time (in UTC) that the message was quarantined.</span></span> 
    
- <span data-ttu-id="7fcae-112">**Taille** Taille du message, en kilo-octets (Ko).</span><span class="sxs-lookup"><span data-stu-id="7fcae-112">**Size** The size of the message, in kilobytes (KBs).</span></span> 
    
<span data-ttu-id="7fcae-113">Actuellement, il existe deux actions que vous pouvez effectuer avec un message en quarantaine:</span><span class="sxs-lookup"><span data-stu-id="7fcae-113">Currently, there are two actions you can take with a quarantined message:</span></span>
  
- <span data-ttu-id="7fcae-114">**Publier dans la boîte de réception** Choisissez cette adresse pour envoyer le message vers votre boîte de réception, où vous pouvez l'afficher.</span><span class="sxs-lookup"><span data-stu-id="7fcae-114">**Release to Inbox** Choose this to send the message to your inbox, where you can view it.</span></span> 
    
- <span data-ttu-id="7fcae-115">**Signaler comme légitime** Choisissez cette adresse pour envoyer une copie du message à Microsoft pour analyse.</span><span class="sxs-lookup"><span data-stu-id="7fcae-115">**Report as Not Junk** Choose this to send a copy of the message to Microsoft for analysis.</span></span> <span data-ttu-id="7fcae-116">L'équipe du courrier indésirable évalue et analyse le message, puis, selon les résultats de l'analyse, adapte les règles de filtre de courrier indésirable pour autoriser le message.</span><span class="sxs-lookup"><span data-stu-id="7fcae-116">The spam team evaluates and analyzes the message, and, depending on the results of the analysis, adjusts the anti-spam filter rules to allow the message through.</span></span> 
    
<span data-ttu-id="7fcae-117">Prenez en considération ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="7fcae-117">Be aware of the following:</span></span>
  
- <span data-ttu-id="7fcae-118">Les messages mis en quarantaine, car ils correspondent à une règle de flux de messagerie, ne sont pas inclus dans les messages mis en quarantaine par l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7fcae-118">Messages that are quarantined because they matched a mail flow rule are not included in user quarantined messages.</span></span> <span data-ttu-id="7fcae-119">Seuls les messages mis en quarantaine car identifiés comme courrier indésirable sont répertoriés.</span><span class="sxs-lookup"><span data-stu-id="7fcae-119">Only spam-quarantined messages are listed.</span></span>
    
- <span data-ttu-id="7fcae-120">Vous ne pouvez libérer un message et le signaler comme faux positif (légitime) qu'une fois.</span><span class="sxs-lookup"><span data-stu-id="7fcae-120">You can only release a message and report it as a false positive (not junk) once.</span></span>
    

