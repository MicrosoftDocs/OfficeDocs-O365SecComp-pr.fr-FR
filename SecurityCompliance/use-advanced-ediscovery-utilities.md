---
title: Utilisez les utilitaires de découverte électronique Office 365 avancée
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
ms.assetid: 66ca9993-75f4-4724-aea2-5a0719b660c1
description: 'En savoir plus sur les utilitaires d’Office 365 avancée eDiscovery, y compris le journal d’événements, effacer les données, traiter les erreurs, modifiez la pertinence et l’analyse de transparence.  '
ms.openlocfilehash: a68c98dd353971fcaa13fdc6b8e12bcf00c2faf0
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527585"
---
# <a name="use-office-365-advanced-ediscovery-utilities"></a><span data-ttu-id="56897-103">Utilisez les utilitaires de découverte électronique Office 365 avancée</span><span class="sxs-lookup"><span data-stu-id="56897-103">Use Office 365 Advanced eDiscovery utilities</span></span>

> [!NOTE]
> <span data-ttu-id="56897-p101">Découverte avancée nécessite un Office 365 E3 avec le module complémentaire de conformité avancée ou un abonnement E5 pour votre organisation. Si vous n’avez qu’un plan d’et essayer eDiscovery avancé, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="56897-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="56897-106">Les utilitaires sont affichés et disponibles dans eDiscovery avancée dépendent des rôles de contexte et d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="56897-106">The utilities that are displayed and available in Advanced eDiscovery depend on context and user roles.</span></span>
  
## <a name="case-log"></a><span data-ttu-id="56897-107">Journal d’événements</span><span class="sxs-lookup"><span data-stu-id="56897-107">Case log</span></span>

<span data-ttu-id="56897-p102">Le journal des cas fournit une liste détaillée des activités de traitement de l’application, qui peut être utilisé pour le suivi, résoudre les problèmes et pour le traitement des erreurs et avertissements. Le journal peut être généré et stocké localement sur l’hôte ou le serveur ou envoyé directement à une adresse de messagerie.</span><span class="sxs-lookup"><span data-stu-id="56897-p102">The Case log provides a detailed list of application processing activities, which can be used for tracking, troubleshooting, and for addressing errors and warnings. The log can be generated and stored locally on the host or server, or sent directly to an email address.</span></span>
  
<span data-ttu-id="56897-p103">Le fichier journal peut également être téléchargé à l’ordinateur client. L’option de téléchargement du client peut être activée ou désactivée en fonction du rôle d’utilisateur et de configuration.</span><span class="sxs-lookup"><span data-stu-id="56897-p103">The log file can also be downloaded to the client's computer. The client download option may be enabled or disabled according to configuration and user role.</span></span>
  
1. <span data-ttu-id="56897-112">Dans la barre de menus, cliquez sur l’icône **pignon** .</span><span class="sxs-lookup"><span data-stu-id="56897-112">In the menu bar, click the **Cogwheel** icon.</span></span> 
    
2. <span data-ttu-id="56897-113">Dans la **utilitaires et les paramètres \> utilitaires** onglet, sélectionnez **journal des cas \> le programme d’installation**.</span><span class="sxs-lookup"><span data-stu-id="56897-113">In the **Settings and utilities \> Utilities** tab, select **Case log \> Setup**.</span></span>
    
3. <span data-ttu-id="56897-114">Sélectionnez le **niveau de journalisation** comme suit :</span><span class="sxs-lookup"><span data-stu-id="56897-114">Select the **Log level** as follows:</span></span> 
    
  - <span data-ttu-id="56897-p104">**Standard**: inclut les données du journal de base. Cette option n’est généralement nécessaire pour la surveillance et doit être utilisée à moins que recommandé dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="56897-p104">**Standard**: Includes the basic log data. This option is usually necessary for monitoring, and should be used unless recommended otherwise.</span></span>
    
  - <span data-ttu-id="56897-117">**Minimum**: utilisée dans le cas de très grande taille et renvoie uniquement les données les plus récentes.</span><span class="sxs-lookup"><span data-stu-id="56897-117">**Minimal**: Used for very large cases, and returns only the latest data.</span></span>
    
