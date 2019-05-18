---
title: Requêtes par mots clés et conditions de recherche pour la recherche de contenu
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: reference
f1_keywords:
- ms.o365.cc.SearchQueryLearnMore
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: c4639c2e-7223-4302-8e0d-b6e10f1c3be3
description: 'Découvrez les propriétés de messagerie et de fichier que vous pouvez rechercher dans les boîtes aux lettres Exchange Online et dans SharePoint ou OneDrive entreprise à l’aide de l’outil de recherche de contenu dans le centre de sécurité & Compliance Center.  '
ms.openlocfilehash: 01cc40f983ddae6db090f531bc33fc5cc7a638ed
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34152496"
---
# <a name="keyword-queries-and-search-conditions-for-content-search"></a>Requêtes par mots clés et conditions de recherche pour la recherche de contenu

Cette rubrique décrit les propriétés de messagerie et de document que vous pouvez rechercher dans les éléments de courrier électronique dans Exchange Online et les documents stockés sur SharePoint et OneDrive entreprise à l’aide de la fonctionnalité de recherche de contenu dans le centre de sécurité & Compliance Center. Vous pouvez également utiliser les cmdlets ** \*-ComplianceSearch** dans le centre de sécurité & Compliance Center PowerShell pour rechercher ces propriétés. La rubrique décrit également les éléments suivants:   
  
- Utilisation d’opérateurs de recherche booléens, de conditions de recherche et d’autres techniques de requête de recherche pour affiner les résultats de la recherche.
    
- Recherche de types de données sensibles et de types de données sensibles personnalisés dans SharePoint et OneDrive entreprise.
    
- Recherche de contenu de site partagé avec des utilisateurs extérieurs à votre organisation
    
