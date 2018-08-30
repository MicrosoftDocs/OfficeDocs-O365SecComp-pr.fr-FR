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
# <a name="dealing-with-data-corruption-in-office-365"></a>Traitement de Corruption des données dans Office 365

Un des aspects de l’exécution d’un service en nuage à grande échelle difficiles est comment gérer corruption des données, étant donné le volume de données et des systèmes indépendants. Corruption des données peut être dû à :
- Infrastructure ou application bugs, corrompre tout ou partie de l’état de l’application 
- Configuration matérielle des problèmes de perte de données ou une incapacité à lire des données 
- Erreurs opérationnelles humaines 
- Pirates et employés mécontents 
- Incidents dans les services externes entraîner une perte de données 

Car la résistance supérieure dans l’intégrité des données signifie moins incidents liés à la corruption des données, Microsoft a intégré dans Office 365 les mécanismes de protection pour éviter l’endommagement de se produise, ainsi que des systèmes et des processus qui nous permet de récupérer des données si c’est. Contrôles et les processus existent dans les différentes phases du processus de publication ingénierie pour accroître la résilience toute corruption des données, y compris :
- Conception du système
- Organisation de code et la structure 
- Examen du code 
- Tests unitaires, les tests d’intégration et les tests du système
- Voyage fils de tests/portails 

Dans les environnements de production d’Office 365, la réplication égal entre les centres de données permet de s’assurer qu’il n’y a toujours plusieurs copies live de toutes les données. Scripts et des images standards sont utilisés pour la récupération des serveurs perdues, et les données répliquées sont utilisées pour restaurer les données du client. En raison des vérifications de résistance de données intégrée et les processus Microsoft gère les sauvegardes uniquement de la documentation du système d’informations Office 365 (y compris la documentation relatives à la sécurité), à l’aide de la réplication intégrée dans SharePoint Online et notre code interne outil de référentiel, dépôt Source. Documentation du système est stockée dans SharePoint Online et dépôt Source contient des images système et des applications. SharePoint Online et dépôt Source utilisent le contrôle de version et sont répliqués dans presque en temps réel. 