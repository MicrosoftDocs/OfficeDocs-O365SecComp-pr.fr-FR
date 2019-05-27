---
title: Rechercher et identifier les courriers électroniques malveillants remis (Office 365 Threat Investigation and Response
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/19/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 8f54cd33-4af7-4d1b-b800-68f8818e5b2a
ms.collection:
- M365-security-compliance
description: Découvrez comment utiliser les fonctionnalités d’analyse et de réponse aux menaces pour rechercher et examiner des courriers électroniques malveillants.
ms.openlocfilehash: 7e2cef742339e54c094cfb0c3b32fbf596896a3d
ms.sourcegitcommit: 2b46fba650df8d252b1dd2b3c3f080a383183a06
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/23/2019
ms.locfileid: "34408299"
---
# <a name="find-and-investigate-malicious-email-that-was-delivered-office-365-advanced-threat-protection-plan-2"></a>Rechercher et identifier les messages électroniques malveillants qui ont été remis (Office 365 Advanced Threat Protection Plan 2)

[Office 365 Advanced Threat Protection](office-365-atp.md) vous permet d’examiner les activités qui permettent aux utilisateurs de protéger votre organisation. Par exemple, si vous participez à l’équipe de sécurité de votre organisation, vous pouvez rechercher et enquêter sur les messages électroniques suspects qui ont été remis à vos utilisateurs. Vous pouvez le faire à l’aide de l' [Explorateur de menaces (ou des détections en temps réel)](threat-explorer.md).
  
## <a name="before-you-begin"></a>Avant de commencer...

Assurez-vous que les conditions suivantes sont remplies :
  
- Votre organisation a [Office 365 Advanced Threat Protection](office-365-atp.md) (plan 1 ou plan 2) et des [licences sont attribuées à des utilisateurs](https://docs.microsoft.com/en-us/office365/admin/subscriptions-and-billing/assign-licenses-to-users).
    
- La [journalisation d’audit Office 365](turn-audit-log-search-on-or-off.md) est activée pour votre organisation. 
    
- Votre organisation a défini des stratégies pour le blocage du courrier indésirable, anti-programme malveillant, anti-hameçonnage, etc. Consultez la rubrique Protégez-vous [contre les menaces dans Office 365](protect-against-threats.md).
    
- Vous êtes un administrateur général Office 365 ou vous avez l’administrateur de sécurité ou le rôle de recherche et de purge affecté dans le centre &amp; de sécurité et de conformité. Consultez [la rubrique autorisations dans le centre &amp; de sécurité conformité Office 365](permissions-in-the-security-and-compliance-center.md).
    
## <a name="dealing-with-suspicious-emails"></a>Traitement des e-mails suspects

Les utilisateurs malveillants peuvent envoyer des courriers électroniques à vos utilisateurs pour essayer d’envoyer leurs informations d’identification et accéder à vos secrets d’entreprise. Pour éviter cela, vous devez utiliser les services de protection contre les menaces offerts par Office 365, y compris [Exchange Online Protection](eop/exchange-online-protection-overview.md) et [Advanced Threat Protection](office-365-atp.md). Toutefois, il arrive qu’un agresseur puisse envoyer un message électronique à vos utilisateurs contenant une URL et, par la suite, faire pointer cette URL vers du contenu malveillant (programmes malveillants, etc.). En guise d’alternative, vous pouvez vous rendre compte que l’utilisateur de votre organisation a été compromis, tandis que ce dernier a été compromis, un agresseur l’a utilisé pour envoyer des courriers électroniques à d’autres utilisateurs de votre entreprise. Dans le cadre du nettoyage de ces deux scénarios, vous souhaiterez peut-être supprimer les messages électroniques des boîtes de réception des utilisateurs. Dans ce cas, vous pouvez utiliser l' [Explorateur de menaces (ou les détections en temps réel)](threat-explorer.md) pour rechercher et supprimer ces messages électroniques.
  
## <a name="find-and-delete-suspicious-email-that-was-delivered"></a>Rechercher et supprimer les e-mails suspects qui ont été remis

> [!TIP]
> L’Explorateur de menaces (également appelé Explorateur) est un rapport puissant qui peut servir plusieurs objectifs, tels que la recherche et la suppression de messages, l’identification de l’adresse IP d’un expéditeur de courrier malveillant ou le démarrage d’un incident à des fins d’enquête. La procédure suivante décrit l’utilisation de l’Explorateur pour rechercher et supprimer des courriers électroniques malveillants provenant de boîtes aux lettres de destinataires. 
  
1. Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous à l’aide de votre compte professionnel ou scolaire pour Office 365. Vous accédez au centre de sécurité &amp; conformité. 
    
2. Dans le volet de navigation de gauche, choisissez **Explorateur**de **gestion** \> des menaces.
    
3. Dans le menu Affichage, choisissez **tous les messages électroniques**.<br/>![Utiliser le menu Affichage pour choisir entre les rapports de courrier électronique et de contenu](media/d39013ff-93b6-42f6-bee5-628895c251c2.png)
  
4. Notez les étiquettes qui apparaissent dans le rapport, telles que **remis**, **inconnu**ou **remis au courrier**indésirable.<br/>![Explorateur de menaces affichant les données de tous les messages électroniques](media/208826ed-a85e-446f-b276-b5fdc312fbcb.png)<br/>(En fonction des actions effectuées sur les messages électroniques de votre organisation, vous pouvez voir des étiquettes supplémentaires, telles que **bloqué** ou **remplacé**.)
    
5. Dans le rapport, choisissez **remis** pour afficher uniquement les courriels qui se sont terminés dans les boîtes de réception des utilisateurs.<br/>![Le fait de cliquer sur «remis au courrier indésirable» supprime ces données de l’affichage](media/e6fb2e47-461e-4f6f-8c65-c331bd858758.png)
  
6. Sous le graphique, passez en revue la liste des **messages** sous le graphique.<br/>![Sous le graphique, affichez la liste des messages électroniques qui ont été détectés.](media/dfb60590-1236-499d-97da-86c68621e2bc.png)
  
7. Dans la liste, choisissez un élément pour afficher plus d’informations sur ce message électronique. Par exemple, vous pouvez cliquer sur la ligne d’objet pour afficher des informations sur l’expéditeur, les destinataires, les pièces jointes et d’autres messages électroniques similaires.<br/>![Vous pouvez afficher des informations supplémentaires sur un élément, notamment des détails et des pièces jointes.](media/5a5707c3-d62a-4610-ae7b-900fff8708b2.png)
  
8. Après avoir consulté les informations sur les messages électroniques, sélectionnez un ou plusieurs éléments de la liste à activer **+ actions**.
    
9. Utilisez la liste **+ actions** pour appliquer une action, telle que **déplacer vers** les éléments supprimés. Cette opération supprime les messages sélectionnés des boîtes aux lettres des destinataires.<br/>![Lorsque vous sélectionnez un ou plusieurs messages électroniques, vous pouvez choisir parmi plusieurs actions disponibles.](media/ef12e10c-60a7-4f66-8f76-68d77ae26de1.png)
  
## <a name="related-topics"></a>Sujets associés

[Plan 2 de protection avancée contre les menaces Office 365](office-365-ti.md)
  
[Se protéger contre les menaces dans Office 365](protect-against-threats.md)
  
[Afficher les rapports pour Office 365 protection avancée contre les menaces](view-reports-for-atp.md)
  

