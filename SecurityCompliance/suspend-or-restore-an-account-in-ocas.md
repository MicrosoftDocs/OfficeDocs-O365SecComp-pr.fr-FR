---
title: Suspendre ou restaurer un compte d’utilisateur dans Office 365 Cloud Application Security
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
ms.assetid: 5f02d20f-b9aa-4b2f-ad2d-506a4a3c4540
description: 'Avec Office 365 de sécurité application Cloud, les gouvernance actions possibles sont de suspendre ou reprendre un compte d’utilisateur. '
ms.openlocfilehash: a5c75edefc6ddb87b5676c4253aafe04817f6a1d
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527695"
---
# <a name="suspend-or-restore-a-user-account-in-office-365-cloud-app-security"></a><span data-ttu-id="cf65c-103">Suspendre ou restaurer un compte d’utilisateur dans Office 365 Cloud Application Security</span><span class="sxs-lookup"><span data-stu-id="cf65c-103">Suspend or restore a user account in Office 365 Cloud App Security</span></span>

<span data-ttu-id="cf65c-104">Gestion de la sécurité Office 365 avancée est désormais sécurité d’application Office 365 dans le nuage.</span><span class="sxs-lookup"><span data-stu-id="cf65c-104">Office 365 Advanced Security Management is now Office 365 Cloud App Security.</span></span>
  
|<span data-ttu-id="cf65c-105">Évaluation **\>**</span><span class="sxs-lookup"><span data-stu-id="cf65c-105">****Evaluation** \>**</span></span>|<span data-ttu-id="cf65c-106">Planification **\>**</span><span class="sxs-lookup"><span data-stu-id="cf65c-106">****Planning** \>**</span></span>|<span data-ttu-id="cf65c-107">Déploiement **\>**</span><span class="sxs-lookup"><span data-stu-id="cf65c-107">****Deployment** \>**</span></span>|<span data-ttu-id="cf65c-108">Utilisation du \*\*\*</span><span class="sxs-lookup"><span data-stu-id="cf65c-108">****Utilization****</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="cf65c-109">Commencer à évaluer</span><span class="sxs-lookup"><span data-stu-id="cf65c-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="cf65c-110">Commencer à planifier</span><span class="sxs-lookup"><span data-stu-id="cf65c-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="cf65c-111">Commencer à déployer</span><span class="sxs-lookup"><span data-stu-id="cf65c-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="cf65c-112">Vous êtes ici !</span><span class="sxs-lookup"><span data-stu-id="cf65c-112">You are here!</span></span>  <br/> [<span data-ttu-id="cf65c-113">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="cf65c-113">Next steps</span></span>](suspend-or-restore-an-account-in-ocas.md#nextsteps) <br/> |
   
<span data-ttu-id="cf65c-p101">Supposons que vous recevez une alerte qu’un des comptes d’utilisateurs de votre organisation pour Office 365 a été compromis. Ou bien, supposez que vous avez reçu une alerte indiquant un que problème avec un compte d’utilisateur. Avec Office 365 de sécurité App dans le nuage, vous pouvez suspendre un compte d’utilisateur et restaurer ultérieurement une fois que vous avez examiné les alertes que vous recevez.</span><span class="sxs-lookup"><span data-stu-id="cf65c-p101">Suppose that you receive an alert that one of your organization's user accounts for Office 365 has been compromised. Or, suppose that you've received an alert that indicates something is wrong with a user account. With Office 365 Cloud App Security, you can suspend a user account and later restore it after you have investigated the alerts you receive.</span></span>
  
