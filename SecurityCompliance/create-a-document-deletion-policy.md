---
title: Création d’une stratégie de suppression de documents
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- SPO160
ms.assetid: 41b2ed73-eb8d-4429-945e-a8197894585a
description: Les organisations doivent souvent conserver des documents pendant une certaine période de temps en raison des réglementations de conformité, juridiques, ou autres. Toutefois, conserver des documents plus longtemps que nécessaire peut exposer l’organisation à un risque juridique.
ms.openlocfilehash: 115e4d7df93d81e7ee5a860f20a00d9cb175f927
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "23013998"
---
# <a name="create-a-document-deletion-policy"></a><span data-ttu-id="0e5a4-104">Création d’une stratégie de suppression de documents</span><span class="sxs-lookup"><span data-stu-id="0e5a4-104">Create a document deletion policy</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0e5a4-p102">Aller plus loin, nous vous conseillons d’utiliser une stratégie de rétention ou étiquettes créées dans la sécurité &amp; centre de conformité au lieu d’une stratégie de suppression de documents. Stratégies de suppression de documents continueront de fonctionner en côte à côte des stratégies de rétention, mais si vous devez conserver ou supprimer du contenu n’importe où dans Office 365, nous vous conseillons d’utiliser une stratégie de rétention. Pour plus d’informations, voir [utiliser une stratégie de rétention au lieu de ces fonctionnalités](retention-policies.md#use-a-retention-policy-instead-of-these-features).</span><span class="sxs-lookup"><span data-stu-id="0e5a4-p102">Moving forward, we recommend that you use a retention policy or labels created in the Security &amp; Compliance Center instead of a document deletion policy. Document deletion policies will continue to work side by side with retention policies, but if you need to retain or delete content anywhere in Office 365, we recommend that you use a retention policy. For more information, see [Use a retention policy instead of these features](retention-policies.md#use-a-retention-policy-instead-of-these-features).</span></span> 
  
<span data-ttu-id="0e5a4-p103">Les organisations doivent souvent conserver des documents pendant une certaine période de temps en raison des réglementations de conformité, juridiques, ou autres. Toutefois, conserver des documents plus longtemps que nécessaire peut exposer l’organisation à un risque juridique.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-p103">Organizations are often required to retain documents for a certain period of time due to compliance, legal, or other regulations. However, retaining documents for longer than required can expose the organization to legal risk.</span></span>
  
<span data-ttu-id="0e5a4-110">Avec une stratégie de suppression de documents, vous pouvez réduire proactive des risques en supprimant des documents dans un site après une période de temps spécifique, par exemple, vous pouvez supprimer les documents dans OneDrive des utilisateurs pour les professionnels sites cinq ans après les documents ont été créés.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-110">With a document deletion policy, you can proactively reduce risk by deleting documents in a site after a specific period of time—for example, you can delete documents in users' OneDrive for Business sites five years after the documents were created.</span></span> 
  
<span data-ttu-id="0e5a4-p104">Après avoir créé une stratégie de suppression de documents, vous pouvez l’affecter à un modèle de collection de sites, pour que la stratégie soit disponible pour toutes les collections de sites créées à partir de ce modèle. Vous pouvez également affecter une stratégie à une collection de sites spécifique, qui remplace toutes les stratégies qui ont pu être affectées au modèle pour cette collection de sites.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-p104">After you create a document deletion policy, you can assign it to a site collection template, so that the policy is available to all site collections created from that template. You can also assign a policy to a specific a site collection, which overrides any policies that may have been assigned to the template for that site collection.</span></span>
  
![Page d’accueil du centre de stratégies de suppression de documents](media/IP-Document-Deletion-Policy-Center-home-page.png)
  
## <a name="policy-templates"></a><span data-ttu-id="0e5a4-114">Modèles de stratégie</span><span class="sxs-lookup"><span data-stu-id="0e5a4-114">Policy templates</span></span>

<span data-ttu-id="0e5a4-p105">Vous pouvez créer une stratégie de suppression de document de A à Z ou vous pouvez utiliser l’un des exemples de stratégie. Le Centre des stratégies de conformité inclut des exemples de stratégie que vous pouvez utiliser en l’état ou que vous pouvez utiliser comme point de départ, pour ensuite les renommer ou les modifier.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-p105">You can create a document deletion policy from scratch, or you can use one of the sample policies. The Compliance Policy Center includes sample policies that you can use as is, or you can use them as a starting point and then rename or modify them.</span></span>
  
![Stratégies de suppression d’exemple de document](media/IP-Sample-deletion-policies.png)
  
## <a name="examples-of-how-to-use-document-deletion-policies"></a><span data-ttu-id="0e5a4-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="0e5a4-118">Examples of how to use document deletion policies</span></span>

<span data-ttu-id="0e5a4-p106">Une collection de sites ou d’un modèle de collection de sites peut avoir une stratégies supplémentaires qui lui est affectés et chacune de ces stratégies peut avoir une ou plusieurs règles. Toutefois, il peut y avoir qu’une seule stratégie est active par site, et il peut y avoir qu’une seule règle de suppression qui est active à tout moment pour les bibliothèques au sein du site.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-p106">A site collection or a site collection template can have one more policies assigned to it, and each of those policies can have one or more rules. However, there can be only one policy that's active per site, and there can be only one deletion rule that's active at any time for the libraries within the site.</span></span>
  
