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
# <a name="yammer-enterprise-access-controls"></a>Contrôles d’accès Yammer Entreprise 

L’accès physique et logique à l’environnement de production Yammer est limité à un petit ensemble de personnes (infrastructure et opérations). Comme avec d’autres ingénieurs Office 365, les ingénieurs Yammer disposent d’un accès permanent aux données client. L’accès doit être demandé à l’aide d’un système de contrôle d’accès juste-à-temps basé sur l’approbation, comme le Lockbox avec un nombre limité d’approbateurs. Les approbateurs vérifient la demande (par exemple, ils vérifient si la demande est légitime en fonction de la demande, du cas client, du temps, etc.), puis approuvez ou refusez la demande. Si la demande est approuvée, l’accès JIT est accordé pour un temps défini et limité. Une fois le temps d’accès dépassé, l’accès expire automatiquement.

Tout comme les autres services Office 365, tout accès à l’environnement de production Yammer utilise l’authentification multifacteur. Tous les accès et historique des commandes sont attribués à un utilisateur et sont consignés et révisés régulièrement par l’équipe de sécurité Yammer.

Pour plus d’informations sur l’administration et la gestion de Yammer, consultez [l’aide de l’administrateur de Yammer](https://support.office.com/article/yammer-–-admin-help-e1464355-1f97-49ac-b2aa-dd320b179dbe?ui=en-US&rs=en-US&ad=US).