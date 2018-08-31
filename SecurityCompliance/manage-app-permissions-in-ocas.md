---
title: Gérer les autorisations d’application à l’aide de la sécurité d’application Office 365 dans le nuage
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/22/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 2062c312-b1e4-4ce7-8cb2-ea39bc0dfdad
description: Autorisations d’application dans Office 365 Cloud application sécurité vous aident à gérer les applications de que vos utilisateurs téléchargement pour une utilisation avec des données d’Office 365
ms.openlocfilehash: 7bda35bbbf3a16cd1d386adcb03b1c7c4176913a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528493"
---
# <a name="manage-app-permissions-using-office-365-cloud-app-security"></a><span data-ttu-id="4d11a-103">Gérer les autorisations d’application à l’aide de la sécurité d’application Office 365 dans le nuage</span><span class="sxs-lookup"><span data-stu-id="4d11a-103">Manage app permissions using Office 365 Cloud App Security</span></span>

<span data-ttu-id="4d11a-104">Gestion de la sécurité Office 365 avancée est désormais sécurité d’application Office 365 dans le nuage.</span><span class="sxs-lookup"><span data-stu-id="4d11a-104">Office 365 Advanced Security Management is now Office 365 Cloud App Security.</span></span>
  
|<span data-ttu-id="4d11a-105">Évaluation **\>**</span><span class="sxs-lookup"><span data-stu-id="4d11a-105">****Evaluation** \>**</span></span>|<span data-ttu-id="4d11a-106">Planification **\>**</span><span class="sxs-lookup"><span data-stu-id="4d11a-106">****Planning** \>**</span></span>|<span data-ttu-id="4d11a-107">Déploiement **\>**</span><span class="sxs-lookup"><span data-stu-id="4d11a-107">****Deployment** \>**</span></span>|<span data-ttu-id="4d11a-108">Utilisation du \*\*\*</span><span class="sxs-lookup"><span data-stu-id="4d11a-108">****Utilization****</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="4d11a-109">Commencer à évaluer</span><span class="sxs-lookup"><span data-stu-id="4d11a-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="4d11a-110">Commencer à planifier</span><span class="sxs-lookup"><span data-stu-id="4d11a-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="4d11a-111">Commencer à déployer</span><span class="sxs-lookup"><span data-stu-id="4d11a-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="4d11a-112">Vous êtes ici !</span><span class="sxs-lookup"><span data-stu-id="4d11a-112">You are here!</span></span>  <br/> [<span data-ttu-id="4d11a-113">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="4d11a-113">Next steps</span></span>](manage-app-permissions-in-ocas.md#nextsteps) <br/> |
   
<span data-ttu-id="4d11a-p101">Personnes amour applications et ils les téléchargent souvent, notamment les applications que les employés de réflexion seront gagner du temps en facilitant à leur travail ou établissement des informations. Cependant, certaines applications susceptibles de contenir un risque pour votre organisation, en fonction de quelles informations ils accèdent et comment gérer ces informations. Avec [Office 365 Cloud application sécurité](office-365-cas-overview.md), si vous êtes un administrateur global ou de sécurité, vous pouvez gérer les autorisations d’application pour votre organisation. Vous pouvez voir les applications qui utilisent les données d’Office 365, les autorisations de ces applications ont et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="4d11a-p101">People love apps and they download them often, especially apps that people think will save time by making it easier to get at their work or school information. However, some apps could potentially be a security risk to your organization, depending on what information they access and how they handle that information. With [Office 365 Cloud App Security](office-365-cas-overview.md), if you are a global or security administrator, you can manage app permissions for your organization. You can see the apps people are using with Office 365 data, what permissions those apps have, and more.</span></span> 
  
<span data-ttu-id="4d11a-118">Cet article décrit comment créer une requête de l’application, où aller pour gérer les autorisations d’application et comment approuver ou interdire l’accès à une application.</span><span class="sxs-lookup"><span data-stu-id="4d11a-118">This article describes where to go to manage app permissions, how to approve or ban an app, and how to create an app query.</span></span>
  
## <a name="how-to-find-the-manage-app-permissions-page"></a><span data-ttu-id="4d11a-119">Comment trouver la page Gérer les autorisations application</span><span class="sxs-lookup"><span data-stu-id="4d11a-119">How to find the Manage app permissions page</span></span>
<span data-ttu-id="4d11a-120"><a name="findappperms"> </a></span><span class="sxs-lookup"><span data-stu-id="4d11a-120"></span></span>

