---
title: Office 365 traitement de Corruption des données
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: Explication de corruption des données dans Office 365 et les efforts de Microsoft de prévention et de récupération.
ms.openlocfilehash: 087be23ce5dad1daf62357cb08e27c0a15962792
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528194"
---
# <a name="dealing-with-data-corruption-in-office-365"></a><span data-ttu-id="a3c1b-103">Traitement de Corruption des données dans Office 365</span><span class="sxs-lookup"><span data-stu-id="a3c1b-103">Dealing with Data Corruption in Office 365</span></span>

<span data-ttu-id="a3c1b-p101">Un des aspects de l’exécution d’un service en nuage à grande échelle difficiles est comment gérer corruption des données, étant donné le volume de données et des systèmes indépendants. Corruption des données peut être dû à :</span><span class="sxs-lookup"><span data-stu-id="a3c1b-p101">One of the challenging aspects of running a large-scale cloud service is how to handle data corruption, given the large volume of data and independent systems. Data corruption can be caused by:</span></span>
- <span data-ttu-id="a3c1b-106">Infrastructure ou application bugs, corrompre tout ou partie de l’état de l’application</span><span class="sxs-lookup"><span data-stu-id="a3c1b-106">Application or infrastructure bugs, corrupting some or all of the application state</span></span> 
- <span data-ttu-id="a3c1b-107">Configuration matérielle des problèmes de perte de données ou une incapacité à lire des données</span><span class="sxs-lookup"><span data-stu-id="a3c1b-107">Hardware issues that result in lost data or an inability to read data</span></span> 
- <span data-ttu-id="a3c1b-108">Erreurs opérationnelles humaines</span><span class="sxs-lookup"><span data-stu-id="a3c1b-108">Human operational errors</span></span> 
- <span data-ttu-id="a3c1b-109">Pirates et employés mécontents</span><span class="sxs-lookup"><span data-stu-id="a3c1b-109">Malicious hackers and disgruntled employees</span></span> 
- <span data-ttu-id="a3c1b-110">Incidents dans les services externes entraîner une perte de données</span><span class="sxs-lookup"><span data-stu-id="a3c1b-110">Incidents in external services that result in some loss of data</span></span> 

<span data-ttu-id="a3c1b-p102">Car la résistance supérieure dans l’intégrité des données signifie moins incidents liés à la corruption des données, Microsoft a intégré dans Office 365 les mécanismes de protection pour éviter l’endommagement de se produise, ainsi que des systèmes et des processus qui nous permet de récupérer des données si c’est. Contrôles et les processus existent dans les différentes phases du processus de publication ingénierie pour accroître la résilience toute corruption des données, y compris :</span><span class="sxs-lookup"><span data-stu-id="a3c1b-p102">Because greater resiliency in data integrity means fewer data corruption incidents, Microsoft has built into Office 365 protection mechanisms to prevent corruption from happening, as well as systems and processes that enable us to recover data if it does. Checks and processes exist within the various stages of the engineering release process to increase resiliency against data corruption, including:</span></span>
- <span data-ttu-id="a3c1b-113">Conception du système</span><span class="sxs-lookup"><span data-stu-id="a3c1b-113">System Design</span></span>
- <span data-ttu-id="a3c1b-114">Organisation de code et la structure</span><span class="sxs-lookup"><span data-stu-id="a3c1b-114">Code organization and structure</span></span> 
- <span data-ttu-id="a3c1b-115">Examen du code</span><span class="sxs-lookup"><span data-stu-id="a3c1b-115">Code review</span></span> 
- <span data-ttu-id="a3c1b-116">Tests unitaires, les tests d’intégration et les tests du système</span><span class="sxs-lookup"><span data-stu-id="a3c1b-116">Unit tests, integration tests, and system tests</span></span>
- <span data-ttu-id="a3c1b-117">Voyage fils de tests/portails</span><span class="sxs-lookup"><span data-stu-id="a3c1b-117">Trip wires tests/gates</span></span> 

<span data-ttu-id="a3c1b-p103">Dans les environnements de production d’Office 365, la réplication égal entre les centres de données permet de s’assurer qu’il n’y a toujours plusieurs copies live de toutes les données. Scripts et des images standards sont utilisés pour la récupération des serveurs perdues, et les données répliquées sont utilisées pour restaurer les données du client. En raison des vérifications de résistance de données intégrée et les processus Microsoft gère les sauvegardes uniquement de la documentation du système d’informations Office 365 (y compris la documentation relatives à la sécurité), à l’aide de la réplication intégrée dans SharePoint Online et notre code interne outil de référentiel, dépôt Source. Documentation du système est stockée dans SharePoint Online et dépôt Source contient des images système et des applications. SharePoint Online et dépôt Source utilisent le contrôle de version et sont répliqués dans presque en temps réel.</span><span class="sxs-lookup"><span data-stu-id="a3c1b-p103">Within Office 365 production environments, peer replication between datacenters ensures that there are always multiple live copies of any data. Standard images and scripts are used to recover lost servers, and replicated data is used to restore customer data. Because of the built-in data resiliency checks and processes, Microsoft maintains backups only of Office 365 information system documentation (including security-related documentation), using built-in replication in SharePoint Online and our internal code repository tool, Source Depot. System documentation is stored in SharePoint Online, and Source Depot contains system and application images. Both SharePoint Online and Source Depot use versioning and are replicated in near real-time.</span></span> 