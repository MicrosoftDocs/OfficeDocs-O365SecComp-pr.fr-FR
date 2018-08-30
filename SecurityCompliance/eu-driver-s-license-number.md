---
title: Numéro de permis de conduire l’Union européenne
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: c3923cd3-ec84-435f-bf41-cadc37996a4b
description: Cette rubrique illustre une stratégie de protection contre la perte données lorsqu’il détecte type d’informations sensibles de l’UE permis de conduire numéro de licence. Ce type d’informations sensibles définit différents motifs, mots clés et autres pour chaque pays.
ms.openlocfilehash: 065684249f9766d567c63e6b8170d36f56692e45
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528065"
---
# <a name="eu-drivers-license-number"></a>Numéro de permis de conduire l’Union européenne

Cette rubrique illustre une stratégie de protection contre la perte données lorsqu’il détecte type d’informations sensibles de l’UE permis de conduire numéro de licence. Ce type d’informations sensibles définit différents motifs, mots clés et autres pour chaque pays.
  
## <a name="austria"></a>Autriche

### <a name="format"></a>Format

Huit chiffres sans espaces et les séparateurs
  
### <a name="pattern"></a>Modèle

Huit chiffres
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_austria_eu_driver's_license_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_austria_eu_driver's_license_number` est trouvée. 
    
```
<!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_driver's_license_number" />
          <Match idRef="Keywords_austria_eu_driver's_license_number" />
        </Pattern>
    </Entity>

```

### <a name="keywords"></a>Keywords

| |
|**Keywords_austria_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> numéro de permis conduire  <br/> licence pilote  <br/> lic pilotes.  <br/> drivers license  <br/> conduire permis de  <br/> driver’s license  <br/> numéro de permis de conduire  <br/> numéro de permis de conduire licence  <br/>  numéro de permis de conduire  <br/> dlno #  <br/> fuhrerschein  <br/> fuhrerschein Slovaquie osterreich  <br/> |
   
## <a name="belgium"></a>Belgique

### <a name="format"></a>Format

10 chiffres sans espaces et les séparateurs
  
### <a name="pattern"></a>Modèle

10 chiffres
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_belgium_eu_driver's_license_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_belgium_eu_driver's_license_number` est trouvée. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_driver's_license_number" />
          <Match idRef="Keywords_belgium_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a>Keywords

| |
|**Keywords__belgium_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> numéro de permis conduire  <br/> licence pilote  <br/> lic pilotes.  <br/> drivers license  <br/> permis de conduire  <br/> driver’s license  <br/> numéro de permis de conduire  <br/> numéro de permis de conduire licence  <br/> dlno #  <br/> rijbewijs  <br/> rijbewijsnummer  <br/> führerscheinnummer  <br/> fuhrerscheinnummer  <br/> fuehrerscheinnummer  <br/> führerschein-nr  <br/> fuehrerschein-Nr  <br/> fuehrerschein-nr  <br/> |
   
## <a name="bulgaria"></a>Bulgarie

### <a name="format"></a>Format

Neuf chiffres sans espaces et les séparateurs
  
### <a name="pattern"></a>Modèle

Neuf chiffres
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_bulgaria_eu_driver's_license_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_bulgaria_eu_driver's_license_number` est trouvée. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
             <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_driver's_license_number" />
          <Match idRef="Keywords_bulgaria_eu_driver's_license_number" />
        </Pattern> 
</Entity>    

```

### <a name="keywords"></a>Keywords

| |
|**Keywords_bulgaria_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> numéro de permis conduire  <br/> licence pilote  <br/> lic pilotes.  <br/> drivers license  <br/> permis de conduire  <br/> driver’s license  <br/> numéro de permis de conduire  <br/> numéro de permis de conduire licence  <br/> numéro de permis de conduire  <br/> dlno #  <br/> СВИДЕТЕЛСТВО ЗА УПРАВЛЕНИЕ НА МПС  <br/> СВИДЕТЕЛСТВО ЗА УПРАВЛЕНИЕ НА МОТОРНО ПРЕВОЗНО СРЕДСТВО  <br/> СУМПС  <br/> ШОФЬОРСКА КНИЖКА  <br/> |
   
## <a name="croatia"></a>Croatie

### <a name="format"></a>Format

Huit chiffres sans espaces et les séparateurs
  
### <a name="pattern"></a>Modèle

