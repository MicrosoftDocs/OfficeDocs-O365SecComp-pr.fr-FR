---
title: Configurer une liste d'URL bloquées personnalisée à l'aide de liens fiables Office 365 ATP
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.date: 02/06/2019
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 896a7efb-1683-465e-a394-261349e5d866
ms.collection: M365-security-compliance
description: Découvrez comment configurer une liste d'URL bloquées pour votre organisation à l'aide d'Office 365 Advanced Threat Protection. Les URL bloquées s'appliquent aux messages électroniques et aux documents Office en fonction de vos stratégies de liens fiables ATP.
ms.openlocfilehash: ad9c613221b94e61022b11541ee068e35e47cc70
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30213024"
---
# <a name="set-up-a-custom-blocked-urls-list-using-office-365-atp-safe-links"></a><span data-ttu-id="e5f6e-104">Configurer une liste d'URL bloquées personnalisée à l'aide de liens fiables Office 365 ATP</span><span class="sxs-lookup"><span data-stu-id="e5f6e-104">Set up a custom blocked URLs list using Office 365 ATP Safe Links</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e5f6e-p102">Cet article est destiné aux clients professionnels. Si vous êtes un utilisateur à domicile et que vous recherchez des informations sur les liens fiables dans Outlook, consultez la rubrique [Advanced Outlook.com Security](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2).</span><span class="sxs-lookup"><span data-stu-id="e5f6e-p102">This article is intended for business customers. If you are a home user looking for information about Safe Links in Outlook, see [Advanced Outlook.com security](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2).</span></span>

<span data-ttu-id="e5f6e-p103">Avec [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP), votre organisation peut avoir une liste personnalisée d'adresses de sites Web (URL) bloquées. Lorsqu'une URL est bloquée, les personnes qui cliquent sur les liens vers l'URL bloquée sont dirigées vers une [page d'avertissement](atp-safe-links-warning-pages.md) semblable à l'image suivante:</span><span class="sxs-lookup"><span data-stu-id="e5f6e-p103">With [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP), your organization can have a custom list of website addresses (URLs) that are blocked. When a URL is blocked, people who click on links to the blocked URL are taken to a [warning page](atp-safe-links-warning-pages.md) that resembles the following image:</span></span> 
  
![Ce site est bloqué](media/6b4bda2d-a1e6-419e-8b10-588e83c3af3f.png)
  
<span data-ttu-id="e5f6e-110">La liste des URL bloquées est définie par l'équipe de sécurité Office 365 de votre organisation et s'applique à tous les membres de l'organisation qui sont couverts par les stratégies de liens approuvés Office 365 ATP.</span><span class="sxs-lookup"><span data-stu-id="e5f6e-110">The blocked URLs list is defined by your organization's Office 365 security team, and that list applies to everyone in the organization who is covered by Office 365 ATP Safe Links policies.</span></span> 
  
<span data-ttu-id="e5f6e-111">Lisez cet article pour découvrir comment configurer la liste des URL bloquées personnalisées de votre organisation pour les [liens fiables ATP dans Office 365](atp-safe-links.md).</span><span class="sxs-lookup"><span data-stu-id="e5f6e-111">Read this article to learn how to set up your organization's custom blocked URLs list for [ATP Safe Links in Office 365](atp-safe-links.md).</span></span>
  
## <a name="view-or-edit-a-custom-list-of-blocked-urls"></a><span data-ttu-id="e5f6e-112">Afficher ou modifier une liste personnalisée d'URL bloquées</span><span class="sxs-lookup"><span data-stu-id="e5f6e-112">View or edit a custom list of blocked URLs</span></span>

<span data-ttu-id="e5f6e-p104">Les [liens approuvés ATP dans Office 365](atp-safe-links.md) utilisent plusieurs listes, y compris la liste des URL bloquées personnalisées de votre organisation. Si vous disposez des autorisations nécessaires, vous pouvez configurer la liste personnalisée de votre organisation. Pour ce faire, vous devez modifier la stratégie de liens approuvés par défaut de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="e5f6e-p104">[ATP Safe Links in Office 365](atp-safe-links.md) uses several lists, including your organization's custom blocked URLs list. If you have the necessary permissions, you can set up your organization's custom list. You do this by editing your organization's default Safe Links policy.</span></span>

