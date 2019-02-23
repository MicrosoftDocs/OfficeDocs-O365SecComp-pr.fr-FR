---
title: Exécuter une recherche de contenu dans le centre de &amp; sécurité conformité Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/26/2018
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.ComplianceSearch
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 61852fd9-fe8a-4880-a339-cb19ed3bff4a
description: 'Utilisez la recherche de contenu dans le centre &amp; de conformité de sécurité Office 365 pour rechercher des boîtes aux lettres, des sites SharePoint Online et des emplacements OneDrive entreprise. '
ms.openlocfilehash: 82e8d2338fe003f2c37cd99994d8f71db2716da8
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219284"
---
# <a name="run-a-content-search-in-the-office-365-security-amp-compliance-center"></a>Exécuter une recherche de contenu dans le centre de &amp; sécurité conformité Office 365

Vous pouvez utiliser l'outil eDiscovery de recherche de contenu dans le centre &amp; de sécurité conformité Office 365 pour rechercher des éléments tels que des courriers électroniques, des documents et des conversations de messagerie instantanée dans votre organisation Office 365. Utilisez cet outil pour rechercher des éléments dans ces services Office 365:
  
- Boîtes aux lettres et dossiers publics Exchange Online
    
- Sites SharePoint Online et OneDrive entreprise
    
- Conversations Skype entreprise
    
- Microsoft Teams 
    
- Groupes Office 365
    
La recherche de contenu est un nouvel outil de recherche de découverte électronique avec de nouvelles fonctionnalités améliorées de mise à l'échelle et de performances. Utiliser la recherche de contenu pour exécuter des recherches eDiscovery très volumineuses. Vous pouvez rechercher toutes les boîtes aux lettres, tous les dossiers publics Exchange, ainsi que tous les sites SharePoint Online et OneDrive entreprise dans une recherche de contenu unique. Il n'existe aucune limite quant au nombre d'emplacements de contenu que vous pouvez rechercher. Il n'existe aucune limite quant au nombre de recherches pouvant être exécutées en même temps. Une fois que vous avez exécuté une recherche de contenu, le nombre d'emplacements de contenu et un nombre estimé de résultats de recherche sont affichés dans le volet d'informations sur la page **recherche de contenu** . Après avoir exécuté une recherche, vous pouvez afficher un aperçu des résultats, obtenir des statistiques sur les mots clés pour une ou plusieurs recherches, modifier en bloc les recherches de contenu et exporter les résultats vers un ordinateur local. 
  
 **Contenu**
  
