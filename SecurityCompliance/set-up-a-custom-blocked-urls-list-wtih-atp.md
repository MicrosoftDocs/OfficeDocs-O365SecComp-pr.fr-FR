---
title: Configurer une liste d’URL bloquée personnalisée à l’aide d’Office 365 DAV fiables liens
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.date: 02/06/2019
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 896a7efb-1683-465e-a394-261349e5d866
description: Découvrez comment configurer une liste d’URL bloqués pour votre organisation à l’aide d’Office 365 avancée protection contre les menaces. Les URL bloquées s’appliquera aux messages électroniques et des documents Office en fonction de vos stratégies de liens fiables DAV.
ms.openlocfilehash: 4d8c9c669310137d3f491f5a79c93f4d6af71ac5
ms.sourcegitcommit: d6a28c4f6db6a676ca960173e8ff8f17d4aa1c4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2019
ms.locfileid: "29755315"
---
# <a name="set-up-a-custom-blocked-urls-list-using-office-365-atp-safe-links"></a><span data-ttu-id="564d1-104">Configurer une liste d’URL bloquée personnalisée à l’aide d’Office 365 DAV fiables liens</span><span class="sxs-lookup"><span data-stu-id="564d1-104">Set up a custom blocked URLs list using Office 365 ATP Safe Links</span></span>

<span data-ttu-id="564d1-p102">Avec [Office 365 avancée protection contre les menaces](office-365-atp.md) (DAV), votre organisation peut avoir une liste personnalisée d’adresses de site Web (URL) qui sont bloqués. Lorsqu’une URL est bloquée, les personnes qui cliquent sur des liens vers l’URL bloqué sont dirigés vers une [page d’avertissement](atp-safe-links-warning-pages.md) qui ressemble à l’image suivante :</span><span class="sxs-lookup"><span data-stu-id="564d1-p102">With [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP), your organization can have a custom list of website addresses (URLs) that are blocked. When a URL is blocked, people who click on links to the blocked URL are taken to a [warning page](atp-safe-links-warning-pages.md) that resembles the following image:</span></span> 
  
![Ce site est bloqué.](media/6b4bda2d-a1e6-419e-8b10-588e83c3af3f.png)
  
<span data-ttu-id="564d1-108">La liste des URL bloquée est définie par l’équipe de sécurité de votre organisation Office 365, et cette liste s’applique à tout le monde dans l’organisation qui est couvert par les stratégies de liaisons sans échec de Office 365 DAV.</span><span class="sxs-lookup"><span data-stu-id="564d1-108">The blocked URLs list is defined by your organization's Office 365 security team, and that list applies to everyone in the organization who is covered by Office 365 ATP Safe Links policies.</span></span> 
  
<span data-ttu-id="564d1-109">Lisez cet article pour apprendre à configurer la liste des URL bloqué personnalisé de votre organisation pour les [Liens sécurisés DAV dans Office 365](atp-safe-links.md).</span><span class="sxs-lookup"><span data-stu-id="564d1-109">Read this article to learn how to set up your organization's custom blocked URLs list for [ATP Safe Links in Office 365](atp-safe-links.md).</span></span>
  
## <a name="view-or-edit-a-custom-list-of-blocked-urls"></a><span data-ttu-id="564d1-110">Afficher ou modifier une liste personnalisée d’URL bloquées</span><span class="sxs-lookup"><span data-stu-id="564d1-110">View or edit a custom list of blocked URLs</span></span>

<span data-ttu-id="564d1-p103">[Liens approuvés DAV dans Office 365](atp-safe-links.md) utilise plusieurs listes, y compris la liste des URL bloqué personnalisé de votre organisation. Si vous disposez des autorisations nécessaires, vous pouvez configurer la liste personnalisée de votre organisation. Pour cela, en modifiant la stratégie de liens fiables par défaut de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="564d1-p103">[ATP Safe Links in Office 365](atp-safe-links.md) uses several lists, including your organization's custom blocked URLs list. If you have the necessary permissions, you can set up your organization's custom list. You do this by editing your organization's default Safe Links policy.</span></span>

