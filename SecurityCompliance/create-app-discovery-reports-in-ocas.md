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
description: Créer des rapports avec Office 365 Cloud App de sécurité qui vous permettent de comprendre comment les personnes dans votre organisation utilisent Office 365 et autres applications.
ms.openlocfilehash: 543a194ec9d441a4feea97b8ad49022094565d7a
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29603715"
---
# <a name="create-app-discovery-reports-using-office-365-cloud-app-security"></a><span data-ttu-id="f5859-103">Créer des rapports de découverte d’application à l’aide de la sécurité des applications cloud Office 365</span><span class="sxs-lookup"><span data-stu-id="f5859-103">Create app discovery reports using Office 365 Cloud App Security</span></span>

<span data-ttu-id="f5859-104">Gestion de la sécurité Office 365 avancée est désormais sécurité d’application Office 365 dans le nuage.</span><span class="sxs-lookup"><span data-stu-id="f5859-104">Office 365 Advanced Security Management is now Office 365 Cloud App Security.</span></span>
  
|<span data-ttu-id="f5859-105">Évaluation **\>**</span><span class="sxs-lookup"><span data-stu-id="f5859-105">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="f5859-106">Planification **\>**</span><span class="sxs-lookup"><span data-stu-id="f5859-106">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="f5859-107">Déploiement **\>**</span><span class="sxs-lookup"><span data-stu-id="f5859-107">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="f5859-108">Utilisation du \*\*\*</span><span class="sxs-lookup"><span data-stu-id="f5859-108">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="f5859-109">Commencer à évaluer</span><span class="sxs-lookup"><span data-stu-id="f5859-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="f5859-110">Commencer à planifier</span><span class="sxs-lookup"><span data-stu-id="f5859-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="f5859-111">Commencer à déployer</span><span class="sxs-lookup"><span data-stu-id="f5859-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="f5859-112">Vous êtes ici !</span><span class="sxs-lookup"><span data-stu-id="f5859-112">You are here!</span></span>  <br/> [<span data-ttu-id="f5859-113">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="f5859-113">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="f5859-p101">Sécurité d’application Office 365 nuage permet les administrateurs globaux, les administrateurs de sécurité et les lecteurs de sécurité Familiarisez-vous avec les services en nuage à l’aide de personnes dans une organisation. Par exemple, vous pouvez voir où les utilisateurs sont le stockage et collaborer sur des documents et la quantité de données est en cours de téléchargement pour les applications ou services qui sont en dehors d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="f5859-p101">Office 365 Cloud App Security helps global administrators, security administrators, and security readers gain insight into the cloud services people in an organization are using. For example, you can see where users are storing and collaborating on documents and how much data is being uploaded to apps or services that are outside of Office 365.</span></span>
  
<span data-ttu-id="f5859-116">Pour générer un rapport de détection d’application, vous téléchargez manuellement vos fichiers de journaux de trafic web à partir de votre pare-feu et des proxys et Office 365 Cloud Application Security analyse et analyse les fichiers pour votre rapport.</span><span class="sxs-lookup"><span data-stu-id="f5859-116">To generate an app discovery report, you manually upload your web traffic log files from your firewalls and proxies, and then Office 365 Cloud App Security parses and analyzes those files for your report.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f5859-p102">Vous devez être un administrateur global, un administrateur de sécurité ou un lecteur de sécurité pour effectuer les tâches décrites dans cet article. Pour plus d’informations, voir [des autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="f5859-p102">You must be a global administrator, security administrator, or security reader to perform the tasks described in this article. To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
## <a name="create-a-report-with-app-discovery"></a><span data-ttu-id="f5859-119">Créer un rapport avec la détection d’application</span><span class="sxs-lookup"><span data-stu-id="f5859-119">Create a report with app discovery</span></span>

<span data-ttu-id="f5859-120">Pour créer un rapport de détection d’application, vous identifiez la source de données de fournisseur pour les fichiers journaux que vous souhaitez avoir analysé, sélectionnez les fichiers journaux et puis demande le rapport.</span><span class="sxs-lookup"><span data-stu-id="f5859-120">To create an app discovery report, you identify the vendor data source for the log files that you want to have analyzed, select the log files, and then request the report.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f5859-121">Utilisez les fichiers journaux de trafic web qui incluent des périodes de trafic de pointe pour obtenir la meilleure représentation d’utilisation dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f5859-121">Use web traffic log files that include peak traffic periods to get the best representation of usage in your organization.</span></span> 
  
