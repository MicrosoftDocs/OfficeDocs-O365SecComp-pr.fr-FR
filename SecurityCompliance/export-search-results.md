---
title: Exporter les résultats de recherche de contenu à partir de la sécurité de 365 Office &amp; centre de conformité
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/22/2018
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.CustomizeExport
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: ed48d448-3714-4c42-85f5-10f75f6a4278
description: 'Exporter les résultats de recherche à partir d’une recherche de contenu de sécurité Office 365 &amp; centre de conformité à un ordinateur local. Résultats de la messagerie Emaill sont exportées dans des fichiers PST. Contenu de SharePoint et OneDrive pour les sites sont exportées dans des documents Office natives. '
ms.openlocfilehash: 9b6db129371b234713b5504f5763ee1dc3d7d638
ms.sourcegitcommit: bf70ec8e11b3f75bf45cd4f760cd1a982593dbad
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/22/2018
ms.locfileid: "24962960"
---
# <a name="export-content-search-results-from-the-office-365-security-amp-compliance-center"></a>Exporter les résultats de recherche de contenu à partir de la sécurité de 365 Office &amp; centre de conformité

Après qu’une recherche de contenu est exécutée correctement, vous pouvez exporter les résultats de recherche sur un ordinateur local. Lorsque vous exportez des résultats de la messagerie, elles sont téléchargées sur votre ordinateur en tant que fichiers PST. Lorsque vous exportez le contenu à partir de SharePoint et OneDrive pour les sites, les copies des documents Office natifs sont exportées. Il existe des documents et des rapports qui sont inclus dans les résultats de recherche exportés.
  
