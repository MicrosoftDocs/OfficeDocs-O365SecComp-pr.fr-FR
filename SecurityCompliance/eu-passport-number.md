---
title: Numéro de passeport UE
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/16/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 8c00df57-9fb3-459c-ba87-40480c87bd55
description: Cette rubrique présente ce qu'une stratégie de protection contre la perte de données (DLP) recherche lorsqu'elle détecte le type d'informations sensibles du numéro de passeport de l'UE. Ce type d'informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.
ms.openlocfilehash: c46f683bd1baf651bcf13c1766dfff3cb953b341
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218264"
---
# <a name="eu-passport-number"></a><span data-ttu-id="204f6-104">Numéro de passeport UE</span><span class="sxs-lookup"><span data-stu-id="204f6-104">EU Passport Number</span></span>

<span data-ttu-id="204f6-p102">Cette rubrique présente ce qu'une stratégie de protection contre la perte de données (DLP) recherche lorsqu'elle détecte le type d'informations sensibles du numéro de passeport de l'UE. Ce type d'informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.</span><span class="sxs-lookup"><span data-stu-id="204f6-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Passport Number sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="204f6-107">Autriche</span><span class="sxs-lookup"><span data-stu-id="204f6-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="204f6-108">Format</span><span class="sxs-lookup"><span data-stu-id="204f6-108">Format</span></span>

<span data-ttu-id="204f6-109">Une lettre suivie d'un espace facultatif et de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="204f6-109">One letter followed by an optional space and seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="204f6-110">Modèle</span><span class="sxs-lookup"><span data-stu-id="204f6-110">Pattern</span></span>

<span data-ttu-id="204f6-111">Une combinaison d'une lettre, de sept chiffres et d'un espace:</span><span class="sxs-lookup"><span data-stu-id="204f6-111">A combination of one letter, seven digits, and one space:</span></span>
  
- <span data-ttu-id="204f6-112">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="204f6-112">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="204f6-113">Un espace (facultatif)</span><span class="sxs-lookup"><span data-stu-id="204f6-113">One space (optional)</span></span>
    
- <span data-ttu-id="204f6-114">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="204f6-114">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="204f6-115">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="204f6-115">Checksum</span></span>

<span data-ttu-id="204f6-116">Non applicable</span><span class="sxs-lookup"><span data-stu-id="204f6-116">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="204f6-117">Définition</span><span class="sxs-lookup"><span data-stu-id="204f6-117">Definition</span></span>

<span data-ttu-id="204f6-118">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="204f6-118">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="204f6-119">L'expression `Regex_austria_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="204f6-119">The regular expression  `Regex_austria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="204f6-120">Un mot clé `Keywords_austria_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="204f6-120">A keyword from  `Keywords_austria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_passport_number" />
          <Match idRef="Keywords_austria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="204f6-121">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="204f6-121">Keywords</span></span>

<span data-ttu-id="204f6-122">| |</span><span class="sxs-lookup"><span data-stu-id="204f6-122"></span></span>
|<span data-ttu-id="204f6-123">**Keywords_austria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="204f6-123">**Keywords_austria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="204f6-124">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-124">passport number</span></span>  <br/> <span data-ttu-id="204f6-125">Numéro de passeport autrichien</span><span class="sxs-lookup"><span data-stu-id="204f6-125">austrian passport number</span></span>  <br/> <span data-ttu-id="204f6-126">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-126">passport no</span></span>  <br/> <span data-ttu-id="204f6-127">reisepass</span><span class="sxs-lookup"><span data-stu-id="204f6-127">reisepass</span></span>  <br/> <span data-ttu-id="204f6-128">österreichisch Reisepass</span><span class="sxs-lookup"><span data-stu-id="204f6-128">österreichisch reisepass</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="204f6-129">Belgique</span><span class="sxs-lookup"><span data-stu-id="204f6-129">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="204f6-130">Format</span><span class="sxs-lookup"><span data-stu-id="204f6-130">Format</span></span>

<span data-ttu-id="204f6-131">Deux lettres suivies de six chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="204f6-131">Two letters followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="204f6-132">Modèle</span><span class="sxs-lookup"><span data-stu-id="204f6-132">Pattern</span></span>

<span data-ttu-id="204f6-133">Deux lettres et suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="204f6-133">Two letters and followed by six digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="204f6-134">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="204f6-134">Checksum</span></span>

<span data-ttu-id="204f6-135">Non applicable</span><span class="sxs-lookup"><span data-stu-id="204f6-135">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="204f6-136">Définition</span><span class="sxs-lookup"><span data-stu-id="204f6-136">Definition</span></span>

<span data-ttu-id="204f6-137">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="204f6-137">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="204f6-138">L'expression `Regex_belgium_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="204f6-138">The regular expression  `Regex_belgium_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="204f6-139">Un mot clé `Keywords_belgium_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="204f6-139">A keyword from  `Keywords_belgium_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium__eu_passport_number" />
          <Match idRef="Keywords_belgium_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="204f6-140">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="204f6-140">Keywords</span></span>

<span data-ttu-id="204f6-141">| |</span><span class="sxs-lookup"><span data-stu-id="204f6-141"></span></span>
|<span data-ttu-id="204f6-142">**Keywords_belgium_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="204f6-142">**Keywords_belgium_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="204f6-143">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-143">passport number</span></span>  <br/> <span data-ttu-id="204f6-144">Numéro de passeport belge</span><span class="sxs-lookup"><span data-stu-id="204f6-144">belgian passport number</span></span>  <br/> <span data-ttu-id="204f6-145">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-145">passport no</span></span>  <br/> <span data-ttu-id="204f6-146">paspoort</span><span class="sxs-lookup"><span data-stu-id="204f6-146">paspoort</span></span>  <br/> <span data-ttu-id="204f6-147">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="204f6-147">paspoortnummer</span></span>  <br/> <span data-ttu-id="204f6-148">Reisepass kein</span><span class="sxs-lookup"><span data-stu-id="204f6-148">reisepass kein</span></span>  <br/> <span data-ttu-id="204f6-149">reisepass</span><span class="sxs-lookup"><span data-stu-id="204f6-149">reisepass</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="204f6-150">Bulgarie</span><span class="sxs-lookup"><span data-stu-id="204f6-150">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="204f6-151">Format</span><span class="sxs-lookup"><span data-stu-id="204f6-151">Format</span></span>

<span data-ttu-id="204f6-152">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="204f6-152">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="204f6-153">Modèle</span><span class="sxs-lookup"><span data-stu-id="204f6-153">Pattern</span></span>

 <span data-ttu-id="204f6-154">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="204f6-154">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="204f6-155">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="204f6-155">Checksum</span></span>

