---
title: Utiliser l’outil de collecte de PST pour rechercher, copier et supprimer des fichiers PST dans votre organisation
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/18/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid: MOE150
ms.assetid: 7a150c84-049c-4a9c-8c91-22355b35f2a7
description: Utilisez l’outil de collecte de PST Microsoft pour rechercher le réseau de votre organisation pour obtenir un inventaire des fichiers PST qui sont éparpillés dans votre organisation. Une fois que vous trouvez des fichiers PST, vous pouvez utiliser l’outil de collecte PST pour les copier dans un emplacement central afin que vous pouvez les importer dans Office 365.
ms.openlocfilehash: 0537a65a32fa25704045bd587cb20f9eee13f628
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038127"
---
# <a name="use-the-pst-collection-tool-to-find-copy-and-delete-pst-files-in-your-organization"></a>Utiliser l’outil de collecte de PST pour rechercher, copier et supprimer des fichiers PST dans votre organisation

Vous pouvez utiliser l’outil de collecte de PST Microsoft pour rechercher le réseau de votre organisation pour les fichiers PST. L’outil vous permet d’obtenir un inventaire des fichiers PST qui sont éparpillés dans votre organisation. Une fois que vous trouvez des fichiers PST, vous pouvez utiliser l’outil de collecte de PST de les copier dans un emplacement central. Ayant des fichiers pst dans un seul endroit, puis vous permet d’importer les boîtes aux lettres Exchange Online (ou d’une seule boîte aux lettres Exchange Online), où vous pouvez ensuite appliquer l’ensemble complet de fonctionnalités de conformité dans Office 365. Cela inclut l’importation des fichiers pst dans l’archive contient des boîtes aux lettres, rechercher des messages spécifiques dans les fichiers PST que vous avez importés à l’aide des outils de recherche de découverte électronique, la conservation des messages à l’aide de découverte électronique des utilisateurs et les stratégies de rétention Office 365 et la gestion de la durée de vie cycle de ces messages à l’aide de la messagerie enregistre des fonctionnalités de gestion dans Exchange Online. Une fois que vous êtes convaincu que les fichiers PST que vous avez collectées ont été importés vers Office 365, vous pouvez utiliser l’outil de les supprimer de leur emplacement d’origine sur votre réseau. 
  
Une autre chose à faire avec l’outil de collecte de PST est d’empêcher les utilisateurs de créer de nouveaux fichiers PST et de modifier les fichiers PST existants que vous trouvez sur votre réseau. Ces fonctionnalités « bloc » vous permettent de rechercher, recueillir et importer un ensemble donné de fichiers PST vers Office 365 et empêcher la multiplication future des fichiers PST dans votre organisation. 
  
## <a name="how-the-pst-collection-tool-works"></a>Fonctionne de l’outil de collecte de PST

Voici une vue d’ensemble rapide du processus d’utilisation de l’outil de collecte de PST pour rechercher, contrôler, collecter et supprimer des fichiers PST dans votre organisation.
  
![Vue d’ensemble du processus d’outil de Collection PST](media/67a29f27-f83c-4f0a-9df4-7ed92d3086fe.png)
  
