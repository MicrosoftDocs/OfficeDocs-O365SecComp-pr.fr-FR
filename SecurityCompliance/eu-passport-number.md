---
title: Numéro de passeport UE
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/16/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: Cette rubrique présente ce qu'une stratégie de protection contre la perte de données (DLP) recherche lorsqu'elle détecte le type d'informations sensibles du numéro de passeport de l'UE. Ce type d'informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.
ms.openlocfilehash: 3ab92e87607f41cffa8c15f1179a4eef5369cb29
ms.sourcegitcommit: ed822a776d3419853453583e882f3c61ca26d4b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "30410929"
---
# <a name="eu-passport-number"></a><span data-ttu-id="d567c-104">Numéro de passeport UE</span><span class="sxs-lookup"><span data-stu-id="d567c-104">EU Passport Number</span></span>

<span data-ttu-id="d567c-105">Cette rubrique présente ce qu'une stratégie de protection contre la perte de données (DLP) recherche lorsqu'elle détecte le type d'informations sensibles du numéro de passeport de l'UE.</span><span class="sxs-lookup"><span data-stu-id="d567c-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Passport Number sensitive information type.</span></span> <span data-ttu-id="d567c-106">Ce type d'informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.</span><span class="sxs-lookup"><span data-stu-id="d567c-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="d567c-107">Autriche</span><span class="sxs-lookup"><span data-stu-id="d567c-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="d567c-108">Format</span><span class="sxs-lookup"><span data-stu-id="d567c-108">Format</span></span>

<span data-ttu-id="d567c-109">Une lettre suivie d'un espace facultatif et de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="d567c-109">One letter followed by an optional space and seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d567c-110">Modèle</span><span class="sxs-lookup"><span data-stu-id="d567c-110">Pattern</span></span>

<span data-ttu-id="d567c-111">Une combinaison d'une lettre, de sept chiffres et d'un espace:</span><span class="sxs-lookup"><span data-stu-id="d567c-111">A combination of one letter, seven digits, and one space:</span></span>
  
- <span data-ttu-id="d567c-112">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="d567c-112">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="d567c-113">Un espace (facultatif)</span><span class="sxs-lookup"><span data-stu-id="d567c-113">One space (optional)</span></span>
    
- <span data-ttu-id="d567c-114">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="d567c-114">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d567c-115">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d567c-115">Checksum</span></span>

<span data-ttu-id="d567c-116">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d567c-116">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d567c-117">Définition</span><span class="sxs-lookup"><span data-stu-id="d567c-117">Definition</span></span>

<span data-ttu-id="d567c-118">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d567c-118">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d567c-119">L'expression `Regex_austria_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d567c-119">The regular expression  `Regex_austria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d567c-120">Un mot clé `Keywords_austria_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d567c-120">A keyword from  `Keywords_austria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_passport_number" />
          <Match idRef="Keywords_austria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d567c-121">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d567c-121">Keywords</span></span>

<span data-ttu-id="d567c-122">| |</span><span class="sxs-lookup"><span data-stu-id="d567c-122"></span></span>
|<span data-ttu-id="d567c-123">**Keywords_austria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d567c-123">**Keywords_austria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d567c-124">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-124">passport number</span></span>  <br/> <span data-ttu-id="d567c-125">Numéro de passeport autrichien</span><span class="sxs-lookup"><span data-stu-id="d567c-125">austrian passport number</span></span>  <br/> <span data-ttu-id="d567c-126">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-126">passport no</span></span>  <br/> <span data-ttu-id="d567c-127">Reisepass</span><span class="sxs-lookup"><span data-stu-id="d567c-127">reisepass</span></span>  <br/> <span data-ttu-id="d567c-128">österreichisch Reisepass</span><span class="sxs-lookup"><span data-stu-id="d567c-128">österreichisch reisepass</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="d567c-129">Belgique</span><span class="sxs-lookup"><span data-stu-id="d567c-129">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="d567c-130">Format</span><span class="sxs-lookup"><span data-stu-id="d567c-130">Format</span></span>

<span data-ttu-id="d567c-131">Deux lettres suivies de six chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d567c-131">Two letters followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d567c-132">Modèle</span><span class="sxs-lookup"><span data-stu-id="d567c-132">Pattern</span></span>

<span data-ttu-id="d567c-133">Deux lettres et suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="d567c-133">Two letters and followed by six digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d567c-134">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d567c-134">Checksum</span></span>

<span data-ttu-id="d567c-135">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d567c-135">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d567c-136">Définition</span><span class="sxs-lookup"><span data-stu-id="d567c-136">Definition</span></span>

<span data-ttu-id="d567c-137">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d567c-137">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d567c-138">L'expression `Regex_belgium_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d567c-138">The regular expression  `Regex_belgium_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d567c-139">Un mot clé `Keywords_belgium_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d567c-139">A keyword from  `Keywords_belgium_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium__eu_passport_number" />
          <Match idRef="Keywords_belgium_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d567c-140">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d567c-140">Keywords</span></span>

<span data-ttu-id="d567c-141">| |</span><span class="sxs-lookup"><span data-stu-id="d567c-141"></span></span>
|<span data-ttu-id="d567c-142">**Keywords_belgium_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d567c-142">**Keywords_belgium_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d567c-143">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-143">passport number</span></span>  <br/> <span data-ttu-id="d567c-144">Numéro de passeport belge</span><span class="sxs-lookup"><span data-stu-id="d567c-144">belgian passport number</span></span>  <br/> <span data-ttu-id="d567c-145">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-145">passport no</span></span>  <br/> <span data-ttu-id="d567c-146">paspoort</span><span class="sxs-lookup"><span data-stu-id="d567c-146">paspoort</span></span>  <br/> <span data-ttu-id="d567c-147">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="d567c-147">paspoortnummer</span></span>  <br/> <span data-ttu-id="d567c-148">Reisepass kein</span><span class="sxs-lookup"><span data-stu-id="d567c-148">reisepass kein</span></span>  <br/> <span data-ttu-id="d567c-149">Reisepass</span><span class="sxs-lookup"><span data-stu-id="d567c-149">reisepass</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="d567c-150">Bulgarie</span><span class="sxs-lookup"><span data-stu-id="d567c-150">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="d567c-151">Format</span><span class="sxs-lookup"><span data-stu-id="d567c-151">Format</span></span>

<span data-ttu-id="d567c-152">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d567c-152">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d567c-153">Modèle</span><span class="sxs-lookup"><span data-stu-id="d567c-153">Pattern</span></span>

 <span data-ttu-id="d567c-154">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="d567c-154">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="d567c-155">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d567c-155">Checksum</span></span>

