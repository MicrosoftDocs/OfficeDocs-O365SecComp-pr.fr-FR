---
title: Audit de partage pour trouver les ressources partagées avec des utilisateurs externes
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- BCS160
- MET150
ms.assetid: 50bbf89f-7870-4c2a-ae14-42635e0cfc01
description: 'Le partage est une activité essentielle dans SharePoint Online et OneDrive entreprise. Les administrateurs peuvent désormais utiliser l’audit de partage dans le journal d’audit Office 365 pour identifier les ressources partagées avec des utilisateurs en dehors de leur organisation. '
ms.openlocfilehash: 8996d404e2dbeaba01952c33a8699ca2f151ad5d
ms.sourcegitcommit: a8049055a48375bee7e6ed81fafcb27a7b2fcdff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/26/2019
ms.locfileid: "35911774"
---
# <a name="use-sharing-auditing-in-the-office-365-audit-log"></a>Audit de partage pour trouver les ressources partagées avec des utilisateurs externes

Le partage est une activité essentielle dans SharePoint Online et OneDrive entreprise, et est largement utilisée dans les organisations Office 365. Les administrateurs peuvent utiliser l’audit de partage dans le journal d’audit Office 365 pour déterminer le mode d’utilisation du partage dans leur organisation. 
  
## <a name="the-sharepoint-sharing-schema"></a>Schéma de partage SharePoint

Les événements de partage (sans inclure les événements liés à la stratégie de partage et les liens de partage) sont différents des événements liés aux fichiers et aux dossiers d’une manière principale: un utilisateur effectue une action qui a un impact sur un autre utilisateur. Par exemple, lorsqu’un utilisateur de ressource A accorde à l’utilisateur B l’accès à un fichier. Dans cet exemple, l’utilisateur A est ** l’utilisateur qui agit et l’utilisateur B est l' *utilisateur cible*. Dans le schéma de fichier SharePoint, l’action de l’utilisateur qui agit n’affecte que le fichier lui-même. Lorsque l’utilisateur A ouvre un fichier, la seule information nécessaire dans l’événement **FileAccessed** est l’utilisateur agissant. Pour résoudre cette différence, il existe un schéma distinct, appelé *schéma de partage SharePoint*, qui capture des informations supplémentaires sur les événements de partage. Cela garantit aux administrateurs une visibilité sur le partage d’une ressource et l’utilisateur avec lequel elle a été partagée. 
  
Le schéma de partage fournit deux champs supplémentaires dans un enregistrement d’audit lié aux événements de partage: 
  
- **TargetUserOrGroupType:** Indique si l’utilisateur ou le groupe cible est membre, invité, SharePointGroup, SecurityGroup ou partenaire.

- **TargetUserOrGroupName:** Stocke l’UPN ou le nom de l’utilisateur ou du groupe cible avec lequel une ressource a été partagée (utilisateur B dans l’exemple précédent). 

Ces deux champs, en plus des autres propriétés du schéma de journal d’audit Office 365, telles que User, Operation et date, peuvent indiquer l’histoire ** complète de quel utilisateur a partagé *quelle* ressource avec *qui* et *quand*. 
  
Il existe une autre propriété de schéma importante pour l’histoire du partage. Lorsque vous exportez les résultats de la recherche dans le journal d’audit, la colonne **AuditData** du fichier CSV exporté stocke des informations sur les événements de partage. Par exemple, lorsqu’un utilisateur partage un site avec un autre utilisateur, l’utilisateur cible est ajouté à un groupe SharePoint. La colonne **AuditData** capture ces informations pour fournir un contexte aux administrateurs. Reportez-vous à l' [étape 2](#step-2-use-the-powerquery-editor-to-format-the-exported-audit-log) pour obtenir des instructions sur la façon d’analyser les informations dans la colonne **AuditData** .

## <a name="sharepoint-sharing-events"></a>Événements de partage SharePoint

Le partage est défini par le fait qu’un utilisateur (l’utilisateur *agissant* ) souhaite partager une ressource avec un autre utilisateur (l’utilisateur *cible* ). Les enregistrements d’audit liés au partage d’une ressource avec un utilisateur externe (un utilisateur qui se trouve en dehors de votre organisation et qui ne dispose pas d’un compte invité dans l’Azure Active Directory de votre organisation) sont identifiés par les événements suivants, qui sont consignés dans Office 365 Journal d’audit:

- **SharingInvitationCreated:** Un utilisateur de votre organisation a essayé de partager une ressource (vraisemblablement un site) avec un utilisateur externe. Une invitation de partage externe est alors envoyée à l’utilisateur cible. Aucun accès à la ressource n’est accordé à ce stade.

