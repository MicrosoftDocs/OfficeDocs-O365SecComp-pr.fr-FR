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
ms.openlocfilehash: 7a7fc1ff826aab4096c46535686eb0fd68173c6f
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2019
ms.locfileid: "25840323"
---
# <a name="eu-passport-number"></a><span data-ttu-id="30bde-104">Numéro de passeport UE</span><span class="sxs-lookup"><span data-stu-id="30bde-104">EU Passport Number</span></span>

<span data-ttu-id="30bde-p102">Cette rubrique illustre une stratégie de protection contre la perte données lorsqu’il détecte le type d’informations sensibles numéro de passeport l’Union européenne. Ce type d’informations sensibles définit différents motifs, mots clés et autres pour chaque pays.</span><span class="sxs-lookup"><span data-stu-id="30bde-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Passport Number sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="30bde-107">Autriche</span><span class="sxs-lookup"><span data-stu-id="30bde-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="30bde-108">Format</span><span class="sxs-lookup"><span data-stu-id="30bde-108">Format</span></span>

<span data-ttu-id="30bde-109">Une lettre suivie d’un espace facultatif et sept chiffres</span><span class="sxs-lookup"><span data-stu-id="30bde-109">One letter followed by an optional space and seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="30bde-110">Modèle</span><span class="sxs-lookup"><span data-stu-id="30bde-110">Pattern</span></span>

<span data-ttu-id="30bde-111">Une combinaison d’une lettre, sept chiffres et un espace :</span><span class="sxs-lookup"><span data-stu-id="30bde-111">A combination of one letter, seven digits, and one space:</span></span>
  
- <span data-ttu-id="30bde-112">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="30bde-112">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="30bde-113">Un espace (facultatif)</span><span class="sxs-lookup"><span data-stu-id="30bde-113">One space (optional)</span></span>
    
- <span data-ttu-id="30bde-114">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="30bde-114">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="30bde-115">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="30bde-115">Checksum</span></span>

<span data-ttu-id="30bde-116">Non applicable</span><span class="sxs-lookup"><span data-stu-id="30bde-116">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="30bde-117">Définition</span><span class="sxs-lookup"><span data-stu-id="30bde-117">Definition</span></span>

<span data-ttu-id="30bde-118">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="30bde-118">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="30bde-119">L’expression régulière `Regex_austria_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="30bde-119">The regular expression  `Regex_austria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="30bde-120">Un mot clé à partir de `Keywords_austria_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="30bde-120">A keyword from  `Keywords_austria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_passport_number" />
          <Match idRef="Keywords_austria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="30bde-121">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="30bde-121">Keywords</span></span>

<span data-ttu-id="30bde-122">| |</span><span class="sxs-lookup"><span data-stu-id="30bde-122"></span></span>
|<span data-ttu-id="30bde-123">**Keywords_austria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="30bde-123">**Keywords_austria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="30bde-124">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="30bde-124">passport number</span></span>  <br/> <span data-ttu-id="30bde-125">numéro de passeport autrichien</span><span class="sxs-lookup"><span data-stu-id="30bde-125">austrian passport number</span></span>  <br/> <span data-ttu-id="30bde-126">passeport aucune</span><span class="sxs-lookup"><span data-stu-id="30bde-126">passport no</span></span>  <br/> <span data-ttu-id="30bde-127">reisepass</span><span class="sxs-lookup"><span data-stu-id="30bde-127">reisepass</span></span>  <br/> <span data-ttu-id="30bde-128">österreichisch reisepass</span><span class="sxs-lookup"><span data-stu-id="30bde-128">österreichisch reisepass</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="30bde-129">Belgique</span><span class="sxs-lookup"><span data-stu-id="30bde-129">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="30bde-130">Format</span><span class="sxs-lookup"><span data-stu-id="30bde-130">Format</span></span>

<span data-ttu-id="30bde-131">Deux lettres suivies de six chiffres sans espaces ni les délimiteurs</span><span class="sxs-lookup"><span data-stu-id="30bde-131">Two letters followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="30bde-132">Modèle</span><span class="sxs-lookup"><span data-stu-id="30bde-132">Pattern</span></span>

<span data-ttu-id="30bde-133">Deux lettres et suivi de six chiffres</span><span class="sxs-lookup"><span data-stu-id="30bde-133">Two letters and followed by six digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="30bde-134">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="30bde-134">Checksum</span></span>

<span data-ttu-id="30bde-135">Non applicable</span><span class="sxs-lookup"><span data-stu-id="30bde-135">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="30bde-136">Définition</span><span class="sxs-lookup"><span data-stu-id="30bde-136">Definition</span></span>

<span data-ttu-id="30bde-137">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="30bde-137">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="30bde-138">L’expression régulière `Regex_belgium_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="30bde-138">The regular expression  `Regex_belgium_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="30bde-139">Un mot clé à partir de `Keywords_belgium_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="30bde-139">A keyword from  `Keywords_belgium_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium__eu_passport_number" />
          <Match idRef="Keywords_belgium_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="30bde-140">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="30bde-140">Keywords</span></span>

<span data-ttu-id="30bde-141">| |</span><span class="sxs-lookup"><span data-stu-id="30bde-141"></span></span>
|<span data-ttu-id="30bde-142">**Keywords_belgium_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="30bde-142">**Keywords_belgium_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="30bde-143">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="30bde-143">passport number</span></span>  <br/> <span data-ttu-id="30bde-144">numéro de passeport belge</span><span class="sxs-lookup"><span data-stu-id="30bde-144">belgian passport number</span></span>  <br/> <span data-ttu-id="30bde-145">passeport aucune</span><span class="sxs-lookup"><span data-stu-id="30bde-145">passport no</span></span>  <br/> <span data-ttu-id="30bde-146">paspoort</span><span class="sxs-lookup"><span data-stu-id="30bde-146">paspoort</span></span>  <br/> <span data-ttu-id="30bde-147">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="30bde-147">paspoortnummer</span></span>  <br/> <span data-ttu-id="30bde-148">reisepass kein</span><span class="sxs-lookup"><span data-stu-id="30bde-148">reisepass kein</span></span>  <br/> <span data-ttu-id="30bde-149">reisepass</span><span class="sxs-lookup"><span data-stu-id="30bde-149">reisepass</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="30bde-150">Bulgarie</span><span class="sxs-lookup"><span data-stu-id="30bde-150">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="30bde-151">Format</span><span class="sxs-lookup"><span data-stu-id="30bde-151">Format</span></span>

<span data-ttu-id="30bde-152">Neuf chiffres sans espaces et les séparateurs</span><span class="sxs-lookup"><span data-stu-id="30bde-152">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="30bde-153">Modèle</span><span class="sxs-lookup"><span data-stu-id="30bde-153">Pattern</span></span>

 <span data-ttu-id="30bde-154">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="30bde-154">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="30bde-155">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="30bde-155">Checksum</span></span>

<span data-ttu-id="30bde-156">Non</span><span class="sxs-lookup"><span data-stu-id="30bde-156">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="30bde-157">Définition</span><span class="sxs-lookup"><span data-stu-id="30bde-157">Definition</span></span>

