---
title: ID de numéro de sécurité sociale de l’Union européenne ou équivalent
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 1fabd341-e594-4bfe-961c-62aa82893f60
description: Cette rubrique illustre une stratégie de protection contre la perte données lorsqu’il détecte le type d’informations sensibles numéro de sécurité sociale de l’Union européenne ou ID équivalente. Ce type d’informations sensibles définit différents motifs, mots clés et autres pour chaque pays.
ms.openlocfilehash: 6f1027dcfb648ed937b8180d74d4bc6348dab650
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527983"
---
# <a name="eu-social-security-number-or-equivalent-id"></a>ID de numéro de sécurité sociale de l’Union européenne ou équivalent

Cette rubrique illustre une stratégie de protection contre la perte données lorsqu’il détecte le type d’informations sensibles UE numéro de sécurité sociale (SSN) ou ID équivalente. Ce type d’informations sensibles définit différents motifs, mots clés et autres pour chaque pays.
  
## <a name="austria"></a>Autriche

### <a name="format"></a>Format

10 chiffres dans le format spécifié
  
### <a name="pattern"></a>Modèle

10 chiffres :
  
-  Trois chiffres qui correspondent à un numéro de série 
    
- Chiffre un contrôle
    
- Six chiffres qui correspondent à la date de naissance (jjmmaa)
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_austria_eu_ssn_or_equivalent` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_austria_eu_ssn_or_equivalent` est trouvée. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_austria_eu_ssn_or_equivalent` recherche de contenu qui correspond au modèle. 
    
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

### <a name="keywords"></a>Keywords

#### <a name="keywordsaustriaeussnorequivalent"></a>Keywords_austria_eu_ssn_or_equivalent

sécurité sociale aucune
  
numéro de sécurité sociale

  

code de sécurité sociale
  
numéro d’assurance
  
Schilling ssn
  
ssn #
  
ssn
  
code d’assurance
  
code d’assurance #
  
socialsecurityno #
  
sozialversicherungsnummer
  
soziale sicherheit kein
  
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
  
- La fonction `Func_belgium_eu_ssn_or_equivalent` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_belgium_eu_ssn_or_equivalent` est trouvée. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_belgium_eu_ssn_or_equivalent` recherche de contenu qui correspond au modèle. 
    
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

### <a name="keywords"></a>Keywords

#### <a name="keywordsbelgiumeussnorequivalent"></a>Keywords_belgium_eu_ssn_or_equivalent

numéro national belge
  
numéro national
  
numéro de sécurité sociale

  
nationalnumber #
  
ssn #
  
ssn
  
nationalnumber
  
bnn #
  
bnn
  
numéro d’identification personnelle
  
personalidnumber #
  
numéro national
  
numéro de sécurité

  
numéro d'assuré
  
Identifiant national
  
identifiantnational #
  
numéronational #
  
## <a name="croatia"></a>Croatie

### <a name="format"></a>Format

11 chiffres sans espaces et les séparateurs
  
### <a name="pattern"></a>Modèle

 11 chiffres : 
  
-  Dix chiffres 
    
- Chiffre un contrôle
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_croatia_eu_ssn_or_equivalent` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_croatia_eu_ssn_or_equivalent` est trouvée. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_croatia_eu_ssn_or_equivalent` recherche de contenu qui correspond au modèle. 
    
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

### <a name="keywords"></a>Keywords

#### <a name="keywordscroatiaeussnorequivalent"></a>Keywords_croatia_eu_ssn_or_equivalent

numéro d’identification personnel
  
nombre de maîtres citoyens
  
numéro d’identification nationale
  
numéro de sécurité sociale

  
nationalnumber #
  
ssn #
  
ssn
  
nationalnumber
  
bnn #
  
bnn
  
numéro d’identification personnelle
  
personalidnumber #
  
oib
  
osobni identifikacijski broj
  
## <a name="czech-republic"></a>République tchèque

### <a name="format"></a>Format

Dix chiffres et une barre oblique inverse dans le modèle spécifié
  
### <a name="pattern"></a>Modèle

Dix chiffres et une barre oblique inverse :
  
- Six chiffres qui correspondent à la date de naissance (AAMMJJ) : 
    
- Une barre oblique inverse
    
- Trois chiffres qui correspondent à un numéro de série qui sépare les personnes naissance à la même date
    
- Chiffre un contrôle
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_czech_republic_eu_ssn_or_equivalent` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_czech_republic_eu_ssn_or_equivalent` est trouvée. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_czech_republic_eu_ssn_or_equivalent` recherche de contenu qui correspond au modèle. 
    
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

### <a name="keywords"></a>Keywords

#### <a name="keywordsczechrepubliceussnorequivalent"></a>Keywords_czech_republic_eu_ssn_or_equivalent

nombre de naissance
  
numéro d’identification nationale
  
numéro d’identification personnel
  
numéro de sécurité sociale

  
nationalnumber #
  
ssn #
  
ssn
  
numéro national
  
numéro d’identification personnelle
  
personalidnumber #
  
rč
  
rodné číslo
  
rodne cislo
  
## <a name="denmark"></a>Danemark

### <a name="format"></a>Format

Dix chiffres et un trait d’union dans le modèle spécifié
  
### <a name="pattern"></a>Modèle

Dix chiffres et un trait d’union :
  
- Six chiffres qui correspondent à la date de naissance (jjmmaa) 
    
- Un trait d’union 
    
- Quatre chiffres qui correspondent à un numéro de séquence
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_denmark_eu_ssn_or_equivalent` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_denmark_eu_ssn_or_equivalent` est trouvée. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_denmark_eu_ssn_or_equivalent` recherche de contenu qui correspond au modèle. 
    
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

