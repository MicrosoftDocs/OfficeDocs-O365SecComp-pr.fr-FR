---
title: Création d’une stratégie DLP pour protéger les documents avec l’ICF ou d’autres propriétés
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 6/29/2018
audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.UnifiedDLPRuleContentPropertyContainsWords
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
description: De nombreuses organisations appliquent déjà un processus permettant d’identifier et de classer les informations sensibles à l’aide des propriétés de classification dans l’infrastructure de classification des fichiers (ICF) Windows Server, des propriétés de document dans SharePoint ou des propriétés de document appliquées par un système tiers. Si vous reconnaissez votre organisation, vous pouvez créer une stratégie DLP dans Office 365 qui reconnaît les propriétés qui ont été appliquées aux documents par l’ICF Windows Server ou un autre système, afin que la stratégie DLP puisse être activée sur les documents Office avec une ICF ou d’autres valeurs de propriété spécifiques.
ms.openlocfilehash: 5f464c2918d7ea91fa5c65b28bc477ee7cc768e3
ms.sourcegitcommit: 7a0cb7e1da39fc485fc29e7325b843d16b9808af
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/07/2019
ms.locfileid: "36230958"
---
# <a name="create-a-dlp-policy-to-protect-documents-with-fci-or-other-properties"></a>Création d’une stratégie DLP pour protéger les documents avec l’ICF ou d’autres propriétés

Dans Office 365, vous pouvez utiliser une stratégie de protection contre la perte de données (DLP) pour identifier, surveiller et protéger les informations sensibles. De nombreuses organisations appliquent déjà un processus permettant d’identifier et de classer les informations sensibles à l’aide des propriétés de classification dans l’infrastructure de classification des fichiers (ICF) Windows Server, des propriétés de document dans SharePoint ou des propriétés de document appliquées par un système tiers. Si vous reconnaissez votre organisation, vous pouvez créer une stratégie DLP dans Office 365 qui reconnaît les propriétés qui ont été appliquées aux documents par l’ICF Windows Server ou un autre système, afin que la stratégie DLP puisse être activée sur les documents Office avec une ICF ou d’autres valeurs de propriété spécifiques.
  
![Diagramme illustrant Office 365 et le système de classement externe](media/59ad0ac1-4146-4919-abd1-c74d8508d25e.png)
  
Par exemple, votre organisation peut utiliser l’ICF Windows Server pour identifier les documents avec des informations d’identification personnelle (PII) telles que des numéros de sécurité sociale, puis classer le document en définissant la propriété **Informations d’identification personnelle** sur **Haut**, **Modéré**, **Faible**, **Public** ou **Non PII** selon le type et le nombre d’occurrences de PII trouvées dans le document. Dans Office 365, vous pouvez créer une stratégie DLP qui identifie les documents pour lesquels cette propriété est définie sur des valeurs spécifiques, telles que **Haut** et **Moyen**, puis exécute une action telle que le blocage de l’accès à ces fichiers. La même stratégie peut disposer d’une autre règle qui exécute une action différente si la propriété est définie sur **Faible**, telle que l’envoi d’une notification par courrier électronique. De cette manière, DLP dans Office 365 s’intègre à Windows Server ICF et peut aider à protéger les documents Office chargés ou partagés vers Office 365 à partir de serveurs de fichiers Windows Server.
  
Une stratégie DLP recherche simplement une paire nom/valeur de propriété spécifique. N’importe quelle propriété de document peut être utilisée, tant que la propriété possède une propriété gérée correspondante pour la recherche SharePoint. Par exemple, une collection de sites SharePoint peut utiliser un type de contenu nommé **Relevé de voyage** avec un champ obligatoire nommé **Client**. Lorsqu’une personne crée un relevé de voyage, elle doit entrer le nom du client. Cette paire nom/valeur de propriété peut également être utilisée dans une stratégie DLP, par exemple, si vous voulez une règle qui bloque l’accès au document pour les utilisateurs externes lorsque le champ **Client** contient **Contoso**.
  