<span data-ttu-id="564d1-114">Pour modifier (ou définir) stratégies DAV, vous devez posséder un des rôles décrits dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="564d1-114">To edit (or define) ATP policies, you must be assigned one of the roles described in the following table:</span></span> 

|<span data-ttu-id="564d1-115">Rôle</span><span class="sxs-lookup"><span data-stu-id="564d1-115">Role</span></span>  |<span data-ttu-id="564d1-116">Où/procédure affecté</span><span class="sxs-lookup"><span data-stu-id="564d1-116">Where/how assigned</span></span>  |
|---------|---------|
|<span data-ttu-id="564d1-117">Administrateur Global d’Office 365</span><span class="sxs-lookup"><span data-stu-id="564d1-117">Office 365 Global Administrator</span></span> |<span data-ttu-id="564d1-p104">La personne qui s’inscrit à acheter Office 365 est un administrateur global par défaut. (Voir [les rôles d’administration sur Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) pour en savoir plus).</span><span class="sxs-lookup"><span data-stu-id="564d1-p104">The person who signs up to buy Office 365 is a global admin by default. (See [About Office 365 admin roles](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) to learn more.)</span></span>         |
|<span data-ttu-id="564d1-120">Administrateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="564d1-120">Security Administrator</span></span> |<span data-ttu-id="564d1-121">Centre d’administration Active Directory Azure ([https://aad.portal.azure.com](https://aad.portal.azure.com))</span><span class="sxs-lookup"><span data-stu-id="564d1-121">Azure Active Directory admin center ([https://aad.portal.azure.com](https://aad.portal.azure.com))</span></span>|
|<span data-ttu-id="564d1-122">Gestion de l’organisation en ligne Exchange</span><span class="sxs-lookup"><span data-stu-id="564d1-122">Exchange Online Organization Management</span></span> |<span data-ttu-id="564d1-123">Centre d’administration Exchange ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp))</span><span class="sxs-lookup"><span data-stu-id="564d1-123">Exchange admin center ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp))</span></span> <br><span data-ttu-id="564d1-124">ou</span><span class="sxs-lookup"><span data-stu-id="564d1-124">or</span></span> <br>  <span data-ttu-id="564d1-125">Applets de commande PowerShell (voir [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps))</span><span class="sxs-lookup"><span data-stu-id="564d1-125">PowerShell cmdlets (See [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps))</span></span> |

