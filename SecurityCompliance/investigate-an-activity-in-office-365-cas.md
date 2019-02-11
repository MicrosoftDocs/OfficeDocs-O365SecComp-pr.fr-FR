---
title: Examiner une activité concernant la sécurité des applications cloud Office 365
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
ms.assetid: 15fa4545-28b4-4dd4-bf85-88e0926bd5fc
description: 'Avec Office 365 de sécurité App dans le nuage, vous pouvez voir ce qui se passe dans votre environnement Office 365 en observant chargées activités et comptes. '
ms.openlocfilehash: e463323cf28738e1d54fcdb65ed0d15290c79994
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29603655"
---
# <a name="investigate-an-activity-in-office-365-cloud-app-security"></a><span data-ttu-id="a9281-103">Examiner une activité concernant la sécurité des applications cloud Office 365</span><span class="sxs-lookup"><span data-stu-id="a9281-103">Investigate an activity in Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="a9281-104">Évaluation **\>**</span><span class="sxs-lookup"><span data-stu-id="a9281-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="a9281-105">Planification **\>**</span><span class="sxs-lookup"><span data-stu-id="a9281-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="a9281-106">Déploiement **\>**</span><span class="sxs-lookup"><span data-stu-id="a9281-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="a9281-107">Utilisation du \*\*\*</span><span class="sxs-lookup"><span data-stu-id="a9281-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="a9281-108">Commencer à évaluer</span><span class="sxs-lookup"><span data-stu-id="a9281-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="a9281-109">Commencer à planifier</span><span class="sxs-lookup"><span data-stu-id="a9281-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="a9281-110">Commencer à déployer</span><span class="sxs-lookup"><span data-stu-id="a9281-110">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="a9281-111">Vous êtes ici !</span><span class="sxs-lookup"><span data-stu-id="a9281-111">You are here!</span></span>  <br/> [<span data-ttu-id="a9281-112">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="a9281-112">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="a9281-p101">Office 365 Cloud application sécurité fonctionne avec [journal d’audit Office 365](detailed-properties-in-the-office-365-audit-log.md). Avec Office 365 de sécurité application Cloud, comme un administrateur global ou administrateur de la sécurité, vous pouvez utiliser la page journal d’activité pour afficher les problèmes potentiels de la manière dont votre organisation utilise Office 365.</span><span class="sxs-lookup"><span data-stu-id="a9281-p101">Office 365 Cloud App Security works with your [Office 365 audit log](detailed-properties-in-the-office-365-audit-log.md). With Office 365 Cloud App Security, as a global administrator or security administrator, you can use the Activity log page to see potential issues in how your organization is using Office 365.</span></span>
  
## <a name="how-to-get-to-the-activity-log-page"></a><span data-ttu-id="a9281-115">Comment accéder à la page journal d’activité</span><span class="sxs-lookup"><span data-stu-id="a9281-115">How to get to the Activity log page</span></span>

1. <span data-ttu-id="a9281-116">Accédez au portail de sécurité des applications dans le nuage ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) et se connecter.</span><span class="sxs-lookup"><span data-stu-id="a9281-116">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span>
  
2. <span data-ttu-id="a9281-117">Dans la barre de navigation dans la partie supérieure de l’écran, choisissez **examiner** \> **le journal d’activité**.</span><span class="sxs-lookup"><span data-stu-id="a9281-117">In the navigation bar across the top of the screen, choose **Investigate** \> **Activity log**.</span></span><br/><span data-ttu-id="a9281-118">![Dans le portail O365 autorités de certification, cliquez sur examiner.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)</span><span class="sxs-lookup"><span data-stu-id="a9281-118">![In the O365 CAS portal, choose Investigate.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)</span></span>
  
## <a name="review-and-investigate-activities"></a><span data-ttu-id="a9281-119">Passez en revue et examiner les activités</span><span class="sxs-lookup"><span data-stu-id="a9281-119">Review and investigate activities</span></span>

