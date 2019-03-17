---
title: Créer un type d’informations sensibles personnalisé dans le Centre de Conformité et Sécurité Office 365 PowerShell
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Découvrez comment créer et importer un type d’informations sensibles personnalisé pour DLP dans le Centre de Conformité et Sécurité Office 365.
ms.openlocfilehash: bf917ac40f98ec19332aac90f2d954d44b9a834d
ms.sourcegitcommit: 8657e003ab1ff49113f222d1ee8400eff174cb54
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2019
ms.locfileid: "30639121"
---
# <a name="create-a-custom-sensitive-information-type-in-office-365-security--compliance-center-powershell"></a>Création d’un type personnalisé d’informations sensibles dans le Centre de Conformité et Sécurité Office 365 PowerShell

La protection contre la perte de données (DLP) dans Office 365 inclut de nombreux [types d’informations sensibles](what-the-sensitive-information-types-look-for.md) intégrés qui sont prêts à l’emploi dans vos stratégies DLP. Ces types intégrés permettent d’identifier et de protéger les numéros de carte de crédit, les numéros de compte bancaire, les numéros de passeport, et bien plus encore. 
  
Cependant, si vous devez identifier et protéger un autre type d’informations sensibles (par exemple, l’ID d’un employé qui utilise un format spécifique de votre organisation), vous pouvez créer un type personnalisé d’informations sensibles. Un type d’informations sensibles est défini dans un fichier XML appelé _package de règles_.
  
Cette rubrique vous explique comment créer un fichier XML qui définit votre propre type d’informations sensibles personnalisé. Vous devez savoir comment créer une expression régulière. Par exemple, cette rubrique permet de créer un type d’informations sensibles personnalisé qui identifie un ID d’employé. Vous pouvez utiliser cet exemple de code XML comme point de départ pour votre propre fichier XML.
  
Après avoir créé un fichier XML correct, vous pouvez le charger sur Office 365 à l’aide de Office 365 PowerShell. Ensuite, vous êtes prêt à utiliser votre type d’informations sensibles personnalisé dans vos stratégies DLP et à vérifier qu’il détecte bien les informations sensibles comme prévu.

> [!NOTE]
> Vous pouvez également créer des types d’informations sensibles personnalisés moins complexes dans le Centre de Conformité de  l’interface utilisateur et de Sécurité. Pour plus d’informations, voir[Créer un type d’informations sensibles personnalisé](create-a-custom-sensitive-information-type.md).

## <a name="important-disclaimer"></a>Clause d’exclusion de responsabilité importante

