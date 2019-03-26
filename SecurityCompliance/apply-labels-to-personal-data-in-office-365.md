---
title: Application d’étiquettes à des données personnelles dans Office 365
ms.author: bcarter
author: brendacarter
manager: laurawi
ms.date: ''
ms.audience: ITPro
ms.topic: overview
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
- GDPR
- M365-security-compliance
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
description: Découvrez comment utiliser des étiquettes Office dans le cadre de votre plan de protection RGPD.
ms.openlocfilehash: e31cd420fe476ace8031fc2c6e52158762814c7a
ms.sourcegitcommit: ef27da3ea5340d6e7a2eaa1288e2e005ef8e4788
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2019
ms.locfileid: "30789429"
---
# <a name="apply-labels-to-personal-data-in-office-365"></a><span data-ttu-id="aa585-103">Application d’étiquettes à des données personnelles dans Office 365</span><span class="sxs-lookup"><span data-stu-id="aa585-103">Apply labels to personal data in Office 365</span></span>

 <span data-ttu-id="aa585-104">Utilisez cette rubrique si vous utilisez des étiquettes de classification dans le cadre de votre plan de protection RGPD.</span><span class="sxs-lookup"><span data-stu-id="aa585-104">Use this topic if you are using classification labels as part of your GDPR protection plan.</span></span> 

<span data-ttu-id="aa585-105">Si vous utilisez des étiquettes pour la protection des données personnelles dans Office 365, Microsoft recommande que vous commenciez avec des[étiquettes de rétention](labels.md).</span><span class="sxs-lookup"><span data-stu-id="aa585-105">If you are using labels for protection of personal data in Office 365, Microsoft recommends you start with [retention labels](labels.md).</span></span> <span data-ttu-id="aa585-106">Avec les étiquettes de rétention, vous pouvez effectuer les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="aa585-106">With retention labels, you can:</span></span>
- <span data-ttu-id="aa585-107">La gouvernance des données avancée permet d’appliquer automatiquement des étiquettes basées sur les types d’informations sensibles ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="aa585-107">Use Advanced Data Governance to automatically apply labels based on sensitive information types or other criteria.</span></span>
-  <span data-ttu-id="aa585-108">Utilisez des étiquettes de rétention avec la protection contre la perte de données pour appliquer la protection.</span><span class="sxs-lookup"><span data-stu-id="aa585-108">Use retention labels with data loss prevention to apply protection.</span></span> 
- <span data-ttu-id="aa585-109">Utiliser des étiquettes avec eDiscovery et recherche de contenu.</span><span class="sxs-lookup"><span data-stu-id="aa585-109">Use labels with eDiscovery and Content Search.</span></span> 
- <span data-ttu-id="aa585-110">Utiliser des étiquettes et types d’informations sensibles avec Cloud App Security pour surveiller des données personnelles qui se trouvent dans d’autres applications SaaS.</span><span class="sxs-lookup"><span data-stu-id="aa585-110">Use both labels and sensitive information types with Cloud App Security to monitor personal data that resides in other SaaS apps.</span></span>

<span data-ttu-id="aa585-111">Les [Étiquettes de sensibilité](sensitivity-labels.md) sont actuellement recommandées pour appliquer des étiquettes à des fichiers en local et dans d’autres services cloud et fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="aa585-111">[Sensitivity labels](sensitivity-labels.md) are currently recommended for applying labels to files on premises and in other cloud services and providers.</span></span> <span data-ttu-id="aa585-112">Ceux-ci sont également recommandées pour les fichiers dans Office 365 nécessitant le chiffrement (point d’installation Azure Information Protection administrative) pour la protection des données, tels que les fichiers secrets commerciaux.</span><span class="sxs-lookup"><span data-stu-id="aa585-112">These are also recommended for files in Office 365 that require Azure Information Protection (AIP) encryption for data protection, such as trade secret files.</span></span>

