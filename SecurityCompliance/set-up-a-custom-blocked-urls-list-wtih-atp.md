---
title: Configurer une liste d’URL bloquée personnalisée à l’aide d’Office 365 DAV fiables liens
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 5/30/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 896a7efb-1683-465e-a394-261349e5d866
description: Lisez cet article pour apprendre à configurer une liste d’URL bloqués pour votre organisation à l’aide d’Office 365 avancée protection contre les menaces. Les URL bloquées s’appliquera aux messages électroniques et des documents Office en fonction de vos stratégies de liens fiables DAV.
ms.openlocfilehash: cd1e7858c8929bf468b2a4d5e09ccde9d5adc7b1
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528146"
---
# <a name="set-up-a-custom-blocked-urls-list-using-office-365-atp-safe-links"></a><span data-ttu-id="8a17c-104">Configurer une liste d’URL bloquée personnalisée à l’aide d’Office 365 DAV fiables liens</span><span class="sxs-lookup"><span data-stu-id="8a17c-104">Set up a custom blocked URLs list using Office 365 ATP Safe Links</span></span>

<span data-ttu-id="8a17c-p102">Avec [Office 365 avancée protection contre les menaces](office-365-atp.md) (DAV), votre organisation peut avoir une liste personnalisée d’adresses de site Web (URL) qui sont bloqués. Lorsqu’une URL est bloquée, les personnes qui cliquent sur des liens vers l’URL bloqué sont dirigés vers une [page d’avertissement](atp-safe-links-warning-pages.md) qui ressemble à l’image suivante :</span><span class="sxs-lookup"><span data-stu-id="8a17c-p102">With [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP), your organization can have a custom list of website addresses (URLs) that are blocked. When a URL is blocked, people who click on links to the blocked URL are taken to a [warning page](atp-safe-links-warning-pages.md) that resembles the following image:</span></span> 
  
![Ce site est bloqué.](media/6b4bda2d-a1e6-419e-8b10-588e83c3af3f.png)
  
<span data-ttu-id="8a17c-108">La liste des URL bloquée est définie par l’équipe de sécurité de votre organisation Office 365, et cette liste s’applique à tout le monde dans l’organisation qui est couvert par les stratégies de liaisons sans échec de Office 365 DAV.</span><span class="sxs-lookup"><span data-stu-id="8a17c-108">The blocked URLs list is defined by your organization's Office 365 security team, and that list applies to everyone in the organization who is covered by Office 365 ATP Safe Links policies.</span></span> 
  
<span data-ttu-id="8a17c-109">Lisez cet article pour apprendre à configurer la liste des URL bloqué personnalisé de votre organisation pour les [Liens sécurisés DAV dans Office 365](atp-safe-links.md).</span><span class="sxs-lookup"><span data-stu-id="8a17c-109">Read this article to learn how to set up your organization's custom blocked URLs list for [ATP Safe Links in Office 365](atp-safe-links.md).</span></span>
  
## <a name="view-or-edit-a-custom-list-of-blocked-urls"></a><span data-ttu-id="8a17c-110">Afficher ou modifier une liste personnalisée d’URL bloquées</span><span class="sxs-lookup"><span data-stu-id="8a17c-110">View or edit a custom list of blocked URLs</span></span>

<span data-ttu-id="8a17c-p103">[Liens approuvés DAV dans Office 365](atp-safe-links.md) utilise plusieurs listes, y compris la liste des URL bloqué personnalisé de votre organisation. Si vous disposez des autorisations nécessaires, vous pouvez configurer la liste personnalisée de votre organisation. Pour cela, en modifiant la stratégie de liens fiables par défaut de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8a17c-p103">[ATP Safe Links in Office 365](atp-safe-links.md) uses several lists, including your organization's custom blocked URLs list. If you have the necessary permissions, you can set up your organization's custom list. You do this by editing your organization's default Safe Links policy.</span></span>
  