> [!NOTE]
> <span data-ttu-id="4d11a-p102">Autorisations d’application sont gérées dans le portail Office 365 Cloud Application Security. Vous devez être un administrateur global ou un administrateur de sécurité pour effectuer la tâche suivante. Pour en savoir plus, consultez [les autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="4d11a-p102">App permissions are managed in the Office 365 Cloud App Security portal. You must be a global administrator or security administrator to perform the following task. To learn more see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
1. <span data-ttu-id="4d11a-p103">Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous à l’aide de votre compte professionnel ou de l’école pour Office 365. (Cela vous amène à la sécurité &amp; centre de conformité.)</span><span class="sxs-lookup"><span data-stu-id="4d11a-p103">Go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account for Office 365. (This takes you to the Security &amp; Compliance Center.)</span></span> 
    
2. <span data-ttu-id="4d11a-126">Accédez à des **alertes** \> **Gestion avancée des alertes**.</span><span class="sxs-lookup"><span data-stu-id="4d11a-126">Go to **Alerts** \> **Manage advanced alerts**.</span></span>
    
3. <span data-ttu-id="4d11a-127">Cliquez (ou appuyez) **accédez à la sécurité d’application Office 365 dans le nuage**.</span><span class="sxs-lookup"><span data-stu-id="4d11a-127">Click (or tap) **Go to Office 365 Cloud App Security**.</span></span>
    
    ![Dans la sécurité &amp; centre de conformité, cliquez sur Gérer les alertes avancées pour accéder à la sécurité d’application dans le nuage Office 365](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)
  
    > [!NOTE]
    > <span data-ttu-id="4d11a-p104">Si la sécurité d’application Office 365 dans le nuage n’est pas encore activée, vous pouvez le faire dans cette page. Consultez [préparer à Office 365 nuage sécurité des applications](get-ready-for-office-365-cas.md).</span><span class="sxs-lookup"><span data-stu-id="4d11a-p104">If Office 365 Cloud App Security is not turned on yet, you can do that on this page. See [Get ready for Office 365 Cloud App Security](get-ready-for-office-365-cas.md).</span></span> 
  
4. <span data-ttu-id="4d11a-131">Cliquez sur **examiner** \> **autorisations d’application**.</span><span class="sxs-lookup"><span data-stu-id="4d11a-131">Choose **Investigate** \> **App permissions**.</span></span>
    
    ![Dans le portail O365 autorités de certification, cliquez sur examiner.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)
  
## <a name="what-youll-see-on-the-manage-app-permissions-page"></a><span data-ttu-id="4d11a-133">Vous verrez sur la page Gérer les autorisations application</span><span class="sxs-lookup"><span data-stu-id="4d11a-133">What you'll see on the Manage app permissions page</span></span>
<span data-ttu-id="4d11a-134"><a name="whatsonpage"> </a></span><span class="sxs-lookup"><span data-stu-id="4d11a-134"></span></span>

<span data-ttu-id="4d11a-135">Le tableau suivant décrit les contrôles et les options disponibles sur la page Gérer les autorisations application.</span><span class="sxs-lookup"><span data-stu-id="4d11a-135">The following table describes the controls and options available on the Manage app permissions page.</span></span>
  
|<span data-ttu-id="4d11a-136">**Élément**</span><span class="sxs-lookup"><span data-stu-id="4d11a-136">**Item**</span></span>|<span data-ttu-id="4d11a-137">**Description**</span><span class="sxs-lookup"><span data-stu-id="4d11a-137">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4d11a-138">Icône de base dans la barre d’application requête</span><span class="sxs-lookup"><span data-stu-id="4d11a-138">Basic icon in the app query bar</span></span>  <br/> ![Icône qui indique le mode de requête de base pour interroger les autorisations d’application](media/a459bc51-e86b-43d5-a0ee-661b9fb4afc9.png)|<span data-ttu-id="4d11a-140">Sélectionnez cette option pour passer à la vue avancée.</span><span class="sxs-lookup"><span data-stu-id="4d11a-140">Select this to switch to the Advanced view.</span></span>  <br/> <span data-ttu-id="4d11a-141">(Si vous voyez **base**, vous utilisez l’affichage avancé)</span><span class="sxs-lookup"><span data-stu-id="4d11a-141">(If you see **Basic**, you are using the Advanced view)</span></span>  <br/> |
|<span data-ttu-id="4d11a-142">Icône avancée dans la barre d’application requête</span><span class="sxs-lookup"><span data-stu-id="4d11a-142">Advanced icon in the app query bar</span></span>  <br/> ![Icône qui indique que la vue de requête pour interroger les autorisations d’application avancée](media/9958d832-2c81-45ed-a642-d926310ba6b6.png)|<span data-ttu-id="4d11a-144">Sélectionnez cette option pour passer à la vue de base.</span><span class="sxs-lookup"><span data-stu-id="4d11a-144">Select this to switch to the Basic view.</span></span>  <br/> <span data-ttu-id="4d11a-145">(Si vous voyez **Avancé**, vous utilisez l’affichage de base.)</span><span class="sxs-lookup"><span data-stu-id="4d11a-145">(If you see **Advanced**, you are using the Basic view.)</span></span>  <br/> |
|<span data-ttu-id="4d11a-146">Ouvrir ou fermer tous les détails icône dans la liste de l’application</span><span class="sxs-lookup"><span data-stu-id="4d11a-146">Open or close all details icon in the app list</span></span>  <br/> ![Cliquez sur cette icône pour ouvrir ou fermer tous les détails pour toutes les applications](media/018fa996-10e8-48ff-986e-55f2b69a5753.png)|<span data-ttu-id="4d11a-148">Sélectionnez cette icône pour afficher plus ou moins plus d’informations sur chaque application.</span><span class="sxs-lookup"><span data-stu-id="4d11a-148">Select this icon to view more or fewer details about each app.</span></span>  <br/> |
|<span data-ttu-id="4d11a-149">Icône d’exportation dans la liste de l’application</span><span class="sxs-lookup"><span data-stu-id="4d11a-149">Export icon in the app list</span></span>  <br/> ![Cliquez sur cette icône pour exporter un fichier csv de toutes les applications](media/98446851-fd96-4d09-9bb0-831db33090c1.png)|<span data-ttu-id="4d11a-151">Sélectionnez cette icône pour exporter un fichier CSV contenant une liste des applications, le nombre d’utilisateurs pour chaque application, les autorisations associées à l’application, le niveau d’autorisation, l’état de l’application, et utiliser le niveau de la Communauté.</span><span class="sxs-lookup"><span data-stu-id="4d11a-151">Select this icon to export a CSV file that contains a list of apps, number of users for each app, permissions associated with the app, permissions level, app state, and community use level.</span></span>  <br/> |
|<span data-ttu-id="4d11a-152">Name</span><span class="sxs-lookup"><span data-stu-id="4d11a-152">Name</span></span>  <br/> |<span data-ttu-id="4d11a-p105">Permet d’afficher le nom d’une application, sélectionnez le nom à afficher plus d’informations, telles que sa description, publisher, site Web d’application et les ID d’application.</span><span class="sxs-lookup"><span data-stu-id="4d11a-p105">Use this to see the name of an app. Select the name to view more information, such as its description, publisher, app website and app ID.</span></span>  <br/> |
|<span data-ttu-id="4d11a-155">Autorisé par</span><span class="sxs-lookup"><span data-stu-id="4d11a-155">Authorized by</span></span>  <br/> |<span data-ttu-id="4d11a-p106">Permet de voir combien d’utilisateurs ont autorisés à une application pour accéder à leur compte Office 365. Sélectionnez le numéro pour afficher plus d’informations, telle qu’une liste des comptes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="4d11a-p106">Use this to see how many users have authorized an app to access their Office 365 account. Select the number to view more information, such as a list of user accounts.</span></span>  <br/> |
|<span data-ttu-id="4d11a-158">Niveau d’autorisation</span><span class="sxs-lookup"><span data-stu-id="4d11a-158">Permissions Level</span></span>  <br/> ![Icône qui indique le niveau de permisiions pour une application](media/aaebdd29-35b6-4c62-aef1-7c7817bd803d.png)|<span data-ttu-id="4d11a-p107">Permet de déterminer le niveau d’accès une application a aux données d’Office 365. Les niveaux d’autorisation indiquent **faible**, **moyen**ou **élevé**, où **faible** peut indiquer que l’application accède uniquement au profil et le nom d’un utilisateur. Sélectionnez le niveau pour afficher plus d’informations, telles que les autorisations accordées à l’application, l’utilisation de la Communauté et activité associé dans le [journal de la gouvernance](suspend-or-restore-an-account-in-ocas.md).</span><span class="sxs-lookup"><span data-stu-id="4d11a-p107">Use this to see how much access an app has to Office 365 data. Permissions levels indicate **Low**, **Medium**, or **High**, where **Low** might indicate that the app only accesses a user's profile and name. Select the level to view more information, such as permissions granted to the app, community use, and related activity in the [Governance log](suspend-or-restore-an-account-in-ocas.md).  </span></span><br/> |
|<span data-ttu-id="4d11a-163">État d’application ( **indéterminé**, **approuvé**ou **exclus**)</span><span class="sxs-lookup"><span data-stu-id="4d11a-163">App state ( **Banned**, **Approved**, or **Undetermined**)</span></span>  <br/> <span data-ttu-id="4d11a-164">![Icônes d’autorisations application une fois autorisés, bloqués ou aucune action n’a été pris par un administrateur](media/5748bd02-cd59-4bd1-a36f-d25a186e8055.png)</span><span class="sxs-lookup"><span data-stu-id="4d11a-164">![App permissions icons after being allowed, blocked, or no action has been taken by an admin](media/5748bd02-cd59-4bd1-a36f-d25a186e8055.png)</span></span>|<span data-ttu-id="4d11a-165">Utiliser cette option pour marquer une application comme approuvé ou exclus, ou conservez l’indéterminée.</span><span class="sxs-lookup"><span data-stu-id="4d11a-165">Use this to mark an app as Approved or Banned, or leave it as undetermined.</span></span>  <br/> |
   
## <a name="mark-an-app-as-approved"></a><span data-ttu-id="4d11a-166">Marquer une application approuvée</span><span class="sxs-lookup"><span data-stu-id="4d11a-166">Mark an app as approved</span></span>
<span data-ttu-id="4d11a-167"><a name="approveapp"> </a></span><span class="sxs-lookup"><span data-stu-id="4d11a-167"></span></span>

<span data-ttu-id="4d11a-168">Dans la page **Gérer les autorisations d’application** , recherchez l’application que vous souhaitez approuver et choisissez l’icône **d’application de marquer comme approuvée** .</span><span class="sxs-lookup"><span data-stu-id="4d11a-168">On the **Manage app permissions** page, locate the app you want to approve, and choose the **Mark app as approved** icon.</span></span> 
  
![Choisissez l’application de la marque sous forme d’icône approuvé](media/dd1b7690-441a-48c9-9c3a-58466513c63d.png)
  
<span data-ttu-id="4d11a-170">L’icône s’affiche en verte et l’application est approuvée pour tous vos utilisateurs Office 365.</span><span class="sxs-lookup"><span data-stu-id="4d11a-170">The icon turns green, and the app is approved for all your Office 365 users.</span></span>
  
> [!NOTE]
> <span data-ttu-id="4d11a-p108">Lorsque vous marquez une application approuvée, il n’a aucun effet sur l’utilisateur final. Visuellement les applications approuvées permet de les séparer des applications qui n’ont pas été vérifiées.</span><span class="sxs-lookup"><span data-stu-id="4d11a-p108">When you mark an app as approved, there is no effect on the end user. Visually marking the apps that are approved helps to separate them from apps that haven't been reviewed yet.</span></span> 
  
## <a name="ban-an-app"></a><span data-ttu-id="4d11a-173">Interdire l’accès à une application</span><span class="sxs-lookup"><span data-stu-id="4d11a-173">Ban an app</span></span>
<span data-ttu-id="4d11a-174"><a name="banapp"> </a></span><span class="sxs-lookup"><span data-stu-id="4d11a-174"></span></span>

1. <span data-ttu-id="4d11a-175">Dans la page **Gérer les autorisations d’application** , recherchez l’application que vous souhaitez interdire et sélectionnez l’icône **application marquer comme interdites** .</span><span class="sxs-lookup"><span data-stu-id="4d11a-175">On the **Manage app permissions** page, locate the app you want to ban, and choose the **Mark app as banned** icon.</span></span> 
    
    ![Choisissez l’application de la marque sous forme d’icône interdit](media/b9b1c5f6-fde7-46d5-8589-1564d05702b3.png)
  
2. <span data-ttu-id="4d11a-177">Indiquez si vous souhaitez permettre aux utilisateurs de connaître interdits par leur application.</span><span class="sxs-lookup"><span data-stu-id="4d11a-177">Choose whether to let users know that their app has been banned.</span></span>
    
    <span data-ttu-id="4d11a-178">(Recommandé) Pour informer les utilisateurs, sélectionnez **avertir les utilisateurs ayant accès à cette application interdite**et comment ajouter ou modifier un message de notification personnalisé.</span><span class="sxs-lookup"><span data-stu-id="4d11a-178">(Recommended) To let users know, select **Notify users who granted access to this banned app**, and add or edit a custom notification message.</span></span>
    
    <span data-ttu-id="4d11a-179">Pour ne pas informer les utilisateurs, désactivez **avertir les utilisateurs ayant accès à cette application interdite**.</span><span class="sxs-lookup"><span data-stu-id="4d11a-179">To not let users know, clear **Notify users who granted access to this banned app**.</span></span>
    
    ![Le modèle de messagerie pour une application interdit](media/6d132700-5f7f-472c-bfb5-a44549e69c16.jpg)
  
3. <span data-ttu-id="4d11a-181">Choisissez **application interdiction**.</span><span class="sxs-lookup"><span data-stu-id="4d11a-181">Choose **Ban app**.</span></span>
    
## <a name="create-an-app-query"></a><span data-ttu-id="4d11a-182">Créer une requête de l’application</span><span class="sxs-lookup"><span data-stu-id="4d11a-182">Create an app query</span></span>
<span data-ttu-id="4d11a-183"><a name="createapp"> </a></span><span class="sxs-lookup"><span data-stu-id="4d11a-183"></span></span>

1. <span data-ttu-id="4d11a-p109">Dans la barre de requête d’application, si vous voyez les **Options avancées**, cliquez sur (ou appuyez sur) pour accéder à la vue avancée. (Si vous voyez Basic, vous utilisez la vue avancée ; conserver votre affichage tel qu’il s’agit.)</span><span class="sxs-lookup"><span data-stu-id="4d11a-p109">In the app query bar, if you see **Advanced**, click (or tap) it to go to the Advanced view. (If you see Basic, you are using the Advanced view; keep your view as it is.)</span></span>
    
2. <span data-ttu-id="4d11a-p110">Utilisez la liste **Sélectionnez un filtre** pour choisir une option. Le tableau suivant récapitule les options de filtre disponibles.</span><span class="sxs-lookup"><span data-stu-id="4d11a-p110">Use the **Select a filter** list to choose an option. The following table summarizes your available filter options.</span></span> 
    
|<span data-ttu-id="4d11a-188">**Utilisez ce filtre**</span><span class="sxs-lookup"><span data-stu-id="4d11a-188">**Use this filter**</span></span>|<span data-ttu-id="4d11a-189">**Pour afficher**</span><span class="sxs-lookup"><span data-stu-id="4d11a-189">**To display**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4d11a-190">**App**</span><span class="sxs-lookup"><span data-stu-id="4d11a-190">**App**</span></span> <br/> |<span data-ttu-id="4d11a-191">Applications avec certains noms</span><span class="sxs-lookup"><span data-stu-id="4d11a-191">Apps with certain names</span></span>  <br/> |
|<span data-ttu-id="4d11a-192">**État de l’application**</span><span class="sxs-lookup"><span data-stu-id="4d11a-192">**App state**</span></span> <br/> |<span data-ttu-id="4d11a-193">Applications en fonction de leur état (approuvé, exclus ou indéterminé)</span><span class="sxs-lookup"><span data-stu-id="4d11a-193">Apps based on their state (Approved, Banned, or Undetermined)</span></span>  <br/> |
|<span data-ttu-id="4d11a-194">**Utilisation de la Communauté**</span><span class="sxs-lookup"><span data-stu-id="4d11a-194">**Community use**</span></span> <br/> |<span data-ttu-id="4d11a-195">Les applications en fonction de la Communauté utiliser niveaux (rares, Uncommon ou commune)</span><span class="sxs-lookup"><span data-stu-id="4d11a-195">Apps based on community use levels (Rare, Uncommon, or Common)</span></span>  <br/> |
|<span data-ttu-id="4d11a-196">**Niveau d’autorisation**</span><span class="sxs-lookup"><span data-stu-id="4d11a-196">**Permission level**</span></span> <br/> |<span data-ttu-id="4d11a-197">En fonction de certains niveaux d’autorisation des applications</span><span class="sxs-lookup"><span data-stu-id="4d11a-197">Apps based on certain permission levels</span></span>  <br/> |
|<span data-ttu-id="4d11a-198">**Autorisations**</span><span class="sxs-lookup"><span data-stu-id="4d11a-198">**Permissions**</span></span> <br/> |<span data-ttu-id="4d11a-199">Applications qui nécessitent certaines autorisations</span><span class="sxs-lookup"><span data-stu-id="4d11a-199">Apps that require certain permissions</span></span>  <br/> |
|<span data-ttu-id="4d11a-200">**Éditeur**</span><span class="sxs-lookup"><span data-stu-id="4d11a-200">**Publisher**</span></span> <br/> |<span data-ttu-id="4d11a-201">Applications à partir de certains éditeurs</span><span class="sxs-lookup"><span data-stu-id="4d11a-201">Apps from certain publishers</span></span>  <br/> |
|<span data-ttu-id="4d11a-202">**User**</span><span class="sxs-lookup"><span data-stu-id="4d11a-202">**User**</span></span> <br/> |<span data-ttu-id="4d11a-203">Applications autorisés d’un utilisateur donné</span><span class="sxs-lookup"><span data-stu-id="4d11a-203">Apps that a certain user authorized</span></span>  <br/> |
   
3. <span data-ttu-id="4d11a-204">Sélectionnez **est égal à** ou **n’est pas égal**, puis spécifiez une valeur pour votre filtre.</span><span class="sxs-lookup"><span data-stu-id="4d11a-204">Select **equals** or **does not equal**, and then specify a value for your filter.</span></span>
    
4. <span data-ttu-id="4d11a-205">Pour ajouter d’autres filtres, sélectionnez le signe plus)</span><span class="sxs-lookup"><span data-stu-id="4d11a-205">To add more filters, select the plus sign (</span></span>![Ajouter une icône de filtre pour l’interrogation d’applications](media/771b2958-67cd-4e14-9302-283ef238cae5.jpg)<span data-ttu-id="4d11a-207">), puis répétez les étapes 2 et 3.</span><span class="sxs-lookup"><span data-stu-id="4d11a-207">), and then repeat steps 2 and 3.</span></span>
    
