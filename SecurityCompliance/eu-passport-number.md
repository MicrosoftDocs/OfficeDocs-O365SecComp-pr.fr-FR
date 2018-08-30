---
title: Numéro de passeport UE
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/16/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 8c00df57-9fb3-459c-ba87-40480c87bd55
description: Cette rubrique illustre une stratégie de protection contre la perte données lorsqu’il détecte le type d’informations sensibles numéro de passeport l’Union européenne. Ce type d’informations sensibles définit différents motifs, mots clés et autres pour chaque pays.
ms.openlocfilehash: 71acc39b885c057e1771ec13b2f3c25017ac1bb6
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528186"
---
# <a name="eu-passport-number"></a><span data-ttu-id="abe6b-104">Numéro de passeport UE</span><span class="sxs-lookup"><span data-stu-id="abe6b-104">EU Passport Number</span></span>

<span data-ttu-id="abe6b-p102">Cette rubrique illustre une stratégie de protection contre la perte données lorsqu’il détecte le type d’informations sensibles numéro de passeport l’Union européenne. Ce type d’informations sensibles définit différents motifs, mots clés et autres pour chaque pays.</span><span class="sxs-lookup"><span data-stu-id="abe6b-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Passport Number sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="abe6b-107">Autriche</span><span class="sxs-lookup"><span data-stu-id="abe6b-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="abe6b-108">Format</span><span class="sxs-lookup"><span data-stu-id="abe6b-108">Format</span></span>

<span data-ttu-id="abe6b-109">Une lettre suivie d’un espace facultatif et sept chiffres</span><span class="sxs-lookup"><span data-stu-id="abe6b-109">One letter followed by an optional space and seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="abe6b-110">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe6b-110">Pattern</span></span>

<span data-ttu-id="abe6b-111">Une combinaison d’une lettre, sept chiffres et un espace :</span><span class="sxs-lookup"><span data-stu-id="abe6b-111">A combination of one letter, seven digits, and one space:</span></span>
  
- <span data-ttu-id="abe6b-112">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="abe6b-112">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="abe6b-113">Un espace (facultatif)</span><span class="sxs-lookup"><span data-stu-id="abe6b-113">One space (optional)</span></span>
    
- <span data-ttu-id="abe6b-114">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="abe6b-114">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="abe6b-115">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe6b-115">Checksum</span></span>

<span data-ttu-id="abe6b-116">Non applicable</span><span class="sxs-lookup"><span data-stu-id="abe6b-116">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="abe6b-117">Définition</span><span class="sxs-lookup"><span data-stu-id="abe6b-117">Definition</span></span>

<span data-ttu-id="abe6b-118">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe6b-118">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="abe6b-119">L’expression régulière `Regex_austria_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe6b-119">The regular expression  `Regex_austria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="abe6b-120">Un mot clé à partir de `Keywords_austria_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="abe6b-120">A keyword from  `Keywords_austria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_passport_number" />
          <Match idRef="Keywords_austria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe6b-121">Keywords</span><span class="sxs-lookup"><span data-stu-id="abe6b-121">Keywords</span></span>

<span data-ttu-id="abe6b-122">| |</span><span class="sxs-lookup"><span data-stu-id="abe6b-122"></span></span>
|<span data-ttu-id="abe6b-123">**Keywords_austria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="abe6b-123">**Keywords_austria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="abe6b-124">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="abe6b-124">passport number</span></span>  <br/> <span data-ttu-id="abe6b-125">numéro de passeport autrichien</span><span class="sxs-lookup"><span data-stu-id="abe6b-125">austrian passport number</span></span>  <br/> <span data-ttu-id="abe6b-126">passeport aucune</span><span class="sxs-lookup"><span data-stu-id="abe6b-126">passport no</span></span>  <br/> <span data-ttu-id="abe6b-127">reisepass</span><span class="sxs-lookup"><span data-stu-id="abe6b-127">reisepass</span></span>  <br/> <span data-ttu-id="abe6b-128">österreichisch reisepass</span><span class="sxs-lookup"><span data-stu-id="abe6b-128">österreichisch reisepass</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="abe6b-129">Belgique</span><span class="sxs-lookup"><span data-stu-id="abe6b-129">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="abe6b-130">Format</span><span class="sxs-lookup"><span data-stu-id="abe6b-130">Format</span></span>

<span data-ttu-id="abe6b-131">Deux lettres suivies de six chiffres sans espaces ni les délimiteurs</span><span class="sxs-lookup"><span data-stu-id="abe6b-131">Two letters followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="abe6b-132">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe6b-132">Pattern</span></span>

<span data-ttu-id="abe6b-133">Deux lettres et suivi de six chiffres</span><span class="sxs-lookup"><span data-stu-id="abe6b-133">Two letters and followed by six digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="abe6b-134">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe6b-134">Checksum</span></span>

<span data-ttu-id="abe6b-135">Non applicable</span><span class="sxs-lookup"><span data-stu-id="abe6b-135">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="abe6b-136">Définition</span><span class="sxs-lookup"><span data-stu-id="abe6b-136">Definition</span></span>

<span data-ttu-id="abe6b-137">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe6b-137">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="abe6b-138">L’expression régulière `Regex_belgium_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe6b-138">The regular expression  `Regex_belgium_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="abe6b-139">Un mot clé à partir de `Keywords_belgium_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="abe6b-139">A keyword from  `Keywords_belgium_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium__eu_passport_number" />
          <Match idRef="Keywords_belgium_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe6b-140">Keywords</span><span class="sxs-lookup"><span data-stu-id="abe6b-140">Keywords</span></span>

<span data-ttu-id="abe6b-141">| |</span><span class="sxs-lookup"><span data-stu-id="abe6b-141"></span></span>
|<span data-ttu-id="abe6b-142">**Keywords_belgium_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="abe6b-142">**Keywords_belgium_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="abe6b-143">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="abe6b-143">passport number</span></span>  <br/> <span data-ttu-id="abe6b-144">numéro de passeport belge</span><span class="sxs-lookup"><span data-stu-id="abe6b-144">belgian passport number</span></span>  <br/> <span data-ttu-id="abe6b-145">passeport aucune</span><span class="sxs-lookup"><span data-stu-id="abe6b-145">passport no</span></span>  <br/> <span data-ttu-id="abe6b-146">paspoort</span><span class="sxs-lookup"><span data-stu-id="abe6b-146">paspoort</span></span>  <br/> <span data-ttu-id="abe6b-147">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="abe6b-147">paspoortnummer</span></span>  <br/> <span data-ttu-id="abe6b-148">reisepass kein</span><span class="sxs-lookup"><span data-stu-id="abe6b-148">reisepass kein</span></span>  <br/> <span data-ttu-id="abe6b-149">reisepass</span><span class="sxs-lookup"><span data-stu-id="abe6b-149">reisepass</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="abe6b-150">Bulgarie</span><span class="sxs-lookup"><span data-stu-id="abe6b-150">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="abe6b-151">Format</span><span class="sxs-lookup"><span data-stu-id="abe6b-151">Format</span></span>

<span data-ttu-id="abe6b-152">Neuf chiffres sans espaces et les séparateurs</span><span class="sxs-lookup"><span data-stu-id="abe6b-152">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="abe6b-153">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe6b-153">Pattern</span></span>

 <span data-ttu-id="abe6b-154">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="abe6b-154">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="abe6b-155">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe6b-155">Checksum</span></span>

