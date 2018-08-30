---
title: Prendre en main la stratégie DLP par défaut
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/10/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: e0ada764-6422-4b44-9472-513bed04837b
description: Avant de créer même votre stratégie de protection contre la perte données premier, DLP contribue à protéger vos informations sensibles avec une stratégie par défaut. Cette stratégie par défaut et ses aident à protéger votre contenu sensible par pour vous avertir lorsque le numéro de carte de messagerie ou des documents contenant un crédit ont été partagé avec une personne extérieure à votre organisation recommandation (voir ci-dessous).
ms.openlocfilehash: 1b522a2c04e72353970ef5dfcd62183023a01994
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528765"
---
# <a name="get-started-with-the-default-dlp-policy"></a><span data-ttu-id="438c9-104">Prendre en main la stratégie DLP par défaut</span><span class="sxs-lookup"><span data-stu-id="438c9-104">Get started with the default DLP policy</span></span>

<span data-ttu-id="438c9-p102">Avant de créer même votre stratégie de protection contre la perte données premier, DLP contribue à protéger vos informations sensibles avec une stratégie par défaut. Cette stratégie par défaut et ses aident à protéger votre contenu sensible par pour vous avertir lorsque le numéro de carte de messagerie ou des documents contenant un crédit ont été partagé avec une personne extérieure à votre organisation recommandation (voir ci-dessous). Cette recommandation s’affiche sur la page **d’accueil** de la sécurité &amp; centre de conformité.</span><span class="sxs-lookup"><span data-stu-id="438c9-p102">Before you even create your first data loss prevention (DLP) policy, DLP is helping to protect your sensitive information with a default policy. This default policy and its recommendation (shown below) help keep your sensitive content secure by notifying you when email or documents containing a credit card number were shared with someone outside your organization. You'll see this recommendation on the **Home** page of the Security &amp; Compliance Center.</span></span> 
  
<span data-ttu-id="438c9-p103">Vous pouvez utiliser ce widget afficher rapidement quand et la quantité d’informations sensible a été partagée et puis affiner la stratégie DLP par défaut dans seulement un ou deux clics. Vous pouvez également modifier la stratégie DLP par défaut à tout moment, car elle est entièrement personnalisable. Notez que si vous ne voyez pas la recommandation en premier lieu, essayez de cliquer sur **+ plus** en bas de la section **recommandé pour vous** .</span><span class="sxs-lookup"><span data-stu-id="438c9-p103">You can use this widget to quickly view when and how much sensitive information was shared, and then refine the default DLP policy in just a click or two. You can also edit the default DLP policy at any time because it's fully customizable. Note that if you don't see the recommendation at first, try clicking **+More** at the bottom of the **Recommended for you** section.</span></span> 
  
![Widget nommé supplémentaires protéger le contenu partagé](media/2bae6dbc-cc92-4f35-b54c-c36e60226b5b.png)
  
## <a name="view-the-report-and-refine-the-default-dlp-policy"></a><span data-ttu-id="438c9-112">Afficher le rapport et affiner la stratégie DLP par défaut</span><span class="sxs-lookup"><span data-stu-id="438c9-112">View the report and refine the default DLP policy</span></span>

<span data-ttu-id="438c9-113">Lorsque le widget vous indique que les utilisateurs ont les informations sensibles partagées avec des personnes extérieures à votre organisation, choisissez **une stratégie DLP affiner** en bas.</span><span class="sxs-lookup"><span data-stu-id="438c9-113">When the widget shows you that users have shared sensitive information with people outside your organization, choose **Refine DLP policy** at the bottom.</span></span> 
  
<span data-ttu-id="438c9-p104">Le rapport détaillé vous indique quand et comment la quantité de contenu qui contient les numéros de carte de crédit a été partagée au cours des 30 derniers jours. Notez que les correspondances de règle peuvent prendre jusqu'à 48 heures s’affiche dans le widget.</span><span class="sxs-lookup"><span data-stu-id="438c9-p104">The detailed report shows you when and how much content containing credit card numbers was shared in the past 30 days. Note that rule matches can take up to 48 hours to show up in the widget.</span></span>
  
