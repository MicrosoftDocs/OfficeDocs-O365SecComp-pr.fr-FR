---
title: Recherche de contenu permet de rechercher des données tiers qui a été importées dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/27/2017
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: ec2677ff-c4d7-4363-a9e7-22c80e015688
description: Utiliser l’outil de découverte électronique de recherche de contenu pour rechercher des éléments qui ont été importés pour les boîtes aux lettres dans Office 365 à partir d’une source de données tierce. Vous pouvez créer une requête pour rechercher tous les éléments importés ou pour créer une requête pour rechercher des types de données tiers spécifiques. Cet article répertorie les valeurs que vous pouvez utiliser dans une requête de mot clé pour rechercher les types de données de tiers qui peuvent être importés dans Office 365.
ms.openlocfilehash: 90d9dc52dcd9dba9bc273dfcf1c5f22e3913d6ba
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528350"
---
# <a name="use-content-search-to-search-third-party-data-that-was-imported-to-office-365"></a><span data-ttu-id="2c1e9-105">Recherche de contenu permet de rechercher des données tiers qui a été importées dans Office 365</span><span class="sxs-lookup"><span data-stu-id="2c1e9-105">Use Content Search to search third-party data that was imported to Office 365</span></span>

<span data-ttu-id="2c1e9-p102">Vous pouvez utiliser l' [outil de découverte électronique de recherche de contenu](content-search.md) de sécurité Office 365 &amp; centre de conformité pour rechercher des éléments qui ont été importés pour les boîtes aux lettres dans Office 365 à partir d’une source de données tierce. Vous pouvez créer une requête pour rechercher importé tous les éléments de données de tiers ou vous pouvez créer une requête de recherche uniquement les éléments de données tiers spécifiques. En outre, vous pouvez également créer une stratégie de conservation basée sur une requête ou une découverte basée sur une requête attente permettant de conserver des données tierces dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="2c1e9-p102">You can use the [Content Search eDiscovery tool](content-search.md) in the Office 365 Security &amp; Compliance Center to search for items that were imported to mailboxes in Office 365 from a third-party data source. You can create a query to search all imported third-party data items or you can create a query to only search specific third-party data items. Additionally, you can also create a query-based Preservation Policy or a query-based eDiscovery hold to preserve third-party data in Office 365.</span></span> 
  
<span data-ttu-id="2c1e9-109">Pour plus d’informations sur l’importation des données tierces et une liste des types de données de tiers qui peuvent être importés dans Office 365, voir [l’archivage des données tierces dans Office 365](archiving-third-party-data.md).</span><span class="sxs-lookup"><span data-stu-id="2c1e9-109">For more information about importing third-party data and a list of the third-party data types that can be imported to Office 365, see [Archiving third-party data in Office 365](archiving-third-party-data.md).</span></span> 
  
## <a name="creating-a-query-to-search-all-third-party-data"></a><span data-ttu-id="2c1e9-110">Création d’une requête pour rechercher toutes les données de tiers</span><span class="sxs-lookup"><span data-stu-id="2c1e9-110">Creating a query to search all third-party data</span></span>

<span data-ttu-id="2c1e9-p103">Recherche (ou mise en attente) n’importe quel type de données de tiers que vous avez importés vers Office 365, vous pouvez vous permet de la `kind:externaldata` paire de messages valeur de la propriété dans la zone mots clés pour une recherche de contenu ou lors de la création d’une suspension basée sur une requête. Par exemple, pour rechercher des éléments qui ont été importés à partir d’une source de données tierce et contiennent le mot « contoso » dans la propriété Subject de l’élément importé, vous utiliseriez la requête suivante :</span><span class="sxs-lookup"><span data-stu-id="2c1e9-p103">To search (or place on hold) any type of third-party data that you've imported to Office 365, you can you can use the  `kind:externaldata` message property-value pair in the keyword box for a Content Search or when creating a query-based hold. For example, to search for items that were imported from any third-party data source and contain the word "contoso" in the Subject property of the imported item, you would use the following query:</span></span> 
  
```
kind:externaldata AND subject:contoso
```