> [!NOTE]
> <span data-ttu-id="cf65c-p102">Sécurité d’application Office 365 dans le nuage est disponible dans Office 365 entreprise E5. Si votre organisation utilise un autre abonnement Office 365 pour entreprises, Office 365 Cloud application sécurité peut être achetée comme module complémentaire. (En tant qu’administrateur global, dans le centre d’administration Office 365, choisissez **facturation** \> **abonnements Add**.) Pour plus d’informations, voir [Office 365 Platform Service Description : Office 365 sécurité &amp; centre de conformité](https://technet.microsoft.com/en-us/library/dn933793.aspx) et [acheter ou modifier un module complémentaire pour Office 365 pour entreprises](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).</span><span class="sxs-lookup"><span data-stu-id="cf65c-p102">Office 365 Cloud App Security is available in Office 365 Enterprise E5. If your organization is using another Office 365 Enterprise subscription, Office 365 Cloud App Security can be purchased as an add-on. (As a global administrator, in the Office 365 admin center, choose **Billing** \> **Add subscriptions**.) For more information, see [Office 365 Platform Service Description: Office 365 Security &amp; Compliance Center](https://technet.microsoft.com/en-us/library/dn933793.aspx) and [Buy or edit an add-on for Office 365 for business](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).</span></span> 
  
## <a name="to-suspend-a-user-account-in-office-365-cloud-app-security"></a><span data-ttu-id="cf65c-120">Pour suspendre un compte d’utilisateur dans Office 365 Cloud Application Security</span><span class="sxs-lookup"><span data-stu-id="cf65c-120">To suspend a user account in Office 365 Cloud App Security</span></span>

<span data-ttu-id="cf65c-p103">Lorsque vous interrompez un compte d’utilisateur, vous empêchez l’utilisateur de se connecter à nouveau. Il est identique à la modification directement dans Office 365 pour définir le statut de connexion pour la **connexion bloqué**le compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cf65c-p103">When you suspend a user account, you prevent the user from signing in again. It's the same as editing the user account directly in Office 365 to set the Sign-in status to **Sign-in blocked**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="cf65c-p104">Si vous bloquez un utilisateur de se connecter à Office 365, en leur suspension ou en modifiant son statut de connexion, sachez que peut prendre une heure ou afin de prendre effet sur tous les clients ([Modifier un utilisateur dans Office 365](https://support.office.com/article/42BB3F17-8F9D-4182-B434-5F1C8024E614#SingleUserPreview)) et les périphériques de l’utilisateur. Si l’utilisateur est connecté à Office 365, le bloc prendra effet chaque fois qu’Office 365 tenus de se reconnecter.</span><span class="sxs-lookup"><span data-stu-id="cf65c-p104">If you block a user from signing in to Office 365, either by suspending them or by editing their sign-in status, be aware that it can take an hour or so to take effect on all of the user's devices and clients ([Edit or change a user in Office 365](https://support.office.com/article/42BB3F17-8F9D-4182-B434-5F1C8024E614#SingleUserPreview)). If the user is signed in to Office 365, the block will take effect whenever Office 365 requires them to sign in again.</span></span> 
  
1. <span data-ttu-id="cf65c-p105">En tant qu’un [administrateur global ou administrateur de sécurité](permissions-in-the-security-and-compliance-center.md), accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous à l’aide de votre compte professionnel ou de l’école. (Cela vous amène à la sécurité &amp; centre de conformité.)</span><span class="sxs-lookup"><span data-stu-id="cf65c-p105">As a [global administrator or security administrator](permissions-in-the-security-and-compliance-center.md), go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account. (This takes you to the Security &amp; Compliance Center.)</span></span> 
    
2. <span data-ttu-id="cf65c-127">Dans la sécurité &amp; centre de conformité, sélectionnez **alertes** \> **Gestion avancée des alertes**.</span><span class="sxs-lookup"><span data-stu-id="cf65c-127">In the Security &amp; Compliance Center, choose **Alerts** \> **Manage advanced alerts**.</span></span>
    
3. <span data-ttu-id="cf65c-128">Cliquez sur **Aller à la sécurité d’application Office 365 dans le nuage**.</span><span class="sxs-lookup"><span data-stu-id="cf65c-128">Choose **Go to Office 365 Cloud App Security**.</span></span>
    
    ![Dans la sécurité &amp; centre de conformité, cliquez sur Gérer les alertes avancées pour accéder à la sécurité d’application dans le nuage Office 365](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)
  
4. <span data-ttu-id="cf65c-130">Dans la barre de navigation dans la partie supérieure de l’écran, cliquez sur **alertes**.</span><span class="sxs-lookup"><span data-stu-id="cf65c-130">In the navigation bar across the top of the screen, choose **Alerts**.</span></span>
    
5. <span data-ttu-id="cf65c-131">Dans la colonne **alerte** , double-cliquez sur une alerte qui se rapporte à un compte d’utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="cf65c-131">In the **Alert** column, double-click an alert that pertains to a specific user account.</span></span> 
    
6. <span data-ttu-id="cf65c-132">Sous **comptes**, dans la colonne **état** , choisissez paramètres ![icône paramètres](media/e01b75cc-b28f-4b83-8f86-b1b13dc27ab2.png) \> **utilisateur Suspend**.</span><span class="sxs-lookup"><span data-stu-id="cf65c-132">Under **Accounts**, in the **Status** column, choose Settings ![settings icon](media/e01b75cc-b28f-4b83-8f86-b1b13dc27ab2.png) \> **Suspend user**.</span></span>
    
## <a name="to-restore-a-user-account"></a><span data-ttu-id="cf65c-133">Pour restaurer un compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="cf65c-133">To restore a user account</span></span>

<span data-ttu-id="cf65c-134">Reportez-vous à la section [restaurer un utilisateur dans Office 365](https://support.office.com/article/2c261e42-5dd1-48b0-845f-2a016d29cfc1)</span><span class="sxs-lookup"><span data-stu-id="cf65c-134">See [Restore a user in Office 365](https://support.office.com/article/2c261e42-5dd1-48b0-845f-2a016d29cfc1)</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="cf65c-135">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="cf65c-135">Next steps</span></span>

- [<span data-ttu-id="cf65c-136">Passez en revue et effectuer une action sur les alertes de sécurité pour application Cloud Microsoft Office 365</span><span class="sxs-lookup"><span data-stu-id="cf65c-136">Review and take action on alerts in Office 365 Cloud App Security</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="cf65c-137">Gérer les autorisations d’application à l’aide de la sécurité d’application Office 365 dans le nuage</span><span class="sxs-lookup"><span data-stu-id="cf65c-137">Manage app permissions using Office 365 Cloud App Security</span></span>](manage-app-permissions-in-ocas.md)
    
- <span data-ttu-id="cf65c-138">Passez en revue vos [activités utilisation Office 365 nuage sécurité des applications](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="cf65c-138">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

