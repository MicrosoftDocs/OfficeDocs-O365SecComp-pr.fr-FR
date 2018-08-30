---
title: Gérer la gouvernance des données dans Office 365
ms.author: stephow
author: stephow-msft
manager: laurawi
ms.date: 5/9/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 48064107-fed2-4db0-9e5c-aa5ddd5ccb09
description: La gouvernance des données est axé sur la sécurisation de vos données autour lorsque vous avez besoin et l’obtention de la supprimer lorsque vous n’avez pas. Avec la gouvernance de données dans Office 365, vous pouvez gérer le cycle de vie complète de contenu, d’importation et le stockage des données au début, à la création de stratégies de fidélisation et puis supprimer définitivement le contenu à la fin.
ms.openlocfilehash: ca3443c3b90a067bf171ddf89be604d262a7b9a4
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528620"
---
# <a name="manage-data-governance-in-office-365"></a>Gérer la gouvernance des données dans Office 365

La gouvernance des données est axé sur la sécurisation de vos données autour lorsque vous avez besoin et l’obtention de la supprimer lorsque vous n’avez pas. Avec la gouvernance de données dans Office 365, vous pouvez gérer le cycle de vie complète de contenu, d’importation et le stockage des données au début, à la création de stratégies de fidélisation et puis supprimer définitivement le contenu à la fin.
  
## <a name="import"></a>Importer

Certains de vos données peuvent être stockées dans des lieux le nuage, tels que des serveurs locaux ou dans les applications tierces. Le service d’importation facilite intégrer votre messagerie, SharePoint et OneDrive pour les données métiers dans Office 365, en téléchargeant directement sur le réseau ou un lecteur chiffré de livraison nous. Vous pouvez également utiliser la fonctionnalité d’importation intelligente dans le service d’importation pour filtrer les éléments dans les fichiers PST sont réellement importées pour les boîtes aux lettres cible. 
  
- [Vue d’ensemble de l’importation de fichiers PST vers Office 365](https://support.office.com/article/ba688e0a-0fcb-4bd7-8e57-2b669564ea84)
    
- [Utiliser le chargement réseau pour importer des fichiers PST vers Office 365](use-network-upload-to-import-pst-files.md)
    
- [Utiliser l’expédition de disque pour importer des fichiers PST dans Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md)
    
- [Utiliser l’outil de Collection PST pour rechercher, copier et supprimer des fichiers PST dans votre organisation](find-copy-and-delete-pst-files-in-your-organization.md)
    
- [Filtrer les données lors de l’importation des fichiers PST vers Office 365](filter-data-when-importing-pst-files.md)
    
- [Chargement de contenu local vers SharePoint Online à l’aide des cmdlets PowerShell](https://support.office.com/article/555049c6-15ef-45a6-9a1f-a1ef673b867c)
    
## <a name="govern-i-store-data"></a>Régir i : stocker des données

Une fois que vous importez des données, vous devrez peut-être augmenter l’espace de stockage. La fonctionnalité d’archivage illimitée dans Office 365 (appelée développer automatiquement l’archivage) fournit un nombre illimité de stockage de boîtes aux lettres d’archive.
  
- [Activer des boîtes aux lettres d’archive de sécurité Office 365 &amp; centre de conformité](enable-archive-mailboxes.md)

- [Vue d’ensemble de l’archivage illimité dans Office 365](unlimited-archiving.md)
    
- [Activer l’archivage illimité dans Office 365](enable-unlimited-archiving.md)
    

    
## <a name="govern-ii-create-policies-and-labels-to-retain-content"></a>Régir II : Créer des stratégies et des étiquettes de conserver le contenu

Une stratégie de rétention vous aide à vous conformer proactive réglementations et stratégies internes en s’assurant que vous conserverez le contenu en tant que mais n’est plus nécessaire à celle. Une stratégie de rétention unique peut couvrir toute votre organisation. En outre, vous pouvez utiliser des étiquettes pour implémenter un plan de fichiers en la classification des données au sein de votre organisation pour la gouvernance et puis en appliquant les règles de rétention en fonction de cette catégorie.
  
- [Vue d’ensemble des stratégies de rétention](retention-policies.md)
    
- [Vue d’ensemble des étiquettes](labels.md)
    
- [En bloc créer et publier des étiquettes à l’aide de PowerShell](https://support.office.com/article/8986701b-ffa1-46ec-8fd0-8f7e81d5b25f.aspx)
    
- [Vue d’ensemble des révisions de destruction](disposition-reviews.md)
    
- [Vue d’ensemble de rétention pilotée par événements](event-driven-retention.md)
    
## <a name="govern-iii-retain-the-email-of-former-employees"></a>Régir III : Conserver l’adresse de messagerie d’anciens employés

Lorsqu’une personne quitte votre organisation, vous pouvez conserver leur messagerie électronique en créant une boîte aux lettres inactive. Une boîte aux lettres devienne inactive lorsqu’un litige, stratégie de rétention d’Office 365, ou autre type de suspension est appliquée, et le compte d’utilisateur Office 365 correspondant est alors supprimé. Éléments d’une boîte aux lettres inactive sont conservés pendant la durée de la stratégie de blocage ou de rétention qui a été placée dans la boîte aux lettres avant qu’il a été inactif.
  
- [Vue d’ensemble des boîtes aux lettres inactives dans Office 365](inactive-mailboxes-in-office-365.md)
    
- [Créer et gérer des boîtes aux lettres inactives dans Office 365](create-and-manage-inactive-mailboxes.md)

- [Modifier la durée d’attente pour une boîte aux lettres inactive dans Office 365](change-the-hold-duration-for-an-inactive-mailbox.md)
  
- [Récupérer une boîte aux lettres inactive dans Office 365](recover-an-inactive-mailbox.md)
 
- [Restaurer une boîte aux lettres inactive dans Office 365](restore-an-inactive-mailbox.md)

- [Supprimer une boîte aux lettres inactive dans Office 365](delete-an-inactive-mailbox.md)

## <a name="monitor"></a>Surveiller

Surveillance vous permet de définir des stratégies de capturer les e-mails et communications partie 3 rd dans votre organisation examinés par des réviseurs internes ou externes. Relecteurs ensuite classer ces communications, vérifier si qu'elles sont compatibles avec les stratégies de votre organisation et transformer en matière suspect si nécessaire.
  
Vous pouvez également utiliser les rapports de la gouvernance des données et l’Explorateur d’activité étiquette à surveiller que les étiquettes sont appliqués au contenu comme vous le souhaitez.
  
- [Configurer des stratégies de surveillance pour votre organisation](configure-supervision-policies.md)
    
- [Rapports de surveillance](supervision-reports.md)
    
- [Afficher l’activité étiquette pour les documents](view-label-activity-for-documents.md)
    
- [Afficher les rapports de la gouvernance des données](view-the-data-governance-reports.md)
    
## <a name="more-information"></a>Plus d'informations

- [Regardez des vidéos de l’équipe de gouvernance de données Microsoft](https://go.microsoft.com/fwlink/?linkid=867039)
    
- [Regarder une vue d’ensemble de la gouvernance des données dans Office 365](https://go.microsoft.com/fwlink/?linkid=852644)
    
- [Sécurité Office 365 &amp; applets de commande de centre de conformité](https://go.microsoft.com/fwlink/?linkid=852310)
    

