---
title: Informations de référence technique de chiffrement dans Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/12/2018
ms.audience: ITPro
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: 862cbe93-4268-4ef9-ba79-277545ecf221
description: Afficher les informations techniques de chiffrement dans Office 365.
ms.openlocfilehash: d86692119f7558d74e2083165b4eb6ab4a07da70
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528505"
---
# <a name="technical-reference-details-about-encryption-in-office-365"></a>Informations de référence technique de chiffrement dans Office 365

Reportez-vous à cet article pour en savoir plus sur les certificats, les technologies et TLS suites de chiffrement utilisées pour le [chiffrement dans Office 365](encryption.md). Cet article fournit également des détails sur planifiées à éviter.
  
- Si vous recherchez des informations générales, voir [chiffrement dans Office 365](encryption.md).
    
- Si vous recherchez des informations de configuration, voir [configurer le chiffrement dans Office 365 pour entreprises](set-up-encryption.md).
    
## <a name="microsoft-office-365-certificate-ownership-and-management"></a>Gestion et propriété de certificats Microsoft Office 365

Il est inutile d’acheter ou de mettre à jour les certificats pour Office 365 car Microsoft utilise ses propres certificats.
  
## <a name="current-encryption-standards-and-planned-deprecations"></a>Les normes de chiffrement en cours et planifiées à éviter

Pour pouvoir continuer à fournir un chiffrement de pointe pour Office 365, Microsoft examine régulièrement les normes de chiffrement pris en charge. Parfois, il faut supprimer des normes anciens dès qu’elles sont obsolètes et par conséquent moins sécurisé. Cette rubrique décrit les suites de chiffrement pris en charge actuellement et autres normes ainsi que des détails sur planifiées à éviter.
  
## <a name="versions-of-tls-supported-by-office-365"></a>Versions de TLS prises en charge par Office 365

Les protocoles TLS (Transport Layer Security) et SSL (antérieur au protocole TLS) sont des protocoles de chiffrement qui sécurisent les communications sur un réseau à l’aide de certificats de sécurité pour chiffrer une connexion entre plusieurs ordinateurs. Office 365 prend en charge plusieurs versions du protocole TLS, notamment :
  
- TLS version 1.2 (TLS 1.2)
    
- TLS version 1.1 (TLS 1.1)
    
