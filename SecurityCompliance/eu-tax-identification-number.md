---
title: Numéro d’identification fiscale de l’UE
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: Cette rubrique montre ce qu’une stratégie de protection contre la perte de données (DLP) recherche lorsqu’il détecte le type d’informations sensibles du numéro d’identification fiscale de l’UE. Ce type d’informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.
ms.openlocfilehash: adcd9be9b5f8775ad39010d771ff2ac214df1e17
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34152956"
---
# <a name="eu-tax-identification-number"></a>Numéro d’identification fiscale de l’UE

Cette rubrique montre ce qu’une stratégie de protection contre la perte de données (DLP) recherche lorsqu’il détecte le type d’informations sensibles de l’ID taxe de l’UE (TIN). Ce type d’informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.
  
## <a name="austria"></a>Autriche

### <a name="format"></a>Format

Neuf chiffres avec un trait d’union conditionnel et une barre oblique
  
### <a name="pattern"></a>Modèle

Neuf chiffres avec un trait d’Union et une barre oblique facultatifs:
  
-  Deux chiffres 
    
- Un trait d’union (facultatif)
    
- Trois chiffres
    
- Une barre oblique (facultative)
    
- Quatre chiffres
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_austria_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_austria_eu_tax_file_number` from est trouvé. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_austria_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
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

### <a name="keywords"></a>Mots clés

#### <a name="keywordsaustriaeutaxfilenumber"></a>Keywords_austria_eu_tax_file_number

Numéro de taxe
  
number
  
Numéro d’enregistrement taxe
  
id fiscal
  
st.nr.
  
steuernummer
  
## <a name="belgium"></a>Belgique

### <a name="format"></a>Format

11 chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

11 chiffres :
  
- Deux chiffres
    
- «0» ou «1»
    
- Un chiffre
    
- «0» ou «1» ou «2» ou «3» 
    
- Six chiffres
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression `Regex_belgium_eu_tax_file_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_belgium_eu_tax_file_number` from est trouvé. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_tax_file_number" />
          <Match idRef="Keywords_belgium_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordsbelgiumeutaxfilenumber"></a>Keywords_belgium_eu_tax_file_number

Numéro de taxe
  
Numéro d’enregistrement national
  
Numéro d’enregistrement taxe
  
id fiscal
  
nPour
  
nPour
  
Numéro de registre national
  
Numéro d’identification fiscale
  
## <a name="bulgaria"></a>Bulgarie

### <a name="format"></a>Format

Dix chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

10 chiffres
  
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_bulgaria_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_bulgaria_eu_tax_file_number` from est trouvé. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_bulgaria_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
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

### <a name="keywords"></a>Mots clés

#### <a name="keywordsbulgariaeutaxfilenumber"></a>Keywords_bulgaria_eu_tax_file_number

bucn
  
numéro civil uniforme
  
bucn#
  
uniformcivilnumber#
  
ID civil uniforme
  
non civil uniforme
  
egn
  
numéro civil uniforme bulgare
  
uniformcivilno#
  
egn#
  
униформ граждански номер
  
ID униформ
  
униформ граждански ID
  
униформ граждански не
  
## <a name="croatia"></a>Croatie

### <a name="format"></a>Format

11 chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

11 chiffres :
  
- Dix chiffres, choisis de manière aléatoire
    
- Un chiffre de contrôle
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_croatia_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_croatia_eu_tax_file_number` from est trouvé. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_croatia_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
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

### <a name="keywords"></a>Mots clés

#### <a name="keywordscroatiaeutaxfilenumber"></a>Keywords_croatia_eu_tax_file_number

Numéro de taxe
  
codes
  
id fiscal
  
oid
  
OID
  
porezni broj
  
## <a name="cyprus"></a>Chypre

### <a name="format"></a>Format

Huit chiffres et une lettre dans le modèle spécifié
  
### <a name="pattern"></a>Modèle

Huit chiffres et une lettre:
  
-  «0» 
    
- Sept chiffres 
    
- Une lettre (ne respecte pas la casse)
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_cyprus_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_cyprus_eu_tax_file_number` from est trouvé. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_cyprus_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
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