Huit chiffres
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_croatia_eu_driver's_license_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_croatia_eu_driver's_license_number` est trouvée. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_driver's_license_number" />
          <Match idRef="Keywords_croatia_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a>Keywords

| |
|**Keywords_croatia_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> numéro de permis conduire  <br/> licence pilote  <br/> lic pilotes.  <br/> drivers license  <br/> permis de conduire  <br/> driver’s license  <br/> numéro de permis de conduire  <br/> numéro de permis de conduire licence  <br/> numéro de permis de conduire  <br/> dlno #  <br/> vozačka dozvola  <br/> |
   
## <a name="cyprus"></a>Chypre

### <a name="format"></a>Format

12 chiffres sans espaces et les séparateurs
  
### <a name="pattern"></a>Modèle

12 chiffres
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_cyprus_eu_driver's_license_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_cyprus_eu_driver's_license_number` est trouvée. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_driver's_license_number" />
          <Match idRef="Keywords_cyprus_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_cyprus_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> numéro de permis conduire  <br/> licence pilote  <br/> lic pilotes.  <br/> drivers license  <br/> permis de conduire  <br/> numéro de permis de conduire  <br/> numéro de permis de conduire licence  <br/> numéro de permis de conduire  <br/> dlno #  <br/> ΆΔΕΙΑ ΟΔΉΓΗΣΗΣ  <br/> |
   
## <a name="czech-republic"></a>République tchèque

### <a name="format"></a>Format

Deux lettres suivies de six chiffres
  
### <a name="pattern"></a>Modèle

Huit lettres et chiffres :
  
- Deux lettres (pas la casse)
    
- Un espace (facultatif) 
    
- Six chiffres
    
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_czech_republic_eu_driver's_license_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_czech_republic_eu_driver's_license_number` est trouvée. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_driver's_license_number" />
          <Match idRef="Keywords_czech_republic_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a>Keywords

| |
|**Keywords_czech_republic_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> numéro de permis conduire  <br/> licence pilote  <br/> lic pilotes.  <br/> drivers license  <br/> permis de conduire  <br/> driver’s license  <br/> numéro de permis de conduire  <br/> numéro de permis de conduire  <br/> numéro de permis de conduire licence  <br/> numéro de permis de conduire  <br/> dlno #  <br/> Řidičský prúkaz  <br/> |
   
## <a name="denmark"></a>Danemark

### <a name="format"></a>Format

Huit chiffres sans espaces et les séparateurs
  
### <a name="pattern"></a>Modèle

Huit chiffres
  
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_denmark_eu_driver's_license_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_denmark_eu_driver's_license_number` est trouvée. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_driver's_license_number" />
          <Match idRef="Keywords_denmark_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a>Keywords

| |
|**Keywords_denmark_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> numéro de permis conduire  <br/> licence pilote  <br/> lic pilotes.  <br/> drivers license  <br/> permis de conduire  <br/> driver’s license  <br/> numéro de permis de conduire  <br/> numéro de permis de conduire licence  <br/> numéro de permis de conduire  <br/> dlno #  <br/> kørekort  <br/> kørekortnummer  <br/> |
   
## <a name="estonia"></a>Estonie

### <a name="format"></a>Format

Deux lettres suivies de six chiffres
  
### <a name="pattern"></a>Modèle

Deux lettres et six chiffres :
  
-  Les lettres « ET « (pas la casse) 
    
- Six chiffres
    
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_estonia_eu_driver's_license_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_estonia_eu_driver's_license_number` est trouvée. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_driver's_license_number" />
          <Match idRef="Keywords_estonia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_estonia_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> numéro de permis conduire  <br/> numéro de permis conduire  <br/> licence pilote  <br/> lic pilotes.  <br/> drivers license  <br/> permis de conduire  <br/> driver’s license  <br/> numéro de permis de conduire  <br/> numéro de permis de conduire  <br/> dlno #  <br/> 
permis de conduire  <br/> |
   
## <a name="finland"></a>Finlande

### <a name="format"></a>Format

10 chiffres contenant un trait d’union
  
### <a name="pattern"></a>Modèle

10 chiffres contenant un trait d’union :
  
-  Six chiffres 
    
- Un trait d’union
    
-  Quatre chiffres 
    
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_finland_eu_driver's_license_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_finland_eu_driver's_license_number` est trouvée. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_driver's_license_number" />
          <Match idRef="Keywords_finland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_finland_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> numéro de permis conduire  <br/> licence pilote  <br/> lic pilotes.  <br/> drivers license  <br/> permis de conduire  <br/> driver’s license  <br/> numéro de permis de conduire  <br/> numéro de permis de conduire licence  <br/> numéro de permis de conduire  <br/> dlno #  <br/> ajokortti  <br/> |
   
## <a name="france"></a>France

Pour plus d’informations, voir la section « Numéro de permis de conduire France » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="germany"></a>Allemagne

