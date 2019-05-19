---
title: cas de découverte électronique dans le centre de sécurité & conformité
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 8dd335ab-29d0-41c3-8dd8-9f7c7481e60c
description: Utilisez le centre de sécurité & Compliance Center pour créer et gérer des cas eDiscovery dans votre organisation. Vous pouvez affecter des membres au cas, placer des emplacements de contenu en conservation, exécuter des recherches de contenu associées à l’incident et exporter les résultats de la recherche. Vous pouvez également préparer des données de cas pour une analyse approfondie dans Advanced eDiscovery.
ms.openlocfilehash: f0487a7657b1d6cc4374bfc7308092285aebc979
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155016"
---
# <a name="ediscovery-cases-in-the-security--compliance-center"></a>cas de découverte électronique dans le centre de sécurité & conformité

Vous pouvez utiliser des cas eDiscovery dans le centre de conformité dans Office 365 et Microsoft 365 pour contrôler qui peut créer, consulter et gérer les cas eDiscovery dans votre organisation. Si votre organisation a un abonnement Office 365 E5, vous pouvez également utiliser des cas eDiscovery pour analyser les résultats de la recherche à l’aide d’Office 365 Advanced eDiscovery.
  
Un cas de découverte électronique permet d’ajouter des membres à un cas, de contrôler les types d’actions que les membres de cas spécifiques peuvent effectuer, de placer des emplacements de contenu associés à un dossier juridique en conservation, et d’associer plusieurs recherches de contenu à un seul cas. Vous pouvez également exporter les résultats d’une recherche de contenu associée à un cas ou préparer les résultats de recherche pour analyse dans Advanced eDiscovery. Les cas de découverte électronique constituent un bon moyen de limiter les personnes ayant accès aux recherches de contenu et aux résultats de recherche pour un dossier juridique spécifique dans votre organisation.
  
Utilisez le flux de travail suivant pour configurer et utiliser des cas eDiscovery dans le centre de sécurité & Compliance Center et Advanced eDiscovery.

