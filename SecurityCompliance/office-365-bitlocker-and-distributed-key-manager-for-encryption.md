---
title: Office 365 BitLocker pour le chiffrement
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
description: 'Résumé: informations sur BitLocker pour le chiffrement dans le Cloud.'
ms.openlocfilehash: 77de478899591be54bdaf7c3ac9e7d591dd418b1
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30212904"
---
# <a name="bitlocker-and-distributed-key-manager-dkm-for-encryption"></a>BitLocker et Distributed Key Manager (DKM) pour le chiffrement
Les serveurs Office 365 utilisent BitLocker pour chiffrer les lecteurs de disque contenant des données client au repos au niveau du volume. Le chiffrement BitLocker est une fonctionnalité de protection des données intégrée à Windows. BitLocker est l'une des technologies utilisées pour se protéger contre les menaces en cas de chute d'autres processus ou contrôles (par exemple, le contrôle d'accès ou le recyclage du matériel) susceptibles d'entraîner l'accès physique à des disques contenant des données client. Dans ce cas, BitLocker élimine le risque de vol ou d'exposition des données en raison d'ordinateurs et de disques perdus, volés ou incorrectement mis en service.

BitLocker est déployé avec le chiffrement AES (Advanced enCryption standard) 256 bits sur des disques contenant des données client dans Exchange Online, SharePoint Online et Skype entreprise. Les secteurs de disque sont chiffrés avec une clé de chiffrement de volume complet (FVEK), qui est chiffrée avec la clé VMK (volume Master Key), qui est à son tour liée au module de plateforme sécurisée (TPM) du serveur. Le VMK protège directement la FVEK et, par conséquent, la protection de la clé VMK devient essentielle. La figure suivante illustre un exemple de la chaîne de protection de clé BitLocker pour un serveur donné (dans ce cas, à l'aide d'un serveur Exchange Online).

Le tableau suivant décrit la chaîne de protection de clé BitLocker pour un serveur donné (dans ce cas, un serveur Exchange Online).

| PROTECTEUR DE CLÉ | GRANULARITÉ | COMMENT EST-ELLE GÉNÉRÉE? | OÙ EST-IL STOCKÉ? | PROTÈGE |
|--------------------------------------------------------------------------------|-------------------------------------------------|----------------|-------------------------|--------------------------------------------------------------------------------------------------|
| Clé externe 256 bits AES | Par serveur | API BitLocker | TPM ou secrets secrets | Lockbox/contrôle d'accès |
|  |  |  | Registre du serveur de boîtes aux lettres | TPM chiffré |
| Mot de passe numérique de 48 chiffres | Par disque | API BitLocker | Active Directory | Lockbox/contrôle d'accès |
| Certificat X. 509 en tant qu'agent de récupération de données (DRA), également appelé protecteur de clé publique | Environnement (par exemple, Exchange Online multiclient) | AUTORITÉ de certification Microsoft | Système de génération | Aucun utilisateur ne dispose du mot de passe complet de la clé privée. Le mot de passe est sous protection physique. |


La gestion de clés BitLocker implique la gestion des clés de récupération utilisées pour déverrouiller/récupérer des disques chiffrés dans un centre de contenu Office 365. Office 365 stocke les clés principales dans un partage sécurisé, uniquement accessible par les personnes qui ont été filtrées et approuvées. Les informations d'identification des clés sont stockées dans un référentiel sécurisé pour les données de contrôle d'accès (ce que nous appelons «Banque secrète»), ce qui nécessite un niveau élevé d'approbation et de gestion pour accéder à l'aide d'un outil d'élévation d'accès juste-à-temps.

BitLocker prend en charge les clés qui se répartissent en deux catégories de gestion:
- Clés gérées par BitLocker, qui sont généralement éphémères et liées à la durée de vie d'une instance de système d'exploitation installée sur un serveur ou sur un disque donné. Ces clés sont supprimées et réinitialisées lors de la réinstallation du serveur ou de la mise en forme du disque.
- Clés de récupération BitLocker, gérées en dehors de BitLocker mais utilisées pour le déchiffrement du disque. BitLocker utilise des clés de récupération pour le scénario dans lequel un système d'exploitation est réinstallé et des disques de données chiffrés existent déjà. Les clés de récupération sont également utilisées par les sondes de surveillance de disponibilité gérée dans Exchange Online, où un répondeur peut avoir besoin de déverrouiller un disque.

Les volumes protégés par BitLocker sont chiffrés à l'aide d'une clé de chiffrement de volume complet, qui est à son tour chiffrée avec une clé principale de volume. BitLocker utilise des algorithmes conformes à FIPS pour s'assurer que les clés de chiffrement ne sont jamais stockées ou envoyées sur le réseau en clair. [! Remarque] l'implémentation Office 365 de la protection des données client-inactive ne s'écarte pas de l'implémentation BitLocker par défaut.