---
title: Exporter les résultats dans Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a9951a07-10b3-48cb-b37a-0ffaa24931ad
description: 'Découvrez comment définir des options pour l’exportation des résultats à partir d’Office 365 Advanced eDiscovery, notamment la procédure de spécification des paramètres pour un lot d’exportation. '
ms.openlocfilehash: ad11ac742f3157811523164c7e4d063e1d101343
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34152926"
---
# <a name="export-results-in-office-365-advanced-ediscovery"></a>Exporter les résultats dans Office 365 Advanced eDiscovery

> [!NOTE]
> Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous [inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Cette rubrique décrit les options avancées de configuration de l’exportation eDiscovery.
  
 **Dans cette rubrique:**
  
- [Définition des lots d’exportation et des sessions](export-results-in-advanced-ediscovery.md#BK_Define)
    
- [Exportations incrémentielles et supplémentaires](export-results-in-advanced-ediscovery.md#BK_IncrementalReports)
    
- [Configurer les paramètres d’exportation par lot](export-results-in-advanced-ediscovery.md#BK_SetUpExport)
    
- [Exporter les fichiers de sortie de rapport](export-results-in-advanced-ediscovery.md#BK_ExportOutputFIles)
    
## <a name="defining-export-batches-and-sessions"></a>Définition des lots d’exportation et des sessions
<a name="BK_Define"> </a>

Un lot d’exportation permet le traitement de l’exportation à l’aide d’un ensemble de paramètres définis. Advanced eDiscovery vous permet de définir des lots pour personnaliser chaque exportation.
  
Les paramètres sont définis par lot d’exportation. Un lot nommé «export batch 01» est créé par défaut pour le premier lot d’un cas. Vous pouvez également modifier le nom et la description du lot.
  
Une session d’exportation est une exécution d’une exportation eDiscovery avancée dans un lot d’exportation.
  
## <a name="incremental-and-additional-exports"></a>Exportations incrémentielles et supplémentaires
<a name="BK_IncrementalReports"> </a>

Vous pouvez exécuter plusieurs sessions d’exportation dans un lot d’exportation afin de garantir des résultats cohérents en fonction des mêmes paramètres et modèle d’exportation. Pour chaque session au sein d’un lot, vous pouvez exporter Analytics pour les données de cas nouvellement traitées et traiter chaque «de manière incrémentielle».
  
Pour exporter à l’aide d’un autre ensemble de paramètres, vous devez d’abord créer un nouveau lot. La première session du nouveau lot génère des résultats pour les fichiers traités dans le cas où, si ces fichiers ont été importés et traités sur une ou plusieurs importations. Chaque lot recalcule les tableaux croisés dynamiques, similarités, inclusifs, etc. Les sessions utilisent les paramètres définis pour le lot et ne recalculent pas les tableaux croisés dynamiques, la similarité, les inclusives, etc. pour chaque exécution de session.
  
Par exemple, supposons qu’un cas a été importé et que ses données ont été analysées. Pour récupérer les résultats des threads de proximité et des doublons de données pour les données incrémentielles, cliquez sur **créer une session d’exportation** dans le même lot utilisé pour exporter les données. 
  
## <a name="set-up-batch-export-parameters"></a>Configurer les paramètres d’exportation par lot
<a name="BK_SetUpExport"> </a>

L’outil d’exportation de découverte électronique est utilisé pour exporter les résultats de recherche d’Advanced eDiscovery vers votre ordinateur local. Pour augmenter le débit de transfert de données et accélérer le processus d’exportation, vous pouvez configurer un paramètre de Registre Windows sur l’ordinateur que vous utilisez pour exporter les résultats de la recherche. Si vous souhaitez augmenter la vitesse de téléchargement, configurez le paramètre de Registre avant de configurer les paramètres d’exportation. Pour plus d’informations, consultez [la rubrique augmentation de la vitesse de téléchargement lors de l’exportation des résultats de recherche eDiscovery à partir d’Office 365](increase-download-speeds-when-exporting-ediscovery-results.md).
  
1. Dans Advanced eDiscovery, sélectionnez un cas et cliquez sur **Exporter** \> la **configuration**.
    
    - Dans la liste **Exporter le lot** , sélectionnez le nom du lot ou exportez les résultats vers l’export lot 01 (par défaut). 
    
    - Pour exporter les résultats pour les nouveaux fichiers que vous avez ajoutés à un cas existant, continuez avec votre lot actuel. Pour créer une session dans le lot, sélectionnez le même numéro de lot, puis cliquez sur **créer une session d’exportation** vous pouvez utiliser cette option pour exporter les mêmes paramètres que le lot précédent, de manière incrémentielle. 
    
    - Pour exporter vers un nouveau lot, cliquez sur **Ajouter** ![une](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png)icône Ajouter et entrez un nouveau nom dans le **champ nom du lot** (ou acceptez la valeur par défaut) et une description dans **Description du lot**. Cliquez sur **OK**.
    
    - Pour modifier un nom de lot ou une description, sélectionnez le nom dans **Exporter le lot**, cliquez](media/3d613660-7602-4df2-bdb9-14e9ca2f9cf2.png)sur **modifier** ![l’icône d’édition, puis modifiez les champs.
    
      > [!NOTE]
      > Une fois que vous avez exécuté des sessions pour un lot d’exportation, il est impossible de les supprimer. De plus, seuls certains paramètres peuvent être modifiés une fois la première session exécutée. 
  
    - Pour créer un lot d’exportation en double, sélectionnez dupliquer un **lot** ![d’exportation en](media/3f6d5f59-e842-4946-a493-473528af0119.jpg) double créez un lot d’exportation en double et entrez un nom et une description pour le lot dupliqué dans le panneau. 
    
    - Pour supprimer un lot d’exportation, sélectionnez **supprimer** ![supprimer une icône](media/92a9f8e0-d469-48da-addb-69365e7ffb6f.jpg)exporter un lot.
    
    - Pour afficher l’historique d’un lot, sélectionnez **** ![l’icône](media/a80cc320-d96c-4d91-8884-75fe2cb147e2.jpg)historique du lot-afficher l’historique.
    
2. Sous **remplissage**, sélectionnez **inclure uniquement les fichiers au-dessus du score** de découpage de pertinence et/ou affiner l' **exportation de lot** si vous souhaitez affiner les paramètres de votre lot d’exportation. 
    
3. Si vous sélectionnez **inclure uniquement les fichiers au-dessus du score**de découpage de pertinence, le **problème** est alors activé. Si le score de pertinence du fichier est supérieur au score de découpage du problème sélectionné, le fichier est exporté sauf s’il est exclu par le filtre «pour révision». 
  
    Si vous sélectionnez **affiner l’exportation**, les cases d’option **de déduplication** et de filtrage par «pour révision» sont activées. Si vous choisissez **** la déduplication, les fichiers dupliqués sont filtrés en fonction de la stratégie définie [niveau de cas (par défaut): à partir de chaque ensemble de fichiers en double dans le cas entier, tous les fichiers sauf un seront de duped. Niveau des dépositaires: à partir de chaque ensemble de fichiers en double du même dépositaire, tous les fichiers sauf un seront de duped.] La sortie d’exportation contient un enregistrement de tous les fichiers en double. Si vous choisissez **Filtrer par champ de révision** , sélectionnez **modifier sous métadonnées** pour entrer les paramètres de champ **«pour révision»** . Sélectionnez **inclure les fichiers d’entrée** pour inclure les fichiers sources dans le contenu du package. Vous pouvez désactiver ce paramètre pour accélérer le processus d’exportation. Notez que les fichiers natifs seront exportés dans tous les cas. 
    
4. Sous **métadonnées**, sélectionnez l’une des options suivantes dans la liste **Exporter le modèle** (une fois par session). 
    
    - **Standard**: ensemble de base des éléments de données, des métadonnées et des propriétés. Utilisez cette option lorsque les données d’importation ont déjà été traitées dans Advanced eDiscovery et que les données d’exportation sont téléchargées vers un système qui contient déjà les fichiers. Par défaut, les colonnes de modèle d’exportation sont créées et remplies.
    
    - **All**: ensemble complet de métadonnées standard incluant toutes les données de traitement, ainsi que les scores d’analyse et de pertinence. Ce modèle est requis lorsque Advanced eDiscovery effectue le traitement et que les données de fichier sont téléchargées sur un système externe pour la première fois.
    
    - **Problèmes**: sélectionnez **tous les problèmes** ou sélectionnez un problème particulier que vous avez créé. 
    
5. Sous **destination**:
    
    - **Téléchargement sur l’ordinateur local**
    
    - **Exportation vers l’objet BLOB Azure défini par l’utilisateur**: si cette option est activée, vous pouvez spécifier une URL de conteneur et un jeton SAS.
    
      > [!NOTE]
      > Une fois qu’un package d’exportation est stocké dans l’objet BLOB Azure défini par l’utilisateur, les données ne sont plus gérées par Advanced eDiscovery; elle est gérée par l’objet BLOB Azure. Cela signifie que si vous supprimez le cas, les fichiers exportés resteront toujours sur le BLOB Azure. 
  
    - **Enregistrer le jeton SAS pour une session d’exportation future**: si cette option est activée, le jeton SAS est chiffré dans la base de données interne avancée eDiscovery pour une utilisation ultérieure.
    
      > [!NOTE]
      > Actuellement, le jeton SAS expire au bout d’un mois. Si vous essayez d’effectuer un téléchargement après plus d’un mois, vous devez annuler la dernière session, puis effectuer une nouvelle exportation. 
  
6. Cliquez sur **modifier** pour définir les paramètres de champ «pour la révision». 
    
    ![Configurer les paramètres de champ de révision pour un lot d’exportation](media/39451aba-f6fe-4a01-8ed0-0be6a6ce889a.png)
  
   - Sous **pour la révision des paramètres de champ**, dans la liste déroulante **Sélectionner un scénario** , sélectionnez le scénario et l’étendue de la révision. Les paramètres sont affichés en fonction de votre sélection.
    
      - **Vérifier tout** (valeur par défaut): tous les messages électroniques, pièces jointes et documents sont sélectionnés par défaut. 
    
      - **Examinez tout le contenu unique d’un jeu**: inclusifs et copies inclusives uniques, pièces jointes uniques dans le niveau du jeu de courrier, représentatives de chaque ensemble de doublons exacts.
    
      - **Examiner tout le contenu unique d’un ensemble-aucune copie inclusive**: inclus, pièces jointes uniques dans le niveau du jeu de messages, représentative de chaque ensemble de doublons exacts.
    
      - **Examinez tous les fichiers de famille et de contenu uniques**: inclus, pièces jointes uniques dans le niveau du jeu de messages, représentatif de chaque ensemble de doublons exacts, puis développez pour inclure les fichiers de famille.
    
      - **Personnalisé** (vous permet de définir les options dans la boîte de dialogue): par défaut, les sélections actuelles sont conservées et toutes les options de boîte de dialogue sont activées, afin d’autoriser leur sélection. Si vous sélectionnez cette option, vous pouvez personnaliser les paramètres des e-mails, des documents, des pièces jointes et des fichiers divers.
    
    - Sous **e-mails**, sélectionnez les courriers électroniques que vous souhaitez exporter.
    
      - **Tous les messages électroniques**: (par défaut) tous les messages électroniques sont sélectionnés.
    
      - **Inclusif**: un message électronique inclusif est le dernier courrier électronique d’un thread, qui contient tous les autres messages électroniques provenant du thread.
    
      - **Inclusifs et copies inclusives uniques**: copies inclusives et inclusifs avec le même objet, le même corps et les mêmes pièces jointes; les copies inclusives uniques sont des copies uniques de ces messages électroniques.
    
    - Sous **documents**, sélectionnez les documents que vous souhaitez exporter. 
    
      - **Tous les documents**: (par défaut) tous les documents sont sélectionnés.
    
      - **Pivots**: fichier choisi comme représentative de l’ensemble des doublons, généralement utilisé comme ligne de base lors de l’examen de l’ensemble.
    
      - **Représentatif de chaque ensemble de doublons exacts**: fichiers uniques de proximité (y compris le tableau croisé dynamique).
    
    - Sous **pièces jointes**, sélectionnez les pièces jointes que vous souhaitez exporter. 
    
      - **Toutes les pièces jointes**: (par défaut) toutes les pièces jointes sont sélectionnées.
    
      - **Pièce jointe unique au niveau du cas**: fichiers de pièces jointes uniques dans le cas spécifié.
    
      - **Pièce jointe unique dans le niveau du jeu de courrier électronique**: fichiers de pièces jointes uniques dans le cas d’un message électronique spécifié.
    
   - Sous**Micellaneous**, vous pouvez choisir de **traiter les pièces jointes en tant que documents**, de **traiter les courriers électroniques comme des documents**ou **de développer pour inclure des fichiers de famille**. Lorsque vous choisissez **développer pour inclure des fichiers de famille**, pour chaque fichier marqué pour révision, tous les fichiers de la même famille seront également marqués.
    
7. Sélectionnez **Enregistrer** pour enregistrer les paramètres. 
    
8. Une fois que vous avez spécifié les paramètres d’exportation, cliquez sur **créer une session**d’exportation pour démarrer l’exportation de lot.
    
    Lors de l’exportation, l’État est affiché dans l’état de la **tâche**. Les résultats sont affichés dans le résumé de l' **exportation**.
    
9. Dans la fenêtre **Télécharger les fichiers** , cliquez sur **copier dans le presse-papiers** pour copier la clé d’exportation. 
    
    ![Télécharger des fichiers](media/99cf2c13-4954-479f-9741-80d7458c1a15.png)
  
10. Cliquez sur **Fermer**. 
    
    L’outil d’exportation de découverte électronique est démarré.
    
    ![Outil d’exportation de la découverte électronique](media/705756ca-ee97-4d24-b70f-8b23513f6d11.gif)
  
11. Dans l' **outil d’exportation de découverte électronique**:
    
    -  Dans **coller la signature d’accès partagé qui sera utilisée pour se connecter à la source**, collez la clé d’exportation youcopied dans le presse-papiers à l’étape 7.
    
    - Cliquez sur **Parcourir** pour sélectionner l’emplacement cible pour le stockage des fichiers d’exportation téléchargés sur l’ordinateur local. 
    
    - Cliquez sur **Démarrer**. Les fichiers d’exportation sont téléchargés sur l’ordinateur local. Si vous avez choisi **Exporter vers un objet BLOB Azure défini** par l’utilisateur à l’étape 4, la session est exportée vers une URL de stockage BLOB de votre choix.
    
Pour une description complète des champs figurant dans le rapport d’exportation, voir [Export report fields](export-report-fields-in-advanced-ediscovery.md).
  
## <a name="export-report-output-files"></a>Exporter les fichiers de sortie de rapport
<a name="BK_ExportOutputFIles"> </a>

Le tableau suivant répertorie les fichiers de sortie générés lors de l’exécution d’un lot d’exportation.
  
|**Nom de fichier**|**Type de fichier**|**Description**|
|:-----|:-----|:-----|
|Exporter le résumé  <br/> |value  <br/> |Un fichier journal généré par l’outil d’exportation de découverte électronique.  <br/> |
|Suivi  <br/> |txt  <br/> |Un fichier journal généré par l’outil d’exportation de découverte électronique.  <br/> |
|Fichiers texte extraits  <br/> |Dossier de fichiers  <br/> |Dossier qui contient les fichiers texte extraits des fichiers exportés.  <br/> |
|Fichiers d’entrée ou natifs  <br/> |Dossier de fichiers  <br/> |Dossier qui contient les fichiers d’entrée et d’entrée natifs des fichiers exportés.  <br/> |
|Exporter la liste  <br/> |xlsx  <br/> |Métadonnées de fichiers exportées au format xlsx. Les champs de fichiers sont en fonction du modèle que l’utilisateur choisit d’exporter. Si nécessaire, plusieurs fichiers sont créés, chacun contenant 100 150K lignes. Si une certaine valeur contient plus de caractères qu’une cellule Excel ne peut contenir (actuellement la limite est de 32 767 caractères), la valeur sera réduite à la longueur maximale autorisée. Si une valeur est ajustée, la couleur d’arrière-plan de la cellule est rouge pour l’indiquer à l’utilisateur. " «Participants à la messagerie» est un exemple de champ qui peut dépasser la limite de longueur, si le courrier électronique a été envoyé à une grande distribution. Pour plus d’informations sur les champs de sortie, voir [Export report fields](export-report-fields-in-advanced-ediscovery.md) .  <br/> |
|Charger un fichier  <br/> |value  <br/> |Métadonnées de fichiers exportées au format CSV pour chargement dans une autre application. Les champs de fichiers sont en fonction du modèle que l’utilisateur choisit d’exporter.  <br/> |
|Indicateur de réussite  <br/> |txt  <br/> |Créé uniquement lors de l’exportation vers un objet BLOB Azure tiers. Si l’exportation réussit complètement, le fichier est créé. En cas de défaillance ou de la réussite partielle, le fichier ne sera pas créé. Le fichier est créé dans le dossier racine, ce qui permet le suivi automatique des différents statuts de lots/sessions d’exportation. Il s’agit d’un fichier vide. Son nom est: TenantId_CaseId_ExternalCaseId_CaseName_ExportBatchId_SessionId_DateTime. txt.  <br/> |
   
## <a name="see-also"></a>Voir aussi

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[Affichage de l’historique du lot et exportation des résultats passés](view-batch-history-and-export-past-results.md)
  
[Configuration rapide d’Office 365 Advanced eDiscovery](quick-setup-for-advanced-ediscovery.md)

[Exportation des champs d’un rapport](export-report-fields-in-advanced-ediscovery.md)
  
[Augmentation de la vitesse de téléchargement lors de l’exportation des résultats de recherche eDiscovery à partir d’Office 365](increase-download-speeds-when-exporting-ediscovery-results.md)

