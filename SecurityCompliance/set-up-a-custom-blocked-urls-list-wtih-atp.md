---
title: Configurer une liste d’URL bloquée personnalisée à l’aide d’Office 365 DAV fiables liens
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 896a7efb-1683-465e-a394-261349e5d866
description: Lisez cet article pour apprendre à configurer une liste d’URL bloqués pour votre organisation à l’aide d’Office 365 avancée protection contre les menaces. Les URL bloquées s’appliquera aux messages électroniques et des documents Office en fonction de vos stratégies de liens fiables DAV.
ms.openlocfilehash: cd17fe61b7ecd5becd0918323952f304a73a4ce0
ms.sourcegitcommit: 2cf7f5bb282c971d33e00f65d9982a3f14aec74e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/27/2018
ms.locfileid: "26706208"
---
# <a name="set-up-a-custom-blocked-urls-list-using-office-365-atp-safe-links"></a><span data-ttu-id="b49b1-104">Configurer une liste d’URL bloquée personnalisée à l’aide d’Office 365 DAV fiables liens</span><span class="sxs-lookup"><span data-stu-id="b49b1-104">Set up a custom blocked URLs list using Office 365 ATP Safe Links</span></span>

<span data-ttu-id="b49b1-p102">Avec [Office 365 avancée protection contre les menaces](office-365-atp.md) (DAV), votre organisation peut avoir une liste personnalisée d’adresses de site Web (URL) qui sont bloqués. Lorsqu’une URL est bloquée, les personnes qui cliquent sur des liens vers l’URL bloqué sont dirigés vers une [page d’avertissement](atp-safe-links-warning-pages.md) qui ressemble à l’image suivante :</span><span class="sxs-lookup"><span data-stu-id="b49b1-p102">With [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP), your organization can have a custom list of website addresses (URLs) that are blocked. When a URL is blocked, people who click on links to the blocked URL are taken to a [warning page](atp-safe-links-warning-pages.md) that resembles the following image:</span></span> 
  
![Ce site est bloqué.](media/6b4bda2d-a1e6-419e-8b10-588e83c3af3f.png)
  
<span data-ttu-id="b49b1-108">La liste des URL bloquée est définie par l’équipe de sécurité de votre organisation Office 365, et cette liste s’applique à tout le monde dans l’organisation qui est couvert par les stratégies de liaisons sans échec de Office 365 DAV.</span><span class="sxs-lookup"><span data-stu-id="b49b1-108">The blocked URLs list is defined by your organization's Office 365 security team, and that list applies to everyone in the organization who is covered by Office 365 ATP Safe Links policies.</span></span> 
  
<span data-ttu-id="b49b1-109">Lisez cet article pour apprendre à configurer la liste des URL bloqué personnalisé de votre organisation pour les [Liens sécurisés DAV dans Office 365](atp-safe-links.md).</span><span class="sxs-lookup"><span data-stu-id="b49b1-109">Read this article to learn how to set up your organization's custom blocked URLs list for [ATP Safe Links in Office 365](atp-safe-links.md).</span></span>
  
## <a name="view-or-edit-a-custom-list-of-blocked-urls"></a><span data-ttu-id="b49b1-110">Afficher ou modifier une liste personnalisée d’URL bloquées</span><span class="sxs-lookup"><span data-stu-id="b49b1-110">View or edit a custom list of blocked URLs</span></span>

<span data-ttu-id="b49b1-p103">[Liens approuvés DAV dans Office 365](atp-safe-links.md) utilise plusieurs listes, y compris la liste des URL bloqué personnalisé de votre organisation. Si vous disposez des autorisations nécessaires, vous pouvez configurer la liste personnalisée de votre organisation. Pour cela, en modifiant la stratégie de liens fiables par défaut de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b49b1-p103">[ATP Safe Links in Office 365](atp-safe-links.md) uses several lists, including your organization's custom blocked URLs list. If you have the necessary permissions, you can set up your organization's custom list. You do this by editing your organization's default Safe Links policy.</span></span>
  