> [!TIP]
> <span data-ttu-id="564d1-126">Pour en savoir plus sur les rôles et autorisations, voir [des autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="564d1-126">To learn more about roles and permissions, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

### <a name="to-view-or-edit-a-custom-blocked-urls-list"></a><span data-ttu-id="564d1-127">Pour afficher ou modifier une liste d’URL bloquée personnalisée</span><span class="sxs-lookup"><span data-stu-id="564d1-127">To view or edit a custom blocked URLs list</span></span>
  
1. <span data-ttu-id="564d1-128">Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous avec votre compte professionnel ou de l’école.</span><span class="sxs-lookup"><span data-stu-id="564d1-128">Go to [https://protection.office.com](https://protection.office.com) and sign in with your work or school account.</span></span> 
    
2. <span data-ttu-id="564d1-129">Dans la navigation de gauche, sous **Gestion des menaces**, choisissez **stratégie** \> **Liens fiables**.</span><span class="sxs-lookup"><span data-stu-id="564d1-129">In the left navigation, under **Threat management**, choose **Policy** \> **Safe Links**.</span></span>
    
3. <span data-ttu-id="564d1-130">Dans la section **stratégies qui s’appliquent à toute l’organisation** , sélectionnez **par défaut**, puis choisissez **Modifier** (le bouton Modifier ressemble à un crayon).</span><span class="sxs-lookup"><span data-stu-id="564d1-130">In the **Policies that apply to the entire organization** section, select **Default**, and then choose **Edit** (the Edit button resembles a pencil).</span></span><br/><span data-ttu-id="564d1-131">![Cliquez sur Modifier pour modifier votre stratégie par défaut pour la protection des liens fiables](media/d08f9615-d947-4033-813a-d310ec2c8cca.png)</span><span class="sxs-lookup"><span data-stu-id="564d1-131">![Click Edit to edit your default policy for Safe Links protection](media/d08f9615-d947-4033-813a-d310ec2c8cca.png)</span></span><br/><span data-ttu-id="564d1-p105">Cela vous permet d’afficher la liste des URL bloquées. Tout d’abord, vous ne disposez pas des URL répertoriées ici.</span><span class="sxs-lookup"><span data-stu-id="564d1-p105">This enables you to view your list of blocked URLs. At first, you might not have any URLs listed here.</span></span><br/><span data-ttu-id="564d1-134">![Liste des URL dans la stratégie de liens fiables par défaut bloqués](media/575e1449-6191-40ac-b626-030a2fd3fb11.png)</span><span class="sxs-lookup"><span data-stu-id="564d1-134">![Blocked URLs list in the default Safe Links policy](media/575e1449-6191-40ac-b626-030a2fd3fb11.png)</span></span>
  
4. <span data-ttu-id="564d1-135">Sélectionnez la zone **Tapez une URL valide** , tapez une URL, puis cliquez sur le signe plus (**+**).</span><span class="sxs-lookup"><span data-stu-id="564d1-135">Select the **Enter a valid URL** box, type a URL, and then choose the plus sign (**+**).</span></span> 

5. <span data-ttu-id="564d1-136">Lorsque vous avez terminé d’ajouter des URL, dans le coin inférieur droit de l’écran, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="564d1-136">When you are finished adding URLs, in the lower right corner of the screen, choose **Save**.</span></span>
    
## <a name="a-few-things-to-keep-in-mind"></a><span data-ttu-id="564d1-137">Quelques éléments à prendre en compte</span><span class="sxs-lookup"><span data-stu-id="564d1-137">A few things to keep in mind</span></span>

<span data-ttu-id="564d1-138">Lorsque vous ajoutez à votre liste des URL, gardez les points suivants à l’esprit :</span><span class="sxs-lookup"><span data-stu-id="564d1-138">While you add URLs to your list, keep the following points in mind:</span></span> 

- <span data-ttu-id="564d1-p106">N’incluez pas une barre oblique ( **/**) à la fin de l’URL. Par exemple, au lieu de saisir `http://www.contoso.com/`, entrez `http://www.contoso.com`.</span><span class="sxs-lookup"><span data-stu-id="564d1-p106">Do not include a forward slash ( **/**) at the end of the URL. For example, instead of entering `http://www.contoso.com/`, enter `http://www.contoso.com`.</span></span>
    
- <span data-ttu-id="564d1-p107">Vous pouvez spécifier une URL de domaine (comme `contoso.com` ou `tailspintoys.com`). Cela empêchera clics sur n’importe quelle URL qui contient le domaine.</span><span class="sxs-lookup"><span data-stu-id="564d1-p107">You can specify a domain-only URL (like `contoso.com` or `tailspintoys.com`). This will block clicks on any URL that contains the domain.</span></span>

- <span data-ttu-id="564d1-p108">Vous pouvez spécifier un sous-domaine (comme `toys.contoso.com*`) sans bloquer un domaine complet (comme `contoso.com`). Il est bloc clique sur une URL qui contient le sous-domaine, mais il ne bloque clique sur une URL qui contient le domaine complet.</span><span class="sxs-lookup"><span data-stu-id="564d1-p108">You can specify a subdomain (like `toys.contoso.com*`) without blocking a full domain (like `contoso.com`). This will block clicks any URL that contains the subdomain, but it won't block clicks to a URL that contains the full domain.</span></span>  
    
- <span data-ttu-id="564d1-p109">Vous pouvez inclure jusqu'à trois astérisques générique (\*) par l’URL. Le tableau suivant répertorie quelques exemples de ce que vous pouvez entrer et les effets que ces entrées ont.</span><span class="sxs-lookup"><span data-stu-id="564d1-p109">You can include up to three wildcard asterisks (\*) per URL. The following table lists some examples of what you can enter and what effect those entries have.</span></span>
    
|<span data-ttu-id="564d1-147">**Exemple d’entrée**</span><span class="sxs-lookup"><span data-stu-id="564d1-147">**Example Entry**</span></span>|<span data-ttu-id="564d1-148">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="564d1-148">**What It Does**</span></span>|
|:-----|:-----|
|<span data-ttu-id="564d1-149">`contoso.com`ou`*contoso.com*`</span><span class="sxs-lookup"><span data-stu-id="564d1-149">`contoso.com` or `*contoso.com*`</span></span>  <br/> |<span data-ttu-id="564d1-150">Bloque le domaine, les sous-domaines et les chemins d’accès, tel que `https://www.contoso.com`, `http://sub.contoso.com`, et`http://contoso.com/abc`</span><span class="sxs-lookup"><span data-stu-id="564d1-150">Blocks the domain, subdomains, and paths, such as `https://www.contoso.com`, `http://sub.contoso.com`, and `http://contoso.com/abc`</span></span>  <br/> |
|`http://contoso.com/a`  <br/> |<span data-ttu-id="564d1-151">Bloque un site `http://contoso.com/a` mais pas les autres sections`http://contoso.com/a/b`</span><span class="sxs-lookup"><span data-stu-id="564d1-151">Blocks a site `http://contoso.com/a` but not additional subpaths like `http://contoso.com/a/b`</span></span>  <br/> |
|`http://contoso.com/a*`  <br/> |<span data-ttu-id="564d1-152">Bloque un site `http://contoso.com/a` et sections supplémentaires`http://contoso.com/a/b`</span><span class="sxs-lookup"><span data-stu-id="564d1-152">Blocks a site `http://contoso.com/a` and additional subpaths like `http://contoso.com/a/b`</span></span>  <br/> |
|`http://toys.contoso.com*`  <br/> |<span data-ttu-id="564d1-153">Bloque un sous-domaine (« toys » dans ce cas), mais autoriser les clics vers d’autres URL de domaine (comme `http://contoso.com` ou `http://home.contoso.com`).</span><span class="sxs-lookup"><span data-stu-id="564d1-153">Blocks a subdomain ("toys" in this case) but allow clicks to other domain URLs (like `http://contoso.com` or `http://home.contoso.com`).</span></span>  <br/> |
   

## <a name="how-to-define-exceptions-for-certain-users-in-an-organization"></a><span data-ttu-id="564d1-154">Comment définir des exceptions pour certains utilisateurs dans une organisation</span><span class="sxs-lookup"><span data-stu-id="564d1-154">How to define exceptions for certain users in an organization</span></span>

<span data-ttu-id="564d1-p110">Si vous souhaitez que certains groupes pour être en mesure d’afficher les URL qui peuvent être bloquées pour d’autres personnes, vous pouvez spécifier une stratégie de liens fiables DAV qui s’applique à des destinataires spécifiques. Voir [configurer une liste d’URL personnalisée du « pas de rewrite » à l’aide de liens fiables DAV](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).</span><span class="sxs-lookup"><span data-stu-id="564d1-p110">If you want certain groups to be able to view URLs that might be blocked for others, you can specify an ATP Safe Links policy that applies to specific recipients. See [Set up a custom "do not rewrite" URLs list using ATP Safe Links](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).</span></span>
  

