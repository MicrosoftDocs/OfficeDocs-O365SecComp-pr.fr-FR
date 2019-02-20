---
title: Créer des rapports de découverte d’application à l’aide de la sécurité des applications cloud Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 1/28/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 3e68e691-1fc4-4d3e-a2c0-d3134eb64055
description: Créer des rapports avec la sécurité des applications Cloud Office 365 qui vous permettent de comprendre comment les personnes de votre organisation utilisent Office 365 et d'autres applications.
ms.openlocfilehash: e0d515ddd9b08aa4a70276177060f273cc89949e
ms.sourcegitcommit: 8679937354c1d8870ecd41519a59d2d7468c23c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2019
ms.locfileid: "30087293"
---
# <a name="create-app-discovery-reports-using-office-365-cloud-app-security"></a><span data-ttu-id="2553f-103">Créer des rapports de découverte d’application à l’aide de la sécurité des applications cloud Office 365</span><span class="sxs-lookup"><span data-stu-id="2553f-103">Create app discovery reports using Office 365 Cloud App Security</span></span>

|<span data-ttu-id="2553f-104">Évaluation \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="2553f-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="2553f-105">Planification \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="2553f-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="2553f-106">Déploiement \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="2553f-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="2553f-107">Utilisation \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="2553f-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="2553f-108">Commencer l'évaluation</span><span class="sxs-lookup"><span data-stu-id="2553f-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="2553f-109">Commencer la planification</span><span class="sxs-lookup"><span data-stu-id="2553f-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="2553f-110">Démarrer le déploiement</span><span class="sxs-lookup"><span data-stu-id="2553f-110">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="2553f-111">Vous êtes là!</span><span class="sxs-lookup"><span data-stu-id="2553f-111">You are here!</span></span>  <br/> [<span data-ttu-id="2553f-112">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="2553f-112">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="2553f-p101">Office 365 Cloud App Security aide les administrateurs généraux, les administrateurs de sécurité et les lecteurs de sécurité à obtenir des informations sur les services Cloud que les utilisateurs d'une organisation utilisent. Par exemple, vous pouvez voir où les utilisateurs stockent et collaborent sur des documents et la proportion de données téléchargées vers des applications ou des services qui se trouvent en dehors d'Office 365.</span><span class="sxs-lookup"><span data-stu-id="2553f-p101">Office 365 Cloud App Security helps global administrators, security administrators, and security readers gain insight into the cloud services people in an organization are using. For example, you can see where users are storing and collaborating on documents and how much data is being uploaded to apps or services that are outside of Office 365.</span></span>
  
<span data-ttu-id="2553f-115">Pour générer un rapport de découverte d'application, vous devez charger manuellement vos fichiers journaux de trafic Web à partir de vos pare-feu et de vos proxys, puis Office 365 Cloud App Security analyse et analyse ces fichiers pour votre rapport.</span><span class="sxs-lookup"><span data-stu-id="2553f-115">To generate an app discovery report, you manually upload your web traffic log files from your firewalls and proxies, and then Office 365 Cloud App Security parses and analyzes those files for your report.</span></span>
  
