---
title: Recherche et localisation des données personnelles
ms.author: bcarter
author: brendacarter
manager: laurawi
ms.date: 2/7/2018
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
description: Découvrez comment rechercher et localiser des données personnelles dans Office 365.
ms.openlocfilehash: 3c2981116e2abb3518a132084a697618ef3261cc
ms.sourcegitcommit: 54d58da1777eb83adb82826d1bb1adb94903c8e1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2019
ms.locfileid: "30955177"
---
# <a name="search-for-and-find-personal-data"></a><span data-ttu-id="16206-103">Recherche et localisation des données personnelles</span><span class="sxs-lookup"><span data-stu-id="16206-103">Search for and find personal data</span></span>

<span data-ttu-id="16206-104">Les données personnelles sont définies à très grande échelle dans le cadre du RGPD comme les données associées à une personne naturelle identifiée ou identifiable qui est résidente de l’Union européenne (UE).</span><span class="sxs-lookup"><span data-stu-id="16206-104">Personal data is defined very broadly under the GDPR as any data that relates to an identified or identifiable natural person that is a resident of the European Union (EU).</span></span>

<span data-ttu-id="16206-105">Article 4 - Définitions</span><span class="sxs-lookup"><span data-stu-id="16206-105">Article 4 – Definitions</span></span>

> <span data-ttu-id="16206-106">Les « données personnelles » correspondent aux informations relatives à une personne naturelle identifiée ou identifiable (« la personne concernée ») ; une personne naturelle identifiable est une personne qui peut être identifiée, directement ou indirectement, notamment par référence à un identificateur par exemple, un nom, un numéro d’identification, des données de localisation, un identificateur en ligne, ou un ou plusieurs facteurs spécifiques de l’identité physique, physiologique, génétique, mentale, économique, culturelle ou sociale de cette personne naturelle ;</span><span class="sxs-lookup"><span data-stu-id="16206-106">‘personal data’ means any information relating to an identified or identifiable natural person (‘data subject’); an identifiable natural person is one who can be identified, directly or indirectly, in particular by reference to an identifier such as a name, an identification number, location data, an online identifier or to one or more factors specific to the physical, physiological, genetic, mental, economic, cultural or social identity of that natural person;</span></span>

<span data-ttu-id="16206-107">Cet article explique comment rechercher des données personnelles stockées dans SharePoint Online et OneDrive Entreprise (qui inclut les sites de tous les groupes Office 365 et Microsoft Teams).</span><span class="sxs-lookup"><span data-stu-id="16206-107">This article demonstrates how to find personal data stored in SharePoint Online and OneDrive for Business (which includes the sites for all Office 365 groups and Microsoft Teams).</span></span>

<span data-ttu-id="16206-p101">La recherche de données personnelles soumises au RGPD repose sur l’utilisation de types d’informations sensibles dans Office 365. Ceux-ci définissent comment le processus automatisé reconnaît des types d’informations spécifiques tels que les numéros de sécurité sociale et les numéros de carte de crédit. Pour l’instant, ils ne permettent pas de rechercher des données dans les boîtes aux lettres Exchange au repos. Toutefois, les types d’informations sensibles peuvent être utilisés avec des stratégies de protection contre la perte de données pour rechercher des données personnelles dans le courrier en transit.</span><span class="sxs-lookup"><span data-stu-id="16206-p101">Finding personal data subject to GDPR relies on using sensitive information types in Office 365. These define how the automated process recognizes specific information types such as health service numbers and credit card numbers. At this time these cannot be used to find data in Exchange mailboxes at rest. However, sensitive information types can be used with data loss prevention policies to find personal data in mail while in transit.</span></span>

<span data-ttu-id="16206-112">Par conséquent, même si vous ne pouvez pas utiliser actuellement la recherche de contenu pour rechercher des données personnelles au repos dans les boîtes aux lettres Exchange Online, vous pouvez utiliser les types d’informations sensibles que vous gérez pour le RGPD pour rechercher et protéger des informations personnelles lors de leur envoi par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="16206-112">So, while you can’t currently use Content Search to find personal data at rest in Exchange Online mailboxes, you can use the sensitive information types you curate for GDPR to find and protect personal information as it is sent through email.</span></span>

