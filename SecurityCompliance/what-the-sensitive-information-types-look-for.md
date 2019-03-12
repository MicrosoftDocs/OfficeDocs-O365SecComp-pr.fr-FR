---
title: Éléments recherchés par les types d’informations sensibles
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
search.appverid: MET150
ms.topic: reference
f1_keywords:
- ms.o365.cc.UnifiedDLPRuleContainsSensitiveInformation
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
description: La protection contre la perte de données (DLP) dans &amp; le centre de sécurité conformité d'Office 365 inclut 80 types d'informations sensibles que vous pouvez utiliser dans vos stratégies DLP. Cette rubrique répertorie tous ces types d'informations sensibles et indique ce qu'une stratégie DLP recherche pour chaque type.
ms.openlocfilehash: e9811b285e98a791570dc91e275cb5cead4f8bc9
ms.sourcegitcommit: 6e8e2b43a4bea31c1e835c5b050824651c6a0094
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/11/2019
ms.locfileid: "30537641"
---
# <a name="what-the-sensitive-information-types-look-for"></a><span data-ttu-id="64f1e-104">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="64f1e-104">What the sensitive information types look for</span></span>

<span data-ttu-id="64f1e-105">La protection contre la perte de données (DLP) dans &amp; le centre de sécurité conformité Office 365 inclut de nombreux types d'informations sensibles que vous pouvez utiliser dans vos stratégies DLP.</span><span class="sxs-lookup"><span data-stu-id="64f1e-105">Data loss prevention (DLP) in the Office 365 Security &amp; Compliance Center includes many sensitive information types that are ready for you to use in your DLP policies.</span></span> <span data-ttu-id="64f1e-106">Cette rubrique répertorie tous ces types d'informations sensibles et indique ce qu'une stratégie DLP recherche pour chaque type.</span><span class="sxs-lookup"><span data-stu-id="64f1e-106">This topic lists all of these sensitive information types and shows what a DLP policy looks for when it detects each type.</span></span> <span data-ttu-id="64f1e-107">Un type d'informations sensibles est défini par un modèle qui peut être identifié par une fonction ou une expression régulière.</span><span class="sxs-lookup"><span data-stu-id="64f1e-107">A sensitive information type is defined by a pattern that can be identified by a regular expression or a function.</span></span> <span data-ttu-id="64f1e-108">En outre, des preuves corroborantes comme les mots clés et les sommes de contrôle peuvent être utilisées pour identifier un type d'informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="64f1e-108">In addition, corroborative evidence such as keywords and checksums can be used to identify a sensitive information type.</span></span> <span data-ttu-id="64f1e-109">Le niveau de confiance et la proximité sont également utilisés dans le processus d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="64f1e-109">Confidence level and proximity are also used in the evaluation process.</span></span>
  
## <a name="aba-routing-number"></a><span data-ttu-id="64f1e-110">Numéro de routage ABA</span><span class="sxs-lookup"><span data-stu-id="64f1e-110">ABA Routing Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-111">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-111">Format</span></span>

<span data-ttu-id="64f1e-112">9 chiffres mis en forme ou non mis en forme</span><span class="sxs-lookup"><span data-stu-id="64f1e-112">9 digits which may be in a formatted or unformatted pattern</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-113">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-113">Pattern</span></span>

<span data-ttu-id="64f1e-114">Avec</span><span class="sxs-lookup"><span data-stu-id="64f1e-114">Formatted:</span></span>
- <span data-ttu-id="64f1e-115">Quatre chiffres commençant par 0, 1, 2, 3, 6, 7 ou 8</span><span class="sxs-lookup"><span data-stu-id="64f1e-115">Four digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span>
- <span data-ttu-id="64f1e-116">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="64f1e-116">A hyphen</span></span>
- <span data-ttu-id="64f1e-117">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-117">Four digits</span></span>
- <span data-ttu-id="64f1e-118">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="64f1e-118">A hyphen</span></span>
- <span data-ttu-id="64f1e-119">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="64f1e-119">A digit</span></span>

<span data-ttu-id="64f1e-120">Non mis en forme: 9 chiffres consécutifs commençant par 0, 1, 2, 3, 6, 7 ou 8</span><span class="sxs-lookup"><span data-stu-id="64f1e-120">Unformatted: 9 consecutive digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span> 

### <a name="checksum"></a><span data-ttu-id="64f1e-121">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-121">Checksum</span></span>

<span data-ttu-id="64f1e-122">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-122">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-123">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-123">Definition</span></span>

<span data-ttu-id="64f1e-124">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-124">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-125">La fonction Func_aba_routing trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-125">The function Func_aba_routing finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-126">Un mot clé figurant dans la liste Keyword_ABA_Routing est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-126">A keyword from Keyword_ABA_Routing is found.</span></span>

```
<!-- ABA Routing Number -->
<Entity id="cb353f78-2b72-4c3c-8827-92ebe4f69fdf" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_aba_routing" />
        <Match idRef="Keyword_ABA_Routing" />
      </Pattern>
 </Entity>
```


### <a name="keywords"></a><span data-ttu-id="64f1e-127">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-127">Keywords</span></span>

#### <a name="keywordabarouting"></a><span data-ttu-id="64f1e-128">Keyword_ABA_Routing</span><span class="sxs-lookup"><span data-stu-id="64f1e-128">Keyword_ABA_Routing</span></span>

- <span data-ttu-id="64f1e-129">ABA</span><span class="sxs-lookup"><span data-stu-id="64f1e-129">aba</span></span>
- <span data-ttu-id="64f1e-130"># aba</span><span class="sxs-lookup"><span data-stu-id="64f1e-130">aba #</span></span>
- <span data-ttu-id="64f1e-131"># routage aba</span><span class="sxs-lookup"><span data-stu-id="64f1e-131">aba routing #</span></span>
- <span data-ttu-id="64f1e-132">numéro de routage aba</span><span class="sxs-lookup"><span data-stu-id="64f1e-132">aba routing number</span></span>
- <span data-ttu-id="64f1e-133">ABA</span><span class="sxs-lookup"><span data-stu-id="64f1e-133">aba#</span></span>
- <span data-ttu-id="64f1e-134">abarouting #</span><span class="sxs-lookup"><span data-stu-id="64f1e-134">abarouting#</span></span>
- <span data-ttu-id="64f1e-135">numéro aba</span><span class="sxs-lookup"><span data-stu-id="64f1e-135">aba number</span></span>
- <span data-ttu-id="64f1e-136">abaroutingnumber</span><span class="sxs-lookup"><span data-stu-id="64f1e-136">abaroutingnumber</span></span>
- <span data-ttu-id="64f1e-137"># routage american bank association</span><span class="sxs-lookup"><span data-stu-id="64f1e-137">american bank association routing #</span></span>
- <span data-ttu-id="64f1e-138">numéro de routage american bank association</span><span class="sxs-lookup"><span data-stu-id="64f1e-138">american bank association routing number</span></span>
- <span data-ttu-id="64f1e-139">americanbankassociationrouting #</span><span class="sxs-lookup"><span data-stu-id="64f1e-139">americanbankassociationrouting#</span></span>
- <span data-ttu-id="64f1e-140">americanbankassociationroutingnumber</span><span class="sxs-lookup"><span data-stu-id="64f1e-140">americanbankassociationroutingnumber</span></span>
- <span data-ttu-id="64f1e-141">numéro de routage bancaire</span><span class="sxs-lookup"><span data-stu-id="64f1e-141">bank routing number</span></span>
- <span data-ttu-id="64f1e-142">bankrouting #</span><span class="sxs-lookup"><span data-stu-id="64f1e-142">bankrouting#</span></span>
- <span data-ttu-id="64f1e-143">bankroutingnumber</span><span class="sxs-lookup"><span data-stu-id="64f1e-143">bankroutingnumber</span></span>
- <span data-ttu-id="64f1e-144">numéro de routage</span><span class="sxs-lookup"><span data-stu-id="64f1e-144">routing transit number</span></span>
- <span data-ttu-id="64f1e-145">RTN</span><span class="sxs-lookup"><span data-stu-id="64f1e-145">RTN</span></span> 
   
## <a name="argentina-national-identity-dni-number"></a><span data-ttu-id="64f1e-146">Numéro d’identité nationale (DNI) pour l’Argentine</span><span class="sxs-lookup"><span data-stu-id="64f1e-146">Argentina National Identity (DNI) Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-147">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-147">Format</span></span>

<span data-ttu-id="64f1e-148">Huit chiffres séparés par des points</span><span class="sxs-lookup"><span data-stu-id="64f1e-148">Eight digits separated by periods</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-149">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-149">Pattern</span></span>

<span data-ttu-id="64f1e-150">Huit chiffres :</span><span class="sxs-lookup"><span data-stu-id="64f1e-150">Eight digits:</span></span>
- <span data-ttu-id="64f1e-151">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-151">Two digits</span></span>
- <span data-ttu-id="64f1e-152">Un point </span><span class="sxs-lookup"><span data-stu-id="64f1e-152">A period</span></span>
- <span data-ttu-id="64f1e-153">Trois chiffres </span><span class="sxs-lookup"><span data-stu-id="64f1e-153">Three digits</span></span>
- <span data-ttu-id="64f1e-154">Un point </span><span class="sxs-lookup"><span data-stu-id="64f1e-154">A period</span></span>
- <span data-ttu-id="64f1e-155">Trois chiffres </span><span class="sxs-lookup"><span data-stu-id="64f1e-155">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-156">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-156">Checksum</span></span>

<span data-ttu-id="64f1e-157">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-157">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-158">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-158">Definition</span></span>

<span data-ttu-id="64f1e-159">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-159">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-160">L’expression régulière Regex_argentina_national_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-160">The regular expression Regex_argentina_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-161">Un mot clé figurant dans la liste Keyword_argentina_national_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-161">A keyword from Keyword_argentina_national_id is found.</span></span>

```
<!-- Argentina National Identity (DNI) Number -->
<Entity id="eefbb00e-8282-433c-8620-8f1da3bffdb2" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_argentina_national_id"/>
      <Match idRef="Keyword_argentina_national_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-162">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-162">Keywords</span></span>

#### <a name="keywordargentinanationalid"></a><span data-ttu-id="64f1e-163">Keyword_argentina_national_id</span><span class="sxs-lookup"><span data-stu-id="64f1e-163">Keyword_argentina_national_id</span></span>

- <span data-ttu-id="64f1e-164">Argentina National Identity number</span><span class="sxs-lookup"><span data-stu-id="64f1e-164">Argentina National Identity number</span></span> 
- <span data-ttu-id="64f1e-165">Identité</span><span class="sxs-lookup"><span data-stu-id="64f1e-165">Identity</span></span> 
- <span data-ttu-id="64f1e-166">Identification de la carte d'identité nationale</span><span class="sxs-lookup"><span data-stu-id="64f1e-166">Identification National Identity Card</span></span> 
- <span data-ttu-id="64f1e-167">DNI</span><span class="sxs-lookup"><span data-stu-id="64f1e-167">DNI</span></span> 
- <span data-ttu-id="64f1e-168">CARTE d'interface réseau nationale du registre des personnes</span><span class="sxs-lookup"><span data-stu-id="64f1e-168">NIC National Registry of Persons</span></span> 
- <span data-ttu-id="64f1e-169">Documento Nacional de Identidad</span><span class="sxs-lookup"><span data-stu-id="64f1e-169">Documento Nacional de Identidad</span></span> 
- <span data-ttu-id="64f1e-170">Registro Nacional de las Personas</span><span class="sxs-lookup"><span data-stu-id="64f1e-170">Registro Nacional de las Personas</span></span> 
- <span data-ttu-id="64f1e-171">Identidad</span><span class="sxs-lookup"><span data-stu-id="64f1e-171">Identidad</span></span> 
- <span data-ttu-id="64f1e-172">Identificación</span><span class="sxs-lookup"><span data-stu-id="64f1e-172">Identificación</span></span> 
   
## <a name="australia-bank-account-number"></a><span data-ttu-id="64f1e-173">Numéro de compte bancaire Australie</span><span class="sxs-lookup"><span data-stu-id="64f1e-173">Australia Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-174">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-174">Format</span></span>

<span data-ttu-id="64f1e-175">6 à 10 chiffres avec ou sans le numéro d’agence bancaire de l’État</span><span class="sxs-lookup"><span data-stu-id="64f1e-175">6-10 digits with or without a bank state branch number</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-176">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-176">Pattern</span></span>

<span data-ttu-id="64f1e-177">Le numéro de compte est composé de 6 à 10 chiffres.</span><span class="sxs-lookup"><span data-stu-id="64f1e-177">Account number is 6-10 digits.</span></span>
<span data-ttu-id="64f1e-178">Numéro de succursale bancaire en Australie :</span><span class="sxs-lookup"><span data-stu-id="64f1e-178">Australia bank state branch number:</span></span>
- <span data-ttu-id="64f1e-179">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-179">Three digits</span></span> 
- <span data-ttu-id="64f1e-180">Un trait d’union</span><span class="sxs-lookup"><span data-stu-id="64f1e-180">A hyphen</span></span> 
- <span data-ttu-id="64f1e-181">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-181">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-182">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-182">Checksum</span></span>

<span data-ttu-id="64f1e-183">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-183">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-184">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-184">Definition</span></span>

<span data-ttu-id="64f1e-185">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-185">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-186">L’expression régulière Regex_australia_bank_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-186">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="64f1e-187">Un mot clé figurant dans la liste Keyword_australia_bank_account_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-187">A keyword from Keyword_australia_bank_account_number is found.</span></span>
- <span data-ttu-id="64f1e-188">L’expression régulière Regex_australia_bank_account_number_bsb trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-188">The regular expression Regex_australia_bank_account_number_bsb finds content that matches the pattern.</span></span>

<span data-ttu-id="64f1e-189">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-189">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-190">L’expression régulière Regex_australia_bank_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-190">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="64f1e-191">Un mot clé figurant dans la liste Keyword_australia_bank_account_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-191">A keyword from Keyword_australia_bank_account_number is found.</span></span>

```
<!-- Australia Bank Account Number -->
<Entity id="74a54de9-2a30-4aa0-a8aa-3d9327fc07c7" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Regex_australia_bank_account_number" />
        <Match idRef="Keyword_australia_bank_account_number" />
        <Match idRef="Regex_australia_bank_account_number_bsb" />
  </Pattern>
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_australia_bank_account_number" />
        <Match idRef="Keyword_australia_bank_account_number" />
  </Pattern>
 </Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-192">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-192">Keywords</span></span>

#### <a name="keywordaustraliabankaccountnumber"></a><span data-ttu-id="64f1e-193">Keyword_australia_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="64f1e-193">Keyword_australia_bank_account_number</span></span>

- <span data-ttu-id="64f1e-194">code swift banque</span><span class="sxs-lookup"><span data-stu-id="64f1e-194">swift bank code</span></span>
- <span data-ttu-id="64f1e-195">banque correspondante</span><span class="sxs-lookup"><span data-stu-id="64f1e-195">correspondent bank</span></span>
- <span data-ttu-id="64f1e-196">devise de base</span><span class="sxs-lookup"><span data-stu-id="64f1e-196">base currency</span></span>
- <span data-ttu-id="64f1e-197">compte aux États-Unis</span><span class="sxs-lookup"><span data-stu-id="64f1e-197">usa account</span></span>
- <span data-ttu-id="64f1e-198">adresse du titulaire</span><span class="sxs-lookup"><span data-stu-id="64f1e-198">holder address</span></span>
- <span data-ttu-id="64f1e-199">adresse de la banque</span><span class="sxs-lookup"><span data-stu-id="64f1e-199">bank address</span></span>
- <span data-ttu-id="64f1e-200">informations du compte</span><span class="sxs-lookup"><span data-stu-id="64f1e-200">information account</span></span>
- <span data-ttu-id="64f1e-201">transferts de fonds</span><span class="sxs-lookup"><span data-stu-id="64f1e-201">fund transfers</span></span>
- <span data-ttu-id="64f1e-202">frais bancaires</span><span class="sxs-lookup"><span data-stu-id="64f1e-202">bank charges</span></span>
- <span data-ttu-id="64f1e-203">informations sur la banque</span><span class="sxs-lookup"><span data-stu-id="64f1e-203">bank details</span></span>
- <span data-ttu-id="64f1e-204">informations bancaires</span><span class="sxs-lookup"><span data-stu-id="64f1e-204">banking information</span></span>
- <span data-ttu-id="64f1e-205">noms complets</span><span class="sxs-lookup"><span data-stu-id="64f1e-205">full names</span></span>
- <span data-ttu-id="64f1e-206">auront</span><span class="sxs-lookup"><span data-stu-id="64f1e-206">iaea</span></span>

   
## <a name="australia-drivers-license-number"></a><span data-ttu-id="64f1e-207">Numéro de permis de conduire Australie</span><span class="sxs-lookup"><span data-stu-id="64f1e-207">Australia Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-208">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-208">Format</span></span>

<span data-ttu-id="64f1e-209">Neuf lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-209">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-210">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-210">Pattern</span></span>

<span data-ttu-id="64f1e-211">Neuf lettres et chiffres :</span><span class="sxs-lookup"><span data-stu-id="64f1e-211">Nine letters and digits:</span></span> 

- <span data-ttu-id="64f1e-212">Deux chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="64f1e-212">Two digits or letters (not case sensitive)</span></span> 
- <span data-ttu-id="64f1e-213">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-213">Two digits</span></span> 
- <span data-ttu-id="64f1e-214">Cinq chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="64f1e-214">Five digits or letters (not case sensitive)</span></span>

<span data-ttu-id="64f1e-215">OU</span><span class="sxs-lookup"><span data-stu-id="64f1e-215">OR</span></span>

- <span data-ttu-id="64f1e-216">1 ou 2 lettres facultatives (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="64f1e-216">1-2 optional letters (not case sensitive)</span></span> 
- <span data-ttu-id="64f1e-217">4 à 9 chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-217">4-9 digits</span></span>

<span data-ttu-id="64f1e-218">OU</span><span class="sxs-lookup"><span data-stu-id="64f1e-218">OR</span></span>

- <span data-ttu-id="64f1e-219">Neuf chiffres ou lettres (ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="64f1e-219">Nine digits or letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-220">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-220">Checksum</span></span>

<span data-ttu-id="64f1e-221">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-221">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-222">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-222">Definition</span></span>

<span data-ttu-id="64f1e-223">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-223">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-224">L’expression régulière Regex_australia_drivers_license_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-224">The regular expression Regex_australia_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-225">Un mot clé figurant dans la liste Keyword_australia_drivers_license_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-225">A keyword from Keyword_australia_drivers_license_number is found.</span></span>
- <span data-ttu-id="64f1e-226">Aucun mot clé figurant dans la liste Keyword_australia_drivers_license_number_exclusions n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-226">No keyword from Keyword_australia_drivers_license_number_exclusions is found.</span></span>

```
<!-- Australia Drivers License Number -->
<Entity id="1cbbc8f5-9216-4392-9eb5-5ac2298d1356" patternsProximity="300" recommendedConfidence="75">
   <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_australia_drivers_license_number" />
        <Match idRef="Keyword_australia_drivers_license_number" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_australia_drivers_license_number_exclusions" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-227">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-227">Keywords</span></span>

#### <a name="keywordaustraliadriverslicensenumber"></a><span data-ttu-id="64f1e-228">Keyword_australia_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="64f1e-228">Keyword_australia_drivers_license_number</span></span>

- <span data-ttu-id="64f1e-229">permis de conduite internationaux</span><span class="sxs-lookup"><span data-stu-id="64f1e-229">international driving permits</span></span>
- <span data-ttu-id="64f1e-230">australian automobile association</span><span class="sxs-lookup"><span data-stu-id="64f1e-230">australian automobile association</span></span>
- <span data-ttu-id="64f1e-231">permis de conduite international</span><span class="sxs-lookup"><span data-stu-id="64f1e-231">international driving permit</span></span>
- <span data-ttu-id="64f1e-232">DriverLicence</span><span class="sxs-lookup"><span data-stu-id="64f1e-232">DriverLicence</span></span>
- <span data-ttu-id="64f1e-233">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="64f1e-233">DriverLicences</span></span>
- <span data-ttu-id="64f1e-234">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-234">Driver Lic</span></span>
- <span data-ttu-id="64f1e-235">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-235">Driver Licence</span></span>
- <span data-ttu-id="64f1e-236">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-236">Driver Licences</span></span>
- <span data-ttu-id="64f1e-237">DriversLic</span><span class="sxs-lookup"><span data-stu-id="64f1e-237">DriversLic</span></span>
- <span data-ttu-id="64f1e-238">DriversLicence</span><span class="sxs-lookup"><span data-stu-id="64f1e-238">DriversLicence</span></span>
- <span data-ttu-id="64f1e-239">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="64f1e-239">DriversLicences</span></span>
- <span data-ttu-id="64f1e-240">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-240">Drivers Lic</span></span>
- <span data-ttu-id="64f1e-241">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-241">Drivers Lics</span></span>
- <span data-ttu-id="64f1e-242">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-242">Drivers Licence</span></span>
- <span data-ttu-id="64f1e-243">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-243">Drivers Licences</span></span>
- <span data-ttu-id="64f1e-244">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="64f1e-244">Driver'Lic</span></span>
- <span data-ttu-id="64f1e-245">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="64f1e-245">Driver'Lics</span></span>
- <span data-ttu-id="64f1e-246">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="64f1e-246">Driver'Licence</span></span>
- <span data-ttu-id="64f1e-247">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="64f1e-247">Driver'Licences</span></span>
- <span data-ttu-id="64f1e-248">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-248">Driver' Lic</span></span>
- <span data-ttu-id="64f1e-249">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-249">Driver' Lics</span></span>
- <span data-ttu-id="64f1e-250">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-250">Driver' Licence</span></span>
- <span data-ttu-id="64f1e-251">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-251">Driver' Licences</span></span>
- <span data-ttu-id="64f1e-252">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="64f1e-252">Driver'sLic</span></span>
- <span data-ttu-id="64f1e-253">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="64f1e-253">Driver'sLics</span></span>
- <span data-ttu-id="64f1e-254">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="64f1e-254">Driver'sLicence</span></span>
- <span data-ttu-id="64f1e-255">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="64f1e-255">Driver'sLicences</span></span>
- <span data-ttu-id="64f1e-256">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-256">Driver's Lic</span></span>
- <span data-ttu-id="64f1e-257">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-257">Driver's Lics</span></span>
- <span data-ttu-id="64f1e-258">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-258">Driver's Licence</span></span>
- <span data-ttu-id="64f1e-259">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-259">Driver's Licences</span></span>
- <span data-ttu-id="64f1e-260">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="64f1e-260">DriverLic#</span></span>
- <span data-ttu-id="64f1e-261">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="64f1e-261">DriverLics#</span></span>
- <span data-ttu-id="64f1e-262">DriverLicence #</span><span class="sxs-lookup"><span data-stu-id="64f1e-262">DriverLicence#</span></span>
- <span data-ttu-id="64f1e-263">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="64f1e-263">DriverLicences#</span></span>
- <span data-ttu-id="64f1e-264">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-264">Driver Lic#</span></span>
- <span data-ttu-id="64f1e-265">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-265">Driver Lics#</span></span>
- <span data-ttu-id="64f1e-266">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-266">Driver Licence#</span></span>
- <span data-ttu-id="64f1e-267">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-267">Driver Licences#</span></span>
- <span data-ttu-id="64f1e-268">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="64f1e-268">DriversLic#</span></span>
- <span data-ttu-id="64f1e-269">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="64f1e-269">DriversLics#</span></span>
- <span data-ttu-id="64f1e-270">DriversLicence #</span><span class="sxs-lookup"><span data-stu-id="64f1e-270">DriversLicence#</span></span>
- <span data-ttu-id="64f1e-271">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="64f1e-271">DriversLicences#</span></span>
- <span data-ttu-id="64f1e-272">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-272">Drivers Lic#</span></span>
- <span data-ttu-id="64f1e-273">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-273">Drivers Lics#</span></span>
- <span data-ttu-id="64f1e-274">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-274">Drivers Licence#</span></span>
- <span data-ttu-id="64f1e-275">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-275">Drivers Licences#</span></span>
- <span data-ttu-id="64f1e-276">Driver'Lic #</span><span class="sxs-lookup"><span data-stu-id="64f1e-276">Driver'Lic#</span></span>
- <span data-ttu-id="64f1e-277">Driver'Lics #</span><span class="sxs-lookup"><span data-stu-id="64f1e-277">Driver'Lics#</span></span>
- <span data-ttu-id="64f1e-278">Driver'Licence #</span><span class="sxs-lookup"><span data-stu-id="64f1e-278">Driver'Licence#</span></span>
- <span data-ttu-id="64f1e-279">Driver'Licences #</span><span class="sxs-lookup"><span data-stu-id="64f1e-279">Driver'Licences#</span></span>
- <span data-ttu-id="64f1e-280">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-280">Driver' Lic#</span></span>
- <span data-ttu-id="64f1e-281">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-281">Driver' Lics#</span></span>
- <span data-ttu-id="64f1e-282">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-282">Driver' Licence#</span></span>
- <span data-ttu-id="64f1e-283">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-283">Driver' Licences#</span></span>
- <span data-ttu-id="64f1e-284">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="64f1e-284">Driver'sLic#</span></span>
- <span data-ttu-id="64f1e-285">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="64f1e-285">Driver'sLics#</span></span>
- <span data-ttu-id="64f1e-286">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="64f1e-286">Driver'sLicence#</span></span>
- <span data-ttu-id="64f1e-287">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="64f1e-287">Driver'sLicences#</span></span>
- <span data-ttu-id="64f1e-288">#Permisconduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-288">Driver's Lic#</span></span>
- <span data-ttu-id="64f1e-289">#Permisconduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-289">Driver's Lics#</span></span>
- <span data-ttu-id="64f1e-290">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-290">Driver's Licence#</span></span>
- <span data-ttu-id="64f1e-291">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-291">Driver's Licences#</span></span> 

#### <a name="keywordaustraliadriverslicensenumberexclusions"></a><span data-ttu-id="64f1e-292">Keyword_australia_drivers_license_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="64f1e-292">Keyword_australia_drivers_license_number_exclusions</span></span>

- <span data-ttu-id="64f1e-293">AAA</span><span class="sxs-lookup"><span data-stu-id="64f1e-293">aaa</span></span>
- <span data-ttu-id="64f1e-294">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="64f1e-294">DriverLicense</span></span>
- <span data-ttu-id="64f1e-295">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="64f1e-295">DriverLicenses</span></span>
- <span data-ttu-id="64f1e-296">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-296">Driver License</span></span>
- <span data-ttu-id="64f1e-297">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-297">Driver Licenses</span></span>
- <span data-ttu-id="64f1e-298">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="64f1e-298">DriversLicense</span></span>
- <span data-ttu-id="64f1e-299">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="64f1e-299">DriversLicenses</span></span>
- <span data-ttu-id="64f1e-300">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-300">Drivers License</span></span>
- <span data-ttu-id="64f1e-301">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-301">Drivers Licenses</span></span>
- <span data-ttu-id="64f1e-302">Driver'License</span><span class="sxs-lookup"><span data-stu-id="64f1e-302">Driver'License</span></span>
- <span data-ttu-id="64f1e-303">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="64f1e-303">Driver'Licenses</span></span>
- <span data-ttu-id="64f1e-304">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-304">Driver' License</span></span>
- <span data-ttu-id="64f1e-305">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-305">Driver' Licenses</span></span>
- <span data-ttu-id="64f1e-306">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="64f1e-306">Driver'sLicense</span></span>
- <span data-ttu-id="64f1e-307">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="64f1e-307">Driver'sLicenses</span></span>
- <span data-ttu-id="64f1e-308">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-308">Driver's License</span></span>
- <span data-ttu-id="64f1e-309">Driver’s Licenses</span><span class="sxs-lookup"><span data-stu-id="64f1e-309">Driver's Licenses</span></span>
- <span data-ttu-id="64f1e-310">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="64f1e-310">DriverLicense#</span></span>
- <span data-ttu-id="64f1e-311">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="64f1e-311">DriverLicenses#</span></span>
- <span data-ttu-id="64f1e-312">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-312">Driver License#</span></span>
- <span data-ttu-id="64f1e-313">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-313">Driver Licenses#</span></span>
- <span data-ttu-id="64f1e-314">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="64f1e-314">DriversLicense#</span></span>
- <span data-ttu-id="64f1e-315">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="64f1e-315">DriversLicenses#</span></span>
- <span data-ttu-id="64f1e-316">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-316">Drivers License#</span></span>
- <span data-ttu-id="64f1e-317">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-317">Drivers Licenses#</span></span>
- <span data-ttu-id="64f1e-318">Driver'License #</span><span class="sxs-lookup"><span data-stu-id="64f1e-318">Driver'License#</span></span>
- <span data-ttu-id="64f1e-319">Driver'Licenses #</span><span class="sxs-lookup"><span data-stu-id="64f1e-319">Driver'Licenses#</span></span>
- <span data-ttu-id="64f1e-320">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-320">Driver' License#</span></span>
- <span data-ttu-id="64f1e-321">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-321">Driver' Licenses#</span></span>
- <span data-ttu-id="64f1e-322">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="64f1e-322">Driver'sLicense#</span></span>
- <span data-ttu-id="64f1e-323">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="64f1e-323">Driver'sLicenses#</span></span>
- <span data-ttu-id="64f1e-324">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-324">Driver's License#</span></span>
- <span data-ttu-id="64f1e-325">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-325">Driver's Licenses#</span></span>
   
## <a name="australia-medical-account-number"></a><span data-ttu-id="64f1e-326">Numéro de dossier médical Australie</span><span class="sxs-lookup"><span data-stu-id="64f1e-326">Australia Medical Account Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-327">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-327">Format</span></span>

<span data-ttu-id="64f1e-328">10 à 11 chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-328">10-11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-329">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-329">Pattern</span></span>

<span data-ttu-id="64f1e-330">10 à 11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="64f1e-330">10-11 digits:</span></span>
- <span data-ttu-id="64f1e-331">Le premier chiffre est compris entre 2 et 6</span><span class="sxs-lookup"><span data-stu-id="64f1e-331">First digit is in the range 2-6</span></span>
- <span data-ttu-id="64f1e-332">Le neuvième chiffre est un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-332">Ninth digit is a check digit</span></span>
- <span data-ttu-id="64f1e-333">Le dixième chiffre est le chiffre d’émission</span><span class="sxs-lookup"><span data-stu-id="64f1e-333">Tenth digit is the issue digit</span></span>
- <span data-ttu-id="64f1e-334">Le onzième chiffre (facultatif) est le numéro individuel</span><span class="sxs-lookup"><span data-stu-id="64f1e-334">Eleventh digit (optional) is the individual number</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-335">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-335">Checksum</span></span>

<span data-ttu-id="64f1e-336">Oui</span><span class="sxs-lookup"><span data-stu-id="64f1e-336">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-337">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-337">Definition</span></span>

<span data-ttu-id="64f1e-338">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 95 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-338">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-339">La fonction Func_australian_medical_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-339">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-340">Un mot clé figurant dans la liste Keyword_Australia_Medical_Account_Number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-340">A keyword from Keyword_Australia_Medical_Account_Number is found.</span></span>
- <span data-ttu-id="64f1e-341">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-341">The checksum passes.</span></span>

<span data-ttu-id="64f1e-342">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-342">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-343">La fonction Func_australian_medical_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-343">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-344">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-344">The checksum passes.</span></span>

```
  <!-- Australia Medical Account Number -->
<Entity id="104a99a0-3d3b-4542-a40d-ab0b9e1efe63" recommendedConfidence="85" patternsProximity="300">
    <Pattern confidenceLevel="95">
     <IdMatch idRef="Func_australian_medical_account_number"/>
     <Any minMatches="1">
     <Match idRef="Keyword_Australia_Medical_Account_Number"/>
     </Any>
  </Pattern>
<Pattern confidenceLevel="85">
     <IdMatch idRef="Func_australian_medical_account_number"/>
     <Any minMatches="0" maxMatches="0">
  <Match idRef="Keyword_Australia_Medical_Account_Number"/>
     </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-345">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-345">Keywords</span></span>

#### <a name="keywordaustraliamedicalaccountnumber"></a><span data-ttu-id="64f1e-346">Keyword_Australia_Medical_Account_Number</span><span class="sxs-lookup"><span data-stu-id="64f1e-346">Keyword_Australia_Medical_Account_Number</span></span>

- <span data-ttu-id="64f1e-347">informations sur le compte bancaire</span><span class="sxs-lookup"><span data-stu-id="64f1e-347">bank account details</span></span>
- <span data-ttu-id="64f1e-348">remboursements d’assurance maladie</span><span class="sxs-lookup"><span data-stu-id="64f1e-348">medicare payments</span></span>
- <span data-ttu-id="64f1e-349">compte de prêts immobiliers</span><span class="sxs-lookup"><span data-stu-id="64f1e-349">mortgage account</span></span>
- <span data-ttu-id="64f1e-350">paiements bancaires</span><span class="sxs-lookup"><span data-stu-id="64f1e-350">bank payments</span></span>
- <span data-ttu-id="64f1e-351">direction de l’information</span><span class="sxs-lookup"><span data-stu-id="64f1e-351">information branch</span></span>
- <span data-ttu-id="64f1e-352">prêt sur carte de crédit</span><span class="sxs-lookup"><span data-stu-id="64f1e-352">credit card loan</span></span>
- <span data-ttu-id="64f1e-353">département des services sociaux</span><span class="sxs-lookup"><span data-stu-id="64f1e-353">department of human services</span></span>
- <span data-ttu-id="64f1e-354">service local</span><span class="sxs-lookup"><span data-stu-id="64f1e-354">local service</span></span>
- <span data-ttu-id="64f1e-355">médicaux</span><span class="sxs-lookup"><span data-stu-id="64f1e-355">medicare</span></span>

   
## <a name="australia-passport-number"></a><span data-ttu-id="64f1e-356">Numéro de passeport Australie</span><span class="sxs-lookup"><span data-stu-id="64f1e-356">Australia Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-357">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-357">Format</span></span>

<span data-ttu-id="64f1e-358">Une lettre suivie de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-358">A letter followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-359">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-359">Pattern</span></span>

<span data-ttu-id="64f1e-360">Une lettre (ne respectant pas la casse) suivie de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-360">A letter (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-361">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-361">Checksum</span></span>

<span data-ttu-id="64f1e-362">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-362">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-363">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-363">Definition</span></span>

<span data-ttu-id="64f1e-364">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-365">L’expression régulière Regex_australia_passport_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-365">The regular expression Regex_australia_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-366">Un mot clé depuis Keyword_passport ou Keyword_australia_passport_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-366">A keyword from Keyword_passport or Keyword_australia_passport_number is found.</span></span>

```
<!-- Australia Passport Number -->
<Entity id="29869db6-602d-4853-ab93-3484f905df50" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_australia_passport_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_passport" />
          <Match idRef="Keyword_australia_passport_number" />
        </Any>
   </Pattern>
</Entity>   
```

### <a name="keywords"></a><span data-ttu-id="64f1e-367">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-367">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="64f1e-368">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="64f1e-368">Keyword_passport</span></span>

- <span data-ttu-id="64f1e-369">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="64f1e-369">Passport Number</span></span>
- <span data-ttu-id="64f1e-370">N° de passeport</span><span class="sxs-lookup"><span data-stu-id="64f1e-370">Passport No</span></span>
- <span data-ttu-id="64f1e-371"># Passeport</span><span class="sxs-lookup"><span data-stu-id="64f1e-371">Passport #</span></span>
- <span data-ttu-id="64f1e-372">Tel</span><span class="sxs-lookup"><span data-stu-id="64f1e-372">Passport#</span></span>
- <span data-ttu-id="64f1e-373">PassportID</span><span class="sxs-lookup"><span data-stu-id="64f1e-373">PassportID</span></span>
- <span data-ttu-id="64f1e-374">N ° passeport</span><span class="sxs-lookup"><span data-stu-id="64f1e-374">Passportno</span></span>
- <span data-ttu-id="64f1e-375">passportnumber</span><span class="sxs-lookup"><span data-stu-id="64f1e-375">passportnumber</span></span>
- <span data-ttu-id="64f1e-376">パスポート</span><span class="sxs-lookup"><span data-stu-id="64f1e-376">パスポート</span></span>
- <span data-ttu-id="64f1e-377">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="64f1e-377">パスポート番号</span></span>
- <span data-ttu-id="64f1e-378">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="64f1e-378">パスポートのNum</span></span>
- <span data-ttu-id="64f1e-379">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="64f1e-379">パスポート ＃</span></span> 
- <span data-ttu-id="64f1e-380">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="64f1e-380">Numéro de passeport</span></span>
- <span data-ttu-id="64f1e-381">Passeport n°</span><span class="sxs-lookup"><span data-stu-id="64f1e-381">Passeport n °</span></span>
- <span data-ttu-id="64f1e-382">Passeport numéro</span><span class="sxs-lookup"><span data-stu-id="64f1e-382">Passeport Non</span></span>
- <span data-ttu-id="64f1e-383"># Passeport</span><span class="sxs-lookup"><span data-stu-id="64f1e-383">Passeport #</span></span>
- <span data-ttu-id="64f1e-384">Passeport</span><span class="sxs-lookup"><span data-stu-id="64f1e-384">Passeport#</span></span>
- <span data-ttu-id="64f1e-385">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="64f1e-385">PasseportNon</span></span>
- <span data-ttu-id="64f1e-386">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="64f1e-386">Passeportn °</span></span>

#### <a name="keywordaustraliapassportnumber"></a><span data-ttu-id="64f1e-387">Keyword_australia_passport_number</span><span class="sxs-lookup"><span data-stu-id="64f1e-387">Keyword_australia_passport_number</span></span>

- <span data-ttu-id="64f1e-388">tel</span><span class="sxs-lookup"><span data-stu-id="64f1e-388">passport</span></span>
- <span data-ttu-id="64f1e-389">informations sur le passeport</span><span class="sxs-lookup"><span data-stu-id="64f1e-389">passport details</span></span>
- <span data-ttu-id="64f1e-390">immigration et citoyenneté</span><span class="sxs-lookup"><span data-stu-id="64f1e-390">immigration and citizenship</span></span>
- <span data-ttu-id="64f1e-391">Australie</span><span class="sxs-lookup"><span data-stu-id="64f1e-391">commonwealth of australia</span></span>
- <span data-ttu-id="64f1e-392">service de l’immigration</span><span class="sxs-lookup"><span data-stu-id="64f1e-392">department of immigration</span></span>
- <span data-ttu-id="64f1e-393">adresse de résidence</span><span class="sxs-lookup"><span data-stu-id="64f1e-393">residential address</span></span>
- <span data-ttu-id="64f1e-394">service de l’immigration et de la citoyenneté</span><span class="sxs-lookup"><span data-stu-id="64f1e-394">department of immigration and citizenship</span></span>
- <span data-ttu-id="64f1e-395">délivrance</span><span class="sxs-lookup"><span data-stu-id="64f1e-395">visa</span></span>
- <span data-ttu-id="64f1e-396">Carte nationale d’identité</span><span class="sxs-lookup"><span data-stu-id="64f1e-396">national identity card</span></span>
- <span data-ttu-id="64f1e-397">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="64f1e-397">passport number</span></span>
- <span data-ttu-id="64f1e-398">document de voyage</span><span class="sxs-lookup"><span data-stu-id="64f1e-398">travel document</span></span>
- <span data-ttu-id="64f1e-399">autorité émettrice</span><span class="sxs-lookup"><span data-stu-id="64f1e-399">issuing authority</span></span>
   
## <a name="australia-tax-file-number"></a><span data-ttu-id="64f1e-400">Numéro de dossier fiscal Australie</span><span class="sxs-lookup"><span data-stu-id="64f1e-400">Australia Tax File Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-401">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-401">Format</span></span>

<span data-ttu-id="64f1e-402">8 ou 9 chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-402">8-9 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-403">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-403">Pattern</span></span>

<span data-ttu-id="64f1e-404">8 à 9 chiffres généralement entrecoupés d’espaces comme suit :</span><span class="sxs-lookup"><span data-stu-id="64f1e-404">8-9 digits typically presented with spaces as follows:</span></span>
- <span data-ttu-id="64f1e-405">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-405">Three digits</span></span> 
- <span data-ttu-id="64f1e-406">Un espace facultatif</span><span class="sxs-lookup"><span data-stu-id="64f1e-406">An optional space</span></span> 
- <span data-ttu-id="64f1e-407">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-407">Three digits</span></span> 
- <span data-ttu-id="64f1e-408">Un espace facultatif</span><span class="sxs-lookup"><span data-stu-id="64f1e-408">An optional space</span></span> 
- <span data-ttu-id="64f1e-409">2 à 3 chiffres où le dernier chiffre est un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-409">2-3 digits where the last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-410">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-410">Checksum</span></span>

<span data-ttu-id="64f1e-411">Oui</span><span class="sxs-lookup"><span data-stu-id="64f1e-411">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-412">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-412">Definition</span></span>

<span data-ttu-id="64f1e-413">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-413">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-414">La fonction Func_australian_tax_file_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-414">The function Func_australian_tax_file_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-415">Aucun mot clé figurant dans la liste Keyword_Australia_Tax_File_Number ou Keyword_number_exclusions n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-415">No keyword from Keyword_Australia_Tax_File_Number or Keyword_number_exclusions is found.</span></span>
- <span data-ttu-id="64f1e-416">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-416">The checksum passes.</span></span>

```
    <!-- Australia Tax File Number -->
<Entity id="e29bc95f-ff70-4a37-aa01-04d17360a4c5" patternsProximity="300" recommendedConfidence="85">
    
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_australian_tax_file_number" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_Australia_Tax_File_Number" />
          <Match idRef="Keyword_number_exclusions" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-417">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-417">Keywords</span></span>

#### <a name="keywordaustraliataxfilenumber"></a><span data-ttu-id="64f1e-418">Keyword_Australia_Tax_File_Number</span><span class="sxs-lookup"><span data-stu-id="64f1e-418">Keyword_Australia_Tax_File_Number</span></span>

- <span data-ttu-id="64f1e-419">numéro d’entreprise australien</span><span class="sxs-lookup"><span data-stu-id="64f1e-419">australian business number</span></span>
- <span data-ttu-id="64f1e-420">taux d’imposition marginale</span><span class="sxs-lookup"><span data-stu-id="64f1e-420">marginal tax rate</span></span>
- <span data-ttu-id="64f1e-421">prélèvement d’assurance maladie</span><span class="sxs-lookup"><span data-stu-id="64f1e-421">medicare levy</span></span>
- <span data-ttu-id="64f1e-422">numéro de portefeuille</span><span class="sxs-lookup"><span data-stu-id="64f1e-422">portfolio number</span></span>
- <span data-ttu-id="64f1e-423">service des vétérans</span><span class="sxs-lookup"><span data-stu-id="64f1e-423">service veterans</span></span>
- <span data-ttu-id="64f1e-424">retenue à la source</span><span class="sxs-lookup"><span data-stu-id="64f1e-424">withholding tax</span></span>
- <span data-ttu-id="64f1e-425">déclaration d’impôts individuels</span><span class="sxs-lookup"><span data-stu-id="64f1e-425">individual tax return</span></span>
- <span data-ttu-id="64f1e-426">numéro de dossier fiscal</span><span class="sxs-lookup"><span data-stu-id="64f1e-426">tax file number</span></span>

#### <a name="keywordnumberexclusions"></a><span data-ttu-id="64f1e-427">Keyword_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="64f1e-427">Keyword_number_exclusions</span></span>

- <span data-ttu-id="64f1e-428">00000000</span><span class="sxs-lookup"><span data-stu-id="64f1e-428">00000000</span></span>
- <span data-ttu-id="64f1e-429">11111111</span><span class="sxs-lookup"><span data-stu-id="64f1e-429">11111111</span></span>
- <span data-ttu-id="64f1e-430">22222222</span><span class="sxs-lookup"><span data-stu-id="64f1e-430">22222222</span></span>
- <span data-ttu-id="64f1e-431">33333333</span><span class="sxs-lookup"><span data-stu-id="64f1e-431">33333333</span></span>
- <span data-ttu-id="64f1e-432">44444444</span><span class="sxs-lookup"><span data-stu-id="64f1e-432">44444444</span></span>
- <span data-ttu-id="64f1e-433">55555555</span><span class="sxs-lookup"><span data-stu-id="64f1e-433">55555555</span></span>
- <span data-ttu-id="64f1e-434">66666666</span><span class="sxs-lookup"><span data-stu-id="64f1e-434">66666666</span></span>
- <span data-ttu-id="64f1e-435">77777777</span><span class="sxs-lookup"><span data-stu-id="64f1e-435">77777777</span></span>
- <span data-ttu-id="64f1e-436">88888888</span><span class="sxs-lookup"><span data-stu-id="64f1e-436">88888888</span></span>
- <span data-ttu-id="64f1e-437">99999999</span><span class="sxs-lookup"><span data-stu-id="64f1e-437">99999999</span></span>
- <span data-ttu-id="64f1e-438">000000000</span><span class="sxs-lookup"><span data-stu-id="64f1e-438">000000000</span></span>
- <span data-ttu-id="64f1e-439">111111111</span><span class="sxs-lookup"><span data-stu-id="64f1e-439">111111111</span></span>
- <span data-ttu-id="64f1e-440">222222222</span><span class="sxs-lookup"><span data-stu-id="64f1e-440">222222222</span></span>
- <span data-ttu-id="64f1e-441">333333333</span><span class="sxs-lookup"><span data-stu-id="64f1e-441">333333333</span></span>
- <span data-ttu-id="64f1e-442">444444444</span><span class="sxs-lookup"><span data-stu-id="64f1e-442">444444444</span></span>
- <span data-ttu-id="64f1e-443">555555555</span><span class="sxs-lookup"><span data-stu-id="64f1e-443">555555555</span></span>
- <span data-ttu-id="64f1e-444">666666666</span><span class="sxs-lookup"><span data-stu-id="64f1e-444">666666666</span></span>
- <span data-ttu-id="64f1e-445">777777777</span><span class="sxs-lookup"><span data-stu-id="64f1e-445">777777777</span></span>
- <span data-ttu-id="64f1e-446">888888888</span><span class="sxs-lookup"><span data-stu-id="64f1e-446">888888888</span></span>
- <span data-ttu-id="64f1e-447">999999999</span><span class="sxs-lookup"><span data-stu-id="64f1e-447">999999999</span></span>
- <span data-ttu-id="64f1e-448">0000000000</span><span class="sxs-lookup"><span data-stu-id="64f1e-448">0000000000</span></span>
- <span data-ttu-id="64f1e-449">1111111111</span><span class="sxs-lookup"><span data-stu-id="64f1e-449">1111111111</span></span>
- <span data-ttu-id="64f1e-450">2222222222</span><span class="sxs-lookup"><span data-stu-id="64f1e-450">2222222222</span></span>
- <span data-ttu-id="64f1e-451">3333333333</span><span class="sxs-lookup"><span data-stu-id="64f1e-451">3333333333</span></span>
- <span data-ttu-id="64f1e-452">4444444444</span><span class="sxs-lookup"><span data-stu-id="64f1e-452">4444444444</span></span>
- <span data-ttu-id="64f1e-453">5555555555</span><span class="sxs-lookup"><span data-stu-id="64f1e-453">5555555555</span></span>
- <span data-ttu-id="64f1e-454">6666666666</span><span class="sxs-lookup"><span data-stu-id="64f1e-454">6666666666</span></span>
- <span data-ttu-id="64f1e-455">7777777777</span><span class="sxs-lookup"><span data-stu-id="64f1e-455">7777777777</span></span>
- <span data-ttu-id="64f1e-456">8888888888</span><span class="sxs-lookup"><span data-stu-id="64f1e-456">8888888888</span></span>
- <span data-ttu-id="64f1e-457">9999999999</span><span class="sxs-lookup"><span data-stu-id="64f1e-457">9999999999</span></span>

## <a name="azure-documentdb-auth-key"></a><span data-ttu-id="64f1e-458">Clé d'authentification Azure DocumentDB</span><span class="sxs-lookup"><span data-stu-id="64f1e-458">Azure DocumentDB Auth Key</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-459">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-459">Format</span></span>

<span data-ttu-id="64f1e-460">La chaîne «DocumentDb» suivie des caractères et des chaînes présentés dans le modèle ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="64f1e-460">The string "DocumentDb" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-461">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-461">Pattern</span></span>

- <span data-ttu-id="64f1e-462">La chaîne «DocumentDb»</span><span class="sxs-lookup"><span data-stu-id="64f1e-462">The string "DocumentDb"</span></span>
- <span data-ttu-id="64f1e-463">N'importe quelle combinaison entre 3-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="64f1e-463">Any combination of between 3-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="64f1e-464">Symbole supérieur à (>), signe égal (=), guillemet (") ou apostrophe (')</span><span class="sxs-lookup"><span data-stu-id="64f1e-464">A greater than symbol (>), an equal sign (=), a quotation mark ("), or an apostrophe (')</span></span>
- <span data-ttu-id="64f1e-465">Toute combinaison de 86 lettres majuscules ou minuscules, des chiffres, une barre oblique (/) ou un signe plus (+)</span><span class="sxs-lookup"><span data-stu-id="64f1e-465">Any combination of 86 lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="64f1e-466">Deux signes égal (=)</span><span class="sxs-lookup"><span data-stu-id="64f1e-466">Two equal signs (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-467">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-467">Checksum</span></span>

<span data-ttu-id="64f1e-468">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-468">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-469">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-469">Definition</span></span>

<span data-ttu-id="64f1e-470">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-470">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-471">L'expression régulière CEP_Regex_AzureDocumentDBAuthKey trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-471">The regular expression CEP_Regex_AzureDocumentDBAuthKey finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-472">L'expression régulière CEP_CommonExampleKeywords ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-472">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```
<!-- Azure Document DB Auth Key -->
<Entity id="0f587d92-eb28-44a9-bd1c-90f2892b47aa" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureDocumentDBAuthKey" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_CommonExampleKeywords" />
          </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-473">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-473">Keywords</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="64f1e-474">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="64f1e-474">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="64f1e-475">(Notez que techniquement, ce type d'informations sensibles identifie ces mots clés à l'aide d'une expression régulière, et non d'une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="64f1e-475">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="64f1e-476">contoso</span><span class="sxs-lookup"><span data-stu-id="64f1e-476">contoso</span></span>
- <span data-ttu-id="64f1e-477">société</span><span class="sxs-lookup"><span data-stu-id="64f1e-477">fabrikam</span></span>
- <span data-ttu-id="64f1e-478">Northwind</span><span class="sxs-lookup"><span data-stu-id="64f1e-478">northwind</span></span>
- <span data-ttu-id="64f1e-479">immédiatement</span><span class="sxs-lookup"><span data-stu-id="64f1e-479">sandbox</span></span>
- <span data-ttu-id="64f1e-480">OneBox</span><span class="sxs-lookup"><span data-stu-id="64f1e-480">onebox</span></span>
- <span data-ttu-id="64f1e-481">hôte</span><span class="sxs-lookup"><span data-stu-id="64f1e-481">localhost</span></span>
- <span data-ttu-id="64f1e-482">bouclage</span><span class="sxs-lookup"><span data-stu-id="64f1e-482">127.0.0.1</span></span>
- <span data-ttu-id="64f1e-483">TESTACS. <!--no-hyperlink-->com</span><span class="sxs-lookup"><span data-stu-id="64f1e-483">testacs.<!--no-hyperlink-->com</span></span>
- <span data-ttu-id="64f1e-484">s-int.<!--no-hyperlink-->net</span><span class="sxs-lookup"><span data-stu-id="64f1e-484">s-int.<!--no-hyperlink-->net</span></span>

## <a name="azure-iaas-database-connection-string-and-azure-sql-connection-string"></a><span data-ttu-id="64f1e-485">Chaîne de connexion à la base de données IAAS Azure et chaîne de connexion Azure SQL</span><span class="sxs-lookup"><span data-stu-id="64f1e-485">Azure IAAS Database Connection String and Azure SQL Connection String</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-486">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-486">Format</span></span>

<span data-ttu-id="64f1e-487">La chaîne «Server», «Server» ou «Data source» suivie des caractères et des chaînes décrits dans le modèle ci-dessous, y compris la chaîne «cloudapp. Azure. <!--no-hyperlink-->com» ou «cloudapp. Azure. <!--no-hyperlink-->net "ou" Database. Windows. <!--no-hyperlink-->net ", et la chaîne" password "ou" password "ou" PWD ".</span><span class="sxs-lookup"><span data-stu-id="64f1e-487">The string "Server", "server", or "data source" followed by the characters and strings outlined in the pattern below, including the string "cloudapp.azure.<!--no-hyperlink-->com" or "cloudapp.azure.<!--no-hyperlink-->net" or "database.windows.<!--no-hyperlink-->net", and the string "Password" or "password" or "pwd".</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-488">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-488">Pattern</span></span>

- <span data-ttu-id="64f1e-489">Chaîne «serveur», «serveur» ou «source de données»</span><span class="sxs-lookup"><span data-stu-id="64f1e-489">The string "Server", "server", or "data source"</span></span>
- <span data-ttu-id="64f1e-490">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="64f1e-490">0-2 whitespace characters</span></span>
- <span data-ttu-id="64f1e-491">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="64f1e-491">An equal sign (=)</span></span>
- <span data-ttu-id="64f1e-492">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="64f1e-492">0-2 whitespace characters</span></span>
- <span data-ttu-id="64f1e-493">N'importe quelle combinaison entre 1-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="64f1e-493">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="64f1e-494">La chaîne «cloudapp. Azure. <!--no-hyperlink-->com "," cloudapp. Azure. <!--no-hyperlink-->net "ou" Database. Windows. <!--no-hyperlink-->net "</span><span class="sxs-lookup"><span data-stu-id="64f1e-494">The string "cloudapp.azure.<!--no-hyperlink-->com", "cloudapp.azure.<!--no-hyperlink-->net", or "database.windows.<!--no-hyperlink-->net"</span></span>
- <span data-ttu-id="64f1e-495">N'importe quelle combinaison entre 1-300 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="64f1e-495">Any combination of between 1-300 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="64f1e-496">La chaîne "password", "password" ou "PWD"</span><span class="sxs-lookup"><span data-stu-id="64f1e-496">The string "Password", "password", or "pwd"</span></span>
- <span data-ttu-id="64f1e-497">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="64f1e-497">0-2 whitespace characters</span></span>
- <span data-ttu-id="64f1e-498">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="64f1e-498">An equal sign (=)</span></span>
- <span data-ttu-id="64f1e-499">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="64f1e-499">0-2 whitespace characters</span></span>
- <span data-ttu-id="64f1e-500">Un ou plusieurs caractères qui ne sont pas des points-virgules (;), guillemets (") ou apostrophe (')</span><span class="sxs-lookup"><span data-stu-id="64f1e-500">One or more characters that is not a semicolon (;), quotation mark ("), or apostrophe (')</span></span>
- <span data-ttu-id="64f1e-501">Un point-virgule (;), guillemet (") ou apostrophe (')</span><span class="sxs-lookup"><span data-stu-id="64f1e-501">A semicolon (;), quotation mark ("), or apostrophe (')</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-502">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-502">Checksum</span></span>

<span data-ttu-id="64f1e-503">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-503">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-504">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-504">Definition</span></span>

<span data-ttu-id="64f1e-505">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-505">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-506">L'expression régulière CEP_Regex_AzureConnectionString trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-506">The regular expression CEP_Regex_AzureConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-507">L'expression régulière CEP_CommonExampleKeywords ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-507">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```
<!--Azure IAAS Database Connection String and Azure SQL Connection String-->
<Entity id="ce1a126d-186f-4700-8c0c-486157b953fd" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureConnectionString" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-508">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-508">Keywords</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="64f1e-509">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="64f1e-509">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="64f1e-510">(Notez que techniquement, ce type d'informations sensibles identifie ces mots clés à l'aide d'une expression régulière, et non d'une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="64f1e-510">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="64f1e-511">contoso</span><span class="sxs-lookup"><span data-stu-id="64f1e-511">contoso</span></span>
- <span data-ttu-id="64f1e-512">société</span><span class="sxs-lookup"><span data-stu-id="64f1e-512">fabrikam</span></span>
- <span data-ttu-id="64f1e-513">Northwind</span><span class="sxs-lookup"><span data-stu-id="64f1e-513">northwind</span></span>
- <span data-ttu-id="64f1e-514">immédiatement</span><span class="sxs-lookup"><span data-stu-id="64f1e-514">sandbox</span></span>
- <span data-ttu-id="64f1e-515">OneBox</span><span class="sxs-lookup"><span data-stu-id="64f1e-515">onebox</span></span>
- <span data-ttu-id="64f1e-516">hôte</span><span class="sxs-lookup"><span data-stu-id="64f1e-516">localhost</span></span>
- <span data-ttu-id="64f1e-517">bouclage</span><span class="sxs-lookup"><span data-stu-id="64f1e-517">127.0.0.1</span></span>
- <span data-ttu-id="64f1e-518">TESTACS. <!--no-hyperlink-->com</span><span class="sxs-lookup"><span data-stu-id="64f1e-518">testacs.<!--no-hyperlink-->com</span></span>
- <span data-ttu-id="64f1e-519">s-int.<!--no-hyperlink-->net</span><span class="sxs-lookup"><span data-stu-id="64f1e-519">s-int.<!--no-hyperlink-->net</span></span>

## <a name="azure-iot-connection-string"></a><span data-ttu-id="64f1e-520">Chaîne de connexion Azure IoT</span><span class="sxs-lookup"><span data-stu-id="64f1e-520">Azure IoT Connection String</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-521">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-521">Format</span></span>

<span data-ttu-id="64f1e-522">La chaîne «nomhôte» suivie des caractères et des chaînes décrits dans le modèle ci-dessous, y compris les chaînes «Azure-appareils. <!--no-hyperlink-->net "et" SharedAccessKey ".</span><span class="sxs-lookup"><span data-stu-id="64f1e-522">The string "HostName" followed by the characters and strings outlined in the pattern below, including the strings "azure-devices.<!--no-hyperlink-->net" and "SharedAccessKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-523">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-523">Pattern</span></span>

- <span data-ttu-id="64f1e-524">La chaîne «nomhôte»</span><span class="sxs-lookup"><span data-stu-id="64f1e-524">The string "HostName"</span></span>
- <span data-ttu-id="64f1e-525">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="64f1e-525">0-2 whitespace characters</span></span>
- <span data-ttu-id="64f1e-526">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="64f1e-526">An equal sign (=)</span></span>
- <span data-ttu-id="64f1e-527">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="64f1e-527">0-2 whitespace characters</span></span>
- <span data-ttu-id="64f1e-528">N'importe quelle combinaison entre 1-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="64f1e-528">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="64f1e-529">La chaîne «Azure-appareils. <!--no-hyperlink-->net "</span><span class="sxs-lookup"><span data-stu-id="64f1e-529">The string "azure-devices.<!--no-hyperlink-->net"</span></span>
- <span data-ttu-id="64f1e-530">N'importe quelle combinaison entre 1-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="64f1e-530">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="64f1e-531">La chaîne «SharedAccessKey»</span><span class="sxs-lookup"><span data-stu-id="64f1e-531">The string "SharedAccessKey"</span></span>
- <span data-ttu-id="64f1e-532">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="64f1e-532">0-2 whitespace characters</span></span>
- <span data-ttu-id="64f1e-533">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="64f1e-533">An equal sign (=)</span></span>
- <span data-ttu-id="64f1e-534">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="64f1e-534">0-2 whitespace characters</span></span>
- <span data-ttu-id="64f1e-535">Toute combinaison de 43 lettres majuscules ou minuscules, des chiffres, une barre oblique (/) ou un signe plus (+)</span><span class="sxs-lookup"><span data-stu-id="64f1e-535">Any combination of 43 lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="64f1e-536">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="64f1e-536">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-537">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-537">Checksum</span></span>

<span data-ttu-id="64f1e-538">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-538">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-539">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-539">Definition</span></span>

<span data-ttu-id="64f1e-540">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-540">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-541">L'expression régulière CEP_Regex_AzureIoTConnectionString trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-541">The regular expression CEP_Regex_AzureIoTConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-542">L'expression régulière CEP_CommonExampleKeywords ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-542">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```
<!--Azure IoT Connection String-->
<Entity id="0b34bec3-d5d6-4974-b7b0-dcdb5c90c29d" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureIoTConnectionString" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-543">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-543">Keywords</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="64f1e-544">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="64f1e-544">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="64f1e-545">(Notez que techniquement, ce type d'informations sensibles identifie ces mots clés à l'aide d'une expression régulière, et non d'une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="64f1e-545">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="64f1e-546">contoso</span><span class="sxs-lookup"><span data-stu-id="64f1e-546">contoso</span></span>
- <span data-ttu-id="64f1e-547">société</span><span class="sxs-lookup"><span data-stu-id="64f1e-547">fabrikam</span></span>
- <span data-ttu-id="64f1e-548">Northwind</span><span class="sxs-lookup"><span data-stu-id="64f1e-548">northwind</span></span>
- <span data-ttu-id="64f1e-549">immédiatement</span><span class="sxs-lookup"><span data-stu-id="64f1e-549">sandbox</span></span>
- <span data-ttu-id="64f1e-550">OneBox</span><span class="sxs-lookup"><span data-stu-id="64f1e-550">onebox</span></span>
- <span data-ttu-id="64f1e-551">hôte</span><span class="sxs-lookup"><span data-stu-id="64f1e-551">localhost</span></span>
- <span data-ttu-id="64f1e-552">bouclage</span><span class="sxs-lookup"><span data-stu-id="64f1e-552">127.0.0.1</span></span>
- <span data-ttu-id="64f1e-553">TESTACS. <!--no-hyperlink-->com</span><span class="sxs-lookup"><span data-stu-id="64f1e-553">testacs.<!--no-hyperlink-->com</span></span>
- <span data-ttu-id="64f1e-554">s-int.<!--no-hyperlink-->net</span><span class="sxs-lookup"><span data-stu-id="64f1e-554">s-int.<!--no-hyperlink-->net</span></span>

## <a name="azure-publish-setting-password"></a><span data-ttu-id="64f1e-555">Mot de passe de paramètre de publication Azure</span><span class="sxs-lookup"><span data-stu-id="64f1e-555">Azure Publish Setting Password</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-556">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-556">Format</span></span>

<span data-ttu-id="64f1e-557">La chaîne «userpwd =» suivie d'une chaîne alphanumérique.</span><span class="sxs-lookup"><span data-stu-id="64f1e-557">The string "userpwd=" followed by an alphanumeric string.</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-558">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-558">Pattern</span></span>

- <span data-ttu-id="64f1e-559">La chaîne «userpwd =»</span><span class="sxs-lookup"><span data-stu-id="64f1e-559">The string "userpwd="</span></span>
- <span data-ttu-id="64f1e-560">N'importe quelle combinaison de 60 lettres minuscules ou chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-560">Any combination of 60 lowercase letters or digits</span></span>
- <span data-ttu-id="64f1e-561">Guillemet (")</span><span class="sxs-lookup"><span data-stu-id="64f1e-561">A quotation mark (")</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-562">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-562">Checksum</span></span>

<span data-ttu-id="64f1e-563">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-563">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-564">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-564">Definition</span></span>

<span data-ttu-id="64f1e-565">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-565">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-566">L'expression régulière CEP_Regex_AzurePublishSettingPasswords trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-566">The regular expression CEP_Regex_AzurePublishSettingPasswords finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-567">L'expression régulière CEP_CommonExampleKeywords ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-567">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>


```
<!--Azure Publish Setting Password-->
<Entity id="75f4cc8a-a68e-49e5-89ce-fa8f03d286a5" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
       <IdMatch idRef="CEP_Regex_AzurePublishSettingPasswords" />
       <Any minMatches="0" maxMatches="0">
           <Match idRef="CEP_CommonExampleKeywords" />
       </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-568">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-568">Keywords</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="64f1e-569">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="64f1e-569">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="64f1e-570">(Notez que techniquement, ce type d'informations sensibles identifie ces mots clés à l'aide d'une expression régulière, et non d'une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="64f1e-570">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="64f1e-571">contoso</span><span class="sxs-lookup"><span data-stu-id="64f1e-571">contoso</span></span>
- <span data-ttu-id="64f1e-572">société</span><span class="sxs-lookup"><span data-stu-id="64f1e-572">fabrikam</span></span>
- <span data-ttu-id="64f1e-573">Northwind</span><span class="sxs-lookup"><span data-stu-id="64f1e-573">northwind</span></span>
- <span data-ttu-id="64f1e-574">immédiatement</span><span class="sxs-lookup"><span data-stu-id="64f1e-574">sandbox</span></span>
- <span data-ttu-id="64f1e-575">OneBox</span><span class="sxs-lookup"><span data-stu-id="64f1e-575">onebox</span></span>
- <span data-ttu-id="64f1e-576">hôte</span><span class="sxs-lookup"><span data-stu-id="64f1e-576">localhost</span></span>
- <span data-ttu-id="64f1e-577">bouclage</span><span class="sxs-lookup"><span data-stu-id="64f1e-577">127.0.0.1</span></span>
- <span data-ttu-id="64f1e-578">TESTACS. <!--no-hyperlink-->com</span><span class="sxs-lookup"><span data-stu-id="64f1e-578">testacs.<!--no-hyperlink-->com</span></span>
- <span data-ttu-id="64f1e-579">s-int.<!--no-hyperlink-->net</span><span class="sxs-lookup"><span data-stu-id="64f1e-579">s-int.<!--no-hyperlink-->net</span></span>

## <a name="azure-redis-cache-connection-string"></a><span data-ttu-id="64f1e-580">Chaîne de connexion au cache des inversions Azure</span><span class="sxs-lookup"><span data-stu-id="64f1e-580">Azure Redis Cache Connection String</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-581">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-581">Format</span></span>

<span data-ttu-id="64f1e-582">La chaîne «ReDim. cache. Windows. <!--no-hyperlink-->net "suivi des caractères et des chaînes décrits dans le modèle ci-dessous, y compris la chaîne" password "ou" PWD ".</span><span class="sxs-lookup"><span data-stu-id="64f1e-582">The string "redis.cache.windows.<!--no-hyperlink-->net" followed by the characters and strings outlined in the pattern below, including the string "password" or "pwd".</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-583">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-583">Pattern</span></span>

- <span data-ttu-id="64f1e-584">La chaîne «ReDim. cache. Windows. <!--no-hyperlink-->net "</span><span class="sxs-lookup"><span data-stu-id="64f1e-584">The string "redis.cache.windows.<!--no-hyperlink-->net"</span></span>
- <span data-ttu-id="64f1e-585">N'importe quelle combinaison entre 1-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="64f1e-585">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="64f1e-586">La chaîne «password» ou «pwd»</span><span class="sxs-lookup"><span data-stu-id="64f1e-586">The string "password" or "pwd"</span></span>
- <span data-ttu-id="64f1e-587">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="64f1e-587">0-2 whitespace characters</span></span>
- <span data-ttu-id="64f1e-588">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="64f1e-588">An equal sign (=)</span></span>
- <span data-ttu-id="64f1e-589">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="64f1e-589">0-2 whitespace characters</span></span>
- <span data-ttu-id="64f1e-590">Toute combinaison de 43 caractères majuscules ou minuscules, des chiffres, une barre oblique (/) ou un signe plus (+)</span><span class="sxs-lookup"><span data-stu-id="64f1e-590">Any combination of 43 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="64f1e-591">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="64f1e-591">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-592">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-592">Checksum</span></span>

<span data-ttu-id="64f1e-593">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-593">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-594">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-594">Definition</span></span>

<span data-ttu-id="64f1e-595">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-595">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-596">L'expression régulière CEP_Regex_AzureRedisCacheConnectionString trouve le contenu qui correspond au modèle..</span><span class="sxs-lookup"><span data-stu-id="64f1e-596">The regular expression CEP_Regex_AzureRedisCacheConnectionString finds content that matches the pattern..</span></span>
- <span data-ttu-id="64f1e-597">L'expression régulière CEP_CommonExampleKeywords ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-597">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```
<!--Azure Redis Cache Connection String-->
<Entity id="095a7e6c-efd8-46d5-af7b-5298d53a49fc" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureRedisCacheConnectionString" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-598">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-598">Keywords</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="64f1e-599">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="64f1e-599">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="64f1e-600">(Notez que techniquement, ce type d'informations sensibles identifie ces mots clés à l'aide d'une expression régulière, et non d'une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="64f1e-600">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="64f1e-601">contoso</span><span class="sxs-lookup"><span data-stu-id="64f1e-601">contoso</span></span>
- <span data-ttu-id="64f1e-602">société</span><span class="sxs-lookup"><span data-stu-id="64f1e-602">fabrikam</span></span>
- <span data-ttu-id="64f1e-603">Northwind</span><span class="sxs-lookup"><span data-stu-id="64f1e-603">northwind</span></span>
- <span data-ttu-id="64f1e-604">immédiatement</span><span class="sxs-lookup"><span data-stu-id="64f1e-604">sandbox</span></span>
- <span data-ttu-id="64f1e-605">OneBox</span><span class="sxs-lookup"><span data-stu-id="64f1e-605">onebox</span></span>
- <span data-ttu-id="64f1e-606">hôte</span><span class="sxs-lookup"><span data-stu-id="64f1e-606">localhost</span></span>
- <span data-ttu-id="64f1e-607">bouclage</span><span class="sxs-lookup"><span data-stu-id="64f1e-607">127.0.0.1</span></span>
- <span data-ttu-id="64f1e-608">TESTACS. <!--no-hyperlink-->com</span><span class="sxs-lookup"><span data-stu-id="64f1e-608">testacs.<!--no-hyperlink-->com</span></span>
- <span data-ttu-id="64f1e-609">s-int.<!--no-hyperlink-->net</span><span class="sxs-lookup"><span data-stu-id="64f1e-609">s-int.<!--no-hyperlink-->net</span></span>

## <a name="azure-sas"></a><span data-ttu-id="64f1e-610">SAS Azure</span><span class="sxs-lookup"><span data-stu-id="64f1e-610">Azure SAS</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-611">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-611">Format</span></span>

<span data-ttu-id="64f1e-612">La chaîne «SIG» suivie des caractères et des chaînes présentés dans le modèle ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="64f1e-612">The string "sig" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-613">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-613">Pattern</span></span>

- <span data-ttu-id="64f1e-614">La chaîne «SIG»</span><span class="sxs-lookup"><span data-stu-id="64f1e-614">The string "sig"</span></span>
- <span data-ttu-id="64f1e-615">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="64f1e-615">0-2 whitespace characters</span></span>
- <span data-ttu-id="64f1e-616">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="64f1e-616">An equal sign (=)</span></span>
- <span data-ttu-id="64f1e-617">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="64f1e-617">0-2 whitespace characters</span></span>
- <span data-ttu-id="64f1e-618">Toute combinaison comprise entre 43-53 caractères majuscules ou minuscules, des chiffres ou le signe pourcentage (%)</span><span class="sxs-lookup"><span data-stu-id="64f1e-618">Any combination of between 43-53 characters that are lower- or uppercase letters, digits, or the percent sign (%)</span></span>
- <span data-ttu-id="64f1e-619">La chaîne «% 3D»</span><span class="sxs-lookup"><span data-stu-id="64f1e-619">The string "%3d"</span></span>
- <span data-ttu-id="64f1e-620">Tout caractère qui n'est pas une lettre majuscule, un chiffre ou un signe de pourcentage (%)</span><span class="sxs-lookup"><span data-stu-id="64f1e-620">Any character that is not a lower- or uppercase letter, digit, or percent sign (%)</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-621">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-621">Checksum</span></span>

<span data-ttu-id="64f1e-622">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-622">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-623">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-623">Definition</span></span>

<span data-ttu-id="64f1e-624">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-624">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-625">L'expression régulière CEP_Regex_AzureSAS trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-625">The regular expression CEP_Regex_AzureSAS finds content that matches the pattern.</span></span>

```
<!--Azure SAS-->
<Entity id="4d235014-e564-47f4-a6fb-6ebb4a826834" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureSAS" />
  </Pattern>
</Entity>
```

## <a name="azure-service-bus-connection-string"></a><span data-ttu-id="64f1e-626">Chaîne de connexion au bus des services Azure</span><span class="sxs-lookup"><span data-stu-id="64f1e-626">Azure Service Bus Connection String</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-627">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-627">Format</span></span>

<span data-ttu-id="64f1e-628">La chaîne «point de terminaison» suivie des caractères et des chaînes décrits dans le modèle ci-dessous, y compris les chaînes «ServiceBus. Windows. <!--no-hyperlink-->net "et" SharedAccesKey ".</span><span class="sxs-lookup"><span data-stu-id="64f1e-628">The string "EndPoint" followed by the characters and strings outlined in the pattern below, including the strings "servicebus.windows.<!--no-hyperlink-->net" and "SharedAccesKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-629">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-629">Pattern</span></span>

- <span data-ttu-id="64f1e-630">Chaîne «point de terminaison»</span><span class="sxs-lookup"><span data-stu-id="64f1e-630">The string "EndPoint"</span></span>
- <span data-ttu-id="64f1e-631">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="64f1e-631">0-2 whitespace characters</span></span>
- <span data-ttu-id="64f1e-632">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="64f1e-632">An equal sign (=)</span></span>
- <span data-ttu-id="64f1e-633">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="64f1e-633">0-2 whitespace characters</span></span>
- <span data-ttu-id="64f1e-634">N'importe quelle combinaison entre 1-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="64f1e-634">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="64f1e-635">La chaîne «ServiceBus. Windows. <!--no-hyperlink-->net "</span><span class="sxs-lookup"><span data-stu-id="64f1e-635">The string "servicebus.windows.<!--no-hyperlink-->net"</span></span>
- <span data-ttu-id="64f1e-636">N'importe quelle combinaison entre 1-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="64f1e-636">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="64f1e-637">La chaîne «SharedAccessKey»</span><span class="sxs-lookup"><span data-stu-id="64f1e-637">The string "SharedAccessKey"</span></span>
- <span data-ttu-id="64f1e-638">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="64f1e-638">0-2 whitespace characters</span></span>
- <span data-ttu-id="64f1e-639">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="64f1e-639">An equal sign (=)</span></span>
- <span data-ttu-id="64f1e-640">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="64f1e-640">0-2 whitespace characters</span></span>
- <span data-ttu-id="64f1e-641">Toute combinaison de 43 caractères majuscules ou minuscules, des chiffres, une barre oblique (/) ou un signe plus (+)</span><span class="sxs-lookup"><span data-stu-id="64f1e-641">Any combination of 43 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="64f1e-642">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="64f1e-642">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-643">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-643">Checksum</span></span>

<span data-ttu-id="64f1e-644">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-644">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-645">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-645">Definition</span></span>

<span data-ttu-id="64f1e-646">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-646">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-647">L'expression régulière CEP_Regex_AzureServiceBusConnectionString trouve le contenu qui correspond au modèle..</span><span class="sxs-lookup"><span data-stu-id="64f1e-647">The regular expression CEP_Regex_AzureServiceBusConnectionString finds content that matches the pattern..</span></span>
- <span data-ttu-id="64f1e-648">L'expression régulière CEP_CommonExampleKeywords ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-648">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```
<!--Azure Service Bus Connection String-->
<Entity id="b9a6578f-a83f-4fcd-bf44-2130bae49a6f" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureServiceBusConnectionString" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-649">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-649">Keywords</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="64f1e-650">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="64f1e-650">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="64f1e-651">(Notez que techniquement, ce type d'informations sensibles identifie ces mots clés à l'aide d'une expression régulière, et non d'une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="64f1e-651">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="64f1e-652">contoso</span><span class="sxs-lookup"><span data-stu-id="64f1e-652">contoso</span></span>
- <span data-ttu-id="64f1e-653">société</span><span class="sxs-lookup"><span data-stu-id="64f1e-653">fabrikam</span></span>
- <span data-ttu-id="64f1e-654">Northwind</span><span class="sxs-lookup"><span data-stu-id="64f1e-654">northwind</span></span>
- <span data-ttu-id="64f1e-655">immédiatement</span><span class="sxs-lookup"><span data-stu-id="64f1e-655">sandbox</span></span>
- <span data-ttu-id="64f1e-656">OneBox</span><span class="sxs-lookup"><span data-stu-id="64f1e-656">onebox</span></span>
- <span data-ttu-id="64f1e-657">hôte</span><span class="sxs-lookup"><span data-stu-id="64f1e-657">localhost</span></span>
- <span data-ttu-id="64f1e-658">bouclage</span><span class="sxs-lookup"><span data-stu-id="64f1e-658">127.0.0.1</span></span>
- <span data-ttu-id="64f1e-659">TESTACS. <!--no-hyperlink-->com</span><span class="sxs-lookup"><span data-stu-id="64f1e-659">testacs.<!--no-hyperlink-->com</span></span>
- <span data-ttu-id="64f1e-660">s-int.<!--no-hyperlink-->net</span><span class="sxs-lookup"><span data-stu-id="64f1e-660">s-int.<!--no-hyperlink-->net</span></span>

## <a name="azure-storage-account-key"></a><span data-ttu-id="64f1e-661">Clé de compte de stockage Azure</span><span class="sxs-lookup"><span data-stu-id="64f1e-661">Azure Storage Account Key</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-662">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-662">Format</span></span>

<span data-ttu-id="64f1e-663">La chaîne «DefaultEndpointsProtocol» suivie des caractères et des chaînes décrits dans le modèle ci-dessous, y compris la chaîne «AccountKey».</span><span class="sxs-lookup"><span data-stu-id="64f1e-663">The string "DefaultEndpointsProtocol" followed by the characters and strings outlined in the pattern below, including the string "AccountKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-664">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-664">Pattern</span></span>

- <span data-ttu-id="64f1e-665">La chaîne «DefaultEndpointsProtocol»</span><span class="sxs-lookup"><span data-stu-id="64f1e-665">The string "DefaultEndpointsProtocol"</span></span>
- <span data-ttu-id="64f1e-666">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="64f1e-666">0-2 whitespace characters</span></span>
- <span data-ttu-id="64f1e-667">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="64f1e-667">An equal sign (=)</span></span>
- <span data-ttu-id="64f1e-668">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="64f1e-668">0-2 whitespace characters</span></span>
- <span data-ttu-id="64f1e-669">N'importe quelle combinaison entre 1-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="64f1e-669">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="64f1e-670">La chaîne «AccountKey»</span><span class="sxs-lookup"><span data-stu-id="64f1e-670">The string "AccountKey"</span></span>
- <span data-ttu-id="64f1e-671">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="64f1e-671">0-2 whitespace characters</span></span>
- <span data-ttu-id="64f1e-672">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="64f1e-672">An equal sign (=)</span></span>
- <span data-ttu-id="64f1e-673">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="64f1e-673">0-2 whitespace characters</span></span>
- <span data-ttu-id="64f1e-674">Toute combinaison de 86 caractères majuscules ou minuscules, des chiffres, une barre oblique (/) ou un signe plus (+)</span><span class="sxs-lookup"><span data-stu-id="64f1e-674">Any combination of 86 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="64f1e-675">Deux signes égal (=)</span><span class="sxs-lookup"><span data-stu-id="64f1e-675">Two equal signs (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-676">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-676">Checksum</span></span>

<span data-ttu-id="64f1e-677">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-677">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-678">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-678">Definition</span></span>

<span data-ttu-id="64f1e-679">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-679">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-680">L'expression régulière CEP_Regex_AzureStorageAccountKey trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-680">The regular expression CEP_Regex_AzureStorageAccountKey finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-681">L'expression régulière CEP_AzureEmulatorStorageAccountFilter ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-681">The regular expression CEP_AzureEmulatorStorageAccountFilter does **not** find content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-682">L'expression régulière CEP_CommonExampleKeywords ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-682">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```
<!--Azure Storage Account Key-->
<Entity id="c7bc98e8-551a-4c35-a92d-d2c8cda714a7" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureStorageAccountKey" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_AzureEmulatorStorageAccountFilter" />
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-683">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-683">Keywords</span></span>

#### <a name="cepazureemulatorstorageaccountfilter"></a><span data-ttu-id="64f1e-684">CEP_AzureEmulatorStorageAccountFilter</span><span class="sxs-lookup"><span data-stu-id="64f1e-684">CEP_AzureEmulatorStorageAccountFilter</span></span>

<span data-ttu-id="64f1e-685">(Notez que techniquement, ce type d'informations sensibles identifie ces mots clés à l'aide d'une expression régulière, et non d'une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="64f1e-685">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="64f1e-686">Eby8vdM02xNOcqFlqUwJPLlmEtlCDXJ1OUzFT50uSRZ6IFsuFq2UVErCz4I6tq/K1SZFPTOtr/KBHBeksoGMGw = =</span><span class="sxs-lookup"><span data-stu-id="64f1e-686">Eby8vdM02xNOcqFlqUwJPLlmEtlCDXJ1OUzFT50uSRZ6IFsuFq2UVErCz4I6tq/K1SZFPTOtr/KBHBeksoGMGw==</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="64f1e-687">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="64f1e-687">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="64f1e-688">(Notez que techniquement, ce type d'informations sensibles identifie ces mots clés à l'aide d'une expression régulière, et non d'une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="64f1e-688">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="64f1e-689">contoso</span><span class="sxs-lookup"><span data-stu-id="64f1e-689">contoso</span></span>
- <span data-ttu-id="64f1e-690">société</span><span class="sxs-lookup"><span data-stu-id="64f1e-690">fabrikam</span></span>
- <span data-ttu-id="64f1e-691">Northwind</span><span class="sxs-lookup"><span data-stu-id="64f1e-691">northwind</span></span>
- <span data-ttu-id="64f1e-692">immédiatement</span><span class="sxs-lookup"><span data-stu-id="64f1e-692">sandbox</span></span>
- <span data-ttu-id="64f1e-693">OneBox</span><span class="sxs-lookup"><span data-stu-id="64f1e-693">onebox</span></span>
- <span data-ttu-id="64f1e-694">hôte</span><span class="sxs-lookup"><span data-stu-id="64f1e-694">localhost</span></span>
- <span data-ttu-id="64f1e-695">bouclage</span><span class="sxs-lookup"><span data-stu-id="64f1e-695">127.0.0.1</span></span>
- <span data-ttu-id="64f1e-696">TESTACS. <!--no-hyperlink-->com</span><span class="sxs-lookup"><span data-stu-id="64f1e-696">testacs.<!--no-hyperlink-->com</span></span>
- <span data-ttu-id="64f1e-697">s-int.<!--no-hyperlink-->net</span><span class="sxs-lookup"><span data-stu-id="64f1e-697">s-int.<!--no-hyperlink-->net</span></span>

## <a name="azure-storage-account-key-generic"></a><span data-ttu-id="64f1e-698">Clé de compte de stockage Azure (Générique)</span><span class="sxs-lookup"><span data-stu-id="64f1e-698">Azure Storage Account Key (Generic)</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-699">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-699">Format</span></span>

<span data-ttu-id="64f1e-700">Toute combinaison de 86 lettres majuscules ou minuscules, des chiffres, la barre oblique (/) ou le signe plus (+), précédée ou suivie des caractères décrits dans le modèle ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="64f1e-700">Any combination of 86 lower- or uppercase letters, digits, the forward slash (/), or plus sign (+), preceded or followed by the characters outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-701">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-701">Pattern</span></span>

- <span data-ttu-id="64f1e-702">0-1 du symbole supérieur à (>), apostrophe ('), signe égal (=), guillemet (") ou dièse (#)</span><span class="sxs-lookup"><span data-stu-id="64f1e-702">0-1 of the greater than symbol (>), apostrophe ('), equal sign (=), quotation mark ("), or number sign (#)</span></span>
- <span data-ttu-id="64f1e-703">Toute combinaison de 86 caractères majuscules ou minuscules, des chiffres, la barre oblique (/) ou le signe plus (+)</span><span class="sxs-lookup"><span data-stu-id="64f1e-703">Any combination of 86 characters that are lower- or uppercase letters, digits, the forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="64f1e-704">Deux signes égal (=)</span><span class="sxs-lookup"><span data-stu-id="64f1e-704">Two equal signs (=)</span></span>


### <a name="checksum"></a><span data-ttu-id="64f1e-705">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-705">Checksum</span></span>

<span data-ttu-id="64f1e-706">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-706">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-707">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-707">Definition</span></span>

<span data-ttu-id="64f1e-708">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-708">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-709">L'expression régulière CEP_Regex_AzureStorageAccountKeyGeneric trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-709">The regular expression CEP_Regex_AzureStorageAccountKeyGeneric finds content that matches the pattern.</span></span>

```
<!--Azure Storage Account Key (Generic)-->
<Entity id="7ff41bd0-5419-4523-91d6-383b3a37f084" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureStorageAccountKeyGeneric" />
  </Pattern>
</Entity>
```

## <a name="belgium-national-number"></a><span data-ttu-id="64f1e-710">Numéro national Belgique</span><span class="sxs-lookup"><span data-stu-id="64f1e-710">Belgium National Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-711">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-711">Format</span></span>

<span data-ttu-id="64f1e-712">11 chiffres plus des délimiteurs</span><span class="sxs-lookup"><span data-stu-id="64f1e-712">11 digits plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-713">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-713">Pattern</span></span>

<span data-ttu-id="64f1e-714">11 chiffres plus des délimiteurs :</span><span class="sxs-lookup"><span data-stu-id="64f1e-714">11 digits plus delimiters:</span></span>
- <span data-ttu-id="64f1e-715">Six chiffres et deux points au format AA.MM.JJ pour la date de naissance </span><span class="sxs-lookup"><span data-stu-id="64f1e-715">Six digits and two periods in the format YY.MM.DD for date of birth</span></span> 
- <span data-ttu-id="64f1e-716">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="64f1e-716">A hyphen</span></span> 
- <span data-ttu-id="64f1e-717">Trois chiffres séquentiels (impairs pour les hommes, pairs pour les femmes) </span><span class="sxs-lookup"><span data-stu-id="64f1e-717">Three sequential digits (odd for males, even for females)</span></span> 
- <span data-ttu-id="64f1e-718">Un point</span><span class="sxs-lookup"><span data-stu-id="64f1e-718">A period</span></span> 
- <span data-ttu-id="64f1e-719">Deux chiffres de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-719">Two digits that are a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-720">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-720">Checksum</span></span>

<span data-ttu-id="64f1e-721">Oui</span><span class="sxs-lookup"><span data-stu-id="64f1e-721">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-722">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-722">Definition</span></span>

<span data-ttu-id="64f1e-723">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-723">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-724">La fonction Func_belgium_national_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-724">The function Func_belgium_national_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-725">Un mot clé figurant dans la liste Keyword_belgium_national_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-725">A keyword from Keyword_belgium_national_number is found.</span></span>
- <span data-ttu-id="64f1e-726">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-726">The checksum passes.</span></span>

```
<!-- Belgium National Number -->
  <Entity id="fb969c9e-0fd1-4b18-8091-a2123c5e6a54" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_belgium_national_number"/>
     <Match idRef="Keyword_belgium_national_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-727">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-727">Keywords</span></span>

#### <a name="keywordbelgiumnationalnumber"></a><span data-ttu-id="64f1e-728">Keyword_belgium_national_number</span><span class="sxs-lookup"><span data-stu-id="64f1e-728">Keyword_belgium_national_number</span></span>

- <span data-ttu-id="64f1e-729">Identité</span><span class="sxs-lookup"><span data-stu-id="64f1e-729">Identity</span></span>
- <span data-ttu-id="64f1e-730">Son</span><span class="sxs-lookup"><span data-stu-id="64f1e-730">Registration</span></span>
- <span data-ttu-id="64f1e-731">Identificateur</span><span class="sxs-lookup"><span data-stu-id="64f1e-731">Identification</span></span> 
- <span data-ttu-id="64f1e-732">ID</span><span class="sxs-lookup"><span data-stu-id="64f1e-732">ID</span></span> 
- <span data-ttu-id="64f1e-733">Identiteitskaart</span><span class="sxs-lookup"><span data-stu-id="64f1e-733">Identiteitskaart</span></span>
- <span data-ttu-id="64f1e-734">Registratie nummer</span><span class="sxs-lookup"><span data-stu-id="64f1e-734">Registratie nummer</span></span> 
- <span data-ttu-id="64f1e-735">Identificatie nummer</span><span class="sxs-lookup"><span data-stu-id="64f1e-735">Identificatie nummer</span></span> 
- <span data-ttu-id="64f1e-736">Identiteit</span><span class="sxs-lookup"><span data-stu-id="64f1e-736">Identiteit</span></span>
- <span data-ttu-id="64f1e-737">Registratie</span><span class="sxs-lookup"><span data-stu-id="64f1e-737">Registratie</span></span>
- <span data-ttu-id="64f1e-738">Identificatie</span><span class="sxs-lookup"><span data-stu-id="64f1e-738">Identificatie</span></span> 
- <span data-ttu-id="64f1e-739">Carte d’identité</span><span class="sxs-lookup"><span data-stu-id="64f1e-739">Carte d’identité</span></span> 
- <span data-ttu-id="64f1e-740">numéro d’immatriculation</span><span class="sxs-lookup"><span data-stu-id="64f1e-740">numéro d'immatriculation</span></span>
- <span data-ttu-id="64f1e-741">numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="64f1e-741">numéro d'identification</span></span>
- <span data-ttu-id="64f1e-742">identité</span><span class="sxs-lookup"><span data-stu-id="64f1e-742">identité</span></span> 
- <span data-ttu-id="64f1e-743">inscriptions</span><span class="sxs-lookup"><span data-stu-id="64f1e-743">inscription</span></span> 
- <span data-ttu-id="64f1e-744">Identifikation</span><span class="sxs-lookup"><span data-stu-id="64f1e-744">Identifikation</span></span>
- <span data-ttu-id="64f1e-745">Identifizierung</span><span class="sxs-lookup"><span data-stu-id="64f1e-745">Identifizierung</span></span>
- <span data-ttu-id="64f1e-746">Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="64f1e-746">Identifikationsnummer</span></span>
- <span data-ttu-id="64f1e-747">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="64f1e-747">Personalausweis</span></span>
- <span data-ttu-id="64f1e-748">Registrierung</span><span class="sxs-lookup"><span data-stu-id="64f1e-748">Registrierung</span></span>
- <span data-ttu-id="64f1e-749">Registrationsnummer</span><span class="sxs-lookup"><span data-stu-id="64f1e-749">Registrationsnummer</span></span>

   
## <a name="brazil-cpf-number"></a><span data-ttu-id="64f1e-750">Numéro CPF Brésil</span><span class="sxs-lookup"><span data-stu-id="64f1e-750">Brazil CPF Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-751">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-751">Format</span></span>

<span data-ttu-id="64f1e-752">11 chiffres qui incluent un chiffre de contrôle et peuvent ou non être mis en forme </span><span class="sxs-lookup"><span data-stu-id="64f1e-752">11 digits that include a check digit and can be formatted or unformatted</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-753">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-753">Pattern</span></span>

<span data-ttu-id="64f1e-754">Avec</span><span class="sxs-lookup"><span data-stu-id="64f1e-754">Formatted:</span></span>
- <span data-ttu-id="64f1e-755">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-755">Three digits</span></span> 
- <span data-ttu-id="64f1e-756">Un point </span><span class="sxs-lookup"><span data-stu-id="64f1e-756">A period</span></span> 
- <span data-ttu-id="64f1e-757">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-757">Three digits</span></span> 
- <span data-ttu-id="64f1e-758">Un point </span><span class="sxs-lookup"><span data-stu-id="64f1e-758">A period</span></span> 
- <span data-ttu-id="64f1e-759">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-759">Three digits</span></span> 
- <span data-ttu-id="64f1e-760">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="64f1e-760">A hyphen</span></span> 
- <span data-ttu-id="64f1e-761">Deux chiffres de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-761">Two digits which are check digits</span></span>

<span data-ttu-id="64f1e-762">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-762">Unformatted:</span></span>
- <span data-ttu-id="64f1e-763">11 chiffres où les deux derniers sont des chiffres de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-763">11 digits where the last two digits are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-764">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-764">Checksum</span></span>

<span data-ttu-id="64f1e-765">Oui</span><span class="sxs-lookup"><span data-stu-id="64f1e-765">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-766">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-766">Definition</span></span>

<span data-ttu-id="64f1e-767">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-767">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-768">La fonction Func_brazil_cpf trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-768">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-769">Un mot clé figurant dans la liste Keyword_brazil_cpf est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-769">A keyword from Keyword_brazil_cpf is found.</span></span>
- <span data-ttu-id="64f1e-770">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-770">The checksum passes.</span></span>

<span data-ttu-id="64f1e-771">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-771">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-772">La fonction Func_brazil_cpf trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-772">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-773">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-773">The checksum passes.</span></span>

```
<!-- Brazil CPF Number -->
<Entity id="78e09124-f2c3-4656-b32a-c1a132cd2711" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_brazil_cpf"/>
     <Match idRef="Keyword_brazil_cpf"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_brazil_cpf"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-774">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-774">Keywords</span></span>

#### <a name="keywordbrazilcpf"></a><span data-ttu-id="64f1e-775">Keyword_brazil_cpf</span><span class="sxs-lookup"><span data-stu-id="64f1e-775">Keyword_brazil_cpf</span></span>

- <span data-ttu-id="64f1e-776">CPF</span><span class="sxs-lookup"><span data-stu-id="64f1e-776">CPF</span></span>
- <span data-ttu-id="64f1e-777">Identificateur</span><span class="sxs-lookup"><span data-stu-id="64f1e-777">Identification</span></span>
- <span data-ttu-id="64f1e-778">Son</span><span class="sxs-lookup"><span data-stu-id="64f1e-778">Registration</span></span>
- <span data-ttu-id="64f1e-779">Parts</span><span class="sxs-lookup"><span data-stu-id="64f1e-779">Revenue</span></span>
- <span data-ttu-id="64f1e-780">Cadastro de Pessoas Físicas</span><span class="sxs-lookup"><span data-stu-id="64f1e-780">Cadastro de Pessoas Físicas</span></span> 
- <span data-ttu-id="64f1e-781">Imposto</span><span class="sxs-lookup"><span data-stu-id="64f1e-781">Imposto</span></span> 
- <span data-ttu-id="64f1e-782">Identificação</span><span class="sxs-lookup"><span data-stu-id="64f1e-782">Identificação</span></span> 
- <span data-ttu-id="64f1e-783">Inscrição</span><span class="sxs-lookup"><span data-stu-id="64f1e-783">Inscrição</span></span> 
- <span data-ttu-id="64f1e-784">Receita</span><span class="sxs-lookup"><span data-stu-id="64f1e-784">Receita</span></span> 
   
## <a name="brazil-legal-entity-number-cnpj"></a><span data-ttu-id="64f1e-785">Numéro d’entité juridique (CNPJ) Brésil</span><span class="sxs-lookup"><span data-stu-id="64f1e-785">Brazil Legal Entity Number (CNPJ)</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-786">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-786">Format</span></span>

<span data-ttu-id="64f1e-787">14 chiffres qui incluent un numéro d’enregistrement, un numéro de succursale et des chiffres de contrôle, avec des délimiteurs en plus</span><span class="sxs-lookup"><span data-stu-id="64f1e-787">14 digits that include a registration number, branch number, and check digits, plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-788">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-788">Pattern</span></span>
<span data-ttu-id="64f1e-789">14 chiffres plus des délimiteurs :</span><span class="sxs-lookup"><span data-stu-id="64f1e-789">14 digits, plus delimiters:</span></span>
- <span data-ttu-id="64f1e-790">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-790">Two digits</span></span> 
- <span data-ttu-id="64f1e-791">Un point </span><span class="sxs-lookup"><span data-stu-id="64f1e-791">A period</span></span> 
- <span data-ttu-id="64f1e-792">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-792">Three digits</span></span> 
- <span data-ttu-id="64f1e-793">Un point </span><span class="sxs-lookup"><span data-stu-id="64f1e-793">A period</span></span> 
- <span data-ttu-id="64f1e-794">Trois chiffres (ces huit premiers chiffres composent le numéro d’enregistrement) </span><span class="sxs-lookup"><span data-stu-id="64f1e-794">Three digits (these first eight digits are the registration number)</span></span> 
- <span data-ttu-id="64f1e-795">Une barre oblique </span><span class="sxs-lookup"><span data-stu-id="64f1e-795">A forward slash</span></span> 
- <span data-ttu-id="64f1e-796">Le numéro de succursale à quatre chiffres </span><span class="sxs-lookup"><span data-stu-id="64f1e-796">Four-digit branch number</span></span> 
- <span data-ttu-id="64f1e-797">Un trait d’union</span><span class="sxs-lookup"><span data-stu-id="64f1e-797">A hyphen</span></span> 
- <span data-ttu-id="64f1e-798">Deux chiffres de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-798">Two digits which are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-799">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-799">Checksum</span></span>

<span data-ttu-id="64f1e-800">Oui</span><span class="sxs-lookup"><span data-stu-id="64f1e-800">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-801">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-801">Definition</span></span>

<span data-ttu-id="64f1e-802">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-802">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-803">La fonction Func_brazil_cnpj trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-803">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-804">Un mot clé figurant dans la liste Keyword_brazil_cnpj est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-804">A keyword from Keyword_brazil_cnpj is found.</span></span>
- <span data-ttu-id="64f1e-805">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-805">The checksum passes.</span></span>

<span data-ttu-id="64f1e-806">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-806">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-807">La fonction Func_brazil_cnpj trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-807">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-808">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-808">The checksum passes.</span></span>

```
<!-- Brazil Legal Entity Number (CNPJ) -->
<Entity id="9b58b5cd-5e90-4df6-b34f-1ebcc88ceae4" recommendedConfidence="85" patternsProximity="300">
   <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_brazil_cnpj"/>
     <Match idRef="Keyword_brazil_cnpj"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_brazil_cnpj"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-809">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-809">Keywords</span></span>

#### <a name="keywordbrazilcnpj"></a><span data-ttu-id="64f1e-810">Keyword_brazil_cnpj</span><span class="sxs-lookup"><span data-stu-id="64f1e-810">Keyword_brazil_cnpj</span></span>

- <span data-ttu-id="64f1e-811">CNPJ</span><span class="sxs-lookup"><span data-stu-id="64f1e-811">CNPJ</span></span> 
- <span data-ttu-id="64f1e-812">CNPJ/MF</span><span class="sxs-lookup"><span data-stu-id="64f1e-812">CNPJ/MF</span></span> 
- <span data-ttu-id="64f1e-813">CNPJ-MF</span><span class="sxs-lookup"><span data-stu-id="64f1e-813">CNPJ-MF</span></span> 
- <span data-ttu-id="64f1e-814">National Registry of Legal Entities</span><span class="sxs-lookup"><span data-stu-id="64f1e-814">National Registry of Legal Entities</span></span> 
- <span data-ttu-id="64f1e-815">Taxpayers Registry</span><span class="sxs-lookup"><span data-stu-id="64f1e-815">Taxpayers Registry</span></span> 
- <span data-ttu-id="64f1e-816">Legal entity</span><span class="sxs-lookup"><span data-stu-id="64f1e-816">Legal entity</span></span> 
- <span data-ttu-id="64f1e-817">Legal entities</span><span class="sxs-lookup"><span data-stu-id="64f1e-817">Legal entities</span></span> 
- <span data-ttu-id="64f1e-818">Registration Status</span><span class="sxs-lookup"><span data-stu-id="64f1e-818">Registration Status</span></span> 
- <span data-ttu-id="64f1e-819">Business</span><span class="sxs-lookup"><span data-stu-id="64f1e-819">Business</span></span> 
- <span data-ttu-id="64f1e-820">Company</span><span class="sxs-lookup"><span data-stu-id="64f1e-820">Company</span></span>
- <span data-ttu-id="64f1e-821">CNPJ</span><span class="sxs-lookup"><span data-stu-id="64f1e-821">CNPJ</span></span> 
- <span data-ttu-id="64f1e-822">Cadastro Nacional da Pessoa Jurídica</span><span class="sxs-lookup"><span data-stu-id="64f1e-822">Cadastro Nacional da Pessoa Jurídica</span></span> 
- <span data-ttu-id="64f1e-823">Cadastro Geral de Contribuintes</span><span class="sxs-lookup"><span data-stu-id="64f1e-823">Cadastro Geral de Contribuintes</span></span> 
- <span data-ttu-id="64f1e-824">CGC</span><span class="sxs-lookup"><span data-stu-id="64f1e-824">CGC</span></span> 
- <span data-ttu-id="64f1e-825">Pessoa jurídica</span><span class="sxs-lookup"><span data-stu-id="64f1e-825">Pessoa jurídica</span></span> 
- <span data-ttu-id="64f1e-826">Pessoas jurídicas</span><span class="sxs-lookup"><span data-stu-id="64f1e-826">Pessoas jurídicas</span></span> 
- <span data-ttu-id="64f1e-827">Situação cadastral</span><span class="sxs-lookup"><span data-stu-id="64f1e-827">Situação cadastral</span></span> 
- <span data-ttu-id="64f1e-828">Inscrição</span><span class="sxs-lookup"><span data-stu-id="64f1e-828">Inscrição</span></span> 
- <span data-ttu-id="64f1e-829">Empresa</span><span class="sxs-lookup"><span data-stu-id="64f1e-829">Empresa</span></span> 
   
## <a name="brazil-national-id-card-rg"></a><span data-ttu-id="64f1e-830">	Brazil National ID Card (RG)</span><span class="sxs-lookup"><span data-stu-id="64f1e-830">Brazil National ID Card (RG)</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-831">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-831">Format</span></span>

<span data-ttu-id="64f1e-832">Registro Geral (ancien format): neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-832">Registro Geral (old format): Nine digits</span></span>

<span data-ttu-id="64f1e-833">Registro de identidade (RIC) (nouveau format): 11 chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-833">Registro de Identidade (RIC) (new format): 11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-834">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-834">Pattern</span></span>

<span data-ttu-id="64f1e-835">Registro Geral (ancien format) :</span><span class="sxs-lookup"><span data-stu-id="64f1e-835">Registro Geral (old format):</span></span>
- <span data-ttu-id="64f1e-836">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-836">Two digits</span></span> 
- <span data-ttu-id="64f1e-837">Un point </span><span class="sxs-lookup"><span data-stu-id="64f1e-837">A period</span></span> 
- <span data-ttu-id="64f1e-838">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-838">Three digits</span></span> 
- <span data-ttu-id="64f1e-839">Un point </span><span class="sxs-lookup"><span data-stu-id="64f1e-839">A period</span></span> 
- <span data-ttu-id="64f1e-840">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-840">Three digits</span></span> 
- <span data-ttu-id="64f1e-841">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="64f1e-841">A hyphen</span></span> 
- <span data-ttu-id="64f1e-842">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-842">One digit which is a check digit</span></span>

<span data-ttu-id="64f1e-843">Registro de identidade (RIC) (nouveau format):</span><span class="sxs-lookup"><span data-stu-id="64f1e-843">Registro de Identidade (RIC) (new format):</span></span>
- <span data-ttu-id="64f1e-844">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-844">10 digits</span></span> 
- <span data-ttu-id="64f1e-845">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="64f1e-845">A hyphen</span></span> 
- <span data-ttu-id="64f1e-846">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-846">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-847">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-847">Checksum</span></span>

<span data-ttu-id="64f1e-848">Oui</span><span class="sxs-lookup"><span data-stu-id="64f1e-848">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-849">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-849">Definition</span></span>

<span data-ttu-id="64f1e-850">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-850">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-851">La fonction Func_brazil_rg trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-851">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-852">Un mot clé figurant dans la liste Keyword_brazil_rg est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-852">A keyword from Keyword_brazil_rg is found.</span></span>
- <span data-ttu-id="64f1e-853">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-853">The checksum passes.</span></span>

<span data-ttu-id="64f1e-854">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-854">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-855">La fonction Func_brazil_rg trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-855">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-856">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-856">The checksum passes.</span></span>

```
<!-- Brazil National ID Card (RG) -->
<Entity id="486de900-db70-41b3-a886-abdf25af119c" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_brazil_rg"/>
     <Match idRef="Keyword_brazil_rg"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_brazil_rg"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-857">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-857">Keywords</span></span>

#### <a name="keywordbrazilrg"></a><span data-ttu-id="64f1e-858">Keyword_brazil_rg</span><span class="sxs-lookup"><span data-stu-id="64f1e-858">Keyword_brazil_rg</span></span>

<span data-ttu-id="64f1e-859">Cédula de identidade carte d'identité número de rregistro Registro de identidade Registro Geral RG (ce mot clé respecte la casse) RIC (ce mot clé respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="64f1e-859">Cédula de identidade identity card national id número de rregistro registro de Iidentidade registro geral RG (this keyword is case sensitive) RIC (this keyword is case sensitive)</span></span> 
   
## <a name="canada-bank-account-number"></a><span data-ttu-id="64f1e-860">Numéro de compte bancaire Canada</span><span class="sxs-lookup"><span data-stu-id="64f1e-860">Canada Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-861">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-861">Format</span></span>

<span data-ttu-id="64f1e-862">Sept ou douze chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-862">Seven or twelve digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-863">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-863">Pattern</span></span>

<span data-ttu-id="64f1e-864">Un numéro de compte bancaire au Canada est composé de sept ou douze chiffres.</span><span class="sxs-lookup"><span data-stu-id="64f1e-864">A Canada Bank Account Number is seven or twelve digits.</span></span>

<span data-ttu-id="64f1e-865">Un numéro de transit de compte bancaire du Canada est indiqué au format suivant :</span><span class="sxs-lookup"><span data-stu-id="64f1e-865">A Canada bank account transit number is:</span></span>
- <span data-ttu-id="64f1e-866">Cinq chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-866">Five digits</span></span> 
- <span data-ttu-id="64f1e-867">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="64f1e-867">A hyphen</span></span> 
- <span data-ttu-id="64f1e-868">Trois chiffres ou</span><span class="sxs-lookup"><span data-stu-id="64f1e-868">Three digits OR</span></span>
- <span data-ttu-id="64f1e-869">Un zéro « 0 » </span><span class="sxs-lookup"><span data-stu-id="64f1e-869">A zero "0"</span></span> 
- <span data-ttu-id="64f1e-870">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-870">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-871">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-871">Checksum</span></span>

<span data-ttu-id="64f1e-872">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-872">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-873">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-873">Definition</span></span>

<span data-ttu-id="64f1e-874">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-874">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-875">L’expression régulière Regex_canada_bank_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-875">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-876">Un mot clé figurant dans la liste Keyword_canada_bank_account_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-876">A keyword from Keyword_canada_bank_account_number is found.</span></span>
- <span data-ttu-id="64f1e-877">L’expression régulière Regex_canada_bank_account_transit_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-877">The regular expression Regex_canada_bank_account_transit_number finds content that matches the pattern.</span></span>

<span data-ttu-id="64f1e-878">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-878">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-879">L’expression régulière Regex_canada_bank_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-879">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-880">Un mot clé figurant dans la liste Keyword_canada_bank_account_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-880">A keyword from Keyword_canada_bank_account_number is found.</span></span>

```
<!-- Canada Bank Account Number -->
<Entity id="552e814c-cb50-4d94-bbaa-bb1d1ffb34de" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Regex_canada_bank_account_number" />
        <Match idRef="Keyword_canada_bank_account_number" />
        <Match idRef="Regex_canada_bank_account_transit_number" />
   </Pattern>
   <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_canada_bank_account_number" />
        <Match idRef="Keyword_canada_bank_account_number" />
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-881">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-881">Keywords</span></span>

#### <a name="keywordcanadabankaccountnumber"></a><span data-ttu-id="64f1e-882">Keyword_canada_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="64f1e-882">Keyword_canada_bank_account_number</span></span>

- <span data-ttu-id="64f1e-883">obligations d’épargne du Canada</span><span class="sxs-lookup"><span data-stu-id="64f1e-883">canada savings bonds</span></span>
- <span data-ttu-id="64f1e-884">agence du revenu du Canada</span><span class="sxs-lookup"><span data-stu-id="64f1e-884">canada revenue agency</span></span>
- <span data-ttu-id="64f1e-885">institution financière du Canada</span><span class="sxs-lookup"><span data-stu-id="64f1e-885">canadian financial institution</span></span>
- <span data-ttu-id="64f1e-886">formulaire de dépôt direct</span><span class="sxs-lookup"><span data-stu-id="64f1e-886">direct deposit form</span></span>
- <span data-ttu-id="64f1e-887">citoyen canadien</span><span class="sxs-lookup"><span data-stu-id="64f1e-887">canadian citizen</span></span>
- <span data-ttu-id="64f1e-888">représentant légal</span><span class="sxs-lookup"><span data-stu-id="64f1e-888">legal representative</span></span>
- <span data-ttu-id="64f1e-889">notaire</span><span class="sxs-lookup"><span data-stu-id="64f1e-889">notary public</span></span>
- <span data-ttu-id="64f1e-890">commissaire à l’assermentation</span><span class="sxs-lookup"><span data-stu-id="64f1e-890">commissioner for oaths</span></span>
- <span data-ttu-id="64f1e-891">prestation pour la garde d’enfants</span><span class="sxs-lookup"><span data-stu-id="64f1e-891">child care benefit</span></span>
- <span data-ttu-id="64f1e-892">prestation universelle pour la garde d’enfants</span><span class="sxs-lookup"><span data-stu-id="64f1e-892">universal child care</span></span>
- <span data-ttu-id="64f1e-893">prestation fiscale canadienne pour enfants</span><span class="sxs-lookup"><span data-stu-id="64f1e-893">canada child tax benefit</span></span>
- <span data-ttu-id="64f1e-894">prestation fiscale pour le revenu gagné</span><span class="sxs-lookup"><span data-stu-id="64f1e-894">income tax benefit</span></span>
- <span data-ttu-id="64f1e-895">taxe de vente harmonisée</span><span class="sxs-lookup"><span data-stu-id="64f1e-895">harmonized sales tax</span></span>
- <span data-ttu-id="64f1e-896">numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="64f1e-896">social insurance number</span></span>
- <span data-ttu-id="64f1e-897">remboursement d’impôt</span><span class="sxs-lookup"><span data-stu-id="64f1e-897">income tax refund</span></span>
- <span data-ttu-id="64f1e-898">prestation fiscale pour enfants</span><span class="sxs-lookup"><span data-stu-id="64f1e-898">child tax benefit</span></span>
- <span data-ttu-id="64f1e-899">paiements aux territoires</span><span class="sxs-lookup"><span data-stu-id="64f1e-899">territorial payments</span></span>
- <span data-ttu-id="64f1e-900">numéro d’institution</span><span class="sxs-lookup"><span data-stu-id="64f1e-900">institution number</span></span>
- <span data-ttu-id="64f1e-901">demande de dépôt</span><span class="sxs-lookup"><span data-stu-id="64f1e-901">deposit request</span></span>
- <span data-ttu-id="64f1e-902">informations bancaires</span><span class="sxs-lookup"><span data-stu-id="64f1e-902">banking information</span></span>
- <span data-ttu-id="64f1e-903">dépôt direct</span><span class="sxs-lookup"><span data-stu-id="64f1e-903">direct deposit</span></span>
   
## <a name="canada-drivers-license-number"></a><span data-ttu-id="64f1e-904">Numéro de permis de conduire Canada</span><span class="sxs-lookup"><span data-stu-id="64f1e-904">Canada Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-905">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-905">Format</span></span>

<span data-ttu-id="64f1e-906">Varie selon la province</span><span class="sxs-lookup"><span data-stu-id="64f1e-906">Varies by province</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-907">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-907">Pattern</span></span>

<span data-ttu-id="64f1e-908">Plusieurs modèles pour les différentes provinces : Alberta, Colombie-Britannique, Manitoba, Nouveau-Brunswick, Terre-Neuve-et-Labrador, Nouvelle-Écosse, Ontario, Île-du-Prince-Édouard, Québec et Saskatchewan</span><span class="sxs-lookup"><span data-stu-id="64f1e-908">Various patterns covering Alberta, British Columbia, Manitoba, New Brunswick, Newfoundland/Labrador, Nova Scotia, Ontario, Prince Edward Island, Quebec, and Saskatchewan</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-909">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-909">Checksum</span></span>

<span data-ttu-id="64f1e-910">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-910">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-911">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-911">Definition</span></span>

<span data-ttu-id="64f1e-912">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-912">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-913">La fonction Func_[province_name]_drivers_license_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-913">The function Func_[province_name]_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-914">Un mot clé figurant dans la liste Keyword_[province_name]_drivers_license_name est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-914">A keyword from Keyword_[province_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="64f1e-915">Un mot clé figurant dans la liste Keyword_canada_drivers_license est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-915">A keyword from Keyword_canada_drivers_license is found.</span></span>

```
<!-- Canada Driver's License Number -->
    <Entity id="37186abb-8e48-4800-ad3c-e3d1610b3db0" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_alberta_drivers_license_number" />
        <Match idRef="Keyword_alberta_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_british_columbia_drivers_license_number" />
        <Match idRef="Keyword_british_columbia_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_manitoba_drivers_license_number" />
        <Match idRef="Keyword_manitoba_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_new_brunswick_drivers_license_number" />
        <Match idRef="Keyword_new_brunswick_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_newfoundland_labrador_drivers_license_number" />
        <Match idRef="Keyword_newfoundland_labrador_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_nova_scotia_drivers_license_number" />
        <Match idRef="Keyword_nova_scotia_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_ontario_drivers_license_number" />
        <Match idRef="Keyword_ontario_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_prince_edward_island_drivers_license_number" />
        <Match idRef="Keyword_prince_edward_island_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_quebec_drivers_license_number" />
        <Match idRef="Keyword_quebec_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_saskatchewan_drivers_license_number" />
        <Match idRef="Keyword_saskatchewan_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
    </Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-916">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-916">Keywords</span></span>

#### <a name="keywordprovincenamedriverslicensename"></a><span data-ttu-id="64f1e-917">Keyword_ [province_name] _drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="64f1e-917">Keyword_[province_name]_drivers_license_name</span></span>

- <span data-ttu-id="64f1e-918">L’abréviation de la province, par exemple AB</span><span class="sxs-lookup"><span data-stu-id="64f1e-918">The province abbreviation, for example AB</span></span>
- <span data-ttu-id="64f1e-919">Le nom de la province, par exemple Alberta</span><span class="sxs-lookup"><span data-stu-id="64f1e-919">The province name, for example Alberta</span></span>

#### <a name="keywordcanadadriverslicense"></a><span data-ttu-id="64f1e-920">Keyword_canada_drivers_license</span><span class="sxs-lookup"><span data-stu-id="64f1e-920">Keyword_canada_drivers_license</span></span>

- <span data-ttu-id="64f1e-921">LD</span><span class="sxs-lookup"><span data-stu-id="64f1e-921">DL</span></span>
- <span data-ttu-id="64f1e-922">DISTRIBUTION</span><span class="sxs-lookup"><span data-stu-id="64f1e-922">DLS</span></span>
- <span data-ttu-id="64f1e-923">CÈDE</span><span class="sxs-lookup"><span data-stu-id="64f1e-923">CDL</span></span>
- <span data-ttu-id="64f1e-924">CDLS</span><span class="sxs-lookup"><span data-stu-id="64f1e-924">CDLS</span></span>
- <span data-ttu-id="64f1e-925">DriverLic</span><span class="sxs-lookup"><span data-stu-id="64f1e-925">DriverLic</span></span>
- <span data-ttu-id="64f1e-926">DriverLics</span><span class="sxs-lookup"><span data-stu-id="64f1e-926">DriverLics</span></span>
- <span data-ttu-id="64f1e-927">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="64f1e-927">DriverLicense</span></span>
- <span data-ttu-id="64f1e-928">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="64f1e-928">DriverLicenses</span></span>
- <span data-ttu-id="64f1e-929">DriverLicence</span><span class="sxs-lookup"><span data-stu-id="64f1e-929">DriverLicence</span></span>
- <span data-ttu-id="64f1e-930">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="64f1e-930">DriverLicences</span></span>
- <span data-ttu-id="64f1e-931">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-931">Driver Lic</span></span>
- <span data-ttu-id="64f1e-932">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-932">Driver Lics</span></span>
- <span data-ttu-id="64f1e-933">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-933">Driver License</span></span>
- <span data-ttu-id="64f1e-934">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-934">Driver Licenses</span></span>
- <span data-ttu-id="64f1e-935">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-935">Driver Licence</span></span>
- <span data-ttu-id="64f1e-936">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-936">Driver Licences</span></span>
- <span data-ttu-id="64f1e-937">DriversLic</span><span class="sxs-lookup"><span data-stu-id="64f1e-937">DriversLic</span></span>
- <span data-ttu-id="64f1e-938">DriversLics</span><span class="sxs-lookup"><span data-stu-id="64f1e-938">DriversLics</span></span>
- <span data-ttu-id="64f1e-939">DriversLicence</span><span class="sxs-lookup"><span data-stu-id="64f1e-939">DriversLicence</span></span>
- <span data-ttu-id="64f1e-940">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="64f1e-940">DriversLicences</span></span>
- <span data-ttu-id="64f1e-941">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="64f1e-941">DriversLicense</span></span>
- <span data-ttu-id="64f1e-942">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="64f1e-942">DriversLicenses</span></span>
- <span data-ttu-id="64f1e-943">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-943">Drivers Lic</span></span>
- <span data-ttu-id="64f1e-944">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-944">Drivers Lics</span></span>
- <span data-ttu-id="64f1e-945">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-945">Drivers License</span></span>
- <span data-ttu-id="64f1e-946">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-946">Drivers Licenses</span></span>
- <span data-ttu-id="64f1e-947">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-947">Drivers Licence</span></span>
- <span data-ttu-id="64f1e-948">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-948">Drivers Licences</span></span>
- <span data-ttu-id="64f1e-949">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="64f1e-949">Driver'Lic</span></span>
- <span data-ttu-id="64f1e-950">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="64f1e-950">Driver'Lics</span></span>
- <span data-ttu-id="64f1e-951">Driver'License</span><span class="sxs-lookup"><span data-stu-id="64f1e-951">Driver'License</span></span>
- <span data-ttu-id="64f1e-952">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="64f1e-952">Driver'Licenses</span></span>
- <span data-ttu-id="64f1e-953">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="64f1e-953">Driver'Licence</span></span>
- <span data-ttu-id="64f1e-954">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="64f1e-954">Driver'Licences</span></span>
- <span data-ttu-id="64f1e-955">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-955">Driver' Lic</span></span>
- <span data-ttu-id="64f1e-956">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-956">Driver' Lics</span></span>
- <span data-ttu-id="64f1e-957">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-957">Driver' License</span></span>
- <span data-ttu-id="64f1e-958">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-958">Driver' Licenses</span></span>
- <span data-ttu-id="64f1e-959">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-959">Driver' Licence</span></span>
- <span data-ttu-id="64f1e-960">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-960">Driver' Licences</span></span>
- <span data-ttu-id="64f1e-961">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="64f1e-961">Driver'sLic</span></span>
- <span data-ttu-id="64f1e-962">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="64f1e-962">Driver'sLics</span></span>
- <span data-ttu-id="64f1e-963">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="64f1e-963">Driver'sLicense</span></span>
- <span data-ttu-id="64f1e-964">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="64f1e-964">Driver'sLicenses</span></span>
- <span data-ttu-id="64f1e-965">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="64f1e-965">Driver'sLicence</span></span>
- <span data-ttu-id="64f1e-966">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="64f1e-966">Driver'sLicences</span></span>
- <span data-ttu-id="64f1e-967">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-967">Driver's Lic</span></span>
- <span data-ttu-id="64f1e-968">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-968">Driver's Lics</span></span>
- <span data-ttu-id="64f1e-969">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-969">Driver's License</span></span>
- <span data-ttu-id="64f1e-970">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-970">Driver's Licenses</span></span>
- <span data-ttu-id="64f1e-971">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-971">Driver's Licence</span></span>
- <span data-ttu-id="64f1e-972">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-972">Driver's Licences</span></span>
- <span data-ttu-id="64f1e-973">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-973">Permis de Conduire</span></span>
- <span data-ttu-id="64f1e-974">id</span><span class="sxs-lookup"><span data-stu-id="64f1e-974">id</span></span>
- <span data-ttu-id="64f1e-975">Ids</span><span class="sxs-lookup"><span data-stu-id="64f1e-975">ids</span></span>
- <span data-ttu-id="64f1e-976">numéro carte d’identification</span><span class="sxs-lookup"><span data-stu-id="64f1e-976">idcard number</span></span>
- <span data-ttu-id="64f1e-977">numéros carte d’identification</span><span class="sxs-lookup"><span data-stu-id="64f1e-977">idcard numbers</span></span>
- <span data-ttu-id="64f1e-978"># carte d’identification</span><span class="sxs-lookup"><span data-stu-id="64f1e-978">idcard #</span></span>
- <span data-ttu-id="64f1e-979"># carte d’identification</span><span class="sxs-lookup"><span data-stu-id="64f1e-979">idcard #s</span></span>
- <span data-ttu-id="64f1e-980">carte d’identification</span><span class="sxs-lookup"><span data-stu-id="64f1e-980">idcard card</span></span>
- <span data-ttu-id="64f1e-981">cartes d’identification</span><span class="sxs-lookup"><span data-stu-id="64f1e-981">idcard cards</span></span>
- <span data-ttu-id="64f1e-982">carte d'identification</span><span class="sxs-lookup"><span data-stu-id="64f1e-982">idcard</span></span>
- <span data-ttu-id="64f1e-983">numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="64f1e-983">identification number</span></span>
- <span data-ttu-id="64f1e-984">numéros d’identification</span><span class="sxs-lookup"><span data-stu-id="64f1e-984">identification numbers</span></span>
- <span data-ttu-id="64f1e-985"># identification</span><span class="sxs-lookup"><span data-stu-id="64f1e-985">identification #</span></span>
- <span data-ttu-id="64f1e-986"># identification</span><span class="sxs-lookup"><span data-stu-id="64f1e-986">identification #s</span></span>
- <span data-ttu-id="64f1e-987">carte d’identification</span><span class="sxs-lookup"><span data-stu-id="64f1e-987">identification card</span></span>
- <span data-ttu-id="64f1e-988">cartes d’identification</span><span class="sxs-lookup"><span data-stu-id="64f1e-988">identification cards</span></span>
- <span data-ttu-id="64f1e-989">identificateur</span><span class="sxs-lookup"><span data-stu-id="64f1e-989">identification</span></span> 
- <span data-ttu-id="64f1e-990">LD</span><span class="sxs-lookup"><span data-stu-id="64f1e-990">DL#</span></span>
- <span data-ttu-id="64f1e-991">DISTRIBUTION</span><span class="sxs-lookup"><span data-stu-id="64f1e-991">DLS#</span></span> 
- <span data-ttu-id="64f1e-992">CÈDE</span><span class="sxs-lookup"><span data-stu-id="64f1e-992">CDL#</span></span> 
- <span data-ttu-id="64f1e-993">CDLS #</span><span class="sxs-lookup"><span data-stu-id="64f1e-993">CDLS#</span></span> 
- <span data-ttu-id="64f1e-994">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="64f1e-994">DriverLic#</span></span> 
- <span data-ttu-id="64f1e-995">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="64f1e-995">DriverLics#</span></span> 
- <span data-ttu-id="64f1e-996">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="64f1e-996">DriverLicense#</span></span> 
- <span data-ttu-id="64f1e-997">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="64f1e-997">DriverLicenses#</span></span> 
- <span data-ttu-id="64f1e-998">DriverLicence #</span><span class="sxs-lookup"><span data-stu-id="64f1e-998">DriverLicence#</span></span> 
- <span data-ttu-id="64f1e-999">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="64f1e-999">DriverLicences#</span></span> 
- <span data-ttu-id="64f1e-1000">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-1000">Driver Lic#</span></span>
- <span data-ttu-id="64f1e-1001">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-1001">Driver Lics#</span></span> 
- <span data-ttu-id="64f1e-1002">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-1002">Driver License#</span></span> 
- <span data-ttu-id="64f1e-1003">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-1003">Driver Licenses#</span></span> 
- <span data-ttu-id="64f1e-1004">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-1004">Driver License#</span></span> 
- <span data-ttu-id="64f1e-1005">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-1005">Driver Licences#</span></span> 
- <span data-ttu-id="64f1e-1006">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="64f1e-1006">DriversLic#</span></span> 
- <span data-ttu-id="64f1e-1007">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="64f1e-1007">DriversLics#</span></span> 
- <span data-ttu-id="64f1e-1008">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="64f1e-1008">DriversLicense#</span></span> 
- <span data-ttu-id="64f1e-1009">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="64f1e-1009">DriversLicenses#</span></span> 
- <span data-ttu-id="64f1e-1010">DriversLicence #</span><span class="sxs-lookup"><span data-stu-id="64f1e-1010">DriversLicence#</span></span> 
- <span data-ttu-id="64f1e-1011">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="64f1e-1011">DriversLicences#</span></span> 
- <span data-ttu-id="64f1e-1012">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-1012">Drivers Lic#</span></span> 
- <span data-ttu-id="64f1e-1013">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-1013">Drivers Lics#</span></span> 
- <span data-ttu-id="64f1e-1014">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-1014">Drivers License#</span></span> 
- <span data-ttu-id="64f1e-1015">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-1015">Drivers Licenses#</span></span> 
- <span data-ttu-id="64f1e-1016">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-1016">Drivers Licence#</span></span> 
- <span data-ttu-id="64f1e-1017">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-1017">Drivers Licences#</span></span> 
- <span data-ttu-id="64f1e-1018">Driver'Lic #</span><span class="sxs-lookup"><span data-stu-id="64f1e-1018">Driver'Lic#</span></span> 
- <span data-ttu-id="64f1e-1019">Driver'Lics #</span><span class="sxs-lookup"><span data-stu-id="64f1e-1019">Driver'Lics#</span></span> 
- <span data-ttu-id="64f1e-1020">Driver'License #</span><span class="sxs-lookup"><span data-stu-id="64f1e-1020">Driver'License#</span></span> 
- <span data-ttu-id="64f1e-1021">Driver'Licenses #</span><span class="sxs-lookup"><span data-stu-id="64f1e-1021">Driver'Licenses#</span></span> 
- <span data-ttu-id="64f1e-1022">Driver'Licence #</span><span class="sxs-lookup"><span data-stu-id="64f1e-1022">Driver'Licence#</span></span> 
- <span data-ttu-id="64f1e-1023">Driver'Licences #</span><span class="sxs-lookup"><span data-stu-id="64f1e-1023">Driver'Licences#</span></span> 
- <span data-ttu-id="64f1e-1024">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-1024">Driver' Lic#</span></span> 
- <span data-ttu-id="64f1e-1025">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-1025">Driver' Lics#</span></span> 
- <span data-ttu-id="64f1e-1026">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-1026">Driver' License#</span></span> 
- <span data-ttu-id="64f1e-1027">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-1027">Driver' Licenses#</span></span> 
- <span data-ttu-id="64f1e-1028">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-1028">Driver' Licence#</span></span> 
- <span data-ttu-id="64f1e-1029">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-1029">Driver' Licences#</span></span> 
- <span data-ttu-id="64f1e-1030">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="64f1e-1030">Driver'sLic#</span></span> 
- <span data-ttu-id="64f1e-1031">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="64f1e-1031">Driver'sLics#</span></span> 
- <span data-ttu-id="64f1e-1032">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="64f1e-1032">Driver'sLicense#</span></span> 
- <span data-ttu-id="64f1e-1033">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="64f1e-1033">Driver'sLicenses#</span></span> 
- <span data-ttu-id="64f1e-1034">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="64f1e-1034">Driver'sLicence#</span></span> 
- <span data-ttu-id="64f1e-1035">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="64f1e-1035">Driver'sLicences#</span></span> 
- <span data-ttu-id="64f1e-1036">#Permisconduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-1036">Driver's Lic#</span></span> 
- <span data-ttu-id="64f1e-1037">#Permisconduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-1037">Driver's Lics#</span></span> 
- <span data-ttu-id="64f1e-1038">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-1038">Driver's License#</span></span> 
- <span data-ttu-id="64f1e-1039">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-1039">Driver's Licenses#</span></span> 
- <span data-ttu-id="64f1e-1040">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-1040">Driver's Licence#</span></span> 
- <span data-ttu-id="64f1e-1041">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-1041">Driver's Licences#</span></span> 
- <span data-ttu-id="64f1e-1042">Permis de conduire #</span><span class="sxs-lookup"><span data-stu-id="64f1e-1042">Permis de Conduire#</span></span> 
- <span data-ttu-id="64f1e-1043">Réf</span><span class="sxs-lookup"><span data-stu-id="64f1e-1043">id#</span></span> 
- <span data-ttu-id="64f1e-1044">codes</span><span class="sxs-lookup"><span data-stu-id="64f1e-1044">ids#</span></span> 
- <span data-ttu-id="64f1e-1045">#carte carte d’identification</span><span class="sxs-lookup"><span data-stu-id="64f1e-1045">idcard card#</span></span> 
- <span data-ttu-id="64f1e-1046">#cartes carte d’identification</span><span class="sxs-lookup"><span data-stu-id="64f1e-1046">idcard cards#</span></span> 
- <span data-ttu-id="64f1e-1047">carte d'identification</span><span class="sxs-lookup"><span data-stu-id="64f1e-1047">idcard#</span></span> 
- <span data-ttu-id="64f1e-1048">#carte d’identification</span><span class="sxs-lookup"><span data-stu-id="64f1e-1048">identification card#</span></span> 
- <span data-ttu-id="64f1e-1049">#cartes d’identification</span><span class="sxs-lookup"><span data-stu-id="64f1e-1049">identification cards#</span></span> 
- <span data-ttu-id="64f1e-1050">identificateur</span><span class="sxs-lookup"><span data-stu-id="64f1e-1050">identification#</span></span> 
   
## <a name="canada-health-service-number"></a><span data-ttu-id="64f1e-1051">Numéro de service de santé Canada</span><span class="sxs-lookup"><span data-stu-id="64f1e-1051">Canada Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-1052">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-1052">Format</span></span>

<span data-ttu-id="64f1e-1053">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-1053">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-1054">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-1054">Pattern</span></span>

<span data-ttu-id="64f1e-1055">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-1055">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-1056">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-1056">Checksum</span></span>

<span data-ttu-id="64f1e-1057">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-1057">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-1058">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-1058">Definition</span></span>

<span data-ttu-id="64f1e-1059">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-1059">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-1060">L’expression régulière Regex_canada_health_service_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1060">The regular expression Regex_canada_health_service_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-1061">Un mot clé figurant dans la liste Keyword_canada_health_service_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1061">A keyword from Keyword_canada_health_service_number is found.</span></span>

```
<!-- Canada Health Service Number -->
<Entity id="59c0bf39-7fab-482c-af25-00faa4384c94" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_canada_health_service_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_canada_health_service_number" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-1062">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-1062">Keywords</span></span>

#### <a name="keywordcanadahealthservicenumber"></a><span data-ttu-id="64f1e-1063">Keyword_canada_health_service_number</span><span class="sxs-lookup"><span data-stu-id="64f1e-1063">Keyword_canada_health_service_number</span></span>

- <span data-ttu-id="64f1e-1064">numéro d’assurance-maladie</span><span class="sxs-lookup"><span data-stu-id="64f1e-1064">personal health number</span></span>
- <span data-ttu-id="64f1e-1065">informations sur le patient</span><span class="sxs-lookup"><span data-stu-id="64f1e-1065">patient information</span></span>
- <span data-ttu-id="64f1e-1066">services de santé</span><span class="sxs-lookup"><span data-stu-id="64f1e-1066">health services</span></span>
- <span data-ttu-id="64f1e-1067">services spécialisés</span><span class="sxs-lookup"><span data-stu-id="64f1e-1067">speciality services</span></span>
- <span data-ttu-id="64f1e-1068">accident automobile</span><span class="sxs-lookup"><span data-stu-id="64f1e-1068">automobile accident</span></span>
- <span data-ttu-id="64f1e-1069">hôpital pour malades</span><span class="sxs-lookup"><span data-stu-id="64f1e-1069">patient hospital</span></span>
- <span data-ttu-id="64f1e-1070">Psychiatrist</span><span class="sxs-lookup"><span data-stu-id="64f1e-1070">psychiatrist</span></span>
- <span data-ttu-id="64f1e-1071">indemnisation des salariés</span><span class="sxs-lookup"><span data-stu-id="64f1e-1071">workers compensation</span></span>
- <span data-ttu-id="64f1e-1072">incapacité</span><span class="sxs-lookup"><span data-stu-id="64f1e-1072">disability</span></span>
      
## <a name="canada-passport-number"></a><span data-ttu-id="64f1e-1073">Numéro de passeport Canada</span><span class="sxs-lookup"><span data-stu-id="64f1e-1073">Canada Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-1074">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-1074">Format</span></span>

<span data-ttu-id="64f1e-1075">Deux lettres majuscules suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-1075">Two uppercase letters followed by six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-1076">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-1076">Pattern</span></span>

<span data-ttu-id="64f1e-1077">Deux lettres majuscules suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-1077">Two uppercase letters followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-1078">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-1078">Checksum</span></span>

<span data-ttu-id="64f1e-1079">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-1079">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-1080">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-1080">Definition</span></span>

<span data-ttu-id="64f1e-1081">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-1081">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-1082">L’expression régulière Regex_canada_passport_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1082">The regular expression Regex_canada_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-1083">Un mot clé depuis Keyword_canada_passport_number ou Keyword_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1083">A keyword from Keyword_canada_passport_number or Keyword_passport is found.</span></span>

``` 
<!-- Canada Passport Number -->
<Entity id="14d0db8b-498a-43ed-9fca-f6097ae687eb" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_canada_passport_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_canada_passport_number" />
          <Match idRef="Keyword_passport" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-1084">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-1084">Keywords</span></span>

#### <a name="keywordcanadapassportnumber"></a><span data-ttu-id="64f1e-1085">Keyword_canada_passport_number</span><span class="sxs-lookup"><span data-stu-id="64f1e-1085">Keyword_canada_passport_number</span></span>

- <span data-ttu-id="64f1e-1086">citoyenneté canadienne</span><span class="sxs-lookup"><span data-stu-id="64f1e-1086">canadian citizenship</span></span>
- <span data-ttu-id="64f1e-1087">passeport canadien</span><span class="sxs-lookup"><span data-stu-id="64f1e-1087">canadian passport</span></span>
- <span data-ttu-id="64f1e-1088">demande de passeport</span><span class="sxs-lookup"><span data-stu-id="64f1e-1088">passport application</span></span>
- <span data-ttu-id="64f1e-1089">photos pour passeport</span><span class="sxs-lookup"><span data-stu-id="64f1e-1089">passport photos</span></span>
- <span data-ttu-id="64f1e-1090">traducteur agréé</span><span class="sxs-lookup"><span data-stu-id="64f1e-1090">certified translator</span></span>
- <span data-ttu-id="64f1e-1091">citoyens canadiens</span><span class="sxs-lookup"><span data-stu-id="64f1e-1091">canadian citizens</span></span>
- <span data-ttu-id="64f1e-1092">temps de traitement</span><span class="sxs-lookup"><span data-stu-id="64f1e-1092">processing times</span></span>
- <span data-ttu-id="64f1e-1093">demande de renouvellement</span><span class="sxs-lookup"><span data-stu-id="64f1e-1093">renewal application</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="64f1e-1094">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="64f1e-1094">Keyword_passport</span></span>

- <span data-ttu-id="64f1e-1095">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="64f1e-1095">Passport Number</span></span>
- <span data-ttu-id="64f1e-1096">N° de passeport</span><span class="sxs-lookup"><span data-stu-id="64f1e-1096">Passport No</span></span>
- <span data-ttu-id="64f1e-1097"># Passeport</span><span class="sxs-lookup"><span data-stu-id="64f1e-1097">Passport #</span></span>
- <span data-ttu-id="64f1e-1098">Tel</span><span class="sxs-lookup"><span data-stu-id="64f1e-1098">Passport#</span></span>
- <span data-ttu-id="64f1e-1099">PassportID</span><span class="sxs-lookup"><span data-stu-id="64f1e-1099">PassportID</span></span>
- <span data-ttu-id="64f1e-1100">N ° passeport</span><span class="sxs-lookup"><span data-stu-id="64f1e-1100">Passportno</span></span>
- <span data-ttu-id="64f1e-1101">passportnumber</span><span class="sxs-lookup"><span data-stu-id="64f1e-1101">passportnumber</span></span>
- <span data-ttu-id="64f1e-1102">パスポート</span><span class="sxs-lookup"><span data-stu-id="64f1e-1102">パスポート</span></span>
- <span data-ttu-id="64f1e-1103">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="64f1e-1103">パスポート番号</span></span>
- <span data-ttu-id="64f1e-1104">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="64f1e-1104">パスポートのNum</span></span>
- <span data-ttu-id="64f1e-1105">パスポート #</span><span class="sxs-lookup"><span data-stu-id="64f1e-1105">パスポート＃</span></span>
- <span data-ttu-id="64f1e-1106">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="64f1e-1106">Numéro de passeport</span></span>
- <span data-ttu-id="64f1e-1107">Passeport n°</span><span class="sxs-lookup"><span data-stu-id="64f1e-1107">Passeport n °</span></span>
- <span data-ttu-id="64f1e-1108">Passeport numéro</span><span class="sxs-lookup"><span data-stu-id="64f1e-1108">Passeport Non</span></span>
- <span data-ttu-id="64f1e-1109"># Passeport</span><span class="sxs-lookup"><span data-stu-id="64f1e-1109">Passeport #</span></span>
- <span data-ttu-id="64f1e-1110">Passeport</span><span class="sxs-lookup"><span data-stu-id="64f1e-1110">Passeport#</span></span>
- <span data-ttu-id="64f1e-1111">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="64f1e-1111">PasseportNon</span></span>
- <span data-ttu-id="64f1e-1112">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="64f1e-1112">Passeportn °</span></span>
   
## <a name="canada-personal-health-identification-number-phin"></a><span data-ttu-id="64f1e-1113">NIMP (numéro d’identification médicale personnel) Canada</span><span class="sxs-lookup"><span data-stu-id="64f1e-1113">Canada Personal Health Identification Number (PHIN)</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-1114">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-1114">Format</span></span>

<span data-ttu-id="64f1e-1115">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-1115">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-1116">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-1116">Pattern</span></span>

<span data-ttu-id="64f1e-1117">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-1117">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-1118">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-1118">Checksum</span></span>

<span data-ttu-id="64f1e-1119">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-1119">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-1120">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-1120">Definition</span></span>

<span data-ttu-id="64f1e-1121">Une stratégie DLP est sûre à 75% d'avoir détecté ce type d'informations sensibles si, dans une proximité de 300 caractères: l'expression régulière Regex_canada_phin trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1121">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_canada_phin finds content that matches the pattern.</span></span>
<span data-ttu-id="64f1e-1122">Au moins deux mots clés de Keyword_canada_phin ou Keyword_canada_provinces sont trouvés..</span><span class="sxs-lookup"><span data-stu-id="64f1e-1122">At least two keywords from Keyword_canada_phin or Keyword_canada_provinces are found..</span></span>

```
<!-- Canada PHIN -->
<Entity id="722e12ac-c89a-4ec8-a1b7-fea3469f89db" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_canada_phin" />
        <Any minMatches="2">
          <Match idRef="Keyword_canada_phin" />
          <Match idRef="Keyword_canada_provinces" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-1123">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-1123">Keywords</span></span>

#### <a name="keywordcanadaphin"></a><span data-ttu-id="64f1e-1124">Keyword_canada_phin</span><span class="sxs-lookup"><span data-stu-id="64f1e-1124">Keyword_canada_phin</span></span>

- <span data-ttu-id="64f1e-1125">numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="64f1e-1125">social insurance number</span></span>
- <span data-ttu-id="64f1e-1126">loi sur les renseignements médicaux</span><span class="sxs-lookup"><span data-stu-id="64f1e-1126">health information act</span></span>
- <span data-ttu-id="64f1e-1127">renseignements relatifs à l’impôt sur le revenu</span><span class="sxs-lookup"><span data-stu-id="64f1e-1127">income tax information</span></span>
- <span data-ttu-id="64f1e-1128">santé Manitoba</span><span class="sxs-lookup"><span data-stu-id="64f1e-1128">manitoba health</span></span>
- <span data-ttu-id="64f1e-1129">enregistrement aux services de santé</span><span class="sxs-lookup"><span data-stu-id="64f1e-1129">health registration</span></span>
- <span data-ttu-id="64f1e-1130">achats de médicaments sur ordonnance</span><span class="sxs-lookup"><span data-stu-id="64f1e-1130">prescription purchases</span></span>
- <span data-ttu-id="64f1e-1131">admissibilité aux prestations</span><span class="sxs-lookup"><span data-stu-id="64f1e-1131">benefit eligibility</span></span>
- <span data-ttu-id="64f1e-1132">santé personnelle</span><span class="sxs-lookup"><span data-stu-id="64f1e-1132">personal health</span></span>
- <span data-ttu-id="64f1e-1133">procuration</span><span class="sxs-lookup"><span data-stu-id="64f1e-1133">power of attorney</span></span>
- <span data-ttu-id="64f1e-1134">numéro d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="64f1e-1134">registration number</span></span>
- <span data-ttu-id="64f1e-1135">numéro d’assurance-maladie</span><span class="sxs-lookup"><span data-stu-id="64f1e-1135">personal health number</span></span>
- <span data-ttu-id="64f1e-1136">recommandation par le médecin</span><span class="sxs-lookup"><span data-stu-id="64f1e-1136">practitioner referral</span></span>
- <span data-ttu-id="64f1e-1137">professionnel de bien-être</span><span class="sxs-lookup"><span data-stu-id="64f1e-1137">wellness professional</span></span>
- <span data-ttu-id="64f1e-1138">orientation d’un patient</span><span class="sxs-lookup"><span data-stu-id="64f1e-1138">patient referral</span></span>
- <span data-ttu-id="64f1e-1139">santé et bien-être</span><span class="sxs-lookup"><span data-stu-id="64f1e-1139">health and wellness</span></span>

#### <a name="keywordcanadaprovinces"></a><span data-ttu-id="64f1e-1140">Keyword_canada_provinces</span><span class="sxs-lookup"><span data-stu-id="64f1e-1140">Keyword_canada_provinces</span></span>

- <span data-ttu-id="64f1e-1141">Nunavut</span><span class="sxs-lookup"><span data-stu-id="64f1e-1141">Nunavut</span></span>
- <span data-ttu-id="64f1e-1142">Régime</span><span class="sxs-lookup"><span data-stu-id="64f1e-1142">Quebec</span></span>
- <span data-ttu-id="64f1e-1143">Territoires du Nord-Ouest</span><span class="sxs-lookup"><span data-stu-id="64f1e-1143">Northwest Territories</span></span>
- <span data-ttu-id="64f1e-1144">Brand</span><span class="sxs-lookup"><span data-stu-id="64f1e-1144">Ontario</span></span>
- <span data-ttu-id="64f1e-1145">Colombie-britannique</span><span class="sxs-lookup"><span data-stu-id="64f1e-1145">British Columbia</span></span>
- <span data-ttu-id="64f1e-1146">Alberta</span><span class="sxs-lookup"><span data-stu-id="64f1e-1146">Alberta</span></span>
- <span data-ttu-id="64f1e-1147">En-dessus</span><span class="sxs-lookup"><span data-stu-id="64f1e-1147">Saskatchewan</span></span>
- <span data-ttu-id="64f1e-1148">Manitoba</span><span class="sxs-lookup"><span data-stu-id="64f1e-1148">Manitoba</span></span>
- <span data-ttu-id="64f1e-1149">Yukon</span><span class="sxs-lookup"><span data-stu-id="64f1e-1149">Yukon</span></span>
- <span data-ttu-id="64f1e-1150">Terre-Neuve-et-Labrador</span><span class="sxs-lookup"><span data-stu-id="64f1e-1150">Newfoundland and Labrador</span></span>
- <span data-ttu-id="64f1e-1151">Nouveau-Brunswick</span><span class="sxs-lookup"><span data-stu-id="64f1e-1151">New Brunswick</span></span>
- <span data-ttu-id="64f1e-1152">Nouvelle-Écosse</span><span class="sxs-lookup"><span data-stu-id="64f1e-1152">Nova Scotia</span></span>
- <span data-ttu-id="64f1e-1153">Île-du-Prince-Édouard</span><span class="sxs-lookup"><span data-stu-id="64f1e-1153">Prince Edward Island</span></span>
- <span data-ttu-id="64f1e-1154">Canada</span><span class="sxs-lookup"><span data-stu-id="64f1e-1154">Canada</span></span>
   
## <a name="canada-social-insurance-number"></a><span data-ttu-id="64f1e-1155">Numéro d'assurance sociale Canada</span><span class="sxs-lookup"><span data-stu-id="64f1e-1155">Canada Social Insurance Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-1156">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-1156">Format</span></span>

<span data-ttu-id="64f1e-1157">Neuf chiffres avec éventuellement des traits d’union ou des espaces</span><span class="sxs-lookup"><span data-stu-id="64f1e-1157">Nine digits with optional hyphens or spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-1158">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-1158">Pattern</span></span>

<span data-ttu-id="64f1e-1159">Avec</span><span class="sxs-lookup"><span data-stu-id="64f1e-1159">Formatted:</span></span>
- <span data-ttu-id="64f1e-1160">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-1160">Three digits</span></span> 
- <span data-ttu-id="64f1e-1161">Un trait d’union ou un espace</span><span class="sxs-lookup"><span data-stu-id="64f1e-1161">A hyphen or space</span></span> 
- <span data-ttu-id="64f1e-1162">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-1162">Three digits</span></span> 
- <span data-ttu-id="64f1e-1163">Un trait d’union ou un espace</span><span class="sxs-lookup"><span data-stu-id="64f1e-1163">A hyphen or space</span></span> 
- <span data-ttu-id="64f1e-1164">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-1164">Three digits</span></span>

<span data-ttu-id="64f1e-1165">Non mis en forme: neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-1165">Unformatted: Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-1166">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-1166">Checksum</span></span>

<span data-ttu-id="64f1e-1167">Oui</span><span class="sxs-lookup"><span data-stu-id="64f1e-1167">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-1168">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-1168">Definition</span></span>

<span data-ttu-id="64f1e-1169">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-1169">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-1170">La fonction Func_canadian_sin trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1170">The function Func_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-1171">Au moins deux des éléments suivants, quelle que soit la combinaison :</span><span class="sxs-lookup"><span data-stu-id="64f1e-1171">At least two of any combination of the following:</span></span>
    - <span data-ttu-id="64f1e-1172">Un mot clé figurant dans la liste Keyword_sin est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1172">A keyword from Keyword_sin is found.</span></span>
    - <span data-ttu-id="64f1e-1173">Un mot clé figurant dans la liste Keyword_sin_collaborative est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1173">A keyword from Keyword_sin_collaborative is found.</span></span>
    - <span data-ttu-id="64f1e-1174">La fonction Func_eu_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1174">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="64f1e-1175">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1175">The checksum passes.</span></span>

<span data-ttu-id="64f1e-1176">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-1176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-1177">La fonction Func_unformatted_canadian_sin trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1177">The function Func_unformatted_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-1178">Un mot clé figurant dans la liste Keyword_sin est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1178">A keyword from Keyword_sin is found.</span></span>
- <span data-ttu-id="64f1e-1179">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1179">The checksum passes.</span></span>

```
<!-- Canada Social Insurance Number -->
<Entity id="a2f29c85-ecb8-4514-a610-364790c0773e" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_canadian_sin" />
        <Any minMatches="2">
          <Match idRef="Keyword_sin" />
          <Match idRef="Keyword_sin_collaborative" />
          <Match idRef="Func_eu_date" />
        </Any>
  </Pattern>
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_unformatted_canadian_sin" />
        <Match idRef="Keyword_sin" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-1180">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-1180">Keywords</span></span>

#### <a name="keywordsin"></a><span data-ttu-id="64f1e-1181">Keyword_sin</span><span class="sxs-lookup"><span data-stu-id="64f1e-1181">Keyword_sin</span></span>

- <span data-ttu-id="64f1e-1182">assoc</span><span class="sxs-lookup"><span data-stu-id="64f1e-1182">sin</span></span> 
- <span data-ttu-id="64f1e-1183">assurance sociale</span><span class="sxs-lookup"><span data-stu-id="64f1e-1183">social insurance</span></span> 
- <span data-ttu-id="64f1e-1184">numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="64f1e-1184">numero d'assurance sociale</span></span> 
- <span data-ttu-id="64f1e-1185">péchés</span><span class="sxs-lookup"><span data-stu-id="64f1e-1185">sins</span></span> 
- <span data-ttu-id="64f1e-1186">SSN</span><span class="sxs-lookup"><span data-stu-id="64f1e-1186">ssn</span></span> 
- <span data-ttu-id="64f1e-1187">numéros</span><span class="sxs-lookup"><span data-stu-id="64f1e-1187">ssns</span></span> 
- <span data-ttu-id="64f1e-1188">sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="64f1e-1188">social security</span></span> 
- <span data-ttu-id="64f1e-1189">numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="64f1e-1189">numero d'assurance social</span></span> 
- <span data-ttu-id="64f1e-1190">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="64f1e-1190">national identification number</span></span> 
- <span data-ttu-id="64f1e-1191">id national</span><span class="sxs-lookup"><span data-stu-id="64f1e-1191">national id</span></span> 
- <span data-ttu-id="64f1e-1192">sine</span><span class="sxs-lookup"><span data-stu-id="64f1e-1192">sin#</span></span> 
- <span data-ttu-id="64f1e-1193">ass soc</span><span class="sxs-lookup"><span data-stu-id="64f1e-1193">soc ins</span></span> 
- <span data-ttu-id="64f1e-1194">ass sociale</span><span class="sxs-lookup"><span data-stu-id="64f1e-1194">social ins</span></span> 

#### <a name="keywordsincollaborative"></a><span data-ttu-id="64f1e-1195">Keyword_sin_collaborative</span><span class="sxs-lookup"><span data-stu-id="64f1e-1195">Keyword_sin_collaborative</span></span>

- <span data-ttu-id="64f1e-1196">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-1196">driver's license</span></span> 
- <span data-ttu-id="64f1e-1197">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-1197">drivers license</span></span> 
- <span data-ttu-id="64f1e-1198">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-1198">driver's licence</span></span> 
- <span data-ttu-id="64f1e-1199">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-1199">drivers licence</span></span> 
- <span data-ttu-id="64f1e-1200">DOB</span><span class="sxs-lookup"><span data-stu-id="64f1e-1200">DOB</span></span> 
- <span data-ttu-id="64f1e-1201">Birthdate</span><span class="sxs-lookup"><span data-stu-id="64f1e-1201">Birthdate</span></span> 
- <span data-ttu-id="64f1e-1202">Anniversaire</span><span class="sxs-lookup"><span data-stu-id="64f1e-1202">Birthday</span></span> 
- <span data-ttu-id="64f1e-1203">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="64f1e-1203">Date of Birth</span></span> 
   
## <a name="chile-identity-card-number"></a><span data-ttu-id="64f1e-1204">	Numéro de carte d’identité Chili</span><span class="sxs-lookup"><span data-stu-id="64f1e-1204">Chile Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-1205">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-1205">Format</span></span>

<span data-ttu-id="64f1e-1206">7-8 chiffres plus des délimiteurs un chiffre ou une lettre</span><span class="sxs-lookup"><span data-stu-id="64f1e-1206">7-8 digits plus delimiters a check digit or letter</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-1207">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-1207">Pattern</span></span>

<span data-ttu-id="64f1e-1208">7 ou 8 chiffres, plus des délimiteurs :</span><span class="sxs-lookup"><span data-stu-id="64f1e-1208">7-8 digits plus delimiters:</span></span>
- <span data-ttu-id="64f1e-1209">1 ou 2 chiffres </span><span class="sxs-lookup"><span data-stu-id="64f1e-1209">1-2 digits</span></span> 
- <span data-ttu-id="64f1e-1210">Un point </span><span class="sxs-lookup"><span data-stu-id="64f1e-1210">A period</span></span> 
- <span data-ttu-id="64f1e-1211">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-1211">Three digits</span></span> 
- <span data-ttu-id="64f1e-1212">Un point </span><span class="sxs-lookup"><span data-stu-id="64f1e-1212">A period</span></span> 
- <span data-ttu-id="64f1e-1213">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-1213">Three digits</span></span> 
- <span data-ttu-id="64f1e-1214">Un tiret</span><span class="sxs-lookup"><span data-stu-id="64f1e-1214">A dash</span></span> 
- <span data-ttu-id="64f1e-1215">Un chiffre ou une lettre (ne respectant pas la casse) de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-1215">One digit or letter (not case sensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-1216">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-1216">Checksum</span></span>

<span data-ttu-id="64f1e-1217">Oui</span><span class="sxs-lookup"><span data-stu-id="64f1e-1217">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-1218">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-1218">Definition</span></span>

<span data-ttu-id="64f1e-1219">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-1219">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-1220">La fonction Func_chile_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1220">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-1221">Un mot clé figurant dans la liste Keyword_chile_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1221">A keyword from Keyword_chile_id_card is found.</span></span>
- <span data-ttu-id="64f1e-1222">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1222">The checksum passes.</span></span>

<span data-ttu-id="64f1e-1223">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-1223">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-1224">La fonction Func_chile_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1224">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-1225">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1225">The checksum passes.</span></span>

```
<!-- Chile Identity Card Number -->
<Entity id="4e979794-49a0-407e-a0b9-2c536937b925" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_chile_id_card"/>
     <Match idRef="Keyword_chile_id_card"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_chile_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-1226">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-1226">Keywords</span></span>

#### <a name="keywordchileidcard"></a><span data-ttu-id="64f1e-1227">Keyword_chile_id_card</span><span class="sxs-lookup"><span data-stu-id="64f1e-1227">Keyword_chile_id_card</span></span>

- <span data-ttu-id="64f1e-1228">National Identification Number</span><span class="sxs-lookup"><span data-stu-id="64f1e-1228">National Identification Number</span></span> 
- <span data-ttu-id="64f1e-1229">Identity card</span><span class="sxs-lookup"><span data-stu-id="64f1e-1229">Identity card</span></span> 
- <span data-ttu-id="64f1e-1230">ID</span><span class="sxs-lookup"><span data-stu-id="64f1e-1230">ID</span></span> 
- <span data-ttu-id="64f1e-1231">Identificateur</span><span class="sxs-lookup"><span data-stu-id="64f1e-1231">Identification</span></span> 
- <span data-ttu-id="64f1e-1232">Rol Único Nacional</span><span class="sxs-lookup"><span data-stu-id="64f1e-1232">Rol Único Nacional</span></span> 
- <span data-ttu-id="64f1e-1233">GÉNÉRER</span><span class="sxs-lookup"><span data-stu-id="64f1e-1233">RUN</span></span> 
- <span data-ttu-id="64f1e-1234">Rol Único Tributario</span><span class="sxs-lookup"><span data-stu-id="64f1e-1234">Rol Único Tributario</span></span> 
- <span data-ttu-id="64f1e-1235">ROUTINE</span><span class="sxs-lookup"><span data-stu-id="64f1e-1235">RUT</span></span> 
- <span data-ttu-id="64f1e-1236">Cédula de Identidad</span><span class="sxs-lookup"><span data-stu-id="64f1e-1236">Cédula de Identidad</span></span> 
- <span data-ttu-id="64f1e-1237">Número De Identificación Nacional</span><span class="sxs-lookup"><span data-stu-id="64f1e-1237">Número De Identificación Nacional</span></span> 
- <span data-ttu-id="64f1e-1238">Tarjeta de identificación</span><span class="sxs-lookup"><span data-stu-id="64f1e-1238">Tarjeta de identificación</span></span> 
- <span data-ttu-id="64f1e-1239">Identificación</span><span class="sxs-lookup"><span data-stu-id="64f1e-1239">Identificación</span></span> 
   
## <a name="china-resident-identity-card-prc-number"></a><span data-ttu-id="64f1e-1240">	Numéro de carte d’identité de résident Chine (RPC)</span><span class="sxs-lookup"><span data-stu-id="64f1e-1240">China Resident Identity Card (PRC) Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-1241">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-1241">Format</span></span>

<span data-ttu-id="64f1e-1242">18 chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-1242">18 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-1243">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-1243">Pattern</span></span>

<span data-ttu-id="64f1e-1244">18 chiffres :</span><span class="sxs-lookup"><span data-stu-id="64f1e-1244">18 digits:</span></span>
- <span data-ttu-id="64f1e-1245">Six chiffres qui composent un code d’adresse </span><span class="sxs-lookup"><span data-stu-id="64f1e-1245">Six digits which are an address code</span></span> 
- <span data-ttu-id="64f1e-1246">Huit chiffres sous la forme AAAAMMJJ qui correspondent à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="64f1e-1246">Eight digits in the form YYYYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="64f1e-1247">Trois chiffres qui correspondent à un code d’opération </span><span class="sxs-lookup"><span data-stu-id="64f1e-1247">Three digits which are an order code</span></span> 
- <span data-ttu-id="64f1e-1248">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-1248">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-1249">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-1249">Checksum</span></span>

<span data-ttu-id="64f1e-1250">Oui</span><span class="sxs-lookup"><span data-stu-id="64f1e-1250">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-1251">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-1251">Definition</span></span>

<span data-ttu-id="64f1e-1252">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-1252">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-1253">La fonction Func_china_resident_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1253">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-1254">Un mot clé figurant dans la liste Keyword_china_resident_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1254">A keyword from Keyword_china_resident_id is found.</span></span>
- <span data-ttu-id="64f1e-1255">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1255">The checksum passes.</span></span>

<span data-ttu-id="64f1e-1256">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-1256">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-1257">La fonction Func_china_resident_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1257">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-1258">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1258">The checksum passes.</span></span>

```
<!-- China Resident Identity Card (PRC) Number -->
<Entity id="c92daa86-2d16-4871-901f-816b3f554fc1" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_china_resident_id"/>
     <Match idRef="Keyword_china_resident_id"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_china_resident_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-1259">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-1259">Keywords</span></span>

### <a name="keywordchinaresidentid"></a><span data-ttu-id="64f1e-1260">Keyword_china_resident_id</span><span class="sxs-lookup"><span data-stu-id="64f1e-1260">Keyword_china_resident_id</span></span>

- <span data-ttu-id="64f1e-1261">Resident Identity Card</span><span class="sxs-lookup"><span data-stu-id="64f1e-1261">Resident Identity Card</span></span> 
- <span data-ttu-id="64f1e-1262">FIGURANT</span><span class="sxs-lookup"><span data-stu-id="64f1e-1262">PRC</span></span> 
- <span data-ttu-id="64f1e-1263">National Identification Card</span><span class="sxs-lookup"><span data-stu-id="64f1e-1263">National Identification Card</span></span> 
- <span data-ttu-id="64f1e-1264">身份证</span><span class="sxs-lookup"><span data-stu-id="64f1e-1264">身份证</span></span> 
- <span data-ttu-id="64f1e-1265">居民 身份证</span><span class="sxs-lookup"><span data-stu-id="64f1e-1265">居民 身份证</span></span> 
- <span data-ttu-id="64f1e-1266">居民身份证</span><span class="sxs-lookup"><span data-stu-id="64f1e-1266">居民身份证</span></span> 
- <span data-ttu-id="64f1e-1267">鉴定</span><span class="sxs-lookup"><span data-stu-id="64f1e-1267">鉴定</span></span> 
- <span data-ttu-id="64f1e-1268">身分證</span><span class="sxs-lookup"><span data-stu-id="64f1e-1268">身分證</span></span> 
- <span data-ttu-id="64f1e-1269">居民 身份證</span><span class="sxs-lookup"><span data-stu-id="64f1e-1269">居民 身份證</span></span>
- <span data-ttu-id="64f1e-1270">鑑定</span><span class="sxs-lookup"><span data-stu-id="64f1e-1270">鑑定</span></span> 
   
## <a name="credit-card-number"></a><span data-ttu-id="64f1e-1271">Numéro de carte de crédit</span><span class="sxs-lookup"><span data-stu-id="64f1e-1271">Credit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-1272">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-1272">Format</span></span>

<span data-ttu-id="64f1e-1273">16 chiffres qui peuvent être mis en forme ou non (dddddddddddddddd) et doivent réussir le test Luhn.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1273">16 digits which can be formatted or unformatted (dddddddddddddddd) and must pass the Luhn test.</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-1274">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-1274">Pattern</span></span>

<span data-ttu-id="64f1e-1275">Modèle très complexe et puissant qui détecte les cartes de visite de toutes les principales marques du monde, notamment Visa, MasterCard, Discover Card, JCB, American Express, etc.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1275">Very complex and robust pattern that detects cards from all major brands worldwide, including Visa, MasterCard, Discover Card, JCB, American Express, gift cards, and diner cards.</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-1276">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-1276">Checksum</span></span>

<span data-ttu-id="64f1e-1277">Oui, la somme de contrôle de Luhn</span><span class="sxs-lookup"><span data-stu-id="64f1e-1277">Yes, the Luhn checksum</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-1278">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-1278">Definition</span></span>

<span data-ttu-id="64f1e-1279">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-1279">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-1280">La fonction Func_credit_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1280">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-1281">L’une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="64f1e-1281">One of the following is true:</span></span>
    - <span data-ttu-id="64f1e-1282">Un mot clé figurant dans la liste Keyword_cc_verification est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1282">A keyword from Keyword_cc_verification is found.</span></span>
    - <span data-ttu-id="64f1e-1283">Un mot clé figurant dans la liste Keyword_cc_name est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1283">A keyword from Keyword_cc_name is found.</span></span>
    - <span data-ttu-id="64f1e-1284">La fonction Func_expiration_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1284">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="64f1e-1285">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1285">The checksum passes.</span></span>

<span data-ttu-id="64f1e-1286">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-1286">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-1287">La fonction Func_credit_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1287">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-1288">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1288">The checksum passes.</span></span>

```
<!-- Credit Card Number -->
<Entity id="50842eb7-edc8-4019-85dd-5a5c1f2bb085" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_credit_card" />
        <Any minMatches="1">
          <Match idRef="Keyword_cc_verification" />
          <Match idRef="Keyword_cc_name" />
          <Match idRef="Func_expiration_date" />
        </Any>
  </Pattern>
  <Pattern confidenceLevel="65">
        <IdMatch idRef="Func_credit_card" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-1289">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-1289">Keywords</span></span>

#### <a name="keywordccverification"></a><span data-ttu-id="64f1e-1290">Keyword_cc_verification</span><span class="sxs-lookup"><span data-stu-id="64f1e-1290">Keyword_cc_verification</span></span>

- <span data-ttu-id="64f1e-1291">vérification de la carte</span><span class="sxs-lookup"><span data-stu-id="64f1e-1291">card verification</span></span>
- <span data-ttu-id="64f1e-1292">numéro d’identification de la carte</span><span class="sxs-lookup"><span data-stu-id="64f1e-1292">card identification number</span></span>
- <span data-ttu-id="64f1e-1293">cryptogramme</span><span class="sxs-lookup"><span data-stu-id="64f1e-1293">cvn</span></span>
- <span data-ttu-id="64f1e-1294">nic</span><span class="sxs-lookup"><span data-stu-id="64f1e-1294">cid</span></span>
- <span data-ttu-id="64f1e-1295">CVC2</span><span class="sxs-lookup"><span data-stu-id="64f1e-1295">cvc2</span></span>
- <span data-ttu-id="64f1e-1296">CVV2</span><span class="sxs-lookup"><span data-stu-id="64f1e-1296">cvv2</span></span>
- <span data-ttu-id="64f1e-1297">pin block</span><span class="sxs-lookup"><span data-stu-id="64f1e-1297">pin block</span></span>
- <span data-ttu-id="64f1e-1298">code de sécurité</span><span class="sxs-lookup"><span data-stu-id="64f1e-1298">security code</span></span>
- <span data-ttu-id="64f1e-1299">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="64f1e-1299">security number</span></span>
- <span data-ttu-id="64f1e-1300">n° de sécurité</span><span class="sxs-lookup"><span data-stu-id="64f1e-1300">security no</span></span>
- <span data-ttu-id="64f1e-1301">numéro d’émission</span><span class="sxs-lookup"><span data-stu-id="64f1e-1301">issue number</span></span>
- <span data-ttu-id="64f1e-1302">n° d’émission</span><span class="sxs-lookup"><span data-stu-id="64f1e-1302">issue no</span></span>
- <span data-ttu-id="64f1e-1303">cryptogramme</span><span class="sxs-lookup"><span data-stu-id="64f1e-1303">cryptogramme</span></span>
- <span data-ttu-id="64f1e-1304">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="64f1e-1304">numéro de sécurité</span></span>
- <span data-ttu-id="64f1e-1305">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="64f1e-1305">numero de securite</span></span>
- <span data-ttu-id="64f1e-1306">kreditkartenprüfnummer</span><span class="sxs-lookup"><span data-stu-id="64f1e-1306">kreditkartenprüfnummer</span></span>
- <span data-ttu-id="64f1e-1307">kreditkartenprufnummer</span><span class="sxs-lookup"><span data-stu-id="64f1e-1307">kreditkartenprufnummer</span></span>
- <span data-ttu-id="64f1e-1308">Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="64f1e-1308">prüfziffer</span></span>
- <span data-ttu-id="64f1e-1309">prufziffer</span><span class="sxs-lookup"><span data-stu-id="64f1e-1309">prufziffer</span></span>
- <span data-ttu-id="64f1e-1310">sicherheits Kode</span><span class="sxs-lookup"><span data-stu-id="64f1e-1310">sicherheits Kode</span></span>
- <span data-ttu-id="64f1e-1311">Sicherheitscode</span><span class="sxs-lookup"><span data-stu-id="64f1e-1311">sicherheitscode</span></span>
- <span data-ttu-id="64f1e-1312">sicherheitsnummer</span><span class="sxs-lookup"><span data-stu-id="64f1e-1312">sicherheitsnummer</span></span>
- <span data-ttu-id="64f1e-1313">verfalldatum</span><span class="sxs-lookup"><span data-stu-id="64f1e-1313">verfalldatum</span></span>
- <span data-ttu-id="64f1e-1314">codice di verifica</span><span class="sxs-lookup"><span data-stu-id="64f1e-1314">codice di verifica</span></span>
- <span data-ttu-id="64f1e-1315">contre.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1315">cod.</span></span> <span data-ttu-id="64f1e-1316">sicurezza</span><span class="sxs-lookup"><span data-stu-id="64f1e-1316">sicurezza</span></span>
- <span data-ttu-id="64f1e-1317">cod sicurezza</span><span class="sxs-lookup"><span data-stu-id="64f1e-1317">cod sicurezza</span></span>
- <span data-ttu-id="64f1e-1318">n autorizzazione</span><span class="sxs-lookup"><span data-stu-id="64f1e-1318">n autorizzazione</span></span>
- <span data-ttu-id="64f1e-1319">Código</span><span class="sxs-lookup"><span data-stu-id="64f1e-1319">código</span></span>
- <span data-ttu-id="64f1e-1320">Codigo</span><span class="sxs-lookup"><span data-stu-id="64f1e-1320">codigo</span></span>
- <span data-ttu-id="64f1e-1321">contre.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1321">cod.</span></span> <span data-ttu-id="64f1e-1322">SEG</span><span class="sxs-lookup"><span data-stu-id="64f1e-1322">seg</span></span>
- <span data-ttu-id="64f1e-1323">cod seg</span><span class="sxs-lookup"><span data-stu-id="64f1e-1323">cod seg</span></span>
- <span data-ttu-id="64f1e-1324">código de segurança</span><span class="sxs-lookup"><span data-stu-id="64f1e-1324">código de segurança</span></span>
- <span data-ttu-id="64f1e-1325">codigo de seguranca</span><span class="sxs-lookup"><span data-stu-id="64f1e-1325">codigo de seguranca</span></span>
- <span data-ttu-id="64f1e-1326">codigo de segurança</span><span class="sxs-lookup"><span data-stu-id="64f1e-1326">codigo de segurança</span></span>
- <span data-ttu-id="64f1e-1327">código de seguranca</span><span class="sxs-lookup"><span data-stu-id="64f1e-1327">código de seguranca</span></span>
- <span data-ttu-id="64f1e-1328">Cód.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1328">cód.</span></span> <span data-ttu-id="64f1e-1329">Segurança</span><span class="sxs-lookup"><span data-stu-id="64f1e-1329">segurança</span></span>
- <span data-ttu-id="64f1e-1330">contre.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1330">cod.</span></span> <span data-ttu-id="64f1e-1331">Seguranca COD.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1331">seguranca cod.</span></span> <span data-ttu-id="64f1e-1332">Segurança</span><span class="sxs-lookup"><span data-stu-id="64f1e-1332">segurança</span></span>
- <span data-ttu-id="64f1e-1333">Cód.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1333">cód.</span></span> <span data-ttu-id="64f1e-1334">Seguranca</span><span class="sxs-lookup"><span data-stu-id="64f1e-1334">seguranca</span></span>
- <span data-ttu-id="64f1e-1335">cód segurança</span><span class="sxs-lookup"><span data-stu-id="64f1e-1335">cód segurança</span></span>
- <span data-ttu-id="64f1e-1336">COD Seguranca COD Segurança</span><span class="sxs-lookup"><span data-stu-id="64f1e-1336">cod seguranca cod segurança</span></span>
- <span data-ttu-id="64f1e-1337">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="64f1e-1337">cód seguranca</span></span>
- <span data-ttu-id="64f1e-1338">número de verificação</span><span class="sxs-lookup"><span data-stu-id="64f1e-1338">número de verificação</span></span>
- <span data-ttu-id="64f1e-1339">numero de verificacao</span><span class="sxs-lookup"><span data-stu-id="64f1e-1339">numero de verificacao</span></span>
- <span data-ttu-id="64f1e-1340">Ablauf</span><span class="sxs-lookup"><span data-stu-id="64f1e-1340">ablauf</span></span>
- <span data-ttu-id="64f1e-1341">gültig bis</span><span class="sxs-lookup"><span data-stu-id="64f1e-1341">gültig bis</span></span>
- <span data-ttu-id="64f1e-1342">gültigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="64f1e-1342">gültigkeitsdatum</span></span>
- <span data-ttu-id="64f1e-1343">gultig bis</span><span class="sxs-lookup"><span data-stu-id="64f1e-1343">gultig bis</span></span>
- <span data-ttu-id="64f1e-1344">gultigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="64f1e-1344">gultigkeitsdatum</span></span>
- <span data-ttu-id="64f1e-1345">scadenza</span><span class="sxs-lookup"><span data-stu-id="64f1e-1345">scadenza</span></span>
- <span data-ttu-id="64f1e-1346">data scad</span><span class="sxs-lookup"><span data-stu-id="64f1e-1346">data scad</span></span>
- <span data-ttu-id="64f1e-1347">fecha de expiracion</span><span class="sxs-lookup"><span data-stu-id="64f1e-1347">fecha de expiracion</span></span>
- <span data-ttu-id="64f1e-1348">fecha de venc</span><span class="sxs-lookup"><span data-stu-id="64f1e-1348">fecha de venc</span></span>
- <span data-ttu-id="64f1e-1349">vencimiento</span><span class="sxs-lookup"><span data-stu-id="64f1e-1349">vencimiento</span></span>
- <span data-ttu-id="64f1e-1350">válido hasta</span><span class="sxs-lookup"><span data-stu-id="64f1e-1350">válido hasta</span></span>
- <span data-ttu-id="64f1e-1351">valido hasta</span><span class="sxs-lookup"><span data-stu-id="64f1e-1351">valido hasta</span></span>
- <span data-ttu-id="64f1e-1352">vto</span><span class="sxs-lookup"><span data-stu-id="64f1e-1352">vto</span></span>
- <span data-ttu-id="64f1e-1353">data de expiração</span><span class="sxs-lookup"><span data-stu-id="64f1e-1353">data de expiração</span></span>
- <span data-ttu-id="64f1e-1354">data de expiracao</span><span class="sxs-lookup"><span data-stu-id="64f1e-1354">data de expiracao</span></span>
- <span data-ttu-id="64f1e-1355">data em que expira</span><span class="sxs-lookup"><span data-stu-id="64f1e-1355">data em que expira</span></span>
- <span data-ttu-id="64f1e-1356">Validade</span><span class="sxs-lookup"><span data-stu-id="64f1e-1356">validade</span></span>
- <span data-ttu-id="64f1e-1357">valorisation</span><span class="sxs-lookup"><span data-stu-id="64f1e-1357">valor</span></span>
- <span data-ttu-id="64f1e-1358">vencimento</span><span class="sxs-lookup"><span data-stu-id="64f1e-1358">vencimento</span></span>
- <span data-ttu-id="64f1e-1359">Venc</span><span class="sxs-lookup"><span data-stu-id="64f1e-1359">Venc</span></span> 

#### <a name="keywordccname"></a><span data-ttu-id="64f1e-1360">Keyword_cc_name</span><span class="sxs-lookup"><span data-stu-id="64f1e-1360">Keyword_cc_name</span></span>

- <span data-ttu-id="64f1e-1361">American</span><span class="sxs-lookup"><span data-stu-id="64f1e-1361">amex</span></span>
- <span data-ttu-id="64f1e-1362">american express</span><span class="sxs-lookup"><span data-stu-id="64f1e-1362">american express</span></span>
- <span data-ttu-id="64f1e-1363">AmericanExpress</span><span class="sxs-lookup"><span data-stu-id="64f1e-1363">americanexpress</span></span>
- <span data-ttu-id="64f1e-1364">Délivrance</span><span class="sxs-lookup"><span data-stu-id="64f1e-1364">Visa</span></span>
- <span data-ttu-id="64f1e-1365">MasterCard</span><span class="sxs-lookup"><span data-stu-id="64f1e-1365">mastercard</span></span>
- <span data-ttu-id="64f1e-1366">master card</span><span class="sxs-lookup"><span data-stu-id="64f1e-1366">master card</span></span>
- <span data-ttu-id="64f1e-1367">McDonald</span><span class="sxs-lookup"><span data-stu-id="64f1e-1367">mc</span></span> 
- <span data-ttu-id="64f1e-1368">MasterCard</span><span class="sxs-lookup"><span data-stu-id="64f1e-1368">mastercards</span></span>
- <span data-ttu-id="64f1e-1369">master cards</span><span class="sxs-lookup"><span data-stu-id="64f1e-1369">master cards</span></span>
- <span data-ttu-id="64f1e-1370">diner’s Club</span><span class="sxs-lookup"><span data-stu-id="64f1e-1370">diner's Club</span></span>
- <span data-ttu-id="64f1e-1371">diners club</span><span class="sxs-lookup"><span data-stu-id="64f1e-1371">diners club</span></span>
- <span data-ttu-id="64f1e-1372">DinersClub</span><span class="sxs-lookup"><span data-stu-id="64f1e-1372">dinersclub</span></span>
- <span data-ttu-id="64f1e-1373">discover card</span><span class="sxs-lookup"><span data-stu-id="64f1e-1373">discover card</span></span>
- <span data-ttu-id="64f1e-1374">discovercard</span><span class="sxs-lookup"><span data-stu-id="64f1e-1374">discovercard</span></span>
- <span data-ttu-id="64f1e-1375">discover cards</span><span class="sxs-lookup"><span data-stu-id="64f1e-1375">discover cards</span></span>
- <span data-ttu-id="64f1e-1376">JCB</span><span class="sxs-lookup"><span data-stu-id="64f1e-1376">JCB</span></span>
- <span data-ttu-id="64f1e-1377">japanese card bureau</span><span class="sxs-lookup"><span data-stu-id="64f1e-1377">japanese card bureau</span></span>
- <span data-ttu-id="64f1e-1378">carte blanche</span><span class="sxs-lookup"><span data-stu-id="64f1e-1378">carte blanche</span></span>
- <span data-ttu-id="64f1e-1379">carteblanche</span><span class="sxs-lookup"><span data-stu-id="64f1e-1379">carteblanche</span></span>
- <span data-ttu-id="64f1e-1380">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="64f1e-1380">credit card</span></span>
- <span data-ttu-id="64f1e-1381">CC</span><span class="sxs-lookup"><span data-stu-id="64f1e-1381">cc#</span></span>
- <span data-ttu-id="64f1e-1382">n ° de CC:</span><span class="sxs-lookup"><span data-stu-id="64f1e-1382">cc#:</span></span>
- <span data-ttu-id="64f1e-1383">date d’expiration</span><span class="sxs-lookup"><span data-stu-id="64f1e-1383">expiration date</span></span>
- <span data-ttu-id="64f1e-1384">date d’exp</span><span class="sxs-lookup"><span data-stu-id="64f1e-1384">exp date</span></span>
- <span data-ttu-id="64f1e-1385">date d’expiration</span><span class="sxs-lookup"><span data-stu-id="64f1e-1385">expiry date</span></span>
- <span data-ttu-id="64f1e-1386">date d’expiration</span><span class="sxs-lookup"><span data-stu-id="64f1e-1386">date d’expiration</span></span>
- <span data-ttu-id="64f1e-1387">date d’exp</span><span class="sxs-lookup"><span data-stu-id="64f1e-1387">date d'exp</span></span>
- <span data-ttu-id="64f1e-1388">date expiration</span><span class="sxs-lookup"><span data-stu-id="64f1e-1388">date expiration</span></span>
- <span data-ttu-id="64f1e-1389">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="64f1e-1389">bank card</span></span>
- <span data-ttu-id="64f1e-1390">BankCard</span><span class="sxs-lookup"><span data-stu-id="64f1e-1390">bankcard</span></span>
- <span data-ttu-id="64f1e-1391">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="64f1e-1391">card number</span></span>
- <span data-ttu-id="64f1e-1392">num de carte</span><span class="sxs-lookup"><span data-stu-id="64f1e-1392">card num</span></span>
- <span data-ttu-id="64f1e-1393">carte</span><span class="sxs-lookup"><span data-stu-id="64f1e-1393">cardnumber</span></span>
- <span data-ttu-id="64f1e-1394">carte</span><span class="sxs-lookup"><span data-stu-id="64f1e-1394">cardnumbers</span></span>
- <span data-ttu-id="64f1e-1395">numéros de carte</span><span class="sxs-lookup"><span data-stu-id="64f1e-1395">card numbers</span></span>
- <span data-ttu-id="64f1e-1396">CreditCard</span><span class="sxs-lookup"><span data-stu-id="64f1e-1396">creditcard</span></span>
- <span data-ttu-id="64f1e-1397">cartes de crédit</span><span class="sxs-lookup"><span data-stu-id="64f1e-1397">credit cards</span></span>
- <span data-ttu-id="64f1e-1398">crédit</span><span class="sxs-lookup"><span data-stu-id="64f1e-1398">creditcards</span></span>
- <span data-ttu-id="64f1e-1399">CCN</span><span class="sxs-lookup"><span data-stu-id="64f1e-1399">ccn</span></span>
- <span data-ttu-id="64f1e-1400">titulaire de la carte</span><span class="sxs-lookup"><span data-stu-id="64f1e-1400">card holder</span></span>
- <span data-ttu-id="64f1e-1401">titulaires</span><span class="sxs-lookup"><span data-stu-id="64f1e-1401">cardholder</span></span>
- <span data-ttu-id="64f1e-1402">titulaires de la carte</span><span class="sxs-lookup"><span data-stu-id="64f1e-1402">card holders</span></span>
- <span data-ttu-id="64f1e-1403">titulaires</span><span class="sxs-lookup"><span data-stu-id="64f1e-1403">cardholders</span></span>
- <span data-ttu-id="64f1e-1404">carte de vérification</span><span class="sxs-lookup"><span data-stu-id="64f1e-1404">check card</span></span>
- <span data-ttu-id="64f1e-1405">carte</span><span class="sxs-lookup"><span data-stu-id="64f1e-1405">checkcard</span></span>
- <span data-ttu-id="64f1e-1406">cartes de vérification</span><span class="sxs-lookup"><span data-stu-id="64f1e-1406">check cards</span></span>
- <span data-ttu-id="64f1e-1407">cartes</span><span class="sxs-lookup"><span data-stu-id="64f1e-1407">checkcards</span></span>
- <span data-ttu-id="64f1e-1408">carte de débit</span><span class="sxs-lookup"><span data-stu-id="64f1e-1408">debit card</span></span>
- <span data-ttu-id="64f1e-1409">débit</span><span class="sxs-lookup"><span data-stu-id="64f1e-1409">debitcard</span></span>
- <span data-ttu-id="64f1e-1410">cartes de débit</span><span class="sxs-lookup"><span data-stu-id="64f1e-1410">debit cards</span></span>
- <span data-ttu-id="64f1e-1411">débit</span><span class="sxs-lookup"><span data-stu-id="64f1e-1411">debitcards</span></span>
- <span data-ttu-id="64f1e-1412">carte de retrait</span><span class="sxs-lookup"><span data-stu-id="64f1e-1412">atm card</span></span>
- <span data-ttu-id="64f1e-1413">retrait</span><span class="sxs-lookup"><span data-stu-id="64f1e-1413">atmcard</span></span>
- <span data-ttu-id="64f1e-1414">cartes de retrait</span><span class="sxs-lookup"><span data-stu-id="64f1e-1414">atm cards</span></span>
- <span data-ttu-id="64f1e-1415">retrait</span><span class="sxs-lookup"><span data-stu-id="64f1e-1415">atmcards</span></span>
- <span data-ttu-id="64f1e-1416">envoier</span><span class="sxs-lookup"><span data-stu-id="64f1e-1416">enroute</span></span>
- <span data-ttu-id="64f1e-1417">en route</span><span class="sxs-lookup"><span data-stu-id="64f1e-1417">en route</span></span>
- <span data-ttu-id="64f1e-1418">type de carte</span><span class="sxs-lookup"><span data-stu-id="64f1e-1418">card type</span></span>
- <span data-ttu-id="64f1e-1419">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="64f1e-1419">carte bancaire</span></span>
- <span data-ttu-id="64f1e-1420">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="64f1e-1420">carte de crédit</span></span>
- <span data-ttu-id="64f1e-1421">carte de credit</span><span class="sxs-lookup"><span data-stu-id="64f1e-1421">carte de credit</span></span>
- <span data-ttu-id="64f1e-1422">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="64f1e-1422">numéro de carte</span></span>
- <span data-ttu-id="64f1e-1423">numero de carte</span><span class="sxs-lookup"><span data-stu-id="64f1e-1423">numero de carte</span></span>
- <span data-ttu-id="64f1e-1424">nº de la carte</span><span class="sxs-lookup"><span data-stu-id="64f1e-1424">nº de la carte</span></span>
- <span data-ttu-id="64f1e-1425">nº de carte</span><span class="sxs-lookup"><span data-stu-id="64f1e-1425">nº de carte</span></span>
- <span data-ttu-id="64f1e-1426">Kreditkarte</span><span class="sxs-lookup"><span data-stu-id="64f1e-1426">kreditkarte</span></span>
- <span data-ttu-id="64f1e-1427">Karte</span><span class="sxs-lookup"><span data-stu-id="64f1e-1427">karte</span></span>
- <span data-ttu-id="64f1e-1428">karteninhaber</span><span class="sxs-lookup"><span data-stu-id="64f1e-1428">karteninhaber</span></span>
- <span data-ttu-id="64f1e-1429">karteninhabers</span><span class="sxs-lookup"><span data-stu-id="64f1e-1429">karteninhabers</span></span>
- <span data-ttu-id="64f1e-1430">kreditkarteninhaber</span><span class="sxs-lookup"><span data-stu-id="64f1e-1430">kreditkarteninhaber</span></span>
- <span data-ttu-id="64f1e-1431">kreditkarteninstitut</span><span class="sxs-lookup"><span data-stu-id="64f1e-1431">kreditkarteninstitut</span></span>
- <span data-ttu-id="64f1e-1432">kreditkartentyp</span><span class="sxs-lookup"><span data-stu-id="64f1e-1432">kreditkartentyp</span></span>
- <span data-ttu-id="64f1e-1433">eigentümername</span><span class="sxs-lookup"><span data-stu-id="64f1e-1433">eigentümername</span></span>
- <span data-ttu-id="64f1e-1434">kartennr</span><span class="sxs-lookup"><span data-stu-id="64f1e-1434">kartennr</span></span> 
- <span data-ttu-id="64f1e-1435">kartennummer</span><span class="sxs-lookup"><span data-stu-id="64f1e-1435">kartennummer</span></span>
- <span data-ttu-id="64f1e-1436">Kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="64f1e-1436">kreditkartennummer</span></span>
- <span data-ttu-id="64f1e-1437">Kreditkarten-Nummer</span><span class="sxs-lookup"><span data-stu-id="64f1e-1437">kreditkarten-nummer</span></span>
- <span data-ttu-id="64f1e-1438">Carta di credito</span><span class="sxs-lookup"><span data-stu-id="64f1e-1438">carta di credito</span></span>
- <span data-ttu-id="64f1e-1439">Carta credito</span><span class="sxs-lookup"><span data-stu-id="64f1e-1439">carta credito</span></span>
- <span data-ttu-id="64f1e-1440">Carta</span><span class="sxs-lookup"><span data-stu-id="64f1e-1440">carta</span></span>
- <span data-ttu-id="64f1e-1441">n carta</span><span class="sxs-lookup"><span data-stu-id="64f1e-1441">n carta</span></span>
- <span data-ttu-id="64f1e-1442">Nr.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1442">nr.</span></span> <span data-ttu-id="64f1e-1443">Carta</span><span class="sxs-lookup"><span data-stu-id="64f1e-1443">carta</span></span>
- <span data-ttu-id="64f1e-1444">nr carta</span><span class="sxs-lookup"><span data-stu-id="64f1e-1444">nr carta</span></span>
- <span data-ttu-id="64f1e-1445">numero carta</span><span class="sxs-lookup"><span data-stu-id="64f1e-1445">numero carta</span></span>
- <span data-ttu-id="64f1e-1446">numero della carta</span><span class="sxs-lookup"><span data-stu-id="64f1e-1446">numero della carta</span></span>
- <span data-ttu-id="64f1e-1447">numero di carta</span><span class="sxs-lookup"><span data-stu-id="64f1e-1447">numero di carta</span></span>
- <span data-ttu-id="64f1e-1448">tarjeta credito</span><span class="sxs-lookup"><span data-stu-id="64f1e-1448">tarjeta credito</span></span>
- <span data-ttu-id="64f1e-1449">tarjeta de credito</span><span class="sxs-lookup"><span data-stu-id="64f1e-1449">tarjeta de credito</span></span>
- <span data-ttu-id="64f1e-1450">tarjeta crédito</span><span class="sxs-lookup"><span data-stu-id="64f1e-1450">tarjeta crédito</span></span>
- <span data-ttu-id="64f1e-1451">tarjeta de crédito</span><span class="sxs-lookup"><span data-stu-id="64f1e-1451">tarjeta de crédito</span></span>
- <span data-ttu-id="64f1e-1452">tarjeta de atm</span><span class="sxs-lookup"><span data-stu-id="64f1e-1452">tarjeta de atm</span></span>
- <span data-ttu-id="64f1e-1453">tarjeta atm</span><span class="sxs-lookup"><span data-stu-id="64f1e-1453">tarjeta atm</span></span>
- <span data-ttu-id="64f1e-1454">tarjeta debito</span><span class="sxs-lookup"><span data-stu-id="64f1e-1454">tarjeta debito</span></span>
- <span data-ttu-id="64f1e-1455">tarjeta de debito</span><span class="sxs-lookup"><span data-stu-id="64f1e-1455">tarjeta de debito</span></span>
- <span data-ttu-id="64f1e-1456">tarjeta débito</span><span class="sxs-lookup"><span data-stu-id="64f1e-1456">tarjeta débito</span></span>
- <span data-ttu-id="64f1e-1457">tarjeta de débito</span><span class="sxs-lookup"><span data-stu-id="64f1e-1457">tarjeta de débito</span></span>
- <span data-ttu-id="64f1e-1458">nº de tarjeta</span><span class="sxs-lookup"><span data-stu-id="64f1e-1458">nº de tarjeta</span></span>
- <span data-ttu-id="64f1e-1459">Nbre.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1459">no.</span></span> <span data-ttu-id="64f1e-1460">de tarjeta</span><span class="sxs-lookup"><span data-stu-id="64f1e-1460">de tarjeta</span></span>
- <span data-ttu-id="64f1e-1461">no de tarjeta</span><span class="sxs-lookup"><span data-stu-id="64f1e-1461">no de tarjeta</span></span>
- <span data-ttu-id="64f1e-1462">numero de tarjeta</span><span class="sxs-lookup"><span data-stu-id="64f1e-1462">numero de tarjeta</span></span>
- <span data-ttu-id="64f1e-1463">número de tarjeta</span><span class="sxs-lookup"><span data-stu-id="64f1e-1463">número de tarjeta</span></span>
- <span data-ttu-id="64f1e-1464">tarjeta no</span><span class="sxs-lookup"><span data-stu-id="64f1e-1464">tarjeta no</span></span>
- <span data-ttu-id="64f1e-1465">tarjetahabiente</span><span class="sxs-lookup"><span data-stu-id="64f1e-1465">tarjetahabiente</span></span>
- <span data-ttu-id="64f1e-1466">cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="64f1e-1466">cartão de crédito</span></span>
- <span data-ttu-id="64f1e-1467">cartão de credito</span><span class="sxs-lookup"><span data-stu-id="64f1e-1467">cartão de credito</span></span>
- <span data-ttu-id="64f1e-1468">cartao de crédito</span><span class="sxs-lookup"><span data-stu-id="64f1e-1468">cartao de crédito</span></span>
- <span data-ttu-id="64f1e-1469">cartao de credito</span><span class="sxs-lookup"><span data-stu-id="64f1e-1469">cartao de credito</span></span>
- <span data-ttu-id="64f1e-1470">cartão de débito</span><span class="sxs-lookup"><span data-stu-id="64f1e-1470">cartão de débito</span></span>
- <span data-ttu-id="64f1e-1471">cartao de débito</span><span class="sxs-lookup"><span data-stu-id="64f1e-1471">cartao de débito</span></span>
- <span data-ttu-id="64f1e-1472">cartão de debito</span><span class="sxs-lookup"><span data-stu-id="64f1e-1472">cartão de debito</span></span>
- <span data-ttu-id="64f1e-1473">cartao de debito</span><span class="sxs-lookup"><span data-stu-id="64f1e-1473">cartao de debito</span></span>
- <span data-ttu-id="64f1e-1474">débito automático</span><span class="sxs-lookup"><span data-stu-id="64f1e-1474">débito automático</span></span>
- <span data-ttu-id="64f1e-1475">debito automatico</span><span class="sxs-lookup"><span data-stu-id="64f1e-1475">debito automatico</span></span>
- <span data-ttu-id="64f1e-1476">número do cartão</span><span class="sxs-lookup"><span data-stu-id="64f1e-1476">número do cartão</span></span>
- <span data-ttu-id="64f1e-1477">numero do cartão</span><span class="sxs-lookup"><span data-stu-id="64f1e-1477">numero do cartão</span></span> 
- <span data-ttu-id="64f1e-1478">número do cartao</span><span class="sxs-lookup"><span data-stu-id="64f1e-1478">número do cartao</span></span>
- <span data-ttu-id="64f1e-1479">numero do cartao</span><span class="sxs-lookup"><span data-stu-id="64f1e-1479">numero do cartao</span></span>
- <span data-ttu-id="64f1e-1480">número de cartão</span><span class="sxs-lookup"><span data-stu-id="64f1e-1480">número de cartão</span></span>
- <span data-ttu-id="64f1e-1481">numero de cartão</span><span class="sxs-lookup"><span data-stu-id="64f1e-1481">numero de cartão</span></span>
- <span data-ttu-id="64f1e-1482">número de cartao</span><span class="sxs-lookup"><span data-stu-id="64f1e-1482">número de cartao</span></span>
- <span data-ttu-id="64f1e-1483">numero de cartao</span><span class="sxs-lookup"><span data-stu-id="64f1e-1483">numero de cartao</span></span>
- <span data-ttu-id="64f1e-1484">nº do cartão</span><span class="sxs-lookup"><span data-stu-id="64f1e-1484">nº do cartão</span></span>
- <span data-ttu-id="64f1e-1485">nº do cartao</span><span class="sxs-lookup"><span data-stu-id="64f1e-1485">nº do cartao</span></span>
- <span data-ttu-id="64f1e-1486">n º.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1486">nº.</span></span> <span data-ttu-id="64f1e-1487">do cartão</span><span class="sxs-lookup"><span data-stu-id="64f1e-1487">do cartão</span></span>
- <span data-ttu-id="64f1e-1488">no do cartão</span><span class="sxs-lookup"><span data-stu-id="64f1e-1488">no do cartão</span></span>
- <span data-ttu-id="64f1e-1489">no do cartao</span><span class="sxs-lookup"><span data-stu-id="64f1e-1489">no do cartao</span></span>
- <span data-ttu-id="64f1e-1490">Nbre.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1490">no.</span></span> <span data-ttu-id="64f1e-1491">do cartão</span><span class="sxs-lookup"><span data-stu-id="64f1e-1491">do cartão</span></span>
- <span data-ttu-id="64f1e-1492">Nbre.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1492">no.</span></span> <span data-ttu-id="64f1e-1493">do cartao</span><span class="sxs-lookup"><span data-stu-id="64f1e-1493">do cartao</span></span> 
   
## <a name="croatia-identity-card-number"></a><span data-ttu-id="64f1e-1494">	Numéro de carte d’identité Croatie</span><span class="sxs-lookup"><span data-stu-id="64f1e-1494">Croatia Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-1495">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-1495">Format</span></span>

<span data-ttu-id="64f1e-1496">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-1496">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-1497">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-1497">Pattern</span></span>

<span data-ttu-id="64f1e-1498">Neuf chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="64f1e-1498">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-1499">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-1499">Checksum</span></span>

<span data-ttu-id="64f1e-1500">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-1500">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-1501">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-1501">Definition</span></span>

<span data-ttu-id="64f1e-1502">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-1502">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-1503">La fonction Func_croatia_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1503">The function Func_croatia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-1504">Un mot clé figurant dans la liste Keyword_croatia_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1504">A keyword from Keyword_croatia_id_card is found.</span></span>

```
<!--Croatia Identity Card Number-->
<Entity id="ff12f884-c20a-4189-b185-34c8e7258d47" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_croatia_id_card"/>
     <Match idRef="Keyword_croatia_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-1505">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-1505">Keywords</span></span>

#### <a name="keywordcroatiaidcard"></a><span data-ttu-id="64f1e-1506">Keyword_croatia_id_card</span><span class="sxs-lookup"><span data-stu-id="64f1e-1506">Keyword_croatia_id_card</span></span>

- <span data-ttu-id="64f1e-1507">Croatian identity card</span><span class="sxs-lookup"><span data-stu-id="64f1e-1507">Croatian identity card</span></span>
- <span data-ttu-id="64f1e-1508">Osobna iskaznica</span><span class="sxs-lookup"><span data-stu-id="64f1e-1508">Osobna iskaznica</span></span>

   
## <a name="croatia-personal-identification-oib-number"></a><span data-ttu-id="64f1e-1509">	Numéro d’identification personnel (OIB) Croatie</span><span class="sxs-lookup"><span data-stu-id="64f1e-1509">Croatia Personal Identification (OIB) Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-1510">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-1510">Format</span></span>

<span data-ttu-id="64f1e-1511">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-1511">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-1512">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-1512">Pattern</span></span>

<span data-ttu-id="64f1e-1513">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="64f1e-1513">11 digits:</span></span>
- <span data-ttu-id="64f1e-1514">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-1514">10 digits</span></span> 
- <span data-ttu-id="64f1e-1515">Le chiffre final est un chiffre de contrôle aux fins de l'échange de données internationales, les lettres HR sont ajoutées avant les onze chiffres.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1515">Final digit is a check digit For the purposes of international data exchange, the letters HR are added preceding the eleven digits.</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-1516">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-1516">Checksum</span></span>

<span data-ttu-id="64f1e-1517">Oui</span><span class="sxs-lookup"><span data-stu-id="64f1e-1517">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-1518">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-1518">Definition</span></span>

<span data-ttu-id="64f1e-1519">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-1519">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-1520">La fonction Func_croatia_oib_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1520">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-1521">Un mot clé figurant dans la liste Keyword_croatia_oib_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1521">A keyword from Keyword_croatia_oib_number is found.</span></span>
- <span data-ttu-id="64f1e-1522">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1522">The checksum passes.</span></span>

<span data-ttu-id="64f1e-1523">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-1523">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-1524">La fonction Func_croatia_oib_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1524">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-1525">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1525">The checksum passes.</span></span>

```
<!-- Croatia Personal Identification (OIB) Number -->
<Entity id="31983b6d-db95-4eb2-a630-b44bd091968d" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_croatia_oib_number"/>
     <Match idRef="Keyword_croatia_oib_number"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_croatia_oib_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-1526">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-1526">Keywords</span></span>

#### <a name="keywordcroatiaoibnumber"></a><span data-ttu-id="64f1e-1527">Keyword_croatia_oib_number</span><span class="sxs-lookup"><span data-stu-id="64f1e-1527">Keyword_croatia_oib_number</span></span>

- <span data-ttu-id="64f1e-1528">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="64f1e-1528">Personal Identification Number</span></span>
- <span data-ttu-id="64f1e-1529">Osobni identifikacijski broj</span><span class="sxs-lookup"><span data-stu-id="64f1e-1529">Osobni identifikacijski broj</span></span> 
- <span data-ttu-id="64f1e-1530">OIB</span><span class="sxs-lookup"><span data-stu-id="64f1e-1530">OIB</span></span> 

   
## <a name="czech-personal-identity-number"></a><span data-ttu-id="64f1e-1531">Numéro d'identité personnelle tchèque</span><span class="sxs-lookup"><span data-stu-id="64f1e-1531">Czech Personal Identity Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-1532">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-1532">Format</span></span>

<span data-ttu-id="64f1e-1533">Neuf chiffres avec une barre oblique inverse facultative (ancien format) 10 chiffres avec une barre oblique facultative (nouveau format)</span><span class="sxs-lookup"><span data-stu-id="64f1e-1533">Nine digits with optional forward slash (old format) 10 digits with optional forward slash (new format)</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-1534">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-1534">Pattern</span></span>

<span data-ttu-id="64f1e-1535">Neuf chiffres (ancien format):</span><span class="sxs-lookup"><span data-stu-id="64f1e-1535">Nine digits (old format):</span></span>
- <span data-ttu-id="64f1e-1536">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-1536">Nine digits</span></span>

<span data-ttu-id="64f1e-1537">OU</span><span class="sxs-lookup"><span data-stu-id="64f1e-1537">OR</span></span>

- <span data-ttu-id="64f1e-1538">Six chiffres qui représentent la date de naissance</span><span class="sxs-lookup"><span data-stu-id="64f1e-1538">Six digits that represent date of birth</span></span>
- <span data-ttu-id="64f1e-1539">Une barre oblique </span><span class="sxs-lookup"><span data-stu-id="64f1e-1539">A forward slash</span></span>
- <span data-ttu-id="64f1e-1540">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-1540">Three digits</span></span>

<span data-ttu-id="64f1e-1541">10 chiffres (nouveau format):</span><span class="sxs-lookup"><span data-stu-id="64f1e-1541">10 digits (new format):</span></span>
- <span data-ttu-id="64f1e-1542">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-1542">10 digits</span></span>

<span data-ttu-id="64f1e-1543">OU</span><span class="sxs-lookup"><span data-stu-id="64f1e-1543">OR</span></span>

- <span data-ttu-id="64f1e-1544">Six chiffres qui représentent la date de naissance</span><span class="sxs-lookup"><span data-stu-id="64f1e-1544">Six digits that represent date of birth</span></span>
- <span data-ttu-id="64f1e-1545">Une barre oblique </span><span class="sxs-lookup"><span data-stu-id="64f1e-1545">A forward slash</span></span> 
- <span data-ttu-id="64f1e-1546">Quatre chiffres où le dernier chiffre est un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-1546">Four digits where last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-1547">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-1547">Checksum</span></span>

<span data-ttu-id="64f1e-1548">Oui</span><span class="sxs-lookup"><span data-stu-id="64f1e-1548">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-1549">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-1549">Definition</span></span>

<span data-ttu-id="64f1e-1550">Une stratégie DLP est sûre à 85% d'avoir détecté ce type d'informations sensibles si, dans une proximité de 300 caractères: la fonction Func_czech_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1550">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_czech_id_card finds content that matches the pattern.</span></span>
<span data-ttu-id="64f1e-1551">Un mot clé figurant dans la liste Keyword_czech_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1551">A keyword from Keyword_czech_id_card is found.</span></span>
<span data-ttu-id="64f1e-1552">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1552">The checksum passes.</span></span>

```
<!-- Czech Personal Identity Number -->
<Entity id="60c0725a-4eb6-455b-9dda-05d8a7396497"      patternsProximity="300" recommendedConfidence="85">
   <Pattern confidenceLevel="85">
      <IdMatch idRef="Func_czech_id_card" />
      <Match idRef="Keyword_czech_id_card" />
   </Pattern>
</Entity>
```
### <a name="keywords"></a><span data-ttu-id="64f1e-1553">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-1553">Keywords</span></span>

- <span data-ttu-id="64f1e-1554">Numéro d'identité personnelle tchèque</span><span class="sxs-lookup"><span data-stu-id="64f1e-1554">czech personal identity number</span></span>
- <span data-ttu-id="64f1e-1555">Rodné číslo</span><span class="sxs-lookup"><span data-stu-id="64f1e-1555">Rodné číslo</span></span>
   
## <a name="denmark-personal-identification-number"></a><span data-ttu-id="64f1e-1556">	Numéro d’identification personnel Danemark</span><span class="sxs-lookup"><span data-stu-id="64f1e-1556">Denmark Personal Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-1557">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-1557">Format</span></span>

<span data-ttu-id="64f1e-1558">10 chiffres contenant un trait d’union</span><span class="sxs-lookup"><span data-stu-id="64f1e-1558">10 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-1559">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-1559">Pattern</span></span>

<span data-ttu-id="64f1e-1560">10 chiffres :</span><span class="sxs-lookup"><span data-stu-id="64f1e-1560">10 digits:</span></span>
- <span data-ttu-id="64f1e-1561">Six chiffres au format JJMMAA qui correspondent à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="64f1e-1561">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="64f1e-1562">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="64f1e-1562">A hyphen</span></span> 
- <span data-ttu-id="64f1e-1563">Quatre chiffres où le dernier chiffre est un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-1563">Four digits where the final digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-1564">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-1564">Checksum</span></span>

<span data-ttu-id="64f1e-1565">Oui</span><span class="sxs-lookup"><span data-stu-id="64f1e-1565">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-1566">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-1566">Definition</span></span>

<span data-ttu-id="64f1e-1567">Une stratégie DLP est sûre à 75% d'avoir détecté ce type d'informations sensibles si, dans une proximité de 300 caractères: l'expression régulière Regex_denmark_id trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1567">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_denmark_id finds content that matches the pattern.</span></span>
<span data-ttu-id="64f1e-1568">Un mot clé figurant dans la liste Keyword_denmark_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1568">A keyword from Keyword_denmark_id is found.</span></span>
<span data-ttu-id="64f1e-1569">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1569">The checksum passes.</span></span>

```
<!-- Denmark Personal Identification Number -->
<Entity id="6c4f2fef-56e1-4c00-8093-88d7a01cf460" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_denmark_id"/>
     <Match idRef="Keyword_denmark_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-1570">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-1570">Keywords</span></span>

#### <a name="keyworddenmarkid"></a><span data-ttu-id="64f1e-1571">Keyword_denmark_id</span><span class="sxs-lookup"><span data-stu-id="64f1e-1571">Keyword_denmark_id</span></span>

- <span data-ttu-id="64f1e-1572">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="64f1e-1572">Personal Identification Number</span></span>
- <span data-ttu-id="64f1e-1573">CARDIO</span><span class="sxs-lookup"><span data-stu-id="64f1e-1573">CPR</span></span>
- <span data-ttu-id="64f1e-1574">Det Centrale Personregister</span><span class="sxs-lookup"><span data-stu-id="64f1e-1574">Det Centrale Personregister</span></span>
- <span data-ttu-id="64f1e-1575">Personnummer</span><span class="sxs-lookup"><span data-stu-id="64f1e-1575">Personnummer</span></span>
   
## <a name="drug-enforcement-agency-dea-number"></a><span data-ttu-id="64f1e-1576">Numéro de la Drug Enforcement Agency (DEA)</span><span class="sxs-lookup"><span data-stu-id="64f1e-1576">Drug Enforcement Agency (DEA) Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-1577">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-1577">Format</span></span>

<span data-ttu-id="64f1e-1578">Deux lettres suivies de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-1578">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-1579">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-1579">Pattern</span></span>

<span data-ttu-id="64f1e-1580">Le modèle doit inclure tous les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="64f1e-1580">Pattern must include all of the following:</span></span>
- <span data-ttu-id="64f1e-1581">Une lettre (ne respecte pas la casse) à partir de cet ensemble de lettres possibles : abcdefghjklmnprstux, qui est un code d’utilisateur enregistré</span><span class="sxs-lookup"><span data-stu-id="64f1e-1581">One letter (not case sensitive) from this set of possible letters: abcdefghjklmnprstux, which is a registrant code</span></span> 
- <span data-ttu-id="64f1e-1582">Une lettre (ne respecte pas la casse), qui est la première lettre du nom de l’utilisateur enregistré</span><span class="sxs-lookup"><span data-stu-id="64f1e-1582">One letter (not case sensitive), which is the first letter of the registrant's last name</span></span> 
- <span data-ttu-id="64f1e-1583">Sept chiffres, le dernier est le chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-1583">Seven digits, the last of which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-1584">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-1584">Checksum</span></span>

<span data-ttu-id="64f1e-1585">Oui</span><span class="sxs-lookup"><span data-stu-id="64f1e-1585">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-1586">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-1586">Definition</span></span>

<span data-ttu-id="64f1e-1587">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-1587">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-1588">La fonction Func_dea_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1588">The function Func_dea_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-1589">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1589">The checksum passes.</span></span>

```
<!-- DEA Number -->
<Entity id="9a5445ad-406e-43eb-8bd7-cac17ab6d0e4" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_dea_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-1590">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-1590">Keywords</span></span>

<span data-ttu-id="64f1e-1591">Aucun</span><span class="sxs-lookup"><span data-stu-id="64f1e-1591">None</span></span>

   
## <a name="eu-debit-card-number"></a><span data-ttu-id="64f1e-1592">Numéro de carte de débit Union européenne</span><span class="sxs-lookup"><span data-stu-id="64f1e-1592">EU Debit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-1593">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-1593">Format</span></span>

<span data-ttu-id="64f1e-1594">16 chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-1594">16 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-1595">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-1595">Pattern</span></span>

<span data-ttu-id="64f1e-1596">Modèle très complexe et puissant</span><span class="sxs-lookup"><span data-stu-id="64f1e-1596">Very complex and robust pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-1597">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-1597">Checksum</span></span>

<span data-ttu-id="64f1e-1598">Oui</span><span class="sxs-lookup"><span data-stu-id="64f1e-1598">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-1599">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-1599">Definition</span></span>

<span data-ttu-id="64f1e-1600">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-1600">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-1601">La fonction Func_eu_debit_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1601">The function Func_eu_debit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-1602">Au moins une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="64f1e-1602">At least one of the following is true:</span></span>
    - <span data-ttu-id="64f1e-1603">Un mot clé figurant dans la liste Keyword_eu_debit_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1603">A keyword from Keyword_eu_debit_card is found.</span></span>
    - <span data-ttu-id="64f1e-1604">Un mot clé figurant dans la liste Keyword_card_terms_dict est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1604">A keyword from Keyword_card_terms_dict is found.</span></span>
    - <span data-ttu-id="64f1e-1605">Un mot clé figurant dans la liste Keyword_card_security_terms_dict est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1605">A keyword from Keyword_card_security_terms_dict is found.</span></span>
    - <span data-ttu-id="64f1e-1606">Un mot clé figurant dans la liste Keyword_card_expiration_terms_dict est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1606">A keyword from Keyword_card_expiration_terms_dict is found.</span></span>
    - <span data-ttu-id="64f1e-1607">La fonction Func_expiration_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1607">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="64f1e-1608">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1608">The checksum passes.</span></span>

```
    <!-- EU Debit Card Number -->
    <Entity id="0e9b3178-9678-47dd-a509-37222ca96b42" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_eu_debit_card" />
        <Any minMatches="1">
          <Match idRef="Keyword_eu_debit_card" />
          <Match idRef="Keyword_card_terms_dict" />
          <Match idRef="Keyword_card_security_terms_dict" />
          <Match idRef="Keyword_card_expiration_terms_dict" />
          <Match idRef="Func_expiration_date" />
        </Any>
      </Pattern>
    </Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-1609">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-1609">Keywords</span></span>

#### <a name="keywordeudebitcard"></a><span data-ttu-id="64f1e-1610">Keyword_eu_debit_card</span><span class="sxs-lookup"><span data-stu-id="64f1e-1610">Keyword_eu_debit_card</span></span>

- <span data-ttu-id="64f1e-1611">numéro de compte</span><span class="sxs-lookup"><span data-stu-id="64f1e-1611">account number</span></span> 
- <span data-ttu-id="64f1e-1612">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="64f1e-1612">card number</span></span> 
- <span data-ttu-id="64f1e-1613">n° carte</span><span class="sxs-lookup"><span data-stu-id="64f1e-1613">card no.</span></span> 
- <span data-ttu-id="64f1e-1614">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="64f1e-1614">security number</span></span> 
- <span data-ttu-id="64f1e-1615">CC</span><span class="sxs-lookup"><span data-stu-id="64f1e-1615">cc#</span></span> 

#### <a name="keywordcardtermsdict"></a><span data-ttu-id="64f1e-1616">Keyword_card_terms_dict</span><span class="sxs-lookup"><span data-stu-id="64f1e-1616">Keyword_card_terms_dict</span></span>

- <span data-ttu-id="64f1e-1617">num de compte</span><span class="sxs-lookup"><span data-stu-id="64f1e-1617">acct nbr</span></span> 
- <span data-ttu-id="64f1e-1618">num de compte</span><span class="sxs-lookup"><span data-stu-id="64f1e-1618">acct num</span></span> 
- <span data-ttu-id="64f1e-1619">n° compte</span><span class="sxs-lookup"><span data-stu-id="64f1e-1619">acct no</span></span> 
- <span data-ttu-id="64f1e-1620">american express</span><span class="sxs-lookup"><span data-stu-id="64f1e-1620">american express</span></span> 
- <span data-ttu-id="64f1e-1621">AmericanExpress</span><span class="sxs-lookup"><span data-stu-id="64f1e-1621">americanexpress</span></span> 
- <span data-ttu-id="64f1e-1622">americano espresso</span><span class="sxs-lookup"><span data-stu-id="64f1e-1622">americano espresso</span></span> 
- <span data-ttu-id="64f1e-1623">American</span><span class="sxs-lookup"><span data-stu-id="64f1e-1623">amex</span></span> 
- <span data-ttu-id="64f1e-1624">carte de retrait</span><span class="sxs-lookup"><span data-stu-id="64f1e-1624">atm card</span></span> 
- <span data-ttu-id="64f1e-1625">cartes de retrait</span><span class="sxs-lookup"><span data-stu-id="64f1e-1625">atm cards</span></span> 
- <span data-ttu-id="64f1e-1626">atm kaart</span><span class="sxs-lookup"><span data-stu-id="64f1e-1626">atm kaart</span></span> 
- <span data-ttu-id="64f1e-1627">retrait</span><span class="sxs-lookup"><span data-stu-id="64f1e-1627">atmcard</span></span> 
- <span data-ttu-id="64f1e-1628">retrait</span><span class="sxs-lookup"><span data-stu-id="64f1e-1628">atmcards</span></span> 
- <span data-ttu-id="64f1e-1629">atmkaart</span><span class="sxs-lookup"><span data-stu-id="64f1e-1629">atmkaart</span></span> 
- <span data-ttu-id="64f1e-1630">atmkaarten</span><span class="sxs-lookup"><span data-stu-id="64f1e-1630">atmkaarten</span></span> 
- <span data-ttu-id="64f1e-1631">Bancontact</span><span class="sxs-lookup"><span data-stu-id="64f1e-1631">bancontact</span></span> 
- <span data-ttu-id="64f1e-1632">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="64f1e-1632">bank card</span></span> 
- <span data-ttu-id="64f1e-1633">bankkaart</span><span class="sxs-lookup"><span data-stu-id="64f1e-1633">bankkaart</span></span> 
- <span data-ttu-id="64f1e-1634">titulaire de la carte</span><span class="sxs-lookup"><span data-stu-id="64f1e-1634">card holder</span></span> 
- <span data-ttu-id="64f1e-1635">titulaires de la carte</span><span class="sxs-lookup"><span data-stu-id="64f1e-1635">card holders</span></span> 
- <span data-ttu-id="64f1e-1636">num de carte</span><span class="sxs-lookup"><span data-stu-id="64f1e-1636">card num</span></span> 
- <span data-ttu-id="64f1e-1637">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="64f1e-1637">card number</span></span> 
- <span data-ttu-id="64f1e-1638">numéros de carte</span><span class="sxs-lookup"><span data-stu-id="64f1e-1638">card numbers</span></span> 
- <span data-ttu-id="64f1e-1639">type de carte</span><span class="sxs-lookup"><span data-stu-id="64f1e-1639">card type</span></span> 
- <span data-ttu-id="64f1e-1640">cardano numerico</span><span class="sxs-lookup"><span data-stu-id="64f1e-1640">cardano numerico</span></span> 
- <span data-ttu-id="64f1e-1641">titulaires</span><span class="sxs-lookup"><span data-stu-id="64f1e-1641">cardholder</span></span> 
- <span data-ttu-id="64f1e-1642">titulaires</span><span class="sxs-lookup"><span data-stu-id="64f1e-1642">cardholders</span></span> 
- <span data-ttu-id="64f1e-1643">carte</span><span class="sxs-lookup"><span data-stu-id="64f1e-1643">cardnumber</span></span> 
- <span data-ttu-id="64f1e-1644">carte</span><span class="sxs-lookup"><span data-stu-id="64f1e-1644">cardnumbers</span></span> 
- <span data-ttu-id="64f1e-1645">carta bianca</span><span class="sxs-lookup"><span data-stu-id="64f1e-1645">carta bianca</span></span> 
- <span data-ttu-id="64f1e-1646">Carta credito</span><span class="sxs-lookup"><span data-stu-id="64f1e-1646">carta credito</span></span> 
- <span data-ttu-id="64f1e-1647">Carta di credito</span><span class="sxs-lookup"><span data-stu-id="64f1e-1647">carta di credito</span></span> 
- <span data-ttu-id="64f1e-1648">cartao de credito</span><span class="sxs-lookup"><span data-stu-id="64f1e-1648">cartao de credito</span></span> 
- <span data-ttu-id="64f1e-1649">cartao de crédito</span><span class="sxs-lookup"><span data-stu-id="64f1e-1649">cartao de crédito</span></span> 
- <span data-ttu-id="64f1e-1650">cartao de debito</span><span class="sxs-lookup"><span data-stu-id="64f1e-1650">cartao de debito</span></span> 
- <span data-ttu-id="64f1e-1651">cartao de débito</span><span class="sxs-lookup"><span data-stu-id="64f1e-1651">cartao de débito</span></span> 
- <span data-ttu-id="64f1e-1652">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="64f1e-1652">carte bancaire</span></span> 
- <span data-ttu-id="64f1e-1653">carte blanche</span><span class="sxs-lookup"><span data-stu-id="64f1e-1653">carte blanche</span></span> 
- <span data-ttu-id="64f1e-1654">carte bleue</span><span class="sxs-lookup"><span data-stu-id="64f1e-1654">carte bleue</span></span> 
- <span data-ttu-id="64f1e-1655">carte de credit</span><span class="sxs-lookup"><span data-stu-id="64f1e-1655">carte de credit</span></span> 
- <span data-ttu-id="64f1e-1656">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="64f1e-1656">carte de crédit</span></span> 
- <span data-ttu-id="64f1e-1657">carte di credito</span><span class="sxs-lookup"><span data-stu-id="64f1e-1657">carte di credito</span></span> 
- <span data-ttu-id="64f1e-1658">carteblanche</span><span class="sxs-lookup"><span data-stu-id="64f1e-1658">carteblanche</span></span> 
- <span data-ttu-id="64f1e-1659">cartão de credito</span><span class="sxs-lookup"><span data-stu-id="64f1e-1659">cartão de credito</span></span> 
- <span data-ttu-id="64f1e-1660">cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="64f1e-1660">cartão de crédito</span></span> 
- <span data-ttu-id="64f1e-1661">cartão de debito</span><span class="sxs-lookup"><span data-stu-id="64f1e-1661">cartão de debito</span></span> 
- <span data-ttu-id="64f1e-1662">cartão de débito</span><span class="sxs-lookup"><span data-stu-id="64f1e-1662">cartão de débito</span></span> 
- <span data-ttu-id="64f1e-1663">cb</span><span class="sxs-lookup"><span data-stu-id="64f1e-1663">cb</span></span> 
- <span data-ttu-id="64f1e-1664">CCN</span><span class="sxs-lookup"><span data-stu-id="64f1e-1664">ccn</span></span> 
- <span data-ttu-id="64f1e-1665">carte de vérification</span><span class="sxs-lookup"><span data-stu-id="64f1e-1665">check card</span></span> 
- <span data-ttu-id="64f1e-1666">cartes de vérification</span><span class="sxs-lookup"><span data-stu-id="64f1e-1666">check cards</span></span> 
- <span data-ttu-id="64f1e-1667">carte</span><span class="sxs-lookup"><span data-stu-id="64f1e-1667">checkcard</span></span>
- <span data-ttu-id="64f1e-1668">cartes</span><span class="sxs-lookup"><span data-stu-id="64f1e-1668">checkcards</span></span> 
- <span data-ttu-id="64f1e-1669">chequekaart</span><span class="sxs-lookup"><span data-stu-id="64f1e-1669">chequekaart</span></span> 
- <span data-ttu-id="64f1e-1670">Cirrus</span><span class="sxs-lookup"><span data-stu-id="64f1e-1670">cirrus</span></span> 
- <span data-ttu-id="64f1e-1671">Cirrus-EDC-Maestro</span><span class="sxs-lookup"><span data-stu-id="64f1e-1671">cirrus-edc-maestro</span></span> 
- <span data-ttu-id="64f1e-1672">controlekaart</span><span class="sxs-lookup"><span data-stu-id="64f1e-1672">controlekaart</span></span> 
- <span data-ttu-id="64f1e-1673">controlekaarten</span><span class="sxs-lookup"><span data-stu-id="64f1e-1673">controlekaarten</span></span> 
- <span data-ttu-id="64f1e-1674">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="64f1e-1674">credit card</span></span> 
- <span data-ttu-id="64f1e-1675">cartes de crédit</span><span class="sxs-lookup"><span data-stu-id="64f1e-1675">credit cards</span></span> 
- <span data-ttu-id="64f1e-1676">CreditCard</span><span class="sxs-lookup"><span data-stu-id="64f1e-1676">creditcard</span></span> 
- <span data-ttu-id="64f1e-1677">crédit</span><span class="sxs-lookup"><span data-stu-id="64f1e-1677">creditcards</span></span> 
- <span data-ttu-id="64f1e-1678">debetkaart</span><span class="sxs-lookup"><span data-stu-id="64f1e-1678">debetkaart</span></span> 
- <span data-ttu-id="64f1e-1679">debetkaarten</span><span class="sxs-lookup"><span data-stu-id="64f1e-1679">debetkaarten</span></span> 
- <span data-ttu-id="64f1e-1680">carte de débit</span><span class="sxs-lookup"><span data-stu-id="64f1e-1680">debit card</span></span> 
- <span data-ttu-id="64f1e-1681">cartes de débit</span><span class="sxs-lookup"><span data-stu-id="64f1e-1681">debit cards</span></span> 
- <span data-ttu-id="64f1e-1682">débit</span><span class="sxs-lookup"><span data-stu-id="64f1e-1682">debitcard</span></span> 
- <span data-ttu-id="64f1e-1683">débit</span><span class="sxs-lookup"><span data-stu-id="64f1e-1683">debitcards</span></span> 
- <span data-ttu-id="64f1e-1684">debito automatico</span><span class="sxs-lookup"><span data-stu-id="64f1e-1684">debito automatico</span></span> 
- <span data-ttu-id="64f1e-1685">diners club</span><span class="sxs-lookup"><span data-stu-id="64f1e-1685">diners club</span></span> 
- <span data-ttu-id="64f1e-1686">DinersClub</span><span class="sxs-lookup"><span data-stu-id="64f1e-1686">dinersclub</span></span> 
- <span data-ttu-id="64f1e-1687">connaissance</span><span class="sxs-lookup"><span data-stu-id="64f1e-1687">discover</span></span> 
- <span data-ttu-id="64f1e-1688">discover card</span><span class="sxs-lookup"><span data-stu-id="64f1e-1688">discover card</span></span> 
- <span data-ttu-id="64f1e-1689">discover cards</span><span class="sxs-lookup"><span data-stu-id="64f1e-1689">discover cards</span></span> 
- <span data-ttu-id="64f1e-1690">discovercard</span><span class="sxs-lookup"><span data-stu-id="64f1e-1690">discovercard</span></span> 
- <span data-ttu-id="64f1e-1691">discovercards</span><span class="sxs-lookup"><span data-stu-id="64f1e-1691">discovercards</span></span> 
- <span data-ttu-id="64f1e-1692">débito automático</span><span class="sxs-lookup"><span data-stu-id="64f1e-1692">débito automático</span></span>
- <span data-ttu-id="64f1e-1693">EDC</span><span class="sxs-lookup"><span data-stu-id="64f1e-1693">edc</span></span> 
- <span data-ttu-id="64f1e-1694">eigentümername</span><span class="sxs-lookup"><span data-stu-id="64f1e-1694">eigentümername</span></span> 
- <span data-ttu-id="64f1e-1695">carte de crédit européenne</span><span class="sxs-lookup"><span data-stu-id="64f1e-1695">european debit card</span></span> 
- <span data-ttu-id="64f1e-1696">hoofdkaart</span><span class="sxs-lookup"><span data-stu-id="64f1e-1696">hoofdkaart</span></span> 
- <span data-ttu-id="64f1e-1697">hoofdkaarten</span><span class="sxs-lookup"><span data-stu-id="64f1e-1697">hoofdkaarten</span></span> 
- <span data-ttu-id="64f1e-1698">in viaggio</span><span class="sxs-lookup"><span data-stu-id="64f1e-1698">in viaggio</span></span> 
- <span data-ttu-id="64f1e-1699">japanese card bureau</span><span class="sxs-lookup"><span data-stu-id="64f1e-1699">japanese card bureau</span></span> 
- <span data-ttu-id="64f1e-1700">japanse kaartdienst</span><span class="sxs-lookup"><span data-stu-id="64f1e-1700">japanse kaartdienst</span></span> 
- <span data-ttu-id="64f1e-1701">JCB</span><span class="sxs-lookup"><span data-stu-id="64f1e-1701">jcb</span></span> 
- <span data-ttu-id="64f1e-1702">Kaart</span><span class="sxs-lookup"><span data-stu-id="64f1e-1702">kaart</span></span> 
- <span data-ttu-id="64f1e-1703">kaart num</span><span class="sxs-lookup"><span data-stu-id="64f1e-1703">kaart num</span></span> 
- <span data-ttu-id="64f1e-1704">kaartaantal</span><span class="sxs-lookup"><span data-stu-id="64f1e-1704">kaartaantal</span></span> 
- <span data-ttu-id="64f1e-1705">kaartaantallen</span><span class="sxs-lookup"><span data-stu-id="64f1e-1705">kaartaantallen</span></span> 
- <span data-ttu-id="64f1e-1706">kaarthouder</span><span class="sxs-lookup"><span data-stu-id="64f1e-1706">kaarthouder</span></span> 
- <span data-ttu-id="64f1e-1707">kaarthouders</span><span class="sxs-lookup"><span data-stu-id="64f1e-1707">kaarthouders</span></span> 
- <span data-ttu-id="64f1e-1708">Karte</span><span class="sxs-lookup"><span data-stu-id="64f1e-1708">karte</span></span>  
- <span data-ttu-id="64f1e-1709">karteninhaber</span><span class="sxs-lookup"><span data-stu-id="64f1e-1709">karteninhaber</span></span> 
- <span data-ttu-id="64f1e-1710">karteninhabers</span><span class="sxs-lookup"><span data-stu-id="64f1e-1710">karteninhabers</span></span>
- <span data-ttu-id="64f1e-1711">kartennr</span><span class="sxs-lookup"><span data-stu-id="64f1e-1711">kartennr</span></span> 
- <span data-ttu-id="64f1e-1712">kartennummer</span><span class="sxs-lookup"><span data-stu-id="64f1e-1712">kartennummer</span></span> 
- <span data-ttu-id="64f1e-1713">Kreditkarte</span><span class="sxs-lookup"><span data-stu-id="64f1e-1713">kreditkarte</span></span> 
- <span data-ttu-id="64f1e-1714">Kreditkarten-Nummer</span><span class="sxs-lookup"><span data-stu-id="64f1e-1714">kreditkarten-nummer</span></span> 
- <span data-ttu-id="64f1e-1715">kreditkarteninhaber</span><span class="sxs-lookup"><span data-stu-id="64f1e-1715">kreditkarteninhaber</span></span> 
- <span data-ttu-id="64f1e-1716">kreditkarteninstitut</span><span class="sxs-lookup"><span data-stu-id="64f1e-1716">kreditkarteninstitut</span></span> 
- <span data-ttu-id="64f1e-1717">Kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="64f1e-1717">kreditkartennummer</span></span> 
- <span data-ttu-id="64f1e-1718">kreditkartentyp</span><span class="sxs-lookup"><span data-stu-id="64f1e-1718">kreditkartentyp</span></span> 
- <span data-ttu-id="64f1e-1719">sonne</span><span class="sxs-lookup"><span data-stu-id="64f1e-1719">maestro</span></span> 
- <span data-ttu-id="64f1e-1720">master card</span><span class="sxs-lookup"><span data-stu-id="64f1e-1720">master card</span></span> 
- <span data-ttu-id="64f1e-1721">master cards</span><span class="sxs-lookup"><span data-stu-id="64f1e-1721">master cards</span></span> 
- <span data-ttu-id="64f1e-1722">MasterCard</span><span class="sxs-lookup"><span data-stu-id="64f1e-1722">mastercard</span></span> 
- <span data-ttu-id="64f1e-1723">MasterCard</span><span class="sxs-lookup"><span data-stu-id="64f1e-1723">mastercards</span></span> 
- <span data-ttu-id="64f1e-1724">McDonald</span><span class="sxs-lookup"><span data-stu-id="64f1e-1724">mc</span></span> 
- <span data-ttu-id="64f1e-1725">mister cash</span><span class="sxs-lookup"><span data-stu-id="64f1e-1725">mister cash</span></span> 
- <span data-ttu-id="64f1e-1726">n carta</span><span class="sxs-lookup"><span data-stu-id="64f1e-1726">n carta</span></span> 
- <span data-ttu-id="64f1e-1727">Carta</span><span class="sxs-lookup"><span data-stu-id="64f1e-1727">carta</span></span> 
- <span data-ttu-id="64f1e-1728">no de tarjeta</span><span class="sxs-lookup"><span data-stu-id="64f1e-1728">no de tarjeta</span></span> 
- <span data-ttu-id="64f1e-1729">no do cartao</span><span class="sxs-lookup"><span data-stu-id="64f1e-1729">no do cartao</span></span> 
- <span data-ttu-id="64f1e-1730">no do cartão</span><span class="sxs-lookup"><span data-stu-id="64f1e-1730">no do cartão</span></span> 
- <span data-ttu-id="64f1e-1731">Nbre.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1731">no.</span></span> <span data-ttu-id="64f1e-1732">de tarjeta</span><span class="sxs-lookup"><span data-stu-id="64f1e-1732">de tarjeta</span></span> 
- <span data-ttu-id="64f1e-1733">Nbre.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1733">no.</span></span> <span data-ttu-id="64f1e-1734">do cartao</span><span class="sxs-lookup"><span data-stu-id="64f1e-1734">do cartao</span></span> 
- <span data-ttu-id="64f1e-1735">Nbre.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1735">no.</span></span> <span data-ttu-id="64f1e-1736">do cartão</span><span class="sxs-lookup"><span data-stu-id="64f1e-1736">do cartão</span></span> 
- <span data-ttu-id="64f1e-1737">nr carta</span><span class="sxs-lookup"><span data-stu-id="64f1e-1737">nr carta</span></span> 
- <span data-ttu-id="64f1e-1738">Nr.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1738">nr.</span></span> <span data-ttu-id="64f1e-1739">Carta</span><span class="sxs-lookup"><span data-stu-id="64f1e-1739">carta</span></span> 
- <span data-ttu-id="64f1e-1740">numeri di scheda</span><span class="sxs-lookup"><span data-stu-id="64f1e-1740">numeri di scheda</span></span> 
- <span data-ttu-id="64f1e-1741">numero carta</span><span class="sxs-lookup"><span data-stu-id="64f1e-1741">numero carta</span></span> 
- <span data-ttu-id="64f1e-1742">numero de cartao</span><span class="sxs-lookup"><span data-stu-id="64f1e-1742">numero de cartao</span></span> 
- <span data-ttu-id="64f1e-1743">numero de carte</span><span class="sxs-lookup"><span data-stu-id="64f1e-1743">numero de carte</span></span> 
- <span data-ttu-id="64f1e-1744">numero de cartão</span><span class="sxs-lookup"><span data-stu-id="64f1e-1744">numero de cartão</span></span> 
- <span data-ttu-id="64f1e-1745">numero de tarjeta</span><span class="sxs-lookup"><span data-stu-id="64f1e-1745">numero de tarjeta</span></span>
- <span data-ttu-id="64f1e-1746">numero della carta</span><span class="sxs-lookup"><span data-stu-id="64f1e-1746">numero della carta</span></span> 
- <span data-ttu-id="64f1e-1747">numero di carta</span><span class="sxs-lookup"><span data-stu-id="64f1e-1747">numero di carta</span></span> 
- <span data-ttu-id="64f1e-1748">numero di scheda</span><span class="sxs-lookup"><span data-stu-id="64f1e-1748">numero di scheda</span></span> 
- <span data-ttu-id="64f1e-1749">numero do cartao</span><span class="sxs-lookup"><span data-stu-id="64f1e-1749">numero do cartao</span></span> 
- <span data-ttu-id="64f1e-1750">numero do cartão</span><span class="sxs-lookup"><span data-stu-id="64f1e-1750">numero do cartão</span></span> 
- <span data-ttu-id="64f1e-1751">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="64f1e-1751">numéro de carte</span></span> 
- <span data-ttu-id="64f1e-1752">nº carta</span><span class="sxs-lookup"><span data-stu-id="64f1e-1752">nº carta</span></span> 
- <span data-ttu-id="64f1e-1753">nº de carte</span><span class="sxs-lookup"><span data-stu-id="64f1e-1753">nº de carte</span></span> 
- <span data-ttu-id="64f1e-1754">nº de la carte</span><span class="sxs-lookup"><span data-stu-id="64f1e-1754">nº de la carte</span></span> 
- <span data-ttu-id="64f1e-1755">nº de tarjeta</span><span class="sxs-lookup"><span data-stu-id="64f1e-1755">nº de tarjeta</span></span> 
- <span data-ttu-id="64f1e-1756">nº do cartao</span><span class="sxs-lookup"><span data-stu-id="64f1e-1756">nº do cartao</span></span> 
- <span data-ttu-id="64f1e-1757">nº do cartão</span><span class="sxs-lookup"><span data-stu-id="64f1e-1757">nº do cartão</span></span> 
- <span data-ttu-id="64f1e-1758">n º.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1758">nº.</span></span> <span data-ttu-id="64f1e-1759">do cartão</span><span class="sxs-lookup"><span data-stu-id="64f1e-1759">do cartão</span></span> 
- <span data-ttu-id="64f1e-1760">número de cartao</span><span class="sxs-lookup"><span data-stu-id="64f1e-1760">número de cartao</span></span> 
- <span data-ttu-id="64f1e-1761">número de cartão</span><span class="sxs-lookup"><span data-stu-id="64f1e-1761">número de cartão</span></span> 
- <span data-ttu-id="64f1e-1762">número de tarjeta</span><span class="sxs-lookup"><span data-stu-id="64f1e-1762">número de tarjeta</span></span> 
- <span data-ttu-id="64f1e-1763">número do cartao</span><span class="sxs-lookup"><span data-stu-id="64f1e-1763">número do cartao</span></span> 
- <span data-ttu-id="64f1e-1764">scheda dell’assegno</span><span class="sxs-lookup"><span data-stu-id="64f1e-1764">scheda dell'assegno</span></span> 
- <span data-ttu-id="64f1e-1765">scheda dell’atmosfera</span><span class="sxs-lookup"><span data-stu-id="64f1e-1765">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="64f1e-1766">scheda dell’atmosfera</span><span class="sxs-lookup"><span data-stu-id="64f1e-1766">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="64f1e-1767">scheda della banca</span><span class="sxs-lookup"><span data-stu-id="64f1e-1767">scheda della banca</span></span> 
- <span data-ttu-id="64f1e-1768">scheda di controllo</span><span class="sxs-lookup"><span data-stu-id="64f1e-1768">scheda di controllo</span></span> 
- <span data-ttu-id="64f1e-1769">scheda di debito</span><span class="sxs-lookup"><span data-stu-id="64f1e-1769">scheda di debito</span></span> 
- <span data-ttu-id="64f1e-1770">scheda matrice</span><span class="sxs-lookup"><span data-stu-id="64f1e-1770">scheda matrice</span></span> 
- <span data-ttu-id="64f1e-1771">schede dell’atmosfera</span><span class="sxs-lookup"><span data-stu-id="64f1e-1771">schede dell'atmosfera</span></span> 
- <span data-ttu-id="64f1e-1772">schede di controllo</span><span class="sxs-lookup"><span data-stu-id="64f1e-1772">schede di controllo</span></span> 
- <span data-ttu-id="64f1e-1773">schede di debito</span><span class="sxs-lookup"><span data-stu-id="64f1e-1773">schede di debito</span></span> 
- <span data-ttu-id="64f1e-1774">schede matrici</span><span class="sxs-lookup"><span data-stu-id="64f1e-1774">schede matrici</span></span> 
- <span data-ttu-id="64f1e-1775">scoprono la scheda</span><span class="sxs-lookup"><span data-stu-id="64f1e-1775">scoprono la scheda</span></span> 
- <span data-ttu-id="64f1e-1776">scoprono le schede</span><span class="sxs-lookup"><span data-stu-id="64f1e-1776">scoprono le schede</span></span> 
- <span data-ttu-id="64f1e-1777">tracteur</span><span class="sxs-lookup"><span data-stu-id="64f1e-1777">solo</span></span> 
- <span data-ttu-id="64f1e-1778">supporti di scheda</span><span class="sxs-lookup"><span data-stu-id="64f1e-1778">supporti di scheda</span></span> 
- <span data-ttu-id="64f1e-1779">supporto di scheda</span><span class="sxs-lookup"><span data-stu-id="64f1e-1779">supporto di scheda</span></span> 
- <span data-ttu-id="64f1e-1780">accéder</span><span class="sxs-lookup"><span data-stu-id="64f1e-1780">switch</span></span> 
- <span data-ttu-id="64f1e-1781">tarjeta atm</span><span class="sxs-lookup"><span data-stu-id="64f1e-1781">tarjeta atm</span></span> 
- <span data-ttu-id="64f1e-1782">tarjeta credito</span><span class="sxs-lookup"><span data-stu-id="64f1e-1782">tarjeta credito</span></span> 
- <span data-ttu-id="64f1e-1783">tarjeta de atm</span><span class="sxs-lookup"><span data-stu-id="64f1e-1783">tarjeta de atm</span></span> 
- <span data-ttu-id="64f1e-1784">tarjeta de credito</span><span class="sxs-lookup"><span data-stu-id="64f1e-1784">tarjeta de credito</span></span> 
- <span data-ttu-id="64f1e-1785">tarjeta de debito</span><span class="sxs-lookup"><span data-stu-id="64f1e-1785">tarjeta de debito</span></span> 
- <span data-ttu-id="64f1e-1786">tarjeta debito</span><span class="sxs-lookup"><span data-stu-id="64f1e-1786">tarjeta debito</span></span> 
- <span data-ttu-id="64f1e-1787">tarjeta no</span><span class="sxs-lookup"><span data-stu-id="64f1e-1787">tarjeta no</span></span>
- <span data-ttu-id="64f1e-1788">tarjetahabiente</span><span class="sxs-lookup"><span data-stu-id="64f1e-1788">tarjetahabiente</span></span> 
- <span data-ttu-id="64f1e-1789">tipo della scheda</span><span class="sxs-lookup"><span data-stu-id="64f1e-1789">tipo della scheda</span></span> 
- <span data-ttu-id="64f1e-1790">ufficio giapponese della</span><span class="sxs-lookup"><span data-stu-id="64f1e-1790">ufficio giapponese della</span></span> 
- <span data-ttu-id="64f1e-1791">scheda</span><span class="sxs-lookup"><span data-stu-id="64f1e-1791">scheda</span></span> 
- <span data-ttu-id="64f1e-1792">v pay</span><span class="sxs-lookup"><span data-stu-id="64f1e-1792">v pay</span></span> 
- <span data-ttu-id="64f1e-1793">v-Pay</span><span class="sxs-lookup"><span data-stu-id="64f1e-1793">v-pay</span></span> 
- <span data-ttu-id="64f1e-1794">délivrance</span><span class="sxs-lookup"><span data-stu-id="64f1e-1794">visa</span></span> 
- <span data-ttu-id="64f1e-1795">visa plus</span><span class="sxs-lookup"><span data-stu-id="64f1e-1795">visa plus</span></span> 
- <span data-ttu-id="64f1e-1796">visa electron</span><span class="sxs-lookup"><span data-stu-id="64f1e-1796">visa electron</span></span> 
- <span data-ttu-id="64f1e-1797">visto</span><span class="sxs-lookup"><span data-stu-id="64f1e-1797">visto</span></span> 
- <span data-ttu-id="64f1e-1798">visum</span><span class="sxs-lookup"><span data-stu-id="64f1e-1798">visum</span></span> 
- <span data-ttu-id="64f1e-1799">vpay</span><span class="sxs-lookup"><span data-stu-id="64f1e-1799">vpay</span></span>   

#### <a name="keywordcardsecuritytermsdict"></a><span data-ttu-id="64f1e-1800">Keyword_card_security_terms_dict</span><span class="sxs-lookup"><span data-stu-id="64f1e-1800">Keyword_card_security_terms_dict</span></span>

- <span data-ttu-id="64f1e-1801">numéro d’identification de la carte</span><span class="sxs-lookup"><span data-stu-id="64f1e-1801">card identification number</span></span>
- <span data-ttu-id="64f1e-1802">vérification de la carte</span><span class="sxs-lookup"><span data-stu-id="64f1e-1802">card verification</span></span> 
- <span data-ttu-id="64f1e-1803">cardi la verifica</span><span class="sxs-lookup"><span data-stu-id="64f1e-1803">cardi la verifica</span></span> 
- <span data-ttu-id="64f1e-1804">nic</span><span class="sxs-lookup"><span data-stu-id="64f1e-1804">cid</span></span> 
- <span data-ttu-id="64f1e-1805">cod seg</span><span class="sxs-lookup"><span data-stu-id="64f1e-1805">cod seg</span></span> 
- <span data-ttu-id="64f1e-1806">cod seguranca</span><span class="sxs-lookup"><span data-stu-id="64f1e-1806">cod seguranca</span></span> 
- <span data-ttu-id="64f1e-1807">cod segurança</span><span class="sxs-lookup"><span data-stu-id="64f1e-1807">cod segurança</span></span> 
- <span data-ttu-id="64f1e-1808">cod sicurezza</span><span class="sxs-lookup"><span data-stu-id="64f1e-1808">cod sicurezza</span></span> 
- <span data-ttu-id="64f1e-1809">contre.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1809">cod.</span></span> <span data-ttu-id="64f1e-1810">SEG</span><span class="sxs-lookup"><span data-stu-id="64f1e-1810">seg</span></span> 
- <span data-ttu-id="64f1e-1811">contre.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1811">cod.</span></span> <span data-ttu-id="64f1e-1812">Seguranca</span><span class="sxs-lookup"><span data-stu-id="64f1e-1812">seguranca</span></span> 
- <span data-ttu-id="64f1e-1813">contre.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1813">cod.</span></span> <span data-ttu-id="64f1e-1814">Segurança</span><span class="sxs-lookup"><span data-stu-id="64f1e-1814">segurança</span></span> 
- <span data-ttu-id="64f1e-1815">contre.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1815">cod.</span></span> <span data-ttu-id="64f1e-1816">sicurezza</span><span class="sxs-lookup"><span data-stu-id="64f1e-1816">sicurezza</span></span> 
- <span data-ttu-id="64f1e-1817">codice di sicurezza</span><span class="sxs-lookup"><span data-stu-id="64f1e-1817">codice di sicurezza</span></span> 
- <span data-ttu-id="64f1e-1818">codice di verifica</span><span class="sxs-lookup"><span data-stu-id="64f1e-1818">codice di verifica</span></span> 
- <span data-ttu-id="64f1e-1819">Codigo</span><span class="sxs-lookup"><span data-stu-id="64f1e-1819">codigo</span></span> 
- <span data-ttu-id="64f1e-1820">codigo de seguranca</span><span class="sxs-lookup"><span data-stu-id="64f1e-1820">codigo de seguranca</span></span> 
- <span data-ttu-id="64f1e-1821">codigo de segurança</span><span class="sxs-lookup"><span data-stu-id="64f1e-1821">codigo de segurança</span></span> 
- <span data-ttu-id="64f1e-1822">crittogramma</span><span class="sxs-lookup"><span data-stu-id="64f1e-1822">crittogramma</span></span> 
- <span data-ttu-id="64f1e-1823">Cryptogram</span><span class="sxs-lookup"><span data-stu-id="64f1e-1823">cryptogram</span></span> 
- <span data-ttu-id="64f1e-1824">cryptogramme</span><span class="sxs-lookup"><span data-stu-id="64f1e-1824">cryptogramme</span></span> 
- <span data-ttu-id="64f1e-1825">CV2</span><span class="sxs-lookup"><span data-stu-id="64f1e-1825">cv2</span></span> 
- <span data-ttu-id="64f1e-1826">lâche</span><span class="sxs-lookup"><span data-stu-id="64f1e-1826">cvc</span></span> 
- <span data-ttu-id="64f1e-1827">CVC2</span><span class="sxs-lookup"><span data-stu-id="64f1e-1827">cvc2</span></span> 
- <span data-ttu-id="64f1e-1828">cryptogramme</span><span class="sxs-lookup"><span data-stu-id="64f1e-1828">cvn</span></span> 
- <span data-ttu-id="64f1e-1829">CVV</span><span class="sxs-lookup"><span data-stu-id="64f1e-1829">cvv</span></span> 
- <span data-ttu-id="64f1e-1830">CVV2</span><span class="sxs-lookup"><span data-stu-id="64f1e-1830">cvv2</span></span> 
- <span data-ttu-id="64f1e-1831">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="64f1e-1831">cód seguranca</span></span> 
- <span data-ttu-id="64f1e-1832">cód segurança</span><span class="sxs-lookup"><span data-stu-id="64f1e-1832">cód segurança</span></span> 
- <span data-ttu-id="64f1e-1833">Cód.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1833">cód.</span></span> <span data-ttu-id="64f1e-1834">Seguranca</span><span class="sxs-lookup"><span data-stu-id="64f1e-1834">seguranca</span></span> 
- <span data-ttu-id="64f1e-1835">Cód.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1835">cód.</span></span> <span data-ttu-id="64f1e-1836">Segurança</span><span class="sxs-lookup"><span data-stu-id="64f1e-1836">segurança</span></span> 
- <span data-ttu-id="64f1e-1837">Código</span><span class="sxs-lookup"><span data-stu-id="64f1e-1837">código</span></span> 
- <span data-ttu-id="64f1e-1838">código de seguranca</span><span class="sxs-lookup"><span data-stu-id="64f1e-1838">código de seguranca</span></span> 
- <span data-ttu-id="64f1e-1839">código de segurança</span><span class="sxs-lookup"><span data-stu-id="64f1e-1839">código de segurança</span></span> 
- <span data-ttu-id="64f1e-1840">de kaart controle</span><span class="sxs-lookup"><span data-stu-id="64f1e-1840">de kaart controle</span></span> 
- <span data-ttu-id="64f1e-1841">geeft nr suit</span><span class="sxs-lookup"><span data-stu-id="64f1e-1841">geeft nr uit</span></span> 
- <span data-ttu-id="64f1e-1842">n° d’émission</span><span class="sxs-lookup"><span data-stu-id="64f1e-1842">issue no</span></span> 
- <span data-ttu-id="64f1e-1843">numéro d’émission</span><span class="sxs-lookup"><span data-stu-id="64f1e-1843">issue number</span></span> 
- <span data-ttu-id="64f1e-1844">kaartidentificatienummer</span><span class="sxs-lookup"><span data-stu-id="64f1e-1844">kaartidentificatienummer</span></span> 
- <span data-ttu-id="64f1e-1845">kreditkartenprufnummer</span><span class="sxs-lookup"><span data-stu-id="64f1e-1845">kreditkartenprufnummer</span></span> 
- <span data-ttu-id="64f1e-1846">kreditkartenprüfnummer</span><span class="sxs-lookup"><span data-stu-id="64f1e-1846">kreditkartenprüfnummer</span></span> 
- <span data-ttu-id="64f1e-1847">kwestieaantal</span><span class="sxs-lookup"><span data-stu-id="64f1e-1847">kwestieaantal</span></span> 
- <span data-ttu-id="64f1e-1848">Nbre.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1848">no.</span></span> <span data-ttu-id="64f1e-1849">dell'edizione</span><span class="sxs-lookup"><span data-stu-id="64f1e-1849">dell'edizione</span></span> 
- <span data-ttu-id="64f1e-1850">Nbre.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1850">no.</span></span> <span data-ttu-id="64f1e-1851">di sicurezza</span><span class="sxs-lookup"><span data-stu-id="64f1e-1851">di sicurezza</span></span> 
- <span data-ttu-id="64f1e-1852">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="64f1e-1852">numero de securite</span></span> 
- <span data-ttu-id="64f1e-1853">numero de verificacao</span><span class="sxs-lookup"><span data-stu-id="64f1e-1853">numero de verificacao</span></span> 
- <span data-ttu-id="64f1e-1854">numero dell’edizione</span><span class="sxs-lookup"><span data-stu-id="64f1e-1854">numero dell'edizione</span></span> 
- <span data-ttu-id="64f1e-1855">numero di identificazione della</span><span class="sxs-lookup"><span data-stu-id="64f1e-1855">numero di identificazione della</span></span> 
- <span data-ttu-id="64f1e-1856">scheda</span><span class="sxs-lookup"><span data-stu-id="64f1e-1856">scheda</span></span> 
- <span data-ttu-id="64f1e-1857">numero di sicurezza</span><span class="sxs-lookup"><span data-stu-id="64f1e-1857">numero di sicurezza</span></span> 
- <span data-ttu-id="64f1e-1858">numero van veiligheid</span><span class="sxs-lookup"><span data-stu-id="64f1e-1858">numero van veiligheid</span></span> 
- <span data-ttu-id="64f1e-1859">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="64f1e-1859">numéro de sécurité</span></span> 
- <span data-ttu-id="64f1e-1860">nº autorizzazione</span><span class="sxs-lookup"><span data-stu-id="64f1e-1860">nº autorizzazione</span></span> 
- <span data-ttu-id="64f1e-1861">número de verificação</span><span class="sxs-lookup"><span data-stu-id="64f1e-1861">número de verificação</span></span> 
- <span data-ttu-id="64f1e-1862">perno il blocco</span><span class="sxs-lookup"><span data-stu-id="64f1e-1862">perno il blocco</span></span> 
- <span data-ttu-id="64f1e-1863">pin block</span><span class="sxs-lookup"><span data-stu-id="64f1e-1863">pin block</span></span> 
- <span data-ttu-id="64f1e-1864">prufziffer</span><span class="sxs-lookup"><span data-stu-id="64f1e-1864">prufziffer</span></span> 
- <span data-ttu-id="64f1e-1865">Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="64f1e-1865">prüfziffer</span></span> 
- <span data-ttu-id="64f1e-1866">code de sécurité</span><span class="sxs-lookup"><span data-stu-id="64f1e-1866">security code</span></span> 
- <span data-ttu-id="64f1e-1867">n° de sécurité</span><span class="sxs-lookup"><span data-stu-id="64f1e-1867">security no</span></span> 
- <span data-ttu-id="64f1e-1868">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="64f1e-1868">security number</span></span> 
- <span data-ttu-id="64f1e-1869">sicherheits kode</span><span class="sxs-lookup"><span data-stu-id="64f1e-1869">sicherheits kode</span></span> 
- <span data-ttu-id="64f1e-1870">Sicherheitscode</span><span class="sxs-lookup"><span data-stu-id="64f1e-1870">sicherheitscode</span></span> 
- <span data-ttu-id="64f1e-1871">sicherheitsnummer</span><span class="sxs-lookup"><span data-stu-id="64f1e-1871">sicherheitsnummer</span></span> 
- <span data-ttu-id="64f1e-1872">speldblok</span><span class="sxs-lookup"><span data-stu-id="64f1e-1872">speldblok</span></span> 
- <span data-ttu-id="64f1e-1873">veiligheid nr</span><span class="sxs-lookup"><span data-stu-id="64f1e-1873">veiligheid nr</span></span> 
- <span data-ttu-id="64f1e-1874">veiligheidsaantal</span><span class="sxs-lookup"><span data-stu-id="64f1e-1874">veiligheidsaantal</span></span> 
- <span data-ttu-id="64f1e-1875">veiligheidscode</span><span class="sxs-lookup"><span data-stu-id="64f1e-1875">veiligheidscode</span></span> 
- <span data-ttu-id="64f1e-1876">veiligheidsnummer</span><span class="sxs-lookup"><span data-stu-id="64f1e-1876">veiligheidsnummer</span></span> 
- <span data-ttu-id="64f1e-1877">verfalldatum</span><span class="sxs-lookup"><span data-stu-id="64f1e-1877">verfalldatum</span></span> 

#### <a name="keywordcardexpirationtermsdict"></a><span data-ttu-id="64f1e-1878">Keyword_card_expiration_terms_dict</span><span class="sxs-lookup"><span data-stu-id="64f1e-1878">Keyword_card_expiration_terms_dict</span></span>

- <span data-ttu-id="64f1e-1879">Ablauf</span><span class="sxs-lookup"><span data-stu-id="64f1e-1879">ablauf</span></span> 
- <span data-ttu-id="64f1e-1880">data de expiracao</span><span class="sxs-lookup"><span data-stu-id="64f1e-1880">data de expiracao</span></span> 
- <span data-ttu-id="64f1e-1881">data de expiração</span><span class="sxs-lookup"><span data-stu-id="64f1e-1881">data de expiração</span></span> 
- <span data-ttu-id="64f1e-1882">data del exp</span><span class="sxs-lookup"><span data-stu-id="64f1e-1882">data del exp</span></span> 
- <span data-ttu-id="64f1e-1883">data di exp</span><span class="sxs-lookup"><span data-stu-id="64f1e-1883">data di exp</span></span> 
- <span data-ttu-id="64f1e-1884">data di scadenza</span><span class="sxs-lookup"><span data-stu-id="64f1e-1884">data di scadenza</span></span> 
- <span data-ttu-id="64f1e-1885">data em que expira</span><span class="sxs-lookup"><span data-stu-id="64f1e-1885">data em que expira</span></span> 
- <span data-ttu-id="64f1e-1886">data scad</span><span class="sxs-lookup"><span data-stu-id="64f1e-1886">data scad</span></span> 
- <span data-ttu-id="64f1e-1887">data scadenza</span><span class="sxs-lookup"><span data-stu-id="64f1e-1887">data scadenza</span></span> 
- <span data-ttu-id="64f1e-1888">date de validité</span><span class="sxs-lookup"><span data-stu-id="64f1e-1888">date de validité</span></span> 
- <span data-ttu-id="64f1e-1889">datum afloop</span><span class="sxs-lookup"><span data-stu-id="64f1e-1889">datum afloop</span></span> 
- <span data-ttu-id="64f1e-1890">datum van exp</span><span class="sxs-lookup"><span data-stu-id="64f1e-1890">datum van exp</span></span> 
- <span data-ttu-id="64f1e-1891">de afloop</span><span class="sxs-lookup"><span data-stu-id="64f1e-1891">de afloop</span></span> 
- <span data-ttu-id="64f1e-1892">Espira</span><span class="sxs-lookup"><span data-stu-id="64f1e-1892">espira</span></span> 
- <span data-ttu-id="64f1e-1893">Espira</span><span class="sxs-lookup"><span data-stu-id="64f1e-1893">espira</span></span> 
- <span data-ttu-id="64f1e-1894">date d’exp</span><span class="sxs-lookup"><span data-stu-id="64f1e-1894">exp date</span></span> 
- <span data-ttu-id="64f1e-1895">exp datum</span><span class="sxs-lookup"><span data-stu-id="64f1e-1895">exp datum</span></span> 
- <span data-ttu-id="64f1e-1896">pire</span><span class="sxs-lookup"><span data-stu-id="64f1e-1896">expiration</span></span> 
- <span data-ttu-id="64f1e-1897">expiration</span><span class="sxs-lookup"><span data-stu-id="64f1e-1897">expire</span></span> 
- <span data-ttu-id="64f1e-1898">expire</span><span class="sxs-lookup"><span data-stu-id="64f1e-1898">expires</span></span> 
- <span data-ttu-id="64f1e-1899">expiration</span><span class="sxs-lookup"><span data-stu-id="64f1e-1899">expiry</span></span> 
- <span data-ttu-id="64f1e-1900">fecha de expiracion</span><span class="sxs-lookup"><span data-stu-id="64f1e-1900">fecha de expiracion</span></span> 
- <span data-ttu-id="64f1e-1901">fecha de venc</span><span class="sxs-lookup"><span data-stu-id="64f1e-1901">fecha de venc</span></span> 
- <span data-ttu-id="64f1e-1902">gultig bis</span><span class="sxs-lookup"><span data-stu-id="64f1e-1902">gultig bis</span></span> 
- <span data-ttu-id="64f1e-1903">gultigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="64f1e-1903">gultigkeitsdatum</span></span> 
- <span data-ttu-id="64f1e-1904">gültig bis</span><span class="sxs-lookup"><span data-stu-id="64f1e-1904">gültig bis</span></span> 
- <span data-ttu-id="64f1e-1905">gültigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="64f1e-1905">gültigkeitsdatum</span></span> 
- <span data-ttu-id="64f1e-1906">la scadenza</span><span class="sxs-lookup"><span data-stu-id="64f1e-1906">la scadenza</span></span> 
- <span data-ttu-id="64f1e-1907">scadenza</span><span class="sxs-lookup"><span data-stu-id="64f1e-1907">scadenza</span></span> 
- <span data-ttu-id="64f1e-1908">valable</span><span class="sxs-lookup"><span data-stu-id="64f1e-1908">valable</span></span> 
- <span data-ttu-id="64f1e-1909">Validade</span><span class="sxs-lookup"><span data-stu-id="64f1e-1909">validade</span></span> 
- <span data-ttu-id="64f1e-1910">valido hasta</span><span class="sxs-lookup"><span data-stu-id="64f1e-1910">valido hasta</span></span> 
- <span data-ttu-id="64f1e-1911">valorisation</span><span class="sxs-lookup"><span data-stu-id="64f1e-1911">valor</span></span> 
- <span data-ttu-id="64f1e-1912">venc</span><span class="sxs-lookup"><span data-stu-id="64f1e-1912">venc</span></span> 
- <span data-ttu-id="64f1e-1913">vencimento</span><span class="sxs-lookup"><span data-stu-id="64f1e-1913">vencimento</span></span> 
- <span data-ttu-id="64f1e-1914">vencimiento</span><span class="sxs-lookup"><span data-stu-id="64f1e-1914">vencimiento</span></span> 
- <span data-ttu-id="64f1e-1915">verloopt</span><span class="sxs-lookup"><span data-stu-id="64f1e-1915">verloopt</span></span> 
- <span data-ttu-id="64f1e-1916">vervaldag</span><span class="sxs-lookup"><span data-stu-id="64f1e-1916">vervaldag</span></span> 
- <span data-ttu-id="64f1e-1917">vervaldatum</span><span class="sxs-lookup"><span data-stu-id="64f1e-1917">vervaldatum</span></span> 
- <span data-ttu-id="64f1e-1918">vto</span><span class="sxs-lookup"><span data-stu-id="64f1e-1918">vto</span></span> 
- <span data-ttu-id="64f1e-1919">válido hasta</span><span class="sxs-lookup"><span data-stu-id="64f1e-1919">válido hasta</span></span> 
   
## <a name="eu-drivers-license-number"></a><span data-ttu-id="64f1e-1920">Numéro de permis de conduire de l'UE</span><span class="sxs-lookup"><span data-stu-id="64f1e-1920">EU Driver's License Number</span></span>

<span data-ttu-id="64f1e-1921">Pour en savoir plus, consultez [la rubrique informations sensibles sur le numéro de permis de conduire du pilote de l'UE](eu-driver-s-license-number.md).</span><span class="sxs-lookup"><span data-stu-id="64f1e-1921">To learn more, see [EU Driver's License Number sensitive information type](eu-driver-s-license-number.md).</span></span>
  
## <a name="eu-national-identification-number"></a><span data-ttu-id="64f1e-1922">Numéro d'identification nationale de l'UE</span><span class="sxs-lookup"><span data-stu-id="64f1e-1922">EU National Identification Number</span></span>

<span data-ttu-id="64f1e-1923">Pour en savoir plus, consultez la rubrique [informations sensibles du numéro d'identification national](eu-national-identification-number.md)de l'UE.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1923">To learn more, see [EU National Identification Number sensitive information type](eu-national-identification-number.md).</span></span>
  
## <a name="eu-passport-number"></a><span data-ttu-id="64f1e-1924">Numéro de passeport UE</span><span class="sxs-lookup"><span data-stu-id="64f1e-1924">EU Passport Number</span></span>

<span data-ttu-id="64f1e-1925">Pour en savoir plus, consultez la rubrique [type d'informations sensibles du numéro de passeport européen](eu-passport-number.md).</span><span class="sxs-lookup"><span data-stu-id="64f1e-1925">To learn more, see [EU Passport Number sensitive information type](eu-passport-number.md).</span></span>
  
## <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="64f1e-1926">Numéro de sécurité sociale de l'UE ou ID équivalent</span><span class="sxs-lookup"><span data-stu-id="64f1e-1926">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="64f1e-1927">Pour en savoir plus, consultez la rubrique [numéro de sécurité sociale de l'UE ou type d'informations sensibles ID équivalent](eu-social-security-number-or-equivalent-id.md).</span><span class="sxs-lookup"><span data-stu-id="64f1e-1927">To learn more, see [EU Social Security Number or Equivalent ID sensitive information type](eu-social-security-number-or-equivalent-id.md).</span></span>
  
## <a name="eu-tax-identification-number"></a><span data-ttu-id="64f1e-1928">Numéro d'identification fiscale de l'UE</span><span class="sxs-lookup"><span data-stu-id="64f1e-1928">EU Tax Identification Number</span></span>

<span data-ttu-id="64f1e-1929">Pour en savoir plus, consultez la rubrique [euro Tax identification number sensitive type information](eu-tax-identification-number.md).</span><span class="sxs-lookup"><span data-stu-id="64f1e-1929">To learn more, see [EU Tax Identification Number sensitive information type](eu-tax-identification-number.md).</span></span>
  
## <a name="finland-national-id"></a><span data-ttu-id="64f1e-1930">ID national finlandais</span><span class="sxs-lookup"><span data-stu-id="64f1e-1930">Finland National ID</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-1931">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-1931">Format</span></span>

<span data-ttu-id="64f1e-1932">Six chiffres plus un caractère indiquant un siècle plus trois chiffres plus un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-1932">Six digits plus a character indicating a century plus three digits plus a check digit</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-1933">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-1933">Pattern</span></span>

<span data-ttu-id="64f1e-1934">Le modèle doit inclure tous les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="64f1e-1934">Pattern must include all of the following:</span></span>
- <span data-ttu-id="64f1e-1935">Six chiffres au format JJMMAA qui représentent la date de naissance</span><span class="sxs-lookup"><span data-stu-id="64f1e-1935">Six digits in the format format DDMMYY which are a date of birth</span></span> 
- <span data-ttu-id="64f1e-1936">Marqueur de siècle (soit « - », « + » ou « a »)</span><span class="sxs-lookup"><span data-stu-id="64f1e-1936">Century marker (either '-', '+' or 'a')</span></span> 
- <span data-ttu-id="64f1e-1937">Numéro d’identification personnel à trois chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-1937">Three-digit personal identification number</span></span> 
- <span data-ttu-id="64f1e-1938">Un chiffre ou une lettre (ne respectant pas la casse) de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-1938">A digit or letter (case insensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-1939">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-1939">Checksum</span></span>

<span data-ttu-id="64f1e-1940">Oui</span><span class="sxs-lookup"><span data-stu-id="64f1e-1940">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-1941">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-1941">Definition</span></span>

<span data-ttu-id="64f1e-1942">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-1942">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-1943">La fonction Func_finnish_national_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1943">The function Func_finnish_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-1944">Un mot clé figurant dans la liste Keyword_finnish_national_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1944">A keyword from Keyword_finnish_national_id is found.</span></span>
- <span data-ttu-id="64f1e-1945">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1945">The checksum passes.</span></span>

```
<!-- Finnish National ID-->
<Entity id="338FD995-4CB5-4F87-AD35-79BD1DD926C1" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finnish_national_id" />
          <Match idRef="Keyword_finnish_national_id" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-1946">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-1946">Keywords</span></span>

- <span data-ttu-id="64f1e-1947">Keyword_finnish_national_id</span><span class="sxs-lookup"><span data-stu-id="64f1e-1947">Keyword_finnish_national_id</span></span>
- <span data-ttu-id="64f1e-1948">Sosiaaliturvatunnus</span><span class="sxs-lookup"><span data-stu-id="64f1e-1948">Sosiaaliturvatunnus</span></span>
- <span data-ttu-id="64f1e-1949">SOTU Henkilötunnus HETU</span><span class="sxs-lookup"><span data-stu-id="64f1e-1949">SOTU Henkilötunnus HETU</span></span>
- <span data-ttu-id="64f1e-1950">Personbeteckning</span><span class="sxs-lookup"><span data-stu-id="64f1e-1950">Personbeteckning</span></span>
- <span data-ttu-id="64f1e-1951">Personnummer</span><span class="sxs-lookup"><span data-stu-id="64f1e-1951">Personnummer</span></span>
   
## <a name="finland-passport-number"></a><span data-ttu-id="64f1e-1952">Numéro de passeport Finlande</span><span class="sxs-lookup"><span data-stu-id="64f1e-1952">Finland Passport Number</span></span>

<span data-ttu-id="64f1e-1953">Combinaison de format de neuf lettres et chiffres combinaison de neuf lettres et chiffres: deux lettres (ne respectant pas la casse) sept chiffres somme de contrôle no la stratégie DLP est de 75% en certitude qu'elle a détecté ce type d'informations sensibles si, dans un proximité de 300 caractères: l'expression régulière Regex_finland_passport_number trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1953">Format Combination of nine letters and digits Pattern Combination of nine letters and digits: Two letters (not case sensitive) Seven digits Checksum No Definition A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_finland_passport_number finds content that matches the pattern.</span></span>
<span data-ttu-id="64f1e-1954">Un mot clé figurant dans la liste Keyword_finland_passport_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1954">A keyword from Keyword_finland_passport_number is found.</span></span>
<span data-ttu-id="64f1e-1955"><!-- Finland Passport Number -->
<Entity id="d1685ac3-1d3a-40f8-8198-32ef5669c7a5" recommendedConfidence="75" patternsProximity="300"> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_finland_passport_number"/> <Match idRef="Keyword_finland_passport_number"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="64f1e-1955"></span></span>
<span data-ttu-id="64f1e-1956">Mots clés Keyword_finland_passport_number Passport passes</span><span class="sxs-lookup"><span data-stu-id="64f1e-1956">Keywords Keyword_finland_passport_number Passport Passi</span></span>
   
## <a name="france-drivers-license-number"></a><span data-ttu-id="64f1e-1957">Numéro de permis de conduire France</span><span class="sxs-lookup"><span data-stu-id="64f1e-1957">France Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-1958">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-1958">Format</span></span>

<span data-ttu-id="64f1e-1959">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-1959">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-1960">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-1960">Pattern</span></span>

<span data-ttu-id="64f1e-1961">12 chiffres avec validation pour écarter les modèles similaires, comme les numéros de téléphone français</span><span class="sxs-lookup"><span data-stu-id="64f1e-1961">12 digits with validation to discount similar patterns such as French telephone numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-1962">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-1962">Checksum</span></span>

<span data-ttu-id="64f1e-1963">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-1963">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-1964">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-1964">Definition</span></span>

<span data-ttu-id="64f1e-1965">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-1965">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-1966">La fonction Func_french_drivers_license trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1966">The function Func_french_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-1967">Au moins une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="64f1e-1967">At least one of the following is true:</span></span>
- <span data-ttu-id="64f1e-1968">Un mot clé figurant dans la liste Keyword_french_drivers_license est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1968">A keyword from Keyword_french_drivers_license is found.</span></span>
- <span data-ttu-id="64f1e-1969">La fonction Func_eu_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1969">The function Func_eu_date finds a date in the right date format.</span></span>

```
<!-- France Driver's License Number -->
<Entity id="18e55a36-a01b-4b0f-943d-dc10282a1824" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_french_drivers_license" />
        <Any minMatches="1">
          <Match idRef="Keyword_french_drivers_license" />
          <Match idRef="Func_eu_date" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-1970">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-1970">Keywords</span></span>

#### <a name="keywordfrenchdriverslicense"></a><span data-ttu-id="64f1e-1971">Keyword_french_drivers_license</span><span class="sxs-lookup"><span data-stu-id="64f1e-1971">Keyword_french_drivers_license</span></span>

- <span data-ttu-id="64f1e-1972">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-1972">drivers licence</span></span>
- <span data-ttu-id="64f1e-1973">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-1973">drivers license</span></span>
- <span data-ttu-id="64f1e-1974">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-1974">driving licence</span></span>
- <span data-ttu-id="64f1e-1975">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-1975">driving license</span></span>
- <span data-ttu-id="64f1e-1976">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-1976">permis de conduire</span></span>
- <span data-ttu-id="64f1e-1977">numéro de permis</span><span class="sxs-lookup"><span data-stu-id="64f1e-1977">licence number</span></span>
- <span data-ttu-id="64f1e-1978">numéro de permis</span><span class="sxs-lookup"><span data-stu-id="64f1e-1978">license number</span></span>
- <span data-ttu-id="64f1e-1979">numéros de permis</span><span class="sxs-lookup"><span data-stu-id="64f1e-1979">licence numbers</span></span>
- <span data-ttu-id="64f1e-1980">numéros de permis</span><span class="sxs-lookup"><span data-stu-id="64f1e-1980">license numbers</span></span>

## <a name="france-national-id-card-cni"></a><span data-ttu-id="64f1e-1981">Carte nationale d’identité (CNI) France</span><span class="sxs-lookup"><span data-stu-id="64f1e-1981">France National ID Card (CNI)</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-1982">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-1982">Format</span></span>

<span data-ttu-id="64f1e-1983">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-1983">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-1984">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-1984">Pattern</span></span>

<span data-ttu-id="64f1e-1985">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-1985">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-1986">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-1986">Checksum</span></span>

<span data-ttu-id="64f1e-1987">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-1987">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-1988">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-1988">Definition</span></span>

<span data-ttu-id="64f1e-1989">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-1989">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-1990">L’expression régulière Regex_france_cni trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-1990">The regular expression Regex_france_cni finds content that matches the pattern.</span></span>

```
<!-- France CNI -->
<Entity id="f741ac74-1bc0-4665-b69b-f0c7f927c0c4" patternsProximity="300" recommendedConfidence="65">
  <Pattern confidenceLevel="65">
        <IdMatch idRef="Regex_france_cni" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-1991">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-1991">Keywords</span></span>

<span data-ttu-id="64f1e-1992">Aucun</span><span class="sxs-lookup"><span data-stu-id="64f1e-1992">None</span></span>
   
## <a name="france-passport-number"></a><span data-ttu-id="64f1e-1993">Numéro de passeport France</span><span class="sxs-lookup"><span data-stu-id="64f1e-1993">France Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-1994">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-1994">Format</span></span>

<span data-ttu-id="64f1e-1995">Neuf chiffres et lettres</span><span class="sxs-lookup"><span data-stu-id="64f1e-1995">Nine digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-1996">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-1996">Pattern</span></span>

<span data-ttu-id="64f1e-1997">Neuf chiffres et lettres :</span><span class="sxs-lookup"><span data-stu-id="64f1e-1997">Nine digits and letters:</span></span>
- <span data-ttu-id="64f1e-1998">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-1998">Two digits</span></span> 
- <span data-ttu-id="64f1e-1999">Deux lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="64f1e-1999">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="64f1e-2000">Cinq chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2000">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-2001">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2001">Checksum</span></span>

<span data-ttu-id="64f1e-2002">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-2002">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-2003">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-2003">Definition</span></span>

<span data-ttu-id="64f1e-2004">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2004">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-2005">La fonction Func_fr_passport trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2005">The function Func_fr_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-2006">Un mot clé figurant dans la liste Keyword_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2006">A keyword from Keyword_passport is found.</span></span>

```
<!-- France Passport Number -->
<Entity id="3008b884-8c8c-4cd8-a289-99f34fc7ff5d" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_fr_passport" />
        <Match idRef="Keyword_passport" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-2007">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-2007">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="64f1e-2008">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="64f1e-2008">Keyword_passport</span></span>

- <span data-ttu-id="64f1e-2009">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="64f1e-2009">Passport Number</span></span>
- <span data-ttu-id="64f1e-2010">N° de passeport</span><span class="sxs-lookup"><span data-stu-id="64f1e-2010">Passport No</span></span>
- <span data-ttu-id="64f1e-2011"># Passeport</span><span class="sxs-lookup"><span data-stu-id="64f1e-2011">Passport #</span></span>
- <span data-ttu-id="64f1e-2012">Tel</span><span class="sxs-lookup"><span data-stu-id="64f1e-2012">Passport#</span></span>
- <span data-ttu-id="64f1e-2013">PassportID</span><span class="sxs-lookup"><span data-stu-id="64f1e-2013">PassportID</span></span>
- <span data-ttu-id="64f1e-2014">N ° passeport</span><span class="sxs-lookup"><span data-stu-id="64f1e-2014">Passportno</span></span>
- <span data-ttu-id="64f1e-2015">passportnumber</span><span class="sxs-lookup"><span data-stu-id="64f1e-2015">passportnumber</span></span>
- <span data-ttu-id="64f1e-2016">パスポート</span><span class="sxs-lookup"><span data-stu-id="64f1e-2016">パスポート</span></span>
- <span data-ttu-id="64f1e-2017">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="64f1e-2017">パスポート番号</span></span>
- <span data-ttu-id="64f1e-2018">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="64f1e-2018">パスポートのNum</span></span>
- <span data-ttu-id="64f1e-2019">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="64f1e-2019">パスポート ＃</span></span> 
- <span data-ttu-id="64f1e-2020">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="64f1e-2020">Numéro de passeport</span></span>
- <span data-ttu-id="64f1e-2021">Passeport n°</span><span class="sxs-lookup"><span data-stu-id="64f1e-2021">Passeport n °</span></span>
- <span data-ttu-id="64f1e-2022">Passeport numéro</span><span class="sxs-lookup"><span data-stu-id="64f1e-2022">Passeport Non</span></span>
- <span data-ttu-id="64f1e-2023"># Passeport</span><span class="sxs-lookup"><span data-stu-id="64f1e-2023">Passeport #</span></span>
- <span data-ttu-id="64f1e-2024">Passeport</span><span class="sxs-lookup"><span data-stu-id="64f1e-2024">Passeport#</span></span>
- <span data-ttu-id="64f1e-2025">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="64f1e-2025">PasseportNon</span></span>
- <span data-ttu-id="64f1e-2026">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="64f1e-2026">Passeportn °</span></span>

      
## <a name="france-social-security-number-insee"></a><span data-ttu-id="64f1e-2027">Numéro de sécurité sociale (INSEE) France</span><span class="sxs-lookup"><span data-stu-id="64f1e-2027">France Social Security Number (INSEE)</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-2028">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-2028">Format</span></span>

<span data-ttu-id="64f1e-2029">15 chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2029">15 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-2030">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2030">Pattern</span></span>

<span data-ttu-id="64f1e-2031">Doit correspondre à l’un des deux modèles suivants :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2031">Must match one of two patterns:</span></span>
- <span data-ttu-id="64f1e-2032">13 chiffres suivis d'un espace suivi de deux chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2032">13 digits followed by a space followed by two digits</span></span><br/>
<span data-ttu-id="64f1e-2033">ou</span><span class="sxs-lookup"><span data-stu-id="64f1e-2033">or</span></span>
- <span data-ttu-id="64f1e-2034">15 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="64f1e-2034">15 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-2035">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2035">Checksum</span></span>

<span data-ttu-id="64f1e-2036">Oui</span><span class="sxs-lookup"><span data-stu-id="64f1e-2036">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-2037">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-2037">Definition</span></span>

<span data-ttu-id="64f1e-2038">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 95 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2038">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-2039">La fonction Func_french_insee ou Func_fr_insee trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2039">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-2040">Un mot clé figurant dans la liste Keyword_fr_insee est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2040">A keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="64f1e-2041">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2041">The checksum passes.</span></span>

<span data-ttu-id="64f1e-2042">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2042">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-2043">La fonction Func_french_insee ou Func_fr_insee trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2043">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-2044">Aucun mot clé figurant dans la liste Keyword_fr_insee n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2044">No keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="64f1e-2045">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2045">The checksum passes.</span></span>

```
<!-- France INSEE -->
<Entity id="71f62b97-efe0-4aa1-aa49-e14de253619d" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="95">
        <IdMatch idRef="Func_french_insee" />
        <Match idRef="Func_fr_insee" />
        <Any minMatches="1">
          <Match idRef="Keyword_fr_insee" />
        </Any>
  </Pattern>
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_french_insee" />
        <Match idRef="Func_fr_insee" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_fr_insee" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-2046">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-2046">Keywords</span></span>

#### <a name="keywordfrinsee"></a><span data-ttu-id="64f1e-2047">Keyword_fr_insee</span><span class="sxs-lookup"><span data-stu-id="64f1e-2047">Keyword_fr_insee</span></span>

- <span data-ttu-id="64f1e-2048">INSEE</span><span class="sxs-lookup"><span data-stu-id="64f1e-2048">insee</span></span>
- <span data-ttu-id="64f1e-2049">securité sociale</span><span class="sxs-lookup"><span data-stu-id="64f1e-2049">securité sociale</span></span>
- <span data-ttu-id="64f1e-2050">securite sociale</span><span class="sxs-lookup"><span data-stu-id="64f1e-2050">securite sociale</span></span>
- <span data-ttu-id="64f1e-2051">id national</span><span class="sxs-lookup"><span data-stu-id="64f1e-2051">national id</span></span>
- <span data-ttu-id="64f1e-2052">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="64f1e-2052">national identification</span></span>
- <span data-ttu-id="64f1e-2053">numéro d’identité</span><span class="sxs-lookup"><span data-stu-id="64f1e-2053">numéro d'identité</span></span>
- <span data-ttu-id="64f1e-2054">n° d’identité</span><span class="sxs-lookup"><span data-stu-id="64f1e-2054">no d'identité</span></span>
- <span data-ttu-id="64f1e-2055">Nbre.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2055">no.</span></span> <span data-ttu-id="64f1e-2056">d'identité</span><span class="sxs-lookup"><span data-stu-id="64f1e-2056">d'identité</span></span>
- <span data-ttu-id="64f1e-2057">numéro d’identité</span><span class="sxs-lookup"><span data-stu-id="64f1e-2057">numero d'identite</span></span>
- <span data-ttu-id="64f1e-2058">n° d’identité</span><span class="sxs-lookup"><span data-stu-id="64f1e-2058">no d'identite</span></span>
- <span data-ttu-id="64f1e-2059">Nbre.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2059">no.</span></span> <span data-ttu-id="64f1e-2060">d'identite</span><span class="sxs-lookup"><span data-stu-id="64f1e-2060">d'identite</span></span>
- <span data-ttu-id="64f1e-2061">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="64f1e-2061">social security number</span></span>
- <span data-ttu-id="64f1e-2062">code de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="64f1e-2062">social security code</span></span>
- <span data-ttu-id="64f1e-2063">numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="64f1e-2063">social insurance number</span></span>
- <span data-ttu-id="64f1e-2064">le numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="64f1e-2064">le numéro d'identification nationale</span></span>
- <span data-ttu-id="64f1e-2065">d’identité nationale</span><span class="sxs-lookup"><span data-stu-id="64f1e-2065">d'identité nationale</span></span>
- <span data-ttu-id="64f1e-2066">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="64f1e-2066">numéro de sécurité sociale</span></span>
- <span data-ttu-id="64f1e-2067">le code de la sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="64f1e-2067">le code de la sécurité sociale</span></span>
- <span data-ttu-id="64f1e-2068">numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="64f1e-2068">numéro d'assurance sociale</span></span>
- <span data-ttu-id="64f1e-2069">numéro de sécu</span><span class="sxs-lookup"><span data-stu-id="64f1e-2069">numéro de sécu</span></span>
- <span data-ttu-id="64f1e-2070">code sécu</span><span class="sxs-lookup"><span data-stu-id="64f1e-2070">code sécu</span></span> 
   
## <a name="german-drivers-license-number"></a><span data-ttu-id="64f1e-2071">Numéro de permis de conduire Allemagne</span><span class="sxs-lookup"><span data-stu-id="64f1e-2071">German Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-2072">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-2072">Format</span></span>

<span data-ttu-id="64f1e-2073">Combinaison de 11 chiffres et lettres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2073">Combination of 11 digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-2074">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2074">Pattern</span></span>

<span data-ttu-id="64f1e-2075">11 chiffres et lettres (ne respectent pas la casse) :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2075">11 digits and letters (not case sensitive):</span></span>
- <span data-ttu-id="64f1e-2076">Un chiffre ou une lettre</span><span class="sxs-lookup"><span data-stu-id="64f1e-2076">A digit or letter</span></span> 
- <span data-ttu-id="64f1e-2077">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2077">Two digits</span></span> 
- <span data-ttu-id="64f1e-2078">Six chiffres ou lettres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2078">Six digits or letters</span></span> 
- <span data-ttu-id="64f1e-2079">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="64f1e-2079">A digit</span></span> 
- <span data-ttu-id="64f1e-2080">Un chiffre ou une lettre</span><span class="sxs-lookup"><span data-stu-id="64f1e-2080">A digit or letter</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-2081">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2081">Checksum</span></span>

<span data-ttu-id="64f1e-2082">Oui</span><span class="sxs-lookup"><span data-stu-id="64f1e-2082">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-2083">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-2083">Definition</span></span>

<span data-ttu-id="64f1e-2084">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2084">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-2085">La fonction Func_german_drivers_license trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2085">The function Func_german_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-2086">Au moins une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2086">At least one of the following is true:</span></span>
    - <span data-ttu-id="64f1e-2087">Un mot clé figurant dans la liste Keyword_german_drivers_license_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2087">A keyword from Keyword_german_drivers_license_number is found.</span></span>
    - <span data-ttu-id="64f1e-2088">Un mot clé figurant dans la liste Keyword_german_drivers_license_collaborative est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2088">A keyword from Keyword_german_drivers_license_collaborative is found.</span></span>
    - <span data-ttu-id="64f1e-2089">Un mot clé figurant dans la liste Keyword_german_drivers_license est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2089">A keyword from Keyword_german_drivers_license is found.</span></span>
- <span data-ttu-id="64f1e-2090">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2090">The checksum passes.</span></span>

```
<!-- German Driver's License Number -->
<Entity id="91da9335-1edb-45b7-a95f-5fe41a16c63c" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_german_drivers_license" />
        <Any minMatches="1">
          <Match idRef="Keyword_german_drivers_license_number" />
          <Match idRef="Keyword_german_drivers_license_collaborative" />
          <Match idRef="Keyword_german_drivers_license" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-2091">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-2091">Keywords</span></span>

#### <a name="keywordgermandriverslicensenumber"></a><span data-ttu-id="64f1e-2092">Keyword_german_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="64f1e-2092">Keyword_german_drivers_license_number</span></span>

- <span data-ttu-id="64f1e-2093">Führerschein</span><span class="sxs-lookup"><span data-stu-id="64f1e-2093">Führerschein</span></span>
- <span data-ttu-id="64f1e-2094">Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="64f1e-2094">Fuhrerschein</span></span>
- <span data-ttu-id="64f1e-2095">Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="64f1e-2095">Fuehrerschein</span></span>
- <span data-ttu-id="64f1e-2096">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="64f1e-2096">Führerscheinnummer</span></span>
- <span data-ttu-id="64f1e-2097">Fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="64f1e-2097">Fuhrerscheinnummer</span></span>
- <span data-ttu-id="64f1e-2098">Fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="64f1e-2098">Fuehrerscheinnummer</span></span>
- <span data-ttu-id="64f1e-2099">Führerschein</span><span class="sxs-lookup"><span data-stu-id="64f1e-2099">Führerschein-</span></span> 
- <span data-ttu-id="64f1e-2100">Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="64f1e-2100">Fuhrerschein-</span></span> 
- <span data-ttu-id="64f1e-2101">Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="64f1e-2101">Fuehrerschein-</span></span> 
- <span data-ttu-id="64f1e-2102">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="64f1e-2102">FührerscheinnummerNr</span></span>
- <span data-ttu-id="64f1e-2103">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="64f1e-2103">FuhrerscheinnummerNr</span></span>
- <span data-ttu-id="64f1e-2104">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="64f1e-2104">FuehrerscheinnummerNr</span></span>
- <span data-ttu-id="64f1e-2105">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="64f1e-2105">FührerscheinnummerKlasse</span></span>
- <span data-ttu-id="64f1e-2106">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="64f1e-2106">FuhrerscheinnummerKlasse</span></span>
- <span data-ttu-id="64f1e-2107">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="64f1e-2107">FuehrerscheinnummerKlasse</span></span>
- <span data-ttu-id="64f1e-2108">Führerschein - Nr</span><span class="sxs-lookup"><span data-stu-id="64f1e-2108">Führerschein- Nr</span></span>
- <span data-ttu-id="64f1e-2109">Fuhrerschein - Nr</span><span class="sxs-lookup"><span data-stu-id="64f1e-2109">Fuhrerschein- Nr</span></span>
- <span data-ttu-id="64f1e-2110">Fuehrerschein - Nr</span><span class="sxs-lookup"><span data-stu-id="64f1e-2110">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="64f1e-2111">Führerschein - Klasse</span><span class="sxs-lookup"><span data-stu-id="64f1e-2111">Führerschein- Klasse</span></span> 
- <span data-ttu-id="64f1e-2112">Fuhrerschein - Klasse</span><span class="sxs-lookup"><span data-stu-id="64f1e-2112">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="64f1e-2113">Fuehrerschein - Klasse</span><span class="sxs-lookup"><span data-stu-id="64f1e-2113">Fuehrerschein- Klasse</span></span>
- <span data-ttu-id="64f1e-2114">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="64f1e-2114">FührerscheinnummerNr</span></span> 
- <span data-ttu-id="64f1e-2115">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="64f1e-2115">FuhrerscheinnummerNr</span></span> 
- <span data-ttu-id="64f1e-2116">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="64f1e-2116">FuehrerscheinnummerNr</span></span> 
- <span data-ttu-id="64f1e-2117">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="64f1e-2117">FührerscheinnummerKlasse</span></span> 
- <span data-ttu-id="64f1e-2118">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="64f1e-2118">FuhrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="64f1e-2119">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="64f1e-2119">FuehrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="64f1e-2120">Führerschein - Nr</span><span class="sxs-lookup"><span data-stu-id="64f1e-2120">Führerschein- Nr</span></span> 
- <span data-ttu-id="64f1e-2121">Fuhrerschein - Nr</span><span class="sxs-lookup"><span data-stu-id="64f1e-2121">Fuhrerschein- Nr</span></span> 
- <span data-ttu-id="64f1e-2122">Fuehrerschein - Nr</span><span class="sxs-lookup"><span data-stu-id="64f1e-2122">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="64f1e-2123">Führerschein - Klasse</span><span class="sxs-lookup"><span data-stu-id="64f1e-2123">Führerschein- Klasse</span></span> 
- <span data-ttu-id="64f1e-2124">Fuhrerschein - Klasse</span><span class="sxs-lookup"><span data-stu-id="64f1e-2124">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="64f1e-2125">Fuehrerschein - Klasse</span><span class="sxs-lookup"><span data-stu-id="64f1e-2125">Fuehrerschein- Klasse</span></span> 
- <span data-ttu-id="64f1e-2126">LD</span><span class="sxs-lookup"><span data-stu-id="64f1e-2126">DL</span></span> 
- <span data-ttu-id="64f1e-2127">DISTRIBUTION</span><span class="sxs-lookup"><span data-stu-id="64f1e-2127">DLS</span></span>
- <span data-ttu-id="64f1e-2128">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2128">Driv Lic</span></span> 
- <span data-ttu-id="64f1e-2129">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2129">Driv Licen</span></span> 
- <span data-ttu-id="64f1e-2130">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2130">Driv License</span></span>
- <span data-ttu-id="64f1e-2131">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2131">Driv Licenses</span></span> 
- <span data-ttu-id="64f1e-2132">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2132">Driv Licence</span></span> 
- <span data-ttu-id="64f1e-2133">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2133">Driv Licences</span></span> 
- <span data-ttu-id="64f1e-2134">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2134">Driv Lic</span></span> 
- <span data-ttu-id="64f1e-2135">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2135">Driver Licen</span></span> 
- <span data-ttu-id="64f1e-2136">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2136">Driver License</span></span> 
- <span data-ttu-id="64f1e-2137">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2137">Driver Licenses</span></span> 
- <span data-ttu-id="64f1e-2138">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2138">Driver Licence</span></span> 
- <span data-ttu-id="64f1e-2139">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2139">Driver Licences</span></span> 
- <span data-ttu-id="64f1e-2140">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2140">Drivers Lic</span></span> 
- <span data-ttu-id="64f1e-2141">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2141">Drivers Licen</span></span> 
- <span data-ttu-id="64f1e-2142">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2142">Drivers License</span></span> 
- <span data-ttu-id="64f1e-2143">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2143">Drivers Licenses</span></span> 
- <span data-ttu-id="64f1e-2144">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2144">Drivers Licence</span></span> 
- <span data-ttu-id="64f1e-2145">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2145">Drivers Licences</span></span> 
- <span data-ttu-id="64f1e-2146">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2146">Driver's Lic</span></span> 
- <span data-ttu-id="64f1e-2147">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2147">Driver's Licen</span></span> 
- <span data-ttu-id="64f1e-2148">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2148">Driver's License</span></span> 
- <span data-ttu-id="64f1e-2149">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2149">Driver's Licenses</span></span> 
- <span data-ttu-id="64f1e-2150">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2150">Driver's Licence</span></span> 
- <span data-ttu-id="64f1e-2151">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2151">Driver's Licences</span></span> 
- <span data-ttu-id="64f1e-2152">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2152">Driving Lic</span></span> 
- <span data-ttu-id="64f1e-2153">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2153">Driving Licen</span></span> 
- <span data-ttu-id="64f1e-2154">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2154">Driving License</span></span> 
- <span data-ttu-id="64f1e-2155">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2155">Driving Licenses</span></span> 
- <span data-ttu-id="64f1e-2156">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2156">Driving Licence</span></span> 
- <span data-ttu-id="64f1e-2157">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2157">Driving Licences</span></span>

#### <a name="keywordgermandriverslicensecollaborative"></a><span data-ttu-id="64f1e-2158">Keyword_german_drivers_license_collaborative</span><span class="sxs-lookup"><span data-stu-id="64f1e-2158">Keyword_german_drivers_license_collaborative</span></span>

- <span data-ttu-id="64f1e-2159">Nr-Führerschein</span><span class="sxs-lookup"><span data-stu-id="64f1e-2159">Nr-Führerschein</span></span> 
- <span data-ttu-id="64f1e-2160">Nr-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="64f1e-2160">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="64f1e-2161">Nr-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="64f1e-2161">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="64f1e-2162">Non-Führerschein</span><span class="sxs-lookup"><span data-stu-id="64f1e-2162">No-Führerschein</span></span> 
- <span data-ttu-id="64f1e-2163">Non-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="64f1e-2163">No-Fuhrerschein</span></span> 
- <span data-ttu-id="64f1e-2164">Non-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="64f1e-2164">No-Fuehrerschein</span></span> 
- <span data-ttu-id="64f1e-2165">N-Führerschein</span><span class="sxs-lookup"><span data-stu-id="64f1e-2165">N-Führerschein</span></span> 
- <span data-ttu-id="64f1e-2166">N-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="64f1e-2166">N-Fuhrerschein</span></span> 
- <span data-ttu-id="64f1e-2167">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="64f1e-2167">N-Fuehrerschein</span></span>
- <span data-ttu-id="64f1e-2168">Nr-Führerschein</span><span class="sxs-lookup"><span data-stu-id="64f1e-2168">Nr-Führerschein</span></span> 
- <span data-ttu-id="64f1e-2169">Nr-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="64f1e-2169">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="64f1e-2170">Nr-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="64f1e-2170">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="64f1e-2171">Non-Führerschein</span><span class="sxs-lookup"><span data-stu-id="64f1e-2171">No-Führerschein</span></span> 
- <span data-ttu-id="64f1e-2172">Non-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="64f1e-2172">No-Fuhrerschein</span></span> 
- <span data-ttu-id="64f1e-2173">Non-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="64f1e-2173">No-Fuehrerschein</span></span> 
- <span data-ttu-id="64f1e-2174">N-Führerschein</span><span class="sxs-lookup"><span data-stu-id="64f1e-2174">N-Führerschein</span></span> 
- <span data-ttu-id="64f1e-2175">N-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="64f1e-2175">N-Fuhrerschein</span></span> 
- <span data-ttu-id="64f1e-2176">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="64f1e-2176">N-Fuehrerschein</span></span> 

#### <a name="keywordgermandriverslicense"></a><span data-ttu-id="64f1e-2177">Keyword_german_drivers_license</span><span class="sxs-lookup"><span data-stu-id="64f1e-2177">Keyword_german_drivers_license</span></span>

- <span data-ttu-id="64f1e-2178">ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="64f1e-2178">ausstellungsdatum</span></span>
- <span data-ttu-id="64f1e-2179">ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="64f1e-2179">ausstellungsort</span></span>
- <span data-ttu-id="64f1e-2180">ausstellende behöde</span><span class="sxs-lookup"><span data-stu-id="64f1e-2180">ausstellende behöde</span></span>
- <span data-ttu-id="64f1e-2181">ausstellende behorde</span><span class="sxs-lookup"><span data-stu-id="64f1e-2181">ausstellende behorde</span></span>
- <span data-ttu-id="64f1e-2182">ausstellende behoerde</span><span class="sxs-lookup"><span data-stu-id="64f1e-2182">ausstellende behoerde</span></span>
   
## <a name="german-passport-number"></a><span data-ttu-id="64f1e-2183">Numéro de passeport Allemagne</span><span class="sxs-lookup"><span data-stu-id="64f1e-2183">German Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-2184">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-2184">Format</span></span>

<span data-ttu-id="64f1e-2185">10 chiffres ou lettres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2185">10 digits or letters</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-2186">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2186">Pattern</span></span>

<span data-ttu-id="64f1e-2187">Le modèle doit inclure tous les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2187">Pattern must include all of the following:</span></span>
- <span data-ttu-id="64f1e-2188">Le premier caractère est un chiffre ou une lettre de cet ensemble (C, F, G, H, J, K)</span><span class="sxs-lookup"><span data-stu-id="64f1e-2188">First character is a digit or a letter from this set (C, F, G, H, J, K)</span></span> 
- <span data-ttu-id="64f1e-2189">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2189">Three digits</span></span> 
- <span data-ttu-id="64f1e-2190">Cinq chiffres ou lettres à partir de cet ensemble (C, -H, J-N, P, R, T, V-Z)</span><span class="sxs-lookup"><span data-stu-id="64f1e-2190">Five digits or letters from this set (C, -H, J-N, P, R, T, V-Z)</span></span> 
- <span data-ttu-id="64f1e-2191">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="64f1e-2191">A digit</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-2192">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2192">Checksum</span></span>

<span data-ttu-id="64f1e-2193">Oui</span><span class="sxs-lookup"><span data-stu-id="64f1e-2193">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-2194">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-2194">Definition</span></span>

<span data-ttu-id="64f1e-2195">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2195">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-2196">La fonction Func_german_passport trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2196">The function Func_german_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-2197">Un mot clé présent dans l’une des cinq listes de mots clés est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2197">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="64f1e-2198">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2198">The checksum passes.</span></span>

<span data-ttu-id="64f1e-2199">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2199">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-2200">La fonction Func_german_passport_data trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2200">The function Func_german_passport_data finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-2201">Un mot clé présent dans l’une des cinq listes de mots clés est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2201">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="64f1e-2202">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2202">The checksum passes.</span></span>

```
<!-- German Passport Number -->
<Entity id="2e3da144-d42b-47ed-b123-fbf78604e52c" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_german_passport" />
        <Any minMatches="1">
          <Match idRef="Keyword_german_passport" />
          <Match idRef="Keyword_german_passport_collaborative" />
          <Match idRef="Keyword_german_passport_number" />
          <Match idRef="Keyword_german_passport1" />
          <Match idRef="Keyword_german_passport2" />
        </Any>
  </Pattern>
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_german_passport_data" />
        <Any minMatches="1">
          <Match idRef="Keyword_german_passport" />
          <Match idRef="Keyword_german_passport_collaborative" />
          <Match idRef="Keyword_german_passport_number" />
          <Match idRef="Keyword_german_passport1" />
          <Match idRef="Keyword_german_passport2" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-2203">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-2203">Keywords</span></span>

#### <a name="keywordgermanpassport"></a><span data-ttu-id="64f1e-2204">Keyword_german_passport</span><span class="sxs-lookup"><span data-stu-id="64f1e-2204">Keyword_german_passport</span></span>

- <span data-ttu-id="64f1e-2205">Reisepass</span><span class="sxs-lookup"><span data-stu-id="64f1e-2205">reisepass</span></span>
- <span data-ttu-id="64f1e-2206">reisepasse</span><span class="sxs-lookup"><span data-stu-id="64f1e-2206">reisepasse</span></span>
- <span data-ttu-id="64f1e-2207">reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="64f1e-2207">reisepassnummer</span></span>
- <span data-ttu-id="64f1e-2208">tel</span><span class="sxs-lookup"><span data-stu-id="64f1e-2208">passport</span></span>
- <span data-ttu-id="64f1e-2209">passeports</span><span class="sxs-lookup"><span data-stu-id="64f1e-2209">passports</span></span>

#### <a name="keywordgermanpassportcollaborative"></a><span data-ttu-id="64f1e-2210">Keyword_german_passport_collaborative</span><span class="sxs-lookup"><span data-stu-id="64f1e-2210">Keyword_german_passport_collaborative</span></span>

- <span data-ttu-id="64f1e-2211">geburtsdatum</span><span class="sxs-lookup"><span data-stu-id="64f1e-2211">geburtsdatum</span></span>
- <span data-ttu-id="64f1e-2212">ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="64f1e-2212">ausstellungsdatum</span></span>
- <span data-ttu-id="64f1e-2213">ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="64f1e-2213">ausstellungsort</span></span>

#### <a name="keywordgermanpassportnumber"></a><span data-ttu-id="64f1e-2214">Keyword_german_passport_number</span><span class="sxs-lookup"><span data-stu-id="64f1e-2214">Keyword_german_passport_number</span></span>

<span data-ttu-id="64f1e-2215">No-Reisepass Nr-Reisepass</span><span class="sxs-lookup"><span data-stu-id="64f1e-2215">No-Reisepass Nr-Reisepass</span></span>

#### <a name="keywordgermanpassport1"></a><span data-ttu-id="64f1e-2216">Keyword_german_passport1</span><span class="sxs-lookup"><span data-stu-id="64f1e-2216">Keyword_german_passport1</span></span>

<span data-ttu-id="64f1e-2217">Reisepass-Nr</span><span class="sxs-lookup"><span data-stu-id="64f1e-2217">Reisepass-Nr</span></span>

#### <a name="keywordgermanpassport2"></a><span data-ttu-id="64f1e-2218">Keyword_german_passport2</span><span class="sxs-lookup"><span data-stu-id="64f1e-2218">Keyword_german_passport2</span></span>

<span data-ttu-id="64f1e-2219">bnationalit. t</span><span class="sxs-lookup"><span data-stu-id="64f1e-2219">bnationalit.t</span></span>
   
## <a name="germany-identity-card-number"></a><span data-ttu-id="64f1e-2220">Numéro de carte d’identité allemand</span><span class="sxs-lookup"><span data-stu-id="64f1e-2220">Germany Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-2221">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-2221">Format</span></span>

<span data-ttu-id="64f1e-2222">Depuis le 1er novembre 2010: neuf lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2222">Since 1 November 2010: Nine letters and digits</span></span>

<span data-ttu-id="64f1e-2223">Du 1er avril 1987 au 31 octobre 2010:10 chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2223">From 1 April 1987 until 31 October 2010: 10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-2224">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2224">Pattern</span></span>

<span data-ttu-id="64f1e-2225">Depuis le 1er novembre 2010 :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2225">Since 1 November 2010:</span></span>
- <span data-ttu-id="64f1e-2226">Une lettre (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="64f1e-2226">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="64f1e-2227">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2227">Eight digits</span></span>

<span data-ttu-id="64f1e-2228">Du 1er avril 1987 au 31 octobre 2010:</span><span class="sxs-lookup"><span data-stu-id="64f1e-2228">From 1 April 1987 until 31 October 2010:</span></span>
- <span data-ttu-id="64f1e-2229">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2229">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-2230">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2230">Checksum</span></span>

<span data-ttu-id="64f1e-2231">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-2231">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-2232">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-2232">Definition</span></span>

<span data-ttu-id="64f1e-2233">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2233">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-2234">L’expression régulière Regex_germany_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2234">The regular expression Regex_germany_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-2235">Un mot clé figurant dans la liste Keyword_germany_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2235">A keyword from Keyword_germany_id_card is found.</span></span>

```
<!-- Germany Identity Card Number -->
<Entity id="e577372f-c42e-47a0-9d85-bebed1c237d4" recommendedConfidence="65" patternsProximity="300">
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Regex_germany_id_card"/>
     <Match idRef="Keyword_germany_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-2236">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-2236">Keywords</span></span>

#### <a name="keywordgermanyidcard"></a><span data-ttu-id="64f1e-2237">Keyword_germany_id_card</span><span class="sxs-lookup"><span data-stu-id="64f1e-2237">Keyword_germany_id_card</span></span>

- <span data-ttu-id="64f1e-2238">Identity Card</span><span class="sxs-lookup"><span data-stu-id="64f1e-2238">Identity Card</span></span>
- <span data-ttu-id="64f1e-2239">ID</span><span class="sxs-lookup"><span data-stu-id="64f1e-2239">ID</span></span>
- <span data-ttu-id="64f1e-2240">Identificateur</span><span class="sxs-lookup"><span data-stu-id="64f1e-2240">Identification</span></span>
- <span data-ttu-id="64f1e-2241">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="64f1e-2241">Personalausweis</span></span>
- <span data-ttu-id="64f1e-2242">Identifizierungsnummer</span><span class="sxs-lookup"><span data-stu-id="64f1e-2242">Identifizierungsnummer</span></span>
- <span data-ttu-id="64f1e-2243">Ausweis</span><span class="sxs-lookup"><span data-stu-id="64f1e-2243">Ausweis</span></span>
- <span data-ttu-id="64f1e-2244">Identifikation</span><span class="sxs-lookup"><span data-stu-id="64f1e-2244">Identifikation</span></span>
   
## <a name="greece-national-id-card"></a><span data-ttu-id="64f1e-2245">Carte d’identité nationale Grèce</span><span class="sxs-lookup"><span data-stu-id="64f1e-2245">Greece National ID Card</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-2246">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-2246">Format</span></span>

<span data-ttu-id="64f1e-2247">Combinaison de 7 ou 8 lettres et chiffres, plus un tiret</span><span class="sxs-lookup"><span data-stu-id="64f1e-2247">Combination of 7-8 letters and numbers plus a dash</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-2248">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2248">Pattern</span></span>

<span data-ttu-id="64f1e-2249">Sept lettres et chiffres (ancien format) :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2249">Seven letters and numbers (old format):</span></span>
- <span data-ttu-id="64f1e-2250">Une lettre (de l’alphabet grec) </span><span class="sxs-lookup"><span data-stu-id="64f1e-2250">One letter (any letter of the Greek alphabet)</span></span> 
- <span data-ttu-id="64f1e-2251">Un tiret</span><span class="sxs-lookup"><span data-stu-id="64f1e-2251">A dash</span></span> 
- <span data-ttu-id="64f1e-2252">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2252">Six digits</span></span>

<span data-ttu-id="64f1e-2253">Huit lettres et chiffres (nouveau format) :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2253">Eight letters and numbers (new format):</span></span>
- <span data-ttu-id="64f1e-2254">Deux lettres dont le caractère majuscule figure à la fois dans l’alphabet grec et l’alphabet latin (ABEZHIKMNOPTYX) </span><span class="sxs-lookup"><span data-stu-id="64f1e-2254">Two letters whose uppercase character occurs in both the Greek and Latin alphabets (ABEZHIKMNOPTYX)</span></span> 
- <span data-ttu-id="64f1e-2255">Un tiret</span><span class="sxs-lookup"><span data-stu-id="64f1e-2255">A dash</span></span> 
- <span data-ttu-id="64f1e-2256">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2256">Six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-2257">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2257">Checksum</span></span>

<span data-ttu-id="64f1e-2258">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-2258">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-2259">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-2259">Definition</span></span>

<span data-ttu-id="64f1e-2260">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2260">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-2261">L’expression régulière Regex_greece_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2261">The regular expression Regex_greece_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-2262">Un mot clé figurant dans la liste Keyword_greece_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2262">A keyword from Keyword_greece_id_card is found.</span></span>

```
<!-- Greece National ID Card -->
<Entity id="82568215-1da1-46d3-874a-d2294d81b5ac" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_greece_id_card"/>
     <Match idRef="Keyword_greece_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-2263">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-2263">Keywords</span></span>

#### <a name="keywordgreeceidcard"></a><span data-ttu-id="64f1e-2264">Keyword_greece_id_card</span><span class="sxs-lookup"><span data-stu-id="64f1e-2264">Keyword_greece_id_card</span></span>

- <span data-ttu-id="64f1e-2265">Greek identity Card</span><span class="sxs-lookup"><span data-stu-id="64f1e-2265">Greek identity Card</span></span>
- <span data-ttu-id="64f1e-2266">Tautotita</span><span class="sxs-lookup"><span data-stu-id="64f1e-2266">Tautotita</span></span>
- <span data-ttu-id="64f1e-2267">Δελτίο αστυνομικής ταυτότητας</span><span class="sxs-lookup"><span data-stu-id="64f1e-2267">Δελτίο αστυνομικής ταυτότητας</span></span>
- <span data-ttu-id="64f1e-2268">Ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="64f1e-2268">Ταυτότητα</span></span>
   
## <a name="hong-kong-identity-card-hkid-number"></a><span data-ttu-id="64f1e-2269">Numéro de carte d’identité (HKID) Hong Kong</span><span class="sxs-lookup"><span data-stu-id="64f1e-2269">Hong Kong Identity Card (HKID) Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-2270">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-2270">Format</span></span>

<span data-ttu-id="64f1e-2271">Combinaison de 8 ou 9 lettres et chiffres plus éventuellement des parenthèses autour du dernier caractère</span><span class="sxs-lookup"><span data-stu-id="64f1e-2271">Combination of 8-9 letters and numbers plus optional parentheses around the final character</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-2272">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2272">Pattern</span></span>

<span data-ttu-id="64f1e-2273">Combinaison de 8 ou 9 lettres :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2273">Combination of 8-9 letters:</span></span>
- <span data-ttu-id="64f1e-2274">1 ou 2 lettres (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="64f1e-2274">1-2 letters (not case sensitive)</span></span> 
- <span data-ttu-id="64f1e-2275">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2275">Six digits</span></span> 
- <span data-ttu-id="64f1e-2276">Le dernier caractère (un chiffre ou la lettre A), qui est le chiffre de contrôle et est éventuellement entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2276">The final character (any digit or the letter A), which is the check digit and is optionally enclosed in parentheses.</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-2277">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2277">Checksum</span></span>

<span data-ttu-id="64f1e-2278">Oui</span><span class="sxs-lookup"><span data-stu-id="64f1e-2278">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-2279">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-2279">Definition</span></span>

<span data-ttu-id="64f1e-2280">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2280">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-2281">La fonction Func_hong_kong_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2281">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-2282">Un mot clé figurant dans la liste Keyword_hong_kong_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2282">A keyword from Keyword_hong_kong_id_card is found.</span></span>
- <span data-ttu-id="64f1e-2283">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2283">The checksum passes.</span></span>

<span data-ttu-id="64f1e-2284">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2284">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-2285">La fonction Func_hong_kong_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2285">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-2286">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2286">The checksum passes.</span></span>

```
<!-- Hong Kong Identity Card (HKID) number -->
<Entity id="e63c28a7-ad29-4c17-a41a-3d2a0b70fd9c" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_hong_kong_id_card"/>
     <Match idRef="Keyword_hong_kong_id_card"/>
  </Pattern>
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Func_hong_kong_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-2287">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-2287">Keywords</span></span>

#### <a name="keywordhongkongidcard"></a><span data-ttu-id="64f1e-2288">Keyword_hong_kong_id_card</span><span class="sxs-lookup"><span data-stu-id="64f1e-2288">Keyword_hong_kong_id_card</span></span>

- <span data-ttu-id="64f1e-2289">carte d'identité de Hong Kong</span><span class="sxs-lookup"><span data-stu-id="64f1e-2289">hong kong identity card</span></span>
- <span data-ttu-id="64f1e-2290">HKIDC</span><span class="sxs-lookup"><span data-stu-id="64f1e-2290">HKIDC</span></span>
- <span data-ttu-id="64f1e-2291">carte d’identité</span><span class="sxs-lookup"><span data-stu-id="64f1e-2291">id card</span></span>
- <span data-ttu-id="64f1e-2292">Carte d’identité</span><span class="sxs-lookup"><span data-stu-id="64f1e-2292">identity card</span></span>
- <span data-ttu-id="64f1e-2293">carte d'identité HK</span><span class="sxs-lookup"><span data-stu-id="64f1e-2293">hk identity card</span></span>
- <span data-ttu-id="64f1e-2294">ID Hong Kong</span><span class="sxs-lookup"><span data-stu-id="64f1e-2294">hong kong id</span></span>
- <span data-ttu-id="64f1e-2295">香港身份證</span><span class="sxs-lookup"><span data-stu-id="64f1e-2295">香港身份證</span></span>
- <span data-ttu-id="64f1e-2296">香港永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="64f1e-2296">香港永久性居民身份證</span></span>
- <span data-ttu-id="64f1e-2297">身份證</span><span class="sxs-lookup"><span data-stu-id="64f1e-2297">身份證</span></span>
- <span data-ttu-id="64f1e-2298">身份証</span><span class="sxs-lookup"><span data-stu-id="64f1e-2298">身份証</span></span>
- <span data-ttu-id="64f1e-2299">身分證</span><span class="sxs-lookup"><span data-stu-id="64f1e-2299">身分證</span></span>
- <span data-ttu-id="64f1e-2300">身分証</span><span class="sxs-lookup"><span data-stu-id="64f1e-2300">身分証</span></span>
- <span data-ttu-id="64f1e-2301">香港身份証</span><span class="sxs-lookup"><span data-stu-id="64f1e-2301">香港身份証</span></span>
- <span data-ttu-id="64f1e-2302">香港身分證</span><span class="sxs-lookup"><span data-stu-id="64f1e-2302">香港身分證</span></span>
- <span data-ttu-id="64f1e-2303">香港身分証</span><span class="sxs-lookup"><span data-stu-id="64f1e-2303">香港身分証</span></span>
- <span data-ttu-id="64f1e-2304">香港身份證</span><span class="sxs-lookup"><span data-stu-id="64f1e-2304">香港身份證</span></span>
- <span data-ttu-id="64f1e-2305">香港居民身份證</span><span class="sxs-lookup"><span data-stu-id="64f1e-2305">香港居民身份證</span></span>
- <span data-ttu-id="64f1e-2306">香港居民身份証</span><span class="sxs-lookup"><span data-stu-id="64f1e-2306">香港居民身份証</span></span>
- <span data-ttu-id="64f1e-2307">香港居民身分證</span><span class="sxs-lookup"><span data-stu-id="64f1e-2307">香港居民身分證</span></span>
- <span data-ttu-id="64f1e-2308">香港居民身分証</span><span class="sxs-lookup"><span data-stu-id="64f1e-2308">香港居民身分証</span></span>
- <span data-ttu-id="64f1e-2309">香港永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="64f1e-2309">香港永久性居民身份証</span></span>
- <span data-ttu-id="64f1e-2310">香港永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="64f1e-2310">香港永久性居民身分證</span></span>
- <span data-ttu-id="64f1e-2311">香港永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="64f1e-2311">香港永久性居民身分証</span></span>
- <span data-ttu-id="64f1e-2312">香港永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="64f1e-2312">香港永久性居民身份證</span></span>
- <span data-ttu-id="64f1e-2313">香港非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="64f1e-2313">香港非永久性居民身份證</span></span>
- <span data-ttu-id="64f1e-2314">香港非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="64f1e-2314">香港非永久性居民身份証</span></span>
- <span data-ttu-id="64f1e-2315">香港非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="64f1e-2315">香港非永久性居民身分證</span></span>
- <span data-ttu-id="64f1e-2316">香港非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="64f1e-2316">香港非永久性居民身分証</span></span>
- <span data-ttu-id="64f1e-2317">香港特別行政區永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="64f1e-2317">香港特別行政區永久性居民身份證</span></span>
- <span data-ttu-id="64f1e-2318">香港特別行政區永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="64f1e-2318">香港特別行政區永久性居民身份証</span></span>
- <span data-ttu-id="64f1e-2319">香港特別行政區永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="64f1e-2319">香港特別行政區永久性居民身分證</span></span>
- <span data-ttu-id="64f1e-2320">香港特別行政區永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="64f1e-2320">香港特別行政區永久性居民身分証</span></span>
- <span data-ttu-id="64f1e-2321">香港特別行政區非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="64f1e-2321">香港特別行政區非永久性居民身份證</span></span>
- <span data-ttu-id="64f1e-2322">香港特別行政區非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="64f1e-2322">香港特別行政區非永久性居民身份証</span></span>
- <span data-ttu-id="64f1e-2323">香港特別行政區非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="64f1e-2323">香港特別行政區非永久性居民身分證</span></span>
- <span data-ttu-id="64f1e-2324">香港特別行政區非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="64f1e-2324">香港特別行政區非永久性居民身分証</span></span>
   
## <a name="india-permanent-account-number-pan"></a><span data-ttu-id="64f1e-2325">Numéro de compte permanent Inde</span><span class="sxs-lookup"><span data-stu-id="64f1e-2325">India Permanent Account Number (PAN)</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-2326">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-2326">Format</span></span>

<span data-ttu-id="64f1e-2327">10 lettres ou chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2327">10 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-2328">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2328">Pattern</span></span>

<span data-ttu-id="64f1e-2329">10 lettres ou chiffres :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2329">10 letters or digits:</span></span>
- <span data-ttu-id="64f1e-2330">Cinq lettres (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="64f1e-2330">Five letters (not case sensitive)</span></span> 
- <span data-ttu-id="64f1e-2331">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2331">Four digits</span></span> 
- <span data-ttu-id="64f1e-2332">Une lettre qui est un chiffre de contrôle alphabétique</span><span class="sxs-lookup"><span data-stu-id="64f1e-2332">A letter which is an alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-2333">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2333">Checksum</span></span>

<span data-ttu-id="64f1e-2334">Oui</span><span class="sxs-lookup"><span data-stu-id="64f1e-2334">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-2335">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-2335">Definition</span></span>

<span data-ttu-id="64f1e-2336">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2336">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-2337">L’expression régulière Regex_india_permanent_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2337">The regular expression Regex_india_permanent_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-2338">Un mot clé figurant dans la liste Keyword_india_permanent_account_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2338">A keyword from Keyword_india_permanent_account_number is found.</span></span>
- <span data-ttu-id="64f1e-2339">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2339">The checksum passes.</span></span>

```
<!-- India Permanent Account Number -->
<Entity id="2602bfee-9bb0-47a5-a7a6-2bf3053e2804" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_india_permanent_account_number"/>
     <Match idRef="Keyword_india_permanent_account_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-2340">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-2340">Keywords</span></span>

#### <a name="keywordindiapermanentaccountnumber"></a><span data-ttu-id="64f1e-2341">Keyword_india_permanent_account_number</span><span class="sxs-lookup"><span data-stu-id="64f1e-2341">Keyword_india_permanent_account_number</span></span>

- <span data-ttu-id="64f1e-2342">Permanent Account Number</span><span class="sxs-lookup"><span data-stu-id="64f1e-2342">Permanent Account Number</span></span> 
- <span data-ttu-id="64f1e-2343">PANEUROPÉENNES</span><span class="sxs-lookup"><span data-stu-id="64f1e-2343">PAN</span></span> 
   
## <a name="india-unique-identification-aadhaar-number"></a><span data-ttu-id="64f1e-2344">Numéro d’identification unique (Aadhaar) Inde</span><span class="sxs-lookup"><span data-stu-id="64f1e-2344">India Unique Identification (Aadhaar) Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-2345">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-2345">Format</span></span>

<span data-ttu-id="64f1e-2346">12 chiffres contenant éventuellement des espaces ou des tirets</span><span class="sxs-lookup"><span data-stu-id="64f1e-2346">12 digits containing optional spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-2347">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2347">Pattern</span></span>

<span data-ttu-id="64f1e-2348">12 chiffres :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2348">12 digits:</span></span>
- <span data-ttu-id="64f1e-2349">Quatre chiffres </span><span class="sxs-lookup"><span data-stu-id="64f1e-2349">Four digits</span></span> 
- <span data-ttu-id="64f1e-2350">Éventuellement un tiret ou un espace </span><span class="sxs-lookup"><span data-stu-id="64f1e-2350">An optional space or dash</span></span> 
- <span data-ttu-id="64f1e-2351">Quatre chiffres </span><span class="sxs-lookup"><span data-stu-id="64f1e-2351">Four digits</span></span> 
- <span data-ttu-id="64f1e-2352">Éventuellement un tiret ou un espace </span><span class="sxs-lookup"><span data-stu-id="64f1e-2352">An optional space or dash</span></span> 
- <span data-ttu-id="64f1e-2353">Le chiffre final, qui est le chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2353">The final digit which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-2354">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2354">Checksum</span></span>

<span data-ttu-id="64f1e-2355">Oui</span><span class="sxs-lookup"><span data-stu-id="64f1e-2355">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-2356">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-2356">Definition</span></span>

<span data-ttu-id="64f1e-2357">Une stratégie DLP est sûre à 85% d'avoir détecté ce type d'informations sensibles si, dans une proximité de 300 caractères: la fonction Func_india_aadhaar trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2357">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern.</span></span>
<span data-ttu-id="64f1e-2358">Un mot clé figurant dans la liste Keyword_india_aadhar est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2358">A keyword from Keyword_india_aadhar is found.</span></span>
<span data-ttu-id="64f1e-2359">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2359">The checksum passes.</span></span>
<span data-ttu-id="64f1e-2360">Une stratégie DLP est sûre à 75% d'avoir détecté ce type d'informations sensibles si, dans une proximité de 300 caractères: la fonction Func_india_aadhaar trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2360">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern.</span></span>
<span data-ttu-id="64f1e-2361">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2361">The checksum passes.</span></span>
<span data-ttu-id="64f1e-2362"><!-- India Unique Identification (Aadhaar) number -->
<Entity id="1ca46b29-76f5-4f46-9383-cfa15e91048f" recommendedConfidence="85" patternsProximity="300"> <Pattern confidenceLevel="85"> <IdMatch idRef="Func_india_aadhaar"/> <Match idRef="Keyword_india_aadhar"/> </Pattern> <Pattern confidenceLevel="75"> <IdMatch idRef="Func_india_aadhaar"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="64f1e-2362"></span></span>

### <a name="keywords"></a><span data-ttu-id="64f1e-2363">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-2363">Keywords</span></span>
   
#### <a name="keywordindiaaadhar"></a><span data-ttu-id="64f1e-2364">Keyword_india_aadhar</span><span class="sxs-lookup"><span data-stu-id="64f1e-2364">Keyword_india_aadhar</span></span>
- <span data-ttu-id="64f1e-2365">Aadhar</span><span class="sxs-lookup"><span data-stu-id="64f1e-2365">Aadhar</span></span>
- <span data-ttu-id="64f1e-2366">Aadhaar</span><span class="sxs-lookup"><span data-stu-id="64f1e-2366">Aadhaar</span></span>
- <span data-ttu-id="64f1e-2367">UID</span><span class="sxs-lookup"><span data-stu-id="64f1e-2367">UID</span></span>
- <span data-ttu-id="64f1e-2368">आधार</span><span class="sxs-lookup"><span data-stu-id="64f1e-2368">आधार</span></span>
   
## <a name="indonesia-identity-card-ktp-number"></a><span data-ttu-id="64f1e-2369">Numéro de carte d’identité (KTP) Indonésie</span><span class="sxs-lookup"><span data-stu-id="64f1e-2369">Indonesia Identity Card (KTP) Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-2370">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-2370">Format</span></span>

<span data-ttu-id="64f1e-2371">16 chiffres contenant éventuellement des points</span><span class="sxs-lookup"><span data-stu-id="64f1e-2371">16 digits containing optional periods</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-2372">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2372">Pattern</span></span>

<span data-ttu-id="64f1e-2373">16 chiffres :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2373">16 digits:</span></span>
- <span data-ttu-id="64f1e-2374">Code à deux chiffres désignant la province </span><span class="sxs-lookup"><span data-stu-id="64f1e-2374">Two-digit province code</span></span> 
- <span data-ttu-id="64f1e-2375">Un point (facultatif) </span><span class="sxs-lookup"><span data-stu-id="64f1e-2375">A period (optional)</span></span> 
- <span data-ttu-id="64f1e-2376">Code à deux chiffres désignant une régence ou une ville </span><span class="sxs-lookup"><span data-stu-id="64f1e-2376">Two-digit regency or city code</span></span> 
- <span data-ttu-id="64f1e-2377">Code à deux chiffres désignant un sous-district </span><span class="sxs-lookup"><span data-stu-id="64f1e-2377">Two-digit subdistrict code</span></span> 
- <span data-ttu-id="64f1e-2378">Un point (facultatif) </span><span class="sxs-lookup"><span data-stu-id="64f1e-2378">A period (optional)</span></span> 
- <span data-ttu-id="64f1e-2379">Six chiffres au format JJMMAA qui correspondent à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="64f1e-2379">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="64f1e-2380">Un point (facultatif) </span><span class="sxs-lookup"><span data-stu-id="64f1e-2380">A period (optional)</span></span> 
- <span data-ttu-id="64f1e-2381">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2381">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-2382">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2382">Checksum</span></span>

<span data-ttu-id="64f1e-2383">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-2383">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-2384">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-2384">Definition</span></span>

<span data-ttu-id="64f1e-2385">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2385">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-2386">L’expression régulière Regex_indonesia_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2386">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-2387">Un mot clé figurant dans la liste Keyword_indonesia_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2387">A keyword from Keyword_indonesia_id_card is found.</span></span>

<span data-ttu-id="64f1e-2388">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2388">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-2389">L’expression régulière Regex_indonesia_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2389">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>

```
<!-- Indonesia Identity Card (KTP) Number -->
<Entity id="da68fdb0-f383-4981-8c86-82689d3b7d55" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_indonesia_id_card"/>
     <Match idRef="Keyword_indonesia_id_card"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_indonesia_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-2390">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-2390">Keywords</span></span>
   
#### <a name="keywordindonesiaidcard"></a><span data-ttu-id="64f1e-2391">Keyword_indonesia_id_card</span><span class="sxs-lookup"><span data-stu-id="64f1e-2391">Keyword_indonesia_id_card</span></span>

- <span data-ttu-id="64f1e-2392">KTP</span><span class="sxs-lookup"><span data-stu-id="64f1e-2392">KTP</span></span>
- <span data-ttu-id="64f1e-2393">Kartu Tanda Penduduk</span><span class="sxs-lookup"><span data-stu-id="64f1e-2393">Kartu Tanda Penduduk</span></span> 
- <span data-ttu-id="64f1e-2394">Nomor Induk Kependudukan</span><span class="sxs-lookup"><span data-stu-id="64f1e-2394">Nomor Induk Kependudukan</span></span> 
   
## <a name="international-banking-account-number-iban"></a><span data-ttu-id="64f1e-2395">Numéro de compte bancaire international (IBAN)</span><span class="sxs-lookup"><span data-stu-id="64f1e-2395">International Banking Account Number (IBAN)</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-2396">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-2396">Format</span></span>

<span data-ttu-id="64f1e-2397">Code pays (à deux lettres) plus chiffres de contrôle (à deux chiffres) plus numéro BBAN (jusqu’à 30 chiffres)</span><span class="sxs-lookup"><span data-stu-id="64f1e-2397">Country code (two letters) plus check digits (two digits) plus bban number (up to 30 characters)</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-2398">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2398">Pattern</span></span>

<span data-ttu-id="64f1e-2399">Le modèle doit inclure tous les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2399">Pattern must include all of the following:</span></span>

- <span data-ttu-id="64f1e-2400">Code pays à deux lettres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2400">Two-letter country code</span></span>
- <span data-ttu-id="64f1e-2401">Deux chiffres de contrôle (suivis d’un espace facultatif) </span><span class="sxs-lookup"><span data-stu-id="64f1e-2401">Two check digits (followed by an optional space)</span></span> 
- <span data-ttu-id="64f1e-2402">1 à 7 groupes de quatre lettres ou chiffres (séparés par des espaces facultatifs)</span><span class="sxs-lookup"><span data-stu-id="64f1e-2402">1-7 groups of four letters or digits (can be separated by spaces)</span></span>
- <span data-ttu-id="64f1e-2403">1 à 3 lettres ou chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2403">1-3 letters or digits</span></span>

<span data-ttu-id="64f1e-p134">Le format pour chaque pays est légèrement différent. Le type d’informations sensibles IBAN recouvre ces 60 pays :</span><span class="sxs-lookup"><span data-stu-id="64f1e-p134">The format for each country is slightly different. The IBAN sensitive information type covers these 60 countries:</span></span>

<span data-ttu-id="64f1e-2406">ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg</span><span class="sxs-lookup"><span data-stu-id="64f1e-2406">ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-2407">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2407">Checksum</span></span>

<span data-ttu-id="64f1e-2408">Oui</span><span class="sxs-lookup"><span data-stu-id="64f1e-2408">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-2409">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-2409">Definition</span></span>

<span data-ttu-id="64f1e-2410">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2410">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-2411">La fonction Func_iban trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2411">The function Func_iban finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-2412">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2412">The checksum passes.</span></span>

```
<Entity id="e7dc4711-11b7-4cb0-b88b-2c394a771f0e" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_iban" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-2413">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-2413">Keywords</span></span>

<span data-ttu-id="64f1e-2414">Aucun</span><span class="sxs-lookup"><span data-stu-id="64f1e-2414">None</span></span>

   
## <a name="ip-address"></a><span data-ttu-id="64f1e-2415">Adresse IP</span><span class="sxs-lookup"><span data-stu-id="64f1e-2415">IP Address</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-2416">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-2416">Format</span></span>

#### <a name="ipv4"></a><span data-ttu-id="64f1e-2417">IPv6</span><span class="sxs-lookup"><span data-stu-id="64f1e-2417">IPv4:</span></span>
<span data-ttu-id="64f1e-2418">Modèle complexe qui tient compte des versions mises en forme (points) et non mises en forme (sans points) des adresses IPv4</span><span class="sxs-lookup"><span data-stu-id="64f1e-2418">Complex pattern which accounts for formatted (periods) and unformatted (no periods) versions of the IPv4 addresses</span></span>

#### <a name="ipv6"></a><span data-ttu-id="64f1e-2419">IPv4/IPv6</span><span class="sxs-lookup"><span data-stu-id="64f1e-2419">IPv6:</span></span>
<span data-ttu-id="64f1e-2420"> Modèle complexe qui tient compte des numéros IPv6 mis en forme (qui incluent les signes deux-points)</span><span class="sxs-lookup"><span data-stu-id="64f1e-2420">Complex pattern which accounts for formatted IPv6 numbers (which include colons)</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-2421">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2421">Pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-2422">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2422">Checksum</span></span>

<span data-ttu-id="64f1e-2423">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-2423">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-2424">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-2424">Definition</span></span>

<span data-ttu-id="64f1e-2425">Pour IPv6, le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2425">For IPv6, a DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-2426">L’expression régulière Regex_ipv6_address trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2426">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-2427">Aucun mot clé figurant dans la liste Keyword_ipaddress n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2427">No keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="64f1e-2428">Pour IPv4, le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 95 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2428">For IPv4, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-2429">L’expression régulière Regex_ipv4_address trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2429">The regular expression Regex_ipv4_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-2430">Un mot clé figurant dans la liste Keyword_ipaddress est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2430">A keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="64f1e-2431">Pour IPv6, le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 95 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2431">For IPv6, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-2432">L’expression régulière Regex_ipv6_address trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2432">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-2433">Aucun mot clé figurant dans la liste Keyword_ipaddress n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2433">No keyword from Keyword_ipaddress is found.</span></span>

```
    <!-- IP Address -->
    <Entity id="1daa4ad5-e2dd-4ca4-a788-54722c09efb2" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Regex_ipv6_address" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_ipaddress" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="95">
        <IdMatch idRef="Regex_ipv4_address" />
        <Any minMatches="1">
          <Match idRef="Keyword_ipaddress" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="95">
        <IdMatch idRef="Regex_ipv6_address" />
        <Any minMatches="1">
          <Match idRef="Keyword_ipaddress" />
        </Any>
      </Pattern>
    </Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-2434">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-2434">Keywords</span></span>

#### <a name="keywordipaddress"></a><span data-ttu-id="64f1e-2435">Keyword_ipaddress</span><span class="sxs-lookup"><span data-stu-id="64f1e-2435">Keyword_ipaddress</span></span>

- <span data-ttu-id="64f1e-2436">IP (ce mot clé respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="64f1e-2436">IP (this keyword is case sensitive)</span></span>
- <span data-ttu-id="64f1e-2437">ip address</span><span class="sxs-lookup"><span data-stu-id="64f1e-2437">ip address</span></span> 
- <span data-ttu-id="64f1e-2438">adresses IP</span><span class="sxs-lookup"><span data-stu-id="64f1e-2438">ip addresses</span></span>
- <span data-ttu-id="64f1e-2439">protocole internet</span><span class="sxs-lookup"><span data-stu-id="64f1e-2439">internet protocol</span></span>
- <span data-ttu-id="64f1e-2440">IP-כתובת ה</span><span class="sxs-lookup"><span data-stu-id="64f1e-2440">IP-כתובת ה</span></span> 
   
## <a name="international-classification-of-diseases-icd-10-cm"></a><span data-ttu-id="64f1e-2441">Classification internationale des maladies (ICD-10-CM)</span><span class="sxs-lookup"><span data-stu-id="64f1e-2441">International Classification of Diseases (ICD-10-CM)</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-2442">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-2442">Format</span></span>

<span data-ttu-id="64f1e-2443">Dictionary</span><span class="sxs-lookup"><span data-stu-id="64f1e-2443">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-2444">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2444">Pattern</span></span>

<span data-ttu-id="64f1e-2445">Mot clé</span><span class="sxs-lookup"><span data-stu-id="64f1e-2445">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-2446">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2446">Checksum</span></span>

<span data-ttu-id="64f1e-2447">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-2447">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-2448">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-2448">Definition</span></span>

<span data-ttu-id="64f1e-2449">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2449">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-2450">Un mot clé depuis Dictionary_icd_10_cm est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2450">A keyword from Dictionary_icd_10_cm is found.</span></span>

```
      <!-- ICD-10 CM -->
      <Entity id="3356946c-6bb7-449b-b253-6ffa419c0ce7" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_10_cm" />
        </Pattern>
      </Entity>
```

<span data-ttu-id="64f1e-2451">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-2451">Keywords</span></span>

<span data-ttu-id="64f1e-2452">Tout terme du dictionnaire de mots clés Dictionary_icd_10_cm, qui est basé sur la [Classification internationale des maladies, dixième révision, modification clinique (ICD-10-cm)](https://go.microsoft.com/fwlink/?linkid=852604).</span><span class="sxs-lookup"><span data-stu-id="64f1e-2452">Any term from the Dictionary_icd_10_cm keyword dictionary, which is based on the [International Classification of Diseases, Tenth Revision, Clinical Modification (ICD-10-CM)](https://go.microsoft.com/fwlink/?linkid=852604).</span></span> <span data-ttu-id="64f1e-2453">Ce type recherche uniquement le terme, pas les codes d'assurance.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2453">This type looks only for the term, not the insurance codes.</span></span>

   
## <a name="international-classification-of-diseases-icd-9-cm"></a><span data-ttu-id="64f1e-2454">Classification internationale des maladies (ICD-9-CM)</span><span class="sxs-lookup"><span data-stu-id="64f1e-2454">International Classification of Diseases (ICD-9-CM)</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-2455">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-2455">Format</span></span>

<span data-ttu-id="64f1e-2456">Dictionary</span><span class="sxs-lookup"><span data-stu-id="64f1e-2456">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-2457">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2457">Pattern</span></span>

<span data-ttu-id="64f1e-2458">Mot clé</span><span class="sxs-lookup"><span data-stu-id="64f1e-2458">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-2459">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2459">Checksum</span></span>

<span data-ttu-id="64f1e-2460">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-2460">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-2461">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-2461">Definition</span></span>

<span data-ttu-id="64f1e-2462">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2462">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-2463">Un mot clé depuis Dictionary_icd_9_cm est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2463">A keyword from Dictionary_icd_9_cm is found.</span></span>

```
      <Entity id="fa3f9c74-ee07-4c52-b5f2-085d6b2c0ec4" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_9_cm" />
        </Pattern>
      </Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-2464">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-2464">Keywords</span></span>

<span data-ttu-id="64f1e-2465">Tout terme du dictionnaire de mots clés Dictionary_icd_9_cm, qui est basé sur la [Classification internationale des maladies, neuvième révision, modification clinique (ICD-9-cm)](https://go.microsoft.com/fwlink/?linkid=852605).</span><span class="sxs-lookup"><span data-stu-id="64f1e-2465">Any term from the Dictionary_icd_9_cm keyword dictionary, which is based on the [International Classification of Diseases,Ninth Revision, Clinical Modification (ICD-9-CM)](https://go.microsoft.com/fwlink/?linkid=852605).</span></span> <span data-ttu-id="64f1e-2466">Ce type recherche uniquement le terme, pas les codes d'assurance.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2466">This type looks only for the term, not the insurance codes.</span></span>
   
## <a name="ireland-personal-public-service-pps-number"></a><span data-ttu-id="64f1e-2467">Numéro de service public personnel (PPS) Irlande</span><span class="sxs-lookup"><span data-stu-id="64f1e-2467">Ireland Personal Public Service (PPS) Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-2468">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-2468">Format</span></span>

<span data-ttu-id="64f1e-2469">Ancien format (jusqu'au 31 décembre 2012):</span><span class="sxs-lookup"><span data-stu-id="64f1e-2469">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="64f1e-2470">Sept chiffres suivis de 1 ou 2 lettres </span><span class="sxs-lookup"><span data-stu-id="64f1e-2470">Seven digits followed by 1-2 letters</span></span> 

<span data-ttu-id="64f1e-2471">Nouveau format (1er janvier 2013 et après):</span><span class="sxs-lookup"><span data-stu-id="64f1e-2471">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="64f1e-2472">Sept chiffres suivis de deux lettres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2472">Seven digits followed by two letters</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-2473">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2473">Pattern</span></span>

<span data-ttu-id="64f1e-2474">Ancien format (jusqu'au 31 décembre 2012):</span><span class="sxs-lookup"><span data-stu-id="64f1e-2474">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="64f1e-2475">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="64f1e-2475">Seven digits</span></span> 
- <span data-ttu-id="64f1e-2476">1 ou 2 lettres (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="64f1e-2476">1-2 letters (not case sensitive)</span></span> 

<span data-ttu-id="64f1e-2477">Nouveau format (1er janvier 2013 et après):</span><span class="sxs-lookup"><span data-stu-id="64f1e-2477">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="64f1e-2478">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="64f1e-2478">Seven digits</span></span> 
- <span data-ttu-id="64f1e-2479">Une lettre (ne respectant pas la casse), qui est un chiffre de contrôle alphabétique </span><span class="sxs-lookup"><span data-stu-id="64f1e-2479">A letter (not case sensitive) which is an alphabetic check digit</span></span> 
- <span data-ttu-id="64f1e-2480">La lettre « A » ou « H » (ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="64f1e-2480">The letter "A" or "H" (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-2481">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2481">Checksum</span></span>

<span data-ttu-id="64f1e-2482">Oui</span><span class="sxs-lookup"><span data-stu-id="64f1e-2482">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-2483">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-2483">Definition</span></span>

<span data-ttu-id="64f1e-2484">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2484">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-2485">La fonction Func_ireland_pps trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2485">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-2486">L’une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2486">One of the following is true:</span></span>
    - <span data-ttu-id="64f1e-2487">Un mot clé figurant dans la liste Keyword_ireland_pps est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2487">A keyword from Keyword_ireland_pps is found.</span></span>
    - <span data-ttu-id="64f1e-2488">La fonction Func_eu_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2488">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="64f1e-2489">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2489">The checksum passes.</span></span>

<span data-ttu-id="64f1e-2490">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2490">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-2491">La fonction Func_ireland_pps trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2491">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-2492">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2492">The checksum passes.</span></span>

```
<!-- Ireland Personal Public Service (PPS) Number -->
<Entity id="1cdb674d-c19a-4fcf-9f4b-7f56cc87345a" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_ireland_pps"/>
     <Any minMatches="1">
  <Match idRef="Keyword_ireland_pps"/>
  <Match idRef="Func_eu_date"/>
     </Any>
  </Pattern>
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Func_ireland_pps"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-2493">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-2493">Keywords</span></span>

#### <a name="keywordirelandpps"></a><span data-ttu-id="64f1e-2494">Keyword_ireland_pps</span><span class="sxs-lookup"><span data-stu-id="64f1e-2494">Keyword_ireland_pps</span></span>

- <span data-ttu-id="64f1e-2495">Personal Public Service Number</span><span class="sxs-lookup"><span data-stu-id="64f1e-2495">Personal Public Service Number</span></span> 
- <span data-ttu-id="64f1e-2496">PPS Number</span><span class="sxs-lookup"><span data-stu-id="64f1e-2496">PPS Number</span></span> 
- <span data-ttu-id="64f1e-2497">PPS Num</span><span class="sxs-lookup"><span data-stu-id="64f1e-2497">PPS Num</span></span> 
- <span data-ttu-id="64f1e-2498">PPS No.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2498">PPS No.</span></span> 
- <span data-ttu-id="64f1e-2499">PPS #</span><span class="sxs-lookup"><span data-stu-id="64f1e-2499">PPS #</span></span> 
- <span data-ttu-id="64f1e-2500">Spa</span><span class="sxs-lookup"><span data-stu-id="64f1e-2500">PPS#</span></span> 
- <span data-ttu-id="64f1e-2501">PPSN</span><span class="sxs-lookup"><span data-stu-id="64f1e-2501">PPSN</span></span> 
- <span data-ttu-id="64f1e-2502">Public Services Card</span><span class="sxs-lookup"><span data-stu-id="64f1e-2502">Public Services Card</span></span> 
- <span data-ttu-id="64f1e-2503">Uimhir Phearsanta Seirbhíse Poiblí</span><span class="sxs-lookup"><span data-stu-id="64f1e-2503">Uimhir Phearsanta Seirbhíse Poiblí</span></span> 
- <span data-ttu-id="64f1e-2504">Uimh.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2504">Uimh.</span></span> <span data-ttu-id="64f1e-2505">TOXINE</span><span class="sxs-lookup"><span data-stu-id="64f1e-2505">PSP</span></span> 
- <span data-ttu-id="64f1e-2506">TOXINE</span><span class="sxs-lookup"><span data-stu-id="64f1e-2506">PSP</span></span> 
   
## <a name="israel-bank-account-number"></a><span data-ttu-id="64f1e-2507">Numéro de compte bancaire Israël</span><span class="sxs-lookup"><span data-stu-id="64f1e-2507">Israel Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-2508">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-2508">Format</span></span>

<span data-ttu-id="64f1e-2509">13 chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2509">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-2510">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2510">Pattern</span></span>

<span data-ttu-id="64f1e-2511">Avec</span><span class="sxs-lookup"><span data-stu-id="64f1e-2511">Formatted:</span></span>
- <span data-ttu-id="64f1e-2512">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2512">Two digits</span></span> 
- <span data-ttu-id="64f1e-2513">Un tiret</span><span class="sxs-lookup"><span data-stu-id="64f1e-2513">A dash</span></span> 
- <span data-ttu-id="64f1e-2514">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2514">Three digits</span></span> 
- <span data-ttu-id="64f1e-2515">Un tiret</span><span class="sxs-lookup"><span data-stu-id="64f1e-2515">A dash</span></span> 
- <span data-ttu-id="64f1e-2516">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2516">Eight digits</span></span>

<span data-ttu-id="64f1e-2517">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-2517">Unformatted:</span></span>
- <span data-ttu-id="64f1e-2518">	13 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="64f1e-2518">13 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-2519">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2519">Checksum</span></span>

<span data-ttu-id="64f1e-2520">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-2520">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-2521">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-2521">Definition</span></span>

<span data-ttu-id="64f1e-2522">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2522">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-2523">L’expression régulière Regex_israel_bank_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2523">The regular expression Regex_israel_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-2524">Un mot clé figurant dans la liste Keyword_israel_bank_account_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2524">A keyword from Keyword_israel_bank_account_number is found.</span></span>

```
<!-- Israel Bank Account Number -->
<Entity id="7d08b2ff-a0b9-437f-957c-aeddbf9b2b25" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_israel_bank_account_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_israel_bank_account_number" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-2525">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-2525">Keywords</span></span>

#### <a name="keywordisraelbankaccountnumber"></a><span data-ttu-id="64f1e-2526">Keyword_israel_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="64f1e-2526">Keyword_israel_bank_account_number</span></span>

- <span data-ttu-id="64f1e-2527">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="64f1e-2527">Bank Account Number</span></span> 
- <span data-ttu-id="64f1e-2528">Bank Account</span><span class="sxs-lookup"><span data-stu-id="64f1e-2528">Bank Account</span></span> 
- <span data-ttu-id="64f1e-2529">Numéro de compte</span><span class="sxs-lookup"><span data-stu-id="64f1e-2529">Account Number</span></span> 
- <span data-ttu-id="64f1e-2530">מספר חשבון בנק</span><span class="sxs-lookup"><span data-stu-id="64f1e-2530">מספר חשבון בנק</span></span> 
   
## <a name="israel-national-id"></a><span data-ttu-id="64f1e-2531">Carte nationale d’identité Israël</span><span class="sxs-lookup"><span data-stu-id="64f1e-2531">Israel National ID</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-2532">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-2532">Format</span></span>

<span data-ttu-id="64f1e-2533">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2533">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-2534">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2534">Pattern</span></span>

<span data-ttu-id="64f1e-2535">Neuf chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="64f1e-2535">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-2536">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2536">Checksum</span></span>

<span data-ttu-id="64f1e-2537">Oui</span><span class="sxs-lookup"><span data-stu-id="64f1e-2537">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-2538">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-2538">Definition</span></span>

<span data-ttu-id="64f1e-2539">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2539">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-2540">La fonction Func_israeli_national_id_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2540">The function Func_israeli_national_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-2541">Un mot clé figurant dans la liste Keyword_Israel_National_ID est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2541">A keyword from Keyword_Israel_National_ID is found.</span></span>
- <span data-ttu-id="64f1e-2542">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2542">The checksum passes.</span></span>

```
<!-- Israel National ID Number -->
<Entity id="e05881f5-1db1-418c-89aa-a3ac5c5277ee" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_israeli_national_id_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_Israel_National_ID" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-2543">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-2543">Keywords</span></span>

#### <a name="keywordisraelnationalid"></a><span data-ttu-id="64f1e-2544">Keyword_Israel_National_ID</span><span class="sxs-lookup"><span data-stu-id="64f1e-2544">Keyword_Israel_National_ID</span></span>

- <span data-ttu-id="64f1e-2545">מספר זהות</span><span class="sxs-lookup"><span data-stu-id="64f1e-2545">מספר זהות</span></span> 
- <span data-ttu-id="64f1e-2546">Numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="64f1e-2546">National ID Number</span></span>
   
## <a name="italy-drivers-license-number"></a><span data-ttu-id="64f1e-2547">Numéro de permis de conduire Italie</span><span class="sxs-lookup"><span data-stu-id="64f1e-2547">Italy Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-2548">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-2548">Format</span></span>

<span data-ttu-id="64f1e-2549">Une combinaison de 10 lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2549">A combination of 10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-2550">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2550">Pattern</span></span>

- <span data-ttu-id="64f1e-2551">Une combinaison de 10 lettres et chiffres :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2551">A combination of 10 letters and digits:</span></span>
- <span data-ttu-id="64f1e-2552">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="64f1e-2552">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="64f1e-2553">La lettre « A » ou « V » (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="64f1e-2553">The letter "A" or "V" (not case sensitive)</span></span> 
- <span data-ttu-id="64f1e-2554">Sept lettres (ne respectent pas la casse), des chiffres ou le trait de soulignement</span><span class="sxs-lookup"><span data-stu-id="64f1e-2554">Seven letters (not case sensitive), digits, or the underscore character</span></span> 
- <span data-ttu-id="64f1e-2555">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="64f1e-2555">One letter (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-2556">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2556">Checksum</span></span>

<span data-ttu-id="64f1e-2557">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-2557">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-2558">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-2558">Definition</span></span>

<span data-ttu-id="64f1e-2559">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2559">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-2560">L’expression régulière Regex_italy_drivers_license_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2560">The regular expression Regex_italy_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-2561">Un mot clé figurant dans la liste Keyword_italy_drivers_license_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2561">A keyword from Keyword_italy_drivers_license_number is found.</span></span>

```
<!-- Italy Driver's license Number -->
<Entity id="97d6244f-9157-41bd-8e0c-9d669a5c4d71" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_italy_drivers_license_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_italy_drivers_license_number" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-2562">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-2562">Keywords</span></span>

#### <a name="keyworditalydriverslicensenumber"></a><span data-ttu-id="64f1e-2563">Keyword_italy_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="64f1e-2563">Keyword_italy_drivers_license_number</span></span>

- <span data-ttu-id="64f1e-2564">numero di patente di guida</span><span class="sxs-lookup"><span data-stu-id="64f1e-2564">numero di patente di guida</span></span> 
- <span data-ttu-id="64f1e-2565">patente di guida</span><span class="sxs-lookup"><span data-stu-id="64f1e-2565">patente di guida</span></span> 
   
## <a name="japan-bank-account-number"></a><span data-ttu-id="64f1e-2566">Numéro de compte bancaire Japon</span><span class="sxs-lookup"><span data-stu-id="64f1e-2566">Japan Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-2567">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-2567">Format</span></span>

<span data-ttu-id="64f1e-2568">Sept ou huit chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2568">Seven or eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-2569">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2569">Pattern</span></span>

<span data-ttu-id="64f1e-2570">Numéro de compte bancaire :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2570">Bank account number:</span></span>
- <span data-ttu-id="64f1e-2571">Sept ou huit chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2571">Seven or eight digits</span></span>
- <span data-ttu-id="64f1e-2572">Code guichet du compte bancaire :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2572">Bank account branch code:</span></span>
- <span data-ttu-id="64f1e-2573">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2573">Four digits</span></span> 
- <span data-ttu-id="64f1e-2574">Un espace ou un tiret (facultatif)</span><span class="sxs-lookup"><span data-stu-id="64f1e-2574">A space or dash (optional)</span></span> 
- <span data-ttu-id="64f1e-2575">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2575">Three digits</span></span>

<span data-ttu-id="64f1e-2576">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2576">Checksum</span></span>

<span data-ttu-id="64f1e-2577">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-2577">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-2578">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-2578">Definition</span></span>

<span data-ttu-id="64f1e-2579">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2579">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-2580">La fonction Func_jp_bank_account trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2580">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-2581">Un mot clé figurant dans la liste Keyword_jp_bank_account est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2581">A keyword from Keyword_jp_bank_account is found.</span></span>
- <span data-ttu-id="64f1e-2582">L’une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2582">One of the following is true:</span></span>
- <span data-ttu-id="64f1e-2583">La fonction Func_jp_bank_account_branch_code trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2583">The function Func_jp_bank_account_branch_code finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-2584">Un mot clé figurant dans la liste Keyword_jp_bank_branch_code est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2584">A keyword from Keyword_jp_bank_branch_code is found.</span></span>

<span data-ttu-id="64f1e-2585">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2585">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-2586">La fonction Func_jp_bank_account trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2586">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-2587">Un mot clé figurant dans la liste Keyword_jp_bank_account est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2587">A keyword from Keyword_jp_bank_account is found.</span></span>

```
<!-- Japan Bank Account Number -->
<Entity id="d354f95b-96ee-4b80-80bc-4377312b55bc" patternsProximity="300" recommendedConfidence="75">
  <Version minEngineVersion="15.01.0131.000">
    <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_jp_bank_account" />
          <Match idRef="Keyword_jp_bank_account" />
          <Any minMatches="1">
            <Match idRef="Func_jp_bank_account_branch_code" />
            <Match idRef="Keyword_jp_bank_branch_code" />
          </Any>
      </Pattern>
  </Version>    
     <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_bank_account" />
        <Match idRef="Keyword_jp_bank_account" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-2588">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-2588">Keywords</span></span>

#### <a name="keywordjpbankaccount"></a><span data-ttu-id="64f1e-2589">Keyword_jp_bank_account</span><span class="sxs-lookup"><span data-stu-id="64f1e-2589">Keyword_jp_bank_account</span></span>

- <span data-ttu-id="64f1e-2590">Numéro de compte courant</span><span class="sxs-lookup"><span data-stu-id="64f1e-2590">Checking Account Number</span></span> 
- <span data-ttu-id="64f1e-2591">Compte courant</span><span class="sxs-lookup"><span data-stu-id="64f1e-2591">Checking Account</span></span> 
- <span data-ttu-id="64f1e-2592"># compte courant</span><span class="sxs-lookup"><span data-stu-id="64f1e-2592">Checking Account #</span></span> 
- <span data-ttu-id="64f1e-2593">Numéro compte courant</span><span class="sxs-lookup"><span data-stu-id="64f1e-2593">Checking Acct Number</span></span> 
- <span data-ttu-id="64f1e-2594"># compte courant</span><span class="sxs-lookup"><span data-stu-id="64f1e-2594">Checking Acct #</span></span> 
- <span data-ttu-id="64f1e-2595">N° de compte courant</span><span class="sxs-lookup"><span data-stu-id="64f1e-2595">Checking Acct No.</span></span> 
- <span data-ttu-id="64f1e-2596">N° de compte courant</span><span class="sxs-lookup"><span data-stu-id="64f1e-2596">Checking Account No.</span></span> 
- <span data-ttu-id="64f1e-2597">Numéro de compte bancaire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2597">Bank Account Number</span></span> 
- <span data-ttu-id="64f1e-2598">Compte bancaire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2598">Bank Account</span></span> 
- <span data-ttu-id="64f1e-2599"># Compte bancaire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2599">Bank Account #</span></span> 
- <span data-ttu-id="64f1e-2600">Numéro de compte bancaire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2600">Bank Acct Number</span></span> 
- <span data-ttu-id="64f1e-2601"># Compte bancaire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2601">Bank Acct #</span></span> 
- <span data-ttu-id="64f1e-2602">N° de compte bancaire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2602">Bank Acct No.</span></span> 
- <span data-ttu-id="64f1e-2603">N° de compte bancaire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2603">Bank Account No.</span></span> 
- <span data-ttu-id="64f1e-2604">Numéro de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="64f1e-2604">Savings Account Number</span></span> 
- <span data-ttu-id="64f1e-2605">Compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="64f1e-2605">Savings Account</span></span> 
- <span data-ttu-id="64f1e-2606">N° de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="64f1e-2606">Savings Account #</span></span> 
- <span data-ttu-id="64f1e-2607">Numéro de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="64f1e-2607">Savings Acct Number</span></span> 
- <span data-ttu-id="64f1e-2608"># compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="64f1e-2608">Savings Acct #</span></span> 
- <span data-ttu-id="64f1e-2609">N° de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="64f1e-2609">Savings Acct No.</span></span> 
- <span data-ttu-id="64f1e-2610">N° de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="64f1e-2610">Savings Account No.</span></span> 
- <span data-ttu-id="64f1e-2611">Numéro de compte de débit</span><span class="sxs-lookup"><span data-stu-id="64f1e-2611">Debit Account Number</span></span> 
- <span data-ttu-id="64f1e-2612">Compte de débit</span><span class="sxs-lookup"><span data-stu-id="64f1e-2612">Debit Account</span></span> 
- <span data-ttu-id="64f1e-2613"># Compte de débit</span><span class="sxs-lookup"><span data-stu-id="64f1e-2613">Debit Account #</span></span> 
- <span data-ttu-id="64f1e-2614">Numéro de compte de débit</span><span class="sxs-lookup"><span data-stu-id="64f1e-2614">Debit Acct Number</span></span> 
- <span data-ttu-id="64f1e-2615"># Compte de débit</span><span class="sxs-lookup"><span data-stu-id="64f1e-2615">Debit Acct #</span></span> 
- <span data-ttu-id="64f1e-2616">N° de compte de débit</span><span class="sxs-lookup"><span data-stu-id="64f1e-2616">Debit Acct No.</span></span> 
- <span data-ttu-id="64f1e-2617">N° de compte de débit</span><span class="sxs-lookup"><span data-stu-id="64f1e-2617">Debit Account No.</span></span> 
- <span data-ttu-id="64f1e-2618">口座番号を当座預金口座の確認</span><span class="sxs-lookup"><span data-stu-id="64f1e-2618">口座番号を当座預金口座の確認</span></span> 
- <span data-ttu-id="64f1e-2619">#アカウントの確認 、 勘定番号の確認</span><span class="sxs-lookup"><span data-stu-id="64f1e-2619">＃アカウントの確認、勘定番号の確認</span></span> 
- <span data-ttu-id="64f1e-2620">#勘定の確認</span><span class="sxs-lookup"><span data-stu-id="64f1e-2620">＃勘定の確認</span></span> 
- <span data-ttu-id="64f1e-2621">勘定番号の確認</span><span class="sxs-lookup"><span data-stu-id="64f1e-2621">勘定番号の確認</span></span> 
- <span data-ttu-id="64f1e-2622">口座番号の確認</span><span class="sxs-lookup"><span data-stu-id="64f1e-2622">口座番号の確認</span></span> 
- <span data-ttu-id="64f1e-2623">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="64f1e-2623">銀行口座番号</span></span> 
- <span data-ttu-id="64f1e-2624">銀行口座</span><span class="sxs-lookup"><span data-stu-id="64f1e-2624">銀行口座</span></span> 
- <span data-ttu-id="64f1e-2625">銀行口座 #</span><span class="sxs-lookup"><span data-stu-id="64f1e-2625">銀行口座＃</span></span> 
- <span data-ttu-id="64f1e-2626">銀行の勘定番号</span><span class="sxs-lookup"><span data-stu-id="64f1e-2626">銀行の勘定番号</span></span> 
- <span data-ttu-id="64f1e-2627">銀行のacct #</span><span class="sxs-lookup"><span data-stu-id="64f1e-2627">銀行のacct＃</span></span> 
- <span data-ttu-id="64f1e-2628">銀行の勘定いいえ</span><span class="sxs-lookup"><span data-stu-id="64f1e-2628">銀行の勘定いいえ</span></span> 
- <span data-ttu-id="64f1e-2629">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="64f1e-2629">銀行口座番号</span></span>
- <span data-ttu-id="64f1e-2630">普通預金口座番号</span><span class="sxs-lookup"><span data-stu-id="64f1e-2630">普通預金口座番号</span></span> 
- <span data-ttu-id="64f1e-2631">預金口座</span><span class="sxs-lookup"><span data-stu-id="64f1e-2631">預金口座</span></span> 
- <span data-ttu-id="64f1e-2632">貯蓄口座 #</span><span class="sxs-lookup"><span data-stu-id="64f1e-2632">貯蓄口座＃</span></span> 
- <span data-ttu-id="64f1e-2633">貯蓄勘定の数</span><span class="sxs-lookup"><span data-stu-id="64f1e-2633">貯蓄勘定の数</span></span> 
- <span data-ttu-id="64f1e-2634">貯蓄勘定 #</span><span class="sxs-lookup"><span data-stu-id="64f1e-2634">貯蓄勘定＃</span></span> 
- <span data-ttu-id="64f1e-2635">貯蓄勘定番号</span><span class="sxs-lookup"><span data-stu-id="64f1e-2635">貯蓄勘定番号</span></span> 
- <span data-ttu-id="64f1e-2636">普通預金口座番号</span><span class="sxs-lookup"><span data-stu-id="64f1e-2636">普通預金口座番号</span></span> 
- <span data-ttu-id="64f1e-2637">引き落とし口座番号</span><span class="sxs-lookup"><span data-stu-id="64f1e-2637">引き落とし口座番号</span></span> 
- <span data-ttu-id="64f1e-2638">口座番号</span><span class="sxs-lookup"><span data-stu-id="64f1e-2638">口座番号</span></span> 
- <span data-ttu-id="64f1e-2639">口座番号 #</span><span class="sxs-lookup"><span data-stu-id="64f1e-2639">口座番号＃</span></span> 
- <span data-ttu-id="64f1e-2640">デビットのacct番号</span><span class="sxs-lookup"><span data-stu-id="64f1e-2640">デビットのacct番号</span></span> 
- <span data-ttu-id="64f1e-2641">デビット勘定 #</span><span class="sxs-lookup"><span data-stu-id="64f1e-2641">デビット勘定＃</span></span> 
- <span data-ttu-id="64f1e-2642">デビットACCTの番号</span><span class="sxs-lookup"><span data-stu-id="64f1e-2642">デビットACCTの番号</span></span> 
- <span data-ttu-id="64f1e-2643">デビット口座番号</span><span class="sxs-lookup"><span data-stu-id="64f1e-2643">デビット口座番号</span></span> 

#### <a name="keywordjpbankbranchcode"></a><span data-ttu-id="64f1e-2644">Keyword_jp_bank_branch_code</span><span class="sxs-lookup"><span data-stu-id="64f1e-2644">Keyword_jp_bank_branch_code</span></span>

<span data-ttu-id="64f1e-2645">Otemachi</span><span class="sxs-lookup"><span data-stu-id="64f1e-2645">Otemachi</span></span>

## <a name="japan-drivers-license-number"></a><span data-ttu-id="64f1e-2646">Numéro de permis de conduire Japon</span><span class="sxs-lookup"><span data-stu-id="64f1e-2646">Japan Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-2647">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-2647">Format</span></span>

<span data-ttu-id="64f1e-2648">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2648">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-2649">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2649">Pattern</span></span>

<span data-ttu-id="64f1e-2650">12 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="64f1e-2650">12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-2651">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2651">Checksum</span></span>

<span data-ttu-id="64f1e-2652">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-2652">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-2653">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-2653">Definition</span></span>

<span data-ttu-id="64f1e-2654">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2654">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-2655">La fonction Func_jp_drivers_license_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2655">The function Func_jp_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-2656">Un mot clé figurant dans la liste Keyword_jp_drivers_license_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2656">A keyword from Keyword_jp_drivers_license_number is found.</span></span>

```
<!-- Japan Driver's License Number -->
<Entity id="c6011143-d087-451c-8313-7f6d4aed2270" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_drivers_license_number" />
        <Match idRef ="Keyword_jp_drivers_license_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-2657">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-2657">Keywords</span></span>

#### <a name="keywordjpdriverslicensenumber"></a><span data-ttu-id="64f1e-2658">Keyword_jp_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="64f1e-2658">Keyword_jp_drivers_license_number</span></span>

- <span data-ttu-id="64f1e-2659">LD</span><span class="sxs-lookup"><span data-stu-id="64f1e-2659">dl#</span></span> 
- <span data-ttu-id="64f1e-2660">LD</span><span class="sxs-lookup"><span data-stu-id="64f1e-2660">DL＃</span></span> 
- <span data-ttu-id="64f1e-2661">distribution</span><span class="sxs-lookup"><span data-stu-id="64f1e-2661">dls#</span></span> 
- <span data-ttu-id="64f1e-2662">DISTRIBUTION</span><span class="sxs-lookup"><span data-stu-id="64f1e-2662">DLS＃</span></span> 
- <span data-ttu-id="64f1e-2663">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2663">driver license</span></span> 
- <span data-ttu-id="64f1e-2664">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2664">driver licenses</span></span> 
- <span data-ttu-id="64f1e-2665">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2665">drivers license</span></span> 
- <span data-ttu-id="64f1e-2666">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2666">driver's license</span></span> 
- <span data-ttu-id="64f1e-2667">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2667">drivers licenses</span></span> 
- <span data-ttu-id="64f1e-2668">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2668">driver's licenses</span></span> 
- <span data-ttu-id="64f1e-2669">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2669">driving licence</span></span> 
- <span data-ttu-id="64f1e-2670">Profil</span><span class="sxs-lookup"><span data-stu-id="64f1e-2670">lic#</span></span> 
- <span data-ttu-id="64f1e-2671">Profil</span><span class="sxs-lookup"><span data-stu-id="64f1e-2671">LIC＃</span></span> 
- <span data-ttu-id="64f1e-2672">conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-2672">lics#</span></span> 
- <span data-ttu-id="64f1e-2673">id d’état</span><span class="sxs-lookup"><span data-stu-id="64f1e-2673">state id</span></span> 
- <span data-ttu-id="64f1e-2674">identification d’état</span><span class="sxs-lookup"><span data-stu-id="64f1e-2674">state identification</span></span> 
- <span data-ttu-id="64f1e-2675">numéro d’identification d’état</span><span class="sxs-lookup"><span data-stu-id="64f1e-2675">state identification number</span></span> 
- <span data-ttu-id="64f1e-2676">低所得国 #</span><span class="sxs-lookup"><span data-stu-id="64f1e-2676">低所得国＃</span></span> 
- <span data-ttu-id="64f1e-2677">免許証</span><span class="sxs-lookup"><span data-stu-id="64f1e-2677">免許証</span></span> 
- <span data-ttu-id="64f1e-2678">状態ID</span><span class="sxs-lookup"><span data-stu-id="64f1e-2678">状態ID</span></span>
- <span data-ttu-id="64f1e-2679">状態の識別</span><span class="sxs-lookup"><span data-stu-id="64f1e-2679">状態の識別</span></span> 
- <span data-ttu-id="64f1e-2680">状態の識別番号</span><span class="sxs-lookup"><span data-stu-id="64f1e-2680">状態の識別番号</span></span> 
- <span data-ttu-id="64f1e-2681">運転免許</span><span class="sxs-lookup"><span data-stu-id="64f1e-2681">運転免許</span></span> 
- <span data-ttu-id="64f1e-2682">運転免許証</span><span class="sxs-lookup"><span data-stu-id="64f1e-2682">運転免許証</span></span> 
- <span data-ttu-id="64f1e-2683">運転免許証番号</span><span class="sxs-lookup"><span data-stu-id="64f1e-2683">運転免許証番号</span></span> 
   
## <a name="japan-passport-number"></a><span data-ttu-id="64f1e-2684">Numéro de passeport Japon</span><span class="sxs-lookup"><span data-stu-id="64f1e-2684">Japan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-2685">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-2685">Format</span></span>

<span data-ttu-id="64f1e-2686">Deux lettres suivies de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2686">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-2687">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2687">Pattern</span></span>

<span data-ttu-id="64f1e-2688">Deux lettres (ne respectant pas la casse) suivies de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2688">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-2689">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2689">Checksum</span></span>

<span data-ttu-id="64f1e-2690">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-2690">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-2691">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-2691">Definition</span></span>

<span data-ttu-id="64f1e-2692">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2692">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-2693">La fonction Func_jp_passport trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2693">The function Func_jp_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-2694">Un mot clé figurant dans la liste Keyword_jp_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2694">A keyword from Keyword_jp_passport is found.</span></span>

```
<!-- Japan Passport Number -->
<Entity id="75177310-1a09-4613-bf6d-833aae3743f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_passport" />
        <Match idRef="Keyword_jp_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-2695">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-2695">Keywords</span></span>

#### <a name="keywordjppassport"></a><span data-ttu-id="64f1e-2696">Keyword_jp_passport</span><span class="sxs-lookup"><span data-stu-id="64f1e-2696">Keyword_jp_passport</span></span>

- <span data-ttu-id="64f1e-2697">パスポート</span><span class="sxs-lookup"><span data-stu-id="64f1e-2697">パスポート</span></span> 
- <span data-ttu-id="64f1e-2698">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="64f1e-2698">パスポート番号</span></span> 
- <span data-ttu-id="64f1e-2699">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="64f1e-2699">パスポートのNum</span></span> 
- <span data-ttu-id="64f1e-2700">パスポート #</span><span class="sxs-lookup"><span data-stu-id="64f1e-2700">パスポート＃</span></span> 
   
## <a name="japan-resident-registration-number"></a><span data-ttu-id="64f1e-2701">Matricule de résident Japon</span><span class="sxs-lookup"><span data-stu-id="64f1e-2701">Japan Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-2702">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-2702">Format</span></span>

<span data-ttu-id="64f1e-2703">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2703">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-2704">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2704">Pattern</span></span>

<span data-ttu-id="64f1e-2705">11 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="64f1e-2705">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-2706">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2706">Checksum</span></span>

<span data-ttu-id="64f1e-2707">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-2707">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-2708">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-2708">Definition</span></span>

<span data-ttu-id="64f1e-2709">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2709">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-2710">La fonction Func_jp_resident_registration_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2710">The function Func_jp_resident_registration_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-2711">Un mot clé figurant dans la liste Keyword_jp_resident_registration_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2711">A keyword from Keyword_jp_resident_registration_number is found.</span></span>

```
<!-- Japan Resident Registration Number -->
<Entity id="01c1209b-6389-4faf-a5f8-3f7e13899652" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_resident_registration_number" />
        <Match idRef ="Keyword_jp_resident_registration_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-2712">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-2712">Keywords</span></span>

#### <a name="keywordjpresidentregistrationnumber"></a><span data-ttu-id="64f1e-2713">Keyword_jp_resident_registration_number</span><span class="sxs-lookup"><span data-stu-id="64f1e-2713">Keyword_jp_resident_registration_number</span></span>

- <span data-ttu-id="64f1e-2714">Numéro d’enregistrement du résident</span><span class="sxs-lookup"><span data-stu-id="64f1e-2714">Resident Registration Number</span></span>
- <span data-ttu-id="64f1e-2715">Numéro d’enregistrement du résident</span><span class="sxs-lookup"><span data-stu-id="64f1e-2715">Resident Register Number</span></span> 
- <span data-ttu-id="64f1e-2716">Numéro de base d’enregistrement des résidents</span><span class="sxs-lookup"><span data-stu-id="64f1e-2716">Residents Basic Registry Number</span></span> 
- <span data-ttu-id="64f1e-2717">N° d’enregistrement du résident</span><span class="sxs-lookup"><span data-stu-id="64f1e-2717">Resident Registration No.</span></span> 
- <span data-ttu-id="64f1e-2718">N° d’enregistrement du résident</span><span class="sxs-lookup"><span data-stu-id="64f1e-2718">Resident Register No.</span></span> 
- <span data-ttu-id="64f1e-2719">N° de base d’enregistrement des résidents</span><span class="sxs-lookup"><span data-stu-id="64f1e-2719">Residents Basic Registry No.</span></span> 
- <span data-ttu-id="64f1e-2720">N° d’enregistrement du résident de base</span><span class="sxs-lookup"><span data-stu-id="64f1e-2720">Basic Resident Register No.</span></span> 
- <span data-ttu-id="64f1e-2721">住民登録番号 、 登録番号をレジデント</span><span class="sxs-lookup"><span data-stu-id="64f1e-2721">住民登録番号、登録番号をレジデント</span></span> 
- <span data-ttu-id="64f1e-2722">住民基本登録番号 、 登録番号</span><span class="sxs-lookup"><span data-stu-id="64f1e-2722">住民基本登録番号、登録番号</span></span> 
- <span data-ttu-id="64f1e-2723">住民基本レジストリ番号を常駐</span><span class="sxs-lookup"><span data-stu-id="64f1e-2723">住民基本レジストリ番号を常駐</span></span> 
- <span data-ttu-id="64f1e-2724">登録番号を常駐住民基本台帳登録番号</span><span class="sxs-lookup"><span data-stu-id="64f1e-2724">登録番号を常駐住民基本台帳登録番号</span></span> 

   
## <a name="japan-social-insurance-number-sin"></a><span data-ttu-id="64f1e-2725">Numéro d’assurance sociale Japon</span><span class="sxs-lookup"><span data-stu-id="64f1e-2725">Japan Social Insurance Number (SIN)</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-2726">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-2726">Format</span></span>

<span data-ttu-id="64f1e-2727">7 à 12 chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2727">7-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-2728">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2728">Pattern</span></span>

<span data-ttu-id="64f1e-2729">7 à 12 chiffres :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2729">7-12 digits:</span></span>
- <span data-ttu-id="64f1e-2730">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2730">Four digits</span></span> 
- <span data-ttu-id="64f1e-2731">Un trait d’union (facultatif)</span><span class="sxs-lookup"><span data-stu-id="64f1e-2731">A hyphen (optional)</span></span> 
- <span data-ttu-id="64f1e-2732">Six chiffres ou</span><span class="sxs-lookup"><span data-stu-id="64f1e-2732">Six digits OR</span></span>
- <span data-ttu-id="64f1e-2733">7 à 12 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="64f1e-2733">7-12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-2734">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2734">Checksum</span></span>

<span data-ttu-id="64f1e-2735">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-2735">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-2736">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-2736">Definition</span></span>

<span data-ttu-id="64f1e-2737">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2737">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-2738">La fonction Func_jp_sin trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2738">The function Func_jp_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-2739">Un mot clé figurant dans la liste Keyword_jp_sin est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2739">A keyword from Keyword_jp_sin is found.</span></span>

<span data-ttu-id="64f1e-2740">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2740">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-2741">La fonction Func_jp_sin_pre_1997 trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2741">The function Func_jp_sin_pre_1997 finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-2742">Un mot clé figurant dans la liste Keyword_jp_sin est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2742">A keyword from Keyword_jp_sin is found.</span></span>

```
<!-- Japan Social Insurance Number -->
<Entity id="c840e719-0896-45bb-84fd-1ed5c95e45ff" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_jp_sin" />
        <Match idRef="Keyword_jp_sin" />
    </Pattern>
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_sin_pre_1997" />
        <Match idRef="Keyword_jp_sin" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-2743">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-2743">Keywords</span></span>

#### <a name="keywordjpsin"></a><span data-ttu-id="64f1e-2744">Keyword_jp_sin</span><span class="sxs-lookup"><span data-stu-id="64f1e-2744">Keyword_jp_sin</span></span>

- <span data-ttu-id="64f1e-2745">N° d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="64f1e-2745">Social Insurance No.</span></span> 
- <span data-ttu-id="64f1e-2746">Numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="64f1e-2746">Social Insurance Num</span></span> 
- <span data-ttu-id="64f1e-2747">Numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="64f1e-2747">Social Insurance Number</span></span> 
- <span data-ttu-id="64f1e-2748">社会保険のテンキー</span><span class="sxs-lookup"><span data-stu-id="64f1e-2748">社会保険のテンキー</span></span> 
- <span data-ttu-id="64f1e-2749">社会保険番号</span><span class="sxs-lookup"><span data-stu-id="64f1e-2749">社会保険番号</span></span> 

## <a name="japanese-residence-card-number"></a><span data-ttu-id="64f1e-2750">Numéro de carte de séjour japonaise</span><span class="sxs-lookup"><span data-stu-id="64f1e-2750">Japanese Residence Card Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-2751">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-2751">Format</span></span>

<span data-ttu-id="64f1e-2752">12 lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2752">12 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-2753">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2753">Pattern</span></span>

<span data-ttu-id="64f1e-2754">12 lettres et chiffres:</span><span class="sxs-lookup"><span data-stu-id="64f1e-2754">12 letters and digits:</span></span>
- <span data-ttu-id="64f1e-2755">Deux lettres (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="64f1e-2755">Two letters (not case sensitive)</span></span>
- <span data-ttu-id="64f1e-2756">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2756">Eight digits</span></span> 
- <span data-ttu-id="64f1e-2757">Deux lettres (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="64f1e-2757">Two letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-2758">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2758">Checksum</span></span>

<span data-ttu-id="64f1e-2759">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-2759">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-2760">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-2760">Definition</span></span>

<span data-ttu-id="64f1e-2761">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2761">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-2762">L'expression régulière Regex_jp_residence_card_number trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2762">The regular expression Regex_jp_residence_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-2763">Un mot clé depuis Keyword_jp_residence_card_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2763">A keyword from Keyword_jp_residence_card_number is found.</span></span>

```
<!--Japan Residence Card Number-->
-<Entity id="ac36fef2-a289-4e2c-bb48-b02366e89fc0" recommendedConfidence="75" patternsProximity="300">
   -<Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_jp_residence_card_number"/>
      <Match idRef="Keyword_jp_residence_card_number"/>
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-2764">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-2764">Keywords</span></span>

#### <a name="keywordjpresidencecardnumber"></a><span data-ttu-id="64f1e-2765">Keyword_jp_residence_card_number</span><span class="sxs-lookup"><span data-stu-id="64f1e-2765">Keyword_jp_residence_card_number</span></span>

- <span data-ttu-id="64f1e-2766">Numéro de carte de séjour</span><span class="sxs-lookup"><span data-stu-id="64f1e-2766">Residence card number</span></span>
- <span data-ttu-id="64f1e-2767">N ° carte de séjour</span><span class="sxs-lookup"><span data-stu-id="64f1e-2767">Residence card no</span></span>
- <span data-ttu-id="64f1e-2768">N ° de carte de séjour</span><span class="sxs-lookup"><span data-stu-id="64f1e-2768">Residence card #</span></span>
- <span data-ttu-id="64f1e-2769">在留カード番号</span><span class="sxs-lookup"><span data-stu-id="64f1e-2769">在留カード番号</span></span>
   
## <a name="malaysia-id-card-number"></a><span data-ttu-id="64f1e-2770">Numéro de carte d’identité Malaisie</span><span class="sxs-lookup"><span data-stu-id="64f1e-2770">Malaysia ID Card Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-2771">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-2771">Format</span></span>

<span data-ttu-id="64f1e-2772">12 chiffres contenant éventuellement des traits d’union</span><span class="sxs-lookup"><span data-stu-id="64f1e-2772">12 digits containing optional hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-2773">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2773">Pattern</span></span>

<span data-ttu-id="64f1e-2774">12 chiffres :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2774">12 digits:</span></span>
- <span data-ttu-id="64f1e-2775">Six chiffres au format AAMMJJ correspondant à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="64f1e-2775">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="64f1e-2776">Un tiret (facultatif) </span><span class="sxs-lookup"><span data-stu-id="64f1e-2776">A dash (optional)</span></span> 
- <span data-ttu-id="64f1e-2777">Le code à deux lettres du lieu de naissance </span><span class="sxs-lookup"><span data-stu-id="64f1e-2777">Two-letter place-of-birth code</span></span> 
- <span data-ttu-id="64f1e-2778">Un tiret (facultatif) </span><span class="sxs-lookup"><span data-stu-id="64f1e-2778">A dash (optional)</span></span> 
- <span data-ttu-id="64f1e-2779">Trois chiffres aléatoires </span><span class="sxs-lookup"><span data-stu-id="64f1e-2779">Three random digits</span></span> 
- <span data-ttu-id="64f1e-2780">Code de sexe à un chiffre</span><span class="sxs-lookup"><span data-stu-id="64f1e-2780">One-digit gender code</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-2781">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2781">Checksum</span></span>

<span data-ttu-id="64f1e-2782">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-2782">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-2783">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-2783">Definition</span></span>

<span data-ttu-id="64f1e-2784">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2784">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-2785">L’expression régulière Regex_malaysia_id_card_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2785">The regular expression Regex_malaysia_id_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-2786">Un mot clé figurant dans la liste Keyword_malaysia_id_card_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2786">A keyword from Keyword_malaysia_id_card_number is found.</span></span>

```
<!-- Malaysia ID Card Number -->
</Entity>
      <Entity id="7f0e921c-9677-435b-aba2-bb8f1013c749" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
            <IdMatch idRef="Regex_malaysia_id_card_number" />
            <Match idRef="Keyword_malaysia_id_card_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-2787">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-2787">Keywords</span></span>
   
#### <a name="keywordmalaysiaidcardnumber"></a><span data-ttu-id="64f1e-2788">Keyword_malaysia_id_card_number</span><span class="sxs-lookup"><span data-stu-id="64f1e-2788">Keyword_malaysia_id_card_number</span></span>

- <span data-ttu-id="64f1e-2789">carte d'application numérique</span><span class="sxs-lookup"><span data-stu-id="64f1e-2789">digital application card</span></span>
- <span data-ttu-id="64f1e-2790">i/c</span><span class="sxs-lookup"><span data-stu-id="64f1e-2790">i/c</span></span>
- <span data-ttu-id="64f1e-2791">n ° i/c non</span><span class="sxs-lookup"><span data-stu-id="64f1e-2791">i/c no</span></span>
- <span data-ttu-id="64f1e-2792">combustion</span><span class="sxs-lookup"><span data-stu-id="64f1e-2792">ic</span></span>
- <span data-ttu-id="64f1e-2793">n ° IC</span><span class="sxs-lookup"><span data-stu-id="64f1e-2793">ic no</span></span>
- <span data-ttu-id="64f1e-2794">carte d’identité</span><span class="sxs-lookup"><span data-stu-id="64f1e-2794">id card</span></span>
- <span data-ttu-id="64f1e-2795">Carte d'identification</span><span class="sxs-lookup"><span data-stu-id="64f1e-2795">identification Card</span></span>
- <span data-ttu-id="64f1e-2796">Carte d’identité</span><span class="sxs-lookup"><span data-stu-id="64f1e-2796">identity card</span></span>
- <span data-ttu-id="64f1e-2797">k/p</span><span class="sxs-lookup"><span data-stu-id="64f1e-2797">k/p</span></span>
- <span data-ttu-id="64f1e-2798">n ° k/p</span><span class="sxs-lookup"><span data-stu-id="64f1e-2798">k/p no</span></span>
- <span data-ttu-id="64f1e-2799">Kad akuan diri</span><span class="sxs-lookup"><span data-stu-id="64f1e-2799">kad akuan diri</span></span>
- <span data-ttu-id="64f1e-2800">Kad aplikasi numérique</span><span class="sxs-lookup"><span data-stu-id="64f1e-2800">kad aplikasi digital</span></span>
- <span data-ttu-id="64f1e-2801">Kad Pengenalan Malaisie</span><span class="sxs-lookup"><span data-stu-id="64f1e-2801">kad pengenalan malaysia</span></span>
- <span data-ttu-id="64f1e-2802">kgf</span><span class="sxs-lookup"><span data-stu-id="64f1e-2802">kp</span></span>
- <span data-ttu-id="64f1e-2803">KP non</span><span class="sxs-lookup"><span data-stu-id="64f1e-2803">kp no</span></span>
- <span data-ttu-id="64f1e-2804">MyKad</span><span class="sxs-lookup"><span data-stu-id="64f1e-2804">mykad</span></span>
- <span data-ttu-id="64f1e-2805">mykas</span><span class="sxs-lookup"><span data-stu-id="64f1e-2805">mykas</span></span>
- <span data-ttu-id="64f1e-2806">MyKid</span><span class="sxs-lookup"><span data-stu-id="64f1e-2806">mykid</span></span>
- <span data-ttu-id="64f1e-2807">mypr</span><span class="sxs-lookup"><span data-stu-id="64f1e-2807">mypr</span></span>
- <span data-ttu-id="64f1e-2808">mytentera</span><span class="sxs-lookup"><span data-stu-id="64f1e-2808">mytentera</span></span>
- <span data-ttu-id="64f1e-2809">carte d'identité Malaisie</span><span class="sxs-lookup"><span data-stu-id="64f1e-2809">malaysia identity card</span></span>
- <span data-ttu-id="64f1e-2810">carte d'identité malais</span><span class="sxs-lookup"><span data-stu-id="64f1e-2810">malaysian identity card</span></span>
- <span data-ttu-id="64f1e-2811">NRIC</span><span class="sxs-lookup"><span data-stu-id="64f1e-2811">nric</span></span>
- <span data-ttu-id="64f1e-2812">carte d'identification personnelle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2812">personal identification card</span></span>
   
## <a name="netherlands-citizens-service-bsn-number"></a><span data-ttu-id="64f1e-2813">Numéro de service du citoyen (BSN) Pays-Bas</span><span class="sxs-lookup"><span data-stu-id="64f1e-2813">Netherlands Citizen's Service (BSN) Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-2814">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-2814">Format</span></span>

<span data-ttu-id="64f1e-2815">8 à 9 chiffres contenant éventuellement des espaces</span><span class="sxs-lookup"><span data-stu-id="64f1e-2815">8-9 digits containing optional spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-2816">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2816">Pattern</span></span>

<span data-ttu-id="64f1e-2817">8 à 9 chiffres :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2817">8-9 digits:</span></span>
- <span data-ttu-id="64f1e-2818">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2818">Three digits</span></span> 
- <span data-ttu-id="64f1e-2819">Un espace (facultatif) </span><span class="sxs-lookup"><span data-stu-id="64f1e-2819">A space (optional)</span></span> 
- <span data-ttu-id="64f1e-2820">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2820">Three digits</span></span> 
- <span data-ttu-id="64f1e-2821">Un espace (facultatif) </span><span class="sxs-lookup"><span data-stu-id="64f1e-2821">A space (optional)</span></span> 
- <span data-ttu-id="64f1e-2822">2 à 3 chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2822">2-3 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-2823">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2823">Checksum</span></span>

<span data-ttu-id="64f1e-2824">Oui</span><span class="sxs-lookup"><span data-stu-id="64f1e-2824">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-2825">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-2825">Definition</span></span>

<span data-ttu-id="64f1e-2826">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2826">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-2827">La fonction Func_netherlands_bsn trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2827">The function Func_netherlands_bsn finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-2828">Un mot clé figurant dans la liste Keyword_netherlands_bsn est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2828">A keyword from Keyword_netherlands_bsn is found.</span></span>
- <span data-ttu-id="64f1e-2829">La fonction Func_eu_date2 trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2829">The function Func_eu_date2 finds a date in the right date format.</span></span>
- <span data-ttu-id="64f1e-2830">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2830">The checksum passes.</span></span>

```
<!-- Netherlands Citizen's Service (BSN) Number -->
<Entity id="c5f54253-ef7e-44f6-a578-440ed67e946d" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
       <IdMatch idRef="Func_netherlands_bsn" /> 
       <Match idRef="Keyword_netherlands_bsn" /> 
       <Match idRef="Func_eu_date2" /> 
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-2831">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-2831">Keywords</span></span>

#### <a name="keywordnetherlandsbsn"></a><span data-ttu-id="64f1e-2832">Keyword_netherlands_bsn</span><span class="sxs-lookup"><span data-stu-id="64f1e-2832">Keyword_netherlands_bsn</span></span>

- <span data-ttu-id="64f1e-2833">Citizen service number</span><span class="sxs-lookup"><span data-stu-id="64f1e-2833">Citizen service number</span></span> 
- <span data-ttu-id="64f1e-2834">BSN</span><span class="sxs-lookup"><span data-stu-id="64f1e-2834">BSN</span></span> 
- <span data-ttu-id="64f1e-2835">Burgerservicenummer</span><span class="sxs-lookup"><span data-stu-id="64f1e-2835">Burgerservicenummer</span></span> 
- <span data-ttu-id="64f1e-2836">Sofinummer</span><span class="sxs-lookup"><span data-stu-id="64f1e-2836">Sofinummer</span></span> 
- <span data-ttu-id="64f1e-2837">Persoonsgebonden nummer</span><span class="sxs-lookup"><span data-stu-id="64f1e-2837">Persoonsgebonden nummer</span></span> 
- <span data-ttu-id="64f1e-2838">Persoonsnummer</span><span class="sxs-lookup"><span data-stu-id="64f1e-2838">Persoonsnummer</span></span>    

   
## <a name="new-zealand-ministry-of-health-number"></a><span data-ttu-id="64f1e-2839">Numéro du Ministère de la santé Nouvelle-Zélande</span><span class="sxs-lookup"><span data-stu-id="64f1e-2839">New Zealand Ministry of Health Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-2840">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-2840">Format</span></span>

<span data-ttu-id="64f1e-2841">Trois lettres, un espace (facultatif) et quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2841">Three letters, a space (optional), and four digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-2842">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2842">Pattern</span></span>

<span data-ttu-id="64f1e-2843">Trois lettres (ne respectant pas la casse) un espace (facultatif) quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2843">Three letters (not case sensitive) a space (optional) four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-2844">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2844">Checksum</span></span>

<span data-ttu-id="64f1e-2845">Oui</span><span class="sxs-lookup"><span data-stu-id="64f1e-2845">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-2846">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-2846">Definition</span></span>

<span data-ttu-id="64f1e-2847">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2847">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-2848">La fonction Func_new_zealand_ministry_of_health_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2848">The function Func_new_zealand_ministry_of_health_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-2849">Un mot clé figurant dans la liste Keyword_nz_terms est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2849">A keyword from Keyword_nz_terms is found.</span></span>
- <span data-ttu-id="64f1e-2850">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2850">The checksum passes.</span></span>

```
<!-- New Zealand Health Number -->
<Entity id="2b71c1c8-d14e-4430-82dc-fd1ed6bf05c7" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_new_zealand_ministry_of_health_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_nz_terms" />
        </Any>
    </Pattern>
</Entity>
```

<span data-ttu-id="64f1e-2851">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-2851">Keywords</span></span>

<span data-ttu-id="64f1e-2852">Keyword_nz_terms</span><span class="sxs-lookup"><span data-stu-id="64f1e-2852">Keyword_nz_terms</span></span>

- <span data-ttu-id="64f1e-2853">NHI</span><span class="sxs-lookup"><span data-stu-id="64f1e-2853">NHI</span></span> 
- <span data-ttu-id="64f1e-2854">Nouvelle-Zélande</span><span class="sxs-lookup"><span data-stu-id="64f1e-2854">New Zealand</span></span> 
- <span data-ttu-id="64f1e-2855">Intégrité</span><span class="sxs-lookup"><span data-stu-id="64f1e-2855">Health</span></span> 
- <span data-ttu-id="64f1e-2856">destinations</span><span class="sxs-lookup"><span data-stu-id="64f1e-2856">treatment</span></span> 
   
## <a name="norway-identification-number"></a><span data-ttu-id="64f1e-2857">Numéro d’identification Norvège</span><span class="sxs-lookup"><span data-stu-id="64f1e-2857">Norway Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-2858">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-2858">Format</span></span>

<span data-ttu-id="64f1e-2859">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2859">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-2860">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2860">Pattern</span></span>

<span data-ttu-id="64f1e-2861">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2861">11 digits:</span></span>
- <span data-ttu-id="64f1e-2862">Six chiffres au format JJMMAA qui correspondent à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="64f1e-2862">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="64f1e-2863">Numéro individuel à trois chiffres </span><span class="sxs-lookup"><span data-stu-id="64f1e-2863">Three-digit individual number</span></span> 
- <span data-ttu-id="64f1e-2864">Deux chiffres de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2864">Two check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-2865">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2865">Checksum</span></span>

<span data-ttu-id="64f1e-2866">Oui</span><span class="sxs-lookup"><span data-stu-id="64f1e-2866">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-2867">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-2867">Definition</span></span>

<span data-ttu-id="64f1e-2868">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2868">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-2869">La fonction Func_norway_id_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2869">The function Func_norway_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-2870">Un mot clé figurant dans la liste Keyword_norway_id_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2870">A keyword from Keyword_norway_id_number is found.</span></span>
- <span data-ttu-id="64f1e-2871">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2871">The checksum passes.</span></span>
- <span data-ttu-id="64f1e-2872">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2872">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-2873">La fonction Func_norway_id_numbe trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2873">The function Func_norway_id_numbe finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-2874">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2874">The checksum passes.</span></span>

```
<!-- Norway Identification Number -->
<Entity id="d4c8a798-e9f2-4bd3-9652-500d24080fc3" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_norway_id_number"/>
     <Match idRef="Keyword_norway_id_number"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_norway_id_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-2875">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-2875">Keywords</span></span>

#### <a name="keywordnorwayidnumber"></a><span data-ttu-id="64f1e-2876">Keyword_norway_id_number</span><span class="sxs-lookup"><span data-stu-id="64f1e-2876">Keyword_norway_id_number</span></span>

- <span data-ttu-id="64f1e-2877">Personal identification number</span><span class="sxs-lookup"><span data-stu-id="64f1e-2877">Personal identification number</span></span>
- <span data-ttu-id="64f1e-2878">Norwegian ID Number</span><span class="sxs-lookup"><span data-stu-id="64f1e-2878">Norwegian ID Number</span></span>
- <span data-ttu-id="64f1e-2879">ID Number</span><span class="sxs-lookup"><span data-stu-id="64f1e-2879">ID Number</span></span>
- <span data-ttu-id="64f1e-2880">Identificateur</span><span class="sxs-lookup"><span data-stu-id="64f1e-2880">Identification</span></span>
- <span data-ttu-id="64f1e-2881">Personnummer</span><span class="sxs-lookup"><span data-stu-id="64f1e-2881">Personnummer</span></span>
- <span data-ttu-id="64f1e-2882">Fødselsnummer</span><span class="sxs-lookup"><span data-stu-id="64f1e-2882">Fødselsnummer</span></span>

   
## <a name="philippines-unified-multi-purpose-id-number"></a><span data-ttu-id="64f1e-2883">Numéro d’identification multifonction unifié Philippines</span><span class="sxs-lookup"><span data-stu-id="64f1e-2883">Philippines Unified Multi-Purpose ID Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-2884">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-2884">Format</span></span>

<span data-ttu-id="64f1e-2885">12 chiffres séparés par des traits d’union</span><span class="sxs-lookup"><span data-stu-id="64f1e-2885">12 digits separated by hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-2886">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2886">Pattern</span></span>

<span data-ttu-id="64f1e-2887">12 chiffres :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2887">12 digits:</span></span>
- <span data-ttu-id="64f1e-2888">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2888">Four digits</span></span> 
- <span data-ttu-id="64f1e-2889">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="64f1e-2889">A hyphen</span></span> 
- <span data-ttu-id="64f1e-2890">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="64f1e-2890">Seven digits</span></span> 
- <span data-ttu-id="64f1e-2891">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="64f1e-2891">A hyphen</span></span> 
- <span data-ttu-id="64f1e-2892">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="64f1e-2892">One digit</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-2893">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2893">Checksum</span></span>

<span data-ttu-id="64f1e-2894">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-2894">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-2895">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-2895">Definition</span></span>

<span data-ttu-id="64f1e-2896">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2896">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-2897">L’expression régulière Regex_philippines_unified_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2897">The regular expression Regex_philippines_unified_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-2898">Un mot clé figurant dans la liste Keyword_philippines_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2898">A keyword from Keyword_philippines_id is found.</span></span>

```
<!-- Philippines Unified Multi-Purpose ID number -->
<Entity id="019b39dd-8c25-4765-91a3-d9c6baf3c3b3" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_philippines_unified_id"/>
     <Match idRef="Keyword_philippines_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-2899">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-2899">Keywords</span></span>
   
#### <a name="keywordphilippinesid"></a><span data-ttu-id="64f1e-2900">Keyword_philippines_id</span><span class="sxs-lookup"><span data-stu-id="64f1e-2900">Keyword_philippines_id</span></span>

- <span data-ttu-id="64f1e-2901">Unified Multi-Purpose ID</span><span class="sxs-lookup"><span data-stu-id="64f1e-2901">Unified Multi-Purpose ID</span></span> 
- <span data-ttu-id="64f1e-2902">UMID</span><span class="sxs-lookup"><span data-stu-id="64f1e-2902">UMID</span></span> 
- <span data-ttu-id="64f1e-2903">Identity Card</span><span class="sxs-lookup"><span data-stu-id="64f1e-2903">Identity Card</span></span> 
- <span data-ttu-id="64f1e-2904">Pinag-isang Multi-Layunin ID</span><span class="sxs-lookup"><span data-stu-id="64f1e-2904">Pinag-isang Multi-Layunin ID</span></span>
   
## <a name="poland-identity-card"></a><span data-ttu-id="64f1e-2905">Carte d'identité Pologne</span><span class="sxs-lookup"><span data-stu-id="64f1e-2905">Poland Identity Card</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-2906">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-2906">Format</span></span>

<span data-ttu-id="64f1e-2907">Trois lettres et six chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2907">Three letters and six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-2908">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2908">Pattern</span></span>

<span data-ttu-id="64f1e-2909">Trois lettres (ne respectant pas la casse) suivis de six chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2909">Three letters (not case sensitive) followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-2910">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2910">Checksum</span></span>

<span data-ttu-id="64f1e-2911">Oui</span><span class="sxs-lookup"><span data-stu-id="64f1e-2911">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-2912">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-2912">Definition</span></span>

<span data-ttu-id="64f1e-2913">Une stratégie DLP est sûre à 75% d'avoir détecté ce type d'informations sensibles si, dans une proximité de 300 caractères: la fonction Func_polish_national_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2913">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_polish_national_id finds content that matches the pattern.</span></span>
<span data-ttu-id="64f1e-2914">Un mot clé figurant dans la liste Keyword_polish_national_id_passport_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2914">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
<span data-ttu-id="64f1e-2915">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2915">The checksum passes.</span></span>

```
<!-- Poland Identity Card-->
<Entity id="25E64989-ED5D-40CA-A939-6C14183BB7BF" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_national_id" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-2916">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-2916">Keywords</span></span>

#### <a name="keywordpolishnationalidpassportnumber"></a><span data-ttu-id="64f1e-2917">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="64f1e-2917">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="64f1e-2918">Dowód OSOBISTY</span><span class="sxs-lookup"><span data-stu-id="64f1e-2918">Dowód osobisty</span></span>
- <span data-ttu-id="64f1e-2919">Chiffre dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="64f1e-2919">Numer dowodu osobistego</span></span>
- <span data-ttu-id="64f1e-2920">Nazwa i dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="64f1e-2920">Nazwa i numer dowodu osobistego</span></span>
- <span data-ttu-id="64f1e-2921">Nazwa i Nr dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="64f1e-2921">Nazwa i nr dowodu osobistego</span></span>
- <span data-ttu-id="64f1e-2922">Nazwa je nr dowodu tożsamości</span><span class="sxs-lookup"><span data-stu-id="64f1e-2922">Nazwa i nr dowodu tożsamości</span></span>
- <span data-ttu-id="64f1e-2923">Dowód Tożsamości</span><span class="sxs-lookup"><span data-stu-id="64f1e-2923">Dowód Tożsamości</span></span>
- <span data-ttu-id="64f1e-2924">Dow.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2924">dow.</span></span> <span data-ttu-id="64f1e-2925">OS.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2925">os.</span></span>

   
## <a name="poland-national-id-pesel"></a><span data-ttu-id="64f1e-2926">ID national polonais (PESEL)</span><span class="sxs-lookup"><span data-stu-id="64f1e-2926">Poland National ID (PESEL)</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-2927">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-2927">Format</span></span>

<span data-ttu-id="64f1e-2928">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2928">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-2929">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2929">Pattern</span></span>

<span data-ttu-id="64f1e-2930">11 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="64f1e-2930">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-2931">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2931">Checksum</span></span>

<span data-ttu-id="64f1e-2932">Oui</span><span class="sxs-lookup"><span data-stu-id="64f1e-2932">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-2933">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-2933">Definition</span></span>

<span data-ttu-id="64f1e-2934">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2934">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-2935">La fonction Func_pesel_identification_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2935">The function Func_pesel_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-2936">Un mot clé figurant dans la liste Keyword_pesel_identification_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2936">A keyword from Keyword_pesel_identification_number is found.</span></span>
- <span data-ttu-id="64f1e-2937">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2937">The checksum passes.</span></span>

```
<!-- Poland National ID (PESEL) -->      
<Entity id="E3AAF206-4297-412F-9E06-BA8487E22456" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_pesel_identification_number" />
          <Match idRef="Keyword_pesel_identification_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-2938">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-2938">Keywords</span></span>

#### <a name="keywordpeselidentificationnumber"></a><span data-ttu-id="64f1e-2939">Keyword_pesel_identification_number</span><span class="sxs-lookup"><span data-stu-id="64f1e-2939">Keyword_pesel_identification_number</span></span>

- <span data-ttu-id="64f1e-2940">Nr PESEL</span><span class="sxs-lookup"><span data-stu-id="64f1e-2940">Nr PESEL</span></span>
- <span data-ttu-id="64f1e-2941">PESEL</span><span class="sxs-lookup"><span data-stu-id="64f1e-2941">PESEL</span></span>   

   
## <a name="poland-passport"></a><span data-ttu-id="64f1e-2942">Passeport Pologne</span><span class="sxs-lookup"><span data-stu-id="64f1e-2942">Poland Passport</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-2943">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-2943">Format</span></span>

<span data-ttu-id="64f1e-2944">Deux lettres et sept chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2944">Two letters and seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-2945">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2945">Pattern</span></span>

<span data-ttu-id="64f1e-2946">Deux lettres (ne respectant pas la casse) suivies de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2946">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-2947">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2947">Checksum</span></span>

<span data-ttu-id="64f1e-2948">Oui</span><span class="sxs-lookup"><span data-stu-id="64f1e-2948">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-2949">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-2949">Definition</span></span>

<span data-ttu-id="64f1e-2950">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2950">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-2951">La fonction Func_polish_passport_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2951">The function Func_polish_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-2952">Un mot clé figurant dans la liste Keyword_polish_national_id_passport_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2952">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
- <span data-ttu-id="64f1e-2953">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2953">The checksum passes.</span></span>

```
<!-- Poland Passport Number -->
<Entity id="03937FB5-D2B6-4487-B61F-0F8BFF7C3517" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_passport_number" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
</Version>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-2954">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-2954">Keywords</span></span>

#### <a name="keywordpolishnationalidpassportnumber"></a><span data-ttu-id="64f1e-2955">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="64f1e-2955">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="64f1e-2956">Numéro paszportu</span><span class="sxs-lookup"><span data-stu-id="64f1e-2956">Numer paszportu</span></span>
- <span data-ttu-id="64f1e-2957">Nr.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2957">Nr.</span></span> <span data-ttu-id="64f1e-2958">Paszportu</span><span class="sxs-lookup"><span data-stu-id="64f1e-2958">Paszportu</span></span>
- <span data-ttu-id="64f1e-2959">Paszport</span><span class="sxs-lookup"><span data-stu-id="64f1e-2959">Paszport</span></span>

   
## <a name="portugal-citizen-card-number"></a><span data-ttu-id="64f1e-2960">Numéro de carte de citoyen Portugal</span><span class="sxs-lookup"><span data-stu-id="64f1e-2960">Portugal Citizen Card Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-2961">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-2961">Format</span></span>

<span data-ttu-id="64f1e-2962">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2962">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-2963">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2963">Pattern</span></span>

<span data-ttu-id="64f1e-2964">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2964">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-2965">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2965">Checksum</span></span>

<span data-ttu-id="64f1e-2966">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-2966">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-2967">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-2967">Definition</span></span>

<span data-ttu-id="64f1e-2968">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2968">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-2969">L’expression régulière Regex_portugal_citizen_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2969">The regular expression Regex_portugal_citizen_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-2970">Un mot clé figurant dans la liste Keyword_portugal_citizen_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2970">A keyword from Keyword_portugal_citizen_card is found.</span></span>

```
<!-- Portugal Citizen Card Number -->
<Entity id="91a7ece2-add4-4986-9a15-c84544d81ecd" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_portugal_citizen_card"/>
     <Match idRef="Keyword_portugal_citizen_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-2971">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-2971">Keywords</span></span>

#### <a name="keywordportugalcitizencard"></a><span data-ttu-id="64f1e-2972">Keyword_portugal_citizen_card</span><span class="sxs-lookup"><span data-stu-id="64f1e-2972">Keyword_portugal_citizen_card</span></span>

- <span data-ttu-id="64f1e-2973">Citizen Card</span><span class="sxs-lookup"><span data-stu-id="64f1e-2973">Citizen Card</span></span>
- <span data-ttu-id="64f1e-2974">National ID Card</span><span class="sxs-lookup"><span data-stu-id="64f1e-2974">National ID Card</span></span>
- <span data-ttu-id="64f1e-2975">Cc</span><span class="sxs-lookup"><span data-stu-id="64f1e-2975">CC</span></span>
- <span data-ttu-id="64f1e-2976">Cartão de Cidadão</span><span class="sxs-lookup"><span data-stu-id="64f1e-2976">Cartão de Cidadão</span></span>
- <span data-ttu-id="64f1e-2977">Bilhete de Identidade</span><span class="sxs-lookup"><span data-stu-id="64f1e-2977">Bilhete de Identidade</span></span>
   
## <a name="saudi-arabia-national-id"></a><span data-ttu-id="64f1e-2978">ID national Arabie saoudite</span><span class="sxs-lookup"><span data-stu-id="64f1e-2978">Saudi Arabia National ID</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-2979">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-2979">Format</span></span>

<span data-ttu-id="64f1e-2980">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2980">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-2981">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2981">Pattern</span></span>

<span data-ttu-id="64f1e-2982">10 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="64f1e-2982">10 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-2983">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2983">Checksum</span></span>

<span data-ttu-id="64f1e-2984">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-2984">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-2985">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-2985">Definition</span></span>

<span data-ttu-id="64f1e-2986">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2986">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-2987">L’expression régulière Regex_saudi_arabia_national_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2987">The regular expression Regex_saudi_arabia_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-2988">Un mot clé figurant dans la liste Keyword_saudi_arabia_national_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-2988">A keyword from Keyword_saudi_arabia_national_id is found.</span></span>

```
<!-- Saudi Arabia National ID -->
<Entity id="8c5a0ba8-404a-41a3-8871-746aa21ee6c0" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_saudi_arabia_national_id" />
        <Any minMatches="1">
          <Match idRef="Keyword_saudi_arabia_national_id" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-2989">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-2989">Keywords</span></span>

#### <a name="keywordsaudiarabianationalid"></a><span data-ttu-id="64f1e-2990">Keyword_saudi_arabia_national_id</span><span class="sxs-lookup"><span data-stu-id="64f1e-2990">Keyword_saudi_arabia_national_id</span></span>

- <span data-ttu-id="64f1e-2991">Carte d’identification</span><span class="sxs-lookup"><span data-stu-id="64f1e-2991">Identification Card</span></span> 
- <span data-ttu-id="64f1e-2992">numéro de carte d’identité</span><span class="sxs-lookup"><span data-stu-id="64f1e-2992">I card number</span></span> 
- <span data-ttu-id="64f1e-2993">Numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="64f1e-2993">ID number</span></span> 
- <span data-ttu-id="64f1e-2994">الوطنية الهوية بطاقة رقم</span><span class="sxs-lookup"><span data-stu-id="64f1e-2994">الوطنية الهوية بطاقة رقم</span></span> 

   
## <a name="singapore-national-registration-identity-card-nric-number"></a><span data-ttu-id="64f1e-2995">Numéro de carte d’identité d’enregistrement national (NRIC) Singapour</span><span class="sxs-lookup"><span data-stu-id="64f1e-2995">Singapore National Registration Identity Card (NRIC) Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-2996">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-2996">Format</span></span>

<span data-ttu-id="64f1e-2997">Neuf lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-2997">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-2998">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-2998">Pattern</span></span>

- <span data-ttu-id="64f1e-2999">Neuf lettres et chiffres :</span><span class="sxs-lookup"><span data-stu-id="64f1e-2999">Nine letters and digits:</span></span>
- <span data-ttu-id="64f1e-3000">La lettre « F », « G », « S » ou « T » (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="64f1e-3000">The letter "F", "G", "S", or "T" (not case sensitive)</span></span> 
- <span data-ttu-id="64f1e-3001">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="64f1e-3001">Seven digits</span></span> 
- <span data-ttu-id="64f1e-3002">Un chiffre de contrôle alphabétique</span><span class="sxs-lookup"><span data-stu-id="64f1e-3002">An alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-3003">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3003">Checksum</span></span>

<span data-ttu-id="64f1e-3004">Oui</span><span class="sxs-lookup"><span data-stu-id="64f1e-3004">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-3005">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-3005">Definition</span></span>

<span data-ttu-id="64f1e-3006">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3006">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-3007">L’expression régulière Regex_singapore_nric trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3007">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-3008">Un mot clé figurant dans la liste Keyword_singapore_nric est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3008">A keyword from Keyword_singapore_nric is found.</span></span>
- <span data-ttu-id="64f1e-3009">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3009">The checksum passes.</span></span>

<span data-ttu-id="64f1e-3010">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3010">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-3011">L’expression régulière Regex_singapore_nric trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3011">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-3012">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3012">The checksum passes.</span></span>

```
<!-- Singapore National Registration Identity Card (NRIC) Number -->
<Entity id="cead390a-dd83-4856-9751-fb6dc98c34da" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_singapore_nric"/>
     <Match idRef="Keyword_singapore_nric"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_singapore_nric"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-3013">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-3013">Keywords</span></span>
   
#### <a name="keywordsingaporenric"></a><span data-ttu-id="64f1e-3014">Keyword_singapore_nric</span><span class="sxs-lookup"><span data-stu-id="64f1e-3014">Keyword_singapore_nric</span></span>

- <span data-ttu-id="64f1e-3015">National Registration Identity Card</span><span class="sxs-lookup"><span data-stu-id="64f1e-3015">National Registration Identity Card</span></span> 
- <span data-ttu-id="64f1e-3016">Identity Card Number</span><span class="sxs-lookup"><span data-stu-id="64f1e-3016">Identity Card Number</span></span> 
- <span data-ttu-id="64f1e-3017">NRIC</span><span class="sxs-lookup"><span data-stu-id="64f1e-3017">NRIC</span></span> 
- <span data-ttu-id="64f1e-3018">COMBUSTION</span><span class="sxs-lookup"><span data-stu-id="64f1e-3018">IC</span></span> 
- <span data-ttu-id="64f1e-3019">Foreign Identification Number</span><span class="sxs-lookup"><span data-stu-id="64f1e-3019">Foreign Identification Number</span></span> 
- <span data-ttu-id="64f1e-3020">ECHERCHER</span><span class="sxs-lookup"><span data-stu-id="64f1e-3020">FIN</span></span> 
- <span data-ttu-id="64f1e-3021">身份证</span><span class="sxs-lookup"><span data-stu-id="64f1e-3021">身份证</span></span> 
- <span data-ttu-id="64f1e-3022">身份證</span><span class="sxs-lookup"><span data-stu-id="64f1e-3022">身份證</span></span> 
   
## <a name="south-africa-identification-number"></a><span data-ttu-id="64f1e-3023">Numéro d’identification Afrique du Sud</span><span class="sxs-lookup"><span data-stu-id="64f1e-3023">South Africa Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-3024">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-3024">Format</span></span>

<span data-ttu-id="64f1e-3025">13 chiffres pouvant contenir des espaces</span><span class="sxs-lookup"><span data-stu-id="64f1e-3025">13 digits that may contain spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-3026">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3026">Pattern</span></span>

<span data-ttu-id="64f1e-3027">13 chiffres :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3027">13 digits:</span></span>
- <span data-ttu-id="64f1e-3028">Six chiffres au format AAMMJJ correspondant à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="64f1e-3028">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="64f1e-3029">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-3029">Four digits</span></span> 
- <span data-ttu-id="64f1e-3030">Un indicateur de citoyenneté à un chiffre </span><span class="sxs-lookup"><span data-stu-id="64f1e-3030">A single-digit citizenship indicator</span></span> 
- <span data-ttu-id="64f1e-3031">Le chiffre « 8 » ou « 9 » </span><span class="sxs-lookup"><span data-stu-id="64f1e-3031">The digit "8" or "9"</span></span> 
- <span data-ttu-id="64f1e-3032">Un chiffre pour la somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3032">One digit which is a checksum digit</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-3033">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3033">Checksum</span></span>

<span data-ttu-id="64f1e-3034">Oui</span><span class="sxs-lookup"><span data-stu-id="64f1e-3034">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-3035">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-3035">Definition</span></span>

<span data-ttu-id="64f1e-3036">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3036">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-3037">La fonction Func_south_africa_identification_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3037">The function Func_south_africa_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-3038">Un mot clé figurant dans la liste Keyword_south_africa_identification_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3038">A keyword from Keyword_south_africa_identification_number is found.</span></span>
- <span data-ttu-id="64f1e-3039">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3039">The checksum passes.</span></span>

```
<!-- South Africa Identification Number -->
<Entity id="e2adf7cb-8ea6-4048-a2ed-d89eb65f2780" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_south_africa_identification_number"/>
     <Match idRef="Keyword_south_africa_identification_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-3040">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-3040">Keywords</span></span>
   
#### <a name="keywordsouthafricaidentificationnumber"></a><span data-ttu-id="64f1e-3041">Keyword_south_africa_identification_number</span><span class="sxs-lookup"><span data-stu-id="64f1e-3041">Keyword_south_africa_identification_number</span></span>

- <span data-ttu-id="64f1e-3042">Identity card</span><span class="sxs-lookup"><span data-stu-id="64f1e-3042">Identity card</span></span>
- <span data-ttu-id="64f1e-3043">ID</span><span class="sxs-lookup"><span data-stu-id="64f1e-3043">ID</span></span>
- <span data-ttu-id="64f1e-3044">Identificateur</span><span class="sxs-lookup"><span data-stu-id="64f1e-3044">Identification</span></span> 
   
## <a name="south-korea-resident-registration-number"></a><span data-ttu-id="64f1e-3045">Matricule de résident Corée du Sud</span><span class="sxs-lookup"><span data-stu-id="64f1e-3045">South Korea Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-3046">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-3046">Format</span></span>

<span data-ttu-id="64f1e-3047">13 chiffres contenant un trait d’union</span><span class="sxs-lookup"><span data-stu-id="64f1e-3047">13 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-3048">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3048">Pattern</span></span>

<span data-ttu-id="64f1e-3049">13 chiffres :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3049">13 digits:</span></span>
- <span data-ttu-id="64f1e-3050">Six chiffres au format AAMMJJ correspondant à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="64f1e-3050">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="64f1e-3051">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="64f1e-3051">A hyphen</span></span> 
- <span data-ttu-id="64f1e-3052">Un chiffre déterminé par le siècle et le sexe </span><span class="sxs-lookup"><span data-stu-id="64f1e-3052">One digit determined by the century and gender</span></span> 
- <span data-ttu-id="64f1e-3053">Code à quatre chiffres désignant la région de naissance </span><span class="sxs-lookup"><span data-stu-id="64f1e-3053">Four-digit region-of-birth code</span></span> 
- <span data-ttu-id="64f1e-3054">Un chiffre utilisé pour différencier les personnes dont les chiffres précédents sont identiques. </span><span class="sxs-lookup"><span data-stu-id="64f1e-3054">One digit used to differentiate people for whom the preceding numbers are identical</span></span> 
- <span data-ttu-id="64f1e-3055">Un chiffre de contrôle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3055">A check digit.</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-3056">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3056">Checksum</span></span>

<span data-ttu-id="64f1e-3057">Oui</span><span class="sxs-lookup"><span data-stu-id="64f1e-3057">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-3058">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-3058">Definition</span></span>

<span data-ttu-id="64f1e-3059">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3059">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-3060">La fonction Func_south_korea_resident_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3060">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-3061">Un mot clé figurant dans la liste Keyword_south_korea_resident_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3061">A keyword from Keyword_south_korea_resident_number is found.</span></span>
- <span data-ttu-id="64f1e-3062">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3062">The checksum passes.</span></span>

<span data-ttu-id="64f1e-3063">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3063">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-3064">La fonction Func_south_korea_resident_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3064">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-3065">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3065">The checksum passes.</span></span>

```
<!-- South Korea Resident Registration Number -->
<Entity id="5b802e18-ba80-44c4-bc83-bf2ad36ae36a" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_south_korea_resident_number"/>
     <Match idRef="Keyword_south_korea_resident_number"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_south_korea_resident_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-3066">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-3066">Keywords</span></span>
   
#### <a name="keywordsouthkorearesidentnumber"></a><span data-ttu-id="64f1e-3067">Keyword_south_korea_resident_number</span><span class="sxs-lookup"><span data-stu-id="64f1e-3067">Keyword_south_korea_resident_number</span></span>

- <span data-ttu-id="64f1e-3068">National ID card</span><span class="sxs-lookup"><span data-stu-id="64f1e-3068">National ID card</span></span> 
- <span data-ttu-id="64f1e-3069">Citizen’s Registration Number</span><span class="sxs-lookup"><span data-stu-id="64f1e-3069">Citizen's Registration Number</span></span> 
- <span data-ttu-id="64f1e-3070">Jumin deungnok beonho</span><span class="sxs-lookup"><span data-stu-id="64f1e-3070">Jumin deungnok beonho</span></span> 
- <span data-ttu-id="64f1e-3071">RRN</span><span class="sxs-lookup"><span data-stu-id="64f1e-3071">RRN</span></span> 
- <span data-ttu-id="64f1e-3072">주민등록번호</span><span class="sxs-lookup"><span data-stu-id="64f1e-3072">주민등록번호</span></span>
   
## <a name="spain-social-security-number-ssn"></a><span data-ttu-id="64f1e-3073">Numéro de sécurité sociale Espagne</span><span class="sxs-lookup"><span data-stu-id="64f1e-3073">Spain Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-3074">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-3074">Format</span></span>

<span data-ttu-id="64f1e-3075">11 à 12 chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-3075">11-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-3076">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3076">Pattern</span></span>

<span data-ttu-id="64f1e-3077">11-12 chiffres:</span><span class="sxs-lookup"><span data-stu-id="64f1e-3077">11-12 digits:</span></span>
- <span data-ttu-id="64f1e-3078">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-3078">Two digits</span></span> 
- <span data-ttu-id="64f1e-3079">Une barre oblique (facultative)</span><span class="sxs-lookup"><span data-stu-id="64f1e-3079">A forward slash (optional)</span></span> 
- <span data-ttu-id="64f1e-3080">7 à 8 chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-3080">7-8 digits</span></span> 
- <span data-ttu-id="64f1e-3081">Une barre oblique (facultative)</span><span class="sxs-lookup"><span data-stu-id="64f1e-3081">A forward slash (optional)</span></span> 
- <span data-ttu-id="64f1e-3082">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-3082">Two digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-3083">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3083">Checksum</span></span>

<span data-ttu-id="64f1e-3084">Oui</span><span class="sxs-lookup"><span data-stu-id="64f1e-3084">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-3085">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-3085">Definition</span></span>

<span data-ttu-id="64f1e-3086">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3086">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-3087">La fonction Func_spanish_social_security_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3087">The function Func_spanish_social_security_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-3088">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3088">The checksum passes.</span></span>

```
<!-- Spain SSN -->
<Entity id="5df987c0-8eae-4bce-ace7-b316347f3070" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_spanish_social_security_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-3089">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-3089">Keywords</span></span>

<span data-ttu-id="64f1e-3090">Aucun</span><span class="sxs-lookup"><span data-stu-id="64f1e-3090">None</span></span>

## <a name="sql-server-connection-string"></a><span data-ttu-id="64f1e-3091">Chaîne de connexion SQL Server</span><span class="sxs-lookup"><span data-stu-id="64f1e-3091">SQL Server Connection String</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-3092">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-3092">Format</span></span>

<span data-ttu-id="64f1e-3093">La chaîne «User ID», «User ID», «UID» ou «UserId» suivi des caractères et des chaînes décrits dans le modèle ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3093">The string "User Id", "User ID", "uid", or "UserId" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-3094">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3094">Pattern</span></span>

- <span data-ttu-id="64f1e-3095">La chaîne «User ID», «User ID», «UID» ou «UserId»</span><span class="sxs-lookup"><span data-stu-id="64f1e-3095">The string "User Id", "User ID", "uid", or "UserId"</span></span>
- <span data-ttu-id="64f1e-3096">N'importe quelle combinaison entre 1-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="64f1e-3096">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="64f1e-3097">La chaîne "password" ou "PWD" où "PWD" n'est pas précédé d'une lettre minuscule</span><span class="sxs-lookup"><span data-stu-id="64f1e-3097">The string "Password" or "pwd" where "pwd" is not preceded by a lowercase letter</span></span>
- <span data-ttu-id="64f1e-3098">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="64f1e-3098">An equal sign (=)</span></span>
- <span data-ttu-id="64f1e-3099">Tout caractère qui n'est pas un signe dollar ($), un symbole de pourcentage (%), un symbole supérieur à (>), un symbole (@), un guillemet ("), un point-virgule (;), une accolade ouvrante ([) ou un crochet gauche ({)</span><span class="sxs-lookup"><span data-stu-id="64f1e-3099">Any character that is not a dollar sign ($), percent symbol (%), greater than symbol (>), at symbol (@), quotation mark ("), semicolon (;), left brace ([), or left bracket ({)</span></span>
- <span data-ttu-id="64f1e-3100">N'importe quelle combinaison de 7-128 caractères qui ne sont pas des points-virgules (;), barre oblique (/) ou guillemets (")</span><span class="sxs-lookup"><span data-stu-id="64f1e-3100">Any combination of 7-128 characters that are not a semicolon (;), forward slash (/), or quotation mark (")</span></span>
- <span data-ttu-id="64f1e-3101">Un point-virgule (;) ou guillemets (")</span><span class="sxs-lookup"><span data-stu-id="64f1e-3101">A semicolon (;) or quotation mark (")</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-3102">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3102">Checksum</span></span>

<span data-ttu-id="64f1e-3103">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-3103">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-3104">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-3104">Definition</span></span>

<span data-ttu-id="64f1e-3105">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3105">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-3106">L'expression régulière CEP_Regex_SQLServerConnectionString trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3106">The regular expression CEP_Regex_SQLServerConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-3107">Un mot clé depuis CEP_GlobalFilter \*\*\*\* est introuvable.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3107">A keyword from CEP_GlobalFilter is **not** found.</span></span>
- <span data-ttu-id="64f1e-3108">L'expression régulière CEP_PasswordPlaceHolder ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3108">The regular expression CEP_PasswordPlaceHolder does **not** find content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-3109">L'expression régulière CEP_CommonExampleKeywords ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3109">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```
<!---SQL Server Connection String>
<Entity id="e76b6205-d3cb-46f2-bd63-c90153f2f97d" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_SQLServerConnectionString" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_GlobalFilter" />
            <Match idRef="CEP_PasswordPlaceHolder" />
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-3110">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-3110">Keywords</span></span>

#### <a name="cepglobalfilter"></a><span data-ttu-id="64f1e-3111">CEP_GlobalFilter</span><span class="sxs-lookup"><span data-stu-id="64f1e-3111">CEP_GlobalFilter</span></span>

- <span data-ttu-id="64f1e-3112">some-password</span><span class="sxs-lookup"><span data-stu-id="64f1e-3112">some-password</span></span>
- <span data-ttu-id="64f1e-3113">somepassword</span><span class="sxs-lookup"><span data-stu-id="64f1e-3113">somepassword</span></span>
- <span data-ttu-id="64f1e-3114">secretPassword</span><span class="sxs-lookup"><span data-stu-id="64f1e-3114">secretPassword</span></span>
- <span data-ttu-id="64f1e-3115">échantillonnage</span><span class="sxs-lookup"><span data-stu-id="64f1e-3115">sample</span></span>

#### <a name="ceppasswordplaceholder"></a><span data-ttu-id="64f1e-3116">CEP_PasswordPlaceHolder</span><span class="sxs-lookup"><span data-stu-id="64f1e-3116">CEP_PasswordPlaceHolder</span></span>

<span data-ttu-id="64f1e-3117">(Notez que techniquement, ce type d'informations sensibles identifie ces mots clés à l'aide d'une expression régulière, et non d'une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="64f1e-3117">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="64f1e-3118">Mot de passe ou mot de passe suivi par 0-2 espaces, un signe égal (=), 0-2 espaces et un astérisque (\*)--ou--</span><span class="sxs-lookup"><span data-stu-id="64f1e-3118">Password or pwd followed by 0-2 spaces, an equal sign (=), 0-2 spaces, and an asterisk (\*) --OR--</span></span>
- <span data-ttu-id="64f1e-3119">Mot de passe ou mot de passe suivi par:</span><span class="sxs-lookup"><span data-stu-id="64f1e-3119">Password or pwd followed by:</span></span>
    - <span data-ttu-id="64f1e-3120">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="64f1e-3120">Equal sign (=)</span></span>
    - <span data-ttu-id="64f1e-3121">Symbole inférieur à (<)</span><span class="sxs-lookup"><span data-stu-id="64f1e-3121">Less than symbol (<)</span></span>
    - <span data-ttu-id="64f1e-3122">Toute combinaison de 1-200 caractères qui sont des lettres majuscules ou minuscules, des chiffres, un astérisque (\*), un tiret (-), un trait de soulignement (_) ou un espace blanc</span><span class="sxs-lookup"><span data-stu-id="64f1e-3122">Any combination of 1-200 characters that are upper- or lowercase letters, digits, an asterisk (\*), hyphen (-), underline (_), or whitespace character</span></span>
    - <span data-ttu-id="64f1e-3123">Symbole supérieur à (>)</span><span class="sxs-lookup"><span data-stu-id="64f1e-3123">Greater than symbol (>)</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="64f1e-3124">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="64f1e-3124">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="64f1e-3125">(Notez que techniquement, ce type d'informations sensibles identifie ces mots clés à l'aide d'une expression régulière, et non d'une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="64f1e-3125">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="64f1e-3126">contoso</span><span class="sxs-lookup"><span data-stu-id="64f1e-3126">contoso</span></span>
- <span data-ttu-id="64f1e-3127">société</span><span class="sxs-lookup"><span data-stu-id="64f1e-3127">fabrikam</span></span>
- <span data-ttu-id="64f1e-3128">Northwind</span><span class="sxs-lookup"><span data-stu-id="64f1e-3128">northwind</span></span>
- <span data-ttu-id="64f1e-3129">immédiatement</span><span class="sxs-lookup"><span data-stu-id="64f1e-3129">sandbox</span></span>
- <span data-ttu-id="64f1e-3130">OneBox</span><span class="sxs-lookup"><span data-stu-id="64f1e-3130">onebox</span></span>
- <span data-ttu-id="64f1e-3131">hôte</span><span class="sxs-lookup"><span data-stu-id="64f1e-3131">localhost</span></span>
- <span data-ttu-id="64f1e-3132">bouclage</span><span class="sxs-lookup"><span data-stu-id="64f1e-3132">127.0.0.1</span></span>
- <span data-ttu-id="64f1e-3133">TESTACS. <!--no-hyperlink-->com</span><span class="sxs-lookup"><span data-stu-id="64f1e-3133">testacs.<!--no-hyperlink-->com</span></span>
- <span data-ttu-id="64f1e-3134">s-int.<!--no-hyperlink-->net</span><span class="sxs-lookup"><span data-stu-id="64f1e-3134">s-int.<!--no-hyperlink-->net</span></span>

## <a name="sweden-national-id"></a><span data-ttu-id="64f1e-3135">ID national Suède</span><span class="sxs-lookup"><span data-stu-id="64f1e-3135">Sweden National ID</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-3136">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-3136">Format</span></span>

<span data-ttu-id="64f1e-3137">10 ou 12 chiffres et éventuellement un délimiteur</span><span class="sxs-lookup"><span data-stu-id="64f1e-3137">10 or 12 digits and an optional delimiter</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-3138">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3138">Pattern</span></span>

<span data-ttu-id="64f1e-3139">10 ou 12 chiffres et un délimiteur facultatif :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3139">10 or 12 digits and an optional delimiter:</span></span>
- <span data-ttu-id="64f1e-3140">2 à 4 chiffres (facultatifs)</span><span class="sxs-lookup"><span data-stu-id="64f1e-3140">2-4 digits (optional)</span></span> 
- <span data-ttu-id="64f1e-3141">Six chiffres au format de date AAMMJJ</span><span class="sxs-lookup"><span data-stu-id="64f1e-3141">Six digits in date format YYMMDD</span></span> 
- <span data-ttu-id="64f1e-3142">Séparateur de « - » ou « + » (facultatif), plus</span><span class="sxs-lookup"><span data-stu-id="64f1e-3142">Delimiter of "-" or "+" (optional), plus</span></span>
- <span data-ttu-id="64f1e-3143">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-3143">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-3144">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3144">Checksum</span></span>

<span data-ttu-id="64f1e-3145">Oui</span><span class="sxs-lookup"><span data-stu-id="64f1e-3145">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-3146">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-3146">Definition</span></span>

<span data-ttu-id="64f1e-3147">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3147">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-3148">La fonction Func_swedish_national_identifier trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3148">The function Func_swedish_national_identifier finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-3149">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3149">The checksum passes.</span></span>

```
<!-- Sweden National ID -->
<Entity id="f69aaf40-79be-4fac-8f05-fd1910d272c8" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_swedish_national_identifier" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-3150">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-3150">Keywords</span></span>

<span data-ttu-id="64f1e-3151">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-3151">No</span></span>
   
## <a name="sweden-passport-number"></a><span data-ttu-id="64f1e-3152">Numéro de passeport Suède</span><span class="sxs-lookup"><span data-stu-id="64f1e-3152">Sweden Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-3153">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-3153">Format</span></span>

<span data-ttu-id="64f1e-3154">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-3154">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-3155">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3155">Pattern</span></span>

<span data-ttu-id="64f1e-3156">Huit chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="64f1e-3156">Eight consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-3157">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3157">Checksum</span></span>

<span data-ttu-id="64f1e-3158">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-3158">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-3159">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-3159">Definition</span></span>

<span data-ttu-id="64f1e-3160">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3160">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-3161">L’expression régulière Regex_sweden_passport_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3161">The regular expression Regex_sweden_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-3162">L’une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3162">One of the following is true:</span></span>
    - <span data-ttu-id="64f1e-3163">Un mot clé figurant dans la liste Keyword_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3163">A keyword from Keyword_passport is found.</span></span>
    - <span data-ttu-id="64f1e-3164">Un mot clé figurant dans la liste Keyword_sweden_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3164">A keyword from Keyword_sweden_passport is found.</span></span>

```
<!-- Sweden Passport Number -->
<Entity id="ba4e7456-55a9-4d89-9140-c33673553526" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_sweden_passport_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_passport" />
          <Match idRef="Keyword_sweden_passport" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-3165">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-3165">Keywords</span></span>
   
#### <a name="keywordswedenpassport"></a><span data-ttu-id="64f1e-3166">Keyword_sweden_passport</span><span class="sxs-lookup"><span data-stu-id="64f1e-3166">Keyword_sweden_passport</span></span>

- <span data-ttu-id="64f1e-3167">exigences en matière de visa</span><span class="sxs-lookup"><span data-stu-id="64f1e-3167">visa requirements</span></span> 
- <span data-ttu-id="64f1e-3168">Carte d’enregistrement d’une personne étrangère</span><span class="sxs-lookup"><span data-stu-id="64f1e-3168">Alien Registration Card</span></span> 
- <span data-ttu-id="64f1e-3169">Visas Schengen</span><span class="sxs-lookup"><span data-stu-id="64f1e-3169">Schengen visas</span></span> 
- <span data-ttu-id="64f1e-3170">Visa Schengen</span><span class="sxs-lookup"><span data-stu-id="64f1e-3170">Schengen visa</span></span> 
- <span data-ttu-id="64f1e-3171">Traitement du visa</span><span class="sxs-lookup"><span data-stu-id="64f1e-3171">Visa Processing</span></span> 
- <span data-ttu-id="64f1e-3172">Type de visa</span><span class="sxs-lookup"><span data-stu-id="64f1e-3172">Visa Type</span></span> 
- <span data-ttu-id="64f1e-3173">Entrée unique</span><span class="sxs-lookup"><span data-stu-id="64f1e-3173">Single Entry</span></span> 
- <span data-ttu-id="64f1e-3174">Entrée multiple</span><span class="sxs-lookup"><span data-stu-id="64f1e-3174">Multiple Entry</span></span> 
- <span data-ttu-id="64f1e-3175">Frais de traitement G3</span><span class="sxs-lookup"><span data-stu-id="64f1e-3175">G3 Processing Fees</span></span> 

#### <a name="keywordpassport"></a><span data-ttu-id="64f1e-3176">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="64f1e-3176">Keyword_passport</span></span>

- <span data-ttu-id="64f1e-3177">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="64f1e-3177">Passport Number</span></span> 
- <span data-ttu-id="64f1e-3178">N° de passeport</span><span class="sxs-lookup"><span data-stu-id="64f1e-3178">Passport No</span></span> 
- <span data-ttu-id="64f1e-3179"># Passeport</span><span class="sxs-lookup"><span data-stu-id="64f1e-3179">Passport #</span></span> 
- <span data-ttu-id="64f1e-3180">Tel</span><span class="sxs-lookup"><span data-stu-id="64f1e-3180">Passport#</span></span> 
- <span data-ttu-id="64f1e-3181">PassportID</span><span class="sxs-lookup"><span data-stu-id="64f1e-3181">PassportID</span></span> 
- <span data-ttu-id="64f1e-3182">N ° passeport</span><span class="sxs-lookup"><span data-stu-id="64f1e-3182">Passportno</span></span> 
- <span data-ttu-id="64f1e-3183">passportnumber</span><span class="sxs-lookup"><span data-stu-id="64f1e-3183">passportnumber</span></span> 
- <span data-ttu-id="64f1e-3184">パスポート</span><span class="sxs-lookup"><span data-stu-id="64f1e-3184">パスポート</span></span> 
- <span data-ttu-id="64f1e-3185">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="64f1e-3185">パスポート番号</span></span> 
- <span data-ttu-id="64f1e-3186">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="64f1e-3186">パスポートのNum</span></span> 
- <span data-ttu-id="64f1e-3187">パスポート #</span><span class="sxs-lookup"><span data-stu-id="64f1e-3187">パスポート＃</span></span> 
- <span data-ttu-id="64f1e-3188">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="64f1e-3188">Numéro de passeport</span></span> 
- <span data-ttu-id="64f1e-3189">Passeport n°</span><span class="sxs-lookup"><span data-stu-id="64f1e-3189">Passeport n °</span></span> 
- <span data-ttu-id="64f1e-3190">Passeport numéro</span><span class="sxs-lookup"><span data-stu-id="64f1e-3190">Passeport Non</span></span> 
- <span data-ttu-id="64f1e-3191"># Passeport</span><span class="sxs-lookup"><span data-stu-id="64f1e-3191">Passeport #</span></span> 
- <span data-ttu-id="64f1e-3192">Passeport</span><span class="sxs-lookup"><span data-stu-id="64f1e-3192">Passeport#</span></span> 
- <span data-ttu-id="64f1e-3193">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="64f1e-3193">PasseportNon</span></span> 
- <span data-ttu-id="64f1e-3194">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="64f1e-3194">Passeportn °</span></span> 
   
## <a name="swift-code"></a><span data-ttu-id="64f1e-3195">Code SWIFT</span><span class="sxs-lookup"><span data-stu-id="64f1e-3195">SWIFT Code</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-3196">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-3196">Format</span></span>

<span data-ttu-id="64f1e-3197">Quatre lettres suivies de 5 à 31 lettres ou chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-3197">Four letters followed by 5-31 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-3198">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3198">Pattern</span></span>

<span data-ttu-id="64f1e-3199">Quatre lettres suivies de 5 à 31 lettres ou chiffres :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3199">Four letters followed by 5-31 letters or digits:</span></span>
- <span data-ttu-id="64f1e-3200">Code bancaire à quatre lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="64f1e-3200">Four-letter bank code (not case sensitive)</span></span> 
- <span data-ttu-id="64f1e-3201">Un espace facultatif</span><span class="sxs-lookup"><span data-stu-id="64f1e-3201">An optional space</span></span> 
- <span data-ttu-id="64f1e-3202">4 à 28 lettres ou chiffres (numéro de compte bancaire de base (BBAN))</span><span class="sxs-lookup"><span data-stu-id="64f1e-3202">4-28 letters or digits (the Basic Bank Account Number (BBAN))</span></span> 
- <span data-ttu-id="64f1e-3203">Un espace facultatif</span><span class="sxs-lookup"><span data-stu-id="64f1e-3203">An optional space</span></span> 
- <span data-ttu-id="64f1e-3204">1 à 3 lettres ou chiffres (reste du BBAN)</span><span class="sxs-lookup"><span data-stu-id="64f1e-3204">1-3 letters or digits (remainder of the BBAN)</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-3205">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3205">Checksum</span></span>

<span data-ttu-id="64f1e-3206">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-3206">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-3207">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-3207">Definition</span></span>

<span data-ttu-id="64f1e-3208">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3208">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-3209">L’expression régulière Regex_swift trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3209">The regular expression Regex_swift finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-3210">Un mot clé figurant dans la liste Keyword_swift est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3210">A keyword from Keyword_swift is found.</span></span>

```
<Entity id="cb2ab58c-9cb8-4c81-baf8-a4e106791df4" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_swift" />
        <Match idRef="Keyword_swift" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-3211">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-3211">Keywords</span></span>
   
#### <a name="keywordswift"></a><span data-ttu-id="64f1e-3212">Keyword_swift</span><span class="sxs-lookup"><span data-stu-id="64f1e-3212">Keyword_swift</span></span>

- <span data-ttu-id="64f1e-3213">organisation internationale de normalisation 9362</span><span class="sxs-lookup"><span data-stu-id="64f1e-3213">international organization for standardization 9362</span></span> 
- <span data-ttu-id="64f1e-3214">ISO 9362</span><span class="sxs-lookup"><span data-stu-id="64f1e-3214">iso 9362</span></span> 
- <span data-ttu-id="64f1e-3215">ISO9362</span><span class="sxs-lookup"><span data-stu-id="64f1e-3215">iso9362</span></span> 
- <span data-ttu-id="64f1e-3216">rapide\#</span><span class="sxs-lookup"><span data-stu-id="64f1e-3216">swift\#</span></span> 
- <span data-ttu-id="64f1e-3217">Swiftcode</span><span class="sxs-lookup"><span data-stu-id="64f1e-3217">swiftcode</span></span> 
- <span data-ttu-id="64f1e-3218">swiftnumber</span><span class="sxs-lookup"><span data-stu-id="64f1e-3218">swiftnumber</span></span> 
- <span data-ttu-id="64f1e-3219">swiftroutingnumber</span><span class="sxs-lookup"><span data-stu-id="64f1e-3219">swiftroutingnumber</span></span> 
- <span data-ttu-id="64f1e-3220">code swift</span><span class="sxs-lookup"><span data-stu-id="64f1e-3220">swift code</span></span> 
- <span data-ttu-id="64f1e-3221"># numéro swift</span><span class="sxs-lookup"><span data-stu-id="64f1e-3221">swift number #</span></span> 
- <span data-ttu-id="64f1e-3222">numéro d’acheminement swift</span><span class="sxs-lookup"><span data-stu-id="64f1e-3222">swift routing number</span></span> 
- <span data-ttu-id="64f1e-3223">numéro BIC</span><span class="sxs-lookup"><span data-stu-id="64f1e-3223">bic number</span></span> 
- <span data-ttu-id="64f1e-3224">code BIC</span><span class="sxs-lookup"><span data-stu-id="64f1e-3224">bic code</span></span> 
- <span data-ttu-id="64f1e-3225">BIC\#</span><span class="sxs-lookup"><span data-stu-id="64f1e-3225">bic \#</span></span> 
- <span data-ttu-id="64f1e-3226">BIC\#</span><span class="sxs-lookup"><span data-stu-id="64f1e-3226">bic\#</span></span> 
- <span data-ttu-id="64f1e-3227">code d’identification bancaire</span><span class="sxs-lookup"><span data-stu-id="64f1e-3227">bank identifier code</span></span> 
- <span data-ttu-id="64f1e-3228">標準化 9362</span><span class="sxs-lookup"><span data-stu-id="64f1e-3228">標準化9362</span></span> 
- <span data-ttu-id="64f1e-3229">迅速 #</span><span class="sxs-lookup"><span data-stu-id="64f1e-3229">迅速＃</span></span> 
- <span data-ttu-id="64f1e-3230">SWIFTコード</span><span class="sxs-lookup"><span data-stu-id="64f1e-3230">SWIFTコード</span></span> 
- <span data-ttu-id="64f1e-3231">SWIFT番号</span><span class="sxs-lookup"><span data-stu-id="64f1e-3231">SWIFT番号</span></span> 
- <span data-ttu-id="64f1e-3232">迅速なルーティング番号</span><span class="sxs-lookup"><span data-stu-id="64f1e-3232">迅速なルーティング番号</span></span> 
- <span data-ttu-id="64f1e-3233">BIC番号</span><span class="sxs-lookup"><span data-stu-id="64f1e-3233">BIC番号</span></span> 
- <span data-ttu-id="64f1e-3234">BICコード</span><span class="sxs-lookup"><span data-stu-id="64f1e-3234">BICコード</span></span> 
- <span data-ttu-id="64f1e-3235">銀行識別コードのための国際組織</span><span class="sxs-lookup"><span data-stu-id="64f1e-3235">銀行識別コードのための国際組織</span></span> 
- <span data-ttu-id="64f1e-3236">Organisation internationale de normalisation 9362</span><span class="sxs-lookup"><span data-stu-id="64f1e-3236">Organisation internationale de normalisation 9362</span></span> 
- <span data-ttu-id="64f1e-3237">rapide\#</span><span class="sxs-lookup"><span data-stu-id="64f1e-3237">rapide \#</span></span> 
- <span data-ttu-id="64f1e-3238">code SWIFT</span><span class="sxs-lookup"><span data-stu-id="64f1e-3238">code SWIFT</span></span> 
- <span data-ttu-id="64f1e-3239">le numéro de swift</span><span class="sxs-lookup"><span data-stu-id="64f1e-3239">le numéro de swift</span></span> 
- <span data-ttu-id="64f1e-3240">swift numéro d’acheminement</span><span class="sxs-lookup"><span data-stu-id="64f1e-3240">swift numéro d'acheminement</span></span> 
- <span data-ttu-id="64f1e-3241">le numéro BIC</span><span class="sxs-lookup"><span data-stu-id="64f1e-3241">le numéro BIC</span></span> 
- <span data-ttu-id="64f1e-3242">\#BIC</span><span class="sxs-lookup"><span data-stu-id="64f1e-3242">\# BIC</span></span> 
- <span data-ttu-id="64f1e-3243">code identificateur de banque</span><span class="sxs-lookup"><span data-stu-id="64f1e-3243">code identificateur de banque</span></span> 
   
## <a name="taiwan-national-id"></a><span data-ttu-id="64f1e-3244">ID national à Taïwan</span><span class="sxs-lookup"><span data-stu-id="64f1e-3244">Taiwan National ID</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-3245">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-3245">Format</span></span>

<span data-ttu-id="64f1e-3246">Une lettre  suivie de neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-3246">One letter (in English) followed by nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-3247">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3247">Pattern</span></span>

<span data-ttu-id="64f1e-3248">Une lettre suivie de neuf chiffres :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3248">One letter (in English) followed by nine digits:</span></span>
- <span data-ttu-id="64f1e-3249">Une lettre (en anglais, ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="64f1e-3249">One letter (in English, not case sensitive)</span></span> 
- <span data-ttu-id="64f1e-3250">Le chiffre « 1 » ou « 2 »</span><span class="sxs-lookup"><span data-stu-id="64f1e-3250">The digit "1" or "2"</span></span> 
- <span data-ttu-id="64f1e-3251">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-3251">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-3252">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3252">Checksum</span></span>

<span data-ttu-id="64f1e-3253">Oui</span><span class="sxs-lookup"><span data-stu-id="64f1e-3253">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-3254">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-3254">Definition</span></span>

<span data-ttu-id="64f1e-3255">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3255">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-3256">La fonction Func_taiwanese_national_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3256">The function Func_taiwanese_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-3257">Un mot clé figurant dans la liste Keyword_taiwanese_national_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3257">A keyword from Keyword_taiwanese_national_id is found.</span></span>
- <span data-ttu-id="64f1e-3258">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3258">The checksum passes.</span></span>

```
<!-- Taiwanese National ID -->
<Entity id="4C7BFC34-8DD1-421D-8FB7-6C6182C2AF03" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_taiwanese_national_id" />
          <Match idRef="Keyword_taiwanese_national_id" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-3259">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-3259">Keywords</span></span>

#### <a name="keywordtaiwanesenationalid"></a><span data-ttu-id="64f1e-3260">Keyword_taiwanese_national_id</span><span class="sxs-lookup"><span data-stu-id="64f1e-3260">Keyword_taiwanese_national_id</span></span>

- <span data-ttu-id="64f1e-3261">身份證字號</span><span class="sxs-lookup"><span data-stu-id="64f1e-3261">身份證字號</span></span> 
- <span data-ttu-id="64f1e-3262">身份證</span><span class="sxs-lookup"><span data-stu-id="64f1e-3262">身份證</span></span> 
- <span data-ttu-id="64f1e-3263">身份證號碼</span><span class="sxs-lookup"><span data-stu-id="64f1e-3263">身份證號碼</span></span> 
- <span data-ttu-id="64f1e-3264">身份證號</span><span class="sxs-lookup"><span data-stu-id="64f1e-3264">身份證號</span></span> 
- <span data-ttu-id="64f1e-3265">身分證字號</span><span class="sxs-lookup"><span data-stu-id="64f1e-3265">身分證字號</span></span> 
- <span data-ttu-id="64f1e-3266">身分證</span><span class="sxs-lookup"><span data-stu-id="64f1e-3266">身分證</span></span> 
- <span data-ttu-id="64f1e-3267">身分證號碼</span><span class="sxs-lookup"><span data-stu-id="64f1e-3267">身分證號碼</span></span> 
- <span data-ttu-id="64f1e-3268">身份證號</span><span class="sxs-lookup"><span data-stu-id="64f1e-3268">身份證號</span></span> 
- <span data-ttu-id="64f1e-3269">身分證統一編號</span><span class="sxs-lookup"><span data-stu-id="64f1e-3269">身分證統一編號</span></span> 
- <span data-ttu-id="64f1e-3270">國民身分證統一編號</span><span class="sxs-lookup"><span data-stu-id="64f1e-3270">國民身分證統一編號</span></span> 
- <span data-ttu-id="64f1e-3271">簽名</span><span class="sxs-lookup"><span data-stu-id="64f1e-3271">簽名</span></span> 
- <span data-ttu-id="64f1e-3272">蓋章</span><span class="sxs-lookup"><span data-stu-id="64f1e-3272">蓋章</span></span> 
- <span data-ttu-id="64f1e-3273">簽名或蓋章</span><span class="sxs-lookup"><span data-stu-id="64f1e-3273">簽名或蓋章</span></span> 
- <span data-ttu-id="64f1e-3274">簽章</span><span class="sxs-lookup"><span data-stu-id="64f1e-3274">簽章</span></span>   
   
## <a name="taiwan-passport-number"></a><span data-ttu-id="64f1e-3275">	Numéro de passeport Taïwan</span><span class="sxs-lookup"><span data-stu-id="64f1e-3275">Taiwan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-3276">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-3276">Format</span></span>

- <span data-ttu-id="64f1e-3277">Numéro de passeport biométrique: neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-3277">Biometric passport number: Nine digits</span></span>
- <span data-ttu-id="64f1e-3278">Numéro de passeport non biométrique: neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-3278">Non-biometric passport number: Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-3279">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3279">Pattern</span></span>
<span data-ttu-id="64f1e-3280">Numéro de passeport biométrique:</span><span class="sxs-lookup"><span data-stu-id="64f1e-3280">Biometric passport number:</span></span>
- <span data-ttu-id="64f1e-3281">Le chiffre « 3 » </span><span class="sxs-lookup"><span data-stu-id="64f1e-3281">The digit "3"</span></span> 
- <span data-ttu-id="64f1e-3282">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-3282">Eight digits</span></span>

<span data-ttu-id="64f1e-3283">Numéro de passeport non biométrique:</span><span class="sxs-lookup"><span data-stu-id="64f1e-3283">Non-biometric passport number:</span></span>
- <span data-ttu-id="64f1e-3284">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-3284">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-3285">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3285">Checksum</span></span>

<span data-ttu-id="64f1e-3286">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-3286">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-3287">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-3287">Definition</span></span>

<span data-ttu-id="64f1e-3288">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3288">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-3289">L’expression régulière Regex_taiwan_passport trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3289">The regular expression Regex_taiwan_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-3290">Un mot clé figurant dans la liste Keyword_taiwan_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3290">A keyword from Keyword_taiwan_passport is found.</span></span>

```
<!-- Taiwan Passport Number -->
<Entity id="e7251cb4-4c2c-41df-963e-924eb3dae04a" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_passport"/>
     <Match idRef="Keyword_taiwan_passport"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-3291">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-3291">Keywords</span></span>

#### <a name="keywordtaiwanpassport"></a><span data-ttu-id="64f1e-3292">Keyword_taiwan_passport</span><span class="sxs-lookup"><span data-stu-id="64f1e-3292">Keyword_taiwan_passport</span></span>

- <span data-ttu-id="64f1e-3293">ROC passport number</span><span class="sxs-lookup"><span data-stu-id="64f1e-3293">ROC passport number</span></span> 
- <span data-ttu-id="64f1e-3294">Passport number</span><span class="sxs-lookup"><span data-stu-id="64f1e-3294">Passport number</span></span> 
- <span data-ttu-id="64f1e-3295">Passport no</span><span class="sxs-lookup"><span data-stu-id="64f1e-3295">Passport no</span></span> 
- <span data-ttu-id="64f1e-3296">Passport Num</span><span class="sxs-lookup"><span data-stu-id="64f1e-3296">Passport Num</span></span> 
- <span data-ttu-id="64f1e-3297">Passport #</span><span class="sxs-lookup"><span data-stu-id="64f1e-3297">Passport #</span></span> 
- <span data-ttu-id="64f1e-3298">护照</span><span class="sxs-lookup"><span data-stu-id="64f1e-3298">护照</span></span> 
- <span data-ttu-id="64f1e-3299">中華民國護照</span><span class="sxs-lookup"><span data-stu-id="64f1e-3299">中華民國護照</span></span> 
- <span data-ttu-id="64f1e-3300">Zhōnghuá Mínguó hùzhào</span><span class="sxs-lookup"><span data-stu-id="64f1e-3300">Zhōnghuá Mínguó hùzhào</span></span>
   
## <a name="taiwan-resident-certificate-arctarc-number"></a><span data-ttu-id="64f1e-3301">Numéro de certificat de résident (ARC/TARC) Taïwan</span><span class="sxs-lookup"><span data-stu-id="64f1e-3301">Taiwan Resident Certificate (ARC/TARC) Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-3302">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-3302">Format</span></span>

<span data-ttu-id="64f1e-3303">10 lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-3303">10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-3304">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3304">Pattern</span></span>

<span data-ttu-id="64f1e-3305">10 lettres et chiffres :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3305">10 letters and digits:</span></span>
- <span data-ttu-id="64f1e-3306">Deux lettres (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="64f1e-3306">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="64f1e-3307">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-3307">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-3308">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3308">Checksum</span></span>

<span data-ttu-id="64f1e-3309">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-3309">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-3310">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-3310">Definition</span></span>

<span data-ttu-id="64f1e-3311">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3311">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-3312">L’expression régulière Regex_taiwan_resident_certificate trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3312">The regular expression Regex_taiwan_resident_certificate finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-3313">Un mot clé figurant dans la liste Keyword_taiwan_resident_certificate est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3313">A keyword from Keyword_taiwan_resident_certificate is found.</span></span>

```
<!-- Taiwan Resident Certificate (ARC/TARC) -->
<Entity id="48269fec-05ea-46ea-b326-f5623a58c6e9" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_resident_certificate"/>
     <Match idRef="Keyword_taiwan_resident_certificate"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-3314">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-3314">Keywords</span></span>

#### <a name="keywordtaiwanresidentcertificate"></a><span data-ttu-id="64f1e-3315">Keyword_taiwan_resident_certificate</span><span class="sxs-lookup"><span data-stu-id="64f1e-3315">Keyword_taiwan_resident_certificate</span></span>

- <span data-ttu-id="64f1e-3316">Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="64f1e-3316">Resident Certificate</span></span> 
- <span data-ttu-id="64f1e-3317">Resident Cert</span><span class="sxs-lookup"><span data-stu-id="64f1e-3317">Resident Cert</span></span> 
- <span data-ttu-id="64f1e-3318">Resident Cert.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3318">Resident Cert.</span></span> 
- <span data-ttu-id="64f1e-3319">Identification card</span><span class="sxs-lookup"><span data-stu-id="64f1e-3319">Identification card</span></span> 
- <span data-ttu-id="64f1e-3320">Alien Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="64f1e-3320">Alien Resident Certificate</span></span> 
- <span data-ttu-id="64f1e-3321">ARC</span><span class="sxs-lookup"><span data-stu-id="64f1e-3321">ARC</span></span> 
- <span data-ttu-id="64f1e-3322">Taiwan Area Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="64f1e-3322">Taiwan Area Resident Certificate</span></span> 
- <span data-ttu-id="64f1e-3323">TARC</span><span class="sxs-lookup"><span data-stu-id="64f1e-3323">TARC</span></span> 
- <span data-ttu-id="64f1e-3324">居留證</span><span class="sxs-lookup"><span data-stu-id="64f1e-3324">居留證</span></span> 
- <span data-ttu-id="64f1e-3325">外僑居留證</span><span class="sxs-lookup"><span data-stu-id="64f1e-3325">外僑居留證</span></span> 
- <span data-ttu-id="64f1e-3326">台灣地區居留證</span><span class="sxs-lookup"><span data-stu-id="64f1e-3326">台灣地區居留證</span></span> 

## <a name="thai-population-identification-code"></a><span data-ttu-id="64f1e-3327">Code d'identification du remplissage thaï</span><span class="sxs-lookup"><span data-stu-id="64f1e-3327">Thai Population Identification Code</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-3328">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-3328">Format</span></span>

<span data-ttu-id="64f1e-3329">13 chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-3329">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-3330">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3330">Pattern</span></span>

<span data-ttu-id="64f1e-3331">13 chiffres :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3331">13 digits:</span></span>
- <span data-ttu-id="64f1e-3332">Le premier chiffre est différent de 0 ou de 9</span><span class="sxs-lookup"><span data-stu-id="64f1e-3332">First digit is not 0 or 9</span></span> 
- <span data-ttu-id="64f1e-3333">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-3333">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-3334">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3334">Checksum</span></span>

<span data-ttu-id="64f1e-3335">Oui</span><span class="sxs-lookup"><span data-stu-id="64f1e-3335">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-3336">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-3336">Definition</span></span>

<span data-ttu-id="64f1e-3337">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3337">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-3338">La fonction Func_Thai_Citizen_Id trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3338">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-3339">Un mot clé depuis Keyword_Thai_Citizen_Id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3339">A keyword from Keyword_Thai_Citizen_Id is found.</span></span>

<span data-ttu-id="64f1e-3340">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3340">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-3341">La fonction Func_Thai_Citizen_Id trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3341">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>

```
<!-- Thai Citizen ID -->
-<Entity id="44ca9e86-ead7-4c5d-884a-e2eaa401515e" recommendedConfidence="75" patternsProximity="300">
   -<Pattern confidenceLevel="85">
      <IdMatch idRef="Func_Thai_Citizen_Id"/>
      <Match idRef="Keyword_Thai_Citizen_Id"/>
   </Pattern>
   -<Pattern confidenceLevel="75">
      <IdMatch idRef="Func_Thai_Citizen_Id"/>
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-3342">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-3342">Keywords</span></span>

#### <a name="keywordthaicitizenid"></a><span data-ttu-id="64f1e-3343">Keyword_Thai_Citizen_Id</span><span class="sxs-lookup"><span data-stu-id="64f1e-3343">Keyword_Thai_Citizen_Id</span></span>

- <span data-ttu-id="64f1e-3344">ID Number</span><span class="sxs-lookup"><span data-stu-id="64f1e-3344">ID Number</span></span>
- <span data-ttu-id="64f1e-3345">Numéro d'identification</span><span class="sxs-lookup"><span data-stu-id="64f1e-3345">Identification Number</span></span>
- <span data-ttu-id="64f1e-3346">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="64f1e-3346">บัตรประชาชน</span></span>
- <span data-ttu-id="64f1e-3347">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="64f1e-3347">รหัสบัตรประชาชน</span></span>
- <span data-ttu-id="64f1e-3348">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="64f1e-3348">บัตรประชาชน</span></span>
- <span data-ttu-id="64f1e-3349">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="64f1e-3349">รหัสบัตรประชาชน</span></span>
  
## <a name="turkish-national-identification-number"></a><span data-ttu-id="64f1e-3350">Numéro d'identification national turc</span><span class="sxs-lookup"><span data-stu-id="64f1e-3350">Turkish National Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-3351">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-3351">Format</span></span>

<span data-ttu-id="64f1e-3352">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-3352">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-3353">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3353">Pattern</span></span>

<span data-ttu-id="64f1e-3354">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-3354">11 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-3355">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3355">Checksum</span></span>

<span data-ttu-id="64f1e-3356">Oui</span><span class="sxs-lookup"><span data-stu-id="64f1e-3356">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-3357">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-3357">Definition</span></span>

<span data-ttu-id="64f1e-3358">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3358">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-3359">La fonction Func_Turkish_National_Id trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3359">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-3360">Un mot clé depuis Keyword_Turkish_National_Id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3360">A keyword from Keyword_Turkish_National_Id is found.</span></span>

<span data-ttu-id="64f1e-3361">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3361">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-3362">La fonction Func_Turkish_National_Id trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3362">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>

```
<!-- Turkish National Identity -->
-<Entity id="fb621f20-3876-4cfc-acec-8c8e73ca32c7" recommendedConfidence="75" patternsProximity="300">
   -<Pattern confidenceLevel="85">
      <IdMatch idRef="Func_Turkish_National_Id"/>
      <Match idRef="Keyword_Turkish_National_Id"/>
   </Pattern>
   -<Pattern confidenceLevel="75">
      <IdMatch idRef="Func_Turkish_National_Id"/>
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-3363">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-3363">Keywords</span></span>

#### <a name="keywordturkishnationalid"></a><span data-ttu-id="64f1e-3364">Keyword_Turkish_National_Id</span><span class="sxs-lookup"><span data-stu-id="64f1e-3364">Keyword_Turkish_National_Id</span></span>

- <span data-ttu-id="64f1e-3365">TC Kimlik non</span><span class="sxs-lookup"><span data-stu-id="64f1e-3365">TC Kimlik No</span></span>
- <span data-ttu-id="64f1e-3366">TC Kimlik numarası</span><span class="sxs-lookup"><span data-stu-id="64f1e-3366">TC Kimlik numarası</span></span>
- <span data-ttu-id="64f1e-3367">Vatandaşlık numarası</span><span class="sxs-lookup"><span data-stu-id="64f1e-3367">Vatandaşlık numarası</span></span>
- <span data-ttu-id="64f1e-3368">Vatandaşlık non</span><span class="sxs-lookup"><span data-stu-id="64f1e-3368">Vatandaşlık no</span></span>

## <a name="uk-drivers-license-number"></a><span data-ttu-id="64f1e-p141">Numéro de permis de conduire Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="64f1e-p141">U.K. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-3371">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-3371">Format</span></span>

<span data-ttu-id="64f1e-3372">Combinaison de 18 lettres et chiffres au format spécifié</span><span class="sxs-lookup"><span data-stu-id="64f1e-3372">Combination of 18 letters and digits in the specified format</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-3373">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3373">Pattern</span></span>

<span data-ttu-id="64f1e-3374">18 lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-3374">18 letters and digits:</span></span>
- <span data-ttu-id="64f1e-3375">Cinq lettres (ne respectent pas la casse) ou le chiffre « 9 » à la place d’une lettre</span><span class="sxs-lookup"><span data-stu-id="64f1e-3375">Five letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="64f1e-3376">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="64f1e-3376">One digit</span></span> 
- <span data-ttu-id="64f1e-3377">Cinq chiffres au format de date JJMMA pour la date de naissance</span><span class="sxs-lookup"><span data-stu-id="64f1e-3377">Five digits in the date format DDMMY for date of birth</span></span> 
- <span data-ttu-id="64f1e-3378">Deux lettres (ne respectent pas la casse) ou le chiffre « 9 » à la place d’une lettre</span><span class="sxs-lookup"><span data-stu-id="64f1e-3378">Two letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="64f1e-3379">Cinq chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-3379">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-3380">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3380">Checksum</span></span>

<span data-ttu-id="64f1e-3381">Oui</span><span class="sxs-lookup"><span data-stu-id="64f1e-3381">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-3382">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-3382">Definition</span></span>

<span data-ttu-id="64f1e-3383">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3383">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-3384">La fonction Func_uk_drivers_license trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3384">The function Func_uk_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-3385">Un mot clé figurant dans la liste Keyword_uk_drivers_license est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3385">A keyword from Keyword_uk_drivers_license is found.</span></span>
- <span data-ttu-id="64f1e-3386">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3386">The checksum passes.</span></span>

```
<!-- U.K. Driver's License Number -->
<Entity id="f93de4be-d94c-40df-a8be-461738047551" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_uk_drivers_license" />
        <Match idRef="Keyword_uk_drivers_license" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-3387">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-3387">Keywords</span></span>

#### <a name="keywordukdriverslicense"></a><span data-ttu-id="64f1e-3388">Keyword_uk_drivers_license</span><span class="sxs-lookup"><span data-stu-id="64f1e-3388">Keyword_uk_drivers_license</span></span>

- <span data-ttu-id="64f1e-3389">DVLA</span><span class="sxs-lookup"><span data-stu-id="64f1e-3389">DVLA</span></span> 
- <span data-ttu-id="64f1e-3390">véhicule utilitaire léger</span><span class="sxs-lookup"><span data-stu-id="64f1e-3390">light vans</span></span> 
- <span data-ttu-id="64f1e-3391">Quadbikes</span><span class="sxs-lookup"><span data-stu-id="64f1e-3391">quadbikes</span></span> 
- <span data-ttu-id="64f1e-3392">automobiles</span><span class="sxs-lookup"><span data-stu-id="64f1e-3392">motor cars</span></span> 
- <span data-ttu-id="64f1e-3393">125cc</span><span class="sxs-lookup"><span data-stu-id="64f1e-3393">125cc</span></span> 
- <span data-ttu-id="64f1e-3394">annexes</span><span class="sxs-lookup"><span data-stu-id="64f1e-3394">sidecar</span></span> 
- <span data-ttu-id="64f1e-3395">tricycles</span><span class="sxs-lookup"><span data-stu-id="64f1e-3395">tricycles</span></span> 
- <span data-ttu-id="64f1e-3396">Side</span><span class="sxs-lookup"><span data-stu-id="64f1e-3396">motorcycles</span></span> 
- <span data-ttu-id="64f1e-3397">permis de conduire plastifié</span><span class="sxs-lookup"><span data-stu-id="64f1e-3397">photocard licence</span></span> 
- <span data-ttu-id="64f1e-3398">apprentis conducteurs</span><span class="sxs-lookup"><span data-stu-id="64f1e-3398">learner drivers</span></span> 
- <span data-ttu-id="64f1e-3399">titulaire du permis</span><span class="sxs-lookup"><span data-stu-id="64f1e-3399">licence holder</span></span> 
- <span data-ttu-id="64f1e-3400">titulaires du permis</span><span class="sxs-lookup"><span data-stu-id="64f1e-3400">licence holders</span></span> 
- <span data-ttu-id="64f1e-3401">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-3401">driving licences</span></span> 
- <span data-ttu-id="64f1e-3402">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-3402">driving licence</span></span> 
- <span data-ttu-id="64f1e-3403">voiture à double commande</span><span class="sxs-lookup"><span data-stu-id="64f1e-3403">dual control car</span></span> 
   
## <a name="uk-electoral-roll-number"></a><span data-ttu-id="64f1e-p142">Numéro de liste électorale Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="64f1e-p142">U.K. Electoral Roll Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-3406">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-3406">Format</span></span>

<span data-ttu-id="64f1e-3407">Deux lettres suivies de 1 à 4 chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-3407">Two letters followed by 1-4 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-3408">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3408">Pattern</span></span>

<span data-ttu-id="64f1e-3409">Deux lettres (ne respectant pas la casse) suivies de 1 à 4 chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-3409">Two letters (not case sensitive) followed by 1-4 numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-3410">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3410">Checksum</span></span>

<span data-ttu-id="64f1e-3411">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-3411">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-3412">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-3412">Definition</span></span>

<span data-ttu-id="64f1e-3413">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3413">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-3414">L’expression régulière Regex_uk_electoral trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3414">The regular expression Regex_uk_electoral finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-3415">Un mot clé figurant dans la liste Keyword_uk_electoral est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3415">A keyword from Keyword_uk_electoral is found.</span></span>

```
<!-- U.K. Electoral Number -->
<Entity id="a3eea206-dc0c-4f06-9e22-aa1be3059963" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_uk_electoral" />
        <Any minMatches="1">
          <Match idRef="Keyword_uk_electoral" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-3416">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-3416">Keywords</span></span>

#### <a name="keywordukelectoral"></a><span data-ttu-id="64f1e-3417">Keyword_uk_electoral</span><span class="sxs-lookup"><span data-stu-id="64f1e-3417">Keyword_uk_electoral</span></span>

- <span data-ttu-id="64f1e-3418">nomination au conseil</span><span class="sxs-lookup"><span data-stu-id="64f1e-3418">council nomination</span></span> 
- <span data-ttu-id="64f1e-3419">formulaire de nomination</span><span class="sxs-lookup"><span data-stu-id="64f1e-3419">nomination form</span></span> 
- <span data-ttu-id="64f1e-3420">registre électoral</span><span class="sxs-lookup"><span data-stu-id="64f1e-3420">electoral register</span></span> 
- <span data-ttu-id="64f1e-3421">liste électorale</span><span class="sxs-lookup"><span data-stu-id="64f1e-3421">electoral roll</span></span>

   
## <a name="uk-national-health-service-number"></a><span data-ttu-id="64f1e-p143">Numéro national des services de santé Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="64f1e-p143">U.K. National Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-3424">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-3424">Format</span></span>

<span data-ttu-id="64f1e-3425">10 à 17 chiffres séparés par des espaces</span><span class="sxs-lookup"><span data-stu-id="64f1e-3425">10-17 digits separated by spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-3426">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3426">Pattern</span></span>

<span data-ttu-id="64f1e-3427">10 à 17 chiffres :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3427">10-17 digits:</span></span>
- <span data-ttu-id="64f1e-3428">3 ou 10 chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-3428">Either 3 or 10 digits</span></span> 
- <span data-ttu-id="64f1e-3429">Un espace</span><span class="sxs-lookup"><span data-stu-id="64f1e-3429">A space</span></span> 
- <span data-ttu-id="64f1e-3430">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-3430">Three digits</span></span> 
- <span data-ttu-id="64f1e-3431">Un espace</span><span class="sxs-lookup"><span data-stu-id="64f1e-3431">A space</span></span> 
- <span data-ttu-id="64f1e-3432">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-3432">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-3433">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3433">Checksum</span></span>

<span data-ttu-id="64f1e-3434">Oui</span><span class="sxs-lookup"><span data-stu-id="64f1e-3434">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-3435">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-3435">Definition</span></span>

<span data-ttu-id="64f1e-3436">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3436">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-3437">La fonction Func_uk_nhs_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3437">The function Func_uk_nhs_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-3438">L’une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3438">One of the following is true:</span></span>
    - <span data-ttu-id="64f1e-3439">Un mot clé figurant dans la liste Keyword_uk_nhs_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3439">A keyword from Keyword_uk_nhs_number is found.</span></span>
    - <span data-ttu-id="64f1e-3440">Un mot clé figurant dans la liste Keyword_uk_nhs_number1 est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3440">A keyword from Keyword_uk_nhs_number1 is found.</span></span>
    - <span data-ttu-id="64f1e-3441">Un mot clé figurant dans la liste Keyword_uk_nhs_number_dob est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3441">A keyword from Keyword_uk_nhs_number_dob is found.</span></span>
- <span data-ttu-id="64f1e-3442">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3442">The checksum passes.</span></span>

```
<!-- U.K. NHS Number -->
<Entity id="3192014e-2a16-44e9-aa69-4b20375c9a78" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_uk_nhs_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_uk_nhs_number" />
          <Match idRef="Keyword_uk_nhs_number1" />
          <Match idRef="Keyword_uk_nhs_number_dob" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-3443">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-3443">Keywords</span></span>
   
#### <a name="keyworduknhsnumber"></a><span data-ttu-id="64f1e-3444">Keyword_uk_nhs_number</span><span class="sxs-lookup"><span data-stu-id="64f1e-3444">Keyword_uk_nhs_number</span></span>

- <span data-ttu-id="64f1e-3445">service national de santé</span><span class="sxs-lookup"><span data-stu-id="64f1e-3445">national health service</span></span> 
- <span data-ttu-id="64f1e-3446">NHS</span><span class="sxs-lookup"><span data-stu-id="64f1e-3446">nhs</span></span> 
- <span data-ttu-id="64f1e-3447">administration des services de santé</span><span class="sxs-lookup"><span data-stu-id="64f1e-3447">health services authority</span></span> 
- <span data-ttu-id="64f1e-3448">administration de la santé</span><span class="sxs-lookup"><span data-stu-id="64f1e-3448">health authority</span></span>

#### <a name="keyworduknhsnumber1"></a><span data-ttu-id="64f1e-3449">Keyword_uk_nhs_number1</span><span class="sxs-lookup"><span data-stu-id="64f1e-3449">Keyword_uk_nhs_number1</span></span>

- <span data-ttu-id="64f1e-3450">id du patient</span><span class="sxs-lookup"><span data-stu-id="64f1e-3450">patient id</span></span> 
- <span data-ttu-id="64f1e-3451">identification du patient</span><span class="sxs-lookup"><span data-stu-id="64f1e-3451">patient identification</span></span> 
- <span data-ttu-id="64f1e-3452">n° patient</span><span class="sxs-lookup"><span data-stu-id="64f1e-3452">patient no</span></span> 
- <span data-ttu-id="64f1e-3453">numéro de patient</span><span class="sxs-lookup"><span data-stu-id="64f1e-3453">patient number</span></span>

#### <a name="keyworduknhsnumberdob"></a><span data-ttu-id="64f1e-3454">Keyword_uk_nhs_number_dob</span><span class="sxs-lookup"><span data-stu-id="64f1e-3454">Keyword_uk_nhs_number_dob</span></span>

- <span data-ttu-id="64f1e-3455">GP</span><span class="sxs-lookup"><span data-stu-id="64f1e-3455">GP</span></span> 
- <span data-ttu-id="64f1e-3456">DOB</span><span class="sxs-lookup"><span data-stu-id="64f1e-3456">DOB</span></span> 
- <span data-ttu-id="64f1e-3457">D. O. B</span><span class="sxs-lookup"><span data-stu-id="64f1e-3457">D.O.B</span></span> 
- <span data-ttu-id="64f1e-3458">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="64f1e-3458">Date of Birth</span></span> 
- <span data-ttu-id="64f1e-3459">Birth Date</span><span class="sxs-lookup"><span data-stu-id="64f1e-3459">Birth Date</span></span> 
   
## <a name="uk-national-insurance-number-nino"></a><span data-ttu-id="64f1e-p144">Numéro d'assurance nationale (NINO) Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="64f1e-p144">U.K. National Insurance Number (NINO)</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-3462">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-3462">Format</span></span>

<span data-ttu-id="64f1e-3463">7 caractères ou 9 caractères séparés par des espaces ou des tirets</span><span class="sxs-lookup"><span data-stu-id="64f1e-3463">7 characters or 9 characters separated by spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-3464">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3464">Pattern</span></span>

<span data-ttu-id="64f1e-3465">Deux modèles possibles:</span><span class="sxs-lookup"><span data-stu-id="64f1e-3465">Two possible patterns:</span></span>

- <span data-ttu-id="64f1e-3466">Deux lettres (valides NINOs Utilisez uniquement certains caractères dans ce préfixe, que ce modèle valide; ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="64f1e-3466">Two letters (valid NINOs use only certain characters in this prefix, which this pattern validates; not case sensitive)</span></span>
- <span data-ttu-id="64f1e-3467">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-3467">Six digits</span></span>
- <span data-ttu-id="64f1e-3468">«A», «B», «C» ou «d» (comme le préfixe, seuls certains caractères sont autorisés dans le suffixe; ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="64f1e-3468">Either 'A', 'B', 'C', or 'D' (like the prefix, only certain characters are allowed in the suffix; not case sensitive)</span></span>

<span data-ttu-id="64f1e-3469">OU</span><span class="sxs-lookup"><span data-stu-id="64f1e-3469">OR</span></span>

- <span data-ttu-id="64f1e-3470">Deux lettres</span><span class="sxs-lookup"><span data-stu-id="64f1e-3470">Two letters</span></span>
- <span data-ttu-id="64f1e-3471">Un espace ou un tiret</span><span class="sxs-lookup"><span data-stu-id="64f1e-3471">A space or dash</span></span>
- <span data-ttu-id="64f1e-3472">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-3472">Two digits</span></span>
- <span data-ttu-id="64f1e-3473">Un espace ou un tiret</span><span class="sxs-lookup"><span data-stu-id="64f1e-3473">A space or dash</span></span>
- <span data-ttu-id="64f1e-3474">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-3474">Two digits</span></span>
- <span data-ttu-id="64f1e-3475">Un espace ou un tiret</span><span class="sxs-lookup"><span data-stu-id="64f1e-3475">A space or dash</span></span>
- <span data-ttu-id="64f1e-3476">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-3476">Two digits</span></span>
- <span data-ttu-id="64f1e-3477">Un espace ou un tiret</span><span class="sxs-lookup"><span data-stu-id="64f1e-3477">A space or dash</span></span>
- <span data-ttu-id="64f1e-3478">«A», «B», «C» ou «d»</span><span class="sxs-lookup"><span data-stu-id="64f1e-3478">Either 'A', 'B', 'C', or 'D'</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-3479">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3479">Checksum</span></span>

<span data-ttu-id="64f1e-3480">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-3480">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-3481">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-3481">Definition</span></span>

<span data-ttu-id="64f1e-3482">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3482">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-3483">La fonction Func_uk_nino trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3483">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-3484">Un mot clé figurant dans la liste Keyword_uk_nino est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3484">A keyword from Keyword_uk_nino is found.</span></span>

<span data-ttu-id="64f1e-3485">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3485">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-3486">La fonction Func_uk_nino trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3486">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-3487">Aucun mot clé figurant dans la liste Keyword_uk_nino n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3487">No keyword from Keyword_uk_nino is found.</span></span>

```
<!-- U.K. NINO -->
<Entity id="16c07343-c26f-49d2-a987-3daf717e94cc" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_uk_nino" />
        <Any minMatches="1">
          <Match idRef="Keyword_uk_nino" />
        </Any>
    </Pattern>    
     <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_uk_nino" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_uk_nino" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-3488">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-3488">Keywords</span></span>

#### <a name="keyworduknino"></a><span data-ttu-id="64f1e-3489">Keyword_uk_nino</span><span class="sxs-lookup"><span data-stu-id="64f1e-3489">Keyword_uk_nino</span></span>

- <span data-ttu-id="64f1e-3490">numéro d’assurance nationale</span><span class="sxs-lookup"><span data-stu-id="64f1e-3490">national insurance number</span></span> 
- <span data-ttu-id="64f1e-3491">cotisations sociales</span><span class="sxs-lookup"><span data-stu-id="64f1e-3491">national insurance contributions</span></span> 
- <span data-ttu-id="64f1e-3492">loi sur la protection</span><span class="sxs-lookup"><span data-stu-id="64f1e-3492">protection act</span></span> 
- <span data-ttu-id="64f1e-3493">cotisations</span><span class="sxs-lookup"><span data-stu-id="64f1e-3493">insurance</span></span> 
- <span data-ttu-id="64f1e-3494">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="64f1e-3494">social security number</span></span> 
- <span data-ttu-id="64f1e-3495">demande d’assurance</span><span class="sxs-lookup"><span data-stu-id="64f1e-3495">insurance application</span></span> 
- <span data-ttu-id="64f1e-3496">demande de soins médicaux</span><span class="sxs-lookup"><span data-stu-id="64f1e-3496">medical application</span></span> 
- <span data-ttu-id="64f1e-3497">assurance sociale</span><span class="sxs-lookup"><span data-stu-id="64f1e-3497">social insurance</span></span> 
- <span data-ttu-id="64f1e-3498">soins médicaux</span><span class="sxs-lookup"><span data-stu-id="64f1e-3498">medical attention</span></span> 
- <span data-ttu-id="64f1e-3499">sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="64f1e-3499">social security</span></span> 
- <span data-ttu-id="64f1e-3500">grande-bretagne</span><span class="sxs-lookup"><span data-stu-id="64f1e-3500">great britain</span></span> 
- <span data-ttu-id="64f1e-3501">cotisations</span><span class="sxs-lookup"><span data-stu-id="64f1e-3501">insurance</span></span>    
   
## <a name="us--uk-passport-number"></a><span data-ttu-id="64f1e-p145">Numéro de passeport États-Unis/Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="64f1e-p145">U.S. / U.K. Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-3504">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-3504">Format</span></span>

<span data-ttu-id="64f1e-3505">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-3505">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-3506">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3506">Pattern</span></span>

<span data-ttu-id="64f1e-3507">Neuf chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="64f1e-3507">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-3508">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3508">Checksum</span></span>

<span data-ttu-id="64f1e-3509">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-3509">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-3510">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-3510">Definition</span></span>

<span data-ttu-id="64f1e-3511">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3511">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-3512">La fonction Func_usa_uk_passport trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3512">The function Func_usa_uk_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-3513">Un mot clé figurant dans la liste Keyword_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3513">A keyword from Keyword_passport is found.</span></span>

```
<Entity id="178ec42a-18b4-47cc-85c7-d62c92fd67f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_usa_uk_passport" />
        <Match idRef="Keyword_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-3514">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-3514">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="64f1e-3515">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="64f1e-3515">Keyword_passport</span></span>

- <span data-ttu-id="64f1e-3516">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="64f1e-3516">Passport Number</span></span> 
- <span data-ttu-id="64f1e-3517">N° de passeport</span><span class="sxs-lookup"><span data-stu-id="64f1e-3517">Passport No</span></span> 
- <span data-ttu-id="64f1e-3518"># Passeport</span><span class="sxs-lookup"><span data-stu-id="64f1e-3518">Passport #</span></span> 
- <span data-ttu-id="64f1e-3519">Tel</span><span class="sxs-lookup"><span data-stu-id="64f1e-3519">Passport#</span></span> 
- <span data-ttu-id="64f1e-3520">PassportID</span><span class="sxs-lookup"><span data-stu-id="64f1e-3520">PassportID</span></span> 
- <span data-ttu-id="64f1e-3521">N ° passeport</span><span class="sxs-lookup"><span data-stu-id="64f1e-3521">Passportno</span></span> 
- <span data-ttu-id="64f1e-3522">passportnumber</span><span class="sxs-lookup"><span data-stu-id="64f1e-3522">passportnumber</span></span> 
- <span data-ttu-id="64f1e-3523">パスポート</span><span class="sxs-lookup"><span data-stu-id="64f1e-3523">パスポート</span></span> 
- <span data-ttu-id="64f1e-3524">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="64f1e-3524">パスポート番号</span></span> 
- <span data-ttu-id="64f1e-3525">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="64f1e-3525">パスポートのNum</span></span> 
- <span data-ttu-id="64f1e-3526">パスポート #</span><span class="sxs-lookup"><span data-stu-id="64f1e-3526">パスポート＃</span></span> 
- <span data-ttu-id="64f1e-3527">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="64f1e-3527">Numéro de passeport</span></span> 
- <span data-ttu-id="64f1e-3528">Passeport n°</span><span class="sxs-lookup"><span data-stu-id="64f1e-3528">Passeport n °</span></span> 
- <span data-ttu-id="64f1e-3529">Passeport numéro</span><span class="sxs-lookup"><span data-stu-id="64f1e-3529">Passeport Non</span></span> 
- <span data-ttu-id="64f1e-3530"># Passeport</span><span class="sxs-lookup"><span data-stu-id="64f1e-3530">Passeport #</span></span> 
- <span data-ttu-id="64f1e-3531">Passeport</span><span class="sxs-lookup"><span data-stu-id="64f1e-3531">Passeport#</span></span> 
- <span data-ttu-id="64f1e-3532">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="64f1e-3532">PasseportNon</span></span> 
- <span data-ttu-id="64f1e-3533">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="64f1e-3533">Passeportn °</span></span> 
   
## <a name="us-bank-account-number"></a><span data-ttu-id="64f1e-3534">Numéro de compte bancaire États-Unis</span><span class="sxs-lookup"><span data-stu-id="64f1e-3534">U.S. Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-3535">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-3535">Format</span></span>

<span data-ttu-id="64f1e-3536">8-17 chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-3536">8-17 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-3537">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3537">Pattern</span></span>

<span data-ttu-id="64f1e-3538">8 à 17 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="64f1e-3538">8-17 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-3539">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3539">Checksum</span></span>

<span data-ttu-id="64f1e-3540">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-3540">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-3541">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-3541">Definition</span></span>

<span data-ttu-id="64f1e-3542">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3542">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-3543">L’expression régulière Regex_usa_bank_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3543">The regular expression Regex_usa_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-3544">Un mot clé figurant dans la liste Keyword_usa_Bank_Account est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3544">A keyword from Keyword_usa_Bank_Account is found.</span></span>

```
<!-- U.S. Bank Account Number -->
<Entity id="a2ce32a8-f935-4bb6-8e96-2a5157672e2c" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_usa_bank_account_number" />
        <Match idRef="Keyword_usa_Bank_Account" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-3545">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-3545">Keywords</span></span>

#### <a name="keywordusabankaccount"></a><span data-ttu-id="64f1e-3546">Keyword_usa_Bank_Account</span><span class="sxs-lookup"><span data-stu-id="64f1e-3546">Keyword_usa_Bank_Account</span></span>

- <span data-ttu-id="64f1e-3547">Numéro de compte courant</span><span class="sxs-lookup"><span data-stu-id="64f1e-3547">Checking Account Number</span></span> 
- <span data-ttu-id="64f1e-3548">Compte courant</span><span class="sxs-lookup"><span data-stu-id="64f1e-3548">Checking Account</span></span> 
- <span data-ttu-id="64f1e-3549"># compte courant</span><span class="sxs-lookup"><span data-stu-id="64f1e-3549">Checking Account #</span></span> 
- <span data-ttu-id="64f1e-3550">Numéro compte courant</span><span class="sxs-lookup"><span data-stu-id="64f1e-3550">Checking Acct Number</span></span> 
- <span data-ttu-id="64f1e-3551"># compte courant</span><span class="sxs-lookup"><span data-stu-id="64f1e-3551">Checking Acct #</span></span> 
- <span data-ttu-id="64f1e-3552">N° de compte courant</span><span class="sxs-lookup"><span data-stu-id="64f1e-3552">Checking Acct No.</span></span> 
- <span data-ttu-id="64f1e-3553">N° de compte courant</span><span class="sxs-lookup"><span data-stu-id="64f1e-3553">Checking Account No.</span></span> 
- <span data-ttu-id="64f1e-3554">Numéro de compte bancaire</span><span class="sxs-lookup"><span data-stu-id="64f1e-3554">Bank Account Number</span></span> 
- <span data-ttu-id="64f1e-3555"># Compte bancaire</span><span class="sxs-lookup"><span data-stu-id="64f1e-3555">Bank Account #</span></span> 
- <span data-ttu-id="64f1e-3556">Numéro de compte bancaire</span><span class="sxs-lookup"><span data-stu-id="64f1e-3556">Bank Acct Number</span></span> 
- <span data-ttu-id="64f1e-3557"># Compte bancaire</span><span class="sxs-lookup"><span data-stu-id="64f1e-3557">Bank Acct #</span></span> 
- <span data-ttu-id="64f1e-3558">N° de compte bancaire</span><span class="sxs-lookup"><span data-stu-id="64f1e-3558">Bank Acct No.</span></span> 
- <span data-ttu-id="64f1e-3559">N° de compte bancaire</span><span class="sxs-lookup"><span data-stu-id="64f1e-3559">Bank Account No.</span></span> 
- <span data-ttu-id="64f1e-3560">Numéro de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="64f1e-3560">Savings Account Number</span></span> 
- <span data-ttu-id="64f1e-3561">Compte d’épargne.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3561">Savings Account.</span></span> 
- <span data-ttu-id="64f1e-3562">N° de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="64f1e-3562">Savings Account #</span></span> 
- <span data-ttu-id="64f1e-3563">Numéro de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="64f1e-3563">Savings Acct Number</span></span> 
- <span data-ttu-id="64f1e-3564"># compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="64f1e-3564">Savings Acct #</span></span> 
- <span data-ttu-id="64f1e-3565">N° de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="64f1e-3565">Savings Acct No.</span></span> 
- <span data-ttu-id="64f1e-3566">N° de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="64f1e-3566">Savings Account No.</span></span> 
- <span data-ttu-id="64f1e-3567">Numéro de compte de débit</span><span class="sxs-lookup"><span data-stu-id="64f1e-3567">Debit Account Number</span></span> 
- <span data-ttu-id="64f1e-3568">Compte de débit</span><span class="sxs-lookup"><span data-stu-id="64f1e-3568">Debit Account</span></span> 
- <span data-ttu-id="64f1e-3569"># Compte de débit</span><span class="sxs-lookup"><span data-stu-id="64f1e-3569">Debit Account #</span></span> 
- <span data-ttu-id="64f1e-3570">Numéro de compte de débit</span><span class="sxs-lookup"><span data-stu-id="64f1e-3570">Debit Acct Number</span></span> 
- <span data-ttu-id="64f1e-3571"># Compte de débit</span><span class="sxs-lookup"><span data-stu-id="64f1e-3571">Debit Acct #</span></span> 
- <span data-ttu-id="64f1e-3572">N° de compte de débit</span><span class="sxs-lookup"><span data-stu-id="64f1e-3572">Debit Acct No.</span></span> 
- <span data-ttu-id="64f1e-3573">N° de compte de débit</span><span class="sxs-lookup"><span data-stu-id="64f1e-3573">Debit Account No.</span></span> 
   
## <a name="us-drivers-license-number"></a><span data-ttu-id="64f1e-3574">Numéro de permis de conduire États-Unis</span><span class="sxs-lookup"><span data-stu-id="64f1e-3574">U.S. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-3575">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-3575">Format</span></span>

<span data-ttu-id="64f1e-3576">Dépend de l’État</span><span class="sxs-lookup"><span data-stu-id="64f1e-3576">Depends on the state</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-3577">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3577">Pattern</span></span>

<span data-ttu-id="64f1e-3578">Dépend de l’État, par exemple, New York :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3578">Depends on the state -- for example, New York:</span></span>
- <span data-ttu-id="64f1e-3579">Neuf chiffres au format DDD DDD DDD correspondront.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3579">Nine digits formatted like ddd ddd ddd will match.</span></span>
- <span data-ttu-id="64f1e-3580">Neuf chiffres au format ddddddddd ne correspondront pas.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3580">Nine digits like ddddddddd will not match.</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-3581">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3581">Checksum</span></span>

<span data-ttu-id="64f1e-3582">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-3582">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-3583">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-3583">Definition</span></span>

<span data-ttu-id="64f1e-3584">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3584">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-3585">La fonction Func_new_york_drivers_license_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3585">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-3586">Un mot clé figurant dans la liste Keyword_[state_name]_drivers_license_name est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3586">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="64f1e-3587">Un mot clé figurant dans la liste Keyword_us_drivers_license est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3587">A keyword from Keyword_us_drivers_license is found.</span></span>

<span data-ttu-id="64f1e-3588">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3588">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-3589">La fonction Func_new_york_drivers_license_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3589">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-3590">Un mot clé figurant dans la liste Keyword_[state_name]_drivers_license_name est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3590">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="64f1e-3591">Un mot clé figurant dans la liste Keyword_us_drivers_license_abbreviations est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3591">A keyword from Keyword_us_drivers_license_abbreviations is found.</span></span>
- <span data-ttu-id="64f1e-3592">Aucun mot clé figurant dans la liste Keyword_us_drivers_license n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3592">No keyword from Keyword_us_drivers_license is found.</span></span>

```
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_new_york_drivers_license_number" />
        <Match idRef="Keyword_new_york_drivers_license_name" />
        <Match idRef="Keyword_us_drivers_license" />
    </Pattern>
    <Pattern confidenceLevel="65">
        <IdMatch idRef="Func_new_york_drivers_license_number" />
        <Match idRef="Keyword_new_york_drivers_license_name" />
        <Match idRef="Keyword_us_drivers_license_abbreviations" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_us_drivers_license" />
        </Any>
    </Pattern>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-3593">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-3593">Keywords</span></span>

#### <a name="keywordusdriverslicenseabbreviations"></a><span data-ttu-id="64f1e-3594">Keyword_us_drivers_license_abbreviations</span><span class="sxs-lookup"><span data-stu-id="64f1e-3594">Keyword_us_drivers_license_abbreviations</span></span>

- <span data-ttu-id="64f1e-3595">LD</span><span class="sxs-lookup"><span data-stu-id="64f1e-3595">DL</span></span> 
- <span data-ttu-id="64f1e-3596">DISTRIBUTION</span><span class="sxs-lookup"><span data-stu-id="64f1e-3596">DLS</span></span> 
- <span data-ttu-id="64f1e-3597">CÈDE</span><span class="sxs-lookup"><span data-stu-id="64f1e-3597">CDL</span></span> 
- <span data-ttu-id="64f1e-3598">CDLS</span><span class="sxs-lookup"><span data-stu-id="64f1e-3598">CDLS</span></span> 
- <span data-ttu-id="64f1e-3599">ID</span><span class="sxs-lookup"><span data-stu-id="64f1e-3599">ID</span></span> 
- <span data-ttu-id="64f1e-3600">Codes</span><span class="sxs-lookup"><span data-stu-id="64f1e-3600">IDs</span></span> 
- <span data-ttu-id="64f1e-3601">LD</span><span class="sxs-lookup"><span data-stu-id="64f1e-3601">DL#</span></span> 
- <span data-ttu-id="64f1e-3602">DISTRIBUTION</span><span class="sxs-lookup"><span data-stu-id="64f1e-3602">DLS#</span></span> 
- <span data-ttu-id="64f1e-3603">CÈDE</span><span class="sxs-lookup"><span data-stu-id="64f1e-3603">CDL#</span></span> 
- <span data-ttu-id="64f1e-3604">CDLS #</span><span class="sxs-lookup"><span data-stu-id="64f1e-3604">CDLS#</span></span> 
- <span data-ttu-id="64f1e-3605">Réf</span><span class="sxs-lookup"><span data-stu-id="64f1e-3605">ID#</span></span>
- <span data-ttu-id="64f1e-3606">Codes</span><span class="sxs-lookup"><span data-stu-id="64f1e-3606">IDs#</span></span> 
- <span data-ttu-id="64f1e-3607">Numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="64f1e-3607">ID number</span></span> 
- <span data-ttu-id="64f1e-3608">Numéros d’identification</span><span class="sxs-lookup"><span data-stu-id="64f1e-3608">ID numbers</span></span> 
- <span data-ttu-id="64f1e-3609">Profil</span><span class="sxs-lookup"><span data-stu-id="64f1e-3609">LIC</span></span> 
- <span data-ttu-id="64f1e-3610">Profil</span><span class="sxs-lookup"><span data-stu-id="64f1e-3610">LIC#</span></span> 

#### <a name="keywordusdriverslicense"></a><span data-ttu-id="64f1e-3611">Keyword_us_drivers_license</span><span class="sxs-lookup"><span data-stu-id="64f1e-3611">Keyword_us_drivers_license</span></span>

- <span data-ttu-id="64f1e-3612">DriverLic</span><span class="sxs-lookup"><span data-stu-id="64f1e-3612">DriverLic</span></span> 
- <span data-ttu-id="64f1e-3613">DriverLics</span><span class="sxs-lookup"><span data-stu-id="64f1e-3613">DriverLics</span></span> 
- <span data-ttu-id="64f1e-3614">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="64f1e-3614">DriverLicense</span></span> 
- <span data-ttu-id="64f1e-3615">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="64f1e-3615">DriverLicenses</span></span> 
- <span data-ttu-id="64f1e-3616">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-3616">Driver Lic</span></span> 
- <span data-ttu-id="64f1e-3617">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-3617">Driver Lics</span></span> 
- <span data-ttu-id="64f1e-3618">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-3618">Driver License</span></span> 
- <span data-ttu-id="64f1e-3619">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-3619">Driver Licenses</span></span> 
- <span data-ttu-id="64f1e-3620">DriversLic</span><span class="sxs-lookup"><span data-stu-id="64f1e-3620">DriversLic</span></span> 
- <span data-ttu-id="64f1e-3621">DriversLics</span><span class="sxs-lookup"><span data-stu-id="64f1e-3621">DriversLics</span></span> 
- <span data-ttu-id="64f1e-3622">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="64f1e-3622">DriversLicense</span></span> 
- <span data-ttu-id="64f1e-3623">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="64f1e-3623">DriversLicenses</span></span> 
- <span data-ttu-id="64f1e-3624">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-3624">Drivers Lic</span></span> 
- <span data-ttu-id="64f1e-3625">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-3625">Drivers Lics</span></span> 
- <span data-ttu-id="64f1e-3626">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-3626">Drivers License</span></span> 
- <span data-ttu-id="64f1e-3627">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-3627">Drivers Licenses</span></span> 
- <span data-ttu-id="64f1e-3628">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="64f1e-3628">Driver'Lic</span></span> 
- <span data-ttu-id="64f1e-3629">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="64f1e-3629">Driver'Lics</span></span> 
- <span data-ttu-id="64f1e-3630">Driver'License</span><span class="sxs-lookup"><span data-stu-id="64f1e-3630">Driver'License</span></span> 
- <span data-ttu-id="64f1e-3631">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="64f1e-3631">Driver'Licenses</span></span> 
- <span data-ttu-id="64f1e-3632">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-3632">Driver' Lic</span></span> 
- <span data-ttu-id="64f1e-3633">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-3633">Driver' Lics</span></span> 
- <span data-ttu-id="64f1e-3634">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-3634">Driver' License</span></span> 
- <span data-ttu-id="64f1e-3635">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-3635">Driver' Licenses</span></span>
- <span data-ttu-id="64f1e-3636">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="64f1e-3636">Driver'sLic</span></span> 
- <span data-ttu-id="64f1e-3637">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="64f1e-3637">Driver'sLics</span></span> 
- <span data-ttu-id="64f1e-3638">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="64f1e-3638">Driver'sLicense</span></span> 
- <span data-ttu-id="64f1e-3639">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="64f1e-3639">Driver'sLicenses</span></span> 
- <span data-ttu-id="64f1e-3640">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-3640">Driver's Lic</span></span> 
- <span data-ttu-id="64f1e-3641">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-3641">Driver's Lics</span></span> 
- <span data-ttu-id="64f1e-3642">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-3642">Driver's License</span></span> 
- <span data-ttu-id="64f1e-3643">Driver’s Licenses</span><span class="sxs-lookup"><span data-stu-id="64f1e-3643">Driver's Licenses</span></span> 
- <span data-ttu-id="64f1e-3644">numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="64f1e-3644">identification number</span></span> 
- <span data-ttu-id="64f1e-3645">numéros d’identification</span><span class="sxs-lookup"><span data-stu-id="64f1e-3645">identification numbers</span></span> 
- <span data-ttu-id="64f1e-3646"># identification</span><span class="sxs-lookup"><span data-stu-id="64f1e-3646">identification #</span></span> 
- <span data-ttu-id="64f1e-3647">carte d’identité</span><span class="sxs-lookup"><span data-stu-id="64f1e-3647">id card</span></span> 
- <span data-ttu-id="64f1e-3648">cartes d’identité</span><span class="sxs-lookup"><span data-stu-id="64f1e-3648">id cards</span></span> 
- <span data-ttu-id="64f1e-3649">carte d’identification</span><span class="sxs-lookup"><span data-stu-id="64f1e-3649">identification card</span></span> 
- <span data-ttu-id="64f1e-3650">cartes d’identification</span><span class="sxs-lookup"><span data-stu-id="64f1e-3650">identification cards</span></span> 
- <span data-ttu-id="64f1e-3651">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="64f1e-3651">DriverLic#</span></span> 
- <span data-ttu-id="64f1e-3652">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="64f1e-3652">DriverLics#</span></span> 
- <span data-ttu-id="64f1e-3653">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="64f1e-3653">DriverLicense#</span></span> 
- <span data-ttu-id="64f1e-3654">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="64f1e-3654">DriverLicenses#</span></span> 
- <span data-ttu-id="64f1e-3655">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-3655">Driver Lic#</span></span> 
- <span data-ttu-id="64f1e-3656">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-3656">Driver Lics#</span></span> 
- <span data-ttu-id="64f1e-3657">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-3657">Driver License#</span></span> 
- <span data-ttu-id="64f1e-3658">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-3658">Driver Licenses#</span></span> 
- <span data-ttu-id="64f1e-3659">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="64f1e-3659">DriversLic#</span></span> 
- <span data-ttu-id="64f1e-3660">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="64f1e-3660">DriversLics#</span></span> 
- <span data-ttu-id="64f1e-3661">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="64f1e-3661">DriversLicense#</span></span> 
- <span data-ttu-id="64f1e-3662">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="64f1e-3662">DriversLicenses#</span></span> 
- <span data-ttu-id="64f1e-3663">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-3663">Drivers Lic#</span></span> 
- <span data-ttu-id="64f1e-3664">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-3664">Drivers Lics#</span></span> 
- <span data-ttu-id="64f1e-3665">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-3665">Drivers License#</span></span> 
- <span data-ttu-id="64f1e-3666">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-3666">Drivers Licenses#</span></span> 
- <span data-ttu-id="64f1e-3667">Driver'Lic #</span><span class="sxs-lookup"><span data-stu-id="64f1e-3667">Driver'Lic#</span></span> 
- <span data-ttu-id="64f1e-3668">Driver'Lics #</span><span class="sxs-lookup"><span data-stu-id="64f1e-3668">Driver'Lics#</span></span> 
- <span data-ttu-id="64f1e-3669">Driver'License #</span><span class="sxs-lookup"><span data-stu-id="64f1e-3669">Driver'License#</span></span> 
- <span data-ttu-id="64f1e-3670">Driver'Licenses #</span><span class="sxs-lookup"><span data-stu-id="64f1e-3670">Driver'Licenses#</span></span> 
- <span data-ttu-id="64f1e-3671">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-3671">Driver' Lic#</span></span> 
- <span data-ttu-id="64f1e-3672">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-3672">Driver' Lics#</span></span> 
- <span data-ttu-id="64f1e-3673">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-3673">Driver' License#</span></span> 
- <span data-ttu-id="64f1e-3674">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-3674">Driver' Licenses#</span></span> 
- <span data-ttu-id="64f1e-3675">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="64f1e-3675">Driver'sLic#</span></span> 
- <span data-ttu-id="64f1e-3676">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="64f1e-3676">Driver'sLics#</span></span> 
- <span data-ttu-id="64f1e-3677">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="64f1e-3677">Driver'sLicense#</span></span> 
- <span data-ttu-id="64f1e-3678">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="64f1e-3678">Driver'sLicenses#</span></span> 
- <span data-ttu-id="64f1e-3679">#Permisconduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-3679">Driver's Lic#</span></span> 
- <span data-ttu-id="64f1e-3680">#Permisconduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-3680">Driver's Lics#</span></span> 
- <span data-ttu-id="64f1e-3681">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-3681">Driver's License#</span></span> 
- <span data-ttu-id="64f1e-3682">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="64f1e-3682">Driver's Licenses#</span></span> 
- <span data-ttu-id="64f1e-3683"># carte d’identité</span><span class="sxs-lookup"><span data-stu-id="64f1e-3683">id card#</span></span> 
- <span data-ttu-id="64f1e-3684"># cartes d’identité</span><span class="sxs-lookup"><span data-stu-id="64f1e-3684">id cards#</span></span> 
- <span data-ttu-id="64f1e-3685">#carte d’identification</span><span class="sxs-lookup"><span data-stu-id="64f1e-3685">identification card#</span></span> 
- <span data-ttu-id="64f1e-3686">#cartes d’identification</span><span class="sxs-lookup"><span data-stu-id="64f1e-3686">identification cards#</span></span> 


#### <a name="keywordstatenamedriverslicensename"></a><span data-ttu-id="64f1e-3687">Keyword_ [state_name] _drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="64f1e-3687">Keyword_[state_name]_drivers_license_name</span></span>

- <span data-ttu-id="64f1e-3688">Abréviation de l’État (par exemple, « NY »)</span><span class="sxs-lookup"><span data-stu-id="64f1e-3688">State abbreviation (for example, "NY")</span></span> 
- <span data-ttu-id="64f1e-3689">Nom de l’État (par exemple, « New York »)</span><span class="sxs-lookup"><span data-stu-id="64f1e-3689">State name (for example, "New York")</span></span>    
   
## <a name="us-individual-taxpayer-identification-number-itin"></a><span data-ttu-id="64f1e-3690">Numéro d’identification fiscale individuel (ITIN) États-Unis</span><span class="sxs-lookup"><span data-stu-id="64f1e-3690">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-3691">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-3691">Format</span></span>

<span data-ttu-id="64f1e-3692">Neuf chiffres, le premier étant le « 9 », le quatrième le « 7 » ou le « 8 », éventuellement mis en forme avec des espaces ou des tirets</span><span class="sxs-lookup"><span data-stu-id="64f1e-3692">Nine digits that start with a "9" and contain a "7" or "8" as the fourth digit, optionally formatted with spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-3693">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3693">Pattern</span></span>

<span data-ttu-id="64f1e-3694">Avec</span><span class="sxs-lookup"><span data-stu-id="64f1e-3694">Formatted:</span></span>
- <span data-ttu-id="64f1e-3695">Le chiffre « 9 »</span><span class="sxs-lookup"><span data-stu-id="64f1e-3695">The digit "9"</span></span> 
- <span data-ttu-id="64f1e-3696">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-3696">Two digits</span></span> 
- <span data-ttu-id="64f1e-3697">Un espace ou un tiret</span><span class="sxs-lookup"><span data-stu-id="64f1e-3697">A space or dash</span></span> 
- <span data-ttu-id="64f1e-3698">Un « 7 » ou un « 8 »</span><span class="sxs-lookup"><span data-stu-id="64f1e-3698">A "7" or "8"</span></span> 
- <span data-ttu-id="64f1e-3699">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="64f1e-3699">A digit</span></span> 
- <span data-ttu-id="64f1e-3700">Un espace ou tiret</span><span class="sxs-lookup"><span data-stu-id="64f1e-3700">A space, or dash</span></span> 
- <span data-ttu-id="64f1e-3701">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-3701">Four digits</span></span>

<span data-ttu-id="64f1e-3702">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-3702">Unformatted:</span></span>
- <span data-ttu-id="64f1e-3703">Le chiffre « 9 »</span><span class="sxs-lookup"><span data-stu-id="64f1e-3703">The digit "9"</span></span> 
- <span data-ttu-id="64f1e-3704">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-3704">Two digits</span></span> 
- <span data-ttu-id="64f1e-3705">Un « 7 » ou un « 8 »</span><span class="sxs-lookup"><span data-stu-id="64f1e-3705">A "7" or "8"</span></span> 
- <span data-ttu-id="64f1e-3706">Cinq chiffres</span><span class="sxs-lookup"><span data-stu-id="64f1e-3706">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-3707">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3707">Checksum</span></span>

<span data-ttu-id="64f1e-3708">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-3708">No</span></span>

### <a name="definition"></a><span data-ttu-id="64f1e-3709">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-3709">Definition</span></span>

<span data-ttu-id="64f1e-3710">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3710">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-3711">La fonction Func_formatted_itin trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3711">The function Func_formatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-3712">Au moins une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3712">At least one of the following is true:</span></span>
    - <span data-ttu-id="64f1e-3713">Un mot clé figurant dans la liste Keyword_itin est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3713">A keyword from Keyword_itin is found.</span></span>
    - <span data-ttu-id="64f1e-3714">La fonction Func_us_address trouve une adresse au format correct.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3714">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="64f1e-3715">La fonction Func_us_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3715">The function Func_us_date finds a date in the right date format.</span></span>
    - <span data-ttu-id="64f1e-3716">Un mot clé figurant dans la liste Keyword_itin_collaborative est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3716">A keyword from Keyword_itin_collaborative is found.</span></span>

<span data-ttu-id="64f1e-3717">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3717">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-3718">La fonction Func_unformatted_itin trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3718">The function Func_unformatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-3719">Au moins une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3719">At least one of the following is true:</span></span>
    - <span data-ttu-id="64f1e-3720">Un mot clé figurant dans la liste Keyword_itin_collaborative est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3720">A keyword from Keyword_itin_collaborative is found.</span></span>
    - <span data-ttu-id="64f1e-3721">La fonction Func_us_address trouve une adresse au format correct.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3721">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="64f1e-3722">La fonction Func_us_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3722">The function Func_us_date finds a date in the right date format.</span></span>

```
<!-- U.S. Individual Taxpayer Identification Number (ITIN) -->
<Entity id="e55e2a32-f92d-4985-a35d-a0b269eb687b" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_formatted_itin" />
        <Any minMatches="1">
          <Match idRef="Keyword_itin" />
          <Match idRef="Func_us_address" />
          <Match idRef="Func_us_date" />
          <Match idRef="Keyword_itin_collaborative" />
        </Any>
    </Pattern>
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_unformatted_itin" />
        <Match idRef="Keyword_itin" />
        <Any minMatches="1">
          <Match idRef="Keyword_itin_collaborative" />
          <Match idRef="Func_us_address" />
          <Match idRef="Func_us_date" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-3723">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-3723">Keywords</span></span>

#### <a name="keyworditin"></a><span data-ttu-id="64f1e-3724">Keyword_itin</span><span class="sxs-lookup"><span data-stu-id="64f1e-3724">Keyword_itin</span></span>

- <span data-ttu-id="64f1e-3725">redevable</span><span class="sxs-lookup"><span data-stu-id="64f1e-3725">taxpayer</span></span> 
- <span data-ttu-id="64f1e-3726">id fiscal</span><span class="sxs-lookup"><span data-stu-id="64f1e-3726">tax id</span></span> 
- <span data-ttu-id="64f1e-3727">identification fiscale</span><span class="sxs-lookup"><span data-stu-id="64f1e-3727">tax identification</span></span> 
- <span data-ttu-id="64f1e-3728">ITIN</span><span class="sxs-lookup"><span data-stu-id="64f1e-3728">itin</span></span> 
- <span data-ttu-id="64f1e-3729">SSN</span><span class="sxs-lookup"><span data-stu-id="64f1e-3729">ssn</span></span> 
- <span data-ttu-id="64f1e-3730">Etain</span><span class="sxs-lookup"><span data-stu-id="64f1e-3730">tin</span></span> 
- <span data-ttu-id="64f1e-3731">sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="64f1e-3731">social security</span></span> 
- <span data-ttu-id="64f1e-3732">contribuable</span><span class="sxs-lookup"><span data-stu-id="64f1e-3732">tax payer</span></span> 
- <span data-ttu-id="64f1e-3733">itins</span><span class="sxs-lookup"><span data-stu-id="64f1e-3733">itins</span></span> 
- <span data-ttu-id="64f1e-3734">taxi</span><span class="sxs-lookup"><span data-stu-id="64f1e-3734">taxid</span></span> 
- <span data-ttu-id="64f1e-3735">contribuable individuel</span><span class="sxs-lookup"><span data-stu-id="64f1e-3735">individual taxpayer</span></span> 

#### <a name="keyworditincollaborative"></a><span data-ttu-id="64f1e-3736">Keyword_itin_collaborative</span><span class="sxs-lookup"><span data-stu-id="64f1e-3736">Keyword_itin_collaborative</span></span>

- <span data-ttu-id="64f1e-3737">License</span><span class="sxs-lookup"><span data-stu-id="64f1e-3737">License</span></span> 
- <span data-ttu-id="64f1e-3738">LD</span><span class="sxs-lookup"><span data-stu-id="64f1e-3738">DL</span></span> 
- <span data-ttu-id="64f1e-3739">DOB</span><span class="sxs-lookup"><span data-stu-id="64f1e-3739">DOB</span></span> 
- <span data-ttu-id="64f1e-3740">Birthdate</span><span class="sxs-lookup"><span data-stu-id="64f1e-3740">Birthdate</span></span> 
- <span data-ttu-id="64f1e-3741">Anniversaire</span><span class="sxs-lookup"><span data-stu-id="64f1e-3741">Birthday</span></span> 
- <span data-ttu-id="64f1e-3742">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="64f1e-3742">Date of Birth</span></span> 
   
## <a name="us-social-security-number-ssn"></a><span data-ttu-id="64f1e-3743">Numéro de sécurité sociale (SSN) États-Unis</span><span class="sxs-lookup"><span data-stu-id="64f1e-3743">U.S. Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="64f1e-3744">Format</span><span class="sxs-lookup"><span data-stu-id="64f1e-3744">Format</span></span>

<span data-ttu-id="64f1e-3745">9 chiffres, qui peuvent être mis en forme ou non mis en forme</span><span class="sxs-lookup"><span data-stu-id="64f1e-3745">9 digits, which may be in a formatted or unformatted pattern</span></span>

> [!NOTE]
> <span data-ttu-id="64f1e-3746">La mise en forme d’un numéro de sécurité sociale émis avant le milieu de l’année 2011 est fixe et certaines parties du numéro doivent se situer dans certaines plages pour qu’il soit valide (mais il n’y a pas de somme de contrôle).</span><span class="sxs-lookup"><span data-stu-id="64f1e-3746">If issued before mid-2011, an SSN has strong formatting where certain parts of the number must fall within certain ranges to be valid (but there's no checksum).</span></span>

### <a name="pattern"></a><span data-ttu-id="64f1e-3747">Modèle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3747">Pattern</span></span>

<span data-ttu-id="64f1e-3748">Quatre fonctions permettent de rechercher des numéros de sécurité sociale avec quatre différents modèles :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3748">Four functions look for SSNs in four different patterns:</span></span>
- <span data-ttu-id="64f1e-3749">Func_ssn recherche des numéros de sécurité sociale avec une mise en forme fixe d’avant l’année 2011, mis en forme avec des tirets ou des espaces (ddd-dd-dddd OU ddd dd dddd)</span><span class="sxs-lookup"><span data-stu-id="64f1e-3749">Func_ssn finds SSNs with pre-2011 strong formatting that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="64f1e-3750">Func_unformatted_ssn recherche des numéros de sécurité sociale avec une mise en forme fixe d’avant l’année 2011, avec neuf chiffres consécutifs non mis en forme (ddddddddd)</span><span class="sxs-lookup"><span data-stu-id="64f1e-3750">Func_unformatted_ssn finds SSNs with pre-2011 strong formatting that are unformatted as nine consecutive digits (ddddddddd)</span></span>
- <span data-ttu-id="64f1e-3751">Func_randomized_formatted_ssn recherche des numéros de sécurité sociale d’après l’année 2011, mis en forme avec des tirets ou des espaces  (ddd-dd-dddd OU ddd dd dddd)</span><span class="sxs-lookup"><span data-stu-id="64f1e-3751">Func_randomized_formatted_ssn finds post-2011 SSNs that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="64f1e-3752">Func_randomized_unformatted_ssn recherche des numéros de sécurité sociale d’après l’année 2011, avec neuf chiffres consécutifs non mis en forme (ddddddddd)</span><span class="sxs-lookup"><span data-stu-id="64f1e-3752">Func_randomized_unformatted_ssn finds post-2011 SSNs that are unformatted as nine consecutive digits (ddddddddd)</span></span>

### <a name="checksum"></a><span data-ttu-id="64f1e-3753">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64f1e-3753">Checksum</span></span>

<span data-ttu-id="64f1e-3754">Non</span><span class="sxs-lookup"><span data-stu-id="64f1e-3754">No</span></span>


### <a name="definition"></a><span data-ttu-id="64f1e-3755">Définition</span><span class="sxs-lookup"><span data-stu-id="64f1e-3755">Definition</span></span>

<span data-ttu-id="64f1e-3756">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3756">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-3757">La fonction Func_ssn trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3757">The function Func_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-3758">Un mot clé figurant dans la liste Keyword_ssn est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3758">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="64f1e-3759">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3759">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-3760">La fonction Func_unformatted_ssn trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3760">The function Func_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-3761">Un mot clé figurant dans la liste Keyword_ssn est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3761">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="64f1e-3762">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3762">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-3763">La fonction Func_randomized_formatted_ssn trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3763">The function Func_randomized_formatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-3764">Un mot clé figurant dans la liste Keyword_ssn est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3764">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="64f1e-3765">La fonction Func_ssn ne trouve pas de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3765">The function Func_ssn does not find content that matches the pattern.</span></span>

<span data-ttu-id="64f1e-3766">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 55 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64f1e-3766">A DLP policy is 55% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="64f1e-3767">La fonction Func_randomized_unformatted_ssn trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3767">The function Func_randomized_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="64f1e-3768">Un mot clé figurant dans la liste Keyword_ssn est trouvé.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3768">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="64f1e-3769">La fonction Func_unformatted_ssn ne trouve pas de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64f1e-3769">The function Func_unformatted_ssn does not find content that matches the pattern.</span></span>

```
<!-- U.S. Social Security Number (SSN) -->
    <Entity id="a44669fe-0d48-453d-a9b1-2cc83f2cba77" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_ssn" />
        <Match idRef="Keyword_ssn" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_unformatted_ssn" />
        <Match idRef="Keyword_ssn" />
      </Pattern>
      <Pattern confidenceLevel="65">
        <IdMatch idRef="Func_randomized_formatted_ssn" />
        <Match idRef="Keyword_ssn" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Func_ssn" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="55">
        <IdMatch idRef="Func_randomized_unformatted_ssn" />
        <Match idRef="Keyword_ssn" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Func_unformatted_ssn" />
        </Any>
      </Pattern>
    </Entity>
```

### <a name="keywords"></a><span data-ttu-id="64f1e-3770">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="64f1e-3770">Keywords</span></span>

#### <a name="keywordssn"></a><span data-ttu-id="64f1e-3771">Keyword_ssn</span><span class="sxs-lookup"><span data-stu-id="64f1e-3771">Keyword_ssn</span></span>

- <span data-ttu-id="64f1e-3772">Sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="64f1e-3772">Social Security</span></span> 
- <span data-ttu-id="64f1e-3773"># sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="64f1e-3773">Social Security#</span></span> 
- <span data-ttu-id="64f1e-3774">Sécu sociale</span><span class="sxs-lookup"><span data-stu-id="64f1e-3774">Soc Sec</span></span> 
- <span data-ttu-id="64f1e-3775">SSN</span><span class="sxs-lookup"><span data-stu-id="64f1e-3775">SSN</span></span> 
- <span data-ttu-id="64f1e-3776">NUMÉROS</span><span class="sxs-lookup"><span data-stu-id="64f1e-3776">SSNS</span></span> 
- <span data-ttu-id="64f1e-3777">SSN</span><span class="sxs-lookup"><span data-stu-id="64f1e-3777">SSN#</span></span> 
- <span data-ttu-id="64f1e-3778">SOCIALE</span><span class="sxs-lookup"><span data-stu-id="64f1e-3778">SS#</span></span> 
- <span data-ttu-id="64f1e-3779">IDENTIFIant SSID</span><span class="sxs-lookup"><span data-stu-id="64f1e-3779">SSID</span></span> 
   

