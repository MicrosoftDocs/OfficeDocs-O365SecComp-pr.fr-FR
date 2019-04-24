---
title: Numéro de sécurité sociale de l'UE ou ID équivalent
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: Cette rubrique indique ce qu'est une stratégie de protection contre la perte de données (DLP) lorsqu'elle détecte le type d'informations sensibles de l'UE ou d'un ID équivalent. Ce type d'informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.
ms.openlocfilehash: c0c808eafa52209c79f3b4e8a2113f587fd8a771
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32255552"
---
# <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="b6472-104">Numéro de sécurité sociale de l'UE ou ID équivalent</span><span class="sxs-lookup"><span data-stu-id="b6472-104">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="b6472-105">Cette rubrique présente ce qu'une stratégie de protection contre la perte de données (DLP) recherche lorsqu'elle détecte le type d'informations sensibles de l'UE ou un ID équivalent.</span><span class="sxs-lookup"><span data-stu-id="b6472-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Social Security Number (SSN) or Equivalent ID sensitive information type.</span></span> <span data-ttu-id="b6472-106">Ce type d'informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.</span><span class="sxs-lookup"><span data-stu-id="b6472-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="b6472-107">Autriche</span><span class="sxs-lookup"><span data-stu-id="b6472-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="b6472-108">Format</span><span class="sxs-lookup"><span data-stu-id="b6472-108">Format</span></span>

<span data-ttu-id="b6472-109">10 chiffres au format spécifié</span><span class="sxs-lookup"><span data-stu-id="b6472-109">10 digits in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b6472-110">Modèle</span><span class="sxs-lookup"><span data-stu-id="b6472-110">Pattern</span></span>

<span data-ttu-id="b6472-111">10 chiffres :</span><span class="sxs-lookup"><span data-stu-id="b6472-111">10 digits:</span></span>
  
-  <span data-ttu-id="b6472-112">Trois chiffres correspondant à un numéro de série</span><span class="sxs-lookup"><span data-stu-id="b6472-112">Three digits that correspond to a serial number</span></span> 
    
- <span data-ttu-id="b6472-113">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="b6472-113">One check digit</span></span>
    
- <span data-ttu-id="b6472-114">Six chiffres correspondant à la date de naissance (JJMMAA)</span><span class="sxs-lookup"><span data-stu-id="b6472-114">Six digits that correspond to the birth date (DDMMYY)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b6472-115">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b6472-115">Checksum</span></span>

<span data-ttu-id="b6472-116">Oui</span><span class="sxs-lookup"><span data-stu-id="b6472-116">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b6472-117">Définition</span><span class="sxs-lookup"><span data-stu-id="b6472-117">Definition</span></span>

<span data-ttu-id="b6472-118">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b6472-118">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b6472-119">La fonction `Func_austria_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b6472-119">The function  `Func_austria_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b6472-120">Un mot clé `Keywords_austria_eu_ssn_or_equivalent` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b6472-120">A keyword from  `Keywords_austria_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="b6472-121">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b6472-121">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b6472-122">La fonction `Func_austria_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b6472-122">The function  `Func_austria_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b6472-123">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b6472-123">Keywords</span></span>

#### <a name="keywordsaustriaeussnorequivalent"></a><span data-ttu-id="b6472-124">Keywords_austria_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="b6472-124">Keywords_austria_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="b6472-125">Numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="b6472-125">social security no</span></span>
  
<span data-ttu-id="b6472-126">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="b6472-126">social security number</span></span>
  
<span data-ttu-id="b6472-127">code de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="b6472-127">social security code</span></span>
  
<span data-ttu-id="b6472-128">Numéro d'assurance</span><span class="sxs-lookup"><span data-stu-id="b6472-128">insurance number</span></span>
  
<span data-ttu-id="b6472-129">Numéro de sécurité sociale autrichien</span><span class="sxs-lookup"><span data-stu-id="b6472-129">austrian ssn</span></span>
  
<span data-ttu-id="b6472-130">SSN</span><span class="sxs-lookup"><span data-stu-id="b6472-130">ssn#</span></span>
  
<span data-ttu-id="b6472-131">SSN</span><span class="sxs-lookup"><span data-stu-id="b6472-131">ssn</span></span>
  
<span data-ttu-id="b6472-132">code d'assurance</span><span class="sxs-lookup"><span data-stu-id="b6472-132">insurance code</span></span>
  
<span data-ttu-id="b6472-133">n ° de code d'assurance</span><span class="sxs-lookup"><span data-stu-id="b6472-133">insurance code#</span></span>
  
<span data-ttu-id="b6472-134">socialsecurityno #</span><span class="sxs-lookup"><span data-stu-id="b6472-134">socialsecurityno#</span></span>
  
