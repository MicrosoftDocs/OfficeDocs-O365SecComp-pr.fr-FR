---
title: Exécuter le module de processus d’eDiscovery Office 365 avancée
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
ms.assetid: dbc1e251-0596-443b-ac9b-f398ba955b73
description: 'Découvrez les instructions pour la préparation des fichiers cas de données Office 365 pour l’analyse avec Office 365 avancée de découverte électronique.  '
ms.openlocfilehash: 52b1dce9fb778c6628d90c39135f0c93f08134d7
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528653"
---
# <a name="run-the-process-module-in-office-365-advanced-ediscovery"></a><span data-ttu-id="47ccd-103">Exécuter le module de processus d’eDiscovery Office 365 avancée</span><span class="sxs-lookup"><span data-stu-id="47ccd-103">Run the Process module in Office 365 Advanced eDiscovery</span></span>

<span data-ttu-id="47ccd-104">Dossiers sont chargés dans la découverte électronique avancée lors de la **préparation** \> **processus**.</span><span class="sxs-lookup"><span data-stu-id="47ccd-104">Case files are loaded into the Advanced eDiscovery during **Prepare** \> **Process**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="47ccd-p101">Découverte avancée nécessite un Office 365 E3 avec le module complémentaire de conformité avancée ou un abonnement E5 pour votre organisation. Si vous n’avez qu’un plan d’et essayer eDiscovery avancé, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="47ccd-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
## <a name="guidelines-preparing-data-for-advanced-ediscovery"></a><span data-ttu-id="47ccd-107">Conseils : Préparation des données pour la découverte avancée</span><span class="sxs-lookup"><span data-stu-id="47ccd-107">Guidelines: Preparing data for Advanced eDiscovery</span></span>

- <span data-ttu-id="47ccd-108">**Qualité**: clairement identifier la population dossier pertinente à la casse.</span><span class="sxs-lookup"><span data-stu-id="47ccd-108">**Quality**: Clearly identify the case file population pertinent to the case.</span></span>
    
- <span data-ttu-id="47ccd-109">**Charges**: charger les fichiers dans un emplacement accessible à la découverte électronique avancée.</span><span class="sxs-lookup"><span data-stu-id="47ccd-109">**Loads**: Load the files into a location that is accessible to Advanced eDiscovery.</span></span>
    
- <span data-ttu-id="47ccd-p102">**ID du fichier**: un identificateur de fichier unique d’eDiscovery avancée. Si aucun identificateur de fichier n’est importé, eDiscovery avancé génère automatiquement l’ID. Si vous mappez l’ID une charge de processus suivante et mappez un chemin d’accès autre que de la charge de travail initial, eDiscovery avancée sera remplacer le chemin d’accès (plutôt qu’ajouter une nouvelle entrée de fichier). L’ID peut être utilisé comme une référence dans le processus d’exportation. La valeur d’ID ne doit pas être « -1 ».</span><span class="sxs-lookup"><span data-stu-id="47ccd-p102">**File ID**: A unique file identifier in Advanced eDiscovery. If no file identifier is imported, Advanced eDiscovery automatically generates the ID. If you map the ID in a subsequent Process load, and map a different path than in the initial Process load, Advanced eDiscovery will replace the path (rather than add a new file entry). The ID can be used as a reference in the Export process. The ID value should not be "-1".</span></span>
    
- <span data-ttu-id="47ccd-p103">**MD5**: cette signature est utilisée pour différencier les fichiers (deux fichiers sont considérées comme identiques, sauf si elles ont le même MD5). Par défaut, eDiscovery avancée calcule MD5 des fichiers. Lorsque les fichiers chargés sont des fichiers texte, il est recommandé pour charger et mapper la valeur MD5 d’origine plutôt que le calcul d’eDiscovery avancée.</span><span class="sxs-lookup"><span data-stu-id="47ccd-p103">**MD5**: This signature is used to differentiate between files (two files are not considered exact duplicates unless they have the same MD5). By default, Advanced eDiscovery calculates the MD5 of files. When the loaded files are text files, it is recommended to load and map the original MD5 value instead of calculating it in Advanced eDiscovery.</span></span>
    