En outre, tous les messages électroniques chiffrés RMS qui sont inclus dans les résultats d’une recherche de contenu seront déchiffrés lorsque vous exportez les (comme des messages). Cette fonctionnalité de déchiffrement est activée par défaut pour les membres du groupe de rôles gestionnaire eDiscovery. Il s’agit, car le rôle de gestion de déchiffrement RMS est affecté à ce groupe de rôles. Voir la section [plus d’informations](#more-information) pour plus d’informations sur le déchiffrement RMS lorsque vous exportez des résultats de la recherche. 
  
Exporter les résultats d’une recherche de contenu consiste à préparer les résultats, puis de les télécharger sur un ordinateur local.
  
## <a name="before-you-begin"></a>Avant de commencer

- Pour exporter les résultats de la recherche, vous devez attribuer le rôle de gestion d’exportation de sécurité Office 365 &amp; centre de conformité. Ce rôle est attribué au groupe de rôles intégrés eDiscovery Manager. Il n’est pas affecté par défaut au groupe de rôles de gestion de l’organisation. Pour plus d’informations, voir [attribuer des autorisations de sécurité Office 365 eDiscovery &amp; centre de conformité](assign-ediscovery-permissions.md).
    
- L’ordinateur que vous utilisez pour exporter les résultats de recherche doit répondre aux exigences système suivantes :
    
  - versions 32 ou 64 bits de Windows 7 et versions ultérieures
    
  - Microsoft .NET Framework 4.7
    
  - un navigateur pris en charge :
    
     - Microsoft Edge
    
        OU
    
     - Microsoft Internet Explorer 10 et versions ultérieures
    
    **Remarque :** Microsoft ne fabrique extensions tierces ou les modules complémentaires pour les applications ClickOnce. Exportation des résultats de recherche à l’aide d’un navigateur non pris en charge avec des extensions tierces ou les modules complémentaires n’est pas pris en charge. 
    
- Lorsque vous téléchargez des résultats de la recherche (décrits à l’étape 2), vous pouvez augmenter la vitesse de téléchargement en configurant un paramètre de Registre Windows sur l’ordinateur que vous utilisez pour exporter les résultats de recherche. Pour plus d’informations, voir [augmenter la vitesse de téléchargement lors de l’exportation des résultats de recherche de découverte électronique à partir d’Office 365](increase-download-speeds-when-exporting-ediscovery-results.md).
    
- Lorsque vous exportez des résultats de la recherche, les données sont stockées temporairement dans un emplacement de stockage unique Microsoft Azure dans le nuage Microsoft avant qu’il est téléchargé sur votre ordinateur local. Vérifiez que votre organisation peut se connecter au point de terminaison dans Azure, qui est ** \*. blob.core.windows.net** (le caractère générique représente un identificateur unique pour votre exportation). Les données de résultats de recherche sont supprimées de l’emplacement de stockage Azure deux semaines après sa création. 
    
- Si votre organisation utilise un serveur proxy pour communiquer avec Internet, vous devez définir les paramètres du serveur proxy sur l’ordinateur qui vous permet d’exporter les résultats de recherche (de sorte que l’outil d’exportation pouvant être authentifié par votre serveur proxy). Pour ce faire, ouvrez le fichier *machine.config* à l’emplacement qui correspond à votre version de Windows. 
    
  - **32 bits** - `%windir%\Microsoft.NET\Framework\[version]\Config\machine.config`
    
  - **64 bits** - `%windir%\Microsoft.NET\Framework64\[version]\Config\machine.config`
    
    Ajoutez les lignes suivantes au fichier *machine.config* quelque part entre le `<configuration>` et `</configuration>` balises. Veillez à remplacer `ProxyServer` et `Port` avec les valeurs appropriées pour votre organisation ; par exemple, `proxy01.contoso.com:80` . 
    
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

- Voir la section pour obtenir une description des limites pour l’exportation des résultats de la recherche. 
    
- La taille maximale d’un fichier PST qui peut être exporté est de 10 Go. Si vous souhaitez modifier cette taille par défaut, vous pouvez modifier le Registre Windows sur l’ordinateur que vous utilisez pour exporter les résultats de recherche. Voir [modification de la taille des fichiers PST lors de l’exportation des résultats de recherche eDiscovery](change-the-size-of-pst-files-when-exporting-results.md).
    
## <a name="step-1-prepare-search-results-for-export"></a>Étape 1 : Préparer les résultats de recherche pour l’exportation

La première étape consiste à préparer les résultats de recherche pour l’exportation. Lorsque vous préparez des résultats, ils sont téléchargés vers un emplacement de stockage Azure dans le nuage Microsoft. Notez que le contenu des sites et des boîtes aux lettres est téléchargé au taux maximal de 2 Go par heure.
  
1. Accédez à [https://protection.office.com](https://protection.office.com).
    
2. Connectez-vous à Office 365 à l’aide de votre compte professionnel ou de l’école.
    
3. Dans le volet gauche du Centre de sécurité et de conformité, cliquez sur **Recherches &amp; enquêtes** \> **Recherche de contenu**.
    
4. Dans la page de **recherche de contenu** , sélectionnez une recherche. 
    
5. Dans le volet Détails, sous **Exporter les résultats vers un ordinateur**, cliquez sur **Démarrer l’exportation**.
    
    > [!NOTE]
    > Si les résultats d’une recherche datent d’il y a plus de 7 jours, vous êtes invité à mettre à jour les résultats. Dans ce cas, annulez l’exportation, cliquez sur **Mettre à jour les résultats de recherche** dans le volet Détails de la recherche sélectionnée, puis redémarrez l’exportation lorsque les résultats sont mis à jour.  
  
6. Dans la page **Exporter les résultats de recherche** , sous **inclure ces éléments de la recherche**, choisissez une des options suivantes :
    
    - exporter uniquement les éléments indexés ;
    
    - Exporter les éléments indexés et partiellement indexés
    
    - Exporter les éléments indexés partiellement uniquement
    
    Voir la section [plus d’informations](#more-information) pour une description des éléments indexés comment partiellement sont exportées. Pour plus d’informations sur les éléments indexés partiellement, voir [partiellement indexé des éléments de recherche de contenu](partially-indexed-items-in-content-search.md).
    
7. Sous **contenu Exchange exporter en tant que**, choisissez une des options suivantes :
    
    - **Un fichier pour chaque boîte aux lettres** - exporte un fichier PST pour chaque boîte aux lettres d’utilisateur qui contient les résultats de la recherche. Tous les résultats de la boîte aux lettres de l’utilisateur archive sont inclus dans le même fichier PST. Notez que cette option reproduit la structure de dossiers de boîte aux lettres à partir de la boîte aux lettres source. 
    
    - **Un fichier contenant tous les messages** - exporte un seul fichier PST (appelé *Exchange.pst* ) qui contient les résultats de recherche à partir de toutes les boîtes aux lettres sources inclus dans la recherche. Notez que cette option reproduit la structure de dossiers de boîte aux lettres pour chaque message. 
    
    - **Un fichier contenant tous les messages dans un dossier unique** - exporte les résultats de recherche vers un fichier PST unique où tous les messages sont situés dans un dossier de niveau supérieur unique. Cette option permet aux réviseurs de consulter des éléments dans l’ordre chronologique (les éléments sont triés par date d’envoi) sans devoir quitter la structure de dossiers de boîte aux lettres d’origine pour chaque élément. 
    
    - **Les messages individuels** - exporte les résultats de recherche sous forme de messages électroniques individuels, en utilisant le format .msg. Si vous sélectionnez cette option, les résultats de recherche de messagerie sont exportés vers un dossier dans le système de fichiers. Le chemin d’accès de dossier pour chaque message est la même que celle utilisée si vous avez exporté les résultats aux fichiers PST. 
    
      > [!IMPORTANT]
      > Pour déchiffrer des messages chiffrés RMS lorsqu’ils sont exportés, vous devez exporter les résultats de la recherche électronique sous forme de messages individuels. Messages chiffrés restent chiffrés si vous exportez les résultats de recherche dans un fichier PST. 
  
8. Cliquez sur la case à cocher **Activer la déduplication** pour exclure les messages en double. Cette option apparaît uniquement si les sources de contenu de la recherche inclut des boîtes aux lettres Exchange ou des dossiers publics. 
    
    Si vous sélectionnez cette option, qu’une seule copie d’un message doit être exportée même si plusieurs copies du même message sont trouvent dans les boîtes aux lettres qui ont été exclus. Rapport de résultats de l’exportation (Results.csv) contient une ligne pour chaque copie d’un message en double afin que vous pouvez identifier les boîtes aux lettres (ou les dossiers publics) qui contiennent une copie du message en double. Pour plus d’informations sur la déduplication et comment les doublons sont identifiés, voir [la déduplication dans les résultats de recherche de découverte électronique](de-duplication-in-ediscovery-search-results.md).
    
9. Cliquez sur la case à cocher **inclure les versions des documents SharePoint** pour exporter toutes les versions de documents SharePoint. Cette option apparaît uniquement si les sources de contenu de la recherche inclut les sites SharePoint ou OneDrive. 
    
10. Cliquez sur la case à cocher **exporter des fichiers dans un dossier compressé (zip)** pour exporter les résultats de recherche dans un dossier compressé. Cette option est disponible uniquement lorsque vous choisissez d’exporter les éléments de Exchange en tant que messages individuels et lorsque les résultats de recherche incluent des documents SharePoint ou OneDrive. Cette option est utilisée principalement pour contourner la limite de 260 caractères dans les noms de chemin d’accès de fichier Windows lorsque les éléments sont exportés. Voir les « noms d’éléments exportés » dans la section [plus d’informations](#more-information) . 
    
11. Cliquez sur **Démarrer l’exportation**.
    
    Les résultats de recherche sont préparés pour le téléchargement, ce qui signifie qu’ils sont en cours de téléchargement à l’emplacement de stockage Azure dans le nuage de Microsoft. Lorsque les résultats de recherche sont prêts à être téléchargés, le lien de **téléchargement exporté les résultats** s’affiche sous **Exporter les résultats à un ordinateur** dans le volet détails. 
  
## <a name="step-2-download-the-search-results"></a>Étape 2 : Télécharger les résultats de recherche

L’étape suivante consiste à télécharger les résultats de recherche à partir de l’emplacement de stockage Azure sur votre ordinateur local.
  
Comme expliqué précédemment, vous pouvez augmenter la vitesse de téléchargement en configurant un paramètre de Registre Windows sur l’ordinateur que vous utilisez pour exporter les résultats de recherche. Pour plus d’informations, voir [augmenter la vitesse de téléchargement lors de l’exportation des résultats de recherche de découverte électronique à partir d’Office 365](increase-download-speeds-when-exporting-ediscovery-results.md).
  
1. Dans le volet Détails de la recherche pour laquelle vous avez démarré l’exportation, sous **Exporter les résultats vers un ordinateur**, cliquez sur **Télécharger les résultats exportés**.
    
    La fenêtre **téléchargement exporté les résultats** s’affiche et contient les informations suivantes sur les résultats de recherche qui sera téléchargé sur votre ordinateur. 
    
    - Le nombre d’éléments à télécharger.
    
    - La taille totale estimée des éléments à télécharger.
    
    - Si les éléments indexés ou non indexés seront exportés. Les éléments non indexés sont des éléments qui ont un format reconnu, qui sont chiffrés ou n’ont pas été indexés pour d’autres raisons. Pour plus d’informations, consultez la rubrique [Unindexed items in Content Search](partially-indexed-items-in-content-search.md).
    
    - Si les versions des documents SharePoint seront téléchargés.
    
    - L’état de la préparation. Vous pouvez commencer à télécharger les résultats de recherche, même si la préparation des données n’est pas terminée.
    
2. Sous **Clé d’exportation**, cliquez sur **Copier dans le Presse-papiers**. Cette clé vous permet de télécharger les résultats de recherche à l’étape 5.
    
    > [!NOTE]
    > Étant donné que tout le monde peut installer et lancer l’outil d’exportation de découverte électronique, et utiliser cette clé pour télécharger les résultats de recherche, prenez toutes les précautions nécessaires pour protéger cette clé, comme vous le feriez avec les mots de passe ou d’autres informations de sécurité.  
  
3. Cliquez sur **Télécharger les résultats**.
    
4. Si vous êtes invité à installer **Microsoft Office 365 eDiscovery outil d’exportation**, cliquez sur **installer**.
    
5. Dans l’**outil d’exportation de découverte électronique**, collez la clé d’exportation que vous avez copiée à l’étape 2 dans la zone appropriée. 
    
6. Cliquez sur **Parcourir** pour spécifier l’emplacement de téléchargement du fichier des résultats de recherche. 
    
    > [!NOTE]
    > En raison de la quantité élevée de l’activité du disque (lectures et écritures), vous devez télécharger les résultats de la recherche sur un disque dur local ; ne pas les télécharger vers un lecteur réseau mappé ou un emplacement réseau. 
  
1. Cliquez sur **Démarrer** pour télécharger les résultats de recherche sur votre ordinateur. 
    
    L' **outil d’exportation de découverte électronique** affiche les informations sur le processus d’exportation, y compris une estimation du nombre (et taille) des autres éléments à télécharger. Une fois le processus d’exportation terminée, vous pouvez accéder les fichiers à l’emplacement où ils ont été téléchargés. 
    

  
## <a name="more-information"></a>Plus d'informations
<a name="moreinfo"> </a>

Voici le plus d’informations sur l’exportation de résultats de recherche.
  
[Exporter des limites](export-search-results.md#export-limits)
  
[Exporter des rapports](export-search-results.md#export-reports)
  
[Exportation d’éléments indexés partiellement](#exporting-partially-indexed-items)
  
[Exportation des messages ou des fichiers PST](export-search-results.md#Exporting-individual-messages-or-PST-files)
  
[Déchiffrement des messages chiffrés RMS](export-search-results.md#Decrypting-RMS-encrypted-messages)
  
[Noms de fichier des éléments exportés](export-search-results.md#Filenames-of-exported-items)
  
[Divers](export-search-results.md#miscellaneous)
  
 ### <a name="export-limits"></a>Exporter des limites
  
- Exportation des résultats de recherche à partir de la sécurité &amp; centre de conformité présente les limites suivantes :
    
  - Vous pouvez exporter un maximum de 2 To de données à partir d’une recherche de contenu unique. Si les résultats de recherche soient supérieures à 2 To, envisagez d’utiliser des plages de dates ou d’autres types de filtres pour diminuer la taille totale des résultats de recherche.
    
  - Votre organisation peut exporter un maximum de 2 To de données pendant une journée.
    
  - 10 exportations maximum peuvent être exécutées simultanément au sein de votre organisation.
    
  - Un utilisateur unique peut exécuter un maximum de trois exportations en même temps.
    
  - Exportation des rapports de recherche de contenu ne compte pas sur les limites d’exportation. 
    
- Comme indiqué plus haut, résultats de la recherche de boîtes aux lettres et les sites sont téléchargées vers l’emplacement de stockage Azure (comme décrit dans [étape 1 : préparation pour l’exportation des résultats de recherche](export-search-results.md#step1)) à un taux maximal de 2 Go par heure.
    
- La taille maximale d’un fichier PST qui peut être exporté est de 10 Go par défaut. Cela signifie que si les résultats de recherche de boîte aux lettres d’un utilisateur sont supérieures à 10 Go, les résultats de recherche pour la boîte aux lettres doit être exportées dans deux (ou plusieurs) des fichiers PST distincts. En outre, si vous choisissez d’exporter tous les résultats de recherche dans un seul fichier PST, le fichier PST sera spilt dans des fichiers PST supplémentaires si la taille totale des résultats de recherche est supérieure à 10 Go. Si vous souhaitez modifier cette taille par défaut, vous pouvez modifier le Registre Windows sur l’ordinateur que vous utilisez pour exporter les résultats de recherche. Voir [modification de la taille des fichiers PST lors de l’exportation des résultats de recherche eDiscovery](change-the-size-of-pst-files-when-exporting-results.md).
    
    En outre, les résultats de recherche à partir d’une boîte aux lettres spécifique ne sont pas être répartis entre plusieurs fichiers PST, sauf si le contenu à partir d’une seule boîte aux lettres est supérieure à 10 Go. Si vous décidez d’exporter les résultats de recherche dans un fichier PST fichier qui contient tous les messages dans un dossier unique et les résultats de recherche sont supérieures à 10 Go, les éléments sont toujours organisés dans l’ordre chronologique, afin qu’ils seront être spilt dans des fichiers PST supplémentaires en fonction de la d envoyé ATE.
     
 ### <a name="export-reports"></a>Exporter des rapports
  
- Lorsque vous exportez des résultats de la recherche, les rapports suivants sont inclus en plus des résultats de la recherche.
    
  - **Exporter la synthèse** Un document Excel contenant un résumé de l’exportation. Cela inclut des informations telles que le nombre de sources de contenu qui ont été exclus, la taille estimée et téléchargée des résultats de recherche et l’estimation et téléchargé le nombre d’éléments qui ont été exportés. 
    
  - **Manifeste** Un fichier manifeste (au format XML) qui contient des informations sur chaque élément inclus dans les résultats de recherche. 
    
  - **Résultats** Un document Excel qui contient des informations sur chaque élément qui peut être téléchargé comme un résultat de recherche. Pour le courrier électronique, le journal de résultat contient des informations sur chaque message, y compris : 
    
      - l’emplacement du message dans la boîte aux lettres source (notamment si le message est dans la boîte aux lettres principale ou d’archivage) ;
        
      - la date à laquelle le message a été envoyé ou reçu ;
        
      - l’objet du message ;
        
      - l’expéditeur et les destinataires du message.
        
      - Si le message est un message en double si vous avez activé l’option la déduplication lors de l’exportation des résultats de la recherche. Les messages en double aura une valeur dans la colonne **en double pour l’élément** qui identifie le message comme un doublon. La valeur dans la colonne **en double à élément** contient l’identité de l’élément du message qui a été exporté. Pour plus d’informations, voir [la déduplication dans les résultats de recherche de découverte électronique](de-duplication-in-ediscovery-search-results.md).
        
      Pour les documents à partir de SharePoint et OneDrive pour les sites de l’entreprise, le journal de résultat contient des informations sur tous les documents, y compris :
        
      - l’URL du document ;
        
      - l’URL de la collection de sites qui héberge le document ;
        
      - la date à laquelle le document a été modifié pour la dernière fois ;
        
      - le nom du document (qui se trouve dans la colonne Objet du journal des résultats).
    
  - **Éléments non indexés** Un document Excel qui contient des informations sur tous les éléments indexés partiellement seraient inclus dans les résultats de recherche. Si vous n’incluez pas les éléments indexés partiellement lorsque vous générez le rapport de résultats de recherche, ce rapport est toujours téléchargé, mais sera vide. 
    
  - **Erreurs et avertissements** Contient des erreurs et avertissements rencontrés au cours de l’exportation de fichiers. Consultez la colonne de détails de l’erreur pour plus d’informations spécifiques à chaque erreur individuelle ou d’avertissement. 
    
  - **Éléments ignorés** Lorsque vous exportez des résultats de recherche à partir de SharePoint et OneDrive pour les sites de l’entreprise, l’exportation inclut généralement un rapport d’éléments ignorés (SkippedItems.csv). Les éléments citées dans cet état sont généralement les éléments qui ne seront pas téléchargés, par exemple un dossier ou un document défini. Exportation ne pas ces types d’éléments est normal. Pour les autres éléments ignorés, la « Erreur Type » et le champ de détails de l’erreur dans le rapport éléments ignorés affichent la raison pour laquelle l’élément a été ignoré et n’a pas été téléchargement avec les résultats de recherche. 
    
  - **Journal de suivi** Contient des informations détaillées sur le processus d’exportation et peuvent aider à découvrir des problèmes lors de l’exportation. 
    
    > [!NOTE]
    > Vous pouvez uniquement exporter ces documents sans avoir à exporter les résultats de recherche. Consultez la rubrique [Exporter un rapport de recherche de contenu](export-a-content-search-report.md). 
  
 ### <a name="exporting-partially-indexed-items"></a>Exportation d’éléments indexés partiellement
  
- Si vous exportez des éléments de boîte aux lettres à partir d’une recherche de contenu qui retourne tous les éléments de boîte aux lettres dans les résultats de recherche (car aucun mot clé où inclus dans la requête de recherche), éléments indexés partiellement ne sera copiées dans le fichier qui contient les éléments non indexés. Il s’agit, car tous les éléments, y compris tous les éléments indexés partiellement, sont automatiquement inclus dans les résultats de recherche standard. Cela signifie que les éléments indexés partiellement doivent être incluses dans un fichier PST (ou sous forme de messages individuels) qui contient les autres éléments indexés.
    
    En outre, si vous exportez les éléments indexés et partiellement indexés ou si vous exportez uniquement les éléments indexés d’une recherche de contenu qui retourne tous les éléments, le même nombre d’éléments sera téléchargé. Cela se produit même si les résultats de la recherche estimée pour la recherche de contenu (affichées dans les statistiques de la recherche dans la sécurité &amp; centre de conformité) seront toujours inclure une estimation distincte pour le nombre d’éléments indexés partiellement. Par exemple, supposons que l’estimation pour une recherche qui inclut tous les éléments (aucun mot clé dans la requête de recherche) indique que les 1 000 éléments ont été détectés et que les éléments indexés partiellement 200 ont été détectés également. Dans ce cas, les 1 000 éléments incluent les éléments indexés partiellement étant donné que la recherche retourne tous les éléments. En d’autres termes, il existe des 1 000 nombre total d’éléments renvoyé par la recherche et pas les éléments de 1 200 (comme prévu). Si vous exportez les résultats de la recherche et choisissez Exporter indexés et partiellement indexé éléments (ou éléments indexés uniquement), puis 1 000 éléments seront téléchargés. Là encore, qui est comme éléments partiellement indexés sont inclus dans les résultats (indexés) régulières lorsque vous utilisez une requête de recherche vide pour renvoyer tous les éléments. Dans ce même exemple, si vous choisissez d’exporter les éléments indexés partiellement uniquement, puis uniquement les éléments non indexés 200 doit être téléchargés.
    
    Notez également que dans l’exemple précédent (lorsque vous exportez des éléments indexés et partiellement indexés ou exporter des éléments indexés uniquement), le rapport **Résumé d’exportation** inclus dans les résultats de recherche exporté serait éléments de liste 1 000 éléments estimée et 1 000 téléchargé éléments pour les mêmes raisons comme décrits précédemment. 
    
- Si vous exportez des résultats de la recherche a été une recherche dans les emplacements de contenu spécifiques ou tous les emplacements de contenu dans votre organisation, seuls les partiellement éléments à partir d’emplacements de contenu qui contiennent des éléments qui correspondent aux critères de recherche seront exportés. En d’autres termes, si aucun résultat de recherche n’est détectée dans une boîte aux lettres ou d’un site, puis les partiellement éléments indexés dans cette boîte aux lettres ou site ne sont pas être exporté. La raison en est que l’exportation d’éléments indexés partiellement à partir de nombreux emplacements dans l’organisation peut augmenter la probabilité d’erreurs d’exportation et augmenter le temps que nécessaire pour exporter et télécharger les résultats de recherche.
    
    Pour exporter les éléments indexés partiellement à partir de tous les emplacements de contenu pour une recherche, configurer la recherche pour retourner tous les éléments (en supprimant des mots clés à partir de la requête de recherche), puis l’exporter uniquement les éléments indexés partiellement lorsque vous exportez les résultats de recherche.
    
    ![Utilisez l’option d’exportation décisif pour exporter uniquement les éléments non indexés](media/5d7be338-a0e5-425f-8ba5-92769c24bf75.png)
  
- Lors de l’exportation des résultats de recherche à partir de SharePoint ou OneDrive pour les sites de l’entreprise, la possibilité d’exporter les éléments non indexés dépend également que vous sélectionnez l’option d’exportation et si un site qui a été recherché contient un élément indexé qui correspond aux critères de recherche. Par exemple, si vous recherchez spécifique SharePoint ou OneDrive pour les sites et aucun résultat de recherche n’est trouvé, aucun élément non indexées à partir de ces sites ne doit être exportée si vous choisissez la deuxième option export pour exporter les éléments indexés et non indexés. Si un élément indexé d’un site ne correspond pas aux critères de recherche, tous les éléments non indexées à partir de ce site doit être exportées lors de l’exportation d’éléments indexés et non indexés. L’illustration suivante décrit les options d’exportation en fonction ou non un site contienne un élément indexé qui correspond aux critères de recherche.
    
    ![Choisissez l’option d’exportation en fonction ou non un site contienne un élément indexé qui correspond aux critères de recherche](media/94f78786-c6bb-42fb-96b3-7ea3998bcd39.png)

    
    A - uniquement les éléments indexés qui correspond aux critères de recherche sont exportées. Aucun élément partiellement indexés n’est exportées.
    
    B - si aucun élément indexé d’un site n’aux critères de recherche, des éléments indexés partiellement à partir de ce même site ne sont pas exportés. Si des éléments indexés d’un site sont renvoyés dans les résultats de recherche, les éléments partiellement indexées à partir de ce site sont exportées. En d’autres termes, seuls les éléments partiellement indexées à partir de sites qui contiennent des éléments qui correspondent aux critères de recherche sont exportées.
    
    C - tous les éléments partiellement indexées à partir de tous les sites de la recherche sont exportés, quel que soit si un site contient des éléments qui correspondent aux critères de recherche.
    
    Si vous choisissez d’exporter les éléments indexés partiellement, des éléments de boîte aux lettres partiellement indexés sont exportées dans un fichier PST distinct quel que soit l’option que vous choisissez sous **Exchange exporter du contenu en tant que**.

- Si des éléments indexés partiellement sont renvoyés dans la recherche de résultats (étant donné que les autres propriétés d’un élément partiellement indexé correspond aux critères de recherche), puis ces partiellement indexés sont exportés avec les résultats de recherche ordinaire. Par conséquent, si vous choisissez d’exporter les éléments indexés et éléments indexés partiellement (en sélectionnant l’option d’exportation **sont chiffrées, de tous les éléments, y compris celles qui ont un format non reconnu, ou n’ont pas été indexés pour toute autre raison** ), les éléments indexés partiellement exportés avec la reslts régulière seront consignées dans le rapport Results.csv. Ils ne seront pas figurer dans le rapport items.csv non indexés.
    
 ### <a name="exporting-individual-messages-or-pst-files"></a>Exportation des messages ou des fichiers PST
  
- Si le nom de chemin d’accès de fichier d’un message dépasse la limite maximale de caractères pour Windows, le chemin d’accès est tronqué. Mais le nom de chemin d’accès au fichier d’origine est consignée dans le manifeste et ResultsLog.
    
- Comme expliqué précédemment, envoyez un e-mail recherche résultats sont exportés vers un dossier dans le système de fichiers. Le chemin d’accès de dossier pour chaque message répliquer le chemin d’accès du dossier de boîte aux lettres de l’utilisateur. Par exemple, pour une recherche nommée « ContosoCase101 » les messages dans la boîte de réception d’un utilisateur se trouvent dans le chemin d’accès du dossier `~ContosoCase101\\<date of export\Exchange\user@contoso.com (Primary)\Top of Information Store\Inbox`. 
    
- Si vous choisissez d’exporter des messages électroniques dans un fichier PST contenant tous les messages dans un dossier, un dossier **Éléments supprimés** et un dossier de **Dossiers de recherche** sont inclus dans la partie supérieure du dossier PST. Ces dossiers sera vides. 
  
 ### <a name="decrypting-rms-encrypted-messages"></a>Déchiffrement des messages chiffrés RMS
  
- Comme expliqué précédemment, pour déchiffrer des messages chiffrés RMS lorsque vous exportez, vous devez exporter les résultats de recherche sous forme de messages individuels. Si vous exportez des résultats de recherche vers un fichier PST, messages chiffrés RMS restent chiffrés.
    
- La fonctionnalité de déchiffrement RMS dans la recherche de contenu ne déchiffrer des messages chiffrés avec Office 365 Message Encryption (OME) lorsque vous exportez des résultats de la recherche. Toutefois, si un message chiffré avec OME est envoyé par un utilisateur dans votre organisation, la copie du message dans le dossier éléments envoyés de l’utilisateur n’est pas chiffrée et ne sera visible après avoir est exporté. Toutefois, si les messages chiffrés avec OME sont reçus par les utilisateurs de votre organisation, ils ne sont pas être déchiffrés une fois qu’ils sont exportées. Pour plus d’informations sur OME, voir [Office 365 Message Encryption](https://go.microsoft.com/fwlink/p/?linkid=844966).
    
- Les messages qui sont déchiffrées sont identifiés dans le rapport **ResultsLog** . Ce rapport contient une colonne nommée **Décoder le statut**et la valeur **décodée** dans cette colonne identifie les messages l’ont été déchiffré. 
    
- Actuellement, cette fonctionnalité de déchiffrement n’inclut pas le contenu chiffré à partir de SharePoint et OneDrive pour les sites. Seuls les messages électroniques chiffrés RMS sont déchiffrées lorsque vous exportez les.
    
- Si un message électronique chiffré RMS comporte une pièce jointe (comme un document ou un autre message électronique) qui est également chiffrée, est déchiffré uniquement le premier message.
    
- Vous ne pouvez pas prévisualiser un message électronique chiffré de RMS. Pour afficher un message chiffré, vous devez l’exporter.
    
- Si vous avez besoin empêcher une personne de déchiffrement de messages chiffrés RMS, vous devrez créer un groupe de rôles personnalisés (en copiant l’eDiscovery intégrée groupe de rôle de gestionnaire), puis supprimer le rôle de gestion de déchiffrement RMS à partir du groupe de rôles personnalisé. Puis ajoutez la personne que vous ne souhaitez pas déchiffrer des messages en tant que membre du groupe de rôles personnalisé.
  
 ### <a name="filenames-of-exported-items"></a>Noms de fichier des éléments exportés
  
- Il existe une limite de 260 caractères (imposée par le système d’exploitation) pour le nom de chemin d’accès complet des messages électroniques et des documents du site exportés vers votre ordinateur local. Le nom de chemin d’accès complet pour les éléments exportés inclut l’emplacement d’origine de l’élément et l’emplacement du dossier sur l’ordinateur local où les résultats de recherche sont téléchargés vers. Par exemple, si vous spécifiez pour télécharger les résultats de recherche `C:\Users\Admin\Desktop\SearchResults` dans l’outil d’exportation de découverte électronique, le chemin d’accès complet pour un élément de courrier électronique téléchargé serait `C:\Users\Admin\Desktop\SearchResults\ContentSearch1\03.15.2017-1242PM\Exchange\sarad@contoso.com (Primary)\Top of Information Store\Inbox\Insider trading investigation.msg`.
    
    Si la limite de 260 caractères est dépassée, le nom de chemin d’accès complet pour un élément sera tronqué.
    
  - Si le nom de chemin d’accès complet est plu de 260 caractères, le nom du fichier sera réduit pour obtenir sous la limite ; Notez que le nom de fichier tronqué (à l’exception de l’extension de fichier) ne sont pas être inférieure à 8 caractères.
    
  - Si le nom de chemin d’accès complet est trop long toujours après raccourcir le nom de fichier, l’élément est déplacé à partir de son emplacement actuel vers le dossier parent. Si le chemin d’accès est toujours trop long, puis le processus est répété : raccourcir le nom de fichier, et si nécessaire déplace à nouveau vers le dossier parent. Ce processus est répété jusqu'à ce que le chemin d’accès complet sous la limite de 260 caractères.
    
  - Si un nom de chemin d’accès complet tronqués existe déjà, un numéro de version est ajouté à la fin du nom de fichier ; par exemple, `statusmessage(2).msg`.
    
    Pour atténuer ce problème, prenez en compte le téléchargement des résultats de recherche vers un emplacement avec un nom de chemin d’accès court ; par exemple, le téléchargement de résultats de la recherche dans un dossier nommé `C:\Results` pouvait ajouter moins de caractères pour le nom de chemin d’accès des éléments exportés à les télécharger vers un dossier nommé `C:\Users\Admin\Desktop\Results`.
    
- Lorsque vous exportez des documents du site, il est également possible que le nom de fichier d’origine d’un document sera modifié. Dans ce cas spécifiquement pour les documents qui ont été supprimées à partir de SharePoint OneDrive pour le site d’entreprise qui est mis en attente. Après la suppression d’un document qui se trouve sur un site qui est en attente, document supprimé est déplacé automatiquement à la bibliothèque de conservation permanente pour le site (qui a été créé lorsque le site a été mis en attente). Lorsque le document supprimé est déplacé vers la bibliothèque de conservation permanente, un ID unique et généré de manière aléatoire est ajouté au nom de fichier du document d’origine. Par exemple, si le nom de fichier pour un document est `FY2017Budget.xlsx` et que ce document est ultérieurement supprimé déplacé vers la bibliothèque de blocage de conservation, le nom de fichier du document qui est déplacé vers la bibliothèque de conservation permanente est modifié comme `FY2017Budget_DEAF727D-0478-4A7F-87DE-5487F033C81A2000-07-05T10-37-55.xlsx`. Si un document dans la bibliothèque de conservation attente correspond à la requête d’une recherche de contenu et que vous exportez les résultats de recherche, le fichier exporté aura le nom de fichier modifié ; Dans cet exemple, le nom de fichier du document exporté serait `FY2017Budget_DEAF727D-0478-4A7F-87DE-5487F033C81A2000-07-05T10-37-55.xlsx`.
    
    En outre, lorsqu’un document situé sur un site qui est en attente est modifié (et le contrôle de version pour la bibliothèque de documents dans le site a été activé), une copie du fichier est automatiquement créée dans la bibliothèque de conservation permanente. Dans ce cas, un ID généré de façon aléatoire et unique est également ajouté au nom de fichier du document qui est copié dans la bibliothèque de conservation permanente.
    
    La raison pour laquelle les noms de fichier des documents qui sont déplacés ou copiés vers la bibliothèque de conservation permanente est afin d’éviter les conflits de noms de fichiers. Pour plus d’informations sur placer un blocage sur des sites et la bibliothèque de blocage de conservation, voir [vue d’ensemble de l’archive permanente dans SharePoint Server 2016](https://support.office.com/article/5e400d68-cd51-444a-8fe6-e4df1d20aa95).
    
 ### <a name="miscellaneous"></a>Divers
  
- Tous les résultats de recherche et les rapports d’exportation sont inclus dans un dossier qui a le même nom que la recherche de contenu. Les messages électroniques qui ont été exportés se trouvent dans un dossier nommé **Exchange**. Documents se trouvent dans un dossier nommé **SharePoint**. 
    
- Les métadonnées du système de fichiers pour les documents dans SharePoint et OneDrive pour les sites sont conservée lorsque les documents sont exportés vers votre ordinateur local. Qui signifie que les propriétés de document, telles que la création et la dernière modification de dates, ne sont pas modifiée lorsque les documents sont exportées.