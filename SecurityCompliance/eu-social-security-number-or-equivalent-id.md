---
title: ID de numéro de sécurité sociale de l’Union européenne ou équivalent
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 1fabd341-e594-4bfe-961c-62aa82893f60
description: Cette rubrique illustre une stratégie de protection contre la perte données lorsqu’il détecte le type d’informations sensibles numéro de sécurité sociale de l’Union européenne ou ID équivalente. Ce type d’informations sensibles définit différents motifs, mots clés et autres pour chaque pays.
ms.openlocfilehash: 6f1027dcfb648ed937b8180d74d4bc6348dab650
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527983"
---
# <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="5f8bd-104">ID de numéro de sécurité sociale de l’Union européenne ou équivalent</span><span class="sxs-lookup"><span data-stu-id="5f8bd-104">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="5f8bd-p102">Cette rubrique illustre une stratégie de protection contre la perte données lorsqu’il détecte le type d’informations sensibles UE numéro de sécurité sociale (SSN) ou ID équivalente. Ce type d’informations sensibles définit différents motifs, mots clés et autres pour chaque pays.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Social Security Number (SSN) or Equivalent ID sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="5f8bd-107">Autriche</span><span class="sxs-lookup"><span data-stu-id="5f8bd-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="5f8bd-108">Format</span><span class="sxs-lookup"><span data-stu-id="5f8bd-108">Format</span></span>

<span data-ttu-id="5f8bd-109">10 chiffres dans le format spécifié</span><span class="sxs-lookup"><span data-stu-id="5f8bd-109">10 digits in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5f8bd-110">Modèle</span><span class="sxs-lookup"><span data-stu-id="5f8bd-110">Pattern</span></span>

<span data-ttu-id="5f8bd-111">10 chiffres :</span><span class="sxs-lookup"><span data-stu-id="5f8bd-111">10 digits:</span></span>
  
-  <span data-ttu-id="5f8bd-112">Trois chiffres qui correspondent à un numéro de série</span><span class="sxs-lookup"><span data-stu-id="5f8bd-112">Three digits that correspond to a serial number</span></span> 
    
- <span data-ttu-id="5f8bd-113">Chiffre un contrôle</span><span class="sxs-lookup"><span data-stu-id="5f8bd-113">One check digit</span></span>
    
- <span data-ttu-id="5f8bd-114">Six chiffres qui correspondent à la date de naissance (jjmmaa)</span><span class="sxs-lookup"><span data-stu-id="5f8bd-114">Six digits that correspond to the birth date (DDMMYY)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="5f8bd-115">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="5f8bd-115">Checksum</span></span>

<span data-ttu-id="5f8bd-116">Oui</span><span class="sxs-lookup"><span data-stu-id="5f8bd-116">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="5f8bd-117">Définition</span><span class="sxs-lookup"><span data-stu-id="5f8bd-117">Definition</span></span>

<span data-ttu-id="5f8bd-118">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5f8bd-118">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5f8bd-119">La fonction `Func_austria_eu_ssn_or_equivalent` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-119">The function  `Func_austria_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5f8bd-120">Un mot clé à partir de `Keywords_austria_eu_ssn_or_equivalent` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-120">A keyword from  `Keywords_austria_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="5f8bd-121">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5f8bd-121">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5f8bd-122">La fonction `Func_austria_eu_ssn_or_equivalent` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-122">The function  `Func_austria_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_austria_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_austria_eu_ssn_or_equivalent" />
        </Pattern>
<Pattern confidenceLevel="75">
            <IdMatch idRef="Func_austria_eu_ssn_or_equivalent" />
          </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5f8bd-123">Keywords</span><span class="sxs-lookup"><span data-stu-id="5f8bd-123">Keywords</span></span>

#### <a name="keywordsaustriaeussnorequivalent"></a><span data-ttu-id="5f8bd-124">Keywords_austria_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="5f8bd-124">Keywords_austria_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="5f8bd-125">sécurité sociale aucune</span><span class="sxs-lookup"><span data-stu-id="5f8bd-125">social security no</span></span>
  
<span data-ttu-id="5f8bd-126">numéro de sécurité sociale
</span><span class="sxs-lookup"><span data-stu-id="5f8bd-126">social security number</span></span>
  
<span data-ttu-id="5f8bd-127">
code de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="5f8bd-127">social security code</span></span>
  
<span data-ttu-id="5f8bd-128">numéro d’assurance</span><span class="sxs-lookup"><span data-stu-id="5f8bd-128">insurance number</span></span>
  
<span data-ttu-id="5f8bd-129">Schilling ssn</span><span class="sxs-lookup"><span data-stu-id="5f8bd-129">austrian ssn</span></span>
  
<span data-ttu-id="5f8bd-130">ssn #</span><span class="sxs-lookup"><span data-stu-id="5f8bd-130">ssn#</span></span>
  
<span data-ttu-id="5f8bd-131">ssn</span><span class="sxs-lookup"><span data-stu-id="5f8bd-131">ssn</span></span>
  
<span data-ttu-id="5f8bd-132">code d’assurance</span><span class="sxs-lookup"><span data-stu-id="5f8bd-132">insurance code</span></span>
  
<span data-ttu-id="5f8bd-133">code d’assurance #</span><span class="sxs-lookup"><span data-stu-id="5f8bd-133">insurance code#</span></span>
  
<span data-ttu-id="5f8bd-134">socialsecurityno #</span><span class="sxs-lookup"><span data-stu-id="5f8bd-134">socialsecurityno#</span></span>
  
<span data-ttu-id="5f8bd-135">sozialversicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="5f8bd-135">sozialversicherungsnummer</span></span>
  
<span data-ttu-id="5f8bd-136">soziale sicherheit kein</span><span class="sxs-lookup"><span data-stu-id="5f8bd-136">soziale sicherheit kein</span></span>
  
<span data-ttu-id="5f8bd-137">versicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="5f8bd-137">versicherungsnummer</span></span>
  
## <a name="belgium"></a><span data-ttu-id="5f8bd-138">Belgique</span><span class="sxs-lookup"><span data-stu-id="5f8bd-138">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="5f8bd-139">Format</span><span class="sxs-lookup"><span data-stu-id="5f8bd-139">Format</span></span>

<span data-ttu-id="5f8bd-140">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="5f8bd-140">11 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5f8bd-141">Modèle</span><span class="sxs-lookup"><span data-stu-id="5f8bd-141">Pattern</span></span>

<span data-ttu-id="5f8bd-142">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="5f8bd-142">11 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="5f8bd-143">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="5f8bd-143">Checksum</span></span>

<span data-ttu-id="5f8bd-144">Oui</span><span class="sxs-lookup"><span data-stu-id="5f8bd-144">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="5f8bd-145">Définition</span><span class="sxs-lookup"><span data-stu-id="5f8bd-145">Definition</span></span>

<span data-ttu-id="5f8bd-146">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5f8bd-146">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5f8bd-147">La fonction `Func_belgium_eu_ssn_or_equivalent` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-147">The function  `Func_belgium_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5f8bd-148">Un mot clé à partir de `Keywords_belgium_eu_ssn_or_equivalent` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-148">A keyword from  `Keywords_belgium_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="5f8bd-149">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5f8bd-149">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5f8bd-150">La fonction `Func_belgium_eu_ssn_or_equivalent` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-150">The function  `Func_belgium_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_belgium_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_belgium_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_belgium_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5f8bd-151">Keywords</span><span class="sxs-lookup"><span data-stu-id="5f8bd-151">Keywords</span></span>

