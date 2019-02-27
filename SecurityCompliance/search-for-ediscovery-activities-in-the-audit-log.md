---
title: Rechercher des activités eDiscovery dans le journal d'audit Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/24/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 67cc7f42-a53d-4751-b929-6005c80798f7
description: Découvrez comment rechercher dans le journal d'audit Office 365 des événements consignés lorsque les administrateurs de conformité effectuent des tâches de recherche de &amp; contenu et de cas eDiscovery dans le centre de sécurité conformité.
ms.openlocfilehash: f4778fd2aab48d58b3104dd2466875ba53e2c0a0
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296757"
---
# <a name="search-for-ediscovery-activities-in-the-office-365-audit-log"></a>Rechercher des activités eDiscovery dans le journal d'audit Office 365

Les activités de recherche de contenu et de découverte électronique qui sont effectuées dans &amp; le centre de sécurité conformité d'Office 365 ou en exécutant les cmdlets Windows PowerShell correspondantes sont consignées dans le journal d'audit Office 365. Les événements sont consignés lorsque les administrateurs ou les administrateurs de conformité (ou tout utilisateur disposant d'autorisations eDiscovery) effectuent les tâches de recherche de contenu et &amp; de découverte électronique suivantes dans le centre de sécurité conformité Office 365:
  
- Création et gestion de cas eDiscovery
    
- Création, démarrage et modification de recherches de contenu
    
- Exécution d'actions de recherche de contenu, telles que l'aperçu, l'exportation et la suppression des résultats de recherche
    
- Configuration du filtrage des autorisations pour la recherche de contenu
    
- Gestion du rôle d'administrateur eDiscovery
    
> [!IMPORTANT]
> Les activités décrites dans cet article sont uniquement le résultat des tâches eDiscovery effectuées à l'aide du &amp; Centre de sécurité conformité. les tâches eDiscovery qui ont été effectuées à l'aide de l'outil de découverte électronique inaltérable dans Exchange Online ou dans le centre eDiscovery dans SharePoint Online ne sont pas incluses. 
  
Pour plus d'informations sur la recherche dans le journal d'audit Office 365, les autorisations requises et l'exportation des résultats [de la recherche, voir Search the audit log &amp; dans le centre de sécurité conformité Office 365](search-the-audit-log-in-security-and-compliance.md).
  
## <a name="how-to-search-for-and-view-ediscovery-activities"></a>Comment rechercher et afficher des activités eDiscovery

Actuellement, vous devez effectuer quelques opérations spécifiques pour afficher les activités de découverte électronique dans le journal d'audit Office 365. Voici comment procéder.
  
1. Accédez à la page [https://protection.office.com](https://protection.office.com).
    
2. Connectez-vous à Office 365 à l'aide de votre compte scolaire ou professionnel.
    
3. Dans le volet de gauche, cliquez sur recherches de **recherche &amp; **, puis sur **recherche de journal d'audit**.
    
4. Dans la liste déroulante **activités** , sous **activités de découverte électronique**, cliquez sur une ou plusieurs activités à rechercher. Vous pouvez aussi cliquer sur **activités eDiscovery** pour rechercher toutes les activités eDiscovery associées. 
    
    > [!NOTE]
    > La liste déroulante activités inclut également un groupe d'activités nommé **activités de la cmdlet eDiscovery** qui renverra des enregistrements à partir du journal d'audit de l'applet de commande. 
  
5.  Sélectionnez une date et une plage horaire pour afficher les événements eDiscovery qui se sont produits au cours de cette période. 
    
6. Dans la zone **utilisateurs** , sélectionnez un ou plusieurs utilisateurs pour lesquels vous souhaitez afficher les résultats de la recherche. Laissez cette zone vide pour renvoyer les entrées de tous les utilisateurs. 
    
7. Cliquez sur **Rechercher** pour exécuter la recherche à l'aide de vos critères de recherche. 
    
8. Une fois les résultats de la recherche affichés, vous pouvez cliquer sur **Filtrer les résultats** pour filtrer ou trier les enregistrements d'activité résultants. Malheureusement, vous ne pouvez pas utiliser le filtrage pour exclure explicitement certaines activités. 
    
9. Pour afficher les détails d'une activité, cliquez sur l'enregistrement d'activité dans la liste des résultats de la recherche. 
    
    Une page de survol des **Détails** s'affiche et contient les propriétés détaillées de l'enregistrement d'événement. Pour afficher des détails supplémentaires, cliquez sur **informations**supplémentaires. Pour obtenir une description de ces propriétés, reportez-vous à la section [Propriétés détaillées pour les activités eDiscovery](#detailed-properties-for-ediscovery-activities) . 

  
## <a name="ediscovery-activities"></a>activités eDiscovery

Le tableau suivant décrit la recherche de contenu et les activités liées à la découverte électronique qui sont consignées lorsqu'un administrateur ou un utilisateur effectue une activité &amp; de découverte électronique à l'aide du centre de sécurité conformité ou en exécutant l'applet de commande correspondante dans Remote PowerShell qui est connecté au centre de sécurité &amp; conformité de votre organisation. 
  
> [!NOTE]
> Les activités eDiscovery décrites dans cette section fournissent des informations similaires aux activités de l'applet de commande eDiscovery décrite dans la section suivante. Nous vous recommandons d'utiliser les activités eDiscovery décrites dans cette section, car elles apparaîtront dans les résultats de la recherche dans le journal d'audit dans les 30 minutes. Il faut 24 heures pour que les activités de la cmdlet eDiscovery apparaissent dans les résultats de la recherche dans le journal d'audit. 
  
|**Nom convivial**|**Operation**|**Cmdlet correspondante**|**Description**|
|:-----|:-----|:-----|:-----|
|Ajout d'un membre au cas eDiscovery  <br/> |CaseMemberAdded  <br/> |Add-ComplianceCaseMember  <br/> |Un utilisateur a été ajouté en tant que membre d'un cas de découverte électronique. En tant que membre d'un cas, un utilisateur peut effectuer différentes tâches liées à la casse selon qu'il a reçu ou non les autorisations nécessaires.  <br/> |
|Recherche de contenu modifiée  <br/> |SearchUpdated  <br/> |Set-ComplianceSearch  <br/> |Une recherche de contenu existante a été modifiée. Les modifications peuvent inclure l'ajout ou la suppression d'emplacements de contenu ou la modification de la requête de recherche.  <br/> |
|Appartenance à un administrateur eDiscovery modifiée  <br/> |CaseAdminUpdated  <br/> |Update-eDiscoveryCaseAdmin  <br/> |La liste des administrateurs eDiscovery de votre organisation a été modifiée. Cette activité est enregistrée lorsque la liste des administrateurs eDiscovery est remplacée par un groupe de nouveaux utilisateurs. Si un seul utilisateur est ajouté ou supprimé, l'opération CaseAdminAdded est enregistrée.  <br/> |
|Cas de découverte électronique modifiée  <br/> |CaseUpdated  <br/> |Set-ComplianceCase  <br/> |Un cas de découverte électronique a été modifié. Les modifications incluent la fermeture d'un cas ouvert ou la réouverture d'un cas fermé.  <br/> |
|Appartenance au cas de découverte électronique modifiée  <br/> |CaseMemberUpdated  <br/> |Update-ComplianceCaseMember  <br/> |La liste d'appartenance d'un cas de découverte électronique a été modifiée. Cette activité est enregistrée lorsque tous les membres sont remplacés par un groupe de nouveaux utilisateurs. Si un seul membre est ajouté ou supprimé, l'opération CaseMemberAdded ou CaseMemberRemoved est enregistrée.  <br/> |
|Filtre des autorisations de recherche modifié  <br/> |SearchPermissionUpdated  <br/> |Set-ComplianceSecurityFilter  <br/> |Un filtre d'autorisations de recherche a été modifié.  <br/> |
|Modification d'une requête de recherche pour la conservation de cas eDiscovery  <br/> |HoldUpdated  <br/> |Set-CaseHoldRule  <br/> |Une conservation basée sur une requête associée à un cas de découverte électronique a été modifiée. Les modifications possibles incluent la modification de la requête ou de la plage de dates pour une conservation basée sur une requête.  <br/> |
|Élément d'aperçu de recherche de contenu téléchargé  <br/> |PreviewItemDownloaded  <br/> |S/O  <br/> |Un utilisateur A téléchargé un élément sur son ordinateur local (en cliquant sur le lien **Télécharger l'élément d'origine** ) lors de l'aperçu des résultats de la recherche.  <br/> |
|Élément d'aperçu de recherche de contenu mentionné  <br/> |PreviewItemListed  <br/> |S/O  <br/> |Un utilisateur A cliqué sur **aperçu des résultats** de la recherche pour afficher la page Aperçu des résultats de la recherche, qui répertorie jusqu'à 1000 éléments à partir des résultats d'une recherche de contenu.  <br/> |
|Élément d'aperçu de recherche de contenu affiché  <br/> |PreviewItemRendered  <br/> |S/O  <br/> |Un gestionnaire eDiscovery a affiché un élément en cliquant dessus lors de l'aperçu des résultats de la recherche.  <br/> |
|Recherche de contenu créée  <br/> |SearchCreated  <br/> |New-ComplianceSearch  <br/> |Une nouvelle recherche de contenu a été créée.  <br/> |
|Administrateur eDiscovery créé  <br/> |CaseAdminAdded  <br/> |Add-eDiscoveryCaseAdmin  <br/> |Un utilisateur a été ajouté en tant qu'administrateur de découverte électronique dans l'organisation.  <br/> |
|Création d'un cas eDiscovery  <br/> |CaseAdded  <br/> |New-ComplianceCase  <br/> |Un cas de découverte électronique a été créé. Lors de la création d'un cas, il vous suffit de lui attribuer un nom. D'autres tâches liées à la casse telles que l'ajout de membres, la création de conservations et la création de recherches de contenu associées au cas entraînent la journalisation d'événements supplémentaires.  <br/> |
|Filtre des autorisations de recherche créé  <br/> |SearchPermissionCreated  <br/> |New-ComplianceSecurityFilter  <br/> |Un filtre d'autorisations de recherche a été créé.  <br/> |
|Requête de recherche créée pour la conservation de cas eDiscovery  <br/> |HoldCreated  <br/> |New-CaseHoldRule  <br/> |Une conservation basée sur une requête associée à un cas de découverte électronique a été créée.  <br/> |
|Recherche de contenu supprimé  <br/> |SearchRemoved  <br/> |Remove-ComplianceSearch  <br/> |Une recherche de contenu existante a été supprimée.  <br/> |
|Administrateur eDiscovery supprimé  <br/> |CaseAdminRemoved  <br/> |Remove-eDiscoveryCaseAdmin  <br/> |Un administrateur de découverte électronique a été supprimé de votre organisation.  <br/> |
|Suppression d'un cas eDiscovery  <br/> |CaseRemoved  <br/> |Remove-ComplianceCase  <br/> |Un cas de découverte électronique a été supprimé. Notez que toute conservation associée à la casse doit être supprimée avant de pouvoir supprimer le cas.  <br/> |
|Filtre des autorisations de recherche supprimées  <br/> |SearchPermissionRemoved  <br/> |Remove-ComplianceSecurityFilter  <br/> |Un filtre d'autorisations de recherche a été supprimé.  <br/> |
|Requête de recherche supprimée pour la conservation de cas eDiscovery  <br/> |HoldRemoved  <br/> |Remove-CaseHoldRule  <br/> |Une conservation basée sur une requête associée à un cas de découverte électronique a été supprimée. La suppression de la requête de la suspension est souvent le résultat de la suppression d'une suspension. Lorsqu'une requête de conservation ou de suspension est supprimée, les emplacements de contenu en attente sont libérés.  <br/> |
|Exportation de la recherche de contenu téléchargée  <br/> |SearchExportDownloaded  <br/> |S/O  <br/> |Un utilisateur A téléchargé les résultats d'une recherche de contenu sur son ordinateur local. Notez qu'une **exportation démarrée de l'activité de recherche de contenu** doit être initiée avant de pouvoir télécharger les résultats de la recherche.<br/> |
|Résultats prévisualisés de la recherche de contenu  <br/> |SearchPreviewed  <br/> |S/O  <br/> |Un utilisateur A affiché un aperçu des résultats d'une recherche de contenu.  <br/> |
|Résultats purgés de la recherche de contenu  <br/> |SearchResultsPurged  <br/> |New-ComplianceSearchAction  <br/> |Un utilisateur A purgé les résultats d'une recherche de contenu en exécutant la commande **New-ComplianceSearchAction-purge** .  <br/> |
|Suppression de l'analyse de la recherche de contenu  <br/> |RemovedSearchResultsSentToZoom  <br/> |Remove-ComplianceSearchAction  <br/> |Une action prepare de recherche de contenu (pour préparer les résultats de recherche pour Office 365 Advanced eDiscovery) a été supprimée. Si l'action de préparation était inférieure à deux semaines, les résultats de recherche préparés pour Advanced eDiscovery ont été supprimés de la zone de stockage Microsoft Azure. Si l'action de préparation remonte à plus de 2 semaines, cet événement indique que seule l'action de préparation correspondante a été supprimée.  <br/> |
|Suppression de l'exportation de la recherche de contenu  <br/> |RemovedSearchExported  <br/> |Remove-ComplianceSearchAction  <br/> |Une action d'exportation de recherche de contenu a été supprimée. Si l'action d'exportation était inférieure à deux semaines, les résultats de recherche qui ont été téléchargés dans la zone de stockage Microsoft Azure ont été supprimés. Si l'action d'exportation remonte à plus de 2 semaines, cet événement indique que seule l'action d'exportation correspondante a été supprimée.  <br/> |
|Membre supprimé d'un cas de découverte électronique  <br/> |CaseMemberRemoved  <br/> |Remove-ComplianceCaseMember  <br/> |Un utilisateur a été supprimé en tant que membre d'un cas de découverte électronique.  <br/> |
|Suppression des résultats de la recherche de contenu  <br/> |RemovedSearchPreviewed  <br/> |Remove-ComplianceSearchAction  <br/> |Une action d'aperçu de recherche de contenu a été supprimée.  <br/> |
|Suppression de l'action de purge effectuée lors de la recherche de contenu  <br/> |RemovedSearchResultsPurged  <br/> |Remove-ComplianceSearchAction  <br/> |Une action de purge de recherche de contenu a été supprimée.  <br/> |
|Rapport de recherche supprimé  <br/> |SearchReportRemoved  <br/> |Remove-ComplianceSearchAction  <br/> |Une action de rapport d'exportation de recherche de contenu a été supprimée.  <br/> |
|Début de l'analyse de la recherche de contenu  <br/> |SearchResultsSentToZoom  <br/> |New-ComplianceSearchAction  <br/> |Les résultats d'une recherche de contenu ont été préparés pour analyse dans Advanced eDiscovery.  <br/> |
|Début de la recherche de contenu  <br/> |SearchStarted  <br/> |Start-ComplianceSearch  <br/> |Une recherche de contenu a été démarrée. Lors de la création ou de la modification d'une recherche de &amp; contenu à l'aide de l'interface utilisateur du centre de sécurité conformité, la recherche est démarrée automatiquement. Si vous créez ou modifiez une recherche à l'aide de la cmdlet **New-ComplianceSearch** ou **Set-ComplianceSearch** , vous devez exécuter la cmdlet **Start-ComplianceSearch** pour démarrer la recherche.<br/> |
|Début de l'exportation de la recherche de contenu  <br/> |SearchExported  <br/> |New-ComplianceSearchAction  <br/> |Un utilisateur A exporté les résultats d'une recherche de contenu.  <br/> |
|Début du rapport d'exportation  <br/> |SearchReport  <br/> |New-ComplianceSearchAction  <br/> |Un utilisateur A exporté un rapport de recherche de contenu.  <br/> |
|Recherche de contenu interrompue  <br/> |SearchStopped  <br/> |Stop-ComplianceSearch  <br/> |Un utilisateur a arrêté une recherche de contenu.  <br/> |
  
## <a name="ediscovery-cmdlet-activities"></a>activités de l'applet de commande eDiscovery

Le tableau suivant répertorie les enregistrements du journal d'audit de l'applet de commande enregistrés lorsqu'un administrateur ou un utilisateur effectue une activité de &amp; découverte électronique à l'aide du centre de sécurité conformité ou en exécutant la cmdlet correspondante dans PowerShell à distance connecté au centre de sécurité &amp; conformité de votre organisation. Notez que les informations détaillées dans l'enregistrement du journal d'audit sont différentes pour les activités de cmdlet répertoriées dans ce tableau et les activités eDiscovery décrites dans la section précédente. 
  
Comme indiqué précédemment, les activités de la cmdlet eDiscovery doivent prendre jusqu'à 24 heures pour apparaître dans les résultats de la recherche du journal d'audit.
  
> [!TIP]
> Les cmdlets de la colonne **opération** dans le tableau suivant sont liées à la rubrique d'aide correspondante de la cmdlet sur TechNet. Accédez à la rubrique d'aide de l'applet de commande pour obtenir une description des paramètres disponibles pour chaque cmdlet. Le paramètre et la valeur de paramètre qui ont été utilisés avec une cmdlet sont inclus dans l'entrée du journal d'audit pour chaque activité de cmdlet eDiscovery enregistrée. 
  
|**Nom convivial**|**Opération (cmdlet)**|**Description**|
|:-----|:-----|:-----|
|Blocage créé dans le cas eDiscovery  <br/> |[New-CaseHoldPolicy](https://go.microsoft.com/fwlink/p/?LinkId=823813) <br/> |Une conservation a été créée pour un cas de découverte électronique. Une conservation peut être créée avec ou sans spécification d'une source de contenu. Si des sources de contenu sont spécifiées, elles seront identifiées dans l'entrée du journal d'audit.  <br/> |
|Suppression d'un blocage de découverte électronique  <br/> |[Remove-CaseHoldPolicy](https://go.microsoft.com/fwlink/p/?LinkId=823814) <br/> |Une conservation associée à un cas de découverte électronique a été supprimée. La suppression d'une conservation libère tous les emplacements de contenu de la suspension. La suppression de la conservation entraîne également la suppression des règles de conservation de la casse associées à la conservation (voir **Remove-CaseHoldRule** ci-dessous).<br/> |
|Conservation de blocage modifiée dans la découverte électronique  <br/> |[Set-CaseHoldPolicy](https://go.microsoft.com/fwlink/p/?LinkId=823815) <br/> |Une conservation associée à une découverte électronique a été modifiée. Les modifications possibles incluent l'ajout ou la suppression d'emplacements de contenu ou la désactivation (désactivation) de la conservation.  <br/> |
|Requête de recherche créée pour la conservation de cas eDiscovery  <br/> |[New-CaseHoldRule](https://go.microsoft.com/fwlink/p/?LinkId=823816) <br/> |Une conservation basée sur une requête associée à un cas de découverte électronique a été créée.  <br/> |
|Requête de recherche supprimée pour la conservation de cas eDiscovery  <br/> |[Remove-CaseHoldRule](https://go.microsoft.com/fwlink/p/?LinkId=823820) <br/> |Une conservation basée sur une requête associée à un cas de découverte électronique a été supprimée. La suppression de la requête de la suspension est souvent le résultat de la suppression d'une suspension. Lorsqu'une requête de conservation ou de suspension est supprimée, les emplacements de contenu en attente sont libérés.  <br/> |
|Modification d'une requête de recherche pour la conservation de cas eDiscovery  <br/> |[Set-CaseHoldRule](https://go.microsoft.com/fwlink/p/?LinkId=823819) <br/> |Une conservation basée sur une requête associée à un cas de découverte électronique a été modifiée. Les modifications possibles incluent la modification de la requête ou de la plage de dates pour une conservation basée sur une requête.  <br/> |
|Création d'un cas eDiscovery  <br/> |[New-ComplianceCase](https://go.microsoft.com/fwlink/p/?LinkId=823842) <br/> |Un cas de découverte électronique a été créé. Lors de la création d'un cas, il vous suffit de lui attribuer un nom. D'autres tâches liées à la casse telles que l'ajout de membres, la création de conservations et la création de recherches de contenu associées au cas entraînent la journalisation d'événements supplémentaires.  <br/> |
|Suppression d'un cas eDiscovery  <br/> |[Remove-ComplianceCase](https://go.microsoft.com/fwlink/p/?LinkId=823844) <br/> |Un cas de découverte électronique a été supprimé. Notez que toute conservation associée à la casse doit être supprimée avant de pouvoir supprimer le cas.  <br/> |
|Cas de découverte électronique modifiée  <br/> |[Set-ComplianceCase](https://go.microsoft.com/fwlink/p/?LinkId=823846) <br/> |Un cas de découverte électronique a été modifié. Les modifications incluent la fermeture d'un cas ouvert ou la réouverture d'un cas fermé.  <br/> |
|Ajout d'un membre au cas eDiscovery  <br/> |[Add-ComplianceCaseMember](https://go.microsoft.com/fwlink/p/?LinkId=823848) <br/> |Un utilisateur a été ajouté en tant que membre d'un cas de découverte électronique. En tant que membre d'un cas, un utilisateur peut effectuer différentes tâches liées à la casse selon qu'il a reçu ou non les autorisations nécessaires.  <br/> |
|Membre supprimé d'un cas de découverte électronique  <br/> |[Remove-ComplianceCaseMember](https://go.microsoft.com/fwlink/p/?LinkId=823849) <br/> |Un utilisateur a été supprimé en tant que membre d'un cas de découverte électronique.  <br/> |
|Appartenance au cas de découverte électronique modifiée  <br/> |[Update-ComplianceCaseMember](https://go.microsoft.com/fwlink/p/?LinkId=823850) <br/> |La liste d'appartenance d'un cas de découverte électronique a été modifiée. Cette activité est enregistrée lorsque tous les membres sont remplacés par un groupe de nouveaux utilisateurs. Si un seul membre est ajouté ou supprimé, l'opération **Add-ComplianceCaseMember** ou **Remove-ComplianceCaseMember** est enregistrée.<br/> |
|Recherche de contenu créée  <br/> |[New-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517935) <br/> |Une nouvelle recherche de contenu a été créée.  <br/> |
|Recherche de contenu supprimé  <br/> |[Remove-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517936) <br/> |Une recherche de contenu existante a été supprimée.  <br/> |
|Recherche de contenu modifiée  <br/> |[Set-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517937) <br/> |Une recherche de contenu existante a été modifiée. Les modifications peuvent inclure l'ajout ou la suppression d'emplacements de contenu qui sont recherchés et la modification de la requête de recherche.  <br/> |
|Début de la recherche de contenu  <br/> |[Start-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517938) <br/> |Une recherche de contenu a été démarrée. Lors de la création ou de la modification d'une recherche de &amp; contenu à l'aide de l'interface utilisateur du centre de sécurité conformité, la recherche est démarrée automatiquement. Si vous créez ou modifiez une recherche à l'aide de la cmdlet **New-ComplianceSearch** ou **Set-ComplianceSearch** , vous devez exécuter la cmdlet **Start-ComplianceSearch** pour démarrer la recherche.<br/> |
|Recherche de contenu interrompue  <br/> |[Stop-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517939) <br/> |Une recherche de contenu en cours d'exécution a été arrêtée.  <br/> |
|Action de recherche de contenu créée  <br/> |[New-ComplianceSearchAction](https://go.microsoft.com/fwlink/p/?LinkId=527971) <br/> |Une action de recherche de contenu a été créée. Les actions de recherche de contenu incluent l'aperçu des résultats de recherche, l'exportation des résultats de recherche, la préparation des résultats de recherche pour l'analyse dans Office 365 Advanced eDiscovery et la suppression définitive des éléments qui correspondent aux critères de recherche d'une recherche de contenu.  <br/> |
|Action de recherche de contenu supprimée  <br/> |[Remove-ComplianceSearchAction](https://go.microsoft.com/fwlink/p/?LinkId=824027) <br/> |Une action de recherche de contenu a été supprimée.  <br/> |
|Filtre des autorisations de recherche créé  <br/> |[New-ComplianceSecurityFilter](https://go.microsoft.com/fwlink/p/?LinkId=617542) <br/> |Un filtre d'autorisations de recherche a été créé.  <br/> |
|Filtre des autorisations de recherche supprimées  <br/> |[Remove-ComplianceSecurityFilter](https://go.microsoft.com/fwlink/p/?LinkId=617543) <br/> |Un filtre d'autorisations de recherche a été supprimé.  <br/> |
|Filtre des autorisations de recherche modifié  <br/> |[Set-ComplianceSecurityFilter](https://go.microsoft.com/fwlink/p/?LinkId=617544) <br/> |Un filtre d'autorisations de recherche a été modifié.  <br/> |
|Administrateur eDiscovery créé  <br/> |[Add-eDiscoveryCaseAdmin](https://go.microsoft.com/fwlink/p/?LinkId=798217) <br/> |Un utilisateur a été ajouté en tant qu'administrateur de découverte électronique dans votre organisation.  <br/> |
|Administrateur eDiscovery supprimé  <br/> |[Remove-eDiscoveryCaseAdmin](https://go.microsoft.com/fwlink/p/?LinkId=823945) <br/> |Un administrateur de découverte électronique a été supprimé de votre organisation.  <br/> |
|Appartenance à un administrateur eDiscovery modifiée  <br/> |[Update-eDiscoveryCaseAdmin](https://go.microsoft.com/fwlink/p/?LinkId=823946) <br/> |La liste des administrateurs eDiscovery de votre organisation a été modifiée. Cette activité est enregistrée lorsque la liste des administrateurs eDiscovery est remplacée par un groupe de nouveaux utilisateurs. Si un seul utilisateur est ajouté ou supprimé, l'opération **Add-eDiscoveryCaseAdmin** ou **Remove-eDiscoveryCaseAdmin** est enregistrée.<br/> |
   
## <a name="detailed-properties-for-ediscovery-activities"></a>Propriétés détaillées des activités eDiscovery

Le tableau suivant décrit les propriétés qui sont incluses lorsque vous cliquez sur **informations supplémentaires** sur la page **Détails** d'une activité eDiscovery répertoriée dans les résultats de la recherche. Ces propriétés sont également incluses dans le fichier CSV lorsque vous exportez les résultats de la recherche du journal d'audit. Notez qu'un enregistrement de journal d'audit pour une activité eDiscovery n'inclut pas toutes les propriétés détaillées indiquées ci-dessous. 
  
> [!TIP]
> Lorsque vous exportez les résultats de la recherche, le fichier CSV contient une colonne nommée **détail**, qui contient les propriétés détaillées décrites dans le tableau suivant dans une propriété à valeurs multiples. Vous pouvez utiliser la fonctionnalité Power Query dans Excel pour fractionner cette colonne en plusieurs colonnes afin que chaque propriété dispose de sa propre colonne. Cela vous permettra de trier et de filtrer sur une ou plusieurs de ces propriétés. Pour plus d'informations, reportez-vous à la section «exporter les résultats de la recherche dans un fichier» dans [Search the Audit Log in the Office 365 Security _AMP_ Compliance Center ](search-the-audit-log-in-security-and-compliance.md#step-4-export-the-search-results-to-a-file). 
  
|**Propriété**|**Description**|
|:-----|:-----|
|Cas  <br/> |Identité (GUID) du cas eDiscovery qui a été créé, modifié ou supprimé.  <br/> |
|ClientApplication  <br/> |les activités de l'applet de commande eDiscovery ont une valeur d' **EMC** pour cette propriété. Cela indique que l'activité a été effectuée à l' &amp; aide de l'interface utilisateur du centre de sécurité conformité ou de l'exécution de la cmdlet dans PowerShell.<br/> |
|ClientIP  <br/> |Adresse IP du périphérique qui a été utilisé lors de l'enregistrement de l'activité. L'adresse IP est affichée dans un format d'adresse IPv4 ou IPv6.  <br/> |
|ClientRequestId  <br/> | Pour les activités eDiscovery, cette propriété est généralement vide.  <br/> |
|CmdletVersion  <br/> |Numéro de build de la version du centre de &amp; sécurité conformité en cours d'exécution dans votre organisation.  <br/> |
|CreationTime  <br/> |Date et heure au format UTC (temps universel coordonné) au moment de l'exécution de l'activité eDiscovery.  <br/> |
|EffectiveOrganization  <br/> |Nom de votre organisation Office 365.  <br/> |
|ExchangeLocations  <br/> |Les boîtes aux lettres Exchange Online incluses dans une recherche de contenu ou mises en attente dans un cas eDiscovery.  <br/> |
|Exclusions  <br/> |Emplacements de boîte aux lettres ou de site exclus d'une recherche de contenu ou d'une conservation dans un cas eDiscovery.  <br/> |
|ExtendedProperties  <br/> |Les propriétés supplémentaires d'une recherche de contenu, une action de recherche de contenu ou une conservation dans un cas de découverte électronique, telles que le GUID de l'objet et les paramètres de cmdlet et de cmdlet correspondants qui ont été utilisés lors de l'exécution de l'activité.  <br/> |
|Id  <br/> |ID de l'entrée de rapport. L'ID identifie de manière unique l'entrée du journal d'audit.  <br/> |
|NonPIIParameters  <br/> |Une liste des paramètres (sans aucune valeur) qui ont été utilisés avec la cmdlet identifiée dans la propriété Operation. Les paramètres répertoriés dans cette propriété sont les mêmes que ceux répertoriés dans la propriété paraMeters.  <br/> |
|ObjectId  <br/> |GUID ou nom de l'objet (par exemple, une recherche de contenu ou un cas de découverte électronique) qui a été créé, modifié ou supprimé par l'activité indiquée dans la propriété Operation. Cet objet est également identifié dans la colonne élément dans les résultats de la recherche du journal d'audit.  <br/> |
|ObjectType  <br/> |Type d'objet eDiscovery que l'utilisateur a créé, supprimé ou modifié; par exemple, une action de recherche de contenu (aperçu, exportation ou purge), un cas eDiscovery ou une recherche de contenu.  <br/> |
|Opération  <br/> |Nom de l'opération qui correspond à l'activité eDiscovery effectuée.  <br/> |
|N...  <br/> |GUID de votre organisation Office 365.  <br/> |
|Paramètres  <br/> |Le nom et la valeur des paramètres qui ont été utilisés avec la cmdlet correspondante.  <br/> |
|PublicFolderLocations  <br/> |Emplacements de dossiers publics dans Exchange Online inclus dans une recherche de contenu ou mis en attente dans un cas eDiscovery.  <br/> |
|Requête  <br/> |Requête de recherche associée à l'activité, telle qu'une recherche de contenu ou une conservation basée sur une requête.  <br/> |
|RecordType  <br/> |Type d'opération indiqué par l'enregistrement. La valeur de **18** indique un événement lié à une activité indiquée dans la section activités de l'applet de commande [eDiscovery](#ediscovery-cmdlet-activities) . La valeur **24** indique un événement lié à une activité indiquée dans la section [How to Search for and View eDiscovery Activities](#how-to-search-for-and-view-ediscovery-activities) .<br/> |
|ResultStatus  <br/> |Indique si l'action (spécifiée dans la propriété Operation) a réussi ou non.  <br/> |
|SecurityComplianceCenterEventType  <br/> |Indique que l'activité était un événement &amp; du centre de sécurité conformité. Toutes les activités eDiscovery auront une valeur de **0** pour cette propriété.<br/> |
|SharepointLocations  <br/> |Sites SharePoint Online inclus dans une recherche de contenu ou mis en attente dans un cas de découverte électronique.  <br/> |
|StartTime  <br/> |Date et heure au format UTC (temps universel coordonné) lors du démarrage de l'activité eDiscovery.  <br/> |
|Identifi  <br/> |Utilisateur qui a effectué l'activité (spécifié dans la propriété Operation) qui a entraîné la journalisation de l'enregistrement. Notez que les enregistrements de l'activité eDiscovery effectuée par les comptes système (par exemple, AUTORITE NT\SYSTEM) sont également inclus dans le journal d'audit.  <br/> |
|UserKey  <br/> |Autre ID pour l'utilisateur identifié dans la propriété UserId. Pour les activités eDiscovery, la valeur de cette propriété est généralement identique à celle de la propriété UserId.  <br/> |
|UserServicePlan  <br/> |Abonnement Office 365 utilisé par votre organisation. Pour les activités eDiscovery, cette propriété est généralement vide.  <br/> |
|UserType  <br/> |Type d'utilisateur qui a effectué l'opération. Les valeurs suivantes indiquent le type d'utilisateur.  <br/> 0 utilisateur normal. 2 un administrateur dans votre organisation Office 365. 3 un compte d'administrateur ou de système de centre de connaissances Microsoft. 4 un compte système. 5 une application. 6 un principal de service. |
|Version  <br/> |Indique le numéro de version de l'activité (identifiée par la propriété Operation) qui est enregistrée.  <br/> |
|Charge de travail  <br/> |Service Office 365 où l'activité s'est produite. Pour les activités eDiscovery, la valeur est **SecurityComplianceCenter**.<br/> |
