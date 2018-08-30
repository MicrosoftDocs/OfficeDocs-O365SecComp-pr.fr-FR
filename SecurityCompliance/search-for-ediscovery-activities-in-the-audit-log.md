---
title: Rechercher des activités de découverte électronique dans le journal d’audit d’Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/24/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 67cc7f42-a53d-4751-b929-6005c80798f7
description: Découvrez comment rechercher dans le journal d’audit Office 365 pour les événements qui sont consignés lorsque des administrateurs de conformité effectuer une recherche de contenu et eDiscovery cas la sécurité &amp; centre de conformité.
ms.openlocfilehash: 24bd629f5576fe042e59d5cbbdecf01b3fd59cf0
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528206"
---
# <a name="search-for-ediscovery-activities-in-the-office-365-audit-log"></a>Rechercher des activités de découverte électronique dans le journal d’audit d’Office 365

Activités de découverte électronique qui sont effectuées lors de la sécurité Office 365 et recherche de contenu &amp; centre de conformité ou en exécutant Windows PowerShell correspondant applets de commande sont consignés dans le journal d’audit de Office 365. Les événements sont enregistrés lorsque les administrateurs ou administrateurs de conformité (ou tout utilisateur qui est affecté eDiscovery autorisations) effectuez les tâches liées à la découverte électronique suivant recherche de contenu de sécurité Office 365 &amp; centre de conformité :
  
- Créer et gérer des affaires eDiscovery
    
- Création, de démarrage et de modification des recherches de contenu
    
- Effectuer les opérations de recherche de contenu, tels que l’aperçu, des résultats de recherche, suppression et exportation
    
- Configuration des autorisations de filtrage pour la recherche de contenu
    
- La gestion du rôle d’administrateur de découverte électronique
    
> [!IMPORTANT]
> Les activités décrites dans cet article sont uniquement le résultat de la découverte électronique tâches effectuées à l’aide de la sécurité &amp; centre de conformité. tâches de découverte électronique qui ont été effectuées à l’aide de l’outil de découverte électronique In-Place dans Exchange Online ou le centre eDiscovery dans SharePoint Online ne sont pas inclus. 
  
Pour plus d’informations sur la recherche dans le journal d’audit de Office 365, les autorisations qui sont nécessaires et l’exportation de résultats de recherche, voir [recherche dans le journal d’audit de sécurité Office 365 &amp; centre de conformité](search-the-audit-log-in-security-and-compliance.md).
  
## <a name="how-to-search-for-and-view-ediscovery-activities"></a>Comment rechercher et afficher les activités de découverte électronique

Actuellement, vous devez effectuer quelques opérations spécifiques permet d’afficher les activités de découverte électronique dans le journal d’audit d’Office 365. Voici comment.
  
