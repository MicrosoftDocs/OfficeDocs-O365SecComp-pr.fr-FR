---
title: Exporter les résultats de la recherche de contenu du centre de sécurité & Office 365 Security
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.CustomizeExport
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: ed48d448-3714-4c42-85f5-10f75f6a4278
description: "ExPortez les résultats de la recherche à partir d'une recherche de contenu dans le centre de sécurité & de sécurité Office 365 vers un ordinateur local. Les résultats par courrier électronique sont exportés en tant que fichiers PST. Le contenu de sites SharePoint et OneDrive entreprise est exporté sous forme de documents Office natifs. "
ms.openlocfilehash: 5ec1456c7d1a787a1ede70c15b109e7f0358f60a
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219944"
---
# <a name="export-content-search-results-from-the-office-365-security--compliance-center"></a>Exporter les résultats de la recherche de contenu du centre de sécurité & Office 365 Security

Une fois qu'une recherche de contenu est exécutée correctement, vous pouvez exporter les résultats de la recherche vers un ordinateur local. Lorsque vous exportez les résultats de la messagerie, ceux-ci sont téléchargés sur votre ordinateur en tant que fichiers PST. Lorsque vous exportez du contenu à partir de sites SharePoint et OneDrive entreprise, des copies des documents Office natifs sont exportées. Des documents et rapports supplémentaires sont inclus dans les résultats de recherche exportés.
  
De plus, tous les messages électroniques chiffrés par RMS qui sont inclus dans les résultats d'une recherche de contenu sont déchiffrés lorsque vous les exportez (en tant que messages individuels). Cette fonctionnalité de déchiffrement est activée par défaut pour les membres du groupe de rôles gestionnaire de découverte électronique. Cela est dû au fait que le rôle de gestion de déChiffrement RMS est affecté à ce groupe de rôles. Pour plus d'informations sur le déchiffrement RMS lors de l'exportation des résultats de la recherche, voir la section [more information](#more-information) . 
  
L'exportation des résultats d'une recherche de contenu implique la préparation des résultats, puis leur téléchargement sur un ordinateur local.
  
## <a name="before-you-begin"></a>Avant de commencer