1. <span data-ttu-id="f5859-122">Collecter les [journaux de trafic web et des sources de données Office 365 nuage sécurité des applications](web-traffic-logs-and-data-sources-for-ocas.md).</span><span class="sxs-lookup"><span data-stu-id="f5859-122">Collect your [web traffic logs and data sources for Office 365 Cloud App Security](web-traffic-logs-and-data-sources-for-ocas.md).</span></span>
    
2. <span data-ttu-id="f5859-123">Accédez au portail de sécurité des applications dans le nuage ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) et se connecter.</span><span class="sxs-lookup"><span data-stu-id="f5859-123">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span> 
       
3. <span data-ttu-id="f5859-124">Choisissez **découvrir** \> **Création de rapports**.</span><span class="sxs-lookup"><span data-stu-id="f5859-124">Choose **Discover** \> **Create new report**.</span></span> <br><span data-ttu-id="f5859-125">![Dans le portail Office 365 autorités de certification, cliquez sur découvrir](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)</span><span class="sxs-lookup"><span data-stu-id="f5859-125">![In the Office 365 CAS portal, choose Discover](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)</span></span><br>
  
4. <span data-ttu-id="f5859-126">Spécifiez un nom et une description pour votre rapport, puis sélectionnez la source de données pour les journaux de trafic web dans la liste **source de données** .</span><span class="sxs-lookup"><span data-stu-id="f5859-126">Specify a name and description for your report, and then select the data source for your web traffic logs in the **Data source** list.</span></span> <br><span data-ttu-id="f5859-127">![Dans les autorités de certification O365, choisissez découvrir \> créer le nouveau rapport](media/22e660f0-5eb2-49fa-9fea-f88a5809a07b.png)</span><span class="sxs-lookup"><span data-stu-id="f5859-127">![In O365 CAS, choose Discover \> Create new report](media/22e660f0-5eb2-49fa-9fea-f88a5809a07b.png)</span></span><br><span data-ttu-id="f5859-p103">Si une source de données que vous souhaitez utiliser n’est pas répertoriée, vous pouvez demander que, il doit être ajouté. Sélectionnez **autre** pour la **source de données**, puis tapez le nom de la source de données que vous essayez de télécharger. Nous allons consulter le journal et vous permettent de savoir si nous ajouter la prise en charge pour la source de données qui l’a généré.</span><span class="sxs-lookup"><span data-stu-id="f5859-p103">If a data source that you'd like to use is not listed, you can request that it be added. Select **Other** for **Data source**, and then type the name of the data source that you're trying to upload. We'll review the log, and let you know if we add support for the data source that generated it.</span></span> 
  
5. <span data-ttu-id="f5859-p104">Accédez à l’emplacement des fichiers journaux que vous avez collecté et sélectionnez les fichiers. Les fichiers journaux doivent avoir été générées par la source de données que vous avez choisi pour le rapport.</span><span class="sxs-lookup"><span data-stu-id="f5859-p104">Browse to the location of the log files you collected and select the files. The log files must have been generated by the data source that you chose for the report.</span></span>
    
6. <span data-ttu-id="f5859-133">Cliquez sur **créer** pour démarrer le processus de création de rapport.</span><span class="sxs-lookup"><span data-stu-id="f5859-133">Click **Create** to start the report creation process.</span></span> 
    
7. <span data-ttu-id="f5859-p105">Pour afficher le statut du rapport, cliquez sur **Gérer les rapports de capture instantanée**. Lorsqu’un état est prêt, vous verrez l’option **Afficher l’état** .</span><span class="sxs-lookup"><span data-stu-id="f5859-p105">To see the status of the report, click **Manage snapshot reports**. When a report is ready, you'll see the **View report** option.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="f5859-136">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="f5859-136">Next steps</span></span>

- [<span data-ttu-id="f5859-137">Passez en revue et effectuer une action sur les alertes</span><span class="sxs-lookup"><span data-stu-id="f5859-137">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="f5859-138">Passer en revue les détections d'applications dans la sécurité des applications cloud Office 365</span><span class="sxs-lookup"><span data-stu-id="f5859-138">Review app discovery findings in Office 365 Cloud App Security</span></span>](review-app-discovery-findings-in-ocas.md)
    
- <span data-ttu-id="f5859-139">Passez en revue vos [activités utilisation Office 365 nuage sécurité des applications](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="f5859-139">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

