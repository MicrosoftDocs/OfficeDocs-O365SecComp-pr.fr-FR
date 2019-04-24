---
title: Chiffrement du service Office 365
ms.author: krowley
author: kccross
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 'Résumé: comprendre la résilience des données dans Microsoft Office 365.'
ms.openlocfilehash: 385bb936de2c0cfcb478f0b20d2f7367d5b55ff4
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262386"
---
# <a name="office-365-service-encryption"></a>Chiffrement du service Office 365

En plus de l'utilisation du chiffrement au niveau du volume, Exchange Online, Skype entreprise, SharePoint Online et OneDrive entreprise utilisent également le chiffrement de service pour chiffrer les données client. Le chiffrement de service autorise deux options de gestion clés:
- Microsoft gère toutes les clés de chiffrement. (Cette option est actuellement disponible dans SharePoint Online, OneDrive entreprise et Skype entreprise. Il figure actuellement dans la feuille de route pour Exchange Online.)
- Le client fournit des clés racines utilisées avec le chiffrement de service et le client gère ces clés à l'aide d'Azure Key Vault. Microsoft gère toutes les autres clés. Cette option est appelée clé client et elle est actuellement disponible pour Exchange Online, SharePoint Online et OneDrive entreprise. (Précédemment appelé chiffrement avancé avec BYOK. Consultez la rubrique amélioration de la [transparence et du contrôle pour les clients Office 365](http://blogs.office.com/2015/04/21/enhancing-transparency-and-control-for-office-365-customers/) pour l'annonce d'origine.)

Le chiffrement de service offre plusieurs avantages. Par exemple:
- fournit des fonctionnalités de protection et de gestion des droits en plus de la protection de chiffrement élevée.
- inclut une option de clé de client qui permet aux services mutualisés de fournir une gestion des clés par client.
- permet de séparer les administrateurs du système d'exploitation Windows de l'accès aux données client stockées ou traitées par le système d'exploitation.
- améliore la capacité d'Office 365 à répondre aux exigences des clients qui ont des exigences de conformité concernant le chiffrement.

## <a name="customer-key"></a>Clé client
À l'aide de la clé client, vous pouvez générer vos propres clés de chiffrement à l'aide d'un HSM local ou d'un coffre-fort de clés Azure. Quelle que soit la méthode de génération de la clé, les clients utilisent Azure Key Vault pour contrôler et gérer les clés de chiffrement utilisées par Office 365. Une fois que vos clés sont stockées dans Azure Key Vault, elles peuvent être affectées à des charges de travail telles qu'Exchange Online et SharePoint Online et utilisées comme racine du trousseau utilisé pour chiffrer les données et fichiers de votre boîte aux lettres.
L'un des autres avantages de l'utilisation de la clé client est de contrôler la capacité de Microsoft à traiter les données client. Cette fonctionnalité existe afin qu'un client souhaitant supprimer des données d'Office 365 (par exemple, lorsqu'un client ferme le service avec Microsoft ou supprime une partie des données stockées dans le Cloud) peut le faire et utiliser la clé client comme contrôle technique pour s'assurer que personne , y compris Microsoft, peut accéder aux données ou les traiter. Il s'agit en outre (et un complément) de la fonctionnalité de référentiel sécurisé du client qui permet de contrôler l'accès aux données client par le personnel de Microsoft.

Pour en savoir plus sur la configuration de la clé client pour Office 365 pour Exchange Online, Skype entreprise, SharePoint Online et OneDrive entreprise, reportez-vous à [la rubrique contrôle de vos données dans Office 365 à l'aide de la clé client](https://support.office.com/article/Controlling-your-data-in-Office-365-using-Customer-Key-f2cd475a-e592-46cf-80a3-1bfb0fa17697). Pour plus d'informations, reportez-vous à la rubrique [customEr Key for Office 365 FAQ](https://support.office.com/article/Customer-Key-for-Office-365-FAQ-41ae293a-bd5c-4083-acd8-e1a2b4329da6), ainsi qu'à la rubrique [gérer et contrôler vos données afin de répondre aux besoins de conformité avec la clé client](https://techcommunity.microsoft.com/t5/Microsoft-Ignite-Content-2017/Manage-and-control-your-data-to-help-meet-compliance-needs-with/td-p/117580).
