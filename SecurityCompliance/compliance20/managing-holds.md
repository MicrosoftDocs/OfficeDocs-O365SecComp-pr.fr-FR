---
title: Gérer les suspensions d’eDiscovery avancée (Preview)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 476ea80e61b5354c53368613e29a79c55a50276f
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29695180"
---
# <a name="manage-holds-in-advanced-ediscovery-preview"></a>Gérer les suspensions d’eDiscovery avancée (Preview)

Vous pouvez utiliser un cas eDiscovery avancées (Preview) pour créer des suspensions pour conserver le contenu qui peut-être s’appliquer à votre cas. À l’aide de la découverte électronique avancée (Preview) maintenez les fonctionnalités, vous pouvez placer les suspensions sur dépositaires et leurs sources de données. En outre, vous pouvez placer une suspension non garde sur les boîtes aux lettres et OneDrive pour les sites de l’entreprise. Vous pouvez également placer une suspension sur la boîte aux lettres de groupe, du site SharePoint et OneDrive pour le site de l’entreprise pour un groupe d’Office 365. De même, vous pouvez placer une suspension sur le site qui sont associés à Microsoft Teams et de boîte aux lettres. Lorsque vous placez les emplacements de contenu en attente, le contenu est conservé jusqu'à ce que vous libérez le dépositaire, supprimez un emplacement de données spécifique ou supprimez la totalité de la stratégie de blocage.

## <a name="manage-custodian-based-holds"></a>Gérer les suspensions basée sur dépositaire

Dans certains cas, vous pouvez avoir un ensemble de dépositaires de données que vous avez identifié et choisi de conserver. Dans découverte avancée (Preview), lorsque ces dépositaires sont mis en attente, l’utilisateur et leurs données sélectionnées sources sont automatiquement ajoutées à un dépositaire maintenez stratégie. 

Pour afficher la stratégie de blocage dépositaire :

1. Dans la **sécurité & centre de conformité**, cliquez sur **découverte > découverte avancée (Preview)** pour afficher la liste des incidents dans votre organisation.
   
2. Accédez à l’onglet **dépositaires** pour ajouter dépositaires dans votre cas. Pour savoir comment vous pouvez ajouter et mettre dépositaires en attente dans un cas eDiscovery avancées (Preview), consultez [Ajouter dépositaires à une découverte électronique avancée (Preview) cas](add-custodians-to-case.md). Si vous avez déjà ajouté dépositaires et leur mis en attente, passez à l’étape 3.
   
3. Accédez à l’onglet **contient** et sélectionnez la stratégie de dépositaire.
   
4. Dans la page mobile, vous pouvez voir les statistiques de la stratégie de blocage. Vous pouvez également effectuer des actions comme appliquer une requête à votre attente en fonction de dépositaire. Pour plus d’informations sur la création d’une requête de suspension et à l’aide de conditions, voir [conditions de recherche pour la recherche de contenu et les requêtes de mot clé](../keyword-queries-and-search-conditions.md).
 
## <a name="manage-non-custodial-holds"></a>Gérer les suspensions non garde

Lorsque vous créez une suspension, vous disposez des options suivantes pour définir la portée du contenu est conservé dans les emplacements de contenu spécifiés :

  - Vous créez une attente infinie où tout le contenu est mis en attente. Vous pouvez également créer une suspension basée sur une requête où seulement le contenu qui correspond à une requête de recherche est mis en attente.
  - Vous pouvez spécifier une plage de dates pour contenir uniquement le contenu qui a été envoyé, reçu ou créé dans cette plage de dates. Vous pouvez également maintenir tout le contenu indépendamment lorsqu’il a été envoyé, reçu ou créé.

Pour créer une suspension pour une affaire eDiscovery avancées (Preview) :

1. Dans la **sécurité & centre de conformité**, cliquez sur **découverte > découverte avancée (Preview)** pour afficher la liste des incidents dans votre organisation.
  
2. En regard de que vous souhaitez créer la suspension dans le cas, cliquez sur **Ouvrir** .
  
