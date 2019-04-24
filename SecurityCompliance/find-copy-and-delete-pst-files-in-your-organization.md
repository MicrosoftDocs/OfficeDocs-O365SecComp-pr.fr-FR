---
title: Utiliser l'outil de collecte PST pour rechercher, copier et supprimer des fichiers PST dans votre organisation
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: ''
search.appverid: MOE150
ms.assetid: 7a150c84-049c-4a9c-8c91-22355b35f2a7
description: Utilisez l'outil de collection Microsoft PST pour effectuer des recherches sur le réseau de votre organisation afin d'obtenir un inventaire des fichiers PST disséminés au sein de votre organisation. Une fois que vous avez trouvé des fichiers PST, vous pouvez utiliser l'outil de collecte PST pour les copier dans un emplacement central afin de pouvoir les importer dans Office 365.
ms.openlocfilehash: 87e13ec8a4c58f848ac2ff7a430a7532942ece74
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32255340"
---
# <a name="use-the-pst-collection-tool-to-find-copy-and-delete-pst-files-in-your-organization"></a>Utiliser l'outil de collecte PST pour rechercher, copier et supprimer des fichiers PST dans votre organisation

> [!IMPORTANT]
> L'outil de collecte PST décrit dans cet article n'est pas pris en charge dans les services ou programmes de support standard Microsoft. L'outil est fourni en l'État sans aucune garantie. Microsoft exclut toute garantie implicite, y compris, sans limitation, les garanties implicites de qualité marchande ou d'adéquation à un usage particulier. L'ensemble des risques liés à l'utilisation ou aux performances de l'outil et de la documentation vous incombe. En aucun cas Microsoft, ses auteurs ou toute personne impliquée dans la création, la production ou la livraison de l'outil ne sont responsables de quelque dommage que ce soit (y compris, sans s'y limiter, les dommages pour les pertes de bénéfices, les interruptions d'entreprise, la perte de les informations professionnelles, ou toute autre perte de façon pécuniaire, découlant de l'utilisation ou de l'impossibilité d'utiliser l'outil ou la documentation, même si Microsoft a été avisé de la possibilité de tels dommages.

Vous pouvez utiliser l'outil de collection Microsoft PST pour rechercher des fichiers PST dans le réseau de votre organisation. L'outil vous permet d'obtenir un inventaire des fichiers PST disséminés dans l'ensemble de votre organisation. Une fois que vous avez trouvé des fichiers PST, vous pouvez utiliser l'outil de collecte PST pour les copier à un emplacement central. Le fait d'avoir des fichiers PST en un seul endroit vous permet de les importer dans les boîtes aux lettres Exchange Online (ou dans une seule boîte aux lettres Exchange Online), où vous pouvez ensuite appliquer l'ensemble complet de fonctionnalités de conformité dans Office 365. Cela inclut l'importation de fichiers PST dans les boîtes aux lettres d'archivage des utilisateurs, la recherche de messages spécifiques dans les fichiers PST que vous avez importés à l'aide des outils de recherche eDiscovery, la conservation des messages à l'aide de conservations eDiscovery et de stratégies de rétention Office 365 et la gestion de la vie cycle de ces messages à l'aide des fonctionnalités de gestion des enregistrements de messagerie dans Exchange Online. Une fois que vous êtes certain que les fichiers PST que vous avez collectés ont été correctement importés dans Office 365, vous pouvez utiliser l'outil pour les supprimer de leur emplacement d'origine sur votre réseau. 
  
Vous pouvez également faire en sorte que l'outil de collection PST empêche les utilisateurs de créer de nouveaux fichiers PST et de modifier les fichiers PST existants que vous trouvez sur votre réseau. Ces fonctionnalités de «blocage» vous permettent de rechercher, de collecter et d'importer un ensemble connu de fichiers PST dans Office 365 et d'empêcher la prolifération future de fichiers PST dans votre organisation. 
  
## <a name="how-the-pst-collection-tool-works"></a>Fonctionnement de l'outil de collecte PST

Voici une présentation rapide du processus d'utilisation de l'outil de collecte PST pour rechercher, contrôler, collecter et supprimer des fichiers PST dans votre organisation.
  
![Vue d'ensemble du processus de l'outil de collecte PST](media/67a29f27-f83c-4f0a-9df4-7ed92d3086fe.png)
  
