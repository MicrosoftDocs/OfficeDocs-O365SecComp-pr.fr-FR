---
title: Chiffrement Office 365 pour les données en transit
ms.author: krowley
author: kccross
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_Enterprise
- M365-security-compliance
- Strat_O365_Enterprise
description: 'Résumé: explique brièvement comment Microsoft chiffre les données en transit.'
ms.openlocfilehash: ba1317a0a2a685d0f3ac2216939d04e402503e49
ms.sourcegitcommit: 7adfd8eda038cf25449bdf3df78b5e2fcc1999e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/01/2019
ms.locfileid: "30357605"
---
# <a name="office-365-encryption-for-data-in-transit"></a>Chiffrement Office 365 pour les données en transit

En plus de protéger les données client au repos, Microsoft utilise des technologies de chiffrement pour protéger les données client Office 365 en transit. 

Les données sont en transit:

- Lorsqu'un ordinateur client communique avec un serveur Office 365;
- Lorsqu'un serveur Office 365 communique avec un autre serveur Office 365; les
- Lorsqu'un serveur Office 365 communique avec un serveur 365 non Office (par exemple, Exchange Online de remise de courrier électronique à un serveur de messagerie étranger).

Les communications entre les centres de contenu entre les serveurs Office 365 s'effectuent via TLS ou IPsec, et tous les serveurs de client négocient une session sécurisée à l'aide de TLS avec des machines client (par exemple, Exchange Online utilise TLS 1,2 avec une force de chiffrement de 256 bits est utilisée (FIPS). 140-2 niveau 2 validé). (Consultez les [Détails de référence technique sur le chiffrement dans office 365](https://support.office.com/article/Technical-reference-details-about-encryption-in-Office-365-862CBE93-4268-4EF9-BA79-277545ECF221) pour obtenir une liste des suites de chiffrement TLS prises en charge par Office 365.) Cela s'applique aux protocoles utilisés par des clients tels qu'Outlook, Skype entreprise et Outlook sur le Web (par exemple, HTTP, POP3, etc.).

Les certificats publics sont émis par Microsoft IT SSL à l'aide de SSLAdmin, un outil Microsoft interne permettant de protéger la confidentialité des informations transmises. Tous les certificats émis par le service informatique de Microsoft ont une longueur minimale de 2048 [](http://www.webtrust.org/homepage-documents/item70372.pdf) bits et la conformité WebTrust nécessite SSLAdmin pour s'assurer que les certificats sont émis uniquement vers des adresses IP publiques appartenant à Microsoft. Toutes les adresses IP qui ne satisfont pas à ce critère sont routées via un processus d'exception.

Tous les détails de l'implémentation, tels que la version de TLS utilisée, si le protocole FS (Forward Secrecy) est activé, l'ordre des suites de chiffrement, etc., sont disponibles publiquement. Pour en savoir plus, vous pouvez utiliser un site Web tiers, tel que Qualys (www.ssllabs.com). Vous trouverez ci-dessous les liens vers les pages de test automatisées de Qualys qui affichent des informations sur les services suivants:

- [Portail Office 365](https://www.ssllabs.com/ssltest/analyze.html?d=portal.office.com&hideResults=on)
- [Exchange Online](https://www.ssllabs.com/ssltest/analyze.html?d=outlook.office365.com&hideResults=on)
- [SharePoint Online](https://www.ssllabs.com/ssltest/analyze.html?d=microsoft-my.sharepoint.com&hideResults=on)
- [Skype entreprise (SIP)](https://www.ssllabs.com/ssltest/analyze.html?d=sipdir.online.lync.com)
- [Skype entreprise (Web)](https://www.ssllabs.com/ssltest/analyze.html?d=webdir.online.lync.com&hideResults=on)
- [Exchange Online Protection](https://ssl-tools.net/mailservers/microsoft-com.mail.protection.outlook.com)
- [Microsoft Teams](https://www.ssllabs.com/ssltest/analyze.html?d=teams.microsoft.com&latest)

Pour Exchange Online Protection, les URL varient en fonction des noms de client; Toutefois, tous les clients peuvent tester Office 365 à l'aide de **Microsoft-com.mail.protection.Outlook.com**.
