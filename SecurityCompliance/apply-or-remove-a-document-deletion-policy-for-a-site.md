---
title: Application ou suppression d’une stratégie de suppression de documents pour un site
ms.author: stephow
author: stephow-msft
manager: laurawi
ms.date: 6/29/2018
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- MET150
ms.assetid: e3e92668-f9b2-46ee-8e5e-c623870588b6
description: Les organisations sont souvent soumises à des réglementations de conformité, juridiques ou autres qui les obligent à conserver des documents pendant une certaine période de temps. Toutefois, conserver des documents plus longtemps que nécessaire peut exposer l’organisation à un risque juridique. Pour cette raison, votre organisation peut avoir créé une stratégie de suppression de documents pour votre site (par exemple, il se pourrait que les documents commerciaux généraux doivent être supprimés cinq ans après leur création).
ms.openlocfilehash: c826d6c9e163e79c4e72510e3362328ae902c80c
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34152286"
---
# <a name="apply-or-remove-a-document-deletion-policy-for-a-site"></a><span data-ttu-id="3bd44-105">Application ou suppression d’une stratégie de suppression de documents pour un site</span><span class="sxs-lookup"><span data-stu-id="3bd44-105">Apply or remove a document deletion policy for a site</span></span>

<span data-ttu-id="3bd44-p102">Les organisations sont souvent soumises à des réglementations de conformité, juridiques ou autres qui les obligent à conserver des documents pendant une certaine période de temps. Toutefois, conserver des documents plus longtemps que nécessaire peut exposer l’organisation à un risque juridique. Pour cette raison, votre organisation peut avoir créé une stratégie de suppression de documents pour votre site (par exemple, il se pourrait que les documents commerciaux généraux doivent être supprimés cinq ans après leur création).</span><span class="sxs-lookup"><span data-stu-id="3bd44-p102">Organizations are often subject to compliance, legal, or other regulations that require them to retain documents for a certain period of time. However, retaining documents for longer than required can expose the organization to legal risk. For this reason, your organization may have created a document deletion policy for your site — for example, general business documents might be required to be deleted five years after they were created.</span></span>
  
<span data-ttu-id="3bd44-109">Selon votre organisation, une stratégie de suppression de documents peut être :</span><span class="sxs-lookup"><span data-stu-id="3bd44-109">Depending on your organization, a document deletion policy might be:</span></span>
  
- <span data-ttu-id="3bd44-110">**Obligatoire** Un propriétaire de site ne peut pas désactiver une stratégie obligatoire, qui est automatiquement appliquée au site.</span><span class="sxs-lookup"><span data-stu-id="3bd44-110">**Mandatory** A site owner can't opt out of a mandatory policy, which is automatically applied to the site.</span></span> 
    
- <span data-ttu-id="3bd44-111">**Par défaut** Une stratégie par défaut est automatiquement appliquée à un site, mais un propriétaire de site peut :</span><span class="sxs-lookup"><span data-stu-id="3bd44-111">**Default** A default policy is automatically applied to a site, but a site owner can:</span></span> 
    
  - <span data-ttu-id="3bd44-112">choisir une autre stratégie, le cas échéant ;</span><span class="sxs-lookup"><span data-stu-id="3bd44-112">Choose another policy if available.</span></span>
    
  - <span data-ttu-id="3bd44-113">refuser complètement la stratégie si elle n’est pas pertinente pour le contenu du site.</span><span class="sxs-lookup"><span data-stu-id="3bd44-113">Opt out of the policy entirely if it is not relevant to the content in the site.</span></span>
    
- <span data-ttu-id="3bd44-114">**Ni obligatoire ni par défaut** Dans ce cas, aucune stratégie n’est appliquée automatiquement au site, et le propriétaire du site doit prendre des mesures pour en appliquer une.</span><span class="sxs-lookup"><span data-stu-id="3bd44-114">**Neither mandatory nor default** In this case, no policy is automatically applied to the site, and the site owner needs to take action to apply one.</span></span> 
    