- <span data-ttu-id="47ccd-118">**Nom et type de fichier**:</span><span class="sxs-lookup"><span data-stu-id="47ccd-118">**File type and name**:</span></span>
    
  - <span data-ttu-id="47ccd-p104">Découverte avancée peut traiter les fichiers de différents formats et extraire les fichiers natifs chargés dans un format standard, telles que \*. TXT, HTML ou. XML. le traitement des fichiers texte est plus rapide que les fichiers natifs. Texte extrait les fichiers sont stockés dans le dossier de cas.</span><span class="sxs-lookup"><span data-stu-id="47ccd-p104">Advanced eDiscovery can process files of various formats and extract loaded native files into a standard format, such as \*.TXT, HTML, or .XML. Processing of text files is faster than native files. Extracted text files are stored in the case folder.</span></span>
    
  - <span data-ttu-id="47ccd-p105">Ne pas charger les fichiers qui ne peuvent pas être extraites, telles que les fichiers système ou les images graphiques. Ces fichiers peuvent différer le traitement.</span><span class="sxs-lookup"><span data-stu-id="47ccd-p105">Do not load files that cannot be extracted, such as system files or graphic images. These files may delay processing.</span></span>
    
  - <span data-ttu-id="47ccd-124">Vérifiez que les noms de fichiers sont considérablement nommés et des chemins d’accès sont corrects.</span><span class="sxs-lookup"><span data-stu-id="47ccd-124">Verify that file names are significantly named and paths are correct.</span></span>
    
- <span data-ttu-id="47ccd-125">**Chemin d’accès du fichier**: découverte avancée peut charger des fichiers avec des longueurs de chemin d’accès jusqu'à 400 caractères.</span><span class="sxs-lookup"><span data-stu-id="47ccd-125">**File path**: Advanced eDiscovery can load files with path lengths up to 400 characters.</span></span>
    
- <span data-ttu-id="47ccd-p106">**Extraction de texte**: lors de l’extraction de texte à partir des fichiers natives, en plus du texte normal, les éléments suivants sont également extraits : colonnes de texte masqué (Excel et .doc), masqué (Excel), le suivi des modifications (.doc), objets de notes (.ppt), incorporées haut-parleur (par exemple, Objets Excel dans un .ppt). Ils peuvent être affichés dans l’éditeur de texte.</span><span class="sxs-lookup"><span data-stu-id="47ccd-p106">**Text extraction**: When extracting text from native files, in addition to normal text, the following are also extracted: hidden text (Excel and .doc), hidden columns (Excel), track changes (.doc), speaker notes (.ppt), embedded objects (for example, Excel objects in a .ppt). These can be viewed in the Text editor.</span></span>
    
- <span data-ttu-id="47ccd-p107">**Ignorer le texte**: cette fonctionnalité facultative est définie après l’exécution de processus et avant l’analyse. Ignorer texte doit être utilisé avec précaution, car son utilisation peut réduire les performances de l’analyse des fichiers.</span><span class="sxs-lookup"><span data-stu-id="47ccd-p107">**Ignore Text**: This optional feature is defined after Process is run and before Analyze. Ignore text should be used with caution because its use may reduce the performance of file analysis.</span></span>
    
- <span data-ttu-id="47ccd-130">**Texte multilingue**: eDiscovery avancée ne gère pas actuellement noms multilingues pour les balises, dépositaire et problèmes.</span><span class="sxs-lookup"><span data-stu-id="47ccd-130">**Multilingual text**: Advanced eDiscovery does not currently handle multilingual names for tags, custodian, and issues.</span></span>
    
