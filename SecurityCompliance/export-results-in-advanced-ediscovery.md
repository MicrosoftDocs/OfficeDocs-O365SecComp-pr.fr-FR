---
title: Exporter les résultats dans Office 365 avancée de découverte électronique
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
ms.assetid: a9951a07-10b3-48cb-b37a-0ffaa24931ad
description: 'Découvrez comment définir les options d’exportation des résultats à partir d’Office 365 avancée eDiscovery, y compris la procédure permettant de spécifier des paramètres pour un lot d’exportation. '
ms.openlocfilehash: 92ee107ad096393fbccbc9a3dbe81d8e7dd28da9
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528694"
---
# <a name="export-results-in-office-365-advanced-ediscovery"></a>Exporter les résultats dans Office 365 avancée de découverte électronique

> [!NOTE]
> Découverte avancée nécessite un Office 365 E3 avec le module complémentaire de conformité avancée ou un abonnement E5 pour votre organisation. Si vous n’avez qu’un plan d’et essayer eDiscovery avancé, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Cette rubrique décrit les options de configuration d’exportation avancées eDiscovery.
  
 **Dans cette rubrique :**
  
- [Définition des sessions et exporter les lots](export-results-in-advanced-ediscovery.md#BK_Define)
    
- [Exportations incrémentielles et supplémentaires](export-results-in-advanced-ediscovery.md#BK_IncrementalReports)
    
- [Définir les paramètres d’exportation de lot](export-results-in-advanced-ediscovery.md#BK_SetUpExport)
    
- [Exporter des fichiers de sortie de rapport](export-results-in-advanced-ediscovery.md#BK_ExportOutputFIles)
    
## <a name="defining-export-batches-and-sessions"></a>Définition des sessions et exporter les lots
<a name="BK_Define"> </a>

Un lot d’exportation permet de traitement de l’exportation à l’aide d’un ensemble de paramètres définis. EDiscovery avancée vous permet de vous permet de définir des lots pour personnaliser chaque exportation.
  
Les paramètres sont définis par lot d’exportation. Un lot appelé « Exporter par lots 01 » est créé par défaut pour le premier lot d’un cas. Vous pouvez également modifier le nom et la description.
  
Une session de l’exportation est l’exécution de la découverte avancée exportation au sein d’un lot d’exportation.
  
## <a name="incremental-and-additional-exports"></a>Exportations incrémentielles et supplémentaires
<a name="BK_IncrementalReports"> </a>

Vous pouvez exécuter plusieurs sessions d’exportation au sein d’un lot d’exportation, pour garantir des résultats cohérents selon le même modèle d’exportation et les paramètres. Pour chaque session au sein d’un lot, vous pouvez exporter analytique nouvellement traitement des données d’incidents et traiter chaque « incrémentielle ».
  
Afin d’exporter à l’aide d’un ensemble de paramètres différent, vous devez d’abord créer un nouveau lot. La première session dans le nouveau lot produira des résultats pour les fichiers traités jusque-là, dans le cas ou non ces fichiers ont été importés et traités sur une ou plusieurs importations. Chaque lot recalcule les tableaux croisés dynamiques, similarité, inclusives, etc.. Sessions utilisent les paramètres définis pour le lot et ne pas recalculer des tableaux croisés dynamiques, similarité, inclusives, etc., pour l’exécution de chaque session.
  
Par exemple, supposons un cas a été importé et ses données analysées. Afin de récupérer la proximité des doublons et messagerie Threading des résultats pour les données incrémentielles, cliquez sur **créer exporter la session** dans le même lot qui a été utilisé précédemment pour exporter des données. 
  
## <a name="set-up-batch-export-parameters"></a>Définir les paramètres d’exportation de lot
<a name="BK_SetUpExport"> </a>

L’outil d’exportation eDiscovery est utilisée pour exporter les résultats de la recherche de découverte avancée sur votre ordinateur local. Pour augmenter le débit de transfert de données et accélérer le processus d’exportation, vous pouvez configurer un paramètre de Registre Windows sur l’ordinateur qui vous permet d’exporter les résultats de recherche. Si vous souhaitez augmenter la vitesse de téléchargement, configurer les paramètres de Registre avant de configurer les paramètres d’exportation. Pour plus d’informations, voir [augmenter la vitesse de téléchargement lors de l’exportation des résultats de recherche de découverte électronique à partir d’Office 365](increase-download-speeds-when-exporting-ediscovery-results.md).
  
1. Dans découverte avancée, sélectionnez un cas, cliquez sur **Exporter** \> **le programme d’installation**.
    
  - Dans la liste **Exporter le lot** , sélectionnez le nom ou exporter les résultats dans un lot d’exportation 01, (la feuille par défaut). 
    
  - Pour exporter les résultats pour les nouveaux fichiers ajoutés à un cas existant, continuez avec votre lot en cours. Pour créer une session dans le lot, sélectionnez le même numéro de traitement par lots et cliquez sur **créer exporter la session** , vous pouvez utiliser cette option pour exporter les mêmes paramètres que le lot précédent, de manière incrémentielle. 
    
  - Pour exporter vers un nouveau lot, cliquez sur **Ajouter**![icône Ajouter](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png)et entrez un nouveau nom dans **nom de la feuille** (ou acceptez celui par défaut) et une description dans la **description de lot**. Cliquez sur **OK**.
    
  - Pour modifier un nom ou une description, sélectionnez le nom de **l’exportation de lot**, cliquez sur **Modifier** ![icône Modifier](media/3d613660-7602-4df2-bdb9-14e9ca2f9cf2.png), puis modifiez les champs.
    
    > [!NOTE]
    > Après avoir exécuté les sessions pour un lot d’exportation, ils ne peuvent pas être supprimés. En outre, les seuls certains paramètres peuvent être modifiés une fois que la première session est exécutée. 
  
  - Pour créer un lot d’exportation en double, choisissez le **lot d’exportation en double**![créer une icône de lot d’exportation en double](media/3f6d5f59-e842-4946-a493-473528af0119.jpg) et entrez un nom et une description pour le lot en double dans le panneau de configuration. 
    
  - Pour supprimer un lot d’exportation, cliquez sur **Supprimer**![supprimer une icône d’exportation de lot](media/92a9f8e0-d469-48da-addb-69365e7ffb6f.jpg).
    
  - Pour afficher l’historique d’un lot, cliquez sur **historique de lot**![icône historique d’affichage](media/a80cc320-d96c-4d91-8884-75fe2cb147e2.jpg).
    
2. Sous **remplissage**, sélectionnez **inclure uniquement les fichiers au-dessus note coupure** et/ou de **lot d’exportation affiner** si vous souhaitez ajuster les paramètres de votre lot d’exportation. 
    
3. Si vous sélectionnez **inclure uniquement les fichiers au-dessus note coupure**, le **problème** est activé. Si le score de pertinence du fichier est supérieure au score de limite pour le problème sélectionné, le fichier sera exporté, sauf si elle est exclu par le filtre « pour révision ». 
  
Si vous sélectionnez **lot d’exportation affiner**, la **déduplication** et filtrer par « Pour révision » champ cases d’option sont activés. Si vous choisissez **la déduplication**, puis les fichiers en double seront filtrés en fonction de la stratégie définie [cas niveau (valeur par défaut) : à partir de chaque ensemble de fichiers en double dans le cas d’entier, un seul fichier sera déduplication duped. Niveau dépositaire : à partir de chaque ensemble de fichiers en double de la même dépositaire, un seul fichier sera déduplication duped.] La sortie d’exportation contient un enregistrement de tous les fichiers en double. Si vous choisissez champ **Filter by « pour passer en revue les'** , sélectionnez **Modifier sous métadonnées** pour entrer vos paramètres de champ **« pour révision »** . Sélectionnez **inclure les fichiers d’entrée** à inclure les fichiers sources dans le contenu du package. Vous pouvez désactiver ce paramètre pour accélérer le processus d’exportation. Notez que les fichiers natifs seront exportés dans tous les cas. 
    
4. Sous **métadonnées**, sélectionnez parmi les options suivantes dans la liste **Exporter le modèle** (une seule fois par session). 
    
  - **Standard**: ensemble de base des éléments de données, les métadonnées et les propriétés. Utilisez cette option lorsque importer des données a déjà été traitées dans découverte avancée et d’exporter des données sont téléchargées vers un système qui contient déjà les fichiers. Par défaut, les colonnes de modèle d’exportation sont créés et remplis.
    
  - **Tous les**: ensemble de toutes les données de traitement, ainsi que les scores d’analyser et de la pertinence de métadonnées standard. Ce modèle est requis lors de la découverte électronique avancée effectue le traitement et des données de fichier sont téléchargées vers un système externe pour la première fois.
    
  - **Problèmes**: sélectionnez **Tous les problèmes** ou un problème spécifique que vous avez créé. 
    
5. Sous **Destination**:
    
  - **Télécharger sur l’ordinateur local**
    
  - **Exporter vers définies par l’utilisateur de blob Azure**: Si cette option est activée, vous pouvez spécifier un jeton d’URL et les associations de conteneur.
    
    > [!NOTE]
    > Une fois qu’un package d’exportation est stocké dans blob Azure définis par l’utilisateur, les données ne sont plus gérées par eDiscovery avancée ; Il est géré par l’objet blob Azure. Cela signifie que si vous supprimez le cas, les fichiers exportés resteront toujours sur l’objet blob Azure. 
  
  - **Jeton de session exportation futurs SAS enregistrer**: s’il est activé, le jeton SAS sera chiffré dans la base de données interne de découverte électronique avancées pour une utilisation future.
    
    > [!NOTE]
    > Actuellement, le jeton SAS expire après un mois. Si vous essayez de télécharger après plus d’un mois, que vous devez annuler la dernière session, puis l’exporter à nouveau. 
  
6. Cliquez sur **Modifier** pour définir le » pour passer en revue les « paramètres de champ. 
    
> ![Configurer pour passer en revue les paramètres de champ pour un lot d’exportation](media/39451aba-f6fe-4a01-8ed0-0be6a6ce889a.png)
  
    In **For review field settings** panel, in **Select scenario**, select the scenario and scope of the review. The settings are displayed based on your selection.
    
    **Review all** (default): All emails, attachments, and documents are selected by default. 
    
    **Review all unique content in a set**: Inclusives and unique inclusive copies, unique attachments in email set level, representative from every set of exact duplicates.
    
    **Review all unique content in a set - no inclusive copies**: Inclusives, unique attachments in email set level, representative from every set of exact duplicates.
    
    **Review all unique content and related family files**: Inclusives, unique attachments in email set level, representative from every set of exact duplicates, expand to include family files.
    
    **Custom** (allows you to define the options in the dialog): The default is to keep current selections and enable all dialog options, to allow their selection. 
    
    If you select custom, you can then customize the settings for emails, documents, attachments and miscellaneous.
    
> Dans **les messages électroniques** , sélectionnez les messages électroniques que vous souhaitez exporter : 
    
    **All emails**: (default) All emails are selected.
    
    **Inclusives**: An inclusive email is a last email of a thread, and it contains all the other emails from the thread.
    
    **Inclusives and unique inclusive copies**: Inclusive copies and inclusives with the same subject, body and attachments; unique inclusive copies are unique copies of these emails .
    
> Dans les **Documents** , sélectionnez les documents que vous souhaitez exporter : 
    
    **All documents**: (default) All documents are selected.
    
    **Pivots**: A file chosen as representative of near-duplicates set, which is typically used as the baseline when reviewing the set.
    
    **Representative from every set of exact duplicates**: Unique near-duplicate files (including the pivot).
    
> Dans les **pièces jointes** , sélectionnez les pièces jointes que vous souhaitez exporter 
    
    **All attachments**: (default) All attachments are selected.
    
    **Unique attachment in case level**: Unique attachment files within the specified case.
    
    **Unique attachment in email set level**: Unique attachment files within the specified email case.
    
> Dans **divers** , vous pouvez choisir pour **traiter les pièces jointes en tant que documents**, **traiter les messages électroniques en tant que documents**ou **développer pour inclure des fichiers de votre famille**. Lorsque vous choisissez **développer pour inclure des fichiers de votre famille**, pour chaque fichier est marqué pour révision, tous les fichiers de la même famille également signalées.
    
    Choose **Save** to save the settings. 
    
7. Une fois que vous spécifiez les paramètres d’exportation, pour démarrer le traitement d’exportation, cliquez sur **créer exporter la session**.
    
    Pendant l’exportation, l’état est affiché dans **l’état de la tâche**. Les résultats sont affichés dans **l’exportation de synthèse**.
    
8. Dans la fenêtre **téléchargement de fichiers** , cliquez sur **Copier dans le Presse-papiers** pour copier la clé d’exportation. 
    
    ![Télécharger des fichiers](media/99cf2c13-4954-479f-9741-80d7458c1a15.png)
  
9. Cliquez sur **Fermer**. 
    
    L’outil d’exportation de découverte est démarré.
    
    ![Outil d’exportation de la découverte électronique](media/705756ca-ee97-4d24-b70f-8b23513f6d11.gif)
  
10. Dans l' **outil d’exportation de découverte électronique**:
    
1. **Collez la Signature accès partagé qui sera utilisé pour se connecter à la source**, collez dans la clé d’exportation qui youcopied dans le Presse-papiers à l’étape 7.
    
2. Cliquez sur **Parcourir** pour sélectionner l’emplacement cible pour le stockage des fichiers d’exportation téléchargé sur l’ordinateur local. 
    
11. Cliquez sur **Démarrer**. Les fichiers d’exportation sont téléchargés sur l’ordinateur local. Si vous avez choisi **d’Exporter vers blob Azure de défini par l’utilisateur** à l’étape 4, la session est exportée vers une destination d’URL de stockage Blob de votre choix. 
    
Pour une description complète des champs dans le rapport d’exportation, voir [exporter des champs du rapport](export-report-fields-in-advanced-ediscovery.md).
  
## <a name="export-report-output-files"></a>Exporter des fichiers de sortie de rapport
<a name="BK_ExportOutputFIles"> </a>

Le tableau suivant répertorie les fichiers de sortie qui sont générées lorsque vous exécutez un lot d’exportation.
  
|**Nom de fichier**|**Type de fichier**|**Description**|
|:-----|:-----|:-----|
|Résumé de l’exportation  <br/> |CSV  <br/> |Un fichier journal généré par l’outil d’exportation de découverte électronique.  <br/> |
|Suivi  <br/> |txt  <br/> |Un fichier journal généré par l’outil d’exportation de découverte électronique.  <br/> |
|Fichiers texte extrait  <br/> |Dossier de fichiers  <br/> |Dossier qui contient les fichiers texte extrait les fichiers exportés.  <br/> |
|Entrée ou fichiers natifs  <br/> |Dossier de fichiers  <br/> |Dossier qui contient les fichiers natifs et d’entrée des fichiers exportés.  <br/> |
|Exporter la liste  <br/> |xlsx  <br/> |Métadonnées de fichiers exportés au format xlsx. Champs dans les fichiers sont appliquent aux modèles utilisateur sélectionne à exporter. Si nécessaire, plusieurs fichiers sont créés, chacun contient des lignes de 100 à 150 Ko. Si une certaine valeur contient plus de caractères qu’une cellule Excel peut contenir (actuellement la limite est de 32 767 caractères), puis la valeur est supprimée à la longueur maximale autorisée. Si une valeur est tronquée, couleur d’arrière-plan de la cellule est rouge pour indiquer à l’utilisateur. » Participants e-mail » sont un exemple d’un champ qui dépasse la limite de longueur, si le message électronique a été envoyé à une distribution de grande taille. Pour plus d’informations sur les champs de sortie, voir [exporter des champs du rapport](export-report-fields-in-advanced-ediscovery.md) .<br/> |
|Charger le fichier  <br/> |CSV  <br/> |Métadonnées de fichiers exportés au format csv pour le chargement dans une autre application. Champs dans les fichiers sont appliquent aux modèles utilisateur sélectionne à exporter.  <br/> |
|Indicateur de réussite  <br/> |txt  <br/> |Ne créés lors de l’exportation pour un 3ème partie blob Azure. Si l’exportation a abouti, le fichier sera créé. En cas d’échec, complet ou partiel réussite le fichier ne sera pas créé. Fichier sera créé dans le dossier racine, permettant de suivi automatique sur les différents statuts de lots/sessions d’exportation. Il s’agit d’un fichier vide. Son nom est : TenantId_CaseId_ExternalCaseId_CaseName_ExportBatchId_SessionId_DateTime.txt.  <br/> |
   
## <a name="see-also"></a>Voir aussi
<a name="BK_ExportOutputFIles"> </a>

[eDiscovery avancée Office 365](office-365-advanced-ediscovery.md)
  
[Affichage de l’historique des commandes et l’exportation des résultats antérieurs](view-batch-history-and-export-past-results.md)
  
[Programme d’installation rapide pour la découverte Office 365 avancée](quick-setup-for-advanced-ediscovery.md)

[Champs du rapport d’exportation](export-report-fields-in-advanced-ediscovery.md)
  
[Augmenter la vitesse de téléchargement lors de l’exportation des résultats de recherche de découverte électronique à partir d’Office 365](increase-download-speeds-when-exporting-ediscovery-results.md)