<span data-ttu-id="30bde-158">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="30bde-158">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="30bde-159">L’expression régulière `Regex_bulgaria_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="30bde-159">The regular expression  `Regex_bulgaria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="30bde-160">Un mot clé à partir de `Keywords_bulgaria_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="30bde-160">A keyword from  `Keywords_bulgaria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_passport_number" />
          <Match idRef="Keywords_bulgaria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="30bde-161">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="30bde-161">Keywords</span></span>

<span data-ttu-id="30bde-162">| |</span><span class="sxs-lookup"><span data-stu-id="30bde-162"></span></span>
|<span data-ttu-id="30bde-163">**Keywords_bulgaria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="30bde-163">**Keywords_bulgaria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="30bde-164">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="30bde-164">passport number</span></span>  <br/> <span data-ttu-id="30bde-165">numéro de passeport bulgare</span><span class="sxs-lookup"><span data-stu-id="30bde-165">bulgarian passport number</span></span>  <br/> <span data-ttu-id="30bde-166">passeport aucune</span><span class="sxs-lookup"><span data-stu-id="30bde-166">passport no</span></span>  <br/> <span data-ttu-id="30bde-167">НОМЕР НА ПАСПОРТА</span><span class="sxs-lookup"><span data-stu-id="30bde-167">номер на паспорта</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="30bde-168">Croatie</span><span class="sxs-lookup"><span data-stu-id="30bde-168">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="30bde-169">Format</span><span class="sxs-lookup"><span data-stu-id="30bde-169">Format</span></span>

<span data-ttu-id="30bde-170">Neuf chiffres sans espaces et les séparateurs</span><span class="sxs-lookup"><span data-stu-id="30bde-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="30bde-171">Modèle</span><span class="sxs-lookup"><span data-stu-id="30bde-171">Pattern</span></span>

 <span data-ttu-id="30bde-172">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="30bde-172">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="30bde-173">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="30bde-173">Checksum</span></span>

<span data-ttu-id="30bde-174">Non</span><span class="sxs-lookup"><span data-stu-id="30bde-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="30bde-175">Définition</span><span class="sxs-lookup"><span data-stu-id="30bde-175">Definition</span></span>

<span data-ttu-id="30bde-176">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="30bde-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="30bde-177">L’expression régulière `Regex_croatia_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="30bde-177">The regular expression  `Regex_croatia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="30bde-178">Un mot clé à partir de `Keywords_croatia_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="30bde-178">A keyword from  `Keywords_croatia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_passport_number" />
          <Match idRef="Keywords_croatia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="30bde-179">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="30bde-179">Keywords</span></span>

<span data-ttu-id="30bde-180">| |</span><span class="sxs-lookup"><span data-stu-id="30bde-180"></span></span>
|<span data-ttu-id="30bde-181">**Keywords_croatia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="30bde-181">**Keywords_croatia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="30bde-182">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="30bde-182">passport number</span></span>  <br/> <span data-ttu-id="30bde-183">numéro de passeport croate</span><span class="sxs-lookup"><span data-stu-id="30bde-183">croatian passport number</span></span>  <br/> <span data-ttu-id="30bde-184">passeport aucune</span><span class="sxs-lookup"><span data-stu-id="30bde-184">passport no</span></span>  <br/> <span data-ttu-id="30bde-185">broj putovnice</span><span class="sxs-lookup"><span data-stu-id="30bde-185">broj putovnice</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="30bde-186">Chypre</span><span class="sxs-lookup"><span data-stu-id="30bde-186">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="30bde-187">Format</span><span class="sxs-lookup"><span data-stu-id="30bde-187">Format</span></span>

<span data-ttu-id="30bde-188">Une lettre de suivi de 6 à 8 chiffres sans espaces ni les délimiteurs</span><span class="sxs-lookup"><span data-stu-id="30bde-188">One letter followed by 6-8 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="30bde-189">Modèle</span><span class="sxs-lookup"><span data-stu-id="30bde-189">Pattern</span></span>

<span data-ttu-id="30bde-190">Une lettre de suivi de 6 à 8 chiffres</span><span class="sxs-lookup"><span data-stu-id="30bde-190">One letter followed by six to eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="30bde-191">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="30bde-191">Checksum</span></span>

<span data-ttu-id="30bde-192">Non</span><span class="sxs-lookup"><span data-stu-id="30bde-192">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="30bde-193">Définition</span><span class="sxs-lookup"><span data-stu-id="30bde-193">Definition</span></span>

<span data-ttu-id="30bde-194">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="30bde-194">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="30bde-195">L’expression régulière `Regex_cyprus_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="30bde-195">The regular expression  `Regex_cyprus_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="30bde-196">Un mot clé à partir de `Keywords_cyprus_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="30bde-196">A keyword from  `Keywords_cyprus_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_passport_number" />
          <Match idRef="Keywords_cyprus_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="30bde-197">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="30bde-197">Keywords</span></span>

<span data-ttu-id="30bde-198">| |</span><span class="sxs-lookup"><span data-stu-id="30bde-198"></span></span>
|<span data-ttu-id="30bde-199">**Keywords_cyprus_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="30bde-199">**Keywords_cyprus_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="30bde-200">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="30bde-200">passport number</span></span>  <br/> <span data-ttu-id="30bde-201">numéro de passeport Chypre</span><span class="sxs-lookup"><span data-stu-id="30bde-201">cyprus passport number</span></span>  <br/> <span data-ttu-id="30bde-202">passeport aucune</span><span class="sxs-lookup"><span data-stu-id="30bde-202">passport no</span></span>  <br/> <span data-ttu-id="30bde-203">ΑΡΙΘΜΌ ΔΙΑΒΑΤΗΡΊΟΥ</span><span class="sxs-lookup"><span data-stu-id="30bde-203">αριθμό διαβατηρίου</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="30bde-204">République tchèque</span><span class="sxs-lookup"><span data-stu-id="30bde-204">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="30bde-205">Format</span><span class="sxs-lookup"><span data-stu-id="30bde-205">Format</span></span>

<span data-ttu-id="30bde-206">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="30bde-206">Eight digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="30bde-207">Modèle</span><span class="sxs-lookup"><span data-stu-id="30bde-207">Pattern</span></span>

<span data-ttu-id="30bde-208">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="30bde-208">Eight digits without spaces or delimiters</span></span>
  
### <a name="checksum"></a><span data-ttu-id="30bde-209">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="30bde-209">Checksum</span></span>

<span data-ttu-id="30bde-210">Non</span><span class="sxs-lookup"><span data-stu-id="30bde-210">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="30bde-211">Définition</span><span class="sxs-lookup"><span data-stu-id="30bde-211">Definition</span></span>

<span data-ttu-id="30bde-212">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="30bde-212">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="30bde-213">L’expression régulière `Regex_czech_republic_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="30bde-213">The regular expression  `Regex_czech_republic_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="30bde-214">Un mot clé à partir de `Keywords_czech_republic_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="30bde-214">A keyword from  `Keywords_czech_republic_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_passport_number" />
          <Match idRef="Keywords_czech_republic_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="30bde-215">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="30bde-215">Keywords</span></span>

