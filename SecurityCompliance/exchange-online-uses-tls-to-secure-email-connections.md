---
title: Mode d’utilisation de TLS par Exchange Online pour sécuriser les connexions de messagerie dans Office 365
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 8/2/2018
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
search.appverid:
- MET150
- MOE150
ms.assetid: 4cde0cda-3430-4dc0-b489-f2c0736c929f
description: Découvrez comment Exchange Online et Office 365 utilisent le protocole TLS (Transport Layer Security) et la confidentialité de transmission (FD) pour sécuriser les communications de messagerie. Obtenir également des informations sur le certificat émis par Microsoft pour Exchange Online.
ms.openlocfilehash: 2621bb325c5bf97baa0a25f1e5eb590339856549
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220494"
---
# <a name="how-exchange-online-uses-tls-to-secure-email-connections-in-office-365"></a>Mode d’utilisation de TLS par Exchange Online pour sécuriser les connexions de messagerie dans Office 365

Découvrez comment Exchange Online et Office 365 utilisent le protocole TLS (Transport Layer Security) et la confidentialité de transmission (FD) pour sécuriser les communications de messagerie. Fournit également des informations sur le certificat émis par Microsoft pour Exchange Online.
  
## <a name="tls-basics-for-office-365-and-exchange-online"></a>Concepts de base TLS pour Office 365 et Exchange Online

Le protocole TLS (Transport Layer Security) et SSL fourni avant TLS, sont des protocoles de chiffrement qui sécurisent la communication sur un réseau à l'aide de certificats de sécurité pour chiffrer une connexion entre des ordinateurs. Le protocole TLS remplace SSL (Secure Sockets Layer) et est souvent appelé SSL 3,1. Pour Exchange Online, nous utilisons le protocole TLS pour chiffrer les connexions entre nos serveurs Exchange et les connexions entre nos serveurs Exchange et d'autres serveurs tels que vos serveurs Exchange locaux ou les serveurs de messagerie de vos destinataires. Une fois la connexion chiffrée, toutes les données envoyées via cette connexion sont envoyées via le canal chiffré. Toutefois, si vous transférez un message qui a été envoyé par le biais d'une connexion chiffrée TLS, ce message n'est pas nécessairement chiffré. En d'autres termes, TLS ne chiffre pas le message, mais seulement la connexion.
  
Si vous souhaitez chiffrer le message, vous devez utiliser une technologie de chiffrement qui chiffre le contenu du message, par exemple, le chiffrement de messages Office. Voir [Email encryption in Office 365](email-encryption.md) et [Office 365 Message Encryption (OME)](ome.md) pour plus d’informations sur les options de chiffrement de messages dans Office 365. 
  
Nous vous recommandons d'utiliser le protocole TLS dans les situations où vous souhaitez configurer un canal sécurisé de correspondance entre Office 365 et votre organisation locale ou une autre organisation, telle qu'un partenaire. Exchange Online tente toujours d'utiliser TLS en premier pour sécuriser votre courrier électronique, mais vous ne pouvez pas toujours le faire si l'autre partie n'offre pas de sécurité TLS. Poursuivez votre lecture pour savoir comment sécuriser tous les messages vers vos serveurs locaux ou des partenaires importants à l'aide de *connecteurs*. 
  
## <a name="how-exchange-online-uses-tls-between-exchange-online-customers"></a>Comment Exchange Online utilise TLS entre des clients Exchange Online

Les serveurs Exchange Online chiffrent toujours les connexions à d’autres serveurs Exchange Online de nos centres de données avec le protocole TLS 1.2. Lorsque vous envoyez du courrier à un destinataire qui se trouve au sein de votre organisation Office 365, ce message électronique est automatiquement envoyé via une connexion chiffrée à l’aide du protocole TLS. En outre, tous les messages électroniques que vous envoyez à d’autres clients Office 365 sont envoyés via des connexions qui sont chiffrées à l’aide du protocole TLS et sécurisées à l’aide de FS (Forward Secrecy).
  
## <a name="how-office-365-uses-tls-between-office-365-and-external-trusted-partners"></a>Utilisation de TLS par Office 365 entre Office 365 et des partenaires approuvés externes