<span data-ttu-id="3bd44-p103">Une stratégie de suppression de documents peut contenir plusieurs règles (par exemple, une règle peut exiger la suppression des documents un an après leur création, mais une autre règle peut exiger la suppression des documents un an après leur dernière modification). Si une stratégie contient plusieurs règles, vous pouvez sélectionner la règle qui s’applique le mieux à votre site. La règle de suppression s’appliquera à toutes les bibliothèques du site. Une seule stratégie et une seule règle peuvent être actives simultanément dans un site. À l’instar d’une stratégie, une règle peut être définie comme règle par défaut, afin d’être appliquée automatiquement lorsque la stratégie est appliquée.</span><span class="sxs-lookup"><span data-stu-id="3bd44-p103">A document deletion policy may contain more than one rule — for example, one rule might say delete documents one year after they were created, but another rule might say delete documents one year after they were last modified. If a policy contains more than one rule, you can select the rule that best applies to your site. The delete rule will be applied to all libraries within the site. Only one policy and one rule can be active in a site at one time. Like a policy, a rule can be set as default, so that it is applied automatically when the policy is applied.</span></span>
  
<span data-ttu-id="3bd44-p104">Enfin, les stratégies de suppression de documents sont héritées. Lorsque vous sélectionnez une stratégie ou une règle pour votre site, cette sélection est héritée par tous les sous-sites, bien que le propriétaire d’un sous-site puisse annuler l’héritage en sélectionnant une stratégie ou une règle différente. Lorsque vous sélectionnez une stratégie ou une règle, tenez compte du contenu des sous-sites sous votre site.</span><span class="sxs-lookup"><span data-stu-id="3bd44-p104">Finally, document deletion policies are inherited. When you select a policy or rule for your site, that selection is inherited by all subsites, although an owner of a subsite can break inheritance by selecting a different policy or rule. When you select a policy or rule, consider the content of any subsites below your site.</span></span>
  
## <a name="view-the-document-deletion-policies-available-in-a-site-collection"></a><span data-ttu-id="3bd44-123">Affichage des stratégies de suppression de documents disponibles dans une collection de sites</span><span class="sxs-lookup"><span data-stu-id="3bd44-123">View the document deletion policies available in a site collection</span></span>

<span data-ttu-id="3bd44-p105">Votre organisation peut affecter des stratégies différentes à des collections de sites différentes. Au niveau de la collection de sites, le propriétaire d’une collection de sites peut afficher toutes les stratégies de suppression de documents disponibles pour cette collection de sites. Les stratégies peuvent avoir été mises à la disposition du modèle de collection de sites (et donc de toutes les collections de sites créées à partir de ce modèle) ou de cette collection de sites spécifique.</span><span class="sxs-lookup"><span data-stu-id="3bd44-p105">Your organization may assign different policies to different site collections. At the site collection level, an owner of a site collection can view all of the document deletion policies that are available to that site collection. The policies may have been made available to the site collection template (and therefore all site collections created from this template) or to this specific site collection.</span></span>
  
1. <span data-ttu-id="3bd44-127">Dans le site de niveau supérieur de la collection de sites, dans le coin supérieur droit, sélectionnez **paramètres** [icône d’engrenage \> ] **paramètres de site**.</span><span class="sxs-lookup"><span data-stu-id="3bd44-127">In the top-level site in the site collection, in the upper-right corner, choose **Settings** [gear icon] \> **Site Settings**.</span></span>
    
2. <span data-ttu-id="3bd44-128">Sous **stratégies de suppression de documents**d’administration \> de la collection de **sites** .</span><span class="sxs-lookup"><span data-stu-id="3bd44-128">Under **Site Collection Administration** \> **Document Deletion Policies**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="3bd44-129">Le lien **stratégies de suppression de documents** ne s’affiche pas, sauf si des stratégies ont été affectées à la collection de sites.</span><span class="sxs-lookup"><span data-stu-id="3bd44-129">The **Document Deletion Policies** link won't appear unless policies have been assigned to the site collection.</span></span> <span data-ttu-id="3bd44-130">De plus, le lien ne s’affiche pas immédiatement après que des stratégies ont été affectées au site; le lien des stratégies de **Suppression de documents** peut prendre jusqu’à 24 heures.</span><span class="sxs-lookup"><span data-stu-id="3bd44-130">Also, the link doesn't appear immediately after policies have been assigned to the site — it can take up to 24 hours from when the policies are assigned to when the **Document Deletion Policies** link appears.</span></span> 
  
