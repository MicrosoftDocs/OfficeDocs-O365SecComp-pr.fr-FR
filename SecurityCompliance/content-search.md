---
title: Recherche de contenu dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 53390468-eec6-45cb-b6cd-7511f9c909e4
description: Utilisez l’outil recherche de contenu dans le centre de conformité dans Office 365 ou Microsoft 365 pour rechercher du contenu dans les boîtes aux lettres, les sites SharePoint Online, les comptes OneDrive, Microsoft Teams, les groupes Office 365 et les conversations Skype Entreprise. Vous pouvez utiliser des requêtes de recherche par mot clé et des conditions de recherche pour affiner les résultats de la recherche. Vous pouvez ensuite obtenir un aperçu et exporter les résultats de la recherche. La recherche de contenu est également un outil efficace pour rechercher du contenu lié à une demande d’objet de données RGPD.
ms.openlocfilehash: 2fff94899dabca85338ba1ca924ec37afa1dccf3
ms.sourcegitcommit: 873c5bc0e6cd1ca3dfdb3a99a5371353b419311f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/22/2019
ms.locfileid: "36493165"
---
# <a name="content-search-in-office-365"></a>Recherche de contenu dans Office 365

Vous pouvez utiliser l’outil eDiscovery de la recherche de contenu dans le centre de conformité dans Office 365 ou Microsoft 365 pour rechercher des éléments sur place, tels que des messages électroniques, des documents et des conversations par messagerie instantanée dans votre organisation Office 365. Utilisez cet outil pour rechercher des éléments dans ces services Office 365 :
  
- Boîtes aux lettres et dossiers publics Exchange Online
    
- Sites SharePoint Online et comptes OneDrive Entreprise
    
- Conversations Skype Entreprise
    
- Microsoft Teams 
    
- Groupes Office 365
    
Après avoir exécuté une recherche de contenu, le nombre d’emplacements de contenu et l’estimation du nombre de résultats de recherche sont affichés dans le profil de recherche. Vous pouvez également afficher rapidement des statistiques, telles que les emplacements de contenu qui ont le plus grand nombre d’éléments qui correspondent à la requête de recherche. Une fois que vous avez effectué une recherche, vous pouvez afficher un aperçu des résultats ou les exporter sur un ordinateur local.

## <a name="create-a-search"></a>Créer une recherche

Pour accéder à la page **recherche de contenu** pour effectuer des recherches et afficher un aperçu et exporter les résultats de la recherche, un administrateur, un officier de conformité ou un gestionnaire d’eDiscovery doit être membre du groupe de rôles gestionnaire eDiscovery dans le Centre de conformité & de sécurité. Pour plus d'informations, voir [Attribution d'autorisations eDiscovery](assign-ediscovery-permissions.md).
  
