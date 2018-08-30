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
ms.openlocfilehash: 3d51d9f5cb546b33fa636fab0ca319e4d24b1ad4
ms.sourcegitcommit: edf5db9357c0d34573f8cc406314525ef10d1eb9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/28/2018
ms.locfileid: "23230036"
---
# <a name="archiving-third-party-data-in-office-365"></a><span data-ttu-id="03554-105">Archivage de données tierces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="03554-105">Archiving third-party data in Office 365</span></span>

<span data-ttu-id="03554-p102">Permet d’Office 365 administrateurs importer et archiver des données tierces à partir de plateformes de médias sociaux, de messagerie instantanée plateformes et plates-formes de collaboration de documents, aux boîtes aux lettres dans votre organisation Office 365. Exemples de tiers de sources de données que vous pouvez importer dans Office 365 sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="03554-p102">Office 365 lets administrators import and archive third-party data from social media platforms, instant messaging platforms, and document collaboration platforms, to mailboxes in your Office 365 organization. Examples of third-party data sources that you can import to Office 365 include the following:</span></span> 
  
- <span data-ttu-id="03554-108">**Mise en réseau** - Twitter, Facebook, Yammer et LinkedIn</span><span class="sxs-lookup"><span data-stu-id="03554-108">**Social** - Twitter, Facebook, Yammer, and LinkedIn</span></span> 
    
- <span data-ttu-id="03554-109">**Messagerie instantanée** - Yahoo Messenger, GoogleTalk et Cisco Jabber</span><span class="sxs-lookup"><span data-stu-id="03554-109">**Instant messaging** - Yahoo Messenger, GoogleTalk, and Cisco Jabber</span></span> 
    
- <span data-ttu-id="03554-110">**Collaboration sur des documents** - zone et échange</span><span class="sxs-lookup"><span data-stu-id="03554-110">**Document collaboration** - Box and DropBox</span></span> 
    
- <span data-ttu-id="03554-111">**Secteurs verticaux** - Finance (comme Thomson Reuters et Bloomberg) et gestion des relations client (par exemple, brouillage force de vente)</span><span class="sxs-lookup"><span data-stu-id="03554-111">**Vertical industries** - Customer Relationship Management (such as Salesforce Chatter) and Financials (such as Thomson Reuters and Bloomberg)</span></span> 
    
- <span data-ttu-id="03554-112">**Messagerie texte/SMS** - BlackBerry</span><span class="sxs-lookup"><span data-stu-id="03554-112">**SMS/text messaging** - BlackBerry</span></span> 
    
<span data-ttu-id="03554-p103">Après l’importation des données tierces, vous pouvez appliquer des fonctionnalités de conformité d’Office 365, telles que les stratégies de rétention litige, recherche de contenu, d’archivage sur Place, audit et Office 365 — à ces données. Par exemple, lorsqu’une boîte aux lettres est mis en attente pour litige, des données tierces seront préservées. Vous pouvez rechercher des données tierces à l’aide de la recherche de contenu. Ou vous pouvez appliquer l’archivage et les stratégies de rétention pour des données tierces comme vous pouvez utiliser pour les données de Microsoft. En bref, l’archivage des données tierces dans Office 365 peut aider votre organisation respecter les administrations et réglementaires.</span><span class="sxs-lookup"><span data-stu-id="03554-p103">After third-party data is imported, you can apply Office 365 compliance features—such as Litigation Hold, Content Search, In-Place Archiving, Auditing, and Office 365 retention policies—to this data. For example, when a mailbox is placed on Litigation Hold, third-party data will be preserved. You can search third-party data by using Content Search. Or you can apply archiving and retention polices to third-party data just like you can for Microsoft data. In short, archiving third-party data in Office 365 can help your organization stay compliant with government and regulatory policies.</span></span>
  
<span data-ttu-id="03554-118">Voici une vue d’ensemble du processus et les étapes nécessaires pour importer des données de tiers pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="03554-118">Here's an overview of the process and the steps necessary to import third-party data to Office 365.</span></span>