3. <span data-ttu-id="3bd44-131">Cette page permet d’afficher :</span><span class="sxs-lookup"><span data-stu-id="3bd44-131">On this page you can view:</span></span>
    
  - <span data-ttu-id="3bd44-p107">les stratégies actuellement affectées et les règles associées. Sélectionnez une stratégie pour afficher les règles dans le volet de droite.</span><span class="sxs-lookup"><span data-stu-id="3bd44-p107">The currently assigned policies and the associated rules. Select a policy to view the rules in the right pane.</span></span>
    
  - <span data-ttu-id="3bd44-134">La stratégie par défaut, le cas échéant, affiche **Oui** dans la colonne **Par défaut**.</span><span class="sxs-lookup"><span data-stu-id="3bd44-134">The default policy, if any, displays **Yes** in the **Default** column.</span></span> 
    
  - <span data-ttu-id="3bd44-135">Un message s’affiche sous la liste si la stratégie a été affectée comme **Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="3bd44-135">A message is displayed below the list if the policy has been assigned as **Mandatory**.</span></span>
    
<span data-ttu-id="3bd44-p108">Cette liste est en affichage uniquement, pour que le propriétaire de la collection de sites visualise toutes les stratégies et les règles disponibles. Pour appliquer une stratégie, consultez la section suivante.</span><span class="sxs-lookup"><span data-stu-id="3bd44-p108">This list is view only, for the site collection owner to see all of the available policies and rules. To apply a policy, see the next section.</span></span>
  
![Affichage des stratégies de suppression de documents affectées à une collection de sites](media/f2c0433b-2bb5-407d-a364-ae07c9627176.png)
  
## <a name="apply-or-remove-a-document-deletion-policy-for-a-site"></a><span data-ttu-id="3bd44-139">Application ou suppression d’une stratégie de suppression de documents pour un site</span><span class="sxs-lookup"><span data-stu-id="3bd44-139">Apply or remove a document deletion policy for a site</span></span>

<span data-ttu-id="3bd44-140">En tant que propriétaire de site ou propriétaire de collection de sites, votre organisation peut avoir créé des stratégies que vous pouvez appliquer à votre site ou refuser complètement.</span><span class="sxs-lookup"><span data-stu-id="3bd44-140">As a site owner or site collection owner, your organization may have created policies that you can either apply to your site or opt out of entirely.</span></span>
  
1. <span data-ttu-id="3bd44-141">Dans le coin supérieur droit, sélectionnez paramètres \*\*\*\* du \> **site**paramètres [icône d’engrenage].</span><span class="sxs-lookup"><span data-stu-id="3bd44-141">In the upper-right corner, choose **Settings** [gear icon] \> **Site Settings**.</span></span>
    
2. <span data-ttu-id="3bd44-142">Sous **stratégies de suppression de documents**d’administration \> du **site** .</span><span class="sxs-lookup"><span data-stu-id="3bd44-142">Under **Site Administration** \> **Document Deletion Policies**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="3bd44-143">Le lien **stratégies de suppression de documents** ne s’affiche pas, sauf si des stratégies ont été affectées à la collection de sites.</span><span class="sxs-lookup"><span data-stu-id="3bd44-143">The **Document Deletion Policies** link won't appear unless policies have been assigned to the site collection.</span></span> <span data-ttu-id="3bd44-144">De plus, le lien ne s’affiche pas immédiatement après que des stratégies ont été affectées au site; le lien des stratégies de **Suppression de documents** peut prendre jusqu’à 24 heures.</span><span class="sxs-lookup"><span data-stu-id="3bd44-144">Also, the link doesn't appear immediately after policies have been assigned to the site — it can take up to 24 hours from when the policies are assigned to when the **Document Deletion Policies** link appears.</span></span> 
  
