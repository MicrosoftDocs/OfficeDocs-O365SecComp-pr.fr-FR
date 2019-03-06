---
title: Créer un type d’informations sensibles personnalisé
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Découvrez comment créer, modifier, supprimer et tester des types d’informations sensibles personnalisés pour DLP dans l’interface utilisateur graphique dans le Centre de sécurité et conformité Office 365.
ms.openlocfilehash: 16bc49f23de20479ed18ce56720fd70a05b986e3
ms.sourcegitcommit: ed822a776d3419853453583e882f3c61ca26d4b2
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "30410809"
---
# <a name="create-a-custom-sensitive-information-type"></a><span data-ttu-id="24f0e-103">Créer un type d’informations sensibles personnalisé</span><span class="sxs-lookup"><span data-stu-id="24f0e-103">Create a custom sensitive information type</span></span>

<span data-ttu-id="24f0e-p101">La protection contre la perte de données (DLP) dans Office 365 inclut de nombreux [types d’informations sensibles](what-the-sensitive-information-types-look-for.md) intégrés qui sont prêts à l’emploi dans vos stratégies DLP. Ces types intégrés permettent d’identifier et de protéger les numéros de carte de crédit, les numéros de compte bancaire, les numéros de passeport, et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="24f0e-p101">Data loss prevention (DLP) in Office 365 includes many built-in [sensitive information types](what-the-sensitive-information-types-look-for.md) that are ready for you to use in your DLP policies. These built-in types can help identify and protect credit card numbers, bank account numbers, passport numbers, and more.</span></span> 

<span data-ttu-id="24f0e-106">Cependant, si vous devez identifier et protéger un autre type d’informations sensibles (par exemple, l’ID des employés ou des numéros de projet qui utilisent un format spécifique de votre organisation), vous pouvez créer un type d’informations sensibles personnalisé.</span><span class="sxs-lookup"><span data-stu-id="24f0e-106">But if you need to identify and protect a different type of sensitive information (for example, employee IDs or project numbers that uses a format specific to your organization) you can create a custom sensitive information type.</span></span>

<span data-ttu-id="24f0e-107">Les éléments fondamentaux d’un type d’informations sensibles personnalisé sont :</span><span class="sxs-lookup"><span data-stu-id="24f0e-107">The fundamental parts of a custom sensitive information type are:</span></span>

- <span data-ttu-id="24f0e-108">**Modèle principal** : numéros d’identification d’employé, numéros de projet, etc. Cela est généralement identifié par une expression régulière (RegEx) mais il peut aussi s’agir d’une liste de mots clés.</span><span class="sxs-lookup"><span data-stu-id="24f0e-108">**Primary pattern**: employee ID numbers, project numbers, etc. This is typically identified by a regular expression (RegEx), but it can also be a list of keywords.</span></span>

- <span data-ttu-id="24f0e-p102">**Preuves supplémentaires** : supposons que vous recherchez un numéro d’identification d’employé à neuf chiffres. Tous les numéros à neuf chiffres ne sont pas des numéros d’identification d’employé, donc vous pouvez rechercher un texte supplémentaire : les mots clés comme « employé », « badge », « ID » ou d’autres modèles de texte suivant d’autres expressions régulières. Cette preuve (également appelée preuve _justificative_ ou _probante_) augmente la probabilité que le nombre à neuf chiffres trouvé dans le contenu est réellement un numéro d’identification d’employé.</span><span class="sxs-lookup"><span data-stu-id="24f0e-p102">**Additional evidence**: Suppose you're looking for a nine-digit employee ID number. Not all nine-digit numbers are employee ID numbers, so you can look for additional text: keywords like "employee", "badge", "ID", or other text patterns based on additional regular expressions. This supporting evidence (also known as _supporting_ or _corroborative_ evidence) increases the likelihood that nine-digit number found in content is really an employee ID number.</span></span>

- <span data-ttu-id="24f0e-p103">**Proximité de caractère** : il est logique que plus le modèle principal et la preuve justificative sont proches, plus le contenu détecté a des chances d’être ce que vous recherchez. Vous pouvez spécifier la distance de caractère entre le modèle principal et la preuve justificative (également appelée _fenêtre de proximité_) comme illustré dans le diagramme suivant :</span><span class="sxs-lookup"><span data-stu-id="24f0e-p103">**Character proximity**: It makes sense that the closer the primary pattern and the supporting evidence are to each other, the more likely the detected content is going to be what you're looking for. You can specify the character distance between the primary pattern and the supporting evidence (also known as the _proximity window_) as shown in the following diagram:</span></span>

    ![Diagramme de la fenêtre de proximité et de preuves probantes](media/dc68e38e-dfa1-45b8-b204-89c8ba121f96.png)