<span data-ttu-id="aa585-113">À ce stade, à l’aide d’Azure Information Protection pour appliquer le chiffrement n’est pas recommandée pour les fichiers dans Office 365 avec des données qui est soumis à la RGPD.</span><span class="sxs-lookup"><span data-stu-id="aa585-113">At this time, using Azure Information Protection to apply Azure RMS encryption is not recommended for files in Office 365 with data that is subject to the GDPR. Office 365 services currently cannot read into RMS-encrypted files. Therefore, the service can’t find sensitive data in these files.</span></span> <span data-ttu-id="aa585-114">Les services Office 365 ne peuvent pas lire actuellement dans les fichiers d’installation administrative chiffrés.</span><span class="sxs-lookup"><span data-stu-id="aa585-114">Office 365 services currently cannot read into AIP-encrypted files.</span></span> <span data-ttu-id="aa585-115">Par conséquent, le service ne peut pas trouver des données sensibles dans ces fichiers.</span><span class="sxs-lookup"><span data-stu-id="aa585-115">Therefore, the service can’t find sensitive data in these files.</span></span>

<span data-ttu-id="aa585-116">Les étiquettes de sensibilité peuvent être appliquées à l’application courrier dans Exchange Online et ces étiquettes fonctionnent avec la prévention de perte de données Office 365.</span><span class="sxs-lookup"><span data-stu-id="aa585-116">Sensitivity labels can be applied to mail in Exchange Online and these labels work with Office 365 data loss prevention.</span></span> 

![Étiquettes Office 365 et étiquettes Azure Information Protection](Media/Apply-labels-to-personal-data-in-Office-365-image1.png)


<span data-ttu-id="aa585-118">Dans cette illustration :</span><span class="sxs-lookup"><span data-stu-id="aa585-118">In the illustration:</span></span>

-   <span data-ttu-id="aa585-119">Utilisez les étiquettes de rétention pour les données personnelles ou pour les fichiers contenant des données hautement réglementées et des secrets commerciaux dans SharePoint Online et OneDrive Entreprise.</span><span class="sxs-lookup"><span data-stu-id="aa585-119">Use Office 365 labels for personal data and for highly regulated & trade secret files in SharePoint Online and OneDrive for Business.</span></span>

-   <span data-ttu-id="aa585-120">Utilisez les étiquettes de sensibilité pour les fichiers contenant des données hautement réglementées et des secrets commerciaux, les e-mails Exchange Online, les fichiers dans d’autres services SaaS, les fichiers dans des centres de données en local et les fichiers dans d’autres fournisseurs cloud.</span><span class="sxs-lookup"><span data-stu-id="aa585-120">Use Azure Information Protection (AIP) labels for highly regulated & trade secret files, Exchange Online email, files in other SaaS services, files in on-premises datacenters, and files in other cloud providers.</span></span>


## <a name="use-retention-labels-and-sensitive-information-types-across-microsoft-365-for-information-protection"></a><span data-ttu-id="aa585-121">Utilisation des étiquettes Office et des types d’informations sensibles au sein de Microsoft 365 pour la protection des informations</span><span class="sxs-lookup"><span data-stu-id="aa585-121">Use Office labels and sensitive information types across Microsoft 365 for information protection</span></span>

<span data-ttu-id="aa585-122">L’image suivante montre comment les étiquettes Office et les types d’informations sensibles peuvent être utilisés dans les stratégies d’étiquetage, les stratégies de protection contre la perte de données et les stratégies Cloud App Security.</span><span class="sxs-lookup"><span data-stu-id="aa585-122">The following illustration shows how Office labels and sensitive information types can be used in label policies, data loss prevention policies, and with Cloud App Security policies.</span></span>

![Étiquettes Office et types d’informations sensibles](Media/Apply-labels-to-personal-data-in-Office-365-image2.png)

<span data-ttu-id="aa585-124">Concernant l’accessibilité, le tableau suivant fournit les mêmes exemples dans l’illustration.</span><span class="sxs-lookup"><span data-stu-id="aa585-124">For accessibility, the following table provides the same examples in the illustration.</span></span>