<span data-ttu-id="b6472-135">sozialversicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="b6472-135">sozialversicherungsnummer</span></span>
  
<span data-ttu-id="b6472-136">soziale Sicherheit kein</span><span class="sxs-lookup"><span data-stu-id="b6472-136">soziale sicherheit kein</span></span>
  
<span data-ttu-id="b6472-137">versicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="b6472-137">versicherungsnummer</span></span>
  
## <a name="belgium"></a><span data-ttu-id="b6472-138">Belgique</span><span class="sxs-lookup"><span data-stu-id="b6472-138">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="b6472-139">Format</span><span class="sxs-lookup"><span data-stu-id="b6472-139">Format</span></span>

<span data-ttu-id="b6472-140">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="b6472-140">11 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b6472-141">Modèle</span><span class="sxs-lookup"><span data-stu-id="b6472-141">Pattern</span></span>

<span data-ttu-id="b6472-142">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="b6472-142">11 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="b6472-143">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b6472-143">Checksum</span></span>

<span data-ttu-id="b6472-144">Oui</span><span class="sxs-lookup"><span data-stu-id="b6472-144">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b6472-145">Définition</span><span class="sxs-lookup"><span data-stu-id="b6472-145">Definition</span></span>

<span data-ttu-id="b6472-146">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b6472-146">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b6472-147">La fonction `Func_belgium_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b6472-147">The function  `Func_belgium_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b6472-148">Un mot clé `Keywords_belgium_eu_ssn_or_equivalent` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b6472-148">A keyword from  `Keywords_belgium_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="b6472-149">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b6472-149">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b6472-150">La fonction `Func_belgium_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b6472-150">The function  `Func_belgium_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b6472-151">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b6472-151">Keywords</span></span>

#### <a name="keywordsbelgiumeussnorequivalent"></a><span data-ttu-id="b6472-152">Keywords_belgium_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="b6472-152">Keywords_belgium_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="b6472-153">numéro national belge</span><span class="sxs-lookup"><span data-stu-id="b6472-153">belgian national number</span></span>
  
<span data-ttu-id="b6472-154">numéro national</span><span class="sxs-lookup"><span data-stu-id="b6472-154">national number</span></span>
  
<span data-ttu-id="b6472-155">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="b6472-155">social security number</span></span>
  
<span data-ttu-id="b6472-156">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="b6472-156">nationalnumber#</span></span>
  
<span data-ttu-id="b6472-157">SSN</span><span class="sxs-lookup"><span data-stu-id="b6472-157">ssn#</span></span>
  
<span data-ttu-id="b6472-158">SSN</span><span class="sxs-lookup"><span data-stu-id="b6472-158">ssn</span></span>
  
<span data-ttu-id="b6472-159">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="b6472-159">nationalnumber</span></span>
  
<span data-ttu-id="b6472-160">BNN #</span><span class="sxs-lookup"><span data-stu-id="b6472-160">bnn#</span></span>
  
<span data-ttu-id="b6472-161">BNN</span><span class="sxs-lookup"><span data-stu-id="b6472-161">bnn</span></span>
  
<span data-ttu-id="b6472-162">Numéro d'identification personnel</span><span class="sxs-lookup"><span data-stu-id="b6472-162">personal id number</span></span>
  
<span data-ttu-id="b6472-163">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="b6472-163">personalidnumber#</span></span>
  
<span data-ttu-id="b6472-164">numéro national</span><span class="sxs-lookup"><span data-stu-id="b6472-164">numéro national</span></span>
  
<span data-ttu-id="b6472-165">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="b6472-165">numéro de sécurité</span></span>
  
<span data-ttu-id="b6472-166">numéro d'assuré</span><span class="sxs-lookup"><span data-stu-id="b6472-166">numéro d'assuré</span></span>
  
<span data-ttu-id="b6472-167">identifiant national</span><span class="sxs-lookup"><span data-stu-id="b6472-167">identifiant national</span></span>
  
<span data-ttu-id="b6472-168">identifiantnational #</span><span class="sxs-lookup"><span data-stu-id="b6472-168">identifiantnational#</span></span>
  
<span data-ttu-id="b6472-169">numéronational #</span><span class="sxs-lookup"><span data-stu-id="b6472-169">numéronational#</span></span>
  
## <a name="croatia"></a><span data-ttu-id="b6472-170">Croatie</span><span class="sxs-lookup"><span data-stu-id="b6472-170">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="b6472-171">Format</span><span class="sxs-lookup"><span data-stu-id="b6472-171">Format</span></span>

<span data-ttu-id="b6472-172">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="b6472-172">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b6472-173">Modèle</span><span class="sxs-lookup"><span data-stu-id="b6472-173">Pattern</span></span>

 <span data-ttu-id="b6472-174">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="b6472-174">11 digits:</span></span> 
  