Pour plus d’informations, voir la section « Numéro de permis de conduire Allemagne » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="greece"></a>Grèce

### <a name="format"></a>Format

Neuf chiffres sans espaces et les séparateurs
  
### <a name="pattern"></a>Modèle

 Neuf chiffres 
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_greece_eu_driver's_license_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_greece_eu_driver's_license_number` est trouvée. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_driver's_license_number" />
          <Match idRef="Keywords_greece_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_greece_eu_driver's_license_number**|
|:-----|
|dlL #  <br/> driver license  <br/> numéro de permis conduire  <br/> licence pilote  <br/> lic pilotes.  <br/> drivers license  <br/> permis de conduire  <br/> driver’s license  <br/> numéro de permis de conduire  <br/> numéro de permis de conduire licence  <br/> numéro de permis de conduire  <br/> dlno #  <br/> ΔΕΙΑ ΟΔΉΓΗΣΗΣ  <br/> Adeia odigisis  <br/> |
   
## <a name="hungary"></a>Hongrie

### <a name="format"></a>Format

Deux lettres suivies de six chiffres
  
### <a name="pattern"></a>Modèle

Deux lettres et six chiffres :
  
-  Deux lettres (pas la casse) 
    
- Six chiffres
    
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_hungary_eu_driver's_license_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_hungary_eu_driver's_license_number` est trouvée. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_driver's_license_number" />
          <Match idRef="Keywords_hungary_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_hungary_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> numéro de permis conduire  <br/> licence pilote  <br/> lic pilotes.  <br/> drivers license  <br/> permis de conduire  <br/> driver’s license  <br/> numéro de permis de conduire  <br/> numéro de permis de conduire licence  <br/> numéro de permis de conduire  <br/> dlno #  <br/> vezetoi engedely  <br/> |
   
## <a name="ireland"></a>Irlande

### <a name="format"></a>Format

Six chiffres suivies de quatre lettres
  
### <a name="pattern"></a>Modèle

Six chiffres et quatre lettres :
  
- Six chiffres
    
- Quatre lettres (pas la casse)
    
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_ireland_eu_driver's_license_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_ireland_eu_driver's_license_number` est trouvée. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_driver's_license_number" />
          <Match idRef="Keywords_ireland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_ireland_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> numéro de permis conduire  <br/> licence pilote  <br/> lic pilotes.  <br/> drivers license  <br/> permis de conduire  <br/> driver’s license  <br/> numéro de permis de conduire  <br/> numéro de permis de conduire licence  <br/> numéro de permis de conduire  <br/> dlno #  <br/> ceadúnas tiomána  <br/> |
   
## <a name="italy"></a>Italie

Pour plus d’informations, voir la section « Numéro de permis de conduire Italie » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="latvia"></a>Lettonie

### <a name="format"></a>Format

Trois lettres suivies de six chiffres
  
### <a name="pattern"></a>Modèle

Trois lettres et six chiffres :
  
-  Trois lettres (pas la casse) 
    
- Six chiffres
    
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_latvia_eu_driver's_license_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_latvia_eu_driver's_license_number` est trouvée. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_driver's_license_number" />
          <Match idRef="Keywords_latvia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_latvia_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> numéro de permis conduire  <br/> licence pilote  <br/> lic pilotes.  <br/> drivers license  <br/> permis de conduire  <br/> driver’s license  <br/> numéro de permis de conduire  <br/> numéro de permis de conduire licence  <br/> numéro de permis de conduire  <br/> dlno #  <br/> autovadītāja apliecība  <br/> |
   
## <a name="lithuania"></a>Lituanie

### <a name="format"></a>Format

Huit chiffres sans espaces et les séparateurs
  
### <a name="pattern"></a>Modèle

 Huit chiffres 
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_lithuania_eu_driver's_license_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_lithuania_eu_driver's_license_number` est trouvée. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_driver's_license_number" />
          <Match idRef="Keywords_lithuania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_lithuania_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> numéro de permis conduire  <br/> licence pilote  <br/> lic pilotes.  <br/> drivers license  <br/> permis de conduire  <br/> driver’s license  <br/> numéro de permis de conduire  <br/> numéro de permis de conduire licence  <br/> numéro de permis de conduire  <br/> dlno #  <br/> vairuotojo pažymėjimas  <br/> |
   
## <a name="luxemburg"></a>Luxembourg

### <a name="format"></a>Format

Six chiffres sans espaces et les séparateurs
  
### <a name="pattern"></a>Modèle

 Six chiffres 
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_luxemburg_eu_driver's_license_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_luxemburg_eu_driver's_license_number` est trouvée. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_driver's_license_number" />
          <Match idRef="Keywords_luxemburg_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_luxemburg_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> numéro de permis conduire  <br/> licence pilote  <br/> lic pilotes.  <br/> drivers license  <br/> permis de conduire  <br/> driver’s license  <br/> numéro de permis de conduire  <br/> numéro de permis de conduire licence  <br/> numéro de permis de conduire  <br/> dlno #  <br/> fahrerlaubnis  <br/> |
   
