---
title: Éléments recherchés par les types d’informations sensibles
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: reference
f1_keywords:
- ms.o365.cc.UnifiedDLPRuleContainsSensitiveInformation
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
ms.assetid: fd505979-76be-4d9f-b459-abef3fc9e86b
description: Prévention des pertes de données (DLP) de sécurité Office 365 &amp; centre de conformité inclut 80 types d’informations sensibles qui sont prêts à utiliser dans vos stratégies DLP. Cette rubrique répertorie tous ces types d’informations sensibles et illustre une stratégie DLP lorsqu’il détecte chaque type.
ms.openlocfilehash: 064606085363ba9de972511642993277451c8ce3
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528476"
---
# <a name="what-the-sensitive-information-types-look-for"></a>Éléments recherchés par les types d’informations sensibles

Prévention des pertes de données (DLP) de sécurité Office 365 &amp; centre de conformité inclut de nombreux types d’informations sensibles qui sont prêts à utiliser dans vos stratégies DLP. Cette rubrique répertorie tous ces types d’informations sensibles et illustre une stratégie DLP lorsqu’il détecte chaque type. Un type d’informations sensibles est défini par un modèle qui peut être identifié par une expression régulière ou une fonction. En outre, la preuve corroborante tels que des mots clés et les totaux de contrôle peut servir à identifier un type d’informations sensibles. Proximité et niveau de confiance sont également utilisés dans le processus d’évaluation.
  
## <a name="aba-routing-number"></a>Numéro de routage ABA

### <a name="format"></a>Format

9 chiffres mis en forme ou non mis en forme

### <a name="pattern"></a>Modèle

Mis en forme :
- Quatre chiffres commençant par 0, 1, 2, 3, 6, 7 ou 8
- Un trait d’union
- Quatre chiffres
- Un trait d’union
- Un chiffre

Non formatée : 9 chiffres consécutifs commencent par 0, 1, 2, 3, 6, 7 ou 8 

### <a name="checksum"></a>Somme de contrôle

Non

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- La fonction Func_aba_routing trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_ABA_Routing est trouvé.

```
<!-- ABA Routing Number -->
<Entity id="cb353f78-2b72-4c3c-8827-92ebe4f69fdf" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_aba_routing" />
        <Match idRef="Keyword_ABA_Routing" />
      </Pattern>
 </Entity>
```


### <a name="keywords"></a>Mots clés

#### <a name="keywordabarouting"></a>Keyword_ABA_Routing

- aba
- 
# aba
- 
# routage aba
- numéro de routage ABA
- 
#aba
- 
#routageaba
- 
numéro aba
- 
numéroroutageaba
- 
# routage american bank association
- 
numéro de routage american bank association
- 
#routageamericanbankassociation
- 
numéroderoutageamericanbankassociation
- 
numéro de routage bancaire
- 
#routagebancaire
- 
numéroderoutagebancaire
- 
numéro de routage
- 
RTN
 
   
## <a name="argentina-national-identity-dni-number"></a>Numéro d’identité nationale (DNI) pour l’Argentine

### <a name="format"></a>Format

Huit chiffres séparés par des points

### <a name="pattern"></a>Modèle

Huit chiffres :
- Deux chiffres
- Un point 
- Trois chiffres
- Un point 
- Trois chiffres

### <a name="checksum"></a>Somme de contrôle

Non

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- L’expression régulière Regex_argentina_national_id trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_argentina_national_id est trouvé.

```
<!-- Argentina National Identity (DNI) Number -->
<Entity id="eefbb00e-8282-433c-8620-8f1da3bffdb2" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_argentina_national_id"/>
      <Match idRef="Keyword_argentina_national_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordargentinanationalid"></a>Keyword_argentina_national_id

- Argentina National Identity number
 
- Identité 
- Carte nationale d’identification 
- DNI
 
- Carte réseau Registre National de personnes 
- Documento Nacional de Identidad
 
- Registro Nacional de las Personas
 
- Identidad
 
- Identificación
 
   
## <a name="australia-bank-account-number"></a>Numéro de compte bancaire Australie

### <a name="format"></a>Format

6 à 10 chiffres avec ou sans le numéro d’agence bancaire de l’État

### <a name="pattern"></a>Modèle

Numéro de compte est de 6 à 10 chiffres. Numéro de succursale bancaire Australie état :
- Trois chiffres 
- Un trait d’union  
- Trois chiffres

### <a name="checksum"></a>Somme de contrôle

Non

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
- L’expression régulière Regex_australia_bank_account_number trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_australia_bank_account_number est trouvé.
- L’expression régulière Regex_australia_bank_account_number_bsb trouve un contenu qui correspond au modèle.

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- L’expression régulière Regex_australia_bank_account_number trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_australia_bank_account_number est trouvé.

```
<!-- Australia Bank Account Number -->
<Entity id="74a54de9-2a30-4aa0-a8aa-3d9327fc07c7" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Regex_australia_bank_account_number" />
        <Match idRef="Keyword_australia_bank_account_number" />
        <Match idRef="Regex_australia_bank_account_number_bsb" />
  </Pattern>
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_australia_bank_account_number" />
        <Match idRef="Keyword_australia_bank_account_number" />
  </Pattern>
 </Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordaustraliabankaccountnumber"></a>Keyword_australia_bank_account_number

- code swift banque
- 
banque correspondante
- 
devise de base
- 
compte aux États-Unis
- 
adresse du titulaire
- 
adresse de la banque
- 
informations du compte
- 
transferts de fonds
- 
frais bancaires
- 
informations sur la banque
- 
informations bancaires
- 
noms complets
- 

iaea

   
## <a name="australia-drivers-license-number"></a>Numéro de permis de conduire Australie

### <a name="format"></a>Format

Neuf lettres et chiffres

### <a name="pattern"></a>Modèle

Neuf lettres et chiffres : 

- Deux chiffres ou lettres (ne respectent pas la casse) 
- Deux chiffres 
- Cinq chiffres ou lettres (ne respectent pas la casse)

OU

- 1 ou 2 lettres facultatives (ne respectant pas la casse)  
- 4 à 9 chiffres

OU

- Neuf chiffres ou lettres (ne respectant pas la casse)

### <a name="checksum"></a>Somme de contrôle

Non

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- L’expression régulière Regex_australia_drivers_license_number trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_australia_drivers_license_number est trouvé.
- Aucun mot clé figurant dans la liste Keyword_australia_drivers_license_number_exclusions n’est trouvé.

```
<!-- Australia Drivers License Number -->
<Entity id="1cbbc8f5-9216-4392-9eb5-5ac2298d1356" patternsProximity="300" recommendedConfidence="75">
   <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_australia_drivers_license_number" />
        <Match idRef="Keyword_australia_drivers_license_number" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_australia_drivers_license_number_exclusions" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordaustraliadriverslicensenumber"></a>Keyword_australia_drivers_license_number

- permis de conduite internationaux
- 
australian automobile association
- 
sydney nsw
- 
permis de conduite international
- DriverLicence
- DriverLicences
- Lic pilote
- Permis de conduire

- Permis de conduire

- DriversLic
- DriversLicence
- DriversLicences
- Lic pilotes
- Lics pilotes
- Certificat de pilotes
- Certificats de pilotes
- Driver'Lic
- Driver'Lics
- Driver'Licence
- Driver'Licences
- Pilote ' Lic
- Pilote ' Lics
- Pilote ' certificat
- Pilote « certificats
- Driver'sLic
- Driver'sLics
- Driver'sLicence
- Driver'sLicences
- Lic du pilote
- Lics permis de conduire
- Permis de conduire

- Permis de conduire

- DriverLic #
- DriverLics #
- DriverLicence #
- DriverLicences #
- #Permis conduire
- 
#Permis conduire

- Pilote certificat #
- Pilote certificats #
- DriversLic #
- DriversLics #
- DriversLicence #
- DriversLicences #
- Pilotes Lic #
- Pilotes Lics #
- Licence pilotes #
- Certificats pilotes #
- #Permisconduire

- #Permisconduire

- #Permisdeconduire

- #Permisdeconduire

- #Permis conduire

- #Permis conduire

- Pilote ' certificat #
- Pilote « certificats #
- Driver'sLic #
- Driver'sLics #
- Driver'sLicence #
- Driver'sLicences #
- #Permisconduire

- #Permisconduire

- Certificat de # permis de conduire
- Certificats de # permis de conduire 

#### <a name="keywordaustraliadriverslicensenumberexclusions"></a>Keyword_australia_drivers_license_number_exclusions

- aaa
- DriverLicense
- DriverLicenses
- Conduire
- Licences de pilote
- Conduire
- DriversLicenses
- Permis de conduire
- Licences de pilotes
- Driver'License
- Driver'Licenses
- Pilote ' licence
- Pilote ' licences
- Driver'sLicense
- Driver'sLicenses
- Conduire permis de
- Conduire permis de
- DriverLicense #
- DriverLicenses #
- Pilote licence #
- Licences de pilote #
- Conduire #
- DriversLicenses #
- Licence pilotes #
- Licences pilotes #
- #Permisdeconduire

- #Permisdeconduire

- #Permis de conduire

- #Permis de conduire

- Driver'sLicense #
- Driver'sLicenses #
- #Permis de conduire

- 

#Permis de conduire
   
## <a name="australia-medical-account-number"></a>Numéro de dossier médical Australie

### <a name="format"></a>Format

10 à 11 chiffres

### <a name="pattern"></a>Modèle

10 à 11 chiffres :
- Le premier chiffre est compris entre 2 et 6
- Le neuvième chiffre est un chiffre de contrôle
- Le dixième chiffre est le chiffre d’émission
- Le onzième chiffre (facultatif) est le numéro individuel

### <a name="checksum"></a>Somme de contrôle

Oui

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 95 % si, dans une proximité de 300 caractères :
- La fonction Func_australian_medical_account_number trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_Australia_Medical_Account_Number est trouvé.
- La somme de contrôle est correcte.

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
- La fonction Func_australian_medical_account_number trouve un contenu qui correspond au modèle.
- La somme de contrôle est correcte.

```
  <!-- Australia Medical Account Number -->
<Entity id="104a99a0-3d3b-4542-a40d-ab0b9e1efe63" recommendedConfidence="85" patternsProximity="300">
    <Pattern confidenceLevel="95">
     <IdMatch idRef="Func_australian_medical_account_number"/>
     <Any minMatches="1">
     <Match idRef="Keyword_Australia_Medical_Account_Number"/>
     </Any>
  </Pattern>
<Pattern confidenceLevel="85">
     <IdMatch idRef="Func_australian_medical_account_number"/>
     <Any minMatches="0" maxMatches="0">
  <Match idRef="Keyword_Australia_Medical_Account_Number"/>
     </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordaustraliamedicalaccountnumber"></a>Keyword_Australia_Medical_Account_Number

- informations sur le compte bancaire
- 
remboursements d’assurance maladie
- 
compte de prêts immobiliers
- 
paiements bancaires
- 
direction de l’information
- 
prêt sur carte de crédit
- 
département des services sociaux
- service local
- 

medicare

   
## <a name="australia-passport-number"></a>Numéro de passeport Australie

### <a name="format"></a>Format

Une lettre suivie de sept chiffres

### <a name="pattern"></a>Modèle

Une lettre (ne respectant pas la casse) suivie de sept chiffres

### <a name="checksum"></a>Somme de contrôle

Non

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- L’expression régulière Regex_australia_passport_number trouve un contenu qui correspond au modèle.
- Un mot clé à partir de Keyword_passport ou Keyword_australia_passport_number est trouvé.

```
<!-- Australia Passport Number -->
<Entity id="29869db6-602d-4853-ab93-3484f905df50" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_australia_passport_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_passport" />
          <Match idRef="Keyword_australia_passport_number" />
        </Any>
   </Pattern>
</Entity>   
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordpassport"></a>Keyword_passport

- Numéro de passeport
- 
N° de passeport
- # Passeport

- #Passeport

- IDPassport
- n° passeport

- numéropasseport

- パスポート
- パスポート番号

- パスポートのNum

- 
パスポート＃
 
- Numéro de passeport
- 
Passeport n°
- Passeport numéro

- # Passeport

- Passeport#

- PasseportNon
- Passeportn °


#### <a name="keywordaustraliapassportnumber"></a>Keyword_australia_passport_number

- passeport
- 
informations sur le passeport
- 
immigration et citoyenneté
- 
Australie
- 
service de l’immigration
- 
adresse de résidence
- 
service de l’immigration et de la citoyenneté
- visa

- 
Carte nationale d’identité
- numéro de passeport
- 
document de voyage
- 

autorité émettrice
   
## <a name="australia-tax-file-number"></a>Numéro de dossier fiscal Australie

### <a name="format"></a>Format

8 ou 9 chiffres

### <a name="pattern"></a>Modèle

8 à 9 chiffres généralement entrecoupés d’espaces comme suit :
- Trois chiffres 
- Un espace facultatif 
- Trois chiffres 
- Un espace facultatif 
- 2 à 3 chiffres où le dernier chiffre est un chiffre de contrôle

### <a name="checksum"></a>Somme de contrôle

Oui

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
- La fonction Func_australian_tax_file_number trouve un contenu qui correspond au modèle.
- Aucun mot clé figurant dans la liste Keyword_Australia_Tax_File_Number ou Keyword_number_exclusions n’est trouvé.
- La somme de contrôle est correcte.

```
    <!-- Australia Tax File Number -->
<Entity id="e29bc95f-ff70-4a37-aa01-04d17360a4c5" patternsProximity="300" recommendedConfidence="85">
    
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_australian_tax_file_number" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_Australia_Tax_File_Number" />
          <Match idRef="Keyword_number_exclusions" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordaustraliataxfilenumber"></a>Keyword_Australia_Tax_File_Number

- numéro d’entreprise australien
- 
taux d’imposition marginale
- 
prélèvement d’assurance maladie
- 
numéro de portefeuille
- 
service des vétérans
- 
retenue à la source
- 
déclaration d’impôts individuels
- 

numéro de dossier fiscal

#### <a name="keywordnumberexclusions"></a>Keyword_number_exclusions

- 00000000
- 11111111
- 22222222
- 33333333
- 44444444
- 55555555
- 66666666
- 77777777
- 88888888
- 99999999
- 000000000
- 111111111
- 222222222
- 333333333
- 444444444
- 555555555
- 666666666
- 777777777
- 888888888
- 999999999
- 0000000000
- 1111111111
- 2222222222
- 3333333333
- 4444444444
- 5555555555
- 6666666666
- 7777777777
- 8888888888
- 9999999999
   
## <a name="belgium-national-number"></a>Numéro national Belgique

### <a name="format"></a>Format

11 chiffres plus des délimiteurs

### <a name="pattern"></a>Modèle

11 chiffres plus des délimiteurs :
- Six chiffres et deux points au format AA.MM.JJ pour la date de naissance  
- Un trait d’union  
- Trois chiffres séquentiels (impairs pour les hommes, pairs pour les femmes)  
- Un point  
- Deux chiffres de contrôle

### <a name="checksum"></a>Somme de contrôle

Oui

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- La fonction Func_belgium_national_number trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_belgium_national_number est trouvé.
- La somme de contrôle est correcte.

```
<!-- Belgium National Number -->
  <Entity id="fb969c9e-0fd1-4b18-8091-a2123c5e6a54" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_belgium_national_number"/>
     <Match idRef="Keyword_belgium_national_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordbelgiumnationalnumber"></a>Keyword_belgium_national_number

- Identité
- Registration
- Identification 
- ID 
- Identiteitskaart
- Registratie nummer 
 
- Identificatie nummer
 
- Identiteit
- Registratie
- Identificatie

 
- Carte d’identité
 
- numéro d’immatriculation
- numéro d’identification
- 
identité
 
- inscription
 
- Identifikation
- Identifizierung
- Identifikationsnummer
- Personalausweis
- Registrierung
- Registrationsnummer

   
## <a name="brazil-cpf-number"></a>Numéro CPF Brésil

### <a name="format"></a>Format

11 chiffres qui incluent un chiffre de contrôle et peuvent ou non être mis en forme 

### <a name="pattern"></a>Modèle

Mis en forme :
- Trois chiffres 
- Un point  
- Trois chiffres 
- Un point  
- Trois chiffres 
- Un trait d’union  
- Deux chiffres de contrôle

Non mis en forme :
- 11 chiffres où les deux derniers sont des chiffres de contrôle

### <a name="checksum"></a>Somme de contrôle

Oui

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
- La fonction Func_brazil_cpf trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_brazil_cpf est trouvé.
- La somme de contrôle est correcte.

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- La fonction Func_brazil_cpf trouve un contenu qui correspond au modèle.
- La somme de contrôle est correcte.

```
<!-- Brazil CPF Number -->
<Entity id="78e09124-f2c3-4656-b32a-c1a132cd2711" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_brazil_cpf"/>
     <Match idRef="Keyword_brazil_cpf"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_brazil_cpf"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordbrazilcpf"></a>Keyword_brazil_cpf

