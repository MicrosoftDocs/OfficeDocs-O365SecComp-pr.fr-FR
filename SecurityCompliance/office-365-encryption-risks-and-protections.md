---
title: Protections et les risques de chiffrement office 365
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
description: 'Résumé : Découvrez la résistance des données dans Microsoft Office 365.'
ms.openlocfilehash: 69956c5f32f74a93b2101d2651ef7de03ad1094f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528708"
---
# <a name="encryption-risks-and-protections"></a>Protections et les risques de chiffrement

Microsoft suit une structure de contrôle et de conformité qui se concentre sur les risques pour le service Office 365 et aux données client. Microsoft implémente un grand ensemble de la technologie et les méthodes basées sur les processus (désignés comme contrôles) afin d’atténuer ces risques. Identification, l’évaluation et atténuation des risques via des contrôles est un processus continu. L’implémentation des contrôles dans les différentes couches de services en nuage tels que les installations, réseau, serveurs, applications, les utilisateurs (par exemple, les administrateurs de Microsoft) et données de formulaire une stratégie de défense en profondeur. La clé de cette stratégie est que de nombreux contrôles différents sont implémentées dans les différentes couches de protection contre les scénarios de risque similaires ou identiques. Cette approche multiniveau offre une protection de sécurité intégrée en cas de défaillance d’un contrôle pour une raison quelconque. Certains scénarios impliquant des risques et des technologies de chiffrement actuellement disponibles qui atténuent les sont répertoriés ci-dessous. Ces scénarios sont souvent également réduits par le biais d’autres contrôles implémentés dans Office 365.

| Technologie de chiffrement | les services | Gestion de clés | Scénario de risque | Valeur |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|---------------------|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BitLocker | Exchange Online, SharePoint Online et Skype pour les entreprises | Microsoft | Des disques ou des serveurs dans Office 365 sont volés ou mal recyclés. | BitLocker fournit une approche sécurité intégrée pour la protection contre la perte de données en raison de matériel volé ou mal recyclé (serveur/disque). |
| Chiffrement de service | SharePoint Online, Skype pour les entreprises et OneDrive entreprise ; Exchange Online (sur une feuille de route) | Microsoft | Pirate interne ou externe tente d’accéder aux fichiers individuelles/données comme un objet blob. | Impossible de déchiffrer les données chiffrées sans accès aux clés. Contribue à réduire les risques d’un pirate l’accès aux données. |
| Clé client | SharePoint Online, OneDrive entreprise, Exchange Online et Skype pour les entreprises | Client | N/a (cette fonctionnalité est conçue comme une fonctionnalité de conformité ; pas comme une atténuation pour tout risque). | Permet aux clients de répondre aux règlement interne et les obligations de conformité et la possibilité de laisser le service Office 365 et révoquer l’accès aux données de Microsoft |
| TLS entre les clients et Office 365 | Exchange Online, SharePoint Online, OneDrive entreprise, Skype pour les professionnels et les équipes Yammer | Microsoft, client | Man-in-the-middle ou une autre attaque de cliquer sur le flux de données entre Office 365 et les ordinateurs clients sur Internet. | Cette implémentation offre une valeur à Microsoft et les clients et permet de garantir l’intégrité des données circulant entre le client et Office 365. |
| TLS entre des centres de données Microsoft | Exchange Online, SharePoint Online, OneDrive entreprise et Skype pour les entreprises | Microsoft | Man-in-the-middle ou une autre attaque de cliquer sur le flux de données client entre les serveurs Office 365 situés dans différents centres de données Microsoft. | Cette implémentation est une autre méthode pour protéger les données contre les attaques entre des centres de données Microsoft. |
| Azure Rights Management (inclus dans Office 365 ou Azure Information Protection) | Exchange Online, SharePoint Online et OneDrive entreprise | Client | Données se trouve à la disposition d’une personne qui ne doivent pas comporter de l’accès aux données. | Protection des informations Azure utilise RMS Azure qui fournit la valeur pour les clients à l’aide de stratégies de chiffrement, d’identité et d’autorisation pour aider à sécuriser les fichiers et de messagerie sur plusieurs périphériques. RMS Azure fournit une valeur pour les clients où tous les messages électroniques provenant d’Office 365 qui correspondent à certains critères (autrement dit, tous les messages électroniques à une adresse spécifique) peuvent être automatiquement chiffrées avant d’obtenir envoyés à un autre destinataire. |
| S/MIME | Exchange Online | Client | Courrier électronique se situe à la disposition d’une personne qui n’est pas le destinataire prévu. | S/MIME fournit une valeur pour les clients en garantissant que courrier électronique chiffré avec S/MIME peut uniquement être déchiffré par le destinataire du courrier électronique direct. |
| Chiffrement de messages Office 365 | Exchange Online, SharePoint Online | Client | Courrier électronique, y compris les pièces jointes protégés, fait partie de mains d’une personne dans ou hors d’Office 365 n’est pas le destinataire du message électronique. | OME fournit la valeur pour les clients où tous les messages électroniques provenant d’Office 365 qui correspondent à certains critères (autrement dit, tous les messages électroniques à une adresse spécifique) sont automatiquement chiffrés avant d’obtenir envoyés vers un autre interne ou un destinataire externe. |
| SMTP TLS avec l’organisation partenaire | Exchange Online | Client | Courrier électronique est interceptée par le biais d’une attaque man-in-the-middle ou autres lors de leur transit à partir d’un client Office 365 à une autre organisation partenaire. | Ce scénario fournit la valeur pour le client où ils peuvent envoi/réception tous les messages électroniques entre leur organisation cliente Office 365 et d’organisation de messagerie de leur partenaire à l’intérieur d’un canal SMTP chiffré. |

