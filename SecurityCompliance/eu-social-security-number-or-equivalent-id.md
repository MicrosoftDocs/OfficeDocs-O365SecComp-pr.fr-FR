---
title: Numéro de sécurité sociale de l'UE ou ID équivalent
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: Cette rubrique indique ce qu'est une stratégie de protection contre la perte de données (DLP) lorsqu'elle détecte le type d'informations sensibles de l'UE ou d'un ID équivalent. Ce type d'informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.
ms.openlocfilehash: c0c808eafa52209c79f3b4e8a2113f587fd8a771
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32255552"
---
# <a name="eu-social-security-number-or-equivalent-id"></a>Numéro de sécurité sociale de l'UE ou ID équivalent

Cette rubrique présente ce qu'une stratégie de protection contre la perte de données (DLP) recherche lorsqu'elle détecte le type d'informations sensibles de l'UE ou un ID équivalent. Ce type d'informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.
  
## <a name="austria"></a>Autriche

### <a name="format"></a>Format

10 chiffres au format spécifié
  
### <a name="pattern"></a>Modèle

10 chiffres :
  
-  Trois chiffres correspondant à un numéro de série 
    
- Un chiffre de contrôle
    
- Six chiffres correspondant à la date de naissance (JJMMAA)
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_austria_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_austria_eu_ssn_or_equivalent` from est trouvé. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_austria_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle. 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_austria_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_austria_eu_ssn_or_equivalent" />
        </Pattern>
<Pattern confidenceLevel="75">
            <IdMatch idRef="Func_austria_eu_ssn_or_equivalent" />
          </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordsaustriaeussnorequivalent"></a>Keywords_austria_eu_ssn_or_equivalent

Numéro de sécurité sociale
  
numéro de sécurité sociale
  
code de sécurité sociale
  
Numéro d'assurance
  
Numéro de sécurité sociale autrichien
  
SSN
  
SSN
  
code d'assurance
  
n ° de code d'assurance
  
socialsecurityno #
  
sozialversicherungsnummer
  
soziale Sicherheit kein
  
versicherungsnummer
  
## <a name="belgium"></a>Belgique

### <a name="format"></a>Format

11 chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

11 chiffres
  
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_belgium_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_belgium_eu_ssn_or_equivalent` from est trouvé. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_belgium_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle. 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_belgium_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_belgium_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_belgium_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordsbelgiumeussnorequivalent"></a>Keywords_belgium_eu_ssn_or_equivalent

numéro national belge
  
numéro national
  
numéro de sécurité sociale
  
nationalnumber #
  
SSN
  
SSN
  
nationalnumber
  
BNN #
  
BNN
  
Numéro d'identification personnel
  
personalidnumber #
  
numéro national
  
numéro de sécurité
  
numéro d'assuré
  
identifiant national
  
identifiantnational #
  
numéronational #
  
## <a name="croatia"></a>Croatie

### <a name="format"></a>Format

11 chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

 11 chiffres : 
  
-  Dix chiffres 
    
- Un chiffre de contrôle
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_croatia_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_croatia_eu_ssn_or_equivalent` from est trouvé. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_croatia_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle. 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_croatia_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_croatia_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_croatia_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordscroatiaeussnorequivalent"></a>Keywords_croatia_eu_ssn_or_equivalent

Numéro d'identification personnel
  
Numéro de citoyen principal
  
numéro d’identification nationale
  
numéro de sécurité sociale
  
nationalnumber #
  
SSN
  
SSN
  
nationalnumber
  
BNN #
  
BNN
  
Numéro d'identification personnel
  
personalidnumber #
  
OIB
  
osobni identifikacijski Broj
  
## <a name="czech-republic"></a>République tchèque

### <a name="format"></a>Format

10 chiffres et une barre oblique inverse dans le modèle spécifié
  
### <a name="pattern"></a>Modèle

Dix chiffres et une barre oblique inverse:
  
- Six chiffres correspondant à la date de naissance (AAMMJJ): 
    
- Une barre oblique inverse
    
- Trois chiffres correspondant à un numéro de série qui sépare les personnes nés à la même date
    
- Un chiffre de contrôle
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_czech_republic_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_czech_republic_eu_ssn_or_equivalent` from est trouvé. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_czech_republic_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle. 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_czech_republic_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_czech_republic_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_czech_republic_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordsczechrepubliceussnorequivalent"></a>Keywords_czech_republic_eu_ssn_or_equivalent

Numéro de naissance
  
numéro d’identification nationale
  
Numéro d'identification personnel
  
numéro de sécurité sociale
  
nationalnumber #
  
SSN
  
SSN
  
numéro national
  
Numéro d'identification personnel
  
personalidnumber #
  
rč
  
rodné číslo
  
Rodne Cislo
  
## <a name="denmark"></a>Danemark

### <a name="format"></a>Format

10 chiffres et un trait d'Union dans le modèle spécifié
  
### <a name="pattern"></a>Modèle

Dix chiffres et un trait d'Union:
  
- Six chiffres correspondant à la date de naissance (JJMMAA) 
    
- Un trait d’union 
    