<table>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="aa585-125"><strong>Éléments de classification</strong></span><span class="sxs-lookup"><span data-stu-id="aa585-125"><strong>Classification elements</strong></span></span></th>
<th align="left"><span data-ttu-id="aa585-126"><strong>Stratégies d’étiquetage — 2 exemples</strong></span><span class="sxs-lookup"><span data-stu-id="aa585-126"><strong>Label policies — 2 examples</strong></span></span></th>
<th align="left"><span data-ttu-id="aa585-127"><strong>Stratégies de protection contre la perte de données — 2 exemples</strong></span><span class="sxs-lookup"><span data-stu-id="aa585-127"><strong>Data loss prevention policies — 2 examples</strong></span></span></th>
<th align="left"><span data-ttu-id="aa585-128"><strong>Stratégies Cloud App Security pour toutes les applications SaaS — 1 exemple</strong></span><span class="sxs-lookup"><span data-stu-id="aa585-128"><strong>Cloud App Security policies for all SaaS apps — 1 example</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><span data-ttu-id="aa585-129">Étiquettes de rétention.</span><span class="sxs-lookup"><span data-stu-id="aa585-129">Retention labels</span></span> <span data-ttu-id="aa585-130">Exemples : Personnel, Public, Données client, Données RH, Confidentiel, Hautement confidentiel</span><span class="sxs-lookup"><span data-stu-id="aa585-130">Office labels. Examples: Personal, Public, Customer data, HR data, Confidential, Highly confidential</span></span></td>
<td align="left"><p><span data-ttu-id="aa585-p105">Appliquer automatiquement l’étiquette...</span><span class="sxs-lookup"><span data-stu-id="aa585-p105">Auto apply this label . . .</span></span></p>
<p><span data-ttu-id="aa585-134">Données client</span><span class="sxs-lookup"><span data-stu-id="aa585-134">Customer data</span></span></p>
<p><span data-ttu-id="aa585-p106">... aux documents qui correspondent aux types d’informations sensibles...</span><span class="sxs-lookup"><span data-stu-id="aa585-p106">. . . to documents that match these sensitive information types . . .</span></span></p>
<p><span data-ttu-id="aa585-141">&lt;Liste des types d’informations sensibles disponibles&gt;</span><span class="sxs-lookup"><span data-stu-id="aa585-141">&lt;list of example sensitive information types&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="aa585-p107">Appliquer cette protection...</span><span class="sxs-lookup"><span data-stu-id="aa585-p107">Apply this protection . . .</span></span></p>
<p><span data-ttu-id="aa585-145">&lt;définir la protection&gt;</span><span class="sxs-lookup"><span data-stu-id="aa585-145">&lt;define protection&gt;</span></span></p>
<p><span data-ttu-id="aa585-p108">... à des documents avec cette étiquette...</span><span class="sxs-lookup"><span data-stu-id="aa585-p108">. . . to documents with this label . . .</span></span></p>
<p><span data-ttu-id="aa585-152">Données client</span><span class="sxs-lookup"><span data-stu-id="aa585-152">Customer data</span></span></p></td>
<td align="left"><p><span data-ttu-id="aa585-p109">Avertir quand des fichiers avec les attributs suivants...</span><span class="sxs-lookup"><span data-stu-id="aa585-p109">Alert when files with these attributes . . .</span></span></p>
<p><span data-ttu-id="aa585-156">&lt;attribut PII prédéfini ou expression personnalisée&gt;</span><span class="sxs-lookup"><span data-stu-id="aa585-156">&lt;predefined PII attribute -or- custom expression&gt;</span></span></p>
<p><span data-ttu-id="aa585-p110">... dans des applications SaaS approuvées sont partagés en dehors de l’organisation</span><span class="sxs-lookup"><span data-stu-id="aa585-p110">. . . in any sanctioned SaaS app are shared outside the organization</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="aa585-p111">Types d’informations sensibles. Exemples : numéro national belge, numéro de carte de crédit, numéro de carte d’identité en Croatie, ID national en Finlande</span><span class="sxs-lookup"><span data-stu-id="aa585-p111">Sensitive information types. Examples: Belgium National Number, Credit Card Number, Croatia Identity Cart Number, Finland National ID</span></span></td>
<td align="left"><p><span data-ttu-id="aa585-p112">Publiez ces étiquettes pour que les utilisateurs puissent les appliquer manuellement...</span><span class="sxs-lookup"><span data-stu-id="aa585-p112">Publish these labels for users to manually apply . . .</span></span></p>
<p><span data-ttu-id="aa585-166">&lt;sélectionner des étiquettes&gt;</span><span class="sxs-lookup"><span data-stu-id="aa585-166">&lt;select labels&gt;</span></span></p>
<p><span data-ttu-id="aa585-p113">... à ces emplacements...</span><span class="sxs-lookup"><span data-stu-id="aa585-p113">. . . to these locations . . .</span></span></p>
<p><span data-ttu-id="aa585-173">&lt;tous les emplacements ou choisir des emplacements spécifiques&gt;</span><span class="sxs-lookup"><span data-stu-id="aa585-173">&lt;all locations or choose specific locations&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="aa585-p114">Appliquer cette protection...</span><span class="sxs-lookup"><span data-stu-id="aa585-p114">Apply this protection . . .</span></span></p>
<p><span data-ttu-id="aa585-177">&lt;définir la protection&gt;</span><span class="sxs-lookup"><span data-stu-id="aa585-177">&lt;define protection&gt;</span></span></p>
<p><span data-ttu-id="aa585-p115">... aux documents qui correspondent à ces types d’informations sensibles&gt;</span><span class="sxs-lookup"><span data-stu-id="aa585-p115">. . . to documents that match these sensitive information types&gt;</span></span></p></td>
<td align="left"><span data-ttu-id="aa585-182">Remarque : les attributs prochainement disponibles pour Cloud App Security incluent les types d’informations sensibles Office 365 ainsi que les étiquettes unifiées dans Office 365 et Azure Information Protection.</span><span class="sxs-lookup"><span data-stu-id="aa585-182">Note: Attributes coming soon to Cloud App Security include Office 365 sensitive information types and Unified labels across Office 365 and Azure Information Protection.</span></span></td>
</tr>
</tbody>
</table>