## <a name="use-content-search-to-find-personal-data"></a><span data-ttu-id="16206-113">Utilisation de la recherche de contenu pour rechercher des données personnelles</span><span class="sxs-lookup"><span data-stu-id="16206-113">Use Content Search to find personal data</span></span>

<span data-ttu-id="16206-p102">Microsoft recommande d’utiliser une approche en trois étapes pour rechercher des données personnelles dans Office 365. Le reste de cette rubrique fournit des instructions pour chacune de ces étapes.</span><span class="sxs-lookup"><span data-stu-id="16206-p102">Microsoft recommends a three-stage approach to finding personal data in Office 365. The rest of this topic provides guidance for each of these stages.</span></span>

<table>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="16206-116"><strong>Étape</strong></span><span class="sxs-lookup"><span data-stu-id="16206-116"><strong>Step</strong></span></span></th>
<th align="left"><span data-ttu-id="16206-117"><strong>Description</strong></span><span class="sxs-lookup"><span data-stu-id="16206-117"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="16206-118">1. Recherche des types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="16206-118">1. Search for sensitive information types</span></span></p></td>
<td align="left"><p><span data-ttu-id="16206-p103">Commencez par utiliser des types d’informations sensibles pour rechercher des données personnelles. Créez une requête de recherche de contenu pour chaque type d’informations sensibles. Exécutez la requête et analysez les résultats.</span><span class="sxs-lookup"><span data-stu-id="16206-p103">Start by using sensitive information types to find personal data. Create a Content Search query for each sensitive information type. Run the query and analyze the results.</span></span></p>
<span data-ttu-id="16206-122">Si nécessaire, ajoutez des paramètres à la requête afin de réduire les faux positifs :</span><span class="sxs-lookup"><span data-stu-id="16206-122">If needed, add parameters to the query to reduce false positives:</span></span> <li><span data-ttu-id="16206-123">Plage de nombre</span><span class="sxs-lookup"><span data-stu-id="16206-123">Count range</span></span></li>
    <li><span data-ttu-id="16206-124">Plage de confiance</span><span class="sxs-lookup"><span data-stu-id="16206-124">Confidence range</span></span></li>
    <li><span data-ttu-id="16206-125">Autres propriétés ou opérateurs pour des requêtes plus complexes</span><span class="sxs-lookup"><span data-stu-id="16206-125">Other properties or operators for more complex queries</span></span></li>
<p><span data-ttu-id="16206-126">Si nécessaire, modifiez un type d’informations sensibles pour améliorer la précision pour votre organisation :</span><span class="sxs-lookup"><span data-stu-id="16206-126">If necessary, modify a sensitive information type to improve accuracy for your organization:</span></span></p>
<p><li><span data-ttu-id="16206-127">Ajustez le niveau de confiance directement dans le fichier XML.</span><span class="sxs-lookup"><span data-stu-id="16206-127">Adjust the confidence level directly in the XML.</span></span></li></p>
<p><li><span data-ttu-id="16206-128">Ajoutez des mots-clés.</span><span class="sxs-lookup"><span data-stu-id="16206-128">Add key words.</span></span></li></p>
<p><li><span data-ttu-id="16206-129">Ajustez les exigences de proximité pour les mots-clés.</span><span class="sxs-lookup"><span data-stu-id="16206-129">Adjust the proximity requirements for keywords.</span></span></li></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="16206-130">2. Utilisation du langage de requête de mot-clé (KQL) pour rechercher des données personnelles supplémentaires dans votre environnement</span><span class="sxs-lookup"><span data-stu-id="16206-130">2. Use Keyword Query Language (KQL) to find additional personal data in your environment</span></span></p></td>
<td align="left"><p><span data-ttu-id="16206-131">Pour rechercher des données qui ne sont pas incluses dans des types d’informations sensibles, utilisez le langage de requête de mot-clé KQL pour développer des requêtes personnalisées.</span><span class="sxs-lookup"><span data-stu-id="16206-131">To find data not included in sensitive information types, use the KQL query language to develop custom queries.</span></span></p>
<p><span data-ttu-id="16206-132">Testez les résultats de ces recherches et ajustez la chaîne de requête KQL jusqu'à ce que vous obteniez le résultat attendu.</span><span class="sxs-lookup"><span data-stu-id="16206-132">Test the results of these searches and adjust the KQL query string until you achieve the expected result.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="16206-133">3. Création de types d’informations sensibles personnalisés à l’aide de requêtes KQL</span><span class="sxs-lookup"><span data-stu-id="16206-133">3. Create new custom sensitive information types using the KQL queries</span></span></p></td>
<td align="left"><span data-ttu-id="16206-p104">Après avoir optimisé des requêtes KQL pour rechercher des données cibles, créez des types d’informations sensibles personnalisés à l’aide de ces requêtes. Vous pouvez ensuite utiliser ces types d’informations sensibles personnalisés avec la recherche de contenu, dans les stratégies DLP et d’autres outils, ainsi que dans d’autres requêtes KQL.</span><span class="sxs-lookup"><span data-stu-id="16206-p104">After optimizing KQL queries to find target data, create new custom sensitive information types using these queries. You can then use these custom sensitive information types with Content Search, in DLP policies and other tools, and within other KQL queries.</span></span></td>
</tr>
</tbody>
</table>


