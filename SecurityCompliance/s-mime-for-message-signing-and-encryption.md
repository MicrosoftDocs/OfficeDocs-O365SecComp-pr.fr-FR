---
title: S/MIME pour la signature et le chiffrement des messages
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 887c710b-0ec6-4ff0-8065-5f05f74afef3
description: S/MIME vous permet de chiffrer les messages électroniques et les signer numériquement. Lorsque vous utilisez S/MIME avec un message électronique, il vous aide aux personnes qui reçoivent ces messages pour être certain que ce qu’ils voient dans leur boîte de réception est le message exact en main de l’expéditeur.
ms.openlocfilehash: 26c50fb6e4d1b07b7dba26948ae46e7f36eeaec5
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002764"
---
# <a name="smime-for-message-signing-and-encryption"></a>S/MIME pour la signature et le chiffrement des messages

S/MIME (Secure/Multipurpose Internet Mail Extensions) est une méthode largement acceptée, ou plus précisément un protocole pour l’envoi numériquement signés et des messages chiffrés. S/MIME vous permet de chiffrer les messages électroniques et les signer numériquement. Lorsque vous utilisez S/MIME avec un message électronique, il vous aide aux personnes qui reçoivent ces messages pour être certain que ce qu’ils voient dans leur boîte de réception est le message exact en main de l’expéditeur. Il vous aide également les personnes qui reçoivent des messages pour être certain que le message provient d’un expéditeur spécifique et non d’une personne se faisant passer pour l’expéditeur. Pour ce faire, S/MIME fournit des services de sécurité cryptographiques tels que l’authentification, l’intégrité des messages et non-répudiation d’origine (à l’aide de signatures numériques). Il permet également d’améliorer la confidentialité et sécurité des données (à l’aide du chiffrement) pour la messagerie électronique. Pour un arrière-plan plus complète sur l’historique et l’architecture de S/MIME dans le contexte de messagerie, voir [Understanding S/MIME](https://go.microsoft.com/fwlink/?LinkID=393948). 
  
En tant qu’administrateur, vous pouvez activer S/MIME-sécurité pour votre organisation si vous avez des boîtes aux lettres dans Exchange 2013 SP1 ou Exchange Online, un cadre d’Office 365. Utilisez les conseils dans les rubriques liées ici ainsi que l’environnement Exchange Management Shell pour configurer S/MIME. Pour utiliser S/MIME dans les versions prises en charge d’Outlook ou d’ActiveSync, avec Exchange 2013 SP1 ou Exchange Online, les utilisateurs de votre organisation doivent avoir des certificats émis à des fins de signature et le chiffrement et les données publiées dans Active Directory sur site Service de domaine (AD DS). Votre domaine Active Directory doit se trouver sur des ordinateurs à un emplacement physique que vous contrôlez et pas à une installation à distance ou d’un service en nuage sur internet. Pour plus d’informations sur les services AD DS, voir [Services de domaine Active Directory](https://go.microsoft.com/fwlink/?LinkID=394064).
  
## <a name="supported-scenarios-and-technical-considerations"></a>Scénarios pris en charge et considérations techniques
<a name="sectionSection0"> </a>

Si votre organisation utilise Exchange 2013 SP1 ou Exchange Online, vous pouvez configurer S/MIME pour travailler avec un des points d’extrémité suivantes : 
  
- Outlook 2010
    
- Outlook 2013
    
- Outlook Web App
    
- Exchange ActiveSync (EAS)
    
Les étapes à suivre pour configurer S/MIME avec chacun de ces points de fin sont légèrement différentes selon celui que vous choisissez. En règle générale, vous devez accomplir les tâches suivantes :
  
- Installez une autorité de Certification basée sur Windows et configurer une infrastructure à clé publique pour émettre des certificats S/MIME. Certificats émis par les fournisseurs de certificats tiers sont également pris en charge. Pour plus d’informations, voir [Présentation de Services de certificats Active Directory](https://technet.microsoft.com/library/hh831740.aspx).
    
- Publier le certificat utilisateur dans un compte AD DS local dans les attributs UserSMIMECertificate et/ou UserCertificate.
    
- Pour les organisations Exchange Online, synchronisez les certificats d’utilisateur de domaine Active Directory pour Azure Active Directory à l’aide d’une version appropriée de synchronisation d’annuaire. Ces certificats seront puis obtenir synchronisées depuis Azure Active Directory vers Exchange Online directory et seront utilisés lors du chiffrement d’un message à un destinataire.
    
- Définir une collection de certificats virtuelle afin de valider S/MIME. Cette information est utilisée lorsqu’OWA valide la signature d’un e-mail et vérifie qu’il a été signé par un certificat approuvé.
    
- Définir le point de fin Outlook ou EAS pour qu’il utilise S/MIME. 
    
## <a name="setup-smime-with-outlook-web-app"></a>Configuration de S/MIME avec Outlook Web App
<a name="sectionSection1"> </a>

Configuration de S/MIME pour Exchange 2013 SP1 ou Exchange Online avec Outlook Web App implique les étapes clés suivantes :
  
1. [Configurer les paramètres S/MIME pour Outlook Web App](configure-s-mime-settings-for-outlook-web-app.md)
    
2. [Configuration d'une collection de certificats virtuelle pour la validation des certificats S/MIME](set-up-virtual-certificate-collection-to-validate-s-mime.md)
    
3. [Synchronisation des certificats utilisateur vers Office 365 pour S/MIME](sync-user-certificates-to-office-365-for-s-mime.md) Cette étape s’applique uniquement à Exchange Online. 
    
## <a name="related-message-encryption-technologies"></a>Technologies liées au chiffrement des messages
<a name="sectionSection2"> </a>

Comme la sécurité des messages devient plus importante, les administrateurs doivent comprendre les principes et les concepts de la messagerie sécurisée. Cela est particulièrement important en raison de la diversité croissante des liés à la protection des technologies, telles que S/MIME, qui sont disponibles. Pour en savoir plus sur S/MIME et comment il fonctionne dans le contexte des courriers électroniques, voir [Understanding S/MIME](https://go.microsoft.com/fwlink/?LinkID=393948). Différentes technologies de chiffrement fonctionnent ensemble pour assurer la protection des messages à rest et de transit. S/MIME peuvent travailler simultanément avec les technologies suivantes, mais n’est pas dépendent :
  
> **Transport Layer Security (TLS)** chiffre le tunnel ou le routage entre les serveurs de messagerie pour empêcher la surveillance et l’écoute électroniques. 
    
> **Secure Sockets Layer (SSL)** chiffre la connexion entre les clients de messagerie et les serveurs Office 365. 
    
> **BitLocker** chiffre les données sur un disque dur dans un centre de données afin que si quelqu'un obtient les accès non autorisés, ils ne peuvent pas lire. 
    
### <a name="smime-compared-with-office-365-message-encryption"></a>S/MIME comparé au chiffrement de messages Office 365

S/MIME requiert une infrastructure de certificat et de publication qui est souvent utilisée dans les situations-entreprises et entreprise-client. L’utilisateur contrôle les clés de chiffrement dans S/MIME et peut choisir de les utiliser pour chaque message qu’ils envoient. Programmes de messagerie tels que Outlook recherche un emplacement d’autorité de certificat racine de confiance pour effectuer la signature numérique et la vérification de la signature. Office 365 le chiffrement de messages est un service de chiffrement basée sur une stratégie qui peut être configuré par un administrateur et non un utilisateur individuel, pour chiffrer les messages envoyés à la personne à l’intérieur ou à l’extérieur de l’organisation. Il est un service en ligne qui repose sur Azure RMS (Rights Management) et ne s’appuie pas sur une infrastructure à clé publique. Chiffrement de messages Office 365 fournit également des fonctionnalités supplémentaires, telles que la possibilité de personnaliser le message avec la marque de l’organisation. Pour plus d’informations sur le chiffrement de messages Office 365, voir [Office 365 Message Encryption](https://go.microsoft.com/fwlink/?LinkID=392525).
  
## <a name="more-information"></a>Plus d'informations
<a name="sectionSection3"> </a>

[Outlook Web App](http://technet.microsoft.com/library/3814b665-01e8-4881-9a44-163f14789ee4.aspx)
  
[Courrier sécurisé (2000)](https://technet.microsoft.com/en-us/library/cc962043.aspx)
  

