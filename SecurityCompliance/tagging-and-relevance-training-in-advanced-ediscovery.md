---
title: Marquage et formation au module Pertinence dans Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 8576cc86-d51b-4285-b54b-67184714cc62
description: "Découvrez les étapes à suivre pour marquer, puis utiliser un exemple de formation de 40 fichiers pendant la phase de formation pertinence d'Office 365 Advanced eDiscovery.  "
ms.openlocfilehash: e8c9c02d72a756565f6fe59011a6788f592463eb
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30221064"
---
# <a name="tagging-and-relevance-training-in-office-365-advanced-ediscovery"></a>Marquage et formation au module Pertinence dans Office 365 Advanced eDiscovery

> [!NOTE]
> Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous [inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Cette rubrique décrit la procédure à suivre pour utiliser le module de formation avancé de la pertinence eDiscovery. 
  
Une fois l'évaluation terminée dans Advanced eDiscovery et que vous entrez l'étape de formation pertinente, un exemple de formation de 40 fichiers est placé dans l'onglet tag pour le marquage. 
  
## <a name="performing-relevance-training"></a>Formation à la pertinence

1. Dans l' **onglet \> balise de pertinence** , le volet de marquage est affiché par défaut dans le volet de gauche et les fichiers d'exemple sont affichés, un à la fois pour le marquage. 
    
    ![Volet Balise de pertinence](media/0cf19ab4-b427-4a7f-8749-0f4ed9afaf58.png)
  
    Sous l' **** onglet balise, le nom complet du fichier est affiché. Il peut s'agir du chemin d'accès, de l'objet du courrier électronique, du titre ou du nom défini par l'utilisateur. Vous pouvez copier l'ID, le chemin d'accès ou le chemin d'accès au texte en cliquant avec le bouton droit sur le chemin d'accès du fichier. 
    
    Les **** statistiques de marquage des onglets de balise indiquent le numéro d'exemple de fichier (en haut du volet de gauche), le numéro du fichier actuellement affiché en dehors du total des fichiers dans l'exemple (volet inférieur du volet droit) et le nombre total actuel de fichiers balisés dans l'exemple (en bas de t dans le volet de gauche), qui change lorsque vous balisez des fichiers. Cela s'applique à toutes les balises de pertinence réalisées, qu'il s'agisse d'évaluation, de formation, de rattrapage ou de test. 
    
    Les icônes indiquant l'existence de commentaires, de balises et de fichiers de famille sont affichés dans l'affichage des fichiers dans une barre située au-dessus du fichier.
    
2. Déterminez la pertinence du problème lié au fichier et marquez le fichier à l'aide des boutons d'option d'étiquetage ou des raccourcis clavier, comme indiqué dans le tableau suivant:
    
| |
|**Option de marquage**|**Description**|**Raccourci clavier**|**Pour plusieurs problèmes-raccourci clavier pour les balises en bloc**|
|:-----|:-----|:-----|:-----|
|R  <br/> |Y  <br/> |Z  <br/> |Maj + Z  <br/> |
|NR  <br/> |Non pertinent  <br/> |X  <br/> |Maj + X  <br/> |
|Ignoré  <br/> |Ignoré  <br/> |C  <br/> |Maj + A  <br/> |
   
  - Lorsque plusieurs problèmes existent pour un fichier, après avoir balisé un problème, la sélection se déplace vers le prochain problème (le cas échéant). 
    
  - Mots clés définis par l'administrateur ou le gestionnaire de cas lors de la mise en surbrillance des mots-clés (mise \> en surbrillance des mots-clés), s'affiche (dans les couleurs spécifiées) pour vous aider à identifier les fichiers appropriés lors du marquage. Si un mot clé comporte un double trait de soulignement, vous pouvez cliquer dessus pour afficher une info-bulle avec la description du mot-clé. 
    
    Éventuellement, sous l'onglet **balise** , cliquez sur **paramètres** des balises pour définir les options suivantes: 
    
    ![Paramètres de balise de pertinence](media/533e89fa-7eb4-409e-ab07-f5aab9296dd8.png)
  
  - **BaliSe en bloc**: utilisez cette option pour affecter plusieurs problèmes pour un fichier en sélectionnant **tout** pour définir la balise du fichier sélectionné pour tous les problèmes (remplacement des problèmes déjà marqués) ou en sélectionnant **le reste** pour appliquer la balise aux problèmes non balisés restants. L'option sélectionnée reste en vigueur pour tous les cas de cet utilisateur jusqu'à ce qu'elle soit modifiée par cet utilisateur (le paramètre est défini par utilisateur pour tous les cas de l'utilisateur). 
    
  - **BaliSe automatique**: activez cette case à cocher pour définir d'autres problèmes pour un fichier comme n'étant pas pertinents après une seule balise pertinente.
    
  - **Avance automatique**: activez cette case à cocher pour déplacer la sélection du fichier affiché vers le fichier suivant lors du marquage du dernier problème non marqué ou non marqué. 
    
    Les fichiers ignorés ne sont pas considérés comme des objectifs de formation et de notation de pertinence.
    