<span data-ttu-id="204f6-156">Non</span><span class="sxs-lookup"><span data-stu-id="204f6-156">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="204f6-157">Définition</span><span class="sxs-lookup"><span data-stu-id="204f6-157">Definition</span></span>

<span data-ttu-id="204f6-158">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="204f6-158">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="204f6-159">L'expression `Regex_bulgaria_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="204f6-159">The regular expression  `Regex_bulgaria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="204f6-160">Un mot clé `Keywords_bulgaria_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="204f6-160">A keyword from  `Keywords_bulgaria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_passport_number" />
          <Match idRef="Keywords_bulgaria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="204f6-161">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="204f6-161">Keywords</span></span>

<span data-ttu-id="204f6-162">| |</span><span class="sxs-lookup"><span data-stu-id="204f6-162"></span></span>
|<span data-ttu-id="204f6-163">**Keywords_bulgaria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="204f6-163">**Keywords_bulgaria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="204f6-164">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-164">passport number</span></span>  <br/> <span data-ttu-id="204f6-165">Numéro de Passeport bulgare</span><span class="sxs-lookup"><span data-stu-id="204f6-165">bulgarian passport number</span></span>  <br/> <span data-ttu-id="204f6-166">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-166">passport no</span></span>  <br/> <span data-ttu-id="204f6-167">номер на паспорта</span><span class="sxs-lookup"><span data-stu-id="204f6-167">номер на паспорта</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="204f6-168">Croatie</span><span class="sxs-lookup"><span data-stu-id="204f6-168">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="204f6-169">Format</span><span class="sxs-lookup"><span data-stu-id="204f6-169">Format</span></span>

<span data-ttu-id="204f6-170">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="204f6-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="204f6-171">Modèle</span><span class="sxs-lookup"><span data-stu-id="204f6-171">Pattern</span></span>

 <span data-ttu-id="204f6-172">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="204f6-172">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="204f6-173">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="204f6-173">Checksum</span></span>

<span data-ttu-id="204f6-174">Non</span><span class="sxs-lookup"><span data-stu-id="204f6-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="204f6-175">Définition</span><span class="sxs-lookup"><span data-stu-id="204f6-175">Definition</span></span>

<span data-ttu-id="204f6-176">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="204f6-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="204f6-177">L'expression `Regex_croatia_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="204f6-177">The regular expression  `Regex_croatia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="204f6-178">Un mot clé `Keywords_croatia_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="204f6-178">A keyword from  `Keywords_croatia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_passport_number" />
          <Match idRef="Keywords_croatia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="204f6-179">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="204f6-179">Keywords</span></span>

<span data-ttu-id="204f6-180">| |</span><span class="sxs-lookup"><span data-stu-id="204f6-180"></span></span>
|<span data-ttu-id="204f6-181">**Keywords_croatia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="204f6-181">**Keywords_croatia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="204f6-182">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-182">passport number</span></span>  <br/> <span data-ttu-id="204f6-183">Numéro de passeport croate</span><span class="sxs-lookup"><span data-stu-id="204f6-183">croatian passport number</span></span>  <br/> <span data-ttu-id="204f6-184">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-184">passport no</span></span>  <br/> <span data-ttu-id="204f6-185">Broj putovnice</span><span class="sxs-lookup"><span data-stu-id="204f6-185">broj putovnice</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="204f6-186">Chypre</span><span class="sxs-lookup"><span data-stu-id="204f6-186">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="204f6-187">Format</span><span class="sxs-lookup"><span data-stu-id="204f6-187">Format</span></span>

<span data-ttu-id="204f6-188">Une lettre suivie de 6-8 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="204f6-188">One letter followed by 6-8 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="204f6-189">Modèle</span><span class="sxs-lookup"><span data-stu-id="204f6-189">Pattern</span></span>

<span data-ttu-id="204f6-190">Une lettre suivie de six à huit chiffres</span><span class="sxs-lookup"><span data-stu-id="204f6-190">One letter followed by six to eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="204f6-191">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="204f6-191">Checksum</span></span>

<span data-ttu-id="204f6-192">Non</span><span class="sxs-lookup"><span data-stu-id="204f6-192">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="204f6-193">Définition</span><span class="sxs-lookup"><span data-stu-id="204f6-193">Definition</span></span>

<span data-ttu-id="204f6-194">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="204f6-194">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="204f6-195">L'expression `Regex_cyprus_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="204f6-195">The regular expression  `Regex_cyprus_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="204f6-196">Un mot clé `Keywords_cyprus_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="204f6-196">A keyword from  `Keywords_cyprus_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_passport_number" />
          <Match idRef="Keywords_cyprus_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="204f6-197">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="204f6-197">Keywords</span></span>

<span data-ttu-id="204f6-198">| |</span><span class="sxs-lookup"><span data-stu-id="204f6-198"></span></span>
|<span data-ttu-id="204f6-199">**Keywords_cyprus_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="204f6-199">**Keywords_cyprus_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="204f6-200">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-200">passport number</span></span>  <br/> <span data-ttu-id="204f6-201">Numéro de passeport de Chypre</span><span class="sxs-lookup"><span data-stu-id="204f6-201">cyprus passport number</span></span>  <br/> <span data-ttu-id="204f6-202">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-202">passport no</span></span>  <br/> <span data-ttu-id="204f6-203">αριθμό διαβατηρίου</span><span class="sxs-lookup"><span data-stu-id="204f6-203">αριθμό διαβατηρίου</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="204f6-204">République tchèque</span><span class="sxs-lookup"><span data-stu-id="204f6-204">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="204f6-205">Format</span><span class="sxs-lookup"><span data-stu-id="204f6-205">Format</span></span>

<span data-ttu-id="204f6-206">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="204f6-206">Eight digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="204f6-207">Modèle</span><span class="sxs-lookup"><span data-stu-id="204f6-207">Pattern</span></span>

<span data-ttu-id="204f6-208">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="204f6-208">Eight digits without spaces or delimiters</span></span>
  
### <a name="checksum"></a><span data-ttu-id="204f6-209">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="204f6-209">Checksum</span></span>

<span data-ttu-id="204f6-210">Non</span><span class="sxs-lookup"><span data-stu-id="204f6-210">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="204f6-211">Définition</span><span class="sxs-lookup"><span data-stu-id="204f6-211">Definition</span></span>

