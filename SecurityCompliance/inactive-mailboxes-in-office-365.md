---
title: Vue d'ensemble des boîtes aux lettres inactives dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/1/2018
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 1fbd74e8-7a60-4157-afe8-fe79f05d2038
description: Découvrez comment conserver le contenu des boîtes aux lettres des anciens employés en transformant la boîte aux lettres en boîte aux lettres inactive. Pour ce faire, vous pouvez placer la boîte aux lettres en conservation pour litige ou appliquer une stratégie de rétention Office 365 à la boîte aux lettres, puis supprimer le compte Office 365 correspondant.
ms.openlocfilehash: 12688cb1c0f1d165c21736ce5a6130245db36a06
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2019
ms.locfileid: "31000797"
---
# <a name="overview-of-inactive-mailboxes-in-office-365"></a>Vue d'ensemble des boîtes aux lettres inactives dans Office 365

Votre organisation peut avoir besoin de conserver le courrier électronique des anciens employés après leur départ. En fonction des exigences de rétention de votre organisation, il se peut que vous deviez conserver le contenu de la boîte aux lettres pendant quelques mois ou quelques années après la fin du contrat, ou indéfiniment. Quelle que soit la durée de conservation du courrier électronique, vous pouvez créer des boîtes aux lettres inactives dans Office 365 pour conserver la boîte aux lettres des anciens employés. 
  
## <a name="what-are-inactive-mailboxes"></a>Que sont les boîtes aux lettres inactives ?

Lorsqu'un employé quitte votre organisation (ou passe à un congé prolongé), vous pouvez supprimer son compte Office 365. Les données de boîte aux lettres de l'employé sont conservées pendant 30 jours après la suppression du compte. Pendant cette période, vous pouvez toujours récupérer les données de boîte aux lettres en désupprimant le compte. Après 30 jours, les données sont définitivement supprimées.
  
Toutefois, si votre organisation doit conserver le contenu des boîtes aux lettres des anciens employés, vous pouvez transformer la boîte aux lettres en boîte aux lettres inactive en plaçant la boîte aux lettres en conservation pour litige ou en appliquant une stratégie de rétention Office 365 à la boîte aux lettres dans le centre de sécurité & Compliance Center puis en supprimant le compte Office 365 correspondant. The contents of an inactive mailbox are retained for the duration of the Litigation Hold placed on the mailbox or the retention period of the Office 365 retention policy applied to it before the mailbox was deleted. You can still recover the corresponding user account for a 30-day period. Toutefois, après 30 jours, la boîte aux lettres inactive est conservée dans Office 365 jusqu'à ce que la stratégie de conservation ou de rétention soit supprimée. 
  
**Important:** Nous avons différé le 1er juillet 2017 l'échéance de la création de nouvelles conservations inactives pour désactiver une boîte aux lettres. But later this year or early next year, you won't be able to create new In-Place Holds in Exchange Online. À ce stade, seuls les stratégies de conservation pour litige et Office 365 peuvent être utilisées pour créer une boîte aux lettres inactive. Toutefois, les boîtes aux lettres inactives existantes qui sont en conservation inaltérable sont toujours prises en charge, et vous pouvez continuer à gérer les conservations inactives sur les boîtes aux lettres inactives. Cela inclut le changement de la durée d'une conservation inaltérable et la suppression définitive d'une boîte aux lettres inactive en supprimant la conservation inaltérable. 
 
  
## <a name="inactive-mailboxes-and-office-365-retention-policies"></a>Boîtes aux lettres inactives et stratégies de rétention Office 365

En plus de la mise en attente pour litige, l'utilisation de la nouvelle fonctionnalité de stratégie de rétention Office 365 dans le centre de sécurité & Compliance Center est une autre façon de désactiver une boîte aux lettres. To use a retention policy to make an inactive mailbox: 
  
