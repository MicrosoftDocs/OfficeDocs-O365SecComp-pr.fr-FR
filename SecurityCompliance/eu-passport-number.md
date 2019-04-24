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
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32256822"
---
# <a name="eu-passport-number"></a><span data-ttu-id="65a34-104">Numéro de passeport UE</span><span class="sxs-lookup"><span data-stu-id="65a34-104">EU Passport Number</span></span>

<span data-ttu-id="65a34-105">Cette rubrique présente ce qu'une stratégie de protection contre la perte de données (DLP) recherche lorsqu'elle détecte le type d'informations sensibles du numéro de passeport de l'UE.</span><span class="sxs-lookup"><span data-stu-id="65a34-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Passport Number sensitive information type.</span></span> <span data-ttu-id="65a34-106">Ce type d'informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.</span><span class="sxs-lookup"><span data-stu-id="65a34-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="65a34-107">Autriche</span><span class="sxs-lookup"><span data-stu-id="65a34-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="65a34-108">Format</span><span class="sxs-lookup"><span data-stu-id="65a34-108">Format</span></span>

<span data-ttu-id="65a34-109">Une lettre suivie d'un espace facultatif et de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="65a34-109">One letter followed by an optional space and seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65a34-110">Modèle</span><span class="sxs-lookup"><span data-stu-id="65a34-110">Pattern</span></span>

<span data-ttu-id="65a34-111">Une combinaison d'une lettre, de sept chiffres et d'un espace:</span><span class="sxs-lookup"><span data-stu-id="65a34-111">A combination of one letter, seven digits, and one space:</span></span>
  
- <span data-ttu-id="65a34-112">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="65a34-112">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="65a34-113">Un espace (facultatif)</span><span class="sxs-lookup"><span data-stu-id="65a34-113">One space (optional)</span></span>
    
- <span data-ttu-id="65a34-114">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="65a34-114">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="65a34-115">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65a34-115">Checksum</span></span>

<span data-ttu-id="65a34-116">Non applicable</span><span class="sxs-lookup"><span data-stu-id="65a34-116">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="65a34-117">Définition</span><span class="sxs-lookup"><span data-stu-id="65a34-117">Definition</span></span>

<span data-ttu-id="65a34-118">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65a34-118">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65a34-119">L'expression `Regex_austria_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65a34-119">The regular expression  `Regex_austria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65a34-120">Un mot clé `Keywords_austria_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65a34-120">A keyword from  `Keywords_austria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_passport_number" />
          <Match idRef="Keywords_austria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="65a34-121">Mots clés</span><span class="sxs-lookup"><span data-stu-id="65a34-121">Keywords</span></span>

<span data-ttu-id="65a34-122">| |</span><span class="sxs-lookup"><span data-stu-id="65a34-122"></span></span>
|<span data-ttu-id="65a34-123">**Keywords_austria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="65a34-123">**Keywords_austria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="65a34-124">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-124">passport number</span></span>  <br/> <span data-ttu-id="65a34-125">Numéro de passeport autrichien</span><span class="sxs-lookup"><span data-stu-id="65a34-125">austrian passport number</span></span>  <br/> <span data-ttu-id="65a34-126">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-126">passport no</span></span>  <br/> <span data-ttu-id="65a34-127">Reisepass</span><span class="sxs-lookup"><span data-stu-id="65a34-127">reisepass</span></span>  <br/> <span data-ttu-id="65a34-128">österreichisch Reisepass</span><span class="sxs-lookup"><span data-stu-id="65a34-128">österreichisch reisepass</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="65a34-129">Belgique</span><span class="sxs-lookup"><span data-stu-id="65a34-129">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="65a34-130">Format</span><span class="sxs-lookup"><span data-stu-id="65a34-130">Format</span></span>

<span data-ttu-id="65a34-131">Deux lettres suivies de six chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="65a34-131">Two letters followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65a34-132">Modèle</span><span class="sxs-lookup"><span data-stu-id="65a34-132">Pattern</span></span>

<span data-ttu-id="65a34-133">Deux lettres et suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="65a34-133">Two letters and followed by six digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="65a34-134">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65a34-134">Checksum</span></span>

<span data-ttu-id="65a34-135">Non applicable</span><span class="sxs-lookup"><span data-stu-id="65a34-135">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="65a34-136">Définition</span><span class="sxs-lookup"><span data-stu-id="65a34-136">Definition</span></span>

<span data-ttu-id="65a34-137">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65a34-137">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65a34-138">L'expression `Regex_belgium_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65a34-138">The regular expression  `Regex_belgium_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65a34-139">Un mot clé `Keywords_belgium_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65a34-139">A keyword from  `Keywords_belgium_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium__eu_passport_number" />
          <Match idRef="Keywords_belgium_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="65a34-140">Mots clés</span><span class="sxs-lookup"><span data-stu-id="65a34-140">Keywords</span></span>

<span data-ttu-id="65a34-141">| |</span><span class="sxs-lookup"><span data-stu-id="65a34-141"></span></span>
|<span data-ttu-id="65a34-142">**Keywords_belgium_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="65a34-142">**Keywords_belgium_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="65a34-143">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-143">passport number</span></span>  <br/> <span data-ttu-id="65a34-144">Numéro de passeport belge</span><span class="sxs-lookup"><span data-stu-id="65a34-144">belgian passport number</span></span>  <br/> <span data-ttu-id="65a34-145">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-145">passport no</span></span>  <br/> <span data-ttu-id="65a34-146">paspoort</span><span class="sxs-lookup"><span data-stu-id="65a34-146">paspoort</span></span>  <br/> <span data-ttu-id="65a34-147">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="65a34-147">paspoortnummer</span></span>  <br/> <span data-ttu-id="65a34-148">Reisepass kein</span><span class="sxs-lookup"><span data-stu-id="65a34-148">reisepass kein</span></span>  <br/> <span data-ttu-id="65a34-149">Reisepass</span><span class="sxs-lookup"><span data-stu-id="65a34-149">reisepass</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="65a34-150">Bulgarie</span><span class="sxs-lookup"><span data-stu-id="65a34-150">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="65a34-151">Format</span><span class="sxs-lookup"><span data-stu-id="65a34-151">Format</span></span>

<span data-ttu-id="65a34-152">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="65a34-152">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65a34-153">Modèle</span><span class="sxs-lookup"><span data-stu-id="65a34-153">Pattern</span></span>

 <span data-ttu-id="65a34-154">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="65a34-154">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="65a34-155">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65a34-155">Checksum</span></span>

<span data-ttu-id="65a34-156">Non</span><span class="sxs-lookup"><span data-stu-id="65a34-156">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="65a34-157">Définition</span><span class="sxs-lookup"><span data-stu-id="65a34-157">Definition</span></span>

