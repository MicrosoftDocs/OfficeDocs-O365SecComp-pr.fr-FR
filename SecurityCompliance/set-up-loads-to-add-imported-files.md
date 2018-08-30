---
title: Définissez la charge pour ajouter les fichiers importés dans Office 365 avancée de découverte électronique
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
ms.assetid: 0e0a9d04-294f-4f54-8bf1-b32d81345126
description: 'Passez en revue les étapes pour ajouter les fichiers importés au dernier chargement défini ou par lot, des fichiers avant d’effectuer la formation de la pertinence dans Office 365 avancée de découverte électronique.  '
ms.openlocfilehash: 2c986578b969b671351930fd6939a90e3a821dc2
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528625"
---
# <a name="set-up-loads-to-add-imported-files-in-office-365-advanced-ediscovery"></a>Définissez la charge pour ajouter les fichiers importés dans Office 365 avancée de découverte électronique

> [!NOTE]
> Découverte avancée nécessite un Office 365 E3 avec le module complémentaire de conformité avancée ou un abonnement E5 pour votre organisation. Si vous n’avez qu’un plan d’et essayer eDiscovery avancé, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Dans découverte avancée, une charge est un nouveau lot de fichiers ajoutés à un cas. Par défaut, une charge est définie et tous les fichiers importés sont ajoutés. Avant d’effectuer la formation de pertinence, les fichiers importés doivent être ajoutés à la charge. 
  
Prenez en compte les scénarios suivants :
  
- Nouveaux fichiers connus pour être semblable aux fichiers précédentes chargés dans la base de données de dossier ou la charge précédente des fichiers a été un jeu aléatoire à partir de la collection de fichiers. Dans ce cas, ajoutez les fichiers importés pour le chargement du fichier en cours.
    
- Nouveaux fichiers sont différents des précédents (par exemple, à partir d’une autre source), ou vous ne connaissez pas qu’ils sont similaires ou différentes charges précédente. Dans ce scénario, ajoutez les fichiers importés vers un nouveau fichier charger. Découverte avancée détecte un scénario de charge matériel, appelle un processus rattrapage, verrouille la formation de la pertinence et les calculs par lots jusqu'à ce que rattrapage terminée, la nouvelle charge est intégrée et formée. 
    
## <a name="adding-imported-files-to-the-current-load"></a>Ajout de fichiers importés à la charge actuelle

Tous les fichiers importés doivent être ajoutés à une charge de traitement d’eDiscovery avancée. Les fichiers importés sont ajoutés à la dernière charge définie. Si vous importez des fichiers supplémentaires ultérieurement, ils doivent également être ajoutés à la charge.
  
1. Dans la **la pertinence \> le programme d’installation de la pertinence** , sélectionnez **la charge**.
    
    ![Onglet Charges de configuration de pertinence](media/278aac7f-655f-462f-852a-6baa5d818768.png)
  
2. **Fichiers Include**: sélectionnez une option pour les fichiers à inclure. Par défaut, ajout de fichiers à la charge actuelle est basé sur la population « Tous les fichiers ».
    
    > [!TIP]
    > Chargez tous les fichiers réforme disponibles dans la pertinence. Si vous souhaitez charger uniquement un sous-ensemble des fichiers disponibles, voir tout d’abord cycle avec prise en charge, comme le chargement des sous-ensembles peut affecter la formation de pertinence. 
  
3. Dans la **gestion de la charge**, sélectionnez une charge.
    
4. Cliquez sur **Ajouter des fichiers**. Les fichiers sont ajoutés à la charge et un message de confirmation s’affiche. 
    
5. Cliquez sur **OK**.
    
Les fichiers peuvent maintenant être traités d’eDiscovery avancée pertinence pour les fichiers de formation.
  
## <a name="editing-a-load-name-within-a-case"></a>Modification d’un nom de la charge au sein d’un cas

Si vous modifiez le nom de la charge, il est recommandé d’utiliser un nom qui est important pour le cas.
  
