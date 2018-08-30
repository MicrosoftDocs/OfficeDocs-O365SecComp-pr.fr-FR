---
title: Mode d’utilisation de TLS par Exchange Online pour sécuriser les connexions de messagerie dans Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 8/2/2018
ms.audience: ITPro
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: 4cde0cda-3430-4dc0-b489-f2c0736c929f
description: Découvrez comment Exchange Online et Office 365 utilisent Transport Layer Security (TLS) et transférer secret (FD) pour sécuriser les communications électroniques. Également obtenir des informations sur le certificat émis par Microsoft pour Exchange Online.
ms.openlocfilehash: 079a6f574838f5710dbbbcb53726799abfae1d3a
ms.sourcegitcommit: ddfa0ac1f8ef95a78dcc1468241ef29363d56b5b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/30/2018
ms.locfileid: "23520143"
---
# <a name="how-exchange-online-uses-tls-to-secure-email-connections-in-office-365"></a>Mode d’utilisation de TLS par Exchange Online pour sécuriser les connexions de messagerie dans Office 365

Découvrez comment Exchange Online et Office 365 utilisent Transport Layer Security (TLS) et transférer secret (FD) pour sécuriser les communications électroniques. Fournit des informations sur le certificat émis par Microsoft pour Exchange Online.
  
## <a name="tls-basics-for-office-365-and-exchange-online"></a>Concepts de base TLS pour Office 365 et Exchange Online

Transport Layer Security (TLS) et SSL qui précèdent TLS, sont des protocoles de chiffrement pour sécuriser les communications via un réseau à l’aide de certificats de sécurité pour chiffrer une connexion entre les ordinateurs. TLS remplace Secure Sockets Layer (SSL) et est souvent appelé SSL 3.1. Pour Exchange Online, nous utilisons TLS pour chiffrer les connexions entre nos serveurs Exchange et les connexions entre nos serveurs Exchange et d’autres serveurs tels que des serveurs Exchange locaux ou des serveurs de messagerie de vos destinataires. Une fois la connexion cryptée, toutes les données envoyées via cette connexion est envoyée via le canal chiffré. Toutefois, si vous transférez un message qui a été envoyé via une connexion TLS sécurisée, ce message n’est pas nécessairement chiffré. Il s’agit, car, en termes simples, TLS ne chiffre pas le message, uniquement la connexion.
  
Si vous souhaitez chiffrer le message, vous devez utiliser une technologie de chiffrement qui chiffre le contenu du message, par exemple, le chiffrement de messages Office. Voir [Email encryption in Office 365](email-encryption.md) et [Office 365 Message Encryption (OME)](ome.md) pour plus d’informations sur les options de chiffrement de messages dans Office 365. 
  
Nous recommandons l’utilisation de TLS dans les situations où vous souhaitez configurer un canal sécurisé de correspondance entre Office 365 et votre organisation locale ou une autre organisation, comme un partenaire. Exchange Online toujours tente d’abord utiliser TLS pour sécuriser votre messagerie électronique mais ne peut pas toujours faire ceci si l’autre partie n’offre pas de sécurité TLS. Continuez la lecture pour savoir comment vous pouvez protéger tout le courrier vers vos serveurs locaux ou des partenaires importantes à l’aide de *connecteurs*. 
  
## <a name="how-exchange-online-uses-tls-between-exchange-online-customers"></a>Comment Exchange Online utilise TLS entre des clients Exchange Online

Les serveurs Exchange Online chiffrent toujours les connexions à d’autres serveurs Exchange Online de nos centres de données avec le protocole TLS 1.2. Lorsque vous envoyez du courrier à un destinataire qui se trouve au sein de votre organisation Office 365, ce message électronique est automatiquement envoyé via une connexion chiffrée à l’aide du protocole TLS. En outre, tous les messages électroniques que vous envoyez à d’autres clients Office 365 sont envoyés via des connexions qui sont chiffrées à l’aide du protocole TLS et sécurisées à l’aide de FS (Forward Secrecy).
  
## <a name="how-office-365-uses-tls-between-office-365-and-external-trusted-partners"></a>Comment Office 365 utilise TLS entre partenaires externes, approuvés et Office 365