#### <a name="keywordsbelgiumeussnorequivalent"></a><span data-ttu-id="5f8bd-152">Keywords_belgium_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="5f8bd-152">Keywords_belgium_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="5f8bd-153">numéro national belge</span><span class="sxs-lookup"><span data-stu-id="5f8bd-153">belgian national number</span></span>
  
<span data-ttu-id="5f8bd-154">numéro national</span><span class="sxs-lookup"><span data-stu-id="5f8bd-154">national number</span></span>
  
<span data-ttu-id="5f8bd-155">numéro de sécurité sociale
</span><span class="sxs-lookup"><span data-stu-id="5f8bd-155">social security number</span></span>
  
<span data-ttu-id="5f8bd-156">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="5f8bd-156">nationalnumber#</span></span>
  
<span data-ttu-id="5f8bd-157">ssn #</span><span class="sxs-lookup"><span data-stu-id="5f8bd-157">ssn#</span></span>
  
<span data-ttu-id="5f8bd-158">ssn</span><span class="sxs-lookup"><span data-stu-id="5f8bd-158">ssn</span></span>
  
<span data-ttu-id="5f8bd-159">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="5f8bd-159">nationalnumber</span></span>
  
<span data-ttu-id="5f8bd-160">bnn #</span><span class="sxs-lookup"><span data-stu-id="5f8bd-160">bnn#</span></span>
  
<span data-ttu-id="5f8bd-161">bnn</span><span class="sxs-lookup"><span data-stu-id="5f8bd-161">bnn</span></span>
  
<span data-ttu-id="5f8bd-162">numéro d’identification personnelle</span><span class="sxs-lookup"><span data-stu-id="5f8bd-162">personal id number</span></span>
  
<span data-ttu-id="5f8bd-163">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="5f8bd-163">personalidnumber#</span></span>
  
<span data-ttu-id="5f8bd-164">numéro national</span><span class="sxs-lookup"><span data-stu-id="5f8bd-164">numéro national</span></span>
  
<span data-ttu-id="5f8bd-165">numéro de sécurité
</span><span class="sxs-lookup"><span data-stu-id="5f8bd-165">numéro de sécurité</span></span>
  
<span data-ttu-id="5f8bd-166">numéro d'assuré</span><span class="sxs-lookup"><span data-stu-id="5f8bd-166">numéro d'assuré</span></span>
  
<span data-ttu-id="5f8bd-167">Identifiant national</span><span class="sxs-lookup"><span data-stu-id="5f8bd-167">identifiant national</span></span>
  
<span data-ttu-id="5f8bd-168">identifiantnational #</span><span class="sxs-lookup"><span data-stu-id="5f8bd-168">identifiantnational#</span></span>
  
<span data-ttu-id="5f8bd-169">numéronational #</span><span class="sxs-lookup"><span data-stu-id="5f8bd-169">numéronational#</span></span>
  
## <a name="croatia"></a><span data-ttu-id="5f8bd-170">Croatie</span><span class="sxs-lookup"><span data-stu-id="5f8bd-170">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="5f8bd-171">Format</span><span class="sxs-lookup"><span data-stu-id="5f8bd-171">Format</span></span>