-  <span data-ttu-id="b6472-175">Dix chiffres</span><span class="sxs-lookup"><span data-stu-id="b6472-175">Ten digits</span></span> 
    
- <span data-ttu-id="b6472-176">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="b6472-176">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b6472-177">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b6472-177">Checksum</span></span>

<span data-ttu-id="b6472-178">Oui</span><span class="sxs-lookup"><span data-stu-id="b6472-178">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b6472-179">Définition</span><span class="sxs-lookup"><span data-stu-id="b6472-179">Definition</span></span>

<span data-ttu-id="b6472-180">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b6472-180">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b6472-181">La fonction `Func_croatia_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b6472-181">The function  `Func_croatia_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b6472-182">Un mot clé `Keywords_croatia_eu_ssn_or_equivalent` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b6472-182">A keyword from  `Keywords_croatia_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="b6472-183">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b6472-183">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b6472-184">La fonction `Func_croatia_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b6472-184">The function  `Func_croatia_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b6472-185">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b6472-185">Keywords</span></span>

#### <a name="keywordscroatiaeussnorequivalent"></a><span data-ttu-id="b6472-186">Keywords_croatia_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="b6472-186">Keywords_croatia_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="b6472-187">Numéro d'identification personnel</span><span class="sxs-lookup"><span data-stu-id="b6472-187">personal identification number</span></span>
  
<span data-ttu-id="b6472-188">Numéro de citoyen principal</span><span class="sxs-lookup"><span data-stu-id="b6472-188">master citizen number</span></span>
  
<span data-ttu-id="b6472-189">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="b6472-189">national identification number</span></span>
  
<span data-ttu-id="b6472-190">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="b6472-190">social security number</span></span>
  
<span data-ttu-id="b6472-191">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="b6472-191">nationalnumber#</span></span>
  
<span data-ttu-id="b6472-192">SSN</span><span class="sxs-lookup"><span data-stu-id="b6472-192">ssn#</span></span>
  
<span data-ttu-id="b6472-193">SSN</span><span class="sxs-lookup"><span data-stu-id="b6472-193">ssn</span></span>
  
<span data-ttu-id="b6472-194">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="b6472-194">nationalnumber</span></span>
  
<span data-ttu-id="b6472-195">BNN #</span><span class="sxs-lookup"><span data-stu-id="b6472-195">bnn#</span></span>
  
<span data-ttu-id="b6472-196">BNN</span><span class="sxs-lookup"><span data-stu-id="b6472-196">bnn</span></span>
  
<span data-ttu-id="b6472-197">Numéro d'identification personnel</span><span class="sxs-lookup"><span data-stu-id="b6472-197">personal id number</span></span>
  
<span data-ttu-id="b6472-198">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="b6472-198">personalidnumber#</span></span>
  
<span data-ttu-id="b6472-199">OIB</span><span class="sxs-lookup"><span data-stu-id="b6472-199">oib</span></span>
  
<span data-ttu-id="b6472-200">osobni identifikacijski Broj</span><span class="sxs-lookup"><span data-stu-id="b6472-200">osobni identifikacijski broj</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="b6472-201">République tchèque</span><span class="sxs-lookup"><span data-stu-id="b6472-201">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="b6472-202">Format</span><span class="sxs-lookup"><span data-stu-id="b6472-202">Format</span></span>

<span data-ttu-id="b6472-203">10 chiffres et une barre oblique inverse dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="b6472-203">Ten digits and a backslash in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b6472-204">Modèle</span><span class="sxs-lookup"><span data-stu-id="b6472-204">Pattern</span></span>

<span data-ttu-id="b6472-205">Dix chiffres et une barre oblique inverse:</span><span class="sxs-lookup"><span data-stu-id="b6472-205">Ten digits and a backslash:</span></span>
  
- <span data-ttu-id="b6472-206">Six chiffres correspondant à la date de naissance (AAMMJJ):</span><span class="sxs-lookup"><span data-stu-id="b6472-206">Six digits that correspond to the birth date (YYMMDD):</span></span> 
    
- <span data-ttu-id="b6472-207">Une barre oblique inverse</span><span class="sxs-lookup"><span data-stu-id="b6472-207">A backslash</span></span>
    
- <span data-ttu-id="b6472-208">Trois chiffres correspondant à un numéro de série qui sépare les personnes nés à la même date</span><span class="sxs-lookup"><span data-stu-id="b6472-208">Three digits that correspond to a serial number that separates persons born on the same date</span></span>
    
- <span data-ttu-id="b6472-209">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="b6472-209">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b6472-210">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b6472-210">Checksum</span></span>

