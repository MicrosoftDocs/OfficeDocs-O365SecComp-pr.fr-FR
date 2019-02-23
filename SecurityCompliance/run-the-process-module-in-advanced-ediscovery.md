---
title: Exécuter le module Processus dans Office 365 Advanced eDiscovery
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
ms.assetid: dbc1e251-0596-443b-ac9b-f398ba955b73
description: 'Découvrez les instructions relatives à la préparation des fichiers de cas des données Office 365 pour analyse avec Office 365 Advanced eDiscovery.  '
ms.openlocfilehash: 19d50bda21f752ec7c22fe52b6fa7272592de128
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216114"
---
# <a name="run-the-process-module-in-office-365-advanced-ediscovery"></a><span data-ttu-id="b8daf-103">Exécuter le module Processus dans Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="b8daf-103">Run the Process module in Office 365 Advanced eDiscovery</span></span>

<span data-ttu-id="b8daf-104">Les fichiers case sont chargés dans la découverte électronique avancée lors de la **préparation** \> \*\*\*\*.</span><span class="sxs-lookup"><span data-stu-id="b8daf-104">Case files are loaded into the Advanced eDiscovery during **Prepare** \> **Process**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b8daf-p101">Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous [inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="b8daf-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
## <a name="guidelines-preparing-data-for-advanced-ediscovery"></a><span data-ttu-id="b8daf-107">Recommandations: préparation des données pour Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="b8daf-107">Guidelines: Preparing data for Advanced eDiscovery</span></span>

- <span data-ttu-id="b8daf-108">**Qualité**: Identifiez clairement la population de fichiers de cas pertinente pour le cas.</span><span class="sxs-lookup"><span data-stu-id="b8daf-108">**Quality**: Clearly identify the case file population pertinent to the case.</span></span>
    
- <span data-ttu-id="b8daf-109">**Charge**: charge les fichiers dans un emplacement accessible à la découverte électronique avancée.</span><span class="sxs-lookup"><span data-stu-id="b8daf-109">**Loads**: Load the files into a location that is accessible to Advanced eDiscovery.</span></span>
    
- <span data-ttu-id="b8daf-p102">**ID de fichier**: identificateur de fichier unique dans Advanced eDiscovery. Si aucun identificateur de fichier n'est importé, Advanced eDiscovery génère automatiquement l'ID. Si vous mappez l'ID dans une charge de processus ultérieure et que vous mappez un chemin d'accès différent de celui de la charge de processus initiale, Advanced eDiscovery remplace le chemin d'accès (au lieu d'ajouter une nouvelle entrée de fichier). L'ID peut être utilisé comme référence dans le processus d'exportation. La valeur ID ne doit pas être «-1».</span><span class="sxs-lookup"><span data-stu-id="b8daf-p102">**File ID**: A unique file identifier in Advanced eDiscovery. If no file identifier is imported, Advanced eDiscovery automatically generates the ID. If you map the ID in a subsequent Process load, and map a different path than in the initial Process load, Advanced eDiscovery will replace the path (rather than add a new file entry). The ID can be used as a reference in the Export process. The ID value should not be "-1".</span></span>
    