<span data-ttu-id="5f8bd-172">11 chiffres sans espaces et les séparateurs</span><span class="sxs-lookup"><span data-stu-id="5f8bd-172">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5f8bd-173">Modèle</span><span class="sxs-lookup"><span data-stu-id="5f8bd-173">Pattern</span></span>

 <span data-ttu-id="5f8bd-174">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="5f8bd-174">11 digits:</span></span> 
  
-  <span data-ttu-id="5f8bd-175">Dix chiffres</span><span class="sxs-lookup"><span data-stu-id="5f8bd-175">Ten digits</span></span> 
    
- <span data-ttu-id="5f8bd-176">Chiffre un contrôle</span><span class="sxs-lookup"><span data-stu-id="5f8bd-176">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="5f8bd-177">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="5f8bd-177">Checksum</span></span>

<span data-ttu-id="5f8bd-178">Oui</span><span class="sxs-lookup"><span data-stu-id="5f8bd-178">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="5f8bd-179">Définition</span><span class="sxs-lookup"><span data-stu-id="5f8bd-179">Definition</span></span>

<span data-ttu-id="5f8bd-180">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5f8bd-180">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5f8bd-181">La fonction `Func_croatia_eu_ssn_or_equivalent` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-181">The function  `Func_croatia_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5f8bd-182">Un mot clé à partir de `Keywords_croatia_eu_ssn_or_equivalent` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-182">A keyword from  `Keywords_croatia_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="5f8bd-183">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5f8bd-183">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5f8bd-184">La fonction `Func_croatia_eu_ssn_or_equivalent` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-184">The function  `Func_croatia_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_croatia_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_croatia_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_croatia_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5f8bd-185">Keywords</span><span class="sxs-lookup"><span data-stu-id="5f8bd-185">Keywords</span></span>

#### <a name="keywordscroatiaeussnorequivalent"></a><span data-ttu-id="5f8bd-186">Keywords_croatia_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="5f8bd-186">Keywords_croatia_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="5f8bd-187">numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="5f8bd-187">personal identification number</span></span>
  
<span data-ttu-id="5f8bd-188">nombre de maîtres citoyens</span><span class="sxs-lookup"><span data-stu-id="5f8bd-188">master citizen number</span></span>
  
<span data-ttu-id="5f8bd-189">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="5f8bd-189">national identification number</span></span>
  
<span data-ttu-id="5f8bd-190">numéro de sécurité sociale
</span><span class="sxs-lookup"><span data-stu-id="5f8bd-190">social security number</span></span>
  
<span data-ttu-id="5f8bd-191">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="5f8bd-191">nationalnumber#</span></span>
  
<span data-ttu-id="5f8bd-192">ssn #</span><span class="sxs-lookup"><span data-stu-id="5f8bd-192">ssn#</span></span>
  
<span data-ttu-id="5f8bd-193">ssn</span><span class="sxs-lookup"><span data-stu-id="5f8bd-193">ssn</span></span>
  
<span data-ttu-id="5f8bd-194">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="5f8bd-194">nationalnumber</span></span>
  
<span data-ttu-id="5f8bd-195">bnn #</span><span class="sxs-lookup"><span data-stu-id="5f8bd-195">bnn#</span></span>
  
<span data-ttu-id="5f8bd-196">bnn</span><span class="sxs-lookup"><span data-stu-id="5f8bd-196">bnn</span></span>
  
<span data-ttu-id="5f8bd-197">numéro d’identification personnelle</span><span class="sxs-lookup"><span data-stu-id="5f8bd-197">personal id number</span></span>
  
<span data-ttu-id="5f8bd-198">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="5f8bd-198">personalidnumber#</span></span>
  
<span data-ttu-id="5f8bd-199">oib</span><span class="sxs-lookup"><span data-stu-id="5f8bd-199">oib</span></span>
  
<span data-ttu-id="5f8bd-200">osobni identifikacijski broj</span><span class="sxs-lookup"><span data-stu-id="5f8bd-200">osobni identifikacijski broj</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="5f8bd-201">République tchèque</span><span class="sxs-lookup"><span data-stu-id="5f8bd-201">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="5f8bd-202">Format</span><span class="sxs-lookup"><span data-stu-id="5f8bd-202">Format</span></span>

<span data-ttu-id="5f8bd-203">Dix chiffres et une barre oblique inverse dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="5f8bd-203">Ten digits and a backslash in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5f8bd-204">Modèle</span><span class="sxs-lookup"><span data-stu-id="5f8bd-204">Pattern</span></span>

<span data-ttu-id="5f8bd-205">Dix chiffres et une barre oblique inverse :</span><span class="sxs-lookup"><span data-stu-id="5f8bd-205">Ten digits and a backslash:</span></span>
  
- <span data-ttu-id="5f8bd-206">Six chiffres qui correspondent à la date de naissance (AAMMJJ) :</span><span class="sxs-lookup"><span data-stu-id="5f8bd-206">Six digits that correspond to the birth date (YYMMDD):</span></span> 
    
- <span data-ttu-id="5f8bd-207">Une barre oblique inverse</span><span class="sxs-lookup"><span data-stu-id="5f8bd-207">A backslash</span></span>
    
- <span data-ttu-id="5f8bd-208">Trois chiffres qui correspondent à un numéro de série qui sépare les personnes naissance à la même date</span><span class="sxs-lookup"><span data-stu-id="5f8bd-208">Three digits that correspond to a serial number that separates persons born on the same date</span></span>
    
- <span data-ttu-id="5f8bd-209">Chiffre un contrôle</span><span class="sxs-lookup"><span data-stu-id="5f8bd-209">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="5f8bd-210">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="5f8bd-210">Checksum</span></span>

<span data-ttu-id="5f8bd-211">Oui</span><span class="sxs-lookup"><span data-stu-id="5f8bd-211">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="5f8bd-212">Définition</span><span class="sxs-lookup"><span data-stu-id="5f8bd-212">Definition</span></span>

<span data-ttu-id="5f8bd-213">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5f8bd-213">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5f8bd-214">La fonction `Func_czech_republic_eu_ssn_or_equivalent` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-214">The function  `Func_czech_republic_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5f8bd-215">Un mot clé à partir de `Keywords_czech_republic_eu_ssn_or_equivalent` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-215">A keyword from  `Keywords_czech_republic_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="5f8bd-216">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5f8bd-216">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5f8bd-217">La fonction `Func_czech_republic_eu_ssn_or_equivalent` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-217">The function  `Func_czech_republic_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_czech_republic_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_czech_republic_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_czech_republic_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5f8bd-218">Keywords</span><span class="sxs-lookup"><span data-stu-id="5f8bd-218">Keywords</span></span>

