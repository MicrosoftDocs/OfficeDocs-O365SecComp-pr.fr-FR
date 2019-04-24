---
title: Champs de métadonnées de document dans Advanced eDiscovery (aperçu)
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
ms.openlocfilehash: b9caf390e3ee0c10a35fa12cc68fcb0638987dcb
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32251852"
---
# <a name="document-metadata-fields-in-advanced-ediscovery-preview"></a>Champs de métadonnées de document dans Advanced eDiscovery (aperçu)

Le tableau suivant répertorie les champs de métadonnées des documents dans un jeu de travail dans un cas dans Advanced eDiscovery (Preview). Le tableau indique le nom du champ de métadonnées, indique si le champ peut être recherché lors de l'exécution d'une requête dans une plage de travail, si le champ est présent lors de l'affichage des métadonnées de fichier d'un document sélectionné dans une plage de travail et si le champ est inclus lorsque les documents sont exportés. 

Le tableau suivant répertorie les champs de métadonnées des documents dans un jeu de travail dans un cas dans Advanced eDiscovery (Preview). Le tableau indique le nom du champ de métadonnées, indique si le champ peut être recherché lors de l'exécution d'une requête dans une plage de travail, si le champ est présent lors de l'affichage des métadonnées de fichier d'un document sélectionné dans une plage de travail et si le champ est inclus lorsque les documents sont exportés. 

> [!NOTE]
> Les valeurs entre parenthèses dans la colonne **rechercheable dans l'ensemble de travail** sont le nom de la propriété que vous pouvez rechercher. Les valeurs entre parenthèses dans la colonne **de métadonnées de fichier affichables** sont le nom de la propriété qui s'affiche lorsque vous affichez les métadonnées du fichier.

