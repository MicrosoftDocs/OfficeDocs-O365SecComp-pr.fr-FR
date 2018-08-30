---
title: Utiliser le partage de l’audit dans le journal d’audit de Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 2/13/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- BCS160
- MET150
ms.assetid: 50bbf89f-7870-4c2a-ae14-42635e0cfc01
description: 'Le partage est une activité dans SharePoint Online et OneDrive for Business. Les administrateurs peuvent maintenant utiliser le partage d’audit dans le journal d’audit d’Office 365 pour déterminer comment le partage est utilisé dans leur organisation. '
ms.openlocfilehash: 511f8b0e61d450659d78177d5b87fac9ee636cd4
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528212"
---
# <a name="use-sharing-auditing-in-the-office-365-audit-log"></a>Utiliser le partage de l’audit dans le journal d’audit de Office 365

Le partage est une activité dans SharePoint Online et OneDrive entreprise et largement utilisé dans les organisations Office 365. Les administrateurs peuvent maintenant utiliser le partage d’audit dans le journal d’audit d’Office 365 pour déterminer comment le partage est utilisé dans leur organisation. 
  
## <a name="the-sharepoint-sharing-schema"></a>Le schéma de partage SharePoint

Partage des événements (à l’exclusion des stratégie de partage et lier les événements) sont différentes des événements liées aux fichiers et un dossier d’une manière principale : un utilisateur effectue une action qui a des répercussions sur un autre utilisateur. Par exemple, l’utilisateur A donne accès utilisateur B vers un fichier. Dans cet exemple, l’utilisateur A est le *rôle d’utilisateur* et utilisateur B est l' *utilisateur cible*. Dans le schéma de fichier de SharePoint, action de l’utilisateur agissant n’affecte que le fichier proprement dit. Lorsque l’utilisateur A ouvre un fichier, les seules informations nécessaires dans l’événement **FileAccessed** est l’utilisateur agissant. Pour résoudre cette différence, il existe un schéma distinct, appelé le *schéma de partage SharePoint*, qui capture des informations supplémentaires sur le partage des événements. Cela garantit que les administrateurs ont plus de détails sur ayant une ressource partagée et l’utilisateur de la ressource a été partagé avec. 
  
Le schéma de partage fournit deux champs supplémentaires dans le journal d’audit liés au partage des événements : 
  
- **TargetUserOrGroupName** - stocke l’UPN ou le nom de l’utilisateur ou groupe cible qu’une ressource a été partagée avec (utilisateur B dans l’exemple précédent). 
    
- **TargetUserOrGroupType** - indique si l’utilisateur ou groupe cible est un membre, invité, groupe ou partenaire. 
    
Ces deux champs, en plus d’autres propriétés à partir d’Office 365 d’audit schéma du journal telle que l’utilisateur, opération et la Date peuvent l’histoire complète sur *la* ressource utilisateur partagé *quel* avec *lesquels* et *quand*. 
  
Il existe une autre propriété de schéma est importante de l’histoire de partage. La propriété **EventData** stocke des informations supplémentaires sur le partage des événements. Par exemple, lorsqu’un utilisateur partage un site avec un autre utilisateur, cette opération s’effectue en ajoutant l’utilisateur cible à un groupe SharePoint. La propriété **EventData** capture ces informations supplémentaires pour fournir un contexte pour les administrateurs. 

## <a name="the-sharepoint-sharing-model-and-sharing-events"></a>Modèle de partage et événements SharePoint

Partage réellement défini par trois événements distincts : **SharingSet**, **SharingInvitationCreated**et **SharingInvitaitonAccepted**. Voici le flux de travail pour le partage des événements sont consignés dans le journal d’audit de Office 365. 
  
![Organigramme du fonctionne de l’audit de partage](media/d83dd40f-919b-484f-bfd6-5dc8de31bff6.png)
  
Lorsqu’un utilisateur (agissant) souhaite partager une ressource avec un autre utilisateur (la cible), SharePoint (ou OneDrive entreprise) commence par vérifier si l’adresse de messagerie de l’utilisateur cible est déjà associé à un compte d’utilisateur dans l’annuaire de l’organisation. Si l’utilisateur cible se trouve dans le répertoire de l’organisation, SharePoint effectue les opérations suivantes :
  
-  Immédiatement attribue les autorisations d’utilisateur cible pour accéder à la ressource. 
    