#### <a name="keywordsczechrepubliceussnorequivalent"></a><span data-ttu-id="5f8bd-219">Keywords_czech_republic_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="5f8bd-219">Keywords_czech_republic_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="5f8bd-220">nombre de naissance</span><span class="sxs-lookup"><span data-stu-id="5f8bd-220">birth number</span></span>
  
<span data-ttu-id="5f8bd-221">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="5f8bd-221">national identification number</span></span>
  
<span data-ttu-id="5f8bd-222">numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="5f8bd-222">personal identification number</span></span>
  
<span data-ttu-id="5f8bd-223">numéro de sécurité sociale
</span><span class="sxs-lookup"><span data-stu-id="5f8bd-223">social security number</span></span>
  
<span data-ttu-id="5f8bd-224">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="5f8bd-224">nationalnumber#</span></span>
  
<span data-ttu-id="5f8bd-225">ssn #</span><span class="sxs-lookup"><span data-stu-id="5f8bd-225">ssn#</span></span>
  
<span data-ttu-id="5f8bd-226">ssn</span><span class="sxs-lookup"><span data-stu-id="5f8bd-226">ssn</span></span>
  
<span data-ttu-id="5f8bd-227">numéro national</span><span class="sxs-lookup"><span data-stu-id="5f8bd-227">national number</span></span>
  
<span data-ttu-id="5f8bd-228">numéro d’identification personnelle</span><span class="sxs-lookup"><span data-stu-id="5f8bd-228">personal id number</span></span>
  
<span data-ttu-id="5f8bd-229">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="5f8bd-229">personalidnumber#</span></span>
  
<span data-ttu-id="5f8bd-230">rč</span><span class="sxs-lookup"><span data-stu-id="5f8bd-230">rč</span></span>
  
<span data-ttu-id="5f8bd-231">rodné číslo</span><span class="sxs-lookup"><span data-stu-id="5f8bd-231">rodné číslo</span></span>
  
<span data-ttu-id="5f8bd-232">rodne cislo</span><span class="sxs-lookup"><span data-stu-id="5f8bd-232">rodne cislo</span></span>
  
## <a name="denmark"></a><span data-ttu-id="5f8bd-233">Danemark</span><span class="sxs-lookup"><span data-stu-id="5f8bd-233">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="5f8bd-234">Format</span><span class="sxs-lookup"><span data-stu-id="5f8bd-234">Format</span></span>

<span data-ttu-id="5f8bd-235">Dix chiffres et un trait d’union dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="5f8bd-235">Ten digits and a hyphen in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5f8bd-236">Modèle</span><span class="sxs-lookup"><span data-stu-id="5f8bd-236">Pattern</span></span>

<span data-ttu-id="5f8bd-237">Dix chiffres et un trait d’union :</span><span class="sxs-lookup"><span data-stu-id="5f8bd-237">Ten digits and a hyphen:</span></span>
  
- <span data-ttu-id="5f8bd-238">Six chiffres qui correspondent à la date de naissance (jjmmaa)</span><span class="sxs-lookup"><span data-stu-id="5f8bd-238">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="5f8bd-239">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="5f8bd-239">A hyphen</span></span>
    
- <span data-ttu-id="5f8bd-240">Quatre chiffres qui correspondent à un numéro de séquence</span><span class="sxs-lookup"><span data-stu-id="5f8bd-240">Four digits that correspond to a sequence number</span></span>
    
### <a name="checksum"></a><span data-ttu-id="5f8bd-241">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="5f8bd-241">Checksum</span></span>

<span data-ttu-id="5f8bd-242">Oui</span><span class="sxs-lookup"><span data-stu-id="5f8bd-242">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="5f8bd-243">Définition</span><span class="sxs-lookup"><span data-stu-id="5f8bd-243">Definition</span></span>

