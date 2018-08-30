---
title: Passez en revue les conclusions de découverte d’application dans Office 365 Cloud application sécurité
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 3/19/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: aac65513-e75e-4c82-a668-9a6604dd9f9d
description: Consultation des rapports de détection d’application dans la gestion de la sécurité avancée peut vous aider à en savoir plus sur l’utilisation des applications dans le nuage par les personnes dans votre organisation. Une fois que vous avez créé des rapports de découverte d’application à l’aide de fichiers journaux à partir de votre pare-feu et des proxys, passez en revue les résultats du tableau de bord de détection d’application.
ms.openlocfilehash: 188ef87920b26069e7d99057662b3812be22e46c
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527508"
---
# <a name="review-app-discovery-findings-in-office-365-cloud-app-security"></a><span data-ttu-id="97c83-104">Passez en revue les conclusions de découverte d’application dans Office 365 Cloud application sécurité</span><span class="sxs-lookup"><span data-stu-id="97c83-104">Review app discovery findings in Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="97c83-105">Évaluation **\>**</span><span class="sxs-lookup"><span data-stu-id="97c83-105">****Evaluation** \>**</span></span>|<span data-ttu-id="97c83-106">Planification **\>**</span><span class="sxs-lookup"><span data-stu-id="97c83-106">****Planning** \>**</span></span>|<span data-ttu-id="97c83-107">Déploiement **\>**</span><span class="sxs-lookup"><span data-stu-id="97c83-107">****Deployment** \>**</span></span>|<span data-ttu-id="97c83-108">Utilisation du \*\*\*</span><span class="sxs-lookup"><span data-stu-id="97c83-108">****Utilization****</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="97c83-109">Commencer à évaluer</span><span class="sxs-lookup"><span data-stu-id="97c83-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="97c83-110">Commencer à planifier</span><span class="sxs-lookup"><span data-stu-id="97c83-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="97c83-111">Commencer à déployer</span><span class="sxs-lookup"><span data-stu-id="97c83-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="97c83-112">Vous êtes ici !</span><span class="sxs-lookup"><span data-stu-id="97c83-112">You are here!</span></span>  <br/> [<span data-ttu-id="97c83-113">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="97c83-113">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="97c83-p102">Le tableau de bord dans le nuage découverte fonctionne avec les journaux de trafic web de votre organisation pour fournir des informations détaillées sur l’utilisation des applications dans le nuage. Si vous êtes un administrateur global, un administrateur de sécurité ou un lecteur de sécurité et que votre organisation a [créé des rapports de découverte d’application dans Office 365 Cloud application sécurité](create-app-discovery-reports-in-ocas.md), vous pouvez utiliser le tableau de bord de découverte dans le nuage pour bien comprendre comment les personnes figurant dans votre organisation utilisent Office 365 et autres applications dans le nuage. (Le tableau de bord de découverte dans le nuage est également appelé détection d’application de la productivité).</span><span class="sxs-lookup"><span data-stu-id="97c83-p102">The Cloud Discovery dashboard works with your organization's web traffic logs to provide detailed information about cloud app usage. If you're a global administrator, security administrator, or security reader, and your organization has [created app discovery reports in Office 365 Cloud App Security](create-app-discovery-reports-in-ocas.md), you can use the Cloud Discovery dashboard to gain insight into how people in your organization are using Office 365 and other cloud apps. (The Cloud Discovery dashboard is also known as Productivity App Discovery.)</span></span>
  
 <span data-ttu-id="97c83-117">**À compter de mars 2018, le tableau de bord de découverte dans le nuage offre de nouvelles fonctionnalités** qui vous permet d’afficher des informations détaillées sur comment personnes dans votre organisation sont l’utilisation d’Office 365 et autres applications.</span><span class="sxs-lookup"><span data-stu-id="97c83-117">**As of March 2018, the Cloud Discovery dashboard has new features** that make it easier to view detailed information about how people in your organization are using Office 365 and other apps.</span></span> 
  
![Le tableau de bord dans le nuage découverte a été mis à jour.](media/12712681-c0b3-4cb3-b7fd-2cf2ad4e825f.png)
     
## <a name="go-to-the-cloud-discovery-dashboard"></a><span data-ttu-id="97c83-119">Accédez au tableau de bord de découverte dans le nuage</span><span class="sxs-lookup"><span data-stu-id="97c83-119">Go to the Cloud Discovery dashboard</span></span>

1. <span data-ttu-id="97c83-p103">Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous à l’aide de votre compte professionnel ou de l’école pour Office 365. (Cela vous amène à la sécurité &amp; centre de conformité.)</span><span class="sxs-lookup"><span data-stu-id="97c83-p103">Go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account for Office 365. (This takes you to the Security &amp; Compliance Center.)</span></span> 
    