<span data-ttu-id="d567c-156">Non</span><span class="sxs-lookup"><span data-stu-id="d567c-156">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d567c-157">Définition</span><span class="sxs-lookup"><span data-stu-id="d567c-157">Definition</span></span>

<span data-ttu-id="d567c-158">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d567c-158">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d567c-159">L'expression `Regex_bulgaria_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d567c-159">The regular expression  `Regex_bulgaria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d567c-160">Un mot clé `Keywords_bulgaria_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d567c-160">A keyword from  `Keywords_bulgaria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_passport_number" />
          <Match idRef="Keywords_bulgaria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d567c-161">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d567c-161">Keywords</span></span>

<span data-ttu-id="d567c-162">| |</span><span class="sxs-lookup"><span data-stu-id="d567c-162"></span></span>
|<span data-ttu-id="d567c-163">**Keywords_bulgaria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d567c-163">**Keywords_bulgaria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d567c-164">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-164">passport number</span></span>  <br/> <span data-ttu-id="d567c-165">Numéro de Passeport bulgare</span><span class="sxs-lookup"><span data-stu-id="d567c-165">bulgarian passport number</span></span>  <br/> <span data-ttu-id="d567c-166">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-166">passport no</span></span>  <br/> <span data-ttu-id="d567c-167">номер на паспорта</span><span class="sxs-lookup"><span data-stu-id="d567c-167">номер на паспорта</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="d567c-168">Croatie</span><span class="sxs-lookup"><span data-stu-id="d567c-168">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="d567c-169">Format</span><span class="sxs-lookup"><span data-stu-id="d567c-169">Format</span></span>

<span data-ttu-id="d567c-170">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d567c-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d567c-171">Modèle</span><span class="sxs-lookup"><span data-stu-id="d567c-171">Pattern</span></span>

 <span data-ttu-id="d567c-172">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="d567c-172">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="d567c-173">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d567c-173">Checksum</span></span>

<span data-ttu-id="d567c-174">Non</span><span class="sxs-lookup"><span data-stu-id="d567c-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d567c-175">Définition</span><span class="sxs-lookup"><span data-stu-id="d567c-175">Definition</span></span>

<span data-ttu-id="d567c-176">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d567c-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d567c-177">L'expression `Regex_croatia_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d567c-177">The regular expression  `Regex_croatia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d567c-178">Un mot clé `Keywords_croatia_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d567c-178">A keyword from  `Keywords_croatia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_passport_number" />
          <Match idRef="Keywords_croatia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d567c-179">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d567c-179">Keywords</span></span>

<span data-ttu-id="d567c-180">| |</span><span class="sxs-lookup"><span data-stu-id="d567c-180"></span></span>
|<span data-ttu-id="d567c-181">**Keywords_croatia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d567c-181">**Keywords_croatia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d567c-182">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-182">passport number</span></span>  <br/> <span data-ttu-id="d567c-183">Numéro de passeport croate</span><span class="sxs-lookup"><span data-stu-id="d567c-183">croatian passport number</span></span>  <br/> <span data-ttu-id="d567c-184">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-184">passport no</span></span>  <br/> <span data-ttu-id="d567c-185">Broj putovnice</span><span class="sxs-lookup"><span data-stu-id="d567c-185">broj putovnice</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="d567c-186">Chypre</span><span class="sxs-lookup"><span data-stu-id="d567c-186">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="d567c-187">Format</span><span class="sxs-lookup"><span data-stu-id="d567c-187">Format</span></span>

<span data-ttu-id="d567c-188">Une lettre suivie de 6-8 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d567c-188">One letter followed by 6-8 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d567c-189">Modèle</span><span class="sxs-lookup"><span data-stu-id="d567c-189">Pattern</span></span>

<span data-ttu-id="d567c-190">Une lettre suivie de six à huit chiffres</span><span class="sxs-lookup"><span data-stu-id="d567c-190">One letter followed by six to eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d567c-191">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d567c-191">Checksum</span></span>

<span data-ttu-id="d567c-192">Non</span><span class="sxs-lookup"><span data-stu-id="d567c-192">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d567c-193">Définition</span><span class="sxs-lookup"><span data-stu-id="d567c-193">Definition</span></span>

<span data-ttu-id="d567c-194">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d567c-194">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d567c-195">L'expression `Regex_cyprus_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d567c-195">The regular expression  `Regex_cyprus_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d567c-196">Un mot clé `Keywords_cyprus_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d567c-196">A keyword from  `Keywords_cyprus_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_passport_number" />
          <Match idRef="Keywords_cyprus_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d567c-197">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d567c-197">Keywords</span></span>

<span data-ttu-id="d567c-198">| |</span><span class="sxs-lookup"><span data-stu-id="d567c-198"></span></span>
|<span data-ttu-id="d567c-199">**Keywords_cyprus_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d567c-199">**Keywords_cyprus_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d567c-200">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-200">passport number</span></span>  <br/> <span data-ttu-id="d567c-201">Numéro de passeport de Chypre</span><span class="sxs-lookup"><span data-stu-id="d567c-201">cyprus passport number</span></span>  <br/> <span data-ttu-id="d567c-202">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-202">passport no</span></span>  <br/> <span data-ttu-id="d567c-203">αριθμό διαβατηρίου</span><span class="sxs-lookup"><span data-stu-id="d567c-203">αριθμό διαβατηρίου</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="d567c-204">République tchèque</span><span class="sxs-lookup"><span data-stu-id="d567c-204">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="d567c-205">Format</span><span class="sxs-lookup"><span data-stu-id="d567c-205">Format</span></span>

<span data-ttu-id="d567c-206">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d567c-206">Eight digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d567c-207">Modèle</span><span class="sxs-lookup"><span data-stu-id="d567c-207">Pattern</span></span>

<span data-ttu-id="d567c-208">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d567c-208">Eight digits without spaces or delimiters</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d567c-209">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d567c-209">Checksum</span></span>

<span data-ttu-id="d567c-210">Non</span><span class="sxs-lookup"><span data-stu-id="d567c-210">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d567c-211">Définition</span><span class="sxs-lookup"><span data-stu-id="d567c-211">Definition</span></span>

<span data-ttu-id="d567c-212">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d567c-212">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d567c-213">L'expression `Regex_czech_republic_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d567c-213">The regular expression  `Regex_czech_republic_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d567c-214">Un mot clé `Keywords_czech_republic_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d567c-214">A keyword from  `Keywords_czech_republic_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_passport_number" />
          <Match idRef="Keywords_czech_republic_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d567c-215">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d567c-215">Keywords</span></span>

