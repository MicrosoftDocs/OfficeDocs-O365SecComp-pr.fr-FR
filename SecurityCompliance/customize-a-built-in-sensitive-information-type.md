---
title: Personnaliser un type d’informations sensibles intégré
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/25/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Priority
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 2164ce3d-4d64-4283-b6b1-b81fbe835e8e
description: Lorsque vous recherchez des informations sensibles dans du contenu, vous devez décrire ces informations dans ce que l’on appelle une règle. La protection contre la perte de données (DLP) comprend des règles pour les types d’informations sensibles les plus courants que vous pouvez utiliser immédiatement. Pour utiliser ces règles, vous devez les inclure dans une stratégie. Vous voudrez peut-être ajuster ces règles intégrées pour répondre aux besoins spécifiques de votre organisation, et vous pouvez le faire en créant un type d’informations sensibles personnalisé. Cette rubrique vous montre comment personnaliser le fichier XML qui contient la collection de règles existante pour détecter un plus large éventail d’informations potentielles relatives aux cartes de crédit.
ms.openlocfilehash: 37731eff5af1d37da6e4aaf9fbb93159378e498c
ms.sourcegitcommit: ceb70ea863d8b97afea077a04fc7ec612b870695
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25857272"
---
# <a name="customize-a-built-in-sensitive-information-type"></a>Personnaliser un type d’informations sensibles intégré

Lorsque vous recherchez des informations sensibles dans du contenu, vous devez décrire ces informations dans ce que l’on appelle une *règle*. La protection contre la perte de données (DLP) comprend des règles pour les types d’informations sensibles les plus courants que vous pouvez utiliser immédiatement. Pour utiliser ces règles, vous devez les inclure dans une stratégie. Vous voudrez peut-être ajuster ces règles intégrées pour répondre aux besoins spécifiques de votre organisation, et vous pouvez le faire en créant un type d’informations sensibles personnalisé. Cette rubrique vous montre comment personnaliser le fichier XML qui contient la collection de règles existante pour détecter un plus large éventail d’informations potentielles relatives aux cartes de crédit. 
  
Vous pouvez prendre cet exemple et l’appliquer à d’autres types d’informations sensibles intégrés. Pour obtenir la liste des types d’informations sensibles par défaut et des définitions XML, consultez l’article [Éléments recherchés par les types d’informations sensibles](what-the-sensitive-information-types-look-for.md). 
  
## <a name="export-the-xml-file-of-the-current-rules"></a>Exporter le fichier XML des règles actuelles