<span data-ttu-id="abe6b-156">Non</span><span class="sxs-lookup"><span data-stu-id="abe6b-156">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="abe6b-157">Définition</span><span class="sxs-lookup"><span data-stu-id="abe6b-157">Definition</span></span>

<span data-ttu-id="abe6b-158">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe6b-158">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="abe6b-159">L’expression régulière `Regex_bulgaria_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe6b-159">The regular expression  `Regex_bulgaria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="abe6b-160">Un mot clé à partir de `Keywords_bulgaria_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="abe6b-160">A keyword from  `Keywords_bulgaria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_passport_number" />
          <Match idRef="Keywords_bulgaria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe6b-161">Keywords</span><span class="sxs-lookup"><span data-stu-id="abe6b-161">Keywords</span></span>

<span data-ttu-id="abe6b-162">| |</span><span class="sxs-lookup"><span data-stu-id="abe6b-162"></span></span>
|<span data-ttu-id="abe6b-163">**Keywords_bulgaria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="abe6b-163">**Keywords_bulgaria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="abe6b-164">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="abe6b-164">passport number</span></span>  <br/> <span data-ttu-id="abe6b-165">numéro de passeport bulgare</span><span class="sxs-lookup"><span data-stu-id="abe6b-165">bulgarian passport number</span></span>  <br/> <span data-ttu-id="abe6b-166">passeport aucune</span><span class="sxs-lookup"><span data-stu-id="abe6b-166">passport no</span></span>  <br/> <span data-ttu-id="abe6b-167">НОМЕР НА ПАСПОРТА</span><span class="sxs-lookup"><span data-stu-id="abe6b-167">номер на паспорта</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="abe6b-168">Croatie</span><span class="sxs-lookup"><span data-stu-id="abe6b-168">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="abe6b-169">Format</span><span class="sxs-lookup"><span data-stu-id="abe6b-169">Format</span></span>

<span data-ttu-id="abe6b-170">Neuf chiffres sans espaces et les séparateurs</span><span class="sxs-lookup"><span data-stu-id="abe6b-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="abe6b-171">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe6b-171">Pattern</span></span>

 <span data-ttu-id="abe6b-172">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="abe6b-172">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="abe6b-173">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe6b-173">Checksum</span></span>

<span data-ttu-id="abe6b-174">Non</span><span class="sxs-lookup"><span data-stu-id="abe6b-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="abe6b-175">Définition</span><span class="sxs-lookup"><span data-stu-id="abe6b-175">Definition</span></span>

<span data-ttu-id="abe6b-176">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe6b-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="abe6b-177">L’expression régulière `Regex_croatia_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe6b-177">The regular expression  `Regex_croatia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="abe6b-178">Un mot clé à partir de `Keywords_croatia_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="abe6b-178">A keyword from  `Keywords_croatia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_passport_number" />
          <Match idRef="Keywords_croatia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe6b-179">Keywords</span><span class="sxs-lookup"><span data-stu-id="abe6b-179">Keywords</span></span>

<span data-ttu-id="abe6b-180">| |</span><span class="sxs-lookup"><span data-stu-id="abe6b-180"></span></span>
|<span data-ttu-id="abe6b-181">**Keywords_croatia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="abe6b-181">**Keywords_croatia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="abe6b-182">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="abe6b-182">passport number</span></span>  <br/> <span data-ttu-id="abe6b-183">numéro de passeport croate</span><span class="sxs-lookup"><span data-stu-id="abe6b-183">croatian passport number</span></span>  <br/> <span data-ttu-id="abe6b-184">passeport aucune</span><span class="sxs-lookup"><span data-stu-id="abe6b-184">passport no</span></span>  <br/> <span data-ttu-id="abe6b-185">broj putovnice</span><span class="sxs-lookup"><span data-stu-id="abe6b-185">broj putovnice</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="abe6b-186">Chypre</span><span class="sxs-lookup"><span data-stu-id="abe6b-186">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="abe6b-187">Format</span><span class="sxs-lookup"><span data-stu-id="abe6b-187">Format</span></span>

<span data-ttu-id="abe6b-188">Une lettre de suivi de 6 à 8 chiffres sans espaces ni les délimiteurs</span><span class="sxs-lookup"><span data-stu-id="abe6b-188">One letter followed by 6-8 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="abe6b-189">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe6b-189">Pattern</span></span>

<span data-ttu-id="abe6b-190">Une lettre de suivi de 6 à 8 chiffres</span><span class="sxs-lookup"><span data-stu-id="abe6b-190">One letter followed by six to eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="abe6b-191">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe6b-191">Checksum</span></span>

<span data-ttu-id="abe6b-192">Non</span><span class="sxs-lookup"><span data-stu-id="abe6b-192">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="abe6b-193">Définition</span><span class="sxs-lookup"><span data-stu-id="abe6b-193">Definition</span></span>

<span data-ttu-id="abe6b-194">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe6b-194">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="abe6b-195">L’expression régulière `Regex_cyprus_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe6b-195">The regular expression  `Regex_cyprus_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="abe6b-196">Un mot clé à partir de `Keywords_cyprus_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="abe6b-196">A keyword from  `Keywords_cyprus_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_passport_number" />
          <Match idRef="Keywords_cyprus_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe6b-197">Keywords</span><span class="sxs-lookup"><span data-stu-id="abe6b-197">Keywords</span></span>

<span data-ttu-id="abe6b-198">| |</span><span class="sxs-lookup"><span data-stu-id="abe6b-198"></span></span>
|<span data-ttu-id="abe6b-199">**Keywords_cyprus_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="abe6b-199">**Keywords_cyprus_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="abe6b-200">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="abe6b-200">passport number</span></span>  <br/> <span data-ttu-id="abe6b-201">numéro de passeport Chypre</span><span class="sxs-lookup"><span data-stu-id="abe6b-201">cyprus passport number</span></span>  <br/> <span data-ttu-id="abe6b-202">passeport aucune</span><span class="sxs-lookup"><span data-stu-id="abe6b-202">passport no</span></span>  <br/> <span data-ttu-id="abe6b-203">ΑΡΙΘΜΌ ΔΙΑΒΑΤΗΡΊΟΥ</span><span class="sxs-lookup"><span data-stu-id="abe6b-203">αριθμό διαβατηρίου</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="abe6b-204">République tchèque</span><span class="sxs-lookup"><span data-stu-id="abe6b-204">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="abe6b-205">Format</span><span class="sxs-lookup"><span data-stu-id="abe6b-205">Format</span></span>

<span data-ttu-id="abe6b-206">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="abe6b-206">Eight digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="abe6b-207">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe6b-207">Pattern</span></span>

<span data-ttu-id="abe6b-208">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="abe6b-208">Eight digits without spaces or delimiters</span></span>
  
### <a name="checksum"></a><span data-ttu-id="abe6b-209">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe6b-209">Checksum</span></span>

<span data-ttu-id="abe6b-210">Non</span><span class="sxs-lookup"><span data-stu-id="abe6b-210">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="abe6b-211">Définition</span><span class="sxs-lookup"><span data-stu-id="abe6b-211">Definition</span></span>

<span data-ttu-id="abe6b-212">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe6b-212">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="abe6b-213">L’expression régulière `Regex_czech_republic_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe6b-213">The regular expression  `Regex_czech_republic_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="abe6b-214">Un mot clé à partir de `Keywords_czech_republic_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="abe6b-214">A keyword from  `Keywords_czech_republic_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_passport_number" />
          <Match idRef="Keywords_czech_republic_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe6b-215">Keywords</span><span class="sxs-lookup"><span data-stu-id="abe6b-215">Keywords</span></span>

