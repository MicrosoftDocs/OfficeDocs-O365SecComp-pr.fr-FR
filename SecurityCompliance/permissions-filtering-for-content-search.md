---
title: Configuration du filtrage des autorisations pour la recherche de contenu
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 5/14/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 1adffc35-38e5-4f7d-8495-8e0e8721f377
description: Utiliser des autorisations de recherche de contenu de filtrage pour laisser un gestionnaire de découverte électronique uniquement un sous-ensemble des boîtes aux lettres et des sites de recherche dans votre organisation Office 365.
ms.openlocfilehash: 2b6968a097e7abe5943a84b9ceb9b6d126057cc2
ms.sourcegitcommit: c166964fe14eec69139a2d3d9c10d2c40ab33f91
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/28/2018
ms.locfileid: "23258622"
---
# <a name="configure-permissions-filtering-for-content-search"></a>Configuration du filtrage des autorisations pour la recherche de contenu

Vous pouvez utiliser des autorisations de recherche de filtrage pour laisser un gestionnaire de découverte électronique uniquement un sous-ensemble des boîtes aux lettres et des sites de recherche dans votre organisation Office 365. Vous pouvez également utiliser le filtrage afin de laisser cette même responsable de la découverte électronique de recherche de contenu de site ou de la boîte aux lettres qui répond aux critères de recherche spécifiques uniquement des autorisations. Par exemple, vous pouvez leur permettre un gestionnaire de découverte électronique dans un emplacement spécifique ou un service de recherche uniquement les boîtes aux lettres d’utilisateurs. Pour cela, en créant un filtre qui utilise un filtre de destinataire pris en charge pour limiter les boîtes aux lettres pouvant être recherchées. Vous pouvez également créer un filtre qui spécifie le contenu de la boîte aux lettres pouvant être recherché. Cela s’effectue en créant un filtre qui utilise une propriété disponible pour la recherche de messages. De même, vous pouvez leur permettre un gestionnaire de découverte électronique uniquement rechercher des sites SharePoint spécifiques dans votre organisation. Pour cela, en créant un filtre qui limite les sites peuvent être recherchés. Vous pouvez également créer un filtre qui spécifie le contenu de site pouvant être recherché. Cela s’effectue en créant un filtre qui utilise une propriété disponible pour la recherche de site.

Vous pouvez également utiliser le filtrage afin de créer des limites logiques (appelés *des limites de conformité*) au sein d’une organisation Office 365 qui contrôlent les emplacements de contenu utilisateur (telles que les boîtes aux lettres, les sites SharePoint et comptes OneDrive) des autorisations de recherche qui gestionnaires de découverte électronique spécifique peuvent rechercher. Pour plus d’informations, voir [définir des limites de conformité pour les enquêtes eDiscovery dans Office 365](set-up-compliance-boundaries.md).
  
Autorisations de recherche le filtrage est pris en charge par la fonctionnalité de recherche de contenu de sécurité Office 365 &amp; centre de conformité. Ces quatre cmdlets vous permettent de configurer et gérer des filtres de recherche permisisons :
  