- CPF
- Identification
- Registration
- Revenue
- Cadastro de Pessoas Físicas
 
- Imposto
 
- Identificação
 
- Inscrição
 
- Receita

 
   
## <a name="brazil-legal-entity-number-cnpj"></a>Numéro d’entité juridique (CNPJ) Brésil

### <a name="format"></a>Format

14 chiffres qui incluent un numéro d’enregistrement, un numéro de succursale et des chiffres de contrôle, avec des délimiteurs en plus

### <a name="pattern"></a>Modèle
14 chiffres plus des délimiteurs :
- Deux chiffres 
- Un point  
- Trois chiffres 
- Un point  
- Trois chiffres (ces huit premiers chiffres composent le numéro d’enregistrement)  
- Une barre oblique  
- Le numéro de succursale à quatre chiffres  
- Un trait d’union  
- Deux chiffres de contrôle

### <a name="checksum"></a>Somme de contrôle

Oui

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
- La fonction Func_brazil_cnpj trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_brazil_cnpj est trouvé.
- La somme de contrôle est correcte.

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- La fonction Func_brazil_cnpj trouve un contenu qui correspond au modèle.
- La somme de contrôle est correcte.

```
<!-- Brazil Legal Entity Number (CNPJ) -->
<Entity id="9b58b5cd-5e90-4df6-b34f-1ebcc88ceae4" recommendedConfidence="85" patternsProximity="300">
   <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_brazil_cnpj"/>
     <Match idRef="Keyword_brazil_cnpj"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_brazil_cnpj"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordbrazilcnpj"></a>Keyword_brazil_cnpj

- CNPJ
 
- CNPJ/MF 
- CNPJ-MF
 
- National Registry of Legal Entities
 
- Taxpayers Registry
 
- Legal entity
 
- Legal entities
 
- Registration Status
 
- Business
 
- Company
- CNPJ
 
- Cadastro Nacional da Pessoa Jurídica
 
- Cadastro Geral de Contribuintes
 
- CGC
 
- Pessoa jurídica
 
- Pessoas jurídicas
 
- Situação cadastral
 
- Inscrição
 
- Empresa
 
   
## <a name="brazil-national-id-card-rg"></a>	Brazil National ID Card (RG)

### <a name="format"></a>Format

Registro Geral (ancien format) : neuf chiffres

Registro de Identidade (RIC) (nouveau format) : 11 chiffres

### <a name="pattern"></a>Modèle

Registro Geral (ancien format) :
- Deux chiffres 
- Un point  
- Trois chiffres 
- Un point  
- Trois chiffres 
- Un trait d’union  
- Un chiffre de contrôle

Registro de Identidade (RIC) (nouveau format) :
- 10 chiffres  
- Un trait d’union  
- Un chiffre de contrôle

### <a name="checksum"></a>Somme de contrôle

Oui

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
- La fonction Func_brazil_rg trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_brazil_rg est trouvé.
- La somme de contrôle est correcte.

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- La fonction Func_brazil_rg trouve un contenu qui correspond au modèle.
- La somme de contrôle est correcte.

```
<!-- Brazil National ID Card (RG) -->
<Entity id="486de900-db70-41b3-a886-abdf25af119c" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_brazil_rg"/>
     <Match idRef="Keyword_brazil_rg"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_brazil_rg"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordbrazilrg"></a>Keyword_brazil_rg

Cédula de identidade carte d’identité id national número de rregistro registro de Iidentidade registro geral RG (ce mot clé respecte la casse) RIC (ce mot clé respecte la casse) 
   
## <a name="canada-bank-account-number"></a>Numéro de compte bancaire Canada

### <a name="format"></a>Format

Sept ou douze chiffres

### <a name="pattern"></a>Modèle

Un numéro de compte bancaire au Canada est composé de sept ou douze chiffres.

Un numéro de transit de compte bancaire du Canada est indiqué au format suivant :
- Cinq chiffres 
- Un trait d’union  
- Trois chiffres ou
- Un zéro « 0 »  
- Huit chiffres

### <a name="checksum"></a>Somme de contrôle

Non

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
- L’expression régulière Regex_canada_bank_account_number trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_canada_bank_account_number est trouvé.
- L’expression régulière Regex_canada_bank_account_transit_number trouve un contenu qui correspond au modèle.

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
- L’expression régulière Regex_canada_bank_account_number trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_canada_bank_account_number est trouvé.

```
<!-- Canada Bank Account Number -->
<Entity id="552e814c-cb50-4d94-bbaa-bb1d1ffb34de" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Regex_canada_bank_account_number" />
        <Match idRef="Keyword_canada_bank_account_number" />
        <Match idRef="Regex_canada_bank_account_transit_number" />
   </Pattern>
   <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_canada_bank_account_number" />
        <Match idRef="Keyword_canada_bank_account_number" />
   </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordcanadabankaccountnumber"></a>Keyword_canada_bank_account_number

- obligations d’épargne du Canada
- 
agence du revenu du Canada
- 
institution financière du Canada
- 
formulaire de dépôt direct
- 
citoyen canadien
- 
représentant légal
- 
notaire
- 
commissaire à l’assermentation
- 
prestation pour la garde d’enfants
- 
prestation universelle pour la garde d’enfants
- 
prestation fiscale canadienne pour enfants
- 
prestation fiscale pour le revenu gagné
- 
taxe de vente harmonisée
- numéro d’assurance sociale
- 
remboursement d’impôt
- 
prestation fiscale pour enfants
- 
paiements aux territoires
- 
numéro d’institution
- 
demande de dépôt
- 
informations bancaires
- 

dépôt direct
   
## <a name="canada-drivers-license-number"></a>Numéro de permis de conduire Canada

### <a name="format"></a>Format

Varie selon la province

### <a name="pattern"></a>Modèle

Plusieurs modèles pour les différentes provinces : Alberta, Colombie-Britannique, Manitoba, Nouveau-Brunswick, Terre-Neuve-et-Labrador, Nouvelle-Écosse, Ontario, Île-du-Prince-Édouard, Québec et Saskatchewan

### <a name="checksum"></a>Somme de contrôle

Non

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- La fonction Func_[province_name]_drivers_license_number trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_[province_name]_drivers_license_name est trouvé.
- Un mot clé figurant dans la liste Keyword_canada_drivers_license est trouvé.

```
<!-- Canada Driver's License Number -->
    <Entity id="37186abb-8e48-4800-ad3c-e3d1610b3db0" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_alberta_drivers_license_number" />
        <Match idRef="Keyword_alberta_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_british_columbia_drivers_license_number" />
        <Match idRef="Keyword_british_columbia_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_manitoba_drivers_license_number" />
        <Match idRef="Keyword_manitoba_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_new_brunswick_drivers_license_number" />
        <Match idRef="Keyword_new_brunswick_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_newfoundland_labrador_drivers_license_number" />
        <Match idRef="Keyword_newfoundland_labrador_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_nova_scotia_drivers_license_number" />
        <Match idRef="Keyword_nova_scotia_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_ontario_drivers_license_number" />
        <Match idRef="Keyword_ontario_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_prince_edward_island_drivers_license_number" />
        <Match idRef="Keyword_prince_edward_island_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_quebec_drivers_license_number" />
        <Match idRef="Keyword_quebec_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_saskatchewan_drivers_license_number" />
        <Match idRef="Keyword_saskatchewan_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
    </Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordprovincenamedriverslicensename"></a>Keyword_[province_name]_drivers_license_name

- L’abréviation de la province, par exemple AB
- 
Le nom de la province, par exemple Alberta

#### <a name="keywordcanadadriverslicense"></a>Keyword_canada_drivers_license

- PC
- PC
- CDL
- SYSTÈMES CDL
- DriverLic
- DriverLics
- DriverLicense
- DriverLicenses
- DriverLicence
- DriverLicences
- Lic pilote
- Pilote Lics
- Conduire
- Licences de pilote
- Permis de conduire

- Permis de conduire

- DriversLic
- DriversLics
- DriversLicence
- DriversLicences
- Conduire
- DriversLicenses
- Lic pilotes
- Lics pilotes
- Permis de conduire
- Licences de pilotes
- Certificat de pilotes
- Certificats de pilotes
- Driver'Lic
- Driver'Lics
- Driver'License
- Driver'Licenses
- Driver'Licence
- Driver'Licences
- Pilote ' Lic
- Pilote ' Lics
- Pilote ' licence
- Pilote ' licences
- Pilote ' certificat
- Pilote « certificats
- Driver'sLic
- Driver'sLics
- Driver'sLicense
- Driver'sLicenses
- Driver'sLicence
- Driver'sLicences
- Lic du pilote
- Lics permis de conduire
- Conduire permis de
- Conduire permis de
- Permis de conduire

- Permis de conduire

- Permis de Conduire
- id
- ID
- 
numéro carte d’identification
- 
numéros carte d’identification
- 
# carte d’identification
- 
# carte d’identification
- carte idcard
- cartes idcard
- idcard
- numéro d’identification

- numéros d’identification

- # identification

- 
# identification
- carte d’identification
- cartes d’identification
- 
identification
 
- # PC
- 
# PC
 
- # PCD
 
- # PCD
 
- DriverLic # 
- DriverLics # 
- DriverLicense # 
- DriverLicenses # 
- DriverLicence # 
- DriverLicences # 
- #Permis conduire
- 
#Permis conduire
 
- Pilote licence # 
- Licences de pilote # 
- Pilote licence # 
- Pilote certificats # 
- DriversLic # 
- DriversLics # 
- Conduire # 
- DriversLicenses # 
- DriversLicence # 
- DriversLicences # 
- Pilotes Lic # 
- Pilotes Lics # 
- Licence pilotes # 
- Licences pilotes # 
- Licence pilotes # 
- Certificats pilotes # 
- #Permisconduire
 
- #Permisconduire
 
- #Permisdeconduire
 
- #Permisdeconduire
 
- #Permisdeconduire
 
- #Permisdeconduire
 
- #Permis conduire
 
- #Permis conduire
 
- #Permis de conduire
 
- #Permis de conduire
 
- Pilote ' certificat # 
- Pilote « certificats # 
- Driver'sLic # 
- Driver'sLics # 
- Driver'sLicense # 
- Driver'sLicenses # 
- Driver'sLicence # 
- Driver'sLicences # 
- #Permisconduire
 
- #Permisconduire
 
- #Permis de conduire
 
- #Permis de conduire
 
- Certificat de # permis de conduire 
- Certificats de # permis de conduire 
- Permis de Conduire # 
- numéro d’identification 
- ID # 
- #carte carte d’identification
 
- #cartes carte d’identification
 
- #carte d’identification
 
- #carte d’identification
 
- #cartes d’identification
 
- #identification
 
   
## <a name="canada-health-service-number"></a>Numéro de service de santé Canada

### <a name="format"></a>Format

10 chiffres

### <a name="pattern"></a>Modèle

10 chiffres

### <a name="checksum"></a>Somme de contrôle

Non

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- L’expression régulière Regex_canada_health_service_number trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_canada_health_service_number est trouvé.

```
<!-- Canada Health Service Number -->
<Entity id="59c0bf39-7fab-482c-af25-00faa4384c94" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_canada_health_service_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_canada_health_service_number" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordcanadahealthservicenumber"></a>Keyword_canada_health_service_number

- numéro d’assurance-maladie
- 
informations sur le patient
- services de santé
- 
services spécialisés
- 
accident automobile
- 
hôpital pour malades
- 
psychiatre
- 
indemnisation des salariés
- 
handicap
      
## <a name="canada-passport-number"></a>Numéro de passeport Canada

### <a name="format"></a>Format

Deux lettres majuscules suivies de six chiffres

### <a name="pattern"></a>Modèle

Deux lettres majuscules suivies de six chiffres

### <a name="checksum"></a>Somme de contrôle

Non

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- L’expression régulière Regex_canada_passport_number trouve un contenu qui correspond au modèle.
- Un mot clé à partir de Keyword_canada_passport_number ou Keyword_passport est trouvé.

``` 
<!-- Canada Passport Number -->
<Entity id="14d0db8b-498a-43ed-9fca-f6097ae687eb" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_canada_passport_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_canada_passport_number" />
          <Match idRef="Keyword_passport" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordcanadapassportnumber"></a>Keyword_canada_passport_number

- citoyenneté canadienne
- 
passeport canadien
- 
demande de passeport
- 
photos pour passeport
- 
traducteur agréé
- 
citoyens canadiens
- 
temps de traitement
- 

demande de renouvellement

#### <a name="keywordpassport"></a>Keyword_passport

- Numéro de passeport
- 
N° de passeport
- # Passeport

- #Passeport

- IDPassport
- n° passeport

- numéropasseport

- パスポート
- パスポート番号

- パスポートのNum

- パスポート＃

- Numéro de passeport
- 
Passeport n°
- Passeport numéro

- # Passeport

- Passeport#

- PasseportNon
- 

Passeportn °
   
## <a name="canada-personal-health-identification-number-phin"></a>NIMP (numéro d'identification médicale personnel) Canada

### <a name="format"></a>Format

Neuf chiffres

### <a name="pattern"></a>Modèle

Neuf chiffres

### <a name="checksum"></a>Somme de contrôle

Non

### <a name="definition"></a>Définition

Une stratégie DLP est convaincu que ce type d’informations sensibles a été détecté à 75 % if, au sein d’une proximité de 300 caractères : l’expression régulière Regex_canada_phin recherche de contenu qui correspond au modèle. Contient des mots clés au moins deux des Keyword_canada_phin Keyword_canada_provinces...

```
<!-- Canada PHIN -->
<Entity id="722e12ac-c89a-4ec8-a1b7-fea3469f89db" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_canada_phin" />
        <Any minMatches="2">
          <Match idRef="Keyword_canada_phin" />
          <Match idRef="Keyword_canada_provinces" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordcanadaphin"></a>Keyword_canada_phin

- numéro d’assurance sociale
- 
loi sur les renseignements médicaux
- 
renseignements relatifs à l’impôt sur le revenu
- 
santé Manitoba
- 
enregistrement aux services de santé
- 
achats de médicaments sur ordonnance
- 
admissibilité aux prestations
- 
santé personnelle
- 
procuration
- 
numéro d’enregistrement
- numéro d’assurance-maladie
- 
recommandation par le médecin
- 
professionnel de bien-être
- 
orientation d’un patient
- 

santé et bien-être

#### <a name="keywordcanadaprovinces"></a>Keyword_canada_provinces

- Nunavut
- 
Québec
- 
Territoires du Nord-Ouest
- 
Ontario
- 
Colombie-britannique
- 
Alberta
- 
Saskatchewan
- 
Manitoba
- 
Yukon
- 
Terre-Neuve-et-Labrador
- 
Nouveau-Brunswick
- 
Nouvelle-Écosse
- 
Île-du-Prince-Édouard
- Canada
   
## <a name="canada-social-insurance-number"></a>Numéro d'assurance sociale Canada

### <a name="format"></a>Format

Neuf chiffres avec éventuellement des traits d’union ou des espaces

### <a name="pattern"></a>Modèle

Mis en forme :
- Trois chiffres 
- Un trait d’union ou un espace  
- Trois chiffres 
- Un trait d’union ou un espace  
- Trois chiffres

Non formatée : Neuf chiffres

### <a name="checksum"></a>Somme de contrôle

Oui

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
- La fonction Func_canadian_sin trouve un contenu qui correspond au modèle.
- Au moins deux des éléments suivants, quelle que soit la combinaison :
    - Un mot clé figurant dans la liste Keyword_sin est trouvé.
    - Un mot clé figurant dans la liste Keyword_sin_collaborative est trouvé.
    - La fonction Func_eu_date trouve une date au format correct.
- La somme de contrôle est correcte.

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- La fonction Func_unformatted_canadian_sin trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_sin est trouvé.
- La somme de contrôle est correcte.

```
<!-- Canada Social Insurance Number -->
<Entity id="a2f29c85-ecb8-4514-a610-364790c0773e" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_canadian_sin" />
        <Any minMatches="2">
          <Match idRef="Keyword_sin" />
          <Match idRef="Keyword_sin_collaborative" />
          <Match idRef="Func_eu_date" />
        </Any>
  </Pattern>
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_unformatted_canadian_sin" />
        <Match idRef="Keyword_sin" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordsin"></a>Keyword_sin

- sin 
- assurance sociale
 
- numéro d’assurance sociale
 
- assoc
 
