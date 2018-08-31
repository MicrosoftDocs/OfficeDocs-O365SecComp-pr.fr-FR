---
title: Vue d’ensemble des boîtes aux lettres inactives dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/1/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 1fbd74e8-7a60-4157-afe8-fe79f05d2038
description: Découvrez la conservation de contenu de la boîte aux lettres pour les anciens employés en activant la boîte aux lettres dans une boîte aux lettres inactive. Pour cela, en plaçant la boîte aux lettres en conservation pour litige ou appliquer une stratégie de rétention Office 365 pour la boîte aux lettres puis supprimer le compte Office 365 correspondant.
ms.openlocfilehash: 5b421e32df99a10d13528fe7a75e6a0e8fb54fdc
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528173"
---
# <a name="overview-of-inactive-mailboxes-in-office-365"></a>Vue d’ensemble des boîtes aux lettres inactives dans Office 365

Votre organisation devront conserver e-mail de vos employés ancien avoir quitté l’organisation. Selon les exigences de rétention de votre organisation, vous devrez peut-être conserver le contenu de la boîte aux lettres pour quelques mois ou années après la fin de l’emploi ou vous devrez peut-être conserver indéfiniment le contenu de la boîte aux lettres. Quelle que soit la durée, vous devez conserver le courrier électronique, vous pouvez créer des boîtes aux lettres inactives dans Office 365 pour conserver la boîte aux lettres d’anciens employés. 
  
## <a name="what-are-inactive-mailboxes"></a>Que sont les boîtes aux lettres inactives ?

Lorsqu’un employé quitte l’organisation (ou accède un congé étendue), vous pouvez supprimer leur compte Office 365. Données de boîte aux lettres de l’employé sont conservées pendant 30 jours après que le compte est supprimé. Pendant cette période, vous pouvez toujours récupérer les données de boîtes aux lettres par le compte d’annulation de la suppression. Après 30 jours, les données sont définitivement supprimées.
  
Mais si votre organisation doit conserver le contenu de la boîte aux lettres pour les anciens employés, vous pouvez désactiver la boîte aux lettres dans une boîte aux lettres inactive en plaçant la boîte aux lettres en conservation pour litige ou en appliquant une stratégie de rétention d’Office 365 à la boîte aux lettres de sécurité Office 365 &amp; Centre de conformité, puis en supprimant le compte Office 365 correspondant. Le contenu d’une boîte aux lettres inactive est conservé pendant la durée de la litige placés dans la boîte aux lettres ou de la période de rétention de la stratégie de rétention Office 365 appliquée avant la suppression de la boîte aux lettres. Vous pouvez récupérer le compte d’utilisateur correspondant pour une période de 30 jours. Toutefois, après 30 jours, la boîte aux lettres inactive est conservé dans Office 365 jusqu'à ce que la stratégie de blocage ou de rétention est supprimée. 
  
**IMPORTANT :** Nous avons différée le délai de 1 juillet 2017 pour la création des archives permanentes pour désactiver une boîte aux lettres. Mais cette année ou le début d’année, vous ne pourrez créer des archives permanentes dans Exchange Online. À ce moment, stratégies de rétention pour litige contient et Office 365 peuvent servir à créer une boîte aux lettres inactive. Cependant, les boîtes aux lettres inactives existants qui se trouvent sur In-Place Hold seront toujours être prise en charge et vous pouvez continuer à gérer les boîtes aux lettres inactives conserve In-Place. Cela inclut la modification de la durée d’an In-Place Hold et supprimer définitivement une boîte aux lettres inactive en supprimant la In-Place Hold. 
 
  
## <a name="inactive-mailboxes-and-office-365-retention-policies"></a>Boîtes aux lettres inactives et stratégies de rétention Office 365

En plus de litige, à l’aide de la nouvelle fonctionnalité de stratégie de rétention Office 365 dans la sécurité &amp; centre de conformité est une autre manière de désactiver une boîte aux lettres. Pour utiliser une stratégie de rétention pour rendre une boîte aux lettres inactive : 
  
