---
title: Archivage de données tierces dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 9/5/2017
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 0ce338d5-3666-4a18-86ab-c6910ff408cc
description: Les administrateurs peuvent importer des données tierces à partir de plateformes de médias sociaux, plates-formes de messagerie instantanées et plates-formes de collaboration de documents aux boîtes aux lettres dans votre organisation Office 365. Cela vous permet d’archiver des données à partir de Facebook, Twitter et sources de données dans Office 365. Vous pouvez ensuite appply des fonctionnalités de conformité d’Office 365 (telles que la conservation légale, recherche de contenu et les stratégies de rétention) à des données tierces.
ms.openlocfilehash: f5590d170986b8ae69458e69cedeb8a0ef137ef4
ms.sourcegitcommit: 81c2fd5cd940c51bc43ac7858c7bdfa207ce401a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2018
ms.locfileid: "23809709"
---
# <a name="archiving-third-party-data-in-office-365"></a>Archivage de données tierces dans Office 365

Permet d’Office 365 administrateurs importer et archiver des données tierces à partir de plateformes de médias sociaux, de messagerie instantanée plateformes et plates-formes de collaboration de documents, aux boîtes aux lettres dans votre organisation Office 365. Exemples de tiers de sources de données que vous pouvez importer dans Office 365 sont les suivantes : 
  
- **Mise en réseau** - Twitter, Facebook, Yammer et LinkedIn 
    
- **Messagerie instantanée** - Yahoo Messenger, GoogleTalk et Cisco Jabber 
    
- **Collaboration sur des documents** - zone et échange 
    
- **Secteurs verticaux** - Finance (comme Thomson Reuters et Bloomberg) et gestion des relations client (par exemple, brouillage force de vente) 
    
- **Messagerie texte/SMS** - BlackBerry 
    
Après l’importation des données tierces, vous pouvez appliquer des fonctionnalités de conformité d’Office 365, telles que les stratégies de rétention litige, recherche de contenu, d’archivage sur Place, audit et Office 365 — à ces données. Par exemple, lorsqu’une boîte aux lettres est mis en attente pour litige, des données tierces seront préservées. Vous pouvez rechercher des données tierces à l’aide de la recherche de contenu. Ou vous pouvez appliquer l’archivage et les stratégies de rétention pour des données tierces comme vous pouvez utiliser pour les données de Microsoft. En bref, l’archivage des données tierces dans Office 365 peut aider votre organisation respecter les administrations et réglementaires.
  
Voici une vue d’ensemble du processus et les étapes nécessaires pour importer des données de tiers pour Office 365.

