---
title: Suppression d’un utilisateur du portail Utilisateurs restreints après l’envoi d’un courrier indésirable
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 03/12/2019
audience: ITPro
ms.topic: article
f1_keywords:
- ms.exch.eac.ActionCenter.Restricted.Users.RestrictedUsers
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 712cfcc1-31e8-4e51-8561-b64258a8f1e5
ms.collection:
- M365-security-compliance
description: Si un utilisateur envoie continuellement des courriers électroniques à partir d’Office 365 classés comme courrier indésirable, il ne pourra pas envoyer d’autres messages.
ms.openlocfilehash: 7a44ff7f2bcf88f2132ee4c372cc11b9657dd16a
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34157246"
---
# <a name="removing-a-user-from-the-restricted-users-portal-after-sending-spam-email"></a><span data-ttu-id="4df31-103">Suppression d’un utilisateur du portail Utilisateurs restreints après l’envoi d’un courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="4df31-103">Removing a user from the Restricted Users portal after sending spam email</span></span>

<span data-ttu-id="4df31-104">Si un utilisateur envoie continuellement des courriers électroniques à partir d’Office 365 classés comme courrier indésirable, il ne sera pas autorisé à envoyer d’autres messages sortants.</span><span class="sxs-lookup"><span data-stu-id="4df31-104">If a user continuously sends emails from Office 365 that are classified as spam, they will be restricted from sending any more messages outbound.</span></span> <span data-ttu-id="4df31-105">L’utilisateur est mentionné dans le service en tant qu’expéditeur sortant incorrect et reçoit une notification d’échec de remise qui indique:</span><span class="sxs-lookup"><span data-stu-id="4df31-105">The user will be listed in the service as a bad outbound sender and will receive a Non-Delivery Report (NDR) that states:</span></span>

- <span data-ttu-id="4df31-106">Votre message n’a pas pu être remis car vous n’avez pas été reconnu comme un expéditeur valide.</span><span class="sxs-lookup"><span data-stu-id="4df31-106">Your message couldn't be delivered because you weren't recognized as a valid sender.</span></span> <span data-ttu-id="4df31-107">La raison la plus fréquente de ce message est que votre adresse de courrier est suspecte d’envoyer du courrier indésirable et qu’elle n’est plus autorisée à envoyer des messages en dehors de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="4df31-107">The most common reason for this is that your email address is suspected of sending spam and it's no longer allowed to send messages outside of your organization.</span></span> <span data-ttu-id="4df31-108">Contactez votre administrateur de courrier électronique pour obtenir de l’aide.</span><span class="sxs-lookup"><span data-stu-id="4df31-108">Contact your email admin for assistance.</span></span> <span data-ttu-id="4df31-109">Le serveur distant a renvoyé' 550 5.1.8 accès refusé, expéditeur sortant incorrect "</span><span class="sxs-lookup"><span data-stu-id="4df31-109">Remote Server returned '550 5.1.8 Access denied, bad outbound sender'</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="4df31-110">Ce qu’il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="4df31-110">What do you need to know before you begin?</span></span>
<span data-ttu-id="4df31-111"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="4df31-111"></span></span>

<span data-ttu-id="4df31-112">Durée d'exécution estimée : 5 minutes</span><span class="sxs-lookup"><span data-stu-id="4df31-112">Estimated time to complete: 5 minutes</span></span>
  
