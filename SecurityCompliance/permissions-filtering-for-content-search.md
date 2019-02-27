---
title: Configuration du filtrage des autorisations pour la recherche de contenu
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 5/14/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 1adffc35-38e5-4f7d-8495-8e0e8721f377
description: Utiliser le filtrage des autorisations de recherche de contenu pour permettre à un gestionnaire eDiscovery de rechercher uniquement un sous-ensemble de boîtes aux lettres et de sites dans votre organisation Office 365.
ms.openlocfilehash: f9f3344fce11e5eacfede43aab593b6235cfe1c7
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296907"
---
# <a name="configure-permissions-filtering-for-content-search"></a>Configuration du filtrage des autorisations pour la recherche de contenu

Vous pouvez utiliser le filtrage des autorisations de recherche pour permettre à un gestionnaire eDiscovery de rechercher uniquement un sous-ensemble de boîtes aux lettres et de sites dans votre organisation Office 365. Vous pouvez également utiliser le filtrage des autorisations pour permettre à ce même gestionnaire eDiscovery de rechercher uniquement le contenu de boîte aux lettres ou de site qui répond à des critères de recherche spécifiques. Par exemple, vous pouvez permettre à un gestionnaire eDiscovery de rechercher uniquement les boîtes aux lettres des utilisateurs d'un emplacement ou d'un service spécifique. Pour ce faire, vous devez créer un filtre qui utilise un filtre de destinataires pris en charge pour limiter les boîtes aux lettres pouvant faire l'objet d'une recherche. Vous pouvez également créer un filtre qui spécifie le contenu de boîte aux lettres pouvant faire l'objet d'une recherche. Pour ce faire, vous devez créer un filtre qui utilise une propriété de message pouvant faire l'objet d'une recherche. De même, vous pouvez permettre à un gestionnaire eDiscovery de rechercher uniquement des sites SharePoint spécifiques dans votre organisation. Pour ce faire, vous devez créer un filtre qui limite le site pouvant faire l'objet d'une recherche. Vous pouvez également créer un filtre qui spécifie le contenu de site pouvant faire l'objet d'une recherche. Pour ce faire, vous devez créer un filtre qui utilise une propriété de site pouvant faire l'objet d'une recherche.

Vous pouvez également utiliser le filtrage des autorisations de recherche pour créer des limites logiques (appelées *limites de conformité*) au sein d'une organisation Office 365 qui contrôlent les emplacements de contenu utilisateur (par exemple, les boîtes aux lettres, les sites SharePoint et les comptes OneDrive) qui des gestionnaires eDiscovery spécifiques peuvent effectuer des recherches. Pour plus d'informations, reportez-vous à [la rubrique Set up Compliance Boundaries for eDiscovery investigations in Office 365](set-up-compliance-boundaries.md).
  
Le filtrage des autorisations de recherche est pris en charge par la fonctionnalité de recherche &amp; de contenu dans le centre de sécurité conformité Office 365. Ces quatre cmdlets vous permettent de configurer et de gérer les filtres de recherche permisisons:
  
