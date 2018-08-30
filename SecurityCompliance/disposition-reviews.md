---
title: Vue d’ensemble des révisions de destruction
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: d0c6095b-bfee-4906-a2c7-89c2d7f411c1
description: Lorsque vous créez une étiquette qui conserve le contenu dans Office 365, vous pouvez choisir de déclencher une révision destruction à la fin de la période de rétention.
ms.openlocfilehash: c0a2933f597c9b314ac4ce2e72de9619fac90082
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "23013718"
---
# <a name="overview-of-disposition-reviews"></a><span data-ttu-id="2dbee-103">Vue d’ensemble des révisions de destruction</span><span class="sxs-lookup"><span data-stu-id="2dbee-103">Overview of disposition reviews</span></span>

<span data-ttu-id="2dbee-p101">Lorsque le contenu atteint la fin de sa période de rétention, il existe plusieurs raisons pourquoi vous souhaiterez peut-être réviser ce contenu pour déterminer si elle peut être supprimé en toute sécurité (« supprimée »). Par exemple, vous devrez peut-être :</span><span class="sxs-lookup"><span data-stu-id="2dbee-p101">When content reaches the end of its retention period, there are several reasons why you might want to review that content to decide whether it can be safely deleted ("disposed"). For example, you might need to:</span></span>
  
- <span data-ttu-id="2dbee-106">Suspendre la suppression (« disposition ») du contenu pertinent en cas de litige ou d’audit.</span><span class="sxs-lookup"><span data-stu-id="2dbee-106">Suspend the deletion ("disposition") of relevant content in the event of litigation or an audit.</span></span>
    
- <span data-ttu-id="2dbee-107">Supprimer le contenu de la liste de destruction à stocker dans une archive, si ce contenu a la recherche ou la valeur historique.</span><span class="sxs-lookup"><span data-stu-id="2dbee-107">Remove content from the disposition list to store in an archive, if that content has research or historical value.</span></span>
    
- <span data-ttu-id="2dbee-108">Affecter une période de rétention différentes au contenu, si la stratégie d’origine était une solution temporaire ou provisoire.</span><span class="sxs-lookup"><span data-stu-id="2dbee-108">Assign a different retention period to the content, if the original policy was a temporary or provisional solution.</span></span>
    
- <span data-ttu-id="2dbee-109">Renvoyer le contenu à des clients ou transférer vers une autre organisation.</span><span class="sxs-lookup"><span data-stu-id="2dbee-109">Return the content to clients or transfer it to another organization.</span></span>
    
<span data-ttu-id="2dbee-p102">Lorsque vous créez une étiquette qui conserve le contenu dans Office 365, vous pouvez choisir de déclencher une révision destruction à la fin de la période de rétention. Dans un examen de la disposition :</span><span class="sxs-lookup"><span data-stu-id="2dbee-p102">When you create a label that retains content in Office 365, you can choose to trigger a disposition review at the end of the retention period. In a disposition review:</span></span>
  
- <span data-ttu-id="2dbee-p103">Les personnes que vous choisissez recevoir une notification par courrier électronique qu’ils possèdent pour passer en revue le contenu. Ces relecteurs peuvent être des utilisateurs individuels, de distribution ou de groupes de sécurité ou de groupes d’Office 365. Notez que les notifications sont envoyées une fois par semaine.</span><span class="sxs-lookup"><span data-stu-id="2dbee-p103">The people you choose receive an email notification that they have content to review. These reviewers can be individual users, distribution or security groups, or Office 365 groups. Note that notifications are sent on a weekly basis.</span></span>
    
- <span data-ttu-id="2dbee-115">Relecteurs accédez à la page de **Disposition** de la sécurité &amp; centre de conformité pour consulter le contenu.</span><span class="sxs-lookup"><span data-stu-id="2dbee-115">The reviewers go to the **Disposition** page in the Security &amp; Compliance Center to review the content.</span></span> 
    
- <span data-ttu-id="2dbee-116">Pour chaque document, le réviseur peut :</span><span class="sxs-lookup"><span data-stu-id="2dbee-116">For each document, the reviewer can:</span></span>
    
  - <span data-ttu-id="2dbee-117">Appliquer une étiquette différente.</span><span class="sxs-lookup"><span data-stu-id="2dbee-117">Apply a different label.</span></span>
    
  - <span data-ttu-id="2dbee-118">Étendre sa période de rétention.</span><span class="sxs-lookup"><span data-stu-id="2dbee-118">Extend its retention period.</span></span>
    
  - <span data-ttu-id="2dbee-119">Supprimer définitivement.</span><span class="sxs-lookup"><span data-stu-id="2dbee-119">Permanently delete it.</span></span>
    