|**Nom de champ** </br>|**Recherche dans la plage de travail** |**Affichable dans les métadonnées de fichier** |**Exported** |
|:-------------------------- |:---------------------------------------- |:------------------------|:------------------|
|Balises case                  | Oui (balises)                                      |                         | Oui         |
|Étiquettes de conformité          |                                                 |                         | Oui         |
|Tracé transparent              |                                                 |                         | Oui         |
|ID de conteneur               |                                                 |                         | Oui         |
|Index des conversations         |                                                 |                         | Oui         |
|Custodian                  | Oui (dépositaire)                                 |   Oui (dépositaire)       | Oui         |
|Source de données                | Oui (source)                                    |   Oui (charge de travail)          | Oui         |
|Date                       | Oui (date)                                      |   Oui (date UTC)        | Oui         |
|Chemin d'accès composé Deduped      |                                                 |                         | Oui         |
|Dépositaires Deduped         |                                                 |                         | Oui         |
|ID de fichiers Deduped           |                                                 |                         | Oui         |
|Auteurs de documents                | Oui (auteur) *                                   |    Oui (auteur)         | Oui         |
|Commentaires sur le document               | Oui (commentaires)                                  |                         | Oui         |
|Société doc                |                                                 |                         | Oui         |
|Date de création du document           | Oui (createdTime) *                              |    Oui (heure de création)   | Oui         |
|Date de modification du document          | Oui (lastModifiedDate) *                         |                         | Oui         |
|Mots clés doc               |                                                 |                         | Oui         |
|Dernier enregistrement du document par          |                                                 |                         | Oui         |
|Document modifié par            |                                                 |                         | Oui         |
|Objet doc                |                                                 |  Oui (objet/titre)    | Oui         |
|Modèle de document               |                                                 |                         | Oui         |
|Titre du document                  | Oui (titre)                                     |  Oui (titre)            | Oui         |
|Version du document                |                                                 |                         | Oui         |
|Thème dominant             | Oui (dominantTheme)                             |  Oui (thème dominant)   | Oui         |
|Sous-ensemble dupliqué           |                                                 |                         | Oui         |
|Action de messagerie               |                                                 |                         | Oui         |
|Courrier CCI                  | Oui (CCI)                                       |                         | Oui         |
|Message électronique CC                   | Oui (CC)                                        |                         | Oui         |
|ID de conversation de messagerie      |                                                 |                         | Oui         |
|Date de réception du message électronique        | Oui (reçu)                                  |   Oui (reçu)        | Oui         |
|Date d'envoi du message électronique            | Oui (envoyé)                                      |   Oui (envoyé)            | Oui         |
|Le courrier électronique contient une pièce jointe       |                                                 |                         | Oui         |
|Importance de la messagerie           |                                                 |                         | Oui         |
|En-têtes Internet de messagerie     |                                                 |                         | Oui         |
|Niveau du courrier électronique                |                                                 |                         | Oui         |
|ID du message électronique           |                                                 |                         | Oui         |
|Domaines de participant de messagerie  | Oui (participantDomains)                        |                         | Oui         |
|Participants au courrier électronique         | Oui (participants)                              |                         | Oui         |
|Domaines de destinataires de messagerie    | Oui (recipientDomains)                          |                         | Oui         |
|Destinataires de courrier électronique           | Oui (destinataires)                                |                         | Oui         |
|Sécurité de messagerie             |                                                 |                         | Oui         |
|Expéditeur du courrier électronique               | Oui (expéditeur)                                    |   Oui (expéditeur)          | Oui         |
|Domaine de l'expéditeur du courrier électronique        | Oui (senderDomain)                              |                         | Oui         |
|Sensibilité du courrier électronique          |                                                 |                         | Oui         |
|Message électronique                  | Oui (emailSetId)                                |   Oui (EmailSetID)      | Oui         |
|Objet du message              | Oui (objet)                                   |   Oui (objet/titre)   | Oui         |
|Thread de messagerie               |                                                 |                         | Oui         |
|Courrier électronique à                   | Oui (à)                                        |                         | Oui         |
|Code d'erreur                 | Oui (processingStatus)                          |                         | Oui         |
|Exporter le chemin d'accès natif         |                                                 |                         | Oui         |
|Longueur du texte extrait      |                                                 |                         | Oui         |
|Chemin d'accès au texte extrait        |                                                 |                         | Oui         |
|ID de famille                  | Oui (familyId)                                  |   Oui (FamilyId)        | Oui         |
|Taille de la famille                |                                                 |                         | Oui         |
|Classe file                 | Oui (fileClass)                                 |   Oui (classe de fichiers)      | Oui         |
|ID de fichier                    | Oui (fileId)                                    |   Oui (ID)              | Oui         |
|Comporte du texte                   |                                                 |                         | Oui         |
|Type inClusif             | Oui (inclusiveType)                             |   Oui (type inClusif)  | Oui         |
|Date d'entrée modifiée        |                                                 |                         | Oui         |
|ID du fichier d'entrée              |                                                 |                         | Oui         |
|Chemin d'entrée                 |                                                 |                         | Oui         |
|Identificateur du message Internet        |                                                 |                         | Oui         |
|Est représentatif          | Oui (markAsRepresentative)                      |                         | Oui         |
|Classe de l’élément                 |                                                 |                         | Oui         |
|ID de chargement                    | Oui (loadId)                                    |                         | Oui         |
|Nom de l'emplacement              |                                                 |                         | Oui         |
|Marqué comme tableau croisé dynamique            | Oui (markAsPivot)                               |   Oui (marqué comme tableau croisé dynamique) | Oui         |
|Type de message               | Oui (messageKind)                               |                         | Oui         |
|Extension native           |                                                 |                         | Oui         |
|Nom de fichier natif           |                                                 |    Oui (nom de fichier)      | Oui         |
|MD5 natif                 |                                                 |                         | Oui         |
|SHA Native 256             |                                                 |                         | Oui         |
|Taille native                | Oui (taille)                                      |   Oui (NativeSize)     | Oui         |
|Type natif                | Oui (fileType)                                  |   Oui (type de fichier)       | Oui         |
|ND ET tri, liaison excl     |                                                 |                         | Oui         |
|ND ET Trier avec liaison incluse     |                                                 |                         | Oui         |
|ND défini                     |                                                 |                         | Oui         |
|Auteurs O365               | Oui (auteur) *                                   |   Oui (expéditeur/auteur)   | Oui         |
|O365 créé par            |                                                 |                         | Oui         |
|Date de création d'O365          | Oui (createdTime) *                              |                         | Oui         |
|Date d'Office 365 modifiée         | Oui (lastModifiedDate) *                         |   Oui (date de la dernière modification) | Oui      |
|O365 modifié par           |                                                 |                         | Oui         |
|Nœud parent                |                                                 |                         | Oui         |
|ID de tableau croisé dynamique                   | Oui (pivotId)                                   |  Oui (PivotID)          | Oui         |
|Nombre de destinataires            |                                                 |                         | Oui         |
|Numéro de ligne                 |                                                 |                         | Oui         |
|ID de l'ensemble                     |                                                 |                         | Oui         |
|Définir d'abord les inclusifs de commandes |                                                 |                         | Oui         |
|Pourcentage de similarité         |                                                 |                         | Oui         |
|Liste des thèmes                | Oui (themesList)                                | Oui (liste des thèmes)       | Oui         |
|Word count                 | Oui (wordCount)                                 |                         | Oui         |
|Score de pertinence (problème)    | Oui (relevanceScore_issueNum)                   |                         | Oui           |
|Centile en lecture (émission)    | Oui (readPercentile_issueNum)                   |                         | Oui          |
|Balise de pertinence (problème)      | Oui (relevanceTag_issueNum)                     |                         | Oui           |
|||||

  \*Pour ces champs, si des valeurs sont incorporées dans un document, la recherche les affectera en priorité; dans le cas contraire, il essaiera d'afficher la valeur à partir d'Office 365.