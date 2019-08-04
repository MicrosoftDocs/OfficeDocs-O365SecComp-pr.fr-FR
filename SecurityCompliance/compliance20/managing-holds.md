---
title: Gérer les suspensions dans Advanced eDiscovery
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 4e46eba010cd51ab0722fb43196230ba44f4e9a4
ms.sourcegitcommit: 7c1cb9e8adb1c3e9c667f4cf02ca3cec3ec1e171
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/18/2019
ms.locfileid: "35791990"
---
# <a name="manage-holds-in-advanced-ediscovery"></a>Gérer les suspensions dans Advanced eDiscovery

Vous pouvez utiliser un cas avancé de découverte électronique pour créer des suspensions afin de conserver le contenu susceptible de concerner votre cas. À l’aide des fonctionnalités de mise en attente avancée de eDiscovery, vous pouvez placer des suspensions sur des dépositaires et leurs sources de données. En outre, vous pouvez placer un blocage non privative de direction sur les boîtes aux lettres et les sites OneDrive entreprise. Vous pouvez également placer une suspension sur la boîte aux lettres de groupe, le site SharePoint et le site OneDrive entreprise pour un groupe Office 365. De même, vous pouvez placer une conservation sur la boîte aux lettres et le site associés à Microsoft Teams. Lorsque vous placez des emplacements de contenu en conservation, le contenu est conservé jusqu’à ce que vous libériez le dépositaire, que vous supprimiez un emplacement de données spécifique ou que vous supprimiez entièrement la stratégie de blocage.

## <a name="manage-custodian-based-holds"></a>Gérer les conservations basées sur des dépositaires

Dans certains cas, il se peut que vous ayez identifié un ensemble de dépositaires de données que vous avez identifiés et que vous choisissiez de conserver. Dans Advanced eDiscovery, lorsque ces dépositaires sont mis en attente, l’utilisateur et les sources de données sélectionnées sont automatiquement ajoutés à une stratégie de blocage des dépositaires. 

Pour afficher la stratégie de blocage des dépositaires:

1. Dans le **Centre de sécurité & conformité**, cliquez sur **eDiscovery > Advanced eDiscovery** pour afficher la liste des incidents de votre organisation.
   
2. Accédez à l' **** onglet dépositaires pour ajouter des dépositaires dans votre cas. Pour savoir comment ajouter et placer des dépositaires en attente dans un cas avancé eDiscovery, voir [Add dépositaires to a Advanced eDiscovery case](add-custodians-to-case.md). Si vous avez déjà ajouté des dépositaires et les avez placés en conservation, passez à l’étape 3.
   
3. Accédez à l' **** onglet suspensions et sélectionnez la stratégie de dépositaire.
   
4. Dans la page de menu volant, vous pouvez voir les statistiques de conservation pour la stratégie. Vous pouvez également effectuer des actions comme appliquer une requête à votre conservation basée sur un dépositaire. Pour plus d’informations sur la création d’une requête de suspension et l’utilisation de conditions, consultez la rubrique [requêtes de mots clés et conditions de recherche pour la recherche de contenu](../keyword-queries-and-search-conditions.md).
 
## <a name="manage-non-custodial-holds"></a>Gérer les conservations non privatives de cœur

Lorsque vous créez une suspension, vous disposez des options suivantes pour définir l’étendue du contenu qui se trouve dans les emplacements de contenu spécifiés:

  - Vous créez un blocage infini où tout le contenu est placé en conservation. Vous pouvez également créer une conservation basée sur une requête où seul le contenu qui correspond à une requête de recherche est mis en attente.
  - Vous pouvez spécifier une plage de dates qui doit contenir uniquement le contenu qui a été envoyé, reçu ou créé au sein de cette plage de dates. Vous pouvez également conserver tout le contenu, quel que soit son moment d’envoi, de réception ou de création.

Pour créer une suspension pour un cas de découverte électronique avancée:

1. Dans le **Centre de sécurité & conformité**, cliquez sur **eDiscovery > Advanced eDiscovery** pour afficher la liste des incidents de votre organisation.
  