<span data-ttu-id="30bde-216">| |</span><span class="sxs-lookup"><span data-stu-id="30bde-216"></span></span>
|<span data-ttu-id="30bde-217">**Keywords_czech_republic_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="30bde-217">**Keywords_czech_republic_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="30bde-218">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="30bde-218">passport number</span></span>  <br/> <span data-ttu-id="30bde-219">numéro de passeport tchèque</span><span class="sxs-lookup"><span data-stu-id="30bde-219">czech passport number</span></span>  <br/> <span data-ttu-id="30bde-220">passeport aucune</span><span class="sxs-lookup"><span data-stu-id="30bde-220">passport no</span></span>  <br/> <span data-ttu-id="30bde-221">pas de cestovní</span><span class="sxs-lookup"><span data-stu-id="30bde-221">cestovní pas</span></span>  <br/> <span data-ttu-id="30bde-222">pas</span><span class="sxs-lookup"><span data-stu-id="30bde-222">pas</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="30bde-223">Danemark</span><span class="sxs-lookup"><span data-stu-id="30bde-223">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="30bde-224">Format</span><span class="sxs-lookup"><span data-stu-id="30bde-224">Format</span></span>

<span data-ttu-id="30bde-225">Neuf chiffres sans espaces et les séparateurs</span><span class="sxs-lookup"><span data-stu-id="30bde-225">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="30bde-226">Modèle</span><span class="sxs-lookup"><span data-stu-id="30bde-226">Pattern</span></span>

 <span data-ttu-id="30bde-227">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="30bde-227">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="30bde-228">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="30bde-228">Checksum</span></span>

<span data-ttu-id="30bde-229">Non</span><span class="sxs-lookup"><span data-stu-id="30bde-229">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="30bde-230">Définition</span><span class="sxs-lookup"><span data-stu-id="30bde-230">Definition</span></span>

<span data-ttu-id="30bde-231">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="30bde-231">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="30bde-232">L’expression régulière `Regex_denmark_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="30bde-232">The regular expression  `Regex_denmark_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="30bde-233">Un mot clé à partir de `Keywords_denmark_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="30bde-233">A keyword from  `Keywords_denmark_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_passport_number" />
          <Match idRef="Keywords_denmark_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="30bde-234">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="30bde-234">Keywords</span></span>

<span data-ttu-id="30bde-235">| |</span><span class="sxs-lookup"><span data-stu-id="30bde-235"></span></span>
|<span data-ttu-id="30bde-236">**Keywords_denmark_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="30bde-236">**Keywords_denmark_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="30bde-237">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="30bde-237">passport number</span></span>  <br/> <span data-ttu-id="30bde-238">numéro de passeport danois</span><span class="sxs-lookup"><span data-stu-id="30bde-238">danish passport number</span></span>  <br/> <span data-ttu-id="30bde-239">passeport aucune</span><span class="sxs-lookup"><span data-stu-id="30bde-239">passport no</span></span>  <br/> <span data-ttu-id="30bde-240">pas</span><span class="sxs-lookup"><span data-stu-id="30bde-240">pas</span></span>  <br/> <span data-ttu-id="30bde-241">pasnummer</span><span class="sxs-lookup"><span data-stu-id="30bde-241">pasnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="30bde-242">Estonie</span><span class="sxs-lookup"><span data-stu-id="30bde-242">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="30bde-243">Format</span><span class="sxs-lookup"><span data-stu-id="30bde-243">Format</span></span>

<span data-ttu-id="30bde-244">Une lettre de suivi de sept chiffres sans espaces ni les délimiteurs</span><span class="sxs-lookup"><span data-stu-id="30bde-244">One letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="30bde-245">Modèle</span><span class="sxs-lookup"><span data-stu-id="30bde-245">Pattern</span></span>

<span data-ttu-id="30bde-246">Une lettre de suivi de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="30bde-246">One letter followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="30bde-247">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="30bde-247">Checksum</span></span>

<span data-ttu-id="30bde-248">Non</span><span class="sxs-lookup"><span data-stu-id="30bde-248">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="30bde-249">Définition</span><span class="sxs-lookup"><span data-stu-id="30bde-249">Definition</span></span>

<span data-ttu-id="30bde-250">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="30bde-250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="30bde-251">L’expression régulière `Regex_estonia_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="30bde-251">The regular expression  `Regex_estonia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="30bde-252">Un mot clé à partir de `Keywords_estonia_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="30bde-252">A keyword from  `Keywords_estonia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_passport_number" />
          <Match idRef="Keywords_estonia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="30bde-253">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="30bde-253">Keywords</span></span>

<span data-ttu-id="30bde-254">| |</span><span class="sxs-lookup"><span data-stu-id="30bde-254"></span></span>
|<span data-ttu-id="30bde-255">**Keywords_estonia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="30bde-255">**Keywords_estonia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="30bde-256">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="30bde-256">passport number</span></span>  <br/> <span data-ttu-id="30bde-257">numéro de passeport estonien</span><span class="sxs-lookup"><span data-stu-id="30bde-257">estonian passport number</span></span>  <br/> <span data-ttu-id="30bde-258">passeport aucune</span><span class="sxs-lookup"><span data-stu-id="30bde-258">passport no</span></span>  <br/> <span data-ttu-id="30bde-259">eesti kodaniku passe</span><span class="sxs-lookup"><span data-stu-id="30bde-259">eesti kodaniku pass</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="30bde-260">Finlande</span><span class="sxs-lookup"><span data-stu-id="30bde-260">Finland</span></span>

<span data-ttu-id="30bde-261">Pour plus d’informations, consultez la section « Numéro de passeport Finlande » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="30bde-261">For details, see the section "Finland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="30bde-262">France</span><span class="sxs-lookup"><span data-stu-id="30bde-262">France</span></span>

<span data-ttu-id="30bde-263">Pour plus d’informations, voir la section « Numéro de passeport France » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="30bde-263">For details, see the section "France Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="30bde-264">Allemagne</span><span class="sxs-lookup"><span data-stu-id="30bde-264">Germany</span></span>

<span data-ttu-id="30bde-265">Pour plus d’informations, voir la section « Numéro de passeport Allemagne » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="30bde-265">For details, see the section "Germany Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="30bde-266">Grèce</span><span class="sxs-lookup"><span data-stu-id="30bde-266">Greece</span></span>

### <a name="format"></a><span data-ttu-id="30bde-267">Format</span><span class="sxs-lookup"><span data-stu-id="30bde-267">Format</span></span>

<span data-ttu-id="30bde-268">Deux lettres suivies à sept chiffres sans espaces ni les délimiteurs</span><span class="sxs-lookup"><span data-stu-id="30bde-268">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="30bde-269">Modèle</span><span class="sxs-lookup"><span data-stu-id="30bde-269">Pattern</span></span>

<span data-ttu-id="30bde-270">Deux lettres suivies de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="30bde-270">Two letters followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="30bde-271">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="30bde-271">Checksum</span></span>

<span data-ttu-id="30bde-272">Non</span><span class="sxs-lookup"><span data-stu-id="30bde-272">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="30bde-273">Définition</span><span class="sxs-lookup"><span data-stu-id="30bde-273">Definition</span></span>

