---
title: Fonctionnement des pièces jointes sécurisées ATP Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
audience: Admin
ms.date: 05/17/2019
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
description: La fonctionnalité pièces jointes fiables permet de vérifier le temps de cliquer sur les pièces jointes des messages électroniques. Utilisez des pièces jointes fiables pour protéger votre organisation des fichiers malveillants envoyés ou reçus par courrier électronique.
ms.openlocfilehash: 99d31e327343971f6a7630e2a43ffd3044fbf976
ms.sourcegitcommit: 424a614141c1f19a1c84a67ec2d71dd3d7ef6694
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/30/2019
ms.locfileid: "34592255"
---
# <a name="how-ffice-365-atp-safe-attachments-works"></a>Fonctionnement des pièces jointes fiables ATP 365

## <a name="how-it-works"></a>Mode de fonctionnement

La fonctionnalité pièces jointes approuvées ATP vérifie les pièces jointes de courrier électronique pour les personnes de votre organisation. Lorsqu’une stratégie de pièces jointes approuvées ATP est en place et qu’une personne concernée par cette stratégie affiche son courrier électronique dans Office 365, ses pièces jointes sont vérifiées et les actions appropriées sont prises, en fonction des stratégies de pièces jointes approuvées ATP. En fonction de la définition de vos stratégies, les utilisateurs peuvent continuer à travailler sans jamais savoir qu’ils ont reçu des fichiers malveillants.
  
Voici deux exemples de pièces jointes approuvées ATP au travail.
  
- **Exemple 1: pièce jointe de message électronique** Supposons que Lee reçoit un message électronique comportant une pièce jointe. Il n’est pas évident de savoir si cette pièce jointe est fiable ou si elle contient en réalité des programmes malveillants conçus pour voler les informations d’identification utilisateur de Lee. Dans l’organisation de Lee, un administrateur de sécurité a défini une stratégie de pièces jointes approuvées ATP il y a quelques jours. Avec la fonctionnalité pièces jointes approuvées ATP, la pièce jointe est ouverte et testée dans un environnement virtuel avant que Lee la reçoive. Si la pièce jointe est considérée comme malveillante, elle sera automatiquement supprimée. Si la pièce jointe est sécurisée, elle s’ouvre comme prévu lorsque Lee clique dessus.

- **Exemple 2: fichier dans SharePoint Online** Supposons que Jean a reçu un fichier et l’a téléchargé dans une bibliothèque dans SharePoint Online. Jean partage le lien vers le fichier avec le reste de l’équipe, sans savoir que le fichier est réellement malveillant. Heureusement, la protection avancée contre les menaces [pour SharePoint, OneDrive et Microsoft teams](atp-for-spo-odb-and-teams.md) détecte le fichier malveillant et le bloque. Quelques jours plus tard, Chris ouvre le document. Bien que Chris puisse voir le fichier, Chris ne peut pas l’ouvrir ou le partager, ce qui protège son ordinateur et d’autres personnes du fichier malveillant.

Les stratégies de pièces jointes approuvées ATP peuvent être appliquées à des personnes ou des groupes spécifiques de votre organisation ou à votre domaine entier. En outre, les stratégies de pièces jointes approuvées ATP peuvent être configurées pour utiliser les pièces jointes des espaces réservés pendant l’analyse des pièces jointes réelles. Pour en savoir plus, consultez la rubrique **[configurer des stratégies de pièces jointes approuvées ATP dans Office 365](set-up-atp-safe-attachments-policies.md)**.

> [!NOTE]
> L’analyse des pièces jointes approuvées ATP a lieu dans la région où se trouvent vos données Office 365. Pour plus d’informations sur la géographie du centre de données, voir [où se trouvent vos données?](https://products.office.com/where-is-your-data-located?geo=All) 

