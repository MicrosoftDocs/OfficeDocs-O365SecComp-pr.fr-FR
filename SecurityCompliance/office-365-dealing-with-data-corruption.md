---
title: Office 365 traitant de l'enDommagement des données
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Une explication de la corruption des données dans Office 365, ainsi que les efforts de prévention et de récupération de Microsoft.
ms.openlocfilehash: d33cb298c432db45d560e4c2876d9ac34ab9d6f4
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216544"
---
# <a name="dealing-with-data-corruption-in-office-365"></a><span data-ttu-id="66e75-103">Gestion de l'altération des données dans Office 365</span><span class="sxs-lookup"><span data-stu-id="66e75-103">Dealing with Data Corruption in Office 365</span></span>

<span data-ttu-id="66e75-p101">L'un des aspects les plus délicats de l'exécution d'un service Cloud de grande envergure est la façon de gérer l'altération des données, compte tenu du volume important de données et des systèmes indépendants. La corruption des données peut être causée par:</span><span class="sxs-lookup"><span data-stu-id="66e75-p101">One of the challenging aspects of running a large-scale cloud service is how to handle data corruption, given the large volume of data and independent systems. Data corruption can be caused by:</span></span>
- <span data-ttu-id="66e75-106">Bogues d'application ou d'infrastructure, en corrompant tout ou partie de l'état de l'application</span><span class="sxs-lookup"><span data-stu-id="66e75-106">Application or infrastructure bugs, corrupting some or all of the application state</span></span> 
- <span data-ttu-id="66e75-107">Problèmes matériels entraînant la perte de données ou l'impossibilité de lire des données</span><span class="sxs-lookup"><span data-stu-id="66e75-107">Hardware issues that result in lost data or an inability to read data</span></span> 
- <span data-ttu-id="66e75-108">Erreurs opérationnelles humaines</span><span class="sxs-lookup"><span data-stu-id="66e75-108">Human operational errors</span></span> 
- <span data-ttu-id="66e75-109">Pirates malveillants et employés mécontents</span><span class="sxs-lookup"><span data-stu-id="66e75-109">Malicious hackers and disgruntled employees</span></span> 
- <span data-ttu-id="66e75-110">Incidents dans les services externes entraînant une perte de données</span><span class="sxs-lookup"><span data-stu-id="66e75-110">Incidents in external services that result in some loss of data</span></span> 

<span data-ttu-id="66e75-p102">Étant donné que la résilience accrue de l'intégrité des données signifie moins d'incidents d'endommagement des données, Microsoft a intégré les mécanismes de protection d'Office 365 pour empêcher la corruption, ainsi que les systèmes et les processus qui nous permettent de récupérer les données le cas échéant. Il existe des vérifications et des processus dans les différentes étapes du processus de publication d'ingénierie afin de renforcer la résistance contre l'altération des données, notamment:</span><span class="sxs-lookup"><span data-stu-id="66e75-p102">Because greater resiliency in data integrity means fewer data corruption incidents, Microsoft has built into Office 365 protection mechanisms to prevent corruption from happening, as well as systems and processes that enable us to recover data if it does. Checks and processes exist within the various stages of the engineering release process to increase resiliency against data corruption, including:</span></span>
- <span data-ttu-id="66e75-113">Conception du système</span><span class="sxs-lookup"><span data-stu-id="66e75-113">System Design</span></span>
- <span data-ttu-id="66e75-114">Structure et organisation du code</span><span class="sxs-lookup"><span data-stu-id="66e75-114">Code organization and structure</span></span> 
- <span data-ttu-id="66e75-115">Révision du code</span><span class="sxs-lookup"><span data-stu-id="66e75-115">Code review</span></span> 
- <span data-ttu-id="66e75-116">Tests d'unité, tests d'intégration et tests système</span><span class="sxs-lookup"><span data-stu-id="66e75-116">Unit tests, integration tests, and system tests</span></span>
- <span data-ttu-id="66e75-117">Tests/portails de fils de voyage</span><span class="sxs-lookup"><span data-stu-id="66e75-117">Trip wires tests/gates</span></span> 

<span data-ttu-id="66e75-p103">Dans les environnements de production Office 365, la réplication d'homologue entre centres de données garantit qu'il y a toujours plusieurs copies dynamiques de toutes les données. Les images et les scripts standard permettent de récupérer les serveurs perdus, et les données répliquées sont utilisées pour restaurer les données client. En raison des contrôles et des processus de résilience des données intégrés, Microsoft conserve uniquement les sauvegardes de la documentation du système d'informations Office 365 (y compris la documentation liée à la sécurité), à l'aide de la réplication intégrée dans SharePoint Online et de notre code interne outil référentiel, dépôt source. La documentation système est stockée dans SharePoint Online, et Source Depot contient des images système et d'application. SharePoint Online et le SAV source utilisent tous deux le contrôle de version et sont répliqués en quasi-temps réel.</span><span class="sxs-lookup"><span data-stu-id="66e75-p103">Within Office 365 production environments, peer replication between datacenters ensures that there are always multiple live copies of any data. Standard images and scripts are used to recover lost servers, and replicated data is used to restore customer data. Because of the built-in data resiliency checks and processes, Microsoft maintains backups only of Office 365 information system documentation (including security-related documentation), using built-in replication in SharePoint Online and our internal code repository tool, Source Depot. System documentation is stored in SharePoint Online, and Source Depot contains system and application images. Both SharePoint Online and Source Depot use versioning and are replicated in near real-time.</span></span> 