[Étape 1 : trouver un partenaire de données tierces](#step-1-find-a-third-party-data-partner)

[Étape 2 : créer et configurer une boîte aux lettres pour les données tierces dans Office 365](#step-2-create-and-configure-a-third-party-data-mailbox-in-office-365)

[Étape 3 : configurer des boîtes aux lettres d’utilisateurs pour les données tierces](#step-3-configure-user-mailboxes-for-third-party-data)

[Étape 4 : fournir des informations au partenaire](#step-4-provide-your-partner-with-information)

[Étape 5 : Enregistrer le connecteur des données tierces dans Azure Active Directory](#step-5-register-the-third-party-data-connector-in-azure-active-directory)

## <a name="how-the-third-party-data-import-process-works"></a>Fonctionnement de la façon dont les données tiers processus d’importation >

L’illustration et la description suivantes expliquent le fonctionnement du processus d’importation de données tierces.
  
![Fonctionnement du processus d’importation de données tierces](media/5d4cf8e9-b4cc-4547-90c8-d12d04a9f0e7.png)
  
1. Client fonctionne avec leur partenaire de choix pour configurer un connecteur d’extraire des éléments de la source de données tierce et puis importez ces éléments vers Office 365.
    
2. Le connecteur de partenaire se connecte aux sources de données de tiers via une API de tiers (sur une base planifiée ou configuré en tant que) et extrait les éléments de la source de données. Le connecteur de partenaire convertit le contenu d’un élément dans un format de message électronique. Voir la section [plus d’informations](#more-information) pour une description du schéma de format de message. 
    
3. Connecteur de partenaire se connecte au service Azure dans Office 365 à l’aide d’Exchange Web Services (EWS) par le biais d’un point de terminaison connu.
    
4. Les éléments sont importés dans la boîte aux lettres d’un utilisateur spécifique ou dans une boîte aux lettres « fourre-tout » destinée aux données tierces. L’importation d’un élément dans la boîte aux lettres d’un utilisateur spécifique ou dans la boîte aux lettres de données tierces repose sur les critères suivants :
    
    **éléments qui ont un ID d’utilisateur qui correspond à un compte d’utilisateur Office 365** - si le connecteur de partenaire pouvez mapper l’ID utilisateur de l’élément dans la source de données tiers à un utilisateur spécifique ID dans Office 365, l’élément est copié dans le dossier de **purge** de l’utilisateur d’a. Dossier éléments récupérables. Les utilisateurs ne peuvent pas accéder aux éléments dans le dossier de purge. Toutefois, vous pouvez utiliser les outils de découverte électronique Office 365 pour rechercher des éléments dans le dossier de purge.
    
    b. **les éléments qui n’ont pas un ID d’utilisateur qui correspond à un compte d’utilisateur Office 365** - si le connecteur de partenaire ne peut pas mapper l’ID utilisateur d’un élément à un utilisateur spécifique ID dans Office 365, l’élément est copié dans le dossier **boîte de réception** de la boîte aux lettres des données tierces. Importation d’éléments dans la boîte de réception permet de vous ou une personne de votre organisation à se connecter à la boîte aux lettres de tiers pour afficher et gérer ces éléments et voir si les modifications doivent être effectuées dans la configuration du connecteur partenaire.
 
## <a name="step-1-find-a-third-party-data-partner"></a>Étape 1 : trouver un partenaire de données tierces

Un composant essentiel pour l’archivage des données tierces dans Office 365 est recherche et utilisation d’un partenaire Microsoft spécialisée dans la capture des données à partir d’une source de données de tiers et importées dans Office 365. Une fois que les données sont importées, il peut être archivée et conservé avec votre organisation d’autres données Microsoft, tels que le courrier électronique à partir d’Exchange et des documents dans SharePoint et OneDrive for Business. Un partenaire crée un connecteur qui extrait les données à partir de sources de données tierces de votre organisation (tels que BlackBerry, Facebook, Google +, Reuters Thomson, Twitter et YouTube) et transmet les données à une API Office 365 qui importe les éléments dans les boîtes aux lettres Exchange en tant que les messages électroniques. 
  
Les sections suivantes répertorient les partenaires Microsoft et les sources de données tierces elles prennent en charge, qui participent au programme pour l’archivage des données tierces dans Office 365.

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

[Actiance](https://www.actiance.com) prend en charge les sources de données tierces suivantes : 
  
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

    
- Cisco par messagerie instantanée &amp; serveur de présence (v9.0.1, v9.1, v9.1.1 SU1, 10, v10.5.1 SU1)
    
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

    
- ICE/YellowJacket
    
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

[ArchiveSocial](https://www.archivesocial.com) prend en charge les sources de données tierces suivantes : 
  
- Facebook
    
- Flickr

    
- Instagram

    
- LinkedIn
    
- Pinterest
    
- Twitter
    
- YouTube
    
- Vimeo
  
### <a name="globanet"></a>Globanet

[Globanet](https://www.globanet.com) prend en charge les sources de données tierces suivantes : 
  
- AOL avec client Pivot  
    
- BlackBerry Call Logs (version 5, version 10, version 12)
    
- BlackBerry Messenger (version 5, version 10, version 12)
    
- BlackBerry PIN (version 5, version 10, version 12)
    
- BlackBerry SMS (version 5, version 10, version 12)
    
- Bloomberg Chat

    
- Bloomberg Mail

    
- Box

    
- CipherCloud for Salesforce Chatter
    
- Messagerie instantanée de Cisco &amp; serveur de présence (10, v10.5.1 SU1, v11.0, v11.5 SU2)

- Cisco Webex équipes

- Espace de travail Citrix &amp; ShareFile

- CrowdCompass

- Fichiers texte délimités personnalisés

    
- Fichiers XML personnalisés

    
- Facebook (Pages)
    
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

[OpenText](https://www.opentext.com/what-we-do/products/opentext-product-offerings-catalog/rebranded-products/daegis) prend en charge les sources de données tierces suivantes : 
  
- Axs Encrypted
    
- Axs Exchange
    
- Axs Local Archive
    
- Axs PlaceHolder
    
- Axs Signed
    
- Bloomberg
    
- Thomson Reuters
  
### <a name="verba"></a>Verba

[Verba](https://www.verba.com) prend en charge les sources de données tierces suivantes : 
  
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
    
- Cisco UCCX/UCCE vocale
    
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

Voici les étapes pour créer et configurer une boîte aux lettres de données tiers pour l’importation de données dans Office 365. Précédente comme expliqué, les éléments sont importés à cette boîte aux lettres si le connecteur de partenaire ne peut pas mapper l’ID de l’élément à un compte d’utilisateur Office 365.
  
 **Effectuer ces tâches dans le centre d’administration d’Office 365**
  
1. Créer un nouveau compte d’utilisateur dans Office 365 et l’attribuer une licence Exchange Online Plan 2 ; consultez la rubrique [Ajouter des utilisateurs à Office 365](https://go.microsoft.com/fwlink/p/?LinkId=692098). Une licence Plan 2 est requis pour placer la boîte aux lettres en conservation pour litige ou activer une boîte aux lettres d’archivage qui a un quota de stockage illimitée.
    
2. Ajoutez le compte d’utilisateur pour la boîte aux lettres des données tierces au rôle **administrateur Exchange** admin dans Office 365 ; consultez [assigner des rôles d’administrateur dans Office 365](https://go.microsoft.com/fwlink/p/?LinkId=532393).
    
    > [!TIP]
    > Notez les informations d’identification pour ce compte d’utilisateur. Vous devez les fournir à votre partenaire, comme décrit à l’étape 4. 
  
 **Effectuer ces tâches dans le centre d’administration Exchange**
  
1. Masquer la boîte aux lettres de données tiers à partir du carnet d’adresses et d’autres listes d’adresses dans votre organisation ; voir [Gérer les boîtes aux lettres](https://go.microsoft.com/fwlink/p/?LinkId=616058). Vous pouvez également exécuter la commande PowerShell suivante :
    
    ```
    Set-Mailbox -Identity <identity of third-party data mailbox> -HiddenFromAddressListsEnabled $true
    ```

2. Attribuer l’autorisation **FullAccess** pour la boîte aux lettres des données tierces pour que les administrateurs ou aux règlements puissent ouvrir la boîte aux lettres des données tierces dans le client de bureau Outlook ; voir [Gérer les autorisations pour les destinataires](https://go.microsoft.com/fwlink/p/?LinkId=692104).
    
3. Activer les fonctionnalités Office 365 suivantes relatives à la conformité pour la boîte aux lettres des données tierces :
    
    - Activer la boîte aux lettres d’archivage ; voir [Activer les boîtes aux lettres archive de sécurité Office 365 &amp; centre de conformité](enable-archive-mailboxes.md) et [Activer l’archivage illimité dans Office 365](enable-unlimited-archiving.md). Vous pouvez libérer de l’espace dans la boîte aux lettres principal en configurant une stratégie d’archivage qui déplace les éléments de données tierces dans la boîte aux lettres d’archive. Cela vous fournira stockage illimité pour les données de tiers.
    
    - Placez la boîte aux lettres des données tierces litige. Vous pouvez également appliquer une stratégie de rétention Office 365 de sécurité Office 365 &amp; centre de conformité. Placer cette boîte aux lettres en attente pour conserver des éléments de données de tiers (indéfiniment ou pendant une durée spécifiée) et les empêcher d’être purgées de la boîte aux lettres. Consultez les rubriques suivantes :
    
      - [Place a mailbox on Litigation Hold](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
      - [Vue d'ensemble des stratégies de rétention](retention-policies.md)
    
       
    
    - Activer la boîte aux lettres enregistrement d’audit pour un accès propriétaire, délégué et d’administration pour la boîte aux lettres des données tierces ; consultez la rubrique [Activer la boîte aux lettres de l’audit dans Office 365](enable-mailbox-auditing.md). Cela vous permettra d’auditer toutes les activités effectuées par les utilisateurs ayant accès à la boîte aux lettres des données tierces.

## <a name="step-3-configure-user-mailboxes-for-third-party-data"></a>Étape 3 : configurer des boîtes aux lettres d’utilisateurs pour les données tierces

L’étape suivante consiste à configurer les boîtes aux lettres pour prendre en charge des données tierces. Effectuer ces tâches à l’aide du centre d’administration Exchange ou à l’aide des applets de commande Windows PowerShell correspondant.
  
1. Activer la boîte aux lettres d’archive pour chaque utilisateur ; voir [Activer les boîtes aux lettres archive de sécurité Office 365 &amp; centre de conformité](enable-archive-mailboxes.md) et [Activer l’archivage illimité dans Office 365](enable-unlimited-archiving.md).
    
2. Placer les boîtes aux lettres en conservation pour litige ou appliquer une stratégie de rétention Office 365 ; consultez les rubriques suivantes : 
    
    - [Place a mailbox on Litigation Hold](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
    - [Vue d'ensemble des stratégies de rétention](retention-policies.md)
    
    Comme indiqué précédemment, lorsque vous placez des boîtes aux lettres en conservation, vous pouvez définir la durée de conservation des éléments de la source de données tierces ou vous pouvez choisir de les conserver indéfiniment.

## <a name="step-4-provide-your-partner-with-information"></a>Étape 4 : fournir des informations au partenaire

La dernière étape consiste à fournir à votre partenaire les informations suivantes pour lui permettre de configurer le connecteur afin qu’il se connecte à votre organisation Office 365 pour importer les données vers les boîtes aux lettres des utilisateurs et la boîte aux lettres de données tierces. 
  
- Le point de terminaison utilisé pour se connecter au service Azure dans Office 365 :

    ```
    https://office365ingestionsvc.gble1.protection.outlook.com/service/ThirdPartyIngestionService.svc
    ```

- La connexion dans les informations d’identification (Office 365 ID d’utilisateur et mot de passe) de la boîte aux lettres des données tierces que vous avez créé à l’étape 2. Ces informations d’identification sont nécessaires pour que le connecteur de partenaires permettre accéder et importer des éléments à des boîtes aux lettres utilisateur et à la boîte aux lettres des données tierces.
 
## <a name="step-5-register-the-third-party-data-connector-in-azure-active-directory"></a>Étape 5 : Enregistrer le connecteur des données tierces dans Azure Active Directory

Démarrage du 30 septembre 2018, le service Azure dans Office 365 commencera utilisant l’authentification moderne dans Exchange Online pour authentifier les connecteurs de données tierce qui tentent de se connecter à votre organisation Office 365 pour importer des données. Pour que cette modification parce que l’authentification moderne offre davantage de sécurité que la méthode actuelle, qui repose sur la création de listes autorisées les connecteurs tiers qui utilisent le point de terminaison décrit précédemment pour se connecter au service Azure.

Pour activer un connecteur tiers pour se connecter à Office 365 à l’aide de la nouvelle méthode d’authentification moderne, un administrateur de votre organisation Office 365 doit consentement pour inscrire le connecteur comme une application de service approuvé dans Azure Active Directory. Cela s’effectue par l’acceptation d’une demande d’autorisations pour autoriser le connecteur accéder aux données de votre organisation dans Azure Active Directory. Après avoir accepté cette demande, le connecteur de données tiers est ajouté en tant qu’une application d’entreprise pour Azure Active Directory et représenté sous la forme d’un principal de service. Pour plus d’informations le processus d’autorisation, voir [Consentement de client d’administration](https://docs.microsoft.com/en-us/skype-sdk/trusted-application-api/docs/tenantadminconsent).

Voici les étapes pour accéder et accepter la demande pour inscrire le connecteur :

1. Accédez à [cette page](https://login.microsoftonline.com/common/oauth2/authorize?client_id=8dfbc50b-2111-4d03-9b4d-dd0d00aae7a2&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent) et vous connecter en utilisant les informations d’identification d’un administrateur global d’Office 365.<br/><br/>La boîte de dialogue s’affiche. Vous pouvez développer les crochets pour passer en revue les autorisations qui seront affectées au connecteur.<br/><br/>![La boîte de dialogue de demande d’autorisations s’affiche.](media/O365_ThirdPartyDataConnector_OptIn1.png)
2. Cliquez sur **Accepter**.

Après avoir accepté la demande, le [tableau de bord de portail Azure](https://portal.azure.com) s’affiche. Pour afficher la liste des applications pour votre organisation, cliquez sur **Azure Active Directory** > **applications d’entreprise**. Le connecteur de données tierce Office 365 est répertorié sur la blade **d’applications d’entreprise** .

> [!IMPORTANT]
> Après 30 septembre 2018, les données tiers ne seront n’est plus importées dans les boîtes aux lettres dans votre organisation si vous n’enregistrez un connecteur tiers dans Azure Active Directory. Remarque existants aux connecteurs de données de tiers (ceux créés avant le 30 septembre 2018) doit également être enregistré dans Azure Active Directory en suivant la procédure à l’étape 5.

### <a name="revoking-consent-for-a-third-party-data-connector"></a>Révoquer le consentement de l’utilisateur pour un connecteur tiers

Une fois que votre organisation consent à la demande d’autorisations pour inscrire un connecteur tiers dans Azure Active Directory, votre organisation peut révoquer cette autorisation à tout moment. Toutefois, révoquer l’autorisation d’un connecteur signifie que les données à partir de la source de données tierce ne seront importées dans Office 365.

Pour révoquer l’autorisation pour un connecteur tiers, vous pouvez supprimer l’application (en supprimant le principal de service correspondant) d’Azure Active Directory à l’aide de la lame **d’applications d’entreprise** dans le portail Azure, ou à l’aide de la [ Remove-MsolServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/msonline/remove-msolserviceprincipal) dans Office 365 PowerShell. Vous pouvez également utiliser l’applet de commande [Remove-AzureADServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/azuread/remove-azureadserviceprincipal) dans Windows Azure Active Directory PowerShell.
  
## <a name="more-information"></a>Plus d'informations

- Indiqué comme précédent, les éléments à partir des données tiers sources sont importées dans les boîtes aux lettres Exchange en tant que messages électroniques. Le connecteur de partenaire importe l’élément à l’aide d’un schéma requis par l’API d’Office 365. Le tableau suivant décrit les propriétés de message d’un élément à partir d’une source de données tierce après l’importation de boîte aux lettres Exchange en tant qu’un message électronique. Le tableau indique également si la propriété message est obligatoire. Les propriétés obligatoires doivent être remplies. Si un élément ne dispose pas d’une propriété obligatoire, il ne seront pas importée vers Office 365. Le processus d’importation renverra un message d’erreur expliquant pourquoi un élément n’a pas été importé et que la propriété est manquante.
    
    |**Propriété de message**|**Obligatoire ?**|**Description**|**Exemple de valeur**|
    |:-----|:-----|:-----|:-----|
    |**FROM** <br/> |Oui  <br/> |L’utilisateur qui a créé à l’origine ou de l’élément envoyé dans la source de données tierce. Le connecteur de partenaire tente de mapper l’ID d’utilisateur de la source (par exemple une poignée Twitter) à un compte d’utilisateur Office 365 pour tous les participants (utilisateurs dans les champs FROM et TO). Une copie du message sera importée dans la boîte aux lettres de tous les participants. Si aucun des participants à partir de l’élément peut être mappé à un compte d’utilisateur Office 365, l’élément sera importé dans la boîte aux lettres d’archivage tiers dans Office 365.<br/> <br/> Le participant qui est identifié en tant que l’expéditeur de l’élément doit avoir une boîte aux lettres active dans l’organisation Office 365 qui l’élément en cours d’importation. Si l’expéditeur ne possède une boîte aux lettres active, le message d’erreur suivant est retourné :<br/><br/>  `One or more messages in the Request failed to be delivered to either From or Sender email address. You will need to resend your entire Request. Error: The request failed. The remote server returned an error: (401) Unauthorized.`  | `bob@contoso.com` <br/> |
    |**TO** <br/> |Oui  <br/> |Utilisateur qui a reçu un élément, le cas échéant, pour un élément dans la source de données.  <br/> | `bob@contoso.com` <br/> |
    |**SUBJECT** <br/> |Non  <br/> |Objet de l’élément source.  <br/> | `"Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/> |
    |**DATE** <br/> |Oui  <br/> |Date à laquelle l’élément a été initialement créé ou publié dans la source de données du client, par exemple, date à laquelle un message Twitter a été publié.  <br/> | `01 NOV 2015` <br/> |
    |**BODY** <br/> |Non  <br/> |Le contenu du message ou du billet. Pour des sources de données, le contenu de cette propriété peut être la même que le contenu de la propriété **SUBJECT** . Pendant le processus d’importation, le connecteur partenaire tente de mettre à jour de fidélité à partir de la source de contenu que possible. Dans la mesure du possible les fichiers, des graphiques ou tout autre contenu dans le corps de l’élément source est inclus dans cette propriété. Dans le cas contraire, le contenu de la source est inclus dans la propriété de **pièce jointe** . Le contenu de cette propriété dépendent sur le connecteur de partenaire et de la capacité de la plateforme de la source.<br/> | `Author: bob@contoso.com` <br/>  `Date: 10 DEC 2014` <br/>  `Tweet: "Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/>  `Date: 01 NOV 2015` <br/> |
    |**ATTACHMENT** <br/> |Non  <br/> |Si un élément dans la source de données (par exemple, un tweet Twitter ou une conversation par messagerie instantanée) contient une pièce jointe ou inclure des images, le partenaire connecté sera première tentative à inclure des pièces jointes dans la propriété **BODY** . Si ce n’est pas possible, puis elle est ajoutée à la ** pièce jointe ** propriété. D’autres exemples de pièces jointes incluent j’aime dans Facebook, les métadonnées à partir de la source de contenu et les réponses à un message ou d’un billet.<br/> | `image.gif` <br/> |
    |**MESSAGECLASS** <br/> |Oui  <br/> | Il s’agit d’une propriété à valeurs multiples, qui est créée et remplie par connecteur partenaire. Le format de cette propriété est `IPM.NOTE.Source.Event`. (Cette propriété doit commencer par `IPM.NOTE`; ce format est similaire à celui de la `IPM.NOTE.X` classe de message.) Cette propriété consacrée les informations suivantes :<br/><br/>`Source`-Indique la source de données tierce ; par exemple, Twitter, Facebook ou BlackBerry.  <br/> <br/>  `Event`-Indique le type d’activité qui a été effectuée dans la source de données tierce qui a produit les éléments ; par exemple, un tweet Twitter ou une publication dans Facebook. Les événements sont spécifiques à la source de données.<br/> <br/>  Un des objectifs de cette propriété sont de filtrer des éléments spécifiques en fonction de la source de données où un élément à l’origine ou en fonction du type d’événement. Par exemple, dans une recherche de découverte, vous pouvez créer une requête de recherche pour trouver tous les tweet qui ont été validées par un utilisateur spécifique.<br/> | `IPM.NOTE.Twitter.Tweet` <br/> |
   
- Lorsque les éléments sont importés correctement aux boîtes aux lettres dans Office 365, un identificateur unique est renvoyé à l’appelant dans le cadre de la réponse HTTP. Cet identificateur — appelé `x-IngestionCorrelationID`— peut être utilisé à des fins de résolution des problèmes suivants par les partenaires pour le suivi de bout en bout d’éléments. Il est recommandé de partenaires capturent ces informations et ouvrez une session en conséquence à leur fin. Voici un exemple d’une réponse HTTP avec cet identificateur :

    ```
    HTTP/1.1 200 OK
    Content-Type: text/xml; charset=utf-8
    Server: Microsoft-IIS/8.5
    x-IngestionCorrelationID: 1ec7667d-f097-47fe-a9a2-bc7ab0a7552b
    X-AspNet-Version: 4.0.30319
    X-Powered-By: ASP.NET
    Date: Tue, 02 Feb 2016 22:55:33 GMT 
    ```
 
- Vous pouvez utiliser l’outil de recherche de contenu de sécurité Office 365 &amp; centre de conformité pour rechercher des éléments qui ont été importés pour les boîtes aux lettres dans Office 365 à partir d’une source de données tierce. Pour rechercher spécifiquement ces éléments importés, vous pouvez utiliser les paires de valeur de la propriété message suivantes dans la zone mots clés pour une recherche de contenu. . 
    
  - **`kind:externaldata`**-Utilisez cette paire de valeur de la propriété pour rechercher tous les types de données de tiers. Par exemple, pour rechercher des éléments qui ont été importés à partir d’une source de données tierce et contenu dans le mot « contoso » dans la propriété Subject de l’élément importé, vous utiliseriez la requête de mot clé `kind:externaldata AND subject:contoso`.
    
  - **`itemclass:ipm.externaldata.<third-party data type>`**-Utilisez cette paire de valeur de la propriété pour rechercher un type de spécifier des données tiers uniquement. Par exemple, pour rechercher uniquement les données Facebook qui contient le mot « contoso » dans la propriété Subject, utiliser la requête de mot clé `itemclass:ipm.externaldata.Facebook* AND subject:contoso`. 

  Pour obtenir la liste complète des valeurs à utiliser pour les types de données de tiers pour la `itemclass` propriété, voir [Recherche de contenu utiliser pour rechercher des données tierces qui a été importées dans Office 365](use-content-search-to-search-third-party-data-that-was-imported.md)
    
   Pour plus d’informations sur l’utilisation de la recherche de contenu et la création de requêtes de recherche de mots clés, voir :
    
  - [Recherche de contenu dans Office 365](content-search.md)
    
  - [Requêtes par mots clés et conditions de recherche pour la recherche de contenu](keyword-queries-and-search-conditions.md)
 
