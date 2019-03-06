---
title: Numéro de permis de conduire de l'UE
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: Cette rubrique présente ce qu'une stratégie de protection contre la perte de données (DLP) recherche lorsqu'elle détecte le type d'informations sensibles du pilote de l'UE. Ce type d'informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.
ms.openlocfilehash: be9497c325866a670dff8d82b5170f4ca947c4ad
ms.sourcegitcommit: ed822a776d3419853453583e882f3c61ca26d4b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "30410749"
---
# <a name="eu-drivers-license-number"></a>Numéro de permis de conduire de l'UE

Cette rubrique présente ce qu'une stratégie de protection contre la perte de données (DLP) recherche lorsqu'elle détecte le type d'informations sensibles du pilote de l'UE. Ce type d'informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.
  
## <a name="austria"></a>Autriche

### <a name="format"></a>Format

Huit chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

Huit chiffres
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_austria_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_austria_eu_driver's_license_number` from est trouvé. 
    
```
<!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_driver's_license_number" />
          <Match idRef="Keywords_austria_eu_driver's_license_number" />
        </Pattern>
    </Entity>

```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_austria_eu_driver's_license_number**|
|:-----|
|LD  <br/> Permis de conduire  <br/> Numéro de permis de conduire  <br/> permis de conduire  <br/> pilotes.  <br/> permis de conduire  <br/> permis de conduire  <br/> permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/>  Numéro de permis de conduire  <br/> dlno #  <br/> Fuhrerschein  <br/> Fuhrerschein Republik Osterreich  <br/> |
   
## <a name="belgium"></a>Belgique

### <a name="format"></a>Format

10 chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

10 chiffres
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_belgium_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_belgium_eu_driver's_license_number` from est trouvé. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_driver's_license_number" />
          <Match idRef="Keywords_belgium_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords__belgium_eu_driver's_license_number**|
|:-----|
|LD  <br/> Permis de conduire  <br/> Numéro de permis de conduire  <br/> permis de conduire  <br/> pilotes.  <br/> permis de conduire  <br/> permis de conduire  <br/> permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> dlno #  <br/> rijbewijs  <br/> rijbewijsnummer  <br/> führerscheinnummer  <br/> fuhrerscheinnummer  <br/> fuehrerscheinnummer  <br/> Führerschein-Nr  <br/> fuehrerschein-Nr  <br/> fuehrerschein-Nr  <br/> |
   
## <a name="bulgaria"></a>Bulgarie

### <a name="format"></a>Format

Neuf chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

Neuf chiffres
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_bulgaria_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_bulgaria_eu_driver's_license_number` from est trouvé. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
             <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_driver's_license_number" />
          <Match idRef="Keywords_bulgaria_eu_driver's_license_number" />
        </Pattern> 
</Entity>    

```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_bulgaria_eu_driver's_license_number**|
|:-----|
|LD  <br/> Permis de conduire  <br/> Numéro de permis de conduire  <br/> permis de conduire  <br/> pilotes.  <br/> permis de conduire  <br/> permis de conduire  <br/> permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> dlno #  <br/> свидетелство за Управление на мпс  <br/> свидетелство за Управление на моторно превозно средство  <br/> сумпс  <br/> шофьорска книжка  <br/> |
   
## <a name="croatia"></a>Croatie

### <a name="format"></a>Format

Huit chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

Huit chiffres
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_croatia_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_croatia_eu_driver's_license_number` from est trouvé. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_driver's_license_number" />
          <Match idRef="Keywords_croatia_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_croatia_eu_driver's_license_number**|
|:-----|
|LD  <br/> Permis de conduire  <br/> Numéro de permis de conduire  <br/> permis de conduire  <br/> pilotes.  <br/> permis de conduire  <br/> permis de conduire  <br/> permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> dlno #  <br/> vozačka Dozvola  <br/> |
   
## <a name="cyprus"></a>Chypre

### <a name="format"></a>Format

12 chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