Par défaut, Exchange Online utilise toujours le protocole TLS opportuniste. En d'autres termes, Exchange Online essaie toujours de chiffrer les connexions avec la version la plus sécurisée du protocole TLS en premier, puis le fait descendre dans la liste des chiffrements TLS jusqu'à ce qu'il en trouve un sur lequel les deux parties peuvent s'accorder. Sauf si vous avez configuré Exchange Online pour vous assurer que les messages envoyés à ce destinataire sont uniquement envoyés via des connexions sécurisées, le message est envoyé par défaut sans chiffrement si l'organisation destinataire ne prend pas en charge le chiffrement TLS. Le protocole TLS opportuniste est suffisant pour la plupart des entreprises. Toutefois, pour les entreprises qui ont des exigences de conformité, telles que les organisations médicales, bancaires ou gouvernementales, vous pouvez configurer Exchange Online pour qu'il exige ou force le protocole TLS. Pour obtenir des instructions, consultez la rubrique [configure mail Flow using Connectors in Office 365](https://technet.microsoft.com/library/ms.exch.eac.connectorselection%28v=exchg.150%29.aspx).
  
Si vous décidez de configurer TLS entre votre organisation et une organisation partenaire approuvée, Exchange Online peut utiliser le protocole TLS forcé pour créer des canaux de communication approuvés. Le protocole TLS forcé nécessite que votre organisation partenaire s'authentifie auprès d'Exchange Online avec un certificat de sécurité pour vous envoyer des courriers électroniques. Votre partenaire devra gérer ses propres certificats afin de le faire. Dans Exchange Online, nous utilisons des connecteurs pour protéger les messages que vous envoyez d'un accès non autorisé avant qu'ils n'arrivent au fournisseur de messagerie du destinataire. Pour plus d'informations sur l'utilisation des connecteurs pour configurer le flux de messagerie, consultez la rubrique [configure mail Flow using Connectors in Office 365](https://technet.microsoft.com/library/ms.exch.eac.connectorselection%28v=exchg.150%29.aspx).
  
## <a name="tls-and-hybrid-exchange-server-deployments"></a>Déploiements Exchange Server hybrides et TLS

Si vous gérez un déploiement Exchange hybride, votre serveur Exchange local doit s'authentifier auprès d'Office 365 à l'aide d'un certificat de sécurité afin d'envoyer des messages aux destinataires dont les boîtes aux lettres sont uniquement dans Office 365. Par conséquent, vous devez gérer vos propres certificats de sécurité pour vos serveurs Exchange locaux. Vous devez également stocker et maintenir en toute sécurité ces certificats de serveur. Pour plus d'informations sur la gestion des certificats dans les déploiements hybrides, consultez la rubrique [Certificate Requirements for Hybrid Deployments](https://technet.microsoft.com/library/hh563848%28v=exchg.150%29.aspx).
  
## <a name="how-to-set-up-forced-tls-for-exchange-online-in-office-365"></a>Configuration du TLS forcé pour Exchange Online dans Office 365

Pour les clients Exchange Online, pour que le protocole TLS forcé fonctionne afin de sécuriser tous les messages électroniques envoyés et reçus, vous devez configurer plusieurs connecteurs nécessitant TLS. Vous avez besoin d'un connecteur pour les messages électroniques envoyés à vos boîtes aux lettres utilisateur et un autre connecteur pour les messages envoyés à partir de vos boîtes aux lettres utilisateur. Créez ces connecteurs dans le centre d'administration Exchange dans Office 365. Pour obtenir des instructions, consultez la rubrique [configure mail Flow using Connectors in Office 365](https://technet.microsoft.com/library/ms.exch.eac.connectorselection%28v=exchg.150%29.aspx).
  
## <a name="tls-certificate-information-for-exchange-online"></a>Informations de certificat TLS pour Exchange Online

Les informations de certificat utilisées par Exchange Online sont décrites dans le tableau suivant. Si votre partenaire commercial configure le protocole TLS forcé sur son serveur de messagerie, vous devrez lui fournir ces informations. N'oubliez pas que, pour des raisons de sécurité, nos certificats changent de temps en temps. Nous avons déployé une mise à jour de notre certificat dans nos centres de contenu. Le nouveau certificat est valide à partir du 3 septembre 2018.
  
 **Informations de certificat actuelles valides à partir du 3 septembre 2018**
  
|**Attribut**|**Valeur**|
|:-----|:-----|
|Émetteur racine de l’autorité de certification  <br/> |AUTORITÉ de certification racine GlobalSign – R1 <br/> |
|Nom du certificat  <br/> |mail.protection.Outlook.com  <br/> |
|Organisation  <br/> |Microsoft Corporation  <br/> |
|Unité d’organisation  <br/> |  <br/> |
|Puissance de clé de certificat  <br/> |2048  <br/> |
   
 **Informations de certificat déConseillées valides jusqu'au 3 septembre 2018**
  
Pour vous aider à assurer une transition sans complication, nous continuerons à fournir les anciennes informations de certificat pour votre référence pendant un certain temps, mais vous devez utiliser les informations de certificat actuelles à partir de maintenant.
  
****

|**Attribut**|**Valeur**|
|:-----|:-----|
|Émetteur racine de l’autorité de certification  <br/> |Baltimore CyberTrust Root  <br/> |
|Nom du certificat  <br/> |mail.protection.Outlook.com  <br/> |
|Organisation  <br/> |Microsoft Corporation  <br/> |
|Unité d’organisation  <br/> |Microsoft Corporation  <br/> |
|Puissance de clé de certificat  <br/> |2048  <br/> |
   
## <a name="prepare-for-the-new-exchange-online-certificate"></a>Préparer le nouveau certificat Exchange Online

Le nouveau certificat est émis par une autorité de certification (CA) différente du certificat précédent utilisé par Exchange Online. Par conséquent, vous devrez peut-être effectuer certaines actions pour pouvoir utiliser le nouveau certificat.

Le nouveau certificat nécessite la connexion aux points de terminaison de la nouvelle autorité de certification dans le cadre de la validation du certificat. Si vous ne le faites pas, le flux de messagerie risque d'être affecté. Si vous protégez vos serveurs de messagerie avec des pare-feu qui permettent uniquement aux serveurs de messagerie de se connecter à certaines destinations, vous devez vérifier si votre serveur est en mesure de valider le nouveau certificat. Pour vérifier que votre serveur peut utiliser le nouveau certificat, procédez comme suit:

1. Connectez-vous à votre serveur Exchange local à l'aide de Windows PowerShell, puis exécutez la commande suivante:  
  `certutil -URL http://crl.globalsign.com/gsorganizationvalsha2g3.crl`
2. Dans la fenêtre qui s'affiche, sélectionnez **récupérer**.
3. Lorsque l'utilitaire termine sa vérification, il renvoie un État. Si l'état affiche **OK**, votre serveur de messagerie peut valider le nouveau certificat. Si ce n'est pas le cas, vous devez déterminer la cause de l'échec des connexions. Il est fort probable que vous deviez mettre à jour les paramètres d'un pare-feu. La liste complète des points de terminaison à accéder est la suivante:
    - OCSP.GlobalSign.com
     - CRL.GlobalSign.com
     - Secure.GlobalSign.com   

Normalement, vous recevez automatiquement des mises à jour de vos certificats racines via Windows Update. Toutefois, certains déploiements disposent d'une sécurité supplémentaire qui empêche ces mises à jour de se produire automatiquement. Dans ces déploiements verrouillés où Windows Update ne peut pas mettre à jour automatiquement les certificats racines, vous devez vous assurer que le certificat d'autorité de certification racine correct est installé en procédant comme suit:
1.  Connectez-vous à votre serveur Exchange local à l'aide de Windows PowerShell, puis exécutez la commande suivante:  
  `certmgr.msc`
2. Sous **autorités de certification racines de confiance**, vérifiez que le nouveau certificat est affiché.

## <a name="get-more-information-about-tls-and-office-365"></a>Obtenir plus d’informations sur TLS et Office 365

Pour obtenir la liste des suites de chiffrement prises en charge, consultez la [référence technique détails sur le chiffrement dans Office 365](technical-reference-details-about-encryption.md).
  
[Configurer des connecteurs pour un flux de messagerie sécurisé avec une organisation partenaire](https://technet.microsoft.com/library/dn751021%28v=exchg.150%29.aspx)
  
[Connecteurs avec sécurité de messagerie électronique renforcée](https://technet.microsoft.com/library/261d92e4-7371-4555-b781-2062b5bb5278.aspx)
  
[Chiffrement dans Office 365](encryption.md)
  

