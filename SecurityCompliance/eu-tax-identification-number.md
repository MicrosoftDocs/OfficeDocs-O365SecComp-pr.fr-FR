---
title: Numéro d’Identification de l’UE taxe
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: f04919c8-2356-4de2-bb2a-b9f67f339726
description: Cette rubrique illustre une stratégie de protection contre la perte données lorsqu’il détecte le type d’informations sensibles numéro d’Identification de taxe de l’UE. Ce type d’informations sensibles définit différents motifs, mots clés et autres pour chaque pays.
ms.openlocfilehash: 5192496b393d15fd6d063e09c9bfe1cb3dd7e2dd
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528076"
---
# <a name="eu-tax-identification-number"></a>Numéro d’Identification de l’UE taxe

Cette rubrique illustre une stratégie de protection contre la perte données lorsqu’il détecte le type d’informations sensibles de numéro d’Identification de l’UE taxe (TIN). Ce type d’informations sensibles définit différents motifs, mots clés et autres pour chaque pays.
  
## <a name="austria"></a>Autriche

### <a name="format"></a>Format

Neuf chiffres avec trait d’union conditionnel et une barre oblique
  
### <a name="pattern"></a>Modèle

Neuf chiffres avec trait d’union conditionnel et une barre oblique :
  
-  Deux chiffres 
    
- Un trait d’union (facultatif)
    
- Trois chiffres
    
- Une barre oblique (facultative)
    
- Quatre chiffres
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_austria_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_austria_eu_tax_file_number` est trouvée. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_austria_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_austria_eu_tax_file_number" />
          <Match idRef="Keywords_austria_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_austria_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsaustriaeutaxfilenumber"></a>Keywords_austria_eu_tax_file_number

numéro de taxe
  
nombre
  
numéro d’enregistrement taxe
  
id fiscal

  
St.nr.
  
steuernummer
  
## <a name="belgium"></a>Belgique

### <a name="format"></a>Format

11 chiffres sans espaces et les séparateurs
  
### <a name="pattern"></a>Modèle

11 chiffres :
  
- Deux chiffres
    
- Un « 0 » ou « 1 »
    
- Un chiffre
    
- Un « 0 » ou « 1 » ou « 2 » ou « 3 » 
    
- Six chiffres
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_belgium_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_belgium_eu_tax_file_number` est trouvée. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_tax_file_number" />
          <Match idRef="Keywords_belgium_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsbelgiumeutaxfilenumber"></a>Keywords_belgium_eu_tax_file_number

numéro de taxe
  
numéro national d’enregistrement
  
numéro d’enregistrement taxe
  
id fiscal

  
NIF
  
NIF #
  
numéro de registre national
  
numéro d’identification fiscale
  
## <a name="bulgaria"></a>Bulgarie

### <a name="format"></a>Format

Dix chiffres sans espaces et les séparateurs
  
### <a name="pattern"></a>Modèle

10 chiffres
  
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_bulgaria_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_bulgaria_eu_tax_file_number` est trouvée. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_bulgaria_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_bulgaria_eu_tax_file_number" />
          <Match idRef="Keywords_bulgaria_eu_tax_file_number" />
        </Pattern>
 <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_bulgaria_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsbulgariaeutaxfilenumber"></a>Keywords_bulgaria_eu_tax_file_number

bucn
  
nombre civile uniforme
  
bucn #
  
uniformcivilnumber #
  
id civile uniforme
  
no civile uniforme
  
egn
  
nombre de civile uniform bulgare
  
uniformcivilno #
  
egn #
  
УНИФОРМ ГРАЖДАНСКИ НОМЕР
  
Id униформ
  
Id граждански униформ
  
УНИФОРМ ГРАЖДАНСКИ НЕ
  
## <a name="croatia"></a>Croatie

### <a name="format"></a>Format

11 chiffres sans espaces ni les délimiteurs
  
### <a name="pattern"></a>Modèle

11 chiffres :
  
- Dix chiffres, choisis au hasard
    
- Chiffre un contrôle
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_croatia_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_croatia_eu_tax_file_number` est trouvée. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_croatia_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_croatia_eu_tax_file_number" />
          <Match idRef="Keywords_croatia_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_croatia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordscroatiaeutaxfilenumber"></a>Keywords_croatia_eu_tax_file_number