<span data-ttu-id="abe6b-216">| |</span><span class="sxs-lookup"><span data-stu-id="abe6b-216"></span></span>
|<span data-ttu-id="abe6b-217">**Keywords_czech_republic_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="abe6b-217">**Keywords_czech_republic_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="abe6b-218">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="abe6b-218">passport number</span></span>  <br/> <span data-ttu-id="abe6b-219">numéro de passeport tchèque</span><span class="sxs-lookup"><span data-stu-id="abe6b-219">czech passport number</span></span>  <br/> <span data-ttu-id="abe6b-220">passeport aucune</span><span class="sxs-lookup"><span data-stu-id="abe6b-220">passport no</span></span>  <br/> <span data-ttu-id="abe6b-221">pas de cestovní</span><span class="sxs-lookup"><span data-stu-id="abe6b-221">cestovní pas</span></span>  <br/> <span data-ttu-id="abe6b-222">pas</span><span class="sxs-lookup"><span data-stu-id="abe6b-222">pas</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="abe6b-223">Danemark</span><span class="sxs-lookup"><span data-stu-id="abe6b-223">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="abe6b-224">Format</span><span class="sxs-lookup"><span data-stu-id="abe6b-224">Format</span></span>

<span data-ttu-id="abe6b-225">Neuf chiffres sans espaces et les séparateurs</span><span class="sxs-lookup"><span data-stu-id="abe6b-225">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="abe6b-226">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe6b-226">Pattern</span></span>

 <span data-ttu-id="abe6b-227">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="abe6b-227">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="abe6b-228">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe6b-228">Checksum</span></span>

<span data-ttu-id="abe6b-229">Non</span><span class="sxs-lookup"><span data-stu-id="abe6b-229">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="abe6b-230">Définition</span><span class="sxs-lookup"><span data-stu-id="abe6b-230">Definition</span></span>

<span data-ttu-id="abe6b-231">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe6b-231">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="abe6b-232">L’expression régulière `Regex_denmark_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe6b-232">The regular expression  `Regex_denmark_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="abe6b-233">Un mot clé à partir de `Keywords_denmark_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="abe6b-233">A keyword from  `Keywords_denmark_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_passport_number" />
          <Match idRef="Keywords_denmark_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe6b-234">Keywords</span><span class="sxs-lookup"><span data-stu-id="abe6b-234">Keywords</span></span>

<span data-ttu-id="abe6b-235">| |</span><span class="sxs-lookup"><span data-stu-id="abe6b-235"></span></span>
|<span data-ttu-id="abe6b-236">**Keywords_denmark_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="abe6b-236">**Keywords_denmark_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="abe6b-237">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="abe6b-237">passport number</span></span>  <br/> <span data-ttu-id="abe6b-238">numéro de passeport danois</span><span class="sxs-lookup"><span data-stu-id="abe6b-238">danish passport number</span></span>  <br/> <span data-ttu-id="abe6b-239">passeport aucune</span><span class="sxs-lookup"><span data-stu-id="abe6b-239">passport no</span></span>  <br/> <span data-ttu-id="abe6b-240">pas</span><span class="sxs-lookup"><span data-stu-id="abe6b-240">pas</span></span>  <br/> <span data-ttu-id="abe6b-241">pasnummer</span><span class="sxs-lookup"><span data-stu-id="abe6b-241">pasnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="abe6b-242">Estonie</span><span class="sxs-lookup"><span data-stu-id="abe6b-242">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="abe6b-243">Format</span><span class="sxs-lookup"><span data-stu-id="abe6b-243">Format</span></span>

<span data-ttu-id="abe6b-244">Une lettre de suivi de sept chiffres sans espaces ni les délimiteurs</span><span class="sxs-lookup"><span data-stu-id="abe6b-244">One letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="abe6b-245">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe6b-245">Pattern</span></span>

<span data-ttu-id="abe6b-246">Une lettre de suivi de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="abe6b-246">One letter followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="abe6b-247">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe6b-247">Checksum</span></span>

<span data-ttu-id="abe6b-248">Non</span><span class="sxs-lookup"><span data-stu-id="abe6b-248">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="abe6b-249">Définition</span><span class="sxs-lookup"><span data-stu-id="abe6b-249">Definition</span></span>

<span data-ttu-id="abe6b-250">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe6b-250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="abe6b-251">L’expression régulière `Regex_estonia_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe6b-251">The regular expression  `Regex_estonia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="abe6b-252">Un mot clé à partir de `Keywords_estonia_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="abe6b-252">A keyword from  `Keywords_estonia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_passport_number" />
          <Match idRef="Keywords_estonia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe6b-253">Keywords</span><span class="sxs-lookup"><span data-stu-id="abe6b-253">Keywords</span></span>

<span data-ttu-id="abe6b-254">| |</span><span class="sxs-lookup"><span data-stu-id="abe6b-254"></span></span>
|<span data-ttu-id="abe6b-255">**Keywords_estonia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="abe6b-255">**Keywords_estonia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="abe6b-256">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="abe6b-256">passport number</span></span>  <br/> <span data-ttu-id="abe6b-257">numéro de passeport estonien</span><span class="sxs-lookup"><span data-stu-id="abe6b-257">estonian passport number</span></span>  <br/> <span data-ttu-id="abe6b-258">passeport aucune</span><span class="sxs-lookup"><span data-stu-id="abe6b-258">passport no</span></span>  <br/> <span data-ttu-id="abe6b-259">eesti kodaniku passe</span><span class="sxs-lookup"><span data-stu-id="abe6b-259">eesti kodaniku pass</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="abe6b-260">Finlande</span><span class="sxs-lookup"><span data-stu-id="abe6b-260">Finland</span></span>

<span data-ttu-id="abe6b-261">Pour plus d’informations, consultez la section « Numéro de passeport Finlande » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="abe6b-261">For details, see the section "Finland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="abe6b-262">France</span><span class="sxs-lookup"><span data-stu-id="abe6b-262">France</span></span>

<span data-ttu-id="abe6b-263">Pour plus d’informations, voir la section « Numéro de passeport France » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="abe6b-263">For details, see the section "France Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="abe6b-264">Allemagne</span><span class="sxs-lookup"><span data-stu-id="abe6b-264">Germany</span></span>

<span data-ttu-id="abe6b-265">Pour plus d’informations, voir la section « Numéro de passeport Allemagne » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="abe6b-265">For details, see the section "Germany Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="abe6b-266">Grèce</span><span class="sxs-lookup"><span data-stu-id="abe6b-266">Greece</span></span>

### <a name="format"></a><span data-ttu-id="abe6b-267">Format</span><span class="sxs-lookup"><span data-stu-id="abe6b-267">Format</span></span>

<span data-ttu-id="abe6b-268">Deux lettres suivies à sept chiffres sans espaces ni les délimiteurs</span><span class="sxs-lookup"><span data-stu-id="abe6b-268">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="abe6b-269">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe6b-269">Pattern</span></span>

<span data-ttu-id="abe6b-270">Deux lettres suivies de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="abe6b-270">Two letters followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="abe6b-271">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe6b-271">Checksum</span></span>

