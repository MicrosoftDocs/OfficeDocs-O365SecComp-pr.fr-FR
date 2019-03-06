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
ms.sourcegitcommit: ed822a776d3419853453583e882f3c61ca26d4b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "30410799"
---
# <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="e8e74-104">Numéro de sécurité sociale de l'UE ou ID équivalent</span><span class="sxs-lookup"><span data-stu-id="e8e74-104">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="e8e74-105">Cette rubrique présente ce qu'une stratégie de protection contre la perte de données (DLP) recherche lorsqu'elle détecte le type d'informations sensibles de l'UE ou un ID équivalent.</span><span class="sxs-lookup"><span data-stu-id="e8e74-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Social Security Number (SSN) or Equivalent ID sensitive information type.</span></span> <span data-ttu-id="e8e74-106">Ce type d'informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.</span><span class="sxs-lookup"><span data-stu-id="e8e74-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="e8e74-107">Autriche</span><span class="sxs-lookup"><span data-stu-id="e8e74-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="e8e74-108">Format</span><span class="sxs-lookup"><span data-stu-id="e8e74-108">Format</span></span>

<span data-ttu-id="e8e74-109">10 chiffres au format spécifié</span><span class="sxs-lookup"><span data-stu-id="e8e74-109">10 digits in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e8e74-110">Modèle</span><span class="sxs-lookup"><span data-stu-id="e8e74-110">Pattern</span></span>

<span data-ttu-id="e8e74-111">10 chiffres :</span><span class="sxs-lookup"><span data-stu-id="e8e74-111">10 digits:</span></span>
  
-  <span data-ttu-id="e8e74-112">Trois chiffres correspondant à un numéro de série</span><span class="sxs-lookup"><span data-stu-id="e8e74-112">Three digits that correspond to a serial number</span></span> 
    
- <span data-ttu-id="e8e74-113">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="e8e74-113">One check digit</span></span>
    
- <span data-ttu-id="e8e74-114">Six chiffres correspondant à la date de naissance (JJMMAA)</span><span class="sxs-lookup"><span data-stu-id="e8e74-114">Six digits that correspond to the birth date (DDMMYY)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e8e74-115">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e8e74-115">Checksum</span></span>

<span data-ttu-id="e8e74-116">Oui</span><span class="sxs-lookup"><span data-stu-id="e8e74-116">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e8e74-117">Définition</span><span class="sxs-lookup"><span data-stu-id="e8e74-117">Definition</span></span>

<span data-ttu-id="e8e74-118">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e8e74-118">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e8e74-119">La fonction `Func_austria_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e8e74-119">The function  `Func_austria_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e8e74-120">Un mot clé `Keywords_austria_eu_ssn_or_equivalent` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="e8e74-120">A keyword from  `Keywords_austria_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="e8e74-121">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e8e74-121">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e8e74-122">La fonction `Func_austria_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e8e74-122">The function  `Func_austria_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e8e74-123">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="e8e74-123">Keywords</span></span>

#### <a name="keywordsaustriaeussnorequivalent"></a><span data-ttu-id="e8e74-124">Keywords_austria_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="e8e74-124">Keywords_austria_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="e8e74-125">Numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="e8e74-125">social security no</span></span>
  
<span data-ttu-id="e8e74-126">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="e8e74-126">social security number</span></span>
  
<span data-ttu-id="e8e74-127">code de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="e8e74-127">social security code</span></span>
  
<span data-ttu-id="e8e74-128">Numéro d'assurance</span><span class="sxs-lookup"><span data-stu-id="e8e74-128">insurance number</span></span>
  
<span data-ttu-id="e8e74-129">Numéro de sécurité sociale autrichien</span><span class="sxs-lookup"><span data-stu-id="e8e74-129">austrian ssn</span></span>
  
<span data-ttu-id="e8e74-130">SSN</span><span class="sxs-lookup"><span data-stu-id="e8e74-130">ssn#</span></span>
  
<span data-ttu-id="e8e74-131">SSN</span><span class="sxs-lookup"><span data-stu-id="e8e74-131">ssn</span></span>
  
<span data-ttu-id="e8e74-132">code d'assurance</span><span class="sxs-lookup"><span data-stu-id="e8e74-132">insurance code</span></span>
  
<span data-ttu-id="e8e74-133">n ° de code d'assurance</span><span class="sxs-lookup"><span data-stu-id="e8e74-133">insurance code#</span></span>
  
<span data-ttu-id="e8e74-134">socialsecurityno #</span><span class="sxs-lookup"><span data-stu-id="e8e74-134">socialsecurityno#</span></span>
  
<span data-ttu-id="e8e74-135">sozialversicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="e8e74-135">sozialversicherungsnummer</span></span>
  
<span data-ttu-id="e8e74-136">soziale Sicherheit kein</span><span class="sxs-lookup"><span data-stu-id="e8e74-136">soziale sicherheit kein</span></span>
  
<span data-ttu-id="e8e74-137">versicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="e8e74-137">versicherungsnummer</span></span>
  
## <a name="belgium"></a><span data-ttu-id="e8e74-138">Belgique</span><span class="sxs-lookup"><span data-stu-id="e8e74-138">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="e8e74-139">Format</span><span class="sxs-lookup"><span data-stu-id="e8e74-139">Format</span></span>

<span data-ttu-id="e8e74-140">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="e8e74-140">11 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e8e74-141">Modèle</span><span class="sxs-lookup"><span data-stu-id="e8e74-141">Pattern</span></span>

<span data-ttu-id="e8e74-142">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="e8e74-142">11 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="e8e74-143">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e8e74-143">Checksum</span></span>

<span data-ttu-id="e8e74-144">Oui</span><span class="sxs-lookup"><span data-stu-id="e8e74-144">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e8e74-145">Définition</span><span class="sxs-lookup"><span data-stu-id="e8e74-145">Definition</span></span>

<span data-ttu-id="e8e74-146">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e8e74-146">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e8e74-147">La fonction `Func_belgium_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e8e74-147">The function  `Func_belgium_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e8e74-148">Un mot clé `Keywords_belgium_eu_ssn_or_equivalent` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="e8e74-148">A keyword from  `Keywords_belgium_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="e8e74-149">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e8e74-149">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e8e74-150">La fonction `Func_belgium_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e8e74-150">The function  `Func_belgium_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e8e74-151">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="e8e74-151">Keywords</span></span>