Les tableaux suivants présentent les technologies de chiffrement disponibles dans les environnements Office 365 multiclients et gouvernement nuage communautaire.

| Technologie de chiffrement | Implémentée par | Résistance et l’algorithme d’échange de clé | Gestion de clés * | FIPS 140-2 validées |
|----------------------------------------------------------------------------------|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| BitLocker | Exchange Online | AES 128-bit + | Clé externe AES est stockée dans une clé secrète fiables et dans le Registre du serveur Exchange. La clé secrète sans échec est un référentiel sécurisé qui requiert l’élévation de haut niveau et les approbations pour accéder à. Access peut être demandé et d’approuver uniquement à l’aide d’un outil interne appelé zone de sécurité. La clé externe AES est également stockée dans le Module de plateforme sécurisée sur le serveur. Un mot de passe numérique à 48 chiffres est stocké dans Active Directory et protégé par la zone de sécurité. | Oui, pour les serveurs qui utilisent AES 256-bit ** |
|  | SharePoint Online | AES 256 bits | Clé externe AES est stockée dans une clé secrète fiables. La clé secrète sans échec est un référentiel sécurisé qui requiert l’élévation de haut niveau et les approbations pour accéder à. Access peut être demandé et d’approuver uniquement à l’aide d’un outil interne appelé zone de sécurité. La clé externe AES est également stockée dans le Module de plateforme sécurisée sur le serveur. Un mot de passe numérique à 48 chiffres est stocké dans Active Directory et protégé par la zone de sécurité. | Oui |
|  | Skype Entreprise | AES 256 bits | Clé externe AES est stockée dans une clé secrète fiables. La clé secrète sans échec est un référentiel sécurisé qui requiert l’élévation de haut niveau et les approbations pour accéder à. Access peut être demandé et d’approuver uniquement à l’aide d’un outil interne appelé zone de sécurité. La clé externe AES est également stockée dans le Module de plateforme sécurisée sur le serveur. Un mot de passe numérique à 48 chiffres est stocké dans Active Directory et protégé par la zone de sécurité. | Oui |
| Chiffrement de service | SharePoint Online | AES 256 bits | Les touches utilisées pour chiffrer les objets BLOB sont stockés dans la base de données de contenu en ligne de SharePoint. SharePoint Online bases de données est protégé par des contrôles d’accès de base de données et le chiffrement au repos. Le chiffrement est effectué à l’aide de TDE dans la base de données SQL Azure. Ces secrets sont au niveau du service de SharePoint Online, pas au niveau du client. Ces clés secrètes (parfois appelées les clés principales) sont stockés dans un référentiel sécurisé distinct appelé la banque de clés. TDE offre une sécurité au reste de la base de données active et les sauvegardes de base de données et journaux de transactions. Lorsque les clients fournir la clé facultative, la clé client est stockée dans Azure clé coffre-fort et le service utilise la clé pour chiffrer une clé client, qui est utilisée pour chiffrer une clé de site, qui est ensuite utilisée pour chiffrer les clés de niveau fichier. En fait, une nouvelle hiérarchie des clés est une nouveauté lorsque le client fournit une clé. | Oui |
|  | Skype Entreprise | AES 256 bits | Chaque élément de données est chiffré à l’aide d’une autre clé 256 bits générée de manière aléatoire. La clé de chiffrement est stockée dans un fichier XML métadonnées correspondant est également chiffré par une clé principale de par conférence. La clé principale est également aléatoire générée une seule fois par conférence. | Oui |
|  | Exchange Online | AES 256 bits | Chaque boîte aux lettres est chiffré à l’aide d’une stratégie de chiffrement de données qui utilise des clés de chiffrement contrôlés par Microsoft (sur une feuille de route) ou par le client (lorsque la clé client est utilisée). | Oui |
| TLS entre Office 365 et les clients/partenaires | Exchange Online | [TLS opportuniste prenant en charge plusieurs suites de chiffrement](https://technet.microsoft.com/en-us/library/mt163898.aspx) | Le certificat TLS pour Exchange Online (outlook.office.com) est un certificat SHA256RSA de 2048 bits émis par la racine de CyberTrust Baltimore. | Oui, à 1.2 TLS avec le niveau de chiffrement 256 bits est utilisé. |
|  |  |  | Le certificat racine TLS pour Exchange Online est un certificat SHA1RSA de 2048 bits émis par la racine de CyberTrust Baltimore. |  |
|  | SharePoint Online | TLS 1.2 avec AES 256 | Le certificat TLS pour SharePoint Online (*. sharepoint.com) est un certificat SHA256RSA de 2048 bits émis par la racine de CyberTrust Baltimore. | Oui |
|  |  | [Chiffrement de données dans OneDrive Entreprise et SharePoint Online](https://technet.microsoft.com/en-us/library/dn905447.aspx) | Le certificat racine TLS pour SharePoint Online est un certificat SHA1RSA de 2048 bits émis par la racine de CyberTrust Baltimore. |  |
|  | Skype Entreprise | [TLS pour les communications SIP et les sessions de partage de données PSOM](https://support.office.com/article/Set-up-your-network-for-Skype-for-Business-Online-d21f89b0-3afc-432e-b735-036b2432fdbf) | Le certificat TLS pour Skype pour les entreprises (*. lync.com) est un certificat SHA256RSA de 2048 bits émis par la racine de CyberTrust Baltimore. | Oui |
|  |  |  | Le certificat racine TLS pour Skype pour les entreprises est un certificat SHA256RSA de 2048 bits émis par la racine de CyberTrust Baltimore. |  |
|  | Microsoft Teams | TLS 1.2 avec AES 256 | Le certificat TLS pour Microsoft Teams (teams.microsoft.com, edge.skype.com) est un certificat SHA256RSA de 2048 bits émis par la racine de CyberTrust Baltimore. | Oui |
|  |  | [Forum aux questions sur Microsoft Teams – aide d’administration](https://docs.microsoft.com/MicrosoftTeams/teams-overview) | Le certificat racine TLS pour Microsoft Teams est un certificat SHA256RSA de 2048 bits émis par la racine de CyberTrust Baltimore. |  |
| TLS entre des centres de données Microsoft | Tous les services Office 365 | TLS 1.2 avec AES 256 | Microsoft utilise une autorité de certification interne gérés et déployés pour les communications de serveur à serveur entre des centres de données Microsoft. | Oui |
|  |  | Secure Real-Time Transport Protocol (SRTP) |  |  |
| Azure Rights Management (inclus dans Office 365 ou Azure Information Protection) | Exchange Online | Prend en charge le [chiffrement Mode 2](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/hh867439(v=ws.10)), une implémentation de chiffrement RMS mis à jour et améliorée. Il prend en charge 2048 RSA pour la signature et le chiffrement SHA-256 pour le hachage de la signature. | [Géré par Microsoft](https://docs.microsoft.com/azure/information-protection/plan-implement-tenant-key). | Oui |
|  | SharePoint Online | Prend en charge le [chiffrement Mode 2](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/hh867439(v=ws.10)), une implémentation de chiffrement RMS mis à jour et améliorée. Il prend en charge 2048 RSA pour la signature et le chiffrement SHA-256 pour la signature. | [Géré par Microsoft](https://docs.microsoft.com/azure/information-protection/plan-implement-tenant-key), qui est le paramètre par défaut ; ou | Oui |
|  |  |  | Client géré, qui est une alternative aux clés gérés par Microsoft. Organisation qui ont un abonnement Azure gérés BYOK et de connecter son utilisation sans frais supplémentaires. Pour plus d’informations, voir [implémentation de fournir votre propre clé](https://docs.microsoft.com/azure/information-protection/plan-implement-tenant-key). Dans cette configuration, Thales HSM sont utilisées pour protéger vos clés. Pour plus d’informations, voir [Thales HSM et Azure RMS](http://www.thales-esecurity.com/msrms/cloud). |  |
| S/MIME | Exchange Online | Syntaxe de Message cryptographique 1,5 Standard (PKCS #7) | Dépend de client géré infrastructure à clé publique déployée. Gestion de clés n’est effectuée par le client, et Microsoft n’a jamais accès aux clés privées utilisée pour la signature et le déchiffrement. | Oui, est configuré pour chiffrer les messages sortants avec 3DES ou AES256 |
| Chiffrement de messages Office 365 | Exchange Online | Identique à Azure RMS ([chiffrement Mode 2](https://technet.microsoft.com/en-us/library/dn569290.aspx) - 2048 RSA pour la signature et le chiffrement et SHA-256 pour signature) | Utilise la Protection des informations Azure comme son infrastructure de chiffrement. La méthode de chiffrement utilisée dépend où vous procurer les clés de RMS utilisés pour chiffrer et déchiffrer des messages. | Oui |
| SMTP TLS avec l’organisation partenaire | Exchange Online | TLS 1.2 avec AES 256 | Le certificat TLS pour Exchange Online (outlook.office.com) est un certificat SHA256RSA de 2048 bits émis par la racine de CyberTrust Baltimore. | Oui, à 1.2 TLS avec le niveau de chiffrement 256 bits est utilisé. |
|  |  |  | Le certificat racine TLS pour Exchange Online est un certificat SHA1RSA de 2048 bits émis par la racine de CyberTrust Baltimore. |  |

**Certificats TLS référencés dans ce tableau sont pour les centres de données américains ; centres de données non-US également utilisent des certificats SHA256RSA 2048 bits.*

***La plupart des serveurs dans l’environnement mutualisé Exchange Online ont été déployés avec un chiffrement AES 256 bits pour BitLocker. Serveurs à l’aide d’AES 128 bits sont obsolètes.*

| Technologie de chiffrement | Implémentée par | Résistance et l’algorithme d’échange de clé | Gestion de clés * | FIPS 140-2 validées |
|---------------------------------------------|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| BitLocker | Exchange Online | AES 256 bits | Clé externe AES est stockée dans une clé secrète fiables et dans le Registre du serveur Exchange. La clé secrète sans échec est un référentiel sécurisé qui requiert l’élévation de haut niveau et les approbations pour accéder à. Access peut être demandé et d’approuver uniquement à l’aide d’un outil interne appelé zone de sécurité. La clé externe AES est également stockée dans le Module de plateforme sécurisée sur le serveur. Un mot de passe numérique à 48 chiffres est stocké dans Active Directory et protégé par la zone de sécurité. | Oui |
|  | SharePoint Online | AES 256 bits | Clé externe AES est stockée dans une clé secrète fiables. La clé secrète sans échec est un référentiel sécurisé qui requiert l’élévation de haut niveau et les approbations pour accéder à. Access peut être demandé et d’approuver uniquement à l’aide d’un outil interne appelé zone de sécurité. La clé externe AES est également stockée dans le Module de plateforme sécurisée sur le serveur. Un mot de passe numérique à 48 chiffres est stocké dans Active Directory et protégé par la zone de sécurité. | Oui |
|  | Skype Entreprise | AES 256 bits | Clé externe AES est stockée dans une clé secrète fiables. La clé secrète sans échec est un référentiel sécurisé qui requiert l’élévation de haut niveau et les approbations pour accéder à. Access peut être demandé et d’approuver uniquement à l’aide d’un outil interne appelé zone de sécurité. La clé externe AES est également stockée dans le Module de plateforme sécurisée sur le serveur. Un mot de passe numérique à 48 chiffres est stocké dans Active Directory et protégé par la zone de sécurité. | Oui |
| Chiffrement de service | SharePoint Online | AES 256 bits | Les touches utilisées pour chiffrer les objets BLOB sont stockés dans la base de données de contenu en ligne de SharePoint. SharePoint Online bases de données est protégé par des contrôles d’accès de base de données et le chiffrement au repos. Le chiffrement est effectué à l’aide de TDE dans la base de données SQL Azure. Ces secrets sont au niveau du service de SharePoint Online, pas au niveau du client. Ces clés secrètes (parfois appelées les clés principales) sont stockés dans un référentiel sécurisé distinct appelé la banque de clés. TDE offre une sécurité au reste de la base de données active et les sauvegardes de base de données et journaux de transactions. Lorsque les clients fournir la clé facultative, la clé client est stockée dans Azure clé coffre-fort et le service utilise la clé pour chiffrer une clé client, qui est utilisée pour chiffrer une clé de site, qui est ensuite utilisée pour chiffrer les clés de niveau fichier. En fait, une nouvelle hiérarchie des clés est une nouveauté lorsque le client fournit une clé. | Oui |
|  | Skype Entreprise | AES 256 bits | Chaque élément de données est chiffré à l’aide d’une autre clé 256 bits générée de manière aléatoire. La clé de chiffrement est stockée dans un fichier XML métadonnées correspondant est également chiffré par une clé principale de par conférence. La clé principale est également aléatoire générée une seule fois par conférence. | Oui |
|  | Exchange Online | AES 256 bits | Chaque boîte aux lettres est chiffré à l’aide d’une stratégie de chiffrement de données qui utilise des clés de chiffrement contrôlés par Microsoft ou par le client (lorsque la clé client est utilisée). | Oui |
| TLS entre Office 365 et les clients/partenaires | Exchange Online | [TLS opportuniste prenant en charge plusieurs suites de chiffrement](https://technet.microsoft.com/en-us/library/mt163898.aspx) | Le certificat TLS pour Exchange Online (outlook.office.com) est un certificat SHA256RSA de 2048 bits émis par la racine de CyberTrust Baltimore. | Oui, à 1.2 TLS avec le niveau de chiffrement 256 bits est utilisé. |
|  |  |  | Le certificat racine TLS pour Exchange Online est un certificat SHA1RSA de 2048 bits émis par la racine de CyberTrust Baltimore. |  |
|  | SharePoint Online | TLS 1.2 avec AES 256 | Le certificat TLS pour SharePoint Online (*. sharepoint.com) est un certificat SHA256RSA de 2048 bits émis par la racine de CyberTrust Baltimore. | Oui |
|  |  |  | Le certificat racine TLS pour SharePoint Online est un certificat SHA1RSA de 2048 bits émis par la racine de CyberTrust Baltimore. |  |
|  | Skype Entreprise | TLS pour les communications SIP et les sessions de partage de données PSOM | Le certificat TLS pour Skype pour les entreprises (*. lync.com) est un certificat SHA256RSA de 2048 bits émis par la racine de CyberTrust Baltimore. | Oui |
|  |  |  | Le certificat racine TLS pour Skype pour les entreprises est un certificat SHA256RSA de 2048 bits émis par la racine de CyberTrust Baltimore. |  |
|  | Microsoft Teams | [Forum aux questions sur Microsoft Teams – aide d’administration](https://docs.microsoft.com/MicrosoftTeams/teams-overview) | Le certificat TLS pour Microsoft Teams (teams.microsoft.com ; edge.skype.com) est un certificat SHA256RSA de 2048 bits émis par la racine de CyberTrust Baltimore. | Oui |
|  |  |  | Le certificat racine TLS pour Microsoft Teams est un certificat SHA256RSA de 2048 bits émis par la racine de CyberTrust Baltimore. |  |
| TLS entre des centres de données Microsoft | Exchange Online, SharePoint Online, Skype pour les entreprises | TLS 1.2 avec AES 256 | Microsoft utilise une autorité de certification interne gérés et déployés pour les communications de serveur à serveur entre des centres de données Microsoft. | Oui |
|  |  | Secure Real-Time Transport Protocol (SRTP) |  |  |
| Azure Rights Management Service | Exchange Online | Prend en charge le [chiffrement Mode 2](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/hh867439(v=ws.10)), une implémentation de chiffrement RMS mis à jour et améliorée. Il prend en charge 2048 RSA pour la signature et le chiffrement SHA-256 pour le hachage de la signature. | [Géré par Microsoft](https://docs.microsoft.com/azure/information-protection/plan-implement-tenant-key). | Oui |
|  | SharePoint Online | Prend en charge le [chiffrement Mode 2](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/hh867439(v=ws.10)), une implémentation de chiffrement RMS mis à jour et améliorée. Il prend en charge 2048 RSA pour la signature et le chiffrement SHA-256 pour le hachage de la signature. | [Géré par Microsoft](https://docs.microsoft.com/azure/information-protection/plan-implement-tenant-key), qui est le paramètre par défaut ; ou | Oui |
|  |  |  | Client géré (alias BYOK), qui est une alternative aux clés gérés par Microsoft. Organisation qui ont un abonnement Azure gérés BYOK et de connecter son utilisation sans frais supplémentaires. Pour plus d’informations, voir [implémentation de fournir votre propre clé](https://docs.microsoft.com/azure/information-protection/plan-implement-tenant-key). |  |
|  |  |  | Dans le scénario BYOK, Thales HSM sont utilisées pour protéger vos clés. Pour plus d’informations, voir [Thales HSM et Azure RMS](http://www.thales-esecurity.com/msrms/cloud). |  |
| S/MIME | Exchange Online | Syntaxe de Message cryptographique 1,5 Standard (PKCS #7) | Dépend de l’infrastructure à clé publique déployée. | Oui, est configuré pour chiffrer les messages sortants avec 3DES ou AES-256. |
| Chiffrement de messages Office 365 | Exchange Online | Identique à Azure RMS ([chiffrement Mode 2](https://technet.microsoft.com/en-us/library/dn569290.aspx) - 2048 RSA pour la signature et le chiffrement et SHA-256 pour le hachage de la signature) | Utilise son infrastructure de chiffrement RMS Azure. La méthode de chiffrement utilisée dépend où vous procurer les clés de RMS utilisés pour chiffrer et déchiffrer des messages. | Oui |
|  |  |  | Si vous utilisez Microsoft Azure RMS pour obtenir les clés, chiffrement Mode 2 est utilisé. Si vous utilisez RMS Active Directory (AD) pour obtenir les clés, chiffrement Mode 1 ou 2 de Mode de chiffrement est utilisée. La méthode utilisée dépend de votre site de déploiement AD RMS. Mode de chiffrement 1 est l’implémentation de chiffrement AD RMS d’origine. Il prend en charge RSA 1024 pour la signature et le chiffrement et SHA-1 pour la signature. Ce mode continue à être pris en charge par toutes les versions actuelles du serveur RMS, à l’exception des configurations de BYOK avec des modules HSM. |  |
| SMTP TLS avec l’organisation partenaire | Exchange Online | TLS 1.2 avec AES 256 | Le certificat TLS pour Exchange Online (outlook.office.com) est un certificat SHA256RSA de 2048 bits émis par la racine de CyberTrust Baltimore. | Oui |
|  |  |  | Le certificat racine TLS pour Exchange Online est un certificat de 2048 bits sha1RSA émis par la racine de CyberTrust Baltimore. |  |
|  |  |  | *Sachez que pour des raisons de sécurité, nos certificats changent à tout moment.* |  |

**Certificats TLS référencés dans ce tableau sont pour les centres de données américains ; centres de données non-US également utilisent des certificats SHA256RSA 2048 bits.*