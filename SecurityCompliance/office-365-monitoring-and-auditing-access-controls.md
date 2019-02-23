---
title: Office 365 surveillance et audit des contrôles d'accès
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
description: "Résumé: Résumé des différents contrôles d'accès au contrôle et à l'audit disponibles dans Office 365."
ms.openlocfilehash: 91d78ba3de41554755a7c19799eb1f7b25933b05
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217734"
---
# <a name="monitoring-and-auditing-access-controls-in-office-365"></a>Surveillance et audit des contrôles d'accès dans Office 365

Microsoft effectue une surveillance et un audit détaillés de toutes les délégations, de toutes les opérations de privilèges et de toutes les opérations qui se produisent dans Office 365. Le contrôle d'accès Office 365 est un processus automatisé basé sur le principe des privilèges minimum et pour incorporer les contrôles d'accès aux données et les audits:
- Tous les accès autorisés sont traçables vers un utilisateur unique, ce qui rend les administrateurs responsables de la gestion du contenu du client.
- Les demandes de contrôle d'accès, les approbations et les journaux des opérations d'administration sont capturés pour analyser les informations de sécurité et les événements malveillants.
- Les niveaux d'accès sont examinés en quasi-temps réel en fonction de l'appartenance au groupe de sécurité afin de s'assurer que seuls les utilisateurs qui ont autorisé les justifications professionnelles et satisfont aux exigences d'éligibilité ont accès aux systèmes.
- Office 365, ses contrôles d'accès et ses services de prise en charge, y compris Azure Active Directory et nos centres de documents physiques, sont régulièrement contrôlés par des tiers indépendants pour la conformité à la [norme ISO/iec 27001](https://www.microsoft.com/en-us/TrustCenter/Compliance/iso-iec-27001), [iso/IEC 27018](https://www.microsoft.com/en-us/TrustCenter/Compliance/iso-iec-27018), [SOC](https://www.microsoft.com/en-us/TrustCenter/Compliance/SOC), [FedRAMP](https://www.microsoft.com/en-us/TrustCenter/Compliance/FedRAMP), ainsi que d'autres [normes](https://www.microsoft.com/en-us/TrustCenter/Compliance?service=Office#Icons).
- Les ingénieurs Office 365 sont tenus de prendre des mesures de sécurité annuelles afin de vérifier les meilleures pratiques et les risques d'accès élevés et de faire en sorte que les stratégies de sécurité et de confidentialité de Microsoft continuent de maintenir leurs habilitations pour le service.

Les alertes automatisées sont déclenchées lorsqu'une activité suspecte est détectée, par exemple, plusieurs échecs de connexion au cours d'une courte période. L'équipe de sécurité de la sécurité d'Office 365 utilise l'apprentissage automatique et l'analyse des données volumineuses pour examiner et analyser l'activité des modèles d'accès irréguliers et répondre de manière proactive aux activités anormales et illicites. Microsoft utilise également une équipe dédiée de testeurs de pénétration et s'engage dans les exercices de l'équipe rouge périodique et de l'équipe bleue pour rechercher les problèmes de sécurité et de contrôle d'accès dans le service. Les clients peuvent également vérifier l'efficacité des systèmes de contrôle d'accès à l'aide de rapports d'audit et de l'API activité de gestion fournies par Office 365. 

Pour plus d'informations, voir référence de l' [API activité de gestion office 365](https://msdn.microsoft.com/en-us/library/office/mt227394.aspx) et [audit et création de rapports dans Office 365](office-365-auditing-and-reporting-overview.md).