- Quatre chiffres correspondant à un numéro de séquence
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_denmark_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_denmark_eu_ssn_or_equivalent` from est trouvé. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_denmark_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle. 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_denmark_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_denmark_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_denmark_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordsdenmarkeussnorequivalent"></a>Keywords_denmark_eu_ssn_or_equivalent

Numéro d'identification personnel
  
numéro d’identification nationale
  
numéro de sécurité sociale
  
nationalnumber #
  
SSN
  
SSN
  
numéro national
  
Numéro d'identification personnel
  
personalidnumber #
  
CPR-nummer
  
personnummer
  
## <a name="finland"></a>Finlande

### <a name="format"></a>Format

Combinaison de 11 caractères au format spécifié
  
### <a name="pattern"></a>Modèle

Combinaison de 11 caractères au format spécifié:
  
-  Six chiffres 
    
- Une instance de l'un des éléments suivants:
    
  - Symbole plus
    
  - Symbole moins
    
  - La lettre «A» (ne respecte pas la casse)
    
- Trois chiffres
    
- Une lettre ou un chiffre
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_finland_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_finland_eu_ssn_or_equivalent` from est trouvé. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_finland_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle. 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finland_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_finland_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_finland_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordsfinlandeussnorequivalent"></a>Keywords_finland_eu_ssn_or_equivalent

numéro d’identification
  
ID personnel
  
Numéro d'identité
  
Numéro d'identification national finnois
  
personalidnumber #
  
numéro d’identification nationale
  
Numéro d'identification
  
Numéro d'identification nationale
  
Numéro d'identification national
  
n ° ID
  
tunnistenumero
  
henkilötunnus
  
Yksilöllinen henkilökohtainen tunnistenumero
  
ainutlaatuinen henkilökohtainen tunnus
  
identiteetti numérique
  
Suomen Kansallinen henkilötunnus
  
henkilötunnusnumero #
  
Kansallisen tunnistenumero
  
tunnusnumero
  
Kansallinen tunnus numérique
  
Hetu
  
## <a name="france"></a>France

Pour plus d'informations, reportez-vous à la section «France-numéro de sécurité sociale (INSEE)» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="germany"></a>Allemagne

Pour plus d'informations, reportez-vous à la section «Germany Identity Card Number» dans les [types d'informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="greece"></a>Grèce

Pour plus d'informations, reportez-vous à la section «carte d'identité nationale Grèce» dans [ce que recherche les types d'informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="hungary"></a>Hongrie

### <a name="format"></a>Format

Neuf chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

Neuf chiffres
  
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_hungary_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_hungary_eu_ssn_or_equivalent` from est trouvé. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_hungary_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle. 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_hungary_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_hungary_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_hungary_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordshungaryeussnorequivalent"></a>Keywords_hungary_eu_ssn_or_equivalent

Numéro de sécurité sociale hongrois
  
numéro de sécurité sociale
  
socialsecuritynumber #
  
hssn #
  
socialsecuritynno
  
hssn
  
Taj
  
Taj #
  
SSN
  
SSN
  
Numéro de sécurité sociale
  
ÁFA
  
Közösségi adószám
  
Általános forgalmi adó szám
  
hozzáadottérték adó
  
ÁFA szám
  
Magyar ÁFA szám
  
## <a name="portugal"></a>Portugal

Pour plus d'informations, reportez-vous à la section «numéro de carte de citoyen Portugal» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="spain"></a>Espagne

Pour plus d'informations, reportez-vous à la section «numéro de sécurité sociale Espagne» dans les [types d'informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="sweden"></a>Suède

### <a name="format"></a>Format

12 chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

12 chiffres :
  
-  Huit chiffres correspondant à la date de naissance (AAAAMMJJ) 
    
- Trois chiffres correspondant à un numéro de série où: 
    
  - Le dernier chiffre du numéro de série indique sexe par l'affectation d'un nombre impair pour le mâle et d'un nombre pair pour femelle.
    
  - Jusqu'à 1990, l'affectation du numéro de série correspond au comté où le porteur du numéro est né ou (en naissance avant 1947) où il a été vivant, en fonction des enregistrements fiscaux, le 1er janvier 1947, avec un code spécial (généralement 9 comme le 7 chiffres) pour immigrants 
    
- Un chiffre de contrôle
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_sweden_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_sweden_eu_ssn_or_equivalent` from est trouvé. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_sweden_eu_ssn_or_equivalent` trouve le contenu qui correspond au modèle. 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_sweden_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_sweden_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_sweden_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordsswedeneussnorequivalent"></a>Keywords_sweden_eu_ssn_or_equivalent

Numéro d'identification personnel
  
numéro d’identification
  
Numéro d'identification personnel
  
n ° d'identité
  
Numéro d'identification
  
Numéro d'identification personnel
  
ID personnummer
  
ID personligt-Nummer
  
ID unikt-Nummer
  
personnummer
  
identifikationsnumret
  
personnummer #
  
identifikationsnumret #
  
## <a name="see-also"></a>Voir aussi

[Éléments recherchés par les types d’informations sensibles](what-the-sensitive-information-types-look-for.md)