numéro de taxe
  
taxe
  
id fiscal

  
OID
  
OID #
  
porezni broj
  
## <a name="cyprus"></a>Chypre

### <a name="format"></a>Format

Huit chiffres et une lettre dans le modèle spécifié
  
### <a name="pattern"></a>Modèle

Huit chiffres et une lettre :
  
-  UN « 0 » 
    
- Sept chiffres 
    
- Une lettre (pas la casse)
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_cyprus_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_cyprus_eu_tax_file_number` est trouvée. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_cyprus_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_cyprus_eu_tax_file_number" />
          <Match idRef="Keywords_cyprus_eu_tax_file_number" />
        </Pattern>
Pattern confidenceLevel="75">
          <IdMatch idRef="Func_cyprus_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordscypruseutaxfilenumber"></a>Keywords_cyprus_eu_tax_file_number

numéro de taxe
  
taxe
  
id fiscal

  
codes d’identification
  
TIC
  
TIC #
  
ΑΡΙΘΜΌΣ ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ
  
ΦΟΡΟΛΟΓΙΚΉ ΤΑΥΤΌΤΗΤΑ
  
ΚΩΔΙΚΌΣ ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ
  
## <a name="czech-republic"></a>République tchèque

### <a name="format"></a>Format

Neuf ou dix chiffres avec une barre oblique inverse facultative
  
### <a name="pattern"></a>Modèle

Neuf ou dix chiffres avec un backslashl facultatif :
  
- Six chiffres 
    
- Une barre oblique inverse (facultative)
    
- Trois ou quatre chiffres
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_czech_republic_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_czech_republic_eu_tax_file_number` est trouvée. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_tax_file_number" />
          <Match idRef="Keywords_czech_republic_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsczechrepubliceutaxfilenumber"></a>Keywords_czech_republic_eu_tax_file_number

numéro de taxe
  
taxe
  
id fiscal

  
numéro de téléphone personnel
  
daňové číslo
  
osobní číslo
  
## <a name="denmark"></a>Danemark

### <a name="format"></a>Format

Dix chiffres contenant un trait d’union
  
### <a name="pattern"></a>Modèle

Dix chiffres contenant un hyphenl :
  
-  Six chiffres qui correspondent à la date de naissance (jjmmaa) 
    
- Un trait d’union 
    
- Quatre chiffres qui correspondent à un numéro de séquence où le premier chiffre correspond à la century de naissance et le dernier chiffre correspond au sexe de la personne (impaire pour masculin et même femme)
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_denmark_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_denmark_eu_tax_file_number` est trouvée. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_denmark_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_denmark_eu_tax_file_number" />
          <Match idRef="Keywords_denmark_eu_tax_file_number" />
        </Pattern> 
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_denmark_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsdenmarkeutaxfilenumber"></a>Keywords_denmark_eu_tax_file_number

numéro de taxe
  
taxe
  
id fiscal

  
nombre de CPR
  
CPR #
  
skat nummer
  
id skat
  
## <a name="estonia"></a>Estonie

### <a name="format"></a>Format

11 chiffres sans espaces ni les délimiteurs
  
### <a name="pattern"></a>Modèle

11 chiffres :
  
-  Un chiffre correspondant au sexe et century de naissance où un nombre impair indique masculin et le nombre pair femme comme suit : 1, 2 pour le 19 century ; 3, 4 pour le vingtième century ; 5 et 6 pour le century 21 
    
- Six chiffres qui correspondent à la date de naissance (AAMMJJ)
    
- Trois chiffres qui correspondent à un numéro de série en séparant les personnes naissance à la même date
    
- Chiffre un contrôle
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_estonia_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_estonia_eu_tax_file_number` est trouvée. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_estonia_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_estonia_eu_tax_file_number" />
          <Match idRef="Keywords_estonia_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_estonia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsestoniaeutaxfilenumber"></a>Keywords_estonia_eu_tax_file_number

numéro de taxe
  
taxe
  
id fiscal

  
code personnel
  
maksunumber
  
id maksu
  
isikukood
  
## <a name="finland"></a>Finlande

### <a name="format"></a>Format

Une combinaison de caractères 11 chiffres, des lettres, et plus et moins
  
### <a name="pattern"></a>Modèle

Une combinaison de caractères 11 chiffres, des lettres, et plus et moins :
  
