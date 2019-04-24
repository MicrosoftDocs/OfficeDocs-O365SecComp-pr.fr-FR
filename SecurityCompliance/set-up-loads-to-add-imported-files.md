---
title: Configurer les charges pour ajouter des fichiers importés dans Office 365 Advanced eDiscovery
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
ms.assetid: 0e0a9d04-294f-4f54-8bf1-b32d81345126
description: "Passez en revue les étapes nécessaires pour ajouter des fichiers importés à la dernière charge ou un lot de fichiers défini avant d'effectuer une formation pertinente dans Office 365 Advanced eDiscovery.  "
ms.openlocfilehash: 8c5101628b468719f8aa4f81a4c73cbbb226105f
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32260736"
---
# <a name="set-up-loads-to-add-imported-files-in-office-365-advanced-ediscovery"></a>Configurer les charges pour ajouter des fichiers importés dans Office 365 Advanced eDiscovery

> [!NOTE]
> Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous [inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Dans Advanced eDiscovery, une charge est un nouveau lot de fichiers ajouté à un cas. Par défaut, une charge est définie et tous les fichiers importés sont ajoutés à celle-ci. Avant d'effectuer une formation pertinente, les fichiers importés doivent être ajoutés au chargement. 
  
Plusieurs scénarios sont envisageables :
  
- Les nouveaux fichiers sont semblables aux fichiers précédents chargés dans la base de données de cas, ou le chargement de fichiers précédent était un jeu aléatoire à partir de la collection de fichiers. Dans ce cas, ajoutez les fichiers importés au chargement du fichier en cours.
    
- Les nouveaux fichiers sont différents des fichiers précédents (par exemple, à partir d'une autre source) ou vous n'avez pas connaissance préalable qu'ils sont similaires ou différents des charges précédentes. Dans ce scénario, ajoutez les fichiers importés à un nouveau chargement de fichier. Advanced eDiscovery reconnaît qu'il s'agit d'un scénario de charge propagée, appelle un processus de rattrapage, verrouille la formation à la pertinence et calcule les lots jusqu'à ce que la rattrapage soit terminée, et la nouvelle charge est intégrée et exercée. 
    
## <a name="adding-imported-files-to-the-current-load"></a>Ajout de fichiers importés à la charge actuelle

Tous les fichiers importés doivent être ajoutés à une charge pour être traités dans Advanced eDiscovery. Les fichiers imPortés sont ajoutés au dernier chargement défini. Si vous importez des fichiers supplémentaires ultérieurement, ceux-ci doivent également être ajoutés au chargement.
  
1. Dans l' ** \> onglet Configuration** de pertinence de pertinence, sélectionnez **charges**.
    
    ![Onglet Charges de configuration de pertinence](media/278aac7f-655f-462f-852a-6baa5d818768.png)
  
2. **Fichiers include**: sélectionnez une option pour les fichiers à inclure. Par défaut, l'ajout de fichiers à la charge actuelle est basé sur le remplissage «tous les fichiers».
    
    > [!TIP]
    > Chargez tous les fichiers de Culling disponibles en toute pertinence. Si vous envisagez de ne charger qu'un sous-ensemble des fichiers disponibles, consultez d'abord la prise en charge, car le chargement de sous-ensembles peut affecter la formation à la pertinence. 
  
3. Dans la gestion de la **charge**, sélectionnez un chargement.
    
4. Cliquez sur **Ajouter des fichiers**. Les fichiers sont ajoutés au chargement et un message de confirmation s'affiche. 
    
5. Cliquez sur **OK**.
    
Les fichiers peuvent désormais être traités dans l'intérêt de la découverte électronique avancée pour l'apprentissage des fichiers.
  
## <a name="editing-a-load-name-within-a-case"></a>Modification d'un nom de charge dans un cas

Si vous modifiez le nom de la charge, il est recommandé d'utiliser un nom qui est significatif pour le cas.
  
1. Dans l' ** \> onglet Configuration** de pertinence de pertinence, sélectionnez **charges**.
    
2. Dans la liste **charges de gestion** , sélectionnez une charge, puis cliquez sur l'icône **modifier** . La fenêtre Modifier la charge s'affiche. 
    
3. Entrez les modifications, puis cliquez sur **OK**.
    
## <a name="adding-imported-files-to-a-new-load"></a>Ajout de fichiers importés à une nouvelle charge

Après avoir commencé la formation pertinente ou effectué un calcul par lot, vous souhaiterez peut-être importer et traiter un ensemble de fichiers supplémentaire. 
  
Lors de l'interCeption, vous pouvez créer, marquer et analyser l'ensemble de rattrapage. Advanced eDiscovery compare son évaluation des fichiers pertinents et non pertinents dans le nouveau chargement à ceux des chargements précédents. En fonction des résultats, vous êtes invité à prendre des décisions de rattrapage, si nécessaire, et Advanced eDiscovery fournit des recommandations basées sur les informations de pertinence à recevoir. 
  
Les charges de roulement et les fonctionnalités de rattrapage varient comme suit: 
  
- Lorsque vous importez une nouvelle charge de fichier après le calcul par lot, Advanced eDiscovery détermine dans quelle mesure les fichiers appartiennent à l'une des catégories suivantes:
    
  - Semblable (homogène): une formation de type nouvelle de pertinence personnalisée n'est pas requise et les connaissances allouées à partir de la charge précédente peuvent être appliquées «en l'aspect» à la nouvelle charge. 
    
  - Distinct (hétérogène): une formation de série de pertinence personnalisée est requise et les connaissances allouées à partir de la charge précédente ne peuvent pas être appliquées. 
    
    Ces termes font référence au niveau de similarité des fichiers entre les charges et non dans les charges. 
    
- Lors de l'importation d'une nouvelle charge de fichier lors de l'apprentissage de pertinence (avant le calcul par lot), l'interCeption vous permet de continuer la formation pertinente sur le jeu de fichiers-Unis. Advanced eDiscovery n'évalue pas si la nouvelle charge est similaire ou différente de la charge précédente. Il collecte simplement des informations sur la nouvelle charge et active une formation pertinente pour continuer sur les nouveaux et les derniers ensembles de fichiers. 
    
- Lorsqu'il existe plusieurs problèmes de formation pertinente, ainsi que des problèmes après le calcul par lot, le processus de rattrapage est effectué une fois pour tous les problèmes, et les résultats sont calculés et affichés pour chaque problème.
    
> [!NOTE]
> La taille de l'exemple de rattrapage peut varier. Cela dépend de la taille de la nouvelle charge par rapport aux charges précédentes et du nombre d'échantillons terminés avant l'ajout de la nouvelle charge. L'exemple de rattrapage est généralement un ensemble de 200 à 2 000 fichiers à partir de la nouvelle charge. 
  
> [!TIP]
> Rattrapage arrête toutes les autres tâches et nécessite une balise et une révision de fichier individuelles. Par conséquent, vous pouvez réduire la charge liée à l'ajout de nouveaux fichiers dans des lots volumineux. 
  
## <a name="adding-a-new-file-load-using-catch-up-and-rolling-loads"></a>Ajout d'une nouvelle charge de fichier à l'aide de charges de rattrapage et de laminage

1. Dans l' ** \> onglet Configuration** de pertinence de pertinence, sélectionnez **charges**.
    
2. Sous **chargez la gestion**, **+** cliquez sur l'icône pour ajouter une charge. Un message de confirmation s'affiche. 
    
3. Cliquez sur **Oui** pour continuer. La boîte de dialogue **Ajouter un nouveau chargement** s'affiche. 
    
    > [!NOTE]
    > Vous pouvez ajouter une nouvelle charge uniquement si les actions ont été effectuées au chargement précédent. 
  
4. Dans la boîte de dialogue **Ajouter un nouveau chargement** , tapez les informations dans **charger le nom** et la **Description** , puis cliquez sur **OK**. Advanced eDiscovery ajoute une nouvelle charge.
    
5. Pour importer le nouveau fichier de chargement, cliquez sur **Ajouter des fichiers**. Tous les nouveaux fichiers sont ajoutés à cette charge. Une fois que Advanced eDiscovery importe les fichiers, il reconnaît le scénario de charge propagée et indique qu'il s'agit de l'étape suivante.
    
6. Cliquez **** sur rattraper en bas de la boîte de dialogue pour exécuter le scénario. 
    
    Un seul jeu de rattrapage, contenant généralement 200 à 2 000 fichiers à partir de la nouvelle charge, est créé pour tous les problèmes afin d'autoriser la balise de fichier simultanée.
    
    Des informations détaillées précisent si les charges sont similaires ou distinctes, si Advanced eDiscovery a fusionné ou fractionné le chargement automatique, ainsi que des informations sur le traitement à l'étape suivante.
    
    Vous pouvez ensuite baliser les fichiers et exécuter une opération Calculate. Le balisage permet de déterminer si les charges sont similaires ou distinctes et vous permet de continuer à travailler sur le nouveau jeu de fichiers.
    
7. Une fois le jeu de rattrapage révisé, affichez le **suivi de pertinence \> ** pour les résultats de rattrapage. 
    
1. Si le nouveau chargement de fichier a été ajouté au cours de la formation à la pertinence (ce qui signifie que le problème n'a pas encore été effectué par le calcul par lot), poursuivez la **formation** à l'étape suivante, quels que soient les résultats de rattrapage. 
    
    Les charges nouvelles et précédentes sont traitées en une seule charge et une formation pertinente se poursuit sur l'ensemble américain. Vous avez maintenant terminé cette procédure et pouvez continuer la formation pertinente. 
    
2. Si le nouveau chargement a été ajouté après le calcul par lot, procédez comme suit.
    
8. Pour les nouvelles charges ajoutées après le calcul par lot, Advanced eDiscovery détermine si la nouvelle charge est similaire ou différente des charges précédentes, comme suit:
    
1. Si les charges étaient similaires: aucune formation sur la pertinence supplémentaire n'est nécessaire. Le tableau de bord affiche l'étape suivante recommandée: exécuter * * calcul de lot * * à nouveau pour calculer les scores de pertinence pour le nouveau chargement. Les charges ont été similaires, de sorte que l'analyse de classifieur précédente peut être exécutée sur les nouveaux fichiers. 
    
2. Si les charges ont été jugées distinctes: une formation plus pertinente est nécessaire et l'étape suivante est la décision de rattrapage. Sélectionnez une décision de rattrapage comme suit:
    
    Si vous sélectionnez **fusionner les charges**, Advanced eDiscovery fusions Previous et New loads pour le jeu de formation. Bien que la première charge passe par le calcul par lot, une formation supplémentaire est nécessaire. Poursuivez l'apprentissage des nouvelles et des versions précédentes. Le calcul du lot s'exécutera de nouveau et les notes de calcul du lot précédent doivent être ignorées. Choisissez cette sélection lorsque les scores de pertinence pour les charges existantes peuvent être recalculés, par exemple, lorsque la révision des chargements de fichiers existants n'a pas commencé.
    
    Si vous sélectionnez **fractionner les charges**, ne poursuivez la formation à pertinence que sur le nouveau chargement. Dans ce cas, les scores de calcul du lot précédent resteront tels quels. Choisissez cette option lorsque les scores de pertinence existants pour les charges existantes ne peuvent pas être recalculés, par exemple, si la révision des charges existantes a déjà commencé. Les scores de pertinence sont gérés séparément à ce stade et ne peuvent pas être fusionnés.
    
3. Cliquez sur **Continuer la formation**.
    
## <a name="see-also"></a>Voir aussi

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[Définition des sujets et affectation des utilisateurs](define-issues-and-assign-users.md)
  
[Définition des mots clés surlignés et des options avancées](define-highlighted-keywords-and-advanced-options.md)