- <span data-ttu-id="47ccd-p108">**Métadonnées**: déterminer s’il existe des métadonnées que vous souhaitez enregistrer dans la base de données de dossier pour servir ultérieurement de référence, telles que la plage de dates, taille de fichier, le type de fichier, dépositaire et de l’objet. Métadonnées peuvent être chargée une fois que les fichiers ont été déjà chargés sans réexécuter l’inventaire ou l’ajout de nouveau traitement une surcharge.</span><span class="sxs-lookup"><span data-stu-id="47ccd-p108">**Metadata**: Determine if there is metadata that you want to save in the case database for future reference, such as date range, file size, file type, custodian, and subject. Metadata can be loaded after files were already loaded without rerunning the inventory or adding reprocessing overhead.</span></span> 
    
  - <span data-ttu-id="47ccd-p109">Si les fichiers ont été initialement chargés par le chemin d’accès, mappez la colonne chemin d’accès lorsque vous importez des métadonnées ultérieurement. Il est possible pour faire référence au fichier par ID et de mapper un autre chemin d’accès. Il s’agit d’un scénario utile lorsque vous modifiez les chemins d’accès de fichier.</span><span class="sxs-lookup"><span data-stu-id="47ccd-p109">If the files were originally loaded by path, map the path column when later importing metadata. It is possible to refer to the file by ID and to map a different path. This is a useful scenario when the file paths change.</span></span>
    
  - <span data-ttu-id="47ccd-p110">Si les fichiers ont été initialement chargées par ID de fichier, mappez la colonne ID lors du chargement des métadonnées. Référence au fichier par le chemin d’accès (au lieu d’ID) entraînera fichiers recharger avec un autre code. Découverte avancée crée des copies des fichiers plutôt que du chargement des métadonnées des fichiers existants.</span><span class="sxs-lookup"><span data-stu-id="47ccd-p110">If the files were originally loaded by File ID, map the ID column when loading metadata. Referring to the file by path (instead of ID) will cause files to be re-loaded with a different ID. Advanced eDiscovery creates copies of the files rather that loading metadata of the existing files.</span></span>
    
- <span data-ttu-id="47ccd-139">**Familles**: il n’est pas possible de charger une famille sans parent (chef de famille).</span><span class="sxs-lookup"><span data-stu-id="47ccd-139">**Families**: It is not possible to load a family without its parent (head of family).</span></span> 
    
- <span data-ttu-id="47ccd-p111">**Taille du fichier**: il n’existe aucune limitation de la taille des fichiers chargés à la découverte électronique avancée. Pour l’analyse (analyse, la pertinence, etc.), la limite est 5,242,880 caractères du texte extrait. Fichiers de grande taille sont ignorés (par exemple, dans la pertinence, fichiers ne participe pas le processus de la pertinence de la formation et ne reçoivent pas un score de pertinence après le calcul du lot).</span><span class="sxs-lookup"><span data-stu-id="47ccd-p111">**File size**: There is no limitation on the size of files loaded to Advanced eDiscovery. For analysis (Analyze, Relevance, etc.), the limit is 5,242,880 characters of extracted text. Larger files are ignored (for example, in Relevance, files do not participate in the Relevance training process and do not receive a Relevance score after batch calculation).</span></span>
    
- <span data-ttu-id="47ccd-p112">**Quantité de fichiers**: il n’existe aucune limite sur le nombre de fichiers qui peuvent être gérés dans un seul cas recommandée. Les performances dépendent les ressources de votre système.</span><span class="sxs-lookup"><span data-stu-id="47ccd-p112">**File quantity**: There is no recommended limit on the number of files that can be handled in a single case. Performance depends on the resources of your system.</span></span> 
    
## <a name="filtering-files"></a><span data-ttu-id="47ccd-145">Filtrage des fichiers</span><span class="sxs-lookup"><span data-stu-id="47ccd-145">Filtering files</span></span>

<span data-ttu-id="47ccd-p113">Une étiquette définie par l’utilisateur peut être associée à un ensemble de fichiers pour les exclure des processus ou d’autres tâches. Chaque session de processus est associée à un code de lot. Bien que le code de lot n’est pas visible à l’expert de la pertinence, il est possible à l’aide d’un utilitaire de recherche, en ajoutant un filtre pour le lot en cours et de marquer tous les fichiers appropriés avec une étiquette définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="47ccd-p113">A user-defined label can be associated with a set of files to exclude them from Process or other tasks. Each Process session is associated with a batch ID. Although the batch ID is not visible to the expert in Relevance, this can be done using a search utility, by adding a filter for the current batch and tagging all appropriate files with a user-defined label.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="47ccd-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47ccd-149">See also</span></span>

[<span data-ttu-id="47ccd-150">eDiscovery avancée Office 365</span><span class="sxs-lookup"><span data-stu-id="47ccd-150">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="47ccd-151">Le module de processus en cours d’exécution et de chargement des données</span><span class="sxs-lookup"><span data-stu-id="47ccd-151">Running the Process module and loading data</span></span>](run-the-process-module-and-load-data-in-advanced-ediscovery.md)
  
[<span data-ttu-id="47ccd-152">Affichage des résultats de module de processus</span><span class="sxs-lookup"><span data-stu-id="47ccd-152">Viewing Process module results</span></span>](view-process-module-results-in-advanced-ediscovery.md)

