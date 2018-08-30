---
title: Numéro d’Identification nationales de l’UE
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 2ea971bf-9434-4b61-b825-2bbd28ae6064
description: Cette rubrique illustre une stratégie de protection contre la perte données lorsqu’il détecte le type d’informations sensibles numéro d’Identification de l’UE National. Ce type d’informations sensibles définit différents motifs, mots clés et autres pour chaque pays.
ms.openlocfilehash: 29d2126b937ff46039284a74eb2a84f2ebbacb41
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528043"
---
# <a name="eu-national-identification-number"></a>Numéro d’Identification nationales de l’UE

Cette rubrique illustre une stratégie de protection contre la perte données lorsqu’il détecte le type d’informations sensibles numéro d’Identification de l’UE National. Ce type d’informations sensibles définit différents motifs, mots clés et autres pour chaque pays.
  
## <a name="austria"></a>Autriche

### <a name="format"></a>Format

Une combinaison de caractères 24 des lettres, chiffres et caractères spéciaux
  
### <a name="pattern"></a>Modèle

24 caractères :
  
-  22 (pas la casse) lettres, chiffres, barres obliques inverses, barres obliques ou signes plus 
    
- (Pas la casse) de deux lettres, chiffres, barres obliques inverses, obliques, signes plus ou signe égal
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_austria_eu_national_id_card` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_austria_eu_national_id_card` est trouvée. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_national_id_card" />
          <Match idRef="Keywords_austria_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsaustriaeunationalidcard"></a>Keywords_austria_eu_national_id_card

numéro d’identification autrichien
  
numéro d’identité national
  
numéro d’identité
  

id national
  
personalausweis Slovaquie österreich
  
## <a name="belgium"></a>Belgique

Pour plus d’informations, voir la section « Numéro National Belgique » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="bulgaria"></a>Bulgarie

### <a name="format"></a>Format

Dix chiffres sans espaces et les séparateurs
  
### <a name="pattern"></a>Modèle

Dix chiffres sans espaces et les séparateurs
  
-  Six chiffres qui correspondent à la date de naissance (AAMMJJ) 
    
- Deux chiffres qui correspondent à l’ordre de naissance
    
- Un chiffre correspondant au sexe : un chiffre pair pour masculin et un chiffre impair pour femme
    
- Chiffre un contrôle
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_bulgaria_national_number` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_bulgaria_national_number` est trouvée. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_bulgaria_national_number` recherche de contenu qui correspond au modèle. 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_bulgaria_national_number" />
          <Match idRef="Keywords_bulgaria_national_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_bulgaria_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsbulgarianationalnumber"></a>Keywords_bulgaria_national_number

egn
  
egn #
  
bulgare numéro national
  
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
  
ЕДИНЕН ГРАЖДАНСКИ НОМЕР
  
edinen grazhdanski nomer
  
ЕГН
  
ЕГН #
  
## <a name="croatia"></a>Croatie

Pour plus d’informations, consultez la section « Croatie Identity Number » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="cyprus"></a>Chypre

### <a name="format"></a>Format

Dix chiffres sans espaces et les séparateurs
  
### <a name="pattern"></a>Modèle

 Dix chiffres 
  
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_cyprus_eu_national_id_card` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_cyprus_eu_national_id_card` est trouvée. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_national_id_card" />
          <Match idRef="Keywords_cyprus_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordscypruseunationalidcard"></a>Keywords_cyprus_eu_national_id_card

numéro de carte d’identité
  
numéro d’identification nationale
  
numéro d’identification personnelle
  
numéro de carte d’identité
  
ΤΑΥΤΟΤΗΤΑΣ
  
## <a name="czech-republic"></a>République tchèque

Pour plus d’informations, consultez la section « Numéro d’identité National tchèque » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="denmark"></a>Danemark

Pour plus d’informations, consultez la section « Numéro d’Identification personnelle Danemark » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="estonia"></a>Estonie

### <a name="format"></a>Format

11 chiffres sans espaces et les séparateurs
  
### <a name="pattern"></a>Modèle

11 chiffres :
  
- Un chiffre correspondant au sexe et century de naissance (masculin nombre impair, nombre pair féminin ; 1-2 : 19 century ; 3-4 : 20 century ; 5-6 : century 21)
    
- Six chiffres qui correspondent à la date de naissance (AAMMJJ)
    
- Trois chiffres qui correspondent à un numéro de série en séparant les personnes naissance à la même date
    
- Chiffre un contrôle
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_estonia_eu_national_id_card` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_estonia_eu_national_id_card` est trouvée. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_estonia_eu_national_id_card` recherche de contenu qui correspond au modèle. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_estonia_eu_national_id_card" />
          <Match idRef="Keywords_estonia_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_estonia_eu_national_id_card" />
</Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsestoniaeunationalidcard"></a>Keywords_estonia_eu_national_id_card

code d’identification personnelle
  
numéro d’identification personnel
  
numéro d’identification nationale
  
numéro national
  
numéro d’identification personnelle
  
personalidnumber #
  
IK
  
isikukood
  
ID-kaart
  
## <a name="finland"></a>Finlande

Pour plus d’informations, voir la section « ID National Finlande » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="france"></a>France

Pour plus d’informations, consultez la section « France National carte d’identité (CNI) » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="germany"></a>Allemagne

Pour plus d’informations, consultez la section « Numéro de carte d’identité Allemagne » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="greece"></a>Grèce

Pour plus d’informations, consultez la section « Grèce carte » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="hungary"></a>Hongrie

### <a name="format"></a>Format

11 chiffres
  
### <a name="pattern"></a>Modèle

11 chiffres :
  
-  Un chiffre correspondant au sexe (masculin-1, 2-femme, autres numéros sont également possibles pour les citoyens naissance 1900 ou aux citoyens citoyenneté double) 
    
- Six chiffres qui correspondent à la date de naissance (AAMMJJ)
    
- Trois chiffres qui correspondent à un numéro de série
    
- Chiffre un contrôle
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_hungary_eu_national_id_card` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_hungary_eu_national_id_card` est trouvée. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_hungary_eu_national_id_card` recherche de contenu qui correspond au modèle. 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_hungary_eu_national_id_card" />
          <Match idRef="Keywords_hungary_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_hungary_eu_national_id_card" />
</Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordshungaryeunationalidcard"></a>Keywords_hungary_eu_national_id_card

numéro d’identification personnel
  
numéro d’identification

  
numéro d’identification personnelle
  
személyazonosító igazolvány
  
## <a name="ireland"></a>Irlande

### <a name="format"></a>Format

Une combinaison de caractères neuf des lettres, chiffres et un espace dans le modèle spécifié
  
### <a name="pattern"></a>Modèle

Une combinaison de caractères neuf des lettres, chiffres et un espace dans le modèle spécifié
  
À partir du 01 janvier 2013 jusqu'à maintenant :
  
-  Sept chiffres  
    
- Chiffre un contrôle
    
- Un espace ou la lettre « W » (respecte la casse)
    
Avant de janvier 2013 01 :
  
-  Sept chiffres  
    
- Chiffre un contrôle
    
- Un espace ou une lettre majuscule (respecter la casse)
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction de recherche de contenu qui correspond au modèle.
    
- Un mot clé à partir d’est trouvé.
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction de recherche de contenu qui correspond au modèle.
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_ireland_eu_national_id_card" />
          <Match idRef="Keywords_ireland_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_ireland_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsirelandeunationalidcard"></a>Keywords_ireland_eu_national_id_card

numéro personnel service public
  
PPS aucune
  
numéro d’assurance sociale et de chiffre d’affaires
  
RSI aucune
  
numéro d’identification personnel
  
numéro d’identification

  
numéro d’identification personnelle
  
uimhir phearsanta seirbhíse poiblí
  
uimh. PSP
  
## <a name="italy"></a>Italie

### <a name="format"></a>Format

Une combinaison de 16 caractères de lettres et chiffres dans le modèle spécifié
  
### <a name="pattern"></a>Modèle

Une combinaison de 16 caractères de lettres et chiffres :
  
- Trois lettres qui correspondent aux trois premiers consonnes suivantes dans le nom de famille
    
- Trois lettres qui correspondent à la première, troisième et quatrième consonnes dans le premier nom
    
- Deux chiffres qui correspondent à la dernière chiffres de l’année de naissance
    
- Une lettre qui correspond à la lettre pour le mois de naissance — lettres sont utilisés dans l’ordre alphabétique, mais que les lettres A à E, H, L, M, P, R t sont utilisés (par conséquent, janvier correspond à un et octobre est R)
    
- Deux chiffres correspondant au jour du mois de naissance — afin de différencier sexe, 40 est ajouté à la journée de naissance pour femme
    
- Quatre chiffres qui correspond à l’indicatif régional spécifique à la commune où naissance de la personne (codes de pays échelle sont utilisés pour étranger)
    
- Un chiffre parité
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_italy_eu_national_id_card` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_italy_eu_national_id_card` est trouvée. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_italy_eu_national_id_card` recherche de contenu qui correspond au modèle. 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_italy_eu_national_id_card" />
          <Match idRef="Keywords_italy_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_italy_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsitalyeunationalidcard"></a>Keywords_italy_eu_national_id_card

