---
title: Éléments recherchés par les fonctions DLP
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/18/2016
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 94349ed4-5351-4ee2-bbda-70813c9ed693
description: Les types d’informations sensibles rechercher un modèle spécifique et il corroborer en s’assurant la mise en forme appropriée, appliquer les totaux de contrôle et vous recherchez des mots clés pertinents ou d’autres informations. Certaines fonctionnalités est effectuée par des fonctions internes. Cette rubrique explique ce que ces fonctions Rechercher, pour vous aider à comprendre comment fonctionnent les types d’informations sensibles prédéfinis.
ms.openlocfilehash: 510f98e2b4e1d2480550f11026cf445be6ffc931
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "23013758"
---
# <a name="what-the-dlp-functions-look-for"></a>Éléments recherchés par les fonctions DLP

La protection contre la perte de données (DLP) inclut des types d’informations sensibles, tels que le numéro de carte de crédit et le numéro de carte de débit de l’Union européenne, qui sont prêts à être utilisés dans vos stratégies DLP. Ces types d’informations sensibles recherchent un modèle spécifique et le corroborent en veillant à l’adéquation de la mise en forme, en appliquant des sommes de contrôle et en recherchant des mots clés pertinents ou d’autres informations. Certaines de ces fonctionnalités sont effectuées par des fonctions internes. Par exemple, le type d’informations sensibles de numéro de carte de crédit utilise une fonction pour rechercher des dates mises en forme comme une date d’expiration, pour aider à confirmer qu’un numéro est un numéro de carte de crédit.
  
Cette rubrique explique ce que ces fonctions recherchent, pour vous aider à comprendre le fonctionnement des types d’informations sensibles prédéfinis. Pour plus d’informations, voir [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).
  
## <a name="funcusdate"></a>Func_us_date

Cette fonction recherche une date au format couramment utilisé aux États-Unis. Cela inclut les formats « jour/mois/année », « mois-jour-année », « mois l’année jour ». Les noms ou les abréviations de mois ne respectent pas la casse. 
  
Exemples :
  
- 2 décembre 2016
    
- 2 décembre 2016
    
- déc 2016 02
    
- 12/2/2016
    
- 16/12/02
    
- 2-déc-2016
    
- 12-2-16.
    
Noms de mois acceptés :
  
- Anglais
    
  - Janvier, février, mars, avril, mai, juin, juillet, août, septembre, octobre, novembre, décembre
    
  - Janvier, février mars avril mai juin juillet août septembre octobre novembre décembre.
    
## <a name="funceudate"></a>Func_eu_date

Cette fonction recherche une date au format couramment utilisé dans l’Union européenne (et la plupart des lieux, à l’exception des États-Unis). Cela inclut les formats de « jour/mois/année », « jour-mois-année » et « jour mois année ». Les noms ou les abréviations des mois ne respectent pas la casse.
  
Exemples :
  
- 2 décembre 2016
    
- 02 déc 2016
    
- 2 16 décembre
    
- 2/12/2016
    
- 16/12/02
    
- 2-déc-2016
    
- 16-12-2
    
Noms de mois acceptés :
  
- Anglais
    
  - Janvier, février, mars, avril, mai, juin, juillet, août, septembre, octobre, novembre, décembre
    
  - Janvier, février mars avril mai juin juillet août septembre octobre novembre décembre.
    
- Néerlandais
    
  - januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December
    
  - Jan février entrant maart avr mei juin juillet août sep sept OPO okt nov déc
    
- Français
    
  - débute janvier, février, mars, avril, mai, juin juillet, août, septembre, octobre, novembre, décembre
    
  - janv. févr. mars avril mai juin juil. août septembre. octobre novembre. déc.
    
- Allemand
    
  - jänuar, février, märz, avril, mai, juni juli, août, septembre, oktober, novembre, dezember
    
  - Jan. / Jän. Février März May avril Juni Juli août septembre Okt. Dez novembre.
    
- Italien
    
  - gennaio, febbraio, marzo, aprile, maggio, giugno, luglio, agosto, settembre, ottobre, novembre, dicembre
    
  - Genn. febbr. Mar. avr. magg. giugno luglio ag. sett. ott. nov. dictionnaire.
    
