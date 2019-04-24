---
title: Office 365 isolation et contrôle d'accès dans Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: "Résumé: explication de l'isolation et du contrôle d'accès dans les différentes applications d'Office 365."
ms.openlocfilehash: c4328539f8cca5cb7e76c4a3175cfab0a01b42cf
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262620"
---
# <a name="isolation-and-access-control-in-office-365"></a>Isolation et contrôle d’accès dans Office 365

Azure Active Directory et Office 365 utilisez un modèle de données hautement complexe qui inclut des dizaines de services, des centaines d'entités, des milliers de relations et des dizaines de milliers d'attributs (les entités, les relations et les attributs sont souvent spécifiques aux applications). À un niveau élevé, Azure Active Directory et les annuaires de services sont les conteneurs de clients et de destinataires, et ils sont maintenus synchronisés à l'aide de protocoles de réplication basée sur l'État. En plus des informations d'annuaire stockées dans Azure Active Directory, chacun des services a également leur propre infrastructure de services d'annuaire (par exemple, les services d'annuaire Exchange Online, les services d'annuaire SharePoint Online, etc.). 
 
![Synchronisation des données client Office 365](media/office-365-isolation-tenant-data-sync.png)

Dans ce modèle, il n'existe pas de source unique de données d'annuaire. Chaque élément de données individuel appartient à un système spécifique, mais aucun système ne contient toutes les données. Les services Office 365 collaborent avec Azure Active Directory pour réaliser le modèle de données. Azure Active Directory est le «système de vérité» pour les données partagées, généralement réduit et des données statiques utilisées souvent par chaque service. Le modèle fédéré utilisé dans Office 365 et Azure Active Directory fournit la vue partagée des données.

Office 365 utilise à la fois le stockage physique et le stockage cloud Azure. Exchange Online (y compris Exchange Online Protection) et Skype entreprise utilisent leur propre espace de stockage pour les données client. SharePoint Online tire parti de son stockage SQL Server et de son stockage Azure, ce qui nécessite de disposer d'une isolation supplémentaire des données client au niveau du stockage.

## <a name="exchange-online"></a>Exchange Online
Exchange Online stocke les données client dans les boîtes aux lettres qui sont hébergées dans des bases de données ESE (Extensible Storage Engine) appelées bases de données de boîtes aux lettres. Cela inclut les boîtes aux lettres utilisateur, les boîtes aux lettres liées, les boîtes aux lettres partagées et les boîtes aux lettres de dossiers publics. Les boîtes aux lettres utilisateur peuvent également inclure du contenu Skype entreprise enregistré, tel que des historiques des conversations. Le contenu des boîtes aux lettres utilisateur inclut des courriers électroniques et des pièces jointes, des informations de calendrier et de disponibilité, des contacts, des tâches, des notes, des groupes et des données d'inférence.

Chaque base de données de boîtes aux lettres dans Exchange Online contient des boîtes aux lettres de plusieurs clients. Toutes les boîtes aux lettres sont sécurisées par le code d'autorisation, y compris au sein d'un client. Comme avec un déploiement local d'Exchange, seul l'utilisateur affecté a accès à une boîte aux lettres par défaut. La liste de contrôle d'accès (ACL) qui sécurise une boîte aux lettres contient une identité authentifiée par Azure Active Directory au niveau du client. Les boîtes aux lettres d'un client donné sont limitées aux identités authentifiées par rapport au fournisseur d'authentification de ce client, qui inclut uniquement les utilisateurs de ce client. Le contenu de Locatairea ne peut pas être obtenu par les utilisateurs dans TenantB, sauf s'il est explicitement approuvé par Locatairea.

## <a name="skype-for-business"></a>Skype Entreprise
Skype entreprise stocke les données à différents endroits:
- Les informations d'utilisateur et de compte, qui incluent les points de terminaison de connexion, les ID de client, les plans de numérotation, les paramètres d'itinérance, l'état de présence, les listes de contacts, etc., sont stockées dans les serveurs Skype entreprise Active Directory, ainsi que dans différentes bases de données Skype entreprise serveurs. Les listes de contacts sont stockées dans la boîte aux lettres Exchange Online de l'utilisateur si l'utilisateur est activé pour les deux produits ou sur les serveurs Skype entreprise si l'utilisateur ne l'est pas. Les serveurs de base de données Skype entreprise ne sont pas partitionnés par client, mais l'isolation mutualisée des données est appliquée via RBAC.
- Le contenu de la réunion, tel que le contenu que les utilisateurs téléchargent pendant les réunions Skype entreprise, est stocké sur des partages de système de fichiers distribués. Ce contenu peut également être archivé dans Exchange Online, étant donné que l'archivage est activé. Les partages DFS ne sont pas partitionnés par client, mais le contenu est sécurisé avec des ACL et l'architecture mutualisée est appliquée via RBAC.
- Les enregistrements des détails des appels, qui correspondent à l'historique des activités, comme l'historique des appels, les sessions de messagerie instantanée, le partage d'application, l'historique de la messagerie instantanée, peuvent également être stockés dans Exchange Online, mais la plupart des enregistrements des détails des appels sont stockés temporairement sur les serveurs d'enregistrement des détails des appels. Le contenu n'est pas partitionné par client, mais l'architecture mutualisée est appliquée via RBAC.