<span data-ttu-id="2c1e9-p104">L’exemple de requête de mot clé précédent inclut la propriété subject. Pour obtenir la liste des autres propriétés d’éléments de données tiers peuvent inclus dans une requête de mot clé, voir la section « Plus d’informations » dans [l’archivage des données tierces dans Office 365](archiving-third-party-data.md#more-information).</span><span class="sxs-lookup"><span data-stu-id="2c1e9-p104">The previous keyword query example includes the subject property. For a list of other properties for third-party data items that can included in a keyword query, see the "More information" section in [Archiving third-party data in Office 365](archiving-third-party-data.md#more-information).</span></span>
  
<span data-ttu-id="2c1e9-p105">Lorsque vous créez des requêtes pour rechercher et bloquer les données tiers, vous pouvez également utiliser des conditions pour affiner les résultats de recherche. Pour plus d’informations sur la création de requêtes de recherche de contenu, voir [conditions de recherche pour la recherche de contenu et les requêtes de mot clé](keyword-queries-and-search-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="2c1e9-p105">When creating queries to search and hold third-party data, you can also use conditions to narrow the search results. For more information about creating Content Search queries, see [Keyword queries and search conditions for Content Search](keyword-queries-and-search-conditions.md).</span></span>
  
## <a name="creating-a-query-to-search-specific-types-of-third-party-data"></a><span data-ttu-id="2c1e9-117">Création d’une requête pour rechercher des types spécifiques de données de tiers</span><span class="sxs-lookup"><span data-stu-id="2c1e9-117">Creating a query to search specific types of third-party data</span></span>

<span data-ttu-id="2c1e9-118">Au lieu de la recherche dans tous les types de données tiers, vous pouvez créer de requêtes que seule la recherche pour un type de spécifier des données tiers à l’aide de la paire de valeur de la propriété message suivante dans la zone mots clés pour une recherche de contenu :</span><span class="sxs-lookup"><span data-stu-id="2c1e9-118">Instead of searching all types of third-party data, you can create queries that only search for a specify type of third-party data by using the following message property-value pair in the keyword box for a Content Search:</span></span>
  
```
itemclass:ipm.externaldata.<third-party data type>* 
```

<span data-ttu-id="2c1e9-119">Par exemple, pour rechercher uniquement les données Facebook qui contient le mot « contoso » dans la propriété Subject, vous utiliseriez la requête suivante :</span><span class="sxs-lookup"><span data-stu-id="2c1e9-119">For example, to only search Facebook data that contains the word "contoso" in the Subject property, you would use the following query:</span></span>
  
```
itemclass:ipm.externaldata.Facebook* AND subject:contoso
```

<span data-ttu-id="2c1e9-p106">Le tableau suivant répertorie les types de données de tiers que vous pouvez rechercher et la valeur à utiliser pour le `itemclass:` message, propriété au service de recherche spécifiquement pour ce type de données de tiers. Notez que la syntaxe de requête n’est pas respectant la casse.</span><span class="sxs-lookup"><span data-stu-id="2c1e9-p106">The following table lists the third-party data types that you can search, and the value to use for the  `itemclass:` message property to specifically search for that type of third-party data. Note that the query syntax isn't case sensitive.</span></span> 
  
|<span data-ttu-id="2c1e9-122">**Type de données de tiers**</span><span class="sxs-lookup"><span data-stu-id="2c1e9-122">**Third-party data type**</span></span>|<span data-ttu-id="2c1e9-123">**Valeur `itemclass:` propriété**</span><span class="sxs-lookup"><span data-stu-id="2c1e9-123">**Value for  `itemclass:` property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2c1e9-124">AIM</span><span class="sxs-lookup"><span data-stu-id="2c1e9-124">AIM</span></span>  <br/> | `ipm.externaldata.AIM*` <br/> |
|<span data-ttu-id="2c1e9-125">American Idol</span><span class="sxs-lookup"><span data-stu-id="2c1e9-125">American Idol</span></span>  <br/> | `ipm.externaldata.AmericanIdol*` <br/> |
|<span data-ttu-id="2c1e9-126">AOL avec client Pivot </span><span class="sxs-lookup"><span data-stu-id="2c1e9-126">AOL with Pivot Client</span></span>  <br/> | `ipm.externaldata.Pivot.IM` <br/> |
|<span data-ttu-id="2c1e9-127">Apple Juice</span><span class="sxs-lookup"><span data-stu-id="2c1e9-127">Apple Juice</span></span>  <br/> | `ipm.externaldata.AppleJuice*` <br/> |
|<span data-ttu-id="2c1e9-128">Ares</span><span class="sxs-lookup"><span data-stu-id="2c1e9-128">Ares</span></span>  <br/> | `ipm.externaldata.Ares*` <br/> |
|<span data-ttu-id="2c1e9-129">Axs Encrypted</span><span class="sxs-lookup"><span data-stu-id="2c1e9-129">Axs Encrypted</span></span>  <br/> | `ipm.externaldata.AxsEncrypted*` <br/> |
|<span data-ttu-id="2c1e9-130">Axs Exchange</span><span class="sxs-lookup"><span data-stu-id="2c1e9-130">Axs Exchange</span></span>  <br/> | `ipm.externaldata.AxsExchange*` <br/> |
|<span data-ttu-id="2c1e9-131">Axs Local Archive</span><span class="sxs-lookup"><span data-stu-id="2c1e9-131">Axs Local Archive</span></span>  <br/> | `ipm.externaldata.AxsLocalArchive*` <br/> |
|<span data-ttu-id="2c1e9-132">Espace réservé AX</span><span class="sxs-lookup"><span data-stu-id="2c1e9-132">Axs Placeholder</span></span>  <br/> | `ipm.externaldata.AxsPlaceHolder*` <br/> |
|<span data-ttu-id="2c1e9-133">Axs Signed</span><span class="sxs-lookup"><span data-stu-id="2c1e9-133">Axs Signed</span></span>  <br/> | `ipm.externaldata.AxsSigned*` <br/> |
|<span data-ttu-id="2c1e9-134">Bazaarvoice</span><span class="sxs-lookup"><span data-stu-id="2c1e9-134">Bazaarvoice</span></span>  <br/> | `ipm.externaldata.Bazaarvoice*` <br/> |
|<span data-ttu-id="2c1e9-135">BearShare</span><span class="sxs-lookup"><span data-stu-id="2c1e9-135">Bearshare</span></span>  <br/> | `ipm.externaldata.Bearshare*` <br/> |
|<span data-ttu-id="2c1e9-136">BitTorrent</span><span class="sxs-lookup"><span data-stu-id="2c1e9-136">BitTorrent</span></span>  <br/> | `ipm.externaldata.BitTorrent*` <br/> |
|<span data-ttu-id="2c1e9-137">BlackBerry</span><span class="sxs-lookup"><span data-stu-id="2c1e9-137">Blackberry</span></span>  <br/> | `ipm.externaldata.Blackberry*` <br/> |
|<span data-ttu-id="2c1e9-138">Journaux d’appels blackBerry</span><span class="sxs-lookup"><span data-stu-id="2c1e9-138">BlackBerry Call Logs</span></span>  <br/> | `ipm.externaldata.BlackBerryCall*` <br/> |
|<span data-ttu-id="2c1e9-139">Messenger blackBerry</span><span class="sxs-lookup"><span data-stu-id="2c1e9-139">BlackBerry Messenger</span></span>  <br/> | `ipm.externaldata.BlackBerryMessenger*` <br/> |
|<span data-ttu-id="2c1e9-140">BlackBerry code confidentiel</span><span class="sxs-lookup"><span data-stu-id="2c1e9-140">BlackBerry PIN</span></span>  <br/> | `ipm.externaldata.BlackBerryPIN*` <br/> |
|<span data-ttu-id="2c1e9-141">BlackBerry SMS</span><span class="sxs-lookup"><span data-stu-id="2c1e9-141">BlackBerry SMS</span></span>  <br/> | `ipm.externaldata.BlackBerrySMS*` <br/> |
|<span data-ttu-id="2c1e9-142">Bloomberg</span><span class="sxs-lookup"><span data-stu-id="2c1e9-142">Bloomberg</span></span>  <br/> | `ipm.externaldata.Bloomberg*` <br/> |
|<span data-ttu-id="2c1e9-143">Bloomberg Mail
</span><span class="sxs-lookup"><span data-stu-id="2c1e9-143">Bloomberg Mail</span></span>  <br/> | `ipm.externaldata.BloombergMail*` <br/> |
|<span data-ttu-id="2c1e9-144">Messagerie Bloomberg</span><span class="sxs-lookup"><span data-stu-id="2c1e9-144">Bloomberg Messaging</span></span>  <br/> | `ipm.externaldata.BloombergMessaging*` <br/> |
|<span data-ttu-id="2c1e9-145">Box
</span><span class="sxs-lookup"><span data-stu-id="2c1e9-145">Box</span></span>  <br/> | `ipm.externaldata.Box*` <br/> |
|<span data-ttu-id="2c1e9-146">Messagerie instantanée de Cisco &amp; serveur de présence</span><span class="sxs-lookup"><span data-stu-id="2c1e9-146">Cisco IM &amp; Presence Server</span></span>  <br/> | `ipm.externaldata.Jabber.IM` <br/> |
|<span data-ttu-id="2c1e9-147">Cisco Jabber</span><span class="sxs-lookup"><span data-stu-id="2c1e9-147">Cisco Jabber</span></span>  <br/> | `ipm.externaldata.Jabber*` <br/> |
|<span data-ttu-id="2c1e9-148">CipherCloud for Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="2c1e9-148">CipherCloud for Salesforce Chatter</span></span>  <br/> | `ipm.externaldata.Chatter.Post` <br/>  `ipm.externaldata.Chatter.Comment` <br/> |
|<span data-ttu-id="2c1e9-149">Direct Connect</span><span class="sxs-lookup"><span data-stu-id="2c1e9-149">Direct Connect</span></span>  <br/> | `ipm.externaldata.DirectConnect*` <br/> |
|<span data-ttu-id="2c1e9-150">Facebook</span><span class="sxs-lookup"><span data-stu-id="2c1e9-150">Facebook</span></span>  <br/> | `ipm.externaldata.Facebook*` <br/> |
|<span data-ttu-id="2c1e9-151">FastTrack</span><span class="sxs-lookup"><span data-stu-id="2c1e9-151">FastTrack</span></span>  <br/> | `ipm.externaldata.FastTrack*` <br/> |
|<span data-ttu-id="2c1e9-152">FXConnect</span><span class="sxs-lookup"><span data-stu-id="2c1e9-152">FXConnect</span></span>  <br/> | `ipm.externaldata.FXConnect.chat` <br/> |
|<span data-ttu-id="2c1e9-153">Flickr
</span><span class="sxs-lookup"><span data-stu-id="2c1e9-153">Flickr</span></span>  <br/> | `ipm.externaldata.Flickr*` <br/> |
|<span data-ttu-id="2c1e9-154">Gnutella</span><span class="sxs-lookup"><span data-stu-id="2c1e9-154">Gnutella</span></span>  <br/> | `ipm.externaldata.Gnutella*` <br/> |
|<span data-ttu-id="2c1e9-155">Google+
</span><span class="sxs-lookup"><span data-stu-id="2c1e9-155">Google+</span></span>  <br/> | `ipm.externaldata.GooglePlus*` <br/> |
|<span data-ttu-id="2c1e9-156">Google Talk</span><span class="sxs-lookup"><span data-stu-id="2c1e9-156">Google Talk</span></span>  <br/> | `ipm.externaldata.GoogleTalk*` <br/> |
|<span data-ttu-id="2c1e9-157">GoToMyPC</span><span class="sxs-lookup"><span data-stu-id="2c1e9-157">GoToMyPC</span></span>  <br/> | `ipm.externaldata.GoToMyPC*` <br/> |
|<span data-ttu-id="2c1e9-158">HipChat</span><span class="sxs-lookup"><span data-stu-id="2c1e9-158">HipChat</span></span>  <br/> | `ipm.externaldata.HipChat*` <br/> |
|<span data-ttu-id="2c1e9-159">Hopster</span><span class="sxs-lookup"><span data-stu-id="2c1e9-159">Hopster</span></span>  <br/> | `ipm.externaldata.Hopster*` <br/> |
|<span data-ttu-id="2c1e9-160">HubConnex</span><span class="sxs-lookup"><span data-stu-id="2c1e9-160">HubConnex</span></span>  <br/> | `ipm.externaldata.HubConnex*` <br/> |
|<span data-ttu-id="2c1e9-161">Connexions IBM</span><span class="sxs-lookup"><span data-stu-id="2c1e9-161">IBM Connections</span></span>  <br/> | `ipm.externaldata.Connections*` <br/> |
|<span data-ttu-id="2c1e9-162">IBM SameTime</span><span class="sxs-lookup"><span data-stu-id="2c1e9-162">IBM SameTime</span></span>  <br/> | `ipm.externaldata.Sametime*` <br/> |
|<span data-ttu-id="2c1e9-163">Conversation ICE</span><span class="sxs-lookup"><span data-stu-id="2c1e9-163">ICE Chat</span></span>  <br/> | `ipm.externaldata.ICEChat.Chat` <br/> |
|<span data-ttu-id="2c1e9-164">Indii Messenger
</span><span class="sxs-lookup"><span data-stu-id="2c1e9-164">Indii Messenger</span></span>  <br/> | `ipm.externaldata.Indii*` <br/> |
|<span data-ttu-id="2c1e9-165">Instagram
</span><span class="sxs-lookup"><span data-stu-id="2c1e9-165">Instagram</span></span>  <br/> | `ipm.externaldata.Instagram*` <br/> |
|<span data-ttu-id="2c1e9-166">Instant Bloomberg
</span><span class="sxs-lookup"><span data-stu-id="2c1e9-166">Instant Bloomberg</span></span>  <br/> | `ipm.externaldata.InstantBloomberg*` <br/> |
|<span data-ttu-id="2c1e9-167">InvestEdge</span><span class="sxs-lookup"><span data-stu-id="2c1e9-167">InvestEdge</span></span>  <br/> | `ipm.externaldata.InvestEdge*` <br/> |
|<span data-ttu-id="2c1e9-168">IRC</span><span class="sxs-lookup"><span data-stu-id="2c1e9-168">IRC</span></span>  <br/> | `ipm.externaldata.IRC*` <br/> |
|<span data-ttu-id="2c1e9-169">Jive
</span><span class="sxs-lookup"><span data-stu-id="2c1e9-169">Jive</span></span>  <br/> | `ipm.externaldata.Jive*` <br/> |
|<span data-ttu-id="2c1e9-170">JiveApiRetention</span><span class="sxs-lookup"><span data-stu-id="2c1e9-170">JiveApiRetention</span></span>  <br/> | `ipm.externaldata.JiveApiRetention*` <br/> |
|<span data-ttu-id="2c1e9-171">JXTA</span><span class="sxs-lookup"><span data-stu-id="2c1e9-171">JXTA</span></span>  <br/> | `ipm.externaldata.JXTA*` <br/> |
|<span data-ttu-id="2c1e9-172">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="2c1e9-172">LinkedIn</span></span>  <br/> | `ipm.externaldata.LinkedIn*` <br/> |
|<span data-ttu-id="2c1e9-173">MFTP</span><span class="sxs-lookup"><span data-stu-id="2c1e9-173">MFTP</span></span>  <br/> | `ipm.externaldata.MFTP*` <br/> |
|<span data-ttu-id="2c1e9-174">Communications unifiées de Microsoft</span><span class="sxs-lookup"><span data-stu-id="2c1e9-174">Microsoft UC</span></span>  <br/> | `ipm.externaldata.MicrosoftUC*` <br/> |
|<span data-ttu-id="2c1e9-175">Aligner l’esprit</span><span class="sxs-lookup"><span data-stu-id="2c1e9-175">Mind Align</span></span>  <br/> | `ipm.externaldata.MindAlign*` <br/> |
|<span data-ttu-id="2c1e9-176">Mobile Guard</span><span class="sxs-lookup"><span data-stu-id="2c1e9-176">Mobile Guard</span></span>  <br/> | `ipm.externaldata.MobileGuard*` <br/> |
|<span data-ttu-id="2c1e9-177">MSN</span><span class="sxs-lookup"><span data-stu-id="2c1e9-177">MSN</span></span>  <br/> | `ipm.externaldata.MSN*` <br/> |
|<span data-ttu-id="2c1e9-178">MySpace</span><span class="sxs-lookup"><span data-stu-id="2c1e9-178">MySpace</span></span>  <br/> | `ipm.externaldata.MySpace*` <br/> |
|<span data-ttu-id="2c1e9-179">NEONetwork</span><span class="sxs-lookup"><span data-stu-id="2c1e9-179">NEONetwork</span></span>  <br/> | `ipm.externaldata.NEONetwork*` <br/> |
|<span data-ttu-id="2c1e9-180">OpenNap</span><span class="sxs-lookup"><span data-stu-id="2c1e9-180">OpenNap</span></span>  <br/> | `ipm.externaldata.OpenNap*` <br/> |
|<span data-ttu-id="2c1e9-181">Pinterest</span><span class="sxs-lookup"><span data-stu-id="2c1e9-181">Pinterest</span></span>  <br/> | `ipm.externaldata.Pinterest*` <br/> |
|<span data-ttu-id="2c1e9-182">Pivot</span><span class="sxs-lookup"><span data-stu-id="2c1e9-182">Pivot</span></span>  <br/> | `ipm.externaldata.Pivot*` <br/> |
|<span data-ttu-id="2c1e9-183">QQ</span><span class="sxs-lookup"><span data-stu-id="2c1e9-183">QQ</span></span>  <br/> | `ipm.externaldata.QQ*` <br/> |
|<span data-ttu-id="2c1e9-184">Microsoft SharePoint</span><span class="sxs-lookup"><span data-stu-id="2c1e9-184">Microsoft SharePoint</span></span>  <br/> | `ipm.externaldata.SharePoint*` <br/> |
|<span data-ttu-id="2c1e9-185">Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="2c1e9-185">Salesforce Chatter</span></span>  <br/> | `ipm.externaldata.Chatter*` <br/> |
|<span data-ttu-id="2c1e9-186">Skype Entreprise</span><span class="sxs-lookup"><span data-stu-id="2c1e9-186">Skype for Business</span></span>  <br/> | `ipm.externaldata.Skype*` <br/> |
|<span data-ttu-id="2c1e9-187">Slack Enterprise Grid</span><span class="sxs-lookup"><span data-stu-id="2c1e9-187">Slack Enterprise Grid</span></span>  <br/> | `ipm.externaldata.Slack.IM` <br/> |
|<span data-ttu-id="2c1e9-188">SoftEther</span><span class="sxs-lookup"><span data-stu-id="2c1e9-188">SoftEther</span></span>  <br/> | `ipm.externaldata.SoftEther*` <br/> |
|<span data-ttu-id="2c1e9-189">
Squawker
</span><span class="sxs-lookup"><span data-stu-id="2c1e9-189">Squawker</span></span>  <br/> | `ipm.externaldata.Squawker*` <br/> |
|<span data-ttu-id="2c1e9-190">Symphony
</span><span class="sxs-lookup"><span data-stu-id="2c1e9-190">Symphony</span></span>  <br/> | `ipm.externaldata.Symphony*` <br/> |
|<span data-ttu-id="2c1e9-191">Thomson Reuters</span><span class="sxs-lookup"><span data-stu-id="2c1e9-191">Thomson Reuters</span></span>  <br/> | `ipm.externaldata.Reuters*` <br/> |
| <span data-ttu-id="2c1e9-192">Thomson Reuters Eikon Messenger
</span><span class="sxs-lookup"><span data-stu-id="2c1e9-192">Thomson Reuters Eikon Messenger</span></span>  <br/> | `ipm.externaldata.ReutersEikon*` <br/> |
|<span data-ttu-id="2c1e9-193">Tor</span><span class="sxs-lookup"><span data-stu-id="2c1e9-193">Tor</span></span>  <br/> | `ipm.externaldata.Tor*` <br/> |
|<span data-ttu-id="2c1e9-194">TTT</span><span class="sxs-lookup"><span data-stu-id="2c1e9-194">TTT</span></span>  <br/> | `ipm.externaldata.TTT*` <br/> |
|<span data-ttu-id="2c1e9-195">Twitter</span><span class="sxs-lookup"><span data-stu-id="2c1e9-195">Twitter</span></span>  <br/> | `ipm.externaldata.Twitter*` <br/> |
|<span data-ttu-id="2c1e9-196">UBS Chat
</span><span class="sxs-lookup"><span data-stu-id="2c1e9-196">UBS Chat</span></span>  <br/> | `ipm.externaldata.UBS*` <br/> |
|<span data-ttu-id="2c1e9-197">Vimeo</span><span class="sxs-lookup"><span data-stu-id="2c1e9-197">Vimeo</span></span>  <br/> | `ipm.externaldata.Vimeo*` <br/> |
|<span data-ttu-id="2c1e9-198">WinMX</span><span class="sxs-lookup"><span data-stu-id="2c1e9-198">WinMX</span></span>  <br/> | `ipm.externaldata.WinMX*` <br/> |
|<span data-ttu-id="2c1e9-199">Winny</span><span class="sxs-lookup"><span data-stu-id="2c1e9-199">Winny</span></span>  <br/> | `ipm.externaldata.Winny*` <br/> |
|<span data-ttu-id="2c1e9-200">Yahoo!</span><span class="sxs-lookup"><span data-stu-id="2c1e9-200">Yahoo!</span></span>  <br/> | `ipm.externaldata.Yahoo!*` <br/> |
|<span data-ttu-id="2c1e9-201">Yammer</span><span class="sxs-lookup"><span data-stu-id="2c1e9-201">Yammer</span></span>  <br/> | `ipm.externaldata.Yammer*` <br/> |
|<span data-ttu-id="2c1e9-202">YellowJacket</span><span class="sxs-lookup"><span data-stu-id="2c1e9-202">YellowJacket</span></span>  <br/> | `ipm.externaldata.YellowJacket*` <br/> |
|<span data-ttu-id="2c1e9-203">YouTube</span><span class="sxs-lookup"><span data-stu-id="2c1e9-203">YouTube</span></span>  <br/> | `ipm.externaldata.YouTube*` <br/> |