- La stratégie doit être appliquée aux boîtes aux lettres Exchange ou aux emplacements Skype Entreprise (car le contenu associé à Skype est stocké dans la boîte aux lettres de l'utilisateur). 
    
- Elle doit être configurée pour conserver le contenu ou le conserver pour le supprimer ensuite. Si une stratégie de rétention est configurée uniquement pour supprimer le contenu, la boîte aux lettres concernée par la stratégie ne devient pas inactive après suppression de la boîte aux lettres.
    
- Elle peut reposer sur une requête pour conserver uniquement les éléments correspondant à une requête de recherche. 
    
Pour en savoir plus sur la configuration des stratégies de rétention Office 365, consultez la rubrique [Vue d'ensemble des stratégies de rétention](retention-policies.md).
  
Si vous utilisez une stratégie de rétention Office 365 pour rendre une boîte aux lettres inactive, Office 365 continue de traiter la stratégie de rétention sur la boîte aux lettres inactive. En d'autres termes, si la stratégie de rétention est configurée pour conserver puis supprimer le contenu, les éléments sont déplacés vers le dossier Éléments récupérables à l'expiration de la durée de conservation avant d'être supprimés de la boîte aux lettres inactive. Si la stratégie de rétention Office 365 n'est pas configurée pour supprimer des éléments, les éléments qui n'ont pas été supprimés définitivement par l'utilisateur (avant que la boîte aux lettres soit devenue inactive) ne sont pas déplacés vers le dossier Éléments récupérables et sont conservés indéfiniment dès que la boîte aux lettres devient inactive. 
  
Vous pouvez envisager de créer une stratégie de rétention Office 365 destinée aux boîtes aux lettres inactives. Voici quelques bonnes raisons pour le faire et quelques éléments à garder à l'esprit.
  
- Vous pouvez configurer la stratégie de rétention pour conserver le contenu de la boîte aux lettres uniquement le temps de répondre aux exigences de votre organisation concernant les anciens employés.
    
- Il est un moyen facile pour identifier les boîtes aux lettres inactives, car la stratégie de rétention ne sera appliquée aux boîtes aux lettres inactives.
    
- Vous serez en mesure d’identifier facilement la stratégie de rétention qui est affectée à des boîtes aux lettres inactives dans votre organisation. Cela permettra plus facile de modifier les paramètres de rétention (ou suppression) si nécessaire. Il sera également rendre plus facile de supprimer définitivement une boîte aux lettres inactive, car vous pouvez seulement supprimer à partir de la stratégie à l’aide de la sécurité &amp; centre de conformité. Dans le cas contraire, vous devez utiliser Exchange Online PowerShell pour supprimer un litige à partir d’une boîte aux lettres inactive ou utiliser la sécurité &amp; PowerShell du centre de conformité pour exclure une boîte aux lettres inactive d’une stratégie de rétention d’Office 365 à l’échelle de l’organisation.
    
- Si vous créez une stratégie de rétention Office 365 spécialement pour les boîtes aux lettres inactives, vous pouvez ajouter un nombre maximal de 1 000 boîtes aux lettres à la stratégie. Si vous êtes une organisation de très grande taille, vous devrez peut-être créer plusieurs stratégies de rétention Office 365 pour les utiliser avec les boîtes aux lettres inactives.
  
## <a name="inactive-mailboxes-and-ediscovery-case-holds"></a>Boîtes aux lettres inactives et conservations eDiscovery

Si une suspension associé à un cas de découverte électronique dans la sécurité &amp; centre de conformité est placé sur une boîte aux lettres, puis la boîte aux lettres ou le compte d’utilisateur Office 365 est supprimé, la boîte aux lettres devient une boîte aux lettres inactive. Nous ne recommandons cependant à l’aide de cas de découverte électronique conserve pour désactiver une boîte aux lettres. C’est parce que cas eDiscovery sont destinés aux cas liés au temps spécifiques liées à un problème juridique. Dans certains cas, une affaire juridique se termine sans doute et la suspension associée au cas sera supprimée et le cas de découverte électronique sera fermé. En fait, si une suspension est placée sur une boîte aux lettres inactive est associée à un cas eDiscovery, puis le blocage est terminé ou de la découverte électronique cas est fermé (ou supprimé), la boîte aux lettres inactive est définitivement supprimé. En outre, vous ne pouvez pas créer une suspension eDiscovery basé sur le temps. Qui est contenu dans une boîte aux lettres inactive est conservé indéfiniment ou jusqu'à ce que le blocage est supprimé et la boîte aux lettres inactive est supprimé. Par conséquent, nous recommandons d’utiliser un litige ou une stratégie de rétention Office 365 pour les boîtes aux lettres inactives.
  
Pour plus d’informations sur les cas eDiscovery et blocages, voir [cas eDiscovery de sécurité Office 365 &amp; centre de conformité](ediscovery-cases.md).
  
## <a name="inactive-mailboxes-and-office-365-labels"></a>Boîtes aux lettres inactives et étiquettes Office 365

Les étiquettes dans Office 365 vous permettent de classer les données de messagerie de votre organisation à des fins de gouvernance et d'appliquer des règles de rétention à partir de cette classification. Une étiquette peut être appliquée à un élément de messagerie, soit manuellement par les utilisateurs, soit automatiquement par les administrateurs. De plus, une seule étiquette peut être appliquée à un élément de messagerie. Si une étiquette est appliquée à un seul élément de messagerie de la boîte aux lettres d'un utilisateur et que la boîte aux lettres ou le compte d'utilisateur Office 365 est supprimé, la boîte aux lettres devient inactive. Tout comme les conservations de cas eDiscovery, nous vous déconseillons d'utiliser les étiquettes pour rendre une boîte aux lettres inactive. Nous vous recommandons plutôt d'utiliser une conservation pour litige ou une stratégie de rétention Office 365. Dans le cas des étiquettes, si vous ne voyez pas qu'une étiquette a été appliquée à un élément de messagerie, vous risqueriez de rendre une boîte aux lettres inactive à la suppression du compte d'utilisateur. 
  
Pour en savoir plus sur les étiquettes, consultez la rubrique [Vue d'ensemble des étiquettes](labels.md).
  
## <a name="inactive-mailboxes-and-exchange-mrm-retention-policies"></a>Boîtes aux lettres inactives et stratégies de rétention Exchange MRM

Si une stratégie de rétention Exchange (la fonctionnalité Gestion des enregistrements de messagerie ou MRM, dans Exchange Online) a été appliquée à la boîte aux lettres lorsqu’il a été effectué inactif, toutes les stratégies de suppression (qui sont configurés avec une action de rétention **Supprimer** les balises de rétention) sera continuent d’être traitées dans la boîte aux lettres inactive. Cela signifie que les éléments marqués avec une stratégie de suppression seront déplacées vers le dossier éléments récupérables lors de la période de rétention. Ces éléments sont supprimés de la boîte aux lettres inactive lorsque la durée d’attente expire. Si une durée d’attente n’est pas spécifiée pour la boîte aux lettres inactive, les éléments dans le dossier de récupérer les éléments doivent être conservés indéfiniment. 
  
À l'inverse, les stratégies d'archivage (qui correspondent à des balises de rétention configurées avec une action de rétention **MoveToArchive**) incluses dans la stratégie de rétention attribuée à une boîte aux lettres inactive sont ignorées. Autrement dit, les éléments d'une boîte aux lettres inactive marqués avec une stratégie d'archivage resteront dans la boîte aux lettres principale à l'expiration de la période de rétention. Ils ne sont pas déplacés vers la boîte aux lettres d'archivage ni vers le dossier Éléments récupérables dans la boîte aux lettres d'archivage. Ils seront conservés indéfiniment. 
  
## <a name="creating-an-inactive-mailbox"></a>Création d'une boîte aux lettres inactive

Pour désactiver une boîte aux lettres, il doit être attribué une licence Exchange Online (Plan 2) afin qu’une stratégie de rétention litige ou Office 365 peut être appliquée à la boîte aux lettres avant d’être supprimé. Une fois que la boîte aux lettres est supprimée, la licence Exchange Online qui a été associée à celle-ci sera disponible à affecter à un nouvel utilisateur. Boîtes aux lettres inactives ne nécessitent pas de licences en cours.
  
Le tableau suivant résume le processus de fabrication d’une boîte aux lettres inactive pour les scénarios de rétention différentes. Pour plus d’informations, voir [Gérer les boîtes aux lettres inactives dans Office 365](create-and-manage-inactive-mailboxes.md).
  
|**Pour...**|**Vous devez…**|**Résultat**|
|:-----|:-----|:-----|
|Conserver le contenu de la boîte aux lettres indéfiniment après le départ d'un employé de l'organisation  <br/> | Appliquer une conservation pour litige ou une stratégie de rétention Office 365 à la boîte aux lettres.  <br/>  Éviter d'indiquer une durée pour la conservation pour litige ou de configurer la stratégie de rétention Office 365 pour supprimer des éléments. Utilisez plutôt une stratégie de rétention qui conserve les éléments indéfiniment.  <br/>  Supprimez le compte Office 365 de l'utilisateur.  <br/> |Dans la boîte aux lettres inactive, y compris les éléments dans le dossier éléments récupérables, tout le contenu est conservé indéfiniment.  <br/> |
|Conserver le contenu de la boîte aux lettres pendant une période donnée après le départ d'un employé de l'organisation et le supprimer  <br/> | Appliquer une stratégie de rétention d’Office 365 pour la boîte aux lettres.  <br/>  Configurer la stratégie de rétention pour conserver les supprimer puis des éléments lors de la période de rétention.  <br/>  Supprimez le compte Office 365 de l'utilisateur.  <br/> |L’expiration de la période de rétention pour un élément de boîte aux lettres, l’élément est déplacé vers le dossier éléments récupérables, puis il est définitivement supprimé de (définitivement) de la boîte aux lettres inactive l’expiration de la période de rétention des éléments supprimés (pour les boîtes aux lettres Exchange). La période de rétention de la stratégie de rétention Office 365 peut être configurée en fonction de la date d’origine un élément de boîte aux lettres a été reçu ou créé ou lorsqu’il a été modifié.  <br/> |
   
**Remarque :** Si un litige se trouve déjà dans une boîte aux lettres, ou si une stratégie de rétention Office 365 est déjà fait, il vous est supprimer le compte d’utilisateur Office 365 correspondant pour créer une boîte aux lettres inactive. 
  
## <a name="managing-inactive-mailboxes"></a>Gestion des boîtes aux lettres inactives

Une fois que la boîte aux lettres est inactive, vous pouvez effectuer différentes tâches de gestion.
  
- **Modifier la durée d’attente pour une boîte aux lettres inactive** Après une boîte aux lettres inactive, vous pouvez modifier la durée de la suspension de la stratégie de rétention litige ou Office 365 appliquée à la boîte aux lettres inactive. Pour connaître les procédures, voir [Modifier la durée d’attente pour une boîte aux lettres inactive dans Office 365](change-the-hold-duration-for-an-inactive-mailbox.md).
    
- **Récupérer une boîte aux lettres inactive** Si un ancien employé (ou un employé sur un congé) renvoie à votre organisation, ou si un nouvel employé à effectuer sur les responsabilités de l’ancien employé, vous pouvez récupérer le contenu de la boîte aux lettres inactive. Lorsque vous récupérez une boîte aux lettres inactive, la boîte aux lettres est converti en une nouvelle boîte aux lettres, le contenu et la structure de dossiers de la boîte aux lettres inactive sont conservés, et la boîte aux lettres est liée à un nouveau compte d’utilisateur. Une fois qu’il est récupéré, la boîte aux lettres inactive n’existe plus. Pour plus d’informations sur ce qui se produit lorsque vous récupérez une boîte aux lettres inactive et les procédures pas à pas, consultez la rubrique [récupérer une boîte aux lettres inactive dans Office 365](recover-an-inactive-mailbox.md).
    
- **Restaurer une boîte aux lettres inactive** Si un autre employé prend en charge les responsabilités d’un ancien employé, ou si une autre personne doit avoir accès au contenu de la boîte aux lettres inactive, vous pouvez restaurer (ou fusionner) le contenu de la boîte aux lettres inactive dans une boîte aux lettres existante. Lorsque vous restaurez une boîte aux lettres inactive, le contenu est copié dans une autre boîte aux lettres. La boîte aux lettres inactive est conservée et reste une boîte aux lettres inactive. La boîte aux lettres inactive toujours pouvant être recherchée à l’aide des outils de découverte électronique, son contenu peut être restauré à une autre boîte aux lettres, et peuvent être récupéré ou supprimé à une date ultérieure. Pour connaître les procédures, voir [restaurer une boîte aux lettres inactive dans Office 365](restore-an-inactive-mailbox.md).
    
- **Supprimer une boîte aux lettres inactive** Lorsque vous n’avez plus besoin de conserver le contenu d’une boîte aux lettres inactive, vous pouvez le supprimer définitivement en supprimant toutes les suspensions ou Office 365 les stratégies de rétention appliquées à la boîte aux lettres inactive. Si une boîte aux lettres a été effectuée inactif plus de 30 jours auparavant, il sera marqué pour suppression définitive après la suppression de la suspension. Si la boîte aux lettres a été effectué inactif dans au cours des 30 derniers jours, vous pouvez le rendre actif après la suppression de la stratégie de blocage ou de rétention. Pour connaître les procédures, voir [suppression d’une boîte aux lettres inactive dans Office 365](delete-an-inactive-mailbox.md).