12 chiffres
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_cyprus_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_cyprus_eu_driver's_license_number` from est trouvé. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_driver's_license_number" />
          <Match idRef="Keywords_cyprus_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_cyprus_eu_driver's_license_number**|
|:-----|
|LD  <br/> Permis de conduire  <br/> Numéro de permis de conduire  <br/> permis de conduire  <br/> pilotes.  <br/> permis de conduire  <br/> permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> dlno #  <br/> Άδεια Οδήγησης  <br/> |
   
## <a name="czech-republic"></a>République tchèque

### <a name="format"></a>Format

Deux lettres suivies de six chiffres
  
### <a name="pattern"></a>Modèle

Huit lettres et chiffres:
  
- Deux lettres (ne respectent pas la casse)
    
- Un espace (facultatif) 
    
- Six chiffres
    
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_czech_republic_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_czech_republic_eu_driver's_license_number` from est trouvé. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_driver's_license_number" />
          <Match idRef="Keywords_czech_republic_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_czech_republic_eu_driver's_license_number**|
|:-----|
|LD  <br/> Permis de conduire  <br/> Numéro de permis de conduire  <br/> permis de conduire  <br/> pilotes.  <br/> permis de conduire  <br/> permis de conduire  <br/> permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> dlno #  <br/> řidičský prúkaz  <br/> |
   
## <a name="denmark"></a>Danemark

### <a name="format"></a>Format

Huit chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

Huit chiffres
  
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_denmark_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_denmark_eu_driver's_license_number` from est trouvé. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_driver's_license_number" />
          <Match idRef="Keywords_denmark_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_denmark_eu_driver's_license_number**|
|:-----|
|LD  <br/> Permis de conduire  <br/> Numéro de permis de conduire  <br/> permis de conduire  <br/> pilotes.  <br/> permis de conduire  <br/> permis de conduire  <br/> permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> dlno #  <br/> Kørekort  <br/> kørekortnummer  <br/> |
   
## <a name="estonia"></a>Estonie

### <a name="format"></a>Format

Deux lettres suivies de six chiffres
  
### <a name="pattern"></a>Modèle

Deux lettres et six chiffres:
  
-  Les lettres "ET" (ne respectent pas la casse) 
    
- Six chiffres
    
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_estonia_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_estonia_eu_driver's_license_number` from est trouvé. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_driver's_license_number" />
          <Match idRef="Keywords_estonia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_estonia_eu_driver's_license_number**|
|:-----|
|LD  <br/> Permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> permis de conduire  <br/> pilotes.  <br/> permis de conduire  <br/> permis de conduire  <br/> permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> dlno #  <br/> permis de conduire  <br/> |
   
## <a name="finland"></a>Finlande

### <a name="format"></a>Format

10 chiffres contenant un trait d’union
  
### <a name="pattern"></a>Modèle

10 chiffres contenant un trait d'Union:
  
-  Six chiffres 
    
- Un trait d’union
    
-  Quatre chiffres 
    
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_finland_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_finland_eu_driver's_license_number` from est trouvé. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_driver's_license_number" />
          <Match idRef="Keywords_finland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_finland_eu_driver's_license_number**|
|:-----|
|LD  <br/> Permis de conduire  <br/> Numéro de permis de conduire  <br/> permis de conduire  <br/> pilotes.  <br/> permis de conduire  <br/> permis de conduire  <br/> permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> dlno #  <br/> Ajokortti  <br/> |
   
## <a name="france"></a>France

Pour plus d'informations, reportez-vous à la section «numéro de permis de conduire France» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="germany"></a>Allemagne

Pour plus d'informations, consultez la section «numéro de permis de conduire allemand» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="greece"></a>Grèce

### <a name="format"></a>Format

Neuf chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

 Neuf chiffres 
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_greece_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_greece_eu_driver's_license_number` from est trouvé. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_driver's_license_number" />
          <Match idRef="Keywords_greece_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_greece_eu_driver's_license_number**|