<span data-ttu-id="abe6b-272">Non</span><span class="sxs-lookup"><span data-stu-id="abe6b-272">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="abe6b-273">Définition</span><span class="sxs-lookup"><span data-stu-id="abe6b-273">Definition</span></span>

<span data-ttu-id="abe6b-274">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe6b-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="abe6b-275">L’expression régulière `Regex_greece_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe6b-275">The regular expression  `Regex_greece_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="abe6b-276">Un mot clé à partir de `Keywords_greece_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="abe6b-276">A keyword from  `Keywords_greece_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_passport_number" />
          <Match idRef="Keywords_greece_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe6b-277">Keywords</span><span class="sxs-lookup"><span data-stu-id="abe6b-277">Keywords</span></span>

<span data-ttu-id="abe6b-278">| |</span><span class="sxs-lookup"><span data-stu-id="abe6b-278"></span></span>
|<span data-ttu-id="abe6b-279">**Keywords_greece_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="abe6b-279">**Keywords_greece_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="abe6b-280">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="abe6b-280">passport number</span></span>  <br/> <span data-ttu-id="abe6b-281">numéro de passeport grec</span><span class="sxs-lookup"><span data-stu-id="abe6b-281">greek passport number</span></span>  <br/> <span data-ttu-id="abe6b-282">passeport aucune</span><span class="sxs-lookup"><span data-stu-id="abe6b-282">passport no</span></span>  <br/> <span data-ttu-id="abe6b-283">ΔΙΑΒΑΤΗΡΙΟ</span><span class="sxs-lookup"><span data-stu-id="abe6b-283">διαβατηριο</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="abe6b-284">Hongrie</span><span class="sxs-lookup"><span data-stu-id="abe6b-284">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="abe6b-285">Format</span><span class="sxs-lookup"><span data-stu-id="abe6b-285">Format</span></span>

<span data-ttu-id="abe6b-286">Deux lettres suivies de six ou sept chiffres sans espaces ni les délimiteurs</span><span class="sxs-lookup"><span data-stu-id="abe6b-286">Two letters followed by six or seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="abe6b-287">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe6b-287">Pattern</span></span>

<span data-ttu-id="abe6b-288">Deux lettres suivies de six ou sept chiffres</span><span class="sxs-lookup"><span data-stu-id="abe6b-288">Two letters followed by six or seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="abe6b-289">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe6b-289">Checksum</span></span>

<span data-ttu-id="abe6b-290">Non</span><span class="sxs-lookup"><span data-stu-id="abe6b-290">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="abe6b-291">Définition</span><span class="sxs-lookup"><span data-stu-id="abe6b-291">Definition</span></span>

<span data-ttu-id="abe6b-292">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe6b-292">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="abe6b-293">L’expression régulière `Regex_hungary_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe6b-293">The regular expression  `Regex_hungary_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="abe6b-294">Un mot clé à partir de `Keywords_hungary_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="abe6b-294">A keyword from  `Keywords_hungary_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_passport_number" />
          <Match idRef="Keywords_hungary_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe6b-295">Keywords</span><span class="sxs-lookup"><span data-stu-id="abe6b-295">Keywords</span></span>

<span data-ttu-id="abe6b-296">| |</span><span class="sxs-lookup"><span data-stu-id="abe6b-296"></span></span>
|<span data-ttu-id="abe6b-297">**Keywords_hungary_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="abe6b-297">**Keywords_hungary_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="abe6b-298">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="abe6b-298">passport number</span></span>  <br/> <span data-ttu-id="abe6b-299">numéro de passeport hongrois</span><span class="sxs-lookup"><span data-stu-id="abe6b-299">hungarian passport number</span></span>  <br/> <span data-ttu-id="abe6b-300">passeport aucune</span><span class="sxs-lookup"><span data-stu-id="abe6b-300">passport no</span></span>  <br/> <span data-ttu-id="abe6b-301">útlevél száma</span><span class="sxs-lookup"><span data-stu-id="abe6b-301">útlevél száma</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="abe6b-302">Irlande</span><span class="sxs-lookup"><span data-stu-id="abe6b-302">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="abe6b-303">Format</span><span class="sxs-lookup"><span data-stu-id="abe6b-303">Format</span></span>

<span data-ttu-id="abe6b-304">Deux lettres ou des chiffres suivis sept chiffres sans espaces ni les délimiteurs</span><span class="sxs-lookup"><span data-stu-id="abe6b-304">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="abe6b-305">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe6b-305">Pattern</span></span>

<span data-ttu-id="abe6b-306">Deux lettres ou des chiffres suivis à sept chiffres :</span><span class="sxs-lookup"><span data-stu-id="abe6b-306">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="abe6b-307">Deux chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="abe6b-307">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="abe6b-308">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="abe6b-308">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="abe6b-309">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe6b-309">Checksum</span></span>

<span data-ttu-id="abe6b-310">Non</span><span class="sxs-lookup"><span data-stu-id="abe6b-310">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="abe6b-311">Définition</span><span class="sxs-lookup"><span data-stu-id="abe6b-311">Definition</span></span>

<span data-ttu-id="abe6b-312">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe6b-312">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="abe6b-313">L’expression régulière `Regex_ireland_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe6b-313">The regular expression  `Regex_ireland_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="abe6b-314">Un mot clé à partir de `Keywords_ireland_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="abe6b-314">A keyword from  `Keywords_ireland_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_passport_number" />
          <Match idRef="Keywords_ireland_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe6b-315">Keywords</span><span class="sxs-lookup"><span data-stu-id="abe6b-315">Keywords</span></span>

<span data-ttu-id="abe6b-316">| |</span><span class="sxs-lookup"><span data-stu-id="abe6b-316"></span></span>
|<span data-ttu-id="abe6b-317">**Keywords_ireland_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="abe6b-317">**Keywords_ireland_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="abe6b-318">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="abe6b-318">passport number</span></span>  <br/> <span data-ttu-id="abe6b-319">numéro de passeport irlandais</span><span class="sxs-lookup"><span data-stu-id="abe6b-319">irish passport number</span></span>  <br/> <span data-ttu-id="abe6b-320">passeport aucune</span><span class="sxs-lookup"><span data-stu-id="abe6b-320">passport no</span></span>  <br/> <span data-ttu-id="abe6b-321">pas</span><span class="sxs-lookup"><span data-stu-id="abe6b-321">pas</span></span>  <br/> <span data-ttu-id="abe6b-322">passeport</span><span class="sxs-lookup"><span data-stu-id="abe6b-322">passport</span></span>  <br/> <span data-ttu-id="abe6b-323">passeport</span><span class="sxs-lookup"><span data-stu-id="abe6b-323">passeport</span></span>  <br/> <span data-ttu-id="abe6b-324">numero de passeport</span><span class="sxs-lookup"><span data-stu-id="abe6b-324">passeport numero</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="abe6b-325">Italie</span><span class="sxs-lookup"><span data-stu-id="abe6b-325">Italy</span></span>

### <a name="format"></a><span data-ttu-id="abe6b-326">Format</span><span class="sxs-lookup"><span data-stu-id="abe6b-326">Format</span></span>

<span data-ttu-id="abe6b-327">Deux lettres ou des chiffres suivis sept chiffres sans espaces ni les délimiteurs</span><span class="sxs-lookup"><span data-stu-id="abe6b-327">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="abe6b-328">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe6b-328">Pattern</span></span>

