---
title: Passer en revue les détections d'applications dans la sécurité des applications cloud Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: aac65513-e75e-4c82-a668-9a6604dd9f9d
description: Examen des rapports de découverte d'application dans Office 365 Cloud App Security peut vous aider à en savoir plus sur la façon dont les employés de votre organisation utilisent des applications Cloud. Une fois que vous avez créé des rapports de découverte d'application à l'aide de fichiers journaux de vos pare-feu et de vos proxys, examinez les résultats dans le tableau de bord de découverte d'application.
ms.openlocfilehash: f50ad372450b2a1404829eeb6f6964c1d954dccd
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32264962"
---
# <a name="review-app-discovery-findings-in-office-365-cloud-app-security"></a><span data-ttu-id="6d9b7-104">Passer en revue les détections d'applications dans la sécurité des applications cloud Office 365</span><span class="sxs-lookup"><span data-stu-id="6d9b7-104">Review app discovery findings in Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="6d9b7-105">Évaluation \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="6d9b7-105">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="6d9b7-106">Planification \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="6d9b7-106">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="6d9b7-107">Déploiement \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="6d9b7-107">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="6d9b7-108">Utilisation \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="6d9b7-108">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="6d9b7-109">Commencer l'évaluation</span><span class="sxs-lookup"><span data-stu-id="6d9b7-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="6d9b7-110">Commencer la planification</span><span class="sxs-lookup"><span data-stu-id="6d9b7-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="6d9b7-111">Démarrer le déploiement</span><span class="sxs-lookup"><span data-stu-id="6d9b7-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="6d9b7-112">Vous êtes là!</span><span class="sxs-lookup"><span data-stu-id="6d9b7-112">You are here!</span></span>  <br/> [<span data-ttu-id="6d9b7-113">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="6d9b7-113">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="6d9b7-114">Le tableau de bord de découverte du Cloud fonctionne avec les journaux de trafic Web de votre organisation pour fournir des informations détaillées sur l'utilisation des applications Cloud.</span><span class="sxs-lookup"><span data-stu-id="6d9b7-114">The Cloud Discovery dashboard works with your organization's web traffic logs to provide detailed information about cloud app usage.</span></span> <span data-ttu-id="6d9b7-115">Si vous êtes un administrateur général, un administrateur de sécurité ou un lecteur de sécurité, et que votre organisation a [créé des rapports de découverte d'application dans Office 365 Cloud App Security](create-app-discovery-reports-in-ocas.md), vous pouvez utiliser le tableau de bord de découverte de Cloud pour obtenir des informations sur la façon dont les personnes de votre Organisation utilisent Office 365 et d'autres applications Cloud.</span><span class="sxs-lookup"><span data-stu-id="6d9b7-115">If you're a global administrator, security administrator, or security reader, and your organization has [created app discovery reports in Office 365 Cloud App Security](create-app-discovery-reports-in-ocas.md), you can use the Cloud Discovery dashboard to gain insight into how people in your organization are using Office 365 and other cloud apps.</span></span> <span data-ttu-id="6d9b7-116">(Le tableau de bord de découverte du Cloud est également appelé découverte d'application de productivité.)</span><span class="sxs-lookup"><span data-stu-id="6d9b7-116">(The Cloud Discovery dashboard is also known as Productivity App Discovery.)</span></span>
  
 <span data-ttu-id="6d9b7-117">Le tableau de bord de découverte du Cloud vous permet d'afficher des informations détaillées sur la façon dont les membres de votre organisation utilisent Office 365 et d'autres applications.</span><span class="sxs-lookup"><span data-stu-id="6d9b7-117">The Cloud Discovery dashboard enables you to view detailed information about how people in your organization are using Office 365 and other apps.</span></span> 
  
![Le tableau de bord de découverte du Cloud a été mis à jour](media/12712681-c0b3-4cb3-b7fd-2cf2ad4e825f.png)
     
## <a name="go-to-the-cloud-discovery-dashboard"></a><span data-ttu-id="6d9b7-119">Accéder au tableau de bord de découverte Cloud</span><span class="sxs-lookup"><span data-stu-id="6d9b7-119">Go to the Cloud Discovery dashboard</span></span>

1. <span data-ttu-id="6d9b7-120">Accédez au portail de sécurité des applications Cloud[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)() et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="6d9b7-120">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span>
    
2. <span data-ttu-id="6d9b7-121">Accédez à \*\*\*\* \> la vue d' **exploration du tableau de bord de découverte Cloud**.</span><span class="sxs-lookup"><span data-stu-id="6d9b7-121">Go to **Discover** \> **Cloud Discovery dashboard**.</span></span>
    
## <a name="see-your-top-users-ip-addresses-apps-and-risk-levels"></a><span data-ttu-id="6d9b7-122">Afficher les principaux utilisateurs, adresses IP, applications et niveaux de risque</span><span class="sxs-lookup"><span data-stu-id="6d9b7-122">See your top users, IP addresses, apps, and risk levels</span></span>