<span data-ttu-id="438c9-116">Pour protéger les informations sensibles, la stratégie DLP par défaut :</span><span class="sxs-lookup"><span data-stu-id="438c9-116">To help protect the sensitive information, the default DLP policy:</span></span>
  
- <span data-ttu-id="438c9-117">Détecte lorsque le contenu de Exchange, SharePoint et OneDrive qui contient au moins une carte de crédit est partagé avec des personnes extérieures à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="438c9-117">Detects when content in Exchange, SharePoint, and OneDrive that contains at least one credit card number is shared with people outside your organization.</span></span>
    
- <span data-ttu-id="438c9-p105">Affiche un Conseil de stratégie et envoie une notification par courrier électronique aux utilisateurs lorsqu’ils essaient de partager ces informations sensibles avec des personnes extérieures à votre organisation. Pour plus d’informations sur ces options, voir [Envoyer des notifications par courrier électronique et afficher les conseils de stratégie pour les stratégies DLP](use-notifications-and-policy-tips.md).</span><span class="sxs-lookup"><span data-stu-id="438c9-p105">Shows a policy tip and sends an email notification to users when they attempt to share this sensitive information with people outside your organization. For more information on these options, see [Send email notifications and show policy tips for DLP policies](use-notifications-and-policy-tips.md).</span></span>
    
- <span data-ttu-id="438c9-p106">Génère des rapports d’activité détaillées afin que vous pouvez suivre des éléments comme ayant le contenu partagé avec des personnes extérieures à votre organisation et lorsque que. Vous pouvez utiliser les [rapports DLP](view-the-dlp-reports.md) et [des données du journal d’audit](search-the-audit-log-in-security-and-compliance.md) (où **activité** = **DLP**) pour afficher ces informations.</span><span class="sxs-lookup"><span data-stu-id="438c9-p106">Generates detailed activity reports so that you can track things like who shared the content with people outside your organization and when they did it. You can use the [DLP reports](view-the-dlp-reports.md) and [audit log data](search-the-audit-log-in-security-and-compliance.md) (where **Activity** = **DLP**) to see this information.</span></span>
    
<span data-ttu-id="438c9-122">Pour affiner rapidement la stratégie DLP par défaut, vous pouvez choisir de façon à :</span><span class="sxs-lookup"><span data-stu-id="438c9-122">To quickly refine the default DLP policy, you can choose to have it:</span></span>
  
- <span data-ttu-id="438c9-123">Vous envoyer un message électronique de rapport d’incident lorsque les utilisateurs partagent ces informations sensibles avec des personnes extérieures à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="438c9-123">Send you an incident report email when users share this sensitive information with people outside your organization.</span></span>
    
- <span data-ttu-id="438c9-124">Ajouter d’autres utilisateurs pour le rapport d’incident e-mail.</span><span class="sxs-lookup"><span data-stu-id="438c9-124">Add other users to the email incident report.</span></span>
    
- <span data-ttu-id="438c9-125">Bloquez l’accès au contenu contenant les informations sensibles, mais autoriser l’utilisateur à remplacer et partager ou envoyer s’ils doivent.</span><span class="sxs-lookup"><span data-stu-id="438c9-125">Block access to the content containing the sensitive information, but allow the user to override and share or send if they need to.</span></span>
    
<span data-ttu-id="438c9-126">Pour plus d’informations sur les rapports d’incidents ou restriction de l’accès, voir [vue d’ensemble des stratégies de protection contre la perte de données](data-loss-prevention-policies.md).</span><span class="sxs-lookup"><span data-stu-id="438c9-126">For more information on incident reports or restricting access, see [Overview of data loss prevention policies](data-loss-prevention-policies.md).</span></span>
  
<span data-ttu-id="438c9-127">Si vous souhaitez modifier ces options ultérieurement, vous pouvez modifier la valeur par défaut la stratégie DLP à tout moment - voir la section suivante.</span><span class="sxs-lookup"><span data-stu-id="438c9-127">If you want to change these options later, you can edit the default DLP policy at any time - see the next section.</span></span>
  