![Schéma montrant la relation entre les stratégies](media/IP-Two-policies-four-rules.png)
  
<span data-ttu-id="0e5a4-122">En outre, vous pouvez sélectionner une stratégie comme stratégie obligatoire ou par défaut, et vous pouvez sélectionner une règle de suppression comme règle par défaut :</span><span class="sxs-lookup"><span data-stu-id="0e5a4-122">In addition, you can select a policy as mandatory or default, and you can select a deletion rule as a default rule:</span></span> 
  
- <span data-ttu-id="0e5a4-p107">**Stratégie obligatoire** Lorsqu’une stratégie est marquée comme étant obligatoire, stratégie qu’une seule peut être affectée à la collection de sites ou du modèle. La stratégie doit être marquée comme valeur par défaut et sera appliquée à tous les sites. Les propriétaires de sites ne peut pas refuser la stratégie.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-p107">**Mandatory policy**When a policy is marked as mandatory, only one policy can be assigned to the site collection or template. The policy must be marked as default and will be applied to all sites. Site owners cannot opt out of the policy.</span></span>
    
- <span data-ttu-id="0e5a4-126">**Stratégie par défaut** Lorsqu’une stratégie est définie comme valeur par défaut, la stratégie est automatiquement active dans tous les sites auxquels il est affecté à aucune action requise par le propriétaire du site.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-126">**Default policy**When a policy is set as default, the policy is automatically active in all sites that it's assigned to with no action required by site owner.</span></span>
    
- <span data-ttu-id="0e5a4-127">**Règle par défaut** Lorsqu’une règle de suppression est définie comme valeur par défaut, elle est automatiquement appliquée à toutes les bibliothèques dans les sites qui utilisent la stratégie.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-127">**Default rule**When a deletion rule is set as default, it is automatically applied to all libraries in the sites that use the policy.</span></span>
    
<span data-ttu-id="0e5a4-128">Les exemples suivants expliquent quand vous pouvez utiliser une stratégie obligatoire ou des stratégies et règles par défaut.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-128">The following examples explain when you might want to use a mandatory policy or default policies and rules.</span></span>
  
### <a name="example-1-apply-a-single-policy-with-a-single-rule-to-a-site-collection-template"></a><span data-ttu-id="0e5a4-129">Exemple 1 : Appliquer une stratégie unique avec une règle unique à un modèle de collection de sites</span><span class="sxs-lookup"><span data-stu-id="0e5a4-129">Example 1: Apply a single policy with a single rule to a site collection template</span></span>

<span data-ttu-id="0e5a4-p108">Vous pouvez appliquer une stratégie de suppression de documents à un large éventail de contenus non structurés (tous les sites OneDrive Entreprise ou tous les sites d’équipe, par exemple). Si vous souhaitez vous assurer qu’une stratégie de suppression de documents unique est active dans tous les sites créés à partir d’un modèle de collection de sites, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="0e5a4-p108">You may want to enforce a document deletion policy across a broad range of unstructured content, such as all OneDrive for Business sites or all team sites. If you want to ensure that a single document deletion policy is active in all sites created from a site collection template, you can:</span></span>
  
1. <span data-ttu-id="0e5a4-132">créer une stratégie unique avec une règle de suppression par défaut unique ;</span><span class="sxs-lookup"><span data-stu-id="0e5a4-132">Create a single policy with a single default deletion rule.</span></span>
    
2. <span data-ttu-id="0e5a4-133">définir la stratégie comme étant obligatoire et par défaut ;</span><span class="sxs-lookup"><span data-stu-id="0e5a4-133">Set the policy as mandatory and default.</span></span>
    
3. <span data-ttu-id="0e5a4-134">affecter la stratégie à un modèle de collection de sites.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-134">Assign the policy to a site collection template.</span></span>
    
<span data-ttu-id="0e5a4-p109">Dans cet exemple, la règle de suppression par défaut sera appliquée à toutes les bibliothèques dans toutes les collections de sites créées à partir du modèle, et les propriétaires de sites ne peuvent pas refuser la stratégie. Il s’agit de la façon la plus simple d’appliquer de façon large et rigide une stratégie de suppression de documents.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-p109">In this example, the default deletion rule will be applied to all libraries in all site collections created from the template, and site owners cannot opt out of the policy. This is the simplest way to broadly and rigidly enforce a document deletion policy.</span></span>
  
![Schéma montrant une seule stratégie obligatoire](media/IP-Example-1-doc-deletion-policies.png)
  
### <a name="example-2-apply-a-single-policy-with-several-rules-to-a-site-collection-template"></a><span data-ttu-id="0e5a4-138">Exemple 2 : Appliquer une stratégie unique avec plusieurs règles à un modèle de collection de sites</span><span class="sxs-lookup"><span data-stu-id="0e5a4-138">Example 2: Apply a single policy with several rules to a site collection template</span></span>

