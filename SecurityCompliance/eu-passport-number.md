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
# <a name="eu-passport-number"></a>Numéro de passeport UE

Cette rubrique présente ce qu'une stratégie de protection contre la perte de données (DLP) recherche lorsqu'elle détecte le type d'informations sensibles du numéro de passeport de l'UE. Ce type d'informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.
  
## <a name="austria"></a>Autriche

### <a name="format"></a>Format

Une lettre suivie d'un espace facultatif et de sept chiffres
  
### <a name="pattern"></a>Modèle

Une combinaison d'une lettre, de sept chiffres et d'un espace:
  
- Une lettre (ne respecte pas la casse)
    
- Un espace (facultatif)
    
- Sept chiffres
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_austria_eu_passport_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_austria_eu_passport_number` from est trouvé. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_passport_number" />
          <Match idRef="Keywords_austria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_austria_eu_passport_number**|
|:-----|
|Numéro de passeport  <br/> Numéro de passeport autrichien  <br/> Numéro de passeport  <br/> reisepass  <br/> österreichisch Reisepass  <br/> |
   
## <a name="belgium"></a>Belgique

### <a name="format"></a>Format

Deux lettres suivies de six chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

Deux lettres et suivies de six chiffres
  
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_belgium_eu_passport_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_belgium_eu_passport_number` from est trouvé. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium__eu_passport_number" />
          <Match idRef="Keywords_belgium_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_belgium_eu_passport_number**|
|:-----|
|Numéro de passeport  <br/> Numéro de passeport belge  <br/> Numéro de passeport  <br/> paspoort  <br/> paspoortnummer  <br/> Reisepass kein  <br/> reisepass  <br/> |
   
## <a name="bulgaria"></a>Bulgarie

### <a name="format"></a>Format

Neuf chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

 Neuf chiffres 
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_bulgaria_eu_passport_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_bulgaria_eu_passport_number` from est trouvé. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_passport_number" />
          <Match idRef="Keywords_bulgaria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_bulgaria_eu_passport_number**|
|:-----|
|Numéro de passeport  <br/> Numéro de Passeport bulgare  <br/> Numéro de passeport  <br/> номер на паспорта  <br/> |
   
## <a name="croatia"></a>Croatie

### <a name="format"></a>Format

Neuf chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

 Neuf chiffres 
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_croatia_eu_passport_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_croatia_eu_passport_number` from est trouvé. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_passport_number" />
          <Match idRef="Keywords_croatia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_croatia_eu_passport_number**|
|:-----|
|Numéro de passeport  <br/> Numéro de passeport croate  <br/> Numéro de passeport  <br/> Broj putovnice  <br/> |
   
## <a name="cyprus"></a>Chypre

### <a name="format"></a>Format

Une lettre suivie de 6-8 chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

Une lettre suivie de six à huit chiffres
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_cyprus_eu_passport_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_cyprus_eu_passport_number` from est trouvé. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_passport_number" />
          <Match idRef="Keywords_cyprus_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_cyprus_eu_passport_number**|
|:-----|
|Numéro de passeport  <br/> Numéro de passeport de Chypre  <br/> Numéro de passeport  <br/> αριθμό διαβατηρίου  <br/> |
   
## <a name="czech-republic"></a>République tchèque

### <a name="format"></a>Format

Huit chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

Huit chiffres sans espaces ni délimiteurs
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_czech_republic_eu_passport_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_czech_republic_eu_passport_number` from est trouvé. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_passport_number" />
          <Match idRef="Keywords_czech_republic_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_czech_republic_eu_passport_number**|
|:-----|
|Numéro de passeport  <br/> Numéro de passeport tchèque  <br/> Numéro de passeport  <br/> CESTOVNÍ pas  <br/> boîte  <br/> |
   
## <a name="denmark"></a>Danemark

### <a name="format"></a>Format

Neuf chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

 Neuf chiffres 
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_denmark_eu_passport_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_denmark_eu_passport_number` from est trouvé. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_passport_number" />
          <Match idRef="Keywords_denmark_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_denmark_eu_passport_number**|
|:-----|
|Numéro de passeport  <br/> Numéro de passeport danois  <br/> Numéro de passeport  <br/> boîte  <br/> pasnummer  <br/> |
   
## <a name="estonia"></a>Estonie

### <a name="format"></a>Format

Une lettre suivie de sept chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

Une lettre suivie de sept chiffres
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_estonia_eu_passport_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_estonia_eu_passport_number` from est trouvé. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_passport_number" />
          <Match idRef="Keywords_estonia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_estonia_eu_passport_number**|
|:-----|
|Numéro de passeport  <br/> Numéro de passeport estonien  <br/> Numéro de passeport  <br/> Eesti kodaniku  <br/> |
   