Notez que si vous souhaitez appliquer votre stratégie DLP au contenu avec des étiquettes Office 365 spécifiques, vous ne devez pas suivre les étapes ci-dessous. Au lieu de cela, Découvrez comment [utiliser une étiquette comme condition dans une stratégie DLP](data-loss-prevention-policies.md#using-a-label-as-a-condition-in-a-dlp-policy).
  
## <a name="before-you-create-the-dlp-policy"></a>Avant de créer la stratégie DLP

Avant de pouvoir utiliser une propriété ICF Windows Server ou une autre propriété dans une stratégie DLP, vous devez créer une propriété gérée dans le Centre d’administration SharePoint. Voici pourquoi.
  
Exemples
  
C’est important car DLP dans Office 365 utilise le robot de recherche pour identifier et classer les informations sensibles sur vos sites, puis les stocker dans une partie sécurisée de l’index de recherche. Lorsque vous chargez un document vers Office 365, SharePoint crée automatiquement les propriétés analysées basées sur les propriétés du document. En revanche, pour utiliser une ICF ou une autre propriété dans une stratégie DLP, la propriété analysée doit être mappée sur une propriété gérée afin que le contenu avec cette propriété soit conservé dans l’index.
  
Pour plus d’informations sur la recherche et les propriétés gérées, consultez [la rubrique gérer le schéma de recherche dans SharePoint Online](http://go.microsoft.com/fwlink/p/?LinkID=627454).
  
### <a name="step-1-upload-a-document-with-the-needed-property-to-office-365"></a>Étape 1 : chargement d’un document avec la propriété nécessaire vers Office 365

Vous devez d’abord charger un document avec la propriété que vous souhaitez référencer dans votre stratégie DLP. Office 365 détecte la propriété et crée automatiquement une propriété analysée à partir de celle-ci. Dans l’étape suivante, vous allez créer une propriété gérée, puis mapper la propriété gérée sur cette propriété analysée.
  
### <a name="step-2-create-a-managed-property"></a>Étape 2 : création d’une propriété gérée

1. Connectez-vous au centre d’administration Microsoft 365.
    
2. Dans le volet de navigation de gauche, sélectionnez **centres** \> d’administration **SharePoint**. Vous vous trouvez maintenant dans le Centre d’administration SharePoint.
    
3. Dans le volet de navigation de gauche, sélectionnez **recherche** \> dans la \> **** page Administration de la **recherche** .
    
    ![Page d’administration de la recherche dans le Centre d’administration SharePoint](media/6bcd3aec-d11a-4f8c-9987-8f35da14d80b.png)
  
4. Sur la page \> **propriétés gérées** , **nouvelle propriété gérée**.
    
    ![Page Propriétés gérées avec le bouton Nouvelle propriété gérée mis en surbrillance](media/b161c764-414c-4037-83ed-503a49fb4410.png)
  
5. Entrez un nom et une description pour la propriété. Ce nom apparaîtra dans vos stratégies DLP.
    
6. Pour **Type**, sélectionnez **Texte**. 
    
7. Sous **Caractéristiques principales**, sélectionnez **Utilisable dans une requête** et **Affichable dans les résultats d’une recherche**.
    
8. Sous **mappages sur les propriétés** \> analysées, **Ajoutez un mappage**.
    
9. Dans la boîte \> de dialogue **sélection des propriétés analysées** , recherchez et sélectionnez la propriété analysée qui correspond à la propriété ICF de Windows Server ou à une autre propriété que vous \> utiliserez dans votre stratégie DLP **OK**.
    
    ![Boîte de dialogue de sélection des propriétés analysées](media/aeda1dce-1342-48bf-9594-a8e4f230e8aa.png)
  
10. Au bas de la page \> , **OK**.
    
## <a name="create-a-dlp-policy-that-uses-an-fci-property-or-other-property"></a>Création d’une stratégie DLP qui utilise une propriété ICF ou une autre propriété

Dans cet exemple, une organisation utilise ICF sur ses serveurs de fichiers Windows Server; en particulier, ils utilisent la propriété de classification ICF **appelée informations d’identification personnelle** avec des valeurs possibles: **élevé**, **modéré**, **faible**, **public**et **non PII**. À présent, ils veulent tirer parti de leur classification ICF existante dans leurs stratégies DLP dans Office 365.
  
D’abord, ils suivent les étapes ci-dessus pour créer une propriété gérée dans SharePoint Online, qui est mappée sur la propriété analysée créée automatiquement à partir de la propriété ICF.
  
Ensuite, ils créent une stratégie DLP avec deux règles qui utilisent les **Propriétés de document de condition contiennent l’une des valeurs**suivantes:
  
- **Contenu PII ICF-élevé, modéré** La première règle limite l’accès au document si les **informations d’identification personnelle** de la propriété de classification ICF est **élevée** ou **modérée** et que le document est partagé avec des personnes extérieures à l’organisation. 
    
- **Contenu PII ICF-faible** La deuxième règle envoie une notification au propriétaire du document si la propriété de classification ICF **informations d’identification personnelle** est **faible** et que le document est partagé avec des personnes extérieures à l’organisation. 
    
### <a name="create-the-dlp-policy-by-using-powershell"></a>Création de la stratégie DLP à l’aide de PowerShell

Notez que les propriétés de document de condition **contiennent l’une de ces valeurs** ne sont temporairement pas disponibles dans l' &amp; interface utilisateur du centre de sécurité conformité, mais vous pouvez toujours utiliser cette condition à l’aide de PowerShell. Vous pouvez utiliser les `New\Set\Get-DlpCompliancePolicy` cmdlets pour travailler avec une stratégie DLP et utiliser les `New\Set\Get-DlpComplianceRule` applets de commande avec `ContentPropertyContainsWords` le paramètre pour ajouter les **Propriétés de document de condition contiennent l’une de ces valeurs**.
  
Pour plus d’informations sur ces cmdlets, consultez [la rubrique &amp; Office 365 Security Compliance Center cmdlets](http://go.microsoft.com/fwlink/?LinkID=799772&amp;clcid=0x409).
  
1. [Se connecter au Centre de sécurité &amp; conformité Office 365 à l’aide de PowerShell à distance](http://go.microsoft.com/fwlink/?LinkID=799771&amp;clcid=0x409)
    
2. Créez la stratégie à l' `New-DlpCompliancePolicy`aide de.
    
    Voici un exemple de PowerShell qui crée une stratégie DLP qui s’applique à tous les emplacements.
    
      ```
      New-DlpCompliancePolicy -Name FCI_PII_policy -ExchangeLocation All -SharePointLocation All -OneDriveLocation All -Mode Enable
      ```

3. Créez les deux règles décrites ci-dessus `New-DlpComplianceRule`à l’aide de, où une règle est pour la valeur **faible** et une autre pour les valeurs **élevée** et **modérée** . 
    
    Voici un exemple PowerShell qui crée ces deux règles. Notez que les paires nom/valeur de la propriété sont placées entre guillemets et qu’un nom de propriété peut spécifier plusieurs valeurs séparées par des virgules sans espaces, comme`"<Property1>:<Value1>,<Value2>","<Property2>:<Value3>,<Value4>"....`
    
      ```
      New-DlpComplianceRule -Name FCI_PII_content-High,Moderate -Policy FCI_PII_policy -AccessScope NotInOrganization -BlockAccess $true -ContentPropertyContainsWords "Personally Identifiable Information:High,Moderate" -Disabled $falseNew-DlpComplianceRule -Name FCI_PII_content-Low -Policy FCI_PII_policy -AccessScope NotInOrganization -BlockAccess $false -ContentPropertyContainsWords "Personally Identifiable Information:Low" -Disabled $false -NotifyUser Owner
      ```

    Notez que Windows Server ICF inclut de nombreuses propriétés intégrées, notamment des **informations d’identification personnelle** utilisées dans cet exemple. Les valeurs possibles pour chaque propriété peuvent être différentes pour chaque organisation. Les valeurs **élevée**, **modérée**et **basse** utilisées ici ne sont qu’un exemple. Pour votre organisation, vous pouvez afficher les propriétés de classification Windows Server ICF avec leurs valeurs possibles dans le gestionnaire de ressources du serveur de fichiers sur le serveur de fichiers Windows Server. Pour plus d’informations, consultez [la rubrique Create a classification Property](http://go.microsoft.com/fwlink/p/?LinkID=627456).
    
Lorsque vous avez terminé, votre stratégie doit avoir deux nouvelles règles qui utilisent les **Propriétés du document contiennent l’une de ces valeurs** . Notez que cette condition n’apparaît pas dans l’interface utilisateur, bien que les autres conditions, actions et paramètres apparaissent. 
  
Une règle bloque l’accès au contenu pour lequel la propriété **Informations d’identification personnelle** est définie sur **Haut** ou **Modéré**. Une deuxième règle envoie une notification sur le contenu pour lequel la propriété **Informations d’identification personnelle** est définie sur **Faible**.
  
![Nouvelle boîte de dialogue de stratégie DLP montrant les deux règles venant d’être créées](media/5c56c13b-62a5-4f25-8eb7-ce83a844bb12.png)
  
## <a name="after-you-create-the-dlp-policy"></a>Après avoir créé la stratégie DLP

L’exécution des étapes décrites dans les sections précédentes crée une stratégie DLP qui détecte rapidement le contenu avec cette propriété, mais seulement si ce contenu est téléchargé (de sorte que le contenu est indexé) ou si ce contenu est ancien mais modifié (de sorte que le contenu soit à nouveau indexé) .
  
Pour détecter tout le contenu avec cette propriété, vous voudrez peut-être demander manuellement la réindexation de votre bibliothèque, site ou collection de sites, afin que la stratégie DLP connaisse tout le contenu avec cette propriété. Dans SharePoint Online, le contenu est automatiquement analysé selon une planification d’analyse définie. Le robot récupère le contenu qui a été modifié depuis la dernière analyse et met à jour l’index. Si vous avez besoin que votre stratégie DLP protège le contenu avant la prochaine analyse planifiée, vous pouvez suivre cette procédure.
  
> [!CAUTION]
> La réindexation d’un site peut entraîner une charge importante sur le système de recherche. Ne réindexez pas votre site, sauf si votre scénario l’exige. 
  
Pour plus d’informations, reportez-vous à [demander l’analyse et la réindexation manuelle d’un site, d’une bibliothèque ou d’une liste](http://go.microsoft.com/fwlink/p/?LinkID=627457).
  
### <a name="re-index-a-site-optional"></a>Réindexation d’un site (facultatif)

1. Sur le site, choisissez **paramètres** (icône d’engrenage dans le coin \> **** supérieur droit).
    
2. Sous **recherche**, choisissez **site**de réindexation **de la recherche et de la disponibilité** \> hors connexion.
    
## <a name="more-information"></a>Plus d’informations

- [Vue d’ensemble des stratégies de protection contre la perte de données](data-loss-prevention-policies.md)
    
- [Création d’une stratégie DLP à partir d’un modèle](create-a-dlp-policy-from-a-template.md)
    
- [Envoi des notifications et affichage des conseils de stratégie pour les stratégies DLP](use-notifications-and-policy-tips.md)
    
- [Contenu des modèles de stratégie DLP](what-the-dlp-policy-templates-include.md)
    
- [Inventaire des types d'informations sensibles](what-the-sensitive-information-types-look-for.md)
    