- ssn 
- sécurité sociale. 
- sécurité sociale 
- numéro d’assurance sociale
 
- numéro d’identification nationale 
- 
id national 
- # assoc
 
- ass soc
 
- ass sociale
 

#### <a name="keywordsincollaborative"></a>Keyword_sin_collaborative

- driver’s license 
- drivers license 
- conduire permis de 
- permis de conduire 
- DDN
 
- Birthdate 
- Anniversaire  
- Date of Birth
 
   
## <a name="chile-identity-card-number"></a>	Numéro de carte d’identité Chili

### <a name="format"></a>Format

7-8 chiffres plus délimiteurs un chiffre de contrôle ou d’une lettre

### <a name="pattern"></a>Modèle

7 ou 8 chiffres, plus des délimiteurs :
- 1 ou 2 chiffres  
- Un point  
- Trois chiffres 
- Un point  
- Trois chiffres 
- Un tiret 
- Un chiffre ou une lettre (ne respectant pas la casse) de contrôle

### <a name="checksum"></a>Somme de contrôle

Oui

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
- La fonction Func_chile_id_card trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_chile_id_card est trouvé.
- La somme de contrôle est correcte.

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- La fonction Func_chile_id_card trouve un contenu qui correspond au modèle.
- La somme de contrôle est correcte.

```
<!-- Chile Identity Card Number -->
<Entity id="4e979794-49a0-407e-a0b9-2c536937b925" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_chile_id_card"/>
     <Match idRef="Keyword_chile_id_card"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_chile_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordchileidcard"></a>Keyword_chile_id_card

- National Identification Number
 
- Identity card 
- ID 
- Identification 
- Rol Único Nacional
 
- EXÉCUTER 
- Rol Único Tributario
 
- RUT
 
- Cédula de Identidad
 
- Número De Identificación Nacional
 
- Tarjeta de identificación
 
- Identificación
 
   
## <a name="china-resident-identity-card-prc-number"></a>	Numéro de carte d’identité de résident Chine (RPC)

### <a name="format"></a>Format

18 chiffres

### <a name="pattern"></a>Modèle

18 chiffres :
- Six chiffres qui composent un code d’adresse  
- Huit chiffres sous la forme AAAAMMJJ qui correspondent à la date de naissance  
- Trois chiffres qui correspondent à un code d’opération  
- Un chiffre de contrôle

### <a name="checksum"></a>Somme de contrôle

Oui

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
- La fonction Func_china_resident_id trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_china_resident_id est trouvé.
- La somme de contrôle est correcte.

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- La fonction Func_china_resident_id trouve un contenu qui correspond au modèle.
- La somme de contrôle est correcte.

```
<!-- China Resident Identity Card (PRC) Number -->
<Entity id="c92daa86-2d16-4871-901f-816b3f554fc1" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_china_resident_id"/>
     <Match idRef="Keyword_china_resident_id"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_china_resident_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

### <a name="keywordchinaresidentid"></a>Keyword_china_resident_id

- Resident Identity Card
 
- PRC
 
- National Identification Card
 
- 身份证  
- 居民 身份证  
- 居民身份证
 
- 鉴定

 
- 身分證  
- 居民 身份證
- 鑑定  
   
## <a name="credit-card-number"></a>Numéro de carte de crédit

### <a name="format"></a>Format

16 chiffres qui peuvent être mis en forme ou non mis en forme (dddddddddddddddd) et doit réussir le test Luhn.

### <a name="pattern"></a>Modèle

Modèle très complexe et puissant qui détecte les cartes de visite de toutes les principales marques du monde, notamment Visa, MasterCard, Discover Card, JCB, American Express, etc.

### <a name="checksum"></a>Somme de contrôle

Oui, la somme de contrôle de Luhn

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
- La fonction Func_credit_card trouve un contenu qui correspond au modèle.
- L’une des affirmations suivantes est vraie :
    - Un mot clé figurant dans la liste Keyword_cc_verification est trouvé.
    - Un mot clé figurant dans la liste Keyword_cc_name est trouvé.
    - La fonction Func_expiration_date trouve une date au format correct.
- La somme de contrôle est correcte.

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :
- La fonction Func_credit_card trouve un contenu qui correspond au modèle.
- La somme de contrôle est correcte.

```
<!-- Credit Card Number -->
<Entity id="50842eb7-edc8-4019-85dd-5a5c1f2bb085" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_credit_card" />
        <Any minMatches="1">
          <Match idRef="Keyword_cc_verification" />
          <Match idRef="Keyword_cc_name" />
          <Match idRef="Func_expiration_date" />
        </Any>
  </Pattern>
  <Pattern confidenceLevel="65">
        <IdMatch idRef="Func_credit_card" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordccverification"></a>Keyword_cc_verification

- vérification de la carte
- numéro d’identification de la carte
- nvc

- nic

- CVC2
- VVC2
- pin block

- code de sécurité

- numéro de sécurité

- n° de sécurité

- numéro d’émission

- n° d’émission

- cryptogramme

- numéro de sécurité

- numéro de sécurité

- kreditkartenprüfnummer

- kreditkartenprufnummer

- prüfziffer

- prufziffer

- sicherheits Kode
- sicherheitscode

- sicherheitsnummer

- verfalldatum

- codice di verifica

- cod. sicurezza

- remboursement sicurezza
- 
n autorizzazione
- código

- codigo

- cod. seg

- segment de remboursement
- código de segurança

- codigo de seguranca

- codigo de segurança

- código de seguranca

- cód. Segurança

- remboursement. CR seguranca. Segurança
- cód. seguranca

- cód segurança
- cabillaud seguranca CR segurança
- cód seguranca
- número de verificação

- numero de verificacao

- ablauf

- gültig bis

- gültigkeitsdatum

- gultig bis

- gultigkeitsdatum

- scadenza

- data scad

- fecha de expiracion

- fecha de venc

- vencimiento

- válido hasta

- valido hasta

- vto

- data de expiração

- data de expiracao

- data em que expira

- validade

- valor

- vencimento

- Venc 

#### <a name="keywordccname"></a>Keyword_cc_name

- amex
- 
american express
- americanexpress

- Visa
- mastercard

- master card

- 
mc
 
- mastercards
- 
master cards
- Club de dîner
- diners club

- dinersclub

- discover card

- discovercard

- discover cards

- JCB
- japanese card bureau

- carte blanche

- carteblanche

- carte de crédit

- cc #
- cc #:
- 
date d’expiration
- date d’exp

- 
date d’expiration
- 
date d’expiration
- 
date d’exp
- 
date expiration
- carte bancaire

- 
carte bancaire
- numéro de carte

- num de carte

- numéro de carte

- numéros de carte

- numéros de carte

- carte de crédit

- cartes de crédit

- cartes de crédit

- ncc

- titulaire de la carte

- titulaire de la carte

- titulaires de la carte

- titulaires de la carte

- carte de vérification

- carte de vérification

- cartes de vérification

- cartes de vérification

- carte de débit

- carte de débit

- cartes de débit

- cartes de débit

- carte de retrait

- carte de retrait

- cartes de retrait

- cartes de retrait

- 
enroute
- 
en route
- type de carte

- carte bancaire

- carte de crédit

- carte de credit

- numéro de carte

- numero de carte

- nº de la carte

- nº de carte

- kreditkarte

- karte

- karteninhaber

- karteninhabers
- kreditkarteninhaber

- kreditkarteninstitut

- kreditkartentyp

- eigentümername

- 
kartennr
 
- kartennummer
- 
kreditkartennummer
- kreditkarten-nummer
- Carta di credito

- Carta credito

- Carta
- carta n
- nr. carta

- nr carta
- numero carta

- numero della carta

- numero di carta

- tarjeta credito

- tarjeta de credito

- 
tarjeta crédito
- 
tarjeta de crédito
- tarjeta de atm

- tarjeta atm

- tarjeta debito

- tarjeta de debito

- 
tarjeta débito
- 
tarjeta de débito
- nº de tarjeta

- no. de tarjeta

- Aucun tarjeta de
- numero de tarjeta

- número de tarjeta

- tarjeta no

- tarjetahabiente

- cartão de crédito

- cartão de credito

- cartao de crédito

- cartao de credito

- cartão de débito

- cartao de débito

- cartão de debito

- cartao de debito

- débito automático
- debito automatico

- 
número do cartão
- 
numero do cartão
 
- número do cartao
- 
numero do cartao
- número de cartão

- numero de cartão

- número de cartao

- numero de cartao

- Nº cartão
- nº do cartao

- nº. do cartão

- Aucun cartão
- Aucun cartao
- no. do cartão

- 
no. do cartao
 
   
## <a name="croatia-identity-card-number"></a>Numéro de carte d’identité croate

### <a name="format"></a>Format

Neuf chiffres

### <a name="pattern"></a>Modèle

Neuf chiffres consécutifs

### <a name="checksum"></a>Somme de contrôle

Non

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- La fonction Func_croatia_id_card trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_croatia_id_card est trouvé.

```
<!--Croatia Identity Card Number-->
<Entity id="ff12f884-c20a-4189-b185-34c8e7258d47" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_croatia_id_card"/>
     <Match idRef="Keyword_croatia_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordcroatiaidcard"></a>Keyword_croatia_id_card

- Croatian identity card
- Osobna iskaznica

   
## <a name="croatia-personal-identification-oib-number"></a>	Numéro d’identification personnel (OIB) Croatie

### <a name="format"></a>Format

10 chiffres

### <a name="pattern"></a>Modèle

10 chiffres :
- Six chiffres sous la forme JJMMAA qui correspondent à la date de naissance  
- Quatre chiffres où le dernier chiffre est un chiffre de contrôle

### <a name="checksum"></a>Somme de contrôle

Oui

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
- La fonction Func_croatia_oib_number trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_croatia_oib_number est trouvé.
- La somme de contrôle est correcte.

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- La fonction Func_croatia_oib_number trouve un contenu qui correspond au modèle.
- La somme de contrôle est correcte.

```
<!-- Croatia Personal Identification (OIB) Number -->
<Entity id="31983b6d-db95-4eb2-a630-b44bd091968d" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_croatia_oib_number"/>
     <Match idRef="Keyword_croatia_oib_number"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_croatia_oib_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordcroatiaoibnumber"></a>Keyword_croatia_oib_number

- Personal Identification Number
- Osobni identifikacijski broj
 
- OIB
 

   
## <a name="czech-national-identity-card-number"></a>Numéro de carte d’identité nationale tchèque

### <a name="format"></a>Format

10 chiffres contenant une barre oblique

### <a name="pattern"></a>Modèle

10 chiffres :
- Six chiffres correspondant à la date de naissance  
- Une barre oblique  
- Quatre chiffres où le dernier chiffre est un chiffre de contrôle

### <a name="checksum"></a>Somme de contrôle

Oui

### <a name="definition"></a>Définition

Une stratégie DLP est de 85 % convaincu que ce type d’informations sensibles a été détecté if, au sein d’une proximité de 300 caractères : la fonction Func_czech_id_card recherche le contenu qui correspond au modèle. Un mot clé à partir de Keyword_czech_id_card est trouvé. Passe de la somme de contrôle.

```
<!-- Czech National Identity Card Number -->
<Entity id="60c0725a-4eb6-455b-9dda-05d8a7396497" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_czech_id_card"/>
     <Match idRef="Keyword_czech_id_card"/>
  </Pattern>
</Entity>
```


### <a name="keywords"></a>Mots clés

- Keyword_czech_id_card
- Czech national identity card
- Občanský průka
   
## <a name="denmark-personal-identification-number"></a>	Numéro d’identification personnel Danemark

### <a name="format"></a>Format

10 chiffres contenant un trait d’union

### <a name="pattern"></a>Modèle

10 chiffres :
- Six chiffres au format JJMMAA qui correspondent à la date de naissance  
- Un trait d’union  
- Quatre chiffres où le dernier chiffre est un chiffre de contrôle

### <a name="checksum"></a>Somme de contrôle

Oui

### <a name="definition"></a>Définition

Une stratégie DLP est convaincu que ce type d’informations sensibles a été détecté à 75 % if, au sein d’une proximité de 300 caractères : l’expression régulière Regex_denmark_id recherche de contenu qui correspond au modèle. Un mot clé à partir de Keyword_denmark_id est trouvé. Passe de la somme de contrôle.

```
<!-- Denmark Personal Identification Number -->
<Entity id="6c4f2fef-56e1-4c00-8093-88d7a01cf460" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_denmark_id"/>
     <Match idRef="Keyword_denmark_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keyworddenmarkid"></a>Keyword_denmark_id

- Personal Identification Number
- CPR
- Det Centrale Personregister
- Personnummer
   
## <a name="drug-enforcement-agency-dea-number"></a>Numéro de la Drug Enforcement Agency (DEA)

### <a name="format"></a>Format

Deux lettres suivies de sept chiffres

### <a name="pattern"></a>Modèle

Le modèle doit inclure tous les éléments suivants :
- Une lettre (ne respecte pas la casse) à partir de cet ensemble de lettres possibles : abcdefghjklmnprstux, qui est un code d’utilisateur enregistré 
- Une lettre (ne respecte pas la casse), qui est la première lettre du nom de l’utilisateur enregistré 
- Sept chiffres, le dernier est le chiffre de contrôle

### <a name="checksum"></a>Somme de contrôle

Oui

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
- La fonction Func_dea_number trouve un contenu qui correspond au modèle.
- La somme de contrôle est correcte.

```
<!-- DEA Number -->
<Entity id="9a5445ad-406e-43eb-8bd7-cac17ab6d0e4" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_dea_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

Aucun

   
## <a name="eu-debit-card-number"></a>Numéro de carte de débit Union européenne

### <a name="format"></a>Format

16 chiffres

### <a name="pattern"></a>Modèle

Modèle très complexe et puissant

### <a name="checksum"></a>Somme de contrôle

Oui

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
- La fonction Func_eu_debit_card trouve un contenu qui correspond au modèle.
- Au moins une des affirmations suivantes est vraie :
    - Un mot clé figurant dans la liste Keyword_eu_debit_card est trouvé.
    - Un mot clé figurant dans la liste Keyword_card_terms_dict est trouvé.
    - Un mot clé figurant dans la liste Keyword_card_security_terms_dict est trouvé.
    - Un mot clé figurant dans la liste Keyword_card_expiration_terms_dict est trouvé.
    - La fonction Func_expiration_date trouve une date au format correct.
- La somme de contrôle est correcte.

```
    <!-- EU Debit Card Number -->
    <Entity id="0e9b3178-9678-47dd-a509-37222ca96b42" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_eu_debit_card" />
        <Any minMatches="1">
          <Match idRef="Keyword_eu_debit_card" />
          <Match idRef="Keyword_card_terms_dict" />
          <Match idRef="Keyword_card_security_terms_dict" />
          <Match idRef="Keyword_card_expiration_terms_dict" />
          <Match idRef="Func_expiration_date" />
        </Any>
      </Pattern>
    </Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordeudebitcard"></a>Keyword_eu_debit_card

- numéro de compte 
- numéro de carte
 
- n° carte
 
- numéro de sécurité
 
- cc # 

#### <a name="keywordcardtermsdict"></a>Keyword_card_terms_dict

- num de compte
 
- num de compte
 
- n° compte
 
- american express
 
- americanexpress
 
- americano espresso
 
- amex 
- carte de retrait
 
- cartes de retrait
 
- atm kaart
 
- carte de retrait
 
- cartes de retrait
 
- atmkaart
 
- atmkaarten
 
- bancontact
 
- carte bancaire
 
- bankkaart
 
- titulaire de la carte
 
- titulaires de la carte
 
- num de carte
 
- numéro de carte
 
- numéros de carte
 
- type de carte
 
- cardano numerico
 
- titulaire de la carte
 
- titulaires de la carte
 
- numéro de carte
 
- numéros de carte
 
- carta bianca
 
- Carta credito
 
- Carta di credito
 
- cartao de credito
 
- cartao de crédito
 
- cartao de debito
 
- cartao de débito
 
- carte bancaire
 
- carte blanche
 
- carte bleue
 
- carte de credit
 
- carte de crédit
 
- carte di credito
 
- carteblanche
 
- cartão de credito
 
- cartão de crédito
 
- cartão de debito
 
- cartão de débito
 
- cb
 
- ncc
 
- carte de vérification
 
- cartes de vérification
 
- carte de vérification

- cartes de vérification
 
- chequekaart
 
- cirrus
 
- cirrus-edc-maestro
 
- controlekaart
 
- controlekaarten
 
- carte de crédit
 
- cartes de crédit
 
- carte de crédit
 
- cartes de crédit
 
- debetkaart
 
- debetkaarten
 
- carte de débit
 
- cartes de débit
 
- carte de débit
 