<span data-ttu-id="204f6-212">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="204f6-212">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="204f6-213">L'expression `Regex_czech_republic_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="204f6-213">The regular expression  `Regex_czech_republic_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="204f6-214">Un mot clé `Keywords_czech_republic_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="204f6-214">A keyword from  `Keywords_czech_republic_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_passport_number" />
          <Match idRef="Keywords_czech_republic_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="204f6-215">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="204f6-215">Keywords</span></span>

<span data-ttu-id="204f6-216">| |</span><span class="sxs-lookup"><span data-stu-id="204f6-216"></span></span>
|<span data-ttu-id="204f6-217">**Keywords_czech_republic_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="204f6-217">**Keywords_czech_republic_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="204f6-218">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-218">passport number</span></span>  <br/> <span data-ttu-id="204f6-219">Numéro de passeport tchèque</span><span class="sxs-lookup"><span data-stu-id="204f6-219">czech passport number</span></span>  <br/> <span data-ttu-id="204f6-220">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-220">passport no</span></span>  <br/> <span data-ttu-id="204f6-221">CESTOVNÍ pas</span><span class="sxs-lookup"><span data-stu-id="204f6-221">cestovní pas</span></span>  <br/> <span data-ttu-id="204f6-222">boîte</span><span class="sxs-lookup"><span data-stu-id="204f6-222">pas</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="204f6-223">Danemark</span><span class="sxs-lookup"><span data-stu-id="204f6-223">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="204f6-224">Format</span><span class="sxs-lookup"><span data-stu-id="204f6-224">Format</span></span>

<span data-ttu-id="204f6-225">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="204f6-225">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="204f6-226">Modèle</span><span class="sxs-lookup"><span data-stu-id="204f6-226">Pattern</span></span>

 <span data-ttu-id="204f6-227">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="204f6-227">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="204f6-228">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="204f6-228">Checksum</span></span>

<span data-ttu-id="204f6-229">Non</span><span class="sxs-lookup"><span data-stu-id="204f6-229">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="204f6-230">Définition</span><span class="sxs-lookup"><span data-stu-id="204f6-230">Definition</span></span>

<span data-ttu-id="204f6-231">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="204f6-231">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="204f6-232">L'expression `Regex_denmark_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="204f6-232">The regular expression  `Regex_denmark_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="204f6-233">Un mot clé `Keywords_denmark_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="204f6-233">A keyword from  `Keywords_denmark_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_passport_number" />
          <Match idRef="Keywords_denmark_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="204f6-234">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="204f6-234">Keywords</span></span>

<span data-ttu-id="204f6-235">| |</span><span class="sxs-lookup"><span data-stu-id="204f6-235"></span></span>
|<span data-ttu-id="204f6-236">**Keywords_denmark_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="204f6-236">**Keywords_denmark_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="204f6-237">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-237">passport number</span></span>  <br/> <span data-ttu-id="204f6-238">Numéro de passeport danois</span><span class="sxs-lookup"><span data-stu-id="204f6-238">danish passport number</span></span>  <br/> <span data-ttu-id="204f6-239">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-239">passport no</span></span>  <br/> <span data-ttu-id="204f6-240">boîte</span><span class="sxs-lookup"><span data-stu-id="204f6-240">pas</span></span>  <br/> <span data-ttu-id="204f6-241">pasnummer</span><span class="sxs-lookup"><span data-stu-id="204f6-241">pasnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="204f6-242">Estonie</span><span class="sxs-lookup"><span data-stu-id="204f6-242">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="204f6-243">Format</span><span class="sxs-lookup"><span data-stu-id="204f6-243">Format</span></span>

<span data-ttu-id="204f6-244">Une lettre suivie de sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="204f6-244">One letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="204f6-245">Modèle</span><span class="sxs-lookup"><span data-stu-id="204f6-245">Pattern</span></span>

<span data-ttu-id="204f6-246">Une lettre suivie de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="204f6-246">One letter followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="204f6-247">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="204f6-247">Checksum</span></span>

<span data-ttu-id="204f6-248">Non</span><span class="sxs-lookup"><span data-stu-id="204f6-248">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="204f6-249">Définition</span><span class="sxs-lookup"><span data-stu-id="204f6-249">Definition</span></span>

<span data-ttu-id="204f6-250">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="204f6-250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="204f6-251">L'expression `Regex_estonia_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="204f6-251">The regular expression  `Regex_estonia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="204f6-252">Un mot clé `Keywords_estonia_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="204f6-252">A keyword from  `Keywords_estonia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_passport_number" />
          <Match idRef="Keywords_estonia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="204f6-253">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="204f6-253">Keywords</span></span>

<span data-ttu-id="204f6-254">| |</span><span class="sxs-lookup"><span data-stu-id="204f6-254"></span></span>
|<span data-ttu-id="204f6-255">**Keywords_estonia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="204f6-255">**Keywords_estonia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="204f6-256">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-256">passport number</span></span>  <br/> <span data-ttu-id="204f6-257">Numéro de passeport estonien</span><span class="sxs-lookup"><span data-stu-id="204f6-257">estonian passport number</span></span>  <br/> <span data-ttu-id="204f6-258">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-258">passport no</span></span>  <br/> <span data-ttu-id="204f6-259">Eesti kodaniku</span><span class="sxs-lookup"><span data-stu-id="204f6-259">eesti kodaniku pass</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="204f6-260">Finlande</span><span class="sxs-lookup"><span data-stu-id="204f6-260">Finland</span></span>

<span data-ttu-id="204f6-261">Pour plus d'informations, consultez la section «numéro de passeport de Finlande» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="204f6-261">For details, see the section "Finland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="204f6-262">France</span><span class="sxs-lookup"><span data-stu-id="204f6-262">France</span></span>

<span data-ttu-id="204f6-263">Pour plus d'informations, consultez la section «numéro de passeport français» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="204f6-263">For details, see the section "France Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="204f6-264">Allemagne</span><span class="sxs-lookup"><span data-stu-id="204f6-264">Germany</span></span>

<span data-ttu-id="204f6-265">Pour plus d'informations, reportez-vous à la section «numéro de passeport allemand» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="204f6-265">For details, see the section "Germany Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="204f6-266">Grèce</span><span class="sxs-lookup"><span data-stu-id="204f6-266">Greece</span></span>

### <a name="format"></a><span data-ttu-id="204f6-267">Format</span><span class="sxs-lookup"><span data-stu-id="204f6-267">Format</span></span>

<span data-ttu-id="204f6-268">Deux lettres suivies de sept chiffres, sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="204f6-268">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="204f6-269">Modèle</span><span class="sxs-lookup"><span data-stu-id="204f6-269">Pattern</span></span>

<span data-ttu-id="204f6-270">Deux lettres suivies de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="204f6-270">Two letters followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="204f6-271">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="204f6-271">Checksum</span></span>