<span data-ttu-id="e5f6e-116">Pour modifier (ou définir) des stratégies ATP, vous devez disposer de l'un des rôles décrits dans le tableau suivant:</span><span class="sxs-lookup"><span data-stu-id="e5f6e-116">To edit (or define) ATP policies, you must be assigned one of the roles described in the following table:</span></span> 

|<span data-ttu-id="e5f6e-117">Rôle</span><span class="sxs-lookup"><span data-stu-id="e5f6e-117">Role</span></span>  |<span data-ttu-id="e5f6e-118">WHERE/How Assigned</span><span class="sxs-lookup"><span data-stu-id="e5f6e-118">Where/how assigned</span></span>  |
|---------|---------|
|<span data-ttu-id="e5f6e-119">Administrateur général Office 365</span><span class="sxs-lookup"><span data-stu-id="e5f6e-119">Office 365 Global Administrator</span></span> |<span data-ttu-id="e5f6e-p105">La personne qui s'inscrit pour acheter Office 365 est un administrateur global par défaut. (Pour en savoir plus, consultez la rubrique [à propos des rôles d'administrateur Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) .)</span><span class="sxs-lookup"><span data-stu-id="e5f6e-p105">The person who signs up to buy Office 365 is a global admin by default. (See [About Office 365 admin roles](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) to learn more.)</span></span>         |
|<span data-ttu-id="e5f6e-122">Administrateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="e5f6e-122">Security Administrator</span></span> |<span data-ttu-id="e5f6e-123">Centre d'administration Azure Active Directory[https://aad.portal.azure.com](https://aad.portal.azure.com)()</span><span class="sxs-lookup"><span data-stu-id="e5f6e-123">Azure Active Directory admin center ([https://aad.portal.azure.com](https://aad.portal.azure.com))</span></span>|
|<span data-ttu-id="e5f6e-124">Gestion de l'organisation Exchange Online</span><span class="sxs-lookup"><span data-stu-id="e5f6e-124">Exchange Online Organization Management</span></span> |<span data-ttu-id="e5f6e-125">Centre d'administration Exchange[https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)()</span><span class="sxs-lookup"><span data-stu-id="e5f6e-125">Exchange admin center ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp))</span></span> <br><span data-ttu-id="e5f6e-126">ou</span><span class="sxs-lookup"><span data-stu-id="e5f6e-126">or</span></span> <br>  <span data-ttu-id="e5f6e-127">Applets de commande PowerShell (consultez la rubrique [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps))</span><span class="sxs-lookup"><span data-stu-id="e5f6e-127">PowerShell cmdlets (See [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps))</span></span> |