- cartes de débit
 
- debito automatico
 
- diners club
 
- dinersclub
 
- découvrir 
- discover card
 
- discover cards
 
- discovercard
 
- discovercards
 
- débito automático
- 
edc
 
- eigentümername
 
- carte de crédit européenne
 
- hoofdkaart
 
- hoofdkaarten
 
- in viaggio
 
- japanese card bureau
 
- japanse kaartdienst
 
- jcb
 
- kaart
 
- kaart num
 
- kaartaantal
 
- kaartaantallen
 
- kaarthouder
 
- kaarthouders
 
- karte
  
- karteninhaber
 
- karteninhabers
- 
kartennr
 
- kartennummer 
- kreditkarte
 
- kreditkarten-nummer 
- kreditkarteninhaber
 
- kreditkarteninstitut
 
- kreditkartennummer
 
- kreditkartentyp
 
- maestro
 
- master card
 
- master cards
 
- mastercard
 
- mastercards 
- MC 
- mister cash
 
- carta n 
- Carta 
- Aucun tarjeta de 
- Aucun cartao 
- Aucun cartão 
- no. de tarjeta
 
- no. do cartao
 
- no. do cartão
 
- nr carta 
- nr. carta
 
- numeri di scheda
 
- numero carta
 
- numero de cartao
 
- numero de carte
 
- numero de cartão
 
- numero de tarjeta

- numero della carta
 
- numero di carta
 
- numero di scheda
 
- numero do cartao
 
- numero do cartão
 
- numéro de carte
 
- nº carta
 
- nº de carte
 
- nº de la carte
 
- nº de tarjeta
 
- nº do cartao
 
- Nº cartão 
- nº. do cartão
 
- número de cartao
 
- número de cartão
 
- número de tarjeta
 
- número do cartao 
- scheda dell’assegno
 
- scheda dell’atmosfera
 
- scheda dell’atmosfera
 
- scheda della banca
 
- scheda di controllo
 
- scheda di debito
 
- scheda matrice
 
- schede dell’atmosfera
 
- schede di controllo
 
- schede di debito
 
- schede matrici
 
- scoprono la scheda
 
- scoprono le schede
 
- solo
 
- supporti di scheda
 
- supporto di scheda
 
- commutateur 
- tarjeta atm
 
- tarjeta credito
 
- tarjeta de atm
 
- tarjeta de credito
 
- tarjeta de debito
 
- tarjeta debito
 
- tarjeta no

- tarjetahabiente
 
- tipo della scheda
 
- ufficio giapponese della 
- scheda
 
- v pay
 
- v-paie 
- visa
 
- visa plus
 
- visa electron
 
- visto
 
- visum
 
- vpay
   

#### <a name="keywordcardsecuritytermsdict"></a>Keyword_card_security_terms_dict

- numéro d’identification de la carte
- vérification de la carte 
- cardi la verifica
 
- nic
 
- segment de remboursement 
- remboursement seguranca 
- remboursement segurança 
- remboursement sicurezza 
- cod. seg
 
- cod. seguranca
 
- cod. segurança
 
- cod. sicurezza
 
- codice di sicurezza
 
- codice di verifica
 
- codigo
 
- codigo de seguranca
 
- codigo de segurança
 
- crittogramma
 
- cryptogramme
 
- cryptogramme
 
- CV2 
- cvc
 
- CVC2 
- nvc
 
- cvv
 
- VVC2 
- cód seguranca 
- cód segurança 
- cód. seguranca
 
- cód. Segurança
 
- código
 
- código de seguranca
 
- código de segurança
 
- de kaart controle
 
- geeft nr suit
 
- n° d’émission
 
- numéro d’émission
 
- kaartidentificatienummer
 
- kreditkartenprufnummer
 
- kreditkartenprüfnummer
 
- kwestieaantal
 
- no. dell’edizione
 
- no. di sicurezza
 
- numéro de sécurité
 
- numero de verificacao
 
- numero dell’edizione
 
- numero di identificazione della 
- scheda
 
- numero di sicurezza
 
- numero van veiligheid
 
- numéro de sécurité
 
- nº autorizzazione
 
- número de verificação
 
- perno il blocco
 
- pin block
 
- prufziffer
 
- prüfziffer
 
- code de sécurité
 
- n° de sécurité
 
- numéro de sécurité
 
- sicherheits kode
 
- sicherheitscode
 
- sicherheitsnummer
 
- speldblok
 
- veiligheid nr
 
- veiligheidsaantal
 
- veiligheidscode
 
- veiligheidsnummer
 
- verfalldatum
 

#### <a name="keywordcardexpirationtermsdict"></a>Keyword_card_expiration_terms_dict

- ablauf
 
- data de expiracao
 
- data de expiração
 
- data del exp
 
- data di exp
 
- data di scadenza
 
- data em que expira
 
- data scad
 
- data scadenza
 
- date de validité
 
- datum afloop
 
- datum van exp
 
- de afloop
 
- espira
 
- espira
 
- date d’exp
 
- exp datum
 
- expiration 
- expire
 
- expire
 
- expiration
 
- fecha de expiracion
 
- fecha de venc
 
- gultig bis
 
- gultigkeitsdatum
 
- gültig bis
 
- gültigkeitsdatum
 
- la scadenza
 
- scadenza
 
- valable
 
- validade
 
- valido hasta
 
- valor
 
- venc
 
- vencimento
 
- vencimiento
 
- verloopt
 
- vervaldag
 
- vervaldatum
 
- vto
 
- válido hasta
 
   
## <a name="eu-drivers-license-number"></a>Numéro de permis de conduire l’Union européenne

Pour plus d’informations, voir le [type d’informations sensibles numéro de permis de conduire l’Union européenne](eu-driver-s-license-number.md).
  
## <a name="eu-national-identification-number"></a>Numéro d’Identification nationales de l’UE

Pour plus d’informations, voir le [type d’informations sensibles National numéro d’Identification de l’UE](eu-national-identification-number.md).
  
## <a name="eu-passport-number"></a>Numéro de passeport UE

Pour plus d’informations, voir le [numéro de passeport UE type d’informations sensibles](eu-passport-number.md).
  
## <a name="eu-social-security-number-or-equivalent-id"></a>ID de numéro de sécurité sociale de l’Union européenne ou équivalent

Pour plus d’informations, voir [numéro de sécurité sociale de l’Union européenne ou type d’informations sensibles ID équivalente](eu-social-security-number-or-equivalent-id.md).
  
## <a name="eu-tax-identification-number"></a>Numéro d’Identification de l’UE taxe

Pour plus d’informations, voir [type d’informations sensibles numéro d’Identification de taxe de l’UE](eu-tax-identification-number.md).
  
## <a name="finland-national-id"></a>ID national finlandais

### <a name="format"></a>Format

Six chiffres plus un caractère indiquant un siècle plus trois chiffres plus un chiffre de contrôle

### <a name="pattern"></a>Modèle

Le modèle doit inclure tous les éléments suivants :
- Six chiffres au format JJMMAA qui représentent la date de naissance 
- Marqueur de siècle (soit « - », « + » ou « a ») 
- Numéro d’identification personnel à trois chiffres 
- Un chiffre ou une lettre (ne respectant pas la casse) de contrôle

### <a name="checksum"></a>Somme de contrôle

Oui

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
- La fonction Func_finnish_national_id trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_finnish_national_id est trouvé.
- La somme de contrôle est correcte.

```
<!-- Finnish National ID-->
<Entity id="338FD995-4CB5-4F87-AD35-79BD1DD926C1" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finnish_national_id" />
          <Match idRef="Keyword_finnish_national_id" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

- Keyword_finnish_national_id
- 

Sosiaaliturvatunnus
- SOTU Henkilötunnus HETU
- Personbeteckning
- Personnummer
   
## <a name="finland-passport-number"></a>Numéro de passeport Finlande

Combinaison de lettres et de chiffres motif combinaison de lettres et chiffres de neuf neuf de format : stratégie de somme de contrôle non définition A DLP deux lettres (non sensible à la casse) sept chiffres est 75 % convaincu que ce type d’informations sensibles a été détecté si, dans un proximité de 300 caractères : l’expression régulière Regex_finland_passport_number recherche de contenu qui correspond au modèle. Un mot clé à partir de Keyword_finland_passport_number est trouvé. <!-- Finland Passport Number --> 
 <Entity id="d1685ac3-1d3a-40f8-8198-32ef5669c7a5" recommendedConfidence="75" patternsProximity="300"> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_finland_passport_number"/> <Match idRef="Keyword_finland_passport_number"/> </Pattern> 
 </Entity> REUSSITE de passeport Keyword_finland_passport_number mots clés
   
## <a name="france-drivers-license-number"></a>Numéro de permis de conduire France

### <a name="format"></a>Format

12 chiffres

### <a name="pattern"></a>Modèle

12 chiffres avec validation pour écarter les modèles similaires, comme les numéros de téléphone français

### <a name="checksum"></a>Somme de contrôle

Non

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- La fonction Func_french_drivers_license trouve un contenu qui correspond au modèle.
- Au moins une des affirmations suivantes est vraie :
- Un mot clé figurant dans la liste Keyword_french_drivers_license est trouvé.
- La fonction Func_eu_date trouve une date au format correct.

```
<!-- France Driver's License Number -->
<Entity id="18e55a36-a01b-4b0f-943d-dc10282a1824" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_french_drivers_license" />
        <Any minMatches="1">
          <Match idRef="Keyword_french_drivers_license" />
          <Match idRef="Func_eu_date" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordfrenchdriverslicense"></a>Keyword_french_drivers_license

- permis de conduire
- drivers license
- permis de conduire

- permis de conduire
- 
permis de conduire
- 
numéro de permis
- 
numéro de permis
- 
numéros de permis
- 

numéros de permis

## <a name="france-national-id-card-cni"></a>Carte nationale d'identité (CNI) France

### <a name="format"></a>Format

12 chiffres

### <a name="pattern"></a>Modèle

12 chiffres

### <a name="checksum"></a>Somme de contrôle

Non

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :
- L’expression régulière Regex_france_cni trouve un contenu qui correspond au modèle.

```
<!-- France CNI -->
<Entity id="f741ac74-1bc0-4665-b69b-f0c7f927c0c4" patternsProximity="300" recommendedConfidence="65">
  <Pattern confidenceLevel="65">
        <IdMatch idRef="Regex_france_cni" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

Aucun
   
## <a name="france-passport-number"></a>Numéro de passeport France

### <a name="format"></a>Format

Neuf chiffres et lettres

### <a name="pattern"></a>Modèle

Neuf chiffres et lettres :
- Deux chiffres 
- Deux lettres (ne respectant pas la casse)  
- Cinq chiffres

### <a name="checksum"></a>Somme de contrôle

Non

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- La fonction Func_fr_passport trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_passport est trouvé.

```
<!-- France Passport Number -->
<Entity id="3008b884-8c8c-4cd8-a289-99f34fc7ff5d" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_fr_passport" />
        <Match idRef="Keyword_passport" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordpassport"></a>Keyword_passport

- Numéro de passeport
- 
N° de passeport
- # Passeport

- #Passeport

- IDPassport
- n° passeport

- numéropasseport

- パスポート
- パスポート番号

- パスポートのNum

- 
パスポート＃
 
- Numéro de passeport
- 
Passeport n°
- Passeport numéro

- # Passeport

- Passeport#

- PasseportNon
- 

Passeportn °

      
## <a name="france-social-security-number-insee"></a>Numéro de sécurité sociale (INSEE) France

### <a name="format"></a>Format

15 chiffres

### <a name="pattern"></a>Modèle

Doit correspondre à l’un des deux modèles suivants :
- 13 chiffres suivis d’un espace suivi de deux chiffres</br>
ou
- 15 chiffres consécutifs

### <a name="checksum"></a>Somme de contrôle

Oui

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 95 % si, dans une proximité de 300 caractères :
- La fonction Func_french_insee ou Func_fr_insee recherche de contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_fr_insee est trouvé.
- La somme de contrôle est correcte.

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
- La fonction Func_french_insee ou Func_fr_insee recherche de contenu qui correspond au modèle.
- Aucun mot clé figurant dans la liste Keyword_fr_insee n’est trouvé.
- La somme de contrôle est correcte.

```
<!-- France INSEE -->
<Entity id="71f62b97-efe0-4aa1-aa49-e14de253619d" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="95">
        <IdMatch idRef="Func_french_insee" />
        <Match idRef="Func_fr_insee" />
        <Any minMatches="1">
          <Match idRef="Keyword_fr_insee" />
        </Any>
  </Pattern>
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_french_insee" />
        <Match idRef="Func_fr_insee" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_fr_insee" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordfrinsee"></a>Keyword_fr_insee

- insee
- 
securité sociale
- 
securite sociale
- 
id national
- 
numéro d’identification nationale
- 
numéro d’identité
- Aucun d'identité
- 
n° d’identité
- 
numéro d’identité
- Aucun d'identite
- 
n° d’identité
- numéro de sécurité sociale

- 
code de sécurité sociale
- numéro d’assurance sociale
- 
le numéro d’identification nationale
- 
d’identité nationale
- 
numéro de sécurité sociale
- 
le code de la sécurité sociale
- 
numéro d’assurance sociale
- 
numéro de sécu
- 
code sécu
 
   
## <a name="german-drivers-license-number"></a>Numéro de permis de conduire Allemagne

### <a name="format"></a>Format

Combinaison de 11 chiffres et lettres

### <a name="pattern"></a>Modèle

11 chiffres et lettres (ne respectent pas la casse) :
- Un chiffre ou une lettre 
- Deux chiffres 
- Six chiffres ou lettres 
- Un chiffre 
- Un chiffre ou une lettre

### <a name="checksum"></a>Somme de contrôle

Oui

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- La fonction Func_german_drivers_license trouve un contenu qui correspond au modèle.
- Au moins une des affirmations suivantes est vraie :
    - Un mot clé figurant dans la liste Keyword_german_drivers_license_number est trouvé.
    - Un mot clé figurant dans la liste Keyword_german_drivers_license_collaborative est trouvé.
    - Un mot clé figurant dans la liste Keyword_german_drivers_license est trouvé.
- La somme de contrôle est correcte.

```
<!-- German Driver's License Number -->
<Entity id="91da9335-1edb-45b7-a95f-5fe41a16c63c" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_german_drivers_license" />
        <Any minMatches="1">
          <Match idRef="Keyword_german_drivers_license_number" />
          <Match idRef="Keyword_german_drivers_license_collaborative" />
          <Match idRef="Keyword_german_drivers_license" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordgermandriverslicensenumber"></a>Keyword_german_drivers_license_number

- Führerschein
- 
Fuhrerschein
- Fuehrerschein
- 
Führerscheinnummer
- 
Fuhrerscheinnummer
- 
Fuehrerscheinnummer
- 
Führerschein-
 
- Fuhrerschein-
 
- Fuehrerschein-
 
- FührerscheinnummerNr
- FuhrerscheinnummerNr
- FuehrerscheinnummerNr
- FührerscheinnummerKlasse
- FuhrerscheinnummerKlasse
- FuehrerscheinnummerKlasse
- Führerschein - Nr

- Fuhrerschein - Nr

- Fuehrerschein - Nr
 
- Führerschein - Klasse
 
- Fuhrerschein - Klasse
 
- Fuehrerschein - Klasse
- FührerscheinnummerNr 
- FuhrerscheinnummerNr 
- FuehrerscheinnummerNr 
- FührerscheinnummerKlasse 
- FuhrerscheinnummerKlasse 
- FuehrerscheinnummerKlasse 
- Führerschein - Nr
 
- Fuhrerschein - Nr
 
- Fuehrerschein - Nr
 
- Führerschein - Klasse
 
- Fuhrerschein - Klasse
 
- Fuehrerschein - Klasse 
- PC 
- PC
- 
Permis conduire
 
- Permis conduire
 
- Permis de conduire
- 
Permis de conduire
 
- Permis de conduire
 
- Permis de conduire
 
- Permis conduire
 
- Permis conduire
 
- Conduire 
- Licences de pilote 
- Permis de conduire
 
- Permis de conduire
 
- Lic pilotes 
- Licen pilotes 
- Permis de conduire 
- Licences de pilotes 
- Certificat de pilotes 
- Certificats de pilotes 
- Lic du pilote 
- Permis de conduire
 
- Conduire permis de 
- Conduire permis de 
- Permis de conduire
 
- Permis de conduire
 
- Permis conduire
 
- Permis conduire
 
- Permis de conduire
 
- Permis de conduire
 
- Permis de conduire

 
- Permis de conduire

#### <a name="keywordgermandriverslicensecollaborative"></a>Keyword_german_drivers_license_collaborative

- 
Nr-Führerschein
 