<span data-ttu-id="4df31-113">Des autorisations doivent vous être attribuées avant de pouvoir exécuter cette procédure.</span><span class="sxs-lookup"><span data-stu-id="4df31-113">You need to be assigned permissions before you can perform this procedure or procedures.</span></span> <span data-ttu-id="4df31-114">Pour voir les autorisations qui vous sont nécessaires, consultez la rubrique «entrée anti-courrier indésirable dans la rubrique [autorisations des fonctionnalités dans Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4df31-114">To see what permissions you need, see the "Anti-spam entry in the [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) topic.</span></span>

<span data-ttu-id="4df31-115">La procédure suivante peut également être exécutée par le biais du service PowerShell à distance.</span><span class="sxs-lookup"><span data-stu-id="4df31-115">The following procedure can also be performed via remote PowerShell.</span></span> <span data-ttu-id="4df31-116">Utilisez la cmdlet Get-BlockedSenderAddress pour obtenir la liste des utilisateurs avec accès restreint et Remove-BlockedSenderAddress pour supprimer la restriction.</span><span class="sxs-lookup"><span data-stu-id="4df31-116">Use the Get-BlockedSenderAddress cmdlet to get the list of restricted users and Remove-BlockedSenderAddress to remove the restriction.</span></span> <span data-ttu-id="4df31-117">Pour apprendre à utiliser Windows PowerShell afin de vous connecter à Exchange Online, consultez la rubrique [Connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span><span class="sxs-lookup"><span data-stu-id="4df31-117">To learn how to use Windows PowerShell to connect to Exchange Online, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>

## <a name="remove-restrictions-for-a-blocked-office-365-email-account"></a><span data-ttu-id="4df31-118">Supprimer les restrictions pour un compte de messagerie Office 365 bloqué</span><span class="sxs-lookup"><span data-stu-id="4df31-118">Remove restrictions for a blocked Office 365 email account</span></span>

<span data-ttu-id="4df31-119">Vous effectuez cette tâche dans le centre de sécurité & Compliance Center (SCC).</span><span class="sxs-lookup"><span data-stu-id="4df31-119">You complete this task in the Security & Compliance Center (SCC).</span></span> <span data-ttu-id="4df31-120">Pour plus d’informations sur SCC, [accédez au centre de sécurité _AMP_ Compliance Center](go-to-the-securitycompliance-center.md) .</span><span class="sxs-lookup"><span data-stu-id="4df31-120">[Go to the Security & Compliance Center](go-to-the-securitycompliance-center.md) for more details about SCC.</span></span> <span data-ttu-id="4df31-121">Vous devez être dans le groupe de rôles gestion de l' **organisation** ou **administrateur de sécurité** pour effectuer ces fonctions.</span><span class="sxs-lookup"><span data-stu-id="4df31-121">You need to be in the **Organization Management** or the **Security Administrator** role group in order to perform these functions.</span></span> <span data-ttu-id="4df31-122">[Accédez à autorisations dans le centre de sécurité _AMP_ conformité](permissions-in-the-security-and-compliance-center.md) pour plus d’informations sur les groupes de rôles SCC.</span><span class="sxs-lookup"><span data-stu-id="4df31-122">[Go to Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md) for more details about SCC role groups.</span></span>

1. <span data-ttu-id="4df31-123">À l’aide d’un compte professionnel ou scolaire disposant de privilèges d’administrateur général Office 365, connectez-vous au centre de sécurité et conformité Office 365 et, dans la liste de gauche, développez **gestion des menaces**, choisissez **examiner**, puis choisissez **restreint. Les utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="4df31-123">Using a work or school account that has Office 365 global administrator privileges, sign into the Office 365 Security and Compliance Center and in the list on the left, expand **Threat Management**, choose **Review**, and then choose **Restricted Users**.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="4df31-124">Pour accéder directement à la page **utilisateurs restreints** (anciennement appelé centre de maintenance) dans le &amp; Centre de sécurité conformité, utilisez l’URL suivante: >[https://protection.office.com/#/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span><span class="sxs-lookup"><span data-stu-id="4df31-124">To go directly to the **Restricted Users** page (formerly known as the Action Center) in the Security &amp; Compliance Center, use this URL: > [https://protection.office.com/#/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span></span>

2. <span data-ttu-id="4df31-125">Cette page contient la liste des utilisateurs qui ont été bloqués pour l’envoi de messages à l’extérieur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="4df31-125">This page will contain the list of users that have been blocked from sending mail to outside of your organization.</span></span>  <span data-ttu-id="4df31-126">Recherchez l’utilisateur pour lequel vous souhaitez supprimer les restrictions, puis cliquez \*\*\*\* sur débloquer.</span><span class="sxs-lookup"><span data-stu-id="4df31-126">Find the user you wish to remove restrictions on and then click on **Unblock**.</span></span>

3. <span data-ttu-id="4df31-127">Un passage vers l’extérieur indiquera les détails du compte dont l’envoi est restreint.</span><span class="sxs-lookup"><span data-stu-id="4df31-127">A fly-out will go into the details about the account whose sending is restricted.</span></span> <span data-ttu-id="4df31-128">Vous devez passer en revue les recommandations pour vous assurer que vous prenez les mesures appropriées au cas où le compte est réellement compromis.</span><span class="sxs-lookup"><span data-stu-id="4df31-128">You should go through the recommendations to ensure you're taking the proper actions in case the account is actually compromised.</span></span> <span data-ttu-id="4df31-129">Cliquez sur **suivant** lorsque vous avez fini.</span><span class="sxs-lookup"><span data-stu-id="4df31-129">Click **Next** when done.</span></span>

4. <span data-ttu-id="4df31-130">L’écran suivant contient des recommandations pour vous aider à éviter toute compromission ultérieure.</span><span class="sxs-lookup"><span data-stu-id="4df31-130">The next screen has recommendations to help prevent future compromise.</span></span> <span data-ttu-id="4df31-131">L’activation de l’authentification multifacteur (MFA) et la modification des mots de passe constituent une excellente défense.</span><span class="sxs-lookup"><span data-stu-id="4df31-131">Enabling multi-factor authentication (MFA) and changing the passwords are a good defense.</span></span> <span data-ttu-id="4df31-132">Cliquez sur débloquer l' **utilisateur** lorsque vous avez fini.</span><span class="sxs-lookup"><span data-stu-id="4df31-132">Click **Unblock user** when done.</span></span>

5. <span data-ttu-id="4df31-133">Cliquez sur **Oui** pour confirmer la modification.</span><span class="sxs-lookup"><span data-stu-id="4df31-133">Click **Yes** to confirm the change.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4df31-134">La suppression des restrictions peut prendre jusqu’à 30 minutes.</span><span class="sxs-lookup"><span data-stu-id="4df31-134">It may take up to 30 minutes before restrictions are removed.</span></span> 

## <a name="making-sure-admins-are-alerted-when-this-happens"></a><span data-ttu-id="4df31-135">S’assurer que les administrateurs sont alertés lorsque cela se produit</span><span class="sxs-lookup"><span data-stu-id="4df31-135">Making sure admins are alerted when this happens</span></span>

<span data-ttu-id="4df31-136">Les administrateurs de client reçoivent également une alerte indiquant que l’utilisateur n’a pas été autorisé à envoyer des messages sortants supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="4df31-136">The tenant admins will also receive an alert stating that the user has been restricted from sending any more outbound messages.</span></span> <span data-ttu-id="4df31-137">Il s’agit d’une alerte par défaut fournie pour tous les clients et est indiquée dans la page stratégies d’alerte SCC, intitulée «utilisateur restreint de l’envoi de courrier électronique».</span><span class="sxs-lookup"><span data-stu-id="4df31-137">It is a default alert that is provided for all tenants and is listed in the SCC Alert policies page, titled "User restricted from sending email".</span></span> <span data-ttu-id="4df31-138">Pour plus d’informations sur l’alerte, accédez à [stratégies d’alerte dans le centre de sécurité _AMP_ Compliance Center](https://docs.microsoft.com/en-us/office365/securitycompliance/alert-policies) .</span><span class="sxs-lookup"><span data-stu-id="4df31-138">Go to [Alert policies in the Security & Compliance Center](https://docs.microsoft.com/en-us/office365/securitycompliance/alert-policies) for more information on the alert.</span></span>

## <a name="for-more-information"></a><span data-ttu-id="4df31-139">Pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="4df31-139">For more information</span></span>

[<span data-ttu-id="4df31-140">Réponse à un compte de messagerie compromis</span><span class="sxs-lookup"><span data-stu-id="4df31-140">Responding to a compromised email account</span></span>](responding-to-a-compromised-email-account.md)

[<span data-ttu-id="4df31-141">Présentation de l’alerte utilisateur restreinte de l’envoi de messages électroniques</span><span class="sxs-lookup"><span data-stu-id="4df31-141">Understanding the User restricted from sending email alert</span></span>](https://docs.microsoft.com/en-us/office365/securitycompliance/alert-policies)

[<span data-ttu-id="4df31-142">Pool de remise à risque élevé pour les messages sortants</span><span class="sxs-lookup"><span data-stu-id="4df31-142">High-risk delivery pool for outbound messages</span></span>](high-risk-delivery-pool-for-outbound-messages.md)

[<span data-ttu-id="4df31-143">Autorisations dans le centre de conformité et de sécurité</span><span class="sxs-lookup"><span data-stu-id="4df31-143">Permissions in the Security & Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