- <span data-ttu-id="b8daf-p103">**MD5**: cette signature est utilisée pour différencier les fichiers (deux fichiers ne sont pas considérés comme des doublons exactes, sauf s'ils ont le même MD5). Par défaut, Advanced eDiscovery calcule le MD5 des fichiers. Lorsque les fichiers chargés sont des fichiers texte, il est recommandé de charger et de mapper la valeur MD5 d'origine au lieu de la calculer dans Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="b8daf-p103">**MD5**: This signature is used to differentiate between files (two files are not considered exact duplicates unless they have the same MD5). By default, Advanced eDiscovery calculates the MD5 of files. When the loaded files are text files, it is recommended to load and map the original MD5 value instead of calculating it in Advanced eDiscovery.</span></span>
    
- <span data-ttu-id="b8daf-118">**Nom et type de fichier**:</span><span class="sxs-lookup"><span data-stu-id="b8daf-118">**File type and name**:</span></span>
    
  - <span data-ttu-id="b8daf-p104">Advanced eDiscovery peut traiter des fichiers de différents formats et extraire les fichiers natifs chargés dans un format standard \*, comme. TXT, HTML ou. XML. le traitement des fichiers texte est plus rapide que les fichiers natifs. Les fichiers texte extraits sont stockés dans le dossier case.</span><span class="sxs-lookup"><span data-stu-id="b8daf-p104">Advanced eDiscovery can process files of various formats and extract loaded native files into a standard format, such as \*.TXT, HTML, or .XML. Processing of text files is faster than native files. Extracted text files are stored in the case folder.</span></span>
    
  - <span data-ttu-id="b8daf-p105">Ne chargez pas les fichiers qui ne peuvent pas être extraits, tels que les fichiers système ou les images graphiques. Ces fichiers peuvent retarder le traitement.</span><span class="sxs-lookup"><span data-stu-id="b8daf-p105">Do not load files that cannot be extracted, such as system files or graphic images. These files may delay processing.</span></span>
    
  - <span data-ttu-id="b8daf-124">Vérifiez que les noms de fichiers sont beaucoup nommés et que les chemins d'accès sont corrects.</span><span class="sxs-lookup"><span data-stu-id="b8daf-124">Verify that file names are significantly named and paths are correct.</span></span>
    
- <span data-ttu-id="b8daf-125">**Chemin d'accès de fichier**: Advanced eDiscovery peut charger des fichiers avec des longueurs de chemin d'accès allant jusqu'à 400 caractères.</span><span class="sxs-lookup"><span data-stu-id="b8daf-125">**File path**: Advanced eDiscovery can load files with path lengths up to 400 characters.</span></span>
    
- <span data-ttu-id="b8daf-p106">**Extraction de texte**: lors de l'extraction de texte à partir de fichiers natifs, en plus du texte normal, les éléments suivants sont également extraits: texte masqué (Excel et. doc), colonnes masquées (Excel), suivi des modifications (. doc), notes du présentateur (. ppt), objets incorporés (par exemple, Objets Excel dans un. ppt). Ces éléments peuvent être affichés dans l'éditeur de texte.</span><span class="sxs-lookup"><span data-stu-id="b8daf-p106">**Text extraction**: When extracting text from native files, in addition to normal text, the following are also extracted: hidden text (Excel and .doc), hidden columns (Excel), track changes (.doc), speaker notes (.ppt), embedded objects (for example, Excel objects in a .ppt). These can be viewed in the Text editor.</span></span>
    
- <span data-ttu-id="b8daf-p107">**Ignorer le texte**: cette fonctionnalité facultative est définie après l'exécution du processus et avant l'analyse. Ignorer le texte doit être utilisé avec précaution car son utilisation peut réduire les performances de l'analyse des fichiers.</span><span class="sxs-lookup"><span data-stu-id="b8daf-p107">**Ignore Text**: This optional feature is defined after Process is run and before Analyze. Ignore text should be used with caution because its use may reduce the performance of file analysis.</span></span>
    
- <span data-ttu-id="b8daf-130">**Texte multilingue**: Advanced eDiscovery ne gère actuellement pas les noms multilingues pour les balises, les dépositaires et les problèmes.</span><span class="sxs-lookup"><span data-stu-id="b8daf-130">**Multilingual text**: Advanced eDiscovery does not currently handle multilingual names for tags, custodian, and issues.</span></span>
    
- <span data-ttu-id="b8daf-p108">**Métadonnées**: Déterminez s'il existe des métadonnées que vous souhaitez enregistrer dans la base de données de cas pour référence ultérieure, comme la plage de dates, la taille de fichier, le type de fichier, le dépositaire et l'objet. Les métadonnées peuvent être chargées après que les fichiers ont déjà été chargés sans réexécuter l'inventaire ou ajouter une charge de retraitement.</span><span class="sxs-lookup"><span data-stu-id="b8daf-p108">**Metadata**: Determine if there is metadata that you want to save in the case database for future reference, such as date range, file size, file type, custodian, and subject. Metadata can be loaded after files were already loaded without rerunning the inventory or adding reprocessing overhead.</span></span> 
    
  - <span data-ttu-id="b8daf-p109">Si les fichiers ont été chargés par chemin d'accès, mappez la colonne chemin d'accès lors de l'importation des métadonnées. Il est possible de faire référence au fichier par son ID et de mapper un autre chemin d'accès. Il s'agit d'un scénario utile lorsque les chemins d'accès de fichiers changent.</span><span class="sxs-lookup"><span data-stu-id="b8daf-p109">If the files were originally loaded by path, map the path column when later importing metadata. It is possible to refer to the file by ID and to map a different path. This is a useful scenario when the file paths change.</span></span>
    
  - <span data-ttu-id="b8daf-p110">Si les fichiers ont été initialement chargés par ID de fichier, mappez la colonne ID lors du chargement des métadonnées. Faire référence au fichier par chemin d'accès (au lieu d'ID) entraîne le chargement des fichiers avec un ID différent. Advanced eDiscovery crée des copies des fichiers au lieu de charger les métadonnées des fichiers existants.</span><span class="sxs-lookup"><span data-stu-id="b8daf-p110">If the files were originally loaded by File ID, map the ID column when loading metadata. Referring to the file by path (instead of ID) will cause files to be re-loaded with a different ID. Advanced eDiscovery creates copies of the files rather that loading metadata of the existing files.</span></span>
    