<span data-ttu-id="5f8bd-244">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5f8bd-244">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5f8bd-245">La fonction `Func_denmark_eu_ssn_or_equivalent` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-245">The function  `Func_denmark_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5f8bd-246">Un mot clé à partir de `Keywords_denmark_eu_ssn_or_equivalent` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-246">A keyword from  `Keywords_denmark_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="5f8bd-247">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5f8bd-247">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5f8bd-248">La fonction `Func_denmark_eu_ssn_or_equivalent` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-248">The function  `Func_denmark_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_denmark_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_denmark_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_denmark_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5f8bd-249">Keywords</span><span class="sxs-lookup"><span data-stu-id="5f8bd-249">Keywords</span></span>

#### <a name="keywordsdenmarkeussnorequivalent"></a><span data-ttu-id="5f8bd-250">Keywords_denmark_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="5f8bd-250">Keywords_denmark_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="5f8bd-251">numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="5f8bd-251">personal identification number</span></span>
  
<span data-ttu-id="5f8bd-252">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="5f8bd-252">national identification number</span></span>
  
<span data-ttu-id="5f8bd-253">numéro de sécurité sociale
</span><span class="sxs-lookup"><span data-stu-id="5f8bd-253">social security number</span></span>
  
<span data-ttu-id="5f8bd-254">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="5f8bd-254">nationalnumber#</span></span>
  
<span data-ttu-id="5f8bd-255">ssn #</span><span class="sxs-lookup"><span data-stu-id="5f8bd-255">ssn#</span></span>
  
<span data-ttu-id="5f8bd-256">ssn</span><span class="sxs-lookup"><span data-stu-id="5f8bd-256">ssn</span></span>
  
<span data-ttu-id="5f8bd-257">numéro national</span><span class="sxs-lookup"><span data-stu-id="5f8bd-257">national number</span></span>
  
<span data-ttu-id="5f8bd-258">numéro d’identification personnelle</span><span class="sxs-lookup"><span data-stu-id="5f8bd-258">personal id number</span></span>
  
<span data-ttu-id="5f8bd-259">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="5f8bd-259">personalidnumber#</span></span>
  
<span data-ttu-id="5f8bd-260">CPR-nummer</span><span class="sxs-lookup"><span data-stu-id="5f8bd-260">cpr-nummer</span></span>
  
<span data-ttu-id="5f8bd-261">personnummer</span><span class="sxs-lookup"><span data-stu-id="5f8bd-261">personnummer</span></span>
  
## <a name="finland"></a><span data-ttu-id="5f8bd-262">Finlande</span><span class="sxs-lookup"><span data-stu-id="5f8bd-262">Finland</span></span>

### <a name="format"></a><span data-ttu-id="5f8bd-263">Format</span><span class="sxs-lookup"><span data-stu-id="5f8bd-263">Format</span></span>

<span data-ttu-id="5f8bd-264">Une combinaison de 11 caractères au format spécifié</span><span class="sxs-lookup"><span data-stu-id="5f8bd-264">An 11-character combination in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5f8bd-265">Modèle</span><span class="sxs-lookup"><span data-stu-id="5f8bd-265">Pattern</span></span>

<span data-ttu-id="5f8bd-266">Une combinaison de 11 caractères au format spécifié :</span><span class="sxs-lookup"><span data-stu-id="5f8bd-266">An 11-character combination in the specified format:</span></span>
  
-  <span data-ttu-id="5f8bd-267">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="5f8bd-267">Six digits</span></span> 
    
- <span data-ttu-id="5f8bd-268">Une seule instance d’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="5f8bd-268">One instance of one of the following:</span></span>
    
  - <span data-ttu-id="5f8bd-269">Plus de symbole</span><span class="sxs-lookup"><span data-stu-id="5f8bd-269">Plus symbol</span></span>
    
  - <span data-ttu-id="5f8bd-270">Moins de symbole</span><span class="sxs-lookup"><span data-stu-id="5f8bd-270">Minus symbol</span></span>
    
  - <span data-ttu-id="5f8bd-271">La lettre « A » (pas la casse)</span><span class="sxs-lookup"><span data-stu-id="5f8bd-271">The letter "A" (not case-sensitive)</span></span>
    
- <span data-ttu-id="5f8bd-272">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="5f8bd-272">Three digits</span></span>
    
- <span data-ttu-id="5f8bd-273">Une lettre ou un chiffre</span><span class="sxs-lookup"><span data-stu-id="5f8bd-273">One letter or one digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="5f8bd-274">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="5f8bd-274">Checksum</span></span>

<span data-ttu-id="5f8bd-275">Oui</span><span class="sxs-lookup"><span data-stu-id="5f8bd-275">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="5f8bd-276">Définition</span><span class="sxs-lookup"><span data-stu-id="5f8bd-276">Definition</span></span>

<span data-ttu-id="5f8bd-277">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5f8bd-277">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5f8bd-278">La fonction `Func_finland_eu_ssn_or_equivalent` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-278">The function  `Func_finland_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5f8bd-279">Un mot clé à partir de `Keywords_finland_eu_ssn_or_equivalent` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-279">A keyword from  `Keywords_finland_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="5f8bd-280">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5f8bd-280">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5f8bd-281">La fonction `Func_finland_eu_ssn_or_equivalent` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-281">The function  `Func_finland_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finland_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_finland_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_finland_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5f8bd-282">Keywords</span><span class="sxs-lookup"><span data-stu-id="5f8bd-282">Keywords</span></span>