<span data-ttu-id="d567c-216">| |</span><span class="sxs-lookup"><span data-stu-id="d567c-216"></span></span>
|<span data-ttu-id="d567c-217">**Keywords_czech_republic_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d567c-217">**Keywords_czech_republic_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d567c-218">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-218">passport number</span></span>  <br/> <span data-ttu-id="d567c-219">Numéro de passeport tchèque</span><span class="sxs-lookup"><span data-stu-id="d567c-219">czech passport number</span></span>  <br/> <span data-ttu-id="d567c-220">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-220">passport no</span></span>  <br/> <span data-ttu-id="d567c-221">CESTOVNÍ pas</span><span class="sxs-lookup"><span data-stu-id="d567c-221">cestovní pas</span></span>  <br/> <span data-ttu-id="d567c-222">boîte</span><span class="sxs-lookup"><span data-stu-id="d567c-222">pas</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="d567c-223">Danemark</span><span class="sxs-lookup"><span data-stu-id="d567c-223">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="d567c-224">Format</span><span class="sxs-lookup"><span data-stu-id="d567c-224">Format</span></span>

<span data-ttu-id="d567c-225">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d567c-225">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d567c-226">Modèle</span><span class="sxs-lookup"><span data-stu-id="d567c-226">Pattern</span></span>

 <span data-ttu-id="d567c-227">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="d567c-227">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="d567c-228">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d567c-228">Checksum</span></span>

<span data-ttu-id="d567c-229">Non</span><span class="sxs-lookup"><span data-stu-id="d567c-229">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d567c-230">Définition</span><span class="sxs-lookup"><span data-stu-id="d567c-230">Definition</span></span>

<span data-ttu-id="d567c-231">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d567c-231">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d567c-232">L'expression `Regex_denmark_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d567c-232">The regular expression  `Regex_denmark_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d567c-233">Un mot clé `Keywords_denmark_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d567c-233">A keyword from  `Keywords_denmark_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_passport_number" />
          <Match idRef="Keywords_denmark_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d567c-234">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d567c-234">Keywords</span></span>

<span data-ttu-id="d567c-235">| |</span><span class="sxs-lookup"><span data-stu-id="d567c-235"></span></span>
|<span data-ttu-id="d567c-236">**Keywords_denmark_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d567c-236">**Keywords_denmark_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d567c-237">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-237">passport number</span></span>  <br/> <span data-ttu-id="d567c-238">Numéro de passeport danois</span><span class="sxs-lookup"><span data-stu-id="d567c-238">danish passport number</span></span>  <br/> <span data-ttu-id="d567c-239">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-239">passport no</span></span>  <br/> <span data-ttu-id="d567c-240">boîte</span><span class="sxs-lookup"><span data-stu-id="d567c-240">pas</span></span>  <br/> <span data-ttu-id="d567c-241">pasnummer</span><span class="sxs-lookup"><span data-stu-id="d567c-241">pasnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="d567c-242">Estonie</span><span class="sxs-lookup"><span data-stu-id="d567c-242">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="d567c-243">Format</span><span class="sxs-lookup"><span data-stu-id="d567c-243">Format</span></span>

<span data-ttu-id="d567c-244">Une lettre suivie de sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d567c-244">One letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d567c-245">Modèle</span><span class="sxs-lookup"><span data-stu-id="d567c-245">Pattern</span></span>

<span data-ttu-id="d567c-246">Une lettre suivie de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="d567c-246">One letter followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d567c-247">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d567c-247">Checksum</span></span>

<span data-ttu-id="d567c-248">Non</span><span class="sxs-lookup"><span data-stu-id="d567c-248">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d567c-249">Définition</span><span class="sxs-lookup"><span data-stu-id="d567c-249">Definition</span></span>

<span data-ttu-id="d567c-250">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d567c-250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d567c-251">L'expression `Regex_estonia_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d567c-251">The regular expression  `Regex_estonia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d567c-252">Un mot clé `Keywords_estonia_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d567c-252">A keyword from  `Keywords_estonia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_passport_number" />
          <Match idRef="Keywords_estonia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d567c-253">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d567c-253">Keywords</span></span>

<span data-ttu-id="d567c-254">| |</span><span class="sxs-lookup"><span data-stu-id="d567c-254"></span></span>
|<span data-ttu-id="d567c-255">**Keywords_estonia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d567c-255">**Keywords_estonia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d567c-256">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-256">passport number</span></span>  <br/> <span data-ttu-id="d567c-257">Numéro de passeport estonien</span><span class="sxs-lookup"><span data-stu-id="d567c-257">estonian passport number</span></span>  <br/> <span data-ttu-id="d567c-258">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-258">passport no</span></span>  <br/> <span data-ttu-id="d567c-259">Eesti kodaniku</span><span class="sxs-lookup"><span data-stu-id="d567c-259">eesti kodaniku pass</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="d567c-260">Finlande</span><span class="sxs-lookup"><span data-stu-id="d567c-260">Finland</span></span>

<span data-ttu-id="d567c-261">Pour plus d'informations, consultez la section «numéro de passeport de Finlande» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="d567c-261">For details, see the section "Finland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="d567c-262">France</span><span class="sxs-lookup"><span data-stu-id="d567c-262">France</span></span>

<span data-ttu-id="d567c-263">Pour plus d'informations, consultez la section «numéro de passeport français» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="d567c-263">For details, see the section "France Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="d567c-264">Allemagne</span><span class="sxs-lookup"><span data-stu-id="d567c-264">Germany</span></span>

<span data-ttu-id="d567c-265">Pour plus d'informations, reportez-vous à la section «numéro de passeport allemand» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="d567c-265">For details, see the section "Germany Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="d567c-266">Grèce</span><span class="sxs-lookup"><span data-stu-id="d567c-266">Greece</span></span>

### <a name="format"></a><span data-ttu-id="d567c-267">Format</span><span class="sxs-lookup"><span data-stu-id="d567c-267">Format</span></span>

<span data-ttu-id="d567c-268">Deux lettres suivies de sept chiffres, sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d567c-268">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d567c-269">Modèle</span><span class="sxs-lookup"><span data-stu-id="d567c-269">Pattern</span></span>

<span data-ttu-id="d567c-270">Deux lettres suivies de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="d567c-270">Two letters followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d567c-271">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d567c-271">Checksum</span></span>