### <a name="keywords"></a>Mots clés

#### <a name="keywordscypruseutaxfilenumber"></a>Keywords_cyprus_eu_tax_file_number

Numéro de taxe
  
codes
  
id fiscal
  
code d’identification fiscale
  
graduation
  
graduation
  
αριθμός φορολογικού μητρώου
  
φορολογική ταυτότητα
  
κωδικός φορολογικού μητρώου
  
## <a name="czech-republic"></a>République tchèque

### <a name="format"></a>Format

Neuf ou dix chiffres avec une barre oblique inverse facultative
  
### <a name="pattern"></a>Modèle

Neuf ou dix chiffres avec une barre oblique inverse facultative:
  
- Six chiffres 
    
- Une barre oblique inverse (facultatif)
    
- 3 ou 4 chiffres
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression `Regex_czech_republic_eu_tax_file_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_czech_republic_eu_tax_file_number` from est trouvé. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_tax_file_number" />
          <Match idRef="Keywords_czech_republic_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordsczechrepubliceutaxfilenumber"></a>Keywords_czech_republic_eu_tax_file_number

Numéro de taxe
  
codes
  
id fiscal
  
numéro personnel
  
daňové číslo
  
osobní číslo
  
## <a name="denmark"></a>Danemark

### <a name="format"></a>Format

Dix chiffres contenant un trait d’Union
  
### <a name="pattern"></a>Modèle

Dix chiffres contenant un trait d’Union:
  
-  Six chiffres correspondant à la date de naissance (JJMMAA) 
    
- Un trait d’union 
    
- Quatre chiffres correspondant à un numéro de séquence où le premier chiffre correspond au siècle de naissance et le dernier chiffre correspond au sexe de l’individu (impair pour les hommes et les femmes)
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_denmark_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_denmark_eu_tax_file_number` from est trouvé. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_denmark_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
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

### <a name="keywords"></a>Mots clés

#### <a name="keywordsdenmarkeutaxfilenumber"></a>Keywords_denmark_eu_tax_file_number

Numéro de taxe
  
codes
  
id fiscal
  
numéro CPR
  
cardio
  
skat nummer
  
ID Skat
  
## <a name="estonia"></a>Estonie

### <a name="format"></a>Format

11 chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

11 chiffres :
  
-  Un chiffre correspondant au sexe et au siècle de naissance, où un nombre impair indique le mâle et le nombre pair, la femme comme suit: 1,2 pour le 19 siècle; 3, 4 pour le vingtième siècle; et 5, 6 pour le 21ème siècle 
    
- Six chiffres correspondant à la date de naissance (AAMMJJ)
    
- Trois chiffres correspondant à un numéro de série séparant les personnes nés à la même date
    
- Un chiffre de contrôle
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_estonia_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_estonia_eu_tax_file_number` from est trouvé. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_estonia_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
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

### <a name="keywords"></a>Mots clés

#### <a name="keywordsestoniaeutaxfilenumber"></a>Keywords_estonia_eu_tax_file_number

Numéro de taxe
  
codes
  
id fiscal
  
code personnel
  
maksunumber
  
ID maksu
  
isikukood
  
## <a name="finland"></a>Finlande

### <a name="format"></a>Format

Combinaison de 11 caractères chiffres, lettres, et signe plus et moins
  
### <a name="pattern"></a>Modèle

Combinaison de 11 caractères chiffres, lettres, et signe plus et moins:
  
- Six chiffres
    
- L’une des options suivantes: un signe plus, un signe moins ou la lettre «A» (ne respectant pas la casse), où le signe plus est né entre 1800-1899, le signe moins est né entre 1900-1999, et «A» désigne né 2000 et after
    
- Trois chiffres
    
