---
title: Numéro d’identification nationale de l’UE
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: Cette rubrique présente l’aspect d’une stratégie de protection contre la perte de données (DLP) lorsqu’elle détecte le type d’informations sensibles du numéro d’identification national de l’UE. Ce type d’informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.
ms.openlocfilehash: 205019d040648f0600f3dbf4403063edf9f31c41
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34154456"
---
# <a name="eu-national-identification-number"></a>Numéro d’identification nationale de l’UE

Cette rubrique présente l’aspect d’une stratégie de protection contre la perte de données (DLP) lorsqu’elle détecte le type d’informations sensibles du numéro d’identification national de l’UE. Ce type d’informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.
  
## <a name="austria"></a>Autriche

### <a name="format"></a>Format

Combinaison de 24 caractères de lettres, de chiffres et de caractères spéciaux
  
### <a name="pattern"></a>Modèle

24 caractères:
  
-  22 lettres (ne respectent pas la casse), chiffres, barres obliques inverses, barres obliques ou signes plus 
    
- Deux lettres (ne respectent pas la casse), des chiffres, des barres obliques inverses, des barres obliques, des signes plus ou des signes égal
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression `Regex_austria_eu_national_id_card` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_austria_eu_national_id_card` from est trouvé. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_national_id_card" />
          <Match idRef="Keywords_austria_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordsaustriaeunationalidcard"></a>Keywords_austria_eu_national_id_card

Numéro d’identité autrichien
  
Numéro d’identité nationale
  
Numéro d’identité
  
id national
  
personalausweis republik österreich
  
## <a name="belgium"></a>Belgique

Pour plus d’informations, reportez-vous à la section «Belgique numéro national» dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="bulgaria"></a>Bulgarie

### <a name="format"></a>Format

Dix chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

Dix chiffres sans espaces ni délimiteurs
  
-  Six chiffres correspondant à la date de naissance (AAMMJJ) 
    
- Deux chiffres correspondant à l’ordre de naissance
    
- Un chiffre correspondant au sexe: un chiffre pair pour le mâle et un chiffre impair pour femelle.
    
- Un chiffre de contrôle
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_bulgaria_national_number` trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_bulgaria_national_number` from est trouvé. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_bulgaria_national_number` trouve le contenu qui correspond au modèle. 
    
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

### <a name="keywords"></a>Mots clés

#### <a name="keywordsbulgarianationalnumber"></a>Keywords_bulgaria_national_number

egn
  
egn#
  
numéro national bulgare
  
numéro national
  
numéro de sécurité sociale
  
nationalnumber#
  
SSN
  
SSN
  
nationalnumber
  
bnn#
  
bnn
  
Numéro d’identification personnel
  
personalidnumber#
  
единен граждански номер
  
edinen grazhdanski nomer
  
егн
  
егн#
  
## <a name="croatia"></a>Croatie

Pour plus d’informations, reportez-vous à la section «Croatie Identity Number» dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="cyprus"></a>Chypre

### <a name="format"></a>Format

Dix chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

 Dix chiffres 
  
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression `Regex_cyprus_eu_national_id_card` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_cyprus_eu_national_id_card` from est trouvé. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_national_id_card" />
          <Match idRef="Keywords_cyprus_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordscypruseunationalidcard"></a>Keywords_cyprus_eu_national_id_card

Numéro de carte d’identité
  
numéro d’identification nationale
  
Numéro d’identification personnel
  
Numéro de carte d’identité
  
ταυτοτητασ
  
## <a name="czech-republic"></a>République tchèque

Pour plus d’informations, consultez la section «numéro d’identité nationale tchèque» dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="denmark"></a>Danemark

Pour plus d’informations, reportez-vous à la section «numéro d’identification personnel Danemark» dans [ce que recherche les types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="estonia"></a>Estonie

### <a name="format"></a>Format

11 chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

11 chiffres :
  
- Un chiffre correspondant au sexe et au siècle de naissance (nombre impair mâle, numéro pair femelle; 1-2:19 siècle; 3-4:20ème siècle; 5-6:21ème siècle)
    
- Six chiffres correspondant à la date de naissance (AAMMJJ)
    
- Trois chiffres correspondant à un numéro de série séparant les personnes nés à la même date
    
- Un chiffre de contrôle
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_estonia_eu_national_id_card` trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_estonia_eu_national_id_card` from est trouvé. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_estonia_eu_national_id_card` trouve le contenu qui correspond au modèle. 
    
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