<span data-ttu-id="30bde-274">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="30bde-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="30bde-275">L’expression régulière `Regex_greece_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="30bde-275">The regular expression  `Regex_greece_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="30bde-276">Un mot clé à partir de `Keywords_greece_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="30bde-276">A keyword from  `Keywords_greece_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_passport_number" />
          <Match idRef="Keywords_greece_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="30bde-277">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="30bde-277">Keywords</span></span>

<span data-ttu-id="30bde-278">| |</span><span class="sxs-lookup"><span data-stu-id="30bde-278"></span></span>
|<span data-ttu-id="30bde-279">**Keywords_greece_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="30bde-279">**Keywords_greece_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="30bde-280">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="30bde-280">passport number</span></span>  <br/> <span data-ttu-id="30bde-281">numéro de passeport grec</span><span class="sxs-lookup"><span data-stu-id="30bde-281">greek passport number</span></span>  <br/> <span data-ttu-id="30bde-282">passeport aucune</span><span class="sxs-lookup"><span data-stu-id="30bde-282">passport no</span></span>  <br/> <span data-ttu-id="30bde-283">ΔΙΑΒΑΤΗΡΙΟ</span><span class="sxs-lookup"><span data-stu-id="30bde-283">διαβατηριο</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="30bde-284">Hongrie</span><span class="sxs-lookup"><span data-stu-id="30bde-284">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="30bde-285">Format</span><span class="sxs-lookup"><span data-stu-id="30bde-285">Format</span></span>

<span data-ttu-id="30bde-286">Deux lettres suivies de six ou sept chiffres sans espaces ni les délimiteurs</span><span class="sxs-lookup"><span data-stu-id="30bde-286">Two letters followed by six or seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="30bde-287">Modèle</span><span class="sxs-lookup"><span data-stu-id="30bde-287">Pattern</span></span>

<span data-ttu-id="30bde-288">Deux lettres suivies de six ou sept chiffres</span><span class="sxs-lookup"><span data-stu-id="30bde-288">Two letters followed by six or seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="30bde-289">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="30bde-289">Checksum</span></span>

<span data-ttu-id="30bde-290">Non</span><span class="sxs-lookup"><span data-stu-id="30bde-290">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="30bde-291">Définition</span><span class="sxs-lookup"><span data-stu-id="30bde-291">Definition</span></span>

<span data-ttu-id="30bde-292">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="30bde-292">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="30bde-293">L’expression régulière `Regex_hungary_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="30bde-293">The regular expression  `Regex_hungary_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="30bde-294">Un mot clé à partir de `Keywords_hungary_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="30bde-294">A keyword from  `Keywords_hungary_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_passport_number" />
          <Match idRef="Keywords_hungary_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="30bde-295">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="30bde-295">Keywords</span></span>

<span data-ttu-id="30bde-296">| |</span><span class="sxs-lookup"><span data-stu-id="30bde-296"></span></span>
|<span data-ttu-id="30bde-297">**Keywords_hungary_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="30bde-297">**Keywords_hungary_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="30bde-298">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="30bde-298">passport number</span></span>  <br/> <span data-ttu-id="30bde-299">numéro de passeport hongrois</span><span class="sxs-lookup"><span data-stu-id="30bde-299">hungarian passport number</span></span>  <br/> <span data-ttu-id="30bde-300">passeport aucune</span><span class="sxs-lookup"><span data-stu-id="30bde-300">passport no</span></span>  <br/> <span data-ttu-id="30bde-301">útlevél száma</span><span class="sxs-lookup"><span data-stu-id="30bde-301">útlevél száma</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="30bde-302">Irlande</span><span class="sxs-lookup"><span data-stu-id="30bde-302">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="30bde-303">Format</span><span class="sxs-lookup"><span data-stu-id="30bde-303">Format</span></span>

<span data-ttu-id="30bde-304">Deux lettres ou des chiffres suivis sept chiffres sans espaces ni les délimiteurs</span><span class="sxs-lookup"><span data-stu-id="30bde-304">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="30bde-305">Modèle</span><span class="sxs-lookup"><span data-stu-id="30bde-305">Pattern</span></span>

<span data-ttu-id="30bde-306">Deux lettres ou des chiffres suivis à sept chiffres :</span><span class="sxs-lookup"><span data-stu-id="30bde-306">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="30bde-307">Deux chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="30bde-307">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="30bde-308">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="30bde-308">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="30bde-309">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="30bde-309">Checksum</span></span>

<span data-ttu-id="30bde-310">Non</span><span class="sxs-lookup"><span data-stu-id="30bde-310">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="30bde-311">Définition</span><span class="sxs-lookup"><span data-stu-id="30bde-311">Definition</span></span>

<span data-ttu-id="30bde-312">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="30bde-312">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="30bde-313">L’expression régulière `Regex_ireland_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="30bde-313">The regular expression  `Regex_ireland_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="30bde-314">Un mot clé à partir de `Keywords_ireland_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="30bde-314">A keyword from  `Keywords_ireland_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_passport_number" />
          <Match idRef="Keywords_ireland_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="30bde-315">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="30bde-315">Keywords</span></span>

<span data-ttu-id="30bde-316">| |</span><span class="sxs-lookup"><span data-stu-id="30bde-316"></span></span>
|<span data-ttu-id="30bde-317">**Keywords_ireland_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="30bde-317">**Keywords_ireland_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="30bde-318">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="30bde-318">passport number</span></span>  <br/> <span data-ttu-id="30bde-319">numéro de passeport irlandais</span><span class="sxs-lookup"><span data-stu-id="30bde-319">irish passport number</span></span>  <br/> <span data-ttu-id="30bde-320">passeport aucune</span><span class="sxs-lookup"><span data-stu-id="30bde-320">passport no</span></span>  <br/> <span data-ttu-id="30bde-321">pas</span><span class="sxs-lookup"><span data-stu-id="30bde-321">pas</span></span>  <br/> <span data-ttu-id="30bde-322">passeport</span><span class="sxs-lookup"><span data-stu-id="30bde-322">passport</span></span>  <br/> <span data-ttu-id="30bde-323">passeport</span><span class="sxs-lookup"><span data-stu-id="30bde-323">passeport</span></span>  <br/> <span data-ttu-id="30bde-324">numero de passeport</span><span class="sxs-lookup"><span data-stu-id="30bde-324">passeport numero</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="30bde-325">Italie</span><span class="sxs-lookup"><span data-stu-id="30bde-325">Italy</span></span>

### <a name="format"></a><span data-ttu-id="30bde-326">Format</span><span class="sxs-lookup"><span data-stu-id="30bde-326">Format</span></span>

<span data-ttu-id="30bde-327">Deux lettres ou des chiffres suivis sept chiffres sans espaces ni les délimiteurs</span><span class="sxs-lookup"><span data-stu-id="30bde-327">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="30bde-328">Modèle</span><span class="sxs-lookup"><span data-stu-id="30bde-328">Pattern</span></span>