<span data-ttu-id="204f6-272">Non</span><span class="sxs-lookup"><span data-stu-id="204f6-272">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="204f6-273">Définition</span><span class="sxs-lookup"><span data-stu-id="204f6-273">Definition</span></span>

<span data-ttu-id="204f6-274">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="204f6-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="204f6-275">L'expression `Regex_greece_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="204f6-275">The regular expression  `Regex_greece_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="204f6-276">Un mot clé `Keywords_greece_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="204f6-276">A keyword from  `Keywords_greece_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_passport_number" />
          <Match idRef="Keywords_greece_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="204f6-277">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="204f6-277">Keywords</span></span>

<span data-ttu-id="204f6-278">| |</span><span class="sxs-lookup"><span data-stu-id="204f6-278"></span></span>
|<span data-ttu-id="204f6-279">**Keywords_greece_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="204f6-279">**Keywords_greece_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="204f6-280">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-280">passport number</span></span>  <br/> <span data-ttu-id="204f6-281">Numéro de passeport grec</span><span class="sxs-lookup"><span data-stu-id="204f6-281">greek passport number</span></span>  <br/> <span data-ttu-id="204f6-282">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-282">passport no</span></span>  <br/> <span data-ttu-id="204f6-283">διαβατηριο</span><span class="sxs-lookup"><span data-stu-id="204f6-283">διαβατηριο</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="204f6-284">Hongrie</span><span class="sxs-lookup"><span data-stu-id="204f6-284">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="204f6-285">Format</span><span class="sxs-lookup"><span data-stu-id="204f6-285">Format</span></span>

<span data-ttu-id="204f6-286">Deux lettres suivies de six ou sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="204f6-286">Two letters followed by six or seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="204f6-287">Modèle</span><span class="sxs-lookup"><span data-stu-id="204f6-287">Pattern</span></span>

<span data-ttu-id="204f6-288">Deux lettres suivies de six ou sept chiffres</span><span class="sxs-lookup"><span data-stu-id="204f6-288">Two letters followed by six or seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="204f6-289">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="204f6-289">Checksum</span></span>

<span data-ttu-id="204f6-290">Non</span><span class="sxs-lookup"><span data-stu-id="204f6-290">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="204f6-291">Définition</span><span class="sxs-lookup"><span data-stu-id="204f6-291">Definition</span></span>

<span data-ttu-id="204f6-292">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="204f6-292">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="204f6-293">L'expression `Regex_hungary_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="204f6-293">The regular expression  `Regex_hungary_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="204f6-294">Un mot clé `Keywords_hungary_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="204f6-294">A keyword from  `Keywords_hungary_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_passport_number" />
          <Match idRef="Keywords_hungary_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="204f6-295">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="204f6-295">Keywords</span></span>

<span data-ttu-id="204f6-296">| |</span><span class="sxs-lookup"><span data-stu-id="204f6-296"></span></span>
|<span data-ttu-id="204f6-297">**Keywords_hungary_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="204f6-297">**Keywords_hungary_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="204f6-298">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-298">passport number</span></span>  <br/> <span data-ttu-id="204f6-299">Numéro de passeport hongrois</span><span class="sxs-lookup"><span data-stu-id="204f6-299">hungarian passport number</span></span>  <br/> <span data-ttu-id="204f6-300">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-300">passport no</span></span>  <br/> <span data-ttu-id="204f6-301">útlevél száma</span><span class="sxs-lookup"><span data-stu-id="204f6-301">útlevél száma</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="204f6-302">Irlande</span><span class="sxs-lookup"><span data-stu-id="204f6-302">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="204f6-303">Format</span><span class="sxs-lookup"><span data-stu-id="204f6-303">Format</span></span>

<span data-ttu-id="204f6-304">Deux lettres ou chiffres suivis de sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="204f6-304">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="204f6-305">Modèle</span><span class="sxs-lookup"><span data-stu-id="204f6-305">Pattern</span></span>

<span data-ttu-id="204f6-306">Deux lettres ou chiffres suivis de sept chiffres:</span><span class="sxs-lookup"><span data-stu-id="204f6-306">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="204f6-307">Deux chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="204f6-307">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="204f6-308">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="204f6-308">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="204f6-309">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="204f6-309">Checksum</span></span>

<span data-ttu-id="204f6-310">Non</span><span class="sxs-lookup"><span data-stu-id="204f6-310">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="204f6-311">Définition</span><span class="sxs-lookup"><span data-stu-id="204f6-311">Definition</span></span>

<span data-ttu-id="204f6-312">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="204f6-312">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="204f6-313">L'expression `Regex_ireland_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="204f6-313">The regular expression  `Regex_ireland_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="204f6-314">Un mot clé `Keywords_ireland_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="204f6-314">A keyword from  `Keywords_ireland_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_passport_number" />
          <Match idRef="Keywords_ireland_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="204f6-315">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="204f6-315">Keywords</span></span>

<span data-ttu-id="204f6-316">| |</span><span class="sxs-lookup"><span data-stu-id="204f6-316"></span></span>
|<span data-ttu-id="204f6-317">**Keywords_ireland_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="204f6-317">**Keywords_ireland_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="204f6-318">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-318">passport number</span></span>  <br/> <span data-ttu-id="204f6-319">Numéro de passeport irlandais</span><span class="sxs-lookup"><span data-stu-id="204f6-319">irish passport number</span></span>  <br/> <span data-ttu-id="204f6-320">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-320">passport no</span></span>  <br/> <span data-ttu-id="204f6-321">boîte</span><span class="sxs-lookup"><span data-stu-id="204f6-321">pas</span></span>  <br/> <span data-ttu-id="204f6-322">passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-322">passport</span></span>  <br/> <span data-ttu-id="204f6-323">passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-323">passeport</span></span>  <br/> <span data-ttu-id="204f6-324">passeport numérique</span><span class="sxs-lookup"><span data-stu-id="204f6-324">passeport numero</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="204f6-325">Italie</span><span class="sxs-lookup"><span data-stu-id="204f6-325">Italy</span></span>

### <a name="format"></a><span data-ttu-id="204f6-326">Format</span><span class="sxs-lookup"><span data-stu-id="204f6-326">Format</span></span>

<span data-ttu-id="204f6-327">Deux lettres ou chiffres suivis de sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="204f6-327">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="204f6-328">Modèle</span><span class="sxs-lookup"><span data-stu-id="204f6-328">Pattern</span></span>

<span data-ttu-id="204f6-329">Deux lettres ou chiffres suivis de sept chiffres:</span><span class="sxs-lookup"><span data-stu-id="204f6-329">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="204f6-330">Deux chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="204f6-330">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="204f6-331">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="204f6-331">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="204f6-332">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="204f6-332">Checksum</span></span>