code personnel
  
numéro de code personnel
  
nombre de certificats personnel
  
code fiscal
  
personalcodeno #
  
numéro d’identification personnelle
  
code d’identification personnelle
  
numéro d’identification personale
  
NUMERO certificato personale
  
NUMERO personale
  
NUMERO id personale
  
numéro d’identification id personale
  
numéro d’identification fiscale
  
## <a name="italy"></a>Italie

### <a name="format"></a>Format

11 chiffres et un trait d’union dans le format spécifié
  
### <a name="pattern"></a>Modèle

11 chiffres et un trait d’union :
  
-  Six chiffres qui correspondent à la date de naissance (jjmmaa) 
    
- Un trait d’union 
    
- Un chiffre qui correspond à la century de naissance (« 0 » pour century 19, « 1 » pour le vingtième century et « 2 » pour century 21)
    
- Quatre chiffres, générées de manière aléatoire
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_latvia_eu_national_id_card` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_latvia_eu_national_id_card` est trouvée. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_latvia_eu_national_id_card` recherche de contenu qui correspond au modèle. 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_latvia_eu_national_id_card" />
          <Match idRef="Keywords_latvia_eu_national_id_card" />
        </Pattern>
 <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_latvia_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordslatviaeunationalidcard"></a>Keywords_latvia_eu_national_id_card

code personnel
  
numéro de code personnel
  
nombre de certificats personnel
  
personalcodeno #
  
numéro d’identification personnelle
  
code d’identification personnelle
  
personnages kods
  
## <a name="lithuania"></a>Lituanie

### <a name="format"></a>Format

11 chiffres sans espaces et les séparateurs
  
### <a name="pattern"></a>Modèle

11 chiffres sans espaces et les séparateurs :
  
- Un chiffre qui correspond à la personne sexe et century de naissance
    
-  Six chiffres qui correspondent à la date de naissance (AAMMJJ) 
    
- Trois chiffres correspondant au numéro de série de la date de naissance
    
- Chiffre un contrôle
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_lithuania_eu_national_id_card` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_lithuania_eu_national_id_card` est trouvée. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_lithuania_eu_national_id_card` recherche de contenu qui correspond au modèle. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_lithuania_eu_national_id_card" />
          <Match idRef="Keywords_lithuania_eu_national_id_card" />
        </Pattern> 
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_lithuania_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordslithuaniaeunationalidcard"></a>Keywords_lithuania_eu_national_id_card