- <span data-ttu-id="b8daf-139">**Familles**: il n'est pas possible de charger une famille sans son parent (en-tête de famille).</span><span class="sxs-lookup"><span data-stu-id="b8daf-139">**Families**: It is not possible to load a family without its parent (head of family).</span></span> 
    
- <span data-ttu-id="b8daf-p111">**Taille du fichier**: il n'existe aucune limite quant à la taille des fichiers chargés vers Advanced eDiscovery. Pour l'analyse (analyse, pertinence, etc.), la limite est de 5 242 880 caractères du texte extrait. Les fichiers plus volumineux sont ignorés (par exemple, à des fins de pertinence, les fichiers ne participent pas au processus d'apprentissage de pertinence et ne reçoivent pas de score de pertinence après le calcul par lot).</span><span class="sxs-lookup"><span data-stu-id="b8daf-p111">**File size**: There is no limitation on the size of files loaded to Advanced eDiscovery. For analysis (Analyze, Relevance, etc.), the limit is 5,242,880 characters of extracted text. Larger files are ignored (for example, in Relevance, files do not participate in the Relevance training process and do not receive a Relevance score after batch calculation).</span></span>
    
- <span data-ttu-id="b8daf-p112">**Quantité de fichiers**: il n'y a pas de limite recommandée quant au nombre de fichiers qui peuvent être gérés dans un seul cas. Les performances dépendent des ressources de votre système.</span><span class="sxs-lookup"><span data-stu-id="b8daf-p112">**File quantity**: There is no recommended limit on the number of files that can be handled in a single case. Performance depends on the resources of your system.</span></span> 
    
## <a name="filtering-files"></a><span data-ttu-id="b8daf-145">Filtrage des fichiers</span><span class="sxs-lookup"><span data-stu-id="b8daf-145">Filtering files</span></span>

<span data-ttu-id="b8daf-p113">Une étiquette définie par l'utilisateur peut être associée à un ensemble de fichiers pour les exclure du processus ou d'autres tâches. Chaque session de processus est associée à un ID de lot. Bien que l'ID de lot ne soit pas visible par l'expert en matière de pertinence, vous pouvez le faire à l'aide d'un utilitaire de recherche en ajoutant un filtre pour le lot actuel et en marquant tous les fichiers appropriés avec une étiquette définie par l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b8daf-p113">A user-defined label can be associated with a set of files to exclude them from Process or other tasks. Each Process session is associated with a batch ID. Although the batch ID is not visible to the expert in Relevance, this can be done using a search utility, by adding a filter for the current batch and tagging all appropriate files with a user-defined label.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b8daf-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8daf-149">See also</span></span>

[<span data-ttu-id="b8daf-150">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="b8daf-150">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="b8daf-151">Exécution du module de processus et chargement des données</span><span class="sxs-lookup"><span data-stu-id="b8daf-151">Running the Process module and loading data</span></span>](run-the-process-module-and-load-data-in-advanced-ediscovery.md)
  
[<span data-ttu-id="b8daf-152">Affichage des résultats de module de processus</span><span class="sxs-lookup"><span data-stu-id="b8daf-152">Viewing Process module results</span></span>](view-process-module-results-in-advanced-ediscovery.md)