[Créer une recherche](run-a-content-search-in-the-security-and-compliance-center.md#create)
  
[Exporter les résultats de la recherche](run-a-content-search-in-the-security-and-compliance-center.md#export)
  
[Aperçu des résultats de la recherche](run-a-content-search-in-the-security-and-compliance-center.md#preview)
  
[Mettre à jour des résultats de recherche](run-a-content-search-in-the-security-and-compliance-center.md#restart)
  
[Modifier une recherche](run-a-content-search-in-the-security-and-compliance-center.md#edit)
  
[Réessayer une recherche](run-a-content-search-in-the-security-and-compliance-center.md#retry)
  

  
## <a name="before-you-begin"></a>Avant de commencer

- Pour obtenir des informations et des instructions sur la création de requêtes de recherche et l'utilisation d'opérateurs de recherche booléens, consultez la rubrique [requêtes de mots clés et conditions de recherche pour la recherche de contenu](keyword-queries-and-search-conditions.md) Cet article contient également des informations sur la recherche de types d'informations sensibles et la recherche de contenu partagé avec des personnes à l'intérieur et à l'extérieur de votre organisation.
    
- Pour accéder à la page de **recherche de contenu** afin d'effectuer des recherches et d'afficher un aperçu et d'exporter les résultats de la recherche, un administrateur, un responsable de la mise en conformité ou un &amp; gestionnaire eDiscovery doit être membre du groupe de rôles gestionnaire eDiscovery dans la conformité de la sécurité. Interactif. Vous n'êtes pas obligé d'attribuer des autorisations de recherche supplémentaires dans Exchange Online, SharePoint Online ou pour les sites OneDrive entreprise. Pour plus d'informations, consultez [la rubrique attribution d'autorisations eDiscovery dans &amp; le centre de sécurité conformité Office 365](assign-ediscovery-permissions.md).
    
- Des limites sont appliquées à la recherche de contenu pour maintenir l'intégrité et la qualité des services fournis aux organisations Office 365. Dans la plupart des cas, vous ne pouvez pas modifier ces limites, mais vous devez en tenir compte pour pouvoir prendre ces limites en considération lors de la planification, de l'exécution et du dépannage des recherches. Pour plus d'informations, consultez [la rubrique Limits for Search in &amp; the Office 365 Security Compliance Center](limits-for-content-search.md).
    
- Consultez la section relative aux durées de recherche estimées en fonction du nombre de boîtes aux lettres recherchées dans une recherche de contenu unique. 
    
- Comme indiqué précédemment, vous pouvez utiliser la recherche de contenu pour rechercher du contenu dans les groupes Office 365 et Microsoft Teams. Cela signifie que vous pouvez rechercher la boîte aux lettres de groupe, le calendrier partagé et les sites SharePoint associés à un groupe Office 365 et une équipe Microsoft. En outre, vous pouvez effectuer des recherches dans les conversations de canal dans une équipe Microsoft. Pour plus d'informations sur les groupes Office 365 et Microsoft Teams, voir:
    
  - [En savoir plus sur les groupes Office 365](https://support.office.com/article/b565caa1-5c40-40ef-9915-60fdb2d97fa2)
    
  - [Aide de Microsoft teams](https://support.office.com/article/23156c0c-2c6e-49dd-8b7b-7c564b76508c)
    
    Consultez la section pour obtenir des conseils sur la recherche de contenu dans les groupes Office 365 et Microsoft Teams. 
    
[Return to top](run-a-content-search-in-the-security-and-compliance-center.md#top)
  
## <a name="create-a-search"></a>Créer une recherche
<a name="create"> </a>

1. Accédez à la page [https://protection.office.com](https://protection.office.com).
    
2. Connectez-vous à Office 365 à l'aide de votre compte scolaire ou professionnel.
    
3. Dans le volet gauche du Centre de sécurité et de conformité, cliquez sur **Recherches &amp; enquêtes** \> **Recherche de contenu**.
    
4. Cliquez sur **Nouveau**![Icône Ajouter](media/O365-MDM-CreatePolicy-AddIcon.gif).
    
5. Sur la page **Nouvelle recherche**, entrez un nom pour la recherche de contenu. Ce nom doit être unique dans votre organisation. 
    
6. Choisissez les emplacements de contenu sur lesquels vous souhaitez effectuer la recherche. Vous pouvez rechercher des boîtes aux lettres, des sites et des dossiers publics dans la même recherche.
    
    ![Choisir les emplacements de contenu vers lesquels vous souhaitez effectuer la recherche](media/da32e3f9-6cd6-4a26-8217-e97a5a7071e4.png)
  
1. **Rechercher partout** Sélectionnez cette option pour rechercher tous les emplacements de contenu de votre organisation. Lorsque vous sélectionnez cette option, vous pouvez choisir d'effectuer une recherche dans toutes les boîtes aux lettres (y compris les boîtes aux lettres inactives et les boîtes aux lettres de tous les groupes Office 365 et Microsoft Teams), tous les sites SharePoint et OneDrive entreprise (qui incluent les sites de tous les groupes Office 365 et Microsoft Teams) et tous les dossiers publics.
    
    ![Cliquez sur l'option Rechercher partout pour rechercher tous les emplacements de contenu](media/86f132f1-0a2a-4048-900c-9f219d909ef2.png)
  
2. **Sélection de l'emplacement personnalisé** Sélectionnez cette option pour sélectionner les boîtes aux lettres et les sites dans lesquels vous souhaitez effectuer une recherche. Si vous choisissez cette option, vous disposez de suffisamment de souplesse pour rechercher tous les emplacements de contenu d'un service spécifique (par exemple, la recherche dans toutes les boîtes aux lettres Exchange) ou vous pouvez rechercher des emplacements de contenu spécifiques pour un service Office 365.
    
    Gardez les points suivants à l'esprit lorsque vous ajoutez des emplacements de contenu à Rechercher:
    
    **Boîtes aux lettres**
    
  - Lorsque vous cliquez sur **Ajouter**![une](media/ITPro-EAC-AddIcon.gif) icône Ajouter pour spécifier les boîtes aux lettres à rechercher, le sélecteur de boîtes aux lettres affiché est vide. Il s'agit d'une conception qui améliore les performances. Pour ajouter des destinataires à cette liste, tapez un nom (un minimum de 3 caractères) dans la zone de ****![recherche, puis](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif)cliquez sur icône de recherche de recherche.
    
  - Vous pouvez ajouter des boîtes aux lettres et des groupes de distribution inactifs à la liste des boîtes aux lettres à rechercher. Pour les groupes de distribution, les boîtes aux lettres des membres du groupe sont recherchées. Notez que les groupes de distribution dynamique ne sont pas pris en charge.
    
  - Pour obtenir la liste des boîtes aux lettres inactives dans votre organisation, exécutez la `Get-Mailbox -InactiveMailboxOnly` commande dans Exchange Online PowerShell. Vous pouvez également accéder à la rétention de **gouvernance** \> **** des données &amp; dans le centre de sécurité conformité, puis cliquer sur **autres**![ellipses](media/9723029d-e5cd-4740-b5b1-2806e4f28208.gif) \> de barre de navigation pour les **boîtes aux lettres**inactives.
    
  - Vous pouvez également ajouter la boîte aux lettres associée à un groupe Office 365 ou une équipe Microsoft. Dans ce cas, seule la boîte aux lettres de groupe ou d'équipe est recherchée; les boîtes aux lettres du groupe ou des membres de l'équipe ne sont pas recherchées. Pour les Rechercher, vous devez les ajouter spécifiquement à la recherche.
    
  - Si vous ne souhaitez pas inclure de boîtes aux lettres dans la recherche, sélectionnez **choisir des boîtes aux lettres spécifiques à rechercher**, mais n'ajoutez pas de boîte aux lettres à la liste.
    
    **Sites**
    
  - Cliquez sur **Ajouter**![une](media/ITPro-EAC-AddIcon.gif) icône pour ajouter des sites à la recherche. Tapez l'URL de chaque site sur lequel vous souhaitez effectuer une recherche. L'outil de recherche de contenu valide l'URL, puis l'ajoute à la liste des sites dans lesquels effectuer la recherche. 
    
  - Vous pouvez ajouter le SharePoint associé à un groupe Office 365 ou une équipe Microsoft. Consultez la section pour obtenir des instructions sur la manière de trouver l'URL d'un groupe ou d'une équipe. 
    
  - Si vous ne souhaitez pas inclure de sites dans une recherche, sélectionnez **choisir des sites spécifiques à rechercher**, mais n'ajoutez pas de site à la liste.
    
    **Dossiers publics**
    
    Pour les dossiers publics, vous pouvez choisir d'effectuer une recherche dans tous les dossiers publics de votre organisation Exchange Online ou de ne pas Rechercher des dossiers publics.
    
7. Cliquez sur **Suivant**.
    
8. Sur la page **Nouvelle recherche**, vous pouvez ajouter des mots clés et des conditions pour créer la requête de recherche. 
    
    ![Créer une requête de recherche avec des mots clés et des conditions](media/1b7cf7b5-f1e1-471a-ad5c-48aad8435b00.png)
  
1. Dans la zone située sous **que souhaitez-vous?**, tapez une requête de recherche dans le champ. Vous pouvez spécifier des mots clés, des propriétés de message, telles que des dates d'envoi et de réception, ou des propriétés de document, telles que des noms de fichiers ou la date de la dernière modification d'un document. Vous pouvez utiliser des requêtes plus complexes qui utilisent un opérateur booléen, comme **and**, **or**, **not**, **near**ou **ONEAR**. Vous pouvez également rechercher des informations sensibles (telles que des numéros de sécurité sociale) dans des documents ou Rechercher des documents qui ont été partagés en externe. Si vous laissez la zone mot clé vide, tout le contenu situé dans les emplacements de contenu spécifiés sera inclus dans les résultats de la recherche. 
    
2. Vous pouvez cliquer sur la case à cocher **afficher la liste de mots clés** et entrer un mot clé dans chaque ligne. Dans ce cas, les mots clés de chaque ligne sont connectés par l'opérateur **or** dans la requête de recherche qui est créée. 
    
    ![Vous pouvez taper un mot clé ou une phase de mot-clé dans une ligne de la liste des mots-clés](media/aea1a361-639d-4a82-8c3c-48645ef3fc05.png)
  
    Pourquoi utiliser la liste de mots clés? Vous pouvez obtenir des statistiques qui indiquent le nombre d'éléments qui correspondent à chaque mot clé. Cela peut vous aider à identifier rapidement les mots clés les plus efficaces (et les moins). Vous pouvez également utiliser une phrase de mots clés (entourée de parenthèses) dans une ligne. Pour plus d'informations sur les statistiques de recherche, voir [afficher les statistiques sur les mots clés pour les résultats de la recherche de contenu](view-keyword-statistics-for-content-search.md).
    
    Consultez la section pour obtenir des instructions sur l'utilisation de la liste de mots clés. 
    
3. Cliquez sur **Vérifier la requête pour** Rechercher les fautes de frappe afin de vérifier si votre requête comporte des caractères non pris en charge et des opérateurs booléens qui ne peuvent pas être capitalisés. Les caractères non pris en charge sont souvent masqués et provoquent généralement une erreur de recherche ou renvoient des résultats inattendus. Pour plus d'informations sur les caractères non pris en charge qui sont vérifiés, consultez la rubrique [vérifier votre requête de recherche de contenu pour les erreurs](check-your-content-search-query-for-errors.md).
    
4. Sous **conditions**, ajoutez des conditions à une requête de recherche pour affiner une recherche et renvoyer un ensemble plus raffiné de résultats. Chaque condition ajoute une clause à la requête de recherche KQL créée et exécutée lors du démarrage de la recherche. Une condition est logiquement liée à la requête de mot clé (spécifiée dans la zone de mot clé) par l'opérateur **and** . Cela signifie que les éléments doivent répondre à la fois à la requête de mot clé et à la condition à inclure dans les résultats. Voici comment les conditions vous aident à affiner vos résultats. 
    
||
|:-----|
|Pour plus d'informations sur la création d'une requête de recherche et l'utilisation de conditions, consultez la rubrique [requêtes de mots clés et conditions de recherche pour la recherche de contenu ](keyword-queries-and-search-conditions.md). |
   
9. Cliquez sur **Rechercher** pour enregistrer les paramètres de recherche et commencer la recherche. 
    
    La recherche est démarrée. Une fois la recherche terminée, les informations suivantes s'affichent dans le volet d'informations.
    
    ![Les statistiques de recherche sont affichées dans le volet d'informations de la recherche de contenu sélectionnée](media/2046bb5e-f4cb-4ba7-b7fc-8e5e53dae567.png)
  
1. Date et heure de la dernière exécution de la recherche.
    
2. Nombre (et taille totale) des éléments trouvés qui correspondent à la requête de recherche. Les messages électroniques, les éléments de calendrier et les documents sont des exemples de types d'éléments. Si un élément contient plusieurs instances d'un mot clé recherché, il n'est compté qu'une seule fois dans le nombre total d'éléments. Par exemple, si vous recherchez des mots «stock» ou «Conseil» et qu'un message électronique contient trois occurrences du mot «stock», il n'est compté qu'une seule fois dans le champ **éléments** . 
    
3. Nombre et taille totale des éléments non indexés dans les emplacements de contenu qui ont été recherchés. Le nombre d'éléments non indexés qui ne correspondent pas aux critères de recherche est inclus dans les statistiques de recherche affichées dans le volet d'informations. Si un élément non indexé correspond à la requête de recherche (étant donné que les autres propriétés du message ou du document répondent aux critères de recherche), il ne sera pas inclus dans le nombre estimé d'éléments non indexés. Toutefois, si un élément non indexé est exclu par les critères de recherche, il ne sera pas inclus dans l'estimation des éléments non indexés.
    
4. Nombre de chaque type d'emplacement de contenu dans lequel la recherche a été effectuée. Pour les boîtes aux lettres, Notez que les boîtes aux lettres d'archivage sont incluses dans le nombre total de boîtes aux lettres ayant fait l'objet d'une recherche. Dans l'exemple précédent, quatre boîtes aux lettres utilisateur ont été recherchées et la boîte aux lettres d'archivage de chacun de ces utilisateurs est activée. C'est la raison pour laquelle huit boîtes aux lettres sont mentionnées dans les statistiques de la recherche.
    
5. Liens pour afficher un aperçu des résultats de la recherche ou réexécuter la recherche pour mettre à jour les statistiques de la recherche.
    
    Si nécessaire, cliquez ****![sur Actualiser](media/O365-MDM-Policy-RefreshIcon.gif) l'actualisation pour mettre à jour les informations dans le volet d'informations de la recherche sélectionnée. 
    
[Return to top](run-a-content-search-in-the-security-and-compliance-center.md#top)
  
## <a name="export-search-results"></a>Exporter les résultats de la recherche
<a name="export"> </a>

Une fois que la recherche est exécutée correctement, vous pouvez exporter les résultats de la recherche vers un ordinateur local. Lorsque vous exportez les résultats de la messagerie, ceux-ci sont téléchargés sur votre ordinateur en tant que fichiers PST. Lorsque vous exportez du contenu à partir de sites SharePoint et OneDrive entreprise, des copies des documents Office natifs sont exportées. Des documents et des rapports supplémentaires sont également inclus dans les résultats de recherche exportés. Pour plus d'informations, consultez la rubrique relative [à l'exportation des &amp; résultats de recherche à partir du centre de sécurité conformité Office 365](export-search-results.md).
  
## <a name="preview-search-results"></a>Aperçu des résultats de la recherche
<a name="preview"> </a>

Une fois la recherche terminée, vous pouvez afficher un aperçu des résultats de la recherche. Il existe un certain nombre de limites liées à l'aperçu des résultats de la recherche de contenu. Pour plus d'informations, consultez [la rubrique Limits for Search in &amp; the Office 365 Security Compliance Center](limits-for-content-search.md). Notez que les éléments non indexés ne sont pas disponibles pour l'aperçu.
  
1. Sur la page **recherche de contenu** , sélectionnez une recherche. 
    
2. Dans le volet de détails, sous **Résultats**, cliquez sur **Aperçu des résultats de recherche**. La page **Aperçu des résultats de recherche** s’ouvre et contient la liste des éléments de résultat de recherche. 
    
    Vous pouvez cliquer sur un en-tête de colonne pour trier les résultats en fonction de l'objet, du type, de l'expéditeur ou de la date de réception d'un élément dans la boîte aux lettres source.
    
3. Cliquez sur un élément pour en afficher un aperçu.
    
    L'élément est ouvert dans le volet de visualisation.
    
4. Si un type de fichier n'est pas pris en charge pour l'aperçu ou pour télécharger une copie d'un document, vous pouvez cliquer sur **Télécharger le fichier d'origine** pour le télécharger sur votre ordinateur local. Pour les pages Web. aspx, l'URL de la page est incluse si vous ne disposez pas des autorisations nécessaires pour accéder à la page. 
    
> [!NOTE]
> Si vous affichez un aperçu des résultats de la recherche pour une recherche qui a été exécutée en dernier lieu depuis plus de 7 jours, vous serez invité à mettre à jour les résultats de la recherche. La recherche est réexécutée pour obtenir les résultats les plus récents qui correspondent à la requête de recherche. 
  
### <a name="file-types-that-can-be-previewed"></a>Types de fichiers pouvant être prévisualisés

Vous pouvez afficher un aperçu des types de fichiers pris en charge dans le volet de visualisation. Si un type de fichier n'est pas pris en charge, vous devez télécharger une copie du fichier sur votre ordinateur local pour l'afficher. Les types de fichiers suivants sont pris en charge et peuvent être prévisualisés sur la page **aperçu des résultats** de la recherche. 
  
- . txt,. html,. mhtml
    
- . eml
    
- . doc,. docx,. docm
    
- . pptm,. pptx
    
- .pdf
    
En outre, les types de conteneurs de fichiers suivants sont pris en charge. Vous pouvez afficher la liste des fichiers dans le conteneur dans le volet de visualisation.
  
- .zip
    
- . gzip
    
[Return to top](run-a-content-search-in-the-security-and-compliance-center.md#top)
  
## <a name="update-search-results"></a>Mettre à jour des résultats de recherche
<a name="restart"> </a>

Lorsque vous mettez à jour les résultats d'une recherche de contenu existante, la requête de recherche est réexécutée sur tous les emplacements de contenu spécifiés. La raison évidente de mettre à jour les résultats de la recherche est d'obtenir les données les plus récentes.
  
1. Sur la page **Recherche de contenu**, sélectionnez la recherche dont les résultats doivent être mis à jour. 
    
2. Dans le volet de détails, sous **Résultats**, cliquez sur **Mettre à jour les résultats de la recherche**.
    
    Un message d'État s'affiche indiquant que les résultats sont en cours de récupération. Une fois la recherche terminée, les informations mises à jour s'affichent sous **résultats** dans le volet d'informations. Notez que la date du champ **recherché** dans le volet d'informations est mise à jour à la date et à l'heure actuelles. Pour actualiser les informations dans la liste des recherches de contenu ****![, cliquez sur](media/O365-MDM-Policy-RefreshIcon.gif)actualiser l'actualisation.
    
[Return to top](run-a-content-search-in-the-security-and-compliance-center.md#top)
  
## <a name="edit-a-search"></a>Modifier une recherche
<a name="edit"> </a>

Vous pouvez modifier les boîtes aux lettres sources et la requête de recherche pour une recherche de contenu existante.
  
1. Sur la page **recherche de contenu** , sélectionnez une recherche. 
    
2. Dans le volet de détails, sous **Requête**, cliquez sur **Modifier la recherche**.
    
3. Sur la page **emplacements** , vous pouvez modifier les boîtes aux lettres, les groupes, les sites SharePoint ou les sites OneDrive entreprise à rechercher. Vous pouvez également sélectionner (ou désactiver) pour effectuer une recherche dans tous les dossiers publics dans Exchange. 
    
4. Sur la page de **requête** , vous pouvez modifier la requête de recherche. 
    
5. Pour démarrer la recherche révisée, cliquez sur **Rechercher** sur la page **sources** ou **emplacements** . 
    
    La recherche révisée est démarrée. Lorsque la recherche est terminée, les résultats de la recherche révisée estimés s’affichent dans le volet de détails.
    
## <a name="retry-a-search"></a>Réessayer une recherche
<a name="retry"> </a>

Si une recherche renvoie des erreurs, il n'est pas nécessaire de relancer la recherche dans tous les emplacements de contenu. Vous pouvez réexécuter la recherche de sorte que seuls les emplacements de contenu en échec soient recherchés. Pour relancer la recherche dans tous les emplacements de contenu, vous pouvez mettre à jour les résultats de la recherche.
  
1. Sur la page **recherche de contenu** , sélectionnez la recherche qui contient les emplacements de contenu sur lesquels vous souhaitez effectuer une nouvelle recherche. 
    
2. Dans le volet de détails, sous **Erreur**, cliquez sur **Relancer la recherche**.
    
    Un message d'État s'affiche indiquant que les résultats sont en cours de récupération. Une fois la recherche terminée, les informations mises à jour s'affichent sous **résultats** dans le volet d'informations. Notez que la date du champ **recherché** dans le volet d'informations est mise à jour à la date et à l'heure actuelles. Pour actualiser les informations de la liste des recherches, ****![cliquez sur Actualiser l'actualisation](media/O365-MDM-Policy-RefreshIcon.gif).
    
[Return to top](run-a-content-search-in-the-security-and-compliance-center.md#top)
  
## <a name="more-information"></a>Plus d'informations
<a name="moreinfo"> </a>

Voici plus d'informations sur les recherches de contenu.
  
[Limites et performances](run-a-content-search-in-the-security-and-compliance-center.md#limits)
  
[Éléments non indexés](run-a-content-search-in-the-security-and-compliance-center.md#unindexeditems)
  
[Groupes Microsoft teams et Office 365](run-a-content-search-in-the-security-and-compliance-center.md#teams)
  
[OneDrive Entreprise](run-a-content-search-in-the-security-and-compliance-center.md#onedrive)
  
[Requêtes de recherche](run-a-content-search-in-the-security-and-compliance-center.md#queries)
  
[Recherche de boîtes aux lettres inactives](run-a-content-search-in-the-security-and-compliance-center.md#inactivemailboxes)
  
[Divers](run-a-content-search-in-the-security-and-compliance-center.md#misc)
  
[(Retour au début)](run-a-content-search-in-the-security-and-compliance-center.md#top)
  
 **Limites et performances**
  
- Pour obtenir une description des limites appliquées à la fonctionnalité de recherche de contenu, reportez-vous à la rubrique [Limits for Search in the Office 365 Security &amp; Compliance Center](limits-for-content-search.md).
    
- Microsoft collecte des informations sur les performances des recherches de contenu exécutées par toutes les organisations Office 365. Bien que la complexité de la requête de recherche puisse avoir un impact sur les temps de recherche, le facteur le plus important qui affecte la durée de recherche est le nombre de boîtes aux lettres recherchées. Bien que Microsoft ne fournisse pas de contrat de niveau de service pour les temps de recherche, le tableau suivant répertorie les temps de recherche moyens pour une recherche de contenu sur la base du nombre de boîtes aux lettres incluses dans la recherche.
    
|**Nombre de boîtes aux lettres**|**Durée moyenne de recherche**|
|:-----|:-----|
|100  <br/> |30 secondes  <br/> |
|1,000  <br/> |45 secondes  <br/> |
|10 000  <br/> |4 minutes  <br/> |
|25 000  <br/> |10 minutes  <br/> |
|50 000  <br/> |20 minutes  <br/> |
|100 000  <br/> |25 minutes  <br/> |
   

  
 **Éléments non indexés**
  
- Comme expliqué précédemment, les éléments non indexés dans les emplacements de contenu qui font l'objet de recherches sont inclus dans les résultats de recherche estimés. Si un élément non indexé correspond à la requête de recherche (étant donné que les autres propriétés du message ou du document répondent aux critères de recherche), il ne sera pas inclus dans le nombre estimé d'éléments non indexés. Si un élément non indexé est exclu par les critères de recherche, il n'est pas inclus dans le nombre estimé d'éléments non indexés. Pour plus d'informations, consultez la rubrique [éléments non indexés dans la recherche de contenu](https://go.microsoft.com/fwlink/p/?LinkId=780739).
    

  
 **Groupes Microsoft teams et Office 365**
  
- Microsoft teams est basé sur les groupes Office 365. Par conséquent, la recherche est très similaire. Gardez les points suivants à l'esprit lors de la recherche de contenu dans les groupes Microsoft teams et Office 365.
    
  - Pour rechercher du contenu se trouvant dans des groupes Microsoft teams et Office 365, vous devez spécifier la boîte aux lettres et le site SharePoint qui sont associés à une équipe ou un groupe.
    
  - Exécutez la cmdlet **Get-UnifiedGroup** dans Exchange Online pour afficher les propriétés d'une équipe Microsoft ou d'un groupe Office 365. Il s'agit d'un moyen efficace pour obtenir l'URL du site associé à une équipe ou à un groupe. Par exemple, la commande suivante affiche les propriétés sélectionnées pour un groupe Office 365 nommé équipe leadership senior: 
    
  ```
  Get-UnifiedGroup "Senior Leadership Team" | FL DisplayName,Alias,PrimarySmtpAddress,SharePointSiteUrl
  DisplayName            : Senior Leadership Team
  Alias                  : seniorleadershipteam
  PrimarySmtpAddress     : seniorleadershipteam@contoso.onmicrosoft.com
  SharePointSiteUrl      : https://contoso.sharepoint.com/sites/seniorleadershipteam
  
  ```

    > [!NOTE]
    > Pour exécuter la cmdlet **Get-UnifiedGroup** , vous devez disposer du rôle destinataires en affichage seul dans Exchange Online ou être membre d'un groupe de rôles auquel est affecté le rôle destinataires en affichage seul. 
  
  - Lors de la recherche dans la boîte aux lettres d'un utilisateur, un groupe Microsoft Team ou Office 365 dont l'utilisateur est membre ne sera pas recherché. De même, lorsque vous effectuez une recherche dans une équipe Microsoft ou un groupe Office 365, seule la boîte aux lettres de groupe et le site de groupe que vous spécifiez sont recherchés; les boîtes aux lettres et les comptes OneDrive entreprise des membres du groupe ne sont pas recherchés sauf si vous les ajoutez explicitement à la recherche.
    
  - Pour obtenir la liste des membres d'une équipe Microsoft ou d'un groupe Office 365, vous pouvez afficher les propriétés sur la **page \> groupes d'accueil** dans le centre d'administration Office 365. Vous pouvez également exécuter la commande suivante dans Exchange Online PowerShell: 
    
  ```
  Get-UnifiedGroupLinks <group or team name> -LinkType Members | FL DisplayName,PrimarySmtpAddress 
  ```

    > [!NOTE]
    > Pour exécuter la cmdlet **Get-UnifiedGroupLinks** , vous devez disposer du rôle destinataires en affichage seul dans Exchange Online ou être membre d'un groupe de rôles auquel est affecté le rôle destinataires en affichage seul. 
  
  - Les conversations qui font partie d'un canal Microsoft teams sont stockées dans la boîte aux lettres associée à l'équipe Microsoft. De même, les fichiers que les membres de l'équipe partagent dans un canal sont stockés sur le site SharePoint de l'équipe. Par conséquent, vous devez ajouter la boîte aux lettres d'équipe et le site SharePoint de Microsoft comme emplacement de contenu pour rechercher des conversations et des fichiers dans un canal.
    
  - 
    
    En guise d'alternative, les conversations qui font partie de la liste de conversation de Microsoft teams sont stockées dans la boîte aux lettres Exchange Online des utilisateurs qui participent à la conversation. Et les fichiers qu'un utilisateur partage dans les conversations de conversation sont stockés dans le compte OneDrive entreprise de l'utilisateur qui partage le fichier. Par conséquent, vous devez ajouter les boîtes aux lettres des utilisateurs individuels et les comptes OneDrive entreprise en tant qu'emplacements de contenu pour rechercher des conversations et des fichiers dans la liste des conversations.
    
    > [!NOTE]
    > Les utilisateurs qui participent à des conversations faisant partie de la liste des conversations de Microsoft teams doivent disposer d'une boîte aux lettres Exchange Online (en nuage) pour que vous puissiez Rechercher des conversations de conversation. Cela est dû au fait que les conversations faisant partie de la liste des conversations sont stockées dans les boîtes aux lettres en nuage des participants à la conversation. Si un participant à une conversation ne dispose pas d'une boîte aux lettres Exchange Online, vous ne pourrez pas effectuer de recherche dans les conversations de conversation. Par exemple, dans un déploiement hybride Exchange, les utilisateurs disposant d'une boîte aux lettres locale peuvent participer à des conversations qui font partie de la liste des conversations de Microsoft Teams. Toutefois, dans ce cas, le contenu de cette conversation ne peut pas faire l'objet d'une recherche, car les utilisateurs n'ont pas de boîtes aux lettres en nuage. 
  
  - Chaque canal d'équipe ou d'équipe Microsoft contient un wiki pour la prise de notes et la collaboration. Le contenu wiki est automatiquement enregistré dans un fichier au format. mht. Ce fichier est stocké dans la bibliothèque de documents de données wiki teams sur le site SharePoint de l'équipe. Vous pouvez utiliser l'outil de recherche de contenu pour effectuer des recherches dans le wiki en spécifiant le site SharePoint de l'équipe comme emplacement de contenu à rechercher. 
    
    > [!NOTE]
    > La possibilité de rechercher un wiki pour une équipe ou un canal Microsoft (lors de la recherche sur le site SharePoint de l'équipe) a été publiée le 22 juin 2017. Les pages wiki qui ont été enregistrées ou mises à jour à cette date ou après sont disponibles pour être recherchées. Les pages de wiki enregistrées ou mises à jour avant cette date ne sont pas disponibles pour la recherche. 
  

  
 **OneDrive Entreprise **
  
- Pour collecter une liste des URL pour les sites OneDrive entreprise de votre organisation, consultez la rubrique [créer une liste de tous les emplacements onedrive de votre organisation](https://support.office.com/article/8e200cb2-c768-49cb-88ec-53493e8ad80a). Le script de cet article crée un fichier texte qui contient une liste de tous les sites OneDrive entreprise. Pour exécuter ce script, vous devez installer et utiliser SharePoint Online Management Shell. Veillez à ajouter l'URL du domaine mon site de votre organisation à chaque site OneDrive entreprise que vous souhaitez rechercher. Il s'agit du domaine qui contient l'ensemble de votre OneDrive entreprise; par exemple, `https://contoso-my.sharepoint.com`. Voici un exemple d'URL pour le site OneDrive entreprise d'un utilisateur: `https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft.com`.
    

  
 **Requêtes de recherche**
  
- Gardez les points suivants à l'esprit lors de l'utilisation de la liste de mots clés pour créer une requête de recherche.
    
  - Vous devez activer la case à cocher **afficher la liste des mots** clés, puis taper chaque mot clé dans une ligne distincte pour créer une requête de recherche où les mots clés (ou les expressions de mots clés) de chaque ligne sont reliés par l'opérateur **ou** . Si vous collez simplement une liste de mots clés dans la zone de mot clé ou si vous appuyez sur la touche **entrée** après avoir tapé un mot clé, ils ne seront pas reliés par l'opérateur **or** . Voici un exemple incorrect et approprié pour l'ajout d'une liste de mots clés. 
    
    **Inapproprié**
    
    ![Méthode incorrecte pour mettre en forme une liste de mots clés (en collant la liste dans la zone de mot clé)](media/fb54e3df-232a-439a-b3d7-27a60ec76a4c.png)
  
    **Rectification**
    
    ![La méthode correcte pour mettre en forme une liste de mots clés (en sélectionnant case à cocher et en collant la liste)](media/5d511a7b-c1f9-499c-bffe-e075bfc9adec.png)
  
  - Vous pouvez également préparer une liste de mots clés ou d'expressions de mots clés dans un fichier Excel ou un fichier de texte brut, puis copier et coller votre liste dans la liste des mots clés. Pour ce faire, vous devez activer la case à cocher **afficher la liste de mots clés** . Ensuite, cliquez sur la première ligne de la liste de mots clés et collez votre liste. Chaque ligne du fichier Excel ou texte est collée sur une ligne distincte dans la liste de mots clés. 
    
  - Une fois que vous avez créé une requête à l'aide de la liste de mots clés, il est recommandé de vérifier la syntaxe de requête de recherche (dans le volet d'informations de la recherche sélectionnée) pour que la requête de recherche soit celle que vous souhaitez. Dans la requête de recherche affichée sous **requête** dans le volet d'informations, les mots clés sont séparés par du texte **(c:s)**. cela indique que les mots clés sont connectés par l'opérateur **or** . De même, si votre requête de recherche inclut des conditions, les mots clés et les conditions sont séparés par le texte **(c:c)**. cela indique que les mots clés sont connectés aux conditions par l'opérateur **and** . Voici un exemple de la requête de recherche (affichée dans le volet d'informations) résultant de l'utilisation de la liste de mots clés et d'une condition. 
    
    ![Exemple de requête créée lors de l'utilisation de la liste de mots clés et d'une condition](media/b463750c-57fa-4602-9fed-0d5a420db3ad.png)
  
  - Si vous avez une requête de recherche qui contient des mots clés pour des caractères non anglais (tels que des caractères chinois), vous devrez peut-être utiliser l'applet de commande **Set-ComplianceSearch** pour configurer la propriété de langue pour la recherche de contenu. Lorsque vous créez une recherche de contenu à l'aide de l' &amp; interface utilisateur graphique dans le centre de sécurité conformité, la langue par défaut est neutre. 
    
    Comment savoir si vous devez modifier le paramètre de langue pour une recherche de contenu? Si vous êtes certain que des emplacements de contenu contiennent des caractères non anglais que vous recherchez, mais que la recherche ne renvoie aucun résultat, le paramètre de langue peut en être la cause.
    
    Pour modifier le paramètre de langue d'une recherche de contenu existante, exécutez la commande suivante &amp; dans le centre de sécurité conformité PowerShell:
    
  ```
  Set-ComplianceSearch <name of content search> -Language <culture code value>
  ```

    Par exemple, pour définir le paramètre de langue sur chinois, utilisez `zh-CN` pour la valeur de code de culture. Une fois que vous avez modifié le paramètre de langue, vous devez relancer la recherche. Pour obtenir la liste des valeurs de code de culture possibles, voir [CultureInfo Class](https://go.microsoft.com/fwlink/p/?LinkID=184859). Pour les recherches de contenu, nous vous recommandons d'utiliser des codes de culture en deux parties pour la valeur du paramètre de langue; par exemple, `ja-JP` et non `ja`.
    

  
 **Recherche de boîtes aux lettres inactives**
  
Comme indiqué précédemment, vous pouvez rechercher des boîtes aux lettres inactives dans une recherche de contenu. Voici quelques éléments à garder à l'esprit lors de la recherche de boîtes aux lettres inactives.
  
- Si une recherche de contenu inclut une boîte aux lettres utilisateur et que celle-ci est devenue inactive, la recherche de contenu continue à rechercher dans la boîte aux lettres inactive lorsque vous relancez la recherche après qu'elle a été inactive.
    
- Dans certains cas, un utilisateur peut avoir une boîte aux lettres active et une boîte aux lettres inactive possédant la même adresse SMTP. Dans ce cas, seule la boîte aux lettres spécifique que vous sélectionnez comme emplacement pour une recherche de contenu fera l'objet d'une recherche. En d'autres termes, si vous ajoutez la boîte aux lettres d'un utilisateur à une recherche, vous ne pouvez pas supposer que leurs boîtes aux lettres actives et inactives seront recherchées; seule la boîte aux lettres que vous ajoutez explicitement à la recherche sera recherchée.
    
- Nous vous recommandons vivement d'éviter d'avoir une boîte aux lettres active et une boîte aux lettres inactive avec la même adresse SMTP. Si vous devez réutiliser l'adresse SMTP actuellement attribuée à une boîte aux lettres inactive, nous vous recommandons de récupérer la boîte aux lettres inactive ou de restaurer le contenu d'une boîte aux lettres inactive vers une boîte aux lettres active (ou l'archive d'une boîte aux lettres active), puis de supprimer le boîte aux lettres inactive. Pour plus d'informations, consultez l'une des rubriques suivantes:
    
  - [Récupérer une boîte aux lettres inactive dans Office 365](recover-an-inactive-mailbox.md)
    
  - [Restaurer une boîte aux lettres inactive dans Office 365](restore-an-inactive-mailbox.md)
    
  - [Supprimer une boîte aux lettres inactive dans Office 365](delete-an-inactive-mailbox.md)
    

  
 **Divers**
  
- Les recherches de contenu créées sur la page **recherche** de contenu &amp; dans le centre de sécurité et de conformité ne sont pas affichées dans la page ** &amp; conservation** inaltérable dans le centre d'administration Exchange. Cela est dû au fait que l'architecture de recherche de contenu et les objets &amp; de recherche créés dans le centre de sécurité conformité sont totalement différents de la fonctionnalité de découverte électronique inaltérable dans Exchange Online. 
    
    Pour la même raison, les recherches créées sur la page de **recherche de contenu** ne s'affichent pas sur la page **recherches** d' &amp; un cas de découverte électronique dans le centre de sécurité conformité. 
    
- Quelle est la différence entre le redémarrage et la nouvelle tentative d'une recherche? Lorsque vous redémarrez une recherche, tous les emplacements de contenu spécifiés dans la recherche sont recherchés dans une nouvelle version de la recherche. Toutefois, lorsque vous relancez une recherche, seuls les emplacements de contenu ayant échoué lors de la dernière exécution de la recherche sont recherchés.
   

