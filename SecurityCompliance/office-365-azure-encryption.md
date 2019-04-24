---
title: Chiffrement Office 365 dans Azure
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
description: 'Résumé: explication du chiffrement dans Azure.'
ms.openlocfilehash: b8980b3979ada9ac02232065a27a7891936aa945
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32265876"
---
# <a name="office-365-encryption-in-azure"></a>Chiffrement Office 365 dans Azure

## <a name="introduction"></a>Introduction

Les protections technologiques d'Azure, telles que les communications chiffrées et les processus opérationnels, vous aident à sécuriser vos données. Vous avez également la possibilité d'implémenter des fonctionnalités de chiffrement supplémentaires et de gérer vos propres clés de chiffrement. Quelle que soit la configuration du client, Microsoft applique le chiffrement pour protéger les données client dans Azure. Microsoft vous permet également de contrôler vos données hébergées dans Azure via un éventail de technologies avancées pour chiffrer, contrôler et gérer les clés de chiffrement, contrôler et auditer l'accès aux données. De plus, le stockage Azure fournit un ensemble complet de fonctionnalités de sécurité qui, ensemble, permettent aux développeurs de créer des applications sécurisées.

Azure offre de nombreux mécanismes de protection des données lors de leur déplacement d'un emplacement à un autre. Microsoft utilise le protocole TLS pour protéger les données lorsqu'il est en déplacement entre les services Cloud et les clients. Les centres de services de Microsoft négocient une connexion TLS avec les systèmes clients qui se connectent à Azure services. PFS (Perfect Forward Secrecy) protège les connexions entre les systèmes clients des clients et les services Cloud de Microsoft par des clés uniques. Les connexions utilisent également des longueurs de clés de chiffrement 2 048 bits basées sur RSA. Cette combinaison complique l'interception et l'accès aux données en transit.

Les données peuvent être sécurisées en transit entre une application et Azure à l'aide du [chiffrement côté client](https://docs.microsoft.com/azure/storage/storage-client-side-encryption), HTTPS ou SMB 3,0. Vous pouvez activer le chiffrement pour le trafic entre vos machines virtuelles et vos utilisateurs. Avec les [réseaux virtuels Azure](https://azure.microsoft.com/services/virtual-network/), vous pouvez utiliser le protocole IPSec standard pour chiffrer le trafic entre votre passerelle VPN d'entreprise et Azure, ainsi qu'entre les machines virtuelles situées sur votre réseau virtuel.

