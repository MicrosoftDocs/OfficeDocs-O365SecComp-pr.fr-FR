---
title: Chiffrement de Skype, OneDrive, SharePoint et Exchange Office 365
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
description: 'Résumé : Description de chiffrement pour Skype, OneDrive, SharePoint et Exchange Online.'
ms.openlocfilehash: 5b839b8d290306f2334d3ca3278d0d5dac20a56f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528114"
---
# <a name="office-365-encryption-for-skype-for-business-onedrive-for-business-sharepoint-online-and-exchange-online"></a>Chiffrement pour Skype pour les entreprises, OneDrive Office 365 pour entreprises, SharePoint Online et Exchange Online

Office 365 est un environnement hautement sécurisé qui offre une protection complète dans plusieurs couches : sécurité, sécurité réseau, sécurité d’accès, la sécurité des applications et la sécurité des données du centre de données physiques.

## <a name="skype-for-business"></a>Skype Entreprise
Skype pour les données métiers client peut-être être stockée au repos sous la forme de fichiers ou des présentations qui sont téléchargées par les participants à la réunion. Le serveur de conférence Web chiffre les données du client à l’aide d’AES avec une clé 256 bits. Les données chiffrées client sont stockées sur un partage de fichiers. Chaque élément de données du client est chiffré à l’aide d’une autre clé 256 bits générée de manière aléatoire. Lorsqu’un élément de données du client est partagé dans une conférence, le serveur de conférence Web demande aux conférence aux clients de télécharger les données du client chiffrés via HTTPS. Il envoie la clé correspondante aux clients afin que les données du client pour pouvoir être déchiffrées. Le serveur de conférence Web authentifie également les clients de conférence avant d’autoriser l’accès aux données client de conférence les clients. Pour prendre part à une conférence Web, chaque client de conférence établit une boîte de dialogue SIP avec le composant de focus conférence exécutant tout d’abord à l’intérieur du serveur frontal via TLS. Le focus de la conférence transmet au client de conférence un cookie d’authentification généré par le serveur de conférence Web. Le client de conférence se connecte ensuite au serveur de conférence Web présentant le cookie d’authentification d’être authentifié par le serveur.

## <a name="sharepoint-online-and-onedrive-for-business"></a>Sharepoint Online et OneDrive Entreprise
Tous les fichiers du client dans SharePoint Online sont protégés par des clés par fichier unique, qui sont toujours propres à un seul client. Les clés sont soit créé et géré par le service en ligne de SharePoint ou lorsque la clé client est utilisée, créé et géré par les clients. Lorsqu’un fichier est téléchargé, le chiffrement est effectué par SharePoint Online dans le contexte de la demande de téléchargement, avant d’être envoyés vers un stockage Azure. Lorsqu’un fichier est téléchargé, SharePoint Online récupère le client chiffré, les données du stockage Azure basée sur l’identificateur de document unique et déchiffre les données du client avant de les envoyer à l’utilisateur. Stockage Azure n’a aucune capacité à déchiffrer, ou même à identifier ou à comprendre les données du client. Chiffrement et déchiffrement se produire dans les systèmes qui appliquent l’isolation du locataire, qui sont Azure Active Directory et SharePoint Online.

