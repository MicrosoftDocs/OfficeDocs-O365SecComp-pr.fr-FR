---
title: Office 365 traitant de l’endommagement des données
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Une explication de la corruption des données dans Office 365, ainsi que les efforts de prévention et de récupération de Microsoft.
ms.openlocfilehash: 4997ec0efb60d4e62e3a385af8bbd1a610c5290a
ms.sourcegitcommit: f0d23e57b00f07cef5b1b2d366eaeeeacda37e3e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/18/2019
ms.locfileid: "35786699"
---
# <a name="dealing-with-data-corruption-in-office-365"></a><span data-ttu-id="074ba-103">Gestion de l’altération des données dans Office 365</span><span class="sxs-lookup"><span data-stu-id="074ba-103">Dealing with Data Corruption in Office 365</span></span>

<span data-ttu-id="074ba-104">L’un des aspects les plus délicats de l’exécution d’un service Cloud de grande envergure est la façon de gérer l’altération des données, compte tenu du volume important de données et des systèmes indépendants.</span><span class="sxs-lookup"><span data-stu-id="074ba-104">One of the challenging aspects of running a large-scale cloud service is how to handle data corruption, given the large volume of data and independent systems.</span></span> <span data-ttu-id="074ba-105">La corruption des données peut être causée par:</span><span class="sxs-lookup"><span data-stu-id="074ba-105">Data corruption can be caused by:</span></span>

- <span data-ttu-id="074ba-106">Bogues d’application ou d’infrastructure, en corrompant tout ou partie de l’état de l’application</span><span class="sxs-lookup"><span data-stu-id="074ba-106">Application or infrastructure bugs, corrupting some or all of the application state</span></span>
- <span data-ttu-id="074ba-107">Problèmes matériels entraînant la perte de données ou l’impossibilité de lire des données</span><span class="sxs-lookup"><span data-stu-id="074ba-107">Hardware issues that result in lost data or an inability to read data</span></span>
- <span data-ttu-id="074ba-108">Erreurs opérationnelles humaines</span><span class="sxs-lookup"><span data-stu-id="074ba-108">Human operational errors</span></span>
- <span data-ttu-id="074ba-109">Pirates malveillants et employés mécontents</span><span class="sxs-lookup"><span data-stu-id="074ba-109">Malicious hackers and disgruntled employees</span></span>
- <span data-ttu-id="074ba-110">Incidents dans les services externes entraînant une perte de données</span><span class="sxs-lookup"><span data-stu-id="074ba-110">Incidents in external services that result in some loss of data</span></span>

<span data-ttu-id="074ba-111">Étant donné que la résilience accrue de l’intégrité des données signifie moins d’incidents d’endommagement des données, Microsoft a intégré les mécanismes de protection d’Office 365 pour empêcher la corruption, ainsi que les systèmes et les processus qui nous permettent de récupérer les données le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="074ba-111">Because greater resiliency in data integrity means fewer data corruption incidents, Microsoft has built into Office 365 protection mechanisms to prevent corruption from happening, as well as systems and processes that enable us to recover data if it does.</span></span> <span data-ttu-id="074ba-112">Il existe des vérifications et des processus dans les différentes étapes du processus de publication d’ingénierie afin de renforcer la résistance contre l’altération des données, notamment:</span><span class="sxs-lookup"><span data-stu-id="074ba-112">Checks and processes exist within the various stages of the engineering release process to increase resiliency against data corruption, including:</span></span>

- <span data-ttu-id="074ba-113">Conception du système</span><span class="sxs-lookup"><span data-stu-id="074ba-113">System Design</span></span>
- <span data-ttu-id="074ba-114">Structure et organisation du code</span><span class="sxs-lookup"><span data-stu-id="074ba-114">Code organization and structure</span></span>
- <span data-ttu-id="074ba-115">Révision du code</span><span class="sxs-lookup"><span data-stu-id="074ba-115">Code review</span></span>
- <span data-ttu-id="074ba-116">Tests d’unité, tests d’intégration et tests système</span><span class="sxs-lookup"><span data-stu-id="074ba-116">Unit tests, integration tests, and system tests</span></span>
- <span data-ttu-id="074ba-117">Tests/portails de fils de voyage</span><span class="sxs-lookup"><span data-stu-id="074ba-117">Trip wires tests/gates</span></span>

<span data-ttu-id="074ba-118">Dans les environnements de production Office 365, la réplication d’homologue entre centres de données garantit qu’il y a toujours plusieurs copies dynamiques de toutes les données.</span><span class="sxs-lookup"><span data-stu-id="074ba-118">Within Office 365 production environments, peer replication between datacenters ensures that there are always multiple live copies of any data.</span></span> <span data-ttu-id="074ba-119">Les images et les scripts standard permettent de récupérer les serveurs perdus, et les données répliquées sont utilisées pour restaurer les données client.</span><span class="sxs-lookup"><span data-stu-id="074ba-119">Standard images and scripts are used to recover lost servers, and replicated data is used to restore customer data.</span></span> <span data-ttu-id="074ba-120">En raison des contrôles et des processus de résilience des données intégrés, Microsoft conserve uniquement les sauvegardes de la documentation du système d’informations Office 365 (y compris la documentation liée à la sécurité), à l’aide de la réplication intégrée dans SharePoint Online et de notre code interne outil référentiel, dépôt source.</span><span class="sxs-lookup"><span data-stu-id="074ba-120">Because of the built-in data resiliency checks and processes, Microsoft maintains backups only of Office 365 information system documentation (including security-related documentation), using built-in replication in SharePoint Online and our internal code repository tool, Source Depot.</span></span> <span data-ttu-id="074ba-121">La documentation système est stockée dans SharePoint Online, et Source Depot contient des images système et d’application.</span><span class="sxs-lookup"><span data-stu-id="074ba-121">System documentation is stored in SharePoint Online, and Source Depot contains system and application images.</span></span> <span data-ttu-id="074ba-122">SharePoint Online et le SAV source utilisent tous deux le contrôle de version et sont répliqués en quasi-temps réel.</span><span class="sxs-lookup"><span data-stu-id="074ba-122">Both SharePoint Online and Source Depot use versioning and are replicated in near real time.</span></span>
