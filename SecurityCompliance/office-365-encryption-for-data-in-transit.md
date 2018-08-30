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
# <a name="office-365-encryption-for-data-in-transit"></a>Chiffrement Office 365 pour les données en transit

En plus de la protection des données au repos du client, Microsoft utilise des technologies de chiffrement pour protéger les données du client Office 365 en transit. 

Les données sont en transit :
- Lorsqu’un ordinateur client communique avec un serveur d’Office 365 ;
- Lorsqu’un serveur Office 365 communique avec un autre serveur d’Office 365 ; et
- Lorsqu’un serveur Office 365 communique avec un serveur d’Office 365 (par exemple, Exchange Online en courrier électronique à un serveur de messagerie externe).

Communications inter-centre de données entre les serveurs Office 365 a lieu sur TLS ou IPsec, et tous les serveurs présentés au client négocient une session sécurisée avec les ordinateurs clients utilisant le protocole TLS (par exemple, Exchange Online utilise TLS 1.2 avec 256 bits est utilisée (FIPS 140-2 niveau validé par 2). (Voir [plus d’informations techniques de référence sur le chiffrement dans Office 365](https://support.office.com/article/Technical-reference-details-about-encryption-in-Office-365-862CBE93-4268-4EF9-BA79-277545ECF221) pour obtenir la liste des suites de chiffrement TLS pris en charge par Office 365). Cela s’applique aux protocoles utilisés par les clients tels qu’Outlook, Skype pour les entreprises et Outlook sur le site web (par exemple, HTTP, POP3, etc.).

Les certificats publics sont émises par Microsoft IT SSL à l’aide de SSLAdmin, un outil Microsoft interne pour protéger la confidentialité des informations transmises. Tous les certificats émis par Microsoft IT ont un minimum de 2 048 bits de longueur et conformité [Webtrust](http://www.webtrust.org/homepage-documents/item70372.pdf) nécessite SSLAdmin pour vous assurer que les certificats sont émis uniquement à des adresses IP publiques détenus par Microsoft. Toutes les adresses IP qui ne répond à ce critère sont acheminés via un processus d’exception.

Tous les détails d’implémentation, telles que la version de TLS utilisé, transférer secret (FD) est activé ou non, l’ordre des suites de chiffrement, etc., sont accessibles au public. Permet de voir ces informations consiste à utiliser un site Web tiers, tels que des ateliers de SSL Qualys (www.ssllabs.com). Vous trouverez ci-dessous les liens aux pages de test automatisé de Qualys qui fournissent des informations pour les services suivants :
- [Portail Office 365](https://www.ssllabs.com/ssltest/analyze.html?d=portal.office.com&hideResults=on)
- [Exchange Online](https://www.ssllabs.com/ssltest/analyze.html?d=outlook.office365.com&hideResults=on)
- [SharePoint Online](https://www.ssllabs.com/ssltest/analyze.html?d=microsoft-my.sharepoint.com&hideResults=on)
- [Skype pour les entreprises (SIP)](https://www.ssllabs.com/ssltest/analyze.html?d=sipdir.online.lync.com)
- [Skype pour les entreprises (Web)](https://www.ssllabs.com/ssltest/analyze.html?d=webdir.online.lync.com&hideResults=on)
- [Exchange Online Protection](https://ssl-tools.net/mailservers/microsoft-com.mail.protection.outlook.com)
- [Microsoft Teams](https://www.ssllabs.com/ssltest/analyze.html?d=teams.microsoft.com&latest)

Pour Exchange Online Protection, URL varient selon les noms de client ; Toutefois, tous les clients peuvent tester Office 365 à l’aide de **microsoft-com.mail.protection.outlook.com**.
