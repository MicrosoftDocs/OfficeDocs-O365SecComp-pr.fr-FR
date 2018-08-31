---
title: Chiffrement dans Microsoft Cloud
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
description: Vue d’ensemble du chiffrement dans le Cloud Microsoft.
ms.openlocfilehash: b8dee7ca7a791878763b885ada40a1d87f074e8e
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528520"
---
# <a name="encryption-in-the-microsoft-cloud"></a>Chiffrement dans Microsoft Cloud

Données client dans les services en nuage de Microsoft enterprise sont protégées par un grand nombre de technologies et de processus, y compris les différentes formes de chiffrement. (Données des clients office 365 dans ce document incluent le contenu de boîte aux lettres Exchange Online (corps du message électronique, des entrées de calendrier et le contenu des pièces jointes et le cas échéant, Skype contenus d’entreprise), le contenu du site SharePoint Online et les fichiers stockés dans sites et des fichiers téléchargement vers OneDrive pour les professionnels ou Skype pour les entreprises.) Microsoft utilise plusieurs méthodes de chiffrement, des protocoles et chiffrement sur ses produits et services afin d’offrir un chemin d’accès sécurisé pour les données du client permettent de parcourir les services en nuage et pour aider à protéger la confidentialité des données du client qui sont stockées dans services en nuage. Microsoft utilise les protocoles de chiffrement plus fort et le plus sécurisé disponibles pour fournir les barrières contre tout accès non autorisé aux données client. Gestion de clés appropriée est également un élément essentiel des meilleures pratiques de chiffrement et Microsoft fonctionne pour vous assurer que toutes les clés de chiffrement gérés par Microsoft sont correctement sécurisés.

