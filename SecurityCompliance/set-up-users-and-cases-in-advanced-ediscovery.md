---
title: Configurer les utilisateurs et les cas dans Office 365 avancée de découverte électronique
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 60ffd80b-4376-419d-b6e4-a72029b9907c
description: 'Découvrez comment configurer les rôles d’utilisateur, de créer des cas et affecter des utilisateurs au cas dans Office 365 avancée de découverte électronique.  '
ms.openlocfilehash: 49f76b415d86035cecafc19c23b36c413f7576e5
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528359"
---
# <a name="set-up-users-and-cases-in-office-365-advanced-ediscovery"></a><span data-ttu-id="dfe96-103">Configurer les utilisateurs et les cas dans Office 365 avancée de découverte électronique</span><span class="sxs-lookup"><span data-stu-id="dfe96-103">Set up users and cases in Office 365 Advanced eDiscovery</span></span>

<span data-ttu-id="dfe96-104">Cette rubrique décrit comment configurer les utilisateurs et les cas eDiscovery Office 365 avancés.</span><span class="sxs-lookup"><span data-stu-id="dfe96-104">This topic describes how to set up users and cases for Office 365 Advanced eDiscovery.</span></span>
  
> [!NOTE]
> <span data-ttu-id="dfe96-p101">Découverte avancée nécessite un Office 365 E3 avec le module complémentaire de conformité avancée ou un abonnement E5 pour votre organisation. Si vous n’avez qu’un plan d’et essayer eDiscovery avancé, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="dfe96-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
## <a name="prerequisites"></a><span data-ttu-id="dfe96-107">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="dfe96-107">Prerequisites</span></span>

<span data-ttu-id="dfe96-108">Avant de configurer les cas et les utilisateurs avancé eDiscovery, les éléments suivants est requis :</span><span class="sxs-lookup"><span data-stu-id="dfe96-108">Before setting up cases and users in Advanced eDiscovery, the following is required:</span></span>
  
- <span data-ttu-id="dfe96-p102">Pour analyser les données d’un utilisateur à l’aide de la découverte électronique avancée, l’utilisateur (le dépositaire des données) doit être affecté à une licence Office 365 E5. Autrement, les utilisateurs possédant une licence Office 365 E1 ou E3 peuvent être affectés à une licence autonome de découverte avancée. Les administrateurs et des agents de conformité qui sont affectées à des cas et utilisent eDiscovery avancée pour analyser des données inutile d’une licence E5.</span><span class="sxs-lookup"><span data-stu-id="dfe96-p102">To analyze a user's data using Advanced eDiscovery, the user (the custodian of the data) must be assigned an Office 365 E5 license. Alternatively, users with an Office 365 E1 or E3 license can be assigned an Advanced eDiscovery standalone license. Administrators and compliance officers who are assigned to cases and use Advanced eDiscovery to analyze data don't need an E5 license.</span></span> 
    