<span data-ttu-id="6d9b7-123">Le tableau de bord de découverte du Cloud vous donne une vue d'ensemble des applications utilisées avec Office 365 dans votre organisation, des alertes ouvertes, des utilisateurs les plus fréquents et des niveaux de risque.</span><span class="sxs-lookup"><span data-stu-id="6d9b7-123">The Cloud Discovery dashboard gives you an at-a-glance overview of apps that are used with Office 365 in your organization, any open alerts, top users, and risk levels.</span></span>
  
![Recherche dans le Cloud dashboaard](media/06696946-fbdf-4781-b5b8-2ac074fcb2a1.png)
  
1. <span data-ttu-id="6d9b7-125">Dans l'onglet **tableau de bord** , examinez l'ensemble de l'application Cloud dans votre organisation dans la section vue d'ensemble en haut de l'écran.</span><span class="sxs-lookup"><span data-stu-id="6d9b7-125">On the **Dashboard** tab, look at the overall cloud app use in your organization in the overview section across the top of the screen.</span></span> 
    
2. <span data-ttu-id="6d9b7-126">Voir les **catégories Office 365** pour les applications utilisées dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="6d9b7-126">See the **Office 365 categories** for apps that are used in your organization.</span></span> 
    
3. <span data-ttu-id="6d9b7-127">Consultez le widget **applications découvertes** pour consulter l'utilisation d'Office 365 et d'autres applications dans cet affichage.</span><span class="sxs-lookup"><span data-stu-id="6d9b7-127">Look at the **Discovered apps** widget to see usage of Office 365 and other apps in this view.</span></span> 
    
4. <span data-ttu-id="6d9b7-128">Examinez les **principaux utilisateurs** et les **principaux adresses IP** pour identifier les personnes qui utilisent Office 365 et les applications Cloud les plus utilisées dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="6d9b7-128">Look at the **Top users** and **Top IP addresses** widget to identify those who use Office 365 and cloud apps the most in your organization.</span></span> 
    
5. <span data-ttu-id="6d9b7-129">Voir où les applications que les personnes utilisent sont par emplacement géographique à l'aide de la carte d' **emplacement de siège** de l'application.</span><span class="sxs-lookup"><span data-stu-id="6d9b7-129">See where the apps people are using are by geographical location by using the **Apps headquarters location** map.</span></span> 
    
6. <span data-ttu-id="6d9b7-130">Au-dessus de la zone cartes, jetez un œil à la note de risque des applications découvertes dans la section vue d'ensemble des **niveaux de risque** .</span><span class="sxs-lookup"><span data-stu-id="6d9b7-130">Above the maps area, take a look at the risk score of the discovered apps in the **Risk levels** overview.</span></span> <span data-ttu-id="6d9b7-131">Vous pouvez examiner les risques en utilisant les mêmes groupes et catégories que ceux que vous avez utilisés dans la zone **applications découvertes** .</span><span class="sxs-lookup"><span data-stu-id="6d9b7-131">You can look at risks by the same groups and categories that you used in the **Discovered apps** area.</span></span> <span data-ttu-id="6d9b7-132">Par exemple, vous pouvez voir la proportion de trafic dans chaque regroupement provenant d'applications à risque élevé, moyen ou faible.</span><span class="sxs-lookup"><span data-stu-id="6d9b7-132">For example, you can see how much traffic in each grouping is from high, medium, or low risk apps.</span></span> 
    
## <a name="dive-deeper-into-the-information"></a><span data-ttu-id="6d9b7-133">Approfondir les informations</span><span class="sxs-lookup"><span data-stu-id="6d9b7-133">Dive deeper into the information</span></span>

<span data-ttu-id="6d9b7-134">Vous pouvez utiliser la découverte du Cloud pour avoir un aperçu approfondi des applications, des sous-domaines, des adresses IP et des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="6d9b7-134">You can use Cloud Discovery to take a deeper look at apps, subdomains, IP addresses, and users.</span></span>
  
1. <span data-ttu-id="6d9b7-135">Dans le tableau de bord de découverte du Cloud, sélectionnez l'onglet **applications découvertes** .</span><span class="sxs-lookup"><span data-stu-id="6d9b7-135">In the Cloud Discovery dashboard, choose the **Discovered apps** tab.</span></span> 
    
2. <span data-ttu-id="6d9b7-136">Utilisez la section filtres pour afficher les applications par nom, catégorie, niveau d'utilisation ou date de dernière vue.</span><span class="sxs-lookup"><span data-stu-id="6d9b7-136">Use the filters section to view apps by name, category, usage level, or last seen date.</span></span>
    
