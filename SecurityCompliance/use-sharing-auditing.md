---
title: Audit de partage pour trouver les ressources partagées avec des utilisateurs externes
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 2/13/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- BCS160
- MET150
ms.assetid: 50bbf89f-7870-4c2a-ae14-42635e0cfc01
description: "Le partage est une activité essentielle dans SharePoint Online et OneDrive entreprise. Les administrateurs peuvent désormais utiliser l'audit de partage dans le journal d'audit Office 365 pour déterminer le mode d'utilisation du partage dans leur organisation. "
ms.openlocfilehash: 919592bff43379b552b83258c7b22b7eddb14e7a
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219884"
---
# <a name="use-sharing-auditing-in-the-office-365-audit-log"></a>Audit de partage pour trouver les ressources partagées avec des utilisateurs externes

Le partage est une activité essentielle dans SharePoint Online et OneDrive entreprise, et est largement utilisée dans les organisations Office 365. Les administrateurs peuvent désormais utiliser l'audit de partage dans le journal d'audit Office 365 pour déterminer le mode d'utilisation du partage dans leur organisation. 
  
## <a name="the-sharepoint-sharing-schema"></a>Schéma de partage SharePoint

Les événements de partage (à l'exception des événements de liens de partage et de stratégie) sont différents des événements liés aux fichiers et aux dossiers d'une manière principale: un utilisateur effectue une action qui a un certain effet sur un autre utilisateur. Par exemple, l'utilisateur A accorde à l'utilisateur B l'accès à un fichier. Dans cet exemple, l'utilisateur A est ** l'utilisateur qui agit et l'utilisateur B est l' *utilisateur cible*. Dans le schéma de fichier SharePoint, l'action de l'utilisateur qui agit n'affecte que le fichier lui-même. Lorsque l'utilisateur A ouvre un fichier, la seule information nécessaire dans l'événement **FileAccessed** est l'utilisateur agissant. Pour résoudre cette différence, il existe un schéma distinct, appelé *schéma de partage SharePoint*, qui capture des informations supplémentaires sur les événements de partage. Cela garantit aux administrateurs un aperçu plus détaillé des personnes qui ont partagé une ressource et de l'utilisateur avec lequel elle a été partagée. 
  
Le schéma de partage fournit deux champs supplémentaires dans le journal d'audit concernant les événements de partage: 
  
- **TargetUserOrGroupName** : stocke l'UPN ou le nom de l'utilisateur ou du groupe cible avec lequel une ressource a été partagée (utilisateur B dans l'exemple précédent). 
    
- **TargetUserOrGroupType** : indique si l'utilisateur ou le groupe cible est un membre, un invité, un groupe ou un partenaire. 
    
Ces deux champs, en plus des autres propriétés du schéma de journal d'audit Office 365, telles que User, Operation et date, peuvent indiquer l'histoire ** complète de quel utilisateur a partagé *quelle* ressource avec *qui* et *quand*. 
  
Il existe une autre propriété de schéma importante pour l'histoire du partage. La propriété **EventData** stocke des informations supplémentaires sur les événements de partage. Par exemple, lorsqu'un utilisateur partage un site avec un autre utilisateur, l'utilisateur cible est ajouté à un groupe SharePoint. La propriété **EventData** capture ces informations supplémentaires afin de fournir un contexte aux administrateurs. 

## <a name="the-sharepoint-sharing-model-and-sharing-events"></a>Modèle de partage SharePoint et événements de partage

Le partage est en fait défini par trois événements distincts: **SharingSet**, **SharingInvitationCreated**et **SharingInvitaitonAccepted**. Voici le flux de travail concernant la façon dont les événements de partage sont consignés dans le journal d'audit Office 365. 
  
![Organigramme illustrant le fonctionnement du partage d'audit](media/d83dd40f-919b-484f-bfd6-5dc8de31bff6.png)
  
Lorsqu'un utilisateur (l'utilisateur agissant) souhaite partager une ressource avec un autre utilisateur (l'utilisateur cible), SharePoint (ou OneDrive entreprise) vérifie d'abord si l'adresse de messagerie de l'utilisateur cible est déjà associée à un compte d'utilisateur dans l'annuaire de l'organisation. Si l'utilisateur cible se trouve dans l'annuaire de l'organisation, SharePoint effectue les opérations suivantes:
  
-  Affecte immédiatement les autorisations de l'utilisateur cible pour accéder à la ressource. 
    
- Envoie une notification de partage à l'adresse de messagerie de l'utilisateur cible.
    
- Enregistre un événement **SharingSet** . 
    
 Si un compte d'utilisateur pour l'utilisateur cible ne se trouve pas dans l'annuaire de l'organisation, SharePoint effectue les opérations suivantes: 
  
- Crée une invitation de partage et l'envoie à l'adresse de messagerie de l'utilisateur cible.
    
- Enregistre un événement **SharingInvitationCreated** . 
    
    > [!NOTE]
    > L'événement **SharingInvitationCreated** est le plus souvent associé au partage externe ou invité lorsque l'utilisateur cible n'a pas accès à la ressource qui a été partagée. 
  
Lorsque l'utilisateur cible accepte l'invitation de partage qui lui est envoyée (en cliquant sur le lien dans l'invitation), SharePoint consigne un événement **SharingInvitationAccepted** et affecte les autorisations de l'utilisateur cible pour accéder à la ressource. Des informations supplémentaires sur l'utilisateur cible sont également consignées, telles que l'identité de l'utilisateur auquel l'invitation a été envoyée et l'utilisateur qui a réellement accepté l'invitation. Dans certains cas, ces utilisateurs (ou adresses de messagerie) peuvent être différents. 
  

  
## <a name="how-to-identify-resources-shared-with-external-users"></a>Comment identifier les ressources partagées avec des utilisateurs externes

Une exigence commune pour les administrateurs est la création d'une liste de toutes les ressources qui ont été partagées avec des utilisateurs extérieurs à l'organisation. À l'aide de l'audit de partage dans Office 365, les administrateurs peuvent désormais générer cette liste. Voici comment procéder.
  
### <a name="step-1-search-for-sharing-events-and-export-the-results-to-a-csv-file"></a>Étape 1: Rechercher des événements de partage et exporter les résultats dans un fichier CSV

La première étape consiste à rechercher dans le journal d'audit Office 365 des événements de partage. Pour plus d'informations (y compris les autorisations requises) sur la recherche dans le journal d'audit, voir [Search the audit log &amp; dans le centre de sécurité conformité Office 365](search-the-audit-log-in-security-and-compliance.md).
  
1. Accédez à la page [https://protection.office.com](https://protection.office.com).
    
2. Connectez-vous à Office 365 à l'aide de votre compte scolaire ou professionnel.
    
3. Dans le volet gauche du centre de &amp; sécurité conformité, cliquez sur recherches de **recherche &amp; **, puis sur **recherche de journal d'audit**.
    
    La page **recherche du journal d'audit** s'affiche. 
    
4. Sous **activités**, cliquez sur **activités de partage** pour rechercher uniquement les événements de partage. 
    
    ![Sous activités, sélectionnez activités de partage](media/46bb25b7-1eb2-4adf-903a-cc9ab58639f9.png)
  
5.  Sélectionnez une date et une plage horaire pour rechercher les événements de partage qui se sont produits au cours de cette période. 
    
6. Cliquez sur **Rechercher** pour exécuter la recherche. 
    
7. Lorsque l'exécution de la recherche est terminée et que les résultats sont affichés, cliquez sur **Exporter les résultats** \> pour **Télécharger tous les résultats**.
    
    Une fois que vous avez sélectionné l'option Exporter, un message s'affiche en bas de la fenêtre qui vous invite à ouvrir ou à enregistrer le fichier CSV.
    
8. Cliquez sur **Enregistrer** \> **Enregistrer sous** et enregistrez le fichier CSV dans un dossier sur votre ordinateur local. 
    

  
### <a name="step-2-filter-the-csv-file-for-resources-shared-with-external-users"></a>Étape 2: filtrage du fichier CSV pour les ressources partagées avec des utilisateurs externes

L'étape suivante consiste à filtrer le fichier CSV pour les événements **SharingSet** et **SharingInvitationCreated** , et à afficher les événements pour lesquels la propriété **TargetUserOrGroupType** est **Guest**. Pour ce faire, utilisez la fonctionnalité Power Query dans Excel. La procédure suivante est effectuée dans Excel 2016. 
  
1. Dans Excel 2016, ouvrez un classeur vide.
    
2. Cliquez sur l’onglet **Données**. 
    
3. Cliquez sur **nouvelle requête** \> **à partir d'un fichier** \> **CSV**.
    
    ![Sous l'onglet données, sélectionnez nouvelle requête, sélectionnez à partir du fichier, puis à partir de CSV](media/5170ab34-b449-40ea-bd3f-f1432c1c5973.png)
  
4. Ouvrez le fichier CSV que vous avez téléchargé à l'étape 1.
    
    Le fichier CSV s'ouvre dans l'éditeur de requête. Notez qu'il y a quatre colonnes: **heure**, **utilisateur**, **action**et **détail**. La colonne de **détail** est un champ à plusieurs propriétés. L'étape suivante consiste à créer une nouvelle colonne pour chacune des propriétés dans la colonne de **détail** . 
    
5. Sélectionnez la **colonne détail** , puis, sous l'onglet **Accueil** , cliquez sur Fractionner les **colonnes** \> **par**délimiteur.
    
    ![Sous l'onglet Accueil, cliquez sur Fractionner la colonne, puis sur par déLimiteur.](media/aeb503e8-565b-42ea-91e2-9f127a74c00c.png)
  
6. Dans la fenêtre fractionner les **colonnes par** délimiteur, procédez comme suit: 
    
      - Sous **Sélectionner ou entrer le séparateur**, sélectionnez **virgule**.
    
      - Sous **fractionnement**, sélectionnez **à chaque occurrence du**délimiteur.
    
7. Cliquez sur **OK**.
    
    La colonne de **détail** est divisée en plusieurs colonnes. Chaque nouvelle colonne est nommée **Detail. 1**, **Detail. 2**, **Detail. 3**, etc. Vous remarquerez les valeurs de chaque cellule dans le **détail. n** les colonnes sont précédées du nom de la propriété; par exemple, **operation: SharingSet**, **operation: SharingInvitationAccepted**et **operation: SharingInvitationCreated**.
    
    ![La colonne de détail est divisée en plusieurs colonnes, une pour chaque propriété](media/4b104ead-0313-4bd4-b2a9-f143ccb378ac.png)
  
8. Sous l'onglet **fichier** , cliquez sur **fermer &amp; la charge** pour fermer l'éditeur de requête et ouvrez le fichier dans un classeur Excel. 
    
    L'étape suivante consiste à filtrer le fichier pour n'afficher que les événements **SharingSet** et **SharingInvitationCreated** . 
    
9. Accédez à l'onglet **Accueil** , puis sélectionnez la colonne **action** . 
    
10. Dans la liste déroulante ** &amp; filtre de tri** , effacez toutes les sélections, sélectionnez **SharingSet** et **SharingInvitationCreated**, puis cliquez sur **OK**.
    
    Excel affiche les lignes pour les événements **SharingSet** et **SharingInvitationCreated** . 
    
11. Accédez à la colonne nommée **Detail. 17** (ou quelle que soit la colonne qui contient la propriété **TargetUserOrGroupType** ) et sélectionnez-la. 
    
12. Dans la liste déroulante **filtre de tri &amp; ** , effacez toutes les sélections, sélectionnez **TargetUserOrGroupType: invité**, puis cliquez sur **OK**.
    
    À présent, Excel affiche les lignes pour les événements **SharingInvitationCreated** et **SharingSet** et l'emplacement de l'utilisateur cible à l'extérieur de votre organisation, car les utilisateurs externes sont identifiés par la valeur **TargetUserOrGroupType: Guest**. 
    
Le tableau suivant présente tous les utilisateurs de l'organisation qui ont partagé des ressources avec un utilisateur invité dans une plage de dates spécifiée.
  
![Partage d'événements dans le journal d'audit Office 365](media/0e0ecbe3-c794-4ca6-a2ca-63478fb3bb34.png)
  
Bien qu'elle ne soit pas incluse dans le tableau précédent, la colonne **Detail. 10** (ou la colonne contenant la propriété **ObjectID** ) identifie la ressource qui a été partagée avec l'utilisateur cible; par exemple `ObjectId:https:\/\/contoso-my.sharepoint.com\/personal\/sarad_contoso_com\/Documents\/Southwater Proposal.docx`.
  
> [!TIP]
> Si vous souhaitez identifier à quel moment un utilisateur invité a reçu des autorisations d'accès à une ressource (par opposition aux ressources partagées avec celles-ci), répétez les étapes 10, 11 et 12 et filtrez sur le **SharingInvitationAccepted** et **SharingSet **événements à l'étape 10. 
