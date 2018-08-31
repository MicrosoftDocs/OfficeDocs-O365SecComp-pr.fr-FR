---
title: Marquage et formation de la pertinence dans Office 365 avancée de découverte électronique
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
ms.assetid: 8576cc86-d51b-4285-b54b-67184714cc62
description: 'Découvrez les étapes nécessaires à la balise, puis avec un échantillon de formation de 40 fichiers durant la phase de formation de la pertinence d’eDiscovery Office 365 avancée.  '
ms.openlocfilehash: 90272452c8c1317957e542eba07bc43722f9c0e9
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528137"
---
# <a name="tagging-and-relevance-training-in-office-365-advanced-ediscovery"></a>Marquage et formation de la pertinence dans Office 365 avancée de découverte électronique

> [!NOTE]
> Découverte avancée nécessite un Office 365 E3 avec le module complémentaire de conformité avancée ou un abonnement E5 pour votre organisation. Si vous n’avez qu’un plan d’et essayer eDiscovery avancé, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Cette rubrique décrit la procédure de travail avec le module de formation de la pertinence de la découverte avancée. 
  
Après évaluation est terminée en découverte avancée, et vous permet d’entrer la fenêtre de partage la pertinence de la formation, un exemple de formation de 40 fichiers est placé dans l’onglet de la balise pour le marquage. 
  
## <a name="performing-relevance-training"></a>Effectue la formation de pertinence

1. Dans la **la pertinence \> balise** onglet, le volet de balisage s’affiche par défaut dans le volet de gauche et les fichiers sont affichés, une à la fois pour le marquage. 
    
    ![Volet Balise de pertinence](media/0cf19ab4-b427-4a7f-8749-0f4ed9afaf58.png)
  
    Dans l’onglet **balise** , figure le nom du fichier complet. Cela peut être le chemin d’accès, l’objet de courrier électronique, titre ou nom défini par l’utilisateur. L’ID, le chemin d’accès de fichier ou le chemin d’accès de texte peut être copié en cliquant sur le chemin du fichier. 
    
    L’onglet **balise** balisage statistiques afficher le nombre d’exemple de fichier (en haut du volet de gauche), le numéro du fichier actuellement affiché en dehors du nombre total de fichiers dans l’échantillon (partie inférieure du volet de droite) et le nombre total en cours de fichiers balisés dans l’échantillon (bas de t Il volet gauche), les modifications que vous ajoutez une balise fichiers. Cela s’applique pour n’importe quel intérêt pour marquer terminé, que ce soit dans l’évaluation, formation, rattrapage ou de Test. 
    
    Icônes indiquant l’existence des fichiers de votre famille, les balises et les commentaires sont affichés dans l’affichage du fichier dans une barre au-dessus du fichier.
    
2. Déterminer la pertinence du fichier pour le problème d’incident et la balise le fichier en utilisant le balisage des cases d’option icône ou raccourcis clavier, comme indiqué dans le tableau suivant :
    
| |
|**Option de liaison**|**Description**|**Raccourci clavier**|**Pour les problèmes plusieurs - en bloc des raccourcis clavier de balise**|
|:-----|:-----|:-----|:-----|
|R  <br/> |Pertinents  <br/> |Z  <br/> |MAJ + Z  <br/> |
|NR  <br/> |Non pertinents  <br/> |X  <br/> |MAJ + X  <br/> |
|Ignorer  <br/> |Ignorer  <br/> |C  <br/> |MAJ + A  <br/> |
   
  - Lorsqu’il existent des problèmes divers pour un fichier, après la liaison d’un problème, la sélection se déplace vers le prochain numéro (le cas échéant). 
    
  - Mots clés qui ont été définies par l’administrateur ou un gestionnaire d’incidents lors de la mise en surbrillance des mots clés (le programme d’installation de la pertinence \> mise en surbrillance des mots clés), s’affiche (dans les couleurs spécifiées) pour vous aider à identifier les fichiers appropriés lors de la liaison. Si un mot clé a un double souligné, il peut être sélectionné pour afficher une info-bulle avec la description du mot clé. 
    
    Si vous le souhaitez, dans l’onglet **balise** , cliquez sur **paramètres de balises** pour définir les options suivantes : 
    
    ![Paramètres de balise de pertinence](media/533e89fa-7eb4-409e-ab07-f5aab9296dd8.png)
  
  - **Balise en bloc**: utilisez cette option pour attribuer plusieurs problèmes pour un fichier en sélectionnant **tout** pour définir la balise pour le fichier sélectionné pour tous les problèmes (problèmes déjà balisé substitutions) ou en sélectionnant **le reste** pour appliquer la balise pour les problèmes restants non balisés. L’option sélectionnée est conservé pour tous les cas de cet utilisateur jusqu'à ce que modifié par l’utilisateur (paramètre est par utilisateur pour les cas de tous les utilisateur). 
    
  - **Balise automatique**: Activez cette case à cocher pour définir les autres problèmes liés à un fichier en tant que non pertinent après un marquage pertinent unique.
    
  - **Avance automatique**: Activez cette case à cocher pour déplacer la sélection de fichiers affichés dans le fichier suivant pour marquer le dernier ou uniquement le problème non balisé. 
    
    Les fichiers ignorés ne seront pas considérées pour la formation de la pertinence et à des fins de score de pertinence.
    