<span data-ttu-id="abe6b-329">Deux lettres ou des chiffres suivis à sept chiffres :</span><span class="sxs-lookup"><span data-stu-id="abe6b-329">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="abe6b-330">Deux chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="abe6b-330">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="abe6b-331">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="abe6b-331">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="abe6b-332">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe6b-332">Checksum</span></span>

<span data-ttu-id="abe6b-333">Non applicable</span><span class="sxs-lookup"><span data-stu-id="abe6b-333">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="abe6b-334">Définition</span><span class="sxs-lookup"><span data-stu-id="abe6b-334">Definition</span></span>

<span data-ttu-id="abe6b-335">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe6b-335">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="abe6b-336">L’expression régulière `Regex_italy_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe6b-336">The regular expression  `Regex_italy_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="abe6b-337">Un mot clé à partir de `Keywords_italy_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="abe6b-337">A keyword from  `Keywords_italy_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_passport_number" />
          <Match idRef="Keywords_italy_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe6b-338">Keywords</span><span class="sxs-lookup"><span data-stu-id="abe6b-338">Keywords</span></span>

<span data-ttu-id="abe6b-339">| |</span><span class="sxs-lookup"><span data-stu-id="abe6b-339"></span></span>
|<span data-ttu-id="abe6b-340">**Keywords_italy_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="abe6b-340">**Keywords_italy_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="abe6b-341">numéro de passeport italien</span><span class="sxs-lookup"><span data-stu-id="abe6b-341">italian passport number</span></span>  <br/> <span data-ttu-id="abe6b-342">Repubblica italiana passaporto</span><span class="sxs-lookup"><span data-stu-id="abe6b-342">repubblica italiana passaporto</span></span>  <br/> <span data-ttu-id="abe6b-343">passaporto</span><span class="sxs-lookup"><span data-stu-id="abe6b-343">passaporto</span></span>  <br/> <span data-ttu-id="abe6b-344">passaporto italiana</span><span class="sxs-lookup"><span data-stu-id="abe6b-344">passaporto italiana</span></span>  <br/> <span data-ttu-id="abe6b-345">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="abe6b-345">passport number</span></span>  <br/> <span data-ttu-id="abe6b-346">Italiana passaporto numero</span><span class="sxs-lookup"><span data-stu-id="abe6b-346">italiana passaporto numero</span></span>  <br/> <span data-ttu-id="abe6b-347">numero passaporto</span><span class="sxs-lookup"><span data-stu-id="abe6b-347">passaporto numero</span></span>  <br/> <span data-ttu-id="abe6b-348">numéro passeport italien</span><span class="sxs-lookup"><span data-stu-id="abe6b-348">numéro passeport italien</span></span>  <br/> <span data-ttu-id="abe6b-349">passeport numéro</span><span class="sxs-lookup"><span data-stu-id="abe6b-349">numéro passeport</span></span>  <br/> |
   
## <a name="latvia"></a><span data-ttu-id="abe6b-350">Lettonie</span><span class="sxs-lookup"><span data-stu-id="abe6b-350">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="abe6b-351">Format</span><span class="sxs-lookup"><span data-stu-id="abe6b-351">Format</span></span>

<span data-ttu-id="abe6b-352">Deux lettres ou des chiffres suivis sept chiffres sans espaces ni les délimiteurs</span><span class="sxs-lookup"><span data-stu-id="abe6b-352">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="abe6b-353">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe6b-353">Pattern</span></span>

<span data-ttu-id="abe6b-354">Deux lettres ou des chiffres suivis à sept chiffres :</span><span class="sxs-lookup"><span data-stu-id="abe6b-354">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="abe6b-355">Deux chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="abe6b-355">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="abe6b-356">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="abe6b-356">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="abe6b-357">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe6b-357">Checksum</span></span>

<span data-ttu-id="abe6b-358">Non</span><span class="sxs-lookup"><span data-stu-id="abe6b-358">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="abe6b-359">Définition</span><span class="sxs-lookup"><span data-stu-id="abe6b-359">Definition</span></span>

<span data-ttu-id="abe6b-360">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe6b-360">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="abe6b-361">L’expression régulière `Regex_latvia_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe6b-361">The regular expression  `Regex_latvia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="abe6b-362">Un mot clé à partir de `Keywords_latvia_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="abe6b-362">A keyword from  `Keywords_latvia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_passport_number" />
          <Match idRef="Keywords_latvia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe6b-363">Keywords</span><span class="sxs-lookup"><span data-stu-id="abe6b-363">Keywords</span></span>

<span data-ttu-id="abe6b-364">| |</span><span class="sxs-lookup"><span data-stu-id="abe6b-364"></span></span>
|<span data-ttu-id="abe6b-365">**Keywords_latvia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="abe6b-365">**Keywords_latvia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="abe6b-366">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="abe6b-366">passport number</span></span>  <br/> <span data-ttu-id="abe6b-367">numéro de passeport letton</span><span class="sxs-lookup"><span data-stu-id="abe6b-367">latvian passport number</span></span>  <br/> <span data-ttu-id="abe6b-368">passeport aucune</span><span class="sxs-lookup"><span data-stu-id="abe6b-368">passport no</span></span>  <br/> <span data-ttu-id="abe6b-369">pase numurs</span><span class="sxs-lookup"><span data-stu-id="abe6b-369">pase numurs</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="abe6b-370">Lituanie</span><span class="sxs-lookup"><span data-stu-id="abe6b-370">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="abe6b-371">Format</span><span class="sxs-lookup"><span data-stu-id="abe6b-371">Format</span></span>

<span data-ttu-id="abe6b-372">Huit des chiffres ou des lettres sans espaces ni les délimiteurs</span><span class="sxs-lookup"><span data-stu-id="abe6b-372">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="abe6b-373">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe6b-373">Pattern</span></span>

<span data-ttu-id="abe6b-374">Huit des chiffres ou des lettres (non sensible à la casse)</span><span class="sxs-lookup"><span data-stu-id="abe6b-374">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="abe6b-375">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe6b-375">Checksum</span></span>

<span data-ttu-id="abe6b-376">Non applicable</span><span class="sxs-lookup"><span data-stu-id="abe6b-376">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="abe6b-377">Définition</span><span class="sxs-lookup"><span data-stu-id="abe6b-377">Definition</span></span>

