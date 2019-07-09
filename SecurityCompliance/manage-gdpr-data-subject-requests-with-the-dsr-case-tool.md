---
title: Gérer les demandes des personnes associées aux données RGPD avec l’outil de cas DSR dans le centre de sécurité & conformité
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
ms.assetid: ce9eb942-3589-42cb-88fd-1576ecb09c5c
description: Le RGPD donne aux citoyens de l’Union européenne (appelés «personnes des données») des droits spécifiques sur leurs données personnelles; ces droits incluent l’obtention de copies de celle-ci, la demande de modifications, la limitation du traitement de celle-ci, sa suppression ou sa réception dans un format électronique. Une demande officielle d’un objet de données qui doit agir sur ses données personnelles est appelée demande de l’objet de données ou DSR. Vous pouvez utiliser les dossiers DSR dans le centre de conformité dans Office 365 et Microsoft 365 pour gérer les investigations DSR de votre organisation.
ms.openlocfilehash: 8a4882070509991ca91403c96b55825fac3a2536
ms.sourcegitcommit: 6b2ca6bd153d24a717d6c537efd2d41d35c20a0b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35587839"
---
# <a name="manage-gdpr-data-subject-requests-with-the-dsr-case-tool-in-the-security--compliance-center"></a>Gérer les demandes des personnes associées aux données RGPD avec l’outil de cas DSR dans le centre de sécurité & conformité