<span data-ttu-id="b6472-211">Oui</span><span class="sxs-lookup"><span data-stu-id="b6472-211">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b6472-212">Définition</span><span class="sxs-lookup"><span data-stu-id="b6472-212">Definition</span></span>

<span data-ttu-id="b6472-213">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b6472-213">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b6472-214">La fonction `Func_czech_republic_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b6472-214">The function  `Func_czech_republic_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b6472-215">Un mot clé `Keywords_czech_republic_eu_ssn_or_equivalent` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b6472-215">A keyword from  `Keywords_czech_republic_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="b6472-216">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b6472-216">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b6472-217">La fonction `Func_czech_republic_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b6472-217">The function  `Func_czech_republic_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b6472-218">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b6472-218">Keywords</span></span>

#### <a name="keywordsczechrepubliceussnorequivalent"></a><span data-ttu-id="b6472-219">Keywords_czech_republic_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="b6472-219">Keywords_czech_republic_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="b6472-220">Numéro de naissance</span><span class="sxs-lookup"><span data-stu-id="b6472-220">birth number</span></span>
  
<span data-ttu-id="b6472-221">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="b6472-221">national identification number</span></span>
  
<span data-ttu-id="b6472-222">Numéro d'identification personnel</span><span class="sxs-lookup"><span data-stu-id="b6472-222">personal identification number</span></span>
  
<span data-ttu-id="b6472-223">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="b6472-223">social security number</span></span>
  
<span data-ttu-id="b6472-224">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="b6472-224">nationalnumber#</span></span>
  
<span data-ttu-id="b6472-225">SSN</span><span class="sxs-lookup"><span data-stu-id="b6472-225">ssn#</span></span>
  
<span data-ttu-id="b6472-226">SSN</span><span class="sxs-lookup"><span data-stu-id="b6472-226">ssn</span></span>
  
<span data-ttu-id="b6472-227">numéro national</span><span class="sxs-lookup"><span data-stu-id="b6472-227">national number</span></span>
  
<span data-ttu-id="b6472-228">Numéro d'identification personnel</span><span class="sxs-lookup"><span data-stu-id="b6472-228">personal id number</span></span>
  
<span data-ttu-id="b6472-229">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="b6472-229">personalidnumber#</span></span>
  
<span data-ttu-id="b6472-230">rč</span><span class="sxs-lookup"><span data-stu-id="b6472-230">rč</span></span>
  
<span data-ttu-id="b6472-231">rodné číslo</span><span class="sxs-lookup"><span data-stu-id="b6472-231">rodné číslo</span></span>
  
<span data-ttu-id="b6472-232">Rodne Cislo</span><span class="sxs-lookup"><span data-stu-id="b6472-232">rodne cislo</span></span>
  
## <a name="denmark"></a><span data-ttu-id="b6472-233">Danemark</span><span class="sxs-lookup"><span data-stu-id="b6472-233">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="b6472-234">Format</span><span class="sxs-lookup"><span data-stu-id="b6472-234">Format</span></span>

<span data-ttu-id="b6472-235">10 chiffres et un trait d'Union dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="b6472-235">Ten digits and a hyphen in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b6472-236">Modèle</span><span class="sxs-lookup"><span data-stu-id="b6472-236">Pattern</span></span>

<span data-ttu-id="b6472-237">Dix chiffres et un trait d'Union:</span><span class="sxs-lookup"><span data-stu-id="b6472-237">Ten digits and a hyphen:</span></span>
  
- <span data-ttu-id="b6472-238">Six chiffres correspondant à la date de naissance (JJMMAA)</span><span class="sxs-lookup"><span data-stu-id="b6472-238">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="b6472-239">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="b6472-239">A hyphen</span></span>
    
- <span data-ttu-id="b6472-240">Quatre chiffres correspondant à un numéro de séquence</span><span class="sxs-lookup"><span data-stu-id="b6472-240">Four digits that correspond to a sequence number</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b6472-241">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b6472-241">Checksum</span></span>

<span data-ttu-id="b6472-242">Oui</span><span class="sxs-lookup"><span data-stu-id="b6472-242">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b6472-243">Définition</span><span class="sxs-lookup"><span data-stu-id="b6472-243">Definition</span></span>

<span data-ttu-id="b6472-244">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b6472-244">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b6472-245">La fonction `Func_denmark_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b6472-245">The function  `Func_denmark_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b6472-246">Un mot clé `Keywords_denmark_eu_ssn_or_equivalent` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b6472-246">A keyword from  `Keywords_denmark_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="b6472-247">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b6472-247">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b6472-248">La fonction `Func_denmark_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b6472-248">The function  `Func_denmark_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b6472-249">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b6472-249">Keywords</span></span>