## <a name="prioritize-auto-apply-label-policies"></a><span data-ttu-id="aa585-183">Hiérarchisation des stratégies d’étiquette à application automatique</span><span class="sxs-lookup"><span data-stu-id="aa585-183">Prioritize auto-apply label policies</span></span>

<span data-ttu-id="aa585-p116">Pour les données personnelles soumises au RGPD, Microsoft recommande l’application automatique des étiquettes à l’aide des types d’informations sensibles traités pour votre environnement. Il est important que les stratégies d’étiquettes à application automatique soient conçues correctement et testées pour s’assurer que le comportement attendu se produit.</span><span class="sxs-lookup"><span data-stu-id="aa585-p116">For personal data that is subject to GDPR, Microsoft recommends auto-applying labels by using the sensitive information types you curated for your environment. It is important that auto-apply label policies are well designed and tested to ensure the intended behavior occurs.</span></span>

<span data-ttu-id="aa585-p117">L’ordre de création des stratégies d’application automatique et leur utilisation ou non par les utilisateurs ont une incidence sur le résultat. Par conséquent, il est important de planifier avec soin le déploiement. Voici ce que vous devez savoir.</span><span class="sxs-lookup"><span data-stu-id="aa585-p117">The order that auto-apply policies are created and whether users are also applying these labels affect the result. So, it is important to carefully plan the roll-out. Here’s what you need to know.</span></span>

### <a name="one-label-at-a-time"></a><span data-ttu-id="aa585-188">Une seule étiquette à la fois</span><span class="sxs-lookup"><span data-stu-id="aa585-188">One label at a time</span></span>

<span data-ttu-id="aa585-189">Vous pouvez uniquement attribuer une seule étiquette à un document.</span><span class="sxs-lookup"><span data-stu-id="aa585-189">You can only assign one label to a document.</span></span>

