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
search.appverid: MOE150
ms.assetid: 0ce338d5-3666-4a18-86ab-c6910ff408cc
description: Les administrateurs peuvent importer des données tierces à partir de plateformes de médias sociaux, plates-formes de messagerie instantanées et plates-formes de collaboration de documents aux boîtes aux lettres dans votre organisation Office 365. Cela vous permet d’archiver des données à partir de Facebook, Twitter et sources de données dans Office 365. Vous pouvez ensuite appply des fonctionnalités de conformité d’Office 365 (telles que la conservation légale, recherche de contenu et les stratégies de rétention) à des données tierces.
ms.openlocfilehash: 5e8fe94e0c3e8b39aec479f4755a263438513d35
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038107"
---
# <a name="archiving-third-party-data-in-office-365"></a><span data-ttu-id="77a27-105">Archivage de données tierces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="77a27-105">Archiving third-party data in Office 365</span></span>

<span data-ttu-id="77a27-p102">Permet d’Office 365 administrateurs importer et archiver des données tierces à partir de plateformes de médias sociaux, de messagerie instantanée plateformes et plates-formes de collaboration de documents, aux boîtes aux lettres dans votre organisation Office 365. Exemples de tiers de sources de données que vous pouvez importer dans Office 365 sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="77a27-p102">Office 365 lets administrators import and archive third-party data from social media platforms, instant messaging platforms, and document collaboration platforms, to mailboxes in your Office 365 organization. Examples of third-party data sources that you can import to Office 365 include the following:</span></span> 
  
- <span data-ttu-id="77a27-108">**Mise en réseau** - Twitter, Facebook, Yammer et LinkedIn</span><span class="sxs-lookup"><span data-stu-id="77a27-108">**Social** - Twitter, Facebook, Yammer, and LinkedIn</span></span> 
    
- <span data-ttu-id="77a27-109">**Messagerie instantanée** - Yahoo Messenger, GoogleTalk et Cisco Jabber</span><span class="sxs-lookup"><span data-stu-id="77a27-109">**Instant messaging** - Yahoo Messenger, GoogleTalk, and Cisco Jabber</span></span> 
    
- <span data-ttu-id="77a27-110">**Collaboration sur des documents** - zone et échange</span><span class="sxs-lookup"><span data-stu-id="77a27-110">**Document collaboration** - Box and DropBox</span></span> 
    
- <span data-ttu-id="77a27-111">**Secteurs verticaux** - Finance (comme Thomson Reuters et Bloomberg) et gestion des relations client (par exemple, brouillage force de vente)</span><span class="sxs-lookup"><span data-stu-id="77a27-111">**Vertical industries** - Customer Relationship Management (such as Salesforce Chatter) and Financials (such as Thomson Reuters and Bloomberg)</span></span> 
    
- <span data-ttu-id="77a27-112">**Messagerie texte/SMS** - BlackBerry</span><span class="sxs-lookup"><span data-stu-id="77a27-112">**SMS/text messaging** - BlackBerry</span></span> 
    
<span data-ttu-id="77a27-p103">Après l’importation des données tierces, vous pouvez appliquer des fonctionnalités de conformité d’Office 365, telles que les stratégies de rétention litige, recherche de contenu, d’archivage sur Place, audit et Office 365 — à ces données. Par exemple, lorsqu’une boîte aux lettres est mis en attente pour litige, des données tierces seront préservées. Vous pouvez rechercher des données tierces à l’aide de la recherche de contenu. Ou vous pouvez appliquer l’archivage et les stratégies de rétention pour des données tierces comme vous pouvez utiliser pour les données de Microsoft. En bref, l’archivage des données tierces dans Office 365 peut aider votre organisation respecter les administrations et réglementaires.</span><span class="sxs-lookup"><span data-stu-id="77a27-p103">After third-party data is imported, you can apply Office 365 compliance features—such as Litigation Hold, Content Search, In-Place Archiving, Auditing, and Office 365 retention policies—to this data. For example, when a mailbox is placed on Litigation Hold, third-party data will be preserved. You can search third-party data by using Content Search. Or you can apply archiving and retention polices to third-party data just like you can for Microsoft data. In short, archiving third-party data in Office 365 can help your organization stay compliant with government and regulatory policies.</span></span>
  
<span data-ttu-id="77a27-118">Voici une vue d’ensemble du processus et les étapes nécessaires pour importer des données de tiers pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="77a27-118">Here's an overview of the process and the steps necessary to import third-party data to Office 365.</span></span>

