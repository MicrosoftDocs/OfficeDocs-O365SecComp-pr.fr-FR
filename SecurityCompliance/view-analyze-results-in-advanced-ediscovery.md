---
title: Afficher les résultats d’analyse dans Office 365 avancée de découverte électronique
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 5974f3c2-89fe-4c5f-ac7b-57f214437f7e
description: 'Comprendre où afficher les résultats du processus d’analyse dans Office 365 avancée eDiscovery, y compris les définitions des options de la tâche affichée.  '
ms.openlocfilehash: 8f1de53e5548c8721f8fbfdb83374edb18379114
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528488"
---
# <a name="view-analyze-results-in-office-365-advanced-ediscovery"></a>Afficher les résultats d’analyse dans Office 365 avancée de découverte électronique

> [!NOTE]
> Découverte avancée nécessite un Office 365 E3 avec le module complémentaire de conformité avancée ou un abonnement E5 pour votre organisation. Si vous n’avez qu’un plan d’et essayer eDiscovery avancé, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Dans découverte avancée, progression et les résultats pour le processus d’analyse peuvent être affichés dans une variété d’affiche comme indiqué ci-dessous.
  
## <a name="view-analyze-task-status"></a>Afficher l’état de tâche d’analyse

Dans **Prepare \> analyse \> résultats \> état de la tâche**, l’état est affiché pendant et après l’exécution de processus d’analyse. 
  
![Analyser l’état des tâches](media/d0372978-ce08-4f4e-a1fc-aa918ae44364.png)
  
Les tâches affichées peuvent varier selon les options sélectionnées. 
  
- **ND/ET : le programme d’installation**: prépare pour l’exécution, par exemple, définit les paramètres d’exécution et cas.
    
- **ND/ET : calcul ND**: l’analyse des processus près de copie des fichiers.
    
- **ND/ET : calcul ET**: analyse des effectue un Thread de messagerie sur l’ensemble de messagerie entière.
    
- **ND/ET : tableaux croisés dynamiques et similitudes**: effectue le tableau croisé dynamique et traitement des fichiers similarité.
    
- **ND/ET : mise à jour des métadonnées**: finalise les nouvelles données recueillies sur les fichiers dans la base de données.
    
- **Thèmes : calcul des thèmes**: exécute l’analyse des thèmes. (Affiché uniquement si sélectionné).
    
- **État de la tâche**: cette ligne est affichée après la fin d’une tâche. Lors de l’exécutant des tâches, la durée d’exécution s’affiche.
    
> [!NOTE]
> Les résultats d’analyse de proximité des doublons et les Threads de courrier électronique (ND et ED) s’applique au nombre de documents à traiter. Il n’inclut pas les fichiers en double exactes. 
  
## <a name="view-near-duplicates-and-email-threads-status"></a>Afficher l’état près de doublons et les Threads de courrier électronique

Les résultats de la population **cible** affichent le nombre de documents, messages électroniques, pièces jointes et les erreurs dans la population cible. 
  
Les résultats de **Documents** affichent le nombre de tableaux croisés dynamiques, près de doublons uniques et les fichiers en double exactes. 
  
Les **messages électroniques** de résultats affichent le nombre d’inclus et inclusif moins uniques copies (inclus) et le reste des messages électroniques. Les différents types de résultats de la messagerie sont les suivants : 
  
- **Comprises**: un message électronique (inclus) est le nœud de fin dans un thread de messagerie et contient tous les l’historique de ce thread. Par conséquent, le réviseur peut se concentrer en toute sécurité sur le courrier électronique (inclus), sans avoir besoin de lire les messages précédents dans le thread. 
    
- **Comprises moins**: un message électronique inclus est désigné comme moins inclus s’il y a au moins une autre les pièces jointes associées parents du message (inclus). Dans ce contexte, le terme que parent est utilisé pour les messages vers le haut situés sur le thread de messagerie ou des conversations inclus dans l’e-mail spécifique (inclus). Un réviseur peut utiliser le moins indication comme un signal que bien qu’il ne soit pas nécessaire consulter le contenu des parents messagerie inclus, il peut être utile de consulter les pièces jointes associées les parents du chemin d’accès inclus inclus. 
    
- **Copie (inclus)**: un message électronique (inclus) est désigné comme copie inclus s’il s’agit de la copie d’un autre message marqué comme inclus ou inclus moins. En d’autres termes, ce message a le même objet et corps en tant qu’un autre message inclus et, en tant que telles, CO-réside dans le même nœud. Inclus copier des messages contenant le même contenu, ils peuvent généralement être ignorés dans le processus de révision. 
    
- **Le reste**: cela indique le courrier électronique qui ne contient pas de contenu unique et par conséquent, ne peuvent être classées dans une des trois catégories précédentes. Ces messages électroniques n’avez pas besoin être révisé. Si un message contient une pièce jointe qui ne figure pas dans un message électronique inclus ultérieurement, la pièce jointe devront être révisé. Cela est indiqué par l’existence d’un inclus moins de messagerie dans le thread.
    
Les résultats de **pièces jointes** affichent le nombre de pièces jointes, en fonction de ce type de manière unique et les doublons. 
  
![Doublons à proximité et Threads de messagerie](media/54491303-0ee3-4739-b42e-d1ee486842fd.png)
  
## <a name="see-also"></a>Voir aussi

[eDiscovery avancée Office 365](office-365-advanced-ediscovery.md)
  
[Présentation de similarité de document](understand-document-similarity-in-advanced-ediscovery.md)
  
[Définition des options d’analyse](set-analyze-options-in-advanced-ediscovery.md)
  
[Ignorer le texte du paramètre](set-ignore-text-in-advanced-ediscovery.md)
  
[Analyse de la configuration des paramètres avancés](view-analyze-results-in-advanced-ediscovery.md)

