---
title: Sites d’équipe SharePoint Online isolés
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/15/2017
audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.custom:
- Ent_Solutions
ms.assetid: 71250a04-fd2d-4c3c-a32b-b8a838b19a54
description: "Résumé : Découvrez les utilisations pour les sites d'équipe SharePoint Online isolés."
ms.openlocfilehash: 07f4d84493cdc7c0e153186164824fe8aa1e36bc
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34150066"
---
# <a name="isolated-sharepoint-online-team-sites"></a><span data-ttu-id="c155d-103">Sites d’équipe SharePoint Online isolés</span><span class="sxs-lookup"><span data-stu-id="c155d-103">Isolated SharePoint Online team sites</span></span>

 <span data-ttu-id="c155d-104">**Résumé :** Découvrez les utilisations pour les sites d'équipe SharePoint Online isolés.</span><span class="sxs-lookup"><span data-stu-id="c155d-104">**Summary:** Learn about the uses for isolated SharePoint Online team sites.</span></span>
  
<span data-ttu-id="c155d-p101">Les sites d'équipe SharePoint Online vous permettent de créer facilement et rapidement un espace dédié à la collaboration et au partage des notes, des documents, des articles, du calendrier et d'autres ressources dans Microsoft Office 365. Les sites d'équipe SharePoint Online sont créés à partir d'un groupe Office 365. Ils comportent un modèle d'administration simplifié pour favoriser une collaboration ouverte entre les membres d'un groupe privé ou de l'organisation tout entière. Un site d'équipe SharePoint Online par défaut permet aux membres du groupe Office 365 d'inviter d'autres utilisateurs et de contrôler les paramètres d'autorisations.</span><span class="sxs-lookup"><span data-stu-id="c155d-p101">SharePoint Online team sites are an easy way to quickly create a space for collaboration of notes, documents, articles, a calendar, and other resources in Microsoft Office 365. SharePoint Online team sites are based on an Office 365 group and have a simplified administration model to allow open collaboration with a private set of group members or the entire organization. A default SharePoint Online team site allows members of the Office 365 group to invite other users and control permissions settings.</span></span>
  
<span data-ttu-id="c155d-p102">Toutefois, dans certains cas, vous souhaitez créer un site d'équipe SharePoint Online pour une collaboration où les autorisations de ce site sont plus étroitement contrôlées via l'appartenance au groupe et les niveaux d'autorisation SharePoint Online, qui sont gérés uniquement par les administrateurs SharePoint. C'est ce que nous appelons un site isolé, car il est réservé aux utilisateurs qui collaborent sur le site, consultent son contenu ou gèrent le site. Vous aurez besoin d'un site isolé pour :</span><span class="sxs-lookup"><span data-stu-id="c155d-p102">However, in some cases, you want to create a SharePoint Online team site for collaboration where the permissions of that site are more tightly controlled through group membership and SharePoint Online permission levels, which are only managed by SharePoint administrators. We call this an isolated site, which is isolated to the set of users that are either collaborating, viewing its contents, or administering the site. You might need an isolated site for the following:</span></span>
  
- <span data-ttu-id="c155d-111">travailler sur un projet secret au sein de votre organisation ;</span><span class="sxs-lookup"><span data-stu-id="c155d-111">A secret project within your organization.</span></span>
    
- <span data-ttu-id="c155d-112">stocker des éléments de propriété intellectuelle précieux ou très sensibles pour votre organisation ;</span><span class="sxs-lookup"><span data-stu-id="c155d-112">The location for highly-sensitive or valuable intellectual property for your organization.</span></span>
    
- <span data-ttu-id="c155d-113">conserver les ressources destinées à une procédure judiciaire engagée par votre organisation ou à laquelle elle est soumise ;</span><span class="sxs-lookup"><span data-stu-id="c155d-113">The resources for a legal action taken by your organization or that to which it is being subjected.</span></span>
    
- <span data-ttu-id="c155d-114">partager un abonnement Office 365 avec d’autres organisations dont certaines activités se recoupent, mais qui, pour la plupart, existent en tant qu’entités distinctes.</span><span class="sxs-lookup"><span data-stu-id="c155d-114">To share an Office 365 subscription between multiple organizations that have some overlap, but for the most part exist as separate business entities.</span></span>
    
<span data-ttu-id="c155d-115">Voici les exigences d’un site isolé :</span><span class="sxs-lookup"><span data-stu-id="c155d-115">Here are the requirements of an isolated site:</span></span>
  
- <span data-ttu-id="c155d-116">Seuls les administrateurs SharePoint Online peuvent gérer le site, en particulier l’accès au site par les membres du groupe et la configuration des autorisations personnalisées.</span><span class="sxs-lookup"><span data-stu-id="c155d-116">Only SharePoint Online administrators can perform site administration, which includes group membership for access to the site and configuring custom permissions.</span></span>
    
