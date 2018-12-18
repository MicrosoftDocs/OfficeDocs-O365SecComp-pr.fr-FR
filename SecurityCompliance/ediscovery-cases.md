---
title: cas eDiscovery de sécurité Office 365 &amp; centre de conformité
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 8dd335ab-29d0-41c3-8dd8-9f7c7481e60c
description: Utilisez le Office 365 Security &amp; centre de conformité pour créer et gérer des affaires eDiscovery dans votre organisation. Vous pouvez affecter des membres à la casse, placez le contenu des emplacements en attente, exécutez les recherches de contenu associé avec l’incident et l’exportation les résultats de recherche. Vous pouvez également préparer des données de cas pour une analyse approfondie d’eDiscovery avancée.
ms.openlocfilehash: 8abaa0a962a63cc227a8bb1371e14218a9ee854d
ms.sourcegitcommit: 3cc069415132ccaa1ead5162df15baa2203ca2e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/18/2018
ms.locfileid: "27299360"
---
# <a name="ediscovery-cases-in-the-office-365-security-amp-compliance-center"></a>cas eDiscovery de sécurité Office 365 &amp; centre de conformité

Vous pouvez utiliser des cas eDiscovery de sécurité Office 365 &amp; centre de conformité à contrôler qui peut créer, accéder et gérer des affaires eDiscovery dans votre organisation. Si votre organisation a un abonnement à Office 365 E5, vous pouvez également utiliser des cas eDiscovery pour analyser les résultats de la recherche à l’aide d’Office 365 avancée de découverte électronique.
  
Un cas eDiscovery permet d’ajouter des membres à un cas, les types d’actions que les membres cas spécifiques peuvent effectuer, placer une suspension sur les emplacements de contenu approprié à une affaire juridique et associer plusieurs recherches de contenu à un dossier de contrôle. Vous pouvez également exporter les résultats d’une recherche de contenu qui est associé à un cas ou préparer des résultats de recherche pour l’analyse d’eDiscovery avancée. cas eDiscovery sont un excellent moyen de limiter les personnes ayant accès aux recherches de contenu et des résultats de recherche pour une affaire juridique spécifique dans votre organisation.
  
Utilisez la procédure suivante pour configurer et utiliser des cas eDiscovery dans la sécurité &amp; eDiscovery centre de conformité et options avancées.

