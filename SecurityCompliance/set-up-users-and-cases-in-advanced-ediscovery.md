---
title: Configurer des utilisateurs et des cas dans Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 60ffd80b-4376-419d-b6e4-a72029b9907c
description: "Découvrez comment configurer des rôles d'utilisateur, créer des cas et affecter des utilisateurs à des cas dans Office 365 Advanced eDiscovery.  "
ms.openlocfilehash: 5a22e0683e49ebdaf8391e092aeb101386e0636b
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32260702"
---
# <a name="set-up-users-and-cases-in-office-365-advanced-ediscovery"></a><span data-ttu-id="9ba32-103">Configurer des utilisateurs et des cas dans Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="9ba32-103">Set up users and cases in Office 365 Advanced eDiscovery</span></span>

<span data-ttu-id="9ba32-104">Cette rubrique décrit comment configurer des utilisateurs et des cas pour Office 365 Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="9ba32-104">This topic describes how to set up users and cases for Office 365 Advanced eDiscovery.</span></span>
  
> [!NOTE]
> <span data-ttu-id="9ba32-p101">Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous [inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="9ba32-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
## <a name="prerequisites"></a><span data-ttu-id="9ba32-107">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="9ba32-107">Prerequisites</span></span>

<span data-ttu-id="9ba32-108">Avant de configurer des cas et des utilisateurs dans Advanced eDiscovery, les éléments suivants sont requis:</span><span class="sxs-lookup"><span data-stu-id="9ba32-108">Before setting up cases and users in Advanced eDiscovery, the following is required:</span></span>
  
- <span data-ttu-id="9ba32-109">Pour analyser les données d'un utilisateur à l'aide de Advanced eDiscovery, l'utilisateur (le dépositaire des données) doit disposer d'une licence Office 365 E5.</span><span class="sxs-lookup"><span data-stu-id="9ba32-109">To analyze a user's data using Advanced eDiscovery, the user (the custodian of the data) must be assigned an Office 365 E5 license.</span></span> <span data-ttu-id="9ba32-110">Par ailleurs, les utilisateurs disposant d'une licence Office 365 E1 ou E3 peuvent se voir attribuer une licence avancée eDiscovery autonome.</span><span class="sxs-lookup"><span data-stu-id="9ba32-110">Alternatively, users with an Office 365 E1 or E3 license can be assigned an Advanced eDiscovery standalone license.</span></span> <span data-ttu-id="9ba32-111">Les administrateurs et les responsables de la mise en conformité qui sont affectés à des cas et utilisent Advanced eDiscovery pour analyser les données n'ont pas besoin d'une licence E5.</span><span class="sxs-lookup"><span data-stu-id="9ba32-111">Administrators and compliance officers who are assigned to cases and use Advanced eDiscovery to analyze data don't need an E5 license.</span></span> 
    
- <span data-ttu-id="9ba32-112">Vous devez être membre du groupe de rôles gestionnaire de découverte électronique dans le centre de sécurité &amp; conformité Office 365 pour créer un cas eDiscovery et y ajouter des membres.</span><span class="sxs-lookup"><span data-stu-id="9ba32-112">You have to be a member of the eDiscovery Manager role group in the Office 365 Security &amp; Compliance Center to create an eDiscovery case and add members to it.</span></span> <span data-ttu-id="9ba32-113">Pour vous ajouter au groupe de rôles gestionnaire de découverte électronique &amp; dans le centre de sécurité conformité, vous devez être un administrateur général dans votre organisation Office 365.</span><span class="sxs-lookup"><span data-stu-id="9ba32-113">To add yourself to the eDiscovery Manager role group in Security &amp; Compliance Center, you have to be a global administrator in your Office 365 organization.</span></span> <span data-ttu-id="9ba32-114">Si vous n'êtes pas un administrateur général, vous devrez demander à un administrateur général de vous ajouter au groupe de rôles gestionnaire de découverte électronique.</span><span class="sxs-lookup"><span data-stu-id="9ba32-114">If you're not a global administrator, you 'll have to ask a global administrator to add you to the eDiscovery Manager role group.</span></span> <span data-ttu-id="9ba32-115">Pour plus d'informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="9ba32-115">For more information, see:</span></span>
    
  - [<span data-ttu-id="9ba32-116">Autorisations dans le centre de sécurité &amp; conformité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="9ba32-116">Permissions in the Microsoft 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
    
  - [<span data-ttu-id="9ba32-117">Attribuer des autorisations eDiscovery dans le centre de &amp; sécurité conformité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="9ba32-117">Assign eDiscovery permissions in the Microsoft‍ 365 Security &amp; Compliance Center</span></span>](assign-ediscovery-permissions.md)
    
## <a name="step-1-assign-users-ediscovery-permissions"></a><span data-ttu-id="9ba32-118">Étape 1: attribuer des autorisations eDiscovery aux utilisateurs</span><span class="sxs-lookup"><span data-stu-id="9ba32-118">Step 1: Assign users eDiscovery permissions</span></span>

<span data-ttu-id="9ba32-119">La première étape consiste à attribuer aux utilisateurs les autorisations requises dans le &amp; Centre de sécurité conformité afin qu'ils puissent m'ajouter en tant que membre d'un cas eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="9ba32-119">The first step is to assign users the requirement permissions in the Security &amp; Compliance Center so that they can me added as a member of an eDiscovery case.</span></span> <span data-ttu-id="9ba32-120">Une fois qu'un utilisateur est ajouté en tant que membre d'un cas &amp; dans le centre de sécurité conformité, il pourra accéder à l'incident dans Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="9ba32-120">After a user is added as a member of a case in the Security &amp; Compliance Center, they'll be able to access the case in Advanced eDiscovery.</span></span>
  
<span data-ttu-id="9ba32-121">Pour attribuer aux utilisateurs les autorisations nécessaires afin qu'ils puissent être ajoutés en tant que membre d'un cas de découverte électronique, voir l'étape 1 dans [les cas &amp; eDiscovery dans le centre de sécurité conformité de Microsoft 365](ediscovery-cases.md#step-1-assign-ediscovery-permissions-to-potential-case-members).</span><span class="sxs-lookup"><span data-stu-id="9ba32-121">To assign a user the necessary permissions so they can be added as a member of an eDiscovery case, see Step 1 in [eDiscovery cases in the Microsoft 365 Security &amp; Compliance Center](ediscovery-cases.md#step-1-assign-ediscovery-permissions-to-potential-case-members).</span></span>
  
## <a name="step-2-create-an-ediscovery-case-and-add-members"></a><span data-ttu-id="9ba32-122">Étape 2: créer un cas eDiscovery et ajouter des membres</span><span class="sxs-lookup"><span data-stu-id="9ba32-122">Step 2: Create an eDiscovery case and add members</span></span>

<span data-ttu-id="9ba32-123">L'étape suivante consiste à créer un nouveau cas eDiscovery dans le centre &amp; de sécurité et à ajouter des membres.</span><span class="sxs-lookup"><span data-stu-id="9ba32-123">The next step is to create a new eDiscovery case in the Security &amp; Compliance Center and add members.</span></span> <span data-ttu-id="9ba32-124">Les membres de ce cas seront alors en mesure d'accéder au cas dans Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="9ba32-124">Members of the case will then be able to access the case in Advanced eDiscovery.</span></span>
  
1. <span data-ttu-id="9ba32-125">Pour créer un cas de découverte électronique, voir l'étape 2 dans [cas de découverte électronique dans &amp; le centre de sécurité conformité Microsoft 365](ediscovery-cases.md#step-2-create-a-new-case).</span><span class="sxs-lookup"><span data-stu-id="9ba32-125">To create a new eDiscovery case, see Step 2 in [eDiscovery cases in the Microsoft 365 Security &amp; Compliance Center](ediscovery-cases.md#step-2-create-a-new-case).</span></span>
    
2. <span data-ttu-id="9ba32-126">Pour ajouter des membres à un cas eDiscovery, reportez-vous à l'étape 3 dans [cas de découverte électronique dans le centre de sécurité &amp; conformité Microsoft 365](ediscovery-cases.md#step-3-add-members-to-a-case)</span><span class="sxs-lookup"><span data-stu-id="9ba32-126">To add members to an eDiscovery case, see Step 3 in [eDiscovery cases in the Microsoft 365 Security &amp; Compliance Center](ediscovery-cases.md#step-3-add-members-to-a-case)</span></span>
    
## <a name="step-3-go-a-case-in-advanced-ediscovery"></a><span data-ttu-id="9ba32-127">Étape 3: passer un cas dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="9ba32-127">Step 3: Go a case in Advanced eDiscovery</span></span>

<span data-ttu-id="9ba32-128">Une fois que vous avez créé un cas eDiscovery et ajouté des membres, vous (ou tout membre du cas) pouvez accéder à la casse correspondante dans Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="9ba32-128">After you create an eDiscovery case and add members, you (or any member of the case) can access the corresponding case in Advanced eDiscovery.</span></span> <span data-ttu-id="9ba32-129">Pour accéder à un cas dans Advanced eDiscovery, reportez-vous à l'étape 8 dans [les cas de découverte électronique dans le centre de sécurité &amp; conformité Microsoft 365](ediscovery-cases.md#step-8-go-to-the-case-in-advanced-ediscovery).</span><span class="sxs-lookup"><span data-stu-id="9ba32-129">To access a case in Advanced eDiscovery, see Step 8 in [eDiscovery cases in the Microsoft 365 Security &amp; Compliance Center](ediscovery-cases.md#step-8-go-to-the-case-in-advanced-ediscovery).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9ba32-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ba32-130">See also</span></span>

[<span data-ttu-id="9ba32-131">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="9ba32-131">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="9ba32-132">Préparation des données</span><span class="sxs-lookup"><span data-stu-id="9ba32-132">Preparing data</span></span>](prepare-data-for-advanced-ediscovery.md)
 