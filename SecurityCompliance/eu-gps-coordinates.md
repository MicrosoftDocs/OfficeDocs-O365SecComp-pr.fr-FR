---
title: Coordonnées GPS de l’Union européenne
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/14/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: fdf2aebc-d5a4-4138-b10f-4a81dd70415a
description: Prévention des pertes de données (DLP) de sécurité Office 365 &amp; centre de conformité inclut de nombreux types d’informations sensibles qui sont prêts à utiliser dans vos stratégies DLP. Cette rubrique décrit le type d’informations sensibles des coordonnées GPS pour l’Union européenne.
ms.openlocfilehash: 89fb8420e479b9f793fc2be9aa3a9a9fd5741691
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528020"
---
# <a name="eu-gps-coordinates"></a>Coordonnées GPS de l’Union européenne

Prévention des pertes de données (DLP) de sécurité Office 365 &amp; centre de conformité inclut de nombreux types d’informations sensibles qui sont prêts à utiliser dans vos stratégies DLP. Cette rubrique décrit le type d’informations sensibles des coordonnées GPS pour l’Union européenne.
  
## <a name="austria"></a>Autriche

### <a name="format"></a>Format

Coordonnées pour villes en Autriche se trouvent dans la plage : Latitude à partir de 46.526 48.816 et longitude de 9.6 à 16.945.
  
### <a name="pattern"></a>Modèle

Pour chaque coordonnée, la combinaison de jusqu'à 6 chiffres et un séparateur décimal.
  
- 6 chiffres maximum
    
- Une virgule après la première ou deuxième chiffre.
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_austria_eu_gps_data_1` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_austria_eu_gps_data` est trouvée. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_austria_eu_gps_data_1` recherche de contenu qui correspond au modèle. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_austria_eu_gps_data_2` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_austria_eu_gps_data` est trouvée. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_austria_eu_gps_data_2` recherche de contenu qui correspond au modèle. 
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_gps_data_1" />
          <Match idRef="Keywords_austria_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_austria_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_gps_data_2" />
          <Match idRef="Keywords_austria_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_austria_eu_gps_data_2" />
        </Pattern>

```

### <a name="keywords"></a>Keywords

#### <a name="keywordsaustriaeugpsdata"></a>Keywords_austria_eu_gps_data

suivi du GPS
  
coordonnées GPS
  
emplacement
  
mapper
  
Latitude
  
longitude
  
Suivi de GPS
  
GPS-Koordinaten
  
Standort Karte
  
Breitengrad
  
Längengrad
  
## <a name="belgium"></a>Belgique

### <a name="pattern"></a>Modèle

-  chiffres 
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière recherche de contenu qui correspond au modèle.
    
- Un mot clé à partir d’est trouvé.
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75>">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_gps_data_1" />
          <Match idRef="Keywords_belgium_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_belgium_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_gps_data_2" />
          <Match idRef="Keywords_belgium_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_belgium_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="bulgaria"></a>Bulgarie

### <a name="pattern"></a>Modèle

-  chiffres 
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière recherche de contenu qui correspond au modèle.
    
- Un mot clé à partir d’est trouvé.
    
```
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75>
</Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_belgium_eu_gps_data_2" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_gps_data_1" />
          <Match idRef="Keywords_bulgaria_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_bulgaria_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_gps_data_2" />
          <Match idRef="Keywords_bulgaria_eu_gps_data" />
        </Pattern>
</Entity>
```

## <a name="croatia"></a>Croatie

### <a name="pattern"></a>Modèle

-  chiffres 
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière recherche de contenu qui correspond au modèle.
    
- Un mot clé à partir d’est trouvé.
    
```
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_gps_data_1" />
          <Match idRef="Keywords_croatia_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_croatia_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_gps_data_2" />
          <Match idRef="Keywords_croatia_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_croatia_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="cyprus"></a>Chypre

### <a name="pattern"></a>Modèle

-  chiffres 
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière recherche de contenu qui correspond au modèle.
    
- Un mot clé à partir d’est trouvé.
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_gps_data_1" />
          <Match idRef="Keywords_cyprus_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_cyprus_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_gps_data_2" />
          <Match idRef="Keywords_cyprus_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_cyprus_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="czech-republic"></a>République tchèque

### <a name="pattern"></a>Modèle

-  chiffres 
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
Une stratégie DLP est convaincu que ce type d’informations sensibles a été détecté % if, au sein d’une proximité de caractères :
  