|:-----|
|Fichier  <br/> Permis de conduire  <br/> Numéro de permis de conduire  <br/> permis de conduire  <br/> pilotes.  <br/> permis de conduire  <br/> permis de conduire  <br/> permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> dlno #  <br/> δεια Οδήγησης  <br/> Adeia odigisis  <br/> |
   
## <a name="hungary"></a>Hongrie

### <a name="format"></a>Format

Deux lettres suivies de six chiffres
  
### <a name="pattern"></a>Modèle

Deux lettres et six chiffres:
  
-  Deux lettres (ne respectent pas la casse) 
    
- Six chiffres
    
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_hungary_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_hungary_eu_driver's_license_number` from est trouvé. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_driver's_license_number" />
          <Match idRef="Keywords_hungary_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_hungary_eu_driver's_license_number**|
|:-----|
|LD  <br/> Permis de conduire  <br/> Numéro de permis de conduire  <br/> permis de conduire  <br/> pilotes.  <br/> permis de conduire  <br/> permis de conduire  <br/> permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> dlno #  <br/> vezetoi engedely  <br/> |
   
## <a name="ireland"></a>Irlande

### <a name="format"></a>Format

Six chiffres suivis de quatre lettres
  
### <a name="pattern"></a>Modèle

Six chiffres et quatre lettres:
  
- Six chiffres
    
- Quatre lettres (ne respectent pas la casse)
    
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_ireland_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_ireland_eu_driver's_license_number` from est trouvé. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_driver's_license_number" />
          <Match idRef="Keywords_ireland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_ireland_eu_driver's_license_number**|
|:-----|
|LD  <br/> Permis de conduire  <br/> Numéro de permis de conduire  <br/> permis de conduire  <br/> pilotes.  <br/> permis de conduire  <br/> permis de conduire  <br/> permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> dlno #  <br/> Ceadúnas Tiomána  <br/> |
   
## <a name="italy"></a>Italie

Pour plus d'informations, reportez-vous à la section «Italie numéro de permis de conduire» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="latvia"></a>Lettonie

### <a name="format"></a>Format

Trois lettres suivies de six chiffres
  
### <a name="pattern"></a>Modèle

Trois lettres et six chiffres:
  
-  Trois lettres (ne respectent pas la casse) 
    
- Six chiffres
    
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_latvia_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_latvia_eu_driver's_license_number` from est trouvé. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_driver's_license_number" />
          <Match idRef="Keywords_latvia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_latvia_eu_driver's_license_number**|
|:-----|
|LD  <br/> Permis de conduire  <br/> Numéro de permis de conduire  <br/> permis de conduire  <br/> pilotes.  <br/> permis de conduire  <br/> permis de conduire  <br/> permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> dlno #  <br/> autovadītāja APLIECĪBA  <br/> |
   
## <a name="lithuania"></a>Lituanie

### <a name="format"></a>Format

Huit chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

 Huit chiffres 
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_lithuania_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_lithuania_eu_driver's_license_number` from est trouvé. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_driver's_license_number" />
          <Match idRef="Keywords_lithuania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_lithuania_eu_driver's_license_number**|
|:-----|
|LD  <br/> Permis de conduire  <br/> Numéro de permis de conduire  <br/> permis de conduire  <br/> pilotes.  <br/> permis de conduire  <br/> permis de conduire  <br/> permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> dlno #  <br/> vairuotojo pažymėjimas  <br/> |
   
## <a name="luxemburg"></a>Relatif

### <a name="format"></a>Format

Six chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

 Six chiffres 
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_luxemburg_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_luxemburg_eu_driver's_license_number` from est trouvé. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_driver's_license_number" />
          <Match idRef="Keywords_luxemburg_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_luxemburg_eu_driver's_license_number**|
|:-----|
|LD  <br/> Permis de conduire  <br/> Numéro de permis de conduire  <br/> permis de conduire  <br/> pilotes.  <br/> permis de conduire  <br/> permis de conduire  <br/> permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> dlno #  <br/> fahrerlaubnis  <br/> |
   
## <a name="malta"></a>Malte

### <a name="format"></a>Format