- <span data-ttu-id="2dbee-120">Relecteurs peuvent afficher les problèmes en attente ou historiques et exporter la liste dans un fichier .csv.</span><span class="sxs-lookup"><span data-stu-id="2dbee-120">Reviewers can view either pending or historical dispositions, and export that list as a .csv file.</span></span>
    
<span data-ttu-id="2dbee-121">Notez que le destruction avis nécessitent un abonnement à Office 365 entreprise E5.</span><span class="sxs-lookup"><span data-stu-id="2dbee-121">Note that disposition reviews require an Office 365 Enterprise E5 subscription.</span></span>
  
<span data-ttu-id="2dbee-p104">Un examen de disposition peut inclure le contenu dans les boîtes aux lettres Exchange, les sites SharePoint, OneDrive comptes et groupes d’Office 365. En attente d’un examen de destruction dans les emplacements de contenu est supprimé uniquement après qu’un réviseur choisit de supprimer définitivement le contenu.</span><span class="sxs-lookup"><span data-stu-id="2dbee-p104">A disposition review can include content in Exchange mailboxes, SharePoint sites, OneDrive accounts, and Office 365 groups. Content awaiting a disposition review in those locations is deleted only after a reviewer chooses to permanently delete the content.</span></span>
  
![Page de disposition](media/b7436fb2-1f35-4146-8ca2-32c9d10f7e09.png)
  
## <a name="setting-up-the-disposition-review-by-creating-a-label"></a><span data-ttu-id="2dbee-125">La configuration de la révision de disposition en créant une étiquette</span><span class="sxs-lookup"><span data-stu-id="2dbee-125">Setting up the disposition review by creating a label</span></span>

<span data-ttu-id="2dbee-p105">Il s’agit du flux de travail pour configurer un examen de la disposition. Notez que ce flux présente une étiquette publié et appliquée manuellement par un utilisateur ; une étiquette qui déclenche un examen de disposition peut également être appliquée automatiquement au contenu.</span><span class="sxs-lookup"><span data-stu-id="2dbee-p105">This is the basic workflow for setting up a disposition review. Note that this flow shows a label being published and then manually applied by a user; alternatively, a label that triggers a disposition review can be auto-applied to content.</span></span>
  
![Graphique montrant le flux du fonctionne de destruction](media/5fb3f33a-cb53-468c-becc-6dda0ec52778.png)
  
<span data-ttu-id="2dbee-p106">Un examen de la disposition est une option lorsque vous créez une étiquette dans Office 365. Notez que cette option n’est pas disponible dans une stratégie de rétention, mais uniquement dans une étiquette avec les paramètres de rétention.</span><span class="sxs-lookup"><span data-stu-id="2dbee-p106">A disposition review is an option when you create a label in Office 365. Note that this option is not available in a retention policy but only in a label with retention settings.</span></span>
  
<span data-ttu-id="2dbee-131">Pour plus d’informations sur les étiquettes, voir [vue d’ensemble des étiquettes](labels.md).</span><span class="sxs-lookup"><span data-stu-id="2dbee-131">For more information about labels, see [Overview of labels](labels.md).</span></span>
  
![Paramètres de rétention pour une étiquette](media/a16dd202-8862-40ac-80ff-6fee974de5da.png)
  
## <a name="disposing-content"></a><span data-ttu-id="2dbee-133">Suppression du contenu</span><span class="sxs-lookup"><span data-stu-id="2dbee-133">Disposing content</span></span>

<span data-ttu-id="2dbee-p107">Lorsqu’un réviseur est averti par courrier électronique que le contenu est prêt passer en revue, ils peuvent accéder à la page de **Disposition** dans la sécurité &amp; centre de conformité et sélectionnez un ou plusieurs éléments. Le réviseur peut ensuite :</span><span class="sxs-lookup"><span data-stu-id="2dbee-p107">When a reviewer is notified by email that content is ready to review, they can go to the **Disposition** page in the Security &amp; Compliance Center and select one or more items. The reviewer can then:</span></span> 
  
- <span data-ttu-id="2dbee-136">Appliquer une étiquette différente.</span><span class="sxs-lookup"><span data-stu-id="2dbee-136">Apply a different label.</span></span>
    
- <span data-ttu-id="2dbee-137">Étendre la période de rétention.</span><span class="sxs-lookup"><span data-stu-id="2dbee-137">Extend the retention period.</span></span>
    