Pour les données au repos, Azure propose de nombreuses options de chiffrement, telles que la prise en charge d'AES-256, ce qui vous permet de choisir le scénario de stockage de données qui répond le mieux à vos besoins. Les données peuvent être chiffrées automatiquement lors de l'écriture dans le stockage Azure à l'aide du chiffrement de [service de stockage](https://docs.microsoft.com/azure/storage/storage-service-encryption), et les disques de système d'exploitation et de données utilisés par les machines virtuelles peuvent être chiffrés à l'aide du [chiffrement](https://docs.microsoft.com/azure/security/azure-security-disk-encryption)de De plus, l'accès délégué aux objets de données dans Azure Storage peut être accordé à l'aide de [signatures d'accès partagées](https://docs.microsoft.com/azure/storage/storage-dotnet-shared-access-signature-part-1). Azure fournit également le chiffrement des données au repos à l'aide du [chiffreMent transparent des données pour Azure SQL Database et Data Warehouse](https://docs.microsoft.com/sql/relational-databases/security/encryption/transparent-data-encryption-azure-sql).

Pour plus d'informations sur le chiffrement dans Azure, reportez-vous à Azure Encryption [Overview](https://docs.microsoft.com/azure/security/security-azure-encryption-overview) and [Azure Data Encryption-at-Rest](https://docs.microsoft.com/azure/security/azure-security-encryption-atrest).

## <a name="azure-disk-encryption"></a>Chiffrement de disque Azure

Le chiffrement de [disque Azure](https://docs.microsoft.com/azure/security/azure-security-disk-encryption) vous permet de chiffrer vos disques VM de l'infrastructure Windows et Linux en tant que service (IaaS). Le chiffrement de disque Azure exploite la fonctionnalité BitLocker de Windows et la fonctionnalité de chiffrement de chiffrement de Linux pour fournir un chiffrement au niveau du volume pour le système d'exploitation et les disques de données. Elle garantit également que toutes les données des disques VM sont chiffrées au repos dans votre espace de stockage Azure. Le chiffrement de disque Azure est intégré à Azure Key Vault pour vous aider à contrôler, gérer et auditer l'utilisation des clés de chiffrement et des secrets.

Pour plus d'informations, consultez la rubrique [Azure Disk Encryption for Windows and Linux IaaS VM](https://docs.microsoft.com/azure/security/azure-security-disk-encryption).

## <a name="azure-storage-service-encryption"></a>Chiffrement du service de stockage Azure

Avec le [chiffreMent Azure Storage Service](https://docs.microsoft.com/azure/storage/storage-service-encryption), le stockage Azure chiffre automatiquement les données avant de les conserver dans le stockage et de déchiffrer les données avant de les récupérer. Les processus de chiffrement, de déchiffrement et de gestion de clés sont totalement transparents pour les utilisateurs. Le chiffrement du service de stockage Azure peut être utilisé pour le [stockage BLOB Azure](https://azure.microsoft.com/services/storage/blobs/) et les [fichiers Azure](https://azure.microsoft.com/services/storage/files/). Vous pouvez également utiliser des clés de chiffrement gérées par Microsoft avec le chiffrement du service de stockage Azure, ou vous pouvez utiliser vos propres clés de chiffrement. (Pour plus d'informations sur l'utilisation de vos propres clés, consultez la rubrique [Storage Service Encryption using Customer Managed Keys in Azure Key Vault](https://docs.microsoft.com/azure/storage/common/storage-service-encryption-customer-managed-keys). Pour plus d'informations sur l'utilisation des clés gérées par Microsoft, consultez la rubrique [Storage Service Encryption for Data on Rest](https://docs.microsoft.com/azure/storage/storage-service-encryption). En outre, vous pouvez automatiser l'utilisation du chiffrement. Par exemple, vous pouvez activer ou désactiver par programme le chiffrement de service de stockage sur un compte de stockage à l'aide de l' [API REST du fournisseur](https://msdn.microsoft.com/library/azure/mt163683.aspx)de ressources de stockage Azure, la [bibliothèque cliente du fournisseur de ressources de stockage pour .net](https://msdn.microsoft.com/library/azure/mt131037.aspx), [Azure PowerShell](https://docs.microsoft.com/powershell/azureps-cmdlets-docs)ou l' [interface de commande (CLI) Azure](https://docs.microsoft.com/azure/storage/storage-azure-cli).

Certains services Office 365 utilisent Azure pour stocker des données. Par exemple, les données SharePoint Online et OneDrive entreprise Store dans le stockage BLOB Azure, et Microsoft teams stocke les données pour le service de conversation dans des tables, des objets BLOB et des files d'attente. En outre, la fonctionnalité gestionnaire de conformité du portail d'approbation de service stocke les données entrées par le client qui sont stockées sous forme chiffrée dans [Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/database-encryption-at-rest), une base de données PaaS (plateforme As a service), distribuée globalement et multi-modèles. Le chiffrement du service de stockage Azure chiffre les données stockées dans le stockage BLOB Azure et dans les tables, et le chiffrement de disque Azure chiffre les données dans les files d'attente, ainsi que les disques des machines virtuelles Windows et IaaS pour fournir un chiffrement de volume pour le système d'exploitation et le disque de données. La solution garantit que toutes les données sur les disques des machines virtuelles sont chiffrées au repos dans votre espace de stockage Azure. Le [chiffrement au repos dans Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/database-encryption-at-rest) est implémenté à l'aide de plusieurs technologies de sécurité, notamment les systèmes de stockage de clés sécurisés, les réseaux chiffrés et les API de chiffrement.

## <a name="azure-key-vault"></a>Azure Key Vault

La gestion des clés de sécurité n'est pas simplement essentielle aux meilleures pratiques de chiffrement; elle est également essentielle pour la protection des données dans le Cloud. Le [coffre-fort de clés Azure](https://docs.microsoft.com/azure/key-vault/key-vault-whatis) vous permet de chiffrer des clés et des petits secrets comme les mots de passe qui utilisent des clés stockées dans des modules de sécurité matérielle (HSM). Le coffre-fort de clés Azure est la solution recommandée par Microsoft pour la gestion et le contrôle de l'accès aux clés de chiffrement utilisées par les services Cloud. Les autorisations d'accès aux clés peuvent être attribuées à des services ou aux utilisateurs avec des comptes Azure Active Directory. Le coffre-fort de clés Azure soulage les organisations du besoin de configurer, de corriger et de gérer les modules HSM et les logiciels de gestion de clés. Avec Azure Key Vault, Microsoft ne voit jamais vos clés et applications n'y ont pas accès directement; vous conservez le contrôle. Vous pouvez également importer ou générer des clés dans des HSM. Les organisations disposant d'un abonnement qui inclut Azure information protection peuvent configurer leur client Azure information protection de sorte qu'il utilise une clé gérée par le client, [Mettez votre propre clé](https://docs.microsoft.com/information-protection/plan-design/byok-price-restrictions) (BYOK)) et consignez [son utilisation](https://docs.microsoft.com/information-protection/deploy-use/log-analyze-usage).
