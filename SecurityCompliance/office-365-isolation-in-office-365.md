---
title: Isolation d’Office 365 et de contrôle d’accès dans Office 365
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
description: 'Résumé : Une explication de l’isolation et contrôle d’accès dans les différentes applications d’Office 365.'
ms.openlocfilehash: c1989bc546df357740ea963a1a241dfa14557931
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528654"
---
# <a name="isolation-and-access-control-in-office-365"></a>Isolation et au contrôle d’accès dans Office 365

Azure Active Directory et Office 365 utilisent un modèle de données très complexe qui inclut des dizaines de services, des centaines d’entités, des milliers de relations et des dizaines de milliers d’attributs (entités, relations et attributs sont souvent spécifiques à l’application). À un niveau élevé, Azure Active Directory et les répertoires du service sont les conteneurs de destinataires et les clients, et ils sont synchronisés à l’aide des protocoles de réplication basée sur l’état. Outre les informations d’annuaire dans Azure Active Directory, chacun des services ont également leur propres infrastructure de services d’annuaire (par exemple, les Services d’annuaire Exchange Online, SharePoint Online Services d’annuaire, etc.). 
 
![Synchronisation des données client Office 365](media/office-365-isolation-tenant-data-sync.png)

Dans ce modèle, il n’est pas unique de la source de données de l’annuaire. Chaque élément de données appartient à un système spécifique, mais aucun système unique ne conserve toutes les données. Services Office 365 coopèrent avec Azure Active Directory pour réduire le modèle de données. Azure Active Directory est « le système de vérité » pour les données partagées, qui est généralement petites et des données utilisées par chaque service. Le modèle fédéré utilisé dans Office 365 et Azure Active Directory fournit l’affichage des données partagée.

Office 365 utilise le stockage physique et stockage Azure dans le cloud. Exchange Online (notamment Exchange Online Protection) et Skype pour les entreprises utilisent leur propre stockage de données du client. SharePoint Online exploite son stockage SQL Server et le stockage Azure, ce qui nécessite la nécessité d’isolation supplémentaire des données du client au niveau du stockage.

## <a name="exchange-online"></a>Exchange Online
Exchange Online stocke les données client dans les boîtes aux lettres qui sont hébergées dans des bases de données Extensible Storage Engine (ESE) appelées bases de données de boîtes aux lettres. Cela inclut les boîtes aux lettres utilisateur, de boîtes aux lettres liées, boîtes aux lettres partagées et boîtes aux lettres de dossier public. Boîtes aux lettres de l’utilisateur peuvent également inclure enregistrée Skype contenus d’entreprise, telles que des historiques de conversation. Contenu des boîtes aux lettres utilisateur inclut les messages électroniques et les pièces jointes, les informations de calendriers et informations de disponibilité, contacts, tâches, notes, groupes et données inférence.

Chaque base de données de boîtes aux lettres dans Exchange Online contient des boîtes aux lettres à partir de plusieurs clients. Toutes les boîtes aux lettres sont sécurisés par le code d’autorisation, y compris dans une location. Comme avec un déploiement sur site d’Exchange, par défaut uniquement l’utilisateur affecté dispose d’un accès à une boîte aux lettres. La liste de contrôle d’accès (ACL) qui permet de sécuriser une boîte aux lettres contient une identité qui est authentifiée par Azure Active Directory au niveau du client. Les boîtes aux lettres pour un client donné sont limitées à des identités authentifiées par le fournisseur d’authentification de ce client, qui concernent uniquement les utilisateurs de ce client. Contenu de TenantA ne peut pas en aucune manière être obtenu par les utilisateurs de TenantB, sauf si explicitement approuvé par TenantA.