#### <a name="keywordsbelgiumeussnorequivalent"></a><span data-ttu-id="e8e74-152">Keywords_belgium_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="e8e74-152">Keywords_belgium_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="e8e74-153">numéro national belge</span><span class="sxs-lookup"><span data-stu-id="e8e74-153">belgian national number</span></span>
  
<span data-ttu-id="e8e74-154">numéro national</span><span class="sxs-lookup"><span data-stu-id="e8e74-154">national number</span></span>
  
<span data-ttu-id="e8e74-155">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="e8e74-155">social security number</span></span>
  
<span data-ttu-id="e8e74-156">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="e8e74-156">nationalnumber#</span></span>
  
<span data-ttu-id="e8e74-157">SSN</span><span class="sxs-lookup"><span data-stu-id="e8e74-157">ssn#</span></span>
  
<span data-ttu-id="e8e74-158">SSN</span><span class="sxs-lookup"><span data-stu-id="e8e74-158">ssn</span></span>
  
<span data-ttu-id="e8e74-159">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="e8e74-159">nationalnumber</span></span>
  
<span data-ttu-id="e8e74-160">BNN #</span><span class="sxs-lookup"><span data-stu-id="e8e74-160">bnn#</span></span>
  
<span data-ttu-id="e8e74-161">BNN</span><span class="sxs-lookup"><span data-stu-id="e8e74-161">bnn</span></span>
  
<span data-ttu-id="e8e74-162">Numéro d'identification personnel</span><span class="sxs-lookup"><span data-stu-id="e8e74-162">personal id number</span></span>
  
<span data-ttu-id="e8e74-163">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="e8e74-163">personalidnumber#</span></span>
  
<span data-ttu-id="e8e74-164">numéro national</span><span class="sxs-lookup"><span data-stu-id="e8e74-164">numéro national</span></span>
  
<span data-ttu-id="e8e74-165">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="e8e74-165">numéro de sécurité</span></span>
  
<span data-ttu-id="e8e74-166">numéro d'assuré</span><span class="sxs-lookup"><span data-stu-id="e8e74-166">numéro d'assuré</span></span>
  
<span data-ttu-id="e8e74-167">identifiant national</span><span class="sxs-lookup"><span data-stu-id="e8e74-167">identifiant national</span></span>
  
<span data-ttu-id="e8e74-168">identifiantnational #</span><span class="sxs-lookup"><span data-stu-id="e8e74-168">identifiantnational#</span></span>
  
<span data-ttu-id="e8e74-169">numéronational #</span><span class="sxs-lookup"><span data-stu-id="e8e74-169">numéronational#</span></span>
  
## <a name="croatia"></a><span data-ttu-id="e8e74-170">Croatie</span><span class="sxs-lookup"><span data-stu-id="e8e74-170">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="e8e74-171">Format</span><span class="sxs-lookup"><span data-stu-id="e8e74-171">Format</span></span>

<span data-ttu-id="e8e74-172">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="e8e74-172">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e8e74-173">Modèle</span><span class="sxs-lookup"><span data-stu-id="e8e74-173">Pattern</span></span>

 <span data-ttu-id="e8e74-174">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="e8e74-174">11 digits:</span></span> 
  