> [!TIP]
> <span data-ttu-id="e5f6e-128">Pour en savoir plus sur les rôles et les autorisations, consultez [la rubrique autorisations &amp; dans le centre de sécurité conformité Office 365](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="e5f6e-128">To learn more about roles and permissions, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

### <a name="to-view-or-edit-a-custom-blocked-urls-list"></a><span data-ttu-id="e5f6e-129">Pour afficher ou modifier une liste d'URL bloquées personnalisée</span><span class="sxs-lookup"><span data-stu-id="e5f6e-129">To view or edit a custom blocked URLs list</span></span>
  
1. <span data-ttu-id="e5f6e-130">Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous avec votre compte professionnel ou scolaire.</span><span class="sxs-lookup"><span data-stu-id="e5f6e-130">Go to [https://protection.office.com](https://protection.office.com) and sign in with your work or school account.</span></span> 
    
2. <span data-ttu-id="e5f6e-131">Dans le volet de navigation de gauche, sous **gestion des menaces**, sélectionnez **liens approuvés**de **stratégie** \> .</span><span class="sxs-lookup"><span data-stu-id="e5f6e-131">In the left navigation, under **Threat management**, choose **Policy** \> **Safe Links**.</span></span>
    
3. <span data-ttu-id="e5f6e-132">Dans la section **stratégies qui s'appliquent à l'ensemble de l'organisation** , sélectionnez **par défaut**, puis **modifier** (le bouton modifier ressemble à un crayon).</span><span class="sxs-lookup"><span data-stu-id="e5f6e-132">In the **Policies that apply to the entire organization** section, select **Default**, and then choose **Edit** (the Edit button resembles a pencil).</span></span><br/><span data-ttu-id="e5f6e-133">![Cliquez sur modifier pour modifier votre stratégie par défaut pour la protection des liens fiables.](media/d08f9615-d947-4033-813a-d310ec2c8cca.png)</span><span class="sxs-lookup"><span data-stu-id="e5f6e-133">![Click Edit to edit your default policy for Safe Links protection](media/d08f9615-d947-4033-813a-d310ec2c8cca.png)</span></span><br/><span data-ttu-id="e5f6e-p106">Cela vous permet d'afficher la liste des URL bloquées. Dans un premier temps, il se peut que vous n'ayez aucune URL répertoriée ici.</span><span class="sxs-lookup"><span data-stu-id="e5f6e-p106">This enables you to view your list of blocked URLs. At first, you might not have any URLs listed here.</span></span><br/><span data-ttu-id="e5f6e-136">![Liste des URL bloquées dans la stratégie de liens approuvés par défaut](media/575e1449-6191-40ac-b626-030a2fd3fb11.png)</span><span class="sxs-lookup"><span data-stu-id="e5f6e-136">![Blocked URLs list in the default Safe Links policy](media/575e1449-6191-40ac-b626-030a2fd3fb11.png)</span></span>
  
4. <span data-ttu-id="e5f6e-137">Sélectionnez la zone **Entrez une URL valide** , tapez une URL, puis choisissez le signe plus (**+**).</span><span class="sxs-lookup"><span data-stu-id="e5f6e-137">Select the **Enter a valid URL** box, type a URL, and then choose the plus sign (**+**).</span></span> 

5. <span data-ttu-id="e5f6e-138">Lorsque vous avez terminé d'ajouter des URL, dans le coin inférieur droit de l'écran, sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="e5f6e-138">When you are finished adding URLs, in the lower right corner of the screen, choose **Save**.</span></span>
    
## <a name="a-few-things-to-keep-in-mind"></a><span data-ttu-id="e5f6e-139">Quelques éléments à garder à l'esprit</span><span class="sxs-lookup"><span data-stu-id="e5f6e-139">A few things to keep in mind</span></span>

<span data-ttu-id="e5f6e-140">Lorsque vous ajoutez des URL à votre liste, gardez les points suivants à l'esprit:</span><span class="sxs-lookup"><span data-stu-id="e5f6e-140">While you add URLs to your list, keep the following points in mind:</span></span> 

- <span data-ttu-id="e5f6e-p107">N'incluez pas une barre oblique **/**() à la fin de l'URL. Par exemple, au lieu de `http://www.contoso.com/`taper, `http://www.contoso.com`entrez.</span><span class="sxs-lookup"><span data-stu-id="e5f6e-p107">Do not include a forward slash ( **/**) at the end of the URL. For example, instead of entering `http://www.contoso.com/`, enter `http://www.contoso.com`.</span></span>
    
- <span data-ttu-id="e5f6e-p108">Vous pouvez spécifier une URL de domaine uniquement (par `contoso.com` exemple `tailspintoys.com`, ou). Cette opération bloque les clics sur les URL qui contiennent le domaine.</span><span class="sxs-lookup"><span data-stu-id="e5f6e-p108">You can specify a domain-only URL (like `contoso.com` or `tailspintoys.com`). This will block clicks on any URL that contains the domain.</span></span>

- <span data-ttu-id="e5f6e-p109">Vous pouvez spécifier un sous-domaine ( `toys.contoso.com*`par exemple) sans bloquer un domaine complet `contoso.com`(par exemple,). Cette opération bloque le clic sur toute URL qui contient le sous-domaine, mais ne bloque pas les clics vers une URL qui contient le domaine complet.</span><span class="sxs-lookup"><span data-stu-id="e5f6e-p109">You can specify a subdomain (like `toys.contoso.com*`) without blocking a full domain (like `contoso.com`). This will block clicks any URL that contains the subdomain, but it won't block clicks to a URL that contains the full domain.</span></span>  
    
- <span data-ttu-id="e5f6e-p110">Vous pouvez inclure jusqu'à trois astérisques génériques (\*) par URL. Le tableau suivant répertorie quelques exemples de ce que vous pouvez entrer et de l'effet de ces entrées.</span><span class="sxs-lookup"><span data-stu-id="e5f6e-p110">You can include up to three wildcard asterisks (\*) per URL. The following table lists some examples of what you can enter and what effect those entries have.</span></span>
    
|<span data-ttu-id="e5f6e-149">**Exemple d'entrée**</span><span class="sxs-lookup"><span data-stu-id="e5f6e-149">**Example Entry**</span></span>|<span data-ttu-id="e5f6e-150">**Ce qu'il fait**</span><span class="sxs-lookup"><span data-stu-id="e5f6e-150">**What It Does**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e5f6e-151">`contoso.com`des`*contoso.com*`</span><span class="sxs-lookup"><span data-stu-id="e5f6e-151">`contoso.com` or `*contoso.com*`</span></span>  <br/> |<span data-ttu-id="e5f6e-152">Bloque le domaine, les sous-domaines et les chemins d' `https://www.contoso.com`accès `http://sub.contoso.com`, par exemple, et`http://contoso.com/abc`</span><span class="sxs-lookup"><span data-stu-id="e5f6e-152">Blocks the domain, subdomains, and paths, such as `https://www.contoso.com`, `http://sub.contoso.com`, and `http://contoso.com/abc`</span></span>  <br/> |
|`http://contoso.com/a`  <br/> |<span data-ttu-id="e5f6e-153">Bloque un `http://contoso.com/a` site, mais pas les sous-chemins supplémentaires comme`http://contoso.com/a/b`</span><span class="sxs-lookup"><span data-stu-id="e5f6e-153">Blocks a site `http://contoso.com/a` but not additional subpaths like `http://contoso.com/a/b`</span></span>  <br/> |
|`http://contoso.com/a*`  <br/> |<span data-ttu-id="e5f6e-154">Bloque un `http://contoso.com/a` site et des sous-chemins supplémentaires comme`http://contoso.com/a/b`</span><span class="sxs-lookup"><span data-stu-id="e5f6e-154">Blocks a site `http://contoso.com/a` and additional subpaths like `http://contoso.com/a/b`</span></span>  <br/> |
|`http://toys.contoso.com*`  <br/> |<span data-ttu-id="e5f6e-155">Bloque un sous-domaine («jouets» dans ce cas) tout en permettant de cliquer sur d' `http://contoso.com` autres `http://home.contoso.com`URL de domaine (par exemple, ou).</span><span class="sxs-lookup"><span data-stu-id="e5f6e-155">Blocks a subdomain ("toys" in this case) but allow clicks to other domain URLs (like `http://contoso.com` or `http://home.contoso.com`).</span></span>  <br/> |
   

## <a name="how-to-define-exceptions-for-certain-users-in-an-organization"></a><span data-ttu-id="e5f6e-156">Procédure de définition des exceptions pour certains utilisateurs d'une organisation</span><span class="sxs-lookup"><span data-stu-id="e5f6e-156">How to define exceptions for certain users in an organization</span></span>

<span data-ttu-id="e5f6e-p111">Si vous souhaitez que certains groupes puissent afficher les URL susceptibles d'être bloquées pour d'autres, vous pouvez spécifier une stratégie de liens approuvés ATP qui s'applique à des destinataires spécifiques. Consultez [la rubrique Configurer une liste d'URL personnalisée «ne pas réécrire» à l'aide des liens fiables ATP](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).</span><span class="sxs-lookup"><span data-stu-id="e5f6e-p111">If you want certain groups to be able to view URLs that might be blocked for others, you can specify an ATP Safe Links policy that applies to specific recipients. See [Set up a custom "do not rewrite" URLs list using ATP Safe Links](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).</span></span>
  