2. <span data-ttu-id="97c83-122">Dans la sécurité &amp; centre de conformité, sélectionnez **alertes** \> **Gestion avancée des alertes**.</span><span class="sxs-lookup"><span data-stu-id="97c83-122">In the Security &amp; Compliance Center, choose **Alerts** \> **Manage advanced alerts**.</span></span>
    
    <span data-ttu-id="97c83-123">(Si Office 365 Cloud application sécurité n’est pas encore activée, et vous êtes un administrateur global, [Activer la sécurité d’application Office 365 dans le nuage](turn-on-office-365-cas.md).)</span><span class="sxs-lookup"><span data-stu-id="97c83-123">(If Office 365 Cloud App Security is not yet enabled, and you are a global administrator, [turn on Office 365 Cloud App Security](turn-on-office-365-cas.md).)</span></span>
    
3. <span data-ttu-id="97c83-124">Cliquez sur **Aller à la sécurité d’application Office 365 dans le nuage**.</span><span class="sxs-lookup"><span data-stu-id="97c83-124">Choose **Go to Office 365 Cloud App Security**.</span></span>
    
4. <span data-ttu-id="97c83-125">Accédez à **découvrir** \> **tableau de bord de découverte dans le nuage**.</span><span class="sxs-lookup"><span data-stu-id="97c83-125">Go to **Discover** \> **Cloud Discovery dashboard**.</span></span>
    
## <a name="see-your-top-users-ip-addresses-apps-and-risk-levels"></a><span data-ttu-id="97c83-126">Voir vos utilisateurs les plus fréquents, IP les adresses, applications et des niveaux de risques</span><span class="sxs-lookup"><span data-stu-id="97c83-126">See your top users, IP addresses, apps, and risk levels</span></span>

<span data-ttu-id="97c83-127">Le tableau de bord de découverte dans le Cloud vous donne une vue d’ensemble d’un coup de œil des applications qui sont utilisés avec Office 365 dans votre organisation, les alertes actives, utilisateurs les plus fréquents et des niveaux de risques.</span><span class="sxs-lookup"><span data-stu-id="97c83-127">The Cloud Discovery dashboard gives you an at-a-glance overview of apps that are used with Office 365 in your organization, any open alerts, top users, and risk levels.</span></span>
  
![Dashboaard de découverte dans le nuage](media/06696946-fbdf-4781-b5b8-2ac074fcb2a1.png)
  
1. <span data-ttu-id="97c83-129">Sous l’onglet **tableau de bord** , examinez l’utilisation d’application cloud globale de votre organisation dans la section vue d’ensemble dans la partie supérieure de l’écran.</span><span class="sxs-lookup"><span data-stu-id="97c83-129">On the **Dashboard** tab, look at the overall cloud app use in your organization in the overview section across the top of the screen.</span></span> 
    
2. <span data-ttu-id="97c83-130">Afficher les **catégories d’Office 365** pour les applications qui sont utilisés dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="97c83-130">See the **Office 365 categories** for apps that are used in your organization.</span></span> 
    
3. <span data-ttu-id="97c83-131">Examinez le widget **découvert applications** pour voir l’utilisation d’Office 365 et d’autres applications dans cet affichage.</span><span class="sxs-lookup"><span data-stu-id="97c83-131">Look at the **Discovered apps** widget to see usage of Office 365 and other apps in this view.</span></span> 
    
4. <span data-ttu-id="97c83-132">Examinez le widget **d’utilisateurs les plus fréquents** et **adresses IP haut** pour identifier les personnes qui utilisent Office 365 et applications le plus dans votre organisation en nuage.</span><span class="sxs-lookup"><span data-stu-id="97c83-132">Look at the **Top users** and **Top IP addresses** widget to identify those who use Office 365 and cloud apps the most in your organization.</span></span> 
    
5. <span data-ttu-id="97c83-133">Voir où les applications à l’aide de personnes en emplacement géographique à l’aide de la carte **d’emplacements de sièges sociaux d’applications** .</span><span class="sxs-lookup"><span data-stu-id="97c83-133">See where the apps people are using are by geographical location by using the **Apps headquarters location** map.</span></span> 
    
6. <span data-ttu-id="97c83-p104">Au-dessus de la zone cartes, jetez un œil à note des applications découvertes dans la vue d’ensemble **des niveaux de risques** . Vous pouvez examiner les risques des groupes et des catégories que vous avez utilisée dans la zone **applications découvert** . Par exemple, vous pouvez voir la quantité de trafic dans chaque regroupement est à partir d’applications risque élevé, moyen ou faible.</span><span class="sxs-lookup"><span data-stu-id="97c83-p104">Above the maps area, take a look at the risk score of the discovered apps in the **Risk levels** overview. You can look at risks by the same groups and categories that you used in the **Discovered apps** area. For example, you can see how much traffic in each grouping is from high, medium, or low risk apps.</span></span> 
    
## <a name="dive-deeper-into-the-information"></a><span data-ttu-id="97c83-137">Les informations aller plus loin</span><span class="sxs-lookup"><span data-stu-id="97c83-137">Dive deeper into the information</span></span>

<span data-ttu-id="97c83-138">Vous pouvez utiliser dans le nuage découverte pour jetez un œil plus approfondi à des applications, les sous-domaines, les adresses IP et les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="97c83-138">You can use Cloud Discovery to take a deeper look at apps, subdomains, IP addresses, and users.</span></span>
  