1. **[Étape 1: trouver des fichiers PST sur votre réseau](#step-1-find-pst-files-on-your-network)** : lorsque vous exécutez l'outil pour rechercher des fichiers PST, vous spécifiez un emplacement, tel qu'une unité d'organisation qui contient des objets Active Directory pour les ordinateurs clients et serveurs. Vous pouvez également rechercher des ordinateurs spécifiques ou des partages de fichiers réseau. Lorsque vous exécutez l'outil, un agent de collection «léger» est installé sur les ordinateurs cibles. Cet agent recherche des fichiers PST sur l'ordinateur cible, puis renvoie les informations à l'outil de collecte PST à propos de n'importe quel fichier PST qu'il trouve. L'outil crée des fichiers journaux qui contiennent des informations sur les fichiers PST qui se trouvaient aux emplacements spécifiés. Ces fichiers sont utilisés lors de l'exécution de l'outil dans les étapes ultérieures. 
    
2. **[Étape 2 (facultatif): contrôler l'accès aux fichiers PST](#optional-step-2-control-access-to-pst-files)** : l'outil crée un objet de stratégie de groupe (GPO) avec des paramètres qui empêchent les utilisateurs de créer ou de modifier des fichiers PST. Cet objet de stratégie de groupe est appliqué à tous les utilisateurs de votre domaine. Cette étape facultative vous permet de «verrouiller» les fichiers PST trouvés à l'étape 1, afin que vous puissiez les collecter, les importer et les supprimer sans avoir créé de nouveaux fichiers PST ou modifié les fichiers PST existants. 
    
3. **[Étape 3: copier les fichiers PST vers un emplacement de collection](#step-3-copy-the-pst-files-to-a-collection-location)** : cela vous permet de collecter les fichiers PST à un emplacement afin de pouvoir les importer dans les boîtes aux lettres Exchange Online à l'aide du service d'importation Office 365 à l'étape 4. Lorsque vous exécutez l'outil en mode «collecte», chaque agent de collection copie les fichiers PST à partir de l'ordinateur cible sur lequel l'agent est installé sur l'emplacement de la collection. 
    
4. **[Étape 4: importer les fichiers PST dans Office 365](#step-4-import-the-pst-files-to-office-365)** -une fois que vous avez copié les fichiers PST dans un emplacement, vous êtes prêt à les importer dans les boîtes aux lettres Exchange Online. 
    
5. **[Étape 5: suppression des fichiers PST trouvés sur votre réseau](#step-5-delete-the-pst-files-found-on-your-network)** : une fois que les fichiers PST que vous avez trouvés et collectés ont été importés dans les boîtes aux lettres Exchange Online dans Office 365, vous pouvez utiliser l'outil de collecte PST pour supprimer les fichiers PST des emplacements d'origine où ils ont été trouvés à l'étape 1. 

## <a name="before-you-begin"></a>Avant de commencer

- Procédez comme suit pour télécharger l'outil de collecte PST sur votre ordinateur local. 
    
    1. [Téléchargez l'outil de collection PST](https://aka.ms/pstcollectiontool).
    
    2. Dans la fenêtre contextuelle, cliquez sur **Enregistrer** \> **Enregistrer sous** pour enregistrer le fichier PSTCollectionTool. zip dans un dossier sur votre ordinateur local. 
    
    3. ExTrayez le fichier PSTCollectionTool. zip dans un dossier sur votre ordinateur local; le nom du dossier par défaut est PSTCollectionTool.
    
- Pour exécuter l'outil de collecte PST dans n'importe quel mode (Rechercher, bloquer, copier ou supprimer), vous devez être membre du groupe administrateurs de domaine dans votre domaine Active Directory. 

## <a name="step-1-find-pst-files-on-your-network"></a>Étape 1: trouver des fichiers PST sur votre réseau

La première étape consiste à exécuter l'outil de collecte PST pour rechercher des fichiers PST dans votre organisation. Vous pouvez utiliser l'outil pour effectuer des recherches dans les types d'emplacement suivants. 
  
- Unités d'organisation (UO) dans un domaine Active Directory local. L'outil recherche tous les ordinateurs qui sont contenus dans l'unité d'organisation spécifiée. 
    
- Ordinateurs client et serveur. L'outil recherche les ordinateurs spécifiés. 
    
- Partages de fichiers réseau. L'outil recherche les partages de fichiers réseau spécifiés. 
    
Pour obtenir des exemples de `Locations` syntaxe à utiliser pour chacun de ces types d'emplacement, voir la description du paramètre dans le tableau de la procédure suivante. 
  
> [!IMPORTANT]
> Vous devez exécuter l'outil de collecte PST dans le mode de recherche pour pouvoir effectuer d'autres actions telles que le blocage, la collecte ou la suppression des fichiers PST. 
  
1. Ouvrez une invite de commandes (exécuter en tant qu'administrateur) sur votre ordinateur local.
    
2. Accédez au dossier PSTCollectionTool (ou au dossier dans lequel vous avez extrait le fichier PSTCollectionTool. zip).
    
3. Accédez au répertoire DataCollectorMaster.
    
4. Exécutez la commande suivante pour rechercher les fichiers PST à un emplacement spécifié.
    
    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Find -JobName <Name> -Locations <Locations to search for PSTs> -LogLocation <Location to store log files> -ConfigurationLocation <Location to store configuration files>
    ```

    Le tableau suivant décrit les paramètres et leurs valeurs requises lors de l'exécution de la commande DataCollectorMaster. exe pour rechercher des fichiers PST. 
    
    |Paramètre * * * *|****Description****|Exemples * * * *|
    |:-----|:-----|:-----|
    | `DataSource` <br/> |Spécifie le type de données à rechercher. Actuellement, vous pouvez utiliser l'outil de collection PST pour rechercher des fichiers PST.  <br/> | `-DataSource Pst` <br/> |
    | `Mode` <br/> |Spécifie le type d'opération exécutée par l'outil. Utilisez la valeur `Find` pour localiser les fichiers PST aux emplacements spécifiés. Notez que l'outil peut trouver et obtenir des informations sur les fichiers PST ouverts dans des fichiers Outlook et PST qui sont connectés à des profils Outlook.  <br/> | `-Mode Find` <br/> |
    | `JobName` <br/> |Spécifie le nom du travail de collecte PST. Vous utiliserez ce même nom de travail lorsque vous exécuterez l'outil de collecte PST pour bloquer, collecter et supprimer les fichiers PST trouvés lors de l'exécution de l'outil pour rechercher des fichiers PST. Le nom du travail est également ajouté aux noms des fichiers journaux et de configuration.  <br/> | `-JobName PstSearch1` <br/> |
    | `Locations` <br/> | Spécifie un ou plusieurs emplacements dans lesquels rechercher des fichiers PST. Si vous spécifiez plusieurs emplacements, utilisez un point-virgule (;) pour séparer les emplacements individuels. Veillez à entourer les valeurs individuelles de ce paramètre de guillemets doubles ("").  <br/><br/>   Voici le format de valeur d'identité requis pour les types d'emplacement que vous pouvez rechercher.  <br/><br/>        **** Ou: utilisez le nom unique (DN) pour identifier les unités d'organisation; par exemple:`"OU=NorthAmerica,OU=NWRegion,OU=ITServices,DC=contoso,DC=com"` <br/> > [!IMPORTANT]> vous ne pouvez pas spécifier le conteneur d'ordinateurs intégré (par exemple, CN = Computers, DC = contoso, DC = com), car il ne s'agit pas d'une unité d'organisation.<br/> <br/> **Machines** : utilisez le DN ou le nom de domaine complet (FQDN) pour identifier les ordinateurs client et serveur sur votre réseau; par exemple:  <br/>  APPARENTÉ`"CN=FILESERVER01,CN=Computers,DC=contoso,DC=com"` <br/>  Ou  <br/>  QUALIFIÉ`"FILESERVER01.contoso.com"` <br/><br/>  **Partages de fichiers réseau** : utilisez un nom UNC pour identifier les partages de fichiers réseau; par exemple,`"\\FILESERVER02\Users"` <br/> | `-Locations "CN=FILESERVER01,CN=Computers,DC=contoso,DC=com";"CN=FILESERVER02,CN=Computers,DC=contoso,DC=com"` <br/> |
    | `LogLocation` <br/> |Spécifie le dossier dans lequel les fichiers journaux seront copiés. Si le dossier n'existe pas, il est créé lors de l'exécution de l'outil.  <br/> | `-LogLocation "c:\users\admin\desktop\PSTCollection"` <br/> |
    | `ConfigurationLocation` <br/> |Spécifie le dossier dans lequel le fichier de configuration. xml sera copié. Ce fichier contient des informations sur chaque fichier PST trouvé lors de l'exécution de l'outil. Ce fichier sera utilisé lors de l'exécution de l'outil à l'étape 3 pour copier les fichiers PST trouvés.  <br/> | `-ConfigurationLocation "c:\users\admin\desktop\PSTCollection\Configuration"` <br/> |
    | `ExcludedLocations` <br/> |Ce paramètre facultatif spécifie les emplacements à ignorer pendant une opération de recherche. Vous pouvez exclure des unités d'organisation, des ordinateurs et des partages de fichiers réseau spécifiques. Par exemple, vous pouvez exclure des ordinateurs, tels qu'un ordinateur configuré comme un serveur SQL (ou d'autres types de serveurs d'applications), auxquels les utilisateurs n'ont pas accès. Si vous spécifiez plusieurs emplacements à exclure, utilisez un point-virgule (;) pour séparer les emplacements individuels. Veillez à entourer les valeurs individuelles de ce paramètre de guillemets doubles ("").  <br/> | `-ExcludedLocations "SQLSERVER01.contoso.com"` <br/> |
    | `ForceRestart` <br/> |Ce commutateur facultatif vous permet d'exécuter l'outil dans le mode de recherche pour un travail de collection PST existant. Lorsque vous utilisez le `ForceRestart` commutateur, les résultats de l'opération de recherche précédente pour le travail sont ignorés, et l'outil analyse à nouveau les emplacements spécifiés et crée des fichiers journaux et de configuration.  <br/> | `-ForceRestart` <br/> |
   
    Voici un exemple de la syntaxe de la commande DataCollectorMaster. exe qui utilise les valeurs réelles de chaque paramètre:
    
    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Find -JobName PstSearch1 -Locations "CN=FILESERVER01,CN=Computers,DC=contoso,DC=com";"CN=FILESERVER02,CN=Computers,DC=contoso,DC=com" -LogLocation "c:\users\admin\desktop\PSTCollection" -ConfigurationLocation "c:\users\admin\desktop\PSTCollection\Configuration"
    ```

    Une fois la commande exécutée, des messages d'État détaillés s'affichent pour indiquer la progression de la recherche de fichiers PST aux emplacements spécifiés. Après un certain temps, un message d'état final indique le nombre total de fichiers PST qui ont été trouvés, si le travail est terminé et si des erreurs se sont produites. Les mêmes messages d'État sont copiés dans le fichier. log.
    
### <a name="results-of-running-datacollectormasterexe-in-the-find-mode"></a>Résultats de l'exécution de DataCollectorMaster. exe dans le mode de recherche

Après avoir exécuté l'outil de collecte PST avec succès le mode de recherche, les fichiers suivants sont créés et stockés dans les dossiers `LogLocation` spécifiés par les paramètres et `ConfigurationLocation` . 
  
- **\>__ JobName Rechercher\<DateTimeStamp\>. log: le fichier journal contient les messages \<** d'état affichés. Ce fichier est créé dans le dossier spécifié par le `LogLocation` paramètre. 
    
- **\>__ JobName Rechercher\<DateTimeStamp\>. csv: le fichier CSV contient une ligne pour chaque \<** fichier PST trouvé. Les informations de chaque fichier PST incluent l'ordinateur sur lequel le fichier PST a été trouvé, le chemin d'accès complet au fichier PST, le propriétaire du fichier PST et la taille (en kilo-octets, Ko) du fichier PST. Ce fichier est créé dans le dossier spécifié par le `LogLocation` paramètre. 
    
    > [!TIP]
    > Utilisez l'outil somme automatique dans Excel pour calculer la taille totale (en Ko) de tous les fichiers PST figurant dans le fichier CSV. Vous pouvez ensuite utiliser un calculateur de conversion pour convertir la taille totale en mégaoctets (Mo) ou gigaoctets (Go). 
  
- **\>__ JobName Rechercher\<DateTimeStamp\>. xml-le fichier XML contient des informations sur les valeurs des paramètres utilisées lors de l'exécution de l'outil dans le \<** mode de recherche. Ce fichier contient également des informations sur tous les fichiers PST qui ont été trouvés. Les données contenues dans ce fichier sont utilisées lorsque vous exécutez de nouveau l'outil pour le même travail pour bloquer, collecter ou supprimer les fichiers PST qui ont été trouvés. Ce fichier est créé dans le dossier spécifié par le `ConfigurationLocation` paramètre. 
    
    > [!IMPORTANT]
    > Ne renommez pas ce fichier, ne le modifiez pas ou ne le déplacez pas. Elle est utilisée par l'outil de collecte PST lorsque vous réexécutez l'outil en mode de bloc, de copie ou de suppression pour le même travail. 

## <a name="optional-step-2-control-access-to-pst-files"></a>Module Étape 2: contrôler l'accès aux fichiers PST

Cette étape facultative vous permet de «verrouiller» les fichiers PST qui ont été trouvés à l'étape 1 afin de pouvoir collecter et importer un ensemble connu de fichiers PST dans Office 365. Lorsque vous exécutez l'outil de collecte PST en mode de blocage, les événements suivants se produisent: 
  
- L'outil crée un objet de stratégie de groupe nommé *commandes d'utilisation PST* . Cet objet de stratégie de groupe est lié à votre domaine et s'applique à tous les utilisateurs authentifiés au sein de votre organisation. 
    
- L'objet de stratégie de groupe contrôles de l'utilisation PST crée des paramètres de Registre sur les ordinateurs de votre organisation. Selon le paramètre que vous utilisez, vous pouvez créer un paramètre de Registre pour empêcher les utilisateurs de créer des fichiers PST et un paramètre de Registre qui empêche les utilisateurs de modifier les fichiers PST existants.
    
> [!NOTE]
> Si le contrôle de l'accès aux fichiers PST est trop perturbant pour votre organisation, vous pouvez ignorer cette étape et effectuer l'étape 3 pour copier les fichiers PST vers un emplacement central. Vous pouvez ensuite répéter l'étape 1 pour le même travail (à l' `ForceRestart` aide du paramètre) pour rechercher des fichiers PST supplémentaires créés après avoir copié les fichiers PST à l'emplacement de la collection. Si de nouveaux fichiers PST sont trouvés, vous pouvez les copier à l'emplacement de la collection. Lorsque vous utilisez le `ForceRestart` paramètre lorsque vous réexécutez l'outil dans le mode de recherche, les résultats de l'opération de recherche précédente d'un travail sont ignorés et l'outil analyse à nouveau les emplacements spécifiés. 

Pour bloquer l'accès aux fichiers PST:

1. Ouvrez une invite de commandes (exécuter en tant qu'administrateur) sur votre ordinateur local.
    
2. Accédez au répertoire dans lequel vous avez téléchargé l'outil de collection PST dans.
    
3. Exécutez la commande suivante pour bloquer l'accès aux fichiers PST trouvés à l'étape 1.

    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Block -JobName <Name of job from Step 1> -ConfigurationLocation <Location of configuration files from Step 1> -BlockChangesToFiles -BlockNewFiles
    ```

    Le tableau suivant décrit les paramètres et leurs valeurs requises lors de l'exécution de la commande DataCollectorMaster. exe pour bloquer la création et la modification de fichiers PST. 
    
    |Paramètre * * * *|****Description****|Exemples * * * *|
    |:-----|:-----|:-----|
    | `DataSource` <br/> |Spécifie le type de données à rechercher. Actuellement, vous pouvez utiliser l'outil de collection PST pour rechercher des fichiers PST.  <br/> | `-DataSource Pst` <br/> |
    | `Mode` <br/> |Spécifie le type d'opération exécutée par l'outil. Utilisez la valeur `Block` pour empêcher les utilisateurs de créer de nouveaux fichiers PST et d'apporter des modifications aux fichiers PST existants.  <br/> | `-Mode Block` <br/> |
    | `JobName` <br/> |Spécifie le nom d'un travail de collection PST existant. Vous devez utiliser le même nom de travail que celui que vous avez utilisé lors de l'exécution de l'outil dans le mode de recherche à l'étape 1. Ce nom de travail est également ajouté au nom du fichier journal créé lors de l'exécution de l'outil en mode blocage.  <br/> | `-JobName PstSearch1` <br/> |
    | `ConfigurationLocation` <br/> |Spécifie que le dossier contient le fichier de configuration. XML qui a été créé lors de l'exécution de l'outil dans le mode de recherche. Utilisez la même valeur que celle que vous avez utilisée pour ce paramètre à l'étape 1.  <br/> | `-ConfigurationLocation "c:\users\admin\desktop\PSTCollection\Configuration"` <br/> |
    | `LogLocation` <br/> |Spécifie le dossier dans lequel le fichier journal de l'opération de blocage sera copié. Ce paramètre est facultatif. Si vous ne l'incluez pas, le fichier journal est copié dans le dossier dans lequel vous avez téléchargé l'outil de collecte PST. EnVisagez d'utiliser le même emplacement de journal que celui que vous avez utilisé lors de l'exécution de l'outil dans le mode de recherche à l'étape 1 afin que tous les fichiers journaux soient enregistrés dans le même dossier.  <br/> | `-LogLocation "c:\users\admin\desktop\PSTCollection"` <br/> |
    | `BlockChangesToFiles` <br/> |Utilisez ce commutateur pour empêcher les utilisateurs de modifier un fichier PST. Lorsque vous utilisez ce commutateur, l'entrée de Registre suivante est créée `HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\<version>\Outlook\PST\PstDisableGrow` : et la valeur de données est définie sur 1. Ce paramètre de Registre est créé sur les ordinateurs de votre organisation par l'objet de stratégie de groupe créé lorsque vous exécutez l'outil de collecte PST en mode de blocage.  <br/> | `-BlockChangesToFiles` <br/> |
    | `BlockNewFiles` <br/> |Utilisez ce commutateur pour empêcher les utilisateurs de créer de nouveaux fichiers PST, d'ouvrir et d'importer des fichiers PST dans Outlook et d'exporter des fichiers PST à partir d'Outlook. Lorsque vous utilisez ce commutateur, l'entrée de Registre suivante est créée `HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\<version>\Outlook\DisablePst` : et la valeur de données est définie sur 1. Ce paramètre de Registre est créé sur les ordinateurs de votre organisation par l'objet de stratégie de groupe créé lorsque vous exécutez l'outil de collecte PST en mode de blocage.  <br/> | `-BlockNewFiles` <br/> |
   
    Voici un exemple de la syntaxe de la commande DataCollectorMaster. exe qui utilise les valeurs réelles de chaque paramètre:

    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Block -JobName PstSearch1 -ConfigurationLocation "c:\users\admin\desktop\PSTCollection\Configuration" -LogLocation "c:\users\admin\desktop\PSTCollection" -BlockChangesToFiles -BlockNewFiles
    ```
    
    Vous êtes invité à confirmer que vous souhaitez bloquer les nouveaux fichiers PST ou les modifications apportées aux fichiers PST existants. Une fois que vous avez confirmé que vous souhaitez continuer et que la commande s'exécute correctement, un message s'affiche indiquant qu'un nouvel objet de stratégie de groupe nommé «contrôles d'utilisation PST» a été créé.
    
## <a name="step-3-copy-the-pst-files-to-a-collection-location"></a>Étape 3: copier les fichiers PST vers un emplacement de collection

L'étape suivante consiste à copier les fichiers PST qui se trouvent lors de l'exécution de l'outil de collecte PST dans le mode de recherche. Cela vous permet de collecter les fichiers PST à un emplacement afin de pouvoir les importer ultérieurement dans Office 365. Avant de copier les fichiers PST dans l'emplacement de la collection, pensez à déterminer la quantité totale d'espace de stockage requise. Pour ce faire, utilisez le fichier CSV qui a été créé à l'étape 1 pour calculer la taille totale de tous les fichiers PST.
  
> [!NOTE]
> Une fois que vous avez importé les fichiers PST dans Office 365 et que vous les avez supprimés de leur emplacement d'origine, vous pouvez les supprimer de l'emplacement de collection dans lequel vous les avez copiés à l'étape suivante. 
  
1. Ouvrez une invite de commandes (exécuter en tant qu'administrateur) sur votre ordinateur local.
    
2. Accédez au répertoire dans lequel vous avez téléchargé l'outil de collection PST dans.
    
3. Exécutez la commande suivante pour copier les fichiers PST vers un emplacement spécifié.
    
    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Collect -JobName <Name of job from Step 1> -Locations <same locations from Step 1> -ConfigurationLocation <Location of configuration files from Step 1> -CopyLocation <Location to copy PST files to>
    ```

    Le tableau suivant décrit les paramètres et leurs valeurs requises lors de l'exécution de la commande DataCollectorMaster. exe pour copier des fichiers PST. 
    
    |Paramètre * * * *|****Description****|Exemples * * * *|
    |:-----|:-----|:-----|
    | `DataSource` <br/> |Spécifie le type de données à rechercher. Actuellement, vous pouvez utiliser l'outil de collection PST pour rechercher des fichiers PST.  <br/> | `-DataSource Pst` <br/> |
    | `Mode` <br/> |Spécifie le type d'opération exécutée par l'outil. Utilisez la valeur `Collect` pour copier les fichiers PST qui ont été trouvés lors de l'exécution de l'outil dans le mode de recherche. Notez que l'outil permet de copier des fichiers PST ouverts dans Outlook et de copier des fichiers PST connectés à des profils Outlook.  <br/> | `-Mode Collect` <br/> |
    | `JobName` <br/> |Spécifie le nom d'un travail de collection PST existant. Vous devez utiliser le même nom de travail que celui que vous avez utilisé lors de l'exécution de l'outil dans le mode de recherche à l'étape 1. Ce nom de travail est également ajouté au nom du fichier journal créé lorsque vous exécutez l'outil en mode de collecte.  <br/> | `-JobName PstSearch1` <br/> |
    | `Locations` <br/> |Utilisez la même valeur que celle que vous avez `Locations` utilisée pour le paramètre à l'étape 1. Vous avez inclus ce paramètre lorsque vous exécutez l'outil en mode de collecte si vous voulez réexécuter l'outil pour supprimer les fichiers PST de leur emplacement source à l'étape 5.  <br/> | `-Locations "CN=FILESERVER01,CN=Computers,DC=contoso,DC=com"; "CN=FILESERVER02,CN=Computers,DC=contoso,DC=com"` <br/> |
    | `ConfigurationLocation` <br/> |Spécifie le dossier qui contient le fichier de configuration. XML qui a été créé lors de l'exécution de l'outil dans le mode de recherche. Utilisez la même valeur que celle que vous avez utilisée pour ce paramètre à l'étape 1.  <br/> | `-ConfigurationLocation "c:\users\admin\desktop \PSTCollection\Configuration"` <br/> |
    | `CopyLocation` <br/> |Spécifie l'emplacement de la collection dans laquelle vous souhaitez copier les fichiers PST. Vous pouvez copier des fichiers sur un serveur de fichiers, un partage de fichiers réseau ou un disque dur. L'emplacement doit exister avant l'exécution de l'outil en mode de collecte. L'outil ne crée pas l'emplacement et renvoie une erreur indiquant qu'il n'existe pas.  <br/> En outre, vous devez écrire des autorisations sur l'emplacement de collection spécifié par ce paramètre.  <br/> | `-CopyLocation "\\FILESERVER03\PSTs"` <br/> |
    | `LogLocation` <br/> |Spécifie le dossier dans lequel le fichier journal du mode de collecte sera copié. Ce paramètre est facultatif. Si vous ne l'incluez pas, le fichier journal est copié dans le dossier dans lequel vous avez téléchargé l'outil de collecte PST. EnVisagez d'utiliser le même emplacement de journal que celui que vous avez utilisé lors de l'exécution de l'outil dans le mode de recherche à l'étape 1 afin que tous les fichiers journaux soient enregistrés dans le même dossier.  <br/> | `-LogLocation "c:\users\admin\desktop\PSTCollection"` <br/> |
    | `ForceRestart` <br/> |Ce commutateur facultatif vous permet de réexécuter l'outil en mode de collecte pour un travail de collection PST existant. Si vous avez précédemment exécuté l'outil en mode de collecte, mais que vous l'avez ensuite exécuté dans le mode de `ForceRestart` recherche avec le commutateur pour réanalyser les emplacements des fichiers PST, vous pouvez utiliser ce commutateur pour réexécuter l'outil en mode de collecte et recopier les fichiers PST trouvés lors de votre ré-analysé les emplacements. Lorsque vous utilisez `ForceRestart` le commutateur en mode de collecte, l'outil ignore les opérations de collection précédentes et tente de copier les fichiers PST de toutes pièces.  <br/> | `-ForceRestart` <br/> |
   
    Voici un exemple de la syntaxe de l'outil DataCollectorMaster. exe qui utilise les valeurs réelles de chaque paramètre:
    
    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Collect -JobName PstSearch1 -Locations "CN=FILESERVER01,CN=Computers,DC=contoso,DC=com";"CN=FILESERVER02,CN=Computers,DC=contoso,DC=com" -ConfigurationLocation "c:\users\admin\desktop\PSTCollection\Configuration" -CopyLocation "\\FILESERVER03\PSTs" -LogLocation "c:\users\admin\desktop\PSTCollection"
    ```

    Une fois la commande exécutée, des messages d'État détaillés s'affichent pour indiquer la progression de la collecte des fichiers PST trouvés à l'étape 1. Après un certain temps, un message d'état final indique s'il y a eu des erreurs et l'emplacement où le journal est copié. Les mêmes messages d'État sont copiés dans le fichier. log.
    
### <a name="results-of-running-datacollectormasterexe-in-the-collect-mode"></a>Résultats de l'exécution de DataCollectorMaster. exe en mode de collecte

Une fois que vous avez exécuté DataCollectorMaster. exe en mode de collecte, les fichiers suivants sont créés et stockés dans les dossiers spécifiés par les `LogLocation` paramètres et `ConfigurationLocation` . 
  
- **\>__ JobName Collect\<DateTimeStamp\>. log: le fichier journal contient les messages \<** d'état affichés. Ce fichier est créé dans le dossier spécifié par le `LogLocation` paramètre. 
    
- **\>__ JobName Collect\<DateTimeStamp\>. xml-le fichier XML contient uniquement des informations sur les valeurs de paramètre qui, utilisées par l'outil, ont été exécutées en \<** mode de collecte. Les données contenues dans ce fichier sont utilisées lorsque vous exécutez de nouveau l'outil DataCollectorMaster. exe pour supprimer des fichiers PST; Voir [étape 5](#step-5-delete-the-pst-files-found-on-your-network).
    

## <a name="step-4-import-the-pst-files-to-office-365"></a>Étape 4: importer les fichiers PST dans Office 365

Une fois que vous avez collecté les fichiers PST trouvés à l'étape 1, l'étape suivante consiste à les importer dans des boîtes aux lettres dans Office 365. Dans le cadre du processus d'importation, vous devrez créer un fichier de mappage CSV contenant une ligne de chaque fichier PST que vous souhaitez importer. Les informations contenues dans chaque ligne spécifient le nom du fichier PST, l'adresse de messagerie de l'utilisateur et si vous souhaitez importer le fichier PST dans la boîte aux lettres principale ou d'archivage de l'utilisateur. Utilisez les informations de l' **JobName\>_Rechercher_\<DateTimeStamp. csv** (créé à l'étape) 1 pour vous aider à créer le fichier de mappage CSV. 
  
Pour obtenir des instructions détaillées sur l'importation de fichiers PST dans Office 365, consultez l'une des rubriques suivantes:
  
- [Utiliser le chargement réseau pour importer des fichiers PST vers Office 365](use-network-upload-to-import-pst-files.md)
    
- [Utiliser l’expédition de disque pour importer des fichiers PST dans Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md)
    

## <a name="step-5-delete-the-pst-files-found-on-your-network"></a>Étape 5: supprimer les fichiers PST trouvés sur votre réseau

Une fois que les fichiers PST que vous avez trouvés et collectés ont été importés dans les boîtes aux lettres Exchange Online dans Office 365, vous pouvez utiliser l'outil de collecte PST pour supprimer les fichiers PST des emplacements sources d'origine où ils ont été trouvés à l'étape 1. 
  
1. Ouvrez une invite de commandes (exécuter en tant qu'administrateur) sur votre ordinateur local.
    
2. Accédez au répertoire dans lequel vous avez téléchargé l'outil de collection PST dans.
    
3. Exécutez la commande suivante pour supprimer les fichiers PST.

    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Delete -JobName <Name of job from Step 1> -ConfigurationLocation <Location of configuration files from Step 1> -CopyLocation <Location to copy PST files to>
    ```

    Le tableau suivant décrit les paramètres et leurs valeurs requises lors de l'exécution de la commande DataCollectorMaster. exe pour supprimer des fichiers PST. 
    
    |Paramètre * * * *|****Description****|Exemples * * * *|
    |:-----|:-----|:-----|
    | `DataSource` <br/> |Spécifie le type de données à rechercher. Actuellement, vous pouvez utiliser l'outil de collection PST pour rechercher des fichiers PST. ![espacement](media/b078d05c-3aee-4b9f-8805-6a8a9d8970ee.png)           <br/> | `-DataSource Pst` <br/> |
    | `Mode` <br/> |Spécifie le type d'opération exécutée par l'outil. Utilisez la valeur `Delete` pour supprimer les fichiers PST qui ont été trouvés lors de l'exécution de l'outil dans le mode de recherche.  <br/> | `-Mode Delete` <br/> |
    | `JobName` <br/> |Spécifie le nom d'un travail de collection PST existant. Vous devez utiliser le même nom de travail que celui que vous avez utilisé lors de l'exécution de l'outil dans le mode de recherche et le mode de collecte à l'étape 1 et à l'étape 3. Ce nom de travail est également ajouté au nom du fichier journal créé lors de l'exécution de l'outil en mode suppression.  <br/> | `-JobName PstSearch1` <br/> |
    | `ConfigurationLocation` <br/> |Spécifie le dossier qui contient le fichier de configuration. XML qui a été créé lors de l'exécution de l'outil en mode de collecte. Utilisez la même valeur que celle que vous avez utilisée pour ce paramètre à l'étape 3.  <br/> | `-ConfigurationLocation "c:\users\admin\ desktop\PSTCollection\Configuration"` <br/> |
    | `LogLocation` <br/> |Spécifie le dossier dans lequel le fichier journal du mode de suppression sera copié. Ce paramètre est facultatif. Si vous ne l'incluez pas, le fichier journal est copié dans le dossier dans lequel vous avez téléchargé l'outil de collecte PST. EnVisagez d'utiliser le même emplacement de journal que celui que vous avez utilisé lors de l'exécution de l'outil dans les modes de recherche et de collecte de l'étape 1 et de l'étape 3 afin que tous les fichiers journaux soient enregistrés dans le même dossier.  <br/> | `-LogLocation "c:\users\admin\desktop\PSTCollection"` <br/> |
    | `ForceRestart` <br/> |Ce commutateur facultatif vous permet de réexécuter l'outil en mode de suppression pour un travail de collection PST existant. Si vous avez précédemment exécuté l'outil en mode de suppression, mais que vous l'avez ensuite exécuté dans le mode de `ForceRestart` recherche avec le commutateur pour réanalyser les emplacements des fichiers PST, vous pouvez utiliser ce commutateur pour réexécuter l'outil en mode de suppression et supprimer les fichiers PST trouvés lors de votre reconfiguration nned les emplacements. Lorsque vous utilisez `ForceRestart` le commutateur en mode de suppression, l'outil ignore toutes les opérations de suppression précédentes et tente de supprimer les fichiers PST.  <br/> | `-ForceRestart` <br/> 

    Voici un exemple de la syntaxe de l'outil DataCollectorMaster. exe qui utilise les valeurs réelles de chaque paramètre:
    
    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Delete -JobName PstSearch1 -ConfigurationLocation "c:\users\admin\desktop\PSTCollection\Configuration" -LogLocation "c:\users\admin\desktop\PSTCollection"
    ```
   
    Une fois la commande exécutée, des messages d'État détaillés s'affichent pour indiquer la progression de la suppression des fichiers PST trouvés à l'étape 1 et collectés à l'étape 3. Après un certain temps, un message d'état final indique s'il y a eu des erreurs et l'emplacement où le journal est copié. Les mêmes messages d'État sont copiés dans le fichier. log.
    
### <a name="results-of-running-datacollectormasterexe-in-the-delete-mode"></a>Résultats de l'exécution de DataCollectorMaster. exe en mode de suppression

Après avoir exécuté DataCollectorMaster. exe en mode de suppression, les fichiers suivants sont créés et stockés dans le dossier spécifié par les `LogLocation` paramètres et `ConfigurationLocation` . 
  
- **\>__ JobName supprimer\<DateTimeStamp\>. log: le fichier journal contient les messages \<** d'état affichés. Ce fichier est créé dans le dossier spécifié par le `LogLocation` paramètre. 
    
- **\>__ JobName supprimer\<DateTimeStamp\>. xml-le fichier XML contient uniquement des informations sur les valeurs de paramètre qui, utilisées par l'outil, ont été exécutées en \<** mode de suppression. Il répertorie également le nom et le chemin d'accès de chaque fichier PST qui a été supprimé. Ce fichier est créé dans le dossier spécifié par le `ConfigurationLocation` paramètre. 