2. Cliquez sur **ouvrir** en regard du cas dans lequel vous souhaitez créer les suspensions.
  
3. À partir de la page d’accueil de l’incident **** , cliquez sur l’onglet suspensions.
  
4. Dans l' **** onglet suspensions, cliquez sur **créer**.
  
5. Sur la page **nommer votre suspension** , donnez un nom. Le nom de la conservation doit être unique dans toute votre organisation.
 
6. Module Dans la zone **Description** , ajoutez une description de la conservation.
  
7. Cliquez sur **Suivant**.
  
8. Choisissez les emplacements de contenu que vous souhaitez mettre en attente. Vous pouvez placer les boîtes aux lettres, les sites et les dossiers publics en conservation.

   a. **E-mail Exchange** -cliquez sur **choisir les utilisateurs, les groupes ou les équipes** , puis cliquez à nouveau sur **choisir les utilisateurs, les groupes ou les équipes** pour spécifier les boîtes aux lettres à mettre en attente. Utilisez la zone de recherche pour rechercher des boîtes aux lettres utilisateur et des groupes de distribution (pour mettre en attente les boîtes aux lettres des membres du groupe) à mettre en attente. Vous pouvez également placer une conservation sur la boîte aux lettres associée pour un groupe Office 365 ou une équipe Microsoft. Activez la case à cocher utilisateur, groupe, équipe, cliquez sur **choisir**, puis sur **Terminer**.
 
    > [!NOTE]
    > Lorsque vous cliquez sur **choisir les utilisateurs, les groupes ou les équipes** pour spécifier les boîtes aux lettres à mettre en attente, le sélecteur de boîtes aux lettres affiché est vide. Il s’agit d’une conception qui améliore les performances. Pour ajouter des personnes à cette liste, tapez un nom (un minimum de 3 caractères) dans la zone de recherche.

    b. **Sites SharePoint** : cliquez sur **choisir des sites** , puis cliquez à nouveau sur choisir les **sites** pour spécifier les sites SharePoint et OneDrive entreprise à mettre en attente. Saisissez l’URL de chaque site à placer en conservation. Vous pouvez également ajouter l’URL du site SharePoint pour un groupe Office 365 ou une équipe Microsoft. Cliquez sur **choisir**, puis sur **Terminer**.
    
     Consultez la section **Forum aux questions** pour obtenir des conseils sur la mise en attente des groupes Office 365 et de Microsoft Teams.

    > [!NOTE]
    > Dans le cas rare où le nom d’utilisateur principal (UPN) d’une personne a été modifié, l’URL de son compte OneDrive sera également modifiée de façon à intégrer le nouvel UPN. Dans ce cas, vous devez modifier la conservation en ajoutant la nouvelle URL OneDrive de l’utilisateur et en supprimant l’ancienne.

     c. **Dossiers publics Exchange** : déplacez le bouton bascule vers la position tout pour mettre en attente tous les dossiers publics de votre organisation Exchange Online. Notez que vous ne pouvez pas choisir des dossiers publics spécifiques à mettre en attente. Laissez le commutateur Toggle défini sur **None** si vous ne souhaitez pas mettre de conservation sur les dossiers publics.

9. Lorsque vous avez terminé d’ajouter des emplacements de contenu au blocage, cliquez sur **suivant**.
  
