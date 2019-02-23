---
title: Archivage de données tierces dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 9/5/2017
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid: MOE150
ms.assetid: 0ce338d5-3666-4a18-86ab-c6910ff408cc
description: Les administrateurs peuvent importer des données tierces à partir de plateformes de réseaux sociaux, de plateformes de messagerie instantanée et de documents de collaboration vers des boîtes aux lettres de votre organisation Office 365. Cela vous permet d'archiver des données à partir de Facebook, de Twitter et des sources de données dans Office 365. Vous pouvez ensuite appply les fonctionnalités de conformité d'Office 365 (telles que la conservation légale, la recherche de contenu et les stratégies de rétention) aux données tierces.
ms.openlocfilehash: 37811fdbee52cf956c6371deea53a242c2a3c550
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218494"
---
# <a name="archiving-third-party-data-in-office-365"></a>Archivage de données tierces dans Office 365

Office 365 permet aux administrateurs d'importer et d'archiver des données tierces à partir de plateformes de médias sociaux, de plateformes de messagerie instantanée et de plateformes de collaboration sur des documents, vers des boîtes aux lettres de votre organisation Office 365. Voici des exemples de sources de données tierces que vous pouvez importer dans Office 365: 
  
- **Social** -Twitter, Facebook, Yammer et LinkedIn 
    
- **Messagerie instantanée** -Yahoo Messenger, GoogleTalk et Cisco Jabber 
    
- **Collaboration** sur les documents-zone et boîte de dépôt 
    
- **Industries verticales** -gestion de la relation client (par exemple, Salesforce chatter) et finances (par exemple, Thomson Reuters et Bloomberg) 
    
- **SMS/Text Messaging** -BlackBerry 
    
Une fois les données tierces importées, vous pouvez appliquer les fonctionnalités de conformité d'Office 365, telles que la conservation pour litige, la recherche de contenu, l'archivage inaltérable, l'audit et les stratégies de rétention d'Office 365, à ces données. Par exemple, lorsqu'une boîte aux lettres est placée en conservation pour litige, les données tierces sont conservées. Vous pouvez rechercher des données tierces à l'aide de la recherche de contenu. Vous pouvez également appliquer des stratégies d'archivage et de rétention à des données tierces, comme vous pouvez le faire pour Microsoft Data. En bref, l'archivage des données tierces dans Office 365 peut aider votre organisation à respecter les stratégies gouvernementales et réglementaires.
  
Voici une vue d'ensemble du processus et des étapes nécessaires à l'importation de données tierces dans Office 365.