<span data-ttu-id="30bde-329">Deux lettres ou des chiffres suivis à sept chiffres :</span><span class="sxs-lookup"><span data-stu-id="30bde-329">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="30bde-330">Deux chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="30bde-330">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="30bde-331">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="30bde-331">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="30bde-332">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="30bde-332">Checksum</span></span>

<span data-ttu-id="30bde-333">Non applicable</span><span class="sxs-lookup"><span data-stu-id="30bde-333">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="30bde-334">Définition</span><span class="sxs-lookup"><span data-stu-id="30bde-334">Definition</span></span>

<span data-ttu-id="30bde-335">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="30bde-335">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="30bde-336">L’expression régulière `Regex_italy_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="30bde-336">The regular expression  `Regex_italy_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="30bde-337">Un mot clé à partir de `Keywords_italy_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="30bde-337">A keyword from  `Keywords_italy_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_passport_number" />
          <Match idRef="Keywords_italy_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="30bde-338">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="30bde-338">Keywords</span></span>

<span data-ttu-id="30bde-339">| |</span><span class="sxs-lookup"><span data-stu-id="30bde-339"></span></span>
|<span data-ttu-id="30bde-340">**Keywords_italy_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="30bde-340">**Keywords_italy_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="30bde-341">numéro de passeport italien</span><span class="sxs-lookup"><span data-stu-id="30bde-341">italian passport number</span></span>  <br/> <span data-ttu-id="30bde-342">Repubblica italiana passaporto</span><span class="sxs-lookup"><span data-stu-id="30bde-342">repubblica italiana passaporto</span></span>  <br/> <span data-ttu-id="30bde-343">passaporto</span><span class="sxs-lookup"><span data-stu-id="30bde-343">passaporto</span></span>  <br/> <span data-ttu-id="30bde-344">passaporto italiana</span><span class="sxs-lookup"><span data-stu-id="30bde-344">passaporto italiana</span></span>  <br/> <span data-ttu-id="30bde-345">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="30bde-345">passport number</span></span>  <br/> <span data-ttu-id="30bde-346">Italiana passaporto numero</span><span class="sxs-lookup"><span data-stu-id="30bde-346">italiana passaporto numero</span></span>  <br/> <span data-ttu-id="30bde-347">numero passaporto</span><span class="sxs-lookup"><span data-stu-id="30bde-347">passaporto numero</span></span>  <br/> <span data-ttu-id="30bde-348">numéro passeport italien</span><span class="sxs-lookup"><span data-stu-id="30bde-348">numéro passeport italien</span></span>  <br/> <span data-ttu-id="30bde-349">passeport numéro</span><span class="sxs-lookup"><span data-stu-id="30bde-349">numéro passeport</span></span>  <br/> |
   
## <a name="latvia"></a><span data-ttu-id="30bde-350">Lettonie</span><span class="sxs-lookup"><span data-stu-id="30bde-350">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="30bde-351">Format</span><span class="sxs-lookup"><span data-stu-id="30bde-351">Format</span></span>

<span data-ttu-id="30bde-352">Deux lettres ou des chiffres suivis sept chiffres sans espaces ni les délimiteurs</span><span class="sxs-lookup"><span data-stu-id="30bde-352">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="30bde-353">Modèle</span><span class="sxs-lookup"><span data-stu-id="30bde-353">Pattern</span></span>

<span data-ttu-id="30bde-354">Deux lettres ou des chiffres suivis à sept chiffres :</span><span class="sxs-lookup"><span data-stu-id="30bde-354">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="30bde-355">Deux chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="30bde-355">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="30bde-356">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="30bde-356">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="30bde-357">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="30bde-357">Checksum</span></span>

<span data-ttu-id="30bde-358">Non</span><span class="sxs-lookup"><span data-stu-id="30bde-358">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="30bde-359">Définition</span><span class="sxs-lookup"><span data-stu-id="30bde-359">Definition</span></span>

<span data-ttu-id="30bde-360">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="30bde-360">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="30bde-361">L’expression régulière `Regex_latvia_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="30bde-361">The regular expression  `Regex_latvia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="30bde-362">Un mot clé à partir de `Keywords_latvia_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="30bde-362">A keyword from  `Keywords_latvia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_passport_number" />
          <Match idRef="Keywords_latvia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="30bde-363">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="30bde-363">Keywords</span></span>

<span data-ttu-id="30bde-364">| |</span><span class="sxs-lookup"><span data-stu-id="30bde-364"></span></span>
|<span data-ttu-id="30bde-365">**Keywords_latvia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="30bde-365">**Keywords_latvia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="30bde-366">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="30bde-366">passport number</span></span>  <br/> <span data-ttu-id="30bde-367">numéro de passeport letton</span><span class="sxs-lookup"><span data-stu-id="30bde-367">latvian passport number</span></span>  <br/> <span data-ttu-id="30bde-368">passeport aucune</span><span class="sxs-lookup"><span data-stu-id="30bde-368">passport no</span></span>  <br/> <span data-ttu-id="30bde-369">pase numurs</span><span class="sxs-lookup"><span data-stu-id="30bde-369">pase numurs</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="30bde-370">Lituanie</span><span class="sxs-lookup"><span data-stu-id="30bde-370">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="30bde-371">Format</span><span class="sxs-lookup"><span data-stu-id="30bde-371">Format</span></span>

<span data-ttu-id="30bde-372">Huit des chiffres ou des lettres sans espaces ni les délimiteurs</span><span class="sxs-lookup"><span data-stu-id="30bde-372">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="30bde-373">Modèle</span><span class="sxs-lookup"><span data-stu-id="30bde-373">Pattern</span></span>

<span data-ttu-id="30bde-374">Huit des chiffres ou des lettres (non sensible à la casse)</span><span class="sxs-lookup"><span data-stu-id="30bde-374">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="30bde-375">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="30bde-375">Checksum</span></span>

<span data-ttu-id="30bde-376">Non applicable</span><span class="sxs-lookup"><span data-stu-id="30bde-376">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="30bde-377">Définition</span><span class="sxs-lookup"><span data-stu-id="30bde-377">Definition</span></span>

<span data-ttu-id="30bde-378">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="30bde-378">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="30bde-379">L’expression régulière `Regex_lithuania_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="30bde-379">The regular expression  `Regex_lithuania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="30bde-380">Un mot clé à partir de `Keywords_lithuania_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="30bde-380">A keyword from  `Keywords_lithuania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_passport_number" />
          <Match idRef="Keywords_lithuania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="30bde-381">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="30bde-381">Keywords</span></span>

<span data-ttu-id="30bde-382">| |</span><span class="sxs-lookup"><span data-stu-id="30bde-382"></span></span>
|<span data-ttu-id="30bde-383">**Keywords_lithuania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="30bde-383">**Keywords_lithuania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="30bde-384">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="30bde-384">passport number</span></span>  <br/> <span data-ttu-id="30bde-385">numéro de passeport lithunian</span><span class="sxs-lookup"><span data-stu-id="30bde-385">lithunian passport number</span></span>  <br/> <span data-ttu-id="30bde-386">passeport aucune</span><span class="sxs-lookup"><span data-stu-id="30bde-386">passport no</span></span>  <br/> <span data-ttu-id="30bde-387">Paso numeris</span><span class="sxs-lookup"><span data-stu-id="30bde-387">paso numeris</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="30bde-388">Luxembourg</span><span class="sxs-lookup"><span data-stu-id="30bde-388">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="30bde-389">Format</span><span class="sxs-lookup"><span data-stu-id="30bde-389">Format</span></span>