- <span data-ttu-id="2dbee-138">Supprimer définitivement l’élément.</span><span class="sxs-lookup"><span data-stu-id="2dbee-138">Permanently delete the item.</span></span>
    
<span data-ttu-id="2dbee-p108">Un réviseur peut utiliser le lien pour afficher le document dans son emplacement d’origine, si le réviseur dispose des autorisations à cet emplacement. Lors d’une révision de destruction, le contenu déplace jamais à partir de son emplacement d’origine, et il n’est jamais supprimé jusqu'à ce que le réviseur choisit de le faire.</span><span class="sxs-lookup"><span data-stu-id="2dbee-p108">A reviewer can use the link to view the document in its original location, if the reviewer has permissions for that location. During a disposition review, the content never moves from its original location, and it's never deleted until the reviewer chooses to do so.</span></span>
  
<span data-ttu-id="2dbee-p109">Notez que les notifications par courrier électronique sont automatiquement envoyées aux réviseurs une fois par semaine. Par conséquent, lorsque le contenu atteint la fin de sa période de rétention, il peut prendre jusqu'à sept jours pour les réviseurs recevoir la notification par courrier électronique que le contenu est en attente de destruction.</span><span class="sxs-lookup"><span data-stu-id="2dbee-p109">Note that the email notifications are sent automatically to reviewers on a weekly basis. Therefore, when content reaches the end of its retention period, it may take up to seven days for reviewers to receive the email notification that content is awaiting disposition.</span></span>
  