<span data-ttu-id="d567c-272">Non</span><span class="sxs-lookup"><span data-stu-id="d567c-272">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d567c-273">Définition</span><span class="sxs-lookup"><span data-stu-id="d567c-273">Definition</span></span>

<span data-ttu-id="d567c-274">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d567c-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d567c-275">L'expression `Regex_greece_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d567c-275">The regular expression  `Regex_greece_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d567c-276">Un mot clé `Keywords_greece_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d567c-276">A keyword from  `Keywords_greece_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_passport_number" />
          <Match idRef="Keywords_greece_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d567c-277">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d567c-277">Keywords</span></span>

<span data-ttu-id="d567c-278">| |</span><span class="sxs-lookup"><span data-stu-id="d567c-278"></span></span>
|<span data-ttu-id="d567c-279">**Keywords_greece_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d567c-279">**Keywords_greece_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d567c-280">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-280">passport number</span></span>  <br/> <span data-ttu-id="d567c-281">Numéro de passeport grec</span><span class="sxs-lookup"><span data-stu-id="d567c-281">greek passport number</span></span>  <br/> <span data-ttu-id="d567c-282">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-282">passport no</span></span>  <br/> <span data-ttu-id="d567c-283">διαβατηριο</span><span class="sxs-lookup"><span data-stu-id="d567c-283">διαβατηριο</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="d567c-284">Hongrie</span><span class="sxs-lookup"><span data-stu-id="d567c-284">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="d567c-285">Format</span><span class="sxs-lookup"><span data-stu-id="d567c-285">Format</span></span>

<span data-ttu-id="d567c-286">Deux lettres suivies de six ou sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d567c-286">Two letters followed by six or seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d567c-287">Modèle</span><span class="sxs-lookup"><span data-stu-id="d567c-287">Pattern</span></span>

<span data-ttu-id="d567c-288">Deux lettres suivies de six ou sept chiffres</span><span class="sxs-lookup"><span data-stu-id="d567c-288">Two letters followed by six or seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d567c-289">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d567c-289">Checksum</span></span>

<span data-ttu-id="d567c-290">Non</span><span class="sxs-lookup"><span data-stu-id="d567c-290">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d567c-291">Définition</span><span class="sxs-lookup"><span data-stu-id="d567c-291">Definition</span></span>

<span data-ttu-id="d567c-292">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d567c-292">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d567c-293">L'expression `Regex_hungary_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d567c-293">The regular expression  `Regex_hungary_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d567c-294">Un mot clé `Keywords_hungary_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d567c-294">A keyword from  `Keywords_hungary_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_passport_number" />
          <Match idRef="Keywords_hungary_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d567c-295">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d567c-295">Keywords</span></span>

<span data-ttu-id="d567c-296">| |</span><span class="sxs-lookup"><span data-stu-id="d567c-296"></span></span>
|<span data-ttu-id="d567c-297">**Keywords_hungary_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d567c-297">**Keywords_hungary_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d567c-298">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-298">passport number</span></span>  <br/> <span data-ttu-id="d567c-299">Numéro de passeport hongrois</span><span class="sxs-lookup"><span data-stu-id="d567c-299">hungarian passport number</span></span>  <br/> <span data-ttu-id="d567c-300">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-300">passport no</span></span>  <br/> <span data-ttu-id="d567c-301">útlevél száma</span><span class="sxs-lookup"><span data-stu-id="d567c-301">útlevél száma</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="d567c-302">Irlande</span><span class="sxs-lookup"><span data-stu-id="d567c-302">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="d567c-303">Format</span><span class="sxs-lookup"><span data-stu-id="d567c-303">Format</span></span>

<span data-ttu-id="d567c-304">Deux lettres ou chiffres suivis de sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d567c-304">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d567c-305">Modèle</span><span class="sxs-lookup"><span data-stu-id="d567c-305">Pattern</span></span>

<span data-ttu-id="d567c-306">Deux lettres ou chiffres suivis de sept chiffres:</span><span class="sxs-lookup"><span data-stu-id="d567c-306">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="d567c-307">Deux chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="d567c-307">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="d567c-308">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="d567c-308">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d567c-309">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d567c-309">Checksum</span></span>

<span data-ttu-id="d567c-310">Non</span><span class="sxs-lookup"><span data-stu-id="d567c-310">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d567c-311">Définition</span><span class="sxs-lookup"><span data-stu-id="d567c-311">Definition</span></span>

<span data-ttu-id="d567c-312">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d567c-312">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d567c-313">L'expression `Regex_ireland_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d567c-313">The regular expression  `Regex_ireland_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d567c-314">Un mot clé `Keywords_ireland_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d567c-314">A keyword from  `Keywords_ireland_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_passport_number" />
          <Match idRef="Keywords_ireland_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d567c-315">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d567c-315">Keywords</span></span>

<span data-ttu-id="d567c-316">| |</span><span class="sxs-lookup"><span data-stu-id="d567c-316"></span></span>
|<span data-ttu-id="d567c-317">**Keywords_ireland_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d567c-317">**Keywords_ireland_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d567c-318">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-318">passport number</span></span>  <br/> <span data-ttu-id="d567c-319">Numéro de passeport irlandais</span><span class="sxs-lookup"><span data-stu-id="d567c-319">irish passport number</span></span>  <br/> <span data-ttu-id="d567c-320">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-320">passport no</span></span>  <br/> <span data-ttu-id="d567c-321">boîte</span><span class="sxs-lookup"><span data-stu-id="d567c-321">pas</span></span>  <br/> <span data-ttu-id="d567c-322">tel</span><span class="sxs-lookup"><span data-stu-id="d567c-322">passport</span></span>  <br/> <span data-ttu-id="d567c-323">passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-323">passeport</span></span>  <br/> <span data-ttu-id="d567c-324">passeport numérique</span><span class="sxs-lookup"><span data-stu-id="d567c-324">passeport numero</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="d567c-325">Italie</span><span class="sxs-lookup"><span data-stu-id="d567c-325">Italy</span></span>

### <a name="format"></a><span data-ttu-id="d567c-326">Format</span><span class="sxs-lookup"><span data-stu-id="d567c-326">Format</span></span>

<span data-ttu-id="d567c-327">Deux lettres ou chiffres suivis de sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d567c-327">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d567c-328">Modèle</span><span class="sxs-lookup"><span data-stu-id="d567c-328">Pattern</span></span>

