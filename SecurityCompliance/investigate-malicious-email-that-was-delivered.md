---
title: Rechercher et identifier les courriers électroniques malveillants remis (Office 365 Threat Investigation and Response
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/19/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 8f54cd33-4af7-4d1b-b800-68f8818e5b2a
ms.collection:
- M365-security-compliance
description: Découvrez comment utiliser les fonctionnalités d’analyse et de réponse aux menaces pour rechercher et examiner des courriers électroniques malveillants.
ms.openlocfilehash: febcf6704b1ba9dc23bf4e698715fb4b929b998b
ms.sourcegitcommit: d3b2bffa8af5f19d97fe9771068c80705b890e85
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/01/2019
ms.locfileid: "35414804"
---
# <a name="find-and-investigate-malicious-email-that-was-delivered-office-365-advanced-threat-protection-plan-2"></a><span data-ttu-id="a3395-103">Rechercher et identifier les messages électroniques malveillants qui ont été remis (Office 365 Advanced Threat Protection Plan 2)</span><span class="sxs-lookup"><span data-stu-id="a3395-103">Find and investigate malicious email that was delivered (Office 365 Advanced Threat Protection Plan 2)</span></span>

<span data-ttu-id="a3395-104">[Office 365 Advanced Threat Protection](office-365-atp.md) vous permet d’examiner les activités qui permettent aux utilisateurs de protéger votre organisation.</span><span class="sxs-lookup"><span data-stu-id="a3395-104">[Office 365 Advanced Threat Protection](office-365-atp.md) lets you to investigate activities that put your users at risk and take action to protect your organization.</span></span> <span data-ttu-id="a3395-105">Par exemple, si vous participez à l’équipe de sécurité de votre organisation, vous pouvez rechercher et enquêter sur les messages électroniques suspects qui ont été remis à vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="a3395-105">For example, if you are part of your organization's security team, you can find and investigate suspicious email messages that were delivered to your users.</span></span> <span data-ttu-id="a3395-106">Vous pouvez le faire à l’aide de l' [Explorateur de menaces (ou des détections en temps réel)](threat-explorer.md).</span><span class="sxs-lookup"><span data-stu-id="a3395-106">You can do this by using [Threat Explorer (or real-time detections)](threat-explorer.md).</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="a3395-107">Avant de commencer...</span><span class="sxs-lookup"><span data-stu-id="a3395-107">Before you begin...</span></span>

<span data-ttu-id="a3395-108">Assurez-vous que les conditions suivantes sont remplies :</span><span class="sxs-lookup"><span data-stu-id="a3395-108">Make sure that the following requirements are met:</span></span>
  
- <span data-ttu-id="a3395-109">Votre organisation a [Office 365 Advanced Threat Protection](office-365-atp.md) (plan 1 ou plan 2) et des [licences sont attribuées à des utilisateurs](https://docs.microsoft.com/en-us/office365/admin/subscriptions-and-billing/assign-licenses-to-users).</span><span class="sxs-lookup"><span data-stu-id="a3395-109">Your organization has [Office 365 Advanced Threat Protection](office-365-atp.md) (Plan 1 or Plan 2) and [licenses are assigned to users](https://docs.microsoft.com/en-us/office365/admin/subscriptions-and-billing/assign-licenses-to-users).</span></span>
    
- <span data-ttu-id="a3395-110">La [journalisation d’audit Office 365](turn-audit-log-search-on-or-off.md) est activée pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="a3395-110">[Office 365 audit logging](turn-audit-log-search-on-or-off.md) is turned on for your organization.</span></span> 
    
- <span data-ttu-id="a3395-111">Votre organisation a défini des stratégies pour le blocage du courrier indésirable, anti-programme malveillant, anti-hameçonnage, etc.</span><span class="sxs-lookup"><span data-stu-id="a3395-111">Your organization has policies defined for anti-spam, anti-malware, anti-phishing, and so on.</span></span> <span data-ttu-id="a3395-112">Consultez la rubrique Protégez-vous [contre les menaces dans Office 365](protect-against-threats.md).</span><span class="sxs-lookup"><span data-stu-id="a3395-112">See [Protect against threats in Office 365](protect-against-threats.md).</span></span>
    
- <span data-ttu-id="a3395-113">Vous êtes un administrateur général Office 365 ou vous avez l’administrateur de sécurité ou le rôle de recherche et de purge affecté dans le centre &amp; de sécurité et de conformité.</span><span class="sxs-lookup"><span data-stu-id="a3395-113">You are an Office 365 global administrator, or you have either the Security Administrator or the Search and Purge role assigned in the Security &amp; Compliance Center.</span></span> <span data-ttu-id="a3395-114">Consultez [la rubrique autorisations dans le centre &amp; de sécurité conformité Office 365](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="a3395-114">See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
    
## <a name="dealing-with-suspicious-emails"></a><span data-ttu-id="a3395-115">Traitement des e-mails suspects</span><span class="sxs-lookup"><span data-stu-id="a3395-115">Dealing with suspicious emails</span></span>

<span data-ttu-id="a3395-116">Les utilisateurs malveillants peuvent envoyer des courriers électroniques à vos utilisateurs pour essayer d’envoyer leurs informations d’identification et accéder à vos secrets d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="a3395-116">Malicious attackers may be sending mail to your users to try and phish their credentials and gain access to your corporate secrets!</span></span> <span data-ttu-id="a3395-117">Pour éviter cela, vous devez utiliser les services de protection contre les menaces dans Office 365, y compris [Exchange Online Protection](eop/exchange-online-protection-overview.md) et [Advanced Threat Protection](office-365-atp.md).</span><span class="sxs-lookup"><span data-stu-id="a3395-117">To prevent this, you should use the threat protection services in Office 365, including [Exchange Online Protection](eop/exchange-online-protection-overview.md) and [Advanced Threat Protection](office-365-atp.md).</span></span> <span data-ttu-id="a3395-118">Toutefois, il arrive qu’un agresseur puisse envoyer un message électronique à vos utilisateurs contenant une URL et, par la suite, faire pointer cette URL vers du contenu malveillant (programmes malveillants, etc.).</span><span class="sxs-lookup"><span data-stu-id="a3395-118">However, there are times when an attacker could send mail to your users containing a URL and only later on make that URL point to malicious content (malware, etc.).</span></span> <span data-ttu-id="a3395-119">Par ailleurs, vous pouvez vous rendre compte que l’utilisateur de votre organisation a été compromis et que, pendant qu’il a été compromis, un utilisateur malveillant a utilisé ce compte pour envoyer des courriers électroniques à d’autres utilisateurs de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="a3395-119">Alternately, you may realize too late that a user in your organization has been compromised, and while that user was compromised, an attacker used that account to send email to other users in your company.</span></span> <span data-ttu-id="a3395-120">Dans le cadre du nettoyage de ces deux scénarios, vous souhaiterez peut-être supprimer les messages électroniques des boîtes de réception des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="a3395-120">As part of cleaning up both of these scenarios, you may want to remove email messages from user inboxes.</span></span> <span data-ttu-id="a3395-121">Dans ce cas, vous pouvez utiliser l' [Explorateur de menaces (ou les détections en temps réel)](threat-explorer.md) pour rechercher et supprimer ces messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="a3395-121">In situations like these, you can leverage [Threat Explorer (or real-time detections)](threat-explorer.md) to find and remove those email messages!</span></span>

## <a name="where-re-routed-emails-are-located-after-actions-are-taken"></a><span data-ttu-id="a3395-122">Où se trouvent les messages électroniques reroutés une fois les actions effectuées</span><span class="sxs-lookup"><span data-stu-id="a3395-122">Where re-routed emails are located after actions are taken</span></span>

<span data-ttu-id="a3395-123">L’Explorateur de menaces les détections en temps réel ont ajouté les champs de l’action de remise et de l’emplacement de remise au lieu de l’état de remise.</span><span class="sxs-lookup"><span data-stu-id="a3395-123">Threat Explorer real-time detections has added the Delivery Action and Delivery Location fields in the place of Delivery Status.</span></span> <span data-ttu-id="a3395-124">Cela a pour effet d’obtenir une image plus complète de l’emplacement de vos courriers électroniques.</span><span class="sxs-lookup"><span data-stu-id="a3395-124">This results in a more complete picture of where your emails land.</span></span> <span data-ttu-id="a3395-125">Une partie de cette modification est de faciliter la chasse aux personnes qui effectuent des opérations de sécurité, mais le résultat net est de savoir en un clin d’œil l’emplacement des messages électroniques problématiques.</span><span class="sxs-lookup"><span data-stu-id="a3395-125">Part of the goal of this change is to make hunting easier for Security Ops people, but the net result is knowing the location of problem emails at a glance.</span></span>

<span data-ttu-id="a3395-126">L’état de remise est désormais divisé en deux colonnes:</span><span class="sxs-lookup"><span data-stu-id="a3395-126">Delivery Status is now broken out into two columns:</span></span>

- <span data-ttu-id="a3395-127">**Action de remise** : quel est le statut de ce courrier électronique?</span><span class="sxs-lookup"><span data-stu-id="a3395-127">**Delivery Action** - What is the status of this email?</span></span>
- <span data-ttu-id="a3395-128">**Emplacement de remise** : où ce message électronique a-t-il été routé?</span><span class="sxs-lookup"><span data-stu-id="a3395-128">**Delivery Location** - Where was this email routed as a result?</span></span>

<span data-ttu-id="a3395-129">L’action de remise est l’action entreprise sur un courrier électronique en raison de stratégies ou de détections existantes.</span><span class="sxs-lookup"><span data-stu-id="a3395-129">Delivery Action is the action taken on an email due to existing policies or detections.</span></span> <span data-ttu-id="a3395-130">Voici les actions possibles qu’un courrier électronique peut effectuer:</span><span class="sxs-lookup"><span data-stu-id="a3395-130">Here are the possible actions an email can take:</span></span>

1. <span data-ttu-id="a3395-131">**Remis** : le courrier électronique a été remis à la boîte de réception ou au dossier d’un utilisateur et l’utilisateur peut y accéder directement.</span><span class="sxs-lookup"><span data-stu-id="a3395-131">**Delivered** – email was delivered to inbox or folder of a user and the user can directly access it.</span></span>
2. <span data-ttu-id="a3395-132">**Courrier** indésirable – le courrier électronique a été envoyé vers le dossier de courrier indésirable de l’utilisateur ou le dossier supprimé, et l’utilisateur a accès aux courriers électroniques dans son dossier de courrier indésirable ou supprimé.</span><span class="sxs-lookup"><span data-stu-id="a3395-132">**Junked** – email was sent to either user’s junk folder or deleted folder, and the user has access to emails in their Junk or Deleted folder.</span></span>
3. <span data-ttu-id="a3395-133">**Bloqué** : tous les messages électroniques mis en quarantaine, qui ont échoué ou qui ont été supprimés.</span><span class="sxs-lookup"><span data-stu-id="a3395-133">**Blocked** – any emails that's quarantined, that  failed, or was dropped.</span></span> <span data-ttu-id="a3395-134">Cette inaccessibilité est entièrement inaccessible par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a3395-134">This is completely inaccessible by the user!</span></span>
4. <span data-ttu-id="a3395-135">**Remplacé** : tout message électronique où des pièces jointes malveillantes sont remplacées par des fichiers. txt qui indiquent que la pièce jointe était malveillante.</span><span class="sxs-lookup"><span data-stu-id="a3395-135">**Replaced** – any email where malicious attachments are replaced by .txt files that state the attachment was malicious.</span></span>
 
<span data-ttu-id="a3395-136">Emplacement de remise: affiche les résultats des stratégies et des détections qui exécutent une post-remise.</span><span class="sxs-lookup"><span data-stu-id="a3395-136">Delivery location shows the results of policies and detections that run post-delivery.</span></span> <span data-ttu-id="a3395-137">Elle est liée à une action de remise.</span><span class="sxs-lookup"><span data-stu-id="a3395-137">It's linked to a Delivery Action.</span></span> <span data-ttu-id="a3395-138">Ce champ a été ajouté pour permettre de mieux comprendre l’action entreprise lors de la détection d’un message problématique.</span><span class="sxs-lookup"><span data-stu-id="a3395-138">This field was added to give insight into the action taken when a problem mail is found.</span></span> <span data-ttu-id="a3395-139">Voici les valeurs possibles de l’emplacement de remise:</span><span class="sxs-lookup"><span data-stu-id="a3395-139">Here are the possible values of delivery location:</span></span>

1. <span data-ttu-id="a3395-140">**Boîte de réception ou dossier** : le courrier électronique se trouve dans la boîte de réception ou dans un dossier (en fonction de vos règles de messagerie électronique).</span><span class="sxs-lookup"><span data-stu-id="a3395-140">**Inbox or folder** – The email is in inbox or a folder (according to your email rules).</span></span>
2. <span data-ttu-id="a3395-141">**Local ou externe** : la boîte aux lettres n’existe pas sur le Cloud, mais elle est locale.</span><span class="sxs-lookup"><span data-stu-id="a3395-141">**On-prem or external** – The mailbox doesn’t exist on cloud but is on -premises.</span></span>
3. <span data-ttu-id="a3395-142">**Dossier courrier** indésirable – courrier électronique dans le dossier courrier indésirable d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a3395-142">**Junk folder** – The email in in the Junk folder of a user.</span></span>
4. <span data-ttu-id="a3395-143">**Dossier éléments supprimés** : le courrier électronique dans le dossier éléments supprimés d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a3395-143">**Deleted items folder** – The email in the Deleted items folder of a user.</span></span>
5. <span data-ttu-id="a3395-144">**Quarantaine** : message en quarantaine et absent de la boîte aux lettres d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a3395-144">**Quarantine** – The email in quarantine, and is not in a user’s mailbox.</span></span>
6. <span data-ttu-id="a3395-145">**Échec** : la messagerie n’a pas pu atteindre la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="a3395-145">**Failed** – The email failed to reach the mailbox.</span></span>
7. <span data-ttu-id="a3395-146">**Ignoré** : le courrier électronique est perdu dans le flux de messagerie.</span><span class="sxs-lookup"><span data-stu-id="a3395-146">**Dropped** – The email gets lost somewhere in the Mailflow.</span></span>
  
## <a name="find-and-delete-suspicious-email-that-was-delivered"></a><span data-ttu-id="a3395-147">Rechercher et supprimer les e-mails suspects qui ont été remis</span><span class="sxs-lookup"><span data-stu-id="a3395-147">Find and delete suspicious email that was delivered</span></span>

> [!TIP]
> <span data-ttu-id="a3395-148">L’Explorateur de menaces (parfois appelé Explorateur) est un rapport puissant qui peut servir plusieurs objectifs, tels que la recherche et la suppression de messages, l’identification de l’adresse IP d’un expéditeur de courrier malveillant ou le démarrage d’un incident en vue d’une nouvelle enquête.</span><span class="sxs-lookup"><span data-stu-id="a3395-148">Threat Explorer (sometimes called Explorer), is a powerful report that can serve multiple purposes, such as finding and deleting messages, identifying the IP address of a malicious email sender, or starting an incident for further investigation.</span></span> <span data-ttu-id="a3395-149">La procédure suivante décrit l’utilisation de l’Explorateur pour rechercher et supprimer des courriers électroniques malveillants provenant de boîtes aux lettres de destinataires.</span><span class="sxs-lookup"><span data-stu-id="a3395-149">The following procedure focuses on using Explorer to find and delete malicious email from recipients mailboxes.</span></span>

<span data-ttu-id="a3395-150">Pour afficher les modifications apportées au champ d’état de remise précédent (à présent, action de remise et emplacement de remise):</span><span class="sxs-lookup"><span data-stu-id="a3395-150">To see the changes to the former Delivery Status field (now Delivery Action and Delivery Location):</span></span> 

1. <span data-ttu-id="a3395-151">Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous à l’aide de votre compte professionnel ou scolaire pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="a3395-151">Go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account for Office 365.</span></span> <span data-ttu-id="a3395-152">Vous accédez au centre de sécurité &amp; conformité.</span><span class="sxs-lookup"><span data-stu-id="a3395-152">This takes you to the Security &amp; Compliance Center.</span></span> 
    
2. <span data-ttu-id="a3395-153">Dans le volet de navigation de gauche, choisissez **Explorateur**de **gestion** \> des menaces.</span><span class="sxs-lookup"><span data-stu-id="a3395-153">In the left navigation, choose **Threat management** \> **Explorer**.</span></span>
<!--Comment>
![Threat Explorer with Delivery Action and Delivery Location fields.](media/ThreatExFields.PNG)

    
3. In the View menu, choose **All email**.<br/>![Use the View menu to choose between Email and Content reports](media/d39013ff-93b6-42f6-bee5-628895c251c2.png)
  
4. Notice the labels that appear in the report, such as **Delivered**, **Unknown**, or **Delivered to junk**.<br/>![Threat Explorer showing data for all email](media/208826ed-a85e-446f-b276-b5fdc312fbcb.png)<br/>(Depending on the actions that were taken on email messages for your organization, you might see additional labels, such as **Blocked** or **Replaced**.)
    
5. In the report, choose **Delivered** to view only emails that ended up in users' inboxes.<br/>![Clicking "Delivered to junk" removes that data from view](media/e6fb2e47-461e-4f6f-8c65-c331bd858758.png)
  
6. Below the chart, review the **Email** list below the chart.<br/>![Below the chart, view a list of email messages that were detected](media/dfb60590-1236-499d-97da-86c68621e2bc.png)
  
7. In the list, choose an item to view more details about that email message. For example, you can click the subject line to view information about the sender, recipients, attachments, and other similar email messages.<br/>![You can view additional information about an item, including details and any attachments](media/5a5707c3-d62a-4610-ae7b-900fff8708b2.png)
  
8. After viewing information about email messages, select one or more items in the list to activate **+ Actions**.
    
9. Use the **+ Actions** list to apply an action, such as **Move to deleted** items. This will delete the selected messages from the recipients' mailboxes.<br/>![When you select one or more email messages, you can choose from several available actions](media/ef12e10c-60a7-4f66-8f76-68d77ae26de1.png)
  
-->
## <a name="related-topics"></a><span data-ttu-id="a3395-154">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="a3395-154">Related topics</span></span>

[<span data-ttu-id="a3395-155">Plan 2 de protection avancée contre les menaces Office 365</span><span class="sxs-lookup"><span data-stu-id="a3395-155">Office 365 Advanced Threat Protection Plan 2</span></span>](office-365-ti.md)
  
[<span data-ttu-id="a3395-156">Se protéger contre les menaces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="a3395-156">Protect against threats in Office 365</span></span>](protect-against-threats.md)
  
[<span data-ttu-id="a3395-157">Afficher les rapports pour Office 365 protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="a3395-157">View reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)
  