<span data-ttu-id="65a34-158">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65a34-158">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65a34-159">L'expression `Regex_bulgaria_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65a34-159">The regular expression  `Regex_bulgaria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65a34-160">Un mot clé `Keywords_bulgaria_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65a34-160">A keyword from  `Keywords_bulgaria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_passport_number" />
          <Match idRef="Keywords_bulgaria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="65a34-161">Mots clés</span><span class="sxs-lookup"><span data-stu-id="65a34-161">Keywords</span></span>

<span data-ttu-id="65a34-162">| |</span><span class="sxs-lookup"><span data-stu-id="65a34-162"></span></span>
|<span data-ttu-id="65a34-163">**Keywords_bulgaria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="65a34-163">**Keywords_bulgaria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="65a34-164">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-164">passport number</span></span>  <br/> <span data-ttu-id="65a34-165">Numéro de Passeport bulgare</span><span class="sxs-lookup"><span data-stu-id="65a34-165">bulgarian passport number</span></span>  <br/> <span data-ttu-id="65a34-166">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-166">passport no</span></span>  <br/> <span data-ttu-id="65a34-167">номер на паспорта</span><span class="sxs-lookup"><span data-stu-id="65a34-167">номер на паспорта</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="65a34-168">Croatie</span><span class="sxs-lookup"><span data-stu-id="65a34-168">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="65a34-169">Format</span><span class="sxs-lookup"><span data-stu-id="65a34-169">Format</span></span>

<span data-ttu-id="65a34-170">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="65a34-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65a34-171">Modèle</span><span class="sxs-lookup"><span data-stu-id="65a34-171">Pattern</span></span>

 <span data-ttu-id="65a34-172">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="65a34-172">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="65a34-173">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65a34-173">Checksum</span></span>

<span data-ttu-id="65a34-174">Non</span><span class="sxs-lookup"><span data-stu-id="65a34-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="65a34-175">Définition</span><span class="sxs-lookup"><span data-stu-id="65a34-175">Definition</span></span>

<span data-ttu-id="65a34-176">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65a34-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65a34-177">L'expression `Regex_croatia_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65a34-177">The regular expression  `Regex_croatia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65a34-178">Un mot clé `Keywords_croatia_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65a34-178">A keyword from  `Keywords_croatia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_passport_number" />
          <Match idRef="Keywords_croatia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="65a34-179">Mots clés</span><span class="sxs-lookup"><span data-stu-id="65a34-179">Keywords</span></span>

<span data-ttu-id="65a34-180">| |</span><span class="sxs-lookup"><span data-stu-id="65a34-180"></span></span>
|<span data-ttu-id="65a34-181">**Keywords_croatia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="65a34-181">**Keywords_croatia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="65a34-182">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-182">passport number</span></span>  <br/> <span data-ttu-id="65a34-183">Numéro de passeport croate</span><span class="sxs-lookup"><span data-stu-id="65a34-183">croatian passport number</span></span>  <br/> <span data-ttu-id="65a34-184">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-184">passport no</span></span>  <br/> <span data-ttu-id="65a34-185">Broj putovnice</span><span class="sxs-lookup"><span data-stu-id="65a34-185">broj putovnice</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="65a34-186">Chypre</span><span class="sxs-lookup"><span data-stu-id="65a34-186">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="65a34-187">Format</span><span class="sxs-lookup"><span data-stu-id="65a34-187">Format</span></span>

<span data-ttu-id="65a34-188">Une lettre suivie de 6-8 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="65a34-188">One letter followed by 6-8 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65a34-189">Modèle</span><span class="sxs-lookup"><span data-stu-id="65a34-189">Pattern</span></span>

<span data-ttu-id="65a34-190">Une lettre suivie de six à huit chiffres</span><span class="sxs-lookup"><span data-stu-id="65a34-190">One letter followed by six to eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="65a34-191">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65a34-191">Checksum</span></span>

<span data-ttu-id="65a34-192">Non</span><span class="sxs-lookup"><span data-stu-id="65a34-192">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="65a34-193">Définition</span><span class="sxs-lookup"><span data-stu-id="65a34-193">Definition</span></span>

<span data-ttu-id="65a34-194">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65a34-194">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65a34-195">L'expression `Regex_cyprus_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65a34-195">The regular expression  `Regex_cyprus_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65a34-196">Un mot clé `Keywords_cyprus_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65a34-196">A keyword from  `Keywords_cyprus_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_passport_number" />
          <Match idRef="Keywords_cyprus_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="65a34-197">Mots clés</span><span class="sxs-lookup"><span data-stu-id="65a34-197">Keywords</span></span>

<span data-ttu-id="65a34-198">| |</span><span class="sxs-lookup"><span data-stu-id="65a34-198"></span></span>
|<span data-ttu-id="65a34-199">**Keywords_cyprus_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="65a34-199">**Keywords_cyprus_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="65a34-200">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-200">passport number</span></span>  <br/> <span data-ttu-id="65a34-201">Numéro de passeport de Chypre</span><span class="sxs-lookup"><span data-stu-id="65a34-201">cyprus passport number</span></span>  <br/> <span data-ttu-id="65a34-202">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-202">passport no</span></span>  <br/> <span data-ttu-id="65a34-203">αριθμό διαβατηρίου</span><span class="sxs-lookup"><span data-stu-id="65a34-203">αριθμό διαβατηρίου</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="65a34-204">République tchèque</span><span class="sxs-lookup"><span data-stu-id="65a34-204">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="65a34-205">Format</span><span class="sxs-lookup"><span data-stu-id="65a34-205">Format</span></span>

<span data-ttu-id="65a34-206">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="65a34-206">Eight digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65a34-207">Modèle</span><span class="sxs-lookup"><span data-stu-id="65a34-207">Pattern</span></span>

<span data-ttu-id="65a34-208">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="65a34-208">Eight digits without spaces or delimiters</span></span>
  
### <a name="checksum"></a><span data-ttu-id="65a34-209">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65a34-209">Checksum</span></span>

<span data-ttu-id="65a34-210">Non</span><span class="sxs-lookup"><span data-stu-id="65a34-210">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="65a34-211">Définition</span><span class="sxs-lookup"><span data-stu-id="65a34-211">Definition</span></span>

<span data-ttu-id="65a34-212">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65a34-212">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65a34-213">L'expression `Regex_czech_republic_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65a34-213">The regular expression  `Regex_czech_republic_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65a34-214">Un mot clé `Keywords_czech_republic_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65a34-214">A keyword from  `Keywords_czech_republic_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_passport_number" />
          <Match idRef="Keywords_czech_republic_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="65a34-215">Mots clés</span><span class="sxs-lookup"><span data-stu-id="65a34-215">Keywords</span></span>