- Six chiffres
    
- Un des éléments suivants : un signe plus, un signe moins ou la lettre « A » (pas la casse) où le signe signifie naissance entre 1800-1899, le signe moins signer signifie naissance entre 1900 à 1999 et « A » signifie naissance 2000 et après
    
- Trois chiffres
    
- Une lettre ou un numéro
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_finland_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_finland_eu_tax_file_number` est trouvée. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_finland_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finland_eu_tax_file_number" />
          <Match idRef="Keywords_finland_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_finland_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsfinlandeutaxfilenumber"></a>Keywords_finland_eu_tax_file_number

numéro d’identification

  
identifiant personnel
  
numéro d’identité
  
numéro d’id national Finlande
  
personalidnumber #
  
numéro d’identification nationale
  
numéro d’identification
  
id national aucun.
  
numéro national
  
ID d’aucun
  
tunnistenumero
  
henkilötunnus
  
yksilöllinen henkilökohtainen tunnistenumero
  
ainutlaatuinen henkilökohtainen tunnus
  
numero identiteetti
  
Suomen kansallinen henkilötunnus
  
henkilötunnusnumero #
  
kansallisen tunnistenumero
  
tunnusnumero
  
kansallinen tunnus numero
  
## <a name="france"></a>France

### <a name="format"></a>Format

13 chiffres pour les particuliers et les neuf chiffres pour les entités
  
### <a name="pattern"></a>Modèle

13 chiffres pour les personnes :
  
- Un chiffre doit être 0, 1, 2 ou 3
    
- 12 chiffres
    
Neuf chiffres pour les entités
  
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_france_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_france_eu_tax_file_number` est trouvée. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_france_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_france_eu_tax_file_number" />
          <Match idRef="Keywords_france_eu_tax_file_number" />
        </Pattern>
 <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_france_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsfranceeutaxfilenumber"></a>Keywords_france_eu_tax_file_number

numéro d’identification fiscale
  
numéro de taxe
  
id fiscal

  
numéro d’identification fiscale
  
## <a name="germany"></a>Allemagne

### <a name="format"></a>Format

11 chiffres sans espaces et les séparateurs
  
### <a name="pattern"></a>Modèle

11 chiffres :
  
-  Dix chiffres 
    
- Chiffre un contrôle
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_germany_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_germany_eu_tax_file_number` est trouvée. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_germany_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_germany_eu_tax_file_number" />
          <Match idRef="Keywords_germany_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_germany_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsgermanyeutaxfilenumber"></a>Keywords_germany_eu_tax_file_number

numéro de taxe
  
n° de taxe.
  
taxno #
  
Numéro taxe #
  
Numéro taxe
  
id fiscal

  
taxid #
  
numéro d’identification fiscale
  
identification de taxe ne.
  
steuernummer
  
id steuer
  
steueridentifikationsnummer
  
## <a name="greece"></a>Grèce

### <a name="format"></a>Format

Neuf chiffres sans espaces et les séparateurs
  
### <a name="pattern"></a>Modèle

Neuf chiffres
  
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_greece_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_greece_eu_tax_file_number` est trouvée. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_tax_file_number" />
          <Match idRef="Keywords_greece_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsgreeceeutaxfilenumber"></a>Keywords_greece_eu_tax_file_number

AFM
  
tin

  
id de taxe ne.
  
id de taxe ne
  
numéro d’identification fiscale
  
numéro de Registre de taxe
  
taxe non dans le Registre.
  
AFM #
  
numéro d’identification #
  
taxidno #
  
taxregistryno #
  
ΑΡΙΘΜΌΣ ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ
  
aφμ
  
aφμ αριθμός
  
ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ ΝΟ.
  
ΤΟΝ ΑΡΙΘΜΌ ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ
  
## <a name="hungary"></a>Hongrie

### <a name="format"></a>Format

Dix chiffres sans espaces ni les délimiteurs
  
### <a name="pattern"></a>Modèle

Dix chiffres :
  
-  Un chiffre doit être « 8 » 
    
- Cinq chiffres qui correspondent au nombre de jours entre la date 01/01/1867 et la date de naissance de la personne
    
- Trois chiffres correspondant au numéro généré par hasard pour différencier les personnes naissance le même jour
    