Combinaison de deux caractères et six chiffres dans le modèle spécifié
  
### <a name="pattern"></a>Modèle

Combinaison de deux caractères et six chiffres:
  
- Deux caractères (chiffres ou lettres, ne respectant pas la casse)
    
- Un espace (facultatif) 
    
- Trois chiffres
    
- Un espace (facultatif) 
    
- Trois chiffres
    
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_malta_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_malta_eu_driver's_license_number` from est trouvé. 
    
```
<!-- EU Driver's License Number -->
 <Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_driver's_license_number" />
          <Match idRef="Keywords_malta_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_malta_eu_driver's_license_number**|
|:-----|
|LD  <br/> Permis de conduire  <br/> Numéro de permis de conduire  <br/> permis de conduire  <br/> pilotes.  <br/> permis de conduire  <br/> permis de conduire  <br/> permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> dlno #  <br/> Liċenzja-sewqan  <br/> |
   
## <a name="netherlands"></a>Pays-Bas

### <a name="format"></a>Format

10 chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

10 chiffres
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_netherlands_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_netherlands_eu_driver's_license_number` from est trouvé. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_driver's_license_number" />
          <Match idRef="Keywords_netherlands_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_netherlands_eu_driver's_license_number**|
|:-----|
|LD  <br/> Permis de conduire  <br/> Numéro de permis de conduire  <br/> permis de conduire  <br/> pilotes.  <br/> permis de conduire  <br/> permis de conduire  <br/> permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> dlno #  <br/> permis de conduire  <br/> rijbewijs  <br/> rijbewijsnummer  <br/> |
   
## <a name="poland"></a>Pologne

### <a name="format"></a>Format

14 chiffres contenant 2 barres obliques
  
### <a name="pattern"></a>Modèle

14 chiffres et 2 barres obliques:
  
-  Cinq chiffres 
    
- Une barre oblique 
    
- Deux chiffres
    
- Une barre oblique 
    
- Sept chiffres
    
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_poland_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_poland_eu_driver's_license_number` from est trouvé. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_driver's_license_number" />
          <Match idRef="Keywords_poland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_poland_eu_driver's_license_number**|
|:-----|
|LD  <br/> Permis de conduire  <br/> Numéro de permis de conduire  <br/> permis de conduire  <br/> pilotes.  <br/> permis de conduire  <br/> permis de conduire  <br/> permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> dlno #  <br/> Prawo jazdy  <br/> |
   
## <a name="portugal"></a>Portugal

### <a name="format"></a>Format

Deux lettres suivies d'un nombre de sept chiffres dans le modèle spécifié
  
### <a name="pattern"></a>Modèle

Deux lettres suivies de sept chiffres avec des caractères spéciaux:
  
-  Deux lettres (ne respectent pas la casse) 
    
- Un trait d’union 
    
- Six chiffres
    
- Un espace
    
- Un chiffre
    
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_portugal_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_portugal_eu_driver's_license_number` from est trouvé. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_driver's_license_number" />
          <Match idRef="Keywords_portugal_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_portugal_eu_driver's_license_number**|
|:-----|
|LD  <br/> Permis de conduire  <br/> Numéro de permis de conduire  <br/> permis de conduire  <br/> pilotes.  <br/> permis de conduire  <br/> permis de conduire  <br/> permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> dlno #  <br/> Carteira de motorista  <br/> |
   
## <a name="romania"></a>Roumanie

### <a name="format"></a>Format

Un caractère suivi de huit chiffres
  
### <a name="pattern"></a>Modèle

Un caractère suivi de huit chiffres:
  
-  Une lettre (ne respecte pas la casse) ou un chiffre 
    
- Huit chiffres
    
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_romania_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_romania_eu_driver's_license_number` from est trouvé. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_driver's_license_number" />
          <Match idRef="Keywords_romania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_romania_eu_driver's_license_number**|