- **SharingInvitationAccepted:** L’utilisateur externe a accepté l’invitation de partage envoyée par l’utilisateur agissant et a maintenant accès à la ressource.

- **AnonymousLinkCreated:** Un lien anonyme (également appelé lien «tout le monde») est créé pour une ressource. Étant donné qu’un lien anonyme peut être créé, puis copié, il est raisonnable de supposer que tout document ayant une liaison anonyme a été partagé avec un utilisateur cible.

- **AnonymousLinkUsed:** Comme son nom l’indique, cet événement est enregistré lorsqu’un lien anonyme est utilisé pour accéder à une ressource. 

- **SecureLinkCreated:** Un utilisateur a créé un lien «personnes spécifiques» pour partager une ressource avec une personne spécifique. Cet utilisateur cible peut être une personne extérieure à votre organisation.

- **AddedToSecureLink:** Un utilisateur a été ajouté à un lien personnes spécifiques. Cet utilisateur cible peut être une personne extérieure à votre organisation.

## <a name="sharing-auditing-work-flow"></a>Flux de travail d’audit de partage
  
Lorsqu’un utilisateur (l’utilisateur agissant) souhaite partager une ressource avec un autre utilisateur (l’utilisateur cible), SharePoint (ou OneDrive entreprise) vérifie d’abord si l’adresse de messagerie de l’utilisateur cible est déjà associée à un compte d’utilisateur dans l’annuaire de l’organisation. Si l’utilisateur cible se trouve dans le répertoire (et qu’il a un compte d’utilisateur invité correspondant), SharePoint effectue les opérations suivantes:
  
-  Affecte immédiatement les autorisations de l’utilisateur cible pour accéder à la ressource en ajoutant l’utilisateur cible au groupe SharePoint approprié et consigne un événement **AddedToGroup** . 
    
- Envoie une notification de partage à l’adresse de messagerie de l’utilisateur cible.
    
- Enregistre un événement **SharingSet** . Cet événement porte le nom convivial «partage de fichiers, de dossiers ou de sites» sous **activités de partage et de demande d’accès** dans le sélecteur d’activités de l’outil de recherche du journal d’audit. Voir la capture d’écran à l' [étape 1](#step-1-search-for-sharing-events-and-export-the-results-to-a-csv-file). 
    
Si un compte d’utilisateur pour l’utilisateur cible ne se trouve pas dans le répertoire, SharePoint effectue les opérations suivantes: 
    
   - Enregistre l’un des événements suivants, en fonction de la façon dont la ressource est partagée:
   
      - **AnonymousLinkCreated**
   
      - **SecureLinkCreated**
   
      - **AddedToSecureLink** 

      - **SharingInvitationCreated** (cet événement est enregistré uniquement lorsque la ressource partagée est un site)
    
   - Lorsque l’utilisateur cible accepte l’invitation de partage qui lui est envoyée (en cliquant sur le lien dans l’invitation), SharePoint consigne un événement **SharingInvitationAccepted** et affecte les autorisations de l’utilisateur cible pour accéder à la ressource. Si l’utilisateur cible reçoit un lien anonyme, l’événement **AnonymousLinkUsed** est journalisé une fois que l’utilisateur cible utilise le lien pour accéder à la ressource. Pour les liens sécurisés, un événement **FileAccessed** est enregistré lorsqu’un utilisateur externe utilise le lien pour accéder à la ressource.

Des informations supplémentaires sur l’utilisateur cible sont également consignées, telles que l’identité de l’utilisateur auquel l’invitation est adressée et l’utilisateur qui accepte réellement l’invitation. Dans certains cas, ces utilisateurs (ou adresses de messagerie) peuvent être différents. 

## <a name="how-to-identify-resources-shared-with-external-users"></a>Comment identifier les ressources partagées avec des utilisateurs externes

Une exigence commune pour les administrateurs est la création d’une liste de toutes les ressources qui ont été partagées avec des utilisateurs extérieurs à l’organisation. En utilisant le partage d’audit dans Office 365, les administrateurs peuvent générer cette liste. Voici comment procéder.
  
### <a name="step-1-search-for-sharing-events-and-export-the-results-to-a-csv-file"></a>Étape 1: Rechercher des événements de partage et exporter les résultats dans un fichier CSV

La première étape consiste à rechercher dans le journal d’audit Office 365 des événements de partage. Pour plus d’informations (y compris les autorisations requises) sur la recherche dans le journal d’audit, voir [Search the audit log dans le centre de sécurité & Compliance Center](search-the-audit-log-in-security-and-compliance.md).
  