## <a name="malta"></a>Malte

### <a name="format"></a>Format

Combinaison de deux caractères et six chiffres dans le modèle spécifié
  
### <a name="pattern"></a>Modèle

Combinaison de deux caractères et six chiffres :
  
- Deux caractères (chiffres ou lettres, qui ne respecte pas la casse)
    
- Un espace (facultatif) 
    
- Trois chiffres
    
- Un espace (facultatif) 
    
- Trois chiffres
    
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_malta_eu_driver's_license_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_malta_eu_driver's_license_number` est trouvée. 
    
```
<!-- EU Driver's License Number -->
 <Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_driver's_license_number" />
          <Match idRef="Keywords_malta_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_malta_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> numéro de permis conduire  <br/> licence pilote  <br/> lic pilotes.  <br/> drivers license  <br/> permis de conduire  <br/> driver’s license  <br/> numéro de permis de conduire  <br/> numéro de permis de conduire licence  <br/> numéro de permis de conduire  <br/> dlno #  <br/> tâches liċenzja-sewqan  <br/> |
   
## <a name="netherlands"></a>Pays-Bas

### <a name="format"></a>Format

10 chiffres sans espaces et les séparateurs
  
### <a name="pattern"></a>Modèle

10 chiffres
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_netherlands_eu_driver's_license_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_netherlands_eu_driver's_license_number` est trouvée. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_driver's_license_number" />
          <Match idRef="Keywords_netherlands_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_netherlands_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> numéro de permis conduire  <br/> licence pilote  <br/> lic pilotes.  <br/> drivers license  <br/> permis de conduire  <br/> driver’s license  <br/> numéro de permis de conduire  <br/> numéro de permis de conduire licence  <br/> numéro de permis de conduire  <br/> dlno #  <br/> 
permis de conduire  <br/> rijbewijs  <br/> rijbewijsnummer  <br/> |
   
## <a name="poland"></a>Pologne

### <a name="format"></a>Format

14 chiffres contenant des barres 2 obliques
  
### <a name="pattern"></a>Modèle

14 chiffres et des barres 2 obliques :
  
-  Cinq chiffres 
    
- Une barre oblique 
    
- Deux chiffres
    
- Une barre oblique 
    
- Sept chiffres
    
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_poland_eu_driver's_license_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_poland_eu_driver's_license_number` est trouvée. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_driver's_license_number" />
          <Match idRef="Keywords_poland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_poland_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> numéro de permis conduire  <br/> licence pilote  <br/> lic pilotes.  <br/> drivers license  <br/> permis de conduire  <br/> driver’s license  <br/> numéro de permis de conduire  <br/> numéro de permis de conduire licence  <br/> numéro de permis de conduire  <br/> dlno #  <br/> uzyskać jazdy  <br/> |
   
## <a name="portugal"></a>Portugal

### <a name="format"></a>Format

Deux lettres suivies un sept chiffres dans le modèle spécifié
  
### <a name="pattern"></a>Modèle

Deux lettres suivies de sept chiffres avec des caractères spéciaux :
  
-  Deux lettres (pas la casse) 
    
- Un trait d’union 
    
- Six chiffres
    
- Un espace
    
- Un chiffre
    
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_portugal_eu_driver's_license_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_portugal_eu_driver's_license_number` est trouvée. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_driver's_license_number" />
          <Match idRef="Keywords_portugal_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_portugal_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> numéro de permis conduire  <br/> licence pilote  <br/> lic pilotes.  <br/> drivers license  <br/> permis de conduire  <br/> driver’s license  <br/> numéro de permis de conduire  <br/> numéro de permis de conduire licence  <br/> numéro de permis de conduire  <br/> dlno #  <br/> carteira de motorista  <br/> |
   
## <a name="romania"></a>Roumanie

### <a name="format"></a>Format

Un caractère suivi de huit chiffres
  
### <a name="pattern"></a>Modèle

Un caractère suivi de huit chiffres :
  
-  Une lettre (pas la casse) ou un chiffre 
    
- Huit chiffres
    
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_romania_eu_driver's_license_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_romania_eu_driver's_license_number` est trouvée. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_driver's_license_number" />
          <Match idRef="Keywords_romania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_romania_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> numéro de permis conduire  <br/> licence pilote  <br/> lic pilotes.  <br/> drivers license  <br/> permis de conduire  <br/> driver’s license  <br/> numéro de permis de conduire  <br/> numéro de permis de conduire licence  <br/> numéro de permis de conduire  <br/> dlno #  <br/> permis de conducere  <br/> |
   