## <a name="skype-for-business"></a>Skype Entreprise
Skype pour les entreprises stocke les données dans différents emplacements :
- Utilisateur et compte plus d’informations, qui inclut des points de terminaison de connexion, client ID, plans de numérotation, itinérance paramètres, statut de présence, listes de contacts, etc., est stocké dans le Skype pour les serveurs d’entreprise Active Directory, ainsi que dans diverses Skype pour la base de données métiers serveurs. Listes de contacts sont stockés dans la boîte aux lettres Exchange Online, l’utilisateur activé pour les deux produits ou sur Skype des serveurs d’entreprise si l’utilisateur n’est pas. Skype pour les serveurs de base de données métiers ne sont pas partitionnées par client, mais mutualisée isolation des données est appliquée via RBAC.
- Contenu de la réunion, telles que les utilisateurs de contenu téléchargent pendant Skype pour les réunions d’entreprise, est stocké sur des partages de système de fichiers distribués. Ce contenu peut également être archivé dans Exchange Online à condition que l’archivage est activé. Les partages DFS ne sont pas partitionnées par client, mais le contenu est sécurisé avec les listes ACL et architecture mutualisée est appliquée via RBAC.
- Des détails des appels, qui correspond à l’historique de l’activité, telles que l’historique des appels, les sessions de messagerie instantanée, partage d’application, l’historique de la messagerie instantanée, etc., peuvent également être stockées dans Exchange Online, mais la plupart des enregistrements des détails des appels sont temporairement stockés dans les serveurs d’appel détail enregistrement (CDR). Le contenu n’est pas partitionné par client, mais l’architecture mutualisée est appliquée via RBAC.

## <a name="sharepoint-online"></a>SharePoint Online
Il existe plusieurs mécanismes indépendants unique à SharePoint Online qui fournissent l’isolation des données. SharePoint Online stocke les objets en tant que code abstrait au sein des bases de données application. Par exemple, lorsqu’un utilisateur télécharge un fichier dans SharePoint Online, ce fichier est dissocié traduit en code d’application et stocké dans plusieurs tableaux sur plusieurs bases de données.

Si un utilisateur peut accéder directement au stockage contenant les données, le contenu ne sera interprétable à une personne ou un autre système que SharePoint Online. Ces mécanismes comprennent les propriétés et contrôle d’accès de sécurité. Comme indiqué ci-dessus, toutes les ressources SharePoint Online sont sécurisés par le code d’autorisation et de la stratégie RBAC, y compris dans une location. La liste de contrôle d’accès (ACL) qui permet de sécuriser une ressource contient une identité qui est authentifiée au niveau du client. Comme avec Exchange Online, dans SharePoint Online, les données pour un client donné sont limitées à des identités authentifiées par le fournisseur d’authentification de ce client, qui concernent uniquement les utilisateurs de ce client.

Outre les listes ACL, une propriété de niveau client qui spécifie le fournisseur d’authentification (qui est propre à un client Azure Active Directory), est écrit une fois et ne peut pas être modifiée une fois défini. Une fois que la propriété client du fournisseur d’authentification a été définie pour un client, elle ne peut pas être modifiée à l’aide des API exposées à un client.

Un unique *SubscriptionId* est également utilisé pour chaque client. Tous les sites des clients sont détenus par un client et qui sont assignés un *SubscriptionId* unique pour le client. La propriété *SubscriptionId* sur un site est écrit une fois et ne peut pas être modifiée. Une fois qu’un site est affecté à un client, elle ne peut pas être déplacée vers un autre client ultérieurement à l’aide de l’API du magasin de contenu. Le *SubscriptionId* est également la clé qui est utilisée pour créer l’étendue de la sécurité pour le fournisseur d’authentification et est liée au client.

SharePoint Online utilise le stockage Azure et SQL Server pour le stockage de contenu. Au niveau du SQL, la clé de partition du magasin de contenu est *SiteId*. Lorsque vous exécutez une requête SQL, SharePoint Online utilise un *ID de site* ayant été vérifiée dans le cadre d’une vérification de *SubscriptionId* au niveau du client.

SharePoint Online stocke les fichiers binaires des objets BLOB (par exemple, les flux de fichier) dans Microsoft Azure. Chaque batterie de serveurs SharePoint Online dispose de son propre compte Microsoft Azure et tous les objets BLOB enregistrés dans Azure sont chiffrés individuellement à l’aide d’une clé qui est stockée dans le magasin de contenu SQL. La clé de chiffrement n’est pas exposée directement à l’utilisateur final et est protégée par la couche d’autorisation dans le code. Enfin, SharePoint Online dispose de la surveillance en temps réel en place pour détecter une demande HTTP lit ou écrit les données de plusieurs clients. Pour cela, suivi du *SubscriptionId* de l’identité de la demande par rapport à la *SubscriptionId* de la ressource en cours d’accès. Une demande de l’accès aux ressources de plusieurs clients doit se produire jamais par l’utilisateur final. Il peut se produire pour les demandes de service dans un environnement de plusieurs client, mais. Par exemple, le robot de recherche extrait les modifications de contenu pour une base de données entière en une seule fois. Cela implique généralement l’interrogation des sites de plusieurs clients dans une demande de service unique, qui est effectuée pour des raisons d’efficacité.