#### <a name="keywordsdenmarkeussnorequivalent"></a><span data-ttu-id="b6472-250">Keywords_denmark_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="b6472-250">Keywords_denmark_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="b6472-251">Numéro d'identification personnel</span><span class="sxs-lookup"><span data-stu-id="b6472-251">personal identification number</span></span>
  
<span data-ttu-id="b6472-252">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="b6472-252">national identification number</span></span>
  
<span data-ttu-id="b6472-253">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="b6472-253">social security number</span></span>
  
<span data-ttu-id="b6472-254">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="b6472-254">nationalnumber#</span></span>
  
<span data-ttu-id="b6472-255">SSN</span><span class="sxs-lookup"><span data-stu-id="b6472-255">ssn#</span></span>
  
<span data-ttu-id="b6472-256">SSN</span><span class="sxs-lookup"><span data-stu-id="b6472-256">ssn</span></span>
  
<span data-ttu-id="b6472-257">numéro national</span><span class="sxs-lookup"><span data-stu-id="b6472-257">national number</span></span>
  
<span data-ttu-id="b6472-258">Numéro d'identification personnel</span><span class="sxs-lookup"><span data-stu-id="b6472-258">personal id number</span></span>
  
<span data-ttu-id="b6472-259">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="b6472-259">personalidnumber#</span></span>
  
<span data-ttu-id="b6472-260">CPR-nummer</span><span class="sxs-lookup"><span data-stu-id="b6472-260">cpr-nummer</span></span>
  
<span data-ttu-id="b6472-261">personnummer</span><span class="sxs-lookup"><span data-stu-id="b6472-261">personnummer</span></span>
  
## <a name="finland"></a><span data-ttu-id="b6472-262">Finlande</span><span class="sxs-lookup"><span data-stu-id="b6472-262">Finland</span></span>

### <a name="format"></a><span data-ttu-id="b6472-263">Format</span><span class="sxs-lookup"><span data-stu-id="b6472-263">Format</span></span>

<span data-ttu-id="b6472-264">Combinaison de 11 caractères au format spécifié</span><span class="sxs-lookup"><span data-stu-id="b6472-264">An 11-character combination in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b6472-265">Modèle</span><span class="sxs-lookup"><span data-stu-id="b6472-265">Pattern</span></span>

<span data-ttu-id="b6472-266">Combinaison de 11 caractères au format spécifié:</span><span class="sxs-lookup"><span data-stu-id="b6472-266">An 11-character combination in the specified format:</span></span>
  
-  <span data-ttu-id="b6472-267">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="b6472-267">Six digits</span></span> 
    