### <a name="older-auto-apply-policies-win"></a><span data-ttu-id="aa585-190">Priorité des anciennes stratégies d’application automatique</span><span class="sxs-lookup"><span data-stu-id="aa585-190">Older auto-apply policies win</span></span>

<span data-ttu-id="aa585-p118">S’il existe plusieurs règles attribuant une étiquette à application automatique et si le contenu remplit les critères de plusieurs règles, l’étiquette de la règle la plus ancienne est attribuée. C’est pourquoi il est important de planifier les stratégies d’étiquette avec soin avant de les configurer. Si une organisation a besoin de modifier la priorité des stratégies d’étiquette, elle devra les supprimer et les recréer.</span><span class="sxs-lookup"><span data-stu-id="aa585-p118">If there are multiple rules that assign an auto-apply label and content meets the conditions of multiple rules, the label for the oldest rule is assigned. For this reason, it is important to plan the label policies carefully before configuring them. If an organization requires a change to the priority of the label policies, they will need to delete and recreate them.</span></span>

### <a name="manual-user-applied-labels-trump-auto-applied-labels"></a><span data-ttu-id="aa585-194">Priorité des étiquettes appliquées manuellement par l’utilisateur sur les étiquettes appliquées automatiquement</span><span class="sxs-lookup"><span data-stu-id="aa585-194">Manual user-applied labels trump auto-applied labels</span></span>

<span data-ttu-id="aa585-p119">Les étiquettes appliquées manuellement par l’utilisateur sont prioritaires sur les étiquettes appliquées automatiquement. Les stratégies d’application automatique ne peuvent pas remplacer une étiquette déjà appliquée par un utilisateur. Les utilisateurs peuvent remplacer les étiquettes qui sont appliquées automatiquement.</span><span class="sxs-lookup"><span data-stu-id="aa585-p119">Manual user applied labels trump auto-applied labels. Auto-apply policies cannot replace a label that is already applied by a user. Users can replace labels that are auto-applied.</span></span>

### <a name="auto-assigned-labels-can-be-updated"></a><span data-ttu-id="aa585-198">Possibilité de mise à jour des étiquettes attribuées automatiquement</span><span class="sxs-lookup"><span data-stu-id="aa585-198">Auto-assigned labels can be updated</span></span>

<span data-ttu-id="aa585-199">Les étiquettes attribuées automatiquement peuvent être mises à jour par de nouvelles stratégies d’étiquetage plus récentes ou par l’actualisation de stratégies existantes.</span><span class="sxs-lookup"><span data-stu-id="aa585-199">Auto-assigned labels can be updated by either newer label policies or by updates to existing policies.</span></span>

<span data-ttu-id="aa585-200">Assurez-vous que le plan d’implémentation des étiquettes inclut :</span><span class="sxs-lookup"><span data-stu-id="aa585-200">Be sure your plan for implementing labels includes:</span></span>

-   <span data-ttu-id="aa585-201">la priorisation de l’ordre dans lequel les stratégies d’application automatique sont créées ;</span><span class="sxs-lookup"><span data-stu-id="aa585-201">Prioritizing the order that auto-apply policies are created.</span></span>

-   <span data-ttu-id="aa585-p120">l’octroi de suffisamment de temps pour que les étiquettes soient automatiquement appliquées avant de les déployer pour que les utilisateurs puissent les appliquer manuellement. L’application des étiquettes à tout le contenu remplissant les conditions peut durer sept jours au maximum.</span><span class="sxs-lookup"><span data-stu-id="aa585-p120">Allowing enough time for labels to be automatically applied before rolling these out for users to manually apply. It can take up to seven days for the labels to be applied to all content that matches the conditions.</span></span>

### <a name="example-priority-for-creating-the-auto-apply-policies"></a><span data-ttu-id="aa585-204">Exemple de priorité permettant de créer des stratégies d’application automatique</span><span class="sxs-lookup"><span data-stu-id="aa585-204">Example priority for creating the auto-apply policies</span></span>