[Étape 1 : trouver un partenaire de données tierces](#step-1-find-a-third-party-data-partner)

[Étape 2 : créer et configurer une boîte aux lettres pour les données tierces dans Office 365](#step-2-create-and-configure-a-third-party-data-mailbox-in-office-365)

[Étape 3 : configurer des boîtes aux lettres d’utilisateurs pour les données tierces](#step-3-configure-user-mailboxes-for-third-party-data)

[Étape 4 : fournir des informations au partenaire](#step-4-provide-your-partner-with-information)

[Étape 5: enregistrer le connecteur de données tiers dans Azure Active Directory](#step-5-register-the-third-party-data-connector-in-azure-active-directory)

## <a name="how-the-third-party-data-import-process-works"></a>Works> du processus d'importation de données tierces

L’illustration et la description suivantes expliquent le fonctionnement du processus d’importation de données tierces.
  
![Fonctionnement du processus d’importation de données tierces](media/5d4cf8e9-b4cc-4547-90c8-d12d04a9f0e7.png)
  
1. Le client travaille avec son partenaire de choix pour configurer un connecteur qui extraira les éléments de la source de données tierce, puis importez ces éléments dans Office 365.
    
2. Le connecteur partenaire se connecte à des sources de données tierces via une API tierce (sur la base planifiée ou configurée) et extrait des éléments de la source de données. Le connecteur partenaire convertit le contenu d'un élément au format d'un message électronique. Consultez la section [more information](#more-information) pour obtenir une description du schéma de format des messages. 
    
3. Le connecteur partenaire se connecte au service Azure dans Office 365 à l'aide du service Web Exchange (EWS) via un point de terminaison connu.
    
4. Les éléments sont importés dans la boîte aux lettres d’un utilisateur spécifique ou dans une boîte aux lettres « fourre-tout » destinée aux données tierces. L’importation d’un élément dans la boîte aux lettres d’un utilisateur spécifique ou dans la boîte aux lettres de données tierces repose sur les critères suivants :
    
    a. **items qui possèdent un ID d'utilisateur correspondant à un compte d'utilisateur Office 365** -si le connecteur partenaire peut mapper l'ID utilisateur de l'élément de la source de données tierce à un ID d'utilisateur spécifique dans Office 365, l'élément est copié **** dans le dossier purges de l'utilisateur. Dossier éléments récupérables. Les utilisateurs ne peuvent pas accéder aux éléments du dossier de purges. Toutefois, vous pouvez utiliser les outils eDiscovery d'Office 365 pour rechercher des éléments dans le dossier purges.
    
    b. **éléments qui n'ont pas d'identifiant utilisateur correspondant à un compte d'utilisateur office 365** -si le connecteur partenaire ne peut pas mapper l'ID utilisateur d'un élément sur un ID d'utilisateur spécifique dans Office 365, l'élément est copié dans le dossier boîte de **réception** de la boîte aux lettres de données tierce. L'importation d'éléments dans la boîte de réception vous permet, ou une personne de votre organisation, de se connecter à la boîte aux lettres tierce pour afficher et gérer ces éléments, et de voir si des ajustements doivent être effectués dans la configuration du connecteur partenaire.
 
## <a name="step-1-find-a-third-party-data-partner"></a>Étape 1 : trouver un partenaire de données tierces

Un composant clé pour l'archivage de données tierces dans Office 365 est de trouver et d'utiliser un partenaire Microsoft spécialisé dans la capture de données à partir d'une source de données tierce et l'importation dans Office 365. Une fois les données importées, elles peuvent être archivées et conservées avec les autres données Microsoft de votre organisation, telles que les messages électroniques provenant d'Exchange et de documents provenant de SharePoint et OneDrive entreprise. Un partenaire crée un connecteur qui extrait les données des sources de données tierces de votre organisation (par exemple, BlackBerry, Facebook, Google +, Thomson Reuters, Twitter et YouTube) et transmet ces données à une API Office 365 qui importe des éléments dans les boîtes aux lettres Exchange en tant que messages électroniques. 
  
Les sections suivantes répertorient les partenaires Microsoft et les sources de données tierces qu'ils prennent en charge, qui participent au programme d'archivage de données tierces dans Office 365.

[17a-4 LLC](#17a-4-llc)
  
[Actiance](#actiance)
  
[ArchiveSocial](#archivesocial)
  
[Globanet](#globanet)
  
[OpenText](#opentext)
  
[Verba](#verba)
  
### <a name="17a-4-llc"></a>17a-4 LLC

17a-4 LLC prend en charge les sources de données tierces suivantes :
  
- BlackBerry
    
- Flux de données Bloomberg
    
- Cisco Jabber
    
- FactSet
    
- HipChat
    
- InvestEdge
    
- LivePerson
    
- 
Flux de données MessageLabs

    
- OpenText
    
- Aide en direct « cliquer pour appeler » Oracle/ATG

    
- Pivot IMTRADER

    
- Microsoft SharePoint
    
- MindAlign
    
- Sitrion One (Newsgator)
    
- 
Skype Entreprise (Lync/OCS)
    
- 
Skype Entreprise Online (Lync Online)

    
- Bases de données SQL
    
- 
Squawker

    
- Thomson Reuters Eikon Messenger

  
### <a name="actiance"></a>Actiance

[Actiance](https://www.actiance.com) prend en charge les sources de données tierces suivantes: 
  
- AIM
    
- American Idol
    
- Apple Juice
    
- 
AOL avec client Pivot

    
- Ares
    
- Bazaar Voice
    
- Bear Share
    
- Bit Torrent
    
- BlackBerry Call Logs (version 5, version 10, version 12)
    
- BlackBerry Messenger (version 5, version 10, version 12)
    
- BlackBerry PIN (version 5, version 10, version 12)
    
- BlackBerry SMS (version 5, version 10, version 12)
    
- Bloomberg Mail

    
- CellTrust
    
- Chat Import

    
- Chat Real Time Logging and Policy

    
- Chatter

    
- Serveur de &amp; présence de messagerie instantanée Cisco (version 9.0.1, version 9.1, v 9.1.1 Su1, version 10, v 10.5.1 Su1)
    
- Cisco Unified Presence Server (v8.6.3, v8.6.4, v8.6.5)

    
- Collaboration Import

    
- Collaboration Real Time Logging

    
- Direct Connect
    
- Facebook
    
- FactSet
    
- FastTrack
    
- Gnutella
    
- Google+

    
- GoToMyPC
    
- Hopster
    
- HubConnex
    
- IBM Connections (version 3.0.1, version 4.0, version 4.5, version 4.5 CR3, version 5)

    
- IBM Connections Chat Cloud

    
- IBM Connections Social Cloud

    
- IBM SameTime Advanced 8.5.2 IFR1

    
- IBM SameTime Communicate 9.0

    
- IBM SameTime Community (version 8.0.2, version 8.5.1 IFR2, version 8.5.2 IFR1, version 9.1)

    
- IBM SameTime Complete 9.0

    
- IBM SameTime Conference 9.0

    
- IBM SameTime Meeting 8.5.2 IFR1

    
- GLACE/YellowJacket
    
- IM Import

    
- IM Real Time Logging and Policy

    
- Indii Messenger

    
- Instant Bloomberg

    
- IRC
    
- Jive

    
- Jive 6 Real Time Logging (version 6, version 7)

    
- Jive Import
    
- JXTA
    
- LinkedIn
    
- 
Microsoft Lync (2010, 2013)

    
- MFTP
    
- Microsoft Lync 2013 Voix

    
- Microsoft SharePoint (2010, 2013)

    
- Microsoft SharePoint Online
    
- Microsoft UC (Unified Communications)
    
- MindAlign
    
- Mobile Guard
    
- MSN
    
- My Space
    
- NEONetwork
    
- Office 365 Lync dédié

    
- MI partagée Office 365

    
- Pinterest
    
- Pivot
    
- QQ
    
- Skype Entreprise 2015
    
- SoftEther
    
- Symphony

    
- Thomson Reuters Eikon

    
- Thomson Reuters Messenger

    
- Tor
    
- TTT
    
- Twitter
    
- WinMX
    
- Winny
    
- Yahoo

    
- Yammer
    
- YouTube
    
  
### <a name="archivesocial"></a>ArchiveSocial

[ArchiveSocial](https://www.archivesocial.com) prend en charge les sources de données tierces suivantes: 
  
- Facebook
    
- Flickr

    
- Instagram

    
- LinkedIn
    
- Pinterest
    
- Twitter
    
- YouTube
    
- Vimeo
  
### <a name="globanet"></a>Globanet

[Globanet](https://www.globanet.com) prend en charge les sources de données tierces suivantes: 
  
- AOL avec client Pivot  
    
- BlackBerry Call Logs (version 5, version 10, version 12)
    
- BlackBerry Messenger (version 5, version 10, version 12)
    
- BlackBerry PIN (version 5, version 10, version 12)
    
- BlackBerry SMS (version 5, version 10, version 12)
    
- Bloomberg Chat

    
- Bloomberg Mail

    
- Box
    
- CipherCloud for Salesforce Chatter
    
- Serveur de &amp; présence de messagerie instantanée Cisco (version 10, v 10.5.1 Su1, v 11.0, v 11.5 SU2)

- Teams de Cisco Webex

- ShareFile de &amp; l'espace de travail de Citrix

- CrowdCompass

- Fichiers texte délimités personnalisés

    
- Fichiers XML personnalisés

    
- Facebook (pages)
    
- Factset

    
- FXConnect
    
- ICE Chat/YellowJacket
    
- Jive

    
- Macgregor XIP


- Microsoft Exchange Server
    
- Microsoft OneDrive Entreprise

- Microsoft Teams
       
- Microsoft Yammer

    
- Mobile Guard
    
- Pivot
    
- Salesforce Chatter

- Skype Entreprise Online
    
- Skype Entreprise, versions 2007 R2-2016 (sur site)

    
- Slack Enterprise Grid
    
- Symphony

    
- Thomson Reuters Eikon

    
- Thomson Reuters Messenger

    
- Thomson Reuters Dealings 3000/FX Trading

    
- Twitter
    
- UBS Chat

    
- YouTube
  
### <a name="opentext"></a>OpenText

[OpenText](https://www.opentext.com/what-we-do/products/opentext-product-offerings-catalog/rebranded-products/daegis) prend en charge les sources de données tierces suivantes: 
  
- Axs Encrypted
    
- Axs Exchange
    
- Axs Local Archive
    
- Axs PlaceHolder
    
- Axs Signed
    
- Bloomberg
    
- Thomson Reuters
  
### <a name="verba"></a>Verba

[Verba](https://www.verba.com) prend en charge les sources de données tierces suivantes: 
  
- Avaya Aura Video

    
- Avaya Aura Voice

    
- Avtec Radio

    
- Bosch/Telex Radio

    
- BroadSoft Video

    
- BroadSoft Voice

    
- Centile Voice

    
- Cisco Jabber IM

    
- Cisco UC Video

    
- Cisco UC Voice

    
- Cisco UCCX/UCCE vidéo
    
- Cisco UCCX/UCCE Voice
    
- ESChat Radio
    
- Geoman Contact Expert
    
- IP Trade Voice

    
- Luware LUCS Contact Center
    
- Microsoft UC (Unified Communications)
    
- Mitel MiContact Center for Lync (prairieFyre) 

    
- Oracle / Acme Packet Session Border Controller Video  

    
- Oracle / Acme Packet Session Border Controller Voice

    
- Singtel Mobile Voice

    
- SIPREC Video
    
-  SIPREC Voice 
    
- Skype Entreprise / MI Lync

    
- Skype Entreprise / Vidéo Lync

    
- Skype Entreprise / Voix Lync

    
- Speakerbus Voice

    
- Standard SIP/H.323 Video 

    
- Standard SIP/H.323 Voice 

    
- Truphone Voice

    
- TwistedPair Radio

    
- Écran d’ordinateur de bureau Windows 

  
## <a name="step-2-create-and-configure-a-third-party-data-mailbox-in-office-365"></a>Étape 2 : créer et configurer une boîte aux lettres pour les données tierces dans Office 365

Voici les étapes à suivre pour créer et configurer une boîte aux lettres de données tierce pour l'importation de données dans Office 365. Comme expliqué précédemment, les éléments sont importés dans cette boîte aux lettres si le connecteur partenaire ne peut pas mapper l'ID utilisateur de l'élément sur un compte d'utilisateur Office 365.
  
 **Effectuer ces tâches dans le centre d'administration Office 365**
  
1. Créez un compte d'utilisateur dans Office 365 et attribuez-lui une licence Exchange Online plan 2; Voir [Ajouter des utilisateurs à Office 365](https://go.microsoft.com/fwlink/p/?LinkId=692098). Une licence plan 2 est nécessaire pour placer la boîte aux lettres en conservation pour litige ou pour activer une boîte aux lettres d'archivage dont le quota de stockage est illimité.
    
2. Ajoutez le compte d'utilisateur pour la boîte aux lettres de données tierce au rôle d'administrateur d' **administrateur Exchange** dans Office 365; consultez la rubrique asSigner [des rôles d'administrateur dans Office 365](https://go.microsoft.com/fwlink/p/?LinkId=532393).
    
    > [!TIP]
    > Notez les informations d’identification pour ce compte d’utilisateur. Vous devez les fournir à votre partenaire, comme décrit à l’étape 4. 
  
 **Effectuer ces tâches dans le centre d'administration Exchange**
  
1. Masquer la boîte aux lettres de données tierce dans le carnet d'adresses et les autres listes d'adresses de votre organisation; consultez la rubrique [Manage User mailboxes](https://go.microsoft.com/fwlink/p/?LinkId=616058). Vous pouvez également exécuter la commande PowerShell suivante:
    
    ```
    Set-Mailbox -Identity <identity of third-party data mailbox> -HiddenFromAddressListsEnabled $true
    ```

2. Attribuer l'autorisation **FullAccess** à la boîte aux lettres de données tierce afin que les administrateurs ou les responsables de la mise en conformité puissent ouvrir la boîte aux lettres de données tierce dans le client de bureau Outlook; consultez la rubrique [Manage Permissions for Recipients](https://go.microsoft.com/fwlink/p/?LinkId=692104).
    
3. Activez les fonctionnalités suivantes d'Office 365 liées à la conformité pour la boîte aux lettres de données tierce:
    
    - Activer la boîte aux lettres d'archivage; consultez [la rubrique activation des boîtes aux lettres d'archivage dans le centre de sécurité &amp; conformité Office 365](enable-archive-mailboxes.md) et activez un archivage [illimité dans Office 365](enable-unlimited-archiving.md). Cela vous permettra de libérer de l'espace de stockage dans la boîte aux lettres principale en configurant une stratégie d'archivage qui déplace les éléments de données tiers vers la boîte aux lettres d'archivage. Vous bénéficierez ainsi d'un stockage illimité pour les données tierces.
    
    - Placez la boîte aux lettres de données tierce en conservation pour litige. Vous pouvez également appliquer une stratégie de rétention Office 365 dans le &amp; Centre de sécurité conformité Office 365. La mise en attente de cette boîte aux lettres permet de conserver des éléments de données tiers (indéfiniment ou pour une durée spécifiée) et de les empêcher d'être purgés de la boîte aux lettres. Consultez l'une des rubriques suivantes:
    
      - [Place a mailbox on Litigation Hold](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
      - [Vue d'ensemble des stratégies de rétention](retention-policies.md)
    
       
    
    - Activez l'enregistrement d'audit des boîtes aux lettres pour l'accès des propriétaires, des délégués et des administrateurs à la boîte aux lettres de données tierce. consultez la rubrique [activer l'audit de boîte aux lettres dans Office 365](enable-mailbox-auditing.md). Cela vous permettra d'auditer toutes les activités effectuées par les utilisateurs ayant accès à la boîte aux lettres de données tierce.

## <a name="step-3-configure-user-mailboxes-for-third-party-data"></a>Étape 3 : configurer des boîtes aux lettres d’utilisateurs pour les données tierces

L'étape suivante consiste à configurer des boîtes aux lettres d'utilisateurs pour prendre en charge des données tierces. Effectuez ces tâches à l'aide du centre d'administration Exchange ou à l'aide des applets de commande Windows PowerShell correspondantes.
  
1. Activez la boîte aux lettres d'archivage pour chaque utilisateur; consultez [la rubrique activation des boîtes aux lettres d'archivage dans le centre de sécurité &amp; conformité Office 365](enable-archive-mailboxes.md) et activez un archivage [illimité dans Office 365](enable-unlimited-archiving.md).
    
2. Placer les boîtes aux lettres utilisateur en conservation pour litige ou appliquer une stratégie de rétention Office 365; consultez l'une des rubriques suivantes: 
    
    - [Place a mailbox on Litigation Hold](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
    - [Vue d'ensemble des stratégies de rétention](retention-policies.md)
    
    Comme indiqué précédemment, lorsque vous placez des boîtes aux lettres en conservation, vous pouvez définir la durée de conservation des éléments de la source de données tierces ou vous pouvez choisir de les conserver indéfiniment.

## <a name="step-4-provide-your-partner-with-information"></a>Étape 4 : fournir des informations au partenaire

La dernière étape consiste à fournir à votre partenaire les informations suivantes pour lui permettre de configurer le connecteur afin qu’il se connecte à votre organisation Office 365 pour importer les données vers les boîtes aux lettres des utilisateurs et la boîte aux lettres de données tierces. 
  
- Le point de terminaison utilisé pour se connecter au service Azure dans Office 365:

    ```
    https://office365ingestionsvc.gble1.protection.outlook.com/service/ThirdPartyIngestionService.svc
    ```

- Les informations d'identification de connexion (ID d'utilisateur et mot de passe Office 365) de la boîte aux lettres de données tierce que vous avez créée à l'étape 2. Ces informations d'identification sont requises pour que le connecteur partenaire puisse accéder à des éléments et les importer dans des boîtes aux lettres utilisateur et dans la boîte aux lettres de données tierce.
 
## <a name="step-5-register-the-third-party-data-connector-in-azure-active-directory"></a>Étape 5: enregistrer le connecteur de données tiers dans Azure Active Directory

À partir du 30 septembre 2018, le service Azure d'Office 365 commencera à utiliser l'authentification moderne dans Exchange Online pour authentifier les connecteurs de données tiers qui tentent de se connecter à votre organisation Office 365 pour importer des données. La raison de cette modification est que l'authentification moderne offre davantage de sécurité que la méthode actuelle, basée sur des connecteurs tiers de liste d'accès aux utilisateurs qui utilisent le point de terminaison décrit précédemment pour se connecter au service Azure.

Pour permettre à un connecteur de données tiers de se connecter à Office 365 à l'aide de la nouvelle méthode d'authentification moderne, un administrateur de votre organisation Office 365 doit consentir à inscrire le connecteur en tant qu'application de service approuvée dans Azure Active Directory. Pour ce faire, vous devez accepter une demande d'autorisations pour permettre au connecteur d'accéder aux données de votre organisation dans Azure Active Directory. Une fois que vous avez accepté cette demande, le connecteur de données tiers est ajouté en tant qu'application d'entreprise à Azure Active Directory et représenté en tant que principal de service. Pour plus d'informations sur le processus de consentement, consultez la rubrique consentement de l' [administrateur client](https://docs.microsoft.com/en-us/skype-sdk/trusted-application-api/docs/tenantadminconsent).

Voici les étapes à suivre pour accéder à la demande et l'accepter pour enregistrer le connecteur:

1. Accédez à [cette page](https://login.microsoftonline.com/common/oauth2/authorize?client_id=8dfbc50b-2111-4d03-9b4d-dd0d00aae7a2&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent) et connectez-vous à l'aide des informations d'identification d'un administrateur général Office 365.<br/><br/>La boîte de dialogue suivante s'affiche. Vous pouvez développer les signes pour vérifier les autorisations qui seront affectées au connecteur.<br/><br/>![La boîte de dialogue demande d'autorisations s'affiche.](media/O365_ThirdPartyDataConnector_OptIn1.png)
2. Cliquez sur **accepter**.

Une fois que vous avez accepté la demande, le [portail Azure](https://portal.azure.com) s'affiche. Pour afficher la liste des applications pour votre organisation, cliquez sur**applications d'entreprise** **Azure Active Directory** > . Le connecteur de données tiers 365 Office est affiché dans le panneau **applications d'entreprise** .

> [!IMPORTANT]
> Après le 30 septembre 2018, les données tierces ne seront plus importées dans les boîtes aux lettres de votre organisation si vous n'enregistrez pas un connecteur de données tiers dans Azure Active Directory. Remarque les connecteurs de données tiers existants (ceux créés avant le 30 septembre 2018) doivent également être enregistrés dans Azure Active Directory en suivant la procédure de l'étape 5.

### <a name="revoking-consent-for-a-third-party-data-connector"></a>Révocation du consentement pour un connecteur de données tiers

Une fois que votre organisation a accepté la demande d'autorisations pour enregistrer un connecteur de données tiers dans Azure Active Directory, votre organisation peut révoquer ce consentement à tout moment. Toutefois, la révocation de l'autorisation pour un connecteur signifie que les données de la source de données tierce ne seront plus importées dans Office 365.

Pour révoquer le consentement d'un connecteur de données tiers, vous pouvez supprimer l'application (en supprimant l'entité de service correspondante) à partir d'Azure Active Directory à l'aide du panneau **applications d'entreprise** dans le portail Azure ou à l'aide de l' [ Remove-MsolServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/msonline/remove-msolserviceprincipal) dans Office 365 PowerShell. Vous pouvez également utiliser l'applet de commande [Remove-AzureADServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/azuread/remove-azureadserviceprincipal) dans Azure Active Directory PowerShell.
  
## <a name="more-information"></a>Plus d’informations

- Comme indiqué précédemment, les éléments provenant de sources de données tierces sont importés dans les boîtes aux lettres Exchange sous forme de messages électroniques. Le connecteur partenaire importe l'élément à l'aide d'un schéma requis par l'API Office 365. Le tableau suivant décrit les propriétés de message d'un élément provenant d'une source de données tierce après qu'il a été importé dans une boîte aux lettres Exchange sous la forme d'un message électronique. Le tableau indique également si la propriété message est obligatoire. Les propriétés obligatoires doivent être renseignées. Si une propriété obligatoire est manquante dans un élément, celui-ci ne sera pas importé dans Office 365. Le processus d'importation renvoie un message d'erreur expliquant pourquoi un élément n'a pas été importé et quelle est la propriété manquante.
    
    |**Propriété de message**|**Compléter?**|**Description**|**Exemple de valeur**|
    |:-----|:-----|:-----|:-----|
    |**FROM** <br/> |Oui  <br/> |Utilisateur qui a initialement créé ou envoyé l'élément dans la source de données tierce. Le connecteur partenaire tentera de mapper l'ID utilisateur à partir de l'élément source (par exemple, un handle Twitter) vers un compte d'utilisateur Office 365 pour tous les participants (les utilisateurs figurant dans les champs de et à). Une copie du message sera importée dans la boîte aux lettres de chaque participant. Si aucun des participants de l'élément ne peut être mappé à un compte d'utilisateur Office 365, l'élément sera importé dans la boîte aux lettres d'archivage tierce dans Office 365.<br/> <br/> Le participant identifié comme l'expéditeur de l'élément doit disposer d'une boîte aux lettres active dans l'organisation Office 365 pour laquelle l'élément est importé. Si l'expéditeur ne dispose pas d'une boîte aux lettres active, l'erreur suivante est renvoyée:<br/><br/>  `One or more messages in the Request failed to be delivered to either From or Sender email address. You will need to resend your entire Request. Error: The request failed. The remote server returned an error: (401) Unauthorized.`  | `bob@contoso.com` <br/> |
    |**TO** <br/> |Oui  <br/> |Utilisateur qui a reçu un élément, le cas échéant, pour un élément dans la source de données.  <br/> | `bob@contoso.com` <br/> |
    |**SUBJECT** <br/> |Non  <br/> |Objet de l’élément source.  <br/> | `"Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/> |
    |**JOURS** <br/> |Oui  <br/> |Date à laquelle l’élément a été initialement créé ou publié dans la source de données du client, par exemple, date à laquelle un message Twitter a été publié.  <br/> | `01 NOV 2015` <br/> |
    |**BODY** <br/> |Non  <br/> |Le contenu du message ou de la publication. Pour certaines sources de données, le contenu de cette propriété peut être le même que celui de la propriété **Subject** . Pendant le processus d'importation, le connecteur partenaire tentera de maintenir la fidélité complète de la source de contenu le cas échéant. Si des fichiers, des graphismes ou d'autres contenus possibles du corps de l'élément source sont inclus dans cette propriété. Dans le cas contraire, le contenu de l'élément source **** est inclus dans la propriété Attachment. Le contenu de cette propriété dépend du connecteur du partenaire et de la capacité de la plateforme source.<br/> | `Author: bob@contoso.com` <br/>  `Date: 10 DEC 2014` <br/>  `Tweet: "Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/>  `Date: 01 NOV 2015` <br/> |
    |**ATTACHMENT** <br/> |Non  <br/> |Si un élément de la source de données (par exemple, un tweet dans Twitter ou une conversation de messagerie instantanée) a un fichier joint ou inclut des images, le partenaire Connect tente d'abord d'inclure les pièces jointes dans la propriété **Body** . Si cela n'est pas possible, il est ajouté à la propriété * * ATTACHment * *. Voici d'autres exemples de pièces jointes: J'aime dans Facebook, les métadonnées de la source de contenu et les réponses à un message ou une publication.<br/> | `image.gif` <br/> |
    |**MESSAGECLASS** <br/> |Oui  <br/> | Il s'agit d'une propriété à valeurs multiples, qui est créée et remplie par le connecteur du partenaire. Le format de cette propriété est `IPM.NOTE.Source.Event`. (Cette propriété doit commencer par `IPM.NOTE`; ce format est similaire à celui de la `IPM.NOTE.X` classe de message.) Cette propriété inclut les informations suivantes:<br/><br/>`Source`-Indique la source de données tierce; par exemple, Twitter, Facebook ou BlackBerry.  <br/> <br/>  `Event`-Indique le type d'activité qui a été effectué dans la source de données tierce qui a produit les éléments; par exemple, un tweet dans Twitter ou un billet dans Facebook. Les événements sont spécifiques à la source de données.<br/> <br/>  L'un des objectifs de cette propriété est de filtrer des éléments spécifiques en fonction de la source de données à partir de laquelle un élément est issu ou sur la base du type d'événement. Par exemple, dans une recherche de découverte électronique, vous pouvez créer une requête de recherche pour rechercher tous les tweets publiés par un utilisateur spécifique.<br/> | `IPM.NOTE.Twitter.Tweet` <br/> |
   
- Lorsque des éléments sont correctement importés dans des boîtes aux lettres dans Office 365, un identificateur unique est renvoyé à l'appelant dans le cadre de la réponse HTTP. Cet identificateur, appelé `x-IngestionCorrelationID`, peut être utilisé à des fins de dépannage ultérieure par les partenaires pour le suivi de bout en bout des éléments. Il est recommandé aux partenaires de capturer ces informations et de les enregistrer en conséquence à leur bout. Voici un exemple de réponse HTTP illustrant cet identificateur:

    ```
    HTTP/1.1 200 OK
    Content-Type: text/xml; charset=utf-8
    Server: Microsoft-IIS/8.5
    x-IngestionCorrelationID: 1ec7667d-f097-47fe-a9a2-bc7ab0a7552b
    X-AspNet-Version: 4.0.30319
    X-Powered-By: ASP.NET
    Date: Tue, 02 Feb 2016 22:55:33 GMT 
    ```
 
- Vous pouvez utiliser l'outil de recherche de contenu dans le centre &amp; de sécurité conformité Office 365 pour rechercher des éléments qui ont été importés dans des boîtes aux lettres dans Office 365 à partir d'une source de données tierce. Pour rechercher spécifiquement ces éléments importés, vous pouvez utiliser les paires de propriétés-valeur de message suivantes dans la zone de mot clé pour une recherche de contenu. . 
    
  - **`kind:externaldata`**-Utilisez cette paire de valeurs de propriété pour rechercher tous les types de données tiers. Par exemple, pour rechercher des éléments qui ont été importés à partir d'une source de données tierce et contenant le mot «Contoso» dans la propriété Subject de l'élément importé, vous devez `kind:externaldata AND subject:contoso`utiliser la requête par mot clé.
    
  - **`itemclass:ipm.externaldata.<third-party data type>`**-Utilisez cette paire de valeur de propriété pour rechercher uniquement un type de données tierces. Par exemple, pour rechercher uniquement les données Facebook qui contiennent le mot «Contoso» dans la propriété Subject, vous devez utiliser la requête `itemclass:ipm.externaldata.Facebook* AND subject:contoso`par mot clé. 

  Pour obtenir la liste complète des valeurs à utiliser pour les types de données tiers pour `itemclass` la propriété, reportez-vous à la rubrique [utiliser la recherche de contenu pour rechercher des données tierces importées dans Office 365](use-content-search-to-search-third-party-data-that-was-imported.md)
    
   Pour plus d’informations sur l’utilisation de la recherche de contenu et la création de requêtes de recherche de mots clés, voir :
    
  - [Recherche de contenu dans Office 365](content-search.md)
    
  - [Requêtes par mots clés et conditions de recherche pour la recherche de contenu](keyword-queries-and-search-conditions.md)
 