## <a name="slovakia"></a>République de Slovaquie

### <a name="format"></a>Format

Un caractère suivi de sept chiffres
  
### <a name="pattern"></a>Modèle

Un caractère suivi de sept chiffres
  
- Une lettre (pas la casse) ou un chiffre
    
-  Sept chiffres 
    
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_slovakia_eu_driver's_license_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_slovakia_eu_driver's_license_number` est trouvée. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovaknia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovakia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_slovakia_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> numéro de permis conduire  <br/> licence pilote  <br/> lic pilotes.  <br/> drivers license  <br/> permis de conduire  <br/> driver’s license  <br/> numéro de permis de conduire  <br/> numéro de permis de conduire licence  <br/> numéro de permis de conduire  <br/> dlno #  <br/> vodičský preukaz  <br/> |
   
## <a name="slovenia"></a>Slovénie

### <a name="format"></a>Format

Neuf chiffres sans espaces et les séparateurs
  
### <a name="pattern"></a>Modèle

Neuf chiffres
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_slovenia_eu_driver's_license_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_slovenia_eu_driver's_license_number` est trouvée. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovenia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_slovenia_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> numéro de permis conduire  <br/> licence pilote  <br/> lic pilotes.  <br/> drivers license  <br/> permis de conduire  <br/> driver’s license  <br/> numéro de permis de conduire  <br/> numéro de permis de conduire licence  <br/> numéro de permis de conduire  <br/> dlno #  <br/> vozniško dovoljenje  <br/> |
   
## <a name="spain"></a>Espagne

### <a name="format"></a>Format

Huit chiffres suivies d’un caractère
  
### <a name="pattern"></a>Modèle

Huit chiffres suivies d’un caractère :
  
-  Huit chiffres 
    
- Un chiffre ou une lettre (pas la casse)
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_spain_eu_driver's_license_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_spain_eu_driver's_license_number` est trouvée. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_driver's_license_number" />
          <Match idRef="Keywords_spain_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_spain_eu_driver's_license_number**|
|:-----|
|dlno #  <br/> dl#  <br/> lic pilotes.  <br/> licence pilote  <br/> driver license  <br/> permis de conduire  <br/> drivers license  <br/> conduire permis de  <br/> driver’s license  <br/> permis de conduire
  <br/> permis de conduire  <br/> numéro de licence pilote  <br/> numéro de permis conduire  <br/> nombre de pilotes de licence  <br/> numéro de permis de conduire  <br/> numéro de permis de conduire licence  <br/> numéro de permis de conduire  <br/> numéro de permis de conduire  <br/> numéro de permis de conduire  <br/> permis de conduire  <br/> numéro de permis de conduire  <br/> permiso de conducción  <br/> permiso conducción  <br/> Número licencia conducir  <br/> Número de carnet de conducir  <br/> Número carnet conducir  <br/> licencia conducir  <br/> Número de permiso de conducir  <br/> Número de permiso conducir  <br/> Número permiso conducir  <br/> permiso conducir  <br/> licencia de manejo  <br/> EL carnet de conducir  <br/> Carnet conducir  <br/> |
   
## <a name="sweden"></a>Suède

### <a name="format"></a>Format

Dix chiffres contenant un trait d’union
  
### <a name="pattern"></a>Modèle

Dix chiffres contenant un trait d’union :
  
-  Six chiffres 
    
- Un trait d’union
    
- Quatre chiffres
    
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_sweden_eu_driver's_license_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_sweden_eu_driver's_license_number` est trouvée. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_driver's_license_number" />
          <Match idRef="Keywords_sweden_eu_driver's_license_number" />
        </Pattern>
</Entity> 
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_sweden_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> numéro de permis conduire  <br/> licence pilote  <br/> lic pilotes.  <br/> drivers license  <br/> permis de conduire  <br/> driver’s license  <br/> numéro de permis de conduire  <br/> numéro de permis de conduire licence  <br/> numéro de permis de conduire  <br/> dlno #  <br/> körkort  <br/> |
   
## <a name="uk"></a>ROYAUME-UNI

Pour plus d’informations, voir la section « Numéro de permis de conduire britannique » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="see-also"></a>Voir aussi

[Éléments recherchés par les types d’informations sensibles](what-the-sensitive-information-types-look-for.md)

