---
title: Augmentation de la vitesse de téléchargement lors de l'exportation des résultats de recherche eDiscovery à partir d'Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/14/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid: MOE150
ms.assetid: c4c8f689-9d52-4e80-ae4b-1411ee9efc43
description: Découvrez comment configurer le Registre Windows pour augmenter le débit de données lors du téléchargement des résultats de recherche et des données de recherche à partir du centre de sécurité & Compliance Center et de la fonctionnalité eDiscovery avancée dans Office 365.
ms.openlocfilehash: 36a4f1766f3ac0108d1829c93cfca63bc5cf09f5
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2019
ms.locfileid: "31000917"
---
# <a name="increase-the-download-speed-when-exporting-ediscovery-search-results-from-office-365"></a>Augmentation de la vitesse de téléchargement lors de l'exportation des résultats de recherche eDiscovery à partir d'Office 365

Lorsque vous utilisez l'outil d'exportation de découverte électronique Office 365 pour télécharger les résultats d'une recherche de contenu dans le centre de sécurité & Compliance Center ou télécharger des données à partir d'Office 365 Advanced eDiscovery, l'outil démarre un certain nombre d'opérations d'exportation simultanées à télécharger les données sur votre ordinateur local. Par défaut, le nombre d'opérations simultanées est défini sur 8 fois le nombre de cœurs de l'ordinateur que vous utilisez pour télécharger les données. Par exemple, si vous disposez d'un ordinateur double cœur (ce qui signifie que deux unités de traitement central sur une puce), le nombre d'opérations d'exportation simultanées par défaut est de 16. Pour augmenter le débit de transfert de données et accélérer le processus de téléchargement, vous pouvez augmenter le nombre d'opérations simultanées en configurant un paramètre de Registre Windows sur l'ordinateur que vous utilisez pour télécharger les résultats de la recherche. Pour accélérer le processus de téléchargement, nous vous recommandons de commencer avec un paramètre de 24 opérations simultanées.
  
Si vous téléchargez des résultats de recherche sur un réseau à faible bande passante, l'augmentation de ce paramètre peut avoir un impact négatif. Vous pouvez également augmenter le paramètre sur plus de 24 opérations simultanées dans un réseau à bande passante élevée (le nombre maximal d'opérations simultanées est de 512). Une fois que vous avez configuré ce paramètre de Registre, vous devrez peut-être le modifier pour trouver le nombre optimal d'opérations simultanées pour votre environnement.
  
## <a name="create-a-registry-setting-to-change-the-number-of-concurrent-operations-when-exporting-data"></a>Créer un paramètre de Registre pour modifier le nombre d'opérations simultanées lors de l'exportation des données

Effectuez la procédure suivante sur l'ordinateur que vous allez utiliser pour télécharger les résultats de recherche à partir du centre de sécurité & conformité ou des données d'Advanced eDiscovery.
  
1. Fermez l'outil d'exportation eDiscovery d'Office 365 s'il est ouvert. 
    
2. Enregistrez le texte suivant dans un fichier de Registre Windows à l'aide d'un suffixe de nom de fichier. reg; par exemple, ConcurrentOperations. reg. 
    
    ```
    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool]
    "DownloadConcurrency"="24"
    ```

    Comme indiqué précédemment, nous vous recommandons de commencer par 24 opérations simultanées, puis de modifier ce paramètre selon vos besoins.
    
3. Dans l'Explorateur Windows, cliquez ou double-cliquez sur le fichier. reg que vous avez créé à l'étape précédente.
    
4. Dans la fenêtre contrôle d'accès des utilisateurs, cliquez sur **Oui** pour permettre à l'éditeur du registre de procéder à la modification. 
    
5. Lorsque vous êtes invité à continuer, cliquez sur **Oui**.
    
    L'éditeur du Registre affiche un message indiquant que le paramètre a été ajouté avec succès au registre.
    
6. Vous pouvez répéter les étapes 2-5 pour modifier la valeur du `DownloadConcurrency` paramètre de registre. 
    
    > [!IMPORTANT]
    > Une fois que vous avez créé `DownloadConcurrency` ou modifié le paramètre de Registre, veillez à créer une nouvelle tâche d'exportation ou à redémarrer une tâche d'exportation existante pour les résultats de recherche ou les données que vous souhaitez télécharger. Pour plus d'informations, rePortez-vous à la section [more information](#more-information) . 
  
## <a name="more-information"></a>Plus d’informations

- Une nouvelle clé de Registre est créée lors de la première exécution du fichier. reg que vous avez créé au cours de cette procédure. Le `DownloadConcurrency` paramètre de Registre est ensuite modifié chaque fois que vous modifiez et réexécutez le fichier de modification. reg. 
    
- L'outil d'exportation de découverte électronique Office 365 utilise l' [utilitaire Azure AzCopy](https://go.microsoft.com/fwlink/?linkid=849949) pour télécharger des données de recherche à partir du centre de sécurité & conformité ou d'Advanced eDiscovery. La configuration du `DownloadConcurrency` paramètre de Registre est similaire à l'utilisation du paramètre **/NC** lors de l'exécution de l'utilitaire AzCopy. Par conséquent, le paramètre `"DownloadConcurrency=24"` de Registre aurait le même effet que l'utilisation de la `/NC:24` valeur de paramètre avec l'utilitaire AzCopy. 
    
- Si vous arrêtez le téléchargement d'exportation en cours, puis le redémarrez (en essayant de nouveau de télécharger les résultats de la recherche), l'outil d'exportation de découverte électronique Office 365 reprendra le même téléchargement. Par conséquent, si vous démarrez un téléchargement, que vous l'arrêtez, puis `DownloadConcurrency` que vous modifiez le paramètre de Registre, le téléchargement échouera probablement si vous le redémarrez (en cliquant sur **Télécharger les résultats**exportés). Cela est dû au fait que l'outil d'exportation tente de reprendre le téléchargement précédent en utilisant des paramètres qui ne sont pas valides, car vous avez modifié le paramètre de registre.
    
    Par conséquent, une fois que `DownloadConcurrency` vous avez modifié le paramètre de Registre, veillez à redémarrer le travail d'exportation (en cliquant sur **redémarrer l'exportation**) dans le centre de sécurité & Compliance Center. Vous pouvez ensuite télécharger les résultats exportés. Pour plus d'informations sur l'exportation des données et des résultats de recherche, voir:
    
  - [Exporter les résultats de la recherche de contenu](export-search-results.md)
    
  - [Exporter les résultats dans Office 365 Advanced eDiscovery](export-results-in-advanced-ediscovery.md)
    
