---
title: Chiffrement Office 365 pour Skype, OneDrive, SharePoint et Exchange
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
description: 'Résumé: description du chiffrement pour Skype, OneDrive, SharePoint et Exchange Online.'
ms.openlocfilehash: 55141f671e6cb3d7ea837bfcf9701e37a18fb7ba
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262786"
---
# <a name="office-365-encryption-for-skype-for-business-onedrive-for-business-sharepoint-online-and-exchange-online"></a>Chiffrement Office 365 pour Skype entreprise, OneDrive entreprise, SharePoint Online et Exchange Online

Office 365 est un environnement hautement sécurisé qui fournit une protection étendue à de nombreux niveaux : sécurité de centre de données physique, sécurité réseau, sécurité d'accès, sécurité des applications et sécurité des données.

## <a name="skype-for-business"></a>Skype Entreprise

Les données client Skype entreprise peuvent être stockées sous la forme de fichiers ou de présentations téléchargés par les participants à la réunion. Le serveur de conférence Web chiffre les données client à l'aide de l'AES avec une clé 256 bits. Les données client chiffrées sont stockées sur un partage de fichiers. Chaque donnée client est chiffrée à l'aide d'une clé différente générée de manière aléatoire et de l' 256 bits. Lorsqu'une partie des données client est partagée dans une conférence, le serveur de conférence Web indique aux clients de conférence de télécharger les données client chiffrées via HTTPs. Il envoie la clé correspondante aux clients afin que les données client puissent être déchiffrées. Le serveur de conférence Web authentifie également les clients de conférence avant de permettre aux clients d'accéder aux données des clients de conférence. Lors de la participation à une conférence Web, chaque client de Conférence établit une boîte de dialogue SIP avec le composant de focus de conférence exécuté à l'intérieur du serveur frontal sur TLS en premier. Le focus de conférence transmet au client de conférence un cookie d'authentification généré par le serveur de conférence Web. Le client de conférence se connecte ensuite au serveur de conférence Web présentant le cookie d'authentification à authentifier par le serveur.

## <a name="sharepoint-online-and-onedrive-for-business"></a>Sharepoint Online et OneDrive Entreprise

Tous les fichiers de client dans SharePoint Online sont protégés par des clés uniques par fichier qui sont toujours exclusives à un seul client. Les clés sont créées et gérées par le service SharePoint Online, ou lorsque la clé client est utilisée, créée et gérée par les clients. Lorsqu'un fichier est téléchargé, le chiffrement est effectué par SharePoint Online dans le contexte de la demande de téléchargement, avant d'être envoyé à Azure Storage. Lorsqu'un fichier est téléchargé, SharePoint Online récupère les données client chiffrées à partir de l'emplacement de stockage Azure en fonction de l'identificateur de document unique et déchiffre les données client avant de les envoyer à l'utilisateur. Le stockage Azure ne peut pas déchiffrer, voire identifier ou comprendre les données client. Tout le chiffrement et le déchiffrement se produisent dans les mêmes systèmes qui appliquent l'isolation du client, à savoir Azure Active Directory et SharePoint Online.