- Portugais
    
  - janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro
    
  - Jan fev mar TBD May juin, juillet remonte énoncées dez nov
    
- Espagnol
    
  - enero, febrero, marzo, abril, mayo, junio, julio, agosto, septiembre, octubre, noviembre, diciembre
    
  - enero février. marzo abr. mayo jun. juillet. set/agosto septembre. octobre novembre. dictionnaire.
    
## <a name="funceudate1-deprecated"></a>Func_eu_date1 (déconseillée)

> [!NOTE]
> Cette fonction est déconseillée, car elle prend en charge uniquement les noms de mois portugais, qui sont désormais inclus dans le `Func_eu_date` fonction ci-dessus. 
  
Cette fonction recherche une date au format couramment utilisé en portugais. Le format de cette fonction est identique à `Func_eu_date`, différentes uniquement dans la langue utilisée.
  
Exemples :
  
- 2 Dez 2016
    
- 02 dez 2016
    
- 2 Dez 16
    
- 2/12/2016
    
- 16/12/02
    
- 2-Dez-2016
    
- 16-12-2
    
Noms de mois acceptés :
  
- Portugais
    
  - janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro
    
  - Jan fev mar TBD May juin, juillet remonte énoncées dez nov
    
## <a name="funceudate2-deprecated"></a>Func_eu_date2 (déconseillée)

> [!NOTE]
> Cette fonction est déconseillée, car elle prend en charge uniquement les noms de mois néerlandais, qui sont désormais inclus dans le `Func_eu_date` fonction ci-dessus. 
  
Cette fonction recherche une date au format couramment utilisé en néerlandais. Le format de cette fonction est identique à `Func_eu_date`, différentes uniquement dans la langue utilisée.
  
Exemples :
  
- 2 Mei 2016
    
- 02 mei 2016
    
- 2 Mei 16
    
- 2/12/2016
    
- 16/12/02
    
- 2-Mei-2016
    
- 16-12-2
    
Noms de mois acceptés :
  
- Néerlandais
    
  - januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December
    
  - Jan février entrant maart avr mei juin juillet août sep sept OPO okt nov déc
    
## <a name="funcexpirationdate"></a>Func_expiration_date

Cette fonction recherche une date dans les formats couramment utilisées par les cartes de crédit et de débit, qui excluent les jours par mois. Cette fonction correspondent à des dates dans le format de « mois/année », « mois-année », « [nom du mois] » ou « [abréviation du mois] ans ». Les noms ou les abréviations de mois ne respectent pas la casse.
  
Exemples
  
- MM/AA, par exemple, 01/11 ou 1/11
    
- MM/AAAA, par exemple, 01/2011 ou 1/2011
    
- MM-AA, par exemple, 01-22 ou 1-11
    
- MM-AAAA, par exemple, 01-2000 ou 1-2000
    
Les formats suivants prennent en charge AA ou AAAA :
  
- Mois-AAAA, par exemple, jan-2010, janvier-2010, jan-10 ou janvier-10
    
- Mois AAAA, par exemple, « janvier 2010 », « jan 2010 », « janvier 10 » ou « jan 10 »
    
- MoisAAAA, par exemple, « janvier2010 », « jan2010 », « janvier10 » ou « jan10 »
    
- Mois/aaaa, par exemple, ' janvier/2010' ou « Jan/2010 » ou « 10/janvier » ou « 10/Jan »
    
Noms de mois acceptés :
  
- Anglais
    
  - Janvier, février, mars, avril, mai, juin, juillet, août, septembre, octobre, novembre, décembre
    
  - Janvier, février Mar avr mai juin juillet août septembre Oct Nov Déc
    
## <a name="funcusaddress"></a>Func_us_address

Cette fonction recherche un nom d’état américain ou son abréviation postale, suivi d’un code postal valide, au format utilisé dans les adresses postales. Le code postal doit être l’un des codes postaux corrects qui sont associés au nom de l’état américain ou à son abréviation. Le nom de l’état américain et le code postal ne doivent pas être séparés par des signes de ponctuation ou des lettres.
  
Exemples :
  
- Washington 98052
    
- Washington 98052-9998
    
- WA 98052
    
- WA 98052-9998
    