1. **[Étape 1 : rechercher les fichiers PST sur votre réseau](#step-1-find-pst-files-on-your-network)** - lorsque vous exécutez l’outil pour rechercher les fichiers PST, vous spécifiez un emplacement, tel que d’une unité d’organisation qui contiennent des objets Active Directory pour les ordinateurs client et serveur. Vous pouvez également rechercher des ordinateurs spécifiques ou des partages de fichiers réseau. Lorsque vous exécutez l’outil, un Agent de Collection « léger » est installé sur les ordinateurs cibles. Cet agent de recherche de l’ordinateur cible pour les fichiers PST et envoie ensuite les informations à l’outil PST Collection sur n’importe quel fichier PST qu’il trouve. L’outil crée les fichiers journaux qui contient des informations sur les fichiers PST qui ont été détectés dans les emplacements spécifiés. Ces fichiers sont utilisés lorsque vous exécutez l’outil ultérieurement. 
    
2. **[(Facultatif) étape 2 : contrôler l’accès aux fichiers PST](#optional-step-2-control-access-to-pst-files)** -l’outil crée un objet de stratégie de groupe (GPO) avec des paramètres qui empêchent les utilisateurs de créer ou modifier des fichiers PST. Cet objet de stratégie de groupe est appliquée à tous les utilisateurs de votre domaine. Cette étape facultative vous permet de « verrouiller » les fichiers PST qui ont été trouvées dans l’étape 1, afin que vous pouvez collecter, importer et les supprimer sans avoir créé des fichiers PST ou les fichiers PST existants modifiés. 
    
3. **[Étape 3 : copier les fichiers PST vers un emplacement de la collection](#step-3-copy-the-pst-files-to-a-collection-location)** -cela vous permet de collecter les fichiers PST au même emplacement afin que vous pouvez les importer dans boîtes aux lettres Exchange Online à l’aide du service Office 365 importer à l’étape 4. Lorsque vous exécutez l’outil en mode « collecter », chaque Agent Collection copie les fichiers PST de l’ordinateur cible de que l’agent est installé à l’emplacement de la collection. 
    
4. **[Étape 4 : importer les fichiers PST vers Office 365](#step-4-import-the-pst-files-to-office-365)** -une fois que vous avez copié les fichiers PST à un seul emplacement, vous êtes prêt à importer dans les boîtes aux lettres Exchange Online. 
    
5. **[Étape 5 : supprimer les fichiers PST détectés sur votre réseau](#step-5-delete-the-pst-files-found-on-your-network)** - une fois le fichier PST de fichiers que vous avez trouvé et collectées ont été importés vers des boîtes aux lettres Exchange Online dans Office 365, vous pouvez utiliser l’outil de collecte de PST pour supprimer les fichiers PST à partir des emplacements d’origine où ils a été trouvé à l’étape 1. 

## <a name="before-you-begin"></a>Avant de commencer

- Suivez ces étapes pour télécharger l’outil de collecte de PST sur votre ordinateur local. 
    
    1. [Télécharger l’outil de collecte de PST](https://aka.ms/pstcollectiontool).
    
    2. Dans la fenêtre contextuelle, cliquez sur **Enregistrer** \> **Enregistrer sous** pour enregistrer le fichier PSTCollectionTool.zip dans un dossier sur votre ordinateur local. 
    
    3. Extrayez le fichier PSTCollectionTool.zip dans un dossier sur votre ordinateur local ; le nom du dossier par défaut est PSTCollectionTool.
    
- Pour exécuter l’outil de collecte de PST dans n’importe quel mode (Find, bloquer, copier ou supprimer), vous devez être membre du groupe Administrateurs du domaine dans votre domaine Active Directory. 

## <a name="step-1-find-pst-files-on-your-network"></a>Étape 1 : Rechercher des fichiers PST sur votre réseau

La première étape consiste à exécuter l’outil PST Collection pour rechercher des fichiers PST dans votre organisation. Vous pouvez utiliser l’outil pour rechercher les types suivants d’emplacements. 
  
- Unités d’organisation (UO) dans un domaine d’Active Directory local. L’outil de recherche tous les ordinateurs qui sont contenus dans l’unité d’organisation spécifiée. 
    
- Ordinateurs client et serveur. L’outil de recherche des ordinateurs spécifiés. 
    
- Partages de fichiers réseau. L’outil de recherche dans les partages de fichiers réseau spécifié. 
    
Voir la description de le `Locations` paramètre dans la table dans la procédure suivante pour obtenir des exemples de la syntaxe à utiliser pour chacun de ces types d’emplacement. 
  
> [!IMPORTANT]
> Vous devez l’exécuter l’outil PST Collection dans le mode de recherche avant d’effectuer d’autres actions telles que le blocage, collecte ou la suppression des fichiers PST. 
  
1. Ouvrez une invite de commandes (exécuter en tant qu’administrateur) sur votre ordinateur local.
    
2. Accédez au dossier PSTCollectionTool (ou le dossier que vous avez extrait le fichier PSTCollectionTool.zip).
    
3. Accédez au répertoire DataCollectorMaster.
    
4. Exécutez la commande suivante pour rechercher des fichiers PST dans un emplacement spécifié.
    
    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Find -JobName <Name> -Locations <Locations to search for PSTs> -LogLocation <Location to store log files> -ConfigurationLocation <Location to store configuration files>
    ```

    Le tableau suivant décrit les paramètres et leurs valeurs requis lorsque vous exécutez la commande DataCollectorMaster.exe pour rechercher les fichiers PST. 
    
    |Paramètre ***|****Description****|Exemples ***|
    |:-----|:-----|:-----|
    | `DataSource` <br/> |Spécifie le type de données à rechercher. Actuellement, vous pouvez utiliser l’outil de collecte de PST pour rechercher des fichiers PST.  <br/> | `-DataSource Pst` <br/> |
    | `Mode` <br/> |Spécifie le type d’opération qui exécute l’outil. Utilisez la valeur `Find` pour rechercher les fichiers PST dans les emplacements spécifiés. Notez que l’outil peut rechercher et obtenir des informations sur les fichiers PST qui sont ouvertes dans Outlook et PST les fichiers qui sont reliés aux profils Outlook.<br/> | `-Mode Find` <br/> |
    | `JobName` <br/> |Spécifie le nom de la tâche de la Collection PST. Vous utiliserez ce nom de travail même lorsque vous exécutez l’outil PST Collection pour bloquer, de collecter et de supprimer les fichiers PST rencontrées lorsque vous exécutez l’outil pour rechercher les fichiers PST. Le nom du travail sera également figurer dans les noms de fichiers journaux et de configuration.  <br/> | `-JobName PstSearch1` <br/> |
    | `Locations` <br/> | Spécifie un ou plusieurs emplacements pour rechercher des fichiers PST. Si vous spécifiez plusieurs emplacements, utilisez un point-virgule ( ;) pour séparer les emplacements spécifiques. Veillez à entourer les valeurs individuelles de ce paramètre avec des guillemets (« »).<br/><br/>   Voici le format de la valeur identity requis pour les types d’emplacements que vous pouvez rechercher.  <br/><br/>        **Unités d’organisation** - utilisez le nom unique (DN) pour identifier des unités d’organisation ; par exemple :`"OU=NorthAmerica,OU=NWRegion,OU=ITServices,DC=contoso,DC=com"` <br/> > [!IMPORTANT]> Vous ne pouvez pas spécifier le conteneur ordinateurs intégré (par exemple, CN = Computers, DC = contoso, DC = com »), car il n’est pas une unité d’organisation.<br/> <br/> **Ordinateurs** - utilisez le nom de domaine ou le nom de domaine complet (FQDN) pour identifier les ordinateurs clients et serveurs sur le réseau. par exemple :  <br/>  NOM UNIQUE :`"CN=FILESERVER01,CN=Computers,DC=contoso,DC=com"` <br/>  Ou  <br/>  NOM DE DOMAINE COMPLET :`"FILESERVER01.contoso.com"` <br/><br/>  **Partages de fichiers réseau** : utilisez un nom UNC pour identifier les partages de fichiers réseau ; par exemple,`"\\FILESERVER02\Users"` <br/> | `-Locations "CN=FILESERVER01,CN=Computers,DC=contoso,DC=com";"CN=FILESERVER02,CN=Computers,DC=contoso,DC=com"` <br/> |
    | `LogLocation` <br/> |Spécifie le dossier pour les fichiers journaux sont copiées. Si le dossier n’existe pas, il est créé lorsque vous exécutez l’outil.  <br/> | `-LogLocation "c:\users\admin\desktop\PSTCollection"` <br/> |
    | `ConfigurationLocation` <br/> |Spécifie le dossier qui est copié vers le fichier de configuration .xml. Ce fichier contient des informations sur chaque fichier PST trouvé lorsque vous exécutez l’outil. Ce fichier sera utilisé lorsque vous exécutez l’outil à l’étape 3 pour copier les fichiers PST qui sont trouvent.  <br/> | `-ConfigurationLocation "c:\users\admin\desktop\PSTCollection\Configuration"` <br/> |
    | `ExcludedLocations` <br/> |Ce paramètre facultatif spécifie les emplacements à ignorer pendant une opération de recherche. Vous pouvez exclure des unités d’organisation, les ordinateurs et les partages de fichiers réseau. Par exemple, vous pouvez exclure des ordinateurs, tels que les ordinateurs configurés en tant que SQL server (ou autres types de serveurs d’applications), que les utilisateurs n’ont pas accès. Si vous spécifiez plusieurs emplacements à exclure, utilisez un point-virgule ( ;) pour séparer les emplacements spécifiques. Veillez à entourer les valeurs individuelles de ce paramètre avec des guillemets (« »).  <br/> | `-ExcludedLocations "SQLSERVER01.contoso.com"` <br/> |
    | `ForceRestart` <br/> |Ce commutateur facultatif vous permet d’exécuter l’outil en mode de recherche d’un projet existant de la Collection PST. Lorsque vous utilisez la `ForceRestart` passer, les résultats de l’opération de recherche précédente pour le travail sera ignoré, et l’outil analyser à nouveau les emplacements spécifiés et créent des fichiers journaux et de configuration.<br/> | `-ForceRestart` <br/> |
   
    Voici un exemple de la syntaxe de la commande DataCollectorMaster.exe à l’aide des valeurs réelles pour chaque paramètre :
    
    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Find -JobName PstSearch1 -Locations "CN=FILESERVER01,CN=Computers,DC=contoso,DC=com";"CN=FILESERVER02,CN=Computers,DC=contoso,DC=com" -LogLocation "c:\users\admin\desktop\PSTCollection" -ConfigurationLocation "c:\users\admin\desktop\PSTCollection\Configuration"
    ```

    Après avoir exécuté la commande, messages d’état détaillés sont affichent qui indiquent la progression de la recherche de fichiers PST dans les emplacements spécifiés. Après un certain temps, un message d’état final indique le nombre total de fichiers PST qui ont été détectés, si le travail est terminé et si il y avait des erreurs. Les messages d’état sont copiés dans le fichier .log.
    
### <a name="results-of-running-datacollectormasterexe-in-the-find-mode"></a>Résultats de l’exécution DataCollectorMaster.exe dans le mode de recherche

Après avoir exécuté correctement l’outil PST Collection le mode de recherche, les fichiers suivants sont créés et stockés dans les dossiers spécifiés par le `LogLocation` et `ConfigurationLocation` paramètres. 
  
- **\<JobName\>_trouver_\<DateTimeStamp\>.log** -le fichier journal contient les messages d’état qui ont été affichés. Ce fichier est créé dans le dossier spécifié par le `LogLocation` paramètre. 
    
- **\<JobName\>_trouver_\<DateTimeStamp\>.csv** -fichier CSV la contient une ligne pour chaque fichier PST qui a été trouvé. Les informations pour chaque PST incluent l’ordinateur où le fichier a été trouvée, le chemin d’accès complet du fichier PST, le propriétaire du fichier PST et la taille (en kilo-octets, Kbits/s) du fichier PST. Ce fichier est créé dans le dossier spécifié par le `LogLocation` paramètre. 
    
    > [!TIP]
    > Utilisez l’outil Somme automatique dans Excel pour calculer la taille totale (en Ko) de tous les fichiers PST répertoriés dans le fichier CSV. Ensuite, vous pouvez utiliser un calculateur de conversion pour convertir la taille totale en méga-octets (Mo) ou gigaoctets (Go). 
  
- **\<JobName\>_trouver_\<DateTimeStamp\>.xml** -le fichier XML contient des informations sur les valeurs de paramètre qui où utilisées lorsque vous avez exécuté l’outil en mode de recherche. Ce fichier contient également des informations sur tous les fichiers PST qui a été trouvé. Les données dans ce fichier sont utilisées lorsque vous exécutez réexécuter l’outil pour la même tâche sur block, collecter ou supprimer le fichier PST les fichiers qui ont été détectés. Ce fichier est créé dans le dossier spécifié par le `ConfigurationLocation` paramètre. 
    
    > [!IMPORTANT]
    > Ne pas renommer, modifier ou déplacer ce fichier. Il est utilisé par l’outil PST Collection lorsque vous réexécutez l’outil dans le bloc, copie, ou supprimez le mode de la même tâche. 

## <a name="optional-step-2-control-access-to-pst-files"></a>(Facultatif) Étape 2 : Contrôler l’accès aux fichiers PST

Cette étape facultative vous permet de « verrouiller » les fichiers PST qui ont été détectés à l’étape 1 de sorte que vous pouvez collecter et importer un ensemble donné de PST fichiers vers Office 365. Lorsque vous exécutez l’outil de collecte de PST en mode bloc, les événements suivants se produisent : 
  
- L’outil crée un objet de stratégie de groupe (GPO) nommé *PST l’utilisation de contrôles* . Cet objet de stratégie de groupe est lié à votre domaine et s’applique à tous les utilisateurs authentifiés dans votre organisation. 
    
- La stratégie de groupe PST l’utilisation de contrôles crée les paramètres de Registre sur les ordinateurs de votre organisation. Selon le paramètre que vous utilisez, vous pouvez créer un paramètre de Registre pour empêcher les utilisateurs de créer de nouveaux fichiers PST et un paramètre de Registre qui empêche les utilisateurs de modifier des fichiers PST.
    
> [!NOTE]
> Si le contrôle d’accès aux fichiers PST est trop gênants pour votre organisation, vous pouvez envisager, ignorez cette étape et effectue l’étape 3 pour copier des fichiers PST dans un emplacement central. Puis répétez l’étape 1 de la même tâche (à l’aide de la `ForceRestart` paramètre) pour rechercher les fichiers pst supplémentaires qui ont été créées après que vous avez copié les fichiers PST à l’emplacement de la collection. Si les nouveaux fichiers PST sont détectés, vous pouvez les copier à l’emplacement de la collection. Lorsque vous utilisez la `ForceRestart` paramètre lorsque vous réexécutez l’outil en mode de recherche, les résultats de l’opération de recherche précédente d’un travail seront ignorées et l’outil d’analyse à nouveau les emplacements spécifiés. 

Pour bloquer l’accès aux fichiers PST :

1. Ouvrez une invite de commandes (exécuter en tant qu’administrateur) sur votre ordinateur local.
    
2. Accédez au répertoire où vous avez téléchargé l’outil PST Collection.
    
3. Exécutez la commande suivante pour bloquer l’accès aux fichiers PST trouvé à l’étape 1.

    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Block -JobName <Name of job from Step 1> -ConfigurationLocation <Location of configuration files from Step 1> -BlockChangesToFiles -BlockNewFiles
    ```

    Le tableau suivant décrit les paramètres et leurs valeurs requis lorsque vous exécutez la commande DataCollectorMaster.exe pour bloquer la création et la modification des fichiers PST. 
    
    |Paramètre ***|****Description****|Exemples ***|
    |:-----|:-----|:-----|
    | `DataSource` <br/> |Spécifie le type de données à rechercher. Actuellement, vous pouvez utiliser l’outil de collecte de PST pour rechercher des fichiers PST.  <br/> | `-DataSource Pst` <br/> |
    | `Mode` <br/> |Spécifie le type d’opération qui exécute l’outil. Utilisez la valeur `Block` pour empêcher les utilisateurs de créer de nouveaux fichiers PST et apporter des modifications aux fichiers PST existants.<br/> | `-Mode Block` <br/> |
    | `JobName` <br/> |Spécifie le nom d’un travail existant de la Collection PST. Vous devez utiliser ce même nom de travail que vous avez utilisé lorsque vous avez exécuté l’outil en mode de recherche à l’étape 1. Ce nom de la tâche est également ajouté au nom du fichier journal qui est créé lorsque vous exécutez l’outil en mode bloc.  <br/> | `-JobName PstSearch1` <br/> |
    | `ConfigurationLocation` <br/> |Spécifie que le dossier contient le fichier de configuration .xml qui a été créé lorsque vous avez exécuté l’outil en mode de recherche. Utilisez la même valeur que vous avez utilisé pour ce paramètre à l’étape 1.  <br/> | `-ConfigurationLocation "c:\users\admin\desktop\PSTCollection\Configuration"` <br/> |
    | `LogLocation` <br/> |Spécifie le dossier qui est copié vers le fichier journal pour l’opération de bloc. Il s’agit d’un paramètre facultatif. Si vous ne le sont pas, le fichier journal est copié dans le dossier où vous avez téléchargé l’outil PST Collection. Envisagez d’utiliser le même emplacement de journal que vous avez utilisé lorsque vous avez exécuté l’outil en mode de recherche à l’étape 1 afin que tous les fichiers journaux sont enregistrés dans le même dossier.  <br/> | `-LogLocation "c:\users\admin\desktop\PSTCollection"` <br/> |
    | `BlockChangesToFiles` <br/> |Utilisez ce commutateur pour empêcher les utilisateurs de modifier un fichier PST. Lorsque vous utilisez ce commutateur, l’entrée de Registre suivante est créée : `HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\<version>\Outlook\PST\PstDisableGrow` et la valeur des données est définie sur 1. Ce paramètre de Registre est créé sur les ordinateurs de votre organisation par la stratégie de groupe est créé lorsque vous exécutez l’outil de collecte de PST en mode bloc.<br/> | `-BlockChangesToFiles` <br/> |
    | `BlockNewFiles` <br/> |Utilisez ce commutateur pour empêcher les utilisateurs de la création de nouveaux fichiers PST, l’ouverture et l’importation des fichiers PST à Outlook et exportation de fichiers PST d’Outlook. Lorsque vous utilisez ce commutateur, l’entrée de Registre suivante est créée : `HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\<version>\Outlook\DisablePst` et la valeur des données est définie sur 1. Ce paramètre de Registre est créé sur les ordinateurs de votre organisation par la stratégie de groupe est créé lorsque vous exécutez l’outil de collecte de PST en mode bloc.<br/> | `-BlockNewFiles` <br/> |
   
    Voici un exemple de la syntaxe de la commande DataCollectorMaster.exe à l’aide des valeurs réelles pour chaque paramètre :

    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Block -JobName PstSearch1 -ConfigurationLocation "c:\users\admin\desktop\PSTCollection\Configuration" -LogLocation "c:\users\admin\desktop\PSTCollection" -BlockChangesToFiles -BlockNewFiles
    ```
    
    Vous êtes invité à confirmer que vous souhaitez bloquer les nouveaux fichiers PST ou les modifications apportées aux fichiers PST existants. Une fois que vous confirmez que vous souhaitez continuer et que la commande s’exécute correctement, un message s’affiche indiquant qu’un nouvel objet GPO, nommé « PST l’utilisation de contrôles », a été créé.
    
## <a name="step-3-copy-the-pst-files-to-a-collection-location"></a>Étape 3 : Copier les fichiers PST vers un emplacement de la collection

L’étape suivante consiste à copier le fichier PST où trouver lorsque vous avez exécuté l’outil PST Collection dans le mode de recherche de fichiers. Cela vous permet de collecter les fichiers PST au même emplacement afin que vous pouvez les importer ultérieurement à Office 365. Avant de copier les fichiers PST à l’emplacement de la collection, envisagez de déterminer la quantité totale d’espace de stockage est nécessaire. Vous pouvez le faire à l’aide du fichier CSV qui a été créé à l’étape 1 pour calculer la taille totale de tous les fichiers PST.
  
> [!NOTE]
> Une fois que vous avez importé les fichiers PST vers Office 365 et supprimés de leur emplacement d’origine, vous pouvez souhaiter supprimer de l’emplacement de la collection que vous avez copié les dans cette étape. 
  
1. Ouvrez une invite de commandes (exécuter en tant qu’administrateur) sur votre ordinateur local.
    
2. Accédez au répertoire où vous avez téléchargé l’outil PST Collection.
    
3. Exécutez la commande suivante pour copier les fichiers PST vers un emplacement spécifié.
    
    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Collect -JobName <Name of job from Step 1> -Locations <same locations from Step 1> -ConfigurationLocation <Location of configuration files from Step 1> -CopyLocation <Location to copy PST files to>
    ```

    Le tableau suivant décrit les paramètres et leurs valeurs requis lorsque vous exécutez la commande DataCollectorMaster.exe pour copier les fichiers PST. 
    
    |Paramètre ***|****Description****|Exemples ***|
    |:-----|:-----|:-----|
    | `DataSource` <br/> |Spécifie le type de données à rechercher. Actuellement, vous pouvez utiliser l’outil de collecte de PST pour rechercher des fichiers PST.  <br/> | `-DataSource Pst` <br/> |
    | `Mode` <br/> |Spécifie le type d’opération qui exécute l’outil. Utilisez la valeur `Collect` pour copier que les fichiers PST qui ont été détectés lors de l’exécution de l’outil en mode de recherche. Notez que l’outil est en mesure de copier les fichiers de PST ouverts dans Outlook et copient les fichiers PST qui sont reliés aux profils Outlook.<br/> | `-Mode Collect` <br/> |
    | `JobName` <br/> |Spécifie le nom d’un travail existant de la Collection PST. Vous devez utiliser ce même nom de travail que vous avez utilisé lorsque vous avez exécuté l’outil en mode de recherche à l’étape 1. Ce nom de la tâche est également ajouté au nom du fichier journal qui est créé lorsque vous exécutez l’outil en mode de Collect.  <br/> | `-JobName PstSearch1` <br/> |
    | `Locations` <br/> |Utilisez la même valeur que vous avez utilisé pour le `Locations` paramètre à l’étape 1. Vous avez inclure ce paramètre lorsque vous exécutez l’outil en mode de Collect si vous souhaitez exécuter à nouveau l’outil pour supprimer les fichiers PST de leur emplacement d’origine à l’étape 5.<br/> | `-Locations "CN=FILESERVER01,CN=Computers,DC=contoso,DC=com"; "CN=FILESERVER02,CN=Computers,DC=contoso,DC=com"` <br/> |
    | `ConfigurationLocation` <br/> |Spécifie le dossier qui contient le fichier de configuration .xml qui a été créé lorsque vous avez exécuté l’outil en mode de recherche. Utilisez la même valeur que vous avez utilisé pour ce paramètre à l’étape 1.  <br/> | `-ConfigurationLocation "c:\users\admin\desktop \PSTCollection\Configuration"` <br/> |
    | `CopyLocation` <br/> |Spécifie l’emplacement de la collection où vous souhaitez copier les fichiers PST. Vous pouvez copier les fichiers sur un serveur de fichiers, d’un partage de fichiers réseau ou d’un disque dur. L’emplacement doit exister avant d’exécuter l’outil en mode de Collect. L’outil ne crée pas de l’emplacement et renvoie une erreur indiquant qu’il n’existe pas.  <br/> En outre, vous devez écrire des autorisations à l’emplacement de la collection spécifié par ce paramètre.  <br/> | `-CopyLocation "\\FILESERVER03\PSTs"` <br/> |
    | `LogLocation` <br/> |Spécifie le dossier qui est copié vers le fichier journal pour le mode de Collect. Il s’agit d’un paramètre facultatif. Si vous ne le sont pas, le fichier journal est copié dans le dossier où vous avez téléchargé l’outil PST Collection. Envisagez d’utiliser le même emplacement de journal que vous avez utilisé lorsque vous avez exécuté l’outil en mode de recherche à l’étape 1 afin que tous les fichiers journaux sont enregistrés dans le même dossier.  <br/> | `-LogLocation "c:\users\admin\desktop\PSTCollection"` <br/> |
    | `ForceRestart` <br/> |Ce commutateur facultatif vous permet de réexécuter l’outil dans le mode de collecte d’un projet existant de la Collection PST. Si vous exécutiez l’outil en mode de Collect, mais a exécuté l’outil de nouveau dans le mode de recherche avec le `ForceRestart` commutateur pour analyser à nouveau les emplacements des fichiers PST, vous pouvez utiliser ce commutateur pour réexécuter l’outil en mode de collecte et nouveau copier les fichiers PST il ont été trouvée lorsque votre réanalysés les emplacements. Lorsque vous utilisez la `ForceRestart` commutateur en mode de collecte, l’outil ignore toutes les opérations précédentes Collection et tente de copier les fichiers PST à partir de zéro.<br/> | `-ForceRestart` <br/> |
   
    Voici un exemple de la syntaxe de l’outil DataCollectorMaster.exe à l’aide des valeurs réelles pour chaque paramètre :
    
    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Collect -JobName PstSearch1 -Locations "CN=FILESERVER01,CN=Computers,DC=contoso,DC=com";"CN=FILESERVER02,CN=Computers,DC=contoso,DC=com" -ConfigurationLocation "c:\users\admin\desktop\PSTCollection\Configuration" -CopyLocation "\\FILESERVER03\PSTs" -LogLocation "c:\users\admin\desktop\PSTCollection"
    ```

    Après avoir exécuté la commande, les messages d’état détaillés sont affichées qui affichent la progression de la collecte les fichiers PST qui ont été détectés à l’étape 1. Après un certain temps, un message d’état final indique si consignant les erreurs et l’emplacement du journal est copié dans. Les messages d’état sont copiés dans le fichier .log.
    
### <a name="results-of-running-datacollectormasterexe-in-the-collect-mode"></a>Résultats de l’exécution DataCollectorMaster.exe dans le mode de Collect

Après avoir exécuté correctement DataCollectorMaster.exe dans le mode de Collect, les fichiers suivants sont créés et stockés dans les dossiers spécifiés par le `LogLocation` et `ConfigurationLocation` paramètres. 
  
- **\<JobName\>_collecter_\<DateTimeStamp\>.log** -le fichier journal contient les messages d’état qui ont été affichés. Ce fichier est créé dans le dossier spécifié par le `LogLocation` paramètre. 
    
- **\<JobName\>_collecter_\<DateTimeStamp\>.xml** -le fichier XML contient uniquement des informations sur les valeurs de paramètre où utilisées par l’outil a été exécuté dans le mode de Collect. Les données dans ce fichier sont utilisées lorsque vous exécutez réexécuter l’outil DataCollectorMaster.exe pour supprimer les fichiers PST ; consultez [l’étape 5](#step-5-delete-the-pst-files-found-on-your-network).
    

## <a name="step-4-import-the-pst-files-to-office-365"></a>Étape 4 : Importer les fichiers PST vers Office 365

Une fois que vous avez collecté les fichiers PST trouvés à l’étape 1, l’étape suivante consiste à les importer dans les boîtes aux lettres dans Office 365. Dans le cadre ou le processus d’importation, vous devrez créer un fichier de mappage CSV qui contient une ligne de chaque fichier PST que vous souhaitez importer. Informations de chaque ligne spécifie le nom du fichier PST, adresse de messagerie de l’utilisateur et si vous souhaitez importer le fichier PST à l’utilisateur principale ou archiver des boîtes aux lettres. Utilisez les informations contenues dans le **JobName\>_trouver_\<DateTimeStamp.csv** fichier (créé à l’étape) 1 pour vous aider à créer le fichier de mappage CSV. 
  
Pour obtenir des instructions pas à pas importer des fichiers PST vers Office 365, consultez les rubriques suivantes :
  
- [Utiliser le chargement réseau pour importer des fichiers PST vers Office 365](use-network-upload-to-import-pst-files.md)
    
- [Utiliser l’expédition de disque pour importer des fichiers PST dans Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md)
    

## <a name="step-5-delete-the-pst-files-found-on-your-network"></a>Étape 5 : Supprimer les fichiers PST détectés sur votre réseau

Une fois que les fichiers PST que vous avez trouvé et collectées ont été importés vers des boîtes aux lettres Exchange Online dans Office 365, vous pouvez utiliser l’outil de collecte de PST pour supprimer les fichiers PST de l’emplacement source d’origine où ils ont été trouvées dans l’étape 1. 
  
1. Ouvrez une invite de commandes (exécuter en tant qu’administrateur) sur votre ordinateur local.
    
2. Accédez au répertoire où vous avez téléchargé l’outil PST Collection.
    
3. Exécutez la commande suivante pour supprimer les fichiers PST.

    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Delete -JobName <Name of job from Step 1> -ConfigurationLocation <Location of configuration files from Step 1> -CopyLocation <Location to copy PST files to>
    ```

    Le tableau suivant décrit les paramètres et leurs valeurs requis lorsque vous exécutez la commande DataCollectorMaster.exe pour supprimer les fichiers PST. 
    
    |Paramètre ***|****Description****|Exemples ***|
    |:-----|:-----|:-----|
    | `DataSource` <br/> |Spécifie le type de données à rechercher. Actuellement, vous pouvez utiliser l’outil de collecte de PST pour rechercher des fichiers PST. ![espacement](media/b078d05c-3aee-4b9f-8805-6a8a9d8970ee.png)           <br/> | `-DataSource Pst` <br/> |
    | `Mode` <br/> |Spécifie le type d’opération qui exécute l’outil. Utilisez la valeur `Delete` supprimer que les fichiers PST qui ont été détectés lors de l’exécution de l’outil en mode de recherche.<br/> | `-Mode Delete` <br/> |
    | `JobName` <br/> |Spécifie le nom d’un travail existant de la Collection PST. Vous devez utiliser ce même nom de travail que vous avez utilisé lorsque vous avez exécuté l’outil dans le mode de recherche et le mode de Collect dans l’étape 1 et l’étape 3. Ce nom de la tâche est également ajouté au nom du fichier journal qui est créé lorsque vous exécutez l’outil en mode de suppression.  <br/> | `-JobName PstSearch1` <br/> |
    | `ConfigurationLocation` <br/> |Spécifie le dossier qui contient le fichier de configuration .xml qui a été créé lorsque vous avez exécuté l’outil en mode de Collect. Utilisez la même valeur que vous avez utilisé pour ce paramètre à l’étape 3.  <br/> | `-ConfigurationLocation "c:\users\admin\ desktop\PSTCollection\Configuration"` <br/> |
    | `LogLocation` <br/> |Spécifie le dossier qui est copié vers le fichier journal pour le mode de suppression. Il s’agit d’un paramètre facultatif. Si vous ne le sont pas, le fichier journal est copié dans le dossier où vous avez téléchargé l’outil PST Collection. Envisagez d’utiliser le même emplacement de journal que vous avez utilisé lorsque vous avez exécuté l’outil dans la recherche et les modes collecter dans l’étape 1 et l’étape 3 afin que tous les fichiers journaux sont enregistrés dans le même dossier.  <br/> | `-LogLocation "c:\users\admin\desktop\PSTCollection"` <br/> |
    | `ForceRestart` <br/> |Ce commutateur facultatif vous permet de réexécuter l’outil dans le mode de suppression d’un projet existant de la Collection PST. Si vous exécutiez l’outil en mode de suppression, mais a exécuté l’outil de nouveau dans le mode de recherche avec le `ForceRestart` commutateur pour analyser à nouveau les emplacements des fichiers PST, vous pouvez utiliser ce commutateur pour réexécuter l’outil en mode suppression et supprimer les fichiers PST il ont été trouvée lorsque votre re-sca nned les emplacements. Lorsque vous utilisez la `ForceRestart` commutateur en mode de suppression, l’outil ignore toutes les opérations Delete précédentes et tente de supprimer les fichiers PST à nouveau.<br/> | `-ForceRestart` <br/> 

    Voici un exemple de la syntaxe de l’outil DataCollectorMaster.exe à l’aide des valeurs réelles pour chaque paramètre :
    
    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Delete -JobName PstSearch1 -ConfigurationLocation "c:\users\admin\desktop\PSTCollection\Configuration" -LogLocation "c:\users\admin\desktop\PSTCollection"
    ```
   
    Après avoir exécuté la commande, messages d’état détaillés sont affichent qui indiquent la progression de la suppression des fichiers PST qui ont été trouvés à l’étape 1 et collectées à l’étape 3. Après un certain temps, un message d’état final indique si consignant les erreurs et l’emplacement du journal est copié dans. Les messages d’état sont copiés dans le fichier .log.
    
### <a name="results-of-running-datacollectormasterexe-in-the-delete-mode"></a>Résultats de l’exécution DataCollectorMaster.exe dans le mode de suppression

Après avoir exécuté correctement DataCollectorMaster.exe dans le mode de suppression, les fichiers suivants sont créés et stockés dans le dossier spécifié par le `LogLocation` et `ConfigurationLocation` paramètres. 
  
- **\<JobName\>_Supprimer_\<DateTimeStamp\>.log** -le fichier journal contient les messages d’état qui ont été affichés. Ce fichier est créé dans le dossier spécifié par le `LogLocation` paramètre. 
    
- **\<JobName\>_Supprimer_\<DateTimeStamp\>.xml** -le fichier XML contient uniquement des informations sur les valeurs de paramètre où utilisées par l’outil a été exécuté dans le mode de suppression. Il indique également le nom et le chemin d’accès de chaque fichier PST qui a été supprimé. Ce fichier est créé dans le dossier spécifié par le `ConfigurationLocation` paramètre. 