<span data-ttu-id="204f6-333">Non applicable</span><span class="sxs-lookup"><span data-stu-id="204f6-333">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="204f6-334">Définition</span><span class="sxs-lookup"><span data-stu-id="204f6-334">Definition</span></span>

<span data-ttu-id="204f6-335">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="204f6-335">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="204f6-336">L'expression `Regex_italy_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="204f6-336">The regular expression  `Regex_italy_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="204f6-337">Un mot clé `Keywords_italy_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="204f6-337">A keyword from  `Keywords_italy_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_passport_number" />
          <Match idRef="Keywords_italy_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="204f6-338">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="204f6-338">Keywords</span></span>

<span data-ttu-id="204f6-339">| |</span><span class="sxs-lookup"><span data-stu-id="204f6-339"></span></span>
|<span data-ttu-id="204f6-340">**Keywords_italy_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="204f6-340">**Keywords_italy_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="204f6-341">Numéro de passeport italien</span><span class="sxs-lookup"><span data-stu-id="204f6-341">italian passport number</span></span>  <br/> <span data-ttu-id="204f6-342">Repubblica Italiana passaporto</span><span class="sxs-lookup"><span data-stu-id="204f6-342">repubblica italiana passaporto</span></span>  <br/> <span data-ttu-id="204f6-343">passaporto</span><span class="sxs-lookup"><span data-stu-id="204f6-343">passaporto</span></span>  <br/> <span data-ttu-id="204f6-344">passaporto Italiana</span><span class="sxs-lookup"><span data-stu-id="204f6-344">passaporto italiana</span></span>  <br/> <span data-ttu-id="204f6-345">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-345">passport number</span></span>  <br/> <span data-ttu-id="204f6-346">Italiana passaporto numérique</span><span class="sxs-lookup"><span data-stu-id="204f6-346">italiana passaporto numero</span></span>  <br/> <span data-ttu-id="204f6-347">passaporto numérique</span><span class="sxs-lookup"><span data-stu-id="204f6-347">passaporto numero</span></span>  <br/> <span data-ttu-id="204f6-348">numéro passeport italien</span><span class="sxs-lookup"><span data-stu-id="204f6-348">numéro passeport italien</span></span>  <br/> <span data-ttu-id="204f6-349">numéro passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-349">numéro passeport</span></span>  <br/> |
   
## <a name="latvia"></a><span data-ttu-id="204f6-350">Lettonie</span><span class="sxs-lookup"><span data-stu-id="204f6-350">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="204f6-351">Format</span><span class="sxs-lookup"><span data-stu-id="204f6-351">Format</span></span>

<span data-ttu-id="204f6-352">Deux lettres ou chiffres suivis de sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="204f6-352">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="204f6-353">Modèle</span><span class="sxs-lookup"><span data-stu-id="204f6-353">Pattern</span></span>

<span data-ttu-id="204f6-354">Deux lettres ou chiffres suivis de sept chiffres:</span><span class="sxs-lookup"><span data-stu-id="204f6-354">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="204f6-355">Deux chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="204f6-355">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="204f6-356">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="204f6-356">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="204f6-357">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="204f6-357">Checksum</span></span>

<span data-ttu-id="204f6-358">Non</span><span class="sxs-lookup"><span data-stu-id="204f6-358">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="204f6-359">Définition</span><span class="sxs-lookup"><span data-stu-id="204f6-359">Definition</span></span>

<span data-ttu-id="204f6-360">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="204f6-360">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="204f6-361">L'expression `Regex_latvia_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="204f6-361">The regular expression  `Regex_latvia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="204f6-362">Un mot clé `Keywords_latvia_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="204f6-362">A keyword from  `Keywords_latvia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_passport_number" />
          <Match idRef="Keywords_latvia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="204f6-363">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="204f6-363">Keywords</span></span>

<span data-ttu-id="204f6-364">| |</span><span class="sxs-lookup"><span data-stu-id="204f6-364"></span></span>
|<span data-ttu-id="204f6-365">**Keywords_latvia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="204f6-365">**Keywords_latvia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="204f6-366">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-366">passport number</span></span>  <br/> <span data-ttu-id="204f6-367">Numéro de passeport letton</span><span class="sxs-lookup"><span data-stu-id="204f6-367">latvian passport number</span></span>  <br/> <span data-ttu-id="204f6-368">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-368">passport no</span></span>  <br/> <span data-ttu-id="204f6-369">pase numurs</span><span class="sxs-lookup"><span data-stu-id="204f6-369">pase numurs</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="204f6-370">Lituanie</span><span class="sxs-lookup"><span data-stu-id="204f6-370">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="204f6-371">Format</span><span class="sxs-lookup"><span data-stu-id="204f6-371">Format</span></span>

<span data-ttu-id="204f6-372">Huit chiffres ou lettres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="204f6-372">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="204f6-373">Modèle</span><span class="sxs-lookup"><span data-stu-id="204f6-373">Pattern</span></span>

