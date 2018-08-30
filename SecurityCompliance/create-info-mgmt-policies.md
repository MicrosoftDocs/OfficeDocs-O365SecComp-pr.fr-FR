---
title: Créer et appliquer des stratégies de gestion des informations
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/16/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- OSU150
- OSU160
- MET150
ms.assetid: 8ccac9e4-3a50-49fa-a95b-d186032a6ee3
description: Stratégies de gestion des informations activent les étiquettes de documents ou de votre organisation pour contrôler la durée de conservation de contenu, à auditer que faire les personnes avec du contenu et d’ajouter des codes-barres. Une stratégie peut aider à imposer la conformité aux réglementations juridiques ou des processus d’entreprise interne. En tant qu’administrateur, vous pouvez configurer une stratégie pour contrôler le suivi des documents et la durée de conservation des documents.
ms.openlocfilehash: cc15b7d830e6c13e00045f7e4b672ac4a755a70e
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527788"
---
# <a name="create-and-apply-information-management-policies"></a>Créer et appliquer des stratégies de gestion des informations

Stratégies de gestion des informations activent les étiquettes de documents ou de votre organisation pour contrôler la durée de conservation de contenu, à auditer que faire les personnes avec du contenu et d’ajouter des codes-barres. Une stratégie peut aider à imposer la conformité aux réglementations juridiques ou des processus d’entreprise interne. En tant qu’administrateur, vous pouvez configurer une stratégie pour contrôler le suivi des documents et la durée de conservation des documents.
  
Vous pouvez créer une peut stratégie de gestion des informations dans trois emplacements différents dans la hiérarchie du site, à partir de la plus large à la plus étroite disponible :
  
- Créer une stratégie à utiliser dans plusieurs types de contenu au sein d’une collection de sites.
    
- Créer une stratégie pour un type de contenu de site.
    
- Créer une stratégie pour une liste ou une bibliothèque.
    
Pour plus d’informations, voir [Introduction aux stratégies de gestion des informations](intro-to-info-mgmt-policies.md).
  
## <a name="create-a-policy-for-multiple-content-types-within-a-site-collection"></a>Créer une stratégie pour plusieurs types de contenu au sein d’une collection de sites
<a name="__toc261001590"> </a>

Pour vous assurer qu’une stratégie des informations est appliquée à tous les documents d’un certain type au sein d’une collection de sites, envisagez de créer la stratégie au niveau de la collection de sites, puis appliquez la stratégie aux types de contenu. Elles sont appelées stratégies de collection de sites. 
  
1. Sur la page d’accueil de la collection de sites \> **paramètres**![bouton SharePoint 2016 paramètres sur la barre de titre. ](media/1c22d2d8-39e0-4930-82c6-c3eee44211d3.png) \> **Paramètres du site**.
    
    Dans un site SharePoint connectés au groupe, cliquez sur **paramètres**, cliquez sur le **Contenu du Site**, puis cliquez sur **Paramètres du Site**. 
    
2. Dans la page Paramètres du Site, sous **Administration de la Collection de sites** \> **Modèles de stratégie de Type de contenu**. 
  
![Lien de modèle de stratégie de Type contenu dans la page Paramètres du Site](media/26d3466a-23ec-443f-88f0-2aaff38e992b.png)
  
3. Dans la page stratégies \> **créer**. 
    
4. Entrez un nom et une description pour la stratégie, puis écrire une brève déclaration de stratégie qui explique aux utilisateurs est la stratégie pour.
    
5. Voir la section suivante sur la création de stratégies pour un type de contenu de site apprendre à configurer les fonctionnalités que vous souhaitez associer à la stratégie. 
    
6. Cliquez sur **OK**.
    
## <a name="create-a-policy-for-a-site-content-type"></a>Créer une stratégie pour un type de contenu de site
<a name="__create_a_policy"> </a>