- Chiffre un contrôle
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_hungary_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_hungary_eu_tax_file_number` est trouvée. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_hungary_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_hungary_eu_tax_file_number" />
          <Match idRef="Keywords_hungary_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_hungary_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordshungaryeutaxfilenumber"></a>Keywords_hungary_eu_tax_file_number

numéro d’identification fiscale hongrois
  
numéro d’identification hongrois
  
numéro d’identification de taxe
  
numéro de TVA
  
fiscale ne
  
numéro d’identité Tax id taxe
  
taxidnumber #
  
numéro d’identification #
  
hungatiantin #
  
identification de taxe ne
  
taxidno #
  
adóazonosító szám
  
adószám
  
adóhatóság szám
  
## <a name="ireland"></a>Irlande

### <a name="format"></a>Format

Sept chiffres suivies d’une lettre sans espaces ni les délimiteurs
  
### <a name="pattern"></a>Modèle

Sept chiffres suivies d’une lettre :
  
-  Sept chiffres  
    
- Une lettre (pas la casse)
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_ireland_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_ireland_eu_tax_file_number` est trouvée. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_ireland_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_ireland_eu_tax_file_number" />
          <Match idRef="Keywords_ireland_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_ireland_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsirelandeutaxfilenumber"></a>Keywords_ireland_eu_tax_file_number

service public aucune
  
service public personnel aucune
  
PPS aucune
  
personnel n° de service
  
n° du service PPS
  
ppsno #
  
irlandais pps aucune
  
publicserviceno #
  
numéro personnel service public
  
uimhir phearsanta seirbhíse poiblí
  
uimh PPS
  
uimhir aitheantais phearsanta
  
## <a name="italy"></a>Italie

### <a name="format"></a>Format

16 lettres et chiffres dans le modèle spécifié
  
### <a name="pattern"></a>Modèle

16 lettres et chiffres :
  
-  Trois lettres qui correspondent aux trois premiers consonnes suivantes dans le nom de famille 
    
- Trois lettres qui correspondent à la première, troisième et quatrième consonnes dans le premier nom
    
- Deux chiffres qui correspondent à la dernière chiffres de l’année de naissance
    
- Un chiffre qui correspond au mois de naissance — lettres sont utilisés dans l’ordre alphabétique, mais que les lettres A à E, H, L, M, P, R t sont utilisés (par conséquent, janvier correspond à un et octobre est R)
    
- Deux chiffres correspondant au jour du mois de naissance où 40 est ajouté à la journée de naissance pour femelles différencier les mâles
    
- Quatre chiffres qui correspondent à un code de zone spécifique à la commune où naissance de la personne, les codes de pays échelle sont utilisés pour étranger
    
- Chiffre un contrôle
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_italy_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_italy_eu_tax_file_number` est trouvée. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_italy_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_italy_eu_tax_file_number" />
          <Match idRef="Keywords_italy_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_italy_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsitalyeutaxfilenumber"></a>Keywords_italy_eu_tax_file_number

numéro de taxe
  
n° de taxe.
  
taxno #
  
Numéro taxe #
  
Numéro taxe
  
id fiscal

  
taxid #
  
code fiscal
  
numéro d’identification fiscale
  
## <a name="latvia"></a>Lettonie

### <a name="format"></a>Format

11 chiffres sans espaces ni les délimiteurs
  
### <a name="pattern"></a>Modèle

11 chiffres dans le modèle spécifié
  
-  Six chiffres qui correspondent à la date de naissance (jjmmaa) 
    
- Un chiffre qui correspond à la century de naissance où « 0 » correspond à 19 century, « 1 » correspond à 20 century et « 2 » correspond à century 21
    
- Quatre chiffres
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_latvia_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_latvia_eu_tax_file_number` est trouvée. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_latvia_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_latvia_eu_tax_file_number" />
          <Match idRef="Keywords_latvia_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_latvia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordslatviaeutaxfilenumber"></a>Keywords_latvia_eu_tax_file_number

numéro de taxe
  
n° de taxe.
  
taxno #
  
Numéro taxe #
  
Numéro taxe
  
id fiscal

  
taxid #
  
numéro d’identification fiscale
  
identification de taxe ne.
  
nodokļa numurs
  
nodokļu identifikācijas numurs
  
nodokļu identifikācija numurs
  
