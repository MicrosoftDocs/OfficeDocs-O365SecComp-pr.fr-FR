---
title: Éléments recherchés par les fonctions DLP
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/18/2016
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 94349ed4-5351-4ee2-bbda-70813c9ed693
description: Les types d'informations sensibles recherchent un modèle spécifique et le corroborent en garantissant une mise en forme appropriée, en appliquant des checksums et en recherchant des mots clés pertinents ou d'autres informations. Certaines de ces fonctionnalités sont effectuées par des fonctions internes. Cette rubrique décrit ce que ces fonctions recherchent, pour vous aider à comprendre le fonctionnement des types d'informations sensibles prédéfinis.
ms.openlocfilehash: 55c740e892e92902b368b2dcf7b0999cbc60f3ed
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219354"
---
# <a name="what-the-dlp-functions-look-for"></a>Éléments recherchés par les fonctions DLP

La protection contre la perte de données (DLP) inclut des types d’informations sensibles, tels que le numéro de carte de crédit et le numéro de carte de débit de l’Union européenne, qui sont prêts à être utilisés dans vos stratégies DLP. Ces types d’informations sensibles recherchent un modèle spécifique et le corroborent en veillant à l’adéquation de la mise en forme, en appliquant des sommes de contrôle et en recherchant des mots clés pertinents ou d’autres informations. Certaines de ces fonctionnalités sont effectuées par des fonctions internes. Par exemple, le type d’informations sensibles de numéro de carte de crédit utilise une fonction pour rechercher des dates mises en forme comme une date d’expiration, pour aider à confirmer qu’un numéro est un numéro de carte de crédit.
  
Cette rubrique explique ce que ces fonctions recherchent, pour vous aider à comprendre le fonctionnement des types d’informations sensibles prédéfinis. Pour plus d’informations, voir [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).
  
## <a name="funcusdate"></a>Func_us_date

Cette fonction recherche une date au format couramment utilisé aux États-Unis. Cela inclut les formats «mois/jour/année», «mois-jour-année» et «mois de jour du mois». Les noms ou abréviations des mois ne sont pas sensibles à la casse. 
  
Exemples :
  
- 2 décembre 2016
    
- 2 décembre 2016
    
- DEC 02 2016
    
- 12/2/2016
    
- 12/02/16
    
- Déc-2-2016
    
- 12-2-16
    
Noms de mois acceptés :
  
- Anglais
    
  - Janvier, février, mars, avril, mai, juin, juillet, août, septembre, octobre, novembre, décembre
    
  - Jan. fév. Mar. mai du 1er juillet aoû. septembre. Oct. nov. déc
    
## <a name="funceudate"></a>Func_eu_date

Cette fonction recherche une date au format couramment utilisé dans l’Union européenne (et la plupart des lieux, à l’exception des États-Unis). Cela inclut les formats de « jour/mois/année », « jour-mois-année » et « jour mois année ». Les noms ou les abréviations des mois ne respectent pas la casse.
  
Exemples :
  
- 2 déc 2016
    
- 02 déc 2016
    
- 2 déc 16
    
- 2/12/2016
    
- 02/12/16
    
- 2-déc-2016
    
- 2-12-16
    
Noms de mois acceptés :
  
- Anglais
    
  - Janvier, février, mars, avril, mai, juin, juillet, août, septembre, octobre, novembre, décembre
    
  - Jan. fév. Mar. mai du 1er juillet aoû. septembre. Oct. nov. déc
    
- Néerlandais
    
  - januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December
    
  - Jan fév maart avr Mei Jun Jul aoû Sep sept oct OKT nov déc
    
- Français
    
  - janvier, février, mars, avril, mai, juin juillet, août, septembre, octobre, novembre, décembre
    
  - janv. févr. mars avril Maï juin juil. août sept. oct. nov. déc.
    
- Allemand
    
  - jänuar, Februar, März, avril, mai, Juni Juli, août, septembre, oktober, novembre, Dezember
    
  - Jan./Jän. Fév. März avr. Maï Juni Juli aoû. sept. Okt. Nov. Dez.
    
- Italien
    
  - gennaio, febbraio, marzo, Aprile, Maggio, Giugno, luglio, Agosto, Settembre, Ottobre, novembre, dicembre
    
  - Genn. febbr. détériore. avancé. Magg. giugno luglio AG. Sett. Verlag. novembre. DIC.
    
