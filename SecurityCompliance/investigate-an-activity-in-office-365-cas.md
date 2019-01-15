---
title: Examiner une activité concernant la sécurité des applications cloud Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/26/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 15fa4545-28b4-4dd4-bf85-88e0926bd5fc
description: 'Avec Office 365 de sécurité App dans le nuage, vous pouvez voir ce qui se passe dans votre environnement Office 365 en observant chargées activités et comptes. '
ms.openlocfilehash: d988a86c5ceaa2ec46bc27f1aaff540fa3e0b3b4
ms.sourcegitcommit: 9034809b6f308bedc3b8ddcca8242586b5c30f94
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/15/2019
ms.locfileid: "28014896"
---
# <a name="investigate-an-activity-in-office-365-cloud-app-security"></a><span data-ttu-id="b53a3-103">Examiner une activité concernant la sécurité des applications cloud Office 365</span><span class="sxs-lookup"><span data-stu-id="b53a3-103">Investigate an activity in Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="b53a3-104">Évaluation **\>**</span><span class="sxs-lookup"><span data-stu-id="b53a3-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="b53a3-105">Planification **\>**</span><span class="sxs-lookup"><span data-stu-id="b53a3-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="b53a3-106">Déploiement **\>**</span><span class="sxs-lookup"><span data-stu-id="b53a3-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="b53a3-107">Utilisation du \*\*\*</span><span class="sxs-lookup"><span data-stu-id="b53a3-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="b53a3-108">Commencer à évaluer</span><span class="sxs-lookup"><span data-stu-id="b53a3-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="b53a3-109">Commencer à planifier</span><span class="sxs-lookup"><span data-stu-id="b53a3-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="b53a3-110">Commencer à déployer</span><span class="sxs-lookup"><span data-stu-id="b53a3-110">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="b53a3-111">Vous êtes ici !</span><span class="sxs-lookup"><span data-stu-id="b53a3-111">You are here!</span></span>  <br/> [<span data-ttu-id="b53a3-112">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="b53a3-112">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="b53a3-p101">Office 365 Cloud application sécurité fonctionne avec [journal d’audit Office 365](detailed-properties-in-the-office-365-audit-log.md). Avec Office 365 de sécurité application Cloud, comme un administrateur global ou administrateur de la sécurité, vous pouvez utiliser la page journal d’activité pour afficher les problèmes potentiels de la manière dont votre organisation utilise Office 365.</span><span class="sxs-lookup"><span data-stu-id="b53a3-p101">Office 365 Cloud App Security works with your [Office 365 audit log](detailed-properties-in-the-office-365-audit-log.md). With Office 365 Cloud App Security, as a global administrator or security administrator, you can use the Activity log page to see potential issues in how your organization is using Office 365.</span></span>
  
## <a name="how-to-get-to-the-activity-log-page"></a><span data-ttu-id="b53a3-115">Comment accéder à la page journal d’activité</span><span class="sxs-lookup"><span data-stu-id="b53a3-115">How to get to the Activity log page</span></span>

1. <span data-ttu-id="b53a3-p102">En tant qu’un administrateur global ou administrateur de sécurité, accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous à l’aide de votre compte professionnel ou de l’école. (Voir [les autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md).)</span><span class="sxs-lookup"><span data-stu-id="b53a3-p102">As a global administrator or security administrator, go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account. (See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).)</span></span>
    
2. <span data-ttu-id="b53a3-118">Dans la sécurité &amp; centre de conformité, sélectionnez **alertes** \> **Gestion avancée des alertes**.</span><span class="sxs-lookup"><span data-stu-id="b53a3-118">In the Security &amp; Compliance Center, choose **Alerts** \> **Manage advanced alerts**.</span></span>
    
