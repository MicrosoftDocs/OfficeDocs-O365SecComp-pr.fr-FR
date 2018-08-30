---
title: Modifier la taille des fichiers PST lors de l’exportation des résultats de recherche eDiscovery
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 11/30/2016
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 04e9de2d-765b-457b-a98a-d0f60bfb13f2
description: Vous pouvez modifier le la taille par défaut des fichiers PST qui est téléchargé sur votre ordinateur lorsque vous exportez des résultats de recherche eDiscovery.
ms.openlocfilehash: d38189c437154dbe27a084230d4d3fd4de418ece
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527568"
---
# <a name="change-the-size-of-pst-files-when-exporting-ediscovery-search-results"></a>Modifier la taille des fichiers PST lors de l’exportation des résultats de recherche eDiscovery

Lorsque vous utilisez l’outil d’exportation de découverte électronique Office 365 pour exporter les résultats de la messagerie d’une recherche de découverte électronique à partir de différents outils Microsoft eDiscovery, la taille par défaut d’un fichier PST qui peut être exporté est de 10 Go. Si vous souhaitez modifier cette taille par défaut, vous pouvez modifier le Registre Windows sur l’ordinateur que vous utilisez pour exporter les résultats de recherche. Une des raisons à cela étant un fichier PST tiennent sur un support amovible, tel un DVD, un CD-ROM ou une clé USB. 
  
> [!NOTE]
>  L’outil d’exportation de découverte électronique Office 365 est utilisée pour exporter les résultats de recherche lors de l’utilisation de la recherche de contenu de sécurité Office 365 &amp; centre de conformité, eDiscovery sur Place dans Exchange Online et le centre eDiscovery dans SharePoint Online. 
  
## <a name="create-a-registry-setting-to-change-the-size-of-pst-files-when-you-export-ediscovery-search-results"></a>Créer un paramètre de Registre pour modifier la taille des fichiers PST lors de l’exportation de résultats de recherche eDiscovery

Effectuez la procédure suivante sur l’ordinateur que vous allez utiliser pour exporter les résultats d’une recherche eDiscovery.
  
1. Fermez l’outil d’exportation de découverte électronique Office 365 si elle est ouverte. 
    
2. Enregistrez le texte suivant dans un fichier de Registre de fenêtre à l’aide d’un suffixe de nom de fichier de .reg ; par exemple, PstExportSize.reg. 
    
    ```
    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool]
    "PstSizeLimitInBytes"="1073741824"
    ```

    Dans l’exemple ci-dessus, le `PstSizeLimitInBytes` valeur est définie sur 1 073 741 824 octets ou environ 1 Go. Voici quelques autres exemples de valeurs pour le `PstSizeLimitInBytes` paramètre. 
    
    |**Taille en Go (environ)**|**Taille en octets**|
    |:-----|:-----|
    |.7 GO (700 MO)  <br/> |751619277  <br/> |
    |2 Go  <br/> |2147483648  <br/> |
    |4 Go  <br/> |4294967296  <br/> |
    |8 Go  <br/> |8589934592  <br/> |
   
3. Modifier la `PstSizeLimitInBytes` valeur à la taille maximale de votre choix d’un fichier PST lorsque vous exportez les résultats de recherche, puis enregistrez le fichier. 
    
4. Dans l’Explorateur Windows, cliquez sur ou double-cliquez sur le fichier .reg que vous avez créée lors des étapes précédentes.
    
5. Dans la fenêtre de contrôle d’accès utilisateur, cliquez sur **Oui** pour laisser l’Éditeur du Registre que la modification. 
    
6. Lorsque vous y êtes invité à continuer, cliquez sur **Oui**.
    
    L’Éditeur du Registre affiche un message indiquant que le paramètre a été correctement ajouté au Registre.
    
7. Vous pouvez répéter les étapes 3 à 6 pour modifier la valeur pour le `PstSizeLimitInBytes` paramètre de Registre. 
  
## <a name="frequently-asked-questions-about-changing-the-default-size-of-pst-files-when-you-export-ediscovery-search-results"></a>Forum aux questions sur la modification de la taille par défaut des fichiers PST lors de l’exportation de résultats de recherche eDiscovery

 **Pourquoi est la valeur par défaut taille 10 Go ?**
  
La taille par défaut de 10 Go a été en fonction des commentaires des clients ; 10 Go est un bon équilibre entre la quantité de contenu dans un fichier PST unique et avec un risque de corruption de fichier minimal optimale.
  
 **Dois-je augmenter ou diminuer la taille par défaut des fichiers PST ?**
  
Les clients ont tendance à diminuer la limite de taille afin que les résultats de recherche adapté sur un support amovible qu’ils peuvent physiquement expédier autres emplacements dans leur organisation. Nous ne recommandons pas augmenter la taille par défaut, car il est supérieure à 10 Go peut-être des problèmes de corruption des fichiers PST.
  
 **Quel ordinateur dois-je faire ?**
  
Vous devez modifier le paramètre de Registre sur un ordinateur local que vous exécutez l’outil d’exportation de découverte électronique Office 365 sur.
  
 **Après modification de ce paramètre, dois-je redémarrer l’ordinateur ?**
  
Non, vous n’êtes pas obligé de redémarrer l’ordinateur. Mais, si l’outil d’exportation de découverte électronique Office 365 est en cours d’exécution, vous devrez fermer et le redémarrage après vous modifier ce paramètre.
  
 **Est une clé de Registre existante obtenir modifiée ou est une nouvelle clé sont créée ?**
  
Une nouvelle clé de Registre est créée la première fois que vous exécutez le fichier .reg que vous avez créé dans cette procédure. Puis le paramètre est modifié à chaque fois que vous modifiez et réexécutez la modifier le fichier .reg.