3. <span data-ttu-id="3bd44-145">Effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="3bd44-145">Do one of the following:</span></span>
    
  - <span data-ttu-id="3bd44-146">**Pour appliquer une stratégie** Sélectionnez une stratégie \> sélectionnez une règle dans l' \> **enregistrement**de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="3bd44-146">**To apply a policy** Select a policy \> select a rule in that policy \> **Save**.</span></span>
    
    <span data-ttu-id="3bd44-p110">Une seule stratégie et une seule règle peuvent être actives simultanément dans un site. Votre organisation peut fournir plusieurs stratégies et règles à choisir, ou une seule stratégie ou règle.</span><span class="sxs-lookup"><span data-stu-id="3bd44-p110">Only one policy and one rule can be active in a site at one time. Your organization may provide several policies and rules to choose from, or only one policy or rule.</span></span>
    
    ![Sélectionner l’option de stratégie](media/f7c7c055-fca7-4a4f-bb97-63e35a65beac.png)
  
  - <span data-ttu-id="3bd44-150">**Pour désactiver une stratégie** Choisissez **opt-out: do Remarque Delete** \> **Save**.</span><span class="sxs-lookup"><span data-stu-id="3bd44-150">**To opt out of a policy** Choose **Opt-Out: Do Note Delete** \> **Save**.</span></span>
    
    <span data-ttu-id="3bd44-p111">En tant que propriétaire du site, vous pouvez refuser une stratégie de suppression de documents si vous déterminez que la stratégie ne s’applique pas au contenu de votre site. Toutefois, vous ne pouvez pas refuser une stratégie qui a été marquée comme **Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="3bd44-p111">As a site owner, you can opt out of a document deletion policy if you determine that the policy is not applicable to the content in your site. However, you cannot opt out of a policy that has been marked as **Mandatory**.</span></span>
    
    ![Option de désactivation](media/efac709c-bef7-4a02-a09d-5bc7d2b4ec63.png)
  
## <a name="document-deletion-policies-override-other-policies"></a><span data-ttu-id="3bd44-154">Les stratégies de suppression de documents remplacent les autres stratégies</span><span class="sxs-lookup"><span data-stu-id="3bd44-154">Document deletion policies override other policies</span></span>

<span data-ttu-id="3bd44-155">Un site peut utiliser d’autres stratégies pour la conservation et la suppression du contenu :</span><span class="sxs-lookup"><span data-stu-id="3bd44-155">A site may use other policies for retaining and deleting content:</span></span>
  
- <span data-ttu-id="3bd44-156">stratégies de type de contenu de la collection de sites ;</span><span class="sxs-lookup"><span data-stu-id="3bd44-156">Content type policies for the site collection.</span></span>
    
- <span data-ttu-id="3bd44-157">stratégies de gestion des informations pour une liste ou une bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="3bd44-157">Information management policies for a list or library.</span></span>
    
<span data-ttu-id="3bd44-158">Si vous appliquez une stratégie de suppression de documents à un site qui utilise déjà des stratégies de type de contenu ou des stratégies de gestion des informations pour une liste ou une bibliothèque, ces stratégies sont ignorées alors que la stratégie de suppression de documents est appliquée.</span><span class="sxs-lookup"><span data-stu-id="3bd44-158">If you apply a document deletion policy to a site that already uses content type policies or information management policies for a list or library, those policies are ignored while the document deletion policy is in effect.</span></span> <span data-ttu-id="3bd44-159">Si d’autres stratégies sont ignorées, le message «le contenu sur ce site utilise les stratégies de suppression de documents» s’affiche.</span><span class="sxs-lookup"><span data-stu-id="3bd44-159">If other policies are ignored, you will see the message "Content on this site uses Document Deletion Policies".</span></span>
  
<span data-ttu-id="3bd44-p113">Cela signifie que vous devez planifier qu’un site n’utilise que des stratégies destinées à du contenu structuré (stratégies de gestion des informations et stratégies de type de contenu) ou à du contenu non structuré (stratégies de suppression de documents), et non les deux. Si vous refusez une stratégie de suppression de documents, l’avertissement ne s’affiche pas et d’autres types de stratégies continueront à fonctionner.</span><span class="sxs-lookup"><span data-stu-id="3bd44-p113">This means you should plan for a site to use only policies meant for structured content (information management policies and content type policies) or unstructured content (document deletion policies), not both. If you opt out of a document deletion policy, the warning will not be displayed and other types of policies will continue to work.</span></span>
  
<span data-ttu-id="3bd44-162">Les stratégies de site ne sont pas affectées par les stratégies de suppression de documents.</span><span class="sxs-lookup"><span data-stu-id="3bd44-162">Site policies are not affected by document deletion policies.</span></span>
  
### <a name="determine-if-content-type-policies-are-being-ignored"></a><span data-ttu-id="3bd44-163">Déterminer si les stratégies de type de contenu sont ignorées</span><span class="sxs-lookup"><span data-stu-id="3bd44-163">Determine if content type policies are being ignored</span></span>

