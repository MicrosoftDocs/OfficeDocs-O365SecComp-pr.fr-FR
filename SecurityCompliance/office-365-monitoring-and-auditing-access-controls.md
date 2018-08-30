---
title: Office 365 surveillance et l’audit des contrôles d’accès
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
description: 'Résumé : Un résumé des différents surveillance et audit contrôles d’accès disponibles dans Office 365.'
ms.openlocfilehash: 7ef25d62ce3c4fa320dd0b164183c6f67be7d76d
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528622"
---
# <a name="monitoring-and-auditing-access-controls-in-office-365"></a>Surveillance et l’audit des contrôles d’accès dans Office 365

Microsoft effectue des étendues de surveillance et d’audit de toutes les opérations qui se produisent dans Office 365, l’utilisation de privilèges et la délégation tous les. Contrôle d’accès 365 Office est un processus automatisé reposant sur le principe des privilèges minimum et à intégrer les données des contrôles d’accès et des audits :
- Tous les accès autorisés sont conforme à un utilisateur unique, pour les administrateurs responsables de leur traitement de contenu de client.
- Demandes de contrôle d’accès, les approbations et les journaux d’opérations d’administration sont capturés pour l’analyse des perspectives sur la sécurité et les événements malveillants.
- Niveaux d’accès sont examinées dans près de l’appartenance au groupe de sécurité en fonction d’en temps réel pour garantir que seuls les utilisateurs qui ont autorisé justification métier et de réunir les conditions préalables ont accès aux systèmes.
- Office 365, ses contrôles d’accès et les services de prise en charge, y compris Azure Active Directory et nos centres de données physique, sont régulièrement audités par des tiers indépendants pour se conformer à la [spécification ISO/IEC 27001](https://www.microsoft.com/en-us/TrustCenter/Compliance/iso-iec-27001), [ISO/IEC 27018](https://www.microsoft.com/en-us/TrustCenter/Compliance/iso-iec-27018), [sociale](https://www.microsoft.com/en-us/TrustCenter/Compliance/SOC), [FedRAMP](https://www.microsoft.com/en-us/TrustCenter/Compliance/FedRAMP)et autres [normes](https://www.microsoft.com/en-us/TrustCenter/Compliance?service=Office#Icons).
- Ingénieurs d’Office 365 sont nécessaires pour prendre annuel formation sécurité examen des risques et des méthodes conseillées avec élévation de privilèges d’accès et confirmer la sécurité et les stratégies de confidentialité pour continuer à gérer leurs droits d’accès au service de Microsoft.

Alertes automatiques sont déclenchées lorsqu’une activité suspecte est détectée, tels que plusieurs échecs de connexion au sein d’une courte période. L’équipe de réponse de sécurité Office 365 utilise apprentissage automatique et l’analyse des données big passer en revue et analyser l’activité des modèles d’accès irrégulier et répondre aux activités anormales et illicites de manière proactive. Microsoft utilise une équipe de testeurs d’intrusion spécialisés et effectue des équipes rouge périodiques et bleu exercices pour trouver la sécurité et d’accéder aux problèmes de contrôle dans le service. Les clients peuvent également vérifier l’efficacité des systèmes de contrôle d’accès à l’aide de rapports d’audit et l’activité de gestion des API fournie par Office 365. 

Pour plus d’informations, voir [référence de l’API d’activité Office 365 gestion](https://msdn.microsoft.com/en-us/library/office/mt227394.aspx) et [l’audit et la création de rapports dans Office 365](office-365-auditing-and-reporting-overview.md).