<span data-ttu-id="abe6b-378">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe6b-378">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="abe6b-379">L’expression régulière `Regex_lithuania_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe6b-379">The regular expression  `Regex_lithuania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="abe6b-380">Un mot clé à partir de `Keywords_lithuania_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="abe6b-380">A keyword from  `Keywords_lithuania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_passport_number" />
          <Match idRef="Keywords_lithuania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe6b-381">Keywords</span><span class="sxs-lookup"><span data-stu-id="abe6b-381">Keywords</span></span>

<span data-ttu-id="abe6b-382">| |</span><span class="sxs-lookup"><span data-stu-id="abe6b-382"></span></span>
|<span data-ttu-id="abe6b-383">**Keywords_lithuania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="abe6b-383">**Keywords_lithuania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="abe6b-384">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="abe6b-384">passport number</span></span>  <br/> <span data-ttu-id="abe6b-385">numéro de passeport lithunian</span><span class="sxs-lookup"><span data-stu-id="abe6b-385">lithunian passport number</span></span>  <br/> <span data-ttu-id="abe6b-386">passeport aucune</span><span class="sxs-lookup"><span data-stu-id="abe6b-386">passport no</span></span>  <br/> <span data-ttu-id="abe6b-387">Paso numeris</span><span class="sxs-lookup"><span data-stu-id="abe6b-387">paso numeris</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="abe6b-388">Luxembourg</span><span class="sxs-lookup"><span data-stu-id="abe6b-388">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="abe6b-389">Format</span><span class="sxs-lookup"><span data-stu-id="abe6b-389">Format</span></span>

<span data-ttu-id="abe6b-390">Huit des chiffres ou des lettres sans espaces ni les délimiteurs</span><span class="sxs-lookup"><span data-stu-id="abe6b-390">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="abe6b-391">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe6b-391">Pattern</span></span>

<span data-ttu-id="abe6b-392">Huit des chiffres ou des lettres (non sensible à la casse)</span><span class="sxs-lookup"><span data-stu-id="abe6b-392">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="abe6b-393">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe6b-393">Checksum</span></span>

<span data-ttu-id="abe6b-394">Non</span><span class="sxs-lookup"><span data-stu-id="abe6b-394">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="abe6b-395">Définition</span><span class="sxs-lookup"><span data-stu-id="abe6b-395">Definition</span></span>

<span data-ttu-id="abe6b-396">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe6b-396">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="abe6b-397">L’expression régulière `Regex_nation_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe6b-397">The regular expression  `Regex_nation_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="abe6b-398">Un mot clé à partir de `Keywords_nation_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="abe6b-398">A keyword from  `Keywords_nation_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_nation_eu_passport_number" />
          <Match idRef="Keywords_nation_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe6b-399">Keywords</span><span class="sxs-lookup"><span data-stu-id="abe6b-399">Keywords</span></span>

<span data-ttu-id="abe6b-400">| |</span><span class="sxs-lookup"><span data-stu-id="abe6b-400"></span></span>
|<span data-ttu-id="abe6b-401">**Keywords_nation_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="abe6b-401">**Keywords_nation_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="abe6b-402">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="abe6b-402">passport number</span></span>  <br/> <span data-ttu-id="abe6b-403">numéro de passeport letton</span><span class="sxs-lookup"><span data-stu-id="abe6b-403">latvian passport number</span></span>  <br/> <span data-ttu-id="abe6b-404">passeport aucune</span><span class="sxs-lookup"><span data-stu-id="abe6b-404">passport no</span></span>  <br/> <span data-ttu-id="abe6b-405">passnummer</span><span class="sxs-lookup"><span data-stu-id="abe6b-405">passnummer</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="abe6b-406">Malte</span><span class="sxs-lookup"><span data-stu-id="abe6b-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="abe6b-407">Format</span><span class="sxs-lookup"><span data-stu-id="abe6b-407">Format</span></span>

<span data-ttu-id="abe6b-408">Sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="abe6b-408">Seven digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="abe6b-409">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe6b-409">Pattern</span></span>

 <span data-ttu-id="abe6b-410">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="abe6b-410">Seven digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="abe6b-411">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe6b-411">Checksum</span></span>

<span data-ttu-id="abe6b-412">Non</span><span class="sxs-lookup"><span data-stu-id="abe6b-412">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="abe6b-413">Définition</span><span class="sxs-lookup"><span data-stu-id="abe6b-413">Definition</span></span>

<span data-ttu-id="abe6b-414">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe6b-414">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="abe6b-415">L’expression régulière `Regex_malta_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe6b-415">The regular expression  `Regex_malta_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="abe6b-416">Un mot clé à partir de `Keywords_malta_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="abe6b-416">A keyword from  `Keywords_malta_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_passport_number" />
          <Match idRef="Keywords_malta_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe6b-417">Keywords</span><span class="sxs-lookup"><span data-stu-id="abe6b-417">Keywords</span></span>

<span data-ttu-id="abe6b-418">| |</span><span class="sxs-lookup"><span data-stu-id="abe6b-418"></span></span>
|<span data-ttu-id="abe6b-419">**Keywords_malta_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="abe6b-419">**Keywords_malta_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="abe6b-420">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="abe6b-420">passport number</span></span>  <br/> <span data-ttu-id="abe6b-421">numéro de passeport maltais</span><span class="sxs-lookup"><span data-stu-id="abe6b-421">maltese passport number</span></span>  <br/> <span data-ttu-id="abe6b-422">passeport aucune</span><span class="sxs-lookup"><span data-stu-id="abe6b-422">passport no</span></span>  <br/> <span data-ttu-id="abe6b-423">numérique un numru-passaport</span><span class="sxs-lookup"><span data-stu-id="abe6b-423">numru tal-passaport</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="abe6b-424">Pays-Bas</span><span class="sxs-lookup"><span data-stu-id="abe6b-424">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="abe6b-425">Format</span><span class="sxs-lookup"><span data-stu-id="abe6b-425">Format</span></span>

<span data-ttu-id="abe6b-426">Neuf des lettres ou des chiffres sans espaces ni les délimiteurs</span><span class="sxs-lookup"><span data-stu-id="abe6b-426">Nine letters or digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="abe6b-427">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe6b-427">Pattern</span></span>

<span data-ttu-id="abe6b-428">Neuf des lettres ou des chiffres</span><span class="sxs-lookup"><span data-stu-id="abe6b-428">Nine letters or digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="abe6b-429">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe6b-429">Checksum</span></span>

<span data-ttu-id="abe6b-430">Non applicable</span><span class="sxs-lookup"><span data-stu-id="abe6b-430">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="abe6b-431">Définition</span><span class="sxs-lookup"><span data-stu-id="abe6b-431">Definition</span></span>

<span data-ttu-id="abe6b-432">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe6b-432">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="abe6b-433">L’expression régulière `Regex_netherlands_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe6b-433">The regular expression  `Regex_netherlands_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="abe6b-434">Un mot clé à partir de `Keywords_netherlands_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="abe6b-434">A keyword from  `Keywords_netherlands_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_passport_number" />
          <Match idRef="Keywords_netherlands_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe6b-435">Keywords</span><span class="sxs-lookup"><span data-stu-id="abe6b-435">Keywords</span></span>

<span data-ttu-id="abe6b-436">| |</span><span class="sxs-lookup"><span data-stu-id="abe6b-436"></span></span>
|<span data-ttu-id="abe6b-437">**Keywords_netherlands_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="abe6b-437">**Keywords_netherlands_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="abe6b-438">numéro de passeport néerlandais</span><span class="sxs-lookup"><span data-stu-id="abe6b-438">dutch passport number</span></span>  <br/> <span data-ttu-id="abe6b-439">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="abe6b-439">passport number</span></span>  <br/> <span data-ttu-id="abe6b-440">numéro de passeport pays-bas</span><span class="sxs-lookup"><span data-stu-id="abe6b-440">netherlands passport number</span></span>  <br/> <span data-ttu-id="abe6b-441">nederlanden paspoort nummer</span><span class="sxs-lookup"><span data-stu-id="abe6b-441">nederlanden paspoort nummer</span></span>  <br/> <span data-ttu-id="abe6b-442">paspoort</span><span class="sxs-lookup"><span data-stu-id="abe6b-442">paspoort</span></span>  <br/> <span data-ttu-id="abe6b-443">nederlanden paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="abe6b-443">nederlanden paspoortnummer</span></span>  <br/> <span data-ttu-id="abe6b-444">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="abe6b-444">paspoortnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="abe6b-445">Pologne</span><span class="sxs-lookup"><span data-stu-id="abe6b-445">Poland</span></span>

