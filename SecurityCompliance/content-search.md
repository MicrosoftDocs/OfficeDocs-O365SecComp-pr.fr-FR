---
title: Recherche de contenu dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/28/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 53390468-eec6-45cb-b6cd-7511f9c909e4
description: Utiliser la recherche de contenu de sécurité Office 365 &amp; centre de conformité pour rechercher du contenu dans les boîtes aux lettres, les sites SharePoint Online, les comptes OneDrive, Microsoft Teams, groupes d’Office 365 et Skype pour des Conversations. Vous pouvez utiliser des requêtes de recherche de mot clé et conditions pour affiner les résultats de recherche. Ensuite, vous pouvez afficher un aperçu et exporter les résultats de recherche. Recherche de contenu est également un outil efficace pour rechercher du contenu qui peut être lié à une demande d’objet de données PIBR.
ms.openlocfilehash: f0064ae08226b1b0e864b25bb845054184f1efa4
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528784"
---
# <a name="content-search-in-office-365"></a>Recherche de contenu dans Office 365

Vous pouvez utiliser l’outil de découverte électronique de recherche de contenu de sécurité Office 365 &amp; centre de conformité pour rechercher des éléments sur place tels que le courrier électronique, les documents et les conversations dans votre organisation Office 365 de messagerie instantanée. Utilisez cet outil pour rechercher des éléments dans ces services Office 365 :
  
- Dossiers publics et boîtes aux lettres Exchange Online
    
- Sites SharePoint Online et OneDrive pour les comptes d’entreprise
    
- Skype pour des conversations
    
- Microsoft Teams 
    
- Groupes Office 365
    
Une fois que vous exécutez une recherche de contenu, le nombre d’emplacements de contenu et un estimation du nombre de résultats de la recherche est affiché dans le profil de la recherche. Vous pouvez également rapidement afficher les statistiques, tels que les emplacements de contenu dont la plupart des éléments qui correspondent à la requête de recherche. Après avoir exécuté une recherche, vous pouvez afficher les résultats ou les exporter vers un ordinateur local.


## <a name="create-a-new-search"></a>Créer une nouvelle recherche

Pour accéder à la page de **recherche de contenu** pour exécuter des recherches et aperçus et exporter les résultats de recherche, un administrateur, responsable de la conformité ou un gestionnaire eDiscovery doit être un membre du groupe de rôles eDiscovery responsable de la sécurité &amp; centre de conformité. Pour plus d’informations, voir [attribuer des autorisations de sécurité Office 365 eDiscovery &amp; centre de conformité](assign-ediscovery-permissions.md).
  