## <a name="lithuania"></a>Lituanie

### <a name="format"></a>Format

11 chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

11 chiffres
  
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_lithuania_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_lithuania_eu_tax_file_number` est trouvée. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_lithuania_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_lithuania_eu_tax_file_number" />
          <Match idRef="Keywords_lithuania_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_lithuania_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordslithuaniaeutaxfilenumber"></a>Keywords_lithuania_eu_tax_file_number

numéro de taxe
  
n° de taxe.
  
fiscales no #
  
Numéro taxe #
  
Numéro taxe
  
id fiscal

  
taxid #
  
numéro d’identification fiscale
  
identification de taxe ne.
  
id mokesčių
  
mokesčių numeris
  
mokesčių identifikavimas numeris
  
## <a name="luxemburg"></a>Luxembourg

### <a name="format"></a>Format

13 chiffres sans espaces ni les délimiteurs
  
### <a name="pattern"></a>Modèle

13 chiffres :
  
-  11 chiffres 
    
- Deux chiffres de contrôle
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_luxemburg_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_luxemburg_eu_tax_file_number` est trouvée. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_luxemburg_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_luxemburg_eu_tax_file_number" />
          <Match idRef="Keywords_luxemburg_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_luxemburg_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsluxemburgeutaxfilenumber"></a>Keywords_luxemburg_eu_tax_file_number

numéro de taxe
  
n° de taxe.
  
taxno #
  
Numéro taxe #
  
Numéro taxe
  
id fiscal

  
taxid #
  
numéro d’identification fiscale
  
identification de taxe ne.
  
steuernummer
  
id steuer
  
steueridentifikationsnummer
  
## <a name="malta"></a>Malte

### <a name="format"></a>Format

Pour maltaise nationaux : 7 chiffres et une lettre dans le modèle spécifié
  
Non-maltaise nationaux et les entités maltaises : 9 chiffres
  
### <a name="pattern"></a>Modèle

Maltais nationaux : 7 chiffres et une lettre
  
-  Sept chiffres  
    
- Une lettre (pas la casse)
    
Non-maltaise nationaux et les entités maltaises : 9 chiffres
  
-  Neuf chiffres 
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_malta_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_malta_eu_tax_file_number` est trouvée. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_malta_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_malta_eu_tax_file_number" />
          <Match idRef="Keywords_malta_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_malta_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsmaltaeutaxfilenumber"></a>Keywords_malta_eu_tax_file_number

numéro de taxe
  
n° de taxe.
  
taxno #
  
Numéro taxe #
  
Numéro taxe
  
id fiscal

  
taxid #
  
numéro d’identification fiscale
  
identification de taxe ne.
  
tat-taxxa numru
  
ID tat-taxxa
  
numru ta ' identifikazzjoni tat-taxxa
  
## <a name="netherlands"></a>Pays-Bas

### <a name="format"></a>Format

Neuf chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

Neuf chiffres 
  
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_netherlands_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_netherlands_eu_tax_file_number` est trouvée. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_netherlands_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_netherlands_eu_tax_file_number" />
          <Match idRef="Keywords_netherlands_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_netherlands_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsnetherlandseutaxfilenumber"></a>Keywords_netherlands_eu_tax_file_number

numéro d’identification fiscale pays-bas
  
identification de taxe pays-bas
  
numéro d’identification du Antilles taxe
  
identification de taxe du Antilles
  
numéro d’identification fiscale
  
id de taxe néerlandais
  
numéro d’identification fiscale néerlandais
  
id fiscal

  
n° de sécurité sociale
  
numéro de taxe
  
fiscales no #
  
taxe #
  
tin

  
numéro d’identification #
  
numéro d’identification pays-bas
  
numéro d’identification du Antilles
  
néerlandais Omzetbelasting identificatienummer
  
identificatienummer van Omzetbelasting
  
Omzetbelasting identificatienummer
  
néerlandais Omzetbelasting identificatie
  
néerlandais Omzetbelasting id nummer
  
néerlandais belastingnummer
  
BTW nummer
  
Nederlandse Omzetbelasting identificatie
  
## <a name="poland"></a>Pologne

### <a name="format"></a>Format

Onze chiffres sans espaces ni les délimiteurs
  
### <a name="pattern"></a>Modèle

