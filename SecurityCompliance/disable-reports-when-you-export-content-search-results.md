---
title: Désactiver les rapports lorsque vous exportez des résultats de recherche de &amp; contenu dans le centre de sécurité conformité Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/30/2016
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: MOE150
ms.assetid: c9b0ff0c-282b-4a44-b43f-cfc5b96557f9
description: Modifiez le Registre Windows sur votre ordinateur local pour désactiver les rapports lorsque vous exportez les résultats d'une recherche de contenu à &amp; partir du centre de Comliance de sécurité Office 365. La désActivation de ces rapports permet d'accélérer le temps de téléchargement et d'économiser de l'espace disque.
ms.openlocfilehash: f08f5e7143022591d38bda787301e71ae80fb3d3
ms.sourcegitcommit: 8a65a29aa3bfe5dcad0ff152a7cd795e02877dd9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/28/2019
ms.locfileid: "30936714"
---
# <a name="disable-reports-when-you-export-content-search-results-in-the-office-365-security-amp-compliance-center"></a>Désactiver les rapports lorsque vous exportez des résultats de recherche de &amp; contenu dans le centre de sécurité conformité Office 365

Lorsque vous utilisez l'outil d'exportation de découverte électronique Office 365 pour exporter les résultats d'une recherche de &amp; contenu dans le centre de sécurité conformité, l'outil crée et exporte automatiquement deux rapports contenant des informations supplémentaires sur le contenu exporté. Ces rapports sont les fichiers Results. csv et manifest. XML (voir la section Forum [aux questions sur](#frequently-asked-questions-about-disabling-export-reports) la désactivation des rapports d'exportation de cette rubrique pour obtenir des descriptions détaillées de ces rapports). Étant donné que ces fichiers peuvent être très volumineux, vous pouvez accélérer le temps de téléchargement et économiser de l'espace disque en empêchant l'exportation de ces fichiers. Pour ce faire, vous pouvez modifier le Registre Windows sur l'ordinateur que vous utilisez pour exporter les résultats de la recherche. Si vous souhaitez inclure les rapports ultérieurement, vous pouvez modifier le paramètre de registre. 
  
## <a name="create-registry-settings-to-disable-the-export-reports"></a>Créer des paramètres de Registre pour désactiver les rapports d'exportation

Effectuez la procédure suivante sur l'ordinateur que vous allez utiliser pour exporter les résultats d'une recherche de contenu.
  
1. Fermez l'outil d'exportation eDiscovery d'Office 365 s'il est ouvert.
    
2. Effectuez l'une des étapes suivantes, ou les deux, en fonction de l'état d'exportation que vous souhaitez désactiver.
    
    - **Results. csv**
    
      Enregistrez le texte suivant dans un fichier de Registre Windows à l'aide d'un suffixe de nom de fichier. reg; par exemple, DisableResultsCsv. reg.
    
      ```
      Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultCsvEnabled /t REG_SZ /d False 
      ```

    - **Manifest. Xml**
    
      Enregistrez le texte suivant dans un fichier de Registre Windows à l'aide d'un suffixe de nom de fichier. reg; par exemple, DisableManifestXml. reg.
    
      ```
      Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultEdrmEnabled /t REG_SZ /d False 
      ```

3. Dans l'Explorateur Windows, cliquez ou double-cliquez sur le fichier. reg que vous avez créé au cours des étapes précédentes.
    
4. Dans la fenêtre contrôle d'accès des utilisateurs, cliquez sur **Oui** pour permettre à l'éditeur du registre de procéder à la modification. 
    
5. Lorsque vous êtes invité à continuer, cliquez sur **Oui**.
    
    L'éditeur du Registre affiche un message indiquant que le paramètre a été ajouté avec succès au registre.
  
## <a name="edit-registry-settings-to-re-enable-the-export-reports"></a>Modifier les paramètres du Registre pour réactiver les rapports d'exportation

Si vous avez désactivé les rapports results. csv et manifest. XML en créant les fichiers. reg dans la procédure précédente, vous pouvez modifier ces fichiers pour réactiver un rapport afin qu'il soit exporté avec les résultats de la recherche. À nouveau, effectuez la procédure suivante sur l'ordinateur que vous allez utiliser pour exporter les résultats d'une recherche de contenu.
  
1. Fermez l'outil d'exportation eDiscovery d'Office 365 s'il est ouvert.
    
2. Modifiez l'un des fichiers d'édition. reg que vous avez créés dans la procédure précédente ou les deux.
    
    - **Results. csv**
    
        Ouvrez le fichier DisableResultsCsv. reg dans le bloc-notes, `False` remplacez `True`la valeur par, puis enregistrez le fichier. Par exemple, après avoir modifié le fichier, il se présente comme suit:
    
        ```
        Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultCsvEnabled /t REG_SZ /d True
        ```

    - **Manifest. Xml**
    
        Ouvrez le fichier DisableManifestXml. reg dans le bloc-notes, `False` remplacez `True`la valeur par, puis enregistrez le fichier. Par exemple, après avoir modifié le fichier, il se présente comme suit:
    
      ```
      Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultEdrmEnabled /t REG_SZ /d True
      ```

3. Dans l'Explorateur Windows, cliquez ou double-cliquez sur un fichier. reg que vous avez modifié à l'étape précédente.
    
4. Dans la fenêtre contrôle d'accès des utilisateurs, cliquez sur **Oui** pour permettre à l'éditeur du registre de procéder à la modification. 
    
5. Lorsque vous êtes invité à continuer, cliquez sur **Oui**.
    
    L'éditeur du Registre affiche un message indiquant que le paramètre a été ajouté avec succès au registre.
  
## <a name="frequently-asked-questions-about-disabling-export-reports"></a>Forum aux questions sur la désactivation des rapports d'exportation
<a name="faqs"> </a>

 **Quels sont les rapports results. csv et manifest. Xml?**
  
Les fichiers Results. csv et manifest. XML contiennent des informations supplémentaires sur le contenu qui a été exporté.
  
- **Results. csv** document Excel qui contient des informations sur chaque élément téléchargé en tant que résultat de la recherche. Pour le courrier électronique, le journal des résultats contient des informations sur chaque message, y compris : 
    
  - l’emplacement du message dans la boîte aux lettres source (notamment si le message est dans la boîte aux lettres principale ou d’archivage) ;
    
  - la date à laquelle le message a été envoyé ou reçu ;
    
  - l’objet du message ;
    
  - l’expéditeur et les destinataires du message.
    
  - Si le message est un message en double si vous avez activé la déduplication lors de l'exportation des résultats de la recherche. Les messages en double comportent une valeur dans la colonne **ItemId parent** qui identifie le message en tant que doublon. La valeur dans la colonne **ItemId parent** est identique à la valeur de la colonne **élément DocumentID** du message qui a été exporté. 
    
    Pour les documents provenant de sites SharePoint et OneDrive entreprise, le journal des résultats contient des informations sur chaque document, notamment:
    
  - l’URL du document ;
    
  - l’URL de la collection de sites qui héberge le document ;
    
  - la date à laquelle le document a été modifié pour la dernière fois ;
    
  - le nom du document (qui se trouve dans la colonne Objet du journal des résultats).
    
- **Manifest. xml** fichier manifeste (au format XML) qui contient des informations sur chaque élément inclus dans les résultats de la recherche. Les informations contenues dans ce rapport sont identiques à celles du rapport results. csv, mais elles sont au format spécifié par le modèle de référence de découverte électronique (EDRM). Pour plus d'informations sur EDRM, consultez [https://www.edrm.net](https://www.edrm.net)la rubrique.
    
 **Quand dois-je désactiver l'exportation de ces rapports?**
  
Cela dépend de vos besoins spécifiques. De nombreuses organisations n'ont pas besoin d'informations supplémentaires sur les résultats de la recherche et n'ont pas besoin de ces rapports.
  
 **Sur quel ordinateur dois-je effectuer cette opération?**
  
 Vous devez modifier le paramètre de Registre sur tout ordinateur local sur lequel vous exécutez l'outil d'exportation de découverte électronique Office 365. 
  
 **Après avoir modifié ce paramètre, dois-je redémarrer l'ordinateur?**
  
Non, il n'est pas nécessaire de redémarrer l'ordinateur. Toutefois, si l'outil d'exportation eDiscovery d'Office 365 est en cours d'exécution, vous devez le fermer, puis le redémarrer une fois le paramètre de Registre modifié.
  
 **Une clé de Registre existante est-elle modifiée ou une nouvelle clé est-elle créée?**
  
Une nouvelle clé de Registre est créée lors de la première exécution du fichier. reg que vous avez créé dans la procédure de cette rubrique. Le paramètre est ensuite modifié chaque fois que vous modifiez et réexécutez le fichier de modification. reg.
