---
title: Contrôles d'accès Yammer Enterprise pour Office 365
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
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: "Résumé: Résumé succinct sur les contrôles d'accès aux entreprises Yammer dans l'environnement de production."
ms.openlocfilehash: 33126ee6acf42a97148c12917855535a8578e8cf
ms.sourcegitcommit: c94cb88a9ce5bcc2d3c558f0fcc648519cc264a2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2019
ms.locfileid: "30090726"
---
# <a name="yammer-enterprise-access-controls"></a>Contrôles d’accès Yammer Entreprise 

L'accès physique et logique à l'environnement de production Yammer est limité à un très petit ensemble de personnes (infrastructure et opérations). Comme avec d'autres ingénieurs Office 365, les ingénieurs Yammer disposent d'un accès permanent aux données client. L'accès doit être demandé à l'aide d'un système de contrôle d'accès juste-à-temps basé sur l'approbation, comme le Lockbox, et il existe un nombre limité d'approbateurs. Les apProbateurs vérifient la demande (par exemple, ils vérifient si la demande est légitime en fonction de la demande, du cas client, du temps, etc.), puis approuvez ou refusez la demande. Si la demande est approuvée, l'accès JIT est accordé pour un temps défini et limité, après quoi il expire automatiquement. 

Tout comme les autres services Office 365, tous les accès à l'environnement de production Yammer tirent parti de l'authentification multifacteur. Tous les accès et historique des commandes sont attribués à un utilisateur et sont consignés et révisés régulièrement par l'équipe de sécurité Yammer.

Pour plus d'informations sur l'administration et la gestion de Yammer, consultez [l'aide de l'administrateur de Yammer](https://support.office.com/article/yammer-–-admin-help-e1464355-1f97-49ac-b2aa-dd320b179dbe?ui=en-US&rs=en-US&ad=US).