- Une lettre ou un chiffre
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_finland_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_finland_eu_tax_file_number` from est trouvé. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_finland_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
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

### <a name="keywords"></a>Mots clés

#### <a name="keywordsfinlandeutaxfilenumber"></a>Keywords_finland_eu_tax_file_number

numéro d’identification
  
ID personnel
  
Numéro d’identité
  
Numéro d’identification national finnois
  
personalidnumber#
  
numéro d’identification nationale
  
Numéro d’identification
  
Numéro d’identification nationale
  
Numéro d’identification national
  
n ° ID
  
tunnistenumero
  
henkilötunnus
  
yksilöllinen henkilökohtainen tunnistenumero
  
ainutlaatuinen henkilökohtainen tunnus
  
identiteetti numérique
  
suomen kansallinen henkilötunnus
  
henkilötunnusnumero#
  
kansallisen tunnistenumero
  
tunnusnumero
  
Kansallinen tunnus numérique
  
## <a name="france"></a>France

### <a name="format"></a>Format

13 chiffres pour les personnes et neuf chiffres pour les entités
  
### <a name="pattern"></a>Modèle

13 chiffres pour les personnes:
  
- Un chiffre qui doit être 0, 1, 2 ou 3
    
- 12 chiffres
    
Neuf chiffres pour les entités
  
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_france_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_france_eu_tax_file_number` from est trouvé. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_france_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
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

### <a name="keywords"></a>Mots clés

#### <a name="keywordsfranceeutaxfilenumber"></a>Keywords_france_eu_tax_file_number

Numéro d’identification de taxe
  
Numéro de taxe
  
id fiscal
  
Numéro d’identification fiscale
  
## <a name="germany"></a>Allemagne

### <a name="format"></a>Format

11 chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

11 chiffres:
  
-  Dix chiffres 
    
- Un chiffre de contrôle
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_germany_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_germany_eu_tax_file_number` from est trouvé. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_germany_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
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

### <a name="keywords"></a>Mots clés

#### <a name="keywordsgermanyeutaxfilenumber"></a>Keywords_germany_eu_tax_file_number

Numéro de taxe
  
n ° taxe
  
taxno#
  
taxnumber#
  
taxnumber
  
id fiscal
  
n ° de taxi
  
Numéro d’identification de taxe
  
n ° d’identification fiscale
  
steuernummer
  
ID Steuer
  
steueridentifikationsnummer
  
## <a name="greece"></a>Grèce

### <a name="format"></a>Format

Neuf chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

Neuf chiffres
  
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression `Regex_greece_eu_tax_file_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_greece_eu_tax_file_number` from est trouvé. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_tax_file_number" />
          <Match idRef="Keywords_greece_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordsgreeceeutaxfilenumber"></a>Keywords_greece_eu_tax_file_number

financement
  
Etain
  
n ° ID taxe
  
n ° de taxe
  
Numéro d’identification de taxe
  
Numéro de registre des taxes
  
n ° de Registre taxe
  
financement
  
Etain
  
taxidno#
  
taxregistryno#
  
αριθμός φορολογικού μητρώου
  
aφμ
  
aφμ αριθμός
  
φορολογικού μητρώου νο.
  
τον αριθμό φορολογικού μητρώου
  
## <a name="hungary"></a>Hongrie

### <a name="format"></a>Format

Dix chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

Dix chiffres:
  
-  Un chiffre qui doit être «8» 
    
- Cinq chiffres correspondant au nombre de jours entre la date 01/01/1867 et la date de naissance de la personne
    
- Trois chiffres correspondant au nombre généré par l’opportunité pour différencier les individus nés le même jour
    
- Un chiffre de contrôle
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_hungary_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_hungary_eu_tax_file_number` from est trouvé. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_hungary_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
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

### <a name="keywords"></a>Mots clés

#### <a name="keywordshungaryeutaxfilenumber"></a>Keywords_hungary_eu_tax_file_number

Numéro d’identification de taxe hongrois
  
étain hongrois
  
Numéro d’identification de taxe
  