#### <a name="keywordsfinlandeussnorequivalent"></a><span data-ttu-id="5f8bd-283">Keywords_finland_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="5f8bd-283">Keywords_finland_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="5f8bd-284">numéro d’identification
</span><span class="sxs-lookup"><span data-stu-id="5f8bd-284">identification number</span></span>
  
<span data-ttu-id="5f8bd-285">identifiant personnel</span><span class="sxs-lookup"><span data-stu-id="5f8bd-285">personal id</span></span>
  
<span data-ttu-id="5f8bd-286">numéro d’identité</span><span class="sxs-lookup"><span data-stu-id="5f8bd-286">identity number</span></span>
  
<span data-ttu-id="5f8bd-287">numéro d’id national Finlande</span><span class="sxs-lookup"><span data-stu-id="5f8bd-287">finnish national id number</span></span>
  
<span data-ttu-id="5f8bd-288">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="5f8bd-288">personalidnumber#</span></span>
  
<span data-ttu-id="5f8bd-289">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="5f8bd-289">national identification number</span></span>
  
<span data-ttu-id="5f8bd-290">numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="5f8bd-290">id number</span></span>
  
<span data-ttu-id="5f8bd-291">id national aucun.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-291">national id no.</span></span>
  
<span data-ttu-id="5f8bd-292">numéro national</span><span class="sxs-lookup"><span data-stu-id="5f8bd-292">national id number</span></span>
  
<span data-ttu-id="5f8bd-293">ID d’aucun</span><span class="sxs-lookup"><span data-stu-id="5f8bd-293">id no</span></span>
  
<span data-ttu-id="5f8bd-294">tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="5f8bd-294">tunnistenumero</span></span>
  
<span data-ttu-id="5f8bd-295">henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="5f8bd-295">henkilötunnus</span></span>
  
<span data-ttu-id="5f8bd-296">yksilöllinen henkilökohtainen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="5f8bd-296">yksilöllinen henkilökohtainen tunnistenumero</span></span>
  
<span data-ttu-id="5f8bd-297">ainutlaatuinen henkilökohtainen tunnus</span><span class="sxs-lookup"><span data-stu-id="5f8bd-297">ainutlaatuinen henkilökohtainen tunnus</span></span>
  
<span data-ttu-id="5f8bd-298">numero identiteetti</span><span class="sxs-lookup"><span data-stu-id="5f8bd-298">identiteetti numero</span></span>
  
<span data-ttu-id="5f8bd-299">Suomen kansallinen henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="5f8bd-299">suomen kansallinen henkilötunnus</span></span>
  
<span data-ttu-id="5f8bd-300">henkilötunnusnumero #</span><span class="sxs-lookup"><span data-stu-id="5f8bd-300">henkilötunnusnumero#</span></span>
  
<span data-ttu-id="5f8bd-301">kansallisen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="5f8bd-301">kansallisen tunnistenumero</span></span>
  
<span data-ttu-id="5f8bd-302">tunnusnumero</span><span class="sxs-lookup"><span data-stu-id="5f8bd-302">tunnusnumero</span></span>
  
<span data-ttu-id="5f8bd-303">kansallinen tunnus numero</span><span class="sxs-lookup"><span data-stu-id="5f8bd-303">kansallinen tunnus numero</span></span>
  
<span data-ttu-id="5f8bd-304">hetu</span><span class="sxs-lookup"><span data-stu-id="5f8bd-304">hetu</span></span>
  
## <a name="france"></a><span data-ttu-id="5f8bd-305">France</span><span class="sxs-lookup"><span data-stu-id="5f8bd-305">France</span></span>

<span data-ttu-id="5f8bd-306">Pour plus d’informations, consultez la section « France numéro de sécurité sociale (INSEE) » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="5f8bd-306">For details, see the section "France Social Security Number (INSEE)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="5f8bd-307">Allemagne</span><span class="sxs-lookup"><span data-stu-id="5f8bd-307">Germany</span></span>

<span data-ttu-id="5f8bd-308">Pour plus d’informations, consultez la section « Numéro de carte d’identité Allemagne » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="5f8bd-308">For details, see the section "Germany Identity Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="5f8bd-309">Grèce</span><span class="sxs-lookup"><span data-stu-id="5f8bd-309">Greece</span></span>

<span data-ttu-id="5f8bd-310">Pour plus d’informations, consultez la section « Grèce carte » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="5f8bd-310">For details, see the section "Greece National ID Card" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="hungary"></a><span data-ttu-id="5f8bd-311">Hongrie</span><span class="sxs-lookup"><span data-stu-id="5f8bd-311">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="5f8bd-312">Format</span><span class="sxs-lookup"><span data-stu-id="5f8bd-312">Format</span></span>

<span data-ttu-id="5f8bd-313">Neuf chiffres sans espaces et les séparateurs</span><span class="sxs-lookup"><span data-stu-id="5f8bd-313">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5f8bd-314">Modèle</span><span class="sxs-lookup"><span data-stu-id="5f8bd-314">Pattern</span></span>

<span data-ttu-id="5f8bd-315">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="5f8bd-315">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="5f8bd-316">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="5f8bd-316">Checksum</span></span>

<span data-ttu-id="5f8bd-317">Oui</span><span class="sxs-lookup"><span data-stu-id="5f8bd-317">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="5f8bd-318">Définition</span><span class="sxs-lookup"><span data-stu-id="5f8bd-318">Definition</span></span>

