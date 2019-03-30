---
title: Suspendre ou restaurer un compte d’utilisateur dans la sécurité des applications cloud Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 12/03/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 5f02d20f-b9aa-4b2f-ad2d-506a4a3c4540
description: "Avec la sécurité des applications Cloud d'Office 365, les actions de gouvernance que vous pouvez effectuer sont la suspension ou l'annulation de l'interruption d'un compte d'utilisateur. "
ms.openlocfilehash: d162be9d4e5382c6c03c63ae1b30043edbf0295b
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2019
ms.locfileid: "30998867"
---
# <a name="suspend-or-restore-a-user-account-in-office-365-cloud-app-security"></a><span data-ttu-id="dacc2-103">Suspendre ou restaurer un compte d’utilisateur dans la sécurité des applications cloud Office 365</span><span class="sxs-lookup"><span data-stu-id="dacc2-103">Suspend or restore a user account in Office 365 Cloud App Security</span></span>

|<span data-ttu-id="dacc2-104">Évaluation \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="dacc2-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="dacc2-105">Planification \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="dacc2-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="dacc2-106">Déploiement \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="dacc2-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="dacc2-107">Utilisation \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="dacc2-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="dacc2-108">Commencer l'évaluation</span><span class="sxs-lookup"><span data-stu-id="dacc2-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="dacc2-109">Commencer la planification</span><span class="sxs-lookup"><span data-stu-id="dacc2-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="dacc2-110">Démarrer le déploiement</span><span class="sxs-lookup"><span data-stu-id="dacc2-110">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="dacc2-111">Vous êtes là!</span><span class="sxs-lookup"><span data-stu-id="dacc2-111">You are here!</span></span>  <br/> [<span data-ttu-id="dacc2-112">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="dacc2-112">Next steps</span></span>](#next-steps)<br/> |
   
<span data-ttu-id="dacc2-113">Supposons que vous recevez une alerte indiquant qu'un des comptes d'utilisateur de votre organisation pour Office 365 a été compromis.</span><span class="sxs-lookup"><span data-stu-id="dacc2-113">Suppose that you receive an alert that one of your organization's user accounts for Office 365 has been compromised.</span></span> <span data-ttu-id="dacc2-114">Supposons que vous ayez reçu une alerte indiquant un problème lié à un compte d'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dacc2-114">Or, suppose that you've received an alert that indicates something is wrong with a user account.</span></span> <span data-ttu-id="dacc2-115">Avec la sécurité des applications Cloud d'Office 365, vous pouvez suspendre un compte d'utilisateur et le restaurer ultérieurement après avoir étudié les alertes que vous recevez.</span><span class="sxs-lookup"><span data-stu-id="dacc2-115">With Office 365 Cloud App Security, you can suspend a user account and later restore it after you have investigated the alerts you receive.</span></span>
  
> [!NOTE]
> <span data-ttu-id="dacc2-116">Office 365 Cloud App Security est disponible dans Office 365 entreprise E5.</span><span class="sxs-lookup"><span data-stu-id="dacc2-116">Office 365 Cloud App Security is available in Office 365 Enterprise E5.</span></span> <span data-ttu-id="dacc2-117">Si votre organisation utilise un autre abonnement entreprise 365 Enterprise, Office 365 Cloud App Security peut être acheté en tant que module complémentaire.</span><span class="sxs-lookup"><span data-stu-id="dacc2-117">If your organization is using another Office 365 Enterprise subscription, Office 365 Cloud App Security can be purchased as an add-on.</span></span> <span data-ttu-id="dacc2-118">(en tant qu'administrateur général, dans le centre d'administration Microsoft 365, sélectionnez **facturation** \> : **ajouter**des abonnements.) Pour plus d'informations, reportez-vous à [la rubrique office &amp; 365 Platform Service Description: Office 365 Security Compliance Center](https://technet.microsoft.com/en-us/library/dn933793.aspx) et [acheter ou modifier un composant additionnel pour Office 365 pour les entreprises](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).</span><span class="sxs-lookup"><span data-stu-id="dacc2-118">(As a global administrator, in the Microsoft 365 admin center, choose **Billing** \> **Add subscriptions**.) For more information, see [Office 365 Platform Service Description: Office 365 Security &amp; Compliance Center](https://technet.microsoft.com/en-us/library/dn933793.aspx) and [Buy or edit an add-on for Office 365 for business](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).</span></span> 
  
## <a name="to-suspend-a-user-account-in-office-365-cloud-app-security"></a><span data-ttu-id="dacc2-119">Pour suspendre un compte d'utilisateur dans Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="dacc2-119">To suspend a user account in Office 365 Cloud App Security</span></span>

