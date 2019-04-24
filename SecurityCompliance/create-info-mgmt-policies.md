---
title: Créer et appliquer des stratégies de gestion des informations
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 5/16/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
- OSU150
- OSU160
- MET150
ms.assetid: 8ccac9e4-3a50-49fa-a95b-d186032a6ee3
ms.collection:
- M365-security-compliance
description: Les stratégies de gestion des informations permettent à votre organisation de contrôler la durée de conservation du contenu, d'auditer les opérations effectuées par les utilisateurs et d'ajouter des codes-barres ou des étiquettes aux documents. Une stratégie peut contribuer à renforcer la conformité aux réglementations juridiques et gouvernementales ou aux processus d'entreprise internes. En tant qu'administrateur, vous pouvez configurer une stratégie pour contrôler le suivi des documents et la durée de conservation des documents.
ms.openlocfilehash: 1d17dd8cadb721478831ab8fe77413c08f959f29
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32258840"
---
# <a name="create-and-apply-information-management-policies"></a>Créer et appliquer des stratégies de gestion des informations

Les stratégies de gestion des informations permettent à votre organisation de contrôler la durée de conservation du contenu, d'auditer les opérations effectuées par les utilisateurs et d'ajouter des codes-barres ou des étiquettes aux documents. Une stratégie peut contribuer à renforcer la conformité aux réglementations juridiques et gouvernementales ou aux processus d'entreprise internes. En tant qu'administrateur, vous pouvez configurer une stratégie pour contrôler le suivi des documents et la durée de conservation des documents.
  
Vous pouvez créer une stratégie de gestion des informations sur trois emplacements différents dans la hiérarchie du site, du plus large au plus étroit:
  
- Créer une stratégie à utiliser sur plusieurs types de contenu au sein d'une collection de sites.
    
- Créer une stratégie pour un type de contenu de site.
    
- Créer une stratégie pour une liste ou une bibliothèque.
    
Pour plus d'informations, consultez la rubrique [Présentation des stratégies de gestion des informations](intro-to-info-mgmt-policies.md).
  
## <a name="create-a-policy-for-multiple-content-types-within-a-site-collection"></a>Créer une stratégie pour plusieurs types de contenu au sein d'une collection de sites
<a name="__toc261001590"> </a>

Pour vous assurer qu'une stratégie d'informations est appliquée à tous les documents d'un certain type au sein d'une collection de sites, envisagez de créer la stratégie au niveau de la collection de sites, puis appliquez la stratégie aux types de contenu. Il s'agit des stratégies de collection de sites. 
  