<span data-ttu-id="65a34-216">| |</span><span class="sxs-lookup"><span data-stu-id="65a34-216"></span></span>
|<span data-ttu-id="65a34-217">**Keywords_czech_republic_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="65a34-217">**Keywords_czech_republic_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="65a34-218">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-218">passport number</span></span>  <br/> <span data-ttu-id="65a34-219">Numéro de passeport tchèque</span><span class="sxs-lookup"><span data-stu-id="65a34-219">czech passport number</span></span>  <br/> <span data-ttu-id="65a34-220">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-220">passport no</span></span>  <br/> <span data-ttu-id="65a34-221">CESTOVNÍ pas</span><span class="sxs-lookup"><span data-stu-id="65a34-221">cestovní pas</span></span>  <br/> <span data-ttu-id="65a34-222">boîte</span><span class="sxs-lookup"><span data-stu-id="65a34-222">pas</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="65a34-223">Danemark</span><span class="sxs-lookup"><span data-stu-id="65a34-223">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="65a34-224">Format</span><span class="sxs-lookup"><span data-stu-id="65a34-224">Format</span></span>

<span data-ttu-id="65a34-225">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="65a34-225">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65a34-226">Modèle</span><span class="sxs-lookup"><span data-stu-id="65a34-226">Pattern</span></span>

 <span data-ttu-id="65a34-227">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="65a34-227">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="65a34-228">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65a34-228">Checksum</span></span>

<span data-ttu-id="65a34-229">Non</span><span class="sxs-lookup"><span data-stu-id="65a34-229">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="65a34-230">Définition</span><span class="sxs-lookup"><span data-stu-id="65a34-230">Definition</span></span>

<span data-ttu-id="65a34-231">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65a34-231">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65a34-232">L'expression `Regex_denmark_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65a34-232">The regular expression  `Regex_denmark_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65a34-233">Un mot clé `Keywords_denmark_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65a34-233">A keyword from  `Keywords_denmark_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_passport_number" />
          <Match idRef="Keywords_denmark_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="65a34-234">Mots clés</span><span class="sxs-lookup"><span data-stu-id="65a34-234">Keywords</span></span>

<span data-ttu-id="65a34-235">| |</span><span class="sxs-lookup"><span data-stu-id="65a34-235"></span></span>
|<span data-ttu-id="65a34-236">**Keywords_denmark_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="65a34-236">**Keywords_denmark_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="65a34-237">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-237">passport number</span></span>  <br/> <span data-ttu-id="65a34-238">Numéro de passeport danois</span><span class="sxs-lookup"><span data-stu-id="65a34-238">danish passport number</span></span>  <br/> <span data-ttu-id="65a34-239">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-239">passport no</span></span>  <br/> <span data-ttu-id="65a34-240">boîte</span><span class="sxs-lookup"><span data-stu-id="65a34-240">pas</span></span>  <br/> <span data-ttu-id="65a34-241">pasnummer</span><span class="sxs-lookup"><span data-stu-id="65a34-241">pasnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="65a34-242">Estonie</span><span class="sxs-lookup"><span data-stu-id="65a34-242">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="65a34-243">Format</span><span class="sxs-lookup"><span data-stu-id="65a34-243">Format</span></span>

<span data-ttu-id="65a34-244">Une lettre suivie de sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="65a34-244">One letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65a34-245">Modèle</span><span class="sxs-lookup"><span data-stu-id="65a34-245">Pattern</span></span>

<span data-ttu-id="65a34-246">Une lettre suivie de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="65a34-246">One letter followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="65a34-247">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65a34-247">Checksum</span></span>

<span data-ttu-id="65a34-248">Non</span><span class="sxs-lookup"><span data-stu-id="65a34-248">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="65a34-249">Définition</span><span class="sxs-lookup"><span data-stu-id="65a34-249">Definition</span></span>

<span data-ttu-id="65a34-250">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65a34-250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65a34-251">L'expression `Regex_estonia_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65a34-251">The regular expression  `Regex_estonia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65a34-252">Un mot clé `Keywords_estonia_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65a34-252">A keyword from  `Keywords_estonia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_passport_number" />
          <Match idRef="Keywords_estonia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="65a34-253">Mots clés</span><span class="sxs-lookup"><span data-stu-id="65a34-253">Keywords</span></span>

<span data-ttu-id="65a34-254">| |</span><span class="sxs-lookup"><span data-stu-id="65a34-254"></span></span>
|<span data-ttu-id="65a34-255">**Keywords_estonia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="65a34-255">**Keywords_estonia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="65a34-256">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-256">passport number</span></span>  <br/> <span data-ttu-id="65a34-257">Numéro de passeport estonien</span><span class="sxs-lookup"><span data-stu-id="65a34-257">estonian passport number</span></span>  <br/> <span data-ttu-id="65a34-258">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-258">passport no</span></span>  <br/> <span data-ttu-id="65a34-259">Eesti kodaniku</span><span class="sxs-lookup"><span data-stu-id="65a34-259">eesti kodaniku pass</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="65a34-260">Finlande</span><span class="sxs-lookup"><span data-stu-id="65a34-260">Finland</span></span>

<span data-ttu-id="65a34-261">Pour plus d'informations, consultez la section «numéro de passeport de Finlande» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="65a34-261">For details, see the section "Finland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="65a34-262">France</span><span class="sxs-lookup"><span data-stu-id="65a34-262">France</span></span>

<span data-ttu-id="65a34-263">Pour plus d'informations, consultez la section «numéro de passeport français» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="65a34-263">For details, see the section "France Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="65a34-264">Allemagne</span><span class="sxs-lookup"><span data-stu-id="65a34-264">Germany</span></span>

<span data-ttu-id="65a34-265">Pour plus d'informations, reportez-vous à la section «numéro de passeport allemand» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="65a34-265">For details, see the section "Germany Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="65a34-266">Grèce</span><span class="sxs-lookup"><span data-stu-id="65a34-266">Greece</span></span>

### <a name="format"></a><span data-ttu-id="65a34-267">Format</span><span class="sxs-lookup"><span data-stu-id="65a34-267">Format</span></span>

<span data-ttu-id="65a34-268">Deux lettres suivies de sept chiffres, sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="65a34-268">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65a34-269">Modèle</span><span class="sxs-lookup"><span data-stu-id="65a34-269">Pattern</span></span>

<span data-ttu-id="65a34-270">Deux lettres suivies de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="65a34-270">Two letters followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="65a34-271">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65a34-271">Checksum</span></span>

<span data-ttu-id="65a34-272">Non</span><span class="sxs-lookup"><span data-stu-id="65a34-272">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="65a34-273">Définition</span><span class="sxs-lookup"><span data-stu-id="65a34-273">Definition</span></span>