Ajout d’une stratégie de gestion des informations à un type de contenu facilite l’associer des fonctionnalités de stratégie avec plusieurs listes ou bibliothèques. Vous pouvez choisir d’ajouter une stratégie de gestion des informations existante à un type de contenu ou créer une stratégie unique spécifique à un type de contenu spécifique.
  
 Vous pouvez également ajouter une stratégie de gestion des informations pour un type de contenu qui est spécifique à des listes. Cela a pour effet de l’application de la stratégie uniquement aux éléments de la liste qui utilisent le type de contenu. 
  
1. Sur la page d’accueil de la collection de sites \> **paramètres**![bouton SharePoint 2016 paramètres sur la barre de titre. ](media/1c22d2d8-39e0-4930-82c6-c3eee44211d3.png) \> **Paramètres du site**.
    
    Dans un site SharePoint connectés au groupe, cliquez sur **paramètres**, cliquez sur le **Contenu du Site**, puis cliquez sur **Paramètres du Site**. 
    
2. Dans la page Paramètres du Site, sous **Galeries du Concepteur Web** \> **types de contenu de Site**.
  
![Lien de types de contenu de site sur la page Paramètres du Site](media/6f6fa51f-15d7-4782-b06f-a7b36e874cd3.png)
  
3. Dans la page Paramètres de Type de contenu de Site, sélectionnez le type de contenu que vous souhaitez ajouter une stratégie.
    
4. Dans la page Type de contenu de Site, sous **paramètres** \> **paramètres de stratégie de gestion des informations**.
    
5. Dans la page Modifier la stratégie, entrez un nom et une description pour la stratégie, puis écrire une brève description qui explique aux utilisateurs est la stratégie pour.
    
6. Dans les sections suivantes, sélectionnez les fonctionnalités de stratégie individuelles que vous souhaitez ajouter à votre stratégie de gestion des informations. 
  
![Types de stratégies de contenu](media/19fcb8a3-974b-40d3-a13f-b76088d122f8.png)
  
7. Pour spécifier une période de rétention des documents et des éléments qui sont soumis à cette stratégie, sélectionnez **Activer la rétention**, puis spécifiez la période de rétention et les actions que vous souhaitez se produisent lorsque les éléments expirent.
    
    Pour spécifier une période de rétention
    
||||||**1.**|** Choisissez ** Ajoutez une étape de rétention pour les enregistrements... ***|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
||||||2.  <br/> | Sélectionnez une option de période de rétention pour spécifier quand les documents ou éléments sont configurés pour expirer. Effectuez l’une des options suivantes :<br/>  Pour définir la date d’expiration basée sur une propriété de date, sous **événement** \> **cette étape repose sur une propriété de date sur l’élément**et puis sélectionnez l’action de document ou un élément (par exemple, création ou modification) et l’incrément de temps après cette action () par exemple, le nombre de jours, mois ou années) lorsque vous souhaitez que l’élément expire.  <br/>  Pour utiliser une formule de rétention personnalisée afin de déterminer l’expiration, choisissez **définir par une formule de rétention personnalisée installée sur ce serveur**.  <br/> > [!NOTE]> Cette option est uniquement disponible si une formule personnalisée a été configurée par votre administrateur.           |
||||||3.  <br/> |L’option **Démarrer un flux de travail** est disponible uniquement si vous définissez une stratégie pour une liste, une bibliothèque ou un type de contenu qui a déjà associé un flux de travail. Vous aura un choix de flux de travail à sélectionner.<br/> |
||||||4.  <br/> |Dans la section **périodicité** , sélectionnez **Répétez l’action de cette étape...** et entrez la fréquence à laquelle vous souhaitez que l’action à nouveau.  <br/> > [!NOTE]> Cette option est uniquement disponible si l’action que vous avez sélectionné peut être répétée. Par exemple, vous ne pouvez pas définir périodicité pour l’action **Supprimer définitivement**.           |
||||||5.  <br/> |Choisissez **OK**.  <br/> |
   
1. Pour activer l’audit des documents et des éléments qui sont soumis à cette stratégie, sélectionnez **Activer l’audit**, puis spécifiez les événements à auditer.
    
    Pour activer l’audit
    