- <span data-ttu-id="b6472-268">Une instance de l'un des éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="b6472-268">One instance of one of the following:</span></span>
    
  - <span data-ttu-id="b6472-269">Symbole plus</span><span class="sxs-lookup"><span data-stu-id="b6472-269">Plus symbol</span></span>
    
  - <span data-ttu-id="b6472-270">Symbole moins</span><span class="sxs-lookup"><span data-stu-id="b6472-270">Minus symbol</span></span>
    
  - <span data-ttu-id="b6472-271">La lettre «A» (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="b6472-271">The letter "A" (not case-sensitive)</span></span>
    
- <span data-ttu-id="b6472-272">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="b6472-272">Three digits</span></span>
    
- <span data-ttu-id="b6472-273">Une lettre ou un chiffre</span><span class="sxs-lookup"><span data-stu-id="b6472-273">One letter or one digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b6472-274">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b6472-274">Checksum</span></span>

<span data-ttu-id="b6472-275">Oui</span><span class="sxs-lookup"><span data-stu-id="b6472-275">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b6472-276">Définition</span><span class="sxs-lookup"><span data-stu-id="b6472-276">Definition</span></span>

<span data-ttu-id="b6472-277">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b6472-277">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b6472-278">La fonction `Func_finland_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b6472-278">The function  `Func_finland_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b6472-279">Un mot clé `Keywords_finland_eu_ssn_or_equivalent` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b6472-279">A keyword from  `Keywords_finland_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="b6472-280">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b6472-280">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b6472-281">La fonction `Func_finland_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b6472-281">The function  `Func_finland_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b6472-282">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b6472-282">Keywords</span></span>

#### <a name="keywordsfinlandeussnorequivalent"></a><span data-ttu-id="b6472-283">Keywords_finland_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="b6472-283">Keywords_finland_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="b6472-284">numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="b6472-284">identification number</span></span>
  
<span data-ttu-id="b6472-285">ID personnel</span><span class="sxs-lookup"><span data-stu-id="b6472-285">personal id</span></span>
  
<span data-ttu-id="b6472-286">Numéro d'identité</span><span class="sxs-lookup"><span data-stu-id="b6472-286">identity number</span></span>
  
<span data-ttu-id="b6472-287">Numéro d'identification national finnois</span><span class="sxs-lookup"><span data-stu-id="b6472-287">finnish national id number</span></span>
  
<span data-ttu-id="b6472-288">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="b6472-288">personalidnumber#</span></span>
  
<span data-ttu-id="b6472-289">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="b6472-289">national identification number</span></span>
  
<span data-ttu-id="b6472-290">Numéro d'identification</span><span class="sxs-lookup"><span data-stu-id="b6472-290">id number</span></span>
  
<span data-ttu-id="b6472-291">Numéro d'identification nationale</span><span class="sxs-lookup"><span data-stu-id="b6472-291">national id no.</span></span>
  
<span data-ttu-id="b6472-292">Numéro d'identification national</span><span class="sxs-lookup"><span data-stu-id="b6472-292">national id number</span></span>
  
<span data-ttu-id="b6472-293">n ° ID</span><span class="sxs-lookup"><span data-stu-id="b6472-293">id no</span></span>
  
<span data-ttu-id="b6472-294">tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="b6472-294">tunnistenumero</span></span>
  
<span data-ttu-id="b6472-295">henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="b6472-295">henkilötunnus</span></span>
  
<span data-ttu-id="b6472-296">Yksilöllinen henkilökohtainen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="b6472-296">yksilöllinen henkilökohtainen tunnistenumero</span></span>
  
<span data-ttu-id="b6472-297">ainutlaatuinen henkilökohtainen tunnus</span><span class="sxs-lookup"><span data-stu-id="b6472-297">ainutlaatuinen henkilökohtainen tunnus</span></span>
  
<span data-ttu-id="b6472-298">identiteetti numérique</span><span class="sxs-lookup"><span data-stu-id="b6472-298">identiteetti numero</span></span>
  
<span data-ttu-id="b6472-299">Suomen Kansallinen henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="b6472-299">suomen kansallinen henkilötunnus</span></span>
  
<span data-ttu-id="b6472-300">henkilötunnusnumero #</span><span class="sxs-lookup"><span data-stu-id="b6472-300">henkilötunnusnumero#</span></span>
  
<span data-ttu-id="b6472-301">Kansallisen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="b6472-301">kansallisen tunnistenumero</span></span>
  
<span data-ttu-id="b6472-302">tunnusnumero</span><span class="sxs-lookup"><span data-stu-id="b6472-302">tunnusnumero</span></span>
  
<span data-ttu-id="b6472-303">Kansallinen tunnus numérique</span><span class="sxs-lookup"><span data-stu-id="b6472-303">kansallinen tunnus numero</span></span>
  
<span data-ttu-id="b6472-304">Hetu</span><span class="sxs-lookup"><span data-stu-id="b6472-304">hetu</span></span>
  
## <a name="france"></a><span data-ttu-id="b6472-305">France</span><span class="sxs-lookup"><span data-stu-id="b6472-305">France</span></span>

<span data-ttu-id="b6472-306">Pour plus d'informations, reportez-vous à la section «France-numéro de sécurité sociale (INSEE)» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="b6472-306">For details, see the section "France Social Security Number (INSEE)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="b6472-307">Allemagne</span><span class="sxs-lookup"><span data-stu-id="b6472-307">Germany</span></span>

<span data-ttu-id="b6472-308">Pour plus d'informations, reportez-vous à la section «Germany Identity Card Number» dans les [types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="b6472-308">For details, see the section "Germany Identity Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="b6472-309">Grèce</span><span class="sxs-lookup"><span data-stu-id="b6472-309">Greece</span></span>

<span data-ttu-id="b6472-310">Pour plus d'informations, reportez-vous à la section «carte d'identité nationale Grèce» dans [ce que recherche les types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="b6472-310">For details, see the section "Greece National ID Card" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="hungary"></a><span data-ttu-id="b6472-311">Hongrie</span><span class="sxs-lookup"><span data-stu-id="b6472-311">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="b6472-312">Format</span><span class="sxs-lookup"><span data-stu-id="b6472-312">Format</span></span>

<span data-ttu-id="b6472-313">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="b6472-313">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b6472-314">Modèle</span><span class="sxs-lookup"><span data-stu-id="b6472-314">Pattern</span></span>

<span data-ttu-id="b6472-315">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="b6472-315">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="b6472-316">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b6472-316">Checksum</span></span>

<span data-ttu-id="b6472-317">Oui</span><span class="sxs-lookup"><span data-stu-id="b6472-317">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b6472-318">Définition</span><span class="sxs-lookup"><span data-stu-id="b6472-318">Definition</span></span>

<span data-ttu-id="b6472-319">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b6472-319">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b6472-320">La fonction `Func_hungary_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b6472-320">The function  `Func_hungary_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b6472-321">Un mot clé `Keywords_hungary_eu_ssn_or_equivalent` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b6472-321">A keyword from  `Keywords_hungary_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="b6472-322">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b6472-322">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b6472-323">La fonction `Func_hungary_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b6472-323">The function  `Func_hungary_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b6472-324">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b6472-324">Keywords</span></span>

#### <a name="keywordshungaryeussnorequivalent"></a><span data-ttu-id="b6472-325">Keywords_hungary_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="b6472-325">Keywords_hungary_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="b6472-326">Numéro de sécurité sociale hongrois</span><span class="sxs-lookup"><span data-stu-id="b6472-326">hungarian social security number</span></span>
  
<span data-ttu-id="b6472-327">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="b6472-327">social security number</span></span>
  
<span data-ttu-id="b6472-328">socialsecuritynumber #</span><span class="sxs-lookup"><span data-stu-id="b6472-328">socialsecuritynumber#</span></span>
  
<span data-ttu-id="b6472-329">hssn #</span><span class="sxs-lookup"><span data-stu-id="b6472-329">hssn#</span></span>
  
<span data-ttu-id="b6472-330">socialsecuritynno</span><span class="sxs-lookup"><span data-stu-id="b6472-330">socialsecuritynno</span></span>
  
<span data-ttu-id="b6472-331">hssn</span><span class="sxs-lookup"><span data-stu-id="b6472-331">hssn</span></span>
  
<span data-ttu-id="b6472-332">Taj</span><span class="sxs-lookup"><span data-stu-id="b6472-332">taj</span></span>
  
<span data-ttu-id="b6472-333">Taj #</span><span class="sxs-lookup"><span data-stu-id="b6472-333">taj#</span></span>
  
<span data-ttu-id="b6472-334">SSN</span><span class="sxs-lookup"><span data-stu-id="b6472-334">ssn</span></span>
  
<span data-ttu-id="b6472-335">SSN</span><span class="sxs-lookup"><span data-stu-id="b6472-335">ssn#</span></span>
  
<span data-ttu-id="b6472-336">Numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="b6472-336">social security no</span></span>
  
<span data-ttu-id="b6472-337">ÁFA</span><span class="sxs-lookup"><span data-stu-id="b6472-337">áfa</span></span>
  
<span data-ttu-id="b6472-338">Közösségi adószám</span><span class="sxs-lookup"><span data-stu-id="b6472-338">közösségi adószám</span></span>
  
<span data-ttu-id="b6472-339">Általános forgalmi adó szám</span><span class="sxs-lookup"><span data-stu-id="b6472-339">általános forgalmi adó szám</span></span>
  
<span data-ttu-id="b6472-340">hozzáadottérték adó</span><span class="sxs-lookup"><span data-stu-id="b6472-340">hozzáadottérték adó</span></span>
  
<span data-ttu-id="b6472-341">ÁFA szám</span><span class="sxs-lookup"><span data-stu-id="b6472-341">áfa szám</span></span>
  
<span data-ttu-id="b6472-342">Magyar ÁFA szám</span><span class="sxs-lookup"><span data-stu-id="b6472-342">magyar áfa szám</span></span>
  
## <a name="portugal"></a><span data-ttu-id="b6472-343">Portugal</span><span class="sxs-lookup"><span data-stu-id="b6472-343">Portugal</span></span>

<span data-ttu-id="b6472-344">Pour plus d'informations, reportez-vous à la section «numéro de carte de citoyen Portugal» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="b6472-344">For details, see the section "Portugal Citizen Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="spain"></a><span data-ttu-id="b6472-345">Espagne</span><span class="sxs-lookup"><span data-stu-id="b6472-345">Spain</span></span>

<span data-ttu-id="b6472-346">Pour plus d'informations, reportez-vous à la section «numéro de sécurité sociale Espagne» dans les [types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="b6472-346">For details, see the section "Spain Social Security Number (SSN)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="sweden"></a><span data-ttu-id="b6472-347">Suède</span><span class="sxs-lookup"><span data-stu-id="b6472-347">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="b6472-348">Format</span><span class="sxs-lookup"><span data-stu-id="b6472-348">Format</span></span>

<span data-ttu-id="b6472-349">12 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="b6472-349">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b6472-350">Modèle</span><span class="sxs-lookup"><span data-stu-id="b6472-350">Pattern</span></span>

<span data-ttu-id="b6472-351">12 chiffres :</span><span class="sxs-lookup"><span data-stu-id="b6472-351">12 digits:</span></span>
  
-  <span data-ttu-id="b6472-352">Huit chiffres correspondant à la date de naissance (AAAAMMJJ)</span><span class="sxs-lookup"><span data-stu-id="b6472-352">Eight digits that correspond to the birth date (YYYYMMDD)</span></span> 
    
- <span data-ttu-id="b6472-353">Trois chiffres correspondant à un numéro de série où:</span><span class="sxs-lookup"><span data-stu-id="b6472-353">Three digits that correspond to a serial number where:</span></span> 
    
  - <span data-ttu-id="b6472-354">Le dernier chiffre du numéro de série indique sexe par l'affectation d'un nombre impair pour le mâle et d'un nombre pair pour femelle.</span><span class="sxs-lookup"><span data-stu-id="b6472-354">The last digit in the serial number indicates gender by the assignment of an odd number for male and an even number for female</span></span>
    
  - <span data-ttu-id="b6472-355">Jusqu'à 1990, l'affectation du numéro de série correspond au comté où le porteur du numéro est né ou (en naissance avant 1947) où il a été vivant, en fonction des enregistrements fiscaux, le 1er janvier 1947, avec un code spécial (généralement 9 comme le 7 chiffres) pour immigrants</span><span class="sxs-lookup"><span data-stu-id="b6472-355">Up to 1990, the assignment of serial number corresponded to the county where the bearer of the number was born or (if born before 1947) where he/she had been living, according to tax records, on January 1, 1947, with a special code (usually 9 as the 7th digit) for immigrants</span></span> 
    
- <span data-ttu-id="b6472-356">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="b6472-356">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b6472-357">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="b6472-357">Checksum</span></span>

<span data-ttu-id="b6472-358">Oui</span><span class="sxs-lookup"><span data-stu-id="b6472-358">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b6472-359">Définition</span><span class="sxs-lookup"><span data-stu-id="b6472-359">Definition</span></span>

<span data-ttu-id="b6472-360">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b6472-360">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b6472-361">La fonction `Func_sweden_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b6472-361">The function  `Func_sweden_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b6472-362">Un mot clé `Keywords_sweden_eu_ssn_or_equivalent` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b6472-362">A keyword from  `Keywords_sweden_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="b6472-363">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="b6472-363">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b6472-364">La fonction `Func_sweden_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b6472-364">The function  `Func_sweden_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b6472-365">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b6472-365">Keywords</span></span>

#### <a name="keywordsswedeneussnorequivalent"></a><span data-ttu-id="b6472-366">Keywords_sweden_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="b6472-366">Keywords_sweden_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="b6472-367">Numéro d'identification personnel</span><span class="sxs-lookup"><span data-stu-id="b6472-367">personal id number</span></span>
  
<span data-ttu-id="b6472-368">numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="b6472-368">identification number</span></span>
  
<span data-ttu-id="b6472-369">Numéro d'identification personnel</span><span class="sxs-lookup"><span data-stu-id="b6472-369">personal id no</span></span>
  
<span data-ttu-id="b6472-370">n ° d'identité</span><span class="sxs-lookup"><span data-stu-id="b6472-370">identity no</span></span>
  
<span data-ttu-id="b6472-371">Numéro d'identification</span><span class="sxs-lookup"><span data-stu-id="b6472-371">identification no</span></span>
  
<span data-ttu-id="b6472-372">Numéro d'identification personnel</span><span class="sxs-lookup"><span data-stu-id="b6472-372">personal identification no</span></span>
  
<span data-ttu-id="b6472-373">ID personnummer</span><span class="sxs-lookup"><span data-stu-id="b6472-373">personnummer id</span></span>
  
<span data-ttu-id="b6472-374">ID personligt-Nummer</span><span class="sxs-lookup"><span data-stu-id="b6472-374">personligt id-nummer</span></span>
  
<span data-ttu-id="b6472-375">ID unikt-Nummer</span><span class="sxs-lookup"><span data-stu-id="b6472-375">unikt id-nummer</span></span>
  
<span data-ttu-id="b6472-376">personnummer</span><span class="sxs-lookup"><span data-stu-id="b6472-376">personnummer</span></span>
  
<span data-ttu-id="b6472-377">identifikationsnumret</span><span class="sxs-lookup"><span data-stu-id="b6472-377">identifikationsnumret</span></span>
  
<span data-ttu-id="b6472-378">personnummer #</span><span class="sxs-lookup"><span data-stu-id="b6472-378">personnummer#</span></span>
  
<span data-ttu-id="b6472-379">identifikationsnumret #</span><span class="sxs-lookup"><span data-stu-id="b6472-379">identifikationsnumret#</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b6472-380">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6472-380">See also</span></span>

[<span data-ttu-id="b6472-381">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="b6472-381">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