3. Dans la page d’accueil pour le cas, cliquez sur l’onglet **contient** .
  
4. Sous l’onglet **contient** , cliquez sur **créer**.
  
5. Dans la page **nom de votre suspension** , nommez la suspension. Le nom de la suspension doit être unique dans votre organisation.
 
6. (Facultatif) Dans la zone **Description** , ajoutez une description de la suspension.
  
7. Cliquez sur **Suivant**.
  
8. Choisissez les emplacements de contenu que vous souhaitez mettre en attente. Vous pouvez placer des boîtes aux lettres, les sites et les dossiers publics en attente.

   a **aux messages électroniques Exchange** - cliquez sur **Choisir des utilisateurs, des équipes ou des groupes** , puis cliquez sur **Choisir des utilisateurs, des équipes ou des groupes** pour spécifier les boîtes aux lettres à mettre en attente. Utilisez la zone Rechercher pour rechercher les boîtes aux lettres utilisateur et des groupes de distribution (pour émettre un blocage sur les boîtes aux lettres des membres du groupe) pour mettre en attente. Vous pouvez également placer une suspension sur la boîte aux lettres associée pour un groupe d’Office 365 ou un Team Microsoft. Sélectionnez l’utilisateur, le groupe, la case à cocher de l’équipe, cliquez sur **Choisir**, puis cliquez sur **terminé**.
 
    > [!NOTE]
    > Lorsque vous cliquez sur **Choisir les utilisateurs, groupes ou équipes** pour spécifier des boîtes aux lettres à mettre en attente, le sélecteur de boîte aux lettres qui s’affiche est vide. Il s’agit par défaut pour améliorer les performances. Pour ajouter des personnes à cette liste, tapez un nom (un minimum de 3 caractères) dans la zone de recherche.

    b. **Les Sites SharePoint** : cliquez sur **Choisir les sites** , puis cliquez sur **Choisir les sites** pour spécifier SharePoint et OneDrive pour les sites à mettre en attente. Tapez l’URL pour chaque site que vous souhaitez mettre en attente. Vous pouvez également ajouter l’URL du site SharePoint pour un groupe d’Office 365 ou un Team Microsoft. Cliquez sur **Choisir**, puis cliquez sur **terminé**.
    
     Consultez la section **Forum aux questions** pour obtenir des conseils sur le fait de placer des groupes Office 365 et Microsoft Teams en attente.

    > [!NOTE]
    > Dans ce cas rare nom d’une personne utilisateur principal (UPN) a été modifiée, l’URL de leur compte OneDrive système aussi être modifié pour incorporer le nouvel UPN. Dans ce cas, vous devrez modifier la suspension en ajoutant une nouvelle URL l’utilisateur de OneDrive et de supprimer l’ancien.

     c. **des dossiers publics Exchange** - déplacer le bouton bascule vers la position tous les placer tous les dossiers publics dans votre Exchange Online blocage de l’organisation. Notez que vous ne pouvez pas choisir des dossiers publics spécifiques à mettre en attente. Laissez le commutateur bascule défini sur **None** si vous ne souhaitez pas placer une suspension sur les dossiers publics.

9. Lorsque vous avez terminé d’ajouter des emplacements de contenu à la suspension, cliquez sur **suivant**.
  