<span data-ttu-id="a9281-p102">Sur la page journal d’activité, vous pouvez voir une liste des différentes activités qui ont lieu au sein de votre organisation à l’aide d’Office 365. Vous pouvez utiliser des filtres dans la partie supérieure de l’écran pour vous concentrer sur un type spécifique d’activité ou d’un utilisateur spécifique. Par exemple, l’image suivante affiche des informations sur la modification du mot de passe du compte d’administrateur d’une organisation Office 365 :</span><span class="sxs-lookup"><span data-stu-id="a9281-p102">On the Activity log page, you can see a list of various activities that are taking place within your organization using Office 365. You can use filters across the top of the screen to focus on a specific type of activity or a specific user. For example, the following image shows information about an organization's Office 365 admin account's password change:</span></span>
  
![Dans Office 365 Cloud application sécurité, choisissez examiner \> le journal d’activité.](media/5d54600c-59cd-4f33-b4f0-29b75c37baae.png)
  
<span data-ttu-id="a9281-p103">Lorsque vous examinez chaque élément dans le journal d’activité, vous pouvez cliquer sur le bouton de sélection pour rechercher les autres activités associées. Par exemple, vous pouvez afficher d’autres activités du même type, à partir de la même adresse IP, ou à partir du même pays ou région.</span><span class="sxs-lookup"><span data-stu-id="a9281-p103">As you look at each item in the Activity log, you can click the ellipses to find other related activities. For example, you can view other activities of the same type, from the same IP address, or from the same country/region.</span></span>
  
<span data-ttu-id="a9281-p104">Vous pouvez afficher des informations sur les nombreux autres types d’activités, trop. Par exemple, voici les activités, que vous pouvez afficher dans le journal d’activité :</span><span class="sxs-lookup"><span data-stu-id="a9281-p104">You can view information about many other kinds of activities, too. For example, here are some of the activities you can view in the Activity log:</span></span>
  
- <span data-ttu-id="a9281-128">Membres ajoutés ou supprimés à partir de groupes</span><span class="sxs-lookup"><span data-stu-id="a9281-128">Members added to or removed from groups</span></span>
    
- <span data-ttu-id="a9281-129">Modifications dans les licences utilisateur</span><span class="sxs-lookup"><span data-stu-id="a9281-129">Changes in user licenses</span></span>
    
- <span data-ttu-id="a9281-130">Fichiers ou dossiers partagés interne ou externe</span><span class="sxs-lookup"><span data-stu-id="a9281-130">Files or folders shared internally or externally</span></span>
    
- <span data-ttu-id="a9281-131">Les sites créés ou supprimés ou les collections de sites</span><span class="sxs-lookup"><span data-stu-id="a9281-131">Created or deleted sites or site collections</span></span>
    
- <span data-ttu-id="a9281-132">Règles de transfert de courrier électronique</span><span class="sxs-lookup"><span data-stu-id="a9281-132">Email forwarding rules</span></span>
    
<span data-ttu-id="a9281-133">Utilisez la page de journal d’activité pour découvrir comment les personnes dans votre organisation utilisent Office 365 et quelles sont les problèmes qu’ils peut-être avoir tout au long du processus.</span><span class="sxs-lookup"><span data-stu-id="a9281-133">Use the Activity log page to get acquainted with how people in your organization are using Office 365 and what issues they might be having along the way.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="a9281-134">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="a9281-134">Next steps</span></span>

- [<span data-ttu-id="a9281-135">Passer en revue et effectuer une action sur les alertes dans la sécurité des applications cloud Office 365</span><span class="sxs-lookup"><span data-stu-id="a9281-135">Review and take action on alerts in Office 365 Cloud App Security</span></span>](review-office-365-cas-alerts.md)
    
- <span data-ttu-id="a9281-136">Passez en revue vos [activités utilisation Office 365 nuage sécurité des applications](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="a9281-136">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

