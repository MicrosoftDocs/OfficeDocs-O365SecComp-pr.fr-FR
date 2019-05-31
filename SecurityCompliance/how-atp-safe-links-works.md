---
title: Fonctionnement des liaisons approuvées ATP Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
audience: Admin
ms.date: 05/19/2019
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: La fonctionnalité liens fiables permet de vérifier le temps de cliquer sur les liens hypertexte dans les documents Office et dans les messages électroniques. Lisez cet article pour découvrir le fonctionnement des liens fiables ATP.
ms.openlocfilehash: eb4c9f9eea18990df190185a78b5a8c333e53659
ms.sourcegitcommit: 424a614141c1f19a1c84a67ec2d71dd3d7ef6694
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/30/2019
ms.locfileid: "34592256"
---
# <a name="how-office-365-atp-safe-links-works"></a>Fonctionnement des liaisons approuvées ATP Office 365
         
## <a name="how-atp-safe-links-works-with-urls-in-email"></a>Fonctionnement des liaisons approuvées ATP avec les URL dans les messages électroniques

À un niveau élevé, voici le fonctionnement de la protection [des liens fiables ATP](atp-safe-links.md) pour les URL dans les messages électroniques (hébergé dans Office 365, pas en local):
  
1. Les utilisateurs reçoivent des messages électroniques, dont certains contiennent des URL.
    
2. Tous les messages passent par Exchange Online Protection, où les filtres IP (Internet Protocol) et des enveloppes, la protection contre les programmes malveillants basée sur la signature, le blocage du courrier indésirable et les filtres anti-programme malveillant sont appliqués. 
    
3. Le courrier électronique arrive dans les boîtes de réception des utilisateurs.
    
4. Un utilisateur se connecte à Office 365 et accède à sa boîte de réception.
    
5. L’utilisateur ouvre un message électronique et clique sur une URL dans le message électronique.
    
6. La fonctionnalité de liens fiables ATP vérifie immédiatement l’URL avant d’ouvrir le site Web. L’URL est identifiée comme étant bloquée, malveillante ou sécurisée.
    
    - Si l’URL est vers un site Web qui est inclus dans une [liste d’URL «ne pas réécrire» personnalisée](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) pour une stratégie qui s’applique à l’utilisateur, le site Web s’ouvre. 
    
    - Si l’URL est vers un site Web inclus dans la [liste des URL bloquées personnalisées](set-up-a-custom-blocked-urls-list-wtih-atp.md)de l’organisation, une [page d’avertissement](atp-safe-links-warning-pages.md) s’ouvre. 
    
    - Si l’URL est vers un site Web qui a été jugé malveillant, une [page d’avertissement](atp-safe-links-warning-pages.md) s’ouvre. 
    
    - Si l’URL est dirigée vers un fichier téléchargeable et que les [stratégies de liens fiables ATP](set-up-atp-safe-links-policies.md) de votre organisation sont configurées pour analyser ce contenu, le fichier téléchargeable est vérifié. 
    
    - Si l’URL est jugée fiable, le site Web s’ouvre.
    
## <a name="how-atp-safe-links-works-with-urls-in-office-documents"></a>Fonctionnement des liaisons approuvées ATP avec les URL des documents Office

À un niveau élevé, voici le fonctionnement de la protection [des liens fiables ATP](atp-safe-links.md) pour les URL dans les applications Office 365 ProPlus (versions actuelles de Word, Excel et PowerPoint sur Windows ou Mac, les applications Office sur les appareils iOS ou Android, Visio sur Windows, OneNote Online et Office En ligne):
  
1. Les utilisateurs ont installé Office 365 ProPlus sur leur ordinateur, smartphone ou tablette. (Ou, ils utilisent Office Online dans leur navigateur.)
    
2. Un utilisateur ouvre un mot, Excel, PowerPoint ou Visio et se connecte à Office 365 Enterprise à l’aide de son compte professionnel ou scolaire. Le document contient des URL.
    
3. Lorsque l’utilisateur clique sur une URL dans le document, le lien est vérifié par le service de liens fiables ATP.
    
      - Si l’URL est vers un site Web qui est inclus dans une [liste d’URL «ne pas réécrire» personnalisée](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) pour une stratégie qui s’applique à l’utilisateur, cet utilisateur est dirigé vers le site Web. 
    
      - Si l’URL est vers un site Web inclus dans la [liste des URL bloquées personnalisées](set-up-a-custom-blocked-urls-list-wtih-atp.md)de l’organisation, l’utilisateur est dirigé vers une [page d’avertissement](atp-safe-links-warning-pages.md).
    
      - Si l’URL est vers un site Web qui a été jugé malveillant, l’utilisateur est dirigé vers une [page d’avertissement](atp-safe-links-warning-pages.md).
    
      - Si l’URL mène à un fichier téléchargeable et que les [stratégies de liens fiables ATP](set-up-atp-safe-links-policies.md) sont configurées pour analyser ces téléchargements, le fichier téléchargeable est vérifié. 
    
      - Si l’URL est considérée comme fiable, l’utilisateur est dirigé vers le site Web.