Pour obtenir des instructions détaillées sur la façon de créer une recherche de contenu, consultez la rubrique [recherche de contenu dans Office 365](content-search.md).

  
> [!NOTE]
> Recherche de contenu dans le centre de sécurité & Compliance Center et les applets de commande ** \*ComplianceSearch** correspondantes dans le centre de sécurité & Compliance Center utilisent le langage de requête de mot clé (KQL). Pour plus d’informations, voir [référence de syntaxe du langage de requête de mot clé](https://go.microsoft.com/fwlink/?LinkId=269603). 
  
## <a name="searchable-email-properties"></a>Propriétés de messagerie utilisables dans une requête

Le tableau suivant répertorie les propriétés de message électronique pouvant faire l’objet d’une recherche à l’aide de la fonctionnalité de recherche de contenu dans le centre de sécurité & Compliance Center ou à l’aide de la cmdlet Set- **ComplianceSearch** ou de l’applet de commande **Set-ComplianceSearch** . Il inclut un exemple de syntaxe  _property:value_ pour chaque propriété et une description des résultats de recherche renvoyés par ces exemples. Vous pouvez taper ces `property:value` paires dans la zone Mots clés d’une recherche de contenu. 
  
|**Propriété**|**Description de la propriété**|**Exemples**|**Résultats de recherche renvoyés par les exemples**|
|:-----|:-----|:-----|:-----|
|AttachmentNames|Nom des fichiers joints à un message électronique.|`attachmentnames:annualreport.ppt`  <br/> `attachmentnames:annual*`|Messages possédant un fichier joint nommé annualreport.ppt. Dans le deuxième exemple, l’utilisation du caractère générique renvoie des messages contenant le mot « annuel » dans le nom d’un fichier joint.|
|Bcc|Champ Cci d'un message électronique.<sup>1</sup>|`bcc:pilarp@contoso.com`  <br/> `bcc:pilarp`  <br/> `bcc:"Pilar Pinilla"`|Tous les exemples renvoient des messages dont « Pilar Pinilla » est en copie carbone invisible.|
|Category| Catégories à rechercher. Les catégories peuvent être définies par les utilisateurs à l’aide d’Outlook ou d’Outlook sur le Web (anciennement Outlook Web App). Les valeurs possibles sont les suivantes :  <br/><br/>  blue  <br/>  green  <br/>  orange  <br/>  purple  <br/>  red  <br/>  yellow|`category:"Red Category"`|Messages auxquels a été attribuée la catégorie « red » dans les boîtes aux lettres source.|
|Cc|Champ Cc d'un message électronique.<sup>1</sup>|`cc:pilarp@contoso.com`  <br/> `cc:"Pilar Pinilla"`|Dans les deux exemples, les résultats renvoient les messages contenant « Pilar Pinilla » dans le champ Cc.|
|Folderid|ID de dossier (GUID) d’un dossier de boîte aux lettres spécifique. Si vous utilisez cette propriété, assurez-vous d’effectuer une recherche dans la boîte aux lettres dans laquelle se trouve le dossier spécifié. Notez que seul le dossier spécifié fera l’objet d’une recherche. Les sous-dossiers du dossier ne feront pas l’objet d’une recherche. Pour rechercher des sous-dossiers, vous devez utiliser la propriété FolderId pour le sous-dossier dans lequel vous souhaitez effectuer la recherche.  <br/> Pour plus d’informations sur la recherche de la propriété FolderId et l’utilisation d’un script pour obtenir les ID de dossier pour une boîte aux lettres spécifique, voir [use content Search in Office 365 for Targeted collections](use-content-search-for-targeted-collections.md).|`folderid:4D6DD7F943C29041A65787E30F02AD1F00000000013A0000`  <br/> `folderid:2370FB455F82FC44BE31397F47B632A70000000001160000 AND participants:garthf@contoso.com`|Le premier exemple renvoie tous les éléments dans le dossier de boîte aux lettres spécifié. Le deuxième exemple renvoie tous les éléments dans le dossier de boîte aux lettres spécifié qui ont été envoyés ou reçus par garthf@contoso.com.|
|From|Expéditeur d'un message électronique.<sup>1</sup>|`from:pilarp@contoso.com`  <br/> `from:contoso.com`|Messages envoyés par l'utilisateur indiqué ou à partir d'un domaine spécifié.|
|HasAttachment|Indique si un message contient une pièce jointe. Utilisez les valeurs **true** ou **false**.|`from:pilar@contoso.com AND hasattachment:true`|Messages envoyés par l’utilisateur spécifié qui ont des pièces jointes.|
|Importance|Importance d'un message électronique, que l'expéditeur peut préciser lors de l'envoi. Par défaut, les messages sont envoyés avec une importance normale, à moins que l'expéditeur préfère une importance **haute** ou **faible**.  |`importance:high`  <br/> `importance:medium`  <br/> `importance:low`|Messages marqués comme ayant une importance haute, normale ou faible.|
|IsRead|Indique si les messages ont été lus ou non. Utilisez les valeurs **true** ou **false**.|`isread:true`  <br/> `isread:false`|Le premier exemple renvoie des messages dont la propriété IsRead a la valeur **true**. Le deuxième exemple renvoie les messages dont la propriété IsRead a **** la valeur false.|
|ItemClass|Utilisez cette propriété pour rechercher des types de données tiers spécifiques importés par votre organisation dans Office 365. Utilisez la syntaxe suivante pour cette propriété:`itemclass:ipm.externaldata.<third-party data type>*`|`itemclass:ipm.externaldata.Facebook* AND subject:contoso`  <br/> `itemclass:ipm.externaldata.Twitter* AND from:"Ann Beebe" AND "Northwind Traders"`|Le premier exemple renvoie les éléments Facebook qui contiennent le mot «Contoso» dans la propriété Subject. Le deuxième exemple renvoie les éléments Twitter publiés par Ann Beebe et qui contiennent l’expression de mot-clé «Northwind Traders».  <br/> Pour obtenir la liste complète des valeurs à utiliser pour les types de données tiers pour la propriété ItemClass, consultez la rubrique [use content Search to Search tierce-Party Data imported to Office 365](use-content-search-to-search-third-party-data-that-was-imported.md).|
|Kind| Type de message électronique à rechercher. Valeurs possibles :  <br/>  contacts  <br/>  docs  <br/>  email  <br/>  externaldata  <br/>  faxes  <br/>  im  <br/>  journals  <br/>  meetings  <br/>  microsoftteams (renvoie les éléments des conversations, réunions et appels dans Microsoft Teams)  <br/>  notes  <br/>  posts  <br/>  rssfeeds  <br/>  tasks  <br/>  voicemail|`kind:email`  <br/> `kind:email OR kind:im OR kind:voicemail`  <br/> `kind:externaldata`|Le premier exemple renvoie des messages électroniques qui répondent aux critères de recherche. Le deuxième exemple renvoie les messages électroniques, les conversations de messagerie instantanée (y compris les conversations et conversations Skype entreprise dans Microsoft Teams) et les messages vocaux correspondant aux critères de recherche. Le troisième exemple renvoie les éléments qui ont été importés dans des boîtes aux lettres dans Office 365 à partir de sources de données tierces, telles que Twitter, Facebook et Cisco Jabber, qui répondent aux critères de recherche. Pour plus d’informations, consultez la rubrique [archivage de données tierces dans Office 365](https://go.microsoft.com/fwlink/p/?linkid=716918).|
|Participants|Tous les champs de contacts compris dans un message électronique ; De, À, Cc et Cci.<sup>1</sup>|`participants:garthf@contoso.com`  <br/> `participants:contoso.com`|Messages envoyés par ou envoyés à garthf@contoso.com. Le deuxième exemple renvoie tous les messages envoyés par ou envoyés à un utilisateur dans le domaine contoso.com.|
|Received|Date à laquelle un message électronique a été reçu par un destinataire.|`received:04/15/2016`  <br/> `received>=01/01/2016 AND received<=03/31/2016`|Messages reçus le 15 avril 2016. Le deuxième exemple renvoie tous les messages reçus entre le 1er janvier 2016 et le 31 mars 2016.|
|Recipients|Tous les champs de destinataires compris dans un message électronique ; À, Cc et Cci.<sup>1</sup>|`recipients:garthf@contoso.com`  <br/> `recipients:contoso.com`|Messages envoyés à garthf@contoso.com. Le deuxième exemple renvoie les messages envoyés à tous les destinataires dans le domaine contoso.com.|
|Sent|Date à laquelle un message électronique a été envoyé par l'expéditeur.|`sent:07/01/2016`  <br/> `sent>=06/01/2016 AND sent<=07/01/2016`|Messages envoyés à la date indiquée ou entre les dates spécifiées.|
|Size|Taille d'un élément, en octets.|`size>26214400`  <br/> `size:1..1048567`|Messages supérieurs à 25? Mbit. Le deuxième exemple renvoie les messages dont la taille est comprise entre 1 et 1 048 567 octets (1 Mo).|
|Subject|Texte de la ligne d'objet d'un message électronique.  <br/> **Remarque:** Lorsque vous utilisez la propriété Subject dans une requête, ???the recherche renvoie tous les messages dans lesquels la ligne d’objet contient le texte que vous recherchez. En d’autres termes, la requête ne renvoie que les messages qui ont une correspondance exacte. Par exemple, si vous recherchez `subject:"Quarterly Financials"`, vos résultats incluent les messages dont l’objet est «trimestriel financials 2018».|`subject:"Quarterly Financials"`  <br/> `subject:northwind`|Messages contenant l’expression «trimestriel Financials» n’importe où dans le texte de la ligne d’objet. Le deuxième exemple renvoie tous les messages contenant le mot « northwind » dans la ligne d'objet.|
|To|Champ À d'un message électronique.<sup>1</sup>|`to:annb@contoso.com`  <br/> `to:annb ` <br/> `to:"Ann Beebe"`|Tous les exemples renvoient les messages dans lesquels « Ann Beebe » est indiqué sur la ligne À.|
   
> [!NOTE]
> <sup>1</sup> pour la valeur d’une propriété de destinataire, vous pouvez utiliser l’adresse de messagerie (également appelée *nom d’utilisateur principal* ou UPN), le nom d’affichage ou l’alias pour spécifier un utilisateur. Par exemple, vous pouvez utiliser annb@contoso.com, annb ou « Ann Beebe » pour spécifier l'utilisateur Ann Beebe.<br/><br/>Lors de la recherche dans n’importe quelle propriété du destinataire (de, à, CC, CCI, participants et destinataires), Office 365 tente de développer l’identité de chaque utilisateur en le recherchant dans Azure Active Directory.  Si l’utilisateur est trouvé dans Azure Active Directory, la requête est étendue de manière à inclure l’adresse de messagerie (ou UPN), l’alias, le nom d’affichage et le LegacyExchangeDN de l’utilisateur.<br/><br/>Par exemple, une requête telle que `participants:ronnie@contoso.com` Expands to `participants:ronnie@contoso.com OR participants:ronnie OR participants:"Ronald Nelson" OR participants:"<LegacyExchangeDN>"`.

## <a name="searchable-site-properties"></a>Propriétés de site utilisables dans une requête

Le tableau suivant répertorie certaines des propriétés SharePoint et OneDrive entreprise qui peuvent être recherchées à l’aide de la fonctionnalité de recherche de contenu dans le centre de sécurité & Compliance Center ou à l’aide de **New-ComplianceSearch** ou de **Set-ComplianceSearch **cmdlet. Il inclut un exemple de syntaxe  _property:value_ pour chaque propriété et une description des résultats de recherche renvoyés par ces exemples. 
  
Pour obtenir la liste complète des propriétés SharePoint pouvant faire l’objet d’une recherche, voir [vue d’ensemble des propriétés analysées et gérées dans SharePoint](https://go.microsoft.com/fwlink/p/?LinkId=331599). Les propriétés marquées par **Oui** dans la colonne pouvant faire l’objet d’une **requête** peuvent être recherchées. 
  
|**Propriété**|**Description de la propriété**|**Exemple**|**Résultats de recherche renvoyés par les exemples**|
|:-----|:-----|:-----|:-----|
|Auteur|Champ Auteur des documents Office (subsiste si un document est copié). Par exemple, si un utilisateur crée un document et l’envoie par courrier électronique à une personne qui le charge ensuite sur SharePoint, le document conserve toujours l’auteur d’origine. Veillez à utiliser le nom complet de l’utilisateur pour cette propriété.|`author:"Garth Fort"`|Tous les documents créés par Garth Fort.|
|ContentType|Type de contenu SharePoint d’un élément, tel qu’un élément, un document ou une vidéo.|`contenttype:document`|Tous les documents sont renvoyés.|
|Created|Date de création d’un élément.|`created\>=06/01/2016`|Tous les éléments créés le 1er juin 2016 ou après cette fin.|
|CreatedBy|Personne qui a créé ou chargé un élément. Veillez à utiliser le nom complet de l’utilisateur pour cette propriété.|`createdby:"Garth Fort"`|Tous les éléments créés ou chargés par Garth Fort.|
|DetectedLanguage|Langue d’un élément.|`detectedlanguage:english`|Tous les éléments en anglais.|
|DocumentLink|Chemin d’accès (URL) d’un dossier spécifique sur un site SharePoint ou OneDrive entreprise. Si vous utilisez cette propriété, assurez-vous de rechercher le site dans lequel se trouve le dossier spécifié.  <br/> Pour renvoyer les éléments situés dans les sous-dossiers du dossier que vous spécifiez pour la propriété documentlink, vous devez ajouter\* /à l’URL du dossier spécifié; par exemple,`documentlink: "https://contoso.sharepoint.com/Shared Documents/*"`  <br/> <br/>Pour plus d’informations sur la recherche de la propriété documentlink et l’utilisation d’un script pour obtenir les URL documentlink pour les dossiers d’un site spécifique, voir [use content Search in Office 365 for Targeted collections](use-content-search-for-targeted-collections.md).|`documentlink:"https://contoso-my.sharepoint.com/personal/garthf_contoso_com/Documents/Private"`  <br/> `documentlink:"https://contoso-my.sharepoint.com/personal/garthf_contoso_com/Documents/Shared with Everyone/*" AND filename:confidential`|Le premier exemple renvoie tous les éléments dans le dossier OneDrive entreprise spécifié. Le deuxième exemple renvoie des documents dans le dossier de site spécifié (et tous les sous-dossiers) qui contiennent le mot «Confidential» dans le nom de fichier.|
|FileExtension|Extension d’un fichier; par exemple, docx, One, pptx ou xlsx.|`fileextension:xlsx`|Tous les fichiers Excel (Excel 2007 et versions ultérieures)|
|FileName|Nom d’un fichier.|`filename:"marketing plan"`  <br/> `filename:estimate`|Le premier exemple renvoie les fichiers contenant l’expression « marketing plan » (plan marketing) dans le titre. Le second exemple renvoie les fichiers contenant le mot « estimate » (devis) dans le nom du fichier.|
|LastModifiedTime|Date à laquelle un élément a été modifié pour la dernière fois.|`lastmodifiedtime>=05/01/2016`  <br/> `lastmodifiedtime>=05/10/2016 AND lastmodifiedtime<=06/1/2016`|Le premier exemple renvoie les éléments qui ont été modifiés à ou après le 1er mai 2016. Le deuxième exemple renvoie les éléments modifiés entre le 1er mai 2016 et le 1er juin 2016.|
|ModifiedBy|Personne qui a apporté les dernières modifications. Veillez à utiliser le nom complet de l’utilisateur pour cette propriété.|`modifiedby:"Garth Fort"`|Tous les éléments qui ont été modifiés en dernier par Garth Fort.|
|Path|Chemin d’accès (URL) d’un site spécifique dans un site SharePoint ou OneDrive entreprise.  <br/> Pour renvoyer des éléments situés dans des dossiers du site que vous spécifiez pour la propriété Path, vous devez ajouter\* /à l’URL du site spécifié; par exemple,`path: "https://contoso.sharepoint.com/Shared Documents/*"`  <br/> <br/> **Remarque:** L’utilisation `Path` de la propriété pour rechercher des emplacements OneDrive ne renverra pas les fichiers multimédias, tels que les fichiers. png,. TIFF ou. wav, dans les résultats de la recherche. Utilisez une autre propriété de site dans votre requête de recherche pour rechercher des fichiers multimédias dans les dossiers OneDrive. <br/>|`path:"https://contoso-my.sharepoint.com/personal/garthf_contoso_com/"`  <br/> `path:"https://contoso-my.sharepoint.com/personal/garthf_contoso_com/*" AND filename:confidential`|Le premier exemple renvoie tous les éléments du site OneDrive entreprise spécifié. Le deuxième exemple renvoie des documents dans le site spécifié (et les dossiers du site) qui contiennent le mot «Confidential» dans le nom de fichier.|
|SharedWithUsersOWSUser|Documents qui ont été partagés avec l’utilisateur spécifié et qui s’affichent dans la page **partagé avec moi** du site OneDrive entreprise de l’utilisateur. Il s’agit de documents qui ont été explicitement partagés avec l’utilisateur spécifié par d’autres personnes de votre organisation. Lorsque vous exportez des documents qui correspondent à une requête de recherche qui utilise la propriété SharedWithUsersOWSUser, les documents sont exportés à partir de l’emplacement de contenu d’origine de la personne qui a partagé le document avec l’utilisateur spécifié. Pour plus d’informations, consultez [la rubrique recherche de contenu de site partagé au sein de votre organisation](#searching-for-site-content-shared-within-your-organization).|`sharedwithusersowsuser:garthf`  <br/> `sharedwithusersowsuser:"garthf@contoso.com"`|Ces deux exemples renvoient tous les documents internes qui ont été explicitement partagés avec Garth fort et qui apparaissent sur la page **partagé avec moi** du compte OneDrive entreprise de Garth.|
|Site|URL d’un site ou d’un groupe de sites de votre organisation.|`site:"https://contoso-my.sharepoint.com"`  <br/> `site:"https://contoso.sharepoint.com/sites/teams"`|Le premier exemple renvoie des éléments à partir des sites OneDrive entreprise pour tous les utilisateurs de l’organisation. Le second exemple renvoie les éléments de tous les sites d’équipe.|
|Size|Taille d'un élément, en octets.|`size>=1`  <br/> `size:1..10000`|Le premier exemple renvoie les éléments dont la taille est supérieure à 1 octet. Le deuxième exemple renvoie les éléments dont la taille est comprise entre 1 et 10 000 octets.|
|Titre|Titre du document. La propriété Title est une métadonnée qui est spécifiée dans des documents Microsoft Office. Il est différent du nom de fichier du document.|`title:"communication plan"`|Tout document qui contient l’expression « communication plan » (plan de communication) dans la propriété de métadonnées du titre d’un document Office.|
   
## <a name="searchable-contact-properties"></a>Propriétés de contact pouvant faire l’objet d’une recherche

Le tableau suivant répertorie les propriétés de contact qui sont indexées et que vous pouvez rechercher à l’aide de la recherche de contenu. Il s’agit des propriétés que les utilisateurs peuvent configurer pour les contacts (également appelés contacts personnels) qui se trouvent dans le carnet d’adresses personnel de la boîte aux lettres d’un utilisateur. Pour rechercher des contacts, vous pouvez sélectionner les boîtes aux lettres à rechercher, puis utiliser une ou plusieurs propriétés de contact dans la requête par mot clé.
  
> [!TIP]
> Pour rechercher des valeurs qui contiennent des espaces ou des caractères spéciaux, utilisez des guillemets doubles ("") pour contenir l’expression; par exemple, `businessaddress:"123 Main Street"`. 
  
|**Propriété**|**Description de la propriété**|
|:-----|:-----|
|BusinessAddress|L’adresse dans la propriété de l’adresse de l' **entreprise** . La propriété est également appelée adresse **professionnelle** sur la page des propriétés du contact.|
|BusinessPhone|Le numéro de téléphone dans l’une des propriétés de numéro de **téléphone professionnel** .|
|CompanyName|Nom dans la propriété **Company** .|
|Service|Nom dans la propriété **Department** .|
|DisplayName|Nom d’affichage du contact. Il s’agit du nom dans la propriété **nom complet** du contact.|
|EmailAddress|Adresse de n’importe quelle propriété d’adresse de messagerie pour le contact. Notez que les utilisateurs peuvent ajouter plusieurs adresses de messagerie pour un contact. L’utilisation de cette propriété renvoie les contacts qui correspondent à l’une des adresses de messagerie du contact.|
|FileAs|Le **fichier en tant que** propriété. Cette propriété est utilisée pour spécifier la manière dont le contact est répertorié dans la liste des contacts de l’utilisateur. Par exemple, un contact peut être mentionné en tant que *prénom, nom* ou *nom, prénom* .|
|GivenName|Nom dans la propriété **First Name** .|
|HomeAddress|L’adresse dans n’importe quelle propriété d’adresse **personnelle** .|
|HomePhone|Le numéro de téléphone dans l’un des propriétés de numéro de téléphone du **domicile** .|
|IMAddress|La propriété d’adresse de messagerie instantanée, qui est généralement une adresse de messagerie utilisée pour la messagerie instantanée.|
|MiddleName|Nom dans la propriété de nom de **milieu** .|
|MobilePhone|Numéro de téléphone dans la propriété de numéro de téléphone **mobile** .|
|Nickname|Nom dans la propriété **Nickname** .|
|OfficeLocation|Valeur dans la propriété emplacement **Office** ou **Office** .|
|OtherAddress|Valeur de l' **autre** propriété Address.|
|Surname|Nom dans la propriété **Last** Name.|
|Titre|Titre de la propriété de **fonction** .|
   

## <a name="searchable-sensitive-data-types"></a>Types de données sensibles utilisables dans une requête

Vous pouvez utiliser la fonctionnalité de recherche de contenu dans le centre de sécurité et de conformité pour rechercher des données sensibles, telles que des numéros de carte de crédit ou des numéros de sécurité sociale, qui sont stockées dans des documents sur des sites SharePoint et OneDrive entreprise. Pour ce faire, vous pouvez utiliser `SensitiveType` la propriété et le nom d’un type d’informations sensibles dans une requête de mot clé. Par exemple, la requête `SensitiveType:"Credit Card Number"` renvoie des documents qui contiennent un numéro de carte de crédit. La requête `SensitiveType:"U.S. Social Security Number (SSN)"` renvoie des documents qui contiennent un numéro de sécurité sociale américain. Pour afficher la liste des types de données sensibles que vous pouvez rechercher, accédez à **classifications** \> **types d’informations sensibles** dans le centre de sécurité & Compliance Center. Vous pouvez utiliser la cmdlet **Get-DlpSensitiveInformationType** dans le centre de sécurité _AMP_ Compliance Center PowerShell pour afficher la liste des types d’informations sensibles. 
  
Vous pouvez également utiliser la `SensitiveType` propriété pour rechercher le nom d’un type d’informations sensibles personnalisé créé par vous (ou un autre administrateur) pour votre organisation. Notez que vous pouvez utiliser la colonne **éditeur** de la page **types d’informations sensibles** dans le centre de sécurité & Compliance Center (ou la propriété **Publisher** dans PowerShell) pour différencier les informations sensibles intégrées et personnalisées. catégories. Pour plus d’informations, consultez [la rubrique créer un type d’informations sensibles personnalisé](create-a-custom-sensitive-information-type.md).
  
Pour plus d’informations sur la création de `SensitiveType` requêtes à l’aide de la propriété, voir créer [une requête pour trouver des données sensibles stockées sur des sites](form-a-query-to-find-sensitive-data-stored-on-sites.md).

> [!NOTE]
> Vous ne pouvez pas utiliser les types de `SensitiveType` données sensibles et la propriété Search pour rechercher des données sensibles dans les boîtes aux lettres Exchange Online. Toutefois, vous pouvez utiliser des stratégies de protection contre la perte de données (DLP) pour protéger les données e-mail sensibles en transit. Pour plus d’informations, consultez la rubrique [vue d’ensemble des stratégies de protection contre la perte de données](data-loss-prevention-policies.md) et [recherche et recherche de données personnelles](search-for-and-find-personal-data.md).
  
## <a name="search-operators"></a>Opérateurs de recherche

Les opérateurs de recherche booléens, tels que **and**, **or**et **not**, permettent de définir des recherches plus précises en incluant ou en excluant des mots spécifiques dans la requête de recherche. D’autres techniques, telles que l’utilisation d’opérateurs de \>propriété (par exemple, = ou..), des guillemets, des parenthèses et des caractères génériques, vous aident à affiner une requête de recherche. Le tableau suivant répertorie les opérateurs disponibles pour restreindre ou élargir les résultats de recherche. 
  
|**Opérateur**|**Utilisation**|**Description**|
|:-----|:-----|:-----|
|AND|keyword1 AND keyword2|Renvoie les éléments qui incluent tous les mots clés ou `property:value` expressions spécifiés. Par exemple, `from:"Ann Beebe" AND subject:northwind` renvoie tous les messages envoyés par Ann Beebe qui contiennent le mot «Northwind» dans la ligne d’objet. <sup>n°2</sup>|
|+|keyword1 + keyword2 + keyword3|Renvoie les éléments qui contiennent  *soit*  `keyword2` soit  `keyword3` *, et*  qui contiennent également  `keyword1`. Par conséquent, cet exemple équivaut à la requête  `(keyword2 OR keyword3) AND keyword1`.  <br/> Notez que la requête  `keyword1 + keyword2` (avec un espace après le symbole **+** ) revient au même que d'utiliser l'opérateur ** AND **. Cette requête est équivalente à  `"keyword1 + keyword2"` et renvoie des éléments contenant l'expression exacte  `"keyword1 + keyword2"`.  |
|OR|keyword1 OR keyword2|Renvoie les éléments qui incluent un ou plusieurs mots clés ou `property:value` expressions spécifiés. <sup>n°2</sup>|
|NOT|keyword1 NOT keyword2  <br/> NOT from:"Ann Beebe"  <br/> NON Kind: messagerie instantanée|Exclut les éléments spécifiés par un mot `property:value` clé ou une expression. Dans le deuxième exemple, les messages envoyés par Ann Beebe. Le troisième exemple exclut les conversations de messagerie instantanée, telles que les conversations Skype entreprise qui sont enregistrées dans le dossier de boîte aux lettres historique des conversations. <sup>n°2</sup>|
|-|keyword1 -keyword2|Identique à l'opérateur **NOT**. Cette requête renvoie donc des éléments qui `keyword1` contiennent et excluent les éléments `keyword2`qui contiennent.|
|NEAR|keyword1 NEAR(n) keyword2|Renvoie les éléments qui incluent des mots proches les uns des autres, n étant égal au nombre de mots. Par exemple, `best NEAR(5) worst` renvoie tout élément dont le mot «pire» se trouve à moins de cinq mots de «meilleur». Si aucun nombre n'est spécifié, la distance par défaut est de huit mots. <sup>n°2</sup>|
|ONEAR|keyword1 ONEAR(n) keyword2|Similaire à **near**, mais retourne des éléments avec des mots proches l’un de l’autre dans l’ordre spécifié. Par exemple, `best ONEAR(5) worst` renvoie tout élément où le mot «Best» se produit avant le mot «pires» et les deux mots se situent entre cinq mots. Si aucun nombre n'est spécifié, la distance par défaut est de huit mots. <sup>n°2</sup> <br/> > [!NOTE]> l’opérateur **ONEAR** n’est pas pris en charge lors de la recherche de boîtes aux lettres; elle fonctionne uniquement lors de la recherche de sites SharePoint et OneDrive entreprise. Si vous recherchez des boîtes aux lettres et des sites dans la même recherche et que la requête inclut l’opérateur **ONEAR** , la recherche renverra des éléments de boîte aux lettres comme si vous utilisiez l’opérateur **near** . En d’autres termes, la recherche renvoie les éléments dans lesquels les mots spécifiés sont proches les uns des autres, quel que soit l’ordre dans lequel ils se produisent.|
|:|property:value|Le signe deux-points (:) dans la `property:value` syntaxe, indique que la valeur de la propriété recherchée contient la valeur spécifiée. Par exemple,  `recipients:garthf@contoso.com` renvoie les messages envoyés à garthf@contoso.com.|
|=|propriété = valeur|Identique à l’opérateur **:** .|
|\<|property\<value|Indique que la propriété recherchée est inférieure à la valeur spécifiée.<sup>1</sup>|
|\>|property\>value|Indique que la propriété recherchée est supérieure à la valeur spécifiée.<sup>1</sup>|
|\<=|property\<=value|Indique que la propriété recherchée est inférieure ou égale à la valeur spécifiée.<sup>1</sup>|
|\>=|property\>=value|Indique que la propriété recherchée est supérieure ou égale à la valeur spécifiée.<sup>1</sup>|
|..|propriété: valeur1.. valeur2|Indique que la propriété recherchée est supérieure ou égale à value1 et inférieure ou égale à value2.<sup>1</sup>|
|"  "|"fair value"  <br/> subject:"Quarterly Financials"|Utilisez des guillemets doubles ("") pour rechercher une expression ou un terme exact dans les `property:value` requêtes de mot clé et de recherche.|
|\*|cat\*  <br/> subject:set\*|Les recherches par caractères génériques préfixées (où l'astérisque est placée à la fin d'un mot) correspondent à zéro ou plusieurs caractères dans les mots-clés ou les requêtes  `property:value`. Par exemple, `title:set*` renvoie les documents qui contiennent le mot set, Setup et Setting (et les autres mots commençant par «set») dans le titre du document.  <br/><br/> **Remarque:** Vous pouvez utiliser uniquement des recherches par caractères génériques avec préfixe; par exemple, **Cat\* ** ou **Set\***. Les recherches de suffixe ( ** \*Cat** ), les recherches d’infixe ( **\*c t** ) et les recherches de sous-chaînes ( ** \*Cat\* ** ) ne sont pas prises en charge.|
|(  )| (fair OR free) AND from:contoso.com  <br/> (IPO OR initial) AND (stock OR shares)  <br/> (quarterly financials)|Les parenthèses regroupent des expressions booléennes, des éléments  `property:value` et des mots-clés. Par exemple,  `(quarterly financials)` renvoie les éléments contenant les mots « quarterly » et « financials ».  |
   
> [!NOTE]
> <sup>1</sup> Utilisez cet opérateur pour les propriétés ayant des valeurs de date ou des valeurs numériques.<br/> <sup>2</sup> Les opérateurs booléens doivent être en majuscules, par exemple **AND**. Si vous utilisez un opérateur en minuscules, comme **and**, il sera traité comme un mot clé dans la requête de recherche. 
  
## <a name="search-conditions"></a>Conditions de recherche

Vous pouvez ajouter des conditions à une requête de recherche pour affiner une recherche et renvoyer un ensemble de résultats plus raffiné. Chaque condition ajoute une clause à la requête de recherche KQL qui est créée et exécutée lorsque vous démarrez la recherche.
  
[Conditions de propriétés communes ](#conditions-for-common-properties)

[Conditions pour les propriétés de messagerie](#conditions-for-mail-properties)

[Conditions des propriétés de document](#conditions-for-document-properties)

[Opérateurs utilisés avec des conditions](#operators-used-with-conditions)

[Instructions relatives à l’utilisation des conditions](#guidelines-for-using-conditions)

[Exemples](#examples-of-using-conditions-in-search-queries)
  
### <a name="conditions-for-common-properties"></a>Conditions de propriétés communes

Créez une condition avec des propriétés communes lorsque vous recherchez des boîtes aux lettres et des sites dans la même recherche. Le tableau suivant répertorie les propriétés disponibles à utiliser lors de l’ajout d’une condition.
  
|**Condition**|**Description**|
|:-----|:-----|
|Date|Pour la messagerie électronique, date à laquelle un message a été reçu par un destinataire ou envoyé par l’expéditeur. Pour les documents, date de la dernière modification d’un document.|
|Expéditeur/auteur|Pour la messagerie électronique, personne ayant envoyé le message. Pour les documents, personne mentionnée dans le champ Auteur des documents Office. Vous pouvez saisir plusieurs noms, séparés par des virgules. Deux ou plusieurs valeurs sont connectées logiquement par l’opérateur **OR**.|
|Taille (en octets)|Pour la messagerie électronique et les documents, taille de l’élément (en octets).|
|Subject/title|Pour la messagerie électronique, texte de la ligne d’objet d’un message. Pour les documents, titre du document. Comme expliqué précédemment, la propriété Title est des métadonnées spécifiées dans les documents Microsoft Office. Vous pouvez taper le nom de plus d’un objet/titre, séparé par des virgules. Deux ou plusieurs valeurs sont connectées logiquement par l’opérateur **OR**.|
|Balise de conformité|Pour les courriers électroniques et les documents, étiquettes qui ont été attribuées automatiquement à des messages et des documents par des étiquettes ou des stratégies qui ont été affectées manuellement par les utilisateurs. Les étiquettes sont utilisées pour classer le courrier électronique et les documents à des fins de gouvernance des données et appliquer des règles de rétention basées sur la classification définie par l’étiquette. Vous pouvez taper une partie du nom de l’étiquette et utiliser un caractère générique ou taper le nom complet de l’étiquette. Pour plus d’informations, consultez la rubrique [vue d’ensemble des étiquettes dans Office 365](labels.md).|
  
### <a name="conditions-for-mail-properties"></a>Conditions pour les propriétés de messagerie

Créez une condition à l’aide des propriétés de messagerie lorsque vous recherchez des éléments dans des boîtes aux lettres ou des dossiers publics. Le tableau suivant répertorie les propriétés de messagerie que vous pouvez utiliser pour une condition. Notez que ces propriétés sont un sous-ensemble des propriétés de messagerie qui ont été décrites précédemment. Ces descriptions sont répétées pour faciliter votre travail.
  
|**Condition**|**Description**|
|:-----|:-----|
|Type de message| Type de message à rechercher. Il s’agit de la même propriété que la propriété de messagerie Kind. Valeurs possibles :  <br/><br/>  contacts  <br/>  docs  <br/>  email  <br/>  externaldata  <br/>  faxes  <br/>  im  <br/>  journals  <br/>  meetings  <br/>  microsoftteams  <br/>  notes  <br/>  posts  <br/>  rssfeeds  <br/>  tasks  <br/>  voicemail|
|Participants|Tous les champs de contacts compris dans un message électronique ; De, À, Cc et Cci.|
|Type|Propriété de classe de message pour un élément de courrier électronique. Il s’agit de la même propriété que la propriété de messagerie ItemClass. Il s’agit également d’une condition à valeurs multiples. Pour sélectionner plusieurs classes de message, maintenez la touche **CTRL** enfoncée, puis cliquez sur au moins deux classes de messages dans la liste déroulante que vous souhaitez ajouter à la condition. Chaque classe de message que vous sélectionnez dans la liste est logiquement connectée par l’opérateur **or** dans la requête de recherche correspondante.  <br/> Pour obtenir la liste des classes de message (et de leur ID de classe de message correspondant) utilisées par Exchange et que vous pouvez sélectionner dans la liste de **classes de message** , voir [types d’éléments et classes de messages](https://go.microsoft.com/fwlink/?linkid=848143).|
|Received|Date à laquelle un message électronique a été reçu par un destinataire. Il s’agit de la même propriété que la propriété de messagerie Received.|
|Destinataires|Personne à laquelle un message électronique a été envoyé. Il s’agit de la même propriété que la propriété de messagerie To.|
|Expéditeur|Expéditeur d’un message électronique.|
|Sent|Date à laquelle un message électronique a été envoyé par l’expéditeur. Il s’agit de la même propriété que la propriété de messagerie Sent.|
|Subject|Texte de la ligne d'objet d'un message électronique.|
|À|Destinataire d’un message électronique.|
  
### <a name="conditions-for-document-properties"></a>Conditions des propriétés de document

Créer une condition à l’aide des propriétés de document lors de la recherche de documents sur des sites SharePoint et OneDrive entreprise. Le tableau suivant répertorie les propriétés de document que vous pouvez utiliser pour une condition. Notez que ces propriétés sont un sous-ensemble des propriétés de site qui ont été décrites précédemment; ces descriptions sont répétées dans un souci de commodité.
  
|**Condition**|**Description**|
|:-----|:-----|
|Auteur|Champ Auteur des documents Office (subsiste si un document est copié). Par exemple, si un utilisateur crée un document et l’envoie par courrier électronique à une personne qui le charge ensuite sur SharePoint, le document conserve toujours l’auteur d’origine.|
|Titre|Titre du document. Cette propriété correspond aux métadonnées spécifiées dans les documents Office. Il est différent du nom de fichier du document.|
|Created|Date de création d’un document.|
|Dernière modification|Date de la dernière modification apportée à un document.|
|Type de fichier|Extension d’un fichier; par exemple, docx, One, pptx ou xlsx. Il s’agit de la même propriété que la propriété de site FileExtension.|
  
### <a name="operators-used-with-conditions"></a>Opérateurs utilisés avec des conditions

Lorsque vous ajoutez une condition, vous pouvez sélectionner un opérateur pertinent par rapport au type de propriété pour la condition. Le tableau suivant décrit les opérateurs qui sont utilisés avec les conditions et répertorie l’équivalent utilisé dans la requête de recherche.
  
|**Opérateur**|**Équivalent dans la requête**|**Description**|
|:-----|:-----|:-----|
|Après|`property>date`|Utilisé avec les conditions de date. Renvoie les éléments qui ont été envoyés, reçus ou modifiés après la date spécifiée. |
|Avant|`property<date`|Utilisé avec les conditions de date. Renvoie les éléments qui ont été envoyés, reçus ou modifiés avant la date spécifiée.|
|Existant|`date..date`|Utilisé avec les conditions de date et de taille. Lorsqu’il est utilisé avec une condition de date, renvoie les éléments qui ont été envoyés, reçus ou modifiés dans la plage de dates spécifiée. Lorsqu’il est utilisé avec une condition de taille, renvoie les éléments dont la taille est comprise dans la plage spécifiée.|
|Contient l’un des éléments|`(property:value) OR (property:value)`|Utilisé avec les conditions des propriétés qui spécifient une valeur de chaîne. Renvoie les éléments qui contiennent une partie d’une ou plusieurs valeurs de chaîne spécifiées.|
|Ne contient pas|`-property:value`  <br/> `NOT property:value`|Utilisé avec les conditions des propriétés qui spécifient une valeur de chaîne. Renvoie les éléments qui ne contiennent aucune partie de la valeur de chaîne spécifiée.|
|N’est pas égal à|`-property=value`  <br/> `NOT property=value`|Utilisé avec les conditions des propriétés qui spécifient une valeur de chaîne. Renvoie les éléments qui ne contiennent pas la chaîne spécifique.|
|Égal à|`size=value`|Renvoie les éléments qui sont égaux à la taille spécifiée. <sup>1</sup>|
|Est égal à l’un des éléments|`(property=value) OR (property=value)`|Utilisé avec les conditions des propriétés qui spécifient une valeur de chaîne. Renvoie les éléments qui correspondent exactement à une ou plusieurs valeurs de chaîne spécifiées.|
|Dépasse|`size>value`|Renvoie les éléments pour lesquels la propriété spécifiée est supérieure à la valeur spécifiée. <sup>1</sup>|
|Supérieur ou égal|`size>=value`|Renvoie les éléments pour lesquels la propriété spécifiée est supérieure ou égale à la valeur spécifiée. <sup>1</sup>|
|Supérieur|`size<value`|Renvoie les éléments qui sont supérieurs ou égaux à la valeur spécifique. <sup>1</sup>|
|Inférieur ou égal|`size<=value`|Renvoie les éléments qui sont supérieurs ou égaux à la valeur spécifique. <sup>1</sup>|
|Différent de|`size<>value`|Renvoie les éléments qui ne sont pas égaux à la taille spécifiée. <sup>1</sup>|
   
> [!NOTE]
> <sup>1</sup> cet opérateur est disponible uniquement pour les conditions qui utilisent la propriété Size. 
  
### <a name="guidelines-for-using-conditions"></a>Instructions relatives à l’utilisation des conditions

Gardez les points suivants à l’esprit lorsque vous utilisez des critères de recherche.
  
- Une condition est connectée à la requête de mot-clé (spécifiée dans la zone de mot-clé) sur le plan logique par l’opérateur **AND**. Cela signifie que les éléments doivent satisfaire la requête de mot-clé et la condition pour être inclus dans les résultats. C’est ainsi que les conditions contribuent à affiner vos résultats. 
    
- Si vous ajoutez deux ou plusieurs conditions uniques à une requête de recherche (conditions qui spécifient différentes propriétés), ces conditions sont logiquement liées par l’opérateur **and** . Cela signifie que seuls les éléments qui répondent à toutes les conditions (en plus des requêtes de mot-clé) sont renvoyés. 
    
- Si vous ajoutez plusieurs conditions pour la même propriété, celles-ci sont connectées sur le plan logique par l’opérateur **OR**. Cela signifie que les éléments renvoyés sont ceux qui satisfont la requête de mot-clé et l’une des conditions. Par conséquent, les groupes de mêmes conditions sont connectés par l’opérateur **OR** et les ensembles de conditions uniques sont connectés par l’opérateur **AND**. 
    
- Si vous ajoutez plusieurs valeurs (séparées par des virgules ou des points-virgules) à une seule condition, ces valeurs sont reliées par l’opérateur **ou** . Les éléments renvoyés sont ceux qui contiennent l’une des valeurs spécifiées pour la propriété dans la condition. 
    
- La requête de recherche créée à l’aide de la zone Mots clés et conditions est affichée sur la page de **recherche** , dans le volet d’informations de la recherche sélectionnée. Dans une requête, tout ce qui se trouve à droite `(c:c)` de la notation indique les conditions qui sont ajoutées à la requête. 
    
- Les conditions ajoutent uniquement des propriétés à la requête de recherche; les opérateurs ne pas ajouter. C’est pourquoi la requête affichée dans le volet détail n’affiche pas les opérateurs à droite de `(c:c)` la notation. KQL ajoute les opérateurs logiques (conformément aux règles précédemment expliquées) lors de l’exécution de la requête. 
    
- Vous pouvez utiliser la commande glisser-déposer pour modifier l’ordre des conditions. Cliquez simplement sur la commande pour une condition et déplacez-la vers le haut ou vers le bas.
    
- Comme indiqué précédemment, certaines propriétés de condition vous permettent de saisir plusieurs valeurs. Chaque valeur est connectée sur le plan logique par l’opérateur **OR**. Cela entraîne la même logique que la présence de plusieurs instances de la même condition avec une valeur unique pour chacune. Les illustrations suivantes montrent un exemple de condition unique avec plusieurs valeurs et un exemple de conditions multiples (pour la même propriété) avec une valeur unique. Les deux exemples entraînent la même requête:`(filetype="docx") OR (filetype="pptx") OR (filetype="xlsx")`
    
    ![Un message doit remplir toutes les conditions de la règle. Si vous souhaitez qu’une condition ou une autre s’applique, utilisez des règles distinctes pour chaque condition. Par exemple, si vous souhaitez ajouter la même clause d’exclusion de responsabilité aux messages comportant des pièces jointes et aux messages dont le contenu correspond à un modèle, créez une règle pour chaque condition. Vous pouvez facilement copier une règle.](media/9880aa29-d117-4531-be20-6d53f1d21341.gif)
  
    ![Plusieurs conditions de recherche pour la même propriété](media/1e63d37d-6d8d-4c9b-a509-a7e1c3a05193.gif)
  
> [!TIP]
> Si une condition accepte plusieurs valeurs, nous vous recommandons d’utiliser une condition unique et de spécifier plusieurs valeurs (séparées par des virgules ou des points-virgules). Cela permet de vous assurer que la logique de requête appliquée est celle que vous souhaitez. 
  
### <a name="examples-of-using-conditions-in-search-queries"></a>Exemples

Les exemples suivants illustrent la version basée sur l’interface utilisateur graphique d’une requête de recherche avec des conditions, la syntaxe de requête de recherche qui s’affiche dans le volet d’informations de la recherche sélectionnée (qui est également renvoyée par la cmdlet **Get-ComplianceSearch** ) et la logique du requête KQL correspondante. 
  
#### <a name="example-1"></a>Exemple 1

Cet exemple renvoie des documents sur des sites SharePoint et OneDrive entreprise qui contiennent un numéro de carte de crédit et ont été modifiés pour la dernière fois avant le 1er janvier 2016.
  
 **Interface utilisateur graphique**
  
![Premier exemple de conditions de recherche](media/099515ba-d4ee-474e-af25-3aa48816b87b.gif)
  
 **Syntaxe de requête de recherche**
  
 `SensitiveType:"Credit Card Number(c:c)(lastmodifiedtime<2016-01-01)`
  
 **Logique de requête de recherche**
  
 `SensitiveType:"Credit Card Number" AND (lastmodifiedtime<2016-01-01)`
  
#### <a name="example-2"></a>Exemple 2

Cet exemple renvoie les éléments de messagerie ou les documents qui contiennent le mot clé « report », ont été envoyés ou créés avant le 1er avril 2105, et contiennent le mot « northwind » dans le champ Objet des messages électroniques ou dans la propriété Title des documents. La requête exclut les pages Web qui répondent à d’autres critères de recherche. 
  
 **Interface utilisateur graphique**
  
![Deuxième exemple de conditions de recherche](media/fe07d495-df81-42da-8106-3cdb409c6e7f.gif)
  
 **Syntaxe de requête de recherche**
  
 `report(c:c)(date<2016-04-01)(subjecttitle:"northwind")(-filetype="aspx")`
  
 **Logique de requête de recherche**
  
 `report AND (date<2016-04-01) AND (subjecttitle:"northwind") NOT (filetype="aspx")`
  
#### <a name="example-3"></a>Exemple 3
<a name="conditionexamples"> </a>

Cet exemple renvoie des messages électroniques ou des réunions de calendrier qui ont été envoyés entre 12/1/2016 et 11/30/2016 et qui contiennent des mots commençant par «Phone» ou «Smartphone».
  
 **Interface utilisateur graphique**
  
![Troisième exemple de conditions de recherche](media/973d45fc-0923-43d6-9d0a-25e4a625f057.gif)
  
 **Syntaxe de requête de recherche**
  
 `phone* OR smartphone*(c:c)(sent=2016-12-01..2016-11-30)(kind="email")(kind="meetings")`
  
 **Logique de requête de recherche**
  
 `phone* OR smartphone* AND (sent=2016-12-01..2016-11-30) AND ((kind="email") OR (kind="meetings"))`
  
## <a name="searching-for-site-content-shared-with-external-users"></a>Rechercher du contenu de site partagé avec des utilisateurs externes

Vous pouvez également utiliser la fonctionnalité de recherche de contenu dans le centre de sécurité & Compliance Center pour rechercher des documents stockés sur SharePoint et OneDrive entreprise qui ont été partagés avec des personnes extérieures à votre organisation. Ainsi, vous pouvez identifier les informations sensibles ou confidentielles qui sont partagées en dehors de votre organisation. Pour ce faire, vous pouvez utiliser `ViewableByExternalUsers` la propriété dans une requête de mot clé. Cette propriété renvoie des documents ou des sites qui ont été partagés avec des utilisateurs externes à l’aide de l’une des méthodes de partage suivantes: 
  
- Invitation de partage qui exige que les utilisateurs se connectent à votre organisation en tant qu’utilisateur authentifié.
    
- Lien invité anonyme, qui permet à toute personne disposant de ce lien d’accéder à la ressource sans avoir à être authentifiée.
    
Voici quelques exemples :
  
- La requête `ViewableByExternalUsers:true AND SensitiveType:"Credit Card Number"` renverra tous les éléments qui ont été partagés avec des personnes extérieures à votre organisation et qui contiennent un numéro de carte de crédit. 
    
- La requête `ViewableByExternalUsers:true AND ContentType:document AND site:"https://contoso.sharepoint.com/Sites/Teams"` renverra une liste de documents sur tous les sites d’équipe de l’organisation qui ont été partagés avec des utilisateurs externes. 
    
> [!TIP]
> Une requête de recherche telle `ViewableByExternalUsers:true AND ContentType:document` que peut renvoyer un grand nombre de fichiers. aspx dans les résultats de la recherche. Pour éliminer ces éléments (ou d’autres types de fichiers), vous pouvez `FileExtension` utiliser la propriété pour exclure des types de fichiers spécifiques; par exemple `ViewableByExternalUsers:true AND ContentType:document NOT FileExtension:aspx`. 
  
Qu’est-ce qui est considéré comme du contenu partagé avec des personnes extérieures à votre organisation ? Documents dans les sites SharePoint et OneDrive entreprise de votre organisation partagés en envoyant des invitations de partage ou partagés dans des emplacements publics. Par exemple, les activités utilisateur suivantes produisent du contenu visible par les utilisateurs externes :
  
- Un utilisateur partage un fichier ou un dossier avec une personne extérieure à votre organisation.
    
- Un utilisateur crée et envoie un lien vers un fichier partagé à une personne extérieure à votre organisation. Ce lien permet à l’utilisateur externe d’ouvrir (ou de modifier) le fichier.
    
- Un utilisateur envoie une invitation de partage ou un lien invité à une personne extérieure à votre organisation pour ouvrir (ou modifier) un fichier partagé.
    
### <a name="issues-using-the-viewablebyexternalusers-property"></a>Problèmes liés à l’utilisation de la propriété ViewableByExternalUsers

Tandis `ViewableByExternalUsers` que la propriété indique l’état du partage d’un document ou d’un site avec des utilisateurs externes, il existe quelques éléments à prendre en compte pour ce qui est de la propriété et non. Dans les scénarios suivants, la valeur de la `ViewableByExternalUsers` propriété n’est pas mise à jour et les résultats d’une requête de recherche de contenu qui utilise cette propriété peuvent être imprécis. 
  
- Modifications apportées à la stratégie de partage, telles que la désactivation du partage externe pour un site ou une organisation. La propriété affiche toujours les documents précédemment partagés comme étant accessibles de l’extérieur, même si l’accès externe a pu être révoqué.
    
- Modifications apportées à l’appartenance à un groupe, telles que l’ajout ou la suppression d’utilisateurs externes dans des groupes Office 365 ou des groupes de sécurité Office 365. La propriété n’est pas mise à jour automatiquement pour les éléments auxquels le groupe a accès.
    
- Envoi d’invitations de partage à des utilisateurs externes où le destinataire n’a pas accepté l’invitation et, par conséquent, n’a pas encore accès au contenu.
    
Dans ces scénarios, la `ViewableByExternalUsers` propriété ne reflète pas l’état de partage actuel tant que le site ou la bibliothèque de documents n’est pas ré-analysée et réindexée. 

## <a name="searching-for-site-content-shared-within-your-organization"></a>Recherche de contenu de site partagé au sein de votre organisation

Comme expliqué précédemment, vous pouvez utiliser la `SharedWithUsersOWSUser` propriété afin de rechercher des documents qui ont été partagés entre les personnes de votre organisation. Lorsqu’une personne partage un fichier (ou dossier) avec un autre utilisateur au sein de votre organisation, un lien vers le fichier partagé apparaît dans la page **partagé avec moi** du compte OneDrive entreprise de la personne avec laquelle le fichier a été partagé. Par exemple, pour rechercher les documents qui ont été partagés avec Sara Davis, vous pouvez utiliser la requête `SharedWithUsersOWSUser:"sarad@contoso.com"`. Si vous exportez les résultats de cette recherche, les documents d’origine (situés dans l’emplacement de contenu de la personne qui a partagé les documents avec Sara) seront téléchargés.
  
Notez que les documents doivent être explicitement partagés avec un utilisateur spécifique pour être renvoyés dans les résultats de `SharedWithUsersOWSUser` la recherche lors de l’utilisation de la propriété. Par exemple, lorsqu’une personne partage un document dans son compte OneDrive, elle a la possibilité de la partager avec tout le monde (à l’intérieur ou à l’extérieur de l’organisation), de la partager avec des personnes de l’organisation ou de la partager avec une personne spécifique. Voici une capture d’écran de la fenêtre de **partage** dans OneDrive, qui présente les trois options de partage. 
  
![Seuls les fichiers partagés avec des personnes spécifiques seront renvoyés par une requête de recherche qui utilise la propriété SharedWithUsersOWSUser](media/469a4b61-68bd-4ab0-b612-ab6302973886.png)
  
Seuls les documents partagés à l’aide de la troisième option (partagés avec des **personnes spécifiques**) sont renvoyés par une requête de recherche `SharedWithUsersOWSUser` qui utilise la propriété. 

## <a name="searching-for-skype-for-business-conversations"></a>Recherche de conversations Skype entreprise

Vous pouvez utiliser la requête de mot clé suivante pour rechercher spécifiquement du contenu dans les conversations de Skype entreprise:

```
kind:im
```

Remarque la requête de recherche précédente renverra également des conversations à partir de Microsoft Teams. Pour éviter cela, vous pouvez limiter les résultats de la recherche pour inclure uniquement les conversations Skype entreprise à l’aide de la requête de mot clé suivante:

```
kind:im AND subject:conversation
```

La requête par mot clé précédente exclut les conversations dans Microsoft Teams, car les conversations de Skype entreprise sont enregistrées sous forme de messages électroniques dont la ligne d’objet commence par le mot «conversation».

Pour rechercher des conversations Skype entreprise qui se sont produites dans une plage de dates spécifique, utilisez la requête de mot clé suivante:

```
kind:im AND subject:conversation AND (received=startdate..enddate)
```

## <a name="search-tips-and-tricks"></a>Conseils et astuces pour la recherche

- Les recherches par mot-clé ne respectent pas la casse. Par exemple, **cat** et **CAT** renvoient les mêmes résultats. 
    
- Les opérateurs booléens **and**, **or**, **not**, **near**et **ONEAR** doivent être en majuscules. 
    
- Un espace entre deux mots-clés ou deux expressions  `property:value` revient au même que d'utiliser l'opérateur **AND**. Par exemple, `from:"Sara Davis" subject:reorganization` renvoie tous les messages envoyés par Sara Davis qui contiennent le mot Reorganization dans la ligne d’objet. 
    
- Utilisez la syntaxe correspondant au format  `property:value`. Les valeurs ne respectent pas la casse et doivent être collées à l'opérateur. Si un espace est présent, la valeur prévue fera l’objet d’une recherche en texte intégral. Par exemple `to: pilarp` , recherche «pilarp» comme mot clé, plutôt que pour les messages qui ont été envoyés à pilarp. 
    
- Lorsque vous lancez une recherche sur une propriété de destinataire, telle que To, From, Cc ou Recipients, vous pouvez utiliser une adresse SMTP, un alias ou un nom d'affichage pour désigner un destinataire. Par exemple, vous pouvez saisir pilarp@contoso.com, pilarp ou « Pilar Pinilla ».
    
- Vous pouvez utiliser uniquement des recherches par caractères génériques avec préfixe; par exemple, **Cat\* ** ou **Set\***. Les recherches de suffixe ( ** \*Cat** ), les recherches d’infixe ( **\*c t** ) et les recherches de sous-chaînes ( ** \*Cat\* ** ) ne sont pas prises en charge. 
    
- Lorsque vous recherchez une propriété, utilisez des guillemets doubles ("") si la valeur de recherche se compose de plusieurs mots. Par exemple `subject:budget Q1` , renvoie les messages qui contiennent le **budget** dans la ligne d’objet et qui contiennent **Q1** Anywhere dans le message ou dans n’importe quelle propriété du message. À `subject:"budget Q1"` l’aide de renvoie tous les messages contenant le **budget Q1** n’importe où dans la ligne d’objet. 
    
- Pour exclure de vos résultats de recherche du contenu marqué avec une certaine valeur de propriété, placez un signe moins (-) avant le nom de la propriété. Par exemple, `-from:"Sara Davis"` exclut tous les messages envoyés par Sara Davis.

- Certains caractères spéciaux ne sont pas inclus dans l’index de recherche et, par conséquent, ne peuvent pas faire l’objet d’une recherche, ils incluent les opérateurs de recherche (+-=:) et les caractères suivants, qui sont remplacés par un $null, peuvent provoquer des erreurs si elles sont recherchées. @ #% ^ &; _ / ?

- Vous pouvez exporter des éléments en fonction du type de message. Par exemple, pour exporter des conversations Skype et des conversations dans Microsoft Teams, utilisez `kind:im`la syntaxe. Pour renvoyer uniquement les messages électroniques, utilisez `kind:email`. Pour renvoyer des conversations, des réunions et des appels dans Microsoft teams `kind:microsoftteams`, utilisez.
