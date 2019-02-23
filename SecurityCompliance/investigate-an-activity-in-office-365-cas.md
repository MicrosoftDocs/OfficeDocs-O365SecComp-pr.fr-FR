---
title: Examiner une activité concernant la sécurité des applications cloud Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 1/28/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 15fa4545-28b4-4dd4-bf85-88e0926bd5fc
description: "Avec la sécurité des applications Cloud d'Office 365, vous pouvez voir ce qui se passe dans votre environnement Office 365 en consultant et en examinant les activités et les comptes. "
ms.openlocfilehash: 0cc3860d953b40b0b0c247af6fb2b157d1abb235
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218964"
---
# <a name="investigate-an-activity-in-office-365-cloud-app-security"></a><span data-ttu-id="f756d-103">Examiner une activité concernant la sécurité des applications cloud Office 365</span><span class="sxs-lookup"><span data-stu-id="f756d-103">Investigate an activity in Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="f756d-104">Évaluation \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="f756d-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="f756d-105">Planification \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="f756d-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="f756d-106">Déploiement \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="f756d-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="f756d-107">Utilisation \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="f756d-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="f756d-108">Commencer l'évaluation</span><span class="sxs-lookup"><span data-stu-id="f756d-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="f756d-109">Commencer la planification</span><span class="sxs-lookup"><span data-stu-id="f756d-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="f756d-110">Démarrer le déploiement</span><span class="sxs-lookup"><span data-stu-id="f756d-110">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="f756d-111">Vous êtes là!</span><span class="sxs-lookup"><span data-stu-id="f756d-111">You are here!</span></span>  <br/> [<span data-ttu-id="f756d-112">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="f756d-112">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="f756d-p101">Office 365 Cloud App Security fonctionne avec votre [Journal d'audit office 365](detailed-properties-in-the-office-365-audit-log.md). Avec la sécurité des applications Cloud d'Office 365, en tant qu'administrateur général ou administrateur de sécurité, vous pouvez utiliser la page journal des activités pour voir les problèmes potentiels liés à la façon dont votre organisation utilise Office 365.</span><span class="sxs-lookup"><span data-stu-id="f756d-p101">Office 365 Cloud App Security works with your [Office 365 audit log](detailed-properties-in-the-office-365-audit-log.md). With Office 365 Cloud App Security, as a global administrator or security administrator, you can use the Activity log page to see potential issues in how your organization is using Office 365.</span></span>
  
## <a name="how-to-get-to-the-activity-log-page"></a><span data-ttu-id="f756d-115">Comment accéder à la page du journal des activités</span><span class="sxs-lookup"><span data-stu-id="f756d-115">How to get to the Activity log page</span></span>

1. <span data-ttu-id="f756d-116">Accédez au portail de sécurité des applications Cloud[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)() et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="f756d-116">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span>
  
2. <span data-ttu-id="f756d-117">Dans la barre de navigation en haut de l'écran, choisissez **analyser** \> le **Journal d'activité**.</span><span class="sxs-lookup"><span data-stu-id="f756d-117">In the navigation bar across the top of the screen, choose **Investigate** \> **Activity log**.</span></span><br/><span data-ttu-id="f756d-118">![Dans le portail CAS d'O365, sélectionnez enquête.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)</span><span class="sxs-lookup"><span data-stu-id="f756d-118">![In the O365 CAS portal, choose Investigate.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)</span></span>
  
## <a name="review-and-investigate-activities"></a><span data-ttu-id="f756d-119">Examiner et examiner les activités</span><span class="sxs-lookup"><span data-stu-id="f756d-119">Review and investigate activities</span></span>

<span data-ttu-id="f756d-p102">Sur la page journal des activités, vous pouvez voir la liste des différentes activités qui ont lieu au sein de votre organisation à l'aide d'Office 365. Vous pouvez utiliser des filtres dans la partie supérieure de l'écran pour vous concentrer sur un type d'activité spécifique ou un utilisateur spécifique. Par exemple, l'image suivante affiche des informations sur la modification du mot de passe d'un compte d'administrateur Office 365:</span><span class="sxs-lookup"><span data-stu-id="f756d-p102">On the Activity log page, you can see a list of various activities that are taking place within your organization using Office 365. You can use filters across the top of the screen to focus on a specific type of activity or a specific user. For example, the following image shows information about an organization's Office 365 admin account's password change:</span></span>
  
![Dans la sécurité des applications Cloud Office 365, \> sélectionnez examiner le journal d'activité.](media/5d54600c-59cd-4f33-b4f0-29b75c37baae.png)
  
<span data-ttu-id="f756d-p103">Lorsque vous examinez chaque élément dans le journal d'activité, vous pouvez cliquer sur les ellipses pour rechercher d'autres activités connexes. Par exemple, vous pouvez afficher les autres activités du même type, à partir de la même adresse IP ou à partir du même pays/région.</span><span class="sxs-lookup"><span data-stu-id="f756d-p103">As you look at each item in the Activity log, you can click the ellipses to find other related activities. For example, you can view other activities of the same type, from the same IP address, or from the same country/region.</span></span>
  
<span data-ttu-id="f756d-p104">Vous pouvez également afficher des informations sur de nombreux autres types d'activités. Par exemple, voici quelques-unes des activités que vous pouvez afficher dans le journal d'activité:</span><span class="sxs-lookup"><span data-stu-id="f756d-p104">You can view information about many other kinds of activities, too. For example, here are some of the activities you can view in the Activity log:</span></span>
  
- <span data-ttu-id="f756d-128">Membres ajoutés ou supprimés des groupes</span><span class="sxs-lookup"><span data-stu-id="f756d-128">Members added to or removed from groups</span></span>
    
- <span data-ttu-id="f756d-129">Modifications apPortées aux licences utilisateur</span><span class="sxs-lookup"><span data-stu-id="f756d-129">Changes in user licenses</span></span>
    
- <span data-ttu-id="f756d-130">Fichiers ou dossiers partagés en interne ou en externe</span><span class="sxs-lookup"><span data-stu-id="f756d-130">Files or folders shared internally or externally</span></span>
    
- <span data-ttu-id="f756d-131">Sites ou collections de sites créés ou supprimés</span><span class="sxs-lookup"><span data-stu-id="f756d-131">Created or deleted sites or site collections</span></span>
    
- <span data-ttu-id="f756d-132">Règles de transfert de courrier électronique</span><span class="sxs-lookup"><span data-stu-id="f756d-132">Email forwarding rules</span></span>
    
<span data-ttu-id="f756d-133">Utilisez la page journal des activités pour vous familiariser avec la façon dont les membres de votre organisation utilisent Office 365 et les problèmes qu'ils peuvent rencontrer.</span><span class="sxs-lookup"><span data-stu-id="f756d-133">Use the Activity log page to get acquainted with how people in your organization are using Office 365 and what issues they might be having along the way.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="f756d-134">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="f756d-134">Next steps</span></span>

- [<span data-ttu-id="f756d-135">Passer en revue et effectuer une action sur les alertes dans la sécurité des applications cloud Office 365</span><span class="sxs-lookup"><span data-stu-id="f756d-135">Review and take action on alerts in Office 365 Cloud App Security</span></span>](review-office-365-cas-alerts.md)
    
- <span data-ttu-id="f756d-136">Examiner vos [activités d'utilisation pour Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="f756d-136">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