- Envoie une notification de partage à l’adresse de messagerie de l’utilisateur cible.
    
- Enregistre un événement **SharingSet** . 
    
 Si un compte d’utilisateur pour l’utilisateur cible n’est pas dans l’annuaire de l’organisation, SharePoint effectue les opérations suivantes : 
  
- Crée une invitation de partage et l’envoie à l’adresse de messagerie de l’utilisateur cible.
    
- Enregistre un événement **SharingInvitationCreated** . 
    
    > [!NOTE]
    > L’événement **SharingInvitationCreated** associée presque toujours externe ou invité partage lors de l’utilisateur cible n’a pas accès à la ressource qui a été partagée. 
  
Lorsque l’utilisateur cible accepte l’invitation de partage qui lui a envoyé (en cliquant sur le lien dans l’invitation), SharePoint consigne un événement **SharingInvitationAccepted** et attribue les autorisations d’utilisateur cible pour accéder à la ressource. Plus d’informations sur l’utilisateur cible sont également connectés, telles que l’identité de l’utilisateur qui a été envoyée l’invitation et l’utilisateur ayant effectivement accepté l’invitation. Dans certains cas, ces utilisateurs (ou les adresses de messagerie) peuvent être différents. 
  

  
## <a name="how-to-identify-resources-shared-with-external-users"></a>Comment identifier les ressources partagées avec des utilisateurs externes

Une exigence courante pour les administrateurs consiste à créer une liste de toutes les ressources qui ont été partagés avec les utilisateurs en dehors de l’organisation. En utilisant le partage de l’audit dans Office 365, les administrateurs peuvent désormais générer cette liste. Voici comment.
  
### <a name="step-1-search-for-sharing-events-and-export-the-results-to-a-csv-file"></a>Étape 1 : Rechercher des événements de partage et exporter les résultats vers un fichier CSV

La première étape consiste à rechercher dans le journal d’audit Office 365 pour le partage d’événements. Pour plus d’informations (y compris les autorisations requises) sur la recherche dans le journal d’audit, consultez la rubrique [recherche dans le journal d’audit de sécurité Office 365 &amp; centre de conformité](search-the-audit-log-in-security-and-compliance.md).
  