- <span data-ttu-id="24f0e-p104">**Niveau de confiance** : plus la preuve que vous possédez est justificative, plus la probabilité qu’un résultat contienne les informations sensibles que vous recherchez est élevée. Vous pouvez affecter des niveaux de confiance supérieurs pour les correspondances détectées en utilisant plus de preuves.</span><span class="sxs-lookup"><span data-stu-id="24f0e-p104">**Confidence level**: The more supporting evidence you have, the higher the likelihood that a match contains the sensitive information you're looking for. You can assign higher levels of confidence for matches that are detected by using more evidence.</span></span>

  <span data-ttu-id="24f0e-p105">Lorsqu’il est satisfait, un modèle renvoie un nombre et un niveau de confiance, que vous pouvez utiliser dans les conditions dans votre stratégie DLP. Lorsque vous ajoutez une condition de détection d’un type d’informations sensibles à une stratégie DLP, vous pouvez modifier le nombre et le niveau de confiance comme illustré dans le diagramme suivant :</span><span class="sxs-lookup"><span data-stu-id="24f0e-p105">When satisfied, a pattern returns a count and confidence level, which you can use in the conditions in your DLP policies. When you add a condition for detecting a sensitive information type to a DLP policy, you can edit the count and confidence level as shown in the following diagram:</span></span>

    ![Nombre d’instances et options de précision des résultats](media/11d0b51e-7c3f-4cc6-96d8-b29bcdae1aeb.png)

<span data-ttu-id="24f0e-120">Vous disposez des options suivantes pour créer des types d’informations sensibles personnalisés dans le Centre de Conformité et Sécurité Office 365 :</span><span class="sxs-lookup"><span data-stu-id="24f0e-120">To create custom sensitive information types in the Office 365 Security & Compliance Center, you have the following options:</span></span>

- <span data-ttu-id="24f0e-p106">**Utiliser l’interface utilisateur** : cette méthode est plus facile et plus rapide, mais vous disposez de moins d’options de configuration que PowerShell. Le reste de cette rubrique décrit ces procédures.</span><span class="sxs-lookup"><span data-stu-id="24f0e-p106">**Use the UI**: This method is easier and faster, but you have less configuration options than PowerShell. The rest of this topic describes these procedures.</span></span>