<span data-ttu-id="65a34-274">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65a34-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65a34-275">L'expression `Regex_greece_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65a34-275">The regular expression  `Regex_greece_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65a34-276">Un mot clé `Keywords_greece_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65a34-276">A keyword from  `Keywords_greece_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_passport_number" />
          <Match idRef="Keywords_greece_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="65a34-277">Mots clés</span><span class="sxs-lookup"><span data-stu-id="65a34-277">Keywords</span></span>

<span data-ttu-id="65a34-278">| |</span><span class="sxs-lookup"><span data-stu-id="65a34-278"></span></span>
|<span data-ttu-id="65a34-279">**Keywords_greece_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="65a34-279">**Keywords_greece_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="65a34-280">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-280">passport number</span></span>  <br/> <span data-ttu-id="65a34-281">Numéro de passeport grec</span><span class="sxs-lookup"><span data-stu-id="65a34-281">greek passport number</span></span>  <br/> <span data-ttu-id="65a34-282">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-282">passport no</span></span>  <br/> <span data-ttu-id="65a34-283">διαβατηριο</span><span class="sxs-lookup"><span data-stu-id="65a34-283">διαβατηριο</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="65a34-284">Hongrie</span><span class="sxs-lookup"><span data-stu-id="65a34-284">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="65a34-285">Format</span><span class="sxs-lookup"><span data-stu-id="65a34-285">Format</span></span>

<span data-ttu-id="65a34-286">Deux lettres suivies de six ou sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="65a34-286">Two letters followed by six or seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65a34-287">Modèle</span><span class="sxs-lookup"><span data-stu-id="65a34-287">Pattern</span></span>

<span data-ttu-id="65a34-288">Deux lettres suivies de six ou sept chiffres</span><span class="sxs-lookup"><span data-stu-id="65a34-288">Two letters followed by six or seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="65a34-289">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65a34-289">Checksum</span></span>

<span data-ttu-id="65a34-290">Non</span><span class="sxs-lookup"><span data-stu-id="65a34-290">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="65a34-291">Définition</span><span class="sxs-lookup"><span data-stu-id="65a34-291">Definition</span></span>

<span data-ttu-id="65a34-292">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65a34-292">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65a34-293">L'expression `Regex_hungary_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65a34-293">The regular expression  `Regex_hungary_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65a34-294">Un mot clé `Keywords_hungary_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65a34-294">A keyword from  `Keywords_hungary_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_passport_number" />
          <Match idRef="Keywords_hungary_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="65a34-295">Mots clés</span><span class="sxs-lookup"><span data-stu-id="65a34-295">Keywords</span></span>

<span data-ttu-id="65a34-296">| |</span><span class="sxs-lookup"><span data-stu-id="65a34-296"></span></span>
|<span data-ttu-id="65a34-297">**Keywords_hungary_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="65a34-297">**Keywords_hungary_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="65a34-298">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-298">passport number</span></span>  <br/> <span data-ttu-id="65a34-299">Numéro de passeport hongrois</span><span class="sxs-lookup"><span data-stu-id="65a34-299">hungarian passport number</span></span>  <br/> <span data-ttu-id="65a34-300">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-300">passport no</span></span>  <br/> <span data-ttu-id="65a34-301">útlevél száma</span><span class="sxs-lookup"><span data-stu-id="65a34-301">útlevél száma</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="65a34-302">Irlande</span><span class="sxs-lookup"><span data-stu-id="65a34-302">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="65a34-303">Format</span><span class="sxs-lookup"><span data-stu-id="65a34-303">Format</span></span>

<span data-ttu-id="65a34-304">Deux lettres ou chiffres suivis de sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="65a34-304">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65a34-305">Modèle</span><span class="sxs-lookup"><span data-stu-id="65a34-305">Pattern</span></span>

<span data-ttu-id="65a34-306">Deux lettres ou chiffres suivis de sept chiffres:</span><span class="sxs-lookup"><span data-stu-id="65a34-306">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="65a34-307">Deux chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="65a34-307">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="65a34-308">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="65a34-308">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="65a34-309">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65a34-309">Checksum</span></span>

<span data-ttu-id="65a34-310">Non</span><span class="sxs-lookup"><span data-stu-id="65a34-310">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="65a34-311">Définition</span><span class="sxs-lookup"><span data-stu-id="65a34-311">Definition</span></span>

<span data-ttu-id="65a34-312">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65a34-312">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65a34-313">L'expression `Regex_ireland_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65a34-313">The regular expression  `Regex_ireland_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65a34-314">Un mot clé `Keywords_ireland_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65a34-314">A keyword from  `Keywords_ireland_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_passport_number" />
          <Match idRef="Keywords_ireland_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="65a34-315">Mots clés</span><span class="sxs-lookup"><span data-stu-id="65a34-315">Keywords</span></span>

<span data-ttu-id="65a34-316">| |</span><span class="sxs-lookup"><span data-stu-id="65a34-316"></span></span>
|<span data-ttu-id="65a34-317">**Keywords_ireland_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="65a34-317">**Keywords_ireland_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="65a34-318">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-318">passport number</span></span>  <br/> <span data-ttu-id="65a34-319">Numéro de passeport irlandais</span><span class="sxs-lookup"><span data-stu-id="65a34-319">irish passport number</span></span>  <br/> <span data-ttu-id="65a34-320">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-320">passport no</span></span>  <br/> <span data-ttu-id="65a34-321">boîte</span><span class="sxs-lookup"><span data-stu-id="65a34-321">pas</span></span>  <br/> <span data-ttu-id="65a34-322">tel</span><span class="sxs-lookup"><span data-stu-id="65a34-322">passport</span></span>  <br/> <span data-ttu-id="65a34-323">passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-323">passeport</span></span>  <br/> <span data-ttu-id="65a34-324">passeport numérique</span><span class="sxs-lookup"><span data-stu-id="65a34-324">passeport numero</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="65a34-325">Italie</span><span class="sxs-lookup"><span data-stu-id="65a34-325">Italy</span></span>

### <a name="format"></a><span data-ttu-id="65a34-326">Format</span><span class="sxs-lookup"><span data-stu-id="65a34-326">Format</span></span>

<span data-ttu-id="65a34-327">Deux lettres ou chiffres suivis de sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="65a34-327">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65a34-328">Modèle</span><span class="sxs-lookup"><span data-stu-id="65a34-328">Pattern</span></span>

<span data-ttu-id="65a34-329">Deux lettres ou chiffres suivis de sept chiffres:</span><span class="sxs-lookup"><span data-stu-id="65a34-329">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="65a34-330">Deux chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="65a34-330">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="65a34-331">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="65a34-331">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="65a34-332">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65a34-332">Checksum</span></span>