<span data-ttu-id="2dbee-p110">Notez également que toutes les actions de destruction auditées. Pour ce faire, vous devez activer l’audit au moins un jour avant la première action de destruction - pour plus d’informations, voir [recherche dans le journal d’audit de sécurité Office 365 &amp; centre de conformité](search-the-audit-log-in-security-and-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="2dbee-p110">Also note that all disposition actions are audited. To ensure this, you must turn on auditing at least one day prior to the first disposition action - for more information, see [Search the audit log in the Office 365 Security &amp; Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span></span> 
  
![Options de disposition d’un document](media/771630fd-a9b0-47cf-983b-fe85eb4cdafd.png)
  
## <a name="permissions-for-disposition"></a><span data-ttu-id="2dbee-146">Autorisations pour la disposition</span><span class="sxs-lookup"><span data-stu-id="2dbee-146">Permissions for disposition</span></span>

<span data-ttu-id="2dbee-p111">Pour accéder à la page de **Disposition** , relecteurs doivent être membres du rôle **Gestion de la Disposition** et le rôle **Journaux d’Audit en affichage seul** . Nous vous recommandons de créer un nouveau groupe de rôle appelé relecteurs de destruction, en ajoutant ces deux rôles à ce groupe de rôles et puis ajouter des membres au groupe de rôles.</span><span class="sxs-lookup"><span data-stu-id="2dbee-p111">To get access to the **Disposition** page, reviewers must be members of the **Disposition Management** role and the **View-Only Audit Logs** role. We recommend creating a new role group called Disposition Reviewers, adding these two roles to that role group, and then adding members to the role group.</span></span> 
  
<span data-ttu-id="2dbee-149">Pour plus d’informations, voir [donner aux utilisateurs l’accès à l’Office 365 Security &amp; centre de conformité](grant-access-to-the-security-and-compliance-center.md)</span><span class="sxs-lookup"><span data-stu-id="2dbee-149">For more information, see [Give users access to the Office 365 Security &amp; Compliance Center](grant-access-to-the-security-and-compliance-center.md)</span></span>
  
## <a name="how-long-until-disposed-content-is-permanently-deleted"></a><span data-ttu-id="2dbee-150">Combien de temps jusqu'à ce que le contenu supprimé est définitivement supprimé.</span><span class="sxs-lookup"><span data-stu-id="2dbee-150">How long until disposed content is permanently deleted</span></span>

<span data-ttu-id="2dbee-p112">En attente d’un examen de la disposition de contenu est supprimé uniquement après qu’un réviseur choisit de supprimer définitivement le contenu. Lorsque le réviseur choisit cette option, le contenu dans le site SharePoint ou le compte de OneDrive devient éligible pour le processus de nettoyage standard décrit dans cette section : [fonctionne d’une stratégie de rétention avec contenu sur place](retention-policies.md#how-a-retention-policy-works-with-content-in-place).</span><span class="sxs-lookup"><span data-stu-id="2dbee-p112">Content awaiting a disposition review is deleted only after a reviewer chooses to permanently delete the content. When the reviewer chooses this option, the content in the SharePoint site or OneDrive account becomes eligible for the standard cleanup process described in this section: [How a retention policy works with content in place](retention-policies.md#how-a-retention-policy-works-with-content-in-place).</span></span>
  
<span data-ttu-id="2dbee-153">Cela signifie que :</span><span class="sxs-lookup"><span data-stu-id="2dbee-153">This means that:</span></span>
  
- <span data-ttu-id="2dbee-p113">Le contenu dans une bibliothèque de documents sera déplacé vers la première phase Corbeille **dans les 7 jours** de destruction et puis définitivement supprimés **93 jours** après. La Corbeille n’est pas indexée par la recherche et par conséquent, son contenu n’est pas disponible pour un blocage eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="2dbee-p113">Content in a document library will be moved to the first-stage Recycle Bin **within 7 days** of disposition, and then permanently deleted **93 days** after that. The Recycle Bin is not indexed by search and therefore its contents are not available to an eDiscovery hold.</span></span> 
    
- <span data-ttu-id="2dbee-156">Le contenu de la conservation permanente bibliothèque seront définitivement supprimés **dans les 7 jours** de disposition.</span><span class="sxs-lookup"><span data-stu-id="2dbee-156">Content in the Preservation Hold library will be permanently deleted **within 7 days** of disposition.</span></span> 
    
## <a name="view-pending-and-completed-dispositions"></a><span data-ttu-id="2dbee-157">Afficher en attente et dispositions terminées</span><span class="sxs-lookup"><span data-stu-id="2dbee-157">View pending and completed dispositions</span></span>

<span data-ttu-id="2dbee-158">Dans la page de **Disposition** de la sécurité &amp; centre de conformité, vous pouvez afficher les problèmes en attente et terminées :</span><span class="sxs-lookup"><span data-stu-id="2dbee-158">On the **Disposition** page of the Security &amp; Compliance Center, you can view both pending and completed dispositions:</span></span> 
  
- <span data-ttu-id="2dbee-p114">Dispositions **en attente** ont atteint la fin de leur période de rétention et nécessitent un examen de la disposition. Après avoir examiné chaque élément, décidez si vous voulez lui appliquer une étiquette différente, d’étendre sa période de rétention ou le supprimer définitivement.</span><span class="sxs-lookup"><span data-stu-id="2dbee-p114">**Pending** dispositions have reached the end of their retention period and require a disposition review. After reviewing each item, decide if you want to apply a different label to it, extend its retention period, or permanently delete it.</span></span> 
    
- <span data-ttu-id="2dbee-p115">Dispositions **terminé** ont été approuvées pour la suppression au cours d’un examen de la disposition et sont en cours de suppression définitive. Éléments qui avaient un libellé différent appliqué ou leur période de rétention étendue comme partie d’un examen ne s’affiche ici.</span><span class="sxs-lookup"><span data-stu-id="2dbee-p115">**Completed** dispositions were approved for deletion during a disposition review and are now in the process of being permanently deleted. Items that had a different label applied or their retention period extended as part of a review won't appear here.</span></span> 
    
### <a name="filter-the-disposition-views"></a><span data-ttu-id="2dbee-163">Filtrer les affichages de destruction</span><span class="sxs-lookup"><span data-stu-id="2dbee-163">Filter the disposition views</span></span>

<span data-ttu-id="2dbee-p116">Vous pouvez filtrer ces affichages par étiquette ou la plage horaire. Pour en attente de dispositions, la plage de temps est basée sur la date d’expiration. Pour les problèmes historiques, la plage de temps est basée sur la date de suppression.</span><span class="sxs-lookup"><span data-stu-id="2dbee-p116">You can filter these views by label or time range. For pending dispositions, the time range is based on the expiry date. For historical dispositions, the time range is based on the deletion date.</span></span>
  
![Options de filtre sur la page de Disposition](media/8682a9f5-a77d-45ae-b902-8418a3ebbea1.png)
  
### <a name="export-the-disposition-items"></a><span data-ttu-id="2dbee-168">Exporter les éléments de disposition</span><span class="sxs-lookup"><span data-stu-id="2dbee-168">Export the disposition items</span></span>

<span data-ttu-id="2dbee-169">En outre, vous pouvez exporter les éléments de l’affichage dans un fichier .csv que vous pouvez ouvrir dans Excel.</span><span class="sxs-lookup"><span data-stu-id="2dbee-169">In addition, you can export the items in either view as a .csv file that you can open in Excel.</span></span>
  
![Destruction exporté les données dans Excel](media/08e3bc09-b132-47b4-a051-a590b697e725.png)
  