||||||1.* **|Dans la page Modifier la stratégie, ** **sous** **audit** **\>** **Activer l’audit** **, et puis sélectionnez les cases à cocher en regard des événements que vous souhaitez conserver un audit traçage for.* **|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
||||||**2.** <br/> |**Pour inviter les utilisateurs à insérer ces codes-barres dans les documents,** **Choisissez** **Inviter les utilisateurs à insérer un code-barres avant l’enregistrement ou l’impression** **.** <br/> |
||||||**3.** <br/> |**Choisissez** **OK** ** pour appliquer la fonctionnalité d’audit à la stratégie. ** <br/> |
|||||||La fonctionnalité de stratégie d’audit permet aux organisations de créer et d’analyser les journaux d’audit pour les documents et éléments de liste telles que des listes de tâches, des listes de problèmes, des groupes de discussion et des calendriers. Cette fonctionnalité de stratégie fournit un journal d’audit qui enregistre des événements tels que lorsque le contenu est affiché, modifié ou supprimé.  <br/> |
|||||||Lorsque l’audit est activé dans le cadre d’une stratégie de gestion des informations, les administrateurs peuvent afficher les données d’audit dans des rapports d’utilisation de stratégies basées dans Microsoft Excel et qui synthétiser en cours d’utilisation. Les administrateurs peuvent utiliser ces rapports pour déterminer l’utilisation des informations au sein de l’organisation. Ces rapports peuvent également aider les organisations à vérifier et à documenter leur conformité aux exigences réglementaires ou pour examiner les problèmes potentiels.  <br/> |
|||||||Le journal d'audit consigne les informations suivantes : nom de l'événement, date et heure de l'événement et nom système de l'utilisateur ayant exécuté l'action.  <br/> |
   
1. Lorsque les codes-barres sont activés dans le cadre d’une stratégie, ils sont ajoutés aux propriétés de document et affichés dans la zone d’en-tête du document auquel est appliqué le code-barres. Comme les étiquettes, les codes-barres peuvent également être supprimés manuellement à partir d’un document. Vous pouvez spécifier si les utilisateurs doivent être invités à inclure le code à barres lors de l’impression ou l’enregistrement d’un élément, ou si le code-barres doit être inséré manuellement à l’aide de l’onglet **Insertion** dans 2010 Office publient des programmes. 
    
    Pour activer les codes-barres
    
||||||1.* **|**Dans la page Modifier la stratégie, sous **codes-barres** \> **Activer codes-barres**.**|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
||||||**2.** <br/> |Pour inviter les utilisateurs à insérer ces codes-barres dans les documents, cliquez sur **inviter les utilisateurs à insérer un code-barres avant l’enregistrement ou l’impression**.  <br/> |
||||||**3.** <br/> |Cliquez sur **OK** pour appliquer la fonctionnalité de code-barres à la stratégie.  <br/> |
|||||||
 La stratégie de code-barres génère des codes-barres Code 39. Chaque image de code-barres comprend le texte sous le symbole de code-barres qui représente la valeur de code-barres. Ainsi, les données de code-barres à utiliser même lors de l’analyse de matériel n’est pas disponible. Les utilisateurs peuvent taper manuellement le numéro de code-barres dans la zone Rechercher pour localiser l’élément sur un site.  <br/> |
   
1. Pour exiger que les documents sont soumis à cette stratégie sont dotées d’étiquettes, choisissez **Activer les étiquettes**, puis spécifiez les paramètres que vous souhaitez pour les étiquettes.
    
    Pour activer les étiquettes
    