<span data-ttu-id="204f6-374">Huit chiffres ou lettres (ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="204f6-374">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="204f6-375">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="204f6-375">Checksum</span></span>

<span data-ttu-id="204f6-376">Non applicable</span><span class="sxs-lookup"><span data-stu-id="204f6-376">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="204f6-377">Définition</span><span class="sxs-lookup"><span data-stu-id="204f6-377">Definition</span></span>

<span data-ttu-id="204f6-378">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="204f6-378">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="204f6-379">L'expression `Regex_lithuania_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="204f6-379">The regular expression  `Regex_lithuania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="204f6-380">Un mot clé `Keywords_lithuania_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="204f6-380">A keyword from  `Keywords_lithuania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_passport_number" />
          <Match idRef="Keywords_lithuania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="204f6-381">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="204f6-381">Keywords</span></span>

<span data-ttu-id="204f6-382">| |</span><span class="sxs-lookup"><span data-stu-id="204f6-382"></span></span>
|<span data-ttu-id="204f6-383">**Keywords_lithuania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="204f6-383">**Keywords_lithuania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="204f6-384">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-384">passport number</span></span>  <br/> <span data-ttu-id="204f6-385">Numéro de passeport lithunian</span><span class="sxs-lookup"><span data-stu-id="204f6-385">lithunian passport number</span></span>  <br/> <span data-ttu-id="204f6-386">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-386">passport no</span></span>  <br/> <span data-ttu-id="204f6-387">Paso chiffres</span><span class="sxs-lookup"><span data-stu-id="204f6-387">paso numeris</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="204f6-388">Relatif</span><span class="sxs-lookup"><span data-stu-id="204f6-388">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="204f6-389">Format</span><span class="sxs-lookup"><span data-stu-id="204f6-389">Format</span></span>

<span data-ttu-id="204f6-390">Huit chiffres ou lettres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="204f6-390">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="204f6-391">Modèle</span><span class="sxs-lookup"><span data-stu-id="204f6-391">Pattern</span></span>

<span data-ttu-id="204f6-392">Huit chiffres ou lettres (ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="204f6-392">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="204f6-393">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="204f6-393">Checksum</span></span>

<span data-ttu-id="204f6-394">Non</span><span class="sxs-lookup"><span data-stu-id="204f6-394">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="204f6-395">Définition</span><span class="sxs-lookup"><span data-stu-id="204f6-395">Definition</span></span>

<span data-ttu-id="204f6-396">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="204f6-396">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="204f6-397">L'expression `Regex_nation_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="204f6-397">The regular expression  `Regex_nation_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="204f6-398">Un mot clé `Keywords_nation_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="204f6-398">A keyword from  `Keywords_nation_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_nation_eu_passport_number" />
          <Match idRef="Keywords_nation_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="204f6-399">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="204f6-399">Keywords</span></span>

<span data-ttu-id="204f6-400">| |</span><span class="sxs-lookup"><span data-stu-id="204f6-400"></span></span>
|<span data-ttu-id="204f6-401">**Keywords_nation_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="204f6-401">**Keywords_nation_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="204f6-402">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-402">passport number</span></span>  <br/> <span data-ttu-id="204f6-403">Numéro de passeport letton</span><span class="sxs-lookup"><span data-stu-id="204f6-403">latvian passport number</span></span>  <br/> <span data-ttu-id="204f6-404">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-404">passport no</span></span>  <br/> <span data-ttu-id="204f6-405">passnummer</span><span class="sxs-lookup"><span data-stu-id="204f6-405">passnummer</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="204f6-406">Malte</span><span class="sxs-lookup"><span data-stu-id="204f6-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="204f6-407">Format</span><span class="sxs-lookup"><span data-stu-id="204f6-407">Format</span></span>

<span data-ttu-id="204f6-408">Sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="204f6-408">Seven digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="204f6-409">Modèle</span><span class="sxs-lookup"><span data-stu-id="204f6-409">Pattern</span></span>

 <span data-ttu-id="204f6-410">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="204f6-410">Seven digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="204f6-411">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="204f6-411">Checksum</span></span>

<span data-ttu-id="204f6-412">Non</span><span class="sxs-lookup"><span data-stu-id="204f6-412">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="204f6-413">Définition</span><span class="sxs-lookup"><span data-stu-id="204f6-413">Definition</span></span>

<span data-ttu-id="204f6-414">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="204f6-414">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="204f6-415">L'expression `Regex_malta_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="204f6-415">The regular expression  `Regex_malta_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="204f6-416">Un mot clé `Keywords_malta_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="204f6-416">A keyword from  `Keywords_malta_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_passport_number" />
          <Match idRef="Keywords_malta_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="204f6-417">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="204f6-417">Keywords</span></span>

<span data-ttu-id="204f6-418">| |</span><span class="sxs-lookup"><span data-stu-id="204f6-418"></span></span>
|<span data-ttu-id="204f6-419">**Keywords_malta_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="204f6-419">**Keywords_malta_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="204f6-420">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-420">passport number</span></span>  <br/> <span data-ttu-id="204f6-421">Numéro de passeport maltais</span><span class="sxs-lookup"><span data-stu-id="204f6-421">maltese passport number</span></span>  <br/> <span data-ttu-id="204f6-422">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-422">passport no</span></span>  <br/> <span data-ttu-id="204f6-423">numru Tal-Passaport</span><span class="sxs-lookup"><span data-stu-id="204f6-423">numru tal-passaport</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="204f6-424">Pays-Bas</span><span class="sxs-lookup"><span data-stu-id="204f6-424">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="204f6-425">Format</span><span class="sxs-lookup"><span data-stu-id="204f6-425">Format</span></span>

<span data-ttu-id="204f6-426">Neuf lettres ou chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="204f6-426">Nine letters or digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="204f6-427">Modèle</span><span class="sxs-lookup"><span data-stu-id="204f6-427">Pattern</span></span>

<span data-ttu-id="204f6-428">Neuf lettres ou chiffres</span><span class="sxs-lookup"><span data-stu-id="204f6-428">Nine letters or digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="204f6-429">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="204f6-429">Checksum</span></span>

<span data-ttu-id="204f6-430">Non applicable</span><span class="sxs-lookup"><span data-stu-id="204f6-430">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="204f6-431">Définition</span><span class="sxs-lookup"><span data-stu-id="204f6-431">Definition</span></span>

<span data-ttu-id="204f6-432">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="204f6-432">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="204f6-433">L'expression `Regex_netherlands_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="204f6-433">The regular expression  `Regex_netherlands_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="204f6-434">Un mot clé `Keywords_netherlands_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="204f6-434">A keyword from  `Keywords_netherlands_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_passport_number" />
          <Match idRef="Keywords_netherlands_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="204f6-435">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="204f6-435">Keywords</span></span>

<span data-ttu-id="204f6-436">| |</span><span class="sxs-lookup"><span data-stu-id="204f6-436"></span></span>
|<span data-ttu-id="204f6-437">**Keywords_netherlands_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="204f6-437">**Keywords_netherlands_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="204f6-438">Numéro de passeport néerlandais</span><span class="sxs-lookup"><span data-stu-id="204f6-438">dutch passport number</span></span>  <br/> <span data-ttu-id="204f6-439">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-439">passport number</span></span>  <br/> <span data-ttu-id="204f6-440">Numéro de passeport néerlandais</span><span class="sxs-lookup"><span data-stu-id="204f6-440">netherlands passport number</span></span>  <br/> <span data-ttu-id="204f6-441">Nederlanden paspoort Nummer</span><span class="sxs-lookup"><span data-stu-id="204f6-441">nederlanden paspoort nummer</span></span>  <br/> <span data-ttu-id="204f6-442">paspoort</span><span class="sxs-lookup"><span data-stu-id="204f6-442">paspoort</span></span>  <br/> <span data-ttu-id="204f6-443">Nederlanden paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="204f6-443">nederlanden paspoortnummer</span></span>  <br/> <span data-ttu-id="204f6-444">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="204f6-444">paspoortnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="204f6-445">Pologne</span><span class="sxs-lookup"><span data-stu-id="204f6-445">Poland</span></span>

<span data-ttu-id="204f6-446">Pour plus d'informations, reportez-vous à la section «numéro de passeport polonais» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="204f6-446">For details, see the section "Poland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="204f6-447">Portugal</span><span class="sxs-lookup"><span data-stu-id="204f6-447">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="204f6-448">Format</span><span class="sxs-lookup"><span data-stu-id="204f6-448">Format</span></span>

<span data-ttu-id="204f6-449">Une lettre suivie de six chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="204f6-449">One letter followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="204f6-450">Modèle</span><span class="sxs-lookup"><span data-stu-id="204f6-450">Pattern</span></span>

<span data-ttu-id="204f6-451">Une lettre suivie de six chiffres:</span><span class="sxs-lookup"><span data-stu-id="204f6-451">One letter followed by six digits:</span></span>
  
- <span data-ttu-id="204f6-452">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="204f6-452">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="204f6-453">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="204f6-453">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="204f6-454">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="204f6-454">Checksum</span></span>

<span data-ttu-id="204f6-455">Non</span><span class="sxs-lookup"><span data-stu-id="204f6-455">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="204f6-456">Définition</span><span class="sxs-lookup"><span data-stu-id="204f6-456">Definition</span></span>

<span data-ttu-id="204f6-457">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="204f6-457">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="204f6-458">L'expression `Regex_portugal_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="204f6-458">The regular expression  `Regex_portugal_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="204f6-459">Un mot clé `Keywords_portugal_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="204f6-459">A keyword from  `Keywords_portugal_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_passport_number" />
          <Match idRef="Keywords_portugal_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="204f6-460">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="204f6-460">Keywords</span></span>

<span data-ttu-id="204f6-461">| |</span><span class="sxs-lookup"><span data-stu-id="204f6-461"></span></span>
|<span data-ttu-id="204f6-462">**Keywords_portugal_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="204f6-462">**Keywords_portugal_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="204f6-463">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-463">passport number</span></span>  <br/> <span data-ttu-id="204f6-464">Numéro de passeport Portugais</span><span class="sxs-lookup"><span data-stu-id="204f6-464">portuguese passport number</span></span>  <br/> <span data-ttu-id="204f6-465">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-465">passport no</span></span>  <br/> <span data-ttu-id="204f6-466">número do Passaporte</span><span class="sxs-lookup"><span data-stu-id="204f6-466">número do passaporte</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="204f6-467">Roumanie</span><span class="sxs-lookup"><span data-stu-id="204f6-467">Romania</span></span>

### <a name="format"></a><span data-ttu-id="204f6-468">Format</span><span class="sxs-lookup"><span data-stu-id="204f6-468">Format</span></span>

<span data-ttu-id="204f6-469">Huit ou neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="204f6-469">Eight or nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="204f6-470">Modèle</span><span class="sxs-lookup"><span data-stu-id="204f6-470">Pattern</span></span>

<span data-ttu-id="204f6-471">Huit ou neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="204f6-471">Eight or nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="204f6-472">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="204f6-472">Checksum</span></span>

<span data-ttu-id="204f6-473">Non</span><span class="sxs-lookup"><span data-stu-id="204f6-473">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="204f6-474">Définition</span><span class="sxs-lookup"><span data-stu-id="204f6-474">Definition</span></span>

<span data-ttu-id="204f6-475">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="204f6-475">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="204f6-476">L'expression `Regex_romania_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="204f6-476">The regular expression  `Regex_romania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="204f6-477">Un mot clé `Keywords_romania_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="204f6-477">A keyword from  `Keywords_romania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_passport_number" />
          <Match idRef="Keywords_romania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="204f6-478">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="204f6-478">Keywords</span></span>

<span data-ttu-id="204f6-479">| |</span><span class="sxs-lookup"><span data-stu-id="204f6-479"></span></span>
|<span data-ttu-id="204f6-480">**Keywords_romania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="204f6-480">**Keywords_romania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="204f6-481">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-481">passport number</span></span>  <br/> <span data-ttu-id="204f6-482">Numéro de passeport roumain</span><span class="sxs-lookup"><span data-stu-id="204f6-482">romanian passport number</span></span>  <br/> <span data-ttu-id="204f6-483">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-483">passport no</span></span>  <br/> <span data-ttu-id="204f6-484">numărul pașaportului</span><span class="sxs-lookup"><span data-stu-id="204f6-484">numărul pașaportului</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="204f6-485">République de Slovaquie</span><span class="sxs-lookup"><span data-stu-id="204f6-485">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="204f6-486">Format</span><span class="sxs-lookup"><span data-stu-id="204f6-486">Format</span></span>

<span data-ttu-id="204f6-487">Un chiffre ou une lettre suivi de sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="204f6-487">One digit or letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="204f6-488">Modèle</span><span class="sxs-lookup"><span data-stu-id="204f6-488">Pattern</span></span>

<span data-ttu-id="204f6-489">Un chiffre ou une lettre (ne respectant pas la casse) suivi de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="204f6-489">One digit or letter (not case sensitive) followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="204f6-490">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="204f6-490">Checksum</span></span>

<span data-ttu-id="204f6-491">Non</span><span class="sxs-lookup"><span data-stu-id="204f6-491">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="204f6-492">Définition</span><span class="sxs-lookup"><span data-stu-id="204f6-492">Definition</span></span>

<span data-ttu-id="204f6-493">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="204f6-493">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="204f6-494">L'expression `Regex_slovakia_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="204f6-494">The regular expression  `Regex_slovakia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="204f6-495">Un mot clé `Keywords_slovakia_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="204f6-495">A keyword from  `Keywords_slovakia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_passport_number" />
          <Match idRef="Keywords_slovakia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="204f6-496">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="204f6-496">Keywords</span></span>

<span data-ttu-id="204f6-497">| |</span><span class="sxs-lookup"><span data-stu-id="204f6-497"></span></span>
|<span data-ttu-id="204f6-498">**Keywords_slovakia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="204f6-498">**Keywords_slovakia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="204f6-499">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-499">passport number</span></span>  <br/> <span data-ttu-id="204f6-500">Numéro de passeport slovaque</span><span class="sxs-lookup"><span data-stu-id="204f6-500">slovakian passport number</span></span>  <br/> <span data-ttu-id="204f6-501">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-501">passport no</span></span>  <br/> <span data-ttu-id="204f6-502">číslo Pasu</span><span class="sxs-lookup"><span data-stu-id="204f6-502">číslo pasu</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="204f6-503">Slovénie</span><span class="sxs-lookup"><span data-stu-id="204f6-503">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="204f6-504">Format</span><span class="sxs-lookup"><span data-stu-id="204f6-504">Format</span></span>

<span data-ttu-id="204f6-505">Deux lettres suivies de sept chiffres, sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="204f6-505">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="204f6-506">Modèle</span><span class="sxs-lookup"><span data-stu-id="204f6-506">Pattern</span></span>

<span data-ttu-id="204f6-507">Deux lettres suivies de sept chiffres:</span><span class="sxs-lookup"><span data-stu-id="204f6-507">Two letters followed by seven digits:</span></span>
  
- <span data-ttu-id="204f6-508">La lettre «P»</span><span class="sxs-lookup"><span data-stu-id="204f6-508">The letter "P"</span></span>
    
- <span data-ttu-id="204f6-509">Une lettre majuscule</span><span class="sxs-lookup"><span data-stu-id="204f6-509">One uppercase letter</span></span>
    
- <span data-ttu-id="204f6-510">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="204f6-510">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="204f6-511">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="204f6-511">Checksum</span></span>

<span data-ttu-id="204f6-512">Non</span><span class="sxs-lookup"><span data-stu-id="204f6-512">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="204f6-513">Définition</span><span class="sxs-lookup"><span data-stu-id="204f6-513">Definition</span></span>

<span data-ttu-id="204f6-514">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="204f6-514">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="204f6-515">L'expression `Regex_slovenia_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="204f6-515">The regular expression  `Regex_slovenia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="204f6-516">Un mot clé `Keywords_slovenia_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="204f6-516">A keyword from  `Keywords_slovenia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_passport_number" />
          <Match idRef="Keywords_slovenia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="204f6-517">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="204f6-517">Keywords</span></span>

<span data-ttu-id="204f6-518">| |</span><span class="sxs-lookup"><span data-stu-id="204f6-518"></span></span>
|<span data-ttu-id="204f6-519">**Keywords_slovenia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="204f6-519">**Keywords_slovenia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="204f6-520">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-520">passport number</span></span>  <br/> <span data-ttu-id="204f6-521">Numéro de passeport slovène</span><span class="sxs-lookup"><span data-stu-id="204f6-521">slovenian passport number</span></span>  <br/> <span data-ttu-id="204f6-522">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-522">passport no</span></span>  <br/> <span data-ttu-id="204f6-523">številka potnega Lista</span><span class="sxs-lookup"><span data-stu-id="204f6-523">številka potnega lista</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="204f6-524">Espagne</span><span class="sxs-lookup"><span data-stu-id="204f6-524">Spain</span></span>

### <a name="format"></a><span data-ttu-id="204f6-525">Format</span><span class="sxs-lookup"><span data-stu-id="204f6-525">Format</span></span>

<span data-ttu-id="204f6-526">Combinaison de huit ou neuf caractères de lettres et de chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="204f6-526">An eight- or nine-character combination of letters and numbers with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="204f6-527">Modèle</span><span class="sxs-lookup"><span data-stu-id="204f6-527">Pattern</span></span>

<span data-ttu-id="204f6-528">Combinaison de huit ou neuf caractères de lettres et de chiffres:</span><span class="sxs-lookup"><span data-stu-id="204f6-528">An eight- or nine-character combination of letters and numbers:</span></span>
  
-  <span data-ttu-id="204f6-529">Deux chiffres ou lettres</span><span class="sxs-lookup"><span data-stu-id="204f6-529">Two digits or letters</span></span> 
    
- <span data-ttu-id="204f6-530">Un chiffre ou une lettre (facultatif)</span><span class="sxs-lookup"><span data-stu-id="204f6-530">One digit or letter (optional)</span></span>
    
- <span data-ttu-id="204f6-531">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="204f6-531">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="204f6-532">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="204f6-532">Checksum</span></span>

<span data-ttu-id="204f6-533">Non applicable</span><span class="sxs-lookup"><span data-stu-id="204f6-533">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="204f6-534">Définition</span><span class="sxs-lookup"><span data-stu-id="204f6-534">Definition</span></span>

<span data-ttu-id="204f6-535">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="204f6-535">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="204f6-536">L'expression `Regex_spain_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="204f6-536">The regular expression  `Regex_spain_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="204f6-537">Un mot clé `Keywords_spain_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="204f6-537">A keyword from  `Keywords_spain_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_passport_number" />
          <Match idRef="Keywords_spain_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="204f6-538">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="204f6-538">Keywords</span></span>

<span data-ttu-id="204f6-539">| |</span><span class="sxs-lookup"><span data-stu-id="204f6-539"></span></span>
|<span data-ttu-id="204f6-540">**Keywords_spain_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="204f6-540">**Keywords_spain_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="204f6-541">passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-541">passport</span></span>  <br/> <span data-ttu-id="204f6-542">Passport Espagne</span><span class="sxs-lookup"><span data-stu-id="204f6-542">spain passport</span></span>  <br/> <span data-ttu-id="204f6-543">livre de passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-543">passport book</span></span>  <br/> <span data-ttu-id="204f6-544">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-544">passport number</span></span>  <br/> <span data-ttu-id="204f6-545">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="204f6-545">passport no</span></span>  <br/> <span data-ttu-id="204f6-546">Libreta pasaporte</span><span class="sxs-lookup"><span data-stu-id="204f6-546">libreta pasaporte</span></span>  <br/> <span data-ttu-id="204f6-547">número pasaporte</span><span class="sxs-lookup"><span data-stu-id="204f6-547">número pasaporte</span></span>  <br/> <span data-ttu-id="204f6-548">España pasaporte</span><span class="sxs-lookup"><span data-stu-id="204f6-548">españa pasaporte</span></span>  <br/> <span data-ttu-id="204f6-549">pasaporte</span><span class="sxs-lookup"><span data-stu-id="204f6-549">pasaporte</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="204f6-550">Suède</span><span class="sxs-lookup"><span data-stu-id="204f6-550">Sweden</span></span>

<span data-ttu-id="204f6-551">Pour plus d'informations, reportez-vous à la section «numéro de passeport Suède» dans [ce que recherche les types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="204f6-551">For details, see the section "Sweden Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="uk"></a><span data-ttu-id="204f6-552">R.U.</span><span class="sxs-lookup"><span data-stu-id="204f6-552">UK</span></span>

<span data-ttu-id="204f6-p103">Pour plus d'informations, reportez-vous à la section «US/numéro de passeport britannique» dans les [types d'informations sensibles que vous recherchez](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="204f6-p103">For details, see the section "U.S. / U.K. Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="204f6-555">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="204f6-555">See also</span></span>

[<span data-ttu-id="204f6-556">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="204f6-556">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