[Nouvelle ComplianceSecurityFilter](#new-compliancesecurityfilter)

[Get-ComplianceSecurityFilter](#get-compliancesecurityfilter)

[Set-ComplianceSecurityFilter](#set-compliancesecurityfilter)

[Remove-ComplianceSecurityFilter](#remove-compliancesecurityfilter)

## <a name="before-you-begin"></a>Avant de commencer

- Pour exécuter les cmdlets de filtre de sécurité de conformité, vous devez être membre du groupe de rôles de gestion de l’organisation de la sécurité &amp; centre de conformité. Pour plus d’informations, voir [des autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md).
    
- Vous devez vous connecter Windows PowerShell pour la sécurité &amp; centre de conformité et à votre organisation Exchange Online à utiliser les cmdlets de filtre de sécurité de la conformité. Cela est nécessaire car ces applets de commande ont besoin d’accéder aux propriétés de boîte aux lettres, c’est pourquoi vous devez vous connecter à Exchange Online. Voir les étapes décrites dans la section suivante. 
    
- Consultez la section [More information](#more-information) pour plus d’informations sur les filtres d’autorisations de recherche. 
    
- Autorisations de recherche de filtrage s’applique aux boîtes aux lettres inactives, ce qui signifie que vous pouvez utiliser la boîte aux lettres et filtrage pour limiter les utilisateurs permettre rechercher une boîte aux lettres inactive du contenu de boîte aux lettres. Voir la section [plus d’informations](#more-information) pour plus d’informations sur les autorisations de filtrage et de boîtes aux lettres inactives. 
    
-  Filtrage des autorisations de recherche ne peut pas être utilisées pour limiter qui peut rechercher des dossiers publics dans Exchange. 
    
- Il n’existe aucune limite au nombre de filtres des autorisations de recherche qui peuvent être créés dans une organisation. Toutefois, les performances de recherche seront affectées quand il y a plus de 100 filtres d’autorisations de recherche. Pour conserver le nombre de filtres d’autorisations de recherche dans votre organisation plus petit possible, créer des filtres qui associent des règles pour Exchange, SharePoint et OneDrive dans un seul filtre la mesure du possible.
    
## <a name="connect-to-the-security-amp-compliance-center-and-exchange-online-in-a-single-remote-powershell-session"></a>Se connecter à la sécurité &amp; centre de conformité et Exchange Online dans une seule session PowerShell distante

1. Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l’aide d’un suffixe de nom de fichier de .ps1. Par exemple, vous pourriez l’enregistrer dans un fichier nommé ConnectEXO-CC.ps1.
    
    ```
    $UserCredential = Get-Credential
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -DisableNameChecking
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -AllowClobber -DisableNameChecking
    $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Exchange Online + Compliance Center)"
    ```

2. Sur votre ordinateur local, ouvrez Windows PowerShell, accédez au dossier où se trouve le script que vous avez créé à l’étape précédente, puis exécutez le script ; par exemple :
    
    ```
    .\ConnectEXO-CC.ps1
    ```
 
Comment savoir si cela a fonctionné ? Après avoir exécuté le script, les applets de commande de la sécurité &amp; centre de conformité et Exchange Online sont importés dans votre session Windows PowerShell locale. Si vous ne recevez des erreurs, vous connecté avec succès. Un test rapide consiste à exécuter une sécurité &amp; centre de conformité cmdlet — par exemple, **Install-UnifiedCompliancePrerequisite** et une applet de commande Exchange Online, telles que **Get-Mailbox**. 
  
Si vous recevez des erreurs, vérifiez les conditions requises suivantes :
  
- Un mot de passe incorrect est un problème courant. Exécutez à nouveau les deux étapes et portez une attention particulière au nom d’utilisateur et au mot de passe que vous entrez à l’étape 1.
    
- Vérifiez que votre compte est autorisé à accéder à la sécurité &amp; centre de conformité. Pour plus d’informations, voir [donner aux utilisateurs l’accès à la sécurité &amp; centre de conformité](grant-access-to-the-security-and-compliance-center.md).
    
- Pour éviter les attaques par déni de service (DoS), vous êtes limité à trois connexions PowerShell à distance ouvertes à la sécurité &amp; centre de conformité.
    
- Windows PowerShell doit être configuré pour l'exécution de scripts. Vous devez configurer ce paramètre une fois seulement sur votre ordinateur, pas à chaque connexion. Pour activer l'exécution de scripts signés dans Windows PowerShell, exécutez la commande suivante dans une fenêtre Windows PowerShell élevée (fenêtre Windows PowerShell ouverte en sélectionnant **Exécuter en tant qu'administrateur**).

    ```
    Set-ExecutionPolicy RemoteSigned
    ```
- Le trafic TCP port 80 doit être ouvert entre votre ordinateur local et d’Office 365. Il n’est probablement ouvert, mais il s’agit d’un élément à prendre en compte si votre organisation possède une stratégie d’accès Internet restrictive.
    

  
## <a name="new-compliancesecurityfilter"></a>Nouvelle ComplianceSecurityFilter
<a name="New"> </a>

Le **Nouveau-ComplianceSecurityFilter** est utilisée pour créer un nouveau filtre d’autorisations de recherche. Le tableau suivant décrit les paramètres de cette applet de commande. Tous les paramètres sont nécessaires pour créer un filtre de sécurité de la conformité. 
  
|**Paramètre**|**Description**|
|:-----|:-----|
| _Action_ <br/> | Le paramètre _Action_ spécifie ce type d’action de recherche le filtre est appliqué à. Les actions de recherche de contenu possibles sont les suivants :<br/><br/> **Exporter** - le filtre est appliqué lors de l’exportation des résultats de la recherche.  <br/> **Aperçu** - le filtre est appliqué lors de l’aperçu des résultats de la recherche.  <br/> **Vider** - le filtre est appliqué lors de la purge des résultats de la recherche.  <br/> **Recherche** - le filtre est appliqué lors de l’exécution d’une recherche.  <br/> **Tous les** - le filtre est appliqué à toutes les actions de recherche.  <br/> |
| _FilterName_ <br/> |Le paramètre _FilterName_ Spécifie le nom du filtre d’autorisations. Ce nom est utilisé pour identifier un filtre lorsque vous utilisez les applets de commande **Get-ComplianceSecurityFilter**, **Set-ComplianceSecurityFilter** et **Remove-ComplianceSecurityFilter** .<br/> |
| _Filtres_ <br/> | Le paramètre de _filtre_ spécifie les critères de recherche pour le filtre de sécurité de la conformité. Vous pouvez créer trois différents types de filtres :<br/><br/> **Filtrage de boîte aux lettres** - ce type de filtre spécifie les boîtes aux lettres de l’utilisateur affecté (spécifié par le paramètre _utilisateur_ ) peut rechercher. La syntaxe de ce type de filtre est **Mailbox_** _MailboxPropertyName_, où _MailboxPropertyName_ spécifie une propriété de la boîte aux lettres utilisée pour les boîtes aux lettres qui peuvent être recherchés d’étendue. Par exemple, le filtre de boîte aux lettres `"Mailbox_CustomAttribute10 -eq 'OttawaUsers'"` permettrait affecté à l’utilisateur ce filtre pour qu’il recherche les boîtes aux lettres qui ont la valeur « OttawaUsers » dans la propriété CustomAttribute10.<br/>  N’importe quelle propriété de destinataire filtrable pris en charge peut être utilisée pour la propriété _MailboxPropertyName_ . Pour obtenir la liste des propriétés prises en charge, voir [propriétés filtrables pour le paramètre - RecipientFilter](https://go.microsoft.com/fwlink/p/?LinkId=784903).<br/><br/> **Filtrage de contenu de la boîte aux lettres** - ce type de filtre est appliqué sur le contenu qui peut être recherché. Il spécifie le contenu de la boîte aux lettres que peut rechercher l’utilisateur affecté. La syntaxe de ce type de filtre est **MailboxContent_** _SearchablePropertyName:value_, où _SearchablePropertyName_ spécifie une propriété de langage de requête de mot clé (KQL) qui peut être spécifiée dans une recherche de contenu. Par exemple, le filtre de contenu de boîte aux lettres `MailboxContent_recipients:contoso.com` permet à l’utilisateur affecté ce filtre pour qu’il recherche pour les messages envoyés aux destinataires dans le domaine contoso.com.<br/>  Pour obtenir la liste des propriétés de message utilisables dans une requête, voir [conditions de recherche pour la recherche de contenu et les requêtes de mot clé](keyword-queries-and-search-conditions.md).  <br/><br/> **Filtrage de site et contenu de site** : il existe deux SharePoint et OneDrive pour les filtres Business liés au site que vous pouvez utiliser pour spécifier le site ou le contenu de site les utilisateurs peuvent effectuer des recherches :  <br/><br/> - **Site_** _SearchableSiteProperty_ <br/> - **SiteContent_** _SearchableSiteProperty_ <br/><br/>  Ces deux filtres sont interchangeables ; par exemple `"Site_Path -like 'https://contoso.sharepoint.com/sites/doctors*'"` et `"SiteContent_Path -like 'https://contoso.sharepoint.com/sites/doctors*'"` retournera les mêmes résultats. Mais pour vous aider à identifier ce que fait un filtre, vous pouvez utiliser `Site_` pour spécifier les propriétés liées au site (par exemple une URL de site) et `SiteContent_` pour spécifier les propriétés liées au contenu (par exemple, les types de document. Par exemple, le filtre `"Site_Path -like 'https://contoso.sharepoint.com/sites/doctors*'"` permet à l’utilisateur affecté ce filtre pour qu’il recherche du contenu dans le https://contoso.sharepoint.com/sites/doctors collection de sites. Le filtre `"SiteContent_FileExtension -eq 'docx'"` permet à l’utilisateur affecté ce filtre pour qu’il recherche pour les documents Word (Word 2007 et versions ultérieur).<br/><br/>  Pour obtenir la liste des propriétés du site de recherche, voir [vue d’ensemble des propriétés analysées et gérées dans SharePoint](https://go.microsoft.com/fwlink/p/?LinkId=331599). Les propriétés marquées avec un **Oui** dans la ** Queryable ** colonne peut être utilisée pour créer un site ou un filtrage de contenu de site.<br/> <br/> **Important :**  Un filtre de recherche unique peut comporter un type de filtre ; Il ne peut pas contenir un filtre de boîte aux lettres et un filtre de site ; de même, il ne peut pas contenir un filtre de boîte aux lettres et un filtre de contenu de boîte aux lettres. Toutefois, un filtre peut contenir une requête plus complexe du même type. Par exemple,`"Mailbox_CustomAttribute10 -eq 'FTE' -and Mailbox_MemberOfGroup -eq '$($DG.DistinguishedName)'"` <br/><br/> **Important :** Vous devez créer un filtre d’autorisations de recherche pour empêcher explicitement les utilisateurs de rechercher des emplacements de contenu dans un service Office 365 spécifique (par exemple, afin d’empêcher un utilisateur de rechercher une boîte aux lettres Exchange ou un site SharePoint). En d’autres termes, création d’un filtre d’autorisations de recherche qui permet à un utilisateur de rechercher tous les sites SharePoint dans l’organisation n’empêche que l’utilisateur de rechercher les boîtes aux lettres. Par exemple, pour autoriser les administrateurs SharePoint pour qu’il recherche les sites SharePoint, vous devez créer un filtre qui les empêche de rechercher les boîtes aux lettres. De même, pour permettre aux administrateurs Exchange pour qu’il recherche les boîtes aux lettres, vous devez créer un filtre qui empêche les sites de recherche.           |
| _Utilisateurs_ <br/> |Le paramètre _utilisateurs_ spécifie les utilisateurs qui reçoivent ce filtre appliqué à leurs recherches de contenu. Identifier les utilisateurs par leurs alias ou l’adresse SMTP principale. Vous pouvez spécifier plusieurs valeurs séparées par des virgules, ou vous pouvez affecter le filtre à tous les utilisateurs à l’aide de la valeur **All**.<br/> Vous pouvez également utiliser le paramètre _utilisateurs_ pour spécifier une sécurité &amp; groupe de rôles de centre de conformité. Filtre recherche les autorisations de groupe permet d’affecter ce rôle et créer un groupe de rôles personnalisés. Par exemple, supposons que vous avez un groupe de rôles personnalisés pour les responsables de découverte électronique pour la filiale US d’une entreprise multinationale. Vous pouvez utiliser le paramètre _utilisateurs_ pour spécifier ce groupe de rôles (à l’aide de la propriété Name du groupe de rôles), puis utilisez le paramètre _Filter_ pour autoriser uniquement les boîtes aux lettres dans le fuseau horaire à rechercher.<br/> Vous ne pouvez pas spécifier de groupes de distribution avec ce paramètre.  <br/> |
   

## <a name="examples-of-creating-search-permissions-filters"></a>Exemples de création de filtres d’autorisations de recherche

Voici quelques exemples d’utilisation de la cmdlet **New-ComplianceSecurityFilter** pour créer un filtre d’autorisations de recherche. 
  
Cet exemple permet à l’utilisateur annb@contoso.com effectuer toutes les actions de recherche de contenu uniquement pour les boîtes aux lettres au Canada. Ce filtre contient l’indicatif du pays numérique à trois chiffres pour le Canada de la norme ISO 3166-1.

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
   
Cet exemple permet à ses membres du groupe de rôles personnalisés OneDrive eDiscovery responsables pour rechercher uniquement le contenu de OneDrive pour des sites dans l’organisation.

```
New-ComplianceSecurityFilter -FilterName OneDriveOnly  -Users "OneDrive eDiscovery Managers" -Filters "Site_Path -like 'https://contoso-my.sharepoint.com/personal*'" -Action Search
```
   
> [!NOTE]
> Pour limiter l’accès des utilisateurs à la recherche des sites spécifiques, utilisez le filtre `Site_Path`, comme illustré dans l’exemple précédent. À l’aide de `Site_Site` ne fonctionne pas. 
  
Cet exemple limite l’utilisateur à l’exécution de toutes les actions de recherche de contenu uniquement sur les messages électroniques envoyés au cours de l’année 2015.

```
New-ComplianceSecurityFilter -FilterName EmailDateRestrictionFilter -Users donh@contoso.com -Filters "MailboxContent_Received -ge '01-01-2015' -and MailboxContent_Received -le '12-31-2015'" -Action All
```
   
Comme l’exemple précédent, cet exemple limite l’utilisateur à l’exécution de toutes les actions de recherche de contenu sur les documents modifiés au cours de l’année 2015.

```
New-ComplianceSecurityFilter -FilterName DocumentDateRestrictionFilter -Users donh@contoso.com -Filters "SiteContent_LastModifiedTime -ge '01-01-2015' -and SiteContent_LastModifiedTime -le '12-31-2015'" -Action All
```
   
Cet exemple empêche les membres du groupe de rôles « Gestionnaires de découverte OneDrive » d’effectuer des actions de recherche de contenu sur une boîte aux lettres dans l’organisation. 

```
New-ComplianceSecurityFilter -FilterName NoEXO -Users "OneDrive Discovery Managers" -Filters "Mailbox_Alias -notlike '*'"  -Action All
```
  
## <a name="get-compliancesecurityfilter"></a>Get-ComplianceSecurityFilter

La **Get-ComplianceSecurityFilter** est utilisée pour renvoyer une liste de filtres des autorisations de recherche. Utilisez le paramètre _FilterName_ pour retourner des informations pour un filtre de recherche spécifique. 
  
## <a name="set-compliancesecurityfilter"></a>Set-ComplianceSecurityFilter

Le **Jeu-ComplianceSecurityFilter** est utilisé pour modifier un filtre d’autorisations recherche existant. Le seul paramètre requis est _FilterName_. 
  
|**Paramètre**|**Description**|
|:-----|:-----|
| _Action_| Le paramètre _Action_ spécifie ce type d’action de recherche le filtre est appliqué à. Les actions de recherche de contenu possibles sont les suivants :<br/><br/> **Exporter** - le filtre est appliqué lors de l’exportation des résultats de la recherche.  <br/> **Aperçu** - le filtre est appliqué lors de l’aperçu des résultats de la recherche.  <br/> **Vider** - le filtre est appliqué lors de la purge des résultats de la recherche.  <br/> **Recherche** - le filtre est appliqué lors de l’exécution d’une recherche.  <br/> **Tous les** - le filtre est appliqué à toutes les actions de recherche.  <br/> |
| _FilterName_|Le paramètre _FilterName_ Spécifie le nom du filtre d’autorisations. |
| _Filtres_| Le paramètre de _filtre_ spécifie les critères de recherche pour le filtre de sécurité de la conformité. Vous pouvez créer deux différents types de filtres :<br/><br/>**Filtrage de boîte aux lettres** - ce type de filtre spécifie les boîtes aux lettres de l’utilisateur affecté (spécifié par le paramètre _utilisateur_ ) peut rechercher. La syntaxe de ce type de filtre est **Mailbox_** _MailboxPropertyName_, où _MailboxPropertyName_ spécifie une propriété de la boîte aux lettres utilisée pour les boîtes aux lettres qui peuvent être recherchés d’étendue. Par exemple, le filtre de boîte aux lettres `"Mailbox_CustomAttribute10 -eq 'OttawaUsers'"` permettrait affecté à l’utilisateur ce filtre pour qu’il recherche les boîtes aux lettres qui ont la valeur « OttawaUsers » dans la propriété CustomAttribute10.  N’importe quelle propriété de destinataire filtrable pris en charge peut être utilisée pour la propriété _MailboxPropertyName_ . Pour obtenir la liste des propriétés prises en charge, voir [propriétés filtrables pour le paramètre - RecipientFilter](https://go.microsoft.com/fwlink/p/?LinkId=784903).<br/><br/>**Filtrage de contenu de la boîte aux lettres**- ce type de filtre est appliqué sur le contenu qui peut être recherché. Il spécifie le contenu de la boîte aux lettres que peut rechercher l’utilisateur affecté. La syntaxe de ce type de filtre est **MailboxContent_** _SearchablePropertyName:value_, où _SearchablePropertyName_ spécifie une propriété de langage de requête de mot clé (KQL) qui peut être spécifiée dans une recherche de contenu. Par exemple, le filtre de contenu de boîte aux lettres `MailboxContent_recipients:contoso.com` permet à l’utilisateur affecté ce filtre pour qu’il recherche pour les messages envoyés aux destinataires dans le domaine contoso.com.  Pour obtenir la liste des propriétés de message utilisables dans une requête, voir [requêtes de mot clé pour la recherche de contenu](keyword-queries-and-search-conditions.md).<br/><br/>**Filtrage de site et contenu de site** Il existe deux SharePoint et OneDrive pour les filtres Business liés au site que vous pouvez utiliser pour spécifier le site ou le contenu de site les utilisateurs peuvent effectuer des recherches : <br/><br/>- **Site_** *SearchableSiteProperty* <br/>- **SiteContent**_*SearchableSiteProperty*<br/><br/>Ces deux filtres sont interchangeables ; par exemple `"Site_Path -like 'https://contoso.spoppe.com/sites/doctors*'"` et `"SiteContent_Path -like 'https://contoso.spoppe.com/sites/doctors*'"` retournera les mêmes résultats. Mais pour vous aider à identifier ce que fait un filtre, vous pouvez utiliser `Site_` pour spécifier les propriétés liées au site (par exemple une URL de site) et `SiteContent_` pour spécifier les propriétés liées au contenu (par exemple, les types de document. Par exemple, le filtre `"Site_Path -like 'https://contoso.spoppe.com/sites/doctors*'"` permet à l’utilisateur affecté ce filtre pour qu’il recherche du contenu dans le https://contoso.spoppe.com/sites/doctors collection de sites. Le filtre `"SiteContent_FileExtension -eq 'docx'"` permet à l’utilisateur affecté ce filtre pour qu’il recherche pour les documents Word (Word 2007 et versions ultérieur).<br/><br/>Pour obtenir la liste des propriétés du site de recherche, voir [vue d’ensemble des propriétés analysées et gérées dans SharePoint](https://go.microsoft.com/fwlink/p/?LinkId=331599). Propriétés marquées par un **Oui** dans la colonne **utilisable dans une requête** peuvent être utilisées pour créer un site ou un filtrage de contenu de site.<br/><br/> **Important :** Un filtre de recherche unique peut comporter un type de filtre ; Il ne peut pas contenir un filtre de boîte aux lettres et un filtre de site ; de même, il ne peut pas contenir un filtre de boîte aux lettres et un filtre de contenu de boîte aux lettres. Toutefois, un filtre peut contenir une requête plus complexe du même type. Par exemple,`"Mailbox_CustomAttribute10 -eq 'FTE' -and Mailbox_MemberOfGroup -eq '$($DG.DistinguishedName)'"`          |
| _Utilisateurs_|Le paramètre _utilisateurs_ spécifie les utilisateurs qui reçoivent ce filtre appliqué à leurs recherches de contenu. Car il s’agit d’une propriété à valeurs multiples, la spécification d’un utilisateur ou un groupe d’utilisateurs avec ce paramètre remplacera la liste des utilisateurs existants. Voir les exemples suivants pour la syntaxe pour ajouter et supprimer les utilisateurs sélectionnés.<br/><br/>Vous pouvez également utiliser le paramètre _utilisateurs_ pour spécifier une sécurité &amp; groupe de rôles de centre de conformité. Filtre recherche les autorisations de groupe permet d’affecter ce rôle et créer un groupe de rôles personnalisés. Par exemple, supposons que vous avez un groupe de rôles personnalisés pour les responsables de découverte électronique pour la filiale US d’une entreprise multinationale. Vous pouvez utiliser le paramètre _utilisateurs_ pour spécifier ce groupe de rôles (à l’aide de la propriété Name du groupe de rôles), puis utilisez le paramètre _Filter_ pour autoriser uniquement les boîtes aux lettres dans le fuseau horaire à rechercher.<br/><br/>Vous ne pouvez pas spécifier de groupes de distribution avec ce paramètre. |

## <a name="examples-of-changing-search-permissions-filters"></a>Exemples de filtres de recherche des autorisations de modification

Les exemples suivants indiquent comment utiliser les applets de commande **Get-ComplianceSecurityFilter** et **Set-ComplianceSecurityFilter** pour ajouter ou supprimer un utilisateur à la liste d’utilisateurs auquel appartient le filtre existant. Lorsque vous ajoutez ou supprimez des utilisateurs d’un filtre, spécifiez l’utilisateur à l’aide de leur adresse SMTP. 
  
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

La **Suppression-ComplianceSecurityFilter** est utilisée pour supprimer un filtre de recherche. Utilisez le paramètre _FilterName_ pour spécifier le filtre que vous souhaitez supprimer. 
  
## <a name="more-information"></a>Plus d'informations

- **Comment ne recherche pas les autorisations filtrage ?** Le filtre d’autorisations est ajouté à la requête de recherche lors de l’exécution d’une recherche de contenu. Le filtre d’autorisations est essentiellement lié à la requête de recherche par l’opérateur booléen **AND** . Par exemple, que vous avez un filtre d’autorisations permettant de Bob effectuer toutes les actions de recherche sur les boîtes aux lettres des membres du groupe de distribution travailleurs. Bob exécute une recherche de contenu sur toutes les boîtes aux lettres dans l’organisation avec la requête de recherche `sender:jerry@adatum.com`. Étant donné que le filtre d’autorisations et la requête de recherche sont associées logiquement par l’opérateur **et** , la recherche retournera tous les messages envoyés par jerry@adatum.com pour tous les membres du groupe de distribution travailleurs. 
    
- **Que se passe-t-il si vous disposez de plusieurs filtres d’autorisations de recherche ?** Dans une requête de recherche de contenu, plusieurs filtres autorisations sont combinées par des opérateurs booléens **ou** . Ainsi, les résultats doivent être retournés si les filtres sont remplies. Dans une recherche de contenu, tous les filtres (combinées par des opérateurs **ou** ) puis associés à la requête de recherche par l’opérateur **AND** . Prenons l’exemple précédent, où un filtre de recherche permet de Bob pour qu’il recherche les membres du groupe de distribution travailleurs de boîtes aux lettres. Nous créons ensuite un autre filtre Bob empêche la recherche de boîte aux lettres de Phil (« alias_boîte_aux_lettres - ne « Phil » »). Et supposons également que Phil est membre du groupe de collaborateurs. Si Bob exécute une recherche de contenu (à partir de l’exemple précédent) sur toutes les boîtes aux lettres dans l’organisation, les résultats de recherche est renvoyées pour la boîte aux lettres de Phil même si vous avez appliqué le filtre pour empêcher la recherche de boîte aux lettres de Phil Bob. Il s’agit, car le premier filtre, qui permet de Bob rechercher le groupe de collaborateurs, a la valeur true. Et Phil étant un membre du groupe de collaborateurs, Bob peut rechercher les boîtes aux lettres de Phil. 
    
- **Ne recherche pas les autorisations pour les boîtes aux lettres inactives filtrage ?** Oui, vous pouvez utiliser les boîtes aux lettres et des filtres de contenu de boîte aux lettres pour limiter qui peut rechercher les boîtes aux lettres inactives dans votre organisation. Comme une boîte aux lettres régulière, une boîte aux lettres inactive doit être configuré avec la propriété destinataire qui est utilisée pour créer un filtre d’autorisations. Si nécessaire, vous pouvez utiliser la commande **Get-Mailbox-InactiveMailboxOnly** pour afficher les propriétés de boîtes aux lettres inactives. Pour plus d’informations, voir [créer et gérer des boîtes aux lettres inactives dans Office 365](create-and-manage-inactive-mailboxes.md).
    
- **Ne recherche pas les autorisations pour les dossiers publics filtrage ?** Non. Comme expliquée précédemment, recherche les autorisations de filtrage ne peut pas être utilisées pour limiter qui peut rechercher des dossiers publics dans Exchange. Par exemple, éléments dans les dossiers publics ne peuvent pas être exclus les résultats de recherche par un filtre d’autorisations. 
    
- **Ne permettant à un utilisateur de rechercher tous les emplacements de contenu dans un service spécifique les empêche également de rechercher des emplacements de contenu dans un autre service ?** Non. Comme expliqué précédemment, vous devez créer un filtre d’autorisations de recherche pour empêcher explicitement les utilisateurs de rechercher des emplacements de contenu dans un service Office 365 spécifique (par exemple, afin d’empêcher un utilisateur de rechercher une boîte aux lettres Exchange ou un site SharePoint). En d’autres termes, création d’un filtre d’autorisations de recherche qui permet à un utilisateur de rechercher tous les sites SharePoint dans l’organisation n’empêche que l’utilisateur de rechercher les boîtes aux lettres. Par exemple, pour autoriser les administrateurs SharePoint pour qu’il recherche les sites SharePoint, vous devez créer un filtre qui les empêche de rechercher les boîtes aux lettres. De même, pour permettre aux administrateurs Exchange pour qu’il recherche les boîtes aux lettres, vous devez créer un filtre qui empêche les sites de recherche.