<span data-ttu-id="5f8bd-319">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5f8bd-319">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5f8bd-320">La fonction `Func_hungary_eu_ssn_or_equivalent` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-320">The function  `Func_hungary_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5f8bd-321">Un mot clé à partir de `Keywords_hungary_eu_ssn_or_equivalent` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-321">A keyword from  `Keywords_hungary_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="5f8bd-322">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5f8bd-322">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5f8bd-323">La fonction `Func_hungary_eu_ssn_or_equivalent` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-323">The function  `Func_hungary_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_hungary_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_hungary_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_hungary_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5f8bd-324">Keywords</span><span class="sxs-lookup"><span data-stu-id="5f8bd-324">Keywords</span></span>

#### <a name="keywordshungaryeussnorequivalent"></a><span data-ttu-id="5f8bd-325">Keywords_hungary_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="5f8bd-325">Keywords_hungary_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="5f8bd-326">numéro de sécurité sociale hongrois</span><span class="sxs-lookup"><span data-stu-id="5f8bd-326">hungarian social security number</span></span>
  
<span data-ttu-id="5f8bd-327">numéro de sécurité sociale
</span><span class="sxs-lookup"><span data-stu-id="5f8bd-327">social security number</span></span>
  
<span data-ttu-id="5f8bd-328">socialsecuritynumber #</span><span class="sxs-lookup"><span data-stu-id="5f8bd-328">socialsecuritynumber#</span></span>
  
<span data-ttu-id="5f8bd-329">hssn #</span><span class="sxs-lookup"><span data-stu-id="5f8bd-329">hssn#</span></span>
  
<span data-ttu-id="5f8bd-330">socialsecuritynno</span><span class="sxs-lookup"><span data-stu-id="5f8bd-330">socialsecuritynno</span></span>
  
<span data-ttu-id="5f8bd-331">hssn</span><span class="sxs-lookup"><span data-stu-id="5f8bd-331">hssn</span></span>
  
<span data-ttu-id="5f8bd-332">TAJ</span><span class="sxs-lookup"><span data-stu-id="5f8bd-332">taj</span></span>
  
<span data-ttu-id="5f8bd-333">TAJ #</span><span class="sxs-lookup"><span data-stu-id="5f8bd-333">taj#</span></span>
  
<span data-ttu-id="5f8bd-334">ssn</span><span class="sxs-lookup"><span data-stu-id="5f8bd-334">ssn</span></span>
  
<span data-ttu-id="5f8bd-335">ssn #</span><span class="sxs-lookup"><span data-stu-id="5f8bd-335">ssn#</span></span>
  
<span data-ttu-id="5f8bd-336">sécurité sociale aucune</span><span class="sxs-lookup"><span data-stu-id="5f8bd-336">social security no</span></span>
  
<span data-ttu-id="5f8bd-337">áfa</span><span class="sxs-lookup"><span data-stu-id="5f8bd-337">áfa</span></span>
  
<span data-ttu-id="5f8bd-338">közösségi adószám</span><span class="sxs-lookup"><span data-stu-id="5f8bd-338">közösségi adószám</span></span>
  
<span data-ttu-id="5f8bd-339">általános forgalmi adó szám</span><span class="sxs-lookup"><span data-stu-id="5f8bd-339">általános forgalmi adó szám</span></span>
  
<span data-ttu-id="5f8bd-340">hozzáadottérték adó</span><span class="sxs-lookup"><span data-stu-id="5f8bd-340">hozzáadottérték adó</span></span>
  
<span data-ttu-id="5f8bd-341">áfa szám</span><span class="sxs-lookup"><span data-stu-id="5f8bd-341">áfa szám</span></span>
  
<span data-ttu-id="5f8bd-342">áfa magyar szám</span><span class="sxs-lookup"><span data-stu-id="5f8bd-342">magyar áfa szám</span></span>
  
## <a name="portugal"></a><span data-ttu-id="5f8bd-343">Portugal</span><span class="sxs-lookup"><span data-stu-id="5f8bd-343">Portugal</span></span>

<span data-ttu-id="5f8bd-344">Pour plus d’informations, consultez la section « Portugal citoyens carte numéro » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="5f8bd-344">For details, see the section "Portugal Citizen Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="spain"></a><span data-ttu-id="5f8bd-345">Espagne</span><span class="sxs-lookup"><span data-stu-id="5f8bd-345">Spain</span></span>

<span data-ttu-id="5f8bd-346">Pour plus d’informations, consultez la section « Espagne numéro de sécurité sociale (SSN) » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="5f8bd-346">For details, see the section "Spain Social Security Number (SSN)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="sweden"></a><span data-ttu-id="5f8bd-347">Suède</span><span class="sxs-lookup"><span data-stu-id="5f8bd-347">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="5f8bd-348">Format</span><span class="sxs-lookup"><span data-stu-id="5f8bd-348">Format</span></span>

<span data-ttu-id="5f8bd-349">12 chiffres sans espaces et les séparateurs</span><span class="sxs-lookup"><span data-stu-id="5f8bd-349">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5f8bd-350">Modèle</span><span class="sxs-lookup"><span data-stu-id="5f8bd-350">Pattern</span></span>

<span data-ttu-id="5f8bd-351">12 chiffres :</span><span class="sxs-lookup"><span data-stu-id="5f8bd-351">12 digits:</span></span>
  
-  <span data-ttu-id="5f8bd-352">Huit chiffres qui correspondent à la date de naissance (AAAAMMJJ)</span><span class="sxs-lookup"><span data-stu-id="5f8bd-352">Eight digits that correspond to the birth date (YYYYMMDD)</span></span> 
    
- <span data-ttu-id="5f8bd-353">Trois chiffres qui correspondent à un numéro de série où :</span><span class="sxs-lookup"><span data-stu-id="5f8bd-353">Three digits that correspond to a serial number where:</span></span> 
    
  - <span data-ttu-id="5f8bd-354">Le dernier chiffre du numéro de série indique le sexe par l’affectation d’un nombre impair de masculin et un nombre pair pour femme</span><span class="sxs-lookup"><span data-stu-id="5f8bd-354">The last digit in the serial number indicates gender by the assignment of an odd number for male and an even number for female</span></span>
    
  - <span data-ttu-id="5f8bd-355">Jusqu'à 1990, l’affectation de numéro de série correspondant à la région où le support du nombre de naissance ou (si naissance avant 1947) où il avait été courantes, en fonction des enregistrements de taxe sur 1 janvier 1947, avec un code spécial (généralement 9 en tant que le chiffre 7) pour immigrants</span><span class="sxs-lookup"><span data-stu-id="5f8bd-355">Up to 1990, the assignment of serial number corresponded to the county where the bearer of the number was born or (if born before 1947) where he/she had been living, according to tax records, on January 1, 1947, with a special code (usually 9 as the 7th digit) for immigrants</span></span> 
    
- <span data-ttu-id="5f8bd-356">Chiffre un contrôle</span><span class="sxs-lookup"><span data-stu-id="5f8bd-356">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="5f8bd-357">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="5f8bd-357">Checksum</span></span>

<span data-ttu-id="5f8bd-358">Oui</span><span class="sxs-lookup"><span data-stu-id="5f8bd-358">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="5f8bd-359">Définition</span><span class="sxs-lookup"><span data-stu-id="5f8bd-359">Definition</span></span>

<span data-ttu-id="5f8bd-360">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5f8bd-360">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5f8bd-361">La fonction `Func_sweden_eu_ssn_or_equivalent` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-361">The function  `Func_sweden_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5f8bd-362">Un mot clé à partir de `Keywords_sweden_eu_ssn_or_equivalent` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-362">A keyword from  `Keywords_sweden_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="5f8bd-363">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5f8bd-363">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5f8bd-364">La fonction `Func_sweden_eu_ssn_or_equivalent` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5f8bd-364">The function  `Func_sweden_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_sweden_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_sweden_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_sweden_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5f8bd-365">Keywords</span><span class="sxs-lookup"><span data-stu-id="5f8bd-365">Keywords</span></span>