4. <span data-ttu-id="56897-p105">Cliquez sur **journal d’exécuter les cas**. Le journal est généré et le chemin d’accès est affiché. Les informations de l’avancement des tâches pour la tâche en cours et le dernier s’affiche dans le volet d’état.</span><span class="sxs-lookup"><span data-stu-id="56897-p105">Click **Run Case log**. The log is generated and path is displayed. The task progress information for the current and last task is displayed in the Task status pane.</span></span>
    
## <a name="clear-data"></a><span data-ttu-id="56897-121">Effacer les données</span><span class="sxs-lookup"><span data-stu-id="56897-121">Clear data</span></span>

<span data-ttu-id="56897-p106">S’il est nécessaire de supprimer ou réinitialiser les données de cas, l’instance de base de données doit être initialisé. L’utilitaire d’effacement des données supprime spécifiées toutes les entrées de la casse de la base de données, fichiers texte, dossier de cas et résultats cumulés. La fonction peut uniquement être effectuée par un administrateur.</span><span class="sxs-lookup"><span data-stu-id="56897-p106">If it is necessary to delete or reinitialize case data, the database instance must be initialized. The Clear data utility deletes all specified entries from the case database, text files, case folder, and accumulated results. The function can only be performed by an administrator.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="56897-p107">Cette action n’est pas réversible et efface toutes les marquer la pertinence et analyse effectuée par l’expert. Enregistrer une sauvegarde de données, si nécessaire. Utilisez cette option avec précaution. Suppression des fichiers balisés et classés peut avoir un impact sur les résultats de la pertinence.</span><span class="sxs-lookup"><span data-stu-id="56897-p107">This action is not reversible and will clear all Relevance tagging and analysis performed by the expert. Save a backup of data, if necessary. Use this option with extreme care. Deleting tagged and ranked files can impact the Relevance results.</span></span> 
  
1. <span data-ttu-id="56897-129">Dans la barre de menus, cliquez sur l’icône **pignon** .</span><span class="sxs-lookup"><span data-stu-id="56897-129">In the menu bar, click the **Cogwheel** icon.</span></span> 
    
2. <span data-ttu-id="56897-130">Dans la **utilitaires et les paramètres \> utilitaires** onglet, sélectionnez **Effacer les données \> le programme d’installation**.</span><span class="sxs-lookup"><span data-stu-id="56897-130">In the **Settings and utilities \> Utilities** tab, select **Clear data \> Setup**.</span></span>
    
3. <span data-ttu-id="56897-131">Sélectionnez une option pour obtenir les informations d’initialisation :</span><span class="sxs-lookup"><span data-stu-id="56897-131">Select an option for the information to initialize:</span></span>
    
  - <span data-ttu-id="56897-p108">**Pertinence**: supprime tous les, dans la pertinence, y compris la définition de la charge et l’association de fichiers à des charges de travail. Il supprime tous les exemples et marquage.</span><span class="sxs-lookup"><span data-stu-id="56897-p108">**Relevance**: Deletes all work done in Relevance, including definition of loads and association of files to loads. It deletes all samples and tagging.</span></span>
    
  - <span data-ttu-id="56897-134">**Près de doublons et les threads de messagerie**: supprime toutes les informations d’analyse de proximité des doublons et les threads de messagerie.</span><span class="sxs-lookup"><span data-stu-id="56897-134">**Near-duplicates and email threads**: Deletes all analysis information of near-duplicates and email threads.</span></span>
    
  - <span data-ttu-id="56897-135">**Thèmes**: supprime les données liées à des thèmes.</span><span class="sxs-lookup"><span data-stu-id="56897-135">**Themes**: Deletes themes-related data.</span></span>
    
  - <span data-ttu-id="56897-136">**Exporter l’historique**: supprime les informations d’historique des lots de l’exportation.</span><span class="sxs-lookup"><span data-stu-id="56897-136">**Export history**: Deletes history information of Export batches.</span></span>
    