code numérique personnel
  
numéro d’identification unique
  
numéro de service citoyens
  
numéro d’identification unique
  
uniqueidentityno #
  
code personnel.
  
asmeninis skaitmeninis kodas
  
unikalus identifikavimo numeris
  
piliečio paslaugos numeris
  
unikalus identifikavimo kodas
  
asmens kodas.
  
## <a name="luxemburg"></a>Luxembourg

### <a name="format"></a>Format

11 chiffres sans espaces et les séparateurs
  
### <a name="pattern"></a>Modèle

11 chiffres
  
- Un chiffre qui correspond à la personne sexe et century de naissance
    
-  Six chiffres qui correspondent à la date de naissance (AAMMJJ) 
    
- Trois chiffres correspondant au numéro de série de la date de naissance
    
- Chiffre un contrôle
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_luxemburg_eu_national_id_card` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_luxemburg_eu_national_id_card` est trouvée. 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_national_id_card" />
          <Match idRef="Keywords_luxemburg_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsluxemburgeunationalidcard"></a>Keywords_luxemburg_eu_national_id_card

identifiant personnel
  
numéro d’identification personnelle
  
personalidno #
  
numéro d’identification unique
  
personalidnumber #
  
clé de l’id unique
  
code d’identification personnelle
  
uniqueidkey #
  
code individuels
  
id individuel
  
id d’eindeutige-nummer
  
id eindeutige
  
ID personnelle
  
numéro d’identification personnel
  
idpersonnelle #
  
persönliche identifikationsnummer
  
eindeutigeid #
  
## <a name="malta"></a>Malte

### <a name="format"></a>Format

Sept chiffres suivies d’une lettre
  
### <a name="pattern"></a>Modèle

Sept chiffres suivies d’une lettre :
  
-  Sept chiffres  
    
- Une lettre majuscule (respecte la casse)
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_malta_eu_national_id_card` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_malta_eu_national_id_card` est trouvée. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_malta_eu_national_id_card` recherche de contenu qui correspond au modèle. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_national_id_card" />
          <Match idRef="Keywords_malta_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_malta_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsmaltaeunationalidcard"></a>Keywords_malta_eu_national_id_card

code numérique personnel
  
numéro d’identification unique
  
numéro de service citoyens
  
numéro d’identification unique
  
uniqueidentityno #
  
kodiċi numerali personali
  
numru ta ' identifikazzjoni uniku
  
numru tas-servizz taċ-ċittadin
  
numru ta' identità uniku
  
## <a name="netherlands"></a>Pays-Bas

### <a name="format"></a>Format

Neuf chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

Neuf chiffres
  
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_netherlands_eu_national_id_card` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir d’est trouvé.
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_netherlands_eu_national_id_card` recherche de contenu qui correspond au modèle. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_netherlands_eu_national_id_card" />
          <Match idRef="Keywords_netherlands_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_netherlands_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsnetherlandseunationalidcard"></a>Keywords_netherlands_eu_national_id_card

code numérique personnel
  
numéro d’identification unique
  
numéro de service citoyens
  
numéro d’identification unique
  
uniqueidentityno #
  
bsn
  
bsn #
  
code de numerieke persoonlijke
  
uniek identificatienummer
  
burgerservicenummer
  
uniek identiteitsnummer
  
## <a name="poland"></a>Pologne

Pour plus d’informations, consultez la section « Pologne National ID (PESEL) » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="portugal"></a>Portugal

Pour plus d’informations, consultez la section « Portugal citoyens carte numéro » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="romania"></a>Roumanie

### <a name="format"></a>Format

13 chiffres sans espaces et les séparateurs
  
### <a name="pattern"></a>Modèle

13 chiffres
  
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_romania_eu_national_id_card` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_romania_eu_national_id_card` est trouvée. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_romania_eu_national_id_card` recherche de contenu qui correspond au modèle. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_romania_eu_national_id_card" />
          <Match idRef="Keywords_romania_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_romania_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsromaniaeunationalidcard"></a>Keywords_romania_eu_national_id_card