Plusieurs charges de travail dans Office 365 stockent des données dans SharePoint Online, y compris Microsoft Teams, qui stocke tous les fichiers dans SharePoint Online et OneDrive entreprise qui utilise SharePoint Online pour son emplacement de stockage. Toutes les données du client stockées dans SharePoint Online est chiffré (avec une ou plusieurs clés AES 256 bits) et réparties sur le centre de données comme suit. (Chaque étape de ce processus de chiffrement est FIPS 140-2 de niveau 2 validé. Pour plus d’informations sur la conformité FIPS 140-2, voir [la conformité FIPS 140-2](https://docs.microsoft.com/previous-versions/sql/sql-server-2008-r2/bb326611(v=sql.105)).)
- Chaque fichier est divisé en un ou plusieurs segments, en fonction de la taille du fichier. Chaque bloc est chiffré avec sa propre clé AES 256 bits unique.
- Lorsqu’un fichier est mis à jour, la mise à jour est géré de la même manière : la modification est divisée en un ou plusieurs segments, et chaque bloc est chiffré avec une clé unique distincte.
- Ces segments – fichiers, fichiers et mise à jour delta – sont stockées en tant qu’objets BLOB dans le stockage Azure répartis de manière aléatoire entre plusieurs comptes de stockage Azure. 
- Le jeu de clés de chiffrement pour ces segments de données du client est elle-même chiffré.
   - Les touches utilisées pour chiffrer les objets BLOB sont stockés dans la base de données de contenu en ligne de SharePoint.
   - La base de données de contenu est protégé par des contrôles d’accès de base de données et le chiffrement au repos. Le chiffrement est effectué à l’aide du [Chiffrement Transparent des données](https://docs.microsoft.com/sql/relational-databases/security/encryption/transparent-data-encryption-tde) (TDE) dans la [Base de données SQL Azure](https://docs.microsoft.com/azure/sql-database/sql-database-technical-overview). (Base de données SQL azure est un service de base de données relationnelle à usage général dans Microsoft Azure qui prend en charge les structures de données relationnelles, JSON, spatiale et XML). Ces secrets sont au niveau du service de SharePoint Online, pas au niveau du client. Ces clés secrètes (parfois appelées les clés principales) sont stockés dans un référentiel sécurisé distinct appelé la banque de clés. TDE offre une sécurité au reste de la base de données active et les sauvegardes de base de données et journaux de transactions. 
   - Lorsque les clients fournir la clé facultative, la clé client est stockée dans Azure clé coffre-fort et le service utilise la clé pour chiffrer une clé client, qui est utilisée pour chiffrer une clé de site, qui est ensuite utilisée pour chiffrer les clés de niveau fichier. En fait, une nouvelle hiérarchie des clés est une nouveauté lorsque le client fournit une clé.
- Le mappage de ré-assembler le fichier est stocké dans la base de données ainsi que les clés chiffrées, indépendamment de la clé principale nécessaires pour déchiffrer les.
- Chaque compte de stockage Azure possède ses propres informations d’identification uniques par type d’accès (lecture, écriture, énumérer et supprimer). Chaque jeu d’informations d’identification est conservé dans la banque d’informations sécurisé clé et est actualisé régulièrement. Comme décrit plus haut, il existe trois types de magasins, chacun avec une fonction distincte :
- Données du client sont stockées en tant que BLOB chiffrés dans le stockage Azure. La clé à chaque bloc de données du client est chiffrée et stockée séparément dans la base de données de contenu. Les données du client ne contient aucun doute sur la façon dont il peut être déchiffré.
- La base de données est une base de données SQL Server. Il conserve le mappage requis pour rechercher et rassembler les blobs de données client en stockage Azure, ainsi que les clés nécessaires pour chiffrer les données BLOB. Toutefois, le jeu de clés est elle-même cryptée (comme expliqué ci-dessus) et conservé dans un magasin distinct de la clé.
- Le magasin de la clé est physiquement distinct du stockage de base de données de contenu et Azure. Il conserve les informations d’identification pour chaque conteneur de stockage Azure et la clé principale à l’ensemble de clés cryptées contenues dans la base de données de contenu.

Chacun de ces trois composants de stockage – magasin blob Azure, la base de données de contenu et la banque de clés – est physiquement distinct. Les informations contenues dans l’un des composants sont inutilisables sur son propre. Sans accès à tous les trois, il est impossible récupérer les clés pour les segments, déchiffrer les clés pour rendre utilisables, associez les clés de leurs segments correspondants, déchiffrer chaque bloc ou reconstruire ses segments constitutifs d’un document.

Certificats BitLocker, qui protègent les volumes de disques physiques sur les ordinateurs dans le centre de données, sont stockés dans un référentiel sécurisé (magasin secrète SharePoint Online) qui est protégé par la clé de la batterie de serveurs.

Les clés TDE qui protègent les clés par blob sont stockées à deux endroits :
- Le référentiel sécurisé, qui héberge les certificats BitLocker et est protégé par la clé de la batterie de serveurs ; et
- Dans un référentiel sécurisé, géré par base de données SQL Azure.

Les informations d’identification utilisées pour accéder aux conteneurs de stockage Azure figurent également dans SharePoint Online secret stocker et délégué pour chaque batterie de serveurs SharePoint Online selon vos besoins. Ces informations d’identification sont des signatures SAS stockage Azure, avec des informations d’identification distinctes utilisées pour lire et écrire des données et stratégie appliquée afin qu’ils auto-expirent tous les 60 jours. Différentes informations d’identification sont utilisées pour lire ou écrire des données (mais pas les deux) et batteries de serveurs SharePoint Online disposent pas d’autorisations pour énumérer.

> Clients de NOTE pour Office 365 américaine, des objets BLOB sont stockés dans le stockage pour le gouvernement Azure US. En outre, l’accès aux clés de SharePoint Online dans Office 365 américaine est limité à Office 365 personnel qui ont été filtré spécifiquement. Le personnel des opérations américaine Azure n’ont pas accès au magasin de clés SharePoint Online est utilisé pour le chiffrement des objets BLOB.

Pour plus d’informations sur le chiffrement des données dans SharePoint Online et OneDrive entreprise, voir le [Chiffrement des données dans OneDrive for Business et SharePoint Online](https://technet.microsoft.com/en-us/library/dn905447.aspx).

### <a name="list-items-in-sharepoint-online"></a>Éléments de liste dans SharePoint Online
Éléments de liste sont plus petits blocs de données sont créées ad hoc ou qui peuvent live plus dynamique au sein d’un site, telles que les lignes d’une liste créée par l’utilisateur, des publications dans un blog SharePoint Online, ou des entrées dans une page wiki SharePoint Online de client. Éléments de liste sont stockés dans la base de données de contenu (de base de données SQL Azure) et protégés avec transparent.

## <a name="encryption-of-data-in-transit"></a>Chiffrement des données lors de leur transport
Dans OneDrive Entreprise et SharePoint Online, il existe deux scénarios dans lesquels les données entrent et sortent des centres de données.
- **Communication du client avec le serveur** - Communication vers OneDrive entreprise sur Internet utilise les connexions SSL/TLS. Toutes les connexions SSL sont établies à l’aide des clés 2048 bits.
- **Déplacement des données entre des centres de données** - la raison principale pour déplacer des données entre des centres de données est de réplication géographique activer la récupération d’urgence. Par exemple, les journaux de transactions SQL Server et delta du stockage blob se déplacent le long de ce canal. Alors que ces données sont déjà transmises à l’aide d’un réseau privé, il est protégé supplémentaire avec le chiffrement de pointe.


## <a name="exchange-online"></a>Exchange Online
Exchange Online utilise BitLocker pour toutes les données de boîtes aux lettres, et la configuration de BitLocker est décrite dans [BitLocker pour le chiffrement](office-365-bitlocker-and-distributed-key-manager-for-encryption.md). Chiffrement au niveau du service chiffre toutes les données de boîtes aux lettres au niveau de la boîte aux lettres. 

Outre le chiffrement-service, Office 365 prend en charge la clé client, qui repose sur le service de chiffrement. Clé de client est une option de clé gérés par Microsoft pour le chiffrement service Exchange Online qui se trouve également dans la feuille de route de Microsoft. Cette méthode de chiffrement fournit une protection renforcée ne pas offerte par BitLocker, car elle fournit la séparation des administrateurs de serveur et les clés de chiffrement nécessaires pour le déchiffrement des données et car le chiffrement est appliqué directement aux données (en contraste avec BitLocker, qui applique le chiffrement sur le volume de disque logique) des données client copiées à partir d’un serveur Exchange restent chiffrées.

L’étendue pour le chiffrement de service Exchange Online est données client stockées au repos dans Exchange Online. (Skype pour les entreprises stocke presque tous les générés par l’utilisateur contenus dans la boîte aux lettres Exchange Online et par conséquent hérite de la fonctionnalité de chiffrement de service d’Exchange Online).