[<span data-ttu-id="03554-119">Étape 1 : trouver un partenaire de données tierces</span><span class="sxs-lookup"><span data-stu-id="03554-119">Step 1: Find a third-party data partner</span></span>](#step-1-find-a-third-party-data-partner)

[<span data-ttu-id="03554-120">Étape 2 : créer et configurer une boîte aux lettres pour les données tierces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="03554-120">Step 2: Create and configure a third-party data mailbox in Office 365</span></span>](#step-2-create-and-configure-a-third-party-data-mailbox-in-office-365)

[<span data-ttu-id="03554-121">Étape 3 : configurer des boîtes aux lettres d’utilisateurs pour les données tierces</span><span class="sxs-lookup"><span data-stu-id="03554-121">Step 3: Configure user mailboxes for third-party data</span></span>](#step-3-configure-user-mailboxes-for-third-party-data)

[<span data-ttu-id="03554-122">Étape 4 : fournir des informations au partenaire</span><span class="sxs-lookup"><span data-stu-id="03554-122">Step 4: Provide your partner with information</span></span>](#step-4-provide-your-partner-with-information)

## <a name="how-the-third-party-data-import-process-works"></a><span data-ttu-id="03554-123">Fonctionnement de la façon dont les données tiers processus d’importation ></span><span class="sxs-lookup"><span data-stu-id="03554-123">How the third-party data import process works></span></span>

<span data-ttu-id="03554-124">L’illustration et la description suivantes expliquent le fonctionnement du processus d’importation de données tierces.</span><span class="sxs-lookup"><span data-stu-id="03554-124">The following illustration and description explain how the third-party data import process works.</span></span>
  
![Fonctionnement du processus d’importation de données tierces](media/5d4cf8e9-b4cc-4547-90c8-d12d04a9f0e7.png)
  
1. <span data-ttu-id="03554-126">Client fonctionne avec leur partenaire de choix pour configurer un connecteur d’extraire des éléments de la source de données tierce et puis importez ces éléments vers Office 365.</span><span class="sxs-lookup"><span data-stu-id="03554-126">Customer works with their partner of choice to configure a connector that will extract items from the third-party data source and then import those items to Office 365.</span></span>
    
2. <span data-ttu-id="03554-p104">Le connecteur de partenaire se connecte aux sources de données de tiers via une API de tiers (sur une base planifiée ou configuré en tant que) et extrait les éléments de la source de données. Le connecteur de partenaire convertit le contenu d’un élément dans un format de message électronique. Voir la section [plus d’informations](#more-information) pour une description du schéma de format de message.</span><span class="sxs-lookup"><span data-stu-id="03554-p104">The partner connector connects to third-party data sources via a third-party API (on a scheduled or as-configured basis) and extracts items from the data source. The partner connector converts the content of an item to an email message format. See the [More information](#more-information) section for a description of the message format schema.</span></span> 
    
3. <span data-ttu-id="03554-130">Connecteur de partenaire se connecte au service Azure dans Office 365 à l’aide d’Exchange Web Services (EWS) par le biais d’un point de terminaison connu.</span><span class="sxs-lookup"><span data-stu-id="03554-130">Partner connector connects to the Azure service in Office 365 by using Exchange Web Service (EWS) via a well-known end point.</span></span>
    
4. <span data-ttu-id="03554-p105">Les éléments sont importés dans la boîte aux lettres d’un utilisateur spécifique ou dans une boîte aux lettres « fourre-tout » destinée aux données tierces. L’importation d’un élément dans la boîte aux lettres d’un utilisateur spécifique ou dans la boîte aux lettres de données tierces repose sur les critères suivants :</span><span class="sxs-lookup"><span data-stu-id="03554-p105">Items are imported into the mailbox of a specific user or into a "catch-all" third-party data mailbox. Whether an item is imported into a specific user mailbox or to the third-party data mailbox is based on the following criteria:</span></span>
    
    <span data-ttu-id="03554-p106">**éléments qui ont un ID d’utilisateur qui correspond à un compte d’utilisateur Office 365** - si le connecteur de partenaire pouvez mapper l’ID utilisateur de l’élément dans la source de données tiers à un utilisateur spécifique ID dans Office 365, l’élément est copié dans le dossier de **purge** de l’utilisateur d’a. Dossier éléments récupérables. Les utilisateurs ne peuvent pas accéder aux éléments dans le dossier de purge. Toutefois, vous pouvez utiliser les outils de découverte électronique Office 365 pour rechercher des éléments dans le dossier de purge.</span><span class="sxs-lookup"><span data-stu-id="03554-p106">a. **Items that have a user ID that corresponds to an Office 365 user account** - If the partner connector can map the user ID of the item in the third-party data source to a specific user ID in Office 365, the item is copied to the **Purges** folder in the user's Recoverable Items folder. Users can't access items in the Purges folder. However, you can use Office 365 eDiscovery tools to search for items in the Purges folder.</span></span>
    
    <span data-ttu-id="03554-p107">b. **les éléments qui n’ont pas un ID d’utilisateur qui correspond à un compte d’utilisateur Office 365** - si le connecteur de partenaire ne peut pas mapper l’ID utilisateur d’un élément à un utilisateur spécifique ID dans Office 365, l’élément est copié dans le dossier **boîte de réception** de la boîte aux lettres des données tierces. Importation d’éléments dans la boîte de réception permet de vous ou une personne de votre organisation à se connecter à la boîte aux lettres de tiers pour afficher et gérer ces éléments et voir si les modifications doivent être effectuées dans la configuration du connecteur partenaire.</span><span class="sxs-lookup"><span data-stu-id="03554-p107">b. **Items that don't have a user ID that corresponds to an Office 365 user account** - If the partner connector can't map the user ID of an item to a specific user ID in Office 365, the item is copied to the **Inbox** folder of the third-party data mailbox. Importing items to the inbox allows you or someone in your organization to sign in to the third-party mailbox to view and manage these items, and see if any adjustments need to be made in the partner connector configuration.</span></span>
 
## <a name="step-1-find-a-third-party-data-partner"></a><span data-ttu-id="03554-140">Étape 1 : trouver un partenaire de données tierces</span><span class="sxs-lookup"><span data-stu-id="03554-140">Step 1: Find a third-party data partner</span></span>

<span data-ttu-id="03554-p108">Un composant essentiel pour l’archivage des données tierces dans Office 365 est recherche et utilisation d’un partenaire Microsoft spécialisée dans la capture des données à partir d’une source de données de tiers et importées dans Office 365. Une fois que les données sont importées, il peut être archivée et conservé avec votre organisation d’autres données Microsoft, tels que le courrier électronique à partir d’Exchange et des documents dans SharePoint et OneDrive for Business. Un partenaire crée un connecteur qui extrait les données à partir de sources de données tierces de votre organisation (tels que BlackBerry, Facebook, Google +, Reuters Thomson, Twitter et YouTube) et transmet les données à une API Office 365 qui importe les éléments dans les boîtes aux lettres Exchange en tant que les messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="03554-p108">A key component for archiving third-party data in Office 365 is finding and working with a Microsoft partner that specializes in capturing data from a third-party data source and importing it to Office 365. After the data is imported, it can be archived and preserved along with your organization's other Microsoft data, such as email from Exchange and documents from SharePoint and OneDrive for Business. A partner creates a connector that extracts data from your organization's third-party data sources (such as BlackBerry, Facebook, Google+, Thomson Reuters, Twitter, and YouTube) and passes that data to an Office 365 API that imports items to Exchange mailboxes as email messages.</span></span> 
  
<span data-ttu-id="03554-144">Les sections suivantes répertorient les partenaires Microsoft et les sources de données tierces elles prennent en charge, qui participent au programme pour l’archivage des données tierces dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="03554-144">The following sections list the Microsoft partners—and the third-party data sources they support—that are participating in the program for archiving third-party data in Office 365.</span></span>

[<span data-ttu-id="03554-145">17a-4 LLC</span><span class="sxs-lookup"><span data-stu-id="03554-145">17a-4 LLC</span></span>](#17a-4-llc)
  
[<span data-ttu-id="03554-146">Actiance</span><span class="sxs-lookup"><span data-stu-id="03554-146">Actiance</span></span>](#actiance)
  
[<span data-ttu-id="03554-147">ArchiveSocial</span><span class="sxs-lookup"><span data-stu-id="03554-147">ArchiveSocial</span></span>](#archivesocial)
  
[<span data-ttu-id="03554-148">Globanet</span><span class="sxs-lookup"><span data-stu-id="03554-148">Globanet</span></span>](#globanet)
  
[<span data-ttu-id="03554-149">OpenText</span><span class="sxs-lookup"><span data-stu-id="03554-149">OpenText</span></span>](#opentext)
  
[<span data-ttu-id="03554-150">Verba</span><span class="sxs-lookup"><span data-stu-id="03554-150">Verba</span></span>](#verba)
  
### <a name="17a-4-llc"></a><span data-ttu-id="03554-151">17a-4 LLC</span><span class="sxs-lookup"><span data-stu-id="03554-151">17a-4 LLC</span></span>

<span data-ttu-id="03554-152">17a-4 LLC prend en charge les sources de données tierces suivantes :</span><span class="sxs-lookup"><span data-stu-id="03554-152">17a-4 LLC supports the following third-party data sources:</span></span>
  
- <span data-ttu-id="03554-153">BlackBerry</span><span class="sxs-lookup"><span data-stu-id="03554-153">BlackBerry</span></span>
    
- <span data-ttu-id="03554-154">Flux de données Bloomberg</span><span class="sxs-lookup"><span data-stu-id="03554-154">Bloomberg Data Streams</span></span>
    
- <span data-ttu-id="03554-155">Cisco Jabber</span><span class="sxs-lookup"><span data-stu-id="03554-155">Cisco Jabber</span></span>
    
- <span data-ttu-id="03554-156">FactSet</span><span class="sxs-lookup"><span data-stu-id="03554-156">FactSet</span></span>
    
- <span data-ttu-id="03554-157">HipChat</span><span class="sxs-lookup"><span data-stu-id="03554-157">HipChat</span></span>
    
- <span data-ttu-id="03554-158">InvestEdge</span><span class="sxs-lookup"><span data-stu-id="03554-158">InvestEdge</span></span>
    
- <span data-ttu-id="03554-159">LivePerson</span><span class="sxs-lookup"><span data-stu-id="03554-159">LivePerson</span></span>
    
- <span data-ttu-id="03554-160">
Flux de données MessageLabs
</span><span class="sxs-lookup"><span data-stu-id="03554-160">MessageLabs Data Streams</span></span>
    
- <span data-ttu-id="03554-161">OpenText</span><span class="sxs-lookup"><span data-stu-id="03554-161">OpenText</span></span>
    
- <span data-ttu-id="03554-162">Aide en direct « cliquer pour appeler » Oracle/ATG
</span><span class="sxs-lookup"><span data-stu-id="03554-162">Oracle/ATG 'click-to-call' Live Help</span></span>
    
- <span data-ttu-id="03554-163">Pivot IMTRADER
</span><span class="sxs-lookup"><span data-stu-id="03554-163">Pivot IMTRADER</span></span>
    
- <span data-ttu-id="03554-164">Microsoft SharePoint</span><span class="sxs-lookup"><span data-stu-id="03554-164">Microsoft SharePoint</span></span>
    
- <span data-ttu-id="03554-165">MindAlign</span><span class="sxs-lookup"><span data-stu-id="03554-165">MindAlign</span></span>
    
- <span data-ttu-id="03554-166">Sitrion One (Newsgator)</span><span class="sxs-lookup"><span data-stu-id="03554-166">Sitrion One (Newsgator)</span></span>
    
- <span data-ttu-id="03554-167">
Skype Entreprise (Lync/OCS)</span><span class="sxs-lookup"><span data-stu-id="03554-167">Skype for Business (Lync/OCS)</span></span>
    
- <span data-ttu-id="03554-168">
Skype Entreprise Online (Lync Online)
</span><span class="sxs-lookup"><span data-stu-id="03554-168">Skype for Business Online (Lync Online)</span></span>
    
- <span data-ttu-id="03554-169">Bases de données SQL</span><span class="sxs-lookup"><span data-stu-id="03554-169">SQL Databases</span></span>
    
- <span data-ttu-id="03554-170">
Squawker
</span><span class="sxs-lookup"><span data-stu-id="03554-170">Squawker</span></span>
    
- <span data-ttu-id="03554-171">Thomson Reuters Eikon Messenger
</span><span class="sxs-lookup"><span data-stu-id="03554-171">Thomson Reuters Eikon Messenger</span></span>
  
### <a name="actiance"></a><span data-ttu-id="03554-172">Actiance</span><span class="sxs-lookup"><span data-stu-id="03554-172">Actiance</span></span>

<span data-ttu-id="03554-173">[Actiance](https://www.actiance.com) prend en charge les sources de données tierces suivantes :</span><span class="sxs-lookup"><span data-stu-id="03554-173">[Actiance](https://www.actiance.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="03554-174">AIM</span><span class="sxs-lookup"><span data-stu-id="03554-174">AIM</span></span>
    
- <span data-ttu-id="03554-175">American Idol</span><span class="sxs-lookup"><span data-stu-id="03554-175">American Idol</span></span>
    
- <span data-ttu-id="03554-176">Apple Juice</span><span class="sxs-lookup"><span data-stu-id="03554-176">Apple Juice</span></span>
    
- <span data-ttu-id="03554-177">
AOL avec client Pivot
</span><span class="sxs-lookup"><span data-stu-id="03554-177">AOL with Pivot client</span></span>
    
- <span data-ttu-id="03554-178">Ares</span><span class="sxs-lookup"><span data-stu-id="03554-178">Ares</span></span>
    
- <span data-ttu-id="03554-179">Bazaar Voice</span><span class="sxs-lookup"><span data-stu-id="03554-179">Bazaar Voice</span></span>
    
- <span data-ttu-id="03554-180">Bear Share</span><span class="sxs-lookup"><span data-stu-id="03554-180">Bear Share</span></span>
    
- <span data-ttu-id="03554-181">Bit Torrent</span><span class="sxs-lookup"><span data-stu-id="03554-181">Bit Torrent</span></span>
    
- <span data-ttu-id="03554-182">BlackBerry Call Logs (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="03554-182">BlackBerry Call Logs (v5, v10, v12)</span></span>
    
- <span data-ttu-id="03554-183">BlackBerry Messenger (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="03554-183">BlackBerry Messenger (v5, v10, v12)</span></span>
    
- <span data-ttu-id="03554-184">BlackBerry PIN (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="03554-184">BlackBerry PIN (v5, v10, v12)</span></span>
    
- <span data-ttu-id="03554-185">BlackBerry SMS (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="03554-185">BlackBerry SMS (v5, v10, v12)</span></span>
    
- <span data-ttu-id="03554-186">Bloomberg Mail
</span><span class="sxs-lookup"><span data-stu-id="03554-186">Bloomberg Mail</span></span>
    
- <span data-ttu-id="03554-187">CellTrust</span><span class="sxs-lookup"><span data-stu-id="03554-187">CellTrust</span></span>
    
- <span data-ttu-id="03554-188">Chat Import
</span><span class="sxs-lookup"><span data-stu-id="03554-188">Chat Import</span></span>
    
- <span data-ttu-id="03554-189">Chat Real Time Logging and Policy
</span><span class="sxs-lookup"><span data-stu-id="03554-189">Chat Real Time Logging and Policy</span></span>
    
- <span data-ttu-id="03554-190">Chatter
</span><span class="sxs-lookup"><span data-stu-id="03554-190">Chatter</span></span>
    
- <span data-ttu-id="03554-191">Cisco par messagerie instantanée &amp; serveur de présence (v9.0.1, v9.1, v9.1.1 SU1, 10, v10.5.1 SU1)</span><span class="sxs-lookup"><span data-stu-id="03554-191">Cisco IM &amp; Presence Server (v9.0.1, v9.1, v9.1.1 SU1, v10, v10.5.1 SU1)</span></span>
    
- <span data-ttu-id="03554-192">Cisco Unified Presence Server (v8.6.3, v8.6.4, v8.6.5)
</span><span class="sxs-lookup"><span data-stu-id="03554-192">Cisco Unified Presence Server (v8.6.3, v8.6.4, v8.6.5)</span></span>
    
- <span data-ttu-id="03554-193">Collaboration Import
</span><span class="sxs-lookup"><span data-stu-id="03554-193">Collaboration Import</span></span>
    
- <span data-ttu-id="03554-194">Collaboration Real Time Logging
</span><span class="sxs-lookup"><span data-stu-id="03554-194">Collaboration Real Time Logging</span></span>
    
- <span data-ttu-id="03554-195">Direct Connect</span><span class="sxs-lookup"><span data-stu-id="03554-195">Direct Connect</span></span>
    
- <span data-ttu-id="03554-196">Facebook</span><span class="sxs-lookup"><span data-stu-id="03554-196">Facebook</span></span>
    
- <span data-ttu-id="03554-197">FactSet</span><span class="sxs-lookup"><span data-stu-id="03554-197">FactSet</span></span>
    
- <span data-ttu-id="03554-198">FastTrack</span><span class="sxs-lookup"><span data-stu-id="03554-198">FastTrack</span></span>
    
- <span data-ttu-id="03554-199">Gnutella</span><span class="sxs-lookup"><span data-stu-id="03554-199">Gnutella</span></span>
    
- <span data-ttu-id="03554-200">Google+
</span><span class="sxs-lookup"><span data-stu-id="03554-200">Google+</span></span>
    
- <span data-ttu-id="03554-201">GoToMyPC</span><span class="sxs-lookup"><span data-stu-id="03554-201">GoToMyPC</span></span>
    
- <span data-ttu-id="03554-202">Hopster</span><span class="sxs-lookup"><span data-stu-id="03554-202">Hopster</span></span>
    
- <span data-ttu-id="03554-203">HubConnex</span><span class="sxs-lookup"><span data-stu-id="03554-203">HubConnex</span></span>
    
- <span data-ttu-id="03554-204">IBM Connections (version 3.0.1, version 4.0, version 4.5, version 4.5 CR3, version 5)
</span><span class="sxs-lookup"><span data-stu-id="03554-204">IBM Connections (v3.0.1, v4.0, v4.5, v4.5 CR3, v5)</span></span>
    
- <span data-ttu-id="03554-205">IBM Connections Chat Cloud
</span><span class="sxs-lookup"><span data-stu-id="03554-205">IBM Connections Chat Cloud</span></span>
    
- <span data-ttu-id="03554-206">IBM Connections Social Cloud
</span><span class="sxs-lookup"><span data-stu-id="03554-206">IBM Connections Social Cloud</span></span>
    
- <span data-ttu-id="03554-207">IBM SameTime Advanced 8.5.2 IFR1
</span><span class="sxs-lookup"><span data-stu-id="03554-207">IBM SameTime Advanced 8.5.2 IFR1</span></span>
    
- <span data-ttu-id="03554-208">IBM SameTime Communicate 9.0
</span><span class="sxs-lookup"><span data-stu-id="03554-208">IBM SameTime Communicate 9.0</span></span>
    
- <span data-ttu-id="03554-209">IBM SameTime Community (version 8.0.2, version 8.5.1 IFR2, version 8.5.2 IFR1, version 9.1)
</span><span class="sxs-lookup"><span data-stu-id="03554-209">IBM SameTime Community (v8.0.2, v8.5.1 IFR2, v8.5.2 IFR1, v9.1)</span></span>
    
- <span data-ttu-id="03554-210">IBM SameTime Complete 9.0
</span><span class="sxs-lookup"><span data-stu-id="03554-210">IBM SameTime Complete 9.0</span></span>
    
- <span data-ttu-id="03554-211">IBM SameTime Conference 9.0
</span><span class="sxs-lookup"><span data-stu-id="03554-211">IBM SameTime Conference 9.0</span></span>
    
- <span data-ttu-id="03554-212">IBM SameTime Meeting 8.5.2 IFR1
</span><span class="sxs-lookup"><span data-stu-id="03554-212">IBM SameTime Meeting 8.5.2 IFR1</span></span>
    
- <span data-ttu-id="03554-213">ICE/YellowJacket</span><span class="sxs-lookup"><span data-stu-id="03554-213">ICE/YellowJacket</span></span>
    
- <span data-ttu-id="03554-214">IM Import
</span><span class="sxs-lookup"><span data-stu-id="03554-214">IM Import</span></span>
    
- <span data-ttu-id="03554-215">IM Real Time Logging and Policy
</span><span class="sxs-lookup"><span data-stu-id="03554-215">IM Real Time Logging and Policy</span></span>
    
- <span data-ttu-id="03554-216">Indii Messenger
</span><span class="sxs-lookup"><span data-stu-id="03554-216">Indii Messenger</span></span>
    
- <span data-ttu-id="03554-217">Instant Bloomberg
</span><span class="sxs-lookup"><span data-stu-id="03554-217">Instant Bloomberg</span></span>
    
- <span data-ttu-id="03554-218">IRC</span><span class="sxs-lookup"><span data-stu-id="03554-218">IRC</span></span>
    
- <span data-ttu-id="03554-219">Jive
</span><span class="sxs-lookup"><span data-stu-id="03554-219">Jive</span></span>
    
- <span data-ttu-id="03554-220">Jive 6 Real Time Logging (version 6, version 7)
</span><span class="sxs-lookup"><span data-stu-id="03554-220">Jive 6 Real Time Logging (v6, v7)</span></span>
    
- <span data-ttu-id="03554-221">Jive Import</span><span class="sxs-lookup"><span data-stu-id="03554-221">Jive Import</span></span>
    
- <span data-ttu-id="03554-222">JXTA</span><span class="sxs-lookup"><span data-stu-id="03554-222">JXTA</span></span>
    
- <span data-ttu-id="03554-223">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="03554-223">LinkedIn</span></span>
    
- <span data-ttu-id="03554-224">
Microsoft Lync (2010, 2013)
</span><span class="sxs-lookup"><span data-stu-id="03554-224">Microsoft Lync (2010, 2013)</span></span>
    
- <span data-ttu-id="03554-225">MFTP</span><span class="sxs-lookup"><span data-stu-id="03554-225">MFTP</span></span>
    
- <span data-ttu-id="03554-226">Microsoft Lync 2013 Voix
</span><span class="sxs-lookup"><span data-stu-id="03554-226">Microsoft Lync 2013 Voice</span></span>
    
- <span data-ttu-id="03554-227">Microsoft SharePoint (2010, 2013)
</span><span class="sxs-lookup"><span data-stu-id="03554-227">Microsoft SharePoint (2010, 2013)</span></span>
    
- <span data-ttu-id="03554-228">Microsoft SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="03554-228">Microsoft SharePoint Online</span></span>
    
- <span data-ttu-id="03554-229">Microsoft UC (Unified Communications)</span><span class="sxs-lookup"><span data-stu-id="03554-229">Microsoft UC (Unified Communications)</span></span>
    
- <span data-ttu-id="03554-230">MindAlign</span><span class="sxs-lookup"><span data-stu-id="03554-230">MindAlign</span></span>
    
- <span data-ttu-id="03554-231">Mobile Guard</span><span class="sxs-lookup"><span data-stu-id="03554-231">Mobile Guard</span></span>
    
- <span data-ttu-id="03554-232">MSN</span><span class="sxs-lookup"><span data-stu-id="03554-232">MSN</span></span>
    
- <span data-ttu-id="03554-233">My Space</span><span class="sxs-lookup"><span data-stu-id="03554-233">My Space</span></span>
    
- <span data-ttu-id="03554-234">NEONetwork</span><span class="sxs-lookup"><span data-stu-id="03554-234">NEONetwork</span></span>
    
- <span data-ttu-id="03554-235">Office 365 Lync dédié
</span><span class="sxs-lookup"><span data-stu-id="03554-235">Office 365 Lync Dedicated</span></span>
    
- <span data-ttu-id="03554-236">MI partagée Office 365
</span><span class="sxs-lookup"><span data-stu-id="03554-236">Office 365 Shared IM</span></span>
    
- <span data-ttu-id="03554-237">Pinterest</span><span class="sxs-lookup"><span data-stu-id="03554-237">Pinterest</span></span>
    
- <span data-ttu-id="03554-238">Pivot</span><span class="sxs-lookup"><span data-stu-id="03554-238">Pivot</span></span>
    
- <span data-ttu-id="03554-239">QQ</span><span class="sxs-lookup"><span data-stu-id="03554-239">QQ</span></span>
    
- <span data-ttu-id="03554-240">Skype Entreprise 2015</span><span class="sxs-lookup"><span data-stu-id="03554-240">Skype for Business 2015</span></span>
    
- <span data-ttu-id="03554-241">SoftEther</span><span class="sxs-lookup"><span data-stu-id="03554-241">SoftEther</span></span>
    
- <span data-ttu-id="03554-242">Symphony
</span><span class="sxs-lookup"><span data-stu-id="03554-242">Symphony</span></span>
    
- <span data-ttu-id="03554-243">Thomson Reuters Eikon
</span><span class="sxs-lookup"><span data-stu-id="03554-243">Thomson Reuters Eikon</span></span>
    
- <span data-ttu-id="03554-244">Thomson Reuters Messenger
</span><span class="sxs-lookup"><span data-stu-id="03554-244">Thomson Reuters Messenger</span></span>
    
- <span data-ttu-id="03554-245">Tor</span><span class="sxs-lookup"><span data-stu-id="03554-245">Tor</span></span>
    
- <span data-ttu-id="03554-246">TTT</span><span class="sxs-lookup"><span data-stu-id="03554-246">TTT</span></span>
    
- <span data-ttu-id="03554-247">Twitter</span><span class="sxs-lookup"><span data-stu-id="03554-247">Twitter</span></span>
    
- <span data-ttu-id="03554-248">WinMX</span><span class="sxs-lookup"><span data-stu-id="03554-248">WinMX</span></span>
    
- <span data-ttu-id="03554-249">Winny</span><span class="sxs-lookup"><span data-stu-id="03554-249">Winny</span></span>
    
- <span data-ttu-id="03554-250">Yahoo
</span><span class="sxs-lookup"><span data-stu-id="03554-250">Yahoo</span></span>
    
- <span data-ttu-id="03554-251">Yammer</span><span class="sxs-lookup"><span data-stu-id="03554-251">Yammer</span></span>
    
- <span data-ttu-id="03554-252">YouTube</span><span class="sxs-lookup"><span data-stu-id="03554-252">YouTube</span></span>
    
  
### <a name="archivesocial"></a><span data-ttu-id="03554-253">ArchiveSocial</span><span class="sxs-lookup"><span data-stu-id="03554-253">ArchiveSocial</span></span>

<span data-ttu-id="03554-254">[ArchiveSocial](https://www.archivesocial.com) prend en charge les sources de données tierces suivantes :</span><span class="sxs-lookup"><span data-stu-id="03554-254">[ArchiveSocial ](https://www.archivesocial.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="03554-255">Facebook</span><span class="sxs-lookup"><span data-stu-id="03554-255">Facebook</span></span>
    
- <span data-ttu-id="03554-256">Flickr
</span><span class="sxs-lookup"><span data-stu-id="03554-256">Flickr</span></span>
    
- <span data-ttu-id="03554-257">Instagram
</span><span class="sxs-lookup"><span data-stu-id="03554-257">Instagram</span></span>
    
- <span data-ttu-id="03554-258">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="03554-258">LinkedIn</span></span>
    
- <span data-ttu-id="03554-259">Pinterest</span><span class="sxs-lookup"><span data-stu-id="03554-259">Pinterest</span></span>
    
- <span data-ttu-id="03554-260">Twitter</span><span class="sxs-lookup"><span data-stu-id="03554-260">Twitter</span></span>
    
- <span data-ttu-id="03554-261">YouTube</span><span class="sxs-lookup"><span data-stu-id="03554-261">YouTube</span></span>
    
- <span data-ttu-id="03554-262">Vimeo</span><span class="sxs-lookup"><span data-stu-id="03554-262">Vimeo</span></span>
  
### <a name="globanet"></a><span data-ttu-id="03554-263">Globanet</span><span class="sxs-lookup"><span data-stu-id="03554-263">Globanet</span></span>

<span data-ttu-id="03554-264">[Globanet](https://www.globanet.com) prend en charge les sources de données tierces suivantes :</span><span class="sxs-lookup"><span data-stu-id="03554-264">[Globanet](https://www.globanet.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="03554-265">AOL avec client Pivot </span><span class="sxs-lookup"><span data-stu-id="03554-265">AOL with Pivot Client</span></span> 
    
- <span data-ttu-id="03554-266">BlackBerry Call Logs (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="03554-266">BlackBerry Call Logs (v5, v10, v12)</span></span>
    
- <span data-ttu-id="03554-267">BlackBerry Messenger (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="03554-267">BlackBerry Messenger (v5, v10, v12)</span></span>
    
- <span data-ttu-id="03554-268">BlackBerry PIN (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="03554-268">BlackBerry PIN (v5, v10, v12)</span></span>
    
- <span data-ttu-id="03554-269">BlackBerry SMS (version 5, version 10, version 12)</span><span class="sxs-lookup"><span data-stu-id="03554-269">BlackBerry SMS (v5, v10, v12)</span></span>
    
- <span data-ttu-id="03554-270">Bloomberg Chat
</span><span class="sxs-lookup"><span data-stu-id="03554-270">Bloomberg Chat</span></span>
    
- <span data-ttu-id="03554-271">Bloomberg Mail
</span><span class="sxs-lookup"><span data-stu-id="03554-271">Bloomberg Mail</span></span>
    
- <span data-ttu-id="03554-272">Box
</span><span class="sxs-lookup"><span data-stu-id="03554-272">Box</span></span>
    
- <span data-ttu-id="03554-273">CipherCloud for Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="03554-273">CipherCloud for Salesforce Chatter</span></span>
    
- <span data-ttu-id="03554-274">Messagerie instantanée de Cisco &amp; serveur de présence (10, v10.5.1 SU1, v11.0, v11.5 SU2)</span><span class="sxs-lookup"><span data-stu-id="03554-274">Cisco IM &amp; Presence Server (v10, v10.5.1 SU1, v11.0, v11.5 SU2)</span></span>

- <span data-ttu-id="03554-275">Cisco Webex équipes</span><span class="sxs-lookup"><span data-stu-id="03554-275">Cisco Webex Teams</span></span>

- <span data-ttu-id="03554-276">Espace de travail Citrix &amp; ShareFile</span><span class="sxs-lookup"><span data-stu-id="03554-276">Citrix Workspace &amp; ShareFile</span></span>

- <span data-ttu-id="03554-277">CrowdCompass</span><span class="sxs-lookup"><span data-stu-id="03554-277">CrowdCompass</span></span>

- <span data-ttu-id="03554-278">Fichiers texte délimités personnalisés
</span><span class="sxs-lookup"><span data-stu-id="03554-278">Custom delimited text files</span></span>
    
- <span data-ttu-id="03554-279">Fichiers XML personnalisés
</span><span class="sxs-lookup"><span data-stu-id="03554-279">Custom XML files</span></span>
    
- <span data-ttu-id="03554-280">Facebook (Pages)</span><span class="sxs-lookup"><span data-stu-id="03554-280">Facebook (Pages)</span></span>
    
- <span data-ttu-id="03554-281">Factset
</span><span class="sxs-lookup"><span data-stu-id="03554-281">Factset</span></span>
    
- <span data-ttu-id="03554-282">FXConnect</span><span class="sxs-lookup"><span data-stu-id="03554-282">FXConnect</span></span>
    
- <span data-ttu-id="03554-283">ICE Chat/YellowJacket</span><span class="sxs-lookup"><span data-stu-id="03554-283">ICE Chat/YellowJacket</span></span>
    
- <span data-ttu-id="03554-284">Jive
</span><span class="sxs-lookup"><span data-stu-id="03554-284">Jive</span></span>
    
- <span data-ttu-id="03554-285">Macgregor XIP
</span><span class="sxs-lookup"><span data-stu-id="03554-285">Macgregor XIP</span></span>

- <span data-ttu-id="03554-286">Microsoft Exchange Server</span><span class="sxs-lookup"><span data-stu-id="03554-286">Microsoft Exchange Server</span></span>
    
- <span data-ttu-id="03554-287">Microsoft OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="03554-287">Microsoft OneDrive for Business</span></span>

- <span data-ttu-id="03554-288">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="03554-288">Microsoft Teams</span></span>
       
- <span data-ttu-id="03554-289">Microsoft Yammer
</span><span class="sxs-lookup"><span data-stu-id="03554-289">Microsoft Yammer</span></span>
    
- <span data-ttu-id="03554-290">Mobile Guard</span><span class="sxs-lookup"><span data-stu-id="03554-290">Mobile Guard</span></span>
    
- <span data-ttu-id="03554-291">Pivot</span><span class="sxs-lookup"><span data-stu-id="03554-291">Pivot</span></span>
    
- <span data-ttu-id="03554-292">Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="03554-292">Salesforce Chatter</span></span>

- <span data-ttu-id="03554-293">Skype Entreprise Online</span><span class="sxs-lookup"><span data-stu-id="03554-293">Skype for Business Online</span></span>
    
- <span data-ttu-id="03554-294">Skype Entreprise, versions 2007 R2-2016 (sur site)
</span><span class="sxs-lookup"><span data-stu-id="03554-294">Skype for Business, versions 2007 R2 - 2016 (on-premises)</span></span>
    
- <span data-ttu-id="03554-295">Slack Enterprise Grid</span><span class="sxs-lookup"><span data-stu-id="03554-295">Slack Enterprise Grid</span></span>
    
- <span data-ttu-id="03554-296">Symphony
</span><span class="sxs-lookup"><span data-stu-id="03554-296">Symphony</span></span>
    
- <span data-ttu-id="03554-297">Thomson Reuters Eikon
</span><span class="sxs-lookup"><span data-stu-id="03554-297">Thomson Reuters Eikon</span></span>
    
- <span data-ttu-id="03554-298">Thomson Reuters Messenger
</span><span class="sxs-lookup"><span data-stu-id="03554-298">Thomson Reuters Messenger</span></span>
    
- <span data-ttu-id="03554-299">Thomson Reuters Dealings 3000/FX Trading
</span><span class="sxs-lookup"><span data-stu-id="03554-299">Thomson Reuters Dealings 3000 / FX Trading</span></span>
    
- <span data-ttu-id="03554-300">Twitter</span><span class="sxs-lookup"><span data-stu-id="03554-300">Twitter</span></span>
    
- <span data-ttu-id="03554-301">UBS Chat
</span><span class="sxs-lookup"><span data-stu-id="03554-301">UBS Chat</span></span>
    
- <span data-ttu-id="03554-302">YouTube</span><span class="sxs-lookup"><span data-stu-id="03554-302">YouTube</span></span>
  
### <a name="opentext"></a><span data-ttu-id="03554-303">OpenText</span><span class="sxs-lookup"><span data-stu-id="03554-303">OpenText</span></span>

<span data-ttu-id="03554-304">[OpenText](https://www.opentext.com/what-we-do/products/opentext-product-offerings-catalog/rebranded-products/daegis) prend en charge les sources de données tierces suivantes :</span><span class="sxs-lookup"><span data-stu-id="03554-304">[OpenText](https://www.opentext.com/what-we-do/products/opentext-product-offerings-catalog/rebranded-products/daegis) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="03554-305">Axs Encrypted</span><span class="sxs-lookup"><span data-stu-id="03554-305">Axs Encrypted</span></span>
    
- <span data-ttu-id="03554-306">Axs Exchange</span><span class="sxs-lookup"><span data-stu-id="03554-306">Axs Exchange</span></span>
    
- <span data-ttu-id="03554-307">Axs Local Archive</span><span class="sxs-lookup"><span data-stu-id="03554-307">Axs Local Archive</span></span>
    
- <span data-ttu-id="03554-308">Axs PlaceHolder</span><span class="sxs-lookup"><span data-stu-id="03554-308">Axs PlaceHolder</span></span>
    
- <span data-ttu-id="03554-309">Axs Signed</span><span class="sxs-lookup"><span data-stu-id="03554-309">Axs Signed</span></span>
    
- <span data-ttu-id="03554-310">Bloomberg</span><span class="sxs-lookup"><span data-stu-id="03554-310">Bloomberg</span></span>
    
- <span data-ttu-id="03554-311">Thomson Reuters</span><span class="sxs-lookup"><span data-stu-id="03554-311">Thomson Reuters</span></span>
  
### <a name="verba"></a><span data-ttu-id="03554-312">Verba</span><span class="sxs-lookup"><span data-stu-id="03554-312">Verba</span></span>

<span data-ttu-id="03554-313">[Verba](https://www.verba.com) prend en charge les sources de données tierces suivantes :</span><span class="sxs-lookup"><span data-stu-id="03554-313">[Verba](https://www.verba.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="03554-314">Avaya Aura Video
</span><span class="sxs-lookup"><span data-stu-id="03554-314">Avaya Aura Video</span></span>
    
- <span data-ttu-id="03554-315">Avaya Aura Voice
</span><span class="sxs-lookup"><span data-stu-id="03554-315">Avaya Aura Voice</span></span>
    
- <span data-ttu-id="03554-316">Avtec Radio
</span><span class="sxs-lookup"><span data-stu-id="03554-316">Avtec Radio</span></span>
    
- <span data-ttu-id="03554-317">Bosch/Telex Radio
</span><span class="sxs-lookup"><span data-stu-id="03554-317">Bosch/Telex Radio</span></span>
    
- <span data-ttu-id="03554-318">BroadSoft Video
</span><span class="sxs-lookup"><span data-stu-id="03554-318">BroadSoft Video</span></span>
    
- <span data-ttu-id="03554-319">BroadSoft Voice
</span><span class="sxs-lookup"><span data-stu-id="03554-319">BroadSoft Voice</span></span>
    
- <span data-ttu-id="03554-320">Centile Voice
</span><span class="sxs-lookup"><span data-stu-id="03554-320">Centile Voice</span></span>
    
- <span data-ttu-id="03554-321">Cisco Jabber IM
</span><span class="sxs-lookup"><span data-stu-id="03554-321">Cisco Jabber IM</span></span>
    
- <span data-ttu-id="03554-322">Cisco UC Video
</span><span class="sxs-lookup"><span data-stu-id="03554-322">Cisco UC Video</span></span>
    
- <span data-ttu-id="03554-323">Cisco UC Voice
</span><span class="sxs-lookup"><span data-stu-id="03554-323">Cisco UC Voice</span></span>
    
- <span data-ttu-id="03554-324">Cisco UCCX/UCCE vidéo</span><span class="sxs-lookup"><span data-stu-id="03554-324">Cisco UCCX/UCCE Video</span></span>
    
- <span data-ttu-id="03554-325">Cisco UCCX/UCCE vocale</span><span class="sxs-lookup"><span data-stu-id="03554-325">Cisco UCCX/UCCE Voice</span></span>
    
- <span data-ttu-id="03554-326">ESChat Radio</span><span class="sxs-lookup"><span data-stu-id="03554-326">ESChat Radio</span></span>
    
- <span data-ttu-id="03554-327">Geoman Contact Expert</span><span class="sxs-lookup"><span data-stu-id="03554-327">Geoman Contact Expert</span></span>
    
- <span data-ttu-id="03554-328">IP Trade Voice
</span><span class="sxs-lookup"><span data-stu-id="03554-328">IP Trade Voice</span></span>
    
- <span data-ttu-id="03554-329">Luware LUCS Contact Center</span><span class="sxs-lookup"><span data-stu-id="03554-329">Luware LUCS Contact Center</span></span>
    
- <span data-ttu-id="03554-330">Microsoft UC (Unified Communications)</span><span class="sxs-lookup"><span data-stu-id="03554-330">Microsoft UC (Unified Communications)</span></span>
    
- <span data-ttu-id="03554-331">Mitel MiContact Center for Lync (prairieFyre) 
</span><span class="sxs-lookup"><span data-stu-id="03554-331">Mitel MiContact Center for Lync (prairieFyre)</span></span>
    
- <span data-ttu-id="03554-332">Oracle / Acme Packet Session Border Controller Video  
</span><span class="sxs-lookup"><span data-stu-id="03554-332">Oracle / Acme Packet Session Border Controller Video</span></span>
    
- <span data-ttu-id="03554-333">Oracle / Acme Packet Session Border Controller Voice
</span><span class="sxs-lookup"><span data-stu-id="03554-333">Oracle / Acme Packet Session Border Controller Voice</span></span>
    
- <span data-ttu-id="03554-334">Singtel Mobile Voice
</span><span class="sxs-lookup"><span data-stu-id="03554-334">Singtel Mobile Voice</span></span>
    
- <span data-ttu-id="03554-335">SIPREC Video</span><span class="sxs-lookup"><span data-stu-id="03554-335">SIPREC Video</span></span>
    
-  <span data-ttu-id="03554-336">SIPREC Voice</span><span class="sxs-lookup"><span data-stu-id="03554-336">SIPREC Voice</span></span> 
    
- <span data-ttu-id="03554-337">Skype Entreprise / MI Lync
</span><span class="sxs-lookup"><span data-stu-id="03554-337">Skype for Business / Lync IM</span></span>
    
- <span data-ttu-id="03554-338">Skype Entreprise / Vidéo Lync
</span><span class="sxs-lookup"><span data-stu-id="03554-338">Skype for Business / Lync Video</span></span>
    
- <span data-ttu-id="03554-339">Skype Entreprise / Voix Lync
</span><span class="sxs-lookup"><span data-stu-id="03554-339">Skype for Business / Lync Voice</span></span>
    
- <span data-ttu-id="03554-340">Speakerbus Voice
</span><span class="sxs-lookup"><span data-stu-id="03554-340">Speakerbus Voice</span></span>
    
- <span data-ttu-id="03554-341">Standard SIP/H.323 Video 
</span><span class="sxs-lookup"><span data-stu-id="03554-341">Standard SIP/H.323 Video</span></span>
    
- <span data-ttu-id="03554-342">Standard SIP/H.323 Voice 
</span><span class="sxs-lookup"><span data-stu-id="03554-342">Standard SIP/H.323 Voice</span></span>
    
- <span data-ttu-id="03554-343">Truphone Voice
</span><span class="sxs-lookup"><span data-stu-id="03554-343">Truphone Voice</span></span>
    
- <span data-ttu-id="03554-344">TwistedPair Radio
</span><span class="sxs-lookup"><span data-stu-id="03554-344">TwistedPair Radio</span></span>
    
- <span data-ttu-id="03554-345">Écran d’ordinateur de bureau Windows 
</span><span class="sxs-lookup"><span data-stu-id="03554-345">Windows Desktop Computer Screen</span></span>
  
## <a name="step-2-create-and-configure-a-third-party-data-mailbox-in-office-365"></a><span data-ttu-id="03554-346">Étape 2 : créer et configurer une boîte aux lettres pour les données tierces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="03554-346">Step 2: Create and configure a third-party data mailbox in Office 365</span></span>

<span data-ttu-id="03554-p109">Voici les étapes pour créer et configurer une boîte aux lettres de données tiers pour l’importation de données dans Office 365. Précédente comme expliqué, les éléments sont importés à cette boîte aux lettres si le connecteur de partenaire ne peut pas mapper l’ID de l’élément à un compte d’utilisateur Office 365.</span><span class="sxs-lookup"><span data-stu-id="03554-p109">Here are the steps for creating and configuring a third-party data mailbox for importing data to Office 365. As previous explained, items are imported to this mailbox if the partner connector can't map the user ID of the item to an Office 365 user account.</span></span>
  
 <span data-ttu-id="03554-349">**Effectuer ces tâches dans le centre d’administration d’Office 365**</span><span class="sxs-lookup"><span data-stu-id="03554-349">**Complete these tasks in the Office 365 admin center**</span></span>
  
1. <span data-ttu-id="03554-p110">Créer un nouveau compte d’utilisateur dans Office 365 et l’attribuer une licence Exchange Online Plan 2 ; consultez la rubrique [Ajouter des utilisateurs à Office 365](https://go.microsoft.com/fwlink/p/?LinkId=692098). Une licence Plan 2 est requis pour placer la boîte aux lettres en conservation pour litige ou activer une boîte aux lettres d’archivage qui a un quota de stockage illimitée.</span><span class="sxs-lookup"><span data-stu-id="03554-p110">Create a new user account in Office 365 and assign it an Exchange Online Plan 2 license; see [Add users to Office 365](https://go.microsoft.com/fwlink/p/?LinkId=692098). A Plan 2 license is required to place the mailbox on Litigation Hold or enable an archive mailbox that has an unlimited storage quota.</span></span>
    
2. <span data-ttu-id="03554-352">Ajoutez le compte d’utilisateur pour la boîte aux lettres des données tierces au rôle **administrateur Exchange** admin dans Office 365 ; consultez [assigner des rôles d’administrateur dans Office 365](https://go.microsoft.com/fwlink/p/?LinkId=532393).</span><span class="sxs-lookup"><span data-stu-id="03554-352">Add the user account for the third-party data mailbox to the **Exchange administrator** admin role in Office 365; see [Assign admin roles in Office 365](https://go.microsoft.com/fwlink/p/?LinkId=532393).</span></span>
    
    > [!TIP]
    > <span data-ttu-id="03554-p111">Notez les informations d’identification pour ce compte d’utilisateur. Vous devez les fournir à votre partenaire, comme décrit à l’étape 4.</span><span class="sxs-lookup"><span data-stu-id="03554-p111">Write down the credentials for this user account. You need to provide them to your partner, as described in Step 4.</span></span> 
  
 <span data-ttu-id="03554-355">**Effectuer ces tâches dans le centre d’administration Exchange**</span><span class="sxs-lookup"><span data-stu-id="03554-355">**Complete these tasks in the Exchange admin center**</span></span>
  
1. <span data-ttu-id="03554-p112">Masquer la boîte aux lettres de données tiers à partir du carnet d’adresses et d’autres listes d’adresses dans votre organisation ; voir [Gérer les boîtes aux lettres](https://go.microsoft.com/fwlink/p/?LinkId=616058). Vous pouvez également exécuter la commande PowerShell suivante :</span><span class="sxs-lookup"><span data-stu-id="03554-p112">Hide the third-party data mailbox from the address book and other address lists in your organization; see [Manage user mailboxes](https://go.microsoft.com/fwlink/p/?LinkId=616058). Alternatively, you can run the following PowerShell command:</span></span>
    
    ```
    Set-Mailbox -Identity <identity of third-party data mailbox> -HiddenFromAddressListsEnabled $true
    ```

2. <span data-ttu-id="03554-358">Attribuer l’autorisation **FullAccess** pour la boîte aux lettres des données tierces pour que les administrateurs ou aux règlements puissent ouvrir la boîte aux lettres des données tierces dans le client de bureau Outlook ; voir [Gérer les autorisations pour les destinataires](https://go.microsoft.com/fwlink/p/?LinkId=692104).</span><span class="sxs-lookup"><span data-stu-id="03554-358">Assign the **FullAccess** permission to the third-party data mailbox so that administrators or compliance officers can open the third-party data mailbox in the Outlook desktop client; see [Manage permissions for recipients](https://go.microsoft.com/fwlink/p/?LinkId=692104).</span></span>
    
3. <span data-ttu-id="03554-359">Activer les fonctionnalités Office 365 suivantes relatives à la conformité pour la boîte aux lettres des données tierces :</span><span class="sxs-lookup"><span data-stu-id="03554-359">Enable the following compliance-related Office 365 features for the third-party data mailbox:</span></span>
    
    - <span data-ttu-id="03554-p113">Activer la boîte aux lettres d’archivage ; voir [Activer les boîtes aux lettres archive de sécurité Office 365 &amp; centre de conformité](enable-archive-mailboxes.md) et [Activer l’archivage illimité dans Office 365](enable-unlimited-archiving.md). Vous pouvez libérer de l’espace dans la boîte aux lettres principal en configurant une stratégie d’archivage qui déplace les éléments de données tierces dans la boîte aux lettres d’archive. Cela vous fournira stockage illimité pour les données de tiers.</span><span class="sxs-lookup"><span data-stu-id="03554-p113">Enable the archive mailbox; see [Enable archive mailboxes in the Office 365 Security &amp; Compliance Center](enable-archive-mailboxes.md) and [Enable unlimited archiving in Office 365](enable-unlimited-archiving.md). This will let you free-up storage space in the primary mailbox by setting up an archive policy that moves third-party data items to the archive mailbox. This will provide you with unlimited storage for third-party data.</span></span>
    
    - <span data-ttu-id="03554-p114">Placez la boîte aux lettres des données tierces litige. Vous pouvez également appliquer une stratégie de rétention Office 365 de sécurité Office 365 &amp; centre de conformité. Placer cette boîte aux lettres en attente pour conserver des éléments de données de tiers (indéfiniment ou pendant une durée spécifiée) et les empêcher d’être purgées de la boîte aux lettres. Consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="03554-p114">Place the third-party data mailbox on Litigation Hold. You can also apply an Office 365 retention policy in the Office 365 Security &amp; Compliance Center. Placing this mailbox on hold will retain third-party data items (indefinitely or for a specified duration) and prevent them from being purged from the mailbox. See one of the following topics:</span></span>
    
      - [<span data-ttu-id="03554-367">Place a mailbox on Litigation Hold</span><span class="sxs-lookup"><span data-stu-id="03554-367">Place a mailbox on Litigation Hold</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
      - [<span data-ttu-id="03554-368">Vue d'ensemble des stratégies de rétention</span><span class="sxs-lookup"><span data-stu-id="03554-368">Overview of retention policies in Office 365</span></span>](retention-policies.md)
    
       
    
    - <span data-ttu-id="03554-p115">Activer la boîte aux lettres enregistrement d’audit pour un accès propriétaire, délégué et d’administration pour la boîte aux lettres des données tierces ; consultez la rubrique [Activer la boîte aux lettres de l’audit dans Office 365](enable-mailbox-auditing.md). Cela vous permettra d’auditer toutes les activités effectuées par les utilisateurs ayant accès à la boîte aux lettres des données tierces.</span><span class="sxs-lookup"><span data-stu-id="03554-p115">Enable mailbox audit logging for owner, delegate, and admin access to the third-party data mailbox; see [Enable mailbox auditing in Office 365](enable-mailbox-auditing.md). This will allow you to audit all activity performed by any user who has access to the third-party data mailbox.</span></span>

## <a name="step-3-configure-user-mailboxes-for-third-party-data"></a><span data-ttu-id="03554-371">Étape 3 : configurer des boîtes aux lettres d’utilisateurs pour les données tierces</span><span class="sxs-lookup"><span data-stu-id="03554-371">Step 3: Configure user mailboxes for third-party data</span></span>

<span data-ttu-id="03554-p116">L’étape suivante consiste à configurer les boîtes aux lettres pour prendre en charge des données tierces. Effectuer ces tâches à l’aide du centre d’administration Exchange ou à l’aide des applets de commande Windows PowerShell correspondant.</span><span class="sxs-lookup"><span data-stu-id="03554-p116">The next step is to configure user mailboxes to support third-party data. Complete these tasks by using the Exchange admin center or by using the corresponding Windows PowerShell cmdlets.</span></span>
  
1. <span data-ttu-id="03554-374">Activer la boîte aux lettres d’archive pour chaque utilisateur ; voir [Activer les boîtes aux lettres archive de sécurité Office 365 &amp; centre de conformité](enable-archive-mailboxes.md) et [Activer l’archivage illimité dans Office 365](enable-unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="03554-374">Enable the archive mailbox for each user; see [Enable archive mailboxes in the Office 365 Security &amp; Compliance Center](enable-archive-mailboxes.md) and [Enable unlimited archiving in Office 365](enable-unlimited-archiving.md).</span></span>
    
2. <span data-ttu-id="03554-375">Placer les boîtes aux lettres en conservation pour litige ou appliquer une stratégie de rétention Office 365 ; consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="03554-375">Place user mailboxes on Litigation Hold or apply an Office 365 retention policy; see one of the following topics:</span></span> 
    
    - [<span data-ttu-id="03554-376">Place a mailbox on Litigation Hold</span><span class="sxs-lookup"><span data-stu-id="03554-376">Place a mailbox on Litigation Hold</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
    - [<span data-ttu-id="03554-377">Vue d'ensemble des stratégies de rétention</span><span class="sxs-lookup"><span data-stu-id="03554-377">Overview of retention policies in Office 365</span></span>](retention-policies.md)
    
    <span data-ttu-id="03554-378">Comme indiqué précédemment, lorsque vous placez des boîtes aux lettres en conservation, vous pouvez définir la durée de conservation des éléments de la source de données tierces ou vous pouvez choisir de les conserver indéfiniment.</span><span class="sxs-lookup"><span data-stu-id="03554-378">As previously stated, when you place mailboxes on hold, you can set a duration for how long to hold items from the third-party data source or you can choose to hold items indefinitely.</span></span>

## <a name="step-4-provide-your-partner-with-information"></a><span data-ttu-id="03554-379">Étape 4 : fournir des informations au partenaire</span><span class="sxs-lookup"><span data-stu-id="03554-379">Step 4: Provide your partner with information</span></span>

<span data-ttu-id="03554-380">La dernière étape consiste à fournir à votre partenaire les informations suivantes pour lui permettre de configurer le connecteur afin qu’il se connecte à votre organisation Office 365 pour importer les données vers les boîtes aux lettres des utilisateurs et la boîte aux lettres de données tierces.</span><span class="sxs-lookup"><span data-stu-id="03554-380">The final step is to provide your partner with the following information so they can configure the connector to connect to your Office 365 organization to import data to user mailboxes and to the third-party data mailbox.</span></span> 
  
- <span data-ttu-id="03554-381">Le point de terminaison utilisé pour se connecter au service Azure dans Office 365 :</span><span class="sxs-lookup"><span data-stu-id="03554-381">The endpoint used to connect to the Azure service in Office 365:</span></span>

    ```
    https://office365ingestionsvc.gble1.protection.outlook.com/service/ThirdPartyIngestionService.svc
    ```

- <span data-ttu-id="03554-p117">La connexion dans les informations d’identification (Office 365 ID d’utilisateur et mot de passe) de la boîte aux lettres des données tierces que vous avez créé à l’étape 2. Ces informations d’identification sont nécessaires pour que le connecteur de partenaires permettre accéder et importer des éléments à des boîtes aux lettres utilisateur et à la boîte aux lettres des données tierces.</span><span class="sxs-lookup"><span data-stu-id="03554-p117">The sign in credentials (Office 365 user ID and password) of the third-party data mailbox that you created in Step 2. These credentials are required so that the partner connector can access and import items to user mailboxes and to the third-party data mailbox.</span></span>
    

  
## <a name="more-information"></a><span data-ttu-id="03554-384">Plus d'informations</span><span class="sxs-lookup"><span data-stu-id="03554-384">More information</span></span>

- <span data-ttu-id="03554-p118">Indiqué comme précédent, les éléments à partir des données tiers sources sont importées dans les boîtes aux lettres Exchange en tant que messages électroniques. Le connecteur de partenaire importe l’élément à l’aide d’un schéma requis par l’API d’Office 365. Le tableau suivant décrit les propriétés de message d’un élément à partir d’une source de données tierce après l’importation de boîte aux lettres Exchange en tant qu’un message électronique. Le tableau indique également si la propriété message est obligatoire. Les propriétés obligatoires doivent être remplies. Si un élément ne dispose pas d’une propriété obligatoire, il ne seront pas importée vers Office 365. Le processus d’importation renverra un message d’erreur expliquant pourquoi un élément n’a pas été importé et que la propriété est manquante.</span><span class="sxs-lookup"><span data-stu-id="03554-p118">As previous explained, items from third-party data sources are imported to Exchange mailboxes as email messages. The partner connector imports the item using a schema required by the Office 365 API. The following table describes the message properties of an item from a third-party data source after it's imported to an Exchange mailbox as an email message. The table also indicates if the message property is mandatory. Mandatory properties must be populated. If an item is missing a mandatory property, it won't be imported to Office 365. The import process will return an error message explaining why an item wasn't imported and which property is missing.</span></span>
    
    |<span data-ttu-id="03554-392">**Propriété de message**</span><span class="sxs-lookup"><span data-stu-id="03554-392">**Message property**</span></span>|<span data-ttu-id="03554-393">**Obligatoire ?**</span><span class="sxs-lookup"><span data-stu-id="03554-393">**Mandatory?**</span></span>|<span data-ttu-id="03554-394">**Description**</span><span class="sxs-lookup"><span data-stu-id="03554-394">**Description**</span></span>|<span data-ttu-id="03554-395">**Exemple de valeur**</span><span class="sxs-lookup"><span data-stu-id="03554-395">**Example value**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="03554-396">**FROM**</span><span class="sxs-lookup"><span data-stu-id="03554-396">**FROM**</span></span> <br/> |<span data-ttu-id="03554-397">Oui</span><span class="sxs-lookup"><span data-stu-id="03554-397">Yes</span></span>  <br/> |<span data-ttu-id="03554-p119">L’utilisateur qui a créé à l’origine ou de l’élément envoyé dans la source de données tierce. Le connecteur de partenaire tente de mapper l’ID d’utilisateur de la source (par exemple une poignée Twitter) à un compte d’utilisateur Office 365 pour tous les participants (utilisateurs dans les champs FROM et TO). Une copie du message sera importée dans la boîte aux lettres de tous les participants. Si aucun des participants à partir de l’élément peut être mappé à un compte d’utilisateur Office 365, l’élément sera importé dans la boîte aux lettres d’archivage tiers dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="03554-p119">The user who originally created or sent the item in the third-party data source. The partner connector will attempt to map the user ID from the source item (for example a Twitter handle) to an Office 365 user account for all participants (users in the FROM and TO fields). A copy of the message will be imported to the mailbox of every participant. If none of the participants from the item can be mapped to an Office 365 user account, the item will be imported to the third-party archiving mailbox in Office 365.  </span></span><br/> <br/> <span data-ttu-id="03554-p120">Le participant qui est identifié en tant que l’expéditeur de l’élément doit avoir une boîte aux lettres active dans l’organisation Office 365 qui l’élément en cours d’importation. Si l’expéditeur ne possède une boîte aux lettres active, le message d’erreur suivant est retourné :</span><span class="sxs-lookup"><span data-stu-id="03554-p120">The participant who's identified as the sender of the item must have an active mailbox in the Office 365 organization that the item is being imported to. If the sender doesn't have an active mailbox, the following error is returned:</span></span><br/><br/>  `One or more messages in the Request failed to be delivered to either From or Sender email address. You will need to resend your entire Request. Error: The request failed. The remote server returned an error: (401) Unauthorized.`  | `bob@contoso.com` <br/> |
    |<span data-ttu-id="03554-404">**TO**</span><span class="sxs-lookup"><span data-stu-id="03554-404">**TO**</span></span> <br/> |<span data-ttu-id="03554-405">Oui</span><span class="sxs-lookup"><span data-stu-id="03554-405">Yes</span></span>  <br/> |<span data-ttu-id="03554-406">Utilisateur qui a reçu un élément, le cas échéant, pour un élément dans la source de données.</span><span class="sxs-lookup"><span data-stu-id="03554-406">The user who received an item, if applicable for an item in the data source.</span></span>  <br/> | `bob@contoso.com` <br/> |
    |<span data-ttu-id="03554-407">**SUBJECT**</span><span class="sxs-lookup"><span data-stu-id="03554-407">**SUBJECT**</span></span> <br/> |<span data-ttu-id="03554-408">Non</span><span class="sxs-lookup"><span data-stu-id="03554-408">No</span></span>  <br/> |<span data-ttu-id="03554-409">Objet de l’élément source.</span><span class="sxs-lookup"><span data-stu-id="03554-409">The subject from the source item.</span></span>  <br/> | `"Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/> |
    |<span data-ttu-id="03554-410">**DATE**</span><span class="sxs-lookup"><span data-stu-id="03554-410">**DATE**</span></span> <br/> |<span data-ttu-id="03554-411">Oui</span><span class="sxs-lookup"><span data-stu-id="03554-411">Yes</span></span>  <br/> |<span data-ttu-id="03554-412">Date à laquelle l’élément a été initialement créé ou publié dans la source de données du client, par exemple, date à laquelle un message Twitter a été publié.</span><span class="sxs-lookup"><span data-stu-id="03554-412">The date the item was originally created or posted in the customer data source; for example, that date when a Twitter message was tweeted.</span></span>  <br/> | `01 NOV 2015` <br/> |
    |<span data-ttu-id="03554-413">**BODY**</span><span class="sxs-lookup"><span data-stu-id="03554-413">**BODY**</span></span> <br/> |<span data-ttu-id="03554-414">Non</span><span class="sxs-lookup"><span data-stu-id="03554-414">No</span></span>  <br/> |<span data-ttu-id="03554-p121">Le contenu du message ou du billet. Pour des sources de données, le contenu de cette propriété peut être la même que le contenu de la propriété **SUBJECT** . Pendant le processus d’importation, le connecteur partenaire tente de mettre à jour de fidélité à partir de la source de contenu que possible. Dans la mesure du possible les fichiers, des graphiques ou tout autre contenu dans le corps de l’élément source est inclus dans cette propriété. Dans le cas contraire, le contenu de la source est inclus dans la propriété de **pièce jointe** . Le contenu de cette propriété dépendent sur le connecteur de partenaire et de la capacité de la plateforme de la source.</span><span class="sxs-lookup"><span data-stu-id="03554-p121">The contents of the message or post. For some data sources, the contents of this property could be the same as the content for the **SUBJECT** property. During the import process, the partner connector will attempt to maintain full fidelity from the content source as possible. If possible files, graphics, or other content from the body of the source item is included in this property. Otherwise, content from the source item is included in the **ATTACHMENT** property. The contents of this property will depend on the partner connector and on the capability of the source platform.  </span></span><br/> | `Author: bob@contoso.com` <br/>  `Date: 10 DEC 2014` <br/>  `Tweet: "Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/>  `Date: 01 NOV 2015` <br/> |
    |<span data-ttu-id="03554-421">**ATTACHMENT**</span><span class="sxs-lookup"><span data-stu-id="03554-421">**ATTACHMENT**</span></span> <br/> |<span data-ttu-id="03554-422">Non</span><span class="sxs-lookup"><span data-stu-id="03554-422">No</span></span>  <br/> |<span data-ttu-id="03554-p122">Si un élément dans la source de données (par exemple, un tweet Twitter ou une conversation par messagerie instantanée) contient une pièce jointe ou inclure des images, le partenaire connecté sera première tentative à inclure des pièces jointes dans la propriété **BODY** . Si ce n’est pas possible, puis elle est ajoutée à la ** pièce jointe ** propriété. D’autres exemples de pièces jointes incluent j’aime dans Facebook, les métadonnées à partir de la source de contenu et les réponses à un message ou d’un billet.</span><span class="sxs-lookup"><span data-stu-id="03554-p122">If an item in the data source (such as a tweet in Twitter or an instant messaging conversation) has an attached file or include images, the partner connect will first attempt to include attachments in the **BODY** property. If that isn't possible, then it's added to the ** ATTACHMENT ** property. Other examples of attachments include Likes in Facebook, metadata from the content source, and responses to a message or post.  </span></span><br/> | `image.gif` <br/> |
    |<span data-ttu-id="03554-426">**MESSAGECLASS**</span><span class="sxs-lookup"><span data-stu-id="03554-426">**MESSAGECLASS**</span></span> <br/> |<span data-ttu-id="03554-427">Oui</span><span class="sxs-lookup"><span data-stu-id="03554-427">Yes</span></span>  <br/> | <span data-ttu-id="03554-p123">Il s’agit d’une propriété à valeurs multiples, qui est créée et remplie par connecteur partenaire. Le format de cette propriété est `IPM.NOTE.Source.Event`. (Cette propriété doit commencer par `IPM.NOTE`; ce format est similaire à celui de la `IPM.NOTE.X` classe de message.) Cette propriété consacrée les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="03554-p123">This is a multi-value property, which is created and populated by partner connector. The format of this property is  `IPM.NOTE.Source.Event`. (This property must begin with  `IPM.NOTE`; this format is similar to the one for the  `IPM.NOTE.X` message class.) This property includes the following information:  </span></span><br/><br/><span data-ttu-id="03554-431">`Source`-Indique la source de données tierce ; par exemple, Twitter, Facebook ou BlackBerry.</span><span class="sxs-lookup"><span data-stu-id="03554-431">`Source` - Indicates the third-party data source; for example, Twitter, Facebook, or BlackBerry.</span></span>  <br/> <br/>  <span data-ttu-id="03554-p124">`Event`-Indique le type d’activité qui a été effectuée dans la source de données tierce qui a produit les éléments ; par exemple, un tweet Twitter ou une publication dans Facebook. Les événements sont spécifiques à la source de données.</span><span class="sxs-lookup"><span data-stu-id="03554-p124">`Event` - Indicates the type of activity that was performed in the third-party data source that produced the items; for example, a tweet in Twitter or a post in Facebook. Events are specific to the data source.  </span></span><br/> <br/>  <span data-ttu-id="03554-p125">Un des objectifs de cette propriété sont de filtrer des éléments spécifiques en fonction de la source de données où un élément à l’origine ou en fonction du type d’événement. Par exemple, dans une recherche de découverte, vous pouvez créer une requête de recherche pour trouver tous les tweet qui ont été validées par un utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="03554-p125">One purpose of this property is to filter specific items based on the data source where an item originated or based on the type of event. For example, in an eDiscovery search you could create a search query to find all the tweets that were posted by a specific user.  </span></span><br/> | `IPM.NOTE.Twitter.Tweet` <br/> |
   
- <span data-ttu-id="03554-p126">Lorsque les éléments sont importés correctement aux boîtes aux lettres dans Office 365, un identificateur unique est renvoyé à l’appelant dans le cadre de la réponse HTTP. Cet identificateur — appelé `x-IngestionCorrelationID`— peut être utilisé à des fins de résolution des problèmes suivants par les partenaires pour le suivi de bout en bout d’éléments. Il est recommandé de partenaires capturent ces informations et ouvrez une session en conséquence à leur fin. Voici un exemple d’une réponse HTTP avec cet identificateur :</span><span class="sxs-lookup"><span data-stu-id="03554-p126">When items are successfully imported to mailboxes in Office 365, a unique identifier is returned back to the caller as part of the HTTP response. This identifier—called  `x-IngestionCorrelationID`—can be used for subsequent troubleshooting purposes by partners for end-to-end tracking of items. It's recommended that partners capture this information and log it accordingly at their end. Here's an example of an HTTP response showing this identifier:</span></span>

    ```
    HTTP/1.1 200 OK
    Content-Type: text/xml; charset=utf-8
    Server: Microsoft-IIS/8.5
    x-IngestionCorrelationID: 1ec7667d-f097-47fe-a9a2-bc7ab0a7552b
    X-AspNet-Version: 4.0.30319
    X-Powered-By: ASP.NET
    Date: Tue, 02 Feb 2016 22:55:33 GMT 
    ```
 
- <span data-ttu-id="03554-p127">Vous pouvez utiliser l’outil de recherche de contenu de sécurité Office 365 &amp; centre de conformité pour rechercher des éléments qui ont été importés pour les boîtes aux lettres dans Office 365 à partir d’une source de données tierce. Pour rechercher spécifiquement ces éléments importés, vous pouvez utiliser les paires de valeur de la propriété message suivantes dans la zone mots clés pour une recherche de contenu. .</span><span class="sxs-lookup"><span data-stu-id="03554-p127">You can use the Content Search tool in the Office 365 Security &amp; Compliance Center to search for items that were imported to mailboxes in Office 365 from a third-party data source. To search specifically for these imported items, you can use the following message property-value pairs in the keyword box for a Content Search. .</span></span> 
    
  - <span data-ttu-id="03554-p128">**`kind:externaldata`**-Utilisez cette paire de valeur de la propriété pour rechercher tous les types de données de tiers. Par exemple, pour rechercher des éléments qui ont été importés à partir d’une source de données tierce et contenu dans le mot « contoso » dans la propriété Subject de l’élément importé, vous utiliseriez la requête de mot clé `kind:externaldata AND subject:contoso`.</span><span class="sxs-lookup"><span data-stu-id="03554-p128">**`kind:externaldata`** - Use this property-value pair to search all third-party data types. For example, to search for items that were imported from a third-party data source and contained the word "contoso" in the Subject property of the imported item, you would use the keyword query  `kind:externaldata AND subject:contoso`.</span></span>
    
  - <span data-ttu-id="03554-p129">**`itemclass:ipm.externaldata.<third-party data type>`**-Utilisez cette paire de valeur de la propriété pour rechercher un type de spécifier des données tiers uniquement. Par exemple, pour rechercher uniquement les données Facebook qui contient le mot « contoso » dans la propriété Subject, utiliser la requête de mot clé `itemclass:ipm.externaldata.Facebook* AND subject:contoso`.</span><span class="sxs-lookup"><span data-stu-id="03554-p129">**`itemclass:ipm.externaldata.<third-party data type>`** - Use this property-value pair to only search a specify type of third-party data. For example, to only search Facebook data that contains the word "contoso" in the Subject property, you would use the keyword query  `itemclass:ipm.externaldata.Facebook* AND subject:contoso`.</span></span> 

  <span data-ttu-id="03554-447">Pour obtenir la liste complète des valeurs à utiliser pour les types de données de tiers pour la `itemclass` propriété, voir [Recherche de contenu utiliser pour rechercher des données tierces qui a été importées dans Office 365](use-content-search-to-search-third-party-data-that-was-imported.md)</span><span class="sxs-lookup"><span data-stu-id="03554-447">For a complete list of values to use for third-party data types for the  `itemclass` property, see [Use Content Search to search third-party data that was imported to Office 365](use-content-search-to-search-third-party-data-that-was-imported.md)</span></span>
    
   <span data-ttu-id="03554-448">Pour plus d’informations sur l’utilisation de la recherche de contenu et la création de requêtes de recherche de mots clés, voir :</span><span class="sxs-lookup"><span data-stu-id="03554-448">For more information about using Content Search and creating keyword search queries, see:</span></span>
    
  - [<span data-ttu-id="03554-449">Recherche de contenu dans Office 365</span><span class="sxs-lookup"><span data-stu-id="03554-449">Content Search in Office 365</span></span>](content-search.md)
    
  - [<span data-ttu-id="03554-450">Requêtes par mots clés et conditions de recherche pour la recherche de contenu</span><span class="sxs-lookup"><span data-stu-id="03554-450">Keyword queries and search conditions for Content Search</span></span>](keyword-queries-and-search-conditions.md)
 