10. Pour créer une suspension basée sur une requête avec les conditions, procédez comme suit. Dans le cas contraire, cliquez sur **suivant**.
    
    - Dans la zone sous **mots clés**, une requête de recherche dans la zone type d’afin qu’uniquement le contenu qui répond aux critères de recherche est mis en attente. Vous pouvez spécifier des mots clés, les propriétés de message ou des propriétés de document, tels que des noms de fichiers. Vous pouvez également utiliser des requêtes plus complexes qui utilisent un opérateur booléen, tels que AND, OR ou non. Si vous laissez la zone mot clé vide, puis tout le contenu situé dans les emplacements de contenu spécifiés est mis en attente.

    - Cliquez sur **Ajouter** les conditions pour ajouter une ou plusieurs conditions pour limiter la requête de recherche pour la suspension. Chaque condition ajoute une clause à la requête de recherche KQL qui est créée et exécuter lorsque vous créez la suspension. Par exemple, vous pouvez spécifier une plage de dates afin que le courrier électronique ou site de documents qui ont été créés dans la plage de date sont mis en attente. Une condition est logiquement connectée à la requête de mot clé (spécifiée dans la zone mots clés) par l’opérateur AND. Ce qui signifie que les éléments doivent satisfaire à la fois la requête de mot clé et la condition à être mis en attente.

     Pour plus d’informations sur la création d’une requête de recherche et à l’aide de conditions, voir [conditions de recherche pour la recherche de contenu et les requêtes de mot clé](https://docs.microsoft.com/en-us/office365/SecurityCompliance/keyword-queries-and-search-conditions).

12. Après avoir configuré basée sur une requête permanente, cliquez sur **suivant**.
 
13. Passez en revue vos paramètres, puis cliquez sur **créer cette suspension**.


## <a name="view-hold-statistics"></a>Afficher les statistiques d’attente

Après un certain temps, plus d’informations sur la mise en attente s’affiche dans le volet de détails, sous l’onglet **contient** de la suspension sélectionnée. Ces informations incluent le nombre de boîtes aux lettres maintenez sur les sites et des statistiques sur le contenu qui a été mis en attente, telles que le nombre et la taille des éléments mis en attente et de la dernière exécution de la suspension de calcul des statistiques. Contiennent statistiques vous aider à qu'identifier la quantité de contenu qui est associée à la découverte électronique est en cours.

Gardez les éléments suivants à l’esprit les statistiques d’attente :

- Le nombre total d’éléments en attente indique le nombre d’éléments à partir de toutes les sources de contenu qui sont mis en attente. Si vous avez créé une requête archive basée sur, cette statistique indique le nombre d’éléments qui correspondent à la requête.
  
- Le nombre d’éléments en attente inclut également les éléments non indexés trouvés dans les emplacements de contenu. Notez que si vous créez une suspension basée sur une requête, tous les éléments non indexés dans les emplacements de contenu sont mis en attente. Cela inclut les éléments non indexés qui ne correspondent pas aux critères de recherche d’une suspension basée sur une requête et non indexés qui peuvent être inclus en dehors d’une condition de plage de date. C’est différent de ce qui se produit lorsque vous exécutez une recherche de contenu, dans laquelle les éléments non indexés qui ne correspondent pas à la requête de recherche ou exclus par une condition de plage de date ne sont pas inclus dans les résultats de recherche. Pour plus d’informations sur les éléments non indexées, voir [partiellement indexé des éléments de la recherche de contenu dans Office 365](../partially-indexed-items-in-content-search.md). 

- Vous pouvez obtenir les dernières statistiques de suspension en cliquant sur les statistiques de mise à jour pour réexécuter une estimation de recherche qui calcule le nombre d’éléments en attente en cours.

- Si nécessaire, cliquez sur Actualiser dans la barre d’outils pour mettre à jour les statistiques d’attente dans le volet détails.

- Normal pour le nombre d’éléments de blocage pour augmenter au fil du temps, car les utilisateurs dont la boîte aux lettres ou site sont en attente sont généralement envoi ou la réception de nouveau message électronique et la création SharePoint nouvelle et OneDrive des documents d’entreprise.

- Si un site SharePoint ou un compte OneDrive est déplacé vers une région différente dans un environnement multi-localisés, les statistiques de ce site ne sont pas inclus dans les statistiques d’attente. Toutefois, le contenu du site sera toujours en attente. En outre, si un site est déplacé vers une autre zone de l’URL qui s’affiche dans la suspension ne système pas mis à jour. Vous devrez modifier la suspension et mettre à jour l’URL.

## <a name="frequently-asked-questions"></a>Questions fréquemment posées

- **Comment mapper un site Office 365 groupes ou Microsoft Teams supplémentaire à un dépositaire ? Maintenez l’est-il placer non garde sur Office 365 groupes et Microsoft Teams ?** Teams Microsoft reposent sur les groupes d’Office 365. Par conséquent, leur mise en attente dans un cas eDiscovery est très similaire. Gardez les éléments suivants à l’esprit lorsque le placement des groupes Office 365 et Microsoft Teams sur permanente.
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
    > Pour exécuter l’applet de commande Get-UnifiedGroup, vous devez être affecté le rôle destinataires en affichage seul dans Exchange Online ou être membre d’un groupe de rôles qui a affecté le rôle destinataires en affichage seul.

 - Lorsque la recherche de boîte aux lettres d’un utilisateur, groupe d’Office 365, ni Microsoft Team dont l’utilisateur est un membre de ne sont pas recherché. De même, lorsque vous placez un groupe d’Office 365 ou Microsoft Team maintenez, uniquement les boîtes aux lettres de groupe et le site de groupe sont mis en attente ; les boîtes aux lettres et OneDrive pour les sites d’entreprise des membres du groupe ne sont pas mis en attente, sauf si vous explicitement les ajoutez en tant que dépositaires ou bloquer leurs sources de données. Par conséquent, si vous la nécessité de placer un groupe dans Office 365 ou un Microsoft Team sur pendant un dépositaire spécifique, envisagez de mappage du site de groupe et des boîtes aux lettres de groupe pour le dépositaire (voir gestion des dépositaires d’eDiscovery avancée (Preview)). Si le groupe d’Office 365 ou Team Microsoft n’est pas imputable à un seul dépositaire, envisagez d’ajouter la source à non garde permanente. 
 
 - Pour obtenir une liste des membres d’un groupe dans Office 365 Team Microsoft, vous pouvez afficher les propriétés dans la page de groupes d’accueil > dans le centre d’administration d’Office 365. Vous pouvez également exécuter la commande suivante dans Exchange Online PowerShell :

   ``` 
   Get-UnifiedGroupLinks <group or team name> -LinkType Members | FL DisplayName,PrimarySmtpAddress
   ```

    > [!NOTE]
    > Pour exécuter l’applet de commande **Get-UnifiedGroupLinks** , vous devez être affecté le rôle destinataires en affichage seul dans Exchange Online ou être membre d’un groupe de rôles qui a affecté le rôle destinataires en affichage seul.

- Conversations du canal qui font partie d’un canal Teams Microsoft sont stockées dans la boîte aux lettres qui est associée à l’équipe. De même, les fichiers qui partagent des membres de l’équipe dans un canal sont stockés sur le site SharePoint de l’équipe. Par conséquent, vous devez placer la boîte aux lettres Microsoft Team maintenez le site SharePoint sur Conserver les conversations et les fichiers dans un canal.
  
- Vous pouvez également les conversations qui font partie de la liste de conversation dans Microsoft Teams sont stockées dans la boîte aux lettres de l’utilisateur qui participent à la conversation.  Fichiers utilisateur partage conversation sont stockés dans le site de l’entreprise de l’utilisateur qui partage le fichier OneDrive. Par conséquent, vous devez placer les boîtes aux lettres des utilisateurs individuels et OneDrive sur des sites de Commerce maintenez à conserver les conversations et les fichiers dans la liste de conversation. 
  
- Chaque canal Microsoft Team ou de l’équipe contient un Wiki de prise de notes et de collaboration. Le contenu Wiki est automatiquement enregistré dans un fichier au format .mht. Ce fichier est stocké dans la bibliothèque de documents équipes Wiki données sur le site SharePoint de l’équipe. Vous pouvez placer le contenu dans le Wiki en attente en plaçant le site SharePoint de l’équipe en attente.

  > [!NOTE]
  > La capacité à conserver le contenu Wiki pour un canal Microsoft Team ou de l’équipe (lorsque vous placez le site SharePoint de l’équipe en attente) a été publiée le 22 juin 2017. Si un site d’équipe maintenez, le Wiki contenu sera conservé commençant à cette date. Toutefois, si un site d’équipe est en attente et le contenu Wiki a été supprimé avant le 22 juin 2017, le contenu Wiki n’a été pas conservé.