-  <span data-ttu-id="e8e74-175">Dix chiffres</span><span class="sxs-lookup"><span data-stu-id="e8e74-175">Ten digits</span></span> 
    
- <span data-ttu-id="e8e74-176">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="e8e74-176">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e8e74-177">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e8e74-177">Checksum</span></span>

<span data-ttu-id="e8e74-178">Oui</span><span class="sxs-lookup"><span data-stu-id="e8e74-178">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e8e74-179">Définition</span><span class="sxs-lookup"><span data-stu-id="e8e74-179">Definition</span></span>

<span data-ttu-id="e8e74-180">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e8e74-180">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e8e74-181">La fonction `Func_croatia_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e8e74-181">The function  `Func_croatia_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e8e74-182">Un mot clé `Keywords_croatia_eu_ssn_or_equivalent` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="e8e74-182">A keyword from  `Keywords_croatia_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="e8e74-183">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e8e74-183">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e8e74-184">La fonction `Func_croatia_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e8e74-184">The function  `Func_croatia_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e8e74-185">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="e8e74-185">Keywords</span></span>

#### <a name="keywordscroatiaeussnorequivalent"></a><span data-ttu-id="e8e74-186">Keywords_croatia_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="e8e74-186">Keywords_croatia_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="e8e74-187">Numéro d'identification personnel</span><span class="sxs-lookup"><span data-stu-id="e8e74-187">personal identification number</span></span>
  
<span data-ttu-id="e8e74-188">Numéro de citoyen principal</span><span class="sxs-lookup"><span data-stu-id="e8e74-188">master citizen number</span></span>
  
<span data-ttu-id="e8e74-189">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="e8e74-189">national identification number</span></span>
  
<span data-ttu-id="e8e74-190">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="e8e74-190">social security number</span></span>
  
<span data-ttu-id="e8e74-191">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="e8e74-191">nationalnumber#</span></span>
  
<span data-ttu-id="e8e74-192">SSN</span><span class="sxs-lookup"><span data-stu-id="e8e74-192">ssn#</span></span>
  
<span data-ttu-id="e8e74-193">SSN</span><span class="sxs-lookup"><span data-stu-id="e8e74-193">ssn</span></span>
  
<span data-ttu-id="e8e74-194">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="e8e74-194">nationalnumber</span></span>
  
<span data-ttu-id="e8e74-195">BNN #</span><span class="sxs-lookup"><span data-stu-id="e8e74-195">bnn#</span></span>
  
<span data-ttu-id="e8e74-196">BNN</span><span class="sxs-lookup"><span data-stu-id="e8e74-196">bnn</span></span>
  
<span data-ttu-id="e8e74-197">Numéro d'identification personnel</span><span class="sxs-lookup"><span data-stu-id="e8e74-197">personal id number</span></span>
  
<span data-ttu-id="e8e74-198">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="e8e74-198">personalidnumber#</span></span>
  
<span data-ttu-id="e8e74-199">OIB</span><span class="sxs-lookup"><span data-stu-id="e8e74-199">oib</span></span>
  
<span data-ttu-id="e8e74-200">osobni identifikacijski Broj</span><span class="sxs-lookup"><span data-stu-id="e8e74-200">osobni identifikacijski broj</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="e8e74-201">République tchèque</span><span class="sxs-lookup"><span data-stu-id="e8e74-201">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="e8e74-202">Format</span><span class="sxs-lookup"><span data-stu-id="e8e74-202">Format</span></span>

<span data-ttu-id="e8e74-203">10 chiffres et une barre oblique inverse dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="e8e74-203">Ten digits and a backslash in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e8e74-204">Modèle</span><span class="sxs-lookup"><span data-stu-id="e8e74-204">Pattern</span></span>

<span data-ttu-id="e8e74-205">Dix chiffres et une barre oblique inverse:</span><span class="sxs-lookup"><span data-stu-id="e8e74-205">Ten digits and a backslash:</span></span>
  
- <span data-ttu-id="e8e74-206">Six chiffres correspondant à la date de naissance (AAMMJJ):</span><span class="sxs-lookup"><span data-stu-id="e8e74-206">Six digits that correspond to the birth date (YYMMDD):</span></span> 
    
- <span data-ttu-id="e8e74-207">Une barre oblique inverse</span><span class="sxs-lookup"><span data-stu-id="e8e74-207">A backslash</span></span>
    
- <span data-ttu-id="e8e74-208">Trois chiffres correspondant à un numéro de série qui sépare les personnes nés à la même date</span><span class="sxs-lookup"><span data-stu-id="e8e74-208">Three digits that correspond to a serial number that separates persons born on the same date</span></span>
    
- <span data-ttu-id="e8e74-209">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="e8e74-209">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e8e74-210">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e8e74-210">Checksum</span></span>

<span data-ttu-id="e8e74-211">Oui</span><span class="sxs-lookup"><span data-stu-id="e8e74-211">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e8e74-212">Définition</span><span class="sxs-lookup"><span data-stu-id="e8e74-212">Definition</span></span>

<span data-ttu-id="e8e74-213">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e8e74-213">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e8e74-214">La fonction `Func_czech_republic_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e8e74-214">The function  `Func_czech_republic_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e8e74-215">Un mot clé `Keywords_czech_republic_eu_ssn_or_equivalent` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="e8e74-215">A keyword from  `Keywords_czech_republic_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="e8e74-216">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e8e74-216">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e8e74-217">La fonction `Func_czech_republic_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e8e74-217">The function  `Func_czech_republic_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e8e74-218">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="e8e74-218">Keywords</span></span>