3. <span data-ttu-id="b53a3-119">Cliquez sur **Aller à la sécurité d’application Office 365 dans le nuage**.</span><span class="sxs-lookup"><span data-stu-id="b53a3-119">Choose **Go to Office 365 Cloud App Security**.</span></span><br/><span data-ttu-id="b53a3-120">![Dans la sécurité &amp; centre de conformité, cliquez sur Gérer les alertes avancées pour accéder à la sécurité d’application dans le nuage Office 365](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span><span class="sxs-lookup"><span data-stu-id="b53a3-120">![In the Security &amp; Compliance Center, choose Manage Advanced Alerts to go to Office 365 Cloud App Security](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span></span>
  
4. <span data-ttu-id="b53a3-121">Dans la barre de navigation dans la partie supérieure de l’écran, choisissez **examiner** \> **le journal d’activité**.</span><span class="sxs-lookup"><span data-stu-id="b53a3-121">In the navigation bar across the top of the screen, choose **Investigate** \> **Activity log**.</span></span><br/><span data-ttu-id="b53a3-122">![Dans le portail O365 autorités de certification, cliquez sur examiner.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)</span><span class="sxs-lookup"><span data-stu-id="b53a3-122">![In the O365 CAS portal, choose Investigate.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)</span></span>
  
## <a name="review-and-investigate-activities"></a><span data-ttu-id="b53a3-123">Passez en revue et examiner les activités</span><span class="sxs-lookup"><span data-stu-id="b53a3-123">Review and investigate activities</span></span>

<span data-ttu-id="b53a3-p103">Sur la page journal d’activité, vous pouvez voir une liste des différentes activités qui ont lieu au sein de votre organisation à l’aide d’Office 365. Vous pouvez utiliser des filtres dans la partie supérieure de l’écran pour vous concentrer sur un type spécifique d’activité ou d’un utilisateur spécifique. Par exemple, l’image suivante affiche des informations sur la modification du mot de passe du compte d’administrateur d’une organisation Office 365 :</span><span class="sxs-lookup"><span data-stu-id="b53a3-p103">On the Activity log page, you can see a list of various activities that are taking place within your organization using Office 365. You can use filters across the top of the screen to focus on a specific type of activity or a specific user. For example, the following image shows information about an organization's Office 365 admin account's password change:</span></span>
  
![Dans Office 365 Cloud application sécurité, choisissez examiner \> le journal d’activité.](media/5d54600c-59cd-4f33-b4f0-29b75c37baae.png)
  
<span data-ttu-id="b53a3-p104">Lorsque vous examinez chaque élément dans le journal d’activité, vous pouvez cliquer sur le bouton de sélection pour rechercher les autres activités associées. Par exemple, vous pouvez afficher d’autres activités du même type, à partir de la même adresse IP, ou à partir du même pays ou région.</span><span class="sxs-lookup"><span data-stu-id="b53a3-p104">As you look at each item in the Activity log, you can click the ellipses to find other related activities. For example, you can view other activities of the same type, from the same IP address, or from the same country/region.</span></span>
  
<span data-ttu-id="b53a3-p105">Vous pouvez afficher des informations sur les nombreux autres types d’activités, trop. Par exemple, voici les activités, que vous pouvez afficher dans le journal d’activité :</span><span class="sxs-lookup"><span data-stu-id="b53a3-p105">You can view information about many other kinds of activities, too. For example, here are some of the activities you can view in the Activity log:</span></span>
  
- <span data-ttu-id="b53a3-132">Membres ajoutés ou supprimés à partir de groupes</span><span class="sxs-lookup"><span data-stu-id="b53a3-132">Members added to or removed from groups</span></span>
    
- <span data-ttu-id="b53a3-133">Modifications dans les licences utilisateur</span><span class="sxs-lookup"><span data-stu-id="b53a3-133">Changes in user licenses</span></span>
    
- <span data-ttu-id="b53a3-134">Fichiers ou dossiers partagés interne ou externe</span><span class="sxs-lookup"><span data-stu-id="b53a3-134">Files or folders shared internally or externally</span></span>
    
- <span data-ttu-id="b53a3-135">Les sites créés ou supprimés ou les collections de sites</span><span class="sxs-lookup"><span data-stu-id="b53a3-135">Created or deleted sites or site collections</span></span>
    
- <span data-ttu-id="b53a3-136">Règles de transfert de courrier électronique</span><span class="sxs-lookup"><span data-stu-id="b53a3-136">Email forwarding rules</span></span>
    
<span data-ttu-id="b53a3-137">Utilisez la page de journal d’activité pour découvrir comment les personnes dans votre organisation utilisent Office 365 et quelles sont les problèmes qu’ils peut-être avoir tout au long du processus.</span><span class="sxs-lookup"><span data-stu-id="b53a3-137">Use the Activity log page to get acquainted with how people in your organization are using Office 365 and what issues they might be having along the way.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="b53a3-138">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="b53a3-138">Next steps</span></span>

- [<span data-ttu-id="b53a3-139">Passer en revue et effectuer une action sur les alertes dans la sécurité des applications cloud Office 365</span><span class="sxs-lookup"><span data-stu-id="b53a3-139">Review and take action on alerts in Office 365 Cloud App Security</span></span>](review-office-365-cas-alerts.md)
    
- <span data-ttu-id="b53a3-140">Passez en revue vos [activités utilisation Office 365 nuage sécurité des applications](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="b53a3-140">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