1. Accédez à la page [https://protection.office.com](https://protection.office.com).
    
2. Connectez-vous à Office 365 à l'aide de votre compte scolaire ou professionnel.
    
3. Dans le volet gauche du centre de sécurité & conformité, cliquez ****  > sur Rechercher dans le**Journal d’audit**.
    
    La page **recherche du journal d’audit** s’affiche. 
    
4. Sous **activités**, cliquez sur **activités de partage et d’accès aux requêtes** pour rechercher des événements associés au partage. 
    
    ![Sous activités, sélectionnez activités de partage et d’accès aux demandes.](media/46bb25b7-1eb2-4adf-903a-cc9ab58639f9.png)
  
5.  Sélectionnez une date et une plage horaire pour rechercher les événements de partage qui se sont produits au cours de cette période. 
    
6. Cliquez sur **Rechercher** pour exécuter la recherche. 
    
7. Lorsque l’exécution de la recherche est terminée et que les résultats sont affichés, cliquez sur **Exporter les résultats** \> pour **Télécharger tous les résultats**.
    
    Une fois que vous avez sélectionné l’option Exporter, un message s’affiche en bas de la fenêtre qui vous invite à ouvrir ou à enregistrer le fichier CSV.
    
8. Cliquez sur **Enregistrer** \> **Enregistrer sous** et enregistrez le fichier CSV dans un dossier sur votre ordinateur local. 

### <a name="step-2-use-the-powerquery-editor-to-format-the-exported-audit-log"></a>Étape 2: utiliser l’éditeur PowerQuery pour mettre en forme le journal d’audit exporté

L’étape suivante consiste à utiliser la fonctionnalité transformation JSON de l’éditeur Power Query dans Excel pour fractionner chaque propriété de la colonne **AuditData** (qui se compose d’un objet JSON multi-propriété) dans sa propre colonne. Cela vous permet de filtrer les colonnes pour afficher les enregistrements liés au partage

Pour obtenir des instructions détaillées, reportez-vous à la section «étape 2: formater le journal d’audit exporté à l’aide de l’éditeur de requête Power» dans la rubrique relative à l' [exportation, la configuration et l’affichage des enregistrements du journal d’audit](export-view-audit-log-records.md#step-2-format-the-exported-audit-log-using-the-power-query-editor).

### <a name="step-3-filter-the-csv-file-for-resources-shared-with-external-users"></a>Étape 3: filtrage du fichier CSV pour les ressources partagées avec des utilisateurs externes

L’étape suivante consiste à filtrer le fichier CSV pour les différents événements liés au partage qui ont été décrits précédemment dans la section [événements de partage SharePoint](#sharepoint-sharing-events) . Vous pouvez également filtrer la colonne **TargetUserOrGroupType** pour afficher tous les enregistrements pour lesquels la valeur de cette propriété est **Guest**. 

Une fois que vous avez suivi les instructions de l’étape précédente pour préparer le fichier CSV à l’aide de l’éditeur PowerQuery, procédez comme suit:
    
1. Ouvrez le fichier Excel que vous avez créé à l’étape 2. 

2. Sous l’onglet **Accueil** , cliquez sur **Trier & filtrer**, puis sur **Filtrer**.
    
3. Dans la liste déroulante **trier & filtre** de la colonne **opérations** , effacez toutes les sélections, puis sélectionnez un ou plusieurs des événements associés au partage, puis cliquez sur **OK**.
 
   - **SharingInvitationCreated**
   
   - **AnonymousLinkCreated**
   
   - **SecureLinkCreated**
   
   - **AddedToSecureLink** 
    
    Excel affiche les lignes pour les événements que vous avez sélectionnés.
    
4. Accédez à la colonne nommée **TargetUserOrGroupType** et sélectionnez-la. 
    
5. Dans la liste déroulante **trier & filtre** , effacez toutes les sélections, sélectionnez **TargetUserOrGroupType: invité**, puis cliquez sur **OK**.
    
    À présent, Excel affiche les lignes pour les événements de partage et l’endroit où l’utilisateur cible se trouve à l’extérieur de votre organisation, car les utilisateurs externes sont identifiés par la valeur **TargetUserOrGroupType: Guest**. 
  
> [!TIP]
> Pour les enregistrements d’audit affichés, la colonne **ObjectID** identifie la ressource qui a été partagée avec l’utilisateur cible; par exemple `ObjectId:https:\/\/contoso-my.sharepoint.com\/personal\/sarad_contoso_com\/Documents\/Southwater Proposal.docx`.