- TLS version 1.0 (TLS 1.0)
    
 Prise en charge TLS 1.0 et 1.1 TLS sera déconseillé le 31 octobre 2018. Pour plus d’informations, voir [prise en charge Deprecating pour TLS 1.0 et 1.1 et ce que cela signifie pour vous](technical-reference-details-about-encryption.md#TLS11and12deprecation) . 
  
## <a name="deprecating-support-for-tls-10-and-11-and-what-this-means-for-you"></a>Déconseiller prise en charge TLS 1.0 et 1.1 et ce que cela signifie que vous
<a name="TLS11and12deprecation"> </a>

Provenant des modifications importantes apportées aux options de chiffrement pris en charge pour Office 365. À compter du 31 octobre 2018, Office 365 sera plus en charge l’utilisation de TLS 1.0 ou 1.1 pour les communications vers Office 365. Une fois Office 365 deprecates prise en charge de ces protocoles, toutes les communications vers et depuis les serveurs Office 365 vous devrez utiliser TLS 1.2. Pour plus d’informations sur leur impact sur vous, consultez [Préparation pour l’utilisation de TLS 1.2 dans Office 365 obligatoire](https://support.microsoft.com/en-us/help/4057306/preparing-for-tls-1-2-in-office-365). Serveurs et clients communiquant avec O365 après cette date doivent prendre en charge TLS 1.2.
  
## <a name="deprecating-support-for-3des"></a>Prise en charge 3DES déconseiller
<a name="TLS11and12deprecation"> </a>

À compter du 31 octobre 2018, Office 365 sera plus en charge l’utilisation de suites de chiffrement 3DES pour les communications vers Office 365. Plus précisément, Office 365 ne sera plus en charge la suite de chiffrement TLS_RSA_WITH_3DES_EDE_CBC_SHA. Clients et serveurs de communication avec O365 après cette date doit prendre en charge au moins le chiffrement plus sécurisé répertoriées dans cette rubrique (voir [pris en charge par Office 365 des suites de chiffrement TLS](technical-reference-details-about-encryption.md#TLSCipherSuites)).
  
## <a name="deprecating-sha-1-certificate-support-in-office-365"></a>Arrêt de la prise en charge du certificat SHA-1 dans Office 365
<a name="TLS11and12deprecation"> </a>

À compter de juin 2016, Office 365 n’accepte plus un certificat SHA-1 pour les connexions entrantes ou sortantes. Si vous utilisez actuellement un certificat avec SHA-1 dans la chaîne de certificats, vous devrez mettre à jour la chaîne pour utiliser SHA-2 (Secure 2 d’algorithme de hachage) ou un algorithme de hachage plus puissant.
  
## <a name="deprecating-rc4-support-in-office-365"></a>Arrêt de la prise en charge de RC4 dans Office 365
<a name="TLS11and12deprecation"> </a>

Depuis juillet 2015, les suites de chiffrement RC4 suivantes ne sont plus prises en charge :
  
- TLS_RSA_WITH_RC4_128_SHA
    
- TLS_RSA_WITH_RC4_128_MD5
    
## <a name="deprecating-secure-sockets-layer-ssl-30-support-in-office-365"></a>Déconseiller prise en charge Secure Sockets Layer (SSL) 3.0 dans Office 365
<a name="TLS11and12deprecation"> </a>

Démarrage 1 décembre 2014, Office 365 a commencé à la désactivation de la prise en charge de couche SSL (Secure Sockets) 3.0, le prédécesseur de TLS. Pour plus d’informations, voir [3009008 avis de sécurité](https://technet.microsoft.com/library/security/3009008.aspx). Pour obtenir des instructions sur la vérification de clients sont l’utilisation de TLS 1.0 ou ultérieure et pour désactiver SSL 3.0, consultez la rubrique [protection SSL 3.0 vulnérabilité](http://blogs.office.com/2014/10/29/protecting-ssl-3-0-vulnerability/).
  
## <a name="tls-cipher-suites-supported-by-office-365"></a>Suites de chiffrement TLS pris en charge par Office 365
<a name="TLSCipherSuites"> </a>

Une suite de chiffrement est un ensemble d’algorithmes de chiffrement utilisés par TLS pour établir des connexions sécurisées. Les suites de chiffrement prises en charge par Office 365 sont répertoriées dans le tableau suivant par niveau décroissant. Quand Office 365 reçoit une demande de connexion, il tente tout d’abord de se connecter à l’aide de la première suite de chiffrement, puis en cas d’échec, il utilise la deuxième suite de chiffrement dans la liste, et ainsi de suite. Quand Office 365 envoie une demande de connexion à un autre serveur ou à un client, il incombe au client ou serveur de réception de choisir la suite de chiffrement ou de déterminer s’il convient d’utiliser TLS.
  
|**Protocoles**|**Nom de suite de chiffrement**|**Algorithme d’échange de clés/Niveau**|**Prise en charge de PFS (Perfect Forward Secrecy)**|**Algorithme d’authentification/Niveau**|**Chiffrement/Niveau**|
|:-----|:-----|:-----|:-----|:-----|:-----|
|TLS 1.2  <br/> |TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA384_P384  <br/> |ECDH/192  <br/> |Oui  <br/> |RSA/112  <br/> |AES/256  <br/> |
|TLS 1.2  <br/> |TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA256_P256  <br/> |ECDH/128  <br/> |Oui  <br/> |RSA/112  <br/> |AES/128  <br/> |
|TLS 1.0, 1.1, 1.2  <br/> |TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA_P384  <br/> |ECDH/192  <br/> |Oui  <br/> |RSA/112  <br/> |AES/256  <br/> |
|TLS 1.0, 1.1, 1.2  <br/> |TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA_P256  <br/> |ECDH/128  <br/> |Oui  <br/> |RSA/112  <br/> |AES/128  <br/> |
|TLS 1.2  <br/> |TLS_RSA_WITH_AES_256_CBC_SHA256  <br/> |RSA/112  <br/> |Non  <br/> |RSA/112  <br/> |AES/256  <br/> |
|TLS 1.2  <br/> |TLS_RSA_WITH_AES_128_CBC_SHA256  <br/> |RSA/112  <br/> |Non  <br/> |RSA/112  <br/> |AES/128  <br/> |
|TLS 1.0, 1.1, 1.2  <br/> |TLS_RSA_WITH_AES_256_CBC_SHA  <br/> |RSA/112  <br/> |Non  <br/> |RSA/112  <br/> |AES/256  <br/> |
|TLS 1.0, 1.1, 1.2  <br/> |TLS_RSA_WITH_AES_128_CBC_SHA  <br/> |RSA/112  <br/> |Non  <br/> |RSA/112  <br/> |AES/128  <br/> |
|TLS 1.0, 1.1, 1.2  <br/> |TLS_RSA_WITH_3DES_EDE_CBC_SHA  <br/> |RSA/112  <br/> |Non  <br/> |RSA/112  <br/> |3DES/192  <br/> |
   
## <a name="related-topics"></a>Voir aussi
<a name="TLSCipherSuites"> </a>

[Chiffrement dans Office 365](encryption.md)
  
[Configurez le chiffrement dans Office 365 pour entreprises](set-up-encryption.md)
  
[Implémentation de Schannel de TLS 1.0 dans la mise à jour de l’état de sécurité Windows : 24 novembre 2015](https://support.microsoft.com/kb/3117336)
  
[Améliorations du chiffrement TLS/SSL (Windows IT Center)](https://technet.microsoft.com/en-us/library/cc766285%28v=ws.10%29.aspx)
  