1. Dans la **la pertinence \> le programme d’installation de la pertinence** , sélectionnez **la charge**.
    
2. Dans la liste de la **gestion de la charge** , sélectionnez une charge, cliquez sur l’icône **Modifier** . La fenêtre Modifier la charge est affichée. 
    
3. Entrez les modifications, puis cliquez sur **OK**.
    
## <a name="adding-imported-files-to-a-new-load"></a>Ajout de fichiers importés dans un nouveau chargement

Après avoir démarré la formation de pertinence ou par lot des calculs, vous souhaiterez peut-être importer et traiter un ensemble de fichiers supplémentaire. 
  
Au cours de peut être réduite, vous pouvez créer, balise et analyser l’ensemble de rattrapage. Découverte avancée compare son évaluation des fichiers pertinents et Non-pertinents de la charge de nouveau à celles de chargements précédents. En fonction des résultats, vous êtes invité à prendre des décisions de rattrapage, si nécessaire et confirmé eDiscovery fournit des recommandations en fonction des informations à recevoir la pertinence. 
  
Relatifs des charges et les fonctionnalités rattrapage varie comme suit : 
  
- Lorsque vous importez un nouveau fichier charger après le calcul de lot, eDiscovery avancée détermine dans quelle mesure les fichiers peuvent être classées dans une des catégories suivantes :
    
  - Similaire (homogène) : un arrondi nouvel, personnalisé de formation de la pertinence n’est pas obligatoire et la base de connaissances alloué à partir de la charge précédente peut être appliqué « comme est » à la charge de nouveau. 
    
  - Distinct (hétérogène) : un arrondi nouvel, personnalisé de formation de pertinence est nécessaire, et la base de connaissances alloué à partir de la charge précédente ne peut pas être appliqué. 
    
    Ces termes font référence au niveau de similarité de fichiers entre les charges et non au sein de la charge. 
    
- Lorsque vous importez un nouveau fichier charger au cours de formation de pertinence (avant le calcul du lot), rattrapage vous permet de continuer formation pertinence sur l’ensemble de fichiers États-Unis. Découverte avancée ne pas estimer si la charge de nouveau est similaire à ou distinct de la charge précédente. Il simplement de collecte des informations sur la nouvelle charge et permet la pertinence de la formation continue sur les anciens et les nouveaux ensembles de fichiers. 
    
- Lorsqu’il existe plusieurs problèmes en formation pertinence ainsi que les problèmes après le calcul de lot, le processus de rattrapage est effectué une fois pour tous les problèmes et les résultats sont calculées et affichées pour chaque problème.
    
> [!NOTE]
> La taille de l’échantillon rattrapage peut-être varier. Il dépend de la taille de la charge de nouveau par rapport à la charge précédente et le nombre d’échantillons effectué avant l’ajout de la charge de nouveau. L’exemple de rattrapage est généralement un ensemble de 200 à 2 000 fichiers à partir de la charge de nouveau. 
  
> [!TIP]
> Rattrapage arrête toutes les autres tâches et requiert marquer le fichier individuel et révision. Par conséquent, vous pouvez réduire une surcharge lorsque vous ajoutez des fichiers volumineux par lots. 
  
## <a name="adding-a-new-file-load-using-catch-up-and-rolling-loads"></a>Ajout d’un nouveau chargement de fichiers à l’aide de rattrapage et propagée charge

1. Dans la **la pertinence \> le programme d’installation de la pertinence** , sélectionnez **la charge**.
    
2. Sous **Gestion des charges**, cliquez sur le **+** icône pour ajouter une charge. Un message de confirmation s’affiche. 
    
3. Cliquez sur **Oui** pour continuer. La boîte de dialogue **Nouveau charger** s’affiche. 
    
    > [!NOTE]
    > Vous ne pouvez ajouter un nouveau chargement que si les actions effectuées à la charge précédente. 
  
4. Dans la boîte de dialogue **nouveau de charge** , tapez les informations de **charger le nom** et la **Description** et puis cliquez sur **OK**. Découverte avancée ajoute un nouveau chargement.
    