3. <span data-ttu-id="6d9b7-137">Dans la liste des résultats, placez le curseur sur le nom d'une application pour afficher le lien **afficher les sous-domaines** .</span><span class="sxs-lookup"><span data-stu-id="6d9b7-137">In the list of results, hover by an app name to reveal the **View sub-domains** link.</span></span><br/> <span data-ttu-id="6d9b7-138">![Passer en regard d'une application pour révéler un lien permettant d'afficher les détails d'un sous-domaine](media/4a212215-8a2c-46fd-9ef9-89e4064658a6.png)</span><span class="sxs-lookup"><span data-stu-id="6d9b7-138">![Hover next to an app to reveal a link to view subdomain details](media/4a212215-8a2c-46fd-9ef9-89e4064658a6.png)</span></span><br/><span data-ttu-id="6d9b7-139">Des informations détaillées sur l'application sélectionnée s'affichent.</span><span class="sxs-lookup"><span data-stu-id="6d9b7-139">Detailed information about the selected app will appear.</span></span>
    
4. <span data-ttu-id="6d9b7-140">Pour afficher les détails des adresses IP, cliquez sur l'onglet **adresses IP** .</span><span class="sxs-lookup"><span data-stu-id="6d9b7-140">To view details about IP addresses, choose the **IP addresses** tab.</span></span><br/><span data-ttu-id="6d9b7-141">![La découverte du Cloud affiche des informations détaillées sur les adresses IP](media/0c742bf6-da9e-4d22-8656-a27a5007d5d5.png)</span><span class="sxs-lookup"><span data-stu-id="6d9b7-141">![Cloud Discovery shows detailed information about IP addresses](media/0c742bf6-da9e-4d22-8656-a27a5007d5d5.png)</span></span><br/><span data-ttu-id="6d9b7-142">Dans la liste des résultats, sélectionnez une adresse IP individuelle pour afficher des informations plus détaillées.</span><span class="sxs-lookup"><span data-stu-id="6d9b7-142">In the list of results, select an individual IP address to view more detailed information.</span></span>
    
5. <span data-ttu-id="6d9b7-143">Pour afficher des détails sur les utilisateurs d'Office 365 au sein de votre organisation, cliquez sur l'onglet **utilisateurs** .</span><span class="sxs-lookup"><span data-stu-id="6d9b7-143">To view details about Office 365 users within your organization, choose the **Users** tab.</span></span><br/><span data-ttu-id="6d9b7-144">![Découverte du Cloud: informations sur les utilisateurs](media/2d9c2d85-01e6-4057-8020-d9a68f26bbac.png)</span><span class="sxs-lookup"><span data-stu-id="6d9b7-144">![Cloud Discovery - users info](media/2d9c2d85-01e6-4057-8020-d9a68f26bbac.png)</span></span>
  
## <a name="exclude-entities"></a><span data-ttu-id="6d9b7-145">Exclure des entités</span><span class="sxs-lookup"><span data-stu-id="6d9b7-145">Exclude entities</span></span>

<span data-ttu-id="6d9b7-146">Vous pouvez exclure certains utilisateurs ou adresses IP de votre système afin de vous concentrer sur des informations plus spécifiques.</span><span class="sxs-lookup"><span data-stu-id="6d9b7-146">You can exclude certain system users or IP addresses in order to focus on more specific information.</span></span>
  
1. <span data-ttu-id="6d9b7-147">Choisissez **paramètres** \> de **découverte du Cloud**.</span><span class="sxs-lookup"><span data-stu-id="6d9b7-147">Choose **Settings** \> **Cloud Discovery settings**.</span></span>
    
2. <span data-ttu-id="6d9b7-148">Choisissez **exclure des entités**.</span><span class="sxs-lookup"><span data-stu-id="6d9b7-148">Choose **Exclude entities**.</span></span>
    
3. <span data-ttu-id="6d9b7-149">Choisissez **utilisateurs exclus** ou **adresses IP exclues**.</span><span class="sxs-lookup"><span data-stu-id="6d9b7-149">Choose either **Excluded users** or **Excluded IP addresses**.</span></span>
    
4. <span data-ttu-id="6d9b7-150">Spécifiez les utilisateurs ou les adresses IP, puis dans la zone **Commentaires** , tapez des informations expliquant pourquoi vous excluez ces utilisateurs ou adresses IP.</span><span class="sxs-lookup"><span data-stu-id="6d9b7-150">Specify the users or IP addresses, and in the **Comments** box, type information about why you are excluding those users or IP addresses.</span></span> 
    
5. <span data-ttu-id="6d9b7-151">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="6d9b7-151">Choose **Add**.</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="6d9b7-152">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="6d9b7-152">Next steps</span></span>

- [<span data-ttu-id="6d9b7-153">Passer en revue et effectuer une action sur les alertes</span><span class="sxs-lookup"><span data-stu-id="6d9b7-153">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="6d9b7-154">Créer des rapports de découverte d'application</span><span class="sxs-lookup"><span data-stu-id="6d9b7-154">Create app discovery reports</span></span>](create-app-discovery-reports-in-ocas.md)
    
- <span data-ttu-id="6d9b7-155">Examiner vos [activités d'utilisation pour Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="6d9b7-155">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

