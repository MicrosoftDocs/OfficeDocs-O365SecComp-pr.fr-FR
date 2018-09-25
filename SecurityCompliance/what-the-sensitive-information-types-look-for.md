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
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
ms.assetid: fd505979-76be-4d9f-b459-abef3fc9e86b
description: Prévention des pertes de données (DLP) de sécurité Office 365 &amp; centre de conformité inclut 80 types d’informations sensibles qui sont prêts à utiliser dans vos stratégies DLP. Cette rubrique répertorie tous ces types d’informations sensibles et illustre une stratégie DLP lorsqu’il détecte chaque type.
ms.openlocfilehash: 5097227d8efa833f255631febde50b937add48ef
ms.sourcegitcommit: ede6230c2df398dc0a633e8f32ee0bfede0d5142
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "25002687"
---
# <a name="what-the-sensitive-information-types-look-for"></a><span data-ttu-id="abe74-104">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="abe74-104">What the sensitive information types look for</span></span>

<span data-ttu-id="abe74-p102">Prévention des pertes de données (DLP) de sécurité Office 365 &amp; centre de conformité inclut de nombreux types d’informations sensibles qui sont prêts à utiliser dans vos stratégies DLP. Cette rubrique répertorie tous ces types d’informations sensibles et illustre une stratégie DLP lorsqu’il détecte chaque type. Un type d’informations sensibles est défini par un modèle qui peut être identifié par une expression régulière ou une fonction. En outre, la preuve corroborante tels que des mots clés et les totaux de contrôle peut servir à identifier un type d’informations sensibles. Proximité et niveau de confiance sont également utilisés dans le processus d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="abe74-p102">Data loss prevention (DLP) in the Office 365 Security &amp; Compliance Center includes many sensitive information types that are ready for you to use in your DLP policies. This topic lists all of these sensitive information types and shows what a DLP policy looks for when it detects each type. A sensitive information type is defined by a pattern that can be identified by a regular expression or a function. In addition, corroborative evidence such as keywords and checksums can be used to identify a sensitive information type. Confidence level and proximity are also used in the evaluation process.</span></span>
  
## <a name="aba-routing-number"></a><span data-ttu-id="abe74-110">Numéro de routage ABA</span><span class="sxs-lookup"><span data-stu-id="abe74-110">ABA Routing Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-111">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-111">Format</span></span>

<span data-ttu-id="abe74-112">9 chiffres mis en forme ou non mis en forme</span><span class="sxs-lookup"><span data-stu-id="abe74-112">9 digits which may be in a formatted or unformatted pattern</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-113">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-113">Pattern</span></span>

<span data-ttu-id="abe74-114">Mis en forme :</span><span class="sxs-lookup"><span data-stu-id="abe74-114">Formatted:</span></span>
- <span data-ttu-id="abe74-115">Quatre chiffres commençant par 0, 1, 2, 3, 6, 7 ou 8</span><span class="sxs-lookup"><span data-stu-id="abe74-115">Four digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span>
- <span data-ttu-id="abe74-116">Un trait d’union</span><span class="sxs-lookup"><span data-stu-id="abe74-116">A hyphen</span></span>
- <span data-ttu-id="abe74-117">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-117">Four digits</span></span>
- <span data-ttu-id="abe74-118">Un trait d’union</span><span class="sxs-lookup"><span data-stu-id="abe74-118">A hyphen</span></span>
- <span data-ttu-id="abe74-119">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="abe74-119">A digit</span></span>

<span data-ttu-id="abe74-120">Non formatée : 9 chiffres consécutifs commencent par 0, 1, 2, 3, 6, 7 ou 8</span><span class="sxs-lookup"><span data-stu-id="abe74-120">Unformatted: 9 consecutive digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span> 

### <a name="checksum"></a><span data-ttu-id="abe74-121">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-121">Checksum</span></span>

<span data-ttu-id="abe74-122">Non</span><span class="sxs-lookup"><span data-stu-id="abe74-122">No</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-123">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-123">Definition</span></span>

<span data-ttu-id="abe74-124">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-124">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-125">La fonction Func_aba_routing trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-125">The function Func_aba_routing finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-126">Un mot clé figurant dans la liste Keyword_ABA_Routing est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-126">A keyword from Keyword_ABA_Routing is found.</span></span>

```
<!-- ABA Routing Number -->
<Entity id="cb353f78-2b72-4c3c-8827-92ebe4f69fdf" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_aba_routing" />
        <Match idRef="Keyword_ABA_Routing" />
      </Pattern>
 </Entity>
```


### <a name="keywords"></a><span data-ttu-id="abe74-127">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-127">Keywords</span></span>

#### <a name="keywordabarouting"></a><span data-ttu-id="abe74-128">Keyword_ABA_Routing</span><span class="sxs-lookup"><span data-stu-id="abe74-128">Keyword_ABA_Routing</span></span>

- <span data-ttu-id="abe74-129">aba</span><span class="sxs-lookup"><span data-stu-id="abe74-129">aba</span></span>
- <span data-ttu-id="abe74-130">
# aba</span><span class="sxs-lookup"><span data-stu-id="abe74-130">aba #</span></span>
- <span data-ttu-id="abe74-131">
# routage aba</span><span class="sxs-lookup"><span data-stu-id="abe74-131">aba routing #</span></span>
- <span data-ttu-id="abe74-132">numéro de routage ABA</span><span class="sxs-lookup"><span data-stu-id="abe74-132">aba routing number</span></span>
- <span data-ttu-id="abe74-133">
#aba</span><span class="sxs-lookup"><span data-stu-id="abe74-133">aba#</span></span>
- <span data-ttu-id="abe74-134">
#routageaba</span><span class="sxs-lookup"><span data-stu-id="abe74-134">abarouting#</span></span>
- <span data-ttu-id="abe74-135">
numéro aba</span><span class="sxs-lookup"><span data-stu-id="abe74-135">aba number</span></span>
- <span data-ttu-id="abe74-136">
numéroroutageaba</span><span class="sxs-lookup"><span data-stu-id="abe74-136">abaroutingnumber</span></span>
- <span data-ttu-id="abe74-137">
# routage american bank association</span><span class="sxs-lookup"><span data-stu-id="abe74-137">american bank association routing #</span></span>
- <span data-ttu-id="abe74-138">
numéro de routage american bank association</span><span class="sxs-lookup"><span data-stu-id="abe74-138">american bank association routing number</span></span>
- <span data-ttu-id="abe74-139">
#routageamericanbankassociation</span><span class="sxs-lookup"><span data-stu-id="abe74-139">americanbankassociationrouting#</span></span>
- <span data-ttu-id="abe74-140">
numéroderoutageamericanbankassociation</span><span class="sxs-lookup"><span data-stu-id="abe74-140">americanbankassociationroutingnumber</span></span>
- <span data-ttu-id="abe74-141">
numéro de routage bancaire</span><span class="sxs-lookup"><span data-stu-id="abe74-141">bank routing number</span></span>
- <span data-ttu-id="abe74-142">
#routagebancaire</span><span class="sxs-lookup"><span data-stu-id="abe74-142">bankrouting#</span></span>
- <span data-ttu-id="abe74-143">
numéroderoutagebancaire</span><span class="sxs-lookup"><span data-stu-id="abe74-143">bankroutingnumber</span></span>
- <span data-ttu-id="abe74-144">
numéro de routage</span><span class="sxs-lookup"><span data-stu-id="abe74-144">routing transit number</span></span>
- <span data-ttu-id="abe74-145">
RTN
</span><span class="sxs-lookup"><span data-stu-id="abe74-145">RTN</span></span> 
   
## <a name="argentina-national-identity-dni-number"></a><span data-ttu-id="abe74-146">Numéro d’identité nationale (DNI) pour l’Argentine</span><span class="sxs-lookup"><span data-stu-id="abe74-146">Argentina National Identity (DNI) Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-147">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-147">Format</span></span>

<span data-ttu-id="abe74-148">Huit chiffres séparés par des points</span><span class="sxs-lookup"><span data-stu-id="abe74-148">Eight digits separated by periods</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-149">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-149">Pattern</span></span>

<span data-ttu-id="abe74-150">Huit chiffres :</span><span class="sxs-lookup"><span data-stu-id="abe74-150">Eight digits:</span></span>
- <span data-ttu-id="abe74-151">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-151">Two digits</span></span>
- <span data-ttu-id="abe74-152">Un point </span><span class="sxs-lookup"><span data-stu-id="abe74-152">A period</span></span>
- <span data-ttu-id="abe74-153">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-153">Three digits</span></span>
- <span data-ttu-id="abe74-154">Un point </span><span class="sxs-lookup"><span data-stu-id="abe74-154">A period</span></span>
- <span data-ttu-id="abe74-155">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-155">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-156">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-156">Checksum</span></span>

<span data-ttu-id="abe74-157">Non</span><span class="sxs-lookup"><span data-stu-id="abe74-157">No</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-158">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-158">Definition</span></span>

<span data-ttu-id="abe74-159">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-159">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-160">L’expression régulière Regex_argentina_national_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-160">The regular expression Regex_argentina_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-161">Un mot clé figurant dans la liste Keyword_argentina_national_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-161">A keyword from Keyword_argentina_national_id is found.</span></span>

```
<!-- Argentina National Identity (DNI) Number -->
<Entity id="eefbb00e-8282-433c-8620-8f1da3bffdb2" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_argentina_national_id"/>
      <Match idRef="Keyword_argentina_national_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe74-162">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-162">Keywords</span></span>

#### <a name="keywordargentinanationalid"></a><span data-ttu-id="abe74-163">Keyword_argentina_national_id</span><span class="sxs-lookup"><span data-stu-id="abe74-163">Keyword_argentina_national_id</span></span>

- <span data-ttu-id="abe74-164">Argentina National Identity number
</span><span class="sxs-lookup"><span data-stu-id="abe74-164">Argentina National Identity number</span></span> 
- <span data-ttu-id="abe74-165">Identité</span><span class="sxs-lookup"><span data-stu-id="abe74-165">Identity</span></span> 
- <span data-ttu-id="abe74-166">Carte nationale d’identification</span><span class="sxs-lookup"><span data-stu-id="abe74-166">Identification National Identity Card</span></span> 
- <span data-ttu-id="abe74-167">DNI
</span><span class="sxs-lookup"><span data-stu-id="abe74-167">DNI</span></span> 
- <span data-ttu-id="abe74-168">Carte réseau Registre National de personnes</span><span class="sxs-lookup"><span data-stu-id="abe74-168">NIC National Registry of Persons</span></span> 
- <span data-ttu-id="abe74-169">Documento Nacional de Identidad
</span><span class="sxs-lookup"><span data-stu-id="abe74-169">Documento Nacional de Identidad</span></span> 
- <span data-ttu-id="abe74-170">Registro Nacional de las Personas
</span><span class="sxs-lookup"><span data-stu-id="abe74-170">Registro Nacional de las Personas</span></span> 
- <span data-ttu-id="abe74-171">Identidad
</span><span class="sxs-lookup"><span data-stu-id="abe74-171">Identidad</span></span> 
- <span data-ttu-id="abe74-172">Identificación
</span><span class="sxs-lookup"><span data-stu-id="abe74-172">Identificación</span></span> 
   
## <a name="australia-bank-account-number"></a><span data-ttu-id="abe74-173">Numéro de compte bancaire Australie</span><span class="sxs-lookup"><span data-stu-id="abe74-173">Australia Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-174">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-174">Format</span></span>

<span data-ttu-id="abe74-175">6 à 10 chiffres avec ou sans le numéro d’agence bancaire de l’État</span><span class="sxs-lookup"><span data-stu-id="abe74-175">6-10 digits with or without a bank state branch number</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-176">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-176">Pattern</span></span>

<span data-ttu-id="abe74-p103">Numéro de compte est de 6 à 10 chiffres. Numéro de succursale bancaire Australie état :</span><span class="sxs-lookup"><span data-stu-id="abe74-p103">Account number is 6-10 digits. Australia bank state branch number:</span></span>
- <span data-ttu-id="abe74-179">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-179">Three digits</span></span> 
- <span data-ttu-id="abe74-180">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="abe74-180">A hyphen</span></span> 
- <span data-ttu-id="abe74-181">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-181">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-182">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-182">Checksum</span></span>

<span data-ttu-id="abe74-183">Non</span><span class="sxs-lookup"><span data-stu-id="abe74-183">No</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-184">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-184">Definition</span></span>

<span data-ttu-id="abe74-185">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-185">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-186">L’expression régulière Regex_australia_bank_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-186">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="abe74-187">Un mot clé figurant dans la liste Keyword_australia_bank_account_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-187">A keyword from Keyword_australia_bank_account_number is found.</span></span>
- <span data-ttu-id="abe74-188">L’expression régulière Regex_australia_bank_account_number_bsb trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-188">The regular expression Regex_australia_bank_account_number_bsb finds content that matches the pattern.</span></span>

<span data-ttu-id="abe74-189">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-189">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-190">L’expression régulière Regex_australia_bank_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-190">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="abe74-191">Un mot clé figurant dans la liste Keyword_australia_bank_account_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-191">A keyword from Keyword_australia_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-192">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-192">Keywords</span></span>

#### <a name="keywordaustraliabankaccountnumber"></a><span data-ttu-id="abe74-193">Keyword_australia_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="abe74-193">Keyword_australia_bank_account_number</span></span>

- <span data-ttu-id="abe74-194">code swift banque</span><span class="sxs-lookup"><span data-stu-id="abe74-194">swift bank code</span></span>
- <span data-ttu-id="abe74-195">
banque correspondante</span><span class="sxs-lookup"><span data-stu-id="abe74-195">correspondent bank</span></span>
- <span data-ttu-id="abe74-196">
devise de base</span><span class="sxs-lookup"><span data-stu-id="abe74-196">base currency</span></span>
- <span data-ttu-id="abe74-197">
compte aux États-Unis</span><span class="sxs-lookup"><span data-stu-id="abe74-197">usa account</span></span>
- <span data-ttu-id="abe74-198">
adresse du titulaire</span><span class="sxs-lookup"><span data-stu-id="abe74-198">holder address</span></span>
- <span data-ttu-id="abe74-199">
adresse de la banque</span><span class="sxs-lookup"><span data-stu-id="abe74-199">bank address</span></span>
- <span data-ttu-id="abe74-200">
informations du compte</span><span class="sxs-lookup"><span data-stu-id="abe74-200">information account</span></span>
- <span data-ttu-id="abe74-201">
transferts de fonds</span><span class="sxs-lookup"><span data-stu-id="abe74-201">fund transfers</span></span>
- <span data-ttu-id="abe74-202">
frais bancaires</span><span class="sxs-lookup"><span data-stu-id="abe74-202">bank charges</span></span>
- <span data-ttu-id="abe74-203">
informations sur la banque</span><span class="sxs-lookup"><span data-stu-id="abe74-203">bank details</span></span>
- <span data-ttu-id="abe74-204">
informations bancaires</span><span class="sxs-lookup"><span data-stu-id="abe74-204">banking information</span></span>
- <span data-ttu-id="abe74-205">
noms complets</span><span class="sxs-lookup"><span data-stu-id="abe74-205">full names</span></span>
- <span data-ttu-id="abe74-206">

iaea</span><span class="sxs-lookup"><span data-stu-id="abe74-206">iaea</span></span>

   
## <a name="australia-drivers-license-number"></a><span data-ttu-id="abe74-207">Numéro de permis de conduire Australie</span><span class="sxs-lookup"><span data-stu-id="abe74-207">Australia Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-208">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-208">Format</span></span>

<span data-ttu-id="abe74-209">Neuf lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-209">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-210">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-210">Pattern</span></span>

<span data-ttu-id="abe74-211">Neuf lettres et chiffres :</span><span class="sxs-lookup"><span data-stu-id="abe74-211">Nine letters and digits:</span></span> 

- <span data-ttu-id="abe74-212">Deux chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="abe74-212">Two digits or letters (not case sensitive)</span></span> 
- <span data-ttu-id="abe74-213">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-213">Two digits</span></span> 
- <span data-ttu-id="abe74-214">Cinq chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="abe74-214">Five digits or letters (not case sensitive)</span></span>

<span data-ttu-id="abe74-215">OU</span><span class="sxs-lookup"><span data-stu-id="abe74-215">OR</span></span>

- <span data-ttu-id="abe74-216">1 ou 2 lettres facultatives (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="abe74-216">1-2 optional letters (not case sensitive)</span></span> 
- <span data-ttu-id="abe74-217">4 à 9 chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-217">4-9 digits</span></span>

<span data-ttu-id="abe74-218">OU</span><span class="sxs-lookup"><span data-stu-id="abe74-218">OR</span></span>

- <span data-ttu-id="abe74-219">Neuf chiffres ou lettres (ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="abe74-219">Nine digits or letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-220">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-220">Checksum</span></span>

<span data-ttu-id="abe74-221">Non</span><span class="sxs-lookup"><span data-stu-id="abe74-221">No</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-222">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-222">Definition</span></span>

<span data-ttu-id="abe74-223">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-223">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-224">L’expression régulière Regex_australia_drivers_license_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-224">The regular expression Regex_australia_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-225">Un mot clé figurant dans la liste Keyword_australia_drivers_license_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-225">A keyword from Keyword_australia_drivers_license_number is found.</span></span>
- <span data-ttu-id="abe74-226">Aucun mot clé figurant dans la liste Keyword_australia_drivers_license_number_exclusions n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-226">No keyword from Keyword_australia_drivers_license_number_exclusions is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-227">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-227">Keywords</span></span>

#### <a name="keywordaustraliadriverslicensenumber"></a><span data-ttu-id="abe74-228">Keyword_australia_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="abe74-228">Keyword_australia_drivers_license_number</span></span>

- <span data-ttu-id="abe74-229">permis de conduite internationaux</span><span class="sxs-lookup"><span data-stu-id="abe74-229">international driving permits</span></span>
- <span data-ttu-id="abe74-230">
australian automobile association</span><span class="sxs-lookup"><span data-stu-id="abe74-230">australian automobile association</span></span>
- <span data-ttu-id="abe74-231">
sydney nsw</span><span class="sxs-lookup"><span data-stu-id="abe74-231">sydney nsw</span></span>
- <span data-ttu-id="abe74-232">
permis de conduite international</span><span class="sxs-lookup"><span data-stu-id="abe74-232">international driving permit</span></span>
- <span data-ttu-id="abe74-233">DriverLicence</span><span class="sxs-lookup"><span data-stu-id="abe74-233">DriverLicence</span></span>
- <span data-ttu-id="abe74-234">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="abe74-234">DriverLicences</span></span>
- <span data-ttu-id="abe74-235">Lic pilote</span><span class="sxs-lookup"><span data-stu-id="abe74-235">Driver Lic</span></span>
- <span data-ttu-id="abe74-236">Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-236">Driver Licence</span></span>
- <span data-ttu-id="abe74-237">Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-237">Driver Licences</span></span>
- <span data-ttu-id="abe74-238">DriversLic</span><span class="sxs-lookup"><span data-stu-id="abe74-238">DriversLic</span></span>
- <span data-ttu-id="abe74-239">DriversLicence</span><span class="sxs-lookup"><span data-stu-id="abe74-239">DriversLicence</span></span>
- <span data-ttu-id="abe74-240">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="abe74-240">DriversLicences</span></span>
- <span data-ttu-id="abe74-241">Lic pilotes</span><span class="sxs-lookup"><span data-stu-id="abe74-241">Drivers Lic</span></span>
- <span data-ttu-id="abe74-242">Lics pilotes</span><span class="sxs-lookup"><span data-stu-id="abe74-242">Drivers Lics</span></span>
- <span data-ttu-id="abe74-243">Certificat de pilotes</span><span class="sxs-lookup"><span data-stu-id="abe74-243">Drivers Licence</span></span>
- <span data-ttu-id="abe74-244">Certificats de pilotes</span><span class="sxs-lookup"><span data-stu-id="abe74-244">Drivers Licences</span></span>
- <span data-ttu-id="abe74-245">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="abe74-245">Driver'Lic</span></span>
- <span data-ttu-id="abe74-246">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="abe74-246">Driver'Lics</span></span>
- <span data-ttu-id="abe74-247">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="abe74-247">Driver'Licence</span></span>
- <span data-ttu-id="abe74-248">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="abe74-248">Driver'Licences</span></span>
- <span data-ttu-id="abe74-249">Pilote ' Lic</span><span class="sxs-lookup"><span data-stu-id="abe74-249">Driver' Lic</span></span>
- <span data-ttu-id="abe74-250">Pilote ' Lics</span><span class="sxs-lookup"><span data-stu-id="abe74-250">Driver' Lics</span></span>
- <span data-ttu-id="abe74-251">Pilote ' certificat</span><span class="sxs-lookup"><span data-stu-id="abe74-251">Driver' Licence</span></span>
- <span data-ttu-id="abe74-252">Pilote « certificats</span><span class="sxs-lookup"><span data-stu-id="abe74-252">Driver' Licences</span></span>
- <span data-ttu-id="abe74-253">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="abe74-253">Driver'sLic</span></span>
- <span data-ttu-id="abe74-254">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="abe74-254">Driver'sLics</span></span>
- <span data-ttu-id="abe74-255">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="abe74-255">Driver'sLicence</span></span>
- <span data-ttu-id="abe74-256">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="abe74-256">Driver'sLicences</span></span>
- <span data-ttu-id="abe74-257">Lic du pilote</span><span class="sxs-lookup"><span data-stu-id="abe74-257">Driver's Lic</span></span>
- <span data-ttu-id="abe74-258">Lics permis de conduire</span><span class="sxs-lookup"><span data-stu-id="abe74-258">Driver's Lics</span></span>
- <span data-ttu-id="abe74-259">Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-259">Driver's Licence</span></span>
- <span data-ttu-id="abe74-260">Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-260">Driver's Licences</span></span>
- <span data-ttu-id="abe74-261">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="abe74-261">DriverLic#</span></span>
- <span data-ttu-id="abe74-262">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="abe74-262">DriverLics#</span></span>
- <span data-ttu-id="abe74-263">DriverLicence #</span><span class="sxs-lookup"><span data-stu-id="abe74-263">DriverLicence#</span></span>
- <span data-ttu-id="abe74-264">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="abe74-264">DriverLicences#</span></span>
- <span data-ttu-id="abe74-265">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="abe74-265">Driver Lic#</span></span>
- <span data-ttu-id="abe74-266">
#Permis conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-266">Driver Lics#</span></span>
- <span data-ttu-id="abe74-267">Pilote certificat #</span><span class="sxs-lookup"><span data-stu-id="abe74-267">Driver Licence#</span></span>
- <span data-ttu-id="abe74-268">Pilote certificats #</span><span class="sxs-lookup"><span data-stu-id="abe74-268">Driver Licences#</span></span>
- <span data-ttu-id="abe74-269">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="abe74-269">DriversLic#</span></span>
- <span data-ttu-id="abe74-270">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="abe74-270">DriversLics#</span></span>
- <span data-ttu-id="abe74-271">DriversLicence #</span><span class="sxs-lookup"><span data-stu-id="abe74-271">DriversLicence#</span></span>
- <span data-ttu-id="abe74-272">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="abe74-272">DriversLicences#</span></span>
- <span data-ttu-id="abe74-273">Pilotes Lic #</span><span class="sxs-lookup"><span data-stu-id="abe74-273">Drivers Lic#</span></span>
- <span data-ttu-id="abe74-274">Pilotes Lics #</span><span class="sxs-lookup"><span data-stu-id="abe74-274">Drivers Lics#</span></span>
- <span data-ttu-id="abe74-275">Licence pilotes #</span><span class="sxs-lookup"><span data-stu-id="abe74-275">Drivers Licence#</span></span>
- <span data-ttu-id="abe74-276">Certificats pilotes #</span><span class="sxs-lookup"><span data-stu-id="abe74-276">Drivers Licences#</span></span>
- <span data-ttu-id="abe74-277">#Permisconduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-277">Driver'Lic#</span></span>
- <span data-ttu-id="abe74-278">#Permisconduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-278">Driver'Lics#</span></span>
- <span data-ttu-id="abe74-279">#Permisdeconduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-279">Driver'Licence#</span></span>
- <span data-ttu-id="abe74-280">#Permisdeconduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-280">Driver'Licences#</span></span>
- <span data-ttu-id="abe74-281">#Permis conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-281">Driver' Lic#</span></span>
- <span data-ttu-id="abe74-282">#Permis conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-282">Driver' Lics#</span></span>
- <span data-ttu-id="abe74-283">Pilote ' certificat #</span><span class="sxs-lookup"><span data-stu-id="abe74-283">Driver' Licence#</span></span>
- <span data-ttu-id="abe74-284">Pilote « certificats #</span><span class="sxs-lookup"><span data-stu-id="abe74-284">Driver' Licences#</span></span>
- <span data-ttu-id="abe74-285">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="abe74-285">Driver'sLic#</span></span>
- <span data-ttu-id="abe74-286">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="abe74-286">Driver'sLics#</span></span>
- <span data-ttu-id="abe74-287">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="abe74-287">Driver'sLicence#</span></span>
- <span data-ttu-id="abe74-288">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="abe74-288">Driver'sLicences#</span></span>
- <span data-ttu-id="abe74-289">#Permisconduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-289">Driver's Lic#</span></span>
- <span data-ttu-id="abe74-290">#Permisconduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-290">Driver's Lics#</span></span>
- <span data-ttu-id="abe74-291">Certificat de # permis de conduire</span><span class="sxs-lookup"><span data-stu-id="abe74-291">Driver's Licence#</span></span>
- <span data-ttu-id="abe74-292">Certificats de # permis de conduire</span><span class="sxs-lookup"><span data-stu-id="abe74-292">Driver's Licences#</span></span> 

#### <a name="keywordaustraliadriverslicensenumberexclusions"></a><span data-ttu-id="abe74-293">Keyword_australia_drivers_license_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="abe74-293">Keyword_australia_drivers_license_number_exclusions</span></span>

- <span data-ttu-id="abe74-294">aaa</span><span class="sxs-lookup"><span data-stu-id="abe74-294">aaa</span></span>
- <span data-ttu-id="abe74-295">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="abe74-295">DriverLicense</span></span>
- <span data-ttu-id="abe74-296">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="abe74-296">DriverLicenses</span></span>
- <span data-ttu-id="abe74-297">Conduire</span><span class="sxs-lookup"><span data-stu-id="abe74-297">Driver License</span></span>
- <span data-ttu-id="abe74-298">Licences de pilote</span><span class="sxs-lookup"><span data-stu-id="abe74-298">Driver Licenses</span></span>
- <span data-ttu-id="abe74-299">Conduire</span><span class="sxs-lookup"><span data-stu-id="abe74-299">DriversLicense</span></span>
- <span data-ttu-id="abe74-300">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="abe74-300">DriversLicenses</span></span>
- <span data-ttu-id="abe74-301">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="abe74-301">Drivers License</span></span>
- <span data-ttu-id="abe74-302">Licences de pilotes</span><span class="sxs-lookup"><span data-stu-id="abe74-302">Drivers Licenses</span></span>
- <span data-ttu-id="abe74-303">Driver'License</span><span class="sxs-lookup"><span data-stu-id="abe74-303">Driver'License</span></span>
- <span data-ttu-id="abe74-304">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="abe74-304">Driver'Licenses</span></span>
- <span data-ttu-id="abe74-305">Pilote ' licence</span><span class="sxs-lookup"><span data-stu-id="abe74-305">Driver' License</span></span>
- <span data-ttu-id="abe74-306">Pilote ' licences</span><span class="sxs-lookup"><span data-stu-id="abe74-306">Driver' Licenses</span></span>
- <span data-ttu-id="abe74-307">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="abe74-307">Driver'sLicense</span></span>
- <span data-ttu-id="abe74-308">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="abe74-308">Driver'sLicenses</span></span>
- <span data-ttu-id="abe74-309">Conduire permis de</span><span class="sxs-lookup"><span data-stu-id="abe74-309">Driver's License</span></span>
- <span data-ttu-id="abe74-310">Conduire permis de</span><span class="sxs-lookup"><span data-stu-id="abe74-310">Driver's Licenses</span></span>
- <span data-ttu-id="abe74-311">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="abe74-311">DriverLicense#</span></span>
- <span data-ttu-id="abe74-312">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="abe74-312">DriverLicenses#</span></span>
- <span data-ttu-id="abe74-313">Pilote licence #</span><span class="sxs-lookup"><span data-stu-id="abe74-313">Driver License#</span></span>
- <span data-ttu-id="abe74-314">Licences de pilote #</span><span class="sxs-lookup"><span data-stu-id="abe74-314">Driver Licenses#</span></span>
- <span data-ttu-id="abe74-315">Conduire #</span><span class="sxs-lookup"><span data-stu-id="abe74-315">DriversLicense#</span></span>
- <span data-ttu-id="abe74-316">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="abe74-316">DriversLicenses#</span></span>
- <span data-ttu-id="abe74-317">Licence pilotes #</span><span class="sxs-lookup"><span data-stu-id="abe74-317">Drivers License#</span></span>
- <span data-ttu-id="abe74-318">Licences pilotes #</span><span class="sxs-lookup"><span data-stu-id="abe74-318">Drivers Licenses#</span></span>
- <span data-ttu-id="abe74-319">#Permisdeconduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-319">Driver'License#</span></span>
- <span data-ttu-id="abe74-320">#Permisdeconduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-320">Driver'Licenses#</span></span>
- <span data-ttu-id="abe74-321">#Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-321">Driver' License#</span></span>
- <span data-ttu-id="abe74-322">#Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-322">Driver' Licenses#</span></span>
- <span data-ttu-id="abe74-323">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="abe74-323">Driver'sLicense#</span></span>
- <span data-ttu-id="abe74-324">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="abe74-324">Driver'sLicenses#</span></span>
- <span data-ttu-id="abe74-325">#Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-325">Driver's License#</span></span>
- <span data-ttu-id="abe74-326">

#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="abe74-326">Driver's Licenses#</span></span>
   
## <a name="australia-medical-account-number"></a><span data-ttu-id="abe74-327">Numéro de dossier médical Australie</span><span class="sxs-lookup"><span data-stu-id="abe74-327">Australia Medical Account Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-328">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-328">Format</span></span>

<span data-ttu-id="abe74-329">10 à 11 chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-329">10-11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-330">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-330">Pattern</span></span>

<span data-ttu-id="abe74-331">10 à 11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="abe74-331">10-11 digits:</span></span>
- <span data-ttu-id="abe74-332">Le premier chiffre est compris entre 2 et 6</span><span class="sxs-lookup"><span data-stu-id="abe74-332">First digit is in the range 2-6</span></span>
- <span data-ttu-id="abe74-333">Le neuvième chiffre est un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-333">Ninth digit is a check digit</span></span>
- <span data-ttu-id="abe74-334">Le dixième chiffre est le chiffre d’émission</span><span class="sxs-lookup"><span data-stu-id="abe74-334">Tenth digit is the issue digit</span></span>
- <span data-ttu-id="abe74-335">Le onzième chiffre (facultatif) est le numéro individuel</span><span class="sxs-lookup"><span data-stu-id="abe74-335">Eleventh digit (optional) is the individual number</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-336">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-336">Checksum</span></span>

<span data-ttu-id="abe74-337">Oui</span><span class="sxs-lookup"><span data-stu-id="abe74-337">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-338">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-338">Definition</span></span>

<span data-ttu-id="abe74-339">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 95 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-339">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-340">La fonction Func_australian_medical_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-340">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-341">Un mot clé figurant dans la liste Keyword_Australia_Medical_Account_Number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-341">A keyword from Keyword_Australia_Medical_Account_Number is found.</span></span>
- <span data-ttu-id="abe74-342">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-342">The checksum passes.</span></span>

<span data-ttu-id="abe74-343">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-343">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-344">La fonction Func_australian_medical_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-344">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-345">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-345">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-346">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-346">Keywords</span></span>

#### <a name="keywordaustraliamedicalaccountnumber"></a><span data-ttu-id="abe74-347">Keyword_Australia_Medical_Account_Number</span><span class="sxs-lookup"><span data-stu-id="abe74-347">Keyword_Australia_Medical_Account_Number</span></span>

- <span data-ttu-id="abe74-348">informations sur le compte bancaire</span><span class="sxs-lookup"><span data-stu-id="abe74-348">bank account details</span></span>
- <span data-ttu-id="abe74-349">
remboursements d’assurance maladie</span><span class="sxs-lookup"><span data-stu-id="abe74-349">medicare payments</span></span>
- <span data-ttu-id="abe74-350">
compte de prêts immobiliers</span><span class="sxs-lookup"><span data-stu-id="abe74-350">mortgage account</span></span>
- <span data-ttu-id="abe74-351">
paiements bancaires</span><span class="sxs-lookup"><span data-stu-id="abe74-351">bank payments</span></span>
- <span data-ttu-id="abe74-352">
direction de l’information</span><span class="sxs-lookup"><span data-stu-id="abe74-352">information branch</span></span>
- <span data-ttu-id="abe74-353">
prêt sur carte de crédit</span><span class="sxs-lookup"><span data-stu-id="abe74-353">credit card loan</span></span>
- <span data-ttu-id="abe74-354">
département des services sociaux</span><span class="sxs-lookup"><span data-stu-id="abe74-354">department of human services</span></span>
- <span data-ttu-id="abe74-355">service local</span><span class="sxs-lookup"><span data-stu-id="abe74-355">local service</span></span>
- <span data-ttu-id="abe74-356">

medicare</span><span class="sxs-lookup"><span data-stu-id="abe74-356">medicare</span></span>

   
## <a name="australia-passport-number"></a><span data-ttu-id="abe74-357">Numéro de passeport Australie</span><span class="sxs-lookup"><span data-stu-id="abe74-357">Australia Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-358">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-358">Format</span></span>

<span data-ttu-id="abe74-359">Une lettre suivie de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-359">A letter followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-360">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-360">Pattern</span></span>

<span data-ttu-id="abe74-361">Une lettre (ne respectant pas la casse) suivie de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-361">A letter (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-362">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-362">Checksum</span></span>

<span data-ttu-id="abe74-363">Non</span><span class="sxs-lookup"><span data-stu-id="abe74-363">No</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-364">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-364">Definition</span></span>

<span data-ttu-id="abe74-365">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-365">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-366">L’expression régulière Regex_australia_passport_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-366">The regular expression Regex_australia_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-367">Un mot clé à partir de Keyword_passport ou Keyword_australia_passport_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-367">A keyword from Keyword_passport or Keyword_australia_passport_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-368">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-368">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="abe74-369">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="abe74-369">Keyword_passport</span></span>

- <span data-ttu-id="abe74-370">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="abe74-370">Passport Number</span></span>
- <span data-ttu-id="abe74-371">
N° de passeport</span><span class="sxs-lookup"><span data-stu-id="abe74-371">Passport No</span></span>
- <span data-ttu-id="abe74-372"># Passeport
</span><span class="sxs-lookup"><span data-stu-id="abe74-372">Passport #</span></span>
- <span data-ttu-id="abe74-373">#Passeport
</span><span class="sxs-lookup"><span data-stu-id="abe74-373">Passport#</span></span>
- <span data-ttu-id="abe74-374">IDPassport</span><span class="sxs-lookup"><span data-stu-id="abe74-374">PassportID</span></span>
- <span data-ttu-id="abe74-375">n° passeport
</span><span class="sxs-lookup"><span data-stu-id="abe74-375">Passportno</span></span>
- <span data-ttu-id="abe74-376">numéropasseport
</span><span class="sxs-lookup"><span data-stu-id="abe74-376">passportnumber</span></span>
- <span data-ttu-id="abe74-377">パスポート</span><span class="sxs-lookup"><span data-stu-id="abe74-377">パスポート</span></span>
- <span data-ttu-id="abe74-378">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="abe74-378">パスポート番号</span></span>
- <span data-ttu-id="abe74-379">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="abe74-379">パスポートのNum</span></span>
- <span data-ttu-id="abe74-380">
パスポート＃
</span><span class="sxs-lookup"><span data-stu-id="abe74-380">パスポート ＃</span></span> 
- <span data-ttu-id="abe74-381">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="abe74-381">Numéro de passeport</span></span>
- <span data-ttu-id="abe74-382">
Passeport n°</span><span class="sxs-lookup"><span data-stu-id="abe74-382">Passeport n °</span></span>
- <span data-ttu-id="abe74-383">Passeport numéro
</span><span class="sxs-lookup"><span data-stu-id="abe74-383">Passeport Non</span></span>
- <span data-ttu-id="abe74-384"># Passeport
</span><span class="sxs-lookup"><span data-stu-id="abe74-384">Passeport #</span></span>
- <span data-ttu-id="abe74-385">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="abe74-385">Passeport#</span></span>
- <span data-ttu-id="abe74-386">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="abe74-386">PasseportNon</span></span>
- <span data-ttu-id="abe74-387">Passeportn °
</span><span class="sxs-lookup"><span data-stu-id="abe74-387">Passeportn °</span></span>

#### <a name="keywordaustraliapassportnumber"></a><span data-ttu-id="abe74-388">Keyword_australia_passport_number</span><span class="sxs-lookup"><span data-stu-id="abe74-388">Keyword_australia_passport_number</span></span>

- <span data-ttu-id="abe74-389">passeport</span><span class="sxs-lookup"><span data-stu-id="abe74-389">passport</span></span>
- <span data-ttu-id="abe74-390">
informations sur le passeport</span><span class="sxs-lookup"><span data-stu-id="abe74-390">passport details</span></span>
- <span data-ttu-id="abe74-391">
immigration et citoyenneté</span><span class="sxs-lookup"><span data-stu-id="abe74-391">immigration and citizenship</span></span>
- <span data-ttu-id="abe74-392">
Australie</span><span class="sxs-lookup"><span data-stu-id="abe74-392">commonwealth of australia</span></span>
- <span data-ttu-id="abe74-393">
service de l’immigration</span><span class="sxs-lookup"><span data-stu-id="abe74-393">department of immigration</span></span>
- <span data-ttu-id="abe74-394">
adresse de résidence</span><span class="sxs-lookup"><span data-stu-id="abe74-394">residential address</span></span>
- <span data-ttu-id="abe74-395">
service de l’immigration et de la citoyenneté</span><span class="sxs-lookup"><span data-stu-id="abe74-395">department of immigration and citizenship</span></span>
- <span data-ttu-id="abe74-396">visa
</span><span class="sxs-lookup"><span data-stu-id="abe74-396">visa</span></span>
- <span data-ttu-id="abe74-397">
Carte nationale d’identité</span><span class="sxs-lookup"><span data-stu-id="abe74-397">national identity card</span></span>
- <span data-ttu-id="abe74-398">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="abe74-398">passport number</span></span>
- <span data-ttu-id="abe74-399">
document de voyage</span><span class="sxs-lookup"><span data-stu-id="abe74-399">travel document</span></span>
- <span data-ttu-id="abe74-400">

autorité émettrice</span><span class="sxs-lookup"><span data-stu-id="abe74-400">issuing authority</span></span>
   
## <a name="australia-tax-file-number"></a><span data-ttu-id="abe74-401">Numéro de dossier fiscal Australie</span><span class="sxs-lookup"><span data-stu-id="abe74-401">Australia Tax File Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-402">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-402">Format</span></span>

<span data-ttu-id="abe74-403">8 ou 9 chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-403">8-9 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-404">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-404">Pattern</span></span>

<span data-ttu-id="abe74-405">8 à 9 chiffres généralement entrecoupés d’espaces comme suit :</span><span class="sxs-lookup"><span data-stu-id="abe74-405">8-9 digits typically presented with spaces as follows:</span></span>
- <span data-ttu-id="abe74-406">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-406">Three digits</span></span> 
- <span data-ttu-id="abe74-407">Un espace facultatif</span><span class="sxs-lookup"><span data-stu-id="abe74-407">An optional space</span></span> 
- <span data-ttu-id="abe74-408">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-408">Three digits</span></span> 
- <span data-ttu-id="abe74-409">Un espace facultatif</span><span class="sxs-lookup"><span data-stu-id="abe74-409">An optional space</span></span> 
- <span data-ttu-id="abe74-410">2 à 3 chiffres où le dernier chiffre est un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-410">2-3 digits where the last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-411">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-411">Checksum</span></span>

<span data-ttu-id="abe74-412">Oui</span><span class="sxs-lookup"><span data-stu-id="abe74-412">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-413">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-413">Definition</span></span>

<span data-ttu-id="abe74-414">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-414">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-415">La fonction Func_australian_tax_file_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-415">The function Func_australian_tax_file_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-416">Aucun mot clé figurant dans la liste Keyword_Australia_Tax_File_Number ou Keyword_number_exclusions n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-416">No keyword from Keyword_Australia_Tax_File_Number or Keyword_number_exclusions is found.</span></span>
- <span data-ttu-id="abe74-417">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-417">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-418">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-418">Keywords</span></span>

#### <a name="keywordaustraliataxfilenumber"></a><span data-ttu-id="abe74-419">Keyword_Australia_Tax_File_Number</span><span class="sxs-lookup"><span data-stu-id="abe74-419">Keyword_Australia_Tax_File_Number</span></span>

- <span data-ttu-id="abe74-420">numéro d’entreprise australien</span><span class="sxs-lookup"><span data-stu-id="abe74-420">australian business number</span></span>
- <span data-ttu-id="abe74-421">
taux d’imposition marginale</span><span class="sxs-lookup"><span data-stu-id="abe74-421">marginal tax rate</span></span>
- <span data-ttu-id="abe74-422">
prélèvement d’assurance maladie</span><span class="sxs-lookup"><span data-stu-id="abe74-422">medicare levy</span></span>
- <span data-ttu-id="abe74-423">
numéro de portefeuille</span><span class="sxs-lookup"><span data-stu-id="abe74-423">portfolio number</span></span>
- <span data-ttu-id="abe74-424">
service des vétérans</span><span class="sxs-lookup"><span data-stu-id="abe74-424">service veterans</span></span>
- <span data-ttu-id="abe74-425">
retenue à la source</span><span class="sxs-lookup"><span data-stu-id="abe74-425">withholding tax</span></span>
- <span data-ttu-id="abe74-426">
déclaration d’impôts individuels</span><span class="sxs-lookup"><span data-stu-id="abe74-426">individual tax return</span></span>
- <span data-ttu-id="abe74-427">

numéro de dossier fiscal</span><span class="sxs-lookup"><span data-stu-id="abe74-427">tax file number</span></span>

#### <a name="keywordnumberexclusions"></a><span data-ttu-id="abe74-428">Keyword_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="abe74-428">Keyword_number_exclusions</span></span>

- <span data-ttu-id="abe74-429">00000000</span><span class="sxs-lookup"><span data-stu-id="abe74-429">00000000</span></span>
- <span data-ttu-id="abe74-430">11111111</span><span class="sxs-lookup"><span data-stu-id="abe74-430">11111111</span></span>
- <span data-ttu-id="abe74-431">22222222</span><span class="sxs-lookup"><span data-stu-id="abe74-431">22222222</span></span>
- <span data-ttu-id="abe74-432">33333333</span><span class="sxs-lookup"><span data-stu-id="abe74-432">33333333</span></span>
- <span data-ttu-id="abe74-433">44444444</span><span class="sxs-lookup"><span data-stu-id="abe74-433">44444444</span></span>
- <span data-ttu-id="abe74-434">55555555</span><span class="sxs-lookup"><span data-stu-id="abe74-434">55555555</span></span>
- <span data-ttu-id="abe74-435">66666666</span><span class="sxs-lookup"><span data-stu-id="abe74-435">66666666</span></span>
- <span data-ttu-id="abe74-436">77777777</span><span class="sxs-lookup"><span data-stu-id="abe74-436">77777777</span></span>
- <span data-ttu-id="abe74-437">88888888</span><span class="sxs-lookup"><span data-stu-id="abe74-437">88888888</span></span>
- <span data-ttu-id="abe74-438">99999999</span><span class="sxs-lookup"><span data-stu-id="abe74-438">99999999</span></span>
- <span data-ttu-id="abe74-439">000000000</span><span class="sxs-lookup"><span data-stu-id="abe74-439">000000000</span></span>
- <span data-ttu-id="abe74-440">111111111</span><span class="sxs-lookup"><span data-stu-id="abe74-440">111111111</span></span>
- <span data-ttu-id="abe74-441">222222222</span><span class="sxs-lookup"><span data-stu-id="abe74-441">222222222</span></span>
- <span data-ttu-id="abe74-442">333333333</span><span class="sxs-lookup"><span data-stu-id="abe74-442">333333333</span></span>
- <span data-ttu-id="abe74-443">444444444</span><span class="sxs-lookup"><span data-stu-id="abe74-443">444444444</span></span>
- <span data-ttu-id="abe74-444">555555555</span><span class="sxs-lookup"><span data-stu-id="abe74-444">555555555</span></span>
- <span data-ttu-id="abe74-445">666666666</span><span class="sxs-lookup"><span data-stu-id="abe74-445">666666666</span></span>
- <span data-ttu-id="abe74-446">777777777</span><span class="sxs-lookup"><span data-stu-id="abe74-446">777777777</span></span>
- <span data-ttu-id="abe74-447">888888888</span><span class="sxs-lookup"><span data-stu-id="abe74-447">888888888</span></span>
- <span data-ttu-id="abe74-448">999999999</span><span class="sxs-lookup"><span data-stu-id="abe74-448">999999999</span></span>
- <span data-ttu-id="abe74-449">0000000000</span><span class="sxs-lookup"><span data-stu-id="abe74-449">0000000000</span></span>
- <span data-ttu-id="abe74-450">1111111111</span><span class="sxs-lookup"><span data-stu-id="abe74-450">1111111111</span></span>
- <span data-ttu-id="abe74-451">2222222222</span><span class="sxs-lookup"><span data-stu-id="abe74-451">2222222222</span></span>
- <span data-ttu-id="abe74-452">3333333333</span><span class="sxs-lookup"><span data-stu-id="abe74-452">3333333333</span></span>
- <span data-ttu-id="abe74-453">4444444444</span><span class="sxs-lookup"><span data-stu-id="abe74-453">4444444444</span></span>
- <span data-ttu-id="abe74-454">5555555555</span><span class="sxs-lookup"><span data-stu-id="abe74-454">5555555555</span></span>
- <span data-ttu-id="abe74-455">6666666666</span><span class="sxs-lookup"><span data-stu-id="abe74-455">6666666666</span></span>
- <span data-ttu-id="abe74-456">7777777777</span><span class="sxs-lookup"><span data-stu-id="abe74-456">7777777777</span></span>
- <span data-ttu-id="abe74-457">8888888888</span><span class="sxs-lookup"><span data-stu-id="abe74-457">8888888888</span></span>
- <span data-ttu-id="abe74-458">9999999999</span><span class="sxs-lookup"><span data-stu-id="abe74-458">9999999999</span></span>
   
## <a name="belgium-national-number"></a><span data-ttu-id="abe74-459">Numéro national Belgique</span><span class="sxs-lookup"><span data-stu-id="abe74-459">Belgium National Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-460">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-460">Format</span></span>

<span data-ttu-id="abe74-461">11 chiffres plus des délimiteurs</span><span class="sxs-lookup"><span data-stu-id="abe74-461">11 digits plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-462">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-462">Pattern</span></span>

<span data-ttu-id="abe74-463">11 chiffres plus des délimiteurs :</span><span class="sxs-lookup"><span data-stu-id="abe74-463">11 digits plus delimiters:</span></span>
- <span data-ttu-id="abe74-464">Six chiffres et deux points au format AA.MM.JJ pour la date de naissance </span><span class="sxs-lookup"><span data-stu-id="abe74-464">Six digits and two periods in the format YY.MM.DD for date of birth</span></span> 
- <span data-ttu-id="abe74-465">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="abe74-465">A hyphen</span></span> 
- <span data-ttu-id="abe74-466">Trois chiffres séquentiels (impairs pour les hommes, pairs pour les femmes) </span><span class="sxs-lookup"><span data-stu-id="abe74-466">Three sequential digits (odd for males, even for females)</span></span> 
- <span data-ttu-id="abe74-467">Un point </span><span class="sxs-lookup"><span data-stu-id="abe74-467">A period</span></span> 
- <span data-ttu-id="abe74-468">Deux chiffres de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-468">Two digits that are a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-469">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-469">Checksum</span></span>

<span data-ttu-id="abe74-470">Oui</span><span class="sxs-lookup"><span data-stu-id="abe74-470">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-471">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-471">Definition</span></span>

<span data-ttu-id="abe74-472">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-472">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-473">La fonction Func_belgium_national_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-473">The function Func_belgium_national_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-474">Un mot clé figurant dans la liste Keyword_belgium_national_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-474">A keyword from Keyword_belgium_national_number is found.</span></span>
- <span data-ttu-id="abe74-475">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-475">The checksum passes.</span></span>

```
<!-- Belgium National Number -->
  <Entity id="fb969c9e-0fd1-4b18-8091-a2123c5e6a54" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_belgium_national_number"/>
     <Match idRef="Keyword_belgium_national_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe74-476">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-476">Keywords</span></span>

#### <a name="keywordbelgiumnationalnumber"></a><span data-ttu-id="abe74-477">Keyword_belgium_national_number</span><span class="sxs-lookup"><span data-stu-id="abe74-477">Keyword_belgium_national_number</span></span>

- <span data-ttu-id="abe74-478">Identité</span><span class="sxs-lookup"><span data-stu-id="abe74-478">Identity</span></span>
- <span data-ttu-id="abe74-479">Registration</span><span class="sxs-lookup"><span data-stu-id="abe74-479">Registration</span></span>
- <span data-ttu-id="abe74-480">Identification</span><span class="sxs-lookup"><span data-stu-id="abe74-480">Identification</span></span> 
- <span data-ttu-id="abe74-481">ID</span><span class="sxs-lookup"><span data-stu-id="abe74-481">ID</span></span> 
- <span data-ttu-id="abe74-482">Identiteitskaart</span><span class="sxs-lookup"><span data-stu-id="abe74-482">Identiteitskaart</span></span>
- <span data-ttu-id="abe74-483">Registratie nummer 
</span><span class="sxs-lookup"><span data-stu-id="abe74-483">Registratie nummer</span></span> 
- <span data-ttu-id="abe74-484">Identificatie nummer
</span><span class="sxs-lookup"><span data-stu-id="abe74-484">Identificatie nummer</span></span> 
- <span data-ttu-id="abe74-485">Identiteit</span><span class="sxs-lookup"><span data-stu-id="abe74-485">Identiteit</span></span>
- <span data-ttu-id="abe74-486">Registratie</span><span class="sxs-lookup"><span data-stu-id="abe74-486">Registratie</span></span>
- <span data-ttu-id="abe74-487">Identificatie

</span><span class="sxs-lookup"><span data-stu-id="abe74-487">Identificatie</span></span> 
- <span data-ttu-id="abe74-488">Carte d’identité
</span><span class="sxs-lookup"><span data-stu-id="abe74-488">Carte d’identité</span></span> 
- <span data-ttu-id="abe74-489">numéro d’immatriculation</span><span class="sxs-lookup"><span data-stu-id="abe74-489">numéro d'immatriculation</span></span>
- <span data-ttu-id="abe74-490">numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="abe74-490">numéro d'identification</span></span>
- <span data-ttu-id="abe74-491">
identité
</span><span class="sxs-lookup"><span data-stu-id="abe74-491">identité</span></span> 
- <span data-ttu-id="abe74-492">inscription
</span><span class="sxs-lookup"><span data-stu-id="abe74-492">inscription</span></span> 
- <span data-ttu-id="abe74-493">Identifikation</span><span class="sxs-lookup"><span data-stu-id="abe74-493">Identifikation</span></span>
- <span data-ttu-id="abe74-494">Identifizierung</span><span class="sxs-lookup"><span data-stu-id="abe74-494">Identifizierung</span></span>
- <span data-ttu-id="abe74-495">Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="abe74-495">Identifikationsnummer</span></span>
- <span data-ttu-id="abe74-496">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="abe74-496">Personalausweis</span></span>
- <span data-ttu-id="abe74-497">Registrierung</span><span class="sxs-lookup"><span data-stu-id="abe74-497">Registrierung</span></span>
- <span data-ttu-id="abe74-498">Registrationsnummer</span><span class="sxs-lookup"><span data-stu-id="abe74-498">Registrationsnummer</span></span>

   
## <a name="brazil-cpf-number"></a><span data-ttu-id="abe74-499">Numéro CPF Brésil</span><span class="sxs-lookup"><span data-stu-id="abe74-499">Brazil CPF Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-500">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-500">Format</span></span>

<span data-ttu-id="abe74-501">11 chiffres qui incluent un chiffre de contrôle et peuvent ou non être mis en forme </span><span class="sxs-lookup"><span data-stu-id="abe74-501">11 digits that include a check digit and can be formatted or unformatted</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-502">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-502">Pattern</span></span>

<span data-ttu-id="abe74-503">Mis en forme :</span><span class="sxs-lookup"><span data-stu-id="abe74-503">Formatted:</span></span>
- <span data-ttu-id="abe74-504">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-504">Three digits</span></span> 
- <span data-ttu-id="abe74-505">Un point </span><span class="sxs-lookup"><span data-stu-id="abe74-505">A period</span></span> 
- <span data-ttu-id="abe74-506">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-506">Three digits</span></span> 
- <span data-ttu-id="abe74-507">Un point </span><span class="sxs-lookup"><span data-stu-id="abe74-507">A period</span></span> 
- <span data-ttu-id="abe74-508">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-508">Three digits</span></span> 
- <span data-ttu-id="abe74-509">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="abe74-509">A hyphen</span></span> 
- <span data-ttu-id="abe74-510">Deux chiffres de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-510">Two digits which are check digits</span></span>

<span data-ttu-id="abe74-511">Non mis en forme :</span><span class="sxs-lookup"><span data-stu-id="abe74-511">Unformatted:</span></span>
- <span data-ttu-id="abe74-512">11 chiffres où les deux derniers sont des chiffres de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-512">11 digits where the last two digits are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-513">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-513">Checksum</span></span>

<span data-ttu-id="abe74-514">Oui</span><span class="sxs-lookup"><span data-stu-id="abe74-514">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-515">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-515">Definition</span></span>

<span data-ttu-id="abe74-516">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-516">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-517">La fonction Func_brazil_cpf trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-517">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-518">Un mot clé figurant dans la liste Keyword_brazil_cpf est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-518">A keyword from Keyword_brazil_cpf is found.</span></span>
- <span data-ttu-id="abe74-519">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-519">The checksum passes.</span></span>

<span data-ttu-id="abe74-520">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-520">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-521">La fonction Func_brazil_cpf trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-521">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-522">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-522">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-523">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-523">Keywords</span></span>

#### <a name="keywordbrazilcpf"></a><span data-ttu-id="abe74-524">Keyword_brazil_cpf</span><span class="sxs-lookup"><span data-stu-id="abe74-524">Keyword_brazil_cpf</span></span>

- <span data-ttu-id="abe74-525">CPF</span><span class="sxs-lookup"><span data-stu-id="abe74-525">CPF</span></span>
- <span data-ttu-id="abe74-526">Identification</span><span class="sxs-lookup"><span data-stu-id="abe74-526">Identification</span></span>
- <span data-ttu-id="abe74-527">Registration</span><span class="sxs-lookup"><span data-stu-id="abe74-527">Registration</span></span>
- <span data-ttu-id="abe74-528">Revenue</span><span class="sxs-lookup"><span data-stu-id="abe74-528">Revenue</span></span>
- <span data-ttu-id="abe74-529">Cadastro de Pessoas Físicas
</span><span class="sxs-lookup"><span data-stu-id="abe74-529">Cadastro de Pessoas Físicas</span></span> 
- <span data-ttu-id="abe74-530">Imposto
</span><span class="sxs-lookup"><span data-stu-id="abe74-530">Imposto</span></span> 
- <span data-ttu-id="abe74-531">Identificação
</span><span class="sxs-lookup"><span data-stu-id="abe74-531">Identificação</span></span> 
- <span data-ttu-id="abe74-532">Inscrição
</span><span class="sxs-lookup"><span data-stu-id="abe74-532">Inscrição</span></span> 
- <span data-ttu-id="abe74-533">Receita

</span><span class="sxs-lookup"><span data-stu-id="abe74-533">Receita</span></span> 
   
## <a name="brazil-legal-entity-number-cnpj"></a><span data-ttu-id="abe74-534">Numéro d’entité juridique (CNPJ) Brésil</span><span class="sxs-lookup"><span data-stu-id="abe74-534">Brazil Legal Entity Number (CNPJ)</span></span>

### <a name="format"></a><span data-ttu-id="abe74-535">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-535">Format</span></span>

<span data-ttu-id="abe74-536">14 chiffres qui incluent un numéro d’enregistrement, un numéro de succursale et des chiffres de contrôle, avec des délimiteurs en plus</span><span class="sxs-lookup"><span data-stu-id="abe74-536">14 digits that include a registration number, branch number, and check digits, plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-537">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-537">Pattern</span></span>
<span data-ttu-id="abe74-538">14 chiffres plus des délimiteurs :</span><span class="sxs-lookup"><span data-stu-id="abe74-538">14 digits, plus delimiters:</span></span>
- <span data-ttu-id="abe74-539">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-539">Two digits</span></span> 
- <span data-ttu-id="abe74-540">Un point </span><span class="sxs-lookup"><span data-stu-id="abe74-540">A period</span></span> 
- <span data-ttu-id="abe74-541">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-541">Three digits</span></span> 
- <span data-ttu-id="abe74-542">Un point </span><span class="sxs-lookup"><span data-stu-id="abe74-542">A period</span></span> 
- <span data-ttu-id="abe74-543">Trois chiffres (ces huit premiers chiffres composent le numéro d’enregistrement) </span><span class="sxs-lookup"><span data-stu-id="abe74-543">Three digits (these first eight digits are the registration number)</span></span> 
- <span data-ttu-id="abe74-544">Une barre oblique </span><span class="sxs-lookup"><span data-stu-id="abe74-544">A forward slash</span></span> 
- <span data-ttu-id="abe74-545">Le numéro de succursale à quatre chiffres </span><span class="sxs-lookup"><span data-stu-id="abe74-545">Four-digit branch number</span></span> 
- <span data-ttu-id="abe74-546">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="abe74-546">A hyphen</span></span> 
- <span data-ttu-id="abe74-547">Deux chiffres de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-547">Two digits which are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-548">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-548">Checksum</span></span>

<span data-ttu-id="abe74-549">Oui</span><span class="sxs-lookup"><span data-stu-id="abe74-549">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-550">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-550">Definition</span></span>

<span data-ttu-id="abe74-551">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-551">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-552">La fonction Func_brazil_cnpj trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-552">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-553">Un mot clé figurant dans la liste Keyword_brazil_cnpj est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-553">A keyword from Keyword_brazil_cnpj is found.</span></span>
- <span data-ttu-id="abe74-554">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-554">The checksum passes.</span></span>

<span data-ttu-id="abe74-555">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-555">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-556">La fonction Func_brazil_cnpj trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-556">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-557">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-557">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-558">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-558">Keywords</span></span>

#### <a name="keywordbrazilcnpj"></a><span data-ttu-id="abe74-559">Keyword_brazil_cnpj</span><span class="sxs-lookup"><span data-stu-id="abe74-559">Keyword_brazil_cnpj</span></span>

- <span data-ttu-id="abe74-560">CNPJ
</span><span class="sxs-lookup"><span data-stu-id="abe74-560">CNPJ</span></span> 
- <span data-ttu-id="abe74-561">CNPJ/MF</span><span class="sxs-lookup"><span data-stu-id="abe74-561">CNPJ/MF</span></span> 
- <span data-ttu-id="abe74-562">CNPJ-MF
</span><span class="sxs-lookup"><span data-stu-id="abe74-562">CNPJ-MF</span></span> 
- <span data-ttu-id="abe74-563">National Registry of Legal Entities
</span><span class="sxs-lookup"><span data-stu-id="abe74-563">National Registry of Legal Entities</span></span> 
- <span data-ttu-id="abe74-564">Taxpayers Registry
</span><span class="sxs-lookup"><span data-stu-id="abe74-564">Taxpayers Registry</span></span> 
- <span data-ttu-id="abe74-565">Legal entity
</span><span class="sxs-lookup"><span data-stu-id="abe74-565">Legal entity</span></span> 
- <span data-ttu-id="abe74-566">Legal entities
</span><span class="sxs-lookup"><span data-stu-id="abe74-566">Legal entities</span></span> 
- <span data-ttu-id="abe74-567">Registration Status
</span><span class="sxs-lookup"><span data-stu-id="abe74-567">Registration Status</span></span> 
- <span data-ttu-id="abe74-568">Business
</span><span class="sxs-lookup"><span data-stu-id="abe74-568">Business</span></span> 
- <span data-ttu-id="abe74-569">Company</span><span class="sxs-lookup"><span data-stu-id="abe74-569">Company</span></span>
- <span data-ttu-id="abe74-570">CNPJ
</span><span class="sxs-lookup"><span data-stu-id="abe74-570">CNPJ</span></span> 
- <span data-ttu-id="abe74-571">Cadastro Nacional da Pessoa Jurídica
</span><span class="sxs-lookup"><span data-stu-id="abe74-571">Cadastro Nacional da Pessoa Jurídica</span></span> 
- <span data-ttu-id="abe74-572">Cadastro Geral de Contribuintes
</span><span class="sxs-lookup"><span data-stu-id="abe74-572">Cadastro Geral de Contribuintes</span></span> 
- <span data-ttu-id="abe74-573">CGC
</span><span class="sxs-lookup"><span data-stu-id="abe74-573">CGC</span></span> 
- <span data-ttu-id="abe74-574">Pessoa jurídica
</span><span class="sxs-lookup"><span data-stu-id="abe74-574">Pessoa jurídica</span></span> 
- <span data-ttu-id="abe74-575">Pessoas jurídicas
</span><span class="sxs-lookup"><span data-stu-id="abe74-575">Pessoas jurídicas</span></span> 
- <span data-ttu-id="abe74-576">Situação cadastral
</span><span class="sxs-lookup"><span data-stu-id="abe74-576">Situação cadastral</span></span> 
- <span data-ttu-id="abe74-577">Inscrição
</span><span class="sxs-lookup"><span data-stu-id="abe74-577">Inscrição</span></span> 
- <span data-ttu-id="abe74-578">Empresa
</span><span class="sxs-lookup"><span data-stu-id="abe74-578">Empresa</span></span> 
   
## <a name="brazil-national-id-card-rg"></a><span data-ttu-id="abe74-579">	Brazil National ID Card (RG)</span><span class="sxs-lookup"><span data-stu-id="abe74-579">Brazil National ID Card (RG)</span></span>

### <a name="format"></a><span data-ttu-id="abe74-580">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-580">Format</span></span>

<span data-ttu-id="abe74-581">Registro Geral (ancien format) : neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-581">Registro Geral (old format): Nine digits</span></span>

<span data-ttu-id="abe74-582">Registro de Identidade (RIC) (nouveau format) : 11 chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-582">Registro de Identidade (RIC) (new format): 11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-583">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-583">Pattern</span></span>

<span data-ttu-id="abe74-584">Registro Geral (ancien format) :</span><span class="sxs-lookup"><span data-stu-id="abe74-584">Registro Geral (old format):</span></span>
- <span data-ttu-id="abe74-585">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-585">Two digits</span></span> 
- <span data-ttu-id="abe74-586">Un point </span><span class="sxs-lookup"><span data-stu-id="abe74-586">A period</span></span> 
- <span data-ttu-id="abe74-587">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-587">Three digits</span></span> 
- <span data-ttu-id="abe74-588">Un point </span><span class="sxs-lookup"><span data-stu-id="abe74-588">A period</span></span> 
- <span data-ttu-id="abe74-589">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-589">Three digits</span></span> 
- <span data-ttu-id="abe74-590">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="abe74-590">A hyphen</span></span> 
- <span data-ttu-id="abe74-591">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-591">One digit which is a check digit</span></span>

<span data-ttu-id="abe74-592">Registro de Identidade (RIC) (nouveau format) :</span><span class="sxs-lookup"><span data-stu-id="abe74-592">Registro de Identidade (RIC) (new format):</span></span>
- <span data-ttu-id="abe74-593">10 chiffres </span><span class="sxs-lookup"><span data-stu-id="abe74-593">10 digits</span></span> 
- <span data-ttu-id="abe74-594">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="abe74-594">A hyphen</span></span> 
- <span data-ttu-id="abe74-595">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-595">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-596">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-596">Checksum</span></span>

<span data-ttu-id="abe74-597">Oui</span><span class="sxs-lookup"><span data-stu-id="abe74-597">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-598">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-598">Definition</span></span>

<span data-ttu-id="abe74-599">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-599">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-600">La fonction Func_brazil_rg trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-600">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-601">Un mot clé figurant dans la liste Keyword_brazil_rg est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-601">A keyword from Keyword_brazil_rg is found.</span></span>
- <span data-ttu-id="abe74-602">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-602">The checksum passes.</span></span>

<span data-ttu-id="abe74-603">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-603">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-604">La fonction Func_brazil_rg trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-604">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-605">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-605">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-606">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-606">Keywords</span></span>

#### <a name="keywordbrazilrg"></a><span data-ttu-id="abe74-607">Keyword_brazil_rg</span><span class="sxs-lookup"><span data-stu-id="abe74-607">Keyword_brazil_rg</span></span>

<span data-ttu-id="abe74-608">Cédula de identidade carte d’identité id national número de rregistro registro de Iidentidade registro geral RG (ce mot clé respecte la casse) RIC (ce mot clé respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="abe74-608">Cédula de identidade identity card national id número de rregistro registro de Iidentidade registro geral RG (this keyword is case sensitive) RIC (this keyword is case sensitive)</span></span> 
   
## <a name="canada-bank-account-number"></a><span data-ttu-id="abe74-609">Numéro de compte bancaire Canada</span><span class="sxs-lookup"><span data-stu-id="abe74-609">Canada Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-610">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-610">Format</span></span>

<span data-ttu-id="abe74-611">Sept ou douze chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-611">Seven or twelve digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-612">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-612">Pattern</span></span>

<span data-ttu-id="abe74-613">Un numéro de compte bancaire au Canada est composé de sept ou douze chiffres.</span><span class="sxs-lookup"><span data-stu-id="abe74-613">A Canada Bank Account Number is seven or twelve digits.</span></span>

<span data-ttu-id="abe74-614">Un numéro de transit de compte bancaire du Canada est indiqué au format suivant :</span><span class="sxs-lookup"><span data-stu-id="abe74-614">A Canada bank account transit number is:</span></span>
- <span data-ttu-id="abe74-615">Cinq chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-615">Five digits</span></span> 
- <span data-ttu-id="abe74-616">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="abe74-616">A hyphen</span></span> 
- <span data-ttu-id="abe74-617">Trois chiffres ou</span><span class="sxs-lookup"><span data-stu-id="abe74-617">Three digits OR</span></span>
- <span data-ttu-id="abe74-618">Un zéro « 0 » </span><span class="sxs-lookup"><span data-stu-id="abe74-618">A zero "0"</span></span> 
- <span data-ttu-id="abe74-619">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-619">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-620">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-620">Checksum</span></span>

<span data-ttu-id="abe74-621">Non</span><span class="sxs-lookup"><span data-stu-id="abe74-621">No</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-622">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-622">Definition</span></span>

<span data-ttu-id="abe74-623">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-623">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-624">L’expression régulière Regex_canada_bank_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-624">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-625">Un mot clé figurant dans la liste Keyword_canada_bank_account_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-625">A keyword from Keyword_canada_bank_account_number is found.</span></span>
- <span data-ttu-id="abe74-626">L’expression régulière Regex_canada_bank_account_transit_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-626">The regular expression Regex_canada_bank_account_transit_number finds content that matches the pattern.</span></span>

<span data-ttu-id="abe74-627">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-627">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-628">L’expression régulière Regex_canada_bank_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-628">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-629">Un mot clé figurant dans la liste Keyword_canada_bank_account_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-629">A keyword from Keyword_canada_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-630">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-630">Keywords</span></span>

#### <a name="keywordcanadabankaccountnumber"></a><span data-ttu-id="abe74-631">Keyword_canada_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="abe74-631">Keyword_canada_bank_account_number</span></span>

- <span data-ttu-id="abe74-632">obligations d’épargne du Canada</span><span class="sxs-lookup"><span data-stu-id="abe74-632">canada savings bonds</span></span>
- <span data-ttu-id="abe74-633">
agence du revenu du Canada</span><span class="sxs-lookup"><span data-stu-id="abe74-633">canada revenue agency</span></span>
- <span data-ttu-id="abe74-634">
institution financière du Canada</span><span class="sxs-lookup"><span data-stu-id="abe74-634">canadian financial institution</span></span>
- <span data-ttu-id="abe74-635">
formulaire de dépôt direct</span><span class="sxs-lookup"><span data-stu-id="abe74-635">direct deposit form</span></span>
- <span data-ttu-id="abe74-636">
citoyen canadien</span><span class="sxs-lookup"><span data-stu-id="abe74-636">canadian citizen</span></span>
- <span data-ttu-id="abe74-637">
représentant légal</span><span class="sxs-lookup"><span data-stu-id="abe74-637">legal representative</span></span>
- <span data-ttu-id="abe74-638">
notaire</span><span class="sxs-lookup"><span data-stu-id="abe74-638">notary public</span></span>
- <span data-ttu-id="abe74-639">
commissaire à l’assermentation</span><span class="sxs-lookup"><span data-stu-id="abe74-639">commissioner for oaths</span></span>
- <span data-ttu-id="abe74-640">
prestation pour la garde d’enfants</span><span class="sxs-lookup"><span data-stu-id="abe74-640">child care benefit</span></span>
- <span data-ttu-id="abe74-641">
prestation universelle pour la garde d’enfants</span><span class="sxs-lookup"><span data-stu-id="abe74-641">universal child care</span></span>
- <span data-ttu-id="abe74-642">
prestation fiscale canadienne pour enfants</span><span class="sxs-lookup"><span data-stu-id="abe74-642">canada child tax benefit</span></span>
- <span data-ttu-id="abe74-643">
prestation fiscale pour le revenu gagné</span><span class="sxs-lookup"><span data-stu-id="abe74-643">income tax benefit</span></span>
- <span data-ttu-id="abe74-644">
taxe de vente harmonisée</span><span class="sxs-lookup"><span data-stu-id="abe74-644">harmonized sales tax</span></span>
- <span data-ttu-id="abe74-645">numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="abe74-645">social insurance number</span></span>
- <span data-ttu-id="abe74-646">
remboursement d’impôt</span><span class="sxs-lookup"><span data-stu-id="abe74-646">income tax refund</span></span>
- <span data-ttu-id="abe74-647">
prestation fiscale pour enfants</span><span class="sxs-lookup"><span data-stu-id="abe74-647">child tax benefit</span></span>
- <span data-ttu-id="abe74-648">
paiements aux territoires</span><span class="sxs-lookup"><span data-stu-id="abe74-648">territorial payments</span></span>
- <span data-ttu-id="abe74-649">
numéro d’institution</span><span class="sxs-lookup"><span data-stu-id="abe74-649">institution number</span></span>
- <span data-ttu-id="abe74-650">
demande de dépôt</span><span class="sxs-lookup"><span data-stu-id="abe74-650">deposit request</span></span>
- <span data-ttu-id="abe74-651">
informations bancaires</span><span class="sxs-lookup"><span data-stu-id="abe74-651">banking information</span></span>
- <span data-ttu-id="abe74-652">

dépôt direct</span><span class="sxs-lookup"><span data-stu-id="abe74-652">direct deposit</span></span>
   
## <a name="canada-drivers-license-number"></a><span data-ttu-id="abe74-653">Numéro de permis de conduire Canada</span><span class="sxs-lookup"><span data-stu-id="abe74-653">Canada Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-654">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-654">Format</span></span>

<span data-ttu-id="abe74-655">Varie selon la province</span><span class="sxs-lookup"><span data-stu-id="abe74-655">Varies by province</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-656">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-656">Pattern</span></span>

<span data-ttu-id="abe74-657">Plusieurs modèles pour les différentes provinces : Alberta, Colombie-Britannique, Manitoba, Nouveau-Brunswick, Terre-Neuve-et-Labrador, Nouvelle-Écosse, Ontario, Île-du-Prince-Édouard, Québec et Saskatchewan</span><span class="sxs-lookup"><span data-stu-id="abe74-657">Various patterns covering Alberta, British Columbia, Manitoba, New Brunswick, Newfoundland/Labrador, Nova Scotia, Ontario, Prince Edward Island, Quebec, and Saskatchewan</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-658">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-658">Checksum</span></span>

<span data-ttu-id="abe74-659">Non</span><span class="sxs-lookup"><span data-stu-id="abe74-659">No</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-660">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-660">Definition</span></span>

<span data-ttu-id="abe74-661">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-661">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-662">La fonction Func_[province_name]_drivers_license_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-662">The function Func_[province_name]_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-663">Un mot clé figurant dans la liste Keyword_[province_name]_drivers_license_name est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-663">A keyword from Keyword_[province_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="abe74-664">Un mot clé figurant dans la liste Keyword_canada_drivers_license est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-664">A keyword from Keyword_canada_drivers_license is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-665">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-665">Keywords</span></span>

#### <a name="keywordprovincenamedriverslicensename"></a><span data-ttu-id="abe74-666">Keyword_[province_name]_drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="abe74-666">Keyword_[province_name]_drivers_license_name</span></span>

- <span data-ttu-id="abe74-667">L’abréviation de la province, par exemple AB</span><span class="sxs-lookup"><span data-stu-id="abe74-667">The province abbreviation, for example AB</span></span>
- <span data-ttu-id="abe74-668">
Le nom de la province, par exemple Alberta</span><span class="sxs-lookup"><span data-stu-id="abe74-668">The province name, for example Alberta</span></span>

#### <a name="keywordcanadadriverslicense"></a><span data-ttu-id="abe74-669">Keyword_canada_drivers_license</span><span class="sxs-lookup"><span data-stu-id="abe74-669">Keyword_canada_drivers_license</span></span>

- <span data-ttu-id="abe74-670">PC</span><span class="sxs-lookup"><span data-stu-id="abe74-670">DL</span></span>
- <span data-ttu-id="abe74-671">PC</span><span class="sxs-lookup"><span data-stu-id="abe74-671">DLS</span></span>
- <span data-ttu-id="abe74-672">CDL</span><span class="sxs-lookup"><span data-stu-id="abe74-672">CDL</span></span>
- <span data-ttu-id="abe74-673">SYSTÈMES CDL</span><span class="sxs-lookup"><span data-stu-id="abe74-673">CDLS</span></span>
- <span data-ttu-id="abe74-674">DriverLic</span><span class="sxs-lookup"><span data-stu-id="abe74-674">DriverLic</span></span>
- <span data-ttu-id="abe74-675">DriverLics</span><span class="sxs-lookup"><span data-stu-id="abe74-675">DriverLics</span></span>
- <span data-ttu-id="abe74-676">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="abe74-676">DriverLicense</span></span>
- <span data-ttu-id="abe74-677">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="abe74-677">DriverLicenses</span></span>
- <span data-ttu-id="abe74-678">DriverLicence</span><span class="sxs-lookup"><span data-stu-id="abe74-678">DriverLicence</span></span>
- <span data-ttu-id="abe74-679">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="abe74-679">DriverLicences</span></span>
- <span data-ttu-id="abe74-680">Lic pilote</span><span class="sxs-lookup"><span data-stu-id="abe74-680">Driver Lic</span></span>
- <span data-ttu-id="abe74-681">Pilote Lics</span><span class="sxs-lookup"><span data-stu-id="abe74-681">Driver Lics</span></span>
- <span data-ttu-id="abe74-682">Conduire</span><span class="sxs-lookup"><span data-stu-id="abe74-682">Driver License</span></span>
- <span data-ttu-id="abe74-683">Licences de pilote</span><span class="sxs-lookup"><span data-stu-id="abe74-683">Driver Licenses</span></span>
- <span data-ttu-id="abe74-684">Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-684">Driver Licence</span></span>
- <span data-ttu-id="abe74-685">Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-685">Driver Licences</span></span>
- <span data-ttu-id="abe74-686">DriversLic</span><span class="sxs-lookup"><span data-stu-id="abe74-686">DriversLic</span></span>
- <span data-ttu-id="abe74-687">DriversLics</span><span class="sxs-lookup"><span data-stu-id="abe74-687">DriversLics</span></span>
- <span data-ttu-id="abe74-688">DriversLicence</span><span class="sxs-lookup"><span data-stu-id="abe74-688">DriversLicence</span></span>
- <span data-ttu-id="abe74-689">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="abe74-689">DriversLicences</span></span>
- <span data-ttu-id="abe74-690">Conduire</span><span class="sxs-lookup"><span data-stu-id="abe74-690">DriversLicense</span></span>
- <span data-ttu-id="abe74-691">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="abe74-691">DriversLicenses</span></span>
- <span data-ttu-id="abe74-692">Lic pilotes</span><span class="sxs-lookup"><span data-stu-id="abe74-692">Drivers Lic</span></span>
- <span data-ttu-id="abe74-693">Lics pilotes</span><span class="sxs-lookup"><span data-stu-id="abe74-693">Drivers Lics</span></span>
- <span data-ttu-id="abe74-694">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="abe74-694">Drivers License</span></span>
- <span data-ttu-id="abe74-695">Licences de pilotes</span><span class="sxs-lookup"><span data-stu-id="abe74-695">Drivers Licenses</span></span>
- <span data-ttu-id="abe74-696">Certificat de pilotes</span><span class="sxs-lookup"><span data-stu-id="abe74-696">Drivers Licence</span></span>
- <span data-ttu-id="abe74-697">Certificats de pilotes</span><span class="sxs-lookup"><span data-stu-id="abe74-697">Drivers Licences</span></span>
- <span data-ttu-id="abe74-698">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="abe74-698">Driver'Lic</span></span>
- <span data-ttu-id="abe74-699">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="abe74-699">Driver'Lics</span></span>
- <span data-ttu-id="abe74-700">Driver'License</span><span class="sxs-lookup"><span data-stu-id="abe74-700">Driver'License</span></span>
- <span data-ttu-id="abe74-701">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="abe74-701">Driver'Licenses</span></span>
- <span data-ttu-id="abe74-702">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="abe74-702">Driver'Licence</span></span>
- <span data-ttu-id="abe74-703">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="abe74-703">Driver'Licences</span></span>
- <span data-ttu-id="abe74-704">Pilote ' Lic</span><span class="sxs-lookup"><span data-stu-id="abe74-704">Driver' Lic</span></span>
- <span data-ttu-id="abe74-705">Pilote ' Lics</span><span class="sxs-lookup"><span data-stu-id="abe74-705">Driver' Lics</span></span>
- <span data-ttu-id="abe74-706">Pilote ' licence</span><span class="sxs-lookup"><span data-stu-id="abe74-706">Driver' License</span></span>
- <span data-ttu-id="abe74-707">Pilote ' licences</span><span class="sxs-lookup"><span data-stu-id="abe74-707">Driver' Licenses</span></span>
- <span data-ttu-id="abe74-708">Pilote ' certificat</span><span class="sxs-lookup"><span data-stu-id="abe74-708">Driver' Licence</span></span>
- <span data-ttu-id="abe74-709">Pilote « certificats</span><span class="sxs-lookup"><span data-stu-id="abe74-709">Driver' Licences</span></span>
- <span data-ttu-id="abe74-710">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="abe74-710">Driver'sLic</span></span>
- <span data-ttu-id="abe74-711">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="abe74-711">Driver'sLics</span></span>
- <span data-ttu-id="abe74-712">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="abe74-712">Driver'sLicense</span></span>
- <span data-ttu-id="abe74-713">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="abe74-713">Driver'sLicenses</span></span>
- <span data-ttu-id="abe74-714">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="abe74-714">Driver'sLicence</span></span>
- <span data-ttu-id="abe74-715">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="abe74-715">Driver'sLicences</span></span>
- <span data-ttu-id="abe74-716">Lic du pilote</span><span class="sxs-lookup"><span data-stu-id="abe74-716">Driver's Lic</span></span>
- <span data-ttu-id="abe74-717">Lics permis de conduire</span><span class="sxs-lookup"><span data-stu-id="abe74-717">Driver's Lics</span></span>
- <span data-ttu-id="abe74-718">Conduire permis de</span><span class="sxs-lookup"><span data-stu-id="abe74-718">Driver's License</span></span>
- <span data-ttu-id="abe74-719">Conduire permis de</span><span class="sxs-lookup"><span data-stu-id="abe74-719">Driver's Licenses</span></span>
- <span data-ttu-id="abe74-720">Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-720">Driver's Licence</span></span>
- <span data-ttu-id="abe74-721">Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-721">Driver's Licences</span></span>
- <span data-ttu-id="abe74-722">Permis de Conduire</span><span class="sxs-lookup"><span data-stu-id="abe74-722">Permis de Conduire</span></span>
- <span data-ttu-id="abe74-723">id</span><span class="sxs-lookup"><span data-stu-id="abe74-723">id</span></span>
- <span data-ttu-id="abe74-724">ID</span><span class="sxs-lookup"><span data-stu-id="abe74-724">ids</span></span>
- <span data-ttu-id="abe74-725">
numéro carte d’identification</span><span class="sxs-lookup"><span data-stu-id="abe74-725">idcard number</span></span>
- <span data-ttu-id="abe74-726">
numéros carte d’identification</span><span class="sxs-lookup"><span data-stu-id="abe74-726">idcard numbers</span></span>
- <span data-ttu-id="abe74-727">
# carte d’identification</span><span class="sxs-lookup"><span data-stu-id="abe74-727">idcard #</span></span>
- <span data-ttu-id="abe74-728">
# carte d’identification</span><span class="sxs-lookup"><span data-stu-id="abe74-728">idcard #s</span></span>
- <span data-ttu-id="abe74-729">carte idcard</span><span class="sxs-lookup"><span data-stu-id="abe74-729">idcard card</span></span>
- <span data-ttu-id="abe74-730">cartes idcard</span><span class="sxs-lookup"><span data-stu-id="abe74-730">idcard cards</span></span>
- <span data-ttu-id="abe74-731">idcard</span><span class="sxs-lookup"><span data-stu-id="abe74-731">idcard</span></span>
- <span data-ttu-id="abe74-732">numéro d’identification
</span><span class="sxs-lookup"><span data-stu-id="abe74-732">identification number</span></span>
- <span data-ttu-id="abe74-733">numéros d’identification
</span><span class="sxs-lookup"><span data-stu-id="abe74-733">identification numbers</span></span>
- <span data-ttu-id="abe74-734"># identification
</span><span class="sxs-lookup"><span data-stu-id="abe74-734">identification #</span></span>
- <span data-ttu-id="abe74-735">
# identification</span><span class="sxs-lookup"><span data-stu-id="abe74-735">identification #s</span></span>
- <span data-ttu-id="abe74-736">carte d’identification</span><span class="sxs-lookup"><span data-stu-id="abe74-736">identification card</span></span>
- <span data-ttu-id="abe74-737">cartes d’identification</span><span class="sxs-lookup"><span data-stu-id="abe74-737">identification cards</span></span>
- <span data-ttu-id="abe74-738">
identification
</span><span class="sxs-lookup"><span data-stu-id="abe74-738">identification</span></span> 
- <span data-ttu-id="abe74-739"># PC</span><span class="sxs-lookup"><span data-stu-id="abe74-739">DL#</span></span>
- <span data-ttu-id="abe74-740">
# PC
</span><span class="sxs-lookup"><span data-stu-id="abe74-740">DLS#</span></span> 
- <span data-ttu-id="abe74-741"># PCD
</span><span class="sxs-lookup"><span data-stu-id="abe74-741">CDL#</span></span> 
- <span data-ttu-id="abe74-742"># PCD
</span><span class="sxs-lookup"><span data-stu-id="abe74-742">CDLS#</span></span> 
- <span data-ttu-id="abe74-743">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="abe74-743">DriverLic#</span></span> 
- <span data-ttu-id="abe74-744">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="abe74-744">DriverLics#</span></span> 
- <span data-ttu-id="abe74-745">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="abe74-745">DriverLicense#</span></span> 
- <span data-ttu-id="abe74-746">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="abe74-746">DriverLicenses#</span></span> 
- <span data-ttu-id="abe74-747">DriverLicence #</span><span class="sxs-lookup"><span data-stu-id="abe74-747">DriverLicence#</span></span> 
- <span data-ttu-id="abe74-748">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="abe74-748">DriverLicences#</span></span> 
- <span data-ttu-id="abe74-749">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="abe74-749">Driver Lic#</span></span>
- <span data-ttu-id="abe74-750">
#Permis conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-750">Driver Lics#</span></span> 
- <span data-ttu-id="abe74-751">Pilote licence #</span><span class="sxs-lookup"><span data-stu-id="abe74-751">Driver License#</span></span> 
- <span data-ttu-id="abe74-752">Licences de pilote #</span><span class="sxs-lookup"><span data-stu-id="abe74-752">Driver Licenses#</span></span> 
- <span data-ttu-id="abe74-753">Pilote licence #</span><span class="sxs-lookup"><span data-stu-id="abe74-753">Driver License#</span></span> 
- <span data-ttu-id="abe74-754">Pilote certificats #</span><span class="sxs-lookup"><span data-stu-id="abe74-754">Driver Licences#</span></span> 
- <span data-ttu-id="abe74-755">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="abe74-755">DriversLic#</span></span> 
- <span data-ttu-id="abe74-756">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="abe74-756">DriversLics#</span></span> 
- <span data-ttu-id="abe74-757">Conduire #</span><span class="sxs-lookup"><span data-stu-id="abe74-757">DriversLicense#</span></span> 
- <span data-ttu-id="abe74-758">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="abe74-758">DriversLicenses#</span></span> 
- <span data-ttu-id="abe74-759">DriversLicence #</span><span class="sxs-lookup"><span data-stu-id="abe74-759">DriversLicence#</span></span> 
- <span data-ttu-id="abe74-760">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="abe74-760">DriversLicences#</span></span> 
- <span data-ttu-id="abe74-761">Pilotes Lic #</span><span class="sxs-lookup"><span data-stu-id="abe74-761">Drivers Lic#</span></span> 
- <span data-ttu-id="abe74-762">Pilotes Lics #</span><span class="sxs-lookup"><span data-stu-id="abe74-762">Drivers Lics#</span></span> 
- <span data-ttu-id="abe74-763">Licence pilotes #</span><span class="sxs-lookup"><span data-stu-id="abe74-763">Drivers License#</span></span> 
- <span data-ttu-id="abe74-764">Licences pilotes #</span><span class="sxs-lookup"><span data-stu-id="abe74-764">Drivers Licenses#</span></span> 
- <span data-ttu-id="abe74-765">Licence pilotes #</span><span class="sxs-lookup"><span data-stu-id="abe74-765">Drivers Licence#</span></span> 
- <span data-ttu-id="abe74-766">Certificats pilotes #</span><span class="sxs-lookup"><span data-stu-id="abe74-766">Drivers Licences#</span></span> 
- <span data-ttu-id="abe74-767">#Permisconduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-767">Driver'Lic#</span></span> 
- <span data-ttu-id="abe74-768">#Permisconduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-768">Driver'Lics#</span></span> 
- <span data-ttu-id="abe74-769">#Permisdeconduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-769">Driver'License#</span></span> 
- <span data-ttu-id="abe74-770">#Permisdeconduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-770">Driver'Licenses#</span></span> 
- <span data-ttu-id="abe74-771">#Permisdeconduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-771">Driver'Licence#</span></span> 
- <span data-ttu-id="abe74-772">#Permisdeconduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-772">Driver'Licences#</span></span> 
- <span data-ttu-id="abe74-773">#Permis conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-773">Driver' Lic#</span></span> 
- <span data-ttu-id="abe74-774">#Permis conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-774">Driver' Lics#</span></span> 
- <span data-ttu-id="abe74-775">#Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-775">Driver' License#</span></span> 
- <span data-ttu-id="abe74-776">#Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-776">Driver' Licenses#</span></span> 
- <span data-ttu-id="abe74-777">Pilote ' certificat #</span><span class="sxs-lookup"><span data-stu-id="abe74-777">Driver' Licence#</span></span> 
- <span data-ttu-id="abe74-778">Pilote « certificats #</span><span class="sxs-lookup"><span data-stu-id="abe74-778">Driver' Licences#</span></span> 
- <span data-ttu-id="abe74-779">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="abe74-779">Driver'sLic#</span></span> 
- <span data-ttu-id="abe74-780">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="abe74-780">Driver'sLics#</span></span> 
- <span data-ttu-id="abe74-781">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="abe74-781">Driver'sLicense#</span></span> 
- <span data-ttu-id="abe74-782">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="abe74-782">Driver'sLicenses#</span></span> 
- <span data-ttu-id="abe74-783">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="abe74-783">Driver'sLicence#</span></span> 
- <span data-ttu-id="abe74-784">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="abe74-784">Driver'sLicences#</span></span> 
- <span data-ttu-id="abe74-785">#Permisconduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-785">Driver's Lic#</span></span> 
- <span data-ttu-id="abe74-786">#Permisconduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-786">Driver's Lics#</span></span> 
- <span data-ttu-id="abe74-787">#Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-787">Driver's License#</span></span> 
- <span data-ttu-id="abe74-788">#Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-788">Driver's Licenses#</span></span> 
- <span data-ttu-id="abe74-789">Certificat de # permis de conduire</span><span class="sxs-lookup"><span data-stu-id="abe74-789">Driver's Licence#</span></span> 
- <span data-ttu-id="abe74-790">Certificats de # permis de conduire</span><span class="sxs-lookup"><span data-stu-id="abe74-790">Driver's Licences#</span></span> 
- <span data-ttu-id="abe74-791">Permis de Conduire #</span><span class="sxs-lookup"><span data-stu-id="abe74-791">Permis de Conduire#</span></span> 
- <span data-ttu-id="abe74-792">numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="abe74-792">id#</span></span> 
- <span data-ttu-id="abe74-793">ID #</span><span class="sxs-lookup"><span data-stu-id="abe74-793">ids#</span></span> 
- <span data-ttu-id="abe74-794">#carte carte d’identification
</span><span class="sxs-lookup"><span data-stu-id="abe74-794">idcard card#</span></span> 
- <span data-ttu-id="abe74-795">#cartes carte d’identification
</span><span class="sxs-lookup"><span data-stu-id="abe74-795">idcard cards#</span></span> 
- <span data-ttu-id="abe74-796">#carte d’identification
</span><span class="sxs-lookup"><span data-stu-id="abe74-796">idcard#</span></span> 
- <span data-ttu-id="abe74-797">#carte d’identification
</span><span class="sxs-lookup"><span data-stu-id="abe74-797">identification card#</span></span> 
- <span data-ttu-id="abe74-798">#cartes d’identification
</span><span class="sxs-lookup"><span data-stu-id="abe74-798">identification cards#</span></span> 
- <span data-ttu-id="abe74-799">#identification
</span><span class="sxs-lookup"><span data-stu-id="abe74-799">identification#</span></span> 
   
## <a name="canada-health-service-number"></a><span data-ttu-id="abe74-800">Numéro de service de santé Canada</span><span class="sxs-lookup"><span data-stu-id="abe74-800">Canada Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-801">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-801">Format</span></span>

<span data-ttu-id="abe74-802">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-802">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-803">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-803">Pattern</span></span>

<span data-ttu-id="abe74-804">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-804">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-805">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-805">Checksum</span></span>

<span data-ttu-id="abe74-806">Non</span><span class="sxs-lookup"><span data-stu-id="abe74-806">No</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-807">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-807">Definition</span></span>

<span data-ttu-id="abe74-808">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-808">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-809">L’expression régulière Regex_canada_health_service_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-809">The regular expression Regex_canada_health_service_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-810">Un mot clé figurant dans la liste Keyword_canada_health_service_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-810">A keyword from Keyword_canada_health_service_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-811">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-811">Keywords</span></span>

#### <a name="keywordcanadahealthservicenumber"></a><span data-ttu-id="abe74-812">Keyword_canada_health_service_number</span><span class="sxs-lookup"><span data-stu-id="abe74-812">Keyword_canada_health_service_number</span></span>

- <span data-ttu-id="abe74-813">numéro d’assurance-maladie</span><span class="sxs-lookup"><span data-stu-id="abe74-813">personal health number</span></span>
- <span data-ttu-id="abe74-814">
informations sur le patient</span><span class="sxs-lookup"><span data-stu-id="abe74-814">patient information</span></span>
- <span data-ttu-id="abe74-815">services de santé</span><span class="sxs-lookup"><span data-stu-id="abe74-815">health services</span></span>
- <span data-ttu-id="abe74-816">
services spécialisés</span><span class="sxs-lookup"><span data-stu-id="abe74-816">speciality services</span></span>
- <span data-ttu-id="abe74-817">
accident automobile</span><span class="sxs-lookup"><span data-stu-id="abe74-817">automobile accident</span></span>
- <span data-ttu-id="abe74-818">
hôpital pour malades</span><span class="sxs-lookup"><span data-stu-id="abe74-818">patient hospital</span></span>
- <span data-ttu-id="abe74-819">
psychiatre</span><span class="sxs-lookup"><span data-stu-id="abe74-819">psychiatrist</span></span>
- <span data-ttu-id="abe74-820">
indemnisation des salariés</span><span class="sxs-lookup"><span data-stu-id="abe74-820">workers compensation</span></span>
- <span data-ttu-id="abe74-821">
handicap</span><span class="sxs-lookup"><span data-stu-id="abe74-821">disability</span></span>
      
## <a name="canada-passport-number"></a><span data-ttu-id="abe74-822">Numéro de passeport Canada</span><span class="sxs-lookup"><span data-stu-id="abe74-822">Canada Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-823">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-823">Format</span></span>

<span data-ttu-id="abe74-824">Deux lettres majuscules suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-824">Two uppercase letters followed by six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-825">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-825">Pattern</span></span>

<span data-ttu-id="abe74-826">Deux lettres majuscules suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-826">Two uppercase letters followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-827">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-827">Checksum</span></span>

<span data-ttu-id="abe74-828">Non</span><span class="sxs-lookup"><span data-stu-id="abe74-828">No</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-829">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-829">Definition</span></span>

<span data-ttu-id="abe74-830">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-830">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-831">L’expression régulière Regex_canada_passport_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-831">The regular expression Regex_canada_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-832">Un mot clé à partir de Keyword_canada_passport_number ou Keyword_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-832">A keyword from Keyword_canada_passport_number or Keyword_passport is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-833">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-833">Keywords</span></span>

#### <a name="keywordcanadapassportnumber"></a><span data-ttu-id="abe74-834">Keyword_canada_passport_number</span><span class="sxs-lookup"><span data-stu-id="abe74-834">Keyword_canada_passport_number</span></span>

- <span data-ttu-id="abe74-835">citoyenneté canadienne</span><span class="sxs-lookup"><span data-stu-id="abe74-835">canadian citizenship</span></span>
- <span data-ttu-id="abe74-836">
passeport canadien</span><span class="sxs-lookup"><span data-stu-id="abe74-836">canadian passport</span></span>
- <span data-ttu-id="abe74-837">
demande de passeport</span><span class="sxs-lookup"><span data-stu-id="abe74-837">passport application</span></span>
- <span data-ttu-id="abe74-838">
photos pour passeport</span><span class="sxs-lookup"><span data-stu-id="abe74-838">passport photos</span></span>
- <span data-ttu-id="abe74-839">
traducteur agréé</span><span class="sxs-lookup"><span data-stu-id="abe74-839">certified translator</span></span>
- <span data-ttu-id="abe74-840">
citoyens canadiens</span><span class="sxs-lookup"><span data-stu-id="abe74-840">canadian citizens</span></span>
- <span data-ttu-id="abe74-841">
temps de traitement</span><span class="sxs-lookup"><span data-stu-id="abe74-841">processing times</span></span>
- <span data-ttu-id="abe74-842">

demande de renouvellement</span><span class="sxs-lookup"><span data-stu-id="abe74-842">renewal application</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="abe74-843">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="abe74-843">Keyword_passport</span></span>

- <span data-ttu-id="abe74-844">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="abe74-844">Passport Number</span></span>
- <span data-ttu-id="abe74-845">
N° de passeport</span><span class="sxs-lookup"><span data-stu-id="abe74-845">Passport No</span></span>
- <span data-ttu-id="abe74-846"># Passeport
</span><span class="sxs-lookup"><span data-stu-id="abe74-846">Passport #</span></span>
- <span data-ttu-id="abe74-847">#Passeport
</span><span class="sxs-lookup"><span data-stu-id="abe74-847">Passport#</span></span>
- <span data-ttu-id="abe74-848">IDPassport</span><span class="sxs-lookup"><span data-stu-id="abe74-848">PassportID</span></span>
- <span data-ttu-id="abe74-849">n° passeport
</span><span class="sxs-lookup"><span data-stu-id="abe74-849">Passportno</span></span>
- <span data-ttu-id="abe74-850">numéropasseport
</span><span class="sxs-lookup"><span data-stu-id="abe74-850">passportnumber</span></span>
- <span data-ttu-id="abe74-851">パスポート</span><span class="sxs-lookup"><span data-stu-id="abe74-851">パスポート</span></span>
- <span data-ttu-id="abe74-852">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="abe74-852">パスポート番号</span></span>
- <span data-ttu-id="abe74-853">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="abe74-853">パスポートのNum</span></span>
- <span data-ttu-id="abe74-854">パスポート＃
</span><span class="sxs-lookup"><span data-stu-id="abe74-854">パスポート＃</span></span>
- <span data-ttu-id="abe74-855">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="abe74-855">Numéro de passeport</span></span>
- <span data-ttu-id="abe74-856">
Passeport n°</span><span class="sxs-lookup"><span data-stu-id="abe74-856">Passeport n °</span></span>
- <span data-ttu-id="abe74-857">Passeport numéro
</span><span class="sxs-lookup"><span data-stu-id="abe74-857">Passeport Non</span></span>
- <span data-ttu-id="abe74-858"># Passeport
</span><span class="sxs-lookup"><span data-stu-id="abe74-858">Passeport #</span></span>
- <span data-ttu-id="abe74-859">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="abe74-859">Passeport#</span></span>
- <span data-ttu-id="abe74-860">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="abe74-860">PasseportNon</span></span>
- <span data-ttu-id="abe74-861">

Passeportn °</span><span class="sxs-lookup"><span data-stu-id="abe74-861">Passeportn °</span></span>
   
## <a name="canada-personal-health-identification-number-phin"></a><span data-ttu-id="abe74-862">NIMP (numéro d'identification médicale personnel) Canada</span><span class="sxs-lookup"><span data-stu-id="abe74-862">Canada Personal Health Identification Number (PHIN)</span></span>

### <a name="format"></a><span data-ttu-id="abe74-863">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-863">Format</span></span>

<span data-ttu-id="abe74-864">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-864">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-865">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-865">Pattern</span></span>

<span data-ttu-id="abe74-866">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-866">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-867">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-867">Checksum</span></span>

<span data-ttu-id="abe74-868">Non</span><span class="sxs-lookup"><span data-stu-id="abe74-868">No</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-869">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-869">Definition</span></span>

<span data-ttu-id="abe74-p104">Une stratégie DLP est convaincu que ce type d’informations sensibles a été détecté à 75 % if, au sein d’une proximité de 300 caractères : l’expression régulière Regex_canada_phin recherche de contenu qui correspond au modèle. Contient des mots clés au moins deux des Keyword_canada_phin Keyword_canada_provinces...</span><span class="sxs-lookup"><span data-stu-id="abe74-p104">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_canada_phin finds content that matches the pattern. At least two keywords from Keyword_canada_phin or Keyword_canada_provinces are found..</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-872">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-872">Keywords</span></span>

#### <a name="keywordcanadaphin"></a><span data-ttu-id="abe74-873">Keyword_canada_phin</span><span class="sxs-lookup"><span data-stu-id="abe74-873">Keyword_canada_phin</span></span>

- <span data-ttu-id="abe74-874">numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="abe74-874">social insurance number</span></span>
- <span data-ttu-id="abe74-875">
loi sur les renseignements médicaux</span><span class="sxs-lookup"><span data-stu-id="abe74-875">health information act</span></span>
- <span data-ttu-id="abe74-876">
renseignements relatifs à l’impôt sur le revenu</span><span class="sxs-lookup"><span data-stu-id="abe74-876">income tax information</span></span>
- <span data-ttu-id="abe74-877">
santé Manitoba</span><span class="sxs-lookup"><span data-stu-id="abe74-877">manitoba health</span></span>
- <span data-ttu-id="abe74-878">
enregistrement aux services de santé</span><span class="sxs-lookup"><span data-stu-id="abe74-878">health registration</span></span>
- <span data-ttu-id="abe74-879">
achats de médicaments sur ordonnance</span><span class="sxs-lookup"><span data-stu-id="abe74-879">prescription purchases</span></span>
- <span data-ttu-id="abe74-880">
admissibilité aux prestations</span><span class="sxs-lookup"><span data-stu-id="abe74-880">benefit eligibility</span></span>
- <span data-ttu-id="abe74-881">
santé personnelle</span><span class="sxs-lookup"><span data-stu-id="abe74-881">personal health</span></span>
- <span data-ttu-id="abe74-882">
procuration</span><span class="sxs-lookup"><span data-stu-id="abe74-882">power of attorney</span></span>
- <span data-ttu-id="abe74-883">
numéro d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="abe74-883">registration number</span></span>
- <span data-ttu-id="abe74-884">numéro d’assurance-maladie</span><span class="sxs-lookup"><span data-stu-id="abe74-884">personal health number</span></span>
- <span data-ttu-id="abe74-885">
recommandation par le médecin</span><span class="sxs-lookup"><span data-stu-id="abe74-885">practitioner referral</span></span>
- <span data-ttu-id="abe74-886">
professionnel de bien-être</span><span class="sxs-lookup"><span data-stu-id="abe74-886">wellness professional</span></span>
- <span data-ttu-id="abe74-887">
orientation d’un patient</span><span class="sxs-lookup"><span data-stu-id="abe74-887">patient referral</span></span>
- <span data-ttu-id="abe74-888">

santé et bien-être</span><span class="sxs-lookup"><span data-stu-id="abe74-888">health and wellness</span></span>

#### <a name="keywordcanadaprovinces"></a><span data-ttu-id="abe74-889">Keyword_canada_provinces</span><span class="sxs-lookup"><span data-stu-id="abe74-889">Keyword_canada_provinces</span></span>

- <span data-ttu-id="abe74-890">Nunavut</span><span class="sxs-lookup"><span data-stu-id="abe74-890">Nunavut</span></span>
- <span data-ttu-id="abe74-891">
Québec</span><span class="sxs-lookup"><span data-stu-id="abe74-891">Quebec</span></span>
- <span data-ttu-id="abe74-892">
Territoires du Nord-Ouest</span><span class="sxs-lookup"><span data-stu-id="abe74-892">Northwest Territories</span></span>
- <span data-ttu-id="abe74-893">
Ontario</span><span class="sxs-lookup"><span data-stu-id="abe74-893">Ontario</span></span>
- <span data-ttu-id="abe74-894">
Colombie-britannique</span><span class="sxs-lookup"><span data-stu-id="abe74-894">British Columbia</span></span>
- <span data-ttu-id="abe74-895">
Alberta</span><span class="sxs-lookup"><span data-stu-id="abe74-895">Alberta</span></span>
- <span data-ttu-id="abe74-896">
Saskatchewan</span><span class="sxs-lookup"><span data-stu-id="abe74-896">Saskatchewan</span></span>
- <span data-ttu-id="abe74-897">
Manitoba</span><span class="sxs-lookup"><span data-stu-id="abe74-897">Manitoba</span></span>
- <span data-ttu-id="abe74-898">
Yukon</span><span class="sxs-lookup"><span data-stu-id="abe74-898">Yukon</span></span>
- <span data-ttu-id="abe74-899">
Terre-Neuve-et-Labrador</span><span class="sxs-lookup"><span data-stu-id="abe74-899">Newfoundland and Labrador</span></span>
- <span data-ttu-id="abe74-900">
Nouveau-Brunswick</span><span class="sxs-lookup"><span data-stu-id="abe74-900">New Brunswick</span></span>
- <span data-ttu-id="abe74-901">
Nouvelle-Écosse</span><span class="sxs-lookup"><span data-stu-id="abe74-901">Nova Scotia</span></span>
- <span data-ttu-id="abe74-902">
Île-du-Prince-Édouard</span><span class="sxs-lookup"><span data-stu-id="abe74-902">Prince Edward Island</span></span>
- <span data-ttu-id="abe74-903">Canada</span><span class="sxs-lookup"><span data-stu-id="abe74-903">Canada</span></span>
   
## <a name="canada-social-insurance-number"></a><span data-ttu-id="abe74-904">Numéro d'assurance sociale Canada</span><span class="sxs-lookup"><span data-stu-id="abe74-904">Canada Social Insurance Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-905">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-905">Format</span></span>

<span data-ttu-id="abe74-906">Neuf chiffres avec éventuellement des traits d’union ou des espaces</span><span class="sxs-lookup"><span data-stu-id="abe74-906">Nine digits with optional hyphens or spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-907">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-907">Pattern</span></span>

<span data-ttu-id="abe74-908">Mis en forme :</span><span class="sxs-lookup"><span data-stu-id="abe74-908">Formatted:</span></span>
- <span data-ttu-id="abe74-909">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-909">Three digits</span></span> 
- <span data-ttu-id="abe74-910">Un trait d’union ou un espace </span><span class="sxs-lookup"><span data-stu-id="abe74-910">A hyphen or space</span></span> 
- <span data-ttu-id="abe74-911">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-911">Three digits</span></span> 
- <span data-ttu-id="abe74-912">Un trait d’union ou un espace </span><span class="sxs-lookup"><span data-stu-id="abe74-912">A hyphen or space</span></span> 
- <span data-ttu-id="abe74-913">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-913">Three digits</span></span>

<span data-ttu-id="abe74-914">Non formatée : Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-914">Unformatted: Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-915">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-915">Checksum</span></span>

<span data-ttu-id="abe74-916">Oui</span><span class="sxs-lookup"><span data-stu-id="abe74-916">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-917">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-917">Definition</span></span>

<span data-ttu-id="abe74-918">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-918">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-919">La fonction Func_canadian_sin trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-919">The function Func_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-920">Au moins deux des éléments suivants, quelle que soit la combinaison :</span><span class="sxs-lookup"><span data-stu-id="abe74-920">At least two of any combination of the following:</span></span>
    - <span data-ttu-id="abe74-921">Un mot clé figurant dans la liste Keyword_sin est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-921">A keyword from Keyword_sin is found.</span></span>
    - <span data-ttu-id="abe74-922">Un mot clé figurant dans la liste Keyword_sin_collaborative est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-922">A keyword from Keyword_sin_collaborative is found.</span></span>
    - <span data-ttu-id="abe74-923">La fonction Func_eu_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="abe74-923">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="abe74-924">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-924">The checksum passes.</span></span>

<span data-ttu-id="abe74-925">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-925">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-926">La fonction Func_unformatted_canadian_sin trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-926">The function Func_unformatted_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-927">Un mot clé figurant dans la liste Keyword_sin est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-927">A keyword from Keyword_sin is found.</span></span>
- <span data-ttu-id="abe74-928">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-928">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-929">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-929">Keywords</span></span>

#### <a name="keywordsin"></a><span data-ttu-id="abe74-930">Keyword_sin</span><span class="sxs-lookup"><span data-stu-id="abe74-930">Keyword_sin</span></span>

- <span data-ttu-id="abe74-931">sin</span><span class="sxs-lookup"><span data-stu-id="abe74-931">sin</span></span> 
- <span data-ttu-id="abe74-932">assurance sociale
</span><span class="sxs-lookup"><span data-stu-id="abe74-932">social insurance</span></span> 
- <span data-ttu-id="abe74-933">numéro d’assurance sociale
</span><span class="sxs-lookup"><span data-stu-id="abe74-933">numero d'assurance sociale</span></span> 
- <span data-ttu-id="abe74-934">assoc
</span><span class="sxs-lookup"><span data-stu-id="abe74-934">sins</span></span> 
- <span data-ttu-id="abe74-935">ssn</span><span class="sxs-lookup"><span data-stu-id="abe74-935">ssn</span></span> 
- <span data-ttu-id="abe74-936">sécurité sociale.</span><span class="sxs-lookup"><span data-stu-id="abe74-936">ssns</span></span> 
- <span data-ttu-id="abe74-937">sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="abe74-937">social security</span></span> 
- <span data-ttu-id="abe74-938">numéro d’assurance sociale
</span><span class="sxs-lookup"><span data-stu-id="abe74-938">numero d'assurance social</span></span> 
- <span data-ttu-id="abe74-939">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="abe74-939">national identification number</span></span> 
- <span data-ttu-id="abe74-940">
id national</span><span class="sxs-lookup"><span data-stu-id="abe74-940">national id</span></span> 
- <span data-ttu-id="abe74-941"># assoc
</span><span class="sxs-lookup"><span data-stu-id="abe74-941">sin#</span></span> 
- <span data-ttu-id="abe74-942">ass soc
</span><span class="sxs-lookup"><span data-stu-id="abe74-942">soc ins</span></span> 
- <span data-ttu-id="abe74-943">ass sociale
</span><span class="sxs-lookup"><span data-stu-id="abe74-943">social ins</span></span> 

#### <a name="keywordsincollaborative"></a><span data-ttu-id="abe74-944">Keyword_sin_collaborative</span><span class="sxs-lookup"><span data-stu-id="abe74-944">Keyword_sin_collaborative</span></span>

- <span data-ttu-id="abe74-945">driver’s license</span><span class="sxs-lookup"><span data-stu-id="abe74-945">driver's license</span></span> 
- <span data-ttu-id="abe74-946">drivers license</span><span class="sxs-lookup"><span data-stu-id="abe74-946">drivers license</span></span> 
- <span data-ttu-id="abe74-947">conduire permis de</span><span class="sxs-lookup"><span data-stu-id="abe74-947">driver's licence</span></span> 
- <span data-ttu-id="abe74-948">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="abe74-948">drivers licence</span></span> 
- <span data-ttu-id="abe74-949">DDN
</span><span class="sxs-lookup"><span data-stu-id="abe74-949">DOB</span></span> 
- <span data-ttu-id="abe74-950">Birthdate</span><span class="sxs-lookup"><span data-stu-id="abe74-950">Birthdate</span></span> 
- <span data-ttu-id="abe74-951">Anniversaire </span><span class="sxs-lookup"><span data-stu-id="abe74-951">Birthday</span></span> 
- <span data-ttu-id="abe74-952">Date of Birth
</span><span class="sxs-lookup"><span data-stu-id="abe74-952">Date of Birth</span></span> 
   
## <a name="chile-identity-card-number"></a><span data-ttu-id="abe74-953">	Numéro de carte d’identité Chili</span><span class="sxs-lookup"><span data-stu-id="abe74-953">Chile Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-954">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-954">Format</span></span>

<span data-ttu-id="abe74-955">7-8 chiffres plus délimiteurs un chiffre de contrôle ou d’une lettre</span><span class="sxs-lookup"><span data-stu-id="abe74-955">7-8 digits plus delimiters a check digit or letter</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-956">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-956">Pattern</span></span>

<span data-ttu-id="abe74-957">7 ou 8 chiffres, plus des délimiteurs :</span><span class="sxs-lookup"><span data-stu-id="abe74-957">7-8 digits plus delimiters:</span></span>
- <span data-ttu-id="abe74-958">1 ou 2 chiffres </span><span class="sxs-lookup"><span data-stu-id="abe74-958">1-2 digits</span></span> 
- <span data-ttu-id="abe74-959">Un point </span><span class="sxs-lookup"><span data-stu-id="abe74-959">A period</span></span> 
- <span data-ttu-id="abe74-960">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-960">Three digits</span></span> 
- <span data-ttu-id="abe74-961">Un point </span><span class="sxs-lookup"><span data-stu-id="abe74-961">A period</span></span> 
- <span data-ttu-id="abe74-962">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-962">Three digits</span></span> 
- <span data-ttu-id="abe74-963">Un tiret</span><span class="sxs-lookup"><span data-stu-id="abe74-963">A dash</span></span> 
- <span data-ttu-id="abe74-964">Un chiffre ou une lettre (ne respectant pas la casse) de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-964">One digit or letter (not case sensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-965">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-965">Checksum</span></span>

<span data-ttu-id="abe74-966">Oui</span><span class="sxs-lookup"><span data-stu-id="abe74-966">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-967">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-967">Definition</span></span>

<span data-ttu-id="abe74-968">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-968">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-969">La fonction Func_chile_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-969">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-970">Un mot clé figurant dans la liste Keyword_chile_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-970">A keyword from Keyword_chile_id_card is found.</span></span>
- <span data-ttu-id="abe74-971">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-971">The checksum passes.</span></span>

<span data-ttu-id="abe74-972">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-972">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-973">La fonction Func_chile_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-973">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-974">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-974">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-975">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-975">Keywords</span></span>

#### <a name="keywordchileidcard"></a><span data-ttu-id="abe74-976">Keyword_chile_id_card</span><span class="sxs-lookup"><span data-stu-id="abe74-976">Keyword_chile_id_card</span></span>

- <span data-ttu-id="abe74-977">National Identification Number
</span><span class="sxs-lookup"><span data-stu-id="abe74-977">National Identification Number</span></span> 
- <span data-ttu-id="abe74-978">Identity card</span><span class="sxs-lookup"><span data-stu-id="abe74-978">Identity card</span></span> 
- <span data-ttu-id="abe74-979">ID</span><span class="sxs-lookup"><span data-stu-id="abe74-979">ID</span></span> 
- <span data-ttu-id="abe74-980">Identification</span><span class="sxs-lookup"><span data-stu-id="abe74-980">Identification</span></span> 
- <span data-ttu-id="abe74-981">Rol Único Nacional
</span><span class="sxs-lookup"><span data-stu-id="abe74-981">Rol Único Nacional</span></span> 
- <span data-ttu-id="abe74-982">EXÉCUTER</span><span class="sxs-lookup"><span data-stu-id="abe74-982">RUN</span></span> 
- <span data-ttu-id="abe74-983">Rol Único Tributario
</span><span class="sxs-lookup"><span data-stu-id="abe74-983">Rol Único Tributario</span></span> 
- <span data-ttu-id="abe74-984">RUT
</span><span class="sxs-lookup"><span data-stu-id="abe74-984">RUT</span></span> 
- <span data-ttu-id="abe74-985">Cédula de Identidad
</span><span class="sxs-lookup"><span data-stu-id="abe74-985">Cédula de Identidad</span></span> 
- <span data-ttu-id="abe74-986">Número De Identificación Nacional
</span><span class="sxs-lookup"><span data-stu-id="abe74-986">Número De Identificación Nacional</span></span> 
- <span data-ttu-id="abe74-987">Tarjeta de identificación
</span><span class="sxs-lookup"><span data-stu-id="abe74-987">Tarjeta de identificación</span></span> 
- <span data-ttu-id="abe74-988">Identificación
</span><span class="sxs-lookup"><span data-stu-id="abe74-988">Identificación</span></span> 
   
## <a name="china-resident-identity-card-prc-number"></a><span data-ttu-id="abe74-989">	Numéro de carte d’identité de résident Chine (RPC)</span><span class="sxs-lookup"><span data-stu-id="abe74-989">China Resident Identity Card (PRC) Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-990">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-990">Format</span></span>

<span data-ttu-id="abe74-991">18 chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-991">18 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-992">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-992">Pattern</span></span>

<span data-ttu-id="abe74-993">18 chiffres :</span><span class="sxs-lookup"><span data-stu-id="abe74-993">18 digits:</span></span>
- <span data-ttu-id="abe74-994">Six chiffres qui composent un code d’adresse </span><span class="sxs-lookup"><span data-stu-id="abe74-994">Six digits which are an address code</span></span> 
- <span data-ttu-id="abe74-995">Huit chiffres sous la forme AAAAMMJJ qui correspondent à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="abe74-995">Eight digits in the form YYYYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="abe74-996">Trois chiffres qui correspondent à un code d’opération </span><span class="sxs-lookup"><span data-stu-id="abe74-996">Three digits which are an order code</span></span> 
- <span data-ttu-id="abe74-997">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-997">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-998">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-998">Checksum</span></span>

<span data-ttu-id="abe74-999">Oui</span><span class="sxs-lookup"><span data-stu-id="abe74-999">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-1000">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-1000">Definition</span></span>

<span data-ttu-id="abe74-1001">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-1001">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-1002">La fonction Func_china_resident_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-1002">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-1003">Un mot clé figurant dans la liste Keyword_china_resident_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-1003">A keyword from Keyword_china_resident_id is found.</span></span>
- <span data-ttu-id="abe74-1004">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-1004">The checksum passes.</span></span>

<span data-ttu-id="abe74-1005">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-1005">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-1006">La fonction Func_china_resident_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-1006">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-1007">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-1007">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-1008">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-1008">Keywords</span></span>

### <a name="keywordchinaresidentid"></a><span data-ttu-id="abe74-1009">Keyword_china_resident_id</span><span class="sxs-lookup"><span data-stu-id="abe74-1009">Keyword_china_resident_id</span></span>

- <span data-ttu-id="abe74-1010">Resident Identity Card
</span><span class="sxs-lookup"><span data-stu-id="abe74-1010">Resident Identity Card</span></span> 
- <span data-ttu-id="abe74-1011">PRC
</span><span class="sxs-lookup"><span data-stu-id="abe74-1011">PRC</span></span> 
- <span data-ttu-id="abe74-1012">National Identification Card
</span><span class="sxs-lookup"><span data-stu-id="abe74-1012">National Identification Card</span></span> 
- <span data-ttu-id="abe74-1013">身份证 </span><span class="sxs-lookup"><span data-stu-id="abe74-1013">身份证</span></span> 
- <span data-ttu-id="abe74-1014">居民 身份证 </span><span class="sxs-lookup"><span data-stu-id="abe74-1014">居民 身份证</span></span> 
- <span data-ttu-id="abe74-1015">居民身份证
</span><span class="sxs-lookup"><span data-stu-id="abe74-1015">居民身份证</span></span> 
- <span data-ttu-id="abe74-1016">鉴定

</span><span class="sxs-lookup"><span data-stu-id="abe74-1016">鉴定</span></span> 
- <span data-ttu-id="abe74-1017">身分證 </span><span class="sxs-lookup"><span data-stu-id="abe74-1017">身分證</span></span> 
- <span data-ttu-id="abe74-1018">居民 身份證</span><span class="sxs-lookup"><span data-stu-id="abe74-1018">居民 身份證</span></span>
- <span data-ttu-id="abe74-1019">鑑定 </span><span class="sxs-lookup"><span data-stu-id="abe74-1019">鑑定</span></span> 
   
## <a name="credit-card-number"></a><span data-ttu-id="abe74-1020">Numéro de carte de crédit</span><span class="sxs-lookup"><span data-stu-id="abe74-1020">Credit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-1021">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-1021">Format</span></span>

<span data-ttu-id="abe74-1022">16 chiffres qui peuvent être mis en forme ou non mis en forme (dddddddddddddddd) et doit réussir le test Luhn.</span><span class="sxs-lookup"><span data-stu-id="abe74-1022">16 digits which can be formatted or unformatted (dddddddddddddddd) and must pass the Luhn test.</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-1023">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-1023">Pattern</span></span>

<span data-ttu-id="abe74-1024">Modèle très complexe et puissant qui détecte les cartes de visite de toutes les principales marques du monde, notamment Visa, MasterCard, Discover Card, JCB, American Express, etc.</span><span class="sxs-lookup"><span data-stu-id="abe74-1024">Very complex and robust pattern that detects cards from all major brands worldwide, including Visa, MasterCard, Discover Card, JCB, American Express, gift cards, and diner cards.</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-1025">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-1025">Checksum</span></span>

<span data-ttu-id="abe74-1026">Oui, la somme de contrôle de Luhn</span><span class="sxs-lookup"><span data-stu-id="abe74-1026">Yes, the Luhn checksum</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-1027">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-1027">Definition</span></span>

<span data-ttu-id="abe74-1028">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-1028">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-1029">La fonction Func_credit_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-1029">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-1030">L’une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="abe74-1030">One of the following is true:</span></span>
    - <span data-ttu-id="abe74-1031">Un mot clé figurant dans la liste Keyword_cc_verification est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-1031">A keyword from Keyword_cc_verification is found.</span></span>
    - <span data-ttu-id="abe74-1032">Un mot clé figurant dans la liste Keyword_cc_name est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-1032">A keyword from Keyword_cc_name is found.</span></span>
    - <span data-ttu-id="abe74-1033">La fonction Func_expiration_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="abe74-1033">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="abe74-1034">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-1034">The checksum passes.</span></span>

<span data-ttu-id="abe74-1035">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-1035">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-1036">La fonction Func_credit_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-1036">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-1037">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-1037">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-1038">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-1038">Keywords</span></span>

#### <a name="keywordccverification"></a><span data-ttu-id="abe74-1039">Keyword_cc_verification</span><span class="sxs-lookup"><span data-stu-id="abe74-1039">Keyword_cc_verification</span></span>

- <span data-ttu-id="abe74-1040">vérification de la carte</span><span class="sxs-lookup"><span data-stu-id="abe74-1040">card verification</span></span>
- <span data-ttu-id="abe74-1041">numéro d’identification de la carte</span><span class="sxs-lookup"><span data-stu-id="abe74-1041">card identification number</span></span>
- <span data-ttu-id="abe74-1042">nvc
</span><span class="sxs-lookup"><span data-stu-id="abe74-1042">cvn</span></span>
- <span data-ttu-id="abe74-1043">nic
</span><span class="sxs-lookup"><span data-stu-id="abe74-1043">cid</span></span>
- <span data-ttu-id="abe74-1044">CVC2</span><span class="sxs-lookup"><span data-stu-id="abe74-1044">cvc2</span></span>
- <span data-ttu-id="abe74-1045">VVC2</span><span class="sxs-lookup"><span data-stu-id="abe74-1045">cvv2</span></span>
- <span data-ttu-id="abe74-1046">pin block
</span><span class="sxs-lookup"><span data-stu-id="abe74-1046">pin block</span></span>
- <span data-ttu-id="abe74-1047">code de sécurité
</span><span class="sxs-lookup"><span data-stu-id="abe74-1047">security code</span></span>
- <span data-ttu-id="abe74-1048">numéro de sécurité
</span><span class="sxs-lookup"><span data-stu-id="abe74-1048">security number</span></span>
- <span data-ttu-id="abe74-1049">n° de sécurité
</span><span class="sxs-lookup"><span data-stu-id="abe74-1049">security no</span></span>
- <span data-ttu-id="abe74-1050">numéro d’émission
</span><span class="sxs-lookup"><span data-stu-id="abe74-1050">issue number</span></span>
- <span data-ttu-id="abe74-1051">n° d’émission
</span><span class="sxs-lookup"><span data-stu-id="abe74-1051">issue no</span></span>
- <span data-ttu-id="abe74-1052">cryptogramme
</span><span class="sxs-lookup"><span data-stu-id="abe74-1052">cryptogramme</span></span>
- <span data-ttu-id="abe74-1053">numéro de sécurité
</span><span class="sxs-lookup"><span data-stu-id="abe74-1053">numéro de sécurité</span></span>
- <span data-ttu-id="abe74-1054">numéro de sécurité
</span><span class="sxs-lookup"><span data-stu-id="abe74-1054">numero de securite</span></span>
- <span data-ttu-id="abe74-1055">kreditkartenprüfnummer
</span><span class="sxs-lookup"><span data-stu-id="abe74-1055">kreditkartenprüfnummer</span></span>
- <span data-ttu-id="abe74-1056">kreditkartenprufnummer
</span><span class="sxs-lookup"><span data-stu-id="abe74-1056">kreditkartenprufnummer</span></span>
- <span data-ttu-id="abe74-1057">prüfziffer
</span><span class="sxs-lookup"><span data-stu-id="abe74-1057">prüfziffer</span></span>
- <span data-ttu-id="abe74-1058">prufziffer
</span><span class="sxs-lookup"><span data-stu-id="abe74-1058">prufziffer</span></span>
- <span data-ttu-id="abe74-1059">sicherheits Kode</span><span class="sxs-lookup"><span data-stu-id="abe74-1059">sicherheits Kode</span></span>
- <span data-ttu-id="abe74-1060">sicherheitscode
</span><span class="sxs-lookup"><span data-stu-id="abe74-1060">sicherheitscode</span></span>
- <span data-ttu-id="abe74-1061">sicherheitsnummer
</span><span class="sxs-lookup"><span data-stu-id="abe74-1061">sicherheitsnummer</span></span>
- <span data-ttu-id="abe74-1062">verfalldatum
</span><span class="sxs-lookup"><span data-stu-id="abe74-1062">verfalldatum</span></span>
- <span data-ttu-id="abe74-1063">codice di verifica
</span><span class="sxs-lookup"><span data-stu-id="abe74-1063">codice di verifica</span></span>
- <span data-ttu-id="abe74-p105">cod. sicurezza
</span><span class="sxs-lookup"><span data-stu-id="abe74-p105">cod. sicurezza</span></span>
- <span data-ttu-id="abe74-1066">remboursement sicurezza</span><span class="sxs-lookup"><span data-stu-id="abe74-1066">cod sicurezza</span></span>
- <span data-ttu-id="abe74-1067">
n autorizzazione</span><span class="sxs-lookup"><span data-stu-id="abe74-1067">n autorizzazione</span></span>
- <span data-ttu-id="abe74-1068">código
</span><span class="sxs-lookup"><span data-stu-id="abe74-1068">código</span></span>
- <span data-ttu-id="abe74-1069">codigo
</span><span class="sxs-lookup"><span data-stu-id="abe74-1069">codigo</span></span>
- <span data-ttu-id="abe74-p106">cod. seg
</span><span class="sxs-lookup"><span data-stu-id="abe74-p106">cod. seg</span></span>
- <span data-ttu-id="abe74-1072">segment de remboursement</span><span class="sxs-lookup"><span data-stu-id="abe74-1072">cod seg</span></span>
- <span data-ttu-id="abe74-1073">código de segurança
</span><span class="sxs-lookup"><span data-stu-id="abe74-1073">código de segurança</span></span>
- <span data-ttu-id="abe74-1074">codigo de seguranca
</span><span class="sxs-lookup"><span data-stu-id="abe74-1074">codigo de seguranca</span></span>
- <span data-ttu-id="abe74-1075">codigo de segurança
</span><span class="sxs-lookup"><span data-stu-id="abe74-1075">codigo de segurança</span></span>
- <span data-ttu-id="abe74-1076">código de seguranca
</span><span class="sxs-lookup"><span data-stu-id="abe74-1076">código de seguranca</span></span>
- <span data-ttu-id="abe74-p107">cód. Segurança
</span><span class="sxs-lookup"><span data-stu-id="abe74-p107">cód. segurança</span></span>
- <span data-ttu-id="abe74-p108">remboursement. CR seguranca. Segurança</span><span class="sxs-lookup"><span data-stu-id="abe74-p108">cod. seguranca cod. segurança</span></span>
- <span data-ttu-id="abe74-p109">cód. seguranca
</span><span class="sxs-lookup"><span data-stu-id="abe74-p109">cód. seguranca</span></span>
- <span data-ttu-id="abe74-1084">cód segurança</span><span class="sxs-lookup"><span data-stu-id="abe74-1084">cód segurança</span></span>
- <span data-ttu-id="abe74-1085">cabillaud seguranca CR segurança</span><span class="sxs-lookup"><span data-stu-id="abe74-1085">cod seguranca cod segurança</span></span>
- <span data-ttu-id="abe74-1086">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="abe74-1086">cód seguranca</span></span>
- <span data-ttu-id="abe74-1087">número de verificação
</span><span class="sxs-lookup"><span data-stu-id="abe74-1087">número de verificação</span></span>
- <span data-ttu-id="abe74-1088">numero de verificacao
</span><span class="sxs-lookup"><span data-stu-id="abe74-1088">numero de verificacao</span></span>
- <span data-ttu-id="abe74-1089">ablauf
</span><span class="sxs-lookup"><span data-stu-id="abe74-1089">ablauf</span></span>
- <span data-ttu-id="abe74-1090">gültig bis
</span><span class="sxs-lookup"><span data-stu-id="abe74-1090">gültig bis</span></span>
- <span data-ttu-id="abe74-1091">gültigkeitsdatum
</span><span class="sxs-lookup"><span data-stu-id="abe74-1091">gültigkeitsdatum</span></span>
- <span data-ttu-id="abe74-1092">gultig bis
</span><span class="sxs-lookup"><span data-stu-id="abe74-1092">gultig bis</span></span>
- <span data-ttu-id="abe74-1093">gultigkeitsdatum
</span><span class="sxs-lookup"><span data-stu-id="abe74-1093">gultigkeitsdatum</span></span>
- <span data-ttu-id="abe74-1094">scadenza
</span><span class="sxs-lookup"><span data-stu-id="abe74-1094">scadenza</span></span>
- <span data-ttu-id="abe74-1095">data scad
</span><span class="sxs-lookup"><span data-stu-id="abe74-1095">data scad</span></span>
- <span data-ttu-id="abe74-1096">fecha de expiracion
</span><span class="sxs-lookup"><span data-stu-id="abe74-1096">fecha de expiracion</span></span>
- <span data-ttu-id="abe74-1097">fecha de venc
</span><span class="sxs-lookup"><span data-stu-id="abe74-1097">fecha de venc</span></span>
- <span data-ttu-id="abe74-1098">vencimiento
</span><span class="sxs-lookup"><span data-stu-id="abe74-1098">vencimiento</span></span>
- <span data-ttu-id="abe74-1099">válido hasta
</span><span class="sxs-lookup"><span data-stu-id="abe74-1099">válido hasta</span></span>
- <span data-ttu-id="abe74-1100">valido hasta
</span><span class="sxs-lookup"><span data-stu-id="abe74-1100">valido hasta</span></span>
- <span data-ttu-id="abe74-1101">vto
</span><span class="sxs-lookup"><span data-stu-id="abe74-1101">vto</span></span>
- <span data-ttu-id="abe74-1102">data de expiração
</span><span class="sxs-lookup"><span data-stu-id="abe74-1102">data de expiração</span></span>
- <span data-ttu-id="abe74-1103">data de expiracao
</span><span class="sxs-lookup"><span data-stu-id="abe74-1103">data de expiracao</span></span>
- <span data-ttu-id="abe74-1104">data em que expira
</span><span class="sxs-lookup"><span data-stu-id="abe74-1104">data em que expira</span></span>
- <span data-ttu-id="abe74-1105">validade
</span><span class="sxs-lookup"><span data-stu-id="abe74-1105">validade</span></span>
- <span data-ttu-id="abe74-1106">valor
</span><span class="sxs-lookup"><span data-stu-id="abe74-1106">valor</span></span>
- <span data-ttu-id="abe74-1107">vencimento
</span><span class="sxs-lookup"><span data-stu-id="abe74-1107">vencimento</span></span>
- <span data-ttu-id="abe74-1108">Venc</span><span class="sxs-lookup"><span data-stu-id="abe74-1108">Venc</span></span> 

#### <a name="keywordccname"></a><span data-ttu-id="abe74-1109">Keyword_cc_name</span><span class="sxs-lookup"><span data-stu-id="abe74-1109">Keyword_cc_name</span></span>

- <span data-ttu-id="abe74-1110">amex</span><span class="sxs-lookup"><span data-stu-id="abe74-1110">amex</span></span>
- <span data-ttu-id="abe74-1111">
american express</span><span class="sxs-lookup"><span data-stu-id="abe74-1111">american express</span></span>
- <span data-ttu-id="abe74-1112">americanexpress
</span><span class="sxs-lookup"><span data-stu-id="abe74-1112">americanexpress</span></span>
- <span data-ttu-id="abe74-1113">Visa</span><span class="sxs-lookup"><span data-stu-id="abe74-1113">Visa</span></span>
- <span data-ttu-id="abe74-1114">mastercard
</span><span class="sxs-lookup"><span data-stu-id="abe74-1114">mastercard</span></span>
- <span data-ttu-id="abe74-1115">master card
</span><span class="sxs-lookup"><span data-stu-id="abe74-1115">master card</span></span>
- <span data-ttu-id="abe74-1116">
mc
</span><span class="sxs-lookup"><span data-stu-id="abe74-1116">mc</span></span> 
- <span data-ttu-id="abe74-1117">mastercards</span><span class="sxs-lookup"><span data-stu-id="abe74-1117">mastercards</span></span>
- <span data-ttu-id="abe74-1118">
master cards</span><span class="sxs-lookup"><span data-stu-id="abe74-1118">master cards</span></span>
- <span data-ttu-id="abe74-1119">Club de dîner</span><span class="sxs-lookup"><span data-stu-id="abe74-1119">diner's Club</span></span>
- <span data-ttu-id="abe74-1120">diners club
</span><span class="sxs-lookup"><span data-stu-id="abe74-1120">diners club</span></span>
- <span data-ttu-id="abe74-1121">dinersclub
</span><span class="sxs-lookup"><span data-stu-id="abe74-1121">dinersclub</span></span>
- <span data-ttu-id="abe74-1122">discover card
</span><span class="sxs-lookup"><span data-stu-id="abe74-1122">discover card</span></span>
- <span data-ttu-id="abe74-1123">discovercard
</span><span class="sxs-lookup"><span data-stu-id="abe74-1123">discovercard</span></span>
- <span data-ttu-id="abe74-1124">discover cards
</span><span class="sxs-lookup"><span data-stu-id="abe74-1124">discover cards</span></span>
- <span data-ttu-id="abe74-1125">JCB</span><span class="sxs-lookup"><span data-stu-id="abe74-1125">JCB</span></span>
- <span data-ttu-id="abe74-1126">japanese card bureau
</span><span class="sxs-lookup"><span data-stu-id="abe74-1126">japanese card bureau</span></span>
- <span data-ttu-id="abe74-1127">carte blanche
</span><span class="sxs-lookup"><span data-stu-id="abe74-1127">carte blanche</span></span>
- <span data-ttu-id="abe74-1128">carteblanche
</span><span class="sxs-lookup"><span data-stu-id="abe74-1128">carteblanche</span></span>
- <span data-ttu-id="abe74-1129">carte de crédit
</span><span class="sxs-lookup"><span data-stu-id="abe74-1129">credit card</span></span>
- <span data-ttu-id="abe74-1130">cc #</span><span class="sxs-lookup"><span data-stu-id="abe74-1130">cc#</span></span>
- <span data-ttu-id="abe74-1131">cc #:</span><span class="sxs-lookup"><span data-stu-id="abe74-1131">cc#:</span></span>
- <span data-ttu-id="abe74-1132">
date d’expiration</span><span class="sxs-lookup"><span data-stu-id="abe74-1132">expiration date</span></span>
- <span data-ttu-id="abe74-1133">date d’exp
</span><span class="sxs-lookup"><span data-stu-id="abe74-1133">exp date</span></span>
- <span data-ttu-id="abe74-1134">
date d’expiration</span><span class="sxs-lookup"><span data-stu-id="abe74-1134">expiry date</span></span>
- <span data-ttu-id="abe74-1135">
date d’expiration</span><span class="sxs-lookup"><span data-stu-id="abe74-1135">date d’expiration</span></span>
- <span data-ttu-id="abe74-1136">
date d’exp</span><span class="sxs-lookup"><span data-stu-id="abe74-1136">date d'exp</span></span>
- <span data-ttu-id="abe74-1137">
date expiration</span><span class="sxs-lookup"><span data-stu-id="abe74-1137">date expiration</span></span>
- <span data-ttu-id="abe74-1138">carte bancaire
</span><span class="sxs-lookup"><span data-stu-id="abe74-1138">bank card</span></span>
- <span data-ttu-id="abe74-1139">
carte bancaire</span><span class="sxs-lookup"><span data-stu-id="abe74-1139">bankcard</span></span>
- <span data-ttu-id="abe74-1140">numéro de carte
</span><span class="sxs-lookup"><span data-stu-id="abe74-1140">card number</span></span>
- <span data-ttu-id="abe74-1141">num de carte
</span><span class="sxs-lookup"><span data-stu-id="abe74-1141">card num</span></span>
- <span data-ttu-id="abe74-1142">numéro de carte
</span><span class="sxs-lookup"><span data-stu-id="abe74-1142">cardnumber</span></span>
- <span data-ttu-id="abe74-1143">numéros de carte
</span><span class="sxs-lookup"><span data-stu-id="abe74-1143">cardnumbers</span></span>
- <span data-ttu-id="abe74-1144">numéros de carte
</span><span class="sxs-lookup"><span data-stu-id="abe74-1144">card numbers</span></span>
- <span data-ttu-id="abe74-1145">carte de crédit
</span><span class="sxs-lookup"><span data-stu-id="abe74-1145">creditcard</span></span>
- <span data-ttu-id="abe74-1146">cartes de crédit
</span><span class="sxs-lookup"><span data-stu-id="abe74-1146">credit cards</span></span>
- <span data-ttu-id="abe74-1147">cartes de crédit
</span><span class="sxs-lookup"><span data-stu-id="abe74-1147">creditcards</span></span>
- <span data-ttu-id="abe74-1148">ncc
</span><span class="sxs-lookup"><span data-stu-id="abe74-1148">ccn</span></span>
- <span data-ttu-id="abe74-1149">titulaire de la carte
</span><span class="sxs-lookup"><span data-stu-id="abe74-1149">card holder</span></span>
- <span data-ttu-id="abe74-1150">titulaire de la carte
</span><span class="sxs-lookup"><span data-stu-id="abe74-1150">cardholder</span></span>
- <span data-ttu-id="abe74-1151">titulaires de la carte
</span><span class="sxs-lookup"><span data-stu-id="abe74-1151">card holders</span></span>
- <span data-ttu-id="abe74-1152">titulaires de la carte
</span><span class="sxs-lookup"><span data-stu-id="abe74-1152">cardholders</span></span>
- <span data-ttu-id="abe74-1153">carte de vérification
</span><span class="sxs-lookup"><span data-stu-id="abe74-1153">check card</span></span>
- <span data-ttu-id="abe74-1154">carte de vérification
</span><span class="sxs-lookup"><span data-stu-id="abe74-1154">checkcard</span></span>
- <span data-ttu-id="abe74-1155">cartes de vérification
</span><span class="sxs-lookup"><span data-stu-id="abe74-1155">check cards</span></span>
- <span data-ttu-id="abe74-1156">cartes de vérification
</span><span class="sxs-lookup"><span data-stu-id="abe74-1156">checkcards</span></span>
- <span data-ttu-id="abe74-1157">carte de débit
</span><span class="sxs-lookup"><span data-stu-id="abe74-1157">debit card</span></span>
- <span data-ttu-id="abe74-1158">carte de débit
</span><span class="sxs-lookup"><span data-stu-id="abe74-1158">debitcard</span></span>
- <span data-ttu-id="abe74-1159">cartes de débit
</span><span class="sxs-lookup"><span data-stu-id="abe74-1159">debit cards</span></span>
- <span data-ttu-id="abe74-1160">cartes de débit
</span><span class="sxs-lookup"><span data-stu-id="abe74-1160">debitcards</span></span>
- <span data-ttu-id="abe74-1161">carte de retrait
</span><span class="sxs-lookup"><span data-stu-id="abe74-1161">atm card</span></span>
- <span data-ttu-id="abe74-1162">carte de retrait
</span><span class="sxs-lookup"><span data-stu-id="abe74-1162">atmcard</span></span>
- <span data-ttu-id="abe74-1163">cartes de retrait
</span><span class="sxs-lookup"><span data-stu-id="abe74-1163">atm cards</span></span>
- <span data-ttu-id="abe74-1164">cartes de retrait
</span><span class="sxs-lookup"><span data-stu-id="abe74-1164">atmcards</span></span>
- <span data-ttu-id="abe74-1165">
enroute</span><span class="sxs-lookup"><span data-stu-id="abe74-1165">enroute</span></span>
- <span data-ttu-id="abe74-1166">
en route</span><span class="sxs-lookup"><span data-stu-id="abe74-1166">en route</span></span>
- <span data-ttu-id="abe74-1167">type de carte
</span><span class="sxs-lookup"><span data-stu-id="abe74-1167">card type</span></span>
- <span data-ttu-id="abe74-1168">carte bancaire
</span><span class="sxs-lookup"><span data-stu-id="abe74-1168">carte bancaire</span></span>
- <span data-ttu-id="abe74-1169">carte de crédit
</span><span class="sxs-lookup"><span data-stu-id="abe74-1169">carte de crédit</span></span>
- <span data-ttu-id="abe74-1170">carte de credit
</span><span class="sxs-lookup"><span data-stu-id="abe74-1170">carte de credit</span></span>
- <span data-ttu-id="abe74-1171">numéro de carte
</span><span class="sxs-lookup"><span data-stu-id="abe74-1171">numéro de carte</span></span>
- <span data-ttu-id="abe74-1172">numero de carte
</span><span class="sxs-lookup"><span data-stu-id="abe74-1172">numero de carte</span></span>
- <span data-ttu-id="abe74-1173">nº de la carte
</span><span class="sxs-lookup"><span data-stu-id="abe74-1173">nº de la carte</span></span>
- <span data-ttu-id="abe74-1174">nº de carte
</span><span class="sxs-lookup"><span data-stu-id="abe74-1174">nº de carte</span></span>
- <span data-ttu-id="abe74-1175">kreditkarte
</span><span class="sxs-lookup"><span data-stu-id="abe74-1175">kreditkarte</span></span>
- <span data-ttu-id="abe74-1176">karte
</span><span class="sxs-lookup"><span data-stu-id="abe74-1176">karte</span></span>
- <span data-ttu-id="abe74-1177">karteninhaber
</span><span class="sxs-lookup"><span data-stu-id="abe74-1177">karteninhaber</span></span>
- <span data-ttu-id="abe74-1178">karteninhabers</span><span class="sxs-lookup"><span data-stu-id="abe74-1178">karteninhabers</span></span>
- <span data-ttu-id="abe74-1179">kreditkarteninhaber
</span><span class="sxs-lookup"><span data-stu-id="abe74-1179">kreditkarteninhaber</span></span>
- <span data-ttu-id="abe74-1180">kreditkarteninstitut
</span><span class="sxs-lookup"><span data-stu-id="abe74-1180">kreditkarteninstitut</span></span>
- <span data-ttu-id="abe74-1181">kreditkartentyp
</span><span class="sxs-lookup"><span data-stu-id="abe74-1181">kreditkartentyp</span></span>
- <span data-ttu-id="abe74-1182">eigentümername
</span><span class="sxs-lookup"><span data-stu-id="abe74-1182">eigentümername</span></span>
- <span data-ttu-id="abe74-1183">
kartennr
</span><span class="sxs-lookup"><span data-stu-id="abe74-1183">kartennr</span></span> 
- <span data-ttu-id="abe74-1184">kartennummer</span><span class="sxs-lookup"><span data-stu-id="abe74-1184">kartennummer</span></span>
- <span data-ttu-id="abe74-1185">
kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="abe74-1185">kreditkartennummer</span></span>
- <span data-ttu-id="abe74-1186">kreditkarten-nummer</span><span class="sxs-lookup"><span data-stu-id="abe74-1186">kreditkarten-nummer</span></span>
- <span data-ttu-id="abe74-1187">Carta di credito
</span><span class="sxs-lookup"><span data-stu-id="abe74-1187">carta di credito</span></span>
- <span data-ttu-id="abe74-1188">Carta credito
</span><span class="sxs-lookup"><span data-stu-id="abe74-1188">carta credito</span></span>
- <span data-ttu-id="abe74-1189">Carta</span><span class="sxs-lookup"><span data-stu-id="abe74-1189">carta</span></span>
- <span data-ttu-id="abe74-1190">carta n</span><span class="sxs-lookup"><span data-stu-id="abe74-1190">n carta</span></span>
- <span data-ttu-id="abe74-p110">nr. carta
</span><span class="sxs-lookup"><span data-stu-id="abe74-p110">nr. carta</span></span>
- <span data-ttu-id="abe74-1193">nr carta</span><span class="sxs-lookup"><span data-stu-id="abe74-1193">nr carta</span></span>
- <span data-ttu-id="abe74-1194">numero carta
</span><span class="sxs-lookup"><span data-stu-id="abe74-1194">numero carta</span></span>
- <span data-ttu-id="abe74-1195">numero della carta
</span><span class="sxs-lookup"><span data-stu-id="abe74-1195">numero della carta</span></span>
- <span data-ttu-id="abe74-1196">numero di carta
</span><span class="sxs-lookup"><span data-stu-id="abe74-1196">numero di carta</span></span>
- <span data-ttu-id="abe74-1197">tarjeta credito
</span><span class="sxs-lookup"><span data-stu-id="abe74-1197">tarjeta credito</span></span>
- <span data-ttu-id="abe74-1198">tarjeta de credito
</span><span class="sxs-lookup"><span data-stu-id="abe74-1198">tarjeta de credito</span></span>
- <span data-ttu-id="abe74-1199">
tarjeta crédito</span><span class="sxs-lookup"><span data-stu-id="abe74-1199">tarjeta crédito</span></span>
- <span data-ttu-id="abe74-1200">
tarjeta de crédito</span><span class="sxs-lookup"><span data-stu-id="abe74-1200">tarjeta de crédito</span></span>
- <span data-ttu-id="abe74-1201">tarjeta de atm
</span><span class="sxs-lookup"><span data-stu-id="abe74-1201">tarjeta de atm</span></span>
- <span data-ttu-id="abe74-1202">tarjeta atm
</span><span class="sxs-lookup"><span data-stu-id="abe74-1202">tarjeta atm</span></span>
- <span data-ttu-id="abe74-1203">tarjeta debito
</span><span class="sxs-lookup"><span data-stu-id="abe74-1203">tarjeta debito</span></span>
- <span data-ttu-id="abe74-1204">tarjeta de debito
</span><span class="sxs-lookup"><span data-stu-id="abe74-1204">tarjeta de debito</span></span>
- <span data-ttu-id="abe74-1205">
tarjeta débito</span><span class="sxs-lookup"><span data-stu-id="abe74-1205">tarjeta débito</span></span>
- <span data-ttu-id="abe74-1206">
tarjeta de débito</span><span class="sxs-lookup"><span data-stu-id="abe74-1206">tarjeta de débito</span></span>
- <span data-ttu-id="abe74-1207">nº de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="abe74-1207">nº de tarjeta</span></span>
- <span data-ttu-id="abe74-p111">no. de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="abe74-p111">no. de tarjeta</span></span>
- <span data-ttu-id="abe74-1210">Aucun tarjeta de</span><span class="sxs-lookup"><span data-stu-id="abe74-1210">no de tarjeta</span></span>
- <span data-ttu-id="abe74-1211">numero de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="abe74-1211">numero de tarjeta</span></span>
- <span data-ttu-id="abe74-1212">número de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="abe74-1212">número de tarjeta</span></span>
- <span data-ttu-id="abe74-1213">tarjeta no
</span><span class="sxs-lookup"><span data-stu-id="abe74-1213">tarjeta no</span></span>
- <span data-ttu-id="abe74-1214">tarjetahabiente
</span><span class="sxs-lookup"><span data-stu-id="abe74-1214">tarjetahabiente</span></span>
- <span data-ttu-id="abe74-1215">cartão de crédito
</span><span class="sxs-lookup"><span data-stu-id="abe74-1215">cartão de crédito</span></span>
- <span data-ttu-id="abe74-1216">cartão de credito
</span><span class="sxs-lookup"><span data-stu-id="abe74-1216">cartão de credito</span></span>
- <span data-ttu-id="abe74-1217">cartao de crédito
</span><span class="sxs-lookup"><span data-stu-id="abe74-1217">cartao de crédito</span></span>
- <span data-ttu-id="abe74-1218">cartao de credito
</span><span class="sxs-lookup"><span data-stu-id="abe74-1218">cartao de credito</span></span>
- <span data-ttu-id="abe74-1219">cartão de débito
</span><span class="sxs-lookup"><span data-stu-id="abe74-1219">cartão de débito</span></span>
- <span data-ttu-id="abe74-1220">cartao de débito
</span><span class="sxs-lookup"><span data-stu-id="abe74-1220">cartao de débito</span></span>
- <span data-ttu-id="abe74-1221">cartão de debito
</span><span class="sxs-lookup"><span data-stu-id="abe74-1221">cartão de debito</span></span>
- <span data-ttu-id="abe74-1222">cartao de debito
</span><span class="sxs-lookup"><span data-stu-id="abe74-1222">cartao de debito</span></span>
- <span data-ttu-id="abe74-1223">débito automático</span><span class="sxs-lookup"><span data-stu-id="abe74-1223">débito automático</span></span>
- <span data-ttu-id="abe74-1224">debito automatico
</span><span class="sxs-lookup"><span data-stu-id="abe74-1224">debito automatico</span></span>
- <span data-ttu-id="abe74-1225">
número do cartão</span><span class="sxs-lookup"><span data-stu-id="abe74-1225">número do cartão</span></span>
- <span data-ttu-id="abe74-1226">
numero do cartão
</span><span class="sxs-lookup"><span data-stu-id="abe74-1226">numero do cartão</span></span> 
- <span data-ttu-id="abe74-1227">número do cartao</span><span class="sxs-lookup"><span data-stu-id="abe74-1227">número do cartao</span></span>
- <span data-ttu-id="abe74-1228">
numero do cartao</span><span class="sxs-lookup"><span data-stu-id="abe74-1228">numero do cartao</span></span>
- <span data-ttu-id="abe74-1229">número de cartão
</span><span class="sxs-lookup"><span data-stu-id="abe74-1229">número de cartão</span></span>
- <span data-ttu-id="abe74-1230">numero de cartão
</span><span class="sxs-lookup"><span data-stu-id="abe74-1230">numero de cartão</span></span>
- <span data-ttu-id="abe74-1231">número de cartao
</span><span class="sxs-lookup"><span data-stu-id="abe74-1231">número de cartao</span></span>
- <span data-ttu-id="abe74-1232">numero de cartao
</span><span class="sxs-lookup"><span data-stu-id="abe74-1232">numero de cartao</span></span>
- <span data-ttu-id="abe74-1233">Nº cartão</span><span class="sxs-lookup"><span data-stu-id="abe74-1233">nº do cartão</span></span>
- <span data-ttu-id="abe74-1234">nº do cartao
</span><span class="sxs-lookup"><span data-stu-id="abe74-1234">nº do cartao</span></span>
- <span data-ttu-id="abe74-p112">nº. do cartão
</span><span class="sxs-lookup"><span data-stu-id="abe74-p112">nº. do cartão</span></span>
- <span data-ttu-id="abe74-1237">Aucun cartão</span><span class="sxs-lookup"><span data-stu-id="abe74-1237">no do cartão</span></span>
- <span data-ttu-id="abe74-1238">Aucun cartao</span><span class="sxs-lookup"><span data-stu-id="abe74-1238">no do cartao</span></span>
- <span data-ttu-id="abe74-p113">no. do cartão
</span><span class="sxs-lookup"><span data-stu-id="abe74-p113">no. do cartão</span></span>
- <span data-ttu-id="abe74-p114">
no. do cartao
</span><span class="sxs-lookup"><span data-stu-id="abe74-p114">no. do cartao</span></span> 
   
## <a name="croatia-identity-card-number"></a><span data-ttu-id="abe74-1243">Numéro de carte d’identité croate</span><span class="sxs-lookup"><span data-stu-id="abe74-1243">Croatia Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-1244">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-1244">Format</span></span>

<span data-ttu-id="abe74-1245">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-1245">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-1246">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-1246">Pattern</span></span>

<span data-ttu-id="abe74-1247">Neuf chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="abe74-1247">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-1248">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-1248">Checksum</span></span>

<span data-ttu-id="abe74-1249">Non</span><span class="sxs-lookup"><span data-stu-id="abe74-1249">No</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-1250">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-1250">Definition</span></span>

<span data-ttu-id="abe74-1251">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-1251">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-1252">La fonction Func_croatia_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-1252">The function Func_croatia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-1253">Un mot clé figurant dans la liste Keyword_croatia_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-1253">A keyword from Keyword_croatia_id_card is found.</span></span>

```
<!--Croatia Identity Card Number-->
<Entity id="ff12f884-c20a-4189-b185-34c8e7258d47" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_croatia_id_card"/>
     <Match idRef="Keyword_croatia_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe74-1254">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-1254">Keywords</span></span>

#### <a name="keywordcroatiaidcard"></a><span data-ttu-id="abe74-1255">Keyword_croatia_id_card</span><span class="sxs-lookup"><span data-stu-id="abe74-1255">Keyword_croatia_id_card</span></span>

- <span data-ttu-id="abe74-1256">Croatian identity card</span><span class="sxs-lookup"><span data-stu-id="abe74-1256">Croatian identity card</span></span>
- <span data-ttu-id="abe74-1257">Osobna iskaznica</span><span class="sxs-lookup"><span data-stu-id="abe74-1257">Osobna iskaznica</span></span>

   
## <a name="croatia-personal-identification-oib-number"></a><span data-ttu-id="abe74-1258">	Numéro d’identification personnel (OIB) Croatie</span><span class="sxs-lookup"><span data-stu-id="abe74-1258">Croatia Personal Identification (OIB) Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-1259">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-1259">Format</span></span>

<span data-ttu-id="abe74-1260">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-1260">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-1261">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-1261">Pattern</span></span>

<span data-ttu-id="abe74-1262">10 chiffres :</span><span class="sxs-lookup"><span data-stu-id="abe74-1262">10 digits:</span></span>
- <span data-ttu-id="abe74-1263">Six chiffres sous la forme JJMMAA qui correspondent à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="abe74-1263">Six digits in the form DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="abe74-1264">Quatre chiffres où le dernier chiffre est un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-1264">Four digits where the final digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-1265">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-1265">Checksum</span></span>

<span data-ttu-id="abe74-1266">Oui</span><span class="sxs-lookup"><span data-stu-id="abe74-1266">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-1267">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-1267">Definition</span></span>

<span data-ttu-id="abe74-1268">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-1268">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-1269">La fonction Func_croatia_oib_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-1269">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-1270">Un mot clé figurant dans la liste Keyword_croatia_oib_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-1270">A keyword from Keyword_croatia_oib_number is found.</span></span>
- <span data-ttu-id="abe74-1271">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-1271">The checksum passes.</span></span>

<span data-ttu-id="abe74-1272">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-1272">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-1273">La fonction Func_croatia_oib_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-1273">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-1274">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-1274">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-1275">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-1275">Keywords</span></span>

#### <a name="keywordcroatiaoibnumber"></a><span data-ttu-id="abe74-1276">Keyword_croatia_oib_number</span><span class="sxs-lookup"><span data-stu-id="abe74-1276">Keyword_croatia_oib_number</span></span>

- <span data-ttu-id="abe74-1277">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="abe74-1277">Personal Identification Number</span></span>
- <span data-ttu-id="abe74-1278">Osobni identifikacijski broj
</span><span class="sxs-lookup"><span data-stu-id="abe74-1278">Osobni identifikacijski broj</span></span> 
- <span data-ttu-id="abe74-1279">OIB
</span><span class="sxs-lookup"><span data-stu-id="abe74-1279">OIB</span></span> 

   
## <a name="czech-national-identity-card-number"></a><span data-ttu-id="abe74-1280">Numéro de carte d’identité nationale tchèque</span><span class="sxs-lookup"><span data-stu-id="abe74-1280">Czech National Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-1281">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-1281">Format</span></span>

<span data-ttu-id="abe74-1282">10 chiffres contenant une barre oblique</span><span class="sxs-lookup"><span data-stu-id="abe74-1282">10 digits containing a forward slash</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-1283">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-1283">Pattern</span></span>

<span data-ttu-id="abe74-1284">10 chiffres :</span><span class="sxs-lookup"><span data-stu-id="abe74-1284">10 digits:</span></span>
- <span data-ttu-id="abe74-1285">Six chiffres correspondant à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="abe74-1285">Six digits which are the date of birth</span></span> 
- <span data-ttu-id="abe74-1286">Une barre oblique </span><span class="sxs-lookup"><span data-stu-id="abe74-1286">A forward slash</span></span> 
- <span data-ttu-id="abe74-1287">Quatre chiffres où le dernier chiffre est un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-1287">Four digits where the final digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-1288">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-1288">Checksum</span></span>

<span data-ttu-id="abe74-1289">Oui</span><span class="sxs-lookup"><span data-stu-id="abe74-1289">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-1290">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-1290">Definition</span></span>

<span data-ttu-id="abe74-p115">Une stratégie DLP est de 85 % convaincu que ce type d’informations sensibles a été détecté if, au sein d’une proximité de 300 caractères : la fonction Func_czech_id_card recherche le contenu qui correspond au modèle. Un mot clé à partir de Keyword_czech_id_card est trouvé. Passe de la somme de contrôle.</span><span class="sxs-lookup"><span data-stu-id="abe74-p115">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_czech_id_card finds content that matches the pattern. A keyword from Keyword_czech_id_card is found. The checksum passes.</span></span>

```
<!-- Czech National Identity Card Number -->
<Entity id="60c0725a-4eb6-455b-9dda-05d8a7396497" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_czech_id_card"/>
     <Match idRef="Keyword_czech_id_card"/>
  </Pattern>
</Entity>
```


### <a name="keywords"></a><span data-ttu-id="abe74-1294">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-1294">Keywords</span></span>

- <span data-ttu-id="abe74-1295">Keyword_czech_id_card</span><span class="sxs-lookup"><span data-stu-id="abe74-1295">Keyword_czech_id_card</span></span>
- <span data-ttu-id="abe74-1296">Czech national identity card</span><span class="sxs-lookup"><span data-stu-id="abe74-1296">Czech national identity card</span></span>
- <span data-ttu-id="abe74-1297">Občanský průka</span><span class="sxs-lookup"><span data-stu-id="abe74-1297">Občanský průka</span></span>
   
## <a name="denmark-personal-identification-number"></a><span data-ttu-id="abe74-1298">	Numéro d’identification personnel Danemark</span><span class="sxs-lookup"><span data-stu-id="abe74-1298">Denmark Personal Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-1299">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-1299">Format</span></span>

<span data-ttu-id="abe74-1300">10 chiffres contenant un trait d’union</span><span class="sxs-lookup"><span data-stu-id="abe74-1300">10 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-1301">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-1301">Pattern</span></span>

<span data-ttu-id="abe74-1302">10 chiffres :</span><span class="sxs-lookup"><span data-stu-id="abe74-1302">10 digits:</span></span>
- <span data-ttu-id="abe74-1303">Six chiffres au format JJMMAA qui correspondent à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="abe74-1303">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="abe74-1304">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="abe74-1304">A hyphen</span></span> 
- <span data-ttu-id="abe74-1305">Quatre chiffres où le dernier chiffre est un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-1305">Four digits where the final digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-1306">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-1306">Checksum</span></span>

<span data-ttu-id="abe74-1307">Oui</span><span class="sxs-lookup"><span data-stu-id="abe74-1307">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-1308">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-1308">Definition</span></span>

<span data-ttu-id="abe74-p116">Une stratégie DLP est convaincu que ce type d’informations sensibles a été détecté à 75 % if, au sein d’une proximité de 300 caractères : l’expression régulière Regex_denmark_id recherche de contenu qui correspond au modèle. Un mot clé à partir de Keyword_denmark_id est trouvé. Passe de la somme de contrôle.</span><span class="sxs-lookup"><span data-stu-id="abe74-p116">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_denmark_id finds content that matches the pattern. A keyword from Keyword_denmark_id is found. The checksum passes.</span></span>

```
<!-- Denmark Personal Identification Number -->
<Entity id="6c4f2fef-56e1-4c00-8093-88d7a01cf460" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_denmark_id"/>
     <Match idRef="Keyword_denmark_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe74-1312">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-1312">Keywords</span></span>

#### <a name="keyworddenmarkid"></a><span data-ttu-id="abe74-1313">Keyword_denmark_id</span><span class="sxs-lookup"><span data-stu-id="abe74-1313">Keyword_denmark_id</span></span>

- <span data-ttu-id="abe74-1314">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="abe74-1314">Personal Identification Number</span></span>
- <span data-ttu-id="abe74-1315">CPR</span><span class="sxs-lookup"><span data-stu-id="abe74-1315">CPR</span></span>
- <span data-ttu-id="abe74-1316">Det Centrale Personregister</span><span class="sxs-lookup"><span data-stu-id="abe74-1316">Det Centrale Personregister</span></span>
- <span data-ttu-id="abe74-1317">Personnummer</span><span class="sxs-lookup"><span data-stu-id="abe74-1317">Personnummer</span></span>
   
## <a name="drug-enforcement-agency-dea-number"></a><span data-ttu-id="abe74-1318">Numéro de la Drug Enforcement Agency (DEA)</span><span class="sxs-lookup"><span data-stu-id="abe74-1318">Drug Enforcement Agency (DEA) Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-1319">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-1319">Format</span></span>

<span data-ttu-id="abe74-1320">Deux lettres suivies de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-1320">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-1321">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-1321">Pattern</span></span>

<span data-ttu-id="abe74-1322">Le modèle doit inclure tous les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="abe74-1322">Pattern must include all of the following:</span></span>
- <span data-ttu-id="abe74-1323">Une lettre (ne respecte pas la casse) à partir de cet ensemble de lettres possibles : abcdefghjklmnprstux, qui est un code d’utilisateur enregistré</span><span class="sxs-lookup"><span data-stu-id="abe74-1323">One letter (not case sensitive) from this set of possible letters: abcdefghjklmnprstux, which is a registrant code</span></span> 
- <span data-ttu-id="abe74-1324">Une lettre (ne respecte pas la casse), qui est la première lettre du nom de l’utilisateur enregistré</span><span class="sxs-lookup"><span data-stu-id="abe74-1324">One letter (not case sensitive), which is the first letter of the registrant's last name</span></span> 
- <span data-ttu-id="abe74-1325">Sept chiffres, le dernier est le chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-1325">Seven digits, the last of which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-1326">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-1326">Checksum</span></span>

<span data-ttu-id="abe74-1327">Oui</span><span class="sxs-lookup"><span data-stu-id="abe74-1327">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-1328">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-1328">Definition</span></span>

<span data-ttu-id="abe74-1329">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-1329">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-1330">La fonction Func_dea_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-1330">The function Func_dea_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-1331">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-1331">The checksum passes.</span></span>

```
<!-- DEA Number -->
<Entity id="9a5445ad-406e-43eb-8bd7-cac17ab6d0e4" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_dea_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe74-1332">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-1332">Keywords</span></span>

<span data-ttu-id="abe74-1333">Aucun</span><span class="sxs-lookup"><span data-stu-id="abe74-1333">None</span></span>

   
## <a name="eu-debit-card-number"></a><span data-ttu-id="abe74-1334">Numéro de carte de débit Union européenne</span><span class="sxs-lookup"><span data-stu-id="abe74-1334">EU Debit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-1335">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-1335">Format</span></span>

<span data-ttu-id="abe74-1336">16 chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-1336">16 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-1337">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-1337">Pattern</span></span>

<span data-ttu-id="abe74-1338">Modèle très complexe et puissant</span><span class="sxs-lookup"><span data-stu-id="abe74-1338">Very complex and robust pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-1339">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-1339">Checksum</span></span>

<span data-ttu-id="abe74-1340">Oui</span><span class="sxs-lookup"><span data-stu-id="abe74-1340">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-1341">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-1341">Definition</span></span>

<span data-ttu-id="abe74-1342">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-1342">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-1343">La fonction Func_eu_debit_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-1343">The function Func_eu_debit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-1344">Au moins une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="abe74-1344">At least one of the following is true:</span></span>
    - <span data-ttu-id="abe74-1345">Un mot clé figurant dans la liste Keyword_eu_debit_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-1345">A keyword from Keyword_eu_debit_card is found.</span></span>
    - <span data-ttu-id="abe74-1346">Un mot clé figurant dans la liste Keyword_card_terms_dict est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-1346">A keyword from Keyword_card_terms_dict is found.</span></span>
    - <span data-ttu-id="abe74-1347">Un mot clé figurant dans la liste Keyword_card_security_terms_dict est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-1347">A keyword from Keyword_card_security_terms_dict is found.</span></span>
    - <span data-ttu-id="abe74-1348">Un mot clé figurant dans la liste Keyword_card_expiration_terms_dict est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-1348">A keyword from Keyword_card_expiration_terms_dict is found.</span></span>
    - <span data-ttu-id="abe74-1349">La fonction Func_expiration_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="abe74-1349">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="abe74-1350">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-1350">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-1351">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-1351">Keywords</span></span>

#### <a name="keywordeudebitcard"></a><span data-ttu-id="abe74-1352">Keyword_eu_debit_card</span><span class="sxs-lookup"><span data-stu-id="abe74-1352">Keyword_eu_debit_card</span></span>

- <span data-ttu-id="abe74-1353">numéro de compte</span><span class="sxs-lookup"><span data-stu-id="abe74-1353">account number</span></span> 
- <span data-ttu-id="abe74-1354">numéro de carte
</span><span class="sxs-lookup"><span data-stu-id="abe74-1354">card number</span></span> 
- <span data-ttu-id="abe74-1355">n° carte
</span><span class="sxs-lookup"><span data-stu-id="abe74-1355">card no.</span></span> 
- <span data-ttu-id="abe74-1356">numéro de sécurité
</span><span class="sxs-lookup"><span data-stu-id="abe74-1356">security number</span></span> 
- <span data-ttu-id="abe74-1357">cc #</span><span class="sxs-lookup"><span data-stu-id="abe74-1357">cc#</span></span> 

#### <a name="keywordcardtermsdict"></a><span data-ttu-id="abe74-1358">Keyword_card_terms_dict</span><span class="sxs-lookup"><span data-stu-id="abe74-1358">Keyword_card_terms_dict</span></span>

- <span data-ttu-id="abe74-1359">num de compte
</span><span class="sxs-lookup"><span data-stu-id="abe74-1359">acct nbr</span></span> 
- <span data-ttu-id="abe74-1360">num de compte
</span><span class="sxs-lookup"><span data-stu-id="abe74-1360">acct num</span></span> 
- <span data-ttu-id="abe74-1361">n° compte
</span><span class="sxs-lookup"><span data-stu-id="abe74-1361">acct no</span></span> 
- <span data-ttu-id="abe74-1362">american express
</span><span class="sxs-lookup"><span data-stu-id="abe74-1362">american express</span></span> 
- <span data-ttu-id="abe74-1363">americanexpress
</span><span class="sxs-lookup"><span data-stu-id="abe74-1363">americanexpress</span></span> 
- <span data-ttu-id="abe74-1364">americano espresso
</span><span class="sxs-lookup"><span data-stu-id="abe74-1364">americano espresso</span></span> 
- <span data-ttu-id="abe74-1365">amex</span><span class="sxs-lookup"><span data-stu-id="abe74-1365">amex</span></span> 
- <span data-ttu-id="abe74-1366">carte de retrait
</span><span class="sxs-lookup"><span data-stu-id="abe74-1366">atm card</span></span> 
- <span data-ttu-id="abe74-1367">cartes de retrait
</span><span class="sxs-lookup"><span data-stu-id="abe74-1367">atm cards</span></span> 
- <span data-ttu-id="abe74-1368">atm kaart
</span><span class="sxs-lookup"><span data-stu-id="abe74-1368">atm kaart</span></span> 
- <span data-ttu-id="abe74-1369">carte de retrait
</span><span class="sxs-lookup"><span data-stu-id="abe74-1369">atmcard</span></span> 
- <span data-ttu-id="abe74-1370">cartes de retrait
</span><span class="sxs-lookup"><span data-stu-id="abe74-1370">atmcards</span></span> 
- <span data-ttu-id="abe74-1371">atmkaart
</span><span class="sxs-lookup"><span data-stu-id="abe74-1371">atmkaart</span></span> 
- <span data-ttu-id="abe74-1372">atmkaarten
</span><span class="sxs-lookup"><span data-stu-id="abe74-1372">atmkaarten</span></span> 
- <span data-ttu-id="abe74-1373">bancontact
</span><span class="sxs-lookup"><span data-stu-id="abe74-1373">bancontact</span></span> 
- <span data-ttu-id="abe74-1374">carte bancaire
</span><span class="sxs-lookup"><span data-stu-id="abe74-1374">bank card</span></span> 
- <span data-ttu-id="abe74-1375">bankkaart
</span><span class="sxs-lookup"><span data-stu-id="abe74-1375">bankkaart</span></span> 
- <span data-ttu-id="abe74-1376">titulaire de la carte
</span><span class="sxs-lookup"><span data-stu-id="abe74-1376">card holder</span></span> 
- <span data-ttu-id="abe74-1377">titulaires de la carte
</span><span class="sxs-lookup"><span data-stu-id="abe74-1377">card holders</span></span> 
- <span data-ttu-id="abe74-1378">num de carte
</span><span class="sxs-lookup"><span data-stu-id="abe74-1378">card num</span></span> 
- <span data-ttu-id="abe74-1379">numéro de carte
</span><span class="sxs-lookup"><span data-stu-id="abe74-1379">card number</span></span> 
- <span data-ttu-id="abe74-1380">numéros de carte
</span><span class="sxs-lookup"><span data-stu-id="abe74-1380">card numbers</span></span> 
- <span data-ttu-id="abe74-1381">type de carte
</span><span class="sxs-lookup"><span data-stu-id="abe74-1381">card type</span></span> 
- <span data-ttu-id="abe74-1382">cardano numerico
</span><span class="sxs-lookup"><span data-stu-id="abe74-1382">cardano numerico</span></span> 
- <span data-ttu-id="abe74-1383">titulaire de la carte
</span><span class="sxs-lookup"><span data-stu-id="abe74-1383">cardholder</span></span> 
- <span data-ttu-id="abe74-1384">titulaires de la carte
</span><span class="sxs-lookup"><span data-stu-id="abe74-1384">cardholders</span></span> 
- <span data-ttu-id="abe74-1385">numéro de carte
</span><span class="sxs-lookup"><span data-stu-id="abe74-1385">cardnumber</span></span> 
- <span data-ttu-id="abe74-1386">numéros de carte
</span><span class="sxs-lookup"><span data-stu-id="abe74-1386">cardnumbers</span></span> 
- <span data-ttu-id="abe74-1387">carta bianca
</span><span class="sxs-lookup"><span data-stu-id="abe74-1387">carta bianca</span></span> 
- <span data-ttu-id="abe74-1388">Carta credito
</span><span class="sxs-lookup"><span data-stu-id="abe74-1388">carta credito</span></span> 
- <span data-ttu-id="abe74-1389">Carta di credito
</span><span class="sxs-lookup"><span data-stu-id="abe74-1389">carta di credito</span></span> 
- <span data-ttu-id="abe74-1390">cartao de credito
</span><span class="sxs-lookup"><span data-stu-id="abe74-1390">cartao de credito</span></span> 
- <span data-ttu-id="abe74-1391">cartao de crédito
</span><span class="sxs-lookup"><span data-stu-id="abe74-1391">cartao de crédito</span></span> 
- <span data-ttu-id="abe74-1392">cartao de debito
</span><span class="sxs-lookup"><span data-stu-id="abe74-1392">cartao de debito</span></span> 
- <span data-ttu-id="abe74-1393">cartao de débito
</span><span class="sxs-lookup"><span data-stu-id="abe74-1393">cartao de débito</span></span> 
- <span data-ttu-id="abe74-1394">carte bancaire
</span><span class="sxs-lookup"><span data-stu-id="abe74-1394">carte bancaire</span></span> 
- <span data-ttu-id="abe74-1395">carte blanche
</span><span class="sxs-lookup"><span data-stu-id="abe74-1395">carte blanche</span></span> 
- <span data-ttu-id="abe74-1396">carte bleue
</span><span class="sxs-lookup"><span data-stu-id="abe74-1396">carte bleue</span></span> 
- <span data-ttu-id="abe74-1397">carte de credit
</span><span class="sxs-lookup"><span data-stu-id="abe74-1397">carte de credit</span></span> 
- <span data-ttu-id="abe74-1398">carte de crédit
</span><span class="sxs-lookup"><span data-stu-id="abe74-1398">carte de crédit</span></span> 
- <span data-ttu-id="abe74-1399">carte di credito
</span><span class="sxs-lookup"><span data-stu-id="abe74-1399">carte di credito</span></span> 
- <span data-ttu-id="abe74-1400">carteblanche
</span><span class="sxs-lookup"><span data-stu-id="abe74-1400">carteblanche</span></span> 
- <span data-ttu-id="abe74-1401">cartão de credito
</span><span class="sxs-lookup"><span data-stu-id="abe74-1401">cartão de credito</span></span> 
- <span data-ttu-id="abe74-1402">cartão de crédito
</span><span class="sxs-lookup"><span data-stu-id="abe74-1402">cartão de crédito</span></span> 
- <span data-ttu-id="abe74-1403">cartão de debito
</span><span class="sxs-lookup"><span data-stu-id="abe74-1403">cartão de debito</span></span> 
- <span data-ttu-id="abe74-1404">cartão de débito
</span><span class="sxs-lookup"><span data-stu-id="abe74-1404">cartão de débito</span></span> 
- <span data-ttu-id="abe74-1405">cb
</span><span class="sxs-lookup"><span data-stu-id="abe74-1405">cb</span></span> 
- <span data-ttu-id="abe74-1406">ncc
</span><span class="sxs-lookup"><span data-stu-id="abe74-1406">ccn</span></span> 
- <span data-ttu-id="abe74-1407">carte de vérification
</span><span class="sxs-lookup"><span data-stu-id="abe74-1407">check card</span></span> 
- <span data-ttu-id="abe74-1408">cartes de vérification
</span><span class="sxs-lookup"><span data-stu-id="abe74-1408">check cards</span></span> 
- <span data-ttu-id="abe74-1409">carte de vérification
</span><span class="sxs-lookup"><span data-stu-id="abe74-1409">checkcard</span></span>
- <span data-ttu-id="abe74-1410">cartes de vérification
</span><span class="sxs-lookup"><span data-stu-id="abe74-1410">checkcards</span></span> 
- <span data-ttu-id="abe74-1411">chequekaart
</span><span class="sxs-lookup"><span data-stu-id="abe74-1411">chequekaart</span></span> 
- <span data-ttu-id="abe74-1412">cirrus
</span><span class="sxs-lookup"><span data-stu-id="abe74-1412">cirrus</span></span> 
- <span data-ttu-id="abe74-1413">cirrus-edc-maestro
</span><span class="sxs-lookup"><span data-stu-id="abe74-1413">cirrus-edc-maestro</span></span> 
- <span data-ttu-id="abe74-1414">controlekaart
</span><span class="sxs-lookup"><span data-stu-id="abe74-1414">controlekaart</span></span> 
- <span data-ttu-id="abe74-1415">controlekaarten
</span><span class="sxs-lookup"><span data-stu-id="abe74-1415">controlekaarten</span></span> 
- <span data-ttu-id="abe74-1416">carte de crédit
</span><span class="sxs-lookup"><span data-stu-id="abe74-1416">credit card</span></span> 
- <span data-ttu-id="abe74-1417">cartes de crédit
</span><span class="sxs-lookup"><span data-stu-id="abe74-1417">credit cards</span></span> 
- <span data-ttu-id="abe74-1418">carte de crédit
</span><span class="sxs-lookup"><span data-stu-id="abe74-1418">creditcard</span></span> 
- <span data-ttu-id="abe74-1419">cartes de crédit
</span><span class="sxs-lookup"><span data-stu-id="abe74-1419">creditcards</span></span> 
- <span data-ttu-id="abe74-1420">debetkaart
</span><span class="sxs-lookup"><span data-stu-id="abe74-1420">debetkaart</span></span> 
- <span data-ttu-id="abe74-1421">debetkaarten
</span><span class="sxs-lookup"><span data-stu-id="abe74-1421">debetkaarten</span></span> 
- <span data-ttu-id="abe74-1422">carte de débit
</span><span class="sxs-lookup"><span data-stu-id="abe74-1422">debit card</span></span> 
- <span data-ttu-id="abe74-1423">cartes de débit
</span><span class="sxs-lookup"><span data-stu-id="abe74-1423">debit cards</span></span> 
- <span data-ttu-id="abe74-1424">carte de débit
</span><span class="sxs-lookup"><span data-stu-id="abe74-1424">debitcard</span></span> 
- <span data-ttu-id="abe74-1425">cartes de débit
</span><span class="sxs-lookup"><span data-stu-id="abe74-1425">debitcards</span></span> 
- <span data-ttu-id="abe74-1426">debito automatico
</span><span class="sxs-lookup"><span data-stu-id="abe74-1426">debito automatico</span></span> 
- <span data-ttu-id="abe74-1427">diners club
</span><span class="sxs-lookup"><span data-stu-id="abe74-1427">diners club</span></span> 
- <span data-ttu-id="abe74-1428">dinersclub
</span><span class="sxs-lookup"><span data-stu-id="abe74-1428">dinersclub</span></span> 
- <span data-ttu-id="abe74-1429">découvrir</span><span class="sxs-lookup"><span data-stu-id="abe74-1429">discover</span></span> 
- <span data-ttu-id="abe74-1430">discover card
</span><span class="sxs-lookup"><span data-stu-id="abe74-1430">discover card</span></span> 
- <span data-ttu-id="abe74-1431">discover cards
</span><span class="sxs-lookup"><span data-stu-id="abe74-1431">discover cards</span></span> 
- <span data-ttu-id="abe74-1432">discovercard
</span><span class="sxs-lookup"><span data-stu-id="abe74-1432">discovercard</span></span> 
- <span data-ttu-id="abe74-1433">discovercards
</span><span class="sxs-lookup"><span data-stu-id="abe74-1433">discovercards</span></span> 
- <span data-ttu-id="abe74-1434">débito automático</span><span class="sxs-lookup"><span data-stu-id="abe74-1434">débito automático</span></span>
- <span data-ttu-id="abe74-1435">
edc
</span><span class="sxs-lookup"><span data-stu-id="abe74-1435">edc</span></span> 
- <span data-ttu-id="abe74-1436">eigentümername
</span><span class="sxs-lookup"><span data-stu-id="abe74-1436">eigentümername</span></span> 
- <span data-ttu-id="abe74-1437">carte de crédit européenne
</span><span class="sxs-lookup"><span data-stu-id="abe74-1437">european debit card</span></span> 
- <span data-ttu-id="abe74-1438">hoofdkaart
</span><span class="sxs-lookup"><span data-stu-id="abe74-1438">hoofdkaart</span></span> 
- <span data-ttu-id="abe74-1439">hoofdkaarten
</span><span class="sxs-lookup"><span data-stu-id="abe74-1439">hoofdkaarten</span></span> 
- <span data-ttu-id="abe74-1440">in viaggio
</span><span class="sxs-lookup"><span data-stu-id="abe74-1440">in viaggio</span></span> 
- <span data-ttu-id="abe74-1441">japanese card bureau
</span><span class="sxs-lookup"><span data-stu-id="abe74-1441">japanese card bureau</span></span> 
- <span data-ttu-id="abe74-1442">japanse kaartdienst
</span><span class="sxs-lookup"><span data-stu-id="abe74-1442">japanse kaartdienst</span></span> 
- <span data-ttu-id="abe74-1443">jcb
</span><span class="sxs-lookup"><span data-stu-id="abe74-1443">jcb</span></span> 
- <span data-ttu-id="abe74-1444">kaart
</span><span class="sxs-lookup"><span data-stu-id="abe74-1444">kaart</span></span> 
- <span data-ttu-id="abe74-1445">kaart num
</span><span class="sxs-lookup"><span data-stu-id="abe74-1445">kaart num</span></span> 
- <span data-ttu-id="abe74-1446">kaartaantal
</span><span class="sxs-lookup"><span data-stu-id="abe74-1446">kaartaantal</span></span> 
- <span data-ttu-id="abe74-1447">kaartaantallen
</span><span class="sxs-lookup"><span data-stu-id="abe74-1447">kaartaantallen</span></span> 
- <span data-ttu-id="abe74-1448">kaarthouder
</span><span class="sxs-lookup"><span data-stu-id="abe74-1448">kaarthouder</span></span> 
- <span data-ttu-id="abe74-1449">kaarthouders
</span><span class="sxs-lookup"><span data-stu-id="abe74-1449">kaarthouders</span></span> 
- <span data-ttu-id="abe74-1450">karte
</span><span class="sxs-lookup"><span data-stu-id="abe74-1450">karte</span></span>  
- <span data-ttu-id="abe74-1451">karteninhaber
</span><span class="sxs-lookup"><span data-stu-id="abe74-1451">karteninhaber</span></span> 
- <span data-ttu-id="abe74-1452">karteninhabers</span><span class="sxs-lookup"><span data-stu-id="abe74-1452">karteninhabers</span></span>
- <span data-ttu-id="abe74-1453">
kartennr
</span><span class="sxs-lookup"><span data-stu-id="abe74-1453">kartennr</span></span> 
- <span data-ttu-id="abe74-1454">kartennummer</span><span class="sxs-lookup"><span data-stu-id="abe74-1454">kartennummer</span></span> 
- <span data-ttu-id="abe74-1455">kreditkarte
</span><span class="sxs-lookup"><span data-stu-id="abe74-1455">kreditkarte</span></span> 
- <span data-ttu-id="abe74-1456">kreditkarten-nummer</span><span class="sxs-lookup"><span data-stu-id="abe74-1456">kreditkarten-nummer</span></span> 
- <span data-ttu-id="abe74-1457">kreditkarteninhaber
</span><span class="sxs-lookup"><span data-stu-id="abe74-1457">kreditkarteninhaber</span></span> 
- <span data-ttu-id="abe74-1458">kreditkarteninstitut
</span><span class="sxs-lookup"><span data-stu-id="abe74-1458">kreditkarteninstitut</span></span> 
- <span data-ttu-id="abe74-1459">kreditkartennummer
</span><span class="sxs-lookup"><span data-stu-id="abe74-1459">kreditkartennummer</span></span> 
- <span data-ttu-id="abe74-1460">kreditkartentyp
</span><span class="sxs-lookup"><span data-stu-id="abe74-1460">kreditkartentyp</span></span> 
- <span data-ttu-id="abe74-1461">maestro
</span><span class="sxs-lookup"><span data-stu-id="abe74-1461">maestro</span></span> 
- <span data-ttu-id="abe74-1462">master card
</span><span class="sxs-lookup"><span data-stu-id="abe74-1462">master card</span></span> 
- <span data-ttu-id="abe74-1463">master cards
</span><span class="sxs-lookup"><span data-stu-id="abe74-1463">master cards</span></span> 
- <span data-ttu-id="abe74-1464">mastercard
</span><span class="sxs-lookup"><span data-stu-id="abe74-1464">mastercard</span></span> 
- <span data-ttu-id="abe74-1465">mastercards</span><span class="sxs-lookup"><span data-stu-id="abe74-1465">mastercards</span></span> 
- <span data-ttu-id="abe74-1466">MC</span><span class="sxs-lookup"><span data-stu-id="abe74-1466">mc</span></span> 
- <span data-ttu-id="abe74-1467">mister cash
</span><span class="sxs-lookup"><span data-stu-id="abe74-1467">mister cash</span></span> 
- <span data-ttu-id="abe74-1468">carta n</span><span class="sxs-lookup"><span data-stu-id="abe74-1468">n carta</span></span> 
- <span data-ttu-id="abe74-1469">Carta</span><span class="sxs-lookup"><span data-stu-id="abe74-1469">carta</span></span> 
- <span data-ttu-id="abe74-1470">Aucun tarjeta de</span><span class="sxs-lookup"><span data-stu-id="abe74-1470">no de tarjeta</span></span> 
- <span data-ttu-id="abe74-1471">Aucun cartao</span><span class="sxs-lookup"><span data-stu-id="abe74-1471">no do cartao</span></span> 
- <span data-ttu-id="abe74-1472">Aucun cartão</span><span class="sxs-lookup"><span data-stu-id="abe74-1472">no do cartão</span></span> 
- <span data-ttu-id="abe74-p117">no. de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="abe74-p117">no. de tarjeta</span></span> 
- <span data-ttu-id="abe74-p118">no. do cartao
</span><span class="sxs-lookup"><span data-stu-id="abe74-p118">no. do cartao</span></span> 
- <span data-ttu-id="abe74-p119">no. do cartão
</span><span class="sxs-lookup"><span data-stu-id="abe74-p119">no. do cartão</span></span> 
- <span data-ttu-id="abe74-1479">nr carta</span><span class="sxs-lookup"><span data-stu-id="abe74-1479">nr carta</span></span> 
- <span data-ttu-id="abe74-p120">nr. carta
</span><span class="sxs-lookup"><span data-stu-id="abe74-p120">nr. carta</span></span> 
- <span data-ttu-id="abe74-1482">numeri di scheda
</span><span class="sxs-lookup"><span data-stu-id="abe74-1482">numeri di scheda</span></span> 
- <span data-ttu-id="abe74-1483">numero carta
</span><span class="sxs-lookup"><span data-stu-id="abe74-1483">numero carta</span></span> 
- <span data-ttu-id="abe74-1484">numero de cartao
</span><span class="sxs-lookup"><span data-stu-id="abe74-1484">numero de cartao</span></span> 
- <span data-ttu-id="abe74-1485">numero de carte
</span><span class="sxs-lookup"><span data-stu-id="abe74-1485">numero de carte</span></span> 
- <span data-ttu-id="abe74-1486">numero de cartão
</span><span class="sxs-lookup"><span data-stu-id="abe74-1486">numero de cartão</span></span> 
- <span data-ttu-id="abe74-1487">numero de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="abe74-1487">numero de tarjeta</span></span>
- <span data-ttu-id="abe74-1488">numero della carta
</span><span class="sxs-lookup"><span data-stu-id="abe74-1488">numero della carta</span></span> 
- <span data-ttu-id="abe74-1489">numero di carta
</span><span class="sxs-lookup"><span data-stu-id="abe74-1489">numero di carta</span></span> 
- <span data-ttu-id="abe74-1490">numero di scheda
</span><span class="sxs-lookup"><span data-stu-id="abe74-1490">numero di scheda</span></span> 
- <span data-ttu-id="abe74-1491">numero do cartao
</span><span class="sxs-lookup"><span data-stu-id="abe74-1491">numero do cartao</span></span> 
- <span data-ttu-id="abe74-1492">numero do cartão
</span><span class="sxs-lookup"><span data-stu-id="abe74-1492">numero do cartão</span></span> 
- <span data-ttu-id="abe74-1493">numéro de carte
</span><span class="sxs-lookup"><span data-stu-id="abe74-1493">numéro de carte</span></span> 
- <span data-ttu-id="abe74-1494">nº carta
</span><span class="sxs-lookup"><span data-stu-id="abe74-1494">nº carta</span></span> 
- <span data-ttu-id="abe74-1495">nº de carte
</span><span class="sxs-lookup"><span data-stu-id="abe74-1495">nº de carte</span></span> 
- <span data-ttu-id="abe74-1496">nº de la carte
</span><span class="sxs-lookup"><span data-stu-id="abe74-1496">nº de la carte</span></span> 
- <span data-ttu-id="abe74-1497">nº de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="abe74-1497">nº de tarjeta</span></span> 
- <span data-ttu-id="abe74-1498">nº do cartao
</span><span class="sxs-lookup"><span data-stu-id="abe74-1498">nº do cartao</span></span> 
- <span data-ttu-id="abe74-1499">Nº cartão</span><span class="sxs-lookup"><span data-stu-id="abe74-1499">nº do cartão</span></span> 
- <span data-ttu-id="abe74-p121">nº. do cartão
</span><span class="sxs-lookup"><span data-stu-id="abe74-p121">nº. do cartão</span></span> 
- <span data-ttu-id="abe74-1502">número de cartao
</span><span class="sxs-lookup"><span data-stu-id="abe74-1502">número de cartao</span></span> 
- <span data-ttu-id="abe74-1503">número de cartão
</span><span class="sxs-lookup"><span data-stu-id="abe74-1503">número de cartão</span></span> 
- <span data-ttu-id="abe74-1504">número de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="abe74-1504">número de tarjeta</span></span> 
- <span data-ttu-id="abe74-1505">número do cartao</span><span class="sxs-lookup"><span data-stu-id="abe74-1505">número do cartao</span></span> 
- <span data-ttu-id="abe74-1506">scheda dell’assegno
</span><span class="sxs-lookup"><span data-stu-id="abe74-1506">scheda dell'assegno</span></span> 
- <span data-ttu-id="abe74-1507">scheda dell’atmosfera
</span><span class="sxs-lookup"><span data-stu-id="abe74-1507">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="abe74-1508">scheda dell’atmosfera
</span><span class="sxs-lookup"><span data-stu-id="abe74-1508">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="abe74-1509">scheda della banca
</span><span class="sxs-lookup"><span data-stu-id="abe74-1509">scheda della banca</span></span> 
- <span data-ttu-id="abe74-1510">scheda di controllo
</span><span class="sxs-lookup"><span data-stu-id="abe74-1510">scheda di controllo</span></span> 
- <span data-ttu-id="abe74-1511">scheda di debito
</span><span class="sxs-lookup"><span data-stu-id="abe74-1511">scheda di debito</span></span> 
- <span data-ttu-id="abe74-1512">scheda matrice
</span><span class="sxs-lookup"><span data-stu-id="abe74-1512">scheda matrice</span></span> 
- <span data-ttu-id="abe74-1513">schede dell’atmosfera
</span><span class="sxs-lookup"><span data-stu-id="abe74-1513">schede dell'atmosfera</span></span> 
- <span data-ttu-id="abe74-1514">schede di controllo
</span><span class="sxs-lookup"><span data-stu-id="abe74-1514">schede di controllo</span></span> 
- <span data-ttu-id="abe74-1515">schede di debito
</span><span class="sxs-lookup"><span data-stu-id="abe74-1515">schede di debito</span></span> 
- <span data-ttu-id="abe74-1516">schede matrici
</span><span class="sxs-lookup"><span data-stu-id="abe74-1516">schede matrici</span></span> 
- <span data-ttu-id="abe74-1517">scoprono la scheda
</span><span class="sxs-lookup"><span data-stu-id="abe74-1517">scoprono la scheda</span></span> 
- <span data-ttu-id="abe74-1518">scoprono le schede
</span><span class="sxs-lookup"><span data-stu-id="abe74-1518">scoprono le schede</span></span> 
- <span data-ttu-id="abe74-1519">solo
</span><span class="sxs-lookup"><span data-stu-id="abe74-1519">solo</span></span> 
- <span data-ttu-id="abe74-1520">supporti di scheda
</span><span class="sxs-lookup"><span data-stu-id="abe74-1520">supporti di scheda</span></span> 
- <span data-ttu-id="abe74-1521">supporto di scheda
</span><span class="sxs-lookup"><span data-stu-id="abe74-1521">supporto di scheda</span></span> 
- <span data-ttu-id="abe74-1522">commutateur</span><span class="sxs-lookup"><span data-stu-id="abe74-1522">switch</span></span> 
- <span data-ttu-id="abe74-1523">tarjeta atm
</span><span class="sxs-lookup"><span data-stu-id="abe74-1523">tarjeta atm</span></span> 
- <span data-ttu-id="abe74-1524">tarjeta credito
</span><span class="sxs-lookup"><span data-stu-id="abe74-1524">tarjeta credito</span></span> 
- <span data-ttu-id="abe74-1525">tarjeta de atm
</span><span class="sxs-lookup"><span data-stu-id="abe74-1525">tarjeta de atm</span></span> 
- <span data-ttu-id="abe74-1526">tarjeta de credito
</span><span class="sxs-lookup"><span data-stu-id="abe74-1526">tarjeta de credito</span></span> 
- <span data-ttu-id="abe74-1527">tarjeta de debito
</span><span class="sxs-lookup"><span data-stu-id="abe74-1527">tarjeta de debito</span></span> 
- <span data-ttu-id="abe74-1528">tarjeta debito
</span><span class="sxs-lookup"><span data-stu-id="abe74-1528">tarjeta debito</span></span> 
- <span data-ttu-id="abe74-1529">tarjeta no
</span><span class="sxs-lookup"><span data-stu-id="abe74-1529">tarjeta no</span></span>
- <span data-ttu-id="abe74-1530">tarjetahabiente
</span><span class="sxs-lookup"><span data-stu-id="abe74-1530">tarjetahabiente</span></span> 
- <span data-ttu-id="abe74-1531">tipo della scheda
</span><span class="sxs-lookup"><span data-stu-id="abe74-1531">tipo della scheda</span></span> 
- <span data-ttu-id="abe74-1532">ufficio giapponese della</span><span class="sxs-lookup"><span data-stu-id="abe74-1532">ufficio giapponese della</span></span> 
- <span data-ttu-id="abe74-1533">scheda
</span><span class="sxs-lookup"><span data-stu-id="abe74-1533">scheda</span></span> 
- <span data-ttu-id="abe74-1534">v pay
</span><span class="sxs-lookup"><span data-stu-id="abe74-1534">v pay</span></span> 
- <span data-ttu-id="abe74-1535">v-paie</span><span class="sxs-lookup"><span data-stu-id="abe74-1535">v-pay</span></span> 
- <span data-ttu-id="abe74-1536">visa
</span><span class="sxs-lookup"><span data-stu-id="abe74-1536">visa</span></span> 
- <span data-ttu-id="abe74-1537">visa plus
</span><span class="sxs-lookup"><span data-stu-id="abe74-1537">visa plus</span></span> 
- <span data-ttu-id="abe74-1538">visa electron
</span><span class="sxs-lookup"><span data-stu-id="abe74-1538">visa electron</span></span> 
- <span data-ttu-id="abe74-1539">visto
</span><span class="sxs-lookup"><span data-stu-id="abe74-1539">visto</span></span> 
- <span data-ttu-id="abe74-1540">visum
</span><span class="sxs-lookup"><span data-stu-id="abe74-1540">visum</span></span> 
- <span data-ttu-id="abe74-1541">vpay
</span><span class="sxs-lookup"><span data-stu-id="abe74-1541">vpay</span></span>   

#### <a name="keywordcardsecuritytermsdict"></a><span data-ttu-id="abe74-1542">Keyword_card_security_terms_dict</span><span class="sxs-lookup"><span data-stu-id="abe74-1542">Keyword_card_security_terms_dict</span></span>

- <span data-ttu-id="abe74-1543">numéro d’identification de la carte</span><span class="sxs-lookup"><span data-stu-id="abe74-1543">card identification number</span></span>
- <span data-ttu-id="abe74-1544">vérification de la carte</span><span class="sxs-lookup"><span data-stu-id="abe74-1544">card verification</span></span> 
- <span data-ttu-id="abe74-1545">cardi la verifica
</span><span class="sxs-lookup"><span data-stu-id="abe74-1545">cardi la verifica</span></span> 
- <span data-ttu-id="abe74-1546">nic
</span><span class="sxs-lookup"><span data-stu-id="abe74-1546">cid</span></span> 
- <span data-ttu-id="abe74-1547">segment de remboursement</span><span class="sxs-lookup"><span data-stu-id="abe74-1547">cod seg</span></span> 
- <span data-ttu-id="abe74-1548">remboursement seguranca</span><span class="sxs-lookup"><span data-stu-id="abe74-1548">cod seguranca</span></span> 
- <span data-ttu-id="abe74-1549">remboursement segurança</span><span class="sxs-lookup"><span data-stu-id="abe74-1549">cod segurança</span></span> 
- <span data-ttu-id="abe74-1550">remboursement sicurezza</span><span class="sxs-lookup"><span data-stu-id="abe74-1550">cod sicurezza</span></span> 
- <span data-ttu-id="abe74-p122">cod. seg
</span><span class="sxs-lookup"><span data-stu-id="abe74-p122">cod. seg</span></span> 
- <span data-ttu-id="abe74-p123">cod. seguranca
</span><span class="sxs-lookup"><span data-stu-id="abe74-p123">cod. seguranca</span></span> 
- <span data-ttu-id="abe74-p124">cod. segurança
</span><span class="sxs-lookup"><span data-stu-id="abe74-p124">cod. segurança</span></span> 
- <span data-ttu-id="abe74-p125">cod. sicurezza
</span><span class="sxs-lookup"><span data-stu-id="abe74-p125">cod. sicurezza</span></span> 
- <span data-ttu-id="abe74-1559">codice di sicurezza
</span><span class="sxs-lookup"><span data-stu-id="abe74-1559">codice di sicurezza</span></span> 
- <span data-ttu-id="abe74-1560">codice di verifica
</span><span class="sxs-lookup"><span data-stu-id="abe74-1560">codice di verifica</span></span> 
- <span data-ttu-id="abe74-1561">codigo
</span><span class="sxs-lookup"><span data-stu-id="abe74-1561">codigo</span></span> 
- <span data-ttu-id="abe74-1562">codigo de seguranca
</span><span class="sxs-lookup"><span data-stu-id="abe74-1562">codigo de seguranca</span></span> 
- <span data-ttu-id="abe74-1563">codigo de segurança
</span><span class="sxs-lookup"><span data-stu-id="abe74-1563">codigo de segurança</span></span> 
- <span data-ttu-id="abe74-1564">crittogramma
</span><span class="sxs-lookup"><span data-stu-id="abe74-1564">crittogramma</span></span> 
- <span data-ttu-id="abe74-1565">cryptogramme
</span><span class="sxs-lookup"><span data-stu-id="abe74-1565">cryptogram</span></span> 
- <span data-ttu-id="abe74-1566">cryptogramme
</span><span class="sxs-lookup"><span data-stu-id="abe74-1566">cryptogramme</span></span> 
- <span data-ttu-id="abe74-1567">CV2</span><span class="sxs-lookup"><span data-stu-id="abe74-1567">cv2</span></span> 
- <span data-ttu-id="abe74-1568">cvc
</span><span class="sxs-lookup"><span data-stu-id="abe74-1568">cvc</span></span> 
- <span data-ttu-id="abe74-1569">CVC2</span><span class="sxs-lookup"><span data-stu-id="abe74-1569">cvc2</span></span> 
- <span data-ttu-id="abe74-1570">nvc
</span><span class="sxs-lookup"><span data-stu-id="abe74-1570">cvn</span></span> 
- <span data-ttu-id="abe74-1571">cvv
</span><span class="sxs-lookup"><span data-stu-id="abe74-1571">cvv</span></span> 
- <span data-ttu-id="abe74-1572">VVC2</span><span class="sxs-lookup"><span data-stu-id="abe74-1572">cvv2</span></span> 
- <span data-ttu-id="abe74-1573">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="abe74-1573">cód seguranca</span></span> 
- <span data-ttu-id="abe74-1574">cód segurança</span><span class="sxs-lookup"><span data-stu-id="abe74-1574">cód segurança</span></span> 
- <span data-ttu-id="abe74-p126">cód. seguranca
</span><span class="sxs-lookup"><span data-stu-id="abe74-p126">cód. seguranca</span></span> 
- <span data-ttu-id="abe74-p127">cód. Segurança
</span><span class="sxs-lookup"><span data-stu-id="abe74-p127">cód. segurança</span></span> 
- <span data-ttu-id="abe74-1579">código
</span><span class="sxs-lookup"><span data-stu-id="abe74-1579">código</span></span> 
- <span data-ttu-id="abe74-1580">código de seguranca
</span><span class="sxs-lookup"><span data-stu-id="abe74-1580">código de seguranca</span></span> 
- <span data-ttu-id="abe74-1581">código de segurança
</span><span class="sxs-lookup"><span data-stu-id="abe74-1581">código de segurança</span></span> 
- <span data-ttu-id="abe74-1582">de kaart controle
</span><span class="sxs-lookup"><span data-stu-id="abe74-1582">de kaart controle</span></span> 
- <span data-ttu-id="abe74-1583">geeft nr suit
</span><span class="sxs-lookup"><span data-stu-id="abe74-1583">geeft nr uit</span></span> 
- <span data-ttu-id="abe74-1584">n° d’émission
</span><span class="sxs-lookup"><span data-stu-id="abe74-1584">issue no</span></span> 
- <span data-ttu-id="abe74-1585">numéro d’émission
</span><span class="sxs-lookup"><span data-stu-id="abe74-1585">issue number</span></span> 
- <span data-ttu-id="abe74-1586">kaartidentificatienummer
</span><span class="sxs-lookup"><span data-stu-id="abe74-1586">kaartidentificatienummer</span></span> 
- <span data-ttu-id="abe74-1587">kreditkartenprufnummer
</span><span class="sxs-lookup"><span data-stu-id="abe74-1587">kreditkartenprufnummer</span></span> 
- <span data-ttu-id="abe74-1588">kreditkartenprüfnummer
</span><span class="sxs-lookup"><span data-stu-id="abe74-1588">kreditkartenprüfnummer</span></span> 
- <span data-ttu-id="abe74-1589">kwestieaantal
</span><span class="sxs-lookup"><span data-stu-id="abe74-1589">kwestieaantal</span></span> 
- <span data-ttu-id="abe74-p128">no. dell’edizione
</span><span class="sxs-lookup"><span data-stu-id="abe74-p128">no. dell'edizione</span></span> 
- <span data-ttu-id="abe74-p129">no. di sicurezza
</span><span class="sxs-lookup"><span data-stu-id="abe74-p129">no. di sicurezza</span></span> 
- <span data-ttu-id="abe74-1594">numéro de sécurité
</span><span class="sxs-lookup"><span data-stu-id="abe74-1594">numero de securite</span></span> 
- <span data-ttu-id="abe74-1595">numero de verificacao
</span><span class="sxs-lookup"><span data-stu-id="abe74-1595">numero de verificacao</span></span> 
- <span data-ttu-id="abe74-1596">numero dell’edizione
</span><span class="sxs-lookup"><span data-stu-id="abe74-1596">numero dell'edizione</span></span> 
- <span data-ttu-id="abe74-1597">numero di identificazione della</span><span class="sxs-lookup"><span data-stu-id="abe74-1597">numero di identificazione della</span></span> 
- <span data-ttu-id="abe74-1598">scheda
</span><span class="sxs-lookup"><span data-stu-id="abe74-1598">scheda</span></span> 
- <span data-ttu-id="abe74-1599">numero di sicurezza
</span><span class="sxs-lookup"><span data-stu-id="abe74-1599">numero di sicurezza</span></span> 
- <span data-ttu-id="abe74-1600">numero van veiligheid
</span><span class="sxs-lookup"><span data-stu-id="abe74-1600">numero van veiligheid</span></span> 
- <span data-ttu-id="abe74-1601">numéro de sécurité
</span><span class="sxs-lookup"><span data-stu-id="abe74-1601">numéro de sécurité</span></span> 
- <span data-ttu-id="abe74-1602">nº autorizzazione
</span><span class="sxs-lookup"><span data-stu-id="abe74-1602">nº autorizzazione</span></span> 
- <span data-ttu-id="abe74-1603">número de verificação
</span><span class="sxs-lookup"><span data-stu-id="abe74-1603">número de verificação</span></span> 
- <span data-ttu-id="abe74-1604">perno il blocco
</span><span class="sxs-lookup"><span data-stu-id="abe74-1604">perno il blocco</span></span> 
- <span data-ttu-id="abe74-1605">pin block
</span><span class="sxs-lookup"><span data-stu-id="abe74-1605">pin block</span></span> 
- <span data-ttu-id="abe74-1606">prufziffer
</span><span class="sxs-lookup"><span data-stu-id="abe74-1606">prufziffer</span></span> 
- <span data-ttu-id="abe74-1607">prüfziffer
</span><span class="sxs-lookup"><span data-stu-id="abe74-1607">prüfziffer</span></span> 
- <span data-ttu-id="abe74-1608">code de sécurité
</span><span class="sxs-lookup"><span data-stu-id="abe74-1608">security code</span></span> 
- <span data-ttu-id="abe74-1609">n° de sécurité
</span><span class="sxs-lookup"><span data-stu-id="abe74-1609">security no</span></span> 
- <span data-ttu-id="abe74-1610">numéro de sécurité
</span><span class="sxs-lookup"><span data-stu-id="abe74-1610">security number</span></span> 
- <span data-ttu-id="abe74-1611">sicherheits kode
</span><span class="sxs-lookup"><span data-stu-id="abe74-1611">sicherheits kode</span></span> 
- <span data-ttu-id="abe74-1612">sicherheitscode
</span><span class="sxs-lookup"><span data-stu-id="abe74-1612">sicherheitscode</span></span> 
- <span data-ttu-id="abe74-1613">sicherheitsnummer
</span><span class="sxs-lookup"><span data-stu-id="abe74-1613">sicherheitsnummer</span></span> 
- <span data-ttu-id="abe74-1614">speldblok
</span><span class="sxs-lookup"><span data-stu-id="abe74-1614">speldblok</span></span> 
- <span data-ttu-id="abe74-1615">veiligheid nr
</span><span class="sxs-lookup"><span data-stu-id="abe74-1615">veiligheid nr</span></span> 
- <span data-ttu-id="abe74-1616">veiligheidsaantal
</span><span class="sxs-lookup"><span data-stu-id="abe74-1616">veiligheidsaantal</span></span> 
- <span data-ttu-id="abe74-1617">veiligheidscode
</span><span class="sxs-lookup"><span data-stu-id="abe74-1617">veiligheidscode</span></span> 
- <span data-ttu-id="abe74-1618">veiligheidsnummer
</span><span class="sxs-lookup"><span data-stu-id="abe74-1618">veiligheidsnummer</span></span> 
- <span data-ttu-id="abe74-1619">verfalldatum
</span><span class="sxs-lookup"><span data-stu-id="abe74-1619">verfalldatum</span></span> 

#### <a name="keywordcardexpirationtermsdict"></a><span data-ttu-id="abe74-1620">Keyword_card_expiration_terms_dict</span><span class="sxs-lookup"><span data-stu-id="abe74-1620">Keyword_card_expiration_terms_dict</span></span>

- <span data-ttu-id="abe74-1621">ablauf
</span><span class="sxs-lookup"><span data-stu-id="abe74-1621">ablauf</span></span> 
- <span data-ttu-id="abe74-1622">data de expiracao
</span><span class="sxs-lookup"><span data-stu-id="abe74-1622">data de expiracao</span></span> 
- <span data-ttu-id="abe74-1623">data de expiração
</span><span class="sxs-lookup"><span data-stu-id="abe74-1623">data de expiração</span></span> 
- <span data-ttu-id="abe74-1624">data del exp
</span><span class="sxs-lookup"><span data-stu-id="abe74-1624">data del exp</span></span> 
- <span data-ttu-id="abe74-1625">data di exp
</span><span class="sxs-lookup"><span data-stu-id="abe74-1625">data di exp</span></span> 
- <span data-ttu-id="abe74-1626">data di scadenza
</span><span class="sxs-lookup"><span data-stu-id="abe74-1626">data di scadenza</span></span> 
- <span data-ttu-id="abe74-1627">data em que expira
</span><span class="sxs-lookup"><span data-stu-id="abe74-1627">data em que expira</span></span> 
- <span data-ttu-id="abe74-1628">data scad
</span><span class="sxs-lookup"><span data-stu-id="abe74-1628">data scad</span></span> 
- <span data-ttu-id="abe74-1629">data scadenza
</span><span class="sxs-lookup"><span data-stu-id="abe74-1629">data scadenza</span></span> 
- <span data-ttu-id="abe74-1630">date de validité
</span><span class="sxs-lookup"><span data-stu-id="abe74-1630">date de validité</span></span> 
- <span data-ttu-id="abe74-1631">datum afloop
</span><span class="sxs-lookup"><span data-stu-id="abe74-1631">datum afloop</span></span> 
- <span data-ttu-id="abe74-1632">datum van exp
</span><span class="sxs-lookup"><span data-stu-id="abe74-1632">datum van exp</span></span> 
- <span data-ttu-id="abe74-1633">de afloop
</span><span class="sxs-lookup"><span data-stu-id="abe74-1633">de afloop</span></span> 
- <span data-ttu-id="abe74-1634">espira
</span><span class="sxs-lookup"><span data-stu-id="abe74-1634">espira</span></span> 
- <span data-ttu-id="abe74-1635">espira
</span><span class="sxs-lookup"><span data-stu-id="abe74-1635">espira</span></span> 
- <span data-ttu-id="abe74-1636">date d’exp
</span><span class="sxs-lookup"><span data-stu-id="abe74-1636">exp date</span></span> 
- <span data-ttu-id="abe74-1637">exp datum
</span><span class="sxs-lookup"><span data-stu-id="abe74-1637">exp datum</span></span> 
- <span data-ttu-id="abe74-1638">expiration</span><span class="sxs-lookup"><span data-stu-id="abe74-1638">expiration</span></span> 
- <span data-ttu-id="abe74-1639">expire
</span><span class="sxs-lookup"><span data-stu-id="abe74-1639">expire</span></span> 
- <span data-ttu-id="abe74-1640">expire
</span><span class="sxs-lookup"><span data-stu-id="abe74-1640">expires</span></span> 
- <span data-ttu-id="abe74-1641">expiration
</span><span class="sxs-lookup"><span data-stu-id="abe74-1641">expiry</span></span> 
- <span data-ttu-id="abe74-1642">fecha de expiracion
</span><span class="sxs-lookup"><span data-stu-id="abe74-1642">fecha de expiracion</span></span> 
- <span data-ttu-id="abe74-1643">fecha de venc
</span><span class="sxs-lookup"><span data-stu-id="abe74-1643">fecha de venc</span></span> 
- <span data-ttu-id="abe74-1644">gultig bis
</span><span class="sxs-lookup"><span data-stu-id="abe74-1644">gultig bis</span></span> 
- <span data-ttu-id="abe74-1645">gultigkeitsdatum
</span><span class="sxs-lookup"><span data-stu-id="abe74-1645">gultigkeitsdatum</span></span> 
- <span data-ttu-id="abe74-1646">gültig bis
</span><span class="sxs-lookup"><span data-stu-id="abe74-1646">gültig bis</span></span> 
- <span data-ttu-id="abe74-1647">gültigkeitsdatum
</span><span class="sxs-lookup"><span data-stu-id="abe74-1647">gültigkeitsdatum</span></span> 
- <span data-ttu-id="abe74-1648">la scadenza
</span><span class="sxs-lookup"><span data-stu-id="abe74-1648">la scadenza</span></span> 
- <span data-ttu-id="abe74-1649">scadenza
</span><span class="sxs-lookup"><span data-stu-id="abe74-1649">scadenza</span></span> 
- <span data-ttu-id="abe74-1650">valable
</span><span class="sxs-lookup"><span data-stu-id="abe74-1650">valable</span></span> 
- <span data-ttu-id="abe74-1651">validade
</span><span class="sxs-lookup"><span data-stu-id="abe74-1651">validade</span></span> 
- <span data-ttu-id="abe74-1652">valido hasta
</span><span class="sxs-lookup"><span data-stu-id="abe74-1652">valido hasta</span></span> 
- <span data-ttu-id="abe74-1653">valor
</span><span class="sxs-lookup"><span data-stu-id="abe74-1653">valor</span></span> 
- <span data-ttu-id="abe74-1654">venc
</span><span class="sxs-lookup"><span data-stu-id="abe74-1654">venc</span></span> 
- <span data-ttu-id="abe74-1655">vencimento
</span><span class="sxs-lookup"><span data-stu-id="abe74-1655">vencimento</span></span> 
- <span data-ttu-id="abe74-1656">vencimiento
</span><span class="sxs-lookup"><span data-stu-id="abe74-1656">vencimiento</span></span> 
- <span data-ttu-id="abe74-1657">verloopt
</span><span class="sxs-lookup"><span data-stu-id="abe74-1657">verloopt</span></span> 
- <span data-ttu-id="abe74-1658">vervaldag
</span><span class="sxs-lookup"><span data-stu-id="abe74-1658">vervaldag</span></span> 
- <span data-ttu-id="abe74-1659">vervaldatum
</span><span class="sxs-lookup"><span data-stu-id="abe74-1659">vervaldatum</span></span> 
- <span data-ttu-id="abe74-1660">vto
</span><span class="sxs-lookup"><span data-stu-id="abe74-1660">vto</span></span> 
- <span data-ttu-id="abe74-1661">válido hasta
</span><span class="sxs-lookup"><span data-stu-id="abe74-1661">válido hasta</span></span> 
   
## <a name="eu-drivers-license-number"></a><span data-ttu-id="abe74-1662">Numéro de permis de conduire l’Union européenne</span><span class="sxs-lookup"><span data-stu-id="abe74-1662">EU Driver's License Number</span></span>

<span data-ttu-id="abe74-1663">Pour plus d’informations, voir le [type d’informations sensibles numéro de permis de conduire l’Union européenne](eu-driver-s-license-number.md).</span><span class="sxs-lookup"><span data-stu-id="abe74-1663">To learn more, see [EU Driver's License Number sensitive information type](eu-driver-s-license-number.md).</span></span>
  
## <a name="eu-national-identification-number"></a><span data-ttu-id="abe74-1664">Numéro d’Identification nationales de l’UE</span><span class="sxs-lookup"><span data-stu-id="abe74-1664">EU National Identification Number</span></span>

<span data-ttu-id="abe74-1665">Pour plus d’informations, voir le [type d’informations sensibles National numéro d’Identification de l’UE](eu-national-identification-number.md).</span><span class="sxs-lookup"><span data-stu-id="abe74-1665">To learn more, see [EU National Identification Number sensitive information type](eu-national-identification-number.md).</span></span>
  
## <a name="eu-passport-number"></a><span data-ttu-id="abe74-1666">Numéro de passeport UE</span><span class="sxs-lookup"><span data-stu-id="abe74-1666">EU Passport Number</span></span>

<span data-ttu-id="abe74-1667">Pour plus d’informations, voir le [numéro de passeport UE type d’informations sensibles](eu-passport-number.md).</span><span class="sxs-lookup"><span data-stu-id="abe74-1667">To learn more, see [EU Passport Number sensitive information type](eu-passport-number.md).</span></span>
  
## <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="abe74-1668">ID de numéro de sécurité sociale de l’Union européenne ou équivalent</span><span class="sxs-lookup"><span data-stu-id="abe74-1668">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="abe74-1669">Pour plus d’informations, voir [numéro de sécurité sociale de l’Union européenne ou type d’informations sensibles ID équivalente](eu-social-security-number-or-equivalent-id.md).</span><span class="sxs-lookup"><span data-stu-id="abe74-1669">To learn more, see [EU Social Security Number or Equivalent ID sensitive information type](eu-social-security-number-or-equivalent-id.md).</span></span>
  
## <a name="eu-tax-identification-number"></a><span data-ttu-id="abe74-1670">Numéro d’Identification de l’UE taxe</span><span class="sxs-lookup"><span data-stu-id="abe74-1670">EU Tax Identification Number</span></span>

<span data-ttu-id="abe74-1671">Pour plus d’informations, voir [type d’informations sensibles numéro d’Identification de taxe de l’UE](eu-tax-identification-number.md).</span><span class="sxs-lookup"><span data-stu-id="abe74-1671">To learn more, see [EU Tax Identification Number sensitive information type](eu-tax-identification-number.md).</span></span>
  
## <a name="finland-national-id"></a><span data-ttu-id="abe74-1672">ID national finlandais</span><span class="sxs-lookup"><span data-stu-id="abe74-1672">Finland National ID</span></span>

### <a name="format"></a><span data-ttu-id="abe74-1673">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-1673">Format</span></span>

<span data-ttu-id="abe74-1674">Six chiffres plus un caractère indiquant un siècle plus trois chiffres plus un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-1674">Six digits plus a character indicating a century plus three digits plus a check digit</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-1675">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-1675">Pattern</span></span>

<span data-ttu-id="abe74-1676">Le modèle doit inclure tous les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="abe74-1676">Pattern must include all of the following:</span></span>
- <span data-ttu-id="abe74-1677">Six chiffres au format JJMMAA qui représentent la date de naissance</span><span class="sxs-lookup"><span data-stu-id="abe74-1677">Six digits in the format format DDMMYY which are a date of birth</span></span> 
- <span data-ttu-id="abe74-1678">Marqueur de siècle (soit « - », « + » ou « a »)</span><span class="sxs-lookup"><span data-stu-id="abe74-1678">Century marker (either '-', '+' or 'a')</span></span> 
- <span data-ttu-id="abe74-1679">Numéro d’identification personnel à trois chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-1679">Three-digit personal identification number</span></span> 
- <span data-ttu-id="abe74-1680">Un chiffre ou une lettre (ne respectant pas la casse) de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-1680">A digit or letter (case insensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-1681">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-1681">Checksum</span></span>

<span data-ttu-id="abe74-1682">Oui</span><span class="sxs-lookup"><span data-stu-id="abe74-1682">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-1683">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-1683">Definition</span></span>

<span data-ttu-id="abe74-1684">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-1684">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-1685">La fonction Func_finnish_national_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-1685">The function Func_finnish_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-1686">Un mot clé figurant dans la liste Keyword_finnish_national_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-1686">A keyword from Keyword_finnish_national_id is found.</span></span>
- <span data-ttu-id="abe74-1687">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-1687">The checksum passes.</span></span>

```
<!-- Finnish National ID-->
<Entity id="338FD995-4CB5-4F87-AD35-79BD1DD926C1" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finnish_national_id" />
          <Match idRef="Keyword_finnish_national_id" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe74-1688">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-1688">Keywords</span></span>

- <span data-ttu-id="abe74-1689">Keyword_finnish_national_id</span><span class="sxs-lookup"><span data-stu-id="abe74-1689">Keyword_finnish_national_id</span></span>
- <span data-ttu-id="abe74-1690">

Sosiaaliturvatunnus</span><span class="sxs-lookup"><span data-stu-id="abe74-1690">Sosiaaliturvatunnus</span></span>
- <span data-ttu-id="abe74-1691">SOTU Henkilötunnus HETU</span><span class="sxs-lookup"><span data-stu-id="abe74-1691">SOTU Henkilötunnus HETU</span></span>
- <span data-ttu-id="abe74-1692">Personbeteckning</span><span class="sxs-lookup"><span data-stu-id="abe74-1692">Personbeteckning</span></span>
- <span data-ttu-id="abe74-1693">Personnummer</span><span class="sxs-lookup"><span data-stu-id="abe74-1693">Personnummer</span></span>
   
## <a name="finland-passport-number"></a><span data-ttu-id="abe74-1694">Numéro de passeport finlandais</span><span class="sxs-lookup"><span data-stu-id="abe74-1694">Finland Passport Number</span></span>

<span data-ttu-id="abe74-p130">Combinaison de lettres et de chiffres motif combinaison de lettres et chiffres de neuf neuf de format : stratégie de somme de contrôle non définition A DLP deux lettres (non sensible à la casse) sept chiffres est 75 % convaincu que ce type d’informations sensibles a été détecté si, dans un proximité de 300 caractères : l’expression régulière Regex_finland_passport_number recherche de contenu qui correspond au modèle. Un mot clé à partir de Keyword_finland_passport_number est trouvé. <!-- Finland Passport Number --> 
 <Entity id="d1685ac3-1d3a-40f8-8198-32ef5669c7a5" recommendedConfidence="75" patternsProximity="300"> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_finland_passport_number"/> <Match idRef="Keyword_finland_passport_number"/> </Pattern> 
 </Entity> REUSSITE de passeport Keyword_finland_passport_number mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-p130">Format Combination of nine letters and digits Pattern Combination of nine letters and digits: Two letters (not case sensitive) Seven digits Checksum No Definition A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_finland_passport_number finds content that matches the pattern. A keyword from Keyword_finland_passport_number is found. <!-- Finland Passport Number -->
<Entity id="d1685ac3-1d3a-40f8-8198-32ef5669c7a5" recommendedConfidence="75" patternsProximity="300"> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_finland_passport_number"/> <Match idRef="Keyword_finland_passport_number"/> </Pattern>
</Entity> Keywords Keyword_finland_passport_number Passport Passi</span></span>
   
## <a name="france-drivers-license-number"></a><span data-ttu-id="abe74-1699">Numéro de permis de conduire France</span><span class="sxs-lookup"><span data-stu-id="abe74-1699">France Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-1700">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-1700">Format</span></span>

<span data-ttu-id="abe74-1701">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-1701">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-1702">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-1702">Pattern</span></span>

<span data-ttu-id="abe74-1703">12 chiffres avec validation pour écarter les modèles similaires, comme les numéros de téléphone français</span><span class="sxs-lookup"><span data-stu-id="abe74-1703">12 digits with validation to discount similar patterns such as French telephone numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-1704">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-1704">Checksum</span></span>

<span data-ttu-id="abe74-1705">Non</span><span class="sxs-lookup"><span data-stu-id="abe74-1705">No</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-1706">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-1706">Definition</span></span>

<span data-ttu-id="abe74-1707">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-1707">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-1708">La fonction Func_french_drivers_license trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-1708">The function Func_french_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-1709">Au moins une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="abe74-1709">At least one of the following is true:</span></span>
- <span data-ttu-id="abe74-1710">Un mot clé figurant dans la liste Keyword_french_drivers_license est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-1710">A keyword from Keyword_french_drivers_license is found.</span></span>
- <span data-ttu-id="abe74-1711">La fonction Func_eu_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="abe74-1711">The function Func_eu_date finds a date in the right date format.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-1712">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-1712">Keywords</span></span>

#### <a name="keywordfrenchdriverslicense"></a><span data-ttu-id="abe74-1713">Keyword_french_drivers_license</span><span class="sxs-lookup"><span data-stu-id="abe74-1713">Keyword_french_drivers_license</span></span>

- <span data-ttu-id="abe74-1714">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="abe74-1714">drivers licence</span></span>
- <span data-ttu-id="abe74-1715">drivers license</span><span class="sxs-lookup"><span data-stu-id="abe74-1715">drivers license</span></span>
- <span data-ttu-id="abe74-1716">permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-1716">driving licence</span></span>
- <span data-ttu-id="abe74-1717">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="abe74-1717">driving license</span></span>
- <span data-ttu-id="abe74-1718">
permis de conduire</span><span class="sxs-lookup"><span data-stu-id="abe74-1718">permis de conduire</span></span>
- <span data-ttu-id="abe74-1719">
numéro de permis</span><span class="sxs-lookup"><span data-stu-id="abe74-1719">licence number</span></span>
- <span data-ttu-id="abe74-1720">
numéro de permis</span><span class="sxs-lookup"><span data-stu-id="abe74-1720">license number</span></span>
- <span data-ttu-id="abe74-1721">
numéros de permis</span><span class="sxs-lookup"><span data-stu-id="abe74-1721">licence numbers</span></span>
- <span data-ttu-id="abe74-1722">

numéros de permis</span><span class="sxs-lookup"><span data-stu-id="abe74-1722">license numbers</span></span>

## <a name="france-national-id-card-cni"></a><span data-ttu-id="abe74-1723">Carte nationale d'identité (CNI) France</span><span class="sxs-lookup"><span data-stu-id="abe74-1723">France National ID Card (CNI)</span></span>

### <a name="format"></a><span data-ttu-id="abe74-1724">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-1724">Format</span></span>

<span data-ttu-id="abe74-1725">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-1725">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-1726">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-1726">Pattern</span></span>

<span data-ttu-id="abe74-1727">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-1727">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-1728">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-1728">Checksum</span></span>

<span data-ttu-id="abe74-1729">Non</span><span class="sxs-lookup"><span data-stu-id="abe74-1729">No</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-1730">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-1730">Definition</span></span>

<span data-ttu-id="abe74-1731">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-1731">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-1732">L’expression régulière Regex_france_cni trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-1732">The regular expression Regex_france_cni finds content that matches the pattern.</span></span>

```
<!-- France CNI -->
<Entity id="f741ac74-1bc0-4665-b69b-f0c7f927c0c4" patternsProximity="300" recommendedConfidence="65">
  <Pattern confidenceLevel="65">
        <IdMatch idRef="Regex_france_cni" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe74-1733">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-1733">Keywords</span></span>

<span data-ttu-id="abe74-1734">Aucun</span><span class="sxs-lookup"><span data-stu-id="abe74-1734">None</span></span>
   
## <a name="france-passport-number"></a><span data-ttu-id="abe74-1735">Numéro de passeport France</span><span class="sxs-lookup"><span data-stu-id="abe74-1735">France Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-1736">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-1736">Format</span></span>

<span data-ttu-id="abe74-1737">Neuf chiffres et lettres</span><span class="sxs-lookup"><span data-stu-id="abe74-1737">Nine digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-1738">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-1738">Pattern</span></span>

<span data-ttu-id="abe74-1739">Neuf chiffres et lettres :</span><span class="sxs-lookup"><span data-stu-id="abe74-1739">Nine digits and letters:</span></span>
- <span data-ttu-id="abe74-1740">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-1740">Two digits</span></span> 
- <span data-ttu-id="abe74-1741">Deux lettres (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="abe74-1741">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="abe74-1742">Cinq chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-1742">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-1743">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-1743">Checksum</span></span>

<span data-ttu-id="abe74-1744">Non</span><span class="sxs-lookup"><span data-stu-id="abe74-1744">No</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-1745">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-1745">Definition</span></span>

<span data-ttu-id="abe74-1746">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-1746">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-1747">La fonction Func_fr_passport trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-1747">The function Func_fr_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-1748">Un mot clé figurant dans la liste Keyword_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-1748">A keyword from Keyword_passport is found.</span></span>

```
<!-- France Passport Number -->
<Entity id="3008b884-8c8c-4cd8-a289-99f34fc7ff5d" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_fr_passport" />
        <Match idRef="Keyword_passport" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe74-1749">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-1749">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="abe74-1750">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="abe74-1750">Keyword_passport</span></span>

- <span data-ttu-id="abe74-1751">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="abe74-1751">Passport Number</span></span>
- <span data-ttu-id="abe74-1752">
N° de passeport</span><span class="sxs-lookup"><span data-stu-id="abe74-1752">Passport No</span></span>
- <span data-ttu-id="abe74-1753"># Passeport
</span><span class="sxs-lookup"><span data-stu-id="abe74-1753">Passport #</span></span>
- <span data-ttu-id="abe74-1754">#Passeport
</span><span class="sxs-lookup"><span data-stu-id="abe74-1754">Passport#</span></span>
- <span data-ttu-id="abe74-1755">IDPassport</span><span class="sxs-lookup"><span data-stu-id="abe74-1755">PassportID</span></span>
- <span data-ttu-id="abe74-1756">n° passeport
</span><span class="sxs-lookup"><span data-stu-id="abe74-1756">Passportno</span></span>
- <span data-ttu-id="abe74-1757">numéropasseport
</span><span class="sxs-lookup"><span data-stu-id="abe74-1757">passportnumber</span></span>
- <span data-ttu-id="abe74-1758">パスポート</span><span class="sxs-lookup"><span data-stu-id="abe74-1758">パスポート</span></span>
- <span data-ttu-id="abe74-1759">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="abe74-1759">パスポート番号</span></span>
- <span data-ttu-id="abe74-1760">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="abe74-1760">パスポートのNum</span></span>
- <span data-ttu-id="abe74-1761">
パスポート＃
</span><span class="sxs-lookup"><span data-stu-id="abe74-1761">パスポート ＃</span></span> 
- <span data-ttu-id="abe74-1762">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="abe74-1762">Numéro de passeport</span></span>
- <span data-ttu-id="abe74-1763">
Passeport n°</span><span class="sxs-lookup"><span data-stu-id="abe74-1763">Passeport n °</span></span>
- <span data-ttu-id="abe74-1764">Passeport numéro
</span><span class="sxs-lookup"><span data-stu-id="abe74-1764">Passeport Non</span></span>
- <span data-ttu-id="abe74-1765"># Passeport
</span><span class="sxs-lookup"><span data-stu-id="abe74-1765">Passeport #</span></span>
- <span data-ttu-id="abe74-1766">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="abe74-1766">Passeport#</span></span>
- <span data-ttu-id="abe74-1767">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="abe74-1767">PasseportNon</span></span>
- <span data-ttu-id="abe74-1768">

Passeportn °</span><span class="sxs-lookup"><span data-stu-id="abe74-1768">Passeportn °</span></span>

      
## <a name="france-social-security-number-insee"></a><span data-ttu-id="abe74-1769">Numéro de sécurité sociale (INSEE) France</span><span class="sxs-lookup"><span data-stu-id="abe74-1769">France Social Security Number (INSEE)</span></span>

### <a name="format"></a><span data-ttu-id="abe74-1770">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-1770">Format</span></span>

<span data-ttu-id="abe74-1771">15 chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-1771">15 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-1772">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-1772">Pattern</span></span>

<span data-ttu-id="abe74-1773">Doit correspondre à l’un des deux modèles suivants :</span><span class="sxs-lookup"><span data-stu-id="abe74-1773">Must match one of two patterns:</span></span>
- <span data-ttu-id="abe74-1774">13 chiffres suivis d’un espace suivi de deux chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-1774">13 digits followed by a space followed by two digits</span></span><br/>
<span data-ttu-id="abe74-1775">ou</span><span class="sxs-lookup"><span data-stu-id="abe74-1775">or</span></span>
- <span data-ttu-id="abe74-1776">15 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="abe74-1776">15 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-1777">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-1777">Checksum</span></span>

<span data-ttu-id="abe74-1778">Oui</span><span class="sxs-lookup"><span data-stu-id="abe74-1778">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-1779">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-1779">Definition</span></span>

<span data-ttu-id="abe74-1780">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 95 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-1780">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-1781">La fonction Func_french_insee ou Func_fr_insee recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-1781">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-1782">Un mot clé figurant dans la liste Keyword_fr_insee est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-1782">A keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="abe74-1783">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-1783">The checksum passes.</span></span>

<span data-ttu-id="abe74-1784">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-1784">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-1785">La fonction Func_french_insee ou Func_fr_insee recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-1785">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-1786">Aucun mot clé figurant dans la liste Keyword_fr_insee n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-1786">No keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="abe74-1787">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-1787">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-1788">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-1788">Keywords</span></span>

#### <a name="keywordfrinsee"></a><span data-ttu-id="abe74-1789">Keyword_fr_insee</span><span class="sxs-lookup"><span data-stu-id="abe74-1789">Keyword_fr_insee</span></span>

- <span data-ttu-id="abe74-1790">insee</span><span class="sxs-lookup"><span data-stu-id="abe74-1790">insee</span></span>
- <span data-ttu-id="abe74-1791">
securité sociale</span><span class="sxs-lookup"><span data-stu-id="abe74-1791">securité sociale</span></span>
- <span data-ttu-id="abe74-1792">
securite sociale</span><span class="sxs-lookup"><span data-stu-id="abe74-1792">securite sociale</span></span>
- <span data-ttu-id="abe74-1793">
id national</span><span class="sxs-lookup"><span data-stu-id="abe74-1793">national id</span></span>
- <span data-ttu-id="abe74-1794">
numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="abe74-1794">national identification</span></span>
- <span data-ttu-id="abe74-1795">
numéro d’identité</span><span class="sxs-lookup"><span data-stu-id="abe74-1795">numéro d'identité</span></span>
- <span data-ttu-id="abe74-1796">Aucun d'identité</span><span class="sxs-lookup"><span data-stu-id="abe74-1796">no d'identité</span></span>
- <span data-ttu-id="abe74-p131">
n° d’identité</span><span class="sxs-lookup"><span data-stu-id="abe74-p131">no. d'identité</span></span>
- <span data-ttu-id="abe74-1799">
numéro d’identité</span><span class="sxs-lookup"><span data-stu-id="abe74-1799">numero d'identite</span></span>
- <span data-ttu-id="abe74-1800">Aucun d'identite</span><span class="sxs-lookup"><span data-stu-id="abe74-1800">no d'identite</span></span>
- <span data-ttu-id="abe74-p132">
n° d’identité</span><span class="sxs-lookup"><span data-stu-id="abe74-p132">no. d'identite</span></span>
- <span data-ttu-id="abe74-1803">numéro de sécurité sociale
</span><span class="sxs-lookup"><span data-stu-id="abe74-1803">social security number</span></span>
- <span data-ttu-id="abe74-1804">
code de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="abe74-1804">social security code</span></span>
- <span data-ttu-id="abe74-1805">numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="abe74-1805">social insurance number</span></span>
- <span data-ttu-id="abe74-1806">
le numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="abe74-1806">le numéro d'identification nationale</span></span>
- <span data-ttu-id="abe74-1807">
d’identité nationale</span><span class="sxs-lookup"><span data-stu-id="abe74-1807">d'identité nationale</span></span>
- <span data-ttu-id="abe74-1808">
numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="abe74-1808">numéro de sécurité sociale</span></span>
- <span data-ttu-id="abe74-1809">
le code de la sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="abe74-1809">le code de la sécurité sociale</span></span>
- <span data-ttu-id="abe74-1810">
numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="abe74-1810">numéro d'assurance sociale</span></span>
- <span data-ttu-id="abe74-1811">
numéro de sécu</span><span class="sxs-lookup"><span data-stu-id="abe74-1811">numéro de sécu</span></span>
- <span data-ttu-id="abe74-1812">
code sécu
</span><span class="sxs-lookup"><span data-stu-id="abe74-1812">code sécu</span></span> 
   
## <a name="german-drivers-license-number"></a><span data-ttu-id="abe74-1813">Numéro de permis de conduire Allemagne</span><span class="sxs-lookup"><span data-stu-id="abe74-1813">German Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-1814">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-1814">Format</span></span>

<span data-ttu-id="abe74-1815">Combinaison de 11 chiffres et lettres</span><span class="sxs-lookup"><span data-stu-id="abe74-1815">Combination of 11 digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-1816">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-1816">Pattern</span></span>

<span data-ttu-id="abe74-1817">11 chiffres et lettres (ne respectent pas la casse) :</span><span class="sxs-lookup"><span data-stu-id="abe74-1817">11 digits and letters (not case sensitive):</span></span>
- <span data-ttu-id="abe74-1818">Un chiffre ou une lettre</span><span class="sxs-lookup"><span data-stu-id="abe74-1818">A digit or letter</span></span> 
- <span data-ttu-id="abe74-1819">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-1819">Two digits</span></span> 
- <span data-ttu-id="abe74-1820">Six chiffres ou lettres</span><span class="sxs-lookup"><span data-stu-id="abe74-1820">Six digits or letters</span></span> 
- <span data-ttu-id="abe74-1821">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="abe74-1821">A digit</span></span> 
- <span data-ttu-id="abe74-1822">Un chiffre ou une lettre</span><span class="sxs-lookup"><span data-stu-id="abe74-1822">A digit or letter</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-1823">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-1823">Checksum</span></span>

<span data-ttu-id="abe74-1824">Oui</span><span class="sxs-lookup"><span data-stu-id="abe74-1824">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-1825">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-1825">Definition</span></span>

<span data-ttu-id="abe74-1826">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-1826">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-1827">La fonction Func_german_drivers_license trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-1827">The function Func_german_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-1828">Au moins une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="abe74-1828">At least one of the following is true:</span></span>
    - <span data-ttu-id="abe74-1829">Un mot clé figurant dans la liste Keyword_german_drivers_license_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-1829">A keyword from Keyword_german_drivers_license_number is found.</span></span>
    - <span data-ttu-id="abe74-1830">Un mot clé figurant dans la liste Keyword_german_drivers_license_collaborative est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-1830">A keyword from Keyword_german_drivers_license_collaborative is found.</span></span>
    - <span data-ttu-id="abe74-1831">Un mot clé figurant dans la liste Keyword_german_drivers_license est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-1831">A keyword from Keyword_german_drivers_license is found.</span></span>
- <span data-ttu-id="abe74-1832">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-1832">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-1833">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-1833">Keywords</span></span>

#### <a name="keywordgermandriverslicensenumber"></a><span data-ttu-id="abe74-1834">Keyword_german_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="abe74-1834">Keyword_german_drivers_license_number</span></span>

- <span data-ttu-id="abe74-1835">Führerschein</span><span class="sxs-lookup"><span data-stu-id="abe74-1835">Führerschein</span></span>
- <span data-ttu-id="abe74-1836">
Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="abe74-1836">Fuhrerschein</span></span>
- <span data-ttu-id="abe74-1837">Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="abe74-1837">Fuehrerschein</span></span>
- <span data-ttu-id="abe74-1838">
Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="abe74-1838">Führerscheinnummer</span></span>
- <span data-ttu-id="abe74-1839">
Fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="abe74-1839">Fuhrerscheinnummer</span></span>
- <span data-ttu-id="abe74-1840">
Fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="abe74-1840">Fuehrerscheinnummer</span></span>
- <span data-ttu-id="abe74-1841">
Führerschein-
</span><span class="sxs-lookup"><span data-stu-id="abe74-1841">Führerschein-</span></span> 
- <span data-ttu-id="abe74-1842">Fuhrerschein-
</span><span class="sxs-lookup"><span data-stu-id="abe74-1842">Fuhrerschein-</span></span> 
- <span data-ttu-id="abe74-1843">Fuehrerschein-
</span><span class="sxs-lookup"><span data-stu-id="abe74-1843">Fuehrerschein-</span></span> 
- <span data-ttu-id="abe74-1844">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="abe74-1844">FührerscheinnummerNr</span></span>
- <span data-ttu-id="abe74-1845">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="abe74-1845">FuhrerscheinnummerNr</span></span>
- <span data-ttu-id="abe74-1846">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="abe74-1846">FuehrerscheinnummerNr</span></span>
- <span data-ttu-id="abe74-1847">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="abe74-1847">FührerscheinnummerKlasse</span></span>
- <span data-ttu-id="abe74-1848">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="abe74-1848">FuhrerscheinnummerKlasse</span></span>
- <span data-ttu-id="abe74-1849">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="abe74-1849">FuehrerscheinnummerKlasse</span></span>
- <span data-ttu-id="abe74-1850">Führerschein - Nr
</span><span class="sxs-lookup"><span data-stu-id="abe74-1850">Führerschein- Nr</span></span>
- <span data-ttu-id="abe74-1851">Fuhrerschein - Nr
</span><span class="sxs-lookup"><span data-stu-id="abe74-1851">Fuhrerschein- Nr</span></span>
- <span data-ttu-id="abe74-1852">Fuehrerschein - Nr
</span><span class="sxs-lookup"><span data-stu-id="abe74-1852">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="abe74-1853">Führerschein - Klasse
</span><span class="sxs-lookup"><span data-stu-id="abe74-1853">Führerschein- Klasse</span></span> 
- <span data-ttu-id="abe74-1854">Fuhrerschein - Klasse
</span><span class="sxs-lookup"><span data-stu-id="abe74-1854">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="abe74-1855">Fuehrerschein - Klasse</span><span class="sxs-lookup"><span data-stu-id="abe74-1855">Fuehrerschein- Klasse</span></span>
- <span data-ttu-id="abe74-1856">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="abe74-1856">FührerscheinnummerNr</span></span> 
- <span data-ttu-id="abe74-1857">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="abe74-1857">FuhrerscheinnummerNr</span></span> 
- <span data-ttu-id="abe74-1858">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="abe74-1858">FuehrerscheinnummerNr</span></span> 
- <span data-ttu-id="abe74-1859">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="abe74-1859">FührerscheinnummerKlasse</span></span> 
- <span data-ttu-id="abe74-1860">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="abe74-1860">FuhrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="abe74-1861">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="abe74-1861">FuehrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="abe74-1862">Führerschein - Nr
</span><span class="sxs-lookup"><span data-stu-id="abe74-1862">Führerschein- Nr</span></span> 
- <span data-ttu-id="abe74-1863">Fuhrerschein - Nr
</span><span class="sxs-lookup"><span data-stu-id="abe74-1863">Fuhrerschein- Nr</span></span> 
- <span data-ttu-id="abe74-1864">Fuehrerschein - Nr
</span><span class="sxs-lookup"><span data-stu-id="abe74-1864">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="abe74-1865">Führerschein - Klasse
</span><span class="sxs-lookup"><span data-stu-id="abe74-1865">Führerschein- Klasse</span></span> 
- <span data-ttu-id="abe74-1866">Fuhrerschein - Klasse
</span><span class="sxs-lookup"><span data-stu-id="abe74-1866">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="abe74-1867">Fuehrerschein - Klasse</span><span class="sxs-lookup"><span data-stu-id="abe74-1867">Fuehrerschein- Klasse</span></span> 
- <span data-ttu-id="abe74-1868">PC</span><span class="sxs-lookup"><span data-stu-id="abe74-1868">DL</span></span> 
- <span data-ttu-id="abe74-1869">PC</span><span class="sxs-lookup"><span data-stu-id="abe74-1869">DLS</span></span>
- <span data-ttu-id="abe74-1870">
Permis conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-1870">Driv Lic</span></span> 
- <span data-ttu-id="abe74-1871">Permis conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-1871">Driv Licen</span></span> 
- <span data-ttu-id="abe74-1872">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="abe74-1872">Driv License</span></span>
- <span data-ttu-id="abe74-1873">
Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-1873">Driv Licenses</span></span> 
- <span data-ttu-id="abe74-1874">Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-1874">Driv Licence</span></span> 
- <span data-ttu-id="abe74-1875">Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-1875">Driv Licences</span></span> 
- <span data-ttu-id="abe74-1876">Permis conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-1876">Driv Lic</span></span> 
- <span data-ttu-id="abe74-1877">Permis conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-1877">Driver Licen</span></span> 
- <span data-ttu-id="abe74-1878">Conduire</span><span class="sxs-lookup"><span data-stu-id="abe74-1878">Driver License</span></span> 
- <span data-ttu-id="abe74-1879">Licences de pilote</span><span class="sxs-lookup"><span data-stu-id="abe74-1879">Driver Licenses</span></span> 
- <span data-ttu-id="abe74-1880">Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-1880">Driver Licence</span></span> 
- <span data-ttu-id="abe74-1881">Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-1881">Driver Licences</span></span> 
- <span data-ttu-id="abe74-1882">Lic pilotes</span><span class="sxs-lookup"><span data-stu-id="abe74-1882">Drivers Lic</span></span> 
- <span data-ttu-id="abe74-1883">Licen pilotes</span><span class="sxs-lookup"><span data-stu-id="abe74-1883">Drivers Licen</span></span> 
- <span data-ttu-id="abe74-1884">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="abe74-1884">Drivers License</span></span> 
- <span data-ttu-id="abe74-1885">Licences de pilotes</span><span class="sxs-lookup"><span data-stu-id="abe74-1885">Drivers Licenses</span></span> 
- <span data-ttu-id="abe74-1886">Certificat de pilotes</span><span class="sxs-lookup"><span data-stu-id="abe74-1886">Drivers Licence</span></span> 
- <span data-ttu-id="abe74-1887">Certificats de pilotes</span><span class="sxs-lookup"><span data-stu-id="abe74-1887">Drivers Licences</span></span> 
- <span data-ttu-id="abe74-1888">Lic du pilote</span><span class="sxs-lookup"><span data-stu-id="abe74-1888">Driver's Lic</span></span> 
- <span data-ttu-id="abe74-1889">Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-1889">Driver's Licen</span></span> 
- <span data-ttu-id="abe74-1890">Conduire permis de</span><span class="sxs-lookup"><span data-stu-id="abe74-1890">Driver's License</span></span> 
- <span data-ttu-id="abe74-1891">Conduire permis de</span><span class="sxs-lookup"><span data-stu-id="abe74-1891">Driver's Licenses</span></span> 
- <span data-ttu-id="abe74-1892">Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-1892">Driver's Licence</span></span> 
- <span data-ttu-id="abe74-1893">Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-1893">Driver's Licences</span></span> 
- <span data-ttu-id="abe74-1894">Permis conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-1894">Driving Lic</span></span> 
- <span data-ttu-id="abe74-1895">Permis conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-1895">Driving Licen</span></span> 
- <span data-ttu-id="abe74-1896">Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-1896">Driving License</span></span> 
- <span data-ttu-id="abe74-1897">Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-1897">Driving Licenses</span></span> 
- <span data-ttu-id="abe74-1898">Permis de conduire

</span><span class="sxs-lookup"><span data-stu-id="abe74-1898">Driving Licence</span></span> 
- <span data-ttu-id="abe74-1899">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="abe74-1899">Driving Licences</span></span>

#### <a name="keywordgermandriverslicensecollaborative"></a><span data-ttu-id="abe74-1900">Keyword_german_drivers_license_collaborative</span><span class="sxs-lookup"><span data-stu-id="abe74-1900">Keyword_german_drivers_license_collaborative</span></span>

- <span data-ttu-id="abe74-1901">
Nr-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="abe74-1901">Nr-Führerschein</span></span> 
- <span data-ttu-id="abe74-1902">Nr-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="abe74-1902">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="abe74-1903">Nr-Fuehrerschein
</span><span class="sxs-lookup"><span data-stu-id="abe74-1903">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="abe74-1904">No-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="abe74-1904">No-Führerschein</span></span> 
- <span data-ttu-id="abe74-1905">No-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="abe74-1905">No-Fuhrerschein</span></span> 
- <span data-ttu-id="abe74-1906">No-Fuehrerschein
</span><span class="sxs-lookup"><span data-stu-id="abe74-1906">No-Fuehrerschein</span></span> 
- <span data-ttu-id="abe74-1907">N-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="abe74-1907">N-Führerschein</span></span> 
- <span data-ttu-id="abe74-1908">N-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="abe74-1908">N-Fuhrerschein</span></span> 
- <span data-ttu-id="abe74-1909">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="abe74-1909">N-Fuehrerschein</span></span>
- <span data-ttu-id="abe74-1910">
Nr-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="abe74-1910">Nr-Führerschein</span></span> 
- <span data-ttu-id="abe74-1911">Nr-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="abe74-1911">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="abe74-1912">Nr-Fuehrerschein
</span><span class="sxs-lookup"><span data-stu-id="abe74-1912">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="abe74-1913">No-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="abe74-1913">No-Führerschein</span></span> 
- <span data-ttu-id="abe74-1914">No-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="abe74-1914">No-Fuhrerschein</span></span> 
- <span data-ttu-id="abe74-1915">No-Fuehrerschein
</span><span class="sxs-lookup"><span data-stu-id="abe74-1915">No-Fuehrerschein</span></span> 
- <span data-ttu-id="abe74-1916">N-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="abe74-1916">N-Führerschein</span></span> 
- <span data-ttu-id="abe74-1917">N-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="abe74-1917">N-Fuhrerschein</span></span> 
- <span data-ttu-id="abe74-1918">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="abe74-1918">N-Fuehrerschein</span></span> 

#### <a name="keywordgermandriverslicense"></a><span data-ttu-id="abe74-1919">Keyword_german_drivers_license</span><span class="sxs-lookup"><span data-stu-id="abe74-1919">Keyword_german_drivers_license</span></span>

- <span data-ttu-id="abe74-1920">ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="abe74-1920">ausstellungsdatum</span></span>
- <span data-ttu-id="abe74-1921">
ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="abe74-1921">ausstellungsort</span></span>
- <span data-ttu-id="abe74-1922">
ausstellende behöde</span><span class="sxs-lookup"><span data-stu-id="abe74-1922">ausstellende behöde</span></span>
- <span data-ttu-id="abe74-1923">
ausstellende behorde</span><span class="sxs-lookup"><span data-stu-id="abe74-1923">ausstellende behorde</span></span>
- <span data-ttu-id="abe74-1924">

ausstellende behoerde</span><span class="sxs-lookup"><span data-stu-id="abe74-1924">ausstellende behoerde</span></span>
   
## <a name="german-passport-number"></a><span data-ttu-id="abe74-1925">Numéro de passeport Allemagne</span><span class="sxs-lookup"><span data-stu-id="abe74-1925">German Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-1926">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-1926">Format</span></span>

<span data-ttu-id="abe74-1927">10 chiffres ou lettres</span><span class="sxs-lookup"><span data-stu-id="abe74-1927">10 digits or letters</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-1928">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-1928">Pattern</span></span>

<span data-ttu-id="abe74-1929">Le modèle doit inclure tous les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="abe74-1929">Pattern must include all of the following:</span></span>
- <span data-ttu-id="abe74-1930">Le premier caractère est un chiffre ou une lettre de cet ensemble (C, F, G, H, J, K)</span><span class="sxs-lookup"><span data-stu-id="abe74-1930">First character is a digit or a letter from this set (C, F, G, H, J, K)</span></span> 
- <span data-ttu-id="abe74-1931">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-1931">Three digits</span></span> 
- <span data-ttu-id="abe74-1932">Cinq chiffres ou lettres à partir de cet ensemble (C, -H, J-N, P, R, T, V-Z)</span><span class="sxs-lookup"><span data-stu-id="abe74-1932">Five digits or letters from this set (C, -H, J-N, P, R, T, V-Z)</span></span> 
- <span data-ttu-id="abe74-1933">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="abe74-1933">A digit</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-1934">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-1934">Checksum</span></span>

<span data-ttu-id="abe74-1935">Oui</span><span class="sxs-lookup"><span data-stu-id="abe74-1935">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-1936">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-1936">Definition</span></span>

<span data-ttu-id="abe74-1937">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-1937">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-1938">La fonction Func_german_passport trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-1938">The function Func_german_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-1939">Un mot clé présent dans l’une des cinq listes de mots clés est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-1939">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="abe74-1940">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-1940">The checksum passes.</span></span>

<span data-ttu-id="abe74-1941">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-1941">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-1942">La fonction Func_german_passport_data trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-1942">The function Func_german_passport_data finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-1943">Un mot clé présent dans l’une des cinq listes de mots clés est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-1943">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="abe74-1944">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-1944">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-1945">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-1945">Keywords</span></span>

#### <a name="keywordgermanpassport"></a><span data-ttu-id="abe74-1946">Keyword_german_passport</span><span class="sxs-lookup"><span data-stu-id="abe74-1946">Keyword_german_passport</span></span>

- <span data-ttu-id="abe74-1947">reisepass</span><span class="sxs-lookup"><span data-stu-id="abe74-1947">reisepass</span></span>
- <span data-ttu-id="abe74-1948">
reisepasse</span><span class="sxs-lookup"><span data-stu-id="abe74-1948">reisepasse</span></span>
- <span data-ttu-id="abe74-1949">
reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="abe74-1949">reisepassnummer</span></span>
- <span data-ttu-id="abe74-1950">passeport</span><span class="sxs-lookup"><span data-stu-id="abe74-1950">passport</span></span>
- <span data-ttu-id="abe74-1951">

passports</span><span class="sxs-lookup"><span data-stu-id="abe74-1951">passports</span></span>

#### <a name="keywordgermanpassportcollaborative"></a><span data-ttu-id="abe74-1952">Keyword_german_passport_collaborative</span><span class="sxs-lookup"><span data-stu-id="abe74-1952">Keyword_german_passport_collaborative</span></span>

- <span data-ttu-id="abe74-1953">geburtsdatum</span><span class="sxs-lookup"><span data-stu-id="abe74-1953">geburtsdatum</span></span>
- <span data-ttu-id="abe74-1954">ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="abe74-1954">ausstellungsdatum</span></span>
- <span data-ttu-id="abe74-1955">
ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="abe74-1955">ausstellungsort</span></span>

#### <a name="keywordgermanpassportnumber"></a><span data-ttu-id="abe74-1956">Keyword_german_passport_number</span><span class="sxs-lookup"><span data-stu-id="abe74-1956">Keyword_german_passport_number</span></span>

<span data-ttu-id="abe74-1957">Non-Nr Reisepass-Reisepass</span><span class="sxs-lookup"><span data-stu-id="abe74-1957">No-Reisepass Nr-Reisepass</span></span>

#### <a name="keywordgermanpassport1"></a><span data-ttu-id="abe74-1958">Keyword_german_passport1</span><span class="sxs-lookup"><span data-stu-id="abe74-1958">Keyword_german_passport1</span></span>

<span data-ttu-id="abe74-1959">Reisepass-Nr
</span><span class="sxs-lookup"><span data-stu-id="abe74-1959">Reisepass-Nr</span></span>

#### <a name="keywordgermanpassport2"></a><span data-ttu-id="abe74-1960">Keyword_german_passport2</span><span class="sxs-lookup"><span data-stu-id="abe74-1960">Keyword_german_passport2</span></span>

<span data-ttu-id="abe74-1961">bnationalit.t</span><span class="sxs-lookup"><span data-stu-id="abe74-1961">bnationalit.t</span></span>
   
## <a name="germany-identity-card-number"></a><span data-ttu-id="abe74-1962">Numéro de carte d’identité allemand</span><span class="sxs-lookup"><span data-stu-id="abe74-1962">Germany Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-1963">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-1963">Format</span></span>

<span data-ttu-id="abe74-1964">Depuis le 1er novembre 2010 : neuf lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-1964">Since 1 November 2010: Nine letters and digits</span></span>

<span data-ttu-id="abe74-1965">À partir du 1er avril 1987 jusqu'à 31 octobre 2010:10 chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-1965">From 1 April 1987 until 31 October 2010: 10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-1966">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-1966">Pattern</span></span>

<span data-ttu-id="abe74-1967">Depuis le 1er novembre 2010 :</span><span class="sxs-lookup"><span data-stu-id="abe74-1967">Since 1 November 2010:</span></span>
- <span data-ttu-id="abe74-1968">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="abe74-1968">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="abe74-1969">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-1969">Eight digits</span></span>

<span data-ttu-id="abe74-1970">À partir du 1er avril 1987 jusqu’au 31 octobre 2010 :</span><span class="sxs-lookup"><span data-stu-id="abe74-1970">From 1 April 1987 until 31 October 2010:</span></span>
- <span data-ttu-id="abe74-1971">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-1971">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-1972">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-1972">Checksum</span></span>

<span data-ttu-id="abe74-1973">Non</span><span class="sxs-lookup"><span data-stu-id="abe74-1973">No</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-1974">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-1974">Definition</span></span>

<span data-ttu-id="abe74-1975">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-1975">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-1976">L’expression régulière Regex_germany_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-1976">The regular expression Regex_germany_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-1977">Un mot clé figurant dans la liste Keyword_germany_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-1977">A keyword from Keyword_germany_id_card is found.</span></span>

```
<!-- Germany Identity Card Number -->
<Entity id="e577372f-c42e-47a0-9d85-bebed1c237d4" recommendedConfidence="65" patternsProximity="300">
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Regex_germany_id_card"/>
     <Match idRef="Keyword_germany_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe74-1978">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-1978">Keywords</span></span>

#### <a name="keywordgermanyidcard"></a><span data-ttu-id="abe74-1979">Keyword_germany_id_card</span><span class="sxs-lookup"><span data-stu-id="abe74-1979">Keyword_germany_id_card</span></span>

- <span data-ttu-id="abe74-1980">Identity Card</span><span class="sxs-lookup"><span data-stu-id="abe74-1980">Identity Card</span></span>
- <span data-ttu-id="abe74-1981">ID</span><span class="sxs-lookup"><span data-stu-id="abe74-1981">ID</span></span>
- <span data-ttu-id="abe74-1982">Identification</span><span class="sxs-lookup"><span data-stu-id="abe74-1982">Identification</span></span>
- <span data-ttu-id="abe74-1983">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="abe74-1983">Personalausweis</span></span>
- <span data-ttu-id="abe74-1984">Identifizierungsnummer</span><span class="sxs-lookup"><span data-stu-id="abe74-1984">Identifizierungsnummer</span></span>
- <span data-ttu-id="abe74-1985">Ausweis</span><span class="sxs-lookup"><span data-stu-id="abe74-1985">Ausweis</span></span>
- <span data-ttu-id="abe74-1986">Identifikation</span><span class="sxs-lookup"><span data-stu-id="abe74-1986">Identifikation</span></span>
   
## <a name="greece-national-id-card"></a><span data-ttu-id="abe74-1987">Carte d’identité nationale Grèce</span><span class="sxs-lookup"><span data-stu-id="abe74-1987">Greece National ID Card</span></span>

### <a name="format"></a><span data-ttu-id="abe74-1988">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-1988">Format</span></span>

<span data-ttu-id="abe74-1989">Combinaison de 7 ou 8 lettres et chiffres, plus un tiret</span><span class="sxs-lookup"><span data-stu-id="abe74-1989">Combination of 7-8 letters and numbers plus a dash</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-1990">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-1990">Pattern</span></span>

<span data-ttu-id="abe74-1991">Sept lettres et chiffres (ancien format) :</span><span class="sxs-lookup"><span data-stu-id="abe74-1991">Seven letters and numbers (old format):</span></span>
- <span data-ttu-id="abe74-1992">Une lettre (de l’alphabet grec) </span><span class="sxs-lookup"><span data-stu-id="abe74-1992">One letter (any letter of the Greek alphabet)</span></span> 
- <span data-ttu-id="abe74-1993">Un tiret</span><span class="sxs-lookup"><span data-stu-id="abe74-1993">A dash</span></span> 
- <span data-ttu-id="abe74-1994">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-1994">Six digits</span></span>

<span data-ttu-id="abe74-1995">Huit lettres et chiffres (nouveau format) :</span><span class="sxs-lookup"><span data-stu-id="abe74-1995">Eight letters and numbers (new format):</span></span>
- <span data-ttu-id="abe74-1996">Deux lettres dont le caractère majuscule figure à la fois dans l’alphabet grec et l’alphabet latin (ABEZHIKMNOPTYX) </span><span class="sxs-lookup"><span data-stu-id="abe74-1996">Two letters whose uppercase character occurs in both the Greek and Latin alphabets (ABEZHIKMNOPTYX)</span></span> 
- <span data-ttu-id="abe74-1997">Un tiret</span><span class="sxs-lookup"><span data-stu-id="abe74-1997">A dash</span></span> 
- <span data-ttu-id="abe74-1998">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-1998">Six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-1999">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-1999">Checksum</span></span>

<span data-ttu-id="abe74-2000">Non</span><span class="sxs-lookup"><span data-stu-id="abe74-2000">No</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-2001">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-2001">Definition</span></span>

<span data-ttu-id="abe74-2002">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2002">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2003">L’expression régulière Regex_greece_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2003">The regular expression Regex_greece_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2004">Un mot clé figurant dans la liste Keyword_greece_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-2004">A keyword from Keyword_greece_id_card is found.</span></span>

```
<!-- Greece National ID Card -->
<Entity id="82568215-1da1-46d3-874a-d2294d81b5ac" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_greece_id_card"/>
     <Match idRef="Keyword_greece_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe74-2005">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-2005">Keywords</span></span>

#### <a name="keywordgreeceidcard"></a><span data-ttu-id="abe74-2006">Keyword_greece_id_card</span><span class="sxs-lookup"><span data-stu-id="abe74-2006">Keyword_greece_id_card</span></span>

- <span data-ttu-id="abe74-2007">Greek identity Card</span><span class="sxs-lookup"><span data-stu-id="abe74-2007">Greek identity Card</span></span>
- <span data-ttu-id="abe74-2008">Tautotita</span><span class="sxs-lookup"><span data-stu-id="abe74-2008">Tautotita</span></span>
- <span data-ttu-id="abe74-2009">Δελτίο αστυνομικής ταυτότητας</span><span class="sxs-lookup"><span data-stu-id="abe74-2009">Δελτίο αστυνομικής ταυτότητας</span></span>
- <span data-ttu-id="abe74-2010">Ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="abe74-2010">Ταυτότητα</span></span>
   
## <a name="hong-kong-identity-card-hkid-number"></a><span data-ttu-id="abe74-2011">Numéro de carte d’identité (HKID) Hong Kong</span><span class="sxs-lookup"><span data-stu-id="abe74-2011">Hong Kong Identity Card (HKID) Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-2012">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-2012">Format</span></span>

<span data-ttu-id="abe74-2013">Combinaison de 8 ou 9 lettres et chiffres plus éventuellement des parenthèses autour du dernier caractère</span><span class="sxs-lookup"><span data-stu-id="abe74-2013">Combination of 8-9 letters and numbers plus optional parentheses around the final character</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-2014">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-2014">Pattern</span></span>

<span data-ttu-id="abe74-2015">Combinaison de 8 ou 9 lettres :</span><span class="sxs-lookup"><span data-stu-id="abe74-2015">Combination of 8-9 letters:</span></span>
- <span data-ttu-id="abe74-2016">1 ou 2 lettres (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="abe74-2016">1-2 letters (not case sensitive)</span></span> 
- <span data-ttu-id="abe74-2017">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2017">Six digits</span></span> 
- <span data-ttu-id="abe74-2018">Le dernier caractère (un chiffre ou la lettre A), qui est le chiffre de contrôle et est éventuellement entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="abe74-2018">The final character (any digit or the letter A), which is the check digit and is optionally enclosed in parentheses.</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-2019">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-2019">Checksum</span></span>

<span data-ttu-id="abe74-2020">Oui</span><span class="sxs-lookup"><span data-stu-id="abe74-2020">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-2021">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-2021">Definition</span></span>

<span data-ttu-id="abe74-2022">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2022">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2023">La fonction Func_hong_kong_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2023">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2024">Un mot clé figurant dans la liste Keyword_hong_kong_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-2024">A keyword from Keyword_hong_kong_id_card is found.</span></span>
- <span data-ttu-id="abe74-2025">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-2025">The checksum passes.</span></span>

<span data-ttu-id="abe74-2026">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2026">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2027">La fonction Func_hong_kong_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2027">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2028">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-2028">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-2029">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-2029">Keywords</span></span>

#### <a name="keywordhongkongidcard"></a><span data-ttu-id="abe74-2030">Keyword_hong_kong_id_card</span><span class="sxs-lookup"><span data-stu-id="abe74-2030">Keyword_hong_kong_id_card</span></span>

- <span data-ttu-id="abe74-2031">Hong Kong Identity Card</span><span class="sxs-lookup"><span data-stu-id="abe74-2031">Hong Kong Identity Card</span></span>
- <span data-ttu-id="abe74-2032">HKID</span><span class="sxs-lookup"><span data-stu-id="abe74-2032">HKID</span></span>
- <span data-ttu-id="abe74-2033">ID card</span><span class="sxs-lookup"><span data-stu-id="abe74-2033">ID card</span></span>
- <span data-ttu-id="abe74-2034">香港身份證
</span><span class="sxs-lookup"><span data-stu-id="abe74-2034">香港身份證</span></span> 
- <span data-ttu-id="abe74-2035">香港永久性居民身份證
</span><span class="sxs-lookup"><span data-stu-id="abe74-2035">香港永久性居民身份證</span></span> 
   
## <a name="india-permanent-account-number-pan"></a><span data-ttu-id="abe74-2036">Numéro de compte permanent Inde</span><span class="sxs-lookup"><span data-stu-id="abe74-2036">India Permanent Account Number (PAN)</span></span>

### <a name="format"></a><span data-ttu-id="abe74-2037">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-2037">Format</span></span>

<span data-ttu-id="abe74-2038">10 lettres ou chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2038">10 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-2039">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-2039">Pattern</span></span>

<span data-ttu-id="abe74-2040">10 lettres ou chiffres :</span><span class="sxs-lookup"><span data-stu-id="abe74-2040">10 letters or digits:</span></span>
- <span data-ttu-id="abe74-2041">Cinq lettres (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="abe74-2041">Five letters (not case sensitive)</span></span> 
- <span data-ttu-id="abe74-2042">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2042">Four digits</span></span> 
- <span data-ttu-id="abe74-2043">Une lettre qui est un chiffre de contrôle alphabétique</span><span class="sxs-lookup"><span data-stu-id="abe74-2043">A letter which is an alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-2044">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-2044">Checksum</span></span>

<span data-ttu-id="abe74-2045">Oui</span><span class="sxs-lookup"><span data-stu-id="abe74-2045">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-2046">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-2046">Definition</span></span>

<span data-ttu-id="abe74-2047">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2047">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2048">L’expression régulière Regex_india_permanent_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2048">The regular expression Regex_india_permanent_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2049">Un mot clé figurant dans la liste Keyword_india_permanent_account_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-2049">A keyword from Keyword_india_permanent_account_number is found.</span></span>
- <span data-ttu-id="abe74-2050">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-2050">The checksum passes.</span></span>

```
<!-- India Permanent Account Number -->
<Entity id="2602bfee-9bb0-47a5-a7a6-2bf3053e2804" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_india_permanent_account_number"/>
     <Match idRef="Keyword_india_permanent_account_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe74-2051">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-2051">Keywords</span></span>

#### <a name="keywordindiapermanentaccountnumber"></a><span data-ttu-id="abe74-2052">Keyword_india_permanent_account_number</span><span class="sxs-lookup"><span data-stu-id="abe74-2052">Keyword_india_permanent_account_number</span></span>

- <span data-ttu-id="abe74-2053">Permanent Account Number
</span><span class="sxs-lookup"><span data-stu-id="abe74-2053">Permanent Account Number</span></span> 
- <span data-ttu-id="abe74-2054">PAN
</span><span class="sxs-lookup"><span data-stu-id="abe74-2054">PAN</span></span> 
   
## <a name="india-unique-identification-aadhaar-number"></a><span data-ttu-id="abe74-2055">Numéro d’identification unique (Aadhaar) Inde</span><span class="sxs-lookup"><span data-stu-id="abe74-2055">India Unique Identification (Aadhaar) Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-2056">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-2056">Format</span></span>

<span data-ttu-id="abe74-2057">12 chiffres contenant éventuellement des espaces ou des tirets</span><span class="sxs-lookup"><span data-stu-id="abe74-2057">12 digits containing optional spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-2058">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-2058">Pattern</span></span>

<span data-ttu-id="abe74-2059">12 chiffres :</span><span class="sxs-lookup"><span data-stu-id="abe74-2059">12 digits:</span></span>
- <span data-ttu-id="abe74-2060">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2060">Four digits</span></span> 
- <span data-ttu-id="abe74-2061">Éventuellement un tiret ou un espace </span><span class="sxs-lookup"><span data-stu-id="abe74-2061">An optional space or dash</span></span> 
- <span data-ttu-id="abe74-2062">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2062">Four digits</span></span> 
- <span data-ttu-id="abe74-2063">Éventuellement un tiret ou un espace </span><span class="sxs-lookup"><span data-stu-id="abe74-2063">An optional space or dash</span></span> 
- <span data-ttu-id="abe74-2064">Le chiffre final, qui est le chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-2064">The final digit which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-2065">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-2065">Checksum</span></span>

<span data-ttu-id="abe74-2066">Oui</span><span class="sxs-lookup"><span data-stu-id="abe74-2066">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-2067">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-2067">Definition</span></span>

<span data-ttu-id="abe74-p133">Une stratégie DLP est de 85 % convaincu que ce type d’informations sensibles a été détecté if, au sein d’une proximité de 300 caractères : la fonction Func_india_aadhaar recherche le contenu qui correspond au modèle. Un mot clé à partir de Keyword_india_aadhar est trouvé. Passe de la somme de contrôle. Une stratégie DLP est convaincu que ce type d’informations sensibles a été détecté à 75 % if, au sein d’une proximité de 300 caractères : la fonction Func_india_aadhaar recherche le contenu qui correspond au modèle. Passe de la somme de contrôle. <!-- India Unique Identification (Aadhaar) number -->
<Entity id="1ca46b29-76f5-4f46-9383-cfa15e91048f" recommendedConfidence="85" patternsProximity="300"> <Pattern confidenceLevel="85"> <IdMatch idRef="Func_india_aadhaar"/> <Match idRef="Keyword_india_aadhar"/> </Pattern> <Pattern confidenceLevel="75"> <IdMatch idRef="Func_india_aadhaar"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="abe74-p133">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern. A keyword from Keyword_india_aadhar is found. The checksum passes. A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern. The checksum passes. <!-- India Unique Identification (Aadhaar) number -->
<Entity id="1ca46b29-76f5-4f46-9383-cfa15e91048f" recommendedConfidence="85" patternsProximity="300"> <Pattern confidenceLevel="85"> <IdMatch idRef="Func_india_aadhaar"/> <Match idRef="Keyword_india_aadhar"/> </Pattern> <Pattern confidenceLevel="75"> <IdMatch idRef="Func_india_aadhaar"/> </Pattern>
</Entity></span></span>

### <a name="keywords"></a><span data-ttu-id="abe74-2074">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-2074">Keywords</span></span>
   
#### <a name="keywordindiaaadhar"></a><span data-ttu-id="abe74-2075">Keyword_india_aadhar</span><span class="sxs-lookup"><span data-stu-id="abe74-2075">Keyword_india_aadhar</span></span>
- <span data-ttu-id="abe74-2076">Aadhar</span><span class="sxs-lookup"><span data-stu-id="abe74-2076">Aadhar</span></span>
- <span data-ttu-id="abe74-2077">Aadhaar</span><span class="sxs-lookup"><span data-stu-id="abe74-2077">Aadhaar</span></span>
- <span data-ttu-id="abe74-2078">UID</span><span class="sxs-lookup"><span data-stu-id="abe74-2078">UID</span></span>
- <span data-ttu-id="abe74-2079">आधार</span><span class="sxs-lookup"><span data-stu-id="abe74-2079">आधार</span></span>
   
## <a name="indonesia-identity-card-ktp-number"></a><span data-ttu-id="abe74-2080">Numéro de carte d’identité (KTP) Indonésie</span><span class="sxs-lookup"><span data-stu-id="abe74-2080">Indonesia Identity Card (KTP) Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-2081">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-2081">Format</span></span>

<span data-ttu-id="abe74-2082">16 chiffres contenant éventuellement des points</span><span class="sxs-lookup"><span data-stu-id="abe74-2082">16 digits containing optional periods</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-2083">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-2083">Pattern</span></span>

<span data-ttu-id="abe74-2084">16 chiffres :</span><span class="sxs-lookup"><span data-stu-id="abe74-2084">16 digits:</span></span>
- <span data-ttu-id="abe74-2085">Code à deux chiffres désignant la province </span><span class="sxs-lookup"><span data-stu-id="abe74-2085">Two-digit province code</span></span> 
- <span data-ttu-id="abe74-2086">Un point (facultatif) </span><span class="sxs-lookup"><span data-stu-id="abe74-2086">A period (optional)</span></span> 
- <span data-ttu-id="abe74-2087">Code à deux chiffres désignant une régence ou une ville </span><span class="sxs-lookup"><span data-stu-id="abe74-2087">Two-digit regency or city code</span></span> 
- <span data-ttu-id="abe74-2088">Code à deux chiffres désignant un sous-district </span><span class="sxs-lookup"><span data-stu-id="abe74-2088">Two-digit subdistrict code</span></span> 
- <span data-ttu-id="abe74-2089">Un point (facultatif) </span><span class="sxs-lookup"><span data-stu-id="abe74-2089">A period (optional)</span></span> 
- <span data-ttu-id="abe74-2090">Six chiffres au format JJMMAA qui correspondent à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="abe74-2090">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="abe74-2091">Un point (facultatif) </span><span class="sxs-lookup"><span data-stu-id="abe74-2091">A period (optional)</span></span> 
- <span data-ttu-id="abe74-2092">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2092">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-2093">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-2093">Checksum</span></span>

<span data-ttu-id="abe74-2094">Non</span><span class="sxs-lookup"><span data-stu-id="abe74-2094">No</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-2095">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-2095">Definition</span></span>

<span data-ttu-id="abe74-2096">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2096">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2097">L’expression régulière Regex_indonesia_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2097">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2098">Un mot clé figurant dans la liste Keyword_indonesia_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-2098">A keyword from Keyword_indonesia_id_card is found.</span></span>

<span data-ttu-id="abe74-2099">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2099">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2100">L’expression régulière Regex_indonesia_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2100">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-2101">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-2101">Keywords</span></span>
   
#### <a name="keywordindonesiaidcard"></a><span data-ttu-id="abe74-2102">Keyword_indonesia_id_card</span><span class="sxs-lookup"><span data-stu-id="abe74-2102">Keyword_indonesia_id_card</span></span>

- <span data-ttu-id="abe74-2103">KTP</span><span class="sxs-lookup"><span data-stu-id="abe74-2103">KTP</span></span>
- <span data-ttu-id="abe74-2104">Kartu Tanda Penduduk
</span><span class="sxs-lookup"><span data-stu-id="abe74-2104">Kartu Tanda Penduduk</span></span> 
- <span data-ttu-id="abe74-2105">Nomor Induk Kependudukan
</span><span class="sxs-lookup"><span data-stu-id="abe74-2105">Nomor Induk Kependudukan</span></span> 
   
## <a name="international-banking-account-number-iban"></a><span data-ttu-id="abe74-2106">Numéro de compte bancaire international (IBAN)</span><span class="sxs-lookup"><span data-stu-id="abe74-2106">International Banking Account Number (IBAN)</span></span>

### <a name="format"></a><span data-ttu-id="abe74-2107">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-2107">Format</span></span>

<span data-ttu-id="abe74-2108">Code pays (à deux lettres) plus chiffres de contrôle (à deux chiffres) plus numéro BBAN (jusqu’à 30 chiffres)</span><span class="sxs-lookup"><span data-stu-id="abe74-2108">Country code (two letters) plus check digits (two digits) plus bban number (up to 30 characters)</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-2109">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-2109">Pattern</span></span>

<span data-ttu-id="abe74-2110">Le modèle doit inclure tous les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="abe74-2110">Pattern must include all of the following:</span></span>

- <span data-ttu-id="abe74-2111">Code pays à deux lettres</span><span class="sxs-lookup"><span data-stu-id="abe74-2111">Two-letter country code</span></span>
- <span data-ttu-id="abe74-2112">Deux chiffres de contrôle (suivis d’un espace facultatif) </span><span class="sxs-lookup"><span data-stu-id="abe74-2112">Two check digits (followed by an optional space)</span></span> 
- <span data-ttu-id="abe74-2113">1 à 7 groupes de quatre lettres ou chiffres (séparés par des espaces facultatifs)</span><span class="sxs-lookup"><span data-stu-id="abe74-2113">1-7 groups of four letters or digits (can be separated by spaces)</span></span>
- <span data-ttu-id="abe74-2114">1 à 3 lettres ou chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2114">1-3 letters or digits</span></span>

<span data-ttu-id="abe74-p134">Le format pour chaque pays est légèrement différent. Le type d’informations sensibles IBAN recouvre ces 60 pays :</span><span class="sxs-lookup"><span data-stu-id="abe74-p134">The format for each country is slightly different. The IBAN sensitive information type covers these 60 countries:</span></span>

<span data-ttu-id="abe74-2117">ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg</span><span class="sxs-lookup"><span data-stu-id="abe74-2117">ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-2118">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-2118">Checksum</span></span>

<span data-ttu-id="abe74-2119">Oui</span><span class="sxs-lookup"><span data-stu-id="abe74-2119">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-2120">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-2120">Definition</span></span>

<span data-ttu-id="abe74-2121">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2121">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2122">La fonction Func_iban trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2122">The function Func_iban finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2123">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-2123">The checksum passes.</span></span>

```
<Entity id="e7dc4711-11b7-4cb0-b88b-2c394a771f0e" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_iban" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe74-2124">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-2124">Keywords</span></span>

<span data-ttu-id="abe74-2125">Aucun</span><span class="sxs-lookup"><span data-stu-id="abe74-2125">None</span></span>

   
## <a name="ip-address"></a><span data-ttu-id="abe74-2126">Adresse IP</span><span class="sxs-lookup"><span data-stu-id="abe74-2126">IP Address</span></span>

### <a name="format"></a><span data-ttu-id="abe74-2127">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-2127">Format</span></span>

#### <a name="ipv4"></a><span data-ttu-id="abe74-2128">IPv4 :</span><span class="sxs-lookup"><span data-stu-id="abe74-2128">IPv4:</span></span>
<span data-ttu-id="abe74-2129">Modèle complexe qui tient compte des versions mises en forme (points) et non mises en forme (sans points) des adresses IPv4</span><span class="sxs-lookup"><span data-stu-id="abe74-2129">Complex pattern which accounts for formatted (periods) and unformatted (no periods) versions of the IPv4 addresses</span></span>

#### <a name="ipv6"></a><span data-ttu-id="abe74-2130">IPv6 :</span><span class="sxs-lookup"><span data-stu-id="abe74-2130">IPv6:</span></span>
<span data-ttu-id="abe74-2131"> Modèle complexe qui tient compte des numéros IPv6 mis en forme (qui incluent les signes deux-points)</span><span class="sxs-lookup"><span data-stu-id="abe74-2131">Complex pattern which accounts for formatted IPv6 numbers (which include colons)</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-2132">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-2132">Pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-2133">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-2133">Checksum</span></span>

<span data-ttu-id="abe74-2134">Non</span><span class="sxs-lookup"><span data-stu-id="abe74-2134">No</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-2135">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-2135">Definition</span></span>

<span data-ttu-id="abe74-2136">Pour IPv6, le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2136">For IPv6, a DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2137">L’expression régulière Regex_ipv6_address trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2137">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2138">Aucun mot clé figurant dans la liste Keyword_ipaddress n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-2138">No keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="abe74-2139">Pour IPv4, le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 95 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2139">For IPv4, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2140">L’expression régulière Regex_ipv4_address trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2140">The regular expression Regex_ipv4_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2141">Un mot clé figurant dans la liste Keyword_ipaddress est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-2141">A keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="abe74-2142">Pour IPv6, le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 95 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2142">For IPv6, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2143">L’expression régulière Regex_ipv6_address trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2143">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2144">Aucun mot clé figurant dans la liste Keyword_ipaddress n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-2144">No keyword from Keyword_ipaddress is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-2145">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-2145">Keywords</span></span>

#### <a name="keywordipaddress"></a><span data-ttu-id="abe74-2146">Keyword_ipaddress</span><span class="sxs-lookup"><span data-stu-id="abe74-2146">Keyword_ipaddress</span></span>

- <span data-ttu-id="abe74-2147">IP (ce mot clé respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="abe74-2147">IP (this keyword is case sensitive)</span></span>
- <span data-ttu-id="abe74-2148">ip address
</span><span class="sxs-lookup"><span data-stu-id="abe74-2148">ip address</span></span> 
- <span data-ttu-id="abe74-2149">adresses IP</span><span class="sxs-lookup"><span data-stu-id="abe74-2149">ip addresses</span></span>
- <span data-ttu-id="abe74-2150">protocole internet</span><span class="sxs-lookup"><span data-stu-id="abe74-2150">internet protocol</span></span>
- <span data-ttu-id="abe74-2151">
IP-כתובת ה
</span><span class="sxs-lookup"><span data-stu-id="abe74-2151">IP-כתובת ה</span></span> 
   
## <a name="international-classification-of-diseases-icd-10-cm"></a><span data-ttu-id="abe74-2152">Classification internationale de maux (ICD-10 CM)</span><span class="sxs-lookup"><span data-stu-id="abe74-2152">International Classification of Diseases (ICD-10-CM)</span></span>

### <a name="format"></a><span data-ttu-id="abe74-2153">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-2153">Format</span></span>

<span data-ttu-id="abe74-2154">Dictionnaire</span><span class="sxs-lookup"><span data-stu-id="abe74-2154">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-2155">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-2155">Pattern</span></span>

<span data-ttu-id="abe74-2156">Mot clé</span><span class="sxs-lookup"><span data-stu-id="abe74-2156">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-2157">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-2157">Checksum</span></span>

<span data-ttu-id="abe74-2158">Non</span><span class="sxs-lookup"><span data-stu-id="abe74-2158">No</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-2159">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-2159">Definition</span></span>

<span data-ttu-id="abe74-2160">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2160">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2161">Un mot clé à partir de Dictionary_icd_10_cm est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-2161">A keyword from Dictionary_icd_10_cm is found.</span></span>

```
      <!-- ICD-10 CM -->
      <Entity id="3356946c-6bb7-449b-b253-6ffa419c0ce7" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_10_cm" />
        </Pattern>
      </Entity>
```

<span data-ttu-id="abe74-2162">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="abe74-2162">Keywords</span></span>

<span data-ttu-id="abe74-p135">Les termes à partir du dictionnaire de mot clé Dictionary_icd_10_cm, qui repose sur [International Classification de maux, révision dixième, Modification cliniques (ICD-10-CM)](https://go.microsoft.com/fwlink/?linkid=852604). Ce type de recherche uniquement le terme, pas les codes d’assurance.</span><span class="sxs-lookup"><span data-stu-id="abe74-p135">Any term from the Dictionary_icd_10_cm keyword dictionary, which is based on the [International Classification of Diseases, Tenth Revision, Clinical Modification (ICD-10-CM)](https://go.microsoft.com/fwlink/?linkid=852604). This type looks only for the term, not the insurance codes.</span></span>

   
## <a name="international-classification-of-diseases-icd-9-cm"></a><span data-ttu-id="abe74-2165">Classification internationale de maux (ICD-9-CM)</span><span class="sxs-lookup"><span data-stu-id="abe74-2165">International Classification of Diseases (ICD-9-CM)</span></span>

### <a name="format"></a><span data-ttu-id="abe74-2166">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-2166">Format</span></span>

<span data-ttu-id="abe74-2167">Dictionnaire</span><span class="sxs-lookup"><span data-stu-id="abe74-2167">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-2168">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-2168">Pattern</span></span>

<span data-ttu-id="abe74-2169">Mot clé</span><span class="sxs-lookup"><span data-stu-id="abe74-2169">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-2170">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-2170">Checksum</span></span>

<span data-ttu-id="abe74-2171">Non</span><span class="sxs-lookup"><span data-stu-id="abe74-2171">No</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-2172">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-2172">Definition</span></span>

<span data-ttu-id="abe74-2173">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2173">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2174">Un mot clé à partir de Dictionary_icd_9_cm est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-2174">A keyword from Dictionary_icd_9_cm is found.</span></span>

```
      <Entity id="fa3f9c74-ee07-4c52-b5f2-085d6b2c0ec4" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_9_cm" />
        </Pattern>
      </Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe74-2175">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="abe74-2175">Keywords</span></span>

<span data-ttu-id="abe74-p136">Les termes à partir du dictionnaire de mot clé Dictionary_icd_9_cm, qui repose sur [International Classification de maux, révision neuvième, Modification cliniques (ICD-9-CM)](https://go.microsoft.com/fwlink/?linkid=852605). Ce type de recherche uniquement le terme, pas les codes d’assurance.</span><span class="sxs-lookup"><span data-stu-id="abe74-p136">Any term from the Dictionary_icd_9_cm keyword dictionary, which is based on the [International Classification of Diseases,Ninth Revision, Clinical Modification (ICD-9-CM)](https://go.microsoft.com/fwlink/?linkid=852605). This type looks only for the term, not the insurance codes.</span></span>
   
## <a name="ireland-personal-public-service-pps-number"></a><span data-ttu-id="abe74-2178">Numéro de service public personnel (PPS) Irlande</span><span class="sxs-lookup"><span data-stu-id="abe74-2178">Ireland Personal Public Service (PPS) Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-2179">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-2179">Format</span></span>

<span data-ttu-id="abe74-2180">Ancien format (jusqu'à 31 décembre 2012) :</span><span class="sxs-lookup"><span data-stu-id="abe74-2180">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="abe74-2181">Sept chiffres suivis de 1 ou 2 lettres </span><span class="sxs-lookup"><span data-stu-id="abe74-2181">Seven digits followed by 1-2 letters</span></span> 

<span data-ttu-id="abe74-2182">Nouveau format (1er janvier 2013 et une fois) :</span><span class="sxs-lookup"><span data-stu-id="abe74-2182">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="abe74-2183">Sept chiffres suivis de deux lettres</span><span class="sxs-lookup"><span data-stu-id="abe74-2183">Seven digits followed by two letters</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-2184">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-2184">Pattern</span></span>

<span data-ttu-id="abe74-2185">Ancien format (jusqu'à 31 décembre 2012) :</span><span class="sxs-lookup"><span data-stu-id="abe74-2185">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="abe74-2186">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="abe74-2186">Seven digits</span></span> 
- <span data-ttu-id="abe74-2187">1 ou 2 lettres (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="abe74-2187">1-2 letters (not case sensitive)</span></span> 

<span data-ttu-id="abe74-2188">Nouveau format (1er janvier 2013 et une fois) :</span><span class="sxs-lookup"><span data-stu-id="abe74-2188">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="abe74-2189">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="abe74-2189">Seven digits</span></span> 
- <span data-ttu-id="abe74-2190">Une lettre (ne respectant pas la casse), qui est un chiffre de contrôle alphabétique </span><span class="sxs-lookup"><span data-stu-id="abe74-2190">A letter (not case sensitive) which is an alphabetic check digit</span></span> 
- <span data-ttu-id="abe74-2191">La lettre « A » ou « H » (ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="abe74-2191">The letter "A" or "H" (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-2192">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-2192">Checksum</span></span>

<span data-ttu-id="abe74-2193">Oui</span><span class="sxs-lookup"><span data-stu-id="abe74-2193">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-2194">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-2194">Definition</span></span>

<span data-ttu-id="abe74-2195">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2195">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2196">La fonction Func_ireland_pps trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2196">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2197">L’une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="abe74-2197">One of the following is true:</span></span>
    - <span data-ttu-id="abe74-2198">Un mot clé figurant dans la liste Keyword_ireland_pps est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-2198">A keyword from Keyword_ireland_pps is found.</span></span>
    - <span data-ttu-id="abe74-2199">La fonction Func_eu_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="abe74-2199">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="abe74-2200">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-2200">The checksum passes.</span></span>

<span data-ttu-id="abe74-2201">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2201">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2202">La fonction Func_ireland_pps trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2202">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2203">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-2203">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-2204">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-2204">Keywords</span></span>

#### <a name="keywordirelandpps"></a><span data-ttu-id="abe74-2205">Keyword_ireland_pps</span><span class="sxs-lookup"><span data-stu-id="abe74-2205">Keyword_ireland_pps</span></span>

- <span data-ttu-id="abe74-2206">Personal Public Service Number 
</span><span class="sxs-lookup"><span data-stu-id="abe74-2206">Personal Public Service Number</span></span> 
- <span data-ttu-id="abe74-2207">PPS Number
</span><span class="sxs-lookup"><span data-stu-id="abe74-2207">PPS Number</span></span> 
- <span data-ttu-id="abe74-2208">PPS Num
</span><span class="sxs-lookup"><span data-stu-id="abe74-2208">PPS Num</span></span> 
- <span data-ttu-id="abe74-2209">PPS No.
</span><span class="sxs-lookup"><span data-stu-id="abe74-2209">PPS No.</span></span> 
- <span data-ttu-id="abe74-2210">PPS #
</span><span class="sxs-lookup"><span data-stu-id="abe74-2210">PPS #</span></span> 
- <span data-ttu-id="abe74-2211">PPS #</span><span class="sxs-lookup"><span data-stu-id="abe74-2211">PPS#</span></span> 
- <span data-ttu-id="abe74-2212">PPSN
</span><span class="sxs-lookup"><span data-stu-id="abe74-2212">PPSN</span></span> 
- <span data-ttu-id="abe74-2213">Public Services Card
</span><span class="sxs-lookup"><span data-stu-id="abe74-2213">Public Services Card</span></span> 
- <span data-ttu-id="abe74-2214">Uimhir Phearsanta Seirbhíse Poiblí
</span><span class="sxs-lookup"><span data-stu-id="abe74-2214">Uimhir Phearsanta Seirbhíse Poiblí</span></span> 
- <span data-ttu-id="abe74-p137">Uimh. PSP
</span><span class="sxs-lookup"><span data-stu-id="abe74-p137">Uimh. PSP</span></span> 
- <span data-ttu-id="abe74-2217">PSP
</span><span class="sxs-lookup"><span data-stu-id="abe74-2217">PSP</span></span> 
   
## <a name="israel-bank-account-number"></a><span data-ttu-id="abe74-2218">Numéro de compte bancaire Israël</span><span class="sxs-lookup"><span data-stu-id="abe74-2218">Israel Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-2219">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-2219">Format</span></span>

<span data-ttu-id="abe74-2220">13 chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2220">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-2221">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-2221">Pattern</span></span>

<span data-ttu-id="abe74-2222">Mis en forme :</span><span class="sxs-lookup"><span data-stu-id="abe74-2222">Formatted:</span></span>
- <span data-ttu-id="abe74-2223">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2223">Two digits</span></span> 
- <span data-ttu-id="abe74-2224">Un tiret</span><span class="sxs-lookup"><span data-stu-id="abe74-2224">A dash</span></span> 
- <span data-ttu-id="abe74-2225">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2225">Three digits</span></span> 
- <span data-ttu-id="abe74-2226">Un tiret</span><span class="sxs-lookup"><span data-stu-id="abe74-2226">A dash</span></span> 
- <span data-ttu-id="abe74-2227">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2227">Eight digits</span></span>

<span data-ttu-id="abe74-2228">Non mis en forme :</span><span class="sxs-lookup"><span data-stu-id="abe74-2228">Unformatted:</span></span>
- <span data-ttu-id="abe74-2229">	13 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="abe74-2229">13 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-2230">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-2230">Checksum</span></span>

<span data-ttu-id="abe74-2231">Non</span><span class="sxs-lookup"><span data-stu-id="abe74-2231">No</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-2232">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-2232">Definition</span></span>

<span data-ttu-id="abe74-2233">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2233">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2234">L’expression régulière Regex_israel_bank_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2234">The regular expression Regex_israel_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2235">Un mot clé figurant dans la liste Keyword_israel_bank_account_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-2235">A keyword from Keyword_israel_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-2236">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-2236">Keywords</span></span>

#### <a name="keywordisraelbankaccountnumber"></a><span data-ttu-id="abe74-2237">Keyword_israel_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="abe74-2237">Keyword_israel_bank_account_number</span></span>

- <span data-ttu-id="abe74-2238">Numéro de compte bancaire
</span><span class="sxs-lookup"><span data-stu-id="abe74-2238">Bank Account Number</span></span> 
- <span data-ttu-id="abe74-2239">Compte bancaire
</span><span class="sxs-lookup"><span data-stu-id="abe74-2239">Bank Account</span></span> 
- <span data-ttu-id="abe74-2240">Numéro de compte
</span><span class="sxs-lookup"><span data-stu-id="abe74-2240">Account Number</span></span> 
- <span data-ttu-id="abe74-2241">מספר חשבון בנק
</span><span class="sxs-lookup"><span data-stu-id="abe74-2241">מספר חשבון בנק</span></span> 
   
## <a name="israel-national-id"></a><span data-ttu-id="abe74-2242">Carte nationale d'identité Israël</span><span class="sxs-lookup"><span data-stu-id="abe74-2242">Israel National ID</span></span>

### <a name="format"></a><span data-ttu-id="abe74-2243">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-2243">Format</span></span>

<span data-ttu-id="abe74-2244">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2244">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-2245">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-2245">Pattern</span></span>

<span data-ttu-id="abe74-2246">Neuf chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="abe74-2246">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-2247">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-2247">Checksum</span></span>

<span data-ttu-id="abe74-2248">Oui</span><span class="sxs-lookup"><span data-stu-id="abe74-2248">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-2249">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-2249">Definition</span></span>

<span data-ttu-id="abe74-2250">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2251">La fonction Func_israeli_national_id_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2251">The function Func_israeli_national_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2252">Un mot clé figurant dans la liste Keyword_Israel_National_ID est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-2252">A keyword from Keyword_Israel_National_ID is found.</span></span>
- <span data-ttu-id="abe74-2253">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-2253">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-2254">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-2254">Keywords</span></span>

#### <a name="keywordisraelnationalid"></a><span data-ttu-id="abe74-2255">Keyword_Israel_National_ID</span><span class="sxs-lookup"><span data-stu-id="abe74-2255">Keyword_Israel_National_ID</span></span>

- <span data-ttu-id="abe74-2256">מספר זהות
</span><span class="sxs-lookup"><span data-stu-id="abe74-2256">מספר זהות</span></span> 
- <span data-ttu-id="abe74-2257">Numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="abe74-2257">National ID Number</span></span>
   
## <a name="italy-drivers-license-number"></a><span data-ttu-id="abe74-2258">Numéro de permis de conduire Italie</span><span class="sxs-lookup"><span data-stu-id="abe74-2258">Italy Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-2259">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-2259">Format</span></span>

<span data-ttu-id="abe74-2260">Une combinaison de 10 lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2260">A combination of 10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-2261">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-2261">Pattern</span></span>

- <span data-ttu-id="abe74-2262">Une combinaison de 10 lettres et chiffres :</span><span class="sxs-lookup"><span data-stu-id="abe74-2262">A combination of 10 letters and digits:</span></span>
- <span data-ttu-id="abe74-2263">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="abe74-2263">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="abe74-2264">La lettre « A » ou « V » (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="abe74-2264">The letter "A" or "V" (not case sensitive)</span></span> 
- <span data-ttu-id="abe74-2265">Sept lettres (ne respectent pas la casse), des chiffres ou le trait de soulignement</span><span class="sxs-lookup"><span data-stu-id="abe74-2265">Seven letters (not case sensitive), digits, or the underscore character</span></span> 
- <span data-ttu-id="abe74-2266">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="abe74-2266">One letter (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-2267">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-2267">Checksum</span></span>

<span data-ttu-id="abe74-2268">Non</span><span class="sxs-lookup"><span data-stu-id="abe74-2268">No</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-2269">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-2269">Definition</span></span>

<span data-ttu-id="abe74-2270">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2270">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2271">L’expression régulière Regex_italy_drivers_license_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2271">The regular expression Regex_italy_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2272">Un mot clé figurant dans la liste Keyword_italy_drivers_license_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-2272">A keyword from Keyword_italy_drivers_license_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-2273">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-2273">Keywords</span></span>

#### <a name="keyworditalydriverslicensenumber"></a><span data-ttu-id="abe74-2274">Keyword_italy_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="abe74-2274">Keyword_italy_drivers_license_number</span></span>

- <span data-ttu-id="abe74-2275">numero di patente di guida
</span><span class="sxs-lookup"><span data-stu-id="abe74-2275">numero di patente di guida</span></span> 
- <span data-ttu-id="abe74-2276">patente di guida
</span><span class="sxs-lookup"><span data-stu-id="abe74-2276">patente di guida</span></span> 
   
## <a name="japan-bank-account-number"></a><span data-ttu-id="abe74-2277">Numéro de compte bancaire Japon</span><span class="sxs-lookup"><span data-stu-id="abe74-2277">Japan Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-2278">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-2278">Format</span></span>

<span data-ttu-id="abe74-2279">Sept ou huit chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2279">Seven or eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-2280">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-2280">Pattern</span></span>

<span data-ttu-id="abe74-2281">Numéro de compte bancaire :</span><span class="sxs-lookup"><span data-stu-id="abe74-2281">Bank account number:</span></span>
- <span data-ttu-id="abe74-2282">Sept ou huit chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2282">Seven or eight digits</span></span>
- <span data-ttu-id="abe74-2283">Code guichet du compte bancaire :</span><span class="sxs-lookup"><span data-stu-id="abe74-2283">Bank account branch code:</span></span>
- <span data-ttu-id="abe74-2284">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2284">Four digits</span></span> 
- <span data-ttu-id="abe74-2285">Un espace ou un tiret (facultatif)</span><span class="sxs-lookup"><span data-stu-id="abe74-2285">A space or dash (optional)</span></span> 
- <span data-ttu-id="abe74-2286">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2286">Three digits</span></span>

<span data-ttu-id="abe74-2287">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-2287">Checksum</span></span>

<span data-ttu-id="abe74-2288">Non</span><span class="sxs-lookup"><span data-stu-id="abe74-2288">No</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-2289">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-2289">Definition</span></span>

<span data-ttu-id="abe74-2290">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2290">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2291">La fonction Func_jp_bank_account trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2291">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2292">Un mot clé figurant dans la liste Keyword_jp_bank_account est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-2292">A keyword from Keyword_jp_bank_account is found.</span></span>
- <span data-ttu-id="abe74-2293">L’une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="abe74-2293">One of the following is true:</span></span>
- <span data-ttu-id="abe74-2294">La fonction Func_jp_bank_account_branch_code trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2294">The function Func_jp_bank_account_branch_code finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2295">Un mot clé figurant dans la liste Keyword_jp_bank_branch_code est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-2295">A keyword from Keyword_jp_bank_branch_code is found.</span></span>

<span data-ttu-id="abe74-2296">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2296">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2297">La fonction Func_jp_bank_account trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2297">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2298">Un mot clé figurant dans la liste Keyword_jp_bank_account est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-2298">A keyword from Keyword_jp_bank_account is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-2299">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-2299">Keywords</span></span>

#### <a name="keywordjpbankaccount"></a><span data-ttu-id="abe74-2300">Keyword_jp_bank_account</span><span class="sxs-lookup"><span data-stu-id="abe74-2300">Keyword_jp_bank_account</span></span>

- <span data-ttu-id="abe74-2301">Numéro de compte courant
</span><span class="sxs-lookup"><span data-stu-id="abe74-2301">Checking Account Number</span></span> 
- <span data-ttu-id="abe74-2302">Compte courant
</span><span class="sxs-lookup"><span data-stu-id="abe74-2302">Checking Account</span></span> 
- <span data-ttu-id="abe74-2303"># compte courant
</span><span class="sxs-lookup"><span data-stu-id="abe74-2303">Checking Account #</span></span> 
- <span data-ttu-id="abe74-2304">Numéro compte courant
</span><span class="sxs-lookup"><span data-stu-id="abe74-2304">Checking Acct Number</span></span> 
- <span data-ttu-id="abe74-2305"># compte courant
</span><span class="sxs-lookup"><span data-stu-id="abe74-2305">Checking Acct #</span></span> 
- <span data-ttu-id="abe74-2306">N° de compte courant
</span><span class="sxs-lookup"><span data-stu-id="abe74-2306">Checking Acct No.</span></span> 
- <span data-ttu-id="abe74-2307">N° de compte courant
</span><span class="sxs-lookup"><span data-stu-id="abe74-2307">Checking Account No.</span></span> 
- <span data-ttu-id="abe74-2308">Numéro de compte bancaire
</span><span class="sxs-lookup"><span data-stu-id="abe74-2308">Bank Account Number</span></span> 
- <span data-ttu-id="abe74-2309">Compte bancaire
</span><span class="sxs-lookup"><span data-stu-id="abe74-2309">Bank Account</span></span> 
- <span data-ttu-id="abe74-2310"># Compte bancaire
</span><span class="sxs-lookup"><span data-stu-id="abe74-2310">Bank Account #</span></span> 
- <span data-ttu-id="abe74-2311">Numéro de compte bancaire
</span><span class="sxs-lookup"><span data-stu-id="abe74-2311">Bank Acct Number</span></span> 
- <span data-ttu-id="abe74-2312"># Compte bancaire
</span><span class="sxs-lookup"><span data-stu-id="abe74-2312">Bank Acct #</span></span> 
- <span data-ttu-id="abe74-2313">N° de compte bancaire
</span><span class="sxs-lookup"><span data-stu-id="abe74-2313">Bank Acct No.</span></span> 
- <span data-ttu-id="abe74-2314">N° de compte bancaire
</span><span class="sxs-lookup"><span data-stu-id="abe74-2314">Bank Account No.</span></span> 
- <span data-ttu-id="abe74-2315">Numéro de compte d’épargne
</span><span class="sxs-lookup"><span data-stu-id="abe74-2315">Savings Account Number</span></span> 
- <span data-ttu-id="abe74-2316">Compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="abe74-2316">Savings Account</span></span> 
- <span data-ttu-id="abe74-2317">N° de compte d’épargne
</span><span class="sxs-lookup"><span data-stu-id="abe74-2317">Savings Account #</span></span> 
- <span data-ttu-id="abe74-2318">Numéro de compte d’épargne
</span><span class="sxs-lookup"><span data-stu-id="abe74-2318">Savings Acct Number</span></span> 
- <span data-ttu-id="abe74-2319"># compte d’épargne
</span><span class="sxs-lookup"><span data-stu-id="abe74-2319">Savings Acct #</span></span> 
- <span data-ttu-id="abe74-2320">N° de compte d’épargne
</span><span class="sxs-lookup"><span data-stu-id="abe74-2320">Savings Acct No.</span></span> 
- <span data-ttu-id="abe74-2321">N° de compte d’épargne
</span><span class="sxs-lookup"><span data-stu-id="abe74-2321">Savings Account No.</span></span> 
- <span data-ttu-id="abe74-2322">Numéro de compte de débit
</span><span class="sxs-lookup"><span data-stu-id="abe74-2322">Debit Account Number</span></span> 
- <span data-ttu-id="abe74-2323">Compte de débit
</span><span class="sxs-lookup"><span data-stu-id="abe74-2323">Debit Account</span></span> 
- <span data-ttu-id="abe74-2324"># Compte de débit
</span><span class="sxs-lookup"><span data-stu-id="abe74-2324">Debit Account #</span></span> 
- <span data-ttu-id="abe74-2325">Numéro de compte de débit
</span><span class="sxs-lookup"><span data-stu-id="abe74-2325">Debit Acct Number</span></span> 
- <span data-ttu-id="abe74-2326"># Compte de débit
</span><span class="sxs-lookup"><span data-stu-id="abe74-2326">Debit Acct #</span></span> 
- <span data-ttu-id="abe74-2327">N° de compte de débit
</span><span class="sxs-lookup"><span data-stu-id="abe74-2327">Debit Acct No.</span></span> 
- <span data-ttu-id="abe74-2328">N° de compte de débit
</span><span class="sxs-lookup"><span data-stu-id="abe74-2328">Debit Account No.</span></span> 
- <span data-ttu-id="abe74-2329">口座番号を当座預金口座の確認
</span><span class="sxs-lookup"><span data-stu-id="abe74-2329">口座番号を当座預金口座の確認</span></span> 
- <span data-ttu-id="abe74-2330">＃アカウントの確認、勘定番号の確認
</span><span class="sxs-lookup"><span data-stu-id="abe74-2330">＃アカウントの確認、勘定番号の確認</span></span> 
- <span data-ttu-id="abe74-2331">＃勘定の確認
</span><span class="sxs-lookup"><span data-stu-id="abe74-2331">＃勘定の確認</span></span> 
- <span data-ttu-id="abe74-2332">勘定番号の確認
</span><span class="sxs-lookup"><span data-stu-id="abe74-2332">勘定番号の確認</span></span> 
- <span data-ttu-id="abe74-2333">口座番号の確認
</span><span class="sxs-lookup"><span data-stu-id="abe74-2333">口座番号の確認</span></span> 
- <span data-ttu-id="abe74-2334">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="abe74-2334">銀行口座番号</span></span> 
- <span data-ttu-id="abe74-2335">銀行口座</span><span class="sxs-lookup"><span data-stu-id="abe74-2335">銀行口座</span></span> 
- <span data-ttu-id="abe74-2336">銀行口座＃
</span><span class="sxs-lookup"><span data-stu-id="abe74-2336">銀行口座＃</span></span> 
- <span data-ttu-id="abe74-2337">銀行の勘定番号
</span><span class="sxs-lookup"><span data-stu-id="abe74-2337">銀行の勘定番号</span></span> 
- <span data-ttu-id="abe74-2338">銀行のacct＃
</span><span class="sxs-lookup"><span data-stu-id="abe74-2338">銀行のacct＃</span></span> 
- <span data-ttu-id="abe74-2339">銀行の勘定いいえ
</span><span class="sxs-lookup"><span data-stu-id="abe74-2339">銀行の勘定いいえ</span></span> 
- <span data-ttu-id="abe74-2340">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="abe74-2340">銀行口座番号</span></span>
- <span data-ttu-id="abe74-2341">
普通預金口座番号
</span><span class="sxs-lookup"><span data-stu-id="abe74-2341">普通預金口座番号</span></span> 
- <span data-ttu-id="abe74-2342">預金口座
</span><span class="sxs-lookup"><span data-stu-id="abe74-2342">預金口座</span></span> 
- <span data-ttu-id="abe74-2343">貯蓄口座＃
</span><span class="sxs-lookup"><span data-stu-id="abe74-2343">貯蓄口座＃</span></span> 
- <span data-ttu-id="abe74-2344">貯蓄勘定の数
</span><span class="sxs-lookup"><span data-stu-id="abe74-2344">貯蓄勘定の数</span></span> 
- <span data-ttu-id="abe74-2345">貯蓄勘定＃
</span><span class="sxs-lookup"><span data-stu-id="abe74-2345">貯蓄勘定＃</span></span> 
- <span data-ttu-id="abe74-2346">貯蓄勘定番号
</span><span class="sxs-lookup"><span data-stu-id="abe74-2346">貯蓄勘定番号</span></span> 
- <span data-ttu-id="abe74-2347">普通預金口座番号
</span><span class="sxs-lookup"><span data-stu-id="abe74-2347">普通預金口座番号</span></span> 
- <span data-ttu-id="abe74-2348">引き落とし口座番号
</span><span class="sxs-lookup"><span data-stu-id="abe74-2348">引き落とし口座番号</span></span> 
- <span data-ttu-id="abe74-2349">口座番号</span><span class="sxs-lookup"><span data-stu-id="abe74-2349">口座番号</span></span> 
- <span data-ttu-id="abe74-2350">口座番号 #
</span><span class="sxs-lookup"><span data-stu-id="abe74-2350">口座番号＃</span></span> 
- <span data-ttu-id="abe74-2351">デビットのacct番号
</span><span class="sxs-lookup"><span data-stu-id="abe74-2351">デビットのacct番号</span></span> 
- <span data-ttu-id="abe74-2352">デビット勘定＃
</span><span class="sxs-lookup"><span data-stu-id="abe74-2352">デビット勘定＃</span></span> 
- <span data-ttu-id="abe74-2353">デビットACCTの番号
</span><span class="sxs-lookup"><span data-stu-id="abe74-2353">デビットACCTの番号</span></span> 
- <span data-ttu-id="abe74-2354">デビット口座番号
</span><span class="sxs-lookup"><span data-stu-id="abe74-2354">デビット口座番号</span></span> 

#### <a name="keywordjpbankbranchcode"></a><span data-ttu-id="abe74-2355">Keyword_jp_bank_branch_code</span><span class="sxs-lookup"><span data-stu-id="abe74-2355">Keyword_jp_bank_branch_code</span></span>

<span data-ttu-id="abe74-2356">Otemachi</span><span class="sxs-lookup"><span data-stu-id="abe74-2356">Otemachi</span></span>

## <a name="japan-drivers-license-number"></a><span data-ttu-id="abe74-2357">Numéro de permis de conduire Japon</span><span class="sxs-lookup"><span data-stu-id="abe74-2357">Japan Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-2358">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-2358">Format</span></span>

<span data-ttu-id="abe74-2359">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2359">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-2360">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-2360">Pattern</span></span>

<span data-ttu-id="abe74-2361">12 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="abe74-2361">12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-2362">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-2362">Checksum</span></span>

<span data-ttu-id="abe74-2363">Non</span><span class="sxs-lookup"><span data-stu-id="abe74-2363">No</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-2364">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-2364">Definition</span></span>

<span data-ttu-id="abe74-2365">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2365">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2366">La fonction Func_jp_drivers_license_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2366">The function Func_jp_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2367">Un mot clé figurant dans la liste Keyword_jp_drivers_license_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-2367">A keyword from Keyword_jp_drivers_license_number is found.</span></span>

```
<!-- Japan Driver's License Number -->
<Entity id="c6011143-d087-451c-8313-7f6d4aed2270" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_drivers_license_number" />
        <Match idRef ="Keyword_jp_drivers_license_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe74-2368">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-2368">Keywords</span></span>

#### <a name="keywordjpdriverslicensenumber"></a><span data-ttu-id="abe74-2369">Keyword_jp_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="abe74-2369">Keyword_jp_drivers_license_number</span></span>

- <span data-ttu-id="abe74-2370">dl#</span><span class="sxs-lookup"><span data-stu-id="abe74-2370">dl#</span></span> 
- <span data-ttu-id="abe74-2371">DL #</span><span class="sxs-lookup"><span data-stu-id="abe74-2371">DL＃</span></span> 
- <span data-ttu-id="abe74-2372">dls#</span><span class="sxs-lookup"><span data-stu-id="abe74-2372">dls#</span></span> 
- <span data-ttu-id="abe74-2373">LISTES DE DISTRIBUTION #</span><span class="sxs-lookup"><span data-stu-id="abe74-2373">DLS＃</span></span> 
- <span data-ttu-id="abe74-2374">driver license</span><span class="sxs-lookup"><span data-stu-id="abe74-2374">driver license</span></span> 
- <span data-ttu-id="abe74-2375">driver licenses</span><span class="sxs-lookup"><span data-stu-id="abe74-2375">driver licenses</span></span> 
- <span data-ttu-id="abe74-2376">drivers license</span><span class="sxs-lookup"><span data-stu-id="abe74-2376">drivers license</span></span> 
- <span data-ttu-id="abe74-2377">driver’s license</span><span class="sxs-lookup"><span data-stu-id="abe74-2377">driver's license</span></span> 
- <span data-ttu-id="abe74-2378">drivers licenses</span><span class="sxs-lookup"><span data-stu-id="abe74-2378">drivers licenses</span></span> 
- <span data-ttu-id="abe74-2379">driver’s licenses</span><span class="sxs-lookup"><span data-stu-id="abe74-2379">driver's licenses</span></span> 
- <span data-ttu-id="abe74-2380">permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-2380">driving licence</span></span> 
- <span data-ttu-id="abe74-2381">lic#</span><span class="sxs-lookup"><span data-stu-id="abe74-2381">lic#</span></span> 
- <span data-ttu-id="abe74-2382">LIC #</span><span class="sxs-lookup"><span data-stu-id="abe74-2382">LIC＃</span></span> 
- <span data-ttu-id="abe74-2383">#permis</span><span class="sxs-lookup"><span data-stu-id="abe74-2383">lics#</span></span> 
- <span data-ttu-id="abe74-2384">id d’état</span><span class="sxs-lookup"><span data-stu-id="abe74-2384">state id</span></span> 
- <span data-ttu-id="abe74-2385">identification d’état
</span><span class="sxs-lookup"><span data-stu-id="abe74-2385">state identification</span></span> 
- <span data-ttu-id="abe74-2386">numéro d’identification d’état
</span><span class="sxs-lookup"><span data-stu-id="abe74-2386">state identification number</span></span> 
- <span data-ttu-id="abe74-2387">低所得国＃
</span><span class="sxs-lookup"><span data-stu-id="abe74-2387">低所得国＃</span></span> 
- <span data-ttu-id="abe74-2388">免許証</span><span class="sxs-lookup"><span data-stu-id="abe74-2388">免許証</span></span> 
- <span data-ttu-id="abe74-2389">状態ID</span><span class="sxs-lookup"><span data-stu-id="abe74-2389">状態ID</span></span>
- <span data-ttu-id="abe74-2390">
状態の識別
</span><span class="sxs-lookup"><span data-stu-id="abe74-2390">状態の識別</span></span> 
- <span data-ttu-id="abe74-2391">状態の識別番号
</span><span class="sxs-lookup"><span data-stu-id="abe74-2391">状態の識別番号</span></span> 
- <span data-ttu-id="abe74-2392">運転免許</span><span class="sxs-lookup"><span data-stu-id="abe74-2392">運転免許</span></span> 
- <span data-ttu-id="abe74-2393">運転免許証</span><span class="sxs-lookup"><span data-stu-id="abe74-2393">運転免許証</span></span> 
- <span data-ttu-id="abe74-2394">運転免許証番号</span><span class="sxs-lookup"><span data-stu-id="abe74-2394">運転免許証番号</span></span> 
   
## <a name="japan-passport-number"></a><span data-ttu-id="abe74-2395">Numéro de passeport Japon</span><span class="sxs-lookup"><span data-stu-id="abe74-2395">Japan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-2396">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-2396">Format</span></span>

<span data-ttu-id="abe74-2397">Deux lettres suivies de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2397">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-2398">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-2398">Pattern</span></span>

<span data-ttu-id="abe74-2399">Deux lettres (ne respectant pas la casse) suivies de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2399">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-2400">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-2400">Checksum</span></span>

<span data-ttu-id="abe74-2401">Non</span><span class="sxs-lookup"><span data-stu-id="abe74-2401">No</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-2402">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-2402">Definition</span></span>

<span data-ttu-id="abe74-2403">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2403">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2404">La fonction Func_jp_passport trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2404">The function Func_jp_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2405">Un mot clé figurant dans la liste Keyword_jp_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-2405">A keyword from Keyword_jp_passport is found.</span></span>

```
<!-- Japan Passport Number -->
<Entity id="75177310-1a09-4613-bf6d-833aae3743f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_passport" />
        <Match idRef="Keyword_jp_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe74-2406">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-2406">Keywords</span></span>

#### <a name="keywordjppassport"></a><span data-ttu-id="abe74-2407">Keyword_jp_passport</span><span class="sxs-lookup"><span data-stu-id="abe74-2407">Keyword_jp_passport</span></span>

- <span data-ttu-id="abe74-2408">パスポート
</span><span class="sxs-lookup"><span data-stu-id="abe74-2408">パスポート</span></span> 
- <span data-ttu-id="abe74-2409">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="abe74-2409">パスポート番号</span></span> 
- <span data-ttu-id="abe74-2410">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="abe74-2410">パスポートのNum</span></span> 
- <span data-ttu-id="abe74-2411">パスポート＃
</span><span class="sxs-lookup"><span data-stu-id="abe74-2411">パスポート＃</span></span> 
   
## <a name="japan-resident-registration-number"></a><span data-ttu-id="abe74-2412">Matricule de résident Japon</span><span class="sxs-lookup"><span data-stu-id="abe74-2412">Japan Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-2413">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-2413">Format</span></span>

<span data-ttu-id="abe74-2414">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2414">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-2415">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-2415">Pattern</span></span>

<span data-ttu-id="abe74-2416">11 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="abe74-2416">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-2417">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-2417">Checksum</span></span>

<span data-ttu-id="abe74-2418">Non</span><span class="sxs-lookup"><span data-stu-id="abe74-2418">No</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-2419">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-2419">Definition</span></span>

<span data-ttu-id="abe74-2420">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2420">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2421">La fonction Func_jp_resident_registration_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2421">The function Func_jp_resident_registration_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2422">Un mot clé figurant dans la liste Keyword_jp_resident_registration_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-2422">A keyword from Keyword_jp_resident_registration_number is found.</span></span>

```
<!-- Japan Resident Registration Number -->
<Entity id="01c1209b-6389-4faf-a5f8-3f7e13899652" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_resident_registration_number" />
        <Match idRef ="Keyword_jp_resident_registration_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe74-2423">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-2423">Keywords</span></span>

#### <a name="keywordjpresidentregistrationnumber"></a><span data-ttu-id="abe74-2424">Keyword_jp_resident_registration_number</span><span class="sxs-lookup"><span data-stu-id="abe74-2424">Keyword_jp_resident_registration_number</span></span>

- <span data-ttu-id="abe74-2425">Numéro d’enregistrement du résident</span><span class="sxs-lookup"><span data-stu-id="abe74-2425">Resident Registration Number</span></span>
- <span data-ttu-id="abe74-2426">Numéro d’enregistrement du résident
</span><span class="sxs-lookup"><span data-stu-id="abe74-2426">Resident Register Number</span></span> 
- <span data-ttu-id="abe74-2427">Numéro de base d’enregistrement des résidents
</span><span class="sxs-lookup"><span data-stu-id="abe74-2427">Residents Basic Registry Number</span></span> 
- <span data-ttu-id="abe74-2428">N° d’enregistrement du résident
</span><span class="sxs-lookup"><span data-stu-id="abe74-2428">Resident Registration No.</span></span> 
- <span data-ttu-id="abe74-2429">N° d’enregistrement du résident
</span><span class="sxs-lookup"><span data-stu-id="abe74-2429">Resident Register No.</span></span> 
- <span data-ttu-id="abe74-2430">N° de base d’enregistrement des résidents
</span><span class="sxs-lookup"><span data-stu-id="abe74-2430">Residents Basic Registry No.</span></span> 
- <span data-ttu-id="abe74-2431">N° d’enregistrement du résident de base
</span><span class="sxs-lookup"><span data-stu-id="abe74-2431">Basic Resident Register No.</span></span> 
- <span data-ttu-id="abe74-2432">住民登録番号、登録番号をレジデント
</span><span class="sxs-lookup"><span data-stu-id="abe74-2432">住民登録番号、登録番号をレジデント</span></span> 
- <span data-ttu-id="abe74-2433">住民基本登録番号、登録番号
</span><span class="sxs-lookup"><span data-stu-id="abe74-2433">住民基本登録番号、登録番号</span></span> 
- <span data-ttu-id="abe74-2434">住民基本レジストリ番号を常駐
</span><span class="sxs-lookup"><span data-stu-id="abe74-2434">住民基本レジストリ番号を常駐</span></span> 
- <span data-ttu-id="abe74-2435">登録番号を常駐住民基本台帳登録番号
</span><span class="sxs-lookup"><span data-stu-id="abe74-2435">登録番号を常駐住民基本台帳登録番号</span></span> 

   
## <a name="japan-social-insurance-number-sin"></a><span data-ttu-id="abe74-2436">Numéro d'assurance sociale Japon</span><span class="sxs-lookup"><span data-stu-id="abe74-2436">Japan Social Insurance Number (SIN)</span></span>

### <a name="format"></a><span data-ttu-id="abe74-2437">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-2437">Format</span></span>

<span data-ttu-id="abe74-2438">7 à 12 chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2438">7-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-2439">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-2439">Pattern</span></span>

<span data-ttu-id="abe74-2440">7 à 12 chiffres :</span><span class="sxs-lookup"><span data-stu-id="abe74-2440">7-12 digits:</span></span>
- <span data-ttu-id="abe74-2441">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2441">Four digits</span></span> 
- <span data-ttu-id="abe74-2442">Un trait d’union (facultatif)</span><span class="sxs-lookup"><span data-stu-id="abe74-2442">A hyphen (optional)</span></span> 
- <span data-ttu-id="abe74-2443">Six chiffres ou</span><span class="sxs-lookup"><span data-stu-id="abe74-2443">Six digits OR</span></span>
- <span data-ttu-id="abe74-2444">7 à 12 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="abe74-2444">7-12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-2445">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-2445">Checksum</span></span>

<span data-ttu-id="abe74-2446">Non</span><span class="sxs-lookup"><span data-stu-id="abe74-2446">No</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-2447">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-2447">Definition</span></span>

<span data-ttu-id="abe74-2448">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2448">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2449">La fonction Func_jp_sin trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2449">The function Func_jp_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2450">Un mot clé figurant dans la liste Keyword_jp_sin est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-2450">A keyword from Keyword_jp_sin is found.</span></span>

<span data-ttu-id="abe74-2451">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2451">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2452">La fonction Func_jp_sin_pre_1997 trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2452">The function Func_jp_sin_pre_1997 finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2453">Un mot clé figurant dans la liste Keyword_jp_sin est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-2453">A keyword from Keyword_jp_sin is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-2454">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-2454">Keywords</span></span>

#### <a name="keywordjpsin"></a><span data-ttu-id="abe74-2455">Keyword_jp_sin</span><span class="sxs-lookup"><span data-stu-id="abe74-2455">Keyword_jp_sin</span></span>

- <span data-ttu-id="abe74-2456">N° d’assurance sociale
</span><span class="sxs-lookup"><span data-stu-id="abe74-2456">Social Insurance No.</span></span> 
- <span data-ttu-id="abe74-2457">Numéro d’assurance sociale
</span><span class="sxs-lookup"><span data-stu-id="abe74-2457">Social Insurance Num</span></span> 
- <span data-ttu-id="abe74-2458">Numéro d’assurance sociale
</span><span class="sxs-lookup"><span data-stu-id="abe74-2458">Social Insurance Number</span></span> 
- <span data-ttu-id="abe74-2459">社会保険のテンキー
</span><span class="sxs-lookup"><span data-stu-id="abe74-2459">社会保険のテンキー</span></span> 
- <span data-ttu-id="abe74-2460">社会保険番号
</span><span class="sxs-lookup"><span data-stu-id="abe74-2460">社会保険番号</span></span> 
   
## <a name="malaysia-id-card-number"></a><span data-ttu-id="abe74-2461">Numéro de carte d’identité Malaisie</span><span class="sxs-lookup"><span data-stu-id="abe74-2461">Malaysia ID Card Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-2462">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-2462">Format</span></span>

<span data-ttu-id="abe74-2463">12 chiffres contenant éventuellement des traits d’union</span><span class="sxs-lookup"><span data-stu-id="abe74-2463">12 digits containing optional hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-2464">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-2464">Pattern</span></span>

<span data-ttu-id="abe74-2465">12 chiffres :</span><span class="sxs-lookup"><span data-stu-id="abe74-2465">12 digits:</span></span>
- <span data-ttu-id="abe74-2466">Six chiffres au format AAMMJJ correspondant à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="abe74-2466">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="abe74-2467">Un tiret (facultatif) </span><span class="sxs-lookup"><span data-stu-id="abe74-2467">A dash (optional)</span></span> 
- <span data-ttu-id="abe74-2468">Le code à deux lettres du lieu de naissance </span><span class="sxs-lookup"><span data-stu-id="abe74-2468">Two-letter place-of-birth code</span></span> 
- <span data-ttu-id="abe74-2469">Un tiret (facultatif) </span><span class="sxs-lookup"><span data-stu-id="abe74-2469">A dash (optional)</span></span> 
- <span data-ttu-id="abe74-2470">Trois chiffres aléatoires </span><span class="sxs-lookup"><span data-stu-id="abe74-2470">Three random digits</span></span> 
- <span data-ttu-id="abe74-2471">Code de sexe à un chiffre</span><span class="sxs-lookup"><span data-stu-id="abe74-2471">One-digit gender code</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-2472">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-2472">Checksum</span></span>

<span data-ttu-id="abe74-2473">Non</span><span class="sxs-lookup"><span data-stu-id="abe74-2473">No</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-2474">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-2474">Definition</span></span>

<span data-ttu-id="abe74-2475">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2475">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2476">L’expression régulière Regex_malaysia_id_card_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2476">The regular expression Regex_malaysia_id_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2477">Un mot clé figurant dans la liste Keyword_malaysia_id_card_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-2477">A keyword from Keyword_malaysia_id_card_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-2478">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-2478">Keywords</span></span>
   
#### <a name="keywordmalaysiaidcardnumber"></a><span data-ttu-id="abe74-2479">Keyword_malaysia_id_card_number</span><span class="sxs-lookup"><span data-stu-id="abe74-2479">Keyword_malaysia_id_card_number</span></span>

- <span data-ttu-id="abe74-2480">MyKad</span><span class="sxs-lookup"><span data-stu-id="abe74-2480">MyKad</span></span> 
- <span data-ttu-id="abe74-2481">Identity Card</span><span class="sxs-lookup"><span data-stu-id="abe74-2481">Identity Card</span></span> 
- <span data-ttu-id="abe74-2482">Carte d’identité</span><span class="sxs-lookup"><span data-stu-id="abe74-2482">ID Card</span></span> 
- <span data-ttu-id="abe74-2483">Carte d’identification</span><span class="sxs-lookup"><span data-stu-id="abe74-2483">Identification Card</span></span> 
- <span data-ttu-id="abe74-2484">Digital Application Card
</span><span class="sxs-lookup"><span data-stu-id="abe74-2484">Digital Application Card</span></span> 
- <span data-ttu-id="abe74-2485">Kad Akuan Diri
</span><span class="sxs-lookup"><span data-stu-id="abe74-2485">Kad Akuan Diri</span></span> 
- <span data-ttu-id="abe74-2486">Kad Aplikasi Digital
</span><span class="sxs-lookup"><span data-stu-id="abe74-2486">Kad Aplikasi Digital</span></span> 
   
## <a name="netherlands-citizens-service-bsn-number"></a><span data-ttu-id="abe74-2487">Numéro de service du citoyen (BSN) Pays-Bas</span><span class="sxs-lookup"><span data-stu-id="abe74-2487">Netherlands Citizen's Service (BSN) Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-2488">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-2488">Format</span></span>

<span data-ttu-id="abe74-2489">8 à 9 chiffres contenant éventuellement des espaces</span><span class="sxs-lookup"><span data-stu-id="abe74-2489">8-9 digits containing optional spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-2490">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-2490">Pattern</span></span>

<span data-ttu-id="abe74-2491">8 à 9 chiffres :</span><span class="sxs-lookup"><span data-stu-id="abe74-2491">8-9 digits:</span></span>
- <span data-ttu-id="abe74-2492">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2492">Three digits</span></span> 
- <span data-ttu-id="abe74-2493">Un espace (facultatif) </span><span class="sxs-lookup"><span data-stu-id="abe74-2493">A space (optional)</span></span> 
- <span data-ttu-id="abe74-2494">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2494">Three digits</span></span> 
- <span data-ttu-id="abe74-2495">Un espace (facultatif) </span><span class="sxs-lookup"><span data-stu-id="abe74-2495">A space (optional)</span></span> 
- <span data-ttu-id="abe74-2496">2 à 3 chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2496">2-3 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-2497">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-2497">Checksum</span></span>

<span data-ttu-id="abe74-2498">Oui</span><span class="sxs-lookup"><span data-stu-id="abe74-2498">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-2499">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-2499">Definition</span></span>

<span data-ttu-id="abe74-2500">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2500">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2501">La fonction Func_netherlands_bsn trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2501">The function Func_netherlands_bsn finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2502">Un mot clé figurant dans la liste Keyword_netherlands_bsn est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-2502">A keyword from Keyword_netherlands_bsn is found.</span></span>
- <span data-ttu-id="abe74-2503">La fonction Func_eu_date2 trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="abe74-2503">The function Func_eu_date2 finds a date in the right date format.</span></span>
- <span data-ttu-id="abe74-2504">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-2504">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-2505">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-2505">Keywords</span></span>

#### <a name="keywordnetherlandsbsn"></a><span data-ttu-id="abe74-2506">Keyword_netherlands_bsn</span><span class="sxs-lookup"><span data-stu-id="abe74-2506">Keyword_netherlands_bsn</span></span>

- <span data-ttu-id="abe74-2507">Citizen service number
</span><span class="sxs-lookup"><span data-stu-id="abe74-2507">Citizen service number</span></span> 
- <span data-ttu-id="abe74-2508">BSN

</span><span class="sxs-lookup"><span data-stu-id="abe74-2508">BSN</span></span> 
- <span data-ttu-id="abe74-2509">Burgerservicenummer
</span><span class="sxs-lookup"><span data-stu-id="abe74-2509">Burgerservicenummer</span></span> 
- <span data-ttu-id="abe74-2510">Sofinummer
</span><span class="sxs-lookup"><span data-stu-id="abe74-2510">Sofinummer</span></span> 
- <span data-ttu-id="abe74-2511">Persoonsgebonden nummer
</span><span class="sxs-lookup"><span data-stu-id="abe74-2511">Persoonsgebonden nummer</span></span> 
- <span data-ttu-id="abe74-2512">Persoonsnummer
</span><span class="sxs-lookup"><span data-stu-id="abe74-2512">Persoonsnummer</span></span>    

   
## <a name="new-zealand-ministry-of-health-number"></a><span data-ttu-id="abe74-2513">Numéro du Ministère de la santé Nouvelle-Zélande</span><span class="sxs-lookup"><span data-stu-id="abe74-2513">New Zealand Ministry of Health Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-2514">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-2514">Format</span></span>

<span data-ttu-id="abe74-2515">Trois lettres, un espace (facultatif) et quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2515">Three letters, a space (optional), and four digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-2516">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-2516">Pattern</span></span>

<span data-ttu-id="abe74-2517">Trois lettres (pas la casse), un espace (facultatif) quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2517">Three letters (not case sensitive) a space (optional) four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-2518">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-2518">Checksum</span></span>

<span data-ttu-id="abe74-2519">Oui</span><span class="sxs-lookup"><span data-stu-id="abe74-2519">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-2520">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-2520">Definition</span></span>

<span data-ttu-id="abe74-2521">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2521">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2522">La fonction Func_new_zealand_ministry_of_health_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2522">The function Func_new_zealand_ministry_of_health_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2523">Un mot clé figurant dans la liste Keyword_nz_terms est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-2523">A keyword from Keyword_nz_terms is found.</span></span>
- <span data-ttu-id="abe74-2524">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-2524">The checksum passes.</span></span>

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

<span data-ttu-id="abe74-2525">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-2525">Keywords</span></span>

<span data-ttu-id="abe74-2526">Keyword_nz_terms</span><span class="sxs-lookup"><span data-stu-id="abe74-2526">Keyword_nz_terms</span></span>

- <span data-ttu-id="abe74-2527">NHI
</span><span class="sxs-lookup"><span data-stu-id="abe74-2527">NHI</span></span> 
- <span data-ttu-id="abe74-2528">Nouvelle-Zélande</span><span class="sxs-lookup"><span data-stu-id="abe74-2528">New Zealand</span></span> 
- <span data-ttu-id="abe74-2529">Intégrité</span><span class="sxs-lookup"><span data-stu-id="abe74-2529">Health</span></span> 
- <span data-ttu-id="abe74-2530">treatment
</span><span class="sxs-lookup"><span data-stu-id="abe74-2530">treatment</span></span> 
   
## <a name="norway-identification-number"></a><span data-ttu-id="abe74-2531">Numéro d’identification Norvège</span><span class="sxs-lookup"><span data-stu-id="abe74-2531">Norway Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-2532">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-2532">Format</span></span>

<span data-ttu-id="abe74-2533">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2533">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-2534">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-2534">Pattern</span></span>

<span data-ttu-id="abe74-2535">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="abe74-2535">11 digits:</span></span>
- <span data-ttu-id="abe74-2536">Six chiffres au format JJMMAA qui correspondent à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="abe74-2536">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="abe74-2537">Numéro individuel à trois chiffres </span><span class="sxs-lookup"><span data-stu-id="abe74-2537">Three-digit individual number</span></span> 
- <span data-ttu-id="abe74-2538">Deux chiffres de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-2538">Two check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-2539">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-2539">Checksum</span></span>

<span data-ttu-id="abe74-2540">Oui</span><span class="sxs-lookup"><span data-stu-id="abe74-2540">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-2541">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-2541">Definition</span></span>

<span data-ttu-id="abe74-2542">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2542">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2543">La fonction Func_norway_id_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2543">The function Func_norway_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2544">Un mot clé figurant dans la liste Keyword_norway_id_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-2544">A keyword from Keyword_norway_id_number is found.</span></span>
- <span data-ttu-id="abe74-2545">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-2545">The checksum passes.</span></span>
- <span data-ttu-id="abe74-2546">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2546">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2547">La fonction Func_norway_id_numbe trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2547">The function Func_norway_id_numbe finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2548">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-2548">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-2549">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-2549">Keywords</span></span>

#### <a name="keywordnorwayidnumber"></a><span data-ttu-id="abe74-2550">Keyword_norway_id_number</span><span class="sxs-lookup"><span data-stu-id="abe74-2550">Keyword_norway_id_number</span></span>

- <span data-ttu-id="abe74-2551">Personal identification number</span><span class="sxs-lookup"><span data-stu-id="abe74-2551">Personal identification number</span></span>
- <span data-ttu-id="abe74-2552">Norwegian ID Number</span><span class="sxs-lookup"><span data-stu-id="abe74-2552">Norwegian ID Number</span></span>
- <span data-ttu-id="abe74-2553">ID Number</span><span class="sxs-lookup"><span data-stu-id="abe74-2553">ID Number</span></span>
- <span data-ttu-id="abe74-2554">Identification</span><span class="sxs-lookup"><span data-stu-id="abe74-2554">Identification</span></span>
- <span data-ttu-id="abe74-2555">Personnummer</span><span class="sxs-lookup"><span data-stu-id="abe74-2555">Personnummer</span></span>
- <span data-ttu-id="abe74-2556">Fødselsnummer</span><span class="sxs-lookup"><span data-stu-id="abe74-2556">Fødselsnummer</span></span>

   
## <a name="philippines-unified-multi-purpose-id-number"></a><span data-ttu-id="abe74-2557">Numéro d’identification multifonction unifié Philippines</span><span class="sxs-lookup"><span data-stu-id="abe74-2557">Philippines Unified Multi-Purpose ID Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-2558">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-2558">Format</span></span>

<span data-ttu-id="abe74-2559">12 chiffres séparés par des traits d’union</span><span class="sxs-lookup"><span data-stu-id="abe74-2559">12 digits separated by hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-2560">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-2560">Pattern</span></span>

<span data-ttu-id="abe74-2561">12 chiffres :</span><span class="sxs-lookup"><span data-stu-id="abe74-2561">12 digits:</span></span>
- <span data-ttu-id="abe74-2562">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2562">Four digits</span></span> 
- <span data-ttu-id="abe74-2563">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="abe74-2563">A hyphen</span></span> 
- <span data-ttu-id="abe74-2564">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="abe74-2564">Seven digits</span></span> 
- <span data-ttu-id="abe74-2565">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="abe74-2565">A hyphen</span></span> 
- <span data-ttu-id="abe74-2566">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="abe74-2566">One digit</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-2567">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-2567">Checksum</span></span>

<span data-ttu-id="abe74-2568">Non</span><span class="sxs-lookup"><span data-stu-id="abe74-2568">No</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-2569">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-2569">Definition</span></span>

<span data-ttu-id="abe74-2570">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2570">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2571">L’expression régulière Regex_philippines_unified_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2571">The regular expression Regex_philippines_unified_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2572">Un mot clé figurant dans la liste Keyword_philippines_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-2572">A keyword from Keyword_philippines_id is found.</span></span>

```
<!-- Philippines Unified Multi-Purpose ID number -->
<Entity id="019b39dd-8c25-4765-91a3-d9c6baf3c3b3" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_philippines_unified_id"/>
     <Match idRef="Keyword_philippines_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe74-2573">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-2573">Keywords</span></span>
   
#### <a name="keywordphilippinesid"></a><span data-ttu-id="abe74-2574">Keyword_philippines_id</span><span class="sxs-lookup"><span data-stu-id="abe74-2574">Keyword_philippines_id</span></span>

- <span data-ttu-id="abe74-2575">Unified Multi-Purpose ID
</span><span class="sxs-lookup"><span data-stu-id="abe74-2575">Unified Multi-Purpose ID</span></span> 
- <span data-ttu-id="abe74-2576">UMID
</span><span class="sxs-lookup"><span data-stu-id="abe74-2576">UMID</span></span> 
- <span data-ttu-id="abe74-2577">Identity Card</span><span class="sxs-lookup"><span data-stu-id="abe74-2577">Identity Card</span></span> 
- <span data-ttu-id="abe74-2578">Pinag-isang Multi-Layunin ID</span><span class="sxs-lookup"><span data-stu-id="abe74-2578">Pinag-isang Multi-Layunin ID</span></span>
   
## <a name="poland-identity-card"></a><span data-ttu-id="abe74-2579">Carte d'identité Pologne</span><span class="sxs-lookup"><span data-stu-id="abe74-2579">Poland Identity Card</span></span>

### <a name="format"></a><span data-ttu-id="abe74-2580">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-2580">Format</span></span>

<span data-ttu-id="abe74-2581">Trois lettres et six chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2581">Three letters and six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-2582">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-2582">Pattern</span></span>

<span data-ttu-id="abe74-2583">Trois lettres (ne respectant pas la casse) suivis de six chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2583">Three letters (not case sensitive) followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-2584">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-2584">Checksum</span></span>

<span data-ttu-id="abe74-2585">Oui</span><span class="sxs-lookup"><span data-stu-id="abe74-2585">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-2586">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-2586">Definition</span></span>

<span data-ttu-id="abe74-p138">Une stratégie DLP est convaincu que ce type d’informations sensibles a été détecté à 75 % if, au sein d’une proximité de 300 caractères : la fonction Func_polish_national_id recherche le contenu qui correspond au modèle. Un mot clé à partir de Keyword_polish_national_id_passport_number est trouvé. Passe de la somme de contrôle.</span><span class="sxs-lookup"><span data-stu-id="abe74-p138">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_polish_national_id finds content that matches the pattern. A keyword from Keyword_polish_national_id_passport_number is found. The checksum passes.</span></span>

```
<!-- Poland Identity Card-->
<Entity id="25E64989-ED5D-40CA-A939-6C14183BB7BF" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_national_id" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe74-2590">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-2590">Keywords</span></span>

#### <a name="keywordpolishnationalidpassportnumber"></a><span data-ttu-id="abe74-2591">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="abe74-2591">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="abe74-2592">Nazwa je nr dowodu tożsamości
</span><span class="sxs-lookup"><span data-stu-id="abe74-2592">Nazwa i nr dowodu tożsamości</span></span> 
- <span data-ttu-id="abe74-2593">Dowód Tożsamości
</span><span class="sxs-lookup"><span data-stu-id="abe74-2593">Dowód Tożsamości</span></span> 
- <span data-ttu-id="abe74-p139">dow. os.
</span><span class="sxs-lookup"><span data-stu-id="abe74-p139">dow. os.</span></span> 

   
## <a name="poland-national-id-pesel"></a><span data-ttu-id="abe74-2596">ID national polonais (PESEL)</span><span class="sxs-lookup"><span data-stu-id="abe74-2596">Poland National ID (PESEL)</span></span>

### <a name="format"></a><span data-ttu-id="abe74-2597">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-2597">Format</span></span>

<span data-ttu-id="abe74-2598">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2598">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-2599">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-2599">Pattern</span></span>

<span data-ttu-id="abe74-2600">11 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="abe74-2600">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-2601">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-2601">Checksum</span></span>

<span data-ttu-id="abe74-2602">Oui</span><span class="sxs-lookup"><span data-stu-id="abe74-2602">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-2603">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-2603">Definition</span></span>

<span data-ttu-id="abe74-2604">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2604">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2605">La fonction Func_pesel_identification_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2605">The function Func_pesel_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2606">Un mot clé figurant dans la liste Keyword_pesel_identification_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-2606">A keyword from Keyword_pesel_identification_number is found.</span></span>
- <span data-ttu-id="abe74-2607">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-2607">The checksum passes.</span></span>

```
<!-- Poland National ID (PESEL) -->      
<Entity id="E3AAF206-4297-412F-9E06-BA8487E22456" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_pesel_identification_number" />
          <Match idRef="Keyword_pesel_identification_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe74-2608">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-2608">Keywords</span></span>

#### <a name="keywordpeselidentificationnumber"></a><span data-ttu-id="abe74-2609">Keyword_pesel_identification_number</span><span class="sxs-lookup"><span data-stu-id="abe74-2609">Keyword_pesel_identification_number</span></span>

- <span data-ttu-id="abe74-2610">Nr PESEL</span><span class="sxs-lookup"><span data-stu-id="abe74-2610">Nr PESEL</span></span>
- <span data-ttu-id="abe74-2611">PESEL</span><span class="sxs-lookup"><span data-stu-id="abe74-2611">PESEL</span></span>   

   
## <a name="poland-passport"></a><span data-ttu-id="abe74-2612">Passeport Pologne</span><span class="sxs-lookup"><span data-stu-id="abe74-2612">Poland Passport</span></span>

### <a name="format"></a><span data-ttu-id="abe74-2613">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-2613">Format</span></span>

<span data-ttu-id="abe74-2614">Deux lettres et sept chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2614">Two letters and seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-2615">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-2615">Pattern</span></span>

<span data-ttu-id="abe74-2616">Deux lettres (ne respectant pas la casse) suivies de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2616">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-2617">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-2617">Checksum</span></span>

<span data-ttu-id="abe74-2618">Oui</span><span class="sxs-lookup"><span data-stu-id="abe74-2618">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-2619">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-2619">Definition</span></span>

<span data-ttu-id="abe74-2620">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2620">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2621">La fonction Func_polish_passport_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2621">The function Func_polish_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2622">Un mot clé figurant dans la liste Keyword_polish_national_id_passport_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-2622">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
- <span data-ttu-id="abe74-2623">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-2623">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-2624">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-2624">Keywords</span></span>

#### <a name="keywordpolishnationalidpassportnumber"></a><span data-ttu-id="abe74-2625">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="abe74-2625">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="abe74-2626">Nazwa je nr dowodu tożsamości
</span><span class="sxs-lookup"><span data-stu-id="abe74-2626">Nazwa i nr dowodu tożsamości</span></span> 
- <span data-ttu-id="abe74-2627">Dowód Tożsamości
</span><span class="sxs-lookup"><span data-stu-id="abe74-2627">Dowód Tożsamości</span></span> 
- <span data-ttu-id="abe74-p140">dow. os.
</span><span class="sxs-lookup"><span data-stu-id="abe74-p140">dow. os.</span></span> 

   
## <a name="portugal-citizen-card-number"></a><span data-ttu-id="abe74-2630">Numéro de carte de citoyen portugais</span><span class="sxs-lookup"><span data-stu-id="abe74-2630">Portugal Citizen Card Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-2631">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-2631">Format</span></span>

<span data-ttu-id="abe74-2632">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2632">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-2633">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-2633">Pattern</span></span>

<span data-ttu-id="abe74-2634">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2634">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-2635">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-2635">Checksum</span></span>

<span data-ttu-id="abe74-2636">Non</span><span class="sxs-lookup"><span data-stu-id="abe74-2636">No</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-2637">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-2637">Definition</span></span>

<span data-ttu-id="abe74-2638">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2638">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2639">L’expression régulière Regex_portugal_citizen_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2639">The regular expression Regex_portugal_citizen_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2640">Un mot clé figurant dans la liste Keyword_portugal_citizen_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-2640">A keyword from Keyword_portugal_citizen_card is found.</span></span>

```
<!-- Portugal Citizen Card Number -->
<Entity id="91a7ece2-add4-4986-9a15-c84544d81ecd" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_portugal_citizen_card"/>
     <Match idRef="Keyword_portugal_citizen_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe74-2641">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-2641">Keywords</span></span>

#### <a name="keywordportugalcitizencard"></a><span data-ttu-id="abe74-2642">Keyword_portugal_citizen_card</span><span class="sxs-lookup"><span data-stu-id="abe74-2642">Keyword_portugal_citizen_card</span></span>

- <span data-ttu-id="abe74-2643">Citizen Card</span><span class="sxs-lookup"><span data-stu-id="abe74-2643">Citizen Card</span></span>
- <span data-ttu-id="abe74-2644">National ID Card</span><span class="sxs-lookup"><span data-stu-id="abe74-2644">National ID Card</span></span>
- <span data-ttu-id="abe74-2645">CC</span><span class="sxs-lookup"><span data-stu-id="abe74-2645">CC</span></span>
- <span data-ttu-id="abe74-2646">Cartão de Cidadão</span><span class="sxs-lookup"><span data-stu-id="abe74-2646">Cartão de Cidadão</span></span>
- <span data-ttu-id="abe74-2647">Bilhete de Identidade</span><span class="sxs-lookup"><span data-stu-id="abe74-2647">Bilhete de Identidade</span></span>
   
## <a name="saudi-arabia-national-id"></a><span data-ttu-id="abe74-2648">ID national Arabie saoudite</span><span class="sxs-lookup"><span data-stu-id="abe74-2648">Saudi Arabia National ID</span></span>

### <a name="format"></a><span data-ttu-id="abe74-2649">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-2649">Format</span></span>

<span data-ttu-id="abe74-2650">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2650">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-2651">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-2651">Pattern</span></span>

<span data-ttu-id="abe74-2652">10 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="abe74-2652">10 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-2653">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-2653">Checksum</span></span>

<span data-ttu-id="abe74-2654">Non</span><span class="sxs-lookup"><span data-stu-id="abe74-2654">No</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-2655">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-2655">Definition</span></span>

<span data-ttu-id="abe74-2656">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2656">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2657">L’expression régulière Regex_saudi_arabia_national_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2657">The regular expression Regex_saudi_arabia_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2658">Un mot clé figurant dans la liste Keyword_saudi_arabia_national_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-2658">A keyword from Keyword_saudi_arabia_national_id is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-2659">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-2659">Keywords</span></span>

#### <a name="keywordsaudiarabianationalid"></a><span data-ttu-id="abe74-2660">Keyword_saudi_arabia_national_id</span><span class="sxs-lookup"><span data-stu-id="abe74-2660">Keyword_saudi_arabia_national_id</span></span>

- <span data-ttu-id="abe74-2661">Carte d’identification
</span><span class="sxs-lookup"><span data-stu-id="abe74-2661">Identification Card</span></span> 
- <span data-ttu-id="abe74-2662">numéro de carte d’identité
</span><span class="sxs-lookup"><span data-stu-id="abe74-2662">I card number</span></span> 
- <span data-ttu-id="abe74-2663">numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="abe74-2663">ID number</span></span> 
- <span data-ttu-id="abe74-2664">الوطنية الهوية بطاقة رقم
</span><span class="sxs-lookup"><span data-stu-id="abe74-2664">الوطنية الهوية بطاقة رقم</span></span> 

   
## <a name="singapore-national-registration-identity-card-nric-number"></a><span data-ttu-id="abe74-2665">Numéro de carte d’identité d’enregistrement national (NRIC) Singapour</span><span class="sxs-lookup"><span data-stu-id="abe74-2665">Singapore National Registration Identity Card (NRIC) Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-2666">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-2666">Format</span></span>

<span data-ttu-id="abe74-2667">Neuf lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2667">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-2668">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-2668">Pattern</span></span>

- <span data-ttu-id="abe74-2669">Neuf lettres et chiffres :</span><span class="sxs-lookup"><span data-stu-id="abe74-2669">Nine letters and digits:</span></span>
- <span data-ttu-id="abe74-2670">La lettre « F », « G », « S » ou « T » (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="abe74-2670">The letter "F", "G", "S", or "T" (not case sensitive)</span></span> 
- <span data-ttu-id="abe74-2671">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="abe74-2671">Seven digits</span></span> 
- <span data-ttu-id="abe74-2672">Un chiffre de contrôle alphabétique</span><span class="sxs-lookup"><span data-stu-id="abe74-2672">An alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-2673">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-2673">Checksum</span></span>

<span data-ttu-id="abe74-2674">Oui</span><span class="sxs-lookup"><span data-stu-id="abe74-2674">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-2675">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-2675">Definition</span></span>

<span data-ttu-id="abe74-2676">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2676">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2677">L’expression régulière Regex_singapore_nric trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2677">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2678">Un mot clé figurant dans la liste Keyword_singapore_nric est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-2678">A keyword from Keyword_singapore_nric is found.</span></span>
- <span data-ttu-id="abe74-2679">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-2679">The checksum passes.</span></span>

<span data-ttu-id="abe74-2680">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2680">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2681">L’expression régulière Regex_singapore_nric trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2681">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2682">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-2682">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-2683">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-2683">Keywords</span></span>
   
#### <a name="keywordsingaporenric"></a><span data-ttu-id="abe74-2684">Keyword_singapore_nric</span><span class="sxs-lookup"><span data-stu-id="abe74-2684">Keyword_singapore_nric</span></span>

- <span data-ttu-id="abe74-2685">National Registration Identity Card
</span><span class="sxs-lookup"><span data-stu-id="abe74-2685">National Registration Identity Card</span></span> 
- <span data-ttu-id="abe74-2686">Identity Card Number
</span><span class="sxs-lookup"><span data-stu-id="abe74-2686">Identity Card Number</span></span> 
- <span data-ttu-id="abe74-2687">NRIC
</span><span class="sxs-lookup"><span data-stu-id="abe74-2687">NRIC</span></span> 
- <span data-ttu-id="abe74-2688">IC
</span><span class="sxs-lookup"><span data-stu-id="abe74-2688">IC</span></span> 
- <span data-ttu-id="abe74-2689">Foreign Identification Number
</span><span class="sxs-lookup"><span data-stu-id="abe74-2689">Foreign Identification Number</span></span> 
- <span data-ttu-id="abe74-2690">FIN
</span><span class="sxs-lookup"><span data-stu-id="abe74-2690">FIN</span></span> 
- <span data-ttu-id="abe74-2691">身份证 </span><span class="sxs-lookup"><span data-stu-id="abe74-2691">身份证</span></span> 
- <span data-ttu-id="abe74-2692">身份證
</span><span class="sxs-lookup"><span data-stu-id="abe74-2692">身份證</span></span> 
   
## <a name="south-africa-identification-number"></a><span data-ttu-id="abe74-2693">Numéro d’identification Afrique du Sud</span><span class="sxs-lookup"><span data-stu-id="abe74-2693">South Africa Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-2694">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-2694">Format</span></span>

<span data-ttu-id="abe74-2695">13 chiffres pouvant contenir des espaces</span><span class="sxs-lookup"><span data-stu-id="abe74-2695">13 digits that may contain spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-2696">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-2696">Pattern</span></span>

<span data-ttu-id="abe74-2697">13 chiffres :</span><span class="sxs-lookup"><span data-stu-id="abe74-2697">13 digits:</span></span>
- <span data-ttu-id="abe74-2698">Six chiffres au format AAMMJJ correspondant à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="abe74-2698">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="abe74-2699">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2699">Four digits</span></span> 
- <span data-ttu-id="abe74-2700">Un indicateur de citoyenneté à un chiffre </span><span class="sxs-lookup"><span data-stu-id="abe74-2700">A single-digit citizenship indicator</span></span> 
- <span data-ttu-id="abe74-2701">Le chiffre « 8 » ou « 9 » </span><span class="sxs-lookup"><span data-stu-id="abe74-2701">The digit "8" or "9"</span></span> 
- <span data-ttu-id="abe74-2702">Un chiffre pour la somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-2702">One digit which is a checksum digit</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-2703">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-2703">Checksum</span></span>

<span data-ttu-id="abe74-2704">Oui</span><span class="sxs-lookup"><span data-stu-id="abe74-2704">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-2705">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-2705">Definition</span></span>

<span data-ttu-id="abe74-2706">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2706">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2707">La fonction Func_south_africa_identification_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2707">The function Func_south_africa_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2708">Un mot clé figurant dans la liste Keyword_south_africa_identification_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-2708">A keyword from Keyword_south_africa_identification_number is found.</span></span>
- <span data-ttu-id="abe74-2709">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-2709">The checksum passes.</span></span>

```
<!-- South Africa Identification Number -->
<Entity id="e2adf7cb-8ea6-4048-a2ed-d89eb65f2780" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_south_africa_identification_number"/>
     <Match idRef="Keyword_south_africa_identification_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe74-2710">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-2710">Keywords</span></span>
   
#### <a name="keywordsouthafricaidentificationnumber"></a><span data-ttu-id="abe74-2711">Keyword_south_africa_identification_number</span><span class="sxs-lookup"><span data-stu-id="abe74-2711">Keyword_south_africa_identification_number</span></span>

- <span data-ttu-id="abe74-2712">Identity card</span><span class="sxs-lookup"><span data-stu-id="abe74-2712">Identity card</span></span>
- <span data-ttu-id="abe74-2713">ID</span><span class="sxs-lookup"><span data-stu-id="abe74-2713">ID</span></span>
- <span data-ttu-id="abe74-2714">Identification</span><span class="sxs-lookup"><span data-stu-id="abe74-2714">Identification</span></span> 
   
## <a name="south-korea-resident-registration-number"></a><span data-ttu-id="abe74-2715">Matricule de résident Corée du Sud</span><span class="sxs-lookup"><span data-stu-id="abe74-2715">South Korea Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-2716">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-2716">Format</span></span>

<span data-ttu-id="abe74-2717">13 chiffres contenant un trait d’union</span><span class="sxs-lookup"><span data-stu-id="abe74-2717">13 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-2718">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-2718">Pattern</span></span>

<span data-ttu-id="abe74-2719">13 chiffres :</span><span class="sxs-lookup"><span data-stu-id="abe74-2719">13 digits:</span></span>
- <span data-ttu-id="abe74-2720">Six chiffres au format AAMMJJ correspondant à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="abe74-2720">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="abe74-2721">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="abe74-2721">A hyphen</span></span> 
- <span data-ttu-id="abe74-2722">Un chiffre déterminé par le siècle et le sexe </span><span class="sxs-lookup"><span data-stu-id="abe74-2722">One digit determined by the century and gender</span></span> 
- <span data-ttu-id="abe74-2723">Code à quatre chiffres désignant la région de naissance </span><span class="sxs-lookup"><span data-stu-id="abe74-2723">Four-digit region-of-birth code</span></span> 
- <span data-ttu-id="abe74-2724">Un chiffre utilisé pour différencier les personnes dont les chiffres précédents sont identiques. </span><span class="sxs-lookup"><span data-stu-id="abe74-2724">One digit used to differentiate people for whom the preceding numbers are identical</span></span> 
- <span data-ttu-id="abe74-2725">Un chiffre de contrôle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2725">A check digit.</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-2726">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-2726">Checksum</span></span>

<span data-ttu-id="abe74-2727">Oui</span><span class="sxs-lookup"><span data-stu-id="abe74-2727">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-2728">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-2728">Definition</span></span>

<span data-ttu-id="abe74-2729">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2729">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2730">La fonction Func_south_korea_resident_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2730">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2731">Un mot clé figurant dans la liste Keyword_south_korea_resident_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-2731">A keyword from Keyword_south_korea_resident_number is found.</span></span>
- <span data-ttu-id="abe74-2732">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-2732">The checksum passes.</span></span>

<span data-ttu-id="abe74-2733">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2733">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2734">La fonction Func_south_korea_resident_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2734">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2735">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-2735">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-2736">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-2736">Keywords</span></span>
   
#### <a name="keywordsouthkorearesidentnumber"></a><span data-ttu-id="abe74-2737">Keyword_south_korea_resident_number</span><span class="sxs-lookup"><span data-stu-id="abe74-2737">Keyword_south_korea_resident_number</span></span>

- <span data-ttu-id="abe74-2738">National ID card
</span><span class="sxs-lookup"><span data-stu-id="abe74-2738">National ID card</span></span> 
- <span data-ttu-id="abe74-2739">Citizen’s Registration Number
</span><span class="sxs-lookup"><span data-stu-id="abe74-2739">Citizen's Registration Number</span></span> 
- <span data-ttu-id="abe74-2740">Jumin deungnok beonho
</span><span class="sxs-lookup"><span data-stu-id="abe74-2740">Jumin deungnok beonho</span></span> 
- <span data-ttu-id="abe74-2741">RRN
</span><span class="sxs-lookup"><span data-stu-id="abe74-2741">RRN</span></span> 
- <span data-ttu-id="abe74-2742">주민등록번호</span><span class="sxs-lookup"><span data-stu-id="abe74-2742">주민등록번호</span></span>
   
## <a name="spain-social-security-number-ssn"></a><span data-ttu-id="abe74-2743">Numéro de sécurité sociale Espagne</span><span class="sxs-lookup"><span data-stu-id="abe74-2743">Spain Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="abe74-2744">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-2744">Format</span></span>

<span data-ttu-id="abe74-2745">11 à 12 chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2745">11-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-2746">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-2746">Pattern</span></span>

<span data-ttu-id="abe74-2747">chiffres de 11-12 :</span><span class="sxs-lookup"><span data-stu-id="abe74-2747">11-12 digits:</span></span>
- <span data-ttu-id="abe74-2748">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2748">Two digits</span></span> 
- <span data-ttu-id="abe74-2749">Une barre oblique (facultative)</span><span class="sxs-lookup"><span data-stu-id="abe74-2749">A forward slash (optional)</span></span> 
- <span data-ttu-id="abe74-2750">7 à 8 chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2750">7-8 digits</span></span> 
- <span data-ttu-id="abe74-2751">Une barre oblique (facultative)</span><span class="sxs-lookup"><span data-stu-id="abe74-2751">A forward slash (optional)</span></span> 
- <span data-ttu-id="abe74-2752">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2752">Two digits</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-2753">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-2753">Checksum</span></span>

<span data-ttu-id="abe74-2754">Oui</span><span class="sxs-lookup"><span data-stu-id="abe74-2754">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-2755">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-2755">Definition</span></span>

<span data-ttu-id="abe74-2756">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2756">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2757">La fonction Func_spanish_social_security_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2757">The function Func_spanish_social_security_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2758">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-2758">The checksum passes.</span></span>

```
<!-- Spain SSN -->
<Entity id="5df987c0-8eae-4bce-ace7-b316347f3070" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_spanish_social_security_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe74-2759">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-2759">Keywords</span></span>

<span data-ttu-id="abe74-2760">Aucun</span><span class="sxs-lookup"><span data-stu-id="abe74-2760">None</span></span>
   
## <a name="sweden-national-id"></a><span data-ttu-id="abe74-2761">ID national Suède</span><span class="sxs-lookup"><span data-stu-id="abe74-2761">Sweden National ID</span></span>

### <a name="format"></a><span data-ttu-id="abe74-2762">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-2762">Format</span></span>

<span data-ttu-id="abe74-2763">10 ou 12 chiffres et éventuellement un délimiteur</span><span class="sxs-lookup"><span data-stu-id="abe74-2763">10 or 12 digits and an optional delimiter</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-2764">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-2764">Pattern</span></span>

<span data-ttu-id="abe74-2765">10 ou 12 chiffres et un délimiteur facultatif :</span><span class="sxs-lookup"><span data-stu-id="abe74-2765">10 or 12 digits and an optional delimiter:</span></span>
- <span data-ttu-id="abe74-2766">2 à 4 chiffres (facultatifs)</span><span class="sxs-lookup"><span data-stu-id="abe74-2766">2-4 digits (optional)</span></span> 
- <span data-ttu-id="abe74-2767">Six chiffres au format de date AAMMJJ</span><span class="sxs-lookup"><span data-stu-id="abe74-2767">Six digits in date format YYMMDD</span></span> 
- <span data-ttu-id="abe74-2768">Séparateur de « - » ou « + » (facultatif), plus</span><span class="sxs-lookup"><span data-stu-id="abe74-2768">Delimiter of "-" or "+" (optional), plus</span></span>
- <span data-ttu-id="abe74-2769">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2769">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-2770">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-2770">Checksum</span></span>

<span data-ttu-id="abe74-2771">Oui</span><span class="sxs-lookup"><span data-stu-id="abe74-2771">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-2772">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-2772">Definition</span></span>

<span data-ttu-id="abe74-2773">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2773">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2774">La fonction Func_swedish_national_identifier trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2774">The function Func_swedish_national_identifier finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2775">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-2775">The checksum passes.</span></span>

```
<!-- Sweden National ID -->
<Entity id="f69aaf40-79be-4fac-8f05-fd1910d272c8" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_swedish_national_identifier" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe74-2776">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-2776">Keywords</span></span>

<span data-ttu-id="abe74-2777">Non</span><span class="sxs-lookup"><span data-stu-id="abe74-2777">No</span></span>
   
## <a name="sweden-passport-number"></a><span data-ttu-id="abe74-2778">Numéro de passeport Suède</span><span class="sxs-lookup"><span data-stu-id="abe74-2778">Sweden Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-2779">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-2779">Format</span></span>

<span data-ttu-id="abe74-2780">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2780">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-2781">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-2781">Pattern</span></span>

<span data-ttu-id="abe74-2782">Huit chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="abe74-2782">Eight consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-2783">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-2783">Checksum</span></span>

<span data-ttu-id="abe74-2784">Non</span><span class="sxs-lookup"><span data-stu-id="abe74-2784">No</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-2785">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-2785">Definition</span></span>

<span data-ttu-id="abe74-2786">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2786">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2787">L’expression régulière Regex_sweden_passport_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2787">The regular expression Regex_sweden_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2788">L’une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="abe74-2788">One of the following is true:</span></span>
    - <span data-ttu-id="abe74-2789">Un mot clé figurant dans la liste Keyword_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-2789">A keyword from Keyword_passport is found.</span></span>
    - <span data-ttu-id="abe74-2790">Un mot clé figurant dans la liste Keyword_sweden_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-2790">A keyword from Keyword_sweden_passport is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-2791">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-2791">Keywords</span></span>
   
#### <a name="keywordswedenpassport"></a><span data-ttu-id="abe74-2792">Keyword_sweden_passport</span><span class="sxs-lookup"><span data-stu-id="abe74-2792">Keyword_sweden_passport</span></span>

- <span data-ttu-id="abe74-2793">exigences en matière de visa
</span><span class="sxs-lookup"><span data-stu-id="abe74-2793">visa requirements</span></span> 
- <span data-ttu-id="abe74-2794">Carte d’enregistrement d’une personne étrangère
</span><span class="sxs-lookup"><span data-stu-id="abe74-2794">Alien Registration Card</span></span> 
- <span data-ttu-id="abe74-2795">Visas Schengen
</span><span class="sxs-lookup"><span data-stu-id="abe74-2795">Schengen visas</span></span> 
- <span data-ttu-id="abe74-2796">Visa Schengen
</span><span class="sxs-lookup"><span data-stu-id="abe74-2796">Schengen visa</span></span> 
- <span data-ttu-id="abe74-2797">Traitement du visa
</span><span class="sxs-lookup"><span data-stu-id="abe74-2797">Visa Processing</span></span> 
- <span data-ttu-id="abe74-2798">Type de visa
</span><span class="sxs-lookup"><span data-stu-id="abe74-2798">Visa Type</span></span> 
- <span data-ttu-id="abe74-2799">Entrée unique
</span><span class="sxs-lookup"><span data-stu-id="abe74-2799">Single Entry</span></span> 
- <span data-ttu-id="abe74-2800">Entrée multiple
</span><span class="sxs-lookup"><span data-stu-id="abe74-2800">Multiple Entry</span></span> 
- <span data-ttu-id="abe74-2801">Frais de traitement G3

</span><span class="sxs-lookup"><span data-stu-id="abe74-2801">G3 Processing Fees</span></span> 

#### <a name="keywordpassport"></a><span data-ttu-id="abe74-2802">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="abe74-2802">Keyword_passport</span></span>

- <span data-ttu-id="abe74-2803">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="abe74-2803">Passport Number</span></span> 
- <span data-ttu-id="abe74-2804">
N° de passeport</span><span class="sxs-lookup"><span data-stu-id="abe74-2804">Passport No</span></span> 
- <span data-ttu-id="abe74-2805"># Passeport
</span><span class="sxs-lookup"><span data-stu-id="abe74-2805">Passport #</span></span> 
- <span data-ttu-id="abe74-2806">#Passeport
</span><span class="sxs-lookup"><span data-stu-id="abe74-2806">Passport#</span></span> 
- <span data-ttu-id="abe74-2807">IDPassport</span><span class="sxs-lookup"><span data-stu-id="abe74-2807">PassportID</span></span> 
- <span data-ttu-id="abe74-2808">n° passeport
</span><span class="sxs-lookup"><span data-stu-id="abe74-2808">Passportno</span></span> 
- <span data-ttu-id="abe74-2809">numéropasseport
</span><span class="sxs-lookup"><span data-stu-id="abe74-2809">passportnumber</span></span> 
- <span data-ttu-id="abe74-2810">パスポート</span><span class="sxs-lookup"><span data-stu-id="abe74-2810">パスポート</span></span> 
- <span data-ttu-id="abe74-2811">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="abe74-2811">パスポート番号</span></span> 
- <span data-ttu-id="abe74-2812">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="abe74-2812">パスポートのNum</span></span> 
- <span data-ttu-id="abe74-2813">パスポート＃
</span><span class="sxs-lookup"><span data-stu-id="abe74-2813">パスポート＃</span></span> 
- <span data-ttu-id="abe74-2814">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="abe74-2814">Numéro de passeport</span></span> 
- <span data-ttu-id="abe74-2815">
Passeport n°</span><span class="sxs-lookup"><span data-stu-id="abe74-2815">Passeport n °</span></span> 
- <span data-ttu-id="abe74-2816">Passeport numéro
</span><span class="sxs-lookup"><span data-stu-id="abe74-2816">Passeport Non</span></span> 
- <span data-ttu-id="abe74-2817"># Passeport
</span><span class="sxs-lookup"><span data-stu-id="abe74-2817">Passeport #</span></span> 
- <span data-ttu-id="abe74-2818">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="abe74-2818">Passeport#</span></span> 
- <span data-ttu-id="abe74-2819">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="abe74-2819">PasseportNon</span></span> 
- <span data-ttu-id="abe74-2820">Passeportn °
</span><span class="sxs-lookup"><span data-stu-id="abe74-2820">Passeportn °</span></span> 
   
## <a name="swift-code"></a><span data-ttu-id="abe74-2821">Code SWIFT</span><span class="sxs-lookup"><span data-stu-id="abe74-2821">SWIFT Code</span></span>

### <a name="format"></a><span data-ttu-id="abe74-2822">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-2822">Format</span></span>

<span data-ttu-id="abe74-2823">Quatre lettres suivies de 5 à 31 lettres ou chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2823">Four letters followed by 5-31 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-2824">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-2824">Pattern</span></span>

<span data-ttu-id="abe74-2825">Quatre lettres suivies de 5 à 31 lettres ou chiffres :</span><span class="sxs-lookup"><span data-stu-id="abe74-2825">Four letters followed by 5-31 letters or digits:</span></span>
- <span data-ttu-id="abe74-2826">Code bancaire à quatre lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="abe74-2826">Four-letter bank code (not case sensitive)</span></span> 
- <span data-ttu-id="abe74-2827">Un espace facultatif</span><span class="sxs-lookup"><span data-stu-id="abe74-2827">An optional space</span></span> 
- <span data-ttu-id="abe74-2828">4 à 28 lettres ou chiffres (numéro de compte bancaire de base (BBAN))</span><span class="sxs-lookup"><span data-stu-id="abe74-2828">4-28 letters or digits (the Basic Bank Account Number (BBAN))</span></span> 
- <span data-ttu-id="abe74-2829">Un espace facultatif</span><span class="sxs-lookup"><span data-stu-id="abe74-2829">An optional space</span></span> 
- <span data-ttu-id="abe74-2830">1 à 3 lettres ou chiffres (reste du BBAN)</span><span class="sxs-lookup"><span data-stu-id="abe74-2830">1-3 letters or digits (remainder of the BBAN)</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-2831">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-2831">Checksum</span></span>

<span data-ttu-id="abe74-2832">Non</span><span class="sxs-lookup"><span data-stu-id="abe74-2832">No</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-2833">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-2833">Definition</span></span>

<span data-ttu-id="abe74-2834">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2834">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2835">L’expression régulière Regex_swift trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2835">The regular expression Regex_swift finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2836">Un mot clé figurant dans la liste Keyword_swift est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-2836">A keyword from Keyword_swift is found.</span></span>

```
<Entity id="cb2ab58c-9cb8-4c81-baf8-a4e106791df4" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_swift" />
        <Match idRef="Keyword_swift" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe74-2837">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-2837">Keywords</span></span>
   
#### <a name="keywordswift"></a><span data-ttu-id="abe74-2838">Keyword_swift</span><span class="sxs-lookup"><span data-stu-id="abe74-2838">Keyword_swift</span></span>

- <span data-ttu-id="abe74-2839">organisation internationale de normalisation 9362
</span><span class="sxs-lookup"><span data-stu-id="abe74-2839">international organization for standardization 9362</span></span> 
- <span data-ttu-id="abe74-2840">ISO 9362
</span><span class="sxs-lookup"><span data-stu-id="abe74-2840">iso 9362</span></span> 
- <span data-ttu-id="abe74-2841">iso9362</span><span class="sxs-lookup"><span data-stu-id="abe74-2841">iso9362</span></span> 
- <span data-ttu-id="abe74-2842">SWIFT\#</span><span class="sxs-lookup"><span data-stu-id="abe74-2842">swift\#</span></span> 
- <span data-ttu-id="abe74-2843">codeswift
</span><span class="sxs-lookup"><span data-stu-id="abe74-2843">swiftcode</span></span> 
- <span data-ttu-id="abe74-2844">numéroswift
</span><span class="sxs-lookup"><span data-stu-id="abe74-2844">swiftnumber</span></span> 
- <span data-ttu-id="abe74-2845">numéroroutageswift
</span><span class="sxs-lookup"><span data-stu-id="abe74-2845">swiftroutingnumber</span></span> 
- <span data-ttu-id="abe74-2846">code SWIFT</span><span class="sxs-lookup"><span data-stu-id="abe74-2846">swift code</span></span> 
- <span data-ttu-id="abe74-2847"># numéro swift
</span><span class="sxs-lookup"><span data-stu-id="abe74-2847">swift number #</span></span> 
- <span data-ttu-id="abe74-2848">numéro d’acheminement swift
</span><span class="sxs-lookup"><span data-stu-id="abe74-2848">swift routing number</span></span> 
- <span data-ttu-id="abe74-2849">numéro BIC
</span><span class="sxs-lookup"><span data-stu-id="abe74-2849">bic number</span></span> 
- <span data-ttu-id="abe74-2850">code BIC
</span><span class="sxs-lookup"><span data-stu-id="abe74-2850">bic code</span></span> 
- <span data-ttu-id="abe74-2851">BIC\#</span><span class="sxs-lookup"><span data-stu-id="abe74-2851">bic \#</span></span> 
- <span data-ttu-id="abe74-2852">BIC\#</span><span class="sxs-lookup"><span data-stu-id="abe74-2852">bic\#</span></span> 
- <span data-ttu-id="abe74-2853">code d’identification bancaire
</span><span class="sxs-lookup"><span data-stu-id="abe74-2853">bank identifier code</span></span> 
- <span data-ttu-id="abe74-2854">標準化9362</span><span class="sxs-lookup"><span data-stu-id="abe74-2854">標準化9362</span></span> 
- <span data-ttu-id="abe74-2855">迅速＃
</span><span class="sxs-lookup"><span data-stu-id="abe74-2855">迅速＃</span></span> 
- <span data-ttu-id="abe74-2856">SWIFTコード
</span><span class="sxs-lookup"><span data-stu-id="abe74-2856">SWIFTコード</span></span> 
- <span data-ttu-id="abe74-2857">SWIFT番号
</span><span class="sxs-lookup"><span data-stu-id="abe74-2857">SWIFT番号</span></span> 
- <span data-ttu-id="abe74-2858">迅速なルーティング番号
</span><span class="sxs-lookup"><span data-stu-id="abe74-2858">迅速なルーティング番号</span></span> 
- <span data-ttu-id="abe74-2859">BIC番号
</span><span class="sxs-lookup"><span data-stu-id="abe74-2859">BIC番号</span></span> 
- <span data-ttu-id="abe74-2860">BICコード
</span><span class="sxs-lookup"><span data-stu-id="abe74-2860">BICコード</span></span> 
- <span data-ttu-id="abe74-2861">銀行識別コードのための国際組織
</span><span class="sxs-lookup"><span data-stu-id="abe74-2861">銀行識別コードのための国際組織</span></span> 
- <span data-ttu-id="abe74-2862">Organisation internationale de normalisation 9362
</span><span class="sxs-lookup"><span data-stu-id="abe74-2862">Organisation internationale de normalisation 9362</span></span> 
- <span data-ttu-id="abe74-2863">rapide\#</span><span class="sxs-lookup"><span data-stu-id="abe74-2863">rapide \#</span></span> 
- <span data-ttu-id="abe74-2864">code SWIFT
</span><span class="sxs-lookup"><span data-stu-id="abe74-2864">code SWIFT</span></span> 
- <span data-ttu-id="abe74-2865">le numéro de swift
</span><span class="sxs-lookup"><span data-stu-id="abe74-2865">le numéro de swift</span></span> 
- <span data-ttu-id="abe74-2866">swift numéro d’acheminement
</span><span class="sxs-lookup"><span data-stu-id="abe74-2866">swift numéro d'acheminement</span></span> 
- <span data-ttu-id="abe74-2867">le numéro BIC
</span><span class="sxs-lookup"><span data-stu-id="abe74-2867">le numéro BIC</span></span> 
- <span data-ttu-id="abe74-2868">\#BIC</span><span class="sxs-lookup"><span data-stu-id="abe74-2868">\# BIC</span></span> 
- <span data-ttu-id="abe74-2869">code identificateur de banque
</span><span class="sxs-lookup"><span data-stu-id="abe74-2869">code identificateur de banque</span></span> 
   
## <a name="taiwan-national-id"></a><span data-ttu-id="abe74-2870">ID national à Taïwan</span><span class="sxs-lookup"><span data-stu-id="abe74-2870">Taiwan National ID</span></span>

### <a name="format"></a><span data-ttu-id="abe74-2871">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-2871">Format</span></span>

<span data-ttu-id="abe74-2872">Une lettre  suivie de neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2872">One letter (in English) followed by nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-2873">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-2873">Pattern</span></span>

<span data-ttu-id="abe74-2874">Une lettre suivie de neuf chiffres :</span><span class="sxs-lookup"><span data-stu-id="abe74-2874">One letter (in English) followed by nine digits:</span></span>
- <span data-ttu-id="abe74-2875">Une lettre (en anglais, ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="abe74-2875">One letter (in English, not case sensitive)</span></span> 
- <span data-ttu-id="abe74-2876">Le chiffre « 1 » ou « 2 »</span><span class="sxs-lookup"><span data-stu-id="abe74-2876">The digit "1" or "2"</span></span> 
- <span data-ttu-id="abe74-2877">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2877">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-2878">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-2878">Checksum</span></span>

<span data-ttu-id="abe74-2879">Oui</span><span class="sxs-lookup"><span data-stu-id="abe74-2879">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-2880">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-2880">Definition</span></span>

<span data-ttu-id="abe74-2881">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2881">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2882">La fonction Func_taiwanese_national_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2882">The function Func_taiwanese_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2883">Un mot clé figurant dans la liste Keyword_taiwanese_national_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-2883">A keyword from Keyword_taiwanese_national_id is found.</span></span>
- <span data-ttu-id="abe74-2884">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-2884">The checksum passes.</span></span>

```
<!-- Taiwanese National ID -->
<Entity id="4C7BFC34-8DD1-421D-8FB7-6C6182C2AF03" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_taiwanese_national_id" />
          <Match idRef="Keyword_taiwanese_national_id" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe74-2885">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-2885">Keywords</span></span>

#### <a name="keywordtaiwanesenationalid"></a><span data-ttu-id="abe74-2886">Keyword_taiwanese_national_id</span><span class="sxs-lookup"><span data-stu-id="abe74-2886">Keyword_taiwanese_national_id</span></span>

- <span data-ttu-id="abe74-2887">身份證字號
</span><span class="sxs-lookup"><span data-stu-id="abe74-2887">身份證字號</span></span> 
- <span data-ttu-id="abe74-2888">身份證
</span><span class="sxs-lookup"><span data-stu-id="abe74-2888">身份證</span></span> 
- <span data-ttu-id="abe74-2889">身份證號碼
</span><span class="sxs-lookup"><span data-stu-id="abe74-2889">身份證號碼</span></span> 
- <span data-ttu-id="abe74-2890">身份證號
</span><span class="sxs-lookup"><span data-stu-id="abe74-2890">身份證號</span></span> 
- <span data-ttu-id="abe74-2891">身分證字號
</span><span class="sxs-lookup"><span data-stu-id="abe74-2891">身分證字號</span></span> 
- <span data-ttu-id="abe74-2892">身分證 </span><span class="sxs-lookup"><span data-stu-id="abe74-2892">身分證</span></span> 
- <span data-ttu-id="abe74-2893">身分證號碼
</span><span class="sxs-lookup"><span data-stu-id="abe74-2893">身分證號碼</span></span> 
- <span data-ttu-id="abe74-2894">身份證號
</span><span class="sxs-lookup"><span data-stu-id="abe74-2894">身份證號</span></span> 
- <span data-ttu-id="abe74-2895">身分證統一編號
</span><span class="sxs-lookup"><span data-stu-id="abe74-2895">身分證統一編號</span></span> 
- <span data-ttu-id="abe74-2896">國民身分證統一編號
</span><span class="sxs-lookup"><span data-stu-id="abe74-2896">國民身分證統一編號</span></span> 
- <span data-ttu-id="abe74-2897">簽名
</span><span class="sxs-lookup"><span data-stu-id="abe74-2897">簽名</span></span> 
- <span data-ttu-id="abe74-2898">蓋章
</span><span class="sxs-lookup"><span data-stu-id="abe74-2898">蓋章</span></span> 
- <span data-ttu-id="abe74-2899">簽名或蓋章

</span><span class="sxs-lookup"><span data-stu-id="abe74-2899">簽名或蓋章</span></span> 
- <span data-ttu-id="abe74-2900">簽章</span><span class="sxs-lookup"><span data-stu-id="abe74-2900">簽章</span></span>   
   
## <a name="taiwan-passport-number"></a><span data-ttu-id="abe74-2901">Numéro de passeport Taïwan</span><span class="sxs-lookup"><span data-stu-id="abe74-2901">Taiwan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-2902">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-2902">Format</span></span>

- <span data-ttu-id="abe74-2903">Numéro de passeport biométrique : neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2903">Biometric passport number: Nine digits</span></span>
- <span data-ttu-id="abe74-2904">Numéro de passeport non biométrique : neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2904">Non-biometric passport number: Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-2905">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-2905">Pattern</span></span>
<span data-ttu-id="abe74-2906">Numéro de passeport biométrique :</span><span class="sxs-lookup"><span data-stu-id="abe74-2906">Biometric passport number:</span></span>
- <span data-ttu-id="abe74-2907">Le chiffre « 3 » </span><span class="sxs-lookup"><span data-stu-id="abe74-2907">The digit "3"</span></span> 
- <span data-ttu-id="abe74-2908">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2908">Eight digits</span></span>

<span data-ttu-id="abe74-2909">Numéro de passeport non biométrique :</span><span class="sxs-lookup"><span data-stu-id="abe74-2909">Non-biometric passport number:</span></span>
- <span data-ttu-id="abe74-2910">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2910">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-2911">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-2911">Checksum</span></span>

<span data-ttu-id="abe74-2912">Non</span><span class="sxs-lookup"><span data-stu-id="abe74-2912">No</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-2913">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-2913">Definition</span></span>

<span data-ttu-id="abe74-2914">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2914">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2915">L’expression régulière Regex_taiwan_passport trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2915">The regular expression Regex_taiwan_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2916">Un mot clé figurant dans la liste Keyword_taiwan_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-2916">A keyword from Keyword_taiwan_passport is found.</span></span>

```
<!-- Taiwan Passport Number -->
<Entity id="e7251cb4-4c2c-41df-963e-924eb3dae04a" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_passport"/>
     <Match idRef="Keyword_taiwan_passport"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe74-2917">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-2917">Keywords</span></span>

#### <a name="keywordtaiwanpassport"></a><span data-ttu-id="abe74-2918">Keyword_taiwan_passport</span><span class="sxs-lookup"><span data-stu-id="abe74-2918">Keyword_taiwan_passport</span></span>

- <span data-ttu-id="abe74-2919">ROC passport number
</span><span class="sxs-lookup"><span data-stu-id="abe74-2919">ROC passport number</span></span> 
- <span data-ttu-id="abe74-2920">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="abe74-2920">Passport number</span></span> 
- <span data-ttu-id="abe74-2921">Passeport aucune</span><span class="sxs-lookup"><span data-stu-id="abe74-2921">Passport no</span></span> 
- <span data-ttu-id="abe74-2922">Passport Num
</span><span class="sxs-lookup"><span data-stu-id="abe74-2922">Passport Num</span></span> 
- <span data-ttu-id="abe74-2923"># Passeport
</span><span class="sxs-lookup"><span data-stu-id="abe74-2923">Passport #</span></span> 
- <span data-ttu-id="abe74-2924">护照
</span><span class="sxs-lookup"><span data-stu-id="abe74-2924">护照</span></span> 
- <span data-ttu-id="abe74-2925">中華民國護照
</span><span class="sxs-lookup"><span data-stu-id="abe74-2925">中華民國護照</span></span> 
- <span data-ttu-id="abe74-2926">Zhōnghuá Mínguó hùzhào</span><span class="sxs-lookup"><span data-stu-id="abe74-2926">Zhōnghuá Mínguó hùzhào</span></span>
   
## <a name="taiwan-resident-certificate-arctarc-number"></a><span data-ttu-id="abe74-2927">Numéro de certificat de résident (ARC/TARC) Taïwan</span><span class="sxs-lookup"><span data-stu-id="abe74-2927">Taiwan Resident Certificate (ARC/TARC) Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-2928">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-2928">Format</span></span>

<span data-ttu-id="abe74-2929">10 lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2929">10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-2930">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-2930">Pattern</span></span>

<span data-ttu-id="abe74-2931">10 lettres et chiffres :</span><span class="sxs-lookup"><span data-stu-id="abe74-2931">10 letters and digits:</span></span>
- <span data-ttu-id="abe74-2932">Deux lettres (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="abe74-2932">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="abe74-2933">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2933">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-2934">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-2934">Checksum</span></span>

<span data-ttu-id="abe74-2935">Non</span><span class="sxs-lookup"><span data-stu-id="abe74-2935">No</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-2936">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-2936">Definition</span></span>

<span data-ttu-id="abe74-2937">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2937">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2938">L’expression régulière Regex_taiwan_resident_certificate trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2938">The regular expression Regex_taiwan_resident_certificate finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2939">Un mot clé figurant dans la liste Keyword_taiwan_resident_certificate est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-2939">A keyword from Keyword_taiwan_resident_certificate is found.</span></span>

```
<!-- Taiwan Resident Certificate (ARC/TARC) -->
<Entity id="48269fec-05ea-46ea-b326-f5623a58c6e9" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_resident_certificate"/>
     <Match idRef="Keyword_taiwan_resident_certificate"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe74-2940">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-2940">Keywords</span></span>

#### <a name="keywordtaiwanresidentcertificate"></a><span data-ttu-id="abe74-2941">Keyword_taiwan_resident_certificate</span><span class="sxs-lookup"><span data-stu-id="abe74-2941">Keyword_taiwan_resident_certificate</span></span>

- <span data-ttu-id="abe74-2942">Resident Certificate
</span><span class="sxs-lookup"><span data-stu-id="abe74-2942">Resident Certificate</span></span> 
- <span data-ttu-id="abe74-2943">Cert résident</span><span class="sxs-lookup"><span data-stu-id="abe74-2943">Resident Cert</span></span> 
- <span data-ttu-id="abe74-2944">Resident Cert.
</span><span class="sxs-lookup"><span data-stu-id="abe74-2944">Resident Cert.</span></span> 
- <span data-ttu-id="abe74-2945">Carte d’identification</span><span class="sxs-lookup"><span data-stu-id="abe74-2945">Identification card</span></span> 
- <span data-ttu-id="abe74-2946">Alien Resident Certificate
</span><span class="sxs-lookup"><span data-stu-id="abe74-2946">Alien Resident Certificate</span></span> 
- <span data-ttu-id="abe74-2947">ARC
</span><span class="sxs-lookup"><span data-stu-id="abe74-2947">ARC</span></span> 
- <span data-ttu-id="abe74-2948">Taiwan Area Resident Certificate
</span><span class="sxs-lookup"><span data-stu-id="abe74-2948">Taiwan Area Resident Certificate</span></span> 
- <span data-ttu-id="abe74-2949">TARC
</span><span class="sxs-lookup"><span data-stu-id="abe74-2949">TARC</span></span> 
- <span data-ttu-id="abe74-2950">居留證
</span><span class="sxs-lookup"><span data-stu-id="abe74-2950">居留證</span></span> 
- <span data-ttu-id="abe74-2951">外僑居留證
</span><span class="sxs-lookup"><span data-stu-id="abe74-2951">外僑居留證</span></span> 
- <span data-ttu-id="abe74-2952">台灣地區居留證
</span><span class="sxs-lookup"><span data-stu-id="abe74-2952">台灣地區居留證</span></span> 
   
## <a name="uk-drivers-license-number"></a><span data-ttu-id="abe74-p141">Numéro de permis de conduire Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="abe74-p141">U.K. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-2955">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-2955">Format</span></span>

<span data-ttu-id="abe74-2956">Combinaison de 18 lettres et chiffres au format spécifié</span><span class="sxs-lookup"><span data-stu-id="abe74-2956">Combination of 18 letters and digits in the specified format</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-2957">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-2957">Pattern</span></span>

<span data-ttu-id="abe74-2958">18 lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2958">18 letters and digits:</span></span>
- <span data-ttu-id="abe74-2959">Cinq lettres (ne respectent pas la casse) ou le chiffre « 9 » à la place d’une lettre</span><span class="sxs-lookup"><span data-stu-id="abe74-2959">Five letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="abe74-2960">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="abe74-2960">One digit</span></span> 
- <span data-ttu-id="abe74-2961">Cinq chiffres au format de date JJMMA pour la date de naissance</span><span class="sxs-lookup"><span data-stu-id="abe74-2961">Five digits in the date format DDMMY for date of birth</span></span> 
- <span data-ttu-id="abe74-2962">Deux lettres (ne respectent pas la casse) ou le chiffre « 9 » à la place d’une lettre</span><span class="sxs-lookup"><span data-stu-id="abe74-2962">Two letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="abe74-2963">Cinq chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2963">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-2964">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-2964">Checksum</span></span>

<span data-ttu-id="abe74-2965">Oui</span><span class="sxs-lookup"><span data-stu-id="abe74-2965">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-2966">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-2966">Definition</span></span>

<span data-ttu-id="abe74-2967">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2967">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2968">La fonction Func_uk_drivers_license trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2968">The function Func_uk_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2969">Un mot clé figurant dans la liste Keyword_uk_drivers_license est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-2969">A keyword from Keyword_uk_drivers_license is found.</span></span>
- <span data-ttu-id="abe74-2970">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-2970">The checksum passes.</span></span>

```
<!-- U.K. Driver's License Number -->
<Entity id="f93de4be-d94c-40df-a8be-461738047551" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_uk_drivers_license" />
        <Match idRef="Keyword_uk_drivers_license" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe74-2971">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-2971">Keywords</span></span>

#### <a name="keywordukdriverslicense"></a><span data-ttu-id="abe74-2972">Keyword_uk_drivers_license</span><span class="sxs-lookup"><span data-stu-id="abe74-2972">Keyword_uk_drivers_license</span></span>

- <span data-ttu-id="abe74-2973">DVLA
</span><span class="sxs-lookup"><span data-stu-id="abe74-2973">DVLA</span></span> 
- <span data-ttu-id="abe74-2974">véhicule utilitaire léger
</span><span class="sxs-lookup"><span data-stu-id="abe74-2974">light vans</span></span> 
- <span data-ttu-id="abe74-2975">quad
</span><span class="sxs-lookup"><span data-stu-id="abe74-2975">quadbikes</span></span> 
- <span data-ttu-id="abe74-2976">automobiles
</span><span class="sxs-lookup"><span data-stu-id="abe74-2976">motor cars</span></span> 
- <span data-ttu-id="abe74-2977">125cc</span><span class="sxs-lookup"><span data-stu-id="abe74-2977">125cc</span></span> 
- <span data-ttu-id="abe74-2978">sidecar
</span><span class="sxs-lookup"><span data-stu-id="abe74-2978">sidecar</span></span> 
- <span data-ttu-id="abe74-2979">tricycles
</span><span class="sxs-lookup"><span data-stu-id="abe74-2979">tricycles</span></span> 
- <span data-ttu-id="abe74-2980">motocycles
</span><span class="sxs-lookup"><span data-stu-id="abe74-2980">motorcycles</span></span> 
- <span data-ttu-id="abe74-2981">permis de conduire plastifié
</span><span class="sxs-lookup"><span data-stu-id="abe74-2981">photocard licence</span></span> 
- <span data-ttu-id="abe74-2982">apprentis conducteurs
</span><span class="sxs-lookup"><span data-stu-id="abe74-2982">learner drivers</span></span> 
- <span data-ttu-id="abe74-2983">titulaire du permis
</span><span class="sxs-lookup"><span data-stu-id="abe74-2983">licence holder</span></span> 
- <span data-ttu-id="abe74-2984">titulaires du permis
</span><span class="sxs-lookup"><span data-stu-id="abe74-2984">licence holders</span></span> 
- <span data-ttu-id="abe74-2985">permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-2985">driving licences</span></span> 
- <span data-ttu-id="abe74-2986">permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-2986">driving licence</span></span> 
- <span data-ttu-id="abe74-2987">voiture à double commande
</span><span class="sxs-lookup"><span data-stu-id="abe74-2987">dual control car</span></span> 
   
## <a name="uk-electoral-roll-number"></a><span data-ttu-id="abe74-p142">Numéro de liste électorale Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="abe74-p142">U.K. Electoral Roll Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-2990">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-2990">Format</span></span>

<span data-ttu-id="abe74-2991">Deux lettres suivies de 1 à 4 chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2991">Two letters followed by 1-4 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-2992">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-2992">Pattern</span></span>

<span data-ttu-id="abe74-2993">Deux lettres (ne respectant pas la casse) suivies de 1 à 4 chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-2993">Two letters (not case sensitive) followed by 1-4 numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-2994">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-2994">Checksum</span></span>

<span data-ttu-id="abe74-2995">Non</span><span class="sxs-lookup"><span data-stu-id="abe74-2995">No</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-2996">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-2996">Definition</span></span>

<span data-ttu-id="abe74-2997">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-2997">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-2998">L’expression régulière Regex_uk_electoral trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-2998">The regular expression Regex_uk_electoral finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-2999">Un mot clé figurant dans la liste Keyword_uk_electoral est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-2999">A keyword from Keyword_uk_electoral is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-3000">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-3000">Keywords</span></span>

#### <a name="keywordukelectoral"></a><span data-ttu-id="abe74-3001">Keyword_uk_electoral</span><span class="sxs-lookup"><span data-stu-id="abe74-3001">Keyword_uk_electoral</span></span>

- <span data-ttu-id="abe74-3002">nomination au conseil
</span><span class="sxs-lookup"><span data-stu-id="abe74-3002">council nomination</span></span> 
- <span data-ttu-id="abe74-3003">formulaire de nomination
</span><span class="sxs-lookup"><span data-stu-id="abe74-3003">nomination form</span></span> 
- <span data-ttu-id="abe74-3004">registre électoral

</span><span class="sxs-lookup"><span data-stu-id="abe74-3004">electoral register</span></span> 
- <span data-ttu-id="abe74-3005">liste électorale</span><span class="sxs-lookup"><span data-stu-id="abe74-3005">electoral roll</span></span>

   
## <a name="uk-national-health-service-number"></a><span data-ttu-id="abe74-p143">Numéro national des services de santé Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="abe74-p143">U.K. National Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-3008">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-3008">Format</span></span>

<span data-ttu-id="abe74-3009">10 à 17 chiffres séparés par des espaces</span><span class="sxs-lookup"><span data-stu-id="abe74-3009">10-17 digits separated by spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-3010">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-3010">Pattern</span></span>

<span data-ttu-id="abe74-3011">10 à 17 chiffres :</span><span class="sxs-lookup"><span data-stu-id="abe74-3011">10-17 digits:</span></span>
- <span data-ttu-id="abe74-3012">3 ou 10 chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-3012">Either 3 or 10 digits</span></span> 
- <span data-ttu-id="abe74-3013">Un espace</span><span class="sxs-lookup"><span data-stu-id="abe74-3013">A space</span></span> 
- <span data-ttu-id="abe74-3014">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-3014">Three digits</span></span> 
- <span data-ttu-id="abe74-3015">Un espace</span><span class="sxs-lookup"><span data-stu-id="abe74-3015">A space</span></span> 
- <span data-ttu-id="abe74-3016">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-3016">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-3017">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-3017">Checksum</span></span>

<span data-ttu-id="abe74-3018">Oui</span><span class="sxs-lookup"><span data-stu-id="abe74-3018">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-3019">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-3019">Definition</span></span>

<span data-ttu-id="abe74-3020">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-3020">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-3021">La fonction Func_uk_nhs_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-3021">The function Func_uk_nhs_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-3022">L’une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="abe74-3022">One of the following is true:</span></span>
    - <span data-ttu-id="abe74-3023">Un mot clé figurant dans la liste Keyword_uk_nhs_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-3023">A keyword from Keyword_uk_nhs_number is found.</span></span>
    - <span data-ttu-id="abe74-3024">Un mot clé figurant dans la liste Keyword_uk_nhs_number1 est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-3024">A keyword from Keyword_uk_nhs_number1 is found.</span></span>
    - <span data-ttu-id="abe74-3025">Un mot clé figurant dans la liste Keyword_uk_nhs_number_dob est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-3025">A keyword from Keyword_uk_nhs_number_dob is found.</span></span>
- <span data-ttu-id="abe74-3026">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="abe74-3026">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-3027">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-3027">Keywords</span></span>
   
#### <a name="keyworduknhsnumber"></a><span data-ttu-id="abe74-3028">Keyword_uk_nhs_number</span><span class="sxs-lookup"><span data-stu-id="abe74-3028">Keyword_uk_nhs_number</span></span>

- <span data-ttu-id="abe74-3029">service national de santé
</span><span class="sxs-lookup"><span data-stu-id="abe74-3029">national health service</span></span> 
- <span data-ttu-id="abe74-3030">NHS
</span><span class="sxs-lookup"><span data-stu-id="abe74-3030">nhs</span></span> 
- <span data-ttu-id="abe74-3031">administration des services de santé

</span><span class="sxs-lookup"><span data-stu-id="abe74-3031">health services authority</span></span> 
- <span data-ttu-id="abe74-3032">administration de la santé</span><span class="sxs-lookup"><span data-stu-id="abe74-3032">health authority</span></span>

#### <a name="keyworduknhsnumber1"></a><span data-ttu-id="abe74-3033">Keyword_uk_nhs_number1</span><span class="sxs-lookup"><span data-stu-id="abe74-3033">Keyword_uk_nhs_number1</span></span>

- <span data-ttu-id="abe74-3034">id du patient
</span><span class="sxs-lookup"><span data-stu-id="abe74-3034">patient id</span></span> 
- <span data-ttu-id="abe74-3035">identification du patient
</span><span class="sxs-lookup"><span data-stu-id="abe74-3035">patient identification</span></span> 
- <span data-ttu-id="abe74-3036">n° patient

</span><span class="sxs-lookup"><span data-stu-id="abe74-3036">patient no</span></span> 
- <span data-ttu-id="abe74-3037">numéro de patient</span><span class="sxs-lookup"><span data-stu-id="abe74-3037">patient number</span></span>

#### <a name="keyworduknhsnumberdob"></a><span data-ttu-id="abe74-3038">Keyword_uk_nhs_number_dob</span><span class="sxs-lookup"><span data-stu-id="abe74-3038">Keyword_uk_nhs_number_dob</span></span>

- <span data-ttu-id="abe74-3039">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="abe74-3039">GP</span></span> 
- <span data-ttu-id="abe74-3040">DDN
</span><span class="sxs-lookup"><span data-stu-id="abe74-3040">DOB</span></span> 
- <span data-ttu-id="abe74-3041">D.O.B</span><span class="sxs-lookup"><span data-stu-id="abe74-3041">D.O.B</span></span> 
- <span data-ttu-id="abe74-3042">Date of Birth
</span><span class="sxs-lookup"><span data-stu-id="abe74-3042">Date of Birth</span></span> 
- <span data-ttu-id="abe74-3043">Birth Date
</span><span class="sxs-lookup"><span data-stu-id="abe74-3043">Birth Date</span></span> 
   
## <a name="uk-national-insurance-number-nino"></a><span data-ttu-id="abe74-p144">Numéro d'assurance nationale (NINO) Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="abe74-p144">U.K. National Insurance Number (NINO)</span></span>

### <a name="format"></a><span data-ttu-id="abe74-3046">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-3046">Format</span></span>

<span data-ttu-id="abe74-3047">7 caractères ou 9 caractères séparés par des espaces ou des tirets</span><span class="sxs-lookup"><span data-stu-id="abe74-3047">7 characters or 9 characters separated by spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-3048">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-3048">Pattern</span></span>

<span data-ttu-id="abe74-3049">Deux modèles possibles :</span><span class="sxs-lookup"><span data-stu-id="abe74-3049">Two possible patterns:</span></span>

- <span data-ttu-id="abe74-3050">Deux lettres (valides NINOs utilisent uniquement certains caractères dans ce préfixe, ce modèle est valide ; pas la casse)</span><span class="sxs-lookup"><span data-stu-id="abe74-3050">Two letters (valid NINOs use only certain characters in this prefix, which this pattern validates; not case sensitive)</span></span>
- <span data-ttu-id="abe74-3051">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-3051">Six digits</span></span>
- <span data-ttu-id="abe74-3052">Soit « A », « B », « C », ou a ' (comme le préfixe, seuls certains caractères sont autorisés dans le suffixe ; pas respectant la casse)</span><span class="sxs-lookup"><span data-stu-id="abe74-3052">Either 'A', 'B', 'C', or 'D' (like the prefix, only certain characters are allowed in the suffix; not case sensitive)</span></span>

<span data-ttu-id="abe74-3053">OU</span><span class="sxs-lookup"><span data-stu-id="abe74-3053">OR</span></span>

- <span data-ttu-id="abe74-3054">Deux lettres</span><span class="sxs-lookup"><span data-stu-id="abe74-3054">Two letters</span></span>
- <span data-ttu-id="abe74-3055">Un espace ou un tiret</span><span class="sxs-lookup"><span data-stu-id="abe74-3055">A space or dash</span></span>
- <span data-ttu-id="abe74-3056">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-3056">Two digits</span></span>
- <span data-ttu-id="abe74-3057">Un espace ou un tiret</span><span class="sxs-lookup"><span data-stu-id="abe74-3057">A space or dash</span></span>
- <span data-ttu-id="abe74-3058">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-3058">Two digits</span></span>
- <span data-ttu-id="abe74-3059">Un espace ou un tiret</span><span class="sxs-lookup"><span data-stu-id="abe74-3059">A space or dash</span></span>
- <span data-ttu-id="abe74-3060">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-3060">Two digits</span></span>
- <span data-ttu-id="abe74-3061">Un espace ou un tiret</span><span class="sxs-lookup"><span data-stu-id="abe74-3061">A space or dash</span></span>
- <span data-ttu-id="abe74-3062">'A', 'B', « C », ou a '</span><span class="sxs-lookup"><span data-stu-id="abe74-3062">Either 'A', 'B', 'C', or 'D'</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-3063">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-3063">Checksum</span></span>

<span data-ttu-id="abe74-3064">Non</span><span class="sxs-lookup"><span data-stu-id="abe74-3064">No</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-3065">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-3065">Definition</span></span>

<span data-ttu-id="abe74-3066">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-3066">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-3067">La fonction Func_uk_nino trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-3067">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-3068">Un mot clé figurant dans la liste Keyword_uk_nino est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-3068">A keyword from Keyword_uk_nino is found.</span></span>

<span data-ttu-id="abe74-3069">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-3069">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-3070">La fonction Func_uk_nino trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-3070">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-3071">Aucun mot clé figurant dans la liste Keyword_uk_nino n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-3071">No keyword from Keyword_uk_nino is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-3072">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-3072">Keywords</span></span>

#### <a name="keyworduknino"></a><span data-ttu-id="abe74-3073">Keyword_uk_nino</span><span class="sxs-lookup"><span data-stu-id="abe74-3073">Keyword_uk_nino</span></span>

- <span data-ttu-id="abe74-3074">numéro d’assurance nationale
</span><span class="sxs-lookup"><span data-stu-id="abe74-3074">national insurance number</span></span> 
- <span data-ttu-id="abe74-3075">cotisations sociales
</span><span class="sxs-lookup"><span data-stu-id="abe74-3075">national insurance contributions</span></span> 
- <span data-ttu-id="abe74-3076">loi sur la protection
</span><span class="sxs-lookup"><span data-stu-id="abe74-3076">protection act</span></span> 
- <span data-ttu-id="abe74-3077">assurance
</span><span class="sxs-lookup"><span data-stu-id="abe74-3077">insurance</span></span> 
- <span data-ttu-id="abe74-3078">numéro de sécurité sociale
</span><span class="sxs-lookup"><span data-stu-id="abe74-3078">social security number</span></span> 
- <span data-ttu-id="abe74-3079">demande d’assurance
</span><span class="sxs-lookup"><span data-stu-id="abe74-3079">insurance application</span></span> 
- <span data-ttu-id="abe74-3080">demande de soins médicaux
</span><span class="sxs-lookup"><span data-stu-id="abe74-3080">medical application</span></span> 
- <span data-ttu-id="abe74-3081">assurance sociale
</span><span class="sxs-lookup"><span data-stu-id="abe74-3081">social insurance</span></span> 
- <span data-ttu-id="abe74-3082">soins médicaux
</span><span class="sxs-lookup"><span data-stu-id="abe74-3082">medical attention</span></span> 
- <span data-ttu-id="abe74-3083">sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="abe74-3083">social security</span></span> 
- <span data-ttu-id="abe74-3084">grande-bretagne
</span><span class="sxs-lookup"><span data-stu-id="abe74-3084">great britain</span></span> 
- <span data-ttu-id="abe74-3085">assurance
</span><span class="sxs-lookup"><span data-stu-id="abe74-3085">insurance</span></span>    
   
## <a name="us--uk-passport-number"></a><span data-ttu-id="abe74-p145">Numéro de passeport États-Unis/Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="abe74-p145">U.S. / U.K. Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-3088">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-3088">Format</span></span>

<span data-ttu-id="abe74-3089">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-3089">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-3090">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-3090">Pattern</span></span>

<span data-ttu-id="abe74-3091">Neuf chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="abe74-3091">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-3092">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-3092">Checksum</span></span>

<span data-ttu-id="abe74-3093">Non</span><span class="sxs-lookup"><span data-stu-id="abe74-3093">No</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-3094">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-3094">Definition</span></span>

<span data-ttu-id="abe74-3095">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-3095">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-3096">La fonction Func_usa_uk_passport trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-3096">The function Func_usa_uk_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-3097">Un mot clé figurant dans la liste Keyword_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-3097">A keyword from Keyword_passport is found.</span></span>

```
<Entity id="178ec42a-18b4-47cc-85c7-d62c92fd67f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_usa_uk_passport" />
        <Match idRef="Keyword_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe74-3098">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-3098">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="abe74-3099">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="abe74-3099">Keyword_passport</span></span>

- <span data-ttu-id="abe74-3100">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="abe74-3100">Passport Number</span></span> 
- <span data-ttu-id="abe74-3101">
N° de passeport</span><span class="sxs-lookup"><span data-stu-id="abe74-3101">Passport No</span></span> 
- <span data-ttu-id="abe74-3102"># Passeport
</span><span class="sxs-lookup"><span data-stu-id="abe74-3102">Passport #</span></span> 
- <span data-ttu-id="abe74-3103">#Passeport
</span><span class="sxs-lookup"><span data-stu-id="abe74-3103">Passport#</span></span> 
- <span data-ttu-id="abe74-3104">IDPassport</span><span class="sxs-lookup"><span data-stu-id="abe74-3104">PassportID</span></span> 
- <span data-ttu-id="abe74-3105">n° passeport
</span><span class="sxs-lookup"><span data-stu-id="abe74-3105">Passportno</span></span> 
- <span data-ttu-id="abe74-3106">numéropasseport
</span><span class="sxs-lookup"><span data-stu-id="abe74-3106">passportnumber</span></span> 
- <span data-ttu-id="abe74-3107">パスポート</span><span class="sxs-lookup"><span data-stu-id="abe74-3107">パスポート</span></span> 
- <span data-ttu-id="abe74-3108">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="abe74-3108">パスポート番号</span></span> 
- <span data-ttu-id="abe74-3109">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="abe74-3109">パスポートのNum</span></span> 
- <span data-ttu-id="abe74-3110">パスポート＃
</span><span class="sxs-lookup"><span data-stu-id="abe74-3110">パスポート＃</span></span> 
- <span data-ttu-id="abe74-3111">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="abe74-3111">Numéro de passeport</span></span> 
- <span data-ttu-id="abe74-3112">
Passeport n°</span><span class="sxs-lookup"><span data-stu-id="abe74-3112">Passeport n °</span></span> 
- <span data-ttu-id="abe74-3113">Passeport numéro
</span><span class="sxs-lookup"><span data-stu-id="abe74-3113">Passeport Non</span></span> 
- <span data-ttu-id="abe74-3114"># Passeport
</span><span class="sxs-lookup"><span data-stu-id="abe74-3114">Passeport #</span></span> 
- <span data-ttu-id="abe74-3115">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="abe74-3115">Passeport#</span></span> 
- <span data-ttu-id="abe74-3116">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="abe74-3116">PasseportNon</span></span> 
- <span data-ttu-id="abe74-3117">Passeportn °
</span><span class="sxs-lookup"><span data-stu-id="abe74-3117">Passeportn °</span></span> 
   
## <a name="us-bank-account-number"></a><span data-ttu-id="abe74-3118">Numéro de compte bancaire États-Unis</span><span class="sxs-lookup"><span data-stu-id="abe74-3118">U.S. Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-3119">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-3119">Format</span></span>

<span data-ttu-id="abe74-3120">8-17 chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-3120">8-17 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-3121">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-3121">Pattern</span></span>

<span data-ttu-id="abe74-3122">8 à 17 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="abe74-3122">8-17 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-3123">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-3123">Checksum</span></span>

<span data-ttu-id="abe74-3124">Non</span><span class="sxs-lookup"><span data-stu-id="abe74-3124">No</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-3125">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-3125">Definition</span></span>

<span data-ttu-id="abe74-3126">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-3126">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-3127">L’expression régulière Regex_usa_bank_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-3127">The regular expression Regex_usa_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-3128">Un mot clé figurant dans la liste Keyword_usa_Bank_Account est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-3128">A keyword from Keyword_usa_Bank_Account is found.</span></span>

```
<!-- U.S. Bank Account Number -->
<Entity id="a2ce32a8-f935-4bb6-8e96-2a5157672e2c" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_usa_bank_account_number" />
        <Match idRef="Keyword_usa_Bank_Account" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe74-3129">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-3129">Keywords</span></span>

#### <a name="keywordusabankaccount"></a><span data-ttu-id="abe74-3130">Keyword_usa_Bank_Account</span><span class="sxs-lookup"><span data-stu-id="abe74-3130">Keyword_usa_Bank_Account</span></span>

- <span data-ttu-id="abe74-3131">Numéro de compte courant
</span><span class="sxs-lookup"><span data-stu-id="abe74-3131">Checking Account Number</span></span> 
- <span data-ttu-id="abe74-3132">Compte courant
</span><span class="sxs-lookup"><span data-stu-id="abe74-3132">Checking Account</span></span> 
- <span data-ttu-id="abe74-3133"># compte courant
</span><span class="sxs-lookup"><span data-stu-id="abe74-3133">Checking Account #</span></span> 
- <span data-ttu-id="abe74-3134">Numéro compte courant
</span><span class="sxs-lookup"><span data-stu-id="abe74-3134">Checking Acct Number</span></span> 
- <span data-ttu-id="abe74-3135"># compte courant
</span><span class="sxs-lookup"><span data-stu-id="abe74-3135">Checking Acct #</span></span> 
- <span data-ttu-id="abe74-3136">N° de compte courant
</span><span class="sxs-lookup"><span data-stu-id="abe74-3136">Checking Acct No.</span></span> 
- <span data-ttu-id="abe74-3137">N° de compte courant
</span><span class="sxs-lookup"><span data-stu-id="abe74-3137">Checking Account No.</span></span> 
- <span data-ttu-id="abe74-3138">Numéro de compte bancaire
</span><span class="sxs-lookup"><span data-stu-id="abe74-3138">Bank Account Number</span></span> 
- <span data-ttu-id="abe74-3139"># Compte bancaire
</span><span class="sxs-lookup"><span data-stu-id="abe74-3139">Bank Account #</span></span> 
- <span data-ttu-id="abe74-3140">Numéro de compte bancaire
</span><span class="sxs-lookup"><span data-stu-id="abe74-3140">Bank Acct Number</span></span> 
- <span data-ttu-id="abe74-3141"># Compte bancaire
</span><span class="sxs-lookup"><span data-stu-id="abe74-3141">Bank Acct #</span></span> 
- <span data-ttu-id="abe74-3142">N° de compte bancaire
</span><span class="sxs-lookup"><span data-stu-id="abe74-3142">Bank Acct No.</span></span> 
- <span data-ttu-id="abe74-3143">N° de compte bancaire
</span><span class="sxs-lookup"><span data-stu-id="abe74-3143">Bank Account No.</span></span> 
- <span data-ttu-id="abe74-3144">Numéro de compte d’épargne
</span><span class="sxs-lookup"><span data-stu-id="abe74-3144">Savings Account Number</span></span> 
- <span data-ttu-id="abe74-3145">Compte d’épargne.
</span><span class="sxs-lookup"><span data-stu-id="abe74-3145">Savings Account.</span></span> 
- <span data-ttu-id="abe74-3146">N° de compte d’épargne
</span><span class="sxs-lookup"><span data-stu-id="abe74-3146">Savings Account #</span></span> 
- <span data-ttu-id="abe74-3147">Numéro de compte d’épargne
</span><span class="sxs-lookup"><span data-stu-id="abe74-3147">Savings Acct Number</span></span> 
- <span data-ttu-id="abe74-3148"># compte d’épargne
</span><span class="sxs-lookup"><span data-stu-id="abe74-3148">Savings Acct #</span></span> 
- <span data-ttu-id="abe74-3149">N° de compte d’épargne
</span><span class="sxs-lookup"><span data-stu-id="abe74-3149">Savings Acct No.</span></span> 
- <span data-ttu-id="abe74-3150">N° de compte d’épargne
</span><span class="sxs-lookup"><span data-stu-id="abe74-3150">Savings Account No.</span></span> 
- <span data-ttu-id="abe74-3151">Numéro de compte de débit
</span><span class="sxs-lookup"><span data-stu-id="abe74-3151">Debit Account Number</span></span> 
- <span data-ttu-id="abe74-3152">Compte de débit
</span><span class="sxs-lookup"><span data-stu-id="abe74-3152">Debit Account</span></span> 
- <span data-ttu-id="abe74-3153"># Compte de débit
</span><span class="sxs-lookup"><span data-stu-id="abe74-3153">Debit Account #</span></span> 
- <span data-ttu-id="abe74-3154">Numéro de compte de débit
</span><span class="sxs-lookup"><span data-stu-id="abe74-3154">Debit Acct Number</span></span> 
- <span data-ttu-id="abe74-3155"># Compte de débit
</span><span class="sxs-lookup"><span data-stu-id="abe74-3155">Debit Acct #</span></span> 
- <span data-ttu-id="abe74-3156">N° de compte de débit
</span><span class="sxs-lookup"><span data-stu-id="abe74-3156">Debit Acct No.</span></span> 
- <span data-ttu-id="abe74-3157">N° de compte de débit
</span><span class="sxs-lookup"><span data-stu-id="abe74-3157">Debit Account No.</span></span> 
   
## <a name="us-drivers-license-number"></a><span data-ttu-id="abe74-3158">Numéro de permis de conduire États-Unis</span><span class="sxs-lookup"><span data-stu-id="abe74-3158">U.S. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="abe74-3159">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-3159">Format</span></span>

<span data-ttu-id="abe74-3160">Dépend de l’État</span><span class="sxs-lookup"><span data-stu-id="abe74-3160">Depends on the state</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-3161">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-3161">Pattern</span></span>

<span data-ttu-id="abe74-3162">Dépend de l’État, par exemple, New York :</span><span class="sxs-lookup"><span data-stu-id="abe74-3162">Depends on the state -- for example, New York:</span></span>
- <span data-ttu-id="abe74-3163">Neuf chiffres au format ddd ddd ddd correspondront.</span><span class="sxs-lookup"><span data-stu-id="abe74-3163">Nine digits formatted like ddd ddd ddd will match.</span></span>
- <span data-ttu-id="abe74-3164">Neuf chiffres au format ddddddddd ne correspondront pas.</span><span class="sxs-lookup"><span data-stu-id="abe74-3164">Nine digits like ddddddddd will not match.</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-3165">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-3165">Checksum</span></span>

<span data-ttu-id="abe74-3166">Non</span><span class="sxs-lookup"><span data-stu-id="abe74-3166">No</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-3167">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-3167">Definition</span></span>

<span data-ttu-id="abe74-3168">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-3168">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-3169">La fonction Func_new_york_drivers_license_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-3169">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-3170">Un mot clé figurant dans la liste Keyword_[state_name]_drivers_license_name est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-3170">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="abe74-3171">Un mot clé figurant dans la liste Keyword_us_drivers_license est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-3171">A keyword from Keyword_us_drivers_license is found.</span></span>

<span data-ttu-id="abe74-3172">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-3172">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-3173">La fonction Func_new_york_drivers_license_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-3173">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-3174">Un mot clé figurant dans la liste Keyword_[state_name]_drivers_license_name est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-3174">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="abe74-3175">Un mot clé figurant dans la liste Keyword_us_drivers_license_abbreviations est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-3175">A keyword from Keyword_us_drivers_license_abbreviations is found.</span></span>
- <span data-ttu-id="abe74-3176">Aucun mot clé figurant dans la liste Keyword_us_drivers_license n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-3176">No keyword from Keyword_us_drivers_license is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-3177">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-3177">Keywords</span></span>

#### <a name="keywordusdriverslicenseabbreviations"></a><span data-ttu-id="abe74-3178">Keyword_us_drivers_license_abbreviations</span><span class="sxs-lookup"><span data-stu-id="abe74-3178">Keyword_us_drivers_license_abbreviations</span></span>

- <span data-ttu-id="abe74-3179">PC</span><span class="sxs-lookup"><span data-stu-id="abe74-3179">DL</span></span> 
- <span data-ttu-id="abe74-3180">PC</span><span class="sxs-lookup"><span data-stu-id="abe74-3180">DLS</span></span> 
- <span data-ttu-id="abe74-3181">CDL</span><span class="sxs-lookup"><span data-stu-id="abe74-3181">CDL</span></span> 
- <span data-ttu-id="abe74-3182">SYSTÈMES CDL</span><span class="sxs-lookup"><span data-stu-id="abe74-3182">CDLS</span></span> 
- <span data-ttu-id="abe74-3183">ID</span><span class="sxs-lookup"><span data-stu-id="abe74-3183">ID</span></span> 
- <span data-ttu-id="abe74-3184">ID</span><span class="sxs-lookup"><span data-stu-id="abe74-3184">IDs</span></span> 
- <span data-ttu-id="abe74-3185"># PC</span><span class="sxs-lookup"><span data-stu-id="abe74-3185">DL#</span></span> 
- <span data-ttu-id="abe74-3186">
# PC
</span><span class="sxs-lookup"><span data-stu-id="abe74-3186">DLS#</span></span> 
- <span data-ttu-id="abe74-3187"># PCD
</span><span class="sxs-lookup"><span data-stu-id="abe74-3187">CDL#</span></span> 
- <span data-ttu-id="abe74-3188"># PCD
</span><span class="sxs-lookup"><span data-stu-id="abe74-3188">CDLS#</span></span> 
- <span data-ttu-id="abe74-3189">#ID</span><span class="sxs-lookup"><span data-stu-id="abe74-3189">ID#</span></span>
- <span data-ttu-id="abe74-3190">
#IDs
</span><span class="sxs-lookup"><span data-stu-id="abe74-3190">IDs#</span></span> 
- <span data-ttu-id="abe74-3191">numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="abe74-3191">ID number</span></span> 
- <span data-ttu-id="abe74-3192">Numéros d’identification
</span><span class="sxs-lookup"><span data-stu-id="abe74-3192">ID numbers</span></span> 
- <span data-ttu-id="abe74-3193">LIC</span><span class="sxs-lookup"><span data-stu-id="abe74-3193">LIC</span></span> 
- <span data-ttu-id="abe74-3194"># PERMIS
</span><span class="sxs-lookup"><span data-stu-id="abe74-3194">LIC#</span></span> 

#### <a name="keywordusdriverslicense"></a><span data-ttu-id="abe74-3195">Keyword_us_drivers_license</span><span class="sxs-lookup"><span data-stu-id="abe74-3195">Keyword_us_drivers_license</span></span>

- <span data-ttu-id="abe74-3196">DriverLic</span><span class="sxs-lookup"><span data-stu-id="abe74-3196">DriverLic</span></span> 
- <span data-ttu-id="abe74-3197">DriverLics</span><span class="sxs-lookup"><span data-stu-id="abe74-3197">DriverLics</span></span> 
- <span data-ttu-id="abe74-3198">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="abe74-3198">DriverLicense</span></span> 
- <span data-ttu-id="abe74-3199">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="abe74-3199">DriverLicenses</span></span> 
- <span data-ttu-id="abe74-3200">Lic pilote</span><span class="sxs-lookup"><span data-stu-id="abe74-3200">Driver Lic</span></span> 
- <span data-ttu-id="abe74-3201">Pilote Lics</span><span class="sxs-lookup"><span data-stu-id="abe74-3201">Driver Lics</span></span> 
- <span data-ttu-id="abe74-3202">Conduire</span><span class="sxs-lookup"><span data-stu-id="abe74-3202">Driver License</span></span> 
- <span data-ttu-id="abe74-3203">Licences de pilote</span><span class="sxs-lookup"><span data-stu-id="abe74-3203">Driver Licenses</span></span> 
- <span data-ttu-id="abe74-3204">DriversLic</span><span class="sxs-lookup"><span data-stu-id="abe74-3204">DriversLic</span></span> 
- <span data-ttu-id="abe74-3205">DriversLics</span><span class="sxs-lookup"><span data-stu-id="abe74-3205">DriversLics</span></span> 
- <span data-ttu-id="abe74-3206">Conduire</span><span class="sxs-lookup"><span data-stu-id="abe74-3206">DriversLicense</span></span> 
- <span data-ttu-id="abe74-3207">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="abe74-3207">DriversLicenses</span></span> 
- <span data-ttu-id="abe74-3208">Lic pilotes</span><span class="sxs-lookup"><span data-stu-id="abe74-3208">Drivers Lic</span></span> 
- <span data-ttu-id="abe74-3209">Lics pilotes</span><span class="sxs-lookup"><span data-stu-id="abe74-3209">Drivers Lics</span></span> 
- <span data-ttu-id="abe74-3210">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="abe74-3210">Drivers License</span></span> 
- <span data-ttu-id="abe74-3211">Licences de pilotes</span><span class="sxs-lookup"><span data-stu-id="abe74-3211">Drivers Licenses</span></span> 
- <span data-ttu-id="abe74-3212">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="abe74-3212">Driver'Lic</span></span> 
- <span data-ttu-id="abe74-3213">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="abe74-3213">Driver'Lics</span></span> 
- <span data-ttu-id="abe74-3214">Driver'License</span><span class="sxs-lookup"><span data-stu-id="abe74-3214">Driver'License</span></span> 
- <span data-ttu-id="abe74-3215">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="abe74-3215">Driver'Licenses</span></span> 
- <span data-ttu-id="abe74-3216">Pilote ' Lic</span><span class="sxs-lookup"><span data-stu-id="abe74-3216">Driver' Lic</span></span> 
- <span data-ttu-id="abe74-3217">Pilote ' Lics</span><span class="sxs-lookup"><span data-stu-id="abe74-3217">Driver' Lics</span></span> 
- <span data-ttu-id="abe74-3218">Pilote ' licence</span><span class="sxs-lookup"><span data-stu-id="abe74-3218">Driver' License</span></span> 
- <span data-ttu-id="abe74-3219">Pilote ' licences</span><span class="sxs-lookup"><span data-stu-id="abe74-3219">Driver' Licenses</span></span>
- <span data-ttu-id="abe74-3220">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="abe74-3220">Driver'sLic</span></span> 
- <span data-ttu-id="abe74-3221">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="abe74-3221">Driver'sLics</span></span> 
- <span data-ttu-id="abe74-3222">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="abe74-3222">Driver'sLicense</span></span> 
- <span data-ttu-id="abe74-3223">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="abe74-3223">Driver'sLicenses</span></span> 
- <span data-ttu-id="abe74-3224">Lic du pilote</span><span class="sxs-lookup"><span data-stu-id="abe74-3224">Driver's Lic</span></span> 
- <span data-ttu-id="abe74-3225">Lics permis de conduire</span><span class="sxs-lookup"><span data-stu-id="abe74-3225">Driver's Lics</span></span> 
- <span data-ttu-id="abe74-3226">Conduire permis de</span><span class="sxs-lookup"><span data-stu-id="abe74-3226">Driver's License</span></span> 
- <span data-ttu-id="abe74-3227">Conduire permis de</span><span class="sxs-lookup"><span data-stu-id="abe74-3227">Driver's Licenses</span></span> 
- <span data-ttu-id="abe74-3228">numéro d’identification
</span><span class="sxs-lookup"><span data-stu-id="abe74-3228">identification number</span></span> 
- <span data-ttu-id="abe74-3229">numéros d’identification
</span><span class="sxs-lookup"><span data-stu-id="abe74-3229">identification numbers</span></span> 
- <span data-ttu-id="abe74-3230"># identification
</span><span class="sxs-lookup"><span data-stu-id="abe74-3230">identification #</span></span> 
- <span data-ttu-id="abe74-3231">carte d’identité</span><span class="sxs-lookup"><span data-stu-id="abe74-3231">id card</span></span> 
- <span data-ttu-id="abe74-3232">ID de cartes de visite</span><span class="sxs-lookup"><span data-stu-id="abe74-3232">id cards</span></span> 
- <span data-ttu-id="abe74-3233">carte d’identification</span><span class="sxs-lookup"><span data-stu-id="abe74-3233">identification card</span></span> 
- <span data-ttu-id="abe74-3234">cartes d’identification</span><span class="sxs-lookup"><span data-stu-id="abe74-3234">identification cards</span></span> 
- <span data-ttu-id="abe74-3235">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="abe74-3235">DriverLic#</span></span> 
- <span data-ttu-id="abe74-3236">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="abe74-3236">DriverLics#</span></span> 
- <span data-ttu-id="abe74-3237">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="abe74-3237">DriverLicense#</span></span> 
- <span data-ttu-id="abe74-3238">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="abe74-3238">DriverLicenses#</span></span> 
- <span data-ttu-id="abe74-3239">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="abe74-3239">Driver Lic#</span></span> 
- <span data-ttu-id="abe74-3240">
#Permis conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-3240">Driver Lics#</span></span> 
- <span data-ttu-id="abe74-3241">Pilote licence #</span><span class="sxs-lookup"><span data-stu-id="abe74-3241">Driver License#</span></span> 
- <span data-ttu-id="abe74-3242">Licences de pilote #</span><span class="sxs-lookup"><span data-stu-id="abe74-3242">Driver Licenses#</span></span> 
- <span data-ttu-id="abe74-3243">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="abe74-3243">DriversLic#</span></span> 
- <span data-ttu-id="abe74-3244">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="abe74-3244">DriversLics#</span></span> 
- <span data-ttu-id="abe74-3245">Conduire #</span><span class="sxs-lookup"><span data-stu-id="abe74-3245">DriversLicense#</span></span> 
- <span data-ttu-id="abe74-3246">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="abe74-3246">DriversLicenses#</span></span> 
- <span data-ttu-id="abe74-3247">Pilotes Lic #</span><span class="sxs-lookup"><span data-stu-id="abe74-3247">Drivers Lic#</span></span> 
- <span data-ttu-id="abe74-3248">Pilotes Lics #</span><span class="sxs-lookup"><span data-stu-id="abe74-3248">Drivers Lics#</span></span> 
- <span data-ttu-id="abe74-3249">Licence pilotes #</span><span class="sxs-lookup"><span data-stu-id="abe74-3249">Drivers License#</span></span> 
- <span data-ttu-id="abe74-3250">Licences pilotes #</span><span class="sxs-lookup"><span data-stu-id="abe74-3250">Drivers Licenses#</span></span> 
- <span data-ttu-id="abe74-3251">#Permisconduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-3251">Driver'Lic#</span></span> 
- <span data-ttu-id="abe74-3252">#Permisconduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-3252">Driver'Lics#</span></span> 
- <span data-ttu-id="abe74-3253">#Permisdeconduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-3253">Driver'License#</span></span> 
- <span data-ttu-id="abe74-3254">#Permisdeconduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-3254">Driver'Licenses#</span></span> 
- <span data-ttu-id="abe74-3255">#Permis conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-3255">Driver' Lic#</span></span> 
- <span data-ttu-id="abe74-3256">#Permis conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-3256">Driver' Lics#</span></span> 
- <span data-ttu-id="abe74-3257">#Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-3257">Driver' License#</span></span> 
- <span data-ttu-id="abe74-3258">#Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-3258">Driver' Licenses#</span></span> 
- <span data-ttu-id="abe74-3259">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="abe74-3259">Driver'sLic#</span></span> 
- <span data-ttu-id="abe74-3260">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="abe74-3260">Driver'sLics#</span></span> 
- <span data-ttu-id="abe74-3261">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="abe74-3261">Driver'sLicense#</span></span> 
- <span data-ttu-id="abe74-3262">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="abe74-3262">Driver'sLicenses#</span></span> 
- <span data-ttu-id="abe74-3263">#Permisconduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-3263">Driver's Lic#</span></span> 
- <span data-ttu-id="abe74-3264">#Permisconduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-3264">Driver's Lics#</span></span> 
- <span data-ttu-id="abe74-3265">#Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-3265">Driver's License#</span></span> 
- <span data-ttu-id="abe74-3266">#Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="abe74-3266">Driver's Licenses#</span></span> 
- <span data-ttu-id="abe74-3267">carte d’identité #</span><span class="sxs-lookup"><span data-stu-id="abe74-3267">id card#</span></span> 
- <span data-ttu-id="abe74-3268"># cartes d’identité
</span><span class="sxs-lookup"><span data-stu-id="abe74-3268">id cards#</span></span> 
- <span data-ttu-id="abe74-3269">#carte d’identification
</span><span class="sxs-lookup"><span data-stu-id="abe74-3269">identification card#</span></span> 
- <span data-ttu-id="abe74-3270">#cartes d’identification
</span><span class="sxs-lookup"><span data-stu-id="abe74-3270">identification cards#</span></span> 


#### <a name="keywordstatenamedriverslicensename"></a><span data-ttu-id="abe74-3271">Keyword_[state_name]_drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="abe74-3271">Keyword_[state_name]_drivers_license_name</span></span>

- <span data-ttu-id="abe74-3272">Abréviation de l’État (par exemple, « NY »)
</span><span class="sxs-lookup"><span data-stu-id="abe74-3272">State abbreviation (for example, "NY")</span></span> 
- <span data-ttu-id="abe74-3273">Nom de l’État (par exemple, « New York »)
</span><span class="sxs-lookup"><span data-stu-id="abe74-3273">State name (for example, "New York")</span></span>    
   
## <a name="us-individual-taxpayer-identification-number-itin"></a><span data-ttu-id="abe74-3274">Numéro d'identification fiscale individuel (ITIN) États-Unis</span><span class="sxs-lookup"><span data-stu-id="abe74-3274">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>

### <a name="format"></a><span data-ttu-id="abe74-3275">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-3275">Format</span></span>

<span data-ttu-id="abe74-3276">Neuf chiffres, le premier étant le « 9 », le quatrième le « 7 » ou le « 8 », éventuellement mis en forme avec des espaces ou des tirets</span><span class="sxs-lookup"><span data-stu-id="abe74-3276">Nine digits that start with a "9" and contain a "7" or "8" as the fourth digit, optionally formatted with spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-3277">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-3277">Pattern</span></span>

<span data-ttu-id="abe74-3278">Mis en forme :</span><span class="sxs-lookup"><span data-stu-id="abe74-3278">Formatted:</span></span>
- <span data-ttu-id="abe74-3279">Le chiffre « 9 »</span><span class="sxs-lookup"><span data-stu-id="abe74-3279">The digit "9"</span></span> 
- <span data-ttu-id="abe74-3280">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-3280">Two digits</span></span> 
- <span data-ttu-id="abe74-3281">Un espace ou un tiret</span><span class="sxs-lookup"><span data-stu-id="abe74-3281">A space or dash</span></span> 
- <span data-ttu-id="abe74-3282">Un « 7 » ou un « 8 »</span><span class="sxs-lookup"><span data-stu-id="abe74-3282">A "7" or "8"</span></span> 
- <span data-ttu-id="abe74-3283">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="abe74-3283">A digit</span></span> 
- <span data-ttu-id="abe74-3284">Un espace ou tiret</span><span class="sxs-lookup"><span data-stu-id="abe74-3284">A space, or dash</span></span> 
- <span data-ttu-id="abe74-3285">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-3285">Four digits</span></span>

<span data-ttu-id="abe74-3286">Non mis en forme :</span><span class="sxs-lookup"><span data-stu-id="abe74-3286">Unformatted:</span></span>
- <span data-ttu-id="abe74-3287">Le chiffre « 9 »</span><span class="sxs-lookup"><span data-stu-id="abe74-3287">The digit "9"</span></span> 
- <span data-ttu-id="abe74-3288">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-3288">Two digits</span></span> 
- <span data-ttu-id="abe74-3289">Un « 7 » ou un « 8 »</span><span class="sxs-lookup"><span data-stu-id="abe74-3289">A "7" or "8"</span></span> 
- <span data-ttu-id="abe74-3290">Cinq chiffres</span><span class="sxs-lookup"><span data-stu-id="abe74-3290">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-3291">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-3291">Checksum</span></span>

<span data-ttu-id="abe74-3292">Non</span><span class="sxs-lookup"><span data-stu-id="abe74-3292">No</span></span>

### <a name="definition"></a><span data-ttu-id="abe74-3293">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-3293">Definition</span></span>

<span data-ttu-id="abe74-3294">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-3294">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-3295">La fonction Func_formatted_itin trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-3295">The function Func_formatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-3296">Au moins une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="abe74-3296">At least one of the following is true:</span></span>
    - <span data-ttu-id="abe74-3297">Un mot clé figurant dans la liste Keyword_itin est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-3297">A keyword from Keyword_itin is found.</span></span>
    - <span data-ttu-id="abe74-3298">La fonction Func_us_address trouve une adresse au format correct.</span><span class="sxs-lookup"><span data-stu-id="abe74-3298">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="abe74-3299">La fonction Func_us_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="abe74-3299">The function Func_us_date finds a date in the right date format.</span></span>
    - <span data-ttu-id="abe74-3300">Un mot clé figurant dans la liste Keyword_itin_collaborative est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-3300">A keyword from Keyword_itin_collaborative is found.</span></span>

<span data-ttu-id="abe74-3301">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-3301">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-3302">La fonction Func_unformatted_itin trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-3302">The function Func_unformatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-3303">Au moins une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="abe74-3303">At least one of the following is true:</span></span>
    - <span data-ttu-id="abe74-3304">Un mot clé figurant dans la liste Keyword_itin_collaborative est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-3304">A keyword from Keyword_itin_collaborative is found.</span></span>
    - <span data-ttu-id="abe74-3305">La fonction Func_us_address trouve une adresse au format correct.</span><span class="sxs-lookup"><span data-stu-id="abe74-3305">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="abe74-3306">La fonction Func_us_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="abe74-3306">The function Func_us_date finds a date in the right date format.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-3307">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-3307">Keywords</span></span>

#### <a name="keyworditin"></a><span data-ttu-id="abe74-3308">Keyword_itin</span><span class="sxs-lookup"><span data-stu-id="abe74-3308">Keyword_itin</span></span>

- <span data-ttu-id="abe74-3309">contribuable
</span><span class="sxs-lookup"><span data-stu-id="abe74-3309">taxpayer</span></span> 
- <span data-ttu-id="abe74-3310">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="abe74-3310">tax id</span></span> 
- <span data-ttu-id="abe74-3311">identification fiscale
</span><span class="sxs-lookup"><span data-stu-id="abe74-3311">tax identification</span></span> 
- <span data-ttu-id="abe74-3312">itin
</span><span class="sxs-lookup"><span data-stu-id="abe74-3312">itin</span></span> 
- <span data-ttu-id="abe74-3313">ssn</span><span class="sxs-lookup"><span data-stu-id="abe74-3313">ssn</span></span> 
- <span data-ttu-id="abe74-3314">tin
</span><span class="sxs-lookup"><span data-stu-id="abe74-3314">tin</span></span> 
- <span data-ttu-id="abe74-3315">sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="abe74-3315">social security</span></span> 
- <span data-ttu-id="abe74-3316">contribuable
</span><span class="sxs-lookup"><span data-stu-id="abe74-3316">tax payer</span></span> 
- <span data-ttu-id="abe74-3317">itins
</span><span class="sxs-lookup"><span data-stu-id="abe74-3317">itins</span></span> 
- <span data-ttu-id="abe74-3318">id fiscal

</span><span class="sxs-lookup"><span data-stu-id="abe74-3318">taxid</span></span> 
- <span data-ttu-id="abe74-3319">contribuable individuel
</span><span class="sxs-lookup"><span data-stu-id="abe74-3319">individual taxpayer</span></span> 

#### <a name="keyworditincollaborative"></a><span data-ttu-id="abe74-3320">Keyword_itin_collaborative</span><span class="sxs-lookup"><span data-stu-id="abe74-3320">Keyword_itin_collaborative</span></span>

- <span data-ttu-id="abe74-3321">License</span><span class="sxs-lookup"><span data-stu-id="abe74-3321">License</span></span> 
- <span data-ttu-id="abe74-3322">PC</span><span class="sxs-lookup"><span data-stu-id="abe74-3322">DL</span></span> 
- <span data-ttu-id="abe74-3323">DDN
</span><span class="sxs-lookup"><span data-stu-id="abe74-3323">DOB</span></span> 
- <span data-ttu-id="abe74-3324">Birthdate</span><span class="sxs-lookup"><span data-stu-id="abe74-3324">Birthdate</span></span> 
- <span data-ttu-id="abe74-3325">Anniversaire </span><span class="sxs-lookup"><span data-stu-id="abe74-3325">Birthday</span></span> 
- <span data-ttu-id="abe74-3326">Date of Birth
</span><span class="sxs-lookup"><span data-stu-id="abe74-3326">Date of Birth</span></span> 
   
## <a name="us-social-security-number-ssn"></a><span data-ttu-id="abe74-3327">Numéro de sécurité sociale (SSN) États-Unis</span><span class="sxs-lookup"><span data-stu-id="abe74-3327">U.S. Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="abe74-3328">Format</span><span class="sxs-lookup"><span data-stu-id="abe74-3328">Format</span></span>

<span data-ttu-id="abe74-3329">9 chiffres, qui peuvent être mis en forme ou non mis en forme</span><span class="sxs-lookup"><span data-stu-id="abe74-3329">9 digits, which may be in a formatted or unformatted pattern</span></span>

> [!NOTE]
> <span data-ttu-id="abe74-3330">La mise en forme d’un numéro de sécurité sociale émis avant le milieu de l’année 2011 est fixe et certaines parties du numéro doivent se situer dans certaines plages pour qu’il soit valide (mais il n’y a pas de somme de contrôle).</span><span class="sxs-lookup"><span data-stu-id="abe74-3330">If issued before mid-2011, an SSN has strong formatting where certain parts of the number must fall within certain ranges to be valid (but there's no checksum).</span></span>

### <a name="pattern"></a><span data-ttu-id="abe74-3331">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe74-3331">Pattern</span></span>

<span data-ttu-id="abe74-3332">Quatre fonctions permettent de rechercher des numéros de sécurité sociale avec quatre différents modèles :</span><span class="sxs-lookup"><span data-stu-id="abe74-3332">Four functions look for SSNs in four different patterns:</span></span>
- <span data-ttu-id="abe74-3333">Func_ssn recherche des numéros de sécurité sociale avec une mise en forme fixe d’avant l’année 2011, mis en forme avec des tirets ou des espaces (ddd-dd-dddd OU ddd dd dddd)</span><span class="sxs-lookup"><span data-stu-id="abe74-3333">Func_ssn finds SSNs with pre-2011 strong formatting that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="abe74-3334">Func_unformatted_ssn recherche des numéros de sécurité sociale avec une mise en forme fixe d’avant l’année 2011, avec neuf chiffres consécutifs non mis en forme (ddddddddd)</span><span class="sxs-lookup"><span data-stu-id="abe74-3334">Func_unformatted_ssn finds SSNs with pre-2011 strong formatting that are unformatted as nine consecutive digits (ddddddddd)</span></span>
- <span data-ttu-id="abe74-3335">Func_randomized_formatted_ssn recherche des numéros de sécurité sociale d’après l’année 2011, mis en forme avec des tirets ou des espaces  (ddd-dd-dddd OU ddd dd dddd)</span><span class="sxs-lookup"><span data-stu-id="abe74-3335">Func_randomized_formatted_ssn finds post-2011 SSNs that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="abe74-3336">Func_randomized_unformatted_ssn recherche des numéros de sécurité sociale d’après l’année 2011, avec neuf chiffres consécutifs non mis en forme (ddddddddd)</span><span class="sxs-lookup"><span data-stu-id="abe74-3336">Func_randomized_unformatted_ssn finds post-2011 SSNs that are unformatted as nine consecutive digits (ddddddddd)</span></span>

### <a name="checksum"></a><span data-ttu-id="abe74-3337">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe74-3337">Checksum</span></span>

<span data-ttu-id="abe74-3338">Non</span><span class="sxs-lookup"><span data-stu-id="abe74-3338">No</span></span>


### <a name="definition"></a><span data-ttu-id="abe74-3339">Définition</span><span class="sxs-lookup"><span data-stu-id="abe74-3339">Definition</span></span>

<span data-ttu-id="abe74-3340">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-3340">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-3341">La fonction Func_ssn trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-3341">The function Func_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-3342">Un mot clé figurant dans la liste Keyword_ssn est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-3342">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="abe74-3343">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-3343">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-3344">La fonction Func_unformatted_ssn trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-3344">The function Func_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-3345">Un mot clé figurant dans la liste Keyword_ssn est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-3345">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="abe74-3346">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-3346">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-3347">La fonction Func_randomized_formatted_ssn trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-3347">The function Func_randomized_formatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-3348">Un mot clé figurant dans la liste Keyword_ssn est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-3348">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="abe74-3349">La fonction Func_ssn ne trouve pas de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-3349">The function Func_ssn does not find content that matches the pattern.</span></span>

<span data-ttu-id="abe74-3350">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 55 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe74-3350">A DLP policy is 55% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="abe74-3351">La fonction Func_randomized_unformatted_ssn trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-3351">The function Func_randomized_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="abe74-3352">Un mot clé figurant dans la liste Keyword_ssn est trouvé.</span><span class="sxs-lookup"><span data-stu-id="abe74-3352">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="abe74-3353">La fonction Func_unformatted_ssn ne trouve pas de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe74-3353">The function Func_unformatted_ssn does not find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="abe74-3354">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abe74-3354">Keywords</span></span>

#### <a name="keywordssn"></a><span data-ttu-id="abe74-3355">Keyword_ssn</span><span class="sxs-lookup"><span data-stu-id="abe74-3355">Keyword_ssn</span></span>

- <span data-ttu-id="abe74-3356">Sécurité sociale
</span><span class="sxs-lookup"><span data-stu-id="abe74-3356">Social Security</span></span> 
- <span data-ttu-id="abe74-3357"># sécurité sociale
</span><span class="sxs-lookup"><span data-stu-id="abe74-3357">Social Security#</span></span> 
- <span data-ttu-id="abe74-3358">Sécu sociale
</span><span class="sxs-lookup"><span data-stu-id="abe74-3358">Soc Sec</span></span> 
- <span data-ttu-id="abe74-3359">SSN</span><span class="sxs-lookup"><span data-stu-id="abe74-3359">SSN</span></span> 
- <span data-ttu-id="abe74-3360">NSS
</span><span class="sxs-lookup"><span data-stu-id="abe74-3360">SSNS</span></span> 
- <span data-ttu-id="abe74-3361">#NSS
</span><span class="sxs-lookup"><span data-stu-id="abe74-3361">SSN#</span></span> 
- <span data-ttu-id="abe74-3362"># SS
</span><span class="sxs-lookup"><span data-stu-id="abe74-3362">SS#</span></span> 
- <span data-ttu-id="abe74-3363">IDSS
</span><span class="sxs-lookup"><span data-stu-id="abe74-3363">SSID</span></span> 
   