- Nr-Fuhrerschein
 
- Nr-Fuehrerschein
 
- No-Führerschein
 
- No-Fuhrerschein
 
- No-Fuehrerschein
 
- N-Führerschein
 
- N-Fuhrerschein
 
- N-Fuehrerschein
- 
Nr-Führerschein
 
- Nr-Fuhrerschein
 
- Nr-Fuehrerschein
 
- No-Führerschein
 
- No-Fuhrerschein
 
- No-Fuehrerschein
 
- N-Führerschein
 
- N-Fuhrerschein
 
- N-Fuehrerschein 

#### <a name="keywordgermandriverslicense"></a>Keyword_german_drivers_license

- ausstellungsdatum
- 
ausstellungsort
- 
ausstellende behöde
- 
ausstellende behorde
- 

ausstellende behoerde
   
## <a name="german-passport-number"></a>Numéro de passeport Allemagne

### <a name="format"></a>Format

10 chiffres ou lettres

### <a name="pattern"></a>Modèle

Le modèle doit inclure tous les éléments suivants :
- Le premier caractère est un chiffre ou une lettre de cet ensemble (C, F, G, H, J, K) 
- Trois chiffres 
- Cinq chiffres ou lettres à partir de cet ensemble (C, -H, J-N, P, R, T, V-Z) 
- Un chiffre

### <a name="checksum"></a>Somme de contrôle

Oui

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
- La fonction Func_german_passport trouve un contenu qui correspond au modèle.
- Un mot clé présent dans l’une des cinq listes de mots clés est trouvé.
- La somme de contrôle est correcte.

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- La fonction Func_german_passport_data trouve un contenu qui correspond au modèle.
- Un mot clé présent dans l’une des cinq listes de mots clés est trouvé.
- La somme de contrôle est correcte.

```
<!-- German Passport Number -->
<Entity id="2e3da144-d42b-47ed-b123-fbf78604e52c" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_german_passport" />
        <Any minMatches="1">
          <Match idRef="Keyword_german_passport" />
          <Match idRef="Keyword_german_passport_collaborative" />
          <Match idRef="Keyword_german_passport_number" />
          <Match idRef="Keyword_german_passport1" />
          <Match idRef="Keyword_german_passport2" />
        </Any>
  </Pattern>
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_german_passport_data" />
        <Any minMatches="1">
          <Match idRef="Keyword_german_passport" />
          <Match idRef="Keyword_german_passport_collaborative" />
          <Match idRef="Keyword_german_passport_number" />
          <Match idRef="Keyword_german_passport1" />
          <Match idRef="Keyword_german_passport2" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordgermanpassport"></a>Keyword_german_passport

- reisepass
- 
reisepasse
- 
reisepassnummer
- passeport
- 

passports

#### <a name="keywordgermanpassportcollaborative"></a>Keyword_german_passport_collaborative

- geburtsdatum
- ausstellungsdatum
- 
ausstellungsort

#### <a name="keywordgermanpassportnumber"></a>Keyword_german_passport_number

Non-Nr Reisepass-Reisepass

#### <a name="keywordgermanpassport1"></a>Keyword_german_passport1

Reisepass-Nr


#### <a name="keywordgermanpassport2"></a>Keyword_german_passport2

bnationalit.t
   
## <a name="germany-identity-card-number"></a>Numéro de carte d’identité allemand

### <a name="format"></a>Format

Depuis le 1er novembre 2010 : neuf lettres et chiffres

À partir du 1er avril 1987 jusqu'à 31 octobre 2010:10 chiffres

### <a name="pattern"></a>Modèle

Depuis le 1er novembre 2010 :
- Une lettre (ne respecte pas la casse) 
- Huit chiffres

À partir du 1er avril 1987 jusqu’au 31 octobre 2010 :
- 10 chiffres

### <a name="checksum"></a>Somme de contrôle

Non

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :
- L’expression régulière Regex_germany_id_card trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_germany_id_card est trouvé.

```
<!-- Germany Identity Card Number -->
<Entity id="e577372f-c42e-47a0-9d85-bebed1c237d4" recommendedConfidence="65" patternsProximity="300">
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Regex_germany_id_card"/>
     <Match idRef="Keyword_germany_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordgermanyidcard"></a>Keyword_germany_id_card

- Identity Card
- ID
- Identification
- Personalausweis
- Identifizierungsnummer
- Ausweis
- Identifikation
   
## <a name="greece-national-id-card"></a>Carte d’identité nationale Grèce

### <a name="format"></a>Format

Combinaison de 7 ou 8 lettres et chiffres, plus un tiret

### <a name="pattern"></a>Modèle

Sept lettres et chiffres (ancien format) :
- Une lettre (de l’alphabet grec)  
- Un tiret 
- Six chiffres

Huit lettres et chiffres (nouveau format) :
- Deux lettres dont le caractère majuscule figure à la fois dans l’alphabet grec et l’alphabet latin (ABEZHIKMNOPTYX)  
- Un tiret 
- Six chiffres

### <a name="checksum"></a>Somme de contrôle

Non

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- L’expression régulière Regex_greece_id_card trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_greece_id_card est trouvé.

```
<!-- Greece National ID Card -->
<Entity id="82568215-1da1-46d3-874a-d2294d81b5ac" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_greece_id_card"/>
     <Match idRef="Keyword_greece_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordgreeceidcard"></a>Keyword_greece_id_card

- Greek identity Card
- Tautotita
- Δελτίο αστυνομικής ταυτότητας
- Ταυτότητα
   
## <a name="hong-kong-identity-card-hkid-number"></a>Numéro de carte d’identité (HKID) Hong Kong

### <a name="format"></a>Format

Combinaison de 8 ou 9 lettres et chiffres plus éventuellement des parenthèses autour du dernier caractère

### <a name="pattern"></a>Modèle

Combinaison de 8 ou 9 lettres :
- 1 ou 2 lettres (ne respectant pas la casse)  
- Six chiffres 
- Le dernier caractère (un chiffre ou la lettre A), qui est le chiffre de contrôle et est éventuellement entre parenthèses.

### <a name="checksum"></a>Somme de contrôle

Oui

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- La fonction Func_hong_kong_id_card trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_hong_kong_id_card est trouvé.
- La somme de contrôle est correcte.

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :
- La fonction Func_hong_kong_id_card trouve un contenu qui correspond au modèle.
- La somme de contrôle est correcte.

```
<!-- Hong Kong Identity Card (HKID) number -->
<Entity id="e63c28a7-ad29-4c17-a41a-3d2a0b70fd9c" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_hong_kong_id_card"/>
     <Match idRef="Keyword_hong_kong_id_card"/>
  </Pattern>
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Func_hong_kong_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordhongkongidcard"></a>Keyword_hong_kong_id_card

- Hong Kong Identity Card
- HKID
- ID card
- 香港身份證
 
- 香港永久性居民身份證
 
   
## <a name="india-permanent-account-number-pan"></a>Numéro de compte permanent Inde

### <a name="format"></a>Format

10 lettres ou chiffres

### <a name="pattern"></a>Modèle

10 lettres ou chiffres :
- Cinq lettres (ne respectant pas la casse)  
- Quatre chiffres 
- Une lettre qui est un chiffre de contrôle alphabétique

### <a name="checksum"></a>Somme de contrôle

Oui

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
- L’expression régulière Regex_india_permanent_account_number trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_india_permanent_account_number est trouvé.
- La somme de contrôle est correcte.

```
<!-- India Permanent Account Number -->
<Entity id="2602bfee-9bb0-47a5-a7a6-2bf3053e2804" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_india_permanent_account_number"/>
     <Match idRef="Keyword_india_permanent_account_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordindiapermanentaccountnumber"></a>Keyword_india_permanent_account_number

- Permanent Account Number
 
- PAN
 
   
## <a name="india-unique-identification-aadhaar-number"></a>Numéro d’identification unique (Aadhaar) Inde

### <a name="format"></a>Format

12 chiffres contenant éventuellement des espaces ou des tirets

### <a name="pattern"></a>Modèle

12 chiffres :
- Quatre chiffres 
- Éventuellement un tiret ou un espace  
- Quatre chiffres 
- Éventuellement un tiret ou un espace  
- Le chiffre final, qui est le chiffre de contrôle

### <a name="checksum"></a>Somme de contrôle

Oui

### <a name="definition"></a>Définition

Une stratégie DLP est de 85 % convaincu que ce type d’informations sensibles a été détecté if, au sein d’une proximité de 300 caractères : la fonction Func_india_aadhaar recherche le contenu qui correspond au modèle. Un mot clé à partir de Keyword_india_aadhar est trouvé. Passe de la somme de contrôle. Une stratégie DLP est convaincu que ce type d’informations sensibles a été détecté à 75 % if, au sein d’une proximité de 300 caractères : la fonction Func_india_aadhaar recherche le contenu qui correspond au modèle. Passe de la somme de contrôle. <!-- India Unique Identification (Aadhaar) number -->
<Entity id="1ca46b29-76f5-4f46-9383-cfa15e91048f" recommendedConfidence="85" patternsProximity="300"> <Pattern confidenceLevel="85"> <IdMatch idRef="Func_india_aadhaar"/> <Match idRef="Keyword_india_aadhar"/> </Pattern> <Pattern confidenceLevel="75"> <IdMatch idRef="Func_india_aadhaar"/> </Pattern>
</Entity>

### <a name="keywords"></a>Mots clés
   
#### <a name="keywordindiaaadhar"></a>Keyword_india_aadhar
- Aadhar
- Aadhaar
- UID
- आधार
   
## <a name="indonesia-identity-card-ktp-number"></a>Numéro de carte d’identité (KTP) Indonésie

### <a name="format"></a>Format

16 chiffres contenant éventuellement des points

### <a name="pattern"></a>Modèle

16 chiffres :
- Code à deux chiffres désignant la province  
- Un point (facultatif)  
- Code à deux chiffres désignant une régence ou une ville  
- Code à deux chiffres désignant un sous-district  
- Un point (facultatif)  
- Six chiffres au format JJMMAA qui correspondent à la date de naissance  
- Un point (facultatif)  
- Quatre chiffres

### <a name="checksum"></a>Somme de contrôle

Non

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- L’expression régulière Regex_indonesia_id_card trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_indonesia_id_card est trouvé.

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- L’expression régulière Regex_indonesia_id_card trouve un contenu qui correspond au modèle.

```
<!-- Indonesia Identity Card (KTP) Number -->
<Entity id="da68fdb0-f383-4981-8c86-82689d3b7d55" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_indonesia_id_card"/>
     <Match idRef="Keyword_indonesia_id_card"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_indonesia_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés
   
#### <a name="keywordindonesiaidcard"></a>Keyword_indonesia_id_card

- KTP
- Kartu Tanda Penduduk
 
- Nomor Induk Kependudukan
 
   
## <a name="international-banking-account-number-iban"></a>Numéro de compte bancaire international (IBAN)

### <a name="format"></a>Format

Code pays (à deux lettres) plus chiffres de contrôle (à deux chiffres) plus numéro BBAN (jusqu’à 30 chiffres)

### <a name="pattern"></a>Modèle

Le modèle doit inclure tous les éléments suivants :

- Code pays à deux lettres
- Deux chiffres de contrôle (suivis d’un espace facultatif)  
- 1 à 7 groupes de quatre lettres ou chiffres (séparés par des espaces facultatifs)
- 1 à 3 lettres ou chiffres

Le format pour chaque pays est légèrement différent. Le type d’informations sensibles IBAN recouvre ces 60 pays :

ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg

### <a name="checksum"></a>Somme de contrôle

Oui

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
- La fonction Func_iban trouve un contenu qui correspond au modèle.
- La somme de contrôle est correcte.

```
<Entity id="e7dc4711-11b7-4cb0-b88b-2c394a771f0e" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_iban" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

Aucun

   
## <a name="ip-address"></a>Adresse IP

### <a name="format"></a>Format

#### <a name="ipv4"></a>IPv4 :
Modèle complexe qui tient compte des versions mises en forme (points) et non mises en forme (sans points) des adresses IPv4

#### <a name="ipv6"></a>IPv6 :
 Modèle complexe qui tient compte des numéros IPv6 mis en forme (qui incluent les signes deux-points)

### <a name="pattern"></a>Modèle

### <a name="checksum"></a>Somme de contrôle

Non

### <a name="definition"></a>Définition

Pour IPv6, le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
- L’expression régulière Regex_ipv6_address trouve un contenu qui correspond au modèle.
- Aucun mot clé figurant dans la liste Keyword_ipaddress n’est trouvé.

Pour IPv4, le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 95 % si, dans une proximité de 300 caractères :
- L’expression régulière Regex_ipv4_address trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_ipaddress est trouvé.

Pour IPv6, le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 95 % si, dans une proximité de 300 caractères :
- L’expression régulière Regex_ipv6_address trouve un contenu qui correspond au modèle.
- Aucun mot clé figurant dans la liste Keyword_ipaddress n’est trouvé.

```
    <!-- IP Address -->
    <Entity id="1daa4ad5-e2dd-4ca4-a788-54722c09efb2" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Regex_ipv6_address" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_ipaddress" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="95">
        <IdMatch idRef="Regex_ipv4_address" />
        <Any minMatches="1">
          <Match idRef="Keyword_ipaddress" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="95">
        <IdMatch idRef="Regex_ipv6_address" />
        <Any minMatches="1">
          <Match idRef="Keyword_ipaddress" />
        </Any>
      </Pattern>
    </Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordipaddress"></a>Keyword_ipaddress

- IP (ce mot clé respecte la casse)
- ip address
 
- adresses IP
- protocole internet
- 
IP-כתובת ה
 
   
## <a name="international-classification-of-diseases-icd-10-cm"></a>Classification internationale de maux (ICD-10 CM)

### <a name="format"></a>Format

Dictionnaire

### <a name="pattern"></a>Modèle

Mot clé

### <a name="checksum"></a>Somme de contrôle

Non

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
- Un mot clé à partir de Dictionary_icd_10_cm est trouvé.

```
      <!-- ICD-10 CM -->
      <Entity id="3356946c-6bb7-449b-b253-6ffa419c0ce7" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_10_cm" />
        </Pattern>
      </Entity>
```

Keywords

