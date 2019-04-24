---
title: Secure Score Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/13/2019
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c9e7160f-2c34-4bd0-a548-5ddcc862eaef
description: Vous avez jamais étonnant quelle est la sécurisation de votre organisation dans Office 365? Le score de sécurité est là pour vous aider. Le score sécurisé analyse la sécurité de votre organisation en fonction de vos activités normales et des paramètres de sécurité dans Office 365 et affecte un score.
ms.openlocfilehash: dd0dc87910853eba9f2ec3ec6752e857462b46e5
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262450"
---
# <a name="office-365-secure-score"></a><span data-ttu-id="9a65f-105">Secure Score Office 365</span><span class="sxs-lookup"><span data-stu-id="9a65f-105">Office 365 Secure Score</span></span>

<span data-ttu-id="9a65f-106">**Résumé** Vous avez jamais étonnant quelle est la sécurisation de votre organisation dans Office 365?</span><span class="sxs-lookup"><span data-stu-id="9a65f-106">**Summary** Ever wonder how secure your organization really is in Office 365?</span></span> <span data-ttu-id="9a65f-107">Le score de sécurité est là pour vous aider.</span><span class="sxs-lookup"><span data-stu-id="9a65f-107">Secure Score is here to help.</span></span> <span data-ttu-id="9a65f-108">Le score sécurisé analyse la sécurité de votre organisation en fonction de vos activités normales et des paramètres de sécurité dans Office 365 et affecte un score.</span><span class="sxs-lookup"><span data-stu-id="9a65f-108">Secure Score analyzes your organization's security  based on your regular activities and security settings in Office 365, and assigns a score.</span></span> <span data-ttu-id="9a65f-109">Lisez cet article pour obtenir une vue d'ensemble du score sécurisé et de la façon dont vous pouvez l'utiliser.</span><span class="sxs-lookup"><span data-stu-id="9a65f-109">Read this article to get an overview of Secure Score and how you can use it.</span></span>
  
## <a name="how-to-get-to-secure-score"></a><span data-ttu-id="9a65f-110">Comment obtenir le score sécurisé</span><span class="sxs-lookup"><span data-stu-id="9a65f-110">How to get to Secure Score</span></span>