### <a name="keywords"></a>Mots clés

#### <a name="keywordsestoniaeunationalidcard"></a>Keywords_estonia_eu_national_id_card

code d’identification personnel
  
Numéro d’identification personnel
  
numéro d’identification nationale
  
numéro national
  
Numéro d’identification personnel
  
personalidnumber#
  
inverse
  
isikukood
  
ID-kaart
  
## <a name="finland"></a>Finlande

Pour plus d’informations, reportez-vous à la section «ID national de Finlande» dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="france"></a>France

Pour plus d’informations, reportez-vous à la section «carte d’identité nationale France (CNI)» dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="germany"></a>Allemagne

Pour plus d’informations, reportez-vous à la section «Germany Identity Card Number» dans les [types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="greece"></a>Grèce

Pour plus d’informations, reportez-vous à la section «carte d’identité nationale Grèce» dans [ce que recherche les types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="hungary"></a>Hongrie

### <a name="format"></a>Format

11 chiffres
  
### <a name="pattern"></a>Modèle

11 chiffres :
  
-  Un chiffre correspondant au sexe (1-mâle, 2 femelles), d’autres numéros sont également possibles pour les citoyens nés avant 1900 ou les citoyens ayant une double citoyenneté. 
    
- Six chiffres correspondant à la date de naissance (AAMMJJ)
    
- Trois chiffres correspondant à un numéro de série
    
- Un chiffre de contrôle
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_hungary_eu_national_id_card` trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_hungary_eu_national_id_card` from est trouvé. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_hungary_eu_national_id_card` trouve le contenu qui correspond au modèle. 
    
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

### <a name="keywords"></a>Mots clés

#### <a name="keywordshungaryeunationalidcard"></a>Keywords_hungary_eu_national_id_card

Numéro d’identification personnel
  
numéro d’identification
  
Numéro d’identification personnel
  
személyazonosító igazolvány
  
## <a name="ireland"></a>Irlande

### <a name="format"></a>Format

Combinaison de neuf caractères de lettres, de chiffres et d’un espace dans le modèle spécifié
  
### <a name="pattern"></a>Modèle

Combinaison de neuf caractères de lettres, de chiffres et d’un espace dans le modèle spécifié
  
Du 01 janvier 2013 au maintenant:
  
-  Sept chiffres  
    
- Un chiffre de contrôle
    
- Un espace ou la lettre majuscule «W» (respecte la casse)
    
Avant le 1er janvier 2013:
  
-  Sept chiffres  
    
- Un chiffre de contrôle
    
- Un espace ou une lettre majuscule (respecte la casse)
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction trouve le contenu qui correspond au modèle.
    
- Un mot clé from est trouvé.
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction trouve le contenu qui correspond au modèle.
    
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

### <a name="keywords"></a>Mots clés

#### <a name="keywordsirelandeunationalidcard"></a>Keywords_ireland_eu_national_id_card

Numéro de service public
  
n ° PPS
  
Numéro de produit et d’assurance sociale
  
RSI non
  
Numéro d’identification personnel
  
numéro d’identification
  
Numéro d’identification personnel
  
uimhir phearsanta seirbhíse poiblí
  
uimh. toxine
  
## <a name="italy"></a>Italie

### <a name="format"></a>Format

Combinaison de 16 caractères de lettres et de chiffres dans le modèle spécifié.
  
### <a name="pattern"></a>Modèle

Combinaison de lettres et de chiffres de 16 caractères:
  
- Trois lettres qui correspondent aux trois premières consonnes du nom de la famille
    
- Trois lettres qui correspondent à la première, troisième et quatrième consonnes du prénom
    
- Deux chiffres correspondant aux derniers chiffres de l’année de naissance
    
- Une lettre correspondant à la lettre du mois de naissance: les lettres sont utilisées dans l’ordre alphabétique, mais seules les lettres de A à E, H, L, M, P, R à T sont utilisées (par conséquent, le mois de janvier est A et le mois d’octobre est R).
    
- Deux chiffres correspondant au jour du mois de naissance — afin de différencier les hommes, 40 est ajouté au jour de naissance pour les femmes
    
- Quatre chiffres correspondant à l’indicatif régional propre à la municipalité où la personne est né (des codes pays sont utilisés pour les pays étrangers)
    
- Un chiffre de parité
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_italy_eu_national_id_card` trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_italy_eu_national_id_card` from est trouvé. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_italy_eu_national_id_card` trouve le contenu qui correspond au modèle. 
    
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

### <a name="keywords"></a>Mots clés

#### <a name="keywordsitalyeunationalidcard"></a>Keywords_italy_eu_national_id_card

code personnel
  
Numéro de code personnel
  
Numéro de certificat personnel
  
code fiscal
  
personalcodeno#
  
Numéro d’identification personnel
  
code d’identification personnel
  
codice Personal
  
numération Certificate-personnel
  
numération personnelle
  
ID de numérotation personnelle
  
codice ID personnel
  
Codice fiscale
  
## <a name="italy"></a>Italie

### <a name="format"></a>Format

11 chiffres et un trait d’Union dans le format spécifié
  
### <a name="pattern"></a>Modèle

11 chiffres et un trait d’Union:
  
-  Six chiffres correspondant à la date de naissance (JJMMAA) 
    
- Un trait d’union 
    
- Un chiffre correspondant au siècle de naissance («0» pour le 19 siècle, «1» pour le vingtième siècle et «2» pour le 21ème siècle).
    
- Quatre chiffres, généré de manière aléatoire
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_latvia_eu_national_id_card` trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_latvia_eu_national_id_card` from est trouvé. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_latvia_eu_national_id_card` trouve le contenu qui correspond au modèle. 
    
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

### <a name="keywords"></a>Mots clés

#### <a name="keywordslatviaeunationalidcard"></a>Keywords_latvia_eu_national_id_card

code personnel
  
Numéro de code personnel
  
Numéro de certificat personnel
  
personalcodeno#
  
Numéro d’identification personnel
  
code d’identification personnel
  
Personas kods
  
## <a name="lithuania"></a>Lituanie

### <a name="format"></a>Format

11 chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

11 chiffres sans espaces ni délimiteurs:
  
- Un chiffre correspondant au sexe et au siècle de la personne
    
-  Six chiffres correspondant à la date de naissance (AAMMJJ) 
    
- Trois chiffres correspondant au numéro de série de la date de naissance
    
- Un chiffre de contrôle
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_lithuania_eu_national_id_card` trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_lithuania_eu_national_id_card` from est trouvé. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_lithuania_eu_national_id_card` trouve le contenu qui correspond au modèle. 
    
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

### <a name="keywords"></a>Mots clés

#### <a name="keywordslithuaniaeunationalidcard"></a>Keywords_lithuania_eu_national_id_card

code numérique personnel
  
Numéro d’identification unique
  
Numéro de service du citoyen
  
Numéro d’identité unique
  
uniqueidentityno#
  
code personnel.
  
asmeninis skaitmeninis kodas
  
unikalus identifikavimo
  
piliečio paslaugos
  
unikalus identifikavimo kodas
  
asmens kodas.
  
## <a name="luxemburg"></a>Relatif

### <a name="format"></a>Format

11 chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

11 chiffres
  
- Un chiffre correspondant au sexe et au siècle de la personne
    
-  Six chiffres correspondant à la date de naissance (AAMMJJ) 
    
- Trois chiffres correspondant au numéro de série de la date de naissance
    
- Un chiffre de contrôle
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression `Regex_luxemburg_eu_national_id_card` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_luxemburg_eu_national_id_card` from est trouvé. 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_national_id_card" />
          <Match idRef="Keywords_luxemburg_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordsluxemburgeunationalidcard"></a>Keywords_luxemburg_eu_national_id_card

ID personnel
  
Numéro d’identification personnel
  
personalidno#
  
Numéro d’identification unique
  
personalidnumber#
  
clé d’ID unique
  
code d’identification personnel
  
uniqueidkey#
  
code individuel
  
ID individuel
  
ID eindeutige-Nummer
  
ID eindeutige
  
ID personnelle
  
Numéro d’identification personnel
  
idpersonnelle#
  
persönliche identifikationsnummer
  
eindeutigeid#
  
## <a name="malta"></a>Malte

### <a name="format"></a>Format

Sept chiffres suivis d’une lettre
  
### <a name="pattern"></a>Modèle

Sept chiffres suivis d’une lettre:
  
-  Sept chiffres  
    
- Une lettre majuscule (respecte la casse)
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression `Regex_malta_eu_national_id_card` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_malta_eu_national_id_card` from est trouvé. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :
  
- L’expression `Regex_malta_eu_national_id_card` régulière trouve le contenu qui correspond au modèle. 
    
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

### <a name="keywords"></a>Mots clés

#### <a name="keywordsmaltaeunationalidcard"></a>Keywords_malta_eu_national_id_card

code numérique personnel
  
Numéro d’identification unique
  
Numéro de service du citoyen
  
Numéro d’identité unique
  
uniqueidentityno#
  
Kodiċi numerali
  
numru ta’IDENTIFIKAZZJONI uniku
  
numru-Servizz taċ-ċittadin
  
numru ta’identità uniku
  
## <a name="netherlands"></a>Pays-Bas

### <a name="format"></a>Format

Neuf chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

Neuf chiffres
  
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_netherlands_eu_national_id_card` trouve le contenu qui correspond au modèle. 
    
- Un mot clé from est trouvé.
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_netherlands_eu_national_id_card` trouve le contenu qui correspond au modèle. 
    
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

### <a name="keywords"></a>Mots clés

#### <a name="keywordsnetherlandseunationalidcard"></a>Keywords_netherlands_eu_national_id_card

code numérique personnel
  
Numéro d’identification unique
  
Numéro de service du citoyen
  
Numéro d’identité unique
  
uniqueidentityno#
  
BSN
  
BSN
  
persoonlijke Numerieke de code
  
uniek identificatienummer
  
burgerservicenummer
  
uniek identiteitsnummer
  
## <a name="poland"></a>Pologne

Pour plus d’informations, reportez-vous à la section «Pologne national ID (PESEL)» dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="portugal"></a>Portugal

Pour plus d’informations, reportez-vous à la section «numéro de carte de citoyen Portugal» dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="romania"></a>Roumanie

### <a name="format"></a>Format

13 chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

13 chiffres
  
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_romania_eu_national_id_card` trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_romania_eu_national_id_card` from est trouvé. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_romania_eu_national_id_card` trouve le contenu qui correspond au modèle. 
    
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

### <a name="keywords"></a>Mots clés

#### <a name="keywordsromaniaeunationalidcard"></a>Keywords_romania_eu_national_id_card

code numérique personnel
  
Numéro d’identification unique
  
cnp
  
cnp#
  
ancre
  
ancre
  
Numéro d’assurance
  
insurancenumber#
  
Numéro d’identité unique
  
uniqueidentityno#
  
COD numérique personnel
  
COD IDENTIFICARE personnel
  
COD UNIC IDENTIFICARE
  
UNIC personnel număr
  
număr identitate
  
număr IDENTIFICARE personnel
  
număridentitate#
  
codnumericpersonal#
  
numărpersonalunic#
  
## <a name="slovakia"></a>République de Slovaquie

### <a name="format"></a>Format

Dix chiffres contenant une barre oblique inverse
  
### <a name="pattern"></a>Modèle

Dix chiffres contenant une barre oblique inverse:
  
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_slovakia_eu_national_id_card` trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_slovakia_eu_national_id_card` from est trouvé. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_slovakia_eu_national_id_card` trouve le contenu qui correspond au modèle. 
    
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

### <a name="keywords"></a>Mots clés

#### <a name="keywordsslovakiaeunationalidcard"></a>Keywords_slovakia_eu_national_id_card

Numéro de naissance
  
numéro d’identification nationale
  
Numéro d’identification personnel
  
numéro de sécurité sociale
  
nationalnumber#
  
SSN
  
SSN
  
numéro national
  
Numéro d’identification personnel
  
personalidnumber#
  
rč
  
rodné číslo
  
rodne cislo
  
## <a name="slovenia"></a>Slovénie

### <a name="format"></a>Format

13 chiffres sans espaces ni délimiteurs
  
### <a name="pattern"></a>Modèle

13 chiffres dans le modèle spécifié:
  
-  Sept chiffres correspondant à la date de naissance (DDMMLLL) où «LLL» correspond aux trois derniers chiffres de l’année de naissance 
    
- Deux chiffres correspondant à la zone de naissance
    
- Trois chiffres correspondant à une combinaison de sexe et de numéro de série pour les personnes nées le même jour (000-499 pour les mâles et les 500-999 pour les femelles)
    
- Un chiffre de contrôle
    
### <a name="checksum"></a>Somme de contrôle

Oui
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_slovenia_eu_national_id_card` trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_slovenia_eu_national_id_card` from est trouvé. 
    
Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- La fonction `Func_slovenia_eu_national_id_card` trouve le contenu qui correspond au modèle. 
    
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

### <a name="keywords"></a>Mots clés

#### <a name="keywordssloveniaeunationalidcard"></a>Keywords_slovenia_eu_national_id_card

code numérique personnel
  
Numéro d’identification unique
  
Numéro d’enregistrement unique
  
Numéro d’identité unique
  
uniqueidentityno#
  
Numéro de citoyen principal unique
  
edinstvena identifikacijska številka
  
uniqueidentityno #
  
edinstvena številka glavnega državljana
  
emšo
  
## <a name="spain"></a>Espagne

### <a name="format"></a>Format

Sept chiffres suivis d’un caractère
  
### <a name="pattern"></a>Modèle

Sept chiffres suivis d’un caractère
  
- Sept chiffres 
    
- Un chiffre ou une lettre (ne respectant pas la casse)
    
### <a name="checksum"></a>Somme de contrôle

Non applicable
  
### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
  
- L’expression `Regex_spain_eu_national_id_card` régulière trouve le contenu qui correspond au modèle. 
    
- Un mot clé `Keywords_spain_eu_national_id_card"` from est trouvé. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_national_id_card" />
          <Match idRef="Keywords_spain_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordsspaineunationalidcard"></a>Keywords_spain_eu_national_id_card

DNI
  
numéro d’identification nationale
  
Numéro d’identité nationale
  
Numéro d’assurance
  
Numéro d’identification personnel
  
identité nationale
  
n ° d’identité personnelle
  
Numéro d’identité unique
  
nationalidno#
  
quei
  
DNI
  
nationalid#
  
nie
  
nie
  
nienúmero#
  
nie número
  
Documento Nacional de identidad
  
identidad único
  
número Nacional identidad
  
DNI número
  
dninúmero#
  
identidadúnico#
  
## <a name="sweden"></a>Suède

Pour plus d’informations, reportez-vous à la section «ID national Suède» dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
  
## <a name="see-also"></a>Voir aussi

[Éléments recherchés par les types d’informations sensibles](what-the-sensitive-information-types-look-for.md)