10. Pour créer une conservation basée sur une requête avec des conditions, procédez comme suit. Dans le cas contraire, cliquez sur **suivant**.
    
    - Dans la zone sous **Mots clés**, tapez une requête de recherche dans le champ de sorte que seul le contenu qui répond aux critères de recherche est placé en conservation. Vous pouvez spécifier des mots clés, des propriétés de message ou des propriétés de document, telles que des noms de fichiers. Vous pouvez également utiliser des requêtes plus complexes qui utilisent un opérateur booléen, comme AND, OR ou NOT. Si vous laissez la zone mot clé vide, tout le contenu situé dans les emplacements de contenu spécifiés sera placé en conservation.

    - Cliquez sur **Ajouter** des conditions pour ajouter une ou plusieurs conditions afin de limiter la requête de recherche pour la suspension. Chaque condition ajoute une clause à la requête de recherche KQL créée et exécutée lors de la création de la suspension. Par exemple, vous pouvez spécifier une plage de dates pour que les documents de courrier ou de site créés dans la plage de dates soient suspendus. Une condition est connectée à la requête de mot-clé (spécifiée dans la zone de mot-clé) sur le plan logique par l’opérateur AND. Cela signifie que les éléments doivent satisfaire à la fois la requête de mot clé et la condition à mettre en attente.

     Pour plus d’informations sur la création d’une requête de recherche et l’utilisation de conditions, consultez la rubrique [requêtes de mots clés et conditions de recherche pour la recherche de contenu](https://docs.microsoft.com/en-us/office365/SecurityCompliance/keyword-queries-and-search-conditions).

12. Après avoir configuré une conservation basée sur une requête, cliquez sur **suivant**.
 
13. Vérifiez vos paramètres, puis cliquez sur **créer cette suspension**.


## <a name="view-hold-statistics"></a>Afficher les statistiques de conservation

Après un certain temps, les informations relatives à la nouvelle conservation s’affichent dans le **** volet d’informations de l’onglet suspensions de la suspension sélectionnée. Ces informations incluent le nombre de boîtes aux lettres et de sites en conservation, ainsi que des statistiques sur le contenu qui a été placé en conservation, telles que le nombre total et la taille des éléments mis en attente et la dernière fois que les statistiques de conservation ont été calculées. Ces statistiques de suspension vous aident à identifier la proportion de contenu liée au cas eDiscovery.

Gardez les points suivants à l’esprit concernant les statistiques de conservation:

- Le nombre total d’éléments en attente indique le nombre d’éléments de toutes les sources de contenu qui sont placées en conservation. Si vous avez créé une conservation basée sur une requête, cette statistique indique le nombre d’éléments qui correspondent à la requête.
  
- Le nombre d’éléments en attente inclut également les éléments non indexés trouvés dans les emplacements de contenu. Notez que si vous créez une conservation basée sur une requête, tous les éléments non indexés des emplacements de contenu sont placés en conservation. Cela inclut les éléments non indexés qui ne correspondent pas aux critères de recherche d’une conservation basée sur une requête et les éléments non indexés qui peuvent se situer en dehors d’une condition de plage de dates. Cette opération est différente de ce qui se passe lorsque vous exécutez une recherche de contenu, dans laquelle les éléments non indexés qui ne correspondent pas à la requête de recherche ou qui sont exclus par une condition de plage de dates ne sont pas inclus dans les résultats de la recherche. Pour plus d’informations sur les éléments non indexés, voir [éléments partiellement indexés dans la recherche de contenu dans Office 365](../partially-indexed-items-in-content-search.md). 

- Vous pouvez obtenir les dernières statistiques de conservation en cliquant sur mettre à jour les statistiques pour réexécuter une estimation de recherche qui calcule le nombre actuel d’éléments en attente.

- Si nécessaire, cliquez sur Actualiser dans la barre d’outils pour mettre à jour les statistiques de conservation dans le volet d’informations.

- Il est normal que le nombre d’éléments bloqués augmente au fil du temps, car les utilisateurs dont la boîte aux lettres ou le site est en attente envoient généralement de nouveaux messages électroniques et créent des documents SharePoint et OneDrive entreprise.

- Si un site SharePoint ou un compte OneDrive est déplacé vers une autre région dans un environnement multi-géo, les statistiques de ce site ne sont pas incluses dans les statistiques de conservation. Toutefois, le contenu du site reste bloqué. En outre, si un site est déplacé vers une autre région, l’URL affichée dans la conservation n’est pas mise à jour. Vous devrez modifier la conservation et mettre à jour l’URL.

## <a name="frequently-asked-questions"></a>Questions fréquemment posées

- **Comment mapper un site Office 365 ou Microsoft teams supplémentaire à un dépositaire? Et qu’en est-il de la mise en place d’une absence privative de rôle sur les groupes Office 365 et Microsoft teams?** Microsoft teams est basé sur les groupes Office 365. Par conséquent, leur mise en attente dans un cas eDiscovery est très similaire. Gardez les points suivants à l’esprit lorsque vous importez des groupes Office 365 et Microsoft teams en conservation.
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
    > Pour exécuter la cmdlet Get-UnifiedGroup, vous devez disposer du rôle destinataires en affichage seul dans Exchange Online ou être membre d’un groupe de rôles auquel est affecté le rôle destinataires en affichage seul.

 - Lors de la recherche dans la boîte aux lettres d’un utilisateur, le groupe Office 365 ou l’équipe Microsoft dont l’utilisateur est membre ne feront pas l’objet d’une recherche. De même, lorsque vous placez un groupe Office 365 ou un blocage d’équipe Microsoft, seule la boîte aux lettres de groupe et le site de groupe sont mis en attente; les boîtes aux lettres et les sites OneDrive entreprise des membres du groupe ne sont pas mis en attente, sauf si vous les ajoutez explicitement en tant que dépositaires ou que leurs sources de données ne sont pas conservées. Par conséquent, si vous devez placer un groupe Office 365 ou Microsoft Team en conservation pour un dépositaire spécifique, envisagez de mapper le site de groupe et la boîte aux lettres de groupe au dépositaire (voir Managing dépositaires in Advanced eDiscovery). Si le groupe Office 365 ou l’équipe Microsoft n’est pas attribuable à un seul dépositaire, envisagez d’ajouter la source à une conservation non privatives de personnes. 
 
 - Pour obtenir la liste des membres d’un groupe ou d’une équipe Microsoft Office 365, vous pouvez afficher les propriétés de la page groupes d' > d’accueil dans le centre d’administration Microsoft 365. Vous pouvez également exécuter la commande suivante dans Exchange Online PowerShell:

   ``` 
   Get-UnifiedGroupLinks <group or team name> -LinkType Members | FL DisplayName,PrimarySmtpAddress
   ```

    > [!NOTE]
    > Pour exécuter la cmdlet **Get-UnifiedGroupLinks** , vous devez disposer du rôle destinataires en affichage seul dans Exchange Online ou être membre d’un groupe de rôles auquel est affecté le rôle destinataires en affichage seul.

- Les conversations de canal qui font partie d’un canal Microsoft teams sont stockées dans la boîte aux lettres associée à l’équipe. De même, les fichiers que les membres de l’équipe partagent dans un canal sont stockés sur le site SharePoint de l’équipe. Par conséquent, vous devez placer la boîte aux lettres d’équipe Microsoft et le site SharePoint en conservation pour conserver les conversations et les fichiers dans un canal.
  
- En guise d’alternative, les conversations qui font partie de la liste de conversation de Microsoft teams sont stockées dans la boîte aux lettres de l’utilisateur qui participe à la conversation.  Les fichiers partagés par un utilisateur dans les conversations de conversation sont stockés dans le site OneDrive entreprise de l’utilisateur qui partage le fichier. Par conséquent, vous devez placer les boîtes aux lettres des utilisateurs individuels et les sites OneDrive entreprise en conservation pour conserver les conversations et les fichiers dans la liste des conversations. 
  
- Chaque canal d’équipe ou d’équipe Microsoft contient un wiki pour la prise de notes et la collaboration. Le contenu wiki est automatiquement enregistré dans un fichier au format. mht. Ce fichier est stocké dans la bibliothèque de documents de données wiki teams sur le site SharePoint de l’équipe. Vous pouvez placer le contenu du wiki en conservation en mettant le site SharePoint de l’équipe en conservation.

  > [!NOTE]
  > La capacité à conserver du contenu wiki pour une équipe Microsoft ou un canal d’équipe (lorsque vous placez le blocage du site SharePoint de l’équipe) a été publiée le 22 juin 2017. Si un site d’équipe est en conservation, le contenu wiki est conservé à partir de cette date. Toutefois, si un site d’équipe est en conservation et que le contenu wiki a été supprimé avant le 22 juin 2017, le contenu wiki n’a pas été conservé.
