---
title: Création d’une stratégie DLP pour protéger les documents avec l’ICF ou d’autres propriétés
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.UnifiedDLPRuleContentPropertyContainsWords
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Strat_O365_IP
ms.assetid: 1b9e3c6c-4308-4a20-b11e-c37b8013e177
description: Bon nombre d’organisations ont déjà un processus pour identifier et classer les informations sensibles en utilisant les propriétés de classification dans l’Infrastructure de Classification de fichier (FCI) de Windows Server, les propriétés de document dans SharePoint ou les propriétés de document appliquée à un système tiers. Si cela décrit votre organisation, vous pouvez créer une stratégie DLP dans Office 365 qui reconnaît les propriétés qui ont été appliquées à des documents par Windows Server FCI ou un autre système, afin que la stratégie DLP peut être appliquée dans des documents Office avec FCI spécifique ou autre valeurs de propriété.
ms.openlocfilehash: 057cdad981249e39d6f39f231d8d60ab977e717a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "23013688"
---
# <a name="create-a-dlp-policy-to-protect-documents-with-fci-or-other-properties"></a>Création d’une stratégie DLP pour protéger les documents avec l’ICF ou d’autres propriétés

Dans Office 365, vous pouvez utiliser une stratégie de protection contre la perte de données (DLP) pour identifier, surveiller et protéger les informations sensibles. De nombreuses organisations appliquent déjà un processus permettant d’identifier et de classer les informations sensibles à l’aide des propriétés de classification dans l’infrastructure de classification des fichiers (ICF) Windows Server, des propriétés de document dans SharePoint ou des propriétés de document appliquées par un système tiers. Si vous reconnaissez votre organisation, vous pouvez créer une stratégie DLP dans Office 365 qui reconnaît les propriétés qui ont été appliquées aux documents par l’ICF Windows Server ou un autre système, afin que la stratégie DLP puisse être activée sur les documents Office avec une ICF ou d’autres valeurs de propriété spécifiques.
  
![Diagramme illustrant Office 365 et le système de classement externe](media/59ad0ac1-4146-4919-abd1-c74d8508d25e.png)
  
Par exemple, votre organisation peut Windows Server FCI permet d’identifier les documents avec des informations d’identification personnelle (PII) tels que des numéros de sécurité sociale, puis de classer le document en définissant les **Informations d’identification personnelle** propriété **élevé**, **modéré**, **faible**, **Public**ou **Pas PII** en fonction du type et nombre d’occurrences de PII trouvé dans le document. Dans Office 365, vous pouvez créer une stratégie DLP qui identifie les documents associés à cette propriété les valeurs spécifiques, telles que **haute** et **moyenne**, puis exécute une action tels que de blocage de l’accès à ces fichiers. La même stratégie peut avoir une autre règle qui prend une autre action si la propriété est définie sur **Low**, telles que l’envoi d’une notification par courrier électronique. De cette façon, DLP dans Office 365 s’intègre à Windows Server FCI et permet de protéger les documents Office téléchargé ou partagés vers Office 365 à partir des serveurs de fichiers Windows Server.
  
Une stratégie DLP recherche simplement une paire nom/valeur de propriété spécifique. N’importe quelle propriété de document peut être utilisée, tant que la propriété possède une propriété gérée correspondante pour la recherche SharePoint. Par exemple, une collection de sites SharePoint peut utiliser un type de contenu nommé **Relevé de voyage** avec un champ obligatoire nommé **Client**. Lorsqu’une personne crée un relevé de voyage, elle doit entrer le nom du client. Cette paire nom/valeur de propriété peut également être utilisée dans une stratégie DLP, par exemple, si vous voulez une règle qui bloque l’accès au document pour les utilisateurs externes lorsque le champ **Client** contient **Contoso**.
  