3. Les commentaires en texte libre, associés à un fichier, peuvent être affichés et modifiés via l'option **Commentaire** dans la liste déroulante du volet de gauche. module 
    
4. Vous pouvez afficher les instructions de marquage en sélectionnant l'option **indications de marquage** dans la liste déroulante volet de gauche. 
    
5. Une fois que vous avez terminé le marquage de tous les fichiers de la liste et que vous êtes prêt à calculer les résultats, cliquez sur **calculer**. L'onglet **suivi** est affiché. 
    
## <a name="working-with-the-sample-files-list"></a>Utilisation de la liste des exemples de fichiers

La liste exemple de fichiers vous permet d'afficher la liste des fichiers dans un exemple de formation et d'effectuer diverses actions sur un ou plusieurs fichiers. Dans l'onglet de la balise de **pertinence** \> **** , le volet de gauche **fichiers d'exemple** affiche une liste d'exemples de fichiers à traiter avec les processus d'évaluation, de formation, de rattrapage et d'incohérence. 
  
1. Dans l' **onglet \> balise de pertinence** , sélectionnez les fichiers de l'exemple dans la liste déroulante du volet de gauche. Les fichiers de l'exemple sont répertoriés dans le volet de gauche. 
    
    ![Liste d’exemples de fichiers de balise de pertinence](media/fd058bdd-645a-4af1-a1eb-bff08581cb18.png)
  
2. Sélectionnez un exemple ou un numéro de fichier spécifique en entrant ou en sélectionnant son numéro dans les zones **exemple** ou **fichier** . 
    
  -   - Un numéro de séquence de fichier est répertorié dans la colonne de gauche de la liste des **** fichiers affichés sous l'onglet balise. En cliquant sur l'en-tête, l'ordre d'origine affiché des fichiers reprend son ordre d'origine. 
    
  - Le simple clic sur une ligne de fichier affiche son contenu dans le volet de droite.
    
  - Naviguer entre les fichiers dans l'exemple actuel à l'aide des options de la barre de menus inférieure. Les raccourcis clavier de navigation sont également disponibles:
    
    Pour accéder au premier fichier de l'exemple: Maj + Ctrl +\<
    
    Pour accéder au fichier précédent dans l'exemple: Maj +\<
    
    Pour accéder au fichier suivant dans l'exemple: Maj +\>
    
    Pour accéder au dernier fichier de l'exemple: Maj + Ctrl +\>
    
## <a name="see-also"></a>Voir aussi

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[Présentation de l'évaluation en matière de pertinence](assessment-in-relevance-in-advanced-ediscovery.md)
  
[Balisage et évaluation](tagging-and-assessment-in-advanced-ediscovery.md)
  
[Analyse de la pertinence](track-relevance-analysis-in-advanced-ediscovery.md)
  
[Choix en fonction des résultats](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[Évaluation de l'analyse de pertinence](test-relevance-analysis-in-advanced-ediscovery.md)