Plusieurs charges de travail dans Office 365 stockent des données dans SharePoint Online, notamment Microsoft Teams, qui stocke tous les fichiers dans SharePoint Online et OneDrive entreprise, qui utilise SharePoint Online pour son stockage. Toutes les données client stockées dans SharePoint Online sont chiffrées (avec une ou plusieurs clés AES 256 bits) et distribuées dans le centre de données comme suit. (Chaque étape de ce processus de chiffrement est validée par le niveau 2 FIPS 140-2. Pour plus d'informations sur la conformité FIPS 140-2, voir [fips 140-2 Compliance](https://docs.microsoft.com/previous-versions/sql/sql-server-2008-r2/bb326611(v=sql.105)).)

- Chaque fichier est divisé en un ou plusieurs segments, en fonction de la taille du fichier. Chaque segment est chiffré à l'aide de sa propre clé AES 256 bits unique.
- Lorsqu'un fichier est mis à jour, la mise à jour est gérée de la manière suivante: la modification est divisée en un ou plusieurs segments, et chaque segment est chiffré avec une clé unique distincte.
- Ces blocs (fichiers, fragments de fichiers et deltas de mise à jour) sont stockés en tant qu'objets BLOB dans le stockage Azure qui sont répartis de manière aléatoire entre plusieurs comptes de stockage Azure.
- L'ensemble des clés de chiffrement pour ces blocs de données client est lui-même chiffré.

    - Les clés utilisées pour chiffrer les objets BLOB sont stockées dans la base de données de contenu SharePoint Online.
    - La base de données de contenu est protégée par les contrôles d'accès aux bases de données et le chiffrement au repos. Le chiffrement est effectué à l'aide du [chiffreMent transparent des données](https://docs.microsoft.com/sql/relational-databases/security/encryption/transparent-data-encryption-tde) (TDE) dans la [base de données SQL Azure](https://docs.microsoft.com/azure/sql-database/sql-database-technical-overview). (Azure SQL Database est un service de base de données relationnelle à usage général dans Microsoft Azure qui prend en charge des structures telles que des données relationnelles, JSON, spatiale et XML.) Ces secrets se situent au niveau du service pour SharePoint Online, et non au niveau du client. Ces secrets (parfois appelés clés principales) sont stockés dans un référentiel sécurisé distinct appelé magasin de clés. TDE fournit la sécurité au repos pour la base de données active et les sauvegardes de base de données et les journaux de transaction.
    - Lorsque les clients fournissent la clé facultative, la clé client est stockée dans le coffre de clés Azure et le service utilise la clé pour chiffrer une clé de client, qui est utilisée pour chiffrer une clé de site, qui est ensuite utilisée pour chiffrer les clés de niveau fichier. Fondamentalement, une nouvelle hiérarchie de clés est introduite lorsque le client fournit une clé.
- Le mappage utilisé pour ré-assembler le fichier est stocké dans la base de données de contenu avec les clés chiffrées, séparément de la clé principale nécessaire pour les déchiffrer.
- Chaque compte de stockage Azure possède ses propres informations d'identification propres par type d'accès (lecture, écriture, énumération et suppression). Chaque jeu d’informations d’identification est conservé dans le magasin de clés sécurisé et est régulièrement actualisé. Comme indiqué ci-dessus, il existe trois types différents de magasins, chacun avec une fonction distincte:
    - Les données client sont stockées en tant qu'objets BLOB chiffrés dans le stockage Azure. La clé de chaque segment de données client est chiffrée et stockée séparément dans la base de données de contenu. Les données client elles-mêmes ne contiennent aucune indication quant à la façon dont elles peuvent être déchiffrées.
    - La base de données de contenu est une base de données SQL Server. Il contient le mappage requis pour localiser et réassembler les blobs de données client détenus dans le stockage Azure, ainsi que les clés nécessaires pour chiffrer ces objets BLOB. Toutefois, le jeu de clés est lui-même chiffré (comme expliqué ci-dessus) et il est conservé dans un magasin de clés distinct.
    - Le magasin de clés est physiquement distinct de la base de données de contenu et de l'espace de stockage Azure. Il contient les informations d'identification de chaque conteneur de stockage Azure et la clé principale de l'ensemble des clés chiffrées contenues dans la base de données de contenu.

Chacun de ces trois composants de stockage (le magasin d'objets BLOB Azure, la base de données de contenu et le magasin de clés) est physiquement distinct. Les informations contenues dans l'un des composants sont inutilisables en tant que telles. S'il n'y a pas accès aux trois, il est impossible de récupérer les clés des segments, de déchiffrer les clés pour les rendre utilisables, d'associer les clés à leurs segments correspondants, de déchiffrer chaque segment ou de reconstruire un document à partir de ses segments constitutifs.

Les certificats BitLocker, qui protègent les volumes des disques physiques sur les ordinateurs du centre de contenu, sont stockés dans un référentiel sécurisé (le magasin de secrets SharePoint Online) qui est protégé par la clé de la batterie de serveurs.

Les clés TDE qui protègent les clés par BLOB sont stockées à deux emplacements:

- Le référentiel sécurisé, qui héberge les certificats BitLocker, est protégé par la clé de la batterie de serveurs; les
- Dans un référentiel sécurisé géré par Azure SQL Database.

Les informations d'identification utilisées pour accéder aux conteneurs Azure Storage sont également conservées dans le magasin de secrets SharePoint Online et déléguées à chaque batterie de serveurs SharePoint Online selon vos besoins. Ces informations d'identification sont des signatures Azure Storage SAS, avec des informations d'identification distinctes utilisées pour lire ou écrire des données, et une stratégie appliquée de sorte qu'elles expirent automatiquement tous les 60 jours. D'autres informations d'identification sont utilisées pour lire ou écrire des données (pas les deux) et les batteries de serveurs SharePoint Online ne reçoivent pas les autorisations d'énumération.

> [!NOTE]
> Pour les clients du gouvernement des États-Unis Office 365, les blobs de données sont stockés dans le stockage du gouvernement américain Azure. En outre, l'accès aux clés SharePoint Online dans Office 365 le gouvernement américain est limité à Office 365 personnel qui a été spécifiquement filtré. Le personnel des opérations du gouvernement américain d'Azure n'a pas accès au magasin de clés SharePoint Online utilisé pour chiffrer les blobs de données.

Pour plus d'informations sur le chiffrement des données dans SharePoint Online et OneDrive entreprise, voir [chiffrement des données dans Onedrive entreprise et SharePoint Online](https://technet.microsoft.com/en-us/library/dn905447.aspx).

### <a name="list-items-in-sharepoint-online"></a>Éléments de liste dans SharePoint Online

Les éléments de liste sont des plus petits blocs de données client qui sont créés ou qui peuvent vivre plus dynamiquement au sein d'un site, comme les lignes d'une liste créée par l'utilisateur, les publications individuelles dans un blog SharePoint Online ou les entrées d'une page wiki SharePoint Online. Les éléments de liste sont stockés dans la base de données de contenu (base de données SQL Azure) et protégés par TDE.

## <a name="encryption-of-data-in-transit"></a>Chiffrement des données lors de leur transport

Dans OneDrive Entreprise et SharePoint Online, il existe deux scénarios dans lesquels les données entrent et sortent des centres de données.

- **Communication client avec le serveur** : la communication vers OneDrive entreprise sur Internet utilise des connexions SSL/TLS. Toutes les connexions SSL sont établies à l’aide de clés 2 048 bits.
- **Déplacement de données entre centres de données** : la principale raison de déplacer des données entre centres de données est la réplication géo pour activer la récupération d'urgence. Par exemple, les deltas de stockage d'objets blob et les journaux de transaction SQL Server transitent par ce canal. Alors que ces données sont déjà transmises par le biais d'un réseau privé, elles sont encore mieux protégées à l'aide du meilleur chiffrement de sa catégorie.

## <a name="exchange-online"></a>Exchange Online

Exchange Online utilise BitLocker pour toutes les données de boîte aux lettres, et la configuration BitLocker est décrite dans [BitLocker pour](office-365-bitlocker-and-distributed-key-manager-for-encryption.md)le chiffrement. Le chiffrement au niveau du service chiffre toutes les données de boîte aux lettres au niveau de la boîte aux lettres. 

Outre le chiffrement de service, Office 365 prend en charge la clé client, qui est basée sur le chiffrement de service. La clé client est une option de clé gérée par Microsoft pour le chiffrement de service Exchange Online, qui se trouve également dans la feuille de route de Microsoft. Cette méthode de chiffrement offre une protection accrue non offerte par BitLocker car elle permet de séparer les administrateurs de serveur et les clés de chiffrement nécessaires au déchiffrement des données, et le chiffrement est appliqué directement aux données (dans contraste avec BitLocker, qui applique le chiffrement sur le volume de disque logique) toutes les données client copiées à partir d'un serveur Exchange restent chiffrées.

L'étendue du chiffrement du service Exchange Online est les données client qui sont stockées au repos dans Exchange Online. (Skype entreprise stocke presque tout le contenu généré par l'utilisateur au sein de la boîte aux lettres Exchange Online de l'utilisateur, ce qui hérite de la fonctionnalité de chiffrement de service d'Exchange Online.)