- <span data-ttu-id="24f0e-p107">**Utiliser PowerShell** : cette méthode exige que vous commenciez par créer un fichier XML (appelé _package de règles_) contenant un ou plusieurs types d’informations sensibles, puis que vous utilisiez PowerShell pour importer le package de règles (l’importation du package de règles est simple par rapport à la création du package de règles). Cette méthode est beaucoup plus complexe que l’interface utilisateur, mais vous disposez de davantage d’options de configuration. Pour obtenir des instructions, consultez la rubrique [Créer un type d’informations sensibles personnalisé dans le Centre de Conformité et Sécurité Office 365 PowerShell](create-a-custom-sensitive-information-type-in-scc-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="24f0e-p107">**Use PowerShell**: This method requires that you first create an XML file (called a _rule package_) that contains one or more sensitive information types, and then you use PowerShell to import the rule package (importing the rule package is trivial compared to creating the rule package. This method is much more complex than the UI, but you have more configuration options. For instructions, see [Create a custom sensitive information type in Office 365 Security & Compliance Center PowerShell](create-a-custom-sensitive-information-type-in-scc-powershell.md).</span></span>

<span data-ttu-id="24f0e-126">Les différences clés sont décrites dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="24f0e-126">The key differences are described in the following table:</span></span>

|<span data-ttu-id="24f0e-127">**Types d’informations sensibles personnalisés dans l’interface utilisateur**</span><span class="sxs-lookup"><span data-stu-id="24f0e-127">**Custom sensitive information types in the UI**</span></span>|<span data-ttu-id="24f0e-128">**Types d’informations sensibles personnalisés dans PowerShell**</span><span class="sxs-lookup"><span data-stu-id="24f0e-128">**Custom sensitive information types in PowerShell**</span></span>|
|:-----|:-----|
|<span data-ttu-id="24f0e-129">Le nom et la description apparaissent dans une langue.</span><span class="sxs-lookup"><span data-stu-id="24f0e-129">Name and Description are in one language.</span></span>|<span data-ttu-id="24f0e-130">Prend en charge plusieurs langues pour le nom et la description.</span><span class="sxs-lookup"><span data-stu-id="24f0e-130">Supports multiple languages for Name and Description.</span></span>|
|<span data-ttu-id="24f0e-131">Prend en charge un motif.</span><span class="sxs-lookup"><span data-stu-id="24f0e-131">Supports one pattern.</span></span>|<span data-ttu-id="24f0e-132">Prend en charge plusieurs motifs.</span><span class="sxs-lookup"><span data-stu-id="24f0e-132">Supports multiple patterns.</span></span>|
|<span data-ttu-id="24f0e-133">La preuve justificative peut être :</span><span class="sxs-lookup"><span data-stu-id="24f0e-133">Supporting evidence can be:</span></span> <br/><span data-ttu-id="24f0e-134">• Expressions régulières</span><span class="sxs-lookup"><span data-stu-id="24f0e-134">• Regular expressions</span></span> <br/><span data-ttu-id="24f0e-135">• Mots clés</span><span class="sxs-lookup"><span data-stu-id="24f0e-135">• Keywords</span></span> <br/><span data-ttu-id="24f0e-136">• Dictionnaires de mots clés</span><span class="sxs-lookup"><span data-stu-id="24f0e-136">• Keyword dictionaries</span></span>|<span data-ttu-id="24f0e-137">La preuve justificative peut être :</span><span class="sxs-lookup"><span data-stu-id="24f0e-137">Supporting evidence can be:</span></span> <br/><span data-ttu-id="24f0e-138">• Expressions régulières</span><span class="sxs-lookup"><span data-stu-id="24f0e-138">• Regular expressions</span></span> <br/><span data-ttu-id="24f0e-139">• Mots clés</span><span class="sxs-lookup"><span data-stu-id="24f0e-139">• Keywords</span></span> <br/><span data-ttu-id="24f0e-140">• Dictionnaires de mots clés</span><span class="sxs-lookup"><span data-stu-id="24f0e-140">• Keyword dictionaries</span></span> <br/><span data-ttu-id="24f0e-141">• [Fonctions DLP intégrées](what-the-dlp-functions-look-for.md)</span><span class="sxs-lookup"><span data-stu-id="24f0e-141">• [Built-in DLP functions](what-the-dlp-functions-look-for.md)</span></span>|
|<span data-ttu-id="24f0e-142">Types d’informations sensibles personnalisés ajoutées au package de règles nommé Microsoft.SCCManaged.CustomRulePack</span><span class="sxs-lookup"><span data-stu-id="24f0e-142">Custom sensitive information types are added to the rule package named Microsoft.SCCManaged.CustomRulePack</span></span>|<span data-ttu-id="24f0e-143">Vous pouvez créer jusqu'à 10 packages de règles contenant des types d’informations sensibles personnalisés.</span><span class="sxs-lookup"><span data-stu-id="24f0e-143">You can create up to 10 rule packages that contain custom sensitive information types.</span></span>|
|<span data-ttu-id="24f0e-144">La recherche par modèle exige la détection du modèle principal et de toutes les preuves justificatives (l’opérateur implicite AND est utilisé).</span><span class="sxs-lookup"><span data-stu-id="24f0e-144">Pattern match requires the detection of the primary pattern and all supporting evidence (the implicit AND operator is used).</span></span>|<span data-ttu-id="24f0e-145">La recherche par modèle exige la détection du modèle principal et d’un nombre configurable de preuves justificatives (les opérateurs implicites AND et OR sont utilisés).</span><span class="sxs-lookup"><span data-stu-id="24f0e-145">Pattern match requires the detection of the primary pattern and a configurable amount of supporting evidence (implicit AND and OR operators can be used).</span></span>|

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="24f0e-146">Ce qu’il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="24f0e-146">What do you need to know before you begin?</span></span>

- <span data-ttu-id="24f0e-147">Pour ouvrir le Centre de conformité et sécurité, consultez la rubrique [Accéder au centre de conformité et sécurité d’Office 365](go-to-the-securitycompliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="24f0e-147">To open the Security & Compliance Center, see [Go to the Office 365 Security & Compliance Center](go-to-the-securitycompliance-center.md).</span></span>

- <span data-ttu-id="24f0e-p108">Les types d’informations sensibles personnalisés exigent des connaissances relatives aux expressions régulières (RegEx). Pour plus d’informations sur le moteur Boost.RegEx (anciennement appelé RegEx++) utilisé pour le traitement du texte, consultez l’article [Boost.Regex 5.1.3](https://www.boost.org/doc/libs/1_68_0/libs/regex/doc/html/).</span><span class="sxs-lookup"><span data-stu-id="24f0e-p108">Custom sensitive information types require familiarity with regular expressions (RegEx). For more information about the Boost.RegEx (formerly known as RegEx++) engine that's used for processing the text, see [Boost.Regex 5.1.3](https://www.boost.org/doc/libs/1_68_0/libs/regex/doc/html/).</span></span>

  <span data-ttu-id="24f0e-p109">Le Support technique et Service clientèle Microsoft ne peut pas aider à fournir des définitions de recherche de contenu personnalisées (création de classifications personnalisées ou de modèles d’expressions régulières). Les ingénieurs du support technique peuvent fournir un support limité pour la fonctionnalité (en fournissant, par exemple, des exemples de modèles d’expressions régulières à des fins de test, ou en aidant à résoudre des problèmes avec un modèle d’expression régulière existant ne se déclenchant pas comme prévu), mais ne peuvent pas garantir que le développement de correspondance de contenu personnalisé satisfera vos exigences ou obligations.</span><span class="sxs-lookup"><span data-stu-id="24f0e-p109">Microsoft Customer Service & Support can't assist with providing custom content-matching definitions (creating custom classifications or regular expression patterns). Support engineers can provide limited support for the feature (for example, providing sample regular expression patterns for testing purposes, or assisting with troubleshooting an existing regular expression pattern that's not triggering as expected), but can't provide assurances that any custom content-matching development will fulfill your requirements or obligations.</span></span>

- <span data-ttu-id="24f0e-p110">DLP utilise le robot de recherche pour identifier et classer les informations sensibles dans les sites SharePoint Online et OneDrive Entreprise. Pour identifier votre nouveau type d’informations sensibles personnalisé dans le contenu existant, le contenu doit être de nouveau analysé. La nouvelle analyse du contenu est planifiée mais vous pouvez réanalyser manuellement le contenu pour une collection de sites, une liste ou une bibliothèque. Pour plus d’informations, consultez la rubrique relative à la façon de [demander manuellement l’analyse et la réindexation d’un site, d’une bibliothèque ou d’une liste](https://docs.microsoft.com/sharepoint/crawl-site-content).</span><span class="sxs-lookup"><span data-stu-id="24f0e-p110">DLP uses the search crawler to identify and classify sensitive information in SharePoint Online and OneDrive for Business sites. To identify your new custom sensitive information type in existing content, the content must be recrawled. Content is recrawled based on a schedule, but you can manually recrawl content for a site collection, list, or library. For more information, see [Manually request crawling and re-indexing of a site, a library or a list](https://docs.microsoft.com/sharepoint/crawl-site-content).</span></span>

## <a name="create-custom-sensitive-information-types-in-the-security--compliance-center"></a><span data-ttu-id="24f0e-156">Créer un type d’informations sensibles personnalisé dans le Centre de Conformité et Sécurité</span><span class="sxs-lookup"><span data-stu-id="24f0e-156">Create custom sensitive information types in the Security & Compliance Center</span></span>

<span data-ttu-id="24f0e-157">Dans le Centre de Conformité et Sécurité, accédez à **Classifications** \> **Types d’informations sensibles** et cliquez sur **Créer**.</span><span class="sxs-lookup"><span data-stu-id="24f0e-157">In the Security & Compliance Center, go to **Classifications** \> **Sensitive info types** and click **Create**.</span></span>

<span data-ttu-id="24f0e-158">Les paramètres sont relativement évidents. Ils sont décrits sur la page associée de l’Assistant :</span><span class="sxs-lookup"><span data-stu-id="24f0e-158">The settings are fairly self-evident, and are explained on the associate page of the wizard:</span></span>

- <span data-ttu-id="24f0e-159">**Nom**</span><span class="sxs-lookup"><span data-stu-id="24f0e-159">**Name**</span></span>

- <span data-ttu-id="24f0e-160">**Description**</span><span class="sxs-lookup"><span data-stu-id="24f0e-160">**Description**</span></span>

- <span data-ttu-id="24f0e-161">**Proximité**</span><span class="sxs-lookup"><span data-stu-id="24f0e-161">**Proximity**</span></span>

- <span data-ttu-id="24f0e-162">**Niveau de confiance**</span><span class="sxs-lookup"><span data-stu-id="24f0e-162">**Confidence level**</span></span>

- <span data-ttu-id="24f0e-163">**Élément de modèle principal** (mots clés, expression régulière ou dictionnaire)</span><span class="sxs-lookup"><span data-stu-id="24f0e-163">**Primary pattern element** (keywords, regular expression, or dictionary)</span></span>

- <span data-ttu-id="24f0e-164">Facultatif **Éléments de modèle pris en charge** (mots clés, expression régulière ou dictionnaire) et une valeur de **Coût minimum** correspondante.</span><span class="sxs-lookup"><span data-stu-id="24f0e-164">Optional **Supporting pattern elements** (keywords, regular expression, or dictionary) and a corresponding **Minimum cost** value.</span></span>

<span data-ttu-id="24f0e-p111">Voici un scénario : vous souhaitez créer un type d’informations sensibles personnalisé qui détecte les numéros d’identification d’employé à 9 chiffres dans un contenu, ainsi que les mots clés « employé », « ID » et « badge ». Pour créer ce type d’informations sensibles personnalisé, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="24f0e-p111">Here's a scenario: You want a custom sensitive information type that detects 9-digit employee numbers in content, along with the keywords "employee" "ID" and "badge". To create this custom sensitive information type, do the following steps:</span></span>

1. <span data-ttu-id="24f0e-167">Dans le Centre de conformité et sécurité, accédez à **Classifications** \> **Types d’informations sensibles** et cliquez sur **Créer**.</span><span class="sxs-lookup"><span data-stu-id="24f0e-167">In the Security & Compliance Center, go to **Classifications** \> **Sensitive info types** and click **Create**.</span></span>

    ![Emplacement des types d’informations sensibles et bouton Créer](media/scc-cust-sens-info-type-new.png)

2. <span data-ttu-id="24f0e-169">Sur la page **Choisir un nom et une description** qui s’ouvre, entrez les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="24f0e-169">In the **Choose a name and description** page that opens, enter the following values:</span></span>

  - <span data-ttu-id="24f0e-170">**Nom** : ID d’employé.</span><span class="sxs-lookup"><span data-stu-id="24f0e-170">**Name**: Employee ID.</span></span>

  - <span data-ttu-id="24f0e-171">**Description** : détecte les numéros d’identification d’employé Contoso à neuf chiffres.</span><span class="sxs-lookup"><span data-stu-id="24f0e-171">**Description**: Detect nine-digit Contoso employee ID numbers.</span></span>

    ![Nom et page de description](media/scc-cust-sens-info-type-new-name-desc.png)

    <span data-ttu-id="24f0e-173">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="24f0e-173">When you're finished, click **Next**.</span></span>

3. <span data-ttu-id="24f0e-174">Sur la page **Conditions requises pour la correspondance** qui s’ouvre, cliquez sur **Ajouter un élément** et configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="24f0e-174">In the **Requirements for matching** page that opens, click **Add an element** configure the following settings:</span></span>

    - <span data-ttu-id="24f0e-175">**Détecter le contenu contenant** :</span><span class="sxs-lookup"><span data-stu-id="24f0e-175">**Detect content containing**:</span></span>
 
      <span data-ttu-id="24f0e-p112">a. Cliquez sur **L’un de ces éléments** et sélectionnez **Expression régulière**.</span><span class="sxs-lookup"><span data-stu-id="24f0e-p112">a. Click **Any of these** and select **Regular expression**.</span></span>

      <span data-ttu-id="24f0e-p113">b. Dans la zone de l’expression régulière, entrez `(\s)(\d{9})(\s)` (numéros à neuf chiffres encadrés d’un espace blanc)</span><span class="sxs-lookup"><span data-stu-id="24f0e-p113">b. In the regular expression box, enter `(\s)(\d{9})(\s)` (nine-digit numbers surrounded by white space).</span></span>
  
    - <span data-ttu-id="24f0e-180">**Éléments de prise en charge** : cliquez sur **Ajouter des éléments de prise en charge** et sélectionnez **Contient cette liste de mots clés**.</span><span class="sxs-lookup"><span data-stu-id="24f0e-180">**Supporting elements**: Click **Add supporting elements** and select **Contains this keyword list**.</span></span>

    - <span data-ttu-id="24f0e-181">Dans la zone **Contient cette liste de mots clés** qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="24f0e-181">In the **Contains this keyword list** area that appears, configure the following settings:</span></span>

      - <span data-ttu-id="24f0e-182">**Liste de mots clés** : saisissez la valeur suivante : employé, ID, badge.</span><span class="sxs-lookup"><span data-stu-id="24f0e-182">**Keyword list**: Enter the following value: employee,ID,badge.</span></span>

      - <span data-ttu-id="24f0e-183">**Nombre minimal** : conservez la valeur par défaut 1.</span><span class="sxs-lookup"><span data-stu-id="24f0e-183">**Minimum count**: Leave the default value 1.</span></span>

    - <span data-ttu-id="24f0e-184">Conservez la valeur par défaut **Niveau de confiance** 60.</span><span class="sxs-lookup"><span data-stu-id="24f0e-184">Leave the default **Confidence level** value 60.</span></span> 

    - <span data-ttu-id="24f0e-185">Conservez la valeur par défaut **Caractère de proximité** 300.</span><span class="sxs-lookup"><span data-stu-id="24f0e-185">Leave the default **Character proximity** value 300.</span></span>

    ![Configuration requise pour la page correspondante](media/scc-cust-sens-info-type-new-reqs.png)

    <span data-ttu-id="24f0e-187">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="24f0e-187">When you're finished, click **Next**.</span></span>

4. <span data-ttu-id="24f0e-188">Sur la page **Revoir et finaliser** qui s’affiche, passez en revue les paramètres, puis cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="24f0e-188">On the **Review and finalize** page that opens, review the settings and click **Finish**.</span></span>

    ![Examen et finalisation de la page](media/scc-cust-sens-info-type-new-review.png)

5. <span data-ttu-id="24f0e-p114">La page suivante vous encourage à tester le nouveau type d’informations sensibles personnalisés en cliquant sur **Oui**. Pour plus d’informations, reportez-vous à l’article [Tester des types d’informations sensibles personnalisés dans le Centre de conformité et sécurité](#test-custom-sensitive-information-types-in-the-security--compliance-center). Sinon, cliquez sur **Non**.</span><span class="sxs-lookup"><span data-stu-id="24f0e-p114">The next page encourages you to test the new custom sensitive information type by clicking **Yes**. For more information, see [Test custom sensitive information types in the Security & Compliance Center](#test-custom-sensitive-information-types-in-the-security--compliance-center). To test the rule later, click **No**.</span></span>

    ![Page de recommandation de test](media/scc-cust-sens-info-type-new-test.png)

### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="24f0e-194">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="24f0e-194">How do you know this worked?</span></span>

<span data-ttu-id="24f0e-195">Pour vérifier que vous avez correctement créé un nouveau type d’informations sensibles, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="24f0e-195">To verify that you've successfully created a new sensitive information type, do any of the following steps:</span></span>

  - <span data-ttu-id="24f0e-196">Accédez à **Classifications** \> **Types d’informations sensibles** et vérifiez que le nouveau type d’informations sensibles personnalisé apparaît.</span><span class="sxs-lookup"><span data-stu-id="24f0e-196">Go to **Classifications** \> **Sensitive info types** and verify the new custom sensitive information type is listed.</span></span>

  - <span data-ttu-id="24f0e-p115">Testez le nouveau type d’informations sensibles personnalisés. Pour plus d’informations, reportez-vous à la rubrique [Tester des types d’informations sensibles personnalisés dans le Centre de Conformité et Sécurité](#test-custom-sensitive-information-types-in-the-security--compliance-center).</span><span class="sxs-lookup"><span data-stu-id="24f0e-p115">Test the new custom sensitive information type. For more information, see [Test custom sensitive information types in the Security & Compliance Center](#test-custom-sensitive-information-types-in-the-security--compliance-center).</span></span>

## <a name="modify-custom-sensitive-information-types-in-the-security--compliance-center"></a><span data-ttu-id="24f0e-199">Modifier des types d’informations sensibles personnalisés dans le Centre de conformité et sécurité</span><span class="sxs-lookup"><span data-stu-id="24f0e-199">Modify custom sensitive information types in the Security & Compliance Center</span></span>

<span data-ttu-id="24f0e-200">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="24f0e-200">**Notes**:</span></span>

- <span data-ttu-id="24f0e-p116">Vous pouvez modifier uniquement les types d’informations sensibles personnalisés ; vous ne pouvez pas modifier les types d’informations sensibles intégrés. Cependant, vous pouvez utiliser PowerShell pour exporter des types d’informations sensibles personnalisés intégrés, les personnaliser et les importer comme types d’informations sensibles personnalisés. Pour plus d’informations, consultez la rubrique [Personnaliser un type d’informations sensibles intégré](customize-a-built-in-sensitive-information-type.md).</span><span class="sxs-lookup"><span data-stu-id="24f0e-p116">You can only modify custom sensitive information types; you can't modify built-in sensitive information types. But you can use PowerShell to export built-in custom sensitive information types, customize them, and import them as custom sensitive information types. For more information, see [Customize a built-in sensitive information type](customize-a-built-in-sensitive-information-type.md).</span></span>

- <span data-ttu-id="24f0e-p117">Vous pouvez uniquement modifier les types d’informations sensibles personnalisés que vous avez créés dans l’interface utilisateur. Si vous avez utilisé la [procédure PowerShell](create-a-custom-sensitive-information-type-in-scc-powershell.md) pour importer un package de règles pour les types d’informations sensibles personnalisés, vous recevrez une erreur.</span><span class="sxs-lookup"><span data-stu-id="24f0e-p117">You can only modify custom sensitive information types that you created in the UI. If you used the [PowerShell procedure](create-a-custom-sensitive-information-type-in-scc-powershell.md) to import a custom sensitive information type rule package, you'll get an error.</span></span>

<span data-ttu-id="24f0e-206">Dans le Centre de conformité et sécurité, accédez à **Classifications** \> **Types d’informations sensibles**, sélectionnez le type d’informations sensibles personnalisé à modifier, puis cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="24f0e-206">In the Security & Compliance Center, go to **Classifications** \> **Sensitive info types**, select the custom sensitive information type that you want to modify, and then click **Edit**.</span></span>

  ![Emplacement des types d’informations sensibles et bouton Modifier](media/scc-cust-sens-info-type-edit.png)

<span data-ttu-id="24f0e-p118">Les mêmes options sont disponibles ici comme lorsque vous avez créé le type d’informations sensibles personnalisé dans le Centre de Conformité et Sécurité. Pour plus d’informations, consultez la rubrique [Créer un type d’informations sensibles personnalisé dans le Centre de Conformité et Sécurité](#create-custom-sensitive-information-types-in-the-security--compliance-center).</span><span class="sxs-lookup"><span data-stu-id="24f0e-p118">The same options are available here as when you created the custom sensitive information type in the Security & Compliance Center. For more information, see [Create custom sensitive information types in the Security & Compliance Center](#create-custom-sensitive-information-types-in-the-security--compliance-center).</span></span>

### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="24f0e-210">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="24f0e-210">How do you know this worked?</span></span>

<span data-ttu-id="24f0e-211">Pour vérifier que vous avez correctement modifié un type d’informations sensibles, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="24f0e-211">To verify that you've successfully modified a sensitive information type, do any of the following steps:</span></span>

  - <span data-ttu-id="24f0e-212">Accédez à **Classifications** \> **Types d’informations sensibles** pour vérifier les propriétés du type d’informations sensibles personnalisé modifié.</span><span class="sxs-lookup"><span data-stu-id="24f0e-212">Go to **Classifications** \> **Sensitive info types** to verify the properties of the modified custom sensitive information type.</span></span> 

  - <span data-ttu-id="24f0e-p119">Testez le type d’informations sensibles personnalisés modifié. Pour plus d’informations, reportez-vous à la rubrique [Tester des types d’informations sensibles personnalisés dans le Centre de Conformité et Sécurité](#test-custom-sensitive-information-types-in-the-security--compliance-center).</span><span class="sxs-lookup"><span data-stu-id="24f0e-p119">Test the modified custom sensitive information type. For more information, see [Test custom sensitive information types in the Security & Compliance Center](#test-custom-sensitive-information-types-in-the-security--compliance-center).</span></span>

## <a name="remove-custom-sensitive-information-types-in-the-security--compliance-center"></a><span data-ttu-id="24f0e-215">Supprimer des types d’informations sensibles personnalisés dans le Centre de Conformité et Sécurité</span><span class="sxs-lookup"><span data-stu-id="24f0e-215">Remove custom sensitive information types in the Security & Compliance Center</span></span> 

<span data-ttu-id="24f0e-216">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="24f0e-216">**Notes**:</span></span>

- <span data-ttu-id="24f0e-217">Vous pouvez uniquement supprimer des types d’informations sensibles personnalisés ; vous ne pouvez pas supprimer des types d’informations sensibles intégrés.</span><span class="sxs-lookup"><span data-stu-id="24f0e-217">You can only remove custom sensitive information types; you can't remove built-in sensitive information types.</span></span>

- <span data-ttu-id="24f0e-218">Avant de supprimer un type d’informations sensibles personnalisé, vérifiez qu’aucune stratégie DLP ou règle de flux de courrier Exchange (également appelées règles de transport) ne référence toujours le type d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="24f0e-218">Before your remove a custom sensitive information type, verify that no DLP policies or Exchange mail flow rules (also known as transport rules) still reference the sensitive information type.</span></span>

1. <span data-ttu-id="24f0e-219">Dans le Centre de Conformité et Sécurité, accédez à **Classifications** \> **Types d’informations sensibles** et sélectionnez un ou plusieurs types d’informations sensibles personnalisés à supprimer.</span><span class="sxs-lookup"><span data-stu-id="24f0e-219">In the Security & Compliance Center, go to **Classifications** \> **Sensitive info types** and select one or more custom sensitive information types that you want to remove.</span></span>

2. <span data-ttu-id="24f0e-220">Dans la boîte de dialogue qui s’ouvre, cliquez sur **Supprimer** (ou **Supprimer des types d’informations sensibles** si vous en avez sélectionnés plusieurs).</span><span class="sxs-lookup"><span data-stu-id="24f0e-220">In the fly-out that opens, click **Delete** (or **Delete sensitive info types** if you selected more than one).</span></span>

    ![Emplacement des types d’informations sensibles et bouton Supprimer](media/scc-cust-sens-info-type-delete.png)

3. <span data-ttu-id="24f0e-222">Cliquez sur **Oui** lorsque le message d’avertissement s’affiche.</span><span class="sxs-lookup"><span data-stu-id="24f0e-222">In the warning message that appears, click **Yes**.</span></span>

### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="24f0e-223">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="24f0e-223">How do you know this worked?</span></span>

<span data-ttu-id="24f0e-224">Pour vérifier que vous avez supprimé correctement un type d’informations sensibles personnalisé, accédez à **Classifications** \> **Types d’informations sensibles** pour vérifier que le type d’informations sensibles personnalisé n’est plus répertorié.</span><span class="sxs-lookup"><span data-stu-id="24f0e-224">To verify that you've successfully removed a custom sensitive information type, go to **Classifications** \> **Sensitive info types** to verify the custom sensitive information type is no longer listed.</span></span>

## <a name="test-custom-sensitive-information-types-in-the-security--compliance-center"></a><span data-ttu-id="24f0e-225">Tester des types d’informations sensibles personnalisés dans le Centre de Conformité et Sécurité</span><span class="sxs-lookup"><span data-stu-id="24f0e-225">Test custom sensitive information types in the Security & Compliance Center</span></span>

1. <span data-ttu-id="24f0e-226">Dans le Centre de Conformité et Sécurité, accédez à **Classifications** \> **Types d’informations sensibles**.</span><span class="sxs-lookup"><span data-stu-id="24f0e-226">In the Security & Compliance Center, go to **Classifications** \> **Sensitive info types**.</span></span>

2. <span data-ttu-id="24f0e-p120">Sélectionnez un ou plusieurs types d’informations sensibles personnalisés à tester. Dans la boîte de dialogue qui s’ouvre, cliquez sur **Type de test** (ou **Tester des types d’informations sensibles** si vous en avez sélectionnés plusieurs).</span><span class="sxs-lookup"><span data-stu-id="24f0e-p120">Select one or more custom sensitive information types to test. In the fly-out that opens, click **Test type** (or **Test sensitive info types** if you selected more than one).</span></span>

    ![Emplacement des types d’informations sensibles et bouton Tester le type](media/scc-cust-sens-info-type-test.png)

3. <span data-ttu-id="24f0e-230">Dans la page **Télécharger le fichier à tester** qui s’ouvre, chargez un document à tester en faisant glisser un fichier ou en cliquant sur **Parcourir** et en sélectionnant un fichier.</span><span class="sxs-lookup"><span data-stu-id="24f0e-230">On the **Upload file to test** page that opens, upload a document to test by dragging and dropping a file or by clicking **Browse** and selecting a file.</span></span>

    ![Charger le fichier sur la page de test](media/scc-cust-sens-info-type-test-upload.png)

4. <span data-ttu-id="24f0e-232">Cliquez sur le bouton **Tester** pour rechercher des modèles dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="24f0e-232">Click the **Test** button to test the document for pattern matches in the file.</span></span>

5. <span data-ttu-id="24f0e-233">Sur la page **Mettre en correspondance les résultats**, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="24f0e-233">On the **Match results** page, click **Finish**.</span></span>

    ![Mettre en correspondance les résultats](media/scc-cust-sens-info-type-test-results.png)