<span data-ttu-id="3bd44-164">Si votre site utilisait des stratégies de type de contenu et que ce message s’affiche maintenant, ces stratégies ne sont plus appliquées.</span><span class="sxs-lookup"><span data-stu-id="3bd44-164">If your site was using content type policies and you now see this message, those policies are no longer in effect.</span></span> <span data-ttu-id="3bd44-165">Pour restaurer les stratégies de type de contenu, vous pouvez supprimer la stratégie de suppression de documents de votre site, comme décrit précédemment, si une option de désactivation est disponible.</span><span class="sxs-lookup"><span data-stu-id="3bd44-165">To restore the content type policies, you can remove the document deletion policy from your site, as described earlier, if there's an opt-out option available.</span></span> <span data-ttu-id="3bd44-166">S’il n’existe pas d’option à désactiver, la stratégie de suppression de documents est obligatoire et vous devez contacter l’officier de conformité de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="3bd44-166">If there's no option to opt out, the document deletion policy is mandatory, and you need to contact the compliance officer in your organization.</span></span>
  
1. <span data-ttu-id="3bd44-167">Dans le coin supérieur droit, sélectionnez paramètres \*\*\*\* du \> **site**paramètres [icône d’engrenage].</span><span class="sxs-lookup"><span data-stu-id="3bd44-167">In the upper-right corner, choose **Settings** [gear icon] \> **Site Settings**.</span></span>
    
2. <span data-ttu-id="3bd44-168">Sous **modèles de stratégie de type de contenu**d’administration \> de **site** .</span><span class="sxs-lookup"><span data-stu-id="3bd44-168">Under **Site Administration** \> **Content Type Policy Templates**.</span></span>
    
    ![Avertissement sur le site utilisé par les stratégies de suppression de documents](media/4cc3d703-9aff-4695-9670-f78c291c0010.png)
  
### <a name="determine-if-information-management-policies-are-being-ignored"></a><span data-ttu-id="3bd44-170">Déterminer si les stratégies de gestion des informations sont ignorées</span><span class="sxs-lookup"><span data-stu-id="3bd44-170">Determine if information management policies are being ignored</span></span>

<span data-ttu-id="3bd44-171">Si votre site utilisait des stratégies de gestion des informations et que ce message s’affiche maintenant, ces stratégies ne sont plus appliquées.</span><span class="sxs-lookup"><span data-stu-id="3bd44-171">If your site was using information management policies and you now see this message, those policies are no longer in effect.</span></span> <span data-ttu-id="3bd44-172">Pour restaurer les stratégies de gestion des informations, vous pouvez supprimer la stratégie de suppression de documents de votre site, comme décrit précédemment, si une option de désactivation est disponible.</span><span class="sxs-lookup"><span data-stu-id="3bd44-172">To restore the information management policies, you can remove the document deletion policy from your site, as described earlier, if there's an opt-out option available.</span></span> <span data-ttu-id="3bd44-173">S’il n’existe pas d’option à désactiver, la stratégie de suppression de documents est obligatoire et vous devez contacter l’officier de conformité de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="3bd44-173">If there's no option to opt out, the document deletion policy is mandatory, and you need to contact the compliance officer in your organization.</span></span>
  
- <span data-ttu-id="3bd44-174">Pour une liste ou une bibliothèque, dans les \> \*\*\*\* \> **paramètres** \> de la bibliothèque d’onglets de la bibliothèque du ruban, sous **paramètres de stratégie de gestion des informations**de **gestion** \> et des autorisations.</span><span class="sxs-lookup"><span data-stu-id="3bd44-174">For a list or library, on the Ribbon \> **Library** tab \> **Library Settings** \> under **Permissions and Management** \> **Information Management Policy Settings**.</span></span>
    
    ![Avertissement sur le site utilisé par les stratégies de suppression de documents](media/3f043057-a741-4cd8-a165-6d139b986064.png)
  
## <a name="see-also"></a><span data-ttu-id="3bd44-176">Voir également</span><span class="sxs-lookup"><span data-stu-id="3bd44-176">See also</span></span>

<span data-ttu-id="3bd44-177">
  [Vue d’ensemble des stratégies de suppression de documents](document-deletion-policies.md)</span><span class="sxs-lookup"><span data-stu-id="3bd44-177">[Overview of document deletion policies](document-deletion-policies.md)</span></span>
  
[<span data-ttu-id="3bd44-178">Création d’une stratégie de suppression de documents</span><span class="sxs-lookup"><span data-stu-id="3bd44-178">Create a document deletion policy</span></span>](create-a-document-deletion-policy.md)