<span data-ttu-id="0e5a4-p110">Les propriétaires de sites sont souvent les mieux placés pour savoir quel type de contenu leur site contient, donc vous pouvez choisir de les autoriser à sélectionner la règle de suppression qui s’applique le mieux à leur site. Vous pouvez également autoriser les propriétaires de sites à refuser une stratégie entièrement.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-p110">Site owners often know best what type of content their site contains, so you may choose to allow site owners to select the deletion rule that best applies to their site. You may also want to allow site owners to opt out of a policy entirely.</span></span>
  
<span data-ttu-id="0e5a4-p111">Simultanément, vous pouvez toujours créer et gérer centralement les stratégies. Vous pouvez également sélectionner une stratégie et une règle comme stratégie et règle par défaut, pour que la stratégie soit toujours active tant que le propriétaire du site n’en choisit pas une autre ou la refuse. Si vous souhaitez offrir une telle flexibilité aux propriétaires de sites, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="0e5a4-p111">At the same time, you can still centrally create and manage the policies. You can also select one policy and rule as the default, so that a policy is always in effect until the site owner chooses a different one or opts out. If you want to provide such flexibility to site owners, you can:</span></span>
  
1. <span data-ttu-id="0e5a4-143">créer une stratégie unique avec plusieurs règles de suppression et définir une règle par défaut ;</span><span class="sxs-lookup"><span data-stu-id="0e5a4-143">Create a single policy with several deletion rules, and set one rule as the default.</span></span>
    
2. <span data-ttu-id="0e5a4-144">définir la stratégie comme stratégie par défaut ;</span><span class="sxs-lookup"><span data-stu-id="0e5a4-144">Set the policy as the default policy.</span></span>
    
3. <span data-ttu-id="0e5a4-145">affecter la stratégie à un modèle de collection de sites.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-145">Assign the policy to a site collection template.</span></span>
    
<span data-ttu-id="0e5a4-146">Les propriétaires de sites peuvent choisir l’une des règles de suppression alternatives, refuser la stratégie, ou ne rien faire et être soumis à la stratégie et à la règle par défaut.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-146">Site owners can select one of the alternate deletion rules, opt out of the policy, or do nothing and be subject to the default policy and rule.</span></span>
  
![Schéma montrant une stratégie comportant beaucoup de règles](media/IP-Example-2-doc-deletion-policies.png)
  
### <a name="example-3-apply-several-policies-with-one-or-more-rules-to-a-site-collection"></a><span data-ttu-id="0e5a4-148">Exemple 3 : Appliquer plusieurs stratégies avec une ou plusieurs règles à une collection de sites</span><span class="sxs-lookup"><span data-stu-id="0e5a4-148">Example 3: Apply several policies with one or more rules to a site collection</span></span>

<span data-ttu-id="0e5a4-p112">Cet exemple fournit le maximum de flexibilité pour les propriétaires de sites car ils peuvent choisir parmi plusieurs stratégies, et après avoir sélectionné une règle, ils peuvent souvent effectuer un choix parmi plusieurs règles. Une stratégie et une règle sont définies comme stratégie et règle par défaut, pour que la stratégie soit toujours active tant que le propriétaire du site n’en choisit pas une autre ou la refuse. Notez que si vous ne définissez pas une stratégie et une règle par défaut, aucune stratégie ou aucune règle ne sera active pour les bibliothèques de documents dans le site tant que le propriétaire du site ne prendra pas des mesures pour les sélectionner et les appliquer.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-p112">This example provides the maximum flexibility to site owners because they can choose from several policies, and after selecting a policy they can often choose from several rules. One policy and rule are set as default, so that a policy is always in effect until the site owner chooses a different one or opts out. Note that if you do not set a policy and rule as the default, then no policies or rules will be active for the document libraries in the site until the site owner takes action to select and apply them.</span></span>
  
<span data-ttu-id="0e5a4-p113">Contrairement aux deux exemples précédents, ces stratégies sont affectées à une collection de sites spécifique, et non au modèle de collection de sites. Cela signifie que les stratégies peuvent être adaptées plus spécifiquement au contenu dans une collection de sites donnée.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-p113">Unlike the previous two examples, these policies are assigned to a specific site collection — not the site collection template. This means the policies can be more specifically tailored for the content in a specific site collection.</span></span>
  
<span data-ttu-id="0e5a4-p114">Les stratégies et les règles sont héritées. Les propriétaires de sites peuvent sélectionner une stratégie et une règle pour leur site, et tous les sous-sites héritent de la stratégie du parent. Toutefois, le propriétaire d’un sous-site peut annuler l’héritage en sélectionnant une stratégie et une règle différentes, qui s’appliquent à leur tour à tous les sous-sites tant que l’héritage n’est pas de nouveau annulé.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-p114">Policies and rules are inherited. Site owners can select a policy and rule for their site, and all subsites inherit the policy from the parent. However, an owner of a subsite can break inheritance by selecting a different policy and rule, which in turn applies to all subsites until inheritance is broken again.</span></span>
  