Notez que si vous souhaitez appliquer votre stratégie DLP à un contenu avec des étiquettes de Office 365 spécifiques, vous ne devez pas suivre les étapes décrites ici. Au lieu de cela, découvrez comment [utiliser une étiquette comme une condition dans une stratégie DLP](data-loss-prevention-policies.md#using-a-label-as-a-condition-in-a-dlp-policy).
  
## <a name="before-you-create-the-dlp-policy"></a>Avant de créer la stratégie DLP

Avant de pouvoir utiliser une propriété de Windows Server FCI ou autres droits de propriété d’une stratégie DLP, vous devez créer une propriété gérée dans le centre d’administration de SharePoint. Pourquoi ?
  
Exemples
  
C’est important car DLP dans Office 365 utilise le robot de recherche pour identifier et classer les informations sensibles sur vos sites, puis les stocker dans une partie sécurisée de l’index de recherche. Lorsque vous chargez un document vers Office 365, SharePoint crée automatiquement les propriétés analysées basées sur les propriétés du document. En revanche, pour utiliser une ICF ou une autre propriété dans une stratégie DLP, la propriété analysée doit être mappée sur une propriété gérée afin que le contenu avec cette propriété soit conservé dans l’index.
  
Pour plus d’informations sur la recherche et des propriétés gérées, voir [gérer le schéma de recherche dans SharePoint Online](http://go.microsoft.com/fwlink/p/?LinkID=627454).
  
### <a name="step-1-upload-a-document-with-the-needed-property-to-office-365"></a>Étape 1 : chargement d’un document avec la propriété nécessaire vers Office 365

Vous devez d’abord télécharger un document avec la propriété que vous souhaitez référencer dans votre stratégie DLP. Office 365 détecte la propriété et créer automatiquement une propriété analysée à partir de celui-ci. Dans l’étape suivante, vous allez créer une propriété gérée, puis mapper la propriété gérée à cette propriété analysée.
  
### <a name="step-2-create-a-managed-property"></a>Étape 2 : création d’une propriété gérée

1. Connectez-vous au centre d’administration Office 365.
    
2. Dans la navigation de gauche, choisissez **Admin centres** \> **SharePoint**. Vous êtes maintenant dans le centre d’administration de SharePoint.
    
3. Dans la navigation de gauche, choisissez **Rechercher** \> dans la page **administration de la recherche** \> **Gérer un schéma de recherche**.
    
    ![Page d’administration de la recherche dans le Centre d’administration SharePoint](media/6bcd3aec-d11a-4f8c-9987-8f35da14d80b.png)
  
4. Dans la page de **Propriétés gérées** \> **Nouvelle propriété gérée**.
    
    ![Page Propriétés gérées avec le bouton Nouvelle propriété gérée mis en surbrillance](media/b161c764-414c-4037-83ed-503a49fb4410.png)
  
5. Entrez un nom et une description pour la propriété. Ce nom apparaîtra dans vos stratégies DLP.
    
6. Pour **Type**, sélectionnez **Texte**. 
    
7. Sous **Caractéristiques principales**, sélectionnez **Utilisable dans une requête** et **Affichable dans les résultats d’une recherche**.
    
8. Sous **mappages sur les propriétés analysées** \> **Ajouter un mappage**.
    
9. Dans la boîte de dialogue **analysé sélection de propriété** \> recherchez et sélectionnez la propriété analysée qui correspond à la propriété Windows Server FCI ou autres que vous allez utiliser dans votre stratégie DLP \> **OK**.
    
    ![Boîte de dialogue de sélection des propriétés analysées](media/aeda1dce-1342-48bf-9594-a8e4f230e8aa.png)
  
10. En bas de la page \> **OK**.
    
## <a name="create-a-dlp-policy-that-uses-an-fci-property-or-other-property"></a>Création d’une stratégie DLP qui utilise une propriété ICF ou une autre propriété

Dans cet exemple, une organisation utilise FCI sur ses serveurs de fichiers Windows Server ; plus précisément, ils utilisent la propriété de classification FCI nommée des **Informations d’identification personnelle** avec les valeurs possibles de **élevé**, **modéré**, **faible**, **Public**et **Pas PII**. Maintenant qu’ils souhaitent tirer parti de leur classification FCI existante dans leurs stratégies DLP dans Office 365.
  
D’abord, ils suivent les étapes ci-dessus pour créer une propriété gérée dans SharePoint Online, qui est mappée sur la propriété analysée créée automatiquement à partir de la propriété ICF.
  
Ensuite, ils créent une stratégie DLP avec deux règles qui utilisent toutes deux la condition de **Propriétés de Document contiennent une des valeurs suivantes**:
  
- **Contenu FCI PII - élevé, modéré** La première règle restreint l’accès au document si la propriété de classification des **Informations d’identification personnelle** FCI est égale à **haute** ou **modéré** et le document est partagé avec des personnes en dehors de l’organisation. 
    
- **Contenu FCI PII - faible** La deuxième règle envoie une notification au propriétaire du document si la propriété de classification des **Informations d’identification personnelle** FCI est égale à **faible** et le document est partagée avec des personnes en dehors de l’organisation. 
    
### <a name="create-the-dlp-policy-by-using-powershell"></a>Créer la stratégie DLP à l’aide de PowerShell

Notez que la condition de **Propriétés de Document contiennent une de ces valeurs** est temporairement pas disponible dans l’interface utilisateur de la sécurité &amp; centre de conformité, mais vous pouvez toujours utiliser cette condition à l’aide de PowerShell. Vous pouvez utiliser la `New\Set\Get-DlpCompliancePolicy` à utiliser avec une stratégie DLP et à utiliser des applets de commande le `New\Set\Get-DlpComplianceRule` applets de commande avec la `ContentPropertyContainsWords` paramètre pour ajouter la condition de **Propriétés de Document contiennent une de ces valeurs**.
  
Pour plus d’informations sur ces applets de commande, voir [Office 365 sécurité &amp; centre de conformité des applets de commande](http://go.microsoft.com/fwlink/?LinkID=799772&amp;clcid=0x409).
  
1. [Se connecter à l’Office 365 Security &amp; centre de conformité à l’aide de PowerShell à distance](http://go.microsoft.com/fwlink/?LinkID=799771&amp;clcid=0x409)
    
2. Créer la stratégie à l’aide de `New-DlpCompliancePolicy`.
    
    Voici un exemple de PowerShell qui crée une stratégie DLP qui s’applique à tous les emplacements.
    
      ```
      New-DlpCompliancePolicy -Name FCI_PII_policy -ExchangeLocation All -SharePointLocation All -OneDriveLocation All -Mode Enable
      ```

3. Créer les deux règles décrites ci-dessus à l’aide de `New-DlpComplianceRule`, où une règle est la valeur **faible** , et une autre règle est pour les valeurs **élevés** et **modérés** . 
    
    Voici un exemple de PowerShell qui crée ces deux règles. Notez que les paires nom/valeur de propriété sont placé entre guillemets, et un nom de propriété peut spécifier plusieurs valeurs séparées par des virgules sans espaces, comme`"<Property1>:<Value1>,<Value2>","<Property2>:<Value3>,<Value4>"....`
    
      ```
      New-DlpComplianceRule -Name FCI_PII_content-High,Moderate -Policy FCI_PII_policy -AccessScope NotInOrganization -BlockAccess $true -ContentPropertyContainsWords "Personally Identifiable Information:High,Moderate" -Disabled $falseNew-DlpComplianceRule -Name FCI_PII_content-Low -Policy FCI_PII_policy -AccessScope NotInOrganization -BlockAccess $false -ContentPropertyContainsWords "Personally Identifiable Information:Low" -Disabled $false -NotifyUser Owner
      ```

    Notez que Windows Server FCI inclut de nombreuses propriétés intégrées, y compris les **Informations d’identification personnelle** utilisé dans cet exemple. Les valeurs possibles pour chaque propriété peuvent être différents pour chaque organisation. La **élevé**, **modéré**ou **faible** valeurs ici ne sont qu’un exemple. Pour votre organisation, vous pouvez afficher les propriétés de classification de Windows Server FCI avec leurs valeurs possibles dans le Gestionnaire de ressources du serveur de fichier sur le serveur de fichiers basé sur Windows Server. Pour plus d’informations, voir [créer une propriété de classification](http://go.microsoft.com/fwlink/p/?LinkID=627456).
    
Lorsque vous avez terminé, votre stratégie doit avoir deux nouvelles règles qui utilisent toutes deux la condition de **Propriétés de Document contiennent une de ces valeurs** . Notez que cette condition n’apparaître pas dans l’interface utilisateur, mais les autres conditions, les actions et paramètres seront affiche. 
  
Une règle bloque l’accès de contenu où la propriété des **Informations d’identification personnelle** est égale à **haute** ou **modérée**. Une deuxième règle envoie une notification à propos de contenu où la propriété des **Informations d’identification personnelle** est égale à **faible**.
  
![Nouvelle boîte de dialogue de stratégie DLP montrant les deux règles venant d’être créées](media/5c56c13b-62a5-4f25-8eb7-ce83a844bb12.png)
  
## <a name="after-you-create-the-dlp-policy"></a>Après avoir créé la stratégie DLP

Suivre les étapes décrites dans les sections précédentes crée une stratégie DLP détectera rapidement contenu à cette propriété, mais uniquement si ce contenu est téléchargé nouvellement (de sorte que du contenu indexé), ou si de contenu qui est ancien mais seulement modifiée (de sorte que le contenu nouveau indexée) .
  
Pour détecter tout le contenu avec cette propriété, vous voudrez peut-être demander manuellement la réindexation de votre bibliothèque, site ou collection de sites, afin que la stratégie DLP connaisse tout le contenu avec cette propriété. Dans SharePoint Online, le contenu est automatiquement analysé selon une planification d’analyse définie. Le robot récupère le contenu qui a été modifié depuis la dernière analyse et met à jour l’index. Si vous avez besoin que votre stratégie DLP protège le contenu avant la prochaine analyse planifiée, vous pouvez suivre cette procédure.
  
> [!CAUTION]
> Réindexation un site peut entraîner une charge importante sur le système de recherche. Ne pas réindexer votre site, sauf si votre scénario absolument besoin. 
  
Pour plus d’informations, voir [demander manuellement l’analyse et la réindexation d’un site, une bibliothèque ou une liste](http://go.microsoft.com/fwlink/p/?LinkID=627457).
  
### <a name="re-index-a-site-optional"></a>Réindexation d’un site (facultatif)

1. Sur le site, choisissez **paramètres** (icône représentant un engrenage dans le coin supérieur droit) \> **Paramètres du Site**.
    
2. Dans la zone de **recherche**, choisissez **Search et disponibilité hors connexion** \> **réindexer du site**.
    
## <a name="more-information"></a>Plus d'informations

- [Vue d’ensemble des stratégies de protection contre la perte de données](data-loss-prevention-policies.md)
    
- [Création d'une stratégie DLP à partir d'un modèle](create-a-dlp-policy-from-a-template.md)
    
- [Envoi des notifications et affichage des conseils de stratégie pour les stratégies DLP](use-notifications-and-policy-tips.md)
    
- [Ce qu’incluent les modèles de stratégie DLP](what-the-dlp-policy-templates-include.md)
    
- [Inventaire des types d'informations sensibles](what-the-sensitive-information-types-look-for.md)
    