En raison des différences dans les environnements client et les exigences de correspondance de contenu, le support Microsoft ne peut pas fournir de définitions de correspondance de contenu personnalisée, par exemple, en définissant des classifications personnalisées ou des modèles d’expressions régulières (« RegEx »). Pour le développement, le test et le débogage liés à la correspondance de contenu personnalisée, les clients Office 365 doivent s’appuyer sur leurs ressources informatiques internes ou recourir à une ressource de conseil externe telle que Microsoft Consulting Services (MCS). Les ingénieurs du support peuvent fournir une assistance limitée pour la fonctionnalité, mais ils ne peuvent pas fournir de garanties en matière d’adéquation entre les obligations ou exigences d’un client et le développement de correspondances de contenu personnalisées. Dans le cadre de l’assistance susceptible d’être fournie, des exemples de modèles d’expression régulière peuvent être donnés à des fins de test. Le support peut également aider à résoudre un problème de modèle RegEx existant dont le déclenchement ne fonctionne pas comme prévu avec un exemple de contenu spécifique unique.

 Pour plus d’informations sur le moteur Boost.RegEx (anciennement RegEx ++) utilisé pour traiter le texte, consultez [Boost.Regex 5.1.3](https://www.boost.org/doc/libs/1_68_0/libs/regex/doc/html/).
    
## <a name="sample-xml-of-a-rule-package"></a>Exemple de code XML d’un package de règles

Voici l’exemple de code XML du package de règles que nous allons créer dans cette rubrique. Les éléments et les attributs sont expliqués dans les sections ci-après.
  
```
<?xml version="1.0" encoding="UTF-16"?>
<RulePackage xmlns="http://schemas.microsoft.com/office/2011/mce">
<RulePack id="DAD86A92-AB18-43BB-AB35-96F7C594ADAA">
    <Version build="0" major="1" minor="0" revision="0"/>
    <Publisher id="619DD8C3-7B80-4998-A312-4DF0402BAC04"/>
    <Details defaultLangCode="en-us">
        <LocalizedDetails langcode="en-us">
            <PublisherName>Contoso</PublisherName>
            <Name>Employee ID Custom Rule Pack</Name>
            <Description>
            This rule package contains the custom Employee ID entity.
            </Description>
        </LocalizedDetails>
    </Details>
</RulePack>
<Rules>
<!-- Employee ID -->
    <Entity id="E1CC861E-3FE9-4A58-82DF-4BD259EAB378" patternsProximity="300" recommendedConfidence="70">
        <Pattern confidenceLevel="60">
            <IdMatch idRef="Regex_employee_id"/>
        </Pattern>
        <Pattern confidenceLevel="70">
            <IdMatch idRef="Regex_employee_id"/>
            <Match idRef="Func_us_date"/>
        </Pattern>
        <Pattern confidenceLevel="80">
            <IdMatch idRef="Regex_employee_id"/>
            <Match idRef="Func_us_date"/>
            <Any minMatches="1">
                <Match idRef="Keyword_badge" minCount="2"/>
                <Match idRef="Keyword_employee"/>
            </Any>
            <Any minMatches="0" maxMatches="0">
                <Match idRef="Keyword_false_positives_local"/>
                <Match idRef="Keyword_false_positives_intl"/>
            </Any>
        </Pattern>
    </Entity>
    <Regex id="Regex_employee_id">(\s)(\d{9})(\s)</Regex>
    <Keyword id="Keyword_employee">
        <Group matchStyle="word">
            <Term>Identification</Term>
            <Term>Contoso Employee</Term>
        </Group>
    </Keyword>
    <Keyword id="Keyword_badge">
        <Group matchStyle="string">
            <Term>card</Term>
            <Term>badge</Term>
            <Term caseSensitive="true">ID</Term>
        </Group>
    </Keyword>
    <Keyword id="Keyword_false_positives_local">
        <Group matchStyle="word">
            <Term>credit card</Term>
            <Term>national ID</Term>
        </Group>
    </Keyword>
    <Keyword id="Keyword_false_positives_intl">
        <Group matchStyle="word">
            <Term>identity card</Term>
            <Term>national ID</Term>
            <Term>EU debit card</Term>
        </Group>
    </Keyword>
    <LocalizedStrings>
        <Resource idRef="E1CC861E-3FE9-4A58-82DF-4BD259EAB378">
            <Name default="true" langcode="en-us">Employee ID</Name>
            <Description default="true" langcode="en-us">
            A custom classification for detecting Employee IDs.
            </Description>
            <Name default="true" langcode="de-de">Name for German locale</Name>
            <Description default="true" langcode="de-de">
            Description for German locale.
            </Description>
        </Resource>
    </LocalizedStrings>
</Rules>
</RulePackage>
```

## <a name="what-are-your-key-requirements-rule-entity-pattern-elements"></a>Quelles sont vos principales exigences ? [éléments Rule, Entity et Pattern]

Avant de commencer, il est utile de comprendre la structure de base du schéma XML d’une règle et comment utiliser cette structure pour définir votre type d’informations sensibles personnalisé afin qu’il identifie le contenu approprié.
  
Une règle (Rule) définit une ou plusieurs entités (Entity ; types d’informations sensibles), et chaque entité définit un ou plusieurs modèles (Pattern). Un modèle est l’élément recherché par la stratégie DLP lorsqu’elle évalue du contenu tel que les e-mails et les documents.
  
Note rapide sur la terminologie : si vous connaissez bien les stratégies DLP, vous savez qu’une stratégie contient une ou plusieurs règles composées de conditions et d’actions. Cependant, dans cette rubrique, le balisage XML utilise l’élément Rule pour désigner les modèles qui définissent une entité, également appelé type d’informations sensibles. Par conséquent, dans cette rubrique, lorsque vous voyez l’élément Rule, pensez entité ou type d’informations sensibles, mais pas conditions et actions.
  
### <a name="simplest-scenario-entity-with-one-pattern"></a>Scénario le plus simple : entité avec un modèle

Voici le scénario le plus simple : vous souhaitez que votre stratégie DLP identifie le contenu qui contient les ID d’employé de votre organisation mis au format d’un nombre à neuf chiffres. Le modèle fait donc référence à une expression régulière contenue dans la règle qui identifie le nombre à neuf chiffres. Tout contenu comprenant un nombre à neuf chiffres satisfait le modèle.
  
![Diagramme d’une entité avec un modèle](media/4cc82dcf-068f-43ff-99b2-bac3892e9819.png)
  
Même s’il est simple, ce modèle peut identifier de nombreux faux positifs en faisant correspondre du contenu comprenant un nombre à neuf chiffres qui n’est pas nécessairement un ID d’employé.
  
### <a name="more-common-scenario-entity-with-multiple-patterns"></a>Scénario le plus courant : entité avec plusieurs modèles

Pour cette raison, il est plus courant de définir une entité à l’aide de plusieurs modèles, où ces derniers identifient la preuve à l’appui (par exemple, un mot clé ou une date) en plus de l’entité (par exemple, un nombre à neuf chiffres).
  
Par exemple, pour augmenter la probabilité d’identifier le contenu qui contient un ID d’employé, vous pouvez définir un autre modèle qui identifie également une date d’embauche, et définir un autre modèle qui identifie une date d’embauche et un mot clé (par exemple, « ID d’employé ») en plus du nombre à neuf chiffres.
  
![Diagramme d’une entité avec plusieurs modèle](media/c8dc2c9d-00c6-4ebc-889a-53b41a90024a.png)
  
Voici quelques aspects importants de cette structure à prendre en compte :
  
- Les modèles qui nécessitent davantage de preuves ont un niveau de confiance supérieur. Ceci est utile, car lorsque vous utilisez ultérieurement ce type d’informations sensibles dans une stratégie DLP, vous pouvez utiliser des actions plus restrictives (par exemple, le blocage de contenu) avec uniquement les correspondances de confiance les plus élevées, et vous pouvez utiliser les actions moins restrictives (par exemple, envoyer une notification) avec les correspondances de confiance inférieures.
    
- Les éléments de soutien IdMatch et Match font référence à des regex (expressions régulières) et à des mots clés qui sont des enfants de l’élément Rule, pas de l’élément Pattern. Ces éléments de soutien sont référencés par le modèle, mais inclus dans la règle. Cela signifie qu’une seule définition d’un élément de soutien, par exemple, une expression régulière ou une liste de mots clés, peut être référencée par plusieurs entités et modèles.
    
## <a name="what-entity-do-you-need-to-identify-entity-element-id-attribute"></a>Quelle entité devez-vous identifier ? [élément Entity, attribut id]

Une entité est un type d’informations sensibles, tel qu’un numéro de carte de crédit, associé à un modèle bien défini. Chaque entité possède un GUID unique en tant qu’ID.
  
### <a name="name-the-entity-and-generate-its-guid"></a>Nommer l’entité et générer son GUID

Ajoutez les éléments Rules et Entity. Ensuite, ajoutez un commentaire qui contient le nom de votre entité personnalisée, dans cet exemple, « Employee ID » (ID d’employé). Plus tard, vous allez ajouter le nom de l’entité à la section de chaînes localisées et ce nom est celui qui apparaît dans l’interface utilisateur lorsque vous créez une stratégie DLP.
  
Ensuite, générez un GUID pour votre entité. Il existe plusieurs méthodes pour générer des GUID, mais vous pouvez le faire facilement dans PowerShell en saisissant [guid]::NewGuid(). Plus tard, vous ajouterez également le GUID de l’entité à la section de chaînes localisées.
  
![Balisage XML montrant les éléments Rules et Entity](media/c46c0209-0947-44e0-ac3a-8fd5209a81aa.png)
  
## <a name="what-pattern-do-you-want-to-match-pattern-element-idmatch-element-regex-element"></a>Quel modèle voulez-vous faire correspondre [élément Pattern, élément IdMatch et élément Regex]

Le modèle contient la liste des éléments recherchés par le type d’informations sensibles. Cela peut inclure des regex, des mots clés et des fonctions intégrées (qui effectuent des tâches telles que l’exécution des expressions régulières pour rechercher des dates ou des adresses). Ces types d’informations sensibles peuvent avoir plusieurs modèles avec des niveaux de confiance uniques.
  
Le point commun de tous les modèles suivants est qu’ils référencent tous la même expression régulière, qui recherche un nombre à neuf chiffres (\d{9}) entre espaces (\s) … (\s). Cette expression régulière est référencée par l’élément IdMatch et est la condition requise commune à tous les modèles qui recherchent l’entité Employee ID. IdMatch est l’identificateur que le modèle cherche à faire correspondre, par exemple, comme ID d’employé, numéro de carte de crédit ou numéro de sécurité sociale. Un élément Pattern doit avoir exactement un élément IdMatch.
  
![Balisage XML montrant plusieurs éléments Pattern référençant un seul élément Regex](media/8f3f497b-3b8b-4bad-9c6a-d9abf0520854.png)
  
Lorsqu’il est satisfait, un modèle renvoie un nombre et un niveau de confiance, que vous pouvez utiliser dans les conditions dans votre stratégie DLP. Lorsque vous ajoutez une condition de détection d’un type d’informations sensibles à une stratégie DLP, vous pouvez modifier le nombre et le niveau de confiance comme illustré ici. Le niveau de confiance (également appelée précision de correspondance) est expliqué plus loin dans cette rubrique.
  
![Nombre d’instances et options de précision de correspondance](media/11d0b51e-7c3f-4cc6-96d8-b29bcdae1aeb.png)
  
Lorsque vous créez une expression régulière, n’oubliez pas que des problèmes peuvent survenir. Par exemple, si vous écrivez et chargez une regex qui identifie trop de contenu, cela peut nuire aux performances. Pour en savoir plus sur ces problèmes potentiels, consultez la section ultérieure [Problèmes de validation éventuels à prendre en compte](#potential-validation-issues-to-be-aware-of).
  
## <a name="do-you-want-to-require-additional-evidence-match-element-mincount-attribute"></a>Voulez-vous demander des preuves supplémentaires ? [élément Match, attribut minCount]

En plus de l’élément IdMatch, un modèle peut utiliser l’élément Match pour demander des preuves à l’appui supplémentaires, telles qu’un mot clé, une regex, une date ou une adresse.
  
Un élément Pattern peut comporter plusieurs éléments Match ; ces éléments sont inclus directement dans l’élément Pattern ou combinés à l’aide de l’élément Any. Les éléments Match sont joints par un opérateur implicite AND ; tous les éléments Match doivent être satisfaits pour que le modèle corresponde. Vous pouvez utiliser l’élément Any pour introduire les opérateurs AND ou OR (plus d’informations dans une section ultérieure).
  
Vous pouvez utiliser l’attribut facultatif minCount pour spécifier le nombre d’instances d’une correspondance qui doivent être trouvées pour chaque élément Match. Par exemple, vous pouvez spécifier qu’un modèle est satisfait uniquement lorsqu’au moins deux mots clés d’une liste de mots clés sont trouvés.
  
![Balisage XML montrant l’élément Match avec l’attribut minOccurs](media/607f6b5e-2c7d-43a5-a131-a649f122e15a.png)
  
### <a name="keywords-keyword-group-and-term-elements-matchstyle-and-casesensitive-attributes"></a>Mots clés [éléments Keyword, Group et Term, attributs matchStyle et caseSensitive]

Lorsque vous identifiez les informations sensibles, telles qu’un ID d’employé, vous pouvez demander des mots clés comme preuve probante. Par exemple, en plus de faire correspondre un nombre à neuf chiffres, vous souhaiterez peut-être rechercher des mots tels que « carte », « badge » ou « ID ». Pour ce faire, utilisez l’élément Keyword. L’élément Keyword possède l’attribut id qui peut être référencé par plusieurs éléments Match dans plusieurs modèles ou entités.
  
Les mots clés sont inclus sous forme de liste d’éléments Term dans un élément Group. L’élément Group possède un attribut matchStyle avec deux valeurs possibles :
  
- **matchStyle="word"** La correspondance de mots identifie des mots entiers entourés par des espaces ou d’autres séparateurs. Vous devez toujours utiliser « word », sauf si vous devez faire correspondre des parties de mots ou des mots dans des langues asiatiques. 
    
- **matchStyle="string"** La correspondance de chaînes identifie les chaînes, peu importe ce qui les entoure. Par exemple, « id » correspondra à « bid» et à « idea ». Utilisez « string » uniquement lorsque vous recherchez des mots asiatiques ou si votre mot clé est inclus dans d’autres chaînes. 
    
Enfin, vous pouvez utiliser l’attribut caseSensitive de l’élément Term pour préciser que le contenu doit correspondre exactement au mot clé, notamment les lettres minuscules et majuscules.
  
![Balisage XML montrant les éléments Match référençant des mots clés](media/e729ba27-dec6-46f4-9242-584c6c12fd85.png)
  
### <a name="regular-expressions-regex-element"></a>Expressions régulières [élément Regex]

Dans cet exemple, l’entité d’ID d’employé utilise déjà l’élément IdMatch pour référencer une regex pour le modèle (un nombre à neuf chiffres entouré d’espaces). De plus, un modèle peut utiliser un élément Match pour référencer un élément Regex supplémentaire afin d’identifier la preuve probante, par exemple un nombre de cinq ou neuf chiffres sous la forme d’un code postal des États-Unis.
  
### <a name="additional-patterns-such-as-dates-or-addresses-built-in-functions"></a>Autres modèles tels que des dates ou des adresses [fonctions intégrées]

En plus des types d’informations sensibles intégrés, la DLP inclut également des fonctions intégrées qui peuvent identifier une preuve probante telle qu’une date américaine, une date européenne, une date d’expiration ou une adresse des États-Unis. La DLP ne prend pas en charge le chargement de fonctions personnalisées, mais lorsque vous créez un type d’informations sensibles personnalisé, votre entité peut référencer les fonctions intégrées.
  
Par exemple, une date figure sur les badges d’ID d’employé. Cette entité personnalisée peut donc utiliser la fonction intégrée `Func_us_date` pour identifier une date au format utilisé aux États-Unis. 
  
Pour obtenir plus d’informations, consultez l’article [Éléments recherchés par les fonctions DLP](what-the-dlp-functions-look-for.md).
  
![Balisage XML montrant les éléments Match référençant une fonction intégrée](media/dac6eae3-9c52-4537-b984-f9f127cc9c33.png)
  
## <a name="different-combinations-of-evidence-any-element-minmatches-and-maxmatches-attributes"></a>Différentes combinaisons de preuves [élément Any, attributs minMatches et maxMatches]

Dans un élément Pattern, tous les éléments IdMatch et Match sont joints par un opérateur implicite AND : toutes les correspondances doivent être satisfaites pour que le modèle soit satisfait. Cependant, vous pouvez créer une logique de correspondance plus flexible en utilisant l’élément Any afin de regrouper des éléments Match. Par exemple, vous pouvez utiliser l’élément Any pour faire correspondre tous les sous-ensembles, aucun sous-ensemble ou un sous-ensemble exact de ses éléments Match enfants.
  
L’élément Any a des attributs minMatches et maxMatches facultatifs que vous pouvez utiliser pour définir le nombre d’éléments Match enfants qui doivent être satisfaits pour que le modèle corresponde. Notez que ces attributs définissent le nombre d’éléments Match qui doivent être satisfaits, pas le nombre d’instances de preuves trouvées pour les correspondances. Pour définir un nombre minimal d’instances pour une correspondance spécifique, par exemple, deux mots clés d’une liste, utilisez l’attribut minCount d’un élément Match (voir ci-dessus).
  
### <a name="match-at-least-one-child-match-element"></a>Faire correspondre au moins un élément Match enfant

Si vous voulez exiger qu’au moins un nombre minimal d’éléments Match corresponde, vous pouvez utiliser l’attribut minMatches. En effet, ces éléments Match sont joints par un opérateur implicite OR. Cet élément Any est satisfait si une date au format américain ou un mot clé d’une liste est trouvé.
  
![Balisage XML montrant l’élément Any avec l’attribut minMatches](media/385db1b1-571b-4a05-81b3-db28f5099c17.png)
  
### <a name="match-an-exact-subset-of-any-children-match-elements"></a>Faire correspondre un sous-ensemble exact d’éléments Match enfants

Si vous voulez exiger qu’un nombre exact d’éléments Match corresponde, vous pouvez définir les attributs minMatches et maxMatches sur la même valeur. Cet élément Any est satisfait uniquement si une seule date ou un seul mot clé est trouvé (si plusieurs dates ou mots clés sont trouvés, le modèle ne correspond pas).
  
![Balisage XML montrant l’élément Any avec les attributs minMatches et maxMatches](media/97b10002-7781-42e8-ac5a-20ad8c5a887e.png)
  
### <a name="match-none-of-children-match-elements"></a>Faire correspondre tous les enfants Match enfants

Si vous voulez exiger l’absence de preuve spécifique pour qu’un modèle soit satisfait, vous pouvez définir les attributs minMatches et maxMatches sur 0. Cela est utile si vous avez une liste de mots clés ou d’autres preuves susceptibles d’indiquer de faux positifs.
  
Par exemple, l’entité d’ID d’employé recherche le mot clé « carte », car il peut désigner une « carte d’identité ». Toutefois, si « carte » apparaît uniquement dans l’expression « carte de crédit », il est peu probable que « carte » dans ce contenu signifie « carte d’identité ». Par conséquent, vous pouvez ajouter « carte de crédit » comme mot clé à une liste de termes que vous voulez exclure de la satisfaction du modèle.
  
![Balisage XML montrant la valeur de l’attribut maxMatches égale à zéro](media/f81d44e5-3db8-48a8-8919-f483a386afdf.png)
  
## <a name="how-close-to-the-entity-must-the-other-evidence-be-patternsproximity-attribute"></a>Quel doit être le degré de proximité de l’entité par rapport à l’autre preuve ? [attribut patternsProximity]

Votre type d’informations sensibles recherche un modèle qui représente un ID d’employé et dans le cadre de ce modèle, il recherche également comme preuve probante un mot clé tel que « ID ». Il est logique que plus la proximité de cette preuve est élevée, plus le modèle est susceptible d’être un ID d’employé. Vous pouvez déterminer le degré de proximité d’autres preuves par rapport à l’entité dans le modèle à l’aide de l’attribut obligatoire patternsProximity de l’élément Entity.
  
![Balisage XML montrant l’attribut patternsProximity](media/e97eb7dc-b897-4e11-9325-91c742d9839b.png)
  
Pour chaque modèle de l’entité, la valeur de l’attribut patternsProximity définit la distance (en caractères Unicode) à partir de l’emplacement IdMatch pour toutes les autres correspondances spécifiées pour ce modèle. La fenêtre de proximité est ancrée par l’emplacement IdMatch. La fenêtre s’étend à gauche et à droite de l’IdMatch.
  
![Diagramme de la fenêtre de proximité](media/b593dfd1-5eef-4d79-8726-a28923f7c31e.png)
  
L’exemple indiqué ci-après illustre comment la fenêtre de proximité affecte la correspondance du modèle là où l’élément IdMatch requiert au moins une correspondance probante de mot clé ou de date pour l’entité personnalisée d’ID d’employé. Seul ID1 correspond, car pour ID2 et ID3, seule une preuve probante partielle (voire aucune preuve probante) a été détectée au sein de la fenêtre de proximité.
  
![Diagramme de la fenêtre de proximité et de preuves probantes](media/dc68e38e-dfa1-45b8-b204-89c8ba121f96.png)
  
Notez que pour la messagerie, le corps du message et chaque pièce jointe sont traités comme des éléments distincts. Cela signifie que la fenêtre de proximité ne s’étend pas au-delà de chacun de ces éléments. Pour chaque élément (pièce jointe ou corps), l’attribut idMatch et la preuve probante doivent résider dans cet élément.
  
## <a name="what-are-the-right-confidence-levels-for-different-patterns-confidencelevel-attribute-recommendedconfidence-attribute"></a>Quels sont les niveaux de confiance appropriés pour les différents modèles ? [attributs confidenceLevel et recommendedConfidence]

Plus un modèle nécessite de preuves, plus vous pouvez être certain qu’une entité (par exemple, l’ID d’employé) a effectivement été identifiée lorsque le modèle a été mis en correspondance. Par exemple, vous pouvez davantage compter sur un modèle qui nécessite un numéro d’identification à neuf chiffres, une date d’embauche et un mot clé situés à proximité immédiate les uns des autres, que sur un modèle qui nécessite uniquement un numéro d’identification à neuf chiffres.
  
L’élément Pattern possède un attribut confidenceLevel obligatoire. Vous pouvez considérer la valeur confidenceLevel (un nombre entier compris entre 1 et 100) comme un ID unique pour chaque modèle d’une entité (les modèles d’une entité doivent avoir des niveaux de confiance distincts que vous attribuez). La valeur précise de l’entier n’a pas d’importance : sélectionnez simplement un nombre ayant du sens pour votre équipe de conformité. Une fois que vous chargez votre type d’informations sensibles personnalisé et créez une stratégie DLP, vous pouvez référencer ces niveaux de confiance dans les conditions des règles que vous créez.
  
![Balisage XML montrant les éléments Pattern avec des valeurs différentes pour l’attribut confidenceLevel](media/301e0ba1-2deb-4add-977b-f6e9e18fba8b.png)
  
En plus de l’attribut confidenceLevel de chaque modèle, l’entité possède un attribut recommendedConfidence. L’attribut de confiance recommandé est assimilable au niveau de confiance par défaut de la règle. Lorsque vous créez une règle dans une stratégie DLP, si vous ne spécifiez aucun niveau de confiance pour la règle à utiliser, cette règle correspondra en fonction du niveau de confiance recommandé pour l’entité.
  
## <a name="do-you-want-to-support-other-languages-in-the-ui-of-the-security-amp-compliance-center-localizedstrings-element"></a>Voulez-vous prendre en charge d’autres langues dans l’interface utilisateur du Centre de sécurité &amp; conformité ? [élément LocalizedStrings]

Si votre équipe de conformité utilise le Centre de sécurité &amp; conformité Office 365 pour créer des stratégies DLP avec différents paramètres régionaux et dans différentes langues, vous pouvez fournir des versions localisées du nom et de la description de votre type d’informations sensibles personnalisé. Lorsque votre équipe de conformité utilise Office 365 dans une langue prise en charge, le nom localisé s’affiche dans l’interface utilisateur.
  
![Nombre d’instances et options de précision de correspondance](media/11d0b51e-7c3f-4cc6-96d8-b29bcdae1aeb.png)
  
L’élément Rules doit contenir un élément LocalizedStrings, qui contient un élément Resource référençant le GUID de votre entité personnalisée. À son tour, chaque élément Resource contient un ou plusieurs éléments Name et Description qui utilisent l’attribut langcode afin de fournir une chaîne localisée pour une langue spécifique.
  
![Balisage XML montrant le contenu de l’élément LocalizedStrings](media/a96fc34a-b93d-498f-8b92-285b16a7bbe6.png)
  
Notez que vous utilisez des chaînes localisées uniquement pour la manière dont le type d’informations sensibles personnalisé apparaît dans l’interface utilisateur du Centre de sécurité &amp; conformité. Vous ne pouvez pas utiliser des chaînes localisées pour fournir différentes versions localisées d’une liste de mots clés ou une expression régulière.
  
## <a name="other-rule-package-markup-rulepack-guid"></a>Autre balisage de package de règles [GUID RulePack]

Enfin, le début de chaque RulePackage contient des informations générales que vous avez besoin de compléter. Vous pouvez utiliser le balisage suivant comme modèle et remplacer les espaces réservés « ... » avec vos propres informations.
  
Vous devez surtout générer un GUID pour le RulePack. Ci-dessus, vous avez généré un GUID pour l’entité ; il s’agit d’un second GUID pour le RulePack. Il existe plusieurs méthodes pour générer des GUID, mais vous pouvez le faire facilement dans PowerShell en saisissant [guid]::NewGuid().
  
L’élément Version est également important. Lorsque vous chargez votre package de règles pour la première fois, Office 365 prend note du numéro de version. Si vous mettez à jour le package de règles ultérieurement et téléchargez une nouvelle version, veillez à mettre à jour le numéro de version, sinon Office 365 ne déploiera pas le package de règles.
  
```
<?xml version="1.0" encoding="utf-16"?>
<RulePackage xmlns="http://schemas.microsoft.com/office/2011/mce">
  <RulePack id=". . .">
    <Version major="1" minor="0" build="0" revision="0" />
    <Publisher id=". . ." /> 
    <Details defaultLangCode=". . .">
      <LocalizedDetails langcode=" . . . ">
         <PublisherName>. . .</PublisherName>
         <Name>. . .</Name>
         <Description>. . .</Description>
      </LocalizedDetails>
    </Details>
  </RulePack>
  
 <Rules>
    . . .
 </Rules>
</RulePackage>

```

Lorsque vous avez terminé, votre élément RulePack doit ressembler à ce qui suit :
  
![Balisage XML montrant l’élément RulePack](media/fd0f31a7-c3ee-43cd-a71b-6a3813b21155.png)
  
## <a name="changes-for-exchange-online"></a>Modifications pour Exchange Online

Auparavant, vous utilisiez peut-être Exchange Online PowerShell pour importer vos types d’informations sensibles personnalisés pour DLP. Désormais, vos types d’informations sensibles personnalisés peuvent être utilisés dans le Centre d’administration Exchange et le Centre de sécurité et de conformité. Dans le cadre de cette amélioration, vous devez utiliser le Centre de sécurité et de conformité PowerShell pour importer vos types d’informations sensibles personnalisés (vous ne pouvez plus les importer à partir d’Exchange PowerShell). Vos types d’informations sensibles personnalisés continueront de fonctionner comme avant. Cependant, l’affichage des modifications apportées aux types d’informations sensibles personnalisés dans le Centre de sécurité et de conformité dans le Centre d’administration Exchange peut prendre jusqu’à une heure.
  
Dans le Centre de sécurité et de conformité, vous pouvez utiliser la cmdlet `DlpSensitiveInformationTypeRulePackage` pour charger un package de règles. Auparavant, dans le Centre d’administration Exchange, vous utilisiez la cmdlet `ClassificationRuleCollection`. 
  
## <a name="upload-your-rule-package"></a>Télécharger votre package de règles

Pour télécharger votre package de règles, procédez comme suit :
  
1. Enregistrez-le en tant que fichier .xml avec le codage Unicode.
    
2. [Connexion au Centre de Conformité et Sécurité Office 365 PowerShell ](http://go.microsoft.com/fwlink/p/?LinkID=799771)
    
3. Utilisez la syntaxe suivante :

    ```
    New-DlpSensitiveInformationTypeRulePackage -FileData (Get-Content -Path "PathToUnicodeXMLFile" -Encoding Byte)
    ```

    Cet exemple télécharge le fichier XML Unicode nommé MyNewRulePack.xml à partir de C:\My Documents.

    ```
    New-DlpSensitiveInformationTypeRulePackage -FileData (Get-Content -Path "C:\My Documents\MyNewRulePack.xml" -Encoding Byte)
    ```

    Pour une syntaxe détaillée et des informations de paramètrage, voir [New-DlpSensitiveInformationTypeRulePackage](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/new-dlpsensitiveinformationtyperulepackage).

5. Pour vérifier que vous avez correctement créé un nouveau type d’informations sensibles, effectuez l’une des opérations suivantes :

  - Exécutez la commande suivante et vérifiez que le package de règles est répertorié:

    ```
    Get-DlpSensitiveInformationTypeRulePackage
    ``` 

  - Exécutez la commande suivante et vérifiez que le package d’informations est répertorié:

    ```
    Get-DlpSensitiveInformationType
    ``` 

    Pour les types d’informations sensibles personnalisés, la valeur de propriété Publisher sera un numéro autre que Microsoft Corporation.

  - Remplacez\<Nom\> avec la valeur Nom du type d’informations sensibles (par exemple, ID d’employé) et exécutez la commande suivante :

    ```
    Get-DlpSensitiveInformationType -Identity "<Name>"
    ```
    
## <a name="potential-validation-issues-to-be-aware-of"></a>Problèmes de validation éventuels à prendre en compte

Lorsque vous chargez votre fichier XML de package de règles, le système valide le fichier XML et recherche des modèles incorrects connus et des problèmes de performance évidents. Voici quelques-uns des problèmes connus que la validation contrôle. Une expression régulière :
  
- ne peut pas commencer ou se terminer par l’alternateur « | », qui correspond à tous les éléments, car il est considéré comme une correspondance vide ;
    
    Par exemple, « |a » ou « b| » échoue à la validation.
    
- ne peut pas commencer ou se terminer par un modèle « .{0,m} » qui n’a aucune fonction et nuit uniquement aux performances ;
    
    Par exemple, « .{0,50}ASDF » ou « ASDF.{0,50} » échoue à la validation.
    
- ne peut pas contenir « .{0,m} » ou « .{1,m} » dans des groupes, et ne peut pas contenir « .\* » ou « .+ » dans des groupes ;
    
    Par exemple, « (.{0,50000}) » échoue à la validation.
    
- ne peut pas contenir de caractère avec les répéteurs « {0,m} » ou « {1, m} » dans des groupes ;
    
    Par exemple, « (a\*) » échoue à la validation.
    
- ne peut pas commencer ou se terminer par « .{1,m} » ; utilisez simplement « . » ;
    
    Par exemple, « .{1,m}asdf » échoue à la validation ; utilisez simplement « .asdf ».
    
- ne peut pas contenir de répéteur illimité (tel que « \* » ou « + ») dans un groupe.
    
    Par exemple, « (xx)\* » et « (xx)+ » échouent à la validation.
    
Si un type d’informations sensibles personnalisé contient un problème qui peut affecter les performances, il n’est pas chargé et l’un des messages d’erreur suivants s’affichent :
  
- **Quantificateurs génériques correspondant à plus de contenu que prévu (par exemple, « + » et « \* »)**
    
- **Assertions d’inspection**
    
- **Regroupement complexe conjointement avec des quantificateurs généraux**
    
## <a name="recrawl-your-content-to-identify-the-sensitive-information"></a>Analyser de nouveau le contenu pour identifier les informations sensibles

DLP utilise le robot de recherche pour identifier et classer les informations sensibles du contenu de site. Le contenu des sites SharePoint Online et OneDrive Entreprise est analysé automatiquement à chaque fois que celui-ci est mis à jour. Cependant, pour identifier votre nouveau type d’informations sensibles personnalisé dans l’ensemble du contenu existant, ce contenu doit être à nouveau analysé.
  
Dans Office 365, vous ne pouvez pas demander manuellement une nouvelle analyse de l’ensemble d’un client, mais vous pouvez le faire pour une collection de sites, une liste ou une bibliothèque (consultez l’article [Demander manuellement l’analyse et la réindexation d’un site, d’une bibliothèque ou d’une liste](https://support.office.com/article/9afa977d-39de-4321-b4ca-8c7c7e6d264e)).
  
## <a name="remove-a-custom-sensitive-information-type"></a>Supprimer un type d’informations sensibles personnalisé

**Remarque**: avant de supprimer un type d’informations sensibles personnalisé, vérifiez qu’aucune stratégie DLP ou règles de flux de courrier Exchange (également appelées règles de transport) ne référence toujours le type d’informations sensibles.

Dans le Centre de Conformité et de sécurité PowerShell, il existe deux méthodes pour supprimer des types d’informations sensibles personnalisés :

- **Supprimer des types d’informations sensibles personnalisés individuels**: utiliser la méthode décrite dans [Modifier un type d’informations sensibles personnalisé](#modify-a-custom-sensitive-information-type). Vous exportez le package de règles personnalisé qui contient le type d’informations sensibles personnalisé, supprimez le type d’informations sensibles du fichier XML et importerez le fichier XML mis à jour dans le package de règles personnalisé existant.

- **Supprimer un package de règles personnalisé et tous les types d’informations sensibles personnalisés qu’il contient**: cette méthode est présentée dans cette section.

1. [Connexion au Centre de Conformité et Sécurité Office 365 PowerShell ](http://go.microsoft.com/fwlink/p/?LinkID=799771)

2. Pour supprimer un package de règles personnalisé, utilisez la syntaxe suivante :

    ```
    Remove-DlpSensitiveInformationTypeRulePackage -Identity "RulePackageIdentity"
    ```

    Vous pouvez utiliser la valeur Nom (pour n’importe quelle langue) ou la`RulePack id` valeur (GUID) pour identifier le package de règles.

    Cet exemple supprime le package de règles nommé « Package règle personnalisé employé ID ».

    ```
       Remove-DlpSensitiveInformationTypeRulePackage -Identity "Employee ID Custom Rule Pack"
    ```

    Pour une syntaxe détaillée et des informations de paramétrage, voir [Remove-DlpSensitiveInformationTypeRulePackage](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/remove-dlpsensitiveinformationtyperulepackage).

3. Afin de vérifier que vous avez correctement retiré un nouveau type d’informations sensibles, effectuez l’une des opérations suivantes :

  - Exécutez la commande suivante et vérifiez que le package de règles n’est plus répertorié:

    ```
    Get-DlpSensitiveInformationTypeRulePackage
    ``` 

  - Exécutez la commande suivante et vérifiez que les types d’informations sensibles dans le package de règles supprimés n’est plus répertorié :

    ```
    Get-DlpSensitiveInformationType
    ``` 

    Pour les types d’informations sensibles personnalisés, la valeur de propriété Publisher sera un numéro autre que Microsoft Corporation.

  - Remplacez\<Nom\> avec la valeur Nom du type d’informations sensibles (par exemple, ID d’employé) et exécutez la commande suivante afin de vérifier que le type d’informations sensible n’est plus répertorié:

    ```
    Get-DlpSensitiveInformationType -Identity "<Name>"
    ```

## <a name="modify-a-custom-sensitive-information-type"></a>Modifier un type d’informations sensibles personnalisé

Dans le Centre de Conformité et sécurité PowerShell ,modifier un type d’informations sensibles personnalisé vous oblige à:

1. Exportez le package de règles existant qui contient le type d’informations sensibles personnalisé dans un fichier XML (ou utilisez le fichier XML existant si vous avez un). 

2. Modifier le type d’informations sensibles personnalisé dans un fichier exporté XML.

3. Importer le fichier XML mis à jour vers le package de règles existant.

Afin de vous connecter au Centre  de Conformité et de Sécurité PowerShell, voir[Se connecter au Centre de Conformité et de Sécurité Office 365 PowerShell](http://go.microsoft.com/fwlink/p/?LinkID=799771).

#### <a name="step-1-export-the-existing-rule-package-to-an-xml-file"></a>Étape 1 : Exporter le package de règles existant vers un fichier XML

**Remarque**: Si vous avez une copie du fichier XML (par exemple, vous venez de créer et d’importer), vous pouvez passer directement à l’étape suivante pour modifier le fichier XML.

1. Si vous ne le connaissez pas encore, exécutez la commande suivante pour trouver le nom du package de règles personnalisé :

    ```
    Get-DlpSensitiveInformationTypeRulePackage
    ```

    **Remarque**: le package de règles intégré qui contient les types d’informations sensibles intégrés est nommé Package de règles Microsoft. Le package de règles qui contient les types d’informations sensibles personnalisés que vous avez créés dans le Centre de Conformité de sécurité de l’interface utilisateur et est nommé Microsoft.SCCManaged.CustomRulePack.

2. Utilisez la syntaxe suivante afin de stocker le package de règles personnalisé vers une variable :

    ```
    $rulepak = Get-DlpSensitiveInformationTypeRulePackage -Identity "RulePackageName"
    ```

   Par exemple, si le nom du package de règles est « Pack règle personnalisée employé ID », exécutez la commande suivante :

    ```
    $rulepak = Get-DlpSensitiveInformationTypeRulePackage -Identity "Employee ID Custom Rule Pack"
    ```

3. Utilisez la syntaxe suivante afin d’exporter le package de règles personnalisé vers un fichier XML:

    ```
    Set-Content -Path "XMLFileAndPath" -Encoding Byte -Value $rulepak.SerializedClassificationRuleCollection
    ```

    Cet exemple exporte le package de règles dans le fichier nommé ExportedRulePackage.xml dans le dossier Documents C:\My Documents folder.

    ```
    Set-Content -Path "C:\My Documents\ExportedRulePackage.xml" -Encoding Byte -Value $rulepak.SerializedClassificationRuleCollection
    ```

#### <a name="step-2-modify-the-sensitive-information-type-in-the-exported-xml-file"></a>Étape 2: Modifier le type d’informations sensibles personnalisé dans un fichier exporté XML.

Les types d’informations sensibles dans le fichier XML et d’autres éléments dans le fichier sont décrits précédemment dans cette rubrique.

#### <a name="step-3-import-the-updated-xml-file-back-into-the-existing-rule-package"></a>Étape 3: Importer de nouveau le fichier XML mis à jour vers le package de règles existant.

Afin d’importer de nouveau le fichier XML mis à jour vers le package de règles existant, utilisez la syntaxe suivante:

```
Set-DlpSensitiveInformationTypeRulePackage -Identity "RulePackageIdentity" -FileData (Get-Content -Path "PathToUnicodeXMLFile" -Encoding Byte)
```

Vous pouvez utiliser la valeur Nom ou la`RulePack id` valeur (GUID) afin d’identifier le package de règles.

Cet exemple télécharge le fichier XML Unicode mis à jour nommé MyUpdatedRulePack.xml à partir de C:\My Documents dans le package de règles existant nommé « Package règle personnalisé employé ID ».

```
Set-DlpSensitiveInformationTypeRulePackage -Identity "Employee ID Custom Rule Pack" -FileData (Get-Content -Path "C:\My Documents\MyUpdatedRulePack.xml" -Encoding Byte)
```

Pour une syntaxe détaillée et des informations de paramétrage, voir [Set-DlpSensitiveInformationTypeRulePackage](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/set-dlpsensitiveinformationtyperulepackage).

## <a name="reference-rule-package-xml-schema-definition"></a>Référence : Définition du schéma XML du package de règles

Vous pouvez copier ce balisage, l’enregistrer sous la forme d’un fichier XSD et l’utiliser pour valider le fichier XML de votre package de règles.
  
```
<?xml version="1.0" encoding="utf-8"?>
<xs:schema xmlns:mce="http://schemas.microsoft.com/office/2011/mce"
           targetNamespace="http://schemas.microsoft.com/office/2011/mce" 
           xmlns:xs="http://www.w3.org/2001/XMLSchema"
           elementFormDefault="qualified"
           attributeFormDefault="unqualified"
           id="RulePackageSchema">
  <!-- Use include if this schema has the same target namespace as the schema being referenced, otherwise use import -->
  <xs:element name="RulePackage" type="mce:RulePackageType"/>
  <xs:simpleType name="LangType">
    <xs:union memberTypes="xs:language">
      <xs:simpleType>
        <xs:restriction base="xs:string">
          <xs:enumeration value=""/>
        </xs:restriction>
      </xs:simpleType>
    </xs:union>
  </xs:simpleType>
  <xs:simpleType name="GuidType" final="#all">
    <xs:restriction base="xs:token">
      <xs:pattern value="[0-9a-fA-F]{8}\-([0-9a-fA-F]{4}\-){3}[0-9a-fA-F]{12}"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:complexType name="RulePackageType">
    <xs:sequence>
      <xs:element name="RulePack" type="mce:RulePackType"/>
      <xs:element name="Rules" type="mce:RulesType">
        <xs:key name="UniqueRuleId">
          <xs:selector xpath="mce:Entity|mce:Affinity|mce:Version/mce:Entity|mce:Version/mce:Affinity"/>
          <xs:field xpath="@id"/>
        </xs:key>
        <xs:key name="UniqueProcessorId">
          <xs:selector xpath="mce:Regex|mce:Keyword|mce:Fingerprint"></xs:selector>
          <xs:field xpath="@id"/>
        </xs:key>
        <xs:key name="UniqueResourceIdRef">
          <xs:selector xpath="mce:LocalizedStrings/mce:Resource"/>
          <xs:field xpath="@idRef"/>
        </xs:key>        
        <xs:keyref name="ReferencedRuleMustExist" refer="mce:UniqueRuleId">
          <xs:selector xpath="mce:LocalizedStrings/mce:Resource"/>
          <xs:field xpath="@idRef"/>
        </xs:keyref>
        <xs:keyref name="RuleMustHaveResource" refer="mce:UniqueResourceIdRef">
          <xs:selector xpath="mce:Entity|mce:Affinity|mce:Version/mce:Entity|mce:Version/mce:Affinity"/>
          <xs:field xpath="@id"/>
        </xs:keyref>
      </xs:element>
    </xs:sequence>
  </xs:complexType>
  <xs:complexType name="RulePackType">
    <xs:sequence>
      <xs:element name="Version" type="mce:VersionType"/>
      <xs:element name="Publisher" type="mce:PublisherType"/>
      <xs:element name="Details" type="mce:DetailsType">
        <xs:key name="UniqueLangCodeInLocalizedDetails">
          <xs:selector xpath="mce:LocalizedDetails"/>
          <xs:field xpath="@langcode"/>
        </xs:key>
        <xs:keyref name="DefaultLangCodeMustExist" refer="mce:UniqueLangCodeInLocalizedDetails">
          <xs:selector xpath="."/>
          <xs:field xpath="@defaultLangCode"/>
        </xs:keyref>
      </xs:element>
      <xs:element name="Encryption" type="mce:EncryptionType" minOccurs="0" maxOccurs="1"/>
    </xs:sequence>
    <xs:attribute name="id" type="mce:GuidType" use="required"/>
  </xs:complexType>
  <xs:complexType name="VersionType">
    <xs:attribute name="major" type="xs:unsignedShort" use="required"/>
    <xs:attribute name="minor" type="xs:unsignedShort" use="required"/>
    <xs:attribute name="build" type="xs:unsignedShort" use="required"/>
    <xs:attribute name="revision" type="xs:unsignedShort" use="required"/>
  </xs:complexType>
  <xs:complexType name="PublisherType">
    <xs:attribute name="id" type="mce:GuidType" use="required"/>
  </xs:complexType>
  <xs:complexType name="LocalizedDetailsType">
    <xs:sequence>
      <xs:element name="PublisherName" type="mce:NameType"/>
      <xs:element name="Name" type="mce:RulePackNameType"/>
      <xs:element name="Description" type="mce:OptionalNameType"/>
    </xs:sequence>
    <xs:attribute name="langcode" type="mce:LangType" use="required"/>
  </xs:complexType>
  <xs:complexType name="DetailsType">
    <xs:sequence>
      <xs:element name="LocalizedDetails" type="mce:LocalizedDetailsType" maxOccurs="unbounded"/>
    </xs:sequence>
    <xs:attribute name="defaultLangCode" type="mce:LangType" use="required"/>
  </xs:complexType>
  <xs:complexType name="EncryptionType">
    <xs:sequence>
      <xs:element name="Key" type="xs:normalizedString"/>
      <xs:element name="IV" type="xs:normalizedString"/>
    </xs:sequence>
  </xs:complexType>
  <xs:simpleType name="RulePackNameType">
    <xs:restriction base="xs:token">
      <xs:minLength value="1"/>
      <xs:maxLength value="64"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:simpleType name="NameType">
    <xs:restriction base="xs:normalizedString">
      <xs:minLength value="1"/>
      <xs:maxLength value="256"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:simpleType name="OptionalNameType">
    <xs:restriction base="xs:normalizedString">
      <xs:minLength value="0"/>
      <xs:maxLength value="256"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:simpleType name="RestrictedTermType">
    <xs:restriction base="xs:string">
      <xs:minLength value="1"/>
      <xs:maxLength value="100"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:complexType name="RulesType">
    <xs:sequence>
      <xs:choice maxOccurs="unbounded">
        <xs:element name="Entity" type="mce:EntityType"/>
        <xs:element name="Affinity" type="mce:AffinityType"/>
        <xs:element name="Version" type="mce:VersionedRuleType"/>
      </xs:choice>
      <xs:choice minOccurs="0" maxOccurs="unbounded">
        <xs:element name="Regex" type="mce:RegexType"/>
        <xs:element name="Keyword" type="mce:KeywordType"/>
        <xs:element name="Fingerprint" type="mce:FingerprintType"/>
        <xs:element name="ExtendedKeyword" type="mce:ExtendedKeywordType"/>
      </xs:choice>
      <xs:element name="LocalizedStrings" type="mce:LocalizedStringsType"/>
    </xs:sequence>
  </xs:complexType>
  <xs:complexType name="EntityType">
    <xs:sequence>
      <xs:element name="Pattern" type="mce:PatternType" maxOccurs="unbounded"/>
      <xs:element name="Version" type="mce:VersionedPatternType" minOccurs="0" maxOccurs="unbounded" />
    </xs:sequence>
    <xs:attribute name="id" type="mce:GuidType" use="required"/>
    <xs:attribute name="patternsProximity" type="mce:ProximityType" use="required"/>
    <xs:attribute name="recommendedConfidence" type="mce:ProbabilityType"/>
    <xs:attribute name="workload" type="mce:WorkloadType"/>
  </xs:complexType>
  <xs:complexType name="PatternType">
    <xs:sequence>
      <xs:element name="IdMatch" type="mce:IdMatchType"/>
      <xs:choice minOccurs="0" maxOccurs="unbounded">
        <xs:element name="Match" type="mce:MatchType"/>
        <xs:element name="Any" type="mce:AnyType"/>
      </xs:choice>
    </xs:sequence>
    <xs:attribute name="confidenceLevel" type="mce:ProbabilityType" use="required"/>
  </xs:complexType>
  <xs:complexType name="AffinityType">
    <xs:sequence>
      <xs:element name="Evidence" type="mce:EvidenceType" maxOccurs="unbounded"/>
      <xs:element name="Version" type="mce:VersionedEvidenceType" minOccurs="0" maxOccurs="unbounded" />
    </xs:sequence>
    <xs:attribute name="id" type="mce:GuidType" use="required"/>
    <xs:attribute name="evidencesProximity" type="mce:ProximityType" use="required"/>
    <xs:attribute name="thresholdConfidenceLevel" type="mce:ProbabilityType" use="required"/>
    <xs:attribute name="workload" type="mce:WorkloadType"/>
  </xs:complexType>
  <xs:complexType name="EvidenceType">
    <xs:sequence>
      <xs:choice maxOccurs="unbounded">
        <xs:element name="Match" type="mce:MatchType"/>
        <xs:element name="Any" type="mce:AnyType"/>
      </xs:choice>
    </xs:sequence>
    <xs:attribute name="confidenceLevel" type="mce:ProbabilityType" use="required"/>
  </xs:complexType>
  <xs:complexType name="IdMatchType">
    <xs:attribute name="idRef" type="xs:string" use="required"/>
  </xs:complexType>
  <xs:complexType name="MatchType">
    <xs:attribute name="idRef" type="xs:string" use="required"/>
    <xs:attribute name="minCount" type="xs:positiveInteger" use="optional"/>
    <xs:attribute name="uniqueResults" type="xs:boolean" use="optional"/>
  </xs:complexType>
  <xs:complexType name="AnyType">
    <xs:sequence>
      <xs:choice maxOccurs="unbounded">
        <xs:element name="Match" type="mce:MatchType"/>
        <xs:element name="Any" type="mce:AnyType"/>
      </xs:choice>
    </xs:sequence>
    <xs:attribute name="minMatches" type="xs:nonNegativeInteger" default="1"/>
    <xs:attribute name="maxMatches" type="xs:nonNegativeInteger" use="optional"/>
  </xs:complexType>
  <xs:simpleType name="ProximityType">
    <xs:union>
      <xs:simpleType>
        <xs:restriction base='xs:string'>
          <xs:enumeration value="unlimited"/>
        </xs:restriction>
      </xs:simpleType>
      <xs:simpleType>
        <xs:restriction base="xs:positiveInteger">
          <xs:minInclusive value="1"/>
        </xs:restriction>
      </xs:simpleType>
    </xs:union>
  </xs:simpleType>
  <xs:simpleType name="ProbabilityType">
    <xs:restriction base="xs:integer">
      <xs:minInclusive value="1"/>
      <xs:maxInclusive value="100"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:simpleType name="WorkloadType">
    <xs:restriction base="xs:string">
      <xs:enumeration value="Exchange"/>
      <xs:enumeration value="Outlook"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:simpleType name="EngineVersionType">
    <xs:restriction base="xs:token">
      <xs:pattern value="^\d{2}\.01?\.\d{3,4}\.\d{1,3}$"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:complexType name="VersionedRuleType">
    <xs:choice maxOccurs="unbounded">
      <xs:element name="Entity" type="mce:EntityType"/>
      <xs:element name="Affinity" type="mce:AffinityType"/>
    </xs:choice>
    <xs:attribute name="minEngineVersion" type="mce:EngineVersionType" use="required" />
  </xs:complexType>
  <xs:complexType name="VersionedPatternType">
    <xs:sequence>
      <xs:element name="Pattern" type="mce:PatternType" maxOccurs="unbounded"/>
    </xs:sequence>
    <xs:attribute name="minEngineVersion" type="mce:EngineVersionType" use="required" />
  </xs:complexType>
  <xs:complexType name="VersionedEvidenceType">
    <xs:sequence>
      <xs:element name="Evidence" type="mce:EvidenceType" maxOccurs="unbounded"/>
    </xs:sequence>
    <xs:attribute name="minEngineVersion" type="mce:EngineVersionType" use="required" />
  </xs:complexType>
  <xs:simpleType name="FingerprintValueType">
    <xs:restriction base="xs:string">
      <xs:minLength value="2732"/>
      <xs:maxLength value="2732"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:complexType name="FingerprintType">
    <xs:simpleContent>
      <xs:extension base="mce:FingerprintValueType">
        <xs:attribute name="id" type="xs:token" use="required"/>
        <xs:attribute name="threshold" type="mce:ProbabilityType" use="required"/>
        <xs:attribute name="shingleCount" type="xs:positiveInteger" use="required"/>
        <xs:attribute name="description" type="xs:string" use="optional"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>
  <xs:complexType name="RegexType">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="id" type="xs:token" use="required"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>
  <xs:complexType name="KeywordType">
    <xs:sequence>
      <xs:element name="Group" type="mce:GroupType" maxOccurs="unbounded"/>
    </xs:sequence>
    <xs:attribute name="id" type="xs:token" use="required"/>
  </xs:complexType>
  <xs:complexType name="GroupType">
    <xs:sequence>
      <xs:choice>
        <xs:element name="Term" type="mce:TermType" maxOccurs="unbounded"/>
      </xs:choice>
    </xs:sequence>
    <xs:attribute name="matchStyle" default="word">
      <xs:simpleType>
        <xs:restriction base="xs:NMTOKEN">
          <xs:enumeration value="word"/>
          <xs:enumeration value="string"/>
        </xs:restriction>
      </xs:simpleType>
    </xs:attribute>
  </xs:complexType>
  <xs:complexType name="TermType">
    <xs:simpleContent>
      <xs:extension base="mce:RestrictedTermType">
        <xs:attribute name="caseSensitive" type="xs:boolean" default="false"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>
  <xs:complexType name="ExtendedKeywordType">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="id" type="xs:token" use="required"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>
  <xs:complexType name="LocalizedStringsType">
    <xs:sequence>
      <xs:element name="Resource" type="mce:ResourceType" maxOccurs="unbounded">
      <xs:key name="UniqueLangCodeUsedInNamePerResource">
        <xs:selector xpath="mce:Name"/>
        <xs:field xpath="@langcode"/>
      </xs:key>
      <xs:key name="UniqueLangCodeUsedInDescriptionPerResource">
        <xs:selector xpath="mce:Description"/>
        <xs:field xpath="@langcode"/>
      </xs:key>
    </xs:element>
    </xs:sequence>
  </xs:complexType>
  <xs:complexType name="ResourceType">
    <xs:sequence>
      <xs:element name="Name" type="mce:ResourceNameType" maxOccurs="unbounded"/>
      <xs:element name="Description" type="mce:DescriptionType" minOccurs="0" maxOccurs="unbounded"/>
    </xs:sequence>
    <xs:attribute name="idRef" type="mce:GuidType" use="required"/>
  </xs:complexType>
  <xs:complexType name="ResourceNameType">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="default" type="xs:boolean" default="false"/>
        <xs:attribute name="langcode" type="mce:LangType" use="required"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>
  <xs:complexType name="DescriptionType">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="default" type="xs:boolean" default="false"/>
        <xs:attribute name="langcode" type="mce:LangType" use="required"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>
</xs:schema>

```

## <a name="more-information"></a>Plus d’informations

- [Vue d’ensemble des stratégies de protection contre la perte de données](data-loss-prevention-policies.md)
    
- [Éléments recherchés par les types d’informations sensibles](what-the-sensitive-information-types-look-for.md)
    
- [Éléments recherchés par les fonctions DLP](what-the-dlp-functions-look-for.md)
    

