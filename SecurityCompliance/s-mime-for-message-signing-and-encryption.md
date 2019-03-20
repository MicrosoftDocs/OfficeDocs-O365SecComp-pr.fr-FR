---
title: S/MIME pour la signature et le chiffrement des messages dans Exchange Online
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 887c710b-0ec6-4ff0-8065-5f05f74afef3
description: Les administrateurs peuvent en savoir plus sur l'utilisation de S/MIME dans Exchange Online.
ms.openlocfilehash: 7c7225efce247928e19946e695c19931f198ae32
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693393"
---
# <a name="smime-for-message-signing-and-encryption-in-exchange-online"></a>S/MIME pour la signature et le chiffrement des messages dans Exchange Online

S/MIME (Secure/Multipurpose Internet Mail Extensions) est une méthode largement acceptée (ou plus précisément, un protocole) pour l'envoi de messages chiffrés et signés numériquement. S/MIME vous permet de chiffrer les courriers électroniques et les signer numériquement. Lorsque vous utilisez S/MIME avec un message électronique, il permet aux personnes qui reçoivent ce message de s'assurer que ce qu'elles voient dans leur boîte de réception est le message exact démarré avec l'expéditeur. Elle permet également aux utilisateurs qui reçoivent des messages de s'assurer que le message provenait d'un expéditeur spécifique et non d'une personne prétendant être l'expéditeur. Pour ce faire, S/MIME fournit des services de sécurité de chiffrement tels que l'authentification, l'intégrité des messages et la non-répudiation de l'origine (à l'aide de signatures numériques). Elle contribue également à améliorer la confidentialité et la sécurité des données (à l'aide du chiffrement) pour la messagerie électronique. Pour en savoir plus sur l'histoire et l'architecture du protocole S/MIME dans le cadre de la messagerie, consultez la rubrique [Présentation du protocole S/MIME](https://go.microsoft.com/fwlink/?LinkID=393948).

En tant qu'administrateur Exchange Online, vous pouvez activer la sécurité basée sur S/MIME pour les boîtes aux lettres de votre organisation. Utilisez les conseils des rubriques associées avec Exchange Online PowerShell pour configurer S/MIME. Pour utiliser S/MIME dans les clients de messagerie pris en charge, les utilisateurs de votre organisation doivent disposer de certificats délivrés à des fins de signature et de chiffrement, ainsi que des données publiées sur votre service de domaine Active Directory (AD DS) local. Vos services AD DS doivent se trouver sur des ordinateurs à un emplacement physique que vous contrôlez et non sur une installation à distance ou un service en nuage sur Internet. Pour plus d'informations sur le service AD DS, consultez la rubrique [Services de domaine Active Directory](https://go.microsoft.com/fwlink/?LinkID=394064).

## <a name="supported-scenarios-and-technical-considerations"></a>Scénarios pris en charge et considérations techniques

Vous pouvez configurer la norme S/MIME afin qu'elle fonctionne avec n'importe lequel des points de terminaison suivants :

- Outlook 2010 ou version ultérieure

- Outlook sur le web (anciennement nommé Outlook Web App)

- Exchange ActiveSync (EAS)

Les étapes à suivre pour configurer S/MIME avec chacun de ces points de terminaison sont légèrement différentes. En règle générale, vous devez effectuer les étapes suivantes:

- Installer une autorité de certification reposant sur Windows et configurer une infrastructure à clé publique pour émettre des certificats S/MIME. Les certificats délivrés par des fournisseurs de certificats tiers sont également pris en charge. Pour plus de détails, reportez-vous à [Vue d'ensemble des services de certificats Active Directory](https://technet.microsoft.com/library/hh831740.aspx).

- Publiez le certificat utilisateur dans un compte AD DS sur site dans les attributs **UserSMIMECertificate** et/ou **UserCertificate** .

- Pour les organisations Exchange Online, synchronisez les certificats utilisateur entre AD DS et Azure Active Directory à l'aide d'une version appropriée de dirSync. Ces certificats seront ensuite synchronisés à partir d'Azure Active Directory vers l'annuaire Exchange Online et seront utilisés lors du chiffrement d'un message à un destinataire.

- Configurer une collection de certificats virtuelle afin de valider S/MIME. Ces informations sont utilisées par Outlook sur le web lorsqu'il valide la signature d'un courrier électronique et vérifie qu'il a été signé par un certificat approuvé.

- Configurer le point de terminaison Outlook ou EAS de sorte qu'il utilise S/MIME.

## <a name="setup-smime-with-outlook-on-the-web"></a>Configuration de S/MIME avec Outlook sur le Web

La configuration de S/MIME pour Exchange Online avec Outlook sur le Web implique les étapes clés suivantes:

1. [Configurer des paramètres S/MIME pour Outlook sur le web](configure-s-mime-settings-for-outlook-web-app.md)

2. [Configuration d’une collection de certificats virtuelle pour la validation des certificats S/MIME](set-up-virtual-certificate-collection-to-validate-s-mime.md)

3. [Synchronisation des certificats utilisateur vers Office 365 pour S/MIME](sync-user-certificates-to-office-365-for-s-mime.md)

## <a name="related-message-encryption-technologies"></a>Technologies liées au chiffrement des messages

Lorsque la sécurité des messages devient plus importante, les administrateurs doivent comprendre les principes et les concepts de la messagerie sécurisée. Cette compréhension est particulièrement importante en raison de l'éventail croissant de technologies liées à la protection (y compris S/MIME) disponibles. Pour en savoir plus sur S/MIME et son fonctionnement dans le contexte de la messagerie, consultez la rubrique [understandIng s/MIME](https://go.microsoft.com/fwlink/?LinkID=393948). Diverses technologies de chiffrement fonctionnent ensemble pour assurer la protection des messages au repos et en transit. S/MIME peut fonctionner simultanément avec les technologies suivantes, mais elle ne dépend pas:

- Le **protocole TLS (Transport Layer Security)** chiffre le tunnel ou le routage entre les serveurs de messagerie afin d'éviter la surveillance et l'espionnage.

- Le **protocole SSL (Secure Sockets Layer)** chiffre la connexion entre les clients de messagerie et les serveurs Office 365.

- **BitLocker** chiffre les données sur un disque dur dans un centre de données de sorte que si quelqu'un obtient un accès non autorisé, il ne peut pas le lire.

### <a name="smime-compared-with-office-365-message-encryption"></a>S/MIME comparé au chiffrement de messages Office 365

S/MIME requiert un certificat et une infrastructure de publication qui est souvent utilisée dans les situations entreprise-entreprise et entreprise-client. L'utilisateur contrôle les clés de chiffrement dans S/MIME et peut choisir de les utiliser ou non pour chaque message qu'il envoie. Les programmes de messagerie (par exemple, Outlook) recherchent un emplacement de certification racine approuvée pour effectuer la signature numérique et vérifier la signature. Le chiffrement de messages Office 365 est un service de chiffrement basé sur une stratégie qui peut être configuré par un administrateur, et non par un utilisateur, afin de chiffrer les messages envoyés à des personnes à l'intérieur ou à l'extérieur de l'organisation. Il s'agit d'un service en ligne basé sur Azure Rights Management (RMS) et qui ne repose pas sur une infrastructure de clé publique. Le chiffrement de messages Office 365 fournit également des fonctionnalités supplémentaires, telles que la fonctionnalité de personnalisation du courrier électronique avec la marque de l'organisation. Pour plus d'informations sur le chiffrement de messages Office 365, consultez la rubrique [office 365 message](https://go.microsoft.com/fwlink/?LinkID=392525)Encryption.

## <a name="more-information"></a>Plus d’informations

[Outlook sur le web](http://technet.microsoft.com/library/3814b665-01e8-4881-9a44-163f14789ee4.aspx)

[Messagerie sécurisée (2000)](https://technet.microsoft.com/en-us/library/cc962043.aspx)