Numéro de TVA
  
Numéro de l’autorité fiscale
  
Numéro d’identité fiscale de l’ID taxe
  
taxidnumber#
  
Etain
  
hungatiantin#
  
n ° d’identification fiscale
  
taxidno#
  
adóazonosító szám
  
adószám
  
adóhatóság szám
  
## <a name="ireland"></a>Irlande

### <a name="format"></a>Format

Sept chiffres suivis d’une lettre sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

Sept chiffres suivis d’une lettre:
  
-  Sept chiffres  
    
- Une lettre (ne respecte pas la casse)
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_ireland_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_ireland_eu_tax_file_number` from est trouvé. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_ireland_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
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

### <a name="keywords"></a>Mots clés

#### <a name="keywordsirelandeutaxfilenumber"></a>Keywords_ireland_eu_tax_file_number

Numéro de service public
  
service public personnel
  
n ° PPS
  
Numéro de service personnel
  
n ° de Service PPS
  
ppsno#
  
n ° PPS irlandais
  
publicserviceno#
  
Numéro de service public
  
uimhir phearsanta seirbhíse poiblí
  
PPS uimh
  
uimhir aitheantais phearsanta
  
## <a name="italy"></a>Italie

### <a name="format"></a>Format

16 lettres et chiffres dans le modèle spécifié
  
### <a name="pattern"></a>Modèle

16 lettres et chiffres:
  
-  Trois lettres qui correspondent aux trois premières consonnes du nom de la famille 
    
- Trois lettres qui correspondent à la première, troisième et quatrième consonnes du prénom
    
- Deux chiffres correspondant aux derniers chiffres de l’année de naissance
    
- Un chiffre correspondant au mois de naissance: les lettres sont utilisées par ordre alphabétique, mais seules les lettres de A à E, H, L, M, P, R à T sont utilisées (en janvier, A et octobre est R).
    
- Deux chiffres correspondant au jour du mois de naissance où 40 est ajouté au jour de naissance pour que les femmes différencient les hommes
    
- Quatre chiffres correspondant à un indicatif régional spécifique à la municipalité où la personne est né — des codes nationaux sont utilisés pour les pays étrangers
    
- Un chiffre de contrôle
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_italy_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_italy_eu_tax_file_number` from est trouvé. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_italy_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
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

### <a name="keywords"></a>Mots clés

#### <a name="keywordsitalyeutaxfilenumber"></a>Keywords_italy_eu_tax_file_number

Numéro de taxe
  
n ° taxe
  
taxno#
  
taxnumber#
  
taxnumber
  
id fiscal
  
n ° de taxi
  
code fiscal
  
Codice fiscale
  
## <a name="latvia"></a>Lettonie

### <a name="format"></a>Format

11 chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

11 chiffres dans le modèle spécifié
  
-  Six chiffres correspondant à la date de naissance (JJMMAA) 
    
- Un chiffre correspondant au siècle de naissance où «0» correspond à 19 siècle, «1» correspond au vingtième siècle et «2» au 21ème siècle.
    
- Quatre chiffres
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_latvia_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_latvia_eu_tax_file_number` from est trouvé. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_latvia_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
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

### <a name="keywords"></a>Mots clés

#### <a name="keywordslatviaeutaxfilenumber"></a>Keywords_latvia_eu_tax_file_number

Numéro de taxe
  
n ° taxe
  
taxno#
  
taxnumber#
  
taxnumber
  
id fiscal
  
n ° de taxi
  
Numéro d’identification de taxe
  
n ° d’identification fiscale
  
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
  
- La fonction `Func_lithuania_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_lithuania_eu_tax_file_number` from est trouvé. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_lithuania_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
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

### <a name="keywords"></a>Mots clés

#### <a name="keywordslithuaniaeutaxfilenumber"></a>Keywords_lithuania_eu_tax_file_number

Numéro de taxe
  
n ° taxe
  
n ° de taxe n °
  
taxnumber#
  
taxnumber
  
id fiscal
  
n ° de taxi
  
Numéro d’identification de taxe
  
n ° d’identification fiscale
  
ID mokesčių
  
mokesčių chiffres
  
mokesčių identifikavimas
  
## <a name="luxemburg"></a>Relatif

### <a name="format"></a>Format

13 chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

13 chiffres :
  
-  11 chiffres 
    
- Deux chiffres de contrôle
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_luxemburg_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_luxemburg_eu_tax_file_number` from est trouvé. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_luxemburg_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
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