- <span data-ttu-id="dfe96-p103">Vous devez être membre du groupe de rôles eDiscovery Gestionnaire de sécurité Office 365 &amp; centre de conformité pour créer un cas eDiscovery et ajouter des membres. Ajouter au groupe de rôles de gestionnaire de découverte de la sécurité &amp; centre de conformité, vous devez être un administrateur global dans votre organisation Office 365. Si vous n’êtes pas un administrateur global, vous devrez demander à un administrateur global pour vous ajouter au groupe de rôles gestionnaire eDiscovery. Pour plus d’informations, voir :</span><span class="sxs-lookup"><span data-stu-id="dfe96-p103">You have to be a member of the eDiscovery Manager role group in the Office 365 Security &amp; Compliance Center to create an eDiscovery case and add members to it. To add yourself to the eDiscovery Manager role group in Security &amp; Compliance Center, you have to be a global administrator in your Office 365 organization. If you're not a global administrator, you 'll have to ask a global administrator to add you to the eDiscovery Manager role group. For more information, see:</span></span>
    
  - [<span data-ttu-id="dfe96-116">Autorisations de sécurité Office 365 &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="dfe96-116">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
    
  - [<span data-ttu-id="dfe96-117">Attribuer des autorisations de sécurité Office 365 eDiscovery &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="dfe96-117">Assign eDiscovery permissions in the Office‍ 365 Security &amp; Compliance Center</span></span>](assign-ediscovery-permissions.md)
    
## <a name="step-1-assign-users-ediscovery-permissions"></a><span data-ttu-id="dfe96-118">Étape 1 : Attribuer aux utilisateurs les autorisations de découverte électronique</span><span class="sxs-lookup"><span data-stu-id="dfe96-118">Step 1: Assign users eDiscovery permissions</span></span>

<span data-ttu-id="dfe96-p104">La première étape consiste à attribuer aux utilisateurs les autorisations exigence de sécurité &amp; sorte qu’ils puissent m’ajouté en tant que membre d’un cas de découverte électronique du centre de conformité. Après l’ajout d’un utilisateur en tant que membre d’un cas de la sécurité &amp; centre de conformité, ils pourront accéder à la casse d’eDiscovery avancée.</span><span class="sxs-lookup"><span data-stu-id="dfe96-p104">The first step is to assign users the requirement permissions in the Security &amp; Compliance Center so that they can me added as a member of an eDiscovery case. After a user is added as a member of a case in the Security &amp; Compliance Center, they'll be able to access the case in Advanced eDiscovery.</span></span>
  
<span data-ttu-id="dfe96-121">Pour affecter un utilisateur les autorisations nécessaires pour pouvoir être ajoutés en tant que membre d’un cas eDiscovery, voir l’étape 1 dans [cas eDiscovery de sécurité Office 365 &amp; centre de conformité](ediscovery-cases.md#step-1-assign-ediscovery-permissions-to-potential-case-members).</span><span class="sxs-lookup"><span data-stu-id="dfe96-121">To assign a user the necessary permissions so they can be added as a member of an eDiscovery case, see Step 1 in [eDiscovery cases in the Office 365 Security &amp; Compliance Center](ediscovery-cases.md#step-1-assign-ediscovery-permissions-to-potential-case-members).</span></span>
  
## <a name="step-2-create-an-ediscovery-case-and-add-members"></a><span data-ttu-id="dfe96-122">Étape 2 : Créer un cas eDiscovery et ajouter des membres</span><span class="sxs-lookup"><span data-stu-id="dfe96-122">Step 2: Create an eDiscovery case and add members</span></span>

<span data-ttu-id="dfe96-p105">L’étape suivante consiste à créer un nouveau cas eDiscovery dans la sécurité &amp; centre de conformité et ajouter des membres. Membres de l’incident seront en mesure d’accéder à la casse d’eDiscovery avancée.</span><span class="sxs-lookup"><span data-stu-id="dfe96-p105">The next step is to create a new eDiscovery case in the Security &amp; Compliance Center and add members. Members of the case will then be able to access the case in Advanced eDiscovery.</span></span>
  
1. <span data-ttu-id="dfe96-125">Pour créer un nouveau cas eDiscovery, voir l’étape 2 de [cas eDiscovery de sécurité Office 365 &amp; centre de conformité](ediscovery-cases.md#step-2-create-a-new-case).</span><span class="sxs-lookup"><span data-stu-id="dfe96-125">To create a new eDiscovery case, see Step 2 in [eDiscovery cases in the Office 365 Security &amp; Compliance Center](ediscovery-cases.md#step-2-create-a-new-case).</span></span>
    
2. <span data-ttu-id="dfe96-126">Pour ajouter des membres à une affaire eDiscovery, consultez l’étape 3 dans [cas eDiscovery de sécurité Office 365 &amp; centre de conformité](ediscovery-cases.md#step-3-add-members-to-a-case)</span><span class="sxs-lookup"><span data-stu-id="dfe96-126">To add members to an eDiscovery case, see Step 3 in [eDiscovery cases in the Office 365 Security &amp; Compliance Center](ediscovery-cases.md#step-3-add-members-to-a-case)</span></span>
    
## <a name="step-3-go-a-case-in-advanced-ediscovery"></a><span data-ttu-id="dfe96-127">Étape 3 : Accéder à un cas de découverte électronique avancée</span><span class="sxs-lookup"><span data-stu-id="dfe96-127">Step 3: Go a case in Advanced eDiscovery</span></span>

<span data-ttu-id="dfe96-p106">Une fois que vous créez un cas eDiscovery et ajoutez des membres, vous (ou un membre de la casse) peut accéder à la casse correspondante d’eDiscovery avancée. Pour accéder à un cas de découverte électronique avancée, voir l’étape 8 dans [cas eDiscovery de sécurité Office 365 &amp; centre de conformité](ediscovery-cases.md#step-8-go-to-the-case-in-advanced-ediscovery).</span><span class="sxs-lookup"><span data-stu-id="dfe96-p106">After you create an eDiscovery case and add members, you (or any member of the case) can access the corresponding case in Advanced eDiscovery. To access a case in Advanced eDiscovery, see Step 8 in [eDiscovery cases in the Office 365 Security &amp; Compliance Center](ediscovery-cases.md#step-8-go-to-the-case-in-advanced-ediscovery).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="dfe96-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dfe96-130">See also</span></span>

[<span data-ttu-id="dfe96-131">eDiscovery avancée Office 365</span><span class="sxs-lookup"><span data-stu-id="dfe96-131">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="dfe96-132">Préparation des données</span><span class="sxs-lookup"><span data-stu-id="dfe96-132">Preparing data</span></span>](prepare-data-for-advanced-ediscovery.md)
  
[<span data-ttu-id="dfe96-133">Accès et rôles d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="dfe96-133">User roles and access</span></span>](user-roles-and-access-in-advanced-ediscovery.md)