Quelle que soit la configuration du client, les données du client stockées dans les services en nuage de Microsoft enterprise sont protégées à l’aide d’un ou plusieurs formulaires de chiffrement. (Validation de notre stratégie de chiffrement et de son application est vérifiée indépendamment de plusieurs comptes de tiers, et les rapports de ces audits sont disponibles sur le [Portail de gestion de la confidentialité du Service](https://aka.ms/stp)).

Microsoft propose des technologies côté service chiffrement les données au repos et en transit du client. Par exemple, pour les données du client au repos, Microsoft Azure utilise [BitLocker](https://docs.microsoft.com/windows/device-security/bitlocker/bitlocker-overview) et [Gd-cryptage](https://en.wikipedia.org/wiki/Dm-crypt)et Microsoft Office 365 utilise service BitLocker, le [Chiffrement de Service de stockage Azure](https://azure.microsoft.com/documentation/articles/storage-service-encryption/), [Distribué le Gestionnaire de clés](https://support.office.com/article/989ba10c-f73f-4efb-ad1b-af3322e5f376) (DKM) et Office 365 chiffrement. Des données du client en transit, Azure, Office 365, Support Commercial de Microsoft, Microsoft Dynamics 365, Microsoft Power BI et Visual Studio Team Services utilisent des protocoles de transport sécurisé standard de l’industrie, telles que la sécurité du protocole Internet (IPsec) et Transport Layer Security (TLS) entre les centres de données Microsoft et entre les périphériques de l’utilisateur et de centres de données Microsoft.

Outre le niveau de base de sécurité de chiffrement fourni par Microsoft, services en nuage comprennent également des options de chiffrement supplémentaires que vous pouvez gérer. Par exemple, vous pouvez activer le chiffrement pour le trafic entre les machines virtuelles Azure (VM) et leurs utilisateurs. [Réseaux virtuels Azure](https://azure.microsoft.com/services/virtual-network/), vous pouvez utiliser le protocole IPsec standard pour chiffrer le trafic entre votre passerelle VPN d’entreprise et les Azure ainsi qu’entre les ordinateurs virtuels situés sur votre réseau virtuel. En outre, en outre, [nouvelles fonctionnalités d’Office 365 Message Encryption](set-up-new-message-encryption-capabilities.md) permettent d’envoyer un message chiffré à tout le monde.

Selon le Public Key Infrastructure opérationnelle sécurité Standard, qui est un composant de la [Stratégie de sécurité de Microsoft](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5868ecc8-50b7-4f91-b43f-640e2b99e86e&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ%20and%20White%20Papers), Microsoft tire parti des fonctionnalités cryptographiques incluses dans le système d’exploitation Windows pour les certificats et mécanismes d’authentification, qui inclut l’utilisation des modules de chiffrement qui répondent à de la réglementation américaine [Federal Information Processing Standards](http://csrc.nist.gov/publications/PubsFIPS.html) (FIPS) standard 140-2. (Numéros de certificat NIST pertinents pour Microsoft se trouvent àhttp://csrc.nist.gov/groups/STM/cmvp/documents/140-1/1401vend.htm.)

> [NOTE] Pour accéder à la stratégie de sécurité de Microsoft en tant que ressource, vous devez vous connecter à l’aide de votre compte professionnel ou de l’école. Si vous ne disposez pas un abonnement encore, [vous pouvez vous inscrire pour un essai gratuit](https://servicetrust.microsoft.com/Home/TrialSubscriptions).

FIPS 140-2 est une norme conçue spécifiquement pour la validation des modules de produit qui implémentent le chiffrement plutôt que les produits qui les utilisent. Modules de chiffrement qui sont implémentés dans un service peuvent être certifiées en tant que la configuration requise pour la notoriété de hachage, gestion de clés et le type de réunion. Chaque fois que les fonctions de chiffrement sont utilisées pour protéger la confidentialité, l’intégrité ou la disponibilité des données dans les services en nuage de Microsoft, les modules et le chiffrement utilisé satisfaire FIPS 140-2 standard.

Microsoft atteste les modules de chiffrement sous-jacent utilisés dans les services en nuage avec chaque nouvelle version du système d’exploitation Windows :
- Azure et Azure américaine
- Dynamics 365 et Dynamics 365 américaine
- Office 365, Office 365 américaine et la défense américain gouvernement Office 365

Chiffrement des données du client Office 365 au repos est fourni par plusieurs technologies côté service, y compris BitLocker, DKM, chiffrement de Service de stockage Azure et le chiffrement de service dans Exchange Online, Skype pour les entreprises, OneDrive pour les entreprises et SharePoint En ligne. Le chiffrement Office 365 service inclut une option pour utiliser des clés de chiffrement gérés par le client qui sont stockés dans Azure clé coffre-fort. Cette option clée client géré, appelée [Clé de client Office 365](https://support.office.com/article/f2cd475a-e592-46cf-80a3-1bfb0fa17697), est disponible pour Exchange Online, SharePoint Online, Skype pour les entreprises et OneDrive for Business.

Pour les données du client en transit, tous les serveurs Office 365 négocient sessions sécurisées à l’aide de TLS par défaut avec les ordinateurs clients pour sécuriser les données du client.  Cela s’applique aux protocoles sur n’importe quel appareil utilisé par les clients, tels que Skype pour les entreprises, Outlook et Outlook sur le web, les clients mobiles, de navigateurs web.

(Tous les serveurs présentés au client la négociation TLS 1,2 par défaut, mais nous prennent également en charge négocier une norme inférieure, si nécessaire).

## <a name="related-links"></a>Liens connexes

- [Chiffrement dans Azure](office-365-azure-encryption.md)
- [BitLocker et distribué Gestionnaire de clés (DKM) pour le chiffrement](office-365-bitlocker-and-distributed-key-manager-for-encryption.md)
- [Chiffrement du Service Office 365](office-365-service-encryption.md)
- [Chiffrement pour Skype pour les entreprises, OneDrive Office 365 pour entreprises, SharePoint Online et Exchange Online](office-365-encryption-for-skype-onedrive-sharepoint-and-exchange.md)
- [Chiffrement des données en Transit](office-365-encryption-for-data-in-transit.md)
- [Fonctionnalités de chiffrement de client géré](office-365-customer-managed-encryption-features.md)
- [Protections et les risques de chiffrement](office-365-encryption-risks-and-protections.md)
- [Chiffrement dans Microsoft Dynamics 365](office-365-encryption-in-microsoft-dynamics-365.md)