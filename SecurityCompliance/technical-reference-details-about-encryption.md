---
title: Détails techniques de référence sur le chiffrement dans Office 365
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
ms.openlocfilehash: 69365b66479ab89a9c036fe489b4087d327460eb
ms.sourcegitcommit: e4ebef6aaf756eefb86c9f3a602cf75f5d344271
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026521"
---
# <a name="technical-reference-details-about-encryption-in-office-365"></a>Détails techniques de référence sur le chiffrement dans Office 365

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

À compter du 31 octobre 2018, Office 365 sera n’est plus prise en charge TLS 1.0 et 1.1. Cela signifie que Microsoft résoudra pas les problèmes qui sont trouvent dans les clients, les périphériques ou les services qui se connectent à Office 365 à l’aide de TLS 1.0 et 1.1.

Notez que cela ne signifie pas Qu'office 365 empêchera TLS 1.0 et 1.1 connexions. Il n’existe aucune date officielle de désactivation ou suppression du service TLS pour les connexions client TLS 1.0 et 1.1. La date de désapprobation éventuelle sera déterminée par la télémétrie client et n’est pas encore connue. Une fois la décision, il y aura une annonce six mois à l’avance, sauf si nous connaissance d’un compromis connu, auquel cas, nous pouvons disposer agir en moins de six mois pour protéger les clients qui utilisent les services.

Vous devez vous assurer que toutes les combinaisons client-serveur et le navigateur et le serveur utilisent TLS 1.2 (ou version ultérieure) pour maintenir la connexion aux services Office 365. Vous devrez peut-être mettre à jour certaines combinaisons client-serveur et le navigateur et le serveur. Pour plus d’informations sur leur impact sur vous, consultez [Préparation pour l’utilisation de TLS 1.2 dans Office 365 obligatoire](https://support.microsoft.com/en-us/help/4057306/preparing-for-tls-1-2-in-office-365).
  
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
  
[Configurer le chiffrement dans Office 365 Entreprise](set-up-encryption.md)
  
[Implémentation de Schannel de TLS 1.0 dans la mise à jour de l’état de sécurité Windows : 24 novembre 2015](https://support.microsoft.com/kb/3117336)
  
[Améliorations du chiffrement TLS/SSL (Windows IT Center)](https://technet.microsoft.com/en-us/library/cc766285%28v=ws.10%29.aspx)
  