5. Pour importer le nouveau fichier de charge, cliquez sur **Ajouter des fichiers**. Tous les nouveaux fichiers sont ajoutés à cette charge. Une fois la découverte avancée importe les fichiers, il reconnaît le scénario de charge matériel et indique rattrapage en tant que l’étape suivante.
    
6. Cliquez sur **rattrapage** au bas de la boîte de dialogue pour exécuter le scénario. 
    
    Un seul ensemble de rattrapage, généralement contenant 200 à 2 000 fichiers à partir de la charge de nouveau, est créé pour tous les problèmes permettre de marquer le fichier simultané.
    
    Plus d’informations sont fournies sur si les charges sont similaires ou distinct, eDiscovery avancée fusionnées ou fractionnées automatiquement de la charge et informations relatives au traitement de l’étape suivante.
    
    Vous pouvez ensuite baliser des fichiers et exécuter une opération de calculer. Le balisage permet de pertinence déterminer si les charges sont similaires ou distinctes et vous permet de continuer à travailler sur le nouveau jeu de fichiers.
    
7. Une fois la révision, l’ensemble de rattrapage afficher **pertinence \> suivi** pour les résultats de rattrapage. 
    
1. Si le chargement du fichier a été ajouté au cours de formation de pertinence (ce qui signifie que le problème n’a pas encore été par le biais de calcul du lot), **la formation continuer** est l’étape suivante, quel que soit le résultat rattrapage. 
    
    Les charges précédents et nouveau sont traitées comme une charge et formation pertinence continue sur l’ensemble États-Unis. Vous sont maintenant terminées avec cette procédure et que vous pouvez continuer de formation de pertinence. 
    
2. Si la nouvelle charge a été ajoutée après le calcul de lot, passez à la procédure suivante.
    
8. Pour les charges de nouveau ajoutés après le calcul de lot, eDiscovery avancé détermine si la nouvelle charge est similaire à ou différent du précédente se charge, comme suit :
    
1. Si la charge a été trouvée pour être similaire : aucune formation pertinence supplémentaire n’est nécessaire. Le tableau de bord affiche l’étape suivante recommandée consiste à exécuter ** calcul du lot ** pour calculer des résultats de la pertinence de la charge de nouveau. Charge a été trouvée pour être similaire, afin que l’analyse de classifieur précédente peut être exécutée sur les nouveaux fichiers. 
    
2. Si la charge a été trouvée distincte : formation plus la pertinence est nécessaire et l’étape suivante consiste à la décision rattrapage. Sélectionnez une décision rattrapage comme suit :
    
    Si vous sélectionnez **charges de fusion**, avancée eDiscovery fusionne les charges précédents et nouveau pour le jeu de formation. Bien que le premier chargement est passé par le biais de calcul de lot, plus de formations est nécessaire. Continuer la formation charges précédents et nouveau ensemble. Calcul de lot puis réexécuter et les résultats de calcul de lot précédentes doivent être ignorées. Choisissez cette sélection lorsque des résultats de la pertinence de charges existantes peuvent être recalculées, par exemple, lors de la révision des charges de fichier existant n’a pas démarré.
    
    Si vous sélectionnez **charge fractionné**, continuer formation pertinence uniquement sur la charge de nouveau. Dans ce cas, scores de calcul de lot précédentes reste inchangée. Choisissez cette option lorsque existants scores de pertinence pour charges existantes ne peuvent pas être recalculées, par exemple, passer en revue les charges existant a déjà démarré. Résultats de la pertinence sont gérés séparément à partir de ce point et ne peuvent pas être fusionnées.
    
3. Cliquez sur **Continuer formation**.
    
## <a name="see-also"></a>Voir aussi

[eDiscovery avancée Office 365](office-365-advanced-ediscovery.md)
  
[Définition des problèmes et affectation des utilisateurs](define-issues-and-assign-users.md)
  
[Définition de mise en surbrillance des mots clés et avancées options](define-highlighted-keywords-and-advanced-options.md)