- Portugais
    
  - janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro
    
  - Jan Fev Mar Abr mai Jun Jul a été défini sur le mois de novembre dez
    
- Espagnol
    
  - Enero, febrero, marzo, Abril, Mayo, junio, Julio, Agosto, septiembre, octubre, noviembre, diciembre
    
  - enero fév. marzo abr. Mayo Jun. Jul. agosto sept./Set. oct. nov. DIC.
    
## <a name="funceudate1-deprecated"></a>Func_eu_date1 (déconseillée)

> [!NOTE]
> Cette fonction est déconseillée, car elle prend en charge uniquement les noms de mois portugais, `Func_eu_date` qui sont désormais inclus dans la fonction ci-dessus. 
  
Cette fonction recherche une date dans le format couramment utilisé en Portugais. Le format de cette fonction est le même que `Func_eu_date`, qui diffère uniquement dans la langue utilisée.
  
Exemples :
  
- 2 dez 2016
    
- 02 dez 2016
    
- 2 dez 16
    
- 2/12/2016
    
- 02/12/16
    
- 2-dez-2016
    
- 2-12-16
    
Noms de mois acceptés :
  
- Portugais
    
  - janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro
    
  - Jan Fev Mar Abr mai Jun Jul a été défini sur le mois de novembre dez
    
## <a name="funceudate2-deprecated"></a>Func_eu_date2 (déconseillée)

> [!NOTE]
> Cette fonction est déconseillée, car elle prend en charge uniquement les noms de mois néerlandais, `Func_eu_date` qui sont désormais inclus dans la fonction ci-dessus. 
  
Cette fonction recherche une date dans le format couramment utilisé en Néerlandais. Le format de cette fonction est le même que `Func_eu_date`, qui diffère uniquement dans la langue utilisée.
  
Exemples :
  
- 2 Mei 2016
    
- 02 Mei 2016
    
- 2 Mei 16
    
- 2/12/2016
    
- 02/12/16
    
- 2-Mei-2016
    
- 2-12-16
    
Noms de mois acceptés :
  
- Néerlandais
    
  - januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December
    
  - Jan fév maart avr Mei Jun Jul aoû Sep sept oct OKT nov déc
    
## <a name="funcexpirationdate"></a>Func_expiration_date

Cette fonction recherche une date dans les formats couramment utilisés par les cartes de crédit et de débit, ce qui exclut les jours en faveur des mois. Cette fonction correspond aux dates au format «mois/année», «mois-année», «[nom du mois] année» et «[abréviation mois-année]». Les noms ou abréviations des mois ne sont pas sensibles à la casse.
  
Exemples
  
- MM/AA, par exemple, 01/11 ou 1/11
    
- MM/AAAA, par exemple, 01/2011 ou 1/2011
    
- MM-AA, par exemple, 01-22 ou 1-11
    
- MM-AAAA, par exemple, 01-2000 ou 1-2000
    
Les formats suivants prennent en charge AA ou AAAA :
  
- Mois-AAAA, par exemple, jan-2010, janvier-2010, jan-10 ou janvier-10
    
- Mois AAAA, par exemple, « janvier 2010 », « jan 2010 », « janvier 10 » ou « jan 10 »
    
- MoisAAAA, par exemple, « janvier2010 », « jan2010 », « janvier10 » ou « jan10 »
    
- Mois/aaaa--par exemple, «janvier/2010» ou «Jan/2010», «janvier/10» ou «Jan/10»
    
Noms de mois acceptés :
  
- Anglais
    
  - Janvier, février, mars, avril, mai, juin, juillet, août, septembre, octobre, novembre, décembre
    
  - Jan Fév Mar Avr mai juin septembre sept octobre déc
    
## <a name="funcusaddress"></a>Func_us_address

Cette fonction recherche un nom d’état américain ou son abréviation postale, suivi d’un code postal valide, au format utilisé dans les adresses postales. Le code postal doit être l’un des codes postaux corrects qui sont associés au nom de l’état américain ou à son abréviation. Le nom de l’état américain et le code postal ne doivent pas être séparés par des signes de ponctuation ou des lettres.
  
Exemples :
  
- Washington 98052
    
- Washington 98052-9998
    
- WA 98052
    
- WA 98052-9998
    