1. Accédez à [https://protection.office.com](https://protection.office.com).
    
2. Connectez-vous à Office 365 à l’aide de votre compte professionnel ou de l’école.
    
3. Dans le volet gauche de la sécurité &amp; centre de conformité, cliquez sur **recherche &amp; enquête**, puis cliquez sur **Rechercher des journaux d’Audit**.
    
    La page de **recherche des journaux d’Audit** s’affiche. 
    
4. Sous **activités**, cliquez sur **activités de partage** pour rechercher uniquement des événements de partage. 
    
    ![Sous activités, sélectionnez les activités de partage](media/46bb25b7-1eb2-4adf-903a-cc9ab58639f9.png)
  
5.  Sélectionnez une plage de date et heure pour rechercher les événements de partage s’est produite dans ce délai. 
    
6. Cliquez sur **Rechercher** pour lancer la recherche. 
    
7. Lors de la recherche est terminée en cours d’exécution et les résultats sont affichés, cliquez sur **Exporter les résultats** \> **Téléchargez tous les résultats**.
    
    Une fois que vous sélectionnez l’option d’exportation, un message s’affiche en bas de la fenêtre qui vous invite à ouvrir ou enregistrer le fichier CSV.
    
8. Cliquez sur **Enregistrer** \> **Enregistrer sous** et enregistrez le fichier CSV dans un dossier sur votre ordinateur local. 
    

  
### <a name="step-2-filter-the-csv-file-for-resources-shared-with-external-users"></a>Étape 2 : Filtrer le fichier CSV pour les ressources partagées avec des utilisateurs externes

L’étape suivante consiste à filtrer le CSV pour les événements **SharingSet** et **SharingInvitationCreated** et pour afficher les événements dont la propriété **TargetUserOrGroupType** est **invité**. Vous allez utiliser la fonctionnalité de requête d’alimentation dans Excel pour effectuer cette opération. La procédure suivante est effectuée dans Excel 2016. 
  
1. Dans Excel, 2016, ouvrez un classeur vierge.
    
2. Cliquez sur l’onglet **Données**. 
    
3. Cliquez sur **Nouvelle requête** \> **à partir du fichier** \> **De CSV**.
    
    ![Sous l’onglet données, sélectionnez Nouvelle requête, sélectionnez fichier et sélectionnez CSV à partir de](media/5170ab34-b449-40ea-bd3f-f1432c1c5973.png)
  
4. Ouvrez le fichier CSV que vous avez téléchargé à l’étape 1.
    
    Le fichier CSV est ouvert dans l’éditeur de requête. Notez qu’il existe quatre colonnes : **heure**, **utilisateur**, **Action**et **Détail**. La colonne **Détail** est un champ de propriété à plusieurs. L’étape suivante consiste à créer une nouvelle colonne pour chacune des propriétés dans la colonne de **Détail** . 
    
5. Sélectionnez la colonne **Détail** , puis cliquez sur l’onglet **accueil** , **Colonne fractionnée** \> **Par délimiteur**.
    
    ![Sous l’onglet Accueil, cliquez sur la colonne fractionnée, puis cliquez sur par délimiteur](media/aeb503e8-565b-42ea-91e2-9f127a74c00c.png)
  
6. Dans la fenêtre de la **Colonne fractionnée par délimiteur** , procédez comme suit : 
    
      - Sous, **Sélectionnez ou entrez délimiteur**, sélectionnez **une virgule**.
    
      - Sous **Fractionné**, sélectionnez **à chaque occurrence du délimiteur**.
    
7. Cliquez sur **OK**.
    
    La colonne **Détail** est divisée en plusieurs colonnes. Chaque nouvelle colonne est nommé **Detail.1**, **Detail.2**, **Detail.3**et ainsi de suite. Vous constaterez que les valeurs de chacune des cellules dans les colonnes **Detail.n** portent le préfixe du nom de la propriété ; par exemple, **Opération : SharingSet**, **Opération : SharingInvitationAccepted**et **Opération : SharingInvitationCreated**.
    
    ![La colonne détail est divisée en plusieurs colonnes, une pour chaque propriété](media/4b104ead-0313-4bd4-b2a9-f143ccb378ac.png)
  
8. Sous l’onglet **fichier** , cliquez sur **Fermer &amp; charge** pour fermer l’éditeur de requête et ouvrez le fichier dans un classeur Excel. 
    
    L’étape suivante consiste à filtrer le fichier pour afficher uniquement les événements **SharingSet** et **SharingInvitationCreated** . 
    
9. Accédez à l’onglet **accueil** , puis sélectionnez la colonne **Action** . 
    
10. Dans la **tri &amp; Filter** liste déroulante, désactivez toutes les sélections, puis sélectionnez **SharingSet** et **SharingInvitationCreated**, puis cliquez sur **OK**.
    
    Excel affiche les lignes pour les événements **SharingSet** et **SharingInvitationCreated** . 
    
11. Accédez à la colonne nommée **Detail.17** (ou la colonne contient la propriété **TargetUserOrGroupType** ) et sélectionnez-le. 
    
12. Dans la **tri &amp; Filter** liste déroulante, désactivez toutes les sélections, sélectionnez **TargetUserOrGroupType:Guest**, puis cliquez sur **OK**.
    
    Excel affiche maintenant les lignes pour les événements **SharingInvitationCreated** et **SharingSet** et où l’utilisateur cible à l’extérieur de votre organisation, car les utilisateurs externes sont identifiés par la valeur **TargetUserOrGroupType:Guest**. 
    
Le tableau suivant indique tous les utilisateurs dans l’organisation et des ressources partagées avec un utilisateur invité au sein d’une plage de dates spécifiée.
  
![Journal d’audit de partage d’événements dans Office 365](media/0e0ecbe3-c794-4ca6-a2ca-63478fb3bb34.png)
  
Bien qu’il n’est pas inclus dans le tableau précédent, la colonne **Detail.10** (ou la colonne contient la propriété **ObjectId** ) identifie la ressource qui a été partagée avec l’utilisateur cible ; par exemple `ObjectId:https:\/\/contoso-my.sharepoint.com\/personal\/sarad_contoso_com\/Documents\/Southwater Proposal.docx`.
  
> [!TIP]
> Si vous souhaitez identifier quand un utilisateur invité a été réellement affecté des autorisations pour accéder à une ressource (au lieu de simplement les ressources dont partagé avec eux), répétez les étapes 10, 11 et 12 et filtrer les **SharingInvitationAccepted** et **SharingSet **événements à l’étape 10. 