### <a name="keywords"></a>Mots clés

#### <a name="keywordsluxemburgeutaxfilenumber"></a>Keywords_luxemburg_eu_tax_file_number

Numéro de taxe
  
n ° taxe
  
taxno#
  
taxnumber#
  
taxnumber
  
id fiscal
  
n ° de taxi
  
Numéro d’identification de taxe
  
n ° d’identification fiscale
  
steuernummer
  
ID Steuer
  
steueridentifikationsnummer
  
## <a name="malta"></a>Malte

### <a name="format"></a>Format

Pour les ressortissants maltais: 7 chiffres et une lettre dans le modèle spécifié
  
Ressortissants non maltaises et entités maltaises: 9 chiffres
  
### <a name="pattern"></a>Modèle

Ressortissants maltaises: 7 chiffres et une lettre
  
-  Sept chiffres  
    
- Une lettre (ne respecte pas la casse)
    
Ressortissants non maltaises et entités maltaises: 9 chiffres
  
-  Neuf chiffres 
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_malta_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_malta_eu_tax_file_number` from est trouvé. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_malta_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
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

### <a name="keywords"></a>Mots clés

#### <a name="keywordsmaltaeutaxfilenumber"></a>Keywords_malta_eu_tax_file_number

Numéro de taxe
  
n ° taxe
  
taxno#
  
taxnumber#
  
taxnumber
  
id fiscal
  
n ° de taxi
  
Numéro d’identification de taxe
  
n ° d’identification fiscale
  
numru tat-Taxxa
  
ID tat-Taxxa
  
numru ta’IDENTIFIKAZZJONI tat-Taxxa
  
## <a name="netherlands"></a>Pays-Bas

### <a name="format"></a>Format

Neuf chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

Neuf chiffres 
  
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_netherlands_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_netherlands_eu_tax_file_number` from est trouvé. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_netherlands_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
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

### <a name="keywords"></a>Mots clés

#### <a name="keywordsnetherlandseutaxfilenumber"></a>Keywords_netherlands_eu_tax_file_number

Numéro d’identification fiscale néerlandaise
  
identification fiscale néerlandaise
  
Numéro d’identification de taxe de Netherland
  
identification fiscale de Netherland
  
Numéro d’identification de taxe
  
ID de taxe néerlandaise
  
Numéro d’identification de taxe néerlandaise
  
id fiscal
  
n ° de taxe
  
Numéro de taxe
  
n ° de taxe n °
  
codes
  
Etain
  
Etain
  
étain (Pays-Bas)
  
Netherland d’étain
  
néerlandais qui a identificatienummer
  
identificatienummer van à l’avant-dernière
  
identificatienummer qui a été modifié
  
néerlandais qui a identificatie
  
néerlandais qui a pour ID Nummer
  
Néerlandais belastingnummer
  
btw nummer
  
Nederlandse qui a identificatie
  
## <a name="poland"></a>Pologne

### <a name="format"></a>Format

Onze chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

