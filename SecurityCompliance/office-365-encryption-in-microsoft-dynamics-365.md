---
title: Chiffrement Office 365 dans Microsoft Dynamics 365
ms.author: krowley
author: kccross
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 'Résumé: comprendre le chiffrement dans Microsoft Dynamics 365.'
ms.openlocfilehash: faf9df09b8dcd8a76a38671e4f5d5145094eec88
ms.sourcegitcommit: 24659bdb09f49d0ffed180a4b80bbb7c45c2d301
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2019
ms.locfileid: "29664070"
---
# <a name="office-365-encryption-in-microsoft-dynamics-365"></a>Chiffrement Office 365 dans Microsoft Dynamics 365

Microsoft utilise la technologie de chiffrement pour protéger les données client dans Dynamics 365 tout en restant dans une base de données Microsoft et en transit entre les appareils utilisateur et nos centres de données. Les connexions établies entre les clients et les centres de donnés Microsoft sont chiffrées et tous les points de terminaison publics sont sécurisés à l'aide du protocole TLS standard. TLS établit efficacement une connexion de navigateur à serveur améliorée pour garantir la confidentialité et l'intégrité des données entre les ordinateurs de bureau et les centres de données. Une fois que le chiffrement de données est activé, il ne peut pas être désactivé. Pour plus d'informations, consultez la rubrique relative [au chiffreMent des données au niveau du champ](https://msdn.microsoft.com/en-us/library/dn481562.aspx).

Dynamics 365 utilise le chiffrement de niveau cellule Microsoft SQL Server standard pour un ensemble d'attributs d'entité par défaut qui contiennent des informations sensibles, telles que des noms d'utilisateur et des mots de passe de messagerie. Cette fonctionnalité peut aider les organisations à répondre aux exigences de conformité associées à la norme FIPS 140-2. Le chiffrement des données au niveau du champ est particulièrement important dans les scénarios qui exploitent le [routeur de messagerie Microsoft Dynamics CRM](https://technet.microsoft.com/en-us/library/hh699800.aspx), qui doit stocker les noms d'utilisateur et les mots de passe pour permettre l'intégration entre une instance Dynamics 365 et un service de messagerie. 

Toutes les instances de Dynamics 365 utilisent le chiffrement de [données transparent Microsoft SQL Server](https://docs.microsoft.com/sql/relational-databases/security/encryption/transparent-data-encryption?view=sql-server-2017) (TDE) pour effectuer le chiffrement des données en temps réel lors de l'écriture sur le disque (au repos). TDE chiffre les fichiers de données SQL Server, Azure SQL Database et Azure SQL Data Warehouse. Par défaut, Microsoft stocke et gère les clés de chiffrement de base de données pour vos instances de Dynamics 365. (Les clés utilisées par Dynamics 365 pour les finances sont générées par l'API de protection des données .NET Framework.) 

La fonctionnalité gérer les clés du centre d'administration Dynamics 365 permet aux administrateurs de gérer eux-mêmes les clés de chiffrement de base de données associées à des instances de Dynamics 365. (Les clés de chiffrement de base de données auto-gérées sont uniquement disponibles dans la mise à jour de janvier 2017 pour Microsoft Dynamics 365 et peuvent ne pas être mises à disposition pour les versions ultérieures. Pour plus d'informations, consultez [la rubrique gérer les clés de chiffrement pour votre instance Dynamics 365 (en ligne)](https://docs.microsoft.com/dynamics365/customer-engagement/admin/manage-encryption-keys-instance).) La fonctionnalité de gestion des clés prend en charge les fichiers de clés de chiffrement PFX et BYOK, tels que ceux stockés dans un HSM. (Pour plus d'informations sur la génération et le transfert d'une clé protégée par HSM sur Internet, consultez [la rubrique How to Generate and Transfer My protected Keys for Azure Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-hsm-protected-keys).) 

Pour utiliser l'option Télécharger la clé de chiffrement, vous avez besoin à la fois de la clé de chiffrement publique et privée.

La fonctionnalité de gestion des clés simplifie la gestion des clés de chiffrement à l'aide d'Azure Key Vault pour stocker en toute sécurité les clés de chiffrement. Azure Key Vault protège les clés de chiffrement et les secrets utilisés par les applications et les services Cloud. La fonctionnalité de gestion des clés n'exige pas que vous disposiez d'un abonnement Azure Key Vault et, dans la plupart des cas, il n'est pas nécessaire d'accéder aux clés de chiffrement utilisées pour Dynamics 365 dans la chambre forte.