||||||**1.**|** Pour obliger les utilisateurs à ajouter une étiquette à un document, cliquez sur **inviter les utilisateurs à insérer une étiquette avant l’enregistrement ou l’impression**.  <br/> > [!NOTE]> Si vous souhaitez que les étiquettes soient facultatives, ne sélectionnez pas cette case à cocher.        **|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
||||||2.  <br/> |Pour verrouiller une étiquette afin qu’il ne peut pas être modifiée une fois qu’il a été inséré, sélectionnez **empêcher la modification d’étiquettes après que les avoir ajoutées**.  <br/>  Ce paramètre empêche le texte de l’étiquette de mise à jour une fois que l’étiquette a été inséré dans un élément au sein d’une application cliente comme Word, Excel et PowerPoint. Si vous souhaitez que l’étiquette à mettre à jour les propriétés de ce document ou un élément de mise à jour, ne sélectionnez pas cette case à cocher.<br/> |
||||||3.  <br/> |Dans la zone format d’étiquette, entrez le texte de l’étiquette comme vous le souhaitez à afficher. Les étiquettes peuvent contenir jusqu'à 10 références de colonnes, chacune d’elles peut contenir jusqu'à 255 caractères. Pour créer le format de l’étiquette, procédez comme suit :  <br/> Tapez les noms des colonnes que vous souhaitez inclure dans l’étiquette dans l’ordre dans lequel vous souhaitez les voir apparaître. Placez les noms de colonne entre accolades ({}), comme illustré dans l’exemple dans la page Modifier la stratégie.  <br/> Tapez des mots permettant d’identifier les colonnes en dehors des accolades, comme illustré dans l’exemple dans la page Modifier la stratégie.  <br/> |
||||||4.  <br/> |Pour ajouter un saut de ligne, entrez **\n** où vous souhaitez faire apparaître le saut de ligne.  <br/> |
||||||5.  <br/> |Sélectionnez la taille de police et le style de votre choix, indiquez si vous souhaitez que l’étiquette placée à gauche, centre ou droite dans le document.  <br/>  Sélectionnez une police et un style disponibles sur les ordinateurs des utilisateurs. La taille de la police affecte la quantité de texte peut être affiché sur l’étiquette.  <br/> |
||||||6.  <br/> |Entrez la hauteur et la largeur de l’étiquette. Hauteur d’étiquette compris entre 25 et 20 pouces et la largeur d’étiquette compris entre 25 et 20 pouces. Texte de l’étiquette est toujours centré verticalement dans l’image d’étiquette.  <br/> |
||||||7.  <br/> |Cliquez sur **Actualiser** pour afficher un aperçu du contenu de l’étiquette.  <br/> |
   
1. Cliquez sur **OK**.
    
## <a name="create-a-policy-for-a-list-library-or-folder-location-based-retention-policy"></a>Créer une stratégie pour une liste, une bibliothèque ou un dossier (stratégie de rétention basée sur l’emplacement)
<a name="__create_a_policy"> </a>

Vous pouvez définir une stratégie de rétention qui s’applique uniquement à une liste spécifique, la bibliothèque ou le dossier. Toutefois, si vous créez une stratégie de rétention de cette manière, vous ne pouvez pas réutiliser cette stratégie sur d’autres listes, bibliothèques, des dossiers ou les sites, et vous ne pouvez pas appliquer une stratégie de collection de sites à une stratégie d’emplacement en fonction de.
  
Si vous souhaitez appliquer une stratégie de rétention unique à tous les types de contenu dans un seul emplacement, vous souhaiterez probablement utiliser rétention basée sur l’emplacement. Dans la plupart des cas, vous devez vérifier qu’une stratégie de rétention est spécifiée pour tous les types de contenu.
  
 Chaque sous-dossier hérite de la stratégie de rétention de son parent, sauf si vous choisissez de bloquer l’héritage et définir une nouvelle stratégie de rétention au niveau des enfants. 
  
Si vous souhaitez définir une stratégie de gestion des informations autres que de rétention à une liste ou une bibliothèque, vous devez définir une stratégie de gestion des informations pour chaque type de contenu de liste associé à cette liste ou bibliothèque.
  
 Si à tout moment, que vous décidez de changer de type de contenu aux stratégies d’emplacement pour une liste ou une bibliothèque, la stratégie de rétention seulement doit être utilisée en tant que la stratégie d’emplacement. Toutes les autres stratégies de gestion (audits, codes-barres et codes-barres) seront héritées pour les types de contenu associées. 
  
 Stratégies d’emplacement en fonction de peuvent être désactivées pour une collection de sites en désactivant la fonctionnalité de bibliothèque et de rétention de dossier. Ainsi, les administrateurs de collection de sites pour s’assurer que leurs stratégies de type de contenu ne sont pas remplacées par les stratégies d’emplacement en fonction de l’administrateur d’une liste. 
  