### <a name="keywords"></a>Keywords

#### <a name="keywordsdenmarkeussnorequivalent"></a>Keywords_denmark_eu_ssn_or_equivalent

numéro d’identification personnel
  
numéro d’identification nationale
  
numéro de sécurité sociale

  
nationalnumber #
  
ssn #
  
ssn
  
numéro national
  
numéro d’identification personnelle
  
personalidnumber #
  
CPR-nummer
  
personnummer
  
## <a name="finland"></a>Finlande

### <a name="format"></a>Format

Une combinaison de 11 caractères au format spécifié
  
### <a name="pattern"></a>Modèle

Une combinaison de 11 caractères au format spécifié :
  
-  Six chiffres 
    
- Une seule instance d’une des opérations suivantes :
    
  - Plus de symbole
    
  - Moins de symbole
    
  - La lettre « A » (pas la casse)
    
- Trois chiffres
    
- Une lettre ou un chiffre
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_finland_eu_ssn_or_equivalent` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_finland_eu_ssn_or_equivalent` est trouvée. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_finland_eu_ssn_or_equivalent` recherche de contenu qui correspond au modèle. 
    
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

### <a name="keywords"></a>Keywords

#### <a name="keywordsfinlandeussnorequivalent"></a>Keywords_finland_eu_ssn_or_equivalent

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
  
hetu
  
## <a name="france"></a>France

Pour plus d’informations, consultez la section « France numéro de sécurité sociale (INSEE) » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="germany"></a>Allemagne

Pour plus d’informations, consultez la section « Numéro de carte d’identité Allemagne » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="greece"></a>Grèce

Pour plus d’informations, consultez la section « Grèce carte » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="hungary"></a>Hongrie

### <a name="format"></a>Format

Neuf chiffres sans espaces et les séparateurs
  
### <a name="pattern"></a>Modèle

Neuf chiffres
  
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_hungary_eu_ssn_or_equivalent` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_hungary_eu_ssn_or_equivalent` est trouvée. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_hungary_eu_ssn_or_equivalent` recherche de contenu qui correspond au modèle. 
    
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

### <a name="keywords"></a>Keywords

#### <a name="keywordshungaryeussnorequivalent"></a>Keywords_hungary_eu_ssn_or_equivalent

numéro de sécurité sociale hongrois
  
numéro de sécurité sociale

  
socialsecuritynumber #
  
hssn #
  
socialsecuritynno
  
hssn
  
TAJ
  
TAJ #
  
ssn
  
ssn #
  
sécurité sociale aucune
  
áfa
  
közösségi adószám
  
általános forgalmi adó szám
  
hozzáadottérték adó
  
áfa szám
  
áfa magyar szám
  
## <a name="portugal"></a>Portugal

Pour plus d’informations, consultez la section « Portugal citoyens carte numéro » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="spain"></a>Espagne

Pour plus d’informations, consultez la section « Espagne numéro de sécurité sociale (SSN) » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="sweden"></a>Suède

### <a name="format"></a>Format

12 chiffres sans espaces et les séparateurs
  
### <a name="pattern"></a>Modèle

12 chiffres :
  
-  Huit chiffres qui correspondent à la date de naissance (AAAAMMJJ) 
    
- Trois chiffres qui correspondent à un numéro de série où : 
    
  - Le dernier chiffre du numéro de série indique le sexe par l’affectation d’un nombre impair de masculin et un nombre pair pour femme
    
  - Jusqu'à 1990, l’affectation de numéro de série correspondant à la région où le support du nombre de naissance ou (si naissance avant 1947) où il avait été courantes, en fonction des enregistrements de taxe sur 1 janvier 1947, avec un code spécial (généralement 9 en tant que le chiffre 7) pour immigrants 
    
- Chiffre un contrôle
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_sweden_eu_ssn_or_equivalent` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_sweden_eu_ssn_or_equivalent` est trouvée. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_sweden_eu_ssn_or_equivalent` recherche de contenu qui correspond au modèle. 
    
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

### <a name="keywords"></a>Keywords

#### <a name="keywordsswedeneussnorequivalent"></a>Keywords_sweden_eu_ssn_or_equivalent

numéro d’identification personnelle
  
numéro d’identification

  
identifiant personnel aucune
  
identité aucune
  
identification aucune
  
identification personnel aucune
  
id personnummer
  
id de personligt-nummer
  
id d’unikt-nummer
  
personnummer
  
identifikationsnumret
  
personnummer #
  
identifikationsnumret #
  
## <a name="see-also"></a>Voir aussi

[Éléments recherchés par les types d’informations sensibles](what-the-sensitive-information-types-look-for.md)