- <span data-ttu-id="c155d-117">Les membres du site ne peuvent pas inviter d’autres membres à accéder au site d’équipe.</span><span class="sxs-lookup"><span data-stu-id="c155d-117">Members of the site cannot invite other members to the team site.</span></span>
    
- <span data-ttu-id="c155d-p103">Les utilisateurs qui ne sont pas membres du site isolé ne peuvent pas demander l'accès au site. Lorsqu'ils essaieront d'accéder à une URL associée au site, ils seront redirigés vers une page web leur indiquant que l'accès a été refusé.</span><span class="sxs-lookup"><span data-stu-id="c155d-p103">Users who are not members of the isolated site cannot request access to the site. They will receive an access denied web page when they attempt to access any URL associated with the site.</span></span>
    
<span data-ttu-id="c155d-p104">Grâce à une gestion centralisée des accès et aux autorisations personnalisées, le site reste isolé en tout temps. Par exemple, les membres du groupe ne peuvent pas, volontairement ou accidentellement, configurer des autorisations personnalisées pour d'autres utilisateurs de l'abonnement Office 365 qui ne devraient pas être membres du site ou les inviter.</span><span class="sxs-lookup"><span data-stu-id="c155d-p104">The tradeoff of requiring centralized access control and custom permissions by SharePoint Online administrators is that the site remains isolated over time. For example, current members cannot, either intentionally or accidentally, invite or configure custom permissions for other users within the Office 365 subscription who should not be members of the site.</span></span>
  
<span data-ttu-id="c155d-122">Un site isolé peut être utilisé avec d’autres fonctionnalités, telles que :</span><span class="sxs-lookup"><span data-stu-id="c155d-122">An isolated site can be used with other features, such as:</span></span>
  
- <span data-ttu-id="c155d-123">la gestion des droits relatifs à l’information pour garantir que les ressources du site restent chiffrées même si elles sont téléchargées localement et chargées sur un autre site accessible à toute l’entreprise ;</span><span class="sxs-lookup"><span data-stu-id="c155d-123">Information Rights Management to ensure that the resources on the site remain encrypted, even if they are downloaded locally and uploaded to another site that is available to the entire organization.</span></span>
    
- <span data-ttu-id="c155d-124">la protection contre la perte de données pour empêcher les utilisateurs d’envoyer par e-mail les ressources du site, comme des fichiers.</span><span class="sxs-lookup"><span data-stu-id="c155d-124">Data loss prevention to prevent users from sending the resources of the site, such as files, in email.</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="c155d-125">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="c155d-125">Next steps</span></span>

<span data-ttu-id="c155d-126">Pour tester un site d'équipe SharePoint Online isolé faisant partie d'un abonnement à la version d'évaluation, consultez la rubrique [Site d'équipe SharePoint Online isolé dans votre environnement de développement/test d'Office 365](isolated-sharepoint-online-team-site-dev-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="c155d-126">To try out an isolated SharePoint Online team site in a trial subscription, see the step-by-step instructions in [Isolated SharePoint Online team site dev/test environment](isolated-sharepoint-online-team-site-dev-test-environment.md).</span></span>
  
<span data-ttu-id="c155d-127">Lorsque vous souhaitez déployer un site d'équipe SharePoint Online isolé en production, lisez la procédure détaillée dans la rubrique [Conception d'un site d'équipe SharePoint Online isolé](design-an-isolated-sharepoint-online-team-site.md).</span><span class="sxs-lookup"><span data-stu-id="c155d-127">When you are ready to deploy an isolated SharePoint Online team site in production, see the step-by-step design considerations in [Design an isolated SharePoint Online team site](design-an-isolated-sharepoint-online-team-site.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c155d-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c155d-128">See Also</span></span>

[<span data-ttu-id="c155d-129">Conception d'un site d'équipe SharePoint Online isolé</span><span class="sxs-lookup"><span data-stu-id="c155d-129">Design an isolated SharePoint Online team site</span></span>](design-an-isolated-sharepoint-online-team-site.md)
  
[<span data-ttu-id="c155d-130">Gestion d’un site d’équipe SharePoint Online isolé</span><span class="sxs-lookup"><span data-stu-id="c155d-130">Manage an isolated SharePoint Online team site</span></span>](manage-an-isolated-sharepoint-online-team-site.md)

[<span data-ttu-id="c155d-131">Déploiement d’un site d’équipe SharePoint Online isolé</span><span class="sxs-lookup"><span data-stu-id="c155d-131">Deploy an isolated SharePoint Online team site</span></span>](deploy-an-isolated-sharepoint-online-team-site.md)