Vous devez au moins l’autorisation Gérer les listes pour modifier les paramètres de stratégie de gestion des informations pour une liste ou une bibliothèque.
  
1. Accédez à la liste ou la bibliothèque pour laquelle vous souhaitez spécifier une stratégie de gestion des informations. 
    
2. Dans le ruban, cliquez sur l’onglet **bibliothèque** ou **liste** \> **Paramètres de la bibliothèque** ou **Paramètres de la liste**.
    
    Dans SharePoint Online, cliquez sur **paramètres** , puis cliquez sur **paramètres de la liste** ou **paramètres de la bibliothèque**. 
    
3. Sous **autorisations et gestion** \> **paramètres de stratégie de gestion des informations**.
  
![Lien de stratégies de gestion des informations sur la page Paramètres de la bibliothèque de documents](media/9fa6d366-6aab-49e1-a05c-898ac6f536e6.png)
  
4. Dans la page Paramètres de stratégie de gestion des informations, assurez-vous que la source de rétention pour la liste ou la bibliothèque est définie sur la bibliothèque et les dossiers. 
  
Si le **Type de contenu** apparaît comme source, cliquez sur **Modifier la Source**, puis cliquez sur **bibliothèque et des dossiers**. Vous êtes averti que les stratégies de rétention de type de contenu seront ignorées. Cliquez sur **OK**. 
    
5. Dans la page Modifier la stratégie, sous **Planification de rétention en fonction de la bibliothèque**, entrez une brève description de la stratégie que vous créez. 
    
6. Cliquez sur **Ajouter une étape de rétention...**
    
     Notez que sous enregistrements, vous pouvez choisir définir des stratégies de rétention différentes pour les enregistrements en sélectionnant les définir différentes étapes de rétention pour l’option d’enregistrements. 
    
7. Dans la boîte de dialogue Propriétés de fenêtre de partage, sélectionnez une option de période de rétention pour spécifier quand les documents ou éléments de sont configurés pour expirer. Effectuez l’une des options suivantes :
    
  - Pour définir la date d’expiration basée sur une propriété de date, sous **événement** \> **cette étape repose sur une propriété de date sur l’élément**et puis sélectionnez l’action de document ou un élément (par exemple, création ou modification) et l’incrément de temps après cette action () par exemple, le nombre de jours, mois ou années) lorsque vous souhaitez que l’élément expire. 
    
  - Pour utiliser une formule de rétention personnalisée afin de déterminer l’expiration, choisissez **définir par une formule de rétention personnalisée installée sur ce serveur**. 
    
    > [!NOTE]
    >  Cette option est uniquement disponible si une formule personnalisée a été configurée par votre administrateur. 
  
  - Sous **Action**, indiquer ce qui doit se produire lorsque le document ou l’élément arrive à expiration. Pour activer une action spécifique sur le document ou l’élément (suppression, par exemple), sélectionnez une action dans la liste. 
    
8. L’option **Démarrer un flux de travail** est disponible uniquement si vous définissez une stratégie pour une liste, une bibliothèque ou un type de contenu qui a déjà associé un flux de travail. Vous aura un choix de flux de travail à sélectionner. 
    
9. Sous **périodicité**, choisissez **Répétez l’action de cette étape...** et entrez la fréquence à laquelle vous souhaitez que l’action à nouveau. 
    
    > [!NOTE]
    >  Cette option est uniquement disponible si l’action que vous avez sélectionné peut être répétée. Par exemple, vous ne pouvez pas définir périodicité pour l’action **Supprimer définitivement**. 
  
10. Cliquez sur **OK**.
    
## <a name="apply-a-site-collection-policy-to-a-content-type"></a>Appliquer une stratégie de collection de sites à un type de contenu
<a name="__apply_a_site"> </a>