## <a name="sharepoint-online"></a>SharePoint Online
Il existe plusieurs mécanismes indépendants propres à SharePoint Online qui permettent d'isoler les données. SharePoint Online stocke les objets en tant que code abstrait dans les bases de données d'application. Par exemple, lorsqu'un utilisateur télécharge un fichier vers SharePoint Online, ce fichier est décomposé et converti en code d'application et stocké dans plusieurs tables sur plusieurs bases de données.

Si un utilisateur peut accéder directement au stockage qui contient les données, le contenu ne peut pas être interprété comme une personne ou un système autre que SharePoint Online. Ces mécanismes incluent le contrôle d'accès de sécurité et les propriétés. Comme indiqué ci-dessus, toutes les ressources SharePoint Online sont sécurisées par le code d'autorisation et la stratégie RBAC, y compris au sein d'un client. La liste de contrôle d'accès (ACL) qui sécurise une ressource contient une identité authentifiée au niveau du client. Comme avec Exchange Online, dans SharePoint Online, les données d'un client donné sont limitées aux identités authentifiées par rapport au fournisseur d'authentification de ce client, qui incluent uniquement les utilisateurs de ce client.

En plus des ACL, une propriété de niveau client qui spécifie le fournisseur d'authentification (qui est l'Azure Active Directory propre au client), est écrite une seule fois et ne peut pas être modifiée. Une fois que la propriété client du fournisseur d'authentification a été définie pour un client, elle ne peut plus être modifiée à l'aide de n'importe quelle API exposée à un client.

Un *SubscriptionId* unique est également utilisé pour chaque client. Tous les sites de client appartiennent à un client et un *SubscriptionId* unique est affecté au client. La propriété *SubscriptionId* sur un site est écrite une seule fois et ne peut pas être modifiée. Une fois qu'un site est affecté à un client, il ne peut pas être déplacé vers un autre client ultérieurement à l'aide de l'API de magasin de contenu. Le *SubscriptionId* est également la clé qui est utilisée pour créer l'étendue de sécurité pour le fournisseur d'authentification et est liée au client.

SharePoint Online utilise SQL Server et le stockage Azure pour le stockage du contenu. Au niveau SQL, la clé de partition pour le magasin de contenu est *siteid*. Lors de l'exécution d'une requête SQL, SharePoint Online utilise un *siteid* qui a été vérifié dans le cadre d'une vérification *SubscriptionId* au niveau du client.

SharePoint Online stocke les objets BLOB binaires de fichiers (par exemple, les flux de fichiers) dans Microsoft Azure. Chaque batterie de serveurs SharePoint Online dispose de son propre compte Microsoft Azure et tous les objets BLOB enregistrés dans Azure sont chiffrés individuellement à l'aide d'une clé stockée dans le magasin de contenu SQL. La clé de chiffrement n'est pas exposée directement à l'utilisateur final et est protégée dans le code par la couche d'autorisation. Enfin, SharePoint Online dispose d'une surveillance en temps réel pour détecter quand une requête HTTP lit ou écrit des données pour plusieurs clients. Pour ce faire, il effectue le suivi de la *SubscriptionId* de l'identité de la demande par rapport à l' *SubscriptionId* de la ressource en cours d'accès. Une demande accédant à des ressources de plus d'un client ne doit jamais se produire par l'utilisateur final. Toutefois, cela peut se produire pour les demandes de service dans un environnement mutualisée. Par exemple, le robot de recherche extrait les modifications de contenu d'une base de données complète en une seule fois. Cela implique généralement l'interrogation de sites de plusieurs clients dans une seule demande de service, ce qui est nécessaire pour des raisons d'efficacité.