#### <a name="keywordsczechrepubliceussnorequivalent"></a><span data-ttu-id="e8e74-219">Keywords_czech_republic_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="e8e74-219">Keywords_czech_republic_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="e8e74-220">Numéro de naissance</span><span class="sxs-lookup"><span data-stu-id="e8e74-220">birth number</span></span>
  
<span data-ttu-id="e8e74-221">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="e8e74-221">national identification number</span></span>
  
<span data-ttu-id="e8e74-222">Numéro d'identification personnel</span><span class="sxs-lookup"><span data-stu-id="e8e74-222">personal identification number</span></span>
  
<span data-ttu-id="e8e74-223">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="e8e74-223">social security number</span></span>
  
<span data-ttu-id="e8e74-224">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="e8e74-224">nationalnumber#</span></span>
  
<span data-ttu-id="e8e74-225">SSN</span><span class="sxs-lookup"><span data-stu-id="e8e74-225">ssn#</span></span>
  
<span data-ttu-id="e8e74-226">SSN</span><span class="sxs-lookup"><span data-stu-id="e8e74-226">ssn</span></span>
  
<span data-ttu-id="e8e74-227">numéro national</span><span class="sxs-lookup"><span data-stu-id="e8e74-227">national number</span></span>
  
<span data-ttu-id="e8e74-228">Numéro d'identification personnel</span><span class="sxs-lookup"><span data-stu-id="e8e74-228">personal id number</span></span>
  
<span data-ttu-id="e8e74-229">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="e8e74-229">personalidnumber#</span></span>
  
<span data-ttu-id="e8e74-230">rč</span><span class="sxs-lookup"><span data-stu-id="e8e74-230">rč</span></span>
  
<span data-ttu-id="e8e74-231">rodné číslo</span><span class="sxs-lookup"><span data-stu-id="e8e74-231">rodné číslo</span></span>
  
<span data-ttu-id="e8e74-232">Rodne Cislo</span><span class="sxs-lookup"><span data-stu-id="e8e74-232">rodne cislo</span></span>
  
## <a name="denmark"></a><span data-ttu-id="e8e74-233">Danemark</span><span class="sxs-lookup"><span data-stu-id="e8e74-233">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="e8e74-234">Format</span><span class="sxs-lookup"><span data-stu-id="e8e74-234">Format</span></span>

<span data-ttu-id="e8e74-235">10 chiffres et un trait d'Union dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="e8e74-235">Ten digits and a hyphen in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e8e74-236">Modèle</span><span class="sxs-lookup"><span data-stu-id="e8e74-236">Pattern</span></span>

<span data-ttu-id="e8e74-237">Dix chiffres et un trait d'Union:</span><span class="sxs-lookup"><span data-stu-id="e8e74-237">Ten digits and a hyphen:</span></span>
  
- <span data-ttu-id="e8e74-238">Six chiffres correspondant à la date de naissance (JJMMAA)</span><span class="sxs-lookup"><span data-stu-id="e8e74-238">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="e8e74-239">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="e8e74-239">A hyphen</span></span>
    
- <span data-ttu-id="e8e74-240">Quatre chiffres correspondant à un numéro de séquence</span><span class="sxs-lookup"><span data-stu-id="e8e74-240">Four digits that correspond to a sequence number</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e8e74-241">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e8e74-241">Checksum</span></span>

<span data-ttu-id="e8e74-242">Oui</span><span class="sxs-lookup"><span data-stu-id="e8e74-242">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e8e74-243">Définition</span><span class="sxs-lookup"><span data-stu-id="e8e74-243">Definition</span></span>