Les termes à partir du dictionnaire de mot clé Dictionary_icd_10_cm, qui repose sur [International Classification de maux, révision dixième, Modification cliniques (ICD-10-CM)](https://go.microsoft.com/fwlink/?linkid=852604). Ce type de recherche uniquement le terme, pas les codes d’assurance.

   
## <a name="international-classification-of-diseases-icd-9-cm"></a>Classification internationale de maux (ICD-9-CM)

### <a name="format"></a>Format

Dictionnaire

### <a name="pattern"></a>Modèle

Mot clé

### <a name="checksum"></a>Somme de contrôle

Non

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
- Un mot clé à partir de Dictionary_icd_9_cm est trouvé.

```
      <Entity id="fa3f9c74-ee07-4c52-b5f2-085d6b2c0ec4" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_9_cm" />
        </Pattern>
      </Entity>
```

### <a name="keywords"></a>Keywords

Les termes à partir du dictionnaire de mot clé Dictionary_icd_9_cm, qui repose sur [International Classification de maux, révision neuvième, Modification cliniques (ICD-9-CM)](https://go.microsoft.com/fwlink/?linkid=852605). Ce type de recherche uniquement le terme, pas les codes d’assurance.
   
## <a name="ireland-personal-public-service-pps-number"></a>Numéro de service public personnel (PPS) Irlande

### <a name="format"></a>Format

Ancien format (jusqu'à 31 décembre 2012) :
- Sept chiffres suivis de 1 ou 2 lettres  

Nouveau format (1er janvier 2013 et une fois) :
- Sept chiffres suivis de deux lettres

### <a name="pattern"></a>Modèle

Ancien format (jusqu'à 31 décembre 2012) :
- Sept chiffres  
- 1 ou 2 lettres (ne respectant pas la casse)  

Nouveau format (1er janvier 2013 et une fois) :
- Sept chiffres  
- Une lettre (ne respectant pas la casse), qui est un chiffre de contrôle alphabétique  
- La lettre « A » ou « H » (ne respectant pas la casse)

### <a name="checksum"></a>Somme de contrôle

Oui

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
- La fonction Func_ireland_pps trouve un contenu qui correspond au modèle.
- L’une des affirmations suivantes est vraie :
    - Un mot clé figurant dans la liste Keyword_ireland_pps est trouvé.
    - La fonction Func_eu_date trouve une date au format correct.
- La somme de contrôle est correcte.

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :
- La fonction Func_ireland_pps trouve un contenu qui correspond au modèle.
- La somme de contrôle est correcte.

```
<!-- Ireland Personal Public Service (PPS) Number -->
<Entity id="1cdb674d-c19a-4fcf-9f4b-7f56cc87345a" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_ireland_pps"/>
     <Any minMatches="1">
  <Match idRef="Keyword_ireland_pps"/>
  <Match idRef="Func_eu_date"/>
     </Any>
  </Pattern>
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Func_ireland_pps"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordirelandpps"></a>Keyword_ireland_pps

- Personal Public Service Number 
 
- PPS Number
 
- PPS Num
 
- PPS No.
 
- PPS #
 
- PPS # 
- PPSN
 
- Public Services Card
 
- Uimhir Phearsanta Seirbhíse Poiblí
 
- Uimh. PSP
 
- PSP
 
   
## <a name="israel-bank-account-number"></a>Numéro de compte bancaire Israël

### <a name="format"></a>Format

13 chiffres

### <a name="pattern"></a>Modèle

Mis en forme :
- Deux chiffres 
- Un tiret 
- Trois chiffres 
- Un tiret 
- Huit chiffres

Non mis en forme :
- 	13 chiffres consécutifs

### <a name="checksum"></a>Somme de contrôle

Non

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- L’expression régulière Regex_israel_bank_account_number trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_israel_bank_account_number est trouvé.

```
<!-- Israel Bank Account Number -->
<Entity id="7d08b2ff-a0b9-437f-957c-aeddbf9b2b25" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_israel_bank_account_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_israel_bank_account_number" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordisraelbankaccountnumber"></a>Keyword_israel_bank_account_number

- Numéro de compte bancaire
 
- Compte bancaire
 
- Numéro de compte
 
- מספר חשבון בנק
 
   
## <a name="israel-national-id"></a>Carte nationale d'identité Israël

### <a name="format"></a>Format

Neuf chiffres

### <a name="pattern"></a>Modèle

Neuf chiffres consécutifs

### <a name="checksum"></a>Somme de contrôle

Oui

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- La fonction Func_israeli_national_id_number trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_Israel_National_ID est trouvé.
- La somme de contrôle est correcte.

```
<!-- Israel National ID Number -->
<Entity id="e05881f5-1db1-418c-89aa-a3ac5c5277ee" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_israeli_national_id_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_Israel_National_ID" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordisraelnationalid"></a>Keyword_Israel_National_ID

- מספר זהות
 
- Numéro d’identification nationale
   
## <a name="italy-drivers-license-number"></a>Numéro de permis de conduire Italie

### <a name="format"></a>Format

Une combinaison de 10 lettres et chiffres

### <a name="pattern"></a>Modèle

- Une combinaison de 10 lettres et chiffres :
- Une lettre (ne respecte pas la casse) 
- La lettre « A » ou « V » (ne respecte pas la casse) 
- Sept lettres (ne respectent pas la casse), des chiffres ou le trait de soulignement 
- Une lettre (ne respecte pas la casse)

### <a name="checksum"></a>Somme de contrôle

Non

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- L’expression régulière Regex_italy_drivers_license_number trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_italy_drivers_license_number est trouvé.

```
<!-- Italy Driver's license Number -->
<Entity id="97d6244f-9157-41bd-8e0c-9d669a5c4d71" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_italy_drivers_license_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_italy_drivers_license_number" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keyworditalydriverslicensenumber"></a>Keyword_italy_drivers_license_number

- numero di patente di guida
 
- patente di guida
 
   
## <a name="japan-bank-account-number"></a>Numéro de compte bancaire Japon

### <a name="format"></a>Format

Sept ou huit chiffres

### <a name="pattern"></a>Modèle

Numéro de compte bancaire :
- Sept ou huit chiffres
- Code guichet du compte bancaire :
- Quatre chiffres 
- Un espace ou un tiret (facultatif) 
- Trois chiffres

Somme de contrôle

Non

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
- La fonction Func_jp_bank_account trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_jp_bank_account est trouvé.
- L’une des affirmations suivantes est vraie :
- La fonction Func_jp_bank_account_branch_code trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_jp_bank_branch_code est trouvé.

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- La fonction Func_jp_bank_account trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_jp_bank_account est trouvé.

```
<!-- Japan Bank Account Number -->
<Entity id="d354f95b-96ee-4b80-80bc-4377312b55bc" patternsProximity="300" recommendedConfidence="75">
  <Version minEngineVersion="15.01.0131.000">
    <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_jp_bank_account" />
          <Match idRef="Keyword_jp_bank_account" />
          <Any minMatches="1">
            <Match idRef="Func_jp_bank_account_branch_code" />
            <Match idRef="Keyword_jp_bank_branch_code" />
          </Any>
      </Pattern>
  </Version>    
     <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_bank_account" />
        <Match idRef="Keyword_jp_bank_account" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordjpbankaccount"></a>Keyword_jp_bank_account

- Numéro de compte courant
 
- Compte courant
 
- # compte courant
 
- Numéro compte courant
 
- # compte courant
 
- N° de compte courant
 
- N° de compte courant
 
- Numéro de compte bancaire
 
- Compte bancaire
 
- # Compte bancaire
 
- Numéro de compte bancaire
 
- # Compte bancaire
 
- N° de compte bancaire
 
- N° de compte bancaire
 
- Numéro de compte d’épargne
 
- Compte d’épargne 
- N° de compte d’épargne
 
- Numéro de compte d’épargne
 
- # compte d’épargne
 
- N° de compte d’épargne
 
- N° de compte d’épargne
 
- Numéro de compte de débit
 
- Compte de débit
 
- # Compte de débit
 
- Numéro de compte de débit
 
- # Compte de débit
 
- N° de compte de débit
 
- N° de compte de débit
 
- 口座番号を当座預金口座の確認
 
- ＃アカウントの確認、勘定番号の確認
 
- ＃勘定の確認
 
- 勘定番号の確認
 
- 口座番号の確認
 
- 銀行口座番号 
- 銀行口座 
- 銀行口座＃
 
- 銀行の勘定番号
 
- 銀行のacct＃
 
- 銀行の勘定いいえ
 
- 銀行口座番号
- 
普通預金口座番号
 
- 預金口座
 
- 貯蓄口座＃
 
- 貯蓄勘定の数
 
- 貯蓄勘定＃
 
- 貯蓄勘定番号
 
- 普通預金口座番号
 
- 引き落とし口座番号
 
- 口座番号 
- 口座番号 #
 
- デビットのacct番号
 
- デビット勘定＃
 
- デビットACCTの番号
 
- デビット口座番号
 

#### <a name="keywordjpbankbranchcode"></a>Keyword_jp_bank_branch_code

Otemachi

## <a name="japan-drivers-license-number"></a>Numéro de permis de conduire Japon

### <a name="format"></a>Format

12 chiffres

### <a name="pattern"></a>Modèle

12 chiffres consécutifs

### <a name="checksum"></a>Somme de contrôle

Non

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- La fonction Func_jp_drivers_license_number trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_jp_drivers_license_number est trouvé.

```
<!-- Japan Driver's License Number -->
<Entity id="c6011143-d087-451c-8313-7f6d4aed2270" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_drivers_license_number" />
        <Match idRef ="Keyword_jp_drivers_license_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordjpdriverslicensenumber"></a>Keyword_jp_drivers_license_number

- dl# 
- DL # 
- dls# 
- LISTES DE DISTRIBUTION # 
- driver license 
- driver licenses 
- drivers license 
- driver’s license 
- drivers licenses 
- driver’s licenses 
- permis de conduire
 
- lic# 
- LIC # 
- #permis 
- id d’état 
- identification d’état
 
- numéro d’identification d’état
 
- 低所得国＃
 
- 免許証 
- 状態ID
- 
状態の識別
 
- 状態の識別番号
 
- 運転免許 
- 運転免許証 
- 運転免許証番号 
   
## <a name="japan-passport-number"></a>Numéro de passeport Japon

### <a name="format"></a>Format

Deux lettres suivies de sept chiffres

### <a name="pattern"></a>Modèle

Deux lettres (ne respectant pas la casse) suivies de sept chiffres

### <a name="checksum"></a>Somme de contrôle

Non

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- La fonction Func_jp_passport trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_jp_passport est trouvé.

```
<!-- Japan Passport Number -->
<Entity id="75177310-1a09-4613-bf6d-833aae3743f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_passport" />
        <Match idRef="Keyword_jp_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordjppassport"></a>Keyword_jp_passport

- パスポート
 
- パスポート番号
 
- パスポートのNum
 
- パスポート＃
 
   
## <a name="japan-resident-registration-number"></a>Matricule de résident Japon

### <a name="format"></a>Format

11 chiffres

### <a name="pattern"></a>Modèle

11 chiffres consécutifs

### <a name="checksum"></a>Somme de contrôle

Non

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- La fonction Func_jp_resident_registration_number trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_jp_resident_registration_number est trouvé.

```
<!-- Japan Resident Registration Number -->
<Entity id="01c1209b-6389-4faf-a5f8-3f7e13899652" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_resident_registration_number" />
        <Match idRef ="Keyword_jp_resident_registration_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordjpresidentregistrationnumber"></a>Keyword_jp_resident_registration_number

- Numéro d’enregistrement du résident
- Numéro d’enregistrement du résident
 
- Numéro de base d’enregistrement des résidents
 
- N° d’enregistrement du résident
 
- N° d’enregistrement du résident
 
- N° de base d’enregistrement des résidents
 
- N° d’enregistrement du résident de base
 
- 住民登録番号、登録番号をレジデント
 
- 住民基本登録番号、登録番号
 
- 住民基本レジストリ番号を常駐
 
- 登録番号を常駐住民基本台帳登録番号
 

   
## <a name="japan-social-insurance-number-sin"></a>Numéro d'assurance sociale Japon

### <a name="format"></a>Format

7 à 12 chiffres

### <a name="pattern"></a>Modèle

7 à 12 chiffres :
- Quatre chiffres 
- Un trait d’union (facultatif) 
- Six chiffres ou
- 7 à 12 chiffres consécutifs

### <a name="checksum"></a>Somme de contrôle

Non

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
- La fonction Func_jp_sin trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_jp_sin est trouvé.

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- La fonction Func_jp_sin_pre_1997 trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_jp_sin est trouvé.

```
<!-- Japan Social Insurance Number -->
<Entity id="c840e719-0896-45bb-84fd-1ed5c95e45ff" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_jp_sin" />
        <Match idRef="Keyword_jp_sin" />
    </Pattern>
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_sin_pre_1997" />
        <Match idRef="Keyword_jp_sin" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordjpsin"></a>Keyword_jp_sin

- N° d’assurance sociale
 
- Numéro d’assurance sociale
 
- Numéro d’assurance sociale
 
- 社会保険のテンキー
 
- 社会保険番号
 
   
## <a name="malaysia-id-card-number"></a>Numéro de carte d’identité Malaisie

### <a name="format"></a>Format

12 chiffres contenant éventuellement des traits d’union

### <a name="pattern"></a>Modèle

12 chiffres :
- Six chiffres au format AAMMJJ correspondant à la date de naissance  
- Un tiret (facultatif)  
- Le code à deux lettres du lieu de naissance  
- Un tiret (facultatif)  
- Trois chiffres aléatoires  
- Code de sexe à un chiffre

### <a name="checksum"></a>Somme de contrôle

Non

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
- L’expression régulière Regex_malaysia_id_card_number trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_malaysia_id_card_number est trouvé.

```
<!-- Malaysia ID Card Number -->
</Entity>
      <Entity id="7f0e921c-9677-435b-aba2-bb8f1013c749" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
            <IdMatch idRef="Regex_malaysia_id_card_number" />
            <Match idRef="Keyword_malaysia_id_card_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés
   
#### <a name="keywordmalaysiaidcardnumber"></a>Keyword_malaysia_id_card_number

- MyKad 
- Identity Card 
- Carte d’identité 
- Carte d’identification 
- Digital Application Card
 
- Kad Akuan Diri
 
- Kad Aplikasi Digital
 
   
## <a name="netherlands-citizens-service-bsn-number"></a>Numéro de service du citoyen (BSN) Pays-Bas

### <a name="format"></a>Format

8 à 9 chiffres contenant éventuellement des espaces

### <a name="pattern"></a>Modèle

8 à 9 chiffres :
- Trois chiffres 
- Un espace (facultatif)  
- Trois chiffres 
- Un espace (facultatif)  
- 2 à 3 chiffres

### <a name="checksum"></a>Somme de contrôle

Oui

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
- La fonction Func_netherlands_bsn trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_netherlands_bsn est trouvé.
- La fonction Func_eu_date2 trouve une date au format correct.
- La somme de contrôle est correcte.

```
<!-- Netherlands Citizen's Service (BSN) Number -->
<Entity id="c5f54253-ef7e-44f6-a578-440ed67e946d" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
       <IdMatch idRef="Func_netherlands_bsn" /> 
       <Match idRef="Keyword_netherlands_bsn" /> 
       <Match idRef="Func_eu_date2" /> 
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordnetherlandsbsn"></a>Keyword_netherlands_bsn

- Citizen service number
 
- BSN

 
- Burgerservicenummer
 
- Sofinummer
 
- Persoonsgebonden nummer
 
- Persoonsnummer
    

   
## <a name="new-zealand-ministry-of-health-number"></a>Numéro du Ministère de la santé Nouvelle-Zélande

### <a name="format"></a>Format

Trois lettres, un espace (facultatif) et quatre chiffres

### <a name="pattern"></a>Modèle

Trois lettres (pas la casse), un espace (facultatif) quatre chiffres

### <a name="checksum"></a>Somme de contrôle

Oui

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
- La fonction Func_new_zealand_ministry_of_health_number trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_nz_terms est trouvé.
- La somme de contrôle est correcte.

```
<!-- New Zealand Health Number -->
<Entity id="2b71c1c8-d14e-4430-82dc-fd1ed6bf05c7" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_new_zealand_ministry_of_health_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_nz_terms" />
        </Any>
    </Pattern>
</Entity>
```

Mots clés

Keyword_nz_terms

- NHI
 
- Nouvelle-Zélande 
- Intégrité 
- treatment
 
   
## <a name="norway-identification-number"></a>Numéro d’identification Norvège

### <a name="format"></a>Format

11 chiffres

### <a name="pattern"></a>Modèle

11 chiffres :
- Six chiffres au format JJMMAA qui correspondent à la date de naissance  
- Numéro individuel à trois chiffres  
- Deux chiffres de contrôle

### <a name="checksum"></a>Somme de contrôle

Oui

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
- La fonction Func_norway_id_number trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_norway_id_number est trouvé.
- La somme de contrôle est correcte.
- Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- La fonction Func_norway_id_numbe trouve un contenu qui correspond au modèle.
- La somme de contrôle est correcte.

```
<!-- Norway Identification Number -->
<Entity id="d4c8a798-e9f2-4bd3-9652-500d24080fc3" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_norway_id_number"/>
     <Match idRef="Keyword_norway_id_number"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_norway_id_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordnorwayidnumber"></a>Keyword_norway_id_number

- Personal identification number
- Norwegian ID Number
- ID Number
- Identification
- Personnummer
- Fødselsnummer

   
## <a name="philippines-unified-multi-purpose-id-number"></a>Numéro d’identification multifonction unifié Philippines

### <a name="format"></a>Format

12 chiffres séparés par des traits d’union

### <a name="pattern"></a>Modèle

12 chiffres :
- Quatre chiffres 
- Un trait d’union  
- Sept chiffres  
- Un trait d’union  
- Un chiffre

### <a name="checksum"></a>Somme de contrôle

Non

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- L’expression régulière Regex_philippines_unified_id trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_philippines_id est trouvé.

```
<!-- Philippines Unified Multi-Purpose ID number -->
<Entity id="019b39dd-8c25-4765-91a3-d9c6baf3c3b3" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_philippines_unified_id"/>
     <Match idRef="Keyword_philippines_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés
   
#### <a name="keywordphilippinesid"></a>Keyword_philippines_id

- Unified Multi-Purpose ID
 
- UMID
 
- Identity Card 
- Pinag-isang Multi-Layunin ID
   
## <a name="poland-identity-card"></a>Carte d'identité Pologne

### <a name="format"></a>Format

Trois lettres et six chiffres

### <a name="pattern"></a>Modèle

Trois lettres (ne respectant pas la casse) suivis de six chiffres

### <a name="checksum"></a>Somme de contrôle

Oui

### <a name="definition"></a>Définition

Une stratégie DLP est convaincu que ce type d’informations sensibles a été détecté à 75 % if, au sein d’une proximité de 300 caractères : la fonction Func_polish_national_id recherche le contenu qui correspond au modèle. Un mot clé à partir de Keyword_polish_national_id_passport_number est trouvé. Passe de la somme de contrôle.

```
<!-- Poland Identity Card-->
<Entity id="25E64989-ED5D-40CA-A939-6C14183BB7BF" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_national_id" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordpolishnationalidpassportnumber"></a>Keyword_polish_national_id_passport_number

- Nazwa je nr dowodu tożsamości
 
- Dowód Tożsamości
 
- dow. os.
 

   
## <a name="poland-national-id-pesel"></a>ID national polonais (PESEL)

### <a name="format"></a>Format

11 chiffres

### <a name="pattern"></a>Modèle

11 chiffres consécutifs

### <a name="checksum"></a>Somme de contrôle

Oui

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
- La fonction Func_pesel_identification_number trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_pesel_identification_number est trouvé.
- La somme de contrôle est correcte.

```
<!-- Poland National ID (PESEL) -->      
<Entity id="E3AAF206-4297-412F-9E06-BA8487E22456" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_pesel_identification_number" />
          <Match idRef="Keyword_pesel_identification_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordpeselidentificationnumber"></a>Keyword_pesel_identification_number

- Nr PESEL
- PESEL   

   
## <a name="poland-passport"></a>Passeport Pologne

### <a name="format"></a>Format

Deux lettres et sept chiffres

### <a name="pattern"></a>Modèle

Deux lettres (ne respectant pas la casse) suivies de sept chiffres

### <a name="checksum"></a>Somme de contrôle

Oui

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
- La fonction Func_polish_passport_number trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_polish_national_id_passport_number est trouvé.
- La somme de contrôle est correcte.

```
<!-- Poland Passport Number -->
<Entity id="03937FB5-D2B6-4487-B61F-0F8BFF7C3517" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_passport_number" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
</Version>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordpolishnationalidpassportnumber"></a>Keyword_polish_national_id_passport_number

- Nazwa je nr dowodu tożsamości
 
- Dowód Tożsamości
 
- dow. os.
 

   
## <a name="portugal-citizen-card-number"></a>Numéro de carte de citoyen Portugal

### <a name="format"></a>Format

Huit chiffres

### <a name="pattern"></a>Modèle

Huit chiffres

### <a name="checksum"></a>Somme de contrôle

Non

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
- L’expression régulière Regex_portugal_citizen_card trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_portugal_citizen_card est trouvé.

```
<!-- Portugal Citizen Card Number -->
<Entity id="91a7ece2-add4-4986-9a15-c84544d81ecd" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_portugal_citizen_card"/>
     <Match idRef="Keyword_portugal_citizen_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordportugalcitizencard"></a>Keyword_portugal_citizen_card

- Citizen Card
- National ID Card
- CC
- Cartão de Cidadão
- Bilhete de Identidade
   
## <a name="saudi-arabia-national-id"></a>ID national Arabie saoudite

### <a name="format"></a>Format

10 chiffres

### <a name="pattern"></a>Modèle

10 chiffres consécutifs

### <a name="checksum"></a>Somme de contrôle

Non

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- L’expression régulière Regex_saudi_arabia_national_id trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_saudi_arabia_national_id est trouvé.

```
<!-- Saudi Arabia National ID -->
<Entity id="8c5a0ba8-404a-41a3-8871-746aa21ee6c0" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_saudi_arabia_national_id" />
        <Any minMatches="1">
          <Match idRef="Keyword_saudi_arabia_national_id" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordsaudiarabianationalid"></a>Keyword_saudi_arabia_national_id

- Carte d’identification
 
- numéro de carte d’identité
 
- numéro d’identification 
- الوطنية الهوية بطاقة رقم
 

   
## <a name="singapore-national-registration-identity-card-nric-number"></a>Numéro de carte d’identité d’enregistrement national (NRIC) Singapour

### <a name="format"></a>Format

Neuf lettres et chiffres

### <a name="pattern"></a>Modèle

- Neuf lettres et chiffres :
- La lettre « F », « G », « S » ou « T » (ne respectant pas la casse)  
- Sept chiffres  
- Un chiffre de contrôle alphabétique

### <a name="checksum"></a>Somme de contrôle

Oui

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
- L’expression régulière Regex_singapore_nric trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_singapore_nric est trouvé.
- La somme de contrôle est correcte.

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- L’expression régulière Regex_singapore_nric trouve un contenu qui correspond au modèle.
- La somme de contrôle est correcte.

```
<!-- Singapore National Registration Identity Card (NRIC) Number -->
<Entity id="cead390a-dd83-4856-9751-fb6dc98c34da" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_singapore_nric"/>
     <Match idRef="Keyword_singapore_nric"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_singapore_nric"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés
   
#### <a name="keywordsingaporenric"></a>Keyword_singapore_nric

- National Registration Identity Card
 
- Identity Card Number
 
- NRIC
 
- IC
 
- Foreign Identification Number
 
- FIN
 
- 身份证  
- 身份證
 
   
## <a name="south-africa-identification-number"></a>Numéro d’identification Afrique du Sud

### <a name="format"></a>Format

13 chiffres pouvant contenir des espaces

### <a name="pattern"></a>Modèle

13 chiffres :
- Six chiffres au format AAMMJJ correspondant à la date de naissance  
- Quatre chiffres 
- Un indicateur de citoyenneté à un chiffre  
- Le chiffre « 8 » ou « 9 »  
- Un chiffre pour la somme de contrôle

### <a name="checksum"></a>Somme de contrôle

Oui

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
- La fonction Func_south_africa_identification_number trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_south_africa_identification_number est trouvé.
- La somme de contrôle est correcte.

```
<!-- South Africa Identification Number -->
<Entity id="e2adf7cb-8ea6-4048-a2ed-d89eb65f2780" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_south_africa_identification_number"/>
     <Match idRef="Keyword_south_africa_identification_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés
   
#### <a name="keywordsouthafricaidentificationnumber"></a>Keyword_south_africa_identification_number

- Identity card
- ID
- Identification 
   
## <a name="south-korea-resident-registration-number"></a>Matricule de résident Corée du Sud

### <a name="format"></a>Format

13 chiffres contenant un trait d’union

### <a name="pattern"></a>Modèle

13 chiffres :
- Six chiffres au format AAMMJJ correspondant à la date de naissance  
- Un trait d’union  
- Un chiffre déterminé par le siècle et le sexe  
- Code à quatre chiffres désignant la région de naissance  
- Un chiffre utilisé pour différencier les personnes dont les chiffres précédents sont identiques.  
- Un chiffre de contrôle.

### <a name="checksum"></a>Somme de contrôle

Oui

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
- La fonction Func_south_korea_resident_number trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_south_korea_resident_number est trouvé.
- La somme de contrôle est correcte.

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- La fonction Func_south_korea_resident_number trouve un contenu qui correspond au modèle.
- La somme de contrôle est correcte.

```
<!-- South Korea Resident Registration Number -->
<Entity id="5b802e18-ba80-44c4-bc83-bf2ad36ae36a" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_south_korea_resident_number"/>
     <Match idRef="Keyword_south_korea_resident_number"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_south_korea_resident_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés
   
#### <a name="keywordsouthkorearesidentnumber"></a>Keyword_south_korea_resident_number

- National ID card
 
- Citizen’s Registration Number
 
- Jumin deungnok beonho
 
- RRN
 
- 주민등록번호
   
## <a name="spain-social-security-number-ssn"></a>Numéro de sécurité sociale Espagne

### <a name="format"></a>Format

11 à 12 chiffres

### <a name="pattern"></a>Modèle

chiffres de 11-12 :
- Deux chiffres 
- Une barre oblique (facultative) 
- 7 à 8 chiffres 
- Une barre oblique (facultative) 
- Deux chiffres

### <a name="checksum"></a>Somme de contrôle

Oui

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
- La fonction Func_spanish_social_security_number trouve un contenu qui correspond au modèle.
- La somme de contrôle est correcte.

```
<!-- Spain SSN -->
<Entity id="5df987c0-8eae-4bce-ace7-b316347f3070" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_spanish_social_security_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

Aucun
   
## <a name="sweden-national-id"></a>ID national Suède

### <a name="format"></a>Format

10 ou 12 chiffres et éventuellement un délimiteur

### <a name="pattern"></a>Modèle

10 ou 12 chiffres et un délimiteur facultatif :
- 2 à 4 chiffres (facultatifs) 
- Six chiffres au format de date AAMMJJ 
- Séparateur de « - » ou « + » (facultatif), plus
- Quatre chiffres

### <a name="checksum"></a>Somme de contrôle

Oui

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
- La fonction Func_swedish_national_identifier trouve un contenu qui correspond au modèle.
- La somme de contrôle est correcte.

```
<!-- Sweden National ID -->
<Entity id="f69aaf40-79be-4fac-8f05-fd1910d272c8" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_swedish_national_identifier" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

Non
   
## <a name="sweden-passport-number"></a>Numéro de passeport Suède

### <a name="format"></a>Format

Huit chiffres

### <a name="pattern"></a>Modèle

Huit chiffres consécutifs

### <a name="checksum"></a>Somme de contrôle

Non

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- L’expression régulière Regex_sweden_passport_number trouve un contenu qui correspond au modèle.
- L’une des affirmations suivantes est vraie :
    - Un mot clé figurant dans la liste Keyword_passport est trouvé.
    - Un mot clé figurant dans la liste Keyword_sweden_passport est trouvé.

```
<!-- Sweden Passport Number -->
<Entity id="ba4e7456-55a9-4d89-9140-c33673553526" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_sweden_passport_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_passport" />
          <Match idRef="Keyword_sweden_passport" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés
   
#### <a name="keywordswedenpassport"></a>Keyword_sweden_passport

- exigences en matière de visa
 
- Carte d’enregistrement d’une personne étrangère
 
- Visas Schengen
 
- Visa Schengen
 
- Traitement du visa
 
- Type de visa
 
- Entrée unique
 
- Entrée multiple
 
- Frais de traitement G3

 

#### <a name="keywordpassport"></a>Keyword_passport

- Numéro de passeport 
- 
N° de passeport 
- # Passeport
 
- #Passeport
 
- IDPassport 
- n° passeport
 
- numéropasseport
 
- パスポート 
- パスポート番号
 
- パスポートのNum
 
- パスポート＃
 
- Numéro de passeport 
- 
Passeport n° 
- Passeport numéro
 
- # Passeport
 
- Passeport#
 
- PasseportNon 
- Passeportn °
 
   
## <a name="swift-code"></a>Code SWIFT

### <a name="format"></a>Format

Quatre lettres suivies de 5 à 31 lettres ou chiffres

### <a name="pattern"></a>Modèle

Quatre lettres suivies de 5 à 31 lettres ou chiffres :
- Code bancaire à quatre lettres (ne respectent pas la casse) 
- Un espace facultatif 
- 4 à 28 lettres ou chiffres (numéro de compte bancaire de base (BBAN)) 
- Un espace facultatif 
- 1 à 3 lettres ou chiffres (reste du BBAN)

### <a name="checksum"></a>Somme de contrôle

Non

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- L’expression régulière Regex_swift trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_swift est trouvé.

```
<Entity id="cb2ab58c-9cb8-4c81-baf8-a4e106791df4" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_swift" />
        <Match idRef="Keyword_swift" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés
   
#### <a name="keywordswift"></a>Keyword_swift

- organisation internationale de normalisation 9362
 
- ISO 9362
 
- iso9362 
- SWIFT\# 
- codeswift
 
- numéroswift
 
- numéroroutageswift
 
- code SWIFT 
- # numéro swift
 
- numéro d’acheminement swift
 
- numéro BIC
 
- code BIC
 
- BIC\# 
- BIC\# 
- code d’identification bancaire
 
- 標準化9362 
- 迅速＃
 
- SWIFTコード
 
- SWIFT番号
 
- 迅速なルーティング番号
 
- BIC番号
 
- BICコード
 
- 銀行識別コードのための国際組織
 
- Organisation internationale de normalisation 9362
 
- rapide\# 
- code SWIFT
 
- le numéro de swift
 
- swift numéro d’acheminement
 
- le numéro BIC
 
- \#BIC 
- code identificateur de banque
 
   
## <a name="taiwan-national-id"></a>ID national à Taïwan

### <a name="format"></a>Format

Une lettre  suivie de neuf chiffres

### <a name="pattern"></a>Modèle

Une lettre suivie de neuf chiffres :
- Une lettre (en anglais, ne respecte pas la casse) 
- Le chiffre « 1 » ou « 2 » 
- Huit chiffres

### <a name="checksum"></a>Somme de contrôle

Oui

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
- La fonction Func_taiwanese_national_id trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_taiwanese_national_id est trouvé.
- La somme de contrôle est correcte.

```
<!-- Taiwanese National ID -->
<Entity id="4C7BFC34-8DD1-421D-8FB7-6C6182C2AF03" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_taiwanese_national_id" />
          <Match idRef="Keyword_taiwanese_national_id" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordtaiwanesenationalid"></a>Keyword_taiwanese_national_id

- 身份證字號
 
- 身份證
 
- 身份證號碼
 
- 身份證號
 
- 身分證字號
 
- 身分證  
- 身分證號碼
 
- 身份證號
 
- 身分證統一編號
 
- 國民身分證統一編號
 
- 簽名
 
- 蓋章
 
- 簽名或蓋章

 
- 簽章   
   
## <a name="taiwan-passport-number"></a>Numéro de passeport Taïwan

### <a name="format"></a>Format

- Numéro de passeport biométrique : neuf chiffres
- Numéro de passeport non biométrique : neuf chiffres

### <a name="pattern"></a>Modèle
Numéro de passeport biométrique :
- Le chiffre « 3 »  
- Huit chiffres

Numéro de passeport non biométrique :
- Neuf chiffres

### <a name="checksum"></a>Somme de contrôle

Non

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- L’expression régulière Regex_taiwan_passport trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_taiwan_passport est trouvé.

```
<!-- Taiwan Passport Number -->
<Entity id="e7251cb4-4c2c-41df-963e-924eb3dae04a" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_passport"/>
     <Match idRef="Keyword_taiwan_passport"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordtaiwanpassport"></a>Keyword_taiwan_passport

- ROC passport number
 
- Numéro de passeport 
- Passeport aucune 
- Passport Num
 
- # Passeport
 
- 护照
 
- 中華民國護照
 
- Zhōnghuá Mínguó hùzhào
   
## <a name="taiwan-resident-certificate-arctarc-number"></a>Numéro de certificat de résident (ARC/TARC) Taïwan

### <a name="format"></a>Format

10 lettres et chiffres

### <a name="pattern"></a>Modèle

10 lettres et chiffres :
- Deux lettres (ne respectant pas la casse)  
- Huit chiffres

### <a name="checksum"></a>Somme de contrôle

Non

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- L’expression régulière Regex_taiwan_resident_certificate trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_taiwan_resident_certificate est trouvé.

```
<!-- Taiwan Resident Certificate (ARC/TARC) -->
<Entity id="48269fec-05ea-46ea-b326-f5623a58c6e9" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_resident_certificate"/>
     <Match idRef="Keyword_taiwan_resident_certificate"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordtaiwanresidentcertificate"></a>Keyword_taiwan_resident_certificate

- Resident Certificate
 
- Cert résident 
- Resident Cert.
 
- Carte d’identification 
- Alien Resident Certificate
 
- ARC
 
- Taiwan Area Resident Certificate
 
- TARC
 
- 居留證
 
- 外僑居留證
 
- 台灣地區居留證
 
   
## <a name="uk-drivers-license-number"></a>Numéro de permis de conduire Royaume-Uni

### <a name="format"></a>Format

Combinaison de 18 lettres et chiffres au format spécifié

### <a name="pattern"></a>Modèle

18 lettres et chiffres
- Cinq lettres (ne respectent pas la casse) ou le chiffre « 9 » à la place d’une lettre 
- Un chiffre 
- Cinq chiffres au format de date JJMMA pour la date de naissance 
- Deux lettres (ne respectent pas la casse) ou le chiffre « 9 » à la place d’une lettre 
- Cinq chiffres

### <a name="checksum"></a>Somme de contrôle

Oui

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- La fonction Func_uk_drivers_license trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_uk_drivers_license est trouvé.
- La somme de contrôle est correcte.

```
<!-- U.K. Driver's License Number -->
<Entity id="f93de4be-d94c-40df-a8be-461738047551" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_uk_drivers_license" />
        <Match idRef="Keyword_uk_drivers_license" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordukdriverslicense"></a>Keyword_uk_drivers_license

- DVLA
 
- véhicule utilitaire léger
 
- quad
 
- automobiles
 
- 125cc 
- sidecar
 
- tricycles
 
- motocycles
 
- permis de conduire plastifié
 
- apprentis conducteurs
 
- titulaire du permis
 
- titulaires du permis
 
- permis de conduire
 
- permis de conduire
 
- voiture à double commande
 
   
## <a name="uk-electoral-roll-number"></a>Numéro de liste électorale Royaume-Uni

### <a name="format"></a>Format

Deux lettres suivies de 1 à 4 chiffres

### <a name="pattern"></a>Modèle

Deux lettres (ne respectant pas la casse) suivies de 1 à 4 chiffres

### <a name="checksum"></a>Somme de contrôle

Non

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- L’expression régulière Regex_uk_electoral trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_uk_electoral est trouvé.

```
<!-- U.K. Electoral Number -->
<Entity id="a3eea206-dc0c-4f06-9e22-aa1be3059963" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_uk_electoral" />
        <Any minMatches="1">
          <Match idRef="Keyword_uk_electoral" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordukelectoral"></a>Keyword_uk_electoral

- nomination au conseil
 
- formulaire de nomination
 
- registre électoral

 
- liste électorale

   
## <a name="uk-national-health-service-number"></a>Numéro national des services de santé Royaume-Uni

### <a name="format"></a>Format

10 à 17 chiffres séparés par des espaces

### <a name="pattern"></a>Modèle

10 à 17 chiffres :
- 3 ou 10 chiffres 
- Un espace 
- Trois chiffres 
- Un espace 
- Quatre chiffres

### <a name="checksum"></a>Somme de contrôle

Oui

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
- La fonction Func_uk_nhs_number trouve un contenu qui correspond au modèle.
- L’une des affirmations suivantes est vraie :
    - Un mot clé figurant dans la liste Keyword_uk_nhs_number est trouvé.
    - Un mot clé figurant dans la liste Keyword_uk_nhs_number1 est trouvé.
    - Un mot clé figurant dans la liste Keyword_uk_nhs_number_dob est trouvé.
- La somme de contrôle est correcte.

```
<!-- U.K. NHS Number -->
<Entity id="3192014e-2a16-44e9-aa69-4b20375c9a78" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_uk_nhs_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_uk_nhs_number" />
          <Match idRef="Keyword_uk_nhs_number1" />
          <Match idRef="Keyword_uk_nhs_number_dob" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés
   
#### <a name="keyworduknhsnumber"></a>Keyword_uk_nhs_number

- service national de santé
 
- NHS
 
- administration des services de santé

 
- administration de la santé

#### <a name="keyworduknhsnumber1"></a>Keyword_uk_nhs_number1

- id du patient
 
- identification du patient
 
- n° patient

 
- numéro de patient

#### <a name="keyworduknhsnumberdob"></a>Keyword_uk_nhs_number_dob

- Stratégie de groupe 
- DDN
 
- D.O.B 
- Date of Birth
 
- Birth Date
 
   
## <a name="uk-national-insurance-number-nino"></a>Numéro d'assurance nationale (NINO) Royaume-Uni

### <a name="format"></a>Format

7 caractères ou 9 caractères séparés par des espaces ou des tirets

### <a name="pattern"></a>Modèle

Deux modèles possibles :

- Deux lettres (valides NINOs utilisent uniquement certains caractères dans ce préfixe, ce modèle est valide ; pas la casse)
- Six chiffres
- Soit « A », « B », « C », ou a ' (comme le préfixe, seuls certains caractères sont autorisés dans le suffixe ; pas respectant la casse)

OU

- Deux lettres
- Un espace ou un tiret
- Deux chiffres
- Un espace ou un tiret
- Deux chiffres
- Un espace ou un tiret
- Deux chiffres
- Un espace ou un tiret
- 'A', 'B', « C », ou a '

### <a name="checksum"></a>Somme de contrôle

Non

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
- La fonction Func_uk_nino trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_uk_nino est trouvé.

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- La fonction Func_uk_nino trouve un contenu qui correspond au modèle.
- Aucun mot clé figurant dans la liste Keyword_uk_nino n’est trouvé.

```
<!-- U.K. NINO -->
<Entity id="16c07343-c26f-49d2-a987-3daf717e94cc" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_uk_nino" />
        <Any minMatches="1">
          <Match idRef="Keyword_uk_nino" />
        </Any>
    </Pattern>    
     <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_uk_nino" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_uk_nino" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keyworduknino"></a>Keyword_uk_nino

- numéro d’assurance nationale
 
- cotisations sociales
 
- loi sur la protection
 
- assurance
 
- numéro de sécurité sociale
 
- demande d’assurance
 
- demande de soins médicaux
 
- assurance sociale
 
- soins médicaux
 
- sécurité sociale 
- grande-bretagne
 
- assurance
    
   
## <a name="us--uk-passport-number"></a>Numéro de passeport États-Unis/Royaume-Uni

### <a name="format"></a>Format

Neuf chiffres

### <a name="pattern"></a>Modèle

Neuf chiffres consécutifs

### <a name="checksum"></a>Somme de contrôle

Non

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- La fonction Func_usa_uk_passport trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_passport est trouvé.

```
<Entity id="178ec42a-18b4-47cc-85c7-d62c92fd67f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_usa_uk_passport" />
        <Match idRef="Keyword_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordpassport"></a>Keyword_passport

- Numéro de passeport 
- 
N° de passeport 
- # Passeport
 
- #Passeport
 
- IDPassport 
- n° passeport
 
- numéropasseport
 
- パスポート 
- パスポート番号
 
- パスポートのNum
 
- パスポート＃
 
- Numéro de passeport 
- 
Passeport n° 
- Passeport numéro
 
- # Passeport
 
- Passeport#
 
- PasseportNon 
- Passeportn °
 
   
## <a name="us-bank-account-number"></a>Numéro de compte bancaire États-Unis

### <a name="format"></a>Format

8-17 chiffres

### <a name="pattern"></a>Modèle

8 à 17 chiffres consécutifs

### <a name="checksum"></a>Somme de contrôle

Non

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- L’expression régulière Regex_usa_bank_account_number trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_usa_Bank_Account est trouvé.

```
<!-- U.S. Bank Account Number -->
<Entity id="a2ce32a8-f935-4bb6-8e96-2a5157672e2c" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_usa_bank_account_number" />
        <Match idRef="Keyword_usa_Bank_Account" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordusabankaccount"></a>Keyword_usa_Bank_Account

- Numéro de compte courant
 
- Compte courant
 
- # compte courant
 
- Numéro compte courant
 
- # compte courant
 
- N° de compte courant
 
- N° de compte courant
 
- Numéro de compte bancaire
 
- # Compte bancaire
 
- Numéro de compte bancaire
 
- # Compte bancaire
 
- N° de compte bancaire
 
- N° de compte bancaire
 
- Numéro de compte d’épargne
 
- Compte d’épargne.
 
- N° de compte d’épargne
 
- Numéro de compte d’épargne
 
- # compte d’épargne
 
- N° de compte d’épargne
 
- N° de compte d’épargne
 
- Numéro de compte de débit
 
- Compte de débit
 
- # Compte de débit
 
- Numéro de compte de débit
 
- # Compte de débit
 
- N° de compte de débit
 
- N° de compte de débit
 
   
## <a name="us-drivers-license-number"></a>Numéro de permis de conduire États-Unis

### <a name="format"></a>Format

Dépend de l’État

### <a name="pattern"></a>Modèle

Dépend de l’État, par exemple, New York :
- Neuf chiffres au format ddd ddd ddd correspondront.
- Neuf chiffres au format ddddddddd ne correspondront pas.

### <a name="checksum"></a>Somme de contrôle

Non

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- La fonction Func_new_york_drivers_license_number trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_[state_name]_drivers_license_name est trouvé.
- Un mot clé figurant dans la liste Keyword_us_drivers_license est trouvé.

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :
- La fonction Func_new_york_drivers_license_number trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_[state_name]_drivers_license_name est trouvé.
- Un mot clé figurant dans la liste Keyword_us_drivers_license_abbreviations est trouvé.
- Aucun mot clé figurant dans la liste Keyword_us_drivers_license n’est trouvé.

```
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_new_york_drivers_license_number" />
        <Match idRef="Keyword_new_york_drivers_license_name" />
        <Match idRef="Keyword_us_drivers_license" />
    </Pattern>
    <Pattern confidenceLevel="65">
        <IdMatch idRef="Func_new_york_drivers_license_number" />
        <Match idRef="Keyword_new_york_drivers_license_name" />
        <Match idRef="Keyword_us_drivers_license_abbreviations" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_us_drivers_license" />
        </Any>
    </Pattern>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordusdriverslicenseabbreviations"></a>Keyword_us_drivers_license_abbreviations

- PC 
- PC 
- CDL 
- SYSTÈMES CDL 
- ID 
- ID 
- # PC 
- 
# PC
 
- # PCD
 
- # PCD
 
- #ID
- 
#IDs
 
- numéro d’identification 
- Numéros d’identification
 
- LIC 
- # PERMIS
 

#### <a name="keywordusdriverslicense"></a>Keyword_us_drivers_license

- DriverLic 
- DriverLics 
- DriverLicense 
- DriverLicenses 
- Lic pilote 
- Pilote Lics 
- Conduire 
- Licences de pilote 
- DriversLic 
- DriversLics 
- Conduire 
- DriversLicenses 
- Lic pilotes 
- Lics pilotes 
- Permis de conduire 
- Licences de pilotes 
- Driver'Lic 
- Driver'Lics 
- Driver'License 
- Driver'Licenses 
- Pilote ' Lic 
- Pilote ' Lics 
- Pilote ' licence 
- Pilote ' licences
- Driver'sLic 
- Driver'sLics 
- Driver'sLicense 
- Driver'sLicenses 
- Lic du pilote 
- Lics permis de conduire 
- Conduire permis de 
- Conduire permis de 
- numéro d’identification
 
- numéros d’identification
 
- # identification
 
- carte d’identité 
- ID de cartes de visite 
- carte d’identification 
- cartes d’identification 
- DriverLic # 
- DriverLics # 
- DriverLicense # 
- DriverLicenses # 
- #Permis conduire 
- 
#Permis conduire
 
- Pilote licence # 
- Licences de pilote # 
- DriversLic # 
- DriversLics # 
- Conduire # 
- DriversLicenses # 
- Pilotes Lic # 
- Pilotes Lics # 
- Licence pilotes # 
- Licences pilotes # 
- #Permisconduire
 
- #Permisconduire
 
- #Permisdeconduire
 
- #Permisdeconduire
 
- #Permis conduire
 
- #Permis conduire
 
- #Permis de conduire
 
- #Permis de conduire
 
- Driver'sLic # 
- Driver'sLics # 
- Driver'sLicense # 
- Driver'sLicenses # 
- #Permisconduire
 
- #Permisconduire
 
- #Permis de conduire
 
- #Permis de conduire
 
- carte d’identité # 
- # cartes d’identité
 
- #carte d’identification
 
- #cartes d’identification
 


#### <a name="keywordstatenamedriverslicensename"></a>Keyword_[state_name]_drivers_license_name

- Abréviation de l’État (par exemple, « NY »)
 
- Nom de l’État (par exemple, « New York »)
    
   
## <a name="us-individual-taxpayer-identification-number-itin"></a>Numéro d'identification fiscale individuel (ITIN) États-Unis

### <a name="format"></a>Format

Neuf chiffres, le premier étant le « 9 », le quatrième le « 7 » ou le « 8 », éventuellement mis en forme avec des espaces ou des tirets

### <a name="pattern"></a>Modèle

Mis en forme :
- Le chiffre « 9 » 
- Deux chiffres 
- Un espace ou un tiret 
- Un « 7 » ou un « 8 » 
- Un chiffre 
- Un espace ou tiret 
- Quatre chiffres

Non mis en forme :
- Le chiffre « 9 » 
- Deux chiffres 
- Un « 7 » ou un « 8 » 
- Cinq chiffres

### <a name="checksum"></a>Somme de contrôle

Non

### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
- La fonction Func_formatted_itin trouve un contenu qui correspond au modèle.
- Au moins une des affirmations suivantes est vraie :
    - Un mot clé figurant dans la liste Keyword_itin est trouvé.
    - La fonction Func_us_address trouve une adresse au format correct.
    - La fonction Func_us_date trouve une date au format correct.
    - Un mot clé figurant dans la liste Keyword_itin_collaborative est trouvé.

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- La fonction Func_unformatted_itin trouve un contenu qui correspond au modèle.
- Au moins une des affirmations suivantes est vraie :
    - Un mot clé figurant dans la liste Keyword_itin_collaborative est trouvé.
    - La fonction Func_us_address trouve une adresse au format correct.
    - La fonction Func_us_date trouve une date au format correct.

```
<!-- U.S. Individual Taxpayer Identification Number (ITIN) -->
<Entity id="e55e2a32-f92d-4985-a35d-a0b269eb687b" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_formatted_itin" />
        <Any minMatches="1">
          <Match idRef="Keyword_itin" />
          <Match idRef="Func_us_address" />
          <Match idRef="Func_us_date" />
          <Match idRef="Keyword_itin_collaborative" />
        </Any>
    </Pattern>
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_unformatted_itin" />
        <Match idRef="Keyword_itin" />
        <Any minMatches="1">
          <Match idRef="Keyword_itin_collaborative" />
          <Match idRef="Func_us_address" />
          <Match idRef="Func_us_date" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keyworditin"></a>Keyword_itin

- contribuable
 
- id fiscal
 
- identification fiscale
 
- itin
 
- ssn 
- tin
 
- sécurité sociale 
- contribuable
 
- itins
 
- id fiscal

 
- contribuable individuel
 

#### <a name="keyworditincollaborative"></a>Keyword_itin_collaborative

- License 
- PC 
- DDN
 
- Birthdate 
- Anniversaire  
- Date of Birth
 
   
## <a name="us-social-security-number-ssn"></a>Numéro de sécurité sociale (SSN) États-Unis

### <a name="format"></a>Format

9 chiffres, qui peuvent être mis en forme ou non mis en forme

> [!NOTE]
> La mise en forme d’un numéro de sécurité sociale émis avant le milieu de l’année 2011 est fixe et certaines parties du numéro doivent se situer dans certaines plages pour qu’il soit valide (mais il n’y a pas de somme de contrôle).

### <a name="pattern"></a>Modèle

Quatre fonctions permettent de rechercher des numéros de sécurité sociale avec quatre différents modèles :
- Func_ssn recherche des numéros de sécurité sociale avec une mise en forme fixe d’avant l’année 2011, mis en forme avec des tirets ou des espaces (ddd-dd-dddd OU ddd dd dddd)
- Func_unformatted_ssn recherche des numéros de sécurité sociale avec une mise en forme fixe d’avant l’année 2011, avec neuf chiffres consécutifs non mis en forme (ddddddddd)
- Func_randomized_formatted_ssn recherche des numéros de sécurité sociale d’après l’année 2011, mis en forme avec des tirets ou des espaces  (ddd-dd-dddd OU ddd dd dddd)
- Func_randomized_unformatted_ssn recherche des numéros de sécurité sociale d’après l’année 2011, avec neuf chiffres consécutifs non mis en forme (ddddddddd)

### <a name="checksum"></a>Somme de contrôle

Non


### <a name="definition"></a>Définition

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :
- La fonction Func_ssn trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_ssn est trouvé.

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :
- La fonction Func_unformatted_ssn trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_ssn est trouvé.

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :
- La fonction Func_randomized_formatted_ssn trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_ssn est trouvé.
- La fonction Func_ssn ne trouve pas de contenu qui correspond au modèle.

Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 55 % si, dans une proximité de 300 caractères :
- La fonction Func_randomized_unformatted_ssn trouve un contenu qui correspond au modèle.
- Un mot clé figurant dans la liste Keyword_ssn est trouvé.
- La fonction Func_unformatted_ssn ne trouve pas de contenu qui correspond au modèle.

```
<!-- U.S. Social Security Number (SSN) -->
    <Entity id="a44669fe-0d48-453d-a9b1-2cc83f2cba77" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_ssn" />
        <Match idRef="Keyword_ssn" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_unformatted_ssn" />
        <Match idRef="Keyword_ssn" />
      </Pattern>
      <Pattern confidenceLevel="65">
        <IdMatch idRef="Func_randomized_formatted_ssn" />
        <Match idRef="Keyword_ssn" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Func_ssn" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="55">
        <IdMatch idRef="Func_randomized_unformatted_ssn" />
        <Match idRef="Keyword_ssn" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Func_unformatted_ssn" />
        </Any>
      </Pattern>
    </Entity>
```

### <a name="keywords"></a>Mots clés

#### <a name="keywordssn"></a>Keyword_ssn

- Sécurité sociale
 
- # sécurité sociale
 
- Sécu sociale
 
- SSN 
- NSS
 
- #NSS
 
- # SS
 
- IDSS
 
   
