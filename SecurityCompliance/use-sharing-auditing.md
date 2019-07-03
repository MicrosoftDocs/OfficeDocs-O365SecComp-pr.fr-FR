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
description: 'Le partage est une activité essentielle dans SharePoint Online et OneDrive entreprise. Les administrateurs peuvent désormais utiliser l’audit de partage dans le journal d’audit Office 365 pour déterminer le mode d’utilisation du partage dans leur organisation. '
ms.openlocfilehash: e2865d35e988d8c0e42a6c51f78507db8b170d4c
ms.sourcegitcommit: b262d40f6daf06be26e7586f37b736e09f8a4511
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/02/2019
ms.locfileid: "35435237"
---
# <a name="use-sharing-auditing-in-the-office-365-audit-log"></a>Audit de partage pour trouver les ressources partagées avec des utilisateurs externes

Le partage est une activité essentielle dans SharePoint Online et OneDrive entreprise, et est largement utilisée dans les organisations Office 365. Les administrateurs peuvent désormais utiliser l’audit de partage dans le journal d’audit Office 365 pour déterminer le mode d’utilisation du partage dans leur organisation. 
  
## <a name="the-sharepoint-sharing-schema"></a>Schéma de partage SharePoint

Les événements de partage (à l’exception des événements de liens de partage et de stratégie) sont différents des événements liés aux fichiers et aux dossiers d’une manière principale: un utilisateur effectue une action qui a un certain effet sur un autre utilisateur. Par exemple, l’utilisateur A accorde à l’utilisateur B l’accès à un fichier. Dans cet exemple, l’utilisateur A est ** l’utilisateur qui agit et l’utilisateur B est l' *utilisateur cible*. Dans le schéma de fichier SharePoint, l’action de l’utilisateur qui agit n’affecte que le fichier lui-même. Lorsque l’utilisateur A ouvre un fichier, la seule information nécessaire dans l’événement **FileAccessed** est l’utilisateur agissant. Pour résoudre cette différence, il existe un schéma distinct, appelé *schéma de partage SharePoint*, qui capture des informations supplémentaires sur les événements de partage. Cela garantit aux administrateurs un aperçu plus détaillé des personnes qui ont partagé une ressource et de l’utilisateur avec lequel elle a été partagée. 
  
Le schéma de partage fournit deux champs supplémentaires dans le journal d’audit concernant les événements de partage: 
  
- **TargetUserOrGroupName** : stocke l’UPN ou le nom de l’utilisateur ou du groupe cible avec lequel une ressource a été partagée (utilisateur B dans l’exemple précédent). 
    
- **TargetUserOrGroupType** : indique si l’utilisateur ou le groupe cible est un membre, un invité, un groupe ou un partenaire. 
    
Ces deux champs, en plus des autres propriétés du schéma de journal d’audit Office 365, telles que User, Operation et date, peuvent indiquer l’histoire ** complète de quel utilisateur a partagé *quelle* ressource avec *qui* et *quand*. 
  
Il existe une autre propriété de schéma importante pour l’histoire du partage. La propriété **EventData** stocke des informations supplémentaires sur les événements de partage. Par exemple, lorsqu’un utilisateur partage un site avec un autre utilisateur, l’utilisateur cible est ajouté à un groupe SharePoint. La propriété **EventData** capture ces informations supplémentaires afin de fournir un contexte aux administrateurs. 

## <a name="the-sharepoint-sharing-model-and-sharing-events"></a>Modèle de partage SharePoint et événements de partage

Le partage est défini par trois événements distincts: **SharingSet**, **SharingInvitationCreated**et **SharingInvitaitonAccepted**. Voici le flux de travail concernant la façon dont les événements de partage sont consignés dans le journal d’audit Office 365. 
  
![Organigramme illustrant le fonctionnement du partage d’audit](media/d83dd40f-919b-484f-bfd6-5dc8de31bff6.png)
  
Lorsqu’un utilisateur (l’utilisateur agissant) souhaite partager une ressource avec un autre utilisateur (l’utilisateur cible), SharePoint (ou OneDrive entreprise) vérifie d’abord si l’adresse de messagerie de l’utilisateur cible est déjà associée à un compte d’utilisateur dans l’annuaire de l’organisation. Si l’utilisateur cible se trouve dans l’annuaire de l’organisation, SharePoint effectue les opérations suivantes:
  
-  Affecte immédiatement les autorisations de l’utilisateur cible pour accéder à la ressource. 
    
- Envoie une notification de partage à l’adresse de messagerie de l’utilisateur cible.
    
