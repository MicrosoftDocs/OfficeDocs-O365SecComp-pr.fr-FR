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
ms.openlocfilehash: 4b083f80e02c80053b63ee897b2515a4505c16d9
ms.sourcegitcommit: 8c5a88433cff23c59b436260808cf3d91b06fdef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/07/2018
ms.locfileid: "27194735"
---
# <a name="what-the-sensitive-information-types-look-for"></a><span data-ttu-id="d8d84-104">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="d8d84-104">What the sensitive information types look for</span></span>

<span data-ttu-id="d8d84-p102">Prévention des pertes de données (DLP) de sécurité Office 365 &amp; centre de conformité inclut de nombreux types d’informations sensibles qui sont prêts à utiliser dans vos stratégies DLP. Cette rubrique répertorie tous ces types d’informations sensibles et illustre une stratégie DLP lorsqu’il détecte chaque type. Un type d’informations sensibles est défini par un modèle qui peut être identifié par une expression régulière ou une fonction. En outre, la preuve corroborante tels que des mots clés et les totaux de contrôle peut servir à identifier un type d’informations sensibles. Proximité et niveau de confiance sont également utilisés dans le processus d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="d8d84-p102">Data loss prevention (DLP) in the Office 365 Security &amp; Compliance Center includes many sensitive information types that are ready for you to use in your DLP policies. This topic lists all of these sensitive information types and shows what a DLP policy looks for when it detects each type. A sensitive information type is defined by a pattern that can be identified by a regular expression or a function. In addition, corroborative evidence such as keywords and checksums can be used to identify a sensitive information type. Confidence level and proximity are also used in the evaluation process.</span></span>
  
## <a name="aba-routing-number"></a><span data-ttu-id="d8d84-110">Numéro de routage ABA</span><span class="sxs-lookup"><span data-stu-id="d8d84-110">ABA Routing Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-111">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-111">Format</span></span>

<span data-ttu-id="d8d84-112">9 chiffres mis en forme ou non mis en forme</span><span class="sxs-lookup"><span data-stu-id="d8d84-112">9 digits which may be in a formatted or unformatted pattern</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-113">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-113">Pattern</span></span>

<span data-ttu-id="d8d84-114">Mis en forme :</span><span class="sxs-lookup"><span data-stu-id="d8d84-114">Formatted:</span></span>
- <span data-ttu-id="d8d84-115">Quatre chiffres commençant par 0, 1, 2, 3, 6, 7 ou 8</span><span class="sxs-lookup"><span data-stu-id="d8d84-115">Four digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span>
- <span data-ttu-id="d8d84-116">Un trait d’union</span><span class="sxs-lookup"><span data-stu-id="d8d84-116">A hyphen</span></span>
- <span data-ttu-id="d8d84-117">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-117">Four digits</span></span>
- <span data-ttu-id="d8d84-118">Un trait d’union</span><span class="sxs-lookup"><span data-stu-id="d8d84-118">A hyphen</span></span>
- <span data-ttu-id="d8d84-119">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="d8d84-119">A digit</span></span>

<span data-ttu-id="d8d84-120">Non formatée : 9 chiffres consécutifs commencent par 0, 1, 2, 3, 6, 7 ou 8</span><span class="sxs-lookup"><span data-stu-id="d8d84-120">Unformatted: 9 consecutive digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span> 

### <a name="checksum"></a><span data-ttu-id="d8d84-121">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-121">Checksum</span></span>

<span data-ttu-id="d8d84-122">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-122">No</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-123">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-123">Definition</span></span>

<span data-ttu-id="d8d84-124">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-124">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-125">La fonction Func_aba_routing trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-125">The function Func_aba_routing finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-126">Un mot clé figurant dans la liste Keyword_ABA_Routing est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-126">A keyword from Keyword_ABA_Routing is found.</span></span>

```
<!-- ABA Routing Number -->
<Entity id="cb353f78-2b72-4c3c-8827-92ebe4f69fdf" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_aba_routing" />
        <Match idRef="Keyword_ABA_Routing" />
      </Pattern>
 </Entity>
```


### <a name="keywords"></a><span data-ttu-id="d8d84-127">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-127">Keywords</span></span>

#### <a name="keywordabarouting"></a><span data-ttu-id="d8d84-128">Keyword_ABA_Routing</span><span class="sxs-lookup"><span data-stu-id="d8d84-128">Keyword_ABA_Routing</span></span>

- <span data-ttu-id="d8d84-129">aba</span><span class="sxs-lookup"><span data-stu-id="d8d84-129">aba</span></span>
- <span data-ttu-id="d8d84-130">
# aba</span><span class="sxs-lookup"><span data-stu-id="d8d84-130">aba #</span></span>
- <span data-ttu-id="d8d84-131">
# routage aba</span><span class="sxs-lookup"><span data-stu-id="d8d84-131">aba routing #</span></span>
- <span data-ttu-id="d8d84-132">numéro de routage ABA</span><span class="sxs-lookup"><span data-stu-id="d8d84-132">aba routing number</span></span>
- <span data-ttu-id="d8d84-133">
#aba</span><span class="sxs-lookup"><span data-stu-id="d8d84-133">aba#</span></span>
- <span data-ttu-id="d8d84-134">
#routageaba</span><span class="sxs-lookup"><span data-stu-id="d8d84-134">abarouting#</span></span>
- <span data-ttu-id="d8d84-135">
numéro aba</span><span class="sxs-lookup"><span data-stu-id="d8d84-135">aba number</span></span>
- <span data-ttu-id="d8d84-136">
numéroroutageaba</span><span class="sxs-lookup"><span data-stu-id="d8d84-136">abaroutingnumber</span></span>
- <span data-ttu-id="d8d84-137">
# routage american bank association</span><span class="sxs-lookup"><span data-stu-id="d8d84-137">american bank association routing #</span></span>
- <span data-ttu-id="d8d84-138">
numéro de routage american bank association</span><span class="sxs-lookup"><span data-stu-id="d8d84-138">american bank association routing number</span></span>
- <span data-ttu-id="d8d84-139">
#routageamericanbankassociation</span><span class="sxs-lookup"><span data-stu-id="d8d84-139">americanbankassociationrouting#</span></span>
- <span data-ttu-id="d8d84-140">
numéroderoutageamericanbankassociation</span><span class="sxs-lookup"><span data-stu-id="d8d84-140">americanbankassociationroutingnumber</span></span>
- <span data-ttu-id="d8d84-141">
numéro de routage bancaire</span><span class="sxs-lookup"><span data-stu-id="d8d84-141">bank routing number</span></span>
- <span data-ttu-id="d8d84-142">
#routagebancaire</span><span class="sxs-lookup"><span data-stu-id="d8d84-142">bankrouting#</span></span>
- <span data-ttu-id="d8d84-143">
numéroderoutagebancaire</span><span class="sxs-lookup"><span data-stu-id="d8d84-143">bankroutingnumber</span></span>
- <span data-ttu-id="d8d84-144">
numéro de routage</span><span class="sxs-lookup"><span data-stu-id="d8d84-144">routing transit number</span></span>
- <span data-ttu-id="d8d84-145">
RTN
</span><span class="sxs-lookup"><span data-stu-id="d8d84-145">RTN</span></span> 
   
## <a name="argentina-national-identity-dni-number"></a><span data-ttu-id="d8d84-146">Numéro d’identité nationale (DNI) pour l’Argentine</span><span class="sxs-lookup"><span data-stu-id="d8d84-146">Argentina National Identity (DNI) Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-147">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-147">Format</span></span>

<span data-ttu-id="d8d84-148">Huit chiffres séparés par des points</span><span class="sxs-lookup"><span data-stu-id="d8d84-148">Eight digits separated by periods</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-149">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-149">Pattern</span></span>

<span data-ttu-id="d8d84-150">Huit chiffres :</span><span class="sxs-lookup"><span data-stu-id="d8d84-150">Eight digits:</span></span>
- <span data-ttu-id="d8d84-151">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-151">Two digits</span></span>
- <span data-ttu-id="d8d84-152">Un point </span><span class="sxs-lookup"><span data-stu-id="d8d84-152">A period</span></span>
- <span data-ttu-id="d8d84-153">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-153">Three digits</span></span>
- <span data-ttu-id="d8d84-154">Un point </span><span class="sxs-lookup"><span data-stu-id="d8d84-154">A period</span></span>
- <span data-ttu-id="d8d84-155">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-155">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-156">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-156">Checksum</span></span>

<span data-ttu-id="d8d84-157">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-157">No</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-158">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-158">Definition</span></span>

<span data-ttu-id="d8d84-159">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-159">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-160">L’expression régulière Regex_argentina_national_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-160">The regular expression Regex_argentina_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-161">Un mot clé figurant dans la liste Keyword_argentina_national_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-161">A keyword from Keyword_argentina_national_id is found.</span></span>

```
<!-- Argentina National Identity (DNI) Number -->
<Entity id="eefbb00e-8282-433c-8620-8f1da3bffdb2" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_argentina_national_id"/>
      <Match idRef="Keyword_argentina_national_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8d84-162">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-162">Keywords</span></span>

#### <a name="keywordargentinanationalid"></a><span data-ttu-id="d8d84-163">Keyword_argentina_national_id</span><span class="sxs-lookup"><span data-stu-id="d8d84-163">Keyword_argentina_national_id</span></span>

- <span data-ttu-id="d8d84-164">Argentina National Identity number
</span><span class="sxs-lookup"><span data-stu-id="d8d84-164">Argentina National Identity number</span></span> 
- <span data-ttu-id="d8d84-165">Identité</span><span class="sxs-lookup"><span data-stu-id="d8d84-165">Identity</span></span> 
- <span data-ttu-id="d8d84-166">Carte nationale d’identification</span><span class="sxs-lookup"><span data-stu-id="d8d84-166">Identification National Identity Card</span></span> 
- <span data-ttu-id="d8d84-167">DNI
</span><span class="sxs-lookup"><span data-stu-id="d8d84-167">DNI</span></span> 
- <span data-ttu-id="d8d84-168">Carte réseau Registre National de personnes</span><span class="sxs-lookup"><span data-stu-id="d8d84-168">NIC National Registry of Persons</span></span> 
- <span data-ttu-id="d8d84-169">Documento Nacional de Identidad
</span><span class="sxs-lookup"><span data-stu-id="d8d84-169">Documento Nacional de Identidad</span></span> 
- <span data-ttu-id="d8d84-170">Registro Nacional de las Personas
</span><span class="sxs-lookup"><span data-stu-id="d8d84-170">Registro Nacional de las Personas</span></span> 
- <span data-ttu-id="d8d84-171">Identidad
</span><span class="sxs-lookup"><span data-stu-id="d8d84-171">Identidad</span></span> 
- <span data-ttu-id="d8d84-172">Identificación
</span><span class="sxs-lookup"><span data-stu-id="d8d84-172">Identificación</span></span> 
   
## <a name="australia-bank-account-number"></a><span data-ttu-id="d8d84-173">Numéro de compte bancaire Australie</span><span class="sxs-lookup"><span data-stu-id="d8d84-173">Australia Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-174">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-174">Format</span></span>

<span data-ttu-id="d8d84-175">6 à 10 chiffres avec ou sans le numéro d’agence bancaire de l’État</span><span class="sxs-lookup"><span data-stu-id="d8d84-175">6-10 digits with or without a bank state branch number</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-176">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-176">Pattern</span></span>

<span data-ttu-id="d8d84-p103">Numéro de compte est de 6 à 10 chiffres. Numéro de succursale bancaire Australie état :</span><span class="sxs-lookup"><span data-stu-id="d8d84-p103">Account number is 6-10 digits. Australia bank state branch number:</span></span>
- <span data-ttu-id="d8d84-179">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-179">Three digits</span></span> 
- <span data-ttu-id="d8d84-180">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="d8d84-180">A hyphen</span></span> 
- <span data-ttu-id="d8d84-181">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-181">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-182">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-182">Checksum</span></span>

<span data-ttu-id="d8d84-183">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-183">No</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-184">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-184">Definition</span></span>

<span data-ttu-id="d8d84-185">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-185">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-186">L’expression régulière Regex_australia_bank_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-186">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="d8d84-187">Un mot clé figurant dans la liste Keyword_australia_bank_account_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-187">A keyword from Keyword_australia_bank_account_number is found.</span></span>
- <span data-ttu-id="d8d84-188">L’expression régulière Regex_australia_bank_account_number_bsb trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-188">The regular expression Regex_australia_bank_account_number_bsb finds content that matches the pattern.</span></span>

<span data-ttu-id="d8d84-189">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-189">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-190">L’expression régulière Regex_australia_bank_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-190">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="d8d84-191">Un mot clé figurant dans la liste Keyword_australia_bank_account_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-191">A keyword from Keyword_australia_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-192">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-192">Keywords</span></span>

#### <a name="keywordaustraliabankaccountnumber"></a><span data-ttu-id="d8d84-193">Keyword_australia_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="d8d84-193">Keyword_australia_bank_account_number</span></span>

- <span data-ttu-id="d8d84-194">code swift banque</span><span class="sxs-lookup"><span data-stu-id="d8d84-194">swift bank code</span></span>
- <span data-ttu-id="d8d84-195">
banque correspondante</span><span class="sxs-lookup"><span data-stu-id="d8d84-195">correspondent bank</span></span>
- <span data-ttu-id="d8d84-196">
devise de base</span><span class="sxs-lookup"><span data-stu-id="d8d84-196">base currency</span></span>
- <span data-ttu-id="d8d84-197">
compte aux États-Unis</span><span class="sxs-lookup"><span data-stu-id="d8d84-197">usa account</span></span>
- <span data-ttu-id="d8d84-198">
adresse du titulaire</span><span class="sxs-lookup"><span data-stu-id="d8d84-198">holder address</span></span>
- <span data-ttu-id="d8d84-199">
adresse de la banque</span><span class="sxs-lookup"><span data-stu-id="d8d84-199">bank address</span></span>
- <span data-ttu-id="d8d84-200">
informations du compte</span><span class="sxs-lookup"><span data-stu-id="d8d84-200">information account</span></span>
- <span data-ttu-id="d8d84-201">
transferts de fonds</span><span class="sxs-lookup"><span data-stu-id="d8d84-201">fund transfers</span></span>
- <span data-ttu-id="d8d84-202">
frais bancaires</span><span class="sxs-lookup"><span data-stu-id="d8d84-202">bank charges</span></span>
- <span data-ttu-id="d8d84-203">
informations sur la banque</span><span class="sxs-lookup"><span data-stu-id="d8d84-203">bank details</span></span>
- <span data-ttu-id="d8d84-204">
informations bancaires</span><span class="sxs-lookup"><span data-stu-id="d8d84-204">banking information</span></span>
- <span data-ttu-id="d8d84-205">
noms complets</span><span class="sxs-lookup"><span data-stu-id="d8d84-205">full names</span></span>
- <span data-ttu-id="d8d84-206">

iaea</span><span class="sxs-lookup"><span data-stu-id="d8d84-206">iaea</span></span>

   
## <a name="australia-drivers-license-number"></a><span data-ttu-id="d8d84-207">Numéro de permis de conduire Australie</span><span class="sxs-lookup"><span data-stu-id="d8d84-207">Australia Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-208">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-208">Format</span></span>

<span data-ttu-id="d8d84-209">Neuf lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-209">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-210">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-210">Pattern</span></span>

<span data-ttu-id="d8d84-211">Neuf lettres et chiffres :</span><span class="sxs-lookup"><span data-stu-id="d8d84-211">Nine letters and digits:</span></span> 

- <span data-ttu-id="d8d84-212">Deux chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="d8d84-212">Two digits or letters (not case sensitive)</span></span> 
- <span data-ttu-id="d8d84-213">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-213">Two digits</span></span> 
- <span data-ttu-id="d8d84-214">Cinq chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="d8d84-214">Five digits or letters (not case sensitive)</span></span>

<span data-ttu-id="d8d84-215">OU</span><span class="sxs-lookup"><span data-stu-id="d8d84-215">OR</span></span>

- <span data-ttu-id="d8d84-216">1 ou 2 lettres facultatives (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="d8d84-216">1-2 optional letters (not case sensitive)</span></span> 
- <span data-ttu-id="d8d84-217">4 à 9 chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-217">4-9 digits</span></span>

<span data-ttu-id="d8d84-218">OU</span><span class="sxs-lookup"><span data-stu-id="d8d84-218">OR</span></span>

- <span data-ttu-id="d8d84-219">Neuf chiffres ou lettres (ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="d8d84-219">Nine digits or letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-220">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-220">Checksum</span></span>

<span data-ttu-id="d8d84-221">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-221">No</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-222">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-222">Definition</span></span>

<span data-ttu-id="d8d84-223">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-223">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-224">L’expression régulière Regex_australia_drivers_license_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-224">The regular expression Regex_australia_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-225">Un mot clé figurant dans la liste Keyword_australia_drivers_license_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-225">A keyword from Keyword_australia_drivers_license_number is found.</span></span>
- <span data-ttu-id="d8d84-226">Aucun mot clé figurant dans la liste Keyword_australia_drivers_license_number_exclusions n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-226">No keyword from Keyword_australia_drivers_license_number_exclusions is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-227">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-227">Keywords</span></span>

#### <a name="keywordaustraliadriverslicensenumber"></a><span data-ttu-id="d8d84-228">Keyword_australia_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="d8d84-228">Keyword_australia_drivers_license_number</span></span>

- <span data-ttu-id="d8d84-229">permis de conduite internationaux</span><span class="sxs-lookup"><span data-stu-id="d8d84-229">international driving permits</span></span>
- <span data-ttu-id="d8d84-230">
australian automobile association</span><span class="sxs-lookup"><span data-stu-id="d8d84-230">australian automobile association</span></span>
- <span data-ttu-id="d8d84-231">
permis de conduite international</span><span class="sxs-lookup"><span data-stu-id="d8d84-231">international driving permit</span></span>
- <span data-ttu-id="d8d84-232">DriverLicence</span><span class="sxs-lookup"><span data-stu-id="d8d84-232">DriverLicence</span></span>
- <span data-ttu-id="d8d84-233">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="d8d84-233">DriverLicences</span></span>
- <span data-ttu-id="d8d84-234">Lic pilote</span><span class="sxs-lookup"><span data-stu-id="d8d84-234">Driver Lic</span></span>
- <span data-ttu-id="d8d84-235">Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-235">Driver Licence</span></span>
- <span data-ttu-id="d8d84-236">Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-236">Driver Licences</span></span>
- <span data-ttu-id="d8d84-237">DriversLic</span><span class="sxs-lookup"><span data-stu-id="d8d84-237">DriversLic</span></span>
- <span data-ttu-id="d8d84-238">DriversLicence</span><span class="sxs-lookup"><span data-stu-id="d8d84-238">DriversLicence</span></span>
- <span data-ttu-id="d8d84-239">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="d8d84-239">DriversLicences</span></span>
- <span data-ttu-id="d8d84-240">Lic pilotes</span><span class="sxs-lookup"><span data-stu-id="d8d84-240">Drivers Lic</span></span>
- <span data-ttu-id="d8d84-241">Lics pilotes</span><span class="sxs-lookup"><span data-stu-id="d8d84-241">Drivers Lics</span></span>
- <span data-ttu-id="d8d84-242">Certificat de pilotes</span><span class="sxs-lookup"><span data-stu-id="d8d84-242">Drivers Licence</span></span>
- <span data-ttu-id="d8d84-243">Certificats de pilotes</span><span class="sxs-lookup"><span data-stu-id="d8d84-243">Drivers Licences</span></span>
- <span data-ttu-id="d8d84-244">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="d8d84-244">Driver'Lic</span></span>
- <span data-ttu-id="d8d84-245">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="d8d84-245">Driver'Lics</span></span>
- <span data-ttu-id="d8d84-246">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="d8d84-246">Driver'Licence</span></span>
- <span data-ttu-id="d8d84-247">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="d8d84-247">Driver'Licences</span></span>
- <span data-ttu-id="d8d84-248">Pilote ' Lic</span><span class="sxs-lookup"><span data-stu-id="d8d84-248">Driver' Lic</span></span>
- <span data-ttu-id="d8d84-249">Pilote ' Lics</span><span class="sxs-lookup"><span data-stu-id="d8d84-249">Driver' Lics</span></span>
- <span data-ttu-id="d8d84-250">Pilote ' certificat</span><span class="sxs-lookup"><span data-stu-id="d8d84-250">Driver' Licence</span></span>
- <span data-ttu-id="d8d84-251">Pilote « certificats</span><span class="sxs-lookup"><span data-stu-id="d8d84-251">Driver' Licences</span></span>
- <span data-ttu-id="d8d84-252">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="d8d84-252">Driver'sLic</span></span>
- <span data-ttu-id="d8d84-253">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="d8d84-253">Driver'sLics</span></span>
- <span data-ttu-id="d8d84-254">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="d8d84-254">Driver'sLicence</span></span>
- <span data-ttu-id="d8d84-255">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="d8d84-255">Driver'sLicences</span></span>
- <span data-ttu-id="d8d84-256">Lic du pilote</span><span class="sxs-lookup"><span data-stu-id="d8d84-256">Driver's Lic</span></span>
- <span data-ttu-id="d8d84-257">Lics permis de conduire</span><span class="sxs-lookup"><span data-stu-id="d8d84-257">Driver's Lics</span></span>
- <span data-ttu-id="d8d84-258">Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-258">Driver's Licence</span></span>
- <span data-ttu-id="d8d84-259">Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-259">Driver's Licences</span></span>
- <span data-ttu-id="d8d84-260">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="d8d84-260">DriverLic#</span></span>
- <span data-ttu-id="d8d84-261">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="d8d84-261">DriverLics#</span></span>
- <span data-ttu-id="d8d84-262">DriverLicence #</span><span class="sxs-lookup"><span data-stu-id="d8d84-262">DriverLicence#</span></span>
- <span data-ttu-id="d8d84-263">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="d8d84-263">DriverLicences#</span></span>
- <span data-ttu-id="d8d84-264">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="d8d84-264">Driver Lic#</span></span>
- <span data-ttu-id="d8d84-265">
#Permis conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-265">Driver Lics#</span></span>
- <span data-ttu-id="d8d84-266">Pilote certificat #</span><span class="sxs-lookup"><span data-stu-id="d8d84-266">Driver Licence#</span></span>
- <span data-ttu-id="d8d84-267">Pilote certificats #</span><span class="sxs-lookup"><span data-stu-id="d8d84-267">Driver Licences#</span></span>
- <span data-ttu-id="d8d84-268">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="d8d84-268">DriversLic#</span></span>
- <span data-ttu-id="d8d84-269">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="d8d84-269">DriversLics#</span></span>
- <span data-ttu-id="d8d84-270">DriversLicence #</span><span class="sxs-lookup"><span data-stu-id="d8d84-270">DriversLicence#</span></span>
- <span data-ttu-id="d8d84-271">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="d8d84-271">DriversLicences#</span></span>
- <span data-ttu-id="d8d84-272">Pilotes Lic #</span><span class="sxs-lookup"><span data-stu-id="d8d84-272">Drivers Lic#</span></span>
- <span data-ttu-id="d8d84-273">Pilotes Lics #</span><span class="sxs-lookup"><span data-stu-id="d8d84-273">Drivers Lics#</span></span>
- <span data-ttu-id="d8d84-274">Licence pilotes #</span><span class="sxs-lookup"><span data-stu-id="d8d84-274">Drivers Licence#</span></span>
- <span data-ttu-id="d8d84-275">Certificats pilotes #</span><span class="sxs-lookup"><span data-stu-id="d8d84-275">Drivers Licences#</span></span>
- <span data-ttu-id="d8d84-276">#Permisconduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-276">Driver'Lic#</span></span>
- <span data-ttu-id="d8d84-277">#Permisconduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-277">Driver'Lics#</span></span>
- <span data-ttu-id="d8d84-278">#Permisdeconduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-278">Driver'Licence#</span></span>
- <span data-ttu-id="d8d84-279">#Permisdeconduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-279">Driver'Licences#</span></span>
- <span data-ttu-id="d8d84-280">#Permis conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-280">Driver' Lic#</span></span>
- <span data-ttu-id="d8d84-281">#Permis conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-281">Driver' Lics#</span></span>
- <span data-ttu-id="d8d84-282">Pilote ' certificat #</span><span class="sxs-lookup"><span data-stu-id="d8d84-282">Driver' Licence#</span></span>
- <span data-ttu-id="d8d84-283">Pilote « certificats #</span><span class="sxs-lookup"><span data-stu-id="d8d84-283">Driver' Licences#</span></span>
- <span data-ttu-id="d8d84-284">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="d8d84-284">Driver'sLic#</span></span>
- <span data-ttu-id="d8d84-285">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="d8d84-285">Driver'sLics#</span></span>
- <span data-ttu-id="d8d84-286">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="d8d84-286">Driver'sLicence#</span></span>
- <span data-ttu-id="d8d84-287">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="d8d84-287">Driver'sLicences#</span></span>
- <span data-ttu-id="d8d84-288">#Permisconduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-288">Driver's Lic#</span></span>
- <span data-ttu-id="d8d84-289">#Permisconduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-289">Driver's Lics#</span></span>
- <span data-ttu-id="d8d84-290">Certificat de # permis de conduire</span><span class="sxs-lookup"><span data-stu-id="d8d84-290">Driver's Licence#</span></span>
- <span data-ttu-id="d8d84-291">Certificats de # permis de conduire</span><span class="sxs-lookup"><span data-stu-id="d8d84-291">Driver's Licences#</span></span> 

#### <a name="keywordaustraliadriverslicensenumberexclusions"></a><span data-ttu-id="d8d84-292">Keyword_australia_drivers_license_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="d8d84-292">Keyword_australia_drivers_license_number_exclusions</span></span>

- <span data-ttu-id="d8d84-293">aaa</span><span class="sxs-lookup"><span data-stu-id="d8d84-293">aaa</span></span>
- <span data-ttu-id="d8d84-294">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="d8d84-294">DriverLicense</span></span>
- <span data-ttu-id="d8d84-295">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="d8d84-295">DriverLicenses</span></span>
- <span data-ttu-id="d8d84-296">Conduire</span><span class="sxs-lookup"><span data-stu-id="d8d84-296">Driver License</span></span>
- <span data-ttu-id="d8d84-297">Licences de pilote</span><span class="sxs-lookup"><span data-stu-id="d8d84-297">Driver Licenses</span></span>
- <span data-ttu-id="d8d84-298">Conduire</span><span class="sxs-lookup"><span data-stu-id="d8d84-298">DriversLicense</span></span>
- <span data-ttu-id="d8d84-299">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="d8d84-299">DriversLicenses</span></span>
- <span data-ttu-id="d8d84-300">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="d8d84-300">Drivers License</span></span>
- <span data-ttu-id="d8d84-301">Licences de pilotes</span><span class="sxs-lookup"><span data-stu-id="d8d84-301">Drivers Licenses</span></span>
- <span data-ttu-id="d8d84-302">Driver'License</span><span class="sxs-lookup"><span data-stu-id="d8d84-302">Driver'License</span></span>
- <span data-ttu-id="d8d84-303">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="d8d84-303">Driver'Licenses</span></span>
- <span data-ttu-id="d8d84-304">Pilote ' licence</span><span class="sxs-lookup"><span data-stu-id="d8d84-304">Driver' License</span></span>
- <span data-ttu-id="d8d84-305">Pilote ' licences</span><span class="sxs-lookup"><span data-stu-id="d8d84-305">Driver' Licenses</span></span>
- <span data-ttu-id="d8d84-306">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="d8d84-306">Driver'sLicense</span></span>
- <span data-ttu-id="d8d84-307">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="d8d84-307">Driver'sLicenses</span></span>
- <span data-ttu-id="d8d84-308">Conduire permis de</span><span class="sxs-lookup"><span data-stu-id="d8d84-308">Driver's License</span></span>
- <span data-ttu-id="d8d84-309">Conduire permis de</span><span class="sxs-lookup"><span data-stu-id="d8d84-309">Driver's Licenses</span></span>
- <span data-ttu-id="d8d84-310">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="d8d84-310">DriverLicense#</span></span>
- <span data-ttu-id="d8d84-311">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="d8d84-311">DriverLicenses#</span></span>
- <span data-ttu-id="d8d84-312">Pilote licence #</span><span class="sxs-lookup"><span data-stu-id="d8d84-312">Driver License#</span></span>
- <span data-ttu-id="d8d84-313">Licences de pilote #</span><span class="sxs-lookup"><span data-stu-id="d8d84-313">Driver Licenses#</span></span>
- <span data-ttu-id="d8d84-314">Conduire #</span><span class="sxs-lookup"><span data-stu-id="d8d84-314">DriversLicense#</span></span>
- <span data-ttu-id="d8d84-315">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="d8d84-315">DriversLicenses#</span></span>
- <span data-ttu-id="d8d84-316">Licence pilotes #</span><span class="sxs-lookup"><span data-stu-id="d8d84-316">Drivers License#</span></span>
- <span data-ttu-id="d8d84-317">Licences pilotes #</span><span class="sxs-lookup"><span data-stu-id="d8d84-317">Drivers Licenses#</span></span>
- <span data-ttu-id="d8d84-318">#Permisdeconduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-318">Driver'License#</span></span>
- <span data-ttu-id="d8d84-319">#Permisdeconduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-319">Driver'Licenses#</span></span>
- <span data-ttu-id="d8d84-320">#Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-320">Driver' License#</span></span>
- <span data-ttu-id="d8d84-321">#Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-321">Driver' Licenses#</span></span>
- <span data-ttu-id="d8d84-322">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="d8d84-322">Driver'sLicense#</span></span>
- <span data-ttu-id="d8d84-323">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="d8d84-323">Driver'sLicenses#</span></span>
- <span data-ttu-id="d8d84-324">#Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-324">Driver's License#</span></span>
- <span data-ttu-id="d8d84-325">

#Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="d8d84-325">Driver's Licenses#</span></span>
   
## <a name="australia-medical-account-number"></a><span data-ttu-id="d8d84-326">Numéro de dossier médical Australie</span><span class="sxs-lookup"><span data-stu-id="d8d84-326">Australia Medical Account Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-327">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-327">Format</span></span>

<span data-ttu-id="d8d84-328">10 à 11 chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-328">10-11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-329">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-329">Pattern</span></span>

<span data-ttu-id="d8d84-330">10 à 11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="d8d84-330">10-11 digits:</span></span>
- <span data-ttu-id="d8d84-331">Le premier chiffre est compris entre 2 et 6</span><span class="sxs-lookup"><span data-stu-id="d8d84-331">First digit is in the range 2-6</span></span>
- <span data-ttu-id="d8d84-332">Le neuvième chiffre est un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-332">Ninth digit is a check digit</span></span>
- <span data-ttu-id="d8d84-333">Le dixième chiffre est le chiffre d’émission</span><span class="sxs-lookup"><span data-stu-id="d8d84-333">Tenth digit is the issue digit</span></span>
- <span data-ttu-id="d8d84-334">Le onzième chiffre (facultatif) est le numéro individuel</span><span class="sxs-lookup"><span data-stu-id="d8d84-334">Eleventh digit (optional) is the individual number</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-335">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-335">Checksum</span></span>

<span data-ttu-id="d8d84-336">Oui</span><span class="sxs-lookup"><span data-stu-id="d8d84-336">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-337">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-337">Definition</span></span>

<span data-ttu-id="d8d84-338">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 95 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-338">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-339">La fonction Func_australian_medical_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-339">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-340">Un mot clé figurant dans la liste Keyword_Australia_Medical_Account_Number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-340">A keyword from Keyword_Australia_Medical_Account_Number is found.</span></span>
- <span data-ttu-id="d8d84-341">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-341">The checksum passes.</span></span>

<span data-ttu-id="d8d84-342">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-342">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-343">La fonction Func_australian_medical_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-343">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-344">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-344">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-345">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-345">Keywords</span></span>

#### <a name="keywordaustraliamedicalaccountnumber"></a><span data-ttu-id="d8d84-346">Keyword_Australia_Medical_Account_Number</span><span class="sxs-lookup"><span data-stu-id="d8d84-346">Keyword_Australia_Medical_Account_Number</span></span>

- <span data-ttu-id="d8d84-347">informations sur le compte bancaire</span><span class="sxs-lookup"><span data-stu-id="d8d84-347">bank account details</span></span>
- <span data-ttu-id="d8d84-348">
remboursements d’assurance maladie</span><span class="sxs-lookup"><span data-stu-id="d8d84-348">medicare payments</span></span>
- <span data-ttu-id="d8d84-349">
compte de prêts immobiliers</span><span class="sxs-lookup"><span data-stu-id="d8d84-349">mortgage account</span></span>
- <span data-ttu-id="d8d84-350">
paiements bancaires</span><span class="sxs-lookup"><span data-stu-id="d8d84-350">bank payments</span></span>
- <span data-ttu-id="d8d84-351">
direction de l’information</span><span class="sxs-lookup"><span data-stu-id="d8d84-351">information branch</span></span>
- <span data-ttu-id="d8d84-352">
prêt sur carte de crédit</span><span class="sxs-lookup"><span data-stu-id="d8d84-352">credit card loan</span></span>
- <span data-ttu-id="d8d84-353">
département des services sociaux</span><span class="sxs-lookup"><span data-stu-id="d8d84-353">department of human services</span></span>
- <span data-ttu-id="d8d84-354">service local</span><span class="sxs-lookup"><span data-stu-id="d8d84-354">local service</span></span>
- <span data-ttu-id="d8d84-355">

medicare</span><span class="sxs-lookup"><span data-stu-id="d8d84-355">medicare</span></span>

   
## <a name="australia-passport-number"></a><span data-ttu-id="d8d84-356">Numéro de passeport Australie</span><span class="sxs-lookup"><span data-stu-id="d8d84-356">Australia Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-357">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-357">Format</span></span>

<span data-ttu-id="d8d84-358">Une lettre suivie de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-358">A letter followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-359">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-359">Pattern</span></span>

<span data-ttu-id="d8d84-360">Une lettre (ne respectant pas la casse) suivie de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-360">A letter (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-361">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-361">Checksum</span></span>

<span data-ttu-id="d8d84-362">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-362">No</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-363">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-363">Definition</span></span>

<span data-ttu-id="d8d84-364">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-365">L’expression régulière Regex_australia_passport_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-365">The regular expression Regex_australia_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-366">Un mot clé à partir de Keyword_passport ou Keyword_australia_passport_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-366">A keyword from Keyword_passport or Keyword_australia_passport_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-367">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-367">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="d8d84-368">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="d8d84-368">Keyword_passport</span></span>

- <span data-ttu-id="d8d84-369">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8d84-369">Passport Number</span></span>
- <span data-ttu-id="d8d84-370">
N° de passeport</span><span class="sxs-lookup"><span data-stu-id="d8d84-370">Passport No</span></span>
- <span data-ttu-id="d8d84-371"># Passeport
</span><span class="sxs-lookup"><span data-stu-id="d8d84-371">Passport #</span></span>
- <span data-ttu-id="d8d84-372">#Passeport
</span><span class="sxs-lookup"><span data-stu-id="d8d84-372">Passport#</span></span>
- <span data-ttu-id="d8d84-373">IDPassport</span><span class="sxs-lookup"><span data-stu-id="d8d84-373">PassportID</span></span>
- <span data-ttu-id="d8d84-374">n° passeport
</span><span class="sxs-lookup"><span data-stu-id="d8d84-374">Passportno</span></span>
- <span data-ttu-id="d8d84-375">numéropasseport
</span><span class="sxs-lookup"><span data-stu-id="d8d84-375">passportnumber</span></span>
- <span data-ttu-id="d8d84-376">パスポート</span><span class="sxs-lookup"><span data-stu-id="d8d84-376">パスポート</span></span>
- <span data-ttu-id="d8d84-377">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="d8d84-377">パスポート番号</span></span>
- <span data-ttu-id="d8d84-378">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="d8d84-378">パスポートのNum</span></span>
- <span data-ttu-id="d8d84-379">
パスポート＃
</span><span class="sxs-lookup"><span data-stu-id="d8d84-379">パスポート ＃</span></span> 
- <span data-ttu-id="d8d84-380">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8d84-380">Numéro de passeport</span></span>
- <span data-ttu-id="d8d84-381">
Passeport n°</span><span class="sxs-lookup"><span data-stu-id="d8d84-381">Passeport n °</span></span>
- <span data-ttu-id="d8d84-382">Passeport numéro
</span><span class="sxs-lookup"><span data-stu-id="d8d84-382">Passeport Non</span></span>
- <span data-ttu-id="d8d84-383"># Passeport
</span><span class="sxs-lookup"><span data-stu-id="d8d84-383">Passeport #</span></span>
- <span data-ttu-id="d8d84-384">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="d8d84-384">Passeport#</span></span>
- <span data-ttu-id="d8d84-385">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="d8d84-385">PasseportNon</span></span>
- <span data-ttu-id="d8d84-386">Passeportn °
</span><span class="sxs-lookup"><span data-stu-id="d8d84-386">Passeportn °</span></span>

#### <a name="keywordaustraliapassportnumber"></a><span data-ttu-id="d8d84-387">Keyword_australia_passport_number</span><span class="sxs-lookup"><span data-stu-id="d8d84-387">Keyword_australia_passport_number</span></span>

- <span data-ttu-id="d8d84-388">passeport</span><span class="sxs-lookup"><span data-stu-id="d8d84-388">passport</span></span>
- <span data-ttu-id="d8d84-389">
informations sur le passeport</span><span class="sxs-lookup"><span data-stu-id="d8d84-389">passport details</span></span>
- <span data-ttu-id="d8d84-390">
immigration et citoyenneté</span><span class="sxs-lookup"><span data-stu-id="d8d84-390">immigration and citizenship</span></span>
- <span data-ttu-id="d8d84-391">
Australie</span><span class="sxs-lookup"><span data-stu-id="d8d84-391">commonwealth of australia</span></span>
- <span data-ttu-id="d8d84-392">
service de l’immigration</span><span class="sxs-lookup"><span data-stu-id="d8d84-392">department of immigration</span></span>
- <span data-ttu-id="d8d84-393">
adresse de résidence</span><span class="sxs-lookup"><span data-stu-id="d8d84-393">residential address</span></span>
- <span data-ttu-id="d8d84-394">
service de l’immigration et de la citoyenneté</span><span class="sxs-lookup"><span data-stu-id="d8d84-394">department of immigration and citizenship</span></span>
- <span data-ttu-id="d8d84-395">visa
</span><span class="sxs-lookup"><span data-stu-id="d8d84-395">visa</span></span>
- <span data-ttu-id="d8d84-396">
Carte nationale d’identité</span><span class="sxs-lookup"><span data-stu-id="d8d84-396">national identity card</span></span>
- <span data-ttu-id="d8d84-397">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8d84-397">passport number</span></span>
- <span data-ttu-id="d8d84-398">
document de voyage</span><span class="sxs-lookup"><span data-stu-id="d8d84-398">travel document</span></span>
- <span data-ttu-id="d8d84-399">

autorité émettrice</span><span class="sxs-lookup"><span data-stu-id="d8d84-399">issuing authority</span></span>
   
## <a name="australia-tax-file-number"></a><span data-ttu-id="d8d84-400">Numéro de dossier fiscal Australie</span><span class="sxs-lookup"><span data-stu-id="d8d84-400">Australia Tax File Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-401">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-401">Format</span></span>

<span data-ttu-id="d8d84-402">8 ou 9 chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-402">8-9 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-403">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-403">Pattern</span></span>

<span data-ttu-id="d8d84-404">8 à 9 chiffres généralement entrecoupés d’espaces comme suit :</span><span class="sxs-lookup"><span data-stu-id="d8d84-404">8-9 digits typically presented with spaces as follows:</span></span>
- <span data-ttu-id="d8d84-405">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-405">Three digits</span></span> 
- <span data-ttu-id="d8d84-406">Un espace facultatif</span><span class="sxs-lookup"><span data-stu-id="d8d84-406">An optional space</span></span> 
- <span data-ttu-id="d8d84-407">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-407">Three digits</span></span> 
- <span data-ttu-id="d8d84-408">Un espace facultatif</span><span class="sxs-lookup"><span data-stu-id="d8d84-408">An optional space</span></span> 
- <span data-ttu-id="d8d84-409">2 à 3 chiffres où le dernier chiffre est un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-409">2-3 digits where the last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-410">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-410">Checksum</span></span>

<span data-ttu-id="d8d84-411">Oui</span><span class="sxs-lookup"><span data-stu-id="d8d84-411">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-412">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-412">Definition</span></span>

<span data-ttu-id="d8d84-413">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-413">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-414">La fonction Func_australian_tax_file_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-414">The function Func_australian_tax_file_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-415">Aucun mot clé figurant dans la liste Keyword_Australia_Tax_File_Number ou Keyword_number_exclusions n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-415">No keyword from Keyword_Australia_Tax_File_Number or Keyword_number_exclusions is found.</span></span>
- <span data-ttu-id="d8d84-416">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-416">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-417">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-417">Keywords</span></span>

#### <a name="keywordaustraliataxfilenumber"></a><span data-ttu-id="d8d84-418">Keyword_Australia_Tax_File_Number</span><span class="sxs-lookup"><span data-stu-id="d8d84-418">Keyword_Australia_Tax_File_Number</span></span>

- <span data-ttu-id="d8d84-419">numéro d’entreprise australien</span><span class="sxs-lookup"><span data-stu-id="d8d84-419">australian business number</span></span>
- <span data-ttu-id="d8d84-420">
taux d’imposition marginale</span><span class="sxs-lookup"><span data-stu-id="d8d84-420">marginal tax rate</span></span>
- <span data-ttu-id="d8d84-421">
prélèvement d’assurance maladie</span><span class="sxs-lookup"><span data-stu-id="d8d84-421">medicare levy</span></span>
- <span data-ttu-id="d8d84-422">
numéro de portefeuille</span><span class="sxs-lookup"><span data-stu-id="d8d84-422">portfolio number</span></span>
- <span data-ttu-id="d8d84-423">
service des vétérans</span><span class="sxs-lookup"><span data-stu-id="d8d84-423">service veterans</span></span>
- <span data-ttu-id="d8d84-424">
retenue à la source</span><span class="sxs-lookup"><span data-stu-id="d8d84-424">withholding tax</span></span>
- <span data-ttu-id="d8d84-425">
déclaration d’impôts individuels</span><span class="sxs-lookup"><span data-stu-id="d8d84-425">individual tax return</span></span>
- <span data-ttu-id="d8d84-426">

numéro de dossier fiscal</span><span class="sxs-lookup"><span data-stu-id="d8d84-426">tax file number</span></span>

#### <a name="keywordnumberexclusions"></a><span data-ttu-id="d8d84-427">Keyword_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="d8d84-427">Keyword_number_exclusions</span></span>

- <span data-ttu-id="d8d84-428">00000000</span><span class="sxs-lookup"><span data-stu-id="d8d84-428">00000000</span></span>
- <span data-ttu-id="d8d84-429">11111111</span><span class="sxs-lookup"><span data-stu-id="d8d84-429">11111111</span></span>
- <span data-ttu-id="d8d84-430">22222222</span><span class="sxs-lookup"><span data-stu-id="d8d84-430">22222222</span></span>
- <span data-ttu-id="d8d84-431">33333333</span><span class="sxs-lookup"><span data-stu-id="d8d84-431">33333333</span></span>
- <span data-ttu-id="d8d84-432">44444444</span><span class="sxs-lookup"><span data-stu-id="d8d84-432">44444444</span></span>
- <span data-ttu-id="d8d84-433">55555555</span><span class="sxs-lookup"><span data-stu-id="d8d84-433">55555555</span></span>
- <span data-ttu-id="d8d84-434">66666666</span><span class="sxs-lookup"><span data-stu-id="d8d84-434">66666666</span></span>
- <span data-ttu-id="d8d84-435">77777777</span><span class="sxs-lookup"><span data-stu-id="d8d84-435">77777777</span></span>
- <span data-ttu-id="d8d84-436">88888888</span><span class="sxs-lookup"><span data-stu-id="d8d84-436">88888888</span></span>
- <span data-ttu-id="d8d84-437">99999999</span><span class="sxs-lookup"><span data-stu-id="d8d84-437">99999999</span></span>
- <span data-ttu-id="d8d84-438">000000000</span><span class="sxs-lookup"><span data-stu-id="d8d84-438">000000000</span></span>
- <span data-ttu-id="d8d84-439">111111111</span><span class="sxs-lookup"><span data-stu-id="d8d84-439">111111111</span></span>
- <span data-ttu-id="d8d84-440">222222222</span><span class="sxs-lookup"><span data-stu-id="d8d84-440">222222222</span></span>
- <span data-ttu-id="d8d84-441">333333333</span><span class="sxs-lookup"><span data-stu-id="d8d84-441">333333333</span></span>
- <span data-ttu-id="d8d84-442">444444444</span><span class="sxs-lookup"><span data-stu-id="d8d84-442">444444444</span></span>
- <span data-ttu-id="d8d84-443">555555555</span><span class="sxs-lookup"><span data-stu-id="d8d84-443">555555555</span></span>
- <span data-ttu-id="d8d84-444">666666666</span><span class="sxs-lookup"><span data-stu-id="d8d84-444">666666666</span></span>
- <span data-ttu-id="d8d84-445">777777777</span><span class="sxs-lookup"><span data-stu-id="d8d84-445">777777777</span></span>
- <span data-ttu-id="d8d84-446">888888888</span><span class="sxs-lookup"><span data-stu-id="d8d84-446">888888888</span></span>
- <span data-ttu-id="d8d84-447">999999999</span><span class="sxs-lookup"><span data-stu-id="d8d84-447">999999999</span></span>
- <span data-ttu-id="d8d84-448">0000000000</span><span class="sxs-lookup"><span data-stu-id="d8d84-448">0000000000</span></span>
- <span data-ttu-id="d8d84-449">1111111111</span><span class="sxs-lookup"><span data-stu-id="d8d84-449">1111111111</span></span>
- <span data-ttu-id="d8d84-450">2222222222</span><span class="sxs-lookup"><span data-stu-id="d8d84-450">2222222222</span></span>
- <span data-ttu-id="d8d84-451">3333333333</span><span class="sxs-lookup"><span data-stu-id="d8d84-451">3333333333</span></span>
- <span data-ttu-id="d8d84-452">4444444444</span><span class="sxs-lookup"><span data-stu-id="d8d84-452">4444444444</span></span>
- <span data-ttu-id="d8d84-453">5555555555</span><span class="sxs-lookup"><span data-stu-id="d8d84-453">5555555555</span></span>
- <span data-ttu-id="d8d84-454">6666666666</span><span class="sxs-lookup"><span data-stu-id="d8d84-454">6666666666</span></span>
- <span data-ttu-id="d8d84-455">7777777777</span><span class="sxs-lookup"><span data-stu-id="d8d84-455">7777777777</span></span>
- <span data-ttu-id="d8d84-456">8888888888</span><span class="sxs-lookup"><span data-stu-id="d8d84-456">8888888888</span></span>
- <span data-ttu-id="d8d84-457">9999999999</span><span class="sxs-lookup"><span data-stu-id="d8d84-457">9999999999</span></span>
   
## <a name="belgium-national-number"></a><span data-ttu-id="d8d84-458">Numéro national Belgique</span><span class="sxs-lookup"><span data-stu-id="d8d84-458">Belgium National Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-459">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-459">Format</span></span>

<span data-ttu-id="d8d84-460">11 chiffres plus des délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d8d84-460">11 digits plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-461">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-461">Pattern</span></span>

<span data-ttu-id="d8d84-462">11 chiffres plus des délimiteurs :</span><span class="sxs-lookup"><span data-stu-id="d8d84-462">11 digits plus delimiters:</span></span>
- <span data-ttu-id="d8d84-463">Six chiffres et deux points au format AA.MM.JJ pour la date de naissance </span><span class="sxs-lookup"><span data-stu-id="d8d84-463">Six digits and two periods in the format YY.MM.DD for date of birth</span></span> 
- <span data-ttu-id="d8d84-464">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="d8d84-464">A hyphen</span></span> 
- <span data-ttu-id="d8d84-465">Trois chiffres séquentiels (impairs pour les hommes, pairs pour les femmes) </span><span class="sxs-lookup"><span data-stu-id="d8d84-465">Three sequential digits (odd for males, even for females)</span></span> 
- <span data-ttu-id="d8d84-466">Un point </span><span class="sxs-lookup"><span data-stu-id="d8d84-466">A period</span></span> 
- <span data-ttu-id="d8d84-467">Deux chiffres de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-467">Two digits that are a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-468">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-468">Checksum</span></span>

<span data-ttu-id="d8d84-469">Oui</span><span class="sxs-lookup"><span data-stu-id="d8d84-469">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-470">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-470">Definition</span></span>

<span data-ttu-id="d8d84-471">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-471">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-472">La fonction Func_belgium_national_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-472">The function Func_belgium_national_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-473">Un mot clé figurant dans la liste Keyword_belgium_national_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-473">A keyword from Keyword_belgium_national_number is found.</span></span>
- <span data-ttu-id="d8d84-474">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-474">The checksum passes.</span></span>

```
<!-- Belgium National Number -->
  <Entity id="fb969c9e-0fd1-4b18-8091-a2123c5e6a54" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_belgium_national_number"/>
     <Match idRef="Keyword_belgium_national_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8d84-475">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-475">Keywords</span></span>

#### <a name="keywordbelgiumnationalnumber"></a><span data-ttu-id="d8d84-476">Keyword_belgium_national_number</span><span class="sxs-lookup"><span data-stu-id="d8d84-476">Keyword_belgium_national_number</span></span>

- <span data-ttu-id="d8d84-477">Identité</span><span class="sxs-lookup"><span data-stu-id="d8d84-477">Identity</span></span>
- <span data-ttu-id="d8d84-478">Registration</span><span class="sxs-lookup"><span data-stu-id="d8d84-478">Registration</span></span>
- <span data-ttu-id="d8d84-479">Identification</span><span class="sxs-lookup"><span data-stu-id="d8d84-479">Identification</span></span> 
- <span data-ttu-id="d8d84-480">ID</span><span class="sxs-lookup"><span data-stu-id="d8d84-480">ID</span></span> 
- <span data-ttu-id="d8d84-481">Identiteitskaart</span><span class="sxs-lookup"><span data-stu-id="d8d84-481">Identiteitskaart</span></span>
- <span data-ttu-id="d8d84-482">Registratie nummer 
</span><span class="sxs-lookup"><span data-stu-id="d8d84-482">Registratie nummer</span></span> 
- <span data-ttu-id="d8d84-483">Identificatie nummer
</span><span class="sxs-lookup"><span data-stu-id="d8d84-483">Identificatie nummer</span></span> 
- <span data-ttu-id="d8d84-484">Identiteit</span><span class="sxs-lookup"><span data-stu-id="d8d84-484">Identiteit</span></span>
- <span data-ttu-id="d8d84-485">Registratie</span><span class="sxs-lookup"><span data-stu-id="d8d84-485">Registratie</span></span>
- <span data-ttu-id="d8d84-486">Identificatie

</span><span class="sxs-lookup"><span data-stu-id="d8d84-486">Identificatie</span></span> 
- <span data-ttu-id="d8d84-487">Carte d’identité
</span><span class="sxs-lookup"><span data-stu-id="d8d84-487">Carte d’identité</span></span> 
- <span data-ttu-id="d8d84-488">numéro d’immatriculation</span><span class="sxs-lookup"><span data-stu-id="d8d84-488">numéro d'immatriculation</span></span>
- <span data-ttu-id="d8d84-489">numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="d8d84-489">numéro d'identification</span></span>
- <span data-ttu-id="d8d84-490">
identité
</span><span class="sxs-lookup"><span data-stu-id="d8d84-490">identité</span></span> 
- <span data-ttu-id="d8d84-491">inscription
</span><span class="sxs-lookup"><span data-stu-id="d8d84-491">inscription</span></span> 
- <span data-ttu-id="d8d84-492">Identifikation</span><span class="sxs-lookup"><span data-stu-id="d8d84-492">Identifikation</span></span>
- <span data-ttu-id="d8d84-493">Identifizierung</span><span class="sxs-lookup"><span data-stu-id="d8d84-493">Identifizierung</span></span>
- <span data-ttu-id="d8d84-494">Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="d8d84-494">Identifikationsnummer</span></span>
- <span data-ttu-id="d8d84-495">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="d8d84-495">Personalausweis</span></span>
- <span data-ttu-id="d8d84-496">Registrierung</span><span class="sxs-lookup"><span data-stu-id="d8d84-496">Registrierung</span></span>
- <span data-ttu-id="d8d84-497">Registrationsnummer</span><span class="sxs-lookup"><span data-stu-id="d8d84-497">Registrationsnummer</span></span>

   
## <a name="brazil-cpf-number"></a><span data-ttu-id="d8d84-498">Numéro CPF Brésil</span><span class="sxs-lookup"><span data-stu-id="d8d84-498">Brazil CPF Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-499">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-499">Format</span></span>

<span data-ttu-id="d8d84-500">11 chiffres qui incluent un chiffre de contrôle et peuvent ou non être mis en forme </span><span class="sxs-lookup"><span data-stu-id="d8d84-500">11 digits that include a check digit and can be formatted or unformatted</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-501">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-501">Pattern</span></span>

<span data-ttu-id="d8d84-502">Mis en forme :</span><span class="sxs-lookup"><span data-stu-id="d8d84-502">Formatted:</span></span>
- <span data-ttu-id="d8d84-503">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-503">Three digits</span></span> 
- <span data-ttu-id="d8d84-504">Un point </span><span class="sxs-lookup"><span data-stu-id="d8d84-504">A period</span></span> 
- <span data-ttu-id="d8d84-505">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-505">Three digits</span></span> 
- <span data-ttu-id="d8d84-506">Un point </span><span class="sxs-lookup"><span data-stu-id="d8d84-506">A period</span></span> 
- <span data-ttu-id="d8d84-507">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-507">Three digits</span></span> 
- <span data-ttu-id="d8d84-508">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="d8d84-508">A hyphen</span></span> 
- <span data-ttu-id="d8d84-509">Deux chiffres de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-509">Two digits which are check digits</span></span>

<span data-ttu-id="d8d84-510">Non mis en forme :</span><span class="sxs-lookup"><span data-stu-id="d8d84-510">Unformatted:</span></span>
- <span data-ttu-id="d8d84-511">11 chiffres où les deux derniers sont des chiffres de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-511">11 digits where the last two digits are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-512">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-512">Checksum</span></span>

<span data-ttu-id="d8d84-513">Oui</span><span class="sxs-lookup"><span data-stu-id="d8d84-513">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-514">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-514">Definition</span></span>

<span data-ttu-id="d8d84-515">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-515">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-516">La fonction Func_brazil_cpf trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-516">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-517">Un mot clé figurant dans la liste Keyword_brazil_cpf est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-517">A keyword from Keyword_brazil_cpf is found.</span></span>
- <span data-ttu-id="d8d84-518">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-518">The checksum passes.</span></span>

<span data-ttu-id="d8d84-519">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-519">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-520">La fonction Func_brazil_cpf trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-520">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-521">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-521">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-522">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-522">Keywords</span></span>

#### <a name="keywordbrazilcpf"></a><span data-ttu-id="d8d84-523">Keyword_brazil_cpf</span><span class="sxs-lookup"><span data-stu-id="d8d84-523">Keyword_brazil_cpf</span></span>

- <span data-ttu-id="d8d84-524">CPF</span><span class="sxs-lookup"><span data-stu-id="d8d84-524">CPF</span></span>
- <span data-ttu-id="d8d84-525">Identification</span><span class="sxs-lookup"><span data-stu-id="d8d84-525">Identification</span></span>
- <span data-ttu-id="d8d84-526">Registration</span><span class="sxs-lookup"><span data-stu-id="d8d84-526">Registration</span></span>
- <span data-ttu-id="d8d84-527">Revenue</span><span class="sxs-lookup"><span data-stu-id="d8d84-527">Revenue</span></span>
- <span data-ttu-id="d8d84-528">Cadastro de Pessoas Físicas
</span><span class="sxs-lookup"><span data-stu-id="d8d84-528">Cadastro de Pessoas Físicas</span></span> 
- <span data-ttu-id="d8d84-529">Imposto
</span><span class="sxs-lookup"><span data-stu-id="d8d84-529">Imposto</span></span> 
- <span data-ttu-id="d8d84-530">Identificação
</span><span class="sxs-lookup"><span data-stu-id="d8d84-530">Identificação</span></span> 
- <span data-ttu-id="d8d84-531">Inscrição
</span><span class="sxs-lookup"><span data-stu-id="d8d84-531">Inscrição</span></span> 
- <span data-ttu-id="d8d84-532">Receita

</span><span class="sxs-lookup"><span data-stu-id="d8d84-532">Receita</span></span> 
   
## <a name="brazil-legal-entity-number-cnpj"></a><span data-ttu-id="d8d84-533">Numéro d’entité juridique (CNPJ) Brésil</span><span class="sxs-lookup"><span data-stu-id="d8d84-533">Brazil Legal Entity Number (CNPJ)</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-534">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-534">Format</span></span>

<span data-ttu-id="d8d84-535">14 chiffres qui incluent un numéro d’enregistrement, un numéro de succursale et des chiffres de contrôle, avec des délimiteurs en plus</span><span class="sxs-lookup"><span data-stu-id="d8d84-535">14 digits that include a registration number, branch number, and check digits, plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-536">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-536">Pattern</span></span>
<span data-ttu-id="d8d84-537">14 chiffres plus des délimiteurs :</span><span class="sxs-lookup"><span data-stu-id="d8d84-537">14 digits, plus delimiters:</span></span>
- <span data-ttu-id="d8d84-538">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-538">Two digits</span></span> 
- <span data-ttu-id="d8d84-539">Un point </span><span class="sxs-lookup"><span data-stu-id="d8d84-539">A period</span></span> 
- <span data-ttu-id="d8d84-540">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-540">Three digits</span></span> 
- <span data-ttu-id="d8d84-541">Un point </span><span class="sxs-lookup"><span data-stu-id="d8d84-541">A period</span></span> 
- <span data-ttu-id="d8d84-542">Trois chiffres (ces huit premiers chiffres composent le numéro d’enregistrement) </span><span class="sxs-lookup"><span data-stu-id="d8d84-542">Three digits (these first eight digits are the registration number)</span></span> 
- <span data-ttu-id="d8d84-543">Une barre oblique </span><span class="sxs-lookup"><span data-stu-id="d8d84-543">A forward slash</span></span> 
- <span data-ttu-id="d8d84-544">Le numéro de succursale à quatre chiffres </span><span class="sxs-lookup"><span data-stu-id="d8d84-544">Four-digit branch number</span></span> 
- <span data-ttu-id="d8d84-545">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="d8d84-545">A hyphen</span></span> 
- <span data-ttu-id="d8d84-546">Deux chiffres de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-546">Two digits which are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-547">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-547">Checksum</span></span>

<span data-ttu-id="d8d84-548">Oui</span><span class="sxs-lookup"><span data-stu-id="d8d84-548">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-549">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-549">Definition</span></span>

<span data-ttu-id="d8d84-550">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-550">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-551">La fonction Func_brazil_cnpj trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-551">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-552">Un mot clé figurant dans la liste Keyword_brazil_cnpj est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-552">A keyword from Keyword_brazil_cnpj is found.</span></span>
- <span data-ttu-id="d8d84-553">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-553">The checksum passes.</span></span>

<span data-ttu-id="d8d84-554">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-554">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-555">La fonction Func_brazil_cnpj trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-555">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-556">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-556">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-557">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-557">Keywords</span></span>

#### <a name="keywordbrazilcnpj"></a><span data-ttu-id="d8d84-558">Keyword_brazil_cnpj</span><span class="sxs-lookup"><span data-stu-id="d8d84-558">Keyword_brazil_cnpj</span></span>

- <span data-ttu-id="d8d84-559">CNPJ
</span><span class="sxs-lookup"><span data-stu-id="d8d84-559">CNPJ</span></span> 
- <span data-ttu-id="d8d84-560">CNPJ/MF</span><span class="sxs-lookup"><span data-stu-id="d8d84-560">CNPJ/MF</span></span> 
- <span data-ttu-id="d8d84-561">CNPJ-MF
</span><span class="sxs-lookup"><span data-stu-id="d8d84-561">CNPJ-MF</span></span> 
- <span data-ttu-id="d8d84-562">National Registry of Legal Entities
</span><span class="sxs-lookup"><span data-stu-id="d8d84-562">National Registry of Legal Entities</span></span> 
- <span data-ttu-id="d8d84-563">Taxpayers Registry
</span><span class="sxs-lookup"><span data-stu-id="d8d84-563">Taxpayers Registry</span></span> 
- <span data-ttu-id="d8d84-564">Legal entity
</span><span class="sxs-lookup"><span data-stu-id="d8d84-564">Legal entity</span></span> 
- <span data-ttu-id="d8d84-565">Legal entities
</span><span class="sxs-lookup"><span data-stu-id="d8d84-565">Legal entities</span></span> 
- <span data-ttu-id="d8d84-566">Registration Status
</span><span class="sxs-lookup"><span data-stu-id="d8d84-566">Registration Status</span></span> 
- <span data-ttu-id="d8d84-567">Business
</span><span class="sxs-lookup"><span data-stu-id="d8d84-567">Business</span></span> 
- <span data-ttu-id="d8d84-568">Company</span><span class="sxs-lookup"><span data-stu-id="d8d84-568">Company</span></span>
- <span data-ttu-id="d8d84-569">CNPJ
</span><span class="sxs-lookup"><span data-stu-id="d8d84-569">CNPJ</span></span> 
- <span data-ttu-id="d8d84-570">Cadastro Nacional da Pessoa Jurídica
</span><span class="sxs-lookup"><span data-stu-id="d8d84-570">Cadastro Nacional da Pessoa Jurídica</span></span> 
- <span data-ttu-id="d8d84-571">Cadastro Geral de Contribuintes
</span><span class="sxs-lookup"><span data-stu-id="d8d84-571">Cadastro Geral de Contribuintes</span></span> 
- <span data-ttu-id="d8d84-572">CGC
</span><span class="sxs-lookup"><span data-stu-id="d8d84-572">CGC</span></span> 
- <span data-ttu-id="d8d84-573">Pessoa jurídica
</span><span class="sxs-lookup"><span data-stu-id="d8d84-573">Pessoa jurídica</span></span> 
- <span data-ttu-id="d8d84-574">Pessoas jurídicas
</span><span class="sxs-lookup"><span data-stu-id="d8d84-574">Pessoas jurídicas</span></span> 
- <span data-ttu-id="d8d84-575">Situação cadastral
</span><span class="sxs-lookup"><span data-stu-id="d8d84-575">Situação cadastral</span></span> 
- <span data-ttu-id="d8d84-576">Inscrição
</span><span class="sxs-lookup"><span data-stu-id="d8d84-576">Inscrição</span></span> 
- <span data-ttu-id="d8d84-577">Empresa
</span><span class="sxs-lookup"><span data-stu-id="d8d84-577">Empresa</span></span> 
   
## <a name="brazil-national-id-card-rg"></a><span data-ttu-id="d8d84-578">	Brazil National ID Card (RG)</span><span class="sxs-lookup"><span data-stu-id="d8d84-578">Brazil National ID Card (RG)</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-579">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-579">Format</span></span>

<span data-ttu-id="d8d84-580">Registro Geral (ancien format) : neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-580">Registro Geral (old format): Nine digits</span></span>

<span data-ttu-id="d8d84-581">Registro de Identidade (RIC) (nouveau format) : 11 chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-581">Registro de Identidade (RIC) (new format): 11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-582">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-582">Pattern</span></span>

<span data-ttu-id="d8d84-583">Registro Geral (ancien format) :</span><span class="sxs-lookup"><span data-stu-id="d8d84-583">Registro Geral (old format):</span></span>
- <span data-ttu-id="d8d84-584">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-584">Two digits</span></span> 
- <span data-ttu-id="d8d84-585">Un point </span><span class="sxs-lookup"><span data-stu-id="d8d84-585">A period</span></span> 
- <span data-ttu-id="d8d84-586">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-586">Three digits</span></span> 
- <span data-ttu-id="d8d84-587">Un point </span><span class="sxs-lookup"><span data-stu-id="d8d84-587">A period</span></span> 
- <span data-ttu-id="d8d84-588">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-588">Three digits</span></span> 
- <span data-ttu-id="d8d84-589">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="d8d84-589">A hyphen</span></span> 
- <span data-ttu-id="d8d84-590">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-590">One digit which is a check digit</span></span>

<span data-ttu-id="d8d84-591">Registro de Identidade (RIC) (nouveau format) :</span><span class="sxs-lookup"><span data-stu-id="d8d84-591">Registro de Identidade (RIC) (new format):</span></span>
- <span data-ttu-id="d8d84-592">10 chiffres </span><span class="sxs-lookup"><span data-stu-id="d8d84-592">10 digits</span></span> 
- <span data-ttu-id="d8d84-593">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="d8d84-593">A hyphen</span></span> 
- <span data-ttu-id="d8d84-594">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-594">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-595">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-595">Checksum</span></span>

<span data-ttu-id="d8d84-596">Oui</span><span class="sxs-lookup"><span data-stu-id="d8d84-596">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-597">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-597">Definition</span></span>

<span data-ttu-id="d8d84-598">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-598">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-599">La fonction Func_brazil_rg trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-599">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-600">Un mot clé figurant dans la liste Keyword_brazil_rg est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-600">A keyword from Keyword_brazil_rg is found.</span></span>
- <span data-ttu-id="d8d84-601">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-601">The checksum passes.</span></span>

<span data-ttu-id="d8d84-602">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-602">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-603">La fonction Func_brazil_rg trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-603">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-604">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-604">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-605">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-605">Keywords</span></span>

#### <a name="keywordbrazilrg"></a><span data-ttu-id="d8d84-606">Keyword_brazil_rg</span><span class="sxs-lookup"><span data-stu-id="d8d84-606">Keyword_brazil_rg</span></span>

<span data-ttu-id="d8d84-607">Cédula de identidade carte d’identité id national número de rregistro registro de Iidentidade registro geral RG (ce mot clé respecte la casse) RIC (ce mot clé respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="d8d84-607">Cédula de identidade identity card national id número de rregistro registro de Iidentidade registro geral RG (this keyword is case sensitive) RIC (this keyword is case sensitive)</span></span> 
   
## <a name="canada-bank-account-number"></a><span data-ttu-id="d8d84-608">Numéro de compte bancaire Canada</span><span class="sxs-lookup"><span data-stu-id="d8d84-608">Canada Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-609">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-609">Format</span></span>

<span data-ttu-id="d8d84-610">Sept ou douze chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-610">Seven or twelve digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-611">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-611">Pattern</span></span>

<span data-ttu-id="d8d84-612">Un numéro de compte bancaire au Canada est composé de sept ou douze chiffres.</span><span class="sxs-lookup"><span data-stu-id="d8d84-612">A Canada Bank Account Number is seven or twelve digits.</span></span>

<span data-ttu-id="d8d84-613">Un numéro de transit de compte bancaire du Canada est indiqué au format suivant :</span><span class="sxs-lookup"><span data-stu-id="d8d84-613">A Canada bank account transit number is:</span></span>
- <span data-ttu-id="d8d84-614">Cinq chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-614">Five digits</span></span> 
- <span data-ttu-id="d8d84-615">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="d8d84-615">A hyphen</span></span> 
- <span data-ttu-id="d8d84-616">Trois chiffres ou</span><span class="sxs-lookup"><span data-stu-id="d8d84-616">Three digits OR</span></span>
- <span data-ttu-id="d8d84-617">Un zéro « 0 » </span><span class="sxs-lookup"><span data-stu-id="d8d84-617">A zero "0"</span></span> 
- <span data-ttu-id="d8d84-618">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-618">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-619">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-619">Checksum</span></span>

<span data-ttu-id="d8d84-620">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-620">No</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-621">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-621">Definition</span></span>

<span data-ttu-id="d8d84-622">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-622">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-623">L’expression régulière Regex_canada_bank_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-623">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-624">Un mot clé figurant dans la liste Keyword_canada_bank_account_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-624">A keyword from Keyword_canada_bank_account_number is found.</span></span>
- <span data-ttu-id="d8d84-625">L’expression régulière Regex_canada_bank_account_transit_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-625">The regular expression Regex_canada_bank_account_transit_number finds content that matches the pattern.</span></span>

<span data-ttu-id="d8d84-626">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-626">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-627">L’expression régulière Regex_canada_bank_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-627">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-628">Un mot clé figurant dans la liste Keyword_canada_bank_account_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-628">A keyword from Keyword_canada_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-629">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-629">Keywords</span></span>

#### <a name="keywordcanadabankaccountnumber"></a><span data-ttu-id="d8d84-630">Keyword_canada_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="d8d84-630">Keyword_canada_bank_account_number</span></span>

- <span data-ttu-id="d8d84-631">obligations d’épargne du Canada</span><span class="sxs-lookup"><span data-stu-id="d8d84-631">canada savings bonds</span></span>
- <span data-ttu-id="d8d84-632">
agence du revenu du Canada</span><span class="sxs-lookup"><span data-stu-id="d8d84-632">canada revenue agency</span></span>
- <span data-ttu-id="d8d84-633">
institution financière du Canada</span><span class="sxs-lookup"><span data-stu-id="d8d84-633">canadian financial institution</span></span>
- <span data-ttu-id="d8d84-634">
formulaire de dépôt direct</span><span class="sxs-lookup"><span data-stu-id="d8d84-634">direct deposit form</span></span>
- <span data-ttu-id="d8d84-635">
citoyen canadien</span><span class="sxs-lookup"><span data-stu-id="d8d84-635">canadian citizen</span></span>
- <span data-ttu-id="d8d84-636">
représentant légal</span><span class="sxs-lookup"><span data-stu-id="d8d84-636">legal representative</span></span>
- <span data-ttu-id="d8d84-637">
notaire</span><span class="sxs-lookup"><span data-stu-id="d8d84-637">notary public</span></span>
- <span data-ttu-id="d8d84-638">
commissaire à l’assermentation</span><span class="sxs-lookup"><span data-stu-id="d8d84-638">commissioner for oaths</span></span>
- <span data-ttu-id="d8d84-639">
prestation pour la garde d’enfants</span><span class="sxs-lookup"><span data-stu-id="d8d84-639">child care benefit</span></span>
- <span data-ttu-id="d8d84-640">
prestation universelle pour la garde d’enfants</span><span class="sxs-lookup"><span data-stu-id="d8d84-640">universal child care</span></span>
- <span data-ttu-id="d8d84-641">
prestation fiscale canadienne pour enfants</span><span class="sxs-lookup"><span data-stu-id="d8d84-641">canada child tax benefit</span></span>
- <span data-ttu-id="d8d84-642">
prestation fiscale pour le revenu gagné</span><span class="sxs-lookup"><span data-stu-id="d8d84-642">income tax benefit</span></span>
- <span data-ttu-id="d8d84-643">
taxe de vente harmonisée</span><span class="sxs-lookup"><span data-stu-id="d8d84-643">harmonized sales tax</span></span>
- <span data-ttu-id="d8d84-644">numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="d8d84-644">social insurance number</span></span>
- <span data-ttu-id="d8d84-645">
remboursement d’impôt</span><span class="sxs-lookup"><span data-stu-id="d8d84-645">income tax refund</span></span>
- <span data-ttu-id="d8d84-646">
prestation fiscale pour enfants</span><span class="sxs-lookup"><span data-stu-id="d8d84-646">child tax benefit</span></span>
- <span data-ttu-id="d8d84-647">
paiements aux territoires</span><span class="sxs-lookup"><span data-stu-id="d8d84-647">territorial payments</span></span>
- <span data-ttu-id="d8d84-648">
numéro d’institution</span><span class="sxs-lookup"><span data-stu-id="d8d84-648">institution number</span></span>
- <span data-ttu-id="d8d84-649">
demande de dépôt</span><span class="sxs-lookup"><span data-stu-id="d8d84-649">deposit request</span></span>
- <span data-ttu-id="d8d84-650">
informations bancaires</span><span class="sxs-lookup"><span data-stu-id="d8d84-650">banking information</span></span>
- <span data-ttu-id="d8d84-651">

dépôt direct</span><span class="sxs-lookup"><span data-stu-id="d8d84-651">direct deposit</span></span>
   
## <a name="canada-drivers-license-number"></a><span data-ttu-id="d8d84-652">Numéro de permis de conduire Canada</span><span class="sxs-lookup"><span data-stu-id="d8d84-652">Canada Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-653">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-653">Format</span></span>

<span data-ttu-id="d8d84-654">Varie selon la province</span><span class="sxs-lookup"><span data-stu-id="d8d84-654">Varies by province</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-655">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-655">Pattern</span></span>

<span data-ttu-id="d8d84-656">Plusieurs modèles pour les différentes provinces : Alberta, Colombie-Britannique, Manitoba, Nouveau-Brunswick, Terre-Neuve-et-Labrador, Nouvelle-Écosse, Ontario, Île-du-Prince-Édouard, Québec et Saskatchewan</span><span class="sxs-lookup"><span data-stu-id="d8d84-656">Various patterns covering Alberta, British Columbia, Manitoba, New Brunswick, Newfoundland/Labrador, Nova Scotia, Ontario, Prince Edward Island, Quebec, and Saskatchewan</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-657">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-657">Checksum</span></span>

<span data-ttu-id="d8d84-658">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-658">No</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-659">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-659">Definition</span></span>

<span data-ttu-id="d8d84-660">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-660">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-661">La fonction Func_[province_name]_drivers_license_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-661">The function Func_[province_name]_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-662">Un mot clé figurant dans la liste Keyword_[province_name]_drivers_license_name est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-662">A keyword from Keyword_[province_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="d8d84-663">Un mot clé figurant dans la liste Keyword_canada_drivers_license est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-663">A keyword from Keyword_canada_drivers_license is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-664">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-664">Keywords</span></span>

#### <a name="keywordprovincenamedriverslicensename"></a><span data-ttu-id="d8d84-665">Keyword_[province_name]_drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="d8d84-665">Keyword_[province_name]_drivers_license_name</span></span>

- <span data-ttu-id="d8d84-666">L’abréviation de la province, par exemple AB</span><span class="sxs-lookup"><span data-stu-id="d8d84-666">The province abbreviation, for example AB</span></span>
- <span data-ttu-id="d8d84-667">
Le nom de la province, par exemple Alberta</span><span class="sxs-lookup"><span data-stu-id="d8d84-667">The province name, for example Alberta</span></span>

#### <a name="keywordcanadadriverslicense"></a><span data-ttu-id="d8d84-668">Keyword_canada_drivers_license</span><span class="sxs-lookup"><span data-stu-id="d8d84-668">Keyword_canada_drivers_license</span></span>

- <span data-ttu-id="d8d84-669">PC</span><span class="sxs-lookup"><span data-stu-id="d8d84-669">DL</span></span>
- <span data-ttu-id="d8d84-670">PC</span><span class="sxs-lookup"><span data-stu-id="d8d84-670">DLS</span></span>
- <span data-ttu-id="d8d84-671">CDL</span><span class="sxs-lookup"><span data-stu-id="d8d84-671">CDL</span></span>
- <span data-ttu-id="d8d84-672">SYSTÈMES CDL</span><span class="sxs-lookup"><span data-stu-id="d8d84-672">CDLS</span></span>
- <span data-ttu-id="d8d84-673">DriverLic</span><span class="sxs-lookup"><span data-stu-id="d8d84-673">DriverLic</span></span>
- <span data-ttu-id="d8d84-674">DriverLics</span><span class="sxs-lookup"><span data-stu-id="d8d84-674">DriverLics</span></span>
- <span data-ttu-id="d8d84-675">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="d8d84-675">DriverLicense</span></span>
- <span data-ttu-id="d8d84-676">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="d8d84-676">DriverLicenses</span></span>
- <span data-ttu-id="d8d84-677">DriverLicence</span><span class="sxs-lookup"><span data-stu-id="d8d84-677">DriverLicence</span></span>
- <span data-ttu-id="d8d84-678">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="d8d84-678">DriverLicences</span></span>
- <span data-ttu-id="d8d84-679">Lic pilote</span><span class="sxs-lookup"><span data-stu-id="d8d84-679">Driver Lic</span></span>
- <span data-ttu-id="d8d84-680">Pilote Lics</span><span class="sxs-lookup"><span data-stu-id="d8d84-680">Driver Lics</span></span>
- <span data-ttu-id="d8d84-681">Conduire</span><span class="sxs-lookup"><span data-stu-id="d8d84-681">Driver License</span></span>
- <span data-ttu-id="d8d84-682">Licences de pilote</span><span class="sxs-lookup"><span data-stu-id="d8d84-682">Driver Licenses</span></span>
- <span data-ttu-id="d8d84-683">Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-683">Driver Licence</span></span>
- <span data-ttu-id="d8d84-684">Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-684">Driver Licences</span></span>
- <span data-ttu-id="d8d84-685">DriversLic</span><span class="sxs-lookup"><span data-stu-id="d8d84-685">DriversLic</span></span>
- <span data-ttu-id="d8d84-686">DriversLics</span><span class="sxs-lookup"><span data-stu-id="d8d84-686">DriversLics</span></span>
- <span data-ttu-id="d8d84-687">DriversLicence</span><span class="sxs-lookup"><span data-stu-id="d8d84-687">DriversLicence</span></span>
- <span data-ttu-id="d8d84-688">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="d8d84-688">DriversLicences</span></span>
- <span data-ttu-id="d8d84-689">Conduire</span><span class="sxs-lookup"><span data-stu-id="d8d84-689">DriversLicense</span></span>
- <span data-ttu-id="d8d84-690">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="d8d84-690">DriversLicenses</span></span>
- <span data-ttu-id="d8d84-691">Lic pilotes</span><span class="sxs-lookup"><span data-stu-id="d8d84-691">Drivers Lic</span></span>
- <span data-ttu-id="d8d84-692">Lics pilotes</span><span class="sxs-lookup"><span data-stu-id="d8d84-692">Drivers Lics</span></span>
- <span data-ttu-id="d8d84-693">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="d8d84-693">Drivers License</span></span>
- <span data-ttu-id="d8d84-694">Licences de pilotes</span><span class="sxs-lookup"><span data-stu-id="d8d84-694">Drivers Licenses</span></span>
- <span data-ttu-id="d8d84-695">Certificat de pilotes</span><span class="sxs-lookup"><span data-stu-id="d8d84-695">Drivers Licence</span></span>
- <span data-ttu-id="d8d84-696">Certificats de pilotes</span><span class="sxs-lookup"><span data-stu-id="d8d84-696">Drivers Licences</span></span>
- <span data-ttu-id="d8d84-697">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="d8d84-697">Driver'Lic</span></span>
- <span data-ttu-id="d8d84-698">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="d8d84-698">Driver'Lics</span></span>
- <span data-ttu-id="d8d84-699">Driver'License</span><span class="sxs-lookup"><span data-stu-id="d8d84-699">Driver'License</span></span>
- <span data-ttu-id="d8d84-700">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="d8d84-700">Driver'Licenses</span></span>
- <span data-ttu-id="d8d84-701">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="d8d84-701">Driver'Licence</span></span>
- <span data-ttu-id="d8d84-702">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="d8d84-702">Driver'Licences</span></span>
- <span data-ttu-id="d8d84-703">Pilote ' Lic</span><span class="sxs-lookup"><span data-stu-id="d8d84-703">Driver' Lic</span></span>
- <span data-ttu-id="d8d84-704">Pilote ' Lics</span><span class="sxs-lookup"><span data-stu-id="d8d84-704">Driver' Lics</span></span>
- <span data-ttu-id="d8d84-705">Pilote ' licence</span><span class="sxs-lookup"><span data-stu-id="d8d84-705">Driver' License</span></span>
- <span data-ttu-id="d8d84-706">Pilote ' licences</span><span class="sxs-lookup"><span data-stu-id="d8d84-706">Driver' Licenses</span></span>
- <span data-ttu-id="d8d84-707">Pilote ' certificat</span><span class="sxs-lookup"><span data-stu-id="d8d84-707">Driver' Licence</span></span>
- <span data-ttu-id="d8d84-708">Pilote « certificats</span><span class="sxs-lookup"><span data-stu-id="d8d84-708">Driver' Licences</span></span>
- <span data-ttu-id="d8d84-709">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="d8d84-709">Driver'sLic</span></span>
- <span data-ttu-id="d8d84-710">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="d8d84-710">Driver'sLics</span></span>
- <span data-ttu-id="d8d84-711">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="d8d84-711">Driver'sLicense</span></span>
- <span data-ttu-id="d8d84-712">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="d8d84-712">Driver'sLicenses</span></span>
- <span data-ttu-id="d8d84-713">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="d8d84-713">Driver'sLicence</span></span>
- <span data-ttu-id="d8d84-714">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="d8d84-714">Driver'sLicences</span></span>
- <span data-ttu-id="d8d84-715">Lic du pilote</span><span class="sxs-lookup"><span data-stu-id="d8d84-715">Driver's Lic</span></span>
- <span data-ttu-id="d8d84-716">Lics permis de conduire</span><span class="sxs-lookup"><span data-stu-id="d8d84-716">Driver's Lics</span></span>
- <span data-ttu-id="d8d84-717">Conduire permis de</span><span class="sxs-lookup"><span data-stu-id="d8d84-717">Driver's License</span></span>
- <span data-ttu-id="d8d84-718">Conduire permis de</span><span class="sxs-lookup"><span data-stu-id="d8d84-718">Driver's Licenses</span></span>
- <span data-ttu-id="d8d84-719">Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-719">Driver's Licence</span></span>
- <span data-ttu-id="d8d84-720">Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-720">Driver's Licences</span></span>
- <span data-ttu-id="d8d84-721">Permis de Conduire</span><span class="sxs-lookup"><span data-stu-id="d8d84-721">Permis de Conduire</span></span>
- <span data-ttu-id="d8d84-722">id</span><span class="sxs-lookup"><span data-stu-id="d8d84-722">id</span></span>
- <span data-ttu-id="d8d84-723">ID</span><span class="sxs-lookup"><span data-stu-id="d8d84-723">ids</span></span>
- <span data-ttu-id="d8d84-724">
numéro carte d’identification</span><span class="sxs-lookup"><span data-stu-id="d8d84-724">idcard number</span></span>
- <span data-ttu-id="d8d84-725">
numéros carte d’identification</span><span class="sxs-lookup"><span data-stu-id="d8d84-725">idcard numbers</span></span>
- <span data-ttu-id="d8d84-726">
# carte d’identification</span><span class="sxs-lookup"><span data-stu-id="d8d84-726">idcard #</span></span>
- <span data-ttu-id="d8d84-727">
# carte d’identification</span><span class="sxs-lookup"><span data-stu-id="d8d84-727">idcard #s</span></span>
- <span data-ttu-id="d8d84-728">carte idcard</span><span class="sxs-lookup"><span data-stu-id="d8d84-728">idcard card</span></span>
- <span data-ttu-id="d8d84-729">cartes idcard</span><span class="sxs-lookup"><span data-stu-id="d8d84-729">idcard cards</span></span>
- <span data-ttu-id="d8d84-730">idcard</span><span class="sxs-lookup"><span data-stu-id="d8d84-730">idcard</span></span>
- <span data-ttu-id="d8d84-731">numéro d’identification
</span><span class="sxs-lookup"><span data-stu-id="d8d84-731">identification number</span></span>
- <span data-ttu-id="d8d84-732">numéros d’identification
</span><span class="sxs-lookup"><span data-stu-id="d8d84-732">identification numbers</span></span>
- <span data-ttu-id="d8d84-733"># identification
</span><span class="sxs-lookup"><span data-stu-id="d8d84-733">identification #</span></span>
- <span data-ttu-id="d8d84-734">
# identification</span><span class="sxs-lookup"><span data-stu-id="d8d84-734">identification #s</span></span>
- <span data-ttu-id="d8d84-735">carte d’identification</span><span class="sxs-lookup"><span data-stu-id="d8d84-735">identification card</span></span>
- <span data-ttu-id="d8d84-736">cartes d’identification</span><span class="sxs-lookup"><span data-stu-id="d8d84-736">identification cards</span></span>
- <span data-ttu-id="d8d84-737">
identification
</span><span class="sxs-lookup"><span data-stu-id="d8d84-737">identification</span></span> 
- <span data-ttu-id="d8d84-738"># PC</span><span class="sxs-lookup"><span data-stu-id="d8d84-738">DL#</span></span>
- <span data-ttu-id="d8d84-739">
# PC
</span><span class="sxs-lookup"><span data-stu-id="d8d84-739">DLS#</span></span> 
- <span data-ttu-id="d8d84-740"># PCD
</span><span class="sxs-lookup"><span data-stu-id="d8d84-740">CDL#</span></span> 
- <span data-ttu-id="d8d84-741"># PCD
</span><span class="sxs-lookup"><span data-stu-id="d8d84-741">CDLS#</span></span> 
- <span data-ttu-id="d8d84-742">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="d8d84-742">DriverLic#</span></span> 
- <span data-ttu-id="d8d84-743">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="d8d84-743">DriverLics#</span></span> 
- <span data-ttu-id="d8d84-744">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="d8d84-744">DriverLicense#</span></span> 
- <span data-ttu-id="d8d84-745">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="d8d84-745">DriverLicenses#</span></span> 
- <span data-ttu-id="d8d84-746">DriverLicence #</span><span class="sxs-lookup"><span data-stu-id="d8d84-746">DriverLicence#</span></span> 
- <span data-ttu-id="d8d84-747">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="d8d84-747">DriverLicences#</span></span> 
- <span data-ttu-id="d8d84-748">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="d8d84-748">Driver Lic#</span></span>
- <span data-ttu-id="d8d84-749">
#Permis conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-749">Driver Lics#</span></span> 
- <span data-ttu-id="d8d84-750">Pilote licence #</span><span class="sxs-lookup"><span data-stu-id="d8d84-750">Driver License#</span></span> 
- <span data-ttu-id="d8d84-751">Licences de pilote #</span><span class="sxs-lookup"><span data-stu-id="d8d84-751">Driver Licenses#</span></span> 
- <span data-ttu-id="d8d84-752">Pilote licence #</span><span class="sxs-lookup"><span data-stu-id="d8d84-752">Driver License#</span></span> 
- <span data-ttu-id="d8d84-753">Pilote certificats #</span><span class="sxs-lookup"><span data-stu-id="d8d84-753">Driver Licences#</span></span> 
- <span data-ttu-id="d8d84-754">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="d8d84-754">DriversLic#</span></span> 
- <span data-ttu-id="d8d84-755">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="d8d84-755">DriversLics#</span></span> 
- <span data-ttu-id="d8d84-756">Conduire #</span><span class="sxs-lookup"><span data-stu-id="d8d84-756">DriversLicense#</span></span> 
- <span data-ttu-id="d8d84-757">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="d8d84-757">DriversLicenses#</span></span> 
- <span data-ttu-id="d8d84-758">DriversLicence #</span><span class="sxs-lookup"><span data-stu-id="d8d84-758">DriversLicence#</span></span> 
- <span data-ttu-id="d8d84-759">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="d8d84-759">DriversLicences#</span></span> 
- <span data-ttu-id="d8d84-760">Pilotes Lic #</span><span class="sxs-lookup"><span data-stu-id="d8d84-760">Drivers Lic#</span></span> 
- <span data-ttu-id="d8d84-761">Pilotes Lics #</span><span class="sxs-lookup"><span data-stu-id="d8d84-761">Drivers Lics#</span></span> 
- <span data-ttu-id="d8d84-762">Licence pilotes #</span><span class="sxs-lookup"><span data-stu-id="d8d84-762">Drivers License#</span></span> 
- <span data-ttu-id="d8d84-763">Licences pilotes #</span><span class="sxs-lookup"><span data-stu-id="d8d84-763">Drivers Licenses#</span></span> 
- <span data-ttu-id="d8d84-764">Licence pilotes #</span><span class="sxs-lookup"><span data-stu-id="d8d84-764">Drivers Licence#</span></span> 
- <span data-ttu-id="d8d84-765">Certificats pilotes #</span><span class="sxs-lookup"><span data-stu-id="d8d84-765">Drivers Licences#</span></span> 
- <span data-ttu-id="d8d84-766">#Permisconduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-766">Driver'Lic#</span></span> 
- <span data-ttu-id="d8d84-767">#Permisconduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-767">Driver'Lics#</span></span> 
- <span data-ttu-id="d8d84-768">#Permisdeconduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-768">Driver'License#</span></span> 
- <span data-ttu-id="d8d84-769">#Permisdeconduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-769">Driver'Licenses#</span></span> 
- <span data-ttu-id="d8d84-770">#Permisdeconduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-770">Driver'Licence#</span></span> 
- <span data-ttu-id="d8d84-771">#Permisdeconduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-771">Driver'Licences#</span></span> 
- <span data-ttu-id="d8d84-772">#Permis conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-772">Driver' Lic#</span></span> 
- <span data-ttu-id="d8d84-773">#Permis conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-773">Driver' Lics#</span></span> 
- <span data-ttu-id="d8d84-774">#Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-774">Driver' License#</span></span> 
- <span data-ttu-id="d8d84-775">#Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-775">Driver' Licenses#</span></span> 
- <span data-ttu-id="d8d84-776">Pilote ' certificat #</span><span class="sxs-lookup"><span data-stu-id="d8d84-776">Driver' Licence#</span></span> 
- <span data-ttu-id="d8d84-777">Pilote « certificats #</span><span class="sxs-lookup"><span data-stu-id="d8d84-777">Driver' Licences#</span></span> 
- <span data-ttu-id="d8d84-778">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="d8d84-778">Driver'sLic#</span></span> 
- <span data-ttu-id="d8d84-779">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="d8d84-779">Driver'sLics#</span></span> 
- <span data-ttu-id="d8d84-780">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="d8d84-780">Driver'sLicense#</span></span> 
- <span data-ttu-id="d8d84-781">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="d8d84-781">Driver'sLicenses#</span></span> 
- <span data-ttu-id="d8d84-782">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="d8d84-782">Driver'sLicence#</span></span> 
- <span data-ttu-id="d8d84-783">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="d8d84-783">Driver'sLicences#</span></span> 
- <span data-ttu-id="d8d84-784">#Permisconduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-784">Driver's Lic#</span></span> 
- <span data-ttu-id="d8d84-785">#Permisconduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-785">Driver's Lics#</span></span> 
- <span data-ttu-id="d8d84-786">#Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-786">Driver's License#</span></span> 
- <span data-ttu-id="d8d84-787">#Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-787">Driver's Licenses#</span></span> 
- <span data-ttu-id="d8d84-788">Certificat de # permis de conduire</span><span class="sxs-lookup"><span data-stu-id="d8d84-788">Driver's Licence#</span></span> 
- <span data-ttu-id="d8d84-789">Certificats de # permis de conduire</span><span class="sxs-lookup"><span data-stu-id="d8d84-789">Driver's Licences#</span></span> 
- <span data-ttu-id="d8d84-790">Permis de Conduire #</span><span class="sxs-lookup"><span data-stu-id="d8d84-790">Permis de Conduire#</span></span> 
- <span data-ttu-id="d8d84-791">numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="d8d84-791">id#</span></span> 
- <span data-ttu-id="d8d84-792">ID #</span><span class="sxs-lookup"><span data-stu-id="d8d84-792">ids#</span></span> 
- <span data-ttu-id="d8d84-793">#carte carte d’identification
</span><span class="sxs-lookup"><span data-stu-id="d8d84-793">idcard card#</span></span> 
- <span data-ttu-id="d8d84-794">#cartes carte d’identification
</span><span class="sxs-lookup"><span data-stu-id="d8d84-794">idcard cards#</span></span> 
- <span data-ttu-id="d8d84-795">#carte d’identification
</span><span class="sxs-lookup"><span data-stu-id="d8d84-795">idcard#</span></span> 
- <span data-ttu-id="d8d84-796">#carte d’identification
</span><span class="sxs-lookup"><span data-stu-id="d8d84-796">identification card#</span></span> 
- <span data-ttu-id="d8d84-797">#cartes d’identification
</span><span class="sxs-lookup"><span data-stu-id="d8d84-797">identification cards#</span></span> 
- <span data-ttu-id="d8d84-798">#identification
</span><span class="sxs-lookup"><span data-stu-id="d8d84-798">identification#</span></span> 
   
## <a name="canada-health-service-number"></a><span data-ttu-id="d8d84-799">Numéro de service de santé Canada</span><span class="sxs-lookup"><span data-stu-id="d8d84-799">Canada Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-800">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-800">Format</span></span>

<span data-ttu-id="d8d84-801">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-801">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-802">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-802">Pattern</span></span>

<span data-ttu-id="d8d84-803">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-803">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-804">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-804">Checksum</span></span>

<span data-ttu-id="d8d84-805">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-805">No</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-806">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-806">Definition</span></span>

<span data-ttu-id="d8d84-807">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-807">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-808">L’expression régulière Regex_canada_health_service_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-808">The regular expression Regex_canada_health_service_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-809">Un mot clé figurant dans la liste Keyword_canada_health_service_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-809">A keyword from Keyword_canada_health_service_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-810">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-810">Keywords</span></span>

#### <a name="keywordcanadahealthservicenumber"></a><span data-ttu-id="d8d84-811">Keyword_canada_health_service_number</span><span class="sxs-lookup"><span data-stu-id="d8d84-811">Keyword_canada_health_service_number</span></span>

- <span data-ttu-id="d8d84-812">numéro d’assurance-maladie</span><span class="sxs-lookup"><span data-stu-id="d8d84-812">personal health number</span></span>
- <span data-ttu-id="d8d84-813">
informations sur le patient</span><span class="sxs-lookup"><span data-stu-id="d8d84-813">patient information</span></span>
- <span data-ttu-id="d8d84-814">services de santé</span><span class="sxs-lookup"><span data-stu-id="d8d84-814">health services</span></span>
- <span data-ttu-id="d8d84-815">
services spécialisés</span><span class="sxs-lookup"><span data-stu-id="d8d84-815">speciality services</span></span>
- <span data-ttu-id="d8d84-816">
accident automobile</span><span class="sxs-lookup"><span data-stu-id="d8d84-816">automobile accident</span></span>
- <span data-ttu-id="d8d84-817">
hôpital pour malades</span><span class="sxs-lookup"><span data-stu-id="d8d84-817">patient hospital</span></span>
- <span data-ttu-id="d8d84-818">
psychiatre</span><span class="sxs-lookup"><span data-stu-id="d8d84-818">psychiatrist</span></span>
- <span data-ttu-id="d8d84-819">
indemnisation des salariés</span><span class="sxs-lookup"><span data-stu-id="d8d84-819">workers compensation</span></span>
- <span data-ttu-id="d8d84-820">
handicap</span><span class="sxs-lookup"><span data-stu-id="d8d84-820">disability</span></span>
      
## <a name="canada-passport-number"></a><span data-ttu-id="d8d84-821">Numéro de passeport Canada</span><span class="sxs-lookup"><span data-stu-id="d8d84-821">Canada Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-822">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-822">Format</span></span>

<span data-ttu-id="d8d84-823">Deux lettres majuscules suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-823">Two uppercase letters followed by six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-824">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-824">Pattern</span></span>

<span data-ttu-id="d8d84-825">Deux lettres majuscules suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-825">Two uppercase letters followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-826">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-826">Checksum</span></span>

<span data-ttu-id="d8d84-827">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-827">No</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-828">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-828">Definition</span></span>

<span data-ttu-id="d8d84-829">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-829">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-830">L’expression régulière Regex_canada_passport_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-830">The regular expression Regex_canada_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-831">Un mot clé à partir de Keyword_canada_passport_number ou Keyword_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-831">A keyword from Keyword_canada_passport_number or Keyword_passport is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-832">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-832">Keywords</span></span>

#### <a name="keywordcanadapassportnumber"></a><span data-ttu-id="d8d84-833">Keyword_canada_passport_number</span><span class="sxs-lookup"><span data-stu-id="d8d84-833">Keyword_canada_passport_number</span></span>

- <span data-ttu-id="d8d84-834">citoyenneté canadienne</span><span class="sxs-lookup"><span data-stu-id="d8d84-834">canadian citizenship</span></span>
- <span data-ttu-id="d8d84-835">
passeport canadien</span><span class="sxs-lookup"><span data-stu-id="d8d84-835">canadian passport</span></span>
- <span data-ttu-id="d8d84-836">
demande de passeport</span><span class="sxs-lookup"><span data-stu-id="d8d84-836">passport application</span></span>
- <span data-ttu-id="d8d84-837">
photos pour passeport</span><span class="sxs-lookup"><span data-stu-id="d8d84-837">passport photos</span></span>
- <span data-ttu-id="d8d84-838">
traducteur agréé</span><span class="sxs-lookup"><span data-stu-id="d8d84-838">certified translator</span></span>
- <span data-ttu-id="d8d84-839">
citoyens canadiens</span><span class="sxs-lookup"><span data-stu-id="d8d84-839">canadian citizens</span></span>
- <span data-ttu-id="d8d84-840">
temps de traitement</span><span class="sxs-lookup"><span data-stu-id="d8d84-840">processing times</span></span>
- <span data-ttu-id="d8d84-841">

demande de renouvellement</span><span class="sxs-lookup"><span data-stu-id="d8d84-841">renewal application</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="d8d84-842">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="d8d84-842">Keyword_passport</span></span>

- <span data-ttu-id="d8d84-843">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8d84-843">Passport Number</span></span>
- <span data-ttu-id="d8d84-844">
N° de passeport</span><span class="sxs-lookup"><span data-stu-id="d8d84-844">Passport No</span></span>
- <span data-ttu-id="d8d84-845"># Passeport
</span><span class="sxs-lookup"><span data-stu-id="d8d84-845">Passport #</span></span>
- <span data-ttu-id="d8d84-846">#Passeport
</span><span class="sxs-lookup"><span data-stu-id="d8d84-846">Passport#</span></span>
- <span data-ttu-id="d8d84-847">IDPassport</span><span class="sxs-lookup"><span data-stu-id="d8d84-847">PassportID</span></span>
- <span data-ttu-id="d8d84-848">n° passeport
</span><span class="sxs-lookup"><span data-stu-id="d8d84-848">Passportno</span></span>
- <span data-ttu-id="d8d84-849">numéropasseport
</span><span class="sxs-lookup"><span data-stu-id="d8d84-849">passportnumber</span></span>
- <span data-ttu-id="d8d84-850">パスポート</span><span class="sxs-lookup"><span data-stu-id="d8d84-850">パスポート</span></span>
- <span data-ttu-id="d8d84-851">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="d8d84-851">パスポート番号</span></span>
- <span data-ttu-id="d8d84-852">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="d8d84-852">パスポートのNum</span></span>
- <span data-ttu-id="d8d84-853">パスポート＃
</span><span class="sxs-lookup"><span data-stu-id="d8d84-853">パスポート＃</span></span>
- <span data-ttu-id="d8d84-854">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8d84-854">Numéro de passeport</span></span>
- <span data-ttu-id="d8d84-855">
Passeport n°</span><span class="sxs-lookup"><span data-stu-id="d8d84-855">Passeport n °</span></span>
- <span data-ttu-id="d8d84-856">Passeport numéro
</span><span class="sxs-lookup"><span data-stu-id="d8d84-856">Passeport Non</span></span>
- <span data-ttu-id="d8d84-857"># Passeport
</span><span class="sxs-lookup"><span data-stu-id="d8d84-857">Passeport #</span></span>
- <span data-ttu-id="d8d84-858">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="d8d84-858">Passeport#</span></span>
- <span data-ttu-id="d8d84-859">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="d8d84-859">PasseportNon</span></span>
- <span data-ttu-id="d8d84-860">

Passeportn °</span><span class="sxs-lookup"><span data-stu-id="d8d84-860">Passeportn °</span></span>
   
## <a name="canada-personal-health-identification-number-phin"></a><span data-ttu-id="d8d84-861">NIMP (numéro d'identification médicale personnel) Canada</span><span class="sxs-lookup"><span data-stu-id="d8d84-861">Canada Personal Health Identification Number (PHIN)</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-862">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-862">Format</span></span>

<span data-ttu-id="d8d84-863">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-863">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-864">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-864">Pattern</span></span>

<span data-ttu-id="d8d84-865">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-865">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-866">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-866">Checksum</span></span>

<span data-ttu-id="d8d84-867">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-867">No</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-868">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-868">Definition</span></span>

<span data-ttu-id="d8d84-p104">Une stratégie DLP est convaincu que ce type d’informations sensibles a été détecté à 75 % if, au sein d’une proximité de 300 caractères : l’expression régulière Regex_canada_phin recherche de contenu qui correspond au modèle. Contient des mots clés au moins deux des Keyword_canada_phin Keyword_canada_provinces...</span><span class="sxs-lookup"><span data-stu-id="d8d84-p104">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_canada_phin finds content that matches the pattern. At least two keywords from Keyword_canada_phin or Keyword_canada_provinces are found..</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-871">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-871">Keywords</span></span>

#### <a name="keywordcanadaphin"></a><span data-ttu-id="d8d84-872">Keyword_canada_phin</span><span class="sxs-lookup"><span data-stu-id="d8d84-872">Keyword_canada_phin</span></span>

- <span data-ttu-id="d8d84-873">numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="d8d84-873">social insurance number</span></span>
- <span data-ttu-id="d8d84-874">
loi sur les renseignements médicaux</span><span class="sxs-lookup"><span data-stu-id="d8d84-874">health information act</span></span>
- <span data-ttu-id="d8d84-875">
renseignements relatifs à l’impôt sur le revenu</span><span class="sxs-lookup"><span data-stu-id="d8d84-875">income tax information</span></span>
- <span data-ttu-id="d8d84-876">
santé Manitoba</span><span class="sxs-lookup"><span data-stu-id="d8d84-876">manitoba health</span></span>
- <span data-ttu-id="d8d84-877">
enregistrement aux services de santé</span><span class="sxs-lookup"><span data-stu-id="d8d84-877">health registration</span></span>
- <span data-ttu-id="d8d84-878">
achats de médicaments sur ordonnance</span><span class="sxs-lookup"><span data-stu-id="d8d84-878">prescription purchases</span></span>
- <span data-ttu-id="d8d84-879">
admissibilité aux prestations</span><span class="sxs-lookup"><span data-stu-id="d8d84-879">benefit eligibility</span></span>
- <span data-ttu-id="d8d84-880">
santé personnelle</span><span class="sxs-lookup"><span data-stu-id="d8d84-880">personal health</span></span>
- <span data-ttu-id="d8d84-881">
procuration</span><span class="sxs-lookup"><span data-stu-id="d8d84-881">power of attorney</span></span>
- <span data-ttu-id="d8d84-882">
numéro d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="d8d84-882">registration number</span></span>
- <span data-ttu-id="d8d84-883">numéro d’assurance-maladie</span><span class="sxs-lookup"><span data-stu-id="d8d84-883">personal health number</span></span>
- <span data-ttu-id="d8d84-884">
recommandation par le médecin</span><span class="sxs-lookup"><span data-stu-id="d8d84-884">practitioner referral</span></span>
- <span data-ttu-id="d8d84-885">
professionnel de bien-être</span><span class="sxs-lookup"><span data-stu-id="d8d84-885">wellness professional</span></span>
- <span data-ttu-id="d8d84-886">
orientation d’un patient</span><span class="sxs-lookup"><span data-stu-id="d8d84-886">patient referral</span></span>
- <span data-ttu-id="d8d84-887">

santé et bien-être</span><span class="sxs-lookup"><span data-stu-id="d8d84-887">health and wellness</span></span>

#### <a name="keywordcanadaprovinces"></a><span data-ttu-id="d8d84-888">Keyword_canada_provinces</span><span class="sxs-lookup"><span data-stu-id="d8d84-888">Keyword_canada_provinces</span></span>

- <span data-ttu-id="d8d84-889">Nunavut</span><span class="sxs-lookup"><span data-stu-id="d8d84-889">Nunavut</span></span>
- <span data-ttu-id="d8d84-890">
Québec</span><span class="sxs-lookup"><span data-stu-id="d8d84-890">Quebec</span></span>
- <span data-ttu-id="d8d84-891">
Territoires du Nord-Ouest</span><span class="sxs-lookup"><span data-stu-id="d8d84-891">Northwest Territories</span></span>
- <span data-ttu-id="d8d84-892">
Ontario</span><span class="sxs-lookup"><span data-stu-id="d8d84-892">Ontario</span></span>
- <span data-ttu-id="d8d84-893">
Colombie-britannique</span><span class="sxs-lookup"><span data-stu-id="d8d84-893">British Columbia</span></span>
- <span data-ttu-id="d8d84-894">
Alberta</span><span class="sxs-lookup"><span data-stu-id="d8d84-894">Alberta</span></span>
- <span data-ttu-id="d8d84-895">
Saskatchewan</span><span class="sxs-lookup"><span data-stu-id="d8d84-895">Saskatchewan</span></span>
- <span data-ttu-id="d8d84-896">
Manitoba</span><span class="sxs-lookup"><span data-stu-id="d8d84-896">Manitoba</span></span>
- <span data-ttu-id="d8d84-897">
Yukon</span><span class="sxs-lookup"><span data-stu-id="d8d84-897">Yukon</span></span>
- <span data-ttu-id="d8d84-898">
Terre-Neuve-et-Labrador</span><span class="sxs-lookup"><span data-stu-id="d8d84-898">Newfoundland and Labrador</span></span>
- <span data-ttu-id="d8d84-899">
Nouveau-Brunswick</span><span class="sxs-lookup"><span data-stu-id="d8d84-899">New Brunswick</span></span>
- <span data-ttu-id="d8d84-900">
Nouvelle-Écosse</span><span class="sxs-lookup"><span data-stu-id="d8d84-900">Nova Scotia</span></span>
- <span data-ttu-id="d8d84-901">
Île-du-Prince-Édouard</span><span class="sxs-lookup"><span data-stu-id="d8d84-901">Prince Edward Island</span></span>
- <span data-ttu-id="d8d84-902">Canada</span><span class="sxs-lookup"><span data-stu-id="d8d84-902">Canada</span></span>
   
## <a name="canada-social-insurance-number"></a><span data-ttu-id="d8d84-903">Numéro d'assurance sociale Canada</span><span class="sxs-lookup"><span data-stu-id="d8d84-903">Canada Social Insurance Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-904">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-904">Format</span></span>

<span data-ttu-id="d8d84-905">Neuf chiffres avec éventuellement des traits d’union ou des espaces</span><span class="sxs-lookup"><span data-stu-id="d8d84-905">Nine digits with optional hyphens or spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-906">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-906">Pattern</span></span>

<span data-ttu-id="d8d84-907">Mis en forme :</span><span class="sxs-lookup"><span data-stu-id="d8d84-907">Formatted:</span></span>
- <span data-ttu-id="d8d84-908">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-908">Three digits</span></span> 
- <span data-ttu-id="d8d84-909">Un trait d’union ou un espace </span><span class="sxs-lookup"><span data-stu-id="d8d84-909">A hyphen or space</span></span> 
- <span data-ttu-id="d8d84-910">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-910">Three digits</span></span> 
- <span data-ttu-id="d8d84-911">Un trait d’union ou un espace </span><span class="sxs-lookup"><span data-stu-id="d8d84-911">A hyphen or space</span></span> 
- <span data-ttu-id="d8d84-912">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-912">Three digits</span></span>

<span data-ttu-id="d8d84-913">Non formatée : Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-913">Unformatted: Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-914">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-914">Checksum</span></span>

<span data-ttu-id="d8d84-915">Oui</span><span class="sxs-lookup"><span data-stu-id="d8d84-915">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-916">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-916">Definition</span></span>

<span data-ttu-id="d8d84-917">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-917">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-918">La fonction Func_canadian_sin trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-918">The function Func_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-919">Au moins deux des éléments suivants, quelle que soit la combinaison :</span><span class="sxs-lookup"><span data-stu-id="d8d84-919">At least two of any combination of the following:</span></span>
    - <span data-ttu-id="d8d84-920">Un mot clé figurant dans la liste Keyword_sin est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-920">A keyword from Keyword_sin is found.</span></span>
    - <span data-ttu-id="d8d84-921">Un mot clé figurant dans la liste Keyword_sin_collaborative est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-921">A keyword from Keyword_sin_collaborative is found.</span></span>
    - <span data-ttu-id="d8d84-922">La fonction Func_eu_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="d8d84-922">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="d8d84-923">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-923">The checksum passes.</span></span>

<span data-ttu-id="d8d84-924">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-924">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-925">La fonction Func_unformatted_canadian_sin trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-925">The function Func_unformatted_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-926">Un mot clé figurant dans la liste Keyword_sin est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-926">A keyword from Keyword_sin is found.</span></span>
- <span data-ttu-id="d8d84-927">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-927">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-928">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-928">Keywords</span></span>

#### <a name="keywordsin"></a><span data-ttu-id="d8d84-929">Keyword_sin</span><span class="sxs-lookup"><span data-stu-id="d8d84-929">Keyword_sin</span></span>

- <span data-ttu-id="d8d84-930">sin</span><span class="sxs-lookup"><span data-stu-id="d8d84-930">sin</span></span> 
- <span data-ttu-id="d8d84-931">assurance sociale
</span><span class="sxs-lookup"><span data-stu-id="d8d84-931">social insurance</span></span> 
- <span data-ttu-id="d8d84-932">numéro d’assurance sociale
</span><span class="sxs-lookup"><span data-stu-id="d8d84-932">numero d'assurance sociale</span></span> 
- <span data-ttu-id="d8d84-933">assoc
</span><span class="sxs-lookup"><span data-stu-id="d8d84-933">sins</span></span> 
- <span data-ttu-id="d8d84-934">ssn</span><span class="sxs-lookup"><span data-stu-id="d8d84-934">ssn</span></span> 
- <span data-ttu-id="d8d84-935">sécurité sociale.</span><span class="sxs-lookup"><span data-stu-id="d8d84-935">ssns</span></span> 
- <span data-ttu-id="d8d84-936">sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="d8d84-936">social security</span></span> 
- <span data-ttu-id="d8d84-937">numéro d’assurance sociale
</span><span class="sxs-lookup"><span data-stu-id="d8d84-937">numero d'assurance social</span></span> 
- <span data-ttu-id="d8d84-938">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="d8d84-938">national identification number</span></span> 
- <span data-ttu-id="d8d84-939">
id national</span><span class="sxs-lookup"><span data-stu-id="d8d84-939">national id</span></span> 
- <span data-ttu-id="d8d84-940"># assoc
</span><span class="sxs-lookup"><span data-stu-id="d8d84-940">sin#</span></span> 
- <span data-ttu-id="d8d84-941">ass soc
</span><span class="sxs-lookup"><span data-stu-id="d8d84-941">soc ins</span></span> 
- <span data-ttu-id="d8d84-942">ass sociale
</span><span class="sxs-lookup"><span data-stu-id="d8d84-942">social ins</span></span> 

#### <a name="keywordsincollaborative"></a><span data-ttu-id="d8d84-943">Keyword_sin_collaborative</span><span class="sxs-lookup"><span data-stu-id="d8d84-943">Keyword_sin_collaborative</span></span>

- <span data-ttu-id="d8d84-944">driver’s license</span><span class="sxs-lookup"><span data-stu-id="d8d84-944">driver's license</span></span> 
- <span data-ttu-id="d8d84-945">drivers license</span><span class="sxs-lookup"><span data-stu-id="d8d84-945">drivers license</span></span> 
- <span data-ttu-id="d8d84-946">conduire permis de</span><span class="sxs-lookup"><span data-stu-id="d8d84-946">driver's licence</span></span> 
- <span data-ttu-id="d8d84-947">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="d8d84-947">drivers licence</span></span> 
- <span data-ttu-id="d8d84-948">DDN
</span><span class="sxs-lookup"><span data-stu-id="d8d84-948">DOB</span></span> 
- <span data-ttu-id="d8d84-949">Birthdate</span><span class="sxs-lookup"><span data-stu-id="d8d84-949">Birthdate</span></span> 
- <span data-ttu-id="d8d84-950">Anniversaire </span><span class="sxs-lookup"><span data-stu-id="d8d84-950">Birthday</span></span> 
- <span data-ttu-id="d8d84-951">Date of Birth
</span><span class="sxs-lookup"><span data-stu-id="d8d84-951">Date of Birth</span></span> 
   
## <a name="chile-identity-card-number"></a><span data-ttu-id="d8d84-952">	Numéro de carte d’identité Chili</span><span class="sxs-lookup"><span data-stu-id="d8d84-952">Chile Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-953">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-953">Format</span></span>

<span data-ttu-id="d8d84-954">7-8 chiffres plus délimiteurs un chiffre de contrôle ou d’une lettre</span><span class="sxs-lookup"><span data-stu-id="d8d84-954">7-8 digits plus delimiters a check digit or letter</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-955">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-955">Pattern</span></span>

<span data-ttu-id="d8d84-956">7 ou 8 chiffres, plus des délimiteurs :</span><span class="sxs-lookup"><span data-stu-id="d8d84-956">7-8 digits plus delimiters:</span></span>
- <span data-ttu-id="d8d84-957">1 ou 2 chiffres </span><span class="sxs-lookup"><span data-stu-id="d8d84-957">1-2 digits</span></span> 
- <span data-ttu-id="d8d84-958">Un point </span><span class="sxs-lookup"><span data-stu-id="d8d84-958">A period</span></span> 
- <span data-ttu-id="d8d84-959">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-959">Three digits</span></span> 
- <span data-ttu-id="d8d84-960">Un point </span><span class="sxs-lookup"><span data-stu-id="d8d84-960">A period</span></span> 
- <span data-ttu-id="d8d84-961">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-961">Three digits</span></span> 
- <span data-ttu-id="d8d84-962">Un tiret</span><span class="sxs-lookup"><span data-stu-id="d8d84-962">A dash</span></span> 
- <span data-ttu-id="d8d84-963">Un chiffre ou une lettre (ne respectant pas la casse) de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-963">One digit or letter (not case sensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-964">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-964">Checksum</span></span>

<span data-ttu-id="d8d84-965">Oui</span><span class="sxs-lookup"><span data-stu-id="d8d84-965">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-966">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-966">Definition</span></span>

<span data-ttu-id="d8d84-967">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-967">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-968">La fonction Func_chile_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-968">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-969">Un mot clé figurant dans la liste Keyword_chile_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-969">A keyword from Keyword_chile_id_card is found.</span></span>
- <span data-ttu-id="d8d84-970">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-970">The checksum passes.</span></span>

<span data-ttu-id="d8d84-971">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-971">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-972">La fonction Func_chile_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-972">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-973">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-973">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-974">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-974">Keywords</span></span>

#### <a name="keywordchileidcard"></a><span data-ttu-id="d8d84-975">Keyword_chile_id_card</span><span class="sxs-lookup"><span data-stu-id="d8d84-975">Keyword_chile_id_card</span></span>

- <span data-ttu-id="d8d84-976">National Identification Number
</span><span class="sxs-lookup"><span data-stu-id="d8d84-976">National Identification Number</span></span> 
- <span data-ttu-id="d8d84-977">Identity card</span><span class="sxs-lookup"><span data-stu-id="d8d84-977">Identity card</span></span> 
- <span data-ttu-id="d8d84-978">ID</span><span class="sxs-lookup"><span data-stu-id="d8d84-978">ID</span></span> 
- <span data-ttu-id="d8d84-979">Identification</span><span class="sxs-lookup"><span data-stu-id="d8d84-979">Identification</span></span> 
- <span data-ttu-id="d8d84-980">Rol Único Nacional
</span><span class="sxs-lookup"><span data-stu-id="d8d84-980">Rol Único Nacional</span></span> 
- <span data-ttu-id="d8d84-981">EXÉCUTER</span><span class="sxs-lookup"><span data-stu-id="d8d84-981">RUN</span></span> 
- <span data-ttu-id="d8d84-982">Rol Único Tributario
</span><span class="sxs-lookup"><span data-stu-id="d8d84-982">Rol Único Tributario</span></span> 
- <span data-ttu-id="d8d84-983">RUT
</span><span class="sxs-lookup"><span data-stu-id="d8d84-983">RUT</span></span> 
- <span data-ttu-id="d8d84-984">Cédula de Identidad
</span><span class="sxs-lookup"><span data-stu-id="d8d84-984">Cédula de Identidad</span></span> 
- <span data-ttu-id="d8d84-985">Número De Identificación Nacional
</span><span class="sxs-lookup"><span data-stu-id="d8d84-985">Número De Identificación Nacional</span></span> 
- <span data-ttu-id="d8d84-986">Tarjeta de identificación
</span><span class="sxs-lookup"><span data-stu-id="d8d84-986">Tarjeta de identificación</span></span> 
- <span data-ttu-id="d8d84-987">Identificación
</span><span class="sxs-lookup"><span data-stu-id="d8d84-987">Identificación</span></span> 
   
## <a name="china-resident-identity-card-prc-number"></a><span data-ttu-id="d8d84-988">	Numéro de carte d’identité de résident Chine (RPC)</span><span class="sxs-lookup"><span data-stu-id="d8d84-988">China Resident Identity Card (PRC) Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-989">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-989">Format</span></span>

<span data-ttu-id="d8d84-990">18 chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-990">18 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-991">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-991">Pattern</span></span>

<span data-ttu-id="d8d84-992">18 chiffres :</span><span class="sxs-lookup"><span data-stu-id="d8d84-992">18 digits:</span></span>
- <span data-ttu-id="d8d84-993">Six chiffres qui composent un code d’adresse </span><span class="sxs-lookup"><span data-stu-id="d8d84-993">Six digits which are an address code</span></span> 
- <span data-ttu-id="d8d84-994">Huit chiffres sous la forme AAAAMMJJ qui correspondent à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="d8d84-994">Eight digits in the form YYYYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="d8d84-995">Trois chiffres qui correspondent à un code d’opération </span><span class="sxs-lookup"><span data-stu-id="d8d84-995">Three digits which are an order code</span></span> 
- <span data-ttu-id="d8d84-996">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-996">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-997">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-997">Checksum</span></span>

<span data-ttu-id="d8d84-998">Oui</span><span class="sxs-lookup"><span data-stu-id="d8d84-998">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-999">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-999">Definition</span></span>

<span data-ttu-id="d8d84-1000">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-1000">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-1001">La fonction Func_china_resident_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1001">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-1002">Un mot clé figurant dans la liste Keyword_china_resident_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1002">A keyword from Keyword_china_resident_id is found.</span></span>
- <span data-ttu-id="d8d84-1003">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1003">The checksum passes.</span></span>

<span data-ttu-id="d8d84-1004">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-1004">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-1005">La fonction Func_china_resident_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1005">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-1006">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1006">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-1007">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-1007">Keywords</span></span>

### <a name="keywordchinaresidentid"></a><span data-ttu-id="d8d84-1008">Keyword_china_resident_id</span><span class="sxs-lookup"><span data-stu-id="d8d84-1008">Keyword_china_resident_id</span></span>

- <span data-ttu-id="d8d84-1009">Resident Identity Card
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1009">Resident Identity Card</span></span> 
- <span data-ttu-id="d8d84-1010">PRC
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1010">PRC</span></span> 
- <span data-ttu-id="d8d84-1011">National Identification Card
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1011">National Identification Card</span></span> 
- <span data-ttu-id="d8d84-1012">身份证 </span><span class="sxs-lookup"><span data-stu-id="d8d84-1012">身份证</span></span> 
- <span data-ttu-id="d8d84-1013">居民 身份证 </span><span class="sxs-lookup"><span data-stu-id="d8d84-1013">居民 身份证</span></span> 
- <span data-ttu-id="d8d84-1014">居民身份证
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1014">居民身份证</span></span> 
- <span data-ttu-id="d8d84-1015">鉴定

</span><span class="sxs-lookup"><span data-stu-id="d8d84-1015">鉴定</span></span> 
- <span data-ttu-id="d8d84-1016">身分證 </span><span class="sxs-lookup"><span data-stu-id="d8d84-1016">身分證</span></span> 
- <span data-ttu-id="d8d84-1017">居民 身份證</span><span class="sxs-lookup"><span data-stu-id="d8d84-1017">居民 身份證</span></span>
- <span data-ttu-id="d8d84-1018">鑑定 </span><span class="sxs-lookup"><span data-stu-id="d8d84-1018">鑑定</span></span> 
   
## <a name="credit-card-number"></a><span data-ttu-id="d8d84-1019">Numéro de carte de crédit</span><span class="sxs-lookup"><span data-stu-id="d8d84-1019">Credit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-1020">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-1020">Format</span></span>

<span data-ttu-id="d8d84-1021">16 chiffres qui peuvent être mis en forme ou non mis en forme (dddddddddddddddd) et doit réussir le test Luhn.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1021">16 digits which can be formatted or unformatted (dddddddddddddddd) and must pass the Luhn test.</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-1022">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-1022">Pattern</span></span>

<span data-ttu-id="d8d84-1023">Modèle très complexe et puissant qui détecte les cartes de visite de toutes les principales marques du monde, notamment Visa, MasterCard, Discover Card, JCB, American Express, etc.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1023">Very complex and robust pattern that detects cards from all major brands worldwide, including Visa, MasterCard, Discover Card, JCB, American Express, gift cards, and diner cards.</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-1024">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-1024">Checksum</span></span>

<span data-ttu-id="d8d84-1025">Oui, la somme de contrôle de Luhn</span><span class="sxs-lookup"><span data-stu-id="d8d84-1025">Yes, the Luhn checksum</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-1026">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-1026">Definition</span></span>

<span data-ttu-id="d8d84-1027">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-1027">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-1028">La fonction Func_credit_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1028">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-1029">L’une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="d8d84-1029">One of the following is true:</span></span>
    - <span data-ttu-id="d8d84-1030">Un mot clé figurant dans la liste Keyword_cc_verification est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1030">A keyword from Keyword_cc_verification is found.</span></span>
    - <span data-ttu-id="d8d84-1031">Un mot clé figurant dans la liste Keyword_cc_name est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1031">A keyword from Keyword_cc_name is found.</span></span>
    - <span data-ttu-id="d8d84-1032">La fonction Func_expiration_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1032">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="d8d84-1033">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1033">The checksum passes.</span></span>

<span data-ttu-id="d8d84-1034">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-1034">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-1035">La fonction Func_credit_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1035">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-1036">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1036">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-1037">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-1037">Keywords</span></span>

#### <a name="keywordccverification"></a><span data-ttu-id="d8d84-1038">Keyword_cc_verification</span><span class="sxs-lookup"><span data-stu-id="d8d84-1038">Keyword_cc_verification</span></span>

- <span data-ttu-id="d8d84-1039">vérification de la carte</span><span class="sxs-lookup"><span data-stu-id="d8d84-1039">card verification</span></span>
- <span data-ttu-id="d8d84-1040">numéro d’identification de la carte</span><span class="sxs-lookup"><span data-stu-id="d8d84-1040">card identification number</span></span>
- <span data-ttu-id="d8d84-1041">nvc
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1041">cvn</span></span>
- <span data-ttu-id="d8d84-1042">nic
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1042">cid</span></span>
- <span data-ttu-id="d8d84-1043">CVC2</span><span class="sxs-lookup"><span data-stu-id="d8d84-1043">cvc2</span></span>
- <span data-ttu-id="d8d84-1044">VVC2</span><span class="sxs-lookup"><span data-stu-id="d8d84-1044">cvv2</span></span>
- <span data-ttu-id="d8d84-1045">pin block
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1045">pin block</span></span>
- <span data-ttu-id="d8d84-1046">code de sécurité
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1046">security code</span></span>
- <span data-ttu-id="d8d84-1047">numéro de sécurité
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1047">security number</span></span>
- <span data-ttu-id="d8d84-1048">n° de sécurité
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1048">security no</span></span>
- <span data-ttu-id="d8d84-1049">numéro d’émission
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1049">issue number</span></span>
- <span data-ttu-id="d8d84-1050">n° d’émission
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1050">issue no</span></span>
- <span data-ttu-id="d8d84-1051">cryptogramme
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1051">cryptogramme</span></span>
- <span data-ttu-id="d8d84-1052">numéro de sécurité
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1052">numéro de sécurité</span></span>
- <span data-ttu-id="d8d84-1053">numéro de sécurité
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1053">numero de securite</span></span>
- <span data-ttu-id="d8d84-1054">kreditkartenprüfnummer
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1054">kreditkartenprüfnummer</span></span>
- <span data-ttu-id="d8d84-1055">kreditkartenprufnummer
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1055">kreditkartenprufnummer</span></span>
- <span data-ttu-id="d8d84-1056">prüfziffer
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1056">prüfziffer</span></span>
- <span data-ttu-id="d8d84-1057">prufziffer
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1057">prufziffer</span></span>
- <span data-ttu-id="d8d84-1058">sicherheits Kode</span><span class="sxs-lookup"><span data-stu-id="d8d84-1058">sicherheits Kode</span></span>
- <span data-ttu-id="d8d84-1059">sicherheitscode
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1059">sicherheitscode</span></span>
- <span data-ttu-id="d8d84-1060">sicherheitsnummer
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1060">sicherheitsnummer</span></span>
- <span data-ttu-id="d8d84-1061">verfalldatum
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1061">verfalldatum</span></span>
- <span data-ttu-id="d8d84-1062">codice di verifica
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1062">codice di verifica</span></span>
- <span data-ttu-id="d8d84-p105">cod. sicurezza
</span><span class="sxs-lookup"><span data-stu-id="d8d84-p105">cod. sicurezza</span></span>
- <span data-ttu-id="d8d84-1065">remboursement sicurezza</span><span class="sxs-lookup"><span data-stu-id="d8d84-1065">cod sicurezza</span></span>
- <span data-ttu-id="d8d84-1066">
n autorizzazione</span><span class="sxs-lookup"><span data-stu-id="d8d84-1066">n autorizzazione</span></span>
- <span data-ttu-id="d8d84-1067">código
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1067">código</span></span>
- <span data-ttu-id="d8d84-1068">codigo
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1068">codigo</span></span>
- <span data-ttu-id="d8d84-p106">cod. seg
</span><span class="sxs-lookup"><span data-stu-id="d8d84-p106">cod. seg</span></span>
- <span data-ttu-id="d8d84-1071">segment de remboursement</span><span class="sxs-lookup"><span data-stu-id="d8d84-1071">cod seg</span></span>
- <span data-ttu-id="d8d84-1072">código de segurança
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1072">código de segurança</span></span>
- <span data-ttu-id="d8d84-1073">codigo de seguranca
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1073">codigo de seguranca</span></span>
- <span data-ttu-id="d8d84-1074">codigo de segurança
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1074">codigo de segurança</span></span>
- <span data-ttu-id="d8d84-1075">código de seguranca
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1075">código de seguranca</span></span>
- <span data-ttu-id="d8d84-p107">cód. Segurança
</span><span class="sxs-lookup"><span data-stu-id="d8d84-p107">cód. segurança</span></span>
- <span data-ttu-id="d8d84-p108">remboursement. CR seguranca. Segurança</span><span class="sxs-lookup"><span data-stu-id="d8d84-p108">cod. seguranca cod. segurança</span></span>
- <span data-ttu-id="d8d84-p109">cód. seguranca
</span><span class="sxs-lookup"><span data-stu-id="d8d84-p109">cód. seguranca</span></span>
- <span data-ttu-id="d8d84-1083">cód segurança</span><span class="sxs-lookup"><span data-stu-id="d8d84-1083">cód segurança</span></span>
- <span data-ttu-id="d8d84-1084">cabillaud seguranca CR segurança</span><span class="sxs-lookup"><span data-stu-id="d8d84-1084">cod seguranca cod segurança</span></span>
- <span data-ttu-id="d8d84-1085">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="d8d84-1085">cód seguranca</span></span>
- <span data-ttu-id="d8d84-1086">número de verificação
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1086">número de verificação</span></span>
- <span data-ttu-id="d8d84-1087">numero de verificacao
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1087">numero de verificacao</span></span>
- <span data-ttu-id="d8d84-1088">ablauf
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1088">ablauf</span></span>
- <span data-ttu-id="d8d84-1089">gültig bis
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1089">gültig bis</span></span>
- <span data-ttu-id="d8d84-1090">gültigkeitsdatum
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1090">gültigkeitsdatum</span></span>
- <span data-ttu-id="d8d84-1091">gultig bis
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1091">gultig bis</span></span>
- <span data-ttu-id="d8d84-1092">gultigkeitsdatum
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1092">gultigkeitsdatum</span></span>
- <span data-ttu-id="d8d84-1093">scadenza
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1093">scadenza</span></span>
- <span data-ttu-id="d8d84-1094">data scad
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1094">data scad</span></span>
- <span data-ttu-id="d8d84-1095">fecha de expiracion
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1095">fecha de expiracion</span></span>
- <span data-ttu-id="d8d84-1096">fecha de venc
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1096">fecha de venc</span></span>
- <span data-ttu-id="d8d84-1097">vencimiento
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1097">vencimiento</span></span>
- <span data-ttu-id="d8d84-1098">válido hasta
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1098">válido hasta</span></span>
- <span data-ttu-id="d8d84-1099">valido hasta
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1099">valido hasta</span></span>
- <span data-ttu-id="d8d84-1100">vto
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1100">vto</span></span>
- <span data-ttu-id="d8d84-1101">data de expiração
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1101">data de expiração</span></span>
- <span data-ttu-id="d8d84-1102">data de expiracao
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1102">data de expiracao</span></span>
- <span data-ttu-id="d8d84-1103">data em que expira
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1103">data em que expira</span></span>
- <span data-ttu-id="d8d84-1104">validade
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1104">validade</span></span>
- <span data-ttu-id="d8d84-1105">valor
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1105">valor</span></span>
- <span data-ttu-id="d8d84-1106">vencimento
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1106">vencimento</span></span>
- <span data-ttu-id="d8d84-1107">Venc</span><span class="sxs-lookup"><span data-stu-id="d8d84-1107">Venc</span></span> 

#### <a name="keywordccname"></a><span data-ttu-id="d8d84-1108">Keyword_cc_name</span><span class="sxs-lookup"><span data-stu-id="d8d84-1108">Keyword_cc_name</span></span>

- <span data-ttu-id="d8d84-1109">amex</span><span class="sxs-lookup"><span data-stu-id="d8d84-1109">amex</span></span>
- <span data-ttu-id="d8d84-1110">
american express</span><span class="sxs-lookup"><span data-stu-id="d8d84-1110">american express</span></span>
- <span data-ttu-id="d8d84-1111">americanexpress
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1111">americanexpress</span></span>
- <span data-ttu-id="d8d84-1112">Visa</span><span class="sxs-lookup"><span data-stu-id="d8d84-1112">Visa</span></span>
- <span data-ttu-id="d8d84-1113">mastercard
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1113">mastercard</span></span>
- <span data-ttu-id="d8d84-1114">master card
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1114">master card</span></span>
- <span data-ttu-id="d8d84-1115">
mc
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1115">mc</span></span> 
- <span data-ttu-id="d8d84-1116">mastercards</span><span class="sxs-lookup"><span data-stu-id="d8d84-1116">mastercards</span></span>
- <span data-ttu-id="d8d84-1117">
master cards</span><span class="sxs-lookup"><span data-stu-id="d8d84-1117">master cards</span></span>
- <span data-ttu-id="d8d84-1118">Club de dîner</span><span class="sxs-lookup"><span data-stu-id="d8d84-1118">diner's Club</span></span>
- <span data-ttu-id="d8d84-1119">diners club
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1119">diners club</span></span>
- <span data-ttu-id="d8d84-1120">dinersclub
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1120">dinersclub</span></span>
- <span data-ttu-id="d8d84-1121">discover card
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1121">discover card</span></span>
- <span data-ttu-id="d8d84-1122">discovercard
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1122">discovercard</span></span>
- <span data-ttu-id="d8d84-1123">discover cards
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1123">discover cards</span></span>
- <span data-ttu-id="d8d84-1124">JCB</span><span class="sxs-lookup"><span data-stu-id="d8d84-1124">JCB</span></span>
- <span data-ttu-id="d8d84-1125">japanese card bureau
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1125">japanese card bureau</span></span>
- <span data-ttu-id="d8d84-1126">carte blanche
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1126">carte blanche</span></span>
- <span data-ttu-id="d8d84-1127">carteblanche
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1127">carteblanche</span></span>
- <span data-ttu-id="d8d84-1128">carte de crédit
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1128">credit card</span></span>
- <span data-ttu-id="d8d84-1129">cc #</span><span class="sxs-lookup"><span data-stu-id="d8d84-1129">cc#</span></span>
- <span data-ttu-id="d8d84-1130">cc #:</span><span class="sxs-lookup"><span data-stu-id="d8d84-1130">cc#:</span></span>
- <span data-ttu-id="d8d84-1131">
date d’expiration</span><span class="sxs-lookup"><span data-stu-id="d8d84-1131">expiration date</span></span>
- <span data-ttu-id="d8d84-1132">date d’exp
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1132">exp date</span></span>
- <span data-ttu-id="d8d84-1133">
date d’expiration</span><span class="sxs-lookup"><span data-stu-id="d8d84-1133">expiry date</span></span>
- <span data-ttu-id="d8d84-1134">
date d’expiration</span><span class="sxs-lookup"><span data-stu-id="d8d84-1134">date d’expiration</span></span>
- <span data-ttu-id="d8d84-1135">
date d’exp</span><span class="sxs-lookup"><span data-stu-id="d8d84-1135">date d'exp</span></span>
- <span data-ttu-id="d8d84-1136">
date expiration</span><span class="sxs-lookup"><span data-stu-id="d8d84-1136">date expiration</span></span>
- <span data-ttu-id="d8d84-1137">carte bancaire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1137">bank card</span></span>
- <span data-ttu-id="d8d84-1138">
carte bancaire</span><span class="sxs-lookup"><span data-stu-id="d8d84-1138">bankcard</span></span>
- <span data-ttu-id="d8d84-1139">numéro de carte
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1139">card number</span></span>
- <span data-ttu-id="d8d84-1140">num de carte
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1140">card num</span></span>
- <span data-ttu-id="d8d84-1141">numéro de carte
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1141">cardnumber</span></span>
- <span data-ttu-id="d8d84-1142">numéros de carte
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1142">cardnumbers</span></span>
- <span data-ttu-id="d8d84-1143">numéros de carte
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1143">card numbers</span></span>
- <span data-ttu-id="d8d84-1144">carte de crédit
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1144">creditcard</span></span>
- <span data-ttu-id="d8d84-1145">cartes de crédit
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1145">credit cards</span></span>
- <span data-ttu-id="d8d84-1146">cartes de crédit
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1146">creditcards</span></span>
- <span data-ttu-id="d8d84-1147">ncc
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1147">ccn</span></span>
- <span data-ttu-id="d8d84-1148">titulaire de la carte
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1148">card holder</span></span>
- <span data-ttu-id="d8d84-1149">titulaire de la carte
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1149">cardholder</span></span>
- <span data-ttu-id="d8d84-1150">titulaires de la carte
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1150">card holders</span></span>
- <span data-ttu-id="d8d84-1151">titulaires de la carte
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1151">cardholders</span></span>
- <span data-ttu-id="d8d84-1152">carte de vérification
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1152">check card</span></span>
- <span data-ttu-id="d8d84-1153">carte de vérification
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1153">checkcard</span></span>
- <span data-ttu-id="d8d84-1154">cartes de vérification
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1154">check cards</span></span>
- <span data-ttu-id="d8d84-1155">cartes de vérification
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1155">checkcards</span></span>
- <span data-ttu-id="d8d84-1156">carte de débit
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1156">debit card</span></span>
- <span data-ttu-id="d8d84-1157">carte de débit
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1157">debitcard</span></span>
- <span data-ttu-id="d8d84-1158">cartes de débit
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1158">debit cards</span></span>
- <span data-ttu-id="d8d84-1159">cartes de débit
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1159">debitcards</span></span>
- <span data-ttu-id="d8d84-1160">carte de retrait
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1160">atm card</span></span>
- <span data-ttu-id="d8d84-1161">carte de retrait
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1161">atmcard</span></span>
- <span data-ttu-id="d8d84-1162">cartes de retrait
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1162">atm cards</span></span>
- <span data-ttu-id="d8d84-1163">cartes de retrait
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1163">atmcards</span></span>
- <span data-ttu-id="d8d84-1164">
enroute</span><span class="sxs-lookup"><span data-stu-id="d8d84-1164">enroute</span></span>
- <span data-ttu-id="d8d84-1165">
en route</span><span class="sxs-lookup"><span data-stu-id="d8d84-1165">en route</span></span>
- <span data-ttu-id="d8d84-1166">type de carte
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1166">card type</span></span>
- <span data-ttu-id="d8d84-1167">carte bancaire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1167">carte bancaire</span></span>
- <span data-ttu-id="d8d84-1168">carte de crédit
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1168">carte de crédit</span></span>
- <span data-ttu-id="d8d84-1169">carte de credit
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1169">carte de credit</span></span>
- <span data-ttu-id="d8d84-1170">numéro de carte
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1170">numéro de carte</span></span>
- <span data-ttu-id="d8d84-1171">numero de carte
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1171">numero de carte</span></span>
- <span data-ttu-id="d8d84-1172">nº de la carte
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1172">nº de la carte</span></span>
- <span data-ttu-id="d8d84-1173">nº de carte
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1173">nº de carte</span></span>
- <span data-ttu-id="d8d84-1174">kreditkarte
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1174">kreditkarte</span></span>
- <span data-ttu-id="d8d84-1175">karte
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1175">karte</span></span>
- <span data-ttu-id="d8d84-1176">karteninhaber
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1176">karteninhaber</span></span>
- <span data-ttu-id="d8d84-1177">karteninhabers</span><span class="sxs-lookup"><span data-stu-id="d8d84-1177">karteninhabers</span></span>
- <span data-ttu-id="d8d84-1178">kreditkarteninhaber
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1178">kreditkarteninhaber</span></span>
- <span data-ttu-id="d8d84-1179">kreditkarteninstitut
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1179">kreditkarteninstitut</span></span>
- <span data-ttu-id="d8d84-1180">kreditkartentyp
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1180">kreditkartentyp</span></span>
- <span data-ttu-id="d8d84-1181">eigentümername
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1181">eigentümername</span></span>
- <span data-ttu-id="d8d84-1182">
kartennr
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1182">kartennr</span></span> 
- <span data-ttu-id="d8d84-1183">kartennummer</span><span class="sxs-lookup"><span data-stu-id="d8d84-1183">kartennummer</span></span>
- <span data-ttu-id="d8d84-1184">
kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="d8d84-1184">kreditkartennummer</span></span>
- <span data-ttu-id="d8d84-1185">kreditkarten-nummer</span><span class="sxs-lookup"><span data-stu-id="d8d84-1185">kreditkarten-nummer</span></span>
- <span data-ttu-id="d8d84-1186">Carta di credito
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1186">carta di credito</span></span>
- <span data-ttu-id="d8d84-1187">Carta credito
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1187">carta credito</span></span>
- <span data-ttu-id="d8d84-1188">Carta</span><span class="sxs-lookup"><span data-stu-id="d8d84-1188">carta</span></span>
- <span data-ttu-id="d8d84-1189">carta n</span><span class="sxs-lookup"><span data-stu-id="d8d84-1189">n carta</span></span>
- <span data-ttu-id="d8d84-p110">nr. carta
</span><span class="sxs-lookup"><span data-stu-id="d8d84-p110">nr. carta</span></span>
- <span data-ttu-id="d8d84-1192">nr carta</span><span class="sxs-lookup"><span data-stu-id="d8d84-1192">nr carta</span></span>
- <span data-ttu-id="d8d84-1193">numero carta
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1193">numero carta</span></span>
- <span data-ttu-id="d8d84-1194">numero della carta
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1194">numero della carta</span></span>
- <span data-ttu-id="d8d84-1195">numero di carta
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1195">numero di carta</span></span>
- <span data-ttu-id="d8d84-1196">tarjeta credito
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1196">tarjeta credito</span></span>
- <span data-ttu-id="d8d84-1197">tarjeta de credito
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1197">tarjeta de credito</span></span>
- <span data-ttu-id="d8d84-1198">
tarjeta crédito</span><span class="sxs-lookup"><span data-stu-id="d8d84-1198">tarjeta crédito</span></span>
- <span data-ttu-id="d8d84-1199">
tarjeta de crédito</span><span class="sxs-lookup"><span data-stu-id="d8d84-1199">tarjeta de crédito</span></span>
- <span data-ttu-id="d8d84-1200">tarjeta de atm
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1200">tarjeta de atm</span></span>
- <span data-ttu-id="d8d84-1201">tarjeta atm
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1201">tarjeta atm</span></span>
- <span data-ttu-id="d8d84-1202">tarjeta debito
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1202">tarjeta debito</span></span>
- <span data-ttu-id="d8d84-1203">tarjeta de debito
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1203">tarjeta de debito</span></span>
- <span data-ttu-id="d8d84-1204">
tarjeta débito</span><span class="sxs-lookup"><span data-stu-id="d8d84-1204">tarjeta débito</span></span>
- <span data-ttu-id="d8d84-1205">
tarjeta de débito</span><span class="sxs-lookup"><span data-stu-id="d8d84-1205">tarjeta de débito</span></span>
- <span data-ttu-id="d8d84-1206">nº de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1206">nº de tarjeta</span></span>
- <span data-ttu-id="d8d84-p111">no. de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="d8d84-p111">no. de tarjeta</span></span>
- <span data-ttu-id="d8d84-1209">Aucun tarjeta de</span><span class="sxs-lookup"><span data-stu-id="d8d84-1209">no de tarjeta</span></span>
- <span data-ttu-id="d8d84-1210">numero de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1210">numero de tarjeta</span></span>
- <span data-ttu-id="d8d84-1211">número de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1211">número de tarjeta</span></span>
- <span data-ttu-id="d8d84-1212">tarjeta no
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1212">tarjeta no</span></span>
- <span data-ttu-id="d8d84-1213">tarjetahabiente
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1213">tarjetahabiente</span></span>
- <span data-ttu-id="d8d84-1214">cartão de crédito
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1214">cartão de crédito</span></span>
- <span data-ttu-id="d8d84-1215">cartão de credito
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1215">cartão de credito</span></span>
- <span data-ttu-id="d8d84-1216">cartao de crédito
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1216">cartao de crédito</span></span>
- <span data-ttu-id="d8d84-1217">cartao de credito
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1217">cartao de credito</span></span>
- <span data-ttu-id="d8d84-1218">cartão de débito
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1218">cartão de débito</span></span>
- <span data-ttu-id="d8d84-1219">cartao de débito
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1219">cartao de débito</span></span>
- <span data-ttu-id="d8d84-1220">cartão de debito
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1220">cartão de debito</span></span>
- <span data-ttu-id="d8d84-1221">cartao de debito
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1221">cartao de debito</span></span>
- <span data-ttu-id="d8d84-1222">débito automático</span><span class="sxs-lookup"><span data-stu-id="d8d84-1222">débito automático</span></span>
- <span data-ttu-id="d8d84-1223">debito automatico
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1223">debito automatico</span></span>
- <span data-ttu-id="d8d84-1224">
número do cartão</span><span class="sxs-lookup"><span data-stu-id="d8d84-1224">número do cartão</span></span>
- <span data-ttu-id="d8d84-1225">
numero do cartão
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1225">numero do cartão</span></span> 
- <span data-ttu-id="d8d84-1226">número do cartao</span><span class="sxs-lookup"><span data-stu-id="d8d84-1226">número do cartao</span></span>
- <span data-ttu-id="d8d84-1227">
numero do cartao</span><span class="sxs-lookup"><span data-stu-id="d8d84-1227">numero do cartao</span></span>
- <span data-ttu-id="d8d84-1228">número de cartão
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1228">número de cartão</span></span>
- <span data-ttu-id="d8d84-1229">numero de cartão
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1229">numero de cartão</span></span>
- <span data-ttu-id="d8d84-1230">número de cartao
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1230">número de cartao</span></span>
- <span data-ttu-id="d8d84-1231">numero de cartao
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1231">numero de cartao</span></span>
- <span data-ttu-id="d8d84-1232">Nº cartão</span><span class="sxs-lookup"><span data-stu-id="d8d84-1232">nº do cartão</span></span>
- <span data-ttu-id="d8d84-1233">nº do cartao
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1233">nº do cartao</span></span>
- <span data-ttu-id="d8d84-p112">nº. do cartão
</span><span class="sxs-lookup"><span data-stu-id="d8d84-p112">nº. do cartão</span></span>
- <span data-ttu-id="d8d84-1236">Aucun cartão</span><span class="sxs-lookup"><span data-stu-id="d8d84-1236">no do cartão</span></span>
- <span data-ttu-id="d8d84-1237">Aucun cartao</span><span class="sxs-lookup"><span data-stu-id="d8d84-1237">no do cartao</span></span>
- <span data-ttu-id="d8d84-p113">no. do cartão
</span><span class="sxs-lookup"><span data-stu-id="d8d84-p113">no. do cartão</span></span>
- <span data-ttu-id="d8d84-p114">
no. do cartao
</span><span class="sxs-lookup"><span data-stu-id="d8d84-p114">no. do cartao</span></span> 
   
## <a name="croatia-identity-card-number"></a><span data-ttu-id="d8d84-1242">Numéro de carte d’identité croate</span><span class="sxs-lookup"><span data-stu-id="d8d84-1242">Croatia Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-1243">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-1243">Format</span></span>

<span data-ttu-id="d8d84-1244">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-1244">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-1245">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-1245">Pattern</span></span>

<span data-ttu-id="d8d84-1246">Neuf chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="d8d84-1246">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-1247">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-1247">Checksum</span></span>

<span data-ttu-id="d8d84-1248">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-1248">No</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-1249">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-1249">Definition</span></span>

<span data-ttu-id="d8d84-1250">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-1250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-1251">La fonction Func_croatia_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1251">The function Func_croatia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-1252">Un mot clé figurant dans la liste Keyword_croatia_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1252">A keyword from Keyword_croatia_id_card is found.</span></span>

```
<!--Croatia Identity Card Number-->
<Entity id="ff12f884-c20a-4189-b185-34c8e7258d47" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_croatia_id_card"/>
     <Match idRef="Keyword_croatia_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8d84-1253">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-1253">Keywords</span></span>

#### <a name="keywordcroatiaidcard"></a><span data-ttu-id="d8d84-1254">Keyword_croatia_id_card</span><span class="sxs-lookup"><span data-stu-id="d8d84-1254">Keyword_croatia_id_card</span></span>

- <span data-ttu-id="d8d84-1255">Croatian identity card</span><span class="sxs-lookup"><span data-stu-id="d8d84-1255">Croatian identity card</span></span>
- <span data-ttu-id="d8d84-1256">Osobna iskaznica</span><span class="sxs-lookup"><span data-stu-id="d8d84-1256">Osobna iskaznica</span></span>

   
## <a name="croatia-personal-identification-oib-number"></a><span data-ttu-id="d8d84-1257">	Numéro d’identification personnel (OIB) Croatie</span><span class="sxs-lookup"><span data-stu-id="d8d84-1257">Croatia Personal Identification (OIB) Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-1258">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-1258">Format</span></span>

<span data-ttu-id="d8d84-1259">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-1259">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-1260">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-1260">Pattern</span></span>

<span data-ttu-id="d8d84-1261">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="d8d84-1261">11 digits:</span></span>
- <span data-ttu-id="d8d84-1262">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-1262">10 digits</span></span> 
- <span data-ttu-id="d8d84-1263">Chiffre final est un chiffre de contrôle à des fins d’échanges internationaux de données, les lettres de ressources humaines sont ajoutés précédant les onze chiffres.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1263">Final digit is a check digit For the purposes of international data exchange, the letters HR are added preceding the eleven digits.</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-1264">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-1264">Checksum</span></span>

<span data-ttu-id="d8d84-1265">Oui</span><span class="sxs-lookup"><span data-stu-id="d8d84-1265">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-1266">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-1266">Definition</span></span>

<span data-ttu-id="d8d84-1267">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-1267">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-1268">La fonction Func_croatia_oib_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1268">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-1269">Un mot clé figurant dans la liste Keyword_croatia_oib_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1269">A keyword from Keyword_croatia_oib_number is found.</span></span>
- <span data-ttu-id="d8d84-1270">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1270">The checksum passes.</span></span>

<span data-ttu-id="d8d84-1271">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-1271">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-1272">La fonction Func_croatia_oib_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1272">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-1273">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1273">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-1274">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-1274">Keywords</span></span>

#### <a name="keywordcroatiaoibnumber"></a><span data-ttu-id="d8d84-1275">Keyword_croatia_oib_number</span><span class="sxs-lookup"><span data-stu-id="d8d84-1275">Keyword_croatia_oib_number</span></span>

- <span data-ttu-id="d8d84-1276">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="d8d84-1276">Personal Identification Number</span></span>
- <span data-ttu-id="d8d84-1277">Osobni identifikacijski broj
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1277">Osobni identifikacijski broj</span></span> 
- <span data-ttu-id="d8d84-1278">OIB
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1278">OIB</span></span> 

   
## <a name="czech-personal-identity-number"></a><span data-ttu-id="d8d84-1279">Numéro d’identification personnelle tchèque</span><span class="sxs-lookup"><span data-stu-id="d8d84-1279">Czech Personal Identity Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-1280">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-1280">Format</span></span>

<span data-ttu-id="d8d84-1281">Neuf chiffres avec facultatif barre oblique (ancien format) 10 chiffres avec facultatif barre oblique (nouveau format)</span><span class="sxs-lookup"><span data-stu-id="d8d84-1281">Nine digits with optional forward slash (old format) 10 digits with optional forward slash (new format)</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-1282">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-1282">Pattern</span></span>

<span data-ttu-id="d8d84-1283">Neuf chiffres (ancien format) :</span><span class="sxs-lookup"><span data-stu-id="d8d84-1283">Nine digits (old format):</span></span>
- <span data-ttu-id="d8d84-1284">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-1284">Nine digits</span></span>

<span data-ttu-id="d8d84-1285">OU</span><span class="sxs-lookup"><span data-stu-id="d8d84-1285">OR</span></span>

- <span data-ttu-id="d8d84-1286">Six chiffres qui représentent la date de naissance</span><span class="sxs-lookup"><span data-stu-id="d8d84-1286">Six digits that represent date of birth</span></span>
- <span data-ttu-id="d8d84-1287">Une barre oblique </span><span class="sxs-lookup"><span data-stu-id="d8d84-1287">A forward slash</span></span>
- <span data-ttu-id="d8d84-1288">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-1288">Three digits</span></span>

<span data-ttu-id="d8d84-1289">10 chiffres (nouveau format) :</span><span class="sxs-lookup"><span data-stu-id="d8d84-1289">10 digits (new format):</span></span>
- <span data-ttu-id="d8d84-1290">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-1290">10 digits</span></span>

<span data-ttu-id="d8d84-1291">OU</span><span class="sxs-lookup"><span data-stu-id="d8d84-1291">OR</span></span>

- <span data-ttu-id="d8d84-1292">Six chiffres qui représentent la date de naissance</span><span class="sxs-lookup"><span data-stu-id="d8d84-1292">Six digits that represent date of birth</span></span>
- <span data-ttu-id="d8d84-1293">Une barre oblique </span><span class="sxs-lookup"><span data-stu-id="d8d84-1293">A forward slash</span></span> 
- <span data-ttu-id="d8d84-1294">Quatre chiffres où le dernier chiffre est un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-1294">Four digits where last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-1295">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-1295">Checksum</span></span>

<span data-ttu-id="d8d84-1296">Oui</span><span class="sxs-lookup"><span data-stu-id="d8d84-1296">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-1297">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-1297">Definition</span></span>

<span data-ttu-id="d8d84-p115">Une stratégie DLP est de 85 % convaincu que ce type d’informations sensibles a été détecté if, au sein d’une proximité de 300 caractères : la fonction Func_czech_id_card recherche le contenu qui correspond au modèle. Un mot clé à partir de Keyword_czech_id_card est trouvé. Passe de la somme de contrôle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-p115">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_czech_id_card finds content that matches the pattern. A keyword from Keyword_czech_id_card is found. The checksum passes.</span></span>

```
<!-- Czech Personal Identity Number -->
<Entity id="60c0725a-4eb6-455b-9dda-05d8a7396497"      patternsProximity="300" recommendedConfidence="85">
   <Pattern confidenceLevel="85">
      <IdMatch idRef="Func_czech_id_card" />
      <Match idRef="Keyword_czech_id_card" />
   </Pattern>
</Entity>
```
### <a name="keywords"></a><span data-ttu-id="d8d84-1301">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-1301">Keywords</span></span>

- <span data-ttu-id="d8d84-1302">numéro d’identification personnelle tchèque</span><span class="sxs-lookup"><span data-stu-id="d8d84-1302">czech personal identity number</span></span>
- <span data-ttu-id="d8d84-1303">Rodné číslo</span><span class="sxs-lookup"><span data-stu-id="d8d84-1303">Rodné číslo</span></span>
   
## <a name="denmark-personal-identification-number"></a><span data-ttu-id="d8d84-1304">	Numéro d’identification personnel Danemark</span><span class="sxs-lookup"><span data-stu-id="d8d84-1304">Denmark Personal Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-1305">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-1305">Format</span></span>

<span data-ttu-id="d8d84-1306">10 chiffres contenant un trait d’union</span><span class="sxs-lookup"><span data-stu-id="d8d84-1306">10 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-1307">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-1307">Pattern</span></span>

<span data-ttu-id="d8d84-1308">10 chiffres :</span><span class="sxs-lookup"><span data-stu-id="d8d84-1308">10 digits:</span></span>
- <span data-ttu-id="d8d84-1309">Six chiffres au format JJMMAA qui correspondent à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="d8d84-1309">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="d8d84-1310">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="d8d84-1310">A hyphen</span></span> 
- <span data-ttu-id="d8d84-1311">Quatre chiffres où le dernier chiffre est un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-1311">Four digits where the final digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-1312">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-1312">Checksum</span></span>

<span data-ttu-id="d8d84-1313">Oui</span><span class="sxs-lookup"><span data-stu-id="d8d84-1313">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-1314">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-1314">Definition</span></span>

<span data-ttu-id="d8d84-p116">Une stratégie DLP est convaincu que ce type d’informations sensibles a été détecté à 75 % if, au sein d’une proximité de 300 caractères : l’expression régulière Regex_denmark_id recherche de contenu qui correspond au modèle. Un mot clé à partir de Keyword_denmark_id est trouvé. Passe de la somme de contrôle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-p116">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_denmark_id finds content that matches the pattern. A keyword from Keyword_denmark_id is found. The checksum passes.</span></span>

```
<!-- Denmark Personal Identification Number -->
<Entity id="6c4f2fef-56e1-4c00-8093-88d7a01cf460" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_denmark_id"/>
     <Match idRef="Keyword_denmark_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8d84-1318">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-1318">Keywords</span></span>

#### <a name="keyworddenmarkid"></a><span data-ttu-id="d8d84-1319">Keyword_denmark_id</span><span class="sxs-lookup"><span data-stu-id="d8d84-1319">Keyword_denmark_id</span></span>

- <span data-ttu-id="d8d84-1320">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="d8d84-1320">Personal Identification Number</span></span>
- <span data-ttu-id="d8d84-1321">CPR</span><span class="sxs-lookup"><span data-stu-id="d8d84-1321">CPR</span></span>
- <span data-ttu-id="d8d84-1322">Det Centrale Personregister</span><span class="sxs-lookup"><span data-stu-id="d8d84-1322">Det Centrale Personregister</span></span>
- <span data-ttu-id="d8d84-1323">Personnummer</span><span class="sxs-lookup"><span data-stu-id="d8d84-1323">Personnummer</span></span>
   
## <a name="drug-enforcement-agency-dea-number"></a><span data-ttu-id="d8d84-1324">Numéro de la Drug Enforcement Agency (DEA)</span><span class="sxs-lookup"><span data-stu-id="d8d84-1324">Drug Enforcement Agency (DEA) Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-1325">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-1325">Format</span></span>

<span data-ttu-id="d8d84-1326">Deux lettres suivies de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-1326">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-1327">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-1327">Pattern</span></span>

<span data-ttu-id="d8d84-1328">Le modèle doit inclure tous les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="d8d84-1328">Pattern must include all of the following:</span></span>
- <span data-ttu-id="d8d84-1329">Une lettre (ne respecte pas la casse) à partir de cet ensemble de lettres possibles : abcdefghjklmnprstux, qui est un code d’utilisateur enregistré</span><span class="sxs-lookup"><span data-stu-id="d8d84-1329">One letter (not case sensitive) from this set of possible letters: abcdefghjklmnprstux, which is a registrant code</span></span> 
- <span data-ttu-id="d8d84-1330">Une lettre (ne respecte pas la casse), qui est la première lettre du nom de l’utilisateur enregistré</span><span class="sxs-lookup"><span data-stu-id="d8d84-1330">One letter (not case sensitive), which is the first letter of the registrant's last name</span></span> 
- <span data-ttu-id="d8d84-1331">Sept chiffres, le dernier est le chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-1331">Seven digits, the last of which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-1332">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-1332">Checksum</span></span>

<span data-ttu-id="d8d84-1333">Oui</span><span class="sxs-lookup"><span data-stu-id="d8d84-1333">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-1334">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-1334">Definition</span></span>

<span data-ttu-id="d8d84-1335">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-1335">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-1336">La fonction Func_dea_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1336">The function Func_dea_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-1337">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1337">The checksum passes.</span></span>

```
<!-- DEA Number -->
<Entity id="9a5445ad-406e-43eb-8bd7-cac17ab6d0e4" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_dea_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8d84-1338">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-1338">Keywords</span></span>

<span data-ttu-id="d8d84-1339">Aucune</span><span class="sxs-lookup"><span data-stu-id="d8d84-1339">None</span></span>

   
## <a name="eu-debit-card-number"></a><span data-ttu-id="d8d84-1340">Numéro de carte de débit Union européenne</span><span class="sxs-lookup"><span data-stu-id="d8d84-1340">EU Debit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-1341">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-1341">Format</span></span>

<span data-ttu-id="d8d84-1342">16 chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-1342">16 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-1343">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-1343">Pattern</span></span>

<span data-ttu-id="d8d84-1344">Modèle très complexe et puissant</span><span class="sxs-lookup"><span data-stu-id="d8d84-1344">Very complex and robust pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-1345">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-1345">Checksum</span></span>

<span data-ttu-id="d8d84-1346">Oui</span><span class="sxs-lookup"><span data-stu-id="d8d84-1346">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-1347">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-1347">Definition</span></span>

<span data-ttu-id="d8d84-1348">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-1348">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-1349">La fonction Func_eu_debit_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1349">The function Func_eu_debit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-1350">Au moins une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="d8d84-1350">At least one of the following is true:</span></span>
    - <span data-ttu-id="d8d84-1351">Un mot clé figurant dans la liste Keyword_eu_debit_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1351">A keyword from Keyword_eu_debit_card is found.</span></span>
    - <span data-ttu-id="d8d84-1352">Un mot clé figurant dans la liste Keyword_card_terms_dict est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1352">A keyword from Keyword_card_terms_dict is found.</span></span>
    - <span data-ttu-id="d8d84-1353">Un mot clé figurant dans la liste Keyword_card_security_terms_dict est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1353">A keyword from Keyword_card_security_terms_dict is found.</span></span>
    - <span data-ttu-id="d8d84-1354">Un mot clé figurant dans la liste Keyword_card_expiration_terms_dict est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1354">A keyword from Keyword_card_expiration_terms_dict is found.</span></span>
    - <span data-ttu-id="d8d84-1355">La fonction Func_expiration_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1355">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="d8d84-1356">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1356">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-1357">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-1357">Keywords</span></span>

#### <a name="keywordeudebitcard"></a><span data-ttu-id="d8d84-1358">Keyword_eu_debit_card</span><span class="sxs-lookup"><span data-stu-id="d8d84-1358">Keyword_eu_debit_card</span></span>

- <span data-ttu-id="d8d84-1359">numéro de compte</span><span class="sxs-lookup"><span data-stu-id="d8d84-1359">account number</span></span> 
- <span data-ttu-id="d8d84-1360">numéro de carte
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1360">card number</span></span> 
- <span data-ttu-id="d8d84-1361">n° carte
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1361">card no.</span></span> 
- <span data-ttu-id="d8d84-1362">numéro de sécurité
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1362">security number</span></span> 
- <span data-ttu-id="d8d84-1363">cc #</span><span class="sxs-lookup"><span data-stu-id="d8d84-1363">cc#</span></span> 

#### <a name="keywordcardtermsdict"></a><span data-ttu-id="d8d84-1364">Keyword_card_terms_dict</span><span class="sxs-lookup"><span data-stu-id="d8d84-1364">Keyword_card_terms_dict</span></span>

- <span data-ttu-id="d8d84-1365">num de compte
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1365">acct nbr</span></span> 
- <span data-ttu-id="d8d84-1366">num de compte
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1366">acct num</span></span> 
- <span data-ttu-id="d8d84-1367">n° compte
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1367">acct no</span></span> 
- <span data-ttu-id="d8d84-1368">american express
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1368">american express</span></span> 
- <span data-ttu-id="d8d84-1369">americanexpress
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1369">americanexpress</span></span> 
- <span data-ttu-id="d8d84-1370">americano espresso
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1370">americano espresso</span></span> 
- <span data-ttu-id="d8d84-1371">amex</span><span class="sxs-lookup"><span data-stu-id="d8d84-1371">amex</span></span> 
- <span data-ttu-id="d8d84-1372">carte de retrait
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1372">atm card</span></span> 
- <span data-ttu-id="d8d84-1373">cartes de retrait
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1373">atm cards</span></span> 
- <span data-ttu-id="d8d84-1374">atm kaart
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1374">atm kaart</span></span> 
- <span data-ttu-id="d8d84-1375">carte de retrait
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1375">atmcard</span></span> 
- <span data-ttu-id="d8d84-1376">cartes de retrait
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1376">atmcards</span></span> 
- <span data-ttu-id="d8d84-1377">atmkaart
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1377">atmkaart</span></span> 
- <span data-ttu-id="d8d84-1378">atmkaarten
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1378">atmkaarten</span></span> 
- <span data-ttu-id="d8d84-1379">bancontact
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1379">bancontact</span></span> 
- <span data-ttu-id="d8d84-1380">carte bancaire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1380">bank card</span></span> 
- <span data-ttu-id="d8d84-1381">bankkaart
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1381">bankkaart</span></span> 
- <span data-ttu-id="d8d84-1382">titulaire de la carte
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1382">card holder</span></span> 
- <span data-ttu-id="d8d84-1383">titulaires de la carte
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1383">card holders</span></span> 
- <span data-ttu-id="d8d84-1384">num de carte
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1384">card num</span></span> 
- <span data-ttu-id="d8d84-1385">numéro de carte
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1385">card number</span></span> 
- <span data-ttu-id="d8d84-1386">numéros de carte
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1386">card numbers</span></span> 
- <span data-ttu-id="d8d84-1387">type de carte
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1387">card type</span></span> 
- <span data-ttu-id="d8d84-1388">cardano numerico
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1388">cardano numerico</span></span> 
- <span data-ttu-id="d8d84-1389">titulaire de la carte
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1389">cardholder</span></span> 
- <span data-ttu-id="d8d84-1390">titulaires de la carte
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1390">cardholders</span></span> 
- <span data-ttu-id="d8d84-1391">numéro de carte
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1391">cardnumber</span></span> 
- <span data-ttu-id="d8d84-1392">numéros de carte
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1392">cardnumbers</span></span> 
- <span data-ttu-id="d8d84-1393">carta bianca
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1393">carta bianca</span></span> 
- <span data-ttu-id="d8d84-1394">Carta credito
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1394">carta credito</span></span> 
- <span data-ttu-id="d8d84-1395">Carta di credito
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1395">carta di credito</span></span> 
- <span data-ttu-id="d8d84-1396">cartao de credito
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1396">cartao de credito</span></span> 
- <span data-ttu-id="d8d84-1397">cartao de crédito
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1397">cartao de crédito</span></span> 
- <span data-ttu-id="d8d84-1398">cartao de debito
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1398">cartao de debito</span></span> 
- <span data-ttu-id="d8d84-1399">cartao de débito
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1399">cartao de débito</span></span> 
- <span data-ttu-id="d8d84-1400">carte bancaire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1400">carte bancaire</span></span> 
- <span data-ttu-id="d8d84-1401">carte blanche
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1401">carte blanche</span></span> 
- <span data-ttu-id="d8d84-1402">carte bleue
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1402">carte bleue</span></span> 
- <span data-ttu-id="d8d84-1403">carte de credit
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1403">carte de credit</span></span> 
- <span data-ttu-id="d8d84-1404">carte de crédit
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1404">carte de crédit</span></span> 
- <span data-ttu-id="d8d84-1405">carte di credito
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1405">carte di credito</span></span> 
- <span data-ttu-id="d8d84-1406">carteblanche
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1406">carteblanche</span></span> 
- <span data-ttu-id="d8d84-1407">cartão de credito
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1407">cartão de credito</span></span> 
- <span data-ttu-id="d8d84-1408">cartão de crédito
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1408">cartão de crédito</span></span> 
- <span data-ttu-id="d8d84-1409">cartão de debito
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1409">cartão de debito</span></span> 
- <span data-ttu-id="d8d84-1410">cartão de débito
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1410">cartão de débito</span></span> 
- <span data-ttu-id="d8d84-1411">cb
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1411">cb</span></span> 
- <span data-ttu-id="d8d84-1412">ncc
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1412">ccn</span></span> 
- <span data-ttu-id="d8d84-1413">carte de vérification
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1413">check card</span></span> 
- <span data-ttu-id="d8d84-1414">cartes de vérification
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1414">check cards</span></span> 
- <span data-ttu-id="d8d84-1415">carte de vérification
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1415">checkcard</span></span>
- <span data-ttu-id="d8d84-1416">cartes de vérification
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1416">checkcards</span></span> 
- <span data-ttu-id="d8d84-1417">chequekaart
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1417">chequekaart</span></span> 
- <span data-ttu-id="d8d84-1418">cirrus
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1418">cirrus</span></span> 
- <span data-ttu-id="d8d84-1419">cirrus-edc-maestro
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1419">cirrus-edc-maestro</span></span> 
- <span data-ttu-id="d8d84-1420">controlekaart
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1420">controlekaart</span></span> 
- <span data-ttu-id="d8d84-1421">controlekaarten
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1421">controlekaarten</span></span> 
- <span data-ttu-id="d8d84-1422">carte de crédit
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1422">credit card</span></span> 
- <span data-ttu-id="d8d84-1423">cartes de crédit
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1423">credit cards</span></span> 
- <span data-ttu-id="d8d84-1424">carte de crédit
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1424">creditcard</span></span> 
- <span data-ttu-id="d8d84-1425">cartes de crédit
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1425">creditcards</span></span> 
- <span data-ttu-id="d8d84-1426">debetkaart
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1426">debetkaart</span></span> 
- <span data-ttu-id="d8d84-1427">debetkaarten
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1427">debetkaarten</span></span> 
- <span data-ttu-id="d8d84-1428">carte de débit
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1428">debit card</span></span> 
- <span data-ttu-id="d8d84-1429">cartes de débit
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1429">debit cards</span></span> 
- <span data-ttu-id="d8d84-1430">carte de débit
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1430">debitcard</span></span> 
- <span data-ttu-id="d8d84-1431">cartes de débit
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1431">debitcards</span></span> 
- <span data-ttu-id="d8d84-1432">debito automatico
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1432">debito automatico</span></span> 
- <span data-ttu-id="d8d84-1433">diners club
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1433">diners club</span></span> 
- <span data-ttu-id="d8d84-1434">dinersclub
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1434">dinersclub</span></span> 
- <span data-ttu-id="d8d84-1435">découvrir</span><span class="sxs-lookup"><span data-stu-id="d8d84-1435">discover</span></span> 
- <span data-ttu-id="d8d84-1436">discover card
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1436">discover card</span></span> 
- <span data-ttu-id="d8d84-1437">discover cards
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1437">discover cards</span></span> 
- <span data-ttu-id="d8d84-1438">discovercard
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1438">discovercard</span></span> 
- <span data-ttu-id="d8d84-1439">discovercards
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1439">discovercards</span></span> 
- <span data-ttu-id="d8d84-1440">débito automático</span><span class="sxs-lookup"><span data-stu-id="d8d84-1440">débito automático</span></span>
- <span data-ttu-id="d8d84-1441">
edc
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1441">edc</span></span> 
- <span data-ttu-id="d8d84-1442">eigentümername
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1442">eigentümername</span></span> 
- <span data-ttu-id="d8d84-1443">carte de crédit européenne
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1443">european debit card</span></span> 
- <span data-ttu-id="d8d84-1444">hoofdkaart
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1444">hoofdkaart</span></span> 
- <span data-ttu-id="d8d84-1445">hoofdkaarten
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1445">hoofdkaarten</span></span> 
- <span data-ttu-id="d8d84-1446">in viaggio
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1446">in viaggio</span></span> 
- <span data-ttu-id="d8d84-1447">japanese card bureau
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1447">japanese card bureau</span></span> 
- <span data-ttu-id="d8d84-1448">japanse kaartdienst
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1448">japanse kaartdienst</span></span> 
- <span data-ttu-id="d8d84-1449">jcb
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1449">jcb</span></span> 
- <span data-ttu-id="d8d84-1450">kaart
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1450">kaart</span></span> 
- <span data-ttu-id="d8d84-1451">kaart num
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1451">kaart num</span></span> 
- <span data-ttu-id="d8d84-1452">kaartaantal
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1452">kaartaantal</span></span> 
- <span data-ttu-id="d8d84-1453">kaartaantallen
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1453">kaartaantallen</span></span> 
- <span data-ttu-id="d8d84-1454">kaarthouder
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1454">kaarthouder</span></span> 
- <span data-ttu-id="d8d84-1455">kaarthouders
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1455">kaarthouders</span></span> 
- <span data-ttu-id="d8d84-1456">karte
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1456">karte</span></span>  
- <span data-ttu-id="d8d84-1457">karteninhaber
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1457">karteninhaber</span></span> 
- <span data-ttu-id="d8d84-1458">karteninhabers</span><span class="sxs-lookup"><span data-stu-id="d8d84-1458">karteninhabers</span></span>
- <span data-ttu-id="d8d84-1459">
kartennr
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1459">kartennr</span></span> 
- <span data-ttu-id="d8d84-1460">kartennummer</span><span class="sxs-lookup"><span data-stu-id="d8d84-1460">kartennummer</span></span> 
- <span data-ttu-id="d8d84-1461">kreditkarte
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1461">kreditkarte</span></span> 
- <span data-ttu-id="d8d84-1462">kreditkarten-nummer</span><span class="sxs-lookup"><span data-stu-id="d8d84-1462">kreditkarten-nummer</span></span> 
- <span data-ttu-id="d8d84-1463">kreditkarteninhaber
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1463">kreditkarteninhaber</span></span> 
- <span data-ttu-id="d8d84-1464">kreditkarteninstitut
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1464">kreditkarteninstitut</span></span> 
- <span data-ttu-id="d8d84-1465">kreditkartennummer
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1465">kreditkartennummer</span></span> 
- <span data-ttu-id="d8d84-1466">kreditkartentyp
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1466">kreditkartentyp</span></span> 
- <span data-ttu-id="d8d84-1467">maestro
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1467">maestro</span></span> 
- <span data-ttu-id="d8d84-1468">master card
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1468">master card</span></span> 
- <span data-ttu-id="d8d84-1469">master cards
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1469">master cards</span></span> 
- <span data-ttu-id="d8d84-1470">mastercard
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1470">mastercard</span></span> 
- <span data-ttu-id="d8d84-1471">mastercards</span><span class="sxs-lookup"><span data-stu-id="d8d84-1471">mastercards</span></span> 
- <span data-ttu-id="d8d84-1472">MC</span><span class="sxs-lookup"><span data-stu-id="d8d84-1472">mc</span></span> 
- <span data-ttu-id="d8d84-1473">mister cash
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1473">mister cash</span></span> 
- <span data-ttu-id="d8d84-1474">carta n</span><span class="sxs-lookup"><span data-stu-id="d8d84-1474">n carta</span></span> 
- <span data-ttu-id="d8d84-1475">Carta</span><span class="sxs-lookup"><span data-stu-id="d8d84-1475">carta</span></span> 
- <span data-ttu-id="d8d84-1476">Aucun tarjeta de</span><span class="sxs-lookup"><span data-stu-id="d8d84-1476">no de tarjeta</span></span> 
- <span data-ttu-id="d8d84-1477">Aucun cartao</span><span class="sxs-lookup"><span data-stu-id="d8d84-1477">no do cartao</span></span> 
- <span data-ttu-id="d8d84-1478">Aucun cartão</span><span class="sxs-lookup"><span data-stu-id="d8d84-1478">no do cartão</span></span> 
- <span data-ttu-id="d8d84-p117">no. de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="d8d84-p117">no. de tarjeta</span></span> 
- <span data-ttu-id="d8d84-p118">no. do cartao
</span><span class="sxs-lookup"><span data-stu-id="d8d84-p118">no. do cartao</span></span> 
- <span data-ttu-id="d8d84-p119">no. do cartão
</span><span class="sxs-lookup"><span data-stu-id="d8d84-p119">no. do cartão</span></span> 
- <span data-ttu-id="d8d84-1485">nr carta</span><span class="sxs-lookup"><span data-stu-id="d8d84-1485">nr carta</span></span> 
- <span data-ttu-id="d8d84-p120">nr. carta
</span><span class="sxs-lookup"><span data-stu-id="d8d84-p120">nr. carta</span></span> 
- <span data-ttu-id="d8d84-1488">numeri di scheda
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1488">numeri di scheda</span></span> 
- <span data-ttu-id="d8d84-1489">numero carta
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1489">numero carta</span></span> 
- <span data-ttu-id="d8d84-1490">numero de cartao
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1490">numero de cartao</span></span> 
- <span data-ttu-id="d8d84-1491">numero de carte
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1491">numero de carte</span></span> 
- <span data-ttu-id="d8d84-1492">numero de cartão
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1492">numero de cartão</span></span> 
- <span data-ttu-id="d8d84-1493">numero de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1493">numero de tarjeta</span></span>
- <span data-ttu-id="d8d84-1494">numero della carta
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1494">numero della carta</span></span> 
- <span data-ttu-id="d8d84-1495">numero di carta
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1495">numero di carta</span></span> 
- <span data-ttu-id="d8d84-1496">numero di scheda
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1496">numero di scheda</span></span> 
- <span data-ttu-id="d8d84-1497">numero do cartao
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1497">numero do cartao</span></span> 
- <span data-ttu-id="d8d84-1498">numero do cartão
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1498">numero do cartão</span></span> 
- <span data-ttu-id="d8d84-1499">numéro de carte
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1499">numéro de carte</span></span> 
- <span data-ttu-id="d8d84-1500">nº carta
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1500">nº carta</span></span> 
- <span data-ttu-id="d8d84-1501">nº de carte
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1501">nº de carte</span></span> 
- <span data-ttu-id="d8d84-1502">nº de la carte
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1502">nº de la carte</span></span> 
- <span data-ttu-id="d8d84-1503">nº de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1503">nº de tarjeta</span></span> 
- <span data-ttu-id="d8d84-1504">nº do cartao
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1504">nº do cartao</span></span> 
- <span data-ttu-id="d8d84-1505">Nº cartão</span><span class="sxs-lookup"><span data-stu-id="d8d84-1505">nº do cartão</span></span> 
- <span data-ttu-id="d8d84-p121">nº. do cartão
</span><span class="sxs-lookup"><span data-stu-id="d8d84-p121">nº. do cartão</span></span> 
- <span data-ttu-id="d8d84-1508">número de cartao
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1508">número de cartao</span></span> 
- <span data-ttu-id="d8d84-1509">número de cartão
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1509">número de cartão</span></span> 
- <span data-ttu-id="d8d84-1510">número de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1510">número de tarjeta</span></span> 
- <span data-ttu-id="d8d84-1511">número do cartao</span><span class="sxs-lookup"><span data-stu-id="d8d84-1511">número do cartao</span></span> 
- <span data-ttu-id="d8d84-1512">scheda dell’assegno
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1512">scheda dell'assegno</span></span> 
- <span data-ttu-id="d8d84-1513">scheda dell’atmosfera
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1513">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="d8d84-1514">scheda dell’atmosfera
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1514">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="d8d84-1515">scheda della banca
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1515">scheda della banca</span></span> 
- <span data-ttu-id="d8d84-1516">scheda di controllo
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1516">scheda di controllo</span></span> 
- <span data-ttu-id="d8d84-1517">scheda di debito
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1517">scheda di debito</span></span> 
- <span data-ttu-id="d8d84-1518">scheda matrice
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1518">scheda matrice</span></span> 
- <span data-ttu-id="d8d84-1519">schede dell’atmosfera
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1519">schede dell'atmosfera</span></span> 
- <span data-ttu-id="d8d84-1520">schede di controllo
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1520">schede di controllo</span></span> 
- <span data-ttu-id="d8d84-1521">schede di debito
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1521">schede di debito</span></span> 
- <span data-ttu-id="d8d84-1522">schede matrici
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1522">schede matrici</span></span> 
- <span data-ttu-id="d8d84-1523">scoprono la scheda
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1523">scoprono la scheda</span></span> 
- <span data-ttu-id="d8d84-1524">scoprono le schede
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1524">scoprono le schede</span></span> 
- <span data-ttu-id="d8d84-1525">solo
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1525">solo</span></span> 
- <span data-ttu-id="d8d84-1526">supporti di scheda
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1526">supporti di scheda</span></span> 
- <span data-ttu-id="d8d84-1527">supporto di scheda
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1527">supporto di scheda</span></span> 
- <span data-ttu-id="d8d84-1528">commutateur</span><span class="sxs-lookup"><span data-stu-id="d8d84-1528">switch</span></span> 
- <span data-ttu-id="d8d84-1529">tarjeta atm
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1529">tarjeta atm</span></span> 
- <span data-ttu-id="d8d84-1530">tarjeta credito
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1530">tarjeta credito</span></span> 
- <span data-ttu-id="d8d84-1531">tarjeta de atm
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1531">tarjeta de atm</span></span> 
- <span data-ttu-id="d8d84-1532">tarjeta de credito
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1532">tarjeta de credito</span></span> 
- <span data-ttu-id="d8d84-1533">tarjeta de debito
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1533">tarjeta de debito</span></span> 
- <span data-ttu-id="d8d84-1534">tarjeta debito
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1534">tarjeta debito</span></span> 
- <span data-ttu-id="d8d84-1535">tarjeta no
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1535">tarjeta no</span></span>
- <span data-ttu-id="d8d84-1536">tarjetahabiente
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1536">tarjetahabiente</span></span> 
- <span data-ttu-id="d8d84-1537">tipo della scheda
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1537">tipo della scheda</span></span> 
- <span data-ttu-id="d8d84-1538">ufficio giapponese della</span><span class="sxs-lookup"><span data-stu-id="d8d84-1538">ufficio giapponese della</span></span> 
- <span data-ttu-id="d8d84-1539">scheda
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1539">scheda</span></span> 
- <span data-ttu-id="d8d84-1540">v pay
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1540">v pay</span></span> 
- <span data-ttu-id="d8d84-1541">v-paie</span><span class="sxs-lookup"><span data-stu-id="d8d84-1541">v-pay</span></span> 
- <span data-ttu-id="d8d84-1542">visa
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1542">visa</span></span> 
- <span data-ttu-id="d8d84-1543">visa plus
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1543">visa plus</span></span> 
- <span data-ttu-id="d8d84-1544">visa electron
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1544">visa electron</span></span> 
- <span data-ttu-id="d8d84-1545">visto
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1545">visto</span></span> 
- <span data-ttu-id="d8d84-1546">visum
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1546">visum</span></span> 
- <span data-ttu-id="d8d84-1547">vpay
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1547">vpay</span></span>   

#### <a name="keywordcardsecuritytermsdict"></a><span data-ttu-id="d8d84-1548">Keyword_card_security_terms_dict</span><span class="sxs-lookup"><span data-stu-id="d8d84-1548">Keyword_card_security_terms_dict</span></span>

- <span data-ttu-id="d8d84-1549">numéro d’identification de la carte</span><span class="sxs-lookup"><span data-stu-id="d8d84-1549">card identification number</span></span>
- <span data-ttu-id="d8d84-1550">vérification de la carte</span><span class="sxs-lookup"><span data-stu-id="d8d84-1550">card verification</span></span> 
- <span data-ttu-id="d8d84-1551">cardi la verifica
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1551">cardi la verifica</span></span> 
- <span data-ttu-id="d8d84-1552">nic
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1552">cid</span></span> 
- <span data-ttu-id="d8d84-1553">segment de remboursement</span><span class="sxs-lookup"><span data-stu-id="d8d84-1553">cod seg</span></span> 
- <span data-ttu-id="d8d84-1554">remboursement seguranca</span><span class="sxs-lookup"><span data-stu-id="d8d84-1554">cod seguranca</span></span> 
- <span data-ttu-id="d8d84-1555">remboursement segurança</span><span class="sxs-lookup"><span data-stu-id="d8d84-1555">cod segurança</span></span> 
- <span data-ttu-id="d8d84-1556">remboursement sicurezza</span><span class="sxs-lookup"><span data-stu-id="d8d84-1556">cod sicurezza</span></span> 
- <span data-ttu-id="d8d84-p122">cod. seg
</span><span class="sxs-lookup"><span data-stu-id="d8d84-p122">cod. seg</span></span> 
- <span data-ttu-id="d8d84-p123">cod. seguranca
</span><span class="sxs-lookup"><span data-stu-id="d8d84-p123">cod. seguranca</span></span> 
- <span data-ttu-id="d8d84-p124">cod. segurança
</span><span class="sxs-lookup"><span data-stu-id="d8d84-p124">cod. segurança</span></span> 
- <span data-ttu-id="d8d84-p125">cod. sicurezza
</span><span class="sxs-lookup"><span data-stu-id="d8d84-p125">cod. sicurezza</span></span> 
- <span data-ttu-id="d8d84-1565">codice di sicurezza
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1565">codice di sicurezza</span></span> 
- <span data-ttu-id="d8d84-1566">codice di verifica
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1566">codice di verifica</span></span> 
- <span data-ttu-id="d8d84-1567">codigo
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1567">codigo</span></span> 
- <span data-ttu-id="d8d84-1568">codigo de seguranca
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1568">codigo de seguranca</span></span> 
- <span data-ttu-id="d8d84-1569">codigo de segurança
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1569">codigo de segurança</span></span> 
- <span data-ttu-id="d8d84-1570">crittogramma
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1570">crittogramma</span></span> 
- <span data-ttu-id="d8d84-1571">cryptogramme
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1571">cryptogram</span></span> 
- <span data-ttu-id="d8d84-1572">cryptogramme
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1572">cryptogramme</span></span> 
- <span data-ttu-id="d8d84-1573">CV2</span><span class="sxs-lookup"><span data-stu-id="d8d84-1573">cv2</span></span> 
- <span data-ttu-id="d8d84-1574">cvc
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1574">cvc</span></span> 
- <span data-ttu-id="d8d84-1575">CVC2</span><span class="sxs-lookup"><span data-stu-id="d8d84-1575">cvc2</span></span> 
- <span data-ttu-id="d8d84-1576">nvc
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1576">cvn</span></span> 
- <span data-ttu-id="d8d84-1577">cvv
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1577">cvv</span></span> 
- <span data-ttu-id="d8d84-1578">VVC2</span><span class="sxs-lookup"><span data-stu-id="d8d84-1578">cvv2</span></span> 
- <span data-ttu-id="d8d84-1579">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="d8d84-1579">cód seguranca</span></span> 
- <span data-ttu-id="d8d84-1580">cód segurança</span><span class="sxs-lookup"><span data-stu-id="d8d84-1580">cód segurança</span></span> 
- <span data-ttu-id="d8d84-p126">cód. seguranca
</span><span class="sxs-lookup"><span data-stu-id="d8d84-p126">cód. seguranca</span></span> 
- <span data-ttu-id="d8d84-p127">cód. Segurança
</span><span class="sxs-lookup"><span data-stu-id="d8d84-p127">cód. segurança</span></span> 
- <span data-ttu-id="d8d84-1585">código
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1585">código</span></span> 
- <span data-ttu-id="d8d84-1586">código de seguranca
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1586">código de seguranca</span></span> 
- <span data-ttu-id="d8d84-1587">código de segurança
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1587">código de segurança</span></span> 
- <span data-ttu-id="d8d84-1588">de kaart controle
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1588">de kaart controle</span></span> 
- <span data-ttu-id="d8d84-1589">geeft nr suit
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1589">geeft nr uit</span></span> 
- <span data-ttu-id="d8d84-1590">n° d’émission
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1590">issue no</span></span> 
- <span data-ttu-id="d8d84-1591">numéro d’émission
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1591">issue number</span></span> 
- <span data-ttu-id="d8d84-1592">kaartidentificatienummer
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1592">kaartidentificatienummer</span></span> 
- <span data-ttu-id="d8d84-1593">kreditkartenprufnummer
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1593">kreditkartenprufnummer</span></span> 
- <span data-ttu-id="d8d84-1594">kreditkartenprüfnummer
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1594">kreditkartenprüfnummer</span></span> 
- <span data-ttu-id="d8d84-1595">kwestieaantal
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1595">kwestieaantal</span></span> 
- <span data-ttu-id="d8d84-p128">no. dell’edizione
</span><span class="sxs-lookup"><span data-stu-id="d8d84-p128">no. dell'edizione</span></span> 
- <span data-ttu-id="d8d84-p129">no. di sicurezza
</span><span class="sxs-lookup"><span data-stu-id="d8d84-p129">no. di sicurezza</span></span> 
- <span data-ttu-id="d8d84-1600">numéro de sécurité
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1600">numero de securite</span></span> 
- <span data-ttu-id="d8d84-1601">numero de verificacao
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1601">numero de verificacao</span></span> 
- <span data-ttu-id="d8d84-1602">numero dell’edizione
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1602">numero dell'edizione</span></span> 
- <span data-ttu-id="d8d84-1603">numero di identificazione della</span><span class="sxs-lookup"><span data-stu-id="d8d84-1603">numero di identificazione della</span></span> 
- <span data-ttu-id="d8d84-1604">scheda
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1604">scheda</span></span> 
- <span data-ttu-id="d8d84-1605">numero di sicurezza
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1605">numero di sicurezza</span></span> 
- <span data-ttu-id="d8d84-1606">numero van veiligheid
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1606">numero van veiligheid</span></span> 
- <span data-ttu-id="d8d84-1607">numéro de sécurité
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1607">numéro de sécurité</span></span> 
- <span data-ttu-id="d8d84-1608">nº autorizzazione
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1608">nº autorizzazione</span></span> 
- <span data-ttu-id="d8d84-1609">número de verificação
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1609">número de verificação</span></span> 
- <span data-ttu-id="d8d84-1610">perno il blocco
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1610">perno il blocco</span></span> 
- <span data-ttu-id="d8d84-1611">pin block
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1611">pin block</span></span> 
- <span data-ttu-id="d8d84-1612">prufziffer
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1612">prufziffer</span></span> 
- <span data-ttu-id="d8d84-1613">prüfziffer
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1613">prüfziffer</span></span> 
- <span data-ttu-id="d8d84-1614">code de sécurité
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1614">security code</span></span> 
- <span data-ttu-id="d8d84-1615">n° de sécurité
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1615">security no</span></span> 
- <span data-ttu-id="d8d84-1616">numéro de sécurité
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1616">security number</span></span> 
- <span data-ttu-id="d8d84-1617">sicherheits kode
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1617">sicherheits kode</span></span> 
- <span data-ttu-id="d8d84-1618">sicherheitscode
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1618">sicherheitscode</span></span> 
- <span data-ttu-id="d8d84-1619">sicherheitsnummer
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1619">sicherheitsnummer</span></span> 
- <span data-ttu-id="d8d84-1620">speldblok
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1620">speldblok</span></span> 
- <span data-ttu-id="d8d84-1621">veiligheid nr
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1621">veiligheid nr</span></span> 
- <span data-ttu-id="d8d84-1622">veiligheidsaantal
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1622">veiligheidsaantal</span></span> 
- <span data-ttu-id="d8d84-1623">veiligheidscode
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1623">veiligheidscode</span></span> 
- <span data-ttu-id="d8d84-1624">veiligheidsnummer
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1624">veiligheidsnummer</span></span> 
- <span data-ttu-id="d8d84-1625">verfalldatum
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1625">verfalldatum</span></span> 

#### <a name="keywordcardexpirationtermsdict"></a><span data-ttu-id="d8d84-1626">Keyword_card_expiration_terms_dict</span><span class="sxs-lookup"><span data-stu-id="d8d84-1626">Keyword_card_expiration_terms_dict</span></span>

- <span data-ttu-id="d8d84-1627">ablauf
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1627">ablauf</span></span> 
- <span data-ttu-id="d8d84-1628">data de expiracao
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1628">data de expiracao</span></span> 
- <span data-ttu-id="d8d84-1629">data de expiração
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1629">data de expiração</span></span> 
- <span data-ttu-id="d8d84-1630">data del exp
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1630">data del exp</span></span> 
- <span data-ttu-id="d8d84-1631">data di exp
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1631">data di exp</span></span> 
- <span data-ttu-id="d8d84-1632">data di scadenza
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1632">data di scadenza</span></span> 
- <span data-ttu-id="d8d84-1633">data em que expira
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1633">data em que expira</span></span> 
- <span data-ttu-id="d8d84-1634">data scad
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1634">data scad</span></span> 
- <span data-ttu-id="d8d84-1635">data scadenza
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1635">data scadenza</span></span> 
- <span data-ttu-id="d8d84-1636">date de validité
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1636">date de validité</span></span> 
- <span data-ttu-id="d8d84-1637">datum afloop
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1637">datum afloop</span></span> 
- <span data-ttu-id="d8d84-1638">datum van exp
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1638">datum van exp</span></span> 
- <span data-ttu-id="d8d84-1639">de afloop
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1639">de afloop</span></span> 
- <span data-ttu-id="d8d84-1640">espira
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1640">espira</span></span> 
- <span data-ttu-id="d8d84-1641">espira
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1641">espira</span></span> 
- <span data-ttu-id="d8d84-1642">date d’exp
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1642">exp date</span></span> 
- <span data-ttu-id="d8d84-1643">exp datum
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1643">exp datum</span></span> 
- <span data-ttu-id="d8d84-1644">expiration</span><span class="sxs-lookup"><span data-stu-id="d8d84-1644">expiration</span></span> 
- <span data-ttu-id="d8d84-1645">expire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1645">expire</span></span> 
- <span data-ttu-id="d8d84-1646">expire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1646">expires</span></span> 
- <span data-ttu-id="d8d84-1647">expiration
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1647">expiry</span></span> 
- <span data-ttu-id="d8d84-1648">fecha de expiracion
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1648">fecha de expiracion</span></span> 
- <span data-ttu-id="d8d84-1649">fecha de venc
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1649">fecha de venc</span></span> 
- <span data-ttu-id="d8d84-1650">gultig bis
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1650">gultig bis</span></span> 
- <span data-ttu-id="d8d84-1651">gultigkeitsdatum
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1651">gultigkeitsdatum</span></span> 
- <span data-ttu-id="d8d84-1652">gültig bis
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1652">gültig bis</span></span> 
- <span data-ttu-id="d8d84-1653">gültigkeitsdatum
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1653">gültigkeitsdatum</span></span> 
- <span data-ttu-id="d8d84-1654">la scadenza
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1654">la scadenza</span></span> 
- <span data-ttu-id="d8d84-1655">scadenza
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1655">scadenza</span></span> 
- <span data-ttu-id="d8d84-1656">valable
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1656">valable</span></span> 
- <span data-ttu-id="d8d84-1657">validade
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1657">validade</span></span> 
- <span data-ttu-id="d8d84-1658">valido hasta
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1658">valido hasta</span></span> 
- <span data-ttu-id="d8d84-1659">valor
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1659">valor</span></span> 
- <span data-ttu-id="d8d84-1660">venc
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1660">venc</span></span> 
- <span data-ttu-id="d8d84-1661">vencimento
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1661">vencimento</span></span> 
- <span data-ttu-id="d8d84-1662">vencimiento
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1662">vencimiento</span></span> 
- <span data-ttu-id="d8d84-1663">verloopt
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1663">verloopt</span></span> 
- <span data-ttu-id="d8d84-1664">vervaldag
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1664">vervaldag</span></span> 
- <span data-ttu-id="d8d84-1665">vervaldatum
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1665">vervaldatum</span></span> 
- <span data-ttu-id="d8d84-1666">vto
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1666">vto</span></span> 
- <span data-ttu-id="d8d84-1667">válido hasta
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1667">válido hasta</span></span> 
   
## <a name="eu-drivers-license-number"></a><span data-ttu-id="d8d84-1668">Numéro de permis de conduire l’Union européenne</span><span class="sxs-lookup"><span data-stu-id="d8d84-1668">EU Driver's License Number</span></span>

<span data-ttu-id="d8d84-1669">Pour plus d’informations, voir le [type d’informations sensibles numéro de permis de conduire l’Union européenne](eu-driver-s-license-number.md).</span><span class="sxs-lookup"><span data-stu-id="d8d84-1669">To learn more, see [EU Driver's License Number sensitive information type](eu-driver-s-license-number.md).</span></span>
  
## <a name="eu-national-identification-number"></a><span data-ttu-id="d8d84-1670">Numéro d’Identification nationales de l’UE</span><span class="sxs-lookup"><span data-stu-id="d8d84-1670">EU National Identification Number</span></span>

<span data-ttu-id="d8d84-1671">Pour plus d’informations, voir le [type d’informations sensibles National numéro d’Identification de l’UE](eu-national-identification-number.md).</span><span class="sxs-lookup"><span data-stu-id="d8d84-1671">To learn more, see [EU National Identification Number sensitive information type](eu-national-identification-number.md).</span></span>
  
## <a name="eu-passport-number"></a><span data-ttu-id="d8d84-1672">Numéro de passeport UE</span><span class="sxs-lookup"><span data-stu-id="d8d84-1672">EU Passport Number</span></span>

<span data-ttu-id="d8d84-1673">Pour plus d’informations, voir le [numéro de passeport UE type d’informations sensibles](eu-passport-number.md).</span><span class="sxs-lookup"><span data-stu-id="d8d84-1673">To learn more, see [EU Passport Number sensitive information type](eu-passport-number.md).</span></span>
  
## <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="d8d84-1674">ID de numéro de sécurité sociale de l’Union européenne ou équivalent</span><span class="sxs-lookup"><span data-stu-id="d8d84-1674">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="d8d84-1675">Pour plus d’informations, voir [numéro de sécurité sociale de l’Union européenne ou type d’informations sensibles ID équivalente](eu-social-security-number-or-equivalent-id.md).</span><span class="sxs-lookup"><span data-stu-id="d8d84-1675">To learn more, see [EU Social Security Number or Equivalent ID sensitive information type](eu-social-security-number-or-equivalent-id.md).</span></span>
  
## <a name="eu-tax-identification-number"></a><span data-ttu-id="d8d84-1676">Numéro d’Identification de l’UE taxe</span><span class="sxs-lookup"><span data-stu-id="d8d84-1676">EU Tax Identification Number</span></span>

<span data-ttu-id="d8d84-1677">Pour plus d’informations, voir [type d’informations sensibles numéro d’Identification de taxe de l’UE](eu-tax-identification-number.md).</span><span class="sxs-lookup"><span data-stu-id="d8d84-1677">To learn more, see [EU Tax Identification Number sensitive information type](eu-tax-identification-number.md).</span></span>
  
## <a name="finland-national-id"></a><span data-ttu-id="d8d84-1678">ID national finlandais</span><span class="sxs-lookup"><span data-stu-id="d8d84-1678">Finland National ID</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-1679">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-1679">Format</span></span>

<span data-ttu-id="d8d84-1680">Six chiffres plus un caractère indiquant un siècle plus trois chiffres plus un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-1680">Six digits plus a character indicating a century plus three digits plus a check digit</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-1681">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-1681">Pattern</span></span>

<span data-ttu-id="d8d84-1682">Le modèle doit inclure tous les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="d8d84-1682">Pattern must include all of the following:</span></span>
- <span data-ttu-id="d8d84-1683">Six chiffres au format JJMMAA qui représentent la date de naissance</span><span class="sxs-lookup"><span data-stu-id="d8d84-1683">Six digits in the format format DDMMYY which are a date of birth</span></span> 
- <span data-ttu-id="d8d84-1684">Marqueur de siècle (soit « - », « + » ou « a »)</span><span class="sxs-lookup"><span data-stu-id="d8d84-1684">Century marker (either '-', '+' or 'a')</span></span> 
- <span data-ttu-id="d8d84-1685">Numéro d’identification personnel à trois chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-1685">Three-digit personal identification number</span></span> 
- <span data-ttu-id="d8d84-1686">Un chiffre ou une lettre (ne respectant pas la casse) de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-1686">A digit or letter (case insensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-1687">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-1687">Checksum</span></span>

<span data-ttu-id="d8d84-1688">Oui</span><span class="sxs-lookup"><span data-stu-id="d8d84-1688">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-1689">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-1689">Definition</span></span>

<span data-ttu-id="d8d84-1690">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-1690">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-1691">La fonction Func_finnish_national_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1691">The function Func_finnish_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-1692">Un mot clé figurant dans la liste Keyword_finnish_national_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1692">A keyword from Keyword_finnish_national_id is found.</span></span>
- <span data-ttu-id="d8d84-1693">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1693">The checksum passes.</span></span>

```
<!-- Finnish National ID-->
<Entity id="338FD995-4CB5-4F87-AD35-79BD1DD926C1" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finnish_national_id" />
          <Match idRef="Keyword_finnish_national_id" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8d84-1694">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-1694">Keywords</span></span>

- <span data-ttu-id="d8d84-1695">Keyword_finnish_national_id</span><span class="sxs-lookup"><span data-stu-id="d8d84-1695">Keyword_finnish_national_id</span></span>
- <span data-ttu-id="d8d84-1696">

Sosiaaliturvatunnus</span><span class="sxs-lookup"><span data-stu-id="d8d84-1696">Sosiaaliturvatunnus</span></span>
- <span data-ttu-id="d8d84-1697">SOTU Henkilötunnus HETU</span><span class="sxs-lookup"><span data-stu-id="d8d84-1697">SOTU Henkilötunnus HETU</span></span>
- <span data-ttu-id="d8d84-1698">Personbeteckning</span><span class="sxs-lookup"><span data-stu-id="d8d84-1698">Personbeteckning</span></span>
- <span data-ttu-id="d8d84-1699">Personnummer</span><span class="sxs-lookup"><span data-stu-id="d8d84-1699">Personnummer</span></span>
   
## <a name="finland-passport-number"></a><span data-ttu-id="d8d84-1700">Numéro de passeport finlandais</span><span class="sxs-lookup"><span data-stu-id="d8d84-1700">Finland Passport Number</span></span>

<span data-ttu-id="d8d84-p130">Combinaison de lettres et de chiffres motif combinaison de lettres et chiffres de neuf neuf de format : stratégie de somme de contrôle non définition A DLP deux lettres (non sensible à la casse) sept chiffres est 75 % convaincu que ce type d’informations sensibles a été détecté si, dans un proximité de 300 caractères : l’expression régulière Regex_finland_passport_number recherche de contenu qui correspond au modèle. Un mot clé à partir de Keyword_finland_passport_number est trouvé. <!-- Finland Passport Number --> 
 <Entity id="d1685ac3-1d3a-40f8-8198-32ef5669c7a5" recommendedConfidence="75" patternsProximity="300"> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_finland_passport_number"/> <Match idRef="Keyword_finland_passport_number"/> </Pattern> 
 </Entity> REUSSITE de passeport Keyword_finland_passport_number mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-p130">Format Combination of nine letters and digits Pattern Combination of nine letters and digits: Two letters (not case sensitive) Seven digits Checksum No Definition A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_finland_passport_number finds content that matches the pattern. A keyword from Keyword_finland_passport_number is found. <!-- Finland Passport Number -->
<Entity id="d1685ac3-1d3a-40f8-8198-32ef5669c7a5" recommendedConfidence="75" patternsProximity="300"> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_finland_passport_number"/> <Match idRef="Keyword_finland_passport_number"/> </Pattern>
</Entity> Keywords Keyword_finland_passport_number Passport Passi</span></span>
   
## <a name="france-drivers-license-number"></a><span data-ttu-id="d8d84-1705">Numéro de permis de conduire France</span><span class="sxs-lookup"><span data-stu-id="d8d84-1705">France Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-1706">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-1706">Format</span></span>

<span data-ttu-id="d8d84-1707">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-1707">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-1708">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-1708">Pattern</span></span>

<span data-ttu-id="d8d84-1709">12 chiffres avec validation pour écarter les modèles similaires, comme les numéros de téléphone français</span><span class="sxs-lookup"><span data-stu-id="d8d84-1709">12 digits with validation to discount similar patterns such as French telephone numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-1710">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-1710">Checksum</span></span>

<span data-ttu-id="d8d84-1711">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-1711">No</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-1712">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-1712">Definition</span></span>

<span data-ttu-id="d8d84-1713">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-1713">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-1714">La fonction Func_french_drivers_license trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1714">The function Func_french_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-1715">Au moins une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="d8d84-1715">At least one of the following is true:</span></span>
- <span data-ttu-id="d8d84-1716">Un mot clé figurant dans la liste Keyword_french_drivers_license est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1716">A keyword from Keyword_french_drivers_license is found.</span></span>
- <span data-ttu-id="d8d84-1717">La fonction Func_eu_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1717">The function Func_eu_date finds a date in the right date format.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-1718">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-1718">Keywords</span></span>

#### <a name="keywordfrenchdriverslicense"></a><span data-ttu-id="d8d84-1719">Keyword_french_drivers_license</span><span class="sxs-lookup"><span data-stu-id="d8d84-1719">Keyword_french_drivers_license</span></span>

- <span data-ttu-id="d8d84-1720">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="d8d84-1720">drivers licence</span></span>
- <span data-ttu-id="d8d84-1721">drivers license</span><span class="sxs-lookup"><span data-stu-id="d8d84-1721">drivers license</span></span>
- <span data-ttu-id="d8d84-1722">permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1722">driving licence</span></span>
- <span data-ttu-id="d8d84-1723">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="d8d84-1723">driving license</span></span>
- <span data-ttu-id="d8d84-1724">
permis de conduire</span><span class="sxs-lookup"><span data-stu-id="d8d84-1724">permis de conduire</span></span>
- <span data-ttu-id="d8d84-1725">
numéro de permis</span><span class="sxs-lookup"><span data-stu-id="d8d84-1725">licence number</span></span>
- <span data-ttu-id="d8d84-1726">
numéro de permis</span><span class="sxs-lookup"><span data-stu-id="d8d84-1726">license number</span></span>
- <span data-ttu-id="d8d84-1727">
numéros de permis</span><span class="sxs-lookup"><span data-stu-id="d8d84-1727">licence numbers</span></span>
- <span data-ttu-id="d8d84-1728">

numéros de permis</span><span class="sxs-lookup"><span data-stu-id="d8d84-1728">license numbers</span></span>

## <a name="france-national-id-card-cni"></a><span data-ttu-id="d8d84-1729">Carte nationale d'identité (CNI) France</span><span class="sxs-lookup"><span data-stu-id="d8d84-1729">France National ID Card (CNI)</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-1730">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-1730">Format</span></span>

<span data-ttu-id="d8d84-1731">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-1731">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-1732">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-1732">Pattern</span></span>

<span data-ttu-id="d8d84-1733">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-1733">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-1734">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-1734">Checksum</span></span>

<span data-ttu-id="d8d84-1735">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-1735">No</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-1736">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-1736">Definition</span></span>

<span data-ttu-id="d8d84-1737">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-1737">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-1738">L’expression régulière Regex_france_cni trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1738">The regular expression Regex_france_cni finds content that matches the pattern.</span></span>

```
<!-- France CNI -->
<Entity id="f741ac74-1bc0-4665-b69b-f0c7f927c0c4" patternsProximity="300" recommendedConfidence="65">
  <Pattern confidenceLevel="65">
        <IdMatch idRef="Regex_france_cni" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8d84-1739">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-1739">Keywords</span></span>

<span data-ttu-id="d8d84-1740">Aucune</span><span class="sxs-lookup"><span data-stu-id="d8d84-1740">None</span></span>
   
## <a name="france-passport-number"></a><span data-ttu-id="d8d84-1741">Numéro de passeport France</span><span class="sxs-lookup"><span data-stu-id="d8d84-1741">France Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-1742">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-1742">Format</span></span>

<span data-ttu-id="d8d84-1743">Neuf chiffres et lettres</span><span class="sxs-lookup"><span data-stu-id="d8d84-1743">Nine digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-1744">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-1744">Pattern</span></span>

<span data-ttu-id="d8d84-1745">Neuf chiffres et lettres :</span><span class="sxs-lookup"><span data-stu-id="d8d84-1745">Nine digits and letters:</span></span>
- <span data-ttu-id="d8d84-1746">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-1746">Two digits</span></span> 
- <span data-ttu-id="d8d84-1747">Deux lettres (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="d8d84-1747">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="d8d84-1748">Cinq chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-1748">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-1749">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-1749">Checksum</span></span>

<span data-ttu-id="d8d84-1750">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-1750">No</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-1751">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-1751">Definition</span></span>

<span data-ttu-id="d8d84-1752">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-1752">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-1753">La fonction Func_fr_passport trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1753">The function Func_fr_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-1754">Un mot clé figurant dans la liste Keyword_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1754">A keyword from Keyword_passport is found.</span></span>

```
<!-- France Passport Number -->
<Entity id="3008b884-8c8c-4cd8-a289-99f34fc7ff5d" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_fr_passport" />
        <Match idRef="Keyword_passport" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8d84-1755">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-1755">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="d8d84-1756">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="d8d84-1756">Keyword_passport</span></span>

- <span data-ttu-id="d8d84-1757">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8d84-1757">Passport Number</span></span>
- <span data-ttu-id="d8d84-1758">
N° de passeport</span><span class="sxs-lookup"><span data-stu-id="d8d84-1758">Passport No</span></span>
- <span data-ttu-id="d8d84-1759"># Passeport
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1759">Passport #</span></span>
- <span data-ttu-id="d8d84-1760">#Passeport
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1760">Passport#</span></span>
- <span data-ttu-id="d8d84-1761">IDPassport</span><span class="sxs-lookup"><span data-stu-id="d8d84-1761">PassportID</span></span>
- <span data-ttu-id="d8d84-1762">n° passeport
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1762">Passportno</span></span>
- <span data-ttu-id="d8d84-1763">numéropasseport
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1763">passportnumber</span></span>
- <span data-ttu-id="d8d84-1764">パスポート</span><span class="sxs-lookup"><span data-stu-id="d8d84-1764">パスポート</span></span>
- <span data-ttu-id="d8d84-1765">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1765">パスポート番号</span></span>
- <span data-ttu-id="d8d84-1766">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1766">パスポートのNum</span></span>
- <span data-ttu-id="d8d84-1767">
パスポート＃
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1767">パスポート ＃</span></span> 
- <span data-ttu-id="d8d84-1768">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8d84-1768">Numéro de passeport</span></span>
- <span data-ttu-id="d8d84-1769">
Passeport n°</span><span class="sxs-lookup"><span data-stu-id="d8d84-1769">Passeport n °</span></span>
- <span data-ttu-id="d8d84-1770">Passeport numéro
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1770">Passeport Non</span></span>
- <span data-ttu-id="d8d84-1771"># Passeport
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1771">Passeport #</span></span>
- <span data-ttu-id="d8d84-1772">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1772">Passeport#</span></span>
- <span data-ttu-id="d8d84-1773">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="d8d84-1773">PasseportNon</span></span>
- <span data-ttu-id="d8d84-1774">

Passeportn °</span><span class="sxs-lookup"><span data-stu-id="d8d84-1774">Passeportn °</span></span>

      
## <a name="france-social-security-number-insee"></a><span data-ttu-id="d8d84-1775">Numéro de sécurité sociale (INSEE) France</span><span class="sxs-lookup"><span data-stu-id="d8d84-1775">France Social Security Number (INSEE)</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-1776">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-1776">Format</span></span>

<span data-ttu-id="d8d84-1777">15 chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-1777">15 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-1778">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-1778">Pattern</span></span>

<span data-ttu-id="d8d84-1779">Doit correspondre à l’un des deux modèles suivants :</span><span class="sxs-lookup"><span data-stu-id="d8d84-1779">Must match one of two patterns:</span></span>
- <span data-ttu-id="d8d84-1780">13 chiffres suivis d’un espace suivi de deux chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-1780">13 digits followed by a space followed by two digits</span></span><br/>
<span data-ttu-id="d8d84-1781">ou</span><span class="sxs-lookup"><span data-stu-id="d8d84-1781">or</span></span>
- <span data-ttu-id="d8d84-1782">15 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="d8d84-1782">15 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-1783">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-1783">Checksum</span></span>

<span data-ttu-id="d8d84-1784">Oui</span><span class="sxs-lookup"><span data-stu-id="d8d84-1784">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-1785">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-1785">Definition</span></span>

<span data-ttu-id="d8d84-1786">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 95 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-1786">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-1787">La fonction Func_french_insee ou Func_fr_insee recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1787">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-1788">Un mot clé figurant dans la liste Keyword_fr_insee est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1788">A keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="d8d84-1789">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1789">The checksum passes.</span></span>

<span data-ttu-id="d8d84-1790">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-1790">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-1791">La fonction Func_french_insee ou Func_fr_insee recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1791">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-1792">Aucun mot clé figurant dans la liste Keyword_fr_insee n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1792">No keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="d8d84-1793">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1793">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-1794">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-1794">Keywords</span></span>

#### <a name="keywordfrinsee"></a><span data-ttu-id="d8d84-1795">Keyword_fr_insee</span><span class="sxs-lookup"><span data-stu-id="d8d84-1795">Keyword_fr_insee</span></span>

- <span data-ttu-id="d8d84-1796">insee</span><span class="sxs-lookup"><span data-stu-id="d8d84-1796">insee</span></span>
- <span data-ttu-id="d8d84-1797">
securité sociale</span><span class="sxs-lookup"><span data-stu-id="d8d84-1797">securité sociale</span></span>
- <span data-ttu-id="d8d84-1798">
securite sociale</span><span class="sxs-lookup"><span data-stu-id="d8d84-1798">securite sociale</span></span>
- <span data-ttu-id="d8d84-1799">
id national</span><span class="sxs-lookup"><span data-stu-id="d8d84-1799">national id</span></span>
- <span data-ttu-id="d8d84-1800">
numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="d8d84-1800">national identification</span></span>
- <span data-ttu-id="d8d84-1801">
numéro d’identité</span><span class="sxs-lookup"><span data-stu-id="d8d84-1801">numéro d'identité</span></span>
- <span data-ttu-id="d8d84-1802">Aucun d'identité</span><span class="sxs-lookup"><span data-stu-id="d8d84-1802">no d'identité</span></span>
- <span data-ttu-id="d8d84-p131">
n° d’identité</span><span class="sxs-lookup"><span data-stu-id="d8d84-p131">no. d'identité</span></span>
- <span data-ttu-id="d8d84-1805">
numéro d’identité</span><span class="sxs-lookup"><span data-stu-id="d8d84-1805">numero d'identite</span></span>
- <span data-ttu-id="d8d84-1806">Aucun d'identite</span><span class="sxs-lookup"><span data-stu-id="d8d84-1806">no d'identite</span></span>
- <span data-ttu-id="d8d84-p132">
n° d’identité</span><span class="sxs-lookup"><span data-stu-id="d8d84-p132">no. d'identite</span></span>
- <span data-ttu-id="d8d84-1809">numéro de sécurité sociale
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1809">social security number</span></span>
- <span data-ttu-id="d8d84-1810">
code de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="d8d84-1810">social security code</span></span>
- <span data-ttu-id="d8d84-1811">numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="d8d84-1811">social insurance number</span></span>
- <span data-ttu-id="d8d84-1812">
le numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="d8d84-1812">le numéro d'identification nationale</span></span>
- <span data-ttu-id="d8d84-1813">
d’identité nationale</span><span class="sxs-lookup"><span data-stu-id="d8d84-1813">d'identité nationale</span></span>
- <span data-ttu-id="d8d84-1814">
numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="d8d84-1814">numéro de sécurité sociale</span></span>
- <span data-ttu-id="d8d84-1815">
le code de la sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="d8d84-1815">le code de la sécurité sociale</span></span>
- <span data-ttu-id="d8d84-1816">
numéro d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="d8d84-1816">numéro d'assurance sociale</span></span>
- <span data-ttu-id="d8d84-1817">
numéro de sécu</span><span class="sxs-lookup"><span data-stu-id="d8d84-1817">numéro de sécu</span></span>
- <span data-ttu-id="d8d84-1818">
code sécu
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1818">code sécu</span></span> 
   
## <a name="german-drivers-license-number"></a><span data-ttu-id="d8d84-1819">Numéro de permis de conduire Allemagne</span><span class="sxs-lookup"><span data-stu-id="d8d84-1819">German Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-1820">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-1820">Format</span></span>

<span data-ttu-id="d8d84-1821">Combinaison de 11 chiffres et lettres</span><span class="sxs-lookup"><span data-stu-id="d8d84-1821">Combination of 11 digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-1822">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-1822">Pattern</span></span>

<span data-ttu-id="d8d84-1823">11 chiffres et lettres (ne respectent pas la casse) :</span><span class="sxs-lookup"><span data-stu-id="d8d84-1823">11 digits and letters (not case sensitive):</span></span>
- <span data-ttu-id="d8d84-1824">Un chiffre ou une lettre</span><span class="sxs-lookup"><span data-stu-id="d8d84-1824">A digit or letter</span></span> 
- <span data-ttu-id="d8d84-1825">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-1825">Two digits</span></span> 
- <span data-ttu-id="d8d84-1826">Six chiffres ou lettres</span><span class="sxs-lookup"><span data-stu-id="d8d84-1826">Six digits or letters</span></span> 
- <span data-ttu-id="d8d84-1827">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="d8d84-1827">A digit</span></span> 
- <span data-ttu-id="d8d84-1828">Un chiffre ou une lettre</span><span class="sxs-lookup"><span data-stu-id="d8d84-1828">A digit or letter</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-1829">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-1829">Checksum</span></span>

<span data-ttu-id="d8d84-1830">Oui</span><span class="sxs-lookup"><span data-stu-id="d8d84-1830">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-1831">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-1831">Definition</span></span>

<span data-ttu-id="d8d84-1832">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-1832">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-1833">La fonction Func_german_drivers_license trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1833">The function Func_german_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-1834">Au moins une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="d8d84-1834">At least one of the following is true:</span></span>
    - <span data-ttu-id="d8d84-1835">Un mot clé figurant dans la liste Keyword_german_drivers_license_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1835">A keyword from Keyword_german_drivers_license_number is found.</span></span>
    - <span data-ttu-id="d8d84-1836">Un mot clé figurant dans la liste Keyword_german_drivers_license_collaborative est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1836">A keyword from Keyword_german_drivers_license_collaborative is found.</span></span>
    - <span data-ttu-id="d8d84-1837">Un mot clé figurant dans la liste Keyword_german_drivers_license est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1837">A keyword from Keyword_german_drivers_license is found.</span></span>
- <span data-ttu-id="d8d84-1838">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1838">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-1839">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-1839">Keywords</span></span>

#### <a name="keywordgermandriverslicensenumber"></a><span data-ttu-id="d8d84-1840">Keyword_german_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="d8d84-1840">Keyword_german_drivers_license_number</span></span>

- <span data-ttu-id="d8d84-1841">Führerschein</span><span class="sxs-lookup"><span data-stu-id="d8d84-1841">Führerschein</span></span>
- <span data-ttu-id="d8d84-1842">
Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="d8d84-1842">Fuhrerschein</span></span>
- <span data-ttu-id="d8d84-1843">Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="d8d84-1843">Fuehrerschein</span></span>
- <span data-ttu-id="d8d84-1844">
Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="d8d84-1844">Führerscheinnummer</span></span>
- <span data-ttu-id="d8d84-1845">
Fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="d8d84-1845">Fuhrerscheinnummer</span></span>
- <span data-ttu-id="d8d84-1846">
Fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="d8d84-1846">Fuehrerscheinnummer</span></span>
- <span data-ttu-id="d8d84-1847">
Führerschein-
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1847">Führerschein-</span></span> 
- <span data-ttu-id="d8d84-1848">Fuhrerschein-
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1848">Fuhrerschein-</span></span> 
- <span data-ttu-id="d8d84-1849">Fuehrerschein-
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1849">Fuehrerschein-</span></span> 
- <span data-ttu-id="d8d84-1850">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="d8d84-1850">FührerscheinnummerNr</span></span>
- <span data-ttu-id="d8d84-1851">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="d8d84-1851">FuhrerscheinnummerNr</span></span>
- <span data-ttu-id="d8d84-1852">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="d8d84-1852">FuehrerscheinnummerNr</span></span>
- <span data-ttu-id="d8d84-1853">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="d8d84-1853">FührerscheinnummerKlasse</span></span>
- <span data-ttu-id="d8d84-1854">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="d8d84-1854">FuhrerscheinnummerKlasse</span></span>
- <span data-ttu-id="d8d84-1855">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="d8d84-1855">FuehrerscheinnummerKlasse</span></span>
- <span data-ttu-id="d8d84-1856">Führerschein - Nr
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1856">Führerschein- Nr</span></span>
- <span data-ttu-id="d8d84-1857">Fuhrerschein - Nr
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1857">Fuhrerschein- Nr</span></span>
- <span data-ttu-id="d8d84-1858">Fuehrerschein - Nr
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1858">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="d8d84-1859">Führerschein - Klasse
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1859">Führerschein- Klasse</span></span> 
- <span data-ttu-id="d8d84-1860">Fuhrerschein - Klasse
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1860">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="d8d84-1861">Fuehrerschein - Klasse</span><span class="sxs-lookup"><span data-stu-id="d8d84-1861">Fuehrerschein- Klasse</span></span>
- <span data-ttu-id="d8d84-1862">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="d8d84-1862">FührerscheinnummerNr</span></span> 
- <span data-ttu-id="d8d84-1863">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="d8d84-1863">FuhrerscheinnummerNr</span></span> 
- <span data-ttu-id="d8d84-1864">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="d8d84-1864">FuehrerscheinnummerNr</span></span> 
- <span data-ttu-id="d8d84-1865">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="d8d84-1865">FührerscheinnummerKlasse</span></span> 
- <span data-ttu-id="d8d84-1866">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="d8d84-1866">FuhrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="d8d84-1867">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="d8d84-1867">FuehrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="d8d84-1868">Führerschein - Nr
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1868">Führerschein- Nr</span></span> 
- <span data-ttu-id="d8d84-1869">Fuhrerschein - Nr
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1869">Fuhrerschein- Nr</span></span> 
- <span data-ttu-id="d8d84-1870">Fuehrerschein - Nr
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1870">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="d8d84-1871">Führerschein - Klasse
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1871">Führerschein- Klasse</span></span> 
- <span data-ttu-id="d8d84-1872">Fuhrerschein - Klasse
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1872">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="d8d84-1873">Fuehrerschein - Klasse</span><span class="sxs-lookup"><span data-stu-id="d8d84-1873">Fuehrerschein- Klasse</span></span> 
- <span data-ttu-id="d8d84-1874">PC</span><span class="sxs-lookup"><span data-stu-id="d8d84-1874">DL</span></span> 
- <span data-ttu-id="d8d84-1875">PC</span><span class="sxs-lookup"><span data-stu-id="d8d84-1875">DLS</span></span>
- <span data-ttu-id="d8d84-1876">
Permis conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1876">Driv Lic</span></span> 
- <span data-ttu-id="d8d84-1877">Permis conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1877">Driv Licen</span></span> 
- <span data-ttu-id="d8d84-1878">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="d8d84-1878">Driv License</span></span>
- <span data-ttu-id="d8d84-1879">
Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1879">Driv Licenses</span></span> 
- <span data-ttu-id="d8d84-1880">Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1880">Driv Licence</span></span> 
- <span data-ttu-id="d8d84-1881">Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1881">Driv Licences</span></span> 
- <span data-ttu-id="d8d84-1882">Permis conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1882">Driv Lic</span></span> 
- <span data-ttu-id="d8d84-1883">Permis conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1883">Driver Licen</span></span> 
- <span data-ttu-id="d8d84-1884">Conduire</span><span class="sxs-lookup"><span data-stu-id="d8d84-1884">Driver License</span></span> 
- <span data-ttu-id="d8d84-1885">Licences de pilote</span><span class="sxs-lookup"><span data-stu-id="d8d84-1885">Driver Licenses</span></span> 
- <span data-ttu-id="d8d84-1886">Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1886">Driver Licence</span></span> 
- <span data-ttu-id="d8d84-1887">Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1887">Driver Licences</span></span> 
- <span data-ttu-id="d8d84-1888">Lic pilotes</span><span class="sxs-lookup"><span data-stu-id="d8d84-1888">Drivers Lic</span></span> 
- <span data-ttu-id="d8d84-1889">Licen pilotes</span><span class="sxs-lookup"><span data-stu-id="d8d84-1889">Drivers Licen</span></span> 
- <span data-ttu-id="d8d84-1890">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="d8d84-1890">Drivers License</span></span> 
- <span data-ttu-id="d8d84-1891">Licences de pilotes</span><span class="sxs-lookup"><span data-stu-id="d8d84-1891">Drivers Licenses</span></span> 
- <span data-ttu-id="d8d84-1892">Certificat de pilotes</span><span class="sxs-lookup"><span data-stu-id="d8d84-1892">Drivers Licence</span></span> 
- <span data-ttu-id="d8d84-1893">Certificats de pilotes</span><span class="sxs-lookup"><span data-stu-id="d8d84-1893">Drivers Licences</span></span> 
- <span data-ttu-id="d8d84-1894">Lic du pilote</span><span class="sxs-lookup"><span data-stu-id="d8d84-1894">Driver's Lic</span></span> 
- <span data-ttu-id="d8d84-1895">Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1895">Driver's Licen</span></span> 
- <span data-ttu-id="d8d84-1896">Conduire permis de</span><span class="sxs-lookup"><span data-stu-id="d8d84-1896">Driver's License</span></span> 
- <span data-ttu-id="d8d84-1897">Conduire permis de</span><span class="sxs-lookup"><span data-stu-id="d8d84-1897">Driver's Licenses</span></span> 
- <span data-ttu-id="d8d84-1898">Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1898">Driver's Licence</span></span> 
- <span data-ttu-id="d8d84-1899">Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1899">Driver's Licences</span></span> 
- <span data-ttu-id="d8d84-1900">Permis conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1900">Driving Lic</span></span> 
- <span data-ttu-id="d8d84-1901">Permis conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1901">Driving Licen</span></span> 
- <span data-ttu-id="d8d84-1902">Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1902">Driving License</span></span> 
- <span data-ttu-id="d8d84-1903">Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1903">Driving Licenses</span></span> 
- <span data-ttu-id="d8d84-1904">Permis de conduire

</span><span class="sxs-lookup"><span data-stu-id="d8d84-1904">Driving Licence</span></span> 
- <span data-ttu-id="d8d84-1905">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="d8d84-1905">Driving Licences</span></span>

#### <a name="keywordgermandriverslicensecollaborative"></a><span data-ttu-id="d8d84-1906">Keyword_german_drivers_license_collaborative</span><span class="sxs-lookup"><span data-stu-id="d8d84-1906">Keyword_german_drivers_license_collaborative</span></span>

- <span data-ttu-id="d8d84-1907">
Nr-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1907">Nr-Führerschein</span></span> 
- <span data-ttu-id="d8d84-1908">Nr-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1908">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="d8d84-1909">Nr-Fuehrerschein
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1909">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="d8d84-1910">No-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1910">No-Führerschein</span></span> 
- <span data-ttu-id="d8d84-1911">No-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1911">No-Fuhrerschein</span></span> 
- <span data-ttu-id="d8d84-1912">No-Fuehrerschein
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1912">No-Fuehrerschein</span></span> 
- <span data-ttu-id="d8d84-1913">N-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1913">N-Führerschein</span></span> 
- <span data-ttu-id="d8d84-1914">N-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1914">N-Fuhrerschein</span></span> 
- <span data-ttu-id="d8d84-1915">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="d8d84-1915">N-Fuehrerschein</span></span>
- <span data-ttu-id="d8d84-1916">
Nr-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1916">Nr-Führerschein</span></span> 
- <span data-ttu-id="d8d84-1917">Nr-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1917">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="d8d84-1918">Nr-Fuehrerschein
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1918">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="d8d84-1919">No-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1919">No-Führerschein</span></span> 
- <span data-ttu-id="d8d84-1920">No-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1920">No-Fuhrerschein</span></span> 
- <span data-ttu-id="d8d84-1921">No-Fuehrerschein
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1921">No-Fuehrerschein</span></span> 
- <span data-ttu-id="d8d84-1922">N-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1922">N-Führerschein</span></span> 
- <span data-ttu-id="d8d84-1923">N-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1923">N-Fuhrerschein</span></span> 
- <span data-ttu-id="d8d84-1924">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="d8d84-1924">N-Fuehrerschein</span></span> 

#### <a name="keywordgermandriverslicense"></a><span data-ttu-id="d8d84-1925">Keyword_german_drivers_license</span><span class="sxs-lookup"><span data-stu-id="d8d84-1925">Keyword_german_drivers_license</span></span>

- <span data-ttu-id="d8d84-1926">ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="d8d84-1926">ausstellungsdatum</span></span>
- <span data-ttu-id="d8d84-1927">
ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="d8d84-1927">ausstellungsort</span></span>
- <span data-ttu-id="d8d84-1928">
ausstellende behöde</span><span class="sxs-lookup"><span data-stu-id="d8d84-1928">ausstellende behöde</span></span>
- <span data-ttu-id="d8d84-1929">
ausstellende behorde</span><span class="sxs-lookup"><span data-stu-id="d8d84-1929">ausstellende behorde</span></span>
- <span data-ttu-id="d8d84-1930">

ausstellende behoerde</span><span class="sxs-lookup"><span data-stu-id="d8d84-1930">ausstellende behoerde</span></span>
   
## <a name="german-passport-number"></a><span data-ttu-id="d8d84-1931">Numéro de passeport Allemagne</span><span class="sxs-lookup"><span data-stu-id="d8d84-1931">German Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-1932">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-1932">Format</span></span>

<span data-ttu-id="d8d84-1933">10 chiffres ou lettres</span><span class="sxs-lookup"><span data-stu-id="d8d84-1933">10 digits or letters</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-1934">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-1934">Pattern</span></span>

<span data-ttu-id="d8d84-1935">Le modèle doit inclure tous les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="d8d84-1935">Pattern must include all of the following:</span></span>
- <span data-ttu-id="d8d84-1936">Le premier caractère est un chiffre ou une lettre de cet ensemble (C, F, G, H, J, K)</span><span class="sxs-lookup"><span data-stu-id="d8d84-1936">First character is a digit or a letter from this set (C, F, G, H, J, K)</span></span> 
- <span data-ttu-id="d8d84-1937">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-1937">Three digits</span></span> 
- <span data-ttu-id="d8d84-1938">Cinq chiffres ou lettres à partir de cet ensemble (C, -H, J-N, P, R, T, V-Z)</span><span class="sxs-lookup"><span data-stu-id="d8d84-1938">Five digits or letters from this set (C, -H, J-N, P, R, T, V-Z)</span></span> 
- <span data-ttu-id="d8d84-1939">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="d8d84-1939">A digit</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-1940">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-1940">Checksum</span></span>

<span data-ttu-id="d8d84-1941">Oui</span><span class="sxs-lookup"><span data-stu-id="d8d84-1941">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-1942">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-1942">Definition</span></span>

<span data-ttu-id="d8d84-1943">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-1943">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-1944">La fonction Func_german_passport trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1944">The function Func_german_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-1945">Un mot clé présent dans l’une des cinq listes de mots clés est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1945">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="d8d84-1946">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1946">The checksum passes.</span></span>

<span data-ttu-id="d8d84-1947">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-1947">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-1948">La fonction Func_german_passport_data trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1948">The function Func_german_passport_data finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-1949">Un mot clé présent dans l’une des cinq listes de mots clés est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1949">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="d8d84-1950">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1950">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-1951">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-1951">Keywords</span></span>

#### <a name="keywordgermanpassport"></a><span data-ttu-id="d8d84-1952">Keyword_german_passport</span><span class="sxs-lookup"><span data-stu-id="d8d84-1952">Keyword_german_passport</span></span>

- <span data-ttu-id="d8d84-1953">reisepass</span><span class="sxs-lookup"><span data-stu-id="d8d84-1953">reisepass</span></span>
- <span data-ttu-id="d8d84-1954">
reisepasse</span><span class="sxs-lookup"><span data-stu-id="d8d84-1954">reisepasse</span></span>
- <span data-ttu-id="d8d84-1955">
reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="d8d84-1955">reisepassnummer</span></span>
- <span data-ttu-id="d8d84-1956">passeport</span><span class="sxs-lookup"><span data-stu-id="d8d84-1956">passport</span></span>
- <span data-ttu-id="d8d84-1957">

passports</span><span class="sxs-lookup"><span data-stu-id="d8d84-1957">passports</span></span>

#### <a name="keywordgermanpassportcollaborative"></a><span data-ttu-id="d8d84-1958">Keyword_german_passport_collaborative</span><span class="sxs-lookup"><span data-stu-id="d8d84-1958">Keyword_german_passport_collaborative</span></span>

- <span data-ttu-id="d8d84-1959">geburtsdatum</span><span class="sxs-lookup"><span data-stu-id="d8d84-1959">geburtsdatum</span></span>
- <span data-ttu-id="d8d84-1960">ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="d8d84-1960">ausstellungsdatum</span></span>
- <span data-ttu-id="d8d84-1961">
ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="d8d84-1961">ausstellungsort</span></span>

#### <a name="keywordgermanpassportnumber"></a><span data-ttu-id="d8d84-1962">Keyword_german_passport_number</span><span class="sxs-lookup"><span data-stu-id="d8d84-1962">Keyword_german_passport_number</span></span>

<span data-ttu-id="d8d84-1963">Non-Nr Reisepass-Reisepass</span><span class="sxs-lookup"><span data-stu-id="d8d84-1963">No-Reisepass Nr-Reisepass</span></span>

#### <a name="keywordgermanpassport1"></a><span data-ttu-id="d8d84-1964">Keyword_german_passport1</span><span class="sxs-lookup"><span data-stu-id="d8d84-1964">Keyword_german_passport1</span></span>

<span data-ttu-id="d8d84-1965">Reisepass-Nr
</span><span class="sxs-lookup"><span data-stu-id="d8d84-1965">Reisepass-Nr</span></span>

#### <a name="keywordgermanpassport2"></a><span data-ttu-id="d8d84-1966">Keyword_german_passport2</span><span class="sxs-lookup"><span data-stu-id="d8d84-1966">Keyword_german_passport2</span></span>

<span data-ttu-id="d8d84-1967">bnationalit.t</span><span class="sxs-lookup"><span data-stu-id="d8d84-1967">bnationalit.t</span></span>
   
## <a name="germany-identity-card-number"></a><span data-ttu-id="d8d84-1968">Numéro de carte d’identité allemand</span><span class="sxs-lookup"><span data-stu-id="d8d84-1968">Germany Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-1969">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-1969">Format</span></span>

<span data-ttu-id="d8d84-1970">Depuis le 1er novembre 2010 : neuf lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-1970">Since 1 November 2010: Nine letters and digits</span></span>

<span data-ttu-id="d8d84-1971">À partir du 1er avril 1987 jusqu'à 31 octobre 2010:10 chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-1971">From 1 April 1987 until 31 October 2010: 10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-1972">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-1972">Pattern</span></span>

<span data-ttu-id="d8d84-1973">Depuis le 1er novembre 2010 :</span><span class="sxs-lookup"><span data-stu-id="d8d84-1973">Since 1 November 2010:</span></span>
- <span data-ttu-id="d8d84-1974">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="d8d84-1974">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="d8d84-1975">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-1975">Eight digits</span></span>

<span data-ttu-id="d8d84-1976">À partir du 1er avril 1987 jusqu’au 31 octobre 2010 :</span><span class="sxs-lookup"><span data-stu-id="d8d84-1976">From 1 April 1987 until 31 October 2010:</span></span>
- <span data-ttu-id="d8d84-1977">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-1977">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-1978">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-1978">Checksum</span></span>

<span data-ttu-id="d8d84-1979">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-1979">No</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-1980">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-1980">Definition</span></span>

<span data-ttu-id="d8d84-1981">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-1981">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-1982">L’expression régulière Regex_germany_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1982">The regular expression Regex_germany_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-1983">Un mot clé figurant dans la liste Keyword_germany_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-1983">A keyword from Keyword_germany_id_card is found.</span></span>

```
<!-- Germany Identity Card Number -->
<Entity id="e577372f-c42e-47a0-9d85-bebed1c237d4" recommendedConfidence="65" patternsProximity="300">
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Regex_germany_id_card"/>
     <Match idRef="Keyword_germany_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8d84-1984">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-1984">Keywords</span></span>

#### <a name="keywordgermanyidcard"></a><span data-ttu-id="d8d84-1985">Keyword_germany_id_card</span><span class="sxs-lookup"><span data-stu-id="d8d84-1985">Keyword_germany_id_card</span></span>

- <span data-ttu-id="d8d84-1986">Identity Card</span><span class="sxs-lookup"><span data-stu-id="d8d84-1986">Identity Card</span></span>
- <span data-ttu-id="d8d84-1987">ID</span><span class="sxs-lookup"><span data-stu-id="d8d84-1987">ID</span></span>
- <span data-ttu-id="d8d84-1988">Identification</span><span class="sxs-lookup"><span data-stu-id="d8d84-1988">Identification</span></span>
- <span data-ttu-id="d8d84-1989">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="d8d84-1989">Personalausweis</span></span>
- <span data-ttu-id="d8d84-1990">Identifizierungsnummer</span><span class="sxs-lookup"><span data-stu-id="d8d84-1990">Identifizierungsnummer</span></span>
- <span data-ttu-id="d8d84-1991">Ausweis</span><span class="sxs-lookup"><span data-stu-id="d8d84-1991">Ausweis</span></span>
- <span data-ttu-id="d8d84-1992">Identifikation</span><span class="sxs-lookup"><span data-stu-id="d8d84-1992">Identifikation</span></span>
   
## <a name="greece-national-id-card"></a><span data-ttu-id="d8d84-1993">Carte d’identité nationale Grèce</span><span class="sxs-lookup"><span data-stu-id="d8d84-1993">Greece National ID Card</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-1994">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-1994">Format</span></span>

<span data-ttu-id="d8d84-1995">Combinaison de 7 ou 8 lettres et chiffres, plus un tiret</span><span class="sxs-lookup"><span data-stu-id="d8d84-1995">Combination of 7-8 letters and numbers plus a dash</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-1996">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-1996">Pattern</span></span>

<span data-ttu-id="d8d84-1997">Sept lettres et chiffres (ancien format) :</span><span class="sxs-lookup"><span data-stu-id="d8d84-1997">Seven letters and numbers (old format):</span></span>
- <span data-ttu-id="d8d84-1998">Une lettre (de l’alphabet grec) </span><span class="sxs-lookup"><span data-stu-id="d8d84-1998">One letter (any letter of the Greek alphabet)</span></span> 
- <span data-ttu-id="d8d84-1999">Un tiret</span><span class="sxs-lookup"><span data-stu-id="d8d84-1999">A dash</span></span> 
- <span data-ttu-id="d8d84-2000">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2000">Six digits</span></span>

<span data-ttu-id="d8d84-2001">Huit lettres et chiffres (nouveau format) :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2001">Eight letters and numbers (new format):</span></span>
- <span data-ttu-id="d8d84-2002">Deux lettres dont le caractère majuscule figure à la fois dans l’alphabet grec et l’alphabet latin (ABEZHIKMNOPTYX) </span><span class="sxs-lookup"><span data-stu-id="d8d84-2002">Two letters whose uppercase character occurs in both the Greek and Latin alphabets (ABEZHIKMNOPTYX)</span></span> 
- <span data-ttu-id="d8d84-2003">Un tiret</span><span class="sxs-lookup"><span data-stu-id="d8d84-2003">A dash</span></span> 
- <span data-ttu-id="d8d84-2004">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2004">Six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-2005">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2005">Checksum</span></span>

<span data-ttu-id="d8d84-2006">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-2006">No</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-2007">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-2007">Definition</span></span>

<span data-ttu-id="d8d84-2008">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2008">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2009">L’expression régulière Regex_greece_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2009">The regular expression Regex_greece_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2010">Un mot clé figurant dans la liste Keyword_greece_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2010">A keyword from Keyword_greece_id_card is found.</span></span>

```
<!-- Greece National ID Card -->
<Entity id="82568215-1da1-46d3-874a-d2294d81b5ac" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_greece_id_card"/>
     <Match idRef="Keyword_greece_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8d84-2011">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-2011">Keywords</span></span>

#### <a name="keywordgreeceidcard"></a><span data-ttu-id="d8d84-2012">Keyword_greece_id_card</span><span class="sxs-lookup"><span data-stu-id="d8d84-2012">Keyword_greece_id_card</span></span>

- <span data-ttu-id="d8d84-2013">Greek identity Card</span><span class="sxs-lookup"><span data-stu-id="d8d84-2013">Greek identity Card</span></span>
- <span data-ttu-id="d8d84-2014">Tautotita</span><span class="sxs-lookup"><span data-stu-id="d8d84-2014">Tautotita</span></span>
- <span data-ttu-id="d8d84-2015">Δελτίο αστυνομικής ταυτότητας</span><span class="sxs-lookup"><span data-stu-id="d8d84-2015">Δελτίο αστυνομικής ταυτότητας</span></span>
- <span data-ttu-id="d8d84-2016">Ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="d8d84-2016">Ταυτότητα</span></span>
   
## <a name="hong-kong-identity-card-hkid-number"></a><span data-ttu-id="d8d84-2017">Numéro de carte d’identité (HKID) Hong Kong</span><span class="sxs-lookup"><span data-stu-id="d8d84-2017">Hong Kong Identity Card (HKID) Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-2018">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-2018">Format</span></span>

<span data-ttu-id="d8d84-2019">Combinaison de 8 ou 9 lettres et chiffres plus éventuellement des parenthèses autour du dernier caractère</span><span class="sxs-lookup"><span data-stu-id="d8d84-2019">Combination of 8-9 letters and numbers plus optional parentheses around the final character</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-2020">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2020">Pattern</span></span>

<span data-ttu-id="d8d84-2021">Combinaison de 8 ou 9 lettres :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2021">Combination of 8-9 letters:</span></span>
- <span data-ttu-id="d8d84-2022">1 ou 2 lettres (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="d8d84-2022">1-2 letters (not case sensitive)</span></span> 
- <span data-ttu-id="d8d84-2023">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2023">Six digits</span></span> 
- <span data-ttu-id="d8d84-2024">Le dernier caractère (un chiffre ou la lettre A), qui est le chiffre de contrôle et est éventuellement entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2024">The final character (any digit or the letter A), which is the check digit and is optionally enclosed in parentheses.</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-2025">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2025">Checksum</span></span>

<span data-ttu-id="d8d84-2026">Oui</span><span class="sxs-lookup"><span data-stu-id="d8d84-2026">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-2027">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-2027">Definition</span></span>

<span data-ttu-id="d8d84-2028">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2028">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2029">La fonction Func_hong_kong_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2029">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2030">Un mot clé figurant dans la liste Keyword_hong_kong_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2030">A keyword from Keyword_hong_kong_id_card is found.</span></span>
- <span data-ttu-id="d8d84-2031">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2031">The checksum passes.</span></span>

<span data-ttu-id="d8d84-2032">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2032">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2033">La fonction Func_hong_kong_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2033">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2034">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2034">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-2035">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-2035">Keywords</span></span>

#### <a name="keywordhongkongidcard"></a><span data-ttu-id="d8d84-2036">Keyword_hong_kong_id_card</span><span class="sxs-lookup"><span data-stu-id="d8d84-2036">Keyword_hong_kong_id_card</span></span>

- <span data-ttu-id="d8d84-2037">carte d’identité de Hong kong</span><span class="sxs-lookup"><span data-stu-id="d8d84-2037">hong kong identity card</span></span>
- <span data-ttu-id="d8d84-2038">HKIDC</span><span class="sxs-lookup"><span data-stu-id="d8d84-2038">HKIDC</span></span>
- <span data-ttu-id="d8d84-2039">carte d’identité</span><span class="sxs-lookup"><span data-stu-id="d8d84-2039">id card</span></span>
- <span data-ttu-id="d8d84-2040">Carte d’identité</span><span class="sxs-lookup"><span data-stu-id="d8d84-2040">identity card</span></span>
- <span data-ttu-id="d8d84-2041">carte d’identité HK</span><span class="sxs-lookup"><span data-stu-id="d8d84-2041">hk identity card</span></span>
- <span data-ttu-id="d8d84-2042">id de Hong kong</span><span class="sxs-lookup"><span data-stu-id="d8d84-2042">hong kong id</span></span>
- <span data-ttu-id="d8d84-2043">香港身份證
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2043">香港身份證</span></span>
- <span data-ttu-id="d8d84-2044">香港永久性居民身份證
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2044">香港永久性居民身份證</span></span>
- <span data-ttu-id="d8d84-2045">身份證
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2045">身份證</span></span>
- <span data-ttu-id="d8d84-2046">身份証</span><span class="sxs-lookup"><span data-stu-id="d8d84-2046">身份証</span></span>
- <span data-ttu-id="d8d84-2047">身分證 </span><span class="sxs-lookup"><span data-stu-id="d8d84-2047">身分證</span></span>
- <span data-ttu-id="d8d84-2048">身分証</span><span class="sxs-lookup"><span data-stu-id="d8d84-2048">身分証</span></span>
- <span data-ttu-id="d8d84-2049">香港身份証</span><span class="sxs-lookup"><span data-stu-id="d8d84-2049">香港身份証</span></span>
- <span data-ttu-id="d8d84-2050">香港身分證</span><span class="sxs-lookup"><span data-stu-id="d8d84-2050">香港身分證</span></span>
- <span data-ttu-id="d8d84-2051">香港身分証</span><span class="sxs-lookup"><span data-stu-id="d8d84-2051">香港身分証</span></span>
- <span data-ttu-id="d8d84-2052">香港身份證
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2052">香港身份證</span></span>
- <span data-ttu-id="d8d84-2053">香港居民身份證</span><span class="sxs-lookup"><span data-stu-id="d8d84-2053">香港居民身份證</span></span>
- <span data-ttu-id="d8d84-2054">香港居民身份証</span><span class="sxs-lookup"><span data-stu-id="d8d84-2054">香港居民身份証</span></span>
- <span data-ttu-id="d8d84-2055">香港居民身分證</span><span class="sxs-lookup"><span data-stu-id="d8d84-2055">香港居民身分證</span></span>
- <span data-ttu-id="d8d84-2056">香港居民身分証</span><span class="sxs-lookup"><span data-stu-id="d8d84-2056">香港居民身分証</span></span>
- <span data-ttu-id="d8d84-2057">香港永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="d8d84-2057">香港永久性居民身份証</span></span>
- <span data-ttu-id="d8d84-2058">香港永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="d8d84-2058">香港永久性居民身分證</span></span>
- <span data-ttu-id="d8d84-2059">香港永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="d8d84-2059">香港永久性居民身分証</span></span>
- <span data-ttu-id="d8d84-2060">香港永久性居民身份證
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2060">香港永久性居民身份證</span></span>
- <span data-ttu-id="d8d84-2061">香港非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="d8d84-2061">香港非永久性居民身份證</span></span>
- <span data-ttu-id="d8d84-2062">香港非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="d8d84-2062">香港非永久性居民身份証</span></span>
- <span data-ttu-id="d8d84-2063">香港非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="d8d84-2063">香港非永久性居民身分證</span></span>
- <span data-ttu-id="d8d84-2064">香港非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="d8d84-2064">香港非永久性居民身分証</span></span>
- <span data-ttu-id="d8d84-2065">香港特別行政區永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="d8d84-2065">香港特別行政區永久性居民身份證</span></span>
- <span data-ttu-id="d8d84-2066">香港特別行政區永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="d8d84-2066">香港特別行政區永久性居民身份証</span></span>
- <span data-ttu-id="d8d84-2067">香港特別行政區永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="d8d84-2067">香港特別行政區永久性居民身分證</span></span>
- <span data-ttu-id="d8d84-2068">香港特別行政區永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="d8d84-2068">香港特別行政區永久性居民身分証</span></span>
- <span data-ttu-id="d8d84-2069">香港特別行政區非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="d8d84-2069">香港特別行政區非永久性居民身份證</span></span>
- <span data-ttu-id="d8d84-2070">香港特別行政區非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="d8d84-2070">香港特別行政區非永久性居民身份証</span></span>
- <span data-ttu-id="d8d84-2071">香港特別行政區非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="d8d84-2071">香港特別行政區非永久性居民身分證</span></span>
- <span data-ttu-id="d8d84-2072">香港特別行政區非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="d8d84-2072">香港特別行政區非永久性居民身分証</span></span>
   
## <a name="india-permanent-account-number-pan"></a><span data-ttu-id="d8d84-2073">Numéro de compte permanent Inde</span><span class="sxs-lookup"><span data-stu-id="d8d84-2073">India Permanent Account Number (PAN)</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-2074">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-2074">Format</span></span>

<span data-ttu-id="d8d84-2075">10 lettres ou chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2075">10 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-2076">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2076">Pattern</span></span>

<span data-ttu-id="d8d84-2077">10 lettres ou chiffres :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2077">10 letters or digits:</span></span>
- <span data-ttu-id="d8d84-2078">Cinq lettres (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="d8d84-2078">Five letters (not case sensitive)</span></span> 
- <span data-ttu-id="d8d84-2079">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2079">Four digits</span></span> 
- <span data-ttu-id="d8d84-2080">Une lettre qui est un chiffre de contrôle alphabétique</span><span class="sxs-lookup"><span data-stu-id="d8d84-2080">A letter which is an alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-2081">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2081">Checksum</span></span>

<span data-ttu-id="d8d84-2082">Oui</span><span class="sxs-lookup"><span data-stu-id="d8d84-2082">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-2083">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-2083">Definition</span></span>

<span data-ttu-id="d8d84-2084">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2084">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2085">L’expression régulière Regex_india_permanent_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2085">The regular expression Regex_india_permanent_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2086">Un mot clé figurant dans la liste Keyword_india_permanent_account_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2086">A keyword from Keyword_india_permanent_account_number is found.</span></span>
- <span data-ttu-id="d8d84-2087">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2087">The checksum passes.</span></span>

```
<!-- India Permanent Account Number -->
<Entity id="2602bfee-9bb0-47a5-a7a6-2bf3053e2804" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_india_permanent_account_number"/>
     <Match idRef="Keyword_india_permanent_account_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8d84-2088">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-2088">Keywords</span></span>

#### <a name="keywordindiapermanentaccountnumber"></a><span data-ttu-id="d8d84-2089">Keyword_india_permanent_account_number</span><span class="sxs-lookup"><span data-stu-id="d8d84-2089">Keyword_india_permanent_account_number</span></span>

- <span data-ttu-id="d8d84-2090">Permanent Account Number
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2090">Permanent Account Number</span></span> 
- <span data-ttu-id="d8d84-2091">PAN
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2091">PAN</span></span> 
   
## <a name="india-unique-identification-aadhaar-number"></a><span data-ttu-id="d8d84-2092">Numéro d’identification unique (Aadhaar) Inde</span><span class="sxs-lookup"><span data-stu-id="d8d84-2092">India Unique Identification (Aadhaar) Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-2093">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-2093">Format</span></span>

<span data-ttu-id="d8d84-2094">12 chiffres contenant éventuellement des espaces ou des tirets</span><span class="sxs-lookup"><span data-stu-id="d8d84-2094">12 digits containing optional spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-2095">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2095">Pattern</span></span>

<span data-ttu-id="d8d84-2096">12 chiffres :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2096">12 digits:</span></span>
- <span data-ttu-id="d8d84-2097">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2097">Four digits</span></span> 
- <span data-ttu-id="d8d84-2098">Éventuellement un tiret ou un espace </span><span class="sxs-lookup"><span data-stu-id="d8d84-2098">An optional space or dash</span></span> 
- <span data-ttu-id="d8d84-2099">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2099">Four digits</span></span> 
- <span data-ttu-id="d8d84-2100">Éventuellement un tiret ou un espace </span><span class="sxs-lookup"><span data-stu-id="d8d84-2100">An optional space or dash</span></span> 
- <span data-ttu-id="d8d84-2101">Le chiffre final, qui est le chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2101">The final digit which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-2102">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2102">Checksum</span></span>

<span data-ttu-id="d8d84-2103">Oui</span><span class="sxs-lookup"><span data-stu-id="d8d84-2103">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-2104">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-2104">Definition</span></span>

<span data-ttu-id="d8d84-p133">Une stratégie DLP est de 85 % convaincu que ce type d’informations sensibles a été détecté if, au sein d’une proximité de 300 caractères : la fonction Func_india_aadhaar recherche le contenu qui correspond au modèle. Un mot clé à partir de Keyword_india_aadhar est trouvé. Passe de la somme de contrôle. Une stratégie DLP est convaincu que ce type d’informations sensibles a été détecté à 75 % if, au sein d’une proximité de 300 caractères : la fonction Func_india_aadhaar recherche le contenu qui correspond au modèle. Passe de la somme de contrôle. <!-- India Unique Identification (Aadhaar) number -->
<Entity id="1ca46b29-76f5-4f46-9383-cfa15e91048f" recommendedConfidence="85" patternsProximity="300"> <Pattern confidenceLevel="85"> <IdMatch idRef="Func_india_aadhaar"/> <Match idRef="Keyword_india_aadhar"/> </Pattern> <Pattern confidenceLevel="75"> <IdMatch idRef="Func_india_aadhaar"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="d8d84-p133">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern. A keyword from Keyword_india_aadhar is found. The checksum passes. A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern. The checksum passes. <!-- India Unique Identification (Aadhaar) number -->
<Entity id="1ca46b29-76f5-4f46-9383-cfa15e91048f" recommendedConfidence="85" patternsProximity="300"> <Pattern confidenceLevel="85"> <IdMatch idRef="Func_india_aadhaar"/> <Match idRef="Keyword_india_aadhar"/> </Pattern> <Pattern confidenceLevel="75"> <IdMatch idRef="Func_india_aadhaar"/> </Pattern>
</Entity></span></span>

### <a name="keywords"></a><span data-ttu-id="d8d84-2111">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-2111">Keywords</span></span>
   
#### <a name="keywordindiaaadhar"></a><span data-ttu-id="d8d84-2112">Keyword_india_aadhar</span><span class="sxs-lookup"><span data-stu-id="d8d84-2112">Keyword_india_aadhar</span></span>
- <span data-ttu-id="d8d84-2113">Aadhar</span><span class="sxs-lookup"><span data-stu-id="d8d84-2113">Aadhar</span></span>
- <span data-ttu-id="d8d84-2114">Aadhaar</span><span class="sxs-lookup"><span data-stu-id="d8d84-2114">Aadhaar</span></span>
- <span data-ttu-id="d8d84-2115">UID</span><span class="sxs-lookup"><span data-stu-id="d8d84-2115">UID</span></span>
- <span data-ttu-id="d8d84-2116">आधार</span><span class="sxs-lookup"><span data-stu-id="d8d84-2116">आधार</span></span>
   
## <a name="indonesia-identity-card-ktp-number"></a><span data-ttu-id="d8d84-2117">Numéro de carte d’identité (KTP) Indonésie</span><span class="sxs-lookup"><span data-stu-id="d8d84-2117">Indonesia Identity Card (KTP) Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-2118">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-2118">Format</span></span>

<span data-ttu-id="d8d84-2119">16 chiffres contenant éventuellement des points</span><span class="sxs-lookup"><span data-stu-id="d8d84-2119">16 digits containing optional periods</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-2120">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2120">Pattern</span></span>

<span data-ttu-id="d8d84-2121">16 chiffres :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2121">16 digits:</span></span>
- <span data-ttu-id="d8d84-2122">Code à deux chiffres désignant la province </span><span class="sxs-lookup"><span data-stu-id="d8d84-2122">Two-digit province code</span></span> 
- <span data-ttu-id="d8d84-2123">Un point (facultatif) </span><span class="sxs-lookup"><span data-stu-id="d8d84-2123">A period (optional)</span></span> 
- <span data-ttu-id="d8d84-2124">Code à deux chiffres désignant une régence ou une ville </span><span class="sxs-lookup"><span data-stu-id="d8d84-2124">Two-digit regency or city code</span></span> 
- <span data-ttu-id="d8d84-2125">Code à deux chiffres désignant un sous-district </span><span class="sxs-lookup"><span data-stu-id="d8d84-2125">Two-digit subdistrict code</span></span> 
- <span data-ttu-id="d8d84-2126">Un point (facultatif) </span><span class="sxs-lookup"><span data-stu-id="d8d84-2126">A period (optional)</span></span> 
- <span data-ttu-id="d8d84-2127">Six chiffres au format JJMMAA qui correspondent à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="d8d84-2127">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="d8d84-2128">Un point (facultatif) </span><span class="sxs-lookup"><span data-stu-id="d8d84-2128">A period (optional)</span></span> 
- <span data-ttu-id="d8d84-2129">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2129">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-2130">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2130">Checksum</span></span>

<span data-ttu-id="d8d84-2131">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-2131">No</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-2132">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-2132">Definition</span></span>

<span data-ttu-id="d8d84-2133">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2133">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2134">L’expression régulière Regex_indonesia_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2134">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2135">Un mot clé figurant dans la liste Keyword_indonesia_id_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2135">A keyword from Keyword_indonesia_id_card is found.</span></span>

<span data-ttu-id="d8d84-2136">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2136">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2137">L’expression régulière Regex_indonesia_id_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2137">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-2138">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-2138">Keywords</span></span>
   
#### <a name="keywordindonesiaidcard"></a><span data-ttu-id="d8d84-2139">Keyword_indonesia_id_card</span><span class="sxs-lookup"><span data-stu-id="d8d84-2139">Keyword_indonesia_id_card</span></span>

- <span data-ttu-id="d8d84-2140">KTP</span><span class="sxs-lookup"><span data-stu-id="d8d84-2140">KTP</span></span>
- <span data-ttu-id="d8d84-2141">Kartu Tanda Penduduk
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2141">Kartu Tanda Penduduk</span></span> 
- <span data-ttu-id="d8d84-2142">Nomor Induk Kependudukan
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2142">Nomor Induk Kependudukan</span></span> 
   
## <a name="international-banking-account-number-iban"></a><span data-ttu-id="d8d84-2143">Numéro de compte bancaire international (IBAN)</span><span class="sxs-lookup"><span data-stu-id="d8d84-2143">International Banking Account Number (IBAN)</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-2144">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-2144">Format</span></span>

<span data-ttu-id="d8d84-2145">Code pays (à deux lettres) plus chiffres de contrôle (à deux chiffres) plus numéro BBAN (jusqu’à 30 chiffres)</span><span class="sxs-lookup"><span data-stu-id="d8d84-2145">Country code (two letters) plus check digits (two digits) plus bban number (up to 30 characters)</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-2146">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2146">Pattern</span></span>

<span data-ttu-id="d8d84-2147">Le modèle doit inclure tous les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2147">Pattern must include all of the following:</span></span>

- <span data-ttu-id="d8d84-2148">Code pays à deux lettres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2148">Two-letter country code</span></span>
- <span data-ttu-id="d8d84-2149">Deux chiffres de contrôle (suivis d’un espace facultatif) </span><span class="sxs-lookup"><span data-stu-id="d8d84-2149">Two check digits (followed by an optional space)</span></span> 
- <span data-ttu-id="d8d84-2150">1 à 7 groupes de quatre lettres ou chiffres (séparés par des espaces facultatifs)</span><span class="sxs-lookup"><span data-stu-id="d8d84-2150">1-7 groups of four letters or digits (can be separated by spaces)</span></span>
- <span data-ttu-id="d8d84-2151">1 à 3 lettres ou chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2151">1-3 letters or digits</span></span>

<span data-ttu-id="d8d84-p134">Le format pour chaque pays est légèrement différent. Le type d’informations sensibles IBAN recouvre ces 60 pays :</span><span class="sxs-lookup"><span data-stu-id="d8d84-p134">The format for each country is slightly different. The IBAN sensitive information type covers these 60 countries:</span></span>

<span data-ttu-id="d8d84-2154">ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg</span><span class="sxs-lookup"><span data-stu-id="d8d84-2154">ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-2155">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2155">Checksum</span></span>

<span data-ttu-id="d8d84-2156">Oui</span><span class="sxs-lookup"><span data-stu-id="d8d84-2156">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-2157">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-2157">Definition</span></span>

<span data-ttu-id="d8d84-2158">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2158">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2159">La fonction Func_iban trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2159">The function Func_iban finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2160">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2160">The checksum passes.</span></span>

```
<Entity id="e7dc4711-11b7-4cb0-b88b-2c394a771f0e" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_iban" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8d84-2161">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-2161">Keywords</span></span>

<span data-ttu-id="d8d84-2162">Aucune</span><span class="sxs-lookup"><span data-stu-id="d8d84-2162">None</span></span>

   
## <a name="ip-address"></a><span data-ttu-id="d8d84-2163">Adresse IP</span><span class="sxs-lookup"><span data-stu-id="d8d84-2163">IP Address</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-2164">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-2164">Format</span></span>

#### <a name="ipv4"></a><span data-ttu-id="d8d84-2165">IPv4 :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2165">IPv4:</span></span>
<span data-ttu-id="d8d84-2166">Modèle complexe qui tient compte des versions mises en forme (points) et non mises en forme (sans points) des adresses IPv4</span><span class="sxs-lookup"><span data-stu-id="d8d84-2166">Complex pattern which accounts for formatted (periods) and unformatted (no periods) versions of the IPv4 addresses</span></span>

#### <a name="ipv6"></a><span data-ttu-id="d8d84-2167">IPv6 :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2167">IPv6:</span></span>
<span data-ttu-id="d8d84-2168"> Modèle complexe qui tient compte des numéros IPv6 mis en forme (qui incluent les signes deux-points)</span><span class="sxs-lookup"><span data-stu-id="d8d84-2168">Complex pattern which accounts for formatted IPv6 numbers (which include colons)</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-2169">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2169">Pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-2170">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2170">Checksum</span></span>

<span data-ttu-id="d8d84-2171">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-2171">No</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-2172">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-2172">Definition</span></span>

<span data-ttu-id="d8d84-2173">Pour IPv6, le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2173">For IPv6, a DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2174">L’expression régulière Regex_ipv6_address trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2174">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2175">Aucun mot clé figurant dans la liste Keyword_ipaddress n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2175">No keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="d8d84-2176">Pour IPv4, le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 95 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2176">For IPv4, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2177">L’expression régulière Regex_ipv4_address trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2177">The regular expression Regex_ipv4_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2178">Un mot clé figurant dans la liste Keyword_ipaddress est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2178">A keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="d8d84-2179">Pour IPv6, le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 95 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2179">For IPv6, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2180">L’expression régulière Regex_ipv6_address trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2180">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2181">Aucun mot clé figurant dans la liste Keyword_ipaddress n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2181">No keyword from Keyword_ipaddress is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-2182">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-2182">Keywords</span></span>

#### <a name="keywordipaddress"></a><span data-ttu-id="d8d84-2183">Keyword_ipaddress</span><span class="sxs-lookup"><span data-stu-id="d8d84-2183">Keyword_ipaddress</span></span>

- <span data-ttu-id="d8d84-2184">IP (ce mot clé respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="d8d84-2184">IP (this keyword is case sensitive)</span></span>
- <span data-ttu-id="d8d84-2185">ip address
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2185">ip address</span></span> 
- <span data-ttu-id="d8d84-2186">adresses IP</span><span class="sxs-lookup"><span data-stu-id="d8d84-2186">ip addresses</span></span>
- <span data-ttu-id="d8d84-2187">protocole internet</span><span class="sxs-lookup"><span data-stu-id="d8d84-2187">internet protocol</span></span>
- <span data-ttu-id="d8d84-2188">
IP-כתובת ה
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2188">IP-כתובת ה</span></span> 
   
## <a name="international-classification-of-diseases-icd-10-cm"></a><span data-ttu-id="d8d84-2189">Classification internationale de maux (ICD-10 CM)</span><span class="sxs-lookup"><span data-stu-id="d8d84-2189">International Classification of Diseases (ICD-10-CM)</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-2190">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-2190">Format</span></span>

<span data-ttu-id="d8d84-2191">Dictionnaire</span><span class="sxs-lookup"><span data-stu-id="d8d84-2191">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-2192">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2192">Pattern</span></span>

<span data-ttu-id="d8d84-2193">Mot clé</span><span class="sxs-lookup"><span data-stu-id="d8d84-2193">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-2194">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2194">Checksum</span></span>

<span data-ttu-id="d8d84-2195">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-2195">No</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-2196">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-2196">Definition</span></span>

<span data-ttu-id="d8d84-2197">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2197">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2198">Un mot clé à partir de Dictionary_icd_10_cm est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2198">A keyword from Dictionary_icd_10_cm is found.</span></span>

```
      <!-- ICD-10 CM -->
      <Entity id="3356946c-6bb7-449b-b253-6ffa419c0ce7" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_10_cm" />
        </Pattern>
      </Entity>
```

<span data-ttu-id="d8d84-2199">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-2199">Keywords</span></span>

<span data-ttu-id="d8d84-p135">Les termes à partir du dictionnaire de mot clé Dictionary_icd_10_cm, qui repose sur [International Classification de maux, révision dixième, Modification cliniques (ICD-10-CM)](https://go.microsoft.com/fwlink/?linkid=852604). Ce type de recherche uniquement le terme, pas les codes d’assurance.</span><span class="sxs-lookup"><span data-stu-id="d8d84-p135">Any term from the Dictionary_icd_10_cm keyword dictionary, which is based on the [International Classification of Diseases, Tenth Revision, Clinical Modification (ICD-10-CM)](https://go.microsoft.com/fwlink/?linkid=852604). This type looks only for the term, not the insurance codes.</span></span>

   
## <a name="international-classification-of-diseases-icd-9-cm"></a><span data-ttu-id="d8d84-2202">Classification internationale de maux (ICD-9-CM)</span><span class="sxs-lookup"><span data-stu-id="d8d84-2202">International Classification of Diseases (ICD-9-CM)</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-2203">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-2203">Format</span></span>

<span data-ttu-id="d8d84-2204">Dictionnaire</span><span class="sxs-lookup"><span data-stu-id="d8d84-2204">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-2205">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2205">Pattern</span></span>

<span data-ttu-id="d8d84-2206">Mot clé</span><span class="sxs-lookup"><span data-stu-id="d8d84-2206">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-2207">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2207">Checksum</span></span>

<span data-ttu-id="d8d84-2208">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-2208">No</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-2209">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-2209">Definition</span></span>

<span data-ttu-id="d8d84-2210">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2210">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2211">Un mot clé à partir de Dictionary_icd_9_cm est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2211">A keyword from Dictionary_icd_9_cm is found.</span></span>

```
      <Entity id="fa3f9c74-ee07-4c52-b5f2-085d6b2c0ec4" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_9_cm" />
        </Pattern>
      </Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8d84-2212">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-2212">Keywords</span></span>

<span data-ttu-id="d8d84-p136">Les termes à partir du dictionnaire de mot clé Dictionary_icd_9_cm, qui repose sur [International Classification de maux, révision neuvième, Modification cliniques (ICD-9-CM)](https://go.microsoft.com/fwlink/?linkid=852605). Ce type de recherche uniquement le terme, pas les codes d’assurance.</span><span class="sxs-lookup"><span data-stu-id="d8d84-p136">Any term from the Dictionary_icd_9_cm keyword dictionary, which is based on the [International Classification of Diseases,Ninth Revision, Clinical Modification (ICD-9-CM)](https://go.microsoft.com/fwlink/?linkid=852605). This type looks only for the term, not the insurance codes.</span></span>
   
## <a name="ireland-personal-public-service-pps-number"></a><span data-ttu-id="d8d84-2215">Numéro de service public personnel (PPS) Irlande</span><span class="sxs-lookup"><span data-stu-id="d8d84-2215">Ireland Personal Public Service (PPS) Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-2216">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-2216">Format</span></span>

<span data-ttu-id="d8d84-2217">Ancien format (jusqu'à 31 décembre 2012) :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2217">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="d8d84-2218">Sept chiffres suivis de 1 ou 2 lettres </span><span class="sxs-lookup"><span data-stu-id="d8d84-2218">Seven digits followed by 1-2 letters</span></span> 

<span data-ttu-id="d8d84-2219">Nouveau format (1er janvier 2013 et une fois) :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2219">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="d8d84-2220">Sept chiffres suivis de deux lettres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2220">Seven digits followed by two letters</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-2221">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2221">Pattern</span></span>

<span data-ttu-id="d8d84-2222">Ancien format (jusqu'à 31 décembre 2012) :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2222">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="d8d84-2223">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="d8d84-2223">Seven digits</span></span> 
- <span data-ttu-id="d8d84-2224">1 ou 2 lettres (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="d8d84-2224">1-2 letters (not case sensitive)</span></span> 

<span data-ttu-id="d8d84-2225">Nouveau format (1er janvier 2013 et une fois) :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2225">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="d8d84-2226">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="d8d84-2226">Seven digits</span></span> 
- <span data-ttu-id="d8d84-2227">Une lettre (ne respectant pas la casse), qui est un chiffre de contrôle alphabétique </span><span class="sxs-lookup"><span data-stu-id="d8d84-2227">A letter (not case sensitive) which is an alphabetic check digit</span></span> 
- <span data-ttu-id="d8d84-2228">La lettre « A » ou « H » (ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="d8d84-2228">The letter "A" or "H" (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-2229">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2229">Checksum</span></span>

<span data-ttu-id="d8d84-2230">Oui</span><span class="sxs-lookup"><span data-stu-id="d8d84-2230">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-2231">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-2231">Definition</span></span>

<span data-ttu-id="d8d84-2232">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2232">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2233">La fonction Func_ireland_pps trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2233">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2234">L’une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2234">One of the following is true:</span></span>
    - <span data-ttu-id="d8d84-2235">Un mot clé figurant dans la liste Keyword_ireland_pps est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2235">A keyword from Keyword_ireland_pps is found.</span></span>
    - <span data-ttu-id="d8d84-2236">La fonction Func_eu_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2236">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="d8d84-2237">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2237">The checksum passes.</span></span>

<span data-ttu-id="d8d84-2238">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2238">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2239">La fonction Func_ireland_pps trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2239">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2240">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2240">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-2241">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-2241">Keywords</span></span>

#### <a name="keywordirelandpps"></a><span data-ttu-id="d8d84-2242">Keyword_ireland_pps</span><span class="sxs-lookup"><span data-stu-id="d8d84-2242">Keyword_ireland_pps</span></span>

- <span data-ttu-id="d8d84-2243">Personal Public Service Number 
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2243">Personal Public Service Number</span></span> 
- <span data-ttu-id="d8d84-2244">PPS Number
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2244">PPS Number</span></span> 
- <span data-ttu-id="d8d84-2245">PPS Num
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2245">PPS Num</span></span> 
- <span data-ttu-id="d8d84-2246">PPS No.
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2246">PPS No.</span></span> 
- <span data-ttu-id="d8d84-2247">PPS #
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2247">PPS #</span></span> 
- <span data-ttu-id="d8d84-2248">PPS #</span><span class="sxs-lookup"><span data-stu-id="d8d84-2248">PPS#</span></span> 
- <span data-ttu-id="d8d84-2249">PPSN
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2249">PPSN</span></span> 
- <span data-ttu-id="d8d84-2250">Public Services Card
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2250">Public Services Card</span></span> 
- <span data-ttu-id="d8d84-2251">Uimhir Phearsanta Seirbhíse Poiblí
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2251">Uimhir Phearsanta Seirbhíse Poiblí</span></span> 
- <span data-ttu-id="d8d84-p137">Uimh. PSP
</span><span class="sxs-lookup"><span data-stu-id="d8d84-p137">Uimh. PSP</span></span> 
- <span data-ttu-id="d8d84-2254">PSP
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2254">PSP</span></span> 
   
## <a name="israel-bank-account-number"></a><span data-ttu-id="d8d84-2255">Numéro de compte bancaire Israël</span><span class="sxs-lookup"><span data-stu-id="d8d84-2255">Israel Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-2256">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-2256">Format</span></span>

<span data-ttu-id="d8d84-2257">13 chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2257">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-2258">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2258">Pattern</span></span>

<span data-ttu-id="d8d84-2259">Mis en forme :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2259">Formatted:</span></span>
- <span data-ttu-id="d8d84-2260">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2260">Two digits</span></span> 
- <span data-ttu-id="d8d84-2261">Un tiret</span><span class="sxs-lookup"><span data-stu-id="d8d84-2261">A dash</span></span> 
- <span data-ttu-id="d8d84-2262">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2262">Three digits</span></span> 
- <span data-ttu-id="d8d84-2263">Un tiret</span><span class="sxs-lookup"><span data-stu-id="d8d84-2263">A dash</span></span> 
- <span data-ttu-id="d8d84-2264">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2264">Eight digits</span></span>

<span data-ttu-id="d8d84-2265">Non mis en forme :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2265">Unformatted:</span></span>
- <span data-ttu-id="d8d84-2266">	13 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="d8d84-2266">13 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-2267">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2267">Checksum</span></span>

<span data-ttu-id="d8d84-2268">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-2268">No</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-2269">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-2269">Definition</span></span>

<span data-ttu-id="d8d84-2270">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2270">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2271">L’expression régulière Regex_israel_bank_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2271">The regular expression Regex_israel_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2272">Un mot clé figurant dans la liste Keyword_israel_bank_account_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2272">A keyword from Keyword_israel_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-2273">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-2273">Keywords</span></span>

#### <a name="keywordisraelbankaccountnumber"></a><span data-ttu-id="d8d84-2274">Keyword_israel_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="d8d84-2274">Keyword_israel_bank_account_number</span></span>

- <span data-ttu-id="d8d84-2275">Numéro de compte bancaire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2275">Bank Account Number</span></span> 
- <span data-ttu-id="d8d84-2276">Compte bancaire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2276">Bank Account</span></span> 
- <span data-ttu-id="d8d84-2277">Numéro de compte
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2277">Account Number</span></span> 
- <span data-ttu-id="d8d84-2278">מספר חשבון בנק
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2278">מספר חשבון בנק</span></span> 
   
## <a name="israel-national-id"></a><span data-ttu-id="d8d84-2279">Carte nationale d'identité Israël</span><span class="sxs-lookup"><span data-stu-id="d8d84-2279">Israel National ID</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-2280">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-2280">Format</span></span>

<span data-ttu-id="d8d84-2281">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2281">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-2282">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2282">Pattern</span></span>

<span data-ttu-id="d8d84-2283">Neuf chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="d8d84-2283">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-2284">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2284">Checksum</span></span>

<span data-ttu-id="d8d84-2285">Oui</span><span class="sxs-lookup"><span data-stu-id="d8d84-2285">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-2286">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-2286">Definition</span></span>

<span data-ttu-id="d8d84-2287">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2287">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2288">La fonction Func_israeli_national_id_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2288">The function Func_israeli_national_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2289">Un mot clé figurant dans la liste Keyword_Israel_National_ID est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2289">A keyword from Keyword_Israel_National_ID is found.</span></span>
- <span data-ttu-id="d8d84-2290">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2290">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-2291">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-2291">Keywords</span></span>

#### <a name="keywordisraelnationalid"></a><span data-ttu-id="d8d84-2292">Keyword_Israel_National_ID</span><span class="sxs-lookup"><span data-stu-id="d8d84-2292">Keyword_Israel_National_ID</span></span>

- <span data-ttu-id="d8d84-2293">מספר זהות
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2293">מספר זהות</span></span> 
- <span data-ttu-id="d8d84-2294">Numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="d8d84-2294">National ID Number</span></span>
   
## <a name="italy-drivers-license-number"></a><span data-ttu-id="d8d84-2295">Numéro de permis de conduire Italie</span><span class="sxs-lookup"><span data-stu-id="d8d84-2295">Italy Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-2296">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-2296">Format</span></span>

<span data-ttu-id="d8d84-2297">Une combinaison de 10 lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2297">A combination of 10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-2298">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2298">Pattern</span></span>

- <span data-ttu-id="d8d84-2299">Une combinaison de 10 lettres et chiffres :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2299">A combination of 10 letters and digits:</span></span>
- <span data-ttu-id="d8d84-2300">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="d8d84-2300">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="d8d84-2301">La lettre « A » ou « V » (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="d8d84-2301">The letter "A" or "V" (not case sensitive)</span></span> 
- <span data-ttu-id="d8d84-2302">Sept lettres (ne respectent pas la casse), des chiffres ou le trait de soulignement</span><span class="sxs-lookup"><span data-stu-id="d8d84-2302">Seven letters (not case sensitive), digits, or the underscore character</span></span> 
- <span data-ttu-id="d8d84-2303">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="d8d84-2303">One letter (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-2304">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2304">Checksum</span></span>

<span data-ttu-id="d8d84-2305">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-2305">No</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-2306">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-2306">Definition</span></span>

<span data-ttu-id="d8d84-2307">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2307">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2308">L’expression régulière Regex_italy_drivers_license_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2308">The regular expression Regex_italy_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2309">Un mot clé figurant dans la liste Keyword_italy_drivers_license_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2309">A keyword from Keyword_italy_drivers_license_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-2310">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-2310">Keywords</span></span>

#### <a name="keyworditalydriverslicensenumber"></a><span data-ttu-id="d8d84-2311">Keyword_italy_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="d8d84-2311">Keyword_italy_drivers_license_number</span></span>

- <span data-ttu-id="d8d84-2312">numero di patente di guida
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2312">numero di patente di guida</span></span> 
- <span data-ttu-id="d8d84-2313">patente di guida
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2313">patente di guida</span></span> 
   
## <a name="japan-bank-account-number"></a><span data-ttu-id="d8d84-2314">Numéro de compte bancaire Japon</span><span class="sxs-lookup"><span data-stu-id="d8d84-2314">Japan Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-2315">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-2315">Format</span></span>

<span data-ttu-id="d8d84-2316">Sept ou huit chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2316">Seven or eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-2317">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2317">Pattern</span></span>

<span data-ttu-id="d8d84-2318">Numéro de compte bancaire :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2318">Bank account number:</span></span>
- <span data-ttu-id="d8d84-2319">Sept ou huit chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2319">Seven or eight digits</span></span>
- <span data-ttu-id="d8d84-2320">Code guichet du compte bancaire :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2320">Bank account branch code:</span></span>
- <span data-ttu-id="d8d84-2321">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2321">Four digits</span></span> 
- <span data-ttu-id="d8d84-2322">Un espace ou un tiret (facultatif)</span><span class="sxs-lookup"><span data-stu-id="d8d84-2322">A space or dash (optional)</span></span> 
- <span data-ttu-id="d8d84-2323">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2323">Three digits</span></span>

<span data-ttu-id="d8d84-2324">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2324">Checksum</span></span>

<span data-ttu-id="d8d84-2325">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-2325">No</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-2326">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-2326">Definition</span></span>

<span data-ttu-id="d8d84-2327">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2327">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2328">La fonction Func_jp_bank_account trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2328">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2329">Un mot clé figurant dans la liste Keyword_jp_bank_account est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2329">A keyword from Keyword_jp_bank_account is found.</span></span>
- <span data-ttu-id="d8d84-2330">L’une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2330">One of the following is true:</span></span>
- <span data-ttu-id="d8d84-2331">La fonction Func_jp_bank_account_branch_code trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2331">The function Func_jp_bank_account_branch_code finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2332">Un mot clé figurant dans la liste Keyword_jp_bank_branch_code est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2332">A keyword from Keyword_jp_bank_branch_code is found.</span></span>

<span data-ttu-id="d8d84-2333">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2333">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2334">La fonction Func_jp_bank_account trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2334">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2335">Un mot clé figurant dans la liste Keyword_jp_bank_account est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2335">A keyword from Keyword_jp_bank_account is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-2336">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-2336">Keywords</span></span>

#### <a name="keywordjpbankaccount"></a><span data-ttu-id="d8d84-2337">Keyword_jp_bank_account</span><span class="sxs-lookup"><span data-stu-id="d8d84-2337">Keyword_jp_bank_account</span></span>

- <span data-ttu-id="d8d84-2338">Numéro de compte courant
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2338">Checking Account Number</span></span> 
- <span data-ttu-id="d8d84-2339">Compte courant
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2339">Checking Account</span></span> 
- <span data-ttu-id="d8d84-2340"># compte courant
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2340">Checking Account #</span></span> 
- <span data-ttu-id="d8d84-2341">Numéro compte courant
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2341">Checking Acct Number</span></span> 
- <span data-ttu-id="d8d84-2342"># compte courant
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2342">Checking Acct #</span></span> 
- <span data-ttu-id="d8d84-2343">N° de compte courant
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2343">Checking Acct No.</span></span> 
- <span data-ttu-id="d8d84-2344">N° de compte courant
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2344">Checking Account No.</span></span> 
- <span data-ttu-id="d8d84-2345">Numéro de compte bancaire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2345">Bank Account Number</span></span> 
- <span data-ttu-id="d8d84-2346">Compte bancaire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2346">Bank Account</span></span> 
- <span data-ttu-id="d8d84-2347"># Compte bancaire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2347">Bank Account #</span></span> 
- <span data-ttu-id="d8d84-2348">Numéro de compte bancaire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2348">Bank Acct Number</span></span> 
- <span data-ttu-id="d8d84-2349"># Compte bancaire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2349">Bank Acct #</span></span> 
- <span data-ttu-id="d8d84-2350">N° de compte bancaire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2350">Bank Acct No.</span></span> 
- <span data-ttu-id="d8d84-2351">N° de compte bancaire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2351">Bank Account No.</span></span> 
- <span data-ttu-id="d8d84-2352">Numéro de compte d’épargne
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2352">Savings Account Number</span></span> 
- <span data-ttu-id="d8d84-2353">Compte d’épargne</span><span class="sxs-lookup"><span data-stu-id="d8d84-2353">Savings Account</span></span> 
- <span data-ttu-id="d8d84-2354">N° de compte d’épargne
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2354">Savings Account #</span></span> 
- <span data-ttu-id="d8d84-2355">Numéro de compte d’épargne
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2355">Savings Acct Number</span></span> 
- <span data-ttu-id="d8d84-2356"># compte d’épargne
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2356">Savings Acct #</span></span> 
- <span data-ttu-id="d8d84-2357">N° de compte d’épargne
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2357">Savings Acct No.</span></span> 
- <span data-ttu-id="d8d84-2358">N° de compte d’épargne
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2358">Savings Account No.</span></span> 
- <span data-ttu-id="d8d84-2359">Numéro de compte de débit
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2359">Debit Account Number</span></span> 
- <span data-ttu-id="d8d84-2360">Compte de débit
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2360">Debit Account</span></span> 
- <span data-ttu-id="d8d84-2361"># Compte de débit
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2361">Debit Account #</span></span> 
- <span data-ttu-id="d8d84-2362">Numéro de compte de débit
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2362">Debit Acct Number</span></span> 
- <span data-ttu-id="d8d84-2363"># Compte de débit
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2363">Debit Acct #</span></span> 
- <span data-ttu-id="d8d84-2364">N° de compte de débit
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2364">Debit Acct No.</span></span> 
- <span data-ttu-id="d8d84-2365">N° de compte de débit
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2365">Debit Account No.</span></span> 
- <span data-ttu-id="d8d84-2366">口座番号を当座預金口座の確認
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2366">口座番号を当座預金口座の確認</span></span> 
- <span data-ttu-id="d8d84-2367">＃アカウントの確認、勘定番号の確認
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2367">＃アカウントの確認、勘定番号の確認</span></span> 
- <span data-ttu-id="d8d84-2368">＃勘定の確認
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2368">＃勘定の確認</span></span> 
- <span data-ttu-id="d8d84-2369">勘定番号の確認
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2369">勘定番号の確認</span></span> 
- <span data-ttu-id="d8d84-2370">口座番号の確認
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2370">口座番号の確認</span></span> 
- <span data-ttu-id="d8d84-2371">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="d8d84-2371">銀行口座番号</span></span> 
- <span data-ttu-id="d8d84-2372">銀行口座</span><span class="sxs-lookup"><span data-stu-id="d8d84-2372">銀行口座</span></span> 
- <span data-ttu-id="d8d84-2373">銀行口座＃
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2373">銀行口座＃</span></span> 
- <span data-ttu-id="d8d84-2374">銀行の勘定番号
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2374">銀行の勘定番号</span></span> 
- <span data-ttu-id="d8d84-2375">銀行のacct＃
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2375">銀行のacct＃</span></span> 
- <span data-ttu-id="d8d84-2376">銀行の勘定いいえ
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2376">銀行の勘定いいえ</span></span> 
- <span data-ttu-id="d8d84-2377">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="d8d84-2377">銀行口座番号</span></span>
- <span data-ttu-id="d8d84-2378">
普通預金口座番号
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2378">普通預金口座番号</span></span> 
- <span data-ttu-id="d8d84-2379">預金口座
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2379">預金口座</span></span> 
- <span data-ttu-id="d8d84-2380">貯蓄口座＃
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2380">貯蓄口座＃</span></span> 
- <span data-ttu-id="d8d84-2381">貯蓄勘定の数
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2381">貯蓄勘定の数</span></span> 
- <span data-ttu-id="d8d84-2382">貯蓄勘定＃
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2382">貯蓄勘定＃</span></span> 
- <span data-ttu-id="d8d84-2383">貯蓄勘定番号
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2383">貯蓄勘定番号</span></span> 
- <span data-ttu-id="d8d84-2384">普通預金口座番号
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2384">普通預金口座番号</span></span> 
- <span data-ttu-id="d8d84-2385">引き落とし口座番号
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2385">引き落とし口座番号</span></span> 
- <span data-ttu-id="d8d84-2386">口座番号</span><span class="sxs-lookup"><span data-stu-id="d8d84-2386">口座番号</span></span> 
- <span data-ttu-id="d8d84-2387">口座番号 #
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2387">口座番号＃</span></span> 
- <span data-ttu-id="d8d84-2388">デビットのacct番号
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2388">デビットのacct番号</span></span> 
- <span data-ttu-id="d8d84-2389">デビット勘定＃
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2389">デビット勘定＃</span></span> 
- <span data-ttu-id="d8d84-2390">デビットACCTの番号
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2390">デビットACCTの番号</span></span> 
- <span data-ttu-id="d8d84-2391">デビット口座番号
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2391">デビット口座番号</span></span> 

#### <a name="keywordjpbankbranchcode"></a><span data-ttu-id="d8d84-2392">Keyword_jp_bank_branch_code</span><span class="sxs-lookup"><span data-stu-id="d8d84-2392">Keyword_jp_bank_branch_code</span></span>

<span data-ttu-id="d8d84-2393">Otemachi</span><span class="sxs-lookup"><span data-stu-id="d8d84-2393">Otemachi</span></span>

## <a name="japan-drivers-license-number"></a><span data-ttu-id="d8d84-2394">Numéro de permis de conduire Japon</span><span class="sxs-lookup"><span data-stu-id="d8d84-2394">Japan Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-2395">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-2395">Format</span></span>

<span data-ttu-id="d8d84-2396">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2396">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-2397">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2397">Pattern</span></span>

<span data-ttu-id="d8d84-2398">12 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="d8d84-2398">12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-2399">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2399">Checksum</span></span>

<span data-ttu-id="d8d84-2400">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-2400">No</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-2401">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-2401">Definition</span></span>

<span data-ttu-id="d8d84-2402">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2402">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2403">La fonction Func_jp_drivers_license_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2403">The function Func_jp_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2404">Un mot clé figurant dans la liste Keyword_jp_drivers_license_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2404">A keyword from Keyword_jp_drivers_license_number is found.</span></span>

```
<!-- Japan Driver's License Number -->
<Entity id="c6011143-d087-451c-8313-7f6d4aed2270" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_drivers_license_number" />
        <Match idRef ="Keyword_jp_drivers_license_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8d84-2405">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-2405">Keywords</span></span>

#### <a name="keywordjpdriverslicensenumber"></a><span data-ttu-id="d8d84-2406">Keyword_jp_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="d8d84-2406">Keyword_jp_drivers_license_number</span></span>

- <span data-ttu-id="d8d84-2407">dl#</span><span class="sxs-lookup"><span data-stu-id="d8d84-2407">dl#</span></span> 
- <span data-ttu-id="d8d84-2408">DL #</span><span class="sxs-lookup"><span data-stu-id="d8d84-2408">DL＃</span></span> 
- <span data-ttu-id="d8d84-2409">dls#</span><span class="sxs-lookup"><span data-stu-id="d8d84-2409">dls#</span></span> 
- <span data-ttu-id="d8d84-2410">LISTES DE DISTRIBUTION #</span><span class="sxs-lookup"><span data-stu-id="d8d84-2410">DLS＃</span></span> 
- <span data-ttu-id="d8d84-2411">driver license</span><span class="sxs-lookup"><span data-stu-id="d8d84-2411">driver license</span></span> 
- <span data-ttu-id="d8d84-2412">driver licenses</span><span class="sxs-lookup"><span data-stu-id="d8d84-2412">driver licenses</span></span> 
- <span data-ttu-id="d8d84-2413">drivers license</span><span class="sxs-lookup"><span data-stu-id="d8d84-2413">drivers license</span></span> 
- <span data-ttu-id="d8d84-2414">driver’s license</span><span class="sxs-lookup"><span data-stu-id="d8d84-2414">driver's license</span></span> 
- <span data-ttu-id="d8d84-2415">drivers licenses</span><span class="sxs-lookup"><span data-stu-id="d8d84-2415">drivers licenses</span></span> 
- <span data-ttu-id="d8d84-2416">driver’s licenses</span><span class="sxs-lookup"><span data-stu-id="d8d84-2416">driver's licenses</span></span> 
- <span data-ttu-id="d8d84-2417">permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2417">driving licence</span></span> 
- <span data-ttu-id="d8d84-2418">lic#</span><span class="sxs-lookup"><span data-stu-id="d8d84-2418">lic#</span></span> 
- <span data-ttu-id="d8d84-2419">LIC #</span><span class="sxs-lookup"><span data-stu-id="d8d84-2419">LIC＃</span></span> 
- <span data-ttu-id="d8d84-2420">#permis</span><span class="sxs-lookup"><span data-stu-id="d8d84-2420">lics#</span></span> 
- <span data-ttu-id="d8d84-2421">id d’état</span><span class="sxs-lookup"><span data-stu-id="d8d84-2421">state id</span></span> 
- <span data-ttu-id="d8d84-2422">identification d’état
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2422">state identification</span></span> 
- <span data-ttu-id="d8d84-2423">numéro d’identification d’état
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2423">state identification number</span></span> 
- <span data-ttu-id="d8d84-2424">低所得国＃
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2424">低所得国＃</span></span> 
- <span data-ttu-id="d8d84-2425">免許証</span><span class="sxs-lookup"><span data-stu-id="d8d84-2425">免許証</span></span> 
- <span data-ttu-id="d8d84-2426">状態ID</span><span class="sxs-lookup"><span data-stu-id="d8d84-2426">状態ID</span></span>
- <span data-ttu-id="d8d84-2427">
状態の識別
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2427">状態の識別</span></span> 
- <span data-ttu-id="d8d84-2428">状態の識別番号
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2428">状態の識別番号</span></span> 
- <span data-ttu-id="d8d84-2429">運転免許</span><span class="sxs-lookup"><span data-stu-id="d8d84-2429">運転免許</span></span> 
- <span data-ttu-id="d8d84-2430">運転免許証</span><span class="sxs-lookup"><span data-stu-id="d8d84-2430">運転免許証</span></span> 
- <span data-ttu-id="d8d84-2431">運転免許証番号</span><span class="sxs-lookup"><span data-stu-id="d8d84-2431">運転免許証番号</span></span> 
   
## <a name="japan-passport-number"></a><span data-ttu-id="d8d84-2432">Numéro de passeport Japon</span><span class="sxs-lookup"><span data-stu-id="d8d84-2432">Japan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-2433">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-2433">Format</span></span>

<span data-ttu-id="d8d84-2434">Deux lettres suivies de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2434">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-2435">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2435">Pattern</span></span>

<span data-ttu-id="d8d84-2436">Deux lettres (ne respectant pas la casse) suivies de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2436">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-2437">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2437">Checksum</span></span>

<span data-ttu-id="d8d84-2438">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-2438">No</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-2439">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-2439">Definition</span></span>

<span data-ttu-id="d8d84-2440">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2440">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2441">La fonction Func_jp_passport trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2441">The function Func_jp_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2442">Un mot clé figurant dans la liste Keyword_jp_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2442">A keyword from Keyword_jp_passport is found.</span></span>

```
<!-- Japan Passport Number -->
<Entity id="75177310-1a09-4613-bf6d-833aae3743f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_passport" />
        <Match idRef="Keyword_jp_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8d84-2443">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-2443">Keywords</span></span>

#### <a name="keywordjppassport"></a><span data-ttu-id="d8d84-2444">Keyword_jp_passport</span><span class="sxs-lookup"><span data-stu-id="d8d84-2444">Keyword_jp_passport</span></span>

- <span data-ttu-id="d8d84-2445">パスポート
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2445">パスポート</span></span> 
- <span data-ttu-id="d8d84-2446">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2446">パスポート番号</span></span> 
- <span data-ttu-id="d8d84-2447">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2447">パスポートのNum</span></span> 
- <span data-ttu-id="d8d84-2448">パスポート＃
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2448">パスポート＃</span></span> 
   
## <a name="japan-resident-registration-number"></a><span data-ttu-id="d8d84-2449">Matricule de résident Japon</span><span class="sxs-lookup"><span data-stu-id="d8d84-2449">Japan Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-2450">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-2450">Format</span></span>

<span data-ttu-id="d8d84-2451">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2451">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-2452">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2452">Pattern</span></span>

<span data-ttu-id="d8d84-2453">11 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="d8d84-2453">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-2454">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2454">Checksum</span></span>

<span data-ttu-id="d8d84-2455">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-2455">No</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-2456">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-2456">Definition</span></span>

<span data-ttu-id="d8d84-2457">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2457">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2458">La fonction Func_jp_resident_registration_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2458">The function Func_jp_resident_registration_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2459">Un mot clé figurant dans la liste Keyword_jp_resident_registration_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2459">A keyword from Keyword_jp_resident_registration_number is found.</span></span>

```
<!-- Japan Resident Registration Number -->
<Entity id="01c1209b-6389-4faf-a5f8-3f7e13899652" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_resident_registration_number" />
        <Match idRef ="Keyword_jp_resident_registration_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8d84-2460">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-2460">Keywords</span></span>

#### <a name="keywordjpresidentregistrationnumber"></a><span data-ttu-id="d8d84-2461">Keyword_jp_resident_registration_number</span><span class="sxs-lookup"><span data-stu-id="d8d84-2461">Keyword_jp_resident_registration_number</span></span>

- <span data-ttu-id="d8d84-2462">Numéro d’enregistrement du résident</span><span class="sxs-lookup"><span data-stu-id="d8d84-2462">Resident Registration Number</span></span>
- <span data-ttu-id="d8d84-2463">Numéro d’enregistrement du résident
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2463">Resident Register Number</span></span> 
- <span data-ttu-id="d8d84-2464">Numéro de base d’enregistrement des résidents
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2464">Residents Basic Registry Number</span></span> 
- <span data-ttu-id="d8d84-2465">N° d’enregistrement du résident
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2465">Resident Registration No.</span></span> 
- <span data-ttu-id="d8d84-2466">N° d’enregistrement du résident
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2466">Resident Register No.</span></span> 
- <span data-ttu-id="d8d84-2467">N° de base d’enregistrement des résidents
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2467">Residents Basic Registry No.</span></span> 
- <span data-ttu-id="d8d84-2468">N° d’enregistrement du résident de base
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2468">Basic Resident Register No.</span></span> 
- <span data-ttu-id="d8d84-2469">住民登録番号、登録番号をレジデント
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2469">住民登録番号、登録番号をレジデント</span></span> 
- <span data-ttu-id="d8d84-2470">住民基本登録番号、登録番号
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2470">住民基本登録番号、登録番号</span></span> 
- <span data-ttu-id="d8d84-2471">住民基本レジストリ番号を常駐
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2471">住民基本レジストリ番号を常駐</span></span> 
- <span data-ttu-id="d8d84-2472">登録番号を常駐住民基本台帳登録番号
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2472">登録番号を常駐住民基本台帳登録番号</span></span> 

   
## <a name="japan-social-insurance-number-sin"></a><span data-ttu-id="d8d84-2473">Numéro d'assurance sociale Japon</span><span class="sxs-lookup"><span data-stu-id="d8d84-2473">Japan Social Insurance Number (SIN)</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-2474">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-2474">Format</span></span>

<span data-ttu-id="d8d84-2475">7 à 12 chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2475">7-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-2476">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2476">Pattern</span></span>

<span data-ttu-id="d8d84-2477">7 à 12 chiffres :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2477">7-12 digits:</span></span>
- <span data-ttu-id="d8d84-2478">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2478">Four digits</span></span> 
- <span data-ttu-id="d8d84-2479">Un trait d’union (facultatif)</span><span class="sxs-lookup"><span data-stu-id="d8d84-2479">A hyphen (optional)</span></span> 
- <span data-ttu-id="d8d84-2480">Six chiffres ou</span><span class="sxs-lookup"><span data-stu-id="d8d84-2480">Six digits OR</span></span>
- <span data-ttu-id="d8d84-2481">7 à 12 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="d8d84-2481">7-12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-2482">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2482">Checksum</span></span>

<span data-ttu-id="d8d84-2483">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-2483">No</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-2484">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-2484">Definition</span></span>

<span data-ttu-id="d8d84-2485">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2485">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2486">La fonction Func_jp_sin trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2486">The function Func_jp_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2487">Un mot clé figurant dans la liste Keyword_jp_sin est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2487">A keyword from Keyword_jp_sin is found.</span></span>

<span data-ttu-id="d8d84-2488">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2488">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2489">La fonction Func_jp_sin_pre_1997 trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2489">The function Func_jp_sin_pre_1997 finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2490">Un mot clé figurant dans la liste Keyword_jp_sin est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2490">A keyword from Keyword_jp_sin is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-2491">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-2491">Keywords</span></span>

#### <a name="keywordjpsin"></a><span data-ttu-id="d8d84-2492">Keyword_jp_sin</span><span class="sxs-lookup"><span data-stu-id="d8d84-2492">Keyword_jp_sin</span></span>

- <span data-ttu-id="d8d84-2493">N° d’assurance sociale
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2493">Social Insurance No.</span></span> 
- <span data-ttu-id="d8d84-2494">Numéro d’assurance sociale
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2494">Social Insurance Num</span></span> 
- <span data-ttu-id="d8d84-2495">Numéro d’assurance sociale
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2495">Social Insurance Number</span></span> 
- <span data-ttu-id="d8d84-2496">社会保険のテンキー
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2496">社会保険のテンキー</span></span> 
- <span data-ttu-id="d8d84-2497">社会保険番号
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2497">社会保険番号</span></span> 

## <a name="japanese-residence-card-number"></a><span data-ttu-id="d8d84-2498">Numéro de carte de résidence (japonais)</span><span class="sxs-lookup"><span data-stu-id="d8d84-2498">Japanese Residence Card Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-2499">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-2499">Format</span></span>

<span data-ttu-id="d8d84-2500">12 lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2500">12 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-2501">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2501">Pattern</span></span>

<span data-ttu-id="d8d84-2502">12 lettres et chiffres :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2502">12 letters and digits:</span></span>
- <span data-ttu-id="d8d84-2503">Deux lettres (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="d8d84-2503">Two letters (not case sensitive)</span></span>
- <span data-ttu-id="d8d84-2504">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2504">Eight digits</span></span> 
- <span data-ttu-id="d8d84-2505">Deux lettres (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="d8d84-2505">Two letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-2506">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2506">Checksum</span></span>

<span data-ttu-id="d8d84-2507">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-2507">No</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-2508">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-2508">Definition</span></span>

<span data-ttu-id="d8d84-2509">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2509">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2510">L’expression régulière Regex_jp_residence_card_number recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2510">The regular expression Regex_jp_residence_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2511">Un mot clé à partir de Keyword_jp_residence_card_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2511">A keyword from Keyword_jp_residence_card_number is found.</span></span>

```
<!--Japan Residence Card Number-->
-<Entity id="ac36fef2-a289-4e2c-bb48-b02366e89fc0" recommendedConfidence="75" patternsProximity="300">
   -<Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_jp_residence_card_number"/>
      <Match idRef="Keyword_jp_residence_card_number"/>
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8d84-2512">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-2512">Keywords</span></span>

#### <a name="keywordjpresidencecardnumber"></a><span data-ttu-id="d8d84-2513">Keyword_jp_residence_card_number</span><span class="sxs-lookup"><span data-stu-id="d8d84-2513">Keyword_jp_residence_card_number</span></span>

- <span data-ttu-id="d8d84-2514">Numéro de carte de résidence</span><span class="sxs-lookup"><span data-stu-id="d8d84-2514">Residence card number</span></span>
- <span data-ttu-id="d8d84-2515">N° de carte de résidence</span><span class="sxs-lookup"><span data-stu-id="d8d84-2515">Residence card no</span></span>
- <span data-ttu-id="d8d84-2516">Résidence carte #</span><span class="sxs-lookup"><span data-stu-id="d8d84-2516">Residence card #</span></span>
- <span data-ttu-id="d8d84-2517">在留カード番号</span><span class="sxs-lookup"><span data-stu-id="d8d84-2517">在留カード番号</span></span>
   
## <a name="malaysia-id-card-number"></a><span data-ttu-id="d8d84-2518">Numéro de carte d’identité Malaisie</span><span class="sxs-lookup"><span data-stu-id="d8d84-2518">Malaysia ID Card Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-2519">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-2519">Format</span></span>

<span data-ttu-id="d8d84-2520">12 chiffres contenant éventuellement des traits d’union</span><span class="sxs-lookup"><span data-stu-id="d8d84-2520">12 digits containing optional hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-2521">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2521">Pattern</span></span>

<span data-ttu-id="d8d84-2522">12 chiffres :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2522">12 digits:</span></span>
- <span data-ttu-id="d8d84-2523">Six chiffres au format AAMMJJ correspondant à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="d8d84-2523">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="d8d84-2524">Un tiret (facultatif) </span><span class="sxs-lookup"><span data-stu-id="d8d84-2524">A dash (optional)</span></span> 
- <span data-ttu-id="d8d84-2525">Le code à deux lettres du lieu de naissance </span><span class="sxs-lookup"><span data-stu-id="d8d84-2525">Two-letter place-of-birth code</span></span> 
- <span data-ttu-id="d8d84-2526">Un tiret (facultatif) </span><span class="sxs-lookup"><span data-stu-id="d8d84-2526">A dash (optional)</span></span> 
- <span data-ttu-id="d8d84-2527">Trois chiffres aléatoires </span><span class="sxs-lookup"><span data-stu-id="d8d84-2527">Three random digits</span></span> 
- <span data-ttu-id="d8d84-2528">Code de sexe à un chiffre</span><span class="sxs-lookup"><span data-stu-id="d8d84-2528">One-digit gender code</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-2529">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2529">Checksum</span></span>

<span data-ttu-id="d8d84-2530">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-2530">No</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-2531">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-2531">Definition</span></span>

<span data-ttu-id="d8d84-2532">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2532">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2533">L’expression régulière Regex_malaysia_id_card_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2533">The regular expression Regex_malaysia_id_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2534">Un mot clé figurant dans la liste Keyword_malaysia_id_card_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2534">A keyword from Keyword_malaysia_id_card_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-2535">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-2535">Keywords</span></span>
   
#### <a name="keywordmalaysiaidcardnumber"></a><span data-ttu-id="d8d84-2536">Keyword_malaysia_id_card_number</span><span class="sxs-lookup"><span data-stu-id="d8d84-2536">Keyword_malaysia_id_card_number</span></span>

- <span data-ttu-id="d8d84-2537">fiche d’application numérique</span><span class="sxs-lookup"><span data-stu-id="d8d84-2537">digital application card</span></span>
- <span data-ttu-id="d8d84-2538">i / c</span><span class="sxs-lookup"><span data-stu-id="d8d84-2538">i/c</span></span>
- <span data-ttu-id="d8d84-2539">i / c aucune</span><span class="sxs-lookup"><span data-stu-id="d8d84-2539">i/c no</span></span>
- <span data-ttu-id="d8d84-2540">IC</span><span class="sxs-lookup"><span data-stu-id="d8d84-2540">ic</span></span>
- <span data-ttu-id="d8d84-2541">IC aucune</span><span class="sxs-lookup"><span data-stu-id="d8d84-2541">ic no</span></span>
- <span data-ttu-id="d8d84-2542">carte d’identité</span><span class="sxs-lookup"><span data-stu-id="d8d84-2542">id card</span></span>
- <span data-ttu-id="d8d84-2543">Carte d’identification</span><span class="sxs-lookup"><span data-stu-id="d8d84-2543">identification Card</span></span>
- <span data-ttu-id="d8d84-2544">Carte d’identité</span><span class="sxs-lookup"><span data-stu-id="d8d84-2544">identity card</span></span>
- <span data-ttu-id="d8d84-2545">k/p</span><span class="sxs-lookup"><span data-stu-id="d8d84-2545">k/p</span></span>
- <span data-ttu-id="d8d84-2546">k/p aucune</span><span class="sxs-lookup"><span data-stu-id="d8d84-2546">k/p no</span></span>
- <span data-ttu-id="d8d84-2547">kad akuan diri</span><span class="sxs-lookup"><span data-stu-id="d8d84-2547">kad akuan diri</span></span>
- <span data-ttu-id="d8d84-2548">aplikasi kad numérique</span><span class="sxs-lookup"><span data-stu-id="d8d84-2548">kad aplikasi digital</span></span>
- <span data-ttu-id="d8d84-2549">kad pengenalan Malaisie</span><span class="sxs-lookup"><span data-stu-id="d8d84-2549">kad pengenalan malaysia</span></span>
- <span data-ttu-id="d8d84-2550">KP</span><span class="sxs-lookup"><span data-stu-id="d8d84-2550">kp</span></span>
- <span data-ttu-id="d8d84-2551">KP aucune</span><span class="sxs-lookup"><span data-stu-id="d8d84-2551">kp no</span></span>
- <span data-ttu-id="d8d84-2552">mykad</span><span class="sxs-lookup"><span data-stu-id="d8d84-2552">mykad</span></span>
- <span data-ttu-id="d8d84-2553">mykas</span><span class="sxs-lookup"><span data-stu-id="d8d84-2553">mykas</span></span>
- <span data-ttu-id="d8d84-2554">mykid</span><span class="sxs-lookup"><span data-stu-id="d8d84-2554">mykid</span></span>
- <span data-ttu-id="d8d84-2555">mypr</span><span class="sxs-lookup"><span data-stu-id="d8d84-2555">mypr</span></span>
- <span data-ttu-id="d8d84-2556">mytentera</span><span class="sxs-lookup"><span data-stu-id="d8d84-2556">mytentera</span></span>
- <span data-ttu-id="d8d84-2557">carte d’identité Malaisie</span><span class="sxs-lookup"><span data-stu-id="d8d84-2557">malaysia identity card</span></span>
- <span data-ttu-id="d8d84-2558">Malaisie carte d’identité</span><span class="sxs-lookup"><span data-stu-id="d8d84-2558">malaysian identity card</span></span>
- <span data-ttu-id="d8d84-2559">NRIC</span><span class="sxs-lookup"><span data-stu-id="d8d84-2559">nric</span></span>
- <span data-ttu-id="d8d84-2560">carte d’identification personnelle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2560">personal identification card</span></span>
   
## <a name="netherlands-citizens-service-bsn-number"></a><span data-ttu-id="d8d84-2561">Numéro de service du citoyen (BSN) Pays-Bas</span><span class="sxs-lookup"><span data-stu-id="d8d84-2561">Netherlands Citizen's Service (BSN) Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-2562">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-2562">Format</span></span>

<span data-ttu-id="d8d84-2563">8 à 9 chiffres contenant éventuellement des espaces</span><span class="sxs-lookup"><span data-stu-id="d8d84-2563">8-9 digits containing optional spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-2564">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2564">Pattern</span></span>

<span data-ttu-id="d8d84-2565">8 à 9 chiffres :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2565">8-9 digits:</span></span>
- <span data-ttu-id="d8d84-2566">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2566">Three digits</span></span> 
- <span data-ttu-id="d8d84-2567">Un espace (facultatif) </span><span class="sxs-lookup"><span data-stu-id="d8d84-2567">A space (optional)</span></span> 
- <span data-ttu-id="d8d84-2568">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2568">Three digits</span></span> 
- <span data-ttu-id="d8d84-2569">Un espace (facultatif) </span><span class="sxs-lookup"><span data-stu-id="d8d84-2569">A space (optional)</span></span> 
- <span data-ttu-id="d8d84-2570">2 à 3 chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2570">2-3 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-2571">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2571">Checksum</span></span>

<span data-ttu-id="d8d84-2572">Oui</span><span class="sxs-lookup"><span data-stu-id="d8d84-2572">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-2573">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-2573">Definition</span></span>

<span data-ttu-id="d8d84-2574">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2574">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2575">La fonction Func_netherlands_bsn trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2575">The function Func_netherlands_bsn finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2576">Un mot clé figurant dans la liste Keyword_netherlands_bsn est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2576">A keyword from Keyword_netherlands_bsn is found.</span></span>
- <span data-ttu-id="d8d84-2577">La fonction Func_eu_date2 trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2577">The function Func_eu_date2 finds a date in the right date format.</span></span>
- <span data-ttu-id="d8d84-2578">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2578">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-2579">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-2579">Keywords</span></span>

#### <a name="keywordnetherlandsbsn"></a><span data-ttu-id="d8d84-2580">Keyword_netherlands_bsn</span><span class="sxs-lookup"><span data-stu-id="d8d84-2580">Keyword_netherlands_bsn</span></span>

- <span data-ttu-id="d8d84-2581">Citizen service number
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2581">Citizen service number</span></span> 
- <span data-ttu-id="d8d84-2582">BSN

</span><span class="sxs-lookup"><span data-stu-id="d8d84-2582">BSN</span></span> 
- <span data-ttu-id="d8d84-2583">Burgerservicenummer
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2583">Burgerservicenummer</span></span> 
- <span data-ttu-id="d8d84-2584">Sofinummer
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2584">Sofinummer</span></span> 
- <span data-ttu-id="d8d84-2585">Persoonsgebonden nummer
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2585">Persoonsgebonden nummer</span></span> 
- <span data-ttu-id="d8d84-2586">Persoonsnummer
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2586">Persoonsnummer</span></span>    

   
## <a name="new-zealand-ministry-of-health-number"></a><span data-ttu-id="d8d84-2587">Numéro du Ministère de la santé Nouvelle-Zélande</span><span class="sxs-lookup"><span data-stu-id="d8d84-2587">New Zealand Ministry of Health Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-2588">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-2588">Format</span></span>

<span data-ttu-id="d8d84-2589">Trois lettres, un espace (facultatif) et quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2589">Three letters, a space (optional), and four digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-2590">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2590">Pattern</span></span>

<span data-ttu-id="d8d84-2591">Trois lettres (pas la casse), un espace (facultatif) quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2591">Three letters (not case sensitive) a space (optional) four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-2592">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2592">Checksum</span></span>

<span data-ttu-id="d8d84-2593">Oui</span><span class="sxs-lookup"><span data-stu-id="d8d84-2593">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-2594">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-2594">Definition</span></span>

<span data-ttu-id="d8d84-2595">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2595">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2596">La fonction Func_new_zealand_ministry_of_health_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2596">The function Func_new_zealand_ministry_of_health_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2597">Un mot clé figurant dans la liste Keyword_nz_terms est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2597">A keyword from Keyword_nz_terms is found.</span></span>
- <span data-ttu-id="d8d84-2598">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2598">The checksum passes.</span></span>

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

<span data-ttu-id="d8d84-2599">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-2599">Keywords</span></span>

<span data-ttu-id="d8d84-2600">Keyword_nz_terms</span><span class="sxs-lookup"><span data-stu-id="d8d84-2600">Keyword_nz_terms</span></span>

- <span data-ttu-id="d8d84-2601">NHI
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2601">NHI</span></span> 
- <span data-ttu-id="d8d84-2602">Nouvelle-Zélande</span><span class="sxs-lookup"><span data-stu-id="d8d84-2602">New Zealand</span></span> 
- <span data-ttu-id="d8d84-2603">Intégrité</span><span class="sxs-lookup"><span data-stu-id="d8d84-2603">Health</span></span> 
- <span data-ttu-id="d8d84-2604">treatment
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2604">treatment</span></span> 
   
## <a name="norway-identification-number"></a><span data-ttu-id="d8d84-2605">Numéro d’identification Norvège</span><span class="sxs-lookup"><span data-stu-id="d8d84-2605">Norway Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-2606">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-2606">Format</span></span>

<span data-ttu-id="d8d84-2607">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2607">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-2608">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2608">Pattern</span></span>

<span data-ttu-id="d8d84-2609">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2609">11 digits:</span></span>
- <span data-ttu-id="d8d84-2610">Six chiffres au format JJMMAA qui correspondent à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="d8d84-2610">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="d8d84-2611">Numéro individuel à trois chiffres </span><span class="sxs-lookup"><span data-stu-id="d8d84-2611">Three-digit individual number</span></span> 
- <span data-ttu-id="d8d84-2612">Deux chiffres de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2612">Two check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-2613">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2613">Checksum</span></span>

<span data-ttu-id="d8d84-2614">Oui</span><span class="sxs-lookup"><span data-stu-id="d8d84-2614">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-2615">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-2615">Definition</span></span>

<span data-ttu-id="d8d84-2616">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2616">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2617">La fonction Func_norway_id_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2617">The function Func_norway_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2618">Un mot clé figurant dans la liste Keyword_norway_id_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2618">A keyword from Keyword_norway_id_number is found.</span></span>
- <span data-ttu-id="d8d84-2619">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2619">The checksum passes.</span></span>
- <span data-ttu-id="d8d84-2620">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2620">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2621">La fonction Func_norway_id_numbe trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2621">The function Func_norway_id_numbe finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2622">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2622">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-2623">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-2623">Keywords</span></span>

#### <a name="keywordnorwayidnumber"></a><span data-ttu-id="d8d84-2624">Keyword_norway_id_number</span><span class="sxs-lookup"><span data-stu-id="d8d84-2624">Keyword_norway_id_number</span></span>

- <span data-ttu-id="d8d84-2625">Personal identification number</span><span class="sxs-lookup"><span data-stu-id="d8d84-2625">Personal identification number</span></span>
- <span data-ttu-id="d8d84-2626">Norwegian ID Number</span><span class="sxs-lookup"><span data-stu-id="d8d84-2626">Norwegian ID Number</span></span>
- <span data-ttu-id="d8d84-2627">ID Number</span><span class="sxs-lookup"><span data-stu-id="d8d84-2627">ID Number</span></span>
- <span data-ttu-id="d8d84-2628">Identification</span><span class="sxs-lookup"><span data-stu-id="d8d84-2628">Identification</span></span>
- <span data-ttu-id="d8d84-2629">Personnummer</span><span class="sxs-lookup"><span data-stu-id="d8d84-2629">Personnummer</span></span>
- <span data-ttu-id="d8d84-2630">Fødselsnummer</span><span class="sxs-lookup"><span data-stu-id="d8d84-2630">Fødselsnummer</span></span>

   
## <a name="philippines-unified-multi-purpose-id-number"></a><span data-ttu-id="d8d84-2631">Numéro d’identification multifonction unifié Philippines</span><span class="sxs-lookup"><span data-stu-id="d8d84-2631">Philippines Unified Multi-Purpose ID Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-2632">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-2632">Format</span></span>

<span data-ttu-id="d8d84-2633">12 chiffres séparés par des traits d’union</span><span class="sxs-lookup"><span data-stu-id="d8d84-2633">12 digits separated by hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-2634">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2634">Pattern</span></span>

<span data-ttu-id="d8d84-2635">12 chiffres :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2635">12 digits:</span></span>
- <span data-ttu-id="d8d84-2636">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2636">Four digits</span></span> 
- <span data-ttu-id="d8d84-2637">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="d8d84-2637">A hyphen</span></span> 
- <span data-ttu-id="d8d84-2638">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="d8d84-2638">Seven digits</span></span> 
- <span data-ttu-id="d8d84-2639">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="d8d84-2639">A hyphen</span></span> 
- <span data-ttu-id="d8d84-2640">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="d8d84-2640">One digit</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-2641">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2641">Checksum</span></span>

<span data-ttu-id="d8d84-2642">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-2642">No</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-2643">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-2643">Definition</span></span>

<span data-ttu-id="d8d84-2644">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2644">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2645">L’expression régulière Regex_philippines_unified_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2645">The regular expression Regex_philippines_unified_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2646">Un mot clé figurant dans la liste Keyword_philippines_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2646">A keyword from Keyword_philippines_id is found.</span></span>

```
<!-- Philippines Unified Multi-Purpose ID number -->
<Entity id="019b39dd-8c25-4765-91a3-d9c6baf3c3b3" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_philippines_unified_id"/>
     <Match idRef="Keyword_philippines_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8d84-2647">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-2647">Keywords</span></span>
   
#### <a name="keywordphilippinesid"></a><span data-ttu-id="d8d84-2648">Keyword_philippines_id</span><span class="sxs-lookup"><span data-stu-id="d8d84-2648">Keyword_philippines_id</span></span>

- <span data-ttu-id="d8d84-2649">Unified Multi-Purpose ID
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2649">Unified Multi-Purpose ID</span></span> 
- <span data-ttu-id="d8d84-2650">UMID
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2650">UMID</span></span> 
- <span data-ttu-id="d8d84-2651">Identity Card</span><span class="sxs-lookup"><span data-stu-id="d8d84-2651">Identity Card</span></span> 
- <span data-ttu-id="d8d84-2652">Pinag-isang Multi-Layunin ID</span><span class="sxs-lookup"><span data-stu-id="d8d84-2652">Pinag-isang Multi-Layunin ID</span></span>
   
## <a name="poland-identity-card"></a><span data-ttu-id="d8d84-2653">Carte d'identité Pologne</span><span class="sxs-lookup"><span data-stu-id="d8d84-2653">Poland Identity Card</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-2654">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-2654">Format</span></span>

<span data-ttu-id="d8d84-2655">Trois lettres et six chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2655">Three letters and six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-2656">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2656">Pattern</span></span>

<span data-ttu-id="d8d84-2657">Trois lettres (ne respectant pas la casse) suivis de six chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2657">Three letters (not case sensitive) followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-2658">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2658">Checksum</span></span>

<span data-ttu-id="d8d84-2659">Oui</span><span class="sxs-lookup"><span data-stu-id="d8d84-2659">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-2660">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-2660">Definition</span></span>

<span data-ttu-id="d8d84-p138">Une stratégie DLP est convaincu que ce type d’informations sensibles a été détecté à 75 % if, au sein d’une proximité de 300 caractères : la fonction Func_polish_national_id recherche le contenu qui correspond au modèle. Un mot clé à partir de Keyword_polish_national_id_passport_number est trouvé. Passe de la somme de contrôle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-p138">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_polish_national_id finds content that matches the pattern. A keyword from Keyword_polish_national_id_passport_number is found. The checksum passes.</span></span>

```
<!-- Poland Identity Card-->
<Entity id="25E64989-ED5D-40CA-A939-6C14183BB7BF" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_national_id" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8d84-2664">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-2664">Keywords</span></span>

#### <a name="keywordpolishnationalidpassportnumber"></a><span data-ttu-id="d8d84-2665">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="d8d84-2665">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="d8d84-2666">Dowód osobisty</span><span class="sxs-lookup"><span data-stu-id="d8d84-2666">Dowód osobisty</span></span>
- <span data-ttu-id="d8d84-2667">Nombre dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="d8d84-2667">Numer dowodu osobistego</span></span>
- <span data-ttu-id="d8d84-2668">Nazwa i numéro dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="d8d84-2668">Nazwa i numer dowodu osobistego</span></span>
- <span data-ttu-id="d8d84-2669">Nazwa i nr dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="d8d84-2669">Nazwa i nr dowodu osobistego</span></span>
- <span data-ttu-id="d8d84-2670">Nazwa je nr dowodu tożsamości
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2670">Nazwa i nr dowodu tożsamości</span></span>
- <span data-ttu-id="d8d84-2671">Dowód Tożsamości
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2671">Dowód Tożsamości</span></span>
- <span data-ttu-id="d8d84-p139">dow. os.
</span><span class="sxs-lookup"><span data-stu-id="d8d84-p139">dow. os.</span></span>

   
## <a name="poland-national-id-pesel"></a><span data-ttu-id="d8d84-2674">ID national polonais (PESEL)</span><span class="sxs-lookup"><span data-stu-id="d8d84-2674">Poland National ID (PESEL)</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-2675">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-2675">Format</span></span>

<span data-ttu-id="d8d84-2676">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2676">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-2677">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2677">Pattern</span></span>

<span data-ttu-id="d8d84-2678">11 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="d8d84-2678">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-2679">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2679">Checksum</span></span>

<span data-ttu-id="d8d84-2680">Oui</span><span class="sxs-lookup"><span data-stu-id="d8d84-2680">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-2681">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-2681">Definition</span></span>

<span data-ttu-id="d8d84-2682">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2682">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2683">La fonction Func_pesel_identification_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2683">The function Func_pesel_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2684">Un mot clé figurant dans la liste Keyword_pesel_identification_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2684">A keyword from Keyword_pesel_identification_number is found.</span></span>
- <span data-ttu-id="d8d84-2685">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2685">The checksum passes.</span></span>

```
<!-- Poland National ID (PESEL) -->      
<Entity id="E3AAF206-4297-412F-9E06-BA8487E22456" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_pesel_identification_number" />
          <Match idRef="Keyword_pesel_identification_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8d84-2686">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-2686">Keywords</span></span>

#### <a name="keywordpeselidentificationnumber"></a><span data-ttu-id="d8d84-2687">Keyword_pesel_identification_number</span><span class="sxs-lookup"><span data-stu-id="d8d84-2687">Keyword_pesel_identification_number</span></span>

- <span data-ttu-id="d8d84-2688">Nr PESEL</span><span class="sxs-lookup"><span data-stu-id="d8d84-2688">Nr PESEL</span></span>
- <span data-ttu-id="d8d84-2689">PESEL</span><span class="sxs-lookup"><span data-stu-id="d8d84-2689">PESEL</span></span>   

   
## <a name="poland-passport"></a><span data-ttu-id="d8d84-2690">Passeport Pologne</span><span class="sxs-lookup"><span data-stu-id="d8d84-2690">Poland Passport</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-2691">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-2691">Format</span></span>

<span data-ttu-id="d8d84-2692">Deux lettres et sept chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2692">Two letters and seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-2693">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2693">Pattern</span></span>

<span data-ttu-id="d8d84-2694">Deux lettres (ne respectant pas la casse) suivies de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2694">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-2695">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2695">Checksum</span></span>

<span data-ttu-id="d8d84-2696">Oui</span><span class="sxs-lookup"><span data-stu-id="d8d84-2696">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-2697">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-2697">Definition</span></span>

<span data-ttu-id="d8d84-2698">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2698">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2699">La fonction Func_polish_passport_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2699">The function Func_polish_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2700">Un mot clé figurant dans la liste Keyword_polish_national_id_passport_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2700">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
- <span data-ttu-id="d8d84-2701">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2701">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-2702">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-2702">Keywords</span></span>

#### <a name="keywordpolishnationalidpassportnumber"></a><span data-ttu-id="d8d84-2703">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="d8d84-2703">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="d8d84-2704">Numéro paszportu</span><span class="sxs-lookup"><span data-stu-id="d8d84-2704">Numer paszportu</span></span>
- <span data-ttu-id="d8d84-p140">Paszportu nr.</span><span class="sxs-lookup"><span data-stu-id="d8d84-p140">Nr. Paszportu</span></span>
- <span data-ttu-id="d8d84-2707">Paszport</span><span class="sxs-lookup"><span data-stu-id="d8d84-2707">Paszport</span></span>

   
## <a name="portugal-citizen-card-number"></a><span data-ttu-id="d8d84-2708">Numéro de carte de citoyen portugais</span><span class="sxs-lookup"><span data-stu-id="d8d84-2708">Portugal Citizen Card Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-2709">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-2709">Format</span></span>

<span data-ttu-id="d8d84-2710">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2710">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-2711">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2711">Pattern</span></span>

<span data-ttu-id="d8d84-2712">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2712">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-2713">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2713">Checksum</span></span>

<span data-ttu-id="d8d84-2714">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-2714">No</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-2715">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-2715">Definition</span></span>

<span data-ttu-id="d8d84-2716">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2716">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2717">L’expression régulière Regex_portugal_citizen_card trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2717">The regular expression Regex_portugal_citizen_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2718">Un mot clé figurant dans la liste Keyword_portugal_citizen_card est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2718">A keyword from Keyword_portugal_citizen_card is found.</span></span>

```
<!-- Portugal Citizen Card Number -->
<Entity id="91a7ece2-add4-4986-9a15-c84544d81ecd" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_portugal_citizen_card"/>
     <Match idRef="Keyword_portugal_citizen_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8d84-2719">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-2719">Keywords</span></span>

#### <a name="keywordportugalcitizencard"></a><span data-ttu-id="d8d84-2720">Keyword_portugal_citizen_card</span><span class="sxs-lookup"><span data-stu-id="d8d84-2720">Keyword_portugal_citizen_card</span></span>

- <span data-ttu-id="d8d84-2721">Citizen Card</span><span class="sxs-lookup"><span data-stu-id="d8d84-2721">Citizen Card</span></span>
- <span data-ttu-id="d8d84-2722">National ID Card</span><span class="sxs-lookup"><span data-stu-id="d8d84-2722">National ID Card</span></span>
- <span data-ttu-id="d8d84-2723">CC</span><span class="sxs-lookup"><span data-stu-id="d8d84-2723">CC</span></span>
- <span data-ttu-id="d8d84-2724">Cartão de Cidadão</span><span class="sxs-lookup"><span data-stu-id="d8d84-2724">Cartão de Cidadão</span></span>
- <span data-ttu-id="d8d84-2725">Bilhete de Identidade</span><span class="sxs-lookup"><span data-stu-id="d8d84-2725">Bilhete de Identidade</span></span>
   
## <a name="saudi-arabia-national-id"></a><span data-ttu-id="d8d84-2726">ID national Arabie saoudite</span><span class="sxs-lookup"><span data-stu-id="d8d84-2726">Saudi Arabia National ID</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-2727">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-2727">Format</span></span>

<span data-ttu-id="d8d84-2728">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2728">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-2729">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2729">Pattern</span></span>

<span data-ttu-id="d8d84-2730">10 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="d8d84-2730">10 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-2731">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2731">Checksum</span></span>

<span data-ttu-id="d8d84-2732">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-2732">No</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-2733">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-2733">Definition</span></span>

<span data-ttu-id="d8d84-2734">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2734">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2735">L’expression régulière Regex_saudi_arabia_national_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2735">The regular expression Regex_saudi_arabia_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2736">Un mot clé figurant dans la liste Keyword_saudi_arabia_national_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2736">A keyword from Keyword_saudi_arabia_national_id is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-2737">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-2737">Keywords</span></span>

#### <a name="keywordsaudiarabianationalid"></a><span data-ttu-id="d8d84-2738">Keyword_saudi_arabia_national_id</span><span class="sxs-lookup"><span data-stu-id="d8d84-2738">Keyword_saudi_arabia_national_id</span></span>

- <span data-ttu-id="d8d84-2739">Carte d’identification
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2739">Identification Card</span></span> 
- <span data-ttu-id="d8d84-2740">numéro de carte d’identité
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2740">I card number</span></span> 
- <span data-ttu-id="d8d84-2741">numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="d8d84-2741">ID number</span></span> 
- <span data-ttu-id="d8d84-2742">الوطنية الهوية بطاقة رقم
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2742">الوطنية الهوية بطاقة رقم</span></span> 

   
## <a name="singapore-national-registration-identity-card-nric-number"></a><span data-ttu-id="d8d84-2743">Numéro de carte d’identité d’enregistrement national (NRIC) Singapour</span><span class="sxs-lookup"><span data-stu-id="d8d84-2743">Singapore National Registration Identity Card (NRIC) Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-2744">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-2744">Format</span></span>

<span data-ttu-id="d8d84-2745">Neuf lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2745">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-2746">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2746">Pattern</span></span>

- <span data-ttu-id="d8d84-2747">Neuf lettres et chiffres :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2747">Nine letters and digits:</span></span>
- <span data-ttu-id="d8d84-2748">La lettre « F », « G », « S » ou « T » (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="d8d84-2748">The letter "F", "G", "S", or "T" (not case sensitive)</span></span> 
- <span data-ttu-id="d8d84-2749">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="d8d84-2749">Seven digits</span></span> 
- <span data-ttu-id="d8d84-2750">Un chiffre de contrôle alphabétique</span><span class="sxs-lookup"><span data-stu-id="d8d84-2750">An alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-2751">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2751">Checksum</span></span>

<span data-ttu-id="d8d84-2752">Oui</span><span class="sxs-lookup"><span data-stu-id="d8d84-2752">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-2753">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-2753">Definition</span></span>

<span data-ttu-id="d8d84-2754">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2754">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2755">L’expression régulière Regex_singapore_nric trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2755">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2756">Un mot clé figurant dans la liste Keyword_singapore_nric est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2756">A keyword from Keyword_singapore_nric is found.</span></span>
- <span data-ttu-id="d8d84-2757">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2757">The checksum passes.</span></span>

<span data-ttu-id="d8d84-2758">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2758">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2759">L’expression régulière Regex_singapore_nric trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2759">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2760">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2760">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-2761">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-2761">Keywords</span></span>
   
#### <a name="keywordsingaporenric"></a><span data-ttu-id="d8d84-2762">Keyword_singapore_nric</span><span class="sxs-lookup"><span data-stu-id="d8d84-2762">Keyword_singapore_nric</span></span>

- <span data-ttu-id="d8d84-2763">National Registration Identity Card
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2763">National Registration Identity Card</span></span> 
- <span data-ttu-id="d8d84-2764">Identity Card Number
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2764">Identity Card Number</span></span> 
- <span data-ttu-id="d8d84-2765">NRIC
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2765">NRIC</span></span> 
- <span data-ttu-id="d8d84-2766">IC
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2766">IC</span></span> 
- <span data-ttu-id="d8d84-2767">Foreign Identification Number
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2767">Foreign Identification Number</span></span> 
- <span data-ttu-id="d8d84-2768">FIN
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2768">FIN</span></span> 
- <span data-ttu-id="d8d84-2769">身份证 </span><span class="sxs-lookup"><span data-stu-id="d8d84-2769">身份证</span></span> 
- <span data-ttu-id="d8d84-2770">身份證
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2770">身份證</span></span> 
   
## <a name="south-africa-identification-number"></a><span data-ttu-id="d8d84-2771">Numéro d’identification Afrique du Sud</span><span class="sxs-lookup"><span data-stu-id="d8d84-2771">South Africa Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-2772">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-2772">Format</span></span>

<span data-ttu-id="d8d84-2773">13 chiffres pouvant contenir des espaces</span><span class="sxs-lookup"><span data-stu-id="d8d84-2773">13 digits that may contain spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-2774">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2774">Pattern</span></span>

<span data-ttu-id="d8d84-2775">13 chiffres :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2775">13 digits:</span></span>
- <span data-ttu-id="d8d84-2776">Six chiffres au format AAMMJJ correspondant à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="d8d84-2776">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="d8d84-2777">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2777">Four digits</span></span> 
- <span data-ttu-id="d8d84-2778">Un indicateur de citoyenneté à un chiffre </span><span class="sxs-lookup"><span data-stu-id="d8d84-2778">A single-digit citizenship indicator</span></span> 
- <span data-ttu-id="d8d84-2779">Le chiffre « 8 » ou « 9 » </span><span class="sxs-lookup"><span data-stu-id="d8d84-2779">The digit "8" or "9"</span></span> 
- <span data-ttu-id="d8d84-2780">Un chiffre pour la somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2780">One digit which is a checksum digit</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-2781">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2781">Checksum</span></span>

<span data-ttu-id="d8d84-2782">Oui</span><span class="sxs-lookup"><span data-stu-id="d8d84-2782">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-2783">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-2783">Definition</span></span>

<span data-ttu-id="d8d84-2784">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2784">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2785">La fonction Func_south_africa_identification_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2785">The function Func_south_africa_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2786">Un mot clé figurant dans la liste Keyword_south_africa_identification_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2786">A keyword from Keyword_south_africa_identification_number is found.</span></span>
- <span data-ttu-id="d8d84-2787">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2787">The checksum passes.</span></span>

```
<!-- South Africa Identification Number -->
<Entity id="e2adf7cb-8ea6-4048-a2ed-d89eb65f2780" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_south_africa_identification_number"/>
     <Match idRef="Keyword_south_africa_identification_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8d84-2788">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-2788">Keywords</span></span>
   
#### <a name="keywordsouthafricaidentificationnumber"></a><span data-ttu-id="d8d84-2789">Keyword_south_africa_identification_number</span><span class="sxs-lookup"><span data-stu-id="d8d84-2789">Keyword_south_africa_identification_number</span></span>

- <span data-ttu-id="d8d84-2790">Identity card</span><span class="sxs-lookup"><span data-stu-id="d8d84-2790">Identity card</span></span>
- <span data-ttu-id="d8d84-2791">ID</span><span class="sxs-lookup"><span data-stu-id="d8d84-2791">ID</span></span>
- <span data-ttu-id="d8d84-2792">Identification</span><span class="sxs-lookup"><span data-stu-id="d8d84-2792">Identification</span></span> 
   
## <a name="south-korea-resident-registration-number"></a><span data-ttu-id="d8d84-2793">Matricule de résident Corée du Sud</span><span class="sxs-lookup"><span data-stu-id="d8d84-2793">South Korea Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-2794">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-2794">Format</span></span>

<span data-ttu-id="d8d84-2795">13 chiffres contenant un trait d’union</span><span class="sxs-lookup"><span data-stu-id="d8d84-2795">13 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-2796">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2796">Pattern</span></span>

<span data-ttu-id="d8d84-2797">13 chiffres :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2797">13 digits:</span></span>
- <span data-ttu-id="d8d84-2798">Six chiffres au format AAMMJJ correspondant à la date de naissance </span><span class="sxs-lookup"><span data-stu-id="d8d84-2798">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="d8d84-2799">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="d8d84-2799">A hyphen</span></span> 
- <span data-ttu-id="d8d84-2800">Un chiffre déterminé par le siècle et le sexe </span><span class="sxs-lookup"><span data-stu-id="d8d84-2800">One digit determined by the century and gender</span></span> 
- <span data-ttu-id="d8d84-2801">Code à quatre chiffres désignant la région de naissance </span><span class="sxs-lookup"><span data-stu-id="d8d84-2801">Four-digit region-of-birth code</span></span> 
- <span data-ttu-id="d8d84-2802">Un chiffre utilisé pour différencier les personnes dont les chiffres précédents sont identiques. </span><span class="sxs-lookup"><span data-stu-id="d8d84-2802">One digit used to differentiate people for whom the preceding numbers are identical</span></span> 
- <span data-ttu-id="d8d84-2803">Un chiffre de contrôle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2803">A check digit.</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-2804">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2804">Checksum</span></span>

<span data-ttu-id="d8d84-2805">Oui</span><span class="sxs-lookup"><span data-stu-id="d8d84-2805">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-2806">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-2806">Definition</span></span>

<span data-ttu-id="d8d84-2807">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2807">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2808">La fonction Func_south_korea_resident_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2808">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2809">Un mot clé figurant dans la liste Keyword_south_korea_resident_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2809">A keyword from Keyword_south_korea_resident_number is found.</span></span>
- <span data-ttu-id="d8d84-2810">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2810">The checksum passes.</span></span>

<span data-ttu-id="d8d84-2811">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2811">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2812">La fonction Func_south_korea_resident_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2812">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2813">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2813">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-2814">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-2814">Keywords</span></span>
   
#### <a name="keywordsouthkorearesidentnumber"></a><span data-ttu-id="d8d84-2815">Keyword_south_korea_resident_number</span><span class="sxs-lookup"><span data-stu-id="d8d84-2815">Keyword_south_korea_resident_number</span></span>

- <span data-ttu-id="d8d84-2816">National ID card
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2816">National ID card</span></span> 
- <span data-ttu-id="d8d84-2817">Citizen’s Registration Number
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2817">Citizen's Registration Number</span></span> 
- <span data-ttu-id="d8d84-2818">Jumin deungnok beonho
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2818">Jumin deungnok beonho</span></span> 
- <span data-ttu-id="d8d84-2819">RRN
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2819">RRN</span></span> 
- <span data-ttu-id="d8d84-2820">주민등록번호</span><span class="sxs-lookup"><span data-stu-id="d8d84-2820">주민등록번호</span></span>
   
## <a name="spain-social-security-number-ssn"></a><span data-ttu-id="d8d84-2821">Numéro de sécurité sociale Espagne</span><span class="sxs-lookup"><span data-stu-id="d8d84-2821">Spain Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-2822">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-2822">Format</span></span>

<span data-ttu-id="d8d84-2823">11 à 12 chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2823">11-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-2824">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2824">Pattern</span></span>

<span data-ttu-id="d8d84-2825">chiffres de 11-12 :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2825">11-12 digits:</span></span>
- <span data-ttu-id="d8d84-2826">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2826">Two digits</span></span> 
- <span data-ttu-id="d8d84-2827">Une barre oblique (facultative)</span><span class="sxs-lookup"><span data-stu-id="d8d84-2827">A forward slash (optional)</span></span> 
- <span data-ttu-id="d8d84-2828">7 à 8 chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2828">7-8 digits</span></span> 
- <span data-ttu-id="d8d84-2829">Une barre oblique (facultative)</span><span class="sxs-lookup"><span data-stu-id="d8d84-2829">A forward slash (optional)</span></span> 
- <span data-ttu-id="d8d84-2830">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2830">Two digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-2831">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2831">Checksum</span></span>

<span data-ttu-id="d8d84-2832">Oui</span><span class="sxs-lookup"><span data-stu-id="d8d84-2832">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-2833">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-2833">Definition</span></span>

<span data-ttu-id="d8d84-2834">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2834">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2835">La fonction Func_spanish_social_security_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2835">The function Func_spanish_social_security_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2836">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2836">The checksum passes.</span></span>

```
<!-- Spain SSN -->
<Entity id="5df987c0-8eae-4bce-ace7-b316347f3070" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_spanish_social_security_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8d84-2837">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-2837">Keywords</span></span>

<span data-ttu-id="d8d84-2838">Aucune</span><span class="sxs-lookup"><span data-stu-id="d8d84-2838">None</span></span>
   
## <a name="sweden-national-id"></a><span data-ttu-id="d8d84-2839">ID national Suède</span><span class="sxs-lookup"><span data-stu-id="d8d84-2839">Sweden National ID</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-2840">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-2840">Format</span></span>

<span data-ttu-id="d8d84-2841">10 ou 12 chiffres et éventuellement un délimiteur</span><span class="sxs-lookup"><span data-stu-id="d8d84-2841">10 or 12 digits and an optional delimiter</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-2842">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2842">Pattern</span></span>

<span data-ttu-id="d8d84-2843">10 ou 12 chiffres et un délimiteur facultatif :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2843">10 or 12 digits and an optional delimiter:</span></span>
- <span data-ttu-id="d8d84-2844">2 à 4 chiffres (facultatifs)</span><span class="sxs-lookup"><span data-stu-id="d8d84-2844">2-4 digits (optional)</span></span> 
- <span data-ttu-id="d8d84-2845">Six chiffres au format de date AAMMJJ</span><span class="sxs-lookup"><span data-stu-id="d8d84-2845">Six digits in date format YYMMDD</span></span> 
- <span data-ttu-id="d8d84-2846">Séparateur de « - » ou « + » (facultatif), plus</span><span class="sxs-lookup"><span data-stu-id="d8d84-2846">Delimiter of "-" or "+" (optional), plus</span></span>
- <span data-ttu-id="d8d84-2847">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2847">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-2848">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2848">Checksum</span></span>

<span data-ttu-id="d8d84-2849">Oui</span><span class="sxs-lookup"><span data-stu-id="d8d84-2849">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-2850">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-2850">Definition</span></span>

<span data-ttu-id="d8d84-2851">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2851">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2852">La fonction Func_swedish_national_identifier trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2852">The function Func_swedish_national_identifier finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2853">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2853">The checksum passes.</span></span>

```
<!-- Sweden National ID -->
<Entity id="f69aaf40-79be-4fac-8f05-fd1910d272c8" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_swedish_national_identifier" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8d84-2854">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-2854">Keywords</span></span>

<span data-ttu-id="d8d84-2855">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-2855">No</span></span>
   
## <a name="sweden-passport-number"></a><span data-ttu-id="d8d84-2856">Numéro de passeport Suède</span><span class="sxs-lookup"><span data-stu-id="d8d84-2856">Sweden Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-2857">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-2857">Format</span></span>

<span data-ttu-id="d8d84-2858">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2858">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-2859">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2859">Pattern</span></span>

<span data-ttu-id="d8d84-2860">Huit chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="d8d84-2860">Eight consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-2861">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2861">Checksum</span></span>

<span data-ttu-id="d8d84-2862">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-2862">No</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-2863">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-2863">Definition</span></span>

<span data-ttu-id="d8d84-2864">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2864">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2865">L’expression régulière Regex_sweden_passport_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2865">The regular expression Regex_sweden_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2866">L’une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2866">One of the following is true:</span></span>
    - <span data-ttu-id="d8d84-2867">Un mot clé figurant dans la liste Keyword_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2867">A keyword from Keyword_passport is found.</span></span>
    - <span data-ttu-id="d8d84-2868">Un mot clé figurant dans la liste Keyword_sweden_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2868">A keyword from Keyword_sweden_passport is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-2869">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-2869">Keywords</span></span>
   
#### <a name="keywordswedenpassport"></a><span data-ttu-id="d8d84-2870">Keyword_sweden_passport</span><span class="sxs-lookup"><span data-stu-id="d8d84-2870">Keyword_sweden_passport</span></span>

- <span data-ttu-id="d8d84-2871">exigences en matière de visa
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2871">visa requirements</span></span> 
- <span data-ttu-id="d8d84-2872">Carte d’enregistrement d’une personne étrangère
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2872">Alien Registration Card</span></span> 
- <span data-ttu-id="d8d84-2873">Visas Schengen
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2873">Schengen visas</span></span> 
- <span data-ttu-id="d8d84-2874">Visa Schengen
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2874">Schengen visa</span></span> 
- <span data-ttu-id="d8d84-2875">Traitement du visa
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2875">Visa Processing</span></span> 
- <span data-ttu-id="d8d84-2876">Type de visa
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2876">Visa Type</span></span> 
- <span data-ttu-id="d8d84-2877">Entrée unique
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2877">Single Entry</span></span> 
- <span data-ttu-id="d8d84-2878">Entrée multiple
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2878">Multiple Entry</span></span> 
- <span data-ttu-id="d8d84-2879">Frais de traitement G3

</span><span class="sxs-lookup"><span data-stu-id="d8d84-2879">G3 Processing Fees</span></span> 

#### <a name="keywordpassport"></a><span data-ttu-id="d8d84-2880">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="d8d84-2880">Keyword_passport</span></span>

- <span data-ttu-id="d8d84-2881">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8d84-2881">Passport Number</span></span> 
- <span data-ttu-id="d8d84-2882">
N° de passeport</span><span class="sxs-lookup"><span data-stu-id="d8d84-2882">Passport No</span></span> 
- <span data-ttu-id="d8d84-2883"># Passeport
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2883">Passport #</span></span> 
- <span data-ttu-id="d8d84-2884">#Passeport
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2884">Passport#</span></span> 
- <span data-ttu-id="d8d84-2885">IDPassport</span><span class="sxs-lookup"><span data-stu-id="d8d84-2885">PassportID</span></span> 
- <span data-ttu-id="d8d84-2886">n° passeport
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2886">Passportno</span></span> 
- <span data-ttu-id="d8d84-2887">numéropasseport
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2887">passportnumber</span></span> 
- <span data-ttu-id="d8d84-2888">パスポート</span><span class="sxs-lookup"><span data-stu-id="d8d84-2888">パスポート</span></span> 
- <span data-ttu-id="d8d84-2889">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2889">パスポート番号</span></span> 
- <span data-ttu-id="d8d84-2890">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2890">パスポートのNum</span></span> 
- <span data-ttu-id="d8d84-2891">パスポート＃
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2891">パスポート＃</span></span> 
- <span data-ttu-id="d8d84-2892">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8d84-2892">Numéro de passeport</span></span> 
- <span data-ttu-id="d8d84-2893">
Passeport n°</span><span class="sxs-lookup"><span data-stu-id="d8d84-2893">Passeport n °</span></span> 
- <span data-ttu-id="d8d84-2894">Passeport numéro
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2894">Passeport Non</span></span> 
- <span data-ttu-id="d8d84-2895"># Passeport
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2895">Passeport #</span></span> 
- <span data-ttu-id="d8d84-2896">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2896">Passeport#</span></span> 
- <span data-ttu-id="d8d84-2897">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="d8d84-2897">PasseportNon</span></span> 
- <span data-ttu-id="d8d84-2898">Passeportn °
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2898">Passeportn °</span></span> 
   
## <a name="swift-code"></a><span data-ttu-id="d8d84-2899">Code SWIFT</span><span class="sxs-lookup"><span data-stu-id="d8d84-2899">SWIFT Code</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-2900">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-2900">Format</span></span>

<span data-ttu-id="d8d84-2901">Quatre lettres suivies de 5 à 31 lettres ou chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2901">Four letters followed by 5-31 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-2902">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2902">Pattern</span></span>

<span data-ttu-id="d8d84-2903">Quatre lettres suivies de 5 à 31 lettres ou chiffres :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2903">Four letters followed by 5-31 letters or digits:</span></span>
- <span data-ttu-id="d8d84-2904">Code bancaire à quatre lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="d8d84-2904">Four-letter bank code (not case sensitive)</span></span> 
- <span data-ttu-id="d8d84-2905">Un espace facultatif</span><span class="sxs-lookup"><span data-stu-id="d8d84-2905">An optional space</span></span> 
- <span data-ttu-id="d8d84-2906">4 à 28 lettres ou chiffres (numéro de compte bancaire de base (BBAN))</span><span class="sxs-lookup"><span data-stu-id="d8d84-2906">4-28 letters or digits (the Basic Bank Account Number (BBAN))</span></span> 
- <span data-ttu-id="d8d84-2907">Un espace facultatif</span><span class="sxs-lookup"><span data-stu-id="d8d84-2907">An optional space</span></span> 
- <span data-ttu-id="d8d84-2908">1 à 3 lettres ou chiffres (reste du BBAN)</span><span class="sxs-lookup"><span data-stu-id="d8d84-2908">1-3 letters or digits (remainder of the BBAN)</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-2909">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2909">Checksum</span></span>

<span data-ttu-id="d8d84-2910">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-2910">No</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-2911">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-2911">Definition</span></span>

<span data-ttu-id="d8d84-2912">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2912">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2913">L’expression régulière Regex_swift trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2913">The regular expression Regex_swift finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2914">Un mot clé figurant dans la liste Keyword_swift est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2914">A keyword from Keyword_swift is found.</span></span>

```
<Entity id="cb2ab58c-9cb8-4c81-baf8-a4e106791df4" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_swift" />
        <Match idRef="Keyword_swift" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8d84-2915">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-2915">Keywords</span></span>
   
#### <a name="keywordswift"></a><span data-ttu-id="d8d84-2916">Keyword_swift</span><span class="sxs-lookup"><span data-stu-id="d8d84-2916">Keyword_swift</span></span>

- <span data-ttu-id="d8d84-2917">organisation internationale de normalisation 9362
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2917">international organization for standardization 9362</span></span> 
- <span data-ttu-id="d8d84-2918">ISO 9362
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2918">iso 9362</span></span> 
- <span data-ttu-id="d8d84-2919">iso9362</span><span class="sxs-lookup"><span data-stu-id="d8d84-2919">iso9362</span></span> 
- <span data-ttu-id="d8d84-2920">SWIFT\#</span><span class="sxs-lookup"><span data-stu-id="d8d84-2920">swift\#</span></span> 
- <span data-ttu-id="d8d84-2921">codeswift
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2921">swiftcode</span></span> 
- <span data-ttu-id="d8d84-2922">numéroswift
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2922">swiftnumber</span></span> 
- <span data-ttu-id="d8d84-2923">numéroroutageswift
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2923">swiftroutingnumber</span></span> 
- <span data-ttu-id="d8d84-2924">code SWIFT</span><span class="sxs-lookup"><span data-stu-id="d8d84-2924">swift code</span></span> 
- <span data-ttu-id="d8d84-2925"># numéro swift
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2925">swift number #</span></span> 
- <span data-ttu-id="d8d84-2926">numéro d’acheminement swift
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2926">swift routing number</span></span> 
- <span data-ttu-id="d8d84-2927">numéro BIC
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2927">bic number</span></span> 
- <span data-ttu-id="d8d84-2928">code BIC
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2928">bic code</span></span> 
- <span data-ttu-id="d8d84-2929">BIC\#</span><span class="sxs-lookup"><span data-stu-id="d8d84-2929">bic \#</span></span> 
- <span data-ttu-id="d8d84-2930">BIC\#</span><span class="sxs-lookup"><span data-stu-id="d8d84-2930">bic\#</span></span> 
- <span data-ttu-id="d8d84-2931">code d’identification bancaire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2931">bank identifier code</span></span> 
- <span data-ttu-id="d8d84-2932">標準化9362</span><span class="sxs-lookup"><span data-stu-id="d8d84-2932">標準化9362</span></span> 
- <span data-ttu-id="d8d84-2933">迅速＃
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2933">迅速＃</span></span> 
- <span data-ttu-id="d8d84-2934">SWIFTコード
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2934">SWIFTコード</span></span> 
- <span data-ttu-id="d8d84-2935">SWIFT番号
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2935">SWIFT番号</span></span> 
- <span data-ttu-id="d8d84-2936">迅速なルーティング番号
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2936">迅速なルーティング番号</span></span> 
- <span data-ttu-id="d8d84-2937">BIC番号
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2937">BIC番号</span></span> 
- <span data-ttu-id="d8d84-2938">BICコード
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2938">BICコード</span></span> 
- <span data-ttu-id="d8d84-2939">銀行識別コードのための国際組織
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2939">銀行識別コードのための国際組織</span></span> 
- <span data-ttu-id="d8d84-2940">Organisation internationale de normalisation 9362
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2940">Organisation internationale de normalisation 9362</span></span> 
- <span data-ttu-id="d8d84-2941">rapide\#</span><span class="sxs-lookup"><span data-stu-id="d8d84-2941">rapide \#</span></span> 
- <span data-ttu-id="d8d84-2942">code SWIFT
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2942">code SWIFT</span></span> 
- <span data-ttu-id="d8d84-2943">le numéro de swift
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2943">le numéro de swift</span></span> 
- <span data-ttu-id="d8d84-2944">swift numéro d’acheminement
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2944">swift numéro d'acheminement</span></span> 
- <span data-ttu-id="d8d84-2945">le numéro BIC
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2945">le numéro BIC</span></span> 
- <span data-ttu-id="d8d84-2946">\#BIC</span><span class="sxs-lookup"><span data-stu-id="d8d84-2946">\# BIC</span></span> 
- <span data-ttu-id="d8d84-2947">code identificateur de banque
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2947">code identificateur de banque</span></span> 
   
## <a name="taiwan-national-id"></a><span data-ttu-id="d8d84-2948">ID national à Taïwan</span><span class="sxs-lookup"><span data-stu-id="d8d84-2948">Taiwan National ID</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-2949">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-2949">Format</span></span>

<span data-ttu-id="d8d84-2950">Une lettre  suivie de neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2950">One letter (in English) followed by nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-2951">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2951">Pattern</span></span>

<span data-ttu-id="d8d84-2952">Une lettre suivie de neuf chiffres :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2952">One letter (in English) followed by nine digits:</span></span>
- <span data-ttu-id="d8d84-2953">Une lettre (en anglais, ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="d8d84-2953">One letter (in English, not case sensitive)</span></span> 
- <span data-ttu-id="d8d84-2954">Le chiffre « 1 » ou « 2 »</span><span class="sxs-lookup"><span data-stu-id="d8d84-2954">The digit "1" or "2"</span></span> 
- <span data-ttu-id="d8d84-2955">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2955">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-2956">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2956">Checksum</span></span>

<span data-ttu-id="d8d84-2957">Oui</span><span class="sxs-lookup"><span data-stu-id="d8d84-2957">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-2958">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-2958">Definition</span></span>

<span data-ttu-id="d8d84-2959">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2959">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2960">La fonction Func_taiwanese_national_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2960">The function Func_taiwanese_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2961">Un mot clé figurant dans la liste Keyword_taiwanese_national_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2961">A keyword from Keyword_taiwanese_national_id is found.</span></span>
- <span data-ttu-id="d8d84-2962">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2962">The checksum passes.</span></span>

```
<!-- Taiwanese National ID -->
<Entity id="4C7BFC34-8DD1-421D-8FB7-6C6182C2AF03" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_taiwanese_national_id" />
          <Match idRef="Keyword_taiwanese_national_id" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8d84-2963">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-2963">Keywords</span></span>

#### <a name="keywordtaiwanesenationalid"></a><span data-ttu-id="d8d84-2964">Keyword_taiwanese_national_id</span><span class="sxs-lookup"><span data-stu-id="d8d84-2964">Keyword_taiwanese_national_id</span></span>

- <span data-ttu-id="d8d84-2965">身份證字號
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2965">身份證字號</span></span> 
- <span data-ttu-id="d8d84-2966">身份證
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2966">身份證</span></span> 
- <span data-ttu-id="d8d84-2967">身份證號碼
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2967">身份證號碼</span></span> 
- <span data-ttu-id="d8d84-2968">身份證號
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2968">身份證號</span></span> 
- <span data-ttu-id="d8d84-2969">身分證字號
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2969">身分證字號</span></span> 
- <span data-ttu-id="d8d84-2970">身分證 </span><span class="sxs-lookup"><span data-stu-id="d8d84-2970">身分證</span></span> 
- <span data-ttu-id="d8d84-2971">身分證號碼
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2971">身分證號碼</span></span> 
- <span data-ttu-id="d8d84-2972">身份證號
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2972">身份證號</span></span> 
- <span data-ttu-id="d8d84-2973">身分證統一編號
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2973">身分證統一編號</span></span> 
- <span data-ttu-id="d8d84-2974">國民身分證統一編號
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2974">國民身分證統一編號</span></span> 
- <span data-ttu-id="d8d84-2975">簽名
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2975">簽名</span></span> 
- <span data-ttu-id="d8d84-2976">蓋章
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2976">蓋章</span></span> 
- <span data-ttu-id="d8d84-2977">簽名或蓋章

</span><span class="sxs-lookup"><span data-stu-id="d8d84-2977">簽名或蓋章</span></span> 
- <span data-ttu-id="d8d84-2978">簽章</span><span class="sxs-lookup"><span data-stu-id="d8d84-2978">簽章</span></span>   
   
## <a name="taiwan-passport-number"></a><span data-ttu-id="d8d84-2979">Numéro de passeport Taïwan</span><span class="sxs-lookup"><span data-stu-id="d8d84-2979">Taiwan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-2980">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-2980">Format</span></span>

- <span data-ttu-id="d8d84-2981">Numéro de passeport biométrique : neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2981">Biometric passport number: Nine digits</span></span>
- <span data-ttu-id="d8d84-2982">Numéro de passeport non biométrique : neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2982">Non-biometric passport number: Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-2983">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2983">Pattern</span></span>
<span data-ttu-id="d8d84-2984">Numéro de passeport biométrique :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2984">Biometric passport number:</span></span>
- <span data-ttu-id="d8d84-2985">Le chiffre « 3 » </span><span class="sxs-lookup"><span data-stu-id="d8d84-2985">The digit "3"</span></span> 
- <span data-ttu-id="d8d84-2986">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2986">Eight digits</span></span>

<span data-ttu-id="d8d84-2987">Numéro de passeport non biométrique :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2987">Non-biometric passport number:</span></span>
- <span data-ttu-id="d8d84-2988">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-2988">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-2989">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-2989">Checksum</span></span>

<span data-ttu-id="d8d84-2990">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-2990">No</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-2991">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-2991">Definition</span></span>

<span data-ttu-id="d8d84-2992">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-2992">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-2993">L’expression régulière Regex_taiwan_passport trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2993">The regular expression Regex_taiwan_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-2994">Un mot clé figurant dans la liste Keyword_taiwan_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-2994">A keyword from Keyword_taiwan_passport is found.</span></span>

```
<!-- Taiwan Passport Number -->
<Entity id="e7251cb4-4c2c-41df-963e-924eb3dae04a" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_passport"/>
     <Match idRef="Keyword_taiwan_passport"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8d84-2995">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-2995">Keywords</span></span>

#### <a name="keywordtaiwanpassport"></a><span data-ttu-id="d8d84-2996">Keyword_taiwan_passport</span><span class="sxs-lookup"><span data-stu-id="d8d84-2996">Keyword_taiwan_passport</span></span>

- <span data-ttu-id="d8d84-2997">ROC passport number
</span><span class="sxs-lookup"><span data-stu-id="d8d84-2997">ROC passport number</span></span> 
- <span data-ttu-id="d8d84-2998">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8d84-2998">Passport number</span></span> 
- <span data-ttu-id="d8d84-2999">Passeport aucune</span><span class="sxs-lookup"><span data-stu-id="d8d84-2999">Passport no</span></span> 
- <span data-ttu-id="d8d84-3000">Passport Num
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3000">Passport Num</span></span> 
- <span data-ttu-id="d8d84-3001"># Passeport
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3001">Passport #</span></span> 
- <span data-ttu-id="d8d84-3002">护照
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3002">护照</span></span> 
- <span data-ttu-id="d8d84-3003">中華民國護照
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3003">中華民國護照</span></span> 
- <span data-ttu-id="d8d84-3004">Zhōnghuá Mínguó hùzhào</span><span class="sxs-lookup"><span data-stu-id="d8d84-3004">Zhōnghuá Mínguó hùzhào</span></span>
   
## <a name="taiwan-resident-certificate-arctarc-number"></a><span data-ttu-id="d8d84-3005">Numéro de certificat de résident (ARC/TARC) Taïwan</span><span class="sxs-lookup"><span data-stu-id="d8d84-3005">Taiwan Resident Certificate (ARC/TARC) Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-3006">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-3006">Format</span></span>

<span data-ttu-id="d8d84-3007">10 lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-3007">10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-3008">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-3008">Pattern</span></span>

<span data-ttu-id="d8d84-3009">10 lettres et chiffres :</span><span class="sxs-lookup"><span data-stu-id="d8d84-3009">10 letters and digits:</span></span>
- <span data-ttu-id="d8d84-3010">Deux lettres (ne respectant pas la casse) </span><span class="sxs-lookup"><span data-stu-id="d8d84-3010">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="d8d84-3011">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-3011">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-3012">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-3012">Checksum</span></span>

<span data-ttu-id="d8d84-3013">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-3013">No</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-3014">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-3014">Definition</span></span>

<span data-ttu-id="d8d84-3015">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-3015">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-3016">L’expression régulière Regex_taiwan_resident_certificate trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3016">The regular expression Regex_taiwan_resident_certificate finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-3017">Un mot clé figurant dans la liste Keyword_taiwan_resident_certificate est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3017">A keyword from Keyword_taiwan_resident_certificate is found.</span></span>

```
<!-- Taiwan Resident Certificate (ARC/TARC) -->
<Entity id="48269fec-05ea-46ea-b326-f5623a58c6e9" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_resident_certificate"/>
     <Match idRef="Keyword_taiwan_resident_certificate"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8d84-3018">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-3018">Keywords</span></span>

#### <a name="keywordtaiwanresidentcertificate"></a><span data-ttu-id="d8d84-3019">Keyword_taiwan_resident_certificate</span><span class="sxs-lookup"><span data-stu-id="d8d84-3019">Keyword_taiwan_resident_certificate</span></span>

- <span data-ttu-id="d8d84-3020">Resident Certificate
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3020">Resident Certificate</span></span> 
- <span data-ttu-id="d8d84-3021">Cert résident</span><span class="sxs-lookup"><span data-stu-id="d8d84-3021">Resident Cert</span></span> 
- <span data-ttu-id="d8d84-3022">Resident Cert.
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3022">Resident Cert.</span></span> 
- <span data-ttu-id="d8d84-3023">Carte d’identification</span><span class="sxs-lookup"><span data-stu-id="d8d84-3023">Identification card</span></span> 
- <span data-ttu-id="d8d84-3024">Alien Resident Certificate
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3024">Alien Resident Certificate</span></span> 
- <span data-ttu-id="d8d84-3025">ARC
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3025">ARC</span></span> 
- <span data-ttu-id="d8d84-3026">Taiwan Area Resident Certificate
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3026">Taiwan Area Resident Certificate</span></span> 
- <span data-ttu-id="d8d84-3027">TARC
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3027">TARC</span></span> 
- <span data-ttu-id="d8d84-3028">居留證
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3028">居留證</span></span> 
- <span data-ttu-id="d8d84-3029">外僑居留證
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3029">外僑居留證</span></span> 
- <span data-ttu-id="d8d84-3030">台灣地區居留證
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3030">台灣地區居留證</span></span> 

## <a name="thai-population-identification-code"></a><span data-ttu-id="d8d84-3031">Code d’Identification de la Population thaï</span><span class="sxs-lookup"><span data-stu-id="d8d84-3031">Thai Population Identification Code</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-3032">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-3032">Format</span></span>

<span data-ttu-id="d8d84-3033">13 chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-3033">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-3034">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-3034">Pattern</span></span>

<span data-ttu-id="d8d84-3035">13 chiffres :</span><span class="sxs-lookup"><span data-stu-id="d8d84-3035">13 digits:</span></span>
- <span data-ttu-id="d8d84-3036">Premier chiffre n’est pas 0 ou 9</span><span class="sxs-lookup"><span data-stu-id="d8d84-3036">First digit is not 0 or 9</span></span> 
- <span data-ttu-id="d8d84-3037">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-3037">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-3038">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-3038">Checksum</span></span>

<span data-ttu-id="d8d84-3039">Oui</span><span class="sxs-lookup"><span data-stu-id="d8d84-3039">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-3040">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-3040">Definition</span></span>

<span data-ttu-id="d8d84-3041">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-3041">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-3042">La fonction Func_Thai_Citizen_Id recherche le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3042">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-3043">Un mot clé à partir de Keyword_Thai_Citizen_Id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3043">A keyword from Keyword_Thai_Citizen_Id is found.</span></span>

<span data-ttu-id="d8d84-3044">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-3044">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-3045">La fonction Func_Thai_Citizen_Id recherche le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3045">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-3046">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-3046">Keywords</span></span>

#### <a name="keywordthaicitizenid"></a><span data-ttu-id="d8d84-3047">Keyword_Thai_Citizen_Id</span><span class="sxs-lookup"><span data-stu-id="d8d84-3047">Keyword_Thai_Citizen_Id</span></span>

- <span data-ttu-id="d8d84-3048">ID Number</span><span class="sxs-lookup"><span data-stu-id="d8d84-3048">ID Number</span></span>
- <span data-ttu-id="d8d84-3049">Numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="d8d84-3049">Identification Number</span></span>
- <span data-ttu-id="d8d84-3050">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="d8d84-3050">บัตรประชาชน</span></span>
- <span data-ttu-id="d8d84-3051">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="d8d84-3051">รหัสบัตรประชาชน</span></span>
- <span data-ttu-id="d8d84-3052">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="d8d84-3052">บัตรประชาชน</span></span>
- <span data-ttu-id="d8d84-3053">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="d8d84-3053">รหัสบัตรประชาชน</span></span>
  
## <a name="turkish-national-identification-number"></a><span data-ttu-id="d8d84-3054">Numéro d’Identification National turc</span><span class="sxs-lookup"><span data-stu-id="d8d84-3054">Turkish National Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-3055">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-3055">Format</span></span>

<span data-ttu-id="d8d84-3056">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-3056">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-3057">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-3057">Pattern</span></span>

<span data-ttu-id="d8d84-3058">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-3058">11 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-3059">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-3059">Checksum</span></span>

<span data-ttu-id="d8d84-3060">Oui</span><span class="sxs-lookup"><span data-stu-id="d8d84-3060">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-3061">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-3061">Definition</span></span>

<span data-ttu-id="d8d84-3062">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-3062">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-3063">La fonction Func_Turkish_National_Id recherche le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3063">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-3064">Un mot clé à partir de Keyword_Turkish_National_Id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3064">A keyword from Keyword_Turkish_National_Id is found.</span></span>

<span data-ttu-id="d8d84-3065">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-3065">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-3066">La fonction Func_Turkish_National_Id recherche le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3066">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-3067">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-3067">Keywords</span></span>

#### <a name="keywordturkishnationalid"></a><span data-ttu-id="d8d84-3068">Keyword_Turkish_National_Id</span><span class="sxs-lookup"><span data-stu-id="d8d84-3068">Keyword_Turkish_National_Id</span></span>

- <span data-ttu-id="d8d84-3069">TC Kimlik No</span><span class="sxs-lookup"><span data-stu-id="d8d84-3069">TC Kimlik No</span></span>
- <span data-ttu-id="d8d84-3070">TC Kimlik numarası</span><span class="sxs-lookup"><span data-stu-id="d8d84-3070">TC Kimlik numarası</span></span>
- <span data-ttu-id="d8d84-3071">Vatandaşlık numarası</span><span class="sxs-lookup"><span data-stu-id="d8d84-3071">Vatandaşlık numarası</span></span>
- <span data-ttu-id="d8d84-3072">Vatandaşlık aucun</span><span class="sxs-lookup"><span data-stu-id="d8d84-3072">Vatandaşlık no</span></span>

## <a name="uk-drivers-license-number"></a><span data-ttu-id="d8d84-p141">Numéro de permis de conduire Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="d8d84-p141">U.K. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-3075">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-3075">Format</span></span>

<span data-ttu-id="d8d84-3076">Combinaison de 18 lettres et chiffres au format spécifié</span><span class="sxs-lookup"><span data-stu-id="d8d84-3076">Combination of 18 letters and digits in the specified format</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-3077">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-3077">Pattern</span></span>

<span data-ttu-id="d8d84-3078">18 lettres et chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-3078">18 letters and digits:</span></span>
- <span data-ttu-id="d8d84-3079">Cinq lettres (ne respectent pas la casse) ou le chiffre « 9 » à la place d’une lettre</span><span class="sxs-lookup"><span data-stu-id="d8d84-3079">Five letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="d8d84-3080">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="d8d84-3080">One digit</span></span> 
- <span data-ttu-id="d8d84-3081">Cinq chiffres au format de date JJMMA pour la date de naissance</span><span class="sxs-lookup"><span data-stu-id="d8d84-3081">Five digits in the date format DDMMY for date of birth</span></span> 
- <span data-ttu-id="d8d84-3082">Deux lettres (ne respectent pas la casse) ou le chiffre « 9 » à la place d’une lettre</span><span class="sxs-lookup"><span data-stu-id="d8d84-3082">Two letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="d8d84-3083">Cinq chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-3083">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-3084">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-3084">Checksum</span></span>

<span data-ttu-id="d8d84-3085">Oui</span><span class="sxs-lookup"><span data-stu-id="d8d84-3085">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-3086">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-3086">Definition</span></span>

<span data-ttu-id="d8d84-3087">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-3087">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-3088">La fonction Func_uk_drivers_license trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3088">The function Func_uk_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-3089">Un mot clé figurant dans la liste Keyword_uk_drivers_license est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3089">A keyword from Keyword_uk_drivers_license is found.</span></span>
- <span data-ttu-id="d8d84-3090">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3090">The checksum passes.</span></span>

```
<!-- U.K. Driver's License Number -->
<Entity id="f93de4be-d94c-40df-a8be-461738047551" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_uk_drivers_license" />
        <Match idRef="Keyword_uk_drivers_license" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8d84-3091">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-3091">Keywords</span></span>

#### <a name="keywordukdriverslicense"></a><span data-ttu-id="d8d84-3092">Keyword_uk_drivers_license</span><span class="sxs-lookup"><span data-stu-id="d8d84-3092">Keyword_uk_drivers_license</span></span>

- <span data-ttu-id="d8d84-3093">DVLA
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3093">DVLA</span></span> 
- <span data-ttu-id="d8d84-3094">véhicule utilitaire léger
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3094">light vans</span></span> 
- <span data-ttu-id="d8d84-3095">quad
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3095">quadbikes</span></span> 
- <span data-ttu-id="d8d84-3096">automobiles
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3096">motor cars</span></span> 
- <span data-ttu-id="d8d84-3097">125cc</span><span class="sxs-lookup"><span data-stu-id="d8d84-3097">125cc</span></span> 
- <span data-ttu-id="d8d84-3098">sidecar
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3098">sidecar</span></span> 
- <span data-ttu-id="d8d84-3099">tricycles
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3099">tricycles</span></span> 
- <span data-ttu-id="d8d84-3100">motocycles
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3100">motorcycles</span></span> 
- <span data-ttu-id="d8d84-3101">permis de conduire plastifié
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3101">photocard licence</span></span> 
- <span data-ttu-id="d8d84-3102">apprentis conducteurs
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3102">learner drivers</span></span> 
- <span data-ttu-id="d8d84-3103">titulaire du permis
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3103">licence holder</span></span> 
- <span data-ttu-id="d8d84-3104">titulaires du permis
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3104">licence holders</span></span> 
- <span data-ttu-id="d8d84-3105">permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3105">driving licences</span></span> 
- <span data-ttu-id="d8d84-3106">permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3106">driving licence</span></span> 
- <span data-ttu-id="d8d84-3107">voiture à double commande
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3107">dual control car</span></span> 
   
## <a name="uk-electoral-roll-number"></a><span data-ttu-id="d8d84-p142">Numéro de liste électorale Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="d8d84-p142">U.K. Electoral Roll Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-3110">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-3110">Format</span></span>

<span data-ttu-id="d8d84-3111">Deux lettres suivies de 1 à 4 chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-3111">Two letters followed by 1-4 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-3112">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-3112">Pattern</span></span>

<span data-ttu-id="d8d84-3113">Deux lettres (ne respectant pas la casse) suivies de 1 à 4 chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-3113">Two letters (not case sensitive) followed by 1-4 numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-3114">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-3114">Checksum</span></span>

<span data-ttu-id="d8d84-3115">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-3115">No</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-3116">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-3116">Definition</span></span>

<span data-ttu-id="d8d84-3117">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-3117">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-3118">L’expression régulière Regex_uk_electoral trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3118">The regular expression Regex_uk_electoral finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-3119">Un mot clé figurant dans la liste Keyword_uk_electoral est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3119">A keyword from Keyword_uk_electoral is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-3120">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-3120">Keywords</span></span>

#### <a name="keywordukelectoral"></a><span data-ttu-id="d8d84-3121">Keyword_uk_electoral</span><span class="sxs-lookup"><span data-stu-id="d8d84-3121">Keyword_uk_electoral</span></span>

- <span data-ttu-id="d8d84-3122">nomination au conseil
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3122">council nomination</span></span> 
- <span data-ttu-id="d8d84-3123">formulaire de nomination
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3123">nomination form</span></span> 
- <span data-ttu-id="d8d84-3124">registre électoral

</span><span class="sxs-lookup"><span data-stu-id="d8d84-3124">electoral register</span></span> 
- <span data-ttu-id="d8d84-3125">liste électorale</span><span class="sxs-lookup"><span data-stu-id="d8d84-3125">electoral roll</span></span>

   
## <a name="uk-national-health-service-number"></a><span data-ttu-id="d8d84-p143">Numéro national des services de santé Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="d8d84-p143">U.K. National Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-3128">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-3128">Format</span></span>

<span data-ttu-id="d8d84-3129">10 à 17 chiffres séparés par des espaces</span><span class="sxs-lookup"><span data-stu-id="d8d84-3129">10-17 digits separated by spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-3130">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-3130">Pattern</span></span>

<span data-ttu-id="d8d84-3131">10 à 17 chiffres :</span><span class="sxs-lookup"><span data-stu-id="d8d84-3131">10-17 digits:</span></span>
- <span data-ttu-id="d8d84-3132">3 ou 10 chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-3132">Either 3 or 10 digits</span></span> 
- <span data-ttu-id="d8d84-3133">Un espace</span><span class="sxs-lookup"><span data-stu-id="d8d84-3133">A space</span></span> 
- <span data-ttu-id="d8d84-3134">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-3134">Three digits</span></span> 
- <span data-ttu-id="d8d84-3135">Un espace</span><span class="sxs-lookup"><span data-stu-id="d8d84-3135">A space</span></span> 
- <span data-ttu-id="d8d84-3136">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-3136">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-3137">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-3137">Checksum</span></span>

<span data-ttu-id="d8d84-3138">Oui</span><span class="sxs-lookup"><span data-stu-id="d8d84-3138">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-3139">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-3139">Definition</span></span>

<span data-ttu-id="d8d84-3140">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-3140">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-3141">La fonction Func_uk_nhs_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3141">The function Func_uk_nhs_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-3142">L’une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="d8d84-3142">One of the following is true:</span></span>
    - <span data-ttu-id="d8d84-3143">Un mot clé figurant dans la liste Keyword_uk_nhs_number est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3143">A keyword from Keyword_uk_nhs_number is found.</span></span>
    - <span data-ttu-id="d8d84-3144">Un mot clé figurant dans la liste Keyword_uk_nhs_number1 est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3144">A keyword from Keyword_uk_nhs_number1 is found.</span></span>
    - <span data-ttu-id="d8d84-3145">Un mot clé figurant dans la liste Keyword_uk_nhs_number_dob est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3145">A keyword from Keyword_uk_nhs_number_dob is found.</span></span>
- <span data-ttu-id="d8d84-3146">La somme de contrôle est correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3146">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-3147">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-3147">Keywords</span></span>
   
#### <a name="keyworduknhsnumber"></a><span data-ttu-id="d8d84-3148">Keyword_uk_nhs_number</span><span class="sxs-lookup"><span data-stu-id="d8d84-3148">Keyword_uk_nhs_number</span></span>

- <span data-ttu-id="d8d84-3149">service national de santé
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3149">national health service</span></span> 
- <span data-ttu-id="d8d84-3150">NHS
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3150">nhs</span></span> 
- <span data-ttu-id="d8d84-3151">administration des services de santé

</span><span class="sxs-lookup"><span data-stu-id="d8d84-3151">health services authority</span></span> 
- <span data-ttu-id="d8d84-3152">administration de la santé</span><span class="sxs-lookup"><span data-stu-id="d8d84-3152">health authority</span></span>

#### <a name="keyworduknhsnumber1"></a><span data-ttu-id="d8d84-3153">Keyword_uk_nhs_number1</span><span class="sxs-lookup"><span data-stu-id="d8d84-3153">Keyword_uk_nhs_number1</span></span>

- <span data-ttu-id="d8d84-3154">id du patient
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3154">patient id</span></span> 
- <span data-ttu-id="d8d84-3155">identification du patient
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3155">patient identification</span></span> 
- <span data-ttu-id="d8d84-3156">n° patient

</span><span class="sxs-lookup"><span data-stu-id="d8d84-3156">patient no</span></span> 
- <span data-ttu-id="d8d84-3157">numéro de patient</span><span class="sxs-lookup"><span data-stu-id="d8d84-3157">patient number</span></span>

#### <a name="keyworduknhsnumberdob"></a><span data-ttu-id="d8d84-3158">Keyword_uk_nhs_number_dob</span><span class="sxs-lookup"><span data-stu-id="d8d84-3158">Keyword_uk_nhs_number_dob</span></span>

- <span data-ttu-id="d8d84-3159">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="d8d84-3159">GP</span></span> 
- <span data-ttu-id="d8d84-3160">DDN
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3160">DOB</span></span> 
- <span data-ttu-id="d8d84-3161">D.O.B</span><span class="sxs-lookup"><span data-stu-id="d8d84-3161">D.O.B</span></span> 
- <span data-ttu-id="d8d84-3162">Date of Birth
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3162">Date of Birth</span></span> 
- <span data-ttu-id="d8d84-3163">Birth Date
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3163">Birth Date</span></span> 
   
## <a name="uk-national-insurance-number-nino"></a><span data-ttu-id="d8d84-p144">Numéro d'assurance nationale (NINO) Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="d8d84-p144">U.K. National Insurance Number (NINO)</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-3166">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-3166">Format</span></span>

<span data-ttu-id="d8d84-3167">7 caractères ou 9 caractères séparés par des espaces ou des tirets</span><span class="sxs-lookup"><span data-stu-id="d8d84-3167">7 characters or 9 characters separated by spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-3168">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-3168">Pattern</span></span>

<span data-ttu-id="d8d84-3169">Deux modèles possibles :</span><span class="sxs-lookup"><span data-stu-id="d8d84-3169">Two possible patterns:</span></span>

- <span data-ttu-id="d8d84-3170">Deux lettres (valides NINOs utilisent uniquement certains caractères dans ce préfixe, ce modèle est valide ; pas la casse)</span><span class="sxs-lookup"><span data-stu-id="d8d84-3170">Two letters (valid NINOs use only certain characters in this prefix, which this pattern validates; not case sensitive)</span></span>
- <span data-ttu-id="d8d84-3171">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-3171">Six digits</span></span>
- <span data-ttu-id="d8d84-3172">Soit « A », « B », « C », ou a ' (comme le préfixe, seuls certains caractères sont autorisés dans le suffixe ; pas respectant la casse)</span><span class="sxs-lookup"><span data-stu-id="d8d84-3172">Either 'A', 'B', 'C', or 'D' (like the prefix, only certain characters are allowed in the suffix; not case sensitive)</span></span>

<span data-ttu-id="d8d84-3173">OU</span><span class="sxs-lookup"><span data-stu-id="d8d84-3173">OR</span></span>

- <span data-ttu-id="d8d84-3174">Deux lettres</span><span class="sxs-lookup"><span data-stu-id="d8d84-3174">Two letters</span></span>
- <span data-ttu-id="d8d84-3175">Un espace ou un tiret</span><span class="sxs-lookup"><span data-stu-id="d8d84-3175">A space or dash</span></span>
- <span data-ttu-id="d8d84-3176">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-3176">Two digits</span></span>
- <span data-ttu-id="d8d84-3177">Un espace ou un tiret</span><span class="sxs-lookup"><span data-stu-id="d8d84-3177">A space or dash</span></span>
- <span data-ttu-id="d8d84-3178">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-3178">Two digits</span></span>
- <span data-ttu-id="d8d84-3179">Un espace ou un tiret</span><span class="sxs-lookup"><span data-stu-id="d8d84-3179">A space or dash</span></span>
- <span data-ttu-id="d8d84-3180">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-3180">Two digits</span></span>
- <span data-ttu-id="d8d84-3181">Un espace ou un tiret</span><span class="sxs-lookup"><span data-stu-id="d8d84-3181">A space or dash</span></span>
- <span data-ttu-id="d8d84-3182">'A', 'B', « C », ou a '</span><span class="sxs-lookup"><span data-stu-id="d8d84-3182">Either 'A', 'B', 'C', or 'D'</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-3183">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-3183">Checksum</span></span>

<span data-ttu-id="d8d84-3184">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-3184">No</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-3185">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-3185">Definition</span></span>

<span data-ttu-id="d8d84-3186">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-3186">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-3187">La fonction Func_uk_nino trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3187">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-3188">Un mot clé figurant dans la liste Keyword_uk_nino est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3188">A keyword from Keyword_uk_nino is found.</span></span>

<span data-ttu-id="d8d84-3189">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-3189">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-3190">La fonction Func_uk_nino trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3190">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-3191">Aucun mot clé figurant dans la liste Keyword_uk_nino n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3191">No keyword from Keyword_uk_nino is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-3192">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-3192">Keywords</span></span>

#### <a name="keyworduknino"></a><span data-ttu-id="d8d84-3193">Keyword_uk_nino</span><span class="sxs-lookup"><span data-stu-id="d8d84-3193">Keyword_uk_nino</span></span>

- <span data-ttu-id="d8d84-3194">numéro d’assurance nationale
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3194">national insurance number</span></span> 
- <span data-ttu-id="d8d84-3195">cotisations sociales
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3195">national insurance contributions</span></span> 
- <span data-ttu-id="d8d84-3196">loi sur la protection
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3196">protection act</span></span> 
- <span data-ttu-id="d8d84-3197">assurance
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3197">insurance</span></span> 
- <span data-ttu-id="d8d84-3198">numéro de sécurité sociale
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3198">social security number</span></span> 
- <span data-ttu-id="d8d84-3199">demande d’assurance
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3199">insurance application</span></span> 
- <span data-ttu-id="d8d84-3200">demande de soins médicaux
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3200">medical application</span></span> 
- <span data-ttu-id="d8d84-3201">assurance sociale
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3201">social insurance</span></span> 
- <span data-ttu-id="d8d84-3202">soins médicaux
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3202">medical attention</span></span> 
- <span data-ttu-id="d8d84-3203">sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="d8d84-3203">social security</span></span> 
- <span data-ttu-id="d8d84-3204">grande-bretagne
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3204">great britain</span></span> 
- <span data-ttu-id="d8d84-3205">assurance
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3205">insurance</span></span>    
   
## <a name="us--uk-passport-number"></a><span data-ttu-id="d8d84-p145">Numéro de passeport États-Unis/Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="d8d84-p145">U.S. / U.K. Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-3208">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-3208">Format</span></span>

<span data-ttu-id="d8d84-3209">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-3209">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-3210">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-3210">Pattern</span></span>

<span data-ttu-id="d8d84-3211">Neuf chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="d8d84-3211">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-3212">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-3212">Checksum</span></span>

<span data-ttu-id="d8d84-3213">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-3213">No</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-3214">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-3214">Definition</span></span>

<span data-ttu-id="d8d84-3215">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-3215">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-3216">La fonction Func_usa_uk_passport trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3216">The function Func_usa_uk_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-3217">Un mot clé figurant dans la liste Keyword_passport est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3217">A keyword from Keyword_passport is found.</span></span>

```
<Entity id="178ec42a-18b4-47cc-85c7-d62c92fd67f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_usa_uk_passport" />
        <Match idRef="Keyword_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8d84-3218">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-3218">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="d8d84-3219">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="d8d84-3219">Keyword_passport</span></span>

- <span data-ttu-id="d8d84-3220">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8d84-3220">Passport Number</span></span> 
- <span data-ttu-id="d8d84-3221">
N° de passeport</span><span class="sxs-lookup"><span data-stu-id="d8d84-3221">Passport No</span></span> 
- <span data-ttu-id="d8d84-3222"># Passeport
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3222">Passport #</span></span> 
- <span data-ttu-id="d8d84-3223">#Passeport
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3223">Passport#</span></span> 
- <span data-ttu-id="d8d84-3224">IDPassport</span><span class="sxs-lookup"><span data-stu-id="d8d84-3224">PassportID</span></span> 
- <span data-ttu-id="d8d84-3225">n° passeport
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3225">Passportno</span></span> 
- <span data-ttu-id="d8d84-3226">numéropasseport
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3226">passportnumber</span></span> 
- <span data-ttu-id="d8d84-3227">パスポート</span><span class="sxs-lookup"><span data-stu-id="d8d84-3227">パスポート</span></span> 
- <span data-ttu-id="d8d84-3228">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3228">パスポート番号</span></span> 
- <span data-ttu-id="d8d84-3229">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3229">パスポートのNum</span></span> 
- <span data-ttu-id="d8d84-3230">パスポート＃
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3230">パスポート＃</span></span> 
- <span data-ttu-id="d8d84-3231">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d8d84-3231">Numéro de passeport</span></span> 
- <span data-ttu-id="d8d84-3232">
Passeport n°</span><span class="sxs-lookup"><span data-stu-id="d8d84-3232">Passeport n °</span></span> 
- <span data-ttu-id="d8d84-3233">Passeport numéro
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3233">Passeport Non</span></span> 
- <span data-ttu-id="d8d84-3234"># Passeport
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3234">Passeport #</span></span> 
- <span data-ttu-id="d8d84-3235">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3235">Passeport#</span></span> 
- <span data-ttu-id="d8d84-3236">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="d8d84-3236">PasseportNon</span></span> 
- <span data-ttu-id="d8d84-3237">Passeportn °
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3237">Passeportn °</span></span> 
   
## <a name="us-bank-account-number"></a><span data-ttu-id="d8d84-3238">Numéro de compte bancaire États-Unis</span><span class="sxs-lookup"><span data-stu-id="d8d84-3238">U.S. Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-3239">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-3239">Format</span></span>

<span data-ttu-id="d8d84-3240">8-17 chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-3240">8-17 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-3241">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-3241">Pattern</span></span>

<span data-ttu-id="d8d84-3242">8 à 17 chiffres consécutifs</span><span class="sxs-lookup"><span data-stu-id="d8d84-3242">8-17 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-3243">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-3243">Checksum</span></span>

<span data-ttu-id="d8d84-3244">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-3244">No</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-3245">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-3245">Definition</span></span>

<span data-ttu-id="d8d84-3246">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-3246">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-3247">L’expression régulière Regex_usa_bank_account_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3247">The regular expression Regex_usa_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-3248">Un mot clé figurant dans la liste Keyword_usa_Bank_Account est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3248">A keyword from Keyword_usa_Bank_Account is found.</span></span>

```
<!-- U.S. Bank Account Number -->
<Entity id="a2ce32a8-f935-4bb6-8e96-2a5157672e2c" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_usa_bank_account_number" />
        <Match idRef="Keyword_usa_Bank_Account" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d8d84-3249">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-3249">Keywords</span></span>

#### <a name="keywordusabankaccount"></a><span data-ttu-id="d8d84-3250">Keyword_usa_Bank_Account</span><span class="sxs-lookup"><span data-stu-id="d8d84-3250">Keyword_usa_Bank_Account</span></span>

- <span data-ttu-id="d8d84-3251">Numéro de compte courant
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3251">Checking Account Number</span></span> 
- <span data-ttu-id="d8d84-3252">Compte courant
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3252">Checking Account</span></span> 
- <span data-ttu-id="d8d84-3253"># compte courant
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3253">Checking Account #</span></span> 
- <span data-ttu-id="d8d84-3254">Numéro compte courant
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3254">Checking Acct Number</span></span> 
- <span data-ttu-id="d8d84-3255"># compte courant
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3255">Checking Acct #</span></span> 
- <span data-ttu-id="d8d84-3256">N° de compte courant
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3256">Checking Acct No.</span></span> 
- <span data-ttu-id="d8d84-3257">N° de compte courant
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3257">Checking Account No.</span></span> 
- <span data-ttu-id="d8d84-3258">Numéro de compte bancaire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3258">Bank Account Number</span></span> 
- <span data-ttu-id="d8d84-3259"># Compte bancaire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3259">Bank Account #</span></span> 
- <span data-ttu-id="d8d84-3260">Numéro de compte bancaire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3260">Bank Acct Number</span></span> 
- <span data-ttu-id="d8d84-3261"># Compte bancaire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3261">Bank Acct #</span></span> 
- <span data-ttu-id="d8d84-3262">N° de compte bancaire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3262">Bank Acct No.</span></span> 
- <span data-ttu-id="d8d84-3263">N° de compte bancaire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3263">Bank Account No.</span></span> 
- <span data-ttu-id="d8d84-3264">Numéro de compte d’épargne
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3264">Savings Account Number</span></span> 
- <span data-ttu-id="d8d84-3265">Compte d’épargne.
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3265">Savings Account.</span></span> 
- <span data-ttu-id="d8d84-3266">N° de compte d’épargne
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3266">Savings Account #</span></span> 
- <span data-ttu-id="d8d84-3267">Numéro de compte d’épargne
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3267">Savings Acct Number</span></span> 
- <span data-ttu-id="d8d84-3268"># compte d’épargne
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3268">Savings Acct #</span></span> 
- <span data-ttu-id="d8d84-3269">N° de compte d’épargne
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3269">Savings Acct No.</span></span> 
- <span data-ttu-id="d8d84-3270">N° de compte d’épargne
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3270">Savings Account No.</span></span> 
- <span data-ttu-id="d8d84-3271">Numéro de compte de débit
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3271">Debit Account Number</span></span> 
- <span data-ttu-id="d8d84-3272">Compte de débit
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3272">Debit Account</span></span> 
- <span data-ttu-id="d8d84-3273"># Compte de débit
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3273">Debit Account #</span></span> 
- <span data-ttu-id="d8d84-3274">Numéro de compte de débit
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3274">Debit Acct Number</span></span> 
- <span data-ttu-id="d8d84-3275"># Compte de débit
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3275">Debit Acct #</span></span> 
- <span data-ttu-id="d8d84-3276">N° de compte de débit
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3276">Debit Acct No.</span></span> 
- <span data-ttu-id="d8d84-3277">N° de compte de débit
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3277">Debit Account No.</span></span> 
   
## <a name="us-drivers-license-number"></a><span data-ttu-id="d8d84-3278">Numéro de permis de conduire États-Unis</span><span class="sxs-lookup"><span data-stu-id="d8d84-3278">U.S. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-3279">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-3279">Format</span></span>

<span data-ttu-id="d8d84-3280">Dépend de l’État</span><span class="sxs-lookup"><span data-stu-id="d8d84-3280">Depends on the state</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-3281">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-3281">Pattern</span></span>

<span data-ttu-id="d8d84-3282">Dépend de l’État, par exemple, New York :</span><span class="sxs-lookup"><span data-stu-id="d8d84-3282">Depends on the state -- for example, New York:</span></span>
- <span data-ttu-id="d8d84-3283">Neuf chiffres au format ddd ddd ddd correspondront.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3283">Nine digits formatted like ddd ddd ddd will match.</span></span>
- <span data-ttu-id="d8d84-3284">Neuf chiffres au format ddddddddd ne correspondront pas.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3284">Nine digits like ddddddddd will not match.</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-3285">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-3285">Checksum</span></span>

<span data-ttu-id="d8d84-3286">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-3286">No</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-3287">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-3287">Definition</span></span>

<span data-ttu-id="d8d84-3288">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-3288">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-3289">La fonction Func_new_york_drivers_license_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3289">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-3290">Un mot clé figurant dans la liste Keyword_[state_name]_drivers_license_name est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3290">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="d8d84-3291">Un mot clé figurant dans la liste Keyword_us_drivers_license est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3291">A keyword from Keyword_us_drivers_license is found.</span></span>

<span data-ttu-id="d8d84-3292">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-3292">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-3293">La fonction Func_new_york_drivers_license_number trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3293">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-3294">Un mot clé figurant dans la liste Keyword_[state_name]_drivers_license_name est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3294">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="d8d84-3295">Un mot clé figurant dans la liste Keyword_us_drivers_license_abbreviations est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3295">A keyword from Keyword_us_drivers_license_abbreviations is found.</span></span>
- <span data-ttu-id="d8d84-3296">Aucun mot clé figurant dans la liste Keyword_us_drivers_license n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3296">No keyword from Keyword_us_drivers_license is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-3297">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-3297">Keywords</span></span>

#### <a name="keywordusdriverslicenseabbreviations"></a><span data-ttu-id="d8d84-3298">Keyword_us_drivers_license_abbreviations</span><span class="sxs-lookup"><span data-stu-id="d8d84-3298">Keyword_us_drivers_license_abbreviations</span></span>

- <span data-ttu-id="d8d84-3299">PC</span><span class="sxs-lookup"><span data-stu-id="d8d84-3299">DL</span></span> 
- <span data-ttu-id="d8d84-3300">PC</span><span class="sxs-lookup"><span data-stu-id="d8d84-3300">DLS</span></span> 
- <span data-ttu-id="d8d84-3301">CDL</span><span class="sxs-lookup"><span data-stu-id="d8d84-3301">CDL</span></span> 
- <span data-ttu-id="d8d84-3302">SYSTÈMES CDL</span><span class="sxs-lookup"><span data-stu-id="d8d84-3302">CDLS</span></span> 
- <span data-ttu-id="d8d84-3303">ID</span><span class="sxs-lookup"><span data-stu-id="d8d84-3303">ID</span></span> 
- <span data-ttu-id="d8d84-3304">ID</span><span class="sxs-lookup"><span data-stu-id="d8d84-3304">IDs</span></span> 
- <span data-ttu-id="d8d84-3305"># PC</span><span class="sxs-lookup"><span data-stu-id="d8d84-3305">DL#</span></span> 
- <span data-ttu-id="d8d84-3306">
# PC
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3306">DLS#</span></span> 
- <span data-ttu-id="d8d84-3307"># PCD
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3307">CDL#</span></span> 
- <span data-ttu-id="d8d84-3308"># PCD
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3308">CDLS#</span></span> 
- <span data-ttu-id="d8d84-3309">#ID</span><span class="sxs-lookup"><span data-stu-id="d8d84-3309">ID#</span></span>
- <span data-ttu-id="d8d84-3310">
#IDs
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3310">IDs#</span></span> 
- <span data-ttu-id="d8d84-3311">numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="d8d84-3311">ID number</span></span> 
- <span data-ttu-id="d8d84-3312">Numéros d’identification
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3312">ID numbers</span></span> 
- <span data-ttu-id="d8d84-3313">LIC</span><span class="sxs-lookup"><span data-stu-id="d8d84-3313">LIC</span></span> 
- <span data-ttu-id="d8d84-3314"># PERMIS
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3314">LIC#</span></span> 

#### <a name="keywordusdriverslicense"></a><span data-ttu-id="d8d84-3315">Keyword_us_drivers_license</span><span class="sxs-lookup"><span data-stu-id="d8d84-3315">Keyword_us_drivers_license</span></span>

- <span data-ttu-id="d8d84-3316">DriverLic</span><span class="sxs-lookup"><span data-stu-id="d8d84-3316">DriverLic</span></span> 
- <span data-ttu-id="d8d84-3317">DriverLics</span><span class="sxs-lookup"><span data-stu-id="d8d84-3317">DriverLics</span></span> 
- <span data-ttu-id="d8d84-3318">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="d8d84-3318">DriverLicense</span></span> 
- <span data-ttu-id="d8d84-3319">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="d8d84-3319">DriverLicenses</span></span> 
- <span data-ttu-id="d8d84-3320">Lic pilote</span><span class="sxs-lookup"><span data-stu-id="d8d84-3320">Driver Lic</span></span> 
- <span data-ttu-id="d8d84-3321">Pilote Lics</span><span class="sxs-lookup"><span data-stu-id="d8d84-3321">Driver Lics</span></span> 
- <span data-ttu-id="d8d84-3322">Conduire</span><span class="sxs-lookup"><span data-stu-id="d8d84-3322">Driver License</span></span> 
- <span data-ttu-id="d8d84-3323">Licences de pilote</span><span class="sxs-lookup"><span data-stu-id="d8d84-3323">Driver Licenses</span></span> 
- <span data-ttu-id="d8d84-3324">DriversLic</span><span class="sxs-lookup"><span data-stu-id="d8d84-3324">DriversLic</span></span> 
- <span data-ttu-id="d8d84-3325">DriversLics</span><span class="sxs-lookup"><span data-stu-id="d8d84-3325">DriversLics</span></span> 
- <span data-ttu-id="d8d84-3326">Conduire</span><span class="sxs-lookup"><span data-stu-id="d8d84-3326">DriversLicense</span></span> 
- <span data-ttu-id="d8d84-3327">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="d8d84-3327">DriversLicenses</span></span> 
- <span data-ttu-id="d8d84-3328">Lic pilotes</span><span class="sxs-lookup"><span data-stu-id="d8d84-3328">Drivers Lic</span></span> 
- <span data-ttu-id="d8d84-3329">Lics pilotes</span><span class="sxs-lookup"><span data-stu-id="d8d84-3329">Drivers Lics</span></span> 
- <span data-ttu-id="d8d84-3330">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="d8d84-3330">Drivers License</span></span> 
- <span data-ttu-id="d8d84-3331">Licences de pilotes</span><span class="sxs-lookup"><span data-stu-id="d8d84-3331">Drivers Licenses</span></span> 
- <span data-ttu-id="d8d84-3332">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="d8d84-3332">Driver'Lic</span></span> 
- <span data-ttu-id="d8d84-3333">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="d8d84-3333">Driver'Lics</span></span> 
- <span data-ttu-id="d8d84-3334">Driver'License</span><span class="sxs-lookup"><span data-stu-id="d8d84-3334">Driver'License</span></span> 
- <span data-ttu-id="d8d84-3335">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="d8d84-3335">Driver'Licenses</span></span> 
- <span data-ttu-id="d8d84-3336">Pilote ' Lic</span><span class="sxs-lookup"><span data-stu-id="d8d84-3336">Driver' Lic</span></span> 
- <span data-ttu-id="d8d84-3337">Pilote ' Lics</span><span class="sxs-lookup"><span data-stu-id="d8d84-3337">Driver' Lics</span></span> 
- <span data-ttu-id="d8d84-3338">Pilote ' licence</span><span class="sxs-lookup"><span data-stu-id="d8d84-3338">Driver' License</span></span> 
- <span data-ttu-id="d8d84-3339">Pilote ' licences</span><span class="sxs-lookup"><span data-stu-id="d8d84-3339">Driver' Licenses</span></span>
- <span data-ttu-id="d8d84-3340">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="d8d84-3340">Driver'sLic</span></span> 
- <span data-ttu-id="d8d84-3341">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="d8d84-3341">Driver'sLics</span></span> 
- <span data-ttu-id="d8d84-3342">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="d8d84-3342">Driver'sLicense</span></span> 
- <span data-ttu-id="d8d84-3343">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="d8d84-3343">Driver'sLicenses</span></span> 
- <span data-ttu-id="d8d84-3344">Lic du pilote</span><span class="sxs-lookup"><span data-stu-id="d8d84-3344">Driver's Lic</span></span> 
- <span data-ttu-id="d8d84-3345">Lics permis de conduire</span><span class="sxs-lookup"><span data-stu-id="d8d84-3345">Driver's Lics</span></span> 
- <span data-ttu-id="d8d84-3346">Conduire permis de</span><span class="sxs-lookup"><span data-stu-id="d8d84-3346">Driver's License</span></span> 
- <span data-ttu-id="d8d84-3347">Conduire permis de</span><span class="sxs-lookup"><span data-stu-id="d8d84-3347">Driver's Licenses</span></span> 
- <span data-ttu-id="d8d84-3348">numéro d’identification
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3348">identification number</span></span> 
- <span data-ttu-id="d8d84-3349">numéros d’identification
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3349">identification numbers</span></span> 
- <span data-ttu-id="d8d84-3350"># identification
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3350">identification #</span></span> 
- <span data-ttu-id="d8d84-3351">carte d’identité</span><span class="sxs-lookup"><span data-stu-id="d8d84-3351">id card</span></span> 
- <span data-ttu-id="d8d84-3352">ID de cartes de visite</span><span class="sxs-lookup"><span data-stu-id="d8d84-3352">id cards</span></span> 
- <span data-ttu-id="d8d84-3353">carte d’identification</span><span class="sxs-lookup"><span data-stu-id="d8d84-3353">identification card</span></span> 
- <span data-ttu-id="d8d84-3354">cartes d’identification</span><span class="sxs-lookup"><span data-stu-id="d8d84-3354">identification cards</span></span> 
- <span data-ttu-id="d8d84-3355">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="d8d84-3355">DriverLic#</span></span> 
- <span data-ttu-id="d8d84-3356">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="d8d84-3356">DriverLics#</span></span> 
- <span data-ttu-id="d8d84-3357">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="d8d84-3357">DriverLicense#</span></span> 
- <span data-ttu-id="d8d84-3358">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="d8d84-3358">DriverLicenses#</span></span> 
- <span data-ttu-id="d8d84-3359">#Permis conduire</span><span class="sxs-lookup"><span data-stu-id="d8d84-3359">Driver Lic#</span></span> 
- <span data-ttu-id="d8d84-3360">
#Permis conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3360">Driver Lics#</span></span> 
- <span data-ttu-id="d8d84-3361">Pilote licence #</span><span class="sxs-lookup"><span data-stu-id="d8d84-3361">Driver License#</span></span> 
- <span data-ttu-id="d8d84-3362">Licences de pilote #</span><span class="sxs-lookup"><span data-stu-id="d8d84-3362">Driver Licenses#</span></span> 
- <span data-ttu-id="d8d84-3363">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="d8d84-3363">DriversLic#</span></span> 
- <span data-ttu-id="d8d84-3364">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="d8d84-3364">DriversLics#</span></span> 
- <span data-ttu-id="d8d84-3365">Conduire #</span><span class="sxs-lookup"><span data-stu-id="d8d84-3365">DriversLicense#</span></span> 
- <span data-ttu-id="d8d84-3366">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="d8d84-3366">DriversLicenses#</span></span> 
- <span data-ttu-id="d8d84-3367">Pilotes Lic #</span><span class="sxs-lookup"><span data-stu-id="d8d84-3367">Drivers Lic#</span></span> 
- <span data-ttu-id="d8d84-3368">Pilotes Lics #</span><span class="sxs-lookup"><span data-stu-id="d8d84-3368">Drivers Lics#</span></span> 
- <span data-ttu-id="d8d84-3369">Licence pilotes #</span><span class="sxs-lookup"><span data-stu-id="d8d84-3369">Drivers License#</span></span> 
- <span data-ttu-id="d8d84-3370">Licences pilotes #</span><span class="sxs-lookup"><span data-stu-id="d8d84-3370">Drivers Licenses#</span></span> 
- <span data-ttu-id="d8d84-3371">#Permisconduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3371">Driver'Lic#</span></span> 
- <span data-ttu-id="d8d84-3372">#Permisconduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3372">Driver'Lics#</span></span> 
- <span data-ttu-id="d8d84-3373">#Permisdeconduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3373">Driver'License#</span></span> 
- <span data-ttu-id="d8d84-3374">#Permisdeconduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3374">Driver'Licenses#</span></span> 
- <span data-ttu-id="d8d84-3375">#Permis conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3375">Driver' Lic#</span></span> 
- <span data-ttu-id="d8d84-3376">#Permis conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3376">Driver' Lics#</span></span> 
- <span data-ttu-id="d8d84-3377">#Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3377">Driver' License#</span></span> 
- <span data-ttu-id="d8d84-3378">#Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3378">Driver' Licenses#</span></span> 
- <span data-ttu-id="d8d84-3379">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="d8d84-3379">Driver'sLic#</span></span> 
- <span data-ttu-id="d8d84-3380">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="d8d84-3380">Driver'sLics#</span></span> 
- <span data-ttu-id="d8d84-3381">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="d8d84-3381">Driver'sLicense#</span></span> 
- <span data-ttu-id="d8d84-3382">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="d8d84-3382">Driver'sLicenses#</span></span> 
- <span data-ttu-id="d8d84-3383">#Permisconduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3383">Driver's Lic#</span></span> 
- <span data-ttu-id="d8d84-3384">#Permisconduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3384">Driver's Lics#</span></span> 
- <span data-ttu-id="d8d84-3385">#Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3385">Driver's License#</span></span> 
- <span data-ttu-id="d8d84-3386">#Permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3386">Driver's Licenses#</span></span> 
- <span data-ttu-id="d8d84-3387">carte d’identité #</span><span class="sxs-lookup"><span data-stu-id="d8d84-3387">id card#</span></span> 
- <span data-ttu-id="d8d84-3388"># cartes d’identité
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3388">id cards#</span></span> 
- <span data-ttu-id="d8d84-3389">#carte d’identification
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3389">identification card#</span></span> 
- <span data-ttu-id="d8d84-3390">#cartes d’identification
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3390">identification cards#</span></span> 


#### <a name="keywordstatenamedriverslicensename"></a><span data-ttu-id="d8d84-3391">Keyword_[state_name]_drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="d8d84-3391">Keyword_[state_name]_drivers_license_name</span></span>

- <span data-ttu-id="d8d84-3392">Abréviation de l’État (par exemple, « NY »)
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3392">State abbreviation (for example, "NY")</span></span> 
- <span data-ttu-id="d8d84-3393">Nom de l’État (par exemple, « New York »)
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3393">State name (for example, "New York")</span></span>    
   
## <a name="us-individual-taxpayer-identification-number-itin"></a><span data-ttu-id="d8d84-3394">Numéro d'identification fiscale individuel (ITIN) États-Unis</span><span class="sxs-lookup"><span data-stu-id="d8d84-3394">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-3395">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-3395">Format</span></span>

<span data-ttu-id="d8d84-3396">Neuf chiffres, le premier étant le « 9 », le quatrième le « 7 » ou le « 8 », éventuellement mis en forme avec des espaces ou des tirets</span><span class="sxs-lookup"><span data-stu-id="d8d84-3396">Nine digits that start with a "9" and contain a "7" or "8" as the fourth digit, optionally formatted with spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-3397">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-3397">Pattern</span></span>

<span data-ttu-id="d8d84-3398">Mis en forme :</span><span class="sxs-lookup"><span data-stu-id="d8d84-3398">Formatted:</span></span>
- <span data-ttu-id="d8d84-3399">Le chiffre « 9 »</span><span class="sxs-lookup"><span data-stu-id="d8d84-3399">The digit "9"</span></span> 
- <span data-ttu-id="d8d84-3400">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-3400">Two digits</span></span> 
- <span data-ttu-id="d8d84-3401">Un espace ou un tiret</span><span class="sxs-lookup"><span data-stu-id="d8d84-3401">A space or dash</span></span> 
- <span data-ttu-id="d8d84-3402">Un « 7 » ou un « 8 »</span><span class="sxs-lookup"><span data-stu-id="d8d84-3402">A "7" or "8"</span></span> 
- <span data-ttu-id="d8d84-3403">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="d8d84-3403">A digit</span></span> 
- <span data-ttu-id="d8d84-3404">Un espace ou tiret</span><span class="sxs-lookup"><span data-stu-id="d8d84-3404">A space, or dash</span></span> 
- <span data-ttu-id="d8d84-3405">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-3405">Four digits</span></span>

<span data-ttu-id="d8d84-3406">Non mis en forme :</span><span class="sxs-lookup"><span data-stu-id="d8d84-3406">Unformatted:</span></span>
- <span data-ttu-id="d8d84-3407">Le chiffre « 9 »</span><span class="sxs-lookup"><span data-stu-id="d8d84-3407">The digit "9"</span></span> 
- <span data-ttu-id="d8d84-3408">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-3408">Two digits</span></span> 
- <span data-ttu-id="d8d84-3409">Un « 7 » ou un « 8 »</span><span class="sxs-lookup"><span data-stu-id="d8d84-3409">A "7" or "8"</span></span> 
- <span data-ttu-id="d8d84-3410">Cinq chiffres</span><span class="sxs-lookup"><span data-stu-id="d8d84-3410">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-3411">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-3411">Checksum</span></span>

<span data-ttu-id="d8d84-3412">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-3412">No</span></span>

### <a name="definition"></a><span data-ttu-id="d8d84-3413">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-3413">Definition</span></span>

<span data-ttu-id="d8d84-3414">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-3414">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-3415">La fonction Func_formatted_itin trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3415">The function Func_formatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-3416">Au moins une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="d8d84-3416">At least one of the following is true:</span></span>
    - <span data-ttu-id="d8d84-3417">Un mot clé figurant dans la liste Keyword_itin est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3417">A keyword from Keyword_itin is found.</span></span>
    - <span data-ttu-id="d8d84-3418">La fonction Func_us_address trouve une adresse au format correct.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3418">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="d8d84-3419">La fonction Func_us_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3419">The function Func_us_date finds a date in the right date format.</span></span>
    - <span data-ttu-id="d8d84-3420">Un mot clé figurant dans la liste Keyword_itin_collaborative est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3420">A keyword from Keyword_itin_collaborative is found.</span></span>

<span data-ttu-id="d8d84-3421">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-3421">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-3422">La fonction Func_unformatted_itin trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3422">The function Func_unformatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-3423">Au moins une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="d8d84-3423">At least one of the following is true:</span></span>
    - <span data-ttu-id="d8d84-3424">Un mot clé figurant dans la liste Keyword_itin_collaborative est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3424">A keyword from Keyword_itin_collaborative is found.</span></span>
    - <span data-ttu-id="d8d84-3425">La fonction Func_us_address trouve une adresse au format correct.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3425">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="d8d84-3426">La fonction Func_us_date trouve une date au format correct.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3426">The function Func_us_date finds a date in the right date format.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-3427">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-3427">Keywords</span></span>

#### <a name="keyworditin"></a><span data-ttu-id="d8d84-3428">Keyword_itin</span><span class="sxs-lookup"><span data-stu-id="d8d84-3428">Keyword_itin</span></span>

- <span data-ttu-id="d8d84-3429">contribuable
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3429">taxpayer</span></span> 
- <span data-ttu-id="d8d84-3430">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3430">tax id</span></span> 
- <span data-ttu-id="d8d84-3431">identification fiscale
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3431">tax identification</span></span> 
- <span data-ttu-id="d8d84-3432">itin
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3432">itin</span></span> 
- <span data-ttu-id="d8d84-3433">ssn</span><span class="sxs-lookup"><span data-stu-id="d8d84-3433">ssn</span></span> 
- <span data-ttu-id="d8d84-3434">tin
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3434">tin</span></span> 
- <span data-ttu-id="d8d84-3435">sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="d8d84-3435">social security</span></span> 
- <span data-ttu-id="d8d84-3436">contribuable
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3436">tax payer</span></span> 
- <span data-ttu-id="d8d84-3437">itins
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3437">itins</span></span> 
- <span data-ttu-id="d8d84-3438">id fiscal

</span><span class="sxs-lookup"><span data-stu-id="d8d84-3438">taxid</span></span> 
- <span data-ttu-id="d8d84-3439">contribuable individuel
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3439">individual taxpayer</span></span> 

#### <a name="keyworditincollaborative"></a><span data-ttu-id="d8d84-3440">Keyword_itin_collaborative</span><span class="sxs-lookup"><span data-stu-id="d8d84-3440">Keyword_itin_collaborative</span></span>

- <span data-ttu-id="d8d84-3441">License</span><span class="sxs-lookup"><span data-stu-id="d8d84-3441">License</span></span> 
- <span data-ttu-id="d8d84-3442">PC</span><span class="sxs-lookup"><span data-stu-id="d8d84-3442">DL</span></span> 
- <span data-ttu-id="d8d84-3443">DDN
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3443">DOB</span></span> 
- <span data-ttu-id="d8d84-3444">Birthdate</span><span class="sxs-lookup"><span data-stu-id="d8d84-3444">Birthdate</span></span> 
- <span data-ttu-id="d8d84-3445">Anniversaire </span><span class="sxs-lookup"><span data-stu-id="d8d84-3445">Birthday</span></span> 
- <span data-ttu-id="d8d84-3446">Date of Birth
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3446">Date of Birth</span></span> 
   
## <a name="us-social-security-number-ssn"></a><span data-ttu-id="d8d84-3447">Numéro de sécurité sociale (SSN) États-Unis</span><span class="sxs-lookup"><span data-stu-id="d8d84-3447">U.S. Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="d8d84-3448">Format</span><span class="sxs-lookup"><span data-stu-id="d8d84-3448">Format</span></span>

<span data-ttu-id="d8d84-3449">9 chiffres, qui peuvent être mis en forme ou non mis en forme</span><span class="sxs-lookup"><span data-stu-id="d8d84-3449">9 digits, which may be in a formatted or unformatted pattern</span></span>

> [!NOTE]
> <span data-ttu-id="d8d84-3450">La mise en forme d’un numéro de sécurité sociale émis avant le milieu de l’année 2011 est fixe et certaines parties du numéro doivent se situer dans certaines plages pour qu’il soit valide (mais il n’y a pas de somme de contrôle).</span><span class="sxs-lookup"><span data-stu-id="d8d84-3450">If issued before mid-2011, an SSN has strong formatting where certain parts of the number must fall within certain ranges to be valid (but there's no checksum).</span></span>

### <a name="pattern"></a><span data-ttu-id="d8d84-3451">Modèle</span><span class="sxs-lookup"><span data-stu-id="d8d84-3451">Pattern</span></span>

<span data-ttu-id="d8d84-3452">Quatre fonctions permettent de rechercher des numéros de sécurité sociale avec quatre différents modèles :</span><span class="sxs-lookup"><span data-stu-id="d8d84-3452">Four functions look for SSNs in four different patterns:</span></span>
- <span data-ttu-id="d8d84-3453">Func_ssn recherche des numéros de sécurité sociale avec une mise en forme fixe d’avant l’année 2011, mis en forme avec des tirets ou des espaces (ddd-dd-dddd OU ddd dd dddd)</span><span class="sxs-lookup"><span data-stu-id="d8d84-3453">Func_ssn finds SSNs with pre-2011 strong formatting that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="d8d84-3454">Func_unformatted_ssn recherche des numéros de sécurité sociale avec une mise en forme fixe d’avant l’année 2011, avec neuf chiffres consécutifs non mis en forme (ddddddddd)</span><span class="sxs-lookup"><span data-stu-id="d8d84-3454">Func_unformatted_ssn finds SSNs with pre-2011 strong formatting that are unformatted as nine consecutive digits (ddddddddd)</span></span>
- <span data-ttu-id="d8d84-3455">Func_randomized_formatted_ssn recherche des numéros de sécurité sociale d’après l’année 2011, mis en forme avec des tirets ou des espaces  (ddd-dd-dddd OU ddd dd dddd)</span><span class="sxs-lookup"><span data-stu-id="d8d84-3455">Func_randomized_formatted_ssn finds post-2011 SSNs that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="d8d84-3456">Func_randomized_unformatted_ssn recherche des numéros de sécurité sociale d’après l’année 2011, avec neuf chiffres consécutifs non mis en forme (ddddddddd)</span><span class="sxs-lookup"><span data-stu-id="d8d84-3456">Func_randomized_unformatted_ssn finds post-2011 SSNs that are unformatted as nine consecutive digits (ddddddddd)</span></span>

### <a name="checksum"></a><span data-ttu-id="d8d84-3457">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d8d84-3457">Checksum</span></span>

<span data-ttu-id="d8d84-3458">Non</span><span class="sxs-lookup"><span data-stu-id="d8d84-3458">No</span></span>


### <a name="definition"></a><span data-ttu-id="d8d84-3459">Définition</span><span class="sxs-lookup"><span data-stu-id="d8d84-3459">Definition</span></span>

<span data-ttu-id="d8d84-3460">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-3460">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-3461">La fonction Func_ssn trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3461">The function Func_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-3462">Un mot clé figurant dans la liste Keyword_ssn est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3462">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="d8d84-3463">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-3463">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-3464">La fonction Func_unformatted_ssn trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3464">The function Func_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-3465">Un mot clé figurant dans la liste Keyword_ssn est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3465">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="d8d84-3466">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-3466">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-3467">La fonction Func_randomized_formatted_ssn trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3467">The function Func_randomized_formatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-3468">Un mot clé figurant dans la liste Keyword_ssn est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3468">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="d8d84-3469">La fonction Func_ssn ne trouve pas de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3469">The function Func_ssn does not find content that matches the pattern.</span></span>

<span data-ttu-id="d8d84-3470">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 55 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d8d84-3470">A DLP policy is 55% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d8d84-3471">La fonction Func_randomized_unformatted_ssn trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3471">The function Func_randomized_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="d8d84-3472">Un mot clé figurant dans la liste Keyword_ssn est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3472">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="d8d84-3473">La fonction Func_unformatted_ssn ne trouve pas de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d8d84-3473">The function Func_unformatted_ssn does not find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d8d84-3474">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d8d84-3474">Keywords</span></span>

#### <a name="keywordssn"></a><span data-ttu-id="d8d84-3475">Keyword_ssn</span><span class="sxs-lookup"><span data-stu-id="d8d84-3475">Keyword_ssn</span></span>

- <span data-ttu-id="d8d84-3476">Sécurité sociale
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3476">Social Security</span></span> 
- <span data-ttu-id="d8d84-3477"># sécurité sociale
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3477">Social Security#</span></span> 
- <span data-ttu-id="d8d84-3478">Sécu sociale
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3478">Soc Sec</span></span> 
- <span data-ttu-id="d8d84-3479">SSN</span><span class="sxs-lookup"><span data-stu-id="d8d84-3479">SSN</span></span> 
- <span data-ttu-id="d8d84-3480">NSS
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3480">SSNS</span></span> 
- <span data-ttu-id="d8d84-3481">#NSS
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3481">SSN#</span></span> 
- <span data-ttu-id="d8d84-3482"># SS
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3482">SS#</span></span> 
- <span data-ttu-id="d8d84-3483">IDSS
</span><span class="sxs-lookup"><span data-stu-id="d8d84-3483">SSID</span></span> 
   

