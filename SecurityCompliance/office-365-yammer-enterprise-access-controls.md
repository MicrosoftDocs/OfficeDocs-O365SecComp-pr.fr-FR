---
title: Contrôles d’accès Yammer Enterprise pour Office 365
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
description: 'Résumé: Résumé succinct sur les contrôles d’accès aux entreprises Yammer dans l’environnement de production.'
ms.openlocfilehash: ec1a5767495b6b183ceda2af558cbec0c479e956
ms.sourcegitcommit: aa60a6cdf83c67576e858668d1182cd4fffeb5e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2019
ms.locfileid: "33622314"
---
# <a name="yammer-enterprise-access-controls"></a><span data-ttu-id="cb09a-103">Contrôles d’accès Yammer Entreprise</span><span class="sxs-lookup"><span data-stu-id="cb09a-103">Yammer Enterprise Access Controls</span></span> 

<span data-ttu-id="cb09a-104">L’accès physique et logique à l’environnement de production Yammer est limité à un petit ensemble de personnes (infrastructure et opérations).</span><span class="sxs-lookup"><span data-stu-id="cb09a-104">Physical and logical access to the Yammer production environment is restricted to a small set of people (infrastructure and operations).</span></span> <span data-ttu-id="cb09a-105">Comme avec d’autres ingénieurs Office 365, les ingénieurs Yammer disposent d’un accès permanent aux données client.</span><span class="sxs-lookup"><span data-stu-id="cb09a-105">As with other Office 365 engineers, Yammer engineers have zero standing access to Customer Data.</span></span> <span data-ttu-id="cb09a-106">L’accès doit être demandé à l’aide d’un système de contrôle d’accès juste-à-temps basé sur l’approbation, comme le Lockbox avec un nombre limité d’approbateurs.</span><span class="sxs-lookup"><span data-stu-id="cb09a-106">Access must be requested using an approval-based just-in-time access control system similar to Lockbox with a limited number of approvers.</span></span> <span data-ttu-id="cb09a-107">Les approbateurs vérifient la demande (par exemple, ils vérifient si la demande est légitime en fonction de la demande, du cas client, du temps, etc.), puis approuvez ou refusez la demande.</span><span class="sxs-lookup"><span data-stu-id="cb09a-107">Approvers verify the request (for example, they verify whether the request is legitimate based on need, business case, time, etc.), and then approve or deny the request.</span></span> <span data-ttu-id="cb09a-108">Si la demande est approuvée, l’accès JIT est accordé pour un temps défini et limité.</span><span class="sxs-lookup"><span data-stu-id="cb09a-108">If the request is approved, JIT access is granted for a defined and limited time.</span></span> <span data-ttu-id="cb09a-109">Une fois le temps d’accès dépassé, l’accès expire automatiquement.</span><span class="sxs-lookup"><span data-stu-id="cb09a-109">After access time is exceeded, the access automatically expires.</span></span>

<span data-ttu-id="cb09a-110">Tout comme les autres services Office 365, tout accès à l’environnement de production Yammer utilise l’authentification multifacteur.</span><span class="sxs-lookup"><span data-stu-id="cb09a-110">As with other Office 365 services, all access to the Yammer production environment uses multi-factor authentication.</span></span> <span data-ttu-id="cb09a-111">Tous les accès et historique des commandes sont attribués à un utilisateur et sont consignés et révisés régulièrement par l’équipe de sécurité Yammer.</span><span class="sxs-lookup"><span data-stu-id="cb09a-111">All access and command history is attributed to a user, and logged and reviewed regularly by the Yammer security team.</span></span>

<span data-ttu-id="cb09a-112">Pour plus d’informations sur l’administration et la gestion de Yammer, consultez [l’aide de l’administrateur de Yammer](https://support.office.com/article/yammer-–-admin-help-e1464355-1f97-49ac-b2aa-dd320b179dbe?ui=en-US&rs=en-US&ad=US).</span><span class="sxs-lookup"><span data-stu-id="cb09a-112">For more information about Yammer administration and management, see [Yammer Admin Help](https://support.office.com/article/yammer-–-admin-help-e1464355-1f97-49ac-b2aa-dd320b179dbe?ui=en-US&rs=en-US&ad=US).</span></span>