## <a name="finland"></a>Finlande

Pour plus d'informations, consultez la section «numéro de passeport de Finlande» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="france"></a>France

Pour plus d'informations, consultez la section «numéro de passeport français» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="germany"></a>Allemagne

Pour plus d'informations, reportez-vous à la section «numéro de passeport allemand» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="greece"></a>Grèce

### <a name="format"></a>Format

Deux lettres suivies de sept chiffres, sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

Deux lettres suivies de sept chiffres
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_greece_eu_passport_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_greece_eu_passport_number` from est trouvé. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_passport_number" />
          <Match idRef="Keywords_greece_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_greece_eu_passport_number**|
|:-----|
|Numéro de passeport  <br/> Numéro de passeport grec  <br/> Numéro de passeport  <br/> διαβατηριο  <br/> |
   
## <a name="hungary"></a>Hongrie

### <a name="format"></a>Format

Deux lettres suivies de six ou sept chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

Deux lettres suivies de six ou sept chiffres
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_hungary_eu_passport_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_hungary_eu_passport_number` from est trouvé. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_passport_number" />
          <Match idRef="Keywords_hungary_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_hungary_eu_passport_number**|
|:-----|
|Numéro de passeport  <br/> Numéro de passeport hongrois  <br/> Numéro de passeport  <br/> útlevél száma  <br/> |
   
## <a name="ireland"></a>Irlande

### <a name="format"></a>Format

Deux lettres ou chiffres suivis de sept chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

Deux lettres ou chiffres suivis de sept chiffres:
  
- Deux chiffres ou lettres (ne respectent pas la casse)
    
- Sept chiffres
    
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_ireland_eu_passport_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_ireland_eu_passport_number` from est trouvé. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_passport_number" />
          <Match idRef="Keywords_ireland_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_ireland_eu_passport_number**|
|:-----|
|Numéro de passeport  <br/> Numéro de passeport irlandais  <br/> Numéro de passeport  <br/> boîte  <br/> passeport  <br/> passeport  <br/> passeport numérique  <br/> |
   
## <a name="italy"></a>Italie

### <a name="format"></a>Format

Deux lettres ou chiffres suivis de sept chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

Deux lettres ou chiffres suivis de sept chiffres:
  
- Deux chiffres ou lettres (ne respectent pas la casse)
    
- Sept chiffres
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_italy_eu_passport_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_italy_eu_passport_number` from est trouvé. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_passport_number" />
          <Match idRef="Keywords_italy_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_italy_eu_passport_number**|
|:-----|
|Numéro de passeport italien  <br/> Repubblica Italiana passaporto  <br/> passaporto  <br/> passaporto Italiana  <br/> Numéro de passeport  <br/> Italiana passaporto numérique  <br/> passaporto numérique  <br/> numéro passeport italien  <br/> numéro passeport  <br/> |
   
## <a name="latvia"></a>Lettonie

### <a name="format"></a>Format

Deux lettres ou chiffres suivis de sept chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

Deux lettres ou chiffres suivis de sept chiffres:
  
- Deux chiffres ou lettres (ne respectent pas la casse)
    
- Sept chiffres
    
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_latvia_eu_passport_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_latvia_eu_passport_number` from est trouvé. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_passport_number" />
          <Match idRef="Keywords_latvia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_latvia_eu_passport_number**|
|:-----|
|Numéro de passeport  <br/> Numéro de passeport letton  <br/> Numéro de passeport  <br/> pase numurs  <br/> |
   
## <a name="lithuania"></a>Lituanie

### <a name="format"></a>Format

Huit chiffres ou lettres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

Huit chiffres ou lettres (ne respectant pas la casse)
  
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_lithuania_eu_passport_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_lithuania_eu_passport_number` from est trouvé. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_passport_number" />
          <Match idRef="Keywords_lithuania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_lithuania_eu_passport_number**|
|:-----|
|Numéro de passeport  <br/> Numéro de passeport lithunian  <br/> Numéro de passeport  <br/> Paso chiffres  <br/> |
   
## <a name="luxemburg"></a>Relatif

### <a name="format"></a>Format

Huit chiffres ou lettres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

Huit chiffres ou lettres (ne respectant pas la casse)
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_nation_eu_passport_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_nation_eu_passport_number` from est trouvé. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_nation_eu_passport_number" />
          <Match idRef="Keywords_nation_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_nation_eu_passport_number**|
|:-----|
|Numéro de passeport  <br/> Numéro de passeport letton  <br/> Numéro de passeport  <br/> passnummer  <br/> |
   
## <a name="malta"></a>Malte

### <a name="format"></a>Format

Sept chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

 Sept chiffres 
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_malta_eu_passport_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_malta_eu_passport_number` from est trouvé. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_passport_number" />
          <Match idRef="Keywords_malta_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_malta_eu_passport_number**|
