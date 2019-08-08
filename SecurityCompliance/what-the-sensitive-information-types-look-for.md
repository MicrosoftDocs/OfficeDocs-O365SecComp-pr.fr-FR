---
title: Éléments recherchés par les types d’informations sensibles
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 05/20/2019
audience: Admin
search.appverid: MET150
ms.topic: reference
f1_keywords:
- ms.o365.cc.UnifiedDLPRuleContainsSensitiveInformation
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
description: La protection contre la perte de données (DLP) dans &amp; le centre de sécurité conformité d’Office 365 inclut 80 types d’informations sensibles que vous pouvez utiliser dans vos stratégies DLP. Cette rubrique répertorie tous ces types d'informations sensibles et indique ce qu'une stratégie DLP recherche pour chaque type.
ms.openlocfilehash: 7f5c879b35f77ef142b8c45965357715f577832e
ms.sourcegitcommit: 7a0cb7e1da39fc485fc29e7325b843d16b9808af
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/07/2019
ms.locfileid: "36230378"
---
# <a name="what-the-sensitive-information-types-look-for"></a><span data-ttu-id="b9e4a-104">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="b9e4a-104">What the sensitive information types look for</span></span>

<span data-ttu-id="b9e4a-105">La protection contre la perte de données (DLP) dans &amp; le centre de sécurité conformité Office 365 inclut de nombreux types d’informations sensibles que vous pouvez utiliser dans vos stratégies DLP.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-105">Data loss prevention (DLP) in the Office 365 Security &amp; Compliance Center includes many sensitive information types that are ready for you to use in your DLP policies.</span></span> <span data-ttu-id="b9e4a-106">Cette rubrique répertorie tous ces types d'informations sensibles et indique ce qu'une stratégie DLP recherche pour chaque type.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-106">This topic lists all of these sensitive information types and shows what a DLP policy looks for when it detects each type.</span></span> <span data-ttu-id="b9e4a-107">Un type d'informations sensibles est défini par un modèle qui peut être identifié par une fonction ou une expression régulière.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-107">A sensitive information type is defined by a pattern that can be identified by a regular expression or a function.</span></span> <span data-ttu-id="b9e4a-108">En outre, des preuves corroborantes comme les mots clés et les sommes de contrôle peuvent être utilisées pour identifier un type d'informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-108">In addition, corroborative evidence such as keywords and checksums can be used to identify a sensitive information type.</span></span> <span data-ttu-id="b9e4a-109">Le niveau de confiance et la proximité sont également utilisés dans le processus d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-109">Confidence level and proximity are also used in the evaluation process.</span></span>
  
## <a name="aba-routing-number"></a><span data-ttu-id="b9e4a-110">Numéro de routage ABA</span><span class="sxs-lookup"><span data-stu-id="b9e4a-110">ABA Routing Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-111">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-111">Format</span></span>

<span data-ttu-id="b9e4a-112">9 chiffres mis en forme ou non mis en forme</span><span class="sxs-lookup"><span data-stu-id="b9e4a-112">9 digits which may be in a formatted or unformatted pattern</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-113">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-113">Pattern</span></span>

<span data-ttu-id="b9e4a-114">Avec</span><span class="sxs-lookup"><span data-stu-id="b9e4a-114">Formatted:</span></span>
- <span data-ttu-id="b9e4a-115">Quatre chiffres commençant par 0, 1, 2, 3, 6, 7 ou 8</span><span class="sxs-lookup"><span data-stu-id="b9e4a-115">Four digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span>
- <span data-ttu-id="b9e4a-116">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="b9e4a-116">A hyphen</span></span>
- <span data-ttu-id="b9e4a-117">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-117">Four digits</span></span>
- <span data-ttu-id="b9e4a-118">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="b9e4a-118">A hyphen</span></span>
- <span data-ttu-id="b9e4a-119">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="b9e4a-119">A digit</span></span>

<span data-ttu-id="b9e4a-120">Non mis en forme: 9 chiffres consécutifs commençant par 0, 1, 2, 3, 6, 7 ou 8</span><span class="sxs-lookup"><span data-stu-id="b9e4a-120">Unformatted: 9 consecutive digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span> 

### <a name="checksum"></a><span data-ttu-id="b9e4a-121">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-121">Checksum</span></span>

<span data-ttu-id="b9e4a-122">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-122">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-123">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-123">Definition</span></span>

<span data-ttu-id="b9e4a-124">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-124">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-125">La fonction Func_aba_routing trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-125">The function Func_aba_routing finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-126">Un mot clé figurant dans la liste Keyword_ABA_Routing est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-126">A keyword from Keyword_ABA_Routing is found.</span></span>

```
<!-- ABA Routing Number -->
<Entity id="cb353f78-2b72-4c3c-8827-92ebe4f69fdf" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_aba_routing" />
        <Match idRef="Keyword_ABA_Routing" />
      </Pattern>
 </Entity>
```


### <a name="keywords"></a><span data-ttu-id="b9e4a-127">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-127">Keywords</span></span>

#### <a name="keyword_aba_routing"></a><span data-ttu-id="b9e4a-128">Keyword_ABA_Routing</span><span class="sxs-lookup"><span data-stu-id="b9e4a-128">Keyword_ABA_Routing</span></span>

- <span data-ttu-id="b9e4a-129">ABA</span><span class="sxs-lookup"><span data-stu-id="b9e4a-129">aba</span></span>
- <span data-ttu-id="b9e4a-130"># aba</span><span class="sxs-lookup"><span data-stu-id="b9e4a-130">aba #</span></span>
- <span data-ttu-id="b9e4a-131"># routage aba</span><span class="sxs-lookup"><span data-stu-id="b9e4a-131">aba routing #</span></span>
- <span data-ttu-id="b9e4a-132">numéro de routage aba</span><span class="sxs-lookup"><span data-stu-id="b9e4a-132">aba routing number</span></span>
- <span data-ttu-id="b9e4a-133">ABA #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-133">aba#</span></span>
- <span data-ttu-id="b9e4a-134">abarouting #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-134">abarouting#</span></span>
- <span data-ttu-id="b9e4a-135">numéro aba</span><span class="sxs-lookup"><span data-stu-id="b9e4a-135">aba number</span></span>
- <span data-ttu-id="b9e4a-136">abaroutingnumber</span><span class="sxs-lookup"><span data-stu-id="b9e4a-136">abaroutingnumber</span></span>
- <span data-ttu-id="b9e4a-137"># routage american bank association</span><span class="sxs-lookup"><span data-stu-id="b9e4a-137">american bank association routing #</span></span>
- <span data-ttu-id="b9e4a-138">numéro de routage american bank association</span><span class="sxs-lookup"><span data-stu-id="b9e4a-138">american bank association routing number</span></span>
- <span data-ttu-id="b9e4a-139">americanbankassociationrouting #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-139">americanbankassociationrouting#</span></span>
- <span data-ttu-id="b9e4a-140">americanbankassociationroutingnumber</span><span class="sxs-lookup"><span data-stu-id="b9e4a-140">americanbankassociationroutingnumber</span></span>
- <span data-ttu-id="b9e4a-141">numéro de routage bancaire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-141">bank routing number</span></span>
- <span data-ttu-id="b9e4a-142">bankrouting #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-142">bankrouting#</span></span>
- <span data-ttu-id="b9e4a-143">bankroutingnumber</span><span class="sxs-lookup"><span data-stu-id="b9e4a-143">bankroutingnumber</span></span>
- <span data-ttu-id="b9e4a-144">numéro de routage</span><span class="sxs-lookup"><span data-stu-id="b9e4a-144">routing transit number</span></span>
- <span data-ttu-id="b9e4a-145">RTN</span><span class="sxs-lookup"><span data-stu-id="b9e4a-145">RTN</span></span> 
   
## <a name="argentina-national-identity-dni-number"></a><span data-ttu-id="b9e4a-146">Numéro d’identité nationale (DNI) pour l’Argentine</span><span class="sxs-lookup"><span data-stu-id="b9e4a-146">Argentina National Identity (DNI) Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-147">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-147">Format</span></span>

<span data-ttu-id="b9e4a-148">Huit chiffres séparés par des points</span><span class="sxs-lookup"><span data-stu-id="b9e4a-148">Eight digits separated by periods</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-149">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-149">Pattern</span></span>

<span data-ttu-id="b9e4a-150">Huit chiffres :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-150">Eight digits:</span></span>
- <span data-ttu-id="b9e4a-151">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-151">Two digits</span></span>
- <span data-ttu-id="b9e4a-152">Un point </span><span class="sxs-lookup"><span data-stu-id="b9e4a-152">A period</span></span>
- <span data-ttu-id="b9e4a-153">Trois chiffres </span><span class="sxs-lookup"><span data-stu-id="b9e4a-153">Three digits</span></span>
- <span data-ttu-id="b9e4a-154">Un point </span><span class="sxs-lookup"><span data-stu-id="b9e4a-154">A period</span></span>
- <span data-ttu-id="b9e4a-155">Trois chiffres </span><span class="sxs-lookup"><span data-stu-id="b9e4a-155">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-156">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-156">Checksum</span></span>

<span data-ttu-id="b9e4a-157">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-157">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-158">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-158">Definition</span></span>

<span data-ttu-id="b9e4a-159">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-159">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-160">L’expression régulière Regex_argentina_national_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-160">The regular expression Regex_argentina_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-161">Un mot clé figurant dans la liste Keyword_argentina_national_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-161">A keyword from Keyword_argentina_national_id is found.</span></span>

```
<!-- Argentina National Identity (DNI) Number -->
<Entity id="eefbb00e-8282-433c-8620-8f1da3bffdb2" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_argentina_national_id"/>
      <Match idRef="Keyword_argentina_national_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b9e4a-162">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-162">Keywords</span></span>

#### <a name="keyword_argentina_national_id"></a><span data-ttu-id="b9e4a-163">Keyword_argentina_national_id</span><span class="sxs-lookup"><span data-stu-id="b9e4a-163">Keyword_argentina_national_id</span></span>

- <span data-ttu-id="b9e4a-164">Argentina National Identity number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-164">Argentina National Identity number</span></span> 
- <span data-ttu-id="b9e4a-165">Identité</span><span class="sxs-lookup"><span data-stu-id="b9e4a-165">Identity</span></span> 
- <span data-ttu-id="b9e4a-166">Identification de la carte d’identité nationale</span><span class="sxs-lookup"><span data-stu-id="b9e4a-166">Identification National Identity Card</span></span> 
- <span data-ttu-id="b9e4a-167">DNI</span><span class="sxs-lookup"><span data-stu-id="b9e4a-167">DNI</span></span> 
- <span data-ttu-id="b9e4a-168">Carte d’interface réseau nationale du registre des personnes</span><span class="sxs-lookup"><span data-stu-id="b9e4a-168">NIC National Registry of Persons</span></span> 
- <span data-ttu-id="b9e4a-169">Documento Nacional de Identidad</span><span class="sxs-lookup"><span data-stu-id="b9e4a-169">Documento Nacional de Identidad</span></span> 
- <span data-ttu-id="b9e4a-170">Registro Nacional de las Personas</span><span class="sxs-lookup"><span data-stu-id="b9e4a-170">Registro Nacional de las Personas</span></span> 
- <span data-ttu-id="b9e4a-171">Identidad</span><span class="sxs-lookup"><span data-stu-id="b9e4a-171">Identidad</span></span> 
- <span data-ttu-id="b9e4a-172">Identificación</span><span class="sxs-lookup"><span data-stu-id="b9e4a-172">Identificación</span></span> 
   
## <a name="australia-bank-account-number"></a><span data-ttu-id="b9e4a-173">Numéro de compte bancaire Australie</span><span class="sxs-lookup"><span data-stu-id="b9e4a-173">Australia Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-174">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-174">Format</span></span>

<span data-ttu-id="b9e4a-175">6 à 10 chiffres avec ou sans le numéro d’agence bancaire de l’État</span><span class="sxs-lookup"><span data-stu-id="b9e4a-175">6-10 digits with or without a bank state branch number</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-176">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-176">Pattern</span></span>

<span data-ttu-id="b9e4a-177">Le numéro de compte est composé de 6 à 10 chiffres.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-177">Account number is 6-10 digits.</span></span>
<span data-ttu-id="b9e4a-178">Numéro de succursale bancaire en Australie :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-178">Australia bank state branch number:</span></span>
- <span data-ttu-id="b9e4a-179">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-179">Three digits</span></span> 
- <span data-ttu-id="b9e4a-180">Un trait d’union</span><span class="sxs-lookup"><span data-stu-id="b9e4a-180">A hyphen</span></span> 
- <span data-ttu-id="b9e4a-181">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-181">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-182">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-182">Checksum</span></span>

<span data-ttu-id="b9e4a-183">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-183">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-184">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-184">Definition</span></span>

<span data-ttu-id="b9e4a-185">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-185">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-186">L’expression régulière Regex_australia_bank_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-186">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="b9e4a-187">Un mot clé figurant dans la liste Keyword_australia_bank_account_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-187">A keyword from Keyword_australia_bank_account_number is found.</span></span>
- <span data-ttu-id="b9e4a-188">L’expression régulière Regex_australia_bank_account_number_bsb trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-188">The regular expression Regex_australia_bank_account_number_bsb finds content that matches the pattern.</span></span>

<span data-ttu-id="b9e4a-189">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-189">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-190">L’expression régulière Regex_australia_bank_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-190">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="b9e4a-191">Un mot clé figurant dans la liste Keyword_australia_bank_account_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-191">A keyword from Keyword_australia_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-192">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-192">Keywords</span></span>

#### <a name="keyword_australia_bank_account_number"></a><span data-ttu-id="b9e4a-193">Keyword_australia_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-193">Keyword_australia_bank_account_number</span></span>

- <span data-ttu-id="b9e4a-194">code swift banque</span><span class="sxs-lookup"><span data-stu-id="b9e4a-194">swift bank code</span></span>
- <span data-ttu-id="b9e4a-195">banque correspondante</span><span class="sxs-lookup"><span data-stu-id="b9e4a-195">correspondent bank</span></span>
- <span data-ttu-id="b9e4a-196">devise de base</span><span class="sxs-lookup"><span data-stu-id="b9e4a-196">base currency</span></span>
- <span data-ttu-id="b9e4a-197">compte aux États-Unis</span><span class="sxs-lookup"><span data-stu-id="b9e4a-197">usa account</span></span>
- <span data-ttu-id="b9e4a-198">adresse du titulaire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-198">holder address</span></span>
- <span data-ttu-id="b9e4a-199">adresse de la banque</span><span class="sxs-lookup"><span data-stu-id="b9e4a-199">bank address</span></span>
- <span data-ttu-id="b9e4a-200">informations du compte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-200">information account</span></span>
- <span data-ttu-id="b9e4a-201">transferts de fonds</span><span class="sxs-lookup"><span data-stu-id="b9e4a-201">fund transfers</span></span>
- <span data-ttu-id="b9e4a-202">frais bancaires</span><span class="sxs-lookup"><span data-stu-id="b9e4a-202">bank charges</span></span>
- <span data-ttu-id="b9e4a-203">informations sur la banque</span><span class="sxs-lookup"><span data-stu-id="b9e4a-203">bank details</span></span>
- <span data-ttu-id="b9e4a-204">informations bancaires</span><span class="sxs-lookup"><span data-stu-id="b9e4a-204">banking information</span></span>
- <span data-ttu-id="b9e4a-205">noms complets</span><span class="sxs-lookup"><span data-stu-id="b9e4a-205">full names</span></span>
- <span data-ttu-id="b9e4a-206">auront</span><span class="sxs-lookup"><span data-stu-id="b9e4a-206">iaea</span></span>

   
## <a name="australia-drivers-license-number"></a><span data-ttu-id="b9e4a-207">Numéro de permis de conduire Australie</span><span class="sxs-lookup"><span data-stu-id="b9e4a-207">Australia Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-208">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-208">Format</span></span>

<span data-ttu-id="b9e4a-209">Neuf lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-209">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-210">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-210">Pattern</span></span>

<span data-ttu-id="b9e4a-211">Neuf lettres et chiffres :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-211">Nine letters and digits:</span></span> 

- <span data-ttu-id="b9e4a-212">Deux chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-212">Two digits or letters (not case sensitive)</span></span> 
- <span data-ttu-id="b9e4a-213">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-213">Two digits</span></span> 
- <span data-ttu-id="b9e4a-214">Cinq chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-214">Five digits or letters (not case sensitive)</span></span>

<span data-ttu-id="b9e4a-215">OR</span><span class="sxs-lookup"><span data-stu-id="b9e4a-215">OR</span></span>

- <span data-ttu-id="b9e4a-216">1 ou 2 lettres facultatives (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="b9e4a-216">1-2 optional letters (not case sensitive)</span></span> 
- <span data-ttu-id="b9e4a-217">4 à 9 chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-217">4-9 digits</span></span>

<span data-ttu-id="b9e4a-218">OR</span><span class="sxs-lookup"><span data-stu-id="b9e4a-218">OR</span></span>

- <span data-ttu-id="b9e4a-219">Neuf chiffres ou lettres (ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-219">Nine digits or letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-220">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-220">Checksum</span></span>

<span data-ttu-id="b9e4a-221">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-221">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-222">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-222">Definition</span></span>

<span data-ttu-id="b9e4a-223">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-223">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-224">L’expression régulière Regex_australia_drivers_license_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-224">The regular expression Regex_australia_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-225">Un mot clé figurant dans la liste Keyword_australia_drivers_license_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-225">A keyword from Keyword_australia_drivers_license_number is found.</span></span>
- <span data-ttu-id="b9e4a-226">Aucun mot clé figurant dans la liste Keyword_australia_drivers_license_number_exclusions n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-226">No keyword from Keyword_australia_drivers_license_number_exclusions is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-227">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-227">Keywords</span></span>

#### <a name="keyword_australia_drivers_license_number"></a><span data-ttu-id="b9e4a-228">Keyword_australia_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-228">Keyword_australia_drivers_license_number</span></span>

- <span data-ttu-id="b9e4a-229">permis de conduite internationaux</span><span class="sxs-lookup"><span data-stu-id="b9e4a-229">international driving permits</span></span>
- <span data-ttu-id="b9e4a-230">australian automobile association</span><span class="sxs-lookup"><span data-stu-id="b9e4a-230">australian automobile association</span></span>
- <span data-ttu-id="b9e4a-231">permis de conduite international</span><span class="sxs-lookup"><span data-stu-id="b9e4a-231">international driving permit</span></span>
- <span data-ttu-id="b9e4a-232">DriverLicence</span><span class="sxs-lookup"><span data-stu-id="b9e4a-232">DriverLicence</span></span>
- <span data-ttu-id="b9e4a-233">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="b9e4a-233">DriverLicences</span></span>
- <span data-ttu-id="b9e4a-234">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-234">Driver Lic</span></span>
- <span data-ttu-id="b9e4a-235">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-235">Driver Licence</span></span>
- <span data-ttu-id="b9e4a-236">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-236">Driver Licences</span></span>
- <span data-ttu-id="b9e4a-237">DriversLic</span><span class="sxs-lookup"><span data-stu-id="b9e4a-237">DriversLic</span></span>
- <span data-ttu-id="b9e4a-238">DriversLicence</span><span class="sxs-lookup"><span data-stu-id="b9e4a-238">DriversLicence</span></span>
- <span data-ttu-id="b9e4a-239">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="b9e4a-239">DriversLicences</span></span>
- <span data-ttu-id="b9e4a-240">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-240">Drivers Lic</span></span>
- <span data-ttu-id="b9e4a-241">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-241">Drivers Lics</span></span>
- <span data-ttu-id="b9e4a-242">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-242">Drivers Licence</span></span>
- <span data-ttu-id="b9e4a-243">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-243">Drivers Licences</span></span>
- <span data-ttu-id="b9e4a-244">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="b9e4a-244">Driver'Lic</span></span>
- <span data-ttu-id="b9e4a-245">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="b9e4a-245">Driver'Lics</span></span>
- <span data-ttu-id="b9e4a-246">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="b9e4a-246">Driver'Licence</span></span>
- <span data-ttu-id="b9e4a-247">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="b9e4a-247">Driver'Licences</span></span>
- <span data-ttu-id="b9e4a-248">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-248">Driver' Lic</span></span>
- <span data-ttu-id="b9e4a-249">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-249">Driver' Lics</span></span>
- <span data-ttu-id="b9e4a-250">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-250">Driver' Licence</span></span>
- <span data-ttu-id="b9e4a-251">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-251">Driver' Licences</span></span>
- <span data-ttu-id="b9e4a-252">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="b9e4a-252">Driver'sLic</span></span>
- <span data-ttu-id="b9e4a-253">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="b9e4a-253">Driver'sLics</span></span>
- <span data-ttu-id="b9e4a-254">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="b9e4a-254">Driver'sLicence</span></span>
- <span data-ttu-id="b9e4a-255">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="b9e4a-255">Driver'sLicences</span></span>
- <span data-ttu-id="b9e4a-256">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-256">Driver's Lic</span></span>
- <span data-ttu-id="b9e4a-257">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-257">Driver's Lics</span></span>
- <span data-ttu-id="b9e4a-258">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-258">Driver's Licence</span></span>
- <span data-ttu-id="b9e4a-259">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-259">Driver's Licences</span></span>
- <span data-ttu-id="b9e4a-260">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-260">DriverLic#</span></span>
- <span data-ttu-id="b9e4a-261">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-261">DriverLics#</span></span>
- <span data-ttu-id="b9e4a-262">DriverLicence #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-262">DriverLicence#</span></span>
- <span data-ttu-id="b9e4a-263">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-263">DriverLicences#</span></span>
- <span data-ttu-id="b9e4a-264">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-264">Driver Lic#</span></span>
- <span data-ttu-id="b9e4a-265">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-265">Driver Lics#</span></span>
- <span data-ttu-id="b9e4a-266">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-266">Driver Licence#</span></span>
- <span data-ttu-id="b9e4a-267">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-267">Driver Licences#</span></span>
- <span data-ttu-id="b9e4a-268">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-268">DriversLic#</span></span>
- <span data-ttu-id="b9e4a-269">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-269">DriversLics#</span></span>
- <span data-ttu-id="b9e4a-270">DriversLicence #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-270">DriversLicence#</span></span>
- <span data-ttu-id="b9e4a-271">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-271">DriversLicences#</span></span>
- <span data-ttu-id="b9e4a-272">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-272">Drivers Lic#</span></span>
- <span data-ttu-id="b9e4a-273">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-273">Drivers Lics#</span></span>
- <span data-ttu-id="b9e4a-274">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-274">Drivers Licence#</span></span>
- <span data-ttu-id="b9e4a-275">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-275">Drivers Licences#</span></span>
- <span data-ttu-id="b9e4a-276">Driver'Lic #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-276">Driver'Lic#</span></span>
- <span data-ttu-id="b9e4a-277">Driver'Lics #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-277">Driver'Lics#</span></span>
- <span data-ttu-id="b9e4a-278">Driver'Licence #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-278">Driver'Licence#</span></span>
- <span data-ttu-id="b9e4a-279">Driver'Licences #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-279">Driver'Licences#</span></span>
- <span data-ttu-id="b9e4a-280">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-280">Driver' Lic#</span></span>
- <span data-ttu-id="b9e4a-281">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-281">Driver' Lics#</span></span>
- <span data-ttu-id="b9e4a-282">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-282">Driver' Licence#</span></span>
- <span data-ttu-id="b9e4a-283">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-283">Driver' Licences#</span></span>
- <span data-ttu-id="b9e4a-284">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-284">Driver'sLic#</span></span>
- <span data-ttu-id="b9e4a-285">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-285">Driver'sLics#</span></span>
- <span data-ttu-id="b9e4a-286">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-286">Driver'sLicence#</span></span>
- <span data-ttu-id="b9e4a-287">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-287">Driver'sLicences#</span></span>
- <span data-ttu-id="b9e4a-288">#Permisconduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-288">Driver's Lic#</span></span>
- <span data-ttu-id="b9e4a-289">#Permisconduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-289">Driver's Lics#</span></span>
- <span data-ttu-id="b9e4a-290">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-290">Driver's Licence#</span></span>
- <span data-ttu-id="b9e4a-291">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-291">Driver's Licences#</span></span> 

#### <a name="keyword_australia_drivers_license_number_exclusions"></a><span data-ttu-id="b9e4a-292">Keyword_australia_drivers_license_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="b9e4a-292">Keyword_australia_drivers_license_number_exclusions</span></span>

- <span data-ttu-id="b9e4a-293">AAA</span><span class="sxs-lookup"><span data-stu-id="b9e4a-293">aaa</span></span>
- <span data-ttu-id="b9e4a-294">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="b9e4a-294">DriverLicense</span></span>
- <span data-ttu-id="b9e4a-295">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="b9e4a-295">DriverLicenses</span></span>
- <span data-ttu-id="b9e4a-296">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-296">Driver License</span></span>
- <span data-ttu-id="b9e4a-297">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-297">Driver Licenses</span></span>
- <span data-ttu-id="b9e4a-298">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="b9e4a-298">DriversLicense</span></span>
- <span data-ttu-id="b9e4a-299">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="b9e4a-299">DriversLicenses</span></span>
- <span data-ttu-id="b9e4a-300">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-300">Drivers License</span></span>
- <span data-ttu-id="b9e4a-301">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-301">Drivers Licenses</span></span>
- <span data-ttu-id="b9e4a-302">Driver'License</span><span class="sxs-lookup"><span data-stu-id="b9e4a-302">Driver'License</span></span>
- <span data-ttu-id="b9e4a-303">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="b9e4a-303">Driver'Licenses</span></span>
- <span data-ttu-id="b9e4a-304">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-304">Driver' License</span></span>
- <span data-ttu-id="b9e4a-305">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-305">Driver' Licenses</span></span>
- <span data-ttu-id="b9e4a-306">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="b9e4a-306">Driver'sLicense</span></span>
- <span data-ttu-id="b9e4a-307">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="b9e4a-307">Driver'sLicenses</span></span>
- <span data-ttu-id="b9e4a-308">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-308">Driver's License</span></span>
- <span data-ttu-id="b9e4a-309">Driver’s Licenses</span><span class="sxs-lookup"><span data-stu-id="b9e4a-309">Driver's Licenses</span></span>
- <span data-ttu-id="b9e4a-310">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-310">DriverLicense#</span></span>
- <span data-ttu-id="b9e4a-311">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-311">DriverLicenses#</span></span>
- <span data-ttu-id="b9e4a-312">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-312">Driver License#</span></span>
- <span data-ttu-id="b9e4a-313">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-313">Driver Licenses#</span></span>
- <span data-ttu-id="b9e4a-314">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-314">DriversLicense#</span></span>
- <span data-ttu-id="b9e4a-315">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-315">DriversLicenses#</span></span>
- <span data-ttu-id="b9e4a-316">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-316">Drivers License#</span></span>
- <span data-ttu-id="b9e4a-317">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-317">Drivers Licenses#</span></span>
- <span data-ttu-id="b9e4a-318">Driver'License #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-318">Driver'License#</span></span>
- <span data-ttu-id="b9e4a-319">Driver'Licenses #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-319">Driver'Licenses#</span></span>
- <span data-ttu-id="b9e4a-320">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-320">Driver' License#</span></span>
- <span data-ttu-id="b9e4a-321">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-321">Driver' Licenses#</span></span>
- <span data-ttu-id="b9e4a-322">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-322">Driver'sLicense#</span></span>
- <span data-ttu-id="b9e4a-323">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-323">Driver'sLicenses#</span></span>
- <span data-ttu-id="b9e4a-324">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-324">Driver's License#</span></span>
- <span data-ttu-id="b9e4a-325">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-325">Driver's Licenses#</span></span>
   
## <a name="australia-medical-account-number"></a><span data-ttu-id="b9e4a-326">Numéro de dossier médical Australie</span><span class="sxs-lookup"><span data-stu-id="b9e4a-326">Australia Medical Account Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-327">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-327">Format</span></span>

<span data-ttu-id="b9e4a-328">10 à 11 chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-328">10-11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-329">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-329">Pattern</span></span>

<span data-ttu-id="b9e4a-330">10 à 11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-330">10-11 digits:</span></span>
- <span data-ttu-id="b9e4a-331">Le premier chiffre est compris entre 2 et 6</span><span class="sxs-lookup"><span data-stu-id="b9e4a-331">First digit is in the range 2-6</span></span>
- <span data-ttu-id="b9e4a-332">Le neuvième chiffre est un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-332">Ninth digit is a check digit</span></span>
- <span data-ttu-id="b9e4a-333">Le dixième chiffre est le chiffre d’émission</span><span class="sxs-lookup"><span data-stu-id="b9e4a-333">Tenth digit is the issue digit</span></span>
- <span data-ttu-id="b9e4a-334">Le onzième chiffre (facultatif) est le numéro individuel</span><span class="sxs-lookup"><span data-stu-id="b9e4a-334">Eleventh digit (optional) is the individual number</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-335">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-335">Checksum</span></span>

<span data-ttu-id="b9e4a-336">Oui</span><span class="sxs-lookup"><span data-stu-id="b9e4a-336">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-337">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-337">Definition</span></span>

<span data-ttu-id="b9e4a-338">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 95 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-338">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-339">La fonction Func_australian_medical_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-339">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-340">Un mot clé figurant dans la liste Keyword_Australia_Medical_Account_Number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-340">A keyword from Keyword_Australia_Medical_Account_Number is found.</span></span>
- <span data-ttu-id="b9e4a-341">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-341">The checksum passes.</span></span>

<span data-ttu-id="b9e4a-342">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-342">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-343">La fonction Func_australian_medical_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-343">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-344">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-344">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-345">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-345">Keywords</span></span>

#### <a name="keyword_australia_medical_account_number"></a><span data-ttu-id="b9e4a-346">Keyword_Australia_Medical_Account_Number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-346">Keyword_Australia_Medical_Account_Number</span></span>

- <span data-ttu-id="b9e4a-347">informations sur le compte bancaire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-347">bank account details</span></span>
- <span data-ttu-id="b9e4a-348">remboursements d’assurance maladie</span><span class="sxs-lookup"><span data-stu-id="b9e4a-348">medicare payments</span></span>
- <span data-ttu-id="b9e4a-349">compte de prêts immobiliers</span><span class="sxs-lookup"><span data-stu-id="b9e4a-349">mortgage account</span></span>
- <span data-ttu-id="b9e4a-350">paiements bancaires</span><span class="sxs-lookup"><span data-stu-id="b9e4a-350">bank payments</span></span>
- <span data-ttu-id="b9e4a-351">direction de l’information</span><span class="sxs-lookup"><span data-stu-id="b9e4a-351">information branch</span></span>
- <span data-ttu-id="b9e4a-352">prêt sur carte de crédit</span><span class="sxs-lookup"><span data-stu-id="b9e4a-352">credit card loan</span></span>
- <span data-ttu-id="b9e4a-353">département des services sociaux</span><span class="sxs-lookup"><span data-stu-id="b9e4a-353">department of human services</span></span>
- <span data-ttu-id="b9e4a-354">service local</span><span class="sxs-lookup"><span data-stu-id="b9e4a-354">local service</span></span>
- <span data-ttu-id="b9e4a-355">médicaux</span><span class="sxs-lookup"><span data-stu-id="b9e4a-355">medicare</span></span>

   
## <a name="australia-passport-number"></a><span data-ttu-id="b9e4a-356">Numéro de passeport Australie</span><span class="sxs-lookup"><span data-stu-id="b9e4a-356">Australia Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-357">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-357">Format</span></span>

<span data-ttu-id="b9e4a-358">Une lettre suivie de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-358">A letter followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-359">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-359">Pattern</span></span>

<span data-ttu-id="b9e4a-360">Une lettre (ne respectant pas la casse) suivie de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-360">A letter (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-361">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-361">Checksum</span></span>

<span data-ttu-id="b9e4a-362">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-362">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-363">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-363">Definition</span></span>

<span data-ttu-id="b9e4a-364">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-365">L’expression régulière Regex_australia_passport_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-365">The regular expression Regex_australia_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-366">Un mot clé depuis Keyword_passport ou Keyword_australia_passport_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-366">A keyword from Keyword_passport or Keyword_australia_passport_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-367">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-367">Keywords</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="b9e4a-368">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-368">Keyword_passport</span></span>

- <span data-ttu-id="b9e4a-369">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-369">Passport Number</span></span>
- <span data-ttu-id="b9e4a-370">N° de passeport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-370">Passport No</span></span>
- <span data-ttu-id="b9e4a-371"># Passeport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-371">Passport #</span></span>
- <span data-ttu-id="b9e4a-372">Tel #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-372">Passport#</span></span>
- <span data-ttu-id="b9e4a-373">PassportID</span><span class="sxs-lookup"><span data-stu-id="b9e4a-373">PassportID</span></span>
- <span data-ttu-id="b9e4a-374">N ° passeport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-374">Passportno</span></span>
- <span data-ttu-id="b9e4a-375">passportnumber</span><span class="sxs-lookup"><span data-stu-id="b9e4a-375">passportnumber</span></span>
- <span data-ttu-id="b9e4a-376">パスポート</span><span class="sxs-lookup"><span data-stu-id="b9e4a-376">パスポート</span></span>
- <span data-ttu-id="b9e4a-377">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="b9e4a-377">パスポート番号</span></span>
- <span data-ttu-id="b9e4a-378">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="b9e4a-378">パスポートのNum</span></span>
- <span data-ttu-id="b9e4a-379">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="b9e4a-379">パスポート ＃</span></span> 
- <span data-ttu-id="b9e4a-380">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-380">Numéro de passeport</span></span>
- <span data-ttu-id="b9e4a-381">Passeport n°</span><span class="sxs-lookup"><span data-stu-id="b9e4a-381">Passeport n °</span></span>
- <span data-ttu-id="b9e4a-382">Passeport numéro</span><span class="sxs-lookup"><span data-stu-id="b9e4a-382">Passeport Non</span></span>
- <span data-ttu-id="b9e4a-383"># Passeport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-383">Passeport #</span></span>
- <span data-ttu-id="b9e4a-384">Passeport #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-384">Passeport#</span></span>
- <span data-ttu-id="b9e4a-385">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="b9e4a-385">PasseportNon</span></span>
- <span data-ttu-id="b9e4a-386">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="b9e4a-386">Passeportn °</span></span>

#### <a name="keyword_australia_passport_number"></a><span data-ttu-id="b9e4a-387">Keyword_australia_passport_number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-387">Keyword_australia_passport_number</span></span>

- <span data-ttu-id="b9e4a-388">tel</span><span class="sxs-lookup"><span data-stu-id="b9e4a-388">passport</span></span>
- <span data-ttu-id="b9e4a-389">informations sur le passeport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-389">passport details</span></span>
- <span data-ttu-id="b9e4a-390">immigration et citoyenneté</span><span class="sxs-lookup"><span data-stu-id="b9e4a-390">immigration and citizenship</span></span>
- <span data-ttu-id="b9e4a-391">Australie</span><span class="sxs-lookup"><span data-stu-id="b9e4a-391">commonwealth of australia</span></span>
- <span data-ttu-id="b9e4a-392">service de l’immigration</span><span class="sxs-lookup"><span data-stu-id="b9e4a-392">department of immigration</span></span>
- <span data-ttu-id="b9e4a-393">adresse de résidence</span><span class="sxs-lookup"><span data-stu-id="b9e4a-393">residential address</span></span>
- <span data-ttu-id="b9e4a-394">service de l’immigration et de la citoyenneté</span><span class="sxs-lookup"><span data-stu-id="b9e4a-394">department of immigration and citizenship</span></span>
- <span data-ttu-id="b9e4a-395">délivrance</span><span class="sxs-lookup"><span data-stu-id="b9e4a-395">visa</span></span>
- <span data-ttu-id="b9e4a-396">Carte nationale d’identité</span><span class="sxs-lookup"><span data-stu-id="b9e4a-396">national identity card</span></span>
- <span data-ttu-id="b9e4a-397">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-397">passport number</span></span>
- <span data-ttu-id="b9e4a-398">document de voyage</span><span class="sxs-lookup"><span data-stu-id="b9e4a-398">travel document</span></span>
- <span data-ttu-id="b9e4a-399">autorité émettrice</span><span class="sxs-lookup"><span data-stu-id="b9e4a-399">issuing authority</span></span>
   
## <a name="australia-tax-file-number"></a><span data-ttu-id="b9e4a-400">Numéro de dossier fiscal Australie</span><span class="sxs-lookup"><span data-stu-id="b9e4a-400">Australia Tax File Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-401">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-401">Format</span></span>

<span data-ttu-id="b9e4a-402">8 ou 9 chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-402">8-9 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-403">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-403">Pattern</span></span>

<span data-ttu-id="b9e4a-404">8 à 9 chiffres généralement entrecoupés d’espaces comme suit :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-404">8-9 digits typically presented with spaces as follows:</span></span>
- <span data-ttu-id="b9e4a-405">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-405">Three digits</span></span> 
- <span data-ttu-id="b9e4a-406">Un espace facultatif</span><span class="sxs-lookup"><span data-stu-id="b9e4a-406">An optional space</span></span> 
- <span data-ttu-id="b9e4a-407">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-407">Three digits</span></span> 
- <span data-ttu-id="b9e4a-408">Un espace facultatif</span><span class="sxs-lookup"><span data-stu-id="b9e4a-408">An optional space</span></span> 
- <span data-ttu-id="b9e4a-409">2 à 3 chiffres où le dernier chiffre est un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-409">2-3 digits where the last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-410">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-410">Checksum</span></span>

<span data-ttu-id="b9e4a-411">Oui</span><span class="sxs-lookup"><span data-stu-id="b9e4a-411">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-412">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-412">Definition</span></span>

<span data-ttu-id="b9e4a-413">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-413">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-414">La fonction Func_australian_tax_file_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-414">The function Func_australian_tax_file_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-415">Aucun mot clé figurant dans la liste Keyword_Australia_Tax_File_Number ou Keyword_number_exclusions n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-415">No keyword from Keyword_Australia_Tax_File_Number or Keyword_number_exclusions is found.</span></span>
- <span data-ttu-id="b9e4a-416">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-416">The checksum passes.</span></span>

```
   <!-- Australia Tax File Number -->
    <Entity id="e29bc95f-ff70-4a37-aa01-04d17360a4c5" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_australian_tax_file_number" />
        <Match idRef="Keyword_Australia_Tax_File_Number" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_number_exclusions" />
        </Any>
      </Pattern>
    </Entity>
```

### <a name="keywords"></a><span data-ttu-id="b9e4a-417">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-417">Keywords</span></span>

#### <a name="keyword_australia_tax_file_number"></a><span data-ttu-id="b9e4a-418">Keyword_Australia_Tax_File_Number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-418">Keyword_Australia_Tax_File_Number</span></span>

- <span data-ttu-id="b9e4a-419">numéro d’entreprise australien</span><span class="sxs-lookup"><span data-stu-id="b9e4a-419">australian business number</span></span>
- <span data-ttu-id="b9e4a-420">taux d’imposition marginale</span><span class="sxs-lookup"><span data-stu-id="b9e4a-420">marginal tax rate</span></span>
- <span data-ttu-id="b9e4a-421">prélèvement d’assurance maladie</span><span class="sxs-lookup"><span data-stu-id="b9e4a-421">medicare levy</span></span>
- <span data-ttu-id="b9e4a-422">numéro de portefeuille</span><span class="sxs-lookup"><span data-stu-id="b9e4a-422">portfolio number</span></span>
- <span data-ttu-id="b9e4a-423">service des vétérans</span><span class="sxs-lookup"><span data-stu-id="b9e4a-423">service veterans</span></span>
- <span data-ttu-id="b9e4a-424">retenue à la source</span><span class="sxs-lookup"><span data-stu-id="b9e4a-424">withholding tax</span></span>
- <span data-ttu-id="b9e4a-425">déclaration d’impôts individuels</span><span class="sxs-lookup"><span data-stu-id="b9e4a-425">individual tax return</span></span>
- <span data-ttu-id="b9e4a-426">numéro de dossier fiscal</span><span class="sxs-lookup"><span data-stu-id="b9e4a-426">tax file number</span></span>

#### <a name="keyword_number_exclusions"></a><span data-ttu-id="b9e4a-427">Keyword_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="b9e4a-427">Keyword_number_exclusions</span></span>

- <span data-ttu-id="b9e4a-428">00000000</span><span class="sxs-lookup"><span data-stu-id="b9e4a-428">00000000</span></span>
- <span data-ttu-id="b9e4a-429">11111111</span><span class="sxs-lookup"><span data-stu-id="b9e4a-429">11111111</span></span>
- <span data-ttu-id="b9e4a-430">22222222</span><span class="sxs-lookup"><span data-stu-id="b9e4a-430">22222222</span></span>
- <span data-ttu-id="b9e4a-431">33333333</span><span class="sxs-lookup"><span data-stu-id="b9e4a-431">33333333</span></span>
- <span data-ttu-id="b9e4a-432">44444444</span><span class="sxs-lookup"><span data-stu-id="b9e4a-432">44444444</span></span>
- <span data-ttu-id="b9e4a-433">55555555</span><span class="sxs-lookup"><span data-stu-id="b9e4a-433">55555555</span></span>
- <span data-ttu-id="b9e4a-434">66666666</span><span class="sxs-lookup"><span data-stu-id="b9e4a-434">66666666</span></span>
- <span data-ttu-id="b9e4a-435">77777777</span><span class="sxs-lookup"><span data-stu-id="b9e4a-435">77777777</span></span>
- <span data-ttu-id="b9e4a-436">88888888</span><span class="sxs-lookup"><span data-stu-id="b9e4a-436">88888888</span></span>
- <span data-ttu-id="b9e4a-437">99999999</span><span class="sxs-lookup"><span data-stu-id="b9e4a-437">99999999</span></span>
- <span data-ttu-id="b9e4a-438">000000000</span><span class="sxs-lookup"><span data-stu-id="b9e4a-438">000000000</span></span>
- <span data-ttu-id="b9e4a-439">111111111</span><span class="sxs-lookup"><span data-stu-id="b9e4a-439">111111111</span></span>
- <span data-ttu-id="b9e4a-440">222222222</span><span class="sxs-lookup"><span data-stu-id="b9e4a-440">222222222</span></span>
- <span data-ttu-id="b9e4a-441">333333333</span><span class="sxs-lookup"><span data-stu-id="b9e4a-441">333333333</span></span>
- <span data-ttu-id="b9e4a-442">444444444</span><span class="sxs-lookup"><span data-stu-id="b9e4a-442">444444444</span></span>
- <span data-ttu-id="b9e4a-443">555555555</span><span class="sxs-lookup"><span data-stu-id="b9e4a-443">555555555</span></span>
- <span data-ttu-id="b9e4a-444">666666666</span><span class="sxs-lookup"><span data-stu-id="b9e4a-444">666666666</span></span>
- <span data-ttu-id="b9e4a-445">777777777</span><span class="sxs-lookup"><span data-stu-id="b9e4a-445">777777777</span></span>
- <span data-ttu-id="b9e4a-446">888888888</span><span class="sxs-lookup"><span data-stu-id="b9e4a-446">888888888</span></span>
- <span data-ttu-id="b9e4a-447">999999999</span><span class="sxs-lookup"><span data-stu-id="b9e4a-447">999999999</span></span>
- <span data-ttu-id="b9e4a-448">0000000000</span><span class="sxs-lookup"><span data-stu-id="b9e4a-448">0000000000</span></span>
- <span data-ttu-id="b9e4a-449">1111111111</span><span class="sxs-lookup"><span data-stu-id="b9e4a-449">1111111111</span></span>
- <span data-ttu-id="b9e4a-450">2222222222</span><span class="sxs-lookup"><span data-stu-id="b9e4a-450">2222222222</span></span>
- <span data-ttu-id="b9e4a-451">3333333333</span><span class="sxs-lookup"><span data-stu-id="b9e4a-451">3333333333</span></span>
- <span data-ttu-id="b9e4a-452">4444444444</span><span class="sxs-lookup"><span data-stu-id="b9e4a-452">4444444444</span></span>
- <span data-ttu-id="b9e4a-453">5555555555</span><span class="sxs-lookup"><span data-stu-id="b9e4a-453">5555555555</span></span>
- <span data-ttu-id="b9e4a-454">6666666666</span><span class="sxs-lookup"><span data-stu-id="b9e4a-454">6666666666</span></span>
- <span data-ttu-id="b9e4a-455">7777777777</span><span class="sxs-lookup"><span data-stu-id="b9e4a-455">7777777777</span></span>
- <span data-ttu-id="b9e4a-456">8888888888</span><span class="sxs-lookup"><span data-stu-id="b9e4a-456">8888888888</span></span>
- <span data-ttu-id="b9e4a-457">9999999999</span><span class="sxs-lookup"><span data-stu-id="b9e4a-457">9999999999</span></span>

## <a name="azure-documentdb-auth-key"></a><span data-ttu-id="b9e4a-458">Clé d’authentification Azure DocumentDB</span><span class="sxs-lookup"><span data-stu-id="b9e4a-458">Azure DocumentDB Auth Key</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-459">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-459">Format</span></span>

<span data-ttu-id="b9e4a-460">La chaîne «DocumentDb» suivie des caractères et des chaînes présentés dans le modèle ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-460">The string "DocumentDb" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-461">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-461">Pattern</span></span>

- <span data-ttu-id="b9e4a-462">La chaîne «DocumentDb»</span><span class="sxs-lookup"><span data-stu-id="b9e4a-462">The string "DocumentDb"</span></span>
- <span data-ttu-id="b9e4a-463">N’importe quelle combinaison entre 3-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="b9e4a-463">Any combination of between 3-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="b9e4a-464">Symbole supérieur à (>), signe égal (=), guillemet (") ou apostrophe (')</span><span class="sxs-lookup"><span data-stu-id="b9e4a-464">A greater than symbol (>), an equal sign (=), a quotation mark ("), or an apostrophe (')</span></span>
- <span data-ttu-id="b9e4a-465">Toute combinaison de 86 lettres majuscules ou minuscules, des chiffres, une barre oblique (/) ou un signe plus (+)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-465">Any combination of 86 lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="b9e4a-466">Deux signes égal (=)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-466">Two equal signs (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-467">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-467">Checksum</span></span>

<span data-ttu-id="b9e4a-468">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-468">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-469">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-469">Definition</span></span>

<span data-ttu-id="b9e4a-470">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-470">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-471">L’expression régulière CEP_Regex_AzureDocumentDBAuthKey trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-471">The regular expression CEP_Regex_AzureDocumentDBAuthKey finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-472">L’expression régulière CEP_CommonExampleKeywords ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-472">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-473">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-473">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="b9e4a-474">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="b9e4a-474">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="b9e4a-475">(Notez que techniquement, ce type d’informations sensibles identifie ces mots clés à l’aide d’une expression régulière, et non d’une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-475">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="b9e4a-476">contoso</span><span class="sxs-lookup"><span data-stu-id="b9e4a-476">contoso</span></span>
- <span data-ttu-id="b9e4a-477">société</span><span class="sxs-lookup"><span data-stu-id="b9e4a-477">fabrikam</span></span>
- <span data-ttu-id="b9e4a-478">Northwind</span><span class="sxs-lookup"><span data-stu-id="b9e4a-478">northwind</span></span>
- <span data-ttu-id="b9e4a-479">immédiatement</span><span class="sxs-lookup"><span data-stu-id="b9e4a-479">sandbox</span></span>
- <span data-ttu-id="b9e4a-480">onebox</span><span class="sxs-lookup"><span data-stu-id="b9e4a-480">onebox</span></span>
- <span data-ttu-id="b9e4a-481">hôte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-481">localhost</span></span>
- <span data-ttu-id="b9e4a-482">bouclage</span><span class="sxs-lookup"><span data-stu-id="b9e4a-482">127.0.0.1</span></span>
- <span data-ttu-id="b9e4a-483">testacs.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-483">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="b9e4a-484">com</span><span class="sxs-lookup"><span data-stu-id="b9e4a-484">com</span></span>
- <span data-ttu-id="b9e4a-485">s-int.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-485">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="b9e4a-486">NET</span><span class="sxs-lookup"><span data-stu-id="b9e4a-486">net</span></span>

## <a name="azure-iaas-database-connection-string-and-azure-sql-connection-string"></a><span data-ttu-id="b9e4a-487">Chaîne de connexion à la base de données IAAS Azure et chaîne de connexion Azure SQL</span><span class="sxs-lookup"><span data-stu-id="b9e4a-487">Azure IAAS Database Connection String and Azure SQL Connection String</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-488">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-488">Format</span></span>

<span data-ttu-id="b9e4a-489">La chaîne «Server», «Server» ou «Data source» suivie des caractères et des chaînes décrits dans le modèle ci-dessous, y compris la chaîne «cloudapp. Azure.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-489">The string "Server", "server", or "data source" followed by the characters and strings outlined in the pattern below, including the string "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="b9e4a-490">com» ou «cloudapp. Azure.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-490">com" or "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="b9e4a-491">NET "ou" Database. Windows.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-491">net" or "database.windows.</span></span><!--no-hyperlink--><span data-ttu-id="b9e4a-492">NET ", et la chaîne" password "ou" password "ou" PWD ".</span><span class="sxs-lookup"><span data-stu-id="b9e4a-492">net", and the string "Password" or "password" or "pwd".</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-493">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-493">Pattern</span></span>

- <span data-ttu-id="b9e4a-494">Chaîne «serveur», «serveur» ou «source de données»</span><span class="sxs-lookup"><span data-stu-id="b9e4a-494">The string "Server", "server", or "data source"</span></span>
- <span data-ttu-id="b9e4a-495">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="b9e4a-495">0-2 whitespace characters</span></span>
- <span data-ttu-id="b9e4a-496">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-496">An equal sign (=)</span></span>
- <span data-ttu-id="b9e4a-497">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="b9e4a-497">0-2 whitespace characters</span></span>
- <span data-ttu-id="b9e4a-498">N’importe quelle combinaison entre 1-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="b9e4a-498">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="b9e4a-499">La chaîne «cloudapp. Azure.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-499">The string "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="b9e4a-500">com "," cloudapp. Azure.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-500">com", "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="b9e4a-501">NET "ou" Database. Windows.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-501">net", or "database.windows.</span></span><!--no-hyperlink--><span data-ttu-id="b9e4a-502">NET</span><span class="sxs-lookup"><span data-stu-id="b9e4a-502">net"</span></span>
- <span data-ttu-id="b9e4a-503">N’importe quelle combinaison entre 1-300 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="b9e4a-503">Any combination of between 1-300 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="b9e4a-504">La chaîne "password", "password" ou "PWD"</span><span class="sxs-lookup"><span data-stu-id="b9e4a-504">The string "Password", "password", or "pwd"</span></span>
- <span data-ttu-id="b9e4a-505">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="b9e4a-505">0-2 whitespace characters</span></span>
- <span data-ttu-id="b9e4a-506">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-506">An equal sign (=)</span></span>
- <span data-ttu-id="b9e4a-507">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="b9e4a-507">0-2 whitespace characters</span></span>
- <span data-ttu-id="b9e4a-508">Un ou plusieurs caractères qui ne sont pas des points-virgules (;), guillemets (") ou apostrophe (')</span><span class="sxs-lookup"><span data-stu-id="b9e4a-508">One or more characters that is not a semicolon (;), quotation mark ("), or apostrophe (')</span></span>
- <span data-ttu-id="b9e4a-509">Un point-virgule (;), guillemet (") ou apostrophe (')</span><span class="sxs-lookup"><span data-stu-id="b9e4a-509">A semicolon (;), quotation mark ("), or apostrophe (')</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-510">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-510">Checksum</span></span>

<span data-ttu-id="b9e4a-511">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-511">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-512">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-512">Definition</span></span>

<span data-ttu-id="b9e4a-513">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-513">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-514">L’expression régulière CEP_Regex_AzureConnectionString trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-514">The regular expression CEP_Regex_AzureConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-515">L’expression régulière CEP_CommonExampleKeywords ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-515">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-516">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-516">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="b9e4a-517">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="b9e4a-517">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="b9e4a-518">(Notez que techniquement, ce type d’informations sensibles identifie ces mots clés à l’aide d’une expression régulière, et non d’une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-518">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="b9e4a-519">contoso</span><span class="sxs-lookup"><span data-stu-id="b9e4a-519">contoso</span></span>
- <span data-ttu-id="b9e4a-520">société</span><span class="sxs-lookup"><span data-stu-id="b9e4a-520">fabrikam</span></span>
- <span data-ttu-id="b9e4a-521">Northwind</span><span class="sxs-lookup"><span data-stu-id="b9e4a-521">northwind</span></span>
- <span data-ttu-id="b9e4a-522">immédiatement</span><span class="sxs-lookup"><span data-stu-id="b9e4a-522">sandbox</span></span>
- <span data-ttu-id="b9e4a-523">onebox</span><span class="sxs-lookup"><span data-stu-id="b9e4a-523">onebox</span></span>
- <span data-ttu-id="b9e4a-524">hôte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-524">localhost</span></span>
- <span data-ttu-id="b9e4a-525">bouclage</span><span class="sxs-lookup"><span data-stu-id="b9e4a-525">127.0.0.1</span></span>
- <span data-ttu-id="b9e4a-526">testacs.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-526">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="b9e4a-527">com</span><span class="sxs-lookup"><span data-stu-id="b9e4a-527">com</span></span>
- <span data-ttu-id="b9e4a-528">s-int.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-528">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="b9e4a-529">NET</span><span class="sxs-lookup"><span data-stu-id="b9e4a-529">net</span></span>

## <a name="azure-iot-connection-string"></a><span data-ttu-id="b9e4a-530">Chaîne de connexion Azure IoT</span><span class="sxs-lookup"><span data-stu-id="b9e4a-530">Azure IoT Connection String</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-531">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-531">Format</span></span>

<span data-ttu-id="b9e4a-532">La chaîne «nomhôte» suivie des caractères et des chaînes décrits dans le modèle ci-dessous, y compris les chaînes «Azure-appareils.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-532">The string "HostName" followed by the characters and strings outlined in the pattern below, including the strings "azure-devices.</span></span><!--no-hyperlink--><span data-ttu-id="b9e4a-533">NET "et" SharedAccessKey ".</span><span class="sxs-lookup"><span data-stu-id="b9e4a-533">net" and "SharedAccessKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-534">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-534">Pattern</span></span>

- <span data-ttu-id="b9e4a-535">La chaîne «nomhôte»</span><span class="sxs-lookup"><span data-stu-id="b9e4a-535">The string "HostName"</span></span>
- <span data-ttu-id="b9e4a-536">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="b9e4a-536">0-2 whitespace characters</span></span>
- <span data-ttu-id="b9e4a-537">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-537">An equal sign (=)</span></span>
- <span data-ttu-id="b9e4a-538">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="b9e4a-538">0-2 whitespace characters</span></span>
- <span data-ttu-id="b9e4a-539">N’importe quelle combinaison entre 1-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="b9e4a-539">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="b9e4a-540">La chaîne «Azure-appareils.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-540">The string "azure-devices.</span></span><!--no-hyperlink--><span data-ttu-id="b9e4a-541">NET</span><span class="sxs-lookup"><span data-stu-id="b9e4a-541">net"</span></span>
- <span data-ttu-id="b9e4a-542">N’importe quelle combinaison entre 1-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="b9e4a-542">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="b9e4a-543">La chaîne «SharedAccessKey»</span><span class="sxs-lookup"><span data-stu-id="b9e4a-543">The string "SharedAccessKey"</span></span>
- <span data-ttu-id="b9e4a-544">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="b9e4a-544">0-2 whitespace characters</span></span>
- <span data-ttu-id="b9e4a-545">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-545">An equal sign (=)</span></span>
- <span data-ttu-id="b9e4a-546">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="b9e4a-546">0-2 whitespace characters</span></span>
- <span data-ttu-id="b9e4a-547">Toute combinaison de 43 lettres majuscules ou minuscules, des chiffres, une barre oblique (/) ou un signe plus (+)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-547">Any combination of 43 lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="b9e4a-548">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-548">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-549">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-549">Checksum</span></span>

<span data-ttu-id="b9e4a-550">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-550">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-551">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-551">Definition</span></span>

<span data-ttu-id="b9e4a-552">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-552">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-553">L’expression régulière CEP_Regex_AzureIoTConnectionString trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-553">The regular expression CEP_Regex_AzureIoTConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-554">L’expression régulière CEP_CommonExampleKeywords ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-554">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-555">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-555">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="b9e4a-556">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="b9e4a-556">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="b9e4a-557">(Notez que techniquement, ce type d’informations sensibles identifie ces mots clés à l’aide d’une expression régulière, et non d’une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-557">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="b9e4a-558">contoso</span><span class="sxs-lookup"><span data-stu-id="b9e4a-558">contoso</span></span>
- <span data-ttu-id="b9e4a-559">société</span><span class="sxs-lookup"><span data-stu-id="b9e4a-559">fabrikam</span></span>
- <span data-ttu-id="b9e4a-560">Northwind</span><span class="sxs-lookup"><span data-stu-id="b9e4a-560">northwind</span></span>
- <span data-ttu-id="b9e4a-561">immédiatement</span><span class="sxs-lookup"><span data-stu-id="b9e4a-561">sandbox</span></span>
- <span data-ttu-id="b9e4a-562">onebox</span><span class="sxs-lookup"><span data-stu-id="b9e4a-562">onebox</span></span>
- <span data-ttu-id="b9e4a-563">hôte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-563">localhost</span></span>
- <span data-ttu-id="b9e4a-564">bouclage</span><span class="sxs-lookup"><span data-stu-id="b9e4a-564">127.0.0.1</span></span>
- <span data-ttu-id="b9e4a-565">testacs.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-565">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="b9e4a-566">com</span><span class="sxs-lookup"><span data-stu-id="b9e4a-566">com</span></span>
- <span data-ttu-id="b9e4a-567">s-int.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-567">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="b9e4a-568">NET</span><span class="sxs-lookup"><span data-stu-id="b9e4a-568">net</span></span>

## <a name="azure-publish-setting-password"></a><span data-ttu-id="b9e4a-569">Mot de passe de paramètre de publication Azure</span><span class="sxs-lookup"><span data-stu-id="b9e4a-569">Azure Publish Setting Password</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-570">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-570">Format</span></span>

<span data-ttu-id="b9e4a-571">La chaîne «userpwd =» suivie d’une chaîne alphanumérique.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-571">The string "userpwd=" followed by an alphanumeric string.</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-572">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-572">Pattern</span></span>

- <span data-ttu-id="b9e4a-573">La chaîne «userpwd =»</span><span class="sxs-lookup"><span data-stu-id="b9e4a-573">The string "userpwd="</span></span>
- <span data-ttu-id="b9e4a-574">N’importe quelle combinaison de 60 lettres minuscules ou chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-574">Any combination of 60 lowercase letters or digits</span></span>
- <span data-ttu-id="b9e4a-575">Guillemet (")</span><span class="sxs-lookup"><span data-stu-id="b9e4a-575">A quotation mark (")</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-576">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-576">Checksum</span></span>

<span data-ttu-id="b9e4a-577">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-577">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-578">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-578">Definition</span></span>

<span data-ttu-id="b9e4a-579">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-579">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-580">L’expression régulière CEP_Regex_AzurePublishSettingPasswords trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-580">The regular expression CEP_Regex_AzurePublishSettingPasswords finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-581">L’expression régulière CEP_CommonExampleKeywords ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-581">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>


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

### <a name="keywords"></a><span data-ttu-id="b9e4a-582">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-582">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="b9e4a-583">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="b9e4a-583">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="b9e4a-584">(Notez que techniquement, ce type d’informations sensibles identifie ces mots clés à l’aide d’une expression régulière, et non d’une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-584">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="b9e4a-585">contoso</span><span class="sxs-lookup"><span data-stu-id="b9e4a-585">contoso</span></span>
- <span data-ttu-id="b9e4a-586">société</span><span class="sxs-lookup"><span data-stu-id="b9e4a-586">fabrikam</span></span>
- <span data-ttu-id="b9e4a-587">Northwind</span><span class="sxs-lookup"><span data-stu-id="b9e4a-587">northwind</span></span>
- <span data-ttu-id="b9e4a-588">immédiatement</span><span class="sxs-lookup"><span data-stu-id="b9e4a-588">sandbox</span></span>
- <span data-ttu-id="b9e4a-589">onebox</span><span class="sxs-lookup"><span data-stu-id="b9e4a-589">onebox</span></span>
- <span data-ttu-id="b9e4a-590">hôte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-590">localhost</span></span>
- <span data-ttu-id="b9e4a-591">bouclage</span><span class="sxs-lookup"><span data-stu-id="b9e4a-591">127.0.0.1</span></span>
- <span data-ttu-id="b9e4a-592">testacs.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-592">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="b9e4a-593">com</span><span class="sxs-lookup"><span data-stu-id="b9e4a-593">com</span></span>
- <span data-ttu-id="b9e4a-594">s-int.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-594">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="b9e4a-595">NET</span><span class="sxs-lookup"><span data-stu-id="b9e4a-595">net</span></span>

## <a name="azure-redis-cache-connection-string"></a><span data-ttu-id="b9e4a-596">Chaîne de connexion au cache des inversions Azure</span><span class="sxs-lookup"><span data-stu-id="b9e4a-596">Azure Redis Cache Connection String</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-597">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-597">Format</span></span>

<span data-ttu-id="b9e4a-598">La chaîne «ReDim. cache. Windows.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-598">The string "redis.cache.windows.</span></span><!--no-hyperlink--><span data-ttu-id="b9e4a-599">NET "suivi des caractères et des chaînes décrits dans le modèle ci-dessous, y compris la chaîne" password "ou" PWD ".</span><span class="sxs-lookup"><span data-stu-id="b9e4a-599">net" followed by the characters and strings outlined in the pattern below, including the string "password" or "pwd".</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-600">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-600">Pattern</span></span>

- <span data-ttu-id="b9e4a-601">La chaîne «ReDim. cache. Windows.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-601">The string "redis.cache.windows.</span></span><!--no-hyperlink--><span data-ttu-id="b9e4a-602">NET</span><span class="sxs-lookup"><span data-stu-id="b9e4a-602">net"</span></span>
- <span data-ttu-id="b9e4a-603">N’importe quelle combinaison entre 1-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="b9e4a-603">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="b9e4a-604">La chaîne «password» ou «pwd»</span><span class="sxs-lookup"><span data-stu-id="b9e4a-604">The string "password" or "pwd"</span></span>
- <span data-ttu-id="b9e4a-605">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="b9e4a-605">0-2 whitespace characters</span></span>
- <span data-ttu-id="b9e4a-606">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-606">An equal sign (=)</span></span>
- <span data-ttu-id="b9e4a-607">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="b9e4a-607">0-2 whitespace characters</span></span>
- <span data-ttu-id="b9e4a-608">Toute combinaison de 43 caractères majuscules ou minuscules, des chiffres, une barre oblique (/) ou un signe plus (+)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-608">Any combination of 43 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="b9e4a-609">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-609">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-610">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-610">Checksum</span></span>

<span data-ttu-id="b9e4a-611">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-611">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-612">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-612">Definition</span></span>

<span data-ttu-id="b9e4a-613">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-613">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-614">L’expression régulière CEP_Regex_AzureRedisCacheConnectionString trouve le contenu qui correspond au modèle..</span><span class="sxs-lookup"><span data-stu-id="b9e4a-614">The regular expression CEP_Regex_AzureRedisCacheConnectionString finds content that matches the pattern..</span></span>
- <span data-ttu-id="b9e4a-615">L’expression régulière CEP_CommonExampleKeywords ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-615">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-616">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-616">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="b9e4a-617">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="b9e4a-617">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="b9e4a-618">(Notez que techniquement, ce type d’informations sensibles identifie ces mots clés à l’aide d’une expression régulière, et non d’une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-618">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="b9e4a-619">contoso</span><span class="sxs-lookup"><span data-stu-id="b9e4a-619">contoso</span></span>
- <span data-ttu-id="b9e4a-620">société</span><span class="sxs-lookup"><span data-stu-id="b9e4a-620">fabrikam</span></span>
- <span data-ttu-id="b9e4a-621">Northwind</span><span class="sxs-lookup"><span data-stu-id="b9e4a-621">northwind</span></span>
- <span data-ttu-id="b9e4a-622">immédiatement</span><span class="sxs-lookup"><span data-stu-id="b9e4a-622">sandbox</span></span>
- <span data-ttu-id="b9e4a-623">onebox</span><span class="sxs-lookup"><span data-stu-id="b9e4a-623">onebox</span></span>
- <span data-ttu-id="b9e4a-624">hôte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-624">localhost</span></span>
- <span data-ttu-id="b9e4a-625">bouclage</span><span class="sxs-lookup"><span data-stu-id="b9e4a-625">127.0.0.1</span></span>
- <span data-ttu-id="b9e4a-626">testacs.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-626">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="b9e4a-627">com</span><span class="sxs-lookup"><span data-stu-id="b9e4a-627">com</span></span>
- <span data-ttu-id="b9e4a-628">s-int.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-628">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="b9e4a-629">NET</span><span class="sxs-lookup"><span data-stu-id="b9e4a-629">net</span></span>

## <a name="azure-sas"></a><span data-ttu-id="b9e4a-630">SAS Azure</span><span class="sxs-lookup"><span data-stu-id="b9e4a-630">Azure SAS</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-631">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-631">Format</span></span>

<span data-ttu-id="b9e4a-632">La chaîne «SIG» suivie des caractères et des chaînes présentés dans le modèle ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-632">The string "sig" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-633">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-633">Pattern</span></span>

- <span data-ttu-id="b9e4a-634">La chaîne «SIG»</span><span class="sxs-lookup"><span data-stu-id="b9e4a-634">The string "sig"</span></span>
- <span data-ttu-id="b9e4a-635">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="b9e4a-635">0-2 whitespace characters</span></span>
- <span data-ttu-id="b9e4a-636">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-636">An equal sign (=)</span></span>
- <span data-ttu-id="b9e4a-637">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="b9e4a-637">0-2 whitespace characters</span></span>
- <span data-ttu-id="b9e4a-638">Toute combinaison comprise entre 43-53 caractères majuscules ou minuscules, des chiffres ou le signe pourcentage (%)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-638">Any combination of between 43-53 characters that are lower- or uppercase letters, digits, or the percent sign (%)</span></span>
- <span data-ttu-id="b9e4a-639">La chaîne «% 3D»</span><span class="sxs-lookup"><span data-stu-id="b9e4a-639">The string "%3d"</span></span>
- <span data-ttu-id="b9e4a-640">Tout caractère qui n’est pas une lettre majuscule, un chiffre ou un signe de pourcentage (%)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-640">Any character that is not a lower- or uppercase letter, digit, or percent sign (%)</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-641">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-641">Checksum</span></span>

<span data-ttu-id="b9e4a-642">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-642">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-643">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-643">Definition</span></span>

<span data-ttu-id="b9e4a-644">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-644">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-645">L’expression régulière CEP_Regex_AzureSAS trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-645">The regular expression CEP_Regex_AzureSAS finds content that matches the pattern.</span></span>

```
<!--Azure SAS-->
<Entity id="4d235014-e564-47f4-a6fb-6ebb4a826834" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureSAS" />
  </Pattern>
</Entity>
```

## <a name="azure-service-bus-connection-string"></a><span data-ttu-id="b9e4a-646">Chaîne de connexion au bus des services Azure</span><span class="sxs-lookup"><span data-stu-id="b9e4a-646">Azure Service Bus Connection String</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-647">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-647">Format</span></span>

<span data-ttu-id="b9e4a-648">La chaîne «point de terminaison» suivie des caractères et des chaînes décrits dans le modèle ci-dessous, y compris les chaînes «ServiceBus. Windows.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-648">The string "EndPoint" followed by the characters and strings outlined in the pattern below, including the strings "servicebus.windows.</span></span><!--no-hyperlink--><span data-ttu-id="b9e4a-649">NET "et" SharedAccesKey ".</span><span class="sxs-lookup"><span data-stu-id="b9e4a-649">net" and "SharedAccesKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-650">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-650">Pattern</span></span>

- <span data-ttu-id="b9e4a-651">Chaîne «point de terminaison»</span><span class="sxs-lookup"><span data-stu-id="b9e4a-651">The string "EndPoint"</span></span>
- <span data-ttu-id="b9e4a-652">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="b9e4a-652">0-2 whitespace characters</span></span>
- <span data-ttu-id="b9e4a-653">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-653">An equal sign (=)</span></span>
- <span data-ttu-id="b9e4a-654">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="b9e4a-654">0-2 whitespace characters</span></span>
- <span data-ttu-id="b9e4a-655">N’importe quelle combinaison entre 1-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="b9e4a-655">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="b9e4a-656">La chaîne «ServiceBus. Windows.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-656">The string "servicebus.windows.</span></span><!--no-hyperlink--><span data-ttu-id="b9e4a-657">NET</span><span class="sxs-lookup"><span data-stu-id="b9e4a-657">net"</span></span>
- <span data-ttu-id="b9e4a-658">N’importe quelle combinaison entre 1-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="b9e4a-658">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="b9e4a-659">La chaîne «SharedAccessKey»</span><span class="sxs-lookup"><span data-stu-id="b9e4a-659">The string "SharedAccessKey"</span></span>
- <span data-ttu-id="b9e4a-660">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="b9e4a-660">0-2 whitespace characters</span></span>
- <span data-ttu-id="b9e4a-661">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-661">An equal sign (=)</span></span>
- <span data-ttu-id="b9e4a-662">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="b9e4a-662">0-2 whitespace characters</span></span>
- <span data-ttu-id="b9e4a-663">Toute combinaison de 43 caractères majuscules ou minuscules, des chiffres, une barre oblique (/) ou un signe plus (+)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-663">Any combination of 43 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="b9e4a-664">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-664">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-665">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-665">Checksum</span></span>

<span data-ttu-id="b9e4a-666">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-666">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-667">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-667">Definition</span></span>

<span data-ttu-id="b9e4a-668">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-668">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-669">L’expression régulière CEP_Regex_AzureServiceBusConnectionString trouve le contenu qui correspond au modèle..</span><span class="sxs-lookup"><span data-stu-id="b9e4a-669">The regular expression CEP_Regex_AzureServiceBusConnectionString finds content that matches the pattern..</span></span>
- <span data-ttu-id="b9e4a-670">L’expression régulière CEP_CommonExampleKeywords ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-670">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-671">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-671">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="b9e4a-672">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="b9e4a-672">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="b9e4a-673">(Notez que techniquement, ce type d’informations sensibles identifie ces mots clés à l’aide d’une expression régulière, et non d’une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-673">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="b9e4a-674">contoso</span><span class="sxs-lookup"><span data-stu-id="b9e4a-674">contoso</span></span>
- <span data-ttu-id="b9e4a-675">société</span><span class="sxs-lookup"><span data-stu-id="b9e4a-675">fabrikam</span></span>
- <span data-ttu-id="b9e4a-676">Northwind</span><span class="sxs-lookup"><span data-stu-id="b9e4a-676">northwind</span></span>
- <span data-ttu-id="b9e4a-677">immédiatement</span><span class="sxs-lookup"><span data-stu-id="b9e4a-677">sandbox</span></span>
- <span data-ttu-id="b9e4a-678">onebox</span><span class="sxs-lookup"><span data-stu-id="b9e4a-678">onebox</span></span>
- <span data-ttu-id="b9e4a-679">hôte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-679">localhost</span></span>
- <span data-ttu-id="b9e4a-680">bouclage</span><span class="sxs-lookup"><span data-stu-id="b9e4a-680">127.0.0.1</span></span>
- <span data-ttu-id="b9e4a-681">testacs.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-681">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="b9e4a-682">com</span><span class="sxs-lookup"><span data-stu-id="b9e4a-682">com</span></span>
- <span data-ttu-id="b9e4a-683">s-int.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-683">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="b9e4a-684">NET</span><span class="sxs-lookup"><span data-stu-id="b9e4a-684">net</span></span>

## <a name="azure-storage-account-key"></a><span data-ttu-id="b9e4a-685">Clé de compte de stockage Azure</span><span class="sxs-lookup"><span data-stu-id="b9e4a-685">Azure Storage Account Key</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-686">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-686">Format</span></span>

<span data-ttu-id="b9e4a-687">La chaîne «DefaultEndpointsProtocol» suivie des caractères et des chaînes décrits dans le modèle ci-dessous, y compris la chaîne «AccountKey».</span><span class="sxs-lookup"><span data-stu-id="b9e4a-687">The string "DefaultEndpointsProtocol" followed by the characters and strings outlined in the pattern below, including the string "AccountKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-688">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-688">Pattern</span></span>

- <span data-ttu-id="b9e4a-689">La chaîne «DefaultEndpointsProtocol»</span><span class="sxs-lookup"><span data-stu-id="b9e4a-689">The string "DefaultEndpointsProtocol"</span></span>
- <span data-ttu-id="b9e4a-690">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="b9e4a-690">0-2 whitespace characters</span></span>
- <span data-ttu-id="b9e4a-691">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-691">An equal sign (=)</span></span>
- <span data-ttu-id="b9e4a-692">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="b9e4a-692">0-2 whitespace characters</span></span>
- <span data-ttu-id="b9e4a-693">N’importe quelle combinaison entre 1-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="b9e4a-693">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="b9e4a-694">La chaîne «AccountKey»</span><span class="sxs-lookup"><span data-stu-id="b9e4a-694">The string "AccountKey"</span></span>
- <span data-ttu-id="b9e4a-695">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="b9e4a-695">0-2 whitespace characters</span></span>
- <span data-ttu-id="b9e4a-696">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-696">An equal sign (=)</span></span>
- <span data-ttu-id="b9e4a-697">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="b9e4a-697">0-2 whitespace characters</span></span>
- <span data-ttu-id="b9e4a-698">Toute combinaison de 86 caractères majuscules ou minuscules, des chiffres, une barre oblique (/) ou un signe plus (+)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-698">Any combination of 86 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="b9e4a-699">Deux signes égal (=)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-699">Two equal signs (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-700">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-700">Checksum</span></span>

<span data-ttu-id="b9e4a-701">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-701">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-702">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-702">Definition</span></span>

<span data-ttu-id="b9e4a-703">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-703">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-704">L’expression régulière CEP_Regex_AzureStorageAccountKey trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-704">The regular expression CEP_Regex_AzureStorageAccountKey finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-705">L’expression régulière CEP_AzureEmulatorStorageAccountFilter ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-705">The regular expression CEP_AzureEmulatorStorageAccountFilter does **not** find content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-706">L’expression régulière CEP_CommonExampleKeywords ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-706">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-707">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-707">Keywords</span></span>

#### <a name="cep_azureemulatorstorageaccountfilter"></a><span data-ttu-id="b9e4a-708">CEP_AzureEmulatorStorageAccountFilter</span><span class="sxs-lookup"><span data-stu-id="b9e4a-708">CEP_AzureEmulatorStorageAccountFilter</span></span>

<span data-ttu-id="b9e4a-709">(Notez que techniquement, ce type d’informations sensibles identifie ces mots clés à l’aide d’une expression régulière, et non d’une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-709">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="b9e4a-710">Eby8vdM02xNOcqFlqUwJPLlmEtlCDXJ1OUzFT50uSRZ6IFsuFq2UVErCz4I6tq/K1SZFPTOtr/KBHBeksoGMGw = =</span><span class="sxs-lookup"><span data-stu-id="b9e4a-710">Eby8vdM02xNOcqFlqUwJPLlmEtlCDXJ1OUzFT50uSRZ6IFsuFq2UVErCz4I6tq/K1SZFPTOtr/KBHBeksoGMGw==</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="b9e4a-711">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="b9e4a-711">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="b9e4a-712">(Notez que techniquement, ce type d’informations sensibles identifie ces mots clés à l’aide d’une expression régulière, et non d’une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-712">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="b9e4a-713">contoso</span><span class="sxs-lookup"><span data-stu-id="b9e4a-713">contoso</span></span>
- <span data-ttu-id="b9e4a-714">société</span><span class="sxs-lookup"><span data-stu-id="b9e4a-714">fabrikam</span></span>
- <span data-ttu-id="b9e4a-715">Northwind</span><span class="sxs-lookup"><span data-stu-id="b9e4a-715">northwind</span></span>
- <span data-ttu-id="b9e4a-716">immédiatement</span><span class="sxs-lookup"><span data-stu-id="b9e4a-716">sandbox</span></span>
- <span data-ttu-id="b9e4a-717">onebox</span><span class="sxs-lookup"><span data-stu-id="b9e4a-717">onebox</span></span>
- <span data-ttu-id="b9e4a-718">hôte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-718">localhost</span></span>
- <span data-ttu-id="b9e4a-719">bouclage</span><span class="sxs-lookup"><span data-stu-id="b9e4a-719">127.0.0.1</span></span>
- <span data-ttu-id="b9e4a-720">testacs.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-720">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="b9e4a-721">com</span><span class="sxs-lookup"><span data-stu-id="b9e4a-721">com</span></span>
- <span data-ttu-id="b9e4a-722">s-int.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-722">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="b9e4a-723">NET</span><span class="sxs-lookup"><span data-stu-id="b9e4a-723">net</span></span>

## <a name="azure-storage-account-key-generic"></a><span data-ttu-id="b9e4a-724">Clé de compte de stockage Azure (Générique)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-724">Azure Storage Account Key (Generic)</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-725">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-725">Format</span></span>

<span data-ttu-id="b9e4a-726">Toute combinaison de 86 lettres majuscules ou minuscules, des chiffres, la barre oblique (/) ou le signe plus (+), précédée ou suivie des caractères décrits dans le modèle ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-726">Any combination of 86 lower- or uppercase letters, digits, the forward slash (/), or plus sign (+), preceded or followed by the characters outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-727">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-727">Pattern</span></span>

- <span data-ttu-id="b9e4a-728">0-1 du symbole supérieur à (>), apostrophe ('), signe égal (=), guillemet (") ou dièse (#)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-728">0-1 of the greater than symbol (>), apostrophe ('), equal sign (=), quotation mark ("), or number sign (#)</span></span>
- <span data-ttu-id="b9e4a-729">Toute combinaison de 86 caractères majuscules ou minuscules, des chiffres, la barre oblique (/) ou le signe plus (+)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-729">Any combination of 86 characters that are lower- or uppercase letters, digits, the forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="b9e4a-730">Deux signes égal (=)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-730">Two equal signs (=)</span></span>


### <a name="checksum"></a><span data-ttu-id="b9e4a-731">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-731">Checksum</span></span>

<span data-ttu-id="b9e4a-732">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-732">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-733">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-733">Definition</span></span>

<span data-ttu-id="b9e4a-734">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-734">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-735">L’expression régulière CEP_Regex_AzureStorageAccountKeyGeneric trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-735">The regular expression CEP_Regex_AzureStorageAccountKeyGeneric finds content that matches the pattern.</span></span>

```
<!--Azure Storage Account Key (Generic)-->
<Entity id="7ff41bd0-5419-4523-91d6-383b3a37f084" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureStorageAccountKeyGeneric" />
  </Pattern>
</Entity>
```

## <a name="belgium-national-number"></a><span data-ttu-id="b9e4a-736">Numéro national Belgique</span><span class="sxs-lookup"><span data-stu-id="b9e4a-736">Belgium National Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-737">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-737">Format</span></span>

<span data-ttu-id="b9e4a-738">11 chiffres plus des délimiteurs</span><span class="sxs-lookup"><span data-stu-id="b9e4a-738">11 digits plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-739">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-739">Pattern</span></span>

<span data-ttu-id="b9e4a-740">11 chiffres plus des délimiteurs :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-740">11 digits plus delimiters:</span></span>
- <span data-ttu-id="b9e4a-741">Six chiffres et deux points au format AA.MM.JJ pour la date de naissance </span><span class="sxs-lookup"><span data-stu-id="b9e4a-741">Six digits and two periods in the format YY.MM.DD for date of birth</span></span> 
- <span data-ttu-id="b9e4a-742">Un trait d’union</span><span class="sxs-lookup"><span data-stu-id="b9e4a-742">A hyphen</span></span> 
- <span data-ttu-id="b9e4a-743">Trois chiffres séquentiels (impairs pour les hommes, pairs pour les femmes) </span><span class="sxs-lookup"><span data-stu-id="b9e4a-743">Three sequential digits (odd for males, even for females)</span></span> 
- <span data-ttu-id="b9e4a-744">Un point</span><span class="sxs-lookup"><span data-stu-id="b9e4a-744">A period</span></span> 
- <span data-ttu-id="b9e4a-745">Deux chiffres de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-745">Two digits that are a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-746">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-746">Checksum</span></span>

<span data-ttu-id="b9e4a-747">Oui</span><span class="sxs-lookup"><span data-stu-id="b9e4a-747">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-748">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-748">Definition</span></span>

<span data-ttu-id="b9e4a-749">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-749">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-750">La fonction Func_belgium_national_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-750">The function Func_belgium_national_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-751">Un mot clé figurant dans la liste Keyword_belgium_national_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-751">A keyword from Keyword_belgium_national_number is found.</span></span>
- <span data-ttu-id="b9e4a-752">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-752">The checksum passes.</span></span>

```
<!-- Belgium National Number -->
  <Entity id="fb969c9e-0fd1-4b18-8091-a2123c5e6a54" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_belgium_national_number"/>
     <Match idRef="Keyword_belgium_national_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b9e4a-753">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-753">Keywords</span></span>

#### <a name="keyword_belgium_national_number"></a><span data-ttu-id="b9e4a-754">Keyword_belgium_national_number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-754">Keyword_belgium_national_number</span></span>

- <span data-ttu-id="b9e4a-755">Identité</span><span class="sxs-lookup"><span data-stu-id="b9e4a-755">Identity</span></span>
- <span data-ttu-id="b9e4a-756">Son</span><span class="sxs-lookup"><span data-stu-id="b9e4a-756">Registration</span></span>
- <span data-ttu-id="b9e4a-757">Identificateur</span><span class="sxs-lookup"><span data-stu-id="b9e4a-757">Identification</span></span> 
- <span data-ttu-id="b9e4a-758">ID</span><span class="sxs-lookup"><span data-stu-id="b9e4a-758">ID</span></span> 
- <span data-ttu-id="b9e4a-759">Identiteitskaart</span><span class="sxs-lookup"><span data-stu-id="b9e4a-759">Identiteitskaart</span></span>
- <span data-ttu-id="b9e4a-760">Registratie nummer</span><span class="sxs-lookup"><span data-stu-id="b9e4a-760">Registratie nummer</span></span> 
- <span data-ttu-id="b9e4a-761">Identificatie nummer</span><span class="sxs-lookup"><span data-stu-id="b9e4a-761">Identificatie nummer</span></span> 
- <span data-ttu-id="b9e4a-762">Identiteit</span><span class="sxs-lookup"><span data-stu-id="b9e4a-762">Identiteit</span></span>
- <span data-ttu-id="b9e4a-763">Registratie</span><span class="sxs-lookup"><span data-stu-id="b9e4a-763">Registratie</span></span>
- <span data-ttu-id="b9e4a-764">Identificatie</span><span class="sxs-lookup"><span data-stu-id="b9e4a-764">Identificatie</span></span> 
- <span data-ttu-id="b9e4a-765">Carte d’identité</span><span class="sxs-lookup"><span data-stu-id="b9e4a-765">Carte d’identité</span></span> 
- <span data-ttu-id="b9e4a-766">numéro d’immatriculation</span><span class="sxs-lookup"><span data-stu-id="b9e4a-766">numéro d'immatriculation</span></span>
- <span data-ttu-id="b9e4a-767">numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="b9e4a-767">numéro d'identification</span></span>
- <span data-ttu-id="b9e4a-768">identité</span><span class="sxs-lookup"><span data-stu-id="b9e4a-768">identité</span></span> 
- <span data-ttu-id="b9e4a-769">inscriptions</span><span class="sxs-lookup"><span data-stu-id="b9e4a-769">inscription</span></span> 
- <span data-ttu-id="b9e4a-770">Identifikation</span><span class="sxs-lookup"><span data-stu-id="b9e4a-770">Identifikation</span></span>
- <span data-ttu-id="b9e4a-771">Identifizierung</span><span class="sxs-lookup"><span data-stu-id="b9e4a-771">Identifizierung</span></span>
- <span data-ttu-id="b9e4a-772">Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="b9e4a-772">Identifikationsnummer</span></span>
- <span data-ttu-id="b9e4a-773">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="b9e4a-773">Personalausweis</span></span>
- <span data-ttu-id="b9e4a-774">Registrierung</span><span class="sxs-lookup"><span data-stu-id="b9e4a-774">Registrierung</span></span>
- <span data-ttu-id="b9e4a-775">Registrationsnummer</span><span class="sxs-lookup"><span data-stu-id="b9e4a-775">Registrationsnummer</span></span>

   
## <a name="brazil-cpf-number"></a><span data-ttu-id="b9e4a-776">Numéro CPF Brésil</span><span class="sxs-lookup"><span data-stu-id="b9e4a-776">Brazil CPF Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-777">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-777">Format</span></span>

<span data-ttu-id="b9e4a-778">11 chiffres qui incluent un chiffre de contrôle et peuvent ou non être mis en forme </span><span class="sxs-lookup"><span data-stu-id="b9e4a-778">11 digits that include a check digit and can be formatted or unformatted</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-779">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-779">Pattern</span></span>

<span data-ttu-id="b9e4a-780">Avec</span><span class="sxs-lookup"><span data-stu-id="b9e4a-780">Formatted:</span></span>
- <span data-ttu-id="b9e4a-781">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-781">Three digits</span></span> 
- <span data-ttu-id="b9e4a-782">Un point </span><span class="sxs-lookup"><span data-stu-id="b9e4a-782">A period</span></span> 
- <span data-ttu-id="b9e4a-783">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-783">Three digits</span></span> 
- <span data-ttu-id="b9e4a-784">Un point </span><span class="sxs-lookup"><span data-stu-id="b9e4a-784">A period</span></span> 
- <span data-ttu-id="b9e4a-785">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-785">Three digits</span></span> 
- <span data-ttu-id="b9e4a-786">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="b9e4a-786">A hyphen</span></span> 
- <span data-ttu-id="b9e4a-787">Deux chiffres de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-787">Two digits which are check digits</span></span>

<span data-ttu-id="b9e4a-788">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-788">Unformatted:</span></span>
- <span data-ttu-id="b9e4a-789">11 chiffres où les deux derniers sont des chiffres de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-789">11 digits where the last two digits are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-790">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-790">Checksum</span></span>

<span data-ttu-id="b9e4a-791">Oui</span><span class="sxs-lookup"><span data-stu-id="b9e4a-791">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-792">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-792">Definition</span></span>

<span data-ttu-id="b9e4a-793">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-793">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-794">La fonction Func_brazil_cpf trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-794">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-795">Un mot clé figurant dans la liste Keyword_brazil_cpf est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-795">A keyword from Keyword_brazil_cpf is found.</span></span>
- <span data-ttu-id="b9e4a-796">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-796">The checksum passes.</span></span>

<span data-ttu-id="b9e4a-797">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-797">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-798">La fonction Func_brazil_cpf trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-798">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-799">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-799">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-800">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-800">Keywords</span></span>

#### <a name="keyword_brazil_cpf"></a><span data-ttu-id="b9e4a-801">Keyword_brazil_cpf</span><span class="sxs-lookup"><span data-stu-id="b9e4a-801">Keyword_brazil_cpf</span></span>

- <span data-ttu-id="b9e4a-802">CPF</span><span class="sxs-lookup"><span data-stu-id="b9e4a-802">CPF</span></span>
- <span data-ttu-id="b9e4a-803">Identificateur</span><span class="sxs-lookup"><span data-stu-id="b9e4a-803">Identification</span></span>
- <span data-ttu-id="b9e4a-804">Son</span><span class="sxs-lookup"><span data-stu-id="b9e4a-804">Registration</span></span>
- <span data-ttu-id="b9e4a-805">Parts</span><span class="sxs-lookup"><span data-stu-id="b9e4a-805">Revenue</span></span>
- <span data-ttu-id="b9e4a-806">Cadastro de Pessoas Físicas</span><span class="sxs-lookup"><span data-stu-id="b9e4a-806">Cadastro de Pessoas Físicas</span></span> 
- <span data-ttu-id="b9e4a-807">Imposto</span><span class="sxs-lookup"><span data-stu-id="b9e4a-807">Imposto</span></span> 
- <span data-ttu-id="b9e4a-808">Identificação</span><span class="sxs-lookup"><span data-stu-id="b9e4a-808">Identificação</span></span> 
- <span data-ttu-id="b9e4a-809">Inscrição</span><span class="sxs-lookup"><span data-stu-id="b9e4a-809">Inscrição</span></span> 
- <span data-ttu-id="b9e4a-810">Receita</span><span class="sxs-lookup"><span data-stu-id="b9e4a-810">Receita</span></span> 
   
## <a name="brazil-legal-entity-number-cnpj"></a><span data-ttu-id="b9e4a-811">Numéro d’entité juridique (CNPJ) Brésil</span><span class="sxs-lookup"><span data-stu-id="b9e4a-811">Brazil Legal Entity Number (CNPJ)</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-812">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-812">Format</span></span>

<span data-ttu-id="b9e4a-813">14 chiffres qui incluent un numéro d’enregistrement, un numéro de succursale et des chiffres de contrôle, avec des délimiteurs en plus</span><span class="sxs-lookup"><span data-stu-id="b9e4a-813">14 digits that include a registration number, branch number, and check digits, plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-814">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-814">Pattern</span></span>
<span data-ttu-id="b9e4a-815">14 chiffres plus des délimiteurs :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-815">14 digits, plus delimiters:</span></span>
- <span data-ttu-id="b9e4a-816">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-816">Two digits</span></span> 
- <span data-ttu-id="b9e4a-817">Un point </span><span class="sxs-lookup"><span data-stu-id="b9e4a-817">A period</span></span> 
- <span data-ttu-id="b9e4a-818">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-818">Three digits</span></span> 
- <span data-ttu-id="b9e4a-819">Un point </span><span class="sxs-lookup"><span data-stu-id="b9e4a-819">A period</span></span> 
- <span data-ttu-id="b9e4a-820">Trois chiffres (ces huit premiers chiffres composent le numéro d’enregistrement) </span><span class="sxs-lookup"><span data-stu-id="b9e4a-820">Three digits (these first eight digits are the registration number)</span></span> 
- <span data-ttu-id="b9e4a-821">Une barre oblique </span><span class="sxs-lookup"><span data-stu-id="b9e4a-821">A forward slash</span></span> 
- <span data-ttu-id="b9e4a-822">Le numéro de succursale à quatre chiffres </span><span class="sxs-lookup"><span data-stu-id="b9e4a-822">Four-digit branch number</span></span> 
- <span data-ttu-id="b9e4a-823">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="b9e4a-823">A hyphen</span></span> 
- <span data-ttu-id="b9e4a-824">Deux chiffres de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-824">Two digits which are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-825">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-825">Checksum</span></span>

<span data-ttu-id="b9e4a-826">Oui</span><span class="sxs-lookup"><span data-stu-id="b9e4a-826">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-827">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-827">Definition</span></span>

<span data-ttu-id="b9e4a-828">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-828">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-829">La fonction Func_brazil_cnpj trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-829">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-830">Un mot clé figurant dans la liste Keyword_brazil_cnpj est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-830">A keyword from Keyword_brazil_cnpj is found.</span></span>
- <span data-ttu-id="b9e4a-831">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-831">The checksum passes.</span></span>

<span data-ttu-id="b9e4a-832">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-832">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-833">La fonction Func_brazil_cnpj trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-833">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-834">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-834">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-835">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-835">Keywords</span></span>

#### <a name="keyword_brazil_cnpj"></a><span data-ttu-id="b9e4a-836">Keyword_brazil_cnpj</span><span class="sxs-lookup"><span data-stu-id="b9e4a-836">Keyword_brazil_cnpj</span></span>

- <span data-ttu-id="b9e4a-837">CNPJ</span><span class="sxs-lookup"><span data-stu-id="b9e4a-837">CNPJ</span></span> 
- <span data-ttu-id="b9e4a-838">CNPJ/MF</span><span class="sxs-lookup"><span data-stu-id="b9e4a-838">CNPJ/MF</span></span> 
- <span data-ttu-id="b9e4a-839">CNPJ-MF</span><span class="sxs-lookup"><span data-stu-id="b9e4a-839">CNPJ-MF</span></span> 
- <span data-ttu-id="b9e4a-840">National Registry of Legal Entities</span><span class="sxs-lookup"><span data-stu-id="b9e4a-840">National Registry of Legal Entities</span></span> 
- <span data-ttu-id="b9e4a-841">Taxpayers Registry</span><span class="sxs-lookup"><span data-stu-id="b9e4a-841">Taxpayers Registry</span></span> 
- <span data-ttu-id="b9e4a-842">Legal entity</span><span class="sxs-lookup"><span data-stu-id="b9e4a-842">Legal entity</span></span> 
- <span data-ttu-id="b9e4a-843">Legal entities</span><span class="sxs-lookup"><span data-stu-id="b9e4a-843">Legal entities</span></span> 
- <span data-ttu-id="b9e4a-844">Registration Status</span><span class="sxs-lookup"><span data-stu-id="b9e4a-844">Registration Status</span></span> 
- <span data-ttu-id="b9e4a-845">Business</span><span class="sxs-lookup"><span data-stu-id="b9e4a-845">Business</span></span> 
- <span data-ttu-id="b9e4a-846">Company</span><span class="sxs-lookup"><span data-stu-id="b9e4a-846">Company</span></span>
- <span data-ttu-id="b9e4a-847">CNPJ</span><span class="sxs-lookup"><span data-stu-id="b9e4a-847">CNPJ</span></span> 
- <span data-ttu-id="b9e4a-848">Cadastro Nacional da Pessoa Jurídica</span><span class="sxs-lookup"><span data-stu-id="b9e4a-848">Cadastro Nacional da Pessoa Jurídica</span></span> 
- <span data-ttu-id="b9e4a-849">Cadastro Geral de Contribuintes</span><span class="sxs-lookup"><span data-stu-id="b9e4a-849">Cadastro Geral de Contribuintes</span></span> 
- <span data-ttu-id="b9e4a-850">CGC</span><span class="sxs-lookup"><span data-stu-id="b9e4a-850">CGC</span></span> 
- <span data-ttu-id="b9e4a-851">Pessoa jurídica</span><span class="sxs-lookup"><span data-stu-id="b9e4a-851">Pessoa jurídica</span></span> 
- <span data-ttu-id="b9e4a-852">Pessoas jurídicas</span><span class="sxs-lookup"><span data-stu-id="b9e4a-852">Pessoas jurídicas</span></span> 
- <span data-ttu-id="b9e4a-853">Situação cadastral</span><span class="sxs-lookup"><span data-stu-id="b9e4a-853">Situação cadastral</span></span> 
- <span data-ttu-id="b9e4a-854">Inscrição</span><span class="sxs-lookup"><span data-stu-id="b9e4a-854">Inscrição</span></span> 
- <span data-ttu-id="b9e4a-855">Empresa</span><span class="sxs-lookup"><span data-stu-id="b9e4a-855">Empresa</span></span> 
   
## <a name="brazil-national-id-card-rg"></a><span data-ttu-id="b9e4a-856">	Brazil National ID Card (RG)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-856">Brazil National ID Card (RG)</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-857">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-857">Format</span></span>

<span data-ttu-id="b9e4a-858">Registro Geral (ancien format): neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-858">Registro Geral (old format): Nine digits</span></span>

<span data-ttu-id="b9e4a-859">Registro de identidade (RIC) (nouveau format): 11 chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-859">Registro de Identidade (RIC) (new format): 11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-860">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-860">Pattern</span></span>

<span data-ttu-id="b9e4a-861">Registro Geral (ancien format) :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-861">Registro Geral (old format):</span></span>
- <span data-ttu-id="b9e4a-862">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-862">Two digits</span></span> 
- <span data-ttu-id="b9e4a-863">Un point </span><span class="sxs-lookup"><span data-stu-id="b9e4a-863">A period</span></span> 
- <span data-ttu-id="b9e4a-864">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-864">Three digits</span></span> 
- <span data-ttu-id="b9e4a-865">Un point </span><span class="sxs-lookup"><span data-stu-id="b9e4a-865">A period</span></span> 
- <span data-ttu-id="b9e4a-866">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-866">Three digits</span></span> 
- <span data-ttu-id="b9e4a-867">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="b9e4a-867">A hyphen</span></span> 
- <span data-ttu-id="b9e4a-868">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-868">One digit which is a check digit</span></span>

<span data-ttu-id="b9e4a-869">Registro de identidade (RIC) (nouveau format):</span><span class="sxs-lookup"><span data-stu-id="b9e4a-869">Registro de Identidade (RIC) (new format):</span></span>
- <span data-ttu-id="b9e4a-870">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-870">10 digits</span></span> 
- <span data-ttu-id="b9e4a-871">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="b9e4a-871">A hyphen</span></span> 
- <span data-ttu-id="b9e4a-872">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-872">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-873">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-873">Checksum</span></span>

<span data-ttu-id="b9e4a-874">Oui</span><span class="sxs-lookup"><span data-stu-id="b9e4a-874">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-875">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-875">Definition</span></span>

<span data-ttu-id="b9e4a-876">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-876">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-877">La fonction Func_brazil_rg trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-877">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-878">Un mot clé figurant dans la liste Keyword_brazil_rg est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-878">A keyword from Keyword_brazil_rg is found.</span></span>
- <span data-ttu-id="b9e4a-879">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-879">The checksum passes.</span></span>

<span data-ttu-id="b9e4a-880">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-880">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-881">La fonction Func_brazil_rg trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-881">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-882">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-882">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-883">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-883">Keywords</span></span>

#### <a name="keyword_brazil_rg"></a><span data-ttu-id="b9e4a-884">Keyword_brazil_rg</span><span class="sxs-lookup"><span data-stu-id="b9e4a-884">Keyword_brazil_rg</span></span>

<span data-ttu-id="b9e4a-885">Cédula de identidade carte d’identité número de rregistro Registro de identidade Registro Geral RG (ce mot clé respecte la casse) RIC (ce mot clé respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-885">Cédula de identidade identity card national id número de rregistro registro de Iidentidade registro geral RG (this keyword is case sensitive) RIC (this keyword is case sensitive)</span></span> 
   
## <a name="canada-bank-account-number"></a><span data-ttu-id="b9e4a-886">Numéro de compte bancaire Canada</span><span class="sxs-lookup"><span data-stu-id="b9e4a-886">Canada Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-887">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-887">Format</span></span>

<span data-ttu-id="b9e4a-888">Sept ou douze chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-888">Seven or twelve digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-889">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-889">Pattern</span></span>

<span data-ttu-id="b9e4a-890">Un numéro de compte bancaire au Canada est composé de sept ou douze chiffres.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-890">A Canada Bank Account Number is seven or twelve digits.</span></span>

<span data-ttu-id="b9e4a-891">Un numéro de transit de compte bancaire du Canada est indiqué au format suivant :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-891">A Canada bank account transit number is:</span></span>
- <span data-ttu-id="b9e4a-892">Cinq chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-892">Five digits</span></span> 
- <span data-ttu-id="b9e4a-893">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="b9e4a-893">A hyphen</span></span> 
- <span data-ttu-id="b9e4a-894">Trois chiffres ou</span><span class="sxs-lookup"><span data-stu-id="b9e4a-894">Three digits OR</span></span>
- <span data-ttu-id="b9e4a-895">Un zéro « 0 » </span><span class="sxs-lookup"><span data-stu-id="b9e4a-895">A zero "0"</span></span> 
- <span data-ttu-id="b9e4a-896">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-896">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-897">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-897">Checksum</span></span>

<span data-ttu-id="b9e4a-898">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-898">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-899">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-899">Definition</span></span>

<span data-ttu-id="b9e4a-900">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-900">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-901">L’expression régulière Regex_canada_bank_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-901">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-902">Un mot clé figurant dans la liste Keyword_canada_bank_account_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-902">A keyword from Keyword_canada_bank_account_number is found.</span></span>
- <span data-ttu-id="b9e4a-903">L’expression régulière Regex_canada_bank_account_transit_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-903">The regular expression Regex_canada_bank_account_transit_number finds content that matches the pattern.</span></span>

<span data-ttu-id="b9e4a-904">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-904">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-905">L’expression régulière Regex_canada_bank_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-905">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-906">Un mot clé figurant dans la liste Keyword_canada_bank_account_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-906">A keyword from Keyword_canada_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-907">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-907">Keywords</span></span>

#### <a name="keyword_canada_bank_account_number"></a><span data-ttu-id="b9e4a-908">Keyword_canada_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-908">Keyword_canada_bank_account_number</span></span>

- <span data-ttu-id="b9e4a-909">obligations d’épargne du Canada</span><span class="sxs-lookup"><span data-stu-id="b9e4a-909">canada savings bonds</span></span>
- <span data-ttu-id="b9e4a-910">agence du revenu du Canada</span><span class="sxs-lookup"><span data-stu-id="b9e4a-910">canada revenue agency</span></span>
- <span data-ttu-id="b9e4a-911">institution financière du Canada</span><span class="sxs-lookup"><span data-stu-id="b9e4a-911">canadian financial institution</span></span>
- <span data-ttu-id="b9e4a-912">formulaire de dépôt direct</span><span class="sxs-lookup"><span data-stu-id="b9e4a-912">direct deposit form</span></span>
- <span data-ttu-id="b9e4a-913">citoyen canadien</span><span class="sxs-lookup"><span data-stu-id="b9e4a-913">canadian citizen</span></span>
- <span data-ttu-id="b9e4a-914">représentant légal</span><span class="sxs-lookup"><span data-stu-id="b9e4a-914">legal representative</span></span>
- <span data-ttu-id="b9e4a-915">notaire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-915">notary public</span></span>
- <span data-ttu-id="b9e4a-916">commissaire à l’assermentation</span><span class="sxs-lookup"><span data-stu-id="b9e4a-916">commissioner for oaths</span></span>
- <span data-ttu-id="b9e4a-917">prestation pour la garde d’enfants</span><span class="sxs-lookup"><span data-stu-id="b9e4a-917">child care benefit</span></span>
- <span data-ttu-id="b9e4a-918">prestation universelle pour la garde d’enfants</span><span class="sxs-lookup"><span data-stu-id="b9e4a-918">universal child care</span></span>
- <span data-ttu-id="b9e4a-919">prestation fiscale canadienne pour enfants</span><span class="sxs-lookup"><span data-stu-id="b9e4a-919">canada child tax benefit</span></span>
- <span data-ttu-id="b9e4a-920">prestation fiscale pour le revenu gagné</span><span class="sxs-lookup"><span data-stu-id="b9e4a-920">income tax benefit</span></span>
- <span data-ttu-id="b9e4a-921">taxe de vente harmonisée</span><span class="sxs-lookup"><span data-stu-id="b9e4a-921">harmonized sales tax</span></span>
- <span data-ttu-id="b9e4a-922">numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="b9e4a-922">social insurance number</span></span>
- <span data-ttu-id="b9e4a-923">remboursement d’impôt</span><span class="sxs-lookup"><span data-stu-id="b9e4a-923">income tax refund</span></span>
- <span data-ttu-id="b9e4a-924">prestation fiscale pour enfants</span><span class="sxs-lookup"><span data-stu-id="b9e4a-924">child tax benefit</span></span>
- <span data-ttu-id="b9e4a-925">paiements aux territoires</span><span class="sxs-lookup"><span data-stu-id="b9e4a-925">territorial payments</span></span>
- <span data-ttu-id="b9e4a-926">numéro d’institution</span><span class="sxs-lookup"><span data-stu-id="b9e4a-926">institution number</span></span>
- <span data-ttu-id="b9e4a-927">demande de dépôt</span><span class="sxs-lookup"><span data-stu-id="b9e4a-927">deposit request</span></span>
- <span data-ttu-id="b9e4a-928">informations bancaires</span><span class="sxs-lookup"><span data-stu-id="b9e4a-928">banking information</span></span>
- <span data-ttu-id="b9e4a-929">dépôt direct</span><span class="sxs-lookup"><span data-stu-id="b9e4a-929">direct deposit</span></span>
   
## <a name="canada-drivers-license-number"></a><span data-ttu-id="b9e4a-930">Numéro de permis de conduire Canada</span><span class="sxs-lookup"><span data-stu-id="b9e4a-930">Canada Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-931">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-931">Format</span></span>

<span data-ttu-id="b9e4a-932">Varie selon la province</span><span class="sxs-lookup"><span data-stu-id="b9e4a-932">Varies by province</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-933">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-933">Pattern</span></span>

<span data-ttu-id="b9e4a-934">Plusieurs modèles pour les différentes provinces : Alberta, Colombie-Britannique, Manitoba, Nouveau-Brunswick, Terre-Neuve-et-Labrador, Nouvelle-Écosse, Ontario, Île-du-Prince-Édouard, Québec et Saskatchewan</span><span class="sxs-lookup"><span data-stu-id="b9e4a-934">Various patterns covering Alberta, British Columbia, Manitoba, New Brunswick, Newfoundland/Labrador, Nova Scotia, Ontario, Prince Edward Island, Quebec, and Saskatchewan</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-935">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-935">Checksum</span></span>

<span data-ttu-id="b9e4a-936">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-936">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-937">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-937">Definition</span></span>

<span data-ttu-id="b9e4a-938">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-938">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-939">La fonction Func_[province_name]_drivers_license_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-939">The function Func_[province_name]_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-940">Un mot clé figurant dans la liste Keyword_[province_name]_drivers_license_name est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-940">A keyword from Keyword_[province_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="b9e4a-941">Un mot clé figurant dans la liste Keyword_canada_drivers_license est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-941">A keyword from Keyword_canada_drivers_license is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-942">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-942">Keywords</span></span>

#### <a name="keyword_province_name_drivers_license_name"></a><span data-ttu-id="b9e4a-943">Keyword_[province_name]_drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="b9e4a-943">Keyword_[province_name]_drivers_license_name</span></span>

- <span data-ttu-id="b9e4a-944">L’abréviation de la province, par exemple AB</span><span class="sxs-lookup"><span data-stu-id="b9e4a-944">The province abbreviation, for example AB</span></span>
- <span data-ttu-id="b9e4a-945">Le nom de la province, par exemple Alberta</span><span class="sxs-lookup"><span data-stu-id="b9e4a-945">The province name, for example Alberta</span></span>

#### <a name="keyword_canada_drivers_license"></a><span data-ttu-id="b9e4a-946">Keyword_canada_drivers_license</span><span class="sxs-lookup"><span data-stu-id="b9e4a-946">Keyword_canada_drivers_license</span></span>

- <span data-ttu-id="b9e4a-947">LD</span><span class="sxs-lookup"><span data-stu-id="b9e4a-947">DL</span></span>
- <span data-ttu-id="b9e4a-948">DISTRIBUTION</span><span class="sxs-lookup"><span data-stu-id="b9e4a-948">DLS</span></span>
- <span data-ttu-id="b9e4a-949">CÈDE</span><span class="sxs-lookup"><span data-stu-id="b9e4a-949">CDL</span></span>
- <span data-ttu-id="b9e4a-950">CDLS</span><span class="sxs-lookup"><span data-stu-id="b9e4a-950">CDLS</span></span>
- <span data-ttu-id="b9e4a-951">DriverLic</span><span class="sxs-lookup"><span data-stu-id="b9e4a-951">DriverLic</span></span>
- <span data-ttu-id="b9e4a-952">DriverLics</span><span class="sxs-lookup"><span data-stu-id="b9e4a-952">DriverLics</span></span>
- <span data-ttu-id="b9e4a-953">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="b9e4a-953">DriverLicense</span></span>
- <span data-ttu-id="b9e4a-954">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="b9e4a-954">DriverLicenses</span></span>
- <span data-ttu-id="b9e4a-955">DriverLicence</span><span class="sxs-lookup"><span data-stu-id="b9e4a-955">DriverLicence</span></span>
- <span data-ttu-id="b9e4a-956">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="b9e4a-956">DriverLicences</span></span>
- <span data-ttu-id="b9e4a-957">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-957">Driver Lic</span></span>
- <span data-ttu-id="b9e4a-958">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-958">Driver Lics</span></span>
- <span data-ttu-id="b9e4a-959">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-959">Driver License</span></span>
- <span data-ttu-id="b9e4a-960">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-960">Driver Licenses</span></span>
- <span data-ttu-id="b9e4a-961">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-961">Driver Licence</span></span>
- <span data-ttu-id="b9e4a-962">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-962">Driver Licences</span></span>
- <span data-ttu-id="b9e4a-963">DriversLic</span><span class="sxs-lookup"><span data-stu-id="b9e4a-963">DriversLic</span></span>
- <span data-ttu-id="b9e4a-964">DriversLics</span><span class="sxs-lookup"><span data-stu-id="b9e4a-964">DriversLics</span></span>
- <span data-ttu-id="b9e4a-965">DriversLicence</span><span class="sxs-lookup"><span data-stu-id="b9e4a-965">DriversLicence</span></span>
- <span data-ttu-id="b9e4a-966">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="b9e4a-966">DriversLicences</span></span>
- <span data-ttu-id="b9e4a-967">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="b9e4a-967">DriversLicense</span></span>
- <span data-ttu-id="b9e4a-968">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="b9e4a-968">DriversLicenses</span></span>
- <span data-ttu-id="b9e4a-969">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-969">Drivers Lic</span></span>
- <span data-ttu-id="b9e4a-970">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-970">Drivers Lics</span></span>
- <span data-ttu-id="b9e4a-971">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-971">Drivers License</span></span>
- <span data-ttu-id="b9e4a-972">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-972">Drivers Licenses</span></span>
- <span data-ttu-id="b9e4a-973">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-973">Drivers Licence</span></span>
- <span data-ttu-id="b9e4a-974">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-974">Drivers Licences</span></span>
- <span data-ttu-id="b9e4a-975">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="b9e4a-975">Driver'Lic</span></span>
- <span data-ttu-id="b9e4a-976">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="b9e4a-976">Driver'Lics</span></span>
- <span data-ttu-id="b9e4a-977">Driver'License</span><span class="sxs-lookup"><span data-stu-id="b9e4a-977">Driver'License</span></span>
- <span data-ttu-id="b9e4a-978">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="b9e4a-978">Driver'Licenses</span></span>
- <span data-ttu-id="b9e4a-979">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="b9e4a-979">Driver'Licence</span></span>
- <span data-ttu-id="b9e4a-980">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="b9e4a-980">Driver'Licences</span></span>
- <span data-ttu-id="b9e4a-981">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-981">Driver' Lic</span></span>
- <span data-ttu-id="b9e4a-982">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-982">Driver' Lics</span></span>
- <span data-ttu-id="b9e4a-983">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-983">Driver' License</span></span>
- <span data-ttu-id="b9e4a-984">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-984">Driver' Licenses</span></span>
- <span data-ttu-id="b9e4a-985">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-985">Driver' Licence</span></span>
- <span data-ttu-id="b9e4a-986">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-986">Driver' Licences</span></span>
- <span data-ttu-id="b9e4a-987">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="b9e4a-987">Driver'sLic</span></span>
- <span data-ttu-id="b9e4a-988">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="b9e4a-988">Driver'sLics</span></span>
- <span data-ttu-id="b9e4a-989">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="b9e4a-989">Driver'sLicense</span></span>
- <span data-ttu-id="b9e4a-990">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="b9e4a-990">Driver'sLicenses</span></span>
- <span data-ttu-id="b9e4a-991">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="b9e4a-991">Driver'sLicence</span></span>
- <span data-ttu-id="b9e4a-992">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="b9e4a-992">Driver'sLicences</span></span>
- <span data-ttu-id="b9e4a-993">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-993">Driver's Lic</span></span>
- <span data-ttu-id="b9e4a-994">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-994">Driver's Lics</span></span>
- <span data-ttu-id="b9e4a-995">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-995">Driver's License</span></span>
- <span data-ttu-id="b9e4a-996">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-996">Driver's Licenses</span></span>
- <span data-ttu-id="b9e4a-997">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-997">Driver's Licence</span></span>
- <span data-ttu-id="b9e4a-998">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-998">Driver's Licences</span></span>
- <span data-ttu-id="b9e4a-999">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-999">Permis de Conduire</span></span>
- <span data-ttu-id="b9e4a-1000">id</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1000">id</span></span>
- <span data-ttu-id="b9e4a-1001">Ids</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1001">ids</span></span>
- <span data-ttu-id="b9e4a-1002">numéro carte d’identification</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1002">idcard number</span></span>
- <span data-ttu-id="b9e4a-1003">numéros carte d’identification</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1003">idcard numbers</span></span>
- <span data-ttu-id="b9e4a-1004"># carte d’identification</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1004">idcard #</span></span>
- <span data-ttu-id="b9e4a-1005"># carte d’identification</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1005">idcard #s</span></span>
- <span data-ttu-id="b9e4a-1006">carte d’identification</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1006">idcard card</span></span>
- <span data-ttu-id="b9e4a-1007">cartes d’identification</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1007">idcard cards</span></span>
- <span data-ttu-id="b9e4a-1008">carte d’identification</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1008">idcard</span></span>
- <span data-ttu-id="b9e4a-1009">numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1009">identification number</span></span>
- <span data-ttu-id="b9e4a-1010">numéros d’identification</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1010">identification numbers</span></span>
- <span data-ttu-id="b9e4a-1011"># identification</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1011">identification #</span></span>
- <span data-ttu-id="b9e4a-1012"># identification</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1012">identification #s</span></span>
- <span data-ttu-id="b9e4a-1013">carte d’identification</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1013">identification card</span></span>
- <span data-ttu-id="b9e4a-1014">cartes d’identification</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1014">identification cards</span></span>
- <span data-ttu-id="b9e4a-1015">identificateur</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1015">identification</span></span> 
- <span data-ttu-id="b9e4a-1016">LD #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1016">DL#</span></span>
- <span data-ttu-id="b9e4a-1017">DISTRIBUTION #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1017">DLS#</span></span> 
- <span data-ttu-id="b9e4a-1018">CÈDE #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1018">CDL#</span></span> 
- <span data-ttu-id="b9e4a-1019">CDLS #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1019">CDLS#</span></span> 
- <span data-ttu-id="b9e4a-1020">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1020">DriverLic#</span></span> 
- <span data-ttu-id="b9e4a-1021">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1021">DriverLics#</span></span> 
- <span data-ttu-id="b9e4a-1022">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1022">DriverLicense#</span></span> 
- <span data-ttu-id="b9e4a-1023">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1023">DriverLicenses#</span></span> 
- <span data-ttu-id="b9e4a-1024">DriverLicence #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1024">DriverLicence#</span></span> 
- <span data-ttu-id="b9e4a-1025">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1025">DriverLicences#</span></span> 
- <span data-ttu-id="b9e4a-1026">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1026">Driver Lic#</span></span>
- <span data-ttu-id="b9e4a-1027">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1027">Driver Lics#</span></span> 
- <span data-ttu-id="b9e4a-1028">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1028">Driver License#</span></span> 
- <span data-ttu-id="b9e4a-1029">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1029">Driver Licenses#</span></span> 
- <span data-ttu-id="b9e4a-1030">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1030">Driver License#</span></span> 
- <span data-ttu-id="b9e4a-1031">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1031">Driver Licences#</span></span> 
- <span data-ttu-id="b9e4a-1032">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1032">DriversLic#</span></span> 
- <span data-ttu-id="b9e4a-1033">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1033">DriversLics#</span></span> 
- <span data-ttu-id="b9e4a-1034">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1034">DriversLicense#</span></span> 
- <span data-ttu-id="b9e4a-1035">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1035">DriversLicenses#</span></span> 
- <span data-ttu-id="b9e4a-1036">DriversLicence #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1036">DriversLicence#</span></span> 
- <span data-ttu-id="b9e4a-1037">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1037">DriversLicences#</span></span> 
- <span data-ttu-id="b9e4a-1038">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1038">Drivers Lic#</span></span> 
- <span data-ttu-id="b9e4a-1039">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1039">Drivers Lics#</span></span> 
- <span data-ttu-id="b9e4a-1040">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1040">Drivers License#</span></span> 
- <span data-ttu-id="b9e4a-1041">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1041">Drivers Licenses#</span></span> 
- <span data-ttu-id="b9e4a-1042">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1042">Drivers Licence#</span></span> 
- <span data-ttu-id="b9e4a-1043">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1043">Drivers Licences#</span></span> 
- <span data-ttu-id="b9e4a-1044">Driver'Lic #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1044">Driver'Lic#</span></span> 
- <span data-ttu-id="b9e4a-1045">Driver'Lics #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1045">Driver'Lics#</span></span> 
- <span data-ttu-id="b9e4a-1046">Driver'License #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1046">Driver'License#</span></span> 
- <span data-ttu-id="b9e4a-1047">Driver'Licenses #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1047">Driver'Licenses#</span></span> 
- <span data-ttu-id="b9e4a-1048">Driver'Licence #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1048">Driver'Licence#</span></span> 
- <span data-ttu-id="b9e4a-1049">Driver'Licences #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1049">Driver'Licences#</span></span> 
- <span data-ttu-id="b9e4a-1050">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1050">Driver' Lic#</span></span> 
- <span data-ttu-id="b9e4a-1051">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1051">Driver' Lics#</span></span> 
- <span data-ttu-id="b9e4a-1052">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1052">Driver' License#</span></span> 
- <span data-ttu-id="b9e4a-1053">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1053">Driver' Licenses#</span></span> 
- <span data-ttu-id="b9e4a-1054">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1054">Driver' Licence#</span></span> 
- <span data-ttu-id="b9e4a-1055">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1055">Driver' Licences#</span></span> 
- <span data-ttu-id="b9e4a-1056">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1056">Driver'sLic#</span></span> 
- <span data-ttu-id="b9e4a-1057">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1057">Driver'sLics#</span></span> 
- <span data-ttu-id="b9e4a-1058">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1058">Driver'sLicense#</span></span> 
- <span data-ttu-id="b9e4a-1059">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1059">Driver'sLicenses#</span></span> 
- <span data-ttu-id="b9e4a-1060">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1060">Driver'sLicence#</span></span> 
- <span data-ttu-id="b9e4a-1061">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1061">Driver'sLicences#</span></span> 
- <span data-ttu-id="b9e4a-1062">#Permisconduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1062">Driver's Lic#</span></span> 
- <span data-ttu-id="b9e4a-1063">#Permisconduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1063">Driver's Lics#</span></span> 
- <span data-ttu-id="b9e4a-1064">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1064">Driver's License#</span></span> 
- <span data-ttu-id="b9e4a-1065">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1065">Driver's Licenses#</span></span> 
- <span data-ttu-id="b9e4a-1066">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1066">Driver's Licence#</span></span> 
- <span data-ttu-id="b9e4a-1067">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1067">Driver's Licences#</span></span> 
- <span data-ttu-id="b9e4a-1068">Permis de conduire #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1068">Permis de Conduire#</span></span> 
- <span data-ttu-id="b9e4a-1069">Réf #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1069">id#</span></span> 
- <span data-ttu-id="b9e4a-1070">codes #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1070">ids#</span></span> 
- <span data-ttu-id="b9e4a-1071">#carte carte d’identification</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1071">idcard card#</span></span> 
- <span data-ttu-id="b9e4a-1072">#cartes carte d’identification</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1072">idcard cards#</span></span> 
- <span data-ttu-id="b9e4a-1073">carte d’identification #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1073">idcard#</span></span> 
- <span data-ttu-id="b9e4a-1074">#carte d’identification</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1074">identification card#</span></span> 
- <span data-ttu-id="b9e4a-1075">#cartes d’identification</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1075">identification cards#</span></span> 
- <span data-ttu-id="b9e4a-1076">identificateur #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1076">identification#</span></span> 
   
## <a name="canada-health-service-number"></a><span data-ttu-id="b9e4a-1077">Numéro de service de santé Canada</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1077">Canada Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-1078">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1078">Format</span></span>

<span data-ttu-id="b9e4a-1079">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1079">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-1080">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1080">Pattern</span></span>

<span data-ttu-id="b9e4a-1081">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1081">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-1082">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1082">Checksum</span></span>

<span data-ttu-id="b9e4a-1083">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1083">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-1084">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1084">Definition</span></span>

<span data-ttu-id="b9e4a-1085">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1085">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-1086">L’expression régulière Regex_canada_health_service_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1086">The regular expression Regex_canada_health_service_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-1087">Un mot clé figurant dans la liste Keyword_canada_health_service_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1087">A keyword from Keyword_canada_health_service_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-1088">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1088">Keywords</span></span>

#### <a name="keyword_canada_health_service_number"></a><span data-ttu-id="b9e4a-1089">Keyword_canada_health_service_number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1089">Keyword_canada_health_service_number</span></span>

- <span data-ttu-id="b9e4a-1090">numéro d’assurance-maladie</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1090">personal health number</span></span>
- <span data-ttu-id="b9e4a-1091">informations sur le patient</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1091">patient information</span></span>
- <span data-ttu-id="b9e4a-1092">services de santé</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1092">health services</span></span>
- <span data-ttu-id="b9e4a-1093">services spécialisés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1093">speciality services</span></span>
- <span data-ttu-id="b9e4a-1094">accident automobile</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1094">automobile accident</span></span>
- <span data-ttu-id="b9e4a-1095">hôpital pour malades</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1095">patient hospital</span></span>
- <span data-ttu-id="b9e4a-1096">psychiatrist</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1096">psychiatrist</span></span>
- <span data-ttu-id="b9e4a-1097">indemnisation des salariés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1097">workers compensation</span></span>
- <span data-ttu-id="b9e4a-1098">incapacité</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1098">disability</span></span>
      
## <a name="canada-passport-number"></a><span data-ttu-id="b9e4a-1099">Numéro de passeport Canada</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1099">Canada Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-1100">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1100">Format</span></span>

<span data-ttu-id="b9e4a-1101">Deux lettres majuscules suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1101">Two uppercase letters followed by six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-1102">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1102">Pattern</span></span>

<span data-ttu-id="b9e4a-1103">Deux lettres majuscules suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1103">Two uppercase letters followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-1104">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1104">Checksum</span></span>

<span data-ttu-id="b9e4a-1105">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1105">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-1106">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1106">Definition</span></span>

<span data-ttu-id="b9e4a-1107">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1107">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-1108">L’expression régulière Regex_canada_passport_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1108">The regular expression Regex_canada_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-1109">Un mot clé depuis Keyword_canada_passport_number ou Keyword_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1109">A keyword from Keyword_canada_passport_number or Keyword_passport is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-1110">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1110">Keywords</span></span>

#### <a name="keyword_canada_passport_number"></a><span data-ttu-id="b9e4a-1111">Keyword_canada_passport_number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1111">Keyword_canada_passport_number</span></span>

- <span data-ttu-id="b9e4a-1112">citoyenneté canadienne</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1112">canadian citizenship</span></span>
- <span data-ttu-id="b9e4a-1113">passeport canadien</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1113">canadian passport</span></span>
- <span data-ttu-id="b9e4a-1114">demande de passeport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1114">passport application</span></span>
- <span data-ttu-id="b9e4a-1115">photos pour passeport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1115">passport photos</span></span>
- <span data-ttu-id="b9e4a-1116">traducteur agréé</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1116">certified translator</span></span>
- <span data-ttu-id="b9e4a-1117">citoyens canadiens</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1117">canadian citizens</span></span>
- <span data-ttu-id="b9e4a-1118">temps de traitement</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1118">processing times</span></span>
- <span data-ttu-id="b9e4a-1119">demande de renouvellement</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1119">renewal application</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="b9e4a-1120">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1120">Keyword_passport</span></span>

- <span data-ttu-id="b9e4a-1121">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1121">Passport Number</span></span>
- <span data-ttu-id="b9e4a-1122">N° de passeport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1122">Passport No</span></span>
- <span data-ttu-id="b9e4a-1123"># Passeport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1123">Passport #</span></span>
- <span data-ttu-id="b9e4a-1124">Tel #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1124">Passport#</span></span>
- <span data-ttu-id="b9e4a-1125">PassportID</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1125">PassportID</span></span>
- <span data-ttu-id="b9e4a-1126">N ° passeport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1126">Passportno</span></span>
- <span data-ttu-id="b9e4a-1127">passportnumber</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1127">passportnumber</span></span>
- <span data-ttu-id="b9e4a-1128">パスポート</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1128">パスポート</span></span>
- <span data-ttu-id="b9e4a-1129">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1129">パスポート番号</span></span>
- <span data-ttu-id="b9e4a-1130">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1130">パスポートのNum</span></span>
- <span data-ttu-id="b9e4a-1131">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1131">パスポート＃</span></span>
- <span data-ttu-id="b9e4a-1132">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1132">Numéro de passeport</span></span>
- <span data-ttu-id="b9e4a-1133">Passeport n°</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1133">Passeport n °</span></span>
- <span data-ttu-id="b9e4a-1134">Passeport numéro</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1134">Passeport Non</span></span>
- <span data-ttu-id="b9e4a-1135"># Passeport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1135">Passeport #</span></span>
- <span data-ttu-id="b9e4a-1136">Passeport #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1136">Passeport#</span></span>
- <span data-ttu-id="b9e4a-1137">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1137">PasseportNon</span></span>
- <span data-ttu-id="b9e4a-1138">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1138">Passeportn °</span></span>
   
## <a name="canada-personal-health-identification-number-phin"></a><span data-ttu-id="b9e4a-1139">NIMP (numéro d’identification médicale personnel) Canada</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1139">Canada Personal Health Identification Number (PHIN)</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-1140">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1140">Format</span></span>

<span data-ttu-id="b9e4a-1141">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1141">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-1142">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1142">Pattern</span></span>

<span data-ttu-id="b9e4a-1143">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1143">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-1144">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1144">Checksum</span></span>

<span data-ttu-id="b9e4a-1145">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1145">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-1146">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1146">Definition</span></span>

<span data-ttu-id="b9e4a-1147">Une stratégie DLP est sûre à 75% d’avoir détecté ce type d’informations sensibles si, dans une proximité de 300 caractères: l’expression régulière Regex_canada_phin trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1147">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_canada_phin finds content that matches the pattern.</span></span>
<span data-ttu-id="b9e4a-1148">Au moins deux mots clés de Keyword_canada_phin ou Keyword_canada_provinces sont trouvés..</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1148">At least two keywords from Keyword_canada_phin or Keyword_canada_provinces are found..</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-1149">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1149">Keywords</span></span>

#### <a name="keyword_canada_phin"></a><span data-ttu-id="b9e4a-1150">Keyword_canada_phin</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1150">Keyword_canada_phin</span></span>

- <span data-ttu-id="b9e4a-1151">numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1151">social insurance number</span></span>
- <span data-ttu-id="b9e4a-1152">loi sur les renseignements médicaux</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1152">health information act</span></span>
- <span data-ttu-id="b9e4a-1153">renseignements relatifs à l’impôt sur le revenu</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1153">income tax information</span></span>
- <span data-ttu-id="b9e4a-1154">santé Manitoba</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1154">manitoba health</span></span>
- <span data-ttu-id="b9e4a-1155">enregistrement aux services de santé</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1155">health registration</span></span>
- <span data-ttu-id="b9e4a-1156">achats de médicaments sur ordonnance</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1156">prescription purchases</span></span>
- <span data-ttu-id="b9e4a-1157">admissibilité aux prestations</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1157">benefit eligibility</span></span>
- <span data-ttu-id="b9e4a-1158">santé personnelle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1158">personal health</span></span>
- <span data-ttu-id="b9e4a-1159">procuration</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1159">power of attorney</span></span>
- <span data-ttu-id="b9e4a-1160">numéro d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1160">registration number</span></span>
- <span data-ttu-id="b9e4a-1161">numéro d’assurance-maladie</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1161">personal health number</span></span>
- <span data-ttu-id="b9e4a-1162">recommandation par le médecin</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1162">practitioner referral</span></span>
- <span data-ttu-id="b9e4a-1163">professionnel de bien-être</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1163">wellness professional</span></span>
- <span data-ttu-id="b9e4a-1164">orientation d’un patient</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1164">patient referral</span></span>
- <span data-ttu-id="b9e4a-1165">santé et bien-être</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1165">health and wellness</span></span>

#### <a name="keyword_canada_provinces"></a><span data-ttu-id="b9e4a-1166">Keyword_canada_provinces</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1166">Keyword_canada_provinces</span></span>

- <span data-ttu-id="b9e4a-1167">Nunavut</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1167">Nunavut</span></span>
- <span data-ttu-id="b9e4a-1168">Régime</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1168">Quebec</span></span>
- <span data-ttu-id="b9e4a-1169">Territoires du Nord-Ouest</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1169">Northwest Territories</span></span>
- <span data-ttu-id="b9e4a-1170">Brand</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1170">Ontario</span></span>
- <span data-ttu-id="b9e4a-1171">Colombie-britannique</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1171">British Columbia</span></span>
- <span data-ttu-id="b9e4a-1172">Alberta</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1172">Alberta</span></span>
- <span data-ttu-id="b9e4a-1173">En-dessus</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1173">Saskatchewan</span></span>
- <span data-ttu-id="b9e4a-1174">Manitoba</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1174">Manitoba</span></span>
- <span data-ttu-id="b9e4a-1175">Yukon</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1175">Yukon</span></span>
- <span data-ttu-id="b9e4a-1176">Terre-Neuve-et-Labrador</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1176">Newfoundland and Labrador</span></span>
- <span data-ttu-id="b9e4a-1177">Nouveau-Brunswick</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1177">New Brunswick</span></span>
- <span data-ttu-id="b9e4a-1178">Nouvelle-Écosse</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1178">Nova Scotia</span></span>
- <span data-ttu-id="b9e4a-1179">Île-du-Prince-Édouard</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1179">Prince Edward Island</span></span>
- <span data-ttu-id="b9e4a-1180">Canada</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1180">Canada</span></span>
   
## <a name="canada-social-insurance-number"></a><span data-ttu-id="b9e4a-1181">Numéro d'assurance sociale Canada</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1181">Canada Social Insurance Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-1182">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1182">Format</span></span>

<span data-ttu-id="b9e4a-1183">Neuf chiffres avec éventuellement des traits d’union ou des espaces</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1183">Nine digits with optional hyphens or spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-1184">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1184">Pattern</span></span>

<span data-ttu-id="b9e4a-1185">Avec</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1185">Formatted:</span></span>
- <span data-ttu-id="b9e4a-1186">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1186">Three digits</span></span> 
- <span data-ttu-id="b9e4a-1187">Un trait d’union ou un espace</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1187">A hyphen or space</span></span> 
- <span data-ttu-id="b9e4a-1188">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1188">Three digits</span></span> 
- <span data-ttu-id="b9e4a-1189">Un trait d’union ou un espace</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1189">A hyphen or space</span></span> 
- <span data-ttu-id="b9e4a-1190">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1190">Three digits</span></span>

<span data-ttu-id="b9e4a-1191">Non mis en forme: neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1191">Unformatted: Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-1192">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1192">Checksum</span></span>

<span data-ttu-id="b9e4a-1193">Oui</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1193">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-1194">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1194">Definition</span></span>

<span data-ttu-id="b9e4a-1195">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1195">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-1196">La fonction Func_canadian_sin trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1196">The function Func_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-1197">Au moins deux des éléments suivants, quelle que soit la combinaison :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1197">At least two of any combination of the following:</span></span>
    - <span data-ttu-id="b9e4a-1198">Un mot clé figurant dans la liste Keyword_sin est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1198">A keyword from Keyword_sin is found.</span></span>
    - <span data-ttu-id="b9e4a-1199">Un mot clé figurant dans la liste Keyword_sin_collaborative est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1199">A keyword from Keyword_sin_collaborative is found.</span></span>
    - <span data-ttu-id="b9e4a-1200">La fonction Func_eu_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1200">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="b9e4a-1201">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1201">The checksum passes.</span></span>

<span data-ttu-id="b9e4a-1202">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1202">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-1203">La fonction Func_unformatted_canadian_sin trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1203">The function Func_unformatted_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-1204">Un mot clé figurant dans la liste Keyword_sin est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1204">A keyword from Keyword_sin is found.</span></span>
- <span data-ttu-id="b9e4a-1205">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1205">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-1206">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1206">Keywords</span></span>

#### <a name="keyword_sin"></a><span data-ttu-id="b9e4a-1207">Keyword_sin</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1207">Keyword_sin</span></span>

- <span data-ttu-id="b9e4a-1208">assoc</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1208">sin</span></span> 
- <span data-ttu-id="b9e4a-1209">assurance sociale</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1209">social insurance</span></span> 
- <span data-ttu-id="b9e4a-1210">numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1210">numero d'assurance sociale</span></span> 
- <span data-ttu-id="b9e4a-1211">péchés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1211">sins</span></span> 
- <span data-ttu-id="b9e4a-1212">SSN</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1212">ssn</span></span> 
- <span data-ttu-id="b9e4a-1213">numéros</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1213">ssns</span></span> 
- <span data-ttu-id="b9e4a-1214">sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1214">social security</span></span> 
- <span data-ttu-id="b9e4a-1215">numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1215">numero d'assurance social</span></span> 
- <span data-ttu-id="b9e4a-1216">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1216">national identification number</span></span> 
- <span data-ttu-id="b9e4a-1217">id national</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1217">national id</span></span> 
- <span data-ttu-id="b9e4a-1218">sine #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1218">sin#</span></span> 
- <span data-ttu-id="b9e4a-1219">ass soc</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1219">soc ins</span></span> 
- <span data-ttu-id="b9e4a-1220">ass sociale</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1220">social ins</span></span> 

#### <a name="keyword_sin_collaborative"></a><span data-ttu-id="b9e4a-1221">Keyword_sin_collaborative</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1221">Keyword_sin_collaborative</span></span>

- <span data-ttu-id="b9e4a-1222">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1222">driver's license</span></span> 
- <span data-ttu-id="b9e4a-1223">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1223">drivers license</span></span> 
- <span data-ttu-id="b9e4a-1224">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1224">driver's licence</span></span> 
- <span data-ttu-id="b9e4a-1225">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1225">drivers licence</span></span> 
- <span data-ttu-id="b9e4a-1226">DOB</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1226">DOB</span></span> 
- <span data-ttu-id="b9e4a-1227">Birthdate</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1227">Birthdate</span></span> 
- <span data-ttu-id="b9e4a-1228">Birthday</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1228">Birthday</span></span> 
- <span data-ttu-id="b9e4a-1229">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1229">Date of Birth</span></span> 
   
## <a name="chile-identity-card-number"></a><span data-ttu-id="b9e4a-1230">	Numéro de carte d’identité Chili</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1230">Chile Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-1231">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1231">Format</span></span>

<span data-ttu-id="b9e4a-1232">7-8 chiffres plus des délimiteurs un chiffre ou une lettre</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1232">7-8 digits plus delimiters a check digit or letter</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-1233">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1233">Pattern</span></span>

<span data-ttu-id="b9e4a-1234">7 ou 8 chiffres, plus des délimiteurs :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1234">7-8 digits plus delimiters:</span></span>
- <span data-ttu-id="b9e4a-1235">1 ou 2 chiffres </span><span class="sxs-lookup"><span data-stu-id="b9e4a-1235">1-2 digits</span></span> 
- <span data-ttu-id="b9e4a-1236">Un point </span><span class="sxs-lookup"><span data-stu-id="b9e4a-1236">A period</span></span> 
- <span data-ttu-id="b9e4a-1237">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1237">Three digits</span></span> 
- <span data-ttu-id="b9e4a-1238">Un point </span><span class="sxs-lookup"><span data-stu-id="b9e4a-1238">A period</span></span> 
- <span data-ttu-id="b9e4a-1239">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1239">Three digits</span></span> 
- <span data-ttu-id="b9e4a-1240">Un tiret</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1240">A dash</span></span> 
- <span data-ttu-id="b9e4a-1241">Un chiffre ou une lettre (ne respectant pas la casse) de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1241">One digit or letter (not case sensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-1242">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1242">Checksum</span></span>

<span data-ttu-id="b9e4a-1243">Oui</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1243">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-1244">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1244">Definition</span></span>

<span data-ttu-id="b9e4a-1245">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1245">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-1246">La fonction Func_chile_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1246">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-1247">Un mot clé figurant dans la liste Keyword_chile_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1247">A keyword from Keyword_chile_id_card is found.</span></span>
- <span data-ttu-id="b9e4a-1248">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1248">The checksum passes.</span></span>

<span data-ttu-id="b9e4a-1249">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1249">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-1250">La fonction Func_chile_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1250">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-1251">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1251">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-1252">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1252">Keywords</span></span>

#### <a name="keyword_chile_id_card"></a><span data-ttu-id="b9e4a-1253">Keyword_chile_id_card</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1253">Keyword_chile_id_card</span></span>

- <span data-ttu-id="b9e4a-1254">National Identification Number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1254">National Identification Number</span></span> 
- <span data-ttu-id="b9e4a-1255">Identity card</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1255">Identity card</span></span> 
- <span data-ttu-id="b9e4a-1256">ID</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1256">ID</span></span> 
- <span data-ttu-id="b9e4a-1257">Identificateur</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1257">Identification</span></span> 
- <span data-ttu-id="b9e4a-1258">Rol Único Nacional</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1258">Rol Único Nacional</span></span> 
- <span data-ttu-id="b9e4a-1259">GÉNÉRER</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1259">RUN</span></span> 
- <span data-ttu-id="b9e4a-1260">Rol Único Tributario</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1260">Rol Único Tributario</span></span> 
- <span data-ttu-id="b9e4a-1261">ROUTINE</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1261">RUT</span></span> 
- <span data-ttu-id="b9e4a-1262">Cédula de Identidad</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1262">Cédula de Identidad</span></span> 
- <span data-ttu-id="b9e4a-1263">Número De Identificación Nacional</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1263">Número De Identificación Nacional</span></span> 
- <span data-ttu-id="b9e4a-1264">Tarjeta de identificación</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1264">Tarjeta de identificación</span></span> 
- <span data-ttu-id="b9e4a-1265">Identificación</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1265">Identificación</span></span> 
   
## <a name="china-resident-identity-card-prc-number"></a><span data-ttu-id="b9e4a-1266">	Numéro de carte d’identité de résident Chine (RPC)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1266">China Resident Identity Card (PRC) Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-1267">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1267">Format</span></span>

<span data-ttu-id="b9e4a-1268">18 chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1268">18 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-1269">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1269">Pattern</span></span>

<span data-ttu-id="b9e4a-1270">18 chiffres :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1270">18 digits:</span></span>
- <span data-ttu-id="b9e4a-1271">Six chiffres qui composent un code d’adresse </span><span class="sxs-lookup"><span data-stu-id="b9e4a-1271">Six digits which are an address code</span></span> 
- <span data-ttu-id="b9e4a-1272">Huit chiffres sous la forme AAAAMMJJ qui correspondent à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="b9e4a-1272">Eight digits in the form YYYYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="b9e4a-1273">Trois chiffres qui correspondent à un code d’opération </span><span class="sxs-lookup"><span data-stu-id="b9e4a-1273">Three digits which are an order code</span></span> 
- <span data-ttu-id="b9e4a-1274">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1274">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-1275">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1275">Checksum</span></span>

<span data-ttu-id="b9e4a-1276">Oui</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1276">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-1277">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1277">Definition</span></span>

<span data-ttu-id="b9e4a-1278">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1278">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-1279">La fonction Func_china_resident_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1279">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-1280">Un mot clé figurant dans la liste Keyword_china_resident_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1280">A keyword from Keyword_china_resident_id is found.</span></span>
- <span data-ttu-id="b9e4a-1281">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1281">The checksum passes.</span></span>

<span data-ttu-id="b9e4a-1282">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1282">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-1283">La fonction Func_china_resident_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1283">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-1284">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1284">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-1285">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1285">Keywords</span></span>

### <a name="keyword_china_resident_id"></a><span data-ttu-id="b9e4a-1286">Keyword_china_resident_id</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1286">Keyword_china_resident_id</span></span>

- <span data-ttu-id="b9e4a-1287">Resident Identity Card</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1287">Resident Identity Card</span></span> 
- <span data-ttu-id="b9e4a-1288">FIGURANT</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1288">PRC</span></span> 
- <span data-ttu-id="b9e4a-1289">National Identification Card</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1289">National Identification Card</span></span> 
- <span data-ttu-id="b9e4a-1290">身份证</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1290">身份证</span></span> 
- <span data-ttu-id="b9e4a-1291">居民 身份证</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1291">居民 身份证</span></span> 
- <span data-ttu-id="b9e4a-1292">居民身份证</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1292">居民身份证</span></span> 
- <span data-ttu-id="b9e4a-1293">鉴定</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1293">鉴定</span></span> 
- <span data-ttu-id="b9e4a-1294">身分證</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1294">身分證</span></span> 
- <span data-ttu-id="b9e4a-1295">居民 身份證</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1295">居民 身份證</span></span>
- <span data-ttu-id="b9e4a-1296">鑑定</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1296">鑑定</span></span> 
   
## <a name="credit-card-number"></a><span data-ttu-id="b9e4a-1297">Numéro de carte de crédit</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1297">Credit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-1298">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1298">Format</span></span>

<span data-ttu-id="b9e4a-1299">16 chiffres qui peuvent être mis en forme ou non (dddddddddddddddd) et doivent réussir le test Luhn.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1299">16 digits which can be formatted or unformatted (dddddddddddddddd) and must pass the Luhn test.</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-1300">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1300">Pattern</span></span>

<span data-ttu-id="b9e4a-1301">Modèle très complexe et puissant qui détecte les cartes de visite de toutes les principales marques du monde, notamment Visa, MasterCard, Discover Card, JCB, American Express, etc.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1301">Very complex and robust pattern that detects cards from all major brands worldwide, including Visa, MasterCard, Discover Card, JCB, American Express, gift cards, and diner cards.</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-1302">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1302">Checksum</span></span>

<span data-ttu-id="b9e4a-1303">Oui, la somme de contrôle de Luhn</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1303">Yes, the Luhn checksum</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-1304">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1304">Definition</span></span>

<span data-ttu-id="b9e4a-1305">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1305">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-1306">La fonction Func_credit_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1306">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-1307">L’une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1307">One of the following is true:</span></span>
    - <span data-ttu-id="b9e4a-1308">Un mot clé figurant dans la liste Keyword_cc_verification est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1308">A keyword from Keyword_cc_verification is found.</span></span>
    - <span data-ttu-id="b9e4a-1309">Un mot clé figurant dans la liste Keyword_cc_name est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1309">A keyword from Keyword_cc_name is found.</span></span>
    - <span data-ttu-id="b9e4a-1310">La fonction Func_expiration_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1310">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="b9e4a-1311">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1311">The checksum passes.</span></span>

<span data-ttu-id="b9e4a-1312">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1312">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-1313">La fonction Func_credit_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1313">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-1314">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1314">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-1315">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1315">Keywords</span></span>

#### <a name="keyword_cc_verification"></a><span data-ttu-id="b9e4a-1316">Keyword_cc_verification</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1316">Keyword_cc_verification</span></span>

- <span data-ttu-id="b9e4a-1317">vérification de la carte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1317">card verification</span></span>
- <span data-ttu-id="b9e4a-1318">numéro d’identification de la carte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1318">card identification number</span></span>
- <span data-ttu-id="b9e4a-1319">cryptogramme</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1319">cvn</span></span>
- <span data-ttu-id="b9e4a-1320">nic</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1320">cid</span></span>
- <span data-ttu-id="b9e4a-1321">cvc2</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1321">cvc2</span></span>
- <span data-ttu-id="b9e4a-1322">cvv2</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1322">cvv2</span></span>
- <span data-ttu-id="b9e4a-1323">pin block</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1323">pin block</span></span>
- <span data-ttu-id="b9e4a-1324">code de sécurité</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1324">security code</span></span>
- <span data-ttu-id="b9e4a-1325">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1325">security number</span></span>
- <span data-ttu-id="b9e4a-1326">n° de sécurité</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1326">security no</span></span>
- <span data-ttu-id="b9e4a-1327">numéro d’émission</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1327">issue number</span></span>
- <span data-ttu-id="b9e4a-1328">n° d’émission</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1328">issue no</span></span>
- <span data-ttu-id="b9e4a-1329">cryptogramme</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1329">cryptogramme</span></span>
- <span data-ttu-id="b9e4a-1330">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1330">numéro de sécurité</span></span>
- <span data-ttu-id="b9e4a-1331">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1331">numero de securite</span></span>
- <span data-ttu-id="b9e4a-1332">kreditkartenprüfnummer</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1332">kreditkartenprüfnummer</span></span>
- <span data-ttu-id="b9e4a-1333">kreditkartenprufnummer</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1333">kreditkartenprufnummer</span></span>
- <span data-ttu-id="b9e4a-1334">prüfziffer</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1334">prüfziffer</span></span>
- <span data-ttu-id="b9e4a-1335">prufziffer</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1335">prufziffer</span></span>
- <span data-ttu-id="b9e4a-1336">sicherheits Kode</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1336">sicherheits Kode</span></span>
- <span data-ttu-id="b9e4a-1337">sicherheitscode</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1337">sicherheitscode</span></span>
- <span data-ttu-id="b9e4a-1338">sicherheitsnummer</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1338">sicherheitsnummer</span></span>
- <span data-ttu-id="b9e4a-1339">verfalldatum</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1339">verfalldatum</span></span>
- <span data-ttu-id="b9e4a-1340">codice di verifica</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1340">codice di verifica</span></span>
- <span data-ttu-id="b9e4a-1341">contre.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1341">cod.</span></span> <span data-ttu-id="b9e4a-1342">sicurezza</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1342">sicurezza</span></span>
- <span data-ttu-id="b9e4a-1343">cod sicurezza</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1343">cod sicurezza</span></span>
- <span data-ttu-id="b9e4a-1344">n autorizzazione</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1344">n autorizzazione</span></span>
- <span data-ttu-id="b9e4a-1345">código</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1345">código</span></span>
- <span data-ttu-id="b9e4a-1346">codigo</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1346">codigo</span></span>
- <span data-ttu-id="b9e4a-1347">contre.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1347">cod.</span></span> <span data-ttu-id="b9e4a-1348">SEG</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1348">seg</span></span>
- <span data-ttu-id="b9e4a-1349">cod seg</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1349">cod seg</span></span>
- <span data-ttu-id="b9e4a-1350">código de segurança</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1350">código de segurança</span></span>
- <span data-ttu-id="b9e4a-1351">codigo de seguranca</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1351">codigo de seguranca</span></span>
- <span data-ttu-id="b9e4a-1352">codigo de segurança</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1352">codigo de segurança</span></span>
- <span data-ttu-id="b9e4a-1353">código de seguranca</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1353">código de seguranca</span></span>
- <span data-ttu-id="b9e4a-1354">cód.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1354">cód.</span></span> <span data-ttu-id="b9e4a-1355">segurança</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1355">segurança</span></span>
- <span data-ttu-id="b9e4a-1356">contre.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1356">cod.</span></span> <span data-ttu-id="b9e4a-1357">Seguranca COD.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1357">seguranca cod.</span></span> <span data-ttu-id="b9e4a-1358">segurança</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1358">segurança</span></span>
- <span data-ttu-id="b9e4a-1359">cód.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1359">cód.</span></span> <span data-ttu-id="b9e4a-1360">seguranca</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1360">seguranca</span></span>
- <span data-ttu-id="b9e4a-1361">cód segurança</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1361">cód segurança</span></span>
- <span data-ttu-id="b9e4a-1362">COD Seguranca COD Segurança</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1362">cod seguranca cod segurança</span></span>
- <span data-ttu-id="b9e4a-1363">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1363">cód seguranca</span></span>
- <span data-ttu-id="b9e4a-1364">número de verificação</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1364">número de verificação</span></span>
- <span data-ttu-id="b9e4a-1365">numero de verificacao</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1365">numero de verificacao</span></span>
- <span data-ttu-id="b9e4a-1366">ablauf</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1366">ablauf</span></span>
- <span data-ttu-id="b9e4a-1367">gültig bis</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1367">gültig bis</span></span>
- <span data-ttu-id="b9e4a-1368">gültigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1368">gültigkeitsdatum</span></span>
- <span data-ttu-id="b9e4a-1369">gultig bis</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1369">gultig bis</span></span>
- <span data-ttu-id="b9e4a-1370">gultigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1370">gultigkeitsdatum</span></span>
- <span data-ttu-id="b9e4a-1371">scadenza</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1371">scadenza</span></span>
- <span data-ttu-id="b9e4a-1372">data scad</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1372">data scad</span></span>
- <span data-ttu-id="b9e4a-1373">fecha de expiracion</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1373">fecha de expiracion</span></span>
- <span data-ttu-id="b9e4a-1374">fecha de venc</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1374">fecha de venc</span></span>
- <span data-ttu-id="b9e4a-1375">vencimiento</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1375">vencimiento</span></span>
- <span data-ttu-id="b9e4a-1376">válido hasta</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1376">válido hasta</span></span>
- <span data-ttu-id="b9e4a-1377">valido hasta</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1377">valido hasta</span></span>
- <span data-ttu-id="b9e4a-1378">vto</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1378">vto</span></span>
- <span data-ttu-id="b9e4a-1379">data de expiração</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1379">data de expiração</span></span>
- <span data-ttu-id="b9e4a-1380">data de expiracao</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1380">data de expiracao</span></span>
- <span data-ttu-id="b9e4a-1381">data em que expira</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1381">data em que expira</span></span>
- <span data-ttu-id="b9e4a-1382">validade</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1382">validade</span></span>
- <span data-ttu-id="b9e4a-1383">valorisation</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1383">valor</span></span>
- <span data-ttu-id="b9e4a-1384">vencimento</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1384">vencimento</span></span>
- <span data-ttu-id="b9e4a-1385">Venc</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1385">Venc</span></span> 

#### <a name="keyword_cc_name"></a><span data-ttu-id="b9e4a-1386">Keyword_cc_name</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1386">Keyword_cc_name</span></span>

- <span data-ttu-id="b9e4a-1387">American</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1387">amex</span></span>
- <span data-ttu-id="b9e4a-1388">american express</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1388">american express</span></span>
- <span data-ttu-id="b9e4a-1389">americanexpress</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1389">americanexpress</span></span>
- <span data-ttu-id="b9e4a-1390">Délivrance</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1390">Visa</span></span>
- <span data-ttu-id="b9e4a-1391">MasterCard</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1391">mastercard</span></span>
- <span data-ttu-id="b9e4a-1392">master card</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1392">master card</span></span>
- <span data-ttu-id="b9e4a-1393">McDonald</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1393">mc</span></span> 
- <span data-ttu-id="b9e4a-1394">MasterCard</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1394">mastercards</span></span>
- <span data-ttu-id="b9e4a-1395">master cards</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1395">master cards</span></span>
- <span data-ttu-id="b9e4a-1396">diner’s Club</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1396">diner's Club</span></span>
- <span data-ttu-id="b9e4a-1397">diners club</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1397">diners club</span></span>
- <span data-ttu-id="b9e4a-1398">dinersclub</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1398">dinersclub</span></span>
- <span data-ttu-id="b9e4a-1399">discover card</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1399">discover card</span></span>
- <span data-ttu-id="b9e4a-1400">discovercard</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1400">discovercard</span></span>
- <span data-ttu-id="b9e4a-1401">discover cards</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1401">discover cards</span></span>
- <span data-ttu-id="b9e4a-1402">JCB</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1402">JCB</span></span>
- <span data-ttu-id="b9e4a-1403">japanese card bureau</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1403">japanese card bureau</span></span>
- <span data-ttu-id="b9e4a-1404">carte blanche</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1404">carte blanche</span></span>
- <span data-ttu-id="b9e4a-1405">carteblanche</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1405">carteblanche</span></span>
- <span data-ttu-id="b9e4a-1406">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1406">credit card</span></span>
- <span data-ttu-id="b9e4a-1407">CC #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1407">cc#</span></span>
- <span data-ttu-id="b9e4a-1408">n ° de CC:</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1408">cc#:</span></span>
- <span data-ttu-id="b9e4a-1409">date d’expiration</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1409">expiration date</span></span>
- <span data-ttu-id="b9e4a-1410">date d’exp</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1410">exp date</span></span>
- <span data-ttu-id="b9e4a-1411">date d’expiration</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1411">expiry date</span></span>
- <span data-ttu-id="b9e4a-1412">date d’expiration</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1412">date d’expiration</span></span>
- <span data-ttu-id="b9e4a-1413">date d’exp</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1413">date d'exp</span></span>
- <span data-ttu-id="b9e4a-1414">date expiration</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1414">date expiration</span></span>
- <span data-ttu-id="b9e4a-1415">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1415">bank card</span></span>
- <span data-ttu-id="b9e4a-1416">bankcard</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1416">bankcard</span></span>
- <span data-ttu-id="b9e4a-1417">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1417">card number</span></span>
- <span data-ttu-id="b9e4a-1418">num de carte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1418">card num</span></span>
- <span data-ttu-id="b9e4a-1419">carte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1419">cardnumber</span></span>
- <span data-ttu-id="b9e4a-1420">carte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1420">cardnumbers</span></span>
- <span data-ttu-id="b9e4a-1421">numéros de carte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1421">card numbers</span></span>
- <span data-ttu-id="b9e4a-1422">CreditCard</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1422">creditcard</span></span>
- <span data-ttu-id="b9e4a-1423">cartes de crédit</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1423">credit cards</span></span>
- <span data-ttu-id="b9e4a-1424">crédit</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1424">creditcards</span></span>
- <span data-ttu-id="b9e4a-1425">CCN</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1425">ccn</span></span>
- <span data-ttu-id="b9e4a-1426">titulaire de la carte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1426">card holder</span></span>
- <span data-ttu-id="b9e4a-1427">titulaires</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1427">cardholder</span></span>
- <span data-ttu-id="b9e4a-1428">titulaires de la carte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1428">card holders</span></span>
- <span data-ttu-id="b9e4a-1429">titulaires</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1429">cardholders</span></span>
- <span data-ttu-id="b9e4a-1430">carte de vérification</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1430">check card</span></span>
- <span data-ttu-id="b9e4a-1431">carte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1431">checkcard</span></span>
- <span data-ttu-id="b9e4a-1432">cartes de vérification</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1432">check cards</span></span>
- <span data-ttu-id="b9e4a-1433">cartes</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1433">checkcards</span></span>
- <span data-ttu-id="b9e4a-1434">carte de débit</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1434">debit card</span></span>
- <span data-ttu-id="b9e4a-1435">débit</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1435">debitcard</span></span>
- <span data-ttu-id="b9e4a-1436">cartes de débit</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1436">debit cards</span></span>
- <span data-ttu-id="b9e4a-1437">débit</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1437">debitcards</span></span>
- <span data-ttu-id="b9e4a-1438">carte de retrait</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1438">atm card</span></span>
- <span data-ttu-id="b9e4a-1439">retrait</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1439">atmcard</span></span>
- <span data-ttu-id="b9e4a-1440">cartes de retrait</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1440">atm cards</span></span>
- <span data-ttu-id="b9e4a-1441">retrait</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1441">atmcards</span></span>
- <span data-ttu-id="b9e4a-1442">envoier</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1442">enroute</span></span>
- <span data-ttu-id="b9e4a-1443">en route</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1443">en route</span></span>
- <span data-ttu-id="b9e4a-1444">type de carte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1444">card type</span></span>
- <span data-ttu-id="b9e4a-1445">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1445">carte bancaire</span></span>
- <span data-ttu-id="b9e4a-1446">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1446">carte de crédit</span></span>
- <span data-ttu-id="b9e4a-1447">carte de credit</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1447">carte de credit</span></span>
- <span data-ttu-id="b9e4a-1448">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1448">numéro de carte</span></span>
- <span data-ttu-id="b9e4a-1449">numero de carte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1449">numero de carte</span></span>
- <span data-ttu-id="b9e4a-1450">nº de la carte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1450">nº de la carte</span></span>
- <span data-ttu-id="b9e4a-1451">nº de carte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1451">nº de carte</span></span>
- <span data-ttu-id="b9e4a-1452">kreditkarte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1452">kreditkarte</span></span>
- <span data-ttu-id="b9e4a-1453">karte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1453">karte</span></span>
- <span data-ttu-id="b9e4a-1454">karteninhaber</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1454">karteninhaber</span></span>
- <span data-ttu-id="b9e4a-1455">karteninhabers</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1455">karteninhabers</span></span>
- <span data-ttu-id="b9e4a-1456">kreditkarteninhaber</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1456">kreditkarteninhaber</span></span>
- <span data-ttu-id="b9e4a-1457">kreditkarteninstitut</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1457">kreditkarteninstitut</span></span>
- <span data-ttu-id="b9e4a-1458">kreditkartentyp</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1458">kreditkartentyp</span></span>
- <span data-ttu-id="b9e4a-1459">eigentümername</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1459">eigentümername</span></span>
- <span data-ttu-id="b9e4a-1460">kartennr</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1460">kartennr</span></span> 
- <span data-ttu-id="b9e4a-1461">kartennummer</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1461">kartennummer</span></span>
- <span data-ttu-id="b9e4a-1462">kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1462">kreditkartennummer</span></span>
- <span data-ttu-id="b9e4a-1463">kreditkarten-nummer</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1463">kreditkarten-nummer</span></span>
- <span data-ttu-id="b9e4a-1464">Carta di credito</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1464">carta di credito</span></span>
- <span data-ttu-id="b9e4a-1465">Carta credito</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1465">carta credito</span></span>
- <span data-ttu-id="b9e4a-1466">Carta</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1466">carta</span></span>
- <span data-ttu-id="b9e4a-1467">n carta</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1467">n carta</span></span>
- <span data-ttu-id="b9e4a-1468">Nr.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1468">nr.</span></span> <span data-ttu-id="b9e4a-1469">Carta</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1469">carta</span></span>
- <span data-ttu-id="b9e4a-1470">nr carta</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1470">nr carta</span></span>
- <span data-ttu-id="b9e4a-1471">numero carta</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1471">numero carta</span></span>
- <span data-ttu-id="b9e4a-1472">numero della carta</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1472">numero della carta</span></span>
- <span data-ttu-id="b9e4a-1473">numero di carta</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1473">numero di carta</span></span>
- <span data-ttu-id="b9e4a-1474">tarjeta credito</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1474">tarjeta credito</span></span>
- <span data-ttu-id="b9e4a-1475">tarjeta de credito</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1475">tarjeta de credito</span></span>
- <span data-ttu-id="b9e4a-1476">tarjeta crédito</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1476">tarjeta crédito</span></span>
- <span data-ttu-id="b9e4a-1477">tarjeta de crédito</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1477">tarjeta de crédito</span></span>
- <span data-ttu-id="b9e4a-1478">tarjeta de atm</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1478">tarjeta de atm</span></span>
- <span data-ttu-id="b9e4a-1479">tarjeta atm</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1479">tarjeta atm</span></span>
- <span data-ttu-id="b9e4a-1480">tarjeta debito</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1480">tarjeta debito</span></span>
- <span data-ttu-id="b9e4a-1481">tarjeta de debito</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1481">tarjeta de debito</span></span>
- <span data-ttu-id="b9e4a-1482">tarjeta débito</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1482">tarjeta débito</span></span>
- <span data-ttu-id="b9e4a-1483">tarjeta de débito</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1483">tarjeta de débito</span></span>
- <span data-ttu-id="b9e4a-1484">nº de tarjeta</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1484">nº de tarjeta</span></span>
- <span data-ttu-id="b9e4a-1485">Nbre.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1485">no.</span></span> <span data-ttu-id="b9e4a-1486">de tarjeta</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1486">de tarjeta</span></span>
- <span data-ttu-id="b9e4a-1487">no de tarjeta</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1487">no de tarjeta</span></span>
- <span data-ttu-id="b9e4a-1488">numero de tarjeta</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1488">numero de tarjeta</span></span>
- <span data-ttu-id="b9e4a-1489">número de tarjeta</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1489">número de tarjeta</span></span>
- <span data-ttu-id="b9e4a-1490">tarjeta no</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1490">tarjeta no</span></span>
- <span data-ttu-id="b9e4a-1491">tarjetahabiente</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1491">tarjetahabiente</span></span>
- <span data-ttu-id="b9e4a-1492">cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1492">cartão de crédito</span></span>
- <span data-ttu-id="b9e4a-1493">cartão de credito</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1493">cartão de credito</span></span>
- <span data-ttu-id="b9e4a-1494">cartao de crédito</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1494">cartao de crédito</span></span>
- <span data-ttu-id="b9e4a-1495">cartao de credito</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1495">cartao de credito</span></span>
- <span data-ttu-id="b9e4a-1496">cartão de débito</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1496">cartão de débito</span></span>
- <span data-ttu-id="b9e4a-1497">cartao de débito</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1497">cartao de débito</span></span>
- <span data-ttu-id="b9e4a-1498">cartão de debito</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1498">cartão de debito</span></span>
- <span data-ttu-id="b9e4a-1499">cartao de debito</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1499">cartao de debito</span></span>
- <span data-ttu-id="b9e4a-1500">débito automático</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1500">débito automático</span></span>
- <span data-ttu-id="b9e4a-1501">debito automatico</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1501">debito automatico</span></span>
- <span data-ttu-id="b9e4a-1502">número do cartão</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1502">número do cartão</span></span>
- <span data-ttu-id="b9e4a-1503">numero do cartão</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1503">numero do cartão</span></span> 
- <span data-ttu-id="b9e4a-1504">número do cartao</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1504">número do cartao</span></span>
- <span data-ttu-id="b9e4a-1505">numero do cartao</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1505">numero do cartao</span></span>
- <span data-ttu-id="b9e4a-1506">número de cartão</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1506">número de cartão</span></span>
- <span data-ttu-id="b9e4a-1507">numero de cartão</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1507">numero de cartão</span></span>
- <span data-ttu-id="b9e4a-1508">número de cartao</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1508">número de cartao</span></span>
- <span data-ttu-id="b9e4a-1509">numero de cartao</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1509">numero de cartao</span></span>
- <span data-ttu-id="b9e4a-1510">nº do cartão</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1510">nº do cartão</span></span>
- <span data-ttu-id="b9e4a-1511">nº do cartao</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1511">nº do cartao</span></span>
- <span data-ttu-id="b9e4a-1512">n º.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1512">nº.</span></span> <span data-ttu-id="b9e4a-1513">do cartão</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1513">do cartão</span></span>
- <span data-ttu-id="b9e4a-1514">no do cartão</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1514">no do cartão</span></span>
- <span data-ttu-id="b9e4a-1515">no do cartao</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1515">no do cartao</span></span>
- <span data-ttu-id="b9e4a-1516">Nbre.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1516">no.</span></span> <span data-ttu-id="b9e4a-1517">do cartão</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1517">do cartão</span></span>
- <span data-ttu-id="b9e4a-1518">Nbre.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1518">no.</span></span> <span data-ttu-id="b9e4a-1519">do cartao</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1519">do cartao</span></span> 
   
## <a name="croatia-identity-card-number"></a><span data-ttu-id="b9e4a-1520">	Numéro de carte d’identité Croatie</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1520">Croatia Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-1521">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1521">Format</span></span>

<span data-ttu-id="b9e4a-1522">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1522">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-1523">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1523">Pattern</span></span>

<span data-ttu-id="b9e4a-1524">Neuf chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1524">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-1525">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1525">Checksum</span></span>

<span data-ttu-id="b9e4a-1526">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1526">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-1527">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1527">Definition</span></span>

<span data-ttu-id="b9e4a-1528">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1528">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-1529">La fonction Func_croatia_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1529">The function Func_croatia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-1530">Un mot clé figurant dans la liste Keyword_croatia_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1530">A keyword from Keyword_croatia_id_card is found.</span></span>

```
<!--Croatia Identity Card Number-->
<Entity id="ff12f884-c20a-4189-b185-34c8e7258d47" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_croatia_id_card"/>
     <Match idRef="Keyword_croatia_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b9e4a-1531">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1531">Keywords</span></span>

#### <a name="keyword_croatia_id_card"></a><span data-ttu-id="b9e4a-1532">Keyword_croatia_id_card</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1532">Keyword_croatia_id_card</span></span>

- <span data-ttu-id="b9e4a-1533">Croatian identity card</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1533">Croatian identity card</span></span>
- <span data-ttu-id="b9e4a-1534">Osobna iskaznica</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1534">Osobna iskaznica</span></span>

   
## <a name="croatia-personal-identification-oib-number"></a><span data-ttu-id="b9e4a-1535">	Numéro d’identification personnel (OIB) Croatie</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1535">Croatia Personal Identification (OIB) Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-1536">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1536">Format</span></span>

<span data-ttu-id="b9e4a-1537">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1537">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-1538">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1538">Pattern</span></span>

<span data-ttu-id="b9e4a-1539">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1539">11 digits:</span></span>
- <span data-ttu-id="b9e4a-1540">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1540">10 digits</span></span> 
- <span data-ttu-id="b9e4a-1541">Le chiffre final est un chiffre de contrôle aux fins de l’échange de données internationales, les lettres HR sont ajoutées avant les onze chiffres.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1541">Final digit is a check digit For the purposes of international data exchange, the letters HR are added preceding the eleven digits.</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-1542">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1542">Checksum</span></span>

<span data-ttu-id="b9e4a-1543">Oui</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1543">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-1544">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1544">Definition</span></span>

<span data-ttu-id="b9e4a-1545">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1545">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-1546">La fonction Func_croatia_oib_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1546">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-1547">Un mot clé figurant dans la liste Keyword_croatia_oib_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1547">A keyword from Keyword_croatia_oib_number is found.</span></span>
- <span data-ttu-id="b9e4a-1548">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1548">The checksum passes.</span></span>

<span data-ttu-id="b9e4a-1549">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1549">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-1550">La fonction Func_croatia_oib_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1550">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-1551">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1551">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-1552">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1552">Keywords</span></span>

#### <a name="keyword_croatia_oib_number"></a><span data-ttu-id="b9e4a-1553">Keyword_croatia_oib_number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1553">Keyword_croatia_oib_number</span></span>

- <span data-ttu-id="b9e4a-1554">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1554">Personal Identification Number</span></span>
- <span data-ttu-id="b9e4a-1555">Osobni identifikacijski broj</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1555">Osobni identifikacijski broj</span></span> 
- <span data-ttu-id="b9e4a-1556">OIB</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1556">OIB</span></span> 

   
## <a name="czech-personal-identity-number"></a><span data-ttu-id="b9e4a-1557">Numéro d’identité personnelle tchèque</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1557">Czech Personal Identity Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-1558">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1558">Format</span></span>

<span data-ttu-id="b9e4a-1559">Neuf chiffres avec une barre oblique inverse facultative (ancien format) 10 chiffres avec une barre oblique facultative (nouveau format)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1559">Nine digits with optional forward slash (old format) 10 digits with optional forward slash (new format)</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-1560">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1560">Pattern</span></span>

<span data-ttu-id="b9e4a-1561">Neuf chiffres (ancien format):</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1561">Nine digits (old format):</span></span>
- <span data-ttu-id="b9e4a-1562">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1562">Nine digits</span></span>

<span data-ttu-id="b9e4a-1563">OR</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1563">OR</span></span>

- <span data-ttu-id="b9e4a-1564">Six chiffres qui représentent la date de naissance</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1564">Six digits that represent date of birth</span></span>
- <span data-ttu-id="b9e4a-1565">Une barre oblique </span><span class="sxs-lookup"><span data-stu-id="b9e4a-1565">A forward slash</span></span>
- <span data-ttu-id="b9e4a-1566">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1566">Three digits</span></span>

<span data-ttu-id="b9e4a-1567">10 chiffres (nouveau format):</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1567">10 digits (new format):</span></span>
- <span data-ttu-id="b9e4a-1568">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1568">10 digits</span></span>

<span data-ttu-id="b9e4a-1569">OR</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1569">OR</span></span>

- <span data-ttu-id="b9e4a-1570">Six chiffres qui représentent la date de naissance</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1570">Six digits that represent date of birth</span></span>
- <span data-ttu-id="b9e4a-1571">Une barre oblique </span><span class="sxs-lookup"><span data-stu-id="b9e4a-1571">A forward slash</span></span> 
- <span data-ttu-id="b9e4a-1572">Quatre chiffres où le dernier chiffre est un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1572">Four digits where last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-1573">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1573">Checksum</span></span>

<span data-ttu-id="b9e4a-1574">Oui</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1574">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-1575">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1575">Definition</span></span>

<span data-ttu-id="b9e4a-1576">Une stratégie DLP est sûre à 85% d’avoir détecté ce type d’informations sensibles si, dans une proximité de 300 caractères: la fonction Func_czech_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1576">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_czech_id_card finds content that matches the pattern.</span></span>
<span data-ttu-id="b9e4a-1577">Un mot clé figurant dans la liste Keyword_czech_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1577">A keyword from Keyword_czech_id_card is found.</span></span>
<span data-ttu-id="b9e4a-1578">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1578">The checksum passes.</span></span>

```
<!-- Czech Personal Identity Number -->
<Entity id="60c0725a-4eb6-455b-9dda-05d8a7396497"      patternsProximity="300" recommendedConfidence="85">
   <Pattern confidenceLevel="85">
      <IdMatch idRef="Func_czech_id_card" />
      <Match idRef="Keyword_czech_id_card" />
   </Pattern>
</Entity>
```
### <a name="keywords"></a><span data-ttu-id="b9e4a-1579">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1579">Keywords</span></span>

- <span data-ttu-id="b9e4a-1580">Numéro d’identité personnelle tchèque</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1580">czech personal identity number</span></span>
- <span data-ttu-id="b9e4a-1581">Rodné číslo</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1581">Rodné číslo</span></span>
   
## <a name="denmark-personal-identification-number"></a><span data-ttu-id="b9e4a-1582">	Numéro d’identification personnel Danemark</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1582">Denmark Personal Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-1583">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1583">Format</span></span>

<span data-ttu-id="b9e4a-1584">10 chiffres contenant un trait d’union</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1584">10 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-1585">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1585">Pattern</span></span>

<span data-ttu-id="b9e4a-1586">10 chiffres :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1586">10 digits:</span></span>
- <span data-ttu-id="b9e4a-1587">Six chiffres au format JJMMAA qui correspondent à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="b9e4a-1587">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="b9e4a-1588">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="b9e4a-1588">A hyphen</span></span> 
- <span data-ttu-id="b9e4a-1589">Quatre chiffres où le dernier chiffre est un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1589">Four digits where the final digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-1590">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1590">Checksum</span></span>

<span data-ttu-id="b9e4a-1591">Oui</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1591">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-1592">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1592">Definition</span></span>

<span data-ttu-id="b9e4a-1593">Une stratégie DLP est sûre à 75% d’avoir détecté ce type d’informations sensibles si, dans une proximité de 300 caractères: l’expression régulière Regex_denmark_id trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1593">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_denmark_id finds content that matches the pattern.</span></span>
<span data-ttu-id="b9e4a-1594">Un mot clé figurant dans la liste Keyword_denmark_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1594">A keyword from Keyword_denmark_id is found.</span></span>
<span data-ttu-id="b9e4a-1595">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1595">The checksum passes.</span></span>

```
<!-- Denmark Personal Identification Number -->
<Entity id="6c4f2fef-56e1-4c00-8093-88d7a01cf460" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_denmark_id"/>
     <Match idRef="Keyword_denmark_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b9e4a-1596">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1596">Keywords</span></span>

#### <a name="keyword_denmark_id"></a><span data-ttu-id="b9e4a-1597">Keyword_denmark_id</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1597">Keyword_denmark_id</span></span>

- <span data-ttu-id="b9e4a-1598">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1598">Personal Identification Number</span></span>
- <span data-ttu-id="b9e4a-1599">CARDIO</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1599">CPR</span></span>
- <span data-ttu-id="b9e4a-1600">Det Centrale Personregister</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1600">Det Centrale Personregister</span></span>
- <span data-ttu-id="b9e4a-1601">Personnummer</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1601">Personnummer</span></span>
   
## <a name="drug-enforcement-agency-dea-number"></a><span data-ttu-id="b9e4a-1602">Numéro de la Drug Enforcement Agency (DEA)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1602">Drug Enforcement Agency (DEA) Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-1603">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1603">Format</span></span>

<span data-ttu-id="b9e4a-1604">Deux lettres suivies de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1604">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-1605">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1605">Pattern</span></span>

<span data-ttu-id="b9e4a-1606">Le modèle doit inclure tous les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1606">Pattern must include all of the following:</span></span>
- <span data-ttu-id="b9e4a-1607">Une lettre (ne respecte pas la casse) à partir de cet ensemble de lettres possibles : abcdefghjklmnprstux, qui est un code d’utilisateur enregistré</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1607">One letter (not case sensitive) from this set of possible letters: abcdefghjklmnprstux, which is a registrant code</span></span> 
- <span data-ttu-id="b9e4a-1608">Une lettre (ne respecte pas la casse), qui est la première lettre du nom de l’utilisateur enregistré</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1608">One letter (not case sensitive), which is the first letter of the registrant's last name</span></span> 
- <span data-ttu-id="b9e4a-1609">Sept chiffres, le dernier est le chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1609">Seven digits, the last of which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-1610">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1610">Checksum</span></span>

<span data-ttu-id="b9e4a-1611">Oui</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1611">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-1612">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1612">Definition</span></span>

<span data-ttu-id="b9e4a-1613">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1613">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-1614">La fonction Func_dea_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1614">The function Func_dea_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-1615">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1615">The checksum passes.</span></span>

```
<!-- DEA Number -->
<Entity id="9a5445ad-406e-43eb-8bd7-cac17ab6d0e4" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_dea_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b9e4a-1616">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1616">Keywords</span></span>

<span data-ttu-id="b9e4a-1617">Aucun</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1617">None</span></span>

   
## <a name="eu-debit-card-number"></a><span data-ttu-id="b9e4a-1618">Numéro de carte de débit Union européenne</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1618">EU Debit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-1619">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1619">Format</span></span>

<span data-ttu-id="b9e4a-1620">16 chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1620">16 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-1621">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1621">Pattern</span></span>

<span data-ttu-id="b9e4a-1622">Modèle très complexe et puissant</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1622">Very complex and robust pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-1623">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1623">Checksum</span></span>

<span data-ttu-id="b9e4a-1624">Oui</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1624">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-1625">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1625">Definition</span></span>

<span data-ttu-id="b9e4a-1626">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1626">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-1627">La fonction Func_eu_debit_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1627">The function Func_eu_debit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-1628">Au moins une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1628">At least one of the following is true:</span></span>
    - <span data-ttu-id="b9e4a-1629">Un mot clé figurant dans la liste Keyword_eu_debit_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1629">A keyword from Keyword_eu_debit_card is found.</span></span>
    - <span data-ttu-id="b9e4a-1630">Un mot clé figurant dans la liste Keyword_card_terms_dict est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1630">A keyword from Keyword_card_terms_dict is found.</span></span>
    - <span data-ttu-id="b9e4a-1631">Un mot clé figurant dans la liste Keyword_card_security_terms_dict est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1631">A keyword from Keyword_card_security_terms_dict is found.</span></span>
    - <span data-ttu-id="b9e4a-1632">Un mot clé figurant dans la liste Keyword_card_expiration_terms_dict est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1632">A keyword from Keyword_card_expiration_terms_dict is found.</span></span>
    - <span data-ttu-id="b9e4a-1633">La fonction Func_expiration_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1633">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="b9e4a-1634">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1634">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-1635">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1635">Keywords</span></span>

#### <a name="keyword_eu_debit_card"></a><span data-ttu-id="b9e4a-1636">Keyword_eu_debit_card</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1636">Keyword_eu_debit_card</span></span>

- <span data-ttu-id="b9e4a-1637">numéro de compte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1637">account number</span></span> 
- <span data-ttu-id="b9e4a-1638">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1638">card number</span></span> 
- <span data-ttu-id="b9e4a-1639">n° carte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1639">card no.</span></span> 
- <span data-ttu-id="b9e4a-1640">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1640">security number</span></span> 
- <span data-ttu-id="b9e4a-1641">CC #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1641">cc#</span></span> 

#### <a name="keyword_card_terms_dict"></a><span data-ttu-id="b9e4a-1642">Keyword_card_terms_dict</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1642">Keyword_card_terms_dict</span></span>

- <span data-ttu-id="b9e4a-1643">num de compte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1643">acct nbr</span></span> 
- <span data-ttu-id="b9e4a-1644">num de compte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1644">acct num</span></span> 
- <span data-ttu-id="b9e4a-1645">n° compte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1645">acct no</span></span> 
- <span data-ttu-id="b9e4a-1646">american express</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1646">american express</span></span> 
- <span data-ttu-id="b9e4a-1647">americanexpress</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1647">americanexpress</span></span> 
- <span data-ttu-id="b9e4a-1648">americano espresso</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1648">americano espresso</span></span> 
- <span data-ttu-id="b9e4a-1649">American</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1649">amex</span></span> 
- <span data-ttu-id="b9e4a-1650">carte de retrait</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1650">atm card</span></span> 
- <span data-ttu-id="b9e4a-1651">cartes de retrait</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1651">atm cards</span></span> 
- <span data-ttu-id="b9e4a-1652">atm kaart</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1652">atm kaart</span></span> 
- <span data-ttu-id="b9e4a-1653">retrait</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1653">atmcard</span></span> 
- <span data-ttu-id="b9e4a-1654">retrait</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1654">atmcards</span></span> 
- <span data-ttu-id="b9e4a-1655">atmkaart</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1655">atmkaart</span></span> 
- <span data-ttu-id="b9e4a-1656">atmkaarten</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1656">atmkaarten</span></span> 
- <span data-ttu-id="b9e4a-1657">bancontact</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1657">bancontact</span></span> 
- <span data-ttu-id="b9e4a-1658">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1658">bank card</span></span> 
- <span data-ttu-id="b9e4a-1659">bankkaart</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1659">bankkaart</span></span> 
- <span data-ttu-id="b9e4a-1660">titulaire de la carte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1660">card holder</span></span> 
- <span data-ttu-id="b9e4a-1661">titulaires de la carte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1661">card holders</span></span> 
- <span data-ttu-id="b9e4a-1662">num de carte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1662">card num</span></span> 
- <span data-ttu-id="b9e4a-1663">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1663">card number</span></span> 
- <span data-ttu-id="b9e4a-1664">numéros de carte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1664">card numbers</span></span> 
- <span data-ttu-id="b9e4a-1665">type de carte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1665">card type</span></span> 
- <span data-ttu-id="b9e4a-1666">cardano numerico</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1666">cardano numerico</span></span> 
- <span data-ttu-id="b9e4a-1667">titulaires</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1667">cardholder</span></span> 
- <span data-ttu-id="b9e4a-1668">titulaires</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1668">cardholders</span></span> 
- <span data-ttu-id="b9e4a-1669">carte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1669">cardnumber</span></span> 
- <span data-ttu-id="b9e4a-1670">carte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1670">cardnumbers</span></span> 
- <span data-ttu-id="b9e4a-1671">carta bianca</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1671">carta bianca</span></span> 
- <span data-ttu-id="b9e4a-1672">Carta credito</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1672">carta credito</span></span> 
- <span data-ttu-id="b9e4a-1673">Carta di credito</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1673">carta di credito</span></span> 
- <span data-ttu-id="b9e4a-1674">cartao de credito</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1674">cartao de credito</span></span> 
- <span data-ttu-id="b9e4a-1675">cartao de crédito</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1675">cartao de crédito</span></span> 
- <span data-ttu-id="b9e4a-1676">cartao de debito</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1676">cartao de debito</span></span> 
- <span data-ttu-id="b9e4a-1677">cartao de débito</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1677">cartao de débito</span></span> 
- <span data-ttu-id="b9e4a-1678">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1678">carte bancaire</span></span> 
- <span data-ttu-id="b9e4a-1679">carte blanche</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1679">carte blanche</span></span> 
- <span data-ttu-id="b9e4a-1680">carte bleue</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1680">carte bleue</span></span> 
- <span data-ttu-id="b9e4a-1681">carte de credit</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1681">carte de credit</span></span> 
- <span data-ttu-id="b9e4a-1682">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1682">carte de crédit</span></span> 
- <span data-ttu-id="b9e4a-1683">carte di credito</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1683">carte di credito</span></span> 
- <span data-ttu-id="b9e4a-1684">carteblanche</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1684">carteblanche</span></span> 
- <span data-ttu-id="b9e4a-1685">cartão de credito</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1685">cartão de credito</span></span> 
- <span data-ttu-id="b9e4a-1686">cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1686">cartão de crédito</span></span> 
- <span data-ttu-id="b9e4a-1687">cartão de debito</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1687">cartão de debito</span></span> 
- <span data-ttu-id="b9e4a-1688">cartão de débito</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1688">cartão de débito</span></span> 
- <span data-ttu-id="b9e4a-1689">cb</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1689">cb</span></span> 
- <span data-ttu-id="b9e4a-1690">CCN</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1690">ccn</span></span> 
- <span data-ttu-id="b9e4a-1691">carte de vérification</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1691">check card</span></span> 
- <span data-ttu-id="b9e4a-1692">cartes de vérification</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1692">check cards</span></span> 
- <span data-ttu-id="b9e4a-1693">carte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1693">checkcard</span></span>
- <span data-ttu-id="b9e4a-1694">cartes</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1694">checkcards</span></span> 
- <span data-ttu-id="b9e4a-1695">chequekaart</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1695">chequekaart</span></span> 
- <span data-ttu-id="b9e4a-1696">Cirrus</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1696">cirrus</span></span> 
- <span data-ttu-id="b9e4a-1697">Cirrus-EDC-Maestro</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1697">cirrus-edc-maestro</span></span> 
- <span data-ttu-id="b9e4a-1698">controlekaart</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1698">controlekaart</span></span> 
- <span data-ttu-id="b9e4a-1699">controlekaarten</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1699">controlekaarten</span></span> 
- <span data-ttu-id="b9e4a-1700">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1700">credit card</span></span> 
- <span data-ttu-id="b9e4a-1701">cartes de crédit</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1701">credit cards</span></span> 
- <span data-ttu-id="b9e4a-1702">CreditCard</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1702">creditcard</span></span> 
- <span data-ttu-id="b9e4a-1703">crédit</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1703">creditcards</span></span> 
- <span data-ttu-id="b9e4a-1704">debetkaart</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1704">debetkaart</span></span> 
- <span data-ttu-id="b9e4a-1705">debetkaarten</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1705">debetkaarten</span></span> 
- <span data-ttu-id="b9e4a-1706">carte de débit</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1706">debit card</span></span> 
- <span data-ttu-id="b9e4a-1707">cartes de débit</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1707">debit cards</span></span> 
- <span data-ttu-id="b9e4a-1708">débit</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1708">debitcard</span></span> 
- <span data-ttu-id="b9e4a-1709">débit</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1709">debitcards</span></span> 
- <span data-ttu-id="b9e4a-1710">debito automatico</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1710">debito automatico</span></span> 
- <span data-ttu-id="b9e4a-1711">diners club</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1711">diners club</span></span> 
- <span data-ttu-id="b9e4a-1712">dinersclub</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1712">dinersclub</span></span> 
- <span data-ttu-id="b9e4a-1713">connaissance</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1713">discover</span></span> 
- <span data-ttu-id="b9e4a-1714">discover card</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1714">discover card</span></span> 
- <span data-ttu-id="b9e4a-1715">discover cards</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1715">discover cards</span></span> 
- <span data-ttu-id="b9e4a-1716">discovercard</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1716">discovercard</span></span> 
- <span data-ttu-id="b9e4a-1717">discovercards</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1717">discovercards</span></span> 
- <span data-ttu-id="b9e4a-1718">débito automático</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1718">débito automático</span></span>
- <span data-ttu-id="b9e4a-1719">EDC</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1719">edc</span></span> 
- <span data-ttu-id="b9e4a-1720">eigentümername</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1720">eigentümername</span></span> 
- <span data-ttu-id="b9e4a-1721">carte de crédit européenne</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1721">european debit card</span></span> 
- <span data-ttu-id="b9e4a-1722">hoofdkaart</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1722">hoofdkaart</span></span> 
- <span data-ttu-id="b9e4a-1723">hoofdkaarten</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1723">hoofdkaarten</span></span> 
- <span data-ttu-id="b9e4a-1724">in viaggio</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1724">in viaggio</span></span> 
- <span data-ttu-id="b9e4a-1725">japanese card bureau</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1725">japanese card bureau</span></span> 
- <span data-ttu-id="b9e4a-1726">japanse kaartdienst</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1726">japanse kaartdienst</span></span> 
- <span data-ttu-id="b9e4a-1727">JCB</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1727">jcb</span></span> 
- <span data-ttu-id="b9e4a-1728">kaart</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1728">kaart</span></span> 
- <span data-ttu-id="b9e4a-1729">kaart num</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1729">kaart num</span></span> 
- <span data-ttu-id="b9e4a-1730">kaartaantal</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1730">kaartaantal</span></span> 
- <span data-ttu-id="b9e4a-1731">kaartaantallen</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1731">kaartaantallen</span></span> 
- <span data-ttu-id="b9e4a-1732">kaarthouder</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1732">kaarthouder</span></span> 
- <span data-ttu-id="b9e4a-1733">kaarthouders</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1733">kaarthouders</span></span> 
- <span data-ttu-id="b9e4a-1734">karte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1734">karte</span></span>  
- <span data-ttu-id="b9e4a-1735">karteninhaber</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1735">karteninhaber</span></span> 
- <span data-ttu-id="b9e4a-1736">karteninhabers</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1736">karteninhabers</span></span>
- <span data-ttu-id="b9e4a-1737">kartennr</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1737">kartennr</span></span> 
- <span data-ttu-id="b9e4a-1738">kartennummer</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1738">kartennummer</span></span> 
- <span data-ttu-id="b9e4a-1739">kreditkarte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1739">kreditkarte</span></span> 
- <span data-ttu-id="b9e4a-1740">kreditkarten-nummer</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1740">kreditkarten-nummer</span></span> 
- <span data-ttu-id="b9e4a-1741">kreditkarteninhaber</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1741">kreditkarteninhaber</span></span> 
- <span data-ttu-id="b9e4a-1742">kreditkarteninstitut</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1742">kreditkarteninstitut</span></span> 
- <span data-ttu-id="b9e4a-1743">kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1743">kreditkartennummer</span></span> 
- <span data-ttu-id="b9e4a-1744">kreditkartentyp</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1744">kreditkartentyp</span></span> 
- <span data-ttu-id="b9e4a-1745">sonne</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1745">maestro</span></span> 
- <span data-ttu-id="b9e4a-1746">master card</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1746">master card</span></span> 
- <span data-ttu-id="b9e4a-1747">master cards</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1747">master cards</span></span> 
- <span data-ttu-id="b9e4a-1748">MasterCard</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1748">mastercard</span></span> 
- <span data-ttu-id="b9e4a-1749">MasterCard</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1749">mastercards</span></span> 
- <span data-ttu-id="b9e4a-1750">McDonald</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1750">mc</span></span> 
- <span data-ttu-id="b9e4a-1751">mister cash</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1751">mister cash</span></span> 
- <span data-ttu-id="b9e4a-1752">n carta</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1752">n carta</span></span> 
- <span data-ttu-id="b9e4a-1753">Carta</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1753">carta</span></span> 
- <span data-ttu-id="b9e4a-1754">no de tarjeta</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1754">no de tarjeta</span></span> 
- <span data-ttu-id="b9e4a-1755">no do cartao</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1755">no do cartao</span></span> 
- <span data-ttu-id="b9e4a-1756">no do cartão</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1756">no do cartão</span></span> 
- <span data-ttu-id="b9e4a-1757">Nbre.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1757">no.</span></span> <span data-ttu-id="b9e4a-1758">de tarjeta</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1758">de tarjeta</span></span> 
- <span data-ttu-id="b9e4a-1759">Nbre.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1759">no.</span></span> <span data-ttu-id="b9e4a-1760">do cartao</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1760">do cartao</span></span> 
- <span data-ttu-id="b9e4a-1761">Nbre.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1761">no.</span></span> <span data-ttu-id="b9e4a-1762">do cartão</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1762">do cartão</span></span> 
- <span data-ttu-id="b9e4a-1763">nr carta</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1763">nr carta</span></span> 
- <span data-ttu-id="b9e4a-1764">Nr.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1764">nr.</span></span> <span data-ttu-id="b9e4a-1765">Carta</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1765">carta</span></span> 
- <span data-ttu-id="b9e4a-1766">numeri di scheda</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1766">numeri di scheda</span></span> 
- <span data-ttu-id="b9e4a-1767">numero carta</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1767">numero carta</span></span> 
- <span data-ttu-id="b9e4a-1768">numero de cartao</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1768">numero de cartao</span></span> 
- <span data-ttu-id="b9e4a-1769">numero de carte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1769">numero de carte</span></span> 
- <span data-ttu-id="b9e4a-1770">numero de cartão</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1770">numero de cartão</span></span> 
- <span data-ttu-id="b9e4a-1771">numero de tarjeta</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1771">numero de tarjeta</span></span>
- <span data-ttu-id="b9e4a-1772">numero della carta</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1772">numero della carta</span></span> 
- <span data-ttu-id="b9e4a-1773">numero di carta</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1773">numero di carta</span></span> 
- <span data-ttu-id="b9e4a-1774">numero di scheda</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1774">numero di scheda</span></span> 
- <span data-ttu-id="b9e4a-1775">numero do cartao</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1775">numero do cartao</span></span> 
- <span data-ttu-id="b9e4a-1776">numero do cartão</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1776">numero do cartão</span></span> 
- <span data-ttu-id="b9e4a-1777">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1777">numéro de carte</span></span> 
- <span data-ttu-id="b9e4a-1778">nº carta</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1778">nº carta</span></span> 
- <span data-ttu-id="b9e4a-1779">nº de carte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1779">nº de carte</span></span> 
- <span data-ttu-id="b9e4a-1780">nº de la carte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1780">nº de la carte</span></span> 
- <span data-ttu-id="b9e4a-1781">nº de tarjeta</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1781">nº de tarjeta</span></span> 
- <span data-ttu-id="b9e4a-1782">nº do cartao</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1782">nº do cartao</span></span> 
- <span data-ttu-id="b9e4a-1783">nº do cartão</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1783">nº do cartão</span></span> 
- <span data-ttu-id="b9e4a-1784">n º.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1784">nº.</span></span> <span data-ttu-id="b9e4a-1785">do cartão</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1785">do cartão</span></span> 
- <span data-ttu-id="b9e4a-1786">número de cartao</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1786">número de cartao</span></span> 
- <span data-ttu-id="b9e4a-1787">número de cartão</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1787">número de cartão</span></span> 
- <span data-ttu-id="b9e4a-1788">número de tarjeta</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1788">número de tarjeta</span></span> 
- <span data-ttu-id="b9e4a-1789">número do cartao</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1789">número do cartao</span></span> 
- <span data-ttu-id="b9e4a-1790">scheda dell’assegno</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1790">scheda dell'assegno</span></span> 
- <span data-ttu-id="b9e4a-1791">scheda dell’atmosfera</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1791">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="b9e4a-1792">scheda dell’atmosfera</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1792">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="b9e4a-1793">scheda della banca</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1793">scheda della banca</span></span> 
- <span data-ttu-id="b9e4a-1794">scheda di controllo</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1794">scheda di controllo</span></span> 
- <span data-ttu-id="b9e4a-1795">scheda di debito</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1795">scheda di debito</span></span> 
- <span data-ttu-id="b9e4a-1796">scheda matrice</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1796">scheda matrice</span></span> 
- <span data-ttu-id="b9e4a-1797">schede dell’atmosfera</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1797">schede dell'atmosfera</span></span> 
- <span data-ttu-id="b9e4a-1798">schede di controllo</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1798">schede di controllo</span></span> 
- <span data-ttu-id="b9e4a-1799">schede di debito</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1799">schede di debito</span></span> 
- <span data-ttu-id="b9e4a-1800">schede matrici</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1800">schede matrici</span></span> 
- <span data-ttu-id="b9e4a-1801">scoprono la scheda</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1801">scoprono la scheda</span></span> 
- <span data-ttu-id="b9e4a-1802">scoprono le schede</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1802">scoprono le schede</span></span> 
- <span data-ttu-id="b9e4a-1803">tracteur</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1803">solo</span></span> 
- <span data-ttu-id="b9e4a-1804">supporti di scheda</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1804">supporti di scheda</span></span> 
- <span data-ttu-id="b9e4a-1805">supporto di scheda</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1805">supporto di scheda</span></span> 
- <span data-ttu-id="b9e4a-1806">accéder</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1806">switch</span></span> 
- <span data-ttu-id="b9e4a-1807">tarjeta atm</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1807">tarjeta atm</span></span> 
- <span data-ttu-id="b9e4a-1808">tarjeta credito</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1808">tarjeta credito</span></span> 
- <span data-ttu-id="b9e4a-1809">tarjeta de atm</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1809">tarjeta de atm</span></span> 
- <span data-ttu-id="b9e4a-1810">tarjeta de credito</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1810">tarjeta de credito</span></span> 
- <span data-ttu-id="b9e4a-1811">tarjeta de debito</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1811">tarjeta de debito</span></span> 
- <span data-ttu-id="b9e4a-1812">tarjeta debito</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1812">tarjeta debito</span></span> 
- <span data-ttu-id="b9e4a-1813">tarjeta no</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1813">tarjeta no</span></span>
- <span data-ttu-id="b9e4a-1814">tarjetahabiente</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1814">tarjetahabiente</span></span> 
- <span data-ttu-id="b9e4a-1815">tipo della scheda</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1815">tipo della scheda</span></span> 
- <span data-ttu-id="b9e4a-1816">ufficio giapponese della</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1816">ufficio giapponese della</span></span> 
- <span data-ttu-id="b9e4a-1817">scheda</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1817">scheda</span></span> 
- <span data-ttu-id="b9e4a-1818">v pay</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1818">v pay</span></span> 
- <span data-ttu-id="b9e4a-1819">v-Pay</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1819">v-pay</span></span> 
- <span data-ttu-id="b9e4a-1820">délivrance</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1820">visa</span></span> 
- <span data-ttu-id="b9e4a-1821">visa plus</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1821">visa plus</span></span> 
- <span data-ttu-id="b9e4a-1822">visa electron</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1822">visa electron</span></span> 
- <span data-ttu-id="b9e4a-1823">visto</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1823">visto</span></span> 
- <span data-ttu-id="b9e4a-1824">visum</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1824">visum</span></span> 
- <span data-ttu-id="b9e4a-1825">vpay</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1825">vpay</span></span>   

#### <a name="keyword_card_security_terms_dict"></a><span data-ttu-id="b9e4a-1826">Keyword_card_security_terms_dict</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1826">Keyword_card_security_terms_dict</span></span>

- <span data-ttu-id="b9e4a-1827">numéro d’identification de la carte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1827">card identification number</span></span>
- <span data-ttu-id="b9e4a-1828">vérification de la carte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1828">card verification</span></span> 
- <span data-ttu-id="b9e4a-1829">cardi la verifica</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1829">cardi la verifica</span></span> 
- <span data-ttu-id="b9e4a-1830">nic</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1830">cid</span></span> 
- <span data-ttu-id="b9e4a-1831">cod seg</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1831">cod seg</span></span> 
- <span data-ttu-id="b9e4a-1832">cod seguranca</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1832">cod seguranca</span></span> 
- <span data-ttu-id="b9e4a-1833">cod segurança</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1833">cod segurança</span></span> 
- <span data-ttu-id="b9e4a-1834">cod sicurezza</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1834">cod sicurezza</span></span> 
- <span data-ttu-id="b9e4a-1835">contre.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1835">cod.</span></span> <span data-ttu-id="b9e4a-1836">SEG</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1836">seg</span></span> 
- <span data-ttu-id="b9e4a-1837">contre.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1837">cod.</span></span> <span data-ttu-id="b9e4a-1838">seguranca</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1838">seguranca</span></span> 
- <span data-ttu-id="b9e4a-1839">contre.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1839">cod.</span></span> <span data-ttu-id="b9e4a-1840">segurança</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1840">segurança</span></span> 
- <span data-ttu-id="b9e4a-1841">contre.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1841">cod.</span></span> <span data-ttu-id="b9e4a-1842">sicurezza</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1842">sicurezza</span></span> 
- <span data-ttu-id="b9e4a-1843">codice di sicurezza</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1843">codice di sicurezza</span></span> 
- <span data-ttu-id="b9e4a-1844">codice di verifica</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1844">codice di verifica</span></span> 
- <span data-ttu-id="b9e4a-1845">codigo</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1845">codigo</span></span> 
- <span data-ttu-id="b9e4a-1846">codigo de seguranca</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1846">codigo de seguranca</span></span> 
- <span data-ttu-id="b9e4a-1847">codigo de segurança</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1847">codigo de segurança</span></span> 
- <span data-ttu-id="b9e4a-1848">crittogramma</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1848">crittogramma</span></span> 
- <span data-ttu-id="b9e4a-1849">cryptogram</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1849">cryptogram</span></span> 
- <span data-ttu-id="b9e4a-1850">cryptogramme</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1850">cryptogramme</span></span> 
- <span data-ttu-id="b9e4a-1851">cv2</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1851">cv2</span></span> 
- <span data-ttu-id="b9e4a-1852">lâche</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1852">cvc</span></span> 
- <span data-ttu-id="b9e4a-1853">cvc2</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1853">cvc2</span></span> 
- <span data-ttu-id="b9e4a-1854">cryptogramme</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1854">cvn</span></span> 
- <span data-ttu-id="b9e4a-1855">cvv</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1855">cvv</span></span> 
- <span data-ttu-id="b9e4a-1856">cvv2</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1856">cvv2</span></span> 
- <span data-ttu-id="b9e4a-1857">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1857">cód seguranca</span></span> 
- <span data-ttu-id="b9e4a-1858">cód segurança</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1858">cód segurança</span></span> 
- <span data-ttu-id="b9e4a-1859">cód.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1859">cód.</span></span> <span data-ttu-id="b9e4a-1860">seguranca</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1860">seguranca</span></span> 
- <span data-ttu-id="b9e4a-1861">cód.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1861">cód.</span></span> <span data-ttu-id="b9e4a-1862">segurança</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1862">segurança</span></span> 
- <span data-ttu-id="b9e4a-1863">código</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1863">código</span></span> 
- <span data-ttu-id="b9e4a-1864">código de seguranca</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1864">código de seguranca</span></span> 
- <span data-ttu-id="b9e4a-1865">código de segurança</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1865">código de segurança</span></span> 
- <span data-ttu-id="b9e4a-1866">de kaart controle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1866">de kaart controle</span></span> 
- <span data-ttu-id="b9e4a-1867">geeft nr suit</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1867">geeft nr uit</span></span> 
- <span data-ttu-id="b9e4a-1868">n° d’émission</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1868">issue no</span></span> 
- <span data-ttu-id="b9e4a-1869">numéro d’émission</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1869">issue number</span></span> 
- <span data-ttu-id="b9e4a-1870">kaartidentificatienummer</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1870">kaartidentificatienummer</span></span> 
- <span data-ttu-id="b9e4a-1871">kreditkartenprufnummer</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1871">kreditkartenprufnummer</span></span> 
- <span data-ttu-id="b9e4a-1872">kreditkartenprüfnummer</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1872">kreditkartenprüfnummer</span></span> 
- <span data-ttu-id="b9e4a-1873">kwestieaantal</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1873">kwestieaantal</span></span> 
- <span data-ttu-id="b9e4a-1874">Nbre.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1874">no.</span></span> <span data-ttu-id="b9e4a-1875">dell'edizione</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1875">dell'edizione</span></span> 
- <span data-ttu-id="b9e4a-1876">Nbre.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1876">no.</span></span> <span data-ttu-id="b9e4a-1877">di sicurezza</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1877">di sicurezza</span></span> 
- <span data-ttu-id="b9e4a-1878">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1878">numero de securite</span></span> 
- <span data-ttu-id="b9e4a-1879">numero de verificacao</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1879">numero de verificacao</span></span> 
- <span data-ttu-id="b9e4a-1880">numero dell’edizione</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1880">numero dell'edizione</span></span> 
- <span data-ttu-id="b9e4a-1881">numero di identificazione della</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1881">numero di identificazione della</span></span> 
- <span data-ttu-id="b9e4a-1882">scheda</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1882">scheda</span></span> 
- <span data-ttu-id="b9e4a-1883">numero di sicurezza</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1883">numero di sicurezza</span></span> 
- <span data-ttu-id="b9e4a-1884">numero van veiligheid</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1884">numero van veiligheid</span></span> 
- <span data-ttu-id="b9e4a-1885">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1885">numéro de sécurité</span></span> 
- <span data-ttu-id="b9e4a-1886">nº autorizzazione</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1886">nº autorizzazione</span></span> 
- <span data-ttu-id="b9e4a-1887">número de verificação</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1887">número de verificação</span></span> 
- <span data-ttu-id="b9e4a-1888">perno il blocco</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1888">perno il blocco</span></span> 
- <span data-ttu-id="b9e4a-1889">pin block</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1889">pin block</span></span> 
- <span data-ttu-id="b9e4a-1890">prufziffer</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1890">prufziffer</span></span> 
- <span data-ttu-id="b9e4a-1891">prüfziffer</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1891">prüfziffer</span></span> 
- <span data-ttu-id="b9e4a-1892">code de sécurité</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1892">security code</span></span> 
- <span data-ttu-id="b9e4a-1893">n° de sécurité</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1893">security no</span></span> 
- <span data-ttu-id="b9e4a-1894">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1894">security number</span></span> 
- <span data-ttu-id="b9e4a-1895">sicherheits kode</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1895">sicherheits kode</span></span> 
- <span data-ttu-id="b9e4a-1896">sicherheitscode</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1896">sicherheitscode</span></span> 
- <span data-ttu-id="b9e4a-1897">sicherheitsnummer</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1897">sicherheitsnummer</span></span> 
- <span data-ttu-id="b9e4a-1898">speldblok</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1898">speldblok</span></span> 
- <span data-ttu-id="b9e4a-1899">veiligheid nr</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1899">veiligheid nr</span></span> 
- <span data-ttu-id="b9e4a-1900">veiligheidsaantal</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1900">veiligheidsaantal</span></span> 
- <span data-ttu-id="b9e4a-1901">veiligheidscode</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1901">veiligheidscode</span></span> 
- <span data-ttu-id="b9e4a-1902">veiligheidsnummer</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1902">veiligheidsnummer</span></span> 
- <span data-ttu-id="b9e4a-1903">verfalldatum</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1903">verfalldatum</span></span> 

#### <a name="keyword_card_expiration_terms_dict"></a><span data-ttu-id="b9e4a-1904">Keyword_card_expiration_terms_dict</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1904">Keyword_card_expiration_terms_dict</span></span>

- <span data-ttu-id="b9e4a-1905">ablauf</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1905">ablauf</span></span> 
- <span data-ttu-id="b9e4a-1906">data de expiracao</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1906">data de expiracao</span></span> 
- <span data-ttu-id="b9e4a-1907">data de expiração</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1907">data de expiração</span></span> 
- <span data-ttu-id="b9e4a-1908">data del exp</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1908">data del exp</span></span> 
- <span data-ttu-id="b9e4a-1909">data di exp</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1909">data di exp</span></span> 
- <span data-ttu-id="b9e4a-1910">data di scadenza</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1910">data di scadenza</span></span> 
- <span data-ttu-id="b9e4a-1911">data em que expira</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1911">data em que expira</span></span> 
- <span data-ttu-id="b9e4a-1912">data scad</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1912">data scad</span></span> 
- <span data-ttu-id="b9e4a-1913">data scadenza</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1913">data scadenza</span></span> 
- <span data-ttu-id="b9e4a-1914">date de validité</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1914">date de validité</span></span> 
- <span data-ttu-id="b9e4a-1915">datum afloop</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1915">datum afloop</span></span> 
- <span data-ttu-id="b9e4a-1916">datum van exp</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1916">datum van exp</span></span> 
- <span data-ttu-id="b9e4a-1917">de afloop</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1917">de afloop</span></span> 
- <span data-ttu-id="b9e4a-1918">espira</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1918">espira</span></span> 
- <span data-ttu-id="b9e4a-1919">espira</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1919">espira</span></span> 
- <span data-ttu-id="b9e4a-1920">date d’exp</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1920">exp date</span></span> 
- <span data-ttu-id="b9e4a-1921">exp datum</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1921">exp datum</span></span> 
- <span data-ttu-id="b9e4a-1922">pire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1922">expiration</span></span> 
- <span data-ttu-id="b9e4a-1923">expiration</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1923">expire</span></span> 
- <span data-ttu-id="b9e4a-1924">expire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1924">expires</span></span> 
- <span data-ttu-id="b9e4a-1925">expiration</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1925">expiry</span></span> 
- <span data-ttu-id="b9e4a-1926">fecha de expiracion</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1926">fecha de expiracion</span></span> 
- <span data-ttu-id="b9e4a-1927">fecha de venc</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1927">fecha de venc</span></span> 
- <span data-ttu-id="b9e4a-1928">gultig bis</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1928">gultig bis</span></span> 
- <span data-ttu-id="b9e4a-1929">gultigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1929">gultigkeitsdatum</span></span> 
- <span data-ttu-id="b9e4a-1930">gültig bis</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1930">gültig bis</span></span> 
- <span data-ttu-id="b9e4a-1931">gültigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1931">gültigkeitsdatum</span></span> 
- <span data-ttu-id="b9e4a-1932">la scadenza</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1932">la scadenza</span></span> 
- <span data-ttu-id="b9e4a-1933">scadenza</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1933">scadenza</span></span> 
- <span data-ttu-id="b9e4a-1934">valable</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1934">valable</span></span> 
- <span data-ttu-id="b9e4a-1935">validade</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1935">validade</span></span> 
- <span data-ttu-id="b9e4a-1936">valido hasta</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1936">valido hasta</span></span> 
- <span data-ttu-id="b9e4a-1937">valorisation</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1937">valor</span></span> 
- <span data-ttu-id="b9e4a-1938">venc</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1938">venc</span></span> 
- <span data-ttu-id="b9e4a-1939">vencimento</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1939">vencimento</span></span> 
- <span data-ttu-id="b9e4a-1940">vencimiento</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1940">vencimiento</span></span> 
- <span data-ttu-id="b9e4a-1941">verloopt</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1941">verloopt</span></span> 
- <span data-ttu-id="b9e4a-1942">vervaldag</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1942">vervaldag</span></span> 
- <span data-ttu-id="b9e4a-1943">vervaldatum</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1943">vervaldatum</span></span> 
- <span data-ttu-id="b9e4a-1944">vto</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1944">vto</span></span> 
- <span data-ttu-id="b9e4a-1945">válido hasta</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1945">válido hasta</span></span> 
   
## <a name="eu-drivers-license-number"></a><span data-ttu-id="b9e4a-1946">Numéro de permis de conduire de l’UE</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1946">EU Driver's License Number</span></span>

<span data-ttu-id="b9e4a-1947">Pour en savoir plus, consultez [la rubrique informations sensibles sur le numéro de permis de conduire du pilote de l’UE](eu-driver-s-license-number.md).</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1947">To learn more, see [EU Driver's License Number sensitive information type](eu-driver-s-license-number.md).</span></span>
  
## <a name="eu-national-identification-number"></a><span data-ttu-id="b9e4a-1948">Numéro d’identification nationale de l’UE</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1948">EU National Identification Number</span></span>

<span data-ttu-id="b9e4a-1949">Pour en savoir plus, consultez la rubrique [informations sensibles du numéro d’identification national](eu-national-identification-number.md)de l’UE.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1949">To learn more, see [EU National Identification Number sensitive information type](eu-national-identification-number.md).</span></span>
  
## <a name="eu-passport-number"></a><span data-ttu-id="b9e4a-1950">Numéro de passeport UE</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1950">EU Passport Number</span></span>

<span data-ttu-id="b9e4a-1951">Pour en savoir plus, consultez la rubrique [type d’informations sensibles du numéro de passeport européen](eu-passport-number.md).</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1951">To learn more, see [EU Passport Number sensitive information type](eu-passport-number.md).</span></span>
  
## <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="b9e4a-1952">Numéro de sécurité sociale de l’UE ou ID équivalent</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1952">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="b9e4a-1953">Pour en savoir plus, consultez la rubrique [numéro de sécurité sociale de l’UE ou type d’informations sensibles ID équivalent](eu-social-security-number-or-equivalent-id.md).</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1953">To learn more, see [EU Social Security Number or Equivalent ID sensitive information type](eu-social-security-number-or-equivalent-id.md).</span></span>
  
## <a name="eu-tax-identification-number"></a><span data-ttu-id="b9e4a-1954">Numéro d’identification fiscale de l’UE</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1954">EU Tax Identification Number</span></span>

<span data-ttu-id="b9e4a-1955">Pour en savoir plus, consultez la rubrique [euro Tax identification number sensitive type information](eu-tax-identification-number.md).</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1955">To learn more, see [EU Tax Identification Number sensitive information type](eu-tax-identification-number.md).</span></span>
  
## <a name="finland-national-id"></a><span data-ttu-id="b9e4a-1956">ID national finlandais</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1956">Finland National ID</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-1957">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1957">Format</span></span>

<span data-ttu-id="b9e4a-1958">Six chiffres plus un caractère indiquant un siècle plus trois chiffres plus un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1958">Six digits plus a character indicating a century plus three digits plus a check digit</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-1959">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1959">Pattern</span></span>

<span data-ttu-id="b9e4a-1960">Le modèle doit inclure tous les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1960">Pattern must include all of the following:</span></span>
- <span data-ttu-id="b9e4a-1961">Six chiffres au format JJMMAA qui représentent la date de naissance</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1961">Six digits in the format format DDMMYY which are a date of birth</span></span> 
- <span data-ttu-id="b9e4a-1962">Marqueur de siècle (soit « - », « + » ou « a »)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1962">Century marker (either '-', '+' or 'a')</span></span> 
- <span data-ttu-id="b9e4a-1963">Numéro d’identification personnel à trois chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1963">Three-digit personal identification number</span></span> 
- <span data-ttu-id="b9e4a-1964">Un chiffre ou une lettre (ne respectant pas la casse) de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1964">A digit or letter (case insensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-1965">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1965">Checksum</span></span>

<span data-ttu-id="b9e4a-1966">Oui</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1966">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-1967">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1967">Definition</span></span>

<span data-ttu-id="b9e4a-1968">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1968">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-1969">La fonction Func_finnish_national_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1969">The function Func_finnish_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-1970">Un mot clé figurant dans la liste Keyword_finnish_national_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1970">A keyword from Keyword_finnish_national_id is found.</span></span>
- <span data-ttu-id="b9e4a-1971">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1971">The checksum passes.</span></span>

```
<!-- Finnish National ID-->
<Entity id="338FD995-4CB5-4F87-AD35-79BD1DD926C1" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finnish_national_id" />
          <Match idRef="Keyword_finnish_national_id" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b9e4a-1972">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1972">Keywords</span></span>

- <span data-ttu-id="b9e4a-1973">Keyword_finnish_national_id</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1973">Keyword_finnish_national_id</span></span>
- <span data-ttu-id="b9e4a-1974">Sosiaaliturvatunnus</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1974">Sosiaaliturvatunnus</span></span>
- <span data-ttu-id="b9e4a-1975">SOTU Henkilötunnus HETU</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1975">SOTU Henkilötunnus HETU</span></span>
- <span data-ttu-id="b9e4a-1976">Personbeteckning</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1976">Personbeteckning</span></span>
- <span data-ttu-id="b9e4a-1977">Personnummer</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1977">Personnummer</span></span>
   
## <a name="finland-passport-number"></a><span data-ttu-id="b9e4a-1978">Numéro de passeport Finlande</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1978">Finland Passport Number</span></span>

<span data-ttu-id="b9e4a-1979">Combinaison de format de neuf lettres et chiffres combinaison de neuf lettres et chiffres: deux lettres (ne respectant pas la casse) sept chiffres somme de contrôle no la stratégie DLP est de 75% en certitude qu’elle a détecté ce type d’informations sensibles si, dans un proximité de 300 caractères: l’expression régulière Regex_finland_passport_number trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1979">Format Combination of nine letters and digits Pattern Combination of nine letters and digits: Two letters (not case sensitive) Seven digits Checksum No Definition A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_finland_passport_number finds content that matches the pattern.</span></span>
<span data-ttu-id="b9e4a-1980">Un mot clé figurant dans la liste Keyword_finland_passport_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1980">A keyword from Keyword_finland_passport_number is found.</span></span>
<!-- Finland Passport Number -->
<span data-ttu-id="b9e4a-1981"><Entity id="d1685ac3-1d3a-40f8-8198-32ef5669c7a5" recommendedConfidence="75" patternsProximity="300"> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_finland_passport_number"/> <Match idRef="Keyword_finland_passport_number"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="b9e4a-1981"></span></span>
<span data-ttu-id="b9e4a-1982">Mots clés Keyword_finland_passport_number Passport passes</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1982">Keywords Keyword_finland_passport_number Passport Passi</span></span>
   
## <a name="france-drivers-license-number"></a><span data-ttu-id="b9e4a-1983">Numéro de permis de conduire France</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1983">France Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-1984">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1984">Format</span></span>

<span data-ttu-id="b9e4a-1985">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1985">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-1986">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1986">Pattern</span></span>

<span data-ttu-id="b9e4a-1987">12 chiffres avec validation pour écarter les modèles similaires, comme les numéros de téléphone français</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1987">12 digits with validation to discount similar patterns such as French telephone numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-1988">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1988">Checksum</span></span>

<span data-ttu-id="b9e4a-1989">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1989">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-1990">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1990">Definition</span></span>

<span data-ttu-id="b9e4a-1991">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1991">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-1992">La fonction Func_french_drivers_license trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1992">The function Func_french_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-1993">Au moins une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1993">At least one of the following is true:</span></span>
- <span data-ttu-id="b9e4a-1994">Un mot clé figurant dans la liste Keyword_french_drivers_license est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1994">A keyword from Keyword_french_drivers_license is found.</span></span>
- <span data-ttu-id="b9e4a-1995">La fonction Func_eu_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1995">The function Func_eu_date finds a date in the right date format.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-1996">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1996">Keywords</span></span>

#### <a name="keyword_french_drivers_license"></a><span data-ttu-id="b9e4a-1997">Keyword_french_drivers_license</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1997">Keyword_french_drivers_license</span></span>

- <span data-ttu-id="b9e4a-1998">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1998">drivers licence</span></span>
- <span data-ttu-id="b9e4a-1999">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-1999">drivers license</span></span>
- <span data-ttu-id="b9e4a-2000">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2000">driving licence</span></span>
- <span data-ttu-id="b9e4a-2001">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2001">driving license</span></span>
- <span data-ttu-id="b9e4a-2002">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2002">permis de conduire</span></span>
- <span data-ttu-id="b9e4a-2003">numéro de permis</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2003">licence number</span></span>
- <span data-ttu-id="b9e4a-2004">numéro de permis</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2004">license number</span></span>
- <span data-ttu-id="b9e4a-2005">numéros de permis</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2005">licence numbers</span></span>
- <span data-ttu-id="b9e4a-2006">numéros de permis</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2006">license numbers</span></span>

## <a name="france-national-id-card-cni"></a><span data-ttu-id="b9e4a-2007">Carte nationale d’identité (CNI) France</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2007">France National ID Card (CNI)</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-2008">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2008">Format</span></span>

<span data-ttu-id="b9e4a-2009">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2009">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-2010">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2010">Pattern</span></span>

<span data-ttu-id="b9e4a-2011">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2011">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-2012">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2012">Checksum</span></span>

<span data-ttu-id="b9e4a-2013">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2013">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-2014">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2014">Definition</span></span>

<span data-ttu-id="b9e4a-2015">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2015">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-2016">L’expression régulière Regex_france_cni trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2016">The regular expression Regex_france_cni finds content that matches the pattern.</span></span>

```
<!-- France CNI -->
<Entity id="f741ac74-1bc0-4665-b69b-f0c7f927c0c4" patternsProximity="300" recommendedConfidence="65">
  <Pattern confidenceLevel="65">
        <IdMatch idRef="Regex_france_cni" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b9e4a-2017">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2017">Keywords</span></span>

<span data-ttu-id="b9e4a-2018">Aucun</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2018">None</span></span>
   
## <a name="france-passport-number"></a><span data-ttu-id="b9e4a-2019">Numéro de passeport France</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2019">France Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-2020">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2020">Format</span></span>

<span data-ttu-id="b9e4a-2021">Neuf chiffres et lettres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2021">Nine digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-2022">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2022">Pattern</span></span>

<span data-ttu-id="b9e4a-2023">Neuf chiffres et lettres :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2023">Nine digits and letters:</span></span>
- <span data-ttu-id="b9e4a-2024">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2024">Two digits</span></span> 
- <span data-ttu-id="b9e4a-2025">Deux lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2025">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="b9e4a-2026">Cinq chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2026">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-2027">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2027">Checksum</span></span>

<span data-ttu-id="b9e4a-2028">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2028">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-2029">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2029">Definition</span></span>

<span data-ttu-id="b9e4a-2030">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2030">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-2031">La fonction Func_fr_passport trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2031">The function Func_fr_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-2032">Un mot clé figurant dans la liste Keyword_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2032">A keyword from Keyword_passport is found.</span></span>

```
<!-- France Passport Number -->
<Entity id="3008b884-8c8c-4cd8-a289-99f34fc7ff5d" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_fr_passport" />
        <Match idRef="Keyword_passport" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b9e4a-2033">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2033">Keywords</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="b9e4a-2034">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2034">Keyword_passport</span></span>

- <span data-ttu-id="b9e4a-2035">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2035">Passport Number</span></span>
- <span data-ttu-id="b9e4a-2036">N° de passeport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2036">Passport No</span></span>
- <span data-ttu-id="b9e4a-2037"># Passeport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2037">Passport #</span></span>
- <span data-ttu-id="b9e4a-2038">Tel #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2038">Passport#</span></span>
- <span data-ttu-id="b9e4a-2039">PassportID</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2039">PassportID</span></span>
- <span data-ttu-id="b9e4a-2040">N ° passeport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2040">Passportno</span></span>
- <span data-ttu-id="b9e4a-2041">passportnumber</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2041">passportnumber</span></span>
- <span data-ttu-id="b9e4a-2042">パスポート</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2042">パスポート</span></span>
- <span data-ttu-id="b9e4a-2043">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2043">パスポート番号</span></span>
- <span data-ttu-id="b9e4a-2044">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2044">パスポートのNum</span></span>
- <span data-ttu-id="b9e4a-2045">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2045">パスポート ＃</span></span> 
- <span data-ttu-id="b9e4a-2046">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2046">Numéro de passeport</span></span>
- <span data-ttu-id="b9e4a-2047">Passeport n°</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2047">Passeport n °</span></span>
- <span data-ttu-id="b9e4a-2048">Passeport numéro</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2048">Passeport Non</span></span>
- <span data-ttu-id="b9e4a-2049"># Passeport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2049">Passeport #</span></span>
- <span data-ttu-id="b9e4a-2050">Passeport #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2050">Passeport#</span></span>
- <span data-ttu-id="b9e4a-2051">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2051">PasseportNon</span></span>
- <span data-ttu-id="b9e4a-2052">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2052">Passeportn °</span></span>

      
## <a name="france-social-security-number-insee"></a><span data-ttu-id="b9e4a-2053">Numéro de sécurité sociale (INSEE) France</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2053">France Social Security Number (INSEE)</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-2054">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2054">Format</span></span>

<span data-ttu-id="b9e4a-2055">15 chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2055">15 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-2056">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2056">Pattern</span></span>

<span data-ttu-id="b9e4a-2057">Doit correspondre à l’un des deux modèles suivants :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2057">Must match one of two patterns:</span></span>
- <span data-ttu-id="b9e4a-2058">13 chiffres suivis d’un espace suivi de deux chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2058">13 digits followed by a space followed by two digits</span></span><br/>
<span data-ttu-id="b9e4a-2059">ou</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2059">or</span></span>
- <span data-ttu-id="b9e4a-2060">15 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2060">15 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-2061">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2061">Checksum</span></span>

<span data-ttu-id="b9e4a-2062">Oui</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2062">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-2063">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2063">Definition</span></span>

<span data-ttu-id="b9e4a-2064">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 95 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2064">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-2065">La fonction Func_french_insee ou Func_fr_insee trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2065">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-2066">Un mot clé figurant dans la liste Keyword_fr_insee est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2066">A keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="b9e4a-2067">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2067">The checksum passes.</span></span>

<span data-ttu-id="b9e4a-2068">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2068">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-2069">La fonction Func_french_insee ou Func_fr_insee trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2069">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-2070">Aucun mot clé figurant dans la liste Keyword_fr_insee n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2070">No keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="b9e4a-2071">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2071">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-2072">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2072">Keywords</span></span>

#### <a name="keyword_fr_insee"></a><span data-ttu-id="b9e4a-2073">Keyword_fr_insee</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2073">Keyword_fr_insee</span></span>

- <span data-ttu-id="b9e4a-2074">INSEE</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2074">insee</span></span>
- <span data-ttu-id="b9e4a-2075">securité sociale</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2075">securité sociale</span></span>
- <span data-ttu-id="b9e4a-2076">securite sociale</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2076">securite sociale</span></span>
- <span data-ttu-id="b9e4a-2077">id national</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2077">national id</span></span>
- <span data-ttu-id="b9e4a-2078">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2078">national identification</span></span>
- <span data-ttu-id="b9e4a-2079">numéro d’identité</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2079">numéro d'identité</span></span>
- <span data-ttu-id="b9e4a-2080">n° d’identité</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2080">no d'identité</span></span>
- <span data-ttu-id="b9e4a-2081">Nbre.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2081">no.</span></span> <span data-ttu-id="b9e4a-2082">d’identité</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2082">d'identité</span></span>
- <span data-ttu-id="b9e4a-2083">numéro d’identité</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2083">numero d'identite</span></span>
- <span data-ttu-id="b9e4a-2084">n° d’identité</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2084">no d'identite</span></span>
- <span data-ttu-id="b9e4a-2085">Nbre.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2085">no.</span></span> <span data-ttu-id="b9e4a-2086">d’identite</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2086">d'identite</span></span>
- <span data-ttu-id="b9e4a-2087">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2087">social security number</span></span>
- <span data-ttu-id="b9e4a-2088">code de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2088">social security code</span></span>
- <span data-ttu-id="b9e4a-2089">numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2089">social insurance number</span></span>
- <span data-ttu-id="b9e4a-2090">le numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2090">le numéro d'identification nationale</span></span>
- <span data-ttu-id="b9e4a-2091">d’identité nationale</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2091">d'identité nationale</span></span>
- <span data-ttu-id="b9e4a-2092">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2092">numéro de sécurité sociale</span></span>
- <span data-ttu-id="b9e4a-2093">le code de la sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2093">le code de la sécurité sociale</span></span>
- <span data-ttu-id="b9e4a-2094">numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2094">numéro d'assurance sociale</span></span>
- <span data-ttu-id="b9e4a-2095">numéro de sécu</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2095">numéro de sécu</span></span>
- <span data-ttu-id="b9e4a-2096">code sécu</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2096">code sécu</span></span> 
   
## <a name="german-drivers-license-number"></a><span data-ttu-id="b9e4a-2097">Numéro de permis de conduire Allemagne</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2097">German Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-2098">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2098">Format</span></span>

<span data-ttu-id="b9e4a-2099">Combinaison de 11 chiffres et lettres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2099">Combination of 11 digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-2100">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2100">Pattern</span></span>

<span data-ttu-id="b9e4a-2101">11 chiffres et lettres (ne respectent pas la casse) :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2101">11 digits and letters (not case sensitive):</span></span>
- <span data-ttu-id="b9e4a-2102">Un chiffre ou une lettre</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2102">A digit or letter</span></span> 
- <span data-ttu-id="b9e4a-2103">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2103">Two digits</span></span> 
- <span data-ttu-id="b9e4a-2104">Six chiffres ou lettres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2104">Six digits or letters</span></span> 
- <span data-ttu-id="b9e4a-2105">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2105">A digit</span></span> 
- <span data-ttu-id="b9e4a-2106">Un chiffre ou une lettre</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2106">A digit or letter</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-2107">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2107">Checksum</span></span>

<span data-ttu-id="b9e4a-2108">Oui</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2108">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-2109">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2109">Definition</span></span>

<span data-ttu-id="b9e4a-2110">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2110">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-2111">La fonction Func_german_drivers_license trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2111">The function Func_german_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-2112">Au moins une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2112">At least one of the following is true:</span></span>
    - <span data-ttu-id="b9e4a-2113">Un mot clé figurant dans la liste Keyword_german_drivers_license_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2113">A keyword from Keyword_german_drivers_license_number is found.</span></span>
    - <span data-ttu-id="b9e4a-2114">Un mot clé figurant dans la liste Keyword_german_drivers_license_collaborative est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2114">A keyword from Keyword_german_drivers_license_collaborative is found.</span></span>
    - <span data-ttu-id="b9e4a-2115">Un mot clé figurant dans la liste Keyword_german_drivers_license est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2115">A keyword from Keyword_german_drivers_license is found.</span></span>
- <span data-ttu-id="b9e4a-2116">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2116">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-2117">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2117">Keywords</span></span>

#### <a name="keyword_german_drivers_license_number"></a><span data-ttu-id="b9e4a-2118">Keyword_german_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2118">Keyword_german_drivers_license_number</span></span>

- <span data-ttu-id="b9e4a-2119">Führerschein</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2119">Führerschein</span></span>
- <span data-ttu-id="b9e4a-2120">Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2120">Fuhrerschein</span></span>
- <span data-ttu-id="b9e4a-2121">Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2121">Fuehrerschein</span></span>
- <span data-ttu-id="b9e4a-2122">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2122">Führerscheinnummer</span></span>
- <span data-ttu-id="b9e4a-2123">Fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2123">Fuhrerscheinnummer</span></span>
- <span data-ttu-id="b9e4a-2124">Fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2124">Fuehrerscheinnummer</span></span>
- <span data-ttu-id="b9e4a-2125">Führerschein</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2125">Führerschein-</span></span> 
- <span data-ttu-id="b9e4a-2126">Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2126">Fuhrerschein-</span></span> 
- <span data-ttu-id="b9e4a-2127">Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2127">Fuehrerschein-</span></span> 
- <span data-ttu-id="b9e4a-2128">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2128">FührerscheinnummerNr</span></span>
- <span data-ttu-id="b9e4a-2129">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2129">FuhrerscheinnummerNr</span></span>
- <span data-ttu-id="b9e4a-2130">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2130">FuehrerscheinnummerNr</span></span>
- <span data-ttu-id="b9e4a-2131">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2131">FührerscheinnummerKlasse</span></span>
- <span data-ttu-id="b9e4a-2132">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2132">FuhrerscheinnummerKlasse</span></span>
- <span data-ttu-id="b9e4a-2133">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2133">FuehrerscheinnummerKlasse</span></span>
- <span data-ttu-id="b9e4a-2134">Führerschein - Nr</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2134">Führerschein- Nr</span></span>
- <span data-ttu-id="b9e4a-2135">Fuhrerschein - Nr</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2135">Fuhrerschein- Nr</span></span>
- <span data-ttu-id="b9e4a-2136">Fuehrerschein - Nr</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2136">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="b9e4a-2137">Führerschein - Klasse</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2137">Führerschein- Klasse</span></span> 
- <span data-ttu-id="b9e4a-2138">Fuhrerschein - Klasse</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2138">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="b9e4a-2139">Fuehrerschein - Klasse</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2139">Fuehrerschein- Klasse</span></span>
- <span data-ttu-id="b9e4a-2140">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2140">FührerscheinnummerNr</span></span> 
- <span data-ttu-id="b9e4a-2141">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2141">FuhrerscheinnummerNr</span></span> 
- <span data-ttu-id="b9e4a-2142">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2142">FuehrerscheinnummerNr</span></span> 
- <span data-ttu-id="b9e4a-2143">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2143">FührerscheinnummerKlasse</span></span> 
- <span data-ttu-id="b9e4a-2144">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2144">FuhrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="b9e4a-2145">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2145">FuehrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="b9e4a-2146">Führerschein - Nr</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2146">Führerschein- Nr</span></span> 
- <span data-ttu-id="b9e4a-2147">Fuhrerschein - Nr</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2147">Fuhrerschein- Nr</span></span> 
- <span data-ttu-id="b9e4a-2148">Fuehrerschein - Nr</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2148">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="b9e4a-2149">Führerschein - Klasse</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2149">Führerschein- Klasse</span></span> 
- <span data-ttu-id="b9e4a-2150">Fuhrerschein - Klasse</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2150">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="b9e4a-2151">Fuehrerschein - Klasse</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2151">Fuehrerschein- Klasse</span></span> 
- <span data-ttu-id="b9e4a-2152">LD</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2152">DL</span></span> 
- <span data-ttu-id="b9e4a-2153">DISTRIBUTION</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2153">DLS</span></span>
- <span data-ttu-id="b9e4a-2154">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2154">Driv Lic</span></span> 
- <span data-ttu-id="b9e4a-2155">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2155">Driv Licen</span></span> 
- <span data-ttu-id="b9e4a-2156">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2156">Driv License</span></span>
- <span data-ttu-id="b9e4a-2157">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2157">Driv Licenses</span></span> 
- <span data-ttu-id="b9e4a-2158">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2158">Driv Licence</span></span> 
- <span data-ttu-id="b9e4a-2159">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2159">Driv Licences</span></span> 
- <span data-ttu-id="b9e4a-2160">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2160">Driv Lic</span></span> 
- <span data-ttu-id="b9e4a-2161">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2161">Driver Licen</span></span> 
- <span data-ttu-id="b9e4a-2162">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2162">Driver License</span></span> 
- <span data-ttu-id="b9e4a-2163">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2163">Driver Licenses</span></span> 
- <span data-ttu-id="b9e4a-2164">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2164">Driver Licence</span></span> 
- <span data-ttu-id="b9e4a-2165">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2165">Driver Licences</span></span> 
- <span data-ttu-id="b9e4a-2166">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2166">Drivers Lic</span></span> 
- <span data-ttu-id="b9e4a-2167">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2167">Drivers Licen</span></span> 
- <span data-ttu-id="b9e4a-2168">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2168">Drivers License</span></span> 
- <span data-ttu-id="b9e4a-2169">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2169">Drivers Licenses</span></span> 
- <span data-ttu-id="b9e4a-2170">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2170">Drivers Licence</span></span> 
- <span data-ttu-id="b9e4a-2171">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2171">Drivers Licences</span></span> 
- <span data-ttu-id="b9e4a-2172">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2172">Driver's Lic</span></span> 
- <span data-ttu-id="b9e4a-2173">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2173">Driver's Licen</span></span> 
- <span data-ttu-id="b9e4a-2174">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2174">Driver's License</span></span> 
- <span data-ttu-id="b9e4a-2175">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2175">Driver's Licenses</span></span> 
- <span data-ttu-id="b9e4a-2176">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2176">Driver's Licence</span></span> 
- <span data-ttu-id="b9e4a-2177">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2177">Driver's Licences</span></span> 
- <span data-ttu-id="b9e4a-2178">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2178">Driving Lic</span></span> 
- <span data-ttu-id="b9e4a-2179">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2179">Driving Licen</span></span> 
- <span data-ttu-id="b9e4a-2180">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2180">Driving License</span></span> 
- <span data-ttu-id="b9e4a-2181">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2181">Driving Licenses</span></span> 
- <span data-ttu-id="b9e4a-2182">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2182">Driving Licence</span></span> 
- <span data-ttu-id="b9e4a-2183">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2183">Driving Licences</span></span>

#### <a name="keyword_german_drivers_license_collaborative"></a><span data-ttu-id="b9e4a-2184">Keyword_german_drivers_license_collaborative</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2184">Keyword_german_drivers_license_collaborative</span></span>

- <span data-ttu-id="b9e4a-2185">Nr-Führerschein</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2185">Nr-Führerschein</span></span> 
- <span data-ttu-id="b9e4a-2186">Nr-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2186">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="b9e4a-2187">Nr-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2187">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="b9e4a-2188">Non-Führerschein</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2188">No-Führerschein</span></span> 
- <span data-ttu-id="b9e4a-2189">Non-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2189">No-Fuhrerschein</span></span> 
- <span data-ttu-id="b9e4a-2190">Non-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2190">No-Fuehrerschein</span></span> 
- <span data-ttu-id="b9e4a-2191">N-Führerschein</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2191">N-Führerschein</span></span> 
- <span data-ttu-id="b9e4a-2192">N-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2192">N-Fuhrerschein</span></span> 
- <span data-ttu-id="b9e4a-2193">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2193">N-Fuehrerschein</span></span>
- <span data-ttu-id="b9e4a-2194">Nr-Führerschein</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2194">Nr-Führerschein</span></span> 
- <span data-ttu-id="b9e4a-2195">Nr-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2195">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="b9e4a-2196">Nr-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2196">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="b9e4a-2197">Non-Führerschein</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2197">No-Führerschein</span></span> 
- <span data-ttu-id="b9e4a-2198">Non-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2198">No-Fuhrerschein</span></span> 
- <span data-ttu-id="b9e4a-2199">Non-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2199">No-Fuehrerschein</span></span> 
- <span data-ttu-id="b9e4a-2200">N-Führerschein</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2200">N-Führerschein</span></span> 
- <span data-ttu-id="b9e4a-2201">N-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2201">N-Fuhrerschein</span></span> 
- <span data-ttu-id="b9e4a-2202">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2202">N-Fuehrerschein</span></span> 

#### <a name="keyword_german_drivers_license"></a><span data-ttu-id="b9e4a-2203">Keyword_german_drivers_license</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2203">Keyword_german_drivers_license</span></span>

- <span data-ttu-id="b9e4a-2204">ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2204">ausstellungsdatum</span></span>
- <span data-ttu-id="b9e4a-2205">ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2205">ausstellungsort</span></span>
- <span data-ttu-id="b9e4a-2206">ausstellende behöde</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2206">ausstellende behöde</span></span>
- <span data-ttu-id="b9e4a-2207">ausstellende behorde</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2207">ausstellende behorde</span></span>
- <span data-ttu-id="b9e4a-2208">ausstellende behoerde</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2208">ausstellende behoerde</span></span>
   
## <a name="german-passport-number"></a><span data-ttu-id="b9e4a-2209">Numéro de passeport Allemagne</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2209">German Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-2210">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2210">Format</span></span>

<span data-ttu-id="b9e4a-2211">10 chiffres ou lettres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2211">10 digits or letters</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-2212">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2212">Pattern</span></span>

<span data-ttu-id="b9e4a-2213">Le modèle doit inclure tous les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2213">Pattern must include all of the following:</span></span>
- <span data-ttu-id="b9e4a-2214">Le premier caractère est un chiffre ou une lettre de cet ensemble (C, F, G, H, J, K)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2214">First character is a digit or a letter from this set (C, F, G, H, J, K)</span></span> 
- <span data-ttu-id="b9e4a-2215">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2215">Three digits</span></span> 
- <span data-ttu-id="b9e4a-2216">Cinq chiffres ou lettres à partir de cet ensemble (C, -H, J-N, P, R, T, V-Z)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2216">Five digits or letters from this set (C, -H, J-N, P, R, T, V-Z)</span></span> 
- <span data-ttu-id="b9e4a-2217">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2217">A digit</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-2218">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2218">Checksum</span></span>

<span data-ttu-id="b9e4a-2219">Oui</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2219">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-2220">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2220">Definition</span></span>

<span data-ttu-id="b9e4a-2221">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2221">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-2222">La fonction Func_german_passport trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2222">The function Func_german_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-2223">Un mot clé présent dans l’une des cinq listes de mots clés est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2223">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="b9e4a-2224">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2224">The checksum passes.</span></span>

<span data-ttu-id="b9e4a-2225">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2225">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-2226">La fonction Func_german_passport_data trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2226">The function Func_german_passport_data finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-2227">Un mot clé présent dans l’une des cinq listes de mots clés est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2227">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="b9e4a-2228">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2228">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-2229">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2229">Keywords</span></span>

#### <a name="keyword_german_passport"></a><span data-ttu-id="b9e4a-2230">Keyword_german_passport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2230">Keyword_german_passport</span></span>

- <span data-ttu-id="b9e4a-2231">reisepass</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2231">reisepass</span></span>
- <span data-ttu-id="b9e4a-2232">reisepasse</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2232">reisepasse</span></span>
- <span data-ttu-id="b9e4a-2233">reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2233">reisepassnummer</span></span>
- <span data-ttu-id="b9e4a-2234">tel</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2234">passport</span></span>
- <span data-ttu-id="b9e4a-2235">passeports</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2235">passports</span></span>

#### <a name="keyword_german_passport_collaborative"></a><span data-ttu-id="b9e4a-2236">Keyword_german_passport_collaborative</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2236">Keyword_german_passport_collaborative</span></span>

- <span data-ttu-id="b9e4a-2237">geburtsdatum</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2237">geburtsdatum</span></span>
- <span data-ttu-id="b9e4a-2238">ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2238">ausstellungsdatum</span></span>
- <span data-ttu-id="b9e4a-2239">ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2239">ausstellungsort</span></span>

#### <a name="keyword_german_passport_number"></a><span data-ttu-id="b9e4a-2240">Keyword_german_passport_number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2240">Keyword_german_passport_number</span></span>

<span data-ttu-id="b9e4a-2241">No-Reisepass Nr-Reisepass</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2241">No-Reisepass Nr-Reisepass</span></span>

#### <a name="keyword_german_passport1"></a><span data-ttu-id="b9e4a-2242">Keyword_german_passport1</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2242">Keyword_german_passport1</span></span>

<span data-ttu-id="b9e4a-2243">Reisepass-Nr</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2243">Reisepass-Nr</span></span>

#### <a name="keyword_german_passport2"></a><span data-ttu-id="b9e4a-2244">Keyword_german_passport2</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2244">Keyword_german_passport2</span></span>

<span data-ttu-id="b9e4a-2245">bnationalit. t</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2245">bnationalit.t</span></span>
   
## <a name="germany-identity-card-number"></a><span data-ttu-id="b9e4a-2246">Numéro de carte d’identité allemand</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2246">Germany Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-2247">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2247">Format</span></span>

<span data-ttu-id="b9e4a-2248">Depuis le 1er novembre 2010: neuf lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2248">Since 1 November 2010: Nine letters and digits</span></span>

<span data-ttu-id="b9e4a-2249">Du 1er avril 1987 au 31 octobre 2010:10 chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2249">From 1 April 1987 until 31 October 2010: 10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-2250">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2250">Pattern</span></span>

<span data-ttu-id="b9e4a-2251">Depuis le 1er novembre 2010 :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2251">Since 1 November 2010:</span></span>
- <span data-ttu-id="b9e4a-2252">Une lettre (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="b9e4a-2252">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="b9e4a-2253">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2253">Eight digits</span></span>

<span data-ttu-id="b9e4a-2254">Du 1er avril 1987 au 31 octobre 2010:</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2254">From 1 April 1987 until 31 October 2010:</span></span>
- <span data-ttu-id="b9e4a-2255">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2255">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-2256">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2256">Checksum</span></span>

<span data-ttu-id="b9e4a-2257">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2257">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-2258">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2258">Definition</span></span>

<span data-ttu-id="b9e4a-2259">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2259">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-2260">L’expression régulière Regex_germany_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2260">The regular expression Regex_germany_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-2261">Un mot clé figurant dans la liste Keyword_germany_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2261">A keyword from Keyword_germany_id_card is found.</span></span>

```
<!-- Germany Identity Card Number -->
<Entity id="e577372f-c42e-47a0-9d85-bebed1c237d4" recommendedConfidence="65" patternsProximity="300">
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Regex_germany_id_card"/>
     <Match idRef="Keyword_germany_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b9e4a-2262">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2262">Keywords</span></span>

#### <a name="keyword_germany_id_card"></a><span data-ttu-id="b9e4a-2263">Keyword_germany_id_card</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2263">Keyword_germany_id_card</span></span>

- <span data-ttu-id="b9e4a-2264">Identity Card</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2264">Identity Card</span></span>
- <span data-ttu-id="b9e4a-2265">ID</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2265">ID</span></span>
- <span data-ttu-id="b9e4a-2266">Identificateur</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2266">Identification</span></span>
- <span data-ttu-id="b9e4a-2267">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2267">Personalausweis</span></span>
- <span data-ttu-id="b9e4a-2268">Identifizierungsnummer</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2268">Identifizierungsnummer</span></span>
- <span data-ttu-id="b9e4a-2269">Ausweis</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2269">Ausweis</span></span>
- <span data-ttu-id="b9e4a-2270">Identifikation</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2270">Identifikation</span></span>
   
## <a name="greece-national-id-card"></a><span data-ttu-id="b9e4a-2271">Carte d’identité nationale Grèce</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2271">Greece National ID Card</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-2272">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2272">Format</span></span>

<span data-ttu-id="b9e4a-2273">Combinaison de 7 ou 8 lettres et chiffres, plus un tiret</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2273">Combination of 7-8 letters and numbers plus a dash</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-2274">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2274">Pattern</span></span>

<span data-ttu-id="b9e4a-2275">Sept lettres et chiffres (ancien format) :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2275">Seven letters and numbers (old format):</span></span>
- <span data-ttu-id="b9e4a-2276">Une lettre (de l’alphabet grec) </span><span class="sxs-lookup"><span data-stu-id="b9e4a-2276">One letter (any letter of the Greek alphabet)</span></span> 
- <span data-ttu-id="b9e4a-2277">Un tiret</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2277">A dash</span></span> 
- <span data-ttu-id="b9e4a-2278">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2278">Six digits</span></span>

<span data-ttu-id="b9e4a-2279">Huit lettres et chiffres (nouveau format) :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2279">Eight letters and numbers (new format):</span></span>
- <span data-ttu-id="b9e4a-2280">Deux lettres dont le caractère majuscule figure à la fois dans l’alphabet grec et l’alphabet latin (ABEZHIKMNOPTYX) </span><span class="sxs-lookup"><span data-stu-id="b9e4a-2280">Two letters whose uppercase character occurs in both the Greek and Latin alphabets (ABEZHIKMNOPTYX)</span></span> 
- <span data-ttu-id="b9e4a-2281">Un tiret</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2281">A dash</span></span> 
- <span data-ttu-id="b9e4a-2282">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2282">Six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-2283">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2283">Checksum</span></span>

<span data-ttu-id="b9e4a-2284">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2284">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-2285">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2285">Definition</span></span>

<span data-ttu-id="b9e4a-2286">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2286">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-2287">L’expression régulière Regex_greece_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2287">The regular expression Regex_greece_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-2288">Un mot clé figurant dans la liste Keyword_greece_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2288">A keyword from Keyword_greece_id_card is found.</span></span>

```
<!-- Greece National ID Card -->
<Entity id="82568215-1da1-46d3-874a-d2294d81b5ac" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_greece_id_card"/>
     <Match idRef="Keyword_greece_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b9e4a-2289">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2289">Keywords</span></span>

#### <a name="keyword_greece_id_card"></a><span data-ttu-id="b9e4a-2290">Keyword_greece_id_card</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2290">Keyword_greece_id_card</span></span>

- <span data-ttu-id="b9e4a-2291">Greek identity Card</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2291">Greek identity Card</span></span>
- <span data-ttu-id="b9e4a-2292">Tautotita</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2292">Tautotita</span></span>
- <span data-ttu-id="b9e4a-2293">Δελτίο αστυνομικής ταυτότητας</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2293">Δελτίο αστυνομικής ταυτότητας</span></span>
- <span data-ttu-id="b9e4a-2294">Ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2294">Ταυτότητα</span></span>
   
## <a name="hong-kong-identity-card-hkid-number"></a><span data-ttu-id="b9e4a-2295">Numéro de carte d’identité (HKID) Hong Kong</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2295">Hong Kong Identity Card (HKID) Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-2296">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2296">Format</span></span>

<span data-ttu-id="b9e4a-2297">Combinaison de 8 ou 9 lettres et chiffres plus éventuellement des parenthèses autour du dernier caractère</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2297">Combination of 8-9 letters and numbers plus optional parentheses around the final character</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-2298">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2298">Pattern</span></span>

<span data-ttu-id="b9e4a-2299">Combinaison de 8 ou 9 lettres :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2299">Combination of 8-9 letters:</span></span>
- <span data-ttu-id="b9e4a-2300">1 ou 2 lettres (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="b9e4a-2300">1-2 letters (not case sensitive)</span></span> 
- <span data-ttu-id="b9e4a-2301">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2301">Six digits</span></span> 
- <span data-ttu-id="b9e4a-2302">Le dernier caractère (un chiffre ou la lettre A), qui est le chiffre de contrôle et est éventuellement entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2302">The final character (any digit or the letter A), which is the check digit and is optionally enclosed in parentheses.</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-2303">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2303">Checksum</span></span>

<span data-ttu-id="b9e4a-2304">Oui</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2304">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-2305">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2305">Definition</span></span>

<span data-ttu-id="b9e4a-2306">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2306">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-2307">La fonction Func_hong_kong_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2307">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-2308">Un mot clé figurant dans la liste Keyword_hong_kong_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2308">A keyword from Keyword_hong_kong_id_card is found.</span></span>
- <span data-ttu-id="b9e4a-2309">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2309">The checksum passes.</span></span>

<span data-ttu-id="b9e4a-2310">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2310">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-2311">La fonction Func_hong_kong_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2311">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-2312">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2312">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-2313">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2313">Keywords</span></span>

#### <a name="keyword_hong_kong_id_card"></a><span data-ttu-id="b9e4a-2314">Keyword_hong_kong_id_card</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2314">Keyword_hong_kong_id_card</span></span>

- <span data-ttu-id="b9e4a-2315">carte d’identité de Hong Kong</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2315">hong kong identity card</span></span>
- <span data-ttu-id="b9e4a-2316">HKIDC</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2316">HKIDC</span></span>
- <span data-ttu-id="b9e4a-2317">carte d’identité</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2317">id card</span></span>
- <span data-ttu-id="b9e4a-2318">Carte d’identité</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2318">identity card</span></span>
- <span data-ttu-id="b9e4a-2319">carte d’identité HK</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2319">hk identity card</span></span>
- <span data-ttu-id="b9e4a-2320">ID Hong Kong</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2320">hong kong id</span></span>
- <span data-ttu-id="b9e4a-2321">香港身份證</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2321">香港身份證</span></span>
- <span data-ttu-id="b9e4a-2322">香港永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2322">香港永久性居民身份證</span></span>
- <span data-ttu-id="b9e4a-2323">身份證</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2323">身份證</span></span>
- <span data-ttu-id="b9e4a-2324">身份証</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2324">身份証</span></span>
- <span data-ttu-id="b9e4a-2325">身分證</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2325">身分證</span></span>
- <span data-ttu-id="b9e4a-2326">身分証</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2326">身分証</span></span>
- <span data-ttu-id="b9e4a-2327">香港身份証</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2327">香港身份証</span></span>
- <span data-ttu-id="b9e4a-2328">香港身分證</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2328">香港身分證</span></span>
- <span data-ttu-id="b9e4a-2329">香港身分証</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2329">香港身分証</span></span>
- <span data-ttu-id="b9e4a-2330">香港身份證</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2330">香港身份證</span></span>
- <span data-ttu-id="b9e4a-2331">香港居民身份證</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2331">香港居民身份證</span></span>
- <span data-ttu-id="b9e4a-2332">香港居民身份証</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2332">香港居民身份証</span></span>
- <span data-ttu-id="b9e4a-2333">香港居民身分證</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2333">香港居民身分證</span></span>
- <span data-ttu-id="b9e4a-2334">香港居民身分証</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2334">香港居民身分証</span></span>
- <span data-ttu-id="b9e4a-2335">香港永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2335">香港永久性居民身份証</span></span>
- <span data-ttu-id="b9e4a-2336">香港永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2336">香港永久性居民身分證</span></span>
- <span data-ttu-id="b9e4a-2337">香港永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2337">香港永久性居民身分証</span></span>
- <span data-ttu-id="b9e4a-2338">香港永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2338">香港永久性居民身份證</span></span>
- <span data-ttu-id="b9e4a-2339">香港非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2339">香港非永久性居民身份證</span></span>
- <span data-ttu-id="b9e4a-2340">香港非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2340">香港非永久性居民身份証</span></span>
- <span data-ttu-id="b9e4a-2341">香港非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2341">香港非永久性居民身分證</span></span>
- <span data-ttu-id="b9e4a-2342">香港非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2342">香港非永久性居民身分証</span></span>
- <span data-ttu-id="b9e4a-2343">香港特別行政區永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2343">香港特別行政區永久性居民身份證</span></span>
- <span data-ttu-id="b9e4a-2344">香港特別行政區永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2344">香港特別行政區永久性居民身份証</span></span>
- <span data-ttu-id="b9e4a-2345">香港特別行政區永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2345">香港特別行政區永久性居民身分證</span></span>
- <span data-ttu-id="b9e4a-2346">香港特別行政區永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2346">香港特別行政區永久性居民身分証</span></span>
- <span data-ttu-id="b9e4a-2347">香港特別行政區非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2347">香港特別行政區非永久性居民身份證</span></span>
- <span data-ttu-id="b9e4a-2348">香港特別行政區非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2348">香港特別行政區非永久性居民身份証</span></span>
- <span data-ttu-id="b9e4a-2349">香港特別行政區非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2349">香港特別行政區非永久性居民身分證</span></span>
- <span data-ttu-id="b9e4a-2350">香港特別行政區非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2350">香港特別行政區非永久性居民身分証</span></span>
   
## <a name="india-permanent-account-number-pan"></a><span data-ttu-id="b9e4a-2351">Numéro de compte permanent Inde</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2351">India Permanent Account Number (PAN)</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-2352">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2352">Format</span></span>

<span data-ttu-id="b9e4a-2353">10 lettres ou chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2353">10 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-2354">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2354">Pattern</span></span>

<span data-ttu-id="b9e4a-2355">10 lettres ou chiffres :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2355">10 letters or digits:</span></span>
- <span data-ttu-id="b9e4a-2356">Cinq lettres (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="b9e4a-2356">Five letters (not case sensitive)</span></span> 
- <span data-ttu-id="b9e4a-2357">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2357">Four digits</span></span> 
- <span data-ttu-id="b9e4a-2358">Une lettre qui est un chiffre de contrôle alphabétique</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2358">A letter which is an alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-2359">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2359">Checksum</span></span>

<span data-ttu-id="b9e4a-2360">Oui</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2360">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-2361">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2361">Definition</span></span>

<span data-ttu-id="b9e4a-2362">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2362">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-2363">L’expression régulière Regex_india_permanent_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2363">The regular expression Regex_india_permanent_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-2364">Un mot clé figurant dans la liste Keyword_india_permanent_account_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2364">A keyword from Keyword_india_permanent_account_number is found.</span></span>
- <span data-ttu-id="b9e4a-2365">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2365">The checksum passes.</span></span>

```
<!-- India Permanent Account Number -->
<Entity id="2602bfee-9bb0-47a5-a7a6-2bf3053e2804" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_india_permanent_account_number"/>
     <Match idRef="Keyword_india_permanent_account_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b9e4a-2366">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2366">Keywords</span></span>

#### <a name="keyword_india_permanent_account_number"></a><span data-ttu-id="b9e4a-2367">Keyword_india_permanent_account_number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2367">Keyword_india_permanent_account_number</span></span>

- <span data-ttu-id="b9e4a-2368">Permanent Account Number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2368">Permanent Account Number</span></span> 
- <span data-ttu-id="b9e4a-2369">PANEUROPÉENNES</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2369">PAN</span></span> 
   
## <a name="india-unique-identification-aadhaar-number"></a><span data-ttu-id="b9e4a-2370">Numéro d’identification unique (Aadhaar) Inde</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2370">India Unique Identification (Aadhaar) Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-2371">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2371">Format</span></span>

<span data-ttu-id="b9e4a-2372">12 chiffres contenant éventuellement des espaces ou des tirets</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2372">12 digits containing optional spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-2373">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2373">Pattern</span></span>

<span data-ttu-id="b9e4a-2374">12 chiffres :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2374">12 digits:</span></span>
- <span data-ttu-id="b9e4a-2375">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2375">Four digits</span></span> 
- <span data-ttu-id="b9e4a-2376">Éventuellement un tiret ou un espace </span><span class="sxs-lookup"><span data-stu-id="b9e4a-2376">An optional space or dash</span></span> 
- <span data-ttu-id="b9e4a-2377">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2377">Four digits</span></span> 
- <span data-ttu-id="b9e4a-2378">Éventuellement un tiret ou un espace </span><span class="sxs-lookup"><span data-stu-id="b9e4a-2378">An optional space or dash</span></span> 
- <span data-ttu-id="b9e4a-2379">Le chiffre final, qui est le chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2379">The final digit which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-2380">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2380">Checksum</span></span>

<span data-ttu-id="b9e4a-2381">Oui</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2381">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-2382">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2382">Definition</span></span>

<span data-ttu-id="b9e4a-2383">Une stratégie DLP est sûre à 85% d’avoir détecté ce type d’informations sensibles si, dans une proximité de 300 caractères: la fonction Func_india_aadhaar trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2383">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern.</span></span>
<span data-ttu-id="b9e4a-2384">Un mot clé figurant dans la liste Keyword_india_aadhar est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2384">A keyword from Keyword_india_aadhar is found.</span></span>
<span data-ttu-id="b9e4a-2385">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2385">The checksum passes.</span></span>
<span data-ttu-id="b9e4a-2386">Une stratégie DLP est sûre à 75% d’avoir détecté ce type d’informations sensibles si, dans une proximité de 300 caractères: la fonction Func_india_aadhaar trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2386">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern.</span></span>
<span data-ttu-id="b9e4a-2387">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2387">The checksum passes.</span></span>
<!-- India Unique Identification (Aadhaar) number -->
<span data-ttu-id="b9e4a-2388"><Entity id="1ca46b29-76f5-4f46-9383-cfa15e91048f" recommendedConfidence="85" patternsProximity="300"> <Pattern confidenceLevel="85"> <IdMatch idRef="Func_india_aadhaar"/> <Match idRef="Keyword_india_aadhar"/> </Pattern> <Pattern confidenceLevel="75"> <IdMatch idRef="Func_india_aadhaar"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="b9e4a-2388"></span></span>

### <a name="keywords"></a><span data-ttu-id="b9e4a-2389">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2389">Keywords</span></span>
   
#### <a name="keyword_india_aadhar"></a><span data-ttu-id="b9e4a-2390">Keyword_india_aadhar</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2390">Keyword_india_aadhar</span></span>
- <span data-ttu-id="b9e4a-2391">Aadhar</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2391">Aadhar</span></span>
- <span data-ttu-id="b9e4a-2392">Aadhaar</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2392">Aadhaar</span></span>
- <span data-ttu-id="b9e4a-2393">UID</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2393">UID</span></span>
- <span data-ttu-id="b9e4a-2394">आधार</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2394">आधार</span></span>
   
## <a name="indonesia-identity-card-ktp-number"></a><span data-ttu-id="b9e4a-2395">Numéro de carte d’identité (KTP) Indonésie</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2395">Indonesia Identity Card (KTP) Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-2396">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2396">Format</span></span>

<span data-ttu-id="b9e4a-2397">16 chiffres contenant éventuellement des points</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2397">16 digits containing optional periods</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-2398">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2398">Pattern</span></span>

<span data-ttu-id="b9e4a-2399">16 chiffres :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2399">16 digits:</span></span>
- <span data-ttu-id="b9e4a-2400">Code à deux chiffres désignant la province </span><span class="sxs-lookup"><span data-stu-id="b9e4a-2400">Two-digit province code</span></span> 
- <span data-ttu-id="b9e4a-2401">Un point (facultatif) </span><span class="sxs-lookup"><span data-stu-id="b9e4a-2401">A period (optional)</span></span> 
- <span data-ttu-id="b9e4a-2402">Code à deux chiffres désignant une régence ou une ville </span><span class="sxs-lookup"><span data-stu-id="b9e4a-2402">Two-digit regency or city code</span></span> 
- <span data-ttu-id="b9e4a-2403">Code à deux chiffres désignant un sous-district </span><span class="sxs-lookup"><span data-stu-id="b9e4a-2403">Two-digit subdistrict code</span></span> 
- <span data-ttu-id="b9e4a-2404">Un point (facultatif) </span><span class="sxs-lookup"><span data-stu-id="b9e4a-2404">A period (optional)</span></span> 
- <span data-ttu-id="b9e4a-2405">Six chiffres au format JJMMAA qui correspondent à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="b9e4a-2405">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="b9e4a-2406">Un point (facultatif) </span><span class="sxs-lookup"><span data-stu-id="b9e4a-2406">A period (optional)</span></span> 
- <span data-ttu-id="b9e4a-2407">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2407">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-2408">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2408">Checksum</span></span>

<span data-ttu-id="b9e4a-2409">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2409">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-2410">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2410">Definition</span></span>

<span data-ttu-id="b9e4a-2411">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2411">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-2412">L’expression régulière Regex_indonesia_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2412">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-2413">Un mot clé figurant dans la liste Keyword_indonesia_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2413">A keyword from Keyword_indonesia_id_card is found.</span></span>

<span data-ttu-id="b9e4a-2414">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2414">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-2415">L’expression régulière Regex_indonesia_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2415">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-2416">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2416">Keywords</span></span>
   
#### <a name="keyword_indonesia_id_card"></a><span data-ttu-id="b9e4a-2417">Keyword_indonesia_id_card</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2417">Keyword_indonesia_id_card</span></span>

- <span data-ttu-id="b9e4a-2418">KTP</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2418">KTP</span></span>
- <span data-ttu-id="b9e4a-2419">Kartu Tanda Penduduk</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2419">Kartu Tanda Penduduk</span></span> 
- <span data-ttu-id="b9e4a-2420">Nomor Induk Kependudukan</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2420">Nomor Induk Kependudukan</span></span> 
   
## <a name="international-banking-account-number-iban"></a><span data-ttu-id="b9e4a-2421">Numéro de compte bancaire international (IBAN)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2421">International Banking Account Number (IBAN)</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-2422">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2422">Format</span></span>

<span data-ttu-id="b9e4a-2423">Code pays (à deux lettres) plus chiffres de contrôle (à deux chiffres) plus numéro BBAN (jusqu’à 30 chiffres)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2423">Country code (two letters) plus check digits (two digits) plus bban number (up to 30 characters)</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-2424">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2424">Pattern</span></span>

<span data-ttu-id="b9e4a-2425">Le modèle doit inclure tous les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2425">Pattern must include all of the following:</span></span>

- <span data-ttu-id="b9e4a-2426">Code pays à deux lettres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2426">Two-letter country code</span></span>
- <span data-ttu-id="b9e4a-2427">Deux chiffres de contrôle (suivis d’un espace facultatif) </span><span class="sxs-lookup"><span data-stu-id="b9e4a-2427">Two check digits (followed by an optional space)</span></span> 
- <span data-ttu-id="b9e4a-2428">1 à 7 groupes de quatre lettres ou chiffres (séparés par des espaces facultatifs)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2428">1-7 groups of four letters or digits (can be separated by spaces)</span></span>
- <span data-ttu-id="b9e4a-2429">1 à 3 lettres ou chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2429">1-3 letters or digits</span></span>

<span data-ttu-id="b9e4a-p135">Le format pour chaque pays est légèrement différent. Le type d’informations sensibles IBAN recouvre ces 60 pays :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-p135">The format for each country is slightly different. The IBAN sensitive information type covers these 60 countries:</span></span>

<span data-ttu-id="b9e4a-2432">ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2432">ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-2433">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2433">Checksum</span></span>

<span data-ttu-id="b9e4a-2434">Oui</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2434">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-2435">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2435">Definition</span></span>

<span data-ttu-id="b9e4a-2436">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2436">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-2437">La fonction Func_iban trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2437">The function Func_iban finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-2438">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2438">The checksum passes.</span></span>

```
<Entity id="e7dc4711-11b7-4cb0-b88b-2c394a771f0e" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_iban" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b9e4a-2439">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2439">Keywords</span></span>

<span data-ttu-id="b9e4a-2440">Aucun</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2440">None</span></span>

   
## <a name="ip-address"></a><span data-ttu-id="b9e4a-2441">Adresse IP</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2441">IP Address</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-2442">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2442">Format</span></span>

#### <a name="ipv4"></a><span data-ttu-id="b9e4a-2443">IPv6</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2443">IPv4:</span></span>
<span data-ttu-id="b9e4a-2444">Modèle complexe qui tient compte des versions mises en forme (points) et non mises en forme (sans points) des adresses IPv4</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2444">Complex pattern which accounts for formatted (periods) and unformatted (no periods) versions of the IPv4 addresses</span></span>

#### <a name="ipv6"></a><span data-ttu-id="b9e4a-2445">IPv4/IPv6</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2445">IPv6:</span></span>
<span data-ttu-id="b9e4a-2446"> Modèle complexe qui tient compte des numéros IPv6 mis en forme (qui incluent les signes deux-points)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2446">Complex pattern which accounts for formatted IPv6 numbers (which include colons)</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-2447">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2447">Pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-2448">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2448">Checksum</span></span>

<span data-ttu-id="b9e4a-2449">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2449">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-2450">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2450">Definition</span></span>

<span data-ttu-id="b9e4a-2451">Pour IPv6, le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2451">For IPv6, a DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-2452">L’expression régulière Regex_ipv6_address trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2452">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-2453">Aucun mot clé figurant dans la liste Keyword_ipaddress n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2453">No keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="b9e4a-2454">Pour IPv4, le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 95 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2454">For IPv4, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-2455">L’expression régulière Regex_ipv4_address trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2455">The regular expression Regex_ipv4_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-2456">Un mot clé figurant dans la liste Keyword_ipaddress est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2456">A keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="b9e4a-2457">Pour IPv6, le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 95 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2457">For IPv6, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-2458">L’expression régulière Regex_ipv6_address trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2458">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-2459">Aucun mot clé figurant dans la liste Keyword_ipaddress n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2459">No keyword from Keyword_ipaddress is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-2460">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2460">Keywords</span></span>

#### <a name="keyword_ipaddress"></a><span data-ttu-id="b9e4a-2461">Keyword_ipaddress</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2461">Keyword_ipaddress</span></span>

- <span data-ttu-id="b9e4a-2462">IP (ce mot clé respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2462">IP (this keyword is case sensitive)</span></span>
- <span data-ttu-id="b9e4a-2463">ip address</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2463">ip address</span></span> 
- <span data-ttu-id="b9e4a-2464">adresses IP</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2464">ip addresses</span></span>
- <span data-ttu-id="b9e4a-2465">protocole internet</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2465">internet protocol</span></span>
- <span data-ttu-id="b9e4a-2466">IP-כתובת ה</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2466">IP-כתובת ה</span></span> 
   
## <a name="international-classification-of-diseases-icd-10-cm"></a><span data-ttu-id="b9e4a-2467">Classification internationale des maladies (ICD-10-CM)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2467">International Classification of Diseases (ICD-10-CM)</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-2468">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2468">Format</span></span>

<span data-ttu-id="b9e4a-2469">Dictionary</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2469">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-2470">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2470">Pattern</span></span>

<span data-ttu-id="b9e4a-2471">Mot clé</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2471">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-2472">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2472">Checksum</span></span>

<span data-ttu-id="b9e4a-2473">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2473">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-2474">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2474">Definition</span></span>

<span data-ttu-id="b9e4a-2475">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2475">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-2476">Un mot clé depuis Dictionary_icd_10_cm est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2476">A keyword from Dictionary_icd_10_cm is found.</span></span>

```
      <!-- ICD-10 CM -->
      <Entity id="3356946c-6bb7-449b-b253-6ffa419c0ce7" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_10_cm" />
        </Pattern>
      </Entity>
```

<span data-ttu-id="b9e4a-2477">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2477">Keywords</span></span>

<span data-ttu-id="b9e4a-2478">Tout terme du dictionnaire de mots clés Dictionary_icd_10_cm, qui est basé sur la [Classification internationale des maladies, dixième révision, modification clinique (ICD-10-cm)](https://go.microsoft.com/fwlink/?linkid=852604).</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2478">Any term from the Dictionary_icd_10_cm keyword dictionary, which is based on the [International Classification of Diseases, Tenth Revision, Clinical Modification (ICD-10-CM)](https://go.microsoft.com/fwlink/?linkid=852604).</span></span> <span data-ttu-id="b9e4a-2479">Ce type recherche uniquement le terme, pas les codes d’assurance.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2479">This type looks only for the term, not the insurance codes.</span></span>

   
## <a name="international-classification-of-diseases-icd-9-cm"></a><span data-ttu-id="b9e4a-2480">Classification internationale des maladies (ICD-9-CM)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2480">International Classification of Diseases (ICD-9-CM)</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-2481">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2481">Format</span></span>

<span data-ttu-id="b9e4a-2482">Dictionary</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2482">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-2483">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2483">Pattern</span></span>

<span data-ttu-id="b9e4a-2484">Mot clé</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2484">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-2485">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2485">Checksum</span></span>

<span data-ttu-id="b9e4a-2486">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2486">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-2487">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2487">Definition</span></span>

<span data-ttu-id="b9e4a-2488">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2488">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-2489">Un mot clé depuis Dictionary_icd_9_cm est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2489">A keyword from Dictionary_icd_9_cm is found.</span></span>

```
      <Entity id="fa3f9c74-ee07-4c52-b5f2-085d6b2c0ec4" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_9_cm" />
        </Pattern>
      </Entity>
```

### <a name="keywords"></a><span data-ttu-id="b9e4a-2490">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2490">Keywords</span></span>

<span data-ttu-id="b9e4a-2491">Tout terme du dictionnaire de mots clés Dictionary_icd_9_cm, qui est basé sur la [Classification internationale des maladies, neuvième révision, modification clinique (ICD-9-cm)](https://go.microsoft.com/fwlink/?linkid=852605).</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2491">Any term from the Dictionary_icd_9_cm keyword dictionary, which is based on the [International Classification of Diseases,Ninth Revision, Clinical Modification (ICD-9-CM)](https://go.microsoft.com/fwlink/?linkid=852605).</span></span> <span data-ttu-id="b9e4a-2492">Ce type recherche uniquement le terme, pas les codes d’assurance.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2492">This type looks only for the term, not the insurance codes.</span></span>
   
## <a name="ireland-personal-public-service-pps-number"></a><span data-ttu-id="b9e4a-2493">Numéro de service public personnel (PPS) Irlande</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2493">Ireland Personal Public Service (PPS) Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-2494">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2494">Format</span></span>

<span data-ttu-id="b9e4a-2495">Ancien format (jusqu’au 31 décembre 2012):</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2495">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="b9e4a-2496">Sept chiffres suivis de 1 ou 2 lettres </span><span class="sxs-lookup"><span data-stu-id="b9e4a-2496">Seven digits followed by 1-2 letters</span></span> 

<span data-ttu-id="b9e4a-2497">Nouveau format (1er janvier 2013 et après):</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2497">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="b9e4a-2498">Sept chiffres suivis de deux lettres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2498">Seven digits followed by two letters</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-2499">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2499">Pattern</span></span>

<span data-ttu-id="b9e4a-2500">Ancien format (jusqu’au 31 décembre 2012):</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2500">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="b9e4a-2501">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="b9e4a-2501">Seven digits</span></span> 
- <span data-ttu-id="b9e4a-2502">1 ou 2 lettres (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="b9e4a-2502">1-2 letters (not case sensitive)</span></span> 

<span data-ttu-id="b9e4a-2503">Nouveau format (1er janvier 2013 et après):</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2503">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="b9e4a-2504">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="b9e4a-2504">Seven digits</span></span> 
- <span data-ttu-id="b9e4a-2505">Une lettre (ne respectant pas la casse), qui est un chiffre de contrôle alphabétique </span><span class="sxs-lookup"><span data-stu-id="b9e4a-2505">A letter (not case sensitive) which is an alphabetic check digit</span></span> 
- <span data-ttu-id="b9e4a-2506">La lettre « A » ou « H » (ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2506">The letter "A" or "H" (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-2507">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2507">Checksum</span></span>

<span data-ttu-id="b9e4a-2508">Oui</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2508">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-2509">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2509">Definition</span></span>

<span data-ttu-id="b9e4a-2510">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2510">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-2511">La fonction Func_ireland_pps trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2511">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-2512">L’une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2512">One of the following is true:</span></span>
    - <span data-ttu-id="b9e4a-2513">Un mot clé figurant dans la liste Keyword_ireland_pps est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2513">A keyword from Keyword_ireland_pps is found.</span></span>
    - <span data-ttu-id="b9e4a-2514">La fonction Func_eu_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2514">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="b9e4a-2515">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2515">The checksum passes.</span></span>

<span data-ttu-id="b9e4a-2516">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2516">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-2517">La fonction Func_ireland_pps trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2517">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-2518">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2518">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-2519">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2519">Keywords</span></span>

#### <a name="keyword_ireland_pps"></a><span data-ttu-id="b9e4a-2520">Keyword_ireland_pps</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2520">Keyword_ireland_pps</span></span>

- <span data-ttu-id="b9e4a-2521">Personal Public Service Number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2521">Personal Public Service Number</span></span> 
- <span data-ttu-id="b9e4a-2522">PPS Number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2522">PPS Number</span></span> 
- <span data-ttu-id="b9e4a-2523">PPS Num</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2523">PPS Num</span></span> 
- <span data-ttu-id="b9e4a-2524">PPS No.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2524">PPS No.</span></span> 
- <span data-ttu-id="b9e4a-2525">PPS #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2525">PPS #</span></span> 
- <span data-ttu-id="b9e4a-2526">Spa #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2526">PPS#</span></span> 
- <span data-ttu-id="b9e4a-2527">PPSN</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2527">PPSN</span></span> 
- <span data-ttu-id="b9e4a-2528">Public Services Card</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2528">Public Services Card</span></span> 
- <span data-ttu-id="b9e4a-2529">Uimhir Phearsanta Seirbhíse Poiblí</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2529">Uimhir Phearsanta Seirbhíse Poiblí</span></span> 
- <span data-ttu-id="b9e4a-2530">Uimh.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2530">Uimh.</span></span> <span data-ttu-id="b9e4a-2531">TOXINE</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2531">PSP</span></span> 
- <span data-ttu-id="b9e4a-2532">TOXINE</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2532">PSP</span></span> 
   
## <a name="israel-bank-account-number"></a><span data-ttu-id="b9e4a-2533">Numéro de compte bancaire Israël</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2533">Israel Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-2534">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2534">Format</span></span>

<span data-ttu-id="b9e4a-2535">13 chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2535">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-2536">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2536">Pattern</span></span>

<span data-ttu-id="b9e4a-2537">Avec</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2537">Formatted:</span></span>
- <span data-ttu-id="b9e4a-2538">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2538">Two digits</span></span> 
- <span data-ttu-id="b9e4a-2539">Un tiret</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2539">A dash</span></span> 
- <span data-ttu-id="b9e4a-2540">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2540">Three digits</span></span> 
- <span data-ttu-id="b9e4a-2541">Un tiret</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2541">A dash</span></span> 
- <span data-ttu-id="b9e4a-2542">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2542">Eight digits</span></span>

<span data-ttu-id="b9e4a-2543">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2543">Unformatted:</span></span>
- <span data-ttu-id="b9e4a-2544">	13 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2544">13 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-2545">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2545">Checksum</span></span>

<span data-ttu-id="b9e4a-2546">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2546">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-2547">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2547">Definition</span></span>

<span data-ttu-id="b9e4a-2548">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2548">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-2549">L’expression régulière Regex_israel_bank_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2549">The regular expression Regex_israel_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-2550">Un mot clé figurant dans la liste Keyword_israel_bank_account_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2550">A keyword from Keyword_israel_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-2551">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2551">Keywords</span></span>

#### <a name="keyword_israel_bank_account_number"></a><span data-ttu-id="b9e4a-2552">Keyword_israel_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2552">Keyword_israel_bank_account_number</span></span>

- <span data-ttu-id="b9e4a-2553">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2553">Bank Account Number</span></span> 
- <span data-ttu-id="b9e4a-2554">Bank Account</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2554">Bank Account</span></span> 
- <span data-ttu-id="b9e4a-2555">Numéro de compte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2555">Account Number</span></span> 
- <span data-ttu-id="b9e4a-2556">מספר חשבון בנק</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2556">מספר חשבון בנק</span></span> 
   
## <a name="israel-national-id"></a><span data-ttu-id="b9e4a-2557">Carte nationale d’identité Israël</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2557">Israel National ID</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-2558">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2558">Format</span></span>

<span data-ttu-id="b9e4a-2559">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2559">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-2560">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2560">Pattern</span></span>

<span data-ttu-id="b9e4a-2561">Neuf chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2561">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-2562">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2562">Checksum</span></span>

<span data-ttu-id="b9e4a-2563">Oui</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2563">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-2564">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2564">Definition</span></span>

<span data-ttu-id="b9e4a-2565">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2565">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-2566">La fonction Func_israeli_national_id_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2566">The function Func_israeli_national_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-2567">Un mot clé figurant dans la liste Keyword_Israel_National_ID est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2567">A keyword from Keyword_Israel_National_ID is found.</span></span>
- <span data-ttu-id="b9e4a-2568">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2568">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-2569">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2569">Keywords</span></span>

#### <a name="keyword_israel_national_id"></a><span data-ttu-id="b9e4a-2570">Keyword_Israel_National_ID</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2570">Keyword_Israel_National_ID</span></span>

- <span data-ttu-id="b9e4a-2571">מספר זהות</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2571">מספר זהות</span></span> 
- <span data-ttu-id="b9e4a-2572">Numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2572">National ID Number</span></span>
   
## <a name="italy-drivers-license-number"></a><span data-ttu-id="b9e4a-2573">Numéro de permis de conduire Italie</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2573">Italy Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-2574">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2574">Format</span></span>

<span data-ttu-id="b9e4a-2575">Une combinaison de 10 lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2575">A combination of 10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-2576">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2576">Pattern</span></span>

- <span data-ttu-id="b9e4a-2577">Une combinaison de 10 lettres et chiffres :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2577">A combination of 10 letters and digits:</span></span>
- <span data-ttu-id="b9e4a-2578">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2578">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="b9e4a-2579">La lettre « A » ou « V » (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2579">The letter "A" or "V" (not case sensitive)</span></span> 
- <span data-ttu-id="b9e4a-2580">Sept lettres (ne respectent pas la casse), des chiffres ou le trait de soulignement</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2580">Seven letters (not case sensitive), digits, or the underscore character</span></span> 
- <span data-ttu-id="b9e4a-2581">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2581">One letter (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-2582">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2582">Checksum</span></span>

<span data-ttu-id="b9e4a-2583">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2583">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-2584">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2584">Definition</span></span>

<span data-ttu-id="b9e4a-2585">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2585">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-2586">L’expression régulière Regex_italy_drivers_license_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2586">The regular expression Regex_italy_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-2587">Un mot clé figurant dans la liste Keyword_italy_drivers_license_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2587">A keyword from Keyword_italy_drivers_license_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-2588">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2588">Keywords</span></span>

#### <a name="keyword_italy_drivers_license_number"></a><span data-ttu-id="b9e4a-2589">Keyword_italy_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2589">Keyword_italy_drivers_license_number</span></span>

- <span data-ttu-id="b9e4a-2590">numero di patente di guida</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2590">numero di patente di guida</span></span> 
- <span data-ttu-id="b9e4a-2591">patente di guida</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2591">patente di guida</span></span> 
   
## <a name="japan-bank-account-number"></a><span data-ttu-id="b9e4a-2592">Numéro de compte bancaire Japon</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2592">Japan Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-2593">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2593">Format</span></span>

<span data-ttu-id="b9e4a-2594">Sept ou huit chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2594">Seven or eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-2595">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2595">Pattern</span></span>

<span data-ttu-id="b9e4a-2596">Numéro de compte bancaire :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2596">Bank account number:</span></span>
- <span data-ttu-id="b9e4a-2597">Sept ou huit chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2597">Seven or eight digits</span></span>
- <span data-ttu-id="b9e4a-2598">Code guichet du compte bancaire :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2598">Bank account branch code:</span></span>
- <span data-ttu-id="b9e4a-2599">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2599">Four digits</span></span> 
- <span data-ttu-id="b9e4a-2600">Un espace ou un tiret (facultatif)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2600">A space or dash (optional)</span></span> 
- <span data-ttu-id="b9e4a-2601">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2601">Three digits</span></span>

<span data-ttu-id="b9e4a-2602">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2602">Checksum</span></span>

<span data-ttu-id="b9e4a-2603">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2603">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-2604">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2604">Definition</span></span>

<span data-ttu-id="b9e4a-2605">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2605">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-2606">La fonction Func_jp_bank_account trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2606">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-2607">Un mot clé figurant dans la liste Keyword_jp_bank_account est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2607">A keyword from Keyword_jp_bank_account is found.</span></span>
- <span data-ttu-id="b9e4a-2608">L’une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2608">One of the following is true:</span></span>
- <span data-ttu-id="b9e4a-2609">La fonction Func_jp_bank_account_branch_code trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2609">The function Func_jp_bank_account_branch_code finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-2610">Un mot clé figurant dans la liste Keyword_jp_bank_branch_code est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2610">A keyword from Keyword_jp_bank_branch_code is found.</span></span>

<span data-ttu-id="b9e4a-2611">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2611">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-2612">La fonction Func_jp_bank_account trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2612">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-2613">Un mot clé figurant dans la liste Keyword_jp_bank_account est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2613">A keyword from Keyword_jp_bank_account is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-2614">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2614">Keywords</span></span>

#### <a name="keyword_jp_bank_account"></a><span data-ttu-id="b9e4a-2615">Keyword_jp_bank_account</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2615">Keyword_jp_bank_account</span></span>

- <span data-ttu-id="b9e4a-2616">Numéro de compte courant</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2616">Checking Account Number</span></span> 
- <span data-ttu-id="b9e4a-2617">Compte courant</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2617">Checking Account</span></span> 
- <span data-ttu-id="b9e4a-2618"># compte courant</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2618">Checking Account #</span></span> 
- <span data-ttu-id="b9e4a-2619">Numéro compte courant</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2619">Checking Acct Number</span></span> 
- <span data-ttu-id="b9e4a-2620"># compte courant</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2620">Checking Acct #</span></span> 
- <span data-ttu-id="b9e4a-2621">N° de compte courant</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2621">Checking Acct No.</span></span> 
- <span data-ttu-id="b9e4a-2622">N° de compte courant</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2622">Checking Account No.</span></span> 
- <span data-ttu-id="b9e4a-2623">Numéro de compte bancaire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2623">Bank Account Number</span></span> 
- <span data-ttu-id="b9e4a-2624">Compte bancaire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2624">Bank Account</span></span> 
- <span data-ttu-id="b9e4a-2625"># Compte bancaire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2625">Bank Account #</span></span> 
- <span data-ttu-id="b9e4a-2626">Numéro de compte bancaire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2626">Bank Acct Number</span></span> 
- <span data-ttu-id="b9e4a-2627"># Compte bancaire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2627">Bank Acct #</span></span> 
- <span data-ttu-id="b9e4a-2628">N° de compte bancaire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2628">Bank Acct No.</span></span> 
- <span data-ttu-id="b9e4a-2629">N° de compte bancaire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2629">Bank Account No.</span></span> 
- <span data-ttu-id="b9e4a-2630">Numéro de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2630">Savings Account Number</span></span> 
- <span data-ttu-id="b9e4a-2631">Compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2631">Savings Account</span></span> 
- <span data-ttu-id="b9e4a-2632">N° de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2632">Savings Account #</span></span> 
- <span data-ttu-id="b9e4a-2633">Numéro de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2633">Savings Acct Number</span></span> 
- <span data-ttu-id="b9e4a-2634"># compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2634">Savings Acct #</span></span> 
- <span data-ttu-id="b9e4a-2635">N° de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2635">Savings Acct No.</span></span> 
- <span data-ttu-id="b9e4a-2636">N° de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2636">Savings Account No.</span></span> 
- <span data-ttu-id="b9e4a-2637">Numéro de compte de débit</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2637">Debit Account Number</span></span> 
- <span data-ttu-id="b9e4a-2638">Compte de débit</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2638">Debit Account</span></span> 
- <span data-ttu-id="b9e4a-2639"># Compte de débit</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2639">Debit Account #</span></span> 
- <span data-ttu-id="b9e4a-2640">Numéro de compte de débit</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2640">Debit Acct Number</span></span> 
- <span data-ttu-id="b9e4a-2641"># Compte de débit</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2641">Debit Acct #</span></span> 
- <span data-ttu-id="b9e4a-2642">N° de compte de débit</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2642">Debit Acct No.</span></span> 
- <span data-ttu-id="b9e4a-2643">N° de compte de débit</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2643">Debit Account No.</span></span> 
- <span data-ttu-id="b9e4a-2644">口座番号を当座預金口座の確認</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2644">口座番号を当座預金口座の確認</span></span> 
- <span data-ttu-id="b9e4a-2645">#アカウントの確認 、 勘定番号の確認</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2645">＃アカウントの確認、勘定番号の確認</span></span> 
- <span data-ttu-id="b9e4a-2646">#勘定の確認</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2646">＃勘定の確認</span></span> 
- <span data-ttu-id="b9e4a-2647">勘定番号の確認</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2647">勘定番号の確認</span></span> 
- <span data-ttu-id="b9e4a-2648">口座番号の確認</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2648">口座番号の確認</span></span> 
- <span data-ttu-id="b9e4a-2649">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2649">銀行口座番号</span></span> 
- <span data-ttu-id="b9e4a-2650">銀行口座</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2650">銀行口座</span></span> 
- <span data-ttu-id="b9e4a-2651">銀行口座＃</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2651">銀行口座＃</span></span> 
- <span data-ttu-id="b9e4a-2652">銀行の勘定番号</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2652">銀行の勘定番号</span></span> 
- <span data-ttu-id="b9e4a-2653">銀行のacct＃</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2653">銀行のacct＃</span></span> 
- <span data-ttu-id="b9e4a-2654">銀行の勘定いいえ</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2654">銀行の勘定いいえ</span></span> 
- <span data-ttu-id="b9e4a-2655">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2655">銀行口座番号</span></span>
- <span data-ttu-id="b9e4a-2656">普通預金口座番号</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2656">普通預金口座番号</span></span> 
- <span data-ttu-id="b9e4a-2657">預金口座</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2657">預金口座</span></span> 
- <span data-ttu-id="b9e4a-2658">貯蓄口座＃</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2658">貯蓄口座＃</span></span> 
- <span data-ttu-id="b9e4a-2659">貯蓄勘定の数</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2659">貯蓄勘定の数</span></span> 
- <span data-ttu-id="b9e4a-2660">貯蓄勘定＃</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2660">貯蓄勘定＃</span></span> 
- <span data-ttu-id="b9e4a-2661">貯蓄勘定番号</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2661">貯蓄勘定番号</span></span> 
- <span data-ttu-id="b9e4a-2662">普通預金口座番号</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2662">普通預金口座番号</span></span> 
- <span data-ttu-id="b9e4a-2663">引き落とし口座番号</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2663">引き落とし口座番号</span></span> 
- <span data-ttu-id="b9e4a-2664">口座番号</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2664">口座番号</span></span> 
- <span data-ttu-id="b9e4a-2665">口座番号＃</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2665">口座番号＃</span></span> 
- <span data-ttu-id="b9e4a-2666">デビットのacct番号</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2666">デビットのacct番号</span></span> 
- <span data-ttu-id="b9e4a-2667">デビット勘定＃</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2667">デビット勘定＃</span></span> 
- <span data-ttu-id="b9e4a-2668">デビットACCTの番号</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2668">デビットACCTの番号</span></span> 
- <span data-ttu-id="b9e4a-2669">デビット口座番号</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2669">デビット口座番号</span></span> 

#### <a name="keyword_jp_bank_branch_code"></a><span data-ttu-id="b9e4a-2670">Keyword_jp_bank_branch_code</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2670">Keyword_jp_bank_branch_code</span></span>

<span data-ttu-id="b9e4a-2671">Otemachi</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2671">Otemachi</span></span>

## <a name="japan-drivers-license-number"></a><span data-ttu-id="b9e4a-2672">Numéro de permis de conduire Japon</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2672">Japan Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-2673">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2673">Format</span></span>

<span data-ttu-id="b9e4a-2674">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2674">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-2675">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2675">Pattern</span></span>

<span data-ttu-id="b9e4a-2676">12 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2676">12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-2677">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2677">Checksum</span></span>

<span data-ttu-id="b9e4a-2678">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2678">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-2679">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2679">Definition</span></span>

<span data-ttu-id="b9e4a-2680">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2680">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-2681">La fonction Func_jp_drivers_license_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2681">The function Func_jp_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-2682">Un mot clé figurant dans la liste Keyword_jp_drivers_license_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2682">A keyword from Keyword_jp_drivers_license_number is found.</span></span>

```
<!-- Japan Driver's License Number -->
<Entity id="c6011143-d087-451c-8313-7f6d4aed2270" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_drivers_license_number" />
        <Match idRef ="Keyword_jp_drivers_license_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b9e4a-2683">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2683">Keywords</span></span>

#### <a name="keyword_jp_drivers_license_number"></a><span data-ttu-id="b9e4a-2684">Keyword_jp_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2684">Keyword_jp_drivers_license_number</span></span>

- <span data-ttu-id="b9e4a-2685">LD #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2685">dl#</span></span> 
- <span data-ttu-id="b9e4a-2686">LD</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2686">DL＃</span></span> 
- <span data-ttu-id="b9e4a-2687">distribution #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2687">dls#</span></span> 
- <span data-ttu-id="b9e4a-2688">DISTRIBUTION</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2688">DLS＃</span></span> 
- <span data-ttu-id="b9e4a-2689">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2689">driver license</span></span> 
- <span data-ttu-id="b9e4a-2690">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2690">driver licenses</span></span> 
- <span data-ttu-id="b9e4a-2691">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2691">drivers license</span></span> 
- <span data-ttu-id="b9e4a-2692">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2692">driver's license</span></span> 
- <span data-ttu-id="b9e4a-2693">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2693">drivers licenses</span></span> 
- <span data-ttu-id="b9e4a-2694">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2694">driver's licenses</span></span> 
- <span data-ttu-id="b9e4a-2695">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2695">driving licence</span></span> 
- <span data-ttu-id="b9e4a-2696">Profil #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2696">lic#</span></span> 
- <span data-ttu-id="b9e4a-2697">Profil</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2697">LIC＃</span></span> 
- <span data-ttu-id="b9e4a-2698">conduire #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2698">lics#</span></span> 
- <span data-ttu-id="b9e4a-2699">id d’état</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2699">state id</span></span> 
- <span data-ttu-id="b9e4a-2700">identification d’état</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2700">state identification</span></span> 
- <span data-ttu-id="b9e4a-2701">numéro d’identification d’état</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2701">state identification number</span></span> 
- <span data-ttu-id="b9e4a-2702">低所得国＃</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2702">低所得国＃</span></span> 
- <span data-ttu-id="b9e4a-2703">免許証</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2703">免許証</span></span> 
- <span data-ttu-id="b9e4a-2704">状態ID</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2704">状態ID</span></span>
- <span data-ttu-id="b9e4a-2705">状態の識別</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2705">状態の識別</span></span> 
- <span data-ttu-id="b9e4a-2706">状態の識別番号</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2706">状態の識別番号</span></span> 
- <span data-ttu-id="b9e4a-2707">運転免許</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2707">運転免許</span></span> 
- <span data-ttu-id="b9e4a-2708">運転免許証</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2708">運転免許証</span></span> 
- <span data-ttu-id="b9e4a-2709">運転免許証番号</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2709">運転免許証番号</span></span> 
   
## <a name="japan-passport-number"></a><span data-ttu-id="b9e4a-2710">Numéro de passeport Japon</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2710">Japan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-2711">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2711">Format</span></span>

<span data-ttu-id="b9e4a-2712">Deux lettres suivies de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2712">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-2713">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2713">Pattern</span></span>

<span data-ttu-id="b9e4a-2714">Deux lettres (ne respectant pas la casse) suivies de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2714">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-2715">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2715">Checksum</span></span>

<span data-ttu-id="b9e4a-2716">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2716">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-2717">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2717">Definition</span></span>

<span data-ttu-id="b9e4a-2718">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2718">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-2719">La fonction Func_jp_passport trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2719">The function Func_jp_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-2720">Un mot clé figurant dans la liste Keyword_jp_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2720">A keyword from Keyword_jp_passport is found.</span></span>

```
<!-- Japan Passport Number -->
<Entity id="75177310-1a09-4613-bf6d-833aae3743f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_passport" />
        <Match idRef="Keyword_jp_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b9e4a-2721">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2721">Keywords</span></span>

#### <a name="keyword_jp_passport"></a><span data-ttu-id="b9e4a-2722">Keyword_jp_passport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2722">Keyword_jp_passport</span></span>

- <span data-ttu-id="b9e4a-2723">パスポート</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2723">パスポート</span></span> 
- <span data-ttu-id="b9e4a-2724">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2724">パスポート番号</span></span> 
- <span data-ttu-id="b9e4a-2725">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2725">パスポートのNum</span></span> 
- <span data-ttu-id="b9e4a-2726">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2726">パスポート＃</span></span> 
   
## <a name="japan-resident-registration-number"></a><span data-ttu-id="b9e4a-2727">Matricule de résident Japon</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2727">Japan Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-2728">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2728">Format</span></span>

<span data-ttu-id="b9e4a-2729">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2729">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-2730">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2730">Pattern</span></span>

<span data-ttu-id="b9e4a-2731">11 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2731">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-2732">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2732">Checksum</span></span>

<span data-ttu-id="b9e4a-2733">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2733">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-2734">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2734">Definition</span></span>

<span data-ttu-id="b9e4a-2735">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2735">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-2736">La fonction Func_jp_resident_registration_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2736">The function Func_jp_resident_registration_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-2737">Un mot clé figurant dans la liste Keyword_jp_resident_registration_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2737">A keyword from Keyword_jp_resident_registration_number is found.</span></span>

```
<!-- Japan Resident Registration Number -->
<Entity id="01c1209b-6389-4faf-a5f8-3f7e13899652" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_resident_registration_number" />
        <Match idRef ="Keyword_jp_resident_registration_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b9e4a-2738">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2738">Keywords</span></span>

#### <a name="keyword_jp_resident_registration_number"></a><span data-ttu-id="b9e4a-2739">Keyword_jp_resident_registration_number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2739">Keyword_jp_resident_registration_number</span></span>

- <span data-ttu-id="b9e4a-2740">Numéro d’enregistrement du résident</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2740">Resident Registration Number</span></span>
- <span data-ttu-id="b9e4a-2741">Numéro d’enregistrement du résident</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2741">Resident Register Number</span></span> 
- <span data-ttu-id="b9e4a-2742">Numéro de base d’enregistrement des résidents</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2742">Residents Basic Registry Number</span></span> 
- <span data-ttu-id="b9e4a-2743">N° d’enregistrement du résident</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2743">Resident Registration No.</span></span> 
- <span data-ttu-id="b9e4a-2744">N° d’enregistrement du résident</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2744">Resident Register No.</span></span> 
- <span data-ttu-id="b9e4a-2745">N° de base d’enregistrement des résidents</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2745">Residents Basic Registry No.</span></span> 
- <span data-ttu-id="b9e4a-2746">N° d’enregistrement du résident de base</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2746">Basic Resident Register No.</span></span> 
- <span data-ttu-id="b9e4a-2747">住民登録番号、登録番号をレジデント</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2747">住民登録番号、登録番号をレジデント</span></span> 
- <span data-ttu-id="b9e4a-2748">住民基本登録番号、登録番号</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2748">住民基本登録番号、登録番号</span></span> 
- <span data-ttu-id="b9e4a-2749">住民基本レジストリ番号を常駐</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2749">住民基本レジストリ番号を常駐</span></span> 
- <span data-ttu-id="b9e4a-2750">登録番号を常駐住民基本台帳登録番号</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2750">登録番号を常駐住民基本台帳登録番号</span></span> 

   
## <a name="japan-social-insurance-number-sin"></a><span data-ttu-id="b9e4a-2751">Numéro d’assurance sociale Japon</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2751">Japan Social Insurance Number (SIN)</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-2752">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2752">Format</span></span>

<span data-ttu-id="b9e4a-2753">7 à 12 chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2753">7-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-2754">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2754">Pattern</span></span>

<span data-ttu-id="b9e4a-2755">7 à 12 chiffres :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2755">7-12 digits:</span></span>
- <span data-ttu-id="b9e4a-2756">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2756">Four digits</span></span> 
- <span data-ttu-id="b9e4a-2757">Un trait d’union (facultatif)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2757">A hyphen (optional)</span></span> 
- <span data-ttu-id="b9e4a-2758">Six chiffres ou</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2758">Six digits OR</span></span>
- <span data-ttu-id="b9e4a-2759">7 à 12 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2759">7-12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-2760">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2760">Checksum</span></span>

<span data-ttu-id="b9e4a-2761">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2761">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-2762">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2762">Definition</span></span>

<span data-ttu-id="b9e4a-2763">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2763">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-2764">La fonction Func_jp_sin trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2764">The function Func_jp_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-2765">Un mot clé figurant dans la liste Keyword_jp_sin est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2765">A keyword from Keyword_jp_sin is found.</span></span>

<span data-ttu-id="b9e4a-2766">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2766">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-2767">La fonction Func_jp_sin_pre_1997 trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2767">The function Func_jp_sin_pre_1997 finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-2768">Un mot clé figurant dans la liste Keyword_jp_sin est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2768">A keyword from Keyword_jp_sin is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-2769">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2769">Keywords</span></span>

#### <a name="keyword_jp_sin"></a><span data-ttu-id="b9e4a-2770">Keyword_jp_sin</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2770">Keyword_jp_sin</span></span>

- <span data-ttu-id="b9e4a-2771">N° d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2771">Social Insurance No.</span></span> 
- <span data-ttu-id="b9e4a-2772">Numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2772">Social Insurance Num</span></span> 
- <span data-ttu-id="b9e4a-2773">Numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2773">Social Insurance Number</span></span> 
- <span data-ttu-id="b9e4a-2774">社会保険のテンキー</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2774">社会保険のテンキー</span></span> 
- <span data-ttu-id="b9e4a-2775">社会保険番号</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2775">社会保険番号</span></span> 

## <a name="japanese-residence-card-number"></a><span data-ttu-id="b9e4a-2776">Numéro de carte de séjour japonaise</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2776">Japanese Residence Card Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-2777">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2777">Format</span></span>

<span data-ttu-id="b9e4a-2778">12 lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2778">12 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-2779">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2779">Pattern</span></span>

<span data-ttu-id="b9e4a-2780">12 lettres et chiffres:</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2780">12 letters and digits:</span></span>
- <span data-ttu-id="b9e4a-2781">Deux lettres (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="b9e4a-2781">Two letters (not case sensitive)</span></span>
- <span data-ttu-id="b9e4a-2782">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2782">Eight digits</span></span> 
- <span data-ttu-id="b9e4a-2783">Deux lettres (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="b9e4a-2783">Two letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-2784">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2784">Checksum</span></span>

<span data-ttu-id="b9e4a-2785">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2785">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-2786">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2786">Definition</span></span>

<span data-ttu-id="b9e4a-2787">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2787">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-2788">L’expression régulière Regex_jp_residence_card_number trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2788">The regular expression Regex_jp_residence_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-2789">Un mot clé depuis Keyword_jp_residence_card_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2789">A keyword from Keyword_jp_residence_card_number is found.</span></span>

```
<!--Japan Residence Card Number-->
-<Entity id="ac36fef2-a289-4e2c-bb48-b02366e89fc0" recommendedConfidence="75" patternsProximity="300">
   -<Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_jp_residence_card_number"/>
      <Match idRef="Keyword_jp_residence_card_number"/>
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b9e4a-2790">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2790">Keywords</span></span>

#### <a name="keyword_jp_residence_card_number"></a><span data-ttu-id="b9e4a-2791">Keyword_jp_residence_card_number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2791">Keyword_jp_residence_card_number</span></span>

- <span data-ttu-id="b9e4a-2792">Numéro de carte de séjour</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2792">Residence card number</span></span>
- <span data-ttu-id="b9e4a-2793">N ° carte de séjour</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2793">Residence card no</span></span>
- <span data-ttu-id="b9e4a-2794">Carte de séjour #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2794">Residence card #</span></span>
- <span data-ttu-id="b9e4a-2795">在留カード番号</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2795">在留カード番号</span></span>
   
## <a name="malaysia-id-card-number"></a><span data-ttu-id="b9e4a-2796">Numéro de carte d’identité Malaisie</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2796">Malaysia ID Card Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-2797">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2797">Format</span></span>

<span data-ttu-id="b9e4a-2798">12 chiffres contenant éventuellement des traits d’union</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2798">12 digits containing optional hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-2799">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2799">Pattern</span></span>

<span data-ttu-id="b9e4a-2800">12 chiffres :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2800">12 digits:</span></span>
- <span data-ttu-id="b9e4a-2801">Six chiffres au format AAMMJJ correspondant à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="b9e4a-2801">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="b9e4a-2802">Un tiret (facultatif) </span><span class="sxs-lookup"><span data-stu-id="b9e4a-2802">A dash (optional)</span></span> 
- <span data-ttu-id="b9e4a-2803">Le code à deux lettres du lieu de naissance </span><span class="sxs-lookup"><span data-stu-id="b9e4a-2803">Two-letter place-of-birth code</span></span> 
- <span data-ttu-id="b9e4a-2804">Un tiret (facultatif) </span><span class="sxs-lookup"><span data-stu-id="b9e4a-2804">A dash (optional)</span></span> 
- <span data-ttu-id="b9e4a-2805">Trois chiffres aléatoires </span><span class="sxs-lookup"><span data-stu-id="b9e4a-2805">Three random digits</span></span> 
- <span data-ttu-id="b9e4a-2806">Code de sexe à un chiffre</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2806">One-digit gender code</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-2807">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2807">Checksum</span></span>

<span data-ttu-id="b9e4a-2808">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2808">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-2809">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2809">Definition</span></span>

<span data-ttu-id="b9e4a-2810">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2810">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-2811">L’expression régulière Regex_malaysia_id_card_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2811">The regular expression Regex_malaysia_id_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-2812">Un mot clé figurant dans la liste Keyword_malaysia_id_card_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2812">A keyword from Keyword_malaysia_id_card_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-2813">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2813">Keywords</span></span>
   
#### <a name="keyword_malaysia_id_card_number"></a><span data-ttu-id="b9e4a-2814">Keyword_malaysia_id_card_number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2814">Keyword_malaysia_id_card_number</span></span>

- <span data-ttu-id="b9e4a-2815">carte d’application numérique</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2815">digital application card</span></span>
- <span data-ttu-id="b9e4a-2816">i/c</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2816">i/c</span></span>
- <span data-ttu-id="b9e4a-2817">n ° i/c non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2817">i/c no</span></span>
- <span data-ttu-id="b9e4a-2818">combustion</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2818">ic</span></span>
- <span data-ttu-id="b9e4a-2819">n ° IC</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2819">ic no</span></span>
- <span data-ttu-id="b9e4a-2820">carte d’identité</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2820">id card</span></span>
- <span data-ttu-id="b9e4a-2821">Carte d’identification</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2821">identification Card</span></span>
- <span data-ttu-id="b9e4a-2822">Carte d’identité</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2822">identity card</span></span>
- <span data-ttu-id="b9e4a-2823">k/p</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2823">k/p</span></span>
- <span data-ttu-id="b9e4a-2824">n ° k/p</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2824">k/p no</span></span>
- <span data-ttu-id="b9e4a-2825">kad akuan diri</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2825">kad akuan diri</span></span>
- <span data-ttu-id="b9e4a-2826">Kad aplikasi numérique</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2826">kad aplikasi digital</span></span>
- <span data-ttu-id="b9e4a-2827">Kad Pengenalan Malaisie</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2827">kad pengenalan malaysia</span></span>
- <span data-ttu-id="b9e4a-2828">kgf</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2828">kp</span></span>
- <span data-ttu-id="b9e4a-2829">KP non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2829">kp no</span></span>
- <span data-ttu-id="b9e4a-2830">mykad</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2830">mykad</span></span>
- <span data-ttu-id="b9e4a-2831">mykas</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2831">mykas</span></span>
- <span data-ttu-id="b9e4a-2832">mykid</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2832">mykid</span></span>
- <span data-ttu-id="b9e4a-2833">mypr</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2833">mypr</span></span>
- <span data-ttu-id="b9e4a-2834">mytentera</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2834">mytentera</span></span>
- <span data-ttu-id="b9e4a-2835">carte d’identité Malaisie</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2835">malaysia identity card</span></span>
- <span data-ttu-id="b9e4a-2836">carte d’identité malais</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2836">malaysian identity card</span></span>
- <span data-ttu-id="b9e4a-2837">NRIC</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2837">nric</span></span>
- <span data-ttu-id="b9e4a-2838">carte d’identification personnelle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2838">personal identification card</span></span>
   
## <a name="netherlands-citizens-service-bsn-number"></a><span data-ttu-id="b9e4a-2839">Numéro de service du citoyen (BSN) Pays-Bas</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2839">Netherlands Citizen's Service (BSN) Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-2840">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2840">Format</span></span>

<span data-ttu-id="b9e4a-2841">8 à 9 chiffres contenant éventuellement des espaces</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2841">8-9 digits containing optional spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-2842">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2842">Pattern</span></span>

<span data-ttu-id="b9e4a-2843">8 à 9 chiffres :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2843">8-9 digits:</span></span>
- <span data-ttu-id="b9e4a-2844">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2844">Three digits</span></span> 
- <span data-ttu-id="b9e4a-2845">Un espace (facultatif) </span><span class="sxs-lookup"><span data-stu-id="b9e4a-2845">A space (optional)</span></span> 
- <span data-ttu-id="b9e4a-2846">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2846">Three digits</span></span> 
- <span data-ttu-id="b9e4a-2847">Un espace (facultatif) </span><span class="sxs-lookup"><span data-stu-id="b9e4a-2847">A space (optional)</span></span> 
- <span data-ttu-id="b9e4a-2848">2 à 3 chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2848">2-3 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-2849">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2849">Checksum</span></span>

<span data-ttu-id="b9e4a-2850">Oui</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2850">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-2851">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2851">Definition</span></span>

<span data-ttu-id="b9e4a-2852">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2852">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-2853">La fonction Func_netherlands_bsn trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2853">The function Func_netherlands_bsn finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-2854">Un mot clé figurant dans la liste Keyword_netherlands_bsn est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2854">A keyword from Keyword_netherlands_bsn is found.</span></span>
- <span data-ttu-id="b9e4a-2855">La fonction Func_eu_date2 trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2855">The function Func_eu_date2 finds a date in the right date format.</span></span>
- <span data-ttu-id="b9e4a-2856">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2856">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-2857">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2857">Keywords</span></span>

#### <a name="keyword_netherlands_bsn"></a><span data-ttu-id="b9e4a-2858">Keyword_netherlands_bsn</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2858">Keyword_netherlands_bsn</span></span>

- <span data-ttu-id="b9e4a-2859">Citizen service number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2859">Citizen service number</span></span> 
- <span data-ttu-id="b9e4a-2860">BSN</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2860">BSN</span></span> 
- <span data-ttu-id="b9e4a-2861">Burgerservicenummer</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2861">Burgerservicenummer</span></span> 
- <span data-ttu-id="b9e4a-2862">Sofinummer</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2862">Sofinummer</span></span> 
- <span data-ttu-id="b9e4a-2863">Persoonsgebonden nummer</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2863">Persoonsgebonden nummer</span></span> 
- <span data-ttu-id="b9e4a-2864">Persoonsnummer</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2864">Persoonsnummer</span></span>    

   
## <a name="new-zealand-ministry-of-health-number"></a><span data-ttu-id="b9e4a-2865">Numéro du Ministère de la santé Nouvelle-Zélande</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2865">New Zealand Ministry of Health Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-2866">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2866">Format</span></span>

<span data-ttu-id="b9e4a-2867">Trois lettres, un espace (facultatif) et quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2867">Three letters, a space (optional), and four digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-2868">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2868">Pattern</span></span>

<span data-ttu-id="b9e4a-2869">Trois lettres (ne respectant pas la casse) un espace (facultatif) quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2869">Three letters (not case sensitive) a space (optional) four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-2870">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2870">Checksum</span></span>

<span data-ttu-id="b9e4a-2871">Oui</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2871">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-2872">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2872">Definition</span></span>

<span data-ttu-id="b9e4a-2873">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2873">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-2874">La fonction Func_new_zealand_ministry_of_health_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2874">The function Func_new_zealand_ministry_of_health_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-2875">Un mot clé figurant dans la liste Keyword_nz_terms est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2875">A keyword from Keyword_nz_terms is found.</span></span>
- <span data-ttu-id="b9e4a-2876">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2876">The checksum passes.</span></span>

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

<span data-ttu-id="b9e4a-2877">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2877">Keywords</span></span>

<span data-ttu-id="b9e4a-2878">Keyword_nz_terms</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2878">Keyword_nz_terms</span></span>

- <span data-ttu-id="b9e4a-2879">NHI</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2879">NHI</span></span> 
- <span data-ttu-id="b9e4a-2880">Nouvelle-Zélande</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2880">New Zealand</span></span> 
- <span data-ttu-id="b9e4a-2881">Intégrité</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2881">Health</span></span> 
- <span data-ttu-id="b9e4a-2882">destinations</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2882">treatment</span></span> 
   
## <a name="norway-identification-number"></a><span data-ttu-id="b9e4a-2883">Numéro d’identification Norvège</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2883">Norway Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-2884">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2884">Format</span></span>

<span data-ttu-id="b9e4a-2885">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2885">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-2886">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2886">Pattern</span></span>

<span data-ttu-id="b9e4a-2887">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2887">11 digits:</span></span>
- <span data-ttu-id="b9e4a-2888">Six chiffres au format JJMMAA qui correspondent à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="b9e4a-2888">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="b9e4a-2889">Numéro individuel à trois chiffres </span><span class="sxs-lookup"><span data-stu-id="b9e4a-2889">Three-digit individual number</span></span> 
- <span data-ttu-id="b9e4a-2890">Deux chiffres de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2890">Two check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-2891">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2891">Checksum</span></span>

<span data-ttu-id="b9e4a-2892">Oui</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2892">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-2893">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2893">Definition</span></span>

<span data-ttu-id="b9e4a-2894">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2894">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-2895">La fonction Func_norway_id_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2895">The function Func_norway_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-2896">Un mot clé figurant dans la liste Keyword_norway_id_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2896">A keyword from Keyword_norway_id_number is found.</span></span>
- <span data-ttu-id="b9e4a-2897">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2897">The checksum passes.</span></span>
- <span data-ttu-id="b9e4a-2898">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2898">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-2899">La fonction Func_norway_id_numbe trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2899">The function Func_norway_id_numbe finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-2900">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2900">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-2901">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2901">Keywords</span></span>

#### <a name="keyword_norway_id_number"></a><span data-ttu-id="b9e4a-2902">Keyword_norway_id_number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2902">Keyword_norway_id_number</span></span>

- <span data-ttu-id="b9e4a-2903">Personal identification number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2903">Personal identification number</span></span>
- <span data-ttu-id="b9e4a-2904">Norwegian ID Number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2904">Norwegian ID Number</span></span>
- <span data-ttu-id="b9e4a-2905">ID Number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2905">ID Number</span></span>
- <span data-ttu-id="b9e4a-2906">Identificateur</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2906">Identification</span></span>
- <span data-ttu-id="b9e4a-2907">Personnummer</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2907">Personnummer</span></span>
- <span data-ttu-id="b9e4a-2908">Fødselsnummer</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2908">Fødselsnummer</span></span>

   
## <a name="philippines-unified-multi-purpose-id-number"></a><span data-ttu-id="b9e4a-2909">Numéro d’identification multifonction unifié Philippines</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2909">Philippines Unified Multi-Purpose ID Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-2910">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2910">Format</span></span>

<span data-ttu-id="b9e4a-2911">12 chiffres séparés par des traits d’union</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2911">12 digits separated by hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-2912">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2912">Pattern</span></span>

<span data-ttu-id="b9e4a-2913">12 chiffres :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2913">12 digits:</span></span>
- <span data-ttu-id="b9e4a-2914">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2914">Four digits</span></span> 
- <span data-ttu-id="b9e4a-2915">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="b9e4a-2915">A hyphen</span></span> 
- <span data-ttu-id="b9e4a-2916">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="b9e4a-2916">Seven digits</span></span> 
- <span data-ttu-id="b9e4a-2917">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="b9e4a-2917">A hyphen</span></span> 
- <span data-ttu-id="b9e4a-2918">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2918">One digit</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-2919">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2919">Checksum</span></span>

<span data-ttu-id="b9e4a-2920">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2920">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-2921">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2921">Definition</span></span>

<span data-ttu-id="b9e4a-2922">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2922">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-2923">L’expression régulière Regex_philippines_unified_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2923">The regular expression Regex_philippines_unified_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-2924">Un mot clé figurant dans la liste Keyword_philippines_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2924">A keyword from Keyword_philippines_id is found.</span></span>

```
<!-- Philippines Unified Multi-Purpose ID number -->
<Entity id="019b39dd-8c25-4765-91a3-d9c6baf3c3b3" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_philippines_unified_id"/>
     <Match idRef="Keyword_philippines_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b9e4a-2925">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2925">Keywords</span></span>
   
#### <a name="keyword_philippines_id"></a><span data-ttu-id="b9e4a-2926">Keyword_philippines_id</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2926">Keyword_philippines_id</span></span>

- <span data-ttu-id="b9e4a-2927">Unified Multi-Purpose ID</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2927">Unified Multi-Purpose ID</span></span> 
- <span data-ttu-id="b9e4a-2928">UMID</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2928">UMID</span></span> 
- <span data-ttu-id="b9e4a-2929">Identity Card</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2929">Identity Card</span></span> 
- <span data-ttu-id="b9e4a-2930">Pinag-isang Multi-Layunin ID</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2930">Pinag-isang Multi-Layunin ID</span></span>
   
## <a name="poland-identity-card"></a><span data-ttu-id="b9e4a-2931">Carte d'identité Pologne</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2931">Poland Identity Card</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-2932">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2932">Format</span></span>

<span data-ttu-id="b9e4a-2933">Trois lettres et six chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2933">Three letters and six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-2934">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2934">Pattern</span></span>

<span data-ttu-id="b9e4a-2935">Trois lettres (ne respectant pas la casse) suivis de six chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2935">Three letters (not case sensitive) followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-2936">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2936">Checksum</span></span>

<span data-ttu-id="b9e4a-2937">Oui</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2937">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-2938">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2938">Definition</span></span>

<span data-ttu-id="b9e4a-2939">Une stratégie DLP est sûre à 75% d’avoir détecté ce type d’informations sensibles si, dans une proximité de 300 caractères: la fonction Func_polish_national_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2939">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_polish_national_id finds content that matches the pattern.</span></span>
<span data-ttu-id="b9e4a-2940">Un mot clé figurant dans la liste Keyword_polish_national_id_passport_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2940">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
<span data-ttu-id="b9e4a-2941">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2941">The checksum passes.</span></span>

```
<!-- Poland Identity Card-->
<Entity id="25E64989-ED5D-40CA-A939-6C14183BB7BF" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_national_id" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b9e4a-2942">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2942">Keywords</span></span>

#### <a name="keyword_polish_national_id_passport_number"></a><span data-ttu-id="b9e4a-2943">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2943">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="b9e4a-2944">Dowód osobisty</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2944">Dowód osobisty</span></span>
- <span data-ttu-id="b9e4a-2945">Chiffre dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2945">Numer dowodu osobistego</span></span>
- <span data-ttu-id="b9e4a-2946">Nazwa i dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2946">Nazwa i numer dowodu osobistego</span></span>
- <span data-ttu-id="b9e4a-2947">Nazwa i Nr dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2947">Nazwa i nr dowodu osobistego</span></span>
- <span data-ttu-id="b9e4a-2948">Nazwa je nr dowodu tożsamości</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2948">Nazwa i nr dowodu tożsamości</span></span>
- <span data-ttu-id="b9e4a-2949">Dowód Tożsamości</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2949">Dowód Tożsamości</span></span>
- <span data-ttu-id="b9e4a-2950">Dow.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2950">dow.</span></span> <span data-ttu-id="b9e4a-2951">OS.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2951">os.</span></span>

   
## <a name="poland-national-id-pesel"></a><span data-ttu-id="b9e4a-2952">ID national polonais (PESEL)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2952">Poland National ID (PESEL)</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-2953">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2953">Format</span></span>

<span data-ttu-id="b9e4a-2954">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2954">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-2955">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2955">Pattern</span></span>

<span data-ttu-id="b9e4a-2956">11 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2956">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-2957">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2957">Checksum</span></span>

<span data-ttu-id="b9e4a-2958">Oui</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2958">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-2959">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2959">Definition</span></span>

<span data-ttu-id="b9e4a-2960">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2960">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-2961">La fonction Func_pesel_identification_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2961">The function Func_pesel_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-2962">Un mot clé figurant dans la liste Keyword_pesel_identification_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2962">A keyword from Keyword_pesel_identification_number is found.</span></span>
- <span data-ttu-id="b9e4a-2963">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2963">The checksum passes.</span></span>

```
<!-- Poland National ID (PESEL) -->      
<Entity id="E3AAF206-4297-412F-9E06-BA8487E22456" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_pesel_identification_number" />
          <Match idRef="Keyword_pesel_identification_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b9e4a-2964">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2964">Keywords</span></span>

#### <a name="keyword_pesel_identification_number"></a><span data-ttu-id="b9e4a-2965">Keyword_pesel_identification_number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2965">Keyword_pesel_identification_number</span></span>

- <span data-ttu-id="b9e4a-2966">Nr PESEL</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2966">Nr PESEL</span></span>
- <span data-ttu-id="b9e4a-2967">PESEL</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2967">PESEL</span></span>   

   
## <a name="poland-passport"></a><span data-ttu-id="b9e4a-2968">Passeport Pologne</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2968">Poland Passport</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-2969">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2969">Format</span></span>

<span data-ttu-id="b9e4a-2970">Deux lettres et sept chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2970">Two letters and seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-2971">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2971">Pattern</span></span>

<span data-ttu-id="b9e4a-2972">Deux lettres (ne respectant pas la casse) suivies de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2972">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-2973">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2973">Checksum</span></span>

<span data-ttu-id="b9e4a-2974">Oui</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2974">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-2975">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2975">Definition</span></span>

<span data-ttu-id="b9e4a-2976">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2976">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-2977">La fonction Func_polish_passport_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2977">The function Func_polish_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-2978">Un mot clé figurant dans la liste Keyword_polish_national_id_passport_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2978">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
- <span data-ttu-id="b9e4a-2979">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2979">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-2980">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2980">Keywords</span></span>

#### <a name="keyword_polish_national_id_passport_number"></a><span data-ttu-id="b9e4a-2981">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2981">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="b9e4a-2982">Numéro paszportu</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2982">Numer paszportu</span></span>
- <span data-ttu-id="b9e4a-2983">Nr.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2983">Nr.</span></span> <span data-ttu-id="b9e4a-2984">Paszportu</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2984">Paszportu</span></span>
- <span data-ttu-id="b9e4a-2985">Paszport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2985">Paszport</span></span>

   
## <a name="portugal-citizen-card-number"></a><span data-ttu-id="b9e4a-2986">Numéro de carte de citoyen Portugal</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2986">Portugal Citizen Card Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-2987">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2987">Format</span></span>

<span data-ttu-id="b9e4a-2988">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2988">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-2989">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2989">Pattern</span></span>

<span data-ttu-id="b9e4a-2990">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2990">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-2991">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2991">Checksum</span></span>

<span data-ttu-id="b9e4a-2992">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2992">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-2993">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2993">Definition</span></span>

<span data-ttu-id="b9e4a-2994">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2994">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-2995">L’expression régulière Regex_portugal_citizen_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2995">The regular expression Regex_portugal_citizen_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-2996">Un mot clé figurant dans la liste Keyword_portugal_citizen_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2996">A keyword from Keyword_portugal_citizen_card is found.</span></span>

```
<!-- Portugal Citizen Card Number -->
<Entity id="91a7ece2-add4-4986-9a15-c84544d81ecd" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_portugal_citizen_card"/>
     <Match idRef="Keyword_portugal_citizen_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b9e4a-2997">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2997">Keywords</span></span>

#### <a name="keyword_portugal_citizen_card"></a><span data-ttu-id="b9e4a-2998">Keyword_portugal_citizen_card</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2998">Keyword_portugal_citizen_card</span></span>

- <span data-ttu-id="b9e4a-2999">Citizen Card</span><span class="sxs-lookup"><span data-stu-id="b9e4a-2999">Citizen Card</span></span>
- <span data-ttu-id="b9e4a-3000">National ID Card</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3000">National ID Card</span></span>
- <span data-ttu-id="b9e4a-3001">Cc</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3001">CC</span></span>
- <span data-ttu-id="b9e4a-3002">Cartão de Cidadão</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3002">Cartão de Cidadão</span></span>
- <span data-ttu-id="b9e4a-3003">Bilhete de Identidade</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3003">Bilhete de Identidade</span></span>
   
## <a name="saudi-arabia-national-id"></a><span data-ttu-id="b9e4a-3004">ID national Arabie saoudite</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3004">Saudi Arabia National ID</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-3005">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3005">Format</span></span>

<span data-ttu-id="b9e4a-3006">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3006">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-3007">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3007">Pattern</span></span>

<span data-ttu-id="b9e4a-3008">10 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3008">10 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-3009">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3009">Checksum</span></span>

<span data-ttu-id="b9e4a-3010">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3010">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-3011">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3011">Definition</span></span>

<span data-ttu-id="b9e4a-3012">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3012">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-3013">L’expression régulière Regex_saudi_arabia_national_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3013">The regular expression Regex_saudi_arabia_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-3014">Un mot clé figurant dans la liste Keyword_saudi_arabia_national_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3014">A keyword from Keyword_saudi_arabia_national_id is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-3015">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3015">Keywords</span></span>

#### <a name="keyword_saudi_arabia_national_id"></a><span data-ttu-id="b9e4a-3016">Keyword_saudi_arabia_national_id</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3016">Keyword_saudi_arabia_national_id</span></span>

- <span data-ttu-id="b9e4a-3017">Carte d’identification</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3017">Identification Card</span></span> 
- <span data-ttu-id="b9e4a-3018">numéro de carte d’identité</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3018">I card number</span></span> 
- <span data-ttu-id="b9e4a-3019">Numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3019">ID number</span></span> 
- <span data-ttu-id="b9e4a-3020">الوطنية الهوية بطاقة رقم</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3020">الوطنية الهوية بطاقة رقم</span></span> 

   
## <a name="singapore-national-registration-identity-card-nric-number"></a><span data-ttu-id="b9e4a-3021">Numéro de carte d’identité d’enregistrement national (NRIC) Singapour</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3021">Singapore National Registration Identity Card (NRIC) Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-3022">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3022">Format</span></span>

<span data-ttu-id="b9e4a-3023">Neuf lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3023">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-3024">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3024">Pattern</span></span>

- <span data-ttu-id="b9e4a-3025">Neuf lettres et chiffres :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3025">Nine letters and digits:</span></span>
- <span data-ttu-id="b9e4a-3026">La lettre « F », « G », « S » ou « T » (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="b9e4a-3026">The letter "F", "G", "S", or "T" (not case sensitive)</span></span> 
- <span data-ttu-id="b9e4a-3027">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="b9e4a-3027">Seven digits</span></span> 
- <span data-ttu-id="b9e4a-3028">Un chiffre de contrôle alphabétique</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3028">An alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-3029">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3029">Checksum</span></span>

<span data-ttu-id="b9e4a-3030">Oui</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3030">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-3031">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3031">Definition</span></span>

<span data-ttu-id="b9e4a-3032">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3032">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-3033">L’expression régulière Regex_singapore_nric trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3033">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-3034">Un mot clé figurant dans la liste Keyword_singapore_nric est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3034">A keyword from Keyword_singapore_nric is found.</span></span>
- <span data-ttu-id="b9e4a-3035">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3035">The checksum passes.</span></span>

<span data-ttu-id="b9e4a-3036">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3036">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-3037">L’expression régulière Regex_singapore_nric trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3037">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-3038">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3038">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-3039">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3039">Keywords</span></span>
   
#### <a name="keyword_singapore_nric"></a><span data-ttu-id="b9e4a-3040">Keyword_singapore_nric</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3040">Keyword_singapore_nric</span></span>

- <span data-ttu-id="b9e4a-3041">National Registration Identity Card</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3041">National Registration Identity Card</span></span> 
- <span data-ttu-id="b9e4a-3042">Identity Card Number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3042">Identity Card Number</span></span> 
- <span data-ttu-id="b9e4a-3043">NRIC</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3043">NRIC</span></span> 
- <span data-ttu-id="b9e4a-3044">COMBUSTION</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3044">IC</span></span> 
- <span data-ttu-id="b9e4a-3045">Foreign Identification Number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3045">Foreign Identification Number</span></span> 
- <span data-ttu-id="b9e4a-3046">ECHERCHER</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3046">FIN</span></span> 
- <span data-ttu-id="b9e4a-3047">身份证</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3047">身份证</span></span> 
- <span data-ttu-id="b9e4a-3048">身份證</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3048">身份證</span></span> 
   
## <a name="south-africa-identification-number"></a><span data-ttu-id="b9e4a-3049">Numéro d’identification Afrique du Sud</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3049">South Africa Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-3050">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3050">Format</span></span>

<span data-ttu-id="b9e4a-3051">13 chiffres pouvant contenir des espaces</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3051">13 digits that may contain spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-3052">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3052">Pattern</span></span>

<span data-ttu-id="b9e4a-3053">13 chiffres :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3053">13 digits:</span></span>
- <span data-ttu-id="b9e4a-3054">Six chiffres au format AAMMJJ correspondant à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="b9e4a-3054">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="b9e4a-3055">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3055">Four digits</span></span> 
- <span data-ttu-id="b9e4a-3056">Un indicateur de citoyenneté à un chiffre </span><span class="sxs-lookup"><span data-stu-id="b9e4a-3056">A single-digit citizenship indicator</span></span> 
- <span data-ttu-id="b9e4a-3057">Le chiffre « 8 » ou « 9 » </span><span class="sxs-lookup"><span data-stu-id="b9e4a-3057">The digit "8" or "9"</span></span> 
- <span data-ttu-id="b9e4a-3058">Un chiffre pour la somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3058">One digit which is a checksum digit</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-3059">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3059">Checksum</span></span>

<span data-ttu-id="b9e4a-3060">Oui</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3060">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-3061">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3061">Definition</span></span>

<span data-ttu-id="b9e4a-3062">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3062">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-3063">La fonction Func_south_africa_identification_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3063">The function Func_south_africa_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-3064">Un mot clé figurant dans la liste Keyword_south_africa_identification_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3064">A keyword from Keyword_south_africa_identification_number is found.</span></span>
- <span data-ttu-id="b9e4a-3065">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3065">The checksum passes.</span></span>

```
<!-- South Africa Identification Number -->
<Entity id="e2adf7cb-8ea6-4048-a2ed-d89eb65f2780" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_south_africa_identification_number"/>
     <Match idRef="Keyword_south_africa_identification_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b9e4a-3066">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3066">Keywords</span></span>
   
#### <a name="keyword_south_africa_identification_number"></a><span data-ttu-id="b9e4a-3067">Keyword_south_africa_identification_number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3067">Keyword_south_africa_identification_number</span></span>

- <span data-ttu-id="b9e4a-3068">Identity card</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3068">Identity card</span></span>
- <span data-ttu-id="b9e4a-3069">ID</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3069">ID</span></span>
- <span data-ttu-id="b9e4a-3070">Identificateur</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3070">Identification</span></span> 
   
## <a name="south-korea-resident-registration-number"></a><span data-ttu-id="b9e4a-3071">Matricule de résident Corée du Sud</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3071">South Korea Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-3072">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3072">Format</span></span>

<span data-ttu-id="b9e4a-3073">13 chiffres contenant un trait d’union</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3073">13 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-3074">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3074">Pattern</span></span>

<span data-ttu-id="b9e4a-3075">13 chiffres :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3075">13 digits:</span></span>
- <span data-ttu-id="b9e4a-3076">Six chiffres au format AAMMJJ correspondant à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="b9e4a-3076">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="b9e4a-3077">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="b9e4a-3077">A hyphen</span></span> 
- <span data-ttu-id="b9e4a-3078">Un chiffre déterminé par le siècle et le sexe </span><span class="sxs-lookup"><span data-stu-id="b9e4a-3078">One digit determined by the century and gender</span></span> 
- <span data-ttu-id="b9e4a-3079">Code à quatre chiffres désignant la région de naissance </span><span class="sxs-lookup"><span data-stu-id="b9e4a-3079">Four-digit region-of-birth code</span></span> 
- <span data-ttu-id="b9e4a-3080">Un chiffre utilisé pour différencier les personnes dont les chiffres précédents sont identiques. </span><span class="sxs-lookup"><span data-stu-id="b9e4a-3080">One digit used to differentiate people for whom the preceding numbers are identical</span></span> 
- <span data-ttu-id="b9e4a-3081">Un chiffre de contrôle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3081">A check digit.</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-3082">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3082">Checksum</span></span>

<span data-ttu-id="b9e4a-3083">Oui</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3083">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-3084">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3084">Definition</span></span>

<span data-ttu-id="b9e4a-3085">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3085">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-3086">La fonction Func_south_korea_resident_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3086">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-3087">Un mot clé figurant dans la liste Keyword_south_korea_resident_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3087">A keyword from Keyword_south_korea_resident_number is found.</span></span>
- <span data-ttu-id="b9e4a-3088">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3088">The checksum passes.</span></span>

<span data-ttu-id="b9e4a-3089">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3089">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-3090">La fonction Func_south_korea_resident_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3090">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-3091">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3091">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-3092">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3092">Keywords</span></span>
   
#### <a name="keyword_south_korea_resident_number"></a><span data-ttu-id="b9e4a-3093">Keyword_south_korea_resident_number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3093">Keyword_south_korea_resident_number</span></span>

- <span data-ttu-id="b9e4a-3094">National ID card</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3094">National ID card</span></span> 
- <span data-ttu-id="b9e4a-3095">Citizen’s Registration Number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3095">Citizen's Registration Number</span></span> 
- <span data-ttu-id="b9e4a-3096">Jumin deungnok beonho</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3096">Jumin deungnok beonho</span></span> 
- <span data-ttu-id="b9e4a-3097">RRN</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3097">RRN</span></span> 
- <span data-ttu-id="b9e4a-3098">주민등록번호</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3098">주민등록번호</span></span>
   
## <a name="spain-social-security-number-ssn"></a><span data-ttu-id="b9e4a-3099">Numéro de sécurité sociale Espagne</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3099">Spain Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-3100">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3100">Format</span></span>

<span data-ttu-id="b9e4a-3101">11 à 12 chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3101">11-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-3102">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3102">Pattern</span></span>

<span data-ttu-id="b9e4a-3103">11-12 chiffres:</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3103">11-12 digits:</span></span>
- <span data-ttu-id="b9e4a-3104">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3104">Two digits</span></span> 
- <span data-ttu-id="b9e4a-3105">Une barre oblique (facultative)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3105">A forward slash (optional)</span></span> 
- <span data-ttu-id="b9e4a-3106">7 à 8 chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3106">7-8 digits</span></span> 
- <span data-ttu-id="b9e4a-3107">Une barre oblique (facultative)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3107">A forward slash (optional)</span></span> 
- <span data-ttu-id="b9e4a-3108">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3108">Two digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-3109">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3109">Checksum</span></span>

<span data-ttu-id="b9e4a-3110">Oui</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3110">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-3111">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3111">Definition</span></span>

<span data-ttu-id="b9e4a-3112">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3112">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-3113">La fonction Func_spanish_social_security_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3113">The function Func_spanish_social_security_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-3114">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3114">The checksum passes.</span></span>

```
<!-- Spain SSN -->
<Entity id="5df987c0-8eae-4bce-ace7-b316347f3070" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_spanish_social_security_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b9e4a-3115">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3115">Keywords</span></span>

<span data-ttu-id="b9e4a-3116">Aucun</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3116">None</span></span>

## <a name="sql-server-connection-string"></a><span data-ttu-id="b9e4a-3117">Chaîne de connexion SQL Server</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3117">SQL Server Connection String</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-3118">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3118">Format</span></span>

<span data-ttu-id="b9e4a-3119">La chaîne «User ID», «User ID», «UID» ou «UserId» suivi des caractères et des chaînes décrits dans le modèle ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3119">The string "User Id", "User ID", "uid", or "UserId" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-3120">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3120">Pattern</span></span>

- <span data-ttu-id="b9e4a-3121">La chaîne «User ID», «User ID», «UID» ou «UserId»</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3121">The string "User Id", "User ID", "uid", or "UserId"</span></span>
- <span data-ttu-id="b9e4a-3122">N’importe quelle combinaison entre 1-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3122">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="b9e4a-3123">La chaîne "password" ou "PWD" où "PWD" n’est pas précédé d’une lettre minuscule</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3123">The string "Password" or "pwd" where "pwd" is not preceded by a lowercase letter</span></span>
- <span data-ttu-id="b9e4a-3124">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3124">An equal sign (=)</span></span>
- <span data-ttu-id="b9e4a-3125">Tout caractère qui n’est pas un signe dollar ($), un symbole de pourcentage (%), un symbole supérieur à (>), un symbole (@), un guillemet ("), un point-virgule (;), une accolade ouvrante ([) ou un crochet gauche ({)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3125">Any character that is not a dollar sign ($), percent symbol (%), greater than symbol (>), at symbol (@), quotation mark ("), semicolon (;), left brace ([), or left bracket ({)</span></span>
- <span data-ttu-id="b9e4a-3126">N’importe quelle combinaison de 7-128 caractères qui ne sont pas des points-virgules (;), barre oblique (/) ou guillemets (")</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3126">Any combination of 7-128 characters that are not a semicolon (;), forward slash (/), or quotation mark (")</span></span>
- <span data-ttu-id="b9e4a-3127">Un point-virgule (;) ou guillemets (")</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3127">A semicolon (;) or quotation mark (")</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-3128">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3128">Checksum</span></span>

<span data-ttu-id="b9e4a-3129">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3129">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-3130">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3130">Definition</span></span>

<span data-ttu-id="b9e4a-3131">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3131">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-3132">L’expression régulière CEP_Regex_SQLServerConnectionString trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3132">The regular expression CEP_Regex_SQLServerConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-3133">Un mot clé depuis CEP_GlobalFilter \*\*\*\* est introuvable.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3133">A keyword from CEP_GlobalFilter is **not** found.</span></span>
- <span data-ttu-id="b9e4a-3134">L’expression régulière CEP_PasswordPlaceHolder ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3134">The regular expression CEP_PasswordPlaceHolder does **not** find content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-3135">L’expression régulière CEP_CommonExampleKeywords ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3135">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-3136">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3136">Keywords</span></span>

#### <a name="cep_globalfilter"></a><span data-ttu-id="b9e4a-3137">CEP_GlobalFilter</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3137">CEP_GlobalFilter</span></span>

- <span data-ttu-id="b9e4a-3138">some-password</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3138">some-password</span></span>
- <span data-ttu-id="b9e4a-3139">somepassword</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3139">somepassword</span></span>
- <span data-ttu-id="b9e4a-3140">secretPassword</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3140">secretPassword</span></span>
- <span data-ttu-id="b9e4a-3141">échantillonnage</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3141">sample</span></span>

#### <a name="cep_passwordplaceholder"></a><span data-ttu-id="b9e4a-3142">CEP_PasswordPlaceHolder</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3142">CEP_PasswordPlaceHolder</span></span>

<span data-ttu-id="b9e4a-3143">(Notez que techniquement, ce type d’informations sensibles identifie ces mots clés à l’aide d’une expression régulière, et non d’une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3143">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="b9e4a-3144">Mot de passe ou mot de passe suivi par 0-2 espaces, un signe égal (=), 0-2 espaces et un astérisque (\*)--ou--</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3144">Password or pwd followed by 0-2 spaces, an equal sign (=), 0-2 spaces, and an asterisk (\*) --OR--</span></span>
- <span data-ttu-id="b9e4a-3145">Mot de passe ou mot de passe suivi par:</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3145">Password or pwd followed by:</span></span>
    - <span data-ttu-id="b9e4a-3146">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3146">Equal sign (=)</span></span>
    - <span data-ttu-id="b9e4a-3147">Symbole inférieur à (<)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3147">Less than symbol (<)</span></span>
    - <span data-ttu-id="b9e4a-3148">Toute combinaison de 1-200 caractères qui sont des lettres majuscules ou minuscules, des chiffres, un astérisque (\*), un tiret (-), un trait de soulignement (_) ou un espace blanc</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3148">Any combination of 1-200 characters that are upper- or lowercase letters, digits, an asterisk (\*), hyphen (-), underline (_), or whitespace character</span></span>
    - <span data-ttu-id="b9e4a-3149">Symbole supérieur à (>)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3149">Greater than symbol (>)</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="b9e4a-3150">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3150">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="b9e4a-3151">(Notez que techniquement, ce type d’informations sensibles identifie ces mots clés à l’aide d’une expression régulière, et non d’une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3151">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="b9e4a-3152">contoso</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3152">contoso</span></span>
- <span data-ttu-id="b9e4a-3153">société</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3153">fabrikam</span></span>
- <span data-ttu-id="b9e4a-3154">Northwind</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3154">northwind</span></span>
- <span data-ttu-id="b9e4a-3155">immédiatement</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3155">sandbox</span></span>
- <span data-ttu-id="b9e4a-3156">onebox</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3156">onebox</span></span>
- <span data-ttu-id="b9e4a-3157">hôte</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3157">localhost</span></span>
- <span data-ttu-id="b9e4a-3158">bouclage</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3158">127.0.0.1</span></span>
- <span data-ttu-id="b9e4a-3159">testacs.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3159">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="b9e4a-3160">com</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3160">com</span></span>
- <span data-ttu-id="b9e4a-3161">s-int.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3161">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="b9e4a-3162">NET</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3162">net</span></span>

## <a name="sweden-national-id"></a><span data-ttu-id="b9e4a-3163">ID national Suède</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3163">Sweden National ID</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-3164">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3164">Format</span></span>

<span data-ttu-id="b9e4a-3165">10 ou 12 chiffres et éventuellement un délimiteur</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3165">10 or 12 digits and an optional delimiter</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-3166">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3166">Pattern</span></span>

<span data-ttu-id="b9e4a-3167">10 ou 12 chiffres et un délimiteur facultatif :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3167">10 or 12 digits and an optional delimiter:</span></span>
- <span data-ttu-id="b9e4a-3168">2 à 4 chiffres (facultatifs)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3168">2-4 digits (optional)</span></span> 
- <span data-ttu-id="b9e4a-3169">Six chiffres au format de date AAMMJJ</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3169">Six digits in date format YYMMDD</span></span> 
- <span data-ttu-id="b9e4a-3170">Séparateur de « - » ou « + » (facultatif), plus</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3170">Delimiter of "-" or "+" (optional), plus</span></span>
- <span data-ttu-id="b9e4a-3171">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3171">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-3172">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3172">Checksum</span></span>

<span data-ttu-id="b9e4a-3173">Oui</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3173">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-3174">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3174">Definition</span></span>

<span data-ttu-id="b9e4a-3175">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3175">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-3176">La fonction Func_swedish_national_identifier trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3176">The function Func_swedish_national_identifier finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-3177">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3177">The checksum passes.</span></span>

```
<!-- Sweden National ID -->
<Entity id="f69aaf40-79be-4fac-8f05-fd1910d272c8" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_swedish_national_identifier" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b9e4a-3178">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3178">Keywords</span></span>

<span data-ttu-id="b9e4a-3179">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3179">No</span></span>
   
## <a name="sweden-passport-number"></a><span data-ttu-id="b9e4a-3180">Numéro de passeport Suède</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3180">Sweden Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-3181">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3181">Format</span></span>

<span data-ttu-id="b9e4a-3182">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3182">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-3183">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3183">Pattern</span></span>

<span data-ttu-id="b9e4a-3184">Huit chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3184">Eight consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-3185">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3185">Checksum</span></span>

<span data-ttu-id="b9e4a-3186">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3186">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-3187">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3187">Definition</span></span>

<span data-ttu-id="b9e4a-3188">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3188">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-3189">L’expression régulière Regex_sweden_passport_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3189">The regular expression Regex_sweden_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-3190">L’une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3190">One of the following is true:</span></span>
    - <span data-ttu-id="b9e4a-3191">Un mot clé figurant dans la liste Keyword_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3191">A keyword from Keyword_passport is found.</span></span>
    - <span data-ttu-id="b9e4a-3192">Un mot clé figurant dans la liste Keyword_sweden_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3192">A keyword from Keyword_sweden_passport is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-3193">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3193">Keywords</span></span>
   
#### <a name="keyword_sweden_passport"></a><span data-ttu-id="b9e4a-3194">Keyword_sweden_passport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3194">Keyword_sweden_passport</span></span>

- <span data-ttu-id="b9e4a-3195">exigences en matière de visa</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3195">visa requirements</span></span> 
- <span data-ttu-id="b9e4a-3196">Carte d’enregistrement d’une personne étrangère</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3196">Alien Registration Card</span></span> 
- <span data-ttu-id="b9e4a-3197">Visas Schengen</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3197">Schengen visas</span></span> 
- <span data-ttu-id="b9e4a-3198">Visa Schengen</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3198">Schengen visa</span></span> 
- <span data-ttu-id="b9e4a-3199">Traitement du visa</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3199">Visa Processing</span></span> 
- <span data-ttu-id="b9e4a-3200">Type de visa</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3200">Visa Type</span></span> 
- <span data-ttu-id="b9e4a-3201">Entrée unique</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3201">Single Entry</span></span> 
- <span data-ttu-id="b9e4a-3202">Entrée multiple</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3202">Multiple Entry</span></span> 
- <span data-ttu-id="b9e4a-3203">Frais de traitement G3</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3203">G3 Processing Fees</span></span> 

#### <a name="keyword_passport"></a><span data-ttu-id="b9e4a-3204">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3204">Keyword_passport</span></span>

- <span data-ttu-id="b9e4a-3205">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3205">Passport Number</span></span> 
- <span data-ttu-id="b9e4a-3206">N° de passeport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3206">Passport No</span></span> 
- <span data-ttu-id="b9e4a-3207"># Passeport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3207">Passport #</span></span> 
- <span data-ttu-id="b9e4a-3208">Tel #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3208">Passport#</span></span> 
- <span data-ttu-id="b9e4a-3209">PassportID</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3209">PassportID</span></span> 
- <span data-ttu-id="b9e4a-3210">N ° passeport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3210">Passportno</span></span> 
- <span data-ttu-id="b9e4a-3211">passportnumber</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3211">passportnumber</span></span> 
- <span data-ttu-id="b9e4a-3212">パスポート</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3212">パスポート</span></span> 
- <span data-ttu-id="b9e4a-3213">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3213">パスポート番号</span></span> 
- <span data-ttu-id="b9e4a-3214">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3214">パスポートのNum</span></span> 
- <span data-ttu-id="b9e4a-3215">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3215">パスポート＃</span></span> 
- <span data-ttu-id="b9e4a-3216">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3216">Numéro de passeport</span></span> 
- <span data-ttu-id="b9e4a-3217">Passeport n°</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3217">Passeport n °</span></span> 
- <span data-ttu-id="b9e4a-3218">Passeport numéro</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3218">Passeport Non</span></span> 
- <span data-ttu-id="b9e4a-3219"># Passeport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3219">Passeport #</span></span> 
- <span data-ttu-id="b9e4a-3220">Passeport #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3220">Passeport#</span></span> 
- <span data-ttu-id="b9e4a-3221">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3221">PasseportNon</span></span> 
- <span data-ttu-id="b9e4a-3222">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3222">Passeportn °</span></span> 
   
## <a name="swift-code"></a><span data-ttu-id="b9e4a-3223">Code SWIFT</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3223">SWIFT Code</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-3224">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3224">Format</span></span>

<span data-ttu-id="b9e4a-3225">Quatre lettres suivies de 5 à 31 lettres ou chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3225">Four letters followed by 5-31 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-3226">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3226">Pattern</span></span>

<span data-ttu-id="b9e4a-3227">Quatre lettres suivies de 5 à 31 lettres ou chiffres :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3227">Four letters followed by 5-31 letters or digits:</span></span>
- <span data-ttu-id="b9e4a-3228">Code bancaire à quatre lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3228">Four-letter bank code (not case sensitive)</span></span> 
- <span data-ttu-id="b9e4a-3229">Un espace facultatif</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3229">An optional space</span></span> 
- <span data-ttu-id="b9e4a-3230">4 à 28 lettres ou chiffres (numéro de compte bancaire de base (BBAN))</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3230">4-28 letters or digits (the Basic Bank Account Number (BBAN))</span></span> 
- <span data-ttu-id="b9e4a-3231">Un espace facultatif</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3231">An optional space</span></span> 
- <span data-ttu-id="b9e4a-3232">1 à 3 lettres ou chiffres (reste du BBAN)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3232">1-3 letters or digits (remainder of the BBAN)</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-3233">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3233">Checksum</span></span>

<span data-ttu-id="b9e4a-3234">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3234">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-3235">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3235">Definition</span></span>

<span data-ttu-id="b9e4a-3236">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3236">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-3237">L’expression régulière Regex_swift trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3237">The regular expression Regex_swift finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-3238">Un mot clé figurant dans la liste Keyword_swift est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3238">A keyword from Keyword_swift is found.</span></span>

```
<Entity id="cb2ab58c-9cb8-4c81-baf8-a4e106791df4" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_swift" />
        <Match idRef="Keyword_swift" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b9e4a-3239">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3239">Keywords</span></span>
   
#### <a name="keyword_swift"></a><span data-ttu-id="b9e4a-3240">Keyword_swift</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3240">Keyword_swift</span></span>

- <span data-ttu-id="b9e4a-3241">organisation internationale de normalisation 9362</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3241">international organization for standardization 9362</span></span> 
- <span data-ttu-id="b9e4a-3242">ISO 9362</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3242">iso 9362</span></span> 
- <span data-ttu-id="b9e4a-3243">iso9362</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3243">iso9362</span></span> 
- <span data-ttu-id="b9e4a-3244">rapide\#</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3244">swift\#</span></span> 
- <span data-ttu-id="b9e4a-3245">swiftcode</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3245">swiftcode</span></span> 
- <span data-ttu-id="b9e4a-3246">swiftnumber</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3246">swiftnumber</span></span> 
- <span data-ttu-id="b9e4a-3247">swiftroutingnumber</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3247">swiftroutingnumber</span></span> 
- <span data-ttu-id="b9e4a-3248">code swift</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3248">swift code</span></span> 
- <span data-ttu-id="b9e4a-3249"># numéro swift</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3249">swift number #</span></span> 
- <span data-ttu-id="b9e4a-3250">numéro d’acheminement swift</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3250">swift routing number</span></span> 
- <span data-ttu-id="b9e4a-3251">numéro BIC</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3251">bic number</span></span> 
- <span data-ttu-id="b9e4a-3252">code BIC</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3252">bic code</span></span> 
- <span data-ttu-id="b9e4a-3253">BIC\#</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3253">bic \#</span></span> 
- <span data-ttu-id="b9e4a-3254">BIC\#</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3254">bic\#</span></span> 
- <span data-ttu-id="b9e4a-3255">code d’identification bancaire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3255">bank identifier code</span></span> 
- <span data-ttu-id="b9e4a-3256">標準化 9362</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3256">標準化9362</span></span> 
- <span data-ttu-id="b9e4a-3257">迅速＃</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3257">迅速＃</span></span> 
- <span data-ttu-id="b9e4a-3258">SWIFTコード</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3258">SWIFTコード</span></span> 
- <span data-ttu-id="b9e4a-3259">SWIFT番号</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3259">SWIFT番号</span></span> 
- <span data-ttu-id="b9e4a-3260">迅速なルーティング番号</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3260">迅速なルーティング番号</span></span> 
- <span data-ttu-id="b9e4a-3261">BIC番号</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3261">BIC番号</span></span> 
- <span data-ttu-id="b9e4a-3262">BICコード</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3262">BICコード</span></span> 
- <span data-ttu-id="b9e4a-3263">銀行識別コードのための国際組織</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3263">銀行識別コードのための国際組織</span></span> 
- <span data-ttu-id="b9e4a-3264">Organisation internationale de normalisation 9362</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3264">Organisation internationale de normalisation 9362</span></span> 
- <span data-ttu-id="b9e4a-3265">rapide\#</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3265">rapide \#</span></span> 
- <span data-ttu-id="b9e4a-3266">code SWIFT</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3266">code SWIFT</span></span> 
- <span data-ttu-id="b9e4a-3267">le numéro de swift</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3267">le numéro de swift</span></span> 
- <span data-ttu-id="b9e4a-3268">swift numéro d’acheminement</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3268">swift numéro d'acheminement</span></span> 
- <span data-ttu-id="b9e4a-3269">le numéro BIC</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3269">le numéro BIC</span></span> 
- <span data-ttu-id="b9e4a-3270">\#BIC</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3270">\# BIC</span></span> 
- <span data-ttu-id="b9e4a-3271">code identificateur de banque</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3271">code identificateur de banque</span></span> 
   
## <a name="taiwan-national-id"></a><span data-ttu-id="b9e4a-3272">ID national à Taïwan</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3272">Taiwan National ID</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-3273">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3273">Format</span></span>

<span data-ttu-id="b9e4a-3274">Une lettre  suivie de neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3274">One letter (in English) followed by nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-3275">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3275">Pattern</span></span>

<span data-ttu-id="b9e4a-3276">Une lettre suivie de neuf chiffres :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3276">One letter (in English) followed by nine digits:</span></span>
- <span data-ttu-id="b9e4a-3277">Une lettre (en anglais, ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3277">One letter (in English, not case sensitive)</span></span> 
- <span data-ttu-id="b9e4a-3278">Le chiffre « 1 » ou « 2 »</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3278">The digit "1" or "2"</span></span> 
- <span data-ttu-id="b9e4a-3279">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3279">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-3280">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3280">Checksum</span></span>

<span data-ttu-id="b9e4a-3281">Oui</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3281">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-3282">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3282">Definition</span></span>

<span data-ttu-id="b9e4a-3283">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3283">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-3284">La fonction Func_taiwanese_national_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3284">The function Func_taiwanese_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-3285">Un mot clé figurant dans la liste Keyword_taiwanese_national_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3285">A keyword from Keyword_taiwanese_national_id is found.</span></span>
- <span data-ttu-id="b9e4a-3286">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3286">The checksum passes.</span></span>

```
<!-- Taiwanese National ID -->
<Entity id="4C7BFC34-8DD1-421D-8FB7-6C6182C2AF03" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_taiwanese_national_id" />
          <Match idRef="Keyword_taiwanese_national_id" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b9e4a-3287">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3287">Keywords</span></span>

#### <a name="keyword_taiwanese_national_id"></a><span data-ttu-id="b9e4a-3288">Keyword_taiwanese_national_id</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3288">Keyword_taiwanese_national_id</span></span>

- <span data-ttu-id="b9e4a-3289">身份證字號</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3289">身份證字號</span></span> 
- <span data-ttu-id="b9e4a-3290">身份證</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3290">身份證</span></span> 
- <span data-ttu-id="b9e4a-3291">身份證號碼</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3291">身份證號碼</span></span> 
- <span data-ttu-id="b9e4a-3292">身份證號</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3292">身份證號</span></span> 
- <span data-ttu-id="b9e4a-3293">身分證字號</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3293">身分證字號</span></span> 
- <span data-ttu-id="b9e4a-3294">身分證</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3294">身分證</span></span> 
- <span data-ttu-id="b9e4a-3295">身分證號碼</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3295">身分證號碼</span></span> 
- <span data-ttu-id="b9e4a-3296">身份證號</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3296">身份證號</span></span> 
- <span data-ttu-id="b9e4a-3297">身分證統一編號</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3297">身分證統一編號</span></span> 
- <span data-ttu-id="b9e4a-3298">國民身分證統一編號</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3298">國民身分證統一編號</span></span> 
- <span data-ttu-id="b9e4a-3299">簽名</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3299">簽名</span></span> 
- <span data-ttu-id="b9e4a-3300">蓋章</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3300">蓋章</span></span> 
- <span data-ttu-id="b9e4a-3301">簽名或蓋章</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3301">簽名或蓋章</span></span> 
- <span data-ttu-id="b9e4a-3302">簽章</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3302">簽章</span></span>   
   
## <a name="taiwan-passport-number"></a><span data-ttu-id="b9e4a-3303">	Numéro de passeport Taïwan</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3303">Taiwan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-3304">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3304">Format</span></span>

- <span data-ttu-id="b9e4a-3305">Numéro de passeport biométrique: neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3305">Biometric passport number: Nine digits</span></span>
- <span data-ttu-id="b9e4a-3306">Numéro de passeport non biométrique: neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3306">Non-biometric passport number: Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-3307">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3307">Pattern</span></span>
<span data-ttu-id="b9e4a-3308">Numéro de passeport biométrique:</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3308">Biometric passport number:</span></span>
- <span data-ttu-id="b9e4a-3309">Le chiffre « 3 » </span><span class="sxs-lookup"><span data-stu-id="b9e4a-3309">The digit "3"</span></span> 
- <span data-ttu-id="b9e4a-3310">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3310">Eight digits</span></span>

<span data-ttu-id="b9e4a-3311">Numéro de passeport non biométrique:</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3311">Non-biometric passport number:</span></span>
- <span data-ttu-id="b9e4a-3312">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3312">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-3313">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3313">Checksum</span></span>

<span data-ttu-id="b9e4a-3314">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3314">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-3315">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3315">Definition</span></span>

<span data-ttu-id="b9e4a-3316">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3316">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-3317">L’expression régulière Regex_taiwan_passport trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3317">The regular expression Regex_taiwan_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-3318">Un mot clé figurant dans la liste Keyword_taiwan_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3318">A keyword from Keyword_taiwan_passport is found.</span></span>

```
<!-- Taiwan Passport Number -->
<Entity id="e7251cb4-4c2c-41df-963e-924eb3dae04a" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_passport"/>
     <Match idRef="Keyword_taiwan_passport"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b9e4a-3319">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3319">Keywords</span></span>

#### <a name="keyword_taiwan_passport"></a><span data-ttu-id="b9e4a-3320">Keyword_taiwan_passport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3320">Keyword_taiwan_passport</span></span>

- <span data-ttu-id="b9e4a-3321">ROC passport number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3321">ROC passport number</span></span> 
- <span data-ttu-id="b9e4a-3322">Passport number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3322">Passport number</span></span> 
- <span data-ttu-id="b9e4a-3323">Passport no</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3323">Passport no</span></span> 
- <span data-ttu-id="b9e4a-3324">Passport Num</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3324">Passport Num</span></span> 
- <span data-ttu-id="b9e4a-3325">Passport #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3325">Passport #</span></span> 
- <span data-ttu-id="b9e4a-3326">护照</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3326">护照</span></span> 
- <span data-ttu-id="b9e4a-3327">中華民國護照</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3327">中華民國護照</span></span> 
- <span data-ttu-id="b9e4a-3328">Zhōnghuá Mínguó hùzhào</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3328">Zhōnghuá Mínguó hùzhào</span></span>
   
## <a name="taiwan-resident-certificate-arctarc-number"></a><span data-ttu-id="b9e4a-3329">Numéro de certificat de résident (ARC/TARC) Taïwan</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3329">Taiwan Resident Certificate (ARC/TARC) Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-3330">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3330">Format</span></span>

<span data-ttu-id="b9e4a-3331">10 lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3331">10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-3332">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3332">Pattern</span></span>

<span data-ttu-id="b9e4a-3333">10 lettres et chiffres :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3333">10 letters and digits:</span></span>
- <span data-ttu-id="b9e4a-3334">Deux lettres (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="b9e4a-3334">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="b9e4a-3335">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3335">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-3336">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3336">Checksum</span></span>

<span data-ttu-id="b9e4a-3337">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3337">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-3338">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3338">Definition</span></span>

<span data-ttu-id="b9e4a-3339">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3339">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-3340">L’expression régulière Regex_taiwan_resident_certificate trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3340">The regular expression Regex_taiwan_resident_certificate finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-3341">Un mot clé figurant dans la liste Keyword_taiwan_resident_certificate est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3341">A keyword from Keyword_taiwan_resident_certificate is found.</span></span>

```
<!-- Taiwan Resident Certificate (ARC/TARC) -->
<Entity id="48269fec-05ea-46ea-b326-f5623a58c6e9" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_resident_certificate"/>
     <Match idRef="Keyword_taiwan_resident_certificate"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b9e4a-3342">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3342">Keywords</span></span>

#### <a name="keyword_taiwan_resident_certificate"></a><span data-ttu-id="b9e4a-3343">Keyword_taiwan_resident_certificate</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3343">Keyword_taiwan_resident_certificate</span></span>

- <span data-ttu-id="b9e4a-3344">Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3344">Resident Certificate</span></span> 
- <span data-ttu-id="b9e4a-3345">Resident Cert</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3345">Resident Cert</span></span> 
- <span data-ttu-id="b9e4a-3346">Resident Cert.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3346">Resident Cert.</span></span> 
- <span data-ttu-id="b9e4a-3347">Identification card</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3347">Identification card</span></span> 
- <span data-ttu-id="b9e4a-3348">Alien Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3348">Alien Resident Certificate</span></span> 
- <span data-ttu-id="b9e4a-3349">ARC</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3349">ARC</span></span> 
- <span data-ttu-id="b9e4a-3350">Taiwan Area Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3350">Taiwan Area Resident Certificate</span></span> 
- <span data-ttu-id="b9e4a-3351">TARC</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3351">TARC</span></span> 
- <span data-ttu-id="b9e4a-3352">居留證</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3352">居留證</span></span> 
- <span data-ttu-id="b9e4a-3353">外僑居留證</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3353">外僑居留證</span></span> 
- <span data-ttu-id="b9e4a-3354">台灣地區居留證</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3354">台灣地區居留證</span></span> 

## <a name="thai-population-identification-code"></a><span data-ttu-id="b9e4a-3355">Code d’identification du remplissage thaï</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3355">Thai Population Identification Code</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-3356">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3356">Format</span></span>

<span data-ttu-id="b9e4a-3357">13 chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3357">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-3358">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3358">Pattern</span></span>

<span data-ttu-id="b9e4a-3359">13 chiffres :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3359">13 digits:</span></span>
- <span data-ttu-id="b9e4a-3360">Le premier chiffre est différent de 0 ou de 9</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3360">First digit is not 0 or 9</span></span> 
- <span data-ttu-id="b9e4a-3361">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3361">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-3362">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3362">Checksum</span></span>

<span data-ttu-id="b9e4a-3363">Oui</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3363">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-3364">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3364">Definition</span></span>

<span data-ttu-id="b9e4a-3365">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3365">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-3366">La fonction Func_Thai_Citizen_Id trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3366">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-3367">Un mot clé depuis Keyword_Thai_Citizen_Id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3367">A keyword from Keyword_Thai_Citizen_Id is found.</span></span>

<span data-ttu-id="b9e4a-3368">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3368">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-3369">La fonction Func_Thai_Citizen_Id trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3369">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-3370">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3370">Keywords</span></span>

#### <a name="keyword_thai_citizen_id"></a><span data-ttu-id="b9e4a-3371">Keyword_Thai_Citizen_Id</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3371">Keyword_Thai_Citizen_Id</span></span>

- <span data-ttu-id="b9e4a-3372">ID Number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3372">ID Number</span></span>
- <span data-ttu-id="b9e4a-3373">Numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3373">Identification Number</span></span>
- <span data-ttu-id="b9e4a-3374">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3374">บัตรประชาชน</span></span>
- <span data-ttu-id="b9e4a-3375">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3375">รหัสบัตรประชาชน</span></span>
- <span data-ttu-id="b9e4a-3376">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3376">บัตรประชาชน</span></span>
- <span data-ttu-id="b9e4a-3377">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3377">รหัสบัตรประชาชน</span></span>
  
## <a name="turkish-national-identification-number"></a><span data-ttu-id="b9e4a-3378">Numéro d’identification national turc</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3378">Turkish National Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-3379">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3379">Format</span></span>

<span data-ttu-id="b9e4a-3380">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3380">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-3381">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3381">Pattern</span></span>

<span data-ttu-id="b9e4a-3382">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3382">11 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-3383">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3383">Checksum</span></span>

<span data-ttu-id="b9e4a-3384">Oui</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3384">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-3385">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3385">Definition</span></span>

<span data-ttu-id="b9e4a-3386">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3386">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-3387">La fonction Func_Turkish_National_Id trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3387">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-3388">Un mot clé depuis Keyword_Turkish_National_Id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3388">A keyword from Keyword_Turkish_National_Id is found.</span></span>

<span data-ttu-id="b9e4a-3389">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3389">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-3390">La fonction Func_Turkish_National_Id trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3390">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-3391">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3391">Keywords</span></span>

#### <a name="keyword_turkish_national_id"></a><span data-ttu-id="b9e4a-3392">Keyword_Turkish_National_Id</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3392">Keyword_Turkish_National_Id</span></span>

- <span data-ttu-id="b9e4a-3393">TC Kimlik non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3393">TC Kimlik No</span></span>
- <span data-ttu-id="b9e4a-3394">TC Kimlik numarası</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3394">TC Kimlik numarası</span></span>
- <span data-ttu-id="b9e4a-3395">Vatandaşlık numarası</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3395">Vatandaşlık numarası</span></span>
- <span data-ttu-id="b9e4a-3396">Vatandaşlık non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3396">Vatandaşlık no</span></span>

## <a name="uk-drivers-license-number"></a><span data-ttu-id="b9e4a-p142">Numéro de permis de conduire Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="b9e4a-p142">U.K. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-3399">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3399">Format</span></span>

<span data-ttu-id="b9e4a-3400">Combinaison de 18 lettres et chiffres au format spécifié</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3400">Combination of 18 letters and digits in the specified format</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-3401">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3401">Pattern</span></span>

<span data-ttu-id="b9e4a-3402">18 lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3402">18 letters and digits:</span></span>
- <span data-ttu-id="b9e4a-3403">Cinq lettres (ne respectent pas la casse) ou le chiffre « 9 » à la place d’une lettre</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3403">Five letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="b9e4a-3404">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3404">One digit</span></span> 
- <span data-ttu-id="b9e4a-3405">Cinq chiffres au format de date JJMMA pour la date de naissance</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3405">Five digits in the date format DDMMY for date of birth</span></span> 
- <span data-ttu-id="b9e4a-3406">Deux lettres (ne respectent pas la casse) ou le chiffre « 9 » à la place d’une lettre</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3406">Two letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="b9e4a-3407">Cinq chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3407">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-3408">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3408">Checksum</span></span>

<span data-ttu-id="b9e4a-3409">Oui</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3409">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-3410">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3410">Definition</span></span>

<span data-ttu-id="b9e4a-3411">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3411">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-3412">La fonction Func_uk_drivers_license trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3412">The function Func_uk_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-3413">Un mot clé figurant dans la liste Keyword_uk_drivers_license est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3413">A keyword from Keyword_uk_drivers_license is found.</span></span>
- <span data-ttu-id="b9e4a-3414">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3414">The checksum passes.</span></span>

```
<!-- U.K. Driver's License Number -->
<Entity id="f93de4be-d94c-40df-a8be-461738047551" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_uk_drivers_license" />
        <Match idRef="Keyword_uk_drivers_license" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b9e4a-3415">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3415">Keywords</span></span>

#### <a name="keyword_uk_drivers_license"></a><span data-ttu-id="b9e4a-3416">Keyword_uk_drivers_license</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3416">Keyword_uk_drivers_license</span></span>

- <span data-ttu-id="b9e4a-3417">DVLA</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3417">DVLA</span></span> 
- <span data-ttu-id="b9e4a-3418">véhicule utilitaire léger</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3418">light vans</span></span> 
- <span data-ttu-id="b9e4a-3419">quadbikes</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3419">quadbikes</span></span> 
- <span data-ttu-id="b9e4a-3420">automobiles</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3420">motor cars</span></span> 
- <span data-ttu-id="b9e4a-3421">125cc</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3421">125cc</span></span> 
- <span data-ttu-id="b9e4a-3422">annexes</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3422">sidecar</span></span> 
- <span data-ttu-id="b9e4a-3423">tricycles</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3423">tricycles</span></span> 
- <span data-ttu-id="b9e4a-3424">Side</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3424">motorcycles</span></span> 
- <span data-ttu-id="b9e4a-3425">permis de conduire plastifié</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3425">photocard licence</span></span> 
- <span data-ttu-id="b9e4a-3426">apprentis conducteurs</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3426">learner drivers</span></span> 
- <span data-ttu-id="b9e4a-3427">titulaire du permis</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3427">licence holder</span></span> 
- <span data-ttu-id="b9e4a-3428">titulaires du permis</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3428">licence holders</span></span> 
- <span data-ttu-id="b9e4a-3429">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3429">driving licences</span></span> 
- <span data-ttu-id="b9e4a-3430">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3430">driving licence</span></span> 
- <span data-ttu-id="b9e4a-3431">voiture à double commande</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3431">dual control car</span></span> 
   
## <a name="uk-electoral-roll-number"></a><span data-ttu-id="b9e4a-p143">Numéro de liste électorale Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="b9e4a-p143">U.K. Electoral Roll Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-3434">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3434">Format</span></span>

<span data-ttu-id="b9e4a-3435">Deux lettres suivies de 1 à 4 chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3435">Two letters followed by 1-4 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-3436">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3436">Pattern</span></span>

<span data-ttu-id="b9e4a-3437">Deux lettres (ne respectant pas la casse) suivies de 1 à 4 chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3437">Two letters (not case sensitive) followed by 1-4 numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-3438">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3438">Checksum</span></span>

<span data-ttu-id="b9e4a-3439">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3439">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-3440">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3440">Definition</span></span>

<span data-ttu-id="b9e4a-3441">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3441">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-3442">L’expression régulière Regex_uk_electoral trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3442">The regular expression Regex_uk_electoral finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-3443">Un mot clé figurant dans la liste Keyword_uk_electoral est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3443">A keyword from Keyword_uk_electoral is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-3444">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3444">Keywords</span></span>

#### <a name="keyword_uk_electoral"></a><span data-ttu-id="b9e4a-3445">Keyword_uk_electoral</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3445">Keyword_uk_electoral</span></span>

- <span data-ttu-id="b9e4a-3446">nomination au conseil</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3446">council nomination</span></span> 
- <span data-ttu-id="b9e4a-3447">formulaire de nomination</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3447">nomination form</span></span> 
- <span data-ttu-id="b9e4a-3448">registre électoral</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3448">electoral register</span></span> 
- <span data-ttu-id="b9e4a-3449">liste électorale</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3449">electoral roll</span></span>

   
## <a name="uk-national-health-service-number"></a><span data-ttu-id="b9e4a-p144">Numéro national des services de santé Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="b9e4a-p144">U.K. National Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-3452">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3452">Format</span></span>

<span data-ttu-id="b9e4a-3453">10 à 17 chiffres séparés par des espaces</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3453">10-17 digits separated by spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-3454">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3454">Pattern</span></span>

<span data-ttu-id="b9e4a-3455">10 à 17 chiffres :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3455">10-17 digits:</span></span>
- <span data-ttu-id="b9e4a-3456">3 ou 10 chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3456">Either 3 or 10 digits</span></span> 
- <span data-ttu-id="b9e4a-3457">Un espace</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3457">A space</span></span> 
- <span data-ttu-id="b9e4a-3458">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3458">Three digits</span></span> 
- <span data-ttu-id="b9e4a-3459">Un espace</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3459">A space</span></span> 
- <span data-ttu-id="b9e4a-3460">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3460">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-3461">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3461">Checksum</span></span>

<span data-ttu-id="b9e4a-3462">Oui</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3462">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-3463">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3463">Definition</span></span>

<span data-ttu-id="b9e4a-3464">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3464">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-3465">La fonction Func_uk_nhs_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3465">The function Func_uk_nhs_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-3466">L’une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3466">One of the following is true:</span></span>
    - <span data-ttu-id="b9e4a-3467">Un mot clé figurant dans la liste Keyword_uk_nhs_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3467">A keyword from Keyword_uk_nhs_number is found.</span></span>
    - <span data-ttu-id="b9e4a-3468">Un mot clé figurant dans la liste Keyword_uk_nhs_number1 est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3468">A keyword from Keyword_uk_nhs_number1 is found.</span></span>
    - <span data-ttu-id="b9e4a-3469">Un mot clé figurant dans la liste Keyword_uk_nhs_number_dob est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3469">A keyword from Keyword_uk_nhs_number_dob is found.</span></span>
- <span data-ttu-id="b9e4a-3470">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3470">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-3471">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3471">Keywords</span></span>
   
#### <a name="keyword_uk_nhs_number"></a><span data-ttu-id="b9e4a-3472">Keyword_uk_nhs_number</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3472">Keyword_uk_nhs_number</span></span>

- <span data-ttu-id="b9e4a-3473">service national de santé</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3473">national health service</span></span> 
- <span data-ttu-id="b9e4a-3474">NHS</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3474">nhs</span></span> 
- <span data-ttu-id="b9e4a-3475">administration des services de santé</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3475">health services authority</span></span> 
- <span data-ttu-id="b9e4a-3476">administration de la santé</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3476">health authority</span></span>

#### <a name="keyword_uk_nhs_number1"></a><span data-ttu-id="b9e4a-3477">Keyword_uk_nhs_number1</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3477">Keyword_uk_nhs_number1</span></span>

- <span data-ttu-id="b9e4a-3478">id du patient</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3478">patient id</span></span> 
- <span data-ttu-id="b9e4a-3479">identification du patient</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3479">patient identification</span></span> 
- <span data-ttu-id="b9e4a-3480">n° patient</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3480">patient no</span></span> 
- <span data-ttu-id="b9e4a-3481">numéro de patient</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3481">patient number</span></span>

#### <a name="keyword_uk_nhs_number_dob"></a><span data-ttu-id="b9e4a-3482">Keyword_uk_nhs_number_dob</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3482">Keyword_uk_nhs_number_dob</span></span>

- <span data-ttu-id="b9e4a-3483">GP</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3483">GP</span></span> 
- <span data-ttu-id="b9e4a-3484">DOB</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3484">DOB</span></span> 
- <span data-ttu-id="b9e4a-3485">D. O. B</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3485">D.O.B</span></span> 
- <span data-ttu-id="b9e4a-3486">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3486">Date of Birth</span></span> 
- <span data-ttu-id="b9e4a-3487">Birth Date</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3487">Birth Date</span></span> 
   
## <a name="uk-national-insurance-number-nino"></a><span data-ttu-id="b9e4a-p145">Numéro d'assurance nationale (NINO) Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="b9e4a-p145">U.K. National Insurance Number (NINO)</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-3490">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3490">Format</span></span>

<span data-ttu-id="b9e4a-3491">7 caractères ou 9 caractères séparés par des espaces ou des tirets</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3491">7 characters or 9 characters separated by spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-3492">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3492">Pattern</span></span>

<span data-ttu-id="b9e4a-3493">Deux modèles possibles:</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3493">Two possible patterns:</span></span>

- <span data-ttu-id="b9e4a-3494">Deux lettres (valides NINOs Utilisez uniquement certains caractères dans ce préfixe, que ce modèle valide; ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3494">Two letters (valid NINOs use only certain characters in this prefix, which this pattern validates; not case sensitive)</span></span>
- <span data-ttu-id="b9e4a-3495">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3495">Six digits</span></span>
- <span data-ttu-id="b9e4a-3496">«A», «B», «C» ou «d» (comme le préfixe, seuls certains caractères sont autorisés dans le suffixe; ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3496">Either 'A', 'B', 'C', or 'D' (like the prefix, only certain characters are allowed in the suffix; not case sensitive)</span></span>

<span data-ttu-id="b9e4a-3497">OR</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3497">OR</span></span>

- <span data-ttu-id="b9e4a-3498">Deux lettres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3498">Two letters</span></span>
- <span data-ttu-id="b9e4a-3499">Un espace ou un tiret</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3499">A space or dash</span></span>
- <span data-ttu-id="b9e4a-3500">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3500">Two digits</span></span>
- <span data-ttu-id="b9e4a-3501">Un espace ou un tiret</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3501">A space or dash</span></span>
- <span data-ttu-id="b9e4a-3502">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3502">Two digits</span></span>
- <span data-ttu-id="b9e4a-3503">Un espace ou un tiret</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3503">A space or dash</span></span>
- <span data-ttu-id="b9e4a-3504">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3504">Two digits</span></span>
- <span data-ttu-id="b9e4a-3505">Un espace ou un tiret</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3505">A space or dash</span></span>
- <span data-ttu-id="b9e4a-3506">«A», «B», «C» ou «d»</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3506">Either 'A', 'B', 'C', or 'D'</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-3507">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3507">Checksum</span></span>

<span data-ttu-id="b9e4a-3508">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3508">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-3509">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3509">Definition</span></span>

<span data-ttu-id="b9e4a-3510">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3510">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-3511">La fonction Func_uk_nino trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3511">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-3512">Un mot clé figurant dans la liste Keyword_uk_nino est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3512">A keyword from Keyword_uk_nino is found.</span></span>

<span data-ttu-id="b9e4a-3513">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3513">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-3514">La fonction Func_uk_nino trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3514">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-3515">Aucun mot clé figurant dans la liste Keyword_uk_nino n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3515">No keyword from Keyword_uk_nino is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-3516">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3516">Keywords</span></span>

#### <a name="keyword_uk_nino"></a><span data-ttu-id="b9e4a-3517">Keyword_uk_nino</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3517">Keyword_uk_nino</span></span>

- <span data-ttu-id="b9e4a-3518">numéro d’assurance nationale</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3518">national insurance number</span></span> 
- <span data-ttu-id="b9e4a-3519">cotisations sociales</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3519">national insurance contributions</span></span> 
- <span data-ttu-id="b9e4a-3520">loi sur la protection</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3520">protection act</span></span> 
- <span data-ttu-id="b9e4a-3521">cotisations</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3521">insurance</span></span> 
- <span data-ttu-id="b9e4a-3522">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3522">social security number</span></span> 
- <span data-ttu-id="b9e4a-3523">demande d’assurance</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3523">insurance application</span></span> 
- <span data-ttu-id="b9e4a-3524">demande de soins médicaux</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3524">medical application</span></span> 
- <span data-ttu-id="b9e4a-3525">assurance sociale</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3525">social insurance</span></span> 
- <span data-ttu-id="b9e4a-3526">soins médicaux</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3526">medical attention</span></span> 
- <span data-ttu-id="b9e4a-3527">sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3527">social security</span></span> 
- <span data-ttu-id="b9e4a-3528">grande-bretagne</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3528">great britain</span></span> 
- <span data-ttu-id="b9e4a-3529">cotisations</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3529">insurance</span></span>    
   
## <a name="us--uk-passport-number"></a><span data-ttu-id="b9e4a-p146">Numéro de passeport États-Unis/Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="b9e4a-p146">U.S. / U.K. Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-3532">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3532">Format</span></span>

<span data-ttu-id="b9e4a-3533">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3533">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-3534">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3534">Pattern</span></span>

<span data-ttu-id="b9e4a-3535">Neuf chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3535">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-3536">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3536">Checksum</span></span>

<span data-ttu-id="b9e4a-3537">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3537">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-3538">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3538">Definition</span></span>

<span data-ttu-id="b9e4a-3539">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3539">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-3540">La fonction Func_usa_uk_passport trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3540">The function Func_usa_uk_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-3541">Un mot clé figurant dans la liste Keyword_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3541">A keyword from Keyword_passport is found.</span></span>

```
<Entity id="178ec42a-18b4-47cc-85c7-d62c92fd67f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_usa_uk_passport" />
        <Match idRef="Keyword_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b9e4a-3542">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3542">Keywords</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="b9e4a-3543">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3543">Keyword_passport</span></span>

- <span data-ttu-id="b9e4a-3544">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3544">Passport Number</span></span> 
- <span data-ttu-id="b9e4a-3545">N° de passeport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3545">Passport No</span></span> 
- <span data-ttu-id="b9e4a-3546"># Passeport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3546">Passport #</span></span> 
- <span data-ttu-id="b9e4a-3547">Tel #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3547">Passport#</span></span> 
- <span data-ttu-id="b9e4a-3548">PassportID</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3548">PassportID</span></span> 
- <span data-ttu-id="b9e4a-3549">N ° passeport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3549">Passportno</span></span> 
- <span data-ttu-id="b9e4a-3550">passportnumber</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3550">passportnumber</span></span> 
- <span data-ttu-id="b9e4a-3551">パスポート</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3551">パスポート</span></span> 
- <span data-ttu-id="b9e4a-3552">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3552">パスポート番号</span></span> 
- <span data-ttu-id="b9e4a-3553">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3553">パスポートのNum</span></span> 
- <span data-ttu-id="b9e4a-3554">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3554">パスポート＃</span></span> 
- <span data-ttu-id="b9e4a-3555">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3555">Numéro de passeport</span></span> 
- <span data-ttu-id="b9e4a-3556">Passeport n°</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3556">Passeport n °</span></span> 
- <span data-ttu-id="b9e4a-3557">Passeport numéro</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3557">Passeport Non</span></span> 
- <span data-ttu-id="b9e4a-3558"># Passeport</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3558">Passeport #</span></span> 
- <span data-ttu-id="b9e4a-3559">Passeport #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3559">Passeport#</span></span> 
- <span data-ttu-id="b9e4a-3560">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3560">PasseportNon</span></span> 
- <span data-ttu-id="b9e4a-3561">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3561">Passeportn °</span></span> 
   
## <a name="us-bank-account-number"></a><span data-ttu-id="b9e4a-3562">Numéro de compte bancaire États-Unis</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3562">U.S. Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-3563">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3563">Format</span></span>

<span data-ttu-id="b9e4a-3564">8-17 chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3564">8-17 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-3565">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3565">Pattern</span></span>

<span data-ttu-id="b9e4a-3566">8 à 17 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3566">8-17 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-3567">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3567">Checksum</span></span>

<span data-ttu-id="b9e4a-3568">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3568">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-3569">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3569">Definition</span></span>

<span data-ttu-id="b9e4a-3570">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3570">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-3571">L’expression régulière Regex_usa_bank_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3571">The regular expression Regex_usa_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-3572">Un mot clé figurant dans la liste Keyword_usa_Bank_Account est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3572">A keyword from Keyword_usa_Bank_Account is found.</span></span>

```
<!-- U.S. Bank Account Number -->
<Entity id="a2ce32a8-f935-4bb6-8e96-2a5157672e2c" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_usa_bank_account_number" />
        <Match idRef="Keyword_usa_Bank_Account" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b9e4a-3573">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3573">Keywords</span></span>

#### <a name="keyword_usa_bank_account"></a><span data-ttu-id="b9e4a-3574">Keyword_usa_Bank_Account</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3574">Keyword_usa_Bank_Account</span></span>

- <span data-ttu-id="b9e4a-3575">Numéro de compte courant</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3575">Checking Account Number</span></span> 
- <span data-ttu-id="b9e4a-3576">Compte courant</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3576">Checking Account</span></span> 
- <span data-ttu-id="b9e4a-3577"># compte courant</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3577">Checking Account #</span></span> 
- <span data-ttu-id="b9e4a-3578">Numéro compte courant</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3578">Checking Acct Number</span></span> 
- <span data-ttu-id="b9e4a-3579"># compte courant</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3579">Checking Acct #</span></span> 
- <span data-ttu-id="b9e4a-3580">N° de compte courant</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3580">Checking Acct No.</span></span> 
- <span data-ttu-id="b9e4a-3581">N° de compte courant</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3581">Checking Account No.</span></span> 
- <span data-ttu-id="b9e4a-3582">Numéro de compte bancaire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3582">Bank Account Number</span></span> 
- <span data-ttu-id="b9e4a-3583"># Compte bancaire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3583">Bank Account #</span></span> 
- <span data-ttu-id="b9e4a-3584">Numéro de compte bancaire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3584">Bank Acct Number</span></span> 
- <span data-ttu-id="b9e4a-3585"># Compte bancaire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3585">Bank Acct #</span></span> 
- <span data-ttu-id="b9e4a-3586">N° de compte bancaire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3586">Bank Acct No.</span></span> 
- <span data-ttu-id="b9e4a-3587">N° de compte bancaire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3587">Bank Account No.</span></span> 
- <span data-ttu-id="b9e4a-3588">Numéro de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3588">Savings Account Number</span></span> 
- <span data-ttu-id="b9e4a-3589">Compte d’épargne.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3589">Savings Account.</span></span> 
- <span data-ttu-id="b9e4a-3590">N° de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3590">Savings Account #</span></span> 
- <span data-ttu-id="b9e4a-3591">Numéro de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3591">Savings Acct Number</span></span> 
- <span data-ttu-id="b9e4a-3592"># compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3592">Savings Acct #</span></span> 
- <span data-ttu-id="b9e4a-3593">N° de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3593">Savings Acct No.</span></span> 
- <span data-ttu-id="b9e4a-3594">N° de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3594">Savings Account No.</span></span> 
- <span data-ttu-id="b9e4a-3595">Numéro de compte de débit</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3595">Debit Account Number</span></span> 
- <span data-ttu-id="b9e4a-3596">Compte de débit</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3596">Debit Account</span></span> 
- <span data-ttu-id="b9e4a-3597"># Compte de débit</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3597">Debit Account #</span></span> 
- <span data-ttu-id="b9e4a-3598">Numéro de compte de débit</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3598">Debit Acct Number</span></span> 
- <span data-ttu-id="b9e4a-3599"># Compte de débit</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3599">Debit Acct #</span></span> 
- <span data-ttu-id="b9e4a-3600">N° de compte de débit</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3600">Debit Acct No.</span></span> 
- <span data-ttu-id="b9e4a-3601">N° de compte de débit</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3601">Debit Account No.</span></span> 
   
## <a name="us-drivers-license-number"></a><span data-ttu-id="b9e4a-3602">Numéro de permis de conduire États-Unis</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3602">U.S. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-3603">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3603">Format</span></span>

<span data-ttu-id="b9e4a-3604">Dépend de l’État</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3604">Depends on the state</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-3605">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3605">Pattern</span></span>

<span data-ttu-id="b9e4a-3606">Dépend de l’État, par exemple, New York :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3606">Depends on the state -- for example, New York:</span></span>
- <span data-ttu-id="b9e4a-3607">Neuf chiffres au format DDD DDD DDD correspondront.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3607">Nine digits formatted like ddd ddd ddd will match.</span></span>
- <span data-ttu-id="b9e4a-3608">Neuf chiffres au format ddddddddd ne correspondront pas.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3608">Nine digits like ddddddddd will not match.</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-3609">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3609">Checksum</span></span>

<span data-ttu-id="b9e4a-3610">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3610">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-3611">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3611">Definition</span></span>

<span data-ttu-id="b9e4a-3612">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3612">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-3613">La fonction Func_new_york_drivers_license_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3613">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-3614">Un mot clé figurant dans la liste Keyword_[state_name]_drivers_license_name est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3614">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="b9e4a-3615">Un mot clé figurant dans la liste Keyword_us_drivers_license est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3615">A keyword from Keyword_us_drivers_license is found.</span></span>

<span data-ttu-id="b9e4a-3616">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3616">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-3617">La fonction Func_new_york_drivers_license_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3617">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-3618">Un mot clé figurant dans la liste Keyword_[state_name]_drivers_license_name est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3618">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="b9e4a-3619">Un mot clé figurant dans la liste Keyword_us_drivers_license_abbreviations est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3619">A keyword from Keyword_us_drivers_license_abbreviations is found.</span></span>
- <span data-ttu-id="b9e4a-3620">Aucun mot clé figurant dans la liste Keyword_us_drivers_license n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3620">No keyword from Keyword_us_drivers_license is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-3621">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3621">Keywords</span></span>

#### <a name="keyword_us_drivers_license_abbreviations"></a><span data-ttu-id="b9e4a-3622">Keyword_us_drivers_license_abbreviations</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3622">Keyword_us_drivers_license_abbreviations</span></span>

- <span data-ttu-id="b9e4a-3623">LD</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3623">DL</span></span> 
- <span data-ttu-id="b9e4a-3624">DISTRIBUTION</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3624">DLS</span></span> 
- <span data-ttu-id="b9e4a-3625">CÈDE</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3625">CDL</span></span> 
- <span data-ttu-id="b9e4a-3626">CDLS</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3626">CDLS</span></span> 
- <span data-ttu-id="b9e4a-3627">ID</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3627">ID</span></span> 
- <span data-ttu-id="b9e4a-3628">Codes</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3628">IDs</span></span> 
- <span data-ttu-id="b9e4a-3629">LD #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3629">DL#</span></span> 
- <span data-ttu-id="b9e4a-3630">DISTRIBUTION #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3630">DLS#</span></span> 
- <span data-ttu-id="b9e4a-3631">CÈDE #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3631">CDL#</span></span> 
- <span data-ttu-id="b9e4a-3632">CDLS #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3632">CDLS#</span></span> 
- <span data-ttu-id="b9e4a-3633">Réf #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3633">ID#</span></span>
- <span data-ttu-id="b9e4a-3634">Codes #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3634">IDs#</span></span> 
- <span data-ttu-id="b9e4a-3635">Numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3635">ID number</span></span> 
- <span data-ttu-id="b9e4a-3636">Numéros d’identification</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3636">ID numbers</span></span> 
- <span data-ttu-id="b9e4a-3637">Profil</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3637">LIC</span></span> 
- <span data-ttu-id="b9e4a-3638">Profil #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3638">LIC#</span></span> 

#### <a name="keyword_us_drivers_license"></a><span data-ttu-id="b9e4a-3639">Keyword_us_drivers_license</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3639">Keyword_us_drivers_license</span></span>

- <span data-ttu-id="b9e4a-3640">DriverLic</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3640">DriverLic</span></span> 
- <span data-ttu-id="b9e4a-3641">DriverLics</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3641">DriverLics</span></span> 
- <span data-ttu-id="b9e4a-3642">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3642">DriverLicense</span></span> 
- <span data-ttu-id="b9e4a-3643">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3643">DriverLicenses</span></span> 
- <span data-ttu-id="b9e4a-3644">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3644">Driver Lic</span></span> 
- <span data-ttu-id="b9e4a-3645">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3645">Driver Lics</span></span> 
- <span data-ttu-id="b9e4a-3646">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3646">Driver License</span></span> 
- <span data-ttu-id="b9e4a-3647">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3647">Driver Licenses</span></span> 
- <span data-ttu-id="b9e4a-3648">DriversLic</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3648">DriversLic</span></span> 
- <span data-ttu-id="b9e4a-3649">DriversLics</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3649">DriversLics</span></span> 
- <span data-ttu-id="b9e4a-3650">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3650">DriversLicense</span></span> 
- <span data-ttu-id="b9e4a-3651">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3651">DriversLicenses</span></span> 
- <span data-ttu-id="b9e4a-3652">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3652">Drivers Lic</span></span> 
- <span data-ttu-id="b9e4a-3653">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3653">Drivers Lics</span></span> 
- <span data-ttu-id="b9e4a-3654">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3654">Drivers License</span></span> 
- <span data-ttu-id="b9e4a-3655">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3655">Drivers Licenses</span></span> 
- <span data-ttu-id="b9e4a-3656">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3656">Driver'Lic</span></span> 
- <span data-ttu-id="b9e4a-3657">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3657">Driver'Lics</span></span> 
- <span data-ttu-id="b9e4a-3658">Driver'License</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3658">Driver'License</span></span> 
- <span data-ttu-id="b9e4a-3659">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3659">Driver'Licenses</span></span> 
- <span data-ttu-id="b9e4a-3660">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3660">Driver' Lic</span></span> 
- <span data-ttu-id="b9e4a-3661">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3661">Driver' Lics</span></span> 
- <span data-ttu-id="b9e4a-3662">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3662">Driver' License</span></span> 
- <span data-ttu-id="b9e4a-3663">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3663">Driver' Licenses</span></span>
- <span data-ttu-id="b9e4a-3664">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3664">Driver'sLic</span></span> 
- <span data-ttu-id="b9e4a-3665">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3665">Driver'sLics</span></span> 
- <span data-ttu-id="b9e4a-3666">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3666">Driver'sLicense</span></span> 
- <span data-ttu-id="b9e4a-3667">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3667">Driver'sLicenses</span></span> 
- <span data-ttu-id="b9e4a-3668">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3668">Driver's Lic</span></span> 
- <span data-ttu-id="b9e4a-3669">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3669">Driver's Lics</span></span> 
- <span data-ttu-id="b9e4a-3670">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3670">Driver's License</span></span> 
- <span data-ttu-id="b9e4a-3671">Driver’s Licenses</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3671">Driver's Licenses</span></span> 
- <span data-ttu-id="b9e4a-3672">numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3672">identification number</span></span> 
- <span data-ttu-id="b9e4a-3673">numéros d’identification</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3673">identification numbers</span></span> 
- <span data-ttu-id="b9e4a-3674"># identification</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3674">identification #</span></span> 
- <span data-ttu-id="b9e4a-3675">carte d’identité</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3675">id card</span></span> 
- <span data-ttu-id="b9e4a-3676">cartes d’identité</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3676">id cards</span></span> 
- <span data-ttu-id="b9e4a-3677">carte d’identification</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3677">identification card</span></span> 
- <span data-ttu-id="b9e4a-3678">cartes d’identification</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3678">identification cards</span></span> 
- <span data-ttu-id="b9e4a-3679">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3679">DriverLic#</span></span> 
- <span data-ttu-id="b9e4a-3680">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3680">DriverLics#</span></span> 
- <span data-ttu-id="b9e4a-3681">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3681">DriverLicense#</span></span> 
- <span data-ttu-id="b9e4a-3682">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3682">DriverLicenses#</span></span> 
- <span data-ttu-id="b9e4a-3683">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3683">Driver Lic#</span></span> 
- <span data-ttu-id="b9e4a-3684">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3684">Driver Lics#</span></span> 
- <span data-ttu-id="b9e4a-3685">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3685">Driver License#</span></span> 
- <span data-ttu-id="b9e4a-3686">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3686">Driver Licenses#</span></span> 
- <span data-ttu-id="b9e4a-3687">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3687">DriversLic#</span></span> 
- <span data-ttu-id="b9e4a-3688">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3688">DriversLics#</span></span> 
- <span data-ttu-id="b9e4a-3689">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3689">DriversLicense#</span></span> 
- <span data-ttu-id="b9e4a-3690">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3690">DriversLicenses#</span></span> 
- <span data-ttu-id="b9e4a-3691">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3691">Drivers Lic#</span></span> 
- <span data-ttu-id="b9e4a-3692">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3692">Drivers Lics#</span></span> 
- <span data-ttu-id="b9e4a-3693">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3693">Drivers License#</span></span> 
- <span data-ttu-id="b9e4a-3694">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3694">Drivers Licenses#</span></span> 
- <span data-ttu-id="b9e4a-3695">Driver'Lic #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3695">Driver'Lic#</span></span> 
- <span data-ttu-id="b9e4a-3696">Driver'Lics #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3696">Driver'Lics#</span></span> 
- <span data-ttu-id="b9e4a-3697">Driver'License #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3697">Driver'License#</span></span> 
- <span data-ttu-id="b9e4a-3698">Driver'Licenses #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3698">Driver'Licenses#</span></span> 
- <span data-ttu-id="b9e4a-3699">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3699">Driver' Lic#</span></span> 
- <span data-ttu-id="b9e4a-3700">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3700">Driver' Lics#</span></span> 
- <span data-ttu-id="b9e4a-3701">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3701">Driver' License#</span></span> 
- <span data-ttu-id="b9e4a-3702">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3702">Driver' Licenses#</span></span> 
- <span data-ttu-id="b9e4a-3703">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3703">Driver'sLic#</span></span> 
- <span data-ttu-id="b9e4a-3704">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3704">Driver'sLics#</span></span> 
- <span data-ttu-id="b9e4a-3705">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3705">Driver'sLicense#</span></span> 
- <span data-ttu-id="b9e4a-3706">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3706">Driver'sLicenses#</span></span> 
- <span data-ttu-id="b9e4a-3707">#Permisconduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3707">Driver's Lic#</span></span> 
- <span data-ttu-id="b9e4a-3708">#Permisconduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3708">Driver's Lics#</span></span> 
- <span data-ttu-id="b9e4a-3709">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3709">Driver's License#</span></span> 
- <span data-ttu-id="b9e4a-3710">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3710">Driver's Licenses#</span></span> 
- <span data-ttu-id="b9e4a-3711"># carte d’identité</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3711">id card#</span></span> 
- <span data-ttu-id="b9e4a-3712"># cartes d’identité</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3712">id cards#</span></span> 
- <span data-ttu-id="b9e4a-3713">#carte d’identification</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3713">identification card#</span></span> 
- <span data-ttu-id="b9e4a-3714">#cartes d’identification</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3714">identification cards#</span></span> 


#### <a name="keyword_state_name_drivers_license_name"></a><span data-ttu-id="b9e4a-3715">Keyword_[state_name]_drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3715">Keyword_[state_name]_drivers_license_name</span></span>

- <span data-ttu-id="b9e4a-3716">Abréviation de l’État (par exemple, « NY »)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3716">State abbreviation (for example, "NY")</span></span> 
- <span data-ttu-id="b9e4a-3717">Nom de l’État (par exemple, « New York »)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3717">State name (for example, "New York")</span></span>    
   
## <a name="us-individual-taxpayer-identification-number-itin"></a><span data-ttu-id="b9e4a-3718">Numéro d’identification fiscale individuel (ITIN) États-Unis</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3718">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-3719">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3719">Format</span></span>

<span data-ttu-id="b9e4a-3720">Neuf chiffres, le premier étant le « 9 », le quatrième le « 7 » ou le « 8 », éventuellement mis en forme avec des espaces ou des tirets</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3720">Nine digits that start with a "9" and contain a "7" or "8" as the fourth digit, optionally formatted with spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-3721">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3721">Pattern</span></span>

<span data-ttu-id="b9e4a-3722">Avec</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3722">Formatted:</span></span>
- <span data-ttu-id="b9e4a-3723">Le chiffre « 9 »</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3723">The digit "9"</span></span> 
- <span data-ttu-id="b9e4a-3724">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3724">Two digits</span></span> 
- <span data-ttu-id="b9e4a-3725">Un espace ou un tiret</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3725">A space or dash</span></span> 
- <span data-ttu-id="b9e4a-3726">Un « 7 » ou un « 8 »</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3726">A "7" or "8"</span></span> 
- <span data-ttu-id="b9e4a-3727">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3727">A digit</span></span> 
- <span data-ttu-id="b9e4a-3728">Un espace ou tiret</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3728">A space, or dash</span></span> 
- <span data-ttu-id="b9e4a-3729">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3729">Four digits</span></span>

<span data-ttu-id="b9e4a-3730">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3730">Unformatted:</span></span>
- <span data-ttu-id="b9e4a-3731">Le chiffre « 9 »</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3731">The digit "9"</span></span> 
- <span data-ttu-id="b9e4a-3732">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3732">Two digits</span></span> 
- <span data-ttu-id="b9e4a-3733">Un « 7 » ou un « 8 »</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3733">A "7" or "8"</span></span> 
- <span data-ttu-id="b9e4a-3734">Cinq chiffres</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3734">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-3735">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3735">Checksum</span></span>

<span data-ttu-id="b9e4a-3736">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3736">No</span></span>

### <a name="definition"></a><span data-ttu-id="b9e4a-3737">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3737">Definition</span></span>

<span data-ttu-id="b9e4a-3738">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3738">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-3739">La fonction Func_formatted_itin trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3739">The function Func_formatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-3740">Au moins une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3740">At least one of the following is true:</span></span>
    - <span data-ttu-id="b9e4a-3741">Un mot clé figurant dans la liste Keyword_itin est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3741">A keyword from Keyword_itin is found.</span></span>
    - <span data-ttu-id="b9e4a-3742">La fonction Func_us_address trouve une adresse au format correct.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3742">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="b9e4a-3743">La fonction Func_us_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3743">The function Func_us_date finds a date in the right date format.</span></span>
    - <span data-ttu-id="b9e4a-3744">Un mot clé figurant dans la liste Keyword_itin_collaborative est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3744">A keyword from Keyword_itin_collaborative is found.</span></span>

<span data-ttu-id="b9e4a-3745">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3745">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-3746">La fonction Func_unformatted_itin trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3746">The function Func_unformatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-3747">Au moins une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3747">At least one of the following is true:</span></span>
    - <span data-ttu-id="b9e4a-3748">Un mot clé figurant dans la liste Keyword_itin_collaborative est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3748">A keyword from Keyword_itin_collaborative is found.</span></span>
    - <span data-ttu-id="b9e4a-3749">La fonction Func_us_address trouve une adresse au format correct.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3749">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="b9e4a-3750">La fonction Func_us_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3750">The function Func_us_date finds a date in the right date format.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-3751">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3751">Keywords</span></span>

#### <a name="keyword_itin"></a><span data-ttu-id="b9e4a-3752">Keyword_itin</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3752">Keyword_itin</span></span>

- <span data-ttu-id="b9e4a-3753">redevable</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3753">taxpayer</span></span> 
- <span data-ttu-id="b9e4a-3754">id fiscal</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3754">tax id</span></span> 
- <span data-ttu-id="b9e4a-3755">identification fiscale</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3755">tax identification</span></span> 
- <span data-ttu-id="b9e4a-3756">itin</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3756">itin</span></span> 
- <span data-ttu-id="b9e4a-3757">SSN</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3757">ssn</span></span> 
- <span data-ttu-id="b9e4a-3758">Etain</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3758">tin</span></span> 
- <span data-ttu-id="b9e4a-3759">sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3759">social security</span></span> 
- <span data-ttu-id="b9e4a-3760">contribuable</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3760">tax payer</span></span> 
- <span data-ttu-id="b9e4a-3761">itins</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3761">itins</span></span> 
- <span data-ttu-id="b9e4a-3762">taxi</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3762">taxid</span></span> 
- <span data-ttu-id="b9e4a-3763">contribuable individuel</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3763">individual taxpayer</span></span> 

#### <a name="keyword_itin_collaborative"></a><span data-ttu-id="b9e4a-3764">Keyword_itin_collaborative</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3764">Keyword_itin_collaborative</span></span>

- <span data-ttu-id="b9e4a-3765">Licence</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3765">License</span></span> 
- <span data-ttu-id="b9e4a-3766">LD</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3766">DL</span></span> 
- <span data-ttu-id="b9e4a-3767">DOB</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3767">DOB</span></span> 
- <span data-ttu-id="b9e4a-3768">Birthdate</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3768">Birthdate</span></span> 
- <span data-ttu-id="b9e4a-3769">Birthday</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3769">Birthday</span></span> 
- <span data-ttu-id="b9e4a-3770">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3770">Date of Birth</span></span> 
   
## <a name="us-social-security-number-ssn"></a><span data-ttu-id="b9e4a-3771">Numéro de sécurité sociale (SSN) États-Unis</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3771">U.S. Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="b9e4a-3772">Format</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3772">Format</span></span>

<span data-ttu-id="b9e4a-3773">9 chiffres, qui peuvent être mis en forme ou non mis en forme</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3773">9 digits, which may be in a formatted or unformatted pattern</span></span>

> [!NOTE]
> <span data-ttu-id="b9e4a-3774">La mise en forme d’un numéro de sécurité sociale émis avant le milieu de l’année 2011 est fixe et certaines parties du numéro doivent se situer dans certaines plages pour qu’il soit valide (mais il n’y a pas de somme de contrôle).</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3774">If issued before mid-2011, an SSN has strong formatting where certain parts of the number must fall within certain ranges to be valid (but there's no checksum).</span></span>

### <a name="pattern"></a><span data-ttu-id="b9e4a-3775">Modèle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3775">Pattern</span></span>

<span data-ttu-id="b9e4a-3776">Quatre fonctions permettent de rechercher des numéros de sécurité sociale avec quatre différents modèles :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3776">Four functions look for SSNs in four different patterns:</span></span>
- <span data-ttu-id="b9e4a-3777">Func_ssn recherche des numéros de sécurité sociale avec une mise en forme fixe d’avant l’année 2011, mis en forme avec des tirets ou des espaces (ddd-dd-dddd OU ddd dd dddd)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3777">Func_ssn finds SSNs with pre-2011 strong formatting that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="b9e4a-3778">Func_unformatted_ssn recherche des numéros de sécurité sociale avec une mise en forme fixe d’avant l’année 2011, avec neuf chiffres consécutifs non mis en forme (ddddddddd)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3778">Func_unformatted_ssn finds SSNs with pre-2011 strong formatting that are unformatted as nine consecutive digits (ddddddddd)</span></span>
- <span data-ttu-id="b9e4a-3779">Func_randomized_formatted_ssn recherche des numéros de sécurité sociale d’après l’année 2011, mis en forme avec des tirets ou des espaces  (ddd-dd-dddd OU ddd dd dddd)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3779">Func_randomized_formatted_ssn finds post-2011 SSNs that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="b9e4a-3780">Func_randomized_unformatted_ssn recherche des numéros de sécurité sociale d’après l’année 2011, avec neuf chiffres consécutifs non mis en forme (ddddddddd)</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3780">Func_randomized_unformatted_ssn finds post-2011 SSNs that are unformatted as nine consecutive digits (ddddddddd)</span></span>

### <a name="checksum"></a><span data-ttu-id="b9e4a-3781">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3781">Checksum</span></span>

<span data-ttu-id="b9e4a-3782">Non</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3782">No</span></span>


### <a name="definition"></a><span data-ttu-id="b9e4a-3783">Définition</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3783">Definition</span></span>

<span data-ttu-id="b9e4a-3784">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3784">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-3785">La fonction Func_ssn trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3785">The function Func_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-3786">Un mot clé figurant dans la liste Keyword_ssn est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3786">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="b9e4a-3787">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3787">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-3788">La fonction Func_unformatted_ssn trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3788">The function Func_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-3789">Un mot clé figurant dans la liste Keyword_ssn est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3789">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="b9e4a-3790">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3790">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-3791">La fonction Func_randomized_formatted_ssn trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3791">The function Func_randomized_formatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-3792">Un mot clé figurant dans la liste Keyword_ssn est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3792">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="b9e4a-3793">La fonction Func_ssn ne trouve pas de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3793">The function Func_ssn does not find content that matches the pattern.</span></span>

<span data-ttu-id="b9e4a-3794">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 55 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3794">A DLP policy is 55% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="b9e4a-3795">La fonction Func_randomized_unformatted_ssn trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3795">The function Func_randomized_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="b9e4a-3796">Un mot clé figurant dans la liste Keyword_ssn est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3796">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="b9e4a-3797">La fonction Func_unformatted_ssn ne trouve pas de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3797">The function Func_unformatted_ssn does not find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="b9e4a-3798">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3798">Keywords</span></span>

#### <a name="keyword_ssn"></a><span data-ttu-id="b9e4a-3799">Keyword_ssn</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3799">Keyword_ssn</span></span>

- <span data-ttu-id="b9e4a-3800">Sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3800">Social Security</span></span> 
- <span data-ttu-id="b9e4a-3801"># sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3801">Social Security#</span></span> 
- <span data-ttu-id="b9e4a-3802">Sécu sociale</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3802">Soc Sec</span></span> 
- <span data-ttu-id="b9e4a-3803">SSN</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3803">SSN</span></span> 
- <span data-ttu-id="b9e4a-3804">NUMÉROS</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3804">SSNS</span></span> 
- <span data-ttu-id="b9e4a-3805">SSN #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3805">SSN#</span></span> 
- <span data-ttu-id="b9e4a-3806">SOCIALE #</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3806">SS#</span></span> 
- <span data-ttu-id="b9e4a-3807">Identifiant SSID</span><span class="sxs-lookup"><span data-stu-id="b9e4a-3807">SSID</span></span> 
   