> [!NOTE]
> <span data-ttu-id="2553f-p102">Vous devez être un administrateur général, un administrateur de sécurité ou un lecteur de sécurité pour effectuer les tâches décrites dans cet article. Pour en savoir plus, consultez [la rubrique autorisations dans le &amp; Centre de sécurité conformité Office 365](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="2553f-p102">You must be a global administrator, security administrator, or security reader to perform the tasks described in this article. To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
## <a name="create-a-report-with-app-discovery"></a><span data-ttu-id="2553f-118">Créer un rapport avec la découverte des applications</span><span class="sxs-lookup"><span data-stu-id="2553f-118">Create a report with app discovery</span></span>

<span data-ttu-id="2553f-119">Pour créer un rapport de découverte d'application, identifiez la source de données du fournisseur pour les fichiers journaux que vous souhaitez analyser, sélectionnez les fichiers journaux, puis demandez le rapport.</span><span class="sxs-lookup"><span data-stu-id="2553f-119">To create an app discovery report, you identify the vendor data source for the log files that you want to have analyzed, select the log files, and then request the report.</span></span>
  
> [!NOTE]
> <span data-ttu-id="2553f-120">Utilisez les fichiers journaux du trafic Web qui incluent des périodes de trafic maximale pour obtenir la meilleure représentation de l'utilisation dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="2553f-120">Use web traffic log files that include peak traffic periods to get the best representation of usage in your organization.</span></span> 
  
1. <span data-ttu-id="2553f-121">Collectez vos [journaux de trafic Web et sources de données pour la sécurité des applications Cloud Office 365](web-traffic-logs-and-data-sources-for-ocas.md).</span><span class="sxs-lookup"><span data-stu-id="2553f-121">Collect your [web traffic logs and data sources for Office 365 Cloud App Security](web-traffic-logs-and-data-sources-for-ocas.md).</span></span>
    
2. <span data-ttu-id="2553f-122">Accédez au portail de sécurité des applications Cloud[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)() et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="2553f-122">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span> 
       
3. <span data-ttu-id="2553f-123">Sélectionnez **Discover** \> **créer un rapport**.</span><span class="sxs-lookup"><span data-stu-id="2553f-123">Choose **Discover** \> **Create new report**.</span></span> <br><span data-ttu-id="2553f-124">![Dans le portail Office 365 CAS, sélectionnez découvrir](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)</span><span class="sxs-lookup"><span data-stu-id="2553f-124">![In the Office 365 CAS portal, choose Discover](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)</span></span><br>
  
4. <span data-ttu-id="2553f-125">Spécifiez un nom et une description pour votre rapport, puis sélectionnez la source de données pour vos journaux de trafic Web dans la liste **source de données** .</span><span class="sxs-lookup"><span data-stu-id="2553f-125">Specify a name and description for your report, and then select the data source for your web traffic logs in the **Data source** list.</span></span> <br><span data-ttu-id="2553f-126">![Dans les autorités de certification O365 \> , choisissez découvrir créer un rapport](media/22e660f0-5eb2-49fa-9fea-f88a5809a07b.png)</span><span class="sxs-lookup"><span data-stu-id="2553f-126">![In O365 CAS, choose Discover \> Create new report](media/22e660f0-5eb2-49fa-9fea-f88a5809a07b.png)</span></span><br><span data-ttu-id="2553f-p103">Si une source de données que vous souhaitez utiliser n'est pas disponible, vous pouvez demander son ajout. Sélectionnez **autre** pour **source de données**, puis tapez le nom de la source de données que vous essayez de télécharger. Nous allons examiner le journal et vous indiquer si nous ajoutons la prise en charge de la source de données qui l'a générée.</span><span class="sxs-lookup"><span data-stu-id="2553f-p103">If a data source that you'd like to use is not listed, you can request that it be added. Select **Other** for **Data source**, and then type the name of the data source that you're trying to upload. We'll review the log, and let you know if we add support for the data source that generated it.</span></span> 
  
5. <span data-ttu-id="2553f-p104">Naviguez jusqu'à l'emplacement des fichiers journaux que vous avez collectés et sélectionnez les fichiers. Les fichiers journaux doivent avoir été générés par la source de données que vous avez choisie pour le rapport.</span><span class="sxs-lookup"><span data-stu-id="2553f-p104">Browse to the location of the log files you collected and select the files. The log files must have been generated by the data source that you chose for the report.</span></span>
    
6. <span data-ttu-id="2553f-132">Cliquez sur **créer** pour démarrer le processus de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="2553f-132">Click **Create** to start the report creation process.</span></span> 
    
7. <span data-ttu-id="2553f-p105">Pour afficher l'état du rapport, cliquez sur **gérer les rapports de capture instantanée**. Lorsqu'un État est prêt, l'option Afficher le **rapport** s'affiche.</span><span class="sxs-lookup"><span data-stu-id="2553f-p105">To see the status of the report, click **Manage snapshot reports**. When a report is ready, you'll see the **View report** option.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="2553f-135">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="2553f-135">Next steps</span></span>

- [<span data-ttu-id="2553f-136">Passer en revue et effectuer une action sur les alertes</span><span class="sxs-lookup"><span data-stu-id="2553f-136">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="2553f-137">Passer en revue les détections d'applications dans la sécurité des applications cloud Office 365</span><span class="sxs-lookup"><span data-stu-id="2553f-137">Review app discovery findings in Office 365 Cloud App Security</span></span>](review-app-discovery-findings-in-ocas.md)
    
- <span data-ttu-id="2553f-138">Examiner vos [activités d'utilisation pour Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="2553f-138">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

