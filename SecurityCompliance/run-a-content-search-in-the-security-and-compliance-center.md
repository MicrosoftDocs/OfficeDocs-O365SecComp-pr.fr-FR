---
title: Exécuter une recherche de contenu de la sécurité Office 365 &amp; centre de conformité
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/26/2018
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.ComplianceSearch
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 61852fd9-fe8a-4880-a339-cb19ed3bff4a
description: 'Utiliser la recherche de contenu de sécurité Office 365 &amp; pour rechercher les boîtes aux lettres, les sites SharePoint Online et OneDrive pour des sites Centre de conformité. '
ms.openlocfilehash: 61c6c3933a75567acb04f793cb6815322fb3fada
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527945"
---
# <a name="run-a-content-search-in-the-office-365-security-amp-compliance-center"></a>Exécuter une recherche de contenu de la sécurité Office 365 &amp; centre de conformité

Vous pouvez utiliser l’outil de découverte électronique de recherche de contenu de sécurité Office 365 &amp; centre de conformité pour rechercher des éléments tels que le courrier électronique, les documents et les conversations dans votre organisation Office 365 de messagerie instantanée. Utilisez cet outil pour rechercher des éléments dans ces services Office 365 :
  
- Dossiers publics et boîtes aux lettres Exchange Online
    
- SharePoint Online et OneDrive pour les sites de l’entreprise
    
- Skype pour des conversations
    
- Microsoft Teams 
    
- Groupes Office 365
    
Recherche de contenu est un nouvel outil de recherche de découverte électronique grâce à des fonctionnalités nouvelles et améliorées de montée en charge et de performances. Recherche de contenu permet d’exécuter des recherches de découverte électronique très volumineux. Vous pouvez rechercher toutes les boîtes aux lettres, tous les dossiers publics Exchange et tous les sites SharePoint Online et OneDrive pour les comptes d’entreprise dans une recherche de contenu unique. Il n’existe aucune limite sur le nombre d’emplacements de contenu que vous pouvez rechercher. Il n’existe également aucune limite sur le nombre de recherches autorisées à exécuter en même temps. Une fois que vous exécutez une recherche de contenu, le nombre d’emplacements de contenu et un estimation du nombre de résultats de la recherche est affiché dans le volet de détails sur la page de **recherche de contenu** . Après avoir exécuté une recherche, vous pouvez afficher un aperçu des résultats, obtenir les statistiques de mots clés pour une ou plusieurs recherches, modifier en bloc des recherches de contenu et exporter les résultats vers un ordinateur local. 
  
 **Contenu de cette rubrique**
  