code numérique personnel
  
numéro d’identification unique
  
cnp
  
cnp #
  
épingler
  
code confidentiel #
  
numéro d’assurance
  
insurancenumber #
  
numéro d’identification unique
  
uniqueidentityno #
  
remboursement numérique personnel
  
cabillaud identificare personnel
  
remboursement unic identificare
  
unic personnel număr
  
număr identitate
  
identificare număr personnelle
  
număridentitate #
  
codnumericpersonal #
  
numărpersonalunic #
  
## <a name="slovakia"></a>République de Slovaquie

### <a name="format"></a>Format

Dix chiffres contenant une barre oblique inverse
  
### <a name="pattern"></a>Modèle

Dix chiffres contenant une barre oblique inverse :
  
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_slovakia_eu_national_id_card` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_slovakia_eu_national_id_card` est trouvée. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_slovakia_eu_national_id_card` recherche de contenu qui correspond au modèle. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_slovakia_eu_national_id_card" />
          <Match idRef="Keywords_slovakia_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_slovakia_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsslovakiaeunationalidcard"></a>Keywords_slovakia_eu_national_id_card

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
  
## <a name="slovenia"></a>Slovénie

### <a name="format"></a>Format

13 chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

13 chiffres dans le modèle spécifié :
  
-  Sept chiffres qui correspondent à la date de naissance (DDMMLLL) où « LLL » correspond à la dernière trois chiffres de l’année de naissance 
    
- Deux chiffres qui correspondent à la zone de naissance
    
- Trois chiffres qui correspondent à une combinaison de sexe et le numéro de série pour les personnes naissance le même jour (000-499 pour masculin) et 500-999 pour femme
    
- Chiffre un contrôle
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_slovenia_eu_national_id_card` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_slovenia_eu_national_id_card` est trouvée. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_slovenia_eu_national_id_card` recherche de contenu qui correspond au modèle. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_slovenia_eu_national_id_card" />
          <Match idRef="Keywords_slovenia_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_slovenia_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordssloveniaeunationalidcard"></a>Keywords_slovenia_eu_national_id_card

code numérique personnel
  
numéro d’identification unique
  
numéro d’enregistrement unique
  
numéro d’identification unique
  
uniqueidentityno #
  
numéro unique citoyens maître
  
edinstvena identifikacijska številka
  
uniqueidentityno #
  
edinstvena številka glavnega državljana
  
emšo
  
## <a name="spain"></a>Espagne

### <a name="format"></a>Format

Sept chiffres suivies d’un caractère
  
### <a name="pattern"></a>Modèle

Sept chiffres suivies d’un caractère
  
- Sept chiffres 
    
- Un chiffre ou une lettre (pas la casse)
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression régulière `Regex_spain_eu_national_id_card` recherche de contenu qui correspond au modèle. 
    
- Un mot clé à partir de `Keywords_spain_eu_national_id_card"` est trouvée. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_national_id_card" />
          <Match idRef="Keywords_spain_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsspaineunationalidcard"></a>Keywords_spain_eu_national_id_card

DNI
  
numéro d’identification nationale
  
numéro d’identité national
  
numéro d’assurance
  
numéro d’identification personnel
  
identité nationale
  
identité personnelle aucune
  
numéro d’identification unique
  
nationalidno #
  
UniqueID #
  
DNI #
  
nationalid #
  
NIE #
  
NIE
  
nienúmero #
  
NIE número
  
documento nacional de identidad
  
identidad único
  
Número nacional identidad
  
número DNI
  
dninúmero #
  
identidadúnico #
  
## <a name="sweden"></a>Suède

Pour plus d’informations, voir la section « ID National Suède » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="see-also"></a>Voir aussi

[Éléments recherchés par les types d’informations sensibles](what-the-sensitive-information-types-look-for.md)