1. Allez à [https://protection.office.com](https://protection.office.com) et entrez vos adresse de courrier et mot de passe Office 365.
    
2. Cliquez sur**Recherche** \> **Recherche de contenu**.
    
3. Sur la page de**recherche**, cliquez sur la flèche en regard de ![ajouter une icône](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **nouvelle recherche**. 
    
    ![Liste déroulante Nouvelle recherche](media/76b25861-55c5-4f50-9d48-9e2be2d0d078.png)
  
    Vous pouvez choisir l’une des options suivantes :
    
    - **Recherche guidée :** cette option démarre un assistant qui vous guide dans la création de la recherche. L’interface utilisateur permettant de sélectionner des emplacements de contenu et de créer la requête de recherche est identique à l’option **nouvelle recherche**. 
    
    - **Nouvelle recherche:** cette option affiche une interface utilisateur mise à jour pour créer une recherche. Il s’agit de l’option par défaut si vous cliquez sur**nouvelle recherche**.
    
    - **Rechercher par liste d’ID** : cette option vous permet de rechercher des messages électroniques spécifiques et d’autres éléments de boîte aux lettres à l’aide d’une liste d’ID Exchange. Pour créer une recherche de liste d’ID (anciennement appelée recherche ciblée), vous devez envoyer un fichier de valeurs séparées par des virgules (CSV) qui identifie les éléments de boîte aux lettres spécifiques à rechercher. Pour consulter les instructions, voir[Préparer un fichier CSV pour une recherche de contenu de liste d’ID dans Office 365](csv-file-for-an-id-list-content-search.md).
    
    Le reste des étapes de cette procédure s’applique au nouveau flux de travail de recherche par défaut.
    
4. Cliquez sur **nouvelle recherche** dans la liste déroulante. 
    
5. Sous **requête de recherche**, spécifiez les éléments suivants :
    
    ![Spécifier les mots clés, les conditions et les emplacements à rechercher](media/1e6de9dd-eac9-4e2a-819d-9740cf6c9106.png)
  
   - **Mots clés à Rechercher :** tapez une requête de recherche dans la zone**Mots clés**. Vous pouvez spécifier des mots clés, des propriétés de message telles que les dates d’envoi et de réception, ou des propriétés de document telles que les noms de fichier ou la date de dernière modification d’un document. Vous pouvez utiliser des requêtes plus complexes qui utilisent un opérateur booléen, tels que **ET**, **OU**, **PAS**, et **PRÈS**. Vous pouvez également rechercher des informations sensibles (des numéros de sécurité sociale, par exemple) dans des documents ou rechercher des documents qui ont été partagés en externe. Si vous laissez la zone du mot clé vide, tout le contenu se trouvant dans les emplacements de contenu spécifiés sera inclus dans les résultats de recherche.
    
      Vous pouvez également cliquer sur la case à cocher **Afficher la liste de mots clés **puis taper un mot clé dans chaque ligne. Si vous procédez ainsi, les mots clés sur chaque ligne sont connectés à l’aide d'un opérateur logique (**c:s**) qui présente les mêmes fonctionnalités que l’opérateur **OU** de la requête de recherche créée. 
    
      Pourquoi utiliser la liste de mots clés ? Vous pouvez obtenir des statistiques qui indiquent le nombre d’éléments qui correspondent à chaque mot clé. Cela peut vous aider à identifier rapidement les mots clés les plus importants (et les moins). Vous pouvez également utiliser une expression de mot clé (entre parenthèses) dans une ligne. Pour plus d’informations sur les statistiques de recherche, voir [afficher les statistiques des mots clés pour les résultats de recherche de contenu](view-keyword-statistics-for-content-search.md).

     > [!NOTE]
     > Pour réduire les problèmes liés aux longues listes de mots clés, vous êtes désormais limité à 20 lignes au maximum dans la liste de mots clés.
    
    - **Conditions :** vous pouvez ajouter des conditions dans une requête de recherche pour affiner une recherche et obtenir un ensemble de résultats plus précis. Chaque condition ajoute une clause à la requête de recherche qui est créée et exécutée lorsque vous démarrez la recherche. Une condition est connectée à la requête de mot-clé (spécifiée dans la zone de mot-clé) sur le plan logique par l’opérateur logique (**c:c**), qui est similaire dans son fonctionnement à l’opérateur **ET**. Cela signifie que les éléments doivent satisfaire la requête de mot-clé et une ou plusieurs conditions pour être inclus dans les résultats. C’est ainsi que les conditions contribuent à affiner vos résultats. Pour obtenir la liste et la description des conditions que vous pouvez utiliser dans une requête de recherche, voir la section «conditions de recherche» dans les [requêtes par mots-clés et conditions de recherche pour la recherche de contenu](keyword-queries-and-search-conditions.md#search-conditions).
    
       - **Emplacements :** choisissez les emplacements de contenu à rechercher.
    
      - **Tous les emplacements :** utilisez cette option pour rechercher tous les emplacements de contenu au sein de votre organisation. Il s’agit du courrier dans toutes les boîtes aux lettres Exchange (y compris toutes les boîtes aux lettres inactives, les boîtes aux lettres de tous les groupes Office 365, les boîtes aux lettres de toutes les équipes Microsoft), toutes les conversations Skype Entreprise, l’ensemble des sites SharePoint et OneDrive Entreprise (y compris les sites pour tous les groupes Office 365 et Microsoft Teams) et les éléments dans tous les dossiers publics Exchange.
    
      - **Emplacements spécifiques :** Utilisez cette option pour rechercher des emplacements de contenu spécifiques. Vous pouvez effectuer une recherche dans tous les emplacements de contenu pour un service Office 365 spécifique (par exemple, la recherche dans toutes les boîtes aux lettres Exchange ou la recherche dans tous les sites SharePoint), ou vous pouvez rechercher des emplacements spécifiques dans l’un des services Office 365 affichés. 
    
        ![Interface utilisateur permettant de choisir les emplacements de contenu à rechercher](media/9a09708b-f8a2-4382-8c4e-2c610ec33c72.png)
  
         Vous pouvez également ajouter des groupes de distribution à la liste des boîtes aux lettres Exchange dans laquelle effectuer la recherche. Pour les groupes de distribution, la recherche porte sur les boîtes aux lettres des membres du groupe. L’utilisation de groupes de distribution dynamique n’est pas prise en charge.
    
       > [!NOTE]
       > Lorsque vous effectuez une recherche dans tous les emplacements de boîtes aux lettres ou uniquement des boîtes aux lettres spécifiques, les données d’autres applications Office 365 qui sont enregistrées dans les boîtes aux lettres d’utilisateur sont incluses lorsque vous exportez les résultats d’une recherche de contenu. Ces données ne sont pas incluses dans les résultats de recherche estimés et ne sont pas disponibles pour en aperçu. Elles sont incluses lorsque vous exportez et téléchargez les résultats de recherche. Pour plus d'informations, consultez la rubrique [Contenu stocké dans les boîtes aux lettres Exchange Online](what-is-stored-in-exo-mailbox.md).

    
6. Une fois que vous avez configuré votre requête de recherche, cliquez sur**enregistrer & exécuter**.
    
7. Dans la page **enregistrer la recherche**, tapez un nom pour la recherche, puis une description facultative qui vous permet d’identifier la recherche. Le nom de la recherche doit être unique dans toute votre organisation. 
    
8. Cliquez ensuite sur **Enregistrer** pour démarrer la recherche. 
    
    Une fois que vous avez enregistré et exécuté la recherche, les résultats renvoyés par la recherche sont affichés dans le volet résultats. Selon la manière dont le paramètre d’aperçu est configuré, les résultats de la recherche s’affichent ou vous devez cliquer sur **Aperçu des résultats** pour les afficher. Pour plus d’informations, voir la section suivante. 
    
Pour accéder de nouveau à la recherche de contenu ou accéder aux recherches de contenu répertoriées sur la page **recherche de contenu**, sélectionnez la recherche, puis cliquez sur **Ouvrir**. 
  
Pour effacer les résultats ou créer une autre recherche, cliquez sur ![ajouter une icône](media/O365-MDM-CreatePolicy-AddIcon.gif)**nouvelle recherche**. 

  
## <a name="preview-search-results"></a>Aperçu des résultats de la recherche

Il y a deux paramètres de configuration pour afficher un aperçu des résultats de la recherche. Une fois que vous avez exécuté une nouvelle recherche ou ouvert une recherche existante, cliquez sur * * résultats individuels * * pour afficher les paramètres d’aperçu suivants : 
  
![Paramètres aperçu des résultats de la recherche](media/83519477-1c85-4442-8886-481f186fd758.png)
  
1. **Aperçu des résultats automatique** : ce paramètre affiche les résultats de la recherche après l’exécution d’une recherche.
    
2. **Aperçu des résultats manuel** : ce paramètre affiche les espaces réservés dans le volet résultats de la recherche , et affiche le bouton **Aperçu des résultats** sur lequel vous devez cliquer pour afficher les résultats de la recherche. Il s’agit du paramètre par défaut. Il permet d’améliorer les performances de la recherche en n’affichant pas automatiquement les résultats de la recherche lorsque vous ouvrez une recherche existante. 
    
Il existe des limites relatives au nombre d’éléments pouvant être prévisualisés. Pour plus d’informations, voir [Limites des résultats de recherche](limits-for-content-search.md). 
  
Pour obtenir la liste des types de fichiers pris en charge qui peuvent être prévisualisés, voir [aperçu des résultats de la recherche](#previewing-search-results) dans la section «plus d’informations sur la recherche de contenu». Si un type de fichier n’est pas pris en charge pour l’aperçu ou pour télécharger une copie d'un document, vous pouvez cliquer sur **Télécharger le fichier d’origine** pour le télécharger sur votre ordinateur local. Pour les pages Web .aspx, l’URL de la page est incluse, même si vous n’êtes peut-être pas autorisé à accéder à la page. 
  
Les éléments non indexés ne peuvent pas être affichés en aperçu.
  
## <a name="view-information-and-statistics-about-a-search"></a>Afficher les informations et les statistiques d’une recherche

Une fois que vous avez créé et exécuté une recherche de contenu, vous pouvez afficher des statistiques sur les résultats de recherche estimés. Celle-ci inclut un résumé des résultats de la recherche, les statistiques de requête telles que le nombre d’emplacements de contenu contenant des éléments qui correspondent à la requête de recherche, ainsi que le nom des emplacements de contenu qui ont le plus grand nombre d’éléments correspondants. Vous pouvez afficher les statistiques d’une ou plusieurs recherches de contenu. Cela vous permet de comparer rapidement les résultats de plusieurs recherches et de prendre des décisions sur l’efficacité de vos requêtes de recherche.
  
Vous pouvez également télécharger les statistiques de recherche et les statistiques de mots clés dans un fichier CSV. Cela vous permet d’utiliser les fonctionnalités de filtrage et de tri dans Excel pour comparer les résultats et préparer des rapports pour vos résultats de recherche.
  
Pour afficher les statistiques de recherche :
  
1. Dans la **page recherche de contenu**, cliquez sur **Ouvrir**, puis cliquez sur la recherche pour laquelle vous voulez afficher les statistiques. 
    
2. Sur la page volante, cliquez sur **Ouvrir la requête**. 
    
3. Dans la liste déroulante **résultats individuels**, cliquez sur**profil de recherche**.
    
4. Dans la liste déroulante **type**, cliquez sur l’une des options suivantes selon les statistiques de recherche que vous voulez afficher. 
    
  - **Résumé :** affiche des statistiques pour chaque type d’emplacement de contenu recherché. Ce contenu représente le nombre d’emplacements de contenu contenant des éléments qui correspondaient à la requête de recherche, ainsi que le nombre total et la taille des éléments de résultats de recherche. Il s’agit du paramètre par défaut.
    
  - **Requêtes :** affiche les statistiques relatives à la requête de recherche. Il s’agit du type d’emplacement de contenu auquel les statistiques de requête s’appliquent, qui fait partie de la requête de recherche pour laquelle les statistiques sont applicables (Notez que **Primary** indique la requête de recherche entière), le nombre d’emplacements de contenu qui contiennent des éléments qui correspondent à la requête de recherche, ainsi que le nombre total et la taille des éléments trouvés (à l’emplacement de contenu spécifié) qui correspondent à la requête de recherche. Les statistiques relatives aux éléments non indexés ( également appelés *éléments partiellement indexés*) s’affichent également. Toutefois, seuls les éléments partiellement indexés des boîtes aux lettres sont inclus dans les statistiques. Les éléments partiellement indexés de SharePoint et OneDrive ne sont pas inclus dans les statistiques.
    
  - **Emplacements principaux :** affiche des statistiques sur le nombre d’éléments qui correspondent à la requête de recherche dans chaque emplacement de contenu. Les 1 000 principaux emplacements sont affichés.
    
Pour plus d’informations sur les statistiques de recherche, voir [afficher les statistiques des mots clés pour les résultats de recherche de contenu](view-keyword-statistics-for-content-search.md).
  
  
## <a name="export-search-results"></a>Exporter les résultats de la recherche

Après avoir effectué une recherche, vous pouvez exporter les résultats de la recherche vers un ordinateur local. Lorsque vous exportez des résultats du courrier électronique, ils sont téléchargés sur votre ordinateur dans des fichiers PST ou en tant que messages individuels. Lorsque vous exportez du contenu à partir des sites SharePoint et OneDrive, des copies des documents Office natifs sont exportées. D’autres documents et rapports sont inclus dans les résultats exportés. Vous pouvez également exporter le rapport résultats de la recherche et non les éléments réels.
  
Exporter les résultats de la recherche :
  
1. Sur la page **Recherche de contenu**, cliquer sur la recherche dont les résultats doivent être exportés. 
    
2. Dans la page flyout, cliquez sur l’icône![exporter les résultats de la recherche](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png), ** plus**, puis cliquez sur **Exporter les résultats**. Vous pouvez également exporter un rapport des résultats de la recherche.
    
3. Complétez les sections sur la page de passage des **résultats à l’exportation**. Veillez à utiliser la barre de défilement pour afficher toutes les options d’exportation. 
    
Pour obtenir des instructions détaillées et des conseils de dépannage, voir :
  
- [Exporter les résultats de la recherche de contenu](export-search-results.md)
    
- [Exporter un rapport de recherche de contenu](export-a-content-search-report.md)
    
  
## <a name="more-information-about-content-search"></a>Plus d'informations sur le service de recherche de contenu

Pour plus d’informations sur les recherches de contenu, voir les sections suivantes.
  
[Limites de la recherche de contenu](#content-search-limits)
  
[Exécuter une requête de recherche](#building-a-search-query)
  
[Recherche de comptes OneDrive](#searching-onedrive-accounts)
  
[Recherche Microsoft Teams et Groupes Office 365](#searching-microsoft-teams-and-office-365-groups)
  
[Recherche des boîtes aux lettres inactives](#searching-inactive-mailboxes)
  
[Recherche de boîtes aux lettres déconnectées ou sans licence](#searching-disconnected-or-de-licensed-mailboxes)

[Affichage des résultats de recherche](#previewing-search-results)
  
[Éléments partiellement indexés](#partially-indexed-items)
  
### <a name="content-search-limits"></a>Limites de la recherche de contenu

- Pour obtenir une description des limites appliquées à la fonctionnalité de recherche de contenu, consultez la rubrique [Limites de la recherche de contenu](limits-for-content-search.md).
    
- Microsoft collecte les informations de performance pour les recherches de contenu effectuées par toutes les organisations Office 365. Bien que la complexité de la requête de recherche puisse avoir un impact sur les heures de recherche, le facteur le plus important qui détermine la durée de la recherche est le nombre de boîtes aux lettres recherchées. Bien que Microsoft ne fournisse pas d’accord de niveau de service pour les horaires de recherche, le tableau suivant répertorie les durées de recherche moyennes d’une recherche de contenu sur la base du nombre de boîtes aux lettres incluses dans la recherche.
    
|**Nombre de boîtes aux lettres**|**Temps moyen de recherche**|
|:-----|:-----|
|100  <br/> |30 secondes  <br/> |
|1 000  <br/> |45 secondes  <br/> |
|10 000  <br/> |4 minutes  <br/> |
|25 000  <br/> |10 minutes  <br/> |
|50 000  <br/> |20 minutes  <br/> |
|100 000  <br/> |25 minutes  <br/> |
  
### <a name="building-a-search-query"></a>Exécuter une requête de recherche

Pour plus d’informations sur la création d’une requête de recherche, l’utilisation d’opérateurs de recherche booléens et de conditions de recherche, ainsi que la recherche de types d’informations sensibles et de contenu partagés avec des utilisateurs externes à votre organisation, voir [Requêtes par mots clés et recherche conditions pour la recherche de contenu](keyword-queries-and-search-conditions.md).
  
Gardez les points suivants à l’esprit lorsque vous utilisez la liste de mots clés pour créer une requête de recherche.
  
- Vous devez cocher la case **Afficher la liste de mots clés**, puis taper chaque mot-clé dans une ligne distincte pour créer une requête de recherche dans laquelle les mots-clés (ou les phrases de mots-clés) de chaque ligne sont connectés par l’opérateur **ou**. Si vous collez une liste de mots clés dans la zone de mot clé ou appuyez sur la touche **entrée** après avoir tapé un mot clé, ils ne sont pas connectés par l’opérateur **ou**. Voici quelques exemples incorrects et corrects d’ajout d’une liste de mots clés. 
    
    **Incorrect**
    
    ![Procédure incorrecte de mise en forme d’une liste de mots clés (en collant la liste dans la zone mot clé)](media/fb54e3df-232a-439a-b3d7-27a60ec76a4c.png)
  
    **Correct**
    
    ![La façon correcte de mettre en forme une liste de mots clés (en sélectionnant la case à cocher, puis en collant la liste)](media/5d511a7b-c1f9-499c-bffe-e075bfc9adec.png)
  
- Vous pouvez également préparer une liste de mots clés ou d’expressions de mots clés dans un fichier Excel ou un fichier texte brut, puis copier et coller votre liste dans la liste de mots clés. Pour ce faire, vous devez activer la case à cocher **afficher la liste de mots clés**. Cliquez ensuite sur la première ligne de la liste de mots clés, puis collez votre liste. Chaque ligne du fichier Excel ou texte est copiée dans une ligne distincte de la liste des mots clés. 
    
- Une fois que vous avez créé une requête à l’aide de la liste de mots clés, nous vous conseillons de vérifier la syntaxe de requête de recherche pour faire en sorte que la requête corresponde à ce que vous souhaitez. Dans la requête de recherche affichée sous **requête**, dans le volet Détails, les mots clés sont séparés par le texte **(c:s)**. Cela indique que les mots clés sont connectés à l’aide d’un opérateur logique similaire à une fonctionnalité à l’opérateur **ou**. De même, si votre requête de recherche inclut des conditions, les mots clés et les conditions sont séparés par le texte **(c:c)**. Cela indique que les mots clés sont connectés aux conditions à l’aide d’un opérateur logique similaire à une fonctionnalité à l’opérateur **ET**. Voici un exemple de requête de recherche (affichée dans le volet Détails) qui résulte de l’utilisation de la liste de mots clés et d’une condition. 
    
    ![Exemple de requête créée lors de l’utilisation de la liste de mots clés et d’une condition](media/b463750c-57fa-4602-9fed-0d5a420db3ad.png)
  
- Lorsque vous effectuez une recherche de contenu, Office 365 vérifie automatiquement la présence de caractères non pris en charge et d’opérateurs booléens qui ne sont pas en majuscules dans votre requête de recherche. En règle générale, les caractères non pris en charge sont masqués et entraînent une erreur ou renvoient des résultats inattendus. Pour plus d’informations sur les caractères non pris en charge qui ont été vérifiés, voir [vérifier la présence d’erreurs dans votre requête de recherche de contenu](check-your-content-search-query-for-errors.md).
    
- Si vous avez une requête de recherche qui contient des mots clés pour les caractères non anglais (tels que les caractères chinois) , vous pouvez cliquer sur l'icône **langue-pays/région**![requête pays/région dans la recherche de contenu ](media/8d4b60c8-e1f1-40f9-88ae-ee2a7eca0886.png) et sélectionner une valeur de code de culture dans le pays/région pour la recherche. La langue/région par défaut est neutre. Comment savoir si vous avez besoin de modifier le paramètre de langue d’une recherche de contenu ? Si vous êtes certain que les emplacements de contenu contiennent les caractères non anglais que vous recherchez, mais que la recherche ne renvoie aucun résultat, le paramètre de langue peut être à l’origine du problème. 
  
### <a name="searching-onedrive-accounts"></a>Recherche de comptes OneDrive

- Pour recueillir la liste des URL des sites OneDrive au sein de votre organisation, voir [créer une liste de tous les emplacements OneDrive au sein de votre organisation](https://support.office.com/article/8e200cb2-c768-49cb-88ec-53493e8ad80a). Ce script dans cet article crée un fichier texte qui contient une liste de tous les sites OneDrive. Pour exécuter ce script, vous devez installer et utiliser SharePoint Online Management Shell. N’oubliez pas d’ajouter l’URL du domaine MySite de votre organisation à chaque site OneDrive dans lequel vous souhaitez effectuer une recherche. Il s’agit du domaine où se trouve tout le contenu de votre OneDrive (par exemple,`https://contoso-my.sharepoint.com`). Voici un exemple d’URL pour le site d’un utilisateur OneDrive : `https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft.com`.
    
    Dans le cas rare où le nom d’utilisateur principal (UPN) d’une personne est modifié, l’URL de son emplacement OneDrive est modifiée pour incorporer le nouveau nom d’utilisateur principal (UPN). Dans ce cas, vous devez modifier une recherche de contenu en ajoutant la nouvelle URL OneDrive de l’utilisateur et en supprimant l’ancienne.
  
### <a name="searching-microsoft-teams-and-office-365-groups"></a>Recherche Microsoft Teams et Groupes Office 365

Vous pouvez effectuer une recherche dans la boîte aux lettres associée à un groupe Office 365 ou Microsoft Team. Étant donné que Microsoft Teams est basé sur les groupes Office 365, la recherche est similaire. Dans les deux cas, la recherche porte uniquement sur la boîte aux lettres de groupe ou d’équipe. Les boîtes aux lettres des membres du groupe ou de l’équipe ne sont pas recherchées. Pour effectuer une recherche, vous devez les ajouter spécifiquement à la recherche.
  
Gardez les points suivants à l’esprit lors de la recherche de contenu dans les groupes Microsoft Teams et Office 365.
  
- Pour rechercher du contenu se trouvant dans Teams et Groupes Office 365, vous devez spécifier la boîte aux lettres et le site SharePoint qui sont associés à une équipe ou à un groupe.
    
- Exécutez l'applet de commande **Get-UnifiedGroup** dans Exchange Online pour afficher les propriétés d’une équipe ou d’un groupe Office 365. Il s’agit d’un bon moyen pour obtenir l’URL du site associé à une équipe ou à un groupe. Par exemple, la commande suivante affiche les propriétés sélectionnées d’un groupe Office365 nommé Senior Leadership Team : 
    
  ```
  Get-UnifiedGroup "Senior Leadership Team" | FL DisplayName,Alias,PrimarySmtpAddress,SharePointSiteUrl
  DisplayName            : Senior Leadership Team
  Alias                  : seniorleadershipteam
  PrimarySmtpAddress     : seniorleadershipteam@contoso.onmicrosoft.com
  SharePointSiteUrl      : https://contoso.sharepoint.com/sites/seniorleadershipteam
  
  ```

    > [!NOTE]
    > Pour exécuter l'applet de commande **Get-UnifiedGroup**, vous devez avoir le rôle de destinataires en affichage seul dans Exchange Online ou être membre d’un groupe de rôles affecté du rôle de destinataires en affichage seul. 
  
- Lorsque vous effectuez une recherche dans la boîte aux lettres d’un utilisateur, aucun des groupes Office365 ou équipe dont l’utilisateur est membre n’est inclus dans la recherche. De même, lorsque vous effectuez une recherche dans une équipe ou un groupe Office 365, seules les boîtes aux lettres de groupe et les sites de groupe que vous spécifiez sont recherchés. Les boîtes aux lettres et les comptes OneDrive Entreprise des membres du groupe ne sont pas recherchés, sauf si vous les ajoutez explicitement à la recherche.
    
- Pour obtenir la liste des membres d’une équipe ou d’un groupe Office 365, vous pouvez afficher les propriétés sur la page **Accueil \> Groupes** dans le centre d’administration Microsoft 365. Vous pouvez également exécuter la commande suivante dans Exchange Online PowerShell : 
    
  ```
  Get-UnifiedGroupLinks <group or team name> -LinkType Members | FL DisplayName,PrimarySmtpAddress 
  ```

    > [!NOTE]
    > Pour exécuter l'applet de commande **Get-UnifiedGroupLinks**, vous devez avoir le rôle de destinataires en affichage seul dans Exchange Online ou être membre d’un groupe de rôles affecté du rôle de destinataires en affichage seul. 
  
- Les conversations faisant partie d’un canal d’équipe sont stockées dans la boîte aux lettres associée à l’équipe. De même, les fichiers partagés par les membres d’une équipe dans un canal sont stockés sur le site SharePoint de l’équipe. Par conséquent, vous devez ajouter la boîte aux lettres d’équipe et le site SharePoint comme emplacement de contenu pour rechercher des conversations et des fichiers dans un canal.
    
- De même, les conversations faisant partie de la liste de conversations dans Teams sont stockées dans la boîte aux lettres Exchange Online des utilisateurs qui participent à la conversation. Les fichiers partagés par un utilisateur dans les conversations Chat sont stockés dans le compte OneDrive Entreprise de l’utilisateur qui partage le fichier. Par conséquent, vous devez ajouter les boîtes aux lettres d’utilisateur individuelles et les comptes OneDrive Entreprise comme emplacements de contenu pour rechercher des conversations et des fichiers dans la liste de conversations.
    
    > [!NOTE]
    > Dans un déploiement Exchange hybride, les utilisateurs disposant d’une boîte aux lettres locale peuvent participer aux conversations qui font partie de la liste de Conversations dans Teams. Dans ce cas, le contenu de ces conversations peut également faire l’objet d’une recherche, car il est enregistré dans une zone de stockage basée sur le Cloud (appelée *boîte aux lettres basée sur le Cloud pour les utilisateurs locaux*) pour les utilisateurs disposant d’une boîte aux lettres locale. Pour plus d’informations, voir[recherche de boîtes aux lettres dans le Cloud pour les utilisateurs locaux dans Office 365](search-cloud-based-mailboxes-for-on-premises-users.md).
  
- Toutes les équipes ou canaux d’équipe contiennent un site wiki pour la prise de notes et la collaboration. Le contenu wiki est automatiquement enregistré dans un fichier au format .mht. Ce fichier est stocké dans la bibliothèque de documents wiki Teams sur le site SharePoint de l’équipe. Vous pouvez utiliser l’outil recherche de contenu pour effectuer une recherche sur le site wiki en spécifiant le site SharePoint de l’équipe comme emplacement de contenu à rechercher. 
    
    > [!NOTE]
    > La fonctionnalité de recherche d’une équipe ou d’un canal sur le site wiki (lorsque vous effectuez une recherche sur le site SharePoint de l’équipe) a été publiée le 22 juin 2017. Les pages wiki qui ont été enregistrées ou mises à jour à cette date ou après peuvent être recherchées. Les pages wiki enregistrées ou mises à jour avant cette date ne sont pas disponibles pour la recherche. 
 
- Les informations de synthèse pour les réunions et les appels dans un canal Teams sont également stockées dans les boîtes aux lettres des utilisateurs qui composent la réunion ou l’appel. Cela signifie que vous pouvez utiliser la recherche de contenu pour rechercher ces enregistrements de synthèse. Ces informations de résumé sont les suivantes : 
  
  - Date, heure de début, heure de fin et durée d’une réunion ou d’un appel

  - Date et heure quand chaque participant a joint ou quitté la réunion ou de l’appel

  - Appels envoyés à la messagerie vocale

  - Appels manqués ou sans réponse

  - Appels de transfert, représentés par deux appels distincts

  La possibilité d’effectuer une recherche dans les enregistrements de synthèse des réunions et des appels peut prendre jusqu’à 8 heures.

  Dans les résultats de la recherche, les résumés de la réunion sont identifiés en tant que **réunion** dans le**champ type** et les résumés d’appels sont identifiés en tant qu’**appel**. De plus, les conversations qui font partie d’une chaîne de Teams et de conversations 1xN sont identifiées en tant que **messages instantanés** dans le **champ type**.
  
  ![Les réunions, les appels et les conversations 1xN de Teams sont identifiés dans le champ type.](media/O365-ContentSearch-Teams-MessageKind.png)

- Vous pouvez utiliser la propriété**type de courrier**ou la condition de recherche **type de message** pour rechercher spécifiquement du contenu dans Teams. 
  
  - Pour utiliser la propriété**Type** dans le cadre de la requête de recherche par mot clé, dans la zone **Mots clés** d'une requête de recherche, tapez`kind:microsoftteams`.

    ![Utilisez type:microsoftteams dans la zone Mots clés](media/O365-ContentSearch-Teams-Keywords.png)
  
  - Pour utiliser une condition de recherche, ajoutez la condition **type de message** et utilisez la valeur`microsoftteams`. 

    ![Utilisez la condition type de message avec la valeur microsoftteams.](media/O365-ContentSearch-Teams-MessageKindCondition.png)

Les conditions sont logiquement connectées à la requête de mot clé par l’opérateur **et**. Cela signifie qu’un élément doit correspondre à la requête de mot clé et à la condition de recherche à renvoyer dans les résultats de la recherche. Pour obtenir plus d’informations, reportez-vous à la rubrique «Guide des conditions d’utilisation» dans[Requêtes par mots-clés et conditions de recherche pour la recherche de contenu](keyword-queries-and-search-conditions.md#guidelines-for-using-conditions).
  
### <a name="searching-inactive-mailboxes"></a>Recherche des boîtes aux lettres inactives

Vous pouvez effectuer une recherche dans les boîtes aux lettres inactives dans une recherche de contenu. Pour obtenir une liste des boîtes aux lettres inactives de votre organisation, exécutez la commande `Get-Mailbox -InactiveMailboxOnly` dans Exchange Online PowerShell. Vous pouvez également accéder à **Rétention**de la ** gouvernance des données** \> dans le centre de sécurité & conformité, puis cliquer sur **Plus**![ Barre de navigation : sélections ](media/9723029d-e5cd-4740-b5b1-2806e4f28208.gif)\> ** boîtes aux lettres inactives **.
  
Voici quelques éléments à prendre en considération lors de la recherche de boîtes aux lettres inactives.

- Si une recherche de contenu existante inclut une boîte aux lettres utilisateur et que cette boîte aux lettres devient ensuite inactive, la recherche de contenu se poursuit dans la boîte aux lettres inactive lorsque vous relancez cette recherche.
    
- Un utilisateur peut parfois avoir une boîte aux lettres active et une boîte aux lettres inactive portant la même adresse SMTP. Dans ce cas, la recherche porte sur la boîte aux lettres que vous sélectionnez en tant qu’emplacement à des fins de recherche de contenu. En d’autres termes, si vous ajoutez la boîte aux lettres d’un utilisateur à une recherche, vous ne pouvez pas supposer que les boîtes aux lettres actives et inactives sont recherchées. Seules les boîtes aux lettres que vous ajoutez explicitement à la recherche font l’objet d’une recherche.
    
- Vous pouvez utiliser le centre de sécurité et de conformité PowerShell pour créer une recherche de contenu pour effectuer une recherche dans une boîte aux lettres inactive. Pour ce faire, vous devez préalablement ajouter un point (. ) à l’adresse de messagerie du propriétaire de boîte aux lettres inactive. Par exemple, la commande suivante crée une recherche de contenu qui recherche dans une boîte aux lettres inactive l’adresse de courrier pavelb@contoso.onmicrosoft.com:

   ``` 
   New-ComplianceSearch -name InactiveMailboxSearch -ExchangeLocation .pavelb@contoso.onmicrosoft.com -AllowNotFoundExchangeLocationsEnabled $true
   ```

- Nous vous déconseillons vivement d’utiliser une boîte aux lettres active et une boîte aux lettres inactive portant la même adresse SMTP. Si vous devez réutiliser l’adresse SMTP attribuée à une boîte aux lettres inactive, nous vous recommandons de récupérer la boîte aux lettres inactive ou de restaurer le contenu d’une boîte aux lettres inactive dans une boîte aux lettres active (ou l’archive d’une boîte aux lettres active), puis de supprimer la boîte aux lettres inactive. Pour plus d'informations, consultez l'une des rubriques suivantes :
    
  - [Récupérer une boîte aux lettres inactive dans Office 365](recover-an-inactive-mailbox.md)
    
  - [Restaurer une boîte aux lettres inactive dans Office 365](restore-an-inactive-mailbox.md)
    
  - [Supprimer une boîte aux lettres inactive dans Office 365](delete-an-inactive-mailbox.md)

### <a name="searching-disconnected-or-de-licensed-mailboxes"></a>Recherche de boîtes aux lettres déconnectées ou sans licence

Si la licence Exchange Online (ou la licence Office 365 entière) est supprimée d’un compte d’utilisateur dans Office 365 ou Azure Active Directory, la boîte aux lettres de l'utilisateur devient une *boîte aux lettres déconnectée*. Cela signifie que la boîte aux lettres n’est plus associée au compte d’utilisateur. Voici ce qui se produit lorsque vous effectuez des recherches dans les boîtes aux lettres déconnectées :

- Si la licence est supprimée d’une boîte aux lettres, il n’est plus possible d’y effectuer des recherches. 

- Si une recherche de contenu existante inclut une boîte aux lettres dont laquelle la licence est supprimée, aucun résultat de la boîte aux lettres déconnectée ne sera renvoyé si vous réexécutez la recherche de contenu.

- Si vous utilisez la cmdlet **New-ComplianceSearch** pour créer une recherche de contenu et spécifiez une boîte aux lettres déconnectée comme emplacement de contenu Exchange où effectuer la recherche, la recherche de contenu ne renverra aucun résultat de la boîte aux lettres déconnectée.

Si vous devez conserver les données d’une boîte aux lettres déconnectée pour y effectuer des recherches, vous devez placer la boîte aux lettres en conservation avant de supprimer la licence. Cela conserve les données et permet de continuer à effectuer des recherches dans la boîte aux lettres déconnectée jusqu’à ce que la conservation soit supprimée. Pour plus d’informations sur les conservations, voir [Comment identifier le type de conservation placé sur une boîte aux lettres Exchange Online](identify-a-hold-on-an-exchange-online-mailbox.md).

### <a name="previewing-search-results"></a>Affichage des résultats de recherche

Vous pouvez afficher un aperçu des types de fichiers pris en charge dans le volet de visualisation. Si un type de fichier n’est pas pris en charge, vous devez télécharger une copie du fichier sur votre ordinateur local pour l’afficher. Les types de fichiers suivants sont pris en charge et peuvent être prévisualisés dans le volet résultats de la recherche.
  
- .txt, .html, .mhtml
    
- .eml
    
- .doc, .docx, .docm
    
- .pptm, .pptx
    
- .pdf
    
De plus, les types de conteneur de fichier suivants sont pris en charge. Vous pouvez afficher la liste des fichiers dans le conteneur dans le volet de visualisation.
  
- .zip
    
- .gzip
    
### <a name="partially-indexed-items"></a>Éléments partiellement indexés

- Comme indiqué précédemment, les éléments partiellement indexés dans les boîtes aux lettres sont inclus dans les résultats de recherche estimés. Les éléments partiellement indexés de SharePoint et OneDrive ne sont pas inclus dans les résultats de recherche estimés. 
    
- Si un élément partiellement non indexé correspond à la requête de la recherche (car d’autres propriétés de document ou de message répondent aux critères de recherche), il ne sera pas inclus dans l’estimation du nombre d’éléments non indexés. Si un élément partiellement indexé est exclu des critères de recherche, il n’est pas inclus dans le nombre estimé d’éléments non indexés. Pour plus d’informations, voir[Éléments partiellement indexés dans la recherche de contenu dans Office 365](partially-indexed-items-in-content-search.md).