Si des stratégies de gestion des informations ont déjà été créées pour votre site en tant que stratégies de collection de sites, vous pouvez appliquer une des stratégies à un type de contenu. Ce faisant, vous pouvez appliquer la même stratégie à plusieurs types de contenu dans une collection de sites qui ne partagent pas le même type de contenu parent.
  
 Si vous souhaitez appliquer des stratégies à plusieurs types de contenu dans une collection de sites et que vous disposez d’un Service de métadonnées gérées est configuré, vous pouvez utiliser à la publication de Type de contenu pour publier des stratégies de gestion des informations pour plusieurs collections de sites. Voir la section [appliquer une stratégie à des types de contenu entre collections de sites](create-info-mgmt-policies.md#__apply_a_policy) pour plus d’informations. 
  
1. Accédez à la liste ou la bibliothèque qui contient le type de contenu auquel vous souhaitez appliquer une stratégie.
    
2. Dans le ruban, cliquez sur l’onglet **bibliothèque** ou **liste** \> **Paramètres de la bibliothèque** ou **Paramètres de la liste**.
    
    Dans SharePoint Online, cliquez sur **paramètres** , puis cliquez sur **paramètres de la liste** ou **paramètres de la bibliothèque**. 
    
3. Sous **autorisations et gestion** \> **paramètres de stratégie de gestion des informations**.
  
![Lien de stratégies de gestion des informations sur la page Paramètres de la bibliothèque de documents](media/9fa6d366-6aab-49e1-a05c-898ac6f536e6.png)
  
4. Vérifiez que la source de la stratégie est définie sur **Les Types de contenu**et sous **Stratégies de Type de contenu** , sélectionnez le type de contenu que vous souhaitez appliquer la stratégie. 
    
5. Sous **Spécifiez la stratégie** \> **utiliser une stratégie de collection de sites**, puis sélectionnez la stratégie que vous souhaitez appliquer dans la liste. 
    
    > [!NOTE]
    >  Si l’option **utiliser une stratégie de collection de sites** n’est pas disponible, aucune stratégie de collection de sites n’ont été définis pour la collection de sites. 
  
6. Cliquez sur **OK**.
    
     Si la liste ou la bibliothèque que vous utilisez prend en charge la gestion de plusieurs types de contenu, sous **Types de contenu** , vous pouvez choisir le type de contenu pour laquelle vous souhaitez spécifier une stratégie de gestion des informations. Vous dirige directement à l’étape 5 ci-dessus. 
    
## <a name="apply-a-policy-across-site-collections"></a>Appliquer une stratégie entre collections de sites
<a name="__toc260646789"> </a>

Partager les types de contenu entre collections de sites à l’aide d’une application de service de métadonnées gérées pour configurer la publication du type de contenu. Publication du type de contenu vous aident à gérer contenu et les métadonnées régulièrement sur vos sites, car les types de contenu peuvent être créés et mis à jour de façon centralisée, et mises à jour peuvent être publiés en sur plusieurs collections de sites abonnement ou d’applications Web.
  
## <a name="create-a-template-from-an-existing-policy-to-use-across-site-collections"></a>Créer un modèle à partir d’une stratégie existante à utiliser dans les collections de sites
<a name="__toc262125409"> </a>

Vous pouvez définir une stratégie de gestion des informations et puis créer un modèle à partir de l’utilisation nécessaire dans plusieurs collections de sites. Cette méthode peut être utilisée si vous souhaitez disposer d’une sauvegarde de vos stratégies d’informations, ou il peut également servir comme une méthode alternative à l’utilisation de la publication du type de contenu pour appliquer une stratégie entre collections de sites. Vous créez un modèle ou une sauvegarde de la stratégie en exportation de la stratégie à partir d’une collection de sites, puis l’importer vers un emplacement enregistré ou à une autre collection de sites.
  
> [!IMPORTANT]
>  Si vous utilisez l’exportation/importation des fonctionnalités en tant que permet de rendre un ensemble de modèles de stratégie, n’oubliez pas que l’identificateur unique existe dans le fichier .xml de stratégie. Pour cette raison, vous ne pouvez pas importer cette stratégie dans un site plusieurs fois sans modifier cet identificateur unique. 
  
### <a name="export-a-policy"></a>Exporter une stratégie
<a name="__toc260646790"> </a>

1. Sur la page d’accueil de la collection de sites, choisissez **paramètres**![engrenage de paramètres de petite taille qui ont eu lieu de paramètres du Site. ](media/a47a06c3-83fb-46b2-9c52-d1bad63e3e60.png) \> **Paramètres du site**.
    
    Dans un site SharePoint connectés au groupe, cliquez sur **paramètres**, cliquez sur le **Contenu du Site**, puis cliquez sur **Paramètres du Site**. 
    
2. Dans la page Paramètres du Site, sous **Administration de la Collection de sites** \> **Modèles de stratégie de Type de contenu**. 
  
![Lien de modèle de stratégie de Type contenu dans la page Paramètres du Site](media/26d3466a-23ec-443f-88f0-2aaff38e992b.png)
  
3. Choisissez la stratégie que vous souhaitez exporter \> faire défiler vers le bas \> **Exporter**.
    
4. À l’invite pour enregistrer ou ouvrir le fichier, cliquez sur **Enregistrer**, puis sélectionnez un emplacement pour enregistrer le fichier. Veillez à sélectionner un emplacement qui est disponible pour les collections de sites qui importent la stratégie.
    
5. Lorsque la boîte de dialogue Téléchargement terminé s’affiche, choisissez **Fermer**.
    
### <a name="import-a-policy-to-a-different-site-collection"></a>Importer une stratégie à une autre collection de sites
<a name="__toc260646791"> </a>

Importation d’une stratégie de gestion des informations permet d’appliquer à plusieurs types de contenu au niveau du site ou de liste dans n’importe quelle collection de sites donnée. Les avantages de cette opération sont double : vous n’êtes pas obligé de nouveau définir et appliquer la stratégie de chaque type de contenu, et vous pouvez gérer plus facilement les modifications de la stratégie en apportant des modifications à la stratégie dans un seul endroit.
  
1. Dans la page d’accueil de la collection de sites à laquelle vous souhaitez appliquer la stratégie, choisissez **paramètres**![engrenage de paramètres de petite taille qui ont eu lieu de paramètres du Site. ](media/a47a06c3-83fb-46b2-9c52-d1bad63e3e60.png) \> **Paramètres du site**.
    
    Dans un site SharePoint connectés au groupe, cliquez sur **paramètres**, cliquez sur le **Contenu du Site**, puis cliquez sur **Paramètres du Site**. 
    
2. Dans la page Paramètres du Site, sous **Administration de la Collection de sites** \> **Modèles de stratégie de Type de contenu**.
    
3. Dans la page stratégies \> **Import** \> **Parcourir** pour rechercher le fichier XML pour la stratégie. 
    
4. Sélectionnez le fichier XML dans lequel la stratégie a été enregistrée \> **Open**. 
    
5. Dans l’importation une stratégie de Collection de sites page \> **Import** pour ajouter la stratégie à la collection de sites. 
    
Votre importé stratégie peut maintenant être appliquée à un ou plusieurs types de contenu au niveau du site ou de liste. 
  
[Stratégies de gestion des informations activent les étiquettes de documents ou de votre organisation pour contrôler la durée de conservation de contenu, à auditer que faire les personnes avec du contenu et d’ajouter des codes-barres. Une stratégie peut aider à imposer la conformité aux réglementations juridiques ou des processus d’entreprise interne. En tant qu’administrateur, vous pouvez configurer une stratégie pour contrôler le suivi des documents et la durée de conservation des documents. Vous pouvez créer une peut stratégie de gestion des informations dans trois emplacements différents dans la hiérarchie du site, à partir de la plus large à la plus étroite : créer une stratégie à utiliser dans plusieurs types de contenu au sein d’une collection de sites. Créer une stratégie pour un type de contenu de site. Créer une stratégie pour une liste ou une bibliothèque. Pour plus d’informations, voir Introduction aux stratégies de gestion des informations.](create-info-mgmt-policies.md#__top)
  