[Étape 1 : attribuer des autorisations de découverte électronique aux membres potentiels de cas](#step-1-assign-ediscovery-permissions-to-potential-case-members)

[Étape 2 : Créer un nouveau cas](#step-2-create-a-new-case)

[Étape 3 : Ajouter des membres à un cas](#step-3-add-members-to-a-case)

[Étape 4 : Suspendre sur les emplacements de contenu](#step-4-place-content-locations-on-hold)

[Étape 5 : Créer et exécuter une recherche de contenu associé à un incident](#step-5-create-and-run-a-content-search-associated-with-a-case)

[Étape 6 : Exporter les résultats d’une recherche de contenu associé à un incident](#step-6-export-the-results-of-a-content-search-associated-with-a-case)

[Étape 7 : Préparation de résultats pour la découverte avancée de la recherche](#step-7-prepare-search-results-for-advanced-ediscovery)

[Étape 8 : Accédez à la casse d’eDiscovery avancée](#step-8-go-to-the-case-in-advanced-ediscovery)

[(Facultatif) Étape 9 : Fermer un incident](#optional-step-9-close-a-case)

[(Facultatif) Étape 10 : Rouvrir un incident fermé](#optional-step-10-re-open-a-closed-case)

[Plus d’informations](#more-information)
  
## <a name="step-1-assign-ediscovery-permissions-to-potential-case-members"></a>Étape 1 : attribuer des autorisations de découverte électronique aux membres potentiels de cas

La première étape consiste à attribuer les autorisations appropriées liés à la découverte électronique aux personnes afin que vous pouvez les ajouter à une affaire eDiscovery à l’étape 2. Vous devez être membre du groupe de rôles de gestion de l’organisation (ou attribuer le rôle de gestion du rôle) de sécurité Office 365 &amp; centre de conformité pour attribuer des autorisations de découverte électronique. La liste suivante décrit les groupes de rôles liés à la découverte de la sécurité &amp; centre de conformité. 
  
- **Relecteur** - ce groupe de rôles dispose des autorisations plus restrictives liés à la découverte électronique. Le principal objectif de ce groupe de rôles consiste à permettre aux membres de l’affichage et l’accès cas des données dans Office 365 avancée de découverte électronique. Membres de ce groupe peuvent uniquement voir et ouvrir la liste des cas dans la page de **découverte électronique** dans la sécurité &amp; centre de conformité qui ils sont membres de. Une fois que l’utilisateur accède à un cas de la sécurité et le centre de conformité, ils peuvent cliquer sur **commutateur eDiscovery avancé** pour accéder et analyser les données de cas de découverte avancée. Impossible de créer des cas, d’ajouter des membres à un cas, créer des suspensions, créer des recherches, afficher un aperçu des résultats de la recherche, exporter les résultats de recherche ou préparer des résultats pour la découverte avancée. 
    
- **Gestionnaire de découverte électronique** - membres de ce groupe de rôles peut créer et gérer des affaires eDiscovery. Ils peuvent ajouter et supprimer des membres, placer le contenu des emplacements maintenant, créent et modifier des recherches de contenu associé à un cas, exporter les résultats d’une recherche de contenu et préparer les résultats de la recherche pour l’analyse d’eDiscovery avancée. Il existe deux sous-groupes dans ce groupe de rôles. La différence entre ces sous-groupes repose sur étendue.
    
  - **gestionnaire eDiscovery** - peuvent afficher et gérer les cas eDiscovery ou qu’ils créent un membre. Si un autre gestionnaire d’eDiscovery crée un cas mais n’ajoute pas un gestionnaire de deuxième eDiscovery en tant que membre de ce cas, la deuxième eDiscovery gestionnaire n’empêchera pas afficher ou ouvrir le cas dans la page de **découverte électronique** dans la sécurité &amp; centre de conformité. eDiscovery responsables permettre également accéder à leurs cas d’eDiscovery avancé pour effectuer les tâches d’analyse. 
    
  - **eDiscovery administrateur** - peuvent effectuer toutes les tâches de gestion des dossiers qu’un gestionnaire eDiscovery peut faire. En outre, une administrateur de découverte électronique peut :
    
    - Afficher tous les cas répertoriés sur la page **Découverte électronique**. 
    
    - Gérer tous les cas dans l’organisation une fois qu’ils s’ajoutent en tant que membre de la casse.
    
    - Accédez aux données cas d’eDiscovery avancée pour tous les cas dans l’organisation.
    
    Consultez la section [More information](#more-information) pour connaître les raisons pour lesquelles vous pourriez avoir besoin d’un administrateur de découverte électronique dans votre organisation. 
    
> [!IMPORTANT]
> Si une personne n’est pas membre d’un de ces groupes de rôles liés à la découverte électronique, ou n’est pas un membre d’un groupe de rôles qui a attribué le rôle de réviseur, vous ne pouvez pas ajouter les en tant que membre d’un cas de découverte électronique. 

Pour plus d’informations sur les autorisations de découverte électronique, consultez la rubrique [attribuer des autorisations de sécurité Office 365 eDiscovery &amp; centre de conformité](assign-ediscovery-permissions.md).
  
 **Pour attribuer des autorisations de découverte électronique, procédez comme suit :**
  
1. Accédez à la page [https://protection.office.com](https://protection.office.com).
    
2. Connectez-vous à Office 365 à l'aide de votre compte scolaire ou professionnel.
    
3. Dans la sécurité &amp; centre de conformité, cliquez sur **autorisations**, puis effectuez l’une des opérations suivantes en fonction des autorisations que vous souhaitez affecter eDiscovery.
    
    - Pour affecter des autorisations de relecteur, sélectionnez le groupe de rôles **réviseur** , puis en regard de **membres**, cliquez sur **Modifier**. Cliquez sur **Sélectionner les membres**, cliquez sur **Modifier**, cliquez sur ![ajouter une icône](media/ITPro-EAC-AddIcon.gif) **Ajouter**, sélectionnez l’utilisateur que vous souhaitez ajouter au groupe de rôles réviseur, puis cliquez sur **Ajouter**.
    
    - Pour affecter des autorisations de gestionnaire de découverte électronique, sélectionnez le groupe de rôles **gestionnaire eDiscovery** , puis en regard **Gestionnaire de découverte électronique**, cliquez sur **Modifier**. Cliquez sur **Choisir eDiscovery Manager**, cliquez sur **Modifier**, cliquez sur ![ajouter une icône](media/ITPro-EAC-AddIcon.gif) ** ajouter **, sélectionnez l’utilisateur que vous souhaitez ajouter en tant qu’une gestionnaire de découverte électronique, puis cliquez sur **Ajouter**.
    
    - Pour affecter des autorisations d’administrateur de découverte électronique, sélectionnez le groupe de rôles **gestionnaire eDiscovery** , puis en regard **découverte électronique administrateur**, cliquez sur **Modifier**. Cliquez sur **Choisir eDiscovery administrateur**, cliquez sur **Modifier**, cliquez sur ![ajouter une icône](media/ITPro-EAC-AddIcon.gif) **Ajouter**, sélectionnez l’utilisateur que vous souhaitez ajouter en tant qu’une administrateur de découverte électronique, puis cliquez sur **Ajouter**.
    
4. Une fois que vous avez ajouté tous les utilisateurs, cliquez sur **terminé**, cliquez sur **Enregistrer** pour enregistrer les modifications apportées au groupe de rôles, puis cliquez sur **Fermer**.

## <a name="step-2-create-a-new-case"></a>Étape 2 : Créer un nouveau cas

L’étape suivante consiste à créer un nouveau cas eDiscovery. Vous devez être membre du groupe de rôles responsables eDiscovery pour créer des cas de découverte électronique. Comme expliqué, après avoir créé un nouveau cas de la sécurité &amp; centre de conformité, vous (et autres membres de l’incidents) seront en mesure d’accès que même casse d’eDiscovery avancée si vous êtes organisation dispose d’un abonnement à Office 365 E5.
  
1. Accédez à la page [https://protection.office.com](https://protection.office.com).
    
2. Connectez-vous à Office 365 à l'aide de votre compte scolaire ou professionnel.
    
3. Dans la sécurité &amp; centre de conformité, cliquez sur **recherche &amp; enquête** \> **eDiscovery**, puis cliquez sur ![ajouter une icône](media/ITPro-EAC-AddIcon.gif) **créer un cas**.
    
4. Dans la page **Nouveau cas** , donnez un nom à la casse, tapez une description facultative, puis cliquez sur **Enregistrer**. Notez que le nom du dossier doit être unique au sein de votre organisation.
    
    ![Créer un nouveau cas](media/7f78f83b-1525-4c77-9888-4b6bda1e148d.png)
  
    Le nouveau dossier s’affiche dans la liste des incidents dans la page de **découverte électronique** . Notez que vous pouvez pointer le curseur sur un nom de dossier pour afficher des informations sur l’incident, y compris l’état de la casse ( **actif** ou **fermé**), la description de la casse (qui a été créée à l’étape précédente), et lorsque la casse a été modifiée dernière et auteur de la modification.
    
    > [!TIP]
    > Après avoir créé un nouveau cas, vous pouvez le renommer à tout moment. Cliquez simplement sur le nom du dossier dans la page de **découverte électronique** . Dans la page Lanceur de **gérer ce cas** , modifiez le nom affiché dans la zone sous **nom**, puis enregistrer les modifications. 
  
## <a name="step-3-add-members-to-a-case"></a>Étape 3 : Ajouter des membres à un cas

Après avoir créé un nouveau cas, l’étape suivante consiste à ajouter des membres à la casse. Indiqué comme précédente, seuls les utilisateurs qui sont membres du relecteur ou groupes de rôles de gestionnaire de découverte électronique peuvent être ajoutés en tant que membres de l’incident. Notez que le responsable qui a créé le cas de découverte électronique est automatiquement ajouté en tant que membre.
  
1. Dans le Centre de sécurité &amp; conformité, cliquez sur **Recherches &amp; enquêtes** \> **eDiscovery** pour afficher la liste des cas de votre organisation. 
    
2. Cliquez sur le nom du dossier que vous souhaitez ajouter des membres.
    
    La page **gérer ce cas** les flottant s’affiche. 
    
    ![Gérer une page cas flottant](media/11f35ceb-6c98-4580-a3bc-ad688e9c7af9.png)
  
3. Sous **Gérer les membres**, cliquez sur ![ajouter une icône](media/ITPro-EAC-AddIcon.gif) **Ajouter** pour ajouter des membres à la casse. 
    
    Vous pouvez également choisir Ajouter un groupe de rôles à la casse. Sous **Gérer les groupes de rôles**, cliquez sur ![ajouter une icône](media/ITPro-EAC-AddIcon.gif) **Ajouter**.
    
    > [!NOTE]
    > Contrôle de groupes de rôles qui permettre affecter des membres à une affaire eDiscovery. Cela signifie que vous ne pouvez attribuer les groupes de rôles que vous êtes membre à un cas.
    
4. Dans la liste des groupes de personnes ou les rôles qui peuvent être ajoutés en tant que membres de l’incident, cliquez sur la case à cocher en regard des noms des groupes de personnes ou les rôles que vous souhaitez ajouter.
    
    > [!TIP]
    > Si vous disposez d’une grande liste de personnes qui peuvent ajoutés en tant que membres, utilisez la zone **Rechercher** pour rechercher une personne spécifique dans la liste. 
  
5. Une fois que vous avez sélectionné les groupes de rôle ou des personnes à ajouter en tant que membres du groupe, cliquez sur **Ajouter**.
    
    Dans **ce cas, de gérer**, cliquez sur **Enregistrer** pour enregistrer la nouvelle liste de membres de l’incidents. 
    
6. Cliquez sur **Enregistrer** pour enregistrer la nouvelle liste de membres de l’incidents. 
  
## <a name="step-4-place-content-locations-on-hold"></a>Étape 4 : Suspendre sur les emplacements de contenu

Vous pouvez utiliser un cas de découverte électronique pour créer des suspensions pour conserver le contenu qui peut-être s’appliquer à la casse. Vous pouvez placer une suspension sur OneDrive les boîtes aux lettres des personnes qui sont dépositaires dans le cas des sites de commerce. Vous pouvez également placer une suspension sur la boîte aux lettres de groupe, du site SharePoint et OneDrive pour le site de l’entreprise pour un groupe d’Office 365. De même, vous pouvez placer une suspension sur le site qui sont associés à Microsoft Teams et de boîte aux lettres. Lorsque vous placez les emplacements de contenu en attente, le contenu est conservé jusqu'à ce que vous supprimez la suspension de l’emplacement du contenu ou jusqu'à ce que vous supprimez la suspension.

> [!NOTE]
> Après avoir créé un emplacement de contenu en attente, il faut jusqu'à 24 heures pour le blocage prenne effet. 
>   
Lorsque vous créez une suspension, vous disposez des options suivantes pour définir la portée du contenu est conservé dans les emplacements de contenu spécifiés :
  
- Vous créez une attente infinie où tout le contenu est mis en attente. Vous pouvez également créer une suspension basée sur une requête où seulement le contenu qui correspond à une requête de recherche est mis en attente.
    
- Vous pouvez spécifier une plage de dates pour contenir uniquement le contenu qui a été envoyé, reçu ou créé dans cette plage de dates. Vous pouvez également maintenir tout le contenu indépendamment lorsqu’il a été envoyé, reçu ou créé.
    
> [!NOTE]
> Vous pouvez avoir un maximum de 10 000 des stratégies de blocage sur tous les cas de découverte électronique dans votre organisation. 
  
Pour créer une suspension pour un cas de découverte électronique :
  
1. Dans le Centre de sécurité &amp; conformité, cliquez sur **Recherches &amp; enquêtes** \> **eDiscovery** pour afficher la liste des cas de votre organisation. 
    
2. En regard de que vous souhaitez créer la suspension dans le cas, cliquez sur **Ouvrir** . 
    
3. Sur la page **d’accueil** pour le cas, cliquez sur l’onglet mise en **attente** . 
    
    ![Cliquez sur l’onglet blocage](media/3fef2db4-36de-4517-a34d-82f47b82d9bf.png)
  
4. Dans la page **blocage** , cliquez sur ![ajouter une icône](media/ITPro-EAC-AddIcon.gif) **créer**.
    
5. Dans la page **nom de votre suspension** , nommez la suspension. Le nom de la suspension doit être unique dans votre organisation. 
    
    ![Nommez votre attente unique](media/7e15ea63-abd1-4f14-a29c-7ecfb9571d2c.png)
  
6. (Facultatif) Dans la zone **Description** , ajoutez une description de la suspension. 
    
7. Cliquez sur **Suivant**.
    
8. Choisissez les emplacements de contenu que vous souhaitez mettre en attente. Vous pouvez placer des boîtes aux lettres, les sites et les dossiers publics en attente.
    
    ![Choisissez les emplacements de contenu à mettre sous conservation](media/a59e4265-9151-4dbf-913f-6a4ab8db06b4.png)
  
   a **aux messages électroniques Exchange** - cliquez sur **Choisir des utilisateurs, des équipes ou des groupes** , puis sur **Choisir des utilisateurs, des équipes ou des groupes** . Pour spécifier les boîtes aux lettres à mettre en attente. Utilisez la zone Rechercher pour rechercher les boîtes aux lettres utilisateur et des groupes de distribution (pour émettre un blocage sur les boîtes aux lettres des membres du groupe) pour mettre en attente. Vous pouvez également placer une suspension sur la boîte aux lettres associée pour un groupe d’Office 365 ou un Team Microsoft. Sélectionnez l’utilisateur, le groupe, la case à cocher de l’équipe, cliquez sur **Choisir**, puis cliquez sur **terminé**.
    
    > [!NOTE]
    > Lorsque vous cliquez sur **Choisir les utilisateurs, groupes ou équipes** pour spécifier des boîtes aux lettres à mettre en attente, le sélecteur de boîte aux lettres qui s’affiche est vide. Il s’agit par défaut pour améliorer les performances. Pour ajouter des personnes à cette liste, tapez un nom (un minimum de 3 caractères) dans la zone de recherche. 
  
   b. **Les Sites SharePoint** : cliquez sur **Choisir les sites** , puis cliquez sur **Choisir les sites** pour spécifier SharePoint et OneDrive pour les sites à mettre en attente. Tapez l’URL pour chaque site que vous souhaitez mettre en attente. Vous pouvez également ajouter l’URL du site SharePoint pour un groupe d’Office 365 ou un Team Microsoft. Cliquez sur **Choisir**, puis cliquez sur **terminé**.
    
    Voir la section [plus d’informations](#more-information) pour obtenir des conseils sur le fait de placer des groupes Office 365 et Microsoft Teams en attente. 
    
    > [!NOTE]
    > Dans ce cas rare que le nom d’une personne utilisateur principal (UPN) est modifié, l’URL de leur compte OneDrive système aussi être modifié pour incorporer le nouvel UPN. Dans ce cas, vous devrez modifier la suspension en ajoutant une nouvelle URL l’utilisateur de OneDrive et de supprimer l’ancien. 
  
   c. **des dossiers publics Exchange** - déplacer le bouton bascule ![contrôle bascule](media/963dfcd0-1765-4306-bcce-c3008c4406b9.png) vers la position de **toutes les** placer tous les dossiers publics dans votre organisation Exchange Online en attente. Notez que vous ne pouvez pas choisir des dossiers publics spécifiques à mettre en attente. Laissez le commutateur bascule défini sur **None** si vous ne souhaitez pas placer une suspension sur les dossiers publics.
    
9. Lorsque vous avez terminé d’ajouter des emplacements de contenu à la suspension, cliquez sur **suivant**.
    
10. Pour créer une suspension basée sur une requête avec les conditions, procédez comme suit. Sinon, cliquez simplement sur **suivant**
    
    ![Créer une suspension basée sur une requête avec des conditions](media/d587b58e-d05c-4ac0-b0fe-09019e4f1063.png)
  
    
       a dans la zone sous **mots clés**, une requête de recherche dans la zone type d’afin qu’uniquement le contenu qui répond aux critères de recherche est mis en attente. Vous pouvez spécifier des mots clés, les propriétés de message ou des propriétés de document, tels que des noms de fichiers. Vous pouvez également utiliser des requêtes plus complexes qui utilisent un opérateur booléen, tels que **AND**, **OR**ou **pas**. Si vous laissez la zone mot clé vide, puis tout le contenu situé dans les emplacements de contenu spécifiés est mis en attente.
    
    b. Cliquez sur ![ajouter une icône](media/ITPro-EAC-AddIcon.gif) **conditions ajouter** pour ajouter une ou plusieurs conditions pour limiter la requête de recherche pour la suspension. Chaque condition ajoute une clause à la requête de recherche KQL qui est créée et exécuter lorsque vous créez la suspension. Par exemple, vous pouvez spécifier une plage de dates afin que le courrier électronique ou site de documents qui ont été créés dans la plage de date sont mis en attente. Une condition est logiquement connectée à la requête de mot clé (spécifiée dans la zone mots clés) par l’opérateur **AND** . Ce qui signifie que les éléments doivent satisfaire à la fois la requête de mot clé et la condition à être mis en attente.

    Pour plus d’informations sur la création d’une requête de recherche et à l’aide de conditions, voir [conditions de recherche pour la recherche de contenu et les requêtes de mot clé](keyword-queries-and-search-conditions.md).
    
11. Après avoir configuré basée sur une requête permanente, cliquez sur **suivant**.
    
12. Passez en revue vos paramètres, puis cliquez sur **créer cette suspension**.
    
### <a name="hold-statistics"></a>Maintenez les statistiques

Après un certain temps, plus d’informations sur la mise en attente s’affiche dans le volet de détails sur la page **contient** de la suspension sélectionnée. Ces informations incluent le nombre de boîtes aux lettres maintenez sur les sites et des statistiques sur le contenu qui a été mis en attente, telles que le nombre et la taille des éléments mis en attente et de la dernière exécution de la suspension de calcul des statistiques. Contiennent statistiques vous aider à qu'identifier la quantité de contenu qui est associée à la découverte électronique est en cours. 
  
![Maintenez les statistiques](media/575cfe0a-9210-4ae4-8df8-65665d66712e.png)
  
Gardez les éléments suivants à l’esprit les statistiques d’attente :
  
- Le nombre total d’éléments en attente indique le nombre d’éléments à partir de toutes les sources de contenu qui sont mis en attente. Si vous avez créé une requête archive basée sur, cette statistique indique le nombre d’éléments qui correspondent à la requête.
    
- Le nombre d’éléments en attente inclut également les éléments non indexés trouvés dans les emplacements de contenu. Notez que si vous créez une suspension basée sur une requête, tous les éléments non indexés dans les emplacements de contenu sont mis en attente. Cela inclut les éléments non indexés qui ne correspondent pas aux critères de recherche d’une suspension basée sur une requête et non indexés qui peuvent être inclus en dehors d’une condition de plage de date. C’est différent de ce qui se produit lorsque vous exécutez une recherche de contenu, dans laquelle les éléments non indexés qui ne correspondent pas à la requête de recherche ou exclus par une condition de plage de date ne sont pas inclus dans les résultats de recherche. Pour plus d’informations sur les éléments non indexées, voir [partiellement indexé des éléments de la recherche de contenu dans Office 365](partially-indexed-items-in-content-search.md).
    
- Vous pouvez obtenir la dernière version maintenez estimer les statistiques en cliquant sur **mettre à jour les statistiques** pour réexécuter une recherche qui calcule le nombre actuel d’éléments en attente. Si nécessaire, cliquez sur **Actualiser**![icône Actualiser](media/O365-MDM-Policy-RefreshIcon.gif) dans la barre d’outils pour mettre à jour les statistiques d’attente dans le volet détails. 
    
- Normal pour le nombre d’éléments de blocage pour augmenter au fil du temps, car les utilisateurs dont la boîte aux lettres ou site sont en attente sont généralement envoi ou la réception de nouveau message électronique et la création SharePoint nouvelle et OneDrive des documents d’entreprise.
    
> [!NOTE]
> Si un site SharePoint ou un compte OneDrive est déplacé vers une région différente dans un environnement multi-localisés, les statistiques de ce site ne sont pas inclus dans les statistiques d’attente. Toutefois, le contenu du site sera toujours en attente. En outre, si un site est déplacé vers une autre zone de l’URL qui s’affiche dans la suspension ne système pas mis à jour. Vous devrez modifier la suspension et mettre à jour l’URL. 
  
## <a name="step-5-create-and-run-a-content-search-associated-with-a-case"></a>Étape 5 : Créer et exécuter une recherche de contenu associé à un incident

Une fois un cas eDiscovery est créé et les dépositaires liées à la casse sont mis en attente, vous pouvez créer et exécuter une ou plusieurs recherches de contenu qui sont associés à la casse. Contenu associé à un cas de recherche ne sont pas répertoriés dans la page de **recherche** dans la sécurité &amp; centre de conformité. Cela signifie que les recherches de contenu associés à un cas est accessible uniquement par les membres du cas qui sont également membres du groupe de rôles gestionnaire eDiscovery. 
  
1. Dans le Centre de sécurité &amp; conformité, cliquez sur **Recherches &amp; enquêtes** \> **eDiscovery** pour afficher la liste des cas de votre organisation. 
    
2. En regard de la casse que vous souhaitez créer une recherche de contenu, cliquez sur **Ouvrir** . 
    
3. Dans la page **d’accueil** pour le cas, cliquez sur l’onglet de **recherche** . 
    
    ![Onglet de recherche](media/2e15fe32-1a2e-4588-ad0b-5d96f77cece9.png)
  
4. Dans la page de **recherche** , cliquez sur ![ajouter une icône](media/ITPro-EAC-AddIcon.gif) **nouvelle recherche**. 
    
5. Sur la page **Nouvelle recherche**, vous pouvez ajouter des mots clés et des conditions pour créer la requête de recherche. 
    
    ![Nouvelle recherche](media/0e9954e7-c0ea-4e05-820b-e4b81dc5f81d.png)
  
1. Vous pouvez spécifier des mots clés, propriétés, telles qu’envoyés et reçus de dates, ou des propriétés de document, tels que des noms de fichiers ou la date de dernière modification un document de message. Vous pouvez utiliser des requêtes plus complexes qui utilisent un opérateur booléen, tels que **et**, **ou**, **pas**, **NEAR**ou **ONEAR**. Vous pouvez également rechercher des informations sensibles (comme les numéros de sécurité sociale) dans des documents ou de recherche pour les documents qui ont été partagées en externe. Si vous laissez la zone mot clé vide, tout le contenu situé dans les emplacements de contenu spécifiés sera inclus dans les résultats de recherche. 
    
2. Vous pouvez cliquer sur la case à cocher **Afficher la liste des mots clés** et le type de mots clés dans chaque ligne. Si vous procédez ainsi, les mots clés dans chaque ligne sont connectés par l’opérateur **ou** dans la requête de recherche qui est créée. 
    
    ![Liste des mots clés](media/29cceb5d-2817-4fc4-b91a-ced1c5824a17.png)
  
    Pourquoi utiliser la liste des mots clés ? Vous pouvez obtenir des statistiques indiquant le nombre d’éléments correspondent à chaque mot clé. Cela peut vous aider à identifier rapidement les mots clés qui sont le plus (et moins) efficaces. Vous pouvez également utiliser une phrase de mots clés (entourée parenthèses) dans une ligne. Pour plus d’informations sur les statistiques de recherche, voir [Afficher les statistiques de mots clés pour les résultats de recherche de contenu](view-keyword-statistics-for-content-search.md).
    
    Pour plus d’informations sur l’utilisation de la liste des mots clés, consultez [Création d’une requête de recherche](content-search.md#building-a-search-query).
    
3. Dans des **Conditions**, ajouter des conditions à une requête de recherche pour affiner la recherche et de renvoyer un jeu de résultats plus précis. Chaque condition ajoute une clause à la requête de recherche KQL qui est créée et exécutée lorsque vous démarrez la recherche. Une condition est logiquement connectée à la requête de mot clé (spécifiée dans la zone mots clés) par l’opérateur **AND** . Cela signifie que les éléments ont afin de répondre à la requête de mot clé et la condition à inclure dans les résultats. Il s’agit de comment conditions vous aider à limiter les résultats. 
    
    Pour plus d’informations sur la création d’une requête de recherche et l’utilisation de conditions, voir [Keyword queries for Content Search](keyword-queries-and-search-conditions.md).
    
6. Sous **emplacements : emplacements en attente**, choisissez les emplacements de contenu que vous souhaitez rechercher. Vous pouvez rechercher les boîtes aux lettres, les sites et les dossiers publics dans la même recherche.
    
    ![Emplacements, les emplacements en attente](media/d56398aa-0b20-4500-8e26-494eab92a99f.png)
  
  - **Tous les emplacements** - Sélectionnez cette option pour rechercher tous les emplacements de contenu dans votre organisation. Lorsque vous sélectionnez cette option, vous pouvez choisir rechercher toutes les boîtes aux lettres Exchange (qui inclut les boîtes aux lettres pour tous les groupes d’Office 365 et Microsoft Teams), tous les SharePoint et OneDrive pour les sites de l’entreprise (qui inclut les sites pour tous les groupes d’Office 365 et Microsoft Équipes) et tous les dossiers publics.
    
  - **Que tous les emplacements de blocage** - Sélectionnez cette option pour rechercher tous les emplacements de contenu qui ont été mis en attente dans le cas. Si celle-ci contient plusieurs suspensions, le contenu des emplacements toutes les suspensions portera lorsque vous sélectionnez cette option. En outre, si un emplacement de contenu a été mis en une attente basée sur une requête, uniquement les éléments qui sont en attente sont examinés lors de l’exécution de la recherche de contenu que vous créez dans cette étape. Par exemple, si un utilisateur a été mis en attente cas basée sur une requête qui conserve les éléments qui ont été envoyés ou créées avant une date spécifique, uniquement les éléments est recherchés à l’aide de critères de recherche de la recherche de contenu. Cette opération s’effectue en vous connectant la requête cas d’attente et la requête de recherche de contenu par un opérateur **AND** . Voir la section [plus d’informations](ediscovery-cases.md#moreinfo_1) à la fin de cet article pour plus d’informations sur la recherche de contenu du dossier. 
    
  - **Emplacements spécifiques** - Sélectionnez cette option pour sélectionner les boîtes aux lettres et les sites que vous souhaitez rechercher. Lorsque vous sélectionnez cette option et cliquez sur **Modifier**, une liste des emplacements s’affiche. Vous pouvez choisir de rechercher un ou tous les utilisateurs, groupes, les équipes ou sites.
    
    ![Sélectionnez emplacements spécifiques](media/97469b15-7be1-4aee-be27-f8343636152c.png)
  
    Vous pouvez également choisir de rechercher tous les dossiers publics dans votre organisation, mais si vous sélectionnez cette option et n’importe quel emplacement du contenu qui se trouve sur la recherche de blocage, toutes les requêtes d’une suspension cas basée sur une requête ne seront pas appliquées à la requête de recherche. En d’autres termes, tout le contenu d’un emplacement de la recherche est effectuée, pas seulement le contenu qui est protégé par une suspension cas basée sur une requête.
    
    Vous pouvez supprimer les emplacements de contenu cas prédéfinis ou ajouter de nouveaux. Si vous choisissez cette option, vous avez également la possibilité de rechercher tous les emplacements de contenu pour un service spécifique (par exemple, recherche toutes les boîtes aux lettres Exchange), ou vous pouvez rechercher les emplacements de contenu spécifiques d’un service. Vous pouvez également choisir s’il faut rechercher les dossiers publics dans votre organisation.
    
    Gardez à l’esprit lorsque vous ajoutez des emplacements de contenu à rechercher :
    
  - Lorsque vous cliquez sur **Choisir des utilisateurs, des équipes ou des groupes** pour spécifier des boîtes aux lettres à rechercher, le sélecteur de boîte aux lettres qui s’affiche est vide. Il s’agit par défaut pour améliorer les performances. Pour ajouter des destinataires à cette liste, cliquez sur **Choisir des utilisateurs, des équipes ou des groupes**, tapez un nom (un minimum de 3 caractères) dans la zone de recherche, activez la case à cocher en regard du nom, puis cliquez sur **Choisir**. 
    
  - Vous pouvez ajouter des boîtes aux lettres inactives, groupes d’Office 365, Teams Microsoft et des groupes de distribution à la liste des boîtes aux lettres à rechercher. Groupes de distribution dynamique ne sont pas pris en charge. Si vous ajoutez des groupes d’Office 365 ou Microsoft Teams, la boîte aux lettres de groupe ou de l’équipe est recherché ; les membres du groupe de boîtes aux lettres ne sont pas recherchés.
    
  - Pour ajouter des sites cliquez sur **Choisir les sites**et cliquez sur **Choisir des sites** à nouveau, puis tapez l’URL pour chaque site que vous souhaitez rechercher. Vous pouvez également ajouter l’URL du site SharePoint pour les groupes d’Office 365 et Microsoft Teams. 
    
7. Après avoir sélectionné les emplacements de contenu de recherche, cliquez sur **terminé** et puis cliquez sur **Enregistrer**.
    
8. Dans la page **nouvelle recherche** , cliquez sur **Enregistrer** , puis tapez un nom pour la recherche. Recherches de contenu associés à un cas doivent avoir des noms uniques au sein de votre organisation Office 365. 
    
9. Cliquez sur **Enregistrer &amp; exécuter** pour enregistrer les paramètres de recherche. 
    
10. Entrez un nom unique pour la recherche, puis cliquez sur **Enregistrer** pour lancer la recherche. 
    
    La recherche commence. Après un certain temps, une estimation des résultats de recherche s’affiche dans le volet détails. L’estimation inclut la taille totale et le nombre d’éléments qui correspond aux critères de recherche. L’estimation de la recherche inclut également le nombre d’éléments non indexés dans les emplacements de contenu qui ont été exclus. Le nombre d’éléments non indexés qui ne respectent pas les critères de recherche s’être inclus dans les statistiques de la recherche affichés dans le volet détails. Si un élément non indexés correspondances la recherche de requête (étant donné que les autres propriétés de message ou un document aux critères de recherche), il ne sont pas inclus dans l’estimation du nombre d’éléments non indexés. Si un élément non indexée est exclu par les critères de recherche, il n’est également inclus dans l’estimation des éléments non indexés.
    
    Une fois que la recherche est terminée, vous pouvez afficher les résultats de recherche. Si nécessaire, cliquez sur **Actualiser**![icône Actualiser](media/O365-MDM-Policy-RefreshIcon.gif) pour mettre à jour les informations contenues dans le volet de détails. 
    
## <a name="step-6-export-the-results-of-a-content-search-associated-with-a-case"></a>Étape 6 : Exporter les résultats d’une recherche de contenu associé à un incident

Après qu’une recherche est exécutée correctement, vous pouvez exporter les résultats de recherche. Lorsque vous exportez des résultats de la recherche, les éléments de boîte aux lettres sont téléchargés dans des fichiers PST ou sous forme de messages individuels. Lorsque vous exportez le contenu à partir de SharePoint et OneDrive pour les sites, les copies des documents Office natifs et d’autres documents sont exportées. Un fichier manifeste (au format XML) qui contient des informations sur chaque résultat de recherche est également exporté.
  
Vous pouvez exporter les résultats d’un [Exporter les résultats d’une recherche unique associé à un incident](ediscovery-cases.md#singlesearch_1) , ou vous pouvez exporter les résultats [d’Exporter les résultats de plusieurs recherches associées à un cas](ediscovery-cases.md#multiplesearches_1).
  
### <a name="export-the-results-of-a-single-search-associated-with-a-case"></a>Exporter les résultats d’une recherche unique associé à un incident

1. Dans le Centre de sécurité &amp; conformité, cliquez sur **Recherches &amp; enquêtes** \> **eDiscovery** pour afficher la liste des cas de votre organisation. 
    
2. En regard de la casse que vous souhaitez exporter la recherche à partir de, cliquez sur **Ouvrir** . 
    
3. Dans la page **d’accueil** pour le cas, cliquez sur **Rechercher**.
    
4. Dans la liste des recherches dans le cas, cliquez sur la recherche que vous souhaitez exporter les résultats de la recherche, cliquez sur ![icône de résultats de recherche d’exportation](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **plus**, puis sélectionnez **Exporter les résultats** à partir de la liste déroulante. 
    
    La page **Exporter les résultats** s’affiche. 
    
    ![Exporter la page de résultats](media/ab0bb46d-310b-4374-8644-717146df6676.png)
  
    Le flux de travail pour exporter les résultats d’une recherche de contenu associée à un cas qui est identique à exporter les résultats de recherche pour une recherche dans la page de **recherche de contenu** . Pour des instructions détaillées, consultez la rubrique [résultats de la recherche de contenu à exporter à partir de la sécurité du Office 365 &amp; centre de conformité](export-search-results.md).
    
    > [!NOTE]
    > Lorsque vous exportez des résultats de la recherche, vous avez la possibilité d’activer la déduplication, afin qu’une seule copie d’un message électronique est exportée, même si plusieurs instances du même message ont été trouvées dans les boîtes aux lettres qui ont été exclus. Pour plus d’informations sur la déduplication et comment les doublons sont identifiés, voir [la déduplication dans les résultats de recherche de découverte électronique](de-duplication-in-ediscovery-search-results.md). 
  
5. Cliquez sur l’onglet **Exporter** pour afficher la liste des tâches d’exportation qui existent pour ce cas. 
    
    ![Onglet Exporter](media/1b84c45e-4ec9-4ecd-9e07-eaf8fc4cc307.png)
  
    Vous devrez peut-être cliquer sur **Actualiser**![icône Actualiser](media/O365-MDM-Policy-RefreshIcon.gif) pour mettre à jour la liste des tâches d’exportation de sorte qu’il affiche la tâche d’exportation que vous venez de créer. Notez que travaux d’exportation ont le même nom que le contenu correspondant de recherche avec **_Export** ajouté à la fin du nom de la recherche. 
    
6. Cliquez sur la tâche d’exportation que vous venez de créer pour afficher les informations d’état dans le volet détails. Ces informations incluent le pourcentage des éléments qui ont été transférés vers une zone de stockage Azure dans le nuage de Microsoft.
    
    Une fois que tous les éléments ont été transférés, cliquez sur **télécharger les résultats** pour télécharger les résultats de recherche sur votre ordinateur local. Pour plus d’informations, voir l’étape 2 de [des résultats de recherche de contenu à exporter à partir de la sécurité du Office 365 &amp; centre de conformité](export-search-results.md)
    
### <a name="export-the-results-of-multiple-searches-associated-with-a-case"></a>Exporter les résultats de plusieurs recherches associés à un incident

Comme alternative à exporter les résultats d’une recherche de contenu unique associé à un cas, vous pouvez exporter les résultats de plusieurs recherches à partir de la même casse dans une exportation unique. Exporter les résultats de plusieurs recherches est plus rapide et plus facile que d’exporter les résultats de l’un recherche à la fois.
  
> [!NOTE]
> Vous ne pouvez pas exporter les résultats des recherches de plusieurs si une de ces recherches a été configurée pour rechercher tout le contenu. exporter uniquement les résultats des recherches multiples pour les recherches associées à une affaire eDiscovery. Vous ne pouvez pas exporter les résultats de plusieurs recherches répertoriées dans la page de **recherche de contenu** dans la sécurité &amp; centre de conformité. 
  
1. Dans le Centre de sécurité &amp; conformité, cliquez sur **Recherches &amp; enquêtes** \> **eDiscovery** pour afficher la liste des cas de votre organisation. 
    
2. En regard de la casse que vous souhaitez exporter les résultats de la recherche, cliquez sur **Ouvrir** . 
    
3. Dans la page **d’accueil** pour le cas, cliquez sur **Rechercher**.
    
4. Dans la liste des recherches dans le cas, sélectionnez au moins deux recherches que vous souhaitez exporter les résultats de recherche.
    
    > [!NOTE]
    > Pour sélectionner plusieurs recherches, appuyez sur Ctrl lorsque vous cliquez sur chaque recherche. Ou vous pouvez sélectionner plusieurs recherches adjacents en cliquant sur la première recherche, maintenez enfoncée la touche MAJ enfoncée, puis en cliquant sur la dernière recherche. 
  
5. Une fois que vous sélectionnez les recherches, la page **actions en bloc** apparaît. 
    
    ![Dans la page Actions en bloc, cliquez sur Exporter les résultats](media/f34e3707-a9c1-494f-91a4-da1165aa730a.png)
  
    
6. Cliquez sur ![icône de résultats de recherche d’exportation](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **Exporter les résultats**.

7. Dans la page **Exporter les résultats** , nommez l’exportation unique, sélectionnez les options de sortie et choisissez la façon dont le contenu doit être exporté. Cliquez sur **Exporter**.
    
    Le flux de travail pour exporter les résultats de plusieurs recherches de contenu associés à un cas est identique à exporter les résultats de recherche pour une seule recherche. Pour des instructions détaillées, consultez la rubrique [résultats de la recherche de contenu à exporter à partir de la sécurité du Office 365 &amp; centre de conformité](export-search-results.md).
    
    > [!NOTE]
    > Lorsque vous exportez des résultats de recherche à partir de plusieurs recherches associées à un cas, vous avez également la possibilité d’activer la déduplication, afin qu’une seule copie d’un message électronique est exportée, même si plusieurs instances du même message ont été trouvés dans le boîtes aux lettres qui ont été recherchées dans une ou plusieurs des recherches. Pour plus d’informations sur la déduplication et comment les doublons sont identifiés, voir [la déduplication dans les résultats de recherche de découverte électronique](de-duplication-in-ediscovery-search-results.md). 
  
8. Après le démarrage de l’exportation, cliquez sur l’onglet **Exporter** pour afficher la liste des tâches d’exportation pour ce cas. 
    
    ![Onglet Exporter, plusieurs recherches](media/b9505e1b-559f-4a8c-96b3-a3f734753926.png)
  
    Vous devrez peut-être cliquer sur **Actualiser** ![icône Actualiser](media/O365-MDM-Policy-RefreshIcon.gif) pour mettre à jour la liste des tâches d’exportation pour afficher la tâche d’exportation que vous venez de créer. Notez que les recherches qui ont été inclus dans la tâche d’exportation sont répertoriés dans la colonne de **recherche** . 
    
8. Cliquez sur la tâche d’exportation que vous venez de créer pour afficher les informations d’état dans le volet détails. Ces informations incluent le pourcentage des éléments qui ont été transférés vers une zone de stockage Azure dans le nuage de Microsoft.
    
9. Une fois que tous les éléments ont été transférés, cliquez sur **télécharger les résultats** pour télécharger les résultats de recherche sur votre ordinateur local. Pour plus d’informations, voir l’étape 2 de [résultats de la recherche de l’exportation à partir de la sécurité de 365 Office &amp; centre de conformité](export-search-results.md)
    
#### <a name="more-information-about-exporting-the-results-of-multiple-searches"></a>Plus d’informations sur Exporter les résultats des recherches multiples

- Lorsque vous exportez les résultats de plusieurs recherches, les requêtes de recherche à partir de toutes les recherches sont combinés à l’aide des opérateurs **ou** , puis la recherche combinées est démarré. Les résultats de la recherche combinée estimées sont affichés dans le volet de détails de la tâche d’exportation sélectionné. Les résultats de recherche sont ensuite transférées vers la zone de stockage Azure dans le nuage de Microsoft. L’état du transfert est également affiché dans le volet détails. Comme indiqué précédemment, une fois que tous les résultats de recherche ont été transférés, vous pouvez les télécharger sur votre ordinateur local. 
    
- Le nombre maximal de mots clés dans les requêtes de recherche pour toutes les recherches que vous souhaitez exporter est de 500. (il s’agit de la même limite pour une recherche de contenu unique). C’est parce que la tâche d’exportation s’associe à toutes les requêtes de recherche à l’aide de l’opérateur **OR** . Si vous dépassez cette limite, une erreur sera renvoyée. Dans ce cas, vous devrez exporter les résultats des recherches moins ou simplifier les requêtes de recherche de la recherche que vous souhaitez exporter. 
    
- Les résultats de recherche qui sont exportés sont organisés par l’élément a été trouvé dans la source de contenu. Par conséquent, qu'une source de contenu dans les résultats de l’exportation peut avoir des éléments renvoyés par les différentes recherches. Par exemple, si vous décidez d’exporter des messages électroniques dans un fichier PST pour chaque boîte aux lettres, le fichier PST peut-être donner des résultats de plusieurs recherches.
    
- Si le même élément de messagerie ou le document à partir de l’emplacement du contenu même est retournée par plusieurs des recherches que vous exportez, qu’une seule copie de l’élément doit être exportée.
    
- Vous ne pouvez pas modifier une exportation pour plusieurs recherches après sa création. Par exemple, vous ne pouvez pas ajouter ou supprimer des recherches à partir de l’exportation. Vous devrez créer une nouvelle tâche d’exportation pour modifier les résultats de la recherche sont exportées. Après la création d’une tâche d’exportation, vous seulement pourrez télécharger les résultats sur un ordinateur, redémarrez l’exportation ou supprimer la tâche d’exportation.
    
- Si vous redémarrez l’exportation, toute modification apportée aux requêtes des recherches qui constituent la tâche d’exportation n’affecte pas les résultats de recherche qui seront récupérées. Lorsque vous redémarrez une exportation, la même tâche de requête de recherche combinées qui a été exécutée lors de la création de la tâche d’exportation sera exécutée à nouveau.
    
- Si vous redémarrez une exportation dans la page **exportation** dans un cas eDiscovery, les résultats de recherche qui sont transférés vers la zone de stockage Azure remplacera les résultats de la précédentes ; les résultats précédents, il y avait transféré n’est pas disponible pour être téléchargé. 
    
- Préparer les résultats des recherches multiples pour l’analyse d’eDiscovery avancée n’est pas disponible. Vous pouvez uniquement préparer les résultats d’une recherche unique pour l’analyse d’eDiscovery avancée.

## <a name="step-7-prepare-search-results-for-advanced-ediscovery"></a>Étape 7 : Préparation de résultats pour la découverte avancée de la recherche

Si votre organisation a un abonnement à Office 365 E5, vous pouvez préparer les résultats de recherches de contenu associé à un cas pour l’analyse d’eDiscovery avancée. Après avoir préparé les résultats de la recherche, vous pouvez passer à la découverte électronique avancée (voir [étape 8 : accédez à la casse d’eDiscovery avancée](#step-8-go-to-the-case-in-advanced-ediscovery)) et traitent les données de résultats de recherche pour une analyse approfondie d’eDiscovery avancée.
  
Lorsque vous préparez des résultats de la recherche avancée eDiscovery, les fonctionnalités de reconnaissance optique de caractères (OCR) extrait automatiquement le texte à partir d’images. Reconnaissance optique de caractères est pris en charge pour les fichiers à part, pièces jointes et des images incorporées. Cela vous permet d’appliquer les fonctionnalités d’analyse texte d’eDiscovery avancée (près de doublons, messagerie threading, thèmes et codage prédictive) à du texte dans des fichiers image.
  
> [!NOTE]
> Pour analyser les données d’un utilisateur à l’aide de la découverte électronique avancée, l’utilisateur (le dépositaire des données) doit être affecté à une licence Office 365 E5. Autrement, les utilisateurs possédant une licence Office 365 E1 ou E3 peuvent être affectés à une licence autonome de découverte avancée. Les administrateurs et des agents de conformité qui sont affectées à des cas et utilisent eDiscovery avancée pour analyser des données inutile d’une licence E5. 
  
1. Dans le Centre de sécurité &amp; conformité, cliquez sur **Recherches &amp; enquêtes** \> **eDiscovery** pour afficher la liste des cas de votre organisation. 
    
2. En regard de la casse que vous souhaitez préparer des résultats de recherche pour l’analyse d’eDiscovery avancée, cliquez sur **Ouvrir** . 
    
3. Dans la page **d’accueil** pour le cas, cliquez sur **Rechercher**, puis sélectionnez la recherche.
    
4. Dans le volet détails, cliquez sur ![icône de résultats de recherche d’exportation](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **plus**, puis cliquez sur **préparer pour la découverte avancée**.
    
    ![Préparer vos résultats eDiscovery avancées](media/b6548ff0-a6e9-42b1-9ae4-5c15146f5690.png)
  
5. Dans la page **préparer pour la découverte électronique avancée** , choisissez préparer une des options suivantes : 
    
    - Tous les éléments, à l’exception de ceux dont le format non reconnu, sont chiffrées ou n’ont pas été indexés pour d’autres raisons.
    
    - Tous les éléments, y compris ceux qui ont reconnu format, sont chiffrées ou n’ont pas été indexés pour d’autres raisons.
    
    - Uniquement les éléments qui ont un format non reconnaissable, sont chiffrées ou n’ont pas été indexés pour d’autres raisons.
    
6. (Facultatif) Cliquez sur la case à cocher **inclure les versions des fichiers SharePoint** . 
    
7. Cliquez sur **Préparer**.
    
    Les résultats de recherche sont préparés pour l’analyse de découverte électronique avancée.
    
8. Cliquez sur **Fermer** pour fermer le volet d’informations. 
    
## <a name="step-8-go-to-the-case-in-advanced-ediscovery"></a>Étape 8 : Accédez à la casse d’eDiscovery avancée

Après avoir créé un cas de la sécurité &amp; centre de conformité, vous pouvez accéder à la même casse d’eDiscovery avancée.
  
Pour accéder à un cas dans Advanced eDiscovery :
  
1. Dans le Centre de sécurité &amp; conformité, cliquez sur **Recherches &amp; enquêtes** \> **eDiscovery** pour afficher la liste des cas de votre organisation. 
    
2. En regard de la casse que vous souhaitez atteindre dans eDiscovery avancée, cliquez sur **Ouvrir** . 
    
3. Dans la page **d’accueil** pour le cas, cliquez sur **Avancé eDiscovery**.
    
    ![Sélectionnez le commutateur eDiscovery avancées](media/d7e31558-e79c-4782-b841-2b735568a576.png)
  
    La barre de progression **se connectant à la découverte électronique avancé** s’affiche. Lorsque vous êtes connecté à la découverte électronique avancée, une liste de conteneurs s’affiche dans la page. 
    
    ![Barre de progression eDiscorvery avancé](media/4a84273d-765b-44b8-9006-c20e810ea393.png)
  
    Ces conteneurs représentent les résultats de recherche que vous avez préparé pour l’analyse d’eDiscovery avancé à l’étape 7. Notez que le nom du conteneur a le même nom que la recherche de contenu dans le cas de la sécurité &amp; centre de conformité. Les conteneurs dans la liste sont ceux que vous avez préparé. Si un autre utilisateur préparé les résultats de la recherche avancée eDiscovery, les conteneurs correspondants ne sont pas inclus dans la liste.
    
4. Pour charger les données de résultats de recherche à partir d’un conteneur pour le cas d’eDiscovery avancée, sélectionnez un conteneur et cliquez sur **le processus**.
    
    Pour plus d’informations sur la façon de conteneurs de processus, voir [exécuter le module de processus et charger des données dans Office 365 avancée de découverte électronique](run-the-process-module-and-load-data-in-advanced-ediscovery.md).
    
> [!TIP]
> Cliquez sur le **commutateur à la découverte électronique** pour revenir à la casse de la sécurité &amp; centre de conformité. 
  
## <a name="optional-step-9-close-a-case"></a>(Facultatif) Étape 9 : Fermer un incident

Lorsque le jugement pris en charge par un cas eDiscovery ou juridique est terminée, vous pouvez fermer le cas. Voici ce qui se produit lorsque vous fermez un incident :
  
- Si le cas contient les emplacements de contenu en attente, ces suspensions seront désactivées. Cela peut provoquer de contenu définitivement supprimé ou purgés, par l’utilisateur ou par un processus automatisé, comme une stratégie de suppression.
    
- La fermeture d’un cas uniquement désactive la suspension qui sont associée à ce cas. Si les autres blocages sont place sur un emplacement de contenu (par exemple, un pour litige suspension. une stratégie de conservation ou un blocage à partir d’un cas eDiscovery différents) ces suspensions seront toujours conservées.
    
- Le cas est toujours répertorié dans la page de découverte électronique dans la sécurité &amp; centre de conformité. Plus d’informations, suspensions, recherches, les membres d’un incident fermé sont conservés.
    
- Vous pouvez modifier un incident après sa fermeture. Par exemple, vous pouvez ajouter ou supprimer des membres, créer des recherches, exporter les résultats de recherche et préparer le résultat de recherche pour l’analyse d’eDiscovery avancée. La principale différence entre les cas actives et de fermeture est que les suspensions sont désactivées lors de la fermeture d’un incident.
    
Pour fermer un cas :
  
1. Dans le Centre de sécurité &amp; conformité, cliquez sur **Recherches &amp; enquêtes** \> **eDiscovery** pour afficher la liste des cas de votre organisation. 
    
2. Cliquez sur le nom du dossier que vous souhaitez fermer.
    
    La page **gérer ce cas** les flottant s’affiche. 
    
3. Sous **gérer le statut de dossier**, cliquez sur ![supprimer le bouton Aperçu](media/b6512677-5e7b-42b0-a8a3-3be1d7fa23ee.gif) **Fermer le cas**.
    
    Un avertissement s’affiche indiquant que la suspension associée au cas sera désactivée.
    
4. Cliquez sur **Oui** pour fermer le cas. 
    
    L’état sur la page **gérer ce cas** les flottant est modifiée **actif** à **la fermeture**.
    
5. Fermez la page **gérer ce cas** . 
    
6. Dans la page de la **découverte électronique** , cliquez sur ![icône Actualiser](media/O365-MDM-Policy-RefreshIcon.gif) **Actualiser** pour mettre à jour le statut de l’incident fermé. Il peut prendre jusqu'à 60 minutes pour terminer le processus de fermeture. 
    
    Lorsque le processus est terminé, le statut de l’incident est modifié **fermé** dans la page de **découverte électronique** . Cliquez sur le nom de la casse pour afficher la page **gérer ce cas** flottant, qui contient des informations sur la casse a été fermée et qui a été fermé. 
     
## <a name="optional-step-10-re-open-a-closed-case"></a>(Facultatif) Étape 10 : Rouvrir un incident fermé

Lorsque vous rouvrez un cas, les suspensions qui étaient en place lors de la fermeture de la casse ne sont pas automatiquement rétablies. Le cas est rouverte, vous devrez accéder à la page **blocage** et activer la suspension précédente. Pour activer une suspension, sélectionnez-le et cliquez sur **Activer** dans le volet détails. 
  
1. Dans le Centre de sécurité &amp; conformité, cliquez sur **Recherches &amp; enquêtes** \> **eDiscovery** pour afficher la liste des cas de votre organisation. 
    
2. Cliquez sur le nom du dossier que vous souhaitez rouvrir.
    
    La page **gérer ce cas** les flottant s’affiche. 
    
3. Sous **gérer le statut de l’incident**, cliquez sur **rouvrir le cas**.
    
    Un avertissement s’affiche indiquant que les blocages qui ont été associés à la casse lors de sa fermeture ne sont pas être activés automatiquement.
    
4. Cliquez sur **Oui** pour rouvrir le cas. 
    
    L’état dans la page Lanceur de **gérer ce cas** est modifié de **fermé** à **actif**.
    
5. Fermez la page **gérer ce cas** . 
    
6. Dans la page de la **découverte électronique** , cliquez sur ![icône Actualiser](media/O365-MDM-Policy-RefreshIcon.gif) **Actualiser** pour mettre à jour le statut de l’incident rouvert. Il peut prendre jusqu'à 60 minutes pour l’exécution du processus réouverture. 
    
    Lorsque le processus est terminé, le statut de l’incident est modifié **actif** dans la page de **découverte électronique** . 
  
## <a name="more-information"></a>More information

- **y a-t-il des limites pour les cas eDiscovery ou suspensions associées à une affaire eDiscovery ?** Le tableau suivant répertorie les limites pour les cas eDiscovery et blocages cas.
    
  |**Description de la limite**|**Limite**|
  |:-----|:-----|
  |Nombre maximal de cas d’une organisation  <br/> |Sans limite  <br/> |
  |Nombre maximal de cas conserve d’une organisation  <br/> |10 000  <br/> |
  |Nombre maximal de boîtes aux lettres dans un dossier attente  <br/> |1,000  <br/> |
  |Nombre maximal de SharePoint et OneDrive pour les sites d’entreprise dans un seul cas blocage  <br/> |100  <br/> |
   
- **Qu’en est-il des cas qui ont été créés dans la page Gestion des dossiers d’eDiscovery avancée ?** Vous pouvez accéder à une liste des anciens cas eDiscovery avancé en cliquant sur le lien en bas dans la page de **découverte électronique** dans la sécurité &amp; centre de conformité. Toutefois, pour effectuer le travail dans un cas antérieur, vous devez contacter le support technique de Office 365 et demander que le cas être déplacés vers un nouveau cas eDiscovery dans la sécurité &amp; centre de conformité. 
    
- **Pourquoi créer une administrateur de découverte électronique ?** Comme expliqué, une découverte électronique que l’administrateur est membre du groupe de rôles gestionnaire eDiscovery qui peut afficher et accéder à tous les cas de découverte électronique dans votre organisation. Cette capacité à accéder à tous les cas eDiscovery a deux fonctions importantes :
    
  - Si une personne qui est le seul membre d’un cas eDiscovery quitte l’organisation, personne (y compris les membres du groupe de rôles de gestion de l’organisation ou un autre membre du groupe de rôles de gestionnaire de découverte électronique) peuvent accéder à ce cas de découverte électronique car ils ne sont pas un membre d’un cas. Dans ce cas, il n’y aura aucun moyen d’accéder aux données dans le cas. Mais comme une administrateur de découverte électronique peut accéder à tous les cas de découverte électronique dans l’organisation, ils peuvent afficher le cas dans la sécurité &amp; centre de conformité et l’ajouter eux-mêmes ou un autre gestionnaire de découverte électronique en tant que membre de la casse.
    
  - Car une administrateur de découverte électronique peut afficher et accéder à tous les cas eDiscovery, qu’ils puissent d’audit et surveiller tous les cas et les recherches de contenu associée. Cela peut aider à empêcher toute utilisation incorrecte de recherches de contenu ou cas eDiscovery. Et car eDiscovery, les administrateurs permettre accéder à des informations sensibles dans les résultats d’une recherche de contenu, vous devez limiter le nombre de personnes qui sont des administrateurs de découverte électronique.
    
    Enfin, précédente comme expliqué, administrateurs de découverte électronique dans la sécurité &amp; centre de conformité sont automatiquement ajoutés en tant qu’administrateurs d’eDiscovery avancée. Par conséquent, une personne qui est une administrateur de découverte électronique peut effectuer des tâches administratives d’eDiscovery avancée, telles que la configuration des utilisateurs, des cas de création et ajout de données à des cas.
    
- **Quelles sont les conditions de licence pour placer les emplacements de contenu en attente ?** En règle générale, les organisations nécessitent un abonnement à Office 365 E3 ou supérieur pour mettre les emplacements de contenu en attente. Pour mettre des boîtes aux lettres en attente, une licence Exchange Online Plan 2 est requise pour la boîte aux lettres que vous souhaitez mettre en attente.
    
- **Else doivent savoir à propos de la recherche dans tout le contenu à l’étape 5 ?** Comme expliqué précédemment, vous pouvez rechercher les emplacements de contenu qui ont été mis en attente dans le cas. Lorsque vous effectuez cette opération, uniquement le contenu qui correspond aux critères de suspension est recherche. S’il n’existe aucun critère d’attente, tout le contenu est recherché. Si le contenu est sur une requête bloquer, uniquement le contenu que correspond à la fois doit contenir les critères (à partir de la suspension placés à l’étape 4) et les critères de recherche (à partir de la recherche à l’étape 5) est renvoyée avec les résultats de recherche.
    
    Voici quelques autres éléments à prendre en compte lors de la recherche tout le contenu :
    
  - Si un emplacement de contenu fait partie de plusieurs suspensions dans le cas de même, les requêtes de blocage sont combinées par un opérateur **ou** lors de la recherche de cet emplacement de contenu à l’aide de l’option tous les cas le contenu. De même, si un emplacement de contenu fait partie de deux différentes contient, où une est basée sur une requête et l’autre est une attente infinie (où tout le contenu est mis en attente), tout le contenu sera recherche en raison de la suspension infinie. 
    
  - Si une recherche de contenu est un incident et vous avez configuré de manière à tout le contenu de recherche et que vous modifiez une suspension (par ajout ou suppression d’un emplacement de contenu ou modifier la requête de suspension), la configuration de recherche est mis à jour avec ces modifications. Toutefois, vous devez réexécuter la recherche après modification de la suspension pour mettre à jour les résultats de recherche.
    
  - Si plusieurs suspensions cas sont placées dans un emplacement de contenu dans un cas eDiscovery et que vous sélectionnez Rechercher tout le contenu, le nombre maximal de mots clés pour cette requête de recherche est de 500. C’est parce que la recherche de contenu combine toutes les suspensions requête à l’aide de l’opérateur **OR** . S’il existe que plus de 500 mots clés dans le combiné maintenez les requêtes et la requête de recherche de contenu, puis tout le contenu de la boîte aux lettres est recherché, conserve non seulement que le contenu qui correspond à l’un des cas basée sur une requête. 
    
  - Si une suspension cas a le statut **d’activation**, vous pouvez toujours rechercher les emplacements de contenu cas alors que le blocage est activé.
    
  - Comme indiqué plus haut, si une recherche est configurée pour rechercher tout le contenu, vous ne pouvez pas inclure que la recherche si vous souhaitez exporter les résultats de plusieurs recherches. Si une recherche est configurée pour tout le contenu de recherche, vous devrez exporter les résultats de recherche unique.
    
- **Si une boîte aux lettres, un site SharePoint ou un compte OneDrive en attente est déplacé vers une région différente dans un environnement multi-localisés, la suspension toujours s’appliquera ?** Dans tous les cas, le contenu dans une boîte aux lettres, un site ou un compte de OneDrive est toujours conservé. Toutefois, les statistiques de suspension n’est plus incluent les éléments à partir d’un emplacement de contenu qui a été déplacée dans une région différente. Pour inclure les statistiques de suspension pour un emplacement de contenu est migré, vous devrez modifier la suspension et mettre à jour l’URL (ou l’adresse SMTP d’une boîte aux lettres) afin que l’emplacement du contenu est à nouveau inclus dans les statistiques d’attente. 
    
- **Est-il placer un blocage sur les groupes d’Office 365 et Microsoft Teams ?** Teams Microsoft reposent sur les groupes d’Office 365. Par conséquent, leur mise en attente dans un cas eDiscovery est très similaire. Gardez les éléments suivants à l’esprit lorsque le placement des groupes Office 365 et Microsoft Teams sur permanente. 
    
  - Pour placer le contenu stocké dans des groupes d’Office 365 et Microsoft Teams en attente, vous devez spécifier la boîte aux lettres et du site SharePoint associé à un groupe ou d’équipe.
    
  - Exécutez l’applet de commande **Get-UnifiedGroup** dans Exchange Online pour afficher les propriétés d’un groupe dans Office 365 ou un Microsoft Team. Il s’agit d’un excellent moyen d’obtenir l’URL du site qui est associé à un groupe d’Office 365 ou un Team Microsoft. Par exemple, la commande suivante affiche les propriétés sélectionnées d’un groupe d’Office 365 nommé équipe de direction Senior : 
    
     ```
    Get-UnifiedGroup "Senior Leadership Team" | FL DisplayName,Alias,PrimarySmtpAddress,SharePointSiteUrl

     DisplayName            : Senior Leadership Team
     Alias                  : seniorleadershipteam
     PrimarySmtpAddress     : seniorleadershipteam@contoso.onmicrosoft.com
     SharePointSiteUrl      : https://contoso.sharepoint.com/sites/seniorleadershipteam
    ```

    > [!NOTE]
    > Pour exécuter l’applet de commande **Get-UnifiedGroup** , vous devez être affecté le rôle destinataires en affichage seul dans Exchange Online ou être membre d’un groupe de rôles qui a affecté le rôle destinataires en affichage seul. 
  
  - Lorsque la recherche de boîte aux lettres d’un utilisateur, groupe d’Office 365, ni Microsoft Team dont l’utilisateur est un membre de ne sont pas recherché. De même, lorsque vous placez un groupe d’Office 365 ou Microsoft Team maintenez, uniquement les boîtes aux lettres de groupe et le site de groupe sont mis en attente ; les boîtes aux lettres et OneDrive pour les sites d’entreprise des membres du groupe ne sont pas mis en attente, sauf si vous les ajoutez à la suspension. Par conséquent, si vous la nécessité de placer un groupe dans Office 365 ou un Microsoft Team en attente pour des raisons légales, pensez à utiliser les boîtes aux lettres et OneDrive pour les sites de l’entreprise pour les membres d’équipe et de groupe sur le même en attente.
    
  - Pour obtenir une liste des membres d’un groupe dans Office 365 Team Microsoft, vous pouvez afficher les propriétés de le **accueil \> groupes** page dans le centre d’administration d’Office 365. Vous pouvez également exécuter la commande suivante dans Exchange Online PowerShell : 
    
      ```
      Get-UnifiedGroupLinks <group or team name> -LinkType Members | FL DisplayName,PrimarySmtpAddress 
      ```

    > [!NOTE]
    > Pour exécuter l’applet de commande **Get-UnifiedGroupLinks** , vous devez être affecté le rôle destinataires en affichage seul dans Exchange Online ou être membre d’un groupe de rôles qui a affecté le rôle destinataires en affichage seul. 
  
  - Conversations qui font partie d’un canal Teams Microsoft sont stockées dans la boîte aux lettres qui est associé à la Team Microsoft. De même, les fichiers qui partagent des membres de l’équipe dans un canal sont stockés sur le site SharePoint de l’équipe. Par conséquent, vous devez placer la boîte aux lettres Microsoft Team maintenez le site SharePoint sur Conserver les conversations et les fichiers dans un canal.
    
    Vous pouvez également les conversations qui font partie de la liste de conversation dans Microsoft Teams sont stockées dans la boîte aux lettres de l’utilisateur qui participent à la conversation. Et fichiers utilisateur partage conversation sont stockés dans le site de l’entreprise de l’utilisateur qui partage le fichier OneDrive. Par conséquent, vous devez placer les boîtes aux lettres des utilisateurs individuels et OneDrive sur des sites de Commerce maintenez à conserver les conversations et les fichiers dans la liste de conversation. C’est pourquoi il est préférable de placer un blocage sur les boîtes aux lettres des membres d’un Team Microsoft en plus de placer la boîte aux lettres d’équipe (et site) en attente.
    
    > [!IMPORTANT]
    > Les utilisateurs de participer à des conversations qui font partie de la liste de conversation dans Microsoft Teams doivent avoir une boîte aux lettres Exchange Online (en nuage) afin de conserver des conversations lorsque la boîte aux lettres est placé sur un blocage eDiscovery. C’est parce que les conversations qui font partie de la liste de conversation sont stockées dans les boîtes aux lettres en nuage de participants à la conversation. Si un participant de conversation ne possède une boîte aux lettres Exchange Online, vous ne pourrez pas conserver des conversations. Par exemple, dans un déploiement Exchange hybride, les utilisateurs avec une boîte aux lettres locale peuvent être en mesure de participer à des conversations qui font partie de la liste de conversation dans Microsoft Teams. Toutefois dans ce cas, le contenu de ces conversation ne peuvent pas être conservé car les utilisateurs ne disposent pas les boîtes aux lettres en nuage. 
  
  - Chaque canal Microsoft Team ou de l’équipe contient un Wiki de prise de notes et de collaboration. Le contenu Wiki est automatiquement enregistré dans un fichier au format .mht. Ce fichier est stocké dans la bibliothèque de documents équipes Wiki données sur le site SharePoint de l’équipe. Vous pouvez placer le contenu dans le Wiki en attente en plaçant le site SharePoint de l’équipe en attente.
    
    > [!NOTE]
    > La capacité à conserver le contenu Wiki pour un canal Microsoft Team ou de l’équipe (lorsque vous placez le site SharePoint de l’équipe en attente) a été publiée le 22 juin 2017. Si un site d’équipe maintenez, le Wiki contenu sera conservé commençant à cette date. Toutefois, si un site d’équipe est en attente et le contenu Wiki a été supprimé avant le 22 juin 2017, le contenu Wiki n’a été pas conservé. 
  
- **Comment trouver les URL de OneDrive pour les sites de l’entreprise ?** Pour collecter une liste de toutes les URL de OneDrive pour les sites d’entreprise dans votre organisation, vous pouvez les ajouter à une suspension ou de recherche associé à un cas eDiscovery, voir [créer une liste de tous les emplacements de OneDrive dans votre organisation](https://support.office.com/article/8e200cb2-c768-49cb-88ec-53493e8ad80a). Ce script dans cet article crée un fichier texte qui contient une liste de tous les sites OneDrive. Pour exécuter ce script, vous devrez installer et utiliser SharePoint Online Management Shell. Veillez à ajouter l’URL de domaine du site Mon site dans votre organisation à chaque site OneDrive que vous souhaitez rechercher. Il s’agit du domaine qui contient votre OneDrive ; par exemple, `https://contoso-my.sharepoint.com`. Voici un exemple d’URL pour le site de OneDrive d’un utilisateur : `https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft.com`.