Onze chiffres
  
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_poland_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_poland_eu_tax_file_number` from est trouvé. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_poland_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
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

### <a name="keywords"></a>Mots clés

#### <a name="keywordspolandeutaxfilenumber"></a>Keywords_poland_eu_tax_file_number

Numéro de taxe
  
n ° taxe
  
taxno#
  
taxnumber#
  
taxnumber
  
pince
  
pince
  
id fiscal
  
n ° de taxe
  
ID du NIP
  
n ° de NIP
  
Numéro d’identification de taxe
  
n ° d’identification fiscale
  
Numéro de TVA
  
n ° TVA
  
vatno#
  
Numéro de TVA
  
n ° de TVA
  
chiffre identyfikacji podatkowej
  
Polski identyfikacji podatkowej
  
numeridentyfikacjipodatkowej#
  
## <a name="portugal"></a>Portugal

### <a name="format"></a>Format

Neuf chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

Neuf chiffres
  
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_portugal_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_portugal_eu_tax_file_number` from est trouvé. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_portugal_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
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

### <a name="keywords"></a>Mots clés

#### <a name="keywordsportugaleutaxfilenumber"></a>Keywords_portugal_eu_tax_file_number

Numéro de taxe
  
n ° taxe
  
taxno#
  
taxnumber#
  
taxnumber
  
nPour
  
nPour
  
chiffres fiscaux
  
Número de identificação fiscal
  
## <a name="romania"></a>Roumanie

### <a name="format"></a>Format

13 chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

13 chiffres
  
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression `Regex_romania_eu_tax_file_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_romania_eu_tax_file_number` from est trouvé. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_tax_file_number" />
          <Match idRef="Keywords_romania_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordsromaniaeutaxfilenumber"></a>Keywords_romania_eu_tax_file_number

id fiscal
  
Numéro d’identification de taxe
  
n ° fichier taxe
  
numéro de dossier fiscal
  
n ° taxe
  
Numéro de taxe
  
n ° de taxi
  
taxno#
  
ID-UL taxei
  
numărul de IDENTIFICARE fiscală
  
## <a name="slovakia"></a>République de Slovaquie

### <a name="format"></a>Format

10 chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

10 chiffres
  
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression `Regex_slovakia_eu_tax_file_number` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_slovakia_eu_tax_file_number` from est trouvé. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_tax_file_number" />
          <Match idRef="Keywords_slovakia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordsslovakiaeutaxfilenumber"></a>Keywords_slovakia_eu_tax_file_number

id fiscal
  
Numéro d’identification de taxe
  
ID d’étain
  
n ° d’étain
  
ID d’étain slovaque
  
Etain
  
n ° fichier taxe
  
numéro de dossier fiscal
  
n ° taxe
  
Numéro de taxe
  
n ° de taxi
  
taxno#
  
daňové identifikačné číslo
  
daňové číslo
  
daňové číslo súboru
  
## <a name="slovenia"></a>Slovénie

### <a name="format"></a>Format

Huit chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

Huit chiffres
  
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_slovenia_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_slovenia_eu_tax_file_number` from est trouvé. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_slovenia_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
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

### <a name="keywords"></a>Mots clés

#### <a name="keywordssloveniaeutaxfilenumber"></a>Keywords_slovenia_eu_tax_file_number

id fiscal
  
Numéro d’identification de taxe
  
ID d’étain
  
n ° d’étain
  
ID d’étain slovène
  
Etain
  
n ° fichier taxe
  
numéro de dossier fiscal
  
n ° taxe
  
Numéro de taxe
  
n ° de taxi
  
taxno#
  
identifikacijska številka davka
  
davčna številka
  
številka davčne datoteke
  
## <a name="spain"></a>Espagne

### <a name="format"></a>Format

Sept ou huit chiffres et une ou deux lettres dans le modèle spécifié
  
### <a name="pattern"></a>Modèle

Personnes physiques espagnoles avec une carte d’identité nationale d’Espagne:
  
-  Huit chiffres 
    
- Une lettre majuscule (respecte la casse) 
    
Spaniards non résident sans carte d’identité nationale d’Espagne
  
- Une lettre majuscule «L» (respecte la casse)
    
- Sept chiffres 
    
- Une lettre majuscule (respecte la casse) 
    
Spaniards résident de moins de 14 ans sans carte d’identité nationale (Espagne):
  
- Une lettre majuscule «K» (respecte la casse)
    
-  Sept chiffres  
    
