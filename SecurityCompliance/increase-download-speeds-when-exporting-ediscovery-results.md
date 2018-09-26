---
title: Augmenter la vitesse de téléchargement lors de l’exportation des résultats de recherche de découverte électronique à partir d’Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/14/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MOE150
ms.assetid: c4c8f689-9d52-4e80-ae4b-1411ee9efc43
description: Découvrez comment configurer le Registre Windows pour augmenter le débit de données lorsque je télécharge des résultats de la recherche et rechercher des données à partir de la sécurité de 365 Office &amp; centre de conformité et Office 365 avancée eDiscovery.
ms.openlocfilehash: a05c2b786d1d1de7ff5014d12c708484345f908b
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038117"
---
# <a name="increase-the-download-speed-when-exporting-ediscovery-search-results-from-office-365"></a>Augmenter la vitesse de téléchargement lors de l’exportation des résultats de recherche de découverte électronique à partir d’Office 365

Lorsque vous utilisez l’outil d’exportation de découverte électronique Office 365 pour télécharger les résultats d’une recherche de contenu de sécurité Office 365 &amp; centre de conformité ou télécharger des données à partir d’Office 365 avancée eDiscovery, l’outil démarrent un certain nombre d’exportation simultanée opérations pour télécharger les données sur votre ordinateur local. Par défaut, le nombre d’opérations simultanées est défini à 8 fois le nombre de cœurs de l’ordinateur que vous utilisez pour télécharger les données. Par exemple, si vous avez un ordinateur double cœur (ce qui signifie que deux unités centrales sur une puce), le numéro par défaut des opérations d’exportation simultanées est de 16. Pour augmenter le débit de transfert de données et accélérer le processus de téléchargement, vous pouvez augmenter le nombre d’opérations simultanées en configurant un paramètre de Registre Windows sur l’ordinateur que vous utilisez pour télécharger les résultats de recherche. Pour accélérer le processus de téléchargement, nous vous recommandons de commencer avec un paramètre de 24 opérations simultanées.
  
Si vous téléchargez des résultats de la recherche sur un réseau de faible bande passante, l’augmentation de ce paramètre peut avoir un impact négatif. Sinon, vous pourrez peut-être augmenter le paramètre à plus de 24 opérations simultanées dans un réseau à bande passante élevée (le nombre maximal d’opérations simultanées est 512). Après avoir configuré ce paramètre de Registre, vous devrez peut-être modifier pour trouver le nombre optimal d’opérations simultanées pour votre environnement.
  
## <a name="create-a-registry-setting-to-change-the-number-of-concurrent-operations-when-exporting-data"></a>Créer un paramètre de Registre pour modifier le nombre d’opérations simultanées lors de l’exportation des données

Effectuez la procédure suivante sur l’ordinateur que vous utiliserez pour télécharger les résultats de la recherche de la sécurité &amp; centre de conformité ou des données à partir de la découverte électronique avancée.
  
1. Fermez l’outil d’exportation de découverte électronique Office 365 si elle est ouverte. 
    
2. Enregistrez le texte suivant dans un fichier de Registre de fenêtre à l’aide d’un suffixe de nom de fichier de .reg ; par exemple, ConcurrentOperations.reg. 
    
    ```
    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool]
    "DownloadConcurrency"="24"
    ```

    Précédente comme expliqué, nous vous recommandons de démarrer avec 24 opérations simultanées, puis modifier ce paramètre en fonction.
    
3. Dans l’Explorateur Windows, cliquez sur ou double-cliquez sur le fichier .reg que vous avez créé à l’étape précédente.
    
4. Dans la fenêtre de contrôle d’accès utilisateur, cliquez sur **Oui** pour laisser l’Éditeur du Registre que la modification. 
    
5. Lorsque vous y êtes invité à continuer, cliquez sur **Oui**.
    
    L’Éditeur du Registre affiche un message indiquant que le paramètre a été correctement ajouté au Registre.
    
6. Vous pouvez répéter les étapes 2 à 5 pour modifier la valeur pour le `DownloadConcurrency` paramètre de Registre. 
    
    > [!IMPORTANT]
    > Une fois que vous créez ou modifiez la `DownloadConcurrency` clé de Registre, veillez à créer une nouvelle tâche d’exportation ou redémarrer une tâche d’exportation existante pour les résultats de recherche ou les données que vous souhaitez télécharger. Voir la section [plus d’informations](increase-download-speeds-when-exporting-ediscovery-results.md#moreinfo) pour plus d’informations. 
  
## <a name="more-information"></a>Plus d’informations

- Une nouvelle clé de Registre est créée la première fois que vous exécutez le fichier .reg que vous avez créé dans cette procédure. Le `DownloadConcurrency` paramètre de Registre est modifié à chaque fois que vous modifiez et réexécutez la modifier le fichier .reg. 
    
- L’outil d’exportation de découverte électronique Office 365 utilise l' [utilitaire AzCopy Azure](https://go.microsoft.com/fwlink/?linkid=849949) pour télécharger les données de recherche à partir de la sécurité &amp; centre de conformité ou d’eDiscovery avancée. Configuration de la `DownloadConcurrency` paramètre de Registre est similaire à l’aide du paramètre **/NC** lors de l’exécution de l’utilitaire AzCopy. Si le paramètre de Registre de `"DownloadConcurrency=24"` aurait le même effet que l’utilisation de la valeur du paramètre de `/NC:24` avec l’utilitaire AzCopy. 
    
- Si vous arrêtez un téléchargement d’exportation qui est en cours, puis redémarrez (en essayant de télécharger à nouveau les résultats de recherche), l’outil d’exportation de découverte électronique Office 365 tente de reprendre le téléchargement même. Ainsi, si vous démarrez un téléchargement, arrêter, puis modifier la `DownloadConcurrency` Registre définition, le téléchargement probablement échouera si vous le redémarrer (en cliquant sur **Télécharger exporté les résultats**). Il s’agit, car l’outil d’exportation tente de reprendre le téléchargement précédent à l’aide des paramètres qui ne sont pas valides, car vous avez modifié le paramètre de Registre.
    
    Par conséquent, après avoir modifié le `DownloadConcurrency` clé de Registre, n’oubliez pas de redémarrer la tâche d’exportation (en cliquant sur **redémarrer exportation**) de la sécurité &amp; centre de conformité. Vous pouvez télécharger les résultats exportés. Pour plus d’informations sur l’exportation de données et les résultats de la recherche, voir :
    
  - [Exporter les résultats de recherche de contenu à partir de la sécurité de 365 Office &amp; centre de conformité](export-search-results.md)
    
  - [Exporter les résultats dans Office 365 Advanced eDiscovery](export-results-in-advanced-ediscovery.md)
    
