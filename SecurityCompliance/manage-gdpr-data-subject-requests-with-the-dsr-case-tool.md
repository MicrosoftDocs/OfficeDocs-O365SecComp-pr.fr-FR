---
title: Gérer les demandes d’objet de données PIBR avec l’outil DSR de sécurité Office 365 &amp; centre de conformité
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 5/25/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Strat_O365_IP
ms.assetid: ce9eb942-3589-42cb-88fd-1576ecb09c5c
description: Droits PIBR donne l’Union européenne citoyens (appelés personnes concernées) spécifiques à leurs données personnelles ; ces droits incluent obtention de copies de celle-ci, demandant des modifications, une restriction sur le traitement de celle-ci, supprimer ou reçoit sous forme électronique. Une demande officielle par une données soumis à prendre une action sur leurs données personnelles est appelée une demande d’objet de données ou le DSR. Vous pouvez utiliser des cas de DSR de sécurité Office 365 &amp; centre de conformité pour gérer les enquêtes DSR de votre organisation.
ms.openlocfilehash: c8edee8d377865d46662ebbd7f18a5a6f3015192
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528200"
---
# <a name="manage-gdpr-data-subject-requests-with-the-dsr-case-tool-in-the-office-365-security-amp-compliance-center"></a>Gérer les demandes d’objet de données PIBR avec l’outil DSR de sécurité Office 365 &amp; centre de conformité

