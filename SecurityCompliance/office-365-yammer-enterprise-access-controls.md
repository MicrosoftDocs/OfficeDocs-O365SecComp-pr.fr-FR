---
title: Accéder à des contrôles Office 365 Yammer Enterprise
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
description: 'Résumé : Un bref résumé sur Yammer Enterprise accéder à des contrôles dans l’environnement de production.'
ms.openlocfilehash: 3f51e63c16022353e743b57d8e977f2ea2e6a835
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528623"
---
# <a name="yammer-enterprise-access-controls"></a><span data-ttu-id="88fcb-103">Contrôles d’accès entreprise Yammer</span><span class="sxs-lookup"><span data-stu-id="88fcb-103">Yammer Enterprise Access Controls</span></span> 

<span data-ttu-id="88fcb-p101">Accès physique et logique à l’environnement de production Yammer est limité à un très petit ensemble de personnes (infrastructure et opérations). Comme avec les autres ingénieurs d’Office 365, Yammer ingénieurs ont aucun accès permanent aux données client. Access doit être demandé à l’aide d’un système de contrôle d’accès juste-à-temps approbation similaire à la zone de sécurité, et il est un nombre limité d’approbateurs. Approbateurs vérifier la demande (par exemple, ils vérifier si la demande est légitime en fonction de la nécessité, étude de cas, le temps, etc.), puis approuver ou refuser la demande. Si la demande est approuvée, juste l’accès pendant une durée définie et limitée, après laquelle il expire automatiquement.</span><span class="sxs-lookup"><span data-stu-id="88fcb-p101">Both physical and logical access to the Yammer production environment is restricted to a very small set of people (infrastructure and operations). As with other Office 365 engineers, Yammer engineers have zero standing access to Customer Data. Access must be requested using an approval-based just-in-time access control system similar to Lockbox, and there is a limited number of approvers. Approvers verify the request (e.g., they verify whether the request is legitimate based on need, business case, time, etc.), and then approve or deny the request. If the request is approved, JIT access is granted for a defined and limited time, after which it automatically expires.</span></span> 

<span data-ttu-id="88fcb-p102">Comme avec les autres services Office 365, tous les accès à l’environnement de production Yammer s’appuie sur l’authentification multifacteur. Tous les accès et commandes de l’historique est attribué à un utilisateur et ouvert une session et révisé régulièrement par l’équipe de sécurité de Yammer.</span><span class="sxs-lookup"><span data-stu-id="88fcb-p102">As with other Office 365 services, all access to the Yammer production environment leverages multi-factor authentication. All access and command history is attributed to a user, and logged and reviewed regularly by the Yammer security team.</span></span>

<span data-ttu-id="88fcb-111">Pour plus d’informations sur l’administration et de Yammer, voir [Aide de l’administration Yammer](https://support.office.com/article/yammer-–-admin-help-e1464355-1f97-49ac-b2aa-dd320b179dbe?ui=en-US&rs=en-US&ad=US).</span><span class="sxs-lookup"><span data-stu-id="88fcb-111">For more information about Yammer administration and management, see [Yammer Admin Help](https://support.office.com/article/yammer-–-admin-help-e1464355-1f97-49ac-b2aa-dd320b179dbe?ui=en-US&rs=en-US&ad=US).</span></span>