<span data-ttu-id="65a34-333">Non applicable</span><span class="sxs-lookup"><span data-stu-id="65a34-333">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="65a34-334">Définition</span><span class="sxs-lookup"><span data-stu-id="65a34-334">Definition</span></span>

<span data-ttu-id="65a34-335">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65a34-335">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65a34-336">L'expression `Regex_italy_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65a34-336">The regular expression  `Regex_italy_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65a34-337">Un mot clé `Keywords_italy_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65a34-337">A keyword from  `Keywords_italy_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_passport_number" />
          <Match idRef="Keywords_italy_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="65a34-338">Mots clés</span><span class="sxs-lookup"><span data-stu-id="65a34-338">Keywords</span></span>

<span data-ttu-id="65a34-339">| |</span><span class="sxs-lookup"><span data-stu-id="65a34-339"></span></span>
|<span data-ttu-id="65a34-340">**Keywords_italy_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="65a34-340">**Keywords_italy_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="65a34-341">Numéro de passeport italien</span><span class="sxs-lookup"><span data-stu-id="65a34-341">italian passport number</span></span>  <br/> <span data-ttu-id="65a34-342">Repubblica Italiana passaporto</span><span class="sxs-lookup"><span data-stu-id="65a34-342">repubblica italiana passaporto</span></span>  <br/> <span data-ttu-id="65a34-343">passaporto</span><span class="sxs-lookup"><span data-stu-id="65a34-343">passaporto</span></span>  <br/> <span data-ttu-id="65a34-344">passaporto Italiana</span><span class="sxs-lookup"><span data-stu-id="65a34-344">passaporto italiana</span></span>  <br/> <span data-ttu-id="65a34-345">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-345">passport number</span></span>  <br/> <span data-ttu-id="65a34-346">Italiana passaporto numérique</span><span class="sxs-lookup"><span data-stu-id="65a34-346">italiana passaporto numero</span></span>  <br/> <span data-ttu-id="65a34-347">passaporto numérique</span><span class="sxs-lookup"><span data-stu-id="65a34-347">passaporto numero</span></span>  <br/> <span data-ttu-id="65a34-348">numéro passeport italien</span><span class="sxs-lookup"><span data-stu-id="65a34-348">numéro passeport italien</span></span>  <br/> <span data-ttu-id="65a34-349">numéro passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-349">numéro passeport</span></span>  <br/> |
   
## <a name="latvia"></a><span data-ttu-id="65a34-350">Lettonie</span><span class="sxs-lookup"><span data-stu-id="65a34-350">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="65a34-351">Format</span><span class="sxs-lookup"><span data-stu-id="65a34-351">Format</span></span>

<span data-ttu-id="65a34-352">Deux lettres ou chiffres suivis de sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="65a34-352">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65a34-353">Modèle</span><span class="sxs-lookup"><span data-stu-id="65a34-353">Pattern</span></span>

<span data-ttu-id="65a34-354">Deux lettres ou chiffres suivis de sept chiffres:</span><span class="sxs-lookup"><span data-stu-id="65a34-354">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="65a34-355">Deux chiffres ou lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="65a34-355">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="65a34-356">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="65a34-356">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="65a34-357">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65a34-357">Checksum</span></span>

<span data-ttu-id="65a34-358">Non</span><span class="sxs-lookup"><span data-stu-id="65a34-358">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="65a34-359">Définition</span><span class="sxs-lookup"><span data-stu-id="65a34-359">Definition</span></span>

<span data-ttu-id="65a34-360">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65a34-360">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65a34-361">L'expression `Regex_latvia_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65a34-361">The regular expression  `Regex_latvia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65a34-362">Un mot clé `Keywords_latvia_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65a34-362">A keyword from  `Keywords_latvia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_passport_number" />
          <Match idRef="Keywords_latvia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="65a34-363">Mots clés</span><span class="sxs-lookup"><span data-stu-id="65a34-363">Keywords</span></span>

<span data-ttu-id="65a34-364">| |</span><span class="sxs-lookup"><span data-stu-id="65a34-364"></span></span>
|<span data-ttu-id="65a34-365">**Keywords_latvia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="65a34-365">**Keywords_latvia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="65a34-366">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-366">passport number</span></span>  <br/> <span data-ttu-id="65a34-367">Numéro de passeport letton</span><span class="sxs-lookup"><span data-stu-id="65a34-367">latvian passport number</span></span>  <br/> <span data-ttu-id="65a34-368">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-368">passport no</span></span>  <br/> <span data-ttu-id="65a34-369">pase numurs</span><span class="sxs-lookup"><span data-stu-id="65a34-369">pase numurs</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="65a34-370">Lituanie</span><span class="sxs-lookup"><span data-stu-id="65a34-370">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="65a34-371">Format</span><span class="sxs-lookup"><span data-stu-id="65a34-371">Format</span></span>

<span data-ttu-id="65a34-372">Huit chiffres ou lettres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="65a34-372">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65a34-373">Modèle</span><span class="sxs-lookup"><span data-stu-id="65a34-373">Pattern</span></span>