- L’expression régulière recherche de contenu qui correspond au modèle.
    
- Un mot clé à partir d’est trouvé.
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_gps_data_1" />
          <Match idRef="Keywords_czech_republic_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_czech_republic_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_gps_data_2" />
          <Match idRef="Keywords_czech_republic_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_czech_republic_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="denmark"></a>Danemark

### <a name="pattern"></a>Modèle

-  chiffres 
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière recherche de contenu qui correspond au modèle.
    
- Un mot clé à partir d’est trouvé.
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_gps_data_1" />
          <Match idRef="Keywords_denmark_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_denmark_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_gps_data_2" />
          <Match idRef="Keywords_denmark_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_denmark_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="estonia"></a>Estonie

### <a name="pattern"></a>Modèle

-  chiffres 
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière recherche de contenu qui correspond au modèle.
    
- Un mot clé à partir d’est trouvé.
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_gps_data_1" />
          <Match idRef="Keywords_estonia_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_estonia_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_gps_data_2" />
          <Match idRef="Keywords_estonia_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_estonia_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="finland"></a>Finlande

### <a name="pattern"></a>Modèle

-  chiffres 
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière recherche de contenu qui correspond au modèle.
    
- Un mot clé à partir d’est trouvé.
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_gps_data_1" />
          <Match idRef="Keywords_finland_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_finland_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_gps_data_2" />
          <Match idRef="Keywords_finland_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_finland_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="france"></a>France

### <a name="pattern"></a>Modèle

-  chiffres 
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière recherche de contenu qui correspond au modèle.
    
- Un mot clé à partir d’est trouvé.
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
 <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_france_eu_gps_data_1" />
          <Match idRef="Keywords_france_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_france_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_france_eu_gps_data_2" />
          <Match idRef="Keywords_france_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_france_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="germany"></a>Allemagne

### <a name="pattern"></a>Modèle

-  chiffres 
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière recherche de contenu qui correspond au modèle.
    
- Un mot clé à partir d’est trouvé.
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_germany_eu_gps_data_1" />
          <Match idRef="Keywords_germany_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_germany_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_germany_eu_gps_data_2" />
          <Match idRef="Keywords_germany_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_germany_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="greece"></a>Grèce

### <a name="pattern"></a>Modèle

-  chiffres 
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière recherche de contenu qui correspond au modèle.
    
- Un mot clé à partir d’est trouvé.
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_gps_data_1" />
          <Match idRef="Keywords_greece_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_greece_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_gps_data_2" />
          <Match idRef="Keywords_greece_eu_gps_data" />
        </Pattern>
</Entity>
```

## <a name="hungary"></a>Hongrie

### <a name="pattern"></a>Modèle

-  chiffres 
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière recherche de contenu qui correspond au modèle.
    
- Un mot clé à partir d’est trouvé.
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_gps_data_1" />
          <Match idRef="Keywords_hungary_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_hungary_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_gps_data_2" />
          <Match idRef="Keywords_hungary_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_hungary_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="ireland"></a>Irlande

### <a name="pattern"></a>Modèle

-  chiffres 
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière recherche de contenu qui correspond au modèle.
    
- Un mot clé à partir d’est trouvé.
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_gps_data_1" />
          <Match idRef="Keywords_ireland_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_ireland_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_gps_data_2" />
          <Match idRef="Keywords_ireland_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_ireland_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="italy"></a>Italie

### <a name="pattern"></a>Modèle

-  chiffres 
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière recherche de contenu qui correspond au modèle.
    
- Un mot clé à partir d’est trouvé.
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_gps_data_1" />
          <Match idRef="Keywords_italy_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_italy_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_gps_data_2" />
          <Match idRef="Keywords_italy_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_italy_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="latvia"></a>Lettonie

### <a name="pattern"></a>Modèle

-  chiffres 
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière recherche de contenu qui correspond au modèle.
    
- Un mot clé à partir d’est trouvé.
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_gps_data_1" />
          <Match idRef="Keywords_latvia_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_latvia_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_gps_data_2" />
          <Match idRef="Keywords_latvia_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_latvia_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="lithuania"></a>Lituanie

### <a name="pattern"></a>Modèle

-  chiffres 
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière recherche de contenu qui correspond au modèle.
    
- Un mot clé à partir d’est trouvé.
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_gps_data_1" />
          <Match idRef="Keywords_lithuania_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_lithuania_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_gps_data_2" />
          <Match idRef="Keywords_lithuania_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_lithuania_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="luxemburg"></a>Luxembourg

### <a name="pattern"></a>Modèle

-  chiffres 
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière recherche de contenu qui correspond au modèle.
    
- Un mot clé à partir d’est trouvé.
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_gps_data_1" />
          <Match idRef="Keywords_luxemburg_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_luxemburg_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_gps_data_2" />
          <Match idRef="Keywords_luxemburg_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_luxemburg_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="malta"></a>Malte

### <a name="pattern"></a>Modèle

-  chiffres 
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière recherche de contenu qui correspond au modèle.
    
- Un mot clé à partir d’est trouvé.
    
```
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_gps_data_1" />
          <Match idRef="Keywords_malta_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_malta_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_gps_data_2" />
          <Match idRef="Keywords_malta_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_malta_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="netherlands"></a>Pays-Bas

### <a name="pattern"></a>Modèle

-  chiffres 
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière recherche de contenu qui correspond au modèle.
    
- Un mot clé à partir d’est trouvé.
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_gps_data_1" />
          <Match idRef="Keywords_netherlands_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_netherlands_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_gps_data_2" />
          <Match idRef="Keywords_netherlands_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_netherlands_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="poland"></a>Pologne

### <a name="pattern"></a>Modèle

-  chiffres 
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière recherche de contenu qui correspond au modèle.
    
- Un mot clé à partir d’est trouvé.
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_gps_data_1" />
          <Match idRef="Keywords_poland_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_poland_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_gps_data_2" />
          <Match idRef="Keywords_poland_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_poland_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="portugal"></a>Portugal

### <a name="pattern"></a>Modèle

-  chiffres 
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière recherche de contenu qui correspond au modèle.
    
- Un mot clé à partir d’est trouvé.
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_gps_data_1" />
          <Match idRef="Keywords_portugal_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_portugal_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_gps_data_2" />
          <Match idRef="Keywords_portugal_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_portugal_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="romania"></a>Roumanie

### <a name="pattern"></a>Modèle

-  chiffres 
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière recherche de contenu qui correspond au modèle.
    
- Un mot clé à partir d’est trouvé.
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_gps_data_1" />
          <Match idRef="Keywords_romania_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_romania_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_gps_data_2" />
          <Match idRef="Keywords_romania_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_romania_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="slovakia"></a>République de Slovaquie

### <a name="pattern"></a>Modèle

-  chiffres 
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière recherche de contenu qui correspond au modèle.
    
- Un mot clé à partir d’est trouvé.
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_gps_data_1" />
          <Match idRef="Keywords_slovakia_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_slovakia_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_gps_data_2" />
          <Match idRef="Keywords_slovakia_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_slovakia_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="slovenia"></a>Slovénie

### <a name="pattern"></a>Modèle

-  chiffres 
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière recherche de contenu qui correspond au modèle.
    
- Un mot clé à partir d’est trouvé.
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_gps_data_1" />
          <Match idRef="Keywords_slovenia_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_slovenia_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_gps_data_2" />
          <Match idRef="Keywords_slovenia_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_slovenia_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="spain"></a>Espagne

### <a name="pattern"></a>Modèle

-  chiffres 
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière recherche de contenu qui correspond au modèle.
    
- Un mot clé à partir d’est trouvé.
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_gps_data_1" />
          <Match idRef="Keywords_spain_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_spain_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_gps_data_2" />
          <Match idRef="Keywords_spain_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_spain_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="sweden"></a>Suède

### <a name="pattern"></a>Modèle

-  chiffres 
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière recherche de contenu qui correspond au modèle.
    
- Un mot clé à partir d’est trouvé.
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_gps_data_1" />
          <Match idRef="Keywords_sweden_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_sweden_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_gps_data_2" />
          <Match idRef="Keywords_sweden_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_sweden_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="uk"></a>ROYAUME-UNI

### <a name="pattern"></a>Modèle

-  chiffres 
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière recherche de contenu qui correspond au modèle.
    
- Un mot clé à partir d’est trouvé.
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_uk_eu_gps_data_1" />
          <Match idRef="Keywords_uk_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_uk_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_uk_eu_gps_data_2" />
          <Match idRef="Keywords_uk_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_uk_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="see-also"></a>Voir aussi

[Éléments recherchés par les types d’informations sensibles](what-the-sensitive-information-types-look-for.md)