Le règlement général sur la protection des données (RGPD) de l’UE concerne la protection et l’activation des droits de confidentialité des individus au sein de l’Union européenne (UE). Le RGPD donne aux individus de l’Union européenne (appelés «personnes concernées par les données») le droit d’accéder, de récupérer, de corriger, d’effacer et de restreindre le traitement de leurs données personnelles. Sous le RGPD, les données personnelles signifient toute information concernant une personne physique identifiée ou identifiable. Une demande officielle d’une personne à son organisation pour effectuer une action sur ses données personnelles est appelée demande de l’objet de données ou DSR. Pour plus d’informations sur la réponse à DSR pour les données dans Office 365, voir Guide de demande des personnes [concernées pour office 365](https://go.microsoft.com/fwlink/?linkid=871169 ).
  
Pour gérer les enquêtes en réponse à un DSR envoyé par une personne au sein de votre organisation, vous pouvez utiliser l’outil de cas DSR dans le centre de conformité & Compliance Center pour rechercher du contenu stocké dans:
  
- Toute boîte aux lettres utilisateur de votre organisation. Cela inclut les conversations Skype entreprise et les conversations un-à-un dans Microsoft teams
    
- Toutes les boîtes aux lettres associées à un groupe Office 365 et à toutes les boîtes aux lettres d’équipe dans Microsoft teams
    
- Tous les sites SharePoint Online et les comptes OneDrive Entreprise dans votre organisation
    
- Tous les sites teams et les sites de groupe Office 365 au sein de votre organisation
    
- Tous les dossiers publics dans Exchange Online
    
À l’aide de l’outil de cas DSR, vous pouvez:
  
- Créer un dossier distinct pour chaque examen de DPC.
    
- Contrôlez qui a accès au cas DSR en ajoutant des personnes en tant que membres du cas; Seuls les membres peuvent accéder au cas et ne peuvent voir que leurs incidents dans la liste des incidents sur la page des **incidents du DSR** dans le centre de conformité & Compliance Center. En outre, vous pouvez attribuer des autorisations différentes à différents membres de la même casse. Par exemple, vous pouvez autoriser certains membres à afficher uniquement le cas et les résultats de la recherche et permettre à d’autres membres de créer des recherches et d’exporter des résultats de recherche. 
    
- Utilisez la recherche intégrée pour rechercher tout le contenu créé ou téléchargé par un objet de données spécifique.
    
- Modifiez éventuellement la requête de recherche intégrée et réexécutez la recherche pour affiner les résultats de la recherche.
    
- Ajoutez d’autres recherches de contenu associées au boîtier DSR. Cela inclut la création de recherches qui renvoient des éléments partiellement indexés et des journaux générés par le système à partir du service d’itinérance Office.
    
- Exporter les données en réponse à une demande d’accès ou d’exportation DSR.
    
- Supprimez des cas lorsque le processus d’enquête DSR est terminé. Cette opération supprime toutes les recherches et les tâches d’exportation associées au cas.
    
Voici le processus de haut niveau pour l’utilisation de l’outil de cas DSR afin de gérer les investigations DSR:
  
[Step 1: Assign eDiscovery permissions to potential case members](#step-1-assign-ediscovery-permissions-to-potential-case-members)

[Étape 2: créer un cas DSR et ajouter des membres](#step-2-create-a-dsr-case-and-add-members)

[Étape 3: exécuter la requête de recherche](#step-3-run-the-search-query)

[Étape 4: exporter les données](#step-4-export-the-data)

[Module Étape 5: réviser la requête de recherche intégrée](#optional-step-5-revise-the-built-in-search-query)

[Plus d’informations sur l’utilisation de l’outil de cas DSR](#more-information-about-using-the-dsr-case-tool)
  
> [!IMPORTANT]
> Nos outils peuvent aider les administrateurs à effectuer des demandes d’accès ou d’exportation via le DSR en leur permettant d’utiliser les fonctionnalités de recherche et d’exportation intégrées de l’outil de cas DSR. L’outil aide à faciliter l’exportation des données correspondant à une demande DSR soumise par un objet de données. Toutefois, il est important de noter que les résultats de la recherche peuvent varier en fonction de la personne concernée ou des actions d’administration entreprises qui peuvent avoir un impact sur le fait qu’un élément soit considéré comme «données personnelles» à des fins d’exportation ou non. Par exemple, si la personne concernée était la dernière personne à avoir modifié un fichier qu’elle n’a pas créée, le fichier peut ne pas être renvoyé dans les résultats de la recherche. De même, un administrateur peut exporter des données sans inclure les éléments partiellement indexés ou toutes les versions des documents SharePoint. Par conséquent, les outils fournis peuvent faciliter l’accès et l’exportation des demandes de données; Toutefois, les résultats sont soumis à des scénarios d’utilisation spécifiques des personnes et de l’administrateur. 
  
## <a name="step-1-assign-ediscovery-permissions-to-potential-case-members"></a>Étape 1 : attribuer des autorisations de découverte électronique aux membres potentiels de cas

Par défaut, un administrateur général Office 365 peut accéder à l’outil de cas DSR dans le centre de conformité & Compliance Center. De par leur conception, les autres utilisateurs, tels que les responsables de la confidentialité des données, le responsable des ressources humaines ou toute autre personne impliquée dans les investigations DSR n’ont pas accès à l’outil de gestion des incidents DSR et devront disposer des autorisations appropriées pour accéder à l’outil. Pour ce faire, la méthode la plus simple consiste à accéder à la page **autorisations** dans le centre de sécurité & conformité et à ajouter des utilisateurs au groupe de rôles gestionnaire eDiscovery. Vous devez également attribuer ces autorisations afin de pouvoir les ajouter en tant que membres du cas DSR que vous créez à l’étape 2. 
  
Pour obtenir des instructions détaillées, reportez-vous à [la rubrique attribution d’autorisations eDiscovery dans le centre de conformité & Office 365 Security](assign-ediscovery-permissions.md).
  
> [!NOTE]
> Par défaut, un administrateur général Office 365 (ou d’autres membres du groupe de rôles gestion de l’organisation dans le centre de sécurité & conformité ne dispose pas des autorisations nécessaires pour exporter les résultats de la recherche de contenu (Voir l’étape 4 de cet article). Pour résoudre ce cas, un administrateur peut s’ajouter lui-même en tant que membre du groupe de rôles gestionnaire eDiscovery. 
  
## <a name="step-2-create-a-dsr-case-and-add-members"></a>Étape 2: créer un cas DSR et ajouter des membres

L’étape suivante consiste à créer un boîtier DSR. Lorsque vous créez un cas, vous pouvez choisir de démarrer la recherche intégrée ou vous pouvez créer le cas sans lancer la recherche. La procédure suivante vous demande de créer le cas sans lancer la recherche, puis vous montrer comment ajouter des membres au cas.
  
1. Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous à Office 365 à l’aide de votre compte professionnel ou scolaire. 
    
2. Dans le centre de sécurité & conformité, cliquez sur **demandes**des personnes concernées par la **confidentialité** \> des données, puis cliquez sur ![ajouter une icône](media/ITPro-EAC-AddIcon.gif) **nouveau DSR case**.
    
3. Sur la page de la nouvelle boîte flyout du **boîtier DSR** , attribuez un nom à la demande, tapez une description facultative, puis cliquez sur **suivant**. Le nom du cas doit être unique dans toute votre organisation.
    
    > [!TIP]
    > Envisagez d’ajouter le nom de la personne qui a envoyé la demande DSR que vous recherchez dans le nom et/ou la description du nouveau cas. Notez que seuls les membres de ce cas (et les administrateurs eDiscovery) seront en mesure de voir le cas dans la liste des incidents de la page demandes des personnes **concernées** . 
  
4. Sur la page Détails de la **demande** , sous personne **concernée (la personne qui a soumis cette demande)**, sélectionnez la personne pour laquelle vous souhaitez rechercher et exporter les données, puis cliquez sur **suivant**.
    
5. Sur la page **confirmer les paramètres de votre cas** , vous pouvez modifier le nom et la description de la case, puis sélectionner un autre objet de données. Dans le cas contraire, cliquez sur **Enregistrer**.
    
    Une page s’affiche pour confirmer la création du nouveau boîtier DSR.
    
    ![Démarrer la recherche ou fermer la nouvelle page du dossier DSR](media/b5e62c2c-cafe-4a8d-a38c-789ed9f9ccbd.png)
  
    À ce stade, vous pouvez effectuer l’une des deux opérations suivantes:
    
    a. Le fait de cliquer sur **afficher les résultats** de la recherche démarre la recherche. Il s’agit de la sélection par défaut. La recherche intégrée exécutée lorsque vous sélectionnez cette option et les résultats renvoyés sont abordés à l’étape 3.
    
    b. Si vous cliquez sur **Terminer** , le nouvel incident DSR se ferme sans démarrer la recherche intégrée. Lorsque vous sélectionnez cette option, le nouvel incident DSR s’affiche sur la page demandes des personnes **concernées** .
    
6. Cliquez sur **Terminer** pour pouvoir accéder au nouveau boîtier DSR et y ajouter des membres. 
    
7. Sur la page demandes des personnes **concernées** , cliquez sur le nom du boîtier DSR que vous avez créé. 
    
8. Sur la page flyout **gérer ce cas** , sous **gérer les membres**, cliquez sur **Ajouter**. 
    
    Sous **utilisateurs**, une liste de personnes disposant des autorisations eDiscovery appropriées s’affiche. Les personnes auxquelles vous avez attribué des autorisations de découverte électronique à l’étape 1 seront affichées dans cette liste. 
    
9. Sélectionnez les personnes à ajouter en tant que membres du boîtier DSR, cliquez sur **Ajouter**, puis enregistrez vos modifications.
    
    Vous pouvez également ajouter des groupes de rôles en tant que membres du boîtier DSR en cliquant sur **Ajouter** sous **gérer les groupes de rôles**. 
    
## <a name="step-3-run-the-search-query"></a>Étape 3: exécuter la requête de recherche

Une fois que vous avez créé un boîtier DSR et ajouté des membres, l’étape suivante consiste à exécuter la recherche intégrée associée au cas. Cette requête de recherche par défaut effectue les opérations suivantes:
  
- Recherche dans toutes les boîtes aux lettres de votre organisation tous les éléments de courrier électronique qui ont été envoyés ou reçus par la personne concernée. Pour ce faire, utilisez la propriété email des *participants* , qui recherche l’objet de données dans tous les champs de personnes dans un message électronique. Cette propriété renvoie les éléments dans lesquels la personne concernée est comprise dans les champs **de**, **à**, **CC**et **CCI** . Les dossiers publics dans Exchange Online sont également recherchés pour les messages envoyés ou reçus par la personne concernée par les données. 
    
- Recherche dans tous les sites de votre organisation les documents et les éléments créés ou téléchargés par l’objet des données. Pour ce faire, utilisez les propriétés de site suivantes:
    
  - La propriété *auteur* renvoie les éléments dans lesquels la personne concernée est indiquée dans le champ auteur des documents Office. Cette valeur persiste, même si le document est copié et téléchargé par une autre personne. 
    
  - La propriété *CreatedBy* renvoie les éléments qui ont été créés ou téléchargés par l’objet de données. 
    
Voici à quoi ressemble la requête de mot clé pour la recherche intégrée qui est créée automatiquement lors de la création d’un cas DSR.
  
```
participants:"<email address>" OR author:"<display name>" OR createdby:"<display name>"
```

Par exemple, si le nom de la personne concernée est de type Leonte, la requête de mot clé ressemblera à ceci:
  
```
participants:"ina@contoso.com" OR author:"Ina Leonte" OR createdby:"Ina Leonte"
```

 **Pour exécuter la recherche intégrée pour un cas de DSR:**
  
1. Dans le centre de sécurité & conformité, cliquez sur demandes des personnes **concernées**par la **confidentialité** \> des données, puis cliquez sur **ouvrir** en regard du cas DSR que vous avez créé à l’étape 2. 
    
    Cliquez sur l’onglet **Rechercher** en haut de la page, puis cliquez sur la case à cocher en regard de la recherche intégrée créée lors de la création du boîtier DSR. La recherche porte le même nom que le boîtier DSR. 
    
2. Dans la page flyout de recherche, cliquez sur **ouvrir une requête**.
    
    Lorsque vous ouvrez la requête, la recherche est démarrée et se termine dans quelques instants. 
    
3. Une fois la recherche terminée, cliquez sur **aperçu des résultats** pour afficher un aperçu des résultats de la recherche. Pour plus d’informations, consultez la rubrique [aperçu des résultats](content-search.md#preview-search-results)de la recherche.
    
    > [!TIP]
    > Vous pouvez également afficher les statistiques de requête de recherche pour afficher le nombre d’éléments de boîte aux lettres et de site renvoyés par la recherche, ainsi que les emplacements de contenu de niveau supérieur qui contiennent les éléments qui correspondent à la requête de recherche. Pour plus d’informations, consultez [la rubrique afficher les informations et les statistiques relatives à une recherche](content-search.md#view-information-and-statistics-about-a-search). 
  
Vous pouvez modifier la requête de recherche intégrée, modifier les emplacements de contenu qui font l’objet d’une recherche, puis réexécuter la recherche. Pour plus d’informations, voir l' [étape 5](#optional-step-5-revise-the-built-in-search-query) . 
  
## <a name="step-4-export-the-data"></a>Étape 4: exporter les données

Après avoir exécuté la recherche intégrée, vous pouvez exporter les résultats de la recherche. Par ailleurs, avant d’exporter les données, vous souhaiterez peut-être modifier la requête afin de réduire le nombre de résultats de recherche. Pour plus d’informations sur la restriction des résultats de la recherche, voir l’étape 5.
  
Lorsque vous exportez des résultats de recherche, les éléments de boîte aux lettres peuvent être téléchargés dans des fichiers PST ou des messages individuels. Lorsque vous exportez du contenu à partir de comptes SharePoint et OneDrive, les copies des documents Office natifs et d’autres documents sont exportées. Un fichier de résultats qui contient des informations sur chaque élément exporté est inclus dans les résultats de la recherche. Pour plus d’informations sur l’exportation, voir [Export content Search Results](export-search-results.md).
  
> [!NOTE]
> Par défaut, un administrateur général Office 365 (ou d’autres membres du groupe de rôles gestion de l’organisation dans le centre de sécurité & conformité) ne dispose pas des autorisations nécessaires pour exporter les résultats de la recherche de contenu. Pour résoudre ce cas, un administrateur peut s’ajouter lui-même en tant que membre du groupe de rôles gestionnaire eDiscovery. 
  
L’ordinateur que vous utilisez pour exporter des données doit répondre aux exigences système suivantes:
  
- versions 32 bits ou 64 bits de Windows 7 et versions ultérieures
    
- Microsoft .NET Framework 4,7
    
- un navigateur pris en charge :
    
  - Microsoft Edge
    
    Ou
    
  - Microsoft Internet Explorer 10 et versions ultérieures
    
    > [!NOTE]
    > Microsoft ne fabrique pas d’extensions ou de modules complémentaires tiers pour les applications ClickOnce. L’exportation de données à l’aide d’un navigateur non pris en charge avec des extensions ou des modules complémentaires tiers n’est pas prise en charge. 
  
 **Pour exporter les données de la recherche intégrée dans un cas de DSR:**
  
1. Dans le centre de sécurité & conformité, cliquez sur demandes des personnes **concernées**par la **confidentialité** \> des données, puis cliquez sur **ouvrir** en regard du cas DSR à partir duquel vous souhaitez exporter les données. 
    
2. Cliquez sur l’onglet **Rechercher** en haut de la page, puis cliquez sur la case à cocher en regard de la recherche intégrée créée lors de la création du boîtier DSR. Ou cliquez sur une autre recherche pour exporter les données de cette recherche. 
    
3. Sur la page flyout de recherche, ![cliquez sur Exporter les](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) résultats de recherche **plus en plus**, puis sélectionnez **Exporter les résultats** dans la liste déroulante. 
    
4. Sur la page **Exporter les résultats** , sélectionnez les options recommandées suivantes pour les demandes d’exportation DSR. 
    
    ![Configurer les paramètres d’exportation](media/25416b79-57da-46a1-ae07-e640602a8fa4.png)
  
    a. Sous **options de sortie**, sélectionnez la première option (**tous les éléments, sauf ceux dont le format n’est pas reconnu, sont chiffrés ou n’ont pas été indexés pour d’autres raisons**) pour exporter uniquement les éléments indexés. La raison pour laquelle vous ne voulez pas exporter des éléments partiellement indexés à partir de la recherche intégrée est que les éléments partiellement indexés provenant d’autres utilisateurs sont également exportés. Pour exporter uniquement les éléments partiellement indexés de la personne concernée, nous vous recommandons de créer une recherche distincte. Pour plus d’informations, reportez-vous à la rubrique [exportation d’éléments partiellement indexés](#exporting-partially-indexed-items) dans la section «plus d’informations sur l’utilisation de l’outil de cas DSR».
    
    b. Sous **Exporter le contenu Exchange en tant que**, sélectionnez la troisième option, **un fichier PST contenant tous les messages dans un dossier unique**. Étant donné que certains résultats peuvent concerner des éléments provenant de la boîte aux lettres d’un autre utilisateur, cette option répertorie uniquement l’élément dans un seul dossier sans indiquer la boîte aux lettres réelle et est la meilleure option à utiliser lorsque vous Dédupliquez les résultats comme recommandé dans l’élément suivant. . Cette option permet également à la personne concernée de consulter les éléments dans l’ordre chronologique (les éléments sont triés par date d’envoi) sans avoir à naviguer dans la structure de dossiers d’origine de chaque élément.
    
    c. Sélectionnez **activer** la déduplication pour exclure les messages électroniques en double. Cette option est recommandée, car la recherche intégrée effectue une recherche dans toutes les boîtes aux lettres de votre organisation. Par conséquent, si plusieurs copies du même message sont trouvées dans les boîtes aux lettres qui ont été recherchées, cette option signifie qu’une seule copie d’un message sera exportée. Cette option permet d’exporter des messages dans un fichier PST d’un même dossier, ce qui permet aux utilisateurs les plus sollicités pour les demandes d’exportation DSR. Le rapport d’exportation results. csv répertorie tous les emplacements où des messages en double ont été trouvés.
    
    Vous pouvez également sélectionner l’option **inclure des versions pour les documents SharePoint** pour exporter toutes les versions des documents SharePoint et OneDrive. Cette opération exige que le contrôle de version soit activé pour les bibliothèques de documents. Cette option permet de s’assurer que toutes les données pertinentes sont exportées.
    
5. Une fois que vous avez choisi les paramètres d’exportation, cliquez sur **Exporter**.
    
    Les résultats de la recherche sont préparés pour téléchargement, ce qui signifie qu’ils sont téléchargés vers la zone de stockage Azure de votre organisation dans le Cloud Microsoft. Les étapes suivantes vous montrent comment télécharger ces données sur votre ordinateur local.
    
6. Cliquez sur l’onglet **Exporter** pour afficher le travail d’exportation que vous avez créé. Les travaux d’exportation portent le même nom que la recherche correspondante avec **_Export** ajouté à la fin du nom de recherche. 
    
7. Cliquez sur le travail d’exportation que vous venez de créer pour afficher la page de menu volant d’exportation. Cette page affiche des informations sur la recherche, telles que la taille et le nombre total d’éléments à exporter, ainsi que le pourcentage des éléments qui ont été transférés vers une zone de stockage Azure. Cliquez **** sur Actualiser pour mettre à jour les informations d’état de téléchargement. 
    
8. Sous **Clé d’exportation**, cliquez sur **Copier dans le Presse-papiers**. Cette clé est utilisée à l’étape 11 pour télécharger les résultats de la recherche.
    
9. Cliquez ![sur Exporter les résultats](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) de la recherche **Télécharger les résultats** en haut de la page de menu volant d’exportation. 
    
10. Dans la fenêtre contextuelle en bas de la page, cliquez sur **ouvrir** pour ouvrir l’outil d' **exportation de découverte électronique de Microsoft Office 365**. L' **outil d’exportation de découverte électronique** sera installé lors du premier téléchargement des résultats de recherche. 
    
11. Dans l' **outil d’exportation de découverte électronique**, collez la clé d’exportation que vous avez copiée à l’étape 8 dans la zone appropriée.
    
12. Cliquez sur **Parcourir** pour spécifier l’emplacement de téléchargement du fichier des résultats de recherche. 
    
    > [!NOTE]
    > En raison de la quantité élevée d’activité disque (lectures et écritures), vous devez télécharger les résultats de la recherche sur un disque dur local; ne les téléchargez pas sur un lecteur réseau mappé ni sur un autre emplacement réseau. 
  
13. Cliquez sur **Démarrer** pour télécharger les résultats de recherche sur votre ordinateur. 
    
    L’**outil d’exportation de découverte électronique** affiche l’état du processus d’exportation, ainsi qu’une estimation du nombre (et de la taille) d’éléments qui doivent encore être téléchargés. Une fois le processus d’exportation terminé, vous pouvez accéder aux fichiers à l’emplacement où ils ont été téléchargés. Pour plus d’informations sur les rapports inclus lorsque vous téléchargez des résultats de la recherche de contenu, voir la section [plus d’informations](export-search-results.md#more-information) dans «exporter les résultats de la recherche de contenu». 
    
Une fois les données exportées, les résultats de recherche et les rapports d’exportation se trouvent dans un dossier portant le même nom que le boîtier DSR. Les fichiers PST qui contiennent des éléments de boîte aux lettres se trouvent dans un sous-dossier nommé **Exchange**. Les documents et autres éléments provenant de sites se trouvent dans un sous-dossier nommé **SharePoint**. 
  
## <a name="optional-step-5-revise-the-built-in-search-query"></a>Module Étape 5: réviser la requête de recherche intégrée

Après avoir exécuté la recherche intégrée, vous pouvez la modifier pour affiner l’étendue afin de renvoyer moins de résultats. Pour ce faire, vous pouvez ajouter des conditions à la requête. Une condition est logiquement connectée à la requête de mot-clé par l’opérateur **and** . Cela signifie qu’elle doit être renvoyée dans les résultats de la recherche, les éléments doivent répondre à la fois à la requête par mot clé et aux conditions que vous ajoutez. Voici comment les conditions permettent de limiter les résultats. Si vous ajoutez deux ou plusieurs conditions uniques à une requête de recherche (conditions qui spécifient différentes propriétés), ces conditions sont logiquement liées par l’opérateur **and** . Cela signifie que seuls les éléments qui satisfont à toutes les conditions (en plus de la requête de mot clé) sont renvoyés. Si vous ajoutez plusieurs valeurs (séparées par des virgules ou des points-virgules) à une seule condition, ces valeurs sont reliées par l’opérateur **ou** . Les éléments renvoyés sont ceux qui contiennent l’une des valeurs spécifiées pour la propriété dans la condition. 
  
Voici quelques exemples des conditions que vous pouvez ajouter à la requête de recherche intégrée d’un boîtier DSR. Le nom de la propriété réelle utilisée dans une requête de recherche est indiqué entre parenthèses.
  
- **Type de fichier `filetype`()** – spécifie l’extension d’un document ou d’un fichier. Utilisez cette condition pour rechercher des documents et des fichiers créés par des applications Office spécifiques, telles que Word, Excel et OneNote. 
    
- **Type de message `kind`()** – spécifie le type d’élément de courrier électronique à rechercher. Par exemple, vous pouvez utiliser la syntaxe `kind:email OR kind:im` pour renvoyer uniquement les messages électroniques et les conversations Skype entreprise ou les conversations un-à-un dans Microsoft Teams. 
    
- **Balise de`compliancetag`conformité ()** : spécifie une étiquette affectée à un message électronique ou à un document. Cette condition renvoie les éléments classés avec une étiquette spécifique. Les étiquettes sont utilisées pour classer le courrier électronique et les documents à des fins de gouvernance des données et appliquer des règles de rétention basées sur la classification définie par l’étiquette. Il s’agit d’une condition utile pour les investigations du DSR car votre organisation peut utiliser des étiquettes pour classer le contenu lié à la confidentialité des données ou contenant des données personnelles ou des informations sensibles. Pour la valeur de cette condition, utilisez le nom complet de l’étiquette ou la première partie du nom de l’étiquette avec un caractère générique. Pour plus d’informations, consultez la rubrique [vue d’ensemble des étiquettes dans Office 365](labels.md).
    
Pour obtenir la liste et la description de toutes les conditions disponibles dans l’outil de cas DSR, consultez la rubrique [conditions de recherche](keyword-queries-and-search-conditions.md#search-conditions) dans l’article «requêtes de mot-clé et conditions de recherche pour la recherche de contenu». 
  
### <a name="changing-the-content-locations-that-are-searched"></a>Modification des emplacements de contenu qui sont recherchés

En plus de réviser la recherche intégrée pour un cas de DSR, vous pouvez également modifier les emplacements de contenu dans lesquels la recherche est effectuée. Comme expliqué précédemment, la recherche intégrée recherche toutes les boîtes aux lettres et tous les sites de l’organisation, ainsi que les dossiers publics Exchange Online. Par exemple, vous pouvez affiner la recherche pour rechercher uniquement la boîte aux lettres et le compte OneDrive de l’objet de données et les sites SharePoint sélectionnés. Si vous choisissez de rechercher des sites spécifiques, vous devez ajouter chaque site sur lequel vous souhaitez effectuer des recherches.
  
Pour modifier les emplacements de contenu à Rechercher:
  
1. Ouvrez la recherche intégrée dont vous souhaitez modifier les emplacements de contenu.
    
2. Dans la requête de recherche, sous **emplacements**, cliquez sur **modifier** en regard de l’option **emplacements spécifiques** . 
    
    ![Cliquez sur modifier pour modifier les emplacements de contenu de la requête de recherche intégrée.](media/d66f7ba7-b71f-4ff5-a030-460ff02e3123.png)
  
    La page mobile **modifier les emplacements** s’affiche. Voici une description des emplacements de contenu dans la recherche intégrée et des informations sur la modification des emplacements qui font l’objet de la recherche. 
    
    ![Page de menu de modification des emplacements](media/56c033f6-6735-46ba-abb2-a263a2b79836.png)
  
    a. Le bouton bascule sous **Sélectionner tout** dans la boîte aux lettres en haut de la page de menu volant est sélectionné, ce qui indique que toutes les boîtes aux lettres sont recherchées. Pour affiner l’étendue de la recherche, cliquez sur le bouton bascule pour la désélectionner, puis cliquez sur **choisir les utilisateurs, les groupes ou les équipes** , puis choisissez des boîtes aux lettres spécifiques à rechercher.
    
    b. Le bouton bascule sous **Sélectionner tout** dans la section sites au milieu de la page de lanceur est sélectionné, ce qui indique que tous les sites font l’objet d’une recherche. Pour limiter la recherche aux sites sélectionnés, désélectionnez le bouton bascule, puis cliquez sur **choisir les sites**. Vous devez ajouter chaque site spécifique que vous souhaitez rechercher, y compris le compte OneDrive de l’objet de données.
    
    c. Le bouton bascule dans la section dossiers publics Exchange est sélectionné, ce qui signifie que tous les dossiers publics Exchange font l’objet d’une recherche. Vous pouvez uniquement Rechercher tous les dossiers publics Exchange ou aucun d’entre eux. Vous ne pouvez pas choisir des critères de recherche spécifiques.
    
3. Si vous modifiez les emplacements de contenu dans la recherche intégrée, cliquez sur **Enregistrer &amp; exécuter** pour redémarrer la recherche. 

> [!NOTE]
> Lorsque vous recherchez tous les emplacements de boîte aux lettres ou seulement des boîtes aux lettres spécifiques, les données d’autres applications Office 365 enregistrées dans des boîtes aux lettres utilisateur sont incluses lorsque vous exportez les résultats de la recherche. Ces données ne sont pas incluses dans les résultats de recherche estimés et ne sont pas disponibles pour l’aperçu. Toutefois, elle est incluse lorsque vous exportez et téléchargez les résultats de la recherche. Pour plus d’informations sur les applications qui stockent des données dans la boîte aux lettres d’un utilisateur, consultez la rubrique [contenu stocké dans les boîtes aux lettres Exchange Online](what-is-stored-in-exo-mailbox.md).
  
## <a name="more-information-about-using-the-dsr-case-tool"></a>Plus d’informations sur l’utilisation de l’outil de cas DSR

Les sections suivantes contiennent plus d’informations sur l’utilisation de l’outil de cas DSR pour répondre aux demandes d’exportation DSR.
  
[Exportation de données à partir du service d’itinérance Office](#exporting-data-from-the-office-roaming-service)

[Exportation d’éléments partiellement indexés](#exporting-partially-indexed-items)

[Recherche et exportation de données à partir de groupes Microsoft teams et Office 365](#searching-and-exporting-data-from-microsoft-teams-and-office-365-groups)

[Recherche dans les dossiers publics Exchange](#searching-exchange-public-folders)
  
### <a name="exporting-data-from-the-office-roaming-service"></a>Exportation de données à partir du service d’itinérance Office

Vous pouvez utiliser l’outil de cas DSR pour rechercher et exporter les données d’utilisation générées par le service d’itinérance Office. L’itinérance est un service qui stocke les paramètres Office, tels que le thème Office, le dictionnaire personnel, les paramètres de langue, le mode développeur et la correction automatique. 
    
Les données du service d’itinérance Office sont stockées dans la boîte aux lettres d’un objet de données dans un dossier masqué situé dans une sous-arborescence non de message interpersonnel (non-IPM) des boîtes aux lettres Exchange Online. Cela signifie que les données sont masquées dans l’affichage de l’utilisateur lorsqu’elles utilisent Outlook ou d’autres clients de messagerie pour accéder à leur boîte aux lettres. Pour plus d’informations sur les dossiers masqués, consultez la rubrique [MAPI Hidden Folders](https://go.microsoft.com/fwlink/?linkid=872758).
  
Vous pouvez créer une recherche de contenu distincte (et l’associer à un boîtier DSR) qui renvoie les données d’utilisation du service d’itinérance Office dans la boîte aux lettres de l’objet des données. Ces données ne sont pas incluses dans les statistiques de recherche et ne seront pas disponibles pour l’aperçu. Toutefois, vous pouvez l’exporter, puis la transmettre à la personne concernée en réponse à une demande d’exportation DSR.
  
Lorsque vous exportez des données à partir du service d’itinérance Office, les données sont enregistrées dans un dossier distinct situé dans le dossier **ApplicationDataRoot** , qui se trouve sous un dossier dont le nom correspond à l’adresse de messagerie de l’objet de données. Ces données sont exportées en tant que fichiers JSON, qui sont des fichiers texte lisibles humains, similaires aux fichiers XML ou TXT, qui sont joints aux messages électroniques. Actuellement, ce dossier est nommé avec l’identificateur global unique (GUID): **1caee58f-EB14-4a6b-9339-1fe2ddf6692b**. Dans les versions ultérieures de l’outil de cas DSR, le GUID est remplacé par le nom de l’application réelle. 

   
 **Pour rechercher et exporter les données du service d’itinérance Office:**
  
1. Dans le centre de sécurité & conformité, cliquez sur demandes des personnes **concernées**par la **confidentialité** \> des données, puis cliquez sur **ouvrir** en regard du cas du DSR pour la personne concernée dont vous souhaitez exporter les données d’utilisation. 
    
2. Cliquez sur l’onglet **Rechercher** en haut de la page, puis cliquez sur ![ajouter une](media/ITPro-EAC-AddIcon.gif) **recherche guidée**par icône.
    
3. Cliquez sur **Annuler** dans la page **nom de votre recherche** . 
    
4. Sous **requête de recherche**, dans la condition **type** , activez la case à cocher en regard de **service d’itinérance Office**. 
    
    ![Activez la case à cocher service d’itinérance Office pour exporter les données d’utilisation.](media/O365_DSRCase_SDSDataExport1.png)
  
    La condition **type** (qui sont des classes de message électronique) doit être le seul élément de la requête de recherche. Vous pouvez supprimer la zone **Mots clés** ou la laisser vide. 
    
5. Sous **emplacements**, vérifiez que l’option **emplacements spécifiques** est sélectionnée, puis cliquez sur **modifier**.
    
6. En haut de la page mobile **modifier les emplacements** (boîte aux lettres), cliquez sur **choisir les utilisateurs, les groupes ou les équipes**.
    
7. Dans la page **modifier les emplacements** , cliquez sur **choisir les utilisateurs, les groupes ou les équipes**, choisissez la boîte aux lettres de l’objet de données, puis enregistrez votre sélection. 
    
8. Cliquez sur **enregistrer & exécuter**, puis nommez la recherche et enregistrez-la.
    
    La recherche démarre.
    
 **Pour exporter les données du service d’itinérance Office:**
  
1. Lorsque la recherche que vous avez créée à l’étape précédente est terminée, cliquez sur l’onglet **recherche** en haut de la page, puis cliquez sur la case à cocher en regard de la recherche. Vous devrez peut-être ![cliquer](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png) sur Actualiser l' **actualisation** pour afficher la recherche. 
    
2. Sur la page flyout de recherche, ![cliquez sur Exporter les](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) résultats de recherche **plus en plus**, puis sélectionnez **Exporter les résultats** dans la liste déroulante. 
    
3. Sur la page **Exporter les résultats** , sélectionnez les options recommandées pour exporter les données d’utilisation. 
    
    ![Options d’exportation lors de l’exportation des données d’utilisation du service d’itinérance Office](media/470a7d1e-eeae-4b42-95aa-15cb82ce2f68.png)
  
    a. Sous **options de sortie**, sélectionnez la première option (**tous les éléments, sauf ceux dont le format n’est pas reconnu, sont chiffrés ou n’ont pas été indexés pour d’autres raisons**) pour exporter uniquement les éléments indexés.
    
    b. Sous **Exporter le contenu Exchange en tant que**, sélectionnez la deuxième option, **un fichier PST contenant tous les messages**.
    
    c. Laissez les options d’exportation restantes non sélectionnées.
    
4. Une fois que vous avez choisi les paramètres d’exportation, cliquez sur **Exporter**.
    
    Les résultats de la recherche sont préparés pour téléchargement, ce qui signifie qu’ils sont téléchargés vers la zone de stockage Azure de votre organisation dans le Cloud Microsoft. Les étapes suivantes vous montrent comment télécharger ces données sur votre ordinateur local.
    
5. Cliquez sur l’onglet **Exporter** pour afficher le travail d’exportation que vous avez créé. Les travaux d’exportation portent le même nom que la recherche correspondante avec **_Export** ajouté à la fin du nom de recherche. 
    
6. Cliquez sur le travail d’exportation que vous venez de créer pour afficher la page de menu volant d’exportation. 
    
7. Sous **Clé d’exportation**, cliquez sur **Copier dans le Presse-papiers**. Cette clé est utilisée à l’étape 10 pour télécharger les résultats de la recherche.
    
8. Cliquez ![sur Exporter les résultats](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) de la recherche **Télécharger les résultats** en haut de la page de menu volant d’exportation. 
    
9. Dans la fenêtre contextuelle en bas de la page, cliquez sur **ouvrir** pour ouvrir l’outil d' **exportation de découverte électronique de Microsoft Office 365**. L' **outil d’exportation de découverte électronique** sera installé lors du premier téléchargement des résultats de recherche. 
    
10. Dans l’**outil d’exportation de découverte électronique**, collez la clé d’exportation que vous avez copiée à l’étape 7 dans la zone appropriée.
    
11. Cliquez sur **Parcourir** pour spécifier l’emplacement de téléchargement du fichier des résultats de recherche. 
    
    > [!NOTE]
    > En raison de la quantité élevée d’activité disque (lectures et écritures), vous devez télécharger les résultats de la recherche sur un disque dur local; ne les téléchargez pas sur un lecteur réseau mappé ni sur un autre emplacement réseau. 
  
12. Cliquez sur **Démarrer** pour télécharger les résultats de recherche sur votre ordinateur. 
    
    L’**outil d’exportation de découverte électronique** affiche l’état du processus d’exportation, ainsi qu’une estimation du nombre (et de la taille) d’éléments qui doivent encore être téléchargés. Une fois le processus d’exportation terminé, vous pouvez ouvrir le fichier PST Exchange dans Outlook, puis accéder au dossier **ApplicationDataRoot** pour accéder au sous-dossier du service d’itinérance. 
    
    Comme expliqué précédemment, les fichiers JSON qui contiennent les données d’utilisation sont joints aux messages. Pour afficher un fichier JSON, cliquez sur un message, puis ouvrez le fichier JSON joint. 
  
### <a name="exporting-partially-indexed-items"></a>Exportation d’éléments partiellement indexés

Nous vous recommandons de ne pas exporter les éléments partiellement indexés (également appelés éléments non indexés) à partir de la recherche intégrée créée lors de la création d’un cas DSR. Cela est dû au fait que les résultats de la recherche seront bien plus probables que les éléments partiellement indexés pour les autres utilisateurs de votre organisation, et pas seulement les éléments partiellement indexés de la personne concernée). Au lieu de cela, nous vous recommandons de créer une recherche de contenu distincte associée au cas DSR conçu pour exporter uniquement les éléments partiellement indexés liés à la personne concernée. 
  
Voici un processus de haut niveau pour exporter des éléments partiellement indexés. Une fois qu’elles sont exportées, vous pouvez les consulter pour déterminer si un élément répond à une demande d’accès ou d’exportation DSR.
  
1. Ouvrez le DSR et créez une recherche sur la page de **recherche** . 
    
2. Utilisez les critères suivants pour configurer la requête de recherche et les emplacements de contenu à Rechercher:
    
    - Utilisez une requête de mot clé vide/vide. Cette méthode renvoie tous les éléments dans les emplacements de contenu qui sont recherchés.
    
    - Recherchez uniquement la boîte aux lettres Exchange Online de l’objet de données et son compte OneDrive.
    
3. Après avoir exécuté la recherche et terminé, vous pouvez exporter et télécharger les résultats de la recherche (comme décrit à l' [étape 4](#step-4-export-the-data)). Utilisez les paramètres suivants pour exporter des éléments partiellement indexés. 
    
    - Sous **options de sortie**, sélectionnez la troisième option (**seuls les éléments dont le format n’est pas reconnu, sont chiffrés ou n’ont pas été indexés pour d’autres raisons**) pour exporter uniquement les éléments partiellement indexés.
    
    - Sous **Exporter le contenu Exchange en tant que**, vous pouvez sélectionner n’importe quelle option en fonction de vos préférences. 
    
    - La sélection de l’option **inclure les versions pour les documents SharePoint** exporte les versions des documents si une version est partiellement indexée. 
    
Pour plus d’informations sur les éléments partiellement indexés, voir: 
  
- [Éléments partiellement indexés dans la recherche de contenu dans Office 365](partially-indexed-items-in-content-search.md)

- [Exportation d’éléments partiellement indexés](export-search-results.md#exporting-partially-indexed-items)
    
### <a name="searching-and-exporting-data-from-microsoft-teams-and-office-365-groups"></a>Recherche et exportation de données à partir de groupes Microsoft teams et Office 365

Les conversations faisant partie de la liste de conversation de Microsoft Teams (appelées conversations d’équipe ou conversations un-à-un) sont stockées dans la boîte aux lettres Exchange Online des utilisateurs qui participent aux conversations. Par ailleurs, les fichiers qu’une personne partage dans une conversation un-à-un sont stockés dans le compte OneDrive de la personne qui partage le fichier. Étant donné que la recherche intégrée recherche dans toutes les boîtes aux lettres et les comptes OneDrive de l’organisation, les conversations d’équipe et les documents partagés dans une session de conversation (que la personne concernée a créée ou chargée) sont renvoyés par la recherche intégrée dans un cas de DSR.
  
En guise d’alternative, les conversations qui font partie d’un canal Teams (également appelé messages de canal) sont stockées dans la boîte aux lettres associée à une équipe. Ces types de conversations auxquelles l’objet de données a participé sont également renvoyés par la recherche intégrée car toutes les boîtes aux lettres associées à teams sont recherchées. En outre, les fichiers partagés par un objet de données dans un canal teams sont stockés sur le site SharePoint de l’équipe. Les fichiers créés ou téléchargés par l’objet des données sont renvoyés par la recherche intégrée dans un cas de DSR car les sites associés à teams sont inclus dans la recherche.
  
De même, les boîtes aux lettres et les sites SharePoint qui correspondent à un groupe Office 365 sont également inclus dans la recherche intégrée. Cela signifie que les messages électroniques envoyés ou reçus par la personne concernée et les fichiers créés ou téléchargés par l’objet des données sont renvoyés. 
  
Pour plus d’informations sur l’utilisation de la recherche de contenu pour rechercher des éléments dans les groupes Microsoft teams et Office 365 ou pour voir comment obtenir une liste de membres, consultez la section «recherche de groupes Microsoft teams et de groupes Office 365» dans [recherche de contenu dans Office 365](content-search.md#searching-microsoft-teams-and-office-365-groups). 
  
### <a name="searching-exchange-public-folders"></a>Recherche dans les dossiers publics Exchange

La recherche intégrée dans un cas de DSR ne renverra que les messages électroniques envoyés par la personne concernée à un dossier public à extension messagerie ou des messages envoyés par une autre personne à un dossier public, ainsi que la personne concernée par les données. Il ne renvoie pas les messages que la personne concernée a publiée dans un dossier public. Pour rechercher des éléments que la personne concernée a publiée dans un dossier public, vous pouvez créer une recherche de contenu distincte qui recherche tous les éléments publiés dans un dossier public par la personne concernée.
  
Voici un processus de haut niveau permettant de rechercher des éléments que la personne concernée a publiée dans un dossier public. 
  
1. Ouvrez le DSR et créez une recherche sur la page de **recherche** . 
    
2. Utilisez les critères suivants pour configurer la requête de recherche et les emplacements de contenu à Rechercher:
    
  - Dans la zone **Mots clés** , utilisez la requête de recherche suivante: 
    
    ```
    itemclass:ipm.post AND "<email address of the data subject>"
    ```

  - Rechercher tous les dossiers publics Exchange
    
  - Après avoir exécuté la recherche et terminé, vous pouvez exporter et télécharger les résultats de la recherche (comme décrit à l' [étape 4](#step-4-export-the-data)). Utilisez les paramètres suivants pour exporter des éléments partiellement indexés. 