[Créer une recherche](run-a-content-search-in-the-security-and-compliance-center.md#create)
  
[Exporter les résultats de la recherche](run-a-content-search-in-the-security-and-compliance-center.md#export)
  
[Aperçu des résultats de la recherche](run-a-content-search-in-the-security-and-compliance-center.md#preview)
  
[Mettre à jour des résultats de recherche](run-a-content-search-in-the-security-and-compliance-center.md#restart)
  
[Modifier une recherche](run-a-content-search-in-the-security-and-compliance-center.md#edit)
  
[Réessayer une recherche](run-a-content-search-in-the-security-and-compliance-center.md#retry)
  

  
## <a name="before-you-begin"></a>Avant de commencer

- Pour plus d’informations et des conseils sur la création de requêtes de recherche et l’utilisation d’opérateurs de recherche booléens, voir [conditions de recherche pour la recherche de contenu et les requêtes de mot clé](keyword-queries-and-search-conditions.md). Cet article contient également des informations sur la recherche pour les types d’informations sensibles et la recherche de contenu qui est partagé avec des personnes à l’intérieur et à l’extérieur de votre organisation.
    
- Pour accéder à la page de **recherche de contenu** pour effectuer des recherches et aperçu et exporter les résultats de recherche, un administrateur, responsable de la conformité ou un gestionnaire eDiscovery doit être un membre du groupe de rôles eDiscovery responsable de la sécurité &amp; la conformité Centre. Vous n’êtes pas obligé d’attribuer des autorisations dans Exchange Online, SharePoint Online, ou de OneDrive de recherche supplémentaires pour les sites de l’entreprise. Pour plus d’informations, voir [attribuer des autorisations de sécurité Office 365 eDiscovery &amp; centre de conformité](assign-ediscovery-permissions.md).
    
- Il existe des limites appliquées à la recherche de contenu pour maintenir l’intégrité et la qualité des services fournis aux organisations Office 365. Dans la plupart des cas, vous ne pouvez pas modifier ces limites, mais vous devez connaître les afin que vous puissiez prendre ces limites en considération lors de la planification, en cours d’exécution et le dépannage des recherches. Pour plus d’informations, voir [limites pour la recherche de sécurité Office 365 &amp; centre de conformité](limits-for-content-search.md).
    
- Voir la section pour les heures de recherche estimés en fonction du nombre de boîtes aux lettres sont recherchées dans une recherche de contenu unique. 
    
- Comme indiqué précédemment, vous pouvez utiliser la recherche de contenu pour rechercher du contenu dans les groupes d’Office 365 et Microsoft Teams. Cela signifie que vous pouvez rechercher la boîte aux lettres de groupe, calendrier partagé et des sites SharePoint associés à un groupe d’Office 365 et un Team Microsoft. En outre, vous pouvez rechercher les conversations de canal dans un Team Microsoft. Pour plus d’informations sur les groupes d’Office 365 et Microsoft Teams, voir :
    
  - [En savoir plus sur les groupes d’Office 365](https://support.office.com/article/b565caa1-5c40-40ef-9915-60fdb2d97fa2)
    
  - [Aide Microsoft Teams](https://support.office.com/article/23156c0c-2c6e-49dd-8b7b-7c564b76508c)
    
    Voir la section pour obtenir des conseils sur la recherche de contenu dans les groupes d’Office 365 et Microsoft Teams. 
    
[Return to top](run-a-content-search-in-the-security-and-compliance-center.md#top)
  
## <a name="create-a-search"></a>Créer une recherche
<a name="create"> </a>

1. Accédez à [https://protection.office.com](https://protection.office.com).
    
2. Connectez-vous à Office 365 à l’aide de votre compte professionnel ou de l’école.
    
3. Dans le volet gauche du Centre de sécurité et de conformité, cliquez sur **Recherches &amp; enquêtes** \> **Recherche de contenu**.
    
4. Cliquez sur **Nouveau**![Icône Ajouter](media/O365-MDM-CreatePolicy-AddIcon.gif).
    
5. Sur la page **Nouvelle recherche**, entrez un nom pour la recherche de contenu. Ce nom doit être unique dans votre organisation. 
    
6. Choisissez les emplacements de contenu que vous souhaitez rechercher. Vous pouvez rechercher les boîtes aux lettres, les sites et les dossiers publics dans la même recherche.
    
    ![Choisissez les emplacements de contenu que vous souhaitez rechercher](media/da32e3f9-6cd6-4a26-8217-e97a5a7071e4.png)
  
1. **Recherche partout** Sélectionnez cette option pour rechercher tous les emplacements de contenu dans votre organisation. Lorsque vous sélectionnez cette option, vous pouvez choisir rechercher toutes les boîtes aux lettres (y compris les boîtes aux lettres et boîtes aux lettres inactives pour tous les groupes d’Office 365 et Microsoft Teams), tous les SharePoint et OneDrive pour les sites de l’entreprise (qui inclut les sites de tous les groupes d’Office 365 et Les équipes Microsoft) et tous les dossiers publics.
    
    ![Cliquez sur la recherche partout pour rechercher tous les emplacements de contenu](media/86f132f1-0a2a-4048-900c-9f219d909ef2.png)
  
2. **Sélection d’emplacement personnalisé** Sélectionnez cette option pour sélectionner les boîtes aux lettres et les sites que vous souhaitez rechercher. Si vous choisissez cette option, vous avez la possibilité de rechercher tous les emplacements de contenu pour un service spécifique (par exemple, recherche toutes les boîtes aux lettres Exchange), ou vous pouvez rechercher les emplacements de contenu spécifiques pour un service d’Office 365.
    
    Gardez les points suivants à l’esprit lorsque vous ajoutez des emplacements de contenu à rechercher :
    
    **Boîtes aux lettres**
    
  - Lorsque vous cliquez sur **Ajouter**![ajouter une icône](media/ITPro-EAC-AddIcon.gif) pour spécifier les boîtes aux lettres à rechercher, le sélecteur de boîte aux lettres qui s’affiche est vide. Il s’agit par défaut pour améliorer les performances. Pour ajouter des destinataires à cette liste, tapez un nom (un minimum de 3 caractères) dans la zone de recherche, cliquez sur **Rechercher**![icône de recherche](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif).
    
  - Vous pouvez ajouter des boîtes aux lettres inactives et les groupes de distribution à la liste des boîtes aux lettres à rechercher. Pour les groupes de distribution, les boîtes aux lettres des membres du groupe sont recherchés. Notez que les groupes de distribution dynamique ne sont pas pris en charge.
    
  - Pour obtenir une liste des boîtes aux lettres inactives dans votre organisation, exécutez la commande `Get-Mailbox -InactiveMailboxOnly` dans Exchange Online PowerShell. Sinon, vous pouvez passer à la **gouvernance des données** \> **rétention** de sécurité &amp; centre de conformité, puis cliquez sur **plus de**![ellipses barre de Navigation](media/9723029d-e5cd-4740-b5b1-2806e4f28208.gif) \> **boîtes aux lettres inactives**.
    
  - Vous pouvez également ajouter la boîte aux lettres qui est associé à un groupe d’Office 365 ou un Team Microsoft. Dans ce cas, seulement la boîte aux lettres d’équipe ou de groupe est recherchée ; les membres du groupe ou de l’équipe de boîtes aux lettres ne sont pas recherchés. Pour rechercher les, vous devez les ajouter explicitement à la recherche.
    
  - Si vous ne souhaitez pas inclure des boîtes aux lettres à la recherche, sélectionnez **Choisir les boîtes aux lettres spécifiques à rechercher**, mais ne pas ajouter une boîte aux lettres à la liste.
    
    **Sites**
    
  - Cliquez sur **Ajouter**![ajouter une icône](media/ITPro-EAC-AddIcon.gif) pour ajouter des sites à la recherche. Tapez l’URL pour chaque site que vous souhaitez rechercher. L’outil de recherche de contenu sera valider l’URL, puis ajoutez-le à la liste des sites pour la recherche. 
    
  - Vous pouvez ajouter le SharePoint qui est associé à un groupe d’Office 365 ou un Team Microsoft. Voir la section pour obtenir des conseils sur la recherche de l’URL de groupe ou de l’équipe. 
    
  - Si vous ne souhaitez pas inclure tous les sites dans une recherche, sélectionnez **Choisir les sites spécifiques à rechercher**, mais ne pas ajouter un site à la liste.
    
    **Dossiers publics**
    
    Pour les dossiers publics, vous pouvez choisir de rechercher tous les dossiers publics dans votre organisation Exchange Online ou pas rechercher des dossiers publics.
    
7. Cliquez sur **Suivant**.
    
8. Sur la page **Nouvelle recherche**, vous pouvez ajouter des mots clés et des conditions pour créer la requête de recherche. 
    
    ![Créer une requête de recherche avec des mots clés et des conditions](media/1b7cf7b5-f1e1-471a-ad5c-48aad8435b00.png)
  
1. Dans la zone sous **que voulez-vous rechercher les ?**, tapez une requête de recherche dans la zone. Vous pouvez spécifier des mots clés, message propriétés telles qu’envoyés et reçus de dates, ou des propriétés de document telles que les noms de fichiers ou la date de dernière modification un document. Vous pouvez utiliser des requêtes plus complexes qui utilisent un opérateur booléen, tels que **et**, **ou**, **pas**, **NEAR**ou **ONEAR**. Vous pouvez également rechercher des informations sensibles (comme les numéros de sécurité sociale) dans des documents ou de recherche pour les documents qui ont été partagées en externe. Si vous laissez la zone mot clé vide, tout le contenu situé dans les emplacements de contenu spécifiés sera inclus dans les résultats de recherche. 
    
2. Vous pouvez cliquer sur la case à cocher **Afficher la liste des mots clés** et le type d’un mot clé dans chaque ligne. Si vous procédez ainsi, les mots clés dans chaque ligne sont connectés par l’opérateur **ou** dans la requête de recherche qui est créée. 
    
    ![Vous pouvez taper un mot clé ou la phase de mot clé dans une ligne dans la liste des mots clés](media/aea1a361-639d-4a82-8c3c-48645ef3fc05.png)
  
    Pourquoi utiliser la liste des mots clés ? Vous pouvez obtenir des statistiques indiquant le nombre d’éléments correspondent à chaque mot clé. Cela peut vous aider à identifier rapidement les mots clés qui sont le plus (et moins) efficaces. Vous pouvez également utiliser une phrase de mots clés (entourée parenthèses) dans une ligne. Pour plus d’informations sur les statistiques de recherche, voir [Afficher les statistiques de mots clés pour les résultats de recherche de contenu](view-keyword-statistics-for-content-search.md).
    
    Voir la section pour obtenir des instructions sur l’utilisation de la liste des mots clés. 
    
3. Cliquez sur **vérifier la requête pour toute erreur** pour vérifier votre requête pour les caractères non pris en charge et des opérateurs booléens qui ne peuvent pas être mise en majuscule. Caractères non pris en charge sont souvent masqués et généralement de provoquer une erreur de recherche ou renvoyer des résultats inattendus. Pour plus d’informations sur les caractères non pris en charge qui sont en cours, voir [vérifier votre requête de recherche de contenu pour les erreurs](check-your-content-search-query-for-errors.md).
    
4. Dans des **Conditions**, ajouter des conditions à une requête de recherche pour affiner la recherche et de renvoyer un jeu de résultats plus précis. Chaque condition ajoute une clause à la requête de recherche KQL qui est créée et exécutée lorsque vous démarrez la recherche. Une condition est logiquement connectée à la requête de mot clé (spécifiée dans la zone mots clés) par l’opérateur **AND** . Cela signifie que les éléments ont afin de répondre à la requête de mot clé et la condition à inclure dans les résultats. Il s’agit de comment conditions vous aider à limiter les résultats. 
    
||
|:-----|
|Pour plus d’informations sur la création d’une requête de recherche et à l’aide de conditions, voir [conditions de recherche pour la recherche de contenu et les requêtes de mot clé ](keyword-queries-and-search-conditions.md). |
   
9. Cliquez sur **Rechercher** pour enregistrer les paramètres de recherche et commencer la recherche. 
    
    La recherche est lancée. Lors de la recherche est terminée, les informations suivantes s’affiche dans le volet détails.
    
    ![Statistiques de la recherche sont affichés dans le volet de détails de la recherche de contenu sélectionné](media/2046bb5e-f4cb-4ba7-b7fc-8e5e53dae567.png)
  
1. Date et heure de la dernière exécution de la recherche.
    
2. Le nombre (et taille totale) des éléments qui ont été détectés qui correspondant à la requête de recherche. Les exemples de types d’éléments de messages électroniques, éléments de calendrier et des documents. Si un élément contient plusieurs instances d’un mot clé qui est recherchée, elle est comptée uniquement une seule fois dans le nombre total d’éléments. Par exemple, si vous recherchez des mots « stock » ou « tip » et un message électronique contient trois occurrences du mot « stock », il est comptée uniquement une seule fois dans le champ **d’éléments** . 
    
3. Le nombre et la taille totale des éléments non indexés dans les emplacements de contenu qui ont été exclus. Le nombre d’éléments non indexés qui ne respectent pas les critères de recherche s’être inclus dans les statistiques de la recherche affichés dans le volet détails. Si un élément non indexés correspondances la recherche de requête (étant donné que les autres propriétés de message ou un document aux critères de recherche), il ne sont pas inclus dans l’estimation du nombre d’éléments non indexés. Toutefois, si un élément non indexée est exclu par les critères de recherche, il ne sont pas inclus dans l’estimation des éléments non indexés.
    
4. Le nombre de chaque type d’emplacement du contenu qui a été recherché. Pour les boîtes aux lettres, notez que les boîtes aux lettres d’archive sont inclus dans le nombre total de boîtes aux lettres qui ont été exclus. Dans l’exemple précédent, quatre boîtes aux lettres utilisateur ont été exclus et la boîte aux lettres d’archive pour chacun de ces utilisateurs est activé. C’est pourquoi huit boîtes aux lettres sont citées dans les statistiques de la recherche.
    
5. Liens pour afficher un aperçu de la recherche des résultats ou exécuter la recherche pour mettre à jour les statistiques de la recherche.
    
    Si nécessaire, cliquez sur **Actualiser**![icône Actualiser](media/O365-MDM-Policy-RefreshIcon.gif) pour mettre à jour les informations contenues dans le volet d’informations pour la recherche sélectionnée. 
    
[Return to top](run-a-content-search-in-the-security-and-compliance-center.md#top)
  
## <a name="export-search-results"></a>Exporter les résultats de la recherche
<a name="export"> </a>

Après qu’une recherche est exécutée correctement, vous pouvez exporter les résultats de recherche sur un ordinateur local. Lorsque vous exportez des résultats de la messagerie, elles sont téléchargées sur votre ordinateur en tant que fichiers PST. Lorsque vous exportez le contenu à partir de SharePoint et OneDrive pour les sites, les copies des documents Office natifs sont exportées. Il existe également des documents et des rapports qui sont inclus dans les résultats de recherche exportés. Pour plus d’informations, voir [résultats de la recherche de l’exportation à partir de la sécurité de 365 Office &amp; centre de conformité](export-search-results.md).
  
## <a name="preview-search-results"></a>Aperçu des résultats de la recherche
<a name="preview"> </a>

Une fois une recherche terminée avec succès, vous pouvez afficher les résultats de recherche. Il existe un certain nombre de limites liées à afficher un aperçu des résultats de la recherche de contenu. Pour plus d’informations, voir [limites pour la recherche de sécurité Office 365 &amp; centre de conformité](limits-for-content-search.md). Notez que les éléments non indexés ne sont pas disponibles pour afficher un aperçu.
  
1. Dans la page de **recherche de contenu** , sélectionnez une recherche. 
    
2. Dans le volet de détails, sous **Résultats**, cliquez sur **Aperçu des résultats de recherche**. La page **Aperçu des résultats de recherche** s’ouvre et contient la liste des éléments de résultat de recherche. 
    
    Vous pouvez cliquer sur un en-tête de colonne pour trier les résultats en fonction du sujet, type, l’expéditeur ou la date de qu'un élément a été reçu dans la boîte aux lettres source.
    
3. Cliquez sur Afficher un aperçu d’un élément.
    
    L’élément est ouvert dans le volet de visualisation.
    
4. Si un type de fichier n’est pas pris en charge pour aperçu ou pour télécharger une copie d’un document, vous pouvez cliquer sur **Télécharger le fichier d’origine** pour le télécharger sur votre ordinateur local. Pour les pages Web .aspx, l’URL de la page est inclus si vous n’avez ne peut-être pas les autorisations pour accéder à la page. 
    
> [!NOTE]
> Si vous affichez les résultats de recherche pour une recherche de la dernière exécution de plus de 7 jours, vous devrez mettre à jour les résultats de recherche. La recherche est réexécutée pour obtenir des résultats plus récentes qui répondent à la requête de recherche. 
  
### <a name="file-types-that-can-be-previewed"></a>Types de fichiers qui peuvent être affichés

Vous pouvez afficher un aperçu des types de fichiers pris en charge dans le volet de visualisation. Si un type de fichier n’est pas pris en charge, vous devrez télécharger un exemplaire du fichier sur votre ordinateur local pour l’afficher. Types de fichiers suivants sont pris en charge et peuvent être affichés dans la page **Aperçu des résultats de recherche** . 
  
- .txt, .html, .mhtml
    
- .eml
    
- .doc, .docx, .docm
    
- .pptm, .pptx
    
- .pdf
    
En outre, les types de conteneur de fichier suivants sont pris en charge. Vous pouvez afficher la liste des fichiers dans le conteneur dans le volet de visualisation.
  
- .zip
    
- .gzip
    
[Return to top](run-a-content-search-in-the-security-and-compliance-center.md#top)
  
## <a name="update-search-results"></a>Mettre à jour des résultats de recherche
<a name="restart"> </a>

Lorsque vous mettez à jour les résultats d’une recherche de contenu existante, la requête de recherche est réexécutée sur tous les emplacements de contenu spécifiés. La raison évidente à mettre à jour les résultats de recherche consiste à obtenir les données les plus récentes.
  
1. Sur la page **Recherche de contenu**, sélectionnez la recherche dont les résultats doivent être mis à jour. 
    
2. Dans le volet de détails, sous **Résultats**, cliquez sur **Mettre à jour les résultats de la recherche**.
    
    Un message de statut s’affiche indiquant que les résultats sont en cours d’extraction. Lors de la recherche est terminée, les informations mises à jour s’affiche sous **résultats** dans le volet détails. Notez que la date dans le champ de **recherche** dans le volet d’informations est mis à jour à la date et l’heure. Cliquez sur **Actualiser**pour actualiser les informations contenues dans la liste de recherche de contenu,![icône Actualiser](media/O365-MDM-Policy-RefreshIcon.gif).
    
[Return to top](run-a-content-search-in-the-security-and-compliance-center.md#top)
  
## <a name="edit-a-search"></a>Modifier une recherche
<a name="edit"> </a>

Vous pouvez modifier les boîtes aux lettres source et la requête de recherche pour une recherche de contenu existante.
  
1. Dans la page de **recherche de contenu** , sélectionnez une recherche. 
    
2. Dans le volet de détails, sous **Requête**, cliquez sur **Modifier la recherche**.
    
3. Dans la page **emplacements** , vous pouvez modifier les boîtes aux lettres, des groupes, des sites SharePoint ou OneDrive pour les sites à rechercher. Vous pouvez également sélectionner (ou désactivez) pour rechercher tous les dossiers publics dans Exchange. 
    
4. Dans la page de la **requête** , vous pouvez modifier la requête de recherche. 
    
5. Pour démarrer la recherche révisée, cliquez sur **Rechercher** dans les **Sources** ou les **emplacements de** page. 
    
    La recherche révisée est démarrée. Lorsque la recherche est terminée, les résultats de la recherche révisée estimés s’affichent dans le volet de détails.
    
## <a name="retry-a-search"></a>Réessayer une recherche
<a name="retry"> </a>

Si une recherche renvoie des erreurs, vous n’êtes pas obligé de nouveau tous les emplacements de contenu de recherche. Vous pouvez réexécuter la recherche afin qu’uniquement les emplacements de contenu ayant échoué sont recherche à nouveau. Pour renouveler rechercher tous les emplacements de contenu, vous pouvez mettre à jour les résultats de recherche.
  
1. Dans la page **recherche de contenu** , sélectionnez la recherche qui contient les emplacements de contenu que vous souhaitez rechercher de nouveau. 
    
2. Dans le volet de détails, sous **Erreur**, cliquez sur **Relancer la recherche**.
    
    Un message de statut s’affiche indiquant que les résultats sont en cours d’extraction. Lors de la recherche est terminée, les informations mises à jour s’affiche sous **résultats** dans le volet détails. Notez que la date dans le champ de **recherche** dans le volet d’informations est mis à jour à la date et l’heure. Cliquez sur **Actualiser**pour actualiser les informations contenues dans la liste des recherches,![icône Actualiser](media/O365-MDM-Policy-RefreshIcon.gif).
    
[Return to top](run-a-content-search-in-the-security-and-compliance-center.md#top)
  
## <a name="more-information"></a>Plus d'informations
<a name="moreinfo"> </a>

Voici le plus d’informations sur les recherches de contenu.
  
[Limites et performances](run-a-content-search-in-the-security-and-compliance-center.md#limits)
  
[Éléments non indexés](run-a-content-search-in-the-security-and-compliance-center.md#unindexeditems)
  
[Les équipes Microsoft et des groupes d’Office 365](run-a-content-search-in-the-security-and-compliance-center.md#teams)
  
[OneDrive Entreprise](run-a-content-search-in-the-security-and-compliance-center.md#onedrive)
  
[Requêtes de recherche](run-a-content-search-in-the-security-and-compliance-center.md#queries)
  
[Recherche des boîtes aux lettres inactives](run-a-content-search-in-the-security-and-compliance-center.md#inactivemailboxes)
  
[Divers](run-a-content-search-in-the-security-and-compliance-center.md#misc)
  
[(Retour au début)](run-a-content-search-in-the-security-and-compliance-center.md#top)
  
 **Limites et performances**
  
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
   

  
 **Éléments non indexés**
  
- Comme expliqués précédemment éléments non indexés dans les emplacements de contenu qui sont recherchés sont inclus dans les résultats de recherche estimés. Si un élément non indexés correspondances la recherche de requête (étant donné que les autres propriétés de message ou un document aux critères de recherche), il ne sont pas inclus dans l’estimation du nombre d’éléments non indexés. Si un élément non indexée est exclu par les critères de recherche, il n’est également inclus dans l’estimation du nombre d’éléments non indexés. Pour plus d’informations, voir [les éléments non indexés dans la recherche de contenu](https://go.microsoft.com/fwlink/p/?LinkId=780739).
    

  
 **Les équipes Microsoft et des groupes d’Office 365**
  
- Teams Microsoft reposent sur les groupes d’Office 365. Par conséquent, leur recherche est très similaire. Gardez les éléments suivants à l’esprit lors de la recherche du contenu dans Microsoft Teams et groupes d’Office 365.
    
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
    
  - 
    
    Vous pouvez également les conversations qui font partie de la liste de conversation dans Microsoft Teams sont stockées dans la boîte aux lettres Exchange Online des utilisateurs qui participent à la conversation. Et fichiers utilisateur partage conversation sont stockés dans le compte professionnel de l’utilisateur qui partage le fichier OneDrive. Par conséquent, vous devez ajouter les boîtes aux lettres individuelles et OneDrive pour les comptes d’entreprise en tant qu’emplacements de contenu pour rechercher les conversations et les fichiers dans la liste de conversation.
    
    > [!NOTE]
    > Les utilisateurs de participer à des conversations qui font partie de la liste de conversation dans Microsoft Teams doivent avoir une Exchange Online (en nuage) boîte aux lettres dans l’ordre vous permet de rechercher des conversations. C’est parce que les conversations qui font partie de la liste de conversation sont stockées dans les boîtes aux lettres en nuage de participants à la conversation. Si un participant de conversation ne possède une boîte aux lettres Exchange Online, vous ne pourrez pas rechercher des conversations. Par exemple, dans un déploiement Exchange hybride, les utilisateurs avec une boîte aux lettres locale peuvent être en mesure de participer à des conversations qui font partie de la liste de conversation dans Microsoft Teams. Toutefois dans ce cas, le contenu de ces conversation ne sont pas utilisables dans une requête, car les utilisateurs ne possèdent des boîtes aux lettres en nuage. 
  
  - Chaque canal Microsoft Team ou de l’équipe contient un Wiki de prise de notes et de collaboration. Le contenu Wiki est automatiquement enregistré dans un fichier au format .mht. Ce fichier est stocké dans la bibliothèque de documents équipes Wiki données sur le site SharePoint de l’équipe. Vous pouvez utiliser l’outil de recherche de contenu pour rechercher le Wiki en spécifiant des sites SharePoint de l’équipe en tant que l’emplacement de contenu de recherche. 
    
    > [!NOTE]
    > La fonction de recherche le Wiki pour un canal ou Microsoft Team (lors de la recherche de sites SharePoint de l’équipe) a été publiée le 22 juin 2017. Wiki pages qui ont été enregistrées ou mis à jour sur date ou après qui sont disponibles à rechercher. Pages Wiki dernier enregistrement ou mis à jour avant cette date ne sont pas disponibles pour la recherche. 
  

  
 **OneDrive Entreprise **
  
- Pour collecter une liste d’URL pour le OneDrive des sites d’entreprise dans votre organisation, voir [créer une liste de tous les emplacements de OneDrive dans votre organisation](https://support.office.com/article/8e200cb2-c768-49cb-88ec-53493e8ad80a). Le script dans cet article crée un fichier texte qui contient une liste de tous les OneDrive pour les sites de l’entreprise. Pour exécuter ce script, vous devrez installer et utiliser SharePoint Online Management Shell. Veillez à ajouter l’URL de domaine du site Mon site dans votre organisation à chaque site d’entreprise que vous souhaitez rechercher OneDrive. Il s’agit du domaine qui contient tous vos OneDrive entreprise ; par exemple, `https://contoso-my.sharepoint.com`. Voici un exemple d’URL pour OneDrive d’un utilisateur pour le site de l’entreprise : `https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft.com`.
    

  
 **Requêtes de recherche**
  
- Conserver les éléments suivants à l’esprit lors de l’utilisation de la liste des mots clés pour créer une requête de recherche.
    
  - Vous devez sélectionner la case à cocher **Afficher la liste des mots clés** , puis tapez chaque mot clé dans une ligne distincte pour créer une requête de recherche dans laquelle les mots clés (ou des expressions de mot clé) dans chaque ligne sont connectées par l’opérateur **OR** . Si vous venez collez une liste de mots clés dans la zone mot clé ou appuyez sur la touche **entrée** après avoir tapé un mot clé, ils ne sont pas connectés par l’opérateur **OR** . Voici un exemple incorrect et correct de l’ajout d’une liste de mots clés. 
    
    **Incorrect**
    
    ![La façon de mettre en forme une liste des mots clés (en-coller de la liste dans la zone mot clé) incorrecte](media/fb54e3df-232a-439a-b3d7-27a60ec76a4c.png)
  
    **Correct**
    
    ![Comment mettre en forme une liste des mots clés (en activant la case à cocher, puis collage liste)](media/5d511a7b-c1f9-499c-bffe-e075bfc9adec.png)
  
  - Vous pouvez également préparer une liste des mots clés ou expressions de mots clés dans un fichier Excel ou un fichier texte brut, puis copiez et collez dans votre liste à la liste des mots clés. Pour ce faire, vous devez sélectionner la case à cocher **Afficher la liste des mots clés** . Ensuite, cliquez sur la première ligne dans la liste des mots clés et collez votre liste. Chaque ligne du fichier Excel ou du texte est collé pour séparer les lignes dans la liste des mots clés. 
    
  - Après avoir créé une requête à l’aide de la liste des mots clés, il est conseillé de vérifier la syntaxe de requête de recherche (dans le volet de détails de la recherche sélectionné) pour que la recherche requête est ce que vous souhaitiez. Dans la requête de recherche qui s’affiche sous la **requête** dans le volet détails, les mots clés sont séparés par le texte **(c:s)**. cela indique que les mots clés sont connectés par l’opérateur **OR** . De même, si votre requête de recherche comprend les conditions, les mots clés et les conditions sont séparées par le texte **(c : c)**. cela indique que les mots clés sont connectés aux conditions par l’opérateur **AND** . Voici un exemple de la requête de recherche (affichée dans le volet détails) lors de l’utilisation de la liste des mots clés et une condition de résultats. 
    
    ![Exemple de la requête qui est créée lors de l’utilisation de la liste des mots clés et une condition](media/b463750c-57fa-4602-9fed-0d5a420db3ad.png)
  
  - Si vous disposez d’une requête de recherche qui contient des mots clés pour les caractères non anglais (tels que des caractères chinois), vous devrez peut-être utiliser l’applet de commande **Set-ComplianceSearch** pour configurer la propriété language pour la recherche de contenu. Lorsque vous créez une recherche de contenu à l’aide de l’interface utilisateur de la sécurité &amp; centre de conformité, la langue par défaut est neutre. 
    
    Comment savoir si vous devez modifier le paramètre de langue pour une recherche de contenu ? Si vous êtes certains emplacements de contenu contiennent des caractères non anglais que vous recherchez, mais la recherche ne renvoie aucun résultat, le paramètre de langue peut être la cause.
    
    Pour modifier le paramètre de langue pour une recherche de contenu existante, exécutez la commande suivante dans la sécurité &amp; PowerShell du centre de conformité :
    
  ```
  Set-ComplianceSearch <name of content search> -Language <culture code value>
  ```

    Par exemple, pour modifier le paramètre de langue chinois, vous utiliseriez `zh-CN` pour la valeur de code de culture. Une fois que vous modifiez le paramètre de langue, vous devrez réexécuter la recherche. Pour obtenir la liste des valeurs de code de culture possibles, consultez [CultureInfo, classe](https://go.microsoft.com/fwlink/p/?LinkID=184859). Lors de la recherche de contenu, nous vous recommandons d’utiliser les codes de culture de deux parties de la valeur du paramètre de langue ; par exemple, `ja-JP` et non `ja`.
    

  
 **Recherche des boîtes aux lettres inactives**
  
Comme indiqué précédemment, vous pouvez rechercher les boîtes aux lettres inactives dans une recherche de contenu. Voici quelques points à prendre en compte lors de la recherche de boîtes aux lettres inactives.
  
- Si une recherche de contenu inclut une boîte aux lettres utilisateur et que cette boîte aux lettres est ensuite effectuée inactive, la recherche de contenu continuera à rechercher la boîte aux lettres inactive lorsque vous exécutez de nouveau la recherche dès que celui-ci est inactif.
    
- Dans certains cas, un utilisateur peut avoir une boîte aux lettres active et une boîte aux lettres inactive qui ont la même adresse SMTP. Dans ce cas, recherche portera uniquement la boîte aux lettres spécifique que vous sélectionnez un emplacement pour une recherche de contenu. En d’autres termes, si vous ajoutez des boîtes aux lettres d’un utilisateur à une recherche, vous ne pouvez pas supposer que les deux actives et inactives boîtes aux lettres portera ; recherche portera uniquement à la boîte aux lettres que vous ajoutez explicitement à la recherche.
    
- Il est vivement recommandé de ne pas avoir une boîte aux lettres active et la boîte aux lettres inactive avec la même adresse SMTP. Si vous avez besoin de réutiliser l’adresse SMTP qui est actuellement attribué à une boîte aux lettres inactive, nous vous recommandons de récupérer la boîte aux lettres inactive ou restaurer le contenu d’une boîte aux lettres inactive dans une boîte aux lettres active (ou l’archivage d’une boîte aux lettres active) et supprimez le boîte aux lettres inactive. Pour plus d’informations, consultez les rubriques suivantes :
    
  - [Récupérer une boîte aux lettres inactive dans Office 365](recover-an-inactive-mailbox.md)
    
  - [Restaurer une boîte aux lettres inactive dans Office 365](restore-an-inactive-mailbox.md)
    
  - [Supprimer une boîte aux lettres inactive dans Office 365](delete-an-inactive-mailbox.md)
    

  
 **Divers**
  
- Recherches créées dans la page de **recherche de contenu** dans la sécurité de contenu &amp; centre de conformité ne sont pas affichés sur la **In-Place eDiscovery &amp; maintenez** page dans le centre d’administration Exchange. C’est parce que l’architecture de recherche de contenu et les objets de recherche créés dans la sécurité &amp; centre de conformité sont complètement différente de la fonctionnalité de découverte électronique In-Place dans Exchange Online. 
    
    De même, créé dans la page de **recherche de contenu** de recherche ne sont pas affichés dans la page de **recherche** d’un cas de découverte de la sécurité &amp; centre de conformité. 
    
- Quelle est la différence entre le redémarrage et nouvelle tentative en cours d’une recherche ? Lorsque vous redémarrez une recherche, tous les emplacements de contenu qui sont spécifiés dans la recherche sont effectuées à nouveau dans une nouvelle recherche d’aperçu. Toutefois, lorsque vous relancez une recherche, uniquement les emplacements de contenu ayant échoué lors de la dernière exécution de la recherche sont effectuées à nouveau.
   

