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
# <a name="eu-passport-number"></a>Numéro de passeport UE

Cette rubrique illustre une stratégie de protection contre la perte données lorsqu’il détecte le type d’informations sensibles numéro de passeport l’Union européenne. Ce type d’informations sensibles définit différents motifs, mots clés et autres pour chaque pays.
  
## <a name="austria"></a>Autriche

### <a name="format"></a>Format

Une lettre suivie d’un espace facultatif et sept chiffres
  
### <a name="pattern"></a>Modèle

Une combinaison d’une lettre, sept chiffres et un espace :
  
- Une lettre (ne respecte pas la casse)
    
- Un espace (facultatif)
    
- Sept chiffres
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_austria_eu_passport_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_austria_eu_passport_number` est trouvée. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_passport_number" />
          <Match idRef="Keywords_austria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_austria_eu_passport_number**|
|:-----|
|numéro de passeport  <br/> numéro de passeport autrichien  <br/> passeport aucune  <br/> reisepass  <br/> österreichisch reisepass  <br/> |
   
## <a name="belgium"></a>Belgique

### <a name="format"></a>Format

Deux lettres suivies de six chiffres sans espaces ni les délimiteurs
  
### <a name="pattern"></a>Modèle

Deux lettres et suivi de six chiffres
  
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_belgium_eu_passport_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_belgium_eu_passport_number` est trouvée. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium__eu_passport_number" />
          <Match idRef="Keywords_belgium_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_belgium_eu_passport_number**|
|:-----|
|numéro de passeport  <br/> numéro de passeport belge  <br/> passeport aucune  <br/> paspoort  <br/> paspoortnummer  <br/> reisepass kein  <br/> reisepass  <br/> |
   
## <a name="bulgaria"></a>Bulgarie

### <a name="format"></a>Format

Neuf chiffres sans espaces et les séparateurs
  
### <a name="pattern"></a>Modèle

 Neuf chiffres 
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_bulgaria_eu_passport_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_bulgaria_eu_passport_number` est trouvée. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_passport_number" />
          <Match idRef="Keywords_bulgaria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_bulgaria_eu_passport_number**|
|:-----|
|numéro de passeport  <br/> numéro de passeport bulgare  <br/> passeport aucune  <br/> НОМЕР НА ПАСПОРТА  <br/> |
   
## <a name="croatia"></a>Croatie

### <a name="format"></a>Format

Neuf chiffres sans espaces et les séparateurs
  
### <a name="pattern"></a>Modèle

 Neuf chiffres 
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_croatia_eu_passport_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_croatia_eu_passport_number` est trouvée. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_passport_number" />
          <Match idRef="Keywords_croatia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_croatia_eu_passport_number**|
|:-----|
|numéro de passeport  <br/> numéro de passeport croate  <br/> passeport aucune  <br/> broj putovnice  <br/> |
   
## <a name="cyprus"></a>Chypre

### <a name="format"></a>Format

Une lettre de suivi de 6 à 8 chiffres sans espaces ni les délimiteurs
  
### <a name="pattern"></a>Modèle

Une lettre de suivi de 6 à 8 chiffres
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_cyprus_eu_passport_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_cyprus_eu_passport_number` est trouvée. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_passport_number" />
          <Match idRef="Keywords_cyprus_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_cyprus_eu_passport_number**|
|:-----|
|numéro de passeport  <br/> numéro de passeport Chypre  <br/> passeport aucune  <br/> ΑΡΙΘΜΌ ΔΙΑΒΑΤΗΡΊΟΥ  <br/> |
   
## <a name="czech-republic"></a>République tchèque

### <a name="format"></a>Format

Huit chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

Huit chiffres sans espaces ni délimiteurs
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_czech_republic_eu_passport_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_czech_republic_eu_passport_number` est trouvée. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_passport_number" />
          <Match idRef="Keywords_czech_republic_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_czech_republic_eu_passport_number**|
|:-----|
|numéro de passeport  <br/> numéro de passeport tchèque  <br/> passeport aucune  <br/> pas de cestovní  <br/> pas  <br/> |
   
## <a name="denmark"></a>Danemark

### <a name="format"></a>Format

Neuf chiffres sans espaces et les séparateurs
  
### <a name="pattern"></a>Modèle

 Neuf chiffres 
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_denmark_eu_passport_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_denmark_eu_passport_number` est trouvée. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_passport_number" />
          <Match idRef="Keywords_denmark_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_denmark_eu_passport_number**|
|:-----|
|numéro de passeport  <br/> numéro de passeport danois  <br/> passeport aucune  <br/> pas  <br/> pasnummer  <br/> |
   
## <a name="estonia"></a>Estonie

### <a name="format"></a>Format

Une lettre de suivi de sept chiffres sans espaces ni les délimiteurs
  
### <a name="pattern"></a>Modèle

Une lettre de suivi de sept chiffres
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_estonia_eu_passport_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_estonia_eu_passport_number` est trouvée. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_passport_number" />
          <Match idRef="Keywords_estonia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_estonia_eu_passport_number**|