<span data-ttu-id="e8e74-244">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e8e74-244">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e8e74-245">La fonction `Func_denmark_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e8e74-245">The function  `Func_denmark_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e8e74-246">Un mot clé `Keywords_denmark_eu_ssn_or_equivalent` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="e8e74-246">A keyword from  `Keywords_denmark_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="e8e74-247">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e8e74-247">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e8e74-248">La fonction `Func_denmark_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e8e74-248">The function  `Func_denmark_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e8e74-249">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="e8e74-249">Keywords</span></span>

#### <a name="keywordsdenmarkeussnorequivalent"></a><span data-ttu-id="e8e74-250">Keywords_denmark_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="e8e74-250">Keywords_denmark_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="e8e74-251">Numéro d'identification personnel</span><span class="sxs-lookup"><span data-stu-id="e8e74-251">personal identification number</span></span>
  
<span data-ttu-id="e8e74-252">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="e8e74-252">national identification number</span></span>
  
<span data-ttu-id="e8e74-253">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="e8e74-253">social security number</span></span>
  
<span data-ttu-id="e8e74-254">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="e8e74-254">nationalnumber#</span></span>
  
<span data-ttu-id="e8e74-255">SSN</span><span class="sxs-lookup"><span data-stu-id="e8e74-255">ssn#</span></span>
  
<span data-ttu-id="e8e74-256">SSN</span><span class="sxs-lookup"><span data-stu-id="e8e74-256">ssn</span></span>
  
<span data-ttu-id="e8e74-257">numéro national</span><span class="sxs-lookup"><span data-stu-id="e8e74-257">national number</span></span>
  
<span data-ttu-id="e8e74-258">Numéro d'identification personnel</span><span class="sxs-lookup"><span data-stu-id="e8e74-258">personal id number</span></span>
  
<span data-ttu-id="e8e74-259">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="e8e74-259">personalidnumber#</span></span>
  
<span data-ttu-id="e8e74-260">CPR-nummer</span><span class="sxs-lookup"><span data-stu-id="e8e74-260">cpr-nummer</span></span>
  
<span data-ttu-id="e8e74-261">personnummer</span><span class="sxs-lookup"><span data-stu-id="e8e74-261">personnummer</span></span>
  
## <a name="finland"></a><span data-ttu-id="e8e74-262">Finlande</span><span class="sxs-lookup"><span data-stu-id="e8e74-262">Finland</span></span>

### <a name="format"></a><span data-ttu-id="e8e74-263">Format</span><span class="sxs-lookup"><span data-stu-id="e8e74-263">Format</span></span>

<span data-ttu-id="e8e74-264">Combinaison de 11 caractères au format spécifié</span><span class="sxs-lookup"><span data-stu-id="e8e74-264">An 11-character combination in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e8e74-265">Modèle</span><span class="sxs-lookup"><span data-stu-id="e8e74-265">Pattern</span></span>

<span data-ttu-id="e8e74-266">Combinaison de 11 caractères au format spécifié:</span><span class="sxs-lookup"><span data-stu-id="e8e74-266">An 11-character combination in the specified format:</span></span>
  
-  <span data-ttu-id="e8e74-267">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="e8e74-267">Six digits</span></span> 
    
- <span data-ttu-id="e8e74-268">Une instance de l'un des éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="e8e74-268">One instance of one of the following:</span></span>
    
  - <span data-ttu-id="e8e74-269">Symbole plus</span><span class="sxs-lookup"><span data-stu-id="e8e74-269">Plus symbol</span></span>
    
  - <span data-ttu-id="e8e74-270">Symbole moins</span><span class="sxs-lookup"><span data-stu-id="e8e74-270">Minus symbol</span></span>
    
  - <span data-ttu-id="e8e74-271">La lettre «A» (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="e8e74-271">The letter "A" (not case-sensitive)</span></span>
    
- <span data-ttu-id="e8e74-272">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="e8e74-272">Three digits</span></span>
    
- <span data-ttu-id="e8e74-273">Une lettre ou un chiffre</span><span class="sxs-lookup"><span data-stu-id="e8e74-273">One letter or one digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e8e74-274">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e8e74-274">Checksum</span></span>

<span data-ttu-id="e8e74-275">Oui</span><span class="sxs-lookup"><span data-stu-id="e8e74-275">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e8e74-276">Définition</span><span class="sxs-lookup"><span data-stu-id="e8e74-276">Definition</span></span>

<span data-ttu-id="e8e74-277">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e8e74-277">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e8e74-278">La fonction `Func_finland_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e8e74-278">The function  `Func_finland_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e8e74-279">Un mot clé `Keywords_finland_eu_ssn_or_equivalent` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="e8e74-279">A keyword from  `Keywords_finland_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="e8e74-280">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e8e74-280">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e8e74-281">La fonction `Func_finland_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e8e74-281">The function  `Func_finland_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e8e74-282">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="e8e74-282">Keywords</span></span>

#### <a name="keywordsfinlandeussnorequivalent"></a><span data-ttu-id="e8e74-283">Keywords_finland_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="e8e74-283">Keywords_finland_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="e8e74-284">numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="e8e74-284">identification number</span></span>
  
<span data-ttu-id="e8e74-285">ID personnel</span><span class="sxs-lookup"><span data-stu-id="e8e74-285">personal id</span></span>
  
<span data-ttu-id="e8e74-286">Numéro d'identité</span><span class="sxs-lookup"><span data-stu-id="e8e74-286">identity number</span></span>
  