L’Union européenne générale Data Protection règlement (PIBR) est à la protection et l’activation des droits de confidentialité des personnes à l’intérieur de l’Union européenne (UE). PIBR permet de personnes dans l’Union européenne (appelé personnes concernées) le droit d’accès, de récupérer, corriger, effacer et limiter le traitement des données personnelles. Sous le PIBR, données personnelles signifie que les informations relatives à une personne physique identifiée ou identifiable. Une demande formelle par une personne pour leur organisation à effectuer une action sur leurs données personnelles est appelée une demande d’objet de données ou le DSR. Pour plus d’informations sur la réponse à ces évaluations détaillées pour les données dans Office 365, reportez-vous au [Guide de demande Office 365 données Subject](https://go.microsoft.com/fwlink/?linkid=871169 ).
  
Pour gérer les enquêtes en réponse à un DSR envoyé par une personne dans votre organisation, vous pouvez utiliser l’outil DSR de sécurité Office 365 &amp; centre de conformité pour rechercher le contenu stocké dans :
  
- Boîtes aux lettres utilisateur dans votre organisation. Cela inclut Skype pour des conversations et des salles de conversation dans Microsoft Teams
    
- Toutes les boîtes aux lettres associés à un groupe d’Office 365 et toutes les boîtes aux lettres de l’équipe dans Microsoft Teams
    
- Tous les sites SharePoint Online et les comptes OneDrive Entreprise dans votre organisation
    
- Tous les sites d’équipes et Office 365 groupe dans votre organisation
    
- Tous les dossiers publics dans Exchange Online
    
Vous pouvez utiliser l’outil DSR :
  
- Créer un dossier distinct pour chaque examen de DSR.
    
- Contrôler qui a accès à la casse DSR en ajoutant des personnes en tant que membres de l’incident ; Seuls les membres peuvent accéder à la casse et ne pouvez voir leurs cas dans la liste des cas dans la page **cas DSR** dans la sécurité &amp; centre de conformité. En outre, vous pouvez affecter des autorisations différentes à différents membres de la casse. Par exemple, vous pouvez autoriser certains membres uniquement afficher les résultats de recherche et cas et permettre aux autres membres de créer des recherches et exporter les résultats de recherche. 
    
- Utilisez intégrés à une recherche pour tout le contenu créés ou téléchargés par un objet de données spécifique.
    
- Si vous le souhaitez, modifier la requête de recherche intégrée et réexécuter la recherche pour affiner les résultats de recherche.
    
- Ajouter des recherches de contenu supplémentaires associés au cas DSR. Cela comprend la création de recherches de renvoient des éléments indexés partiellement et journaux générés par le système à partir de mon Analytique et le Service d’itinérance Office.
    
- Exporter des données en réponse à un accès DSR ou d’exportation de demande.
    
- Supprimer le cas lorsque l’enquête DSR est terminée ; Cela supprime toutes les recherches et exporter des tâches associées à la casse.
    
Voici la procédure à suivre pour à l’aide de l’outil DSR pour gérer les enquêtes DSR :
  
[Étape 1 : attribuer des autorisations de découverte électronique aux membres potentiels de cas](#step-1-assign-ediscovery-permissions-to-potential-case-members)

[Étape 2 : Créer un cas de DSR et ajouter des membres](#step-2-create-a-dsr-case-and-add-members)

[Étape 3 : Exécution de la requête de recherche](#step-3-run-the-search-query)

[Étape 4 : Exporter les données](#step-4-export-the-data)

[(Facultatif) Étape 5 : Modifier la requête de recherche intégrées](#optional-step-5-revise-the-built-in-search-query)

[Plus d’informations sur l’utilisation de l’outil DSR](#more-information-about-using-the-dsr-case-tool)
  
> [!IMPORTANT]
> Nos outils peuvent aider les administrateurs access DSR ou l’exportation des demandes en leur permettant d’utiliser la recherche intégrée et d’exporter des fonctionnalités de l’outil DSR. L’outil permet de faciliter une méthode mieux pour exporter les données correspondant à une demande de DSR envoyée par un objet de données. Toutefois, il est important de noter que les résultats de la recherche peuvent varier en fonction de l’objet de données ou les actions d’administration qui peuvent affecter ou non un élément doit être considéré comme « données personnelles » à des fins d’exportation. Par exemple, si l’objet de données a été la dernière personne à modifier un fichier qu’ils n’avez pas créé, le fichier ne peut pas être retourné dans les résultats de recherche. De même, un administrateur peut exporter des données sans inclure les éléments indexés partiellement ou toutes les versions de documents SharePoint. Par conséquent, les outils fournis peuvent aider à faciliter l’accès et d’exportation de requêtes de données ; Toutefois, les résultats sont soumis à des scénarios d’utilisation objet d’administration et de données. 
  
## <a name="step-1-assign-ediscovery-permissions-to-potential-case-members"></a>Étape 1 : attribuer des autorisations de découverte électronique aux membres potentiels de cas

Par défaut, un administrateur général Office 365 peut accéder à l’outil de casse DSR dans la sécurité &amp; centre de conformité. Par conception, les autres utilisateurs, par exemple un responsable de confidentialité des données, un gestionnaire de ressources humaines ou autres personnes impliquées dans les enquêtes DSR n’ont pas accès à l’outil DSR et devront disposer des autorisations appropriées pour accéder à l’outil. Le moyen le plus simple consiste à accéder à la page **autorisations** de sécurité &amp; centre de conformité et ajouter des utilisateurs au groupe de rôles gestionnaire eDiscovery. Notez que vous devez également affecter ces autorisations afin que vous pouvez les ajouter en tant que membres de l’incident DSR que vous créez à l’étape 2. 
  
Pour des instructions détaillées, consultez la rubrique [attribuer des autorisations de sécurité Office 365 eDiscovery &amp; centre de conformité](assign-ediscovery-permissions.md).
  
> [!NOTE]
> Par défaut, un administrateur général Office 365 (ou d’autres membres du groupe de rôles de gestion de l’organisation de la sécurité &amp; centre de conformité ne disposent des autorisations nécessaires pour exporter les résultats de recherche de contenu (voir l’étape 4 dans cet article). Pour contourner ce problème, un administrateur peut ajouter eux-mêmes en tant que membre du groupe de rôles gestionnaire eDiscovery. 
  
## <a name="step-2-create-a-dsr-case-and-add-members"></a>Étape 2 : Créer un cas de DSR et ajouter des membres

L’étape suivante consiste à créer un cas DSR. Lorsque vous créez un cas, vous pouvez choisir de lancer la recherche intégrée ou vous pouvez créer le cas sans démarrer la recherche. La procédure suivante vous demandera pour créer le cas sans lancer la recherche et de vous montrer comment ajouter des membres à la casse.
  
1. Accédez à [https://protection.office.com](https://protection.office.com) et se connecter à Office 365 à l’aide de votre compte professionnel ou de l’école. 
    
2. Dans la sécurité &amp; centre de conformité, cliquez sur la **confidentialité des données** \> **demandes de données de l’objet**, puis cliquez sur ![ajouter une icône](media/ITPro-EAC-AddIcon.gif) **nouveau DSR cas**.
    
3. Dans la page flottant **DSR nouveau cas** , donnez un nom à la casse, tapez une description facultative, puis cliquez sur **suivant**. Notez que le nom du dossier doit être unique au sein de votre organisation.
    
    > [!TIP]
    > Envisagez d’ajouter le nom de la personne qui a envoyé la demande DSR que vous êtes des recherches sur le nom ou la description du nouveau dossier. Notez que seuls les membres de ce cas (administrateurs de découverte électronique) seront en mesure de voir le cas dans la liste des cas sur la page **demandes d’objet de données** . 
  
4. Dans la page **Détails de la demande** , sous **objet de données (la personne qui a archivé cette demande)**, sélectionnez la personne que vous souhaitez rechercher et exporter des données et puis cliquez sur **suivant**.
    
5. Dans la page **Confirmer vos paramètres de cas** , vous pouvez modifier le nom du dossier et la description et sélectionnez un objet de données différents. Dans le cas contraire, cliquez sur **Enregistrer**.
    
    Une page s’affiche qui confirme que le nouveau cas DSR a été créé.
    
    ![Lancer la recherche ou simplement fermer la page cas nouveau DSR](media/b5e62c2c-cafe-4a8d-a38c-789ed9f9ccbd.png)
  
    À ce stade, vous pouvez effectuer une des deux choses :
    
    r. en cliquant sur **Afficher les résultats de la recherche** démarre la recherche. Il s’agit de la sélection par défaut. La recherche intégrée qui est exécutée lorsque vous sélectionnez cette option et les résultats sont retournés sont fournies à l’étape 3.
    
    b. en cliquant sur **Terminer** , le nouveau cas DSR ferme sans démarrer la recherche intégrée. Lorsque vous sélectionnez cette option, le nouveau cas DSR s’affiche dans la page **données de demandes de l’objet** .
    
6. Afin que vous pouvez atteindre le nouveau cas DSR et ajouter des membres, cliquez sur **Terminer** . 
    
7. Dans la page **données de demandes de l’objet** , cliquez sur le nom de l’incident DSR que vous venez de créer. 
    
8. Dans la page Lanceur de **gérer ce cas** , sous **Gérer les membres**, cliquez sur **Ajouter**. 
    
    Sous **utilisateurs**, une liste de personnes qui ont été attribués les autorisations appropriées eDiscovery s’affiche. Notez que les personnes que vous attribué des autorisations de découverte électronique à l’étape 1 seront affiche dans cette liste. 
    
9. Sélectionnez les personnes à ajouter en tant que membres de l’incident DSR et cliquez sur **Ajouter**, puis enregistrez vos modifications.
    
    Notez que vous pouvez également ajouter des groupes de rôle en tant que membres de cas DSR en cliquant sur **Ajouter** sous **Gérer les groupes de rôles**. 
    
## <a name="step-3-run-the-search-query"></a>Étape 3 : Exécution de la requête de recherche

Une fois que vous créez un dossier DSR et ajoutez des membres, l’étape suivante consiste à exécuter la recherche intégrée qui est associé à la casse. Cette requête de recherche par défaut effectue les opérations suivantes :
  
- Recherche toutes les boîtes aux lettres dans votre organisation pour tous les éléments de messagerie qui ont été envoyés ou reçus par l’objet de données. Cette opération s’effectue à l’aide de la propriété email de *Participants* , qui recherche l’objet de données dans tous les champs de personnes dans un message électronique. Cette propriété renvoie les éléments dans lequel l’objet de données est le **à partir de**, **à**, **CC**et **Cci** . Dossiers publics dans Exchange Online sont inclus dans la recherche pour les messages envoyés ou reçus par l’objet de données. 
    
- Recherche dans tous les sites dans votre organisation pour les documents et les éléments qui ont été créés ou téléchargés par l’objet de données. Cette opération s’effectue en utilisant les propriétés suivantes :
    
  - La propriété *Author* renvoie les éléments où l’objet de données est répertorié dans le champ auteur dans les documents Office. Cette valeur est conservée, même si le document est copié et téléchargé par une autre personne. 
    
  - La propriété *CreatedBy* renvoie les éléments qui ont été créés ou téléchargés par l’objet de données. 
    
Voici à quoi ressemble la requête de mot clé pour la recherche intégrée qui est créée automatiquement lorsque vous créez un cas DSR.
  
```
participants:"<email address>" OR author:"<display name>" OR createdby:"<display name>"
```

Par exemple, si le nom de l’objet de données est Ina Leonte, la requête de mot clé se présente comme suit :
  
```
participants:"ina@contoso.com" OR author:"Ina Leonte" OR createdby:"Ina Leonte"
```

 **Pour exécuter la recherche pour un cas DSR intégrée :**
  
1. Dans la sécurité &amp; centre de conformité, cliquez sur la **confidentialité des données** \> de **demandes de données de l’objet**, puis cliquez sur **Ouvrir** en regard de la casse DSR que vous avez créé à l’étape 2. 
    
    Cliquez sur l’onglet de **recherche** en haut de la page, puis cliquez sur la case à cocher en regard de la recherche intégrée qui a été créée lorsque vous avez créé le nouveau cas DSR. Notez que la recherche a le même nom que le cas DSR. 
    
2. Dans la page Lanceur de la recherche, cliquez sur **Ouvrir une requête**.
    
    Lorsque vous ouvrez la requête, la recherche est démarrée et se terminera dans quelques instants. 
    
3. Lors de la recherche est terminée, cliquez sur **Aperçu des résultats** pour afficher un aperçu des résultats de la recherche. Pour plus d’informations, consultez [Aperçu des résultats de recherche](content-search.md#preview-search-results).
    
    > [!TIP]
    > Vous pouvez également afficher les statistiques de requête de recherche pour afficher le nombre de boîtes aux lettres et des éléments de site qui sont renvoyés par la recherche et les emplacements de contenu principaux qui contiennent des éléments qui correspondent à la requête de recherche. Pour plus d’informations, voir [afficher des informations et des statistiques sur une recherche](content-search.md#view-information-and-statistics-about-a-search). 
  
Vous pouvez modifier la requête de recherche intégrée, modifier les emplacements de contenu sont recherchées et relancez la recherche. Pour plus d’informations, consultez [l’étape 5](#optional-step-5-revise-the-built-in-search-query) . 
  
## <a name="step-4-export-the-data"></a>Étape 4 : Exporter les données

Après avoir exécuté la recherche intégrée, vous pouvez exporter les résultats de recherche. Avant d’exporter les données, vous pouvez également à modifier la requête pour réduire le nombre de résultats de recherche. Pour plus d’informations sur la limitation des résultats de la recherche, consultez l’étape 5.
  
Lorsque vous exportez des résultats de la recherche, les éléments de boîte aux lettres peuvent être téléchargés dans des fichiers PST ou sous forme de messages individuels. Lorsque vous exportez le contenu à partir de SharePoint et OneDrive des comptes, les copies des documents Office natifs et d’autres documents sont exportées. Un fichier de résultats qui contient des informations sur chaque élément qui est exporté est également inclus dans les résultats de recherche. Pour plus d’informations sur l’exportation, voir [résultats de la recherche de contenu à exporter à partir de la sécurité du Office 365 &amp; centre de conformité](export-search-results.md).
  
> [!NOTE]
> Par défaut, un administrateur général Office 365 (ou d’autres membres du groupe de rôles de gestion de l’organisation de la sécurité &amp; centre de conformité) ne disposez pas des autorisations nécessaires pour exporter les résultats de recherche de contenu. Pour contourner ce problème, un administrateur peut ajouter eux-mêmes en tant que membre du groupe de rôles gestionnaire eDiscovery. 
  
L’ordinateur que vous utilisez pour exporter des données doit répondre aux exigences système suivantes :
  
- versions 32 ou 64 bits de Windows 7 et versions ultérieures
    
- Microsoft .NET Framework 4.7
    
- un navigateur pris en charge :
    
  - Microsoft Edge
    
    Ou
    
  - Microsoft Internet Explorer 10 et versions ultérieures
    
    > [!NOTE]
    > Microsoft ne fabrique extensions tierces ou les modules complémentaires pour les applications ClickOnce. Exportation des données à l’aide d’un navigateur non pris en charge avec des extensions tierces ou les modules complémentaires n’est pas pris en charge. 
  
 **Pour exporter des données à partir de la recherche dans un cas DSR intégrée :**
  
1. Dans la sécurité &amp; centre de conformité, cliquez sur la **confidentialité des données** \> de **demandes de données de l’objet**, puis cliquez sur **Ouvrir** en regard de la casse DSR que vous souhaitez exporter les données. 
    
2. Cliquez sur l’onglet de **recherche** en haut de la page, puis cliquez sur la case à cocher en regard de la recherche intégrée qui a été créée lorsque vous avez créé le cas DSR. Ou cliquez sur Rechercher un autre pour exporter les données de recherche. 
    
3. Dans la page Lanceur de la recherche, cliquez sur ![icône de résultats de recherche d’exportation](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **plus**, puis sélectionnez **Exporter les résultats** à partir de la liste déroulante. 
    
4. Dans la page **Exporter les résultats** , sélectionnez les options pour les demandes d’exportation DSR de recommandées suivantes. 
    
    ![Configurer les paramètres d’exportation](media/25416b79-57da-46a1-ae07-e640602a8fa4.png)
  
    a. sous **options de sortie**, sélectionnez la première option ( **tous les éléments, à l’exception de ceux dont ceux qui ont un format non reconnu, sont chiffrées ou n’ont pas été indexés pour d’autres raisons**) pour exporter les éléments indexés uniquement. Vous ne voulez pas exporter les éléments partiellement indexées à partir de la recherche intégrée est, car les éléments indexés partiellement à partir d’autres utilisateurs seront exportés. Pour exporter uniquement les éléments indexés partiellement pour l’objet de données, nous vous conseillons de créer une recherche distincte. Pour plus d’informations, voir [exportation partiellement des éléments indexés](manage-gdpr-data-subject-requests-with-the-dsr-case-tool.md#exportunindexeditems) dans la section « Plus d’informations sur l’utilisation de l’outil DSR ».
    
    b. sous **Exchange exporter le contenu en tant que**, sélectionnez la troisième option, **un fichier contenant tous les messages dans un dossier unique**. Étant donné que certaines des résultats peuvent être des éléments à l’origine dans la boîte aux lettres d’un autre utilisateur, cette option répertorie l’élément dans un dossier unique sans indiquer la boîte aux lettres uniquement et est la meilleure option à utiliser lorsque vous supprime les doublons les résultats comme indiqué dans l’élément suivant . Cette option permet également de l’objet de données passez en revue les éléments dans l’ordre chronologique (les éléments sont triés par date d’envoi) sans devoir quitter la structure de dossiers de boîte aux lettres d’origine pour chaque élément.
    
    c. Sélectionnez l’option **Activer la déduplication** pour exclut les messages électroniques en double. Cette option est recommandée car la recherche intégrée recherche toutes les boîtes aux lettres dans votre organisation. Si plusieurs copies du même message figurent dans les boîtes aux lettres qui ont été exclus, cette option signifie qu’une seule copie d’un message doit être exportée. Cette option, ensemble seront messages exportation dans un fichier PST dans un seul dossier entraîne la meilleure expérience utilisateur pour DSR demandes d’exportation. Notez que le rapport d’exportation Results.csv répertorie tous les emplacements où les messages en double ont été détectés.
    
    Si vous le souhaitez, vous pouvez sélectionner **inclure les versions des documents SharePoint** permet d’exporter toutes les versions de documents SharePoint et OneDrive. Cela suppose que le contrôle de version est activé pour les bibliothèques de documents. Cette option permet de vous assurer que toutes les données sont exportées.
    
5. Une fois que vous choisissez les paramètres d’exportation, cliquez sur **Exporter**.
    
    Les résultats de recherche sont préparés pour le téléchargement, ce qui signifie que leur téléchargement dans la zone de stockage Azure pour votre organisation dans le nuage de Microsoft. Les étapes suivantes vous montrent comment télécharger ces données sur votre ordinateur local.
    
6. Cliquez sur l’onglet **Exporter** pour afficher la tâche d’exportation que vous venez de créer. Notez que travaux d’exportation ont le même nom que le correspondant de recherche avec **_Export** ajouté à la fin du nom de la recherche. 
    
7. Cliquez sur la tâche d’exportation que vous venez de créer pour afficher la page flottant exporter. Cette page affiche des informations sur la recherche, tels que la taille et le nombre total d’éléments à exporter et le pourcentage des éléments qui ont été transférés vers une zone de stockage Azure. Cliquez sur **Actualiser** pour mettre à jour les informations d’état de téléchargement. 
    
8. **Exporter la clé**, cliquez sur **Copier dans le Presse-papiers**. Vous allez utiliser cette clé à l’étape 11 pour télécharger les résultats de recherche.
    
9. Cliquez sur ![icône de résultats de recherche d’exportation](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **télécharger les résultats** en haut de la page flottant exporter. 
    
10. Dans la fenêtre contextuelle en bas de la page, cliquez sur **Ouvrir** pour ouvrir **découverte électronique outil d’exportation de Microsoft Office 365**. L' **outil d’exportation de découverte électronique** sera installé la première fois que vous téléchargez des résultats de la recherche. 
    
11. Dans l' **outil d’exportation de découverte électronique**, collez la clé d’exportation que vous avez copié à l’étape 8 dans la zone appropriée.
    
12. Cliquez sur **Parcourir** pour spécifier l’emplacement de téléchargement du fichier des résultats de recherche. 
    
    > [!NOTE]
    > En raison de la quantité élevée de l’activité du disque (lectures et écritures), vous devez télécharger les résultats de la recherche sur un disque dur local ; ne pas les télécharger vers un lecteur réseau mappé ou un emplacement réseau. 
  
13. Cliquez sur **Démarrer** pour télécharger les résultats de recherche sur votre ordinateur. 
    
    L' **outil d’exportation de découverte électronique** affiche les informations sur le processus d’exportation, y compris une estimation du nombre (et taille) des autres éléments à télécharger. Une fois le processus d’exportation terminée, vous pouvez accéder les fichiers à l’emplacement où ils ont été téléchargés. Pour plus d’informations sur les rapports inclus lorsque vous téléchargez des résultats de la recherche de contenu, voir la section [plus d’informations](export-search-results.md#more-information) dans « résultats de la recherche de contenu d’exportation à partir de la sécurité Office 365 &amp; centre de conformité ». 
    
Une fois que les données sont exportées, les résultats de la recherche et les rapports d’exportation sont situés dans un dossier qui a le même nom que le cas DSR. Les fichiers PST contenant des éléments de boîte aux lettres se trouvent dans un sous-dossier nommé **Exchange**. Documents et autres éléments à partir des sites se trouvent dans un sous-dossier nommé **SharePoint**. 
  
## <a name="optional-step-5-revise-the-built-in-search-query"></a>(Facultatif) Étape 5 : Modifier la requête de recherche intégrées

Après avoir exécuté la recherche intégrée, vous pouvez le modifier pour limiter l’étendue pour renvoyer le nombre de résultats de recherche. Vous pouvez procéder en ajoutant des conditions à la requête. Une condition est logiquement connectée à la requête de mot clé par l’opérateur **AND** . Par conséquent être renvoyé dans les résultats de recherche, les éléments doivent satisfaire à la fois la requête de mot clé et les conditions que vous ajoutez. Voici comment aider des conditions pour affiner les résultats. Si vous ajoutez deux ou plusieurs conditions uniques à une requête de recherche (les conditions qui spécifient les différentes propriétés), ces conditions sont logiquement connectées par l’opérateur **AND** . Cela signifie que seuls les éléments qui satisfont à toutes les conditions (en plus de la requête de mot clé) sont retournés. Si vous ajoutez plusieurs valeurs (séparés par des virgules ou des points-virgules) à une seule condition, ces valeurs sont connectés par l’opérateur **OR** . Cela signifie que les éléments sont retournés si elles contiennent toutes les valeurs de la propriété de la condition spécifiées. 
  
Voici quelques exemples de conditions que vous pouvez ajouter à la requête de recherche intégrée d’un cas de DSR. Le nom de la propriété réelle utilisée dans une requête de recherche est affiché entre parenthèses.
  
- **Type de fichier ( `filetype`)** -Spécifie l’extension d’un document ou un fichier. Cette condition permet de rechercher des documents et fichiers créés par des applications Office spécifiques, telles que Word, Excel et OneNote. 
    
- **Type de message ( `kind`)** -Spécifie le type d’élément de messagerie à rechercher. Par exemple, vous pouvez utiliser la syntaxe `kind:email OR kind:im` pour renvoyer uniquement les messages électroniques et Skype pour des conversations ou les salles de conversation dans Microsoft Teams. 
    
- **Balise de conformité (`compliancetag`)** -spécifie une étiquette affectée à un message électronique ou un document. Cette condition renvoie les éléments qui sont classés avec une étiquette spécifique. Étiquettes servent à classer les e-mails et documents pour la gouvernance des données et appliquer les règles de rétention en fonction de la classification définie par l’étiquette. Il s’agit d’une condition utile pour les enquêtes DSR, car votre organisation peut-être utiliser des étiquettes de classer le contenu relatif à la confidentialité des données ou contenant des données personnelles ou des informations sensibles. Pour la valeur de cette condition, utilisez le nom d’étiquette complète ou la première partie du nom d’étiquette avec un caractère générique. Pour plus d’informations, voir [vue d’ensemble des étiquettes dans Office 365](labels.md).
    
Pour une liste et une description de toutes les conditions disponibles dans l’outil DSR, voir [conditions de recherche](keyword-queries-and-search-conditions.md#search-conditions) dans l’article « requêtes de mot clé et conditions de recherche pour la recherche de contenu ». 
  
### <a name="changing-the-content-locations-that-are-searched"></a>Modification des emplacements de contenu qui sont recherchés

En plus de révision de la recherche d’un cas de DSR intégrée, vous pouvez également modifier les emplacements de contenu sont recherchés. Comme expliqué précédemment, la recherche intégrée recherche chaque boîte aux lettres et les sites dans l’organisation et des dossiers publics Exchange Online. Par exemple, vous pouvez affiner la recherche pour rechercher uniquement des boîtes aux lettres et le compte OneDrive de l’objet de données et les sites SharePoint sélectionnés. Si vous choisissez de rechercher des sites spécifiques, vous devez ajouter chaque site que vous souhaitez rechercher.
  
Pour modifier les emplacements de contenu à rechercher :
  
1. Ouvrez la recherche intégrée que vous souhaitez modifier les emplacements de contenu.
    
2. Dans la requête de recherche, sous **emplacements**, cliquez sur **Modifier** en regard de l’option **des emplacements spécifiques** . 
    
    ![Cliquez sur Modifier pour modifier les emplacements de contenu de la requête de recherche intégrées](media/d66f7ba7-b71f-4ff5-a030-460ff02e3123.png)
  
    La page Lanceur de **modifier des sites** s’affiche. Voici une description des emplacements de contenu dans la recherche intégrée et certaines informations sur la modification les emplacements dans lesquels sont recherchées. 
    
    ![Modifier les emplacements flottant page](media/56c033f6-6735-46ba-abb2-a263a2b79836.png)
  
    a la bascule sous **Sélectionner tout** dans la section de boîte aux lettres en haut de la page flottant est sélectionnée, ce qui indique que toutes les boîtes aux lettres sont recherchés. Pour limiter l’étendue de la recherche, cliquez sur le bouton pour la désactiver, puis cliquez sur **Choisir des utilisateurs, des équipes ou des groupes** et choisissez les boîtes aux lettres spécifiques à rechercher.
    
    b. la bascule sous **Sélectionner tout** dans la section sites au milieu de la page flottant est sélectionnée, ce qui indique que tous les sites sont recherchés. Pour limiter la recherche aux sites sélectionnés, vous désactivez la bascule et puis cliquez sur **Choisir les sites**. Vous devrez ajouter chaque site spécifique que vous souhaitez effectuer une recherche, y compris le compte OneDrive de l’objet données.
    
    c. la bascule dans la section de dossiers publics Exchange est sélectionnée, ce qui signifie que tous les dossiers publics Exchange sont recherchés. Notez que vous ne pouvez rechercher tous les dossiers publics Exchange ou aucun d'entre eux. Vous ne pouvez pas choisir ceux spécifiques à rechercher.
    
3. Si vous modifiez les emplacements de contenu dans la recherche, cliquez sur **Enregistrer &amp; exécuter** pour redémarrer la recherche. 
  
## <a name="more-information-about-using-the-dsr-case-tool"></a>Plus d’informations sur l’utilisation de l’outil DSR

Les sections suivantes contiennent plus d’informations sur l’utilisation de l’outil DSR pour répondre aux demandes d’exportation DSR.
  
[Exportation des données à partir de MyAnalytics et le Service d’itinérance Office](#exporting-data-from-myanalytics-and-the-office-roaming-service)

[Exportation d’éléments indexés partiellement](#exporting-partially-indexed-items)

[Recherche et exportation de données à partir de Microsoft Teams et groupes d’Office 365](#searching-and-exporting-data-from-microsoft-teams-and-office-365-groups)

[Rechercher des dossiers publics Exchange](#searching-exchange-public-folders)
  
### <a name="exporting-data-from-myanalytics-and-the-office-roaming-service"></a>Exportation des données à partir de MyAnalytics et le Service d’itinérance Office

Vous pouvez utiliser l’outil DSR pour rechercher et exporter des données d’utilisation qui sont générées par MyAnalytics et le Service d’itinérance Office. Voici une description de ce que ces services :
  
- **MyAnalytics** - permet aux utilisateurs d’informations sur la façon dont ils passent leur temps, basées sur les données de messagerie et calendrier dans leur boîte aux lettres. Toutes les analyses MyAnalytics proviennent des en-têtes de courriers électroniques et de la réunion dans la boîte aux lettres de l’utilisateur. Les utilisateurs qui bénéficient d’une licence MyAnalytics peuvent se connecter à Office 365 et accédez au tableau de bord MyAnalytics pour afficher les analyses sur comment ils passent leur temps. (Les utilisateurs peuvent captures d’écran de ces informations en réponse à une demande d’accès DSR). La recherche intégrée dans un cas DSR servant à exporter les données qui sont utilisées pour générer des idées MyAnalytics. 
    
- **Service d’itinérance office** - itinérance est un service qui stocke les paramètres liés à Office, telles que le thème Office, dictionnaire personnalisé, les paramètres de langue, mode développeur et correction automatique. 
    
Les données à partir de MyAnalytics et le service d’itinérance d’Office sont stockées dans la boîte aux lettres d’un objet de données dans des dossiers cachés situé dans une sous-arborescence (non-IPM) de message non interpersonnel de boîtes aux lettres Exchange Online. Cela signifie que les données sont masquées à partir de la vue de l’utilisateur lorsqu’ils utilisent Outlook ou autres clients de messagerie pour accéder à leur boîte aux lettres. Pour plus d’informations sur les dossiers cachés, voir [Dossiers cachés MAPI](https://go.microsoft.com/fwlink/?linkid=872758).
  
Vous pouvez créer une recherche de contenu distincte (et l’associer à un cas DSR) qui retourne le MyAnalytics et les données d’utilisation dans la boîte aux lettres de sujets des données Service d’itinérance Office. Ces données n’est pas incluses dans les statistiques de recherche et il n’est pas disponible pour l’aperçu. Mais vous pouvez l’exporter et puis attribuez-lui l’objet de données en réponse à une demande d’exportation DSR.
  
Lorsque vous exportez des données à partir de MyAnalytics et le Service d’itinérance Office, les données sont enregistrées dans un dossier distinct pour chaque application qui se trouve dans le dossier **ApplicationDataRoot** , qui se trouve dans un dossier qui est le nom et d’adresse de messagerie de l’objet de données. Ces données sont exportées en tant que fichiers JSON, qui sont des fichiers texte explicite similaires au format XML ou TXT, qui sont joints aux messages électroniques. Actuellement, ces dossiers sont nommés avec un identificateur global unique (GUID) qui est affecté à MyAnalytics et le Service d’itinérance Office, qui sont répertoriés dans le tableau suivant. Dans les futures versions de l’outil de casse DSR, le GUID est remplacé par le nom de l’application. 
  
|**Application**|**Nom du GUID/dossier**|
|:-----|:-----|
|MyAnalytics  <br/> |3c896ded-22c5-450F-91f6-3d1ef0848f6e  <br/> |
|Service d’itinérance Office  <br/> |1caee58f-eb14-4a6b-9339-1fe2ddf6692b  <br/> |
   
 **Pour rechercher et exporter des données MyAnalytics et Service d’itinérance Office :**
  
1. Dans la sécurité &amp; centre de conformité, cliquez sur la **confidentialité des données** \> de **demandes de données de l’objet**, puis cliquez sur **Ouvrir** en regard de la casse DSR pour l’objet de données que vous souhaitez exporter les données d’utilisation. 
    
2. Cliquez sur l’onglet de **recherche** en haut de la page, puis cliquez sur ![ajouter une icône](media/ITPro-EAC-AddIcon.gif) **Recherche interactive**.
    
3. Dans la page **nom de la recherche** , cliquez sur **Annuler** . 
    
4. Sous la **requête de recherche**, dans la condition de **Type** , sélectionnez les cases à cocher en regard de **MyAnalytics** et **Service d’itinérance Office**. 
    
    ![Sélectionnez les cases à cocher MyAnalytics et Service d’itinérance Office pour exporter les données d’utilisation](media/3dacbc7a-c314-492c-828c-6757fda84963.png)
  
    Notez que la condition de **Type** (qui sont des classes de messages électroniques) doit être le seul élément dans la requête de recherche. Vous pouvez supprimer de la zone **mots clés** ou laissez ce champ vide. 
    
5. Sous **emplacements**, assurez-vous que **des emplacements spécifiques** est sélectionné, puis sur **Modifier**.
    
6. Dans la partie supérieure de la page Lanceur de **modifier des sites** (section de la boîte aux lettres), cliquez sur **Choisir des utilisateurs, des équipes ou des groupes**.
    
7. Dans la page **Modifier les emplacements** , cliquez sur **Choisir des utilisateurs, des équipes ou des groupes**, cliquez sur boîte aux lettres de l’objet de données, puis enregistrez votre sélection. 
    
8. Cliquez sur **Enregistrer &amp; exécuter**et nom de la recherche, puis enregistrez-le.
    
    La recherche est lancée.
    
 **Pour exporter des données MyAnalytics et Service d’itinérance Office :**
  
1. Lors de la recherche que vous avez créé à l’étape précédente est terminée, cliquez sur l’onglet de **recherche** en haut de la page, puis cliquez sur la case à cocher en regard de la recherche. Vous devrez peut-être cliquez sur ![Actualiser](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png) **Actualiser** pour afficher la recherche. 
    
2. Dans la page Lanceur de la recherche, cliquez sur ![icône de résultats de recherche d’exportation](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **plus**, puis sélectionnez **Exporter les résultats** à partir de la liste déroulante. 
    
3. Dans la page **Exporter les résultats** , sélectionnez ces options pour exporter les données d’utilisation recommandées. 
    
    ![Options d’exportation lors de l’exportation des données d’utilisation MyAnalytics et Service d’itinérance Office](media/470a7d1e-eeae-4b42-95aa-15cb82ce2f68.png)
  
    a. sous **options de sortie**, sélectionnez la première option ( **tous les éléments, à l’exception de ceux dont ceux qui ont un format non reconnu, sont chiffrées ou n’ont pas été indexés pour d’autres raisons**) pour exporter les éléments indexés uniquement.
    
    b. sous **Exchange exporter le contenu en tant que**, sélectionnez la seconde option, **un fichier contenant tous les messages**.
    
    c. Laissez les autres options d’exportation non sélectionnées.
    
4. Une fois que vous choisissez les paramètres d’exportation, cliquez sur **Exporter**.
    
    Les résultats de recherche sont préparés pour le téléchargement, ce qui signifie que leur téléchargement dans la zone de stockage Azure pour votre organisation dans le nuage de Microsoft. Les étapes suivantes vous montrent comment télécharger ces données sur votre ordinateur local.
    
5. Cliquez sur l’onglet **Exporter** pour afficher la tâche d’exportation que vous venez de créer. Notez que travaux d’exportation ont le même nom que le correspondant de recherche avec **_Export** ajouté à la fin du nom de la recherche. 
    
6. Cliquez sur la tâche d’exportation que vous venez de créer pour afficher la page flottant exporter. 
    
7. **Exporter la clé**, cliquez sur **Copier dans le Presse-papiers**. Vous allez utiliser cette clé à l’étape 10 pour télécharger les résultats de recherche.
    
8. Cliquez sur ![icône de résultats de recherche d’exportation](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **télécharger les résultats** en haut de la page flottant exporter. 
    
9. Dans la fenêtre contextuelle en bas de la page, cliquez sur **Ouvrir** pour ouvrir **découverte électronique outil d’exportation de Microsoft Office 365**. L' **outil d’exportation de découverte électronique** sera installé la première fois que vous téléchargez des résultats de la recherche. 
    
10. Dans l’**outil d’exportation de découverte électronique**, collez la clé d’exportation que vous avez copiée à l’étape 7 dans la zone appropriée.
    
11. Cliquez sur **Parcourir** pour spécifier l’emplacement de téléchargement du fichier des résultats de recherche. 
    
    > [!NOTE]
    > En raison de la quantité élevée de l’activité du disque (lectures et écritures), vous devez télécharger les résultats de la recherche sur un disque dur local ; ne pas les télécharger vers un lecteur réseau mappé ou un emplacement réseau. 
  
12. Cliquez sur **Démarrer** pour télécharger les résultats de recherche sur votre ordinateur. 
    
    L' **outil d’exportation de découverte électronique** affiche les informations sur le processus d’exportation, y compris une estimation du nombre (et taille) des autres éléments à télécharger. Une fois le processus d’exportation terminée, vous pouvez ouvrir le fichier PST Exchange dans Outlook et accédez au dossier **ApplicationDataRoot** pour accéder aux sous-dossiers service MyAnalytics et itinérance. 
    
    Comme expliqué précédemment, les fichiers JSON qui contient les données d’utilisation sont joints aux messages. Pour afficher un fichier JSON, cliquez sur un message, puis ouvrez le fichier joint JSON. 
  
### <a name="exporting-partially-indexed-items"></a>Exportation d’éléments indexés partiellement

Il est recommandé que vous ne pas exporter les éléments partiellement indexés (également appelés éléments non indexés) de la recherche intégrée qui est créée lorsque vous créez un nouveau cas DSR. C’est parce que la recherche résultats inclura probablement partiellement indexé d’éléments pour d’autres utilisateurs dans votre organisation et pas seulement partiellement les éléments indexés pour l’objet de données). Au lieu de cela, nous vous conseillons de créer une recherche de contenu distincte qui est associé à la casse DSR conçue pour exporter uniquement les éléments indexés partiellement liées à l’objet de données. 
  
Voici un processus de haut niveau pour exporter les éléments indexés partiellement. Une fois qu’ils vous exporter, vous pouvez les consulter pour déterminer si un élément est réactif à un accès DSR ou exporter la demande.
  
1. Ouvrez le cas DSR et créer une nouvelle recherche sur la page de **recherche** . 
    
2. Utilisez les critères suivants pour configurer la requête de recherche et les emplacements de contenu à rechercher :
    
    - Utiliser une requête de mot clé vide/vide. Elle retournera tous les éléments dans les emplacements de contenu sont recherchés.
    
    - Recherche uniquement les lettres Exchange Online de l’objet de données et leur compte OneDrive.
    
3. Après avoir exécuté la recherche, et elle est terminée, vous pouvez exporter et télécharger les résultats de recherche (comme décrit à [l’étape 4](#step-4-export-the-data)). Utilisez les paramètres suivants pour exporter les éléments indexés partiellement. 
    
    - Sous **options de sortie**, sélectionnez la troisième option ( **uniquement les éléments qui ont un format non reconnu, sont chiffrées, ou n’ont pas été indexés pour d’autres raisons**) pour exporter les éléments indexés partiellement uniquement.
    
    - Sous **contenu Exchange exporter en tant que**, vous pouvez sélectionner une option selon vos préférences. 
    
    - Sélection de l’option **inclure les versions des documents SharePoint** servant à exporter les versions des documents si une version est partiellement indexée. 
    
Pour plus d’informations sur les éléments indexés partiellement, voir : 
  
- [Éléments partiellement indexés dans la recherche de contenu dans Office 365](partially-indexed-items-in-content-search.md)

- [Exportation d’éléments indexés partiellement](export-search-results.md#exporting-partially-indexed-items)
    
### <a name="searching-and-exporting-data-from-microsoft-teams-and-office-365-groups"></a>Recherche et exportation de données à partir de Microsoft Teams et groupes d’Office 365

Conversations qui font partie de la liste de conversation dans Microsoft Teams (appelée conversations d’équipe ou les salles de conversation) sont stockées dans la boîte aux lettres Exchange Online des utilisateurs qui participent à la conversation. En outre, les fichiers de qu'une personne partage dans une salle de conversation sont stockés dans le compte OneDrive de la personne qui partage le fichier. Parce que la recherche intégrée recherche tous les comptes de OneDrive et les boîtes aux lettres dans l’organisation, l’équipe conversations et les documents partagés dans une session de conversation (l’objet de données créés ou téléchargés) seront renvoyés par la recherche intégrée dans un cas DSR.
  
Vous pouvez également conversations qui font partie d’un canal d’équipes (également appelé messages canal) sont stockées dans la boîte aux lettres qui est associé à une équipe. Ces types de conversations qui a participé à l’objet de données sont également renvoyés par la recherche intégrée, car toutes les boîtes aux lettres associées Teams Microsoft sont recherchés. En outre, les mosaïques un objet de données peut avoir partagé dans un canal d’équipes sont stockés sur le site SharePoint de l’équipe. Les fichiers créés ou uploadedby l’objet de données s’afficheront par la recherche intégrée dans un cas DSR, car les sites associés à Microsoft Teams sont inclus dans la recherche.
  
De même, les boîtes aux lettres et des sites SharePoint qui correspondent à un groupe d’Office 365 sont également inclus dans la recherche intégrée. Cela signifie que la messagerie les messages où envoyé ou reçu par l’objet de données et fichiers créés ou téléchargés par l’objet de données seront retournés. 
  
Pour plus d’informations sur l’utilisation de la recherche de contenu pour rechercher des éléments dans Microsoft Teams et Office 365 groupes ou pour savoir comment obtenir une liste de membres, consultez la section « Recherche Microsoft équipes et Office 365 groupes » de la [Recherche de contenu dans Office 365](content-search.md#searching-microsoft-teams-and-office-365-groups). 
  
### <a name="searching-exchange-public-folders"></a>Rechercher des dossiers publics Exchange

La recherche intégrée dans un cas DSR sera e-mails retour uniquement que l’objet de données envoyées à un dossier public à extension messagerie ou des messages que quelqu'un d’autre envoyé à un dossier public et aussi copiés de l’objet de données. Elle ne renvoie pas de message que l’objet de données peut avoir publié dans un dossier public. Pour rechercher des éléments de l’objet de données publié dans un dossier public, vous pouvez créer un distinct créer une recherche de contenu distincte qui recherche n’importe quel élément publié dans un dossier public à l’objet de données.
  
Voici un processus de haut niveau pour rechercher des éléments de l’objet de données peut avoir publié dans un dossier public. 
  
1. Ouvrez le cas DSR et créer une nouvelle recherche sur la page de **recherche** . 
    
2. Utilisez les critères suivants pour configurer la requête de recherche et les emplacements de contenu à rechercher :
    
  - Dans la zone **mots clés** , utilisez la requête de recherche suivantes : 
    
    ```
    itemclass:ipm.post AND "<email address of the data subject>"
    ```

  - Rechercher tous les dossiers publics Exchange
    
  - Après avoir exécuté la recherche, et elle est terminée, vous pouvez exporter et télécharger les résultats de recherche (comme décrit à [l’étape 4](manage-gdpr-data-subject-requests-with-the-dsr-case-tool.md#step4)). Utilisez les paramètres suivants pour exporter les éléments indexés partiellement. 