Onze chiffres
  
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_poland_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_poland_eu_tax_file_number` est trouvée. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_poland_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_poland_eu_tax_file_number" />
          <Match idRef="Keywords_poland_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_poland_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordspolandeutaxfilenumber"></a>Keywords_poland_eu_tax_file_number

numéro de taxe
  
n° de taxe.
  
taxno #
  
Numéro taxe #
  
Numéro taxe
  
point de contact
  
point de contact #
  
id fiscal

  
n° de sécurité sociale
  
id du point de contact
  
numéro d’identification de point de contact
  
numéro d’identification fiscale
  
identification de taxe ne.
  
numéro de TVA
  
taxe non.
  
vatno #
  
code de taxes
  
numéro d’identification de TVA
  
nombre identyfikacji podatkowej
  
polski nombre identyfikacji podatkowej
  
numeridentyfikacjipodatkowej #
  
## <a name="portugal"></a>Portugal

### <a name="format"></a>Format

Neuf chiffres sans espaces ni les délimiteurs
  
### <a name="pattern"></a>Modèle

Neuf chiffres
  
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_portugal_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_portugal_eu_tax_file_number` est trouvée. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_portugal_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_portugal_eu_tax_file_number" />
          <Match idRef="Keywords_portugal_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_portugal_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsportugaleutaxfilenumber"></a>Keywords_portugal_eu_tax_file_number

numéro de taxe
  
n° de taxe.
  
taxno #
  
Numéro taxe #
  
Numéro taxe
  
NIF
  
NIF #
  
NUMERO fiscal
  
Número de identificação fiscale
  
## <a name="romania"></a>Roumanie

### <a name="format"></a>Format

13 chiffres sans espaces ni les délimiteurs
  
### <a name="pattern"></a>Modèle

13 chiffres
  
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_romania_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_romania_eu_tax_file_number` est trouvée. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_tax_file_number" />
          <Match idRef="Keywords_romania_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsromaniaeutaxfilenumber"></a>Keywords_romania_eu_tax_file_number

id fiscal

  
numéro d’identification de taxe
  
Aucun fichier de taxe
  


numéro de dossier fiscal
  
n° de taxe
  
numéro de taxe
  
taxid #
  
taxno #
  
ID-ul taxei
  
numărul de identificare fiscală
  
## <a name="slovakia"></a>République de Slovaquie

### <a name="format"></a>Format

10 chiffres sans espaces ni les délimiteurs
  
### <a name="pattern"></a>Modèle

10 chiffres
  
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_slovakia_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_slovakia_eu_tax_file_number` est trouvée. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_tax_file_number" />
          <Match idRef="Keywords_slovakia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsslovakiaeutaxfilenumber"></a>Keywords_slovakia_eu_tax_file_number

id fiscal

  
numéro d’identification de taxe
  
id d’étain
  
no étain
  
id d’étain slovaque
  
tin

  
Aucun fichier de taxe
  


numéro de dossier fiscal
  
n° de taxe
  
numéro de taxe
  
taxid #
  
taxno #
  
daňové identifikačné číslo
  
daňové číslo
  
daňové číslo súboru
  
## <a name="slovenia"></a>Slovénie

### <a name="format"></a>Format

Huit chiffres sans espaces ni les délimiteurs
  
### <a name="pattern"></a>Modèle