## <a name="search-for-sensitive-information-types-using-content-search"></a><span data-ttu-id="16206-136">Recherche des types d’informations sensibles à l’aide de la recherche de contenu</span><span class="sxs-lookup"><span data-stu-id="16206-136">Search for sensitive information types using Content Search</span></span>

<span data-ttu-id="16206-137">Commencer la recherche en utilisant les types d’informations sensibles incluses dans Office 365 pour les données personnelles.</span><span class="sxs-lookup"><span data-stu-id="16206-137">Begin searching for personal data by using the sensitive information types that are included with Office 365. These are listed in the Security and Compliance Center under Classification.</span></span> <span data-ttu-id="16206-138">Celles-ci sont répertoriées sous Classification dans le centre de sécurité et le centre de conformité.</span><span class="sxs-lookup"><span data-stu-id="16206-138">These are listed under Classification in the security center and compliance center.</span></span>

<span data-ttu-id="16206-139">Cette rubrique inclut une liste de certains types d’informations sensibles qui s’appliquent aux citoyens dans l’Union européenne.</span><span class="sxs-lookup"><span data-stu-id="16206-139">This topic includes a list of some sensitive information types that apply to citizens in the European Union.</span></span> <span data-ttu-id="16206-140">Vérifiez le centre de sécurité ou le centre de conformité pour les nouveaux ajouts qui peuvent vous aider avec la mise en conformité RGPD.</span><span class="sxs-lookup"><span data-stu-id="16206-140">Check the security center or the compliance center for new additions that can help with GDPR compliance.</span></span>