- Pour exporter les résultats de la recherche, vous devez disposer du rôle de gestion de l'exportation dans &amp; le centre de sécurité conformité Office 365. Ce rôle est affecté au groupe de rôles intégré du gestionnaire eDiscovery. Il n'est pas affecté par défaut au groupe de rôles gestion de l'organisation. Pour plus d'informations, consultez [la rubrique attribution d'autorisations eDiscovery dans &amp; le centre de sécurité conformité Office 365](assign-ediscovery-permissions.md).
    
- L’ordinateur que vous utilisez pour exporter les résultats de recherche doit répondre aux exigences système suivantes :
    
  - versions 32 ou 64 bits de Windows 7 et versions ultérieures
    
  - Microsoft .NET Framework 4,7
    
  - un navigateur pris en charge :
    
     - Microsoft Edge
    
        OU
    
     - Microsoft Internet Explorer 10 et versions ultérieures
    
    **Remarque:** Microsoft ne fabrique pas d'extensions ou de modules complémentaires tiers pour les applications ClickOnce. L'exportation des résultats de recherche à l'aide d'un navigateur non pris en charge avec des extensions ou des modules complémentaires tiers n'est pas prise en charge. 
    
- Lorsque vous téléchargez les résultats de recherche (décrit à l'étape 2), vous pouvez augmenter la vitesse de téléchargement en configurant un paramètre de Registre Windows sur l'ordinateur que vous utilisez pour exporter les résultats de la recherche. Pour plus d'informations, consultez [la rubrique augmentation de la vitesse de téléchargement lors de l'exportation des résultats de recherche eDiscovery à partir d'Office 365](increase-download-speeds-when-exporting-ediscovery-results.md).
    
- Lorsque vous exportez des résultats de recherche, les données sont stockées temporairement dans un emplacement de stockage Microsoft Azure unique dans le Cloud Microsoft avant d'être téléchargé sur votre ordinateur local. assurez-vous que votre organisation peut se connecter au point de terminaison dans Azure, c'est-à-dire ** \*. blob.core.windows.net** (le caractère générique représente un identificateur unique pour votre exportation). Les données de résultats de recherche sont supprimées de l'emplacement de stockage Azure deux semaines après sa création. 
    
- Si votre organisation utilise un serveur proxy pour communiquer avec Internet, vous devez définir les paramètres de serveur proxy sur l'ordinateur que vous utilisez pour exporter les résultats de la recherche (de sorte que l'outil d'exportation puisse être authentifié par votre serveur proxy). Pour ce faire, ouvrez le fichier *machine. config* à l'emplacement qui correspond à votre version de Windows. 
    
  - **32 bits** - `%windir%\Microsoft.NET\Framework\[version]\Config\machine.config`
    
  - **64 bits** - `%windir%\Microsoft.NET\Framework64\[version]\Config\machine.config`
    
    Ajoutez les lignes suivantes au fichier *machine. config* entre les `<configuration>` balises et `</configuration>` . N'oubliez pas de `ProxyServer` remplacer `Port` et d'utiliser les valeurs appropriées pour votre organisation; par exemple, `proxy01.contoso.com:80` . 
    
    ```
    <system.net>
       <defaultProxy enabled="true" useDefaultCredentials="true">
         <proxy proxyaddress="http://ProxyServer :Port " 
                usesystemdefault="False" 
                bypassonlocal="True" 
                autoDetect="False" />
       </defaultProxy>
    </system.net>
    ```
    
## <a name="step-1-prepare-search-results-for-export"></a>Étape 1 : Préparer les résultats de recherche pour l’exportation

La première étape consiste à préparer les résultats de la recherche pour l'exportation. Lorsque vous préparez des résultats, ceux-ci sont téléchargés vers un emplacement de stockage Azure dans le Cloud Microsoft. Notez que le contenu provenant de boîtes aux lettres et de sites est téléchargé à un débit maximal de 2 Go par heure.
  
1. Accédez à la page [https://protection.office.com](https://protection.office.com).
    
2. Connectez-vous à Office 365 à l'aide de votre compte scolaire ou professionnel.
    
3. Dans le volet gauche du Centre de sécurité et de conformité, cliquez sur **Recherches &amp; enquêtes** \> **Recherche de contenu**.
    
4. Sur la page **recherche de contenu** , sélectionnez une recherche. 
    
5. Dans le volet Détails, sous **Exporter les résultats vers un ordinateur**, cliquez sur **Démarrer l’exportation**.
    
    > [!NOTE]
    > Si les résultats d’une recherche datent d’il y a plus de 7 jours, vous êtes invité à mettre à jour les résultats. Dans ce cas, annulez l’exportation, cliquez sur **Mettre à jour les résultats de recherche** dans le volet Détails de la recherche sélectionnée, puis redémarrez l’exportation lorsque les résultats sont mis à jour.  
  
6. Sur la page **Exporter les résultats de la recherche** , sous **options de sortie**, choisissez l'une des options suivantes:
    
    - Tous les éléments, à l'exception de ceux dont le format n'est pas reconnu, sont chiffrés ou n'ont pas été indexés pour d'autres raisons
    
    - Tous les éléments, y compris ceux dont le format n'est pas reconnu, sont chiffrés ou n'ont pas été indexés pour d'autres raisons
    
    - Seuls les éléments dont le format n'est pas reconnu sont chiffrés ou n'ont pas été indexés pour d'autres raisons.
    
    Consultez la section [plus d'informations](#more-information) pour obtenir une description du mode d'exportation des éléments partiellement indexés. Pour plus d'informations sur les éléments partiellement indexés, consultez la rubrique [éléments partiellement indexés dans la recherche de contenu](partially-indexed-items-in-content-search.md).
    
7. Sous **Exporter le contenu Exchange en tant que**, choisissez l'une des options suivantes:
    
    - **Un fichier PST pour chaque boîte aux lettres** -exporte un fichier PST pour chaque boîte aux lettres d'utilisateur qui contient les résultats de la recherche. Tous les résultats de la boîte aux lettres d'archivage de l'utilisateur sont inclus dans le même fichier PST. Notez que cette option reproduit la structure de dossiers de boîte aux lettres à partir de la boîte aux lettres source. 
    
    - **Un fichier PST contenant tous les messages** : exporte un seul fichier PST (nommé *Exchange. pst* ) qui contient les résultats de la recherche de toutes les boîtes aux lettres source incluses dans la recherche. Notez que cette option reproduit la structure de dossiers de boîte aux lettres pour chaque message. 
    
    - **Un fichier PST contenant tous les messages dans un dossier unique** : exporte les résultats de la recherche vers un fichier PST unique où tous les messages se trouvent dans un seul dossier de niveau supérieur. Cette option permet aux relecteurs de vérifier les éléments par ordre chronologique (les éléments sont triés par date d'envoi) sans avoir à naviguer dans la structure de dossiers de boîte aux lettres d'origine pour chaque élément. 
    
    - **Messages individuels** : exporte les résultats de recherche en tant que messages électroniques individuels au format. msg. Si vous sélectionnez cette option, les résultats de la recherche de messagerie sont exportés vers un dossier dans le système de fichiers. Le chemin d'accès du dossier pour les messages individuels est le même que celui utilisé si vous avez exporté les résultats vers des fichiers PST. 
    
      > [!IMPORTANT]
      > Pour déchiffrer les messages chiffrés par RMS lorsqu'ils sont exportés, vous devez exporter les résultats de la recherche de courrier électronique en tant que messages individuels. Les messages chiffrés resteront chiffrés si vous exportez les résultats de la recherche en tant que fichier PST. 
  
8. Activez la case à cocher **activer** la déduplication pour exclure les messages en double. Cette option n'est disponible que si les sources de contenu de la recherche incluent des dossiers publics ou des boîtes aux lettres Exchange. 
    
    Si vous sélectionnez cette option, une seule copie d'un message est exportée même si plusieurs copies du même message sont trouvées dans les boîtes aux lettres qui ont été recherchées. Le rapport exporter les résultats (Results. csv) contiendra une ligne pour chaque copie d'un message en double afin que vous puissiez identifier les boîtes aux lettres (ou dossiers publics) qui contiennent une copie du message dupliqué. Pour plus d'informations sur la déduplication et sur l'identification des éléments dupliqués, voir [déduplication dans les résultats de recherche de découverte électronique](de-duplication-in-ediscovery-search-results.md).
    
9. Cliquez sur la case à cocher **inclure les versions pour les documents SharePoint** pour exporter toutes les versions des documents SharePoint. Cette option n'est disponible que si les sources de contenu de la recherche incluent des sites SharePoint ou OneDrive entreprise. 
    
10. Cliquez sur la case à cocher **Exporter les fichiers dans un dossier compressé (zippé)** pour exporter les résultats de recherche dans des dossiers compressés. Cette option est disponible uniquement lorsque vous choisissez d'exporter les éléments Exchange en tant que messages individuels et lorsque les résultats de la recherche incluent des documents SharePoint ou OneDrive. Cette option est principalement utilisée pour contourner la limite de 260 caractères dans les noms de chemin d'accès des fichiers Windows lorsque les éléments sont exportés. Voir «noms de fichier des éléments exportés» dans la section [plus d'informations](#more-information) . 
    
11. Cliquez sur **Démarrer l’exportation**.
    
    Les résultats de la recherche sont préparés pour le téléchargement, ce qui signifie qu'ils sont téléchargés vers l'emplacement de stockage Azure dans le Cloud Microsoft. Lorsque les résultats de la recherche sont prêts à être téléchargés, le lien **Télécharger les résultats** exportés s'affiche sous **Exporter les résultats vers un ordinateur** dans le volet d'informations. 
  
## <a name="step-2-download-the-search-results"></a>Étape 2 : Télécharger les résultats de recherche

L'étape suivante consiste à télécharger les résultats de la recherche à partir de l'emplacement de stockage Azure vers votre ordinateur local.
  
Comme expliqué précédemment, vous pouvez augmenter la vitesse de téléchargement en configurant un paramètre de Registre Windows sur l'ordinateur que vous utilisez pour exporter les résultats de la recherche. Pour plus d'informations, consultez [la rubrique augmentation de la vitesse de téléchargement lors de l'exportation des résultats de recherche eDiscovery à partir d'Office 365](increase-download-speeds-when-exporting-ediscovery-results.md).
  
1. Dans le volet Détails de la recherche pour laquelle vous avez démarré l’exportation, sous **Exporter les résultats vers un ordinateur**, cliquez sur **Télécharger les résultats exportés**.
    
    La fenêtre **Télécharger les résultats** exportés s'affiche et contient les informations suivantes sur les résultats de la recherche qui seront téléchargés sur votre ordinateur. 
    
    - Le nombre d’éléments à télécharger.
    
    - La taille totale estimée des éléments à télécharger.
    
    - Si les éléments indexés ou non indexés seront exportés. Les éléments non indexés sont des éléments qui ont un format reconnu, qui sont chiffrés ou n’ont pas été indexés pour d’autres raisons. Pour plus d’informations, consultez la rubrique [Unindexed items in Content Search](partially-indexed-items-in-content-search.md).
    
    - Si les versions des documents SharePoint seront téléchargés.
    
    - L’état de la préparation. Vous pouvez commencer à télécharger les résultats de recherche, même si la préparation des données n’est pas terminée.
    
2. Sous **Clé d’exportation**, cliquez sur **Copier dans le Presse-papiers**. Cette clé vous permet de télécharger les résultats de recherche à l’étape 5.
    
    > [!NOTE]
    > Étant donné que tout le monde peut installer et lancer l’outil d’exportation de découverte électronique, et utiliser cette clé pour télécharger les résultats de recherche, prenez toutes les précautions nécessaires pour protéger cette clé, comme vous le feriez avec les mots de passe ou d’autres informations de sécurité.  
  
3. Cliquez sur **Télécharger les résultats**.
    
4. Si vous êtes invité à installer l' **outil d'exportation de découverte électronique MicrosoftOffice 365**, cliquez sur **installer**.
    
5. Dans l’**outil d’exportation de découverte électronique**, collez la clé d’exportation que vous avez copiée à l’étape 2 dans la zone appropriée. 
    
6. Cliquez sur **Parcourir** pour spécifier l’emplacement de téléchargement du fichier des résultats de recherche. 
    
    > [!NOTE]
    > En raison de la quantité élevée d'activité disque (lectures et écritures), vous devez télécharger les résultats de la recherche sur un disque dur local; ne les téléchargez pas sur un lecteur réseau mappé ni sur un autre emplacement réseau. 
  
1. Cliquez sur **Démarrer** pour télécharger les résultats de recherche sur votre ordinateur. 
    
    L' **outil d'exportation de découverte électronique** affiche des informations d'État sur le processus d'exportation, y compris une estimation du nombre (et de la taille) des éléments restants à télécharger. Une fois le processus d'exportation terminé, vous pouvez accéder aux fichiers à l'emplacement où ils ont été téléchargés. 
    

  
## <a name="more-information"></a>Plus d’informations

Voici plus d'informations sur l'exportation des résultats de la recherche.
  
[Exporter des limites](#export-limits)
  
[Exporter des rapports](#export-reports)
  
[Exportation d'éléments partiellement indexés](#exporting-partially-indexed-items)

[Exportation de messages individuels ou de fichiers PST](#exporting-individual-messages-or-pst-files)
  
[DéChiffrement des messages chiffrés RMS](#decrypting-rms-encrypted-messages)

[Noms de fichier des éléments exportés](#filenames-of-exported-items)  
  
[Divers](#miscellaneous)
  
 ### <a name="export-limits"></a>Exporter des limites
  
- L'exportation des résultats de recherche &amp; à partir du centre de sécurité conformité présente les limites suivantes:
    
  - Vous pouvez exporter un maximum de 2 to de données à partir d'une seule recherche de contenu. Si les résultats de la recherche sont supérieurs à 2 to, envisagez d'utiliser des plages de dates ou d'autres types de filtres pour réduire la taille totale des résultats de la recherche.
    
  - Votre organisation peut exporter un maximum de 2 to de données pendant un seul jour.
    
  - 10 exportations maximum peuvent être exécutées simultanément au sein de votre organisation.
    
  - Un utilisateur peut exécuter un maximum de trois exportations en même temps.

  > [!NOTE]
  > L'exportation des rapports à partir d'une recherche de contenu permet également de compter sur le nombre d'exportations exécutées en même temps et le nombre d'exportations qu'un utilisateur unique peut exécuter.
    
- Comme indiqué précédemment, les résultats de la recherche provenant de boîtes aux lettres et de sites sont téléchargés vers l'emplacement de stockage Azure (comme décrit dans l' [étape 1: préparer les résultats de recherche pour l'exportation](#step-1-prepare-search-results-for-export)) à un débit maximal de 2 Go par heure.
    
- Par défaut, la taille maximale d'un fichier PST pouvant être exporté est de 10 Go. Cela signifie que si les résultats de la recherche de la boîte aux lettres d'un utilisateur sont supérieurs à 10 Go, les résultats de la recherche de la boîte aux lettres seront exportés dans deux (ou plusieurs) fichiers PST distincts. En outre, si vous choisissez d'exporter tous les résultats de recherche dans un seul fichier PST, le fichier PST sera Spilt dans des fichiers PST supplémentaires si la taille totale des résultats de la recherche est supérieure à 10 Go. Si vous souhaitez modifier cette taille par défaut, vous pouvez modifier le Registre Windows sur l'ordinateur que vous utilisez pour exporter les résultats de la recherche. Consultez [la rubrique modifier la taille des fichiers PST lors de l'exportation des résultats de recherche eDiscovery](change-the-size-of-pst-files-when-exporting-results.md).
    
    De plus, les résultats de recherche d'une boîte aux lettres spécifique ne sont pas réparties entre plusieurs fichiers PST, sauf si le contenu d'une boîte aux lettres unique est supérieur à 10 Go. Si vous avez choisi d'exporter les résultats de la recherche dans un fichier PST pour qui contient tous les messages dans un seul dossier et que les résultats de la recherche sont supérieurs à 10 Go, les éléments sont toujours organisés par ordre chronologique, de sorte qu'ils seront Spilt dans des fichiers PST supplémentaires en fonction du d r.
     
 ### <a name="export-reports"></a>Exporter des rapports
  
- Lorsque vous exportez des résultats de recherche, les rapports suivants sont inclus en plus des résultats de la recherche.
    
  - **Exporter le résumé** Document Excel qui contient un résumé de l'exportation. Cela inclut des informations telles que le nombre de sources de contenu qui ont été recherchées, les tailles estimées et téléchargées des résultats de recherche, ainsi que le nombre d'éléments estimés et téléchargés qui ont été exportés. 
    
  - **Manifeste** Fichier manifeste (au format XML) qui contient des informations sur chaque élément inclus dans les résultats de la recherche. 
    
  - **Résultats** Document Excel qui contient des informations sur chaque élément téléchargé en tant que résultat de la recherche. Pour le courrier électronique, le journal des résultats contient des informations sur chaque message, notamment: 
    
      - l’emplacement du message dans la boîte aux lettres source (notamment si le message est dans la boîte aux lettres principale ou d’archivage) ;
        
      - la date à laquelle le message a été envoyé ou reçu ;
        
      - l’objet du message ;
        
      - l’expéditeur et les destinataires du message.
        
      - S'il s'agit d'un message en double si vous avez activé l'option de déduplication lors de l'exportation des résultats de la recherche. Les messages en double contiennent une valeur dans la colonne **dupliquer à l'élément** qui identifie le message en tant que doublon. La valeur dans la colonne **dupliquer vers l'élément** contient l'identité de l'élément qui a été exporté. Pour plus d'informations, consultez la rubrique [déduplication dans les résultats de recherche de découverte électronique](de-duplication-in-ediscovery-search-results.md).
        
      Pour les documents provenant de sites SharePoint et OneDrive entreprise, le journal des résultats contient des informations sur chaque document, notamment:
        
      - l’URL du document ;
        
      - l’URL de la collection de sites qui héberge le document ;
        
      - la date à laquelle le document a été modifié pour la dernière fois ;
        
      - le nom du document (qui se trouve dans la colonne Objet du journal des résultats).
    
  - **Éléments** non indexés Document Excel qui contient des informations sur les éléments partiellement indexés qui seraient inclus dans les résultats de la recherche. Si vous n'incluez pas les éléments partiellement indexés lorsque vous générez le rapport des résultats de la recherche, ce rapport sera toujours téléchargé, mais il sera vide. 
    
  - **Erreurs et avertissements** Contient des erreurs et des avertissements pour les fichiers rencontrés lors de l'exportation. Consultez la colonne Détails de l'erreur pour obtenir des informations spécifiques sur chaque erreur ou avertissement. 
    
  - **Éléments ignorés** Lorsque vous exportez des résultats de recherche à partir de sites SharePoint et OneDrive entreprise, l'exportation inclut généralement un rapport éléments ignorés (SkippedItems. csv). Les éléments cités dans ce rapport sont généralement des éléments qui ne sont pas téléchargés, tels qu'un dossier ou un ensemble de documents. Ne pas exporter ces types d'éléments est par conception. Pour les autres éléments ignorés, le champ «type d'erreur» et «détails de l'erreur» dans le rapport éléments ignorés indiquent la raison pour laquelle l'élément a été ignoré et n'a pas été téléchargé avec les autres résultats de la recherche. 
    
  - **Journal de suivi** Contient des informations de journalisation détaillées sur le processus d'exportation et peut vous aider à découvrir des problèmes lors de l'exportation. 
    
    > [!NOTE]
    > Vous pouvez simplement exporter ces documents sans avoir à exporter les résultats de la recherche. Consultez [la rubrique Exporter un rapport de recherche de contenu](export-a-content-search-report.md). 
  
 ### <a name="exporting-partially-indexed-items"></a>Exportation d'éléments partiellement indexés
  
- Si vous exportez des éléments de boîte aux lettres à partir d'une recherche de contenu qui renvoie tous les éléments de boîte aux lettres dans les résultats de la recherche (car aucun mot clé n'est inclus dans la requête de recherche), les éléments partiellement indexés ne sont pas copiés dans le fichier PST contenant les éléments non indexés. Cela est dû au fait que tous les éléments, y compris les éléments partiellement indexés, sont automatiquement inclus dans les résultats de la recherche standard. Cela signifie que les éléments partiellement indexés sont inclus dans un fichier PST (ou sous forme de messages individuels) qui contient les autres éléments indexés.
    
    En outre, si vous exportez les éléments indexés et partiellement indexés ou si vous exportez uniquement les éléments indexés à partir d'une recherche de contenu qui renvoie tous les éléments, le même nombre d'éléments sera téléchargé. Cela se produit bien que les résultats de recherche estimés pour la recherche de contenu (affichés dans les statistiques &amp; de recherche dans le centre de sécurité conformité) incluent toujours une estimation distincte pour le nombre d'éléments partiellement indexés. Par exemple, supposons que l'estimation d'une recherche incluant tous les éléments (pas de mot-clé dans la requête de recherche) indique qu' 1 000 éléments ont été trouvés et que 200 éléments partiellement indexés étaient également trouvés. Dans ce cas, les éléments 1 000 incluent les éléments partiellement indexés, car la recherche renvoie tous les éléments. En d'autres termes, 1 000 nombre total d'éléments renvoyés par la recherche, et non pas 1 200 éléments (comme prévu). Si vous exportez les résultats de cette recherche et choisissez d'exporter des éléments indexés et partiellement indexés (ou simplement des éléments indexés), 1 000 éléments seront téléchargés. Là encore, cela est dû au fait que les éléments partiellement indexés sont inclus dans les résultats réguliers (indexés) lorsque vous utilisez une requête de recherche vierge pour renvoyer tous les éléments. Dans le même exemple, si vous choisissez d'exporter uniquement des éléments partiellement indexés, seuls les éléments non indexés 200 seront téléchargés.
    
    Notez également que dans l'exemple précédent (lorsque vous exportez des éléments indexés et partiellement indexés ou que vous exportez uniquement des éléments indexés), le rapport de **synthèse d'exportation** inclus avec les résultats de recherche exportés répertorie 1 000 éléments estimés et 1 000 téléchargé éléments pour les mêmes raisons que celles décrites précédemment. 
    
- Si la recherche à partir de laquelle vous exportez les résultats est une recherche d'emplacements de contenu spécifiques ou de tous les emplacements de contenu de votre organisation, seuls les éléments partiels des emplacements de contenu contenant des éléments qui correspondent aux critères de recherche seront exportés. En d'autres termes, si aucun résultat de recherche n'est trouvé dans une boîte aux lettres ou un site, tous les éléments partiellement indexés de cette boîte aux lettres ou ce site ne seront pas exportés. Cela est dû au fait que l'exportation d'éléments partiellement indexés à partir de nombreux emplacements de l'organisation peut augmenter la probabilité d'erreurs d'exportation et augmenter le temps nécessaire pour exporter et télécharger les résultats de la recherche.
    
    Pour exporter des éléments partiellement indexés de tous les emplacements de contenu pour une recherche, configurez la recherche de sorte qu'elle renvoie tous les éléments (en supprimant les mots clés de la requête de recherche), puis exportez uniquement les éléments partiellement indexés lorsque vous exportez les résultats de la recherche.
    
    ![Utiliser l'option d'exportation Thrid pour exporter uniquement les éléments non indexés](media/5d7be338-a0e5-425f-8ba5-92769c24bf75.png)
  
- Lors de l'exportation des résultats de recherche à partir de sites SharePoint ou OneDrive entreprise, la possibilité d'exporter des éléments non indexés dépend également de l'option d'exportation que vous sélectionnez et selon que le site recherché contient un élément indexé correspondant aux critères de recherche. Par exemple, si vous recherchez des sites SharePoint ou OneDrive entreprise spécifiques et qu'aucun résultat de recherche n'est trouvé, les éléments non indexés de ces sites ne seront pas exportés si vous choisissez la deuxième option d'exportation pour exporter les éléments indexés et non indexés. Si un élément indexé d'un site correspond aux critères de recherche, tous les éléments non indexés de ce site seront exportés lors de l'exportation des éléments indexés et non indexés. L'illustration suivante décrit les options d'exportation selon que le site contient ou non un élément indexé correspondant aux critères de recherche.
    
    ![Choisissez l'option Exporter en fonction du fait qu'un site contient ou non un élément indexé correspondant aux critères de recherche.](media/94f78786-c6bb-42fb-96b3-7ea3998bcd39.png)

    
    Seuls les éléments indexés qui correspondent aux critères de recherche sont exportés. Aucun élément indexé partiellement n'est exporté.
    
    B-si aucun élément indexé d'un site ne correspond aux critères de recherche, alors les éléments partiellement indexés de ce site ne sont pas exportés. Si les éléments indexés d'un site sont renvoyés dans les résultats de la recherche, les éléments partiellement indexés de ce site sont exportés. En d'autres termes, seuls les éléments partiellement indexés des sites qui contiennent des éléments correspondant aux critères de recherche sont exportés.
    
    C-tous les éléments partiellement indexés de tous les sites de la recherche sont exportés, qu'un site contienne ou non des éléments qui correspondent aux critères de recherche.
    
    Si vous choisissez d'exporter des éléments partiellement indexés, les éléments de boîte aux lettres partiellement indexés sont exportés dans un fichier PST distinct quelle que soit l'option sélectionnée sous **Exporter le contenu Exchange en tant que**.

- Si des éléments partiellement indexés sont renvoyés dans les résultats de la recherche (étant donné que les autres propriétés d'un élément partiellement indexé correspondent aux critères de recherche), ces éléments partiellement indexés sont exportés avec les résultats de la recherche standard. Par conséquent, si vous choisissez d'exporter des éléments indexés et des éléments partiellement indexés (en sélectionnant l'option **tous les éléments, y compris ceux dont le format n'est pas reconnu, sont chiffrés ou n'ont pas été indexés pour d'autres raisons** ), les éléments partiellement indexés exportés les résultats réguliers seront affichés dans le rapport results. csv. Elles ne seront pas mentionnées dans le rapport éléments non indexés. csv.
    
 ### <a name="exporting-individual-messages-or-pst-files"></a>Exportation de messages individuels ou de fichiers PST
  
- Si le nom du chemin d'accès du fichier d'un message dépasse la limite de caractères maximale pour Windows, le nom du chemin d'accès du fichier est tronqué. Mais le nom du chemin d'accès du fichier d'origine est affiché dans le manifeste et ResultsLog.
    
- Comme expliqué précédemment, les résultats de la recherche de messagerie sont exportés vers un dossier dans le système de fichiers. Le chemin d'accès du dossier pour les messages individuels réplique le chemin d'accès au dossier dans la boîte aux lettres de l'utilisateur. Par exemple, pour une recherche nommée «ContosoCase101», les messages de la boîte de réception d'un utilisateur se trouveraient dans le chemin d'accès `~ContosoCase101\\<date of export\Exchange\user@contoso.com (Primary)\Top of Information Store\Inbox`du dossier. 
    
- Si vous choisissez d'exporter les messages électroniques dans un fichier PST contenant tous les messages d'un seul dossier, un dossier **éléments supprimés** et un dossier **dossiers de recherche** sont inclus dans le niveau supérieur du dossier PST. Ces dossiers seront vides. 
  
 ### <a name="decrypting-rms-encrypted-messages"></a>DéChiffrement des messages chiffrés RMS
  
- Comme expliqué précédemment, pour déchiffrer les messages chiffrés RMS lorsque vous les exportez, vous devez exporter les résultats de la recherche en tant que messages individuels. Si vous exportez des résultats de recherche vers un fichier PST, les messages chiffrés RMS resteront chiffrés.
    
- La fonctionnalité de déchiffrement RMS dans la recherche de contenu ne déchiffre pas les messages chiffrés avec le chiffrement de messages Office 365 (OME) lorsque vous exportez des résultats de recherche. Toutefois, si un message chiffré avec OME est envoyé par un utilisateur de votre organisation, la copie du message dans le dossier envoyé de l'utilisateur n'est pas chiffrée et sera visible après son exportation. Toutefois, si des messages chiffrés avec OME sont reçus par des utilisateurs de votre organisation, ils ne seront pas déchiffrés après leur exportation. Pour plus d'informations sur OME, consultez la rubrique [Office 365 message](https://go.microsoft.com/fwlink/p/?linkid=844966)Encryption.
    
- Les messages déchiffrés sont identifiés dans le rapport **ResultsLog** . Ce rapport contient une colonne nommée **Decode Status**et une valeur décodée dans cette colonne identifie les messages déchiffrés. **** 
    
- Actuellement, cette fonctionnalité de déchiffrement n'inclut pas le contenu chiffré de sites SharePoint et OneDrive entreprise. Seuls les messages électroniques chiffrés RMS seront déchiffrés lors de leur exportation.
    
- Si un message électronique chiffré RMS comporte une pièce jointe (par exemple, un document ou un autre message électronique) qui est également chiffrée, seul le message électronique de niveau supérieur est déchiffré.
    
- Vous ne pouvez pas prévisualiser un message électronique chiffré par RMS. Pour afficher un message chiffré, vous devez l'exporter.
    
- Si vous devez empêcher quelqu'un de déchiffrer des messages chiffrés par RMS, vous devez créer un groupe de rôles personnalisé (en copiant le groupe de rôles intégré du gestionnaire eDiscovery), puis supprimer le rôle de gestion de déChiffrement RMS du groupe de rôles personnalisé. Ajoutez ensuite la personne dont vous ne voulez pas déchiffrer les messages en tant que membre du groupe de rôles personnalisé.
  
 ### <a name="filenames-of-exported-items"></a>Noms de fichier des éléments exportés
  
- Il existe une limite de 260 caractères (imposée par le système d'exploitation) pour le chemin d'accès complet des messages électroniques et des documents de site exportés vers votre ordinateur local. Le chemin d'accès complet des éléments exportés inclut l'emplacement d'origine de l'élément et l'emplacement du dossier sur l'ordinateur local où les résultats de la recherche sont téléchargés. Par exemple, si vous spécifiez de télécharger les résultats de `C:\Users\Admin\Desktop\SearchResults` la recherche dans dans l'outil d'exportation de découverte électronique, le nom de chemin complet `C:\Users\Admin\Desktop\SearchResults\ContentSearch1\03.15.2017-1242PM\Exchange\sarad@contoso.com (Primary)\Top of Information Store\Inbox\Insider trading investigation.msg`d'un élément de courrier téléchargé serait.
    
    Si la limite de 260 caractères est dépassée, le chemin d'accès complet d'un élément est tronqué.
    
  - Si le chemin d'accès complet est plus long que 260 caractères, le nom du fichier sera raccourci pour s'afficher sous la limite; Notez que le nom de fichier tronqué (à l'exception de l'extension de fichier) ne doit pas être inférieur à 8 caractères.
    
  - Si le nom du chemin d'accès complet reste trop long après avoir raccourci le nom du fichier, l'élément est déplacé de son emplacement actuel vers le dossier parent. Si le chemin d'accès est toujours trop long, le processus est répété: raccourcissez le nom de fichier et, le cas échéant, déplacez-le de nouveau vers le dossier parent. Ce processus est répété jusqu'à ce que le chemin d'accès complet se trouve au-dessous de la limite de 260 caractères.
    
  - S'il existe déjà un nom de chemin d'accès complet tronqué, un numéro de version est ajouté à la fin du nom de fichier; par exemple, `statusmessage(2).msg`.
    
    Pour aider à atténuer ce problème, envisagez de télécharger les résultats de recherche vers un emplacement avec un nom de chemin d'accès court; par exemple, le téléchargement des résultats de recherche dans `C:\Results` un dossier nommé ajoute des caractères aux noms de chemin d'accès des éléments exportés de `C:\Users\Admin\Desktop\Results`sorte qu'ils ne les téléchargent pas dans un dossier nommé.
    
- Lorsque vous exportez des documents de site, il est également possible que le nom de fichier d'origine d'un document soit modifié. Cela se produit spécifiquement pour les documents qui ont été supprimés d'un site SharePoint ou OneDrive entreprise qui a été mis en attente. Après la suppression d'un document situé sur un site en conservation, le document supprimé est automatiquement déplacé vers la bibliothèque de conservation de conservation pour le site (qui a été créé lors de la mise en attente du site). Lorsque le document supprimé est déplacé vers la bibliothèque de conservation de conservation, un ID généré de manière aléatoire et unique est ajouté au nom de fichier d'origine du document. Par exemple, si le nom de fichier d'un `FY2017Budget.xlsx` document est supprimé par la suite et déplacé vers la bibliothèque de conservation, le nom de fichier du document déplacé vers la bibliothèque de conservation de conservation est modifié comme suit `FY2017Budget_DEAF727D-0478-4A7F-87DE-5487F033C81A2000-07-05T10-37-55.xlsx`. Si un document de la bibliothèque de conservation de conservation correspond à la requête d'une recherche de contenu et que vous exportez les résultats de cette recherche, le nom de fichier est modifié dans le fichier exporté. dans cet exemple, le nom de fichier du document exporté est `FY2017Budget_DEAF727D-0478-4A7F-87DE-5487F033C81A2000-07-05T10-37-55.xlsx`.
    
    De plus, lorsqu'un document situé sur un site en conservation est modifié (et que le contrôle de version de la bibliothèque de documents du site a été activé), une copie du fichier est automatiquement créée dans la bibliothèque de conservation de conservation. Dans ce cas, un ID unique et généré de manière aléatoire est également ajouté au nom de fichier du document qui est copié dans la bibliothèque de conservation de conservation.
    
    La raison pour laquelle les noms de fichier des documents qui ont été déplacés ou copiés vers la bibliothèque de conservation de conservation est d'empêcher les noms de fichier conflictuels. Pour plus d'informations sur l'insertion d'une conservation sur les sites et la bibliothèque de conservation des données, voir vue d'ensemble de la conservation inaltérable [dans SharePoint Server 2016](https://support.office.com/article/5e400d68-cd51-444a-8fe6-e4df1d20aa95).
    
 ### <a name="miscellaneous"></a>Divers
  
- Tous les résultats de recherche et les rapports d'exportation sont inclus dans un dossier portant le même nom que la recherche de contenu. Les messages électroniques qui ont été exportés se trouvent dans un dossier nommé **Exchange**. Les documents se trouvent dans un dossier nommé **SharePoint**. 
    
- Les métadonnées du système de fichiers pour les documents sur les sites SharePoint et OneDrive entreprise sont conservées lorsque les documents sont exportés vers votre ordinateur local. Cela signifie que les propriétés de document, telles que créées et les dates de dernière modification, ne sont pas modifiées lorsque les documents sont exportés.

- Si les résultats de la recherche incluent un élément de liste de SharePoint qui correspond à la requête de recherche, toutes les lignes de la liste seront exportées en plus de l'élément correspondant à la requête de recherche. Cela inclut toutes les pièces jointes de la liste. La raison est de fournir un contexte pour les éléments de liste qui sont renvoyés dans les résultats de la recherche. Notez également que les éléments de liste et les pièces jointes supplémentaires peuvent entraîner une différence entre le nombre d'éléments exportés et l'estimation des résultats de la recherche.