5. <span data-ttu-id="4d11a-208">Pour supprimer un filtre, sélectionnez le x (</span><span class="sxs-lookup"><span data-stu-id="4d11a-208">To remove a filter, select the x (</span></span>![Supprimer une icône de filtre pour l’interrogation d’applications](media/5339277f-555d-4749-8dcc-d2574250556e.jpg)<span data-ttu-id="4d11a-210">) en regard du nom d’un filtre.</span><span class="sxs-lookup"><span data-stu-id="4d11a-210">) next to a filter name.</span></span>
    
<span data-ttu-id="4d11a-211">Les filtres sont appliqués automatiquement, et la liste des applications est mis à jour en conséquence.</span><span class="sxs-lookup"><span data-stu-id="4d11a-211">The filters are applied automatically, and the apps list is updated accordingly.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="4d11a-212">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="4d11a-212">Next steps</span></span>
<span data-ttu-id="4d11a-213"><a name="nextsteps"> </a></span><span class="sxs-lookup"><span data-stu-id="4d11a-213"></span></span>

- [<span data-ttu-id="4d11a-214">Passez en revue et effectuer une action sur les alertes</span><span class="sxs-lookup"><span data-stu-id="4d11a-214">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- <span data-ttu-id="4d11a-215">Passez en revue vos [sources de données Office 365 nuage sécurité des applications et de journaux de trafic Web](web-traffic-logs-and-data-sources-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="4d11a-215">Review your [Web traffic logs and data sources for Office 365 Cloud App Security](web-traffic-logs-and-data-sources-for-ocas.md)</span></span>
    
- <span data-ttu-id="4d11a-216">Passez en revue vos [activités utilisation Office 365 nuage sécurité des applications](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="4d11a-216">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