1. <span data-ttu-id="8a17c-114">Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous avec votre compte professionnel ou de l’école.</span><span class="sxs-lookup"><span data-stu-id="8a17c-114">Go to [https://protection.office.com](https://protection.office.com) and sign in with your work or school account.</span></span> 
    
2. <span data-ttu-id="8a17c-115">Dans la navigation de gauche, sous **Gestion des menaces**, choisissez **stratégie** \> **Liens fiables**.</span><span class="sxs-lookup"><span data-stu-id="8a17c-115">In the left navigation, under **Threat management**, choose **Policy** \> **Safe Links**.</span></span>
    
3. <span data-ttu-id="8a17c-116">Dans la section **stratégies qui s’appliquent à toute l’organisation** , sélectionnez **par défaut**, puis choisissez **Modifier** (le bouton Modifier ressemble à un crayon).</span><span class="sxs-lookup"><span data-stu-id="8a17c-116">In the **Policies that apply to the entire organization** section, select **Default**, and then choose **Edit** (the Edit button resembles a pencil).</span></span> 
    
    ![Cliquez sur Modifier pour modifier votre stratégie par défaut pour la protection des liens fiables](media/d08f9615-d947-4033-813a-d310ec2c8cca.png)
  
    <span data-ttu-id="8a17c-p104">C’est là vous permet d’afficher la liste des URL bloquées. Notez que dans un premier temps, vous n’avez aucune URL répertoriées.</span><span class="sxs-lookup"><span data-stu-id="8a17c-p104">This is where you go to view your list of blocked URLs. Note that at first, you won't have any URLs listed.</span></span>
    
    ![La liste des URL bloqués est par défaut stratégie liens fiables qui s’applique à toute votre organisation.](media/575e1449-6191-40ac-b626-030a2fd3fb11.png)
  
4. <span data-ttu-id="8a17c-p105">Sélectionnez la zone **Tapez une URL valide** et tapez une URL, puis cliquez sur le signe plus (+). Voici quelques points à prendre en compte :</span><span class="sxs-lookup"><span data-stu-id="8a17c-p105">Select the **Enter a valid URL** box, and then type a URL, and then choose the plus sign (+). Here are a few things to keep in mind:</span></span> 
    
  - <span data-ttu-id="8a17c-p106">Vous pouvez spécifier une URL de domaine (comme `contoso.com` ou `tailspintoys.com`). Cela empêchera clics sur n’importe quelle URL qui contient le domaine.</span><span class="sxs-lookup"><span data-stu-id="8a17c-p106">You can specify a domain-only URL (like `contoso.com` or `tailspintoys.com`). This will block clicks on any URL that contains the domain.</span></span>
    
  - <span data-ttu-id="8a17c-p107">N’incluez pas une barre oblique ( **/**) à la fin de l’URL. Par exemple, au lieu de saisir `http://www.contoso.com/`, entrez `http://www.contoso.com`.</span><span class="sxs-lookup"><span data-stu-id="8a17c-p107">Do not include a forward slash ( **/**) at the end of the URL. For example, instead of entering `http://www.contoso.com/`, enter `http://www.contoso.com`.</span></span>
    
  - <span data-ttu-id="8a17c-p108">Vous pouvez inclure jusqu'à trois astérisques générique (\*) par l’URL. Le tableau suivant répertorie quelques exemples de ce que vous pouvez entrer et les effets que ces entrées ont.</span><span class="sxs-lookup"><span data-stu-id="8a17c-p108">You can include up to three wildcard asterisks (\*) per URL. The following table lists some examples of what you can enter and what effect those entries have.</span></span>
    
|<span data-ttu-id="8a17c-129">**Exemple d’entrée**</span><span class="sxs-lookup"><span data-stu-id="8a17c-129">**Example Entry**</span></span>|<span data-ttu-id="8a17c-130">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="8a17c-130">**What It Does**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8a17c-131">`contoso.com`ou`\*contoso.com\*`</span><span class="sxs-lookup"><span data-stu-id="8a17c-131">`contoso.com` or `\*contoso.com\*`</span></span>  <br/> |<span data-ttu-id="8a17c-132">Bloque le domaine, les sous-domaines et les chemins d’accès, tel que `https://www.contoso.com`, `http://sub.contoso.com`, et`http://contoso.com/abc`</span><span class="sxs-lookup"><span data-stu-id="8a17c-132">Blocks the domain, subdomains, and paths, such as `https://www.contoso.com`, `http://sub.contoso.com`, and `http://contoso.com/abc`</span></span>  <br/> |
|`http://contoso.com/a`  <br/> |<span data-ttu-id="8a17c-133">Bloque un site `http://contoso.com/a` mais pas les autres sections`http://contoso.com/a/b`</span><span class="sxs-lookup"><span data-stu-id="8a17c-133">Blocks a site `http://contoso.com/a` but not additional subpaths like `http://contoso.com/a/b`</span></span>  <br/> |
|`http://contoso.com/a\*`  <br/> |<span data-ttu-id="8a17c-134">Bloque un site `http://contoso.com/a` et sections supplémentaires`http://contoso.com/a/b`</span><span class="sxs-lookup"><span data-stu-id="8a17c-134">Blocks a site `http://contoso.com/a` and additional subpaths like `http://contoso.com/a/b`</span></span>  <br/> |
   
5. <span data-ttu-id="8a17c-135">Lorsque vous avez terminé d’ajouter des URL, dans le coin inférieur droit de l’écran, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="8a17c-135">When you are finished adding URLs, in the lower right corner of the screen, choose **Save**.</span></span>
    
## <a name="what-if-i-want-to-define-exceptions-for-certain-users-in-my-organization"></a><span data-ttu-id="8a17c-136">Que se passe-t-il si je souhaite définir des exceptions pour certains utilisateurs au sein de mon organisation ?</span><span class="sxs-lookup"><span data-stu-id="8a17c-136">What if I want to define exceptions for certain users in my organization?</span></span>

<span data-ttu-id="8a17c-p109">Si vous souhaitez que certains groupes pour être en mesure d’afficher les URL qui peuvent être bloquées pour d’autres personnes, vous pouvez spécifier une stratégie de liens fiables DAV qui s’applique à des destinataires spécifiques. Voir [configurer une liste d’URL personnalisée du « pas de rewrite » à l’aide de liens fiables DAV](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).</span><span class="sxs-lookup"><span data-stu-id="8a17c-p109">If you want certain groups to be able to view URLs that might be blocked for others, you can specify an ATP Safe Links policy that applies to specific recipients. See [Set up a custom "do not rewrite" URLs list using ATP Safe Links](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="8a17c-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a17c-139">Related topics</span></span>

[<span data-ttu-id="8a17c-140">Protection de Microsoft Office 365 menace avancées</span><span class="sxs-lookup"><span data-stu-id="8a17c-140">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  
[<span data-ttu-id="8a17c-141">Liens DAV Safe dans Office 365</span><span class="sxs-lookup"><span data-stu-id="8a17c-141">ATP Safe Links in Office 365</span></span>](atp-safe-links.md)
  
[<span data-ttu-id="8a17c-142">Définir des stratégies de liens fiables DAV dans Office 365</span><span class="sxs-lookup"><span data-stu-id="8a17c-142">Set up ATP Safe Links policies in Office 365</span></span>](set-up-atp-safe-links-policies.md)
  
[<span data-ttu-id="8a17c-143">Pièces jointes DAV Safe dans Office 365</span><span class="sxs-lookup"><span data-stu-id="8a17c-143">ATP Safe Attachments in Office 365</span></span>](atp-safe-attachments.md)

[<span data-ttu-id="8a17c-144">Autorisations de sécurité Office 365 &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="8a17c-144">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
  

