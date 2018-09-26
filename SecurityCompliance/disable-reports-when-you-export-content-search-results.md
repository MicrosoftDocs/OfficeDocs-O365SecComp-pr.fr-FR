---
title: Désactiver les rapports lorsque vous exportez des résultats de la recherche de contenu de sécurité Office 365 &amp; centre de conformité
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/30/2016
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MOE150
ms.assetid: c9b0ff0c-282b-4a44-b43f-cfc5b96557f9
description: Modifiez le Registre de Windows sur votre ordinateur local pour désactiver les rapports lorsque vous exportez les résultats d’une recherche de contenu à partir de la sécurité de 365 Office &amp; Comliance centre. Désactivation de ces rapports, vous pouvez accélérer le temps de téléchargement et économiser de l’espace disque.
ms.openlocfilehash: 62782c472adca892e1dcf239a45fe80f0fa7251b
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25037977"
---
# <a name="disable-reports-when-you-export-content-search-results-in-the-office-365-security-amp-compliance-center"></a>Désactiver les rapports lorsque vous exportez des résultats de la recherche de contenu de sécurité Office 365 &amp; centre de conformité

Lorsque vous utilisez l’outil d’exportation de découverte électronique Office 365 pour exporter les résultats d’une recherche de contenu dans la sécurité &amp; centre de conformité, l’outil crée automatiquement et exporte les deux rapports qui contiennent des informations supplémentaires sur le contenu exporté. Ces rapports sont le fichier Results.csv et le fichier Manifest.xml (voir la section [Forum aux questions sur la désactivation d’exporter des rapports](#frequently-asked-questions-about-disabling-export-reports) dans cette rubrique pour obtenir des descriptions détaillées de ces rapports). Étant donné que ces fichiers peuvent être très volumineux, vous pouvez accélérer le temps de téléchargement et économiser de l’espace disque en empêchant l’exportation de ces fichiers. Vous pouvez procéder en modifiant le Registre Windows sur l’ordinateur que vous utilisez pour exporter les résultats de recherche. Si vous souhaitez inclure les rapports à une date ultérieure, vous pouvez modifier le paramètre de Registre. 
  
## <a name="create-registry-settings-to-disable-the-export-reports"></a>Créer des paramètres de Registre pour désactiver les rapports d’exportation

Effectuez la procédure suivante sur l’ordinateur que vous utiliserez pour exporter les résultats à une recherche de contenu.
  
1. Fermez l’outil d’exportation de découverte électronique Office 365 si elle est ouverte.
    
2. Effectuez une ou les deux étapes suivantes, en fonction de rapport d’exportation que vous souhaitez désactiver.
    
    - **Results.csv**
    
      Enregistrez le texte suivant dans un fichier de Registre Windows à l’aide d’un suffixe de nom de fichier de .reg ; par exemple, DisableResultsCsv.reg.
    
      ```
      Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultCsvEnabled /t REG_SZ /d False 
      ```

    - **Manifest.Xml**
    
      Enregistrez le texte suivant dans un fichier de Registre Windows à l’aide d’un suffixe de nom de fichier de .reg ; par exemple, DisableManifestXml.reg.
    
      ```
      Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultEdrmEnabled /t REG_SZ /d False 
      ```

3. Dans l’Explorateur Windows, cliquez sur ou double-cliquez sur le fichier .reg que vous avez créée lors des étapes précédentes.
    
4. Dans la fenêtre de contrôle d’accès utilisateur, cliquez sur **Oui** pour laisser l’Éditeur du Registre que la modification. 
    
5. Lorsque vous y êtes invité à continuer, cliquez sur **Oui**.
    
    L’Éditeur du Registre affiche un message indiquant que le paramètre a été correctement ajouté au Registre.
  
## <a name="edit-registry-settings-to-re-enable-the-export-reports"></a>Modifier les paramètres de Registre pour réactiver l’exportation des rapports

Si vous avez désactivé les rapports Results.csv et Manifest.xml en créant les fichiers .reg dans la procédure précédente, vous pouvez modifier ces fichiers pour réactiver un rapport afin qu’il est exporté avec les résultats de recherche. Là encore, effectuez la procédure suivante sur l’ordinateur que vous utiliserez pour exporter les résultats à une recherche de contenu.
  
1. Fermez l’outil d’exportation de découverte électronique Office 365 si elle est ouverte.
    
2. Modification des modification des fichiers .reg que vous avez créé dans la procédure précédente.
    
    - **Results.csv**
    
        Ouvrir le fichier DisableResultsCsv.reg dans le bloc-notes, modifiez la valeur `False` à `True`, puis enregistrez le fichier. Par exemple, une fois que vous avez modifié le fichier, il ressemble à ceci :
    
        ```
        Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultCsvEnabled /t REG_SZ /d True
        ```

    - **Manifest.Xml**
    
        Ouvrir le fichier DisableManifestXml.reg dans le bloc-notes, modifiez la valeur `False` à `True`, puis enregistrez le fichier. Par exemple, une fois que vous avez modifié le fichier, il ressemble à ceci :
    
      ```
      Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultEdrmEnabled /t REG_SZ /d True
      ```

3. Dans l’Explorateur Windows, cliquez sur ou double-cliquez sur un fichier .reg que vous avez modifié à l’étape précédente.
    
4. Dans la fenêtre de contrôle d’accès utilisateur, cliquez sur **Oui** pour laisser l’Éditeur du Registre que la modification. 
    
5. Lorsque vous y êtes invité à continuer, cliquez sur **Oui**.
    
    L’Éditeur du Registre affiche un message indiquant que le paramètre a été correctement ajouté au Registre.
  
## <a name="frequently-asked-questions-about-disabling-export-reports"></a>Forum aux questions sur la désactivation des rapports d’exportation
<a name="faqs"> </a>

 **Quels sont les rapports Results.csv et Manifest.xml ?**
  
Les fichiers Manifest.xml et les Results.csv contiennent plus d’informations sur le contenu qui a été exporté.
  
- **Results.csv** document Microsoft Excel qui contient des informations sur chaque élément qui peut être téléchargé comme un résultat de recherche. Pour le courrier électronique, le journal de résultat contient des informations sur chaque message, y compris : 
    
  - l’emplacement du message dans la boîte aux lettres source (notamment si le message est dans la boîte aux lettres principale ou d’archivage) ;
    
  - la date à laquelle le message a été envoyé ou reçu ;
    
  - l’objet du message ;
    
  - l’expéditeur et les destinataires du message.
    
  - Si le message est un message en double si vous avez activé la déduplication lors de l’exportation des résultats de la recherche. Les messages en double aura une valeur dans la colonne **Parent ItemId** qui identifie le message comme un doublon. La valeur dans la colonne **ID d’élément Parent** est identique à la valeur dans la colonne **DocumentId élément** du message qui a été exporté. 
    
    Pour les documents à partir de SharePoint et OneDrive pour les sites de l’entreprise, le journal de résultat contient des informations sur tous les documents, y compris :
    
  - l’URL du document ;
    
  - l’URL de la collection de sites qui héberge le document ;
    
  - la date à laquelle le document a été modifié pour la dernière fois ;
    
  - le nom du document (qui se trouve dans la colonne Objet du journal des résultats).
    
- Un manifest fichier **manifest.XML** (au format XML) qui contient des informations sur chaque élément inclus dans les résultats de recherche. Les informations contenues dans cet état sont identique à l’état Results.csv, mais il est au format spécifié par le modèle de référence découverte électronique (EDRM). Pour plus d’informations sur EDRM, accédez à [https://www.edrm.net](https://www.edrm.net).
    
 **Quand dois-je désactiver exportation ces rapports ?**
  
Cela dépend de vos besoins spécifiques. Bon nombre d’organisations ne nécessite pas plus d’informations sur les résultats de la recherche et n’avez pas besoin de ces rapports.
  
 **Quel ordinateur dois-je faire ?**
  
 Vous devez modifier le paramètre de Registre sur un ordinateur local que vous exécutez l’outil d’exportation de découverte électronique Office 365 sur. 
  
 **Après modification de ce paramètre, dois-je redémarrer l’ordinateur ?**
  
Non, vous n’êtes pas obligé de redémarrer l’ordinateur. Mais si l’outil d’exportation de découverte électronique Office 365 est en cours d’exécution, vous devez fermer, puis redémarrez après avoir modifié le paramètre de Registre.
  
 **Est une clé de Registre existante obtenir modifiée ou est une nouvelle clé sont créée ?**
  
Une nouvelle clé de Registre est créée la première fois que vous exécutez le fichier .reg que vous avez créé dans la procédure décrite dans cette rubrique. Puis le paramètre est modifié à chaque fois que vous modifiez et réexécutez la modifier le fichier .reg.