1. <span data-ttu-id="97c83-139">Dans le tableau de bord de découverte dans le nuage, choisissez l’onglet **applications découvert** .</span><span class="sxs-lookup"><span data-stu-id="97c83-139">In the Cloud Discovery dashboard, choose the **Discovered apps** tab.</span></span> 
    
2. <span data-ttu-id="97c83-140">Utilisez la section filtres pour afficher les applications par nom, catégorie, au niveau de l’utilisation ou dernière date affichée.</span><span class="sxs-lookup"><span data-stu-id="97c83-140">Use the filters section to view apps by name, category, usage level, or last seen date.</span></span>
    
3. <span data-ttu-id="97c83-141">Dans la liste des résultats, placez le curseur par un nom d’application pour faire apparaître le lien **Afficher les sous-domaines** .</span><span class="sxs-lookup"><span data-stu-id="97c83-141">In the list of results, hover by an app name to reveal the **View sub-domains** link.</span></span> 
    
    ![En regard d’une application pour afficher un lien pour afficher les détails du sous-domaine de pointage](media/4a212215-8a2c-46fd-9ef9-89e4064658a6.png)
  
    <span data-ttu-id="97c83-143">Des informations détaillées sur l’application sélectionnée seront affiche.</span><span class="sxs-lookup"><span data-stu-id="97c83-143">Detailed information about the selected app will appear.</span></span>
    
4. <span data-ttu-id="97c83-144">Pour afficher plus d’informations sur les adresses IP, sélectionnez l’onglet **adresses IP** .</span><span class="sxs-lookup"><span data-stu-id="97c83-144">To view details about IP addresses, choose the **IP addresses** tab.</span></span> 
    
    ![Découverte de nuage affiche des informations détaillées sur les adresses IP](media/0c742bf6-da9e-4d22-8656-a27a5007d5d5.png)
  
    <span data-ttu-id="97c83-146">Dans la liste des résultats, sélectionnez une adresse IP pour afficher des informations plus détaillées.</span><span class="sxs-lookup"><span data-stu-id="97c83-146">In the list of results, select an individual IP address to view more detailed information.</span></span>
    
5. <span data-ttu-id="97c83-147">Pour afficher plus d’informations sur les utilisateurs d’Office 365 au sein de votre organisation, sélectionnez l’onglet **utilisateurs** .</span><span class="sxs-lookup"><span data-stu-id="97c83-147">To view details about Office 365 users within your organization, choose the **Users** tab.</span></span> 
    
    ![Découverte de nuage - informations sur les utilisateurs](media/2d9c2d85-01e6-4057-8020-d9a68f26bbac.png)
  
## <a name="exclude-entities"></a><span data-ttu-id="97c83-149">Exclure les entités</span><span class="sxs-lookup"><span data-stu-id="97c83-149">Exclude entities</span></span>

<span data-ttu-id="97c83-150">Vous pouvez exclure certains utilisateurs du système ou les adresses IP afin de se concentrer sur des informations plus spécifiques.</span><span class="sxs-lookup"><span data-stu-id="97c83-150">You can exclude certain system users or IP addresses in order to focus on more specific information.</span></span>
  
1. <span data-ttu-id="97c83-151">Choisir les **paramètres** \> **paramètres de découverte dans le nuage**.</span><span class="sxs-lookup"><span data-stu-id="97c83-151">Choose **Settings** \> **Cloud Discovery settings**.</span></span>
    
2. <span data-ttu-id="97c83-152">Choisissez **exclure des entités**.</span><span class="sxs-lookup"><span data-stu-id="97c83-152">Choose **Exclude entities**.</span></span>
    
3. <span data-ttu-id="97c83-153">Choisissez **exclu des utilisateurs** ou **des adresses IP exclus**.</span><span class="sxs-lookup"><span data-stu-id="97c83-153">Choose either **Excluded users** or **Excluded IP addresses**.</span></span>
    
4. <span data-ttu-id="97c83-154">Spécifier les utilisateurs ou les adresses IP et dans la zone **commentaires** , tapez les informations sur pourquoi de l’exclusion de ces utilisateurs ou des adresses IP.</span><span class="sxs-lookup"><span data-stu-id="97c83-154">Specify the users or IP addresses, and in the **Comments** box, type information about why you are excluding those users or IP addresses.</span></span> 
    
5. <span data-ttu-id="97c83-155">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="97c83-155">Choose **Add**.</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="97c83-156">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="97c83-156">Next steps</span></span>

- [<span data-ttu-id="97c83-157">Passez en revue et effectuer une action sur les alertes</span><span class="sxs-lookup"><span data-stu-id="97c83-157">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="97c83-158">Créer des rapports de détection d’application</span><span class="sxs-lookup"><span data-stu-id="97c83-158">Create app discovery reports</span></span>](create-app-discovery-reports-in-ocas.md)
    
- <span data-ttu-id="97c83-159">Passez en revue vos [activités utilisation Office 365 nuage sécurité des applications](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="97c83-159">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