<span data-ttu-id="16206-141">Consultez également l’article relatif à la [liste des types d’informations sensibles et à ce qu’ils recherchent](https://support.office.com/fr-FR/article/What-the-sensitive-information-types-look-for-fd505979-76be-4d9f-b459-abef3fc9e86b).</span><span class="sxs-lookup"><span data-stu-id="16206-141">Also see this article: [List of sensitive information types and what each one looks for](https://support.office.com/fr-FR/article/What-the-sensitive-information-types-look-for-fd505979-76be-4d9f-b459-abef3fc9e86b).</span></span>

<span data-ttu-id="16206-p107">Les types d’informations sensibles définissent la façon dont le processus automatisé reconnaît des types d’informations spécifiques tels que les numéros de compte bancaire, de sécurité sociale et de carte de crédit. Les types d’informations sensibles sont également appelés conditions. Un type d’informations sensibles est défini par un modèle qui peut être identifié par une fonction ou une expression régulière. En outre, des preuves corroborantes comme les mots-clés et les sommes de contrôle peuvent être utilisées pour identifier un type d’informations sensibles. La proximité et le niveau de confiance sont également utilisés dans le processus d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="16206-p107">Sensitive information types define how the automated process recognizes specific information types such as bank account numbers, health service numbers, and credit card numbers. Sensitive information types are also referred to as conditions. A sensitive information type is defined by a pattern that can be identified by a regular expression or a function. In addition, corroborative evidence such as keywords and checksums can be used to identify a sensitive information type. Confidence level and proximity are also used in the evaluation process.</span></span>

<span data-ttu-id="16206-147">Pour l’instant, les types d’informations sensibles ne permettent pas de rechercher des données au repos dans les boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="16206-147">At this time sensitive information types cannot be used to find data at rest in mailboxes.</span></span>

### <a name="using-content-search-with-sensitive-information-types"></a><span data-ttu-id="16206-148">Utilisation de la recherche de contenu avec des types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="16206-148">Using Content Search with sensitive information types</span></span>

<table>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="16206-149"><strong>Étape</strong></span><span class="sxs-lookup"><span data-stu-id="16206-149"><strong>Step</strong></span></span></th>
<th align="left"><span data-ttu-id="16206-150"><strong>Plus d’informations</strong></span><span class="sxs-lookup"><span data-stu-id="16206-150"><strong>More information</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd"><td align="left"><p><span data-ttu-id="16206-151">Accédez à Recherche de contenu dans le Centre de sécurité et de conformité</span><span class="sxs-lookup"><span data-stu-id="16206-151">Go to Content Search in the Security and Compliance Center</span></span></p></td>
<td align="left"><p><span data-ttu-id="16206-152">Dans le volet gauche du Centre de sécurité et de conformité, cliquez sur **Recherches &amp; enquêtes** &gt; **Recherche de contenu**.</span><span class="sxs-lookup"><span data-stu-id="16206-152">In the left pane of the Security &amp; Compliance Center, click **Search &amp; investigation** &gt; **Content search**.</span></span></p>
<p><span data-ttu-id="16206-153">Reportez-vous à la rubrique <a href="https://support.office.com/en-us/article/Run-a-Content-Search-in-the-Office-365-Security-Compliance-Center-61852fd9-fe8a-4880-a339-cb19ed3bff4a">Exécuter une recherche de contenu dans le Centre de sécurité et de conformité Office 365</a>.</span><span class="sxs-lookup"><span data-stu-id="16206-153">See <a href="https://support.office.com/en-us/article/Run-a-Content-Search-in-the-Office-365-Security-Compliance-Center-61852fd9-fe8a-4880-a339-cb19ed3bff4a">Run a Content Search in the Office 365 Security &amp; Compliance Center</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="16206-154">Création d’un élément de recherche pour chaque type d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="16206-154">Create a new search item for each sensitive information type</span></span></p></td>
<td align="left"><p><span data-ttu-id="16206-155">Utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="16206-155">Use the following syntax:</span></span></p>
<blockquote>
<p><span data-ttu-id="16206-156">SensitiveType:”&lt;type&gt;”</span><span class="sxs-lookup"><span data-stu-id="16206-156">SensitiveType:”&lt;type&gt;”</span></span></p>
</blockquote>
<p><span data-ttu-id="16206-157">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="16206-157">For example:</span></span></p>
<blockquote>
<p><span data-ttu-id="16206-158">SensitiveType:&quot;Numéro de passeport français&quot;</span><span class="sxs-lookup"><span data-stu-id="16206-158">SensitiveType:&quot;France Passport Number&quot;</span></span></p>
</blockquote>
<p><span data-ttu-id="16206-p108">Étendue de la recherche Scope dans SharePoint (inclut OneDrive Entreprise). Vérifiez que la syntaxe est exacte et qu’il n’y a pas d’espaces supplémentaires ni de fautes de frappe.</span><span class="sxs-lookup"><span data-stu-id="16206-p108">Scope the search to SharePoint (includes OneDrive for Business). Make sure the syntax is exact and there are no extra spaces or typos.</span></span></p>
<p><span data-ttu-id="16206-161">Reportez-vous à la rubrique relative à la <a href="https://support.office.com/fr-FR/article/Form-a-query-to-find-sensitive-data-stored-on-sites-3019fbc5-7f15-4972-8d0e-dc182dc7f836">création d’une requête pour rechercher des données sensibles stockées sur des sites</a>.</span><span class="sxs-lookup"><span data-stu-id="16206-161">See <a href="https://support.office.com/fr-FR/article/Form-a-query-to-find-sensitive-data-stored-on-sites-3019fbc5-7f15-4972-8d0e-dc182dc7f836">Form a query to find sensitive data stored on sites</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="16206-162">Analyse des résultats pour chaque recherche</span><span class="sxs-lookup"><span data-stu-id="16206-162">Review the results for each search</span></span></p></td>
<td align="left"><p><span data-ttu-id="16206-163">Recherchez ces types de problèmes pour déterminer si la précision de la requête est un objectif :</span><span class="sxs-lookup"><span data-stu-id="16206-163">Look for these types of issues to determine if the query accuracy is on target:</span></span></p>
<p><li><span data-ttu-id="16206-164">De nombreux faux positifs</span><span class="sxs-lookup"><span data-stu-id="16206-164">Many false positives</span></span></li></p>
<p><li><span data-ttu-id="16206-165">Instances de données connues manquantes</span><span class="sxs-lookup"><span data-stu-id="16206-165">Missing known instances of data</span></span></li></p>
<p><span data-ttu-id="16206-166">Reportez-vous à la rubrique relative à l’<a href="https://support.office.com/en-us/article/Export-Content-Search-results-from-the-Office-365-Security-Compliance-Center-ed48d448-3714-4c42-85f5-10f75f6a4278">exportation des résultats de la recherche de contenu du Centre de sécurité et de conformité Office 365</a>.</span><span class="sxs-lookup"><span data-stu-id="16206-166">See <a href="https://support.office.com/en-us/article/Export-Content-Search-results-from-the-Office-365-Security-Compliance-Center-ed48d448-3714-4c42-85f5-10f75f6a4278">Export Content Search results from the Office 365 Security &amp; Compliance Center</a>.</span></span></p>
<p><span data-ttu-id="16206-167">Remarque : si vous utilisez Mozilla Firefox ou Chrome, il se peut que vous deviez d’abord télécharger des rapports avec Internet Explorer ou Edge pour installer le complément requis.</span><span class="sxs-lookup"><span data-stu-id="16206-167">Note: if you’re using Mozilla Firefox or Chrome, you might need to first download reports using Internet Explorer or Edge in order to install the required add-in.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="sensitive-information-types-for-eu-citizen-data"></a><span data-ttu-id="16206-168">Types d’informations sensibles pour les données des citoyens européens</span><span class="sxs-lookup"><span data-stu-id="16206-168">Sensitive information types for EU citizen data</span></span>

<span data-ttu-id="16206-p109">Commencez par ces types d’informations sensibles. De nombreux autres types d’informations sensibles seront disponibles prochainement pour les données personnelles dans les pays de l’UE.</span><span class="sxs-lookup"><span data-stu-id="16206-p109">Start with these sensitive information types. Many more sensitive information types are coming soon for personal data in EU countries.</span></span>

> <span data-ttu-id="16206-171">Numéro national belge</span><span class="sxs-lookup"><span data-stu-id="16206-171">Belgium National Number</span></span>
>
> <span data-ttu-id="16206-172">Numéro de carte de crédit</span><span class="sxs-lookup"><span data-stu-id="16206-172">Credit Card Number</span></span>
>
> <span data-ttu-id="16206-173">Numéro de carte d’identité croate</span><span class="sxs-lookup"><span data-stu-id="16206-173">Croatia Identity Card Number</span></span>
>
> <span data-ttu-id="16206-174">Numéro d’identification personnelle croate (OIB)</span><span class="sxs-lookup"><span data-stu-id="16206-174">Croatia Personal Identification (OIB) Number</span></span>
>
> <span data-ttu-id="16206-175">Numéro de carte d’identité nationale tchèque</span><span class="sxs-lookup"><span data-stu-id="16206-175">Czech National Identity Card Number</span></span>
>
> <span data-ttu-id="16206-176">Numéro d’identification personnelle danois</span><span class="sxs-lookup"><span data-stu-id="16206-176">Denmark Personal Identification Number</span></span>
>
> <span data-ttu-id="16206-177">Numéro de carte de crédit de l'U.E.</span><span class="sxs-lookup"><span data-stu-id="16206-177">EU Debit Card Number</span></span>
>
> <span data-ttu-id="16206-178">Numéro d'identification national finlandais</span><span class="sxs-lookup"><span data-stu-id="16206-178">Finland National ID</span></span>
>
> <span data-ttu-id="16206-179">Numéro de passeport finlandais</span><span class="sxs-lookup"><span data-stu-id="16206-179">Finland Passport Number</span></span>
>
> <span data-ttu-id="16206-180">Numéro de permis de conduire français</span><span class="sxs-lookup"><span data-stu-id="16206-180">France Driver's License Number</span></span>
>
> <span data-ttu-id="16206-181">Carte nationale d'identité (CNI) française</span><span class="sxs-lookup"><span data-stu-id="16206-181">France National ID Card (CNI)</span></span>
>
> <span data-ttu-id="16206-182">Numéro de passeport français</span><span class="sxs-lookup"><span data-stu-id="16206-182">France Passport Number</span></span>
>
> <span data-ttu-id="16206-183">Numéro de sécurité sociale (INSEE) français</span><span class="sxs-lookup"><span data-stu-id="16206-183">France Social Security Number (INSEE)</span></span>
>
> <span data-ttu-id="16206-184">Numéro de permis de conduire allemand</span><span class="sxs-lookup"><span data-stu-id="16206-184">German Driver’s License Number</span></span>
>
> <span data-ttu-id="16206-185">Numéro de carte d’identité allemand</span><span class="sxs-lookup"><span data-stu-id="16206-185">Germany Identity Card Number</span></span>
>
> <span data-ttu-id="16206-186">Numéro de passeport allemand</span><span class="sxs-lookup"><span data-stu-id="16206-186">German Passport Number</span></span>
>
> <span data-ttu-id="16206-187">Carte d’identité nationale grecque</span><span class="sxs-lookup"><span data-stu-id="16206-187">Greece National ID Card</span></span>
>
> <span data-ttu-id="16206-188">Numéro de compte international (IBAN)</span><span class="sxs-lookup"><span data-stu-id="16206-188">International Banking Account Number (IBAN)</span></span>
>
> <span data-ttu-id="16206-189">Adresse IP</span><span class="sxs-lookup"><span data-stu-id="16206-189">IP Address</span></span>
>
> <span data-ttu-id="16206-190">Numéro personnel pour le service public irlandais (PPS)</span><span class="sxs-lookup"><span data-stu-id="16206-190">Ireland Personal Public Service (PPS) Number</span></span>
>
> <span data-ttu-id="16206-191">Numéro de permis de conduire italien</span><span class="sxs-lookup"><span data-stu-id="16206-191">Italy’s Driver’s License Number</span></span>
>
> <span data-ttu-id="16206-192">Numéro de service des citoyens hollandais (BSN)</span><span class="sxs-lookup"><span data-stu-id="16206-192">Netherlands Citizen’s Service (BSN) Number</span></span>
>
> <span data-ttu-id="16206-193">Numéro d’identité norvégien</span><span class="sxs-lookup"><span data-stu-id="16206-193">Norway Identity Number</span></span>
>
> <span data-ttu-id="16206-194">Carte d'identité polonaise</span><span class="sxs-lookup"><span data-stu-id="16206-194">Poland Identity Card</span></span>
>
> <span data-ttu-id="16206-195">Numéro d'identification national polonais (PESEL)</span><span class="sxs-lookup"><span data-stu-id="16206-195">Poland National ID (PESEL)</span></span>
>
> <span data-ttu-id="16206-196">Numéro de passeport polonais</span><span class="sxs-lookup"><span data-stu-id="16206-196">Poland Passport</span></span>
>
> <span data-ttu-id="16206-197">Numéro de carte de citoyen portugais</span><span class="sxs-lookup"><span data-stu-id="16206-197">Portugal Citizen Card Number</span></span>
>
> <span data-ttu-id="16206-198">Numéro de sécurité sociale (N° S.S.) espagnol</span><span class="sxs-lookup"><span data-stu-id="16206-198">Spain Social Security Number (SSN)</span></span>
>
> <span data-ttu-id="16206-199">ID national suédois</span><span class="sxs-lookup"><span data-stu-id="16206-199">Sweden National ID</span></span>
>
> <span data-ttu-id="16206-200">Numéro de passeport suédois</span><span class="sxs-lookup"><span data-stu-id="16206-200">Sweden Passport Number</span></span>
>
> <span data-ttu-id="16206-p110">Numéro de permis de conduire britannique</span><span class="sxs-lookup"><span data-stu-id="16206-p110">U.K. Driver’s License Number</span></span>
>
> <span data-ttu-id="16206-p111">Numéro de liste électorale du Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="16206-p111">U.K. Electoral Roll Number</span></span>
>
> <span data-ttu-id="16206-p112">Numéro du service de santé national (NHS) du Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="16206-p112">U.K. National Health Service Number</span></span>
>
> <span data-ttu-id="16206-p113">Numéro d'assurance national (NINO) du Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="16206-p113">U.K. National Insurance Number (NINO)</span></span>
>
> <span data-ttu-id="16206-p114">Numéro de passeport des États-Unis/du Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="16206-p114">U.S./U.K. Passport Number</span></span>

## <a name="add-parameters-to-a-sensitive-information-type-query-to-hone-the-results"></a><span data-ttu-id="16206-211">Ajout de paramètres à une requête de type d’informations sensibles pour affiner les résultats</span><span class="sxs-lookup"><span data-stu-id="16206-211">Add parameters to a sensitive information type query to hone the results</span></span>

<span data-ttu-id="16206-212">Vous pouvez ajouter ces paramètres à une requête de type d’informations sensibles :</span><span class="sxs-lookup"><span data-stu-id="16206-212">You can add these parameters to a sensitive information type query:</span></span>

-   <span data-ttu-id="16206-213">Plage de nombre : définit le nombre d'occurrences des informations sensibles qu'un document doit contenir avant qu'il ne soit inclus dans les résultats de la requête.</span><span class="sxs-lookup"><span data-stu-id="16206-213">Count range — define the number of occurrences of sensitive information a document needs to contain before it’s included in the query results.</span></span>

-   <span data-ttu-id="16206-214">Plage de confiance : niveau de confiance auquel le type d'informations sensibles détecté correspond réellement (par exemple, 85 (85 %)).</span><span class="sxs-lookup"><span data-stu-id="16206-214">Confidence range — the level of confidence that the detected sensitive type is actually a match, such as 85 (85%).</span></span>

<span data-ttu-id="16206-215">Syntaxe :</span><span class="sxs-lookup"><span data-stu-id="16206-215">Syntax:</span></span>

-   <span data-ttu-id="16206-216">SensitiveType:”\<type\>|\<count range\>|\<confidence range\>”</span><span class="sxs-lookup"><span data-stu-id="16206-216">SensitiveType:”\<type\>|\<count range\>|\<confidence range\>”</span></span>

<span data-ttu-id="16206-217">Exemples :</span><span class="sxs-lookup"><span data-stu-id="16206-217">Examples:</span></span>

-   <span data-ttu-id="16206-218">SensitiveType:“Numéro de carte de crédit|5” (renvoie uniquement les documents qui contiennent exactement cinq numéros de carte de crédit)</span><span class="sxs-lookup"><span data-stu-id="16206-218">SensitiveType:“Credit Card Number|5” (return only documents that contain exactly five credit card numbers)</span></span>

-   <span data-ttu-id="16206-p115">SensitiveType:“Numéro de carte de crédit|\*|85..” (la plage de confiance est de 85 % ou supérieure)</span><span class="sxs-lookup"><span data-stu-id="16206-p115">SensitiveType:“Credit Card Number|\*|85..” (confidence range is 85 percent or higher)</span></span>

<span data-ttu-id="16206-221">Remarque : “SensitiveType” est sensible à la casse, mais le reste de la requête ne l’est pas.</span><span class="sxs-lookup"><span data-stu-id="16206-221">Note: “SensitiveType” is case sensitive, but the rest of the query is not.</span></span>

<span data-ttu-id="16206-p116">Vous pouvez également utiliser des propriétés et des opérateurs pour illustrer la façon dont vous pouvez affiner vos requêtes. Pour plus d’informations et des exemples, reportez-vous à la rubrique relative à la [création d’une requête pour rechercher des données sensibles stockées sur des sites](https://support.office.com/fr-FR/article/Form-a-query-to-find-sensitive-data-stored-on-sites-3019fbc5-7f15-4972-8d0e-dc182dc7f836).</span><span class="sxs-lookup"><span data-stu-id="16206-p116">You can also use properties, and operators to illustrate how you can refine your queries. For more information and examples, see [Form a query to find sensitive data stored on sites](https://support.office.com/fr-FR/article/Form-a-query-to-find-sensitive-data-stored-on-sites-3019fbc5-7f15-4972-8d0e-dc182dc7f836).</span></span>