<span data-ttu-id="30bde-390">Huit des chiffres ou des lettres sans espaces ni les délimiteurs</span><span class="sxs-lookup"><span data-stu-id="30bde-390">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="30bde-391">Modèle</span><span class="sxs-lookup"><span data-stu-id="30bde-391">Pattern</span></span>

<span data-ttu-id="30bde-392">Huit des chiffres ou des lettres (non sensible à la casse)</span><span class="sxs-lookup"><span data-stu-id="30bde-392">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="30bde-393">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="30bde-393">Checksum</span></span>

<span data-ttu-id="30bde-394">Non</span><span class="sxs-lookup"><span data-stu-id="30bde-394">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="30bde-395">Définition</span><span class="sxs-lookup"><span data-stu-id="30bde-395">Definition</span></span>

<span data-ttu-id="30bde-396">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="30bde-396">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="30bde-397">L’expression régulière `Regex_nation_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="30bde-397">The regular expression  `Regex_nation_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="30bde-398">Un mot clé à partir de `Keywords_nation_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="30bde-398">A keyword from  `Keywords_nation_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_nation_eu_passport_number" />
          <Match idRef="Keywords_nation_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="30bde-399">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="30bde-399">Keywords</span></span>

<span data-ttu-id="30bde-400">| |</span><span class="sxs-lookup"><span data-stu-id="30bde-400"></span></span>
|<span data-ttu-id="30bde-401">**Keywords_nation_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="30bde-401">**Keywords_nation_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="30bde-402">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="30bde-402">passport number</span></span>  <br/> <span data-ttu-id="30bde-403">numéro de passeport letton</span><span class="sxs-lookup"><span data-stu-id="30bde-403">latvian passport number</span></span>  <br/> <span data-ttu-id="30bde-404">passeport aucune</span><span class="sxs-lookup"><span data-stu-id="30bde-404">passport no</span></span>  <br/> <span data-ttu-id="30bde-405">passnummer</span><span class="sxs-lookup"><span data-stu-id="30bde-405">passnummer</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="30bde-406">Malte</span><span class="sxs-lookup"><span data-stu-id="30bde-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="30bde-407">Format</span><span class="sxs-lookup"><span data-stu-id="30bde-407">Format</span></span>

<span data-ttu-id="30bde-408">Sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="30bde-408">Seven digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="30bde-409">Modèle</span><span class="sxs-lookup"><span data-stu-id="30bde-409">Pattern</span></span>

 <span data-ttu-id="30bde-410">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="30bde-410">Seven digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="30bde-411">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="30bde-411">Checksum</span></span>

<span data-ttu-id="30bde-412">Non</span><span class="sxs-lookup"><span data-stu-id="30bde-412">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="30bde-413">Définition</span><span class="sxs-lookup"><span data-stu-id="30bde-413">Definition</span></span>

<span data-ttu-id="30bde-414">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="30bde-414">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="30bde-415">L’expression régulière `Regex_malta_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="30bde-415">The regular expression  `Regex_malta_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="30bde-416">Un mot clé à partir de `Keywords_malta_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="30bde-416">A keyword from  `Keywords_malta_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_passport_number" />
          <Match idRef="Keywords_malta_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="30bde-417">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="30bde-417">Keywords</span></span>

<span data-ttu-id="30bde-418">| |</span><span class="sxs-lookup"><span data-stu-id="30bde-418"></span></span>
|<span data-ttu-id="30bde-419">**Keywords_malta_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="30bde-419">**Keywords_malta_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="30bde-420">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="30bde-420">passport number</span></span>  <br/> <span data-ttu-id="30bde-421">numéro de passeport maltais</span><span class="sxs-lookup"><span data-stu-id="30bde-421">maltese passport number</span></span>  <br/> <span data-ttu-id="30bde-422">passeport aucune</span><span class="sxs-lookup"><span data-stu-id="30bde-422">passport no</span></span>  <br/> <span data-ttu-id="30bde-423">numérique un numru-passaport</span><span class="sxs-lookup"><span data-stu-id="30bde-423">numru tal-passaport</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="30bde-424">Pays-Bas</span><span class="sxs-lookup"><span data-stu-id="30bde-424">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="30bde-425">Format</span><span class="sxs-lookup"><span data-stu-id="30bde-425">Format</span></span>

<span data-ttu-id="30bde-426">Neuf des lettres ou des chiffres sans espaces ni les délimiteurs</span><span class="sxs-lookup"><span data-stu-id="30bde-426">Nine letters or digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="30bde-427">Modèle</span><span class="sxs-lookup"><span data-stu-id="30bde-427">Pattern</span></span>

<span data-ttu-id="30bde-428">Neuf des lettres ou des chiffres</span><span class="sxs-lookup"><span data-stu-id="30bde-428">Nine letters or digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="30bde-429">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="30bde-429">Checksum</span></span>

<span data-ttu-id="30bde-430">Non applicable</span><span class="sxs-lookup"><span data-stu-id="30bde-430">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="30bde-431">Définition</span><span class="sxs-lookup"><span data-stu-id="30bde-431">Definition</span></span>

<span data-ttu-id="30bde-432">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="30bde-432">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="30bde-433">L’expression régulière `Regex_netherlands_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="30bde-433">The regular expression  `Regex_netherlands_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="30bde-434">Un mot clé à partir de `Keywords_netherlands_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="30bde-434">A keyword from  `Keywords_netherlands_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_passport_number" />
          <Match idRef="Keywords_netherlands_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="30bde-435">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="30bde-435">Keywords</span></span>

<span data-ttu-id="30bde-436">| |</span><span class="sxs-lookup"><span data-stu-id="30bde-436"></span></span>
|<span data-ttu-id="30bde-437">**Keywords_netherlands_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="30bde-437">**Keywords_netherlands_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="30bde-438">numéro de passeport néerlandais</span><span class="sxs-lookup"><span data-stu-id="30bde-438">dutch passport number</span></span>  <br/> <span data-ttu-id="30bde-439">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="30bde-439">passport number</span></span>  <br/> <span data-ttu-id="30bde-440">numéro de passeport pays-bas</span><span class="sxs-lookup"><span data-stu-id="30bde-440">netherlands passport number</span></span>  <br/> <span data-ttu-id="30bde-441">nederlanden paspoort nummer</span><span class="sxs-lookup"><span data-stu-id="30bde-441">nederlanden paspoort nummer</span></span>  <br/> <span data-ttu-id="30bde-442">paspoort</span><span class="sxs-lookup"><span data-stu-id="30bde-442">paspoort</span></span>  <br/> <span data-ttu-id="30bde-443">nederlanden paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="30bde-443">nederlanden paspoortnummer</span></span>  <br/> <span data-ttu-id="30bde-444">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="30bde-444">paspoortnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="30bde-445">Pologne</span><span class="sxs-lookup"><span data-stu-id="30bde-445">Poland</span></span>

