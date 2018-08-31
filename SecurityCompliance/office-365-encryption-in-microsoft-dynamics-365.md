---
title: Chiffrement dans Microsoft Dynamics 365 Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 5/31/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 'Résumé : Découvrez le chiffrement dans Microsoft Dynamics 365.'
ms.openlocfilehash: 181db1724f140c86fb1ac1dbf4a4bfb7063d25a3
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527502"
---
# <a name="office-365-encryption-in-microsoft-dynamics-365"></a>Chiffrement dans Microsoft Dynamics 365 Office 365

Microsoft utilise la technologie de chiffrement pour protéger les données clients dans Dynamics 365 tout en reste dans une base de données Microsoft, et s’il est en transit entre les périphériques de l’utilisateur et de nos centres de données. Les connexions établies entre les clients et les centres de données Microsoft sont chiffrées et tous les points de terminaison publics sont sécurisés à l’aide de la norme TLS. TLS établit efficacement une connexion sécurisée, navigateur et le serveur pour garantir la confidentialité des données et l’intégrité entre les ordinateurs de bureau et des centres de données. Une fois que le chiffrement des données est activé, elle ne peut pas être désactivée. Pour plus d’informations, voir [chiffrement des données au niveau du champ](https://msdn.microsoft.com/en-us/library/dn481562.aspx).

Dynamics 365 utilise le chiffrement au niveau de la cellule Microsoft SQL Server standard pour un ensemble par défaut des attributs d’entités qui contiennent des informations sensibles, telles que les noms d’utilisateur et mots de passe de messagerie. Cette fonctionnalité peut aider les organisations répondent aux exigences de conformité associés avec FIPS 140-2. Chiffrement des données au niveau des champs est particulièrement important dans les scénarios qui tirent parti de [Microsoft Dynamics CRM E-mail Router](https://technet.microsoft.com/en-us/library/hh699800.aspx), qui doit stocker les noms d’utilisateur et les mots de passe pour activer l’intégration entre une instance de Dynamics 365 et un service de messagerie. 

Toutes les instances de Dynamics 365 utilisent [Microsoft SQL Server chiffrement Transparent des données](https://docs.microsoft.com/sql/relational-databases/security/encryption/transparent-data-encryption?view=sql-server-2017) (TDE) pour effectuer le chiffrement des données lors de l’écriture sur le disque (au repos) en temps réel. TDE chiffre les fichiers de données SQL Server, base de données SQL Azure et entrepôt de données SQL Azure. Par défaut, Microsoft stocke et gère les clés de chiffrement de base de données pour vos instances de Dynamics 365. (Les clés qui sont utilisés par Dynamics 365 pour les états financiers générés par l’API de Protection de données .NET Framework.) 

La fonctionnalité Gestion de clés dans le centre d’Administration Dynamics 365 permet aux administrateurs de gérer eux-mêmes les clés de chiffrement de base de données qui sont associés à des instances de Dynamics 365. (Les clés de chiffrement gérés automatiquement de la base de données sont disponibles uniquement dans la mise à jour Microsoft Dynamics 365 2017 janvier et ne peuvent être effectués disponibles pour les versions ultérieures. Pour plus d’informations, voir [Gestion des clés de chiffrement pour votre instance (en ligne) Dynamics 365](https://docs.microsoft.com/dynamics365/customer-engagement/admin/manage-encryption-keys-instance).) La fonctionnalité de gestion de clés prend en charge à la fois PFX et BYOK chiffrement fichiers de clés, telles que celles stockées dans un module HSM. (Pour plus d’informations sur la génération et de transfert d’une clé protégés par HSM sur Internet, voir [comment générer et transférer les clés protégés par HSM pour Azure clé coffre-fort](https://docs.microsoft.com/azure/key-vault/key-vault-hsm-protected-keys)). 

Pour utiliser l’option de clé de chiffrement de téléchargement, vous devez à la fois la clé de chiffrement publiques et privées.

La fonctionnalité de gestion de clés prend la complexité de gestion de clés de chiffrement à l’aide d’Azure clé coffre-fort pour stocker en toute sécurité les clés de chiffrement. Azure clé coffre-fort permet préservent les clés de chiffrement et des clés secrètes utilisés par les services et les applications en nuage. La fonctionnalité de gestion de clés ne nécessite pas que vous disposez d’un abonnement Azure clé coffre-fort et pour la plupart des cas il n’est pas nécessaire pour accéder aux clés de chiffrement utilisés pour Dynamics 365 dans le coffre-fort.