Pour exporter le fichier XML, vous devez vous [connecter au Centre de sécurité et conformité à l’aide de PowerShell à distance](https://go.microsoft.com/fwlink/?linkid=799771).
  
1. Dans PowerShell, saisissez la commande suivante pour afficher les règles de votre organisation à l’écran. Si vous n’avez pas créé votre propre règle, vous ne verrez que les règles intégrées par défaut, sous le libellé « Package de règles Microsoft ».
    
     `Get-DlpSensitiveInformationTypeRulePackage`
    
2. Stockez les règles de votre organisation dans une variable en saisissant ce qui suit. Le stockage d’un élément dans une variable le rend facilement disponible ultérieurement dans un format adapté aux commandes PowerShell distantes.
    
     `$ruleCollections = Get-DlpSensitiveInformationTypeRulePackage`
    
3. Saisissez ce qui suit pour créer un fichier XML mis en forme avec toutes ces données (`Set-content` est la partie de la cmdlet qui écrit le code XML dans le fichier). 
    
     `Set-Content -path "C:\custompath\exportedRules.xml" -Encoding Byte -Value $ruleCollections.SerializedClassificationRuleCollection`
    
    > [!IMPORTANT]
    > Assurez-vous que vous utilisez l’emplacement de fichier dans lequel votre pack de règles est effectivement stocké. `C:\custompath\` est un espace réservé. 
  
## <a name="find-the-rule-that-you-want-to-modify-in-the-xml"></a>Rechercher la règle à modifier dans le fichier XML

Les cmdlets ci-dessus ont exporté l’ensemble de la *collection de règles*, ce qui inclut les règles par défaut que nous fournissons. Ensuite, vous devez rechercher la règle de numéro de carte de crédit spécifique à modifier. 
  
1. Utilisez un éditeur de texte pour ouvrir le fichier XML que vous avez exporté dans la section précédente.
    
2. Faites défiler l’écran jusqu’à la balise `<Rules>`, qui constitue le début de la section qui contient les règles DLP (étant donné que ce fichier XML contient les informations de toute la collection de règles, il contient d’autres informations dans la partie supérieure que vous devez faire défiler pour parvenir aux règles). 
    
3. Recherchez *Func_credit_card* pour trouver la définition de règle de numéro de carte de crédit. (Dans le langage XML, les noms des règles ne peuvent pas contenir d’espaces. Ces derniers sont donc généralement remplacés par des traits de soulignement, et les noms des règles sont parfois abrégés. Par exemple, la règle de numéro de sécurité sociale des États-Unis est abrégée par « SSN ». Le XML de la règle de numéro de carte de crédit doit ressembler à l’exemple de code suivant. 
    
  ```
  <Entity id="50842eb7-edc8-4019-85dd-5a5c1f2bb085"
         patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
         <IdMatch idRef="Func_credit_card" />
          <Any minMatches="1">
            <Match idRef="Keyword_cc_verification" />
            <Match idRef="Keyword_cc_name" />
            <Match idRef="Func_expiration_date" />
          </Any>
        </Pattern>
      </Entity>
  ```

Maintenant que vous avez localisé la définition de règle de numéro de carte de crédit dans le XML, vous pouvez personnaliser le XML de la règle pour répondre à vos besoins. (Pour un rappel sur les définitions XML, voir [Glossaire terminologique](#term-glossary) à la fin de cette rubrique.) 
  
## <a name="modify-the-xml-and-create-a-new-sensitive-information-type"></a>Modifier le XML et créer un type d’informations sensibles

Tout d’abord, vous devez créer un type d’informations sensibles, car vous ne pouvez pas modifier directement les règles par défaut. Vous pouvez effectuer de nombreuses actions avec les types d’informations sensibles personnalisés, comme l’illustre la section [Créer un type d’informations sensibles personnalisé dans le Centre de Conformité et Sécurité Office 365 PowerShell](create-a-custom-sensitive-information-type-in-scc-powershell.md). Pour cet exemple, nous allons rester simples et nous contenter de supprimer les preuves crédibles et d’ajouter des mots clés à la règle de numéro de carte de crédit.
  
Toutes les définitions de règle XML sont construites sur le modèle général suivant. Vous devez copier et coller le XML de définition de numéro de carte de crédit dans le modèle, modifier certaines valeurs (remarquez les espaces réservés « . . ." dans l'exemple suivant), puis télécharger le XML modifié en tant que nouvelle règle pouvant être utilisée dans des stratégies.
  
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
   <!-- Paste the Credit Card Number rule definition here.--> 
      <LocalizedStrings>
         <Resource idRef=". . .">
           <Name default="true" langcode=" . . . ">. . .</Name>
           <Description default="true" langcode=". . ."> . . .</Description>
         </Resource>
      </LocalizedStrings>
   </Rules>
</RulePackage>
```

Vous obtenez maintenant quelque chose qui ressemble au XML suivant. Étant donné que les packages de règles et les règles sont identifiés par leur GUID unique, vous devez générer deux GUID : un pour le package de règles et un pour remplacer le GUID de la règle de numéro de carte de crédit. (Le GUID pour l'ID d'entité dans l'exemple de code suivant est celui de la définition de notre règle intégrée, que vous devez remplacer.) Il existe plusieurs façons de générer des GUID, mais vous pouvez le faire facilement dans PowerShell en saisissant **[guid]::NewGuid()**. 
  
```
<?xml version="1.0" encoding="utf-16"?>
<RulePackage xmlns="http://schemas.microsoft.com/office/2011/mce">
  <RulePack id="8aac8390-e99f-4487-8d16-7f0cdee8defc">
    <Version major="1" minor="0" build="0" revision="0" />
    <Publisher id="8d34806e-cd65-4178-ba0e-5d7d712e5b66" />
    <Details defaultLangCode="en">
      <LocalizedDetails langcode="en">
        <PublisherName>Contoso Ltd.</PublisherName>
        <Name>Financial Information</Name>
        <Description>Modified versions of the Microsoft rule package</Description>
      </LocalizedDetails>
    </Details>
  </RulePack>
  
 <Rules>
    <Entity id="db80b3da-0056-436e-b0ca-1f4cf7080d1f"
       patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_credit_card" />
        <Any minMatches="1">
          <Match idRef="Keyword_cc_verification" />
          <Match idRef="Keyword_cc_name" />
          <Match idRef="Func_expiration_date" />
        </Any>
      </Pattern>
    </Entity>
      <LocalizedStrings>
         <Resource idRef="db80b3da-0056-436e-b0ca-1f4cf7080d1f"> 
<!-- This is the GUID for the preceding Credit Card Number entity because the following text is for that Entity. -->
           <Name default="true" langcode="en-us">Modified Credit Card Number</Name>
           <Description default="true" langcode="en-us">Credit Card Number that looks for additional keywords, and another version of Credit Card Number that doesn't require keywords (but has a lower confidence level)</Description>
         </Resource>
      </LocalizedStrings>
   </Rules>
</RulePackage>
```

## <a name="remove-the-corroborative-evidence-requirement-from-a-sensitive-information-type"></a>Supprimer l’exigence de preuve crédible d’un type d’informations sensibles

Maintenant que vous disposez d’un nouveau type d’informations sensibles que vous pouvez télécharger vers le Centre de sécurité &amp; conformité, la prochaine étape consiste à rendre la règle plus spécifique. Modifiez la règle de sorte qu’elle recherche uniquement un nombre à 16 chiffres qui passe la somme de contrôle, mais qu’elle ne nécessite pas de preuve (crédible) supplémentaire (par exemple, des mots clés). Pour ce faire, vous devez retirer la partie du XML qui recherche la preuve crédible. La preuve crédible est très utile pour réduire les faux positifs, car il existe généralement certains mots clés ou une date d’expiration près du numéro de carte de crédit. Si vous supprimez cette preuve, vous devez également ajuster votre probabilité de trouver un numéro de carte de crédit en abaissant le paramètre `confidenceLevel`, qui est défini sur 85 dans l’exemple.
  
```
<Entity id="db80b3da-0056-436e-b0ca-1f4cf7080d1f" patternsProximity="300"
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_credit_card" />
      </Pattern>
    </Entity>
```

## <a name="look-for-keywords-that-are-specific-to-your-organization"></a>Rechercher des mots clés propres à votre organisation

Vous voulez peut-être exiger des preuves crédibles, mais aussi des mots clés différents ou supplémentaires, et vous voulez aussi peut-être modifier l’endroit où rechercher ces preuves. Vous pouvez ajuster le paramètre `patternsProximity` afin de développer ou réduire la fenêtre pour la preuve probante autour du numéro à 16 chiffres. Pour ajouter vos propres mots clés, vous devez définir une liste de mots clés et la référencer dans votre règle. Le XML suivant ajoute les mots clés « company card » et « Contoso card » de sorte que tous les messages qui contiennent ces expressions au sein des 150 caractères d’un numéro de carte de crédit soient identifiés comme des numéros de carte de crédit. 
  
```
<Rules>
<! -- Modify the patternsProximity to be "150" rather than "300." -->
    <Entity id="db80b3da-0056-436e-b0ca-1f4cf7080d1f" patternsProximity="150" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_credit_card" />
        <Any minMatches="1">
          <Match idRef="Keyword_cc_verification" />
          <Match idRef="Keyword_cc_name" />
<!-- Add the following XML, which references the keywords at the end of the XML sample. -->
          <Match idRef="My_Additional_Keywords" />
          <Match idRef="Func_expiration_date" />
        </Any>
      </Pattern>
    </Entity>
<!-- Add the following XML, and update the information inside the <Term> tags with the keywords that you want to detect. -->
    <Keyword id="My_Additional_Keywords">
      <Group matchStyle="word">
        <Term caseSensitive="false">company card</Term>
        <Term caseSensitive="false">Contoso card</Term>
      </Group>
    </Keyword>
```

## <a name="upload-your-rule"></a>Télécharger votre règle

Pour télécharger votre règle, vous devez procéder comme suit.
  
1. Enregistrez-la en tant que fichier .xml avec le codage Unicode. Ceci est important car la règle ne fonctionne pas si le fichier est enregistré dans un codage différent.
    
2. [Se connecter au Centre de sécurité et conformité à l’aide de PowerShell à distance.](https://go.microsoft.com/fwlink/?linkid=799771)
    
3. Dans PowerShell, saisissez la commande suivante.
    
     `New-DlpSensitiveInformationTypeRulePackage -FileData (Get-Content -Path "C:\custompath\MyNewRulePack.xml" -Encoding Byte)`.
    
    > [!IMPORTANT]
    > Assurez-vous que vous utilisez l’emplacement de fichier dans lequel votre pack de règles est effectivement stocké. `C:\custompath\` est un espace réservé. 
  
4. Pour confirmer, saisissez Y, puis appuyez sur **Entrée**.
    
5. Vérifiez que votre nouvelle règle a été téléchargée en saisissant `Get-DlpSensitiveInformationType`, ce qui affiche désormais le nom de votre règle.
    
Pour commencer à utiliser la nouvelle règle afin de détecter des informations sensibles, vous devez l’ajouter à une stratégie DLP. Pour découvrir comment ajouter la règle à une stratégie, consultez l’article [Création d’une stratégie DLP à partir d’un modèle](create-a-dlp-policy-from-a-template.md).
  
## <a name="term-glossary"></a>Glossaire terminologique

Voici les définitions des termes que vous avez rencontrés au cours de cette procédure.
  
|**Terme**|**Définition**|
|:-----|:-----|
|Entité  <br/> |Les entités sont ce que nous appelons des types d'informations sensibles, comme les numéros de carte de crédit. Chaque entité possède un GUID unique qui constitue son ID. Si vous copiez un GUID et que vous le recherchez dans le XML, vous trouvez la définition de règle XML, ainsi que toutes les traductions localisées de cette règle XML. Vous pouvez également trouver cette définition en localisant le GUID de la traduction, puis en recherchant ce GUID.  <br/> |
|Fonctions  <br/> |Le fichier XML fait référence à `Func_credit_card`, qui est une fonction dans le code compilé. Les fonctions sont utilisées pour exécuter des expressions régulières complexes et vérifier que les sommes de contrôle correspondent pour nos règles intégrées. Étant donné que tout ceci se passe dans le code, certaines variables ne figurent pas dans le fichier XML.  <br/> |
|IdMatch  <br/> |Il s’agit de l’identificateur auquel le modèle tente de correspondre, par exemple un numéro de carte de crédit. Vous pouvez en lire plus à ce sujet et au sujet des balises `Match` dans [Règles d’entité](https://support.office.com/article/c4ab8707-0839-4855-9390-3dbcb43475a7.aspx#dlp-entity).  <br/> |
|Listes de mots clés  <br/> |Le fichier XML fait également référence à `keyword_cc_verification` et à `keyword_cc_name`, qui sont des listes de mots clés dans lesquelles nous recherchons des correspondances à l’intérieur du paramètre `patternsProximity` pour l’entité. Ces éléments ne sont actuellement pas affichés dans le fichier XML.  <br/> |
|Modèle  <br/> |Le modèle contient la liste de ce que le type sensible recherche. Cela inclut des mots clés, des expressions régulières et des fonctions internes (qui effectuent des tâches telles que la vérification des sommes de contrôle). Ces types d’informations sensibles peuvent avoir plusieurs modèles avec des niveaux de confiance uniques. Ceci est utile lors de la création d’un type d’informations sensibles qui renvoie un niveau de confiance élevé si des preuves crédibles sont trouvées et un niveau de confiance faible dans le cas contraire.  <br/> |
|confidenceLevel  <br/> |Il s'agit du niveau de confiance appliqué lorsque le moteur DLP trouve une correspondance. Ce niveau de confiance est associé à une correspondance pour le modèle si les exigences du modèle sont remplies. C'est la mesure de confiance à prendre en considération lorsque vous utilisez des règles de transport Exchange.  <br/> |
|patternsProximity  <br/> |Lorsque nous trouvons ce qui ressemble à un modèle de numéro de carte de crédit, `patternsProximity` correspond à la proximité de recherche de preuves crédibles autour de ce numéro.  <br/> |
|recommendedConfidence  <br/> |Il s’agit du niveau de confiance que nous recommandons pour cette règle. La confiance recommandée s’applique aux entités et aux affinités. Pour les entités, ce nombre n’est jamais évalué par rapport au paramètre `confidenceLevel` pour le modèle. Il s’agit d’une simple suggestion pour vous aider à choisir un niveau de confiance, si vous voulez en appliquer un. Pour les affinités, le paramètre `confidenceLevel` du modèle doit être supérieur au nombre `recommendedConfidence` pour une action de règle de transport Exchange à appeler. Le paramètre `recommendedConfidence` correspond au niveau de confiance par défaut utilisé dans les règles de transport Exchange qui appelle une action. Si vous le souhaitez, vous pouvez modifier manuellement la règle de transport Exchange à appeler pour le faire à partir du niveau de confiance du modèle.  <br/> |
   
## <a name="for-more-information"></a>Pour plus d’informations

- [Éléments recherchés par les types d’informations sensibles](what-the-sensitive-information-types-look-for.md)
    
- [Créer un type d’informations sensibles personnalisé](create-a-custom-sensitive-information-type.md)
    
- [Vue d’ensemble des stratégies de protection contre la perte de données](data-loss-prevention-policies.md)
    