- Enregistre un événement **SharingSet** . 
    
 Si un compte d’utilisateur pour l’utilisateur cible ne se trouve pas dans l’annuaire de l’organisation, SharePoint effectue les opérations suivantes: 
  
- Crée une invitation de partage et l’envoie à l’adresse de messagerie de l’utilisateur cible.
    
- Enregistre un événement **SharingInvitationCreated** . 
    
    > [!NOTE]
    > L’événement **SharingInvitationCreated** est le plus souvent associé au partage externe ou invité lorsque l’utilisateur cible n’a pas accès à la ressource qui a été partagée. 
  
Lorsque l’utilisateur cible accepte l’invitation de partage qui lui est envoyée (en cliquant sur le lien dans l’invitation), SharePoint consigne un événement **SharingInvitationAccepted** et affecte les autorisations de l’utilisateur cible pour accéder à la ressource. Des informations supplémentaires sur l’utilisateur cible sont également consignées, telles que l’identité de l’utilisateur auquel l’invitation a été envoyée et l’utilisateur qui a réellement accepté l’invitation. Dans certains cas, ces utilisateurs (ou adresses de messagerie) peuvent être différents. 
  

  
## <a name="how-to-identify-resources-shared-with-external-users"></a>Comment identifier les ressources partagées avec des utilisateurs externes

Une exigence commune pour les administrateurs est la création d’une liste de toutes les ressources qui ont été partagées avec des utilisateurs extérieurs à l’organisation. À l’aide de l’audit de partage dans Office 365, les administrateurs peuvent désormais générer cette liste. Voici comment procéder.
  
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

### <a name="step-2-filter-the-csv-file-for-resources-shared-with-external-users"></a>Étape 2: filtrage du fichier CSV pour les ressources partagées avec des utilisateurs externes

L’étape suivante consiste à filtrer le fichier CSV pour les événements **SharingSet** et **SharingInvitationCreated** , et à afficher les événements pour lesquels la propriété **TargetUserOrGroupType** est **Guest**. Pour ce faire, utilisez l’outil Éditeur de la requête Power dans Excel. Pour obtenir des instructions pas à pas, reportez-vous à la rubrique [Exporter, configurer et afficher les enregistrements du journal d’audit](export-view-audit-log-records.md). 

Une fois que vous avez suivi les instructions de la rubrique précédente pour préparer le fichier CSV, procédez comme suit:
    
1. Ouvrez le fichier CSV que vous avez préparé avec l’éditeur de Power Query. 

2. Sous l’onglet **Accueil** , cliquez sur **Trier & filtrer**, puis sur **Filtrer**.
    
3. Dans la liste déroulante **trier & filtre** de la colonne **opérations** , effacez toutes les sélections, sélectionnez **SharingSet** et **SharingInvitationCreated**, puis cliquez sur **OK**.
    
    Excel affiche les lignes pour les événements **SharingSet** et **SharingInvitationCreated** . 
    
4. Accédez à la colonne nommée **TargetUserOrGroupType** et sélectionnez-la. 
    
5. Dans la liste déroulante **trier & filtre** , effacez toutes les sélections, sélectionnez **TargetUserOrGroupType: invité**, puis cliquez sur **OK**.
    
    À présent, Excel affiche les lignes pour les événements **SharingInvitationCreated** et **SharingSet** et l’emplacement de l’utilisateur cible à l’extérieur de votre organisation, car les utilisateurs externes sont identifiés par la valeur **TargetUserOrGroupType: Guest**. 
    
Le tableau suivant présente tous les utilisateurs de l’organisation qui ont partagé des ressources avec un utilisateur invité dans une plage de dates spécifiée.
  
![Partage d’événements dans le journal d’audit Office 365](media/0e0ecbe3-c794-4ca6-a2ca-63478fb3bb34.png)
  
Bien qu’elle ne soit pas incluse dans le tableau précédent, la propriété **ObjectID** identifie la ressource qui a été partagée avec l’utilisateur cible; par exemple `ObjectId:https:\/\/contoso-my.sharepoint.com\/personal\/sarad_contoso_com\/Documents\/Southwater Proposal.docx`.
  
> [!TIP]
> Si vous souhaitez identifier à quel moment un utilisateur invité a reçu des autorisations d’accès à une ressource (par opposition aux ressources partagées avec celles-ci), répétez les étapes 2, 3 et 4, et filtrez sur les **SharingInvitationAccepted** et **SharingSet** événements à l’étape 5. 