[Step 1: Assign eDiscovery permissions to potential case members](#step-1-assign-ediscovery-permissions-to-potential-case-members)

[Étape 2: créer un nouveau dossier](#step-2-create-a-new-case)

[Étape 3: ajouter des membres à un cas](#step-3-add-members-to-a-case)

[Étape 4: placer des emplacements de contenu en conservation](#step-4-place-content-locations-on-hold)

[Étape 5: créer et exécuter une recherche de contenu associée à un cas](#step-5-create-and-run-a-content-search-associated-with-a-case)

[Étape 6: exporter les résultats d’une recherche de contenu associée à un cas](#step-6-export-the-results-of-a-content-search-associated-with-a-case)

[Étape 7: préparer les résultats de recherche pour Advanced eDiscovery](#step-7-prepare-search-results-for-advanced-ediscovery)

[Étape 8: atteindre le cas dans Advanced eDiscovery](#step-8-go-to-the-case-in-advanced-ediscovery)

[Module Étape 9: fermer un incident](#optional-step-9-close-a-case)

[Module Étape 10: rouvrir un litige clos](#optional-step-10-re-open-a-closed-case)

[Plus d’informations](#more-information)
  
## <a name="step-1-assign-ediscovery-permissions-to-potential-case-members"></a>Étape 1 : attribuer des autorisations de découverte électronique aux membres potentiels de cas

La première étape consiste à attribuer des autorisations liées à la découverte électronique appropriées à des personnes afin de les ajouter à un cas eDiscovery à l’étape 2. Vous devez être membre du groupe de rôles gestion de l’organisation (ou disposer du rôle de gestion des rôles) dans le centre de sécurité & Compliance Center pour attribuer des autorisations eDiscovery. La liste suivante décrit les groupes de rôles liés à la découverte électronique dans le centre de sécurité & Compliance Center. 
  
- **** Reviewer: ce groupe de rôles dispose des autorisations les plus restrictives liées à la découverte électronique. Le principal objectif de ce groupe de rôles est de permettre aux membres d’afficher et d’accéder aux données de cas dans Office 365 Advanced eDiscovery. Les membres de ce groupe ne peuvent voir et ouvrir que la liste des incidents figurant dans la page de **découverte électronique** dans le centre de sécurité _AMP_ Compliance Center dont ils sont membres. Une fois que l’utilisateur accède à un cas dans le centre de sécurité et de conformité, il peut cliquer sur **basculer vers Advanced eDiscovery** pour accéder aux données de cas et les analyser dans Advanced eDiscovery. Ils ne peuvent pas créer de cas, ajouter des membres à un cas, créer des suspensions, créer des recherches, afficher un aperçu des résultats de la recherche, exporter des résultats de recherche ou préparer des résultats pour Advanced eDiscovery. 
    
- **Gestionnaire eDiscovery** : les membres de ce groupe de rôles peuvent créer et gérer des cas eDiscovery. Ils peuvent ajouter et supprimer des membres, placer des emplacements de contenu en conservation, créer et modifier des recherches de contenu associées à un cas, exporter les résultats d’une recherche de contenu et préparer des résultats de recherche pour analyse dans Advanced eDiscovery. Il existe deux sous-groupes dans ce groupe de rôles. Ces sous-groupes ont différents rôles.
    
  - **Gestionnaire eDiscovery** : permet d’afficher et de gérer les cas eDiscovery qu’ils créent ou dont ils sont membres. Si un autre gestionnaire eDiscovery crée un cas mais n’ajoute pas de deuxième gestionnaire eDiscovery en tant que membre de ce dernier, le deuxième gestionnaire eDiscovery ne pourra pas afficher ou ouvrir le cas sur la page **eDiscovery** dans le centre de sécurité _AMP_ Compliance Center. les gestionnaires eDiscovery peuvent également accéder à leurs incidents dans Advanced eDiscovery pour effectuer des tâches d’analyse. 
    
  - **administrateur eDiscovery** : peut effectuer toutes les tâches de gestion des dossiers qu’un gestionnaire eDiscovery peut effectuer. De plus, un administrateur de découverte électronique peut :
    
    - Afficher tous les cas répertoriés sur la page **Découverte électronique**. 
    
    - Gérez tous les cas dans l’organisation une fois qu’ils ont été ajoutés en tant que membre du cas.
    
    - Accéder aux données de cas dans Advanced eDiscovery pour tous les cas de l’organisation.
    
    Consultez la section [More information](#more-information) pour connaître les raisons pour lesquelles vous pourriez avoir besoin d’un administrateur de découverte électronique dans votre organisation. 
    
> [!IMPORTANT]
> Si une personne n’est pas membre de l’un de ces groupes de rôles liés à la découverte électronique, ou n’est pas membre d’un groupe de rôles auquel est attribué le rôle de réviseur, vous ne pouvez pas l’ajouter en tant que membre d’un cas de découverte électronique. 

Pour plus d’informations sur les autorisations de découverte électronique, consultez la rubrique [attribution d’autorisations eDiscovery](assign-ediscovery-permissions.md).
  
 **Pour attribuer des autorisations de découverte électronique, procédez comme suit :**
  
1. Accédez à la page [https://protection.office.com](https://protection.office.com).
    
2. Connectez-vous à Office 365 à l'aide de votre compte scolaire ou professionnel.
    
3. Dans le centre de sécurité & conformité, cliquez sur **autorisations**, puis effectuez l’une des opérations suivantes en fonction des autorisations de découverte électronique que vous souhaitez attribuer.
    
    - Pour attribuer des autorisations de relecteur, sélectionnez **** le groupe de rôles réviseur, puis en regard de **membres**, cliquez sur **modifier**. Cliquez sur **choisir les membres**, sur **modifier**, ![sur](media/ITPro-EAC-AddIcon.gif) ajouter une icône **Ajouter**, sélectionnez l’utilisateur que vous souhaitez ajouter au groupe de rôles réviseur, puis cliquez sur **Ajouter**.
    
    - Pour attribuer des autorisations de gestionnaire eDiscovery, sélectionnez le groupe de rôles **Gestionnaire de découverte électronique** , puis en regard de **Gestionnaire eDiscovery**, cliquez sur **modifier**. Cliquez sur **choisir le gestionnaire eDiscovery**, sur **modifier**, sur ![ajouter une icône](media/ITPro-EAC-AddIcon.gif) * * ajouter * *, sélectionnez l’utilisateur que vous souhaitez ajouter en tant que gestionnaire eDiscovery, puis cliquez sur **Ajouter**.
    
    - Pour attribuer des autorisations d’administrateur eDiscovery, sélectionnez le groupe de rôles **Gestionnaire de découverte** électronique, puis en regard de **administrateur de découverte électronique**, cliquez sur **modifier**. Cliquez sur **choisir un administrateur de découverte électronique**, ![cliquez sur](media/ITPro-EAC-AddIcon.gif) **modifier**, cliquez sur Ajouter une icône **Ajouter**, sélectionnez l’utilisateur que vous souhaitez ajouter en tant qu’administrateur de découverte électronique, puis cliquez sur **Ajouter**.
    
4. Une fois que vous avez ajouté tous les utilisateurs, cliquez sur **terminé**, cliquez sur **Enregistrer** pour enregistrer les modifications apportées au groupe de rôles, puis cliquez sur **Fermer**.

## <a name="step-2-create-a-new-case"></a>Étape 2: créer un nouveau dossier

L’étape suivante consiste à créer un cas de découverte électronique. Vous devez être membre du groupe de rôles Gestionnaire de découverte électronique pour créer des cas de découverte électronique. Comme expliqué précédemment, une fois que vous avez créé un nouveau cas dans le centre de sécurité & Compliance Center, vous (et d’autres membres de cas) pourrez accéder à cette même demande dans Advanced eDiscovery si votre organisation a un abonnement Office 365 E5.
  
1. Accédez à la page [https://protection.office.com](https://protection.office.com).
    
2. Connectez-vous à Office 365 à l'aide de votre compte scolaire ou professionnel.
    
3. Dans le centre de sécurité & Compliance Center **** \> , cliquez sur eDiscovery **eDiscovery**, ![puis sur](media/ITPro-EAC-AddIcon.gif) Add Icon **Create a case**.
    
4. Sur la page **New case** , attribuez un nom à la demande, tapez une description facultative, puis cliquez sur **Enregistrer**. Notez que le nom du cas doit être unique dans votre organisation.
    
    ![Créer un nouveau cas](media/7f78f83b-1525-4c77-9888-4b6bda1e148d.png)
  
    Le nouvel incident est affiché dans la liste des incidents de la page de **découverte électronique** . Notez que vous pouvez placer le curseur sur un nom de cas pour afficher des informations sur le cas, notamment l’état de la demande de devis ( **actif** ou **fermé**), la description de la demande de devis (créée à l’étape précédente), ainsi que le moment où le cas a été modifié en dernier et qui l’a modifié.
    
    > [!TIP]
    > Une fois que vous avez créé un nouveau cas, vous pouvez le renommer à tout moment. Il vous suffit de cliquer sur le nom de la demande de devis dans la page **eDiscovery** . Sur la page de menu déroulante **gérer ce cas** , modifiez le nom affiché dans la zone sous **nom**, puis enregistrez la modification. 
  
## <a name="step-3-add-members-to-a-case"></a>Étape 3: ajouter des membres à un cas

Une fois que vous avez créé un nouveau cas, l’étape suivante consiste à ajouter des membres au cas. Comme expliqué précédemment, seuls les utilisateurs membres des groupes de rôles Reviewer ou gestionnaire de découverte électronique peuvent être ajoutés en tant que membres du cas. Notez que le gestionnaire eDiscovery qui a créé le cas est automatiquement ajouté en tant que membre.
  
1. Dans le centre de sécurité & Compliance Center **** \> **** , cliquez sur eDiscovery eDiscovery pour afficher la liste des incidents de votre organisation. 
    
2. Cliquez sur le nom de l’incident auquel vous souhaitez ajouter des membres.
    
    La page flyout **gérer ce cas** s’affiche. 
    
    ![Gérer une page de menu volant case](media/11f35ceb-6c98-4580-a3bc-ad688e9c7af9.png)
  
3. Sous **gérer les membres**, ![cliquez sur](media/ITPro-EAC-AddIcon.gif) ajouter une icône **Ajouter** pour ajouter des membres à la demande de devis. 
    
    Vous pouvez également choisir d’ajouter un groupe de rôles à la demande de devis. Sous **gérer les groupes**de rôles ![, cliquez](media/ITPro-EAC-AddIcon.gif) sur Ajouter une icône **Ajouter**.
    
    > [!NOTE]
    > Les groupes de rôles contrôlent les personnes qui peuvent assigner des membres à un cas eDiscovery. Cela signifie que vous pouvez uniquement affecter les groupes de rôles dont vous êtes membre à un cas.
    
4. Dans la liste des personnes ou des groupes de rôles qui peuvent être ajoutés en tant que membres de la case, activez la case à cocher en regard des noms des personnes ou des groupes de rôles que vous souhaitez ajouter.
    
    > [!TIP]
    > Si vous avez une grande liste de personnes pouvant être ajoutées en tant que membres, utilisez la zone de **recherche** pour rechercher une personne spécifique dans la liste. 
  
5. Une fois que vous avez sélectionné les personnes ou les groupes de rôles à ajouter en tant que membres du groupe, cliquez sur **Ajouter**.
    
    Dans **gérer ce cas**, cliquez sur **Enregistrer** pour enregistrer la nouvelle liste de membres de cas. 
    
6. Cliquez sur **Enregistrer** pour enregistrer la nouvelle liste de membres de cas. 
  
## <a name="step-4-place-content-locations-on-hold"></a>Étape 4: placer des emplacements de contenu en conservation

Vous pouvez utiliser un cas de découverte électronique pour créer des conservations et conserver le contenu pouvant être associé au cas. Vous pouvez placer une suspension sur les boîtes aux lettres et les sites OneDrive entreprise des personnes qui sont des dépositaires dans le cas. Vous pouvez également placer une suspension sur la boîte aux lettres de groupe, le site SharePoint et le site OneDrive entreprise pour un groupe Office 365. De même, vous pouvez placer une conservation sur la boîte aux lettres et le site associés à Microsoft Teams. Lorsque vous placez des emplacements de contenu en conservation, le contenu est conservé jusqu’à ce que vous supprimiez le blocage de l’emplacement du contenu ou jusqu’à ce que vous supprimiez la conservation.

> [!NOTE]
> Une fois que vous avez placé un emplacement de contenu, la conservation prend effet jusqu’à 24 heures. 
>   
Lorsque vous créez une suspension, vous disposez des options suivantes pour définir l’étendue du contenu qui se trouve dans les emplacements de contenu spécifiés:
  
- Vous créez un blocage infini où tout le contenu est placé en conservation. Vous pouvez également créer une conservation basée sur une requête où seul le contenu qui correspond à une requête de recherche est mis en attente.
    
- Vous pouvez spécifier une plage de dates qui doit contenir uniquement le contenu qui a été envoyé, reçu ou créé au sein de cette plage de dates. Vous pouvez également conserver tout le contenu, quel que soit son moment d’envoi, de réception ou de création.
    
> [!NOTE]
> Vous pouvez avoir un maximum de 10 000 stratégies de blocage pour tous les cas eDiscovery de votre organisation. 
  
Pour créer une suspension pour un cas eDiscovery:
  
1. Dans le centre de sécurité & Compliance Center **** \> **** , cliquez sur eDiscovery eDiscovery pour afficher la liste des incidents de votre organisation. 
    
2. Cliquez sur **ouvrir** en regard du cas dans lequel vous souhaitez créer les suspensions. 
    
3. Sur la page d' **Accueil** de l’incident, cliquez sur l’onglet **blocage** . 
    
    ![Cliquez sur l’onglet blocage](media/3fef2db4-36de-4517-a34d-82f47b82d9bf.png)
  
4. Sur la page **suspension** , cliquez ![sur Ajouter](media/ITPro-EAC-AddIcon.gif) une icône **créer**.
    
5. Sur la page **nommer votre suspension** , donnez un nom. Le nom de la conservation doit être unique dans toute votre organisation. 
    
    ![Donnez un nom unique à votre conservation](media/7e15ea63-abd1-4f14-a29c-7ecfb9571d2c.png)
  
6. Module Dans la zone **Description** , ajoutez une description de la conservation. 
    
7. Cliquez sur **Suivant**.
    
8. Choisissez les emplacements de contenu que vous souhaitez mettre en attente. Vous pouvez placer les boîtes aux lettres, les sites et les dossiers publics en conservation.
    
    ![Choisissez les emplacements de contenu à mettre sous conservation](media/a59e4265-9151-4dbf-913f-6a4ab8db06b4.png)
  
   a. **Courrier Exchange** -cliquez sur **choisir les utilisateurs, les groupes ou les équipes** , puis cliquez sur **choisir les utilisateurs, les groupes ou les équipes** . pour spécifier les boîtes aux lettres à mettre en attente. Utilisez la zone de recherche pour rechercher des boîtes aux lettres utilisateur et des groupes de distribution (pour mettre en attente les boîtes aux lettres des membres du groupe) à mettre en attente. Vous pouvez également placer une conservation sur la boîte aux lettres associée pour un groupe Office 365 ou une équipe Microsoft. Activez la case à cocher utilisateur, groupe, équipe, cliquez sur **choisir**, puis sur **Terminer**.
    
    > [!NOTE]
    > Lorsque vous cliquez sur **choisir les utilisateurs, les groupes ou les équipes** pour spécifier les boîtes aux lettres à mettre en attente, le sélecteur de boîtes aux lettres affiché est vide. Il s’agit d’une conception qui améliore les performances. Pour ajouter des personnes à cette liste, tapez un nom (un minimum de 3 caractères) dans la zone de recherche. 
  
   b. **Sites SharePoint** : cliquez sur **choisir des sites** , puis cliquez à nouveau sur choisir les **sites** pour spécifier les sites SharePoint et OneDrive entreprise à mettre en attente. Saisissez l’URL de chaque site à placer en conservation. Vous pouvez également ajouter l’URL du site SharePoint pour un groupe Office 365 ou une équipe Microsoft. Cliquez sur **choisir**, puis sur **Terminer**.
    
    Consultez la section [plus d’informations](#more-information) pour obtenir des conseils sur la mise en attente des groupes Office 365 et de Microsoft Teams. 
    
    > [!NOTE]
    > Dans le cas rare où le nom d’utilisateur principal (UPN) d’une personne est modifié, l’URL de son compte OneDrive est également modifiée de façon à intégrer le nouvel UPN. Dans ce cas, vous devez modifier la conservation en ajoutant la nouvelle URL OneDrive de l’utilisateur et en supprimant l’ancienne. 
  
   c. **Dossiers publics Exchange** : déplacer le ![contrôle](media/963dfcd0-1765-4306-bcce-c3008c4406b9.png) bascule basculer vers la position **tout** pour mettre en attente tous les dossiers publics de votre organisation Exchange Online. Notez que vous ne pouvez pas choisir des dossiers publics spécifiques à mettre en attente. Laissez le commutateur Toggle défini sur **None** si vous ne souhaitez pas mettre de conservation sur les dossiers publics.
    
9. Lorsque vous avez terminé d’ajouter des emplacements de contenu au blocage, cliquez sur **suivant**.
    
10. Pour créer une conservation basée sur une requête avec des conditions, procédez comme suit. Dans le cas contraire, cliquez sur **suivant** .
    
    ![Créer une conservation basée sur une requête avec des conditions](media/d587b58e-d05c-4ac0-b0fe-09019e4f1063.png)
  
    
       a. Dans la zone sous **Mots clés**, tapez une requête de recherche dans le champ de sorte que seul le contenu qui répond aux critères de recherche est placé en conservation. Vous pouvez spécifier des mots clés, des propriétés de message ou des propriétés de document, telles que des noms de fichiers. Vous pouvez également utiliser des requêtes plus complexes qui utilisent un opérateur booléen, comme **and**, **or**ou **not**. Si vous laissez la zone mot clé vide, tout le contenu situé dans les emplacements de contenu spécifiés sera placé en conservation.
    
    b. Cliquez ![sur icône](media/ITPro-EAC-AddIcon.gif) ajouter des **conditions** pour ajouter une ou plusieurs conditions afin d’affiner la requête de recherche pour la suspension. Chaque condition ajoute une clause à la requête de recherche KQL créée et exécutée lors de la création de la suspension. Par exemple, vous pouvez spécifier une plage de dates pour que les documents de courrier ou de site créés dans la plage de dates soient suspendus. Une condition est connectée à la requête de mot-clé (spécifiée dans la zone de mot-clé) sur le plan logique par l’opérateur **AND**. Cela signifie que les éléments doivent satisfaire à la fois la requête de mot clé et la condition à mettre en attente.

    Pour plus d’informations sur la création d’une requête de recherche et l’utilisation de conditions, consultez la rubrique [requêtes de mots clés et conditions de recherche pour la recherche de contenu](keyword-queries-and-search-conditions.md).
    
11. Après avoir configuré une conservation basée sur une requête, cliquez sur **suivant**.
    
12. Vérifiez vos paramètres, puis cliquez sur **créer cette suspension**.
    
### <a name="hold-statistics"></a>Statistiques de conservation

Après un certain temps, des informations sur la nouvelle conservation s’affichent dans le volet **** d’informations de la page suspensions de la suspension sélectionnée. Ces informations incluent le nombre de boîtes aux lettres et de sites en conservation, ainsi que des statistiques sur le contenu qui a été placé en conservation, telles que le nombre total et la taille des éléments mis en attente et la dernière fois que les statistiques de conservation ont été calculées. Ces statistiques de suspension vous aident à identifier la proportion de contenu liée au cas eDiscovery. 
  
![Statistiques de conservation](media/575cfe0a-9210-4ae4-8df8-65665d66712e.png)
  
Gardez les points suivants à l’esprit concernant les statistiques de conservation:
  
- Le nombre total d’éléments en attente indique le nombre d’éléments de toutes les sources de contenu qui sont placées en conservation. Si vous avez créé une conservation basée sur une requête, cette statistique indique le nombre d’éléments qui correspondent à la requête.
    
- Le nombre d’éléments en attente inclut également les éléments non indexés trouvés dans les emplacements de contenu. Notez que si vous créez une conservation basée sur une requête, tous les éléments non indexés des emplacements de contenu sont placés en conservation. Cela inclut les éléments non indexés qui ne correspondent pas aux critères de recherche d’une conservation basée sur une requête et les éléments non indexés qui peuvent se situer en dehors d’une condition de plage de dates. Cette opération est différente de ce qui se passe lorsque vous exécutez une recherche de contenu, dans laquelle les éléments non indexés qui ne correspondent pas à la requête de recherche ou qui sont exclus par une condition de plage de dates ne sont pas inclus dans les résultats de la recherche. Pour plus d’informations sur les éléments non indexés, voir [éléments partiellement indexés dans la recherche de contenu dans Office 365](partially-indexed-items-in-content-search.md).
    
- Vous pouvez obtenir les dernières statistiques de conservation en cliquant sur **mettre à jour les statistiques** pour réexécuter une estimation de recherche qui calcule le nombre actuel d’éléments en attente. Si nécessaire, cliquez ****![sur Actualiser](media/O365-MDM-Policy-RefreshIcon.gif) l’actualisation dans la barre d’outils pour mettre à jour les statistiques de conservation dans le volet d’informations. 
    
- Il est normal que le nombre d’éléments bloqués augmente au fil du temps, car les utilisateurs dont la boîte aux lettres ou le site est en attente envoient généralement de nouveaux messages électroniques et créent des documents SharePoint et OneDrive entreprise.
    
> [!NOTE]
> Si un site SharePoint ou un compte OneDrive est déplacé vers une autre région dans un environnement multi-géo, les statistiques de ce site ne sont pas incluses dans les statistiques de conservation. Toutefois, le contenu du site reste bloqué. En outre, si un site est déplacé vers une autre région, l’URL affichée dans la conservation n’est pas mise à jour. Vous devrez modifier la conservation et mettre à jour l’URL. 
  
## <a name="step-5-create-and-run-a-content-search-associated-with-a-case"></a>Étape 5: créer et exécuter une recherche de contenu associée à un cas

Une fois le cas de découverte électronique créé et les dépositaires associés au cas placés en conservation, vous pouvez créer et exécuter des recherches de contenu associées au cas. Les recherches de contenu associées à un cas ne sont pas indiquées sur la page de **recherche** dans le centre de sécurité _AMP_ Compliance Center. Elles sont uniquement accessibles pour les membres du cas qui sont également membres du groupe de rôles Gestionnaire de découverte électronique. 
  
1. Dans le centre de sécurité & Compliance Center **** \> **** , cliquez sur eDiscovery eDiscovery pour afficher la liste des incidents de votre organisation. 
    
2. Cliquez sur **ouvrir** en regard du cas dans lequel vous souhaitez créer une recherche de contenu. 
    
3. Sur la page d' **Accueil** du cas, cliquez sur l’onglet **Rechercher** . 
    
    ![Onglet Rechercher](media/2e15fe32-1a2e-4588-ad0b-5d96f77cece9.png)
  
4. Sur la page **recherche** , cliquez ![sur Ajouter](media/ITPro-EAC-AddIcon.gif) une icône **nouvelle recherche**. 
    
5. Sur la page **Nouvelle recherche**, vous pouvez ajouter des mots clés et des conditions pour créer la requête de recherche. 
    
    ![Nouvelle recherche](media/0e9954e7-c0ea-4e05-820b-e4b81dc5f81d.png)
  
6. Vous pouvez spécifier des mots clés, des propriétés de message, telles que des dates d’envoi et de réception, ou des propriétés de document, telles que des noms de fichiers ou la date de la dernière modification d’un document. Vous pouvez utiliser des requêtes plus complexes qui utilisent un opérateur booléen, comme **and**, **or**, **not**, **near**ou **ONEAR**. Vous pouvez également rechercher des informations sensibles (telles que des numéros de sécurité sociale) dans des documents ou Rechercher des documents qui ont été partagés en externe. Si vous laissez la zone mot clé vide, tout le contenu situé dans les emplacements de contenu spécifiés sera inclus dans les résultats de la recherche. 
    
7. Vous pouvez activer la case à cocher **afficher la liste des mots clés** et taper un mot clé dans chaque ligne. Dans ce cas, les mots clés de chaque ligne sont connectés par l’opérateur **or** dans la requête de recherche qui est créée. 
    
    ![Liste de mots clés](media/29cceb5d-2817-4fc4-b91a-ced1c5824a17.png)
  
    Pourquoi utiliser la liste de mots clés? Vous pouvez obtenir des statistiques qui indiquent le nombre d’éléments qui correspondent à chaque mot clé. Cela peut vous aider à identifier rapidement les mots clés les plus efficaces (et les moins). Vous pouvez également utiliser une phrase de mots clés (entourée de parenthèses) dans une ligne. Pour plus d’informations sur les statistiques de recherche, voir [afficher les statistiques sur les mots clés pour les résultats de la recherche de contenu](view-keyword-statistics-for-content-search.md).
    
    Pour plus d’informations sur l’utilisation de la liste des mots clés, voir [création d’une requête de recherche](content-search.md#building-a-search-query).
    
8. Sous **conditions**, ajoutez des conditions à une requête de recherche pour affiner une recherche et renvoyer un ensemble plus raffiné de résultats. Chaque condition ajoute une clause à la requête de recherche KQL créée et exécutée lors du démarrage de la recherche. Une condition est logiquement connectée à la requête de mot clé (spécifiée dans la zone du mot clé) par l’opérateur **AND** . Cela signifie que les éléments doivent satisfaire la requête de mot-clé et la condition pour être inclus dans les résultats. C’est ainsi que les conditions contribuent à affiner vos résultats. 
    
    Pour plus d’informations sur la création d’une requête de recherche et l’utilisation de conditions, voir [Keyword queries for Content Search](keyword-queries-and-search-conditions.md).
    
9. Sous **emplacements: emplacements en attente**, choisissez les emplacements de contenu sur lesquels vous souhaitez effectuer la recherche. Vous pouvez rechercher des boîtes aux lettres, des sites et des dossiers publics dans la même recherche.
    
    ![Emplacements, en attente](media/d56398aa-0b20-4500-8e26-494eab92a99f.png)
  
    - **Tous les emplacements** : sélectionnez cette option pour rechercher tous les emplacements de contenu de votre organisation. Lorsque vous sélectionnez cette option, vous pouvez choisir d’effectuer une recherche dans toutes les boîtes aux lettres Exchange (qui inclut les boîtes aux lettres de tous les groupes Office 365 et Microsoft Teams), tous les sites SharePoint et OneDrive entreprise (qui incluent les sites pour tous les groupes Office 365 et Microsoft Teams) et tous les dossiers publics.
    
    - **Tous les emplacements en attente** : sélectionnez cette option pour rechercher tous les emplacements de contenu qui ont été mis en attente dans le cas. Si le cas contient plusieurs suspensions, les emplacements de contenu de toutes les suspensions sont recherchés lorsque vous sélectionnez cette option. En outre, si un emplacement de contenu a été placé sur une conservation basée sur une requête, seuls les éléments en attente feront l’objet d’une recherche lors de l’exécution de la recherche de contenu que vous créez au cours de cette étape. Par exemple, si un utilisateur a été placé sur une conservation de casse basée sur une requête qui conserve les éléments qui ont été envoyés ou créés avant une date spécifique, seuls ces éléments seraient recherchés à l’aide des critères de recherche de la recherche de contenu. Pour ce faire, vous connectez la requête de suspension de la casse et la requête de recherche de contenu par un opérateur **and** . Pour plus d’informations sur la recherche de contenu de cas, reportez-vous à la section [plus d’informations](#more-information) à la fin de cet article. 
    
    - **Emplacements spécifiques** : sélectionnez cette option pour sélectionner les boîtes aux lettres et les sites sur lesquels vous souhaitez effectuer la recherche. Lorsque vous sélectionnez cette option et que vous cliquez sur **modifier**, une liste d’emplacements apparaît. Vous pouvez choisir d’effectuer une recherche sur un ou l’ensemble des utilisateurs, des groupes, des équipes ou des emplacements de site.
    
      ![Sélectionner des emplacements spécifiques](media/97469b15-7be1-4aee-be27-f8343636152c.png)
  
      Vous pouvez également choisir d’effectuer une recherche dans tous les dossiers publics de votre organisation, mais si vous sélectionnez cette option et que vous recherchez tout emplacement de contenu en conservation, aucune requête d’une conservation de casse basée sur une requête ne sera appliquée à la requête de recherche. En d’autres termes, tout le contenu d’un emplacement est recherché, pas seulement le contenu qui est préservé par une suspension de casse basée sur une requête.
    
      Vous pouvez supprimer les emplacements de contenu de dossier pré-remplis ou en ajouter de nouveaux. Si vous choisissez cette option, vous avez également la possibilité de rechercher tous les emplacements de contenu d’un service spécifique (par exemple, rechercher toutes les boîtes aux lettres Exchange) ou vous pouvez rechercher des emplacements de contenu spécifiques pour un service. Vous pouvez également choisir de rechercher ou non les dossiers publics dans votre organisation.
    
      Gardez les points suivants à l’esprit lors de l’ajout d’emplacements de contenu à Rechercher:
    
      - Lorsque vous cliquez sur **choisir les utilisateurs, les groupes ou les équipes** pour spécifier les boîtes aux lettres à rechercher, le sélecteur de boîtes aux lettres affiché est vide. Il s’agit d’une conception qui améliore les performances. Pour ajouter des destinataires à cette liste, cliquez sur **choisir les utilisateurs, les groupes ou les équipes**, tapez un nom (un minimum de 3 caractères) dans la zone de recherche, activez la case à cocher en regard du nom, puis cliquez sur **choisir**. 
    
      - Vous pouvez ajouter des boîtes aux lettres inactives, des groupes Office 365, Microsoft teams et des groupes de distribution à la liste des boîtes aux lettres à rechercher. L’utilisation de groupes de distribution dynamique n’est pas prise en charge. Si vous ajoutez des groupes Office 365 ou Microsoft Teams, la boîte aux lettres de groupe ou d’équipe fait l’objet d’une recherche; les boîtes aux lettres des membres du groupe ne sont pas recherchées.
    
      - Pour ajouter des sites, cliquez sur **choisir des sites**, cliquez sur **choisir des sites** , puis tapez l’URL de chaque site sur lequel vous souhaitez effectuer la recherche. Vous pouvez également ajouter l’URL du site SharePoint pour les groupes Office 365 et Microsoft Teams. 
    
10. Une fois que vous avez sélectionné les emplacements de contenu à rechercher, cliquez sur **Terminer** , puis sur **Enregistrer**.
    
11. Sur la page **nouvelle recherche** , cliquez sur **Enregistrer** , puis tapez un nom pour la recherche. Les recherches de contenu associées à un cas doivent posséder des noms uniques au sein de votre organisation Office 365. 
    
12. Cliquez **sur &amp; enregistrer exécuter** pour enregistrer les paramètres de recherche. 
    
13. Entrez un nom unique pour la recherche, puis cliquez sur **Enregistrer** pour démarrer la recherche. 
    
    La recherche commence. Après un certain temps, une estimation des résultats de la recherche s’affiche dans le volet d’informations. L’estimation inclut la taille totale et le nombre d’éléments correspondant aux critères de recherche. L’estimation de la recherche inclut également le nombre d’éléments non indexés dans les emplacements de contenu qui ont été recherchés. Le nombre d’éléments non indexés qui ne répondent pas aux critères de recherche est inclus dans les statistiques de la recherche affichées dans le volet Détails. Si un élément non indexé correspond à la requête de recherche (étant donné que les autres propriétés du message ou du document répondent aux critères de recherche), il ne sera pas inclus dans le nombre estimé d’éléments non indexés. Si un élément non indexé est exclu par les critères de recherche, il ne sera pas inclus dans l’estimation des éléments non indexés.
    
  Une fois la recherche terminée, vous pouvez prévisualiser les résultats de recherche. Si nécessaire, cliquez ****![sur Actualiser](media/O365-MDM-Policy-RefreshIcon.gif) l’actualisation pour mettre à jour les informations dans le volet d’informations. 
    
## <a name="step-6-export-the-results-of-a-content-search-associated-with-a-case"></a>Étape 6: exporter les résultats d’une recherche de contenu associée à un cas

Une fois la recherche exécutée, vous pouvez exporter les résultats de la recherche. Lorsque vous exportez des résultats de recherche, les éléments de boîte aux lettres sont téléchargés dans des fichiers PST ou des messages individuels. Lorsque vous exportez du contenu à partir de sites SharePoint et OneDrive entreprise, des copies de documents Office natifs et d’autres documents sont exportées. Un fichier manifeste (au format XML) qui contient des informations sur chaque résultat de recherche est également exporté.
  
Vous pouvez exporter les résultats d’une [seule recherche associée à un cas](#export-the-results-of-a-single-search-associated-with-a-case) ou vous pouvez exporter les résultats de [plusieurs recherches associées à un cas](#export-the-results-of-multiple-searches-associated-with-a-case).
  
### <a name="export-the-results-of-a-single-search-associated-with-a-case"></a>Exporter les résultats d’une recherche unique associée à un cas

1. Dans le centre de sécurité & Compliance Center **** \> **** , cliquez sur eDiscovery eDiscovery pour afficher la liste des incidents de votre organisation. 
    
2. Cliquez sur **ouvrir** en regard du cas à partir duquel vous souhaitez exporter la recherche. 
    
3. Sur la page d' **Accueil** du cas, cliquez sur **Rechercher**.
    
4. Dans la liste des recherches pour le cas, cliquez sur la recherche à partir de laquelle vous souhaitez exporter les résultats ![de la recherche,](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) cliquez sur Exporter les résultats de la recherche **plus**, puis sélectionnez **Exporter les résultats** dans la liste déroulante. 
    
    La page **Exporter les résultats** s’affiche. 
    
    ![Page exporter les résultats](media/ab0bb46d-310b-4374-8644-717146df6676.png)
  
    Le flux de travail pour exporter les résultats d’une recherche de contenu associée à un cas est le même flux qui sert à exporter les résultats pour une recherche effectuée sur la page **Recherche de contenu**. Pour obtenir des instructions détaillées, voir [Export content Search Results](export-search-results.md).
    
    > [!NOTE]
    > Lorsque vous exportez des résultats de recherche, vous avez la possibilité d’activer la déduplication de sorte qu’une seule copie d’un message électronique soit exportée même si plusieurs instances du même message ont pu être trouvées dans les boîtes aux lettres qui ont été recherchées. Pour plus d’informations sur la déduplication et sur l’identification des éléments dupliqués, voir [déduplication dans les résultats de recherche de découverte électronique](de-duplication-in-ediscovery-search-results.md). 
  
5. Cliquez sur l’onglet **Exporter** pour afficher la liste des travaux d’exportation qui existent dans ce cas. 
    
    ![Onglet exporter](media/1b84c45e-4ec9-4ecd-9e07-eaf8fc4cc307.png)
  
    Vous devrez peut-être ****![cliquer sur Actualiser l’icône](media/O365-MDM-Policy-RefreshIcon.gif) actualiser pour mettre à jour la liste des travaux d’exportation afin d’afficher le travail d’exportation que vous venez de créer. Notez que les travaux d’exportation portent le même nom que la recherche de contenu correspondante avec **_Export** ajouté à la fin du nom de recherche. 
    
6. Cliquez sur le travail d’exportation que vous venez de créer pour afficher les informations d’État dans le volet d’informations. Ces informations incluent le pourcentage d’éléments qui ont été transférés vers une zone de stockage Azure dans le Cloud Microsoft.
    
    Une fois que tous les éléments ont été transférés, cliquez sur **Télécharger les résultats** pour télécharger les résultats de la recherche sur votre ordinateur local. Pour plus d’informations, reportez-vous à l’étape 2 dans [exporter des résultats de recherche de contenu](export-search-results.md)
    
### <a name="export-the-results-of-multiple-searches-associated-with-a-case"></a>Exporter les résultats de plusieurs recherches associées à un cas

En guise d’alternative à l’exportation des résultats d’une recherche de contenu unique associée à un cas, vous pouvez exporter les résultats de plusieurs recherches à partir de la même casse dans une seule exportation. L’exportation des résultats de plusieurs recherches est plus rapide et plus facile que l’exportation des résultats d’une recherche à la fois.
  
> [!NOTE]
> Vous ne pouvez pas exporter les résultats de plusieurs recherches si l’une de ces recherches a été configurée pour effectuer une recherche dans le contenu de tous les cas. exportez uniquement les résultats de plusieurs recherches de recherches associées à un cas de découverte électronique. Vous ne pouvez pas exporter les résultats de plusieurs recherches figurant sur la page **recherche de contenu** dans le centre de sécurité _AMP_ Compliance Center. 
  
1. Dans le centre de sécurité & Compliance Center **** \> **** , cliquez sur eDiscovery eDiscovery pour afficher la liste des incidents de votre organisation. 
    
2. Cliquez sur **ouvrir** en regard du cas à partir duquel vous souhaitez exporter les résultats de la recherche. 
    
3. Sur la page d' **Accueil** du cas, cliquez sur **Rechercher**.
    
4. Dans la liste des recherches pour le cas, sélectionnez au moins deux recherches dont vous souhaitez exporter les résultats de recherche.
    
    > [!NOTE]
    > Pour sélectionner plusieurs recherches, appuyez sur Ctrl tout en cliquant sur chaque recherche. Ou vous pouvez sélectionner plusieurs recherches adjacentes en cliquant sur la première recherche, en maintenant enfoncée la touche Maj, puis en cliquant sur la dernière recherche. 
  
5. Une fois que vous avez sélectionné les recherches, la page **actions en bloc** s’affiche. 
    
    ![Dans la page actions en bloc, cliquez sur Exporter les résultats](media/f34e3707-a9c1-494f-91a4-da1165aa730a.png)
  
    
6. Cliquez ![sur Exporter les résultats](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) de la recherche **Exporter les résultats**.

7. Sur la page **Exporter les résultats** , attribuez un nom unique à l’exportation, sélectionnez les options de sortie, puis choisissez comment votre contenu sera exporté. Cliquez sur **Exporter**.
    
    Le flux de travail d’exportation des résultats à partir de plusieurs recherches de contenu associées à un cas revient à exporter les résultats de la recherche pour une seule recherche. Pour obtenir des instructions détaillées, voir [Export content Search Results](export-search-results.md).
    
    > [!NOTE]
    > Lorsque vous exportez des résultats de recherche à partir de plusieurs recherches associées à un cas, vous avez également la possibilité d’activer la déduplication de sorte qu’une seule copie d’un message électronique soit exportée même si plusieurs instances du même message ont pu être trouvées dans le boîtes aux lettres ayant fait l’objet d’une recherche dans une ou plusieurs recherches. Pour plus d’informations sur la déduplication et sur l’identification des éléments dupliqués, voir [déduplication dans les résultats de recherche de découverte électronique](de-duplication-in-ediscovery-search-results.md). 
  
8. Une fois l’exportation démarrée, cliquez sur l’onglet **Exporter** pour afficher la liste des travaux d’exportation pour ce cas. 
    
    ![Onglet exporter, recherches multiples](media/b9505e1b-559f-4a8c-96b3-a3f734753926.png)
  
    Vous devrez peut-être **** ![cliquer sur Actualiser l’icône](media/O365-MDM-Policy-RefreshIcon.gif) actualiser pour mettre à jour la liste des travaux d’exportation afin d’afficher le travail d’exportation que vous venez de créer. Notez que les recherches comprises dans la tâche d’exportation sont répertoriées dans la colonne **recherches** . 
    
8. Cliquez sur le travail d’exportation que vous venez de créer pour afficher les informations d’État dans le volet d’informations. Ces informations incluent le pourcentage d’éléments qui ont été transférés vers une zone de stockage Azure dans le Cloud Microsoft.
    
9. Une fois que tous les éléments ont été transférés, cliquez sur **Télécharger les résultats** pour télécharger les résultats de la recherche sur votre ordinateur local. Pour plus d’informations, reportez-vous à l’étape 2 dans exporter les résultats de la [recherche de contenu](export-search-results.md).
    
#### <a name="more-information-about-exporting-the-results-of-multiple-searches"></a>Plus d’informations sur l’exportation des résultats de plusieurs recherches

- Lorsque vous exportez les résultats de plusieurs recherches, les requêtes de recherche de toutes les recherches sont combinées à l’aide d’opérateurs **or** , puis la recherche combinée est démarrée. Les résultats estimés de la recherche combinée sont affichés dans le volet d’informations de la tâche d’exportation sélectionnée. Les résultats de la recherche sont ensuite transférés vers la zone de stockage Azure dans le Cloud Microsoft. L’état du transfert s’affiche également dans le volet d’informations. Comme indiqué précédemment, après le transfert de tous les résultats de la recherche, vous pouvez les télécharger sur votre ordinateur local. 
    
- Le nombre maximal de mots clés dans les requêtes de recherche pour toutes les recherches que vous souhaitez exporter est 500. (il s’agit de la même limite pour une seule recherche de contenu). Cela est dû au fait que le travail d’exportation combine toutes les requêtes de recherche à l’aide de l’opérateur **or** . Si vous dépassez cette limite, une erreur est renvoyée. Dans ce cas, vous devez exporter les résultats à partir d’un nombre réduit de recherches ou simplifier les requêtes de recherche des recherches que vous souhaitez exporter. 
    
- Les résultats de recherche exportés sont organisés par la source de contenu dans laquelle l’élément a été trouvé. Cela signifie qu’une source de contenu dans les résultats d’exportation peut avoir des éléments renvoyés par des recherches différentes. Par exemple, si vous avez choisi d’exporter des messages électroniques dans un fichier PST pour chaque boîte aux lettres, le fichier PST peut avoir des résultats provenant de plusieurs recherches.
    
- Si le même élément ou document de courrier à partir du même emplacement de contenu est renvoyé par plusieurs des recherches que vous exportez, seule une copie de l’élément sera exportée.
    
- Vous ne pouvez pas modifier une exportation pour plusieurs recherches une fois que vous l’avez créée. Par exemple, vous ne pouvez pas ajouter ou supprimer des recherches à partir de l’exportation. Vous devrez créer une nouvelle tâche d’exportation pour modifier les résultats de la recherche qui sont exportés. Une fois qu’une tâche d’exportation est créée, vous pouvez uniquement télécharger les résultats sur un ordinateur, redémarrer l’exportation ou supprimer le travail d’exportation.
    
- Si vous redémarrez l’exportation, toute modification apportée aux requêtes des recherches qui composent la tâche d’exportation n’affecte pas les résultats de la recherche qui seront récupérés. Lorsque vous redémarrez une exportation, le même travail de requête de recherche combiné qui a été exécuté lors de la création du travail d’exportation sera réexécuté.
    
- Si vous redémarrez une exportation **** à partir de la page exports dans un cas eDiscovery, les résultats de la recherche transférés vers la zone de stockage Azure remplacent les résultats précédents; les résultats précédents qui ont été transférés ne seront pas disponibles pour être téléchargés. 
    
- La préparation des résultats de plusieurs recherches d’analyse dans Advanced eDiscovery n’est pas disponible. Vous pouvez uniquement préparer les résultats d’une recherche d’analyse unique dans Advanced eDiscovery.

## <a name="step-7-prepare-search-results-for-advanced-ediscovery"></a>Étape 7: préparer les résultats de recherche pour Advanced eDiscovery

Si votre organisation a un abonnement Office 365 E5, vous pouvez préparer les résultats des recherches de contenu associées à un cas d’analyse dans Advanced eDiscovery. Une fois que vous avez préparé les résultats de la recherche, vous pouvez accéder à Advanced eDiscovery (voir [étape 8: atteindre le cas dans Advanced eDiscovery](#step-8-go-to-the-case-in-advanced-ediscovery)) et traiter les données de résultats de recherche pour une analyse approfondie dans Advanced eDiscovery.
  
Lorsque vous préparez des résultats de recherche pour Advanced eDiscovery, la fonctionnalité de reconnaissance optique de caractères (OCR) extrait automatiquement le texte des images. La reconnaissance optique de caractères est prise en charge pour les fichiers libres, les pièces jointes et les images incorporées. Cela vous permet d’appliquer les fonctionnalités d’analyse textuelle de la découverte électronique avancée (quasi-doublons, du Threading de courrier électronique, des thèmes et du codage prédictif) à n’importe quel texte dans des fichiers image.
  
> [!NOTE]
> Pour analyser les données d’un utilisateur à l’aide de Advanced eDiscovery, l’utilisateur (le dépositaire des données) doit disposer d’une licence Office 365 E5. Par ailleurs, les utilisateurs disposant d’une licence Office 365 E1 ou E3 peuvent se voir attribuer une licence avancée eDiscovery autonome. Les administrateurs et les responsables de la mise en conformité qui sont affectés à des cas et utilisent Advanced eDiscovery pour analyser les données n’ont pas besoin d’une licence E5. 
  
1. Dans le centre de sécurité & Compliance Center **** \> **** , cliquez sur eDiscovery eDiscovery pour afficher la liste des incidents de votre organisation. 
    
2. Cliquez sur **ouvrir** en regard du cas pour lequel vous souhaitez préparer les résultats de recherche pour l’analyse dans Advanced eDiscovery. 
    
3. Sur la page d' **Accueil** du cas, cliquez sur **Rechercher**, puis sélectionnez la recherche.
    
4. Dans le volet d’informations, ![cliquez sur Exporter les](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) résultats de recherche **plus en plus**, puis sur **préparer pour Advanced eDiscovery**.
    
    ![Préparer vos résultats pour Advanced eDiscovery](media/b6548ff0-a6e9-42b1-9ae4-5c15146f5690.png)
  
5. Sur la page **préparer pour Advanced eDiscovery** , choisissez de préparer l’une des opérations suivantes: 
    
    - Tous les éléments, à l’exception de ceux dont le format n’est pas reconnu, sont chiffrés ou n’ont pas été indexés pour d’autres raisons.
    
    - Tous les éléments, y compris ceux dont le format n’est pas reconnu, sont chiffrés ou n’ont pas été indexés pour d’autres raisons.
    
    - Seuls les éléments dont le format n’est pas reconnu sont chiffrés ou n’ont pas été indexés pour d’autres raisons.
    
6. Module Activez la case à cocher **inclure les versions pour les fichiers SharePoint** . 
    
7. Cliquez sur **Préparer**.
    
    Les résultats de la recherche sont préparés pour analyse avec Advanced eDiscovery.
    
8. Cliquez sur **Fermer** pour fermer le volet d’informations. 
    
## <a name="step-8-go-to-the-case-in-advanced-ediscovery"></a>Étape 8: atteindre le cas dans Advanced eDiscovery

Une fois que vous avez créé un cas dans le centre de sécurité & Compliance Center, vous pouvez accéder à la même affaire dans Advanced eDiscovery.
  
Pour accéder à un cas dans Advanced eDiscovery :
  
1. Dans le centre de sécurité & Compliance Center **** \> **** , cliquez sur eDiscovery eDiscovery pour afficher la liste des incidents de votre organisation. 
    
2. Cliquez sur **ouvrir** en regard du cas que vous souhaitez atteindre dans Advanced eDiscovery. 
    
3. Sur la page d' **Accueil** du cas, cliquez sur **basculer vers Advanced eDiscovery**.
    
    ![Sélectionnez basculer vers Advanced eDiscovery](media/d7e31558-e79c-4782-b841-2b735568a576.png)
  
    La barre **de progression de la connexion à Advanced eDiscovery** s’affiche. Lorsque vous êtes connecté à Advanced eDiscovery, une liste de conteneurs s’affiche sur la page. 
    
    ![Barre de progression avancée de eDiscorvery](media/4a84273d-765b-44b8-9006-c20e810ea393.png)
  
    Ces conteneurs représentent les résultats de recherche que vous avez préparés pour l’analyse dans Advanced eDiscovery à l’étape 7. Notez que le nom du conteneur porte le même nom que la recherche de contenu dans le centre de sécurité & Compliance Center. Les conteneurs de la liste sont ceux que vous avez préparés. Si un autre utilisateur a préparé des résultats de recherche pour Advanced eDiscovery, les conteneurs correspondants ne seront pas inclus dans la liste.
    
4. Pour charger les données de résultats de recherche d’un conteneur vers le cas dans Advanced eDiscovery, sélectionnez un conteneur et cliquez sur **traiter**.
    
    Pour plus d’informations sur la façon de traiter des conteneurs, voir [exécuter le module de processus et charger des données dans Office 365 Advanced eDiscovery](run-the-process-module-and-load-data-in-advanced-ediscovery.md).
    
> [!TIP]
> Cliquez sur **basculer vers eDiscovery** pour revenir au même cas dans le centre de sécurité _AMP_ Compliance Center. 
  
## <a name="optional-step-9-close-a-case"></a>Module Étape 9: fermer un incident

Lorsque le cas juridique ou l’enquête pris en charge par un cas de découverte électronique est terminé, vous pouvez fermer le cas. Voici ce qui se passe lorsque vous fermez un cas:
  
- Si le cas contient des emplacements de contenu en conservation, ceux-ci sont désactivés. Cela peut entraîner la suppression ou le vidage définitifs du contenu, soit par l’utilisateur, soit par un processus automatisé, tel qu’une stratégie de suppression.
    
- La fermeture d’un incident ne désactive que les blocages associés à ce cas. Si d’autres suspensions sont placées sur un emplacement de contenu (comme une conservation pour litige). une stratégie de conservation, ou une suspension d’un autre cas de découverte électronique (eDiscovery), ces conservations seront toujours conservées.
    
- Le cas est toujours mentionné sur la page eDiscovery dans le centre de sécurité & Compliance Center. Les détails, les conservations, les recherches et les membres d’un cas fermé sont conservés.
    
- Vous pouvez modifier un cas après sa fermeture. Par exemple, vous pouvez ajouter ou supprimer des membres, créer des recherches, exporter des résultats de recherche et préparer des résultats de recherche pour analyse dans Advanced eDiscovery. La principale différence entre les cas actifs et fermés est que les conservations sont désactivées lors de la fermeture d’un cas.
    
Pour fermer un incident:
  
1. Dans le centre de sécurité & Compliance Center **** \> **** , cliquez sur eDiscovery eDiscovery pour afficher la liste des incidents de votre organisation. 
    
2. Cliquez sur le nom de l’incident que vous souhaitez fermer.
    
    La page flyout **gérer ce cas** s’affiche. 
    
3. Sous **gérer l’État**du cas ![, cliquez sur supprimer](media/b6512677-5e7b-42b0-a8a3-3be1d7fa23ee.gif) le **cas de fermeture**du bouton Peek.
    
    Un avertissement s’affiche indiquant que les conservations associées à la casse seront désactivées.
    
4. Cliquez sur **Oui** pour fermer le cas. 
    
    L’état de la page flyout **gérer ce cas** passe de **actif** à **Fermer**.
    
5. Fermez la page **gérer ce cas** . 
    
6. Sur la page **eDiscovery** , cliquez ![sur Actualiser l’icône](media/O365-MDM-Policy-RefreshIcon.gif) **Actualiser** pour mettre à jour l’état du cas fermé. Le processus de clôture peut prendre jusqu’à 60 minutes. 
    
    Une fois le processus terminé, l’état du cas est modifié sur **fermé** sur la page **eDiscovery** . Cliquez de nouveau sur le nom de l’incident pour afficher la page de démarrage **gérer cet incident** , qui contient des informations sur la date et l’auteur de la fermeture du dossier. 
     
## <a name="optional-step-10-re-open-a-closed-case"></a>Module Étape 10: rouvrir un litige clos

Lorsque vous rouvrez un cas, les conservations qui étaient en place lors de la fermeture de l’incident ne sont pas automatiquement rétablis. Une fois le cas rouvert, vous devez accéder à la page de **blocage** et activer les suspensions précédentes. Pour activer une suspension, sélectionnez-la et cliquez sur **activer** dans le volet d’informations. 
  
1. Dans le centre de sécurité & Compliance Center **** \> **** , cliquez sur eDiscovery eDiscovery pour afficher la liste des incidents de votre organisation. 
    
2. Cliquez sur le nom de l’incident à rouvrir.
    
    La page flyout **gérer ce cas** s’affiche. 
    
3. Sous **gérer le statut du cas**, cliquez sur **rouvrir le cas**.
    
    Un avertissement s’affiche indiquant que les conservations associées à la casse lorsqu’elle a été fermée ne sont pas activées automatiquement.
    
4. Cliquez sur **Oui** pour rouvrir le cas. 
    
    L’état de la page flyout **gérer ce cas** passe de **fermé** à **actif**.
    
5. Fermez la page **gérer ce cas** . 
    
6. Sur la page **eDiscovery** , cliquez ![sur Actualiser l’icône](media/O365-MDM-Policy-RefreshIcon.gif) **Actualiser** pour mettre à jour l’état du cas rouvert. Le processus de réouverture peut prendre jusqu’à 60 minutes. 
    
    Une fois le processus terminé, l’état du cas est modifié sur **actif** sur la page **eDiscovery** . 
  
## <a name="more-information"></a>Plus d’informations

- **Existe-t-il des limites pour les cas eDiscovery ou les conservations associés à un cas de découverte électronique?** Le tableau suivant répertorie les limites pour les cas de découverte électronique et les conservations de casse.
    
  |**Description de la limite**|**Limite**|
  |:-----|:-----|
  |Nombre maximal de cas pour une organisation  <br/> |Sans limite  <br/> |
  |Nombre maximal de blocages pour une organisation  <br/> |10 000  <br/> |
  |Nombre maximal de boîtes aux lettres en une seule suspension de cas  <br/> |1,000  <br/> |
  |Nombre maximal de sites SharePoint et OneDrive entreprise en une seule suspension de cas  <br/> |100  <br/> |
   
- **Qu’en est-il des cas qui ont été créés sur la page de gestion des dossiers dans Advanced eDiscovery?** Vous pouvez accéder à la liste des anciens cas de découverte électronique avancée en cliquant sur le lien situé en bas de la page **eDiscovery** dans le centre de sécurité _AMP_ Compliance Center. Toutefois, pour effectuer un travail dans un cas plus ancien, vous devez contacter le support Office 365 et demander que le cas soit déplacé vers un nouveau cas eDiscovery dans le centre de sécurité & Compliance Center. 
    
- **Pourquoi créer un administrateur de découverte électronique ?** Comme indiqué précédemment, un administrateur de découverte électronique est membre du groupe de rôles de gestionnaire de découverte électronique, qui peut afficher tous les cas de découverte électronique, et y accéder, de votre organisation. Cette capacité d’accès à tous les cas de découverte électronique a deux objectifs importants :
    
  - Si une personne qui est le seul membre d’un cas de découverte électronique quitte votre organisation, personne (y compris les membres du groupe de rôles de gestion de l’organisation ou un autre membre du groupe de rôles de gestionnaire de découverte électronique) ne peut accéder à ce cas, car personne n’en est alors membre. Dans ce cas, il n’y aurait aucun moyen d’accéder aux données dans le cas. Toutefois, étant donné qu’un administrateur de découverte électronique peut accéder à tous les cas eDiscovery au sein de l’organisation, il peut afficher le cas dans le centre de sécurité & Compliance Center et s’ajouter eux-mêmes ou un autre gestionnaire eDiscovery en tant que membre du cas.
    
  - Étant donné qu’un administrateur de découverte électronique peut afficher et accéder à tous les cas eDiscovery, ils peuvent auditer et superviser tous les cas et les recherches de contenu associées. Cela contribue à empêcher toute utilisation abusive des recherches de contenu ou des cas de découverte électronique. Néanmoins, sachant que les administrateurs de découverte électronique peuvent accéder à des informations potentiellement sensibles dans les résultats d’une recherche de contenu, vous devez limiter le nombre d’administrateurs de découverte électronique.
    
    Enfin, comme expliqué précédemment, les administrateurs eDiscovery dans le centre de sécurité & Compliance Center sont automatiquement ajoutés en tant qu’administrateurs dans Advanced eDiscovery. Cela signifie qu’une personne qui est un administrateur de découverte électronique peut effectuer des tâches administratives dans Advanced eDiscovery, telles que la configuration des utilisateurs, la création de cas et l’ajout de données à des cas.
    
- **Quelles sont les exigences en matière de licences pour placer des emplacements de contenu en conservation?** En règle générale, les organisations nécessitent un abonnement Office 365 E3 ou une version ultérieure pour placer les emplacements de contenu en conservation. Pour placer des boîtes aux lettres en conservation, une licence Exchange Online plan 2 est requise pour la boîte aux lettres que vous souhaitez mettre en attente.
    
- **Que devez-vous savoir d’autre sur la recherche de tout le contenu des dossiers à l’étape 5?** Comme expliqué précédemment, vous pouvez rechercher les emplacements de contenu qui ont été mis en attente dans le cas. Dans ce cas, seul le contenu correspondant aux critères de suspension est recherche. S’il n’existe aucun critère de conservation, tout le contenu est recherché. Si le contenu se trouve sur une conservation basée sur une requête, seul le contenu qui correspond aux deux critères de conservation (à partir de la suspension effectuée à l’étape 4) et les critères de recherche (de la recherche à l’étape 5) sont renvoyés avec les résultats de la recherche.
    
    Voici quelques autres éléments à garder à l’esprit lors de la recherche de tout le contenu des cas:
    
  - Si un emplacement de contenu fait partie de plusieurs suspensions dans le même cas, les requêtes de conservation sont combinées par un opérateur **or** lorsque vous effectuez une recherche dans cet emplacement de contenu à l’aide de l’option tout le contenu du cas. De même, si un emplacement de contenu fait partie de deux conservations différentes, où l’une est basée sur une requête et l’autre sur un blocage infini (où tout le contenu est placé en conservation), tout le contenu fera l’objet d’une recherche en raison de la suspension infinie. 
    
  - Si une recherche de contenu concerne un cas et que vous l’avez configurée pour effectuer une recherche dans le contenu de tous les cas, puis que vous modifiez une conservation (en ajoutant ou en supprimant un emplacement de contenu ou en modifiant la requête de blocage), la configuration de la recherche est mise à jour avec ces modifications. Toutefois, vous devez réexécuter la recherche après la modification de la conservation pour mettre à jour les résultats de la recherche.
    
  - Si plusieurs blocages de casse sont placés à un emplacement de contenu dans un cas de découverte électronique et que vous choisissez d’effectuer une recherche dans le contenu de tous les cas, le nombre maximal de mots clés pour cette requête de recherche est de 500. Cela est dû au fait que la recherche de contenu combine toutes les conservations basées sur une requête à l’aide de l’opérateur **or** . S’il y a plus de 500 mots clés dans les requêtes de blocage combiné et la requête de recherche de contenu, tout le contenu de la boîte aux lettres est recherché, et pas seulement celui qui correspond à l’une des suspensions de cas basées sur une requête. 
    
  - Si l’état d’une conservation case est activé, vous pouvez toujours effectuer des recherches **dans**les emplacements de contenu de cas pendant que la conservation est activée.
    
  - Comme indiqué précédemment, si une recherche est configurée pour effectuer une recherche dans le contenu de tous les cas, vous ne pouvez pas inclure cette recherche si vous voulez exporter les résultats de plusieurs recherches. Si une recherche est configurée pour effectuer une recherche dans le contenu de tous les cas, vous devez exporter les résultats de cette recherche unique.
    
- **Si une boîte aux lettres, un site SharePoint ou un compte OneDrive en attente est déplacé vers une autre région dans un environnement multi-géo, la conservation reste-t-elle appliquée?** Dans tous les cas, le contenu d’une boîte aux lettres, d’un site ou d’un compte OneDrive reste conservé. Toutefois, les statistiques de conservation n’incluent plus d’éléments provenant d’un emplacement de contenu qui a été déplacé vers une autre région. Pour inclure les statistiques de conservation pour un emplacement de contenu qui a été déplacé, vous devez modifier la conservation et mettre à jour l’URL (ou l’adresse SMTP d’une boîte aux lettres) de sorte que l’emplacement de contenu soit de nouveau inclus dans les statistiques de conservation. 
    
- **Qu’en est-il de la mise en attente sur les groupes Office 365 et Microsoft teams?** Microsoft teams est basé sur les groupes Office 365. Par conséquent, leur mise en attente dans un cas eDiscovery est très similaire. Gardez les points suivants à l’esprit lorsque vous importez des groupes Office 365 et Microsoft teams en conservation. 
    
  - Pour placer le contenu situé dans les groupes Office 365 et Microsoft teams en conservation, vous devez spécifier la boîte aux lettres et le site SharePoint associés à un groupe ou une équipe.
    
  - Exécutez la cmdlet **Get-UnifiedGroup** dans Exchange Online pour afficher les propriétés d’un groupe ou d’une équipe microsoft Office 365. Il s’agit d’un moyen efficace pour obtenir l’URL du site associé à un groupe Office 365 ou une équipe Microsoft. Par exemple, la commande suivante affiche les propriétés sélectionnées pour un groupe Office 365 nommé équipe leadership senior: 
    
     ```
    Get-UnifiedGroup "Senior Leadership Team" | FL DisplayName,Alias,PrimarySmtpAddress,SharePointSiteUrl

     DisplayName            : Senior Leadership Team
     Alias                  : seniorleadershipteam
     PrimarySmtpAddress     : seniorleadershipteam@contoso.onmicrosoft.com
     SharePointSiteUrl      : https://contoso.sharepoint.com/sites/seniorleadershipteam
    ```

    > [!NOTE]
    > Pour exécuter la cmdlet **Get-UnifiedGroup** , vous devez disposer du rôle destinataires en affichage seul dans Exchange Online ou être membre d’un groupe de rôles auquel est affecté le rôle destinataires en affichage seul. 
  
  - Lors de la recherche dans la boîte aux lettres d’un utilisateur, le groupe Office 365 ou l’équipe Microsoft dont l’utilisateur est membre ne feront pas l’objet d’une recherche. De même, lorsque vous placez un groupe Office 365 ou un blocage d’équipe Microsoft, seule la boîte aux lettres de groupe et le site de groupe sont mis en attente; les boîtes aux lettres et les sites OneDrive entreprise des membres du groupe ne sont pas mis en attente, sauf si vous les ajoutez explicitement à la suspension. Par conséquent, si vous devez placer un groupe Office 365 ou Microsoft Team en attente pour des raisons juridiques, songez à ajouter les boîtes aux lettres et les sites OneDrive entreprise pour les membres d’équipe et de groupe sur le même blocage.
    
  - Pour obtenir la liste des membres d’un groupe ou d’une équipe Microsoft Office 365, vous pouvez afficher les propriétés sur la page **groupes d’accueil \> ** dans le centre d’administration Microsoft 365. Vous pouvez également exécuter la commande suivante dans Exchange Online PowerShell: 
    
      ```
      Get-UnifiedGroupLinks <group or team name> -LinkType Members | FL DisplayName,PrimarySmtpAddress 
      ```

    > [!NOTE]
    > Pour exécuter la cmdlet **Get-UnifiedGroupLinks** , vous devez disposer du rôle destinataires en affichage seul dans Exchange Online ou être membre d’un groupe de rôles auquel est affecté le rôle destinataires en affichage seul. 
  
  - Les conversations qui font partie d’un canal Microsoft teams sont stockées dans la boîte aux lettres associée à l’équipe Microsoft. De même, les fichiers que les membres de l’équipe partagent dans un canal sont stockés sur le site SharePoint de l’équipe. Par conséquent, vous devez placer la boîte aux lettres d’équipe Microsoft et le site SharePoint en conservation pour conserver les conversations et les fichiers dans un canal.
    
    En guise d’alternative, les conversations qui font partie de la liste de conversation de Microsoft teams sont stockées dans la boîte aux lettres de l’utilisateur qui participe à la conversation. Et les fichiers qu’un utilisateur partage dans les conversations de conversation sont stockés dans le site OneDrive entreprise de l’utilisateur qui partage le fichier. Par conséquent, vous devez placer les boîtes aux lettres des utilisateurs individuels et les sites OneDrive entreprise en conservation pour conserver les conversations et les fichiers dans la liste des conversations. C’est pourquoi il est recommandé de placer une conservation sur les boîtes aux lettres des membres d’une équipe Microsoft en plus de placer la boîte aux lettres d’équipe (et le site) en conservation.
    
    > [!IMPORTANT]
    > Les utilisateurs qui participent à des conversations faisant partie de la liste des conversations de Microsoft teams doivent disposer d’une boîte aux lettres Exchange Online (en nuage) pour conserver les conversations de conversation lorsque la boîte aux lettres est placée sur une conservation eDiscovery. Cela est dû au fait que les conversations faisant partie de la liste des conversations sont stockées dans les boîtes aux lettres en nuage des participants à la conversation. Si un participant à une conversation ne dispose pas d’une boîte aux lettres Exchange Online, vous ne pourrez pas conserver les conversations de conversation. Par exemple, dans un déploiement hybride Exchange, les utilisateurs disposant d’une boîte aux lettres locale peuvent participer à des conversations qui font partie de la liste des conversations de Microsoft Teams. Toutefois, dans ce cas, le contenu de cette conversation ne peut pas être conservé car les utilisateurs n’ont pas de boîtes aux lettres en nuage. 
  
  - Chaque canal d’équipe ou d’équipe Microsoft contient un wiki pour la prise de notes et la collaboration. Le contenu wiki est automatiquement enregistré dans un fichier au format. mht. Ce fichier est stocké dans la bibliothèque de documents de données wiki teams sur le site SharePoint de l’équipe. Vous pouvez placer le contenu du wiki en conservation en mettant le site SharePoint de l’équipe en conservation.
    
    > [!NOTE]
    > La capacité à conserver du contenu wiki pour une équipe Microsoft ou un canal d’équipe (lorsque vous placez le blocage du site SharePoint de l’équipe) a été publiée le 22 juin 2017. Si un site d’équipe est en conservation, le contenu wiki est conservé à partir de cette date. Toutefois, si un site d’équipe est en conservation et que le contenu wiki a été supprimé avant le 22 juin 2017, le contenu wiki n’a pas été conservé. 
  
- **Comment puis-je trouver l’URL des sites OneDrive entreprise?** Pour collecter une liste des URL pour les sites OneDrive entreprise de votre organisation afin de pouvoir les ajouter à une suspension ou une recherche associée à un cas eDiscovery, consultez la rubrique [créer une liste de tous les emplacements OneDrive de votre organisation](https://support.office.com/article/8e200cb2-c768-49cb-88ec-53493e8ad80a). Ce script dans cet article crée un fichier texte qui contient une liste de tous les sites OneDrive. Pour exécuter ce script, vous devez installer et utiliser SharePoint Online Management Shell. Veillez à ajouter l’URL du domaine mon site de votre organisation à chaque site OneDrive que vous souhaitez rechercher. Il s’agit du domaine qui contient tous vos OneDrive; par exemple, `https://contoso-my.sharepoint.com`. Voici un exemple d’URL pour le site OneDrive d’un utilisateur: `https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft.com`.