<span data-ttu-id="abe6b-446">Pour plus d’informations, voir la section « Numéro de passeport Pologne » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="abe6b-446">For details, see the section "Poland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="abe6b-447">Portugal</span><span class="sxs-lookup"><span data-stu-id="abe6b-447">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="abe6b-448">Format</span><span class="sxs-lookup"><span data-stu-id="abe6b-448">Format</span></span>

<span data-ttu-id="abe6b-449">Une lettre de suivi de six chiffres sans espaces ni les délimiteurs</span><span class="sxs-lookup"><span data-stu-id="abe6b-449">One letter followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="abe6b-450">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe6b-450">Pattern</span></span>

<span data-ttu-id="abe6b-451">Une lettre de suivi de six chiffres :</span><span class="sxs-lookup"><span data-stu-id="abe6b-451">One letter followed by six digits:</span></span>
  
- <span data-ttu-id="abe6b-452">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="abe6b-452">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="abe6b-453">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="abe6b-453">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="abe6b-454">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe6b-454">Checksum</span></span>

<span data-ttu-id="abe6b-455">Non</span><span class="sxs-lookup"><span data-stu-id="abe6b-455">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="abe6b-456">Définition</span><span class="sxs-lookup"><span data-stu-id="abe6b-456">Definition</span></span>

<span data-ttu-id="abe6b-457">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe6b-457">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="abe6b-458">L’expression régulière `Regex_portugal_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe6b-458">The regular expression  `Regex_portugal_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="abe6b-459">Un mot clé à partir de `Keywords_portugal_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="abe6b-459">A keyword from  `Keywords_portugal_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_passport_number" />
          <Match idRef="Keywords_portugal_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe6b-460">Keywords</span><span class="sxs-lookup"><span data-stu-id="abe6b-460">Keywords</span></span>

<span data-ttu-id="abe6b-461">| |</span><span class="sxs-lookup"><span data-stu-id="abe6b-461"></span></span>
|<span data-ttu-id="abe6b-462">**Keywords_portugal_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="abe6b-462">**Keywords_portugal_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="abe6b-463">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="abe6b-463">passport number</span></span>  <br/> <span data-ttu-id="abe6b-464">numéro de passeport portugais</span><span class="sxs-lookup"><span data-stu-id="abe6b-464">portugese passport number</span></span>  <br/> <span data-ttu-id="abe6b-465">passeport aucune</span><span class="sxs-lookup"><span data-stu-id="abe6b-465">passport no</span></span>  <br/> <span data-ttu-id="abe6b-466">Número passaporte</span><span class="sxs-lookup"><span data-stu-id="abe6b-466">número do passaporte</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="abe6b-467">Roumanie</span><span class="sxs-lookup"><span data-stu-id="abe6b-467">Romania</span></span>

### <a name="format"></a><span data-ttu-id="abe6b-468">Format</span><span class="sxs-lookup"><span data-stu-id="abe6b-468">Format</span></span>

<span data-ttu-id="abe6b-469">Huit ou neuf chiffres sans espaces et les séparateurs</span><span class="sxs-lookup"><span data-stu-id="abe6b-469">Eight or nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="abe6b-470">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe6b-470">Pattern</span></span>

<span data-ttu-id="abe6b-471">Huit ou neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="abe6b-471">Eight or nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="abe6b-472">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe6b-472">Checksum</span></span>

<span data-ttu-id="abe6b-473">Non</span><span class="sxs-lookup"><span data-stu-id="abe6b-473">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="abe6b-474">Définition</span><span class="sxs-lookup"><span data-stu-id="abe6b-474">Definition</span></span>

<span data-ttu-id="abe6b-475">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe6b-475">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="abe6b-476">L’expression régulière `Regex_romania_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe6b-476">The regular expression  `Regex_romania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="abe6b-477">Un mot clé à partir de `Keywords_romania_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="abe6b-477">A keyword from  `Keywords_romania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_passport_number" />
          <Match idRef="Keywords_romania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe6b-478">Keywords</span><span class="sxs-lookup"><span data-stu-id="abe6b-478">Keywords</span></span>

<span data-ttu-id="abe6b-479">| |</span><span class="sxs-lookup"><span data-stu-id="abe6b-479"></span></span>
|<span data-ttu-id="abe6b-480">**Keywords_romania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="abe6b-480">**Keywords_romania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="abe6b-481">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="abe6b-481">passport number</span></span>  <br/> <span data-ttu-id="abe6b-482">numéro de passeport roumain</span><span class="sxs-lookup"><span data-stu-id="abe6b-482">romanian passport number</span></span>  <br/> <span data-ttu-id="abe6b-483">passeport aucune</span><span class="sxs-lookup"><span data-stu-id="abe6b-483">passport no</span></span>  <br/> <span data-ttu-id="abe6b-484">numărul pașaportului</span><span class="sxs-lookup"><span data-stu-id="abe6b-484">numărul pașaportului</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="abe6b-485">République de Slovaquie</span><span class="sxs-lookup"><span data-stu-id="abe6b-485">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="abe6b-486">Format</span><span class="sxs-lookup"><span data-stu-id="abe6b-486">Format</span></span>

<span data-ttu-id="abe6b-487">Un chiffre ou une lettre suivi par sept chiffres sans espaces ni les délimiteurs</span><span class="sxs-lookup"><span data-stu-id="abe6b-487">One digit or letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="abe6b-488">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe6b-488">Pattern</span></span>

<span data-ttu-id="abe6b-489">Un chiffre ou une lettre (pas sensible à la casse) suivi de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="abe6b-489">One digit or letter (not case sensitive) followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="abe6b-490">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe6b-490">Checksum</span></span>

<span data-ttu-id="abe6b-491">Non</span><span class="sxs-lookup"><span data-stu-id="abe6b-491">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="abe6b-492">Définition</span><span class="sxs-lookup"><span data-stu-id="abe6b-492">Definition</span></span>