<span data-ttu-id="0e5a4-156">Pour configurer ce scénario, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="0e5a4-156">To set up this scenario, you can:</span></span>
  
1. <span data-ttu-id="0e5a4-157">créer plusieurs stratégies contenant chacune une ou plusieurs règles ;</span><span class="sxs-lookup"><span data-stu-id="0e5a4-157">Create several policies that each contains one or more rules.</span></span>
    
2. <span data-ttu-id="0e5a4-158">définir une stratégie et une règle par défaut ;</span><span class="sxs-lookup"><span data-stu-id="0e5a4-158">Set a policy and rule as the default.</span></span>
    
3. <span data-ttu-id="0e5a4-159">affecter les stratégies à une collection de sites spécifique.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-159">Assign the policies to a specific site collection.</span></span>
    
<span data-ttu-id="0e5a4-160">En outre, les stratégies et les règles sont adaptées à une collection de sites spécifique, où les propriétaires de sites peuvent annuler l’héritage en sélectionnant la stratégie et la règle qui s’appliquent le mieux à leur site.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-160">In addition, the policies and rules are tailored to a specific site collection, where site owners can break inheritance by selecting the policy and rule that best applies to their site.</span></span>
  
![Schéma montrant de nombreuses stratégies et règles](media/IP-Example-3-doc-deletion-policies.png)
  
## <a name="create-a-document-deletion-policy"></a><span data-ttu-id="0e5a4-162">Création d’une stratégie de suppression de documents</span><span class="sxs-lookup"><span data-stu-id="0e5a4-162">Create a document deletion policy</span></span>

