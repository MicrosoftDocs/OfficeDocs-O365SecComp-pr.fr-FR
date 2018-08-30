---
title: BitLocker Office 365 pour le chiffrement
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
description: 'Résumé : Informations sur BitLocker pour le chiffrement dans le nuage.'
ms.openlocfilehash: 86c6bc9282d7c2b0a7d4e08d4636c8f9c2fa5db8
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528118"
---
# <a name="bitlocker-and-distributed-key-manager-dkm-for-encryption"></a>BitLocker et distribué Gestionnaire de clés (DKM) pour le chiffrement
Serveurs Office 365 utilisent BitLocker pour chiffrer les lecteurs de disque contenant des données au repos au niveau du volume du client. Le chiffrement BitLocker est une fonctionnalité de protection de données qui est intégrée à Windows. BitLocker est une des technologies utilisées pour protéger contre les menaces au cas où l’indisponibilité dans d’autres processus ou les contrôles (par exemple, contrôle d’accès ou de recyclage du matériel) qui peuvent amener à une personne physique accéder sur les disques contenant les données du client. Dans ce cas, BitLocker élimine le risque de vol de données ou l’exposition en raison de disques et les ordinateurs perdus, volés ou mis hors service.

BitLocker est déployé avec le chiffrement 256 bits Standard AES (Advanced Encryption) sur les disques contenant des données du client dans Exchange Online, SharePoint Online et Skype pour les entreprises. Secteurs de disque sont chiffrées avec un clé FVEK Full Volume chiffrement (Key), qui est chiffré avec le Volume clé principale (VMK), qui à son tour est lié au Module (TPM) sur le serveur. La VMK protège directement la FVEK et par conséquent, la protection de la clé VMK devient critique. La figure suivante illustre un exemple de la chaîne de protection de la clé BitLocker pour un serveur donné (dans ce cas, à l’aide d’un serveur Exchange en ligne).

Le tableau suivant décrit la chaîne de protection de la clé BitLocker pour un serveur donné (dans ce cas, un serveur Exchange Online).

| LOGICIEL DE PROTECTION DE CLÉ | GRANULARITÉ | COMMENT GÉNÉRÉ ? | OÙ EST STOCKÉ ? | PROTECTION |
|--------------------------------------------------------------------------------|-------------------------------------------------|----------------|-------------------------|--------------------------------------------------------------------------------------------------|
| Clé AES 256 bits externe | Par serveur | API de BitLocker | TPM ou Secret sécurisé | Zone de sécurité / contrôle d’accès |
|  |  |  | Dans le Registre du serveur de boîtes aux lettres | TPM chiffrée |
| mot de passe numérique à 48 chiffres | Par disque | API de BitLocker | Active Directory | Zone de sécurité / contrôle d’accès |
| Certificat X.509 en tant qu’Agent (récupération de données) également appelé logiciel de protection de clé publique | Environnement (par exemple, Exchange Online pouvant être partagée) | Autorité de certification Microsoft | Système de génération | Aucun utilisateur n’a le mot de passe à la clé privée. Le mot de passe est sous protection physique. |


Gestion des clés BitLocker implique la gestion des clés de récupération qui sont utilisées pour déverrouiller/récupérer des disques chiffrés dans un centre de données Office 365. Office 365 stocke les clés de la forme de base dans un partage sécurisé, accessible uniquement par des personnes qui ont été analysés et approuvés. Les informations d’identification pour les clés sont stockées dans un référentiel sécurisé pour les données de contrôle d’accès (ce que nous appelons un « magasin secret »), qui requiert un haut niveau de l’élévation et la gestion des approbations pour accéder à l’aide d’un outil d’élévation access juste-à-temps.

BitLocker prend en charge les clés qui sont répartis en deux catégories de gestion :
- BitLocker géré clés, qui sont généralement courte et liée à la durée de vie d’une instance de système d’exploitation installée sur un serveur ou sur un disque donné. Ces clés sont supprimées et réinitialisés au cours de la mise en forme de disque ou de réinstallation du serveur.
- Clés de récupération BitLocker, qui sont gérés à l’extérieur de BitLocker mais utilisées pour le déchiffrement du disque. BitLocker utilise les clés de récupération pour le scénario dans lequel un système d’exploitation est réinstallé et données chiffrées disques existent déjà. Clés de récupération sont également utilisés par la disponibilité gérée surveillance sondes dans Exchange Online où un répondeur devrez pour déverrouiller un disque.

Volumes protégés par BitLocker sont chiffrées avec une clé de chiffrement de volume complet, qui à son tour, est chiffrée avec une clé principale de volume. BitLocker utilise des algorithmes compatibles FIPS pour s’assurer que les clés de chiffrement sont jamais stockées ou envoyés sur le réseau en clair. L’implémentation d’Office 365 client-à-rest-de protection des données ne s’écarte pas de l’implémentation de BitLocker par défaut.