<span data-ttu-id="30bde-446">Pour plus d’informations, voir la section « Numéro de passeport Pologne » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="30bde-446">For details, see the section "Poland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="30bde-447">Portugal</span><span class="sxs-lookup"><span data-stu-id="30bde-447">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="30bde-448">Format</span><span class="sxs-lookup"><span data-stu-id="30bde-448">Format</span></span>

<span data-ttu-id="30bde-449">Une lettre de suivi de six chiffres sans espaces ni les délimiteurs</span><span class="sxs-lookup"><span data-stu-id="30bde-449">One letter followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="30bde-450">Modèle</span><span class="sxs-lookup"><span data-stu-id="30bde-450">Pattern</span></span>

<span data-ttu-id="30bde-451">Une lettre de suivi de six chiffres :</span><span class="sxs-lookup"><span data-stu-id="30bde-451">One letter followed by six digits:</span></span>
  
- <span data-ttu-id="30bde-452">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="30bde-452">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="30bde-453">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="30bde-453">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="30bde-454">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="30bde-454">Checksum</span></span>

<span data-ttu-id="30bde-455">Non</span><span class="sxs-lookup"><span data-stu-id="30bde-455">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="30bde-456">Définition</span><span class="sxs-lookup"><span data-stu-id="30bde-456">Definition</span></span>

<span data-ttu-id="30bde-457">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="30bde-457">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="30bde-458">L’expression régulière `Regex_portugal_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="30bde-458">The regular expression  `Regex_portugal_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="30bde-459">Un mot clé à partir de `Keywords_portugal_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="30bde-459">A keyword from  `Keywords_portugal_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_passport_number" />
          <Match idRef="Keywords_portugal_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="30bde-460">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="30bde-460">Keywords</span></span>

<span data-ttu-id="30bde-461">| |</span><span class="sxs-lookup"><span data-stu-id="30bde-461"></span></span>
|<span data-ttu-id="30bde-462">**Keywords_portugal_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="30bde-462">**Keywords_portugal_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="30bde-463">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="30bde-463">passport number</span></span>  <br/> <span data-ttu-id="30bde-464">numéro de passeport portugais</span><span class="sxs-lookup"><span data-stu-id="30bde-464">portuguese passport number</span></span>  <br/> <span data-ttu-id="30bde-465">passeport aucune</span><span class="sxs-lookup"><span data-stu-id="30bde-465">passport no</span></span>  <br/> <span data-ttu-id="30bde-466">Número passaporte</span><span class="sxs-lookup"><span data-stu-id="30bde-466">número do passaporte</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="30bde-467">Roumanie</span><span class="sxs-lookup"><span data-stu-id="30bde-467">Romania</span></span>

### <a name="format"></a><span data-ttu-id="30bde-468">Format</span><span class="sxs-lookup"><span data-stu-id="30bde-468">Format</span></span>

<span data-ttu-id="30bde-469">Huit ou neuf chiffres sans espaces et les séparateurs</span><span class="sxs-lookup"><span data-stu-id="30bde-469">Eight or nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="30bde-470">Modèle</span><span class="sxs-lookup"><span data-stu-id="30bde-470">Pattern</span></span>

<span data-ttu-id="30bde-471">Huit ou neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="30bde-471">Eight or nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="30bde-472">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="30bde-472">Checksum</span></span>

<span data-ttu-id="30bde-473">Non</span><span class="sxs-lookup"><span data-stu-id="30bde-473">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="30bde-474">Définition</span><span class="sxs-lookup"><span data-stu-id="30bde-474">Definition</span></span>

<span data-ttu-id="30bde-475">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="30bde-475">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="30bde-476">L’expression régulière `Regex_romania_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="30bde-476">The regular expression  `Regex_romania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="30bde-477">Un mot clé à partir de `Keywords_romania_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="30bde-477">A keyword from  `Keywords_romania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_passport_number" />
          <Match idRef="Keywords_romania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="30bde-478">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="30bde-478">Keywords</span></span>

<span data-ttu-id="30bde-479">| |</span><span class="sxs-lookup"><span data-stu-id="30bde-479"></span></span>
|<span data-ttu-id="30bde-480">**Keywords_romania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="30bde-480">**Keywords_romania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="30bde-481">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="30bde-481">passport number</span></span>  <br/> <span data-ttu-id="30bde-482">numéro de passeport roumain</span><span class="sxs-lookup"><span data-stu-id="30bde-482">romanian passport number</span></span>  <br/> <span data-ttu-id="30bde-483">passeport aucune</span><span class="sxs-lookup"><span data-stu-id="30bde-483">passport no</span></span>  <br/> <span data-ttu-id="30bde-484">numărul pașaportului</span><span class="sxs-lookup"><span data-stu-id="30bde-484">numărul pașaportului</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="30bde-485">République de Slovaquie</span><span class="sxs-lookup"><span data-stu-id="30bde-485">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="30bde-486">Format</span><span class="sxs-lookup"><span data-stu-id="30bde-486">Format</span></span>

<span data-ttu-id="30bde-487">Un chiffre ou une lettre suivi par sept chiffres sans espaces ni les délimiteurs</span><span class="sxs-lookup"><span data-stu-id="30bde-487">One digit or letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="30bde-488">Modèle</span><span class="sxs-lookup"><span data-stu-id="30bde-488">Pattern</span></span>

<span data-ttu-id="30bde-489">Un chiffre ou une lettre (pas sensible à la casse) suivi de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="30bde-489">One digit or letter (not case sensitive) followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="30bde-490">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="30bde-490">Checksum</span></span>

<span data-ttu-id="30bde-491">Non</span><span class="sxs-lookup"><span data-stu-id="30bde-491">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="30bde-492">Définition</span><span class="sxs-lookup"><span data-stu-id="30bde-492">Definition</span></span>

<span data-ttu-id="30bde-493">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="30bde-493">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="30bde-494">L’expression régulière `Regex_slovakia_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="30bde-494">The regular expression  `Regex_slovakia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="30bde-495">Un mot clé à partir de `Keywords_slovakia_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="30bde-495">A keyword from  `Keywords_slovakia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_passport_number" />
          <Match idRef="Keywords_slovakia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="30bde-496">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="30bde-496">Keywords</span></span>

<span data-ttu-id="30bde-497">| |</span><span class="sxs-lookup"><span data-stu-id="30bde-497"></span></span>
|<span data-ttu-id="30bde-498">**Keywords_slovakia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="30bde-498">**Keywords_slovakia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="30bde-499">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="30bde-499">passport number</span></span>  <br/> <span data-ttu-id="30bde-500">numéro de passeport slovaque</span><span class="sxs-lookup"><span data-stu-id="30bde-500">slovakian passport number</span></span>  <br/> <span data-ttu-id="30bde-501">passeport aucune</span><span class="sxs-lookup"><span data-stu-id="30bde-501">passport no</span></span>  <br/> <span data-ttu-id="30bde-502">Číslo pasu</span><span class="sxs-lookup"><span data-stu-id="30bde-502">číslo pasu</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="30bde-503">Slovénie</span><span class="sxs-lookup"><span data-stu-id="30bde-503">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="30bde-504">Format</span><span class="sxs-lookup"><span data-stu-id="30bde-504">Format</span></span>