|:-----|
|LD  <br/> Permis de conduire  <br/> Numéro de permis de conduire  <br/> permis de conduire  <br/> pilotes.  <br/> permis de conduire  <br/> permis de conduire  <br/> permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> dlno #  <br/> permis de conducere  <br/> |
   
## <a name="slovakia"></a>République de Slovaquie

### <a name="format"></a>Format

Un caractère suivi de sept chiffres
  
### <a name="pattern"></a>Modèle

Un caractère suivi de sept chiffres
  
- Une lettre (ne respecte pas la casse) ou un chiffre
    
-  Sept chiffres 
    
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_slovakia_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_slovakia_eu_driver's_license_number` from est trouvé. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovaknia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovakia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_slovakia_eu_driver's_license_number**|
|:-----|
|LD  <br/> Permis de conduire  <br/> Numéro de permis de conduire  <br/> permis de conduire  <br/> pilotes.  <br/> permis de conduire  <br/> permis de conduire  <br/> permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> dlno #  <br/> vodičský PREUKAZ  <br/> |
   
## <a name="slovenia"></a>Slovénie

### <a name="format"></a>Format

Neuf chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

Neuf chiffres
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_slovenia_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_slovenia_eu_driver's_license_number` from est trouvé. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovenia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_slovenia_eu_driver's_license_number**|
|:-----|
|LD  <br/> Permis de conduire  <br/> Numéro de permis de conduire  <br/> permis de conduire  <br/> pilotes.  <br/> permis de conduire  <br/> permis de conduire  <br/> permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> dlno #  <br/> vozniško Dovoljenje  <br/> |
   
## <a name="spain"></a>Espagne

### <a name="format"></a>Format

Huit chiffres suivis d'un caractère
  
### <a name="pattern"></a>Modèle

Huit chiffres suivis d'un caractère:
  
-  Huit chiffres 
    
- Un chiffre ou une lettre (ne respectant pas la casse)
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_spain_eu_driver's_license_number` trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_spain_eu_driver's_license_number` from est trouvé. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_driver's_license_number" />
          <Match idRef="Keywords_spain_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_spain_eu_driver's_license_number**|
|:-----|
|dlno #  <br/> LD  <br/> pilotes.  <br/> permis de conduire  <br/> Permis de conduire  <br/> permis de conduire  <br/> permis de conduire  <br/> permis de conduire  <br/> permis de conduire  <br/> permis de conduire  <br/> permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> permis de conduire  <br/> Numéro de permis de conduire  <br/> permiso de Conducción  <br/> permiso Conducción  <br/> número licencia conducir  <br/> Número de carnet de conducir  <br/> conducir de carnet número  <br/> licencia conducir  <br/> Número de permiso de conducir  <br/> Número de permiso conducir  <br/> número permiso conducir  <br/> permiso conducir  <br/> licencia de manejo  <br/> carnet El de conducir  <br/> carnet conducir  <br/> |
   
## <a name="sweden"></a>Suède

### <a name="format"></a>Format

Dix chiffres contenant un trait d'Union
  
### <a name="pattern"></a>Modèle

Dix chiffres contenant un trait d'Union:
  
-  Six chiffres 
    
- Un trait d’union
    
- Quatre chiffres
    
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_sweden_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_sweden_eu_driver's_license_number` from est trouvé. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_driver's_license_number" />
          <Match idRef="Keywords_sweden_eu_driver's_license_number" />
        </Pattern>
</Entity> 
```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_sweden_eu_driver's_license_number**|
|:-----|
|LD  <br/> Permis de conduire  <br/> Numéro de permis de conduire  <br/> permis de conduire  <br/> pilotes.  <br/> permis de conduire  <br/> permis de conduire  <br/> permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> Numéro de permis de conduire  <br/> dlno #  <br/> körkort  <br/> |
   
## <a name="uk"></a>R.U.

Pour plus d'informations, reportez-vous à la section «Royaume-Uni Numéro de permis de conduire» dans [ce que recherche les types d'informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="see-also"></a>Voir aussi

[Éléments recherchés par les types d’informations sensibles](what-the-sensitive-information-types-look-for.md)