1. Accédez à [https://protection.office.com](https://protection.office.com).
    
2. Connectez-vous à Office 365 à l’aide de votre compte professionnel ou de l’école.
    
3. Dans le volet gauche, cliquez sur **recherche &amp; enquête**, puis cliquez sur **Rechercher des journaux d’Audit**.
    
4. Dans la liste déroulante **activités** , sous **activités eDiscovery**, cliquez sur une ou plusieurs activités à rechercher. Ou vous pouvez cliquer sur **les activités de découverte électronique** pour rechercher toutes les activités liées à la découverte électronique. 
    
    > [!NOTE]
    > La liste déroulante des activités inclut également un groupe d’activités nommé **eDiscovery cmdlet activités** qui retourne des enregistrements de journal d’audit de l’applet de commande. 
  
5.  Sélectionnez une plage de date et heure pour afficher les événements de découverte électronique qui se sont produites pendant cette période. 
    
6. Dans la zone **utilisateurs** , sélectionnez un ou plusieurs utilisateurs pour afficher les résultats de recherche. Laissez cette zone vide de renvoi des entrées pour tous les utilisateurs. 
    
7. Cliquez sur **Rechercher** pour lancer la recherche à l’aide de vos critères de recherche. 
    
8. Une fois les résultats de recherche sont affichés, vous pouvez cliquer sur les **résultats de filtre** pour filtrer ou trier les enregistrements d’activité qui en résulte. Malheureusement, vous ne pouvez pas utiliser le filtrage à exclure explicitement certaines activités. 
    
9. Pour plus d’informations sur une activité, cliquez sur l’enregistrement d’activité dans la liste des résultats de recherche. 
    
    Une brusque **Détails** de page qui contient les propriétés détaillées de l’enregistrement de l’événement s’affiche. Pour afficher plus d’informations, cliquez sur **plus d’informations**. Pour obtenir une description de ces propriétés, consultez la section [propriétés détaillées pour les activités de découverte électronique](#detailed-properties-for-ediscovery-activities) . 

  
## <a name="ediscovery-activities"></a>activités de découverte électronique

Le tableau suivant décrit la recherche de contenu et les activités liées à la découverte électronique qui sont enregistrées lorsqu’un administrateur ou un utilisateur effectue une activité de découverte électronique à l’aide de la sécurité &amp; centre de conformité ou en exécutant l’applet de commande correspondante dans PowerShell distant qui est connecté à la sécurité de votre organisation &amp; centre de conformité. 
  
> [!NOTE]
> Les activités de découverte électronique décrites dans cette section fournissent des informations semblables aux activités eDiscovery applet de commande décrites dans la section suivante. Nous recommandons d’utiliser les activités de découverte électronique décrites dans cette section, car ils s’affichent dans les résultats de recherche du journal d’audit dans les 30 minutes. Nécessaire pour la découverte électronique dans les 24 heures activités d’applet de commande apparaissent dans les résultats de recherche du journal d’audit. 
  
|**Nom convivial**|**Operation**|**Applet de commande correspondant**|**Description**|
|:-----|:-----|:-----|:-----|
|Membre ajouté à un cas de découverte électronique  <br/> |CaseMemberAdded  <br/> |ComplianceCaseMember ajouter  <br/> |Un utilisateur a été ajouté en tant que membre d’un cas de découverte électronique. En tant que membre d’un cas, un utilisateur peut effectuer diverses tâches liées à la casse selon qu’ils sont affectées les autorisations nécessaires.  <br/> |
|Recherche de contenu modifiée  <br/> |SearchUpdated  <br/> |Set-ComplianceSearch  <br/> |Une recherche de contenu existante a été modifiée. Modifications peuvent inclure Ajout ou suppression des emplacements de contenu ou de la modification de la requête de recherche.  <br/> |
|Appartenance au groupe Administrateurs de découverte électronique modifié  <br/> |CaseAdminUpdated  <br/> |Mise à jour-eDiscoveryCaseAdmin  <br/> |La liste des administrateurs de découverte dans votre organisation a été modifiée. Cette action est consignée lors de la liste des administrateurs de découverte électronique est remplacée par un groupe de nouveaux utilisateurs. Si un utilisateur est ajouté ou supprimé, l’opération CaseAdminAdded est consignée.  <br/> |
|Cas de découverte électronique modifié  <br/> |CaseUpdated  <br/> |Set-ComplianceCase  <br/> |Un cas de découverte électronique a été modifié. Modifications incluent la fermeture d’un incident en cours ou rouvrir un incident fermé.  <br/> |
|Appartenance cas eDiscovery modifié  <br/> |CaseMemberUpdated  <br/> |Mise à jour-ComplianceCaseMember  <br/> |La liste d’appartenance d’un cas de découverte électronique a été modifiée. Cette action est consignée lors du remplacement de tous les membres d’un groupe de nouveaux utilisateurs. Si un seul membre est ajouté ou supprimé, opération CaseMemberAdded ou CaseMemberRemoved est enregistrée.  <br/> |
|Modification de filtre des autorisations de recherche  <br/> |SearchPermissionUpdated  <br/> |Set-ComplianceSecurityFilter  <br/> |Un filtre d’autorisations de recherche a été modifié.  <br/> |
|Requête de recherche modifiées pour blocage cas eDiscovery  <br/> |HoldUpdated  <br/> |Set-CaseHoldRule  <br/> |Un blocage de requête associé à un cas de découverte électronique a été modifié. Modifications possibles comprennent la modification de la requête ou mise en suspens de la plage de dates pour basée sur une requête.  <br/> |
|Élément d’aperçu de recherche de contenu téléchargé  <br/> |PreviewItemDownloaded  <br/> |S/O  <br/> |Un utilisateur téléchargé un élément sur leur ordinateur local (en cliquant sur le lien **Télécharger l’élément d’origine** ) s’afficher un aperçu des résultats de la recherche.  <br/> |
|Élément d’aperçu de recherche de contenu répertorié  <br/> |PreviewItemListed  <br/> |S/O  <br/> |Un utilisateur clique sur **Aperçu des résultats de recherche** pour afficher la page de résultats de recherche preview, qui répertorie les jusqu'à 1 000 éléments dans les résultats d’une recherche de contenu.  <br/> |
|Recherche de contenu aperçu affiché  <br/> |PreviewItemRendered  <br/> |S/O  <br/> |Un gestionnaire de découverte électronique afficher un élément en cliquant dessus lors de l’aperçu des résultats de la recherche.  <br/> |
|Recherche de contenu créée  <br/> |SearchCreated  <br/> |New-ComplianceSearch  <br/> |Une recherche de contenu a été créée.  <br/> |
|Administrateur de créer d’eDiscovery  <br/> |CaseAdminAdded  <br/> |EDiscoveryCaseAdmin ajouter  <br/> |Un utilisateur a été ajouté en tant qu’une administrateur de découverte électronique dans l’organisation.  <br/> |
|Cas de découverte électronique créé  <br/> |CaseAdded  <br/> |Nouvelle ComplianceCase  <br/> |Un cas de découverte électronique a été créé. Création d’un cas, il vous suffit de lui donner un nom. Autres tâches liées à la casse, telles que l’ajout de membres, création de suspensions et la création de recherches de contenu associés avec le résultat de la cas dans d’autres événements en cours de journalisation.  <br/> |
|Créé le filtre de recherche des autorisations  <br/> |SearchPermissionCreated  <br/> |Nouvelle ComplianceSecurityFilter  <br/> |Un filtre d’autorisations de recherche a été créé.  <br/> |
|Requête de recherche créés pour mettre en attente cas eDiscovery  <br/> |HoldCreated  <br/> |Nouvelle CaseHoldRule  <br/> |Un blocage de requête associé à un cas de découverte électronique a été créé.  <br/> |
|Recherche de contenu supprimée  <br/> |SearchRemoved  <br/> |Remove-ComplianceSearch  <br/> |Une recherche de contenu existante a été supprimée.  <br/> |
|Administrateur de la découverte électronique supprimé  <br/> |CaseAdminRemoved  <br/> |Remove-eDiscoveryCaseAdmin  <br/> |Une administrateur de découverte électronique a été supprimée de votre organisation.  <br/> |
|Cas de découverte électronique supprimé  <br/> |CaseRemoved  <br/> |Remove-ComplianceCase  <br/> |Un cas de découverte électronique a été supprimé. Notez que toute suspension associée au cas doit être supprimé avant de pouvoir supprimer le cas.  <br/> |
|Filtre des autorisations de recherche supprimés  <br/> |SearchPermissionRemoved  <br/> |Remove-ComplianceSecurityFilter  <br/> |Un filtre d’autorisations de recherche a été supprimé.  <br/> |
|Requête de recherche supprimés pour blocage cas eDiscovery  <br/> |HoldRemoved  <br/> |Remove-CaseHoldRule  <br/> |Un blocage de requête associé à un cas de découverte électronique a été supprimé. Suppression de la requête à partir de la suspension est souvent le résultat de la suppression d’une suspension. Lors d’une suspension ou une requête de suspension sont supprimés, les emplacements de contenu qui ont été en attente sont annulées.  <br/> |
|Exportation téléchargée de recherche de contenu  <br/> |SearchResultDownloaded  <br/> |S/O  <br/> |Un utilisateur a téléchargé les résultats d’une recherche de contenu sur leur ordinateur local. Notez qu’une activité **démarré l’exportation de la recherche de contenu** soient initialisées avant que les résultats de la recherche peuvent être téléchargés.<br/> |
|Aperçu des résultats de recherche de contenu  <br/> |SearchPreviewed  <br/> |S/O  <br/> |Un utilisateur les résultats d’une recherche de contenu d’aperçu.  <br/> |
|Purgés de résultats de recherche de contenu  <br/> |SearchResultsPurged  <br/> |New-ComplianceSearchAction  <br/> |Un utilisateur purgés les résultats d’une recherche de contenu en exécutant la **New-ComplianceSearchAction-purger** commande.  <br/> |
|Suppression d’analyse de recherche de contenu  <br/> |RemovedSearchResultsSentToZoom  <br/> |Remove-ComplianceSearchAction  <br/> |Une recherche de contenu préparer (en vue de résultats de recherche pour la découverte Office 365 avancée) a été supprimé. Si l’action de la préparation a moins de deux semaines, les résultats de recherche qui ont été préparés pour la découverte avancée ont été supprimés de la zone de stockage Microsoft Azure. Si l’action de la préparation est antérieure à 2 semaines, cet événement indique qu’uniquement l’action préparation correspondant a été supprimée.  <br/> |
|Exportation supprimée de la recherche de contenu  <br/> |RemovedSearchExported  <br/> |Remove-ComplianceSearchAction  <br/> |Une action d’exportation de recherche de contenu a été supprimée. Si l’action de l’exportation a moins de deux semaines, les résultats de recherche qui ont été téléchargés dans la zone de stockage Microsoft Azure ont été supprimées. Si l’action d’exportation est antérieure à 2 semaines, cet événement indique que seule l’action d’exportation correspondant a été supprimée.  <br/> |
|Membres supprimés dans le cas de découverte électronique  <br/> |CaseMemberRemoved  <br/> |Remove-ComplianceCaseMember  <br/> |Un utilisateur a été supprimé en tant que membre d’un cas de découverte électronique.  <br/> |
|Supprimer l’aperçu des résultats de recherche de contenu  <br/> |RemovedSearchPreviewed  <br/> |Remove-ComplianceSearchAction  <br/> |Une action d’aperçu de recherche de contenu a été supprimée.  <br/> |
|Purge supprimées action effectuée sur la recherche de contenu  <br/> |RemovedSearchResultsPurged  <br/> |Remove-ComplianceSearchAction  <br/> |Une action de vidage de recherche de contenu a été supprimée.  <br/> |
|Supprimer le rapport de recherche  <br/> |SearchReportRemoved  <br/> |Remove-ComplianceSearchAction  <br/> |Une recherche de contenu Exporter rapport action a été supprimée.  <br/> |
|Prise en main d’analyse de recherche de contenu  <br/> |SearchResultsSentToZoom  <br/> |New-ComplianceSearchAction  <br/> |Les résultats d’une recherche de contenu ont été préparés pour l’analyse d’eDiscovery avancée.  <br/> |
|Recherche de contenu de prise en main  <br/> |SearchStarted  <br/> |Start-ComplianceSearch  <br/> |Une recherche de contenu a été démarrée. Lorsque vous créez ou modifiez une recherche de contenu à l’aide de la sécurité &amp; GUI de centre de conformité, la recherche démarre automatiquement. Si vous créez ou modifiez une recherche à l’aide de **New-ComplianceSearch** ou l’applet de commande **Set-ComplianceSearch** , vous devez exécuter l’applet de commande **Start-ComplianceSearch** pour lancer la recherche.<br/> |
|Prise en main d’exportation de la recherche de contenu  <br/> |SearchExported  <br/> |New-ComplianceSearchAction  <br/> |Un utilisateur exporté les résultats d’une recherche de contenu.  <br/> |
|Rapport d’exportation de prise en main  <br/> |SearchReport  <br/> |New-ComplianceSearchAction  <br/> |Un utilisateur exporté un état de la recherche de contenu.  <br/> |
|Arrêt de la recherche de contenu  <br/> |SearchStopped  <br/> |Stop-ComplianceSearch  <br/> |Un utilisateur a arrêté une recherche de contenu.  <br/> |
  
## <a name="ediscovery-cmdlet-activities"></a>activités de cmdlet eDiscovery

Le tableau suivant répertorie les enregistrements du journal d’audit applet de commande qui sont enregistrés lorsqu’un administrateur ou un utilisateur effectue une activité de découverte électronique à l’aide de la sécurité &amp; centre de conformité ou en exécutant l’applet de commande correspondante dans PowerShell distant qui de connecté à la sécurité de votre organisation &amp; centre de conformité. Notez que les informations détaillées de l’enregistrement du journal d’audit sont différentes pour les activités de l’applet de commande répertoriées dans ce tableau et les activités de découverte électronique décrites dans la section précédente. 
  
Comme indiqué précédemment, il faut jusqu'à 24 heures pour la découverte électronique activités d’applet de commande apparaissent dans les résultats de recherche du journal d’audit.
  
> [!TIP]
> Les applets de commande dans la colonne **opération** dans le tableau suivant sont liés à la rubrique d’aide correspondante cmdlet sur TechNet. Accédez à la rubrique d’aide applet de commande pour obtenir une description des paramètres disponibles pour chaque applet de commande. Le paramètre et la valeur du paramètre qui ont été utilisés avec une applet de commande sont inclus dans l’entrée du journal d’audit pour chaque activité eDiscovery applet de commande qui est consignée. 
  
|**Nom convivial**|**Opération (cmdlet)**|**Description**|
|:-----|:-----|:-----|
|Suspension créée dans le cas de découverte électronique  <br/> |[Nouvelle CaseHoldPolicy](https://go.microsoft.com/fwlink/p/?LinkId=823813) <br/> |Un blocage a été créé pour un cas de découverte électronique. Une suspension peut être créée avec ou sans indication d’une source de contenu. Si les sources de contenu sont spécifiés, ils allez identifiés dans l’entrée du journal d’audit.  <br/> |
|Suspension supprimée à partir de cas de découverte électronique  <br/> |[Remove-CaseHoldPolicy](https://go.microsoft.com/fwlink/p/?LinkId=823814) <br/> |Un blocage qui est associé à un cas de découverte électronique a été supprimé. Suppression d’une suspension libère tous les emplacements de contenu à partir de la suspension. Entraîne la suppression de la suspension également supprimer les règles de casse attente associés à la suspension (voir **Remove-CaseHoldRule** ci-dessous).<br/> |
|Suspension modifiée en cas de découverte électronique  <br/> |[Set-CaseHoldPolicy](https://go.microsoft.com/fwlink/p/?LinkId=823815) <br/> |Un blocage qui est associé à une découverte électronique a été modifié. Ajout ou suppression des emplacements de contenu ou la désactivation (désactivation) sont les éventuelles modifications la suspension.  <br/> |
|Requête de recherche créés pour mettre en attente cas eDiscovery  <br/> |[Nouvelle CaseHoldRule](https://go.microsoft.com/fwlink/p/?LinkId=823816) <br/> |Un blocage de requête associé à un cas de découverte électronique a été créé.  <br/> |
|Requête de recherche supprimés pour blocage cas eDiscovery  <br/> |[Remove-CaseHoldRule](https://go.microsoft.com/fwlink/p/?LinkId=823820) <br/> |Un blocage de requête associé à un cas de découverte électronique a été supprimé. Suppression de la requête à partir de la suspension est souvent le résultat de la suppression d’une suspension. Lors d’une suspension ou une requête de suspension sont supprimés, les emplacements de contenu qui ont été en attente sont annulées.  <br/> |
|Requête de recherche modifiées pour blocage cas eDiscovery  <br/> |[Set-CaseHoldRule](https://go.microsoft.com/fwlink/p/?LinkId=823819) <br/> |Un blocage de requête associé à un cas de découverte électronique a été modifié. Modifications possibles comprennent la modification de la requête ou mise en suspens de la plage de dates pour basée sur une requête.  <br/> |
|Cas de découverte électronique créé  <br/> |[Nouvelle ComplianceCase](https://go.microsoft.com/fwlink/p/?LinkId=823842) <br/> |Un cas de découverte électronique a été créé. Création d’un cas, il vous suffit de lui donner un nom. Autres tâches liées à la casse, telles que l’ajout de membres, création de suspensions et la création de recherches de contenu associés avec le résultat de la cas dans d’autres événements en cours de journalisation.  <br/> |
|Cas de découverte électronique supprimé  <br/> |[Remove-ComplianceCase](https://go.microsoft.com/fwlink/p/?LinkId=823844) <br/> |Un cas de découverte électronique a été supprimé. Notez que toute suspension associée au cas doit être supprimé avant de pouvoir supprimer le cas.  <br/> |
|Cas de découverte électronique modifié  <br/> |[Set-ComplianceCase](https://go.microsoft.com/fwlink/p/?LinkId=823846) <br/> |Un cas de découverte électronique a été modifié. Modifications incluent la fermeture d’un incident en cours ou rouvrir un incident fermé.  <br/> |
|Membre ajouté à un cas de découverte électronique  <br/> |[ComplianceCaseMember ajouter](https://go.microsoft.com/fwlink/p/?LinkId=823848) <br/> |Un utilisateur a été ajouté en tant que membre d’un cas de découverte électronique. En tant que membre d’un cas, un utilisateur peut effectuer diverses tâches liées à la casse selon qu’ils sont affectées les autorisations nécessaires.  <br/> |
|Membres supprimés dans le cas de découverte électronique  <br/> |[Remove-ComplianceCaseMember](https://go.microsoft.com/fwlink/p/?LinkId=823849) <br/> |Un utilisateur a été supprimé en tant que membre d’un cas de découverte électronique.  <br/> |
|Appartenance cas eDiscovery modifié  <br/> |[Mise à jour-ComplianceCaseMember](https://go.microsoft.com/fwlink/p/?LinkId=823850) <br/> |La liste d’appartenance d’un cas de découverte électronique a été modifiée. Cette action est consignée lors du remplacement de tous les membres d’un groupe de nouveaux utilisateurs. Si un seul membre est ajouté ou supprimé, l’opération **Add-ComplianceCaseMember** ou **Remove-ComplianceCaseMember** est consignée.<br/> |
|Recherche de contenu créée  <br/> |[New-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517935) <br/> |Une recherche de contenu a été créée.  <br/> |
|Recherche de contenu supprimée  <br/> |[Remove-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517936) <br/> |Une recherche de contenu existante a été supprimée.  <br/> |
|Recherche de contenu modifiée  <br/> |[Set-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517937) <br/> |Une recherche de contenu existante a été modifiée. Modifications peuvent inclure Ajout ou suppression des emplacements de contenu qui sont recherchés et modification de la requête de recherche.  <br/> |
|Recherche de contenu de prise en main  <br/> |[Start-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517938) <br/> |Une recherche de contenu a été démarrée. Lorsque vous créez ou modifiez une recherche de contenu à l’aide de la sécurité &amp; GUI de centre de conformité, la recherche démarre automatiquement. Si vous créez ou modifiez une recherche à l’aide de **New-ComplianceSearch** ou l’applet de commande **Set-ComplianceSearch** , vous devez exécuter l’applet de commande **Start-ComplianceSearch** pour lancer la recherche.<br/> |
|Arrêt de la recherche de contenu  <br/> |[Stop-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517939) <br/> |Une recherche de contenu en cours d’exécution a été arrêtée.  <br/> |
|Création d’action de recherche de contenu  <br/> |[New-ComplianceSearchAction](https://go.microsoft.com/fwlink/p/?LinkId=527971) <br/> |Une action de recherche de contenu a été créée. Actions de recherche de contenu sont afficher un aperçu des résultats de la recherche, l’exportation de résultats de recherche, préparation des résultats de recherche pour l’analyse dans Office 365 avancée de découverte électronique et supprimer définitivement les éléments qui correspondent aux critères de recherche d’une recherche de contenu.  <br/> |
|Action de recherche de contenu supprimé  <br/> |[Remove-ComplianceSearchAction](https://go.microsoft.com/fwlink/p/?LinkId=824027) <br/> |Une action de recherche de contenu a été supprimée.  <br/> |
|Créé le filtre de recherche des autorisations  <br/> |[Nouvelle ComplianceSecurityFilter](https://go.microsoft.com/fwlink/p/?LinkId=617542) <br/> |Un filtre d’autorisations de recherche a été créé.  <br/> |
|Filtre des autorisations de recherche supprimés  <br/> |[Remove-ComplianceSecurityFilter](https://go.microsoft.com/fwlink/p/?LinkId=617543) <br/> |Un filtre d’autorisations de recherche a été supprimé.  <br/> |
|Modification de filtre des autorisations de recherche  <br/> |[Set-ComplianceSecurityFilter](https://go.microsoft.com/fwlink/p/?LinkId=617544) <br/> |Un filtre d’autorisations de recherche a été modifié.  <br/> |
|Administrateur de créer d’eDiscovery  <br/> |[EDiscoveryCaseAdmin ajouter](https://go.microsoft.com/fwlink/p/?LinkId=798217) <br/> |Un utilisateur a été ajouté en tant qu’une administrateur de découverte électronique dans votre organisation.  <br/> |
|Administrateur de la découverte électronique supprimé  <br/> |[Remove-eDiscoveryCaseAdmin](https://go.microsoft.com/fwlink/p/?LinkId=823945) <br/> |Une administrateur de découverte électronique a été supprimée de votre organisation.  <br/> |
|Appartenance au groupe Administrateurs de découverte électronique modifié  <br/> |[Mise à jour-eDiscoveryCaseAdmin](https://go.microsoft.com/fwlink/p/?LinkId=823946) <br/> |La liste des administrateurs de découverte dans votre organisation a été modifiée. Cette action est consignée lors de la liste des administrateurs de découverte électronique est remplacée par un groupe de nouveaux utilisateurs. Si un utilisateur est ajouté ou supprimé, l’opération **Add-eDiscoveryCaseAdmin** ou **Remove-eDiscoveryCaseAdmin** est consignée.<br/> |
   
## <a name="detailed-properties-for-ediscovery-activities"></a>Propriétés détaillées pour les activités de découverte électronique

Le tableau suivant décrit les propriétés qui sont incluses lorsque vous cliquez sur **plus d’informations** sur la page de **Détails** d’une activité eDiscovery répertoriée dans les résultats de recherche. Ces propriétés sont également incluses dans le fichier CSV lorsque vous exportez les résultats de recherche du journal d’audit. Notez qu’un enregistrement du journal d’audit d’une activité de découverte ne sont pas inclure toutes les propriétés détaillées ci-dessous. 
  
> [!TIP]
> Lorsque vous exportez les résultats de recherche, le fichier CSV contient une colonne nommée **Détail**qui contient les propriétés détaillées décrites dans le tableau suivant dans une propriété à valeurs multiples. Vous pouvez utiliser la fonctionnalité de requête d’alimentation dans Excel pour fractionner cette colonne sur plusieurs colonnes afin que chaque propriété possède sa propre colonne. Cela vous permet de trier et filtrer sur un ou plusieurs de ces propriétés. Pour plus d’informations, consultez la section « Exporter les résultats de recherche dans un fichier » de la [recherche, ouvrez une session de l’audit dans la sécurité pour Microsoft Office 365 et le centre de conformité ](search-the-audit-log-in-security-and-compliance.md#step-4-export-the-search-results-to-a-file). 
  
|**Propriété**|**Description**|
|:-----|:-----|
|Cas  <br/> |L’identité (GUID) de la casse de découverte électronique qui a été créée, modifié ou supprimé.  <br/> |
|ClientApplication  <br/> |activités de cmdlet eDiscovery ont la valeur de la **console de gestion Exchange** pour cette propriété. Cela indique que l’activité a été effectuée à l’aide de la sécurité &amp; interface utilisateur du centre de conformité ou l’exécution de l’applet de commande dans PowerShell.<br/> |
|ClientIP  <br/> |L’adresse IP du périphérique qui a été utilisé lors de l’activité a été enregistrée. L’adresse IP est affichée dans le format d’adresse IPv4 ou IPv6.  <br/> |
|ClientRequestId  <br/> | Pour les activités de découverte électronique, cette propriété est généralement vide.  <br/> |
|CmdletVersion  <br/> |Le numéro de la version de la sécurité &amp; centre de conformité en cours d’exécution dans votre organisation.  <br/> |
|CreationTime  <br/> |La date et l’heure en temps universel coordonné (UTC) lorsque l’activité de découverte électronique s’est terminée.  <br/> |
|EffectiveOrganization  <br/> |Le nom de la votre organisation Office 365.  <br/> |
|ExchangeLocations  <br/> |Les boîtes aux lettres Exchange Online qui sont inclus dans une recherche de contenu ou mis en attente dans un cas eDiscovery.  <br/> |
|Exclusions  <br/> |Emplacements de boîte aux lettres ou de site qui sont exclus d’une recherche de contenu ou une suspension dans un cas eDiscovery.  <br/> |
|ExtendedProperties  <br/> |Propriétés supplémentaires à partir d’un contenu de recherche, une action de recherche de contenu, ou blocage dans un cas eDiscovery, telles que le GUID de l’objet et l’applet de commande correspondant et paramètres d’applet de commande qui ont été utilisés lors de l’exécution de l’activité.  <br/> |
|Id  <br/> |ID de l’entrée du rapport. L’ID identifie l’entrée du journal d’audit.  <br/> |
|NonPIIParameters  <br/> |Liste des paramètres (sans aucune valeur) qui ont été utilisés avec l’applet de commande identifié dans la propriété de l’opération. Les paramètres répertoriés dans cette propriété sont les mêmes que celles répertoriées dans la propriété Parameters.  <br/> |
|ObjectId  <br/> |Le GUID ou le nom de l’objet (par exemple, une recherche de contenu ou un cas de découverte électronique) qui a été créé, modifié ou supprimé par l’activité répertoriée dans la propriété Operation. Cet objet est également identifié dans la colonne de l’élément dans les résultats de recherche du journal d’audit.  <br/> |
|ObjectType  <br/> |Le type d’objet de découverte électronique que l’utilisateur créé, supprimé ou modifié ; par exemple une action de recherche de contenu (preview, exporter ou purge), un cas de découverte électronique ou une recherche de contenu.  <br/> |
|Opération  <br/> |Le nom de l’opération qui correspond à l’activité de découverte électronique qui a été effectuée.  <br/> |
|OrganizationId  <br/> |Le GUID de votre organisation Office 365.  <br/> |
|Paramètres  <br/> |Le nom et la valeur pour les paramètres qui ont été utilisés avec l’applet de commande correspondante.  <br/> |
|PublicFolderLocations  <br/> |Les emplacements de dossiers publics dans Exchange Online qui sont inclus dans une recherche de contenu ou mis en attente dans un cas eDiscovery.  <br/> |
|Requête  <br/> |La requête de recherche associée à l’activité, par exemple une recherche de contenu ou un blocage de requête.  <br/> |
|RecordType  <br/> |Le type d’opération indiquée par l’enregistrement. La valeur de **18** indique un événement lié à une activité répertoriée dans la section [activités d’applet de commande eDiscovery](#ediscovery-cmdlet-activities) . La valeur **24** indique un événement lié à une activité répertoriée dans la section [comment rechercher et afficher les activités de découverte électronique](#how-to-search-for-and-view-ediscovery-activities) .<br/> |
|ResultStatus  <br/> |Indique si l’action (spécifiée dans la propriété Operation) a réussi ou non.  <br/> |
|SecurityComplianceCenterEventType  <br/> |Indique que l’activité a une sécurité &amp; événement centre de conformité. Toutes les activités de découverte électronique aura la valeur **0** pour cette propriété.<br/> |
|SharepointLocations  <br/> |Les sites SharePoint Online qui sont inclus dans une recherche de contenu ou mis en attente dans un cas eDiscovery.  <br/> |
|StartTime  <br/> |La date et l’heure en temps universel coordonné (UTC) lorsque l’activité de découverte électronique a été démarrée.  <br/> |
|Nom d’utilisateur  <br/> |L’utilisateur qui a effectué l’activité (spécifiée dans la propriété Operation) qui a provoqué l’enregistrement en cours de journalisation. Notez que les enregistrements de découverte électronique activité effectuée par des comptes système (par exemple, Autorite NT\SYSTEM) sont également inclus dans le journal d’audit.  <br/> |
|UserKey  <br/> |Un autre ID de l’utilisateur identifié dans la propriété UserId. Pour les activités de découverte électronique, la valeur de cette propriété est généralement identique à la propriété UserId.  <br/> |
|UserServicePlan  <br/> |L’abonnement à Office 365 utilisé par votre organisation. Pour les activités de découverte électronique, cette propriété est généralement vide.  <br/> |
|UserType  <br/> |Le type d’utilisateur qui a effectué l’opération. Les valeurs suivantes indiquent le type d’utilisateur.  <br/> 0 un utilisateur standard. 2 un administrateur de votre organisation Office 365. 3 un centre de données administrateur ou centre de données système compte Microsoft. 4 un compte système. 5 une application. 6 un principal de service. |
|Version  <br/> |Indique le numéro de version de l’activité (identifiée par la propriété Operation) qui est connecté.  <br/> |
|Charge de travail  <br/> |Le service Office 365 où l’activité s’est produite. Pour les activités de découverte électronique, la valeur est **SecurityComplianceCenter**.<br/> |