4. <span data-ttu-id="56897-p109">Cliquez sur **Effacer les données**. Les données des dossiers sont désactivées. Les informations de progression de la tâche en cours et la dernière tâche sont affichées dans le volet **d’état de la tâche** .</span><span class="sxs-lookup"><span data-stu-id="56897-p109">Click **Clear data**. The case data is cleared. The task progress information for the current and last task is displayed in the **Task status** pane.</span></span> 
    
## <a name="modify-relevance"></a><span data-ttu-id="56897-140">Modifier la pertinence</span><span class="sxs-lookup"><span data-stu-id="56897-140">Modify Relevance</span></span>

<span data-ttu-id="56897-141">Cette section décrit comment ignorer ou annuler un exemple de la pertinence.</span><span class="sxs-lookup"><span data-stu-id="56897-141">This section describes how to skip or roll back a Relevance sample.</span></span>
  
1. <span data-ttu-id="56897-142">Dans la barre de menus, cliquez sur l’icône **pignon** .</span><span class="sxs-lookup"><span data-stu-id="56897-142">In the menu bar, click the **Cogwheel** icon.</span></span> 
    
2. <span data-ttu-id="56897-143">Dans la **utilitaires et les paramètres \> utilitaires** , sélectionnez **la pertinence de la modifier**.</span><span class="sxs-lookup"><span data-stu-id="56897-143">In the **Settings and utilities \> Utilities** tab, select **Modify relevance**.</span></span>
    
3. <span data-ttu-id="56897-144">Sélectionnez l’une des options :</span><span class="sxs-lookup"><span data-stu-id="56897-144">Select from the options:</span></span> 
    
  - <span data-ttu-id="56897-p110">**Exemple actuel ignorer - utilisateur actif**: Cela permet d’identifier, comme à **Ignorer**, tous les fichiers non balisés dans l’exemple de cas open de l’utilisateur qui exécute l’utilitaire. Traitement de la pertinence pas sera effectuée sur les fichiers marqués comme à **Ignorer**.</span><span class="sxs-lookup"><span data-stu-id="56897-p110">**Skip current sample - for current user**: This will tag, as **Skip**, all untagged files in the open case sample of the user running the utility. Relevance processing will not be performed on files tagged as **Skip**.</span></span>
    
  - <span data-ttu-id="56897-p111">**Exemple actuel ignorer - tous les exemples d’ouvrir**: Cela permet d’identifier, comme à **Ignorer**, tous les fichiers non balisés dans tous les exemples pour tous les utilisateurs. Cette option n’est pas recommandée si les utilisateurs sont balisage actuellement exemples.</span><span class="sxs-lookup"><span data-stu-id="56897-p111">**Skip current sample - all open samples**: This will tag, as **Skip**, all untagged files in all open samples for all users. This option is not recommended if users are currently tagging samples.</span></span>
    
  - <span data-ttu-id="56897-p112">**Annuler la dernière exemple**: le dernier réalisé la pertinence de la formation sera restaurée, qu’elle soit avant ou après le processus de « Calculer ». Restauration d’un exemple de rattrapage n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="56897-p112">**Roll back last sample**: The last completed Relevance training sample will be rolled back, regardless of whether it is before or after the "Calculate" process. Rollback of a catch-up sample is not allowed.</span></span>
    
4. <span data-ttu-id="56897-151">Cliquez sur **exécuter** pour exécuter.</span><span class="sxs-lookup"><span data-stu-id="56897-151">Click **Execute** to run.</span></span> 
    
## <a name="transparency-analysis"></a><span data-ttu-id="56897-152">Analyse de transparence</span><span class="sxs-lookup"><span data-stu-id="56897-152">Transparency analysis</span></span>

