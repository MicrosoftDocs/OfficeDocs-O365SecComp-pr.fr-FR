---
title: Secure Score Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/25/2019
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c9e7160f-2c34-4bd0-a548-5ddcc862eaef
description: Demandez jamais sécurisé comment votre entreprise est vraiment dans Office 365 ? Score sécurisée est là pour aider. Score sécurisé analyse la sécurité de votre organisation basée sur les activités normales et les paramètres de sécurité dans Office 365 et attribue une note.
ms.openlocfilehash: bc0379e40b09e63e5fded1b1a289d40c306def91
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29559087"
---
# <a name="office-365-secure-score"></a><span data-ttu-id="eb6ec-105">Secure Score Office 365</span><span class="sxs-lookup"><span data-stu-id="eb6ec-105">Office 365 Secure Score</span></span>

<span data-ttu-id="eb6ec-p102">**Résumé** Demandez jamais sécurisé comment votre entreprise est vraiment dans Office 365 ? Score sécurisée est là pour aider. Score sécurisé analyse la sécurité de votre organisation basée sur les activités normales et les paramètres de sécurité dans Office 365 et attribue une note. Lisez cet article pour obtenir une vue d’ensemble de Score d’informations sécurisé et comment vous pouvez l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="eb6ec-p102">**Summary** Ever wonder how secure your organization really is in Office 365? Secure Score is here to help. Secure Score analyzes your organization's security  based on your regular activities and security settings in Office 365, and assigns a score. Read this article to get an overview of Secure Score and how you can use it.</span></span>
  
## <a name="how-to-get-to-secure-score"></a><span data-ttu-id="eb6ec-110">Comment obtenir au Score d’informations sécurisé</span><span class="sxs-lookup"><span data-stu-id="eb6ec-110">How to get to Secure Score</span></span>

