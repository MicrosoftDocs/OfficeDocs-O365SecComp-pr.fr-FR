---
title: Chiffrement Office 365 pour les données en Transit
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 'Résumé : Brièvement comment Microsoft chiffre les données en transit.'
ms.openlocfilehash: 8f4781cf1127fb1b6bf742c267c76e3df39b8209
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527556"
---
# <a name="office-365-encryption-for-data-in-transit"></a><span data-ttu-id="78667-103">Chiffrement Office 365 pour les données en transit</span><span class="sxs-lookup"><span data-stu-id="78667-103">Office 365 encryption for data in transit</span></span>

<span data-ttu-id="78667-104">En plus de la protection des données au repos du client, Microsoft utilise des technologies de chiffrement pour protéger les données du client Office 365 en transit.</span><span class="sxs-lookup"><span data-stu-id="78667-104">In addition to protecting customer data at rest, Microsoft uses encryption technologies to protect Office 365 customer data in transit.</span></span> 

<span data-ttu-id="78667-105">Les données sont en transit :</span><span class="sxs-lookup"><span data-stu-id="78667-105">Data is in transit:</span></span>
- <span data-ttu-id="78667-106">Lorsqu’un ordinateur client communique avec un serveur d’Office 365 ;</span><span class="sxs-lookup"><span data-stu-id="78667-106">when a client machine communicates with an Office 365 server;</span></span>
- <span data-ttu-id="78667-107">Lorsqu’un serveur Office 365 communique avec un autre serveur d’Office 365 ; et</span><span class="sxs-lookup"><span data-stu-id="78667-107">when an Office 365 server communicates with another Office 365 server; and</span></span>
- <span data-ttu-id="78667-108">Lorsqu’un serveur Office 365 communique avec un serveur d’Office 365 (par exemple, Exchange Online en courrier électronique à un serveur de messagerie externe).</span><span class="sxs-lookup"><span data-stu-id="78667-108">when an Office 365 server communicates with a non-Office 365 server (e.g., Exchange Online delivering email to a foreign email server).</span></span>

<span data-ttu-id="78667-p101">Communications inter-centre de données entre les serveurs Office 365 a lieu sur TLS ou IPsec, et tous les serveurs présentés au client négocient une session sécurisée avec les ordinateurs clients utilisant le protocole TLS (par exemple, Exchange Online utilise TLS 1.2 avec 256 bits est utilisée (FIPS 140-2 niveau validé par 2). (Voir [plus d’informations techniques de référence sur le chiffrement dans Office 365](https://support.office.com/article/Technical-reference-details-about-encryption-in-Office-365-862CBE93-4268-4EF9-BA79-277545ECF221) pour obtenir la liste des suites de chiffrement TLS pris en charge par Office 365). Cela s’applique aux protocoles utilisés par les clients tels qu’Outlook, Skype pour les entreprises et Outlook sur le site web (par exemple, HTTP, POP3, etc.).</span><span class="sxs-lookup"><span data-stu-id="78667-p101">Inter-datacenter communications between Office 365 servers takes place over TLS or IPsec, and all customer-facing servers negotiate a secure session using TLS with client machines (e.g., Exchange Online uses TLS 1.2 with 256-bit cipher strength is used (FIPS 140-2 Level 2-validated). (See [Technical reference details about encryption in Office 365](https://support.office.com/article/Technical-reference-details-about-encryption-in-Office-365-862CBE93-4268-4EF9-BA79-277545ECF221) for a list of TLS cipher suites supported by Office 365.) This applies to the protocols that are used by clients such as Outlook, Skype for Business, and Outlook on the web (e.g., HTTP, POP3, etc.).</span></span>

<span data-ttu-id="78667-p102">Les certificats publics sont émises par Microsoft IT SSL à l’aide de SSLAdmin, un outil Microsoft interne pour protéger la confidentialité des informations transmises. Tous les certificats émis par Microsoft IT ont un minimum de 2 048 bits de longueur et conformité [Webtrust](http://www.webtrust.org/homepage-documents/item70372.pdf) nécessite SSLAdmin pour vous assurer que les certificats sont émis uniquement à des adresses IP publiques détenus par Microsoft. Toutes les adresses IP qui ne répond à ce critère sont acheminés via un processus d’exception.</span><span class="sxs-lookup"><span data-stu-id="78667-p102">The public certificates are issued by Microsoft IT SSL using SSLAdmin, an internal Microsoft tool to protect confidentiality of transmitted information. All certificates issued by Microsoft IT have a minimum of 2048 bits in length, and [Webtrust](http://www.webtrust.org/homepage-documents/item70372.pdf) compliance requires SSLAdmin to make sure that certificates are issued only to public IP addresses owned by Microsoft. Any IP addresses that fail to meet this criterion are routed through an exception process.</span></span>

<span data-ttu-id="78667-p103">Tous les détails d’implémentation, telles que la version de TLS utilisé, transférer secret (FD) est activé ou non, l’ordre des suites de chiffrement, etc., sont accessibles au public. Permet de voir ces informations consiste à utiliser un site Web tiers, tels que des ateliers de SSL Qualys (www.ssllabs.com). Vous trouverez ci-dessous les liens aux pages de test automatisé de Qualys qui fournissent des informations pour les services suivants :</span><span class="sxs-lookup"><span data-stu-id="78667-p103">All implementation details such as the version of TLS being used, whether Forward Secrecy (FS) is enabled, the order of cipher suites, etc., are available publicly. One way to see these details is to use a third-party website, such as Qualys SSL Labs (www.ssllabs.com). Below are the links to automated test pages from Qualys that display information for the following services:</span></span>
- [<span data-ttu-id="78667-117">Portail Office 365</span><span class="sxs-lookup"><span data-stu-id="78667-117">Office 365 Portal</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=portal.office.com&hideResults=on)
- [<span data-ttu-id="78667-118">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="78667-118">Exchange Online</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=outlook.office365.com&hideResults=on)
- [<span data-ttu-id="78667-119">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="78667-119">SharePoint Online</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=microsoft-my.sharepoint.com&hideResults=on)
- [<span data-ttu-id="78667-120">Skype pour les entreprises (SIP)</span><span class="sxs-lookup"><span data-stu-id="78667-120">Skype for Business (SIP)</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=sipdir.online.lync.com)
- [<span data-ttu-id="78667-121">Skype pour les entreprises (Web)</span><span class="sxs-lookup"><span data-stu-id="78667-121">Skype for Business (Web)</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=webdir.online.lync.com&hideResults=on)
- [<span data-ttu-id="78667-122">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="78667-122">Exchange Online Protection</span></span>](https://ssl-tools.net/mailservers/microsoft-com.mail.protection.outlook.com)
- [<span data-ttu-id="78667-123">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="78667-123">Microsoft Teams</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=teams.microsoft.com&latest)

<span data-ttu-id="78667-124">Pour Exchange Online Protection, URL varient selon les noms de client ; Toutefois, tous les clients peuvent tester Office 365 à l’aide de **microsoft-com.mail.protection.outlook.com**.</span><span class="sxs-lookup"><span data-stu-id="78667-124">For Exchange Online Protection, URLs vary by tenant names; however, all customers can test Office 365 using **microsoft-com.mail.protection.outlook.com**.</span></span>