<span data-ttu-id="56897-p113">L’utilitaire d’analyse de transparence permet une vue détaillée des fichiers et leurs score de pertinence affecté. Le rapport utilisable comme un contrôle de validité ou pour comparer la pertinence d’un fichier défini par un réviseur humain par rapport à la pertinence attribué par eDiscovery avancée.</span><span class="sxs-lookup"><span data-stu-id="56897-p113">The Transparency analysis utility enables a detailed view of files and their assigned Relevance score. The report can be used as a sanity check or to compare the relevance of a file defined by a human reviewer as compared to the relevance assigned by Advanced eDiscovery.</span></span> 
  
<span data-ttu-id="56897-p114">En plus des résultats de la pertinence, découverte avancée calcule et affecte le poids de mot clé que prendre en compte le contexte du mot clé. Poids différents, selon le contexte et l’emplacement peut être affecté à la même mot dans un fichier. Chaque mot clé est marqué à l’aide d’une échelle augmentation de l’intensité de couleur allant de jaune à orange foncé et différentes nuances de gris. Codage en couleurs est utilisé pour indiquer visuellement la famille du mot contribution positive ou négative pour le score de pertinence.</span><span class="sxs-lookup"><span data-stu-id="56897-p114">In addition to Relevance scores, Advanced eDiscovery calculates and assigns keyword weights that consider the keyword context. The same word in a file can be assigned different weights, depending on context and location. Each keyword is marked using an increasing scale of color intensity ranging from yellow to dark orange and varying shades of gray. Color coding is used to visually indicate the word's relative positive or negative contribution to the Relevance score.</span></span> 
  
<span data-ttu-id="56897-159">Dans un scénario de plusieurs problèmes, un rapport d’analyse de transparence peut être généré pour chaque problème.</span><span class="sxs-lookup"><span data-stu-id="56897-159">In a multiple-issue case scenario, a Transparency analysis report can be generated for each issue.</span></span>
  
1. <span data-ttu-id="56897-160">Dans la barre de menus, cliquez sur l’icône **pignon** .</span><span class="sxs-lookup"><span data-stu-id="56897-160">In the menu bar, click the **Cogwheel** icon.</span></span> 
    
2. <span data-ttu-id="56897-161">Dans la **utilitaires et les paramètres \> utilitaires** onglet, sélectionnez **analyse transparence \> le programme d’installation**.</span><span class="sxs-lookup"><span data-stu-id="56897-161">In the **Settings and utilities \> Utilities** tab, select **Transparency analysis \> Setup**.</span></span>
    
3. <span data-ttu-id="56897-162">Dans ** ID du fichier **, entrez l’ID de fichier du fichier à traiter.</span><span class="sxs-lookup"><span data-stu-id="56897-162">In ** File ID **, enter the file ID of the file to process.</span></span>
    
4. <span data-ttu-id="56897-163">Dans la liste des **problèmes** , sélectionnez le problème pertinent.</span><span class="sxs-lookup"><span data-stu-id="56897-163">In the **Issue** list, select the pertinent issue.</span></span> 
    
5. <span data-ttu-id="56897-p115">Cliquez sur **analyse de transparence**. Une fois terminé, le rapport d’analyse de transparence pour le fichier s’affiche, qui indique la façon dont les couleurs de mot clé marqués correspondent au score de pertinence.</span><span class="sxs-lookup"><span data-stu-id="56897-p115">Click **Transparency analysis**. Upon completion, the Transparency analysis report for the file is displayed, which shows how the marked keyword colors correlate to the overall Relevance score.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="56897-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56897-166">See also</span></span>

[<span data-ttu-id="56897-167">eDiscovery avancée Office 365</span><span class="sxs-lookup"><span data-stu-id="56897-167">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="56897-168">Définir les paramètres de la casse et client</span><span class="sxs-lookup"><span data-stu-id="56897-168">Defining case and tenant settings</span></span>](define-case-and-tenant-settings-in-advanced-ediscovery.md)