<table>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="aa585-205"><strong>Étiquettes</strong></span><span class="sxs-lookup"><span data-stu-id="aa585-205"><strong>Labels</strong></span></span></th>
<th align="left"><span data-ttu-id="aa585-206"><strong>Ordre de priorité pour la création de stratégie d’application automatique</strong></span><span class="sxs-lookup"><span data-stu-id="aa585-206"><strong>Priority order to create auto-apply policies</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><span data-ttu-id="aa585-207">Ressources humaines — Données des employés</span><span class="sxs-lookup"><span data-stu-id="aa585-207">Human Resources — Employee Data</span></span></td>
<td align="left"><span data-ttu-id="aa585-208">1</span><span class="sxs-lookup"><span data-stu-id="aa585-208">-1</span></span></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="aa585-209">Données client</span><span class="sxs-lookup"><span data-stu-id="aa585-209">Customer Data</span></span></td>
<td align="left"><span data-ttu-id="aa585-210">2</span><span class="sxs-lookup"><span data-stu-id="aa585-210">-2</span></span></td>
</tr>
<tr class="odd">
<td align="left"><span data-ttu-id="aa585-211">Hautement confidentiel</span><span class="sxs-lookup"><span data-stu-id="aa585-211">Highly Confidential</span></span></td>
<td align="left"><span data-ttu-id="aa585-212">3</span><span class="sxs-lookup"><span data-stu-id="aa585-212">-3</span></span></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="aa585-213">Ressources humaines — Données salariales</span><span class="sxs-lookup"><span data-stu-id="aa585-213">Human Resources — Salary Data</span></span></td>
<td align="left"><span data-ttu-id="aa585-214">4</span><span class="sxs-lookup"><span data-stu-id="aa585-214">4.</span></span></td>
</tr>
<tr class="odd">
<td align="left"><span data-ttu-id="aa585-215">Confidentiel</span><span class="sxs-lookup"><span data-stu-id="aa585-215">Confidential</span></span></td>
<td align="left"><span data-ttu-id="aa585-216">5</span><span class="sxs-lookup"><span data-stu-id="aa585-216">5.</span></span></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="aa585-217">Public</span><span class="sxs-lookup"><span data-stu-id="aa585-217">Public</span></span></td>
<td align="left"><span data-ttu-id="aa585-218">6</span><span class="sxs-lookup"><span data-stu-id="aa585-218">6.</span></span></td>
</tr>
<tr class="odd">
<td align="left"><span data-ttu-id="aa585-219">Personnelle</span><span class="sxs-lookup"><span data-stu-id="aa585-219">Personal</span></span></td>
<td align="left"><span data-ttu-id="aa585-220">Pas de stratégie d’application automatique</span><span class="sxs-lookup"><span data-stu-id="aa585-220">No auto-apply policy</span></span></td>
</tr>
</tbody>
</table>

## <a name="create-labels-and-auto-apply-label-policies"></a><span data-ttu-id="aa585-221">Création d’étiquettes et de stratégies d’étiquetage à application automatique</span><span class="sxs-lookup"><span data-stu-id="aa585-221">Create labels and auto-apply label policies</span></span>

<span data-ttu-id="aa585-222">Créez des étiquettes et des stratégies dans le Centre de sécurité et de conformité.</span><span class="sxs-lookup"><span data-stu-id="aa585-222">Create labels and policies in the Security & Compliance Center.</span></span>