[New-ComplianceSecurityFilter](#new-compliancesecurityfilter)

[Get-ComplianceSecurityFilter](#get-compliancesecurityfilter)

[Set-ComplianceSecurityFilter](#set-compliancesecurityfilter)

[Remove-ComplianceSecurityFilter](#remove-compliancesecurityfilter)

## <a name="before-you-begin"></a>Avant de commencer

- Pour exécuter les cmdlets du filtre de sécurité de conformité, vous devez être membre du groupe de rôles gestion de l'organisation &amp; dans le centre de sécurité conformité. Pour plus d'informations, consultez [la rubrique autorisations dans le &amp; Centre de sécurité conformité Office 365](permissions-in-the-security-and-compliance-center.md).
    
- Vous devez connecter Windows PowerShell au centre de sécurité &amp; conformité et à votre organisation Exchange Online pour utiliser les cmdlets de filtrage de sécurité de conformité. Cela est nécessaire, car ces applets de commande nécessitent un accès aux propriétés de boîte aux lettres, ce qui explique pourquoi vous devez vous connecter à Exchange Online. Consultez les étapes de la section suivante. 
    
- Consultez la section [More information](#more-information) pour plus d’informations sur les filtres d’autorisations de recherche. 
    
- Le filtrage des autorisations de recherche s'applique aux boîtes aux lettres inactives, ce qui signifie que vous pouvez utiliser le filtrage du contenu des boîtes aux lettres et des boîtes aux lettres pour limiter la recherche d'une boîte aux lettres inactive. Consultez la section [plus d'informations](#more-information) pour obtenir des informations supplémentaires sur le filtrage des autorisations et les boîtes aux lettres inactives. 
    
-  Le filtrage des autorisations de recherche ne peut pas être utilisé pour limiter les personnes pouvant effectuer des recherches dans des dossiers publics dans Exchange. 
    
- Il n'y a pas de limite au nombre de filtres d'autorisations de recherche pouvant être créés dans une organisation. Toutefois, les performances de recherche seront affectées lorsqu'il y aura plus de 100 filtres d'autorisations de recherche. Pour conserver le plus petit nombre de filtres d'autorisations de recherche dans votre organisation, créez des filtres qui combinent les règles pour Exchange, SharePoint et OneDrive dans un seul filtre chaque fois que cela est possible.
    
## <a name="connect-to-the-security-amp-compliance-center-and-exchange-online-in-a-single-remote-powershell-session"></a>Se connecter au centre &amp; de sécurité conformité et à Exchange Online dans une session PowerShell distante unique

1. Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l'aide d'un suffixe de nom de fichier. ps1. Par exemple, vous pouvez l'enregistrer dans un fichier nommé ConnectEXO-CC. ps1.
    
    ```
    $UserCredential = Get-Credential
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -DisableNameChecking
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -AllowClobber -DisableNameChecking
    $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Exchange Online + Compliance Center)"
    ```

2. Sur votre ordinateur local, ouvrez Windows PowerShell, accédez au dossier dans lequel se trouve le script que vous avez créé à l'étape précédente, puis exécutez le script; par exemple:
    
    ```
    .\ConnectEXO-CC.ps1
    ```
 
Comment savoir si cela a fonctionné? Après avoir exécuté le script, les cmdlets du centre &amp; de sécurité conformité et d'Exchange Online sont importées dans votre session Windows PowerShell locale. Si vous ne recevez aucune erreur, vous vous êtes connecté avec succès. Un test rapide consiste à exécuter une cmdlet &amp; du centre de sécurité conformité (par exemple, **install-UnifiedCompliancePrerequisite** ) et une cmdlet Exchange Online, telle que **Get-Mailbox**. 
  
Si vous recevez des erreurs, vérifiez les conditions requises suivantes :
  
- Un mot de passe incorrect est un problème courant. Exécutez à nouveau les deux étapes et portez une attention particulière au nom d’utilisateur et au mot de passe que vous entrez à l’étape 1.
    
- Vérifiez que votre compte dispose des autorisations nécessaires pour accéder &amp; au centre de sécurité conformité. Pour plus d'informations, consultez [la rubrique accorder aux &amp; utilisateurs l'accès au centre de sécurité conformité](grant-access-to-the-security-and-compliance-center.md).
    
- Pour éviter les attaques par déni de service (DoS), vous êtes limité à trois connexions PowerShell à distance vers le centre de sécurité &amp; conformité.
    
- Windows PowerShell doit être configuré pour l'exécution de scripts. Vous devez configurer ce paramètre une fois seulement sur votre ordinateur, pas à chaque connexion. Pour activer l'exécution de scripts signés dans Windows PowerShell, exécutez la commande suivante dans une fenêtre Windows PowerShell élevée (fenêtre Windows PowerShell ouverte en sélectionnant **Exécuter en tant qu'administrateur**).

    ```
    Set-ExecutionPolicy RemoteSigned
    ```
- Le trafic TCP 80 doit être ouvert entre votre ordinateur local et Office 365. Il est probablement ouvert, mais il est utile de considérer si votre organisation a une stratégie d'accès Internet restrictive.
    

  
## <a name="new-compliancesecurityfilter"></a>New-ComplianceSecurityFilter
<a name="New"> </a>

La **ComplianceSecurityFilter** est utilisée pour créer un filtre d'autorisations de recherche. Le tableau suivant décrit les paramètres de cette cmdlet. Tous les paramètres sont requis pour créer un filtre de sécurité de conformité. 
  
|**Paramètre**|**Description**|
|:-----|:-----|
| _Action_ <br/> | Le paramètre _action_ spécifie le type d'action de recherche auquel le filtre est appliqué. Les actions de recherche de contenu possibles sont les suivantes:<br/><br/> **Export** : le filtre est appliqué lors de l'exportation des résultats de la recherche.  <br/> **Aperçu** : le filtre est appliqué lors de l'aperçu des résultats de la recherche.  <br/> **Purge** : le filtre est appliqué lors de la purge des résultats de la recherche.  <br/> **Recherche** : le filtre est appliqué lors de l'exécution d'une recherche.  <br/> **Tout** : le filtre est appliqué à toutes les actions de recherche.  <br/> |
| _FilterName_ <br/> |Le paramètre _FilterName_ spécifie le nom du filtre d'autorisations. Ce nom est utilisé pour identifier un filtre lorsque vous utilisez les cmdlets **Get-ComplianceSecurityFilter**, **Set-ComplianceSecurityFilter** et **Remove-ComplianceSecurityFilter** .<br/> |
| _Filtres_ <br/> | Le __ paramètre Filters spécifie les critères de recherche pour le filtre de sécurité de conformité. Vous pouvez créer trois types de filtres différents:<br/><br/> **Filtrage des boîtes aux lettres** : ce type de filtre spécifie les boîtes aux lettres que les __ utilisateurs affectés (spécifiés par le paramètre Users) peuvent rechercher. La syntaxe de ce type de filtre est **Mailbox_** _MailboxPropertyName_, où _MailboxPropertyName_ spécifie une propriété de boîte aux lettres utilisée pour étendre les boîtes aux lettres pouvant faire l'objet d'une recherche. Par exemple, le filtre `"Mailbox_CustomAttribute10 -eq 'OttawaUsers'"` de boîte aux lettres permet à l'utilisateur d'affecter ce filtre uniquement à des boîtes aux lettres ayant la valeur «OttawaUsers» dans la propriété CustomAttribute10.<br/>  Toutes les propriétés de destinataire filtrables prises en charge peuvent être utilisées pour la propriété _MailboxPropertyName_ . Pour obtenir la liste des propriétés prises en charge, consultez [la rubrique Filterable Properties for the-RecipientFilter Parameter](https://go.microsoft.com/fwlink/p/?LinkId=784903).<br/><br/> **Filtrage du contenu de la boîte aux lettres** : ce type de filtre est appliqué sur le contenu qui peut être recherché. Il spécifie le contenu de la boîte aux lettres que les utilisateurs affectés peuvent rechercher. La syntaxe de ce type de filtre est **MailboxContent_** _SearchablePropertyName: value_, où _SEARCHABLEPROPERTYNAME_ spécifie une propriété KQL (Keyword Query Language) qui peut être spécifiée dans une recherche de contenu. Par exemple, le filtre `MailboxContent_recipients:contoso.com` de contenu de boîte aux lettres permet à l'utilisateur qui a affecté ce filtre de rechercher uniquement les messages envoyés à des destinataires dans le domaine contoso.com.<br/>  Pour obtenir la liste des propriétés de message pouvant faire l'objet d'une recherche, voir [requêtes de mots clés et conditions de recherche pour la recherche de contenu](keyword-queries-and-search-conditions.md).  <br/><br/> **Filtrage de site et de contenu de site** : il existe deux filtres de site SharePoint et OneDrive entreprise que vous pouvez utiliser pour spécifier le site ou le contenu de site que les utilisateurs affectés peuvent rechercher:  <br/><br/> - **Site_** _SearchableSiteProperty_ <br/> - **SiteContent_** _SearchableSiteProperty_ <br/><br/>  Ces deux filtres sont interchangeables; par exemple `"Site_Path -like 'https://contoso.sharepoint.com/sites/doctors*'"` , `"SiteContent_Path -like 'https://contoso.sharepoint.com/sites/doctors*'"` et renverra les mêmes résultats. Toutefois, pour vous aider à identifier ce que fait un filtre, `Site_` vous pouvez utiliser pour spécifier des propriétés liées au site (telles qu'une `SiteContent_` URL de site) et pour spécifier des propriétés liées au contenu (telles que les types de documents. Par exemple, le filtre `"Site_Path -like 'https://contoso.sharepoint.com/sites/doctors*'"` permet à l'utilisateur qui a affecté ce filtre de rechercher uniquement le contenu https://contoso.sharepoint.com/sites/doctors de la collection de sites. Le filtre `"SiteContent_FileExtension -eq 'docx'"` permet à l'utilisateur qui a affecté ce filtre de rechercher uniquement des documents Word (Word 2007 et versions ultérieures).<br/><br/>  Pour obtenir la liste des propriétés de site pouvant faire l'objet d'une recherche, voir [vue d'ensemble des propriétés analysées et gérées dans SharePoint](https://go.microsoft.com/fwlink/p/?LinkId=331599). Les propriétés marquées d'un **Oui** dans la colonne * * Queryable * * peuvent être utilisées pour créer un filtre de site ou de contenu de site.<br/> <br/> **Important:**  Un filtre de recherche unique ne peut avoir qu'un seul type de filtre; il ne peut pas contenir un filtre de boîte aux lettres et un filtre de site; de même, il ne peut pas contenir un filtre de boîte aux lettres et un filtre de contenu de boîte aux lettres. Toutefois, un filtre peut contenir une requête plus complexe du même type. Par exemple,`"Mailbox_CustomAttribute10 -eq 'FTE' -and Mailbox_MemberOfGroup -eq '$($DG.DistinguishedName)'"` <br/><br/> **Important:** Vous devez créer un filtre d'autorisations de recherche pour empêcher explicitement les utilisateurs de rechercher des emplacements de contenu dans un service Office 365 spécifique (par exemple, empêcher un utilisateur de rechercher une boîte aux lettres Exchange ou n'importe quel site SharePoint). En d'autres termes, la création d'un filtre d'autorisations de recherche qui permet à un utilisateur de rechercher tous les sites SharePoint dans l'organisation n'empêche pas cet utilisateur de rechercher des boîtes aux lettres. Par exemple, pour permettre aux administrateurs SharePoint de rechercher uniquement des sites SharePoint, vous devez créer un filtre qui les empêche de rechercher des boîtes aux lettres. De même, pour permettre aux administrateurs Exchange de rechercher uniquement les boîtes aux lettres, vous devez créer un filtre qui les empêche de rechercher des sites.           |
| _Utilisateurs_ <br/> |Le __ paramètre Users spécifie les utilisateurs qui reçoivent ce filtre appliqué à leurs recherches de contenu. Identifiez les utilisateurs en fonction de leur alias ou de leur adresse SMTP principale. Vous pouvez spécifier plusieurs valeurs séparées par des virgules, ou vous pouvez attribuer le filtre à tous les utilisateurs à l'aide de la valeur **All**.<br/> Vous pouvez également utiliser le __ paramètre Users pour spécifier un &amp; groupe de rôles du centre de sécurité conformité. Cela vous permet de créer un groupe de rôles personnalisé, puis d'affecter ce groupe de rôles à un filtre d'autorisations de recherche. Par exemple, imaginons que vous disposez d'un groupe de rôles personnalisé pour les responsables eDiscovery pour la filiale américaine d'une entreprise multinationale. Vous pouvez utiliser le __ paramètre Users pour spécifier ce groupe de rôles (à l'aide de la propriété Name du groupe de rôles), puis utiliser le paramètre _Filter_ pour autoriser la recherche uniquement dans les boîtes aux lettres des États-Unis.<br/> Vous ne pouvez pas spécifier de groupes de distribution avec ce paramètre.  <br/> |
   

## <a name="examples-of-creating-search-permissions-filters"></a>Exemples de création de filtres d'autorisations de recherche

Voici quelques exemples d’utilisation de la cmdlet **New-ComplianceSecurityFilter** pour créer un filtre d’autorisations de recherche. 
  
Cet exemple montre comment autoriser l'utilisateur annb@contoso.com à effectuer toutes les actions de recherche de contenu uniquement pour les boîtes aux lettres au Canada. Ce filtre contient le code pays numérique à trois chiffres pour le Canada à partir de l'ISO 3166-1.

```
New-ComplianceSecurityFilter -FilterName CountryFilter  -Users annb@contoso.com -Filters "Mailbox_CountryCode  -eq '124'" -Action All
```

Cet exemple permet aux utilisateurs donh et suzanf de rechercher uniquement les boîtes aux lettres possédant la valeur « Marketing » pour la propriété de boîte aux lettres CustomAttribute1.

```
New-ComplianceSecurityFilter -FilterName MarketingFilter  -Users donh,suzanf -Filters "Mailbox_CustomAttribute1  -eq 'Marketing'" -Action Search
```
   
Cet exemple permet aux membres du groupe de rôles « US Discovery Managers » d’effectuer toutes les actions de recherche de contenu uniquement sur les boîtes aux lettres aux États-Unis. Ce filtre contient le code pays numérique à trois chiffres pour les États-Unis selon la norme ISO 3166-1.
  
```
New-ComplianceSecurityFilter -FilterName USDiscoveryManagers  -Users "US Discovery Managers" -Filters "Mailbox_CountryCode  -eq '840'" -Action All
```

Cet exemple permet aux membres du groupe de rôles de gestionnaire de découverte électronique de rechercher uniquement les boîtes aux lettres des membres du groupe de distribution Ottawa Users. 
  
```
$DG = Get-DistributionGroup "Ottawa Users"
```

```
New-ComplianceSecurityFilter -FilterName DGFilter  -Users eDiscoveryManager -Filters "Mailbox_MemberOfGroup -eq '$($DG.DistinguishedName)'" -Action Search
```
Cet exemple empêche tout utilisateur de supprimer le contenu des boîtes aux lettres des membres du groupe de distribution Executive Team.

```
$DG = Get-DistributionGroup "Executive Team"
```

```
New-ComplianceSecurityFilter -FilterName NoExecutivesPreview  -Users all -Filters "Mailbox_MemberOfGroup -ne '$($DG.DistinguishedName)'" -Action Purge
```
   
Cet exemple permet aux membres du groupe de rôles personnalisé OneDrive eDiscovery managers de rechercher uniquement du contenu dans OneDrive entreprise au sein de l'organisation.

```
New-ComplianceSecurityFilter -FilterName OneDriveOnly  -Users "OneDrive eDiscovery Managers" -Filters "Site_Path -like 'https://contoso-my.sharepoint.com/personal*'" -Action Search
```
   
> [!NOTE]
> Pour restreindre les utilisateurs à la recherche de sites spécifiques, `Site_Path`utilisez le filtre, comme indiqué dans l'exemple précédent. L' `Site_Site` utilisation de ne fonctionnera pas. 
  
Cet exemple limite l’utilisateur à l’exécution de toutes les actions de recherche de contenu uniquement sur les messages électroniques envoyés au cours de l’année 2015.

```
New-ComplianceSecurityFilter -FilterName EmailDateRestrictionFilter -Users donh@contoso.com -Filters "MailboxContent_Received -ge '01-01-2015' -and MailboxContent_Received -le '12-31-2015'" -Action All
```
   
Comme l’exemple précédent, cet exemple limite l’utilisateur à l’exécution de toutes les actions de recherche de contenu sur les documents modifiés au cours de l’année 2015.

```
New-ComplianceSecurityFilter -FilterName DocumentDateRestrictionFilter -Users donh@contoso.com -Filters "SiteContent_LastModifiedTime -ge '01-01-2015' -and SiteContent_LastModifiedTime -le '12-31-2015'" -Action All
```
   
Cet exemple empêche les membres du groupe de rôles «les gestionnaires de découverte OneDrive» d'effectuer des actions de recherche de contenu sur n'importe quelle boîte aux lettres de l'organisation. 

```
New-ComplianceSecurityFilter -FilterName NoEXO -Users "OneDrive Discovery Managers" -Filters "Mailbox_Alias -notlike '*'"  -Action All
```
  
## <a name="get-compliancesecurityfilter"></a>Get-ComplianceSecurityFilter

La **ComplianceSecurityFilter** est utilisée pour renvoyer une liste de filtres d'autorisations de recherche. Utilisez le paramètre _FilterName_ pour renvoyer des informations pour un filtre de recherche spécifique. 
  
## <a name="set-compliancesecurityfilter"></a>Set-ComplianceSecurityFilter

**Set-ComplianceSecurityFilter** est utilisé pour modifier un filtre d'autorisations de recherche existant. Le seul paramètre obligatoire est _FilterName_. 
  
|**Paramètre**|**Description**|
|:-----|:-----|
| _Action_| Le paramètre _action_ spécifie le type d'action de recherche auquel le filtre est appliqué. Les actions de recherche de contenu possibles sont les suivantes:<br/><br/> **Export** : le filtre est appliqué lors de l'exportation des résultats de la recherche.  <br/> **Aperçu** : le filtre est appliqué lors de l'aperçu des résultats de la recherche.  <br/> **Purge** : le filtre est appliqué lors de la purge des résultats de la recherche.  <br/> **Recherche** : le filtre est appliqué lors de l'exécution d'une recherche.  <br/> **Tout** : le filtre est appliqué à toutes les actions de recherche.  <br/> |
| _FilterName_|Le paramètre _FilterName_ spécifie le nom du filtre d'autorisations. |
| _Filtres_| Le __ paramètre Filters spécifie les critères de recherche pour le filtre de sécurité de conformité. Vous pouvez créer deux types de filtres différents:<br/><br/>**Filtrage des boîtes aux lettres** : ce type de filtre spécifie les boîtes aux lettres que les __ utilisateurs affectés (spécifiés par le paramètre Users) peuvent rechercher. La syntaxe de ce type de filtre est **Mailbox_** _MailboxPropertyName_, où _MailboxPropertyName_ spécifie une propriété de boîte aux lettres utilisée pour étendre les boîtes aux lettres pouvant faire l'objet d'une recherche. Par exemple, le filtre `"Mailbox_CustomAttribute10 -eq 'OttawaUsers'"` de boîte aux lettres permet à l'utilisateur d'affecter ce filtre uniquement à des boîtes aux lettres ayant la valeur «OttawaUsers» dans la propriété CustomAttribute10.  Toutes les propriétés de destinataire filtrables prises en charge peuvent être utilisées pour la propriété _MailboxPropertyName_ . Pour obtenir la liste des propriétés prises en charge, consultez [la rubrique Filterable Properties for the-RecipientFilter Parameter](https://go.microsoft.com/fwlink/p/?LinkId=784903).<br/><br/>**Filtrage du contenu de la boîte aux lettres**: ce type de filtre est appliqué sur le contenu qui peut être recherché. Il spécifie le contenu de la boîte aux lettres que les utilisateurs affectés peuvent rechercher. La syntaxe de ce type de filtre est **MailboxContent_** _SearchablePropertyName: value_, où _SEARCHABLEPROPERTYNAME_ spécifie une propriété KQL (Keyword Query Language) qui peut être spécifiée dans une recherche de contenu. Par exemple, le filtre `MailboxContent_recipients:contoso.com` de contenu de boîte aux lettres permet à l'utilisateur qui a affecté ce filtre de rechercher uniquement les messages envoyés à des destinataires dans le domaine contoso.com.  Pour obtenir la liste des propriétés de message pouvant faire l'objet d'une recherche, voir [Keyword Queries for Content Search](keyword-queries-and-search-conditions.md).<br/><br/>**Filtrage de site et de contenu de site** Il existe deux filtres de site SharePoint et OneDrive entreprise que vous pouvez utiliser pour spécifier le site ou le contenu de site que les utilisateurs affectés peuvent rechercher: <br/><br/>- **Site_** *SearchableSiteProperty* <br/>- **SiteContent**_*SearchableSiteProperty*<br/><br/>Ces deux filtres sont interchangeables; par exemple `"Site_Path -like 'https://contoso.spoppe.com/sites/doctors*'"` , `"SiteContent_Path -like 'https://contoso.spoppe.com/sites/doctors*'"` et renverra les mêmes résultats. Toutefois, pour vous aider à identifier ce que fait un filtre, `Site_` vous pouvez utiliser pour spécifier des propriétés liées au site (telles qu'une `SiteContent_` URL de site) et pour spécifier des propriétés liées au contenu (telles que les types de documents. Par exemple, le filtre `"Site_Path -like 'https://contoso.spoppe.com/sites/doctors*'"` permet à l'utilisateur qui a affecté ce filtre de rechercher uniquement le contenu https://contoso.spoppe.com/sites/doctors de la collection de sites. Le filtre `"SiteContent_FileExtension -eq 'docx'"` permet à l'utilisateur qui a affecté ce filtre de rechercher uniquement des documents Word (Word 2007 et versions ultérieures).<br/><br/>Pour obtenir la liste des propriétés de site pouvant faire l'objet d'une recherche, voir [vue d'ensemble des propriétés analysées et gérées dans SharePoint](https://go.microsoft.com/fwlink/p/?LinkId=331599). Les propriétés marquées par **Oui** dans la colonne **Queryable** peuvent être utilisées pour créer un filtre de site ou de contenu de site.<br/><br/> **Important:** Un filtre de recherche unique ne peut avoir qu'un seul type de filtre; il ne peut pas contenir un filtre de boîte aux lettres et un filtre de site; de même, il ne peut pas contenir un filtre de boîte aux lettres et un filtre de contenu de boîte aux lettres. Toutefois, un filtre peut contenir une requête plus complexe du même type. Par exemple,`"Mailbox_CustomAttribute10 -eq 'FTE' -and Mailbox_MemberOfGroup -eq '$($DG.DistinguishedName)'"`          |
| _Utilisateurs_|Le __ paramètre Users spécifie les utilisateurs qui reçoivent ce filtre appliqué à leurs recherches de contenu. Étant donné qu'il s'agit d'une propriété à valeurs multiples, la spécification d'un utilisateur ou d'un groupe d'utilisateurs à l'aide de ce paramètre remplacera la liste d'utilisateurs existante. Consultez les exemples suivants pour la syntaxe permettant d'ajouter et de supprimer des utilisateurs sélectionnés.<br/><br/>Vous pouvez également utiliser le __ paramètre Users pour spécifier un &amp; groupe de rôles du centre de sécurité conformité. Cela vous permet de créer un groupe de rôles personnalisé, puis d'affecter ce groupe de rôles à un filtre d'autorisations de recherche. Par exemple, imaginons que vous disposez d'un groupe de rôles personnalisé pour les responsables eDiscovery pour la filiale américaine d'une entreprise multinationale. Vous pouvez utiliser le __ paramètre Users pour spécifier ce groupe de rôles (à l'aide de la propriété Name du groupe de rôles), puis utiliser le paramètre _Filter_ pour autoriser la recherche uniquement dans les boîtes aux lettres des États-Unis.<br/><br/>Vous ne pouvez pas spécifier de groupes de distribution avec ce paramètre. |

## <a name="examples-of-changing-search-permissions-filters"></a>Exemples de modification des filtres d'autorisations de recherche

Ces exemples montrent comment utiliser les cmdlets **Get-ComplianceSecurityFilter** et **Set-ComplianceSecurityFilter** pour ajouter ou supprimer un utilisateur dans la liste existante des utilisateurs auxquels le filtre est affecté. Lorsque vous ajoutez ou supprimez des utilisateurs d'un filtre, spécifiez l'utilisateur à l'aide de son adresse SMTP. 
  
Cet exemple ajoute un utilisateur au filtre.

```
$filterusers = Get-ComplianceSecurityFilter -FilterName OttawaUsersFilter
```
```
$filterusers.users.add("pilarp@contoso.com")
```

```
Set-ComplianceSecurityFilter -FilterName OttawaUsersFilter -Users $filterusers.users
```
   
Cet exemple supprime un utilisateur du filtre.

```
$filterusers = Get-ComplianceSecurityFilter -FilterName OttawaUsersFilter
```

```
$filterusers.users.remove("annb@contoso.com")
```

```
Set-ComplianceSecurityFilter -FilterName OttawaUsersFilter -Users $filterusers.users
```
  
## <a name="remove-compliancesecurityfilter"></a>Remove-ComplianceSecurityFilter

La méthode **Remove-ComplianceSecurityFilter** est utilisée pour supprimer un filtre de recherche. Utilisez le paramètre _FilterName_ pour spécifier le filtre à supprimer. 
  
## <a name="more-information"></a>Plus d’informations

- **Comment fonctionne le filtrage des autorisations de recherche?** Le filtre d'autorisations est ajouté à la requête de recherche lors de l'exécution d'une recherche de contenu. Le filtre d'autorisations est essentiellement joint à la requête de recherche par l'opérateur booléen **and** . Par exemple, supposons que vous disposez d'un filtre d'autorisations qui permet à Bob d'effectuer toutes les actions de recherche sur les boîtes aux lettres des membres du groupe de distribution travailleurs. Bob exécute ensuite une recherche de contenu sur toutes les boîtes aux lettres de l'organisation à `sender:jerry@adatum.com`l'aide de la requête de recherche. Étant donné que le filtre des autorisations et la requête de recherche sont combinés de manière logique par un opérateur **and** , la recherche renverra tous les messages envoyés par Jerry@adatum.com à un membre du groupe de distribution travailleurs. 
    
- **Que se passe-t-il si vous avez plusieurs filtres d'autorisations de recherche?** Dans une requête de recherche de contenu, plusieurs filtres d'autorisations sont combinés par **ou** par des opérateurs booléens. Par conséquent, les résultats seront renvoyés si l'un des filtres est true. Dans une recherche de contenu, tous les filtres (combinés par **ou** opérateurs) sont ensuite associés à la requête de recherche par l'opérateur **and** . Prenons l'exemple précédent, dans lequel un filtre de recherche permet à Bob de rechercher uniquement les boîtes aux lettres des membres du groupe de distribution travailleurs. Nous créons ensuite un autre filtre qui empêche Bob de rechercher la boîte aux lettres de Phil ("Mailbox_Alias-ne'Phil'"). Supposons également que Phil est membre du groupe travailleurs. Lorsque Bob exécute une recherche de contenu (à partir de l'exemple précédent) sur toutes les boîtes aux lettres de l'organisation, les résultats de la recherche sont renvoyés pour la boîte aux lettres de Phil même si vous avez appliqué le filtre pour empêcher Bob de rechercher la boîte aux lettres de Phil. Cela est dû au fait que le premier filtre, qui permet à Bob d'effectuer une recherche dans le groupe travailleurs, a la valeur true. Étant donné que Phil est membre du groupe travailleurs, Bob peut effectuer une recherche dans la boîte aux lettres de Phil. 
    
- Le **filtrage des autorisations de recherche pour les boîtes aux lettres inactives est-il activé?** Oui, vous pouvez utiliser des filtres de contenu de boîte aux lettres et de boîte aux lettres pour limiter les personnes pouvant Rechercher des boîtes aux lettres inactives dans votre organisation. À l'inStar d'une boîte aux lettres ordinaire, une boîte aux lettres inactive doit être configurée avec la propriété Recipient qui permet de créer un filtre d'autorisations. Si nécessaire, vous pouvez utiliser la commande **Get-Mailbox-InactiveMailboxOnly** pour afficher les propriétés des boîtes aux lettres inactives. Pour plus d'informations, consultez la rubrique [créer et gérer des boîtes aux lettres inactives dans Office 365](create-and-manage-inactive-mailboxes.md).
    
- Le **filtrage des autorisations de recherche pour les dossiers publics est-il possible?** Nbre. Comme expliqué précédemment, le filtrage des autorisations de recherche ne peut pas être utilisé pour limiter les personnes pouvant effectuer des recherches dans des dossiers publics dans Exchange. Par exemple, les éléments des emplacements de dossier public ne peuvent pas être exclus des résultats de la recherche par un filtre des autorisations. 
    
- **La possibilité pour un utilisateur de rechercher tous les emplacements de contenu d'un service spécifique les empêche-t-il de rechercher des emplacements de contenu dans un autre service?** Nbre. Comme expliqué précédemment, vous devez créer un filtre d'autorisations de recherche pour empêcher explicitement les utilisateurs de rechercher des emplacements de contenu dans un service Office 365 spécifique (par exemple, empêcher un utilisateur de rechercher une boîte aux lettres Exchange ou n'importe quel site SharePoint). En d'autres termes, la création d'un filtre d'autorisations de recherche qui permet à un utilisateur de rechercher tous les sites SharePoint dans l'organisation n'empêche pas cet utilisateur de rechercher des boîtes aux lettres. Par exemple, pour permettre aux administrateurs SharePoint de rechercher uniquement des sites SharePoint, vous devez créer un filtre qui les empêche de rechercher des boîtes aux lettres. De même, pour permettre aux administrateurs Exchange de rechercher uniquement les boîtes aux lettres, vous devez créer un filtre qui les empêche de rechercher des sites.
