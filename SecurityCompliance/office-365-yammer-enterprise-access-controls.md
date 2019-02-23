---
title: Contrôles d'accès Yammer Enterprise pour Office 365
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
description: "Résumé: Résumé succinct sur les contrôles d'accès aux entreprises Yammer dans l'environnement de production."
ms.openlocfilehash: 76b62e7ea026a52d822e5a213461e930b1d595e3
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217884"
---
# <a name="yammer-enterprise-access-controls"></a><span data-ttu-id="b15ea-103">Contrôles d’accès Yammer Entreprise</span><span class="sxs-lookup"><span data-stu-id="b15ea-103">Yammer Enterprise Access Controls</span></span> 

<span data-ttu-id="b15ea-p101">L'accès physique et logique à l'environnement de production Yammer est limité à un très petit ensemble de personnes (infrastructure et opérations). Comme avec d'autres ingénieurs Office 365, les ingénieurs Yammer disposent d'un accès permanent aux données client. L'accès doit être demandé à l'aide d'un système de contrôle d'accès juste-à-temps basé sur l'approbation, comme le Lockbox, et il existe un nombre limité d'approbateurs. Les apProbateurs vérifient la demande (par exemple, ils vérifient si la demande est légitime en fonction de la demande, du cas client, du temps, etc.), puis approuvez ou refusez la demande. Si la demande est approuvée, l'accès JIT est accordé pour un temps défini et limité, après quoi il expire automatiquement.</span><span class="sxs-lookup"><span data-stu-id="b15ea-p101">Both physical and logical access to the Yammer production environment is restricted to a very small set of people (infrastructure and operations). As with other Office 365 engineers, Yammer engineers have zero standing access to Customer Data. Access must be requested using an approval-based just-in-time access control system similar to Lockbox, and there is a limited number of approvers. Approvers verify the request (e.g., they verify whether the request is legitimate based on need, business case, time, etc.), and then approve or deny the request. If the request is approved, JIT access is granted for a defined and limited time, after which it automatically expires.</span></span> 

<span data-ttu-id="b15ea-p102">Tout comme les autres services Office 365, tous les accès à l'environnement de production Yammer tirent parti de l'authentification multifacteur. Tous les accès et historique des commandes sont attribués à un utilisateur et sont consignés et révisés régulièrement par l'équipe de sécurité Yammer.</span><span class="sxs-lookup"><span data-stu-id="b15ea-p102">As with other Office 365 services, all access to the Yammer production environment leverages multi-factor authentication. All access and command history is attributed to a user, and logged and reviewed regularly by the Yammer security team.</span></span>

<span data-ttu-id="b15ea-111">Pour plus d'informations sur l'administration et la gestion de Yammer, consultez [l'aide de l'administrateur de Yammer](https://support.office.com/article/yammer-–-admin-help-e1464355-1f97-49ac-b2aa-dd320b179dbe?ui=en-US&rs=en-US&ad=US).</span><span class="sxs-lookup"><span data-stu-id="b15ea-111">For more information about Yammer administration and management, see [Yammer Admin Help](https://support.office.com/article/yammer-–-admin-help-e1464355-1f97-49ac-b2aa-dd320b179dbe?ui=en-US&rs=en-US&ad=US).</span></span>