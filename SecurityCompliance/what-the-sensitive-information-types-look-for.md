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
ms.openlocfilehash: d486510c35aaf147e6d63e28d1df36ef689e3975
ms.sourcegitcommit: a5a7e43822336ed18d8f5879167766686cf6b2a3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2019
ms.locfileid: "36478253"
---
# <a name="what-the-sensitive-information-types-look-for"></a><span data-ttu-id="fd62e-104">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="fd62e-104">What the sensitive information types look for</span></span>

<span data-ttu-id="fd62e-105">La protection contre la perte de données (DLP) dans &amp; le centre de sécurité conformité Office 365 inclut de nombreux types d’informations sensibles que vous pouvez utiliser dans vos stratégies DLP.</span><span class="sxs-lookup"><span data-stu-id="fd62e-105">Data loss prevention (DLP) in the Office 365 Security &amp; Compliance Center includes many sensitive information types that are ready for you to use in your DLP policies.</span></span> <span data-ttu-id="fd62e-106">Cette rubrique répertorie tous ces types d'informations sensibles et indique ce qu'une stratégie DLP recherche pour chaque type.</span><span class="sxs-lookup"><span data-stu-id="fd62e-106">This topic lists all of these sensitive information types and shows what a DLP policy looks for when it detects each type.</span></span> <span data-ttu-id="fd62e-107">Un type d'informations sensibles est défini par un modèle qui peut être identifié par une fonction ou une expression régulière.</span><span class="sxs-lookup"><span data-stu-id="fd62e-107">A sensitive information type is defined by a pattern that can be identified by a regular expression or a function.</span></span> <span data-ttu-id="fd62e-108">En outre, des preuves corroborantes comme les mots clés et les sommes de contrôle peuvent être utilisées pour identifier un type d'informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="fd62e-108">In addition, corroborative evidence such as keywords and checksums can be used to identify a sensitive information type.</span></span> <span data-ttu-id="fd62e-109">Le niveau de confiance et la proximité sont également utilisés dans le processus d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="fd62e-109">Confidence level and proximity are also used in the evaluation process.</span></span>
  
## <a name="aba-routing-number"></a><span data-ttu-id="fd62e-110">Numéro de routage ABA</span><span class="sxs-lookup"><span data-stu-id="fd62e-110">ABA Routing Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-111">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-111">Format</span></span>

<span data-ttu-id="fd62e-112">9 chiffres mis en forme ou non mis en forme</span><span class="sxs-lookup"><span data-stu-id="fd62e-112">9 digits which may be in a formatted or unformatted pattern</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-113">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-113">Pattern</span></span>

<span data-ttu-id="fd62e-114">Avec</span><span class="sxs-lookup"><span data-stu-id="fd62e-114">Formatted:</span></span>
- <span data-ttu-id="fd62e-115">Quatre chiffres commençant par 0, 1, 2, 3, 6, 7 ou 8</span><span class="sxs-lookup"><span data-stu-id="fd62e-115">Four digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span>
- <span data-ttu-id="fd62e-116">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="fd62e-116">A hyphen</span></span>
- <span data-ttu-id="fd62e-117">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-117">Four digits</span></span>
- <span data-ttu-id="fd62e-118">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="fd62e-118">A hyphen</span></span>
- <span data-ttu-id="fd62e-119">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="fd62e-119">A digit</span></span>

<span data-ttu-id="fd62e-120">Non mis en forme: 9 chiffres consécutifs commençant par 0, 1, 2, 3, 6, 7 ou 8</span><span class="sxs-lookup"><span data-stu-id="fd62e-120">Unformatted: 9 consecutive digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span> 

### <a name="checksum"></a><span data-ttu-id="fd62e-121">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-121">Checksum</span></span>

<span data-ttu-id="fd62e-122">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-122">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-123">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-123">Definition</span></span>

<span data-ttu-id="fd62e-124">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-124">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-125">La fonction Func_aba_routing trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-125">The function Func_aba_routing finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-126">Un mot clé figurant dans la liste Keyword_ABA_Routing est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-126">A keyword from Keyword_ABA_Routing is found.</span></span>

```xml
<!-- ABA Routing Number -->
<Entity id="cb353f78-2b72-4c3c-8827-92ebe4f69fdf" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_aba_routing" />
        <Match idRef="Keyword_ABA_Routing" />
      </Pattern>
 </Entity>
```


### <a name="keywords"></a><span data-ttu-id="fd62e-127">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-127">Keywords</span></span>

#### <a name="keyword_aba_routing"></a><span data-ttu-id="fd62e-128">Keyword_ABA_Routing</span><span class="sxs-lookup"><span data-stu-id="fd62e-128">Keyword_ABA_Routing</span></span>

- <span data-ttu-id="fd62e-129">ABA</span><span class="sxs-lookup"><span data-stu-id="fd62e-129">aba</span></span>
- <span data-ttu-id="fd62e-130"># aba</span><span class="sxs-lookup"><span data-stu-id="fd62e-130">aba #</span></span>
- <span data-ttu-id="fd62e-131"># routage aba</span><span class="sxs-lookup"><span data-stu-id="fd62e-131">aba routing #</span></span>
- <span data-ttu-id="fd62e-132">numéro de routage aba</span><span class="sxs-lookup"><span data-stu-id="fd62e-132">aba routing number</span></span>
- <span data-ttu-id="fd62e-133">ABA #</span><span class="sxs-lookup"><span data-stu-id="fd62e-133">aba#</span></span>
- <span data-ttu-id="fd62e-134">abarouting #</span><span class="sxs-lookup"><span data-stu-id="fd62e-134">abarouting#</span></span>
- <span data-ttu-id="fd62e-135">numéro aba</span><span class="sxs-lookup"><span data-stu-id="fd62e-135">aba number</span></span>
- <span data-ttu-id="fd62e-136">abaroutingnumber</span><span class="sxs-lookup"><span data-stu-id="fd62e-136">abaroutingnumber</span></span>
- <span data-ttu-id="fd62e-137"># routage american bank association</span><span class="sxs-lookup"><span data-stu-id="fd62e-137">american bank association routing #</span></span>
- <span data-ttu-id="fd62e-138">numéro de routage american bank association</span><span class="sxs-lookup"><span data-stu-id="fd62e-138">american bank association routing number</span></span>
- <span data-ttu-id="fd62e-139">americanbankassociationrouting #</span><span class="sxs-lookup"><span data-stu-id="fd62e-139">americanbankassociationrouting#</span></span>
- <span data-ttu-id="fd62e-140">americanbankassociationroutingnumber</span><span class="sxs-lookup"><span data-stu-id="fd62e-140">americanbankassociationroutingnumber</span></span>
- <span data-ttu-id="fd62e-141">numéro de routage bancaire</span><span class="sxs-lookup"><span data-stu-id="fd62e-141">bank routing number</span></span>
- <span data-ttu-id="fd62e-142">bankrouting #</span><span class="sxs-lookup"><span data-stu-id="fd62e-142">bankrouting#</span></span>
- <span data-ttu-id="fd62e-143">bankroutingnumber</span><span class="sxs-lookup"><span data-stu-id="fd62e-143">bankroutingnumber</span></span>
- <span data-ttu-id="fd62e-144">numéro de routage</span><span class="sxs-lookup"><span data-stu-id="fd62e-144">routing transit number</span></span>
- <span data-ttu-id="fd62e-145">RTN</span><span class="sxs-lookup"><span data-stu-id="fd62e-145">RTN</span></span> 
   
## <a name="argentina-national-identity-dni-number"></a><span data-ttu-id="fd62e-146">Numéro d’identité nationale (DNI) pour l’Argentine</span><span class="sxs-lookup"><span data-stu-id="fd62e-146">Argentina National Identity (DNI) Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-147">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-147">Format</span></span>

<span data-ttu-id="fd62e-148">Huit chiffres séparés par des points</span><span class="sxs-lookup"><span data-stu-id="fd62e-148">Eight digits separated by periods</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-149">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-149">Pattern</span></span>

<span data-ttu-id="fd62e-150">Huit chiffres :</span><span class="sxs-lookup"><span data-stu-id="fd62e-150">Eight digits:</span></span>
- <span data-ttu-id="fd62e-151">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-151">Two digits</span></span>
- <span data-ttu-id="fd62e-152">Un point </span><span class="sxs-lookup"><span data-stu-id="fd62e-152">A period</span></span>
- <span data-ttu-id="fd62e-153">Trois chiffres </span><span class="sxs-lookup"><span data-stu-id="fd62e-153">Three digits</span></span>
- <span data-ttu-id="fd62e-154">Un point </span><span class="sxs-lookup"><span data-stu-id="fd62e-154">A period</span></span>
- <span data-ttu-id="fd62e-155">Trois chiffres </span><span class="sxs-lookup"><span data-stu-id="fd62e-155">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-156">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-156">Checksum</span></span>

<span data-ttu-id="fd62e-157">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-157">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-158">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-158">Definition</span></span>

<span data-ttu-id="fd62e-159">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-159">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-160">L’expression régulière Regex_argentina_national_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-160">The regular expression Regex_argentina_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-161">Un mot clé figurant dans la liste Keyword_argentina_national_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-161">A keyword from Keyword_argentina_national_id is found.</span></span>

```xml
<!-- Argentina National Identity (DNI) Number -->
<Entity id="eefbb00e-8282-433c-8620-8f1da3bffdb2" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_argentina_national_id"/>
      <Match idRef="Keyword_argentina_national_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fd62e-162">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-162">Keywords</span></span>

#### <a name="keyword_argentina_national_id"></a><span data-ttu-id="fd62e-163">Keyword_argentina_national_id</span><span class="sxs-lookup"><span data-stu-id="fd62e-163">Keyword_argentina_national_id</span></span>

- <span data-ttu-id="fd62e-164">Argentina National Identity number</span><span class="sxs-lookup"><span data-stu-id="fd62e-164">Argentina National Identity number</span></span> 
- <span data-ttu-id="fd62e-165">Identité</span><span class="sxs-lookup"><span data-stu-id="fd62e-165">Identity</span></span> 
- <span data-ttu-id="fd62e-166">Identification de la carte d’identité nationale</span><span class="sxs-lookup"><span data-stu-id="fd62e-166">Identification National Identity Card</span></span> 
- <span data-ttu-id="fd62e-167">DNI</span><span class="sxs-lookup"><span data-stu-id="fd62e-167">DNI</span></span> 
- <span data-ttu-id="fd62e-168">Carte d’interface réseau nationale du registre des personnes</span><span class="sxs-lookup"><span data-stu-id="fd62e-168">NIC National Registry of Persons</span></span> 
- <span data-ttu-id="fd62e-169">Documento Nacional de Identidad</span><span class="sxs-lookup"><span data-stu-id="fd62e-169">Documento Nacional de Identidad</span></span> 
- <span data-ttu-id="fd62e-170">Registro Nacional de las Personas</span><span class="sxs-lookup"><span data-stu-id="fd62e-170">Registro Nacional de las Personas</span></span> 
- <span data-ttu-id="fd62e-171">Identidad</span><span class="sxs-lookup"><span data-stu-id="fd62e-171">Identidad</span></span> 
- <span data-ttu-id="fd62e-172">Identificación</span><span class="sxs-lookup"><span data-stu-id="fd62e-172">Identificación</span></span> 
   
## <a name="australia-bank-account-number"></a><span data-ttu-id="fd62e-173">Numéro de compte bancaire Australie</span><span class="sxs-lookup"><span data-stu-id="fd62e-173">Australia Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-174">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-174">Format</span></span>

<span data-ttu-id="fd62e-175">6 à 10 chiffres avec ou sans le numéro d’agence bancaire de l’État</span><span class="sxs-lookup"><span data-stu-id="fd62e-175">6-10 digits with or without a bank state branch number</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-176">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-176">Pattern</span></span>

<span data-ttu-id="fd62e-177">Le numéro de compte est composé de 6 à 10 chiffres.</span><span class="sxs-lookup"><span data-stu-id="fd62e-177">Account number is 6-10 digits.</span></span>
<span data-ttu-id="fd62e-178">Numéro de succursale bancaire en Australie :</span><span class="sxs-lookup"><span data-stu-id="fd62e-178">Australia bank state branch number:</span></span>
- <span data-ttu-id="fd62e-179">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-179">Three digits</span></span> 
- <span data-ttu-id="fd62e-180">Un trait d’union</span><span class="sxs-lookup"><span data-stu-id="fd62e-180">A hyphen</span></span> 
- <span data-ttu-id="fd62e-181">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-181">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-182">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-182">Checksum</span></span>

<span data-ttu-id="fd62e-183">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-183">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-184">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-184">Definition</span></span>

<span data-ttu-id="fd62e-185">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-185">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-186">L’expression régulière Regex_australia_bank_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-186">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="fd62e-187">Un mot clé figurant dans la liste Keyword_australia_bank_account_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-187">A keyword from Keyword_australia_bank_account_number is found.</span></span>
- <span data-ttu-id="fd62e-188">L’expression régulière Regex_australia_bank_account_number_bsb trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-188">The regular expression Regex_australia_bank_account_number_bsb finds content that matches the pattern.</span></span>

<span data-ttu-id="fd62e-189">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-189">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-190">L’expression régulière Regex_australia_bank_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-190">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="fd62e-191">Un mot clé figurant dans la liste Keyword_australia_bank_account_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-191">A keyword from Keyword_australia_bank_account_number is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-192">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-192">Keywords</span></span>

#### <a name="keyword_australia_bank_account_number"></a><span data-ttu-id="fd62e-193">Keyword_australia_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="fd62e-193">Keyword_australia_bank_account_number</span></span>

- <span data-ttu-id="fd62e-194">code swift banque</span><span class="sxs-lookup"><span data-stu-id="fd62e-194">swift bank code</span></span>
- <span data-ttu-id="fd62e-195">banque correspondante</span><span class="sxs-lookup"><span data-stu-id="fd62e-195">correspondent bank</span></span>
- <span data-ttu-id="fd62e-196">devise de base</span><span class="sxs-lookup"><span data-stu-id="fd62e-196">base currency</span></span>
- <span data-ttu-id="fd62e-197">compte aux États-Unis</span><span class="sxs-lookup"><span data-stu-id="fd62e-197">usa account</span></span>
- <span data-ttu-id="fd62e-198">adresse du titulaire</span><span class="sxs-lookup"><span data-stu-id="fd62e-198">holder address</span></span>
- <span data-ttu-id="fd62e-199">adresse de la banque</span><span class="sxs-lookup"><span data-stu-id="fd62e-199">bank address</span></span>
- <span data-ttu-id="fd62e-200">informations du compte</span><span class="sxs-lookup"><span data-stu-id="fd62e-200">information account</span></span>
- <span data-ttu-id="fd62e-201">transferts de fonds</span><span class="sxs-lookup"><span data-stu-id="fd62e-201">fund transfers</span></span>
- <span data-ttu-id="fd62e-202">frais bancaires</span><span class="sxs-lookup"><span data-stu-id="fd62e-202">bank charges</span></span>
- <span data-ttu-id="fd62e-203">informations sur la banque</span><span class="sxs-lookup"><span data-stu-id="fd62e-203">bank details</span></span>
- <span data-ttu-id="fd62e-204">informations bancaires</span><span class="sxs-lookup"><span data-stu-id="fd62e-204">banking information</span></span>
- <span data-ttu-id="fd62e-205">noms complets</span><span class="sxs-lookup"><span data-stu-id="fd62e-205">full names</span></span>
- <span data-ttu-id="fd62e-206">auront</span><span class="sxs-lookup"><span data-stu-id="fd62e-206">iaea</span></span>

   
## <a name="australia-drivers-license-number"></a><span data-ttu-id="fd62e-207">Numéro de permis de conduire Australie</span><span class="sxs-lookup"><span data-stu-id="fd62e-207">Australia Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-208">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-208">Format</span></span>

<span data-ttu-id="fd62e-209">Neuf lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-209">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-210">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-210">Pattern</span></span>

<span data-ttu-id="fd62e-211">Neuf lettres et chiffres :</span><span class="sxs-lookup"><span data-stu-id="fd62e-211">Nine letters and digits:</span></span> 

- <span data-ttu-id="fd62e-212">Deux chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="fd62e-212">Two digits or letters (not case sensitive)</span></span> 
- <span data-ttu-id="fd62e-213">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-213">Two digits</span></span> 
- <span data-ttu-id="fd62e-214">Cinq chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="fd62e-214">Five digits or letters (not case sensitive)</span></span>

<span data-ttu-id="fd62e-215">OR</span><span class="sxs-lookup"><span data-stu-id="fd62e-215">OR</span></span>

- <span data-ttu-id="fd62e-216">1 ou 2 lettres facultatives (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="fd62e-216">1-2 optional letters (not case sensitive)</span></span> 
- <span data-ttu-id="fd62e-217">4 à 9 chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-217">4-9 digits</span></span>

<span data-ttu-id="fd62e-218">OR</span><span class="sxs-lookup"><span data-stu-id="fd62e-218">OR</span></span>

- <span data-ttu-id="fd62e-219">Neuf chiffres ou lettres (ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="fd62e-219">Nine digits or letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-220">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-220">Checksum</span></span>

<span data-ttu-id="fd62e-221">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-221">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-222">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-222">Definition</span></span>

<span data-ttu-id="fd62e-223">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-223">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-224">L’expression régulière Regex_australia_drivers_license_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-224">The regular expression Regex_australia_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-225">Un mot clé figurant dans la liste Keyword_australia_drivers_license_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-225">A keyword from Keyword_australia_drivers_license_number is found.</span></span>
- <span data-ttu-id="fd62e-226">Aucun mot clé figurant dans la liste Keyword_australia_drivers_license_number_exclusions n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-226">No keyword from Keyword_australia_drivers_license_number_exclusions is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-227">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-227">Keywords</span></span>

#### <a name="keyword_australia_drivers_license_number"></a><span data-ttu-id="fd62e-228">Keyword_australia_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="fd62e-228">Keyword_australia_drivers_license_number</span></span>

- <span data-ttu-id="fd62e-229">permis de conduite internationaux</span><span class="sxs-lookup"><span data-stu-id="fd62e-229">international driving permits</span></span>
- <span data-ttu-id="fd62e-230">australian automobile association</span><span class="sxs-lookup"><span data-stu-id="fd62e-230">australian automobile association</span></span>
- <span data-ttu-id="fd62e-231">permis de conduite international</span><span class="sxs-lookup"><span data-stu-id="fd62e-231">international driving permit</span></span>
- <span data-ttu-id="fd62e-232">DriverLicence</span><span class="sxs-lookup"><span data-stu-id="fd62e-232">DriverLicence</span></span>
- <span data-ttu-id="fd62e-233">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="fd62e-233">DriverLicences</span></span>
- <span data-ttu-id="fd62e-234">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-234">Driver Lic</span></span>
- <span data-ttu-id="fd62e-235">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-235">Driver Licence</span></span>
- <span data-ttu-id="fd62e-236">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-236">Driver Licences</span></span>
- <span data-ttu-id="fd62e-237">DriversLic</span><span class="sxs-lookup"><span data-stu-id="fd62e-237">DriversLic</span></span>
- <span data-ttu-id="fd62e-238">DriversLicence</span><span class="sxs-lookup"><span data-stu-id="fd62e-238">DriversLicence</span></span>
- <span data-ttu-id="fd62e-239">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="fd62e-239">DriversLicences</span></span>
- <span data-ttu-id="fd62e-240">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-240">Drivers Lic</span></span>
- <span data-ttu-id="fd62e-241">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-241">Drivers Lics</span></span>
- <span data-ttu-id="fd62e-242">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-242">Drivers Licence</span></span>
- <span data-ttu-id="fd62e-243">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-243">Drivers Licences</span></span>
- <span data-ttu-id="fd62e-244">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="fd62e-244">Driver'Lic</span></span>
- <span data-ttu-id="fd62e-245">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="fd62e-245">Driver'Lics</span></span>
- <span data-ttu-id="fd62e-246">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="fd62e-246">Driver'Licence</span></span>
- <span data-ttu-id="fd62e-247">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="fd62e-247">Driver'Licences</span></span>
- <span data-ttu-id="fd62e-248">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-248">Driver' Lic</span></span>
- <span data-ttu-id="fd62e-249">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-249">Driver' Lics</span></span>
- <span data-ttu-id="fd62e-250">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-250">Driver' Licence</span></span>
- <span data-ttu-id="fd62e-251">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-251">Driver' Licences</span></span>
- <span data-ttu-id="fd62e-252">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="fd62e-252">Driver'sLic</span></span>
- <span data-ttu-id="fd62e-253">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="fd62e-253">Driver'sLics</span></span>
- <span data-ttu-id="fd62e-254">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="fd62e-254">Driver'sLicence</span></span>
- <span data-ttu-id="fd62e-255">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="fd62e-255">Driver'sLicences</span></span>
- <span data-ttu-id="fd62e-256">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-256">Driver's Lic</span></span>
- <span data-ttu-id="fd62e-257">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-257">Driver's Lics</span></span>
- <span data-ttu-id="fd62e-258">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-258">Driver's Licence</span></span>
- <span data-ttu-id="fd62e-259">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-259">Driver's Licences</span></span>
- <span data-ttu-id="fd62e-260">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="fd62e-260">DriverLic#</span></span>
- <span data-ttu-id="fd62e-261">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="fd62e-261">DriverLics#</span></span>
- <span data-ttu-id="fd62e-262">DriverLicence #</span><span class="sxs-lookup"><span data-stu-id="fd62e-262">DriverLicence#</span></span>
- <span data-ttu-id="fd62e-263">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="fd62e-263">DriverLicences#</span></span>
- <span data-ttu-id="fd62e-264">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-264">Driver Lic#</span></span>
- <span data-ttu-id="fd62e-265">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-265">Driver Lics#</span></span>
- <span data-ttu-id="fd62e-266">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-266">Driver Licence#</span></span>
- <span data-ttu-id="fd62e-267">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-267">Driver Licences#</span></span>
- <span data-ttu-id="fd62e-268">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="fd62e-268">DriversLic#</span></span>
- <span data-ttu-id="fd62e-269">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="fd62e-269">DriversLics#</span></span>
- <span data-ttu-id="fd62e-270">DriversLicence #</span><span class="sxs-lookup"><span data-stu-id="fd62e-270">DriversLicence#</span></span>
- <span data-ttu-id="fd62e-271">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="fd62e-271">DriversLicences#</span></span>
- <span data-ttu-id="fd62e-272">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-272">Drivers Lic#</span></span>
- <span data-ttu-id="fd62e-273">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-273">Drivers Lics#</span></span>
- <span data-ttu-id="fd62e-274">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-274">Drivers Licence#</span></span>
- <span data-ttu-id="fd62e-275">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-275">Drivers Licences#</span></span>
- <span data-ttu-id="fd62e-276">Driver'Lic #</span><span class="sxs-lookup"><span data-stu-id="fd62e-276">Driver'Lic#</span></span>
- <span data-ttu-id="fd62e-277">Driver'Lics #</span><span class="sxs-lookup"><span data-stu-id="fd62e-277">Driver'Lics#</span></span>
- <span data-ttu-id="fd62e-278">Driver'Licence #</span><span class="sxs-lookup"><span data-stu-id="fd62e-278">Driver'Licence#</span></span>
- <span data-ttu-id="fd62e-279">Driver'Licences #</span><span class="sxs-lookup"><span data-stu-id="fd62e-279">Driver'Licences#</span></span>
- <span data-ttu-id="fd62e-280">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-280">Driver' Lic#</span></span>
- <span data-ttu-id="fd62e-281">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-281">Driver' Lics#</span></span>
- <span data-ttu-id="fd62e-282">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-282">Driver' Licence#</span></span>
- <span data-ttu-id="fd62e-283">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-283">Driver' Licences#</span></span>
- <span data-ttu-id="fd62e-284">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="fd62e-284">Driver'sLic#</span></span>
- <span data-ttu-id="fd62e-285">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="fd62e-285">Driver'sLics#</span></span>
- <span data-ttu-id="fd62e-286">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="fd62e-286">Driver'sLicence#</span></span>
- <span data-ttu-id="fd62e-287">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="fd62e-287">Driver'sLicences#</span></span>
- <span data-ttu-id="fd62e-288">#Permisconduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-288">Driver's Lic#</span></span>
- <span data-ttu-id="fd62e-289">#Permisconduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-289">Driver's Lics#</span></span>
- <span data-ttu-id="fd62e-290">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-290">Driver's Licence#</span></span>
- <span data-ttu-id="fd62e-291">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-291">Driver's Licences#</span></span> 

#### <a name="keyword_australia_drivers_license_number_exclusions"></a><span data-ttu-id="fd62e-292">Keyword_australia_drivers_license_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="fd62e-292">Keyword_australia_drivers_license_number_exclusions</span></span>

- <span data-ttu-id="fd62e-293">AAA</span><span class="sxs-lookup"><span data-stu-id="fd62e-293">aaa</span></span>
- <span data-ttu-id="fd62e-294">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="fd62e-294">DriverLicense</span></span>
- <span data-ttu-id="fd62e-295">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="fd62e-295">DriverLicenses</span></span>
- <span data-ttu-id="fd62e-296">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-296">Driver License</span></span>
- <span data-ttu-id="fd62e-297">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-297">Driver Licenses</span></span>
- <span data-ttu-id="fd62e-298">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="fd62e-298">DriversLicense</span></span>
- <span data-ttu-id="fd62e-299">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="fd62e-299">DriversLicenses</span></span>
- <span data-ttu-id="fd62e-300">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-300">Drivers License</span></span>
- <span data-ttu-id="fd62e-301">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-301">Drivers Licenses</span></span>
- <span data-ttu-id="fd62e-302">Driver'License</span><span class="sxs-lookup"><span data-stu-id="fd62e-302">Driver'License</span></span>
- <span data-ttu-id="fd62e-303">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="fd62e-303">Driver'Licenses</span></span>
- <span data-ttu-id="fd62e-304">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-304">Driver' License</span></span>
- <span data-ttu-id="fd62e-305">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-305">Driver' Licenses</span></span>
- <span data-ttu-id="fd62e-306">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="fd62e-306">Driver'sLicense</span></span>
- <span data-ttu-id="fd62e-307">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="fd62e-307">Driver'sLicenses</span></span>
- <span data-ttu-id="fd62e-308">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-308">Driver's License</span></span>
- <span data-ttu-id="fd62e-309">Driver’s Licenses</span><span class="sxs-lookup"><span data-stu-id="fd62e-309">Driver's Licenses</span></span>
- <span data-ttu-id="fd62e-310">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="fd62e-310">DriverLicense#</span></span>
- <span data-ttu-id="fd62e-311">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="fd62e-311">DriverLicenses#</span></span>
- <span data-ttu-id="fd62e-312">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-312">Driver License#</span></span>
- <span data-ttu-id="fd62e-313">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-313">Driver Licenses#</span></span>
- <span data-ttu-id="fd62e-314">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="fd62e-314">DriversLicense#</span></span>
- <span data-ttu-id="fd62e-315">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="fd62e-315">DriversLicenses#</span></span>
- <span data-ttu-id="fd62e-316">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-316">Drivers License#</span></span>
- <span data-ttu-id="fd62e-317">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-317">Drivers Licenses#</span></span>
- <span data-ttu-id="fd62e-318">Driver'License #</span><span class="sxs-lookup"><span data-stu-id="fd62e-318">Driver'License#</span></span>
- <span data-ttu-id="fd62e-319">Driver'Licenses #</span><span class="sxs-lookup"><span data-stu-id="fd62e-319">Driver'Licenses#</span></span>
- <span data-ttu-id="fd62e-320">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-320">Driver' License#</span></span>
- <span data-ttu-id="fd62e-321">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-321">Driver' Licenses#</span></span>
- <span data-ttu-id="fd62e-322">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="fd62e-322">Driver'sLicense#</span></span>
- <span data-ttu-id="fd62e-323">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="fd62e-323">Driver'sLicenses#</span></span>
- <span data-ttu-id="fd62e-324">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-324">Driver's License#</span></span>
- <span data-ttu-id="fd62e-325">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-325">Driver's Licenses#</span></span>
   
## <a name="australia-medical-account-number"></a><span data-ttu-id="fd62e-326">Numéro de dossier médical Australie</span><span class="sxs-lookup"><span data-stu-id="fd62e-326">Australia Medical Account Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-327">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-327">Format</span></span>

<span data-ttu-id="fd62e-328">10 à 11 chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-328">10-11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-329">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-329">Pattern</span></span>

<span data-ttu-id="fd62e-330">10 à 11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="fd62e-330">10-11 digits:</span></span>
- <span data-ttu-id="fd62e-331">Le premier chiffre est compris entre 2 et 6</span><span class="sxs-lookup"><span data-stu-id="fd62e-331">First digit is in the range 2-6</span></span>
- <span data-ttu-id="fd62e-332">Le neuvième chiffre est un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-332">Ninth digit is a check digit</span></span>
- <span data-ttu-id="fd62e-333">Le dixième chiffre est le chiffre d’émission</span><span class="sxs-lookup"><span data-stu-id="fd62e-333">Tenth digit is the issue digit</span></span>
- <span data-ttu-id="fd62e-334">Le onzième chiffre (facultatif) est le numéro individuel</span><span class="sxs-lookup"><span data-stu-id="fd62e-334">Eleventh digit (optional) is the individual number</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-335">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-335">Checksum</span></span>

<span data-ttu-id="fd62e-336">Oui</span><span class="sxs-lookup"><span data-stu-id="fd62e-336">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-337">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-337">Definition</span></span>

<span data-ttu-id="fd62e-338">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 95 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-338">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-339">La fonction Func_australian_medical_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-339">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-340">Un mot clé figurant dans la liste Keyword_Australia_Medical_Account_Number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-340">A keyword from Keyword_Australia_Medical_Account_Number is found.</span></span>
- <span data-ttu-id="fd62e-341">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-341">The checksum passes.</span></span>

<span data-ttu-id="fd62e-342">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-342">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-343">La fonction Func_australian_medical_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-343">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-344">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-344">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-345">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-345">Keywords</span></span>

#### <a name="keyword_australia_medical_account_number"></a><span data-ttu-id="fd62e-346">Keyword_Australia_Medical_Account_Number</span><span class="sxs-lookup"><span data-stu-id="fd62e-346">Keyword_Australia_Medical_Account_Number</span></span>

- <span data-ttu-id="fd62e-347">informations sur le compte bancaire</span><span class="sxs-lookup"><span data-stu-id="fd62e-347">bank account details</span></span>
- <span data-ttu-id="fd62e-348">remboursements d’assurance maladie</span><span class="sxs-lookup"><span data-stu-id="fd62e-348">medicare payments</span></span>
- <span data-ttu-id="fd62e-349">compte de prêts immobiliers</span><span class="sxs-lookup"><span data-stu-id="fd62e-349">mortgage account</span></span>
- <span data-ttu-id="fd62e-350">paiements bancaires</span><span class="sxs-lookup"><span data-stu-id="fd62e-350">bank payments</span></span>
- <span data-ttu-id="fd62e-351">direction de l’information</span><span class="sxs-lookup"><span data-stu-id="fd62e-351">information branch</span></span>
- <span data-ttu-id="fd62e-352">prêt sur carte de crédit</span><span class="sxs-lookup"><span data-stu-id="fd62e-352">credit card loan</span></span>
- <span data-ttu-id="fd62e-353">département des services sociaux</span><span class="sxs-lookup"><span data-stu-id="fd62e-353">department of human services</span></span>
- <span data-ttu-id="fd62e-354">service local</span><span class="sxs-lookup"><span data-stu-id="fd62e-354">local service</span></span>
- <span data-ttu-id="fd62e-355">médicaux</span><span class="sxs-lookup"><span data-stu-id="fd62e-355">medicare</span></span>

   
## <a name="australia-passport-number"></a><span data-ttu-id="fd62e-356">Numéro de passeport Australie</span><span class="sxs-lookup"><span data-stu-id="fd62e-356">Australia Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-357">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-357">Format</span></span>

<span data-ttu-id="fd62e-358">Une lettre suivie de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-358">A letter followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-359">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-359">Pattern</span></span>

<span data-ttu-id="fd62e-360">Une lettre (ne respectant pas la casse) suivie de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-360">A letter (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-361">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-361">Checksum</span></span>

<span data-ttu-id="fd62e-362">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-362">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-363">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-363">Definition</span></span>

<span data-ttu-id="fd62e-364">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-365">L’expression régulière Regex_australia_passport_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-365">The regular expression Regex_australia_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-366">Un mot clé depuis Keyword_passport ou Keyword_australia_passport_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-366">A keyword from Keyword_passport or Keyword_australia_passport_number is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-367">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-367">Keywords</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="fd62e-368">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="fd62e-368">Keyword_passport</span></span>

- <span data-ttu-id="fd62e-369">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="fd62e-369">Passport Number</span></span>
- <span data-ttu-id="fd62e-370">N° de passeport</span><span class="sxs-lookup"><span data-stu-id="fd62e-370">Passport No</span></span>
- <span data-ttu-id="fd62e-371"># Passeport</span><span class="sxs-lookup"><span data-stu-id="fd62e-371">Passport #</span></span>
- <span data-ttu-id="fd62e-372">Tel #</span><span class="sxs-lookup"><span data-stu-id="fd62e-372">Passport#</span></span>
- <span data-ttu-id="fd62e-373">PassportID</span><span class="sxs-lookup"><span data-stu-id="fd62e-373">PassportID</span></span>
- <span data-ttu-id="fd62e-374">N ° passeport</span><span class="sxs-lookup"><span data-stu-id="fd62e-374">Passportno</span></span>
- <span data-ttu-id="fd62e-375">passportnumber</span><span class="sxs-lookup"><span data-stu-id="fd62e-375">passportnumber</span></span>
- <span data-ttu-id="fd62e-376">パスポート</span><span class="sxs-lookup"><span data-stu-id="fd62e-376">パスポート</span></span>
- <span data-ttu-id="fd62e-377">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="fd62e-377">パスポート番号</span></span>
- <span data-ttu-id="fd62e-378">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="fd62e-378">パスポートのNum</span></span>
- <span data-ttu-id="fd62e-379">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="fd62e-379">パスポート ＃</span></span> 
- <span data-ttu-id="fd62e-380">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="fd62e-380">Numéro de passeport</span></span>
- <span data-ttu-id="fd62e-381">Passeport n°</span><span class="sxs-lookup"><span data-stu-id="fd62e-381">Passeport n °</span></span>
- <span data-ttu-id="fd62e-382">Passeport numéro</span><span class="sxs-lookup"><span data-stu-id="fd62e-382">Passeport Non</span></span>
- <span data-ttu-id="fd62e-383"># Passeport</span><span class="sxs-lookup"><span data-stu-id="fd62e-383">Passeport #</span></span>
- <span data-ttu-id="fd62e-384">Passeport #</span><span class="sxs-lookup"><span data-stu-id="fd62e-384">Passeport#</span></span>
- <span data-ttu-id="fd62e-385">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="fd62e-385">PasseportNon</span></span>
- <span data-ttu-id="fd62e-386">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="fd62e-386">Passeportn °</span></span>

#### <a name="keyword_australia_passport_number"></a><span data-ttu-id="fd62e-387">Keyword_australia_passport_number</span><span class="sxs-lookup"><span data-stu-id="fd62e-387">Keyword_australia_passport_number</span></span>

- <span data-ttu-id="fd62e-388">tel</span><span class="sxs-lookup"><span data-stu-id="fd62e-388">passport</span></span>
- <span data-ttu-id="fd62e-389">informations sur le passeport</span><span class="sxs-lookup"><span data-stu-id="fd62e-389">passport details</span></span>
- <span data-ttu-id="fd62e-390">immigration et citoyenneté</span><span class="sxs-lookup"><span data-stu-id="fd62e-390">immigration and citizenship</span></span>
- <span data-ttu-id="fd62e-391">Australie</span><span class="sxs-lookup"><span data-stu-id="fd62e-391">commonwealth of australia</span></span>
- <span data-ttu-id="fd62e-392">service de l’immigration</span><span class="sxs-lookup"><span data-stu-id="fd62e-392">department of immigration</span></span>
- <span data-ttu-id="fd62e-393">adresse de résidence</span><span class="sxs-lookup"><span data-stu-id="fd62e-393">residential address</span></span>
- <span data-ttu-id="fd62e-394">service de l’immigration et de la citoyenneté</span><span class="sxs-lookup"><span data-stu-id="fd62e-394">department of immigration and citizenship</span></span>
- <span data-ttu-id="fd62e-395">délivrance</span><span class="sxs-lookup"><span data-stu-id="fd62e-395">visa</span></span>
- <span data-ttu-id="fd62e-396">Carte nationale d’identité</span><span class="sxs-lookup"><span data-stu-id="fd62e-396">national identity card</span></span>
- <span data-ttu-id="fd62e-397">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="fd62e-397">passport number</span></span>
- <span data-ttu-id="fd62e-398">document de voyage</span><span class="sxs-lookup"><span data-stu-id="fd62e-398">travel document</span></span>
- <span data-ttu-id="fd62e-399">autorité émettrice</span><span class="sxs-lookup"><span data-stu-id="fd62e-399">issuing authority</span></span>
   
## <a name="australia-tax-file-number"></a><span data-ttu-id="fd62e-400">Numéro de dossier fiscal Australie</span><span class="sxs-lookup"><span data-stu-id="fd62e-400">Australia Tax File Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-401">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-401">Format</span></span>

<span data-ttu-id="fd62e-402">8 ou 9 chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-402">8-9 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-403">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-403">Pattern</span></span>

<span data-ttu-id="fd62e-404">8 à 9 chiffres généralement entrecoupés d’espaces comme suit :</span><span class="sxs-lookup"><span data-stu-id="fd62e-404">8-9 digits typically presented with spaces as follows:</span></span>
- <span data-ttu-id="fd62e-405">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-405">Three digits</span></span> 
- <span data-ttu-id="fd62e-406">Un espace facultatif</span><span class="sxs-lookup"><span data-stu-id="fd62e-406">An optional space</span></span> 
- <span data-ttu-id="fd62e-407">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-407">Three digits</span></span> 
- <span data-ttu-id="fd62e-408">Un espace facultatif</span><span class="sxs-lookup"><span data-stu-id="fd62e-408">An optional space</span></span> 
- <span data-ttu-id="fd62e-409">2 à 3 chiffres où le dernier chiffre est un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-409">2-3 digits where the last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-410">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-410">Checksum</span></span>

<span data-ttu-id="fd62e-411">Oui</span><span class="sxs-lookup"><span data-stu-id="fd62e-411">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-412">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-412">Definition</span></span>

<span data-ttu-id="fd62e-413">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-413">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-414">La fonction Func_australian_tax_file_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-414">The function Func_australian_tax_file_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-415">Aucun mot clé figurant dans la liste Keyword_Australia_Tax_File_Number ou Keyword_number_exclusions n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-415">No keyword from Keyword_Australia_Tax_File_Number or Keyword_number_exclusions is found.</span></span>
- <span data-ttu-id="fd62e-416">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-416">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-417">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-417">Keywords</span></span>

#### <a name="keyword_australia_tax_file_number"></a><span data-ttu-id="fd62e-418">Keyword_Australia_Tax_File_Number</span><span class="sxs-lookup"><span data-stu-id="fd62e-418">Keyword_Australia_Tax_File_Number</span></span>

- <span data-ttu-id="fd62e-419">numéro d’entreprise australien</span><span class="sxs-lookup"><span data-stu-id="fd62e-419">australian business number</span></span>
- <span data-ttu-id="fd62e-420">taux d’imposition marginale</span><span class="sxs-lookup"><span data-stu-id="fd62e-420">marginal tax rate</span></span>
- <span data-ttu-id="fd62e-421">prélèvement d’assurance maladie</span><span class="sxs-lookup"><span data-stu-id="fd62e-421">medicare levy</span></span>
- <span data-ttu-id="fd62e-422">numéro de portefeuille</span><span class="sxs-lookup"><span data-stu-id="fd62e-422">portfolio number</span></span>
- <span data-ttu-id="fd62e-423">service des vétérans</span><span class="sxs-lookup"><span data-stu-id="fd62e-423">service veterans</span></span>
- <span data-ttu-id="fd62e-424">retenue à la source</span><span class="sxs-lookup"><span data-stu-id="fd62e-424">withholding tax</span></span>
- <span data-ttu-id="fd62e-425">déclaration d’impôts individuels</span><span class="sxs-lookup"><span data-stu-id="fd62e-425">individual tax return</span></span>
- <span data-ttu-id="fd62e-426">numéro de dossier fiscal</span><span class="sxs-lookup"><span data-stu-id="fd62e-426">tax file number</span></span>

#### <a name="keyword_number_exclusions"></a><span data-ttu-id="fd62e-427">Keyword_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="fd62e-427">Keyword_number_exclusions</span></span>

- <span data-ttu-id="fd62e-428">00000000</span><span class="sxs-lookup"><span data-stu-id="fd62e-428">00000000</span></span>
- <span data-ttu-id="fd62e-429">11111111</span><span class="sxs-lookup"><span data-stu-id="fd62e-429">11111111</span></span>
- <span data-ttu-id="fd62e-430">22222222</span><span class="sxs-lookup"><span data-stu-id="fd62e-430">22222222</span></span>
- <span data-ttu-id="fd62e-431">33333333</span><span class="sxs-lookup"><span data-stu-id="fd62e-431">33333333</span></span>
- <span data-ttu-id="fd62e-432">44444444</span><span class="sxs-lookup"><span data-stu-id="fd62e-432">44444444</span></span>
- <span data-ttu-id="fd62e-433">55555555</span><span class="sxs-lookup"><span data-stu-id="fd62e-433">55555555</span></span>
- <span data-ttu-id="fd62e-434">66666666</span><span class="sxs-lookup"><span data-stu-id="fd62e-434">66666666</span></span>
- <span data-ttu-id="fd62e-435">77777777</span><span class="sxs-lookup"><span data-stu-id="fd62e-435">77777777</span></span>
- <span data-ttu-id="fd62e-436">88888888</span><span class="sxs-lookup"><span data-stu-id="fd62e-436">88888888</span></span>
- <span data-ttu-id="fd62e-437">99999999</span><span class="sxs-lookup"><span data-stu-id="fd62e-437">99999999</span></span>
- <span data-ttu-id="fd62e-438">000000000</span><span class="sxs-lookup"><span data-stu-id="fd62e-438">000000000</span></span>
- <span data-ttu-id="fd62e-439">111111111</span><span class="sxs-lookup"><span data-stu-id="fd62e-439">111111111</span></span>
- <span data-ttu-id="fd62e-440">222222222</span><span class="sxs-lookup"><span data-stu-id="fd62e-440">222222222</span></span>
- <span data-ttu-id="fd62e-441">333333333</span><span class="sxs-lookup"><span data-stu-id="fd62e-441">333333333</span></span>
- <span data-ttu-id="fd62e-442">444444444</span><span class="sxs-lookup"><span data-stu-id="fd62e-442">444444444</span></span>
- <span data-ttu-id="fd62e-443">555555555</span><span class="sxs-lookup"><span data-stu-id="fd62e-443">555555555</span></span>
- <span data-ttu-id="fd62e-444">666666666</span><span class="sxs-lookup"><span data-stu-id="fd62e-444">666666666</span></span>
- <span data-ttu-id="fd62e-445">777777777</span><span class="sxs-lookup"><span data-stu-id="fd62e-445">777777777</span></span>
- <span data-ttu-id="fd62e-446">888888888</span><span class="sxs-lookup"><span data-stu-id="fd62e-446">888888888</span></span>
- <span data-ttu-id="fd62e-447">999999999</span><span class="sxs-lookup"><span data-stu-id="fd62e-447">999999999</span></span>
- <span data-ttu-id="fd62e-448">0000000000</span><span class="sxs-lookup"><span data-stu-id="fd62e-448">0000000000</span></span>
- <span data-ttu-id="fd62e-449">1111111111</span><span class="sxs-lookup"><span data-stu-id="fd62e-449">1111111111</span></span>
- <span data-ttu-id="fd62e-450">2222222222</span><span class="sxs-lookup"><span data-stu-id="fd62e-450">2222222222</span></span>
- <span data-ttu-id="fd62e-451">3333333333</span><span class="sxs-lookup"><span data-stu-id="fd62e-451">3333333333</span></span>
- <span data-ttu-id="fd62e-452">4444444444</span><span class="sxs-lookup"><span data-stu-id="fd62e-452">4444444444</span></span>
- <span data-ttu-id="fd62e-453">5555555555</span><span class="sxs-lookup"><span data-stu-id="fd62e-453">5555555555</span></span>
- <span data-ttu-id="fd62e-454">6666666666</span><span class="sxs-lookup"><span data-stu-id="fd62e-454">6666666666</span></span>
- <span data-ttu-id="fd62e-455">7777777777</span><span class="sxs-lookup"><span data-stu-id="fd62e-455">7777777777</span></span>
- <span data-ttu-id="fd62e-456">8888888888</span><span class="sxs-lookup"><span data-stu-id="fd62e-456">8888888888</span></span>
- <span data-ttu-id="fd62e-457">9999999999</span><span class="sxs-lookup"><span data-stu-id="fd62e-457">9999999999</span></span>

## <a name="azure-documentdb-auth-key"></a><span data-ttu-id="fd62e-458">Clé d’authentification Azure DocumentDB</span><span class="sxs-lookup"><span data-stu-id="fd62e-458">Azure DocumentDB Auth Key</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-459">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-459">Format</span></span>

<span data-ttu-id="fd62e-460">La chaîne «DocumentDb» suivie des caractères et des chaînes présentés dans le modèle ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="fd62e-460">The string "DocumentDb" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-461">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-461">Pattern</span></span>

- <span data-ttu-id="fd62e-462">La chaîne «DocumentDb»</span><span class="sxs-lookup"><span data-stu-id="fd62e-462">The string "DocumentDb"</span></span>
- <span data-ttu-id="fd62e-463">N’importe quelle combinaison entre 3-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="fd62e-463">Any combination of between 3-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="fd62e-464">Symbole supérieur à (>), signe égal (=), guillemet (") ou apostrophe (')</span><span class="sxs-lookup"><span data-stu-id="fd62e-464">A greater than symbol (>), an equal sign (=), a quotation mark ("), or an apostrophe (')</span></span>
- <span data-ttu-id="fd62e-465">Toute combinaison de 86 lettres majuscules ou minuscules, des chiffres, une barre oblique (/) ou un signe plus (+)</span><span class="sxs-lookup"><span data-stu-id="fd62e-465">Any combination of 86 lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="fd62e-466">Deux signes égal (=)</span><span class="sxs-lookup"><span data-stu-id="fd62e-466">Two equal signs (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-467">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-467">Checksum</span></span>

<span data-ttu-id="fd62e-468">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-468">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-469">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-469">Definition</span></span>

<span data-ttu-id="fd62e-470">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-470">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-471">L’expression régulière CEP_Regex_AzureDocumentDBAuthKey trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-471">The regular expression CEP_Regex_AzureDocumentDBAuthKey finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-472">L’expression régulière CEP_CommonExampleKeywords ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-472">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-473">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-473">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="fd62e-474">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="fd62e-474">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="fd62e-475">(Notez que techniquement, ce type d’informations sensibles identifie ces mots clés à l’aide d’une expression régulière, et non d’une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="fd62e-475">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="fd62e-476">contoso</span><span class="sxs-lookup"><span data-stu-id="fd62e-476">contoso</span></span>
- <span data-ttu-id="fd62e-477">société</span><span class="sxs-lookup"><span data-stu-id="fd62e-477">fabrikam</span></span>
- <span data-ttu-id="fd62e-478">Northwind</span><span class="sxs-lookup"><span data-stu-id="fd62e-478">northwind</span></span>
- <span data-ttu-id="fd62e-479">immédiatement</span><span class="sxs-lookup"><span data-stu-id="fd62e-479">sandbox</span></span>
- <span data-ttu-id="fd62e-480">onebox</span><span class="sxs-lookup"><span data-stu-id="fd62e-480">onebox</span></span>
- <span data-ttu-id="fd62e-481">hôte</span><span class="sxs-lookup"><span data-stu-id="fd62e-481">localhost</span></span>
- <span data-ttu-id="fd62e-482">bouclage</span><span class="sxs-lookup"><span data-stu-id="fd62e-482">127.0.0.1</span></span>
- <span data-ttu-id="fd62e-483">testacs.</span><span class="sxs-lookup"><span data-stu-id="fd62e-483">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="fd62e-484">com</span><span class="sxs-lookup"><span data-stu-id="fd62e-484">com</span></span>
- <span data-ttu-id="fd62e-485">s-int.</span><span class="sxs-lookup"><span data-stu-id="fd62e-485">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="fd62e-486">NET</span><span class="sxs-lookup"><span data-stu-id="fd62e-486">net</span></span>

## <a name="azure-iaas-database-connection-string-and-azure-sql-connection-string"></a><span data-ttu-id="fd62e-487">Chaîne de connexion à la base de données IAAS Azure et chaîne de connexion Azure SQL</span><span class="sxs-lookup"><span data-stu-id="fd62e-487">Azure IAAS Database Connection String and Azure SQL Connection String</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-488">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-488">Format</span></span>

<span data-ttu-id="fd62e-489">La chaîne «Server», «Server» ou «Data source» suivie des caractères et des chaînes décrits dans le modèle ci-dessous, y compris la chaîne «cloudapp. Azure.</span><span class="sxs-lookup"><span data-stu-id="fd62e-489">The string "Server", "server", or "data source" followed by the characters and strings outlined in the pattern below, including the string "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="fd62e-490">com» ou «cloudapp. Azure.</span><span class="sxs-lookup"><span data-stu-id="fd62e-490">com" or "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="fd62e-491">NET "ou" Database. Windows.</span><span class="sxs-lookup"><span data-stu-id="fd62e-491">net" or "database.windows.</span></span><!--no-hyperlink--><span data-ttu-id="fd62e-492">NET ", et la chaîne" password "ou" password "ou" PWD ".</span><span class="sxs-lookup"><span data-stu-id="fd62e-492">net", and the string "Password" or "password" or "pwd".</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-493">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-493">Pattern</span></span>

- <span data-ttu-id="fd62e-494">Chaîne «serveur», «serveur» ou «source de données»</span><span class="sxs-lookup"><span data-stu-id="fd62e-494">The string "Server", "server", or "data source"</span></span>
- <span data-ttu-id="fd62e-495">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="fd62e-495">0-2 whitespace characters</span></span>
- <span data-ttu-id="fd62e-496">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="fd62e-496">An equal sign (=)</span></span>
- <span data-ttu-id="fd62e-497">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="fd62e-497">0-2 whitespace characters</span></span>
- <span data-ttu-id="fd62e-498">N’importe quelle combinaison entre 1-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="fd62e-498">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="fd62e-499">La chaîne «cloudapp. Azure.</span><span class="sxs-lookup"><span data-stu-id="fd62e-499">The string "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="fd62e-500">com "," cloudapp. Azure.</span><span class="sxs-lookup"><span data-stu-id="fd62e-500">com", "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="fd62e-501">NET "ou" Database. Windows.</span><span class="sxs-lookup"><span data-stu-id="fd62e-501">net", or "database.windows.</span></span><!--no-hyperlink--><span data-ttu-id="fd62e-502">NET</span><span class="sxs-lookup"><span data-stu-id="fd62e-502">net"</span></span>
- <span data-ttu-id="fd62e-503">N’importe quelle combinaison entre 1-300 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="fd62e-503">Any combination of between 1-300 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="fd62e-504">La chaîne "password", "password" ou "PWD"</span><span class="sxs-lookup"><span data-stu-id="fd62e-504">The string "Password", "password", or "pwd"</span></span>
- <span data-ttu-id="fd62e-505">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="fd62e-505">0-2 whitespace characters</span></span>
- <span data-ttu-id="fd62e-506">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="fd62e-506">An equal sign (=)</span></span>
- <span data-ttu-id="fd62e-507">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="fd62e-507">0-2 whitespace characters</span></span>
- <span data-ttu-id="fd62e-508">Un ou plusieurs caractères qui ne sont pas des points-virgules (;), guillemets (") ou apostrophe (')</span><span class="sxs-lookup"><span data-stu-id="fd62e-508">One or more characters that is not a semicolon (;), quotation mark ("), or apostrophe (')</span></span>
- <span data-ttu-id="fd62e-509">Un point-virgule (;), guillemet (") ou apostrophe (')</span><span class="sxs-lookup"><span data-stu-id="fd62e-509">A semicolon (;), quotation mark ("), or apostrophe (')</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-510">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-510">Checksum</span></span>

<span data-ttu-id="fd62e-511">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-511">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-512">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-512">Definition</span></span>

<span data-ttu-id="fd62e-513">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-513">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-514">L’expression régulière CEP_Regex_AzureConnectionString trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-514">The regular expression CEP_Regex_AzureConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-515">L’expression régulière CEP_CommonExampleKeywords ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-515">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-516">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-516">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="fd62e-517">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="fd62e-517">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="fd62e-518">(Notez que techniquement, ce type d’informations sensibles identifie ces mots clés à l’aide d’une expression régulière, et non d’une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="fd62e-518">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="fd62e-519">contoso</span><span class="sxs-lookup"><span data-stu-id="fd62e-519">contoso</span></span>
- <span data-ttu-id="fd62e-520">société</span><span class="sxs-lookup"><span data-stu-id="fd62e-520">fabrikam</span></span>
- <span data-ttu-id="fd62e-521">Northwind</span><span class="sxs-lookup"><span data-stu-id="fd62e-521">northwind</span></span>
- <span data-ttu-id="fd62e-522">immédiatement</span><span class="sxs-lookup"><span data-stu-id="fd62e-522">sandbox</span></span>
- <span data-ttu-id="fd62e-523">onebox</span><span class="sxs-lookup"><span data-stu-id="fd62e-523">onebox</span></span>
- <span data-ttu-id="fd62e-524">hôte</span><span class="sxs-lookup"><span data-stu-id="fd62e-524">localhost</span></span>
- <span data-ttu-id="fd62e-525">bouclage</span><span class="sxs-lookup"><span data-stu-id="fd62e-525">127.0.0.1</span></span>
- <span data-ttu-id="fd62e-526">testacs.</span><span class="sxs-lookup"><span data-stu-id="fd62e-526">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="fd62e-527">com</span><span class="sxs-lookup"><span data-stu-id="fd62e-527">com</span></span>
- <span data-ttu-id="fd62e-528">s-int.</span><span class="sxs-lookup"><span data-stu-id="fd62e-528">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="fd62e-529">NET</span><span class="sxs-lookup"><span data-stu-id="fd62e-529">net</span></span>

## <a name="azure-iot-connection-string"></a><span data-ttu-id="fd62e-530">Chaîne de connexion Azure IoT</span><span class="sxs-lookup"><span data-stu-id="fd62e-530">Azure IoT Connection String</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-531">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-531">Format</span></span>

<span data-ttu-id="fd62e-532">La chaîne «nomhôte» suivie des caractères et des chaînes décrits dans le modèle ci-dessous, y compris les chaînes «Azure-appareils.</span><span class="sxs-lookup"><span data-stu-id="fd62e-532">The string "HostName" followed by the characters and strings outlined in the pattern below, including the strings "azure-devices.</span></span><!--no-hyperlink--><span data-ttu-id="fd62e-533">NET "et" SharedAccessKey ".</span><span class="sxs-lookup"><span data-stu-id="fd62e-533">net" and "SharedAccessKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-534">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-534">Pattern</span></span>

- <span data-ttu-id="fd62e-535">La chaîne «nomhôte»</span><span class="sxs-lookup"><span data-stu-id="fd62e-535">The string "HostName"</span></span>
- <span data-ttu-id="fd62e-536">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="fd62e-536">0-2 whitespace characters</span></span>
- <span data-ttu-id="fd62e-537">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="fd62e-537">An equal sign (=)</span></span>
- <span data-ttu-id="fd62e-538">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="fd62e-538">0-2 whitespace characters</span></span>
- <span data-ttu-id="fd62e-539">N’importe quelle combinaison entre 1-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="fd62e-539">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="fd62e-540">La chaîne «Azure-appareils.</span><span class="sxs-lookup"><span data-stu-id="fd62e-540">The string "azure-devices.</span></span><!--no-hyperlink--><span data-ttu-id="fd62e-541">NET</span><span class="sxs-lookup"><span data-stu-id="fd62e-541">net"</span></span>
- <span data-ttu-id="fd62e-542">N’importe quelle combinaison entre 1-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="fd62e-542">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="fd62e-543">La chaîne «SharedAccessKey»</span><span class="sxs-lookup"><span data-stu-id="fd62e-543">The string "SharedAccessKey"</span></span>
- <span data-ttu-id="fd62e-544">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="fd62e-544">0-2 whitespace characters</span></span>
- <span data-ttu-id="fd62e-545">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="fd62e-545">An equal sign (=)</span></span>
- <span data-ttu-id="fd62e-546">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="fd62e-546">0-2 whitespace characters</span></span>
- <span data-ttu-id="fd62e-547">Toute combinaison de 43 lettres majuscules ou minuscules, des chiffres, une barre oblique (/) ou un signe plus (+)</span><span class="sxs-lookup"><span data-stu-id="fd62e-547">Any combination of 43 lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="fd62e-548">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="fd62e-548">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-549">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-549">Checksum</span></span>

<span data-ttu-id="fd62e-550">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-550">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-551">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-551">Definition</span></span>

<span data-ttu-id="fd62e-552">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-552">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-553">L’expression régulière CEP_Regex_AzureIoTConnectionString trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-553">The regular expression CEP_Regex_AzureIoTConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-554">L’expression régulière CEP_CommonExampleKeywords ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-554">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-555">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-555">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="fd62e-556">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="fd62e-556">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="fd62e-557">(Notez que techniquement, ce type d’informations sensibles identifie ces mots clés à l’aide d’une expression régulière, et non d’une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="fd62e-557">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="fd62e-558">contoso</span><span class="sxs-lookup"><span data-stu-id="fd62e-558">contoso</span></span>
- <span data-ttu-id="fd62e-559">société</span><span class="sxs-lookup"><span data-stu-id="fd62e-559">fabrikam</span></span>
- <span data-ttu-id="fd62e-560">Northwind</span><span class="sxs-lookup"><span data-stu-id="fd62e-560">northwind</span></span>
- <span data-ttu-id="fd62e-561">immédiatement</span><span class="sxs-lookup"><span data-stu-id="fd62e-561">sandbox</span></span>
- <span data-ttu-id="fd62e-562">onebox</span><span class="sxs-lookup"><span data-stu-id="fd62e-562">onebox</span></span>
- <span data-ttu-id="fd62e-563">hôte</span><span class="sxs-lookup"><span data-stu-id="fd62e-563">localhost</span></span>
- <span data-ttu-id="fd62e-564">bouclage</span><span class="sxs-lookup"><span data-stu-id="fd62e-564">127.0.0.1</span></span>
- <span data-ttu-id="fd62e-565">testacs.</span><span class="sxs-lookup"><span data-stu-id="fd62e-565">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="fd62e-566">com</span><span class="sxs-lookup"><span data-stu-id="fd62e-566">com</span></span>
- <span data-ttu-id="fd62e-567">s-int.</span><span class="sxs-lookup"><span data-stu-id="fd62e-567">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="fd62e-568">NET</span><span class="sxs-lookup"><span data-stu-id="fd62e-568">net</span></span>

## <a name="azure-publish-setting-password"></a><span data-ttu-id="fd62e-569">Mot de passe de paramètre de publication Azure</span><span class="sxs-lookup"><span data-stu-id="fd62e-569">Azure Publish Setting Password</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-570">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-570">Format</span></span>

<span data-ttu-id="fd62e-571">La chaîne «userpwd =» suivie d’une chaîne alphanumérique.</span><span class="sxs-lookup"><span data-stu-id="fd62e-571">The string "userpwd=" followed by an alphanumeric string.</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-572">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-572">Pattern</span></span>

- <span data-ttu-id="fd62e-573">La chaîne «userpwd =»</span><span class="sxs-lookup"><span data-stu-id="fd62e-573">The string "userpwd="</span></span>
- <span data-ttu-id="fd62e-574">N’importe quelle combinaison de 60 lettres minuscules ou chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-574">Any combination of 60 lowercase letters or digits</span></span>
- <span data-ttu-id="fd62e-575">Guillemet (")</span><span class="sxs-lookup"><span data-stu-id="fd62e-575">A quotation mark (")</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-576">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-576">Checksum</span></span>

<span data-ttu-id="fd62e-577">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-577">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-578">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-578">Definition</span></span>

<span data-ttu-id="fd62e-579">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-579">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-580">L’expression régulière CEP_Regex_AzurePublishSettingPasswords trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-580">The regular expression CEP_Regex_AzurePublishSettingPasswords finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-581">L’expression régulière CEP_CommonExampleKeywords ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-581">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>


```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-582">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-582">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="fd62e-583">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="fd62e-583">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="fd62e-584">(Notez que techniquement, ce type d’informations sensibles identifie ces mots clés à l’aide d’une expression régulière, et non d’une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="fd62e-584">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="fd62e-585">contoso</span><span class="sxs-lookup"><span data-stu-id="fd62e-585">contoso</span></span>
- <span data-ttu-id="fd62e-586">société</span><span class="sxs-lookup"><span data-stu-id="fd62e-586">fabrikam</span></span>
- <span data-ttu-id="fd62e-587">Northwind</span><span class="sxs-lookup"><span data-stu-id="fd62e-587">northwind</span></span>
- <span data-ttu-id="fd62e-588">immédiatement</span><span class="sxs-lookup"><span data-stu-id="fd62e-588">sandbox</span></span>
- <span data-ttu-id="fd62e-589">onebox</span><span class="sxs-lookup"><span data-stu-id="fd62e-589">onebox</span></span>
- <span data-ttu-id="fd62e-590">hôte</span><span class="sxs-lookup"><span data-stu-id="fd62e-590">localhost</span></span>
- <span data-ttu-id="fd62e-591">bouclage</span><span class="sxs-lookup"><span data-stu-id="fd62e-591">127.0.0.1</span></span>
- <span data-ttu-id="fd62e-592">testacs.</span><span class="sxs-lookup"><span data-stu-id="fd62e-592">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="fd62e-593">com</span><span class="sxs-lookup"><span data-stu-id="fd62e-593">com</span></span>
- <span data-ttu-id="fd62e-594">s-int.</span><span class="sxs-lookup"><span data-stu-id="fd62e-594">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="fd62e-595">NET</span><span class="sxs-lookup"><span data-stu-id="fd62e-595">net</span></span>

## <a name="azure-redis-cache-connection-string"></a><span data-ttu-id="fd62e-596">Chaîne de connexion au cache des inversions Azure</span><span class="sxs-lookup"><span data-stu-id="fd62e-596">Azure Redis Cache Connection String</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-597">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-597">Format</span></span>

<span data-ttu-id="fd62e-598">La chaîne «ReDim. cache. Windows.</span><span class="sxs-lookup"><span data-stu-id="fd62e-598">The string "redis.cache.windows.</span></span><!--no-hyperlink--><span data-ttu-id="fd62e-599">NET "suivi des caractères et des chaînes décrits dans le modèle ci-dessous, y compris la chaîne" password "ou" PWD ".</span><span class="sxs-lookup"><span data-stu-id="fd62e-599">net" followed by the characters and strings outlined in the pattern below, including the string "password" or "pwd".</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-600">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-600">Pattern</span></span>

- <span data-ttu-id="fd62e-601">La chaîne «ReDim. cache. Windows.</span><span class="sxs-lookup"><span data-stu-id="fd62e-601">The string "redis.cache.windows.</span></span><!--no-hyperlink--><span data-ttu-id="fd62e-602">NET</span><span class="sxs-lookup"><span data-stu-id="fd62e-602">net"</span></span>
- <span data-ttu-id="fd62e-603">N’importe quelle combinaison entre 1-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="fd62e-603">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="fd62e-604">La chaîne «password» ou «pwd»</span><span class="sxs-lookup"><span data-stu-id="fd62e-604">The string "password" or "pwd"</span></span>
- <span data-ttu-id="fd62e-605">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="fd62e-605">0-2 whitespace characters</span></span>
- <span data-ttu-id="fd62e-606">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="fd62e-606">An equal sign (=)</span></span>
- <span data-ttu-id="fd62e-607">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="fd62e-607">0-2 whitespace characters</span></span>
- <span data-ttu-id="fd62e-608">Toute combinaison de 43 caractères majuscules ou minuscules, des chiffres, une barre oblique (/) ou un signe plus (+)</span><span class="sxs-lookup"><span data-stu-id="fd62e-608">Any combination of 43 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="fd62e-609">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="fd62e-609">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-610">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-610">Checksum</span></span>

<span data-ttu-id="fd62e-611">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-611">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-612">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-612">Definition</span></span>

<span data-ttu-id="fd62e-613">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-613">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-614">L’expression régulière CEP_Regex_AzureRedisCacheConnectionString trouve le contenu qui correspond au modèle..</span><span class="sxs-lookup"><span data-stu-id="fd62e-614">The regular expression CEP_Regex_AzureRedisCacheConnectionString finds content that matches the pattern..</span></span>
- <span data-ttu-id="fd62e-615">L’expression régulière CEP_CommonExampleKeywords ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-615">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-616">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-616">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="fd62e-617">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="fd62e-617">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="fd62e-618">(Notez que techniquement, ce type d’informations sensibles identifie ces mots clés à l’aide d’une expression régulière, et non d’une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="fd62e-618">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="fd62e-619">contoso</span><span class="sxs-lookup"><span data-stu-id="fd62e-619">contoso</span></span>
- <span data-ttu-id="fd62e-620">société</span><span class="sxs-lookup"><span data-stu-id="fd62e-620">fabrikam</span></span>
- <span data-ttu-id="fd62e-621">Northwind</span><span class="sxs-lookup"><span data-stu-id="fd62e-621">northwind</span></span>
- <span data-ttu-id="fd62e-622">immédiatement</span><span class="sxs-lookup"><span data-stu-id="fd62e-622">sandbox</span></span>
- <span data-ttu-id="fd62e-623">onebox</span><span class="sxs-lookup"><span data-stu-id="fd62e-623">onebox</span></span>
- <span data-ttu-id="fd62e-624">hôte</span><span class="sxs-lookup"><span data-stu-id="fd62e-624">localhost</span></span>
- <span data-ttu-id="fd62e-625">bouclage</span><span class="sxs-lookup"><span data-stu-id="fd62e-625">127.0.0.1</span></span>
- <span data-ttu-id="fd62e-626">testacs.</span><span class="sxs-lookup"><span data-stu-id="fd62e-626">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="fd62e-627">com</span><span class="sxs-lookup"><span data-stu-id="fd62e-627">com</span></span>
- <span data-ttu-id="fd62e-628">s-int.</span><span class="sxs-lookup"><span data-stu-id="fd62e-628">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="fd62e-629">NET</span><span class="sxs-lookup"><span data-stu-id="fd62e-629">net</span></span>

## <a name="azure-sas"></a><span data-ttu-id="fd62e-630">SAS Azure</span><span class="sxs-lookup"><span data-stu-id="fd62e-630">Azure SAS</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-631">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-631">Format</span></span>

<span data-ttu-id="fd62e-632">La chaîne «SIG» suivie des caractères et des chaînes présentés dans le modèle ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="fd62e-632">The string "sig" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-633">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-633">Pattern</span></span>

- <span data-ttu-id="fd62e-634">La chaîne «SIG»</span><span class="sxs-lookup"><span data-stu-id="fd62e-634">The string "sig"</span></span>
- <span data-ttu-id="fd62e-635">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="fd62e-635">0-2 whitespace characters</span></span>
- <span data-ttu-id="fd62e-636">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="fd62e-636">An equal sign (=)</span></span>
- <span data-ttu-id="fd62e-637">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="fd62e-637">0-2 whitespace characters</span></span>
- <span data-ttu-id="fd62e-638">Toute combinaison comprise entre 43-53 caractères majuscules ou minuscules, des chiffres ou le signe pourcentage (%)</span><span class="sxs-lookup"><span data-stu-id="fd62e-638">Any combination of between 43-53 characters that are lower- or uppercase letters, digits, or the percent sign (%)</span></span>
- <span data-ttu-id="fd62e-639">La chaîne «% 3D»</span><span class="sxs-lookup"><span data-stu-id="fd62e-639">The string "%3d"</span></span>
- <span data-ttu-id="fd62e-640">Tout caractère qui n’est pas une lettre majuscule, un chiffre ou un signe de pourcentage (%)</span><span class="sxs-lookup"><span data-stu-id="fd62e-640">Any character that is not a lower- or uppercase letter, digit, or percent sign (%)</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-641">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-641">Checksum</span></span>

<span data-ttu-id="fd62e-642">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-642">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-643">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-643">Definition</span></span>

<span data-ttu-id="fd62e-644">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-644">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-645">L’expression régulière CEP_Regex_AzureSAS trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-645">The regular expression CEP_Regex_AzureSAS finds content that matches the pattern.</span></span>

```xml
<!--Azure SAS-->
<Entity id="4d235014-e564-47f4-a6fb-6ebb4a826834" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureSAS" />
  </Pattern>
</Entity>
```

## <a name="azure-service-bus-connection-string"></a><span data-ttu-id="fd62e-646">Chaîne de connexion au bus des services Azure</span><span class="sxs-lookup"><span data-stu-id="fd62e-646">Azure Service Bus Connection String</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-647">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-647">Format</span></span>

<span data-ttu-id="fd62e-648">La chaîne «point de terminaison» suivie des caractères et des chaînes décrits dans le modèle ci-dessous, y compris les chaînes «ServiceBus. Windows.</span><span class="sxs-lookup"><span data-stu-id="fd62e-648">The string "EndPoint" followed by the characters and strings outlined in the pattern below, including the strings "servicebus.windows.</span></span><!--no-hyperlink--><span data-ttu-id="fd62e-649">NET "et" SharedAccesKey ".</span><span class="sxs-lookup"><span data-stu-id="fd62e-649">net" and "SharedAccesKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-650">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-650">Pattern</span></span>

- <span data-ttu-id="fd62e-651">Chaîne «point de terminaison»</span><span class="sxs-lookup"><span data-stu-id="fd62e-651">The string "EndPoint"</span></span>
- <span data-ttu-id="fd62e-652">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="fd62e-652">0-2 whitespace characters</span></span>
- <span data-ttu-id="fd62e-653">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="fd62e-653">An equal sign (=)</span></span>
- <span data-ttu-id="fd62e-654">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="fd62e-654">0-2 whitespace characters</span></span>
- <span data-ttu-id="fd62e-655">N’importe quelle combinaison entre 1-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="fd62e-655">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="fd62e-656">La chaîne «ServiceBus. Windows.</span><span class="sxs-lookup"><span data-stu-id="fd62e-656">The string "servicebus.windows.</span></span><!--no-hyperlink--><span data-ttu-id="fd62e-657">NET</span><span class="sxs-lookup"><span data-stu-id="fd62e-657">net"</span></span>
- <span data-ttu-id="fd62e-658">N’importe quelle combinaison entre 1-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="fd62e-658">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="fd62e-659">La chaîne «SharedAccessKey»</span><span class="sxs-lookup"><span data-stu-id="fd62e-659">The string "SharedAccessKey"</span></span>
- <span data-ttu-id="fd62e-660">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="fd62e-660">0-2 whitespace characters</span></span>
- <span data-ttu-id="fd62e-661">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="fd62e-661">An equal sign (=)</span></span>
- <span data-ttu-id="fd62e-662">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="fd62e-662">0-2 whitespace characters</span></span>
- <span data-ttu-id="fd62e-663">Toute combinaison de 43 caractères majuscules ou minuscules, des chiffres, une barre oblique (/) ou un signe plus (+)</span><span class="sxs-lookup"><span data-stu-id="fd62e-663">Any combination of 43 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="fd62e-664">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="fd62e-664">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-665">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-665">Checksum</span></span>

<span data-ttu-id="fd62e-666">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-666">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-667">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-667">Definition</span></span>

<span data-ttu-id="fd62e-668">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-668">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-669">L’expression régulière CEP_Regex_AzureServiceBusConnectionString trouve le contenu qui correspond au modèle..</span><span class="sxs-lookup"><span data-stu-id="fd62e-669">The regular expression CEP_Regex_AzureServiceBusConnectionString finds content that matches the pattern..</span></span>
- <span data-ttu-id="fd62e-670">L’expression régulière CEP_CommonExampleKeywords ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-670">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-671">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-671">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="fd62e-672">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="fd62e-672">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="fd62e-673">(Notez que techniquement, ce type d’informations sensibles identifie ces mots clés à l’aide d’une expression régulière, et non d’une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="fd62e-673">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="fd62e-674">contoso</span><span class="sxs-lookup"><span data-stu-id="fd62e-674">contoso</span></span>
- <span data-ttu-id="fd62e-675">société</span><span class="sxs-lookup"><span data-stu-id="fd62e-675">fabrikam</span></span>
- <span data-ttu-id="fd62e-676">Northwind</span><span class="sxs-lookup"><span data-stu-id="fd62e-676">northwind</span></span>
- <span data-ttu-id="fd62e-677">immédiatement</span><span class="sxs-lookup"><span data-stu-id="fd62e-677">sandbox</span></span>
- <span data-ttu-id="fd62e-678">onebox</span><span class="sxs-lookup"><span data-stu-id="fd62e-678">onebox</span></span>
- <span data-ttu-id="fd62e-679">hôte</span><span class="sxs-lookup"><span data-stu-id="fd62e-679">localhost</span></span>
- <span data-ttu-id="fd62e-680">bouclage</span><span class="sxs-lookup"><span data-stu-id="fd62e-680">127.0.0.1</span></span>
- <span data-ttu-id="fd62e-681">testacs.</span><span class="sxs-lookup"><span data-stu-id="fd62e-681">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="fd62e-682">com</span><span class="sxs-lookup"><span data-stu-id="fd62e-682">com</span></span>
- <span data-ttu-id="fd62e-683">s-int.</span><span class="sxs-lookup"><span data-stu-id="fd62e-683">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="fd62e-684">NET</span><span class="sxs-lookup"><span data-stu-id="fd62e-684">net</span></span>

## <a name="azure-storage-account-key"></a><span data-ttu-id="fd62e-685">Clé de compte de stockage Azure</span><span class="sxs-lookup"><span data-stu-id="fd62e-685">Azure Storage Account Key</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-686">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-686">Format</span></span>

<span data-ttu-id="fd62e-687">La chaîne «DefaultEndpointsProtocol» suivie des caractères et des chaînes décrits dans le modèle ci-dessous, y compris la chaîne «AccountKey».</span><span class="sxs-lookup"><span data-stu-id="fd62e-687">The string "DefaultEndpointsProtocol" followed by the characters and strings outlined in the pattern below, including the string "AccountKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-688">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-688">Pattern</span></span>

- <span data-ttu-id="fd62e-689">La chaîne «DefaultEndpointsProtocol»</span><span class="sxs-lookup"><span data-stu-id="fd62e-689">The string "DefaultEndpointsProtocol"</span></span>
- <span data-ttu-id="fd62e-690">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="fd62e-690">0-2 whitespace characters</span></span>
- <span data-ttu-id="fd62e-691">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="fd62e-691">An equal sign (=)</span></span>
- <span data-ttu-id="fd62e-692">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="fd62e-692">0-2 whitespace characters</span></span>
- <span data-ttu-id="fd62e-693">N’importe quelle combinaison entre 1-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="fd62e-693">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="fd62e-694">La chaîne «AccountKey»</span><span class="sxs-lookup"><span data-stu-id="fd62e-694">The string "AccountKey"</span></span>
- <span data-ttu-id="fd62e-695">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="fd62e-695">0-2 whitespace characters</span></span>
- <span data-ttu-id="fd62e-696">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="fd62e-696">An equal sign (=)</span></span>
- <span data-ttu-id="fd62e-697">0-2 espaces blancs</span><span class="sxs-lookup"><span data-stu-id="fd62e-697">0-2 whitespace characters</span></span>
- <span data-ttu-id="fd62e-698">Toute combinaison de 86 caractères majuscules ou minuscules, des chiffres, une barre oblique (/) ou un signe plus (+)</span><span class="sxs-lookup"><span data-stu-id="fd62e-698">Any combination of 86 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="fd62e-699">Deux signes égal (=)</span><span class="sxs-lookup"><span data-stu-id="fd62e-699">Two equal signs (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-700">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-700">Checksum</span></span>

<span data-ttu-id="fd62e-701">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-701">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-702">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-702">Definition</span></span>

<span data-ttu-id="fd62e-703">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-703">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-704">L’expression régulière CEP_Regex_AzureStorageAccountKey trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-704">The regular expression CEP_Regex_AzureStorageAccountKey finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-705">L’expression régulière CEP_AzureEmulatorStorageAccountFilter ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-705">The regular expression CEP_AzureEmulatorStorageAccountFilter does **not** find content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-706">L’expression régulière CEP_CommonExampleKeywords ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-706">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-707">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-707">Keywords</span></span>

#### <a name="cep_azureemulatorstorageaccountfilter"></a><span data-ttu-id="fd62e-708">CEP_AzureEmulatorStorageAccountFilter</span><span class="sxs-lookup"><span data-stu-id="fd62e-708">CEP_AzureEmulatorStorageAccountFilter</span></span>

<span data-ttu-id="fd62e-709">(Notez que techniquement, ce type d’informations sensibles identifie ces mots clés à l’aide d’une expression régulière, et non d’une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="fd62e-709">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="fd62e-710">Eby8vdM02xNOcqFlqUwJPLlmEtlCDXJ1OUzFT50uSRZ6IFsuFq2UVErCz4I6tq/K1SZFPTOtr/KBHBeksoGMGw = =</span><span class="sxs-lookup"><span data-stu-id="fd62e-710">Eby8vdM02xNOcqFlqUwJPLlmEtlCDXJ1OUzFT50uSRZ6IFsuFq2UVErCz4I6tq/K1SZFPTOtr/KBHBeksoGMGw==</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="fd62e-711">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="fd62e-711">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="fd62e-712">(Notez que techniquement, ce type d’informations sensibles identifie ces mots clés à l’aide d’une expression régulière, et non d’une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="fd62e-712">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="fd62e-713">contoso</span><span class="sxs-lookup"><span data-stu-id="fd62e-713">contoso</span></span>
- <span data-ttu-id="fd62e-714">société</span><span class="sxs-lookup"><span data-stu-id="fd62e-714">fabrikam</span></span>
- <span data-ttu-id="fd62e-715">Northwind</span><span class="sxs-lookup"><span data-stu-id="fd62e-715">northwind</span></span>
- <span data-ttu-id="fd62e-716">immédiatement</span><span class="sxs-lookup"><span data-stu-id="fd62e-716">sandbox</span></span>
- <span data-ttu-id="fd62e-717">onebox</span><span class="sxs-lookup"><span data-stu-id="fd62e-717">onebox</span></span>
- <span data-ttu-id="fd62e-718">hôte</span><span class="sxs-lookup"><span data-stu-id="fd62e-718">localhost</span></span>
- <span data-ttu-id="fd62e-719">bouclage</span><span class="sxs-lookup"><span data-stu-id="fd62e-719">127.0.0.1</span></span>
- <span data-ttu-id="fd62e-720">testacs.</span><span class="sxs-lookup"><span data-stu-id="fd62e-720">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="fd62e-721">com</span><span class="sxs-lookup"><span data-stu-id="fd62e-721">com</span></span>
- <span data-ttu-id="fd62e-722">s-int.</span><span class="sxs-lookup"><span data-stu-id="fd62e-722">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="fd62e-723">NET</span><span class="sxs-lookup"><span data-stu-id="fd62e-723">net</span></span>

## <a name="azure-storage-account-key-generic"></a><span data-ttu-id="fd62e-724">Clé de compte de stockage Azure (Générique)</span><span class="sxs-lookup"><span data-stu-id="fd62e-724">Azure Storage Account Key (Generic)</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-725">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-725">Format</span></span>

<span data-ttu-id="fd62e-726">Toute combinaison de 86 lettres majuscules ou minuscules, des chiffres, la barre oblique (/) ou le signe plus (+), précédée ou suivie des caractères décrits dans le modèle ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="fd62e-726">Any combination of 86 lower- or uppercase letters, digits, the forward slash (/), or plus sign (+), preceded or followed by the characters outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-727">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-727">Pattern</span></span>

- <span data-ttu-id="fd62e-728">0-1 du symbole supérieur à (>), apostrophe ('), signe égal (=), guillemet (") ou dièse (#)</span><span class="sxs-lookup"><span data-stu-id="fd62e-728">0-1 of the greater than symbol (>), apostrophe ('), equal sign (=), quotation mark ("), or number sign (#)</span></span>
- <span data-ttu-id="fd62e-729">Toute combinaison de 86 caractères majuscules ou minuscules, des chiffres, la barre oblique (/) ou le signe plus (+)</span><span class="sxs-lookup"><span data-stu-id="fd62e-729">Any combination of 86 characters that are lower- or uppercase letters, digits, the forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="fd62e-730">Deux signes égal (=)</span><span class="sxs-lookup"><span data-stu-id="fd62e-730">Two equal signs (=)</span></span>


### <a name="checksum"></a><span data-ttu-id="fd62e-731">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-731">Checksum</span></span>

<span data-ttu-id="fd62e-732">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-732">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-733">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-733">Definition</span></span>

<span data-ttu-id="fd62e-734">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-734">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-735">L’expression régulière CEP_Regex_AzureStorageAccountKeyGeneric trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-735">The regular expression CEP_Regex_AzureStorageAccountKeyGeneric finds content that matches the pattern.</span></span>

```xml
<!--Azure Storage Account Key (Generic)-->
<Entity id="7ff41bd0-5419-4523-91d6-383b3a37f084" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureStorageAccountKeyGeneric" />
  </Pattern>
</Entity>
```

## <a name="belgium-national-number"></a><span data-ttu-id="fd62e-736">Numéro national Belgique</span><span class="sxs-lookup"><span data-stu-id="fd62e-736">Belgium National Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-737">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-737">Format</span></span>

<span data-ttu-id="fd62e-738">11 chiffres plus des délimiteurs</span><span class="sxs-lookup"><span data-stu-id="fd62e-738">11 digits plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-739">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-739">Pattern</span></span>

<span data-ttu-id="fd62e-740">11 chiffres plus des délimiteurs :</span><span class="sxs-lookup"><span data-stu-id="fd62e-740">11 digits plus delimiters:</span></span>
- <span data-ttu-id="fd62e-741">Six chiffres et deux points au format AA.MM.JJ pour la date de naissance </span><span class="sxs-lookup"><span data-stu-id="fd62e-741">Six digits and two periods in the format YY.MM.DD for date of birth</span></span> 
- <span data-ttu-id="fd62e-742">Un trait d’union</span><span class="sxs-lookup"><span data-stu-id="fd62e-742">A hyphen</span></span> 
- <span data-ttu-id="fd62e-743">Trois chiffres séquentiels (impairs pour les hommes, pairs pour les femmes) </span><span class="sxs-lookup"><span data-stu-id="fd62e-743">Three sequential digits (odd for males, even for females)</span></span> 
- <span data-ttu-id="fd62e-744">Un point</span><span class="sxs-lookup"><span data-stu-id="fd62e-744">A period</span></span> 
- <span data-ttu-id="fd62e-745">Deux chiffres de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-745">Two digits that are a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-746">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-746">Checksum</span></span>

<span data-ttu-id="fd62e-747">Oui</span><span class="sxs-lookup"><span data-stu-id="fd62e-747">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-748">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-748">Definition</span></span>

<span data-ttu-id="fd62e-749">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-749">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-750">La fonction Func_belgium_national_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-750">The function Func_belgium_national_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-751">Un mot clé figurant dans la liste Keyword_belgium_national_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-751">A keyword from Keyword_belgium_national_number is found.</span></span>
- <span data-ttu-id="fd62e-752">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-752">The checksum passes.</span></span>

```xml
<!-- Belgium National Number -->
  <Entity id="fb969c9e-0fd1-4b18-8091-a2123c5e6a54" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_belgium_national_number"/>
     <Match idRef="Keyword_belgium_national_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fd62e-753">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-753">Keywords</span></span>

#### <a name="keyword_belgium_national_number"></a><span data-ttu-id="fd62e-754">Keyword_belgium_national_number</span><span class="sxs-lookup"><span data-stu-id="fd62e-754">Keyword_belgium_national_number</span></span>

- <span data-ttu-id="fd62e-755">Identité</span><span class="sxs-lookup"><span data-stu-id="fd62e-755">Identity</span></span>
- <span data-ttu-id="fd62e-756">Son</span><span class="sxs-lookup"><span data-stu-id="fd62e-756">Registration</span></span>
- <span data-ttu-id="fd62e-757">Identificateur</span><span class="sxs-lookup"><span data-stu-id="fd62e-757">Identification</span></span> 
- <span data-ttu-id="fd62e-758">ID</span><span class="sxs-lookup"><span data-stu-id="fd62e-758">ID</span></span> 
- <span data-ttu-id="fd62e-759">Identiteitskaart</span><span class="sxs-lookup"><span data-stu-id="fd62e-759">Identiteitskaart</span></span>
- <span data-ttu-id="fd62e-760">Registratie nummer</span><span class="sxs-lookup"><span data-stu-id="fd62e-760">Registratie nummer</span></span> 
- <span data-ttu-id="fd62e-761">Identificatie nummer</span><span class="sxs-lookup"><span data-stu-id="fd62e-761">Identificatie nummer</span></span> 
- <span data-ttu-id="fd62e-762">Identiteit</span><span class="sxs-lookup"><span data-stu-id="fd62e-762">Identiteit</span></span>
- <span data-ttu-id="fd62e-763">Registratie</span><span class="sxs-lookup"><span data-stu-id="fd62e-763">Registratie</span></span>
- <span data-ttu-id="fd62e-764">Identificatie</span><span class="sxs-lookup"><span data-stu-id="fd62e-764">Identificatie</span></span> 
- <span data-ttu-id="fd62e-765">Carte d’identité</span><span class="sxs-lookup"><span data-stu-id="fd62e-765">Carte d’identité</span></span> 
- <span data-ttu-id="fd62e-766">numéro d’immatriculation</span><span class="sxs-lookup"><span data-stu-id="fd62e-766">numéro d'immatriculation</span></span>
- <span data-ttu-id="fd62e-767">numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="fd62e-767">numéro d'identification</span></span>
- <span data-ttu-id="fd62e-768">identité</span><span class="sxs-lookup"><span data-stu-id="fd62e-768">identité</span></span> 
- <span data-ttu-id="fd62e-769">inscriptions</span><span class="sxs-lookup"><span data-stu-id="fd62e-769">inscription</span></span> 
- <span data-ttu-id="fd62e-770">Identifikation</span><span class="sxs-lookup"><span data-stu-id="fd62e-770">Identifikation</span></span>
- <span data-ttu-id="fd62e-771">Identifizierung</span><span class="sxs-lookup"><span data-stu-id="fd62e-771">Identifizierung</span></span>
- <span data-ttu-id="fd62e-772">Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="fd62e-772">Identifikationsnummer</span></span>
- <span data-ttu-id="fd62e-773">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="fd62e-773">Personalausweis</span></span>
- <span data-ttu-id="fd62e-774">Registrierung</span><span class="sxs-lookup"><span data-stu-id="fd62e-774">Registrierung</span></span>
- <span data-ttu-id="fd62e-775">Registrationsnummer</span><span class="sxs-lookup"><span data-stu-id="fd62e-775">Registrationsnummer</span></span>

   
## <a name="brazil-cpf-number"></a><span data-ttu-id="fd62e-776">Numéro CPF Brésil</span><span class="sxs-lookup"><span data-stu-id="fd62e-776">Brazil CPF Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-777">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-777">Format</span></span>

<span data-ttu-id="fd62e-778">11 chiffres qui incluent un chiffre de contrôle et peuvent ou non être mis en forme </span><span class="sxs-lookup"><span data-stu-id="fd62e-778">11 digits that include a check digit and can be formatted or unformatted</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-779">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-779">Pattern</span></span>

<span data-ttu-id="fd62e-780">Avec</span><span class="sxs-lookup"><span data-stu-id="fd62e-780">Formatted:</span></span>
- <span data-ttu-id="fd62e-781">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-781">Three digits</span></span> 
- <span data-ttu-id="fd62e-782">Un point </span><span class="sxs-lookup"><span data-stu-id="fd62e-782">A period</span></span> 
- <span data-ttu-id="fd62e-783">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-783">Three digits</span></span> 
- <span data-ttu-id="fd62e-784">Un point </span><span class="sxs-lookup"><span data-stu-id="fd62e-784">A period</span></span> 
- <span data-ttu-id="fd62e-785">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-785">Three digits</span></span> 
- <span data-ttu-id="fd62e-786">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="fd62e-786">A hyphen</span></span> 
- <span data-ttu-id="fd62e-787">Deux chiffres de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-787">Two digits which are check digits</span></span>

<span data-ttu-id="fd62e-788">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-788">Unformatted:</span></span>
- <span data-ttu-id="fd62e-789">11 chiffres où les deux derniers sont des chiffres de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-789">11 digits where the last two digits are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-790">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-790">Checksum</span></span>

<span data-ttu-id="fd62e-791">Oui</span><span class="sxs-lookup"><span data-stu-id="fd62e-791">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-792">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-792">Definition</span></span>

<span data-ttu-id="fd62e-793">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-793">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-794">La fonction Func_brazil_cpf trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-794">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-795">Un mot clé figurant dans la liste Keyword_brazil_cpf est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-795">A keyword from Keyword_brazil_cpf is found.</span></span>
- <span data-ttu-id="fd62e-796">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-796">The checksum passes.</span></span>

<span data-ttu-id="fd62e-797">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-797">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-798">La fonction Func_brazil_cpf trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-798">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-799">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-799">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-800">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-800">Keywords</span></span>

#### <a name="keyword_brazil_cpf"></a><span data-ttu-id="fd62e-801">Keyword_brazil_cpf</span><span class="sxs-lookup"><span data-stu-id="fd62e-801">Keyword_brazil_cpf</span></span>

- <span data-ttu-id="fd62e-802">CPF</span><span class="sxs-lookup"><span data-stu-id="fd62e-802">CPF</span></span>
- <span data-ttu-id="fd62e-803">Identificateur</span><span class="sxs-lookup"><span data-stu-id="fd62e-803">Identification</span></span>
- <span data-ttu-id="fd62e-804">Son</span><span class="sxs-lookup"><span data-stu-id="fd62e-804">Registration</span></span>
- <span data-ttu-id="fd62e-805">Parts</span><span class="sxs-lookup"><span data-stu-id="fd62e-805">Revenue</span></span>
- <span data-ttu-id="fd62e-806">Cadastro de Pessoas Físicas</span><span class="sxs-lookup"><span data-stu-id="fd62e-806">Cadastro de Pessoas Físicas</span></span> 
- <span data-ttu-id="fd62e-807">Imposto</span><span class="sxs-lookup"><span data-stu-id="fd62e-807">Imposto</span></span> 
- <span data-ttu-id="fd62e-808">Identificação</span><span class="sxs-lookup"><span data-stu-id="fd62e-808">Identificação</span></span> 
- <span data-ttu-id="fd62e-809">Inscrição</span><span class="sxs-lookup"><span data-stu-id="fd62e-809">Inscrição</span></span> 
- <span data-ttu-id="fd62e-810">Receita</span><span class="sxs-lookup"><span data-stu-id="fd62e-810">Receita</span></span> 
   
## <a name="brazil-legal-entity-number-cnpj"></a><span data-ttu-id="fd62e-811">Numéro d’entité juridique (CNPJ) Brésil</span><span class="sxs-lookup"><span data-stu-id="fd62e-811">Brazil Legal Entity Number (CNPJ)</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-812">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-812">Format</span></span>

<span data-ttu-id="fd62e-813">14 chiffres qui incluent un numéro d’enregistrement, un numéro de succursale et des chiffres de contrôle, avec des délimiteurs en plus</span><span class="sxs-lookup"><span data-stu-id="fd62e-813">14 digits that include a registration number, branch number, and check digits, plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-814">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-814">Pattern</span></span>
<span data-ttu-id="fd62e-815">14 chiffres plus des délimiteurs :</span><span class="sxs-lookup"><span data-stu-id="fd62e-815">14 digits, plus delimiters:</span></span>
- <span data-ttu-id="fd62e-816">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-816">Two digits</span></span> 
- <span data-ttu-id="fd62e-817">Un point </span><span class="sxs-lookup"><span data-stu-id="fd62e-817">A period</span></span> 
- <span data-ttu-id="fd62e-818">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-818">Three digits</span></span> 
- <span data-ttu-id="fd62e-819">Un point </span><span class="sxs-lookup"><span data-stu-id="fd62e-819">A period</span></span> 
- <span data-ttu-id="fd62e-820">Trois chiffres (ces huit premiers chiffres composent le numéro d’enregistrement) </span><span class="sxs-lookup"><span data-stu-id="fd62e-820">Three digits (these first eight digits are the registration number)</span></span> 
- <span data-ttu-id="fd62e-821">Une barre oblique </span><span class="sxs-lookup"><span data-stu-id="fd62e-821">A forward slash</span></span> 
- <span data-ttu-id="fd62e-822">Le numéro de succursale à quatre chiffres </span><span class="sxs-lookup"><span data-stu-id="fd62e-822">Four-digit branch number</span></span> 
- <span data-ttu-id="fd62e-823">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="fd62e-823">A hyphen</span></span> 
- <span data-ttu-id="fd62e-824">Deux chiffres de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-824">Two digits which are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-825">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-825">Checksum</span></span>

<span data-ttu-id="fd62e-826">Oui</span><span class="sxs-lookup"><span data-stu-id="fd62e-826">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-827">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-827">Definition</span></span>

<span data-ttu-id="fd62e-828">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-828">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-829">La fonction Func_brazil_cnpj trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-829">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-830">Un mot clé figurant dans la liste Keyword_brazil_cnpj est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-830">A keyword from Keyword_brazil_cnpj is found.</span></span>
- <span data-ttu-id="fd62e-831">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-831">The checksum passes.</span></span>

<span data-ttu-id="fd62e-832">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-832">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-833">La fonction Func_brazil_cnpj trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-833">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-834">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-834">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-835">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-835">Keywords</span></span>

#### <a name="keyword_brazil_cnpj"></a><span data-ttu-id="fd62e-836">Keyword_brazil_cnpj</span><span class="sxs-lookup"><span data-stu-id="fd62e-836">Keyword_brazil_cnpj</span></span>

- <span data-ttu-id="fd62e-837">CNPJ</span><span class="sxs-lookup"><span data-stu-id="fd62e-837">CNPJ</span></span> 
- <span data-ttu-id="fd62e-838">CNPJ/MF</span><span class="sxs-lookup"><span data-stu-id="fd62e-838">CNPJ/MF</span></span> 
- <span data-ttu-id="fd62e-839">CNPJ-MF</span><span class="sxs-lookup"><span data-stu-id="fd62e-839">CNPJ-MF</span></span> 
- <span data-ttu-id="fd62e-840">National Registry of Legal Entities</span><span class="sxs-lookup"><span data-stu-id="fd62e-840">National Registry of Legal Entities</span></span> 
- <span data-ttu-id="fd62e-841">Taxpayers Registry</span><span class="sxs-lookup"><span data-stu-id="fd62e-841">Taxpayers Registry</span></span> 
- <span data-ttu-id="fd62e-842">Legal entity</span><span class="sxs-lookup"><span data-stu-id="fd62e-842">Legal entity</span></span> 
- <span data-ttu-id="fd62e-843">Legal entities</span><span class="sxs-lookup"><span data-stu-id="fd62e-843">Legal entities</span></span> 
- <span data-ttu-id="fd62e-844">Registration Status</span><span class="sxs-lookup"><span data-stu-id="fd62e-844">Registration Status</span></span> 
- <span data-ttu-id="fd62e-845">Business</span><span class="sxs-lookup"><span data-stu-id="fd62e-845">Business</span></span> 
- <span data-ttu-id="fd62e-846">Company</span><span class="sxs-lookup"><span data-stu-id="fd62e-846">Company</span></span>
- <span data-ttu-id="fd62e-847">CNPJ</span><span class="sxs-lookup"><span data-stu-id="fd62e-847">CNPJ</span></span> 
- <span data-ttu-id="fd62e-848">Cadastro Nacional da Pessoa Jurídica</span><span class="sxs-lookup"><span data-stu-id="fd62e-848">Cadastro Nacional da Pessoa Jurídica</span></span> 
- <span data-ttu-id="fd62e-849">Cadastro Geral de Contribuintes</span><span class="sxs-lookup"><span data-stu-id="fd62e-849">Cadastro Geral de Contribuintes</span></span> 
- <span data-ttu-id="fd62e-850">CGC</span><span class="sxs-lookup"><span data-stu-id="fd62e-850">CGC</span></span> 
- <span data-ttu-id="fd62e-851">Pessoa jurídica</span><span class="sxs-lookup"><span data-stu-id="fd62e-851">Pessoa jurídica</span></span> 
- <span data-ttu-id="fd62e-852">Pessoas jurídicas</span><span class="sxs-lookup"><span data-stu-id="fd62e-852">Pessoas jurídicas</span></span> 
- <span data-ttu-id="fd62e-853">Situação cadastral</span><span class="sxs-lookup"><span data-stu-id="fd62e-853">Situação cadastral</span></span> 
- <span data-ttu-id="fd62e-854">Inscrição</span><span class="sxs-lookup"><span data-stu-id="fd62e-854">Inscrição</span></span> 
- <span data-ttu-id="fd62e-855">Empresa</span><span class="sxs-lookup"><span data-stu-id="fd62e-855">Empresa</span></span> 
   
## <a name="brazil-national-id-card-rg"></a><span data-ttu-id="fd62e-856">	Brazil National ID Card (RG)</span><span class="sxs-lookup"><span data-stu-id="fd62e-856">Brazil National ID Card (RG)</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-857">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-857">Format</span></span>

<span data-ttu-id="fd62e-858">Registro Geral (ancien format): neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-858">Registro Geral (old format): Nine digits</span></span>

<span data-ttu-id="fd62e-859">Registro de identidade (RIC) (nouveau format): 11 chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-859">Registro de Identidade (RIC) (new format): 11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-860">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-860">Pattern</span></span>

<span data-ttu-id="fd62e-861">Registro Geral (ancien format) :</span><span class="sxs-lookup"><span data-stu-id="fd62e-861">Registro Geral (old format):</span></span>
- <span data-ttu-id="fd62e-862">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-862">Two digits</span></span> 
- <span data-ttu-id="fd62e-863">Un point </span><span class="sxs-lookup"><span data-stu-id="fd62e-863">A period</span></span> 
- <span data-ttu-id="fd62e-864">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-864">Three digits</span></span> 
- <span data-ttu-id="fd62e-865">Un point </span><span class="sxs-lookup"><span data-stu-id="fd62e-865">A period</span></span> 
- <span data-ttu-id="fd62e-866">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-866">Three digits</span></span> 
- <span data-ttu-id="fd62e-867">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="fd62e-867">A hyphen</span></span> 
- <span data-ttu-id="fd62e-868">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-868">One digit which is a check digit</span></span>

<span data-ttu-id="fd62e-869">Registro de identidade (RIC) (nouveau format):</span><span class="sxs-lookup"><span data-stu-id="fd62e-869">Registro de Identidade (RIC) (new format):</span></span>
- <span data-ttu-id="fd62e-870">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-870">10 digits</span></span> 
- <span data-ttu-id="fd62e-871">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="fd62e-871">A hyphen</span></span> 
- <span data-ttu-id="fd62e-872">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-872">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-873">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-873">Checksum</span></span>

<span data-ttu-id="fd62e-874">Oui</span><span class="sxs-lookup"><span data-stu-id="fd62e-874">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-875">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-875">Definition</span></span>

<span data-ttu-id="fd62e-876">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-876">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-877">La fonction Func_brazil_rg trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-877">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-878">Un mot clé figurant dans la liste Keyword_brazil_rg est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-878">A keyword from Keyword_brazil_rg is found.</span></span>
- <span data-ttu-id="fd62e-879">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-879">The checksum passes.</span></span>

<span data-ttu-id="fd62e-880">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-880">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-881">La fonction Func_brazil_rg trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-881">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-882">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-882">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-883">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-883">Keywords</span></span>

#### <a name="keyword_brazil_rg"></a><span data-ttu-id="fd62e-884">Keyword_brazil_rg</span><span class="sxs-lookup"><span data-stu-id="fd62e-884">Keyword_brazil_rg</span></span>

<span data-ttu-id="fd62e-885">Cédula de identidade carte d’identité número de rregistro Registro de identidade Registro Geral RG (ce mot clé respecte la casse) RIC (ce mot clé respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="fd62e-885">Cédula de identidade identity card national id número de rregistro registro de Iidentidade registro geral RG (this keyword is case sensitive) RIC (this keyword is case sensitive)</span></span> 
   
## <a name="canada-bank-account-number"></a><span data-ttu-id="fd62e-886">Numéro de compte bancaire Canada</span><span class="sxs-lookup"><span data-stu-id="fd62e-886">Canada Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-887">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-887">Format</span></span>

<span data-ttu-id="fd62e-888">Sept ou douze chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-888">Seven or twelve digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-889">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-889">Pattern</span></span>

<span data-ttu-id="fd62e-890">Un numéro de compte bancaire au Canada est composé de sept ou douze chiffres.</span><span class="sxs-lookup"><span data-stu-id="fd62e-890">A Canada Bank Account Number is seven or twelve digits.</span></span>

<span data-ttu-id="fd62e-891">Un numéro de transit de compte bancaire du Canada est indiqué au format suivant :</span><span class="sxs-lookup"><span data-stu-id="fd62e-891">A Canada bank account transit number is:</span></span>
- <span data-ttu-id="fd62e-892">Cinq chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-892">Five digits</span></span> 
- <span data-ttu-id="fd62e-893">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="fd62e-893">A hyphen</span></span> 
- <span data-ttu-id="fd62e-894">Trois chiffres ou</span><span class="sxs-lookup"><span data-stu-id="fd62e-894">Three digits OR</span></span>
- <span data-ttu-id="fd62e-895">Un zéro « 0 » </span><span class="sxs-lookup"><span data-stu-id="fd62e-895">A zero "0"</span></span> 
- <span data-ttu-id="fd62e-896">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-896">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-897">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-897">Checksum</span></span>

<span data-ttu-id="fd62e-898">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-898">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-899">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-899">Definition</span></span>

<span data-ttu-id="fd62e-900">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-900">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-901">L’expression régulière Regex_canada_bank_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-901">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-902">Un mot clé figurant dans la liste Keyword_canada_bank_account_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-902">A keyword from Keyword_canada_bank_account_number is found.</span></span>
- <span data-ttu-id="fd62e-903">L’expression régulière Regex_canada_bank_account_transit_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-903">The regular expression Regex_canada_bank_account_transit_number finds content that matches the pattern.</span></span>

<span data-ttu-id="fd62e-904">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-904">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-905">L’expression régulière Regex_canada_bank_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-905">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-906">Un mot clé figurant dans la liste Keyword_canada_bank_account_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-906">A keyword from Keyword_canada_bank_account_number is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-907">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-907">Keywords</span></span>

#### <a name="keyword_canada_bank_account_number"></a><span data-ttu-id="fd62e-908">Keyword_canada_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="fd62e-908">Keyword_canada_bank_account_number</span></span>

- <span data-ttu-id="fd62e-909">obligations d’épargne du Canada</span><span class="sxs-lookup"><span data-stu-id="fd62e-909">canada savings bonds</span></span>
- <span data-ttu-id="fd62e-910">agence du revenu du Canada</span><span class="sxs-lookup"><span data-stu-id="fd62e-910">canada revenue agency</span></span>
- <span data-ttu-id="fd62e-911">institution financière du Canada</span><span class="sxs-lookup"><span data-stu-id="fd62e-911">canadian financial institution</span></span>
- <span data-ttu-id="fd62e-912">formulaire de dépôt direct</span><span class="sxs-lookup"><span data-stu-id="fd62e-912">direct deposit form</span></span>
- <span data-ttu-id="fd62e-913">citoyen canadien</span><span class="sxs-lookup"><span data-stu-id="fd62e-913">canadian citizen</span></span>
- <span data-ttu-id="fd62e-914">représentant légal</span><span class="sxs-lookup"><span data-stu-id="fd62e-914">legal representative</span></span>
- <span data-ttu-id="fd62e-915">notaire</span><span class="sxs-lookup"><span data-stu-id="fd62e-915">notary public</span></span>
- <span data-ttu-id="fd62e-916">commissaire à l’assermentation</span><span class="sxs-lookup"><span data-stu-id="fd62e-916">commissioner for oaths</span></span>
- <span data-ttu-id="fd62e-917">prestation pour la garde d’enfants</span><span class="sxs-lookup"><span data-stu-id="fd62e-917">child care benefit</span></span>
- <span data-ttu-id="fd62e-918">prestation universelle pour la garde d’enfants</span><span class="sxs-lookup"><span data-stu-id="fd62e-918">universal child care</span></span>
- <span data-ttu-id="fd62e-919">prestation fiscale canadienne pour enfants</span><span class="sxs-lookup"><span data-stu-id="fd62e-919">canada child tax benefit</span></span>
- <span data-ttu-id="fd62e-920">prestation fiscale pour le revenu gagné</span><span class="sxs-lookup"><span data-stu-id="fd62e-920">income tax benefit</span></span>
- <span data-ttu-id="fd62e-921">taxe de vente harmonisée</span><span class="sxs-lookup"><span data-stu-id="fd62e-921">harmonized sales tax</span></span>
- <span data-ttu-id="fd62e-922">numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="fd62e-922">social insurance number</span></span>
- <span data-ttu-id="fd62e-923">remboursement d’impôt</span><span class="sxs-lookup"><span data-stu-id="fd62e-923">income tax refund</span></span>
- <span data-ttu-id="fd62e-924">prestation fiscale pour enfants</span><span class="sxs-lookup"><span data-stu-id="fd62e-924">child tax benefit</span></span>
- <span data-ttu-id="fd62e-925">paiements aux territoires</span><span class="sxs-lookup"><span data-stu-id="fd62e-925">territorial payments</span></span>
- <span data-ttu-id="fd62e-926">numéro d’institution</span><span class="sxs-lookup"><span data-stu-id="fd62e-926">institution number</span></span>
- <span data-ttu-id="fd62e-927">demande de dépôt</span><span class="sxs-lookup"><span data-stu-id="fd62e-927">deposit request</span></span>
- <span data-ttu-id="fd62e-928">informations bancaires</span><span class="sxs-lookup"><span data-stu-id="fd62e-928">banking information</span></span>
- <span data-ttu-id="fd62e-929">dépôt direct</span><span class="sxs-lookup"><span data-stu-id="fd62e-929">direct deposit</span></span>
   
## <a name="canada-drivers-license-number"></a><span data-ttu-id="fd62e-930">Numéro de permis de conduire Canada</span><span class="sxs-lookup"><span data-stu-id="fd62e-930">Canada Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-931">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-931">Format</span></span>

<span data-ttu-id="fd62e-932">Varie selon la province</span><span class="sxs-lookup"><span data-stu-id="fd62e-932">Varies by province</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-933">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-933">Pattern</span></span>

<span data-ttu-id="fd62e-934">Plusieurs modèles pour les différentes provinces : Alberta, Colombie-Britannique, Manitoba, Nouveau-Brunswick, Terre-Neuve-et-Labrador, Nouvelle-Écosse, Ontario, Île-du-Prince-Édouard, Québec et Saskatchewan</span><span class="sxs-lookup"><span data-stu-id="fd62e-934">Various patterns covering Alberta, British Columbia, Manitoba, New Brunswick, Newfoundland/Labrador, Nova Scotia, Ontario, Prince Edward Island, Quebec, and Saskatchewan</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-935">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-935">Checksum</span></span>

<span data-ttu-id="fd62e-936">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-936">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-937">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-937">Definition</span></span>

<span data-ttu-id="fd62e-938">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-938">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-939">La fonction Func_[province_name]_drivers_license_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-939">The function Func_[province_name]_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-940">Un mot clé figurant dans la liste Keyword_[province_name]_drivers_license_name est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-940">A keyword from Keyword_[province_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="fd62e-941">Un mot clé figurant dans la liste Keyword_canada_drivers_license est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-941">A keyword from Keyword_canada_drivers_license is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-942">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-942">Keywords</span></span>

#### <a name="keyword_province_name_drivers_license_name"></a><span data-ttu-id="fd62e-943">Keyword_[province_name]_drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="fd62e-943">Keyword_[province_name]_drivers_license_name</span></span>

- <span data-ttu-id="fd62e-944">L’abréviation de la province, par exemple AB</span><span class="sxs-lookup"><span data-stu-id="fd62e-944">The province abbreviation, for example AB</span></span>
- <span data-ttu-id="fd62e-945">Le nom de la province, par exemple Alberta</span><span class="sxs-lookup"><span data-stu-id="fd62e-945">The province name, for example Alberta</span></span>

#### <a name="keyword_canada_drivers_license"></a><span data-ttu-id="fd62e-946">Keyword_canada_drivers_license</span><span class="sxs-lookup"><span data-stu-id="fd62e-946">Keyword_canada_drivers_license</span></span>

- <span data-ttu-id="fd62e-947">LD</span><span class="sxs-lookup"><span data-stu-id="fd62e-947">DL</span></span>
- <span data-ttu-id="fd62e-948">DISTRIBUTION</span><span class="sxs-lookup"><span data-stu-id="fd62e-948">DLS</span></span>
- <span data-ttu-id="fd62e-949">CÈDE</span><span class="sxs-lookup"><span data-stu-id="fd62e-949">CDL</span></span>
- <span data-ttu-id="fd62e-950">CDLS</span><span class="sxs-lookup"><span data-stu-id="fd62e-950">CDLS</span></span>
- <span data-ttu-id="fd62e-951">DriverLic</span><span class="sxs-lookup"><span data-stu-id="fd62e-951">DriverLic</span></span>
- <span data-ttu-id="fd62e-952">DriverLics</span><span class="sxs-lookup"><span data-stu-id="fd62e-952">DriverLics</span></span>
- <span data-ttu-id="fd62e-953">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="fd62e-953">DriverLicense</span></span>
- <span data-ttu-id="fd62e-954">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="fd62e-954">DriverLicenses</span></span>
- <span data-ttu-id="fd62e-955">DriverLicence</span><span class="sxs-lookup"><span data-stu-id="fd62e-955">DriverLicence</span></span>
- <span data-ttu-id="fd62e-956">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="fd62e-956">DriverLicences</span></span>
- <span data-ttu-id="fd62e-957">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-957">Driver Lic</span></span>
- <span data-ttu-id="fd62e-958">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-958">Driver Lics</span></span>
- <span data-ttu-id="fd62e-959">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-959">Driver License</span></span>
- <span data-ttu-id="fd62e-960">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-960">Driver Licenses</span></span>
- <span data-ttu-id="fd62e-961">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-961">Driver Licence</span></span>
- <span data-ttu-id="fd62e-962">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-962">Driver Licences</span></span>
- <span data-ttu-id="fd62e-963">DriversLic</span><span class="sxs-lookup"><span data-stu-id="fd62e-963">DriversLic</span></span>
- <span data-ttu-id="fd62e-964">DriversLics</span><span class="sxs-lookup"><span data-stu-id="fd62e-964">DriversLics</span></span>
- <span data-ttu-id="fd62e-965">DriversLicence</span><span class="sxs-lookup"><span data-stu-id="fd62e-965">DriversLicence</span></span>
- <span data-ttu-id="fd62e-966">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="fd62e-966">DriversLicences</span></span>
- <span data-ttu-id="fd62e-967">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="fd62e-967">DriversLicense</span></span>
- <span data-ttu-id="fd62e-968">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="fd62e-968">DriversLicenses</span></span>
- <span data-ttu-id="fd62e-969">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-969">Drivers Lic</span></span>
- <span data-ttu-id="fd62e-970">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-970">Drivers Lics</span></span>
- <span data-ttu-id="fd62e-971">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-971">Drivers License</span></span>
- <span data-ttu-id="fd62e-972">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-972">Drivers Licenses</span></span>
- <span data-ttu-id="fd62e-973">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-973">Drivers Licence</span></span>
- <span data-ttu-id="fd62e-974">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-974">Drivers Licences</span></span>
- <span data-ttu-id="fd62e-975">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="fd62e-975">Driver'Lic</span></span>
- <span data-ttu-id="fd62e-976">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="fd62e-976">Driver'Lics</span></span>
- <span data-ttu-id="fd62e-977">Driver'License</span><span class="sxs-lookup"><span data-stu-id="fd62e-977">Driver'License</span></span>
- <span data-ttu-id="fd62e-978">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="fd62e-978">Driver'Licenses</span></span>
- <span data-ttu-id="fd62e-979">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="fd62e-979">Driver'Licence</span></span>
- <span data-ttu-id="fd62e-980">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="fd62e-980">Driver'Licences</span></span>
- <span data-ttu-id="fd62e-981">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-981">Driver' Lic</span></span>
- <span data-ttu-id="fd62e-982">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-982">Driver' Lics</span></span>
- <span data-ttu-id="fd62e-983">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-983">Driver' License</span></span>
- <span data-ttu-id="fd62e-984">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-984">Driver' Licenses</span></span>
- <span data-ttu-id="fd62e-985">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-985">Driver' Licence</span></span>
- <span data-ttu-id="fd62e-986">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-986">Driver' Licences</span></span>
- <span data-ttu-id="fd62e-987">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="fd62e-987">Driver'sLic</span></span>
- <span data-ttu-id="fd62e-988">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="fd62e-988">Driver'sLics</span></span>
- <span data-ttu-id="fd62e-989">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="fd62e-989">Driver'sLicense</span></span>
- <span data-ttu-id="fd62e-990">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="fd62e-990">Driver'sLicenses</span></span>
- <span data-ttu-id="fd62e-991">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="fd62e-991">Driver'sLicence</span></span>
- <span data-ttu-id="fd62e-992">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="fd62e-992">Driver'sLicences</span></span>
- <span data-ttu-id="fd62e-993">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-993">Driver's Lic</span></span>
- <span data-ttu-id="fd62e-994">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-994">Driver's Lics</span></span>
- <span data-ttu-id="fd62e-995">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-995">Driver's License</span></span>
- <span data-ttu-id="fd62e-996">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-996">Driver's Licenses</span></span>
- <span data-ttu-id="fd62e-997">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-997">Driver's Licence</span></span>
- <span data-ttu-id="fd62e-998">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-998">Driver's Licences</span></span>
- <span data-ttu-id="fd62e-999">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-999">Permis de Conduire</span></span>
- <span data-ttu-id="fd62e-1000">id</span><span class="sxs-lookup"><span data-stu-id="fd62e-1000">id</span></span>
- <span data-ttu-id="fd62e-1001">Ids</span><span class="sxs-lookup"><span data-stu-id="fd62e-1001">ids</span></span>
- <span data-ttu-id="fd62e-1002">numéro carte d’identification</span><span class="sxs-lookup"><span data-stu-id="fd62e-1002">idcard number</span></span>
- <span data-ttu-id="fd62e-1003">numéros carte d’identification</span><span class="sxs-lookup"><span data-stu-id="fd62e-1003">idcard numbers</span></span>
- <span data-ttu-id="fd62e-1004"># carte d’identification</span><span class="sxs-lookup"><span data-stu-id="fd62e-1004">idcard #</span></span>
- <span data-ttu-id="fd62e-1005"># carte d’identification</span><span class="sxs-lookup"><span data-stu-id="fd62e-1005">idcard #s</span></span>
- <span data-ttu-id="fd62e-1006">carte d’identification</span><span class="sxs-lookup"><span data-stu-id="fd62e-1006">idcard card</span></span>
- <span data-ttu-id="fd62e-1007">cartes d’identification</span><span class="sxs-lookup"><span data-stu-id="fd62e-1007">idcard cards</span></span>
- <span data-ttu-id="fd62e-1008">carte d’identification</span><span class="sxs-lookup"><span data-stu-id="fd62e-1008">idcard</span></span>
- <span data-ttu-id="fd62e-1009">numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="fd62e-1009">identification number</span></span>
- <span data-ttu-id="fd62e-1010">numéros d’identification</span><span class="sxs-lookup"><span data-stu-id="fd62e-1010">identification numbers</span></span>
- <span data-ttu-id="fd62e-1011"># identification</span><span class="sxs-lookup"><span data-stu-id="fd62e-1011">identification #</span></span>
- <span data-ttu-id="fd62e-1012"># identification</span><span class="sxs-lookup"><span data-stu-id="fd62e-1012">identification #s</span></span>
- <span data-ttu-id="fd62e-1013">carte d’identification</span><span class="sxs-lookup"><span data-stu-id="fd62e-1013">identification card</span></span>
- <span data-ttu-id="fd62e-1014">cartes d’identification</span><span class="sxs-lookup"><span data-stu-id="fd62e-1014">identification cards</span></span>
- <span data-ttu-id="fd62e-1015">identificateur</span><span class="sxs-lookup"><span data-stu-id="fd62e-1015">identification</span></span> 
- <span data-ttu-id="fd62e-1016">LD #</span><span class="sxs-lookup"><span data-stu-id="fd62e-1016">DL#</span></span>
- <span data-ttu-id="fd62e-1017">DISTRIBUTION #</span><span class="sxs-lookup"><span data-stu-id="fd62e-1017">DLS#</span></span> 
- <span data-ttu-id="fd62e-1018">CÈDE #</span><span class="sxs-lookup"><span data-stu-id="fd62e-1018">CDL#</span></span> 
- <span data-ttu-id="fd62e-1019">CDLS #</span><span class="sxs-lookup"><span data-stu-id="fd62e-1019">CDLS#</span></span> 
- <span data-ttu-id="fd62e-1020">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="fd62e-1020">DriverLic#</span></span> 
- <span data-ttu-id="fd62e-1021">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="fd62e-1021">DriverLics#</span></span> 
- <span data-ttu-id="fd62e-1022">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="fd62e-1022">DriverLicense#</span></span> 
- <span data-ttu-id="fd62e-1023">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="fd62e-1023">DriverLicenses#</span></span> 
- <span data-ttu-id="fd62e-1024">DriverLicence #</span><span class="sxs-lookup"><span data-stu-id="fd62e-1024">DriverLicence#</span></span> 
- <span data-ttu-id="fd62e-1025">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="fd62e-1025">DriverLicences#</span></span> 
- <span data-ttu-id="fd62e-1026">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-1026">Driver Lic#</span></span>
- <span data-ttu-id="fd62e-1027">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-1027">Driver Lics#</span></span> 
- <span data-ttu-id="fd62e-1028">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-1028">Driver License#</span></span> 
- <span data-ttu-id="fd62e-1029">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-1029">Driver Licenses#</span></span> 
- <span data-ttu-id="fd62e-1030">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-1030">Driver License#</span></span> 
- <span data-ttu-id="fd62e-1031">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-1031">Driver Licences#</span></span> 
- <span data-ttu-id="fd62e-1032">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="fd62e-1032">DriversLic#</span></span> 
- <span data-ttu-id="fd62e-1033">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="fd62e-1033">DriversLics#</span></span> 
- <span data-ttu-id="fd62e-1034">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="fd62e-1034">DriversLicense#</span></span> 
- <span data-ttu-id="fd62e-1035">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="fd62e-1035">DriversLicenses#</span></span> 
- <span data-ttu-id="fd62e-1036">DriversLicence #</span><span class="sxs-lookup"><span data-stu-id="fd62e-1036">DriversLicence#</span></span> 
- <span data-ttu-id="fd62e-1037">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="fd62e-1037">DriversLicences#</span></span> 
- <span data-ttu-id="fd62e-1038">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-1038">Drivers Lic#</span></span> 
- <span data-ttu-id="fd62e-1039">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-1039">Drivers Lics#</span></span> 
- <span data-ttu-id="fd62e-1040">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-1040">Drivers License#</span></span> 
- <span data-ttu-id="fd62e-1041">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-1041">Drivers Licenses#</span></span> 
- <span data-ttu-id="fd62e-1042">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-1042">Drivers Licence#</span></span> 
- <span data-ttu-id="fd62e-1043">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-1043">Drivers Licences#</span></span> 
- <span data-ttu-id="fd62e-1044">Driver'Lic #</span><span class="sxs-lookup"><span data-stu-id="fd62e-1044">Driver'Lic#</span></span> 
- <span data-ttu-id="fd62e-1045">Driver'Lics #</span><span class="sxs-lookup"><span data-stu-id="fd62e-1045">Driver'Lics#</span></span> 
- <span data-ttu-id="fd62e-1046">Driver'License #</span><span class="sxs-lookup"><span data-stu-id="fd62e-1046">Driver'License#</span></span> 
- <span data-ttu-id="fd62e-1047">Driver'Licenses #</span><span class="sxs-lookup"><span data-stu-id="fd62e-1047">Driver'Licenses#</span></span> 
- <span data-ttu-id="fd62e-1048">Driver'Licence #</span><span class="sxs-lookup"><span data-stu-id="fd62e-1048">Driver'Licence#</span></span> 
- <span data-ttu-id="fd62e-1049">Driver'Licences #</span><span class="sxs-lookup"><span data-stu-id="fd62e-1049">Driver'Licences#</span></span> 
- <span data-ttu-id="fd62e-1050">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-1050">Driver' Lic#</span></span> 
- <span data-ttu-id="fd62e-1051">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-1051">Driver' Lics#</span></span> 
- <span data-ttu-id="fd62e-1052">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-1052">Driver' License#</span></span> 
- <span data-ttu-id="fd62e-1053">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-1053">Driver' Licenses#</span></span> 
- <span data-ttu-id="fd62e-1054">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-1054">Driver' Licence#</span></span> 
- <span data-ttu-id="fd62e-1055">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-1055">Driver' Licences#</span></span> 
- <span data-ttu-id="fd62e-1056">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="fd62e-1056">Driver'sLic#</span></span> 
- <span data-ttu-id="fd62e-1057">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="fd62e-1057">Driver'sLics#</span></span> 
- <span data-ttu-id="fd62e-1058">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="fd62e-1058">Driver'sLicense#</span></span> 
- <span data-ttu-id="fd62e-1059">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="fd62e-1059">Driver'sLicenses#</span></span> 
- <span data-ttu-id="fd62e-1060">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="fd62e-1060">Driver'sLicence#</span></span> 
- <span data-ttu-id="fd62e-1061">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="fd62e-1061">Driver'sLicences#</span></span> 
- <span data-ttu-id="fd62e-1062">#Permisconduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-1062">Driver's Lic#</span></span> 
- <span data-ttu-id="fd62e-1063">#Permisconduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-1063">Driver's Lics#</span></span> 
- <span data-ttu-id="fd62e-1064">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-1064">Driver's License#</span></span> 
- <span data-ttu-id="fd62e-1065">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-1065">Driver's Licenses#</span></span> 
- <span data-ttu-id="fd62e-1066">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-1066">Driver's Licence#</span></span> 
- <span data-ttu-id="fd62e-1067">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-1067">Driver's Licences#</span></span> 
- <span data-ttu-id="fd62e-1068">Permis de conduire #</span><span class="sxs-lookup"><span data-stu-id="fd62e-1068">Permis de Conduire#</span></span> 
- <span data-ttu-id="fd62e-1069">Réf #</span><span class="sxs-lookup"><span data-stu-id="fd62e-1069">id#</span></span> 
- <span data-ttu-id="fd62e-1070">codes #</span><span class="sxs-lookup"><span data-stu-id="fd62e-1070">ids#</span></span> 
- <span data-ttu-id="fd62e-1071">#carte carte d’identification</span><span class="sxs-lookup"><span data-stu-id="fd62e-1071">idcard card#</span></span> 
- <span data-ttu-id="fd62e-1072">#cartes carte d’identification</span><span class="sxs-lookup"><span data-stu-id="fd62e-1072">idcard cards#</span></span> 
- <span data-ttu-id="fd62e-1073">carte d’identification #</span><span class="sxs-lookup"><span data-stu-id="fd62e-1073">idcard#</span></span> 
- <span data-ttu-id="fd62e-1074">#carte d’identification</span><span class="sxs-lookup"><span data-stu-id="fd62e-1074">identification card#</span></span> 
- <span data-ttu-id="fd62e-1075">#cartes d’identification</span><span class="sxs-lookup"><span data-stu-id="fd62e-1075">identification cards#</span></span> 
- <span data-ttu-id="fd62e-1076">identificateur #</span><span class="sxs-lookup"><span data-stu-id="fd62e-1076">identification#</span></span> 
   
## <a name="canada-health-service-number"></a><span data-ttu-id="fd62e-1077">Numéro de service de santé Canada</span><span class="sxs-lookup"><span data-stu-id="fd62e-1077">Canada Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-1078">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-1078">Format</span></span>

<span data-ttu-id="fd62e-1079">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-1079">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-1080">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-1080">Pattern</span></span>

<span data-ttu-id="fd62e-1081">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-1081">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-1082">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-1082">Checksum</span></span>

<span data-ttu-id="fd62e-1083">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-1083">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-1084">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-1084">Definition</span></span>

<span data-ttu-id="fd62e-1085">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-1085">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-1086">L’expression régulière Regex_canada_health_service_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1086">The regular expression Regex_canada_health_service_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-1087">Un mot clé figurant dans la liste Keyword_canada_health_service_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1087">A keyword from Keyword_canada_health_service_number is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-1088">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-1088">Keywords</span></span>

#### <a name="keyword_canada_health_service_number"></a><span data-ttu-id="fd62e-1089">Keyword_canada_health_service_number</span><span class="sxs-lookup"><span data-stu-id="fd62e-1089">Keyword_canada_health_service_number</span></span>

- <span data-ttu-id="fd62e-1090">numéro d’assurance-maladie</span><span class="sxs-lookup"><span data-stu-id="fd62e-1090">personal health number</span></span>
- <span data-ttu-id="fd62e-1091">informations sur le patient</span><span class="sxs-lookup"><span data-stu-id="fd62e-1091">patient information</span></span>
- <span data-ttu-id="fd62e-1092">services de santé</span><span class="sxs-lookup"><span data-stu-id="fd62e-1092">health services</span></span>
- <span data-ttu-id="fd62e-1093">services spécialisés</span><span class="sxs-lookup"><span data-stu-id="fd62e-1093">speciality services</span></span>
- <span data-ttu-id="fd62e-1094">accident automobile</span><span class="sxs-lookup"><span data-stu-id="fd62e-1094">automobile accident</span></span>
- <span data-ttu-id="fd62e-1095">hôpital pour malades</span><span class="sxs-lookup"><span data-stu-id="fd62e-1095">patient hospital</span></span>
- <span data-ttu-id="fd62e-1096">psychiatrist</span><span class="sxs-lookup"><span data-stu-id="fd62e-1096">psychiatrist</span></span>
- <span data-ttu-id="fd62e-1097">indemnisation des salariés</span><span class="sxs-lookup"><span data-stu-id="fd62e-1097">workers compensation</span></span>
- <span data-ttu-id="fd62e-1098">incapacité</span><span class="sxs-lookup"><span data-stu-id="fd62e-1098">disability</span></span>
      
## <a name="canada-passport-number"></a><span data-ttu-id="fd62e-1099">Numéro de passeport Canada</span><span class="sxs-lookup"><span data-stu-id="fd62e-1099">Canada Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-1100">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-1100">Format</span></span>

<span data-ttu-id="fd62e-1101">Deux lettres majuscules suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-1101">Two uppercase letters followed by six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-1102">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-1102">Pattern</span></span>

<span data-ttu-id="fd62e-1103">Deux lettres majuscules suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-1103">Two uppercase letters followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-1104">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-1104">Checksum</span></span>

<span data-ttu-id="fd62e-1105">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-1105">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-1106">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-1106">Definition</span></span>

<span data-ttu-id="fd62e-1107">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-1107">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-1108">L’expression régulière Regex_canada_passport_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1108">The regular expression Regex_canada_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-1109">Un mot clé depuis Keyword_canada_passport_number ou Keyword_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1109">A keyword from Keyword_canada_passport_number or Keyword_passport is found.</span></span>

```xml 
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

### <a name="keywords"></a><span data-ttu-id="fd62e-1110">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-1110">Keywords</span></span>

#### <a name="keyword_canada_passport_number"></a><span data-ttu-id="fd62e-1111">Keyword_canada_passport_number</span><span class="sxs-lookup"><span data-stu-id="fd62e-1111">Keyword_canada_passport_number</span></span>

- <span data-ttu-id="fd62e-1112">citoyenneté canadienne</span><span class="sxs-lookup"><span data-stu-id="fd62e-1112">canadian citizenship</span></span>
- <span data-ttu-id="fd62e-1113">passeport canadien</span><span class="sxs-lookup"><span data-stu-id="fd62e-1113">canadian passport</span></span>
- <span data-ttu-id="fd62e-1114">demande de passeport</span><span class="sxs-lookup"><span data-stu-id="fd62e-1114">passport application</span></span>
- <span data-ttu-id="fd62e-1115">photos pour passeport</span><span class="sxs-lookup"><span data-stu-id="fd62e-1115">passport photos</span></span>
- <span data-ttu-id="fd62e-1116">traducteur agréé</span><span class="sxs-lookup"><span data-stu-id="fd62e-1116">certified translator</span></span>
- <span data-ttu-id="fd62e-1117">citoyens canadiens</span><span class="sxs-lookup"><span data-stu-id="fd62e-1117">canadian citizens</span></span>
- <span data-ttu-id="fd62e-1118">temps de traitement</span><span class="sxs-lookup"><span data-stu-id="fd62e-1118">processing times</span></span>
- <span data-ttu-id="fd62e-1119">demande de renouvellement</span><span class="sxs-lookup"><span data-stu-id="fd62e-1119">renewal application</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="fd62e-1120">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="fd62e-1120">Keyword_passport</span></span>

- <span data-ttu-id="fd62e-1121">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="fd62e-1121">Passport Number</span></span>
- <span data-ttu-id="fd62e-1122">N° de passeport</span><span class="sxs-lookup"><span data-stu-id="fd62e-1122">Passport No</span></span>
- <span data-ttu-id="fd62e-1123"># Passeport</span><span class="sxs-lookup"><span data-stu-id="fd62e-1123">Passport #</span></span>
- <span data-ttu-id="fd62e-1124">Tel #</span><span class="sxs-lookup"><span data-stu-id="fd62e-1124">Passport#</span></span>
- <span data-ttu-id="fd62e-1125">PassportID</span><span class="sxs-lookup"><span data-stu-id="fd62e-1125">PassportID</span></span>
- <span data-ttu-id="fd62e-1126">N ° passeport</span><span class="sxs-lookup"><span data-stu-id="fd62e-1126">Passportno</span></span>
- <span data-ttu-id="fd62e-1127">passportnumber</span><span class="sxs-lookup"><span data-stu-id="fd62e-1127">passportnumber</span></span>
- <span data-ttu-id="fd62e-1128">パスポート</span><span class="sxs-lookup"><span data-stu-id="fd62e-1128">パスポート</span></span>
- <span data-ttu-id="fd62e-1129">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="fd62e-1129">パスポート番号</span></span>
- <span data-ttu-id="fd62e-1130">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="fd62e-1130">パスポートのNum</span></span>
- <span data-ttu-id="fd62e-1131">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="fd62e-1131">パスポート＃</span></span>
- <span data-ttu-id="fd62e-1132">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="fd62e-1132">Numéro de passeport</span></span>
- <span data-ttu-id="fd62e-1133">Passeport n°</span><span class="sxs-lookup"><span data-stu-id="fd62e-1133">Passeport n °</span></span>
- <span data-ttu-id="fd62e-1134">Passeport numéro</span><span class="sxs-lookup"><span data-stu-id="fd62e-1134">Passeport Non</span></span>
- <span data-ttu-id="fd62e-1135"># Passeport</span><span class="sxs-lookup"><span data-stu-id="fd62e-1135">Passeport #</span></span>
- <span data-ttu-id="fd62e-1136">Passeport #</span><span class="sxs-lookup"><span data-stu-id="fd62e-1136">Passeport#</span></span>
- <span data-ttu-id="fd62e-1137">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="fd62e-1137">PasseportNon</span></span>
- <span data-ttu-id="fd62e-1138">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="fd62e-1138">Passeportn °</span></span>
   
## <a name="canada-personal-health-identification-number-phin"></a><span data-ttu-id="fd62e-1139">NIMP (numéro d’identification médicale personnel) Canada</span><span class="sxs-lookup"><span data-stu-id="fd62e-1139">Canada Personal Health Identification Number (PHIN)</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-1140">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-1140">Format</span></span>

<span data-ttu-id="fd62e-1141">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-1141">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-1142">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-1142">Pattern</span></span>

<span data-ttu-id="fd62e-1143">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-1143">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-1144">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-1144">Checksum</span></span>

<span data-ttu-id="fd62e-1145">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-1145">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-1146">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-1146">Definition</span></span>

<span data-ttu-id="fd62e-1147">Une stratégie DLP est sûre à 75% d’avoir détecté ce type d’informations sensibles si, dans une proximité de 300 caractères: l’expression régulière Regex_canada_phin trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1147">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_canada_phin finds content that matches the pattern.</span></span>
<span data-ttu-id="fd62e-1148">Au moins deux mots clés de Keyword_canada_phin ou Keyword_canada_provinces sont trouvés..</span><span class="sxs-lookup"><span data-stu-id="fd62e-1148">At least two keywords from Keyword_canada_phin or Keyword_canada_provinces are found..</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-1149">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-1149">Keywords</span></span>

#### <a name="keyword_canada_phin"></a><span data-ttu-id="fd62e-1150">Keyword_canada_phin</span><span class="sxs-lookup"><span data-stu-id="fd62e-1150">Keyword_canada_phin</span></span>

- <span data-ttu-id="fd62e-1151">numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="fd62e-1151">social insurance number</span></span>
- <span data-ttu-id="fd62e-1152">loi sur les renseignements médicaux</span><span class="sxs-lookup"><span data-stu-id="fd62e-1152">health information act</span></span>
- <span data-ttu-id="fd62e-1153">renseignements relatifs à l’impôt sur le revenu</span><span class="sxs-lookup"><span data-stu-id="fd62e-1153">income tax information</span></span>
- <span data-ttu-id="fd62e-1154">santé Manitoba</span><span class="sxs-lookup"><span data-stu-id="fd62e-1154">manitoba health</span></span>
- <span data-ttu-id="fd62e-1155">enregistrement aux services de santé</span><span class="sxs-lookup"><span data-stu-id="fd62e-1155">health registration</span></span>
- <span data-ttu-id="fd62e-1156">achats de médicaments sur ordonnance</span><span class="sxs-lookup"><span data-stu-id="fd62e-1156">prescription purchases</span></span>
- <span data-ttu-id="fd62e-1157">admissibilité aux prestations</span><span class="sxs-lookup"><span data-stu-id="fd62e-1157">benefit eligibility</span></span>
- <span data-ttu-id="fd62e-1158">santé personnelle</span><span class="sxs-lookup"><span data-stu-id="fd62e-1158">personal health</span></span>
- <span data-ttu-id="fd62e-1159">procuration</span><span class="sxs-lookup"><span data-stu-id="fd62e-1159">power of attorney</span></span>
- <span data-ttu-id="fd62e-1160">numéro d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="fd62e-1160">registration number</span></span>
- <span data-ttu-id="fd62e-1161">numéro d’assurance-maladie</span><span class="sxs-lookup"><span data-stu-id="fd62e-1161">personal health number</span></span>
- <span data-ttu-id="fd62e-1162">recommandation par le médecin</span><span class="sxs-lookup"><span data-stu-id="fd62e-1162">practitioner referral</span></span>
- <span data-ttu-id="fd62e-1163">professionnel de bien-être</span><span class="sxs-lookup"><span data-stu-id="fd62e-1163">wellness professional</span></span>
- <span data-ttu-id="fd62e-1164">orientation d’un patient</span><span class="sxs-lookup"><span data-stu-id="fd62e-1164">patient referral</span></span>
- <span data-ttu-id="fd62e-1165">santé et bien-être</span><span class="sxs-lookup"><span data-stu-id="fd62e-1165">health and wellness</span></span>

#### <a name="keyword_canada_provinces"></a><span data-ttu-id="fd62e-1166">Keyword_canada_provinces</span><span class="sxs-lookup"><span data-stu-id="fd62e-1166">Keyword_canada_provinces</span></span>

- <span data-ttu-id="fd62e-1167">Nunavut</span><span class="sxs-lookup"><span data-stu-id="fd62e-1167">Nunavut</span></span>
- <span data-ttu-id="fd62e-1168">Régime</span><span class="sxs-lookup"><span data-stu-id="fd62e-1168">Quebec</span></span>
- <span data-ttu-id="fd62e-1169">Territoires du Nord-Ouest</span><span class="sxs-lookup"><span data-stu-id="fd62e-1169">Northwest Territories</span></span>
- <span data-ttu-id="fd62e-1170">Brand</span><span class="sxs-lookup"><span data-stu-id="fd62e-1170">Ontario</span></span>
- <span data-ttu-id="fd62e-1171">Colombie-britannique</span><span class="sxs-lookup"><span data-stu-id="fd62e-1171">British Columbia</span></span>
- <span data-ttu-id="fd62e-1172">Alberta</span><span class="sxs-lookup"><span data-stu-id="fd62e-1172">Alberta</span></span>
- <span data-ttu-id="fd62e-1173">En-dessus</span><span class="sxs-lookup"><span data-stu-id="fd62e-1173">Saskatchewan</span></span>
- <span data-ttu-id="fd62e-1174">Manitoba</span><span class="sxs-lookup"><span data-stu-id="fd62e-1174">Manitoba</span></span>
- <span data-ttu-id="fd62e-1175">Yukon</span><span class="sxs-lookup"><span data-stu-id="fd62e-1175">Yukon</span></span>
- <span data-ttu-id="fd62e-1176">Terre-Neuve-et-Labrador</span><span class="sxs-lookup"><span data-stu-id="fd62e-1176">Newfoundland and Labrador</span></span>
- <span data-ttu-id="fd62e-1177">Nouveau-Brunswick</span><span class="sxs-lookup"><span data-stu-id="fd62e-1177">New Brunswick</span></span>
- <span data-ttu-id="fd62e-1178">Nouvelle-Écosse</span><span class="sxs-lookup"><span data-stu-id="fd62e-1178">Nova Scotia</span></span>
- <span data-ttu-id="fd62e-1179">Île-du-Prince-Édouard</span><span class="sxs-lookup"><span data-stu-id="fd62e-1179">Prince Edward Island</span></span>
- <span data-ttu-id="fd62e-1180">Canada</span><span class="sxs-lookup"><span data-stu-id="fd62e-1180">Canada</span></span>
   
## <a name="canada-social-insurance-number"></a><span data-ttu-id="fd62e-1181">Numéro d'assurance sociale Canada</span><span class="sxs-lookup"><span data-stu-id="fd62e-1181">Canada Social Insurance Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-1182">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-1182">Format</span></span>

<span data-ttu-id="fd62e-1183">Neuf chiffres avec éventuellement des traits d’union ou des espaces</span><span class="sxs-lookup"><span data-stu-id="fd62e-1183">Nine digits with optional hyphens or spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-1184">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-1184">Pattern</span></span>

<span data-ttu-id="fd62e-1185">Avec</span><span class="sxs-lookup"><span data-stu-id="fd62e-1185">Formatted:</span></span>
- <span data-ttu-id="fd62e-1186">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-1186">Three digits</span></span> 
- <span data-ttu-id="fd62e-1187">Un trait d’union ou un espace</span><span class="sxs-lookup"><span data-stu-id="fd62e-1187">A hyphen or space</span></span> 
- <span data-ttu-id="fd62e-1188">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-1188">Three digits</span></span> 
- <span data-ttu-id="fd62e-1189">Un trait d’union ou un espace</span><span class="sxs-lookup"><span data-stu-id="fd62e-1189">A hyphen or space</span></span> 
- <span data-ttu-id="fd62e-1190">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-1190">Three digits</span></span>

<span data-ttu-id="fd62e-1191">Non mis en forme: neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-1191">Unformatted: Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-1192">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-1192">Checksum</span></span>

<span data-ttu-id="fd62e-1193">Oui</span><span class="sxs-lookup"><span data-stu-id="fd62e-1193">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-1194">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-1194">Definition</span></span>

<span data-ttu-id="fd62e-1195">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-1195">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-1196">La fonction Func_canadian_sin trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1196">The function Func_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-1197">Au moins deux des éléments suivants, quelle que soit la combinaison :</span><span class="sxs-lookup"><span data-stu-id="fd62e-1197">At least two of any combination of the following:</span></span>
    - <span data-ttu-id="fd62e-1198">Un mot clé figurant dans la liste Keyword_sin est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1198">A keyword from Keyword_sin is found.</span></span>
    - <span data-ttu-id="fd62e-1199">Un mot clé figurant dans la liste Keyword_sin_collaborative est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1199">A keyword from Keyword_sin_collaborative is found.</span></span>
    - <span data-ttu-id="fd62e-1200">La fonction Func_eu_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1200">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="fd62e-1201">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1201">The checksum passes.</span></span>

<span data-ttu-id="fd62e-1202">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-1202">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-1203">La fonction Func_unformatted_canadian_sin trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1203">The function Func_unformatted_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-1204">Un mot clé figurant dans la liste Keyword_sin est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1204">A keyword from Keyword_sin is found.</span></span>
- <span data-ttu-id="fd62e-1205">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1205">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-1206">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-1206">Keywords</span></span>

#### <a name="keyword_sin"></a><span data-ttu-id="fd62e-1207">Keyword_sin</span><span class="sxs-lookup"><span data-stu-id="fd62e-1207">Keyword_sin</span></span>

- <span data-ttu-id="fd62e-1208">assoc</span><span class="sxs-lookup"><span data-stu-id="fd62e-1208">sin</span></span> 
- <span data-ttu-id="fd62e-1209">assurance sociale</span><span class="sxs-lookup"><span data-stu-id="fd62e-1209">social insurance</span></span> 
- <span data-ttu-id="fd62e-1210">numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="fd62e-1210">numero d'assurance sociale</span></span> 
- <span data-ttu-id="fd62e-1211">péchés</span><span class="sxs-lookup"><span data-stu-id="fd62e-1211">sins</span></span> 
- <span data-ttu-id="fd62e-1212">SSN</span><span class="sxs-lookup"><span data-stu-id="fd62e-1212">ssn</span></span> 
- <span data-ttu-id="fd62e-1213">numéros</span><span class="sxs-lookup"><span data-stu-id="fd62e-1213">ssns</span></span> 
- <span data-ttu-id="fd62e-1214">sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="fd62e-1214">social security</span></span> 
- <span data-ttu-id="fd62e-1215">numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="fd62e-1215">numero d'assurance social</span></span> 
- <span data-ttu-id="fd62e-1216">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="fd62e-1216">national identification number</span></span> 
- <span data-ttu-id="fd62e-1217">id national</span><span class="sxs-lookup"><span data-stu-id="fd62e-1217">national id</span></span> 
- <span data-ttu-id="fd62e-1218">sine #</span><span class="sxs-lookup"><span data-stu-id="fd62e-1218">sin#</span></span> 
- <span data-ttu-id="fd62e-1219">ass soc</span><span class="sxs-lookup"><span data-stu-id="fd62e-1219">soc ins</span></span> 
- <span data-ttu-id="fd62e-1220">ass sociale</span><span class="sxs-lookup"><span data-stu-id="fd62e-1220">social ins</span></span> 

#### <a name="keyword_sin_collaborative"></a><span data-ttu-id="fd62e-1221">Keyword_sin_collaborative</span><span class="sxs-lookup"><span data-stu-id="fd62e-1221">Keyword_sin_collaborative</span></span>

- <span data-ttu-id="fd62e-1222">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-1222">driver's license</span></span> 
- <span data-ttu-id="fd62e-1223">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-1223">drivers license</span></span> 
- <span data-ttu-id="fd62e-1224">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-1224">driver's licence</span></span> 
- <span data-ttu-id="fd62e-1225">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-1225">drivers licence</span></span> 
- <span data-ttu-id="fd62e-1226">DOB</span><span class="sxs-lookup"><span data-stu-id="fd62e-1226">DOB</span></span> 
- <span data-ttu-id="fd62e-1227">Birthdate</span><span class="sxs-lookup"><span data-stu-id="fd62e-1227">Birthdate</span></span> 
- <span data-ttu-id="fd62e-1228">Birthday</span><span class="sxs-lookup"><span data-stu-id="fd62e-1228">Birthday</span></span> 
- <span data-ttu-id="fd62e-1229">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="fd62e-1229">Date of Birth</span></span> 
   
## <a name="chile-identity-card-number"></a><span data-ttu-id="fd62e-1230">	Numéro de carte d’identité Chili</span><span class="sxs-lookup"><span data-stu-id="fd62e-1230">Chile Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-1231">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-1231">Format</span></span>

<span data-ttu-id="fd62e-1232">7-8 chiffres plus des délimiteurs un chiffre ou une lettre</span><span class="sxs-lookup"><span data-stu-id="fd62e-1232">7-8 digits plus delimiters a check digit or letter</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-1233">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-1233">Pattern</span></span>

<span data-ttu-id="fd62e-1234">7 ou 8 chiffres, plus des délimiteurs :</span><span class="sxs-lookup"><span data-stu-id="fd62e-1234">7-8 digits plus delimiters:</span></span>
- <span data-ttu-id="fd62e-1235">1 ou 2 chiffres </span><span class="sxs-lookup"><span data-stu-id="fd62e-1235">1-2 digits</span></span> 
- <span data-ttu-id="fd62e-1236">Un point </span><span class="sxs-lookup"><span data-stu-id="fd62e-1236">A period</span></span> 
- <span data-ttu-id="fd62e-1237">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-1237">Three digits</span></span> 
- <span data-ttu-id="fd62e-1238">Un point </span><span class="sxs-lookup"><span data-stu-id="fd62e-1238">A period</span></span> 
- <span data-ttu-id="fd62e-1239">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-1239">Three digits</span></span> 
- <span data-ttu-id="fd62e-1240">Un tiret</span><span class="sxs-lookup"><span data-stu-id="fd62e-1240">A dash</span></span> 
- <span data-ttu-id="fd62e-1241">Un chiffre ou une lettre (ne respectant pas la casse) de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-1241">One digit or letter (not case sensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-1242">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-1242">Checksum</span></span>

<span data-ttu-id="fd62e-1243">Oui</span><span class="sxs-lookup"><span data-stu-id="fd62e-1243">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-1244">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-1244">Definition</span></span>

<span data-ttu-id="fd62e-1245">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-1245">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-1246">La fonction Func_chile_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1246">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-1247">Un mot clé figurant dans la liste Keyword_chile_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1247">A keyword from Keyword_chile_id_card is found.</span></span>
- <span data-ttu-id="fd62e-1248">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1248">The checksum passes.</span></span>

<span data-ttu-id="fd62e-1249">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-1249">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-1250">La fonction Func_chile_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1250">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-1251">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1251">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-1252">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-1252">Keywords</span></span>

#### <a name="keyword_chile_id_card"></a><span data-ttu-id="fd62e-1253">Keyword_chile_id_card</span><span class="sxs-lookup"><span data-stu-id="fd62e-1253">Keyword_chile_id_card</span></span>

- <span data-ttu-id="fd62e-1254">National Identification Number</span><span class="sxs-lookup"><span data-stu-id="fd62e-1254">National Identification Number</span></span> 
- <span data-ttu-id="fd62e-1255">Identity card</span><span class="sxs-lookup"><span data-stu-id="fd62e-1255">Identity card</span></span> 
- <span data-ttu-id="fd62e-1256">ID</span><span class="sxs-lookup"><span data-stu-id="fd62e-1256">ID</span></span> 
- <span data-ttu-id="fd62e-1257">Identificateur</span><span class="sxs-lookup"><span data-stu-id="fd62e-1257">Identification</span></span> 
- <span data-ttu-id="fd62e-1258">Rol Único Nacional</span><span class="sxs-lookup"><span data-stu-id="fd62e-1258">Rol Único Nacional</span></span> 
- <span data-ttu-id="fd62e-1259">GÉNÉRER</span><span class="sxs-lookup"><span data-stu-id="fd62e-1259">RUN</span></span> 
- <span data-ttu-id="fd62e-1260">Rol Único Tributario</span><span class="sxs-lookup"><span data-stu-id="fd62e-1260">Rol Único Tributario</span></span> 
- <span data-ttu-id="fd62e-1261">ROUTINE</span><span class="sxs-lookup"><span data-stu-id="fd62e-1261">RUT</span></span> 
- <span data-ttu-id="fd62e-1262">Cédula de Identidad</span><span class="sxs-lookup"><span data-stu-id="fd62e-1262">Cédula de Identidad</span></span> 
- <span data-ttu-id="fd62e-1263">Número De Identificación Nacional</span><span class="sxs-lookup"><span data-stu-id="fd62e-1263">Número De Identificación Nacional</span></span> 
- <span data-ttu-id="fd62e-1264">Tarjeta de identificación</span><span class="sxs-lookup"><span data-stu-id="fd62e-1264">Tarjeta de identificación</span></span> 
- <span data-ttu-id="fd62e-1265">Identificación</span><span class="sxs-lookup"><span data-stu-id="fd62e-1265">Identificación</span></span> 
   
## <a name="china-resident-identity-card-prc-number"></a><span data-ttu-id="fd62e-1266">	Numéro de carte d’identité de résident Chine (RPC)</span><span class="sxs-lookup"><span data-stu-id="fd62e-1266">China Resident Identity Card (PRC) Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-1267">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-1267">Format</span></span>

<span data-ttu-id="fd62e-1268">18 chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-1268">18 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-1269">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-1269">Pattern</span></span>

<span data-ttu-id="fd62e-1270">18 chiffres :</span><span class="sxs-lookup"><span data-stu-id="fd62e-1270">18 digits:</span></span>
- <span data-ttu-id="fd62e-1271">Six chiffres qui composent un code d’adresse </span><span class="sxs-lookup"><span data-stu-id="fd62e-1271">Six digits which are an address code</span></span> 
- <span data-ttu-id="fd62e-1272">Huit chiffres sous la forme AAAAMMJJ qui correspondent à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="fd62e-1272">Eight digits in the form YYYYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="fd62e-1273">Trois chiffres qui correspondent à un code d’opération </span><span class="sxs-lookup"><span data-stu-id="fd62e-1273">Three digits which are an order code</span></span> 
- <span data-ttu-id="fd62e-1274">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-1274">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-1275">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-1275">Checksum</span></span>

<span data-ttu-id="fd62e-1276">Oui</span><span class="sxs-lookup"><span data-stu-id="fd62e-1276">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-1277">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-1277">Definition</span></span>

<span data-ttu-id="fd62e-1278">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-1278">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-1279">La fonction Func_china_resident_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1279">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-1280">Un mot clé figurant dans la liste Keyword_china_resident_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1280">A keyword from Keyword_china_resident_id is found.</span></span>
- <span data-ttu-id="fd62e-1281">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1281">The checksum passes.</span></span>

<span data-ttu-id="fd62e-1282">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-1282">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-1283">La fonction Func_china_resident_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1283">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-1284">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1284">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-1285">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-1285">Keywords</span></span>

### <a name="keyword_china_resident_id"></a><span data-ttu-id="fd62e-1286">Keyword_china_resident_id</span><span class="sxs-lookup"><span data-stu-id="fd62e-1286">Keyword_china_resident_id</span></span>

- <span data-ttu-id="fd62e-1287">Resident Identity Card</span><span class="sxs-lookup"><span data-stu-id="fd62e-1287">Resident Identity Card</span></span> 
- <span data-ttu-id="fd62e-1288">FIGURANT</span><span class="sxs-lookup"><span data-stu-id="fd62e-1288">PRC</span></span> 
- <span data-ttu-id="fd62e-1289">National Identification Card</span><span class="sxs-lookup"><span data-stu-id="fd62e-1289">National Identification Card</span></span> 
- <span data-ttu-id="fd62e-1290">身份证</span><span class="sxs-lookup"><span data-stu-id="fd62e-1290">身份证</span></span> 
- <span data-ttu-id="fd62e-1291">居民 身份证</span><span class="sxs-lookup"><span data-stu-id="fd62e-1291">居民 身份证</span></span> 
- <span data-ttu-id="fd62e-1292">居民身份证</span><span class="sxs-lookup"><span data-stu-id="fd62e-1292">居民身份证</span></span> 
- <span data-ttu-id="fd62e-1293">鉴定</span><span class="sxs-lookup"><span data-stu-id="fd62e-1293">鉴定</span></span> 
- <span data-ttu-id="fd62e-1294">身分證</span><span class="sxs-lookup"><span data-stu-id="fd62e-1294">身分證</span></span> 
- <span data-ttu-id="fd62e-1295">居民 身份證</span><span class="sxs-lookup"><span data-stu-id="fd62e-1295">居民 身份證</span></span>
- <span data-ttu-id="fd62e-1296">鑑定</span><span class="sxs-lookup"><span data-stu-id="fd62e-1296">鑑定</span></span> 
   
## <a name="credit-card-number"></a><span data-ttu-id="fd62e-1297">Numéro de carte de crédit</span><span class="sxs-lookup"><span data-stu-id="fd62e-1297">Credit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-1298">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-1298">Format</span></span>

<span data-ttu-id="fd62e-1299">16 chiffres qui peuvent être mis en forme ou non (dddddddddddddddd) et doivent réussir le test Luhn.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1299">16 digits which can be formatted or unformatted (dddddddddddddddd) and must pass the Luhn test.</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-1300">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-1300">Pattern</span></span>

<span data-ttu-id="fd62e-1301">Modèle très complexe et puissant qui détecte les cartes de visite de toutes les principales marques du monde, notamment Visa, MasterCard, Discover Card, JCB, American Express, etc.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1301">Very complex and robust pattern that detects cards from all major brands worldwide, including Visa, MasterCard, Discover Card, JCB, American Express, gift cards, and diner cards.</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-1302">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-1302">Checksum</span></span>

<span data-ttu-id="fd62e-1303">Oui, la somme de contrôle de Luhn</span><span class="sxs-lookup"><span data-stu-id="fd62e-1303">Yes, the Luhn checksum</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-1304">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-1304">Definition</span></span>

<span data-ttu-id="fd62e-1305">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-1305">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-1306">La fonction Func_credit_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1306">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-1307">L’une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="fd62e-1307">One of the following is true:</span></span>
    - <span data-ttu-id="fd62e-1308">Un mot clé figurant dans la liste Keyword_cc_verification est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1308">A keyword from Keyword_cc_verification is found.</span></span>
    - <span data-ttu-id="fd62e-1309">Un mot clé figurant dans la liste Keyword_cc_name est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1309">A keyword from Keyword_cc_name is found.</span></span>
    - <span data-ttu-id="fd62e-1310">La fonction Func_expiration_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1310">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="fd62e-1311">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1311">The checksum passes.</span></span>

<span data-ttu-id="fd62e-1312">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-1312">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-1313">La fonction Func_credit_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1313">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-1314">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1314">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-1315">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-1315">Keywords</span></span>

#### <a name="keyword_cc_verification"></a><span data-ttu-id="fd62e-1316">Keyword_cc_verification</span><span class="sxs-lookup"><span data-stu-id="fd62e-1316">Keyword_cc_verification</span></span>

- <span data-ttu-id="fd62e-1317">vérification de la carte</span><span class="sxs-lookup"><span data-stu-id="fd62e-1317">card verification</span></span>
- <span data-ttu-id="fd62e-1318">numéro d’identification de la carte</span><span class="sxs-lookup"><span data-stu-id="fd62e-1318">card identification number</span></span>
- <span data-ttu-id="fd62e-1319">cryptogramme</span><span class="sxs-lookup"><span data-stu-id="fd62e-1319">cvn</span></span>
- <span data-ttu-id="fd62e-1320">nic</span><span class="sxs-lookup"><span data-stu-id="fd62e-1320">cid</span></span>
- <span data-ttu-id="fd62e-1321">cvc2</span><span class="sxs-lookup"><span data-stu-id="fd62e-1321">cvc2</span></span>
- <span data-ttu-id="fd62e-1322">cvv2</span><span class="sxs-lookup"><span data-stu-id="fd62e-1322">cvv2</span></span>
- <span data-ttu-id="fd62e-1323">pin block</span><span class="sxs-lookup"><span data-stu-id="fd62e-1323">pin block</span></span>
- <span data-ttu-id="fd62e-1324">code de sécurité</span><span class="sxs-lookup"><span data-stu-id="fd62e-1324">security code</span></span>
- <span data-ttu-id="fd62e-1325">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="fd62e-1325">security number</span></span>
- <span data-ttu-id="fd62e-1326">n° de sécurité</span><span class="sxs-lookup"><span data-stu-id="fd62e-1326">security no</span></span>
- <span data-ttu-id="fd62e-1327">numéro d’émission</span><span class="sxs-lookup"><span data-stu-id="fd62e-1327">issue number</span></span>
- <span data-ttu-id="fd62e-1328">n° d’émission</span><span class="sxs-lookup"><span data-stu-id="fd62e-1328">issue no</span></span>
- <span data-ttu-id="fd62e-1329">cryptogramme</span><span class="sxs-lookup"><span data-stu-id="fd62e-1329">cryptogramme</span></span>
- <span data-ttu-id="fd62e-1330">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="fd62e-1330">numéro de sécurité</span></span>
- <span data-ttu-id="fd62e-1331">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="fd62e-1331">numero de securite</span></span>
- <span data-ttu-id="fd62e-1332">kreditkartenprüfnummer</span><span class="sxs-lookup"><span data-stu-id="fd62e-1332">kreditkartenprüfnummer</span></span>
- <span data-ttu-id="fd62e-1333">kreditkartenprufnummer</span><span class="sxs-lookup"><span data-stu-id="fd62e-1333">kreditkartenprufnummer</span></span>
- <span data-ttu-id="fd62e-1334">prüfziffer</span><span class="sxs-lookup"><span data-stu-id="fd62e-1334">prüfziffer</span></span>
- <span data-ttu-id="fd62e-1335">prufziffer</span><span class="sxs-lookup"><span data-stu-id="fd62e-1335">prufziffer</span></span>
- <span data-ttu-id="fd62e-1336">sicherheits Kode</span><span class="sxs-lookup"><span data-stu-id="fd62e-1336">sicherheits Kode</span></span>
- <span data-ttu-id="fd62e-1337">sicherheitscode</span><span class="sxs-lookup"><span data-stu-id="fd62e-1337">sicherheitscode</span></span>
- <span data-ttu-id="fd62e-1338">sicherheitsnummer</span><span class="sxs-lookup"><span data-stu-id="fd62e-1338">sicherheitsnummer</span></span>
- <span data-ttu-id="fd62e-1339">verfalldatum</span><span class="sxs-lookup"><span data-stu-id="fd62e-1339">verfalldatum</span></span>
- <span data-ttu-id="fd62e-1340">codice di verifica</span><span class="sxs-lookup"><span data-stu-id="fd62e-1340">codice di verifica</span></span>
- <span data-ttu-id="fd62e-1341">contre.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1341">cod.</span></span> <span data-ttu-id="fd62e-1342">sicurezza</span><span class="sxs-lookup"><span data-stu-id="fd62e-1342">sicurezza</span></span>
- <span data-ttu-id="fd62e-1343">cod sicurezza</span><span class="sxs-lookup"><span data-stu-id="fd62e-1343">cod sicurezza</span></span>
- <span data-ttu-id="fd62e-1344">n autorizzazione</span><span class="sxs-lookup"><span data-stu-id="fd62e-1344">n autorizzazione</span></span>
- <span data-ttu-id="fd62e-1345">código</span><span class="sxs-lookup"><span data-stu-id="fd62e-1345">código</span></span>
- <span data-ttu-id="fd62e-1346">codigo</span><span class="sxs-lookup"><span data-stu-id="fd62e-1346">codigo</span></span>
- <span data-ttu-id="fd62e-1347">contre.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1347">cod.</span></span> <span data-ttu-id="fd62e-1348">SEG</span><span class="sxs-lookup"><span data-stu-id="fd62e-1348">seg</span></span>
- <span data-ttu-id="fd62e-1349">cod seg</span><span class="sxs-lookup"><span data-stu-id="fd62e-1349">cod seg</span></span>
- <span data-ttu-id="fd62e-1350">código de segurança</span><span class="sxs-lookup"><span data-stu-id="fd62e-1350">código de segurança</span></span>
- <span data-ttu-id="fd62e-1351">codigo de seguranca</span><span class="sxs-lookup"><span data-stu-id="fd62e-1351">codigo de seguranca</span></span>
- <span data-ttu-id="fd62e-1352">codigo de segurança</span><span class="sxs-lookup"><span data-stu-id="fd62e-1352">codigo de segurança</span></span>
- <span data-ttu-id="fd62e-1353">código de seguranca</span><span class="sxs-lookup"><span data-stu-id="fd62e-1353">código de seguranca</span></span>
- <span data-ttu-id="fd62e-1354">cód.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1354">cód.</span></span> <span data-ttu-id="fd62e-1355">segurança</span><span class="sxs-lookup"><span data-stu-id="fd62e-1355">segurança</span></span>
- <span data-ttu-id="fd62e-1356">contre.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1356">cod.</span></span> <span data-ttu-id="fd62e-1357">Seguranca COD.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1357">seguranca cod.</span></span> <span data-ttu-id="fd62e-1358">segurança</span><span class="sxs-lookup"><span data-stu-id="fd62e-1358">segurança</span></span>
- <span data-ttu-id="fd62e-1359">cód.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1359">cód.</span></span> <span data-ttu-id="fd62e-1360">seguranca</span><span class="sxs-lookup"><span data-stu-id="fd62e-1360">seguranca</span></span>
- <span data-ttu-id="fd62e-1361">cód segurança</span><span class="sxs-lookup"><span data-stu-id="fd62e-1361">cód segurança</span></span>
- <span data-ttu-id="fd62e-1362">COD Seguranca COD Segurança</span><span class="sxs-lookup"><span data-stu-id="fd62e-1362">cod seguranca cod segurança</span></span>
- <span data-ttu-id="fd62e-1363">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="fd62e-1363">cód seguranca</span></span>
- <span data-ttu-id="fd62e-1364">número de verificação</span><span class="sxs-lookup"><span data-stu-id="fd62e-1364">número de verificação</span></span>
- <span data-ttu-id="fd62e-1365">numero de verificacao</span><span class="sxs-lookup"><span data-stu-id="fd62e-1365">numero de verificacao</span></span>
- <span data-ttu-id="fd62e-1366">ablauf</span><span class="sxs-lookup"><span data-stu-id="fd62e-1366">ablauf</span></span>
- <span data-ttu-id="fd62e-1367">gültig bis</span><span class="sxs-lookup"><span data-stu-id="fd62e-1367">gültig bis</span></span>
- <span data-ttu-id="fd62e-1368">gültigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="fd62e-1368">gültigkeitsdatum</span></span>
- <span data-ttu-id="fd62e-1369">gultig bis</span><span class="sxs-lookup"><span data-stu-id="fd62e-1369">gultig bis</span></span>
- <span data-ttu-id="fd62e-1370">gultigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="fd62e-1370">gultigkeitsdatum</span></span>
- <span data-ttu-id="fd62e-1371">scadenza</span><span class="sxs-lookup"><span data-stu-id="fd62e-1371">scadenza</span></span>
- <span data-ttu-id="fd62e-1372">data scad</span><span class="sxs-lookup"><span data-stu-id="fd62e-1372">data scad</span></span>
- <span data-ttu-id="fd62e-1373">fecha de expiracion</span><span class="sxs-lookup"><span data-stu-id="fd62e-1373">fecha de expiracion</span></span>
- <span data-ttu-id="fd62e-1374">fecha de venc</span><span class="sxs-lookup"><span data-stu-id="fd62e-1374">fecha de venc</span></span>
- <span data-ttu-id="fd62e-1375">vencimiento</span><span class="sxs-lookup"><span data-stu-id="fd62e-1375">vencimiento</span></span>
- <span data-ttu-id="fd62e-1376">válido hasta</span><span class="sxs-lookup"><span data-stu-id="fd62e-1376">válido hasta</span></span>
- <span data-ttu-id="fd62e-1377">valido hasta</span><span class="sxs-lookup"><span data-stu-id="fd62e-1377">valido hasta</span></span>
- <span data-ttu-id="fd62e-1378">vto</span><span class="sxs-lookup"><span data-stu-id="fd62e-1378">vto</span></span>
- <span data-ttu-id="fd62e-1379">data de expiração</span><span class="sxs-lookup"><span data-stu-id="fd62e-1379">data de expiração</span></span>
- <span data-ttu-id="fd62e-1380">data de expiracao</span><span class="sxs-lookup"><span data-stu-id="fd62e-1380">data de expiracao</span></span>
- <span data-ttu-id="fd62e-1381">data em que expira</span><span class="sxs-lookup"><span data-stu-id="fd62e-1381">data em que expira</span></span>
- <span data-ttu-id="fd62e-1382">validade</span><span class="sxs-lookup"><span data-stu-id="fd62e-1382">validade</span></span>
- <span data-ttu-id="fd62e-1383">valorisation</span><span class="sxs-lookup"><span data-stu-id="fd62e-1383">valor</span></span>
- <span data-ttu-id="fd62e-1384">vencimento</span><span class="sxs-lookup"><span data-stu-id="fd62e-1384">vencimento</span></span>
- <span data-ttu-id="fd62e-1385">Venc</span><span class="sxs-lookup"><span data-stu-id="fd62e-1385">Venc</span></span> 

#### <a name="keyword_cc_name"></a><span data-ttu-id="fd62e-1386">Keyword_cc_name</span><span class="sxs-lookup"><span data-stu-id="fd62e-1386">Keyword_cc_name</span></span>

- <span data-ttu-id="fd62e-1387">American</span><span class="sxs-lookup"><span data-stu-id="fd62e-1387">amex</span></span>
- <span data-ttu-id="fd62e-1388">american express</span><span class="sxs-lookup"><span data-stu-id="fd62e-1388">american express</span></span>
- <span data-ttu-id="fd62e-1389">americanexpress</span><span class="sxs-lookup"><span data-stu-id="fd62e-1389">americanexpress</span></span>
- <span data-ttu-id="fd62e-1390">Délivrance</span><span class="sxs-lookup"><span data-stu-id="fd62e-1390">Visa</span></span>
- <span data-ttu-id="fd62e-1391">MasterCard</span><span class="sxs-lookup"><span data-stu-id="fd62e-1391">mastercard</span></span>
- <span data-ttu-id="fd62e-1392">master card</span><span class="sxs-lookup"><span data-stu-id="fd62e-1392">master card</span></span>
- <span data-ttu-id="fd62e-1393">McDonald</span><span class="sxs-lookup"><span data-stu-id="fd62e-1393">mc</span></span> 
- <span data-ttu-id="fd62e-1394">MasterCard</span><span class="sxs-lookup"><span data-stu-id="fd62e-1394">mastercards</span></span>
- <span data-ttu-id="fd62e-1395">master cards</span><span class="sxs-lookup"><span data-stu-id="fd62e-1395">master cards</span></span>
- <span data-ttu-id="fd62e-1396">diner’s Club</span><span class="sxs-lookup"><span data-stu-id="fd62e-1396">diner's Club</span></span>
- <span data-ttu-id="fd62e-1397">diners club</span><span class="sxs-lookup"><span data-stu-id="fd62e-1397">diners club</span></span>
- <span data-ttu-id="fd62e-1398">dinersclub</span><span class="sxs-lookup"><span data-stu-id="fd62e-1398">dinersclub</span></span>
- <span data-ttu-id="fd62e-1399">discover card</span><span class="sxs-lookup"><span data-stu-id="fd62e-1399">discover card</span></span>
- <span data-ttu-id="fd62e-1400">discovercard</span><span class="sxs-lookup"><span data-stu-id="fd62e-1400">discovercard</span></span>
- <span data-ttu-id="fd62e-1401">discover cards</span><span class="sxs-lookup"><span data-stu-id="fd62e-1401">discover cards</span></span>
- <span data-ttu-id="fd62e-1402">JCB</span><span class="sxs-lookup"><span data-stu-id="fd62e-1402">JCB</span></span>
- <span data-ttu-id="fd62e-1403">japanese card bureau</span><span class="sxs-lookup"><span data-stu-id="fd62e-1403">japanese card bureau</span></span>
- <span data-ttu-id="fd62e-1404">carte blanche</span><span class="sxs-lookup"><span data-stu-id="fd62e-1404">carte blanche</span></span>
- <span data-ttu-id="fd62e-1405">carteblanche</span><span class="sxs-lookup"><span data-stu-id="fd62e-1405">carteblanche</span></span>
- <span data-ttu-id="fd62e-1406">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="fd62e-1406">credit card</span></span>
- <span data-ttu-id="fd62e-1407">CC #</span><span class="sxs-lookup"><span data-stu-id="fd62e-1407">cc#</span></span>
- <span data-ttu-id="fd62e-1408">n ° de CC:</span><span class="sxs-lookup"><span data-stu-id="fd62e-1408">cc#:</span></span>
- <span data-ttu-id="fd62e-1409">date d’expiration</span><span class="sxs-lookup"><span data-stu-id="fd62e-1409">expiration date</span></span>
- <span data-ttu-id="fd62e-1410">date d’exp</span><span class="sxs-lookup"><span data-stu-id="fd62e-1410">exp date</span></span>
- <span data-ttu-id="fd62e-1411">date d’expiration</span><span class="sxs-lookup"><span data-stu-id="fd62e-1411">expiry date</span></span>
- <span data-ttu-id="fd62e-1412">date d’expiration</span><span class="sxs-lookup"><span data-stu-id="fd62e-1412">date d’expiration</span></span>
- <span data-ttu-id="fd62e-1413">date d’exp</span><span class="sxs-lookup"><span data-stu-id="fd62e-1413">date d'exp</span></span>
- <span data-ttu-id="fd62e-1414">date expiration</span><span class="sxs-lookup"><span data-stu-id="fd62e-1414">date expiration</span></span>
- <span data-ttu-id="fd62e-1415">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="fd62e-1415">bank card</span></span>
- <span data-ttu-id="fd62e-1416">bankcard</span><span class="sxs-lookup"><span data-stu-id="fd62e-1416">bankcard</span></span>
- <span data-ttu-id="fd62e-1417">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="fd62e-1417">card number</span></span>
- <span data-ttu-id="fd62e-1418">num de carte</span><span class="sxs-lookup"><span data-stu-id="fd62e-1418">card num</span></span>
- <span data-ttu-id="fd62e-1419">carte</span><span class="sxs-lookup"><span data-stu-id="fd62e-1419">cardnumber</span></span>
- <span data-ttu-id="fd62e-1420">carte</span><span class="sxs-lookup"><span data-stu-id="fd62e-1420">cardnumbers</span></span>
- <span data-ttu-id="fd62e-1421">numéros de carte</span><span class="sxs-lookup"><span data-stu-id="fd62e-1421">card numbers</span></span>
- <span data-ttu-id="fd62e-1422">CreditCard</span><span class="sxs-lookup"><span data-stu-id="fd62e-1422">creditcard</span></span>
- <span data-ttu-id="fd62e-1423">cartes de crédit</span><span class="sxs-lookup"><span data-stu-id="fd62e-1423">credit cards</span></span>
- <span data-ttu-id="fd62e-1424">crédit</span><span class="sxs-lookup"><span data-stu-id="fd62e-1424">creditcards</span></span>
- <span data-ttu-id="fd62e-1425">CCN</span><span class="sxs-lookup"><span data-stu-id="fd62e-1425">ccn</span></span>
- <span data-ttu-id="fd62e-1426">titulaire de la carte</span><span class="sxs-lookup"><span data-stu-id="fd62e-1426">card holder</span></span>
- <span data-ttu-id="fd62e-1427">titulaires</span><span class="sxs-lookup"><span data-stu-id="fd62e-1427">cardholder</span></span>
- <span data-ttu-id="fd62e-1428">titulaires de la carte</span><span class="sxs-lookup"><span data-stu-id="fd62e-1428">card holders</span></span>
- <span data-ttu-id="fd62e-1429">titulaires</span><span class="sxs-lookup"><span data-stu-id="fd62e-1429">cardholders</span></span>
- <span data-ttu-id="fd62e-1430">carte de vérification</span><span class="sxs-lookup"><span data-stu-id="fd62e-1430">check card</span></span>
- <span data-ttu-id="fd62e-1431">carte</span><span class="sxs-lookup"><span data-stu-id="fd62e-1431">checkcard</span></span>
- <span data-ttu-id="fd62e-1432">cartes de vérification</span><span class="sxs-lookup"><span data-stu-id="fd62e-1432">check cards</span></span>
- <span data-ttu-id="fd62e-1433">cartes</span><span class="sxs-lookup"><span data-stu-id="fd62e-1433">checkcards</span></span>
- <span data-ttu-id="fd62e-1434">carte de débit</span><span class="sxs-lookup"><span data-stu-id="fd62e-1434">debit card</span></span>
- <span data-ttu-id="fd62e-1435">débit</span><span class="sxs-lookup"><span data-stu-id="fd62e-1435">debitcard</span></span>
- <span data-ttu-id="fd62e-1436">cartes de débit</span><span class="sxs-lookup"><span data-stu-id="fd62e-1436">debit cards</span></span>
- <span data-ttu-id="fd62e-1437">débit</span><span class="sxs-lookup"><span data-stu-id="fd62e-1437">debitcards</span></span>
- <span data-ttu-id="fd62e-1438">carte de retrait</span><span class="sxs-lookup"><span data-stu-id="fd62e-1438">atm card</span></span>
- <span data-ttu-id="fd62e-1439">retrait</span><span class="sxs-lookup"><span data-stu-id="fd62e-1439">atmcard</span></span>
- <span data-ttu-id="fd62e-1440">cartes de retrait</span><span class="sxs-lookup"><span data-stu-id="fd62e-1440">atm cards</span></span>
- <span data-ttu-id="fd62e-1441">retrait</span><span class="sxs-lookup"><span data-stu-id="fd62e-1441">atmcards</span></span>
- <span data-ttu-id="fd62e-1442">envoier</span><span class="sxs-lookup"><span data-stu-id="fd62e-1442">enroute</span></span>
- <span data-ttu-id="fd62e-1443">en route</span><span class="sxs-lookup"><span data-stu-id="fd62e-1443">en route</span></span>
- <span data-ttu-id="fd62e-1444">type de carte</span><span class="sxs-lookup"><span data-stu-id="fd62e-1444">card type</span></span>
- <span data-ttu-id="fd62e-1445">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="fd62e-1445">carte bancaire</span></span>
- <span data-ttu-id="fd62e-1446">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="fd62e-1446">carte de crédit</span></span>
- <span data-ttu-id="fd62e-1447">carte de credit</span><span class="sxs-lookup"><span data-stu-id="fd62e-1447">carte de credit</span></span>
- <span data-ttu-id="fd62e-1448">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="fd62e-1448">numéro de carte</span></span>
- <span data-ttu-id="fd62e-1449">numero de carte</span><span class="sxs-lookup"><span data-stu-id="fd62e-1449">numero de carte</span></span>
- <span data-ttu-id="fd62e-1450">nº de la carte</span><span class="sxs-lookup"><span data-stu-id="fd62e-1450">nº de la carte</span></span>
- <span data-ttu-id="fd62e-1451">nº de carte</span><span class="sxs-lookup"><span data-stu-id="fd62e-1451">nº de carte</span></span>
- <span data-ttu-id="fd62e-1452">kreditkarte</span><span class="sxs-lookup"><span data-stu-id="fd62e-1452">kreditkarte</span></span>
- <span data-ttu-id="fd62e-1453">karte</span><span class="sxs-lookup"><span data-stu-id="fd62e-1453">karte</span></span>
- <span data-ttu-id="fd62e-1454">karteninhaber</span><span class="sxs-lookup"><span data-stu-id="fd62e-1454">karteninhaber</span></span>
- <span data-ttu-id="fd62e-1455">karteninhabers</span><span class="sxs-lookup"><span data-stu-id="fd62e-1455">karteninhabers</span></span>
- <span data-ttu-id="fd62e-1456">kreditkarteninhaber</span><span class="sxs-lookup"><span data-stu-id="fd62e-1456">kreditkarteninhaber</span></span>
- <span data-ttu-id="fd62e-1457">kreditkarteninstitut</span><span class="sxs-lookup"><span data-stu-id="fd62e-1457">kreditkarteninstitut</span></span>
- <span data-ttu-id="fd62e-1458">kreditkartentyp</span><span class="sxs-lookup"><span data-stu-id="fd62e-1458">kreditkartentyp</span></span>
- <span data-ttu-id="fd62e-1459">eigentümername</span><span class="sxs-lookup"><span data-stu-id="fd62e-1459">eigentümername</span></span>
- <span data-ttu-id="fd62e-1460">kartennr</span><span class="sxs-lookup"><span data-stu-id="fd62e-1460">kartennr</span></span> 
- <span data-ttu-id="fd62e-1461">kartennummer</span><span class="sxs-lookup"><span data-stu-id="fd62e-1461">kartennummer</span></span>
- <span data-ttu-id="fd62e-1462">kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="fd62e-1462">kreditkartennummer</span></span>
- <span data-ttu-id="fd62e-1463">kreditkarten-nummer</span><span class="sxs-lookup"><span data-stu-id="fd62e-1463">kreditkarten-nummer</span></span>
- <span data-ttu-id="fd62e-1464">Carta di credito</span><span class="sxs-lookup"><span data-stu-id="fd62e-1464">carta di credito</span></span>
- <span data-ttu-id="fd62e-1465">Carta credito</span><span class="sxs-lookup"><span data-stu-id="fd62e-1465">carta credito</span></span>
- <span data-ttu-id="fd62e-1466">Carta</span><span class="sxs-lookup"><span data-stu-id="fd62e-1466">carta</span></span>
- <span data-ttu-id="fd62e-1467">n carta</span><span class="sxs-lookup"><span data-stu-id="fd62e-1467">n carta</span></span>
- <span data-ttu-id="fd62e-1468">Nr.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1468">nr.</span></span> <span data-ttu-id="fd62e-1469">Carta</span><span class="sxs-lookup"><span data-stu-id="fd62e-1469">carta</span></span>
- <span data-ttu-id="fd62e-1470">nr carta</span><span class="sxs-lookup"><span data-stu-id="fd62e-1470">nr carta</span></span>
- <span data-ttu-id="fd62e-1471">numero carta</span><span class="sxs-lookup"><span data-stu-id="fd62e-1471">numero carta</span></span>
- <span data-ttu-id="fd62e-1472">numero della carta</span><span class="sxs-lookup"><span data-stu-id="fd62e-1472">numero della carta</span></span>
- <span data-ttu-id="fd62e-1473">numero di carta</span><span class="sxs-lookup"><span data-stu-id="fd62e-1473">numero di carta</span></span>
- <span data-ttu-id="fd62e-1474">tarjeta credito</span><span class="sxs-lookup"><span data-stu-id="fd62e-1474">tarjeta credito</span></span>
- <span data-ttu-id="fd62e-1475">tarjeta de credito</span><span class="sxs-lookup"><span data-stu-id="fd62e-1475">tarjeta de credito</span></span>
- <span data-ttu-id="fd62e-1476">tarjeta crédito</span><span class="sxs-lookup"><span data-stu-id="fd62e-1476">tarjeta crédito</span></span>
- <span data-ttu-id="fd62e-1477">tarjeta de crédito</span><span class="sxs-lookup"><span data-stu-id="fd62e-1477">tarjeta de crédito</span></span>
- <span data-ttu-id="fd62e-1478">tarjeta de atm</span><span class="sxs-lookup"><span data-stu-id="fd62e-1478">tarjeta de atm</span></span>
- <span data-ttu-id="fd62e-1479">tarjeta atm</span><span class="sxs-lookup"><span data-stu-id="fd62e-1479">tarjeta atm</span></span>
- <span data-ttu-id="fd62e-1480">tarjeta debito</span><span class="sxs-lookup"><span data-stu-id="fd62e-1480">tarjeta debito</span></span>
- <span data-ttu-id="fd62e-1481">tarjeta de debito</span><span class="sxs-lookup"><span data-stu-id="fd62e-1481">tarjeta de debito</span></span>
- <span data-ttu-id="fd62e-1482">tarjeta débito</span><span class="sxs-lookup"><span data-stu-id="fd62e-1482">tarjeta débito</span></span>
- <span data-ttu-id="fd62e-1483">tarjeta de débito</span><span class="sxs-lookup"><span data-stu-id="fd62e-1483">tarjeta de débito</span></span>
- <span data-ttu-id="fd62e-1484">nº de tarjeta</span><span class="sxs-lookup"><span data-stu-id="fd62e-1484">nº de tarjeta</span></span>
- <span data-ttu-id="fd62e-1485">Nbre.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1485">no.</span></span> <span data-ttu-id="fd62e-1486">de tarjeta</span><span class="sxs-lookup"><span data-stu-id="fd62e-1486">de tarjeta</span></span>
- <span data-ttu-id="fd62e-1487">no de tarjeta</span><span class="sxs-lookup"><span data-stu-id="fd62e-1487">no de tarjeta</span></span>
- <span data-ttu-id="fd62e-1488">numero de tarjeta</span><span class="sxs-lookup"><span data-stu-id="fd62e-1488">numero de tarjeta</span></span>
- <span data-ttu-id="fd62e-1489">número de tarjeta</span><span class="sxs-lookup"><span data-stu-id="fd62e-1489">número de tarjeta</span></span>
- <span data-ttu-id="fd62e-1490">tarjeta no</span><span class="sxs-lookup"><span data-stu-id="fd62e-1490">tarjeta no</span></span>
- <span data-ttu-id="fd62e-1491">tarjetahabiente</span><span class="sxs-lookup"><span data-stu-id="fd62e-1491">tarjetahabiente</span></span>
- <span data-ttu-id="fd62e-1492">cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="fd62e-1492">cartão de crédito</span></span>
- <span data-ttu-id="fd62e-1493">cartão de credito</span><span class="sxs-lookup"><span data-stu-id="fd62e-1493">cartão de credito</span></span>
- <span data-ttu-id="fd62e-1494">cartao de crédito</span><span class="sxs-lookup"><span data-stu-id="fd62e-1494">cartao de crédito</span></span>
- <span data-ttu-id="fd62e-1495">cartao de credito</span><span class="sxs-lookup"><span data-stu-id="fd62e-1495">cartao de credito</span></span>
- <span data-ttu-id="fd62e-1496">cartão de débito</span><span class="sxs-lookup"><span data-stu-id="fd62e-1496">cartão de débito</span></span>
- <span data-ttu-id="fd62e-1497">cartao de débito</span><span class="sxs-lookup"><span data-stu-id="fd62e-1497">cartao de débito</span></span>
- <span data-ttu-id="fd62e-1498">cartão de debito</span><span class="sxs-lookup"><span data-stu-id="fd62e-1498">cartão de debito</span></span>
- <span data-ttu-id="fd62e-1499">cartao de debito</span><span class="sxs-lookup"><span data-stu-id="fd62e-1499">cartao de debito</span></span>
- <span data-ttu-id="fd62e-1500">débito automático</span><span class="sxs-lookup"><span data-stu-id="fd62e-1500">débito automático</span></span>
- <span data-ttu-id="fd62e-1501">debito automatico</span><span class="sxs-lookup"><span data-stu-id="fd62e-1501">debito automatico</span></span>
- <span data-ttu-id="fd62e-1502">número do cartão</span><span class="sxs-lookup"><span data-stu-id="fd62e-1502">número do cartão</span></span>
- <span data-ttu-id="fd62e-1503">numero do cartão</span><span class="sxs-lookup"><span data-stu-id="fd62e-1503">numero do cartão</span></span> 
- <span data-ttu-id="fd62e-1504">número do cartao</span><span class="sxs-lookup"><span data-stu-id="fd62e-1504">número do cartao</span></span>
- <span data-ttu-id="fd62e-1505">numero do cartao</span><span class="sxs-lookup"><span data-stu-id="fd62e-1505">numero do cartao</span></span>
- <span data-ttu-id="fd62e-1506">número de cartão</span><span class="sxs-lookup"><span data-stu-id="fd62e-1506">número de cartão</span></span>
- <span data-ttu-id="fd62e-1507">numero de cartão</span><span class="sxs-lookup"><span data-stu-id="fd62e-1507">numero de cartão</span></span>
- <span data-ttu-id="fd62e-1508">número de cartao</span><span class="sxs-lookup"><span data-stu-id="fd62e-1508">número de cartao</span></span>
- <span data-ttu-id="fd62e-1509">numero de cartao</span><span class="sxs-lookup"><span data-stu-id="fd62e-1509">numero de cartao</span></span>
- <span data-ttu-id="fd62e-1510">nº do cartão</span><span class="sxs-lookup"><span data-stu-id="fd62e-1510">nº do cartão</span></span>
- <span data-ttu-id="fd62e-1511">nº do cartao</span><span class="sxs-lookup"><span data-stu-id="fd62e-1511">nº do cartao</span></span>
- <span data-ttu-id="fd62e-1512">n º.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1512">nº.</span></span> <span data-ttu-id="fd62e-1513">do cartão</span><span class="sxs-lookup"><span data-stu-id="fd62e-1513">do cartão</span></span>
- <span data-ttu-id="fd62e-1514">no do cartão</span><span class="sxs-lookup"><span data-stu-id="fd62e-1514">no do cartão</span></span>
- <span data-ttu-id="fd62e-1515">no do cartao</span><span class="sxs-lookup"><span data-stu-id="fd62e-1515">no do cartao</span></span>
- <span data-ttu-id="fd62e-1516">Nbre.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1516">no.</span></span> <span data-ttu-id="fd62e-1517">do cartão</span><span class="sxs-lookup"><span data-stu-id="fd62e-1517">do cartão</span></span>
- <span data-ttu-id="fd62e-1518">Nbre.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1518">no.</span></span> <span data-ttu-id="fd62e-1519">do cartao</span><span class="sxs-lookup"><span data-stu-id="fd62e-1519">do cartao</span></span> 
   
## <a name="croatia-identity-card-number"></a><span data-ttu-id="fd62e-1520">	Numéro de carte d’identité Croatie</span><span class="sxs-lookup"><span data-stu-id="fd62e-1520">Croatia Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-1521">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-1521">Format</span></span>

<span data-ttu-id="fd62e-1522">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-1522">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-1523">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-1523">Pattern</span></span>

<span data-ttu-id="fd62e-1524">Neuf chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="fd62e-1524">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-1525">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-1525">Checksum</span></span>

<span data-ttu-id="fd62e-1526">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-1526">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-1527">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-1527">Definition</span></span>

<span data-ttu-id="fd62e-1528">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-1528">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-1529">La fonction Func_croatia_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1529">The function Func_croatia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-1530">Un mot clé figurant dans la liste Keyword_croatia_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1530">A keyword from Keyword_croatia_id_card is found.</span></span>

```xml
<!--Croatia Identity Card Number-->
<Entity id="ff12f884-c20a-4189-b185-34c8e7258d47" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_croatia_id_card"/>
     <Match idRef="Keyword_croatia_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fd62e-1531">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-1531">Keywords</span></span>

#### <a name="keyword_croatia_id_card"></a><span data-ttu-id="fd62e-1532">Keyword_croatia_id_card</span><span class="sxs-lookup"><span data-stu-id="fd62e-1532">Keyword_croatia_id_card</span></span>

- <span data-ttu-id="fd62e-1533">Croatian identity card</span><span class="sxs-lookup"><span data-stu-id="fd62e-1533">Croatian identity card</span></span>
- <span data-ttu-id="fd62e-1534">Osobna iskaznica</span><span class="sxs-lookup"><span data-stu-id="fd62e-1534">Osobna iskaznica</span></span>

   
## <a name="croatia-personal-identification-oib-number"></a><span data-ttu-id="fd62e-1535">	Numéro d’identification personnel (OIB) Croatie</span><span class="sxs-lookup"><span data-stu-id="fd62e-1535">Croatia Personal Identification (OIB) Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-1536">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-1536">Format</span></span>

<span data-ttu-id="fd62e-1537">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-1537">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-1538">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-1538">Pattern</span></span>

<span data-ttu-id="fd62e-1539">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="fd62e-1539">11 digits:</span></span>
- <span data-ttu-id="fd62e-1540">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-1540">10 digits</span></span> 
- <span data-ttu-id="fd62e-1541">Le chiffre final est un chiffre de contrôle aux fins de l’échange de données internationales, les lettres HR sont ajoutées avant les onze chiffres.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1541">Final digit is a check digit For the purposes of international data exchange, the letters HR are added preceding the eleven digits.</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-1542">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-1542">Checksum</span></span>

<span data-ttu-id="fd62e-1543">Oui</span><span class="sxs-lookup"><span data-stu-id="fd62e-1543">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-1544">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-1544">Definition</span></span>

<span data-ttu-id="fd62e-1545">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-1545">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-1546">La fonction Func_croatia_oib_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1546">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-1547">Un mot clé figurant dans la liste Keyword_croatia_oib_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1547">A keyword from Keyword_croatia_oib_number is found.</span></span>
- <span data-ttu-id="fd62e-1548">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1548">The checksum passes.</span></span>

<span data-ttu-id="fd62e-1549">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-1549">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-1550">La fonction Func_croatia_oib_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1550">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-1551">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1551">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-1552">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-1552">Keywords</span></span>

#### <a name="keyword_croatia_oib_number"></a><span data-ttu-id="fd62e-1553">Keyword_croatia_oib_number</span><span class="sxs-lookup"><span data-stu-id="fd62e-1553">Keyword_croatia_oib_number</span></span>

- <span data-ttu-id="fd62e-1554">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="fd62e-1554">Personal Identification Number</span></span>
- <span data-ttu-id="fd62e-1555">Osobni identifikacijski broj</span><span class="sxs-lookup"><span data-stu-id="fd62e-1555">Osobni identifikacijski broj</span></span> 
- <span data-ttu-id="fd62e-1556">OIB</span><span class="sxs-lookup"><span data-stu-id="fd62e-1556">OIB</span></span> 

   
## <a name="czech-personal-identity-number"></a><span data-ttu-id="fd62e-1557">Numéro d’identité personnelle tchèque</span><span class="sxs-lookup"><span data-stu-id="fd62e-1557">Czech Personal Identity Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-1558">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-1558">Format</span></span>

<span data-ttu-id="fd62e-1559">Neuf chiffres avec une barre oblique inverse facultative (ancien format) 10 chiffres avec une barre oblique facultative (nouveau format)</span><span class="sxs-lookup"><span data-stu-id="fd62e-1559">Nine digits with optional forward slash (old format) 10 digits with optional forward slash (new format)</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-1560">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-1560">Pattern</span></span>

<span data-ttu-id="fd62e-1561">Neuf chiffres (ancien format):</span><span class="sxs-lookup"><span data-stu-id="fd62e-1561">Nine digits (old format):</span></span>
- <span data-ttu-id="fd62e-1562">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-1562">Nine digits</span></span>

<span data-ttu-id="fd62e-1563">OR</span><span class="sxs-lookup"><span data-stu-id="fd62e-1563">OR</span></span>

- <span data-ttu-id="fd62e-1564">Six chiffres qui représentent la date de naissance</span><span class="sxs-lookup"><span data-stu-id="fd62e-1564">Six digits that represent date of birth</span></span>
- <span data-ttu-id="fd62e-1565">Une barre oblique </span><span class="sxs-lookup"><span data-stu-id="fd62e-1565">A forward slash</span></span>
- <span data-ttu-id="fd62e-1566">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-1566">Three digits</span></span>

<span data-ttu-id="fd62e-1567">10 chiffres (nouveau format):</span><span class="sxs-lookup"><span data-stu-id="fd62e-1567">10 digits (new format):</span></span>
- <span data-ttu-id="fd62e-1568">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-1568">10 digits</span></span>

<span data-ttu-id="fd62e-1569">OR</span><span class="sxs-lookup"><span data-stu-id="fd62e-1569">OR</span></span>

- <span data-ttu-id="fd62e-1570">Six chiffres qui représentent la date de naissance</span><span class="sxs-lookup"><span data-stu-id="fd62e-1570">Six digits that represent date of birth</span></span>
- <span data-ttu-id="fd62e-1571">Une barre oblique </span><span class="sxs-lookup"><span data-stu-id="fd62e-1571">A forward slash</span></span> 
- <span data-ttu-id="fd62e-1572">Quatre chiffres où le dernier chiffre est un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-1572">Four digits where last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-1573">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-1573">Checksum</span></span>

<span data-ttu-id="fd62e-1574">Oui</span><span class="sxs-lookup"><span data-stu-id="fd62e-1574">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-1575">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-1575">Definition</span></span>

<span data-ttu-id="fd62e-1576">Une stratégie DLP est sûre à 85% d’avoir détecté ce type d’informations sensibles si, dans une proximité de 300 caractères: la fonction Func_czech_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1576">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_czech_id_card finds content that matches the pattern.</span></span>
<span data-ttu-id="fd62e-1577">Un mot clé figurant dans la liste Keyword_czech_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1577">A keyword from Keyword_czech_id_card is found.</span></span>
<span data-ttu-id="fd62e-1578">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1578">The checksum passes.</span></span>

```xml
<!-- Czech Personal Identity Number -->
<Entity id="60c0725a-4eb6-455b-9dda-05d8a7396497"      patternsProximity="300" recommendedConfidence="85">
   <Pattern confidenceLevel="85">
      <IdMatch idRef="Func_czech_id_card" />
      <Match idRef="Keyword_czech_id_card" />
   </Pattern>
</Entity>
```
### <a name="keywords"></a><span data-ttu-id="fd62e-1579">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-1579">Keywords</span></span>

- <span data-ttu-id="fd62e-1580">Numéro d’identité personnelle tchèque</span><span class="sxs-lookup"><span data-stu-id="fd62e-1580">czech personal identity number</span></span>
- <span data-ttu-id="fd62e-1581">Rodné číslo</span><span class="sxs-lookup"><span data-stu-id="fd62e-1581">Rodné číslo</span></span>
   
## <a name="denmark-personal-identification-number"></a><span data-ttu-id="fd62e-1582">	Numéro d’identification personnel Danemark</span><span class="sxs-lookup"><span data-stu-id="fd62e-1582">Denmark Personal Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-1583">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-1583">Format</span></span>

<span data-ttu-id="fd62e-1584">10 chiffres contenant un trait d’union</span><span class="sxs-lookup"><span data-stu-id="fd62e-1584">10 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-1585">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-1585">Pattern</span></span>

<span data-ttu-id="fd62e-1586">10 chiffres :</span><span class="sxs-lookup"><span data-stu-id="fd62e-1586">10 digits:</span></span>
- <span data-ttu-id="fd62e-1587">Six chiffres au format JJMMAA qui correspondent à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="fd62e-1587">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="fd62e-1588">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="fd62e-1588">A hyphen</span></span> 
- <span data-ttu-id="fd62e-1589">Quatre chiffres où le dernier chiffre est un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-1589">Four digits where the final digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-1590">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-1590">Checksum</span></span>

<span data-ttu-id="fd62e-1591">Oui</span><span class="sxs-lookup"><span data-stu-id="fd62e-1591">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-1592">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-1592">Definition</span></span>

<span data-ttu-id="fd62e-1593">Une stratégie DLP est sûre à 75% d’avoir détecté ce type d’informations sensibles si, dans une proximité de 300 caractères: l’expression régulière Regex_denmark_id trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1593">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_denmark_id finds content that matches the pattern.</span></span>
<span data-ttu-id="fd62e-1594">Un mot clé figurant dans la liste Keyword_denmark_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1594">A keyword from Keyword_denmark_id is found.</span></span>
<span data-ttu-id="fd62e-1595">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1595">The checksum passes.</span></span>

```xml
<!-- Denmark Personal Identification Number -->
<Entity id="6c4f2fef-56e1-4c00-8093-88d7a01cf460" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_denmark_id"/>
     <Match idRef="Keyword_denmark_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fd62e-1596">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-1596">Keywords</span></span>

#### <a name="keyword_denmark_id"></a><span data-ttu-id="fd62e-1597">Keyword_denmark_id</span><span class="sxs-lookup"><span data-stu-id="fd62e-1597">Keyword_denmark_id</span></span>

- <span data-ttu-id="fd62e-1598">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="fd62e-1598">Personal Identification Number</span></span>
- <span data-ttu-id="fd62e-1599">CARDIO</span><span class="sxs-lookup"><span data-stu-id="fd62e-1599">CPR</span></span>
- <span data-ttu-id="fd62e-1600">Det Centrale Personregister</span><span class="sxs-lookup"><span data-stu-id="fd62e-1600">Det Centrale Personregister</span></span>
- <span data-ttu-id="fd62e-1601">Personnummer</span><span class="sxs-lookup"><span data-stu-id="fd62e-1601">Personnummer</span></span>
   
## <a name="drug-enforcement-agency-dea-number"></a><span data-ttu-id="fd62e-1602">Numéro de la Drug Enforcement Agency (DEA)</span><span class="sxs-lookup"><span data-stu-id="fd62e-1602">Drug Enforcement Agency (DEA) Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-1603">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-1603">Format</span></span>

<span data-ttu-id="fd62e-1604">Deux lettres suivies de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-1604">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-1605">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-1605">Pattern</span></span>

<span data-ttu-id="fd62e-1606">Le modèle doit inclure tous les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="fd62e-1606">Pattern must include all of the following:</span></span>
- <span data-ttu-id="fd62e-1607">Une lettre (ne respecte pas la casse) à partir de cet ensemble de lettres possibles : abcdefghjklmnprstux, qui est un code d’utilisateur enregistré</span><span class="sxs-lookup"><span data-stu-id="fd62e-1607">One letter (not case sensitive) from this set of possible letters: abcdefghjklmnprstux, which is a registrant code</span></span> 
- <span data-ttu-id="fd62e-1608">Une lettre (ne respecte pas la casse), qui est la première lettre du nom de l’utilisateur enregistré</span><span class="sxs-lookup"><span data-stu-id="fd62e-1608">One letter (not case sensitive), which is the first letter of the registrant's last name</span></span> 
- <span data-ttu-id="fd62e-1609">Sept chiffres, le dernier est le chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-1609">Seven digits, the last of which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-1610">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-1610">Checksum</span></span>

<span data-ttu-id="fd62e-1611">Oui</span><span class="sxs-lookup"><span data-stu-id="fd62e-1611">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-1612">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-1612">Definition</span></span>

<span data-ttu-id="fd62e-1613">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-1613">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-1614">La fonction Func_dea_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1614">The function Func_dea_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-1615">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1615">The checksum passes.</span></span>

```xml
<!-- DEA Number -->
<Entity id="9a5445ad-406e-43eb-8bd7-cac17ab6d0e4" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_dea_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fd62e-1616">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-1616">Keywords</span></span>

<span data-ttu-id="fd62e-1617">Aucun</span><span class="sxs-lookup"><span data-stu-id="fd62e-1617">None</span></span>

   
## <a name="eu-debit-card-number"></a><span data-ttu-id="fd62e-1618">Numéro de carte de débit Union européenne</span><span class="sxs-lookup"><span data-stu-id="fd62e-1618">EU Debit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-1619">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-1619">Format</span></span>

<span data-ttu-id="fd62e-1620">16 chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-1620">16 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-1621">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-1621">Pattern</span></span>

<span data-ttu-id="fd62e-1622">Modèle très complexe et puissant</span><span class="sxs-lookup"><span data-stu-id="fd62e-1622">Very complex and robust pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-1623">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-1623">Checksum</span></span>

<span data-ttu-id="fd62e-1624">Oui</span><span class="sxs-lookup"><span data-stu-id="fd62e-1624">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-1625">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-1625">Definition</span></span>

<span data-ttu-id="fd62e-1626">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-1626">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-1627">La fonction Func_eu_debit_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1627">The function Func_eu_debit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-1628">Au moins une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="fd62e-1628">At least one of the following is true:</span></span>
    - <span data-ttu-id="fd62e-1629">Un mot clé figurant dans la liste Keyword_eu_debit_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1629">A keyword from Keyword_eu_debit_card is found.</span></span>
    - <span data-ttu-id="fd62e-1630">Un mot clé figurant dans la liste Keyword_card_terms_dict est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1630">A keyword from Keyword_card_terms_dict is found.</span></span>
    - <span data-ttu-id="fd62e-1631">Un mot clé figurant dans la liste Keyword_card_security_terms_dict est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1631">A keyword from Keyword_card_security_terms_dict is found.</span></span>
    - <span data-ttu-id="fd62e-1632">Un mot clé figurant dans la liste Keyword_card_expiration_terms_dict est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1632">A keyword from Keyword_card_expiration_terms_dict is found.</span></span>
    - <span data-ttu-id="fd62e-1633">La fonction Func_expiration_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1633">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="fd62e-1634">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1634">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-1635">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-1635">Keywords</span></span>

#### <a name="keyword_eu_debit_card"></a><span data-ttu-id="fd62e-1636">Keyword_eu_debit_card</span><span class="sxs-lookup"><span data-stu-id="fd62e-1636">Keyword_eu_debit_card</span></span>

- <span data-ttu-id="fd62e-1637">numéro de compte</span><span class="sxs-lookup"><span data-stu-id="fd62e-1637">account number</span></span> 
- <span data-ttu-id="fd62e-1638">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="fd62e-1638">card number</span></span> 
- <span data-ttu-id="fd62e-1639">n° carte</span><span class="sxs-lookup"><span data-stu-id="fd62e-1639">card no.</span></span> 
- <span data-ttu-id="fd62e-1640">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="fd62e-1640">security number</span></span> 
- <span data-ttu-id="fd62e-1641">CC #</span><span class="sxs-lookup"><span data-stu-id="fd62e-1641">cc#</span></span> 

#### <a name="keyword_card_terms_dict"></a><span data-ttu-id="fd62e-1642">Keyword_card_terms_dict</span><span class="sxs-lookup"><span data-stu-id="fd62e-1642">Keyword_card_terms_dict</span></span>

- <span data-ttu-id="fd62e-1643">num de compte</span><span class="sxs-lookup"><span data-stu-id="fd62e-1643">acct nbr</span></span> 
- <span data-ttu-id="fd62e-1644">num de compte</span><span class="sxs-lookup"><span data-stu-id="fd62e-1644">acct num</span></span> 
- <span data-ttu-id="fd62e-1645">n° compte</span><span class="sxs-lookup"><span data-stu-id="fd62e-1645">acct no</span></span> 
- <span data-ttu-id="fd62e-1646">american express</span><span class="sxs-lookup"><span data-stu-id="fd62e-1646">american express</span></span> 
- <span data-ttu-id="fd62e-1647">americanexpress</span><span class="sxs-lookup"><span data-stu-id="fd62e-1647">americanexpress</span></span> 
- <span data-ttu-id="fd62e-1648">americano espresso</span><span class="sxs-lookup"><span data-stu-id="fd62e-1648">americano espresso</span></span> 
- <span data-ttu-id="fd62e-1649">American</span><span class="sxs-lookup"><span data-stu-id="fd62e-1649">amex</span></span> 
- <span data-ttu-id="fd62e-1650">carte de retrait</span><span class="sxs-lookup"><span data-stu-id="fd62e-1650">atm card</span></span> 
- <span data-ttu-id="fd62e-1651">cartes de retrait</span><span class="sxs-lookup"><span data-stu-id="fd62e-1651">atm cards</span></span> 
- <span data-ttu-id="fd62e-1652">atm kaart</span><span class="sxs-lookup"><span data-stu-id="fd62e-1652">atm kaart</span></span> 
- <span data-ttu-id="fd62e-1653">retrait</span><span class="sxs-lookup"><span data-stu-id="fd62e-1653">atmcard</span></span> 
- <span data-ttu-id="fd62e-1654">retrait</span><span class="sxs-lookup"><span data-stu-id="fd62e-1654">atmcards</span></span> 
- <span data-ttu-id="fd62e-1655">atmkaart</span><span class="sxs-lookup"><span data-stu-id="fd62e-1655">atmkaart</span></span> 
- <span data-ttu-id="fd62e-1656">atmkaarten</span><span class="sxs-lookup"><span data-stu-id="fd62e-1656">atmkaarten</span></span> 
- <span data-ttu-id="fd62e-1657">bancontact</span><span class="sxs-lookup"><span data-stu-id="fd62e-1657">bancontact</span></span> 
- <span data-ttu-id="fd62e-1658">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="fd62e-1658">bank card</span></span> 
- <span data-ttu-id="fd62e-1659">bankkaart</span><span class="sxs-lookup"><span data-stu-id="fd62e-1659">bankkaart</span></span> 
- <span data-ttu-id="fd62e-1660">titulaire de la carte</span><span class="sxs-lookup"><span data-stu-id="fd62e-1660">card holder</span></span> 
- <span data-ttu-id="fd62e-1661">titulaires de la carte</span><span class="sxs-lookup"><span data-stu-id="fd62e-1661">card holders</span></span> 
- <span data-ttu-id="fd62e-1662">num de carte</span><span class="sxs-lookup"><span data-stu-id="fd62e-1662">card num</span></span> 
- <span data-ttu-id="fd62e-1663">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="fd62e-1663">card number</span></span> 
- <span data-ttu-id="fd62e-1664">numéros de carte</span><span class="sxs-lookup"><span data-stu-id="fd62e-1664">card numbers</span></span> 
- <span data-ttu-id="fd62e-1665">type de carte</span><span class="sxs-lookup"><span data-stu-id="fd62e-1665">card type</span></span> 
- <span data-ttu-id="fd62e-1666">cardano numerico</span><span class="sxs-lookup"><span data-stu-id="fd62e-1666">cardano numerico</span></span> 
- <span data-ttu-id="fd62e-1667">titulaires</span><span class="sxs-lookup"><span data-stu-id="fd62e-1667">cardholder</span></span> 
- <span data-ttu-id="fd62e-1668">titulaires</span><span class="sxs-lookup"><span data-stu-id="fd62e-1668">cardholders</span></span> 
- <span data-ttu-id="fd62e-1669">carte</span><span class="sxs-lookup"><span data-stu-id="fd62e-1669">cardnumber</span></span> 
- <span data-ttu-id="fd62e-1670">carte</span><span class="sxs-lookup"><span data-stu-id="fd62e-1670">cardnumbers</span></span> 
- <span data-ttu-id="fd62e-1671">carta bianca</span><span class="sxs-lookup"><span data-stu-id="fd62e-1671">carta bianca</span></span> 
- <span data-ttu-id="fd62e-1672">Carta credito</span><span class="sxs-lookup"><span data-stu-id="fd62e-1672">carta credito</span></span> 
- <span data-ttu-id="fd62e-1673">Carta di credito</span><span class="sxs-lookup"><span data-stu-id="fd62e-1673">carta di credito</span></span> 
- <span data-ttu-id="fd62e-1674">cartao de credito</span><span class="sxs-lookup"><span data-stu-id="fd62e-1674">cartao de credito</span></span> 
- <span data-ttu-id="fd62e-1675">cartao de crédito</span><span class="sxs-lookup"><span data-stu-id="fd62e-1675">cartao de crédito</span></span> 
- <span data-ttu-id="fd62e-1676">cartao de debito</span><span class="sxs-lookup"><span data-stu-id="fd62e-1676">cartao de debito</span></span> 
- <span data-ttu-id="fd62e-1677">cartao de débito</span><span class="sxs-lookup"><span data-stu-id="fd62e-1677">cartao de débito</span></span> 
- <span data-ttu-id="fd62e-1678">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="fd62e-1678">carte bancaire</span></span> 
- <span data-ttu-id="fd62e-1679">carte blanche</span><span class="sxs-lookup"><span data-stu-id="fd62e-1679">carte blanche</span></span> 
- <span data-ttu-id="fd62e-1680">carte bleue</span><span class="sxs-lookup"><span data-stu-id="fd62e-1680">carte bleue</span></span> 
- <span data-ttu-id="fd62e-1681">carte de credit</span><span class="sxs-lookup"><span data-stu-id="fd62e-1681">carte de credit</span></span> 
- <span data-ttu-id="fd62e-1682">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="fd62e-1682">carte de crédit</span></span> 
- <span data-ttu-id="fd62e-1683">carte di credito</span><span class="sxs-lookup"><span data-stu-id="fd62e-1683">carte di credito</span></span> 
- <span data-ttu-id="fd62e-1684">carteblanche</span><span class="sxs-lookup"><span data-stu-id="fd62e-1684">carteblanche</span></span> 
- <span data-ttu-id="fd62e-1685">cartão de credito</span><span class="sxs-lookup"><span data-stu-id="fd62e-1685">cartão de credito</span></span> 
- <span data-ttu-id="fd62e-1686">cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="fd62e-1686">cartão de crédito</span></span> 
- <span data-ttu-id="fd62e-1687">cartão de debito</span><span class="sxs-lookup"><span data-stu-id="fd62e-1687">cartão de debito</span></span> 
- <span data-ttu-id="fd62e-1688">cartão de débito</span><span class="sxs-lookup"><span data-stu-id="fd62e-1688">cartão de débito</span></span> 
- <span data-ttu-id="fd62e-1689">cb</span><span class="sxs-lookup"><span data-stu-id="fd62e-1689">cb</span></span> 
- <span data-ttu-id="fd62e-1690">CCN</span><span class="sxs-lookup"><span data-stu-id="fd62e-1690">ccn</span></span> 
- <span data-ttu-id="fd62e-1691">carte de vérification</span><span class="sxs-lookup"><span data-stu-id="fd62e-1691">check card</span></span> 
- <span data-ttu-id="fd62e-1692">cartes de vérification</span><span class="sxs-lookup"><span data-stu-id="fd62e-1692">check cards</span></span> 
- <span data-ttu-id="fd62e-1693">carte</span><span class="sxs-lookup"><span data-stu-id="fd62e-1693">checkcard</span></span>
- <span data-ttu-id="fd62e-1694">cartes</span><span class="sxs-lookup"><span data-stu-id="fd62e-1694">checkcards</span></span> 
- <span data-ttu-id="fd62e-1695">chequekaart</span><span class="sxs-lookup"><span data-stu-id="fd62e-1695">chequekaart</span></span> 
- <span data-ttu-id="fd62e-1696">Cirrus</span><span class="sxs-lookup"><span data-stu-id="fd62e-1696">cirrus</span></span> 
- <span data-ttu-id="fd62e-1697">Cirrus-EDC-Maestro</span><span class="sxs-lookup"><span data-stu-id="fd62e-1697">cirrus-edc-maestro</span></span> 
- <span data-ttu-id="fd62e-1698">controlekaart</span><span class="sxs-lookup"><span data-stu-id="fd62e-1698">controlekaart</span></span> 
- <span data-ttu-id="fd62e-1699">controlekaarten</span><span class="sxs-lookup"><span data-stu-id="fd62e-1699">controlekaarten</span></span> 
- <span data-ttu-id="fd62e-1700">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="fd62e-1700">credit card</span></span> 
- <span data-ttu-id="fd62e-1701">cartes de crédit</span><span class="sxs-lookup"><span data-stu-id="fd62e-1701">credit cards</span></span> 
- <span data-ttu-id="fd62e-1702">CreditCard</span><span class="sxs-lookup"><span data-stu-id="fd62e-1702">creditcard</span></span> 
- <span data-ttu-id="fd62e-1703">crédit</span><span class="sxs-lookup"><span data-stu-id="fd62e-1703">creditcards</span></span> 
- <span data-ttu-id="fd62e-1704">debetkaart</span><span class="sxs-lookup"><span data-stu-id="fd62e-1704">debetkaart</span></span> 
- <span data-ttu-id="fd62e-1705">debetkaarten</span><span class="sxs-lookup"><span data-stu-id="fd62e-1705">debetkaarten</span></span> 
- <span data-ttu-id="fd62e-1706">carte de débit</span><span class="sxs-lookup"><span data-stu-id="fd62e-1706">debit card</span></span> 
- <span data-ttu-id="fd62e-1707">cartes de débit</span><span class="sxs-lookup"><span data-stu-id="fd62e-1707">debit cards</span></span> 
- <span data-ttu-id="fd62e-1708">débit</span><span class="sxs-lookup"><span data-stu-id="fd62e-1708">debitcard</span></span> 
- <span data-ttu-id="fd62e-1709">débit</span><span class="sxs-lookup"><span data-stu-id="fd62e-1709">debitcards</span></span> 
- <span data-ttu-id="fd62e-1710">debito automatico</span><span class="sxs-lookup"><span data-stu-id="fd62e-1710">debito automatico</span></span> 
- <span data-ttu-id="fd62e-1711">diners club</span><span class="sxs-lookup"><span data-stu-id="fd62e-1711">diners club</span></span> 
- <span data-ttu-id="fd62e-1712">dinersclub</span><span class="sxs-lookup"><span data-stu-id="fd62e-1712">dinersclub</span></span> 
- <span data-ttu-id="fd62e-1713">connaissance</span><span class="sxs-lookup"><span data-stu-id="fd62e-1713">discover</span></span> 
- <span data-ttu-id="fd62e-1714">discover card</span><span class="sxs-lookup"><span data-stu-id="fd62e-1714">discover card</span></span> 
- <span data-ttu-id="fd62e-1715">discover cards</span><span class="sxs-lookup"><span data-stu-id="fd62e-1715">discover cards</span></span> 
- <span data-ttu-id="fd62e-1716">discovercard</span><span class="sxs-lookup"><span data-stu-id="fd62e-1716">discovercard</span></span> 
- <span data-ttu-id="fd62e-1717">discovercards</span><span class="sxs-lookup"><span data-stu-id="fd62e-1717">discovercards</span></span> 
- <span data-ttu-id="fd62e-1718">débito automático</span><span class="sxs-lookup"><span data-stu-id="fd62e-1718">débito automático</span></span>
- <span data-ttu-id="fd62e-1719">EDC</span><span class="sxs-lookup"><span data-stu-id="fd62e-1719">edc</span></span> 
- <span data-ttu-id="fd62e-1720">eigentümername</span><span class="sxs-lookup"><span data-stu-id="fd62e-1720">eigentümername</span></span> 
- <span data-ttu-id="fd62e-1721">carte de crédit européenne</span><span class="sxs-lookup"><span data-stu-id="fd62e-1721">european debit card</span></span> 
- <span data-ttu-id="fd62e-1722">hoofdkaart</span><span class="sxs-lookup"><span data-stu-id="fd62e-1722">hoofdkaart</span></span> 
- <span data-ttu-id="fd62e-1723">hoofdkaarten</span><span class="sxs-lookup"><span data-stu-id="fd62e-1723">hoofdkaarten</span></span> 
- <span data-ttu-id="fd62e-1724">in viaggio</span><span class="sxs-lookup"><span data-stu-id="fd62e-1724">in viaggio</span></span> 
- <span data-ttu-id="fd62e-1725">japanese card bureau</span><span class="sxs-lookup"><span data-stu-id="fd62e-1725">japanese card bureau</span></span> 
- <span data-ttu-id="fd62e-1726">japanse kaartdienst</span><span class="sxs-lookup"><span data-stu-id="fd62e-1726">japanse kaartdienst</span></span> 
- <span data-ttu-id="fd62e-1727">JCB</span><span class="sxs-lookup"><span data-stu-id="fd62e-1727">jcb</span></span> 
- <span data-ttu-id="fd62e-1728">kaart</span><span class="sxs-lookup"><span data-stu-id="fd62e-1728">kaart</span></span> 
- <span data-ttu-id="fd62e-1729">kaart num</span><span class="sxs-lookup"><span data-stu-id="fd62e-1729">kaart num</span></span> 
- <span data-ttu-id="fd62e-1730">kaartaantal</span><span class="sxs-lookup"><span data-stu-id="fd62e-1730">kaartaantal</span></span> 
- <span data-ttu-id="fd62e-1731">kaartaantallen</span><span class="sxs-lookup"><span data-stu-id="fd62e-1731">kaartaantallen</span></span> 
- <span data-ttu-id="fd62e-1732">kaarthouder</span><span class="sxs-lookup"><span data-stu-id="fd62e-1732">kaarthouder</span></span> 
- <span data-ttu-id="fd62e-1733">kaarthouders</span><span class="sxs-lookup"><span data-stu-id="fd62e-1733">kaarthouders</span></span> 
- <span data-ttu-id="fd62e-1734">karte</span><span class="sxs-lookup"><span data-stu-id="fd62e-1734">karte</span></span>  
- <span data-ttu-id="fd62e-1735">karteninhaber</span><span class="sxs-lookup"><span data-stu-id="fd62e-1735">karteninhaber</span></span> 
- <span data-ttu-id="fd62e-1736">karteninhabers</span><span class="sxs-lookup"><span data-stu-id="fd62e-1736">karteninhabers</span></span>
- <span data-ttu-id="fd62e-1737">kartennr</span><span class="sxs-lookup"><span data-stu-id="fd62e-1737">kartennr</span></span> 
- <span data-ttu-id="fd62e-1738">kartennummer</span><span class="sxs-lookup"><span data-stu-id="fd62e-1738">kartennummer</span></span> 
- <span data-ttu-id="fd62e-1739">kreditkarte</span><span class="sxs-lookup"><span data-stu-id="fd62e-1739">kreditkarte</span></span> 
- <span data-ttu-id="fd62e-1740">kreditkarten-nummer</span><span class="sxs-lookup"><span data-stu-id="fd62e-1740">kreditkarten-nummer</span></span> 
- <span data-ttu-id="fd62e-1741">kreditkarteninhaber</span><span class="sxs-lookup"><span data-stu-id="fd62e-1741">kreditkarteninhaber</span></span> 
- <span data-ttu-id="fd62e-1742">kreditkarteninstitut</span><span class="sxs-lookup"><span data-stu-id="fd62e-1742">kreditkarteninstitut</span></span> 
- <span data-ttu-id="fd62e-1743">kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="fd62e-1743">kreditkartennummer</span></span> 
- <span data-ttu-id="fd62e-1744">kreditkartentyp</span><span class="sxs-lookup"><span data-stu-id="fd62e-1744">kreditkartentyp</span></span> 
- <span data-ttu-id="fd62e-1745">sonne</span><span class="sxs-lookup"><span data-stu-id="fd62e-1745">maestro</span></span> 
- <span data-ttu-id="fd62e-1746">master card</span><span class="sxs-lookup"><span data-stu-id="fd62e-1746">master card</span></span> 
- <span data-ttu-id="fd62e-1747">master cards</span><span class="sxs-lookup"><span data-stu-id="fd62e-1747">master cards</span></span> 
- <span data-ttu-id="fd62e-1748">MasterCard</span><span class="sxs-lookup"><span data-stu-id="fd62e-1748">mastercard</span></span> 
- <span data-ttu-id="fd62e-1749">MasterCard</span><span class="sxs-lookup"><span data-stu-id="fd62e-1749">mastercards</span></span> 
- <span data-ttu-id="fd62e-1750">McDonald</span><span class="sxs-lookup"><span data-stu-id="fd62e-1750">mc</span></span> 
- <span data-ttu-id="fd62e-1751">mister cash</span><span class="sxs-lookup"><span data-stu-id="fd62e-1751">mister cash</span></span> 
- <span data-ttu-id="fd62e-1752">n carta</span><span class="sxs-lookup"><span data-stu-id="fd62e-1752">n carta</span></span> 
- <span data-ttu-id="fd62e-1753">Carta</span><span class="sxs-lookup"><span data-stu-id="fd62e-1753">carta</span></span> 
- <span data-ttu-id="fd62e-1754">no de tarjeta</span><span class="sxs-lookup"><span data-stu-id="fd62e-1754">no de tarjeta</span></span> 
- <span data-ttu-id="fd62e-1755">no do cartao</span><span class="sxs-lookup"><span data-stu-id="fd62e-1755">no do cartao</span></span> 
- <span data-ttu-id="fd62e-1756">no do cartão</span><span class="sxs-lookup"><span data-stu-id="fd62e-1756">no do cartão</span></span> 
- <span data-ttu-id="fd62e-1757">Nbre.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1757">no.</span></span> <span data-ttu-id="fd62e-1758">de tarjeta</span><span class="sxs-lookup"><span data-stu-id="fd62e-1758">de tarjeta</span></span> 
- <span data-ttu-id="fd62e-1759">Nbre.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1759">no.</span></span> <span data-ttu-id="fd62e-1760">do cartao</span><span class="sxs-lookup"><span data-stu-id="fd62e-1760">do cartao</span></span> 
- <span data-ttu-id="fd62e-1761">Nbre.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1761">no.</span></span> <span data-ttu-id="fd62e-1762">do cartão</span><span class="sxs-lookup"><span data-stu-id="fd62e-1762">do cartão</span></span> 
- <span data-ttu-id="fd62e-1763">nr carta</span><span class="sxs-lookup"><span data-stu-id="fd62e-1763">nr carta</span></span> 
- <span data-ttu-id="fd62e-1764">Nr.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1764">nr.</span></span> <span data-ttu-id="fd62e-1765">Carta</span><span class="sxs-lookup"><span data-stu-id="fd62e-1765">carta</span></span> 
- <span data-ttu-id="fd62e-1766">numeri di scheda</span><span class="sxs-lookup"><span data-stu-id="fd62e-1766">numeri di scheda</span></span> 
- <span data-ttu-id="fd62e-1767">numero carta</span><span class="sxs-lookup"><span data-stu-id="fd62e-1767">numero carta</span></span> 
- <span data-ttu-id="fd62e-1768">numero de cartao</span><span class="sxs-lookup"><span data-stu-id="fd62e-1768">numero de cartao</span></span> 
- <span data-ttu-id="fd62e-1769">numero de carte</span><span class="sxs-lookup"><span data-stu-id="fd62e-1769">numero de carte</span></span> 
- <span data-ttu-id="fd62e-1770">numero de cartão</span><span class="sxs-lookup"><span data-stu-id="fd62e-1770">numero de cartão</span></span> 
- <span data-ttu-id="fd62e-1771">numero de tarjeta</span><span class="sxs-lookup"><span data-stu-id="fd62e-1771">numero de tarjeta</span></span>
- <span data-ttu-id="fd62e-1772">numero della carta</span><span class="sxs-lookup"><span data-stu-id="fd62e-1772">numero della carta</span></span> 
- <span data-ttu-id="fd62e-1773">numero di carta</span><span class="sxs-lookup"><span data-stu-id="fd62e-1773">numero di carta</span></span> 
- <span data-ttu-id="fd62e-1774">numero di scheda</span><span class="sxs-lookup"><span data-stu-id="fd62e-1774">numero di scheda</span></span> 
- <span data-ttu-id="fd62e-1775">numero do cartao</span><span class="sxs-lookup"><span data-stu-id="fd62e-1775">numero do cartao</span></span> 
- <span data-ttu-id="fd62e-1776">numero do cartão</span><span class="sxs-lookup"><span data-stu-id="fd62e-1776">numero do cartão</span></span> 
- <span data-ttu-id="fd62e-1777">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="fd62e-1777">numéro de carte</span></span> 
- <span data-ttu-id="fd62e-1778">nº carta</span><span class="sxs-lookup"><span data-stu-id="fd62e-1778">nº carta</span></span> 
- <span data-ttu-id="fd62e-1779">nº de carte</span><span class="sxs-lookup"><span data-stu-id="fd62e-1779">nº de carte</span></span> 
- <span data-ttu-id="fd62e-1780">nº de la carte</span><span class="sxs-lookup"><span data-stu-id="fd62e-1780">nº de la carte</span></span> 
- <span data-ttu-id="fd62e-1781">nº de tarjeta</span><span class="sxs-lookup"><span data-stu-id="fd62e-1781">nº de tarjeta</span></span> 
- <span data-ttu-id="fd62e-1782">nº do cartao</span><span class="sxs-lookup"><span data-stu-id="fd62e-1782">nº do cartao</span></span> 
- <span data-ttu-id="fd62e-1783">nº do cartão</span><span class="sxs-lookup"><span data-stu-id="fd62e-1783">nº do cartão</span></span> 
- <span data-ttu-id="fd62e-1784">n º.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1784">nº.</span></span> <span data-ttu-id="fd62e-1785">do cartão</span><span class="sxs-lookup"><span data-stu-id="fd62e-1785">do cartão</span></span> 
- <span data-ttu-id="fd62e-1786">número de cartao</span><span class="sxs-lookup"><span data-stu-id="fd62e-1786">número de cartao</span></span> 
- <span data-ttu-id="fd62e-1787">número de cartão</span><span class="sxs-lookup"><span data-stu-id="fd62e-1787">número de cartão</span></span> 
- <span data-ttu-id="fd62e-1788">número de tarjeta</span><span class="sxs-lookup"><span data-stu-id="fd62e-1788">número de tarjeta</span></span> 
- <span data-ttu-id="fd62e-1789">número do cartao</span><span class="sxs-lookup"><span data-stu-id="fd62e-1789">número do cartao</span></span> 
- <span data-ttu-id="fd62e-1790">scheda dell’assegno</span><span class="sxs-lookup"><span data-stu-id="fd62e-1790">scheda dell'assegno</span></span> 
- <span data-ttu-id="fd62e-1791">scheda dell’atmosfera</span><span class="sxs-lookup"><span data-stu-id="fd62e-1791">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="fd62e-1792">scheda dell’atmosfera</span><span class="sxs-lookup"><span data-stu-id="fd62e-1792">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="fd62e-1793">scheda della banca</span><span class="sxs-lookup"><span data-stu-id="fd62e-1793">scheda della banca</span></span> 
- <span data-ttu-id="fd62e-1794">scheda di controllo</span><span class="sxs-lookup"><span data-stu-id="fd62e-1794">scheda di controllo</span></span> 
- <span data-ttu-id="fd62e-1795">scheda di debito</span><span class="sxs-lookup"><span data-stu-id="fd62e-1795">scheda di debito</span></span> 
- <span data-ttu-id="fd62e-1796">scheda matrice</span><span class="sxs-lookup"><span data-stu-id="fd62e-1796">scheda matrice</span></span> 
- <span data-ttu-id="fd62e-1797">schede dell’atmosfera</span><span class="sxs-lookup"><span data-stu-id="fd62e-1797">schede dell'atmosfera</span></span> 
- <span data-ttu-id="fd62e-1798">schede di controllo</span><span class="sxs-lookup"><span data-stu-id="fd62e-1798">schede di controllo</span></span> 
- <span data-ttu-id="fd62e-1799">schede di debito</span><span class="sxs-lookup"><span data-stu-id="fd62e-1799">schede di debito</span></span> 
- <span data-ttu-id="fd62e-1800">schede matrici</span><span class="sxs-lookup"><span data-stu-id="fd62e-1800">schede matrici</span></span> 
- <span data-ttu-id="fd62e-1801">scoprono la scheda</span><span class="sxs-lookup"><span data-stu-id="fd62e-1801">scoprono la scheda</span></span> 
- <span data-ttu-id="fd62e-1802">scoprono le schede</span><span class="sxs-lookup"><span data-stu-id="fd62e-1802">scoprono le schede</span></span> 
- <span data-ttu-id="fd62e-1803">tracteur</span><span class="sxs-lookup"><span data-stu-id="fd62e-1803">solo</span></span> 
- <span data-ttu-id="fd62e-1804">supporti di scheda</span><span class="sxs-lookup"><span data-stu-id="fd62e-1804">supporti di scheda</span></span> 
- <span data-ttu-id="fd62e-1805">supporto di scheda</span><span class="sxs-lookup"><span data-stu-id="fd62e-1805">supporto di scheda</span></span> 
- <span data-ttu-id="fd62e-1806">accéder</span><span class="sxs-lookup"><span data-stu-id="fd62e-1806">switch</span></span> 
- <span data-ttu-id="fd62e-1807">tarjeta atm</span><span class="sxs-lookup"><span data-stu-id="fd62e-1807">tarjeta atm</span></span> 
- <span data-ttu-id="fd62e-1808">tarjeta credito</span><span class="sxs-lookup"><span data-stu-id="fd62e-1808">tarjeta credito</span></span> 
- <span data-ttu-id="fd62e-1809">tarjeta de atm</span><span class="sxs-lookup"><span data-stu-id="fd62e-1809">tarjeta de atm</span></span> 
- <span data-ttu-id="fd62e-1810">tarjeta de credito</span><span class="sxs-lookup"><span data-stu-id="fd62e-1810">tarjeta de credito</span></span> 
- <span data-ttu-id="fd62e-1811">tarjeta de debito</span><span class="sxs-lookup"><span data-stu-id="fd62e-1811">tarjeta de debito</span></span> 
- <span data-ttu-id="fd62e-1812">tarjeta debito</span><span class="sxs-lookup"><span data-stu-id="fd62e-1812">tarjeta debito</span></span> 
- <span data-ttu-id="fd62e-1813">tarjeta no</span><span class="sxs-lookup"><span data-stu-id="fd62e-1813">tarjeta no</span></span>
- <span data-ttu-id="fd62e-1814">tarjetahabiente</span><span class="sxs-lookup"><span data-stu-id="fd62e-1814">tarjetahabiente</span></span> 
- <span data-ttu-id="fd62e-1815">tipo della scheda</span><span class="sxs-lookup"><span data-stu-id="fd62e-1815">tipo della scheda</span></span> 
- <span data-ttu-id="fd62e-1816">ufficio giapponese della</span><span class="sxs-lookup"><span data-stu-id="fd62e-1816">ufficio giapponese della</span></span> 
- <span data-ttu-id="fd62e-1817">scheda</span><span class="sxs-lookup"><span data-stu-id="fd62e-1817">scheda</span></span> 
- <span data-ttu-id="fd62e-1818">v pay</span><span class="sxs-lookup"><span data-stu-id="fd62e-1818">v pay</span></span> 
- <span data-ttu-id="fd62e-1819">v-Pay</span><span class="sxs-lookup"><span data-stu-id="fd62e-1819">v-pay</span></span> 
- <span data-ttu-id="fd62e-1820">délivrance</span><span class="sxs-lookup"><span data-stu-id="fd62e-1820">visa</span></span> 
- <span data-ttu-id="fd62e-1821">visa plus</span><span class="sxs-lookup"><span data-stu-id="fd62e-1821">visa plus</span></span> 
- <span data-ttu-id="fd62e-1822">visa electron</span><span class="sxs-lookup"><span data-stu-id="fd62e-1822">visa electron</span></span> 
- <span data-ttu-id="fd62e-1823">visto</span><span class="sxs-lookup"><span data-stu-id="fd62e-1823">visto</span></span> 
- <span data-ttu-id="fd62e-1824">visum</span><span class="sxs-lookup"><span data-stu-id="fd62e-1824">visum</span></span> 
- <span data-ttu-id="fd62e-1825">vpay</span><span class="sxs-lookup"><span data-stu-id="fd62e-1825">vpay</span></span>   

#### <a name="keyword_card_security_terms_dict"></a><span data-ttu-id="fd62e-1826">Keyword_card_security_terms_dict</span><span class="sxs-lookup"><span data-stu-id="fd62e-1826">Keyword_card_security_terms_dict</span></span>

- <span data-ttu-id="fd62e-1827">numéro d’identification de la carte</span><span class="sxs-lookup"><span data-stu-id="fd62e-1827">card identification number</span></span>
- <span data-ttu-id="fd62e-1828">vérification de la carte</span><span class="sxs-lookup"><span data-stu-id="fd62e-1828">card verification</span></span> 
- <span data-ttu-id="fd62e-1829">cardi la verifica</span><span class="sxs-lookup"><span data-stu-id="fd62e-1829">cardi la verifica</span></span> 
- <span data-ttu-id="fd62e-1830">nic</span><span class="sxs-lookup"><span data-stu-id="fd62e-1830">cid</span></span> 
- <span data-ttu-id="fd62e-1831">cod seg</span><span class="sxs-lookup"><span data-stu-id="fd62e-1831">cod seg</span></span> 
- <span data-ttu-id="fd62e-1832">cod seguranca</span><span class="sxs-lookup"><span data-stu-id="fd62e-1832">cod seguranca</span></span> 
- <span data-ttu-id="fd62e-1833">cod segurança</span><span class="sxs-lookup"><span data-stu-id="fd62e-1833">cod segurança</span></span> 
- <span data-ttu-id="fd62e-1834">cod sicurezza</span><span class="sxs-lookup"><span data-stu-id="fd62e-1834">cod sicurezza</span></span> 
- <span data-ttu-id="fd62e-1835">contre.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1835">cod.</span></span> <span data-ttu-id="fd62e-1836">SEG</span><span class="sxs-lookup"><span data-stu-id="fd62e-1836">seg</span></span> 
- <span data-ttu-id="fd62e-1837">contre.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1837">cod.</span></span> <span data-ttu-id="fd62e-1838">seguranca</span><span class="sxs-lookup"><span data-stu-id="fd62e-1838">seguranca</span></span> 
- <span data-ttu-id="fd62e-1839">contre.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1839">cod.</span></span> <span data-ttu-id="fd62e-1840">segurança</span><span class="sxs-lookup"><span data-stu-id="fd62e-1840">segurança</span></span> 
- <span data-ttu-id="fd62e-1841">contre.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1841">cod.</span></span> <span data-ttu-id="fd62e-1842">sicurezza</span><span class="sxs-lookup"><span data-stu-id="fd62e-1842">sicurezza</span></span> 
- <span data-ttu-id="fd62e-1843">codice di sicurezza</span><span class="sxs-lookup"><span data-stu-id="fd62e-1843">codice di sicurezza</span></span> 
- <span data-ttu-id="fd62e-1844">codice di verifica</span><span class="sxs-lookup"><span data-stu-id="fd62e-1844">codice di verifica</span></span> 
- <span data-ttu-id="fd62e-1845">codigo</span><span class="sxs-lookup"><span data-stu-id="fd62e-1845">codigo</span></span> 
- <span data-ttu-id="fd62e-1846">codigo de seguranca</span><span class="sxs-lookup"><span data-stu-id="fd62e-1846">codigo de seguranca</span></span> 
- <span data-ttu-id="fd62e-1847">codigo de segurança</span><span class="sxs-lookup"><span data-stu-id="fd62e-1847">codigo de segurança</span></span> 
- <span data-ttu-id="fd62e-1848">crittogramma</span><span class="sxs-lookup"><span data-stu-id="fd62e-1848">crittogramma</span></span> 
- <span data-ttu-id="fd62e-1849">cryptogram</span><span class="sxs-lookup"><span data-stu-id="fd62e-1849">cryptogram</span></span> 
- <span data-ttu-id="fd62e-1850">cryptogramme</span><span class="sxs-lookup"><span data-stu-id="fd62e-1850">cryptogramme</span></span> 
- <span data-ttu-id="fd62e-1851">cv2</span><span class="sxs-lookup"><span data-stu-id="fd62e-1851">cv2</span></span> 
- <span data-ttu-id="fd62e-1852">lâche</span><span class="sxs-lookup"><span data-stu-id="fd62e-1852">cvc</span></span> 
- <span data-ttu-id="fd62e-1853">cvc2</span><span class="sxs-lookup"><span data-stu-id="fd62e-1853">cvc2</span></span> 
- <span data-ttu-id="fd62e-1854">cryptogramme</span><span class="sxs-lookup"><span data-stu-id="fd62e-1854">cvn</span></span> 
- <span data-ttu-id="fd62e-1855">cvv</span><span class="sxs-lookup"><span data-stu-id="fd62e-1855">cvv</span></span> 
- <span data-ttu-id="fd62e-1856">cvv2</span><span class="sxs-lookup"><span data-stu-id="fd62e-1856">cvv2</span></span> 
- <span data-ttu-id="fd62e-1857">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="fd62e-1857">cód seguranca</span></span> 
- <span data-ttu-id="fd62e-1858">cód segurança</span><span class="sxs-lookup"><span data-stu-id="fd62e-1858">cód segurança</span></span> 
- <span data-ttu-id="fd62e-1859">cód.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1859">cód.</span></span> <span data-ttu-id="fd62e-1860">seguranca</span><span class="sxs-lookup"><span data-stu-id="fd62e-1860">seguranca</span></span> 
- <span data-ttu-id="fd62e-1861">cód.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1861">cód.</span></span> <span data-ttu-id="fd62e-1862">segurança</span><span class="sxs-lookup"><span data-stu-id="fd62e-1862">segurança</span></span> 
- <span data-ttu-id="fd62e-1863">código</span><span class="sxs-lookup"><span data-stu-id="fd62e-1863">código</span></span> 
- <span data-ttu-id="fd62e-1864">código de seguranca</span><span class="sxs-lookup"><span data-stu-id="fd62e-1864">código de seguranca</span></span> 
- <span data-ttu-id="fd62e-1865">código de segurança</span><span class="sxs-lookup"><span data-stu-id="fd62e-1865">código de segurança</span></span> 
- <span data-ttu-id="fd62e-1866">de kaart controle</span><span class="sxs-lookup"><span data-stu-id="fd62e-1866">de kaart controle</span></span> 
- <span data-ttu-id="fd62e-1867">geeft nr suit</span><span class="sxs-lookup"><span data-stu-id="fd62e-1867">geeft nr uit</span></span> 
- <span data-ttu-id="fd62e-1868">n° d’émission</span><span class="sxs-lookup"><span data-stu-id="fd62e-1868">issue no</span></span> 
- <span data-ttu-id="fd62e-1869">numéro d’émission</span><span class="sxs-lookup"><span data-stu-id="fd62e-1869">issue number</span></span> 
- <span data-ttu-id="fd62e-1870">kaartidentificatienummer</span><span class="sxs-lookup"><span data-stu-id="fd62e-1870">kaartidentificatienummer</span></span> 
- <span data-ttu-id="fd62e-1871">kreditkartenprufnummer</span><span class="sxs-lookup"><span data-stu-id="fd62e-1871">kreditkartenprufnummer</span></span> 
- <span data-ttu-id="fd62e-1872">kreditkartenprüfnummer</span><span class="sxs-lookup"><span data-stu-id="fd62e-1872">kreditkartenprüfnummer</span></span> 
- <span data-ttu-id="fd62e-1873">kwestieaantal</span><span class="sxs-lookup"><span data-stu-id="fd62e-1873">kwestieaantal</span></span> 
- <span data-ttu-id="fd62e-1874">Nbre.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1874">no.</span></span> <span data-ttu-id="fd62e-1875">dell'edizione</span><span class="sxs-lookup"><span data-stu-id="fd62e-1875">dell'edizione</span></span> 
- <span data-ttu-id="fd62e-1876">Nbre.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1876">no.</span></span> <span data-ttu-id="fd62e-1877">di sicurezza</span><span class="sxs-lookup"><span data-stu-id="fd62e-1877">di sicurezza</span></span> 
- <span data-ttu-id="fd62e-1878">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="fd62e-1878">numero de securite</span></span> 
- <span data-ttu-id="fd62e-1879">numero de verificacao</span><span class="sxs-lookup"><span data-stu-id="fd62e-1879">numero de verificacao</span></span> 
- <span data-ttu-id="fd62e-1880">numero dell’edizione</span><span class="sxs-lookup"><span data-stu-id="fd62e-1880">numero dell'edizione</span></span> 
- <span data-ttu-id="fd62e-1881">numero di identificazione della</span><span class="sxs-lookup"><span data-stu-id="fd62e-1881">numero di identificazione della</span></span> 
- <span data-ttu-id="fd62e-1882">scheda</span><span class="sxs-lookup"><span data-stu-id="fd62e-1882">scheda</span></span> 
- <span data-ttu-id="fd62e-1883">numero di sicurezza</span><span class="sxs-lookup"><span data-stu-id="fd62e-1883">numero di sicurezza</span></span> 
- <span data-ttu-id="fd62e-1884">numero van veiligheid</span><span class="sxs-lookup"><span data-stu-id="fd62e-1884">numero van veiligheid</span></span> 
- <span data-ttu-id="fd62e-1885">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="fd62e-1885">numéro de sécurité</span></span> 
- <span data-ttu-id="fd62e-1886">nº autorizzazione</span><span class="sxs-lookup"><span data-stu-id="fd62e-1886">nº autorizzazione</span></span> 
- <span data-ttu-id="fd62e-1887">número de verificação</span><span class="sxs-lookup"><span data-stu-id="fd62e-1887">número de verificação</span></span> 
- <span data-ttu-id="fd62e-1888">perno il blocco</span><span class="sxs-lookup"><span data-stu-id="fd62e-1888">perno il blocco</span></span> 
- <span data-ttu-id="fd62e-1889">pin block</span><span class="sxs-lookup"><span data-stu-id="fd62e-1889">pin block</span></span> 
- <span data-ttu-id="fd62e-1890">prufziffer</span><span class="sxs-lookup"><span data-stu-id="fd62e-1890">prufziffer</span></span> 
- <span data-ttu-id="fd62e-1891">prüfziffer</span><span class="sxs-lookup"><span data-stu-id="fd62e-1891">prüfziffer</span></span> 
- <span data-ttu-id="fd62e-1892">code de sécurité</span><span class="sxs-lookup"><span data-stu-id="fd62e-1892">security code</span></span> 
- <span data-ttu-id="fd62e-1893">n° de sécurité</span><span class="sxs-lookup"><span data-stu-id="fd62e-1893">security no</span></span> 
- <span data-ttu-id="fd62e-1894">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="fd62e-1894">security number</span></span> 
- <span data-ttu-id="fd62e-1895">sicherheits kode</span><span class="sxs-lookup"><span data-stu-id="fd62e-1895">sicherheits kode</span></span> 
- <span data-ttu-id="fd62e-1896">sicherheitscode</span><span class="sxs-lookup"><span data-stu-id="fd62e-1896">sicherheitscode</span></span> 
- <span data-ttu-id="fd62e-1897">sicherheitsnummer</span><span class="sxs-lookup"><span data-stu-id="fd62e-1897">sicherheitsnummer</span></span> 
- <span data-ttu-id="fd62e-1898">speldblok</span><span class="sxs-lookup"><span data-stu-id="fd62e-1898">speldblok</span></span> 
- <span data-ttu-id="fd62e-1899">veiligheid nr</span><span class="sxs-lookup"><span data-stu-id="fd62e-1899">veiligheid nr</span></span> 
- <span data-ttu-id="fd62e-1900">veiligheidsaantal</span><span class="sxs-lookup"><span data-stu-id="fd62e-1900">veiligheidsaantal</span></span> 
- <span data-ttu-id="fd62e-1901">veiligheidscode</span><span class="sxs-lookup"><span data-stu-id="fd62e-1901">veiligheidscode</span></span> 
- <span data-ttu-id="fd62e-1902">veiligheidsnummer</span><span class="sxs-lookup"><span data-stu-id="fd62e-1902">veiligheidsnummer</span></span> 
- <span data-ttu-id="fd62e-1903">verfalldatum</span><span class="sxs-lookup"><span data-stu-id="fd62e-1903">verfalldatum</span></span> 

#### <a name="keyword_card_expiration_terms_dict"></a><span data-ttu-id="fd62e-1904">Keyword_card_expiration_terms_dict</span><span class="sxs-lookup"><span data-stu-id="fd62e-1904">Keyword_card_expiration_terms_dict</span></span>

- <span data-ttu-id="fd62e-1905">ablauf</span><span class="sxs-lookup"><span data-stu-id="fd62e-1905">ablauf</span></span> 
- <span data-ttu-id="fd62e-1906">data de expiracao</span><span class="sxs-lookup"><span data-stu-id="fd62e-1906">data de expiracao</span></span> 
- <span data-ttu-id="fd62e-1907">data de expiração</span><span class="sxs-lookup"><span data-stu-id="fd62e-1907">data de expiração</span></span> 
- <span data-ttu-id="fd62e-1908">data del exp</span><span class="sxs-lookup"><span data-stu-id="fd62e-1908">data del exp</span></span> 
- <span data-ttu-id="fd62e-1909">data di exp</span><span class="sxs-lookup"><span data-stu-id="fd62e-1909">data di exp</span></span> 
- <span data-ttu-id="fd62e-1910">data di scadenza</span><span class="sxs-lookup"><span data-stu-id="fd62e-1910">data di scadenza</span></span> 
- <span data-ttu-id="fd62e-1911">data em que expira</span><span class="sxs-lookup"><span data-stu-id="fd62e-1911">data em que expira</span></span> 
- <span data-ttu-id="fd62e-1912">data scad</span><span class="sxs-lookup"><span data-stu-id="fd62e-1912">data scad</span></span> 
- <span data-ttu-id="fd62e-1913">data scadenza</span><span class="sxs-lookup"><span data-stu-id="fd62e-1913">data scadenza</span></span> 
- <span data-ttu-id="fd62e-1914">date de validité</span><span class="sxs-lookup"><span data-stu-id="fd62e-1914">date de validité</span></span> 
- <span data-ttu-id="fd62e-1915">datum afloop</span><span class="sxs-lookup"><span data-stu-id="fd62e-1915">datum afloop</span></span> 
- <span data-ttu-id="fd62e-1916">datum van exp</span><span class="sxs-lookup"><span data-stu-id="fd62e-1916">datum van exp</span></span> 
- <span data-ttu-id="fd62e-1917">de afloop</span><span class="sxs-lookup"><span data-stu-id="fd62e-1917">de afloop</span></span> 
- <span data-ttu-id="fd62e-1918">espira</span><span class="sxs-lookup"><span data-stu-id="fd62e-1918">espira</span></span> 
- <span data-ttu-id="fd62e-1919">espira</span><span class="sxs-lookup"><span data-stu-id="fd62e-1919">espira</span></span> 
- <span data-ttu-id="fd62e-1920">date d’exp</span><span class="sxs-lookup"><span data-stu-id="fd62e-1920">exp date</span></span> 
- <span data-ttu-id="fd62e-1921">exp datum</span><span class="sxs-lookup"><span data-stu-id="fd62e-1921">exp datum</span></span> 
- <span data-ttu-id="fd62e-1922">pire</span><span class="sxs-lookup"><span data-stu-id="fd62e-1922">expiration</span></span> 
- <span data-ttu-id="fd62e-1923">expiration</span><span class="sxs-lookup"><span data-stu-id="fd62e-1923">expire</span></span> 
- <span data-ttu-id="fd62e-1924">expire</span><span class="sxs-lookup"><span data-stu-id="fd62e-1924">expires</span></span> 
- <span data-ttu-id="fd62e-1925">expiration</span><span class="sxs-lookup"><span data-stu-id="fd62e-1925">expiry</span></span> 
- <span data-ttu-id="fd62e-1926">fecha de expiracion</span><span class="sxs-lookup"><span data-stu-id="fd62e-1926">fecha de expiracion</span></span> 
- <span data-ttu-id="fd62e-1927">fecha de venc</span><span class="sxs-lookup"><span data-stu-id="fd62e-1927">fecha de venc</span></span> 
- <span data-ttu-id="fd62e-1928">gultig bis</span><span class="sxs-lookup"><span data-stu-id="fd62e-1928">gultig bis</span></span> 
- <span data-ttu-id="fd62e-1929">gultigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="fd62e-1929">gultigkeitsdatum</span></span> 
- <span data-ttu-id="fd62e-1930">gültig bis</span><span class="sxs-lookup"><span data-stu-id="fd62e-1930">gültig bis</span></span> 
- <span data-ttu-id="fd62e-1931">gültigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="fd62e-1931">gültigkeitsdatum</span></span> 
- <span data-ttu-id="fd62e-1932">la scadenza</span><span class="sxs-lookup"><span data-stu-id="fd62e-1932">la scadenza</span></span> 
- <span data-ttu-id="fd62e-1933">scadenza</span><span class="sxs-lookup"><span data-stu-id="fd62e-1933">scadenza</span></span> 
- <span data-ttu-id="fd62e-1934">valable</span><span class="sxs-lookup"><span data-stu-id="fd62e-1934">valable</span></span> 
- <span data-ttu-id="fd62e-1935">validade</span><span class="sxs-lookup"><span data-stu-id="fd62e-1935">validade</span></span> 
- <span data-ttu-id="fd62e-1936">valido hasta</span><span class="sxs-lookup"><span data-stu-id="fd62e-1936">valido hasta</span></span> 
- <span data-ttu-id="fd62e-1937">valorisation</span><span class="sxs-lookup"><span data-stu-id="fd62e-1937">valor</span></span> 
- <span data-ttu-id="fd62e-1938">venc</span><span class="sxs-lookup"><span data-stu-id="fd62e-1938">venc</span></span> 
- <span data-ttu-id="fd62e-1939">vencimento</span><span class="sxs-lookup"><span data-stu-id="fd62e-1939">vencimento</span></span> 
- <span data-ttu-id="fd62e-1940">vencimiento</span><span class="sxs-lookup"><span data-stu-id="fd62e-1940">vencimiento</span></span> 
- <span data-ttu-id="fd62e-1941">verloopt</span><span class="sxs-lookup"><span data-stu-id="fd62e-1941">verloopt</span></span> 
- <span data-ttu-id="fd62e-1942">vervaldag</span><span class="sxs-lookup"><span data-stu-id="fd62e-1942">vervaldag</span></span> 
- <span data-ttu-id="fd62e-1943">vervaldatum</span><span class="sxs-lookup"><span data-stu-id="fd62e-1943">vervaldatum</span></span> 
- <span data-ttu-id="fd62e-1944">vto</span><span class="sxs-lookup"><span data-stu-id="fd62e-1944">vto</span></span> 
- <span data-ttu-id="fd62e-1945">válido hasta</span><span class="sxs-lookup"><span data-stu-id="fd62e-1945">válido hasta</span></span> 
   
## <a name="eu-drivers-license-number"></a><span data-ttu-id="fd62e-1946">Numéro de permis de conduire de l’UE</span><span class="sxs-lookup"><span data-stu-id="fd62e-1946">EU Driver's License Number</span></span>

<span data-ttu-id="fd62e-1947">Pour en savoir plus, consultez [la rubrique informations sensibles sur le numéro de permis de conduire du pilote de l’UE](eu-driver-s-license-number.md).</span><span class="sxs-lookup"><span data-stu-id="fd62e-1947">To learn more, see [EU Driver's License Number sensitive information type](eu-driver-s-license-number.md).</span></span>
  
## <a name="eu-national-identification-number"></a><span data-ttu-id="fd62e-1948">Numéro d’identification nationale de l’UE</span><span class="sxs-lookup"><span data-stu-id="fd62e-1948">EU National Identification Number</span></span>

<span data-ttu-id="fd62e-1949">Pour en savoir plus, consultez la rubrique [informations sensibles du numéro d’identification national](eu-national-identification-number.md)de l’UE.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1949">To learn more, see [EU National Identification Number sensitive information type](eu-national-identification-number.md).</span></span>
  
## <a name="eu-passport-number"></a><span data-ttu-id="fd62e-1950">Numéro de passeport UE</span><span class="sxs-lookup"><span data-stu-id="fd62e-1950">EU Passport Number</span></span>

<span data-ttu-id="fd62e-1951">Pour en savoir plus, consultez la rubrique [type d’informations sensibles du numéro de passeport européen](eu-passport-number.md).</span><span class="sxs-lookup"><span data-stu-id="fd62e-1951">To learn more, see [EU Passport Number sensitive information type](eu-passport-number.md).</span></span>
  
## <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="fd62e-1952">Numéro de sécurité sociale de l’UE ou ID équivalent</span><span class="sxs-lookup"><span data-stu-id="fd62e-1952">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="fd62e-1953">Pour en savoir plus, consultez la rubrique [numéro de sécurité sociale de l’UE ou type d’informations sensibles ID équivalent](eu-social-security-number-or-equivalent-id.md).</span><span class="sxs-lookup"><span data-stu-id="fd62e-1953">To learn more, see [EU Social Security Number or Equivalent ID sensitive information type](eu-social-security-number-or-equivalent-id.md).</span></span>
  
## <a name="eu-tax-identification-number"></a><span data-ttu-id="fd62e-1954">Numéro d’identification fiscale de l’UE</span><span class="sxs-lookup"><span data-stu-id="fd62e-1954">EU Tax Identification Number</span></span>

<span data-ttu-id="fd62e-1955">Pour en savoir plus, consultez la rubrique [euro Tax identification number sensitive type information](eu-tax-identification-number.md).</span><span class="sxs-lookup"><span data-stu-id="fd62e-1955">To learn more, see [EU Tax Identification Number sensitive information type](eu-tax-identification-number.md).</span></span>
  
## <a name="finland-national-id"></a><span data-ttu-id="fd62e-1956">ID national finlandais</span><span class="sxs-lookup"><span data-stu-id="fd62e-1956">Finland National ID</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-1957">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-1957">Format</span></span>

<span data-ttu-id="fd62e-1958">Six chiffres plus un caractère indiquant un siècle plus trois chiffres plus un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-1958">Six digits plus a character indicating a century plus three digits plus a check digit</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-1959">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-1959">Pattern</span></span>

<span data-ttu-id="fd62e-1960">Le modèle doit inclure tous les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="fd62e-1960">Pattern must include all of the following:</span></span>
- <span data-ttu-id="fd62e-1961">Six chiffres au format JJMMAA qui représentent la date de naissance</span><span class="sxs-lookup"><span data-stu-id="fd62e-1961">Six digits in the format format DDMMYY which are a date of birth</span></span> 
- <span data-ttu-id="fd62e-1962">Marqueur de siècle (soit « - », « + » ou « a »)</span><span class="sxs-lookup"><span data-stu-id="fd62e-1962">Century marker (either '-', '+' or 'a')</span></span> 
- <span data-ttu-id="fd62e-1963">Numéro d’identification personnel à trois chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-1963">Three-digit personal identification number</span></span> 
- <span data-ttu-id="fd62e-1964">Un chiffre ou une lettre (ne respectant pas la casse) de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-1964">A digit or letter (case insensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-1965">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-1965">Checksum</span></span>

<span data-ttu-id="fd62e-1966">Oui</span><span class="sxs-lookup"><span data-stu-id="fd62e-1966">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-1967">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-1967">Definition</span></span>

<span data-ttu-id="fd62e-1968">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-1968">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-1969">La fonction Func_finnish_national_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1969">The function Func_finnish_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-1970">Un mot clé figurant dans la liste Keyword_finnish_national_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1970">A keyword from Keyword_finnish_national_id is found.</span></span>
- <span data-ttu-id="fd62e-1971">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1971">The checksum passes.</span></span>

```xml
<!-- Finnish National ID-->
<Entity id="338FD995-4CB5-4F87-AD35-79BD1DD926C1" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finnish_national_id" />
          <Match idRef="Keyword_finnish_national_id" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fd62e-1972">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-1972">Keywords</span></span>

- <span data-ttu-id="fd62e-1973">Keyword_finnish_national_id</span><span class="sxs-lookup"><span data-stu-id="fd62e-1973">Keyword_finnish_national_id</span></span>
- <span data-ttu-id="fd62e-1974">Sosiaaliturvatunnus</span><span class="sxs-lookup"><span data-stu-id="fd62e-1974">Sosiaaliturvatunnus</span></span>
- <span data-ttu-id="fd62e-1975">SOTU Henkilötunnus HETU</span><span class="sxs-lookup"><span data-stu-id="fd62e-1975">SOTU Henkilötunnus HETU</span></span>
- <span data-ttu-id="fd62e-1976">Personbeteckning</span><span class="sxs-lookup"><span data-stu-id="fd62e-1976">Personbeteckning</span></span>
- <span data-ttu-id="fd62e-1977">Personnummer</span><span class="sxs-lookup"><span data-stu-id="fd62e-1977">Personnummer</span></span>
   
## <a name="finland-passport-number"></a><span data-ttu-id="fd62e-1978">Numéro de passeport Finlande</span><span class="sxs-lookup"><span data-stu-id="fd62e-1978">Finland Passport Number</span></span>

<span data-ttu-id="fd62e-1979">Combinaison de format de neuf lettres et chiffres combinaison de neuf lettres et chiffres: deux lettres (ne respectant pas la casse) sept chiffres somme de contrôle no la stratégie DLP est de 75% en certitude qu’elle a détecté ce type d’informations sensibles si, dans un proximité de 300 caractères: l’expression régulière Regex_finland_passport_number trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1979">Format Combination of nine letters and digits Pattern Combination of nine letters and digits: Two letters (not case sensitive) Seven digits Checksum No Definition A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_finland_passport_number finds content that matches the pattern.</span></span>
<span data-ttu-id="fd62e-1980">Un mot clé figurant dans la liste Keyword_finland_passport_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1980">A keyword from Keyword_finland_passport_number is found.</span></span>
<!-- Finland Passport Number -->
<span data-ttu-id="fd62e-1981"><Entity id="d1685ac3-1d3a-40f8-8198-32ef5669c7a5" recommendedConfidence="75" patternsProximity="300"> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_finland_passport_number"/> <Match idRef="Keyword_finland_passport_number"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="fd62e-1981"></span></span>
<span data-ttu-id="fd62e-1982">Mots clés Keyword_finland_passport_number Passport passes</span><span class="sxs-lookup"><span data-stu-id="fd62e-1982">Keywords Keyword_finland_passport_number Passport Passi</span></span>
   
## <a name="france-drivers-license-number"></a><span data-ttu-id="fd62e-1983">Numéro de permis de conduire France</span><span class="sxs-lookup"><span data-stu-id="fd62e-1983">France Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-1984">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-1984">Format</span></span>

<span data-ttu-id="fd62e-1985">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-1985">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-1986">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-1986">Pattern</span></span>

<span data-ttu-id="fd62e-1987">12 chiffres avec validation pour écarter les modèles similaires, comme les numéros de téléphone français</span><span class="sxs-lookup"><span data-stu-id="fd62e-1987">12 digits with validation to discount similar patterns such as French telephone numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-1988">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-1988">Checksum</span></span>

<span data-ttu-id="fd62e-1989">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-1989">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-1990">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-1990">Definition</span></span>

<span data-ttu-id="fd62e-1991">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-1991">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-1992">La fonction Func_french_drivers_license trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1992">The function Func_french_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-1993">Au moins une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="fd62e-1993">At least one of the following is true:</span></span>
- <span data-ttu-id="fd62e-1994">Un mot clé figurant dans la liste Keyword_french_drivers_license est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1994">A keyword from Keyword_french_drivers_license is found.</span></span>
- <span data-ttu-id="fd62e-1995">La fonction Func_eu_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="fd62e-1995">The function Func_eu_date finds a date in the right date format.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-1996">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-1996">Keywords</span></span>

#### <a name="keyword_french_drivers_license"></a><span data-ttu-id="fd62e-1997">Keyword_french_drivers_license</span><span class="sxs-lookup"><span data-stu-id="fd62e-1997">Keyword_french_drivers_license</span></span>

- <span data-ttu-id="fd62e-1998">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-1998">drivers licence</span></span>
- <span data-ttu-id="fd62e-1999">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-1999">drivers license</span></span>
- <span data-ttu-id="fd62e-2000">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2000">driving licence</span></span>
- <span data-ttu-id="fd62e-2001">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2001">driving license</span></span>
- <span data-ttu-id="fd62e-2002">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2002">permis de conduire</span></span>
- <span data-ttu-id="fd62e-2003">numéro de permis</span><span class="sxs-lookup"><span data-stu-id="fd62e-2003">licence number</span></span>
- <span data-ttu-id="fd62e-2004">numéro de permis</span><span class="sxs-lookup"><span data-stu-id="fd62e-2004">license number</span></span>
- <span data-ttu-id="fd62e-2005">numéros de permis</span><span class="sxs-lookup"><span data-stu-id="fd62e-2005">licence numbers</span></span>
- <span data-ttu-id="fd62e-2006">numéros de permis</span><span class="sxs-lookup"><span data-stu-id="fd62e-2006">license numbers</span></span>

## <a name="france-national-id-card-cni"></a><span data-ttu-id="fd62e-2007">Carte nationale d’identité (CNI) France</span><span class="sxs-lookup"><span data-stu-id="fd62e-2007">France National ID Card (CNI)</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-2008">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-2008">Format</span></span>

<span data-ttu-id="fd62e-2009">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2009">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-2010">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2010">Pattern</span></span>

<span data-ttu-id="fd62e-2011">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2011">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-2012">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2012">Checksum</span></span>

<span data-ttu-id="fd62e-2013">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-2013">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-2014">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-2014">Definition</span></span>

<span data-ttu-id="fd62e-2015">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2015">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-2016">L’expression régulière Regex_france_cni trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2016">The regular expression Regex_france_cni finds content that matches the pattern.</span></span>

```xml
<!-- France CNI -->
<Entity id="f741ac74-1bc0-4665-b69b-f0c7f927c0c4" patternsProximity="300" recommendedConfidence="65">
  <Pattern confidenceLevel="65">
        <IdMatch idRef="Regex_france_cni" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fd62e-2017">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-2017">Keywords</span></span>

<span data-ttu-id="fd62e-2018">Aucun</span><span class="sxs-lookup"><span data-stu-id="fd62e-2018">None</span></span>
   
## <a name="france-passport-number"></a><span data-ttu-id="fd62e-2019">Numéro de passeport France</span><span class="sxs-lookup"><span data-stu-id="fd62e-2019">France Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-2020">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-2020">Format</span></span>

<span data-ttu-id="fd62e-2021">Neuf chiffres et lettres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2021">Nine digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-2022">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2022">Pattern</span></span>

<span data-ttu-id="fd62e-2023">Neuf chiffres et lettres :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2023">Nine digits and letters:</span></span>
- <span data-ttu-id="fd62e-2024">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2024">Two digits</span></span> 
- <span data-ttu-id="fd62e-2025">Deux lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="fd62e-2025">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="fd62e-2026">Cinq chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2026">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-2027">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2027">Checksum</span></span>

<span data-ttu-id="fd62e-2028">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-2028">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-2029">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-2029">Definition</span></span>

<span data-ttu-id="fd62e-2030">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2030">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-2031">La fonction Func_fr_passport trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2031">The function Func_fr_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-2032">Un mot clé figurant dans la liste Keyword_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2032">A keyword from Keyword_passport is found.</span></span>

```xml
<!-- France Passport Number -->
<Entity id="3008b884-8c8c-4cd8-a289-99f34fc7ff5d" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_fr_passport" />
        <Match idRef="Keyword_passport" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fd62e-2033">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-2033">Keywords</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="fd62e-2034">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="fd62e-2034">Keyword_passport</span></span>

- <span data-ttu-id="fd62e-2035">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="fd62e-2035">Passport Number</span></span>
- <span data-ttu-id="fd62e-2036">N° de passeport</span><span class="sxs-lookup"><span data-stu-id="fd62e-2036">Passport No</span></span>
- <span data-ttu-id="fd62e-2037"># Passeport</span><span class="sxs-lookup"><span data-stu-id="fd62e-2037">Passport #</span></span>
- <span data-ttu-id="fd62e-2038">Tel #</span><span class="sxs-lookup"><span data-stu-id="fd62e-2038">Passport#</span></span>
- <span data-ttu-id="fd62e-2039">PassportID</span><span class="sxs-lookup"><span data-stu-id="fd62e-2039">PassportID</span></span>
- <span data-ttu-id="fd62e-2040">N ° passeport</span><span class="sxs-lookup"><span data-stu-id="fd62e-2040">Passportno</span></span>
- <span data-ttu-id="fd62e-2041">passportnumber</span><span class="sxs-lookup"><span data-stu-id="fd62e-2041">passportnumber</span></span>
- <span data-ttu-id="fd62e-2042">パスポート</span><span class="sxs-lookup"><span data-stu-id="fd62e-2042">パスポート</span></span>
- <span data-ttu-id="fd62e-2043">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="fd62e-2043">パスポート番号</span></span>
- <span data-ttu-id="fd62e-2044">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="fd62e-2044">パスポートのNum</span></span>
- <span data-ttu-id="fd62e-2045">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="fd62e-2045">パスポート ＃</span></span> 
- <span data-ttu-id="fd62e-2046">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="fd62e-2046">Numéro de passeport</span></span>
- <span data-ttu-id="fd62e-2047">Passeport n°</span><span class="sxs-lookup"><span data-stu-id="fd62e-2047">Passeport n °</span></span>
- <span data-ttu-id="fd62e-2048">Passeport numéro</span><span class="sxs-lookup"><span data-stu-id="fd62e-2048">Passeport Non</span></span>
- <span data-ttu-id="fd62e-2049"># Passeport</span><span class="sxs-lookup"><span data-stu-id="fd62e-2049">Passeport #</span></span>
- <span data-ttu-id="fd62e-2050">Passeport #</span><span class="sxs-lookup"><span data-stu-id="fd62e-2050">Passeport#</span></span>
- <span data-ttu-id="fd62e-2051">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="fd62e-2051">PasseportNon</span></span>
- <span data-ttu-id="fd62e-2052">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="fd62e-2052">Passeportn °</span></span>

      
## <a name="france-social-security-number-insee"></a><span data-ttu-id="fd62e-2053">Numéro de sécurité sociale (INSEE) France</span><span class="sxs-lookup"><span data-stu-id="fd62e-2053">France Social Security Number (INSEE)</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-2054">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-2054">Format</span></span>

<span data-ttu-id="fd62e-2055">15 chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2055">15 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-2056">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2056">Pattern</span></span>

<span data-ttu-id="fd62e-2057">Doit correspondre à l’un des deux modèles suivants :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2057">Must match one of two patterns:</span></span>
- <span data-ttu-id="fd62e-2058">13 chiffres suivis d’un espace suivi de deux chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2058">13 digits followed by a space followed by two digits</span></span><br/>
<span data-ttu-id="fd62e-2059">ou</span><span class="sxs-lookup"><span data-stu-id="fd62e-2059">or</span></span>
- <span data-ttu-id="fd62e-2060">15 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="fd62e-2060">15 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-2061">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2061">Checksum</span></span>

<span data-ttu-id="fd62e-2062">Oui</span><span class="sxs-lookup"><span data-stu-id="fd62e-2062">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-2063">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-2063">Definition</span></span>

<span data-ttu-id="fd62e-2064">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 95 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2064">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-2065">La fonction Func_french_insee ou Func_fr_insee trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2065">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-2066">Un mot clé figurant dans la liste Keyword_fr_insee est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2066">A keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="fd62e-2067">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2067">The checksum passes.</span></span>

<span data-ttu-id="fd62e-2068">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2068">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-2069">La fonction Func_french_insee ou Func_fr_insee trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2069">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-2070">Aucun mot clé figurant dans la liste Keyword_fr_insee n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2070">No keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="fd62e-2071">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2071">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-2072">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-2072">Keywords</span></span>

#### <a name="keyword_fr_insee"></a><span data-ttu-id="fd62e-2073">Keyword_fr_insee</span><span class="sxs-lookup"><span data-stu-id="fd62e-2073">Keyword_fr_insee</span></span>

- <span data-ttu-id="fd62e-2074">INSEE</span><span class="sxs-lookup"><span data-stu-id="fd62e-2074">insee</span></span>
- <span data-ttu-id="fd62e-2075">securité sociale</span><span class="sxs-lookup"><span data-stu-id="fd62e-2075">securité sociale</span></span>
- <span data-ttu-id="fd62e-2076">securite sociale</span><span class="sxs-lookup"><span data-stu-id="fd62e-2076">securite sociale</span></span>
- <span data-ttu-id="fd62e-2077">id national</span><span class="sxs-lookup"><span data-stu-id="fd62e-2077">national id</span></span>
- <span data-ttu-id="fd62e-2078">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="fd62e-2078">national identification</span></span>
- <span data-ttu-id="fd62e-2079">numéro d’identité</span><span class="sxs-lookup"><span data-stu-id="fd62e-2079">numéro d'identité</span></span>
- <span data-ttu-id="fd62e-2080">n° d’identité</span><span class="sxs-lookup"><span data-stu-id="fd62e-2080">no d'identité</span></span>
- <span data-ttu-id="fd62e-2081">Nbre.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2081">no.</span></span> <span data-ttu-id="fd62e-2082">d’identité</span><span class="sxs-lookup"><span data-stu-id="fd62e-2082">d'identité</span></span>
- <span data-ttu-id="fd62e-2083">numéro d’identité</span><span class="sxs-lookup"><span data-stu-id="fd62e-2083">numero d'identite</span></span>
- <span data-ttu-id="fd62e-2084">n° d’identité</span><span class="sxs-lookup"><span data-stu-id="fd62e-2084">no d'identite</span></span>
- <span data-ttu-id="fd62e-2085">Nbre.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2085">no.</span></span> <span data-ttu-id="fd62e-2086">d’identite</span><span class="sxs-lookup"><span data-stu-id="fd62e-2086">d'identite</span></span>
- <span data-ttu-id="fd62e-2087">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="fd62e-2087">social security number</span></span>
- <span data-ttu-id="fd62e-2088">code de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="fd62e-2088">social security code</span></span>
- <span data-ttu-id="fd62e-2089">numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="fd62e-2089">social insurance number</span></span>
- <span data-ttu-id="fd62e-2090">le numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="fd62e-2090">le numéro d'identification nationale</span></span>
- <span data-ttu-id="fd62e-2091">d’identité nationale</span><span class="sxs-lookup"><span data-stu-id="fd62e-2091">d'identité nationale</span></span>
- <span data-ttu-id="fd62e-2092">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="fd62e-2092">numéro de sécurité sociale</span></span>
- <span data-ttu-id="fd62e-2093">le code de la sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="fd62e-2093">le code de la sécurité sociale</span></span>
- <span data-ttu-id="fd62e-2094">numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="fd62e-2094">numéro d'assurance sociale</span></span>
- <span data-ttu-id="fd62e-2095">numéro de sécu</span><span class="sxs-lookup"><span data-stu-id="fd62e-2095">numéro de sécu</span></span>
- <span data-ttu-id="fd62e-2096">code sécu</span><span class="sxs-lookup"><span data-stu-id="fd62e-2096">code sécu</span></span> 
   
## <a name="german-drivers-license-number"></a><span data-ttu-id="fd62e-2097">Numéro de permis de conduire Allemagne</span><span class="sxs-lookup"><span data-stu-id="fd62e-2097">German Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-2098">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-2098">Format</span></span>

<span data-ttu-id="fd62e-2099">Combinaison de 11 chiffres et lettres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2099">Combination of 11 digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-2100">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2100">Pattern</span></span>

<span data-ttu-id="fd62e-2101">11 chiffres et lettres (ne respectent pas la casse) :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2101">11 digits and letters (not case sensitive):</span></span>
- <span data-ttu-id="fd62e-2102">Un chiffre ou une lettre</span><span class="sxs-lookup"><span data-stu-id="fd62e-2102">A digit or letter</span></span> 
- <span data-ttu-id="fd62e-2103">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2103">Two digits</span></span> 
- <span data-ttu-id="fd62e-2104">Six chiffres ou lettres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2104">Six digits or letters</span></span> 
- <span data-ttu-id="fd62e-2105">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="fd62e-2105">A digit</span></span> 
- <span data-ttu-id="fd62e-2106">Un chiffre ou une lettre</span><span class="sxs-lookup"><span data-stu-id="fd62e-2106">A digit or letter</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-2107">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2107">Checksum</span></span>

<span data-ttu-id="fd62e-2108">Oui</span><span class="sxs-lookup"><span data-stu-id="fd62e-2108">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-2109">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-2109">Definition</span></span>

<span data-ttu-id="fd62e-2110">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2110">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-2111">La fonction Func_german_drivers_license trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2111">The function Func_german_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-2112">Au moins une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2112">At least one of the following is true:</span></span>
    - <span data-ttu-id="fd62e-2113">Un mot clé figurant dans la liste Keyword_german_drivers_license_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2113">A keyword from Keyword_german_drivers_license_number is found.</span></span>
    - <span data-ttu-id="fd62e-2114">Un mot clé figurant dans la liste Keyword_german_drivers_license_collaborative est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2114">A keyword from Keyword_german_drivers_license_collaborative is found.</span></span>
    - <span data-ttu-id="fd62e-2115">Un mot clé figurant dans la liste Keyword_german_drivers_license est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2115">A keyword from Keyword_german_drivers_license is found.</span></span>
- <span data-ttu-id="fd62e-2116">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2116">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-2117">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-2117">Keywords</span></span>

#### <a name="keyword_german_drivers_license_number"></a><span data-ttu-id="fd62e-2118">Keyword_german_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="fd62e-2118">Keyword_german_drivers_license_number</span></span>

- <span data-ttu-id="fd62e-2119">Führerschein</span><span class="sxs-lookup"><span data-stu-id="fd62e-2119">Führerschein</span></span>
- <span data-ttu-id="fd62e-2120">Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="fd62e-2120">Fuhrerschein</span></span>
- <span data-ttu-id="fd62e-2121">Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="fd62e-2121">Fuehrerschein</span></span>
- <span data-ttu-id="fd62e-2122">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="fd62e-2122">Führerscheinnummer</span></span>
- <span data-ttu-id="fd62e-2123">Fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="fd62e-2123">Fuhrerscheinnummer</span></span>
- <span data-ttu-id="fd62e-2124">Fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="fd62e-2124">Fuehrerscheinnummer</span></span>
- <span data-ttu-id="fd62e-2125">Führerschein</span><span class="sxs-lookup"><span data-stu-id="fd62e-2125">Führerschein-</span></span> 
- <span data-ttu-id="fd62e-2126">Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="fd62e-2126">Fuhrerschein-</span></span> 
- <span data-ttu-id="fd62e-2127">Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="fd62e-2127">Fuehrerschein-</span></span> 
- <span data-ttu-id="fd62e-2128">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="fd62e-2128">FührerscheinnummerNr</span></span>
- <span data-ttu-id="fd62e-2129">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="fd62e-2129">FuhrerscheinnummerNr</span></span>
- <span data-ttu-id="fd62e-2130">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="fd62e-2130">FuehrerscheinnummerNr</span></span>
- <span data-ttu-id="fd62e-2131">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="fd62e-2131">FührerscheinnummerKlasse</span></span>
- <span data-ttu-id="fd62e-2132">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="fd62e-2132">FuhrerscheinnummerKlasse</span></span>
- <span data-ttu-id="fd62e-2133">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="fd62e-2133">FuehrerscheinnummerKlasse</span></span>
- <span data-ttu-id="fd62e-2134">Führerschein - Nr</span><span class="sxs-lookup"><span data-stu-id="fd62e-2134">Führerschein- Nr</span></span>
- <span data-ttu-id="fd62e-2135">Fuhrerschein - Nr</span><span class="sxs-lookup"><span data-stu-id="fd62e-2135">Fuhrerschein- Nr</span></span>
- <span data-ttu-id="fd62e-2136">Fuehrerschein - Nr</span><span class="sxs-lookup"><span data-stu-id="fd62e-2136">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="fd62e-2137">Führerschein - Klasse</span><span class="sxs-lookup"><span data-stu-id="fd62e-2137">Führerschein- Klasse</span></span> 
- <span data-ttu-id="fd62e-2138">Fuhrerschein - Klasse</span><span class="sxs-lookup"><span data-stu-id="fd62e-2138">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="fd62e-2139">Fuehrerschein - Klasse</span><span class="sxs-lookup"><span data-stu-id="fd62e-2139">Fuehrerschein- Klasse</span></span>
- <span data-ttu-id="fd62e-2140">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="fd62e-2140">FührerscheinnummerNr</span></span> 
- <span data-ttu-id="fd62e-2141">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="fd62e-2141">FuhrerscheinnummerNr</span></span> 
- <span data-ttu-id="fd62e-2142">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="fd62e-2142">FuehrerscheinnummerNr</span></span> 
- <span data-ttu-id="fd62e-2143">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="fd62e-2143">FührerscheinnummerKlasse</span></span> 
- <span data-ttu-id="fd62e-2144">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="fd62e-2144">FuhrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="fd62e-2145">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="fd62e-2145">FuehrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="fd62e-2146">Führerschein - Nr</span><span class="sxs-lookup"><span data-stu-id="fd62e-2146">Führerschein- Nr</span></span> 
- <span data-ttu-id="fd62e-2147">Fuhrerschein - Nr</span><span class="sxs-lookup"><span data-stu-id="fd62e-2147">Fuhrerschein- Nr</span></span> 
- <span data-ttu-id="fd62e-2148">Fuehrerschein - Nr</span><span class="sxs-lookup"><span data-stu-id="fd62e-2148">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="fd62e-2149">Führerschein - Klasse</span><span class="sxs-lookup"><span data-stu-id="fd62e-2149">Führerschein- Klasse</span></span> 
- <span data-ttu-id="fd62e-2150">Fuhrerschein - Klasse</span><span class="sxs-lookup"><span data-stu-id="fd62e-2150">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="fd62e-2151">Fuehrerschein - Klasse</span><span class="sxs-lookup"><span data-stu-id="fd62e-2151">Fuehrerschein- Klasse</span></span> 
- <span data-ttu-id="fd62e-2152">LD</span><span class="sxs-lookup"><span data-stu-id="fd62e-2152">DL</span></span> 
- <span data-ttu-id="fd62e-2153">DISTRIBUTION</span><span class="sxs-lookup"><span data-stu-id="fd62e-2153">DLS</span></span>
- <span data-ttu-id="fd62e-2154">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2154">Driv Lic</span></span> 
- <span data-ttu-id="fd62e-2155">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2155">Driv Licen</span></span> 
- <span data-ttu-id="fd62e-2156">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2156">Driv License</span></span>
- <span data-ttu-id="fd62e-2157">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2157">Driv Licenses</span></span> 
- <span data-ttu-id="fd62e-2158">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2158">Driv Licence</span></span> 
- <span data-ttu-id="fd62e-2159">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2159">Driv Licences</span></span> 
- <span data-ttu-id="fd62e-2160">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2160">Driv Lic</span></span> 
- <span data-ttu-id="fd62e-2161">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2161">Driver Licen</span></span> 
- <span data-ttu-id="fd62e-2162">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2162">Driver License</span></span> 
- <span data-ttu-id="fd62e-2163">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2163">Driver Licenses</span></span> 
- <span data-ttu-id="fd62e-2164">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2164">Driver Licence</span></span> 
- <span data-ttu-id="fd62e-2165">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2165">Driver Licences</span></span> 
- <span data-ttu-id="fd62e-2166">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2166">Drivers Lic</span></span> 
- <span data-ttu-id="fd62e-2167">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2167">Drivers Licen</span></span> 
- <span data-ttu-id="fd62e-2168">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2168">Drivers License</span></span> 
- <span data-ttu-id="fd62e-2169">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2169">Drivers Licenses</span></span> 
- <span data-ttu-id="fd62e-2170">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2170">Drivers Licence</span></span> 
- <span data-ttu-id="fd62e-2171">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2171">Drivers Licences</span></span> 
- <span data-ttu-id="fd62e-2172">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2172">Driver's Lic</span></span> 
- <span data-ttu-id="fd62e-2173">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2173">Driver's Licen</span></span> 
- <span data-ttu-id="fd62e-2174">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2174">Driver's License</span></span> 
- <span data-ttu-id="fd62e-2175">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2175">Driver's Licenses</span></span> 
- <span data-ttu-id="fd62e-2176">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2176">Driver's Licence</span></span> 
- <span data-ttu-id="fd62e-2177">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2177">Driver's Licences</span></span> 
- <span data-ttu-id="fd62e-2178">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2178">Driving Lic</span></span> 
- <span data-ttu-id="fd62e-2179">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2179">Driving Licen</span></span> 
- <span data-ttu-id="fd62e-2180">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2180">Driving License</span></span> 
- <span data-ttu-id="fd62e-2181">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2181">Driving Licenses</span></span> 
- <span data-ttu-id="fd62e-2182">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2182">Driving Licence</span></span> 
- <span data-ttu-id="fd62e-2183">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2183">Driving Licences</span></span>

#### <a name="keyword_german_drivers_license_collaborative"></a><span data-ttu-id="fd62e-2184">Keyword_german_drivers_license_collaborative</span><span class="sxs-lookup"><span data-stu-id="fd62e-2184">Keyword_german_drivers_license_collaborative</span></span>

- <span data-ttu-id="fd62e-2185">Nr-Führerschein</span><span class="sxs-lookup"><span data-stu-id="fd62e-2185">Nr-Führerschein</span></span> 
- <span data-ttu-id="fd62e-2186">Nr-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="fd62e-2186">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="fd62e-2187">Nr-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="fd62e-2187">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="fd62e-2188">Non-Führerschein</span><span class="sxs-lookup"><span data-stu-id="fd62e-2188">No-Führerschein</span></span> 
- <span data-ttu-id="fd62e-2189">Non-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="fd62e-2189">No-Fuhrerschein</span></span> 
- <span data-ttu-id="fd62e-2190">Non-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="fd62e-2190">No-Fuehrerschein</span></span> 
- <span data-ttu-id="fd62e-2191">N-Führerschein</span><span class="sxs-lookup"><span data-stu-id="fd62e-2191">N-Führerschein</span></span> 
- <span data-ttu-id="fd62e-2192">N-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="fd62e-2192">N-Fuhrerschein</span></span> 
- <span data-ttu-id="fd62e-2193">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="fd62e-2193">N-Fuehrerschein</span></span>
- <span data-ttu-id="fd62e-2194">Nr-Führerschein</span><span class="sxs-lookup"><span data-stu-id="fd62e-2194">Nr-Führerschein</span></span> 
- <span data-ttu-id="fd62e-2195">Nr-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="fd62e-2195">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="fd62e-2196">Nr-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="fd62e-2196">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="fd62e-2197">Non-Führerschein</span><span class="sxs-lookup"><span data-stu-id="fd62e-2197">No-Führerschein</span></span> 
- <span data-ttu-id="fd62e-2198">Non-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="fd62e-2198">No-Fuhrerschein</span></span> 
- <span data-ttu-id="fd62e-2199">Non-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="fd62e-2199">No-Fuehrerschein</span></span> 
- <span data-ttu-id="fd62e-2200">N-Führerschein</span><span class="sxs-lookup"><span data-stu-id="fd62e-2200">N-Führerschein</span></span> 
- <span data-ttu-id="fd62e-2201">N-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="fd62e-2201">N-Fuhrerschein</span></span> 
- <span data-ttu-id="fd62e-2202">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="fd62e-2202">N-Fuehrerschein</span></span> 

#### <a name="keyword_german_drivers_license"></a><span data-ttu-id="fd62e-2203">Keyword_german_drivers_license</span><span class="sxs-lookup"><span data-stu-id="fd62e-2203">Keyword_german_drivers_license</span></span>

- <span data-ttu-id="fd62e-2204">ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="fd62e-2204">ausstellungsdatum</span></span>
- <span data-ttu-id="fd62e-2205">ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="fd62e-2205">ausstellungsort</span></span>
- <span data-ttu-id="fd62e-2206">ausstellende behöde</span><span class="sxs-lookup"><span data-stu-id="fd62e-2206">ausstellende behöde</span></span>
- <span data-ttu-id="fd62e-2207">ausstellende behorde</span><span class="sxs-lookup"><span data-stu-id="fd62e-2207">ausstellende behorde</span></span>
- <span data-ttu-id="fd62e-2208">ausstellende behoerde</span><span class="sxs-lookup"><span data-stu-id="fd62e-2208">ausstellende behoerde</span></span>
   
## <a name="german-passport-number"></a><span data-ttu-id="fd62e-2209">Numéro de passeport Allemagne</span><span class="sxs-lookup"><span data-stu-id="fd62e-2209">German Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-2210">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-2210">Format</span></span>

<span data-ttu-id="fd62e-2211">10 chiffres ou lettres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2211">10 digits or letters</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-2212">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2212">Pattern</span></span>

<span data-ttu-id="fd62e-2213">Le modèle doit inclure tous les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2213">Pattern must include all of the following:</span></span>
- <span data-ttu-id="fd62e-2214">Le premier caractère est un chiffre ou une lettre de cet ensemble (C, F, G, H, J, K)</span><span class="sxs-lookup"><span data-stu-id="fd62e-2214">First character is a digit or a letter from this set (C, F, G, H, J, K)</span></span> 
- <span data-ttu-id="fd62e-2215">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2215">Three digits</span></span> 
- <span data-ttu-id="fd62e-2216">Cinq chiffres ou lettres à partir de cet ensemble (C, -H, J-N, P, R, T, V-Z)</span><span class="sxs-lookup"><span data-stu-id="fd62e-2216">Five digits or letters from this set (C, -H, J-N, P, R, T, V-Z)</span></span> 
- <span data-ttu-id="fd62e-2217">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="fd62e-2217">A digit</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-2218">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2218">Checksum</span></span>

<span data-ttu-id="fd62e-2219">Oui</span><span class="sxs-lookup"><span data-stu-id="fd62e-2219">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-2220">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-2220">Definition</span></span>

<span data-ttu-id="fd62e-2221">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2221">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-2222">La fonction Func_german_passport trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2222">The function Func_german_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-2223">Un mot clé présent dans l’une des cinq listes de mots clés est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2223">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="fd62e-2224">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2224">The checksum passes.</span></span>

<span data-ttu-id="fd62e-2225">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2225">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-2226">La fonction Func_german_passport_data trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2226">The function Func_german_passport_data finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-2227">Un mot clé présent dans l’une des cinq listes de mots clés est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2227">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="fd62e-2228">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2228">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-2229">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-2229">Keywords</span></span>

#### <a name="keyword_german_passport"></a><span data-ttu-id="fd62e-2230">Keyword_german_passport</span><span class="sxs-lookup"><span data-stu-id="fd62e-2230">Keyword_german_passport</span></span>

- <span data-ttu-id="fd62e-2231">reisepass</span><span class="sxs-lookup"><span data-stu-id="fd62e-2231">reisepass</span></span>
- <span data-ttu-id="fd62e-2232">reisepasse</span><span class="sxs-lookup"><span data-stu-id="fd62e-2232">reisepasse</span></span>
- <span data-ttu-id="fd62e-2233">reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="fd62e-2233">reisepassnummer</span></span>
- <span data-ttu-id="fd62e-2234">tel</span><span class="sxs-lookup"><span data-stu-id="fd62e-2234">passport</span></span>
- <span data-ttu-id="fd62e-2235">passeports</span><span class="sxs-lookup"><span data-stu-id="fd62e-2235">passports</span></span>

#### <a name="keyword_german_passport_collaborative"></a><span data-ttu-id="fd62e-2236">Keyword_german_passport_collaborative</span><span class="sxs-lookup"><span data-stu-id="fd62e-2236">Keyword_german_passport_collaborative</span></span>

- <span data-ttu-id="fd62e-2237">geburtsdatum</span><span class="sxs-lookup"><span data-stu-id="fd62e-2237">geburtsdatum</span></span>
- <span data-ttu-id="fd62e-2238">ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="fd62e-2238">ausstellungsdatum</span></span>
- <span data-ttu-id="fd62e-2239">ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="fd62e-2239">ausstellungsort</span></span>

#### <a name="keyword_german_passport_number"></a><span data-ttu-id="fd62e-2240">Keyword_german_passport_number</span><span class="sxs-lookup"><span data-stu-id="fd62e-2240">Keyword_german_passport_number</span></span>

<span data-ttu-id="fd62e-2241">No-Reisepass Nr-Reisepass</span><span class="sxs-lookup"><span data-stu-id="fd62e-2241">No-Reisepass Nr-Reisepass</span></span>

#### <a name="keyword_german_passport1"></a><span data-ttu-id="fd62e-2242">Keyword_german_passport1</span><span class="sxs-lookup"><span data-stu-id="fd62e-2242">Keyword_german_passport1</span></span>

<span data-ttu-id="fd62e-2243">Reisepass-Nr</span><span class="sxs-lookup"><span data-stu-id="fd62e-2243">Reisepass-Nr</span></span>

#### <a name="keyword_german_passport2"></a><span data-ttu-id="fd62e-2244">Keyword_german_passport2</span><span class="sxs-lookup"><span data-stu-id="fd62e-2244">Keyword_german_passport2</span></span>

<span data-ttu-id="fd62e-2245">bnationalit. t</span><span class="sxs-lookup"><span data-stu-id="fd62e-2245">bnationalit.t</span></span>
   
## <a name="germany-identity-card-number"></a><span data-ttu-id="fd62e-2246">Numéro de carte d’identité allemand</span><span class="sxs-lookup"><span data-stu-id="fd62e-2246">Germany Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-2247">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-2247">Format</span></span>

<span data-ttu-id="fd62e-2248">Depuis le 1er novembre 2010: neuf lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2248">Since 1 November 2010: Nine letters and digits</span></span>

<span data-ttu-id="fd62e-2249">Du 1er avril 1987 au 31 octobre 2010:10 chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2249">From 1 April 1987 until 31 October 2010: 10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-2250">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2250">Pattern</span></span>

<span data-ttu-id="fd62e-2251">Depuis le 1er novembre 2010 :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2251">Since 1 November 2010:</span></span>
- <span data-ttu-id="fd62e-2252">Une lettre (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="fd62e-2252">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="fd62e-2253">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2253">Eight digits</span></span>

<span data-ttu-id="fd62e-2254">Du 1er avril 1987 au 31 octobre 2010:</span><span class="sxs-lookup"><span data-stu-id="fd62e-2254">From 1 April 1987 until 31 October 2010:</span></span>
- <span data-ttu-id="fd62e-2255">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2255">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-2256">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2256">Checksum</span></span>

<span data-ttu-id="fd62e-2257">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-2257">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-2258">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-2258">Definition</span></span>

<span data-ttu-id="fd62e-2259">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2259">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-2260">L’expression régulière Regex_germany_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2260">The regular expression Regex_germany_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-2261">Un mot clé figurant dans la liste Keyword_germany_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2261">A keyword from Keyword_germany_id_card is found.</span></span>

```xml
<!-- Germany Identity Card Number -->
<Entity id="e577372f-c42e-47a0-9d85-bebed1c237d4" recommendedConfidence="65" patternsProximity="300">
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Regex_germany_id_card"/>
     <Match idRef="Keyword_germany_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fd62e-2262">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-2262">Keywords</span></span>

#### <a name="keyword_germany_id_card"></a><span data-ttu-id="fd62e-2263">Keyword_germany_id_card</span><span class="sxs-lookup"><span data-stu-id="fd62e-2263">Keyword_germany_id_card</span></span>

- <span data-ttu-id="fd62e-2264">Identity Card</span><span class="sxs-lookup"><span data-stu-id="fd62e-2264">Identity Card</span></span>
- <span data-ttu-id="fd62e-2265">ID</span><span class="sxs-lookup"><span data-stu-id="fd62e-2265">ID</span></span>
- <span data-ttu-id="fd62e-2266">Identificateur</span><span class="sxs-lookup"><span data-stu-id="fd62e-2266">Identification</span></span>
- <span data-ttu-id="fd62e-2267">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="fd62e-2267">Personalausweis</span></span>
- <span data-ttu-id="fd62e-2268">Identifizierungsnummer</span><span class="sxs-lookup"><span data-stu-id="fd62e-2268">Identifizierungsnummer</span></span>
- <span data-ttu-id="fd62e-2269">Ausweis</span><span class="sxs-lookup"><span data-stu-id="fd62e-2269">Ausweis</span></span>
- <span data-ttu-id="fd62e-2270">Identifikation</span><span class="sxs-lookup"><span data-stu-id="fd62e-2270">Identifikation</span></span>
   
## <a name="greece-national-id-card"></a><span data-ttu-id="fd62e-2271">Carte d’identité nationale Grèce</span><span class="sxs-lookup"><span data-stu-id="fd62e-2271">Greece National ID Card</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-2272">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-2272">Format</span></span>

<span data-ttu-id="fd62e-2273">Combinaison de 7 ou 8 lettres et chiffres, plus un tiret</span><span class="sxs-lookup"><span data-stu-id="fd62e-2273">Combination of 7-8 letters and numbers plus a dash</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-2274">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2274">Pattern</span></span>

<span data-ttu-id="fd62e-2275">Sept lettres et chiffres (ancien format) :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2275">Seven letters and numbers (old format):</span></span>
- <span data-ttu-id="fd62e-2276">Une lettre (de l’alphabet grec) </span><span class="sxs-lookup"><span data-stu-id="fd62e-2276">One letter (any letter of the Greek alphabet)</span></span> 
- <span data-ttu-id="fd62e-2277">Un tiret</span><span class="sxs-lookup"><span data-stu-id="fd62e-2277">A dash</span></span> 
- <span data-ttu-id="fd62e-2278">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2278">Six digits</span></span>

<span data-ttu-id="fd62e-2279">Huit lettres et chiffres (nouveau format) :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2279">Eight letters and numbers (new format):</span></span>
- <span data-ttu-id="fd62e-2280">Deux lettres dont le caractère majuscule figure à la fois dans l’alphabet grec et l’alphabet latin (ABEZHIKMNOPTYX) </span><span class="sxs-lookup"><span data-stu-id="fd62e-2280">Two letters whose uppercase character occurs in both the Greek and Latin alphabets (ABEZHIKMNOPTYX)</span></span> 
- <span data-ttu-id="fd62e-2281">Un tiret</span><span class="sxs-lookup"><span data-stu-id="fd62e-2281">A dash</span></span> 
- <span data-ttu-id="fd62e-2282">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2282">Six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-2283">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2283">Checksum</span></span>

<span data-ttu-id="fd62e-2284">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-2284">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-2285">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-2285">Definition</span></span>

<span data-ttu-id="fd62e-2286">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2286">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-2287">L’expression régulière Regex_greece_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2287">The regular expression Regex_greece_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-2288">Un mot clé figurant dans la liste Keyword_greece_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2288">A keyword from Keyword_greece_id_card is found.</span></span>

```xml
<!-- Greece National ID Card -->
<Entity id="82568215-1da1-46d3-874a-d2294d81b5ac" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_greece_id_card"/>
     <Match idRef="Keyword_greece_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fd62e-2289">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-2289">Keywords</span></span>

#### <a name="keyword_greece_id_card"></a><span data-ttu-id="fd62e-2290">Keyword_greece_id_card</span><span class="sxs-lookup"><span data-stu-id="fd62e-2290">Keyword_greece_id_card</span></span>

- <span data-ttu-id="fd62e-2291">Greek identity Card</span><span class="sxs-lookup"><span data-stu-id="fd62e-2291">Greek identity Card</span></span>
- <span data-ttu-id="fd62e-2292">Tautotita</span><span class="sxs-lookup"><span data-stu-id="fd62e-2292">Tautotita</span></span>
- <span data-ttu-id="fd62e-2293">Δελτίο αστυνομικής ταυτότητας</span><span class="sxs-lookup"><span data-stu-id="fd62e-2293">Δελτίο αστυνομικής ταυτότητας</span></span>
- <span data-ttu-id="fd62e-2294">Ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="fd62e-2294">Ταυτότητα</span></span>
   
## <a name="hong-kong-identity-card-hkid-number"></a><span data-ttu-id="fd62e-2295">Numéro de carte d’identité (HKID) Hong Kong</span><span class="sxs-lookup"><span data-stu-id="fd62e-2295">Hong Kong Identity Card (HKID) Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-2296">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-2296">Format</span></span>

<span data-ttu-id="fd62e-2297">Combinaison de 8 ou 9 lettres et chiffres plus éventuellement des parenthèses autour du dernier caractère</span><span class="sxs-lookup"><span data-stu-id="fd62e-2297">Combination of 8-9 letters and numbers plus optional parentheses around the final character</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-2298">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2298">Pattern</span></span>

<span data-ttu-id="fd62e-2299">Combinaison de 8 ou 9 lettres :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2299">Combination of 8-9 letters:</span></span>
- <span data-ttu-id="fd62e-2300">1 ou 2 lettres (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="fd62e-2300">1-2 letters (not case sensitive)</span></span> 
- <span data-ttu-id="fd62e-2301">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2301">Six digits</span></span> 
- <span data-ttu-id="fd62e-2302">Le dernier caractère (un chiffre ou la lettre A), qui est le chiffre de contrôle et est éventuellement entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2302">The final character (any digit or the letter A), which is the check digit and is optionally enclosed in parentheses.</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-2303">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2303">Checksum</span></span>

<span data-ttu-id="fd62e-2304">Oui</span><span class="sxs-lookup"><span data-stu-id="fd62e-2304">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-2305">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-2305">Definition</span></span>

<span data-ttu-id="fd62e-2306">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2306">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-2307">La fonction Func_hong_kong_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2307">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-2308">Un mot clé figurant dans la liste Keyword_hong_kong_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2308">A keyword from Keyword_hong_kong_id_card is found.</span></span>
- <span data-ttu-id="fd62e-2309">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2309">The checksum passes.</span></span>

<span data-ttu-id="fd62e-2310">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2310">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-2311">La fonction Func_hong_kong_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2311">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-2312">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2312">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-2313">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-2313">Keywords</span></span>

#### <a name="keyword_hong_kong_id_card"></a><span data-ttu-id="fd62e-2314">Keyword_hong_kong_id_card</span><span class="sxs-lookup"><span data-stu-id="fd62e-2314">Keyword_hong_kong_id_card</span></span>

- <span data-ttu-id="fd62e-2315">carte d’identité de Hong Kong</span><span class="sxs-lookup"><span data-stu-id="fd62e-2315">hong kong identity card</span></span>
- <span data-ttu-id="fd62e-2316">HKIDC</span><span class="sxs-lookup"><span data-stu-id="fd62e-2316">HKIDC</span></span>
- <span data-ttu-id="fd62e-2317">carte d’identité</span><span class="sxs-lookup"><span data-stu-id="fd62e-2317">id card</span></span>
- <span data-ttu-id="fd62e-2318">Carte d’identité</span><span class="sxs-lookup"><span data-stu-id="fd62e-2318">identity card</span></span>
- <span data-ttu-id="fd62e-2319">carte d’identité HK</span><span class="sxs-lookup"><span data-stu-id="fd62e-2319">hk identity card</span></span>
- <span data-ttu-id="fd62e-2320">ID Hong Kong</span><span class="sxs-lookup"><span data-stu-id="fd62e-2320">hong kong id</span></span>
- <span data-ttu-id="fd62e-2321">香港身份證</span><span class="sxs-lookup"><span data-stu-id="fd62e-2321">香港身份證</span></span>
- <span data-ttu-id="fd62e-2322">香港永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="fd62e-2322">香港永久性居民身份證</span></span>
- <span data-ttu-id="fd62e-2323">身份證</span><span class="sxs-lookup"><span data-stu-id="fd62e-2323">身份證</span></span>
- <span data-ttu-id="fd62e-2324">身份証</span><span class="sxs-lookup"><span data-stu-id="fd62e-2324">身份証</span></span>
- <span data-ttu-id="fd62e-2325">身分證</span><span class="sxs-lookup"><span data-stu-id="fd62e-2325">身分證</span></span>
- <span data-ttu-id="fd62e-2326">身分証</span><span class="sxs-lookup"><span data-stu-id="fd62e-2326">身分証</span></span>
- <span data-ttu-id="fd62e-2327">香港身份証</span><span class="sxs-lookup"><span data-stu-id="fd62e-2327">香港身份証</span></span>
- <span data-ttu-id="fd62e-2328">香港身分證</span><span class="sxs-lookup"><span data-stu-id="fd62e-2328">香港身分證</span></span>
- <span data-ttu-id="fd62e-2329">香港身分証</span><span class="sxs-lookup"><span data-stu-id="fd62e-2329">香港身分証</span></span>
- <span data-ttu-id="fd62e-2330">香港身份證</span><span class="sxs-lookup"><span data-stu-id="fd62e-2330">香港身份證</span></span>
- <span data-ttu-id="fd62e-2331">香港居民身份證</span><span class="sxs-lookup"><span data-stu-id="fd62e-2331">香港居民身份證</span></span>
- <span data-ttu-id="fd62e-2332">香港居民身份証</span><span class="sxs-lookup"><span data-stu-id="fd62e-2332">香港居民身份証</span></span>
- <span data-ttu-id="fd62e-2333">香港居民身分證</span><span class="sxs-lookup"><span data-stu-id="fd62e-2333">香港居民身分證</span></span>
- <span data-ttu-id="fd62e-2334">香港居民身分証</span><span class="sxs-lookup"><span data-stu-id="fd62e-2334">香港居民身分証</span></span>
- <span data-ttu-id="fd62e-2335">香港永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="fd62e-2335">香港永久性居民身份証</span></span>
- <span data-ttu-id="fd62e-2336">香港永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="fd62e-2336">香港永久性居民身分證</span></span>
- <span data-ttu-id="fd62e-2337">香港永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="fd62e-2337">香港永久性居民身分証</span></span>
- <span data-ttu-id="fd62e-2338">香港永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="fd62e-2338">香港永久性居民身份證</span></span>
- <span data-ttu-id="fd62e-2339">香港非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="fd62e-2339">香港非永久性居民身份證</span></span>
- <span data-ttu-id="fd62e-2340">香港非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="fd62e-2340">香港非永久性居民身份証</span></span>
- <span data-ttu-id="fd62e-2341">香港非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="fd62e-2341">香港非永久性居民身分證</span></span>
- <span data-ttu-id="fd62e-2342">香港非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="fd62e-2342">香港非永久性居民身分証</span></span>
- <span data-ttu-id="fd62e-2343">香港特別行政區永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="fd62e-2343">香港特別行政區永久性居民身份證</span></span>
- <span data-ttu-id="fd62e-2344">香港特別行政區永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="fd62e-2344">香港特別行政區永久性居民身份証</span></span>
- <span data-ttu-id="fd62e-2345">香港特別行政區永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="fd62e-2345">香港特別行政區永久性居民身分證</span></span>
- <span data-ttu-id="fd62e-2346">香港特別行政區永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="fd62e-2346">香港特別行政區永久性居民身分証</span></span>
- <span data-ttu-id="fd62e-2347">香港特別行政區非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="fd62e-2347">香港特別行政區非永久性居民身份證</span></span>
- <span data-ttu-id="fd62e-2348">香港特別行政區非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="fd62e-2348">香港特別行政區非永久性居民身份証</span></span>
- <span data-ttu-id="fd62e-2349">香港特別行政區非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="fd62e-2349">香港特別行政區非永久性居民身分證</span></span>
- <span data-ttu-id="fd62e-2350">香港特別行政區非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="fd62e-2350">香港特別行政區非永久性居民身分証</span></span>
   
## <a name="india-permanent-account-number-pan"></a><span data-ttu-id="fd62e-2351">Numéro de compte permanent Inde</span><span class="sxs-lookup"><span data-stu-id="fd62e-2351">India Permanent Account Number (PAN)</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-2352">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-2352">Format</span></span>

<span data-ttu-id="fd62e-2353">10 lettres ou chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2353">10 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-2354">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2354">Pattern</span></span>

<span data-ttu-id="fd62e-2355">10 lettres ou chiffres :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2355">10 letters or digits:</span></span>
- <span data-ttu-id="fd62e-2356">Cinq lettres (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="fd62e-2356">Five letters (not case sensitive)</span></span> 
- <span data-ttu-id="fd62e-2357">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2357">Four digits</span></span> 
- <span data-ttu-id="fd62e-2358">Une lettre qui est un chiffre de contrôle alphabétique</span><span class="sxs-lookup"><span data-stu-id="fd62e-2358">A letter which is an alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-2359">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2359">Checksum</span></span>

<span data-ttu-id="fd62e-2360">Oui</span><span class="sxs-lookup"><span data-stu-id="fd62e-2360">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-2361">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-2361">Definition</span></span>

<span data-ttu-id="fd62e-2362">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2362">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-2363">L’expression régulière Regex_india_permanent_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2363">The regular expression Regex_india_permanent_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-2364">Un mot clé figurant dans la liste Keyword_india_permanent_account_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2364">A keyword from Keyword_india_permanent_account_number is found.</span></span>
- <span data-ttu-id="fd62e-2365">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2365">The checksum passes.</span></span>

```xml
<!-- India Permanent Account Number -->
<Entity id="2602bfee-9bb0-47a5-a7a6-2bf3053e2804" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_india_permanent_account_number"/>
     <Match idRef="Keyword_india_permanent_account_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fd62e-2366">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-2366">Keywords</span></span>

#### <a name="keyword_india_permanent_account_number"></a><span data-ttu-id="fd62e-2367">Keyword_india_permanent_account_number</span><span class="sxs-lookup"><span data-stu-id="fd62e-2367">Keyword_india_permanent_account_number</span></span>

- <span data-ttu-id="fd62e-2368">Permanent Account Number</span><span class="sxs-lookup"><span data-stu-id="fd62e-2368">Permanent Account Number</span></span> 
- <span data-ttu-id="fd62e-2369">PANEUROPÉENNES</span><span class="sxs-lookup"><span data-stu-id="fd62e-2369">PAN</span></span> 
   
## <a name="india-unique-identification-aadhaar-number"></a><span data-ttu-id="fd62e-2370">Numéro d’identification unique (Aadhaar) Inde</span><span class="sxs-lookup"><span data-stu-id="fd62e-2370">India Unique Identification (Aadhaar) Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-2371">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-2371">Format</span></span>

<span data-ttu-id="fd62e-2372">12 chiffres contenant éventuellement des espaces ou des tirets</span><span class="sxs-lookup"><span data-stu-id="fd62e-2372">12 digits containing optional spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-2373">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2373">Pattern</span></span>

<span data-ttu-id="fd62e-2374">12 chiffres :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2374">12 digits:</span></span>
- <span data-ttu-id="fd62e-2375">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2375">Four digits</span></span> 
- <span data-ttu-id="fd62e-2376">Éventuellement un tiret ou un espace </span><span class="sxs-lookup"><span data-stu-id="fd62e-2376">An optional space or dash</span></span> 
- <span data-ttu-id="fd62e-2377">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2377">Four digits</span></span> 
- <span data-ttu-id="fd62e-2378">Éventuellement un tiret ou un espace </span><span class="sxs-lookup"><span data-stu-id="fd62e-2378">An optional space or dash</span></span> 
- <span data-ttu-id="fd62e-2379">Le chiffre final, qui est le chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2379">The final digit which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-2380">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2380">Checksum</span></span>

<span data-ttu-id="fd62e-2381">Oui</span><span class="sxs-lookup"><span data-stu-id="fd62e-2381">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-2382">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-2382">Definition</span></span>

<span data-ttu-id="fd62e-2383">Une stratégie DLP est sûre à 85% d’avoir détecté ce type d’informations sensibles si, dans une proximité de 300 caractères: la fonction Func_india_aadhaar trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2383">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern.</span></span>
<span data-ttu-id="fd62e-2384">Un mot clé figurant dans la liste Keyword_india_aadhar est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2384">A keyword from Keyword_india_aadhar is found.</span></span>
<span data-ttu-id="fd62e-2385">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2385">The checksum passes.</span></span>
<span data-ttu-id="fd62e-2386">Une stratégie DLP est sûre à 75% d’avoir détecté ce type d’informations sensibles si, dans une proximité de 300 caractères: la fonction Func_india_aadhaar trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2386">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern.</span></span>
<span data-ttu-id="fd62e-2387">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2387">The checksum passes.</span></span>
```xml
<!-- India Unique Identification (Aadhaar) number -->
<Entity id="1ca46b29-76f5-4f46-9383-cfa15e91048f" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_india_aadhaar"/>
     <Match idRef="Keyword_india_aadhar"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_india_aadhaar"/>
  </Pattern>
</Entity>

### Keywords
   
#### Keyword_india_aadhar
- Aadhar
- Aadhaar
- UID
- आधार
   
## Indonesia Identity Card (KTP) Number

### Format

16 digits containing optional periods

### Pattern

16 digits:
- Two-digit province code 
- A period (optional) 
- Two-digit regency or city code 
- Two-digit subdistrict code 
- A period (optional) 
- Six digits in the format DDMMYY which are the date of birth 
- A period (optional) 
- Four digits

### Checksum

No

### Definition

A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:
- The regular expression Regex_indonesia_id_card finds content that matches the pattern.
- A keyword from Keyword_indonesia_id_card is found.

A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:
- The regular expression Regex_indonesia_id_card finds content that matches the pattern.

```
<!-- Indonesia Identity Card (KTP) Number -->
<span data-ttu-id="fd62e-2388"><Entity id="da68fdb0-f383-4981-8c86-82689d3b7d55" recommendedConfidence="85" patternsProximity="300"> <Pattern confidenceLevel="85"> <IdMatch idRef="Regex_indonesia_id_card"/> <Match idRef="Keyword_indonesia_id_card"/> </Pattern> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_indonesia_id_card"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="fd62e-2388"></span></span>
```

### Keywords
   
#### Keyword_indonesia_id_card

- KTP
- Kartu Tanda Penduduk 
- Nomor Induk Kependudukan 
   
## International Banking Account Number (IBAN)

### Format

Country code (two letters) plus check digits (two digits) plus bban number (up to 30 characters)

### Pattern

Pattern must include all of the following:

- Two-letter country code
- Two check digits (followed by an optional space) 
- 1-7 groups of four letters or digits (can be separated by spaces)
- 1-3 letters or digits

The format for each country is slightly different. The IBAN sensitive information type covers these 60 countries:

ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg

### Checksum

Yes

### Definition

A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:
- The function Func_iban finds content that matches the pattern.
- The checksum passes.

```xml
<Entity id="e7dc4711-11b7-4cb0-b88b-2c394a771f0e" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_iban" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fd62e-2389">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-2389">Keywords</span></span>

<span data-ttu-id="fd62e-2390">Aucun</span><span class="sxs-lookup"><span data-stu-id="fd62e-2390">None</span></span>

   
## <a name="ip-address"></a><span data-ttu-id="fd62e-2391">Adresse IP</span><span class="sxs-lookup"><span data-stu-id="fd62e-2391">IP Address</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-2392">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-2392">Format</span></span>

#### <a name="ipv4"></a><span data-ttu-id="fd62e-2393">IPv6</span><span class="sxs-lookup"><span data-stu-id="fd62e-2393">IPv4:</span></span>
<span data-ttu-id="fd62e-2394">Modèle complexe qui tient compte des versions mises en forme (points) et non mises en forme (sans points) des adresses IPv4</span><span class="sxs-lookup"><span data-stu-id="fd62e-2394">Complex pattern which accounts for formatted (periods) and unformatted (no periods) versions of the IPv4 addresses</span></span>

#### <a name="ipv6"></a><span data-ttu-id="fd62e-2395">IPv4/IPv6</span><span class="sxs-lookup"><span data-stu-id="fd62e-2395">IPv6:</span></span>
<span data-ttu-id="fd62e-2396"> Modèle complexe qui tient compte des numéros IPv6 mis en forme (qui incluent les signes deux-points)</span><span class="sxs-lookup"><span data-stu-id="fd62e-2396">Complex pattern which accounts for formatted IPv6 numbers (which include colons)</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-2397">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2397">Pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-2398">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2398">Checksum</span></span>

<span data-ttu-id="fd62e-2399">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-2399">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-2400">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-2400">Definition</span></span>

<span data-ttu-id="fd62e-2401">Pour IPv6, le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2401">For IPv6, a DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-2402">L’expression régulière Regex_ipv6_address trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2402">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-2403">Aucun mot clé figurant dans la liste Keyword_ipaddress n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2403">No keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="fd62e-2404">Pour IPv4, le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 95 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2404">For IPv4, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-2405">L’expression régulière Regex_ipv4_address trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2405">The regular expression Regex_ipv4_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-2406">Un mot clé figurant dans la liste Keyword_ipaddress est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2406">A keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="fd62e-2407">Pour IPv6, le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 95 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2407">For IPv6, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-2408">L’expression régulière Regex_ipv6_address trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2408">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-2409">Aucun mot clé figurant dans la liste Keyword_ipaddress n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2409">No keyword from Keyword_ipaddress is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-2410">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-2410">Keywords</span></span>

#### <a name="keyword_ipaddress"></a><span data-ttu-id="fd62e-2411">Keyword_ipaddress</span><span class="sxs-lookup"><span data-stu-id="fd62e-2411">Keyword_ipaddress</span></span>

- <span data-ttu-id="fd62e-2412">IP (ce mot clé respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="fd62e-2412">IP (this keyword is case sensitive)</span></span>
- <span data-ttu-id="fd62e-2413">ip address</span><span class="sxs-lookup"><span data-stu-id="fd62e-2413">ip address</span></span> 
- <span data-ttu-id="fd62e-2414">adresses IP</span><span class="sxs-lookup"><span data-stu-id="fd62e-2414">ip addresses</span></span>
- <span data-ttu-id="fd62e-2415">protocole internet</span><span class="sxs-lookup"><span data-stu-id="fd62e-2415">internet protocol</span></span>
- <span data-ttu-id="fd62e-2416">IP-כתובת ה</span><span class="sxs-lookup"><span data-stu-id="fd62e-2416">IP-כתובת ה</span></span> 
   
## <a name="international-classification-of-diseases-icd-10-cm"></a><span data-ttu-id="fd62e-2417">Classification internationale des maladies (ICD-10-CM)</span><span class="sxs-lookup"><span data-stu-id="fd62e-2417">International Classification of Diseases (ICD-10-CM)</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-2418">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-2418">Format</span></span>

<span data-ttu-id="fd62e-2419">Dictionary</span><span class="sxs-lookup"><span data-stu-id="fd62e-2419">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-2420">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2420">Pattern</span></span>

<span data-ttu-id="fd62e-2421">Mot clé</span><span class="sxs-lookup"><span data-stu-id="fd62e-2421">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-2422">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2422">Checksum</span></span>

<span data-ttu-id="fd62e-2423">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-2423">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-2424">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-2424">Definition</span></span>

<span data-ttu-id="fd62e-2425">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2425">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-2426">Un mot clé depuis Dictionary_icd_10_cm est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2426">A keyword from Dictionary_icd_10_cm is found.</span></span>

```xml
      <!-- ICD-10 CM -->
      <Entity id="3356946c-6bb7-449b-b253-6ffa419c0ce7" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_10_cm" />
        </Pattern>
      </Entity>
```

<span data-ttu-id="fd62e-2427">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-2427">Keywords</span></span>

<span data-ttu-id="fd62e-2428">Tout terme du dictionnaire de mots clés Dictionary_icd_10_cm, qui est basé sur la [Classification internationale des maladies, dixième révision, modification clinique (ICD-10-cm)](https://go.microsoft.com/fwlink/?linkid=852604).</span><span class="sxs-lookup"><span data-stu-id="fd62e-2428">Any term from the Dictionary_icd_10_cm keyword dictionary, which is based on the [International Classification of Diseases, Tenth Revision, Clinical Modification (ICD-10-CM)](https://go.microsoft.com/fwlink/?linkid=852604).</span></span> <span data-ttu-id="fd62e-2429">Ce type recherche uniquement le terme, pas les codes d’assurance.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2429">This type looks only for the term, not the insurance codes.</span></span>

   
## <a name="international-classification-of-diseases-icd-9-cm"></a><span data-ttu-id="fd62e-2430">Classification internationale des maladies (ICD-9-CM)</span><span class="sxs-lookup"><span data-stu-id="fd62e-2430">International Classification of Diseases (ICD-9-CM)</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-2431">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-2431">Format</span></span>

<span data-ttu-id="fd62e-2432">Dictionary</span><span class="sxs-lookup"><span data-stu-id="fd62e-2432">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-2433">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2433">Pattern</span></span>

<span data-ttu-id="fd62e-2434">Mot clé</span><span class="sxs-lookup"><span data-stu-id="fd62e-2434">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-2435">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2435">Checksum</span></span>

<span data-ttu-id="fd62e-2436">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-2436">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-2437">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-2437">Definition</span></span>

<span data-ttu-id="fd62e-2438">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2438">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-2439">Un mot clé depuis Dictionary_icd_9_cm est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2439">A keyword from Dictionary_icd_9_cm is found.</span></span>

```xml
      <Entity id="fa3f9c74-ee07-4c52-b5f2-085d6b2c0ec4" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_9_cm" />
        </Pattern>
      </Entity>
```

### <a name="keywords"></a><span data-ttu-id="fd62e-2440">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-2440">Keywords</span></span>

<span data-ttu-id="fd62e-2441">Tout terme du dictionnaire de mots clés Dictionary_icd_9_cm, qui est basé sur la [Classification internationale des maladies, neuvième révision, modification clinique (ICD-9-cm)](https://go.microsoft.com/fwlink/?linkid=852605).</span><span class="sxs-lookup"><span data-stu-id="fd62e-2441">Any term from the Dictionary_icd_9_cm keyword dictionary, which is based on the [International Classification of Diseases,Ninth Revision, Clinical Modification (ICD-9-CM)](https://go.microsoft.com/fwlink/?linkid=852605).</span></span> <span data-ttu-id="fd62e-2442">Ce type recherche uniquement le terme, pas les codes d’assurance.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2442">This type looks only for the term, not the insurance codes.</span></span>
   
## <a name="ireland-personal-public-service-pps-number"></a><span data-ttu-id="fd62e-2443">Numéro de service public personnel (PPS) Irlande</span><span class="sxs-lookup"><span data-stu-id="fd62e-2443">Ireland Personal Public Service (PPS) Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-2444">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-2444">Format</span></span>

<span data-ttu-id="fd62e-2445">Ancien format (jusqu’au 31 décembre 2012):</span><span class="sxs-lookup"><span data-stu-id="fd62e-2445">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="fd62e-2446">Sept chiffres suivis de 1 ou 2 lettres </span><span class="sxs-lookup"><span data-stu-id="fd62e-2446">Seven digits followed by 1-2 letters</span></span> 

<span data-ttu-id="fd62e-2447">Nouveau format (1er janvier 2013 et après):</span><span class="sxs-lookup"><span data-stu-id="fd62e-2447">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="fd62e-2448">Sept chiffres suivis de deux lettres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2448">Seven digits followed by two letters</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-2449">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2449">Pattern</span></span>

<span data-ttu-id="fd62e-2450">Ancien format (jusqu’au 31 décembre 2012):</span><span class="sxs-lookup"><span data-stu-id="fd62e-2450">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="fd62e-2451">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="fd62e-2451">Seven digits</span></span> 
- <span data-ttu-id="fd62e-2452">1 ou 2 lettres (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="fd62e-2452">1-2 letters (not case sensitive)</span></span> 

<span data-ttu-id="fd62e-2453">Nouveau format (1er janvier 2013 et après):</span><span class="sxs-lookup"><span data-stu-id="fd62e-2453">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="fd62e-2454">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="fd62e-2454">Seven digits</span></span> 
- <span data-ttu-id="fd62e-2455">Une lettre (ne respectant pas la casse), qui est un chiffre de contrôle alphabétique </span><span class="sxs-lookup"><span data-stu-id="fd62e-2455">A letter (not case sensitive) which is an alphabetic check digit</span></span> 
- <span data-ttu-id="fd62e-2456">La lettre « A » ou « H » (ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="fd62e-2456">The letter "A" or "H" (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-2457">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2457">Checksum</span></span>

<span data-ttu-id="fd62e-2458">Oui</span><span class="sxs-lookup"><span data-stu-id="fd62e-2458">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-2459">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-2459">Definition</span></span>

<span data-ttu-id="fd62e-2460">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2460">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-2461">La fonction Func_ireland_pps trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2461">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-2462">L’une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2462">One of the following is true:</span></span>
    - <span data-ttu-id="fd62e-2463">Un mot clé figurant dans la liste Keyword_ireland_pps est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2463">A keyword from Keyword_ireland_pps is found.</span></span>
    - <span data-ttu-id="fd62e-2464">La fonction Func_eu_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2464">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="fd62e-2465">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2465">The checksum passes.</span></span>

<span data-ttu-id="fd62e-2466">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2466">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-2467">La fonction Func_ireland_pps trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2467">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-2468">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2468">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-2469">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-2469">Keywords</span></span>

#### <a name="keyword_ireland_pps"></a><span data-ttu-id="fd62e-2470">Keyword_ireland_pps</span><span class="sxs-lookup"><span data-stu-id="fd62e-2470">Keyword_ireland_pps</span></span>

- <span data-ttu-id="fd62e-2471">Personal Public Service Number</span><span class="sxs-lookup"><span data-stu-id="fd62e-2471">Personal Public Service Number</span></span> 
- <span data-ttu-id="fd62e-2472">PPS Number</span><span class="sxs-lookup"><span data-stu-id="fd62e-2472">PPS Number</span></span> 
- <span data-ttu-id="fd62e-2473">PPS Num</span><span class="sxs-lookup"><span data-stu-id="fd62e-2473">PPS Num</span></span> 
- <span data-ttu-id="fd62e-2474">PPS No.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2474">PPS No.</span></span> 
- <span data-ttu-id="fd62e-2475">PPS #</span><span class="sxs-lookup"><span data-stu-id="fd62e-2475">PPS #</span></span> 
- <span data-ttu-id="fd62e-2476">Spa #</span><span class="sxs-lookup"><span data-stu-id="fd62e-2476">PPS#</span></span> 
- <span data-ttu-id="fd62e-2477">PPSN</span><span class="sxs-lookup"><span data-stu-id="fd62e-2477">PPSN</span></span> 
- <span data-ttu-id="fd62e-2478">Public Services Card</span><span class="sxs-lookup"><span data-stu-id="fd62e-2478">Public Services Card</span></span> 
- <span data-ttu-id="fd62e-2479">Uimhir Phearsanta Seirbhíse Poiblí</span><span class="sxs-lookup"><span data-stu-id="fd62e-2479">Uimhir Phearsanta Seirbhíse Poiblí</span></span> 
- <span data-ttu-id="fd62e-2480">Uimh.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2480">Uimh.</span></span> <span data-ttu-id="fd62e-2481">TOXINE</span><span class="sxs-lookup"><span data-stu-id="fd62e-2481">PSP</span></span> 
- <span data-ttu-id="fd62e-2482">TOXINE</span><span class="sxs-lookup"><span data-stu-id="fd62e-2482">PSP</span></span> 
   
## <a name="israel-bank-account-number"></a><span data-ttu-id="fd62e-2483">Numéro de compte bancaire Israël</span><span class="sxs-lookup"><span data-stu-id="fd62e-2483">Israel Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-2484">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-2484">Format</span></span>

<span data-ttu-id="fd62e-2485">13 chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2485">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-2486">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2486">Pattern</span></span>

<span data-ttu-id="fd62e-2487">Avec</span><span class="sxs-lookup"><span data-stu-id="fd62e-2487">Formatted:</span></span>
- <span data-ttu-id="fd62e-2488">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2488">Two digits</span></span> 
- <span data-ttu-id="fd62e-2489">Un tiret</span><span class="sxs-lookup"><span data-stu-id="fd62e-2489">A dash</span></span> 
- <span data-ttu-id="fd62e-2490">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2490">Three digits</span></span> 
- <span data-ttu-id="fd62e-2491">Un tiret</span><span class="sxs-lookup"><span data-stu-id="fd62e-2491">A dash</span></span> 
- <span data-ttu-id="fd62e-2492">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2492">Eight digits</span></span>

<span data-ttu-id="fd62e-2493">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-2493">Unformatted:</span></span>
- <span data-ttu-id="fd62e-2494">	13 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="fd62e-2494">13 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-2495">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2495">Checksum</span></span>

<span data-ttu-id="fd62e-2496">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-2496">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-2497">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-2497">Definition</span></span>

<span data-ttu-id="fd62e-2498">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2498">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-2499">L’expression régulière Regex_israel_bank_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2499">The regular expression Regex_israel_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-2500">Un mot clé figurant dans la liste Keyword_israel_bank_account_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2500">A keyword from Keyword_israel_bank_account_number is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-2501">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-2501">Keywords</span></span>

#### <a name="keyword_israel_bank_account_number"></a><span data-ttu-id="fd62e-2502">Keyword_israel_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="fd62e-2502">Keyword_israel_bank_account_number</span></span>

- <span data-ttu-id="fd62e-2503">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="fd62e-2503">Bank Account Number</span></span> 
- <span data-ttu-id="fd62e-2504">Bank Account</span><span class="sxs-lookup"><span data-stu-id="fd62e-2504">Bank Account</span></span> 
- <span data-ttu-id="fd62e-2505">Numéro de compte</span><span class="sxs-lookup"><span data-stu-id="fd62e-2505">Account Number</span></span> 
- <span data-ttu-id="fd62e-2506">מספר חשבון בנק</span><span class="sxs-lookup"><span data-stu-id="fd62e-2506">מספר חשבון בנק</span></span> 
   
## <a name="israel-national-id"></a><span data-ttu-id="fd62e-2507">Carte nationale d’identité Israël</span><span class="sxs-lookup"><span data-stu-id="fd62e-2507">Israel National ID</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-2508">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-2508">Format</span></span>

<span data-ttu-id="fd62e-2509">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2509">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-2510">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2510">Pattern</span></span>

<span data-ttu-id="fd62e-2511">Neuf chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="fd62e-2511">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-2512">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2512">Checksum</span></span>

<span data-ttu-id="fd62e-2513">Oui</span><span class="sxs-lookup"><span data-stu-id="fd62e-2513">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-2514">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-2514">Definition</span></span>

<span data-ttu-id="fd62e-2515">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2515">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-2516">La fonction Func_israeli_national_id_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2516">The function Func_israeli_national_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-2517">Un mot clé figurant dans la liste Keyword_Israel_National_ID est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2517">A keyword from Keyword_Israel_National_ID is found.</span></span>
- <span data-ttu-id="fd62e-2518">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2518">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-2519">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-2519">Keywords</span></span>

#### <a name="keyword_israel_national_id"></a><span data-ttu-id="fd62e-2520">Keyword_Israel_National_ID</span><span class="sxs-lookup"><span data-stu-id="fd62e-2520">Keyword_Israel_National_ID</span></span>

- <span data-ttu-id="fd62e-2521">מספר זהות</span><span class="sxs-lookup"><span data-stu-id="fd62e-2521">מספר זהות</span></span> 
- <span data-ttu-id="fd62e-2522">Numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="fd62e-2522">National ID Number</span></span>
   
## <a name="italy-drivers-license-number"></a><span data-ttu-id="fd62e-2523">Numéro de permis de conduire Italie</span><span class="sxs-lookup"><span data-stu-id="fd62e-2523">Italy Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-2524">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-2524">Format</span></span>

<span data-ttu-id="fd62e-2525">Une combinaison de 10 lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2525">A combination of 10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-2526">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2526">Pattern</span></span>

- <span data-ttu-id="fd62e-2527">Une combinaison de 10 lettres et chiffres :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2527">A combination of 10 letters and digits:</span></span>
- <span data-ttu-id="fd62e-2528">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="fd62e-2528">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="fd62e-2529">La lettre « A » ou « V » (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="fd62e-2529">The letter "A" or "V" (not case sensitive)</span></span> 
- <span data-ttu-id="fd62e-2530">Sept lettres (ne respectent pas la casse), des chiffres ou le trait de soulignement</span><span class="sxs-lookup"><span data-stu-id="fd62e-2530">Seven letters (not case sensitive), digits, or the underscore character</span></span> 
- <span data-ttu-id="fd62e-2531">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="fd62e-2531">One letter (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-2532">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2532">Checksum</span></span>

<span data-ttu-id="fd62e-2533">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-2533">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-2534">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-2534">Definition</span></span>

<span data-ttu-id="fd62e-2535">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2535">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-2536">L’expression régulière Regex_italy_drivers_license_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2536">The regular expression Regex_italy_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-2537">Un mot clé figurant dans la liste Keyword_italy_drivers_license_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2537">A keyword from Keyword_italy_drivers_license_number is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-2538">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-2538">Keywords</span></span>

#### <a name="keyword_italy_drivers_license_number"></a><span data-ttu-id="fd62e-2539">Keyword_italy_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="fd62e-2539">Keyword_italy_drivers_license_number</span></span>

- <span data-ttu-id="fd62e-2540">numero di patente di guida</span><span class="sxs-lookup"><span data-stu-id="fd62e-2540">numero di patente di guida</span></span> 
- <span data-ttu-id="fd62e-2541">patente di guida</span><span class="sxs-lookup"><span data-stu-id="fd62e-2541">patente di guida</span></span> 
   
## <a name="japan-bank-account-number"></a><span data-ttu-id="fd62e-2542">Numéro de compte bancaire Japon</span><span class="sxs-lookup"><span data-stu-id="fd62e-2542">Japan Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-2543">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-2543">Format</span></span>

<span data-ttu-id="fd62e-2544">Sept ou huit chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2544">Seven or eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-2545">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2545">Pattern</span></span>

<span data-ttu-id="fd62e-2546">Numéro de compte bancaire :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2546">Bank account number:</span></span>
- <span data-ttu-id="fd62e-2547">Sept ou huit chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2547">Seven or eight digits</span></span>
- <span data-ttu-id="fd62e-2548">Code guichet du compte bancaire :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2548">Bank account branch code:</span></span>
- <span data-ttu-id="fd62e-2549">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2549">Four digits</span></span> 
- <span data-ttu-id="fd62e-2550">Un espace ou un tiret (facultatif)</span><span class="sxs-lookup"><span data-stu-id="fd62e-2550">A space or dash (optional)</span></span> 
- <span data-ttu-id="fd62e-2551">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2551">Three digits</span></span>

<span data-ttu-id="fd62e-2552">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2552">Checksum</span></span>

<span data-ttu-id="fd62e-2553">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-2553">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-2554">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-2554">Definition</span></span>

<span data-ttu-id="fd62e-2555">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2555">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-2556">La fonction Func_jp_bank_account trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2556">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-2557">Un mot clé figurant dans la liste Keyword_jp_bank_account est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2557">A keyword from Keyword_jp_bank_account is found.</span></span>
- <span data-ttu-id="fd62e-2558">L’une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2558">One of the following is true:</span></span>
- <span data-ttu-id="fd62e-2559">La fonction Func_jp_bank_account_branch_code trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2559">The function Func_jp_bank_account_branch_code finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-2560">Un mot clé figurant dans la liste Keyword_jp_bank_branch_code est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2560">A keyword from Keyword_jp_bank_branch_code is found.</span></span>

<span data-ttu-id="fd62e-2561">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2561">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-2562">La fonction Func_jp_bank_account trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2562">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-2563">Un mot clé figurant dans la liste Keyword_jp_bank_account est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2563">A keyword from Keyword_jp_bank_account is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-2564">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-2564">Keywords</span></span>

#### <a name="keyword_jp_bank_account"></a><span data-ttu-id="fd62e-2565">Keyword_jp_bank_account</span><span class="sxs-lookup"><span data-stu-id="fd62e-2565">Keyword_jp_bank_account</span></span>

- <span data-ttu-id="fd62e-2566">Numéro de compte courant</span><span class="sxs-lookup"><span data-stu-id="fd62e-2566">Checking Account Number</span></span> 
- <span data-ttu-id="fd62e-2567">Compte courant</span><span class="sxs-lookup"><span data-stu-id="fd62e-2567">Checking Account</span></span> 
- <span data-ttu-id="fd62e-2568"># compte courant</span><span class="sxs-lookup"><span data-stu-id="fd62e-2568">Checking Account #</span></span> 
- <span data-ttu-id="fd62e-2569">Numéro compte courant</span><span class="sxs-lookup"><span data-stu-id="fd62e-2569">Checking Acct Number</span></span> 
- <span data-ttu-id="fd62e-2570"># compte courant</span><span class="sxs-lookup"><span data-stu-id="fd62e-2570">Checking Acct #</span></span> 
- <span data-ttu-id="fd62e-2571">N° de compte courant</span><span class="sxs-lookup"><span data-stu-id="fd62e-2571">Checking Acct No.</span></span> 
- <span data-ttu-id="fd62e-2572">N° de compte courant</span><span class="sxs-lookup"><span data-stu-id="fd62e-2572">Checking Account No.</span></span> 
- <span data-ttu-id="fd62e-2573">Numéro de compte bancaire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2573">Bank Account Number</span></span> 
- <span data-ttu-id="fd62e-2574">Compte bancaire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2574">Bank Account</span></span> 
- <span data-ttu-id="fd62e-2575"># Compte bancaire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2575">Bank Account #</span></span> 
- <span data-ttu-id="fd62e-2576">Numéro de compte bancaire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2576">Bank Acct Number</span></span> 
- <span data-ttu-id="fd62e-2577"># Compte bancaire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2577">Bank Acct #</span></span> 
- <span data-ttu-id="fd62e-2578">N° de compte bancaire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2578">Bank Acct No.</span></span> 
- <span data-ttu-id="fd62e-2579">N° de compte bancaire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2579">Bank Account No.</span></span> 
- <span data-ttu-id="fd62e-2580">Numéro de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="fd62e-2580">Savings Account Number</span></span> 
- <span data-ttu-id="fd62e-2581">Compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="fd62e-2581">Savings Account</span></span> 
- <span data-ttu-id="fd62e-2582">N° de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="fd62e-2582">Savings Account #</span></span> 
- <span data-ttu-id="fd62e-2583">Numéro de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="fd62e-2583">Savings Acct Number</span></span> 
- <span data-ttu-id="fd62e-2584"># compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="fd62e-2584">Savings Acct #</span></span> 
- <span data-ttu-id="fd62e-2585">N° de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="fd62e-2585">Savings Acct No.</span></span> 
- <span data-ttu-id="fd62e-2586">N° de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="fd62e-2586">Savings Account No.</span></span> 
- <span data-ttu-id="fd62e-2587">Numéro de compte de débit</span><span class="sxs-lookup"><span data-stu-id="fd62e-2587">Debit Account Number</span></span> 
- <span data-ttu-id="fd62e-2588">Compte de débit</span><span class="sxs-lookup"><span data-stu-id="fd62e-2588">Debit Account</span></span> 
- <span data-ttu-id="fd62e-2589"># Compte de débit</span><span class="sxs-lookup"><span data-stu-id="fd62e-2589">Debit Account #</span></span> 
- <span data-ttu-id="fd62e-2590">Numéro de compte de débit</span><span class="sxs-lookup"><span data-stu-id="fd62e-2590">Debit Acct Number</span></span> 
- <span data-ttu-id="fd62e-2591"># Compte de débit</span><span class="sxs-lookup"><span data-stu-id="fd62e-2591">Debit Acct #</span></span> 
- <span data-ttu-id="fd62e-2592">N° de compte de débit</span><span class="sxs-lookup"><span data-stu-id="fd62e-2592">Debit Acct No.</span></span> 
- <span data-ttu-id="fd62e-2593">N° de compte de débit</span><span class="sxs-lookup"><span data-stu-id="fd62e-2593">Debit Account No.</span></span> 
- <span data-ttu-id="fd62e-2594">口座番号を当座預金口座の確認</span><span class="sxs-lookup"><span data-stu-id="fd62e-2594">口座番号を当座預金口座の確認</span></span> 
- <span data-ttu-id="fd62e-2595">#アカウントの確認 、 勘定番号の確認</span><span class="sxs-lookup"><span data-stu-id="fd62e-2595">＃アカウントの確認、勘定番号の確認</span></span> 
- <span data-ttu-id="fd62e-2596">#勘定の確認</span><span class="sxs-lookup"><span data-stu-id="fd62e-2596">＃勘定の確認</span></span> 
- <span data-ttu-id="fd62e-2597">勘定番号の確認</span><span class="sxs-lookup"><span data-stu-id="fd62e-2597">勘定番号の確認</span></span> 
- <span data-ttu-id="fd62e-2598">口座番号の確認</span><span class="sxs-lookup"><span data-stu-id="fd62e-2598">口座番号の確認</span></span> 
- <span data-ttu-id="fd62e-2599">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="fd62e-2599">銀行口座番号</span></span> 
- <span data-ttu-id="fd62e-2600">銀行口座</span><span class="sxs-lookup"><span data-stu-id="fd62e-2600">銀行口座</span></span> 
- <span data-ttu-id="fd62e-2601">銀行口座＃</span><span class="sxs-lookup"><span data-stu-id="fd62e-2601">銀行口座＃</span></span> 
- <span data-ttu-id="fd62e-2602">銀行の勘定番号</span><span class="sxs-lookup"><span data-stu-id="fd62e-2602">銀行の勘定番号</span></span> 
- <span data-ttu-id="fd62e-2603">銀行のacct＃</span><span class="sxs-lookup"><span data-stu-id="fd62e-2603">銀行のacct＃</span></span> 
- <span data-ttu-id="fd62e-2604">銀行の勘定いいえ</span><span class="sxs-lookup"><span data-stu-id="fd62e-2604">銀行の勘定いいえ</span></span> 
- <span data-ttu-id="fd62e-2605">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="fd62e-2605">銀行口座番号</span></span>
- <span data-ttu-id="fd62e-2606">普通預金口座番号</span><span class="sxs-lookup"><span data-stu-id="fd62e-2606">普通預金口座番号</span></span> 
- <span data-ttu-id="fd62e-2607">預金口座</span><span class="sxs-lookup"><span data-stu-id="fd62e-2607">預金口座</span></span> 
- <span data-ttu-id="fd62e-2608">貯蓄口座＃</span><span class="sxs-lookup"><span data-stu-id="fd62e-2608">貯蓄口座＃</span></span> 
- <span data-ttu-id="fd62e-2609">貯蓄勘定の数</span><span class="sxs-lookup"><span data-stu-id="fd62e-2609">貯蓄勘定の数</span></span> 
- <span data-ttu-id="fd62e-2610">貯蓄勘定＃</span><span class="sxs-lookup"><span data-stu-id="fd62e-2610">貯蓄勘定＃</span></span> 
- <span data-ttu-id="fd62e-2611">貯蓄勘定番号</span><span class="sxs-lookup"><span data-stu-id="fd62e-2611">貯蓄勘定番号</span></span> 
- <span data-ttu-id="fd62e-2612">普通預金口座番号</span><span class="sxs-lookup"><span data-stu-id="fd62e-2612">普通預金口座番号</span></span> 
- <span data-ttu-id="fd62e-2613">引き落とし口座番号</span><span class="sxs-lookup"><span data-stu-id="fd62e-2613">引き落とし口座番号</span></span> 
- <span data-ttu-id="fd62e-2614">口座番号</span><span class="sxs-lookup"><span data-stu-id="fd62e-2614">口座番号</span></span> 
- <span data-ttu-id="fd62e-2615">口座番号＃</span><span class="sxs-lookup"><span data-stu-id="fd62e-2615">口座番号＃</span></span> 
- <span data-ttu-id="fd62e-2616">デビットのacct番号</span><span class="sxs-lookup"><span data-stu-id="fd62e-2616">デビットのacct番号</span></span> 
- <span data-ttu-id="fd62e-2617">デビット勘定＃</span><span class="sxs-lookup"><span data-stu-id="fd62e-2617">デビット勘定＃</span></span> 
- <span data-ttu-id="fd62e-2618">デビットACCTの番号</span><span class="sxs-lookup"><span data-stu-id="fd62e-2618">デビットACCTの番号</span></span> 
- <span data-ttu-id="fd62e-2619">デビット口座番号</span><span class="sxs-lookup"><span data-stu-id="fd62e-2619">デビット口座番号</span></span> 

#### <a name="keyword_jp_bank_branch_code"></a><span data-ttu-id="fd62e-2620">Keyword_jp_bank_branch_code</span><span class="sxs-lookup"><span data-stu-id="fd62e-2620">Keyword_jp_bank_branch_code</span></span>

<span data-ttu-id="fd62e-2621">Otemachi</span><span class="sxs-lookup"><span data-stu-id="fd62e-2621">Otemachi</span></span>

## <a name="japan-drivers-license-number"></a><span data-ttu-id="fd62e-2622">Numéro de permis de conduire Japon</span><span class="sxs-lookup"><span data-stu-id="fd62e-2622">Japan Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-2623">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-2623">Format</span></span>

<span data-ttu-id="fd62e-2624">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2624">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-2625">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2625">Pattern</span></span>

<span data-ttu-id="fd62e-2626">12 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="fd62e-2626">12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-2627">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2627">Checksum</span></span>

<span data-ttu-id="fd62e-2628">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-2628">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-2629">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-2629">Definition</span></span>

<span data-ttu-id="fd62e-2630">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2630">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-2631">La fonction Func_jp_drivers_license_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2631">The function Func_jp_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-2632">Un mot clé figurant dans la liste Keyword_jp_drivers_license_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2632">A keyword from Keyword_jp_drivers_license_number is found.</span></span>

```xml
<!-- Japan Driver's License Number -->
<Entity id="c6011143-d087-451c-8313-7f6d4aed2270" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_drivers_license_number" />
        <Match idRef ="Keyword_jp_drivers_license_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fd62e-2633">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-2633">Keywords</span></span>

#### <a name="keyword_jp_drivers_license_number"></a><span data-ttu-id="fd62e-2634">Keyword_jp_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="fd62e-2634">Keyword_jp_drivers_license_number</span></span>

- <span data-ttu-id="fd62e-2635">LD #</span><span class="sxs-lookup"><span data-stu-id="fd62e-2635">dl#</span></span> 
- <span data-ttu-id="fd62e-2636">LD</span><span class="sxs-lookup"><span data-stu-id="fd62e-2636">DL＃</span></span> 
- <span data-ttu-id="fd62e-2637">distribution #</span><span class="sxs-lookup"><span data-stu-id="fd62e-2637">dls#</span></span> 
- <span data-ttu-id="fd62e-2638">DISTRIBUTION</span><span class="sxs-lookup"><span data-stu-id="fd62e-2638">DLS＃</span></span> 
- <span data-ttu-id="fd62e-2639">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2639">driver license</span></span> 
- <span data-ttu-id="fd62e-2640">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2640">driver licenses</span></span> 
- <span data-ttu-id="fd62e-2641">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2641">drivers license</span></span> 
- <span data-ttu-id="fd62e-2642">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2642">driver's license</span></span> 
- <span data-ttu-id="fd62e-2643">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2643">drivers licenses</span></span> 
- <span data-ttu-id="fd62e-2644">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2644">driver's licenses</span></span> 
- <span data-ttu-id="fd62e-2645">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-2645">driving licence</span></span> 
- <span data-ttu-id="fd62e-2646">Profil #</span><span class="sxs-lookup"><span data-stu-id="fd62e-2646">lic#</span></span> 
- <span data-ttu-id="fd62e-2647">Profil</span><span class="sxs-lookup"><span data-stu-id="fd62e-2647">LIC＃</span></span> 
- <span data-ttu-id="fd62e-2648">conduire #</span><span class="sxs-lookup"><span data-stu-id="fd62e-2648">lics#</span></span> 
- <span data-ttu-id="fd62e-2649">id d’état</span><span class="sxs-lookup"><span data-stu-id="fd62e-2649">state id</span></span> 
- <span data-ttu-id="fd62e-2650">identification d’état</span><span class="sxs-lookup"><span data-stu-id="fd62e-2650">state identification</span></span> 
- <span data-ttu-id="fd62e-2651">numéro d’identification d’état</span><span class="sxs-lookup"><span data-stu-id="fd62e-2651">state identification number</span></span> 
- <span data-ttu-id="fd62e-2652">低所得国＃</span><span class="sxs-lookup"><span data-stu-id="fd62e-2652">低所得国＃</span></span> 
- <span data-ttu-id="fd62e-2653">免許証</span><span class="sxs-lookup"><span data-stu-id="fd62e-2653">免許証</span></span> 
- <span data-ttu-id="fd62e-2654">状態ID</span><span class="sxs-lookup"><span data-stu-id="fd62e-2654">状態ID</span></span>
- <span data-ttu-id="fd62e-2655">状態の識別</span><span class="sxs-lookup"><span data-stu-id="fd62e-2655">状態の識別</span></span> 
- <span data-ttu-id="fd62e-2656">状態の識別番号</span><span class="sxs-lookup"><span data-stu-id="fd62e-2656">状態の識別番号</span></span> 
- <span data-ttu-id="fd62e-2657">運転免許</span><span class="sxs-lookup"><span data-stu-id="fd62e-2657">運転免許</span></span> 
- <span data-ttu-id="fd62e-2658">運転免許証</span><span class="sxs-lookup"><span data-stu-id="fd62e-2658">運転免許証</span></span> 
- <span data-ttu-id="fd62e-2659">運転免許証番号</span><span class="sxs-lookup"><span data-stu-id="fd62e-2659">運転免許証番号</span></span> 
   
## <a name="japan-passport-number"></a><span data-ttu-id="fd62e-2660">Numéro de passeport Japon</span><span class="sxs-lookup"><span data-stu-id="fd62e-2660">Japan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-2661">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-2661">Format</span></span>

<span data-ttu-id="fd62e-2662">Deux lettres suivies de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2662">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-2663">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2663">Pattern</span></span>

<span data-ttu-id="fd62e-2664">Deux lettres (ne respectant pas la casse) suivies de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2664">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-2665">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2665">Checksum</span></span>

<span data-ttu-id="fd62e-2666">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-2666">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-2667">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-2667">Definition</span></span>

<span data-ttu-id="fd62e-2668">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2668">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-2669">La fonction Func_jp_passport trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2669">The function Func_jp_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-2670">Un mot clé figurant dans la liste Keyword_jp_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2670">A keyword from Keyword_jp_passport is found.</span></span>

```xml
<!-- Japan Passport Number -->
<Entity id="75177310-1a09-4613-bf6d-833aae3743f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_passport" />
        <Match idRef="Keyword_jp_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fd62e-2671">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-2671">Keywords</span></span>

#### <a name="keyword_jp_passport"></a><span data-ttu-id="fd62e-2672">Keyword_jp_passport</span><span class="sxs-lookup"><span data-stu-id="fd62e-2672">Keyword_jp_passport</span></span>

- <span data-ttu-id="fd62e-2673">パスポート</span><span class="sxs-lookup"><span data-stu-id="fd62e-2673">パスポート</span></span> 
- <span data-ttu-id="fd62e-2674">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="fd62e-2674">パスポート番号</span></span> 
- <span data-ttu-id="fd62e-2675">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="fd62e-2675">パスポートのNum</span></span> 
- <span data-ttu-id="fd62e-2676">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="fd62e-2676">パスポート＃</span></span> 
   
## <a name="japan-resident-registration-number"></a><span data-ttu-id="fd62e-2677">Matricule de résident Japon</span><span class="sxs-lookup"><span data-stu-id="fd62e-2677">Japan Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-2678">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-2678">Format</span></span>

<span data-ttu-id="fd62e-2679">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2679">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-2680">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2680">Pattern</span></span>

<span data-ttu-id="fd62e-2681">11 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="fd62e-2681">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-2682">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2682">Checksum</span></span>

<span data-ttu-id="fd62e-2683">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-2683">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-2684">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-2684">Definition</span></span>

<span data-ttu-id="fd62e-2685">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2685">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-2686">La fonction Func_jp_resident_registration_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2686">The function Func_jp_resident_registration_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-2687">Un mot clé figurant dans la liste Keyword_jp_resident_registration_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2687">A keyword from Keyword_jp_resident_registration_number is found.</span></span>

```xml
<!-- Japan Resident Registration Number -->
<Entity id="01c1209b-6389-4faf-a5f8-3f7e13899652" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_resident_registration_number" />
        <Match idRef ="Keyword_jp_resident_registration_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fd62e-2688">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-2688">Keywords</span></span>

#### <a name="keyword_jp_resident_registration_number"></a><span data-ttu-id="fd62e-2689">Keyword_jp_resident_registration_number</span><span class="sxs-lookup"><span data-stu-id="fd62e-2689">Keyword_jp_resident_registration_number</span></span>

- <span data-ttu-id="fd62e-2690">Numéro d’enregistrement du résident</span><span class="sxs-lookup"><span data-stu-id="fd62e-2690">Resident Registration Number</span></span>
- <span data-ttu-id="fd62e-2691">Numéro d’enregistrement du résident</span><span class="sxs-lookup"><span data-stu-id="fd62e-2691">Resident Register Number</span></span> 
- <span data-ttu-id="fd62e-2692">Numéro de base d’enregistrement des résidents</span><span class="sxs-lookup"><span data-stu-id="fd62e-2692">Residents Basic Registry Number</span></span> 
- <span data-ttu-id="fd62e-2693">N° d’enregistrement du résident</span><span class="sxs-lookup"><span data-stu-id="fd62e-2693">Resident Registration No.</span></span> 
- <span data-ttu-id="fd62e-2694">N° d’enregistrement du résident</span><span class="sxs-lookup"><span data-stu-id="fd62e-2694">Resident Register No.</span></span> 
- <span data-ttu-id="fd62e-2695">N° de base d’enregistrement des résidents</span><span class="sxs-lookup"><span data-stu-id="fd62e-2695">Residents Basic Registry No.</span></span> 
- <span data-ttu-id="fd62e-2696">N° d’enregistrement du résident de base</span><span class="sxs-lookup"><span data-stu-id="fd62e-2696">Basic Resident Register No.</span></span> 
- <span data-ttu-id="fd62e-2697">住民登録番号、登録番号をレジデント</span><span class="sxs-lookup"><span data-stu-id="fd62e-2697">住民登録番号、登録番号をレジデント</span></span> 
- <span data-ttu-id="fd62e-2698">住民基本登録番号、登録番号</span><span class="sxs-lookup"><span data-stu-id="fd62e-2698">住民基本登録番号、登録番号</span></span> 
- <span data-ttu-id="fd62e-2699">住民基本レジストリ番号を常駐</span><span class="sxs-lookup"><span data-stu-id="fd62e-2699">住民基本レジストリ番号を常駐</span></span> 
- <span data-ttu-id="fd62e-2700">登録番号を常駐住民基本台帳登録番号</span><span class="sxs-lookup"><span data-stu-id="fd62e-2700">登録番号を常駐住民基本台帳登録番号</span></span> 

   
## <a name="japan-social-insurance-number-sin"></a><span data-ttu-id="fd62e-2701">Numéro d’assurance sociale Japon</span><span class="sxs-lookup"><span data-stu-id="fd62e-2701">Japan Social Insurance Number (SIN)</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-2702">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-2702">Format</span></span>

<span data-ttu-id="fd62e-2703">7 à 12 chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2703">7-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-2704">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2704">Pattern</span></span>

<span data-ttu-id="fd62e-2705">7 à 12 chiffres :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2705">7-12 digits:</span></span>
- <span data-ttu-id="fd62e-2706">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2706">Four digits</span></span> 
- <span data-ttu-id="fd62e-2707">Un trait d’union (facultatif)</span><span class="sxs-lookup"><span data-stu-id="fd62e-2707">A hyphen (optional)</span></span> 
- <span data-ttu-id="fd62e-2708">Six chiffres ou</span><span class="sxs-lookup"><span data-stu-id="fd62e-2708">Six digits OR</span></span>
- <span data-ttu-id="fd62e-2709">7 à 12 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="fd62e-2709">7-12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-2710">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2710">Checksum</span></span>

<span data-ttu-id="fd62e-2711">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-2711">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-2712">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-2712">Definition</span></span>

<span data-ttu-id="fd62e-2713">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2713">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-2714">La fonction Func_jp_sin trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2714">The function Func_jp_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-2715">Un mot clé figurant dans la liste Keyword_jp_sin est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2715">A keyword from Keyword_jp_sin is found.</span></span>

<span data-ttu-id="fd62e-2716">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2716">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-2717">La fonction Func_jp_sin_pre_1997 trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2717">The function Func_jp_sin_pre_1997 finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-2718">Un mot clé figurant dans la liste Keyword_jp_sin est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2718">A keyword from Keyword_jp_sin is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-2719">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-2719">Keywords</span></span>

#### <a name="keyword_jp_sin"></a><span data-ttu-id="fd62e-2720">Keyword_jp_sin</span><span class="sxs-lookup"><span data-stu-id="fd62e-2720">Keyword_jp_sin</span></span>

- <span data-ttu-id="fd62e-2721">N° d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="fd62e-2721">Social Insurance No.</span></span> 
- <span data-ttu-id="fd62e-2722">Numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="fd62e-2722">Social Insurance Num</span></span> 
- <span data-ttu-id="fd62e-2723">Numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="fd62e-2723">Social Insurance Number</span></span> 
- <span data-ttu-id="fd62e-2724">社会保険のテンキー</span><span class="sxs-lookup"><span data-stu-id="fd62e-2724">社会保険のテンキー</span></span> 
- <span data-ttu-id="fd62e-2725">社会保険番号</span><span class="sxs-lookup"><span data-stu-id="fd62e-2725">社会保険番号</span></span> 

## <a name="japanese-residence-card-number"></a><span data-ttu-id="fd62e-2726">Numéro de carte de séjour japonaise</span><span class="sxs-lookup"><span data-stu-id="fd62e-2726">Japanese Residence Card Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-2727">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-2727">Format</span></span>

<span data-ttu-id="fd62e-2728">12 lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2728">12 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-2729">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2729">Pattern</span></span>

<span data-ttu-id="fd62e-2730">12 lettres et chiffres:</span><span class="sxs-lookup"><span data-stu-id="fd62e-2730">12 letters and digits:</span></span>
- <span data-ttu-id="fd62e-2731">Deux lettres (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="fd62e-2731">Two letters (not case sensitive)</span></span>
- <span data-ttu-id="fd62e-2732">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2732">Eight digits</span></span> 
- <span data-ttu-id="fd62e-2733">Deux lettres (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="fd62e-2733">Two letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-2734">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2734">Checksum</span></span>

<span data-ttu-id="fd62e-2735">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-2735">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-2736">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-2736">Definition</span></span>

<span data-ttu-id="fd62e-2737">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2737">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-2738">L’expression régulière Regex_jp_residence_card_number trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2738">The regular expression Regex_jp_residence_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-2739">Un mot clé depuis Keyword_jp_residence_card_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2739">A keyword from Keyword_jp_residence_card_number is found.</span></span>

```xml
<!--Japan Residence Card Number-->
-<Entity id="ac36fef2-a289-4e2c-bb48-b02366e89fc0" recommendedConfidence="75" patternsProximity="300">
   -<Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_jp_residence_card_number"/>
      <Match idRef="Keyword_jp_residence_card_number"/>
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fd62e-2740">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-2740">Keywords</span></span>

#### <a name="keyword_jp_residence_card_number"></a><span data-ttu-id="fd62e-2741">Keyword_jp_residence_card_number</span><span class="sxs-lookup"><span data-stu-id="fd62e-2741">Keyword_jp_residence_card_number</span></span>

- <span data-ttu-id="fd62e-2742">Numéro de carte de séjour</span><span class="sxs-lookup"><span data-stu-id="fd62e-2742">Residence card number</span></span>
- <span data-ttu-id="fd62e-2743">N ° carte de séjour</span><span class="sxs-lookup"><span data-stu-id="fd62e-2743">Residence card no</span></span>
- <span data-ttu-id="fd62e-2744">Carte de séjour #</span><span class="sxs-lookup"><span data-stu-id="fd62e-2744">Residence card #</span></span>
- <span data-ttu-id="fd62e-2745">在留カード番号</span><span class="sxs-lookup"><span data-stu-id="fd62e-2745">在留カード番号</span></span>
   
## <a name="malaysia-id-card-number"></a><span data-ttu-id="fd62e-2746">Numéro de carte d’identité Malaisie</span><span class="sxs-lookup"><span data-stu-id="fd62e-2746">Malaysia ID Card Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-2747">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-2747">Format</span></span>

<span data-ttu-id="fd62e-2748">12 chiffres contenant éventuellement des traits d’union</span><span class="sxs-lookup"><span data-stu-id="fd62e-2748">12 digits containing optional hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-2749">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2749">Pattern</span></span>

<span data-ttu-id="fd62e-2750">12 chiffres :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2750">12 digits:</span></span>
- <span data-ttu-id="fd62e-2751">Six chiffres au format AAMMJJ correspondant à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="fd62e-2751">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="fd62e-2752">Un tiret (facultatif) </span><span class="sxs-lookup"><span data-stu-id="fd62e-2752">A dash (optional)</span></span> 
- <span data-ttu-id="fd62e-2753">Le code à deux lettres du lieu de naissance </span><span class="sxs-lookup"><span data-stu-id="fd62e-2753">Two-letter place-of-birth code</span></span> 
- <span data-ttu-id="fd62e-2754">Un tiret (facultatif) </span><span class="sxs-lookup"><span data-stu-id="fd62e-2754">A dash (optional)</span></span> 
- <span data-ttu-id="fd62e-2755">Trois chiffres aléatoires </span><span class="sxs-lookup"><span data-stu-id="fd62e-2755">Three random digits</span></span> 
- <span data-ttu-id="fd62e-2756">Code de sexe à un chiffre</span><span class="sxs-lookup"><span data-stu-id="fd62e-2756">One-digit gender code</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-2757">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2757">Checksum</span></span>

<span data-ttu-id="fd62e-2758">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-2758">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-2759">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-2759">Definition</span></span>

<span data-ttu-id="fd62e-2760">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2760">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-2761">L’expression régulière Regex_malaysia_id_card_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2761">The regular expression Regex_malaysia_id_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-2762">Un mot clé figurant dans la liste Keyword_malaysia_id_card_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2762">A keyword from Keyword_malaysia_id_card_number is found.</span></span>

```xml
<!-- Malaysia ID Card Number -->
</Entity>
      <Entity id="7f0e921c-9677-435b-aba2-bb8f1013c749" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
            <IdMatch idRef="Regex_malaysia_id_card_number" />
            <Match idRef="Keyword_malaysia_id_card_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fd62e-2763">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-2763">Keywords</span></span>
   
#### <a name="keyword_malaysia_id_card_number"></a><span data-ttu-id="fd62e-2764">Keyword_malaysia_id_card_number</span><span class="sxs-lookup"><span data-stu-id="fd62e-2764">Keyword_malaysia_id_card_number</span></span>

- <span data-ttu-id="fd62e-2765">carte d’application numérique</span><span class="sxs-lookup"><span data-stu-id="fd62e-2765">digital application card</span></span>
- <span data-ttu-id="fd62e-2766">i/c</span><span class="sxs-lookup"><span data-stu-id="fd62e-2766">i/c</span></span>
- <span data-ttu-id="fd62e-2767">n ° i/c non</span><span class="sxs-lookup"><span data-stu-id="fd62e-2767">i/c no</span></span>
- <span data-ttu-id="fd62e-2768">combustion</span><span class="sxs-lookup"><span data-stu-id="fd62e-2768">ic</span></span>
- <span data-ttu-id="fd62e-2769">n ° IC</span><span class="sxs-lookup"><span data-stu-id="fd62e-2769">ic no</span></span>
- <span data-ttu-id="fd62e-2770">carte d’identité</span><span class="sxs-lookup"><span data-stu-id="fd62e-2770">id card</span></span>
- <span data-ttu-id="fd62e-2771">Carte d’identification</span><span class="sxs-lookup"><span data-stu-id="fd62e-2771">identification Card</span></span>
- <span data-ttu-id="fd62e-2772">Carte d’identité</span><span class="sxs-lookup"><span data-stu-id="fd62e-2772">identity card</span></span>
- <span data-ttu-id="fd62e-2773">k/p</span><span class="sxs-lookup"><span data-stu-id="fd62e-2773">k/p</span></span>
- <span data-ttu-id="fd62e-2774">n ° k/p</span><span class="sxs-lookup"><span data-stu-id="fd62e-2774">k/p no</span></span>
- <span data-ttu-id="fd62e-2775">kad akuan diri</span><span class="sxs-lookup"><span data-stu-id="fd62e-2775">kad akuan diri</span></span>
- <span data-ttu-id="fd62e-2776">Kad aplikasi numérique</span><span class="sxs-lookup"><span data-stu-id="fd62e-2776">kad aplikasi digital</span></span>
- <span data-ttu-id="fd62e-2777">Kad Pengenalan Malaisie</span><span class="sxs-lookup"><span data-stu-id="fd62e-2777">kad pengenalan malaysia</span></span>
- <span data-ttu-id="fd62e-2778">kgf</span><span class="sxs-lookup"><span data-stu-id="fd62e-2778">kp</span></span>
- <span data-ttu-id="fd62e-2779">KP non</span><span class="sxs-lookup"><span data-stu-id="fd62e-2779">kp no</span></span>
- <span data-ttu-id="fd62e-2780">mykad</span><span class="sxs-lookup"><span data-stu-id="fd62e-2780">mykad</span></span>
- <span data-ttu-id="fd62e-2781">mykas</span><span class="sxs-lookup"><span data-stu-id="fd62e-2781">mykas</span></span>
- <span data-ttu-id="fd62e-2782">mykid</span><span class="sxs-lookup"><span data-stu-id="fd62e-2782">mykid</span></span>
- <span data-ttu-id="fd62e-2783">mypr</span><span class="sxs-lookup"><span data-stu-id="fd62e-2783">mypr</span></span>
- <span data-ttu-id="fd62e-2784">mytentera</span><span class="sxs-lookup"><span data-stu-id="fd62e-2784">mytentera</span></span>
- <span data-ttu-id="fd62e-2785">carte d’identité Malaisie</span><span class="sxs-lookup"><span data-stu-id="fd62e-2785">malaysia identity card</span></span>
- <span data-ttu-id="fd62e-2786">carte d’identité malais</span><span class="sxs-lookup"><span data-stu-id="fd62e-2786">malaysian identity card</span></span>
- <span data-ttu-id="fd62e-2787">NRIC</span><span class="sxs-lookup"><span data-stu-id="fd62e-2787">nric</span></span>
- <span data-ttu-id="fd62e-2788">carte d’identification personnelle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2788">personal identification card</span></span>
   
## <a name="netherlands-citizens-service-bsn-number"></a><span data-ttu-id="fd62e-2789">Numéro de service du citoyen (BSN) Pays-Bas</span><span class="sxs-lookup"><span data-stu-id="fd62e-2789">Netherlands Citizen's Service (BSN) Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-2790">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-2790">Format</span></span>

<span data-ttu-id="fd62e-2791">8 à 9 chiffres contenant éventuellement des espaces</span><span class="sxs-lookup"><span data-stu-id="fd62e-2791">8-9 digits containing optional spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-2792">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2792">Pattern</span></span>

<span data-ttu-id="fd62e-2793">8 à 9 chiffres :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2793">8-9 digits:</span></span>
- <span data-ttu-id="fd62e-2794">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2794">Three digits</span></span> 
- <span data-ttu-id="fd62e-2795">Un espace (facultatif) </span><span class="sxs-lookup"><span data-stu-id="fd62e-2795">A space (optional)</span></span> 
- <span data-ttu-id="fd62e-2796">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2796">Three digits</span></span> 
- <span data-ttu-id="fd62e-2797">Un espace (facultatif) </span><span class="sxs-lookup"><span data-stu-id="fd62e-2797">A space (optional)</span></span> 
- <span data-ttu-id="fd62e-2798">2 à 3 chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2798">2-3 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-2799">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2799">Checksum</span></span>

<span data-ttu-id="fd62e-2800">Oui</span><span class="sxs-lookup"><span data-stu-id="fd62e-2800">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-2801">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-2801">Definition</span></span>

<span data-ttu-id="fd62e-2802">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2802">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-2803">La fonction Func_netherlands_bsn trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2803">The function Func_netherlands_bsn finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-2804">Un mot clé figurant dans la liste Keyword_netherlands_bsn est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2804">A keyword from Keyword_netherlands_bsn is found.</span></span>
- <span data-ttu-id="fd62e-2805">La fonction Func_eu_date2 trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2805">The function Func_eu_date2 finds a date in the right date format.</span></span>
- <span data-ttu-id="fd62e-2806">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2806">The checksum passes.</span></span>

```xml
<!-- Netherlands Citizen's Service (BSN) Number -->
<Entity id="c5f54253-ef7e-44f6-a578-440ed67e946d" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
       <IdMatch idRef="Func_netherlands_bsn" /> 
       <Match idRef="Keyword_netherlands_bsn" /> 
       <Match idRef="Func_eu_date2" /> 
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fd62e-2807">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-2807">Keywords</span></span>

#### <a name="keyword_netherlands_bsn"></a><span data-ttu-id="fd62e-2808">Keyword_netherlands_bsn</span><span class="sxs-lookup"><span data-stu-id="fd62e-2808">Keyword_netherlands_bsn</span></span>

- <span data-ttu-id="fd62e-2809">Citizen service number</span><span class="sxs-lookup"><span data-stu-id="fd62e-2809">Citizen service number</span></span> 
- <span data-ttu-id="fd62e-2810">BSN</span><span class="sxs-lookup"><span data-stu-id="fd62e-2810">BSN</span></span> 
- <span data-ttu-id="fd62e-2811">Burgerservicenummer</span><span class="sxs-lookup"><span data-stu-id="fd62e-2811">Burgerservicenummer</span></span> 
- <span data-ttu-id="fd62e-2812">Sofinummer</span><span class="sxs-lookup"><span data-stu-id="fd62e-2812">Sofinummer</span></span> 
- <span data-ttu-id="fd62e-2813">Persoonsgebonden nummer</span><span class="sxs-lookup"><span data-stu-id="fd62e-2813">Persoonsgebonden nummer</span></span> 
- <span data-ttu-id="fd62e-2814">Persoonsnummer</span><span class="sxs-lookup"><span data-stu-id="fd62e-2814">Persoonsnummer</span></span>    

   
## <a name="new-zealand-ministry-of-health-number"></a><span data-ttu-id="fd62e-2815">Numéro du Ministère de la santé Nouvelle-Zélande</span><span class="sxs-lookup"><span data-stu-id="fd62e-2815">New Zealand Ministry of Health Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-2816">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-2816">Format</span></span>

<span data-ttu-id="fd62e-2817">Trois lettres, un espace (facultatif) et quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2817">Three letters, a space (optional), and four digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-2818">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2818">Pattern</span></span>

<span data-ttu-id="fd62e-2819">Trois lettres (ne respectant pas la casse) un espace (facultatif) quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2819">Three letters (not case sensitive) a space (optional) four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-2820">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2820">Checksum</span></span>

<span data-ttu-id="fd62e-2821">Oui</span><span class="sxs-lookup"><span data-stu-id="fd62e-2821">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-2822">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-2822">Definition</span></span>

<span data-ttu-id="fd62e-2823">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2823">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-2824">La fonction Func_new_zealand_ministry_of_health_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2824">The function Func_new_zealand_ministry_of_health_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-2825">Un mot clé figurant dans la liste Keyword_nz_terms est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2825">A keyword from Keyword_nz_terms is found.</span></span>
- <span data-ttu-id="fd62e-2826">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2826">The checksum passes.</span></span>

```xml
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

<span data-ttu-id="fd62e-2827">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-2827">Keywords</span></span>

<span data-ttu-id="fd62e-2828">Keyword_nz_terms</span><span class="sxs-lookup"><span data-stu-id="fd62e-2828">Keyword_nz_terms</span></span>

- <span data-ttu-id="fd62e-2829">NHI</span><span class="sxs-lookup"><span data-stu-id="fd62e-2829">NHI</span></span> 
- <span data-ttu-id="fd62e-2830">Nouvelle-Zélande</span><span class="sxs-lookup"><span data-stu-id="fd62e-2830">New Zealand</span></span> 
- <span data-ttu-id="fd62e-2831">Intégrité</span><span class="sxs-lookup"><span data-stu-id="fd62e-2831">Health</span></span> 
- <span data-ttu-id="fd62e-2832">destinations</span><span class="sxs-lookup"><span data-stu-id="fd62e-2832">treatment</span></span> 
   
## <a name="norway-identification-number"></a><span data-ttu-id="fd62e-2833">Numéro d’identification Norvège</span><span class="sxs-lookup"><span data-stu-id="fd62e-2833">Norway Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-2834">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-2834">Format</span></span>

<span data-ttu-id="fd62e-2835">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2835">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-2836">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2836">Pattern</span></span>

<span data-ttu-id="fd62e-2837">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2837">11 digits:</span></span>
- <span data-ttu-id="fd62e-2838">Six chiffres au format JJMMAA qui correspondent à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="fd62e-2838">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="fd62e-2839">Numéro individuel à trois chiffres </span><span class="sxs-lookup"><span data-stu-id="fd62e-2839">Three-digit individual number</span></span> 
- <span data-ttu-id="fd62e-2840">Deux chiffres de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2840">Two check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-2841">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2841">Checksum</span></span>

<span data-ttu-id="fd62e-2842">Oui</span><span class="sxs-lookup"><span data-stu-id="fd62e-2842">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-2843">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-2843">Definition</span></span>

<span data-ttu-id="fd62e-2844">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2844">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-2845">La fonction Func_norway_id_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2845">The function Func_norway_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-2846">Un mot clé figurant dans la liste Keyword_norway_id_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2846">A keyword from Keyword_norway_id_number is found.</span></span>
- <span data-ttu-id="fd62e-2847">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2847">The checksum passes.</span></span>
- <span data-ttu-id="fd62e-2848">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2848">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-2849">La fonction Func_norway_id_numbe trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2849">The function Func_norway_id_numbe finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-2850">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2850">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-2851">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-2851">Keywords</span></span>

#### <a name="keyword_norway_id_number"></a><span data-ttu-id="fd62e-2852">Keyword_norway_id_number</span><span class="sxs-lookup"><span data-stu-id="fd62e-2852">Keyword_norway_id_number</span></span>

- <span data-ttu-id="fd62e-2853">Personal identification number</span><span class="sxs-lookup"><span data-stu-id="fd62e-2853">Personal identification number</span></span>
- <span data-ttu-id="fd62e-2854">Norwegian ID Number</span><span class="sxs-lookup"><span data-stu-id="fd62e-2854">Norwegian ID Number</span></span>
- <span data-ttu-id="fd62e-2855">ID Number</span><span class="sxs-lookup"><span data-stu-id="fd62e-2855">ID Number</span></span>
- <span data-ttu-id="fd62e-2856">Identificateur</span><span class="sxs-lookup"><span data-stu-id="fd62e-2856">Identification</span></span>
- <span data-ttu-id="fd62e-2857">Personnummer</span><span class="sxs-lookup"><span data-stu-id="fd62e-2857">Personnummer</span></span>
- <span data-ttu-id="fd62e-2858">Fødselsnummer</span><span class="sxs-lookup"><span data-stu-id="fd62e-2858">Fødselsnummer</span></span>

   
## <a name="philippines-unified-multi-purpose-id-number"></a><span data-ttu-id="fd62e-2859">Numéro d’identification multifonction unifié Philippines</span><span class="sxs-lookup"><span data-stu-id="fd62e-2859">Philippines Unified Multi-Purpose ID Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-2860">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-2860">Format</span></span>

<span data-ttu-id="fd62e-2861">12 chiffres séparés par des traits d’union</span><span class="sxs-lookup"><span data-stu-id="fd62e-2861">12 digits separated by hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-2862">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2862">Pattern</span></span>

<span data-ttu-id="fd62e-2863">12 chiffres :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2863">12 digits:</span></span>
- <span data-ttu-id="fd62e-2864">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2864">Four digits</span></span> 
- <span data-ttu-id="fd62e-2865">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="fd62e-2865">A hyphen</span></span> 
- <span data-ttu-id="fd62e-2866">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="fd62e-2866">Seven digits</span></span> 
- <span data-ttu-id="fd62e-2867">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="fd62e-2867">A hyphen</span></span> 
- <span data-ttu-id="fd62e-2868">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="fd62e-2868">One digit</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-2869">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2869">Checksum</span></span>

<span data-ttu-id="fd62e-2870">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-2870">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-2871">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-2871">Definition</span></span>

<span data-ttu-id="fd62e-2872">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2872">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-2873">L’expression régulière Regex_philippines_unified_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2873">The regular expression Regex_philippines_unified_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-2874">Un mot clé figurant dans la liste Keyword_philippines_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2874">A keyword from Keyword_philippines_id is found.</span></span>

```xml
<!-- Philippines Unified Multi-Purpose ID number -->
<Entity id="019b39dd-8c25-4765-91a3-d9c6baf3c3b3" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_philippines_unified_id"/>
     <Match idRef="Keyword_philippines_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fd62e-2875">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-2875">Keywords</span></span>
   
#### <a name="keyword_philippines_id"></a><span data-ttu-id="fd62e-2876">Keyword_philippines_id</span><span class="sxs-lookup"><span data-stu-id="fd62e-2876">Keyword_philippines_id</span></span>

- <span data-ttu-id="fd62e-2877">Unified Multi-Purpose ID</span><span class="sxs-lookup"><span data-stu-id="fd62e-2877">Unified Multi-Purpose ID</span></span> 
- <span data-ttu-id="fd62e-2878">UMID</span><span class="sxs-lookup"><span data-stu-id="fd62e-2878">UMID</span></span> 
- <span data-ttu-id="fd62e-2879">Identity Card</span><span class="sxs-lookup"><span data-stu-id="fd62e-2879">Identity Card</span></span> 
- <span data-ttu-id="fd62e-2880">Pinag-isang Multi-Layunin ID</span><span class="sxs-lookup"><span data-stu-id="fd62e-2880">Pinag-isang Multi-Layunin ID</span></span>
   
## <a name="poland-identity-card"></a><span data-ttu-id="fd62e-2881">Carte d'identité Pologne</span><span class="sxs-lookup"><span data-stu-id="fd62e-2881">Poland Identity Card</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-2882">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-2882">Format</span></span>

<span data-ttu-id="fd62e-2883">Trois lettres et six chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2883">Three letters and six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-2884">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2884">Pattern</span></span>

<span data-ttu-id="fd62e-2885">Trois lettres (ne respectant pas la casse) suivis de six chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2885">Three letters (not case sensitive) followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-2886">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2886">Checksum</span></span>

<span data-ttu-id="fd62e-2887">Oui</span><span class="sxs-lookup"><span data-stu-id="fd62e-2887">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-2888">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-2888">Definition</span></span>

<span data-ttu-id="fd62e-2889">Une stratégie DLP est sûre à 75% d’avoir détecté ce type d’informations sensibles si, dans une proximité de 300 caractères: la fonction Func_polish_national_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2889">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_polish_national_id finds content that matches the pattern.</span></span>
<span data-ttu-id="fd62e-2890">Un mot clé figurant dans la liste Keyword_polish_national_id_passport_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2890">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
<span data-ttu-id="fd62e-2891">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2891">The checksum passes.</span></span>

```xml
<!-- Poland Identity Card-->
<Entity id="25E64989-ED5D-40CA-A939-6C14183BB7BF" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_national_id" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fd62e-2892">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-2892">Keywords</span></span>

#### <a name="keyword_polish_national_id_passport_number"></a><span data-ttu-id="fd62e-2893">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="fd62e-2893">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="fd62e-2894">Dowód osobisty</span><span class="sxs-lookup"><span data-stu-id="fd62e-2894">Dowód osobisty</span></span>
- <span data-ttu-id="fd62e-2895">Chiffre dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="fd62e-2895">Numer dowodu osobistego</span></span>
- <span data-ttu-id="fd62e-2896">Nazwa i dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="fd62e-2896">Nazwa i numer dowodu osobistego</span></span>
- <span data-ttu-id="fd62e-2897">Nazwa i Nr dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="fd62e-2897">Nazwa i nr dowodu osobistego</span></span>
- <span data-ttu-id="fd62e-2898">Nazwa je nr dowodu tożsamości</span><span class="sxs-lookup"><span data-stu-id="fd62e-2898">Nazwa i nr dowodu tożsamości</span></span>
- <span data-ttu-id="fd62e-2899">Dowód Tożsamości</span><span class="sxs-lookup"><span data-stu-id="fd62e-2899">Dowód Tożsamości</span></span>
- <span data-ttu-id="fd62e-2900">Dow.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2900">dow.</span></span> <span data-ttu-id="fd62e-2901">OS.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2901">os.</span></span>

   
## <a name="poland-national-id-pesel"></a><span data-ttu-id="fd62e-2902">ID national polonais (PESEL)</span><span class="sxs-lookup"><span data-stu-id="fd62e-2902">Poland National ID (PESEL)</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-2903">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-2903">Format</span></span>

<span data-ttu-id="fd62e-2904">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2904">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-2905">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2905">Pattern</span></span>

<span data-ttu-id="fd62e-2906">11 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="fd62e-2906">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-2907">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2907">Checksum</span></span>

<span data-ttu-id="fd62e-2908">Oui</span><span class="sxs-lookup"><span data-stu-id="fd62e-2908">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-2909">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-2909">Definition</span></span>

<span data-ttu-id="fd62e-2910">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2910">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-2911">La fonction Func_pesel_identification_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2911">The function Func_pesel_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-2912">Un mot clé figurant dans la liste Keyword_pesel_identification_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2912">A keyword from Keyword_pesel_identification_number is found.</span></span>
- <span data-ttu-id="fd62e-2913">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2913">The checksum passes.</span></span>

```xml
<!-- Poland National ID (PESEL) -->      
<Entity id="E3AAF206-4297-412F-9E06-BA8487E22456" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_pesel_identification_number" />
          <Match idRef="Keyword_pesel_identification_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fd62e-2914">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-2914">Keywords</span></span>

#### <a name="keyword_pesel_identification_number"></a><span data-ttu-id="fd62e-2915">Keyword_pesel_identification_number</span><span class="sxs-lookup"><span data-stu-id="fd62e-2915">Keyword_pesel_identification_number</span></span>

- <span data-ttu-id="fd62e-2916">Nr PESEL</span><span class="sxs-lookup"><span data-stu-id="fd62e-2916">Nr PESEL</span></span>
- <span data-ttu-id="fd62e-2917">PESEL</span><span class="sxs-lookup"><span data-stu-id="fd62e-2917">PESEL</span></span>   

   
## <a name="poland-passport"></a><span data-ttu-id="fd62e-2918">Passeport Pologne</span><span class="sxs-lookup"><span data-stu-id="fd62e-2918">Poland Passport</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-2919">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-2919">Format</span></span>

<span data-ttu-id="fd62e-2920">Deux lettres et sept chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2920">Two letters and seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-2921">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2921">Pattern</span></span>

<span data-ttu-id="fd62e-2922">Deux lettres (ne respectant pas la casse) suivies de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2922">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-2923">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2923">Checksum</span></span>

<span data-ttu-id="fd62e-2924">Oui</span><span class="sxs-lookup"><span data-stu-id="fd62e-2924">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-2925">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-2925">Definition</span></span>

<span data-ttu-id="fd62e-2926">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2926">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-2927">La fonction Func_polish_passport_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2927">The function Func_polish_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-2928">Un mot clé figurant dans la liste Keyword_polish_national_id_passport_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2928">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
- <span data-ttu-id="fd62e-2929">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2929">The checksum passes.</span></span>

```xml
<!-- Poland Passport Number -->
<Entity id="03937FB5-D2B6-4487-B61F-0F8BFF7C3517" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_passport_number" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
</Version>
```

### <a name="keywords"></a><span data-ttu-id="fd62e-2930">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-2930">Keywords</span></span>

#### <a name="keyword_polish_national_id_passport_number"></a><span data-ttu-id="fd62e-2931">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="fd62e-2931">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="fd62e-2932">Numéro paszportu</span><span class="sxs-lookup"><span data-stu-id="fd62e-2932">Numer paszportu</span></span>
- <span data-ttu-id="fd62e-2933">Nr.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2933">Nr.</span></span> <span data-ttu-id="fd62e-2934">Paszportu</span><span class="sxs-lookup"><span data-stu-id="fd62e-2934">Paszportu</span></span>
- <span data-ttu-id="fd62e-2935">Paszport</span><span class="sxs-lookup"><span data-stu-id="fd62e-2935">Paszport</span></span>

   
## <a name="portugal-citizen-card-number"></a><span data-ttu-id="fd62e-2936">Numéro de carte de citoyen Portugal</span><span class="sxs-lookup"><span data-stu-id="fd62e-2936">Portugal Citizen Card Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-2937">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-2937">Format</span></span>

<span data-ttu-id="fd62e-2938">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2938">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-2939">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2939">Pattern</span></span>

<span data-ttu-id="fd62e-2940">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2940">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-2941">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2941">Checksum</span></span>

<span data-ttu-id="fd62e-2942">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-2942">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-2943">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-2943">Definition</span></span>

<span data-ttu-id="fd62e-2944">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2944">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-2945">L’expression régulière Regex_portugal_citizen_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2945">The regular expression Regex_portugal_citizen_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-2946">Un mot clé figurant dans la liste Keyword_portugal_citizen_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2946">A keyword from Keyword_portugal_citizen_card is found.</span></span>

```xml
<!-- Portugal Citizen Card Number -->
<Entity id="91a7ece2-add4-4986-9a15-c84544d81ecd" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_portugal_citizen_card"/>
     <Match idRef="Keyword_portugal_citizen_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fd62e-2947">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-2947">Keywords</span></span>

#### <a name="keyword_portugal_citizen_card"></a><span data-ttu-id="fd62e-2948">Keyword_portugal_citizen_card</span><span class="sxs-lookup"><span data-stu-id="fd62e-2948">Keyword_portugal_citizen_card</span></span>

- <span data-ttu-id="fd62e-2949">Citizen Card</span><span class="sxs-lookup"><span data-stu-id="fd62e-2949">Citizen Card</span></span>
- <span data-ttu-id="fd62e-2950">National ID Card</span><span class="sxs-lookup"><span data-stu-id="fd62e-2950">National ID Card</span></span>
- <span data-ttu-id="fd62e-2951">Cc</span><span class="sxs-lookup"><span data-stu-id="fd62e-2951">CC</span></span>
- <span data-ttu-id="fd62e-2952">Cartão de Cidadão</span><span class="sxs-lookup"><span data-stu-id="fd62e-2952">Cartão de Cidadão</span></span>
- <span data-ttu-id="fd62e-2953">Bilhete de Identidade</span><span class="sxs-lookup"><span data-stu-id="fd62e-2953">Bilhete de Identidade</span></span>
   
## <a name="saudi-arabia-national-id"></a><span data-ttu-id="fd62e-2954">ID national Arabie saoudite</span><span class="sxs-lookup"><span data-stu-id="fd62e-2954">Saudi Arabia National ID</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-2955">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-2955">Format</span></span>

<span data-ttu-id="fd62e-2956">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2956">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-2957">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2957">Pattern</span></span>

<span data-ttu-id="fd62e-2958">10 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="fd62e-2958">10 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-2959">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2959">Checksum</span></span>

<span data-ttu-id="fd62e-2960">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-2960">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-2961">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-2961">Definition</span></span>

<span data-ttu-id="fd62e-2962">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2962">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-2963">L’expression régulière Regex_saudi_arabia_national_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2963">The regular expression Regex_saudi_arabia_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-2964">Un mot clé figurant dans la liste Keyword_saudi_arabia_national_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2964">A keyword from Keyword_saudi_arabia_national_id is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-2965">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-2965">Keywords</span></span>

#### <a name="keyword_saudi_arabia_national_id"></a><span data-ttu-id="fd62e-2966">Keyword_saudi_arabia_national_id</span><span class="sxs-lookup"><span data-stu-id="fd62e-2966">Keyword_saudi_arabia_national_id</span></span>

- <span data-ttu-id="fd62e-2967">Carte d’identification</span><span class="sxs-lookup"><span data-stu-id="fd62e-2967">Identification Card</span></span> 
- <span data-ttu-id="fd62e-2968">numéro de carte d’identité</span><span class="sxs-lookup"><span data-stu-id="fd62e-2968">I card number</span></span> 
- <span data-ttu-id="fd62e-2969">Numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="fd62e-2969">ID number</span></span> 
- <span data-ttu-id="fd62e-2970">الوطنية الهوية بطاقة رقم</span><span class="sxs-lookup"><span data-stu-id="fd62e-2970">الوطنية الهوية بطاقة رقم</span></span> 

   
## <a name="singapore-national-registration-identity-card-nric-number"></a><span data-ttu-id="fd62e-2971">Numéro de carte d’identité d’enregistrement national (NRIC) Singapour</span><span class="sxs-lookup"><span data-stu-id="fd62e-2971">Singapore National Registration Identity Card (NRIC) Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-2972">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-2972">Format</span></span>

<span data-ttu-id="fd62e-2973">Neuf lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-2973">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-2974">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2974">Pattern</span></span>

- <span data-ttu-id="fd62e-2975">Neuf lettres et chiffres :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2975">Nine letters and digits:</span></span>
- <span data-ttu-id="fd62e-2976">La lettre « F », « G », « S » ou « T » (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="fd62e-2976">The letter "F", "G", "S", or "T" (not case sensitive)</span></span> 
- <span data-ttu-id="fd62e-2977">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="fd62e-2977">Seven digits</span></span> 
- <span data-ttu-id="fd62e-2978">Un chiffre de contrôle alphabétique</span><span class="sxs-lookup"><span data-stu-id="fd62e-2978">An alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-2979">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-2979">Checksum</span></span>

<span data-ttu-id="fd62e-2980">Oui</span><span class="sxs-lookup"><span data-stu-id="fd62e-2980">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-2981">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-2981">Definition</span></span>

<span data-ttu-id="fd62e-2982">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2982">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-2983">L’expression régulière Regex_singapore_nric trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2983">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-2984">Un mot clé figurant dans la liste Keyword_singapore_nric est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2984">A keyword from Keyword_singapore_nric is found.</span></span>
- <span data-ttu-id="fd62e-2985">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2985">The checksum passes.</span></span>

<span data-ttu-id="fd62e-2986">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-2986">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-2987">L’expression régulière Regex_singapore_nric trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2987">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-2988">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-2988">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-2989">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-2989">Keywords</span></span>
   
#### <a name="keyword_singapore_nric"></a><span data-ttu-id="fd62e-2990">Keyword_singapore_nric</span><span class="sxs-lookup"><span data-stu-id="fd62e-2990">Keyword_singapore_nric</span></span>

- <span data-ttu-id="fd62e-2991">National Registration Identity Card</span><span class="sxs-lookup"><span data-stu-id="fd62e-2991">National Registration Identity Card</span></span> 
- <span data-ttu-id="fd62e-2992">Identity Card Number</span><span class="sxs-lookup"><span data-stu-id="fd62e-2992">Identity Card Number</span></span> 
- <span data-ttu-id="fd62e-2993">NRIC</span><span class="sxs-lookup"><span data-stu-id="fd62e-2993">NRIC</span></span> 
- <span data-ttu-id="fd62e-2994">COMBUSTION</span><span class="sxs-lookup"><span data-stu-id="fd62e-2994">IC</span></span> 
- <span data-ttu-id="fd62e-2995">Foreign Identification Number</span><span class="sxs-lookup"><span data-stu-id="fd62e-2995">Foreign Identification Number</span></span> 
- <span data-ttu-id="fd62e-2996">ECHERCHER</span><span class="sxs-lookup"><span data-stu-id="fd62e-2996">FIN</span></span> 
- <span data-ttu-id="fd62e-2997">身份证</span><span class="sxs-lookup"><span data-stu-id="fd62e-2997">身份证</span></span> 
- <span data-ttu-id="fd62e-2998">身份證</span><span class="sxs-lookup"><span data-stu-id="fd62e-2998">身份證</span></span> 
   
## <a name="south-africa-identification-number"></a><span data-ttu-id="fd62e-2999">Numéro d’identification Afrique du Sud</span><span class="sxs-lookup"><span data-stu-id="fd62e-2999">South Africa Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-3000">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-3000">Format</span></span>

<span data-ttu-id="fd62e-3001">13 chiffres pouvant contenir des espaces</span><span class="sxs-lookup"><span data-stu-id="fd62e-3001">13 digits that may contain spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-3002">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-3002">Pattern</span></span>

<span data-ttu-id="fd62e-3003">13 chiffres :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3003">13 digits:</span></span>
- <span data-ttu-id="fd62e-3004">Six chiffres au format AAMMJJ correspondant à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="fd62e-3004">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="fd62e-3005">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-3005">Four digits</span></span> 
- <span data-ttu-id="fd62e-3006">Un indicateur de citoyenneté à un chiffre </span><span class="sxs-lookup"><span data-stu-id="fd62e-3006">A single-digit citizenship indicator</span></span> 
- <span data-ttu-id="fd62e-3007">Le chiffre « 8 » ou « 9 » </span><span class="sxs-lookup"><span data-stu-id="fd62e-3007">The digit "8" or "9"</span></span> 
- <span data-ttu-id="fd62e-3008">Un chiffre pour la somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-3008">One digit which is a checksum digit</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-3009">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-3009">Checksum</span></span>

<span data-ttu-id="fd62e-3010">Oui</span><span class="sxs-lookup"><span data-stu-id="fd62e-3010">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-3011">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-3011">Definition</span></span>

<span data-ttu-id="fd62e-3012">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3012">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-3013">La fonction Func_south_africa_identification_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3013">The function Func_south_africa_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-3014">Un mot clé figurant dans la liste Keyword_south_africa_identification_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3014">A keyword from Keyword_south_africa_identification_number is found.</span></span>
- <span data-ttu-id="fd62e-3015">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3015">The checksum passes.</span></span>

```xml
<!-- South Africa Identification Number -->
<Entity id="e2adf7cb-8ea6-4048-a2ed-d89eb65f2780" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_south_africa_identification_number"/>
     <Match idRef="Keyword_south_africa_identification_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fd62e-3016">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-3016">Keywords</span></span>
   
#### <a name="keyword_south_africa_identification_number"></a><span data-ttu-id="fd62e-3017">Keyword_south_africa_identification_number</span><span class="sxs-lookup"><span data-stu-id="fd62e-3017">Keyword_south_africa_identification_number</span></span>

- <span data-ttu-id="fd62e-3018">Identity card</span><span class="sxs-lookup"><span data-stu-id="fd62e-3018">Identity card</span></span>
- <span data-ttu-id="fd62e-3019">ID</span><span class="sxs-lookup"><span data-stu-id="fd62e-3019">ID</span></span>
- <span data-ttu-id="fd62e-3020">Identificateur</span><span class="sxs-lookup"><span data-stu-id="fd62e-3020">Identification</span></span> 
   
## <a name="south-korea-resident-registration-number"></a><span data-ttu-id="fd62e-3021">Matricule de résident Corée du Sud</span><span class="sxs-lookup"><span data-stu-id="fd62e-3021">South Korea Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-3022">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-3022">Format</span></span>

<span data-ttu-id="fd62e-3023">13 chiffres contenant un trait d’union</span><span class="sxs-lookup"><span data-stu-id="fd62e-3023">13 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-3024">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-3024">Pattern</span></span>

<span data-ttu-id="fd62e-3025">13 chiffres :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3025">13 digits:</span></span>
- <span data-ttu-id="fd62e-3026">Six chiffres au format AAMMJJ correspondant à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="fd62e-3026">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="fd62e-3027">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="fd62e-3027">A hyphen</span></span> 
- <span data-ttu-id="fd62e-3028">Un chiffre déterminé par le siècle et le sexe </span><span class="sxs-lookup"><span data-stu-id="fd62e-3028">One digit determined by the century and gender</span></span> 
- <span data-ttu-id="fd62e-3029">Code à quatre chiffres désignant la région de naissance </span><span class="sxs-lookup"><span data-stu-id="fd62e-3029">Four-digit region-of-birth code</span></span> 
- <span data-ttu-id="fd62e-3030">Un chiffre utilisé pour différencier les personnes dont les chiffres précédents sont identiques. </span><span class="sxs-lookup"><span data-stu-id="fd62e-3030">One digit used to differentiate people for whom the preceding numbers are identical</span></span> 
- <span data-ttu-id="fd62e-3031">Un chiffre de contrôle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3031">A check digit.</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-3032">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-3032">Checksum</span></span>

<span data-ttu-id="fd62e-3033">Oui</span><span class="sxs-lookup"><span data-stu-id="fd62e-3033">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-3034">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-3034">Definition</span></span>

<span data-ttu-id="fd62e-3035">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3035">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-3036">La fonction Func_south_korea_resident_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3036">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-3037">Un mot clé figurant dans la liste Keyword_south_korea_resident_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3037">A keyword from Keyword_south_korea_resident_number is found.</span></span>
- <span data-ttu-id="fd62e-3038">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3038">The checksum passes.</span></span>

<span data-ttu-id="fd62e-3039">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3039">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-3040">La fonction Func_south_korea_resident_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3040">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-3041">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3041">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-3042">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-3042">Keywords</span></span>
   
#### <a name="keyword_south_korea_resident_number"></a><span data-ttu-id="fd62e-3043">Keyword_south_korea_resident_number</span><span class="sxs-lookup"><span data-stu-id="fd62e-3043">Keyword_south_korea_resident_number</span></span>

- <span data-ttu-id="fd62e-3044">National ID card</span><span class="sxs-lookup"><span data-stu-id="fd62e-3044">National ID card</span></span> 
- <span data-ttu-id="fd62e-3045">Citizen’s Registration Number</span><span class="sxs-lookup"><span data-stu-id="fd62e-3045">Citizen's Registration Number</span></span> 
- <span data-ttu-id="fd62e-3046">Jumin deungnok beonho</span><span class="sxs-lookup"><span data-stu-id="fd62e-3046">Jumin deungnok beonho</span></span> 
- <span data-ttu-id="fd62e-3047">RRN</span><span class="sxs-lookup"><span data-stu-id="fd62e-3047">RRN</span></span> 
- <span data-ttu-id="fd62e-3048">주민등록번호</span><span class="sxs-lookup"><span data-stu-id="fd62e-3048">주민등록번호</span></span>
   
## <a name="spain-social-security-number-ssn"></a><span data-ttu-id="fd62e-3049">Numéro de sécurité sociale Espagne</span><span class="sxs-lookup"><span data-stu-id="fd62e-3049">Spain Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-3050">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-3050">Format</span></span>

<span data-ttu-id="fd62e-3051">11 à 12 chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-3051">11-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-3052">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-3052">Pattern</span></span>

<span data-ttu-id="fd62e-3053">11-12 chiffres:</span><span class="sxs-lookup"><span data-stu-id="fd62e-3053">11-12 digits:</span></span>
- <span data-ttu-id="fd62e-3054">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-3054">Two digits</span></span> 
- <span data-ttu-id="fd62e-3055">Une barre oblique (facultative)</span><span class="sxs-lookup"><span data-stu-id="fd62e-3055">A forward slash (optional)</span></span> 
- <span data-ttu-id="fd62e-3056">7 à 8 chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-3056">7-8 digits</span></span> 
- <span data-ttu-id="fd62e-3057">Une barre oblique (facultative)</span><span class="sxs-lookup"><span data-stu-id="fd62e-3057">A forward slash (optional)</span></span> 
- <span data-ttu-id="fd62e-3058">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-3058">Two digits</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-3059">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-3059">Checksum</span></span>

<span data-ttu-id="fd62e-3060">Oui</span><span class="sxs-lookup"><span data-stu-id="fd62e-3060">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-3061">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-3061">Definition</span></span>

<span data-ttu-id="fd62e-3062">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3062">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-3063">La fonction Func_spanish_social_security_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3063">The function Func_spanish_social_security_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-3064">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3064">The checksum passes.</span></span>

```xml
<!-- Spain SSN -->
<Entity id="5df987c0-8eae-4bce-ace7-b316347f3070" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_spanish_social_security_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fd62e-3065">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-3065">Keywords</span></span>

<span data-ttu-id="fd62e-3066">Aucun</span><span class="sxs-lookup"><span data-stu-id="fd62e-3066">None</span></span>

## <a name="sql-server-connection-string"></a><span data-ttu-id="fd62e-3067">Chaîne de connexion SQL Server</span><span class="sxs-lookup"><span data-stu-id="fd62e-3067">SQL Server Connection String</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-3068">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-3068">Format</span></span>

<span data-ttu-id="fd62e-3069">La chaîne «User ID», «User ID», «UID» ou «UserId» suivi des caractères et des chaînes décrits dans le modèle ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3069">The string "User Id", "User ID", "uid", or "UserId" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-3070">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-3070">Pattern</span></span>

- <span data-ttu-id="fd62e-3071">La chaîne «User ID», «User ID», «UID» ou «UserId»</span><span class="sxs-lookup"><span data-stu-id="fd62e-3071">The string "User Id", "User ID", "uid", or "UserId"</span></span>
- <span data-ttu-id="fd62e-3072">N’importe quelle combinaison entre 1-200 majuscules ou minuscules, des chiffres, des symboles, des caractères spéciaux ou des espaces</span><span class="sxs-lookup"><span data-stu-id="fd62e-3072">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="fd62e-3073">La chaîne "password" ou "PWD" où "PWD" n’est pas précédé d’une lettre minuscule</span><span class="sxs-lookup"><span data-stu-id="fd62e-3073">The string "Password" or "pwd" where "pwd" is not preceded by a lowercase letter</span></span>
- <span data-ttu-id="fd62e-3074">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="fd62e-3074">An equal sign (=)</span></span>
- <span data-ttu-id="fd62e-3075">Tout caractère qui n’est pas un signe dollar ($), un symbole de pourcentage (%), un symbole supérieur à (>), un symbole (@), un guillemet ("), un point-virgule (;), une accolade ouvrante ([) ou un crochet gauche ({)</span><span class="sxs-lookup"><span data-stu-id="fd62e-3075">Any character that is not a dollar sign ($), percent symbol (%), greater than symbol (>), at symbol (@), quotation mark ("), semicolon (;), left brace ([), or left bracket ({)</span></span>
- <span data-ttu-id="fd62e-3076">N’importe quelle combinaison de 7-128 caractères qui ne sont pas des points-virgules (;), barre oblique (/) ou guillemets (")</span><span class="sxs-lookup"><span data-stu-id="fd62e-3076">Any combination of 7-128 characters that are not a semicolon (;), forward slash (/), or quotation mark (")</span></span>
- <span data-ttu-id="fd62e-3077">Un point-virgule (;) ou guillemets (")</span><span class="sxs-lookup"><span data-stu-id="fd62e-3077">A semicolon (;) or quotation mark (")</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-3078">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-3078">Checksum</span></span>

<span data-ttu-id="fd62e-3079">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-3079">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-3080">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-3080">Definition</span></span>

<span data-ttu-id="fd62e-3081">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3081">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-3082">L’expression régulière CEP_Regex_SQLServerConnectionString trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3082">The regular expression CEP_Regex_SQLServerConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-3083">Un mot clé depuis CEP_GlobalFilter \*\*\*\* est introuvable.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3083">A keyword from CEP_GlobalFilter is **not** found.</span></span>
- <span data-ttu-id="fd62e-3084">L’expression régulière CEP_PasswordPlaceHolder ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3084">The regular expression CEP_PasswordPlaceHolder does **not** find content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-3085">L’expression régulière CEP_CommonExampleKeywords ne trouve **pas** le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3085">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```sql
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

### <a name="keywords"></a><span data-ttu-id="fd62e-3086">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-3086">Keywords</span></span>

#### <a name="cep_globalfilter"></a><span data-ttu-id="fd62e-3087">CEP_GlobalFilter</span><span class="sxs-lookup"><span data-stu-id="fd62e-3087">CEP_GlobalFilter</span></span>

- <span data-ttu-id="fd62e-3088">some-password</span><span class="sxs-lookup"><span data-stu-id="fd62e-3088">some-password</span></span>
- <span data-ttu-id="fd62e-3089">somepassword</span><span class="sxs-lookup"><span data-stu-id="fd62e-3089">somepassword</span></span>
- <span data-ttu-id="fd62e-3090">secretPassword</span><span class="sxs-lookup"><span data-stu-id="fd62e-3090">secretPassword</span></span>
- <span data-ttu-id="fd62e-3091">échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fd62e-3091">sample</span></span>

#### <a name="cep_passwordplaceholder"></a><span data-ttu-id="fd62e-3092">CEP_PasswordPlaceHolder</span><span class="sxs-lookup"><span data-stu-id="fd62e-3092">CEP_PasswordPlaceHolder</span></span>

<span data-ttu-id="fd62e-3093">(Notez que techniquement, ce type d’informations sensibles identifie ces mots clés à l’aide d’une expression régulière, et non d’une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="fd62e-3093">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="fd62e-3094">Mot de passe ou mot de passe suivi par 0-2 espaces, un signe égal (=), 0-2 espaces et un astérisque (\*)--ou--</span><span class="sxs-lookup"><span data-stu-id="fd62e-3094">Password or pwd followed by 0-2 spaces, an equal sign (=), 0-2 spaces, and an asterisk (\*) --OR--</span></span>
- <span data-ttu-id="fd62e-3095">Mot de passe ou mot de passe suivi par:</span><span class="sxs-lookup"><span data-stu-id="fd62e-3095">Password or pwd followed by:</span></span>
    - <span data-ttu-id="fd62e-3096">Signe égal (=)</span><span class="sxs-lookup"><span data-stu-id="fd62e-3096">Equal sign (=)</span></span>
    - <span data-ttu-id="fd62e-3097">Symbole inférieur à (<)</span><span class="sxs-lookup"><span data-stu-id="fd62e-3097">Less than symbol (<)</span></span>
    - <span data-ttu-id="fd62e-3098">Toute combinaison de 1-200 caractères qui sont des lettres majuscules ou minuscules, des chiffres, un astérisque (\*), un tiret (-), un trait de soulignement (_) ou un espace blanc</span><span class="sxs-lookup"><span data-stu-id="fd62e-3098">Any combination of 1-200 characters that are upper- or lowercase letters, digits, an asterisk (\*), hyphen (-), underline (_), or whitespace character</span></span>
    - <span data-ttu-id="fd62e-3099">Symbole supérieur à (>)</span><span class="sxs-lookup"><span data-stu-id="fd62e-3099">Greater than symbol (>)</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="fd62e-3100">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="fd62e-3100">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="fd62e-3101">(Notez que techniquement, ce type d’informations sensibles identifie ces mots clés à l’aide d’une expression régulière, et non d’une liste de mots clés.)</span><span class="sxs-lookup"><span data-stu-id="fd62e-3101">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="fd62e-3102">contoso</span><span class="sxs-lookup"><span data-stu-id="fd62e-3102">contoso</span></span>
- <span data-ttu-id="fd62e-3103">société</span><span class="sxs-lookup"><span data-stu-id="fd62e-3103">fabrikam</span></span>
- <span data-ttu-id="fd62e-3104">Northwind</span><span class="sxs-lookup"><span data-stu-id="fd62e-3104">northwind</span></span>
- <span data-ttu-id="fd62e-3105">immédiatement</span><span class="sxs-lookup"><span data-stu-id="fd62e-3105">sandbox</span></span>
- <span data-ttu-id="fd62e-3106">onebox</span><span class="sxs-lookup"><span data-stu-id="fd62e-3106">onebox</span></span>
- <span data-ttu-id="fd62e-3107">hôte</span><span class="sxs-lookup"><span data-stu-id="fd62e-3107">localhost</span></span>
- <span data-ttu-id="fd62e-3108">bouclage</span><span class="sxs-lookup"><span data-stu-id="fd62e-3108">127.0.0.1</span></span>
- <span data-ttu-id="fd62e-3109">testacs.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3109">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="fd62e-3110">com</span><span class="sxs-lookup"><span data-stu-id="fd62e-3110">com</span></span>
- <span data-ttu-id="fd62e-3111">s-int.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3111">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="fd62e-3112">NET</span><span class="sxs-lookup"><span data-stu-id="fd62e-3112">net</span></span>

## <a name="sweden-national-id"></a><span data-ttu-id="fd62e-3113">ID national Suède</span><span class="sxs-lookup"><span data-stu-id="fd62e-3113">Sweden National ID</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-3114">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-3114">Format</span></span>

<span data-ttu-id="fd62e-3115">10 ou 12 chiffres et éventuellement un délimiteur</span><span class="sxs-lookup"><span data-stu-id="fd62e-3115">10 or 12 digits and an optional delimiter</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-3116">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-3116">Pattern</span></span>

<span data-ttu-id="fd62e-3117">10 ou 12 chiffres et un délimiteur facultatif :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3117">10 or 12 digits and an optional delimiter:</span></span>
- <span data-ttu-id="fd62e-3118">2 à 4 chiffres (facultatifs)</span><span class="sxs-lookup"><span data-stu-id="fd62e-3118">2-4 digits (optional)</span></span> 
- <span data-ttu-id="fd62e-3119">Six chiffres au format de date AAMMJJ</span><span class="sxs-lookup"><span data-stu-id="fd62e-3119">Six digits in date format YYMMDD</span></span> 
- <span data-ttu-id="fd62e-3120">Séparateur de « - » ou « + » (facultatif), plus</span><span class="sxs-lookup"><span data-stu-id="fd62e-3120">Delimiter of "-" or "+" (optional), plus</span></span>
- <span data-ttu-id="fd62e-3121">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-3121">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-3122">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-3122">Checksum</span></span>

<span data-ttu-id="fd62e-3123">Oui</span><span class="sxs-lookup"><span data-stu-id="fd62e-3123">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-3124">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-3124">Definition</span></span>

<span data-ttu-id="fd62e-3125">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3125">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-3126">La fonction Func_swedish_national_identifier trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3126">The function Func_swedish_national_identifier finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-3127">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3127">The checksum passes.</span></span>

```xml
<!-- Sweden National ID -->
<Entity id="f69aaf40-79be-4fac-8f05-fd1910d272c8" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_swedish_national_identifier" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fd62e-3128">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-3128">Keywords</span></span>

<span data-ttu-id="fd62e-3129">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-3129">No</span></span>
   
## <a name="sweden-passport-number"></a><span data-ttu-id="fd62e-3130">Numéro de passeport Suède</span><span class="sxs-lookup"><span data-stu-id="fd62e-3130">Sweden Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-3131">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-3131">Format</span></span>

<span data-ttu-id="fd62e-3132">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-3132">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-3133">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-3133">Pattern</span></span>

<span data-ttu-id="fd62e-3134">Huit chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="fd62e-3134">Eight consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-3135">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-3135">Checksum</span></span>

<span data-ttu-id="fd62e-3136">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-3136">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-3137">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-3137">Definition</span></span>

<span data-ttu-id="fd62e-3138">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3138">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-3139">L’expression régulière Regex_sweden_passport_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3139">The regular expression Regex_sweden_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-3140">L’une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3140">One of the following is true:</span></span>
    - <span data-ttu-id="fd62e-3141">Un mot clé figurant dans la liste Keyword_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3141">A keyword from Keyword_passport is found.</span></span>
    - <span data-ttu-id="fd62e-3142">Un mot clé figurant dans la liste Keyword_sweden_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3142">A keyword from Keyword_sweden_passport is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-3143">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-3143">Keywords</span></span>
   
#### <a name="keyword_sweden_passport"></a><span data-ttu-id="fd62e-3144">Keyword_sweden_passport</span><span class="sxs-lookup"><span data-stu-id="fd62e-3144">Keyword_sweden_passport</span></span>

- <span data-ttu-id="fd62e-3145">exigences en matière de visa</span><span class="sxs-lookup"><span data-stu-id="fd62e-3145">visa requirements</span></span> 
- <span data-ttu-id="fd62e-3146">Carte d’enregistrement d’une personne étrangère</span><span class="sxs-lookup"><span data-stu-id="fd62e-3146">Alien Registration Card</span></span> 
- <span data-ttu-id="fd62e-3147">Visas Schengen</span><span class="sxs-lookup"><span data-stu-id="fd62e-3147">Schengen visas</span></span> 
- <span data-ttu-id="fd62e-3148">Visa Schengen</span><span class="sxs-lookup"><span data-stu-id="fd62e-3148">Schengen visa</span></span> 
- <span data-ttu-id="fd62e-3149">Traitement du visa</span><span class="sxs-lookup"><span data-stu-id="fd62e-3149">Visa Processing</span></span> 
- <span data-ttu-id="fd62e-3150">Type de visa</span><span class="sxs-lookup"><span data-stu-id="fd62e-3150">Visa Type</span></span> 
- <span data-ttu-id="fd62e-3151">Entrée unique</span><span class="sxs-lookup"><span data-stu-id="fd62e-3151">Single Entry</span></span> 
- <span data-ttu-id="fd62e-3152">Entrée multiple</span><span class="sxs-lookup"><span data-stu-id="fd62e-3152">Multiple Entry</span></span> 
- <span data-ttu-id="fd62e-3153">Frais de traitement G3</span><span class="sxs-lookup"><span data-stu-id="fd62e-3153">G3 Processing Fees</span></span> 

#### <a name="keyword_passport"></a><span data-ttu-id="fd62e-3154">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="fd62e-3154">Keyword_passport</span></span>

- <span data-ttu-id="fd62e-3155">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="fd62e-3155">Passport Number</span></span> 
- <span data-ttu-id="fd62e-3156">N° de passeport</span><span class="sxs-lookup"><span data-stu-id="fd62e-3156">Passport No</span></span> 
- <span data-ttu-id="fd62e-3157"># Passeport</span><span class="sxs-lookup"><span data-stu-id="fd62e-3157">Passport #</span></span> 
- <span data-ttu-id="fd62e-3158">Tel #</span><span class="sxs-lookup"><span data-stu-id="fd62e-3158">Passport#</span></span> 
- <span data-ttu-id="fd62e-3159">PassportID</span><span class="sxs-lookup"><span data-stu-id="fd62e-3159">PassportID</span></span> 
- <span data-ttu-id="fd62e-3160">N ° passeport</span><span class="sxs-lookup"><span data-stu-id="fd62e-3160">Passportno</span></span> 
- <span data-ttu-id="fd62e-3161">passportnumber</span><span class="sxs-lookup"><span data-stu-id="fd62e-3161">passportnumber</span></span> 
- <span data-ttu-id="fd62e-3162">パスポート</span><span class="sxs-lookup"><span data-stu-id="fd62e-3162">パスポート</span></span> 
- <span data-ttu-id="fd62e-3163">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="fd62e-3163">パスポート番号</span></span> 
- <span data-ttu-id="fd62e-3164">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="fd62e-3164">パスポートのNum</span></span> 
- <span data-ttu-id="fd62e-3165">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="fd62e-3165">パスポート＃</span></span> 
- <span data-ttu-id="fd62e-3166">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="fd62e-3166">Numéro de passeport</span></span> 
- <span data-ttu-id="fd62e-3167">Passeport n°</span><span class="sxs-lookup"><span data-stu-id="fd62e-3167">Passeport n °</span></span> 
- <span data-ttu-id="fd62e-3168">Passeport numéro</span><span class="sxs-lookup"><span data-stu-id="fd62e-3168">Passeport Non</span></span> 
- <span data-ttu-id="fd62e-3169"># Passeport</span><span class="sxs-lookup"><span data-stu-id="fd62e-3169">Passeport #</span></span> 
- <span data-ttu-id="fd62e-3170">Passeport #</span><span class="sxs-lookup"><span data-stu-id="fd62e-3170">Passeport#</span></span> 
- <span data-ttu-id="fd62e-3171">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="fd62e-3171">PasseportNon</span></span> 
- <span data-ttu-id="fd62e-3172">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="fd62e-3172">Passeportn °</span></span> 
   
## <a name="swift-code"></a><span data-ttu-id="fd62e-3173">Code SWIFT</span><span class="sxs-lookup"><span data-stu-id="fd62e-3173">SWIFT Code</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-3174">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-3174">Format</span></span>

<span data-ttu-id="fd62e-3175">Quatre lettres suivies de 5 à 31 lettres ou chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-3175">Four letters followed by 5-31 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-3176">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-3176">Pattern</span></span>

<span data-ttu-id="fd62e-3177">Quatre lettres suivies de 5 à 31 lettres ou chiffres :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3177">Four letters followed by 5-31 letters or digits:</span></span>
- <span data-ttu-id="fd62e-3178">Code bancaire à quatre lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="fd62e-3178">Four-letter bank code (not case sensitive)</span></span> 
- <span data-ttu-id="fd62e-3179">Un espace facultatif</span><span class="sxs-lookup"><span data-stu-id="fd62e-3179">An optional space</span></span> 
- <span data-ttu-id="fd62e-3180">4 à 28 lettres ou chiffres (numéro de compte bancaire de base (BBAN))</span><span class="sxs-lookup"><span data-stu-id="fd62e-3180">4-28 letters or digits (the Basic Bank Account Number (BBAN))</span></span> 
- <span data-ttu-id="fd62e-3181">Un espace facultatif</span><span class="sxs-lookup"><span data-stu-id="fd62e-3181">An optional space</span></span> 
- <span data-ttu-id="fd62e-3182">1 à 3 lettres ou chiffres (reste du BBAN)</span><span class="sxs-lookup"><span data-stu-id="fd62e-3182">1-3 letters or digits (remainder of the BBAN)</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-3183">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-3183">Checksum</span></span>

<span data-ttu-id="fd62e-3184">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-3184">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-3185">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-3185">Definition</span></span>

<span data-ttu-id="fd62e-3186">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3186">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-3187">L’expression régulière Regex_swift trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3187">The regular expression Regex_swift finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-3188">Un mot clé figurant dans la liste Keyword_swift est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3188">A keyword from Keyword_swift is found.</span></span>

```xml
<Entity id="cb2ab58c-9cb8-4c81-baf8-a4e106791df4" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_swift" />
        <Match idRef="Keyword_swift" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fd62e-3189">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-3189">Keywords</span></span>
   
#### <a name="keyword_swift"></a><span data-ttu-id="fd62e-3190">Keyword_swift</span><span class="sxs-lookup"><span data-stu-id="fd62e-3190">Keyword_swift</span></span>

- <span data-ttu-id="fd62e-3191">organisation internationale de normalisation 9362</span><span class="sxs-lookup"><span data-stu-id="fd62e-3191">international organization for standardization 9362</span></span> 
- <span data-ttu-id="fd62e-3192">ISO 9362</span><span class="sxs-lookup"><span data-stu-id="fd62e-3192">iso 9362</span></span> 
- <span data-ttu-id="fd62e-3193">iso9362</span><span class="sxs-lookup"><span data-stu-id="fd62e-3193">iso9362</span></span> 
- <span data-ttu-id="fd62e-3194">rapide\#</span><span class="sxs-lookup"><span data-stu-id="fd62e-3194">swift\#</span></span> 
- <span data-ttu-id="fd62e-3195">swiftcode</span><span class="sxs-lookup"><span data-stu-id="fd62e-3195">swiftcode</span></span> 
- <span data-ttu-id="fd62e-3196">swiftnumber</span><span class="sxs-lookup"><span data-stu-id="fd62e-3196">swiftnumber</span></span> 
- <span data-ttu-id="fd62e-3197">swiftroutingnumber</span><span class="sxs-lookup"><span data-stu-id="fd62e-3197">swiftroutingnumber</span></span> 
- <span data-ttu-id="fd62e-3198">code swift</span><span class="sxs-lookup"><span data-stu-id="fd62e-3198">swift code</span></span> 
- <span data-ttu-id="fd62e-3199"># numéro swift</span><span class="sxs-lookup"><span data-stu-id="fd62e-3199">swift number #</span></span> 
- <span data-ttu-id="fd62e-3200">numéro d’acheminement swift</span><span class="sxs-lookup"><span data-stu-id="fd62e-3200">swift routing number</span></span> 
- <span data-ttu-id="fd62e-3201">numéro BIC</span><span class="sxs-lookup"><span data-stu-id="fd62e-3201">bic number</span></span> 
- <span data-ttu-id="fd62e-3202">code BIC</span><span class="sxs-lookup"><span data-stu-id="fd62e-3202">bic code</span></span> 
- <span data-ttu-id="fd62e-3203">BIC\#</span><span class="sxs-lookup"><span data-stu-id="fd62e-3203">bic \#</span></span> 
- <span data-ttu-id="fd62e-3204">BIC\#</span><span class="sxs-lookup"><span data-stu-id="fd62e-3204">bic\#</span></span> 
- <span data-ttu-id="fd62e-3205">code d’identification bancaire</span><span class="sxs-lookup"><span data-stu-id="fd62e-3205">bank identifier code</span></span> 
- <span data-ttu-id="fd62e-3206">標準化 9362</span><span class="sxs-lookup"><span data-stu-id="fd62e-3206">標準化9362</span></span> 
- <span data-ttu-id="fd62e-3207">迅速＃</span><span class="sxs-lookup"><span data-stu-id="fd62e-3207">迅速＃</span></span> 
- <span data-ttu-id="fd62e-3208">SWIFTコード</span><span class="sxs-lookup"><span data-stu-id="fd62e-3208">SWIFTコード</span></span> 
- <span data-ttu-id="fd62e-3209">SWIFT番号</span><span class="sxs-lookup"><span data-stu-id="fd62e-3209">SWIFT番号</span></span> 
- <span data-ttu-id="fd62e-3210">迅速なルーティング番号</span><span class="sxs-lookup"><span data-stu-id="fd62e-3210">迅速なルーティング番号</span></span> 
- <span data-ttu-id="fd62e-3211">BIC番号</span><span class="sxs-lookup"><span data-stu-id="fd62e-3211">BIC番号</span></span> 
- <span data-ttu-id="fd62e-3212">BICコード</span><span class="sxs-lookup"><span data-stu-id="fd62e-3212">BICコード</span></span> 
- <span data-ttu-id="fd62e-3213">銀行識別コードのための国際組織</span><span class="sxs-lookup"><span data-stu-id="fd62e-3213">銀行識別コードのための国際組織</span></span> 
- <span data-ttu-id="fd62e-3214">Organisation internationale de normalisation 9362</span><span class="sxs-lookup"><span data-stu-id="fd62e-3214">Organisation internationale de normalisation 9362</span></span> 
- <span data-ttu-id="fd62e-3215">rapide\#</span><span class="sxs-lookup"><span data-stu-id="fd62e-3215">rapide \#</span></span> 
- <span data-ttu-id="fd62e-3216">code SWIFT</span><span class="sxs-lookup"><span data-stu-id="fd62e-3216">code SWIFT</span></span> 
- <span data-ttu-id="fd62e-3217">le numéro de swift</span><span class="sxs-lookup"><span data-stu-id="fd62e-3217">le numéro de swift</span></span> 
- <span data-ttu-id="fd62e-3218">swift numéro d’acheminement</span><span class="sxs-lookup"><span data-stu-id="fd62e-3218">swift numéro d'acheminement</span></span> 
- <span data-ttu-id="fd62e-3219">le numéro BIC</span><span class="sxs-lookup"><span data-stu-id="fd62e-3219">le numéro BIC</span></span> 
- <span data-ttu-id="fd62e-3220">\#BIC</span><span class="sxs-lookup"><span data-stu-id="fd62e-3220">\# BIC</span></span> 
- <span data-ttu-id="fd62e-3221">code identificateur de banque</span><span class="sxs-lookup"><span data-stu-id="fd62e-3221">code identificateur de banque</span></span> 
   
## <a name="taiwan-national-id"></a><span data-ttu-id="fd62e-3222">ID national à Taïwan</span><span class="sxs-lookup"><span data-stu-id="fd62e-3222">Taiwan National ID</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-3223">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-3223">Format</span></span>

<span data-ttu-id="fd62e-3224">Une lettre  suivie de neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-3224">One letter (in English) followed by nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-3225">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-3225">Pattern</span></span>

<span data-ttu-id="fd62e-3226">Une lettre suivie de neuf chiffres :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3226">One letter (in English) followed by nine digits:</span></span>
- <span data-ttu-id="fd62e-3227">Une lettre (en anglais, ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="fd62e-3227">One letter (in English, not case sensitive)</span></span> 
- <span data-ttu-id="fd62e-3228">Le chiffre « 1 » ou « 2 »</span><span class="sxs-lookup"><span data-stu-id="fd62e-3228">The digit "1" or "2"</span></span> 
- <span data-ttu-id="fd62e-3229">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-3229">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-3230">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-3230">Checksum</span></span>

<span data-ttu-id="fd62e-3231">Oui</span><span class="sxs-lookup"><span data-stu-id="fd62e-3231">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-3232">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-3232">Definition</span></span>

<span data-ttu-id="fd62e-3233">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3233">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-3234">La fonction Func_taiwanese_national_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3234">The function Func_taiwanese_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-3235">Un mot clé figurant dans la liste Keyword_taiwanese_national_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3235">A keyword from Keyword_taiwanese_national_id is found.</span></span>
- <span data-ttu-id="fd62e-3236">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3236">The checksum passes.</span></span>

```xml
<!-- Taiwanese National ID -->
<Entity id="4C7BFC34-8DD1-421D-8FB7-6C6182C2AF03" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_taiwanese_national_id" />
          <Match idRef="Keyword_taiwanese_national_id" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fd62e-3237">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-3237">Keywords</span></span>

#### <a name="keyword_taiwanese_national_id"></a><span data-ttu-id="fd62e-3238">Keyword_taiwanese_national_id</span><span class="sxs-lookup"><span data-stu-id="fd62e-3238">Keyword_taiwanese_national_id</span></span>

- <span data-ttu-id="fd62e-3239">身份證字號</span><span class="sxs-lookup"><span data-stu-id="fd62e-3239">身份證字號</span></span> 
- <span data-ttu-id="fd62e-3240">身份證</span><span class="sxs-lookup"><span data-stu-id="fd62e-3240">身份證</span></span> 
- <span data-ttu-id="fd62e-3241">身份證號碼</span><span class="sxs-lookup"><span data-stu-id="fd62e-3241">身份證號碼</span></span> 
- <span data-ttu-id="fd62e-3242">身份證號</span><span class="sxs-lookup"><span data-stu-id="fd62e-3242">身份證號</span></span> 
- <span data-ttu-id="fd62e-3243">身分證字號</span><span class="sxs-lookup"><span data-stu-id="fd62e-3243">身分證字號</span></span> 
- <span data-ttu-id="fd62e-3244">身分證</span><span class="sxs-lookup"><span data-stu-id="fd62e-3244">身分證</span></span> 
- <span data-ttu-id="fd62e-3245">身分證號碼</span><span class="sxs-lookup"><span data-stu-id="fd62e-3245">身分證號碼</span></span> 
- <span data-ttu-id="fd62e-3246">身份證號</span><span class="sxs-lookup"><span data-stu-id="fd62e-3246">身份證號</span></span> 
- <span data-ttu-id="fd62e-3247">身分證統一編號</span><span class="sxs-lookup"><span data-stu-id="fd62e-3247">身分證統一編號</span></span> 
- <span data-ttu-id="fd62e-3248">國民身分證統一編號</span><span class="sxs-lookup"><span data-stu-id="fd62e-3248">國民身分證統一編號</span></span> 
- <span data-ttu-id="fd62e-3249">簽名</span><span class="sxs-lookup"><span data-stu-id="fd62e-3249">簽名</span></span> 
- <span data-ttu-id="fd62e-3250">蓋章</span><span class="sxs-lookup"><span data-stu-id="fd62e-3250">蓋章</span></span> 
- <span data-ttu-id="fd62e-3251">簽名或蓋章</span><span class="sxs-lookup"><span data-stu-id="fd62e-3251">簽名或蓋章</span></span> 
- <span data-ttu-id="fd62e-3252">簽章</span><span class="sxs-lookup"><span data-stu-id="fd62e-3252">簽章</span></span>   
   
## <a name="taiwan-passport-number"></a><span data-ttu-id="fd62e-3253">	Numéro de passeport Taïwan</span><span class="sxs-lookup"><span data-stu-id="fd62e-3253">Taiwan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-3254">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-3254">Format</span></span>

- <span data-ttu-id="fd62e-3255">Numéro de passeport biométrique: neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-3255">Biometric passport number: Nine digits</span></span>
- <span data-ttu-id="fd62e-3256">Numéro de passeport non biométrique: neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-3256">Non-biometric passport number: Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-3257">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-3257">Pattern</span></span>
<span data-ttu-id="fd62e-3258">Numéro de passeport biométrique:</span><span class="sxs-lookup"><span data-stu-id="fd62e-3258">Biometric passport number:</span></span>
- <span data-ttu-id="fd62e-3259">Le chiffre « 3 » </span><span class="sxs-lookup"><span data-stu-id="fd62e-3259">The digit "3"</span></span> 
- <span data-ttu-id="fd62e-3260">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-3260">Eight digits</span></span>

<span data-ttu-id="fd62e-3261">Numéro de passeport non biométrique:</span><span class="sxs-lookup"><span data-stu-id="fd62e-3261">Non-biometric passport number:</span></span>
- <span data-ttu-id="fd62e-3262">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-3262">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-3263">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-3263">Checksum</span></span>

<span data-ttu-id="fd62e-3264">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-3264">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-3265">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-3265">Definition</span></span>

<span data-ttu-id="fd62e-3266">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3266">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-3267">L’expression régulière Regex_taiwan_passport trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3267">The regular expression Regex_taiwan_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-3268">Un mot clé figurant dans la liste Keyword_taiwan_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3268">A keyword from Keyword_taiwan_passport is found.</span></span>

```xml
<!-- Taiwan Passport Number -->
<Entity id="e7251cb4-4c2c-41df-963e-924eb3dae04a" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_passport"/>
     <Match idRef="Keyword_taiwan_passport"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fd62e-3269">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-3269">Keywords</span></span>

#### <a name="keyword_taiwan_passport"></a><span data-ttu-id="fd62e-3270">Keyword_taiwan_passport</span><span class="sxs-lookup"><span data-stu-id="fd62e-3270">Keyword_taiwan_passport</span></span>

- <span data-ttu-id="fd62e-3271">ROC passport number</span><span class="sxs-lookup"><span data-stu-id="fd62e-3271">ROC passport number</span></span> 
- <span data-ttu-id="fd62e-3272">Passport number</span><span class="sxs-lookup"><span data-stu-id="fd62e-3272">Passport number</span></span> 
- <span data-ttu-id="fd62e-3273">Passport no</span><span class="sxs-lookup"><span data-stu-id="fd62e-3273">Passport no</span></span> 
- <span data-ttu-id="fd62e-3274">Passport Num</span><span class="sxs-lookup"><span data-stu-id="fd62e-3274">Passport Num</span></span> 
- <span data-ttu-id="fd62e-3275">Passport #</span><span class="sxs-lookup"><span data-stu-id="fd62e-3275">Passport #</span></span> 
- <span data-ttu-id="fd62e-3276">护照</span><span class="sxs-lookup"><span data-stu-id="fd62e-3276">护照</span></span> 
- <span data-ttu-id="fd62e-3277">中華民國護照</span><span class="sxs-lookup"><span data-stu-id="fd62e-3277">中華民國護照</span></span> 
- <span data-ttu-id="fd62e-3278">Zhōnghuá Mínguó hùzhào</span><span class="sxs-lookup"><span data-stu-id="fd62e-3278">Zhōnghuá Mínguó hùzhào</span></span>
   
## <a name="taiwan-resident-certificate-arctarc-number"></a><span data-ttu-id="fd62e-3279">Numéro de certificat de résident (ARC/TARC) Taïwan</span><span class="sxs-lookup"><span data-stu-id="fd62e-3279">Taiwan Resident Certificate (ARC/TARC) Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-3280">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-3280">Format</span></span>

<span data-ttu-id="fd62e-3281">10 lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-3281">10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-3282">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-3282">Pattern</span></span>

<span data-ttu-id="fd62e-3283">10 lettres et chiffres :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3283">10 letters and digits:</span></span>
- <span data-ttu-id="fd62e-3284">Deux lettres (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="fd62e-3284">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="fd62e-3285">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-3285">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-3286">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-3286">Checksum</span></span>

<span data-ttu-id="fd62e-3287">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-3287">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-3288">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-3288">Definition</span></span>

<span data-ttu-id="fd62e-3289">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3289">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-3290">L’expression régulière Regex_taiwan_resident_certificate trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3290">The regular expression Regex_taiwan_resident_certificate finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-3291">Un mot clé figurant dans la liste Keyword_taiwan_resident_certificate est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3291">A keyword from Keyword_taiwan_resident_certificate is found.</span></span>

```xml
<!-- Taiwan Resident Certificate (ARC/TARC) -->
<Entity id="48269fec-05ea-46ea-b326-f5623a58c6e9" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_resident_certificate"/>
     <Match idRef="Keyword_taiwan_resident_certificate"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fd62e-3292">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-3292">Keywords</span></span>

#### <a name="keyword_taiwan_resident_certificate"></a><span data-ttu-id="fd62e-3293">Keyword_taiwan_resident_certificate</span><span class="sxs-lookup"><span data-stu-id="fd62e-3293">Keyword_taiwan_resident_certificate</span></span>

- <span data-ttu-id="fd62e-3294">Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="fd62e-3294">Resident Certificate</span></span> 
- <span data-ttu-id="fd62e-3295">Resident Cert</span><span class="sxs-lookup"><span data-stu-id="fd62e-3295">Resident Cert</span></span> 
- <span data-ttu-id="fd62e-3296">Resident Cert.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3296">Resident Cert.</span></span> 
- <span data-ttu-id="fd62e-3297">Identification card</span><span class="sxs-lookup"><span data-stu-id="fd62e-3297">Identification card</span></span> 
- <span data-ttu-id="fd62e-3298">Alien Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="fd62e-3298">Alien Resident Certificate</span></span> 
- <span data-ttu-id="fd62e-3299">ARC</span><span class="sxs-lookup"><span data-stu-id="fd62e-3299">ARC</span></span> 
- <span data-ttu-id="fd62e-3300">Taiwan Area Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="fd62e-3300">Taiwan Area Resident Certificate</span></span> 
- <span data-ttu-id="fd62e-3301">TARC</span><span class="sxs-lookup"><span data-stu-id="fd62e-3301">TARC</span></span> 
- <span data-ttu-id="fd62e-3302">居留證</span><span class="sxs-lookup"><span data-stu-id="fd62e-3302">居留證</span></span> 
- <span data-ttu-id="fd62e-3303">外僑居留證</span><span class="sxs-lookup"><span data-stu-id="fd62e-3303">外僑居留證</span></span> 
- <span data-ttu-id="fd62e-3304">台灣地區居留證</span><span class="sxs-lookup"><span data-stu-id="fd62e-3304">台灣地區居留證</span></span> 

## <a name="thai-population-identification-code"></a><span data-ttu-id="fd62e-3305">Code d’identification du remplissage thaï</span><span class="sxs-lookup"><span data-stu-id="fd62e-3305">Thai Population Identification Code</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-3306">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-3306">Format</span></span>

<span data-ttu-id="fd62e-3307">13 chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-3307">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-3308">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-3308">Pattern</span></span>

<span data-ttu-id="fd62e-3309">13 chiffres :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3309">13 digits:</span></span>
- <span data-ttu-id="fd62e-3310">Le premier chiffre est différent de 0 ou de 9</span><span class="sxs-lookup"><span data-stu-id="fd62e-3310">First digit is not 0 or 9</span></span> 
- <span data-ttu-id="fd62e-3311">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-3311">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-3312">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-3312">Checksum</span></span>

<span data-ttu-id="fd62e-3313">Oui</span><span class="sxs-lookup"><span data-stu-id="fd62e-3313">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-3314">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-3314">Definition</span></span>

<span data-ttu-id="fd62e-3315">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3315">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-3316">La fonction Func_Thai_Citizen_Id trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3316">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-3317">Un mot clé depuis Keyword_Thai_Citizen_Id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3317">A keyword from Keyword_Thai_Citizen_Id is found.</span></span>

<span data-ttu-id="fd62e-3318">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3318">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-3319">La fonction Func_Thai_Citizen_Id trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3319">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-3320">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-3320">Keywords</span></span>

#### <a name="keyword_thai_citizen_id"></a><span data-ttu-id="fd62e-3321">Keyword_Thai_Citizen_Id</span><span class="sxs-lookup"><span data-stu-id="fd62e-3321">Keyword_Thai_Citizen_Id</span></span>

- <span data-ttu-id="fd62e-3322">ID Number</span><span class="sxs-lookup"><span data-stu-id="fd62e-3322">ID Number</span></span>
- <span data-ttu-id="fd62e-3323">Numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="fd62e-3323">Identification Number</span></span>
- <span data-ttu-id="fd62e-3324">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="fd62e-3324">บัตรประชาชน</span></span>
- <span data-ttu-id="fd62e-3325">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="fd62e-3325">รหัสบัตรประชาชน</span></span>
- <span data-ttu-id="fd62e-3326">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="fd62e-3326">บัตรประชาชน</span></span>
- <span data-ttu-id="fd62e-3327">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="fd62e-3327">รหัสบัตรประชาชน</span></span>
  
## <a name="turkish-national-identification-number"></a><span data-ttu-id="fd62e-3328">Numéro d’identification national turc</span><span class="sxs-lookup"><span data-stu-id="fd62e-3328">Turkish National Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-3329">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-3329">Format</span></span>

<span data-ttu-id="fd62e-3330">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-3330">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-3331">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-3331">Pattern</span></span>

<span data-ttu-id="fd62e-3332">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-3332">11 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-3333">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-3333">Checksum</span></span>

<span data-ttu-id="fd62e-3334">Oui</span><span class="sxs-lookup"><span data-stu-id="fd62e-3334">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-3335">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-3335">Definition</span></span>

<span data-ttu-id="fd62e-3336">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3336">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-3337">La fonction Func_Turkish_National_Id trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3337">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-3338">Un mot clé depuis Keyword_Turkish_National_Id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3338">A keyword from Keyword_Turkish_National_Id is found.</span></span>

<span data-ttu-id="fd62e-3339">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3339">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-3340">La fonction Func_Turkish_National_Id trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3340">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-3341">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-3341">Keywords</span></span>

#### <a name="keyword_turkish_national_id"></a><span data-ttu-id="fd62e-3342">Keyword_Turkish_National_Id</span><span class="sxs-lookup"><span data-stu-id="fd62e-3342">Keyword_Turkish_National_Id</span></span>

- <span data-ttu-id="fd62e-3343">TC Kimlik non</span><span class="sxs-lookup"><span data-stu-id="fd62e-3343">TC Kimlik No</span></span>
- <span data-ttu-id="fd62e-3344">TC Kimlik numarası</span><span class="sxs-lookup"><span data-stu-id="fd62e-3344">TC Kimlik numarası</span></span>
- <span data-ttu-id="fd62e-3345">Vatandaşlık numarası</span><span class="sxs-lookup"><span data-stu-id="fd62e-3345">Vatandaşlık numarası</span></span>
- <span data-ttu-id="fd62e-3346">Vatandaşlık non</span><span class="sxs-lookup"><span data-stu-id="fd62e-3346">Vatandaşlık no</span></span>

## <a name="uk-drivers-license-number"></a><span data-ttu-id="fd62e-p141">Numéro de permis de conduire Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="fd62e-p141">U.K. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-3349">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-3349">Format</span></span>

<span data-ttu-id="fd62e-3350">Combinaison de 18 lettres et chiffres au format spécifié</span><span class="sxs-lookup"><span data-stu-id="fd62e-3350">Combination of 18 letters and digits in the specified format</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-3351">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-3351">Pattern</span></span>

<span data-ttu-id="fd62e-3352">18 lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-3352">18 letters and digits:</span></span>
- <span data-ttu-id="fd62e-3353">Cinq lettres (ne respectent pas la casse) ou le chiffre « 9 » à la place d’une lettre</span><span class="sxs-lookup"><span data-stu-id="fd62e-3353">Five letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="fd62e-3354">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="fd62e-3354">One digit</span></span> 
- <span data-ttu-id="fd62e-3355">Cinq chiffres au format de date JJMMA pour la date de naissance</span><span class="sxs-lookup"><span data-stu-id="fd62e-3355">Five digits in the date format DDMMY for date of birth</span></span> 
- <span data-ttu-id="fd62e-3356">Deux lettres (ne respectent pas la casse) ou le chiffre « 9 » à la place d’une lettre</span><span class="sxs-lookup"><span data-stu-id="fd62e-3356">Two letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="fd62e-3357">Cinq chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-3357">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-3358">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-3358">Checksum</span></span>

<span data-ttu-id="fd62e-3359">Oui</span><span class="sxs-lookup"><span data-stu-id="fd62e-3359">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-3360">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-3360">Definition</span></span>

<span data-ttu-id="fd62e-3361">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3361">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-3362">La fonction Func_uk_drivers_license trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3362">The function Func_uk_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-3363">Un mot clé figurant dans la liste Keyword_uk_drivers_license est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3363">A keyword from Keyword_uk_drivers_license is found.</span></span>
- <span data-ttu-id="fd62e-3364">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3364">The checksum passes.</span></span>

```xml
<!-- U.K. Driver's License Number -->
<Entity id="f93de4be-d94c-40df-a8be-461738047551" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_uk_drivers_license" />
        <Match idRef="Keyword_uk_drivers_license" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fd62e-3365">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-3365">Keywords</span></span>

#### <a name="keyword_uk_drivers_license"></a><span data-ttu-id="fd62e-3366">Keyword_uk_drivers_license</span><span class="sxs-lookup"><span data-stu-id="fd62e-3366">Keyword_uk_drivers_license</span></span>

- <span data-ttu-id="fd62e-3367">DVLA</span><span class="sxs-lookup"><span data-stu-id="fd62e-3367">DVLA</span></span> 
- <span data-ttu-id="fd62e-3368">véhicule utilitaire léger</span><span class="sxs-lookup"><span data-stu-id="fd62e-3368">light vans</span></span> 
- <span data-ttu-id="fd62e-3369">quadbikes</span><span class="sxs-lookup"><span data-stu-id="fd62e-3369">quadbikes</span></span> 
- <span data-ttu-id="fd62e-3370">automobiles</span><span class="sxs-lookup"><span data-stu-id="fd62e-3370">motor cars</span></span> 
- <span data-ttu-id="fd62e-3371">125cc</span><span class="sxs-lookup"><span data-stu-id="fd62e-3371">125cc</span></span> 
- <span data-ttu-id="fd62e-3372">annexes</span><span class="sxs-lookup"><span data-stu-id="fd62e-3372">sidecar</span></span> 
- <span data-ttu-id="fd62e-3373">tricycles</span><span class="sxs-lookup"><span data-stu-id="fd62e-3373">tricycles</span></span> 
- <span data-ttu-id="fd62e-3374">Side</span><span class="sxs-lookup"><span data-stu-id="fd62e-3374">motorcycles</span></span> 
- <span data-ttu-id="fd62e-3375">permis de conduire plastifié</span><span class="sxs-lookup"><span data-stu-id="fd62e-3375">photocard licence</span></span> 
- <span data-ttu-id="fd62e-3376">apprentis conducteurs</span><span class="sxs-lookup"><span data-stu-id="fd62e-3376">learner drivers</span></span> 
- <span data-ttu-id="fd62e-3377">titulaire du permis</span><span class="sxs-lookup"><span data-stu-id="fd62e-3377">licence holder</span></span> 
- <span data-ttu-id="fd62e-3378">titulaires du permis</span><span class="sxs-lookup"><span data-stu-id="fd62e-3378">licence holders</span></span> 
- <span data-ttu-id="fd62e-3379">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-3379">driving licences</span></span> 
- <span data-ttu-id="fd62e-3380">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-3380">driving licence</span></span> 
- <span data-ttu-id="fd62e-3381">voiture à double commande</span><span class="sxs-lookup"><span data-stu-id="fd62e-3381">dual control car</span></span> 
   
## <a name="uk-electoral-roll-number"></a><span data-ttu-id="fd62e-p142">Numéro de liste électorale Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="fd62e-p142">U.K. Electoral Roll Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-3384">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-3384">Format</span></span>

<span data-ttu-id="fd62e-3385">Deux lettres suivies de 1 à 4 chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-3385">Two letters followed by 1-4 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-3386">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-3386">Pattern</span></span>

<span data-ttu-id="fd62e-3387">Deux lettres (ne respectant pas la casse) suivies de 1 à 4 chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-3387">Two letters (not case sensitive) followed by 1-4 numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-3388">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-3388">Checksum</span></span>

<span data-ttu-id="fd62e-3389">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-3389">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-3390">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-3390">Definition</span></span>

<span data-ttu-id="fd62e-3391">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3391">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-3392">L’expression régulière Regex_uk_electoral trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3392">The regular expression Regex_uk_electoral finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-3393">Un mot clé figurant dans la liste Keyword_uk_electoral est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3393">A keyword from Keyword_uk_electoral is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-3394">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-3394">Keywords</span></span>

#### <a name="keyword_uk_electoral"></a><span data-ttu-id="fd62e-3395">Keyword_uk_electoral</span><span class="sxs-lookup"><span data-stu-id="fd62e-3395">Keyword_uk_electoral</span></span>

- <span data-ttu-id="fd62e-3396">nomination au conseil</span><span class="sxs-lookup"><span data-stu-id="fd62e-3396">council nomination</span></span> 
- <span data-ttu-id="fd62e-3397">formulaire de nomination</span><span class="sxs-lookup"><span data-stu-id="fd62e-3397">nomination form</span></span> 
- <span data-ttu-id="fd62e-3398">registre électoral</span><span class="sxs-lookup"><span data-stu-id="fd62e-3398">electoral register</span></span> 
- <span data-ttu-id="fd62e-3399">liste électorale</span><span class="sxs-lookup"><span data-stu-id="fd62e-3399">electoral roll</span></span>

   
## <a name="uk-national-health-service-number"></a><span data-ttu-id="fd62e-p143">Numéro national des services de santé Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="fd62e-p143">U.K. National Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-3402">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-3402">Format</span></span>

<span data-ttu-id="fd62e-3403">10 à 17 chiffres séparés par des espaces</span><span class="sxs-lookup"><span data-stu-id="fd62e-3403">10-17 digits separated by spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-3404">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-3404">Pattern</span></span>

<span data-ttu-id="fd62e-3405">10 à 17 chiffres :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3405">10-17 digits:</span></span>
- <span data-ttu-id="fd62e-3406">3 ou 10 chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-3406">Either 3 or 10 digits</span></span> 
- <span data-ttu-id="fd62e-3407">Un espace</span><span class="sxs-lookup"><span data-stu-id="fd62e-3407">A space</span></span> 
- <span data-ttu-id="fd62e-3408">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-3408">Three digits</span></span> 
- <span data-ttu-id="fd62e-3409">Un espace</span><span class="sxs-lookup"><span data-stu-id="fd62e-3409">A space</span></span> 
- <span data-ttu-id="fd62e-3410">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-3410">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-3411">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-3411">Checksum</span></span>

<span data-ttu-id="fd62e-3412">Oui</span><span class="sxs-lookup"><span data-stu-id="fd62e-3412">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-3413">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-3413">Definition</span></span>

<span data-ttu-id="fd62e-3414">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3414">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-3415">La fonction Func_uk_nhs_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3415">The function Func_uk_nhs_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-3416">L’une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3416">One of the following is true:</span></span>
    - <span data-ttu-id="fd62e-3417">Un mot clé figurant dans la liste Keyword_uk_nhs_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3417">A keyword from Keyword_uk_nhs_number is found.</span></span>
    - <span data-ttu-id="fd62e-3418">Un mot clé figurant dans la liste Keyword_uk_nhs_number1 est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3418">A keyword from Keyword_uk_nhs_number1 is found.</span></span>
    - <span data-ttu-id="fd62e-3419">Un mot clé figurant dans la liste Keyword_uk_nhs_number_dob est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3419">A keyword from Keyword_uk_nhs_number_dob is found.</span></span>
- <span data-ttu-id="fd62e-3420">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3420">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-3421">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-3421">Keywords</span></span>
   
#### <a name="keyword_uk_nhs_number"></a><span data-ttu-id="fd62e-3422">Keyword_uk_nhs_number</span><span class="sxs-lookup"><span data-stu-id="fd62e-3422">Keyword_uk_nhs_number</span></span>

- <span data-ttu-id="fd62e-3423">service national de santé</span><span class="sxs-lookup"><span data-stu-id="fd62e-3423">national health service</span></span> 
- <span data-ttu-id="fd62e-3424">NHS</span><span class="sxs-lookup"><span data-stu-id="fd62e-3424">nhs</span></span> 
- <span data-ttu-id="fd62e-3425">administration des services de santé</span><span class="sxs-lookup"><span data-stu-id="fd62e-3425">health services authority</span></span> 
- <span data-ttu-id="fd62e-3426">administration de la santé</span><span class="sxs-lookup"><span data-stu-id="fd62e-3426">health authority</span></span>

#### <a name="keyword_uk_nhs_number1"></a><span data-ttu-id="fd62e-3427">Keyword_uk_nhs_number1</span><span class="sxs-lookup"><span data-stu-id="fd62e-3427">Keyword_uk_nhs_number1</span></span>

- <span data-ttu-id="fd62e-3428">id du patient</span><span class="sxs-lookup"><span data-stu-id="fd62e-3428">patient id</span></span> 
- <span data-ttu-id="fd62e-3429">identification du patient</span><span class="sxs-lookup"><span data-stu-id="fd62e-3429">patient identification</span></span> 
- <span data-ttu-id="fd62e-3430">n° patient</span><span class="sxs-lookup"><span data-stu-id="fd62e-3430">patient no</span></span> 
- <span data-ttu-id="fd62e-3431">numéro de patient</span><span class="sxs-lookup"><span data-stu-id="fd62e-3431">patient number</span></span>

#### <a name="keyword_uk_nhs_number_dob"></a><span data-ttu-id="fd62e-3432">Keyword_uk_nhs_number_dob</span><span class="sxs-lookup"><span data-stu-id="fd62e-3432">Keyword_uk_nhs_number_dob</span></span>

- <span data-ttu-id="fd62e-3433">GP</span><span class="sxs-lookup"><span data-stu-id="fd62e-3433">GP</span></span> 
- <span data-ttu-id="fd62e-3434">DOB</span><span class="sxs-lookup"><span data-stu-id="fd62e-3434">DOB</span></span> 
- <span data-ttu-id="fd62e-3435">D. O. B</span><span class="sxs-lookup"><span data-stu-id="fd62e-3435">D.O.B</span></span> 
- <span data-ttu-id="fd62e-3436">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="fd62e-3436">Date of Birth</span></span> 
- <span data-ttu-id="fd62e-3437">Birth Date</span><span class="sxs-lookup"><span data-stu-id="fd62e-3437">Birth Date</span></span> 
   
## <a name="uk-national-insurance-number-nino"></a><span data-ttu-id="fd62e-p144">Numéro d'assurance nationale (NINO) Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="fd62e-p144">U.K. National Insurance Number (NINO)</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-3440">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-3440">Format</span></span>

<span data-ttu-id="fd62e-3441">7 caractères ou 9 caractères séparés par des espaces ou des tirets</span><span class="sxs-lookup"><span data-stu-id="fd62e-3441">7 characters or 9 characters separated by spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-3442">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-3442">Pattern</span></span>

<span data-ttu-id="fd62e-3443">Deux modèles possibles:</span><span class="sxs-lookup"><span data-stu-id="fd62e-3443">Two possible patterns:</span></span>

- <span data-ttu-id="fd62e-3444">Deux lettres (valides NINOs Utilisez uniquement certains caractères dans ce préfixe, que ce modèle valide; ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="fd62e-3444">Two letters (valid NINOs use only certain characters in this prefix, which this pattern validates; not case sensitive)</span></span>
- <span data-ttu-id="fd62e-3445">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-3445">Six digits</span></span>
- <span data-ttu-id="fd62e-3446">«A», «B», «C» ou «d» (comme le préfixe, seuls certains caractères sont autorisés dans le suffixe; ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="fd62e-3446">Either 'A', 'B', 'C', or 'D' (like the prefix, only certain characters are allowed in the suffix; not case sensitive)</span></span>

<span data-ttu-id="fd62e-3447">OR</span><span class="sxs-lookup"><span data-stu-id="fd62e-3447">OR</span></span>

- <span data-ttu-id="fd62e-3448">Deux lettres</span><span class="sxs-lookup"><span data-stu-id="fd62e-3448">Two letters</span></span>
- <span data-ttu-id="fd62e-3449">Un espace ou un tiret</span><span class="sxs-lookup"><span data-stu-id="fd62e-3449">A space or dash</span></span>
- <span data-ttu-id="fd62e-3450">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-3450">Two digits</span></span>
- <span data-ttu-id="fd62e-3451">Un espace ou un tiret</span><span class="sxs-lookup"><span data-stu-id="fd62e-3451">A space or dash</span></span>
- <span data-ttu-id="fd62e-3452">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-3452">Two digits</span></span>
- <span data-ttu-id="fd62e-3453">Un espace ou un tiret</span><span class="sxs-lookup"><span data-stu-id="fd62e-3453">A space or dash</span></span>
- <span data-ttu-id="fd62e-3454">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-3454">Two digits</span></span>
- <span data-ttu-id="fd62e-3455">Un espace ou un tiret</span><span class="sxs-lookup"><span data-stu-id="fd62e-3455">A space or dash</span></span>
- <span data-ttu-id="fd62e-3456">«A», «B», «C» ou «d»</span><span class="sxs-lookup"><span data-stu-id="fd62e-3456">Either 'A', 'B', 'C', or 'D'</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-3457">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-3457">Checksum</span></span>

<span data-ttu-id="fd62e-3458">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-3458">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-3459">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-3459">Definition</span></span>

<span data-ttu-id="fd62e-3460">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3460">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-3461">La fonction Func_uk_nino trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3461">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-3462">Un mot clé figurant dans la liste Keyword_uk_nino est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3462">A keyword from Keyword_uk_nino is found.</span></span>

<span data-ttu-id="fd62e-3463">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3463">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-3464">La fonction Func_uk_nino trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3464">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-3465">Aucun mot clé figurant dans la liste Keyword_uk_nino n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3465">No keyword from Keyword_uk_nino is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-3466">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-3466">Keywords</span></span>

#### <a name="keyword_uk_nino"></a><span data-ttu-id="fd62e-3467">Keyword_uk_nino</span><span class="sxs-lookup"><span data-stu-id="fd62e-3467">Keyword_uk_nino</span></span>

- <span data-ttu-id="fd62e-3468">numéro d’assurance nationale</span><span class="sxs-lookup"><span data-stu-id="fd62e-3468">national insurance number</span></span> 
- <span data-ttu-id="fd62e-3469">cotisations sociales</span><span class="sxs-lookup"><span data-stu-id="fd62e-3469">national insurance contributions</span></span> 
- <span data-ttu-id="fd62e-3470">loi sur la protection</span><span class="sxs-lookup"><span data-stu-id="fd62e-3470">protection act</span></span> 
- <span data-ttu-id="fd62e-3471">cotisations</span><span class="sxs-lookup"><span data-stu-id="fd62e-3471">insurance</span></span> 
- <span data-ttu-id="fd62e-3472">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="fd62e-3472">social security number</span></span> 
- <span data-ttu-id="fd62e-3473">demande d’assurance</span><span class="sxs-lookup"><span data-stu-id="fd62e-3473">insurance application</span></span> 
- <span data-ttu-id="fd62e-3474">demande de soins médicaux</span><span class="sxs-lookup"><span data-stu-id="fd62e-3474">medical application</span></span> 
- <span data-ttu-id="fd62e-3475">assurance sociale</span><span class="sxs-lookup"><span data-stu-id="fd62e-3475">social insurance</span></span> 
- <span data-ttu-id="fd62e-3476">soins médicaux</span><span class="sxs-lookup"><span data-stu-id="fd62e-3476">medical attention</span></span> 
- <span data-ttu-id="fd62e-3477">sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="fd62e-3477">social security</span></span> 
- <span data-ttu-id="fd62e-3478">grande-bretagne</span><span class="sxs-lookup"><span data-stu-id="fd62e-3478">great britain</span></span> 
- <span data-ttu-id="fd62e-3479">cotisations</span><span class="sxs-lookup"><span data-stu-id="fd62e-3479">insurance</span></span>    
   
## <a name="us--uk-passport-number"></a><span data-ttu-id="fd62e-p145">Numéro de passeport États-Unis/Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="fd62e-p145">U.S. / U.K. Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-3482">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-3482">Format</span></span>

<span data-ttu-id="fd62e-3483">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-3483">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-3484">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-3484">Pattern</span></span>

<span data-ttu-id="fd62e-3485">Neuf chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="fd62e-3485">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-3486">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-3486">Checksum</span></span>

<span data-ttu-id="fd62e-3487">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-3487">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-3488">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-3488">Definition</span></span>

<span data-ttu-id="fd62e-3489">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3489">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-3490">La fonction Func_usa_uk_passport trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3490">The function Func_usa_uk_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-3491">Un mot clé figurant dans la liste Keyword_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3491">A keyword from Keyword_passport is found.</span></span>

```xml
<Entity id="178ec42a-18b4-47cc-85c7-d62c92fd67f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_usa_uk_passport" />
        <Match idRef="Keyword_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fd62e-3492">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-3492">Keywords</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="fd62e-3493">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="fd62e-3493">Keyword_passport</span></span>

- <span data-ttu-id="fd62e-3494">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="fd62e-3494">Passport Number</span></span> 
- <span data-ttu-id="fd62e-3495">N° de passeport</span><span class="sxs-lookup"><span data-stu-id="fd62e-3495">Passport No</span></span> 
- <span data-ttu-id="fd62e-3496"># Passeport</span><span class="sxs-lookup"><span data-stu-id="fd62e-3496">Passport #</span></span> 
- <span data-ttu-id="fd62e-3497">Tel #</span><span class="sxs-lookup"><span data-stu-id="fd62e-3497">Passport#</span></span> 
- <span data-ttu-id="fd62e-3498">PassportID</span><span class="sxs-lookup"><span data-stu-id="fd62e-3498">PassportID</span></span> 
- <span data-ttu-id="fd62e-3499">N ° passeport</span><span class="sxs-lookup"><span data-stu-id="fd62e-3499">Passportno</span></span> 
- <span data-ttu-id="fd62e-3500">passportnumber</span><span class="sxs-lookup"><span data-stu-id="fd62e-3500">passportnumber</span></span> 
- <span data-ttu-id="fd62e-3501">パスポート</span><span class="sxs-lookup"><span data-stu-id="fd62e-3501">パスポート</span></span> 
- <span data-ttu-id="fd62e-3502">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="fd62e-3502">パスポート番号</span></span> 
- <span data-ttu-id="fd62e-3503">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="fd62e-3503">パスポートのNum</span></span> 
- <span data-ttu-id="fd62e-3504">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="fd62e-3504">パスポート＃</span></span> 
- <span data-ttu-id="fd62e-3505">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="fd62e-3505">Numéro de passeport</span></span> 
- <span data-ttu-id="fd62e-3506">Passeport n°</span><span class="sxs-lookup"><span data-stu-id="fd62e-3506">Passeport n °</span></span> 
- <span data-ttu-id="fd62e-3507">Passeport numéro</span><span class="sxs-lookup"><span data-stu-id="fd62e-3507">Passeport Non</span></span> 
- <span data-ttu-id="fd62e-3508"># Passeport</span><span class="sxs-lookup"><span data-stu-id="fd62e-3508">Passeport #</span></span> 
- <span data-ttu-id="fd62e-3509">Passeport #</span><span class="sxs-lookup"><span data-stu-id="fd62e-3509">Passeport#</span></span> 
- <span data-ttu-id="fd62e-3510">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="fd62e-3510">PasseportNon</span></span> 
- <span data-ttu-id="fd62e-3511">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="fd62e-3511">Passeportn °</span></span> 
   
## <a name="us-bank-account-number"></a><span data-ttu-id="fd62e-3512">Numéro de compte bancaire États-Unis</span><span class="sxs-lookup"><span data-stu-id="fd62e-3512">U.S. Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-3513">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-3513">Format</span></span>

<span data-ttu-id="fd62e-3514">8-17 chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-3514">8-17 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-3515">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-3515">Pattern</span></span>

<span data-ttu-id="fd62e-3516">8 à 17 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="fd62e-3516">8-17 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-3517">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-3517">Checksum</span></span>

<span data-ttu-id="fd62e-3518">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-3518">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-3519">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-3519">Definition</span></span>

<span data-ttu-id="fd62e-3520">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3520">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-3521">L’expression régulière Regex_usa_bank_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3521">The regular expression Regex_usa_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-3522">Un mot clé figurant dans la liste Keyword_usa_Bank_Account est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3522">A keyword from Keyword_usa_Bank_Account is found.</span></span>

```xml
<!-- U.S. Bank Account Number -->
<Entity id="a2ce32a8-f935-4bb6-8e96-2a5157672e2c" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_usa_bank_account_number" />
        <Match idRef="Keyword_usa_Bank_Account" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="fd62e-3523">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-3523">Keywords</span></span>

#### <a name="keyword_usa_bank_account"></a><span data-ttu-id="fd62e-3524">Keyword_usa_Bank_Account</span><span class="sxs-lookup"><span data-stu-id="fd62e-3524">Keyword_usa_Bank_Account</span></span>

- <span data-ttu-id="fd62e-3525">Numéro de compte courant</span><span class="sxs-lookup"><span data-stu-id="fd62e-3525">Checking Account Number</span></span> 
- <span data-ttu-id="fd62e-3526">Compte courant</span><span class="sxs-lookup"><span data-stu-id="fd62e-3526">Checking Account</span></span> 
- <span data-ttu-id="fd62e-3527"># compte courant</span><span class="sxs-lookup"><span data-stu-id="fd62e-3527">Checking Account #</span></span> 
- <span data-ttu-id="fd62e-3528">Numéro compte courant</span><span class="sxs-lookup"><span data-stu-id="fd62e-3528">Checking Acct Number</span></span> 
- <span data-ttu-id="fd62e-3529"># compte courant</span><span class="sxs-lookup"><span data-stu-id="fd62e-3529">Checking Acct #</span></span> 
- <span data-ttu-id="fd62e-3530">N° de compte courant</span><span class="sxs-lookup"><span data-stu-id="fd62e-3530">Checking Acct No.</span></span> 
- <span data-ttu-id="fd62e-3531">N° de compte courant</span><span class="sxs-lookup"><span data-stu-id="fd62e-3531">Checking Account No.</span></span> 
- <span data-ttu-id="fd62e-3532">Numéro de compte bancaire</span><span class="sxs-lookup"><span data-stu-id="fd62e-3532">Bank Account Number</span></span> 
- <span data-ttu-id="fd62e-3533"># Compte bancaire</span><span class="sxs-lookup"><span data-stu-id="fd62e-3533">Bank Account #</span></span> 
- <span data-ttu-id="fd62e-3534">Numéro de compte bancaire</span><span class="sxs-lookup"><span data-stu-id="fd62e-3534">Bank Acct Number</span></span> 
- <span data-ttu-id="fd62e-3535"># Compte bancaire</span><span class="sxs-lookup"><span data-stu-id="fd62e-3535">Bank Acct #</span></span> 
- <span data-ttu-id="fd62e-3536">N° de compte bancaire</span><span class="sxs-lookup"><span data-stu-id="fd62e-3536">Bank Acct No.</span></span> 
- <span data-ttu-id="fd62e-3537">N° de compte bancaire</span><span class="sxs-lookup"><span data-stu-id="fd62e-3537">Bank Account No.</span></span> 
- <span data-ttu-id="fd62e-3538">Numéro de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="fd62e-3538">Savings Account Number</span></span> 
- <span data-ttu-id="fd62e-3539">Compte d’épargne.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3539">Savings Account.</span></span> 
- <span data-ttu-id="fd62e-3540">N° de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="fd62e-3540">Savings Account #</span></span> 
- <span data-ttu-id="fd62e-3541">Numéro de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="fd62e-3541">Savings Acct Number</span></span> 
- <span data-ttu-id="fd62e-3542"># compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="fd62e-3542">Savings Acct #</span></span> 
- <span data-ttu-id="fd62e-3543">N° de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="fd62e-3543">Savings Acct No.</span></span> 
- <span data-ttu-id="fd62e-3544">N° de compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="fd62e-3544">Savings Account No.</span></span> 
- <span data-ttu-id="fd62e-3545">Numéro de compte de débit</span><span class="sxs-lookup"><span data-stu-id="fd62e-3545">Debit Account Number</span></span> 
- <span data-ttu-id="fd62e-3546">Compte de débit</span><span class="sxs-lookup"><span data-stu-id="fd62e-3546">Debit Account</span></span> 
- <span data-ttu-id="fd62e-3547"># Compte de débit</span><span class="sxs-lookup"><span data-stu-id="fd62e-3547">Debit Account #</span></span> 
- <span data-ttu-id="fd62e-3548">Numéro de compte de débit</span><span class="sxs-lookup"><span data-stu-id="fd62e-3548">Debit Acct Number</span></span> 
- <span data-ttu-id="fd62e-3549"># Compte de débit</span><span class="sxs-lookup"><span data-stu-id="fd62e-3549">Debit Acct #</span></span> 
- <span data-ttu-id="fd62e-3550">N° de compte de débit</span><span class="sxs-lookup"><span data-stu-id="fd62e-3550">Debit Acct No.</span></span> 
- <span data-ttu-id="fd62e-3551">N° de compte de débit</span><span class="sxs-lookup"><span data-stu-id="fd62e-3551">Debit Account No.</span></span> 
   
## <a name="us-drivers-license-number"></a><span data-ttu-id="fd62e-3552">Numéro de permis de conduire États-Unis</span><span class="sxs-lookup"><span data-stu-id="fd62e-3552">U.S. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-3553">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-3553">Format</span></span>

<span data-ttu-id="fd62e-3554">Dépend de l’État</span><span class="sxs-lookup"><span data-stu-id="fd62e-3554">Depends on the state</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-3555">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-3555">Pattern</span></span>

<span data-ttu-id="fd62e-3556">Dépend de l’État, par exemple, New York :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3556">Depends on the state -- for example, New York:</span></span>
- <span data-ttu-id="fd62e-3557">Neuf chiffres au format DDD DDD DDD correspondront.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3557">Nine digits formatted like ddd ddd ddd will match.</span></span>
- <span data-ttu-id="fd62e-3558">Neuf chiffres au format ddddddddd ne correspondront pas.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3558">Nine digits like ddddddddd will not match.</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-3559">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-3559">Checksum</span></span>

<span data-ttu-id="fd62e-3560">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-3560">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-3561">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-3561">Definition</span></span>

<span data-ttu-id="fd62e-3562">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3562">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-3563">La fonction Func_new_york_drivers_license_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3563">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-3564">Un mot clé figurant dans la liste Keyword_[state_name]_drivers_license_name est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3564">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="fd62e-3565">Un mot clé figurant dans la liste Keyword_us_drivers_license est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3565">A keyword from Keyword_us_drivers_license is found.</span></span>

<span data-ttu-id="fd62e-3566">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3566">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-3567">La fonction Func_new_york_drivers_license_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3567">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-3568">Un mot clé figurant dans la liste Keyword_[state_name]_drivers_license_name est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3568">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="fd62e-3569">Un mot clé figurant dans la liste Keyword_us_drivers_license_abbreviations est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3569">A keyword from Keyword_us_drivers_license_abbreviations is found.</span></span>
- <span data-ttu-id="fd62e-3570">Aucun mot clé figurant dans la liste Keyword_us_drivers_license n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3570">No keyword from Keyword_us_drivers_license is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-3571">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-3571">Keywords</span></span>

#### <a name="keyword_us_drivers_license_abbreviations"></a><span data-ttu-id="fd62e-3572">Keyword_us_drivers_license_abbreviations</span><span class="sxs-lookup"><span data-stu-id="fd62e-3572">Keyword_us_drivers_license_abbreviations</span></span>

- <span data-ttu-id="fd62e-3573">LD</span><span class="sxs-lookup"><span data-stu-id="fd62e-3573">DL</span></span> 
- <span data-ttu-id="fd62e-3574">DISTRIBUTION</span><span class="sxs-lookup"><span data-stu-id="fd62e-3574">DLS</span></span> 
- <span data-ttu-id="fd62e-3575">CÈDE</span><span class="sxs-lookup"><span data-stu-id="fd62e-3575">CDL</span></span> 
- <span data-ttu-id="fd62e-3576">CDLS</span><span class="sxs-lookup"><span data-stu-id="fd62e-3576">CDLS</span></span> 
- <span data-ttu-id="fd62e-3577">ID</span><span class="sxs-lookup"><span data-stu-id="fd62e-3577">ID</span></span> 
- <span data-ttu-id="fd62e-3578">Codes</span><span class="sxs-lookup"><span data-stu-id="fd62e-3578">IDs</span></span> 
- <span data-ttu-id="fd62e-3579">LD #</span><span class="sxs-lookup"><span data-stu-id="fd62e-3579">DL#</span></span> 
- <span data-ttu-id="fd62e-3580">DISTRIBUTION #</span><span class="sxs-lookup"><span data-stu-id="fd62e-3580">DLS#</span></span> 
- <span data-ttu-id="fd62e-3581">CÈDE #</span><span class="sxs-lookup"><span data-stu-id="fd62e-3581">CDL#</span></span> 
- <span data-ttu-id="fd62e-3582">CDLS #</span><span class="sxs-lookup"><span data-stu-id="fd62e-3582">CDLS#</span></span> 
- <span data-ttu-id="fd62e-3583">Réf #</span><span class="sxs-lookup"><span data-stu-id="fd62e-3583">ID#</span></span>
- <span data-ttu-id="fd62e-3584">Codes #</span><span class="sxs-lookup"><span data-stu-id="fd62e-3584">IDs#</span></span> 
- <span data-ttu-id="fd62e-3585">Numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="fd62e-3585">ID number</span></span> 
- <span data-ttu-id="fd62e-3586">Numéros d’identification</span><span class="sxs-lookup"><span data-stu-id="fd62e-3586">ID numbers</span></span> 
- <span data-ttu-id="fd62e-3587">Profil</span><span class="sxs-lookup"><span data-stu-id="fd62e-3587">LIC</span></span> 
- <span data-ttu-id="fd62e-3588">Profil #</span><span class="sxs-lookup"><span data-stu-id="fd62e-3588">LIC#</span></span> 

#### <a name="keyword_us_drivers_license"></a><span data-ttu-id="fd62e-3589">Keyword_us_drivers_license</span><span class="sxs-lookup"><span data-stu-id="fd62e-3589">Keyword_us_drivers_license</span></span>

- <span data-ttu-id="fd62e-3590">DriverLic</span><span class="sxs-lookup"><span data-stu-id="fd62e-3590">DriverLic</span></span> 
- <span data-ttu-id="fd62e-3591">DriverLics</span><span class="sxs-lookup"><span data-stu-id="fd62e-3591">DriverLics</span></span> 
- <span data-ttu-id="fd62e-3592">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="fd62e-3592">DriverLicense</span></span> 
- <span data-ttu-id="fd62e-3593">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="fd62e-3593">DriverLicenses</span></span> 
- <span data-ttu-id="fd62e-3594">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-3594">Driver Lic</span></span> 
- <span data-ttu-id="fd62e-3595">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-3595">Driver Lics</span></span> 
- <span data-ttu-id="fd62e-3596">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-3596">Driver License</span></span> 
- <span data-ttu-id="fd62e-3597">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-3597">Driver Licenses</span></span> 
- <span data-ttu-id="fd62e-3598">DriversLic</span><span class="sxs-lookup"><span data-stu-id="fd62e-3598">DriversLic</span></span> 
- <span data-ttu-id="fd62e-3599">DriversLics</span><span class="sxs-lookup"><span data-stu-id="fd62e-3599">DriversLics</span></span> 
- <span data-ttu-id="fd62e-3600">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="fd62e-3600">DriversLicense</span></span> 
- <span data-ttu-id="fd62e-3601">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="fd62e-3601">DriversLicenses</span></span> 
- <span data-ttu-id="fd62e-3602">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-3602">Drivers Lic</span></span> 
- <span data-ttu-id="fd62e-3603">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-3603">Drivers Lics</span></span> 
- <span data-ttu-id="fd62e-3604">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-3604">Drivers License</span></span> 
- <span data-ttu-id="fd62e-3605">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-3605">Drivers Licenses</span></span> 
- <span data-ttu-id="fd62e-3606">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="fd62e-3606">Driver'Lic</span></span> 
- <span data-ttu-id="fd62e-3607">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="fd62e-3607">Driver'Lics</span></span> 
- <span data-ttu-id="fd62e-3608">Driver'License</span><span class="sxs-lookup"><span data-stu-id="fd62e-3608">Driver'License</span></span> 
- <span data-ttu-id="fd62e-3609">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="fd62e-3609">Driver'Licenses</span></span> 
- <span data-ttu-id="fd62e-3610">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-3610">Driver' Lic</span></span> 
- <span data-ttu-id="fd62e-3611">Permis conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-3611">Driver' Lics</span></span> 
- <span data-ttu-id="fd62e-3612">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-3612">Driver' License</span></span> 
- <span data-ttu-id="fd62e-3613">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-3613">Driver' Licenses</span></span>
- <span data-ttu-id="fd62e-3614">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="fd62e-3614">Driver'sLic</span></span> 
- <span data-ttu-id="fd62e-3615">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="fd62e-3615">Driver'sLics</span></span> 
- <span data-ttu-id="fd62e-3616">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="fd62e-3616">Driver'sLicense</span></span> 
- <span data-ttu-id="fd62e-3617">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="fd62e-3617">Driver'sLicenses</span></span> 
- <span data-ttu-id="fd62e-3618">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-3618">Driver's Lic</span></span> 
- <span data-ttu-id="fd62e-3619">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-3619">Driver's Lics</span></span> 
- <span data-ttu-id="fd62e-3620">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-3620">Driver's License</span></span> 
- <span data-ttu-id="fd62e-3621">Driver’s Licenses</span><span class="sxs-lookup"><span data-stu-id="fd62e-3621">Driver's Licenses</span></span> 
- <span data-ttu-id="fd62e-3622">numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="fd62e-3622">identification number</span></span> 
- <span data-ttu-id="fd62e-3623">numéros d’identification</span><span class="sxs-lookup"><span data-stu-id="fd62e-3623">identification numbers</span></span> 
- <span data-ttu-id="fd62e-3624"># identification</span><span class="sxs-lookup"><span data-stu-id="fd62e-3624">identification #</span></span> 
- <span data-ttu-id="fd62e-3625">carte d’identité</span><span class="sxs-lookup"><span data-stu-id="fd62e-3625">id card</span></span> 
- <span data-ttu-id="fd62e-3626">cartes d’identité</span><span class="sxs-lookup"><span data-stu-id="fd62e-3626">id cards</span></span> 
- <span data-ttu-id="fd62e-3627">carte d’identification</span><span class="sxs-lookup"><span data-stu-id="fd62e-3627">identification card</span></span> 
- <span data-ttu-id="fd62e-3628">cartes d’identification</span><span class="sxs-lookup"><span data-stu-id="fd62e-3628">identification cards</span></span> 
- <span data-ttu-id="fd62e-3629">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="fd62e-3629">DriverLic#</span></span> 
- <span data-ttu-id="fd62e-3630">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="fd62e-3630">DriverLics#</span></span> 
- <span data-ttu-id="fd62e-3631">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="fd62e-3631">DriverLicense#</span></span> 
- <span data-ttu-id="fd62e-3632">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="fd62e-3632">DriverLicenses#</span></span> 
- <span data-ttu-id="fd62e-3633">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-3633">Driver Lic#</span></span> 
- <span data-ttu-id="fd62e-3634">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-3634">Driver Lics#</span></span> 
- <span data-ttu-id="fd62e-3635">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-3635">Driver License#</span></span> 
- <span data-ttu-id="fd62e-3636">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-3636">Driver Licenses#</span></span> 
- <span data-ttu-id="fd62e-3637">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="fd62e-3637">DriversLic#</span></span> 
- <span data-ttu-id="fd62e-3638">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="fd62e-3638">DriversLics#</span></span> 
- <span data-ttu-id="fd62e-3639">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="fd62e-3639">DriversLicense#</span></span> 
- <span data-ttu-id="fd62e-3640">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="fd62e-3640">DriversLicenses#</span></span> 
- <span data-ttu-id="fd62e-3641">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-3641">Drivers Lic#</span></span> 
- <span data-ttu-id="fd62e-3642">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-3642">Drivers Lics#</span></span> 
- <span data-ttu-id="fd62e-3643">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-3643">Drivers License#</span></span> 
- <span data-ttu-id="fd62e-3644">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-3644">Drivers Licenses#</span></span> 
- <span data-ttu-id="fd62e-3645">Driver'Lic #</span><span class="sxs-lookup"><span data-stu-id="fd62e-3645">Driver'Lic#</span></span> 
- <span data-ttu-id="fd62e-3646">Driver'Lics #</span><span class="sxs-lookup"><span data-stu-id="fd62e-3646">Driver'Lics#</span></span> 
- <span data-ttu-id="fd62e-3647">Driver'License #</span><span class="sxs-lookup"><span data-stu-id="fd62e-3647">Driver'License#</span></span> 
- <span data-ttu-id="fd62e-3648">Driver'Licenses #</span><span class="sxs-lookup"><span data-stu-id="fd62e-3648">Driver'Licenses#</span></span> 
- <span data-ttu-id="fd62e-3649">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-3649">Driver' Lic#</span></span> 
- <span data-ttu-id="fd62e-3650">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-3650">Driver' Lics#</span></span> 
- <span data-ttu-id="fd62e-3651">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-3651">Driver' License#</span></span> 
- <span data-ttu-id="fd62e-3652">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-3652">Driver' Licenses#</span></span> 
- <span data-ttu-id="fd62e-3653">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="fd62e-3653">Driver'sLic#</span></span> 
- <span data-ttu-id="fd62e-3654">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="fd62e-3654">Driver'sLics#</span></span> 
- <span data-ttu-id="fd62e-3655">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="fd62e-3655">Driver'sLicense#</span></span> 
- <span data-ttu-id="fd62e-3656">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="fd62e-3656">Driver'sLicenses#</span></span> 
- <span data-ttu-id="fd62e-3657">#Permisconduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-3657">Driver's Lic#</span></span> 
- <span data-ttu-id="fd62e-3658">#Permisconduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-3658">Driver's Lics#</span></span> 
- <span data-ttu-id="fd62e-3659">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-3659">Driver's License#</span></span> 
- <span data-ttu-id="fd62e-3660">#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="fd62e-3660">Driver's Licenses#</span></span> 
- <span data-ttu-id="fd62e-3661"># carte d’identité</span><span class="sxs-lookup"><span data-stu-id="fd62e-3661">id card#</span></span> 
- <span data-ttu-id="fd62e-3662"># cartes d’identité</span><span class="sxs-lookup"><span data-stu-id="fd62e-3662">id cards#</span></span> 
- <span data-ttu-id="fd62e-3663">#carte d’identification</span><span class="sxs-lookup"><span data-stu-id="fd62e-3663">identification card#</span></span> 
- <span data-ttu-id="fd62e-3664">#cartes d’identification</span><span class="sxs-lookup"><span data-stu-id="fd62e-3664">identification cards#</span></span> 


#### <a name="keyword_state_name_drivers_license_name"></a><span data-ttu-id="fd62e-3665">Keyword_[state_name]_drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="fd62e-3665">Keyword_[state_name]_drivers_license_name</span></span>

- <span data-ttu-id="fd62e-3666">Abréviation de l’État (par exemple, « NY »)</span><span class="sxs-lookup"><span data-stu-id="fd62e-3666">State abbreviation (for example, "NY")</span></span> 
- <span data-ttu-id="fd62e-3667">Nom de l’État (par exemple, « New York »)</span><span class="sxs-lookup"><span data-stu-id="fd62e-3667">State name (for example, "New York")</span></span>    
   
## <a name="us-individual-taxpayer-identification-number-itin"></a><span data-ttu-id="fd62e-3668">Numéro d’identification fiscale individuel (ITIN) États-Unis</span><span class="sxs-lookup"><span data-stu-id="fd62e-3668">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-3669">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-3669">Format</span></span>

<span data-ttu-id="fd62e-3670">Neuf chiffres, le premier étant le « 9 », le quatrième le « 7 » ou le « 8 », éventuellement mis en forme avec des espaces ou des tirets</span><span class="sxs-lookup"><span data-stu-id="fd62e-3670">Nine digits that start with a "9" and contain a "7" or "8" as the fourth digit, optionally formatted with spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-3671">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-3671">Pattern</span></span>

<span data-ttu-id="fd62e-3672">Avec</span><span class="sxs-lookup"><span data-stu-id="fd62e-3672">Formatted:</span></span>
- <span data-ttu-id="fd62e-3673">Le chiffre « 9 »</span><span class="sxs-lookup"><span data-stu-id="fd62e-3673">The digit "9"</span></span> 
- <span data-ttu-id="fd62e-3674">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-3674">Two digits</span></span> 
- <span data-ttu-id="fd62e-3675">Un espace ou un tiret</span><span class="sxs-lookup"><span data-stu-id="fd62e-3675">A space or dash</span></span> 
- <span data-ttu-id="fd62e-3676">Un « 7 » ou un « 8 »</span><span class="sxs-lookup"><span data-stu-id="fd62e-3676">A "7" or "8"</span></span> 
- <span data-ttu-id="fd62e-3677">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="fd62e-3677">A digit</span></span> 
- <span data-ttu-id="fd62e-3678">Un espace ou tiret</span><span class="sxs-lookup"><span data-stu-id="fd62e-3678">A space, or dash</span></span> 
- <span data-ttu-id="fd62e-3679">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-3679">Four digits</span></span>

<span data-ttu-id="fd62e-3680">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-3680">Unformatted:</span></span>
- <span data-ttu-id="fd62e-3681">Le chiffre « 9 »</span><span class="sxs-lookup"><span data-stu-id="fd62e-3681">The digit "9"</span></span> 
- <span data-ttu-id="fd62e-3682">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-3682">Two digits</span></span> 
- <span data-ttu-id="fd62e-3683">Un « 7 » ou un « 8 »</span><span class="sxs-lookup"><span data-stu-id="fd62e-3683">A "7" or "8"</span></span> 
- <span data-ttu-id="fd62e-3684">Cinq chiffres</span><span class="sxs-lookup"><span data-stu-id="fd62e-3684">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-3685">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-3685">Checksum</span></span>

<span data-ttu-id="fd62e-3686">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-3686">No</span></span>

### <a name="definition"></a><span data-ttu-id="fd62e-3687">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-3687">Definition</span></span>

<span data-ttu-id="fd62e-3688">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3688">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-3689">La fonction Func_formatted_itin trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3689">The function Func_formatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-3690">Au moins une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3690">At least one of the following is true:</span></span>
    - <span data-ttu-id="fd62e-3691">Un mot clé figurant dans la liste Keyword_itin est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3691">A keyword from Keyword_itin is found.</span></span>
    - <span data-ttu-id="fd62e-3692">La fonction Func_us_address trouve une adresse au format correct.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3692">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="fd62e-3693">La fonction Func_us_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3693">The function Func_us_date finds a date in the right date format.</span></span>
    - <span data-ttu-id="fd62e-3694">Un mot clé figurant dans la liste Keyword_itin_collaborative est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3694">A keyword from Keyword_itin_collaborative is found.</span></span>

<span data-ttu-id="fd62e-3695">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3695">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-3696">La fonction Func_unformatted_itin trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3696">The function Func_unformatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-3697">Au moins une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3697">At least one of the following is true:</span></span>
    - <span data-ttu-id="fd62e-3698">Un mot clé figurant dans la liste Keyword_itin_collaborative est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3698">A keyword from Keyword_itin_collaborative is found.</span></span>
    - <span data-ttu-id="fd62e-3699">La fonction Func_us_address trouve une adresse au format correct.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3699">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="fd62e-3700">La fonction Func_us_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3700">The function Func_us_date finds a date in the right date format.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="fd62e-3701">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-3701">Keywords</span></span>

#### <a name="keyword_itin"></a><span data-ttu-id="fd62e-3702">Keyword_itin</span><span class="sxs-lookup"><span data-stu-id="fd62e-3702">Keyword_itin</span></span>

- <span data-ttu-id="fd62e-3703">redevable</span><span class="sxs-lookup"><span data-stu-id="fd62e-3703">taxpayer</span></span> 
- <span data-ttu-id="fd62e-3704">id fiscal</span><span class="sxs-lookup"><span data-stu-id="fd62e-3704">tax id</span></span> 
- <span data-ttu-id="fd62e-3705">identification fiscale</span><span class="sxs-lookup"><span data-stu-id="fd62e-3705">tax identification</span></span> 
- <span data-ttu-id="fd62e-3706">itin</span><span class="sxs-lookup"><span data-stu-id="fd62e-3706">itin</span></span> 
- <span data-ttu-id="fd62e-3707">SSN</span><span class="sxs-lookup"><span data-stu-id="fd62e-3707">ssn</span></span> 
- <span data-ttu-id="fd62e-3708">Etain</span><span class="sxs-lookup"><span data-stu-id="fd62e-3708">tin</span></span> 
- <span data-ttu-id="fd62e-3709">sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="fd62e-3709">social security</span></span> 
- <span data-ttu-id="fd62e-3710">contribuable</span><span class="sxs-lookup"><span data-stu-id="fd62e-3710">tax payer</span></span> 
- <span data-ttu-id="fd62e-3711">itins</span><span class="sxs-lookup"><span data-stu-id="fd62e-3711">itins</span></span> 
- <span data-ttu-id="fd62e-3712">taxi</span><span class="sxs-lookup"><span data-stu-id="fd62e-3712">taxid</span></span> 
- <span data-ttu-id="fd62e-3713">contribuable individuel</span><span class="sxs-lookup"><span data-stu-id="fd62e-3713">individual taxpayer</span></span> 

#### <a name="keyword_itin_collaborative"></a><span data-ttu-id="fd62e-3714">Keyword_itin_collaborative</span><span class="sxs-lookup"><span data-stu-id="fd62e-3714">Keyword_itin_collaborative</span></span>

- <span data-ttu-id="fd62e-3715">Licence</span><span class="sxs-lookup"><span data-stu-id="fd62e-3715">License</span></span> 
- <span data-ttu-id="fd62e-3716">LD</span><span class="sxs-lookup"><span data-stu-id="fd62e-3716">DL</span></span> 
- <span data-ttu-id="fd62e-3717">DOB</span><span class="sxs-lookup"><span data-stu-id="fd62e-3717">DOB</span></span> 
- <span data-ttu-id="fd62e-3718">Birthdate</span><span class="sxs-lookup"><span data-stu-id="fd62e-3718">Birthdate</span></span> 
- <span data-ttu-id="fd62e-3719">Birthday</span><span class="sxs-lookup"><span data-stu-id="fd62e-3719">Birthday</span></span> 
- <span data-ttu-id="fd62e-3720">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="fd62e-3720">Date of Birth</span></span> 
   
## <a name="us-social-security-number-ssn"></a><span data-ttu-id="fd62e-3721">Numéro de sécurité sociale (SSN) États-Unis</span><span class="sxs-lookup"><span data-stu-id="fd62e-3721">U.S. Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="fd62e-3722">Format</span><span class="sxs-lookup"><span data-stu-id="fd62e-3722">Format</span></span>

<span data-ttu-id="fd62e-3723">9 chiffres, qui peuvent être mis en forme ou non mis en forme</span><span class="sxs-lookup"><span data-stu-id="fd62e-3723">9 digits, which may be in a formatted or unformatted pattern</span></span>

> [!NOTE]
> <span data-ttu-id="fd62e-3724">La mise en forme d’un numéro de sécurité sociale émis avant le milieu de l’année 2011 est fixe et certaines parties du numéro doivent se situer dans certaines plages pour qu’il soit valide (mais il n’y a pas de somme de contrôle).</span><span class="sxs-lookup"><span data-stu-id="fd62e-3724">If issued before mid-2011, an SSN has strong formatting where certain parts of the number must fall within certain ranges to be valid (but there's no checksum).</span></span>

### <a name="pattern"></a><span data-ttu-id="fd62e-3725">Modèle</span><span class="sxs-lookup"><span data-stu-id="fd62e-3725">Pattern</span></span>

<span data-ttu-id="fd62e-3726">Quatre fonctions permettent de rechercher des numéros de sécurité sociale avec quatre différents modèles :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3726">Four functions look for SSNs in four different patterns:</span></span>
- <span data-ttu-id="fd62e-3727">Func_ssn recherche des numéros de sécurité sociale avec une mise en forme fixe d’avant l’année 2011, mis en forme avec des tirets ou des espaces (ddd-dd-dddd OU ddd dd dddd)</span><span class="sxs-lookup"><span data-stu-id="fd62e-3727">Func_ssn finds SSNs with pre-2011 strong formatting that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="fd62e-3728">Func_unformatted_ssn recherche des numéros de sécurité sociale avec une mise en forme fixe d’avant l’année 2011, avec neuf chiffres consécutifs non mis en forme (ddddddddd)</span><span class="sxs-lookup"><span data-stu-id="fd62e-3728">Func_unformatted_ssn finds SSNs with pre-2011 strong formatting that are unformatted as nine consecutive digits (ddddddddd)</span></span>
- <span data-ttu-id="fd62e-3729">Func_randomized_formatted_ssn recherche des numéros de sécurité sociale d’après l’année 2011, mis en forme avec des tirets ou des espaces  (ddd-dd-dddd OU ddd dd dddd)</span><span class="sxs-lookup"><span data-stu-id="fd62e-3729">Func_randomized_formatted_ssn finds post-2011 SSNs that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="fd62e-3730">Func_randomized_unformatted_ssn recherche des numéros de sécurité sociale d’après l’année 2011, avec neuf chiffres consécutifs non mis en forme (ddddddddd)</span><span class="sxs-lookup"><span data-stu-id="fd62e-3730">Func_randomized_unformatted_ssn finds post-2011 SSNs that are unformatted as nine consecutive digits (ddddddddd)</span></span>

### <a name="checksum"></a><span data-ttu-id="fd62e-3731">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="fd62e-3731">Checksum</span></span>

<span data-ttu-id="fd62e-3732">Non</span><span class="sxs-lookup"><span data-stu-id="fd62e-3732">No</span></span>


### <a name="definition"></a><span data-ttu-id="fd62e-3733">Définition</span><span class="sxs-lookup"><span data-stu-id="fd62e-3733">Definition</span></span>

<span data-ttu-id="fd62e-3734">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3734">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-3735">La fonction Func_ssn trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3735">The function Func_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-3736">Un mot clé figurant dans la liste Keyword_ssn est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3736">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="fd62e-3737">La fonction Func_us_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3737">The function Func_us_date finds a date in the right date format.</span></span>
- <span data-ttu-id="fd62e-3738">La fonction Func_us_address trouve une adresse au format correct.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3738">The function Func_us_address finds an address in the right format.</span></span>

<span data-ttu-id="fd62e-3739">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3739">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-3740">La fonction Func_unformatted_ssn trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3740">The function Func_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-3741">Un mot clé figurant dans la liste Keyword_ssn est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3741">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="fd62e-3742">La fonction Func_us_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3742">The function Func_us_date finds a date in the right date format.</span></span>
- <span data-ttu-id="fd62e-3743">La fonction Func_us_address trouve une adresse au format correct.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3743">The function Func_us_address finds an address in the right format.</span></span>

<span data-ttu-id="fd62e-3744">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3744">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-3745">La fonction Func_randomized_formatted_ssn trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3745">The function Func_randomized_formatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-3746">Un mot clé figurant dans la liste Keyword_ssn est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3746">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="fd62e-3747">La fonction Func_us_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3747">The function Func_us_date finds a date in the right date format.</span></span>
- <span data-ttu-id="fd62e-3748">La fonction Func_us_address trouve une adresse au format correct.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3748">The function Func_us_address finds an address in the right format.</span></span>

<span data-ttu-id="fd62e-3749">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 55 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="fd62e-3749">A DLP policy is 55% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-3750">La fonction Func_randomized_unformatted_ssn trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3750">The function Func_randomized_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-3751">Un mot clé figurant dans la liste Keyword_ssn est trouvé.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3751">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="fd62e-3752">La fonction Func_us_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3752">The function Func_us_date finds a date in the right date format.</span></span>
- <span data-ttu-id="fd62e-3753">La fonction Func_us_address trouve une adresse au format correct.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3753">The function Func_us_address finds an address in the right format.</span></span>

<span data-ttu-id="fd62e-3754">Une stratégie DLP est sûre à 40% d’avoir détecté ce type d’informations sensibles si, dans une proximité de 300 caractères:</span><span class="sxs-lookup"><span data-stu-id="fd62e-3754">A DLP policy is 40% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="fd62e-3755">La fonction Func_ssn trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3755">The function Func_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-3756">La fonction Func_unformatted_ssn ne trouve pas de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3756">The function Func_unformatted_ssn does not find content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-3757">La fonction Func_randomized_unformatted_ssn ne trouve pas le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3757">The function Func_randomized_unformatted_ssn does not find content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-3758">Un mot clé depuis Keyword_ssn est introuvable.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3758">A keyword from Keyword_ssn is not found.</span></span>
 
<span data-ttu-id="fd62e-3759">Ou</span><span class="sxs-lookup"><span data-stu-id="fd62e-3759">Or</span></span>

- <span data-ttu-id="fd62e-3760">La fonction Func_randomized_formatted_ssn trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3760">The function Func_randomized_formatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-3761">La fonction Func_unformatted_ssn ne trouve pas de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3761">The function Func_unformatted_ssn does not find content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-3762">La fonction Func_randomized_unformatted_ssn ne trouve pas le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3762">The function Func_randomized_unformatted_ssn does not find content that matches the pattern.</span></span>
- <span data-ttu-id="fd62e-3763">Un mot clé depuis Keyword_ssn est introuvable.</span><span class="sxs-lookup"><span data-stu-id="fd62e-3763">A keyword from Keyword_ssn is not found.</span></span>

```xml
<!-- U.S. Social Security Number (SSN) -->
  <Entity id="a44669fe-0d48-453d-a9b1-2cc83f2cba77" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_ssn" />
        <Any minMatches="1">
          <Match idRef="Keyword_ssn" />
          <Match idRef="Func_us_date" />
          <Match idRef="Func_us_address" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_unformatted_ssn" />
        <Match idRef="Keyword_ssn" />
        <Any minMatches="1">
          <Match idRef="Func_us_date" />
          <Match idRef="Func_us_address" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="65">
        <IdMatch idRef="Func_randomized_formatted_ssn" />
        <Any minMatches="1">
          <Match idRef="Keyword_ssn" />
          <Match idRef="Func_us_date" />
          <Match idRef="Func_us_address" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="55">
        <IdMatch idRef="Func_randomized_unformatted_ssn" />
        <Match idRef="Keyword_ssn" />
        <Any minMatches="1">
          <Match idRef="Func_us_date" />
          <Match idRef="Func_us_address" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="40">
        <IdMatch idRef="Func_ssn" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Func_unformatted_ssn" />
          <Match idRef="Func_randomized_unformatted_ssn" />
          <Match idRef="Keyword_ssn" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="40">
        <IdMatch idRef="Func_randomized_formatted_ssn" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Func_unformatted_ssn" />
          <Match idRef="Func_randomized_unformatted_ssn" />
          <Match idRef="Keyword_ssn" />
        </Any>
      </Pattern>
    </Entity>
```

### <a name="keywords"></a><span data-ttu-id="fd62e-3764">Mots clés</span><span class="sxs-lookup"><span data-stu-id="fd62e-3764">Keywords</span></span>

#### <a name="keyword_ssn"></a><span data-ttu-id="fd62e-3765">Keyword_ssn</span><span class="sxs-lookup"><span data-stu-id="fd62e-3765">Keyword_ssn</span></span>

- <span data-ttu-id="fd62e-3766">Sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="fd62e-3766">Social Security</span></span> 
- <span data-ttu-id="fd62e-3767"># sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="fd62e-3767">Social Security#</span></span> 
- <span data-ttu-id="fd62e-3768">Sécu sociale</span><span class="sxs-lookup"><span data-stu-id="fd62e-3768">Soc Sec</span></span> 
- <span data-ttu-id="fd62e-3769">SSN</span><span class="sxs-lookup"><span data-stu-id="fd62e-3769">SSN</span></span> 
- <span data-ttu-id="fd62e-3770">NUMÉROS</span><span class="sxs-lookup"><span data-stu-id="fd62e-3770">SSNS</span></span> 
- <span data-ttu-id="fd62e-3771">SSN #</span><span class="sxs-lookup"><span data-stu-id="fd62e-3771">SSN#</span></span> 
- <span data-ttu-id="fd62e-3772">SOCIALE #</span><span class="sxs-lookup"><span data-stu-id="fd62e-3772">SS#</span></span> 
- <span data-ttu-id="fd62e-3773">Identifiant SSID</span><span class="sxs-lookup"><span data-stu-id="fd62e-3773">SSID</span></span> 
   