Huit chiffres
  
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_slovenia_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_slovenia_eu_tax_file_number` est trouvée. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_slovenia_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_nation_eu_tax_file_number" />
          <Match idRef="Keywords_nation_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_slovenia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordssloveniaeutaxfilenumber"></a>Keywords_slovenia_eu_tax_file_number

id fiscal

  
numéro d’identification de taxe
  
id d’étain
  
no étain
  
id d’étain slovène
  
tin

  
Aucun fichier de taxe
  


numéro de dossier fiscal
  
n° de taxe
  
numéro de taxe
  
taxid #
  
taxno #
  
identifikacijska številka davka
  
davčna številka
  
Številka davčne datoteke
  
## <a name="spain"></a>Espagne

### <a name="format"></a>Format

Sept ou huit chiffres et une ou deux lettres dans le modèle spécifié
  
### <a name="pattern"></a>Modèle

Espagnols personnes physiques avec une carte d’identité National Espagne :
  
-  Huit chiffres 
    
- Une lettre majuscule (respecte la casse) 
    
Spaniards non résident sans une carte d’identité National Espagne
  
- Une lettre majuscule « L » (respecte la casse)
    
- Sept chiffres 
    
- Une lettre majuscule (respecte la casse) 
    
Spaniards résident sous l’âge de 14 ans sans un Espagne National carte d’identité :
  
- Une lettre majuscule « K » (respecte la casse)
    
-  Sept chiffres  
    
- Une lettre majuscule (respecte la casse)
    
Étrangers avec numéro d’Identification d’un étranger
  
- Majuscules une lettre qui est « X », « Y » ou « Z » (respecte la casse) 
    
- Sept chiffres 
    
- Une lettre majuscule (respecte la casse) 
    
Étrangers sans numéro d’Identification d’un étranger
  
- Une lettre est « M » (respecte la casse) 
    
- Sept chiffres 
    
- Une lettre majuscule (respecte la casse) 
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_spain_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_spain_eu_tax_file_number` est trouvée. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_spain_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_spain_eu_tax_file_number" />
          <Match idRef="Keywords_spain_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsspaineutaxfilenumber"></a>Keywords_spain_eu_tax_file_number

id fiscal

  
numéro d’identification de taxe
  
id CIF
  
CIF aucune
  
id cif espagnol
  
CIF
  
Aucun fichier de taxe
  
nombre cif espagnol
  


numéro de dossier fiscal
  
Espagnol cif aucune
  
n° de taxe
  
numéro de taxe
  
taxid #
  
taxno #
  
cifid #
  
spanishcifid #
  
spanishcifno #
  
Número de contribuyente
  
Número de impuesto corporativo
  
Número de identificación fiscale
  
CIF número
  
cifnúmero #
  
## <a name="sweden"></a>Suède

### <a name="format"></a>Format

Dix chiffres et un symbole dans le modèle spécifié
  
### <a name="pattern"></a>Modèle

Dix chiffres et un symbole :
  
-  Six chiffres qui correspondent à la date de naissance (AAMMJJ) 
    
- Un signe plus, un signe moins ou une barre oblique inverse
    
- Trois chiffres qui permettent l’identification numéro unique emplacement : 
    
  - Pour les numéros émis avant 1990, le chiffre septième et huitième identifier la région de naissance ou personnes foreign-born
    
  - Indique le chiffre en neuvième position sexe soit impair pour masculin ou même pour femme
    
- Chiffre un contrôle
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_sweden_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_sweden_eu_tax_file_number` est trouvée. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_sweden_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_sweden_eu_tax_file_number" />
          <Match idRef="Keywords_sweden_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_sweden_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsswedeneutaxfilenumber"></a>Keywords_sweden_eu_tax_file_number

id fiscal

  
id de taxe ne.
  
numéro d’identification de taxe
  
identification fiscale

  
identification Tax #
  
n° de taxe.
  
taxe #
  
taxid #
  
fichier de taxe
  
fiscales aucun fichier.
  
numéro d’identification personnelle
  
skatt id nummer
  
skatt identifikation
  
personnummer
  
## <a name="uk"></a>ROYAUME-UNI

### <a name="format"></a>Format

Référence de contribuable unique (UTR) : 10 chiffres sans espaces et les séparateurs
  
Numéro de sécurité sociale (NINO) : Pour plus d’informations, voir la section « britannique assurance nationale nombre (NINO) » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
  
### <a name="pattern"></a>Modèle

Référence de contribuable unique (UTR) : 10 chiffres
  
Numéro de sécurité sociale (NINO) : Pour plus d’informations, voir la section « britannique assurance nationale nombre (NINO) » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
  
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_uk_eu_tax_file_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_uk_eu_tax_file_number` est trouvée. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_uk_eu_tax_file_number" />
          <Match idRef="Keywords_uk_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsukeutaxfilenumber"></a>Keywords_uk_eu_tax_file_number

id fiscal

  
id de taxe ne.
  
numéro d’identification de taxe
  
identification fiscale

  
identification Tax #
  
n° de taxe.
  
taxe #
  
taxid #
  
fichier de taxe
  
fiscales aucun fichier.
  
## <a name="see-also"></a>Voir aussi

[Éléments recherchés par les types d’informations sensibles](what-the-sensitive-information-types-look-for.md)