<span data-ttu-id="dacc2-120">Lorsque vous suspendez un compte d'utilisateur, vous empêchez l'utilisateur de se reconnecter.</span><span class="sxs-lookup"><span data-stu-id="dacc2-120">When you suspend a user account, you prevent the user from signing in again.</span></span> <span data-ttu-id="dacc2-121">Il s'agit de la modification du compte d'utilisateur directement dans Office 365 pour définir l'état de connexion **bloqué**.</span><span class="sxs-lookup"><span data-stu-id="dacc2-121">It's the same as editing the user account directly in Office 365 to set the Sign-in status to **Sign-in blocked**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="dacc2-122">Si vous empêchez un utilisateur de se connecter à Office 365, soit en le suspendant, soit en modifiant son statut de connexion, sachez qu'il peut prendre une heure ou pour prendre effet sur tous les appareils et clients de l'utilisateur ([modifier ou modifier un utilisateur dans Office 365](https://support.office.com/article/42BB3F17-8F9D-4182-B434-5F1C8024E614#SingleUserPreview)).</span><span class="sxs-lookup"><span data-stu-id="dacc2-122">If you block a user from signing in to Office 365, either by suspending them or by editing their sign-in status, be aware that it can take an hour or so to take effect on all of the user's devices and clients ([Edit or change a user in Office 365](https://support.office.com/article/42BB3F17-8F9D-4182-B434-5F1C8024E614#SingleUserPreview)).</span></span> <span data-ttu-id="dacc2-123">Si l'utilisateur est connecté à Office 365, le blocage prend effet dès qu'Office 365 le demande de se reconnecter.</span><span class="sxs-lookup"><span data-stu-id="dacc2-123">If the user is signed in to Office 365, the block will take effect whenever Office 365 requires them to sign in again.</span></span> 
  
1. <span data-ttu-id="dacc2-124">En tant qu' [administrateur général ou administrateur de sécurité](permissions-in-the-security-and-compliance-center.md), [https://protection.office.com](https://protection.office.com) accédez à et connectez-vous à l'aide de votre compte professionnel ou scolaire.</span><span class="sxs-lookup"><span data-stu-id="dacc2-124">As a [global administrator or security administrator](permissions-in-the-security-and-compliance-center.md), go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account.</span></span> <span data-ttu-id="dacc2-125">(Vous accédez au centre de sécurité &amp; conformité.)</span><span class="sxs-lookup"><span data-stu-id="dacc2-125">(This takes you to the Security &amp; Compliance Center.)</span></span> 
    
2. <span data-ttu-id="dacc2-126">Dans le centre &amp; de sécurité conformité, sélectionnez **alertes** \> **gérer les alertes avancées**.</span><span class="sxs-lookup"><span data-stu-id="dacc2-126">In the Security &amp; Compliance Center, choose **Alerts** \> **Manage advanced alerts**.</span></span>
    
3. <span data-ttu-id="dacc2-127">Sélectionnez **accéder à la sécurité des applications Cloud Office 365**.</span><span class="sxs-lookup"><span data-stu-id="dacc2-127">Choose **Go to Office 365 Cloud App Security**.</span></span><br><span data-ttu-id="dacc2-128">![Dans le centre &amp; de sécurité conformité, choisissez gérer les alertes avancées pour accéder à la sécurité des applications Cloud Office 365](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span><span class="sxs-lookup"><span data-stu-id="dacc2-128">![In the Security &amp; Compliance Center, choose Manage Advanced Alerts to go to Office 365 Cloud App Security](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span></span><br>
  
4. <span data-ttu-id="dacc2-129">Dans la barre de navigation en haut de l'écran, sélectionnez **alertes**.</span><span class="sxs-lookup"><span data-stu-id="dacc2-129">In the navigation bar across the top of the screen, choose **Alerts**.</span></span>
    
5. <span data-ttu-id="dacc2-130">Dans la colonne **alerte** , double-cliquez sur une alerte qui se rapporte à un compte d'utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="dacc2-130">In the **Alert** column, double-click an alert that pertains to a specific user account.</span></span> 
    
6. <span data-ttu-id="dacc2-131">Sous **comptes**, dans la colonne **État** , sélectionnez icône ![](media/e01b75cc-b28f-4b83-8f86-b1b13dc27ab2.png) \> paramètres des paramètres de l' **utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="dacc2-131">Under **Accounts**, in the **Status** column, choose Settings ![settings icon](media/e01b75cc-b28f-4b83-8f86-b1b13dc27ab2.png) \> **Suspend user**.</span></span>
    
## <a name="to-restore-a-user-account"></a><span data-ttu-id="dacc2-132">Pour restaurer un compte d'utilisateur</span><span class="sxs-lookup"><span data-stu-id="dacc2-132">To restore a user account</span></span>

<span data-ttu-id="dacc2-133">Voir [restaurer un utilisateur dans Office 365](https://support.office.com/article/2c261e42-5dd1-48b0-845f-2a016d29cfc1)</span><span class="sxs-lookup"><span data-stu-id="dacc2-133">See [Restore a user in Office 365](https://support.office.com/article/2c261e42-5dd1-48b0-845f-2a016d29cfc1)</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="dacc2-134">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="dacc2-134">Next steps</span></span>

- [<span data-ttu-id="dacc2-135">Passer en revue et effectuer une action sur les alertes dans la sécurité des applications cloud Office 365</span><span class="sxs-lookup"><span data-stu-id="dacc2-135">Review and take action on alerts in Office 365 Cloud App Security</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="dacc2-136">Gérer les applications OAuth à l’aide de la sécurité des applications cloud Office 365</span><span class="sxs-lookup"><span data-stu-id="dacc2-136">Manage OAuth apps using Office 365 Cloud App Security</span></span>](manage-app-permissions-in-ocas.md)
    
- <span data-ttu-id="dacc2-137">Examiner vos [activités d'utilisation pour Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="dacc2-137">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