1. <span data-ttu-id="0e5a4-p115">Dans la 365Security Office &amp; centre de conformité, accédez à **gestion de données** \> **rétention**. Sous **Supprimer**, cliquez sur **Gérer les stratégies de suppression de documents pour SharePoint Online et OneDrive for Business**. Le centre de stratégie de suppression de Document s’ouvre dans un nouvel onglet de navigateur.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-p115">In the Office 365Security &amp; Compliance Center, navigate to **Data management** \> **Retention**. Under **Delete**, click **Manage document deletion policies for SharePoint Online and OneDrive for Business**. The Document Deletion Policy Center opens in a new browser tab.</span></span>
    
    <span data-ttu-id="0e5a4-p116">La première fois que vous accédez à partir de la sécurité &amp; centre de conformité pour le centre de stratégie de suppression de documents, le centre de la stratégie est automatiquement créé pour vous. Vous pouvez également créer manuellement le centre de la stratégie en fonction [de la collection de sites](http://go.microsoft.com/fwlink/p/?LinkID=404342) **Centre de stratégie de conformité** sur l’onglet **entreprise** .</span><span class="sxs-lookup"><span data-stu-id="0e5a4-p116">The first time you navigate from the Security &amp; Compliance Center to the Document Deletion Policy Center, the policy center is automatically created for you. Alternatively, you can manually create the policy center by [creating the site collection](http://go.microsoft.com/fwlink/p/?LinkID=404342) and choosing **Compliance Policy Center** on the **Enterprise** tab.</span></span> 
    
2. <span data-ttu-id="0e5a4-168">Choisissez les **stratégies de suppression**.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-168">Choose **Deletion Policies**.</span></span>
    
    ![Option de suppression des stratégies](media/IP-Deletion-Policies-option.png)
  
3. <span data-ttu-id="0e5a4-170">Choisissez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-170">Choose **new item**.</span></span>
    
4. <span data-ttu-id="0e5a4-p117">Entrez un nom de stratégie et une description. Il se peut que les propriétaires de sites choisissent une stratégie pour leur site en fonction de ce nom et de cette description. Par conséquent, donnez suffisamment d’informations pour qu’ils choisissent la stratégie correcte.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-p117">Enter a policy name and description. Site owners may be selecting a policy for their site based on this name and description, so include enough information for them to choose the correct policy.</span></span>
    
5. <span data-ttu-id="0e5a4-173">Pour créer une règle, choisissez **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-173">To create a rule, choose **New**.</span></span>
    
6. <span data-ttu-id="0e5a4-174">Entrez un nom et choisissez les options suivantes :</span><span class="sxs-lookup"><span data-stu-id="0e5a4-174">Enter a name and choose the following options:</span></span>
    
  - <span data-ttu-id="0e5a4-p118">Choisir la règle sera définitivement supprimer les documents ou de les supprimer dans la Corbeille. La Corbeille fournit un filet de deuxième niveau avant la suppression définitive d’un élément à partir d’un site. Pour plus d’informations sur la Corbeille, voir [Vider la Corbeille ou restaurer vos fichiers](http://go.microsoft.com/fwlink/p/?LinkID=404348).</span><span class="sxs-lookup"><span data-stu-id="0e5a4-p118">Choose whether the rule will permanently delete documents or delete them to the Recycle Bin. The Recycle Bin provides a second-stage safety net before an item is permanently deleted from a site. For more information about the Recycle Bin, see [Empty the Recycle Bin or restore your files](http://go.microsoft.com/fwlink/p/?LinkID=404348).</span></span>
    
  - <span data-ttu-id="0e5a4-178">Indiquez si la date de suppression est calculée à partir de la date de création d’un document ou de la date de dernière modification.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-178">Choose whether the deletion date is calculated from the date when a document was created or last modified.</span></span>
    
  - <span data-ttu-id="0e5a4-179">Entrez un nombre de jours, de mois ou d’années comme période de temps au bout de laquelle un document sera supprimé.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-179">Enter a number of days, months, or years as the time period after which a document will be deleted.</span></span>
    
  - <span data-ttu-id="0e5a4-p119">Indiquez si la règle est une règle par défaut. La première règle que vous créez est automatiquement définie comme règle par défaut. Une règle par défaut est appliquée automatiquement à toutes les bibliothèques dans les sites qui utilisent la stratégie.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-p119">Choose whether the rule is a default rule. The first rule that you create is automatically set as the default rule. A default rule is automatically applied to all libraries in the sites that use the policy.</span></span>
    
![Page Nouvelle règle de suppression](media/IP-New-deletion-rule.png)
  
7. <span data-ttu-id="0e5a4-184">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-184">Click **Save**.</span></span>
    
8. <span data-ttu-id="0e5a4-p120">Créez des règles supplémentaires si vous souhaitez que les propriétaires de sites puissent choisir différentes règles à appliquer à leur site. La règle par défaut, le cas échéant, s’appliquera si le propriétaire du site n’effectue aucune action.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-p120">Create additional rules if you want site owners to be able to choose different rules to apply to their site. The default rule, if any, will be applied if the site owner takes no action.</span></span>
    
9. <span data-ttu-id="0e5a4-187">Pour supprimer une règle d’une stratégie, sélectionnez la règle, cliquez sur **Supprimer**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-187">To remove a rule from a policy, select the rule, click **Delete**, and then click **OK**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="0e5a4-188">Si vous supprimez une règle, la stratégie ne contient-elle pas d’une règle par défaut, puis aucune règle ne sera en vigueur pour cette stratégie — en d’autres termes, aucun document ne sera supprimé.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-188">If you delete a rule, and the policy does not contain a default rule, then no rule will be in effect for that policy—in other words, no documents will be deleted.</span></span> 
  
![Message de confirmation de la suppression de la règle de la stratégie](media/IP-Remove-rule-from-policy-message.png)
  
## <a name="assign-the-document-deletion-policy-to-a-site-collection-template"></a><span data-ttu-id="0e5a4-190">Affectation de la stratégie de suppression de documents à un modèle de collection de sites</span><span class="sxs-lookup"><span data-stu-id="0e5a4-190">Assign the document deletion policy to a site collection template</span></span>

<span data-ttu-id="0e5a4-191">En affectant une stratégie à un modèle de collection de sites, vous mettez la stratégie à la disposition de toutes les collections de sites créées à partir de ce modèle, y compris les collections de sites existantes et les collections de sites créées à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-191">By assigning a policy to a site collection template, you make the policy available to all site collections created from that template, including both existing site collections and site collections created in the future.</span></span>
  
<span data-ttu-id="0e5a4-p121">Il est important de comprendre que la période de temps spécifiée pour un document de stratégie de suppression signifie l’heure dans la mesure où le document a été créé ou modifié, pas l’heure dans la mesure où la stratégie a été attribuée. Lorsque vous attribuez la stratégie pour la première fois, tous les documents dans le site sont évaluées et, si elles répondent aux critères, ils seront supprimés. Cela s’applique à tous les documents existants, pas seulement nouveaux documents créés dans la mesure où la stratégie a été attribuée.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-p121">It's important to understand that the time period specified for a document deletion policy means the time since the document was created or modified, not the time since the policy was assigned. When you assign the policy for the first time, all documents in the site are evaluated and, if they meet the criteria, they will be deleted. This applies to all existing documents, not just new documents created since the policy was assigned.</span></span>
  
1. <span data-ttu-id="0e5a4-p122">Dans la sécurité &amp; centre de conformité, accédez à **gestion de données** \> **rétention**. Sous **Supprimer**, cliquez sur **Gérer les stratégies de suppression de documents pour SharePoint Online et OneDrive for Business**. Le centre de stratégie de suppression de Document s’ouvre dans un nouvel onglet de navigateur.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-p122">In the Security &amp; Compliance Center, navigate to **Data management** \> **Retention**. Under **Delete**, click **Manage document deletion policies for SharePoint Online and OneDrive for Business**. The Document Deletion Policy Center opens in a new browser tab.</span></span>
    
2. <span data-ttu-id="0e5a4-198">Choisissez **Attributions de stratégies pour les modèles**.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-198">Choose **Policy Assignments for Templates**.</span></span>
    
    ![Option d’attributions des stratégies pour les modèles](media/IP-Policy-Assignments-for-Templates-option.png)
  
3. <span data-ttu-id="0e5a4-200">Choisissez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-200">Choose **new item**.</span></span>
    
4. <span data-ttu-id="0e5a4-201">Effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="0e5a4-201">Do one of the following:</span></span>
    
  - <span data-ttu-id="0e5a4-202">Pour affecter la stratégie à un modèle de collection de sites tel que le modèle de site d’équipe, sélectionnez **Affecter au modèle de collection de sites**, puis sélectionnez le modèle de collection de sites.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-202">To assign the policy to a site collection template such as the Team Site template, select **Assign to site collection template**, and then select the site collection template.</span></span>
    
  - <span data-ttu-id="0e5a4-203">Pour affecter la stratégie à un lecteur des utilisateurs pour les entreprises, choisissez **affecter à OneDrive pour le modèle d’entreprise**, mis en surbrillance ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-203">To assign the policy to users' One Drive for Business, choose **Assign to OneDrive for Business Template**, highlighted below.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="0e5a4-204">Lorsque vous affectez une stratégie à un modèle de collection de sites, cette stratégie est disponible à la fois pour les collections de sites existantes créées à partir de ce modèle et pour les collections de sites créées à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-204">When you assign a policy to a site collection template, that policy will be available both to existing site collections created from that template and to site collections created in the future.</span></span> 
  
![Page Choisir un modèle affichant l’option OneDrive](media/IP-Choose-a-template.png)
  
5. <span data-ttu-id="0e5a4-206">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-206">Click **Save**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="0e5a4-p123">Chaque modèle peut avoir qu’un seul ensemble de stratégies qui lui est affecté. Si vous voyez une erreur indiquant que ce modèle possède déjà des stratégies qui lui est affectés, choisissez **Annuler** \> **affecter à la Collection de sites** dans le volet de navigation gauche \> sélectionner une collection de sites pour afficher et gérer l’ensemble des stratégies qui sont déjà affecté.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-p123">Each template can have only one set of policies assigned to it. If you see an error saying that this template already has policies assigned to it, choose **Cancel** \> **Assign to Site Collection** in the left navigation \> select a site collection to view and manage the set of policies that are already assigned.</span></span> 
  
6. <span data-ttu-id="0e5a4-p124">Cliquez sur **Gérer les stratégies affectées**, sélectionnez les stratégies que vous souhaitez attribuer, puis choisissez si une stratégie est la stratégie par défaut. Lorsque vous définissez une stratégie par défaut, tous les sites sont affectés automatiquement à la stratégie disposent de la stratégie active aucune action requise par le propriétaire du site.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-p124">Choose **Manage Assigned Policies**, select the policies that you want to assign, and then choose whether one policy is the default policy. When you set a default policy, all sites assigned to the policy automatically have the policy active with no action required by site owner.</span></span>
    
    ![Page Ajouter et gérer les stratégies](media/IP-Add-and-manage-policies-page.png)
  
7. <span data-ttu-id="0e5a4-212">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-212">Click **Save**.</span></span>
    
8. <span data-ttu-id="0e5a4-p125">Si vous souhaitez appliquer la stratégie sur tous les sites sans autoriser les propriétaires de sites à la refuser, choisissez **Marquer la stratégie comme obligatoire**. Lorsque vous définissez une stratégie comme obligatoire, seule cette stratégie unique peut être affectée au modèle de collection de sites. La stratégie doit également être marquée comme stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-p125">If you want to enforce the policy on all sites without allowing site owners to opt out, choose **Mark Policy as Mandatory**. When you make a policy mandatory, only that single policy can be assigned to the site collection template. The policy must also be marked as default.</span></span>
    
    <span data-ttu-id="0e5a4-216">Si cette option est grisée, choisissez **Gérer les stratégies affectées** et assurez-vous qu’au moins une stratégie est affectée et définie comme stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-216">If this option is grayed out, choose **Manage Assigned Policies** and make sure that at least one policy is assigned and set as default.</span></span> 
    
9. <span data-ttu-id="0e5a4-217">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-217">Click **Save**.</span></span>
    
## <a name="assign-the-document-deletion-policy-to-a-site-collection"></a><span data-ttu-id="0e5a4-218">Affectation de la stratégie de suppression de documents à une collection de sites</span><span class="sxs-lookup"><span data-stu-id="0e5a4-218">Assign the document deletion policy to a site collection</span></span>

<span data-ttu-id="0e5a4-p126">En affectant une stratégie à une collection de sites spécifique, vous mettez la stratégie à disposition uniquement de cette collection de sites spécifique. Cela signifie que vous pouvez adapter des stratégies plus étroitement au contenu dans la collection de sites. En outre, les stratégies affectées à une collection de sites spécifique remplacent toutes les stratégies qui sont affectées au modèle pour cette collection de sites. Par exemple, une stratégie affectée à la collection de sites du département des ventes (créée à partir du modèle du site d’équipe) remplace toutes les stratégies affectées au modèle de site d’équipe.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-p126">By assigning a policy to a specific site collection, you make the policy available only to that specific site collection. This means you can tailor policies more closely to the content in the site collection. Also, policies assigned to a specific site collection will override any policies that are assigned to the template for that site collection. For example, a policy assigned to the Sales Department site collection (created from the Team Site template) will override any policies assigned to the Team Site template.</span></span>
  
<span data-ttu-id="0e5a4-p127">Il est important de comprendre que la période de temps spécifiée pour un document de stratégie de suppression signifie l’heure dans la mesure où le document a été créé ou modifié, pas l’heure dans la mesure où la stratégie a été attribuée. Lorsque vous attribuez la stratégie pour la première fois, tous les documents dans le site sont évaluées et, si elles répondent aux critères, ils seront supprimés. Cela s’applique à tous les documents existants, pas seulement nouveaux documents créés dans la mesure où la stratégie a été attribuée.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-p127">It's important to understand that the time period specified for a document deletion policy means the time since the document was created or modified, not the time since the policy was assigned. When you assign the policy for the first time, all documents in the site are evaluated and, if they meet the criteria, they will be deleted. This applies to all existing documents, not just new documents created since the policy was assigned.</span></span>
  
1. <span data-ttu-id="0e5a4-p128">Dans la sécurité &amp; centre de conformité, accédez à **gestion de données** \> **rétention**. Sous **Supprimer**, sélectionnez **Gérer les stratégies de suppression de documents pour SharePoint Online et OneDrive for Business**. Le centre de stratégie de suppression de Document s’ouvre dans un nouvel onglet de navigateur.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-p128">In the Security &amp; Compliance Center, navigate to **Data management** \> **Retention**. Under **Delete**, choose **Manage document deletion policies for SharePoint Online and OneDrive for Business**. The Document Deletion Policy Center opens in a new browser tab.</span></span>
    
2. <span data-ttu-id="0e5a4-229">Choisissez **Attributions de stratégies pour les collections de sites**.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-229">Choose **Policy Assignments for Site Collections**.</span></span>
    
    ![Option d’attributions des stratégies pour les collections de sites](media/IP-Policy-Assignments-for-Site-Collections-option.png)
  
3. <span data-ttu-id="0e5a4-231">Choisissez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-231">Choose **new item**.</span></span>
    
4. <span data-ttu-id="0e5a4-p129">Choisissez **Choisir une collection de sites**. Recherche de la collection de sites par nom ou URL, sélectionnez la collection de sites, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-p129">Choose **Choose a site collection**. Search for the site collection by name or URL, select the site collection and click **Save**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="0e5a4-p130">Chaque collection de sites peut avoir qu’un seul ensemble de stratégies qui lui est affecté. Si vous voyez une erreur indiquant que cette collection de sites déjà dispose des stratégies qui lui est affectés, choisissez **Annuler** \> **affecter à la Collection de sites** et sélectionnez une collection de sites pour afficher et gérer l’ensemble des stratégies qui sont déjà affectés.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-p130">Each site collection can have only one set of policies assigned to it. If you see an error saying that this site collection already has policies assigned to it, choose **Cancel** \> **Assign to Site Collection** and select a site collection to view and manage the set of policies that are already assigned.</span></span> 
  
![Page Choisir une collection de sites](media/IP-Choose-a-site-collection-page.png)
  
5. <span data-ttu-id="0e5a4-p131">Cliquez sur **Gérer les stratégies affectées**, sélectionnez les stratégies que vous souhaitez attribuer, puis choisissez si une stratégie est la stratégie par défaut. Lorsque vous définissez une stratégie par défaut, tous les sites sont affectés automatiquement à la stratégie disposent de la stratégie active aucune action requise par le propriétaire du site.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-p131">Choose **Manage Assigned Policies**, select the policies that you want to assign, and then choose whether one policy is the default policy. When you set a default policy, all sites assigned to the policy automatically have the policy active with no action required by site owner.</span></span>
    
    ![Page Ajouter et gérer les stratégies](media/IP-Add-and-manage-policies-page.png)
  
6. <span data-ttu-id="0e5a4-240">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-240">Click **Save**.</span></span>
    
7. <span data-ttu-id="0e5a4-p132">Si vous souhaitez appliquer la stratégie sur tous les sites sans autoriser les propriétaires de sites à refuser, choisissez **Marquer la stratégie comme obligatoire**. Lorsque vous définissez une stratégie comme obligatoire, seule cette stratégie unique peut être affectée à la collection de sites. La stratégie doit également être marquée comme stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-p132">If you want to enforce the policy on all sites without allowing site owners to opt out, choose **Mark Policy as Mandatory**. When you make a policy mandatory, only that single policy can be assigned to the site collection. The policy must also be marked as default.</span></span>
    
    <span data-ttu-id="0e5a4-244">Si cette option est grisée, choisissez **Gérer les stratégies affectées** et assurez-vous qu’au moins une stratégie est affectée et définie comme stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-244">If this option is grayed out, choose **Manage Assigned Policies** and make sure that at least one policy is assigned and set as default.</span></span> 
    
8. <span data-ttu-id="0e5a4-245">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-245">Click **Save**.</span></span>
    
## <a name="delete-a-policy-assignment"></a><span data-ttu-id="0e5a4-246">Suppression d’une affectation de stratégie</span><span class="sxs-lookup"><span data-stu-id="0e5a4-246">Delete a policy assignment</span></span>

<span data-ttu-id="0e5a4-247">Lorsque vous supprimez une affectation, les stratégies affectées ne s’appliquent plus à aucun site dans la collection de sites ou le modèle de collection de sites.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-247">When you delete an assignment, the assigned policies will no longer apply to any sites in the site collection or site collection template.</span></span>
  
1. <span data-ttu-id="0e5a4-p133">Dans la sécurité &amp; centre de conformité, accédez à **gestion de données** \> **rétention**. Sous **Supprimer**, sélectionnez **Gérer les stratégies de suppression de documents pour SharePoint Online et OneDrive for Business**. Le centre de stratégie de suppression de Document s’ouvre dans un nouvel onglet de navigateur.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-p133">In the Security &amp; Compliance Center, navigate to **Data management** \> **Retention**. Under **Delete**, choose **Manage document deletion policies for SharePoint Online and OneDrive for Business**. The Document Deletion Policy Center opens in a new browser tab.</span></span>
    
2. <span data-ttu-id="0e5a4-251">Choisissez **Attributions de stratégies pour les modèles** ou **Attributions de stratégies pour les collections de sites**.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-251">Choose either **Policy Assignments for Templates** or **Policy Assignments for Site Collections**.</span></span>
    
3. <span data-ttu-id="0e5a4-252">Sélectionnez l’élément de l’affectation, cliquez sur **Supprimer l’élément**.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-252">Select the assignment item and click **Delete Item**.</span></span>
    
    ![Commande de suppression d’élément pour l’attribution des stratégies](media/IP-Delete-policy-assignment.png)
  
## <a name="delete-a-policy"></a><span data-ttu-id="0e5a4-254">Suppression d’une stratégie</span><span class="sxs-lookup"><span data-stu-id="0e5a4-254">Delete a policy</span></span>

<span data-ttu-id="0e5a4-p134">Vous ne pouvez pas supprimer une stratégie qui est en cours d’utilisation. Avant de supprimer une stratégie, vous devez tout d’abord supprimer toutes les affectations pour les collections de sites et modèles de collection de sites qui incluent cette stratégie, voir la section précédente.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-p134">You can't delete a policy that's in use. Before you can delete a policy, you first need to delete all assignments to site collections and site collection templates that include that policy—see the previous section.</span></span>
  
1. <span data-ttu-id="0e5a4-p135">Dans la sécurité &amp; centre de conformité \> choisissez **Gestion des données** \> **rétention** dans le volet de navigation gauche \> sous **Supprimer** \> **suppression de documents de gérer les stratégies pour SharePoint Online et OneDrive pour les entreprises**. Le centre de stratégie de suppression de Document s’ouvre dans un nouvel onglet de navigateur.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-p135">In the Security &amp; Compliance Center \> choose **Data management** \> **Retention** in the left navigation \> under **Delete** \> **Manage document deletion policies for SharePoint Online and OneDrive for Business**. The Document Deletion Policy Center opens in a new browser tab.</span></span>
    
2. <span data-ttu-id="0e5a4-259">Choisissez ** stratégies de suppression **.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-259">Choose ** Deletion Policies **.</span></span>
    
    ![Option de suppression des stratégies](media/IP-Deletion-Policies-option.png)
  
3. <span data-ttu-id="0e5a4-261">Sélectionnez la stratégie.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-261">Select the policy.</span></span>
    
4. <span data-ttu-id="0e5a4-262">Dans le ruban \> onglet **éléments** \> **Supprimer la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-262">On the Ribbon \> **Items** tab \> **Remove Policy**.</span></span>
    
    ![Bouton Supprimer la stratégie sur le ruban](media/IP-Remove-Policy-button-on-Ribbon.png)
  
5. <span data-ttu-id="0e5a4-p136">Si la stratégie est en cours d’utilisation, le système vous demandera si vous souhaitez supprimer la stratégie de toutes les collections de sites où il est utilisé. Si vous êtes sûr, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="0e5a4-p136">If the policy is in use, you'll be asked if you want to remove the policy from all of the site collections where it's being used. If you're sure, choose **OK**.</span></span>
    
    ![Message de confirmation de suppression de stratégie](media/IP-Delete-policy-confirmation.png)
  
## <a name="see-also"></a><span data-ttu-id="0e5a4-267">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e5a4-267">See also</span></span>

[<span data-ttu-id="0e5a4-268">Vue d’ensemble des stratégies de suppression de documents</span><span class="sxs-lookup"><span data-stu-id="0e5a4-268">Overview of document deletion policies</span></span>](document-deletion-policies.md)

[<span data-ttu-id="0e5a4-269">Application ou suppression d’une stratégie de suppression de documents pour un site</span><span class="sxs-lookup"><span data-stu-id="0e5a4-269">Apply or remove a document deletion policy for a site</span></span>](apply-or-remove-a-document-deletion-policy-for-a-site.md)
 