![Paramètres widget nommé supplémentaires de protection du contenu partagé](media/dad30a84-2715-4c0a-a5c5-44d85492363e.png)
  
## <a name="edit-the-default-dlp-policy"></a><span data-ttu-id="438c9-129">Modifier la stratégie DLP par défaut</span><span class="sxs-lookup"><span data-stu-id="438c9-129">Edit the default DLP policy</span></span>

<span data-ttu-id="438c9-130">Cette stratégie est nommée **stratégie par défaut Office 365 DLP** et s’affiche sous la **prévention des pertes de données** dans la page **stratégie** de la sécurité &amp; centre de conformité.</span><span class="sxs-lookup"><span data-stu-id="438c9-130">This policy is named **Default Office 365 DLP policy** and appears under **Data loss prevention** on the **Policy** page of the Security &amp; Compliance Center.</span></span> 
  
<span data-ttu-id="438c9-p107">Cette stratégie est entièrement personnalisable, identique à toute stratégie DLP que vous avez créés à partir de zéro. Vous pouvez également désactiver ou supprimer la stratégie, afin que vos utilisateurs ne peuvent plus recevoir des conseils de stratégie ou les notifications de messagerie.</span><span class="sxs-lookup"><span data-stu-id="438c9-p107">This policy is fully customizable, the same as any DLP policy that you create yourself from scratch. You can also turn off or delete the policy, so that your users no longer receive policy tips or email notifications.</span></span>
  
![Stratégie DLP nommée stratégie par défaut Office 365 DLP](media/260731e8-4d57-4c98-abec-07b052ec48d5.png)
  
## <a name="when-the-widget-does-and-does-not-appear"></a><span data-ttu-id="438c9-134">Lorsque le widget et n’apparaît pas</span><span class="sxs-lookup"><span data-stu-id="438c9-134">When the widget does and does not appear</span></span>

<span data-ttu-id="438c9-135">Le widget nommé **davantage protéger le contenu partagé** apparaît dans la section **recommandé pour vous** de la page **d’accueil** de la sécurité &amp; centre de conformité.</span><span class="sxs-lookup"><span data-stu-id="438c9-135">The widget named **Further protect shared content** appears in the **Recommended for you** section of the **Home** page of the Security &amp; Compliance Center.</span></span> 
  
<span data-ttu-id="438c9-136">Ce widget s’affiche uniquement lorsque :</span><span class="sxs-lookup"><span data-stu-id="438c9-136">This widget appears only when:</span></span>
  
- <span data-ttu-id="438c9-p108">Il n’existe aucune stratégies de prévention de perte de données de la sécurité &amp; centre de conformité ou le centre d’administration Exchange. Ce widget est destiné à vous aider à prendre en main DLP, elle n’apparaît pas si vous disposez déjà de stratégies DLP.</span><span class="sxs-lookup"><span data-stu-id="438c9-p108">There are no data loss prevention policies in the Security &amp; Compliance Center or Exchange Admin Center. This widget is intended to help you get started with DLP, so it doesn't appear if you already have DLP policies.</span></span>
    
- <span data-ttu-id="438c9-139">Contenu contenant au moins une carte de crédit a été partagé avec une personne extérieure à votre organisation au cours des 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="438c9-139">Content containing least one credit card has been shared with someone outside your organization in the past 30 days.</span></span>
    
<span data-ttu-id="438c9-140">Notez que les correspondances de règle peuvent prendre jusqu'à 48 heures soit disponible pour le widget, une fois que les informations sensibles partagées en externe sont détectées, elle peut prendre jusqu'à deux jours de la recommandation apparaisse.</span><span class="sxs-lookup"><span data-stu-id="438c9-140">Note that rule matches can take up to 48 hours to be available to the widget, so after sensitive information shared externally is detected, it may take up to two days for the recommendation to appear.</span></span>
  
<span data-ttu-id="438c9-141">Enfin, une fois que vous utilisez le widget pour affiner la stratégie DLP par défaut, le widget disparaît de la page **d’accueil** .</span><span class="sxs-lookup"><span data-stu-id="438c9-141">Finally, after you use the widget to refine the default DLP policy, the widget disappears from the **Home** page.</span></span> 
  