3. Comments texte libre, associés à un fichier, peuvent être visualisés et modifiés par le biais de l’option de **commentaires** dans la liste déroulante de gauche. (facultatif) 
    
4. Instructions pour le balisage peuvent être affichées en sélectionnant l’option **instructions de balisage** dans la liste déroulante de gauche. 
    
5. Une fois que vous marquer tous les fichiers dans la liste est terminé et que vous êtes prêt à calculer les résultats, cliquez sur **Calculer**. L’onglet **suivi** s’affiche. 
    
## <a name="working-with-the-sample-files-list"></a>Utilisation de la liste de fichiers d’exemple

L’exemple de liste de fichiers permet d’afficher une liste des fichiers dans un exemple de formation et d’effectuer différentes actions sur un ou plusieurs fichiers. Dans la **pertinence** \> onglet **balise** , le volet gauche **d’exemples de fichiers** affiche la liste des exemples de fichiers pour le traitement à l’évaluation, de formation, rattrapage et incohérences de processus. 
  
1. Dans la **la pertinence \> balise** , sélectionnez les fichiers d’exemple dans la liste déroulante de gauche. Les exemples de fichiers sont répertoriés dans le volet gauche. 
    
    ![Liste d’exemples de fichiers de balise de pertinence](media/fd058bdd-645a-4af1-a1eb-bff08581cb18.png)
  
2. Sélectionnez un nombre spécifique de l’échantillon ou fichier en entrant ou en sélectionnant son numéro dans les zones **exemple** ou un **fichier** . 
    
  -   - Un numéro de séquence du fichier est répertorié dans la colonne de gauche de la liste des fichiers affichés sous l’onglet **balise** . En cliquant sur l’en-tête, la commande affichée d’origine des fichiers renvoie dans leur ordre d’origine. 
    
  - Cliquez sur une ligne du fichier pour afficher son contenu dans le volet droit.
    
  - Naviguer entre les fichiers dans l’exemple en cours en utilisant les options de barre de menus inférieures. En outre, les raccourcis clavier de navigation sont disponibles :
    
    Pour naviguer vers le premier fichier dans l’exemple : Maj + Ctrl +\<
    
    Pour naviguer vers le fichier dans l’exemple précédent : MAJ +\<
    
    Pour accéder au fichier dans l’exemple suivant : MAJ +\>
    
    Pour accéder au dernier fichier dans l’exemple : Maj + Ctrl +\>
    
## <a name="see-also"></a>Voir aussi

[eDiscovery avancée Office 365](office-365-advanced-ediscovery.md)
  
[Évaluation de la présentation de la pertinence](assessment-in-relevance-in-advanced-ediscovery.md)
  
[Marquage et évaluation](tagging-and-assessment-in-advanced-ediscovery.md)
  
[Analyse de la pertinence de suivi](track-relevance-analysis-in-advanced-ediscovery.md)
  
[Selon les résultats de la sélection du conteneur](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[Test d’analyse de la pertinence](test-relevance-analysis-in-advanced-ediscovery.md)

