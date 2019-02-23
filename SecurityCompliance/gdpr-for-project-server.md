---
title: RGPD pour Project Server
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
description: Découvrez comment satisfaire aux exigences du RGPD dans l’environnement Project Server local.
ms.openlocfilehash: 67097cdab4fdab31537cf4b6dd27ce17234c2bdc
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219014"
---
# <a name="gdpr-for-project-server"></a><span data-ttu-id="2928c-103">RGPD pour Project Server</span><span class="sxs-lookup"><span data-stu-id="2928c-103">GDPR for Project Server</span></span>

<span data-ttu-id="2928c-p101">Project Server utilise des scripts personnalisés pour exporter et supprimer des données utilisateur dans Project Web App. Le processus de base est le suivant :</span><span class="sxs-lookup"><span data-stu-id="2928c-p101">Project Server uses custom scripts to export and redact user data in Project Web App. The basic process is:</span></span>

1.  <span data-ttu-id="2928c-106">Recherchez les sites Project Web App dans votre batterie de serveurs.</span><span class="sxs-lookup"><span data-stu-id="2928c-106">Find the Project Web App sites in your farm.</span></span>

2.  <span data-ttu-id="2928c-107">Recherchez les projets dans chaque site contenant l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2928c-107">Find the projects in each site that contain the user.</span></span>

3.  <span data-ttu-id="2928c-108">Exportez et passez en revue les types de données que vous voulez examiner.</span><span class="sxs-lookup"><span data-stu-id="2928c-108">Export and review the types of data that you want to review.</span></span>

4.  <span data-ttu-id="2928c-109">Supprimez des données si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="2928c-109">Redact data as needed.</span></span>

<span data-ttu-id="2928c-110">Ces étapes sont expliquées en détail dans les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="2928c-110">These steps are covered in detail in the following articles:</span></span>

- [<span data-ttu-id="2928c-111">Exportation de données utilisateur depuis Project Server</span><span class="sxs-lookup"><span data-stu-id="2928c-111">Export user data from Project Server</span></span>](/Project/export-user-data-from-project-server?toc=/Office365/Enterprise/toc.json)

- [<span data-ttu-id="2928c-112">Suppression de données utilisateur de Project Server</span><span class="sxs-lookup"><span data-stu-id="2928c-112">Delete user data from Project Server</span></span>](/Project/delete-user-data-from-project-server?toc=/Office365/Enterprise/toc.json)


<span data-ttu-id="2928c-p102">Notez que Project Server est basé sur SharePoint Server et consigne les événements dans les journaux ULS de SharePoint et dans la base de données d’utilisation. Pour en savoir plus, consultez l’article qui traite du [RGPD dans SharePoint Server](gdpr-for-sharepoint-server.md).</span><span class="sxs-lookup"><span data-stu-id="2928c-p102">Note that Project Server is built on top of SharePoint Server and logs events to the SharePoint ULS logs and Usage database. See [GDPR for SharePoint Server](gdpr-for-sharepoint-server.md) for more information.</span></span>
