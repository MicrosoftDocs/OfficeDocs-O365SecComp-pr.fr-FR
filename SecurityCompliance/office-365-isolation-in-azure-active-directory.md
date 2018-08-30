---
title: Isolation d’Office 365 et de contrôle d’accès dans Azure Active Directory
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
description: 'Résumé : Comment l’Isolation et contrôle d’accès fonctionnent dans Azure Active Directory.'
ms.openlocfilehash: db4fa0d026c6c608f09252c65bf1e0de5354f68c
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528630"
---
# <a name="isolation-and-access-control-in-azure-active-directory"></a>Isolation et au contrôle d’accès dans Azure Active Directory

Azure Active Directory a été conçu pour héberger plusieurs clients d’une manière hautement sécurisée via l’isolation logique des données. Accès à Azure Active Directory est contrôlé par un niveau d’autorisation. Azure Active Directory isole les clients qui utilisent des conteneurs client comme limites de sécurité pour protéger le contenu d’un client afin que le contenu ne peut pas être accessible ou compromis par des clients. Trois contrôles sont effectuées par couche d’autorisation Azure d’Active Directory :
- Le principal est activé pour l’accès au client d’Azure Active Directory ?
- Le principal est activé pour l’accès aux données dans ce client ?
- Est le rôle de l’entité de sécurité dans ce client autorisé pour le type d’accès aux données demandées ?

Aucune application, un utilisateur, un serveur ou un service ne peut accéder Azure Active Directory sans authentification correcte et le jeton ou un certificat. Si elles ne sont pas accompagnés d’informations d’identification appropriées, les demandes sont rejetées.

En effet, Azure Active Directory héberge chaque client dans son propre conteneur protégé, des stratégies et des autorisations pour et dans le conteneur uniquement appartenant à et gérés par le client.
 
![Conteneur Azure](media/office-365-isolation-azure-container.png)

Le concept de conteneurs client est profondément principal dans le service d’annuaire à tous les calques, de portails vers un stockage persistant. Même si plusieurs Azure Active Directory client métadonnées sont stockée sur le même disque physique, il n’existe pas de relation entre les conteneurs autre que ce qui est défini par le service d’annuaire, qui à son tour est déterminé par l’administrateur de clients. Il ne peut y avoir aucune connexion directe vers un stockage Azure Active Directory à partir d’une application ou un service sans sur le premier point par le biais de la couche d’autorisation émet.

Dans l’exemple ci-dessous, Contoso et Fabrikam ont conteneurs distincts, dédiés, et même si ces conteneurs peuvent partager la même infrastructure sous-jacente, tels que des serveurs et du stockage, ils restent distincts et isolées et contrôlé par couches de contrôle d’accès et d’autorisation.
 
![Conteneurs dédiés Azure](media/office-365-isolation-azure-dedicated-containers.png)

En outre, aucun composant d’application qui peut s’exécuter à partir Azure Active Directory, et il n’est pas possible pour un client force violation de l’intégrité d’un autre client, pour accéder à des clés de chiffrement d’un autre client ou lire des données brutes à partir du serveur.

Par défaut, Azure Active Directory interdit toutes les opérations émises par des identités dans d’autres clients. Chaque client est logiquement isolé dans Azure Active Directory par le biais de contrôles d’accès basée sur les revendications. Lectures et écritures de répertoire de données sont étendues aux conteneurs client et contrôlées par une couche d’abstraction interne et un calque accès basé sur un rôle (RBAC), qui ensemble appliquer le client en tant que la limite de sécurité. Chaque demande d’accès annuaire données est traitée par ces couches et chaque demande d’accès dans Office 365 est policed par la logique ci-dessus.

Azure Active Directory contient des partitions en Amérique du Nord, américaine, Union européenne, en Allemagne et dans le monde. Il existe un client dans une seule partition et partitions peuvent contenir plusieurs clients. Informations de partition sont retirées par les utilisateurs. Une partition donnée (y compris tous les clients qu’il contient) est répliquée dans plusieurs centres de données. La partition pour un client est choisie en fonction des propriétés du client (par exemple, l’indicatif du pays). Des clés secrètes et autres informations sensibles dans chaque partition est chiffré avec une clé dédiée. Les clés sont générés automatiquement lors de la création d’une nouvelle partition.

Fonctionnalités de système Azure Active Directory sont une instance unique de chaque session de l’utilisateur. En outre, Azure Active Directory utilise des technologies de chiffrement pour assurer l’isolation des ressources système partagées au niveau du réseau pour empêcher le transfert non autorisé et involontaire d’informations.