<span data-ttu-id="65a34-374">Huit chiffres ou lettres (ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="65a34-374">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="65a34-375">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65a34-375">Checksum</span></span>

<span data-ttu-id="65a34-376">Non applicable</span><span class="sxs-lookup"><span data-stu-id="65a34-376">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="65a34-377">Définition</span><span class="sxs-lookup"><span data-stu-id="65a34-377">Definition</span></span>

<span data-ttu-id="65a34-378">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65a34-378">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65a34-379">L'expression `Regex_lithuania_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65a34-379">The regular expression  `Regex_lithuania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65a34-380">Un mot clé `Keywords_lithuania_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65a34-380">A keyword from  `Keywords_lithuania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_passport_number" />
          <Match idRef="Keywords_lithuania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="65a34-381">Mots clés</span><span class="sxs-lookup"><span data-stu-id="65a34-381">Keywords</span></span>

<span data-ttu-id="65a34-382">| |</span><span class="sxs-lookup"><span data-stu-id="65a34-382"></span></span>
|<span data-ttu-id="65a34-383">**Keywords_lithuania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="65a34-383">**Keywords_lithuania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="65a34-384">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-384">passport number</span></span>  <br/> <span data-ttu-id="65a34-385">Numéro de passeport lithunian</span><span class="sxs-lookup"><span data-stu-id="65a34-385">lithunian passport number</span></span>  <br/> <span data-ttu-id="65a34-386">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-386">passport no</span></span>  <br/> <span data-ttu-id="65a34-387">Paso chiffres</span><span class="sxs-lookup"><span data-stu-id="65a34-387">paso numeris</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="65a34-388">Relatif</span><span class="sxs-lookup"><span data-stu-id="65a34-388">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="65a34-389">Format</span><span class="sxs-lookup"><span data-stu-id="65a34-389">Format</span></span>

<span data-ttu-id="65a34-390">Huit chiffres ou lettres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="65a34-390">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65a34-391">Modèle</span><span class="sxs-lookup"><span data-stu-id="65a34-391">Pattern</span></span>

<span data-ttu-id="65a34-392">Huit chiffres ou lettres (ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="65a34-392">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="65a34-393">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65a34-393">Checksum</span></span>

<span data-ttu-id="65a34-394">Non</span><span class="sxs-lookup"><span data-stu-id="65a34-394">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="65a34-395">Définition</span><span class="sxs-lookup"><span data-stu-id="65a34-395">Definition</span></span>

<span data-ttu-id="65a34-396">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65a34-396">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65a34-397">L'expression `Regex_nation_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65a34-397">The regular expression  `Regex_nation_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65a34-398">Un mot clé `Keywords_nation_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65a34-398">A keyword from  `Keywords_nation_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_nation_eu_passport_number" />
          <Match idRef="Keywords_nation_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="65a34-399">Mots clés</span><span class="sxs-lookup"><span data-stu-id="65a34-399">Keywords</span></span>

<span data-ttu-id="65a34-400">| |</span><span class="sxs-lookup"><span data-stu-id="65a34-400"></span></span>
|<span data-ttu-id="65a34-401">**Keywords_nation_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="65a34-401">**Keywords_nation_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="65a34-402">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-402">passport number</span></span>  <br/> <span data-ttu-id="65a34-403">Numéro de passeport letton</span><span class="sxs-lookup"><span data-stu-id="65a34-403">latvian passport number</span></span>  <br/> <span data-ttu-id="65a34-404">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-404">passport no</span></span>  <br/> <span data-ttu-id="65a34-405">passnummer</span><span class="sxs-lookup"><span data-stu-id="65a34-405">passnummer</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="65a34-406">Malte</span><span class="sxs-lookup"><span data-stu-id="65a34-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="65a34-407">Format</span><span class="sxs-lookup"><span data-stu-id="65a34-407">Format</span></span>

<span data-ttu-id="65a34-408">Sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="65a34-408">Seven digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65a34-409">Modèle</span><span class="sxs-lookup"><span data-stu-id="65a34-409">Pattern</span></span>

 <span data-ttu-id="65a34-410">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="65a34-410">Seven digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="65a34-411">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65a34-411">Checksum</span></span>

<span data-ttu-id="65a34-412">Non</span><span class="sxs-lookup"><span data-stu-id="65a34-412">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="65a34-413">Définition</span><span class="sxs-lookup"><span data-stu-id="65a34-413">Definition</span></span>

<span data-ttu-id="65a34-414">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65a34-414">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65a34-415">L'expression `Regex_malta_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65a34-415">The regular expression  `Regex_malta_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65a34-416">Un mot clé `Keywords_malta_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65a34-416">A keyword from  `Keywords_malta_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_passport_number" />
          <Match idRef="Keywords_malta_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="65a34-417">Mots clés</span><span class="sxs-lookup"><span data-stu-id="65a34-417">Keywords</span></span>

<span data-ttu-id="65a34-418">| |</span><span class="sxs-lookup"><span data-stu-id="65a34-418"></span></span>
|<span data-ttu-id="65a34-419">**Keywords_malta_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="65a34-419">**Keywords_malta_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="65a34-420">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-420">passport number</span></span>  <br/> <span data-ttu-id="65a34-421">Numéro de passeport maltais</span><span class="sxs-lookup"><span data-stu-id="65a34-421">maltese passport number</span></span>  <br/> <span data-ttu-id="65a34-422">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-422">passport no</span></span>  <br/> <span data-ttu-id="65a34-423">numru Tal-Passaport</span><span class="sxs-lookup"><span data-stu-id="65a34-423">numru tal-passaport</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="65a34-424">Pays-Bas</span><span class="sxs-lookup"><span data-stu-id="65a34-424">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="65a34-425">Format</span><span class="sxs-lookup"><span data-stu-id="65a34-425">Format</span></span>

<span data-ttu-id="65a34-426">Neuf lettres ou chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="65a34-426">Nine letters or digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65a34-427">Modèle</span><span class="sxs-lookup"><span data-stu-id="65a34-427">Pattern</span></span>

<span data-ttu-id="65a34-428">Neuf lettres ou chiffres</span><span class="sxs-lookup"><span data-stu-id="65a34-428">Nine letters or digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="65a34-429">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65a34-429">Checksum</span></span>

<span data-ttu-id="65a34-430">Non applicable</span><span class="sxs-lookup"><span data-stu-id="65a34-430">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="65a34-431">Définition</span><span class="sxs-lookup"><span data-stu-id="65a34-431">Definition</span></span>

<span data-ttu-id="65a34-432">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65a34-432">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65a34-433">L'expression `Regex_netherlands_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65a34-433">The regular expression  `Regex_netherlands_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65a34-434">Un mot clé `Keywords_netherlands_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65a34-434">A keyword from  `Keywords_netherlands_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_passport_number" />
          <Match idRef="Keywords_netherlands_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="65a34-435">Mots clés</span><span class="sxs-lookup"><span data-stu-id="65a34-435">Keywords</span></span>

<span data-ttu-id="65a34-436">| |</span><span class="sxs-lookup"><span data-stu-id="65a34-436"></span></span>
|<span data-ttu-id="65a34-437">**Keywords_netherlands_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="65a34-437">**Keywords_netherlands_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="65a34-438">Numéro de passeport néerlandais</span><span class="sxs-lookup"><span data-stu-id="65a34-438">dutch passport number</span></span>  <br/> <span data-ttu-id="65a34-439">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-439">passport number</span></span>  <br/> <span data-ttu-id="65a34-440">Numéro de passeport néerlandais</span><span class="sxs-lookup"><span data-stu-id="65a34-440">netherlands passport number</span></span>  <br/> <span data-ttu-id="65a34-441">Nederlanden paspoort Nummer</span><span class="sxs-lookup"><span data-stu-id="65a34-441">nederlanden paspoort nummer</span></span>  <br/> <span data-ttu-id="65a34-442">paspoort</span><span class="sxs-lookup"><span data-stu-id="65a34-442">paspoort</span></span>  <br/> <span data-ttu-id="65a34-443">Nederlanden paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="65a34-443">nederlanden paspoortnummer</span></span>  <br/> <span data-ttu-id="65a34-444">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="65a34-444">paspoortnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="65a34-445">Pologne</span><span class="sxs-lookup"><span data-stu-id="65a34-445">Poland</span></span>

<span data-ttu-id="65a34-446">Pour plus d'informations, reportez-vous à la section «numéro de passeport polonais» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="65a34-446">For details, see the section "Poland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="65a34-447">Portugal</span><span class="sxs-lookup"><span data-stu-id="65a34-447">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="65a34-448">Format</span><span class="sxs-lookup"><span data-stu-id="65a34-448">Format</span></span>

<span data-ttu-id="65a34-449">Une lettre suivie de six chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="65a34-449">One letter followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65a34-450">Modèle</span><span class="sxs-lookup"><span data-stu-id="65a34-450">Pattern</span></span>

<span data-ttu-id="65a34-451">Une lettre suivie de six chiffres:</span><span class="sxs-lookup"><span data-stu-id="65a34-451">One letter followed by six digits:</span></span>
  
- <span data-ttu-id="65a34-452">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="65a34-452">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="65a34-453">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="65a34-453">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="65a34-454">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65a34-454">Checksum</span></span>

<span data-ttu-id="65a34-455">Non</span><span class="sxs-lookup"><span data-stu-id="65a34-455">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="65a34-456">Définition</span><span class="sxs-lookup"><span data-stu-id="65a34-456">Definition</span></span>

<span data-ttu-id="65a34-457">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65a34-457">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65a34-458">L'expression `Regex_portugal_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65a34-458">The regular expression  `Regex_portugal_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65a34-459">Un mot clé `Keywords_portugal_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65a34-459">A keyword from  `Keywords_portugal_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_passport_number" />
          <Match idRef="Keywords_portugal_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="65a34-460">Mots clés</span><span class="sxs-lookup"><span data-stu-id="65a34-460">Keywords</span></span>

<span data-ttu-id="65a34-461">| |</span><span class="sxs-lookup"><span data-stu-id="65a34-461"></span></span>
|<span data-ttu-id="65a34-462">**Keywords_portugal_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="65a34-462">**Keywords_portugal_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="65a34-463">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-463">passport number</span></span>  <br/> <span data-ttu-id="65a34-464">Numéro de passeport Portugais</span><span class="sxs-lookup"><span data-stu-id="65a34-464">portuguese passport number</span></span>  <br/> <span data-ttu-id="65a34-465">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-465">passport no</span></span>  <br/> <span data-ttu-id="65a34-466">número do Passaporte</span><span class="sxs-lookup"><span data-stu-id="65a34-466">número do passaporte</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="65a34-467">Roumanie</span><span class="sxs-lookup"><span data-stu-id="65a34-467">Romania</span></span>

### <a name="format"></a><span data-ttu-id="65a34-468">Format</span><span class="sxs-lookup"><span data-stu-id="65a34-468">Format</span></span>

<span data-ttu-id="65a34-469">Huit ou neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="65a34-469">Eight or nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65a34-470">Modèle</span><span class="sxs-lookup"><span data-stu-id="65a34-470">Pattern</span></span>

<span data-ttu-id="65a34-471">Huit ou neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="65a34-471">Eight or nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="65a34-472">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65a34-472">Checksum</span></span>

<span data-ttu-id="65a34-473">Non</span><span class="sxs-lookup"><span data-stu-id="65a34-473">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="65a34-474">Définition</span><span class="sxs-lookup"><span data-stu-id="65a34-474">Definition</span></span>

<span data-ttu-id="65a34-475">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65a34-475">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65a34-476">L'expression `Regex_romania_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65a34-476">The regular expression  `Regex_romania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65a34-477">Un mot clé `Keywords_romania_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65a34-477">A keyword from  `Keywords_romania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_passport_number" />
          <Match idRef="Keywords_romania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="65a34-478">Mots clés</span><span class="sxs-lookup"><span data-stu-id="65a34-478">Keywords</span></span>

<span data-ttu-id="65a34-479">| |</span><span class="sxs-lookup"><span data-stu-id="65a34-479"></span></span>
|<span data-ttu-id="65a34-480">**Keywords_romania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="65a34-480">**Keywords_romania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="65a34-481">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-481">passport number</span></span>  <br/> <span data-ttu-id="65a34-482">Numéro de passeport roumain</span><span class="sxs-lookup"><span data-stu-id="65a34-482">romanian passport number</span></span>  <br/> <span data-ttu-id="65a34-483">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-483">passport no</span></span>  <br/> <span data-ttu-id="65a34-484">numărul pașaportului</span><span class="sxs-lookup"><span data-stu-id="65a34-484">numărul pașaportului</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="65a34-485">République de Slovaquie</span><span class="sxs-lookup"><span data-stu-id="65a34-485">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="65a34-486">Format</span><span class="sxs-lookup"><span data-stu-id="65a34-486">Format</span></span>

<span data-ttu-id="65a34-487">Un chiffre ou une lettre suivi de sept chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="65a34-487">One digit or letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65a34-488">Modèle</span><span class="sxs-lookup"><span data-stu-id="65a34-488">Pattern</span></span>

<span data-ttu-id="65a34-489">Un chiffre ou une lettre (ne respectant pas la casse) suivi de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="65a34-489">One digit or letter (not case sensitive) followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="65a34-490">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65a34-490">Checksum</span></span>

<span data-ttu-id="65a34-491">Non</span><span class="sxs-lookup"><span data-stu-id="65a34-491">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="65a34-492">Définition</span><span class="sxs-lookup"><span data-stu-id="65a34-492">Definition</span></span>

<span data-ttu-id="65a34-493">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65a34-493">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65a34-494">L'expression `Regex_slovakia_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65a34-494">The regular expression  `Regex_slovakia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65a34-495">Un mot clé `Keywords_slovakia_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65a34-495">A keyword from  `Keywords_slovakia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_passport_number" />
          <Match idRef="Keywords_slovakia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="65a34-496">Mots clés</span><span class="sxs-lookup"><span data-stu-id="65a34-496">Keywords</span></span>

<span data-ttu-id="65a34-497">| |</span><span class="sxs-lookup"><span data-stu-id="65a34-497"></span></span>
|<span data-ttu-id="65a34-498">**Keywords_slovakia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="65a34-498">**Keywords_slovakia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="65a34-499">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-499">passport number</span></span>  <br/> <span data-ttu-id="65a34-500">Numéro de passeport slovaque</span><span class="sxs-lookup"><span data-stu-id="65a34-500">slovakian passport number</span></span>  <br/> <span data-ttu-id="65a34-501">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-501">passport no</span></span>  <br/> <span data-ttu-id="65a34-502">číslo Pasu</span><span class="sxs-lookup"><span data-stu-id="65a34-502">číslo pasu</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="65a34-503">Slovénie</span><span class="sxs-lookup"><span data-stu-id="65a34-503">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="65a34-504">Format</span><span class="sxs-lookup"><span data-stu-id="65a34-504">Format</span></span>

<span data-ttu-id="65a34-505">Deux lettres suivies de sept chiffres, sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="65a34-505">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65a34-506">Modèle</span><span class="sxs-lookup"><span data-stu-id="65a34-506">Pattern</span></span>

<span data-ttu-id="65a34-507">Deux lettres suivies de sept chiffres:</span><span class="sxs-lookup"><span data-stu-id="65a34-507">Two letters followed by seven digits:</span></span>
  
- <span data-ttu-id="65a34-508">La lettre «P»</span><span class="sxs-lookup"><span data-stu-id="65a34-508">The letter "P"</span></span>
    
- <span data-ttu-id="65a34-509">Une lettre majuscule</span><span class="sxs-lookup"><span data-stu-id="65a34-509">One uppercase letter</span></span>
    
- <span data-ttu-id="65a34-510">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="65a34-510">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="65a34-511">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65a34-511">Checksum</span></span>

<span data-ttu-id="65a34-512">Non</span><span class="sxs-lookup"><span data-stu-id="65a34-512">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="65a34-513">Définition</span><span class="sxs-lookup"><span data-stu-id="65a34-513">Definition</span></span>

<span data-ttu-id="65a34-514">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65a34-514">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65a34-515">L'expression `Regex_slovenia_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65a34-515">The regular expression  `Regex_slovenia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65a34-516">Un mot clé `Keywords_slovenia_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65a34-516">A keyword from  `Keywords_slovenia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_passport_number" />
          <Match idRef="Keywords_slovenia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="65a34-517">Mots clés</span><span class="sxs-lookup"><span data-stu-id="65a34-517">Keywords</span></span>

<span data-ttu-id="65a34-518">| |</span><span class="sxs-lookup"><span data-stu-id="65a34-518"></span></span>
|<span data-ttu-id="65a34-519">**Keywords_slovenia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="65a34-519">**Keywords_slovenia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="65a34-520">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-520">passport number</span></span>  <br/> <span data-ttu-id="65a34-521">Numéro de passeport slovène</span><span class="sxs-lookup"><span data-stu-id="65a34-521">slovenian passport number</span></span>  <br/> <span data-ttu-id="65a34-522">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-522">passport no</span></span>  <br/> <span data-ttu-id="65a34-523">številka potnega Lista</span><span class="sxs-lookup"><span data-stu-id="65a34-523">številka potnega lista</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="65a34-524">Espagne</span><span class="sxs-lookup"><span data-stu-id="65a34-524">Spain</span></span>

### <a name="format"></a><span data-ttu-id="65a34-525">Format</span><span class="sxs-lookup"><span data-stu-id="65a34-525">Format</span></span>

<span data-ttu-id="65a34-526">Combinaison de huit ou neuf caractères de lettres et de chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="65a34-526">An eight- or nine-character combination of letters and numbers with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65a34-527">Modèle</span><span class="sxs-lookup"><span data-stu-id="65a34-527">Pattern</span></span>

<span data-ttu-id="65a34-528">Combinaison de huit ou neuf caractères de lettres et de chiffres:</span><span class="sxs-lookup"><span data-stu-id="65a34-528">An eight- or nine-character combination of letters and numbers:</span></span>
  
-  <span data-ttu-id="65a34-529">Deux chiffres ou lettres</span><span class="sxs-lookup"><span data-stu-id="65a34-529">Two digits or letters</span></span> 
    
- <span data-ttu-id="65a34-530">Un chiffre ou une lettre (facultatif)</span><span class="sxs-lookup"><span data-stu-id="65a34-530">One digit or letter (optional)</span></span>
    
- <span data-ttu-id="65a34-531">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="65a34-531">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="65a34-532">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65a34-532">Checksum</span></span>

<span data-ttu-id="65a34-533">Non applicable</span><span class="sxs-lookup"><span data-stu-id="65a34-533">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="65a34-534">Définition</span><span class="sxs-lookup"><span data-stu-id="65a34-534">Definition</span></span>

<span data-ttu-id="65a34-535">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65a34-535">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65a34-536">L'expression `Regex_spain_eu_passport_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65a34-536">The regular expression  `Regex_spain_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65a34-537">Un mot clé `Keywords_spain_eu_passport_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65a34-537">A keyword from  `Keywords_spain_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_passport_number" />
          <Match idRef="Keywords_spain_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="65a34-538">Mots clés</span><span class="sxs-lookup"><span data-stu-id="65a34-538">Keywords</span></span>

<span data-ttu-id="65a34-539">| |</span><span class="sxs-lookup"><span data-stu-id="65a34-539"></span></span>
|<span data-ttu-id="65a34-540">**Keywords_spain_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="65a34-540">**Keywords_spain_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="65a34-541">tel</span><span class="sxs-lookup"><span data-stu-id="65a34-541">passport</span></span>  <br/> <span data-ttu-id="65a34-542">Passport Espagne</span><span class="sxs-lookup"><span data-stu-id="65a34-542">spain passport</span></span>  <br/> <span data-ttu-id="65a34-543">livre de passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-543">passport book</span></span>  <br/> <span data-ttu-id="65a34-544">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-544">passport number</span></span>  <br/> <span data-ttu-id="65a34-545">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="65a34-545">passport no</span></span>  <br/> <span data-ttu-id="65a34-546">Libreta pasaporte</span><span class="sxs-lookup"><span data-stu-id="65a34-546">libreta pasaporte</span></span>  <br/> <span data-ttu-id="65a34-547">número pasaporte</span><span class="sxs-lookup"><span data-stu-id="65a34-547">número pasaporte</span></span>  <br/> <span data-ttu-id="65a34-548">España pasaporte</span><span class="sxs-lookup"><span data-stu-id="65a34-548">españa pasaporte</span></span>  <br/> <span data-ttu-id="65a34-549">pasaporte</span><span class="sxs-lookup"><span data-stu-id="65a34-549">pasaporte</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="65a34-550">Suède</span><span class="sxs-lookup"><span data-stu-id="65a34-550">Sweden</span></span>

<span data-ttu-id="65a34-551">Pour plus d'informations, reportez-vous à la section «numéro de passeport Suède» dans [ce que recherche les types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="65a34-551">For details, see the section "Sweden Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="uk"></a><span data-ttu-id="65a34-552">R.U.</span><span class="sxs-lookup"><span data-stu-id="65a34-552">UK</span></span>

<span data-ttu-id="65a34-553">Pour plus d'informations, reportez-vous à la section «U.S./R.U.</span><span class="sxs-lookup"><span data-stu-id="65a34-553">For details, see the section "U.S. / U.K.</span></span> <span data-ttu-id="65a34-554">Numéro de passeport» dans [ce que recherche les types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="65a34-554">Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="65a34-555">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65a34-555">See also</span></span>

[<span data-ttu-id="65a34-556">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="65a34-556">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

