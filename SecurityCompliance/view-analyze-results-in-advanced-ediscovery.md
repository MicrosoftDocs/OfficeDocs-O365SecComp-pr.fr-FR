---
title: Afficher les résultats de l’analyse dans Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 5974f3c2-89fe-4c5f-ac7b-57f214437f7e
description: 'Comprendre où afficher les résultats du processus d’analyse dans Office 365 Advanced eDiscovery, y compris les définitions des options de tâche affichées.  '
ms.openlocfilehash: 092daa506316b5eb1ef1f5c466055b29e350dc18
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34157856"
---
# <a name="view-analyze-results-in-office-365-advanced-ediscovery"></a>Afficher les résultats de l’analyse dans Office 365 Advanced eDiscovery

> [!NOTE]
> Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous [inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Dans Advanced eDiscovery, la progression et les résultats du processus d’analyse peuvent être affichés dans un grand nombre d’écrans, comme décrit ci-dessous.
  
## <a name="view-analyze-task-status"></a>Afficher l’état de la tâche d’analyse

Dans **préparer \> l' \> analyse \> des résultats**de la tâche, l’État est affiché pendant et après l’exécution de l’analyse. 
  
![Analyser l’état des tâches](media/d0372978-ce08-4f4e-a1fc-aa918ae44364.png)
  
Les tâches affichées peuvent varier en fonction des options sélectionnées. 
  
- **ND/et: configuration**: prépare l’exécution, par exemple, définit les paramètres Run et case.
    
- **ND/tout: calcul de ND**: traite les analyses de fichiers presque en double.
    
- **ND/et: et calcul**: effectue une analyse des threads de messagerie sur l’ensemble du message.
    
- **ND/et: tableaux croisés dynamiques et similitudes**: effectue un traitement de type tableau croisé dynamique et similarité des fichiers.
    
- **ND/et: mise à jour**des métadonnées: finalise les nouvelles données collectées sur les fichiers de la base de données.
    
- **Themes: calculation des thèmes**: exécute l’analyse des thèmes. (Affiché uniquement s’il est sélectionné.)
    
- **État**de la tâche: cette ligne s’affiche une fois la tâche terminée. Pendant l’exécution des tâches, la durée de l’exécution s’affiche.
    
> [!NOTE]
> Les résultats d’analyse des doublons et des threads de messagerie (ND et ED) s’appliquent au nombre de documents à traiter. Il n’inclut pas les fichiers en double exact. 
  
## <a name="view-near-duplicates-and-email-threads-status"></a>Afficher l’état des doublons et des threads de messagerie

Les résultats de la population **cible** affichent le nombre de documents, d’e-mails, de pièces jointes et d’erreurs dans la population cible. 
  
Les résultats des **documents** affichent le nombre de tableaux croisés dynamiques, de doublons uniques et de fichiers en double exact. 
  
Les résultats des **courriers électroniques** affichent le nombre de copies inclusives, inclusives et non incluses, ainsi que le reste des messages électroniques. Les différents types de résultats de messagerie sont les suivants: 
  
- **Inclus**: un message électronique Inclusive est le nœud de terminaison dans un fil de messagerie et contient l’historique précédent de ce thread. Par conséquent, le réviseur peut se concentrer en toute sécurité sur le courrier inclusif, sans avoir à lire les messages précédents dans le fil de discussion. 
    
- **Moins inclusive**: un message électronique inclusif est désigné sous la forme non inclusive, moins s’il y a une ou plusieurs pièces jointes différentes associées aux parents du message inclusif. Dans ce contexte, le terme parent est utilisé pour les messages situés vers le haut sur le thread de courrier électronique ou les conversations incluses dans ce message électronique inclus spécifique. Un réviseur peut utiliser l’indication moins inclusive comme un signal qui, bien qu’il ne soit pas nécessaire de revoir le contenu des parents du courrier électronique inclus, il peut être utile de vérifier les pièces jointes associées aux parents de chemin d’accès inclusifs. 
    
- **Copie inclusive**: un message électronique inclusif est désigné comme copie inclusive s’il s’agit de la copie d’un autre message marqué comme étant inclusive ou inclusive. En d’autres termes, ce message a le même objet et le même corps qu’un autre message inclusif et, en tant que tel, réside dans le même nœud. Étant donné que les messages de copie inclusive contiennent le même contenu, ils peuvent généralement être ignorés lors du processus de révision. 
    
- **Le reste**: indique qu’il s’agit d’un courrier électronique qui ne contient pas de contenu unique et, par conséquent, qu’il n’est pas inclus dans les trois catégories précédentes. Ces messages électroniques n’ont pas besoin d’être vérifiés. Si un message contient une pièce jointe qui ne se trouve pas dans un message électronique plus inclusive, il se peut que la pièce jointe doive être révisée. Cela est indiqué par l’existence d’un courrier inclusif moins le message dans le fil de discussion.
    
Les résultats des **pièces jointes** affichent le nombre de pièces jointes, en fonction de ce type comme uniques et des doublons. 
  
![Doublons à proximité et Threads de messagerie](media/54491303-0ee3-4739-b42e-d1ee486842fd.png)
  
## <a name="see-also"></a>Voir aussi

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[Présentation de la similarité des documents](understand-document-similarity-in-advanced-ediscovery.md)
  
[Définition des options d’analyse](set-analyze-options-in-advanced-ediscovery.md)
  
[Définition d’un texte ignoré](set-ignore-text-in-advanced-ediscovery.md)
  
[Définition des paramètres avancés d’analyse](view-analyze-results-in-advanced-ediscovery.md)