1. <span data-ttu-id="b49b1-114">Accédez à [https://security.microsoft.com](https://security.microsoft.com) et connectez-vous avec votre compte professionnel ou de l’école.</span><span class="sxs-lookup"><span data-stu-id="b49b1-114">Go to [https://security.microsoft.com](https://security.microsoft.com) and sign in with your work or school account.</span></span> 
    
2. <span data-ttu-id="b49b1-115">Dans la navigation de gauche, sous **Gestion des menaces**, choisissez **stratégie** \> **Liens fiables**.</span><span class="sxs-lookup"><span data-stu-id="b49b1-115">In the left navigation, under **Threat management**, choose **Policy** \> **Safe Links**.</span></span>
    
3. <span data-ttu-id="b49b1-116">Dans la section **stratégies qui s’appliquent à toute l’organisation** , sélectionnez **par défaut**, puis choisissez **Modifier** (le bouton Modifier ressemble à un crayon).</span><span class="sxs-lookup"><span data-stu-id="b49b1-116">In the **Policies that apply to the entire organization** section, select **Default**, and then choose **Edit** (the Edit button resembles a pencil).</span></span><br/><span data-ttu-id="b49b1-117">![Cliquez sur Modifier pour modifier votre stratégie par défaut pour la protection des liens fiables](media/d08f9615-d947-4033-813a-d310ec2c8cca.png)</span><span class="sxs-lookup"><span data-stu-id="b49b1-117">![Click Edit to edit your default policy for Safe Links protection](media/d08f9615-d947-4033-813a-d310ec2c8cca.png)</span></span><br/><span data-ttu-id="b49b1-p104">C’est là vous permet d’afficher la liste des URL bloquées. Notez que dans un premier temps, vous n’avez aucune URL répertoriées.</span><span class="sxs-lookup"><span data-stu-id="b49b1-p104">This is where you go to view your list of blocked URLs. Note that at first, you won't have any URLs listed.</span></span><br/><span data-ttu-id="b49b1-120">![La liste des URL bloqués est par défaut stratégie liens fiables qui s’applique à toute votre organisation.](media/575e1449-6191-40ac-b626-030a2fd3fb11.png)</span><span class="sxs-lookup"><span data-stu-id="b49b1-120">![The Blocked URLs list is in the default Safe Links policy that applies to your entire organization.](media/575e1449-6191-40ac-b626-030a2fd3fb11.png)</span></span>
  
4. <span data-ttu-id="b49b1-p105">Sélectionnez la zone **Tapez une URL valide** et tapez une URL, puis cliquez sur le signe plus (+). Voici quelques points à prendre en compte :</span><span class="sxs-lookup"><span data-stu-id="b49b1-p105">Select the **Enter a valid URL** box, and then type a URL, and then choose the plus sign (+). Here are a few things to keep in mind:</span></span> 
    
  - <span data-ttu-id="b49b1-p106">Vous pouvez spécifier une URL de domaine (comme `contoso.com` ou `tailspintoys.com`). Cela empêchera clics sur n’importe quelle URL qui contient le domaine.</span><span class="sxs-lookup"><span data-stu-id="b49b1-p106">You can specify a domain-only URL (like `contoso.com` or `tailspintoys.com`). This will block clicks on any URL that contains the domain.</span></span>
    
  - <span data-ttu-id="b49b1-p107">N’incluez pas une barre oblique ( **/**) à la fin de l’URL. Par exemple, au lieu de saisir `http://www.contoso.com/`, entrez `http://www.contoso.com`.</span><span class="sxs-lookup"><span data-stu-id="b49b1-p107">Do not include a forward slash ( **/**) at the end of the URL. For example, instead of entering `http://www.contoso.com/`, enter `http://www.contoso.com`.</span></span>
    
  - <span data-ttu-id="b49b1-p108">Vous pouvez inclure jusqu'à trois astérisques générique (\*) par l’URL. Le tableau suivant répertorie quelques exemples de ce que vous pouvez entrer et les effets que ces entrées ont.</span><span class="sxs-lookup"><span data-stu-id="b49b1-p108">You can include up to three wildcard asterisks (\*) per URL. The following table lists some examples of what you can enter and what effect those entries have.</span></span>
    
|<span data-ttu-id="b49b1-129">**Exemple d’entrée**</span><span class="sxs-lookup"><span data-stu-id="b49b1-129">**Example Entry**</span></span>|<span data-ttu-id="b49b1-130">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="b49b1-130">**What It Does**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b49b1-131">`contoso.com`ou`*contoso.com*`</span><span class="sxs-lookup"><span data-stu-id="b49b1-131">`contoso.com` or `*contoso.com*`</span></span>  <br/> |<span data-ttu-id="b49b1-132">Bloque le domaine, les sous-domaines et les chemins d’accès, tel que `https://www.contoso.com`, `http://sub.contoso.com`, et`http://contoso.com/abc`</span><span class="sxs-lookup"><span data-stu-id="b49b1-132">Blocks the domain, subdomains, and paths, such as `https://www.contoso.com`, `http://sub.contoso.com`, and `http://contoso.com/abc`</span></span>  <br/> |
|`http://contoso.com/a`  <br/> |<span data-ttu-id="b49b1-133">Bloque un site `http://contoso.com/a` mais pas les autres sections`http://contoso.com/a/b`</span><span class="sxs-lookup"><span data-stu-id="b49b1-133">Blocks a site `http://contoso.com/a` but not additional subpaths like `http://contoso.com/a/b`</span></span>  <br/> |
|`http://contoso.com/a*`  <br/> |<span data-ttu-id="b49b1-134">Bloque un site `http://contoso.com/a` et sections supplémentaires`http://contoso.com/a/b`</span><span class="sxs-lookup"><span data-stu-id="b49b1-134">Blocks a site `http://contoso.com/a` and additional subpaths like `http://contoso.com/a/b`</span></span>  <br/> |
   
5. <span data-ttu-id="b49b1-135">Lorsque vous avez terminé d’ajouter des URL, dans le coin inférieur droit de l’écran, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b49b1-135">When you are finished adding URLs, in the lower right corner of the screen, choose **Save**.</span></span>
    
## <a name="how-to-define-exceptions-for-certain-users-in-an-organization"></a><span data-ttu-id="b49b1-136">Comment définir des exceptions pour certains utilisateurs dans une organisation</span><span class="sxs-lookup"><span data-stu-id="b49b1-136">How to define exceptions for certain users in an organization</span></span>

<span data-ttu-id="b49b1-p109">Si vous souhaitez que certains groupes pour être en mesure d’afficher les URL qui peuvent être bloquées pour d’autres personnes, vous pouvez spécifier une stratégie de liens fiables DAV qui s’applique à des destinataires spécifiques. Voir [configurer une liste d’URL personnalisée du « pas de rewrite » à l’aide de liens fiables DAV](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).</span><span class="sxs-lookup"><span data-stu-id="b49b1-p109">If you want certain groups to be able to view URLs that might be blocked for others, you can specify an ATP Safe Links policy that applies to specific recipients. See [Set up a custom "do not rewrite" URLs list using ATP Safe Links](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).</span></span>
  