1. Accédez à [https://protection.office.com](https://protection.office.com).
    
2. Connectez-vous à l’aide de votre adresse de messagerie Office 365 et le mot de passe. 
    
3. Dans la sécurité &amp; centre de conformité, cliquez sur **recherche &amp; enquête** \> **recherche de contenu**.
    
4. Dans la page de **recherche** , cliquez sur la flèche en regard de l’option ![icône Ajouter](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **nouvelle recherche**. 
    
    ![La nouvelle liste déroulante de recherche](media/76b25861-55c5-4f50-9d48-9e2be2d0d078.png)
  
    Vous pouvez choisir l’une des options suivantes :
    
  - **Recherche interactive** - cette option lance un Assistant qui vous guide à travers la création de la recherche. L’interface utilisateur pour sélectionner les emplacements de contenu et créer la requête de recherche sont les mêmes que l’option **nouvelle recherche** . 
    
  - **Nouvelle recherche** - cette option affiche une interface utilisateur mise à jour pour créer une nouvelle recherche. Il s’agit de l’option par défaut si vous cliquez sur **nouvelle recherche**.
    
  - **ID de liste Rechercher par** - cette option vous permet de rechercher des messages électroniques spécifiques et autres éléments de boîte aux lettres à l’aide d’une liste d’ID Exchange. Pour créer une recherche de liste d’ID (auparavant appelée une recherche ciblée), vous envoyer un fichier (CSV) de valeurs séparées par des virgules qui identifie les éléments de boîte aux lettres spécifique à rechercher. Pour plus d’informations, voir [préparer un fichier CSV pour une liste d’ID de recherche de contenu dans Office 365](csv-file-for-an-id-list-content-search.md).
    
    Le reste de la procédure décrite dans cette procédure suivent le flux de travail par défaut nouvelle recherche.
    
5. Dans la liste déroulante, cliquez sur **nouvelle recherche** . 
    
6. Sous la **requête de recherche**, spécifiez les éléments suivants.
    
    ![Spécifier des mots clés, les conditions et les emplacements dans lesquels rechercher](media/1e6de9dd-eac9-4e2a-819d-9740cf6c9106.png)
  
- **Mots clés pour rechercher** - Type d’une recherche dans la zone **mots clés** de requête. Vous pouvez spécifier des mots clés, message propriétés telles qu’envoyés et reçus de dates, ou des propriétés de document telles que les noms de fichiers ou la date de dernière modification un document. Vous pouvez utiliser des requêtes plus complexes qui utilisent un opérateur booléen, tels que **AND**, **OR**, **pas**et **NEAR**. Vous pouvez également rechercher des informations sensibles (comme les numéros de sécurité sociale) dans des documents ou de recherche pour les documents qui ont été partagées en externe. Si vous laissez la zone mot clé vide, tout le contenu situé dans les emplacements de contenu spécifiés sera inclus dans les résultats de recherche.
    
    Sinon, vous pouvez cliquer sur la case à cocher **Afficher la liste des mots clés** et le type d’un mot clé dans chaque ligne. Si vous procédez ainsi, les mots clés dans chaque ligne sont connectés par un opérateur logique ( **c:s**) des fonctionnalités similaires à l’opérateur **OR** dans la requête de recherche qui est créée. 
    
    Pourquoi utiliser la liste des mots clés ? Vous pouvez obtenir des statistiques indiquant le nombre d’éléments correspondent à chaque mot clé. Cela peut vous aider à identifier rapidement les mots clés qui sont le plus (et moins) efficaces. Vous pouvez également utiliser une phrase de mots clés (entourée parenthèses) dans une ligne. Pour plus d’informations sur les statistiques de recherche, voir [Afficher les statistiques de mots clés pour les résultats de recherche de contenu](view-keyword-statistics-for-content-search.md).
    
- **Conditions** - vous pouvez ajouter des conditions de recherche pour affiner la recherche et de renvoyer un jeu de résultats plus précis. Chaque condition ajoute une clause à la requête de recherche KQL qui est créée et exécutée lorsque vous démarrez la recherche. Une condition est logiquement connectée à la requête de mot clé (spécifiée dans la zone mots clés) par un opérateur logique ( **c : c**) des fonctionnalités similaires à l’opérateur **et** . Cela signifie que les éléments ont afin de répondre à la requête de mot clé et une ou plusieurs conditions à inclure dans les résultats. Il s’agit de comment conditions vous aider à limiter les résultats. Pour une liste et une description des conditions que vous pouvez utiliser dans une requête de recherche, voir la section « Conditions de recherche » dans les [requêtes de mot clé et les conditions de recherche pour la recherche de contenu](keyword-queries-and-search-conditions.md#search-conditions).
    
- **Emplacements** - hoisir les emplacements de contenu à rechercher.
    
  - **Tous les emplacements** - Utilisez cette option pour rechercher tous les emplacements de contenu dans votre organisation. Cela inclut le courrier électronique dans toutes les boîtes aux lettres Exchange (y compris toutes les boîtes aux lettres inactives, les boîtes aux lettres pour tous les groupes d’Office 365, les boîtes aux lettres pour toutes les Microsoft Teams), tous les Skype pour des conversations, tous les SharePoint et OneDrive pour les sites d’entreprise (y compris les sites pour tous les groupes d’Office 365 et Microsoft Teams) et les éléments de tous les dossiers publics Exchange.
    
  - **Emplacements spécifiques** - Utilisez cette option pour rechercher les emplacements de contenu spécifiques. Vous pouvez rechercher tous les emplacements de contenu d’un service Office 365 (par exemple recherche toutes les boîtes aux lettres Exchange ou rechercher tous les sites SharePoint) ou vous pouvez rechercher des emplacements spécifiques dans une ou plusieurs des services Office 365 sont affichés. 
    
    ![Interface utilisateur pour choisir les emplacements de contenu pour la recherche](media/9a09708b-f8a2-4382-8c4e-2c610ec33c72.png)
  
    Notez que vous pouvez également ajouter des groupes de distribution à la liste des boîtes aux lettres Exchange à rechercher. Pour les groupes de distribution, les boîtes aux lettres des membres du groupe sont recherchés. Notez que les groupes de distribution dynamique ne sont pas pris en charge.
    
    **Important :** Lorsque vous recherchez tous les emplacements de boîte aux lettres ou les boîtes aux lettres spécifiques, les données à partir de MyAnalytics et d’autres applications Office 365 qui a enregistré dans les boîtes aux lettres seront incluses lorsque vous exportez les résultats d’une recherche de contenu. Ces données ne pas être incluses dans les résultats de recherche estimés et il n’est pas disponible pour l’aperçu. Il sera inclus uniquement lorsque vous exportez et téléchargez les résultats de recherche ; voir [exportation de données à partir de MyAnalytics et d’autres applications Office 365](#exporting-data-from-myanalytics-and-other-office-365-applications) dans la section « Plus d’informations sur la recherche de contenu ». 
    
7. Une fois que vous avez configuré votre requête de recherche, cliquez sur **Enregistrer &amp; exécuter**.
    
8. Dans la page **Enregistrer la recherche** , tapez un nom pour la recherche et une description facultative qui permet d’identifier la recherche. Notez que le nom de la recherche doit être unique dans votre organisation. 
    
9. Cliquez sur **Enregistrer** pour lancer la recherche. 
    
    Une fois que vous enregistrez et exécuter la recherche, les résultats renvoyés par la recherche sont affichés dans le volet résultats. Selon la façon dont vous avez le paramètre preview configuré, les résultats de recherche sont affichage ou vous devez cliquer sur **Aperçu des résultats** pour les afficher. Voir la section suivante pour plus d’informations. 
    
Pour accéder à nouveau à cette recherche de contenu ou accéder aux autres critères de recherche de contenu répertoriés dans la page de **recherche de contenu** , sélectionnez la recherche, puis cliquez sur **Ouvrir**. 
  
Pour effacer les résultats ou créer une nouvelle recherche, cliquez sur ![icône Ajouter](media/O365-MDM-CreatePolicy-AddIcon.gif) **nouvelle recherche**. 

  
## <a name="preview-search-results"></a>Aperçu des résultats de la recherche

Il existe deux paramètres de configuration pour afficher un aperçu des résultats de la recherche. Une fois que vous exécutez une nouvelle une nouvelle recherche ou ouvrez une recherche existante, cliquez sur ** résultats individuels ** pour afficher les paramètres d’aperçu suivant : 
  
![Paramètres Aperçu des résultats de recherche](media/83519477-1c85-4442-8886-481f186fd758.png)
  
1. **Afficher un aperçu des résultats automatiquement** : ce paramètre affiche les résultats de recherche après avoir un exécuter une recherche.
    
2. **Afficher un aperçu des résultats manuellement** : ce paramètre affiche des espaces réservés dans le volet de résultats de recherche et le bouton **Aperçu des résultats** que vous devez cliquez ici pour afficher les résultats de recherche. Il s’agit du paramètre par défaut ; Il permet d’améliorer les performances de recherche en affichant pas automatiquement les résultats de recherche lorsque vous ouvrez une recherche existante. 
    
Il existe des limites liées au nombre d’éléments est disponible pour être affichés. Pour plus d’informations, voir [limites pour la recherche de sécurité Office 365 &amp; centre de conformité](limits-for-content-search.md). 
  
Pour obtenir la liste des types de fichiers pris en charge qui peuvent être affichés, voir [l’Aperçu des résultats de recherche](#previewing-search-results) dans la section « Plus d’informations sur la recherche de contenu ». Si un type de fichier n’est pas pris en charge pour aperçu ou pour télécharger une copie d’un document, vous pouvez cliquer sur **Télécharger le fichier d’origine** pour le télécharger sur votre ordinateur local. Pour les pages Web .aspx, l’URL de la page est inclus si vous n’avez ne peut-être pas les autorisations pour accéder à la page. 
  
Notez également que les éléments non indexés ne sont pas disponibles pour afficher un aperçu.
  
## <a name="view-information-and-statistics-about-a-search"></a>Afficher des informations et des statistiques sur une recherche

Après avoir créé et exécuter une recherche de contenu, vous pouvez afficher des statistiques sur les résultats de recherche estimés. Cela inclut un résumé des résultats de recherche, tels que le nombre d’emplacements de contenu avec les éléments qui correspondent à la requête de recherche et le nom des emplacements de contenu dont les éléments correspondants plus les statistiques des requêtes. Vous pouvez afficher des statistiques pour une ou plusieurs recherches de contenu. Cela vous permet pour comparer les résultats de plusieurs recherches rapidement et de prendre des décisions concernant l’efficacité de vos requêtes de recherche.
  
Vous pouvez également télécharger les statistiques de recherche et les statistiques de mots clés dans un fichier CSV. Cela vous permet d’utiliser les fonctionnalités de filtrage et de tri dans Excel pour comparer les résultats et établir des rapports pour vos résultats de recherche.
  
Pour afficher les statistiques de la recherche :
  
1. Dans la page de **recherche de contenu** dans la sécurité &amp; centre de conformité, cliquez sur **Ouvrir** , puis cliquez sur la recherche que vous souhaitez afficher les statistiques pour. 
    
2. À la volée page, cliquez sur **Ouvrir une requête**. 
    
3. Dans la liste déroulante **les résultats** , cliquez sur **profil de la recherche**.
    
4. Dans la liste déroulante **Type** , cliquez sur une des options suivantes selon les statistiques de recherche que vous souhaitez afficher. 
    
  - **Résumé** : affiche les statistiques pour chaque type de rechercher les emplacements de contenu. Le nombre d’emplacements de contenu qui contenait les éléments qui correspondent à la requête de recherche de ce contenu et le nombre et la taille des éléments de résultat de recherche. Il s’agit du paramètre par défaut.
    
  - **Requêtes** - affiche les statistiques relatives à la requête de recherche. Cela inclut le type de statistiques de la requête sont applicables à un emplacement de contenu, la partie de la requête de recherche les statistiques sont applicables pour (Notez que **principal** indique la requête de recherche), le nombre d’emplacements de contenu qui contiennent les éléments correspond à la requête de recherche et le nombre total et la taille et les éléments qui ont été détectés (à l’emplacement de contenu spécifié) qui correspondent à la requête de recherche. Notez que les statistiques relatives aux éléments non indexés (également appelés éléments indexés partiellement) sont également affichées. Toutefois, seuls les éléments indexés partiellement des boîtes aux lettres sont inclus dans les statistiques. Éléments partiellement indexées à partir de SharePoint et OneDrive ne sont pas inclus dans les statistiques.
    
  - **Emplacements supérieurs** - affiche les statistiques sur le nombre d’éléments qui correspondent à la requête de recherche dans chaque emplacement du contenu qui a été recherché. Les emplacements de haut 1 000 sont affichés.
    
Pour plus d’informations sur les statistiques de recherche, voir [Afficher les statistiques de mots clés pour les résultats de recherche de contenu](view-keyword-statistics-for-content-search.md).
  
  
## <a name="export-search-results"></a>Exporter les résultats de la recherche

Après qu’une recherche est exécutée correctement, vous pouvez exporter les résultats de recherche sur un ordinateur local. Lorsque vous exportez des résultats de la messagerie, ils peuvent être téléchargés sur votre ordinateur en tant que fichiers PST ou des messages individuels (fichiers .msg). Lorsque vous exportez le contenu à partir des sites SharePoint et OneDrive, les copies des documents Office natifs sont exportées. Il existe également des documents et des rapports qui sont inclus dans les résultats de recherche exportés. Vous pouvez également exporter le rapport de résultats de recherche et pas les éléments réels.
  
Pour exporter les résultats de la recherche :
  
1. Dans la page de **recherche de contenu** dans la sécurité &amp; centre de conformité, cliquez sur **Ouvrir** , puis cliquez sur la recherche que vous souhaitez exporter les résultats de recherche. 
    
2. À la volée page, cliquez sur ![icône de résultats de recherche d’exportation](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **plus**, puis cliquez sur **Exporter les résultats**. Notez que vous pouvez également exporter un rapport de résultats de recherche.
    
3. Complétez les sections sur la page volante **Exporter les résultats**. Veillez à utiliser la barre de défilement pour afficher toutes les options d’exportation. 
    
Pour obtenir des instructions plus détaillées et des conseils de dépannage, voir :
  
- [Exporter les résultats de recherche à partir de la sécurité de 365 Office &amp; centre de conformité](export-search-results.md)
    
- [Exporter un rapport de recherche de contenu](export-a-content-search-report.md)
    

  
## <a name="more-information-about-content-search"></a>Plus d’informations sur la recherche de contenu

Consultez les sections suivantes pour plus d’informations sur les recherches de contenu.
  
[Limites de la recherche de contenu](#content-search-limits)
  
[Création d’une requête de recherche](#building-a-search-query)
  
[Recherche des comptes OneDrive](#searching-onedrive-accounts)
  
[Recherche des équipes Microsoft et des groupes d’Office 365](#searching-microsoft-teams-and-office-365-groups)
  
[Recherche des boîtes aux lettres inactives](#searching-inactive-mailboxes)
  
[Afficher un aperçu des résultats de la recherche](#previewing-search-results)
  
[Éléments indexés partiellement](#partially-indexed-items)
  
[Exportation des données à partir de MyAnalytics et d’autres applications Office 365](#exporting-data-from-myanalytics-and-other-office-365-applications)
  
### <a name="content-search-limits"></a>Limites de la recherche de contenu

- Pour obtenir une description des limites qui sont appliqués à la fonctionnalité de recherche de contenu, voir [limites pour la recherche de sécurité Office 365 &amp; centre de conformité](limits-for-content-search.md).
    
- Microsoft collecte des informations sur les performances lors de la recherche de contenu exécuter à toutes les organisations Office 365. Alors que la complexité des requêtes de recherche permettre affecter les temps de recherche, le facteur décisif qui affecte la durée des recherches est le nombre de boîtes aux lettres recherché. Bien que Microsoft ne fournit pas d’un contrat de niveau de Service pour le temps de recherche, le tableau suivant répertorie les temps de recherche moyen pour une recherche de contenu en fonction du nombre de boîtes aux lettres inclus dans la recherche.
    
|**Nombre de boîtes aux lettres**|**Temps moyen de recherche**|
|:-----|:-----|
|100  <br/> |30 secondes  <br/> |
|1,000  <br/> |45 secondes  <br/> |
|10 000  <br/> |4 minutes  <br/> |
|25 000  <br/> |10 minutes  <br/> |
|50 000  <br/> |20 minutes  <br/> |
|100 000  <br/> |25 minutes  <br/> |
  
### <a name="building-a-search-query"></a>Création d’une requête de recherche

Pour plus d’informations sur la création d’une requête de recherche, à l’aide des opérateurs de recherche booléens et les conditions de recherche et de recherche pour les types d’informations sensibles et de contenu partagé avec des utilisateurs extérieurs à votre organisation, voir requêtes de mot clé [et conditions de recherche pour la recherche de contenu ](keyword-queries-and-search-conditions.md).
  
Conserver les éléments suivants à l’esprit lors de l’utilisation de la liste des mots clés pour créer une requête de recherche.
  
- Vous devez sélectionner la case à cocher **Afficher la liste des mots clés** , puis tapez chaque mot clé dans une ligne distincte pour créer une requête de recherche dans laquelle les mots clés (ou des expressions de mot clé) dans chaque ligne sont connectées par l’opérateur **OR** . Si vous venez collez une liste de mots clés dans la zone mot clé ou appuyez sur la touche **entrée** après avoir tapé un mot clé, ils ne sont pas connectés par l’opérateur **OR** . Voici un exemple incorrect et correct de l’ajout d’une liste de mots clés. 
    
    **Incorrect**
    
    ![La façon de mettre en forme une liste des mots clés (en-coller de la liste dans la zone mot clé) incorrecte](media/fb54e3df-232a-439a-b3d7-27a60ec76a4c.png)
  
    **Correct**
    
    ![Comment mettre en forme une liste des mots clés (en activant la case à cocher, puis collage liste)](media/5d511a7b-c1f9-499c-bffe-e075bfc9adec.png)
  
- Vous pouvez également préparer une liste des mots clés ou expressions de mots clés dans un fichier Excel ou un fichier texte brut, puis copiez et collez dans votre liste à la liste des mots clés. Pour ce faire, vous devez sélectionner la case à cocher **Afficher la liste des mots clés** . Ensuite, cliquez sur la première ligne dans la liste des mots clés et collez votre liste. Chaque ligne du fichier Excel ou du texte est collé pour séparer les lignes dans la liste des mots clés. 
    
- Après avoir créé une requête à l’aide de la liste des mots clés, il est conseillé de vérifier la syntaxe de requête de recherche pour effectuer la requête de recherche est ce que vous souhaitiez. Dans la requête de recherche qui s’affiche sous la **requête** dans le volet détails, les mots clés sont séparés par le texte **(c:s)**. cela indique que les mots clés sont connectés par un opérateur logique des fonctionnalités similaires à l’opérateur **OR** . De même, si votre requête de recherche comprend les conditions, les mots clés et les conditions sont séparées par le texte **(c : c)**. cela indique que les mots clés sont connectés à un opérateur logique des fonctionnalités similaires **et** les conditions opérateur. Voici un exemple de la requête de recherche (affichée dans le volet détails) lors de l’utilisation de la liste des mots clés et une condition de résultats. 
    
    ![Exemple de la requête qui est créée lors de l’utilisation de la liste des mots clés et une condition](media/b463750c-57fa-4602-9fed-0d5a420db3ad.png)
  
- Lorsque vous exécutez une recherche de contenu, Office 365 vérifie automatiquement votre requête de recherche pour les caractères non pris en charge et des opérateurs booléens qui ne peuvent pas être mise en majuscule. Caractères non pris en charge sont souvent masqués et généralement de provoquer une erreur de recherche ou renvoyer des résultats inattendus. Pour plus d’informations sur les caractères non pris en charge qui sont en cours, voir [vérifier votre requête de recherche de contenu pour les erreurs](check-your-content-search-query-for-errors.md).
    
- Si vous disposez d’une requête de recherche qui contient des mots clés pour les caractères non anglais (tels que des caractères chinois), vous pouvez cliquer sur **requête langue-pays/région**![icône de langue-pays/région de requête de recherche de contenu](media/8d4b60c8-e1f1-40f9-88ae-ee2a7eca0886.png) et sélectionnez un valeur de code de culture de la langue-pays pour la recherche. Notez que la langue/région par défaut est neutre. Comment savoir si vous devez modifier le paramètre de langue pour une recherche de contenu ? Si vous êtes certains emplacements de contenu contiennent des caractères non anglais que vous recherchez, mais la recherche ne renvoie aucun résultat, le paramètre de langue peut être la cause. 
  
### <a name="searching-onedrive-accounts"></a>Recherche des comptes OneDrive

- Pour collecter une liste d’URL pour les sites de OneDrive dans votre organisation, voir [créer une liste de tous les emplacements de OneDrive dans votre organisation](https://support.office.com/article/8e200cb2-c768-49cb-88ec-53493e8ad80a). Ce script dans cet article crée un fichier texte qui contient une liste de tous les sites OneDrive. Pour exécuter ce script, vous devrez installer et utiliser SharePoint Online Management Shell. Veillez à ajouter l’URL de domaine du site Mon site dans votre organisation à chaque site OneDrive que vous souhaitez rechercher. Il s’agit du domaine qui contient votre OneDrive ; par exemple, `https://contoso-my.sharepoint.com`. Voici un exemple d’URL pour le site de OneDrive d’un utilisateur : `https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft.com`.
    
    Dans ce cas rare que le nom d’une personne utilisateur principal (UPN) est modifié, l’URL de leur emplacement OneDrive système aussi être modifié pour incorporer le nouvel UPN. Dans ce cas, vous devrez modifier une recherche de contenu en ajoutant une nouvelle URL l’utilisateur de OneDrive et de supprimer l’ancien.
  
### <a name="searching-microsoft-teams-and-office-365-groups"></a>Recherche des équipes Microsoft et des groupes d’Office 365

Vous pouvez rechercher la boîte aux lettres qui est associé à un groupe d’Office 365 ou un Team Microsoft. Microsoft Teams étant basées sur Office 365 groupes, recherche les est très similaire. Dans les deux cas, seulement la boîte aux lettres d’équipe ou de groupe est recherché ; les membres du groupe ou de l’équipe de boîtes aux lettres ne sont pas recherchés. Pour rechercher les, vous devez les ajouter explicitement à la recherche.
  
Gardez les éléments suivants à l’esprit lors de la recherche du contenu dans Microsoft Teams et groupes d’Office 365.
  
- Pour rechercher du contenu situé dans Microsoft Teams et groupes d’Office 365, vous devez spécifier la boîte aux lettres et le site SharePoint qui sont associés à une équipe ou un groupe.
    
- Exécutez l’applet de commande **Get-UnifiedGroup** dans Exchange Online pour afficher les propriétés pour un Team Microsoft ou un groupe d’Office 365. Il s’agit d’un excellent moyen d’obtenir l’URL du site qui est associé à une équipe ou un groupe. Par exemple, la commande suivante affiche les propriétés sélectionnées d’un groupe d’Office 365 nommé équipe de direction Senior : 
    
  ```
  Get-UnifiedGroup "Senior Leadership Team" | FL DisplayName,Alias,PrimarySmtpAddress,SharePointSiteUrl
  DisplayName            : Senior Leadership Team
  Alias                  : seniorleadershipteam
  PrimarySmtpAddress     : seniorleadershipteam@contoso.onmicrosoft.com
  SharePointSiteUrl      : https://contoso.sharepoint.com/sites/seniorleadershipteam
  
  ```

    > [!NOTE]
    > Pour exécuter l’applet de commande **Get-UnifiedGroup** , vous devez être affecté le rôle destinataires en affichage seul dans Exchange Online ou être membre d’un groupe de rôles qui a affecté le rôle destinataires en affichage seul. 
  
- Lorsque la recherche de boîte aux lettres d’un utilisateur, Microsoft Team ni groupe Office 365 dont l’utilisateur est membre ne sont pas recherché. De même, lorsque vous recherchez un Team Microsoft ou un groupe de 365 Office uniquement le boîte aux lettres de groupe et le site du groupe que vous spécifiez est recherché ; les boîtes aux lettres et OneDrive for Business comptes des membres du groupe ne sont pas recherchés sauf si vous les ajoutez à la recherche.
    
- Pour obtenir une liste des membres d’un Team Microsoft ou d’un groupe d’Office 365, vous pouvez afficher les propriétés de le **accueil \> groupes** page dans le centre d’administration d’Office 365. Vous pouvez également exécuter la commande suivante dans Exchange Online PowerShell : 
    
  ```
  Get-UnifiedGroupLinks <group or team name> -LinkType Members | FL DisplayName,PrimarySmtpAddress 
  ```

    > [!NOTE]
    > Pour exécuter l’applet de commande **Get-UnifiedGroupLinks** , vous devez être affecté le rôle destinataires en affichage seul dans Exchange Online ou être membre d’un groupe de rôles qui a affecté le rôle destinataires en affichage seul. 
  
- Conversations qui font partie d’un canal Teams Microsoft sont stockées dans la boîte aux lettres qui est associé à la Team Microsoft. De même, les fichiers qui partagent des membres de l’équipe dans un canal sont stockés sur le site SharePoint de l’équipe. Par conséquent, vous devez ajouter la boîte aux lettres Microsoft Team et un site SharePoint comme emplacement de contenu pour rechercher les conversations et les fichiers dans un canal.
    
- Vous pouvez également les conversations qui font partie de la liste de conversation dans Microsoft Teams sont stockées dans la boîte aux lettres Exchange Online des utilisateurs qui participent à la conversation. Et fichiers utilisateur partage conversation sont stockés dans le compte professionnel de l’utilisateur qui partage le fichier OneDrive. Par conséquent, vous devez ajouter les boîtes aux lettres individuelles et OneDrive pour les comptes d’entreprise en tant qu’emplacements de contenu pour rechercher les conversations et les fichiers dans la liste de conversation.
    
    > [!NOTE]
    > Les utilisateurs de participer à des conversations qui font partie de la liste de conversation dans Microsoft Teams doivent avoir une Exchange Online (en nuage) boîte aux lettres dans l’ordre vous permet de rechercher des conversations. C’est parce que les conversations qui font partie de la liste de conversation sont stockées dans les boîtes aux lettres en nuage de participants à la conversation. Si un participant de conversation ne possède une boîte aux lettres Exchange Online, vous ne pourrez pas rechercher des conversations. Par exemple, dans un déploiement Exchange hybride, les utilisateurs avec une boîte aux lettres locale peuvent être en mesure de participer à des conversations qui font partie de la liste de conversation dans Microsoft Teams. Toutefois dans ce cas, le contenu de ces conversation ne sont pas utilisables dans une requête, car les utilisateurs ne possèdent des boîtes aux lettres en nuage. 
  
- Chaque canal Microsoft Team ou de l’équipe contient un Wiki de prise de notes et de collaboration. Le contenu Wiki est automatiquement enregistré dans un fichier au format .mht. Ce fichier est stocké dans la bibliothèque de documents équipes Wiki données sur le site SharePoint de l’équipe. Vous pouvez utiliser l’outil de recherche de contenu pour rechercher le Wiki en spécifiant des sites SharePoint de l’équipe en tant que l’emplacement de contenu de recherche. 
    
    > [!NOTE]
    > La fonction de recherche le Wiki pour un canal ou Microsoft Team (lors de la recherche de sites SharePoint de l’équipe) a été publiée le 22 juin 2017. Wiki pages qui ont été enregistrées ou mis à jour sur date ou après qui sont disponibles à rechercher. Pages Wiki dernier enregistrement ou mis à jour avant cette date ne sont pas disponibles pour la recherche. 
 
- Informations de synthèse pour les réunions et les appels dans un canal Teams Microsoft sont également stockés dans les boîtes aux lettres d’utilisateurs qui se sont connectés à la réunion ou un appel. Cela signifie que vous pouvez utiliser la recherche de contenu à rechercher ces enregistrements de synthèse. Informations de synthèse incluent : 
  - Date et heure de début, heure de fin et la durée d’une réunion ou un appel

  - La date et l’heure de chaque participant rejoint ou gauche de la réunion ou un appel

  - Appels envoyés vers la messagerie vocale

  - Appels manqués ou sans réponse

  - Transferts d’appel, qui sont représentés sous forme de deux appels séparés

  Notez que peut prendre jusqu'à 8 heures pour les enregistrements de synthèse réunion et d’appel soit disponible à rechercher.

  Dans les résultats de recherche, des résumés de réunion sont identifiés comme **réunion** dans le **champ Type**; appel résumés sont identifiés comme **des appels**. En outre, les conversations qui font partie d’une conversation de canal et 1xN équipes sont identifiées comme **messagerie instantanée** dans le champ **Type** .
  
  ![Réunions d’équipes, les appels et conversations 1xN sont identifiées dans le champ Type](media/O365-ContentSearch-Teams-MessageKind.png)

- Vous pouvez utiliser la propriété email de **type** ou la condition de recherche de **type de Message** pour rechercher le contenu de Microsoft Teams spécifiquement. 
  - Pour utiliser la propriété **type** dans le cadre de la requête de recherche de mot clé, dans la zone **mots clés** d’une requête de recherche, tapez `kind:microsoftteams`.

    ![Utiliser le type : microsoftteams dans la zone mots clés](media/O365-ContentSearch-Teams-Keywords.png)
  
  - Pour utiliser une condition de recherche, ajoutez la condition de **type de Message** et utilisez la valeur `microsoftteams`. 

    ![Utiliser la condition de type de Message avec la valeur microsoftteams.](media/O365-ContentSearch-Teams-MessageKindCondition.png)

Notez que les conditions sont logiquement connectées à la requête de mot clé par l’opérateur **AND** . Par conséquent, un élément doit correspondre à la requête de mot clé et la condition de recherche à renvoyer dans les résultats de recherche. Pour plus d’informations, voir la section « Instructions d’utilisation des conditions » dans [conditions de recherche pour la recherche de contenu et les requêtes de mot clé.](keyword-queries-and-search-conditions.md#guidelines-for-using-conditions)

  
### <a name="searching-inactive-mailboxes"></a>Recherche des boîtes aux lettres inactives

Vous pouvez rechercher les boîtes aux lettres inactives dans une recherche de contenu. Pour obtenir une liste des boîtes aux lettres inactives dans votre organisation, exécutez la commande `Get-Mailbox -InactiveMailboxOnly` dans Exchange Online PowerShell. Sinon, vous pouvez passer à la **gouvernance des données** \> **rétention** de sécurité &amp; centre de conformité, puis cliquez sur **plus de**![ellipses barre de Navigation](media/9723029d-e5cd-4740-b5b1-2806e4f28208.gif) \> **boîtes aux lettres inactives**.
  
Voici quelques points à prendre en compte lors de la recherche de boîtes aux lettres inactives.
  
- Si une recherche de contenu inclut une boîte aux lettres utilisateur et que cette boîte aux lettres est ensuite effectuée inactive, la recherche de contenu continuera à rechercher la boîte aux lettres inactive lorsque vous exécutez de nouveau la recherche dès que celui-ci est inactif.
    
- Dans certains cas, un utilisateur peut avoir une boîte aux lettres active et une boîte aux lettres inactive qui ont la même adresse SMTP. Dans ce cas, recherche portera uniquement la boîte aux lettres spécifique que vous sélectionnez un emplacement pour une recherche de contenu. En d’autres termes, si vous ajoutez des boîtes aux lettres d’un utilisateur à une recherche, vous ne pouvez pas supposer que les deux actives et inactives boîtes aux lettres portera ; recherche portera uniquement à la boîte aux lettres que vous ajoutez explicitement à la recherche.
    
- Il est vivement recommandé de ne pas avoir une boîte aux lettres active et la boîte aux lettres inactive avec la même adresse SMTP. Si vous avez besoin de réutiliser l’adresse SMTP qui est actuellement attribué à une boîte aux lettres inactive, nous vous recommandons de récupérer la boîte aux lettres inactive ou restaurer le contenu d’une boîte aux lettres inactive dans une boîte aux lettres active (ou l’archivage d’une boîte aux lettres active) et supprimez le boîte aux lettres inactive. Pour plus d’informations, consultez les rubriques suivantes :
    
  - [Récupérer une boîte aux lettres inactive dans Office 365](recover-an-inactive-mailbox.md)
    
  - [Restaurer une boîte aux lettres inactive dans Office 365](restore-an-inactive-mailbox.md)
    
  - [Supprimer une boîte aux lettres inactive dans Office 365](delete-an-inactive-mailbox.md)

  
### <a name="previewing-search-results"></a>Afficher un aperçu des résultats de la recherche

Vous pouvez afficher un aperçu des types de fichiers pris en charge dans le volet de visualisation. Si un type de fichier n’est pas pris en charge, vous devrez télécharger un exemplaire du fichier sur votre ordinateur local pour l’afficher. Types de fichiers suivants sont pris en charge et peuvent être affichés dans le volet de résultats de recherche.
  
- .txt, .html, .mhtml
    
- .eml
    
- .doc, .docx, .docm
    
- .pptm, .pptx
    
- .pdf
    
En outre, les types de conteneur de fichier suivants sont pris en charge. Vous pouvez afficher la liste des fichiers dans le conteneur dans le volet de visualisation.
  
- .zip
    
- .gzip
    
### <a name="partially-indexed-items"></a>Éléments indexés partiellement

- Comme expliqués précédemment, partiellement indexés des éléments de boîtes aux lettres sont inclus dans les résultats de recherche estimés ; éléments partiellement indexées à partir de SharePoint et OneDrive ne figurent pas dans les résultats de recherche estimés. 
    
- Si un partiellement élément correspond à la recherche de requête (étant donné que les autres propriétés de message ou un document aux critères de recherche), il ne sont pas inclus dans l’estimation du nombre d’éléments non indexés. Si un partiellement soit exclu par les critères de recherche, il ne sont pas également être inclus dans l’estimation du nombre d’éléments indexés partiellement. Pour plus d’informations, voir [partiellement indexé des éléments de la recherche de contenu dans Office 365](partially-indexed-items-in-content-search.md).
    
### <a name="exporting-data-from-myanalytics-and-other-office-365-applications"></a>Exportation des données à partir de MyAnalytics et d’autres applications Office 365

- À partir de MyAnalytics (par exemple, des informations sur comment les utilisateurs passent leur temps, basées sur les données de messagerie et calendrier dans leur boîte aux lettres) et les données à partir d’autres applications Office 365 est un enregistré à un emplacement masqué (dans une sous-arborescence non-IPM) dans boîte aux lettres en nuage sa. Après avoir exécuté une recherche de contenu, ces données n’est pas incluses dans les résultats de recherche estimés, les statistiques des requêtes, et il n’est pas disponible pour l’aperçu. Toutefois ces données seront exportées lorsque vous exportez les résultats d’une recherche.
    
- Les données MyAnalytics et les données à partir d’autres applications Office 365 est exporté vers un dossier nommé « Autres données Office 365 ». Ce dossier contient les sous-dossiers de chaque utilisateur.
  