- La stratégie doit être appliquée aux boîtes aux lettres Exchange ou aux emplacements Skype Entreprise (car le contenu associé à Skype est stocké dans la boîte aux lettres de l'utilisateur). 
    
- Elle doit être configurée pour conserver le contenu ou le conserver pour le supprimer ensuite. Si une stratégie de rétention est configurée uniquement pour supprimer le contenu, la boîte aux lettres concernée par la stratégie ne devient pas inactive après suppression de la boîte aux lettres.
    
- Elle peut reposer sur une requête pour conserver uniquement les éléments correspondant à une requête de recherche. 
    
Pour en savoir plus sur la configuration des stratégies de rétention Office 365, consultez la rubrique [Vue d'ensemble des stratégies de rétention](retention-policies.md).
  
Si vous utilisez une stratégie de rétention Office 365 pour rendre une boîte aux lettres inactive, Office 365 continue de traiter la stratégie de rétention sur la boîte aux lettres inactive. En d'autres termes, si la stratégie de rétention est configurée pour conserver puis supprimer le contenu, les éléments sont déplacés vers le dossier Éléments récupérables à l'expiration de la durée de conservation avant d'être supprimés de la boîte aux lettres inactive. Si la stratégie de rétention Office 365 n'est pas configurée pour supprimer des éléments, les éléments qui n'ont pas été supprimés définitivement par l'utilisateur (avant que la boîte aux lettres soit devenue inactive) ne sont pas déplacés vers le dossier Éléments récupérables et sont conservés indéfiniment dès que la boîte aux lettres devient inactive. 
  
Vous pouvez envisager de créer une stratégie de rétention Office 365 destinée aux boîtes aux lettres inactives. Voici quelques bonnes raisons pour le faire et quelques éléments à garder à l'esprit.
  
- Vous pouvez configurer la stratégie de rétention pour conserver le contenu de la boîte aux lettres uniquement le temps de répondre aux exigences de votre organisation concernant les anciens employés.
    
- Il s'agit d'un moyen facile d'identifier les boîtes aux lettres inactives, car la stratégie de rétention ne sera appliquée qu'aux boîtes aux lettres inactives.
    
- You'll be able to easily identify the retention policy that's assigned to inactive mailboxes in your organization. This will make it easier to change the retention (or deletion) settings if necessary. Il facilite également la suppression définitive d'une boîte aux lettres inactive car vous pouvez simplement la supprimer de la stratégie à l'aide du centre de sécurité & Compliance Center. Dans le cas contraire, vous devez utiliser Exchange Online PowerShell pour supprimer une suspension pour litige d'une boîte aux lettres inactive ou utiliser le centre de sécurité & Compliance Center PowerShell pour exclure une boîte aux lettres inactive d'une stratégie de rétention Office 365 à l'échelle de l'organisation.
    
- Si vous créez une stratégie de rétention Office 365 spécialement pour les boîtes aux lettres inactives, vous pouvez ajouter un nombre maximal de 1 000 boîtes aux lettres à la stratégie. Si vous êtes une organisation de très grande taille, vous devrez peut-être créer plusieurs stratégies de rétention Office 365 pour les utiliser avec les boîtes aux lettres inactives.
  
## <a name="inactive-mailboxes-and-ediscovery-case-holds"></a>Boîtes aux lettres inactives et conservations eDiscovery

Si une conservation associée à un cas de découverte électronique dans le centre de sécurité & Compliance Center est placée sur une boîte aux lettres et que la boîte aux lettres ou le compte Office 365 de l'utilisateur est supprimé, la boîte aux lettres devient une boîte aux lettres inactive. However, we don't recommend using eDiscovery case holds to make a mailbox inactive. That's because eDiscovery cases are intended for specific, time-bound cases related to a legal issue. At some point, a legal case will probably end and the holds associated with the case will be removed and the eDiscovery case will be closed. In fact, if a hold that's placed on an inactive mailbox is associated with an eDiscovery case, and then the hold is released or the eDiscovery case is closed (or deleted), the inactive mailbox will be permanently deleted. Additionally, you can't create a time-based eDiscovery hold. That's means content in an inactive mailbox will be retained forever or until the hold is removed and the inactive mailbox is deleted. Therefore, we recommend using a Litigation Hold or an Office 365 retention policy for inactive mailboxes.
  
Pour plus d'informations sur les cas de découverte électronique et les conservations, consultez la rubrique [cas eDiscovery](ediscovery-cases.md).
  
## <a name="inactive-mailboxes-and-office-365-labels"></a>Boîtes aux lettres inactives et étiquettes Office 365

Les étiquettes dans Office 365 vous permettent de classer les données de messagerie de votre organisation à des fins de gouvernance et d'appliquer des règles de rétention à partir de cette classification. Une étiquette peut être appliquée à un élément de messagerie, soit manuellement par les utilisateurs, soit automatiquement par les administrateurs. De plus, une seule étiquette peut être appliquée à un élément de messagerie. Si une étiquette est appliquée à un seul élément de messagerie de la boîte aux lettres d'un utilisateur et que la boîte aux lettres ou le compte d'utilisateur Office 365 est supprimé, la boîte aux lettres devient inactive. Tout comme les conservations de cas eDiscovery, nous vous déconseillons d'utiliser les étiquettes pour rendre une boîte aux lettres inactive. Nous vous recommandons plutôt d'utiliser une conservation pour litige ou une stratégie de rétention Office 365. Dans le cas des étiquettes, si vous ne voyez pas qu'une étiquette a été appliquée à un élément de messagerie, vous risqueriez de rendre une boîte aux lettres inactive à la suppression du compte d'utilisateur. 
  
Pour en savoir plus sur les étiquettes, consultez la rubrique [Vue d'ensemble des étiquettes](labels.md).
  
## <a name="inactive-mailboxes-and-exchange-mrm-retention-policies"></a>Boîtes aux lettres inactives et stratégies de rétention Exchange MRM

Si une stratégie de rétention Exchange (fonctionnalité de gestion des enregistrements de messagerie ou MRM dans Exchange Online) a été appliquée à la boîte aux lettres lorsqu'elle était devenue inactive, toutes les stratégies de suppression (qui sont des balises de rétention configurées avec une action de rétention de **suppression** ) seront continuent d'être traitées sur la boîte aux lettres inactive. En d'autres termes, les éléments marqués avec une stratégie de suppression seront déplacés vers le dossier Éléments récupérables à l'expiration de la période de rétention. Ces éléments sont supprimés définitivement de la boîte aux lettres inactive à l'expiration de la durée de la conservation. Si aucune durée de conservation n'est spécifiée pour la boîte aux lettres inactive, les éléments du dossier Éléments récupérables seront conservés indéfiniment. 
  
À l'inverse, les stratégies d'archivage (qui correspondent à des balises de rétention configurées avec une action de rétention **MoveToArchive**) incluses dans la stratégie de rétention attribuée à une boîte aux lettres inactive sont ignorées. Autrement dit, les éléments d'une boîte aux lettres inactive marqués avec une stratégie d'archivage resteront dans la boîte aux lettres principale à l'expiration de la période de rétention. Ils ne sont pas déplacés vers la boîte aux lettres d'archivage ni vers le dossier Éléments récupérables dans la boîte aux lettres d'archivage. Ils seront conservés indéfiniment. 
  
## <a name="creating-an-inactive-mailbox"></a>Création d’une boîte aux lettres inactive

Pour qu'une boîte aux lettres devienne inactive, elle doit disposer d'une licence Exchange Online (Plan 2) afin qu'une conservation pour litige ou une stratégie de rétention Office 365 lui soit attribuée avant sa suppression. Une fois la boîte aux lettres supprimée, la licence Exchange Online qui lui était associée pourra être affectée à un nouvel utilisateur. Les boîtes aux lettres inactives ne requièrent pas de licences en cours.
  
Le tableau suivant résume le processus de création d'une boîte aux lettres inactive pour différents scénarios de rétention. Pour plus d'informations, consultez la rubrique [gestion des boîtes aux lettres inactives dans Office 365](create-and-manage-inactive-mailboxes.md).
  
|**Pour...**|**Vous devez…**|**Résultat**|
|:-----|:-----|:-----|
|Conserver le contenu de la boîte aux lettres indéfiniment après le départ d'un employé de l'organisation  <br/> | Appliquer une conservation pour litige ou une stratégie de rétention Office 365 à la boîte aux lettres.  <br/>  Éviter d'indiquer une durée pour la conservation pour litige ou de configurer la stratégie de rétention Office 365 pour supprimer des éléments. Utilisez plutôt une stratégie de rétention qui conserve les éléments indéfiniment.  <br/>  Supprimez le compte Office 365 de l'utilisateur.  <br/> |Tout le contenu de la boîte aux lettres inactive, y compris les éléments du dossier éléments récupérables, est conservé indéfiniment.  <br/> |
|Conserver le contenu de la boîte aux lettres pendant une période donnée après le départ d'un employé de l'organisation et le supprimer  <br/> | Appliquer une stratégie de rétention Office 365 à la boîte aux lettres.  <br/>  ConFigurez la stratégie de rétention pour conserver, puis supprimer les éléments à l'expiration de la période de rétention.  <br/>  Supprimez le compte Office 365 de l'utilisateur.  <br/> |Lorsque la période de rétention d'un élément de boîte aux lettres expire, l'élément est déplacé vers le dossier éléments récupérables, puis supprimé définitivement (purgé) de la boîte aux lettres inactive lors de l'expiration de la période de rétention des éléments supprimés (pour les boîtes aux lettres Exchange). La période de rétention de la stratégie de rétention Office 365 peut être configurée en fonction de la date d'origine à laquelle un élément de boîte aux lettres a été reçu ou créé, ou lors de sa dernière modification.  <br/> |
   
**Remarque:** Si une mise en attente pour litige est déjà placée sur une boîte aux lettres, ou si une stratégie de rétention Office 365 est déjà appliquée, il vous suffit de supprimer le compte d'utilisateur Office 365 correspondant pour créer une boîte aux lettres inactive. 
  
## <a name="managing-inactive-mailboxes"></a>Gestion des boîtes aux lettres inactives

Une fois que la boîte aux lettres est inactive, vous pouvez effectuer différentes tâches de gestion.
  
- **Modifier la durée de la conservation pour une boîte aux lettres inactive** Lorsqu'une boîte aux lettres devient inactive, vous pouvez modifier la durée de la conservation pour litige ou de la stratégie de rétention Office 365 appliquée à la boîte aux lettres inactive. Pour obtenir des procédures pas à pas, consultez [la rubrique modifier la durée de la conservation pour une boîte aux lettres inactive dans Office 365](change-the-hold-duration-for-an-inactive-mailbox.md).
    
- **Récupérer une boîte aux lettres inactive** Si un ancien employé (ou un employé en congé) réintègre votre organisation, ou si un nouvel employé est embauché pour assumer les responsabilités de l'ancien employé, vous pouvez récupérer le contenu de la boîte aux lettres inactive. Lorsque vous récupérez une boîte aux lettres inactive, la boîte aux lettres est convertie en une nouvelle boîte aux lettres, le contenu et la structure de dossiers de la boîte aux lettres inactive sont conservés, et la boîte aux lettres est liée à un nouveau compte d'utilisateur. Une fois récupérée, la boîte aux lettres inactive n'existe plus. Pour obtenir des procédures pas à pas et des informations sur ce qui se produit lorsque vous récupérez une boîte aux lettres inactive, consultez la rubrique [récupérer une boîte aux lettres inactive dans Office 365](recover-an-inactive-mailbox.md).
    
- **Restaurer une boîte aux lettres inactive** Si un autre employé assume les responsabilités de l'ancien employé, ou si un autre utilisateur doit accéder au contenu de la boîte aux lettres inactive, vous pouvez restaurer (ou fusionner) le contenu de la boîte aux lettres inactive vers une boîte aux lettres existante. Lorsque vous restaurez une boîte aux lettres inactive, le contenu est copié vers une autre boîte aux lettres. La boîte aux lettres inactive est conservée et reste inactive. La boîte aux lettres inactive peut toujours faire l'objet d'une recherche à l'aide des outils eDiscovery, son contenu peut être restauré vers une autre boîte aux lettres et il peut être récupéré ou supprimé ultérieurement. Pour obtenir des procédures pas à pas, reportez-vous à la rubrique [restaurer une boîte aux lettres inactive dans Office 365](restore-an-inactive-mailbox.md).
    
- **Supprimer une boîte aux lettres inactive** Si vous n'avez plus besoin du contenu d'une boîte aux lettres inactive, vous pouvez la supprimer définitivement en retirant toutes les conservations ou les stratégies de rétention Office 365 appliquées à la boîte aux lettres inactive. Si une boîte aux lettres est devenue inactive depuis plus de 30 jours, elle est marquée pour suppression définitive après la suppression de la conservation. Si la boîte aux lettres est devenue inactive au cours des 30 derniers jours, vous pouvez la restaurer après avoir supprimé la conservation ou la stratégie de rétention. Pour obtenir des procédures pas à pas, consultez la rubrique [supprimer une boîte aux lettres inactive dans Office 365](delete-an-inactive-mailbox.md).