Par défaut, Exchange Online utilise toujours TLS opportuniste. Cela signifie que Exchange Online toujours tente d’abord chiffrer les connexions avec la version la plus sécurisée de TLS, puis le fonctionnement son vers le bas de la liste de chiffrement TLS jusqu'à ce qu’il en trouve un sur lequel les deux parties peuvent accepter. Sauf si vous avez configuré Exchange Online pour vous assurer que les messages envoyés à ce destinataire sont envoyées uniquement via une connexion sécurisée, puis par défaut le message sera être envoyé non chiffré si l’entreprise destinataire ne prend pas en charge le chiffrement TLS. TLS opportuniste est suffisante pour la plupart des entreprises. Toutefois, pour les entreprises qui ont des exigences de conformité telles que des soins médicaux, bancaires ou administrations, vous pouvez configurer Exchange Online pour demander ou forcer, TLS. Pour plus d’informations, voir [configurer le flux de messagerie à l’aide de connecteurs dans Office 365](https://technet.microsoft.com/library/ms.exch.eac.connectorselection%28v=exchg.150%29.aspx).
  
Si vous décidez de configurer le TLS entre votre organisation et une organisation partenaire approuvé, Exchange Online peut utiliser TLS forcé pour créer des canaux de communication approuvés. TLS forcé requiert votre organisation partenaire pour authentifier vers Exchange Online avec un certificat de sécurité afin de vous envoyer du courrier électronique. Votre partenaire vous devrez gérer leurs propres certificats pour pouvoir effectuer cette opération. Dans Exchange Online, nous utilisons les connecteurs pour protéger les messages envoyés à partir de tout accès non autorisé avant qu’ils arrivent sur le fournisseur de messagerie électronique du destinataire. Pour plus d’informations sur l’utilisation de connecteurs pour configurer le flux de messagerie, voir [configurer le flux de messagerie à l’aide de connecteurs dans Office 365](https://technet.microsoft.com/library/ms.exch.eac.connectorselection%28v=exchg.150%29.aspx).
  
## <a name="tls-and-hybrid-exchange-server-deployments"></a>Déploiements Exchange Server hybrides et TLS

Si vous gérez un déploiement Exchange hybride, vous avez besoin sur site Exchange server pour s’authentifier auprès d’Office 365 à l’aide d’un certificat de sécurité pour pouvoir envoyer du courrier électronique aux destinataires dont les boîtes aux lettres uniquement dans Office 365. Par conséquent, vous devez gérer vos propres certificats de sécurité des serveurs Exchange locaux. Vous devez également de conserver les certificats de serveur. Pour plus d’informations sur la gestion des certificats dans les déploiements hybrides, consultez [certificats requis pour les déploiements hybrides](https://technet.microsoft.com/library/hh563848%28v=exchg.150%29.aspx).
  
## <a name="how-to-set-up-forced-tls-for-exchange-online-in-office-365"></a>Configuration du TLS forcé pour Exchange Online dans Office 365

Pour les clients Exchange Online, pour TLS forcé à utiliser pour sécuriser tous vos courriers électroniques entrants et sortants, vous devez configurer plusieurs connecteurs qui requiert TLS. Vous aurez besoin d’un connecteur pour le courrier électronique envoyé à vos boîtes aux lettres d’utilisateur et un autre connecteur pour les e-mails envoyés à partir de vos boîtes aux lettres utilisateur. Créez ces connecteurs dans le centre d’administration Exchange dans Office 365. Pour plus d’informations, voir [configurer le flux de messagerie à l’aide de connecteurs dans Office 365](https://technet.microsoft.com/library/ms.exch.eac.connectorselection%28v=exchg.150%29.aspx).
  
## <a name="tls-certificate-information-for-exchange-online"></a>Informations de certificat TLS pour Exchange Online

Les informations de certificat utilisées par Exchange Online sont décrit dans le tableau suivant. Si votre partenaire commercial configure TLS forcé sur leur serveur de messagerie, vous devrez fournir cette information leur. Sachez que pour des raisons de sécurité, nos certificats changent à tout moment. Nous avons déployé une mise à jour à notre certificat dans nos centres de données. Le nouveau certificat valide à partir du 3 septembre 2018.
  
 **Informations de certificat valides à partir du 3 septembre 2018 actuel**
  
|**Attribut**|**Valeur**|
|:-----|:-----|
|Émetteur racine de l’autorité de certification  <br/> |Racine GlobalSign CA – R1 <br/> |
|Nom du certificat  <br/> |Mail.protection.Outlook.com  <br/> |
|Organisation  <br/> |Microsoft Corporation  <br/> |
|Unité d’organisation  <br/> |  <br/> |
|Puissance de clé de certificat  <br/> |2048  <br/> |
   
 **Informations relatives au certificat obsolètes valide jusqu'à ce que le 3 septembre 2018**
  
Pour garantir une transition en douceur, il continuera à fournir les informations de certificat ancienne de référence pendant un certain temps, toutefois, vous devez utiliser désormais les informations de certificat en cours.
  
****

|**Attribut**|**Valeur**|
|:-----|:-----|
|Émetteur racine de l’autorité de certification  <br/> |Baltimore CyberTrust Root  <br/> |
|Nom du certificat  <br/> |Mail.protection.Outlook.com  <br/> |
|Organisation  <br/> |Microsoft Corporation  <br/> |
|Unité d’organisation  <br/> |Microsoft Corporation  <br/> |
|Puissance de clé de certificat  <br/> |2048  <br/> |
   
## <a name="prepare-for-the-new-exchange-online-certificate"></a>Préparer le nouveau certificat Exchange Online

Le nouveau certificat émis par une autorité de certification différente (CA) à partir du certificat précédent utilisé par Exchange Online. Par conséquent, vous devrez peut-être effectuer certaines actions pour pouvoir utiliser le nouveau certificat.

Le nouveau certificat requiert la connexion aux points de terminaison de la nouvelle autorité de certification dans le cadre de la validation du certificat. Cela peut entraîner des flux de messagerie en cours affecté. Si vous protégez vos serveurs de messagerie avec les pare-feu qui permettent uniquement les serveurs de messagerie de se connecter avec certaines destinations, que vous devez vérifier si votre serveur est en mesure de valider le nouveau certificat. Pour vérifier que votre serveur peut utiliser le nouveau certificat, procédez comme suit :

1. Se connecter à votre serveur Exchange local à l’aide de Windows PowerShell, puis exécutez la commande suivante :  
  `certutil -URL http://crl.globalsign.com/gsorganizationvalsha2g3.crl`
2. Dans la fenêtre qui s’affiche, cliquez sur **récupérer**.
3. Lorsque l’utilitaire a terminé ses vérification il renvoie l’état. Si l’état **OK**s’affiche, votre serveur de messagerie peut valider correctement le nouveau certificat. Si ce n’est pas le cas, vous devez déterminer la cause de l’échec des connexions. Très probablement, vous devez mettre à jour les paramètres d’un pare-feu. La liste complète des points de terminaison qui doivent être accessibles sont les suivantes :
    - OCSP.GlobalSign.com
     - CRL.GlobalSign.com
     - Secure.GlobalSign.com   

Normalement, vous recevez des mises à jour pour vos certificats racine automatiquement par le biais de Windows Update. Toutefois, certains déploiements ont plus de sécurité en place qui empêche ces mises à jour automatiquement. Dans ces déploiements verrouillés où Windows Update ne peut pas mettre à jour automatiquement des certificats racines, vous devez vous assurer que le certificat d’autorité de certification racine d’approprié est installé en procédant comme suit :
1.  Se connecter à votre serveur Exchange local à l’aide de Windows PowerShell, puis exécutez la commande suivante :  
  `certmgr.msc`
2. Sous **Approuvés Certification/certificats d’autorité racine**, vérifiez que le nouveau certificat est répertorié.

## <a name="get-more-information-about-tls-and-office-365"></a>Obtenir plus d’informations sur TLS et Office 365

Pour obtenir la liste des suites de chiffrement pris en charge, voir [informations de référence technique de chiffrement dans Office 365](technical-reference-details-about-encryption.md).
  
[Configurer des connecteurs pour un flux de messagerie sécurisé avec une organisation partenaire](https://technet.microsoft.com/library/dn751021%28v=exchg.150%29.aspx)
  
[Connecteurs avec sécurité de messagerie électronique renforcée](https://technet.microsoft.com/library/261d92e4-7371-4555-b781-2062b5bb5278.aspx)
  
[Chiffrement dans Office 365](encryption.md)
  