<table>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="aa585-223"><strong>Étape</strong></span><span class="sxs-lookup"><span data-stu-id="aa585-223"><strong>Step</strong></span></span></th>
<th align="left"><span data-ttu-id="aa585-224"><strong>Description</strong></span><span class="sxs-lookup"><span data-stu-id="aa585-224"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="aa585-225">Accordez des autorisations aux membres de votre équipe de conformité.</span><span class="sxs-lookup"><span data-stu-id="aa585-225">Give permissions to members of your compliance team.</span></span></p></td>
<td align="left"><p><span data-ttu-id="aa585-p121">Les membres de votre équipe de conformité qui créent des étiquettes ont besoin d’autorisations pour utiliser le Centre de sécurité &amp; de conformité. Accédez à des Autorisations dans le Centre de sécurité et de conformité et modifiez les membres du groupe Administrateur de conformité.</span><span class="sxs-lookup"><span data-stu-id="aa585-p121">Members of your compliance team who will create labels need permissions to use the Security &amp; Compliance Center. Go to Permissions in Security and Compliance Center and modify the members of the Compliance Administrator group.</span></span></p>
<p><span data-ttu-id="aa585-228">Reportez-vous à la rubrique <a href="https://support.office.com/en-ie/article/Give-users-access-to-the-Office-365-Security-Compliance-Center-2cfce2c8-20c5-47f9-afc4-24b059c1bd76">Octroi de l’accès au Centre de sécurité &amp; de conformité Office 365 aux utilisateurs</a>.</span><span class="sxs-lookup"><span data-stu-id="aa585-228">See <a href="https://support.office.com/en-ie/article/Give-users-access-to-the-Office-365-Security-Compliance-Center-2cfce2c8-20c5-47f9-afc4-24b059c1bd76">Give users access to the Office 365 Security &amp; Compliance Center</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="aa585-229">Créer des étiquettes de rétention.</span><span class="sxs-lookup"><span data-stu-id="aa585-229">Create retention labels.</span></span></p></td>
<td align="left"><span data-ttu-id="aa585-230">Accédez à Classifications dans le Centre de sécurité et de conformité, sélectionnez Étiquettes, puis créez des étiquettes pour votre environnement.</span><span class="sxs-lookup"><span data-stu-id="aa585-230">Go to Classifications in Security and Compliance Center, choose Labels, and create the labels for your environment.</span></span></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="aa585-231">Créez des stratégies d’application automatique pour les étiquettes.</span><span class="sxs-lookup"><span data-stu-id="aa585-231">Create auto-apply policies for labels.</span></span></p></td>
<td align="left"><span data-ttu-id="aa585-p122">Accédez à Classification dans le Centre de sécurité et de conformité, sélectionnez les stratégies d’étiquetage et créez les stratégies d’application automatique des étiquettes. Veillez à créer ces stratégies par ordre de priorité.</span><span class="sxs-lookup"><span data-stu-id="aa585-p122">Go to Classification in Security and Compliance Center, choose Label policies, and create the policies for auto-applying labels. Be sure to create these policies in the prioritized order.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="aa585-234">L’image suivante montre comment créer une étiquette à application automatique pour l’étiquette de données Client.</span><span class="sxs-lookup"><span data-stu-id="aa585-234">The following illustration shows how to create an auto-apply label for the Customer data label.</span></span>

![Création et application d’étiquette pour des données client](Media/Apply-labels-to-personal-data-in-Office-365-image3.png)

<span data-ttu-id="aa585-236">Dans cette illustration :</span><span class="sxs-lookup"><span data-stu-id="aa585-236">In the illustration:</span></span>

-   <span data-ttu-id="aa585-237">L’étiquette « Données client » est créée.</span><span class="sxs-lookup"><span data-stu-id="aa585-237">The “Customer data” label is created.</span></span>

-   <span data-ttu-id="aa585-238">Les types d’informations sensibles souhaitée pour le RGPD sont répertoriées : numéro national belge, numéro de carte de crédit, numéro de carte d’identité en Croatie, ID national en Finlande</span><span class="sxs-lookup"><span data-stu-id="aa585-238">The desired sensitive information types for GDPR are listed: Belgium National Number, Credit Card Number, Croatia Identity Card Number, Finland National ID.</span></span>

-   <span data-ttu-id="aa585-239">La création d’une stratégie d’application automatique attribue l’étiquette « Données client » à tous les fichiers qui incluent un des types d’informations sensibles que vous ajoutez à la stratégie.</span><span class="sxs-lookup"><span data-stu-id="aa585-239">Create an auto-apply policy assigns the label “Customer data” to any file that includes one of the sensitive information types that you add to the policy.</span></span>