[<span data-ttu-id="77a27-119">Étape 1 : trouver un partenaire de données tierces</span><span class="sxs-lookup"><span data-stu-id="77a27-119">Step 1: Find a third-party data partner</span></span>](#step-1-find-a-third-party-data-partner)

[<span data-ttu-id="77a27-120">Étape 2 : créer et configurer une boîte aux lettres pour les données tierces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="77a27-120">Step 2: Create and configure a third-party data mailbox in Office 365</span></span>](#step-2-create-and-configure-a-third-party-data-mailbox-in-office-365)

[<span data-ttu-id="77a27-121">Étape 3 : configurer des boîtes aux lettres d’utilisateurs pour les données tierces</span><span class="sxs-lookup"><span data-stu-id="77a27-121">Step 3: Configure user mailboxes for third-party data</span></span>](#step-3-configure-user-mailboxes-for-third-party-data)

[<span data-ttu-id="77a27-122">Étape 4 : fournir des informations au partenaire</span><span class="sxs-lookup"><span data-stu-id="77a27-122">Step 4: Provide your partner with information</span></span>](#step-4-provide-your-partner-with-information)

[<span data-ttu-id="77a27-123">Étape 5 : Enregistrer le connecteur des données tierces dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="77a27-123">Step 5: Register the third-party data connector in Azure Active Directory</span></span>](#step-5-register-the-third-party-data-connector-in-azure-active-directory)

## <a name="how-the-third-party-data-import-process-works"></a><span data-ttu-id="77a27-124">Fonctionnement de la façon dont les données tiers processus d’importation ></span><span class="sxs-lookup"><span data-stu-id="77a27-124">How the third-party data import process works></span></span>

<span data-ttu-id="77a27-125">L’illustration et la description suivantes expliquent le fonctionnement du processus d’importation de données tierces.</span><span class="sxs-lookup"><span data-stu-id="77a27-125">The following illustration and description explain how the third-party data import process works.</span></span>
  
![Fonctionnement du processus d’importation de données tierces](media/5d4cf8e9-b4cc-4547-90c8-d12d04a9f0e7.png)
  
1. <span data-ttu-id="77a27-127">Client fonctionne avec leur partenaire de choix pour configurer un connecteur d’extraire des éléments de la source de données tierce et puis importez ces éléments vers Office 365.</span><span class="sxs-lookup"><span data-stu-id="77a27-127">Customer works with their partner of choice to configure a connector that will extract items from the third-party data source and then import those items to Office 365.</span></span>
    
2. <span data-ttu-id="77a27-p104">Le connecteur de partenaire se connecte aux sources de données de tiers via une API de tiers (sur une base planifiée ou configuré en tant que) et extrait les éléments de la source de données. Le connecteur de partenaire convertit le contenu d’un élément dans un format de message électronique. Voir la section [plus d’informations](#more-information) pour une description du schéma de format de message.</span><span class="sxs-lookup"><span data-stu-id="77a27-p104">The partner connector connects to third-party data sources via a third-party API (on a scheduled or as-configured basis) and extracts items from the data source. The partner connector converts the content of an item to an email message format. See the [More information](#more-information) section for a description of the message format schema.</span></span> 
    
3. <span data-ttu-id="77a27-131">Connecteur de partenaire se connecte au service Azure dans Office 365 à l’aide d’Exchange Web Services (EWS) par le biais d’un point de terminaison connu.</span><span class="sxs-lookup"><span data-stu-id="77a27-131">Partner connector connects to the Azure service in Office 365 by using Exchange Web Service (EWS) via a well-known end point.</span></span>
    
4. <span data-ttu-id="77a27-p105">Les éléments sont importés dans la boîte aux lettres d’un utilisateur spécifique ou dans une boîte aux lettres « fourre-tout » destinée aux données tierces. L’importation d’un élément dans la boîte aux lettres d’un utilisateur spécifique ou dans la boîte aux lettres de données tierces repose sur les critères suivants :</span><span class="sxs-lookup"><span data-stu-id="77a27-p105">Items are imported into the mailbox of a specific user or into a "catch-all" third-party data mailbox. Whether an item is imported into a specific user mailbox or to the third-party data mailbox is based on the following criteria:</span></span>
    
    <span data-ttu-id="77a27-p106">**éléments qui ont un ID d’utilisateur qui correspond à un compte d’utilisateur Office 365** - si le connecteur de partenaire pouvez mapper l’ID utilisateur de l’élément dans la source de données tiers à un utilisateur spécifique ID dans Office 365, l’élément est copié dans le dossier de **purge** de l’utilisateur d’a. Dossier éléments récupérables. Les utilisateurs ne peuvent pas accéder aux éléments dans le dossier de purge. Toutefois, vous pouvez utiliser les outils de découverte électronique Office 365 pour rechercher des éléments dans le dossier de purge.</span><span class="sxs-lookup"><span data-stu-id="77a27-p106">a. **Items that have a user ID that corresponds to an Office 365 user account** - If the partner connector can map the user ID of the item in the third-party data source to a specific user ID in Office 365, the item is copied to the **Purges** folder in the user's Recoverable Items folder. Users can't access items in the Purges folder. However, you can use Office 365 eDiscovery tools to search for items in the Purges folder.</span></span>
    
    <span data-ttu-id="77a27-p107">b. **les éléments qui n’ont pas un ID d’utilisateur qui correspond à un compte d’utilisateur Office 365** - si le connecteur de partenaire ne peut pas mapper l’ID utilisateur d’un élément à un utilisateur spécifique ID dans Office 365, l’élément est copié dans le dossier **boîte de réception** de la boîte aux lettres des données tierces. Importation d’éléments dans la boîte de réception permet de vous ou une personne de votre organisation à se connecter à la boîte aux lettres de tiers pour afficher et gérer ces éléments et voir si les modifications doivent être effectuées dans la configuration du connecteur partenaire.</span><span class="sxs-lookup"><span data-stu-id="77a27-p107">b. **Items that don't have a user ID that corresponds to an Office 365 user account** - If the partner connector can't map the user ID of an item to a specific user ID in Office 365, the item is copied to the **Inbox** folder of the third-party data mailbox. Importing items to the inbox allows you or someone in your organization to sign in to the third-party mailbox to view and manage these items, and see if any adjustments need to be made in the partner connector configuration.</span></span>
 
## <a name="step-1-find-a-third-party-data-partner"></a><span data-ttu-id="77a27-141">Étape 1 : trouver un partenaire de données tierces</span><span class="sxs-lookup"><span data-stu-id="77a27-141">Step 1: Find a third-party data partner</span></span>

<span data-ttu-id="77a27-p108">Un composant essentiel pour l’archivage des données tierces dans Office 365 est recherche et utilisation d’un partenaire Microsoft spécialisée dans la capture des données à partir d’une source de données de tiers et importées dans Office 365. Une fois que les données sont importées, il peut être archivée et conservé avec votre organisation d’autres données Microsoft, tels que le courrier électronique à partir d’Exchange et des documents dans SharePoint et OneDrive for Business. Un partenaire crée un connecteur qui extrait les données à partir de sources de données tierces de votre organisation (tels que BlackBerry, Facebook, Google +, Reuters Thomson, Twitter et YouTube) et transmet les données à une API Office 365 qui importe les éléments dans les boîtes aux lettres Exchange en tant que les messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="77a27-p108">A key component for archiving third-party data in Office 365 is finding and working with a Microsoft partner that specializes in capturing data from a third-party data source and importing it to Office 365. After the data is imported, it can be archived and preserved along with your organization's other Microsoft data, such as email from Exchange and documents from SharePoint and OneDrive for Business. A partner creates a connector that extracts data from your organization's third-party data sources (such as BlackBerry, Facebook, Google+, Thomson Reuters, Twitter, and YouTube) and passes that data to an Office 365 API that imports items to Exchange mailboxes as email messages.</span></span> 
  
<span data-ttu-id="77a27-145">Les sections suivantes répertorient les partenaires Microsoft et les sources de données tierces elles prennent en charge, qui participent au programme pour l’archivage des données tierces dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="77a27-145">The following sections list the Microsoft partners—and the third-party data sources they support—that are participating in the program for archiving third-party data in Office 365.</span></span>

[<span data-ttu-id="77a27-146">17a-4 LLC</span><span class="sxs-lookup"><span data-stu-id="77a27-146">17a-4 LLC</span></span>](#17a-4-llc)
  
[<span data-ttu-id="77a27-147">Actiance</span><span class="sxs-lookup"><span data-stu-id="77a27-147">Actiance</span></span>](#actiance)
  
[<span data-ttu-id="77a27-148">ArchiveSocial</span><span class="sxs-lookup"><span data-stu-id="77a27-148">ArchiveSocial</span></span>](#archivesocial)
  
[<span data-ttu-id="77a27-149">Globanet</span><span class="sxs-lookup"><span data-stu-id="77a27-149">Globanet</span></span>](#globanet)
  
[<span data-ttu-id="77a27-150">OpenText</span><span class="sxs-lookup"><span data-stu-id="77a27-150">OpenText</span></span>](#opentext)
  
[<span data-ttu-id="77a27-151">Verba</span><span class="sxs-lookup"><span data-stu-id="77a27-151">Verba</span></span>](#verba)
  
### <a name="17a-4-llc"></a><span data-ttu-id="77a27-152">17a-4 LLC</span><span class="sxs-lookup"><span data-stu-id="77a27-152">17a-4 LLC</span></span>

<span data-ttu-id="77a27-153">17a-4 LLC prend en charge les sources de données tierces suivantes :</span><span class="sxs-lookup"><span data-stu-id="77a27-153">17a-4 LLC supports the following third-party data sources:</span></span>
  
- <span data-ttu-id="77a27-154">BlackBerry</span><span class="sxs-lookup"><span data-stu-id="77a27-154">BlackBerry</span></span>
    
- <span data-ttu-id="77a27-155">Flux de données Bloomberg</span><span class="sxs-lookup"><span data-stu-id="77a27-155">Bloomberg Data Streams</span></span>
    
- <span data-ttu-id="77a27-156">Cisco Jabber</span><span class="sxs-lookup"><span data-stu-id="77a27-156">Cisco Jabber</span></span>
    
- <span data-ttu-id="77a27-157">FactSet</span><span class="sxs-lookup"><span data-stu-id="77a27-157">FactSet</span></span>
    
- <span data-ttu-id="77a27-158">HipChat</span><span class="sxs-lookup"><span data-stu-id="77a27-158">HipChat</span></span>
    
- <span data-ttu-id="77a27-159">InvestEdge</span><span class="sxs-lookup"><span data-stu-id="77a27-159">InvestEdge</span></span>
    
- <span data-ttu-id="77a27-160">LivePerson</span><span class="sxs-lookup"><span data-stu-id="77a27-160">LivePerson</span></span>
    
- <span data-ttu-id="77a27-161">
Flux de données MessageLabs
</span><span class="sxs-lookup"><span data-stu-id="77a27-161">MessageLabs Data Streams</span></span>
    
- <span data-ttu-id="77a27-162">OpenText</span><span class="sxs-lookup"><span data-stu-id="77a27-162">OpenText</span></span>
    
- <span data-ttu-id="77a27-163">Aide en direct « cliquer pour appeler » Oracle/ATG
</span><span class="sxs-lookup"><span data-stu-id="77a27-163">Oracle/ATG 'click-to-call' Live Help</span></span>
    
- <span data-ttu-id="77a27-164">Pivot IMTRADER
</span><span class="sxs-lookup"><span data-stu-id="77a27-164">Pivot IMTRADER</span></span>
    
- <span data-ttu-id="77a27-165">Microsoft SharePoint</span><span class="sxs-lookup"><span data-stu-id="77a27-165">Microsoft SharePoint</span></span>
    
- <span data-ttu-id="77a27-166">MindAlign</span><span class="sxs-lookup"><span data-stu-id="77a27-166">MindAlign</span></span>
    
- <span data-ttu-id="77a27-167">Sitrion One (Newsgator)</span><span class="sxs-lookup"><span data-stu-id="77a27-167">Sitrion One (Newsgator)</span></span>
    
- <span data-ttu-id="77a27-168">
Skype Entreprise (Lync/OCS)</span><span class="sxs-lookup"><span data-stu-id="77a27-168">Skype for Business (Lync/OCS)</span></span>
    
- <span data-ttu-id="77a27-169">
Skype Entreprise Online (Lync Online)
</span><span class="sxs-lookup"><span data-stu-id="77a27-169">Skype for Business Online (Lync Online)</span></span>
    
- <span data-ttu-id="77a27-170">Bases de données SQL</span><span class="sxs-lookup"><span data-stu-id="77a27-170">SQL Databases</span></span>
    
- <span data-ttu-id="77a27-171">
Squawker
</span><span class="sxs-lookup"><span data-stu-id="77a27-171">Squawker</span></span>
    
- <span data-ttu-id="77a27-172">Thomson Reuters Eikon Messenger
</span><span class="sxs-lookup"><span data-stu-id="77a27-172">Thomson Reuters Eikon Messenger</span></span>
  
### <a name="actiance"></a><span data-ttu-id="77a27-173">Actiance</span><span class="sxs-lookup"><span data-stu-id="77a27-173">Actiance</span></span>

<span data-ttu-id="77a27-174">[Actiance](https://www.actiance.com) prend en charge les sources de données tierces suivantes :</span><span class="sxs-lookup"><span data-stu-id="77a27-174">[Actiance](https://www.actiance.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="77a27-175">AIM</span><span class="sxs-lookup"><span data-stu-id="77a27-175">AIM</span></span>
    
- <span data-ttu-id="77a27-176">American Idol</span><span class="sxs-lookup"><span data-stu-id="77a27-176">American Idol</span></span>
    
- <span data-ttu-id="77a27-177">Apple Juice</span><span class="sxs-lookup"><span data-stu-id="77a27-177">Apple Juice</span></span>
    
- <span data-ttu-id="77a27-178">
AOL avec client Pivot
</span><span class="sxs-lookup"><span data-stu-id="77a27-178">AOL with Pivot client</span></span>
    
- <span data-ttu-id="77a27-179">Ares</span><span class="sxs-lookup"><span data-stu-id="77a27-179">Ares</span></span>
    
- <span data-ttu-id="77a27-180">Bazaar Voice</span><span class="sxs-lookup"><span data-stu-id="77a27-180">Bazaar Voice</span></span>
    
- <span data-ttu-id="77a27-181">Bear Share</span><span class="sxs-lookup"><span data-stu-id="77a27-181">Bear Share</span></span>
    
- <span data-ttu-id="77a27-182">Bit Torrent</span><span class="sxs-lookup"><span data-stu-id="77a27-182">Bit Torrent</span></span>
    
- <span data-ttu-id="77a27-183">BlackBerry Call Logs (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="77a27-183">BlackBerry Call Logs (v5, v10, v12)</span></span>
    
- <span data-ttu-id="77a27-184">BlackBerry Messenger (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="77a27-184">BlackBerry Messenger (v5, v10, v12)</span></span>
    
- <span data-ttu-id="77a27-185">BlackBerry PIN (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="77a27-185">BlackBerry PIN (v5, v10, v12)</span></span>
    
- <span data-ttu-id="77a27-186">BlackBerry SMS (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="77a27-186">BlackBerry SMS (v5, v10, v12)</span></span>
    
- <span data-ttu-id="77a27-187">Bloomberg Mail
</span><span class="sxs-lookup"><span data-stu-id="77a27-187">Bloomberg Mail</span></span>
    
- <span data-ttu-id="77a27-188">CellTrust</span><span class="sxs-lookup"><span data-stu-id="77a27-188">CellTrust</span></span>
    
- <span data-ttu-id="77a27-189">Chat Import
</span><span class="sxs-lookup"><span data-stu-id="77a27-189">Chat Import</span></span>
    
- <span data-ttu-id="77a27-190">Chat Real Time Logging and Policy
</span><span class="sxs-lookup"><span data-stu-id="77a27-190">Chat Real Time Logging and Policy</span></span>
    
- <span data-ttu-id="77a27-191">Chatter
</span><span class="sxs-lookup"><span data-stu-id="77a27-191">Chatter</span></span>
    
- <span data-ttu-id="77a27-192">Cisco par messagerie instantanée &amp; serveur de présence (v9.0.1, v9.1, v9.1.1 SU1, 10, v10.5.1 SU1)</span><span class="sxs-lookup"><span data-stu-id="77a27-192">Cisco IM &amp; Presence Server (v9.0.1, v9.1, v9.1.1 SU1, v10, v10.5.1 SU1)</span></span>
    
- <span data-ttu-id="77a27-193">Cisco Unified Presence Server (v8.6.3, v8.6.4, v8.6.5)
</span><span class="sxs-lookup"><span data-stu-id="77a27-193">Cisco Unified Presence Server (v8.6.3, v8.6.4, v8.6.5)</span></span>
    
- <span data-ttu-id="77a27-194">Collaboration Import
</span><span class="sxs-lookup"><span data-stu-id="77a27-194">Collaboration Import</span></span>
    
- <span data-ttu-id="77a27-195">Collaboration Real Time Logging
</span><span class="sxs-lookup"><span data-stu-id="77a27-195">Collaboration Real Time Logging</span></span>
    
- <span data-ttu-id="77a27-196">Direct Connect</span><span class="sxs-lookup"><span data-stu-id="77a27-196">Direct Connect</span></span>
    
- <span data-ttu-id="77a27-197">Facebook</span><span class="sxs-lookup"><span data-stu-id="77a27-197">Facebook</span></span>
    
- <span data-ttu-id="77a27-198">FactSet</span><span class="sxs-lookup"><span data-stu-id="77a27-198">FactSet</span></span>
    
- <span data-ttu-id="77a27-199">FastTrack</span><span class="sxs-lookup"><span data-stu-id="77a27-199">FastTrack</span></span>
    
- <span data-ttu-id="77a27-200">Gnutella</span><span class="sxs-lookup"><span data-stu-id="77a27-200">Gnutella</span></span>
    
- <span data-ttu-id="77a27-201">Google+
</span><span class="sxs-lookup"><span data-stu-id="77a27-201">Google+</span></span>
    
- <span data-ttu-id="77a27-202">GoToMyPC</span><span class="sxs-lookup"><span data-stu-id="77a27-202">GoToMyPC</span></span>
    
- <span data-ttu-id="77a27-203">Hopster</span><span class="sxs-lookup"><span data-stu-id="77a27-203">Hopster</span></span>
    
- <span data-ttu-id="77a27-204">HubConnex</span><span class="sxs-lookup"><span data-stu-id="77a27-204">HubConnex</span></span>
    
- <span data-ttu-id="77a27-205">IBM Connections (version 3.0.1, version 4.0, version 4.5, version 4.5 CR3, version 5)
</span><span class="sxs-lookup"><span data-stu-id="77a27-205">IBM Connections (v3.0.1, v4.0, v4.5, v4.5 CR3, v5)</span></span>
    
- <span data-ttu-id="77a27-206">IBM Connections Chat Cloud
</span><span class="sxs-lookup"><span data-stu-id="77a27-206">IBM Connections Chat Cloud</span></span>
    
- <span data-ttu-id="77a27-207">IBM Connections Social Cloud
</span><span class="sxs-lookup"><span data-stu-id="77a27-207">IBM Connections Social Cloud</span></span>
    
- <span data-ttu-id="77a27-208">IBM SameTime Advanced 8.5.2 IFR1
</span><span class="sxs-lookup"><span data-stu-id="77a27-208">IBM SameTime Advanced 8.5.2 IFR1</span></span>
    
- <span data-ttu-id="77a27-209">IBM SameTime Communicate 9.0
</span><span class="sxs-lookup"><span data-stu-id="77a27-209">IBM SameTime Communicate 9.0</span></span>
    
- <span data-ttu-id="77a27-210">IBM SameTime Community (version 8.0.2, version 8.5.1 IFR2, version 8.5.2 IFR1, version 9.1)
</span><span class="sxs-lookup"><span data-stu-id="77a27-210">IBM SameTime Community (v8.0.2, v8.5.1 IFR2, v8.5.2 IFR1, v9.1)</span></span>
    
- <span data-ttu-id="77a27-211">IBM SameTime Complete 9.0
</span><span class="sxs-lookup"><span data-stu-id="77a27-211">IBM SameTime Complete 9.0</span></span>
    
- <span data-ttu-id="77a27-212">IBM SameTime Conference 9.0
</span><span class="sxs-lookup"><span data-stu-id="77a27-212">IBM SameTime Conference 9.0</span></span>
    
- <span data-ttu-id="77a27-213">IBM SameTime Meeting 8.5.2 IFR1
</span><span class="sxs-lookup"><span data-stu-id="77a27-213">IBM SameTime Meeting 8.5.2 IFR1</span></span>
    
- <span data-ttu-id="77a27-214">ICE/YellowJacket</span><span class="sxs-lookup"><span data-stu-id="77a27-214">ICE/YellowJacket</span></span>
    
- <span data-ttu-id="77a27-215">IM Import
</span><span class="sxs-lookup"><span data-stu-id="77a27-215">IM Import</span></span>
    
- <span data-ttu-id="77a27-216">IM Real Time Logging and Policy
</span><span class="sxs-lookup"><span data-stu-id="77a27-216">IM Real Time Logging and Policy</span></span>
    
- <span data-ttu-id="77a27-217">Indii Messenger
</span><span class="sxs-lookup"><span data-stu-id="77a27-217">Indii Messenger</span></span>
    
- <span data-ttu-id="77a27-218">Instant Bloomberg
</span><span class="sxs-lookup"><span data-stu-id="77a27-218">Instant Bloomberg</span></span>
    
- <span data-ttu-id="77a27-219">IRC</span><span class="sxs-lookup"><span data-stu-id="77a27-219">IRC</span></span>
    
- <span data-ttu-id="77a27-220">Jive
</span><span class="sxs-lookup"><span data-stu-id="77a27-220">Jive</span></span>
    
- <span data-ttu-id="77a27-221">Jive 6 Real Time Logging (version 6, version 7)
</span><span class="sxs-lookup"><span data-stu-id="77a27-221">Jive 6 Real Time Logging (v6, v7)</span></span>
    
- <span data-ttu-id="77a27-222">Jive Import</span><span class="sxs-lookup"><span data-stu-id="77a27-222">Jive Import</span></span>
    
- <span data-ttu-id="77a27-223">JXTA</span><span class="sxs-lookup"><span data-stu-id="77a27-223">JXTA</span></span>
    
- <span data-ttu-id="77a27-224">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="77a27-224">LinkedIn</span></span>
    
- <span data-ttu-id="77a27-225">
Microsoft Lync (2010, 2013)
</span><span class="sxs-lookup"><span data-stu-id="77a27-225">Microsoft Lync (2010, 2013)</span></span>
    
- <span data-ttu-id="77a27-226">MFTP</span><span class="sxs-lookup"><span data-stu-id="77a27-226">MFTP</span></span>
    
- <span data-ttu-id="77a27-227">Microsoft Lync 2013 Voix
</span><span class="sxs-lookup"><span data-stu-id="77a27-227">Microsoft Lync 2013 Voice</span></span>
    
- <span data-ttu-id="77a27-228">Microsoft SharePoint (2010, 2013)
</span><span class="sxs-lookup"><span data-stu-id="77a27-228">Microsoft SharePoint (2010, 2013)</span></span>
    
- <span data-ttu-id="77a27-229">Microsoft SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="77a27-229">Microsoft SharePoint Online</span></span>
    
- <span data-ttu-id="77a27-230">Microsoft UC (Unified Communications)</span><span class="sxs-lookup"><span data-stu-id="77a27-230">Microsoft UC (Unified Communications)</span></span>
    
- <span data-ttu-id="77a27-231">MindAlign</span><span class="sxs-lookup"><span data-stu-id="77a27-231">MindAlign</span></span>
    
- <span data-ttu-id="77a27-232">Mobile Guard</span><span class="sxs-lookup"><span data-stu-id="77a27-232">Mobile Guard</span></span>
    
- <span data-ttu-id="77a27-233">MSN</span><span class="sxs-lookup"><span data-stu-id="77a27-233">MSN</span></span>
    
- <span data-ttu-id="77a27-234">My Space</span><span class="sxs-lookup"><span data-stu-id="77a27-234">My Space</span></span>
    
- <span data-ttu-id="77a27-235">NEONetwork</span><span class="sxs-lookup"><span data-stu-id="77a27-235">NEONetwork</span></span>
    
- <span data-ttu-id="77a27-236">Office 365 Lync dédié
</span><span class="sxs-lookup"><span data-stu-id="77a27-236">Office 365 Lync Dedicated</span></span>
    
- <span data-ttu-id="77a27-237">MI partagée Office 365
</span><span class="sxs-lookup"><span data-stu-id="77a27-237">Office 365 Shared IM</span></span>
    
- <span data-ttu-id="77a27-238">Pinterest</span><span class="sxs-lookup"><span data-stu-id="77a27-238">Pinterest</span></span>
    
- <span data-ttu-id="77a27-239">Pivot</span><span class="sxs-lookup"><span data-stu-id="77a27-239">Pivot</span></span>
    
- <span data-ttu-id="77a27-240">QQ</span><span class="sxs-lookup"><span data-stu-id="77a27-240">QQ</span></span>
    
- <span data-ttu-id="77a27-241">Skype Entreprise 2015</span><span class="sxs-lookup"><span data-stu-id="77a27-241">Skype for Business 2015</span></span>
    
- <span data-ttu-id="77a27-242">SoftEther</span><span class="sxs-lookup"><span data-stu-id="77a27-242">SoftEther</span></span>
    
- <span data-ttu-id="77a27-243">Symphony
</span><span class="sxs-lookup"><span data-stu-id="77a27-243">Symphony</span></span>
    
- <span data-ttu-id="77a27-244">Thomson Reuters Eikon
</span><span class="sxs-lookup"><span data-stu-id="77a27-244">Thomson Reuters Eikon</span></span>
    
- <span data-ttu-id="77a27-245">Thomson Reuters Messenger
</span><span class="sxs-lookup"><span data-stu-id="77a27-245">Thomson Reuters Messenger</span></span>
    
- <span data-ttu-id="77a27-246">Tor</span><span class="sxs-lookup"><span data-stu-id="77a27-246">Tor</span></span>
    
- <span data-ttu-id="77a27-247">TTT</span><span class="sxs-lookup"><span data-stu-id="77a27-247">TTT</span></span>
    
- <span data-ttu-id="77a27-248">Twitter</span><span class="sxs-lookup"><span data-stu-id="77a27-248">Twitter</span></span>
    
- <span data-ttu-id="77a27-249">WinMX</span><span class="sxs-lookup"><span data-stu-id="77a27-249">WinMX</span></span>
    
- <span data-ttu-id="77a27-250">Winny</span><span class="sxs-lookup"><span data-stu-id="77a27-250">Winny</span></span>
    
- <span data-ttu-id="77a27-251">Yahoo
</span><span class="sxs-lookup"><span data-stu-id="77a27-251">Yahoo</span></span>
    
- <span data-ttu-id="77a27-252">Yammer</span><span class="sxs-lookup"><span data-stu-id="77a27-252">Yammer</span></span>
    
- <span data-ttu-id="77a27-253">YouTube</span><span class="sxs-lookup"><span data-stu-id="77a27-253">YouTube</span></span>
    
  
### <a name="archivesocial"></a><span data-ttu-id="77a27-254">ArchiveSocial</span><span class="sxs-lookup"><span data-stu-id="77a27-254">ArchiveSocial</span></span>

<span data-ttu-id="77a27-255">[ArchiveSocial](https://www.archivesocial.com) prend en charge les sources de données tierces suivantes :</span><span class="sxs-lookup"><span data-stu-id="77a27-255">[ArchiveSocial ](https://www.archivesocial.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="77a27-256">Facebook</span><span class="sxs-lookup"><span data-stu-id="77a27-256">Facebook</span></span>
    
- <span data-ttu-id="77a27-257">Flickr
</span><span class="sxs-lookup"><span data-stu-id="77a27-257">Flickr</span></span>
    
- <span data-ttu-id="77a27-258">Instagram
</span><span class="sxs-lookup"><span data-stu-id="77a27-258">Instagram</span></span>
    
- <span data-ttu-id="77a27-259">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="77a27-259">LinkedIn</span></span>
    
- <span data-ttu-id="77a27-260">Pinterest</span><span class="sxs-lookup"><span data-stu-id="77a27-260">Pinterest</span></span>
    
- <span data-ttu-id="77a27-261">Twitter</span><span class="sxs-lookup"><span data-stu-id="77a27-261">Twitter</span></span>
    
- <span data-ttu-id="77a27-262">YouTube</span><span class="sxs-lookup"><span data-stu-id="77a27-262">YouTube</span></span>
    
- <span data-ttu-id="77a27-263">Vimeo</span><span class="sxs-lookup"><span data-stu-id="77a27-263">Vimeo</span></span>
  
### <a name="globanet"></a><span data-ttu-id="77a27-264">Globanet</span><span class="sxs-lookup"><span data-stu-id="77a27-264">Globanet</span></span>

<span data-ttu-id="77a27-265">[Globanet](https://www.globanet.com) prend en charge les sources de données tierces suivantes :</span><span class="sxs-lookup"><span data-stu-id="77a27-265">[Globanet](https://www.globanet.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="77a27-266">AOL avec client Pivot </span><span class="sxs-lookup"><span data-stu-id="77a27-266">AOL with Pivot Client</span></span> 
    
- <span data-ttu-id="77a27-267">BlackBerry Call Logs (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="77a27-267">BlackBerry Call Logs (v5, v10, v12)</span></span>
    
- <span data-ttu-id="77a27-268">BlackBerry Messenger (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="77a27-268">BlackBerry Messenger (v5, v10, v12)</span></span>
    
- <span data-ttu-id="77a27-269">BlackBerry PIN (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="77a27-269">BlackBerry PIN (v5, v10, v12)</span></span>
    
- <span data-ttu-id="77a27-270">BlackBerry SMS (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="77a27-270">BlackBerry SMS (v5, v10, v12)</span></span>
    
- <span data-ttu-id="77a27-271">Bloomberg Chat
</span><span class="sxs-lookup"><span data-stu-id="77a27-271">Bloomberg Chat</span></span>
    
- <span data-ttu-id="77a27-272">Bloomberg Mail
</span><span class="sxs-lookup"><span data-stu-id="77a27-272">Bloomberg Mail</span></span>
    
- <span data-ttu-id="77a27-273">Box
</span><span class="sxs-lookup"><span data-stu-id="77a27-273">Box</span></span>
    
- <span data-ttu-id="77a27-274">CipherCloud for Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="77a27-274">CipherCloud for Salesforce Chatter</span></span>
    
- <span data-ttu-id="77a27-275">Messagerie instantanée de Cisco &amp; serveur de présence (10, v10.5.1 SU1, v11.0, v11.5 SU2)</span><span class="sxs-lookup"><span data-stu-id="77a27-275">Cisco IM &amp; Presence Server (v10, v10.5.1 SU1, v11.0, v11.5 SU2)</span></span>

- <span data-ttu-id="77a27-276">Cisco Webex équipes</span><span class="sxs-lookup"><span data-stu-id="77a27-276">Cisco Webex Teams</span></span>

- <span data-ttu-id="77a27-277">Espace de travail Citrix &amp; ShareFile</span><span class="sxs-lookup"><span data-stu-id="77a27-277">Citrix Workspace &amp; ShareFile</span></span>

- <span data-ttu-id="77a27-278">CrowdCompass</span><span class="sxs-lookup"><span data-stu-id="77a27-278">CrowdCompass</span></span>

- <span data-ttu-id="77a27-279">Fichiers texte délimités personnalisés
</span><span class="sxs-lookup"><span data-stu-id="77a27-279">Custom delimited text files</span></span>
    
- <span data-ttu-id="77a27-280">Fichiers XML personnalisés
</span><span class="sxs-lookup"><span data-stu-id="77a27-280">Custom XML files</span></span>
    
- <span data-ttu-id="77a27-281">Facebook (Pages)</span><span class="sxs-lookup"><span data-stu-id="77a27-281">Facebook (Pages)</span></span>
    
- <span data-ttu-id="77a27-282">Factset
</span><span class="sxs-lookup"><span data-stu-id="77a27-282">Factset</span></span>
    
- <span data-ttu-id="77a27-283">FXConnect</span><span class="sxs-lookup"><span data-stu-id="77a27-283">FXConnect</span></span>
    
- <span data-ttu-id="77a27-284">ICE Chat/YellowJacket</span><span class="sxs-lookup"><span data-stu-id="77a27-284">ICE Chat/YellowJacket</span></span>
    
- <span data-ttu-id="77a27-285">Jive
</span><span class="sxs-lookup"><span data-stu-id="77a27-285">Jive</span></span>
    
- <span data-ttu-id="77a27-286">Macgregor XIP
</span><span class="sxs-lookup"><span data-stu-id="77a27-286">Macgregor XIP</span></span>

- <span data-ttu-id="77a27-287">Microsoft Exchange Server</span><span class="sxs-lookup"><span data-stu-id="77a27-287">Microsoft Exchange Server</span></span>
    
- <span data-ttu-id="77a27-288">Microsoft OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="77a27-288">Microsoft OneDrive for Business</span></span>

- <span data-ttu-id="77a27-289">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="77a27-289">Microsoft Teams</span></span>
       
- <span data-ttu-id="77a27-290">Microsoft Yammer
</span><span class="sxs-lookup"><span data-stu-id="77a27-290">Microsoft Yammer</span></span>
    
- <span data-ttu-id="77a27-291">Mobile Guard</span><span class="sxs-lookup"><span data-stu-id="77a27-291">Mobile Guard</span></span>
    
- <span data-ttu-id="77a27-292">Pivot</span><span class="sxs-lookup"><span data-stu-id="77a27-292">Pivot</span></span>
    
- <span data-ttu-id="77a27-293">Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="77a27-293">Salesforce Chatter</span></span>

- <span data-ttu-id="77a27-294">Skype Entreprise Online</span><span class="sxs-lookup"><span data-stu-id="77a27-294">Skype for Business Online</span></span>
    
- <span data-ttu-id="77a27-295">Skype Entreprise, versions 2007 R2-2016 (sur site)
</span><span class="sxs-lookup"><span data-stu-id="77a27-295">Skype for Business, versions 2007 R2 - 2016 (on-premises)</span></span>
    
- <span data-ttu-id="77a27-296">Slack Enterprise Grid</span><span class="sxs-lookup"><span data-stu-id="77a27-296">Slack Enterprise Grid</span></span>
    
- <span data-ttu-id="77a27-297">Symphony
</span><span class="sxs-lookup"><span data-stu-id="77a27-297">Symphony</span></span>
    
- <span data-ttu-id="77a27-298">Thomson Reuters Eikon
</span><span class="sxs-lookup"><span data-stu-id="77a27-298">Thomson Reuters Eikon</span></span>
    
- <span data-ttu-id="77a27-299">Thomson Reuters Messenger
</span><span class="sxs-lookup"><span data-stu-id="77a27-299">Thomson Reuters Messenger</span></span>
    
- <span data-ttu-id="77a27-300">Thomson Reuters Dealings 3000/FX Trading
</span><span class="sxs-lookup"><span data-stu-id="77a27-300">Thomson Reuters Dealings 3000 / FX Trading</span></span>
    
- <span data-ttu-id="77a27-301">Twitter</span><span class="sxs-lookup"><span data-stu-id="77a27-301">Twitter</span></span>
    
- <span data-ttu-id="77a27-302">UBS Chat
</span><span class="sxs-lookup"><span data-stu-id="77a27-302">UBS Chat</span></span>
    
- <span data-ttu-id="77a27-303">YouTube</span><span class="sxs-lookup"><span data-stu-id="77a27-303">YouTube</span></span>
  
### <a name="opentext"></a><span data-ttu-id="77a27-304">OpenText</span><span class="sxs-lookup"><span data-stu-id="77a27-304">OpenText</span></span>

<span data-ttu-id="77a27-305">[OpenText](https://www.opentext.com/what-we-do/products/opentext-product-offerings-catalog/rebranded-products/daegis) prend en charge les sources de données tierces suivantes :</span><span class="sxs-lookup"><span data-stu-id="77a27-305">[OpenText](https://www.opentext.com/what-we-do/products/opentext-product-offerings-catalog/rebranded-products/daegis) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="77a27-306">Axs Encrypted</span><span class="sxs-lookup"><span data-stu-id="77a27-306">Axs Encrypted</span></span>
    
- <span data-ttu-id="77a27-307">Axs Exchange</span><span class="sxs-lookup"><span data-stu-id="77a27-307">Axs Exchange</span></span>
    
- <span data-ttu-id="77a27-308">Axs Local Archive</span><span class="sxs-lookup"><span data-stu-id="77a27-308">Axs Local Archive</span></span>
    
- <span data-ttu-id="77a27-309">Axs PlaceHolder</span><span class="sxs-lookup"><span data-stu-id="77a27-309">Axs PlaceHolder</span></span>
    
- <span data-ttu-id="77a27-310">Axs Signed</span><span class="sxs-lookup"><span data-stu-id="77a27-310">Axs Signed</span></span>
    
- <span data-ttu-id="77a27-311">Bloomberg</span><span class="sxs-lookup"><span data-stu-id="77a27-311">Bloomberg</span></span>
    
- <span data-ttu-id="77a27-312">Thomson Reuters</span><span class="sxs-lookup"><span data-stu-id="77a27-312">Thomson Reuters</span></span>
  
### <a name="verba"></a><span data-ttu-id="77a27-313">Verba</span><span class="sxs-lookup"><span data-stu-id="77a27-313">Verba</span></span>

<span data-ttu-id="77a27-314">[Verba](https://www.verba.com) prend en charge les sources de données tierces suivantes :</span><span class="sxs-lookup"><span data-stu-id="77a27-314">[Verba](https://www.verba.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="77a27-315">Avaya Aura Video
</span><span class="sxs-lookup"><span data-stu-id="77a27-315">Avaya Aura Video</span></span>
    
- <span data-ttu-id="77a27-316">Avaya Aura Voice
</span><span class="sxs-lookup"><span data-stu-id="77a27-316">Avaya Aura Voice</span></span>
    
- <span data-ttu-id="77a27-317">Avtec Radio
</span><span class="sxs-lookup"><span data-stu-id="77a27-317">Avtec Radio</span></span>
    
- <span data-ttu-id="77a27-318">Bosch/Telex Radio
</span><span class="sxs-lookup"><span data-stu-id="77a27-318">Bosch/Telex Radio</span></span>
    
- <span data-ttu-id="77a27-319">BroadSoft Video
</span><span class="sxs-lookup"><span data-stu-id="77a27-319">BroadSoft Video</span></span>
    
- <span data-ttu-id="77a27-320">BroadSoft Voice
</span><span class="sxs-lookup"><span data-stu-id="77a27-320">BroadSoft Voice</span></span>
    
- <span data-ttu-id="77a27-321">Centile Voice
</span><span class="sxs-lookup"><span data-stu-id="77a27-321">Centile Voice</span></span>
    
- <span data-ttu-id="77a27-322">Cisco Jabber IM
</span><span class="sxs-lookup"><span data-stu-id="77a27-322">Cisco Jabber IM</span></span>
    
- <span data-ttu-id="77a27-323">Cisco UC Video
</span><span class="sxs-lookup"><span data-stu-id="77a27-323">Cisco UC Video</span></span>
    
- <span data-ttu-id="77a27-324">Cisco UC Voice
</span><span class="sxs-lookup"><span data-stu-id="77a27-324">Cisco UC Voice</span></span>
    
- <span data-ttu-id="77a27-325">Cisco UCCX/UCCE vidéo</span><span class="sxs-lookup"><span data-stu-id="77a27-325">Cisco UCCX/UCCE Video</span></span>
    
- <span data-ttu-id="77a27-326">Cisco UCCX/UCCE vocale</span><span class="sxs-lookup"><span data-stu-id="77a27-326">Cisco UCCX/UCCE Voice</span></span>
    
- <span data-ttu-id="77a27-327">ESChat Radio</span><span class="sxs-lookup"><span data-stu-id="77a27-327">ESChat Radio</span></span>
    
- <span data-ttu-id="77a27-328">Geoman Contact Expert</span><span class="sxs-lookup"><span data-stu-id="77a27-328">Geoman Contact Expert</span></span>
    
- <span data-ttu-id="77a27-329">IP Trade Voice
</span><span class="sxs-lookup"><span data-stu-id="77a27-329">IP Trade Voice</span></span>
    
- <span data-ttu-id="77a27-330">Luware LUCS Contact Center</span><span class="sxs-lookup"><span data-stu-id="77a27-330">Luware LUCS Contact Center</span></span>
    
- <span data-ttu-id="77a27-331">Microsoft UC (Unified Communications)</span><span class="sxs-lookup"><span data-stu-id="77a27-331">Microsoft UC (Unified Communications)</span></span>
    
- <span data-ttu-id="77a27-332">Mitel MiContact Center for Lync (prairieFyre) 
</span><span class="sxs-lookup"><span data-stu-id="77a27-332">Mitel MiContact Center for Lync (prairieFyre)</span></span>
    
- <span data-ttu-id="77a27-333">Oracle / Acme Packet Session Border Controller Video  
</span><span class="sxs-lookup"><span data-stu-id="77a27-333">Oracle / Acme Packet Session Border Controller Video</span></span>
    
- <span data-ttu-id="77a27-334">Oracle / Acme Packet Session Border Controller Voice
</span><span class="sxs-lookup"><span data-stu-id="77a27-334">Oracle / Acme Packet Session Border Controller Voice</span></span>
    
- <span data-ttu-id="77a27-335">Singtel Mobile Voice
</span><span class="sxs-lookup"><span data-stu-id="77a27-335">Singtel Mobile Voice</span></span>
    
- <span data-ttu-id="77a27-336">SIPREC Video</span><span class="sxs-lookup"><span data-stu-id="77a27-336">SIPREC Video</span></span>
    
-  <span data-ttu-id="77a27-337">SIPREC Voice</span><span class="sxs-lookup"><span data-stu-id="77a27-337">SIPREC Voice</span></span> 
    
- <span data-ttu-id="77a27-338">Skype Entreprise / MI Lync
</span><span class="sxs-lookup"><span data-stu-id="77a27-338">Skype for Business / Lync IM</span></span>
    
- <span data-ttu-id="77a27-339">Skype Entreprise / Vidéo Lync
</span><span class="sxs-lookup"><span data-stu-id="77a27-339">Skype for Business / Lync Video</span></span>
    
- <span data-ttu-id="77a27-340">Skype Entreprise / Voix Lync
</span><span class="sxs-lookup"><span data-stu-id="77a27-340">Skype for Business / Lync Voice</span></span>
    
- <span data-ttu-id="77a27-341">Speakerbus Voice
</span><span class="sxs-lookup"><span data-stu-id="77a27-341">Speakerbus Voice</span></span>
    
- <span data-ttu-id="77a27-342">Standard SIP/H.323 Video 
</span><span class="sxs-lookup"><span data-stu-id="77a27-342">Standard SIP/H.323 Video</span></span>
    
- <span data-ttu-id="77a27-343">Standard SIP/H.323 Voice 
</span><span class="sxs-lookup"><span data-stu-id="77a27-343">Standard SIP/H.323 Voice</span></span>
    
- <span data-ttu-id="77a27-344">Truphone Voice
</span><span class="sxs-lookup"><span data-stu-id="77a27-344">Truphone Voice</span></span>
    
- <span data-ttu-id="77a27-345">TwistedPair Radio
</span><span class="sxs-lookup"><span data-stu-id="77a27-345">TwistedPair Radio</span></span>
    
- <span data-ttu-id="77a27-346">Écran d’ordinateur de bureau Windows 
</span><span class="sxs-lookup"><span data-stu-id="77a27-346">Windows Desktop Computer Screen</span></span>
  
## <a name="step-2-create-and-configure-a-third-party-data-mailbox-in-office-365"></a><span data-ttu-id="77a27-347">Étape 2 : créer et configurer une boîte aux lettres pour les données tierces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="77a27-347">Step 2: Create and configure a third-party data mailbox in Office 365</span></span>

<span data-ttu-id="77a27-p109">Voici les étapes pour créer et configurer une boîte aux lettres de données tiers pour l’importation de données dans Office 365. Précédente comme expliqué, les éléments sont importés à cette boîte aux lettres si le connecteur de partenaire ne peut pas mapper l’ID de l’élément à un compte d’utilisateur Office 365.</span><span class="sxs-lookup"><span data-stu-id="77a27-p109">Here are the steps for creating and configuring a third-party data mailbox for importing data to Office 365. As previous explained, items are imported to this mailbox if the partner connector can't map the user ID of the item to an Office 365 user account.</span></span>
  
 <span data-ttu-id="77a27-350">**Effectuer ces tâches dans le centre d’administration d’Office 365**</span><span class="sxs-lookup"><span data-stu-id="77a27-350">**Complete these tasks in the Office 365 admin center**</span></span>
  
1. <span data-ttu-id="77a27-p110">Créer un nouveau compte d’utilisateur dans Office 365 et l’attribuer une licence Exchange Online Plan 2 ; consultez la rubrique [Ajouter des utilisateurs à Office 365](https://go.microsoft.com/fwlink/p/?LinkId=692098). Une licence Plan 2 est requis pour placer la boîte aux lettres en conservation pour litige ou activer une boîte aux lettres d’archivage qui a un quota de stockage illimitée.</span><span class="sxs-lookup"><span data-stu-id="77a27-p110">Create a new user account in Office 365 and assign it an Exchange Online Plan 2 license; see [Add users to Office 365](https://go.microsoft.com/fwlink/p/?LinkId=692098). A Plan 2 license is required to place the mailbox on Litigation Hold or enable an archive mailbox that has an unlimited storage quota.</span></span>
    
2. <span data-ttu-id="77a27-353">Ajoutez le compte d’utilisateur pour la boîte aux lettres des données tierces au rôle **administrateur Exchange** admin dans Office 365 ; consultez [assigner des rôles d’administrateur dans Office 365](https://go.microsoft.com/fwlink/p/?LinkId=532393).</span><span class="sxs-lookup"><span data-stu-id="77a27-353">Add the user account for the third-party data mailbox to the **Exchange administrator** admin role in Office 365; see [Assign admin roles in Office 365](https://go.microsoft.com/fwlink/p/?LinkId=532393).</span></span>
    
    > [!TIP]
    > <span data-ttu-id="77a27-p111">Notez les informations d’identification pour ce compte d’utilisateur. Vous devez les fournir à votre partenaire, comme décrit à l’étape 4.</span><span class="sxs-lookup"><span data-stu-id="77a27-p111">Write down the credentials for this user account. You need to provide them to your partner, as described in Step 4.</span></span> 
  
 <span data-ttu-id="77a27-356">**Effectuer ces tâches dans le centre d’administration Exchange**</span><span class="sxs-lookup"><span data-stu-id="77a27-356">**Complete these tasks in the Exchange admin center**</span></span>
  
1. <span data-ttu-id="77a27-p112">Masquer la boîte aux lettres de données tiers à partir du carnet d’adresses et d’autres listes d’adresses dans votre organisation ; voir [Gérer les boîtes aux lettres](https://go.microsoft.com/fwlink/p/?LinkId=616058). Vous pouvez également exécuter la commande PowerShell suivante :</span><span class="sxs-lookup"><span data-stu-id="77a27-p112">Hide the third-party data mailbox from the address book and other address lists in your organization; see [Manage user mailboxes](https://go.microsoft.com/fwlink/p/?LinkId=616058). Alternatively, you can run the following PowerShell command:</span></span>
    
    ```
    Set-Mailbox -Identity <identity of third-party data mailbox> -HiddenFromAddressListsEnabled $true
    ```

2. <span data-ttu-id="77a27-359">Attribuer l’autorisation **FullAccess** pour la boîte aux lettres des données tierces pour que les administrateurs ou aux règlements puissent ouvrir la boîte aux lettres des données tierces dans le client de bureau Outlook ; voir [Gérer les autorisations pour les destinataires](https://go.microsoft.com/fwlink/p/?LinkId=692104).</span><span class="sxs-lookup"><span data-stu-id="77a27-359">Assign the **FullAccess** permission to the third-party data mailbox so that administrators or compliance officers can open the third-party data mailbox in the Outlook desktop client; see [Manage permissions for recipients](https://go.microsoft.com/fwlink/p/?LinkId=692104).</span></span>
    
3. <span data-ttu-id="77a27-360">Activer les fonctionnalités Office 365 suivantes relatives à la conformité pour la boîte aux lettres des données tierces :</span><span class="sxs-lookup"><span data-stu-id="77a27-360">Enable the following compliance-related Office 365 features for the third-party data mailbox:</span></span>
    
    - <span data-ttu-id="77a27-p113">Activer la boîte aux lettres d’archivage ; voir [Activer les boîtes aux lettres archive de sécurité Office 365 &amp; centre de conformité](enable-archive-mailboxes.md) et [Activer l’archivage illimité dans Office 365](enable-unlimited-archiving.md). Vous pouvez libérer de l’espace dans la boîte aux lettres principal en configurant une stratégie d’archivage qui déplace les éléments de données tierces dans la boîte aux lettres d’archive. Cela vous fournira stockage illimité pour les données de tiers.</span><span class="sxs-lookup"><span data-stu-id="77a27-p113">Enable the archive mailbox; see [Enable archive mailboxes in the Office 365 Security &amp; Compliance Center](enable-archive-mailboxes.md) and [Enable unlimited archiving in Office 365](enable-unlimited-archiving.md). This will let you free-up storage space in the primary mailbox by setting up an archive policy that moves third-party data items to the archive mailbox. This will provide you with unlimited storage for third-party data.</span></span>
    
    - <span data-ttu-id="77a27-p114">Placez la boîte aux lettres des données tierces litige. Vous pouvez également appliquer une stratégie de rétention Office 365 de sécurité Office 365 &amp; centre de conformité. Placer cette boîte aux lettres en attente pour conserver des éléments de données de tiers (indéfiniment ou pendant une durée spécifiée) et les empêcher d’être purgées de la boîte aux lettres. Consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="77a27-p114">Place the third-party data mailbox on Litigation Hold. You can also apply an Office 365 retention policy in the Office 365 Security &amp; Compliance Center. Placing this mailbox on hold will retain third-party data items (indefinitely or for a specified duration) and prevent them from being purged from the mailbox. See one of the following topics:</span></span>
    
      - [<span data-ttu-id="77a27-368">Place a mailbox on Litigation Hold</span><span class="sxs-lookup"><span data-stu-id="77a27-368">Place a mailbox on Litigation Hold</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
      - [<span data-ttu-id="77a27-369">Vue d'ensemble des stratégies de rétention</span><span class="sxs-lookup"><span data-stu-id="77a27-369">Overview of retention policies in Office 365</span></span>](retention-policies.md)
    
       
    
    - <span data-ttu-id="77a27-p115">Activer la boîte aux lettres enregistrement d’audit pour un accès propriétaire, délégué et d’administration pour la boîte aux lettres des données tierces ; consultez la rubrique [Activer la boîte aux lettres de l’audit dans Office 365](enable-mailbox-auditing.md). Cela vous permettra d’auditer toutes les activités effectuées par les utilisateurs ayant accès à la boîte aux lettres des données tierces.</span><span class="sxs-lookup"><span data-stu-id="77a27-p115">Enable mailbox audit logging for owner, delegate, and admin access to the third-party data mailbox; see [Enable mailbox auditing in Office 365](enable-mailbox-auditing.md). This will allow you to audit all activity performed by any user who has access to the third-party data mailbox.</span></span>

## <a name="step-3-configure-user-mailboxes-for-third-party-data"></a><span data-ttu-id="77a27-372">Étape 3 : configurer des boîtes aux lettres d’utilisateurs pour les données tierces</span><span class="sxs-lookup"><span data-stu-id="77a27-372">Step 3: Configure user mailboxes for third-party data</span></span>

<span data-ttu-id="77a27-p116">L’étape suivante consiste à configurer les boîtes aux lettres pour prendre en charge des données tierces. Effectuer ces tâches à l’aide du centre d’administration Exchange ou à l’aide des applets de commande Windows PowerShell correspondant.</span><span class="sxs-lookup"><span data-stu-id="77a27-p116">The next step is to configure user mailboxes to support third-party data. Complete these tasks by using the Exchange admin center or by using the corresponding Windows PowerShell cmdlets.</span></span>
  
1. <span data-ttu-id="77a27-375">Activer la boîte aux lettres d’archive pour chaque utilisateur ; voir [Activer les boîtes aux lettres archive de sécurité Office 365 &amp; centre de conformité](enable-archive-mailboxes.md) et [Activer l’archivage illimité dans Office 365](enable-unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="77a27-375">Enable the archive mailbox for each user; see [Enable archive mailboxes in the Office 365 Security &amp; Compliance Center](enable-archive-mailboxes.md) and [Enable unlimited archiving in Office 365](enable-unlimited-archiving.md).</span></span>
    
2. <span data-ttu-id="77a27-376">Placer les boîtes aux lettres en conservation pour litige ou appliquer une stratégie de rétention Office 365 ; consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="77a27-376">Place user mailboxes on Litigation Hold or apply an Office 365 retention policy; see one of the following topics:</span></span> 
    
    - [<span data-ttu-id="77a27-377">Place a mailbox on Litigation Hold</span><span class="sxs-lookup"><span data-stu-id="77a27-377">Place a mailbox on Litigation Hold</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
    - [<span data-ttu-id="77a27-378">Vue d'ensemble des stratégies de rétention</span><span class="sxs-lookup"><span data-stu-id="77a27-378">Overview of retention policies in Office 365</span></span>](retention-policies.md)
    
    <span data-ttu-id="77a27-379">Comme indiqué précédemment, lorsque vous placez des boîtes aux lettres en conservation, vous pouvez définir la durée de conservation des éléments de la source de données tierces ou vous pouvez choisir de les conserver indéfiniment.</span><span class="sxs-lookup"><span data-stu-id="77a27-379">As previously stated, when you place mailboxes on hold, you can set a duration for how long to hold items from the third-party data source or you can choose to hold items indefinitely.</span></span>

## <a name="step-4-provide-your-partner-with-information"></a><span data-ttu-id="77a27-380">Étape 4 : fournir des informations au partenaire</span><span class="sxs-lookup"><span data-stu-id="77a27-380">Step 4: Provide your partner with information</span></span>

<span data-ttu-id="77a27-381">La dernière étape consiste à fournir à votre partenaire les informations suivantes pour lui permettre de configurer le connecteur afin qu’il se connecte à votre organisation Office 365 pour importer les données vers les boîtes aux lettres des utilisateurs et la boîte aux lettres de données tierces.</span><span class="sxs-lookup"><span data-stu-id="77a27-381">The final step is to provide your partner with the following information so they can configure the connector to connect to your Office 365 organization to import data to user mailboxes and to the third-party data mailbox.</span></span> 
  
- <span data-ttu-id="77a27-382">Le point de terminaison utilisé pour se connecter au service Azure dans Office 365 :</span><span class="sxs-lookup"><span data-stu-id="77a27-382">The endpoint used to connect to the Azure service in Office 365:</span></span>

    ```
    https://office365ingestionsvc.gble1.protection.outlook.com/service/ThirdPartyIngestionService.svc
    ```

- <span data-ttu-id="77a27-p117">La connexion dans les informations d’identification (Office 365 ID d’utilisateur et mot de passe) de la boîte aux lettres des données tierces que vous avez créé à l’étape 2. Ces informations d’identification sont nécessaires pour que le connecteur de partenaires permettre accéder et importer des éléments à des boîtes aux lettres utilisateur et à la boîte aux lettres des données tierces.</span><span class="sxs-lookup"><span data-stu-id="77a27-p117">The sign in credentials (Office 365 user ID and password) of the third-party data mailbox that you created in Step 2. These credentials are required so that the partner connector can access and import items to user mailboxes and to the third-party data mailbox.</span></span>
 
## <a name="step-5-register-the-third-party-data-connector-in-azure-active-directory"></a><span data-ttu-id="77a27-385">Étape 5 : Enregistrer le connecteur des données tierces dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="77a27-385">Step 5: Register the third-party data connector in Azure Active Directory</span></span>

<span data-ttu-id="77a27-p118">Démarrage du 30 septembre 2018, le service Azure dans Office 365 commencera utilisant l’authentification moderne dans Exchange Online pour authentifier les connecteurs de données tierce qui tentent de se connecter à votre organisation Office 365 pour importer des données. Pour que cette modification parce que l’authentification moderne offre davantage de sécurité que la méthode actuelle, qui repose sur la création de listes autorisées les connecteurs tiers qui utilisent le point de terminaison décrit précédemment pour se connecter au service Azure.</span><span class="sxs-lookup"><span data-stu-id="77a27-p118">Starting September 30, 2018, the Azure service in Office 365 will begin using modern authentication in Exchange Online to authenticate third-party data connectors that attempt to connect to your Office 365 organization to import data. The reason for this change is that modern authentication provides more security than the current method, which was based on whitelisting third-party connectors that use the previously described endpoint to connect to the Azure service.</span></span>

<span data-ttu-id="77a27-p119">Pour activer un connecteur tiers pour se connecter à Office 365 à l’aide de la nouvelle méthode d’authentification moderne, un administrateur de votre organisation Office 365 doit consentement pour inscrire le connecteur comme une application de service approuvé dans Azure Active Directory. Cela s’effectue par l’acceptation d’une demande d’autorisations pour autoriser le connecteur accéder aux données de votre organisation dans Azure Active Directory. Après avoir accepté cette demande, le connecteur de données tiers est ajouté en tant qu’une application d’entreprise pour Azure Active Directory et représenté sous la forme d’un principal de service. Pour plus d’informations le processus d’autorisation, voir [Consentement de client d’administration](https://docs.microsoft.com/en-us/skype-sdk/trusted-application-api/docs/tenantadminconsent).</span><span class="sxs-lookup"><span data-stu-id="77a27-p119">To enable a third-party data connector to connect to Office 365 using the new modern authentication method, an administrator in your Office 365 organization must consent to register the connector as a trusted service application in Azure Active Directory. This is done by accepting a permissions request to allow the connector to access your organization's data in Azure Active Directory. After you accept this request, the third-party data connector is added as an enterprise application to Azure Active Directory and represented as a service principal. For more information the consent process, see  [Tenant Admin Consent](https://docs.microsoft.com/en-us/skype-sdk/trusted-application-api/docs/tenantadminconsent).</span></span>

<span data-ttu-id="77a27-392">Voici les étapes pour accéder et accepter la demande pour inscrire le connecteur :</span><span class="sxs-lookup"><span data-stu-id="77a27-392">Here are the steps to access and accept the request to register the connector:</span></span>

1. <span data-ttu-id="77a27-393">Accédez à [cette page](https://login.microsoftonline.com/common/oauth2/authorize?client_id=8dfbc50b-2111-4d03-9b4d-dd0d00aae7a2&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent) et vous connecter en utilisant les informations d’identification d’un administrateur global d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="77a27-393">Go to [this page](https://login.microsoftonline.com/common/oauth2/authorize?client_id=8dfbc50b-2111-4d03-9b4d-dd0d00aae7a2&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent) and sign in using the credentials of an Office 365 global administrator.</span></span><br/><br/><span data-ttu-id="77a27-p120">La boîte de dialogue s’affiche. Vous pouvez développer les crochets pour passer en revue les autorisations qui seront affectées au connecteur.</span><span class="sxs-lookup"><span data-stu-id="77a27-p120">The following dialog box is displayed. You can expand the carets to review the permissions that will be assigned to the connector.</span></span><br/><br/><span data-ttu-id="77a27-396">![La boîte de dialogue de demande d’autorisations s’affiche.](media/O365_ThirdPartyDataConnector_OptIn1.png)</span><span class="sxs-lookup"><span data-stu-id="77a27-396">![The permissions request dialog is displayed](media/O365_ThirdPartyDataConnector_OptIn1.png)</span></span>
2. <span data-ttu-id="77a27-397">Cliquez sur **Accepter**.</span><span class="sxs-lookup"><span data-stu-id="77a27-397">Click **Accept**.</span></span>

<span data-ttu-id="77a27-p121">Après avoir accepté la demande, le [portail Azure](https://portal.azure.com) s’affiche. Pour afficher la liste des applications pour votre organisation, cliquez sur **Azure Active Directory** > **applications d’entreprise**. Le connecteur de données tierce Office 365 est répertorié sur la blade **d’applications d’entreprise** .</span><span class="sxs-lookup"><span data-stu-id="77a27-p121">After you accept the request, the [Azure portal](https://portal.azure.com) is displayed. To view the list of applications for your organization, click **Azure Active Directory** > **Enterprise applications**. The Office 365 third-party data connector is listed on the **Enterprise applications** blade.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="77a27-p122">Après 30 septembre 2018, les données tiers ne seront n’est plus importées dans les boîtes aux lettres dans votre organisation si vous n’enregistrez un connecteur tiers dans Azure Active Directory. Remarque existants aux connecteurs de données de tiers (ceux créés avant le 30 septembre 2018) doit également être enregistré dans Azure Active Directory en suivant la procédure à l’étape 5.</span><span class="sxs-lookup"><span data-stu-id="77a27-p122">After September 30, 2018, third-party data will no longer be imported into mailboxes in your organization if you don't register a third-party data connector in Azure Active Directory. Note existing third-party data connectors (those created before September 30, 2018) must also be registered in Azure Active Directory by following the procedure in Step 5.</span></span>

### <a name="revoking-consent-for-a-third-party-data-connector"></a><span data-ttu-id="77a27-403">Révoquer le consentement de l’utilisateur pour un connecteur tiers</span><span class="sxs-lookup"><span data-stu-id="77a27-403">Revoking consent for a third-party data connector</span></span>

<span data-ttu-id="77a27-p123">Une fois que votre organisation consent à la demande d’autorisations pour inscrire un connecteur tiers dans Azure Active Directory, votre organisation peut révoquer cette autorisation à tout moment. Toutefois, révoquer l’autorisation d’un connecteur signifie que les données à partir de la source de données tierce ne seront importées dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="77a27-p123">After your organization consents to the permissions request to register a third-party data connector in Azure Active Directory, your organization can revoke that consent at any time. However, revoking the consent for a connector will mean that data from the third-party data source will no longer be imported into Office 365.</span></span>

<span data-ttu-id="77a27-p124">Pour révoquer l’autorisation pour un connecteur tiers, vous pouvez supprimer l’application (en supprimant le principal de service correspondant) d’Azure Active Directory à l’aide de la lame **d’applications d’entreprise** dans le portail Azure, ou à l’aide de la [ Remove-MsolServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/msonline/remove-msolserviceprincipal) dans Office 365 PowerShell. Vous pouvez également utiliser l’applet de commande [Remove-AzureADServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/azuread/remove-azureadserviceprincipal) dans Windows Azure Active Directory PowerShell.</span><span class="sxs-lookup"><span data-stu-id="77a27-p124">To revoke consent for a third-party data connector, you can delete the application (by deleting the corresponding service principal) from Azure Active Directory using the **Enterprise applications** blade in the Azure portal, or by using the [Remove-MsolServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/msonline/remove-msolserviceprincipal) in Office 365 PowerShell. You can also use the [Remove-AzureADServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/azuread/remove-azureadserviceprincipal) cmdlet in Azure Active Directory PowerShell.</span></span>
  
## <a name="more-information"></a><span data-ttu-id="77a27-408">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="77a27-408">More information</span></span>

- <span data-ttu-id="77a27-p125">Indiqué comme précédent, les éléments à partir des données tiers sources sont importées dans les boîtes aux lettres Exchange en tant que messages électroniques. Le connecteur de partenaire importe l’élément à l’aide d’un schéma requis par l’API d’Office 365. Le tableau suivant décrit les propriétés de message d’un élément à partir d’une source de données tierce après l’importation de boîte aux lettres Exchange en tant qu’un message électronique. Le tableau indique également si la propriété message est obligatoire. Les propriétés obligatoires doivent être remplies. Si un élément ne dispose pas d’une propriété obligatoire, il ne seront pas importée vers Office 365. Le processus d’importation renverra un message d’erreur expliquant pourquoi un élément n’a pas été importé et que la propriété est manquante.</span><span class="sxs-lookup"><span data-stu-id="77a27-p125">As previous explained, items from third-party data sources are imported to Exchange mailboxes as email messages. The partner connector imports the item using a schema required by the Office 365 API. The following table describes the message properties of an item from a third-party data source after it's imported to an Exchange mailbox as an email message. The table also indicates if the message property is mandatory. Mandatory properties must be populated. If an item is missing a mandatory property, it won't be imported to Office 365. The import process will return an error message explaining why an item wasn't imported and which property is missing.</span></span>
    
    |<span data-ttu-id="77a27-416">**Propriété de message**</span><span class="sxs-lookup"><span data-stu-id="77a27-416">**Message property**</span></span>|<span data-ttu-id="77a27-417">**Obligatoire ?**</span><span class="sxs-lookup"><span data-stu-id="77a27-417">**Mandatory?**</span></span>|<span data-ttu-id="77a27-418">**Description**</span><span class="sxs-lookup"><span data-stu-id="77a27-418">**Description**</span></span>|<span data-ttu-id="77a27-419">**Exemple de valeur**</span><span class="sxs-lookup"><span data-stu-id="77a27-419">**Example value**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="77a27-420">**FROM**</span><span class="sxs-lookup"><span data-stu-id="77a27-420">**FROM**</span></span> <br/> |<span data-ttu-id="77a27-421">Oui</span><span class="sxs-lookup"><span data-stu-id="77a27-421">Yes</span></span>  <br/> |<span data-ttu-id="77a27-p126">L’utilisateur qui a créé à l’origine ou de l’élément envoyé dans la source de données tierce. Le connecteur de partenaire tente de mapper l’ID d’utilisateur de la source (par exemple une poignée Twitter) à un compte d’utilisateur Office 365 pour tous les participants (utilisateurs dans les champs FROM et TO). Une copie du message sera importée dans la boîte aux lettres de tous les participants. Si aucun des participants à partir de l’élément peut être mappé à un compte d’utilisateur Office 365, l’élément sera importé dans la boîte aux lettres d’archivage tiers dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="77a27-p126">The user who originally created or sent the item in the third-party data source. The partner connector will attempt to map the user ID from the source item (for example a Twitter handle) to an Office 365 user account for all participants (users in the FROM and TO fields). A copy of the message will be imported to the mailbox of every participant. If none of the participants from the item can be mapped to an Office 365 user account, the item will be imported to the third-party archiving mailbox in Office 365.  </span></span><br/> <br/> <span data-ttu-id="77a27-p127">Le participant qui est identifié en tant que l’expéditeur de l’élément doit avoir une boîte aux lettres active dans l’organisation Office 365 qui l’élément en cours d’importation. Si l’expéditeur ne possède une boîte aux lettres active, le message d’erreur suivant est retourné :</span><span class="sxs-lookup"><span data-stu-id="77a27-p127">The participant who's identified as the sender of the item must have an active mailbox in the Office 365 organization that the item is being imported to. If the sender doesn't have an active mailbox, the following error is returned:</span></span><br/><br/>  `One or more messages in the Request failed to be delivered to either From or Sender email address. You will need to resend your entire Request. Error: The request failed. The remote server returned an error: (401) Unauthorized.`  | `bob@contoso.com` <br/> |
    |<span data-ttu-id="77a27-428">**TO**</span><span class="sxs-lookup"><span data-stu-id="77a27-428">**TO**</span></span> <br/> |<span data-ttu-id="77a27-429">Oui</span><span class="sxs-lookup"><span data-stu-id="77a27-429">Yes</span></span>  <br/> |<span data-ttu-id="77a27-430">Utilisateur qui a reçu un élément, le cas échéant, pour un élément dans la source de données.</span><span class="sxs-lookup"><span data-stu-id="77a27-430">The user who received an item, if applicable for an item in the data source.</span></span>  <br/> | `bob@contoso.com` <br/> |
    |<span data-ttu-id="77a27-431">**SUBJECT**</span><span class="sxs-lookup"><span data-stu-id="77a27-431">**SUBJECT**</span></span> <br/> |<span data-ttu-id="77a27-432">Non</span><span class="sxs-lookup"><span data-stu-id="77a27-432">No</span></span>  <br/> |<span data-ttu-id="77a27-433">Objet de l’élément source.</span><span class="sxs-lookup"><span data-stu-id="77a27-433">The subject from the source item.</span></span>  <br/> | `"Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/> |
    |<span data-ttu-id="77a27-434">**DATE**</span><span class="sxs-lookup"><span data-stu-id="77a27-434">**DATE**</span></span> <br/> |<span data-ttu-id="77a27-435">Oui</span><span class="sxs-lookup"><span data-stu-id="77a27-435">Yes</span></span>  <br/> |<span data-ttu-id="77a27-436">Date à laquelle l’élément a été initialement créé ou publié dans la source de données du client, par exemple, date à laquelle un message Twitter a été publié.</span><span class="sxs-lookup"><span data-stu-id="77a27-436">The date the item was originally created or posted in the customer data source; for example, that date when a Twitter message was tweeted.</span></span>  <br/> | `01 NOV 2015` <br/> |
    |<span data-ttu-id="77a27-437">**BODY**</span><span class="sxs-lookup"><span data-stu-id="77a27-437">**BODY**</span></span> <br/> |<span data-ttu-id="77a27-438">Non</span><span class="sxs-lookup"><span data-stu-id="77a27-438">No</span></span>  <br/> |<span data-ttu-id="77a27-p128">Le contenu du message ou du billet. Pour des sources de données, le contenu de cette propriété peut être la même que le contenu de la propriété **SUBJECT** . Pendant le processus d’importation, le connecteur partenaire tente de mettre à jour de fidélité à partir de la source de contenu que possible. Dans la mesure du possible les fichiers, des graphiques ou tout autre contenu dans le corps de l’élément source est inclus dans cette propriété. Dans le cas contraire, le contenu de la source est inclus dans la propriété de **pièce jointe** . Le contenu de cette propriété dépendent sur le connecteur de partenaire et de la capacité de la plateforme de la source.</span><span class="sxs-lookup"><span data-stu-id="77a27-p128">The contents of the message or post. For some data sources, the contents of this property could be the same as the content for the **SUBJECT** property. During the import process, the partner connector will attempt to maintain full fidelity from the content source as possible. If possible files, graphics, or other content from the body of the source item is included in this property. Otherwise, content from the source item is included in the **ATTACHMENT** property. The contents of this property will depend on the partner connector and on the capability of the source platform.  </span></span><br/> | `Author: bob@contoso.com` <br/>  `Date: 10 DEC 2014` <br/>  `Tweet: "Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/>  `Date: 01 NOV 2015` <br/> |
    |<span data-ttu-id="77a27-445">**ATTACHMENT**</span><span class="sxs-lookup"><span data-stu-id="77a27-445">**ATTACHMENT**</span></span> <br/> |<span data-ttu-id="77a27-446">Non</span><span class="sxs-lookup"><span data-stu-id="77a27-446">No</span></span>  <br/> |<span data-ttu-id="77a27-p129">Si un élément dans la source de données (par exemple, un tweet Twitter ou une conversation par messagerie instantanée) contient une pièce jointe ou inclure des images, le partenaire connecté sera première tentative à inclure des pièces jointes dans la propriété **BODY** . Si ce n’est pas possible, puis elle est ajoutée à la \*\* pièce jointe \*\* propriété. D’autres exemples de pièces jointes incluent j’aime dans Facebook, les métadonnées à partir de la source de contenu et les réponses à un message ou d’un billet.</span><span class="sxs-lookup"><span data-stu-id="77a27-p129">If an item in the data source (such as a tweet in Twitter or an instant messaging conversation) has an attached file or include images, the partner connect will first attempt to include attachments in the **BODY** property. If that isn't possible, then it's added to the \*\* ATTACHMENT \*\* property. Other examples of attachments include Likes in Facebook, metadata from the content source, and responses to a message or post.  </span></span><br/> | `image.gif` <br/> |
    |<span data-ttu-id="77a27-450">**MESSAGECLASS**</span><span class="sxs-lookup"><span data-stu-id="77a27-450">**MESSAGECLASS**</span></span> <br/> |<span data-ttu-id="77a27-451">Oui</span><span class="sxs-lookup"><span data-stu-id="77a27-451">Yes</span></span>  <br/> | <span data-ttu-id="77a27-p130">Il s’agit d’une propriété à valeurs multiples, qui est créée et remplie par connecteur partenaire. Le format de cette propriété est `IPM.NOTE.Source.Event`. (Cette propriété doit commencer par `IPM.NOTE`; ce format est similaire à celui de la `IPM.NOTE.X` classe de message.) Cette propriété consacrée les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="77a27-p130">This is a multi-value property, which is created and populated by partner connector. The format of this property is  `IPM.NOTE.Source.Event`. (This property must begin with  `IPM.NOTE`; this format is similar to the one for the  `IPM.NOTE.X` message class.) This property includes the following information:  </span></span><br/><br/><span data-ttu-id="77a27-455">`Source`-Indique la source de données tierce ; par exemple, Twitter, Facebook ou BlackBerry.</span><span class="sxs-lookup"><span data-stu-id="77a27-455">`Source` - Indicates the third-party data source; for example, Twitter, Facebook, or BlackBerry.</span></span>  <br/> <br/>  <span data-ttu-id="77a27-p131">`Event`-Indique le type d’activité qui a été effectuée dans la source de données tierce qui a produit les éléments ; par exemple, un tweet Twitter ou une publication dans Facebook. Les événements sont spécifiques à la source de données.</span><span class="sxs-lookup"><span data-stu-id="77a27-p131">`Event` - Indicates the type of activity that was performed in the third-party data source that produced the items; for example, a tweet in Twitter or a post in Facebook. Events are specific to the data source.  </span></span><br/> <br/>  <span data-ttu-id="77a27-p132">Un des objectifs de cette propriété sont de filtrer des éléments spécifiques en fonction de la source de données où un élément à l’origine ou en fonction du type d’événement. Par exemple, dans une recherche de découverte, vous pouvez créer une requête de recherche pour trouver tous les tweet qui ont été validées par un utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="77a27-p132">One purpose of this property is to filter specific items based on the data source where an item originated or based on the type of event. For example, in an eDiscovery search you could create a search query to find all the tweets that were posted by a specific user.  </span></span><br/> | `IPM.NOTE.Twitter.Tweet` <br/> |
   
- <span data-ttu-id="77a27-p133">Lorsque les éléments sont importés correctement aux boîtes aux lettres dans Office 365, un identificateur unique est renvoyé à l’appelant dans le cadre de la réponse HTTP. Cet identificateur — appelé `x-IngestionCorrelationID`— peut être utilisé à des fins de résolution des problèmes suivants par les partenaires pour le suivi de bout en bout d’éléments. Il est recommandé de partenaires capturent ces informations et ouvrez une session en conséquence à leur fin. Voici un exemple d’une réponse HTTP avec cet identificateur :</span><span class="sxs-lookup"><span data-stu-id="77a27-p133">When items are successfully imported to mailboxes in Office 365, a unique identifier is returned back to the caller as part of the HTTP response. This identifier—called  `x-IngestionCorrelationID`—can be used for subsequent troubleshooting purposes by partners for end-to-end tracking of items. It's recommended that partners capture this information and log it accordingly at their end. Here's an example of an HTTP response showing this identifier:</span></span>

    ```
    HTTP/1.1 200 OK
    Content-Type: text/xml; charset=utf-8
    Server: Microsoft-IIS/8.5
    x-IngestionCorrelationID: 1ec7667d-f097-47fe-a9a2-bc7ab0a7552b
    X-AspNet-Version: 4.0.30319
    X-Powered-By: ASP.NET
    Date: Tue, 02 Feb 2016 22:55:33 GMT 
    ```
 
- <span data-ttu-id="77a27-p134">Vous pouvez utiliser l’outil de recherche de contenu de sécurité Office 365 &amp; centre de conformité pour rechercher des éléments qui ont été importés pour les boîtes aux lettres dans Office 365 à partir d’une source de données tierce. Pour rechercher spécifiquement ces éléments importés, vous pouvez utiliser les paires de valeur de la propriété message suivantes dans la zone mots clés pour une recherche de contenu. .</span><span class="sxs-lookup"><span data-stu-id="77a27-p134">You can use the Content Search tool in the Office 365 Security &amp; Compliance Center to search for items that were imported to mailboxes in Office 365 from a third-party data source. To search specifically for these imported items, you can use the following message property-value pairs in the keyword box for a Content Search. .</span></span> 
    
  - <span data-ttu-id="77a27-p135">**`kind:externaldata`**-Utilisez cette paire de valeur de la propriété pour rechercher tous les types de données de tiers. Par exemple, pour rechercher des éléments qui ont été importés à partir d’une source de données tierce et contenu dans le mot « contoso » dans la propriété Subject de l’élément importé, vous utiliseriez la requête de mot clé `kind:externaldata AND subject:contoso`.</span><span class="sxs-lookup"><span data-stu-id="77a27-p135">**`kind:externaldata`** - Use this property-value pair to search all third-party data types. For example, to search for items that were imported from a third-party data source and contained the word "contoso" in the Subject property of the imported item, you would use the keyword query  `kind:externaldata AND subject:contoso`.</span></span>
    
  - <span data-ttu-id="77a27-p136">**`itemclass:ipm.externaldata.<third-party data type>`**-Utilisez cette paire de valeur de la propriété pour rechercher un type de spécifier des données tiers uniquement. Par exemple, pour rechercher uniquement les données Facebook qui contient le mot « contoso » dans la propriété Subject, utiliser la requête de mot clé `itemclass:ipm.externaldata.Facebook* AND subject:contoso`.</span><span class="sxs-lookup"><span data-stu-id="77a27-p136">**`itemclass:ipm.externaldata.<third-party data type>`** - Use this property-value pair to only search a specify type of third-party data. For example, to only search Facebook data that contains the word "contoso" in the Subject property, you would use the keyword query  `itemclass:ipm.externaldata.Facebook* AND subject:contoso`.</span></span> 

  <span data-ttu-id="77a27-471">Pour obtenir la liste complète des valeurs à utiliser pour les types de données de tiers pour la `itemclass` propriété, voir [Recherche de contenu utiliser pour rechercher des données tierces qui a été importées dans Office 365](use-content-search-to-search-third-party-data-that-was-imported.md)</span><span class="sxs-lookup"><span data-stu-id="77a27-471">For a complete list of values to use for third-party data types for the  `itemclass` property, see [Use Content Search to search third-party data that was imported to Office 365](use-content-search-to-search-third-party-data-that-was-imported.md)</span></span>
    
   <span data-ttu-id="77a27-472">Pour plus d’informations sur l’utilisation de la recherche de contenu et la création de requêtes de recherche de mots clés, voir :</span><span class="sxs-lookup"><span data-stu-id="77a27-472">For more information about using Content Search and creating keyword search queries, see:</span></span>
    
  - [<span data-ttu-id="77a27-473">Recherche de contenu dans Office 365</span><span class="sxs-lookup"><span data-stu-id="77a27-473">Content Search in Office 365</span></span>](content-search.md)
    
  - [<span data-ttu-id="77a27-474">Requêtes par mots clés et conditions de recherche pour la recherche de contenu</span><span class="sxs-lookup"><span data-stu-id="77a27-474">Keyword queries and search conditions for Content Search</span></span>](keyword-queries-and-search-conditions.md)
 