<span data-ttu-id="e8e74-287">Numéro d'identification national finnois</span><span class="sxs-lookup"><span data-stu-id="e8e74-287">finnish national id number</span></span>
  
<span data-ttu-id="e8e74-288">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="e8e74-288">personalidnumber#</span></span>
  
<span data-ttu-id="e8e74-289">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="e8e74-289">national identification number</span></span>
  
<span data-ttu-id="e8e74-290">Numéro d'identification</span><span class="sxs-lookup"><span data-stu-id="e8e74-290">id number</span></span>
  
<span data-ttu-id="e8e74-291">Numéro d'identification nationale</span><span class="sxs-lookup"><span data-stu-id="e8e74-291">national id no.</span></span>
  
<span data-ttu-id="e8e74-292">Numéro d'identification national</span><span class="sxs-lookup"><span data-stu-id="e8e74-292">national id number</span></span>
  
<span data-ttu-id="e8e74-293">n ° ID</span><span class="sxs-lookup"><span data-stu-id="e8e74-293">id no</span></span>
  
<span data-ttu-id="e8e74-294">tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="e8e74-294">tunnistenumero</span></span>
  
<span data-ttu-id="e8e74-295">henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="e8e74-295">henkilötunnus</span></span>
  
<span data-ttu-id="e8e74-296">Yksilöllinen henkilökohtainen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="e8e74-296">yksilöllinen henkilökohtainen tunnistenumero</span></span>
  
<span data-ttu-id="e8e74-297">ainutlaatuinen henkilökohtainen tunnus</span><span class="sxs-lookup"><span data-stu-id="e8e74-297">ainutlaatuinen henkilökohtainen tunnus</span></span>
  
<span data-ttu-id="e8e74-298">identiteetti numérique</span><span class="sxs-lookup"><span data-stu-id="e8e74-298">identiteetti numero</span></span>
  
<span data-ttu-id="e8e74-299">Suomen Kansallinen henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="e8e74-299">suomen kansallinen henkilötunnus</span></span>
  
<span data-ttu-id="e8e74-300">henkilötunnusnumero #</span><span class="sxs-lookup"><span data-stu-id="e8e74-300">henkilötunnusnumero#</span></span>
  
<span data-ttu-id="e8e74-301">Kansallisen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="e8e74-301">kansallisen tunnistenumero</span></span>
  
<span data-ttu-id="e8e74-302">tunnusnumero</span><span class="sxs-lookup"><span data-stu-id="e8e74-302">tunnusnumero</span></span>
  
<span data-ttu-id="e8e74-303">Kansallinen tunnus numérique</span><span class="sxs-lookup"><span data-stu-id="e8e74-303">kansallinen tunnus numero</span></span>
  
<span data-ttu-id="e8e74-304">Hetu</span><span class="sxs-lookup"><span data-stu-id="e8e74-304">hetu</span></span>
  
## <a name="france"></a><span data-ttu-id="e8e74-305">France</span><span class="sxs-lookup"><span data-stu-id="e8e74-305">France</span></span>

<span data-ttu-id="e8e74-306">Pour plus d'informations, reportez-vous à la section «France-numéro de sécurité sociale (INSEE)» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="e8e74-306">For details, see the section "France Social Security Number (INSEE)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="e8e74-307">Allemagne</span><span class="sxs-lookup"><span data-stu-id="e8e74-307">Germany</span></span>

<span data-ttu-id="e8e74-308">Pour plus d'informations, reportez-vous à la section «Germany Identity Card Number» dans les [types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="e8e74-308">For details, see the section "Germany Identity Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="e8e74-309">Grèce</span><span class="sxs-lookup"><span data-stu-id="e8e74-309">Greece</span></span>

