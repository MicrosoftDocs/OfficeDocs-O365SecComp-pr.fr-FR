---
title: Exporter des documents à partir d’un ensemble de révision
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: ea9db6d95b003b5a741ae8a235fc5f06087f87d6
ms.sourcegitcommit: 4ce350f8f3eb597587945a8ac9b33e9793440c64
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/01/2019
ms.locfileid: "33527159"
---
# <a name="export-documents-from-a-review-set"></a>Exporter des documents à partir d’un ensemble de révision

L’exportation de contenu à partir d’un jeu de révision peut être effectuée à l’aide de trois méthodes différentes:

## <a name="download"></a>Téléchargement

Le téléchargement offre un moyen simple de télécharger du contenu à partir d’un jeu de révision au format natif. Il exploite les fonctionnalités de transfert de données du navigateur, de sorte qu’une invite de navigateur s’affiche une fois que le téléchargement est prêt. Les fichiers téléchargés à l’aide de cette méthode seront Zippés dans un fichier conteneur et seront des fichiers au niveau de l’élément. Cela signifie que si vous sélectionnez une pièce jointe, vous recevrez automatiquement le courrier électronique avec la pièce jointe incluse. De même, si vous sélectionnez une feuille de calcul Excel incorporée dans un document Word, vous recevrez le document Word avec la feuille de calcul Excel incorporée. Les éléments téléchargés conservent la dernière date de modification pouvant être affichée en tant que propriété de fichier.

Pour télécharger du contenu à partir d’un jeu de révision, commencez par sélectionner les fichiers que vous souhaitez télécharger, puis sélectionnez «Télécharger» sous le menu actions.

![Capture d’écran d’une description d’ordinateur générée automatiquement](../media/eDiscoDownload.png)

## <a name="export"></a>Exporter

Exporter permet aux utilisateurs de personnaliser le contenu qui est inclus dans le package de téléchargement. Il fournit une page de configuration avec les paramètres suivants:

### <a name="metadata-file"></a>Fichier de métadonnées

> Cela peut être considéré comme votre «fichier de chargement» qui contient les métadonnées associées aux fichiers que vous avez exportés. Pour obtenir la liste des champs disponibles dans le fichier de métadonnées, consultez la rubrique \[Link\]. Ce fichier peut généralement être ingéré par 3<sup></sup> outils tiers en aval.

### <a name="tag-data"></a>Données de balise

> Ce contenu est ajouté en tant que champs dans le fichier de métadonnées. Elle contient toutes les informations de balise appliquées dans les ensembles de révision.

### <a name="text-files"></a>Fichiers texte

> Des fichiers texte peuvent être générés pour chaque fichier exporté à partir d’un ensemble de révision. Ces fichiers sont souvent requis par les partenaires de services dans le cadre de l’ingestion<sup></sup> de données dans 3 outils tiers en aval.

### <a name="redacted-files"></a>Fichiers biffés

> Si des fichiers PDF biffés sont générés lors de la révision, ces fichiers sont disponibles lors de l’exportation. Les utilisateurs peuvent décider s’il convient d’exporter les fichiers natifs uniquement ou de remplacer les fichiers natifs dont le Redactions avec le fichier PDF est gravé.

### <a name="export-location"></a>Emplacement de l’exportation

> Le contenu exporté est remis à un objet BLOB Azure fourni par Microsoft ou le BLOB d’un client peut être utilisé si les détails sont fournis lors de l’exportation.

## <a name="export-structure"></a>Structure d’exportation

Lorsque le contenu est exporté à partir d’un ensemble de révision, le contenu est organisé dans la structure suivante.

  - Dossier racine – ID de téléchargement
    
      - Export\_load\_file. csv = fichier de métadonnées
    
      - Summary. txt = un fichier résumé avec les statistiques d’exportation
    
      - Fichiers\_d’entrée\_ou natifs = contient tous les fichiers natifs
    
      - Fichiers\_d’erreur = contient les fichiers d’erreur inclus dans l’exportation.
        
          - ExtractionError: CSV qui contient les métadonnées de fichiers disponibles qui n’ont pas été correctement extraites des fichiers parents
        
          - ProcessingError – contenu avec des erreurs de traitement. Ce contenu est de niveau élément: si une pièce jointe a rencontré une erreur de traitement, le courrier électronique qui contient la pièce jointe est inclus dans ce dossier.
    
      - Fichiers\_texte\_extraits = contient tous les fichiers texte extraits générés lors du traitement.

## <a name="review-set"></a>jeu de révision

Le contenu peut être ajouté à un autre ensemble de révision.