<span data-ttu-id="abe6b-493">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe6b-493">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="abe6b-494">L’expression régulière `Regex_slovakia_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe6b-494">The regular expression  `Regex_slovakia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="abe6b-495">Un mot clé à partir de `Keywords_slovakia_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="abe6b-495">A keyword from  `Keywords_slovakia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_passport_number" />
          <Match idRef="Keywords_slovakia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe6b-496">Keywords</span><span class="sxs-lookup"><span data-stu-id="abe6b-496">Keywords</span></span>

<span data-ttu-id="abe6b-497">| |</span><span class="sxs-lookup"><span data-stu-id="abe6b-497"></span></span>
|<span data-ttu-id="abe6b-498">**Keywords_slovakia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="abe6b-498">**Keywords_slovakia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="abe6b-499">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="abe6b-499">passport number</span></span>  <br/> <span data-ttu-id="abe6b-500">numéro de passeport slovaque</span><span class="sxs-lookup"><span data-stu-id="abe6b-500">slovakian passport number</span></span>  <br/> <span data-ttu-id="abe6b-501">passeport aucune</span><span class="sxs-lookup"><span data-stu-id="abe6b-501">passport no</span></span>  <br/> <span data-ttu-id="abe6b-502">Číslo pasu</span><span class="sxs-lookup"><span data-stu-id="abe6b-502">číslo pasu</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="abe6b-503">Slovénie</span><span class="sxs-lookup"><span data-stu-id="abe6b-503">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="abe6b-504">Format</span><span class="sxs-lookup"><span data-stu-id="abe6b-504">Format</span></span>

<span data-ttu-id="abe6b-505">Deux lettres suivies à sept chiffres sans espaces ni les délimiteurs</span><span class="sxs-lookup"><span data-stu-id="abe6b-505">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="abe6b-506">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe6b-506">Pattern</span></span>

<span data-ttu-id="abe6b-507">Deux lettres suivies à sept chiffres :</span><span class="sxs-lookup"><span data-stu-id="abe6b-507">Two letters followed by seven digits:</span></span>
  
- <span data-ttu-id="abe6b-508">La lettre « P »</span><span class="sxs-lookup"><span data-stu-id="abe6b-508">The letter "P"</span></span>
    
- <span data-ttu-id="abe6b-509">Une lettre majuscule</span><span class="sxs-lookup"><span data-stu-id="abe6b-509">One uppercase letter</span></span>
    
- <span data-ttu-id="abe6b-510">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="abe6b-510">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="abe6b-511">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe6b-511">Checksum</span></span>

<span data-ttu-id="abe6b-512">Non</span><span class="sxs-lookup"><span data-stu-id="abe6b-512">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="abe6b-513">Définition</span><span class="sxs-lookup"><span data-stu-id="abe6b-513">Definition</span></span>

<span data-ttu-id="abe6b-514">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe6b-514">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="abe6b-515">L’expression régulière `Regex_slovenia_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe6b-515">The regular expression  `Regex_slovenia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="abe6b-516">Un mot clé à partir de `Keywords_slovenia_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="abe6b-516">A keyword from  `Keywords_slovenia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_passport_number" />
          <Match idRef="Keywords_slovenia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe6b-517">Keywords</span><span class="sxs-lookup"><span data-stu-id="abe6b-517">Keywords</span></span>

<span data-ttu-id="abe6b-518">| |</span><span class="sxs-lookup"><span data-stu-id="abe6b-518"></span></span>
|<span data-ttu-id="abe6b-519">**Keywords_slovenia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="abe6b-519">**Keywords_slovenia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="abe6b-520">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="abe6b-520">passport number</span></span>  <br/> <span data-ttu-id="abe6b-521">numéro de passeport slovène</span><span class="sxs-lookup"><span data-stu-id="abe6b-521">slovenian passport number</span></span>  <br/> <span data-ttu-id="abe6b-522">passeport aucune</span><span class="sxs-lookup"><span data-stu-id="abe6b-522">passport no</span></span>  <br/> <span data-ttu-id="abe6b-523">Številka potnega lista</span><span class="sxs-lookup"><span data-stu-id="abe6b-523">številka potnega lista</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="abe6b-524">Espagne</span><span class="sxs-lookup"><span data-stu-id="abe6b-524">Spain</span></span>

### <a name="format"></a><span data-ttu-id="abe6b-525">Format</span><span class="sxs-lookup"><span data-stu-id="abe6b-525">Format</span></span>

<span data-ttu-id="abe6b-526">Une combinaison de huit ou neuf caractères de lettres et chiffres sans espaces ni les délimiteurs</span><span class="sxs-lookup"><span data-stu-id="abe6b-526">An eight- or nine-character combination of letters and numbers with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="abe6b-527">Modèle</span><span class="sxs-lookup"><span data-stu-id="abe6b-527">Pattern</span></span>

<span data-ttu-id="abe6b-528">Une combinaison de huit ou neuf caractères de lettres et chiffres :</span><span class="sxs-lookup"><span data-stu-id="abe6b-528">An eight- or nine-character combination of letters and numbers:</span></span>
  
-  <span data-ttu-id="abe6b-529">Deux chiffres ou des lettres</span><span class="sxs-lookup"><span data-stu-id="abe6b-529">Two digits or letters</span></span> 
    
- <span data-ttu-id="abe6b-530">Un chiffre ou une lettre (facultatif)</span><span class="sxs-lookup"><span data-stu-id="abe6b-530">One digit or letter (optional)</span></span>
    
- <span data-ttu-id="abe6b-531">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="abe6b-531">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="abe6b-532">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="abe6b-532">Checksum</span></span>

<span data-ttu-id="abe6b-533">Non applicable</span><span class="sxs-lookup"><span data-stu-id="abe6b-533">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="abe6b-534">Définition</span><span class="sxs-lookup"><span data-stu-id="abe6b-534">Definition</span></span>

<span data-ttu-id="abe6b-535">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="abe6b-535">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="abe6b-536">L’expression régulière `Regex_spain_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="abe6b-536">The regular expression  `Regex_spain_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="abe6b-537">Un mot clé à partir de `Keywords_spain_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="abe6b-537">A keyword from  `Keywords_spain_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_passport_number" />
          <Match idRef="Keywords_spain_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="abe6b-538">Keywords</span><span class="sxs-lookup"><span data-stu-id="abe6b-538">Keywords</span></span>

<span data-ttu-id="abe6b-539">| |</span><span class="sxs-lookup"><span data-stu-id="abe6b-539"></span></span>
|<span data-ttu-id="abe6b-540">**Keywords_spain_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="abe6b-540">**Keywords_spain_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="abe6b-541">passeport</span><span class="sxs-lookup"><span data-stu-id="abe6b-541">passport</span></span>  <br/> <span data-ttu-id="abe6b-542">passeport Espagne</span><span class="sxs-lookup"><span data-stu-id="abe6b-542">spain passport</span></span>  <br/> <span data-ttu-id="abe6b-543">livre Passport</span><span class="sxs-lookup"><span data-stu-id="abe6b-543">passport book</span></span>  <br/> <span data-ttu-id="abe6b-544">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="abe6b-544">passport number</span></span>  <br/> <span data-ttu-id="abe6b-545">passeport aucune</span><span class="sxs-lookup"><span data-stu-id="abe6b-545">passport no</span></span>  <br/> <span data-ttu-id="abe6b-546">libreta pasaporte</span><span class="sxs-lookup"><span data-stu-id="abe6b-546">libreta pasaporte</span></span>  <br/> <span data-ttu-id="abe6b-547">Número pasaporte</span><span class="sxs-lookup"><span data-stu-id="abe6b-547">número pasaporte</span></span>  <br/> <span data-ttu-id="abe6b-548">pasaporte España</span><span class="sxs-lookup"><span data-stu-id="abe6b-548">españa pasaporte</span></span>  <br/> <span data-ttu-id="abe6b-549">pasaporte</span><span class="sxs-lookup"><span data-stu-id="abe6b-549">pasaporte</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="abe6b-550">Suède</span><span class="sxs-lookup"><span data-stu-id="abe6b-550">Sweden</span></span>

<span data-ttu-id="abe6b-551">Pour plus d’informations, voir la section « Numéro de passeport Suède » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="abe6b-551">For details, see the section "Sweden Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="uk"></a><span data-ttu-id="abe6b-552">ROYAUME-UNI</span><span class="sxs-lookup"><span data-stu-id="abe6b-552">UK</span></span>

<span data-ttu-id="abe6b-p103">Pour plus d’informations, consultez la section « Numéro de passeport US / britannique » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="abe6b-p103">For details, see the section "U.S. / U.K. Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="abe6b-555">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="abe6b-555">See also</span></span>

[<span data-ttu-id="abe6b-556">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="abe6b-556">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

