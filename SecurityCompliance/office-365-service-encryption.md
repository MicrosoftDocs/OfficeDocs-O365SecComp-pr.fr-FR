---
title: Chiffrement du Service Office 365
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
ms.openlocfilehash: 1273cd5556bf51dcdac9bbde1b3e8003ab818811
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528105"
---
# <a name="office-365-service-encryption"></a>Chiffrement du Service Office 365

Outre l’utilisation de chiffrement au niveau du volume, Exchange Online, Skype pour les entreprises, SharePoint Online et OneDrive entreprise également utiliser Service de chiffrement pour chiffrer les données du client. Permet de service de chiffrement pour les deux options de gestion de clés :
- Microsoft gère toutes les clés de chiffrement. (Cette option est actuellement disponible dans SharePoint Online, OneDrive entreprise, Skype pour les entreprises. Il est affiché sur la feuille de route pour Exchange Online.)
- Le client fournit des clés racine utilisés avec le chiffrement de service et le client gère ces clés à l’aide d’Azure clé coffre-fort. Microsoft gère toutes les autres clés. Cette option est appelée clé client, et il n’est actuellement disponible pour Exchange Online, SharePoint Online et OneDrive for Business. (Précédemment appelé cryptage avancé avec BYOK. Voir [l’amélioration transparence et contrôle pour les clients Office 365](http://blogs.office.com/2015/04/21/enhancing-transparency-and-control-for-office-365-customers/) pour l’annonce d’origine).

Chiffrement service fournit plusieurs avantages. Par exemple, il :
- Fournit des fonctionnalités de protection et de gestion en haut de la protection de chiffrement fort par des droits.
- inclut une option de clé de client qui permet aux services de plusieurs clients d’assurer la gestion de clés par client.
- Fournit la séparation des administrateurs de système d’exploitation Windows à partir de l’accès aux données client stockées ou traitées par le système d’exploitation.
- améliore la capacité d’Office 365 pour répondre aux besoins des clients qui ont des exigences de conformité concernant le chiffrement.

## <a name="customer-key"></a>Clé client
À l’aide de la clé client, vous pouvez générer vos propres clés de chiffrement utilisant un HSM locale ou Azure coffre-fort clé. Quelle que soit la façon dont la clé est générée, les clients utilisent Azure clé coffre-fort pour contrôler et de gérer les clés de chiffrement utilisés par Office 365. Une fois vos clés sont stockés dans Azure clé coffre-fort, elles pouvant être affectés à des charges de travail tels que Exchange Online et SharePoint Online et sert à la racine de la chaîne de clé utilisé pour chiffrer vos données de boîtes aux lettres et fichiers. Un des autres avantages de l’utilisation de la clé client consiste à contrôler la capacité de Microsoft pour traiter les données client. Cette fonctionnalité existe afin qu’un client qui souhaite pour supprimer des données à partir d’Office 365 (comme lorsqu’un client termine service auprès de Microsoft ou supprime une partie des données stockées dans le nuage) peut faire et utiliser la clé client comme contrôle technique pour s’assurer que personne , y compris Microsoft, peuvent accéder ou traitent les données. Il s’agit en outre (et un complément) à la fonctionnalité de zone de sécurité client qui peut servir à contrôler l’accès aux données du client par le personnel de Microsoft.

Pour savoir comment configurer la clé client pour Office 365 pour Exchange Online, Skype pour les entreprises, SharePoint Online et OneDrive entreprise, consultez la section [contrôle vos données dans Office 365 à l’aide de la clé client](https://support.office.com/article/Controlling-your-data-in-Office-365-using-Customer-Key-f2cd475a-e592-46cf-80a3-1bfb0fa17697). Pour plus d’informations, voir la [Clé client pour le Forum aux questions sur Office 365](https://support.office.com/article/Customer-Key-for-Office-365-FAQ-41ae293a-bd5c-4083-acd8-e1a2b4329da6)et [gérer et contrôle a besoin de vos données afin de répondre à la conformité avec la clé client](https://techcommunity.microsoft.com/t5/Microsoft-Ignite-Content-2017/Manage-and-control-your-data-to-help-meet-compliance-needs-with/td-p/117580).
