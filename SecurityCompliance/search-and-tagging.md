---
title: Recherche et marquage
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 6/13/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 22f5adad-1bc0-460d-94a9-8732929f5b99
description: Dans découverte avancée, le module de recherche et de balisage vous permet de recherche, à afficher et organiser les documents dans votre cas. Ce module est actuellement en version bêta.
ms.openlocfilehash: fde887e496e9a40aa88d841053a0c66e48f04200
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528182"
---
# <a name="search-and-tagging"></a>Recherche et marquage

Dans découverte avancée, le module de recherche et de balisage vous permet de recherche, à afficher et organiser les documents dans votre cas. Ce module est actuellement en version bêta.

> [!NOTE]
> Découverte avancée nécessite un Office 365 E3 avec le module complémentaire de conformité avancée ou un abonnement E5 pour votre organisation. Si vous n’avez qu’un plan d’et essayer eDiscovery avancé, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
## <a name="search-the-documents-in-your-case"></a>Recherche les documents dans votre cas.

Une fois que vous avez traité des documents d’eDiscovery avancée et éventuellement exécuter le module d’analyse ou le module de la pertinence, vous pouvez utiliser la recherche et à l’aide de balisage pour rechercher les documents dans le cas et organiser les balises spécifique. Vous pouvez définir vos requêtes en utilisant les cartes condition fournie, ou via un langage de requête KQL comparables dans les mots clés condition carte. La syntaxe de KQL courants, tels que AND, OR, NOT et NEAR(n) sont pris en charge, ainsi que des caractère multiples caractère générique (*). Ces propriétés sont prises en charge dans le nom de propriété de langage de requête :

- caselabel : balises créé/appliquées dans la recherche et le balisage dans ce cas 
- dépositaires : dépositaires affectés dans ce cas - soumises aux limitations
- date : date pour le courrier électronique d’envoi, date pour les documents de modification
- fileid : ID de fichier dans le cas
- FileType : extension de fichier native
- fileclass : courrier électronique, document ou pièce jointe
- senderauthor : l’expéditeur pour les courriers électroniques, auteur pour les documents
- taille : taille du fichier dans la base de connaissances
- subjecttitle : objet pour les courriers électroniques, titre pour les documents
- bcc
- cc
- participants : les adresses de tous les participants dans un thread de messagerie, y compris les liens manquants de messagerie
- reçus : date de réception
- destinataires : noms des destinataires ou des adresses (à, cc, Cci) de messagerie
- expéditeur
- LastModifiedDate : dernière modification d’un document
- envoyés : date d’un message électronique d’envoi
- à
- auteur : auteur d’un message électronique
- titre : titre d’un document
- dominanttheme : thème principal d’un élément\*
- themeslist : des thèmes qui sont associés à un élément\*
- readpercentile_ [issuenum] : lire centile d’un élément à problème [issuenum]\*\*
- relevancescore_ [issuenum] : score de pertinence d’un élément à problème [issuenum]\*\*
- relevancetag_ [issuenum] : si un élément a été marqué manuellement pour la pertinence, sa balise pour [issuenum]\*\*

\*Disponible uniquement si le module de thèmes a été exécuté \* \* disponible uniquement si le module de la pertinence a été exécuté.
  
## <a name="see-also"></a>Voir aussi

[eDiscovery avancée Office 365](office-365-advanced-ediscovery.md)
  
[Évaluation de la présentation de la pertinence](assessment-in-relevance-in-advanced-ediscovery.md)
  
[Marquage et évaluation](tagging-and-assessment-in-advanced-ediscovery.md)
  
[Marquage et formation de pertinence](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[Analyse de la pertinence de suivi](track-relevance-analysis-in-advanced-ediscovery.md)
  
[Selon les résultats de la sélection du conteneur](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[Test d’analyse de la pertinence](test-relevance-analysis-in-advanced-ediscovery.md)