<span data-ttu-id="30bde-505">Deux lettres suivies à sept chiffres sans espaces ni les délimiteurs</span><span class="sxs-lookup"><span data-stu-id="30bde-505">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="30bde-506">Modèle</span><span class="sxs-lookup"><span data-stu-id="30bde-506">Pattern</span></span>

<span data-ttu-id="30bde-507">Deux lettres suivies à sept chiffres :</span><span class="sxs-lookup"><span data-stu-id="30bde-507">Two letters followed by seven digits:</span></span>
  
- <span data-ttu-id="30bde-508">La lettre « P »</span><span class="sxs-lookup"><span data-stu-id="30bde-508">The letter "P"</span></span>
    
- <span data-ttu-id="30bde-509">Une lettre majuscule</span><span class="sxs-lookup"><span data-stu-id="30bde-509">One uppercase letter</span></span>
    
- <span data-ttu-id="30bde-510">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="30bde-510">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="30bde-511">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="30bde-511">Checksum</span></span>

<span data-ttu-id="30bde-512">Non</span><span class="sxs-lookup"><span data-stu-id="30bde-512">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="30bde-513">Définition</span><span class="sxs-lookup"><span data-stu-id="30bde-513">Definition</span></span>

<span data-ttu-id="30bde-514">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="30bde-514">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="30bde-515">L’expression régulière `Regex_slovenia_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="30bde-515">The regular expression  `Regex_slovenia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="30bde-516">Un mot clé à partir de `Keywords_slovenia_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="30bde-516">A keyword from  `Keywords_slovenia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_passport_number" />
          <Match idRef="Keywords_slovenia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="30bde-517">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="30bde-517">Keywords</span></span>

<span data-ttu-id="30bde-518">| |</span><span class="sxs-lookup"><span data-stu-id="30bde-518"></span></span>
|<span data-ttu-id="30bde-519">**Keywords_slovenia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="30bde-519">**Keywords_slovenia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="30bde-520">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="30bde-520">passport number</span></span>  <br/> <span data-ttu-id="30bde-521">numéro de passeport slovène</span><span class="sxs-lookup"><span data-stu-id="30bde-521">slovenian passport number</span></span>  <br/> <span data-ttu-id="30bde-522">passeport aucune</span><span class="sxs-lookup"><span data-stu-id="30bde-522">passport no</span></span>  <br/> <span data-ttu-id="30bde-523">Številka potnega lista</span><span class="sxs-lookup"><span data-stu-id="30bde-523">številka potnega lista</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="30bde-524">Espagne</span><span class="sxs-lookup"><span data-stu-id="30bde-524">Spain</span></span>

### <a name="format"></a><span data-ttu-id="30bde-525">Format</span><span class="sxs-lookup"><span data-stu-id="30bde-525">Format</span></span>

<span data-ttu-id="30bde-526">Une combinaison de huit ou neuf caractères de lettres et chiffres sans espaces ni les délimiteurs</span><span class="sxs-lookup"><span data-stu-id="30bde-526">An eight- or nine-character combination of letters and numbers with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="30bde-527">Modèle</span><span class="sxs-lookup"><span data-stu-id="30bde-527">Pattern</span></span>

<span data-ttu-id="30bde-528">Une combinaison de huit ou neuf caractères de lettres et chiffres :</span><span class="sxs-lookup"><span data-stu-id="30bde-528">An eight- or nine-character combination of letters and numbers:</span></span>
  
-  <span data-ttu-id="30bde-529">Deux chiffres ou des lettres</span><span class="sxs-lookup"><span data-stu-id="30bde-529">Two digits or letters</span></span> 
    
- <span data-ttu-id="30bde-530">Un chiffre ou une lettre (facultatif)</span><span class="sxs-lookup"><span data-stu-id="30bde-530">One digit or letter (optional)</span></span>
    
- <span data-ttu-id="30bde-531">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="30bde-531">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="30bde-532">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="30bde-532">Checksum</span></span>

<span data-ttu-id="30bde-533">Non applicable</span><span class="sxs-lookup"><span data-stu-id="30bde-533">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="30bde-534">Définition</span><span class="sxs-lookup"><span data-stu-id="30bde-534">Definition</span></span>

<span data-ttu-id="30bde-535">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="30bde-535">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="30bde-536">L’expression régulière `Regex_spain_eu_passport_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="30bde-536">The regular expression  `Regex_spain_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="30bde-537">Un mot clé à partir de `Keywords_spain_eu_passport_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="30bde-537">A keyword from  `Keywords_spain_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_passport_number" />
          <Match idRef="Keywords_spain_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="30bde-538">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="30bde-538">Keywords</span></span>

<span data-ttu-id="30bde-539">| |</span><span class="sxs-lookup"><span data-stu-id="30bde-539"></span></span>
|<span data-ttu-id="30bde-540">**Keywords_spain_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="30bde-540">**Keywords_spain_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="30bde-541">passeport</span><span class="sxs-lookup"><span data-stu-id="30bde-541">passport</span></span>  <br/> <span data-ttu-id="30bde-542">passeport Espagne</span><span class="sxs-lookup"><span data-stu-id="30bde-542">spain passport</span></span>  <br/> <span data-ttu-id="30bde-543">livre Passport</span><span class="sxs-lookup"><span data-stu-id="30bde-543">passport book</span></span>  <br/> <span data-ttu-id="30bde-544">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="30bde-544">passport number</span></span>  <br/> <span data-ttu-id="30bde-545">passeport aucune</span><span class="sxs-lookup"><span data-stu-id="30bde-545">passport no</span></span>  <br/> <span data-ttu-id="30bde-546">libreta pasaporte</span><span class="sxs-lookup"><span data-stu-id="30bde-546">libreta pasaporte</span></span>  <br/> <span data-ttu-id="30bde-547">Número pasaporte</span><span class="sxs-lookup"><span data-stu-id="30bde-547">número pasaporte</span></span>  <br/> <span data-ttu-id="30bde-548">pasaporte España</span><span class="sxs-lookup"><span data-stu-id="30bde-548">españa pasaporte</span></span>  <br/> <span data-ttu-id="30bde-549">pasaporte</span><span class="sxs-lookup"><span data-stu-id="30bde-549">pasaporte</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="30bde-550">Suède</span><span class="sxs-lookup"><span data-stu-id="30bde-550">Sweden</span></span>

<span data-ttu-id="30bde-551">Pour plus d’informations, voir la section « Numéro de passeport Suède » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="30bde-551">For details, see the section "Sweden Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="uk"></a><span data-ttu-id="30bde-552">ROYAUME-UNI</span><span class="sxs-lookup"><span data-stu-id="30bde-552">UK</span></span>

<span data-ttu-id="30bde-p103">Pour plus d’informations, consultez la section « Numéro de passeport US / britannique » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="30bde-p103">For details, see the section "U.S. / U.K. Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="30bde-555">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30bde-555">See also</span></span>

[<span data-ttu-id="30bde-556">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="30bde-556">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