<span data-ttu-id="eb6ec-111">Si votre organisation a un abonnement qui inclut [Office 365 pour entreprises](https://docs.microsoft.com/office365/enterprise/), [Microsoft 365 Professionnel](https://docs.microsoft.com/microsoft-365/business/)ou Office 365 entreprise Premium et que vous disposez des [autorisations nécessaires](#required-permissions), vous pouvez afficher le score sécurisée de votre organisation en consultant [https://securescore.office.com](https://securescore.office.com).</span><span class="sxs-lookup"><span data-stu-id="eb6ec-111">If your organization has a subscription that includes [Office 365 Enterprise](https://docs.microsoft.com/office365/enterprise/), [Microsoft 365 Business](https://docs.microsoft.com/microsoft-365/business/), or Office 365 Business Premium, and you have the [necessary permissions](#required-permissions), you can view your organization's secure score by visiting [https://securescore.office.com](https://securescore.office.com).</span></span> 

<span data-ttu-id="eb6ec-112">Sinon, vous pouvez visiter le centre de conformité de & sécurité ([https://protection.office.com](https://protection.office.com)), où vous trouverez un widget Score sécurisé que vous offre votre score actuel.</span><span class="sxs-lookup"><span data-stu-id="eb6ec-112">Alternatively, you can visit the Security & Compliance Center ([https://protection.office.com](https://protection.office.com)), where you'll find a Secure Score widget that provides you with your current score.</span></span>

![Utilisation du widget Score sécurisé](media/SecureScoreWidget-o365.png)

<span data-ttu-id="eb6ec-114">Le widget inclut un lien vers votre tableau de bord de Score d’informations sécurisé.</span><span class="sxs-lookup"><span data-stu-id="eb6ec-114">The widget includes a link to your Secure Score dashboard.</span></span>

![Tableau de bord de Score d’informations sécurisé](media/SecureScore-WelcomeScreen.png)
  
## <a name="how-it-works"></a><span data-ttu-id="eb6ec-116">Fonctionnement</span><span class="sxs-lookup"><span data-stu-id="eb6ec-116">How it works</span></span>

<span data-ttu-id="eb6ec-p103">Score sécurisé détermine quels services Office 365 que vous utilisez (tels que OneDrive, SharePoint et Exchange) puis compare vos paramètres et les activités à une ligne de base établie par Microsoft. Vous obtiendrez un score qui repose sur la façon de bien aligné à votre organisation est avec les meilleures pratiques de sécurité. Vous aurez également des recommandations sur les étapes à que suivre pour améliorer le score de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="eb6ec-p103">Secure Score determines what Office 365 services you're using (such as OneDrive, SharePoint, and Exchange) then compares your settings and activities to a baseline established by Microsoft. You'll get a score based on how well aligned your organization is with security best practices. You'll also get recommendations on steps you can take to improve your organization's score.</span></span> 
  
![File d’attente des actions dans l’outil Office 365 Secure Score](media/SecureScore-ActionsToTake.png)
  
<span data-ttu-id="eb6ec-p104">Score sécurisé calcule votre note basées sur les services que vous avez acheté. Par exemple, si vous avez acheté uniquement un plan Exchange Online, vous ne sont pas marqués pour les fonctionnalités de sécurité SharePoint Online. Le dénominateur de la note est la somme de toutes les lignes de base pour les contrôles qui s’appliquent aux produits que vous avez acheté. Le numérateur est la somme de tous les contrôles pour lesquels vous, ou partiellement achevée, les actions à réaliser ce contrôle.</span><span class="sxs-lookup"><span data-stu-id="eb6ec-p104">Secure Score calculates your score based on the services you purchased. For example, if you only purchased an Exchange Online plan, you won't be scored for SharePoint Online security features. The denominator of the score is the sum of all the baselines for the controls that apply to the products you purchased. The numerator is the sum of all the controls for which you completed, or partially completed, the actions to fulfill that control.</span></span>

<span data-ttu-id="eb6ec-125">Développez une action pour obtenir des informations sur les étapes à entreprendre, les menaces, il vous aider à vous protégeant contre et le nombre de points votre score augmentera une fois que vous suivez les recommandations.</span><span class="sxs-lookup"><span data-stu-id="eb6ec-125">Expand an action to learn about what steps to take, the threats it'll help protect you from, and how many points your score will increase once you follow the recommendation.</span></span>
  
![Étendue d’action dans l’outil Office 365 Secure Score](media/SecureScore-DetailedActionToTake.png)
  
<span data-ttu-id="eb6ec-127">Pour voir l’impact de vos actions sur la sécurité de votre organisation, sélectionnez l’onglet de **L’Analyseur de Score** et consulter l’historique de vos.</span><span class="sxs-lookup"><span data-stu-id="eb6ec-127">To see the impact of your actions on your organization's security, select the **Score Analyzer** tab and review your history.</span></span> 
  
![Onglet de l’Analyseur de score de l’outil Office 365 Secure Score](media/SecureScore-ScoreAnalyzer-7days.png)
  
<span data-ttu-id="eb6ec-129">Sous le graphique, vous verrez une liste de résultats et les actions par catégorie.</span><span class="sxs-lookup"><span data-stu-id="eb6ec-129">Below the chart, you'll see a list of scores and actions by category.</span></span> 
  
![Sous l’onglet de l’Analyseur de Score affichant un point de données sélectionné du graphique](media/SecureScore-Analyzer-breakdownbelowchart.png)
 
<span data-ttu-id="eb6ec-131">Les actions qui sont étiquetées comme **[Pas notés]** sont ceux que vous pouvez effectuer pour votre organisation, mais car ils ne sont pas connectés au Score d’informations sécurisé, ils ne sont pas notés.</span><span class="sxs-lookup"><span data-stu-id="eb6ec-131">Actions that are labeled as **[Not Scored]** are ones you can perform for your organization, but because they are not connected to Secure Score, they are not scored.</span></span>  

<span data-ttu-id="eb6ec-p105">Dans la page de **L’Analyseur de Score** , cliquez sur un point de données pour un jour spécifique, puis faites défiler jusqu'à voir les actions terminées et incomplètes pour le jour permettant de savoir ce qui est modifiées. Le score est calculé une fois par jour (environ 1:00 AM PST). Si vous apportez une modification à une action mesurée, le résultat sera automatiquement à jour le jour suivant. Jusqu'à 48 heures pour une modification soit répercutée dans votre score nécessaire.</span><span class="sxs-lookup"><span data-stu-id="eb6ec-p105">On the **Score Analyzer** page, click a data point for a specific day, then scroll down to see the completed and incomplete actions for that day to find out what changed. The score is calculated once per day (around 1:00 AM PST). If you make a change to a measured action, the score will automatically update the next day. It takes up to 48 hours for a change to be reflected in your score.</span></span>

<span data-ttu-id="eb6ec-p106">Score sécurisée n’exprime pas une mesure absolue de probable que vous êtes à obtenir franchi. Il exprime l’étendue à laquelle vous avez adopté les fonctionnalités que vous pouvant décaler le risque d’être franchi. Aucun service ne garantit que vous ne serez pas franchi, et le Score d’informations sécurisé ne doit pas être interprété comme une garantie en aucune façon.</span><span class="sxs-lookup"><span data-stu-id="eb6ec-p106">Secure Score does not express an absolute measure of how likely you are to get breached. It expresses the extent to which you have adopted features that can offset the risk of being breached. No service can guarantee that you will not be breached, and the Secure Score should not be interpreted as a guarantee in any way.</span></span>
 
## <a name="how-secure-score-helps"></a><span data-ttu-id="eb6ec-139">Comment permet de sécuriser le Score</span><span class="sxs-lookup"><span data-stu-id="eb6ec-139">How Secure Score helps</span></span>

<span data-ttu-id="eb6ec-p107">Dont le Score d’informations sécurisé, vous pouvez aider à améliorer la sécurité de votre organisation en utilisant les fonctionnalités de sécurité intégrées dans Office 365 (dont beaucoup vous déjà acheté mais ne Sachez pas informés de). En savoir plus sur ces fonctionnalités permettent de tranquillité d’esprit que vous prenez les mesures à protéger votre organisation contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="eb6ec-p107">With Secure Score, you can help improve your organization's security posture by using the built-in security features in Office 365 (many of which you already purchased but might not be aware of). Learning more about these features can help give you peace of mind that you're taking the right steps to protect your organization from threats.</span></span>
  
<span data-ttu-id="eb6ec-p108">Mais ne prennent pas simplement notre word pour qu’il. Clients qui utilisent le Score d’informations sécurisé connaissent leur score augmenter plus que les clients qui ne sont pas à l’aide de cinq reprises. (L’augmentation de leur score correspond avec les fonctionnalités de sécurité utilisées dans leur organisation.)</span><span class="sxs-lookup"><span data-stu-id="eb6ec-p108">But don't just take our word for it. Customers who are using Secure Score have seen their score increase five times more than customers who aren't using it. (The increase in their score corresponds with the security features being used in their organizations.)</span></span>
  
> [!NOTE]
> <span data-ttu-id="eb6ec-p109">Score sécurisée n’exprime pas une mesure absolue de probable que vous êtes à obtenir franchi. Il exprime l’étendue à laquelle vous avez adoptées contrôles dont vous pouvant décaler le risque d’être franchi. Aucun service ne garantit que vous ne serez pas franchi et Score d’informations sécurisé ne doit pas être interprété comme une garantie en aucune façon.</span><span class="sxs-lookup"><span data-stu-id="eb6ec-p109">Secure Score does not express an absolute measure of how likely you are to get breached. It expresses the extent to which you have adopted controls which can offset the risk of being breached. No service can guarantee that you will not be breached, and Secure Score should not be interpreted as a guarantee in any way.</span></span> 
  
## <a name="required-permissions"></a><span data-ttu-id="eb6ec-148">Autorisations requises</span><span class="sxs-lookup"><span data-stu-id="eb6ec-148">Required permissions</span></span>

<span data-ttu-id="eb6ec-149">Pour pouvoir afficher et utiliser votre tableau de bord de Score d’informations sécurisé, vous devez posséder un des rôles suivants dans Azure Active Directory :</span><span class="sxs-lookup"><span data-stu-id="eb6ec-149">In order to view and use your Secure Score dashboard, you must be assigned one of the following roles in Azure Active Directory:</span></span>
- <span data-ttu-id="eb6ec-150">Administrateur général</span><span class="sxs-lookup"><span data-stu-id="eb6ec-150">Global Administrator</span></span>
- <span data-ttu-id="eb6ec-151">Administrateur de facturation</span><span class="sxs-lookup"><span data-stu-id="eb6ec-151">Billing Administrator</span></span>
- <span data-ttu-id="eb6ec-152">Administrateur d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="eb6ec-152">User Administrator</span></span>
- <span data-ttu-id="eb6ec-153">Le mot de passe administrateur</span><span class="sxs-lookup"><span data-stu-id="eb6ec-153">Password Administrator</span></span>
- <span data-ttu-id="eb6ec-154">Administrateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="eb6ec-154">Security Administrator</span></span>
- <span data-ttu-id="eb6ec-155">Lecteur de sécurité</span><span class="sxs-lookup"><span data-stu-id="eb6ec-155">Security Reader</span></span>
- <span data-ttu-id="eb6ec-156">Administrateur Exchange</span><span class="sxs-lookup"><span data-stu-id="eb6ec-156">Exchange Administrator</span></span>
- <span data-ttu-id="eb6ec-157">Administrateur SharePoint</span><span class="sxs-lookup"><span data-stu-id="eb6ec-157">SharePoint Administrator</span></span>

 <span data-ttu-id="eb6ec-158">Les utilisateurs qui ne sont pas affectés à un rôle d’administrateur sera en mesure d’accéder de Score d’informations sécurisé.</span><span class="sxs-lookup"><span data-stu-id="eb6ec-158">Users who aren't assigned an admin role won't be able to access Secure Score.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb6ec-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb6ec-159">Related topics</span></span>

[<span data-ttu-id="eb6ec-160">Vue d’ensemble du tableau de bord de sécurité</span><span class="sxs-lookup"><span data-stu-id="eb6ec-160">Security dashboard overview</span></span>](security-dashboard.md)

[<span data-ttu-id="eb6ec-161">Quel abonnement ai-je ?</span><span class="sxs-lookup"><span data-stu-id="eb6ec-161">What subscription do I have?</span></span>](https://docs.microsoft.com/office365/admin/admin-overview/what-subscription-do-i-have?view=o365-worldwide)