|:-----|
|numéro de passeport  <br/> numéro de passeport estonien  <br/> passeport aucune  <br/> eesti kodaniku passe  <br/> |
   
## <a name="finland"></a>Finlande

Pour plus d’informations, consultez la section « Numéro de passeport Finlande » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="france"></a>France

Pour plus d’informations, voir la section « Numéro de passeport France » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="germany"></a>Allemagne

Pour plus d’informations, voir la section « Numéro de passeport Allemagne » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="greece"></a>Grèce

### <a name="format"></a>Format

Deux lettres suivies à sept chiffres sans espaces ni les délimiteurs
  
### <a name="pattern"></a>Modèle

Deux lettres suivies de sept chiffres
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_greece_eu_passport_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_greece_eu_passport_number` est trouvée. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_passport_number" />
          <Match idRef="Keywords_greece_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_greece_eu_passport_number**|
|:-----|
|numéro de passeport  <br/> numéro de passeport grec  <br/> passeport aucune  <br/> ΔΙΑΒΑΤΗΡΙΟ  <br/> |
   
## <a name="hungary"></a>Hongrie

### <a name="format"></a>Format

Deux lettres suivies de six ou sept chiffres sans espaces ni les délimiteurs
  
### <a name="pattern"></a>Modèle

Deux lettres suivies de six ou sept chiffres
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_hungary_eu_passport_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_hungary_eu_passport_number` est trouvée. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_passport_number" />
          <Match idRef="Keywords_hungary_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_hungary_eu_passport_number**|
|:-----|
|numéro de passeport  <br/> numéro de passeport hongrois  <br/> passeport aucune  <br/> útlevél száma  <br/> |
   
## <a name="ireland"></a>Irlande

### <a name="format"></a>Format

Deux lettres ou des chiffres suivis sept chiffres sans espaces ni les délimiteurs
  
### <a name="pattern"></a>Modèle

Deux lettres ou des chiffres suivis à sept chiffres :
  
- Deux chiffres ou lettres (ne respectent pas la casse)
    
- Sept chiffres
    
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_ireland_eu_passport_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_ireland_eu_passport_number` est trouvée. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_passport_number" />
          <Match idRef="Keywords_ireland_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_ireland_eu_passport_number**|
|:-----|
|numéro de passeport  <br/> numéro de passeport irlandais  <br/> passeport aucune  <br/> pas  <br/> passeport  <br/> passeport  <br/> numero de passeport  <br/> |
   
## <a name="italy"></a>Italie

### <a name="format"></a>Format

Deux lettres ou des chiffres suivis sept chiffres sans espaces ni les délimiteurs
  
### <a name="pattern"></a>Modèle

Deux lettres ou des chiffres suivis à sept chiffres :
  
- Deux chiffres ou lettres (ne respectent pas la casse)
    
- Sept chiffres
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_italy_eu_passport_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_italy_eu_passport_number` est trouvée. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_passport_number" />
          <Match idRef="Keywords_italy_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_italy_eu_passport_number**|
|:-----|
|numéro de passeport italien  <br/> Repubblica italiana passaporto  <br/> passaporto  <br/> passaporto italiana  <br/> numéro de passeport  <br/> Italiana passaporto numero  <br/> numero passaporto  <br/> numéro passeport italien  <br/> passeport numéro  <br/> |
   
## <a name="latvia"></a>Lettonie

### <a name="format"></a>Format

Deux lettres ou des chiffres suivis sept chiffres sans espaces ni les délimiteurs
  
### <a name="pattern"></a>Modèle

Deux lettres ou des chiffres suivis à sept chiffres :
  
- Deux chiffres ou lettres (ne respectent pas la casse)
    
- Sept chiffres
    
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_latvia_eu_passport_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_latvia_eu_passport_number` est trouvée. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_passport_number" />
          <Match idRef="Keywords_latvia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_latvia_eu_passport_number**|
|:-----|
|numéro de passeport  <br/> numéro de passeport letton  <br/> passeport aucune  <br/> pase numurs  <br/> |
   
## <a name="lithuania"></a>Lituanie

### <a name="format"></a>Format

Huit des chiffres ou des lettres sans espaces ni les délimiteurs
  
### <a name="pattern"></a>Modèle

Huit des chiffres ou des lettres (non sensible à la casse)
  
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_lithuania_eu_passport_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_lithuania_eu_passport_number` est trouvée. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_passport_number" />
          <Match idRef="Keywords_lithuania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_lithuania_eu_passport_number**|
|:-----|
|numéro de passeport  <br/> numéro de passeport lithunian  <br/> passeport aucune  <br/> Paso numeris  <br/> |
   
## <a name="luxemburg"></a>Luxembourg

### <a name="format"></a>Format

Huit des chiffres ou des lettres sans espaces ni les délimiteurs
  
### <a name="pattern"></a>Modèle

Huit des chiffres ou des lettres (non sensible à la casse)
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_nation_eu_passport_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_nation_eu_passport_number` est trouvée. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_nation_eu_passport_number" />
          <Match idRef="Keywords_nation_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_nation_eu_passport_number**|
|:-----|
|numéro de passeport  <br/> numéro de passeport letton  <br/> passeport aucune  <br/> passnummer  <br/> |
   
## <a name="malta"></a>Malte

### <a name="format"></a>Format

Sept chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

 Sept chiffres 
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_malta_eu_passport_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_malta_eu_passport_number` est trouvée. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_passport_number" />
          <Match idRef="Keywords_malta_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_malta_eu_passport_number**|
|:-----|
|numéro de passeport  <br/> numéro de passeport maltais  <br/> passeport aucune  <br/> numérique un numru-passaport  <br/> |
   
## <a name="netherlands"></a>Pays-Bas

### <a name="format"></a>Format

Neuf des lettres ou des chiffres sans espaces ni les délimiteurs
  
### <a name="pattern"></a>Modèle

Neuf des lettres ou des chiffres
  
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_netherlands_eu_passport_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_netherlands_eu_passport_number` est trouvée. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_passport_number" />
          <Match idRef="Keywords_netherlands_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_netherlands_eu_passport_number**|
|:-----|
|numéro de passeport néerlandais  <br/> numéro de passeport  <br/> numéro de passeport pays-bas  <br/> nederlanden paspoort nummer  <br/> paspoort  <br/> nederlanden paspoortnummer  <br/> paspoortnummer  <br/> |
   
## <a name="poland"></a>Pologne

Pour plus d’informations, voir la section « Numéro de passeport Pologne » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="portugal"></a>Portugal

### <a name="format"></a>Format

Une lettre de suivi de six chiffres sans espaces ni les délimiteurs
  
### <a name="pattern"></a>Modèle

Une lettre de suivi de six chiffres :
  
- Une lettre (ne respecte pas la casse)
    
- Six chiffres
    
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_portugal_eu_passport_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_portugal_eu_passport_number` est trouvée. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_passport_number" />
          <Match idRef="Keywords_portugal_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_portugal_eu_passport_number**|
|:-----|
|numéro de passeport  <br/> numéro de passeport portugais  <br/> passeport aucune  <br/> Número passaporte  <br/> |
   
## <a name="romania"></a>Roumanie

### <a name="format"></a>Format

Huit ou neuf chiffres sans espaces et les séparateurs
  
### <a name="pattern"></a>Modèle

Huit ou neuf chiffres
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_romania_eu_passport_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_romania_eu_passport_number` est trouvée. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_passport_number" />
          <Match idRef="Keywords_romania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_romania_eu_passport_number**|
|:-----|
|numéro de passeport  <br/> numéro de passeport roumain  <br/> passeport aucune  <br/> numărul pașaportului  <br/> |
   
## <a name="slovakia"></a>République de Slovaquie

### <a name="format"></a>Format

Un chiffre ou une lettre suivi par sept chiffres sans espaces ni les délimiteurs
  
### <a name="pattern"></a>Modèle

Un chiffre ou une lettre (pas sensible à la casse) suivi de sept chiffres
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_slovakia_eu_passport_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_slovakia_eu_passport_number` est trouvée. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_passport_number" />
          <Match idRef="Keywords_slovakia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_slovakia_eu_passport_number**|
|:-----|
|numéro de passeport  <br/> numéro de passeport slovaque  <br/> passeport aucune  <br/> Číslo pasu  <br/> |
   
## <a name="slovenia"></a>Slovénie

### <a name="format"></a>Format

Deux lettres suivies à sept chiffres sans espaces ni les délimiteurs
  
### <a name="pattern"></a>Modèle

Deux lettres suivies à sept chiffres :
  
- La lettre « P »
    
- Une lettre majuscule
    
- Sept chiffres
    
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_slovenia_eu_passport_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_slovenia_eu_passport_number` est trouvée. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_passport_number" />
          <Match idRef="Keywords_slovenia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_slovenia_eu_passport_number**|
|:-----|
|numéro de passeport  <br/> numéro de passeport slovène  <br/> passeport aucune  <br/> Številka potnega lista  <br/> |
   
## <a name="spain"></a>Espagne

### <a name="format"></a>Format

Une combinaison de huit ou neuf caractères de lettres et chiffres sans espaces ni les délimiteurs
  
### <a name="pattern"></a>Modèle

Une combinaison de huit ou neuf caractères de lettres et chiffres :
  
-  Deux chiffres ou des lettres 
    
- Un chiffre ou une lettre (facultatif)
    
- Six chiffres
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_spain_eu_passport_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_spain_eu_passport_number` est trouvée. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_passport_number" />
          <Match idRef="Keywords_spain_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_spain_eu_passport_number**|
|:-----|
|passeport  <br/> passeport Espagne  <br/> livre Passport  <br/> numéro de passeport  <br/> passeport aucune  <br/> libreta pasaporte  <br/> Número pasaporte  <br/> pasaporte España  <br/> pasaporte  <br/> |
   
## <a name="sweden"></a>Suède

Pour plus d’informations, voir la section « Numéro de passeport Suède » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="uk"></a>ROYAUME-UNI

Pour plus d’informations, consultez la section « Numéro de passeport US / britannique » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="see-also"></a>Voir aussi

[Éléments recherchés par les types d’informations sensibles](what-the-sensitive-information-types-look-for.md)