<span data-ttu-id="9a65f-111">Si votre organisation dispose d'un abonnement qui inclut [office 365 Enterprise](https://docs.microsoft.com/office365/enterprise/), [Microsoft 365 business](https://docs.microsoft.com/microsoft-365/business/)ou Office 365 Business Premium, et que vous disposez des [autorisations nécessaires](#required-permissions), vous pouvez afficher le score de sécurité de votre organisation en visitant le site [https://securescore.office.com](https://securescore.office.com).</span><span class="sxs-lookup"><span data-stu-id="9a65f-111">If your organization has a subscription that includes [Office 365 Enterprise](https://docs.microsoft.com/office365/enterprise/), [Microsoft 365 Business](https://docs.microsoft.com/microsoft-365/business/), or Office 365 Business Premium, and you have the [necessary permissions](#required-permissions), you can view your organization's secure score by visiting [https://securescore.office.com](https://securescore.office.com).</span></span> 

<span data-ttu-id="9a65f-112">Vous pouvez également visiter le centre de sécurité & Compliance Center ([https://protection.office.com](https://protection.office.com)), où vous trouverez un widget de score sécurisé qui vous fournit votre score actuel.</span><span class="sxs-lookup"><span data-stu-id="9a65f-112">Alternatively, you can visit the Security & Compliance Center ([https://protection.office.com](https://protection.office.com)), where you'll find a Secure Score widget that provides you with your current score.</span></span>

![Widget de score sécurisé](media/SecureScoreWidget-o365.png)

<span data-ttu-id="9a65f-114">Le widget inclut un lien vers votre tableau de bord de score sécurisé.</span><span class="sxs-lookup"><span data-stu-id="9a65f-114">The widget includes a link to your Secure Score dashboard.</span></span>

![Tableau de bord de score sécurisé](media/SecureScore-WelcomeScreen.png)
  
## <a name="how-it-works"></a><span data-ttu-id="9a65f-116">Mode de fonctionnement</span><span class="sxs-lookup"><span data-stu-id="9a65f-116">How it works</span></span>

<span data-ttu-id="9a65f-117">Le score de sécurité détermine les services Office 365 que vous utilisez (par exemple, OneDrive, SharePoint et Exchange), puis compare vos paramètres et activités à une base établie par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9a65f-117">Secure Score determines what Office 365 services you're using (such as OneDrive, SharePoint, and Exchange) then compares your settings and activities to a baseline established by Microsoft.</span></span> <span data-ttu-id="9a65f-118">Vous obtiendrez un score en fonction de la manière dont votre organisation est bien alignée sur les meilleures pratiques en matière de sécurité.</span><span class="sxs-lookup"><span data-stu-id="9a65f-118">You'll get a score based on how well aligned your organization is with security best practices.</span></span> <span data-ttu-id="9a65f-119">Vous obtiendrez également des recommandations sur les étapes que vous pouvez suivre pour améliorer le score de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="9a65f-119">You'll also get recommendations on steps you can take to improve your organization's score.</span></span> 
  
![File d'attente des actions dans l'outil de score sécurisé Office 365](media/SecureScore-ActionsToTake.png)
  
<span data-ttu-id="9a65f-121">Le score de sécurité calcule votre score en fonction des services que vous avez achetés.</span><span class="sxs-lookup"><span data-stu-id="9a65f-121">Secure Score calculates your score based on the services you purchased.</span></span> <span data-ttu-id="9a65f-122">Par exemple, si vous avez acheté uniquement un plan Exchange Online, vous ne serez pas remarqué pour les fonctionnalités de sécurité de SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="9a65f-122">For example, if you only purchased an Exchange Online plan, you won't be scored for SharePoint Online security features.</span></span> <span data-ttu-id="9a65f-123">Le dénominateur du score est la somme de toutes les lignes de base pour les contrôles qui s'appliquent aux produits que vous avez achetés.</span><span class="sxs-lookup"><span data-stu-id="9a65f-123">The denominator of the score is the sum of all the baselines for the controls that apply to the products you purchased.</span></span> <span data-ttu-id="9a65f-124">Le numérateur est la somme de tous les contrôles pour lesquels vous avez terminé, ou partiellement terminé, les actions à effectuer pour répondre à ce contrôle.</span><span class="sxs-lookup"><span data-stu-id="9a65f-124">The numerator is the sum of all the controls for which you completed, or partially completed, the actions to fulfill that control.</span></span>

<span data-ttu-id="9a65f-125">Développez une action pour découvrir les étapes à suivre, les menaces qui vous aideront à vous protéger et le nombre de points que votre score augmentera une fois que vous aurez suivi la recommandation.</span><span class="sxs-lookup"><span data-stu-id="9a65f-125">Expand an action to learn about what steps to take, the threats it'll help protect you from, and how many points your score will increase once you follow the recommendation.</span></span>
  
![Action étendue dans l'outil de score de sécurité d'Office 365](media/SecureScore-DetailedActionToTake.png)
  
<span data-ttu-id="9a65f-127">Pour voir l'impact de vos actions sur la sécurité de votre organisation, sélectionnez l'onglet analyseur de **score** et examinez votre historique.</span><span class="sxs-lookup"><span data-stu-id="9a65f-127">To see the impact of your actions on your organization's security, select the **Score Analyzer** tab and review your history.</span></span> 
  
![Onglet analyseur de score de l'outil de score sécurisé Office 365](media/SecureScore-ScoreAnalyzer-7days.png)
  
<span data-ttu-id="9a65f-129">Sous le graphique, vous verrez une liste de scores et d'actions par catégorie.</span><span class="sxs-lookup"><span data-stu-id="9a65f-129">Below the chart, you'll see a list of scores and actions by category.</span></span> 
  
![Graphique sous l'onglet analyseur de score avec un point de données sélectionné](media/SecureScore-Analyzer-breakdownbelowchart.png)
 
<span data-ttu-id="9a65f-131">Les actions étiquetées **[non score]** sont celles que vous pouvez effectuer pour votre organisation, mais comme elles ne sont pas connectées au score de sécurité, elles ne sont pas évaluées.</span><span class="sxs-lookup"><span data-stu-id="9a65f-131">Actions that are labeled as **[Not Scored]** are ones you can perform for your organization, but because they are not connected to Secure Score, they are not scored.</span></span>  

<span data-ttu-id="9a65f-132">Sur la page analyseur de **score** , cliquez sur un point de données pour un jour spécifique, puis faites défiler la liste pour voir les actions terminées et incomplètes pour ce jour afin de déterminer ce qui a changé.</span><span class="sxs-lookup"><span data-stu-id="9a65f-132">On the **Score Analyzer** page, click a data point for a specific day, then scroll down to see the completed and incomplete actions for that day to find out what changed.</span></span> <span data-ttu-id="9a65f-133">Le score est calculé une fois par jour (environ 1:00 PST).</span><span class="sxs-lookup"><span data-stu-id="9a65f-133">The score is calculated once per day (around 1:00 AM PST).</span></span> <span data-ttu-id="9a65f-134">Si vous modifiez une action mesurée, le score est automatiquement mis à jour le jour suivant.</span><span class="sxs-lookup"><span data-stu-id="9a65f-134">If you make a change to a measured action, the score will automatically update the next day.</span></span> <span data-ttu-id="9a65f-135">Il faut jusqu'à 48 heures pour qu'une modification soit reflétée dans votre score.</span><span class="sxs-lookup"><span data-stu-id="9a65f-135">It takes up to 48 hours for a change to be reflected in your score.</span></span>

<span data-ttu-id="9a65f-136">Le score de sécurité n'exprime pas une mesure absolue de la probabilité d'obtenir une violation.</span><span class="sxs-lookup"><span data-stu-id="9a65f-136">Secure Score does not express an absolute measure of how likely you are to get breached.</span></span> <span data-ttu-id="9a65f-137">Elle exprime la mesure dans laquelle vous avez adopté des fonctionnalités qui peuvent décaler le risque d'être enfreintes.</span><span class="sxs-lookup"><span data-stu-id="9a65f-137">It expresses the extent to which you have adopted features that can offset the risk of being breached.</span></span> <span data-ttu-id="9a65f-138">Aucun service ne peut garantir que vous ne serez pas violé, et le score sécurisé ne doit pas être interprété comme une garantie de quelque façon que ce soit.</span><span class="sxs-lookup"><span data-stu-id="9a65f-138">No service can guarantee that you will not be breached, and the Secure Score should not be interpreted as a guarantee in any way.</span></span>
 
## <a name="how-secure-score-helps"></a><span data-ttu-id="9a65f-139">Aide du score de sécurité</span><span class="sxs-lookup"><span data-stu-id="9a65f-139">How Secure Score helps</span></span>

<span data-ttu-id="9a65f-140">Avec la fonction de chiffrement sécurisé, vous pouvez améliorer la sécurité de votre organisation en utilisant les fonctionnalités de sécurité intégrées dans Office 365 (un grand nombre d'entre vous avez déjà acheté, mais cela n'est peut-être pas conscient).</span><span class="sxs-lookup"><span data-stu-id="9a65f-140">With Secure Score, you can help improve your organization's security posture by using the built-in security features in Office 365 (many of which you already purchased but might not be aware of).</span></span> <span data-ttu-id="9a65f-141">Pour en savoir plus sur ces fonctionnalités, vous pouvez vous assurer que vous prenez les mesures appropriées pour protéger votre organisation contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="9a65f-141">Learning more about these features can help give you peace of mind that you're taking the right steps to protect your organization from threats.</span></span>
  
<span data-ttu-id="9a65f-142">Mais ne suivez pas seulement notre mot pour le service informatique.</span><span class="sxs-lookup"><span data-stu-id="9a65f-142">But don't just take our word for it.</span></span> <span data-ttu-id="9a65f-143">Les clients qui utilisent le score de sécurité ont vu leur score augmenter cinq fois de plus que les clients qui ne l'utilisent pas.</span><span class="sxs-lookup"><span data-stu-id="9a65f-143">Customers who are using Secure Score have seen their score increase five times more than customers who aren't using it.</span></span> <span data-ttu-id="9a65f-144">(L'augmentation de leur score correspond aux fonctionnalités de sécurité utilisées dans leur organisation.)</span><span class="sxs-lookup"><span data-stu-id="9a65f-144">(The increase in their score corresponds with the security features being used in their organizations.)</span></span>
  
> [!NOTE]
> <span data-ttu-id="9a65f-145">Le score de sécurité n'exprime pas une mesure absolue de la probabilité d'obtenir une violation.</span><span class="sxs-lookup"><span data-stu-id="9a65f-145">Secure Score does not express an absolute measure of how likely you are to get breached.</span></span> <span data-ttu-id="9a65f-146">Elle exprime la mesure dans laquelle vous avez adopté des contrôles pouvant dépenser le risque d'être compromis.</span><span class="sxs-lookup"><span data-stu-id="9a65f-146">It expresses the extent to which you have adopted controls which can offset the risk of being breached.</span></span> <span data-ttu-id="9a65f-147">Aucun service ne peut garantir que vous ne serez pas violé, et le score de sécurité ne doit pas être interprété comme une garantie de quelque façon que ce soit.</span><span class="sxs-lookup"><span data-stu-id="9a65f-147">No service can guarantee that you will not be breached, and Secure Score should not be interpreted as a guarantee in any way.</span></span> 
  
## <a name="required-permissions"></a><span data-ttu-id="9a65f-148">Autorisations requises</span><span class="sxs-lookup"><span data-stu-id="9a65f-148">Required permissions</span></span>

<span data-ttu-id="9a65f-149">Pour afficher et utiliser votre tableau de bord de score sécurisé, vous devez disposer de l'un des rôles suivants dans [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles):</span><span class="sxs-lookup"><span data-stu-id="9a65f-149">In order to view and use your Secure Score dashboard, you must be assigned one of the following roles in [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles):</span></span>
- <span data-ttu-id="9a65f-150">Administrateur général</span><span class="sxs-lookup"><span data-stu-id="9a65f-150">Global Administrator</span></span>
- <span data-ttu-id="9a65f-151">Administrateur de facturation</span><span class="sxs-lookup"><span data-stu-id="9a65f-151">Billing Administrator</span></span>
- <span data-ttu-id="9a65f-152">Administrateur d'utilisateur</span><span class="sxs-lookup"><span data-stu-id="9a65f-152">User Administrator</span></span>
- <span data-ttu-id="9a65f-153">Administrateur de mots de passe</span><span class="sxs-lookup"><span data-stu-id="9a65f-153">Password Administrator</span></span>
- <span data-ttu-id="9a65f-154">Administrateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="9a65f-154">Security Administrator</span></span>
- <span data-ttu-id="9a65f-155">Lecteur de sécurité</span><span class="sxs-lookup"><span data-stu-id="9a65f-155">Security Reader</span></span>
- <span data-ttu-id="9a65f-156">Administrateur Exchange</span><span class="sxs-lookup"><span data-stu-id="9a65f-156">Exchange Administrator</span></span>
- <span data-ttu-id="9a65f-157">Administrateur SharePoint</span><span class="sxs-lookup"><span data-stu-id="9a65f-157">SharePoint Administrator</span></span>

 <span data-ttu-id="9a65f-158">Les utilisateurs qui ne sont pas affectés à un rôle d'administrateur ne peuvent pas accéder au score sécurisé.</span><span class="sxs-lookup"><span data-stu-id="9a65f-158">Users who aren't assigned an admin role won't be able to access Secure Score.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a65f-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a65f-159">Related topics</span></span>

[<span data-ttu-id="9a65f-160">Vue d'ensemble du tableau de bord de sécurité</span><span class="sxs-lookup"><span data-stu-id="9a65f-160">Security dashboard overview</span></span>](security-dashboard.md)

[<span data-ttu-id="9a65f-161">Quel abonnement ai-je ?</span><span class="sxs-lookup"><span data-stu-id="9a65f-161">What subscription do I have?</span></span>](https://docs.microsoft.com/office365/admin/admin-overview/what-subscription-do-i-have?view=o365-worldwide)