<span data-ttu-id="e8e74-310">Pour plus d'informations, reportez-vous à la section «carte d'identité nationale Grèce» dans [ce que recherche les types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="e8e74-310">For details, see the section "Greece National ID Card" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="hungary"></a><span data-ttu-id="e8e74-311">Hongrie</span><span class="sxs-lookup"><span data-stu-id="e8e74-311">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="e8e74-312">Format</span><span class="sxs-lookup"><span data-stu-id="e8e74-312">Format</span></span>

<span data-ttu-id="e8e74-313">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="e8e74-313">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e8e74-314">Modèle</span><span class="sxs-lookup"><span data-stu-id="e8e74-314">Pattern</span></span>

<span data-ttu-id="e8e74-315">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="e8e74-315">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="e8e74-316">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e8e74-316">Checksum</span></span>

<span data-ttu-id="e8e74-317">Oui</span><span class="sxs-lookup"><span data-stu-id="e8e74-317">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e8e74-318">Définition</span><span class="sxs-lookup"><span data-stu-id="e8e74-318">Definition</span></span>

<span data-ttu-id="e8e74-319">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e8e74-319">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e8e74-320">La fonction `Func_hungary_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e8e74-320">The function  `Func_hungary_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e8e74-321">Un mot clé `Keywords_hungary_eu_ssn_or_equivalent` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="e8e74-321">A keyword from  `Keywords_hungary_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="e8e74-322">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e8e74-322">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e8e74-323">La fonction `Func_hungary_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e8e74-323">The function  `Func_hungary_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e8e74-324">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="e8e74-324">Keywords</span></span>

#### <a name="keywordshungaryeussnorequivalent"></a><span data-ttu-id="e8e74-325">Keywords_hungary_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="e8e74-325">Keywords_hungary_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="e8e74-326">Numéro de sécurité sociale hongrois</span><span class="sxs-lookup"><span data-stu-id="e8e74-326">hungarian social security number</span></span>
  
<span data-ttu-id="e8e74-327">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="e8e74-327">social security number</span></span>
  
<span data-ttu-id="e8e74-328">socialsecuritynumber #</span><span class="sxs-lookup"><span data-stu-id="e8e74-328">socialsecuritynumber#</span></span>
  
<span data-ttu-id="e8e74-329">hssn #</span><span class="sxs-lookup"><span data-stu-id="e8e74-329">hssn#</span></span>
  
<span data-ttu-id="e8e74-330">socialsecuritynno</span><span class="sxs-lookup"><span data-stu-id="e8e74-330">socialsecuritynno</span></span>
  
<span data-ttu-id="e8e74-331">hssn</span><span class="sxs-lookup"><span data-stu-id="e8e74-331">hssn</span></span>
  
<span data-ttu-id="e8e74-332">Taj</span><span class="sxs-lookup"><span data-stu-id="e8e74-332">taj</span></span>
  
<span data-ttu-id="e8e74-333">Taj #</span><span class="sxs-lookup"><span data-stu-id="e8e74-333">taj#</span></span>
  
<span data-ttu-id="e8e74-334">SSN</span><span class="sxs-lookup"><span data-stu-id="e8e74-334">ssn</span></span>
  
<span data-ttu-id="e8e74-335">SSN</span><span class="sxs-lookup"><span data-stu-id="e8e74-335">ssn#</span></span>
  
<span data-ttu-id="e8e74-336">Numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="e8e74-336">social security no</span></span>
  
<span data-ttu-id="e8e74-337">ÁFA</span><span class="sxs-lookup"><span data-stu-id="e8e74-337">áfa</span></span>
  
<span data-ttu-id="e8e74-338">Közösségi adószám</span><span class="sxs-lookup"><span data-stu-id="e8e74-338">közösségi adószám</span></span>
  
<span data-ttu-id="e8e74-339">Általános forgalmi adó szám</span><span class="sxs-lookup"><span data-stu-id="e8e74-339">általános forgalmi adó szám</span></span>
  
<span data-ttu-id="e8e74-340">hozzáadottérték adó</span><span class="sxs-lookup"><span data-stu-id="e8e74-340">hozzáadottérték adó</span></span>
  
<span data-ttu-id="e8e74-341">ÁFA szám</span><span class="sxs-lookup"><span data-stu-id="e8e74-341">áfa szám</span></span>
  
<span data-ttu-id="e8e74-342">Magyar ÁFA szám</span><span class="sxs-lookup"><span data-stu-id="e8e74-342">magyar áfa szám</span></span>
  
## <a name="portugal"></a><span data-ttu-id="e8e74-343">Portugal</span><span class="sxs-lookup"><span data-stu-id="e8e74-343">Portugal</span></span>

<span data-ttu-id="e8e74-344">Pour plus d'informations, reportez-vous à la section «numéro de carte de citoyen Portugal» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="e8e74-344">For details, see the section "Portugal Citizen Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="spain"></a><span data-ttu-id="e8e74-345">Espagne</span><span class="sxs-lookup"><span data-stu-id="e8e74-345">Spain</span></span>

<span data-ttu-id="e8e74-346">Pour plus d'informations, reportez-vous à la section «numéro de sécurité sociale Espagne» dans les [types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="e8e74-346">For details, see the section "Spain Social Security Number (SSN)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="sweden"></a><span data-ttu-id="e8e74-347">Suède</span><span class="sxs-lookup"><span data-stu-id="e8e74-347">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="e8e74-348">Format</span><span class="sxs-lookup"><span data-stu-id="e8e74-348">Format</span></span>

<span data-ttu-id="e8e74-349">12 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="e8e74-349">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e8e74-350">Modèle</span><span class="sxs-lookup"><span data-stu-id="e8e74-350">Pattern</span></span>

<span data-ttu-id="e8e74-351">12 chiffres :</span><span class="sxs-lookup"><span data-stu-id="e8e74-351">12 digits:</span></span>
  
-  <span data-ttu-id="e8e74-352">Huit chiffres correspondant à la date de naissance (AAAAMMJJ)</span><span class="sxs-lookup"><span data-stu-id="e8e74-352">Eight digits that correspond to the birth date (YYYYMMDD)</span></span> 
    
- <span data-ttu-id="e8e74-353">Trois chiffres correspondant à un numéro de série où:</span><span class="sxs-lookup"><span data-stu-id="e8e74-353">Three digits that correspond to a serial number where:</span></span> 
    
  - <span data-ttu-id="e8e74-354">Le dernier chiffre du numéro de série indique sexe par l'affectation d'un nombre impair pour le mâle et d'un nombre pair pour femelle.</span><span class="sxs-lookup"><span data-stu-id="e8e74-354">The last digit in the serial number indicates gender by the assignment of an odd number for male and an even number for female</span></span>
    
  - <span data-ttu-id="e8e74-355">Jusqu'à 1990, l'affectation du numéro de série correspond au comté où le porteur du numéro est né ou (en naissance avant 1947) où il a été vivant, en fonction des enregistrements fiscaux, le 1er janvier 1947, avec un code spécial (généralement 9 comme le 7 chiffres) pour immigrants</span><span class="sxs-lookup"><span data-stu-id="e8e74-355">Up to 1990, the assignment of serial number corresponded to the county where the bearer of the number was born or (if born before 1947) where he/she had been living, according to tax records, on January 1, 1947, with a special code (usually 9 as the 7th digit) for immigrants</span></span> 
    
- <span data-ttu-id="e8e74-356">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="e8e74-356">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e8e74-357">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e8e74-357">Checksum</span></span>

<span data-ttu-id="e8e74-358">Oui</span><span class="sxs-lookup"><span data-stu-id="e8e74-358">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e8e74-359">Définition</span><span class="sxs-lookup"><span data-stu-id="e8e74-359">Definition</span></span>

<span data-ttu-id="e8e74-360">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e8e74-360">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e8e74-361">La fonction `Func_sweden_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e8e74-361">The function  `Func_sweden_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e8e74-362">Un mot clé `Keywords_sweden_eu_ssn_or_equivalent` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="e8e74-362">A keyword from  `Keywords_sweden_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="e8e74-363">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e8e74-363">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e8e74-364">La fonction `Func_sweden_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e8e74-364">The function  `Func_sweden_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e8e74-365">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="e8e74-365">Keywords</span></span>

#### <a name="keywordsswedeneussnorequivalent"></a><span data-ttu-id="e8e74-366">Keywords_sweden_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="e8e74-366">Keywords_sweden_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="e8e74-367">Numéro d'identification personnel</span><span class="sxs-lookup"><span data-stu-id="e8e74-367">personal id number</span></span>
  
<span data-ttu-id="e8e74-368">numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="e8e74-368">identification number</span></span>
  
<span data-ttu-id="e8e74-369">Numéro d'identification personnel</span><span class="sxs-lookup"><span data-stu-id="e8e74-369">personal id no</span></span>
  
<span data-ttu-id="e8e74-370">n ° d'identité</span><span class="sxs-lookup"><span data-stu-id="e8e74-370">identity no</span></span>
  
<span data-ttu-id="e8e74-371">Numéro d'identification</span><span class="sxs-lookup"><span data-stu-id="e8e74-371">identification no</span></span>
  
<span data-ttu-id="e8e74-372">Numéro d'identification personnel</span><span class="sxs-lookup"><span data-stu-id="e8e74-372">personal identification no</span></span>
  
<span data-ttu-id="e8e74-373">ID personnummer</span><span class="sxs-lookup"><span data-stu-id="e8e74-373">personnummer id</span></span>
  
<span data-ttu-id="e8e74-374">ID personligt-Nummer</span><span class="sxs-lookup"><span data-stu-id="e8e74-374">personligt id-nummer</span></span>
  
<span data-ttu-id="e8e74-375">ID unikt-Nummer</span><span class="sxs-lookup"><span data-stu-id="e8e74-375">unikt id-nummer</span></span>
  
<span data-ttu-id="e8e74-376">personnummer</span><span class="sxs-lookup"><span data-stu-id="e8e74-376">personnummer</span></span>
  
<span data-ttu-id="e8e74-377">identifikationsnumret</span><span class="sxs-lookup"><span data-stu-id="e8e74-377">identifikationsnumret</span></span>
  
<span data-ttu-id="e8e74-378">personnummer #</span><span class="sxs-lookup"><span data-stu-id="e8e74-378">personnummer#</span></span>
  
<span data-ttu-id="e8e74-379">identifikationsnumret #</span><span class="sxs-lookup"><span data-stu-id="e8e74-379">identifikationsnumret#</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e8e74-380">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8e74-380">See also</span></span>

[<span data-ttu-id="e8e74-381">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="e8e74-381">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