|:-----|
|Numéro de passeport  <br/> Numéro de passeport maltais  <br/> Numéro de passeport  <br/> numru Tal-Passaport  <br/> |
   
## <a name="netherlands"></a>Pays-Bas

### <a name="format"></a>Format

Neuf lettres ou chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

Neuf lettres ou chiffres
  
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_netherlands_eu_passport_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_netherlands_eu_passport_number` from est trouvé. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_passport_number" />
          <Match idRef="Keywords_netherlands_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_netherlands_eu_passport_number**|
|:-----|
|Numéro de passeport néerlandais  <br/> Numéro de passeport  <br/> Numéro de passeport néerlandais  <br/> Nederlanden paspoort Nummer  <br/> paspoort  <br/> Nederlanden paspoortnummer  <br/> paspoortnummer  <br/> |
   
## <a name="poland"></a>Pologne

Pour plus d'informations, reportez-vous à la section «numéro de passeport polonais» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="portugal"></a>Portugal

### <a name="format"></a>Format

Une lettre suivie de six chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

Une lettre suivie de six chiffres:
  
- Une lettre (ne respecte pas la casse)
    
- Six chiffres
    
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_portugal_eu_passport_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_portugal_eu_passport_number` from est trouvé. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_passport_number" />
          <Match idRef="Keywords_portugal_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_portugal_eu_passport_number**|
|:-----|
|Numéro de passeport  <br/> Numéro de passeport Portugais  <br/> Numéro de passeport  <br/> número do Passaporte  <br/> |
   
## <a name="romania"></a>Roumanie

### <a name="format"></a>Format

Huit ou neuf chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

Huit ou neuf chiffres
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_romania_eu_passport_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_romania_eu_passport_number` from est trouvé. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_passport_number" />
          <Match idRef="Keywords_romania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_romania_eu_passport_number**|
|:-----|
|Numéro de passeport  <br/> Numéro de passeport roumain  <br/> Numéro de passeport  <br/> numărul pașaportului  <br/> |
   
## <a name="slovakia"></a>République de Slovaquie

### <a name="format"></a>Format

Un chiffre ou une lettre suivi de sept chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

Un chiffre ou une lettre (ne respectant pas la casse) suivi de sept chiffres
  
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_slovakia_eu_passport_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_slovakia_eu_passport_number` from est trouvé. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_passport_number" />
          <Match idRef="Keywords_slovakia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_slovakia_eu_passport_number**|
|:-----|
|Numéro de passeport  <br/> Numéro de passeport slovaque  <br/> Numéro de passeport  <br/> číslo Pasu  <br/> |
   
## <a name="slovenia"></a>Slovénie

### <a name="format"></a>Format

Deux lettres suivies de sept chiffres, sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

Deux lettres suivies de sept chiffres:
  
- La lettre «P»
    
- Une lettre majuscule
    
- Sept chiffres
    
### <a name="checksum"></a>Somme de contrôle

Non
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_slovenia_eu_passport_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_slovenia_eu_passport_number` from est trouvé. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_passport_number" />
          <Match idRef="Keywords_slovenia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_slovenia_eu_passport_number**|
|:-----|
|Numéro de passeport  <br/> Numéro de passeport slovène  <br/> Numéro de passeport  <br/> številka potnega Lista  <br/> |
   
## <a name="spain"></a>Espagne

### <a name="format"></a>Format

Combinaison de huit ou neuf caractères de lettres et de chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

Combinaison de huit ou neuf caractères de lettres et de chiffres:
  
-  Deux chiffres ou lettres 
    
- Un chiffre ou une lettre (facultatif)
    
- Six chiffres
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L'expression `Regex_spain_eu_passport_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_spain_eu_passport_number` from est trouvé. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_passport_number" />
          <Match idRef="Keywords_spain_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots-clés

| |
|**Keywords_spain_eu_passport_number**|
|:-----|
|passeport  <br/> Passport Espagne  <br/> livre de passeport  <br/> Numéro de passeport  <br/> Numéro de passeport  <br/> Libreta pasaporte  <br/> número pasaporte  <br/> España pasaporte  <br/> pasaporte  <br/> |
   
## <a name="sweden"></a>Suède

Pour plus d'informations, reportez-vous à la section «numéro de passeport Suède» dans [ce que recherche les types d'informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="uk"></a>R.U.

Pour plus d'informations, reportez-vous à la section «US/numéro de passeport britannique» dans les [types d'informations sensibles que vous recherchez](what-the-sensitive-information-types-look-for.md).
  
## <a name="see-also"></a>Voir aussi

[Éléments recherchés par les types d’informations sensibles](what-the-sensitive-information-types-look-for.md)