1. dans le bouton paramètres de la \> ****![page d'accueil de la collection de sites SharePoint 2016 paramètres de la barre de titre.](media/1c22d2d8-39e0-4930-82c6-c3eee44211d3.png) \>**Paramètres de site**.
    
    Dans un site connecté à un groupe SharePoint, cliquez sur **paramètres**, sur **contenu du site**, puis sur **paramètres du site**. 
    
2. Sur la page Paramètres du site, sous **modèles de stratégies de type de contenu**administration \> de la collection de **sites** . 
  
![Lien de modèle de stratégie de type de contenu sur la page Paramètres du site](media/26d3466a-23ec-443f-88f0-2aaff38e992b.png)
  
3. Sur la page \> stratégies, **créez**. 
    
4. Entrez un nom et une description pour la stratégie, puis rédigez une brève déclaration de stratégie qui explique aux utilisateurs ce à quoi la stratégie est destinée.
    
5. Consultez la section suivante sur la création de stratégies pour un type de contenu de site pour découvrir comment configurer les fonctionnalités que vous souhaitez associer à la stratégie. 
    
6. Sélectionnez **OK**.
    
## <a name="create-a-policy-for-a-site-content-type"></a>Créer une stratégie pour un type de contenu de site
<a name="__create_a_policy"> </a>

L'ajout d'une stratégie de gestion des informations à un type de contenu facilite l'Association de fonctionnalités de stratégie à plusieurs listes ou bibliothèques. Vous pouvez choisir d'ajouter une stratégie de gestion des informations existante à un type de contenu ou de créer une stratégie unique spécifique à un type de contenu individuel.
  
 Vous pouvez également ajouter une stratégie de gestion des informations à un type de contenu spécifique à des listes. Cela a pour effet d'appliquer la stratégie uniquement aux éléments de cette liste qui utilisent le type de contenu. 
  
1. dans le bouton paramètres de la \> ****![page d'accueil de la collection de sites SharePoint 2016 paramètres de la barre de titre.](media/1c22d2d8-39e0-4930-82c6-c3eee44211d3.png) \>**Paramètres de site**.
    
    Dans un site connecté à un groupe SharePoint, cliquez sur **paramètres**, sur **contenu du site**, puis sur **paramètres du site**. 
    
2. Sur la page Paramètres du site, sous **types de contenu de site**des galeries \> du **Concepteur Web** .
  
![Lien de types de contenu de site sur la page Paramètres du site](media/6f6fa51f-15d7-4782-b06f-a7b36e874cd3.png)
  
3. Sur la page Paramètres de type de contenu de site, sélectionnez le type de contenu auquel vous souhaitez ajouter une stratégie.
    
4. Sur la page type de contenu de site **** \> , sous paramètres de la **stratégie de gestion des informations**.
    
5. Sur la page modifier la stratégie, entrez un nom et une description pour la stratégie, puis rédigez une brève description expliquant aux utilisateurs ce à quoi la stratégie est destinée.
    
6. Dans les sections suivantes, sélectionnez les fonctionnalités de stratégie individuelles que vous souhaitez ajouter à votre stratégie de gestion des informations. 
  
![Types de stratégies de contenu](media/19fcb8a3-974b-40d3-a13f-b76088d122f8.png)
  
7. Pour spécifier une période de rétention pour les documents et les éléments qui sont soumis à cette stratégie, choisissez **activer**la rétention, puis spécifiez la période de rétention et les actions que vous souhaitez voir se produire à l'expiration des éléments.
    
    Pour spécifier une période de rétention
    
||||||**1.**|* * Sélectionnez * * Ajouter une étape de rétention pour les enregistrements... * * * *|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
||||||2.  <br/> | Sélectionnez une option de période de rétention pour spécifier quand des documents ou des éléments sont configurés pour expirer. Effectuez l’une des opérations suivantes :  <br/>  Pour définir la date d'expiration sur la base d'une propriété de date, sous **événement** \> **cette étape est basée sur une propriété de date sur l'élément**, puis sélectionnez l'action de document ou d'élément (par exemple, créé ou modifié) et l'incrément du temps après cette action ( par exemple, le nombre de jours, de mois ou d'années, lorsque vous souhaitez que l'élément expire.  <br/>  Pour utiliser une formule de rétention personnalisée afin de déterminer l'expiration, choisissez **définir par une formule de rétention personnalisée installée sur ce serveur**.  <br/> > [!NOTE]> cette option n'est disponible que si une formule personnalisée a été configurée par votre administrateur.           |
||||||3.  <br/> |L'option **Démarrer un flux de travail** est disponible uniquement si vous définissez une stratégie pour une liste, une bibliothèque ou un type de contenu auquel un flux de travail est déjà associé. Vous aurez alors un choix de flux de travail parmi lesquels choisir.  <br/> |
||||||4.  <br/> |Dans la section **périodicité** , sélectionnez **répéter l'action de cette étape...** et entrez la fréquence à laquelle vous souhaitez que l'action se produise.  <br/> > [!NOTE]> cette option n'est disponible que si l'action que vous avez sélectionnée peut être répétée. Par exemple, vous ne pouvez pas définir la récurrence de l'action **Supprimer définitivement**.           |
||||||5.  <br/> |Choisissez **OK**.  <br/> |
   
1. Pour activer l'audit pour les documents et les éléments qui sont soumis à cette stratégie, sélectionnez **activer l'audit**, puis spécifiez les événements que vous souhaitez auditer.
    
    Pour activer l'audit
    
||||||1. * * * *|Sur la page modifier la stratégie, * * **sous** **Auditing** **\>** **activer l'audit** * *, puis activez les cases à cocher en regard des événements pour lesquels vous souhaitez conserver une trace d'audit. * * * *|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
||||||**2.** <br/> |**Pour inviter les utilisateurs à insérer ces codes-barres dans des documents,** **Sélectionnez** **Inviter les utilisateurs à insérer un code-barres avant l'enregistrement ou l'impression** **.** <br/> |
||||||**3.** <br/> |**Sélectionnez** **OK** * * pour appliquer la fonctionnalité d'audit à la stratégie. ** <br/> |
|||||||La fonctionnalité de stratégie d'audit permet aux organisations de créer et d'analyser des suivis d'audit pour des documents et de répertorier des éléments tels que des listes de tâches, des listes de problèmes, des groupes de discussion et des calendriers. Cette fonctionnalité de stratégie fournit un journal d'audit qui enregistre les événements, par exemple lors de l'affichage, de la modification ou de la suppression du contenu.  <br/> |
|||||||Lorsque l'audit est activé dans le cadre d'une stratégie de gestion des informations, les administrateurs peuvent afficher les données d'audit dans des rapports d'utilisation des stratégies basés dans Microsoft Excel et qui résument l'utilisation actuelle. Les administrateurs peuvent se servir de ces rapports pour déterminer comment l'information est utilisée dans l'organisation. Ces rapports peuvent également aider les organisations à vérifier et à documenter leur conformité réglementaire ou à étudier les préoccupations potentielles.  <br/> |
|||||||Le journal d'audit enregistre les informations suivantes: nom de l'événement, date et heure de l'événement et nom du système de l'utilisateur qui a effectué l'action.  <br/> |
   
1. Lorsque des codes-barres sont activés dans le cadre d'une stratégie, ils sont ajoutés aux propriétés du document et s'affichent dans la zone d'en-tête du document auquel le code-barres est appliqué. Comme les étiquettes, les codes-barres peuvent également être supprimés manuellement d'un document. Vous pouvez spécifier si les utilisateurs doivent être invités à inclure le code-barres lors de l'impression ou de l'enregistrement d'un élément ou si le code-barres doit être inséré manuellement à l'aide de l'onglet **Insérer** dans les programmes de version Office 2010. 
    
    Pour activer les codes-barres
    
||||||1. * * * *|**Sur la page modifier la stratégie, sous **codes-barres** \> , **activez les codes-barres**.**|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
||||||**2.** <br/> |Pour inviter les utilisateurs à insérer ces codes-barres dans les documents, choisissez **inviter les utilisateurs à insérer un code-barres avant l'enregistrement ou l'impression**.  <br/> |
||||||**3.** <br/> |Choisissez **OK** pour appliquer la fonctionnalité de code-barres à la stratégie.  <br/> |
|||||||
 La stratégie code-barres génère le code 39 codes-barres standard. Chaque image de code-barres inclut le texte sous le symbole de code-barres qui représente la valeur de code-barres. Cela permet d'utiliser les données de code-barres même lorsque le matériel d'analyse n'est pas disponible. Les utilisateurs peuvent taper manuellement le numéro de code-barres dans la zone de recherche pour Rechercher l'élément sur un site.  <br/> |
   
1. Pour exiger que les documents soumis à cette stratégie aient des étiquettes, choisissez **activer les étiquettes**, puis spécifiez les paramètres souhaités pour les étiquettes.
    
    Pour activer les étiquettes
    
||||||**1.**|* * Pour obliger les utilisateurs à ajouter une étiquette à un document, choisissez **inviter les utilisateurs à insérer une étiquette avant l'enregistrement ou l'impression**.  <br/> > [!NOTE]> si vous souhaitez que les étiquettes soient facultatives, n'activez pas cette case à cocher.        **|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
||||||2.  <br/> |Pour verrouiller une étiquette de sorte qu'elle ne puisse pas être modifiée une fois qu'elle a été insérée, choisissez **empêcher les modifications apportées aux étiquettes une fois qu'elles**ont été ajoutées.  <br/>  Ce paramètre empêche la mise à jour du texte de l'étiquette une fois que l'étiquette a été insérée dans un élément au sein d'une application cliente telle que Word, Excel ou PowerPoint. Si vous souhaitez que l'étiquette soit mise à jour lorsque les propriétés de ce document ou de cet élément sont mises à jour, n'activez pas cette case à cocher.  <br/> |
||||||3.  <br/> |Dans la zone format d'étiquette, entrez le texte de l'étiquette tel qu'il doit s'afficher. Les étiquettes peuvent contenir jusqu'à 10 références de colonnes, chacune pouvant comporter jusqu'à 255 caractères. Pour créer le format de votre étiquette, procédez comme suit:  <br/> Tapez les noms des colonnes que vous souhaitez inclure dans l'étiquette dans l'ordre dans lequel vous souhaitez les voir apparaître. Placez les noms de colonne entre accolades ({}), comme indiqué dans l'exemple de la page modifier la stratégie.  <br/> Tapez des mots pour identifier les colonnes en dehors des crochets, comme indiqué dans l'exemple de la page modifier la stratégie.  <br/> |
||||||4.  <br/> |Pour ajouter un saut de ligne, entrez **\n** à l'endroit où vous souhaitez que le saut de ligne apparaisse.  <br/> |
||||||5.  <br/> |Sélectionnez la taille et le style de police de votre choix, puis indiquez si vous souhaitez que l'étiquette se trouve à gauche, au centre ou à droite dans le document.  <br/>  Sélectionnez une police et un style qui sont disponibles sur les ordinateurs des utilisateurs. La taille de la police influe sur l'affichage du texte sur l'étiquette.  <br/> |
||||||6.  <br/> |Entrez la hauteur et la largeur de l'étiquette. La hauteur de l'étiquette peut être comprise entre 0,25 pouce et 20 pouces, et la largeur de l'étiquette peut être comprise entre 0,25 pouce et 20 pouces. Le texte de l'étiquette est toujours centré verticalement dans l'image de l'étiquette.  <br/> |
||||||7.  <br/> |Choisissez **Actualiser** pour afficher un aperçu du contenu de l'étiquette.  <br/> |
   
1. Sélectionnez **OK**.
    
## <a name="create-a-policy-for-a-list-library-or-folder-location-based-retention-policy"></a>Créer une stratégie pour une liste, une bibliothèque ou un dossier (stratégie de rétention basée sur l’emplacement)
<a name="__create_a_policy"> </a>

Vous pouvez définir une stratégie de rétention qui s'applique uniquement à une liste, une bibliothèque ou un dossier spécifique. Toutefois, si vous créez une stratégie de rétention de cette façon, vous ne pouvez pas réutiliser cette stratégie sur d'autres listes, bibliothèques, dossiers ou sites, et vous ne pouvez pas appliquer une stratégie de collection de sites à une stratégie basée sur l'emplacement.
  
Si vous souhaitez appliquer une seule stratégie de rétention à tous les types de contenu dans un seul emplacement, vous souhaiterez probablement utiliser la rétention basée sur l'emplacement. Dans la plupart des autres cas, vous voudrez vérifier qu'une stratégie de rétention est spécifiée pour tous les types de contenu.
  
 Chaque sous-dossier hérite de la stratégie de rétention de son parent, sauf si vous choisissez de bloquer l'héritage et de définir une nouvelle stratégie de rétention au niveau de l'enfant. 
  
Si vous souhaitez définir une stratégie de gestion des informations autre que la rétention à une liste ou une bibliothèque, vous devez définir une stratégie de gestion des informations pour chaque type de contenu de liste individuel associé à cette liste ou bibliothèque.
  
 Si, à tout moment, vous décidez de passer du type de contenu aux stratégies basées sur l'emplacement pour une liste ou une bibliothèque, seule la stratégie de rétention sera utilisée comme stratégie basée sur l'emplacement. Toutes les autres stratégies de gestion (audits, codes-barres et codes-barres) sont héritées des types de contenu associés. 
  
 Les stratégies basées sur l'emplacement peuvent être désactivées pour une collection de sites en désactivant la fonctionnalité de réTention basée sur les dossiers et les bibliothèques. Cela permet aux administrateurs de collections de sites de s'assurer que leurs stratégies de type de contenu ne sont pas remplacées par les stratégies d'emplacement d'un administrateur de liste. 
  
Vous avez besoin au minimum de l'autorisation gérer les listes pour modifier les paramètres de la stratégie de gestion des informations d'une liste ou d'une bibliothèque.
  
1. Accédez à la liste ou à la bibliothèque pour laquelle vous souhaitez spécifier une stratégie de gestion des informations. 
    
2. Dans le ruban, sélectionnez les paramètres de **bibliothèque** ou \> de **liste**de l'onglet **bibliothèque** ou **liste** .
    
    Dans SharePoint Online, cliquez sur **paramètres** , puis sur paramètres de la **liste** ou paramètres de la **bibliothèque**. 
    
3. Sous **autorisations et paramètres de stratégie de gestion des informations de gestion** \> ****.
  
![Lien stratégies de gestion des informations sur la page Paramètres de la bibliothèque de documents](media/9fa6d366-6aab-49e1-a05c-898ac6f536e6.png)
  
4. Sur la page Paramètres de la stratégie de gestion des informations, vérifiez que la source de rétention de la liste ou de la bibliothèque est définie sur Bibliothèque et dossiers. 
  
Si le **type de contenu** apparaît en tant que source, cliquez sur modifier la **source**, puis sur **bibliothèque et dossiers**. Vous êtes alerté que les stratégies de rétention de type de contenu seront ignorées. Sélectionnez **OK**. 
    
5. Sur la page modifier la stratégie, sous planification de la réTention **basée sur une bibliothèque**, entrez une brève description de la stratégie que vous créez. 
    
6. Sélectionnez **Ajouter un stade de rétention...**
    
     Notez que sous enregistrements, vous pouvez choisir de définir différentes stratégies de rétention pour les enregistrements en sélectionnant l'option définir différentes étapes de rétention pour les enregistrements. 
    
7. Dans la boîte de dialogue Propriétés de la scène, sélectionnez une option de période de rétention pour spécifier la date d'expiration des documents ou des éléments. Effectuez l’une des opérations suivantes :
    
  - Pour définir la date d'expiration sur la base d'une propriété de date, sous **événement** \> **cette étape est basée sur une propriété de date sur l'élément**, puis sélectionnez l'action de document ou d'élément (par exemple, créé ou modifié) et l'incrément du temps après cette action ( par exemple, le nombre de jours, de mois ou d'années, lorsque vous souhaitez que l'élément expire. 
    
  - Pour utiliser une formule de rétention personnalisée afin de déterminer l'expiration, choisissez **définir par une formule de rétention personnalisée installée sur ce serveur**. 
    
    > [!NOTE]
    >  Cette option est disponible uniquement si votre administrateur a défini une formule personnalisée. 
  
  - Sous **action**, spécifiez ce qui doit se produire lorsque le document ou l'élément expire. Pour activer une action spécifique dans le document ou l'élément (par exemple, la suppression), sélectionnez une action dans la liste. 
    
8. L'option **Démarrer un flux de travail** est disponible uniquement si vous définissez une stratégie pour une liste, une bibliothèque ou un type de contenu auquel un flux de travail est déjà associé. Vous aurez alors un choix de flux de travail parmi lesquels choisir. 
    
9. Sous **périodicité**, sélectionnez **répéter l'action de cette étape...** et entrez la fréquence à laquelle vous souhaitez que l'action se produise. 
    
    > [!NOTE]
    >  Cette option n'est disponible que si l'action que vous avez sélectionnée peut être répétée. Par exemple, vous ne pouvez pas définir la récurrence de l'action **Supprimer définitivement**. 
  
10. Sélectionnez **OK**.
    
## <a name="apply-a-site-collection-policy-to-a-content-type"></a>Appliquer une stratégie de collection de sites à un type de contenu
<a name="__apply_a_site"> </a>

Si des stratégies de gestion des informations ont déjà été créées pour votre site en tant que stratégies de collection de sites, vous pouvez appliquer l'une des stratégies à un type de contenu. En procédant ainsi, vous pouvez appliquer la même stratégie à plusieurs types de contenu dans une collection de sites qui ne partagent pas le même type de contenu parent.
  
 Si vous souhaitez appliquer des stratégies à plusieurs types de contenu dans une collection de sites et que vous disposez d'un service de métadonnées gérées configuré, vous pouvez utiliser la publication de type de contenu pour publier des stratégies de gestion des informations sur plusieurs collections de sites. Pour plus d'informations, consultez la section [appliquer une stratégie sur plusieurs collections de sites](#apply-a-policy-across-site-collections) . 
  
1. Accédez à la liste ou à la bibliothèque qui contient le type de contenu auquel vous souhaitez appliquer une stratégie.
    
2. Dans le ruban, sélectionnez les paramètres de **bibliothèque** ou \> de **liste**de l'onglet **bibliothèque** ou **liste** .
    
    Dans SharePoint Online, cliquez sur **paramètres** , puis sur paramètres de la **liste** ou paramètres de la **bibliothèque**. 
    
3. Sous **autorisations et paramètres de stratégie de gestion des informations de gestion** \> ****.
  
![Lien stratégies de gestion des informations sur la page Paramètres de la bibliothèque de documents](media/9fa6d366-6aab-49e1-a05c-898ac6f536e6.png)
  
4. Vérifiez que la source de la stratégie est définie sur **types de contenu**, puis, sous stratégies de **type de contenu** , sélectionnez le type de contenu auquel vous souhaitez appliquer la stratégie. 
    
5. Sous **spécifier la stratégie** \> **utiliser une stratégie de collection de sites**, puis sélectionnez la stratégie que vous souhaitez appliquer à partir de la liste. 
    
    > [!NOTE]
    >  Si l'option **utiliser une stratégie de collection de sites** n'est pas disponible, aucune stratégie de collection de sites n'a été définie pour la collection de sites. 
  
6. Sélectionnez **OK**.
    
     Si la liste ou la bibliothèque que vous utilisez prend en charge la gestion de plusieurs types de contenu, sous **types de contenu** , vous pouvez choisir le type de contenu pour lequel vous souhaitez spécifier une stratégie de gestion des informations. Cela vous fera passer directement à l'étape 5 ci-dessus. 
    
## <a name="apply-a-policy-across-site-collections"></a>Appliquer une stratégie à travers des collections de sites
<a name="__toc260646789"> </a>

Partager des types de contenu entre des collections de sites à l'aide d'une application de service de métadonnées gérées pour configurer la publication de type de contenu. La publication de type de contenu vous permet de gérer le contenu et les métadonnées de manière cohérente sur vos sites, car les types de contenu peuvent être créés et mis à jour de façon centralisée, et les mises à jour peuvent être publiées vers plusieurs collections de sites ou applications Web.
  
## <a name="create-a-template-from-an-existing-policy-to-use-across-site-collections"></a>Créer un modèle à partir d'une stratégie existante à utiliser dans les collections de sites
<a name="__toc262125409"> </a>

Vous pouvez définir une stratégie de gestion des informations, puis créer un modèle à partir de celle-ci afin de l'utiliser selon vos besoins sur plusieurs collections de sites. Vous pouvez utiliser cette méthode si vous souhaitez disposer d'une sauvegarde de vos stratégies d'informations, ou si elle peut également être utilisée comme une autre méthode pour utiliser la publication de type de contenu pour l'application d'une stratégie à travers des collections de sites. Pour créer un modèle ou une sauvegarde de la stratégie, exportez la stratégie à partir d'une collection de sites, puis importez-la dans un emplacement enregistré ou dans une autre collection de sites.
  
> [!IMPORTANT]
>  Si vous utilisez la fonctionnalité d'exportation/importation pour créer un ensemble de modèles de stratégie, gardez à l'esprit qu'il existe un identificateur unique dans le fichier Policy. Xml. Pour cette raison, vous ne pouvez pas importer cette stratégie sur un site plus d'une fois sans modifier cet identificateur unique. 
  
### <a name="export-a-policy"></a>Exporter une stratégie
<a name="__toc260646790"> </a>

1. Sur la page d'accueil de la collection de sites, sélectionnez **paramètres**![des paramètres de petite taille qui ont pris la place des paramètres de site. ](media/a47a06c3-83fb-46b2-9c52-d1bad63e3e60.png) **site.** \>
    
    Dans un site connecté à un groupe SharePoint, cliquez sur **paramètres**, sur **contenu du site**, puis sur **paramètres du site**. 
    
2. Sur la page Paramètres du site, sous **modèles de stratégies de type de contenu**administration \> de la collection de **sites** . 
  
![Lien de modèle de stratégie de type de contenu sur la page Paramètres du site](media/26d3466a-23ec-443f-88f0-2aaff38e992b.png)
  
3. Sélectionnez la stratégie que vous souhaitez exporter \> vers l' \> **exportation**la plus basse.
    
4. Lorsque vous êtes invité à enregistrer ou ouvrir le fichier, sélectionnez **Enregistrer**, puis sélectionnez l'emplacement auquel vous souhaitez enregistrer le fichier. Veillez à sélectionner un emplacement disponible pour les collections de sites qui importent la stratégie.
    
5. Lorsque la boîte de dialogue Téléchargement terminé s'affiche, cliquez sur **Fermer**.
    
### <a name="import-a-policy-to-a-different-site-collection"></a>Importer une stratégie dans une autre collection de sites
<a name="__toc260646791"> </a>

L'importation d'une stratégie de gestion des informations vous permet de l'appliquer à plusieurs types de contenu au niveau du site ou de la liste dans une collection de sites donnée. Les avantages de cette opération sont les suivants: vous n'avez pas besoin de redéfinir et d'appliquer la stratégie sur chaque type de contenu, et vous pouvez plus facilement gérer les modifications de stratégie en apportant des modifications à la stratégie dans un seul emplacement.
  
1. Sur la page d'accueil de la collection de sites à laquelle vous souhaitez appliquer la stratégie, sélectionnez **paramètres**![des paramètres de petite taille qui ont pris la place des paramètres de site. ](media/a47a06c3-83fb-46b2-9c52-d1bad63e3e60.png) **site.** \>
    
    Dans un site connecté à un groupe SharePoint, cliquez sur **paramètres**, sur **contenu du site**, puis sur **paramètres du site**. 
    
2. Sur la page Paramètres du site, sous **modèles de stratégies de type de contenu**administration \> de la collection de **sites** .
    
3. Sur la page \> stratégies, importez **** \> **** le fichier XML pour la stratégie. 
    
4. Sélectionnez le fichier XML dans lequel la stratégie a été enregistrée \> ****. 
    
5. Dans la page \> importer une stratégie de collection de sites, importez-la pour ajouter la stratégie à la collection de sites. **** 
    
Votre stratégie importée peut désormais être appliquée à un ou plusieurs types de contenu au niveau du site ou de la liste. 
  
Les stratégies de gestion des informations permettent à votre organisation de contrôler la durée de conservation du contenu, d'auditer les opérations effectuées par les utilisateurs et d'ajouter des codes-barres ou des étiquettes aux documents. Une stratégie peut contribuer à renforcer la conformité aux réglementations juridiques et gouvernementales ou aux processus d'entreprise internes. En tant qu'administrateur, vous pouvez configurer une stratégie pour contrôler le suivi des documents et la durée de conservation des documents.

Vous pouvez créer une stratégie de gestion des informations sur trois emplacements différents dans la hiérarchie du site, du plus large au plus étroit:
- Créer une stratégie à utiliser sur plusieurs types de contenu au sein d'une collection de sites.
- Créer une stratégie pour un type de contenu de site.
- Créer une stratégie pour une liste ou une bibliothèque.

Pour plus d'informations, consultez la rubrique [Présentation des stratégies de gestion des informations](intro-to-info-mgmt-policies.md).
  