- Une lettre majuscule (respecte la casse)
    
Foreigners avec le numéro d’identification d’un étranger
  
- Une lettre majuscule qui est «X», «Y» ou «Z» (respecte la casse) 
    
- Sept chiffres 
    
- Une lettre majuscule (respecte la casse) 
    
Foreigners sans numéro d’identification étranger
  
- Une lettre majuscule qui est «M» (respecte la casse) 
    
- Sept chiffres 
    
- Une lettre majuscule (respecte la casse) 
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_spain_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_spain_eu_tax_file_number` from est trouvé. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_spain_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
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

### <a name="keywords"></a>Mots clés

#### <a name="keywordsspaineutaxfilenumber"></a>Keywords_spain_eu_tax_file_number

id fiscal
  
Numéro d’identification de taxe
  
identifiant CAF
  
CAF non
  
ID CAF espagnol
  
importation
  
n ° fichier taxe
  
numéro CAF espagnol
  
numéro de dossier fiscal
  
espagnol (CAF)
  
n ° taxe
  
Numéro de taxe
  
n ° de taxi
  
taxno#
  
cifid#
  
spanishcifid#
  
spanishcifno#
  
Número de contribuyente
  
Número de Impuesto Corporativo
  
Número de Identificación fiscal
  
CIF número
  
cifnúmero#
  
## <a name="sweden"></a>Suède

### <a name="format"></a>Format

Dix chiffres et un symbole dans le modèle spécifié
  
### <a name="pattern"></a>Modèle

Dix chiffres et un symbole:
  
-  Six chiffres correspondant à la date de naissance (AAMMJJ) 
    
- Un signe plus, un signe moins ou une barre oblique inverse
    
- Trois chiffres qui permettent de définir le numéro d’identification unique: 
    
  - Pour les numéros émis avant le 1990, le septième et le huitième chiffre identifient le comté de naissance ou les personnes nées à l’étranger.
    
  - Le chiffre de la neuvième position indique le sexe soit impair, soit pair pour femme.
    
- Un chiffre de contrôle
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_sweden_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_sweden_eu_tax_file_number` from est trouvé. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_sweden_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
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

### <a name="keywords"></a>Mots clés

#### <a name="keywordsswedeneutaxfilenumber"></a>Keywords_sweden_eu_tax_file_number

id fiscal
  
n ° ID taxe
  
Numéro d’identification de taxe
  
identification fiscale
  
n ° d’identification fiscale
  
n ° taxe
  
codes
  
n ° de taxi
  
fichier taxe
  
n ° fichier taxe
  
Numéro d’identification personnel
  
skatt ID Nummer
  
skatt identifikation
  
personnummer
  
## <a name="uk"></a>R.U.

### <a name="format"></a>Format

Référence de contribuable unique (UTR): 10 chiffres sans espaces ni délimiteurs
  
Numéro d’assurance nationale (NINO): pour plus d’informations, reportez-vous à la section «Royaume-Uni National Insurance Number (NINO)» dans [ce que recherche les types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
  
### <a name="pattern"></a>Modèle

Référence de contribuable unique (UTR): 10 chiffres
  
Numéro d’assurance nationale (NINO): pour plus d’informations, reportez-vous à la section «Royaume-Uni National Insurance Number (NINO)» dans [ce que recherche les types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
  
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_uk_eu_tax_file_number` trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_uk_eu_tax_file_number` from est trouvé. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_uk_eu_tax_file_number" />
          <Match idRef="Keywords_uk_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordsukeutaxfilenumber"></a>Keywords_uk_eu_tax_file_number

id fiscal
  
n ° ID taxe
  
Numéro d’identification de taxe
  
identification fiscale
  
n ° d’identification fiscale
  
n ° taxe
  
codes
  
n ° de taxi
  
fichier taxe
  
n ° fichier taxe
  
## <a name="see-also"></a>Voir aussi

[Éléments recherchés par les types d’informations sensibles](what-the-sensitive-information-types-look-for.md)