#### <a name="keywordsswedeneussnorequivalent"></a><span data-ttu-id="5f8bd-366">Keywords_sweden_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="5f8bd-366">Keywords_sweden_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="5f8bd-367">numéro d’identification personnelle</span><span class="sxs-lookup"><span data-stu-id="5f8bd-367">personal id number</span></span>
  
<span data-ttu-id="5f8bd-368">numéro d’identification
</span><span class="sxs-lookup"><span data-stu-id="5f8bd-368">identification number</span></span>
  
<span data-ttu-id="5f8bd-369">identifiant personnel aucune</span><span class="sxs-lookup"><span data-stu-id="5f8bd-369">personal id no</span></span>
  
<span data-ttu-id="5f8bd-370">identité aucune</span><span class="sxs-lookup"><span data-stu-id="5f8bd-370">identity no</span></span>
  
<span data-ttu-id="5f8bd-371">identification aucune</span><span class="sxs-lookup"><span data-stu-id="5f8bd-371">identification no</span></span>
  
<span data-ttu-id="5f8bd-372">identification personnel aucune</span><span class="sxs-lookup"><span data-stu-id="5f8bd-372">personal identification no</span></span>
  
<span data-ttu-id="5f8bd-373">id personnummer</span><span class="sxs-lookup"><span data-stu-id="5f8bd-373">personnummer id</span></span>
  
<span data-ttu-id="5f8bd-374">id de personligt-nummer</span><span class="sxs-lookup"><span data-stu-id="5f8bd-374">personligt id-nummer</span></span>
  
<span data-ttu-id="5f8bd-375">id d’unikt-nummer</span><span class="sxs-lookup"><span data-stu-id="5f8bd-375">unikt id-nummer</span></span>
  
<span data-ttu-id="5f8bd-376">personnummer</span><span class="sxs-lookup"><span data-stu-id="5f8bd-376">personnummer</span></span>
  
<span data-ttu-id="5f8bd-377">identifikationsnumret</span><span class="sxs-lookup"><span data-stu-id="5f8bd-377">identifikationsnumret</span></span>
  
<span data-ttu-id="5f8bd-378">personnummer #</span><span class="sxs-lookup"><span data-stu-id="5f8bd-378">personnummer#</span></span>
  
<span data-ttu-id="5f8bd-379">identifikationsnumret #</span><span class="sxs-lookup"><span data-stu-id="5f8bd-379">identifikationsnumret#</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5f8bd-380">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f8bd-380">See also</span></span>

[<span data-ttu-id="5f8bd-381">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="5f8bd-381">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