<span data-ttu-id="d567c-329">Deux lettres ou chiffres suivis de sept chiffres:</span><span class="sxs-lookup"><span data-stu-id="d567c-329">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="d567c-330">Deux chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="d567c-330">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="d567c-331">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="d567c-331">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d567c-332">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d567c-332">Checksum</span></span>

<span data-ttu-id="d567c-333">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d567c-333">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d567c-334">Définition</span><span class="sxs-lookup"><span data-stu-id="d567c-334">Definition</span></span>

<span data-ttu-id="d567c-335">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d567c-335">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d567c-336">L'expression `Regex_italy_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d567c-336">The regular expression  `Regex_italy_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d567c-337">Un mot clé `Keywords_italy_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d567c-337">A keyword from  `Keywords_italy_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_passport_number" />
          <Match idRef="Keywords_italy_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d567c-338">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d567c-338">Keywords</span></span>

<span data-ttu-id="d567c-339">| |</span><span class="sxs-lookup"><span data-stu-id="d567c-339"></span></span>
|<span data-ttu-id="d567c-340">**Keywords_italy_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d567c-340">**Keywords_italy_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d567c-341">Numéro de passeport italien</span><span class="sxs-lookup"><span data-stu-id="d567c-341">italian passport number</span></span>  <br/> <span data-ttu-id="d567c-342">Repubblica Italiana passaporto</span><span class="sxs-lookup"><span data-stu-id="d567c-342">repubblica italiana passaporto</span></span>  <br/> <span data-ttu-id="d567c-343">passaporto</span><span class="sxs-lookup"><span data-stu-id="d567c-343">passaporto</span></span>  <br/> <span data-ttu-id="d567c-344">passaporto Italiana</span><span class="sxs-lookup"><span data-stu-id="d567c-344">passaporto italiana</span></span>  <br/> <span data-ttu-id="d567c-345">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-345">passport number</span></span>  <br/> <span data-ttu-id="d567c-346">Italiana passaporto numérique</span><span class="sxs-lookup"><span data-stu-id="d567c-346">italiana passaporto numero</span></span>  <br/> <span data-ttu-id="d567c-347">passaporto numérique</span><span class="sxs-lookup"><span data-stu-id="d567c-347">passaporto numero</span></span>  <br/> <span data-ttu-id="d567c-348">numéro passeport italien</span><span class="sxs-lookup"><span data-stu-id="d567c-348">numéro passeport italien</span></span>  <br/> <span data-ttu-id="d567c-349">numéro passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-349">numéro passeport</span></span>  <br/> |
   
## <a name="latvia"></a><span data-ttu-id="d567c-350">Lettonie</span><span class="sxs-lookup"><span data-stu-id="d567c-350">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="d567c-351">Format</span><span class="sxs-lookup"><span data-stu-id="d567c-351">Format</span></span>

<span data-ttu-id="d567c-352">Deux lettres ou chiffres suivis de sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d567c-352">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d567c-353">Modèle</span><span class="sxs-lookup"><span data-stu-id="d567c-353">Pattern</span></span>

<span data-ttu-id="d567c-354">Deux lettres ou chiffres suivis de sept chiffres:</span><span class="sxs-lookup"><span data-stu-id="d567c-354">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="d567c-355">Deux chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="d567c-355">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="d567c-356">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="d567c-356">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d567c-357">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d567c-357">Checksum</span></span>

<span data-ttu-id="d567c-358">Non</span><span class="sxs-lookup"><span data-stu-id="d567c-358">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d567c-359">Définition</span><span class="sxs-lookup"><span data-stu-id="d567c-359">Definition</span></span>

<span data-ttu-id="d567c-360">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d567c-360">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d567c-361">L'expression `Regex_latvia_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d567c-361">The regular expression  `Regex_latvia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d567c-362">Un mot clé `Keywords_latvia_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d567c-362">A keyword from  `Keywords_latvia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_passport_number" />
          <Match idRef="Keywords_latvia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d567c-363">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d567c-363">Keywords</span></span>

<span data-ttu-id="d567c-364">| |</span><span class="sxs-lookup"><span data-stu-id="d567c-364"></span></span>
|<span data-ttu-id="d567c-365">**Keywords_latvia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d567c-365">**Keywords_latvia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d567c-366">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-366">passport number</span></span>  <br/> <span data-ttu-id="d567c-367">Numéro de passeport letton</span><span class="sxs-lookup"><span data-stu-id="d567c-367">latvian passport number</span></span>  <br/> <span data-ttu-id="d567c-368">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-368">passport no</span></span>  <br/> <span data-ttu-id="d567c-369">pase numurs</span><span class="sxs-lookup"><span data-stu-id="d567c-369">pase numurs</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="d567c-370">Lituanie</span><span class="sxs-lookup"><span data-stu-id="d567c-370">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="d567c-371">Format</span><span class="sxs-lookup"><span data-stu-id="d567c-371">Format</span></span>

<span data-ttu-id="d567c-372">Huit chiffres ou lettres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d567c-372">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d567c-373">Modèle</span><span class="sxs-lookup"><span data-stu-id="d567c-373">Pattern</span></span>

<span data-ttu-id="d567c-374">Huit chiffres ou lettres (ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="d567c-374">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d567c-375">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d567c-375">Checksum</span></span>

<span data-ttu-id="d567c-376">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d567c-376">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d567c-377">Définition</span><span class="sxs-lookup"><span data-stu-id="d567c-377">Definition</span></span>

<span data-ttu-id="d567c-378">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d567c-378">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d567c-379">L'expression `Regex_lithuania_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d567c-379">The regular expression  `Regex_lithuania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d567c-380">Un mot clé `Keywords_lithuania_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d567c-380">A keyword from  `Keywords_lithuania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_passport_number" />
          <Match idRef="Keywords_lithuania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d567c-381">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d567c-381">Keywords</span></span>

<span data-ttu-id="d567c-382">| |</span><span class="sxs-lookup"><span data-stu-id="d567c-382"></span></span>
|<span data-ttu-id="d567c-383">**Keywords_lithuania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d567c-383">**Keywords_lithuania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d567c-384">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-384">passport number</span></span>  <br/> <span data-ttu-id="d567c-385">Numéro de passeport lithunian</span><span class="sxs-lookup"><span data-stu-id="d567c-385">lithunian passport number</span></span>  <br/> <span data-ttu-id="d567c-386">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-386">passport no</span></span>  <br/> <span data-ttu-id="d567c-387">Paso chiffres</span><span class="sxs-lookup"><span data-stu-id="d567c-387">paso numeris</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="d567c-388">Relatif</span><span class="sxs-lookup"><span data-stu-id="d567c-388">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="d567c-389">Format</span><span class="sxs-lookup"><span data-stu-id="d567c-389">Format</span></span>

<span data-ttu-id="d567c-390">Huit chiffres ou lettres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d567c-390">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d567c-391">Modèle</span><span class="sxs-lookup"><span data-stu-id="d567c-391">Pattern</span></span>

<span data-ttu-id="d567c-392">Huit chiffres ou lettres (ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="d567c-392">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d567c-393">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d567c-393">Checksum</span></span>

<span data-ttu-id="d567c-394">Non</span><span class="sxs-lookup"><span data-stu-id="d567c-394">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d567c-395">Définition</span><span class="sxs-lookup"><span data-stu-id="d567c-395">Definition</span></span>

<span data-ttu-id="d567c-396">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d567c-396">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d567c-397">L'expression `Regex_nation_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d567c-397">The regular expression  `Regex_nation_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d567c-398">Un mot clé `Keywords_nation_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d567c-398">A keyword from  `Keywords_nation_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_nation_eu_passport_number" />
          <Match idRef="Keywords_nation_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d567c-399">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d567c-399">Keywords</span></span>

<span data-ttu-id="d567c-400">| |</span><span class="sxs-lookup"><span data-stu-id="d567c-400"></span></span>
|<span data-ttu-id="d567c-401">**Keywords_nation_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d567c-401">**Keywords_nation_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d567c-402">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-402">passport number</span></span>  <br/> <span data-ttu-id="d567c-403">Numéro de passeport letton</span><span class="sxs-lookup"><span data-stu-id="d567c-403">latvian passport number</span></span>  <br/> <span data-ttu-id="d567c-404">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-404">passport no</span></span>  <br/> <span data-ttu-id="d567c-405">passnummer</span><span class="sxs-lookup"><span data-stu-id="d567c-405">passnummer</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="d567c-406">Malte</span><span class="sxs-lookup"><span data-stu-id="d567c-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="d567c-407">Format</span><span class="sxs-lookup"><span data-stu-id="d567c-407">Format</span></span>

<span data-ttu-id="d567c-408">Sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d567c-408">Seven digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d567c-409">Modèle</span><span class="sxs-lookup"><span data-stu-id="d567c-409">Pattern</span></span>

 <span data-ttu-id="d567c-410">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="d567c-410">Seven digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="d567c-411">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d567c-411">Checksum</span></span>

<span data-ttu-id="d567c-412">Non</span><span class="sxs-lookup"><span data-stu-id="d567c-412">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d567c-413">Définition</span><span class="sxs-lookup"><span data-stu-id="d567c-413">Definition</span></span>

<span data-ttu-id="d567c-414">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d567c-414">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d567c-415">L'expression `Regex_malta_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d567c-415">The regular expression  `Regex_malta_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d567c-416">Un mot clé `Keywords_malta_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d567c-416">A keyword from  `Keywords_malta_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_passport_number" />
          <Match idRef="Keywords_malta_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d567c-417">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d567c-417">Keywords</span></span>

<span data-ttu-id="d567c-418">| |</span><span class="sxs-lookup"><span data-stu-id="d567c-418"></span></span>
|<span data-ttu-id="d567c-419">**Keywords_malta_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d567c-419">**Keywords_malta_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d567c-420">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-420">passport number</span></span>  <br/> <span data-ttu-id="d567c-421">Numéro de passeport maltais</span><span class="sxs-lookup"><span data-stu-id="d567c-421">maltese passport number</span></span>  <br/> <span data-ttu-id="d567c-422">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-422">passport no</span></span>  <br/> <span data-ttu-id="d567c-423">numru Tal-Passaport</span><span class="sxs-lookup"><span data-stu-id="d567c-423">numru tal-passaport</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="d567c-424">Pays-Bas</span><span class="sxs-lookup"><span data-stu-id="d567c-424">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="d567c-425">Format</span><span class="sxs-lookup"><span data-stu-id="d567c-425">Format</span></span>

<span data-ttu-id="d567c-426">Neuf lettres ou chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d567c-426">Nine letters or digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d567c-427">Modèle</span><span class="sxs-lookup"><span data-stu-id="d567c-427">Pattern</span></span>

<span data-ttu-id="d567c-428">Neuf lettres ou chiffres</span><span class="sxs-lookup"><span data-stu-id="d567c-428">Nine letters or digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d567c-429">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d567c-429">Checksum</span></span>

<span data-ttu-id="d567c-430">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d567c-430">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d567c-431">Définition</span><span class="sxs-lookup"><span data-stu-id="d567c-431">Definition</span></span>

<span data-ttu-id="d567c-432">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d567c-432">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d567c-433">L'expression `Regex_netherlands_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d567c-433">The regular expression  `Regex_netherlands_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d567c-434">Un mot clé `Keywords_netherlands_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d567c-434">A keyword from  `Keywords_netherlands_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_passport_number" />
          <Match idRef="Keywords_netherlands_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d567c-435">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d567c-435">Keywords</span></span>

<span data-ttu-id="d567c-436">| |</span><span class="sxs-lookup"><span data-stu-id="d567c-436"></span></span>
|<span data-ttu-id="d567c-437">**Keywords_netherlands_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d567c-437">**Keywords_netherlands_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d567c-438">Numéro de passeport néerlandais</span><span class="sxs-lookup"><span data-stu-id="d567c-438">dutch passport number</span></span>  <br/> <span data-ttu-id="d567c-439">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-439">passport number</span></span>  <br/> <span data-ttu-id="d567c-440">Numéro de passeport néerlandais</span><span class="sxs-lookup"><span data-stu-id="d567c-440">netherlands passport number</span></span>  <br/> <span data-ttu-id="d567c-441">Nederlanden paspoort Nummer</span><span class="sxs-lookup"><span data-stu-id="d567c-441">nederlanden paspoort nummer</span></span>  <br/> <span data-ttu-id="d567c-442">paspoort</span><span class="sxs-lookup"><span data-stu-id="d567c-442">paspoort</span></span>  <br/> <span data-ttu-id="d567c-443">Nederlanden paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="d567c-443">nederlanden paspoortnummer</span></span>  <br/> <span data-ttu-id="d567c-444">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="d567c-444">paspoortnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="d567c-445">Pologne</span><span class="sxs-lookup"><span data-stu-id="d567c-445">Poland</span></span>

<span data-ttu-id="d567c-446">Pour plus d'informations, reportez-vous à la section «numéro de passeport polonais» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="d567c-446">For details, see the section "Poland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="d567c-447">Portugal</span><span class="sxs-lookup"><span data-stu-id="d567c-447">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="d567c-448">Format</span><span class="sxs-lookup"><span data-stu-id="d567c-448">Format</span></span>

<span data-ttu-id="d567c-449">Une lettre suivie de six chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d567c-449">One letter followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d567c-450">Modèle</span><span class="sxs-lookup"><span data-stu-id="d567c-450">Pattern</span></span>

<span data-ttu-id="d567c-451">Une lettre suivie de six chiffres:</span><span class="sxs-lookup"><span data-stu-id="d567c-451">One letter followed by six digits:</span></span>
  
- <span data-ttu-id="d567c-452">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="d567c-452">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="d567c-453">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="d567c-453">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d567c-454">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d567c-454">Checksum</span></span>

<span data-ttu-id="d567c-455">Non</span><span class="sxs-lookup"><span data-stu-id="d567c-455">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d567c-456">Définition</span><span class="sxs-lookup"><span data-stu-id="d567c-456">Definition</span></span>

<span data-ttu-id="d567c-457">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d567c-457">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d567c-458">L'expression `Regex_portugal_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d567c-458">The regular expression  `Regex_portugal_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d567c-459">Un mot clé `Keywords_portugal_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d567c-459">A keyword from  `Keywords_portugal_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_passport_number" />
          <Match idRef="Keywords_portugal_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d567c-460">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d567c-460">Keywords</span></span>

<span data-ttu-id="d567c-461">| |</span><span class="sxs-lookup"><span data-stu-id="d567c-461"></span></span>
|<span data-ttu-id="d567c-462">**Keywords_portugal_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d567c-462">**Keywords_portugal_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d567c-463">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-463">passport number</span></span>  <br/> <span data-ttu-id="d567c-464">Numéro de passeport Portugais</span><span class="sxs-lookup"><span data-stu-id="d567c-464">portuguese passport number</span></span>  <br/> <span data-ttu-id="d567c-465">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-465">passport no</span></span>  <br/> <span data-ttu-id="d567c-466">número do Passaporte</span><span class="sxs-lookup"><span data-stu-id="d567c-466">número do passaporte</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="d567c-467">Roumanie</span><span class="sxs-lookup"><span data-stu-id="d567c-467">Romania</span></span>

### <a name="format"></a><span data-ttu-id="d567c-468">Format</span><span class="sxs-lookup"><span data-stu-id="d567c-468">Format</span></span>

<span data-ttu-id="d567c-469">Huit ou neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d567c-469">Eight or nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d567c-470">Modèle</span><span class="sxs-lookup"><span data-stu-id="d567c-470">Pattern</span></span>

<span data-ttu-id="d567c-471">Huit ou neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="d567c-471">Eight or nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d567c-472">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d567c-472">Checksum</span></span>

<span data-ttu-id="d567c-473">Non</span><span class="sxs-lookup"><span data-stu-id="d567c-473">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d567c-474">Définition</span><span class="sxs-lookup"><span data-stu-id="d567c-474">Definition</span></span>

<span data-ttu-id="d567c-475">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d567c-475">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d567c-476">L'expression `Regex_romania_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d567c-476">The regular expression  `Regex_romania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d567c-477">Un mot clé `Keywords_romania_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d567c-477">A keyword from  `Keywords_romania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_passport_number" />
          <Match idRef="Keywords_romania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d567c-478">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d567c-478">Keywords</span></span>

<span data-ttu-id="d567c-479">| |</span><span class="sxs-lookup"><span data-stu-id="d567c-479"></span></span>
|<span data-ttu-id="d567c-480">**Keywords_romania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d567c-480">**Keywords_romania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d567c-481">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-481">passport number</span></span>  <br/> <span data-ttu-id="d567c-482">Numéro de passeport roumain</span><span class="sxs-lookup"><span data-stu-id="d567c-482">romanian passport number</span></span>  <br/> <span data-ttu-id="d567c-483">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-483">passport no</span></span>  <br/> <span data-ttu-id="d567c-484">numărul pașaportului</span><span class="sxs-lookup"><span data-stu-id="d567c-484">numărul pașaportului</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="d567c-485">République de Slovaquie</span><span class="sxs-lookup"><span data-stu-id="d567c-485">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="d567c-486">Format</span><span class="sxs-lookup"><span data-stu-id="d567c-486">Format</span></span>

<span data-ttu-id="d567c-487">Un chiffre ou une lettre suivi de sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d567c-487">One digit or letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d567c-488">Modèle</span><span class="sxs-lookup"><span data-stu-id="d567c-488">Pattern</span></span>

<span data-ttu-id="d567c-489">Un chiffre ou une lettre (ne respectant pas la casse) suivi de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="d567c-489">One digit or letter (not case sensitive) followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d567c-490">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d567c-490">Checksum</span></span>

<span data-ttu-id="d567c-491">Non</span><span class="sxs-lookup"><span data-stu-id="d567c-491">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d567c-492">Définition</span><span class="sxs-lookup"><span data-stu-id="d567c-492">Definition</span></span>

<span data-ttu-id="d567c-493">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d567c-493">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d567c-494">L'expression `Regex_slovakia_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d567c-494">The regular expression  `Regex_slovakia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d567c-495">Un mot clé `Keywords_slovakia_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d567c-495">A keyword from  `Keywords_slovakia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_passport_number" />
          <Match idRef="Keywords_slovakia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d567c-496">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d567c-496">Keywords</span></span>

<span data-ttu-id="d567c-497">| |</span><span class="sxs-lookup"><span data-stu-id="d567c-497"></span></span>
|<span data-ttu-id="d567c-498">**Keywords_slovakia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d567c-498">**Keywords_slovakia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d567c-499">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-499">passport number</span></span>  <br/> <span data-ttu-id="d567c-500">Numéro de passeport slovaque</span><span class="sxs-lookup"><span data-stu-id="d567c-500">slovakian passport number</span></span>  <br/> <span data-ttu-id="d567c-501">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-501">passport no</span></span>  <br/> <span data-ttu-id="d567c-502">číslo Pasu</span><span class="sxs-lookup"><span data-stu-id="d567c-502">číslo pasu</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="d567c-503">Slovénie</span><span class="sxs-lookup"><span data-stu-id="d567c-503">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="d567c-504">Format</span><span class="sxs-lookup"><span data-stu-id="d567c-504">Format</span></span>

<span data-ttu-id="d567c-505">Deux lettres suivies de sept chiffres, sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d567c-505">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d567c-506">Modèle</span><span class="sxs-lookup"><span data-stu-id="d567c-506">Pattern</span></span>

<span data-ttu-id="d567c-507">Deux lettres suivies de sept chiffres:</span><span class="sxs-lookup"><span data-stu-id="d567c-507">Two letters followed by seven digits:</span></span>
  
- <span data-ttu-id="d567c-508">La lettre «P»</span><span class="sxs-lookup"><span data-stu-id="d567c-508">The letter "P"</span></span>
    
- <span data-ttu-id="d567c-509">Une lettre majuscule</span><span class="sxs-lookup"><span data-stu-id="d567c-509">One uppercase letter</span></span>
    
- <span data-ttu-id="d567c-510">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="d567c-510">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d567c-511">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d567c-511">Checksum</span></span>

<span data-ttu-id="d567c-512">Non</span><span class="sxs-lookup"><span data-stu-id="d567c-512">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="d567c-513">Définition</span><span class="sxs-lookup"><span data-stu-id="d567c-513">Definition</span></span>

<span data-ttu-id="d567c-514">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d567c-514">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d567c-515">L'expression `Regex_slovenia_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d567c-515">The regular expression  `Regex_slovenia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d567c-516">Un mot clé `Keywords_slovenia_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d567c-516">A keyword from  `Keywords_slovenia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_passport_number" />
          <Match idRef="Keywords_slovenia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d567c-517">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d567c-517">Keywords</span></span>

<span data-ttu-id="d567c-518">| |</span><span class="sxs-lookup"><span data-stu-id="d567c-518"></span></span>
|<span data-ttu-id="d567c-519">**Keywords_slovenia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d567c-519">**Keywords_slovenia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d567c-520">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-520">passport number</span></span>  <br/> <span data-ttu-id="d567c-521">Numéro de passeport slovène</span><span class="sxs-lookup"><span data-stu-id="d567c-521">slovenian passport number</span></span>  <br/> <span data-ttu-id="d567c-522">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-522">passport no</span></span>  <br/> <span data-ttu-id="d567c-523">številka potnega Lista</span><span class="sxs-lookup"><span data-stu-id="d567c-523">številka potnega lista</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="d567c-524">Espagne</span><span class="sxs-lookup"><span data-stu-id="d567c-524">Spain</span></span>

### <a name="format"></a><span data-ttu-id="d567c-525">Format</span><span class="sxs-lookup"><span data-stu-id="d567c-525">Format</span></span>

<span data-ttu-id="d567c-526">Combinaison de huit ou neuf caractères de lettres et de chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d567c-526">An eight- or nine-character combination of letters and numbers with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d567c-527">Modèle</span><span class="sxs-lookup"><span data-stu-id="d567c-527">Pattern</span></span>

<span data-ttu-id="d567c-528">Combinaison de huit ou neuf caractères de lettres et de chiffres:</span><span class="sxs-lookup"><span data-stu-id="d567c-528">An eight- or nine-character combination of letters and numbers:</span></span>
  
-  <span data-ttu-id="d567c-529">Deux chiffres ou lettres</span><span class="sxs-lookup"><span data-stu-id="d567c-529">Two digits or letters</span></span> 
    
- <span data-ttu-id="d567c-530">Un chiffre ou une lettre (facultatif)</span><span class="sxs-lookup"><span data-stu-id="d567c-530">One digit or letter (optional)</span></span>
    
- <span data-ttu-id="d567c-531">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="d567c-531">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d567c-532">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d567c-532">Checksum</span></span>

<span data-ttu-id="d567c-533">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d567c-533">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d567c-534">Définition</span><span class="sxs-lookup"><span data-stu-id="d567c-534">Definition</span></span>

<span data-ttu-id="d567c-535">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d567c-535">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d567c-536">L'expression `Regex_spain_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d567c-536">The regular expression  `Regex_spain_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d567c-537">Un mot clé `Keywords_spain_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d567c-537">A keyword from  `Keywords_spain_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_passport_number" />
          <Match idRef="Keywords_spain_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d567c-538">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d567c-538">Keywords</span></span>

<span data-ttu-id="d567c-539">| |</span><span class="sxs-lookup"><span data-stu-id="d567c-539"></span></span>
|<span data-ttu-id="d567c-540">**Keywords_spain_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="d567c-540">**Keywords_spain_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="d567c-541">tel</span><span class="sxs-lookup"><span data-stu-id="d567c-541">passport</span></span>  <br/> <span data-ttu-id="d567c-542">Passport Espagne</span><span class="sxs-lookup"><span data-stu-id="d567c-542">spain passport</span></span>  <br/> <span data-ttu-id="d567c-543">livre de passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-543">passport book</span></span>  <br/> <span data-ttu-id="d567c-544">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-544">passport number</span></span>  <br/> <span data-ttu-id="d567c-545">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d567c-545">passport no</span></span>  <br/> <span data-ttu-id="d567c-546">Libreta pasaporte</span><span class="sxs-lookup"><span data-stu-id="d567c-546">libreta pasaporte</span></span>  <br/> <span data-ttu-id="d567c-547">número pasaporte</span><span class="sxs-lookup"><span data-stu-id="d567c-547">número pasaporte</span></span>  <br/> <span data-ttu-id="d567c-548">España pasaporte</span><span class="sxs-lookup"><span data-stu-id="d567c-548">españa pasaporte</span></span>  <br/> <span data-ttu-id="d567c-549">pasaporte</span><span class="sxs-lookup"><span data-stu-id="d567c-549">pasaporte</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="d567c-550">Suède</span><span class="sxs-lookup"><span data-stu-id="d567c-550">Sweden</span></span>

<span data-ttu-id="d567c-551">Pour plus d'informations, reportez-vous à la section «numéro de passeport Suède» dans [ce que recherche les types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="d567c-551">For details, see the section "Sweden Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="uk"></a><span data-ttu-id="d567c-552">R.U.</span><span class="sxs-lookup"><span data-stu-id="d567c-552">UK</span></span>

<span data-ttu-id="d567c-553">Pour plus d'informations, reportez-vous à la section «U.S./R.U.</span><span class="sxs-lookup"><span data-stu-id="d567c-553">For details, see the section "U.S. / U.K.</span></span> <span data-ttu-id="d567c-554">Numéro de passeport» dans [ce que recherche les types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="d567c-554">Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d567c-555">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d567c-555">See also</span></span>

[<span data-ttu-id="d567c-556">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="d567c-556">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

