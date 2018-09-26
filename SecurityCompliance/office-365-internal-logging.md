---
title: Enregistrement interne Office 365 pour l’ingénierie Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: Une explication de journalisation comment interne pour Office 365 ingénierie équipes works.
ms.openlocfilehash: 4cade759fb4c095565b4e1f85ce15ed546177082
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038187"
---
# <a name="internal-logging-for-office-365-engineering"></a>Journalisation interne pour Office 365 Engineering
Outre les événements et les données du journal disponibles pour les clients, il existe également un système de collection de données de journal interne qui est disponible pour les ingénieurs d’Office 365. Différents types de données du journal sont téléchargés à partir des serveurs Office 365 à des données internes, big informatique service appelé Cosmos. Chaque équipe service télécharge les journaux d’audit à partir de leurs serveurs respectifs dans la base de données Cosmos d’agrégation et d’analyse. Ce transfert de données se produit via une connexion TLS FIPS 140-2-validé sur spécifiquement approuvées ports et protocoles à l’aide d’un outil d’automatisation propriétaire appelé le chargeur de données Office (ODL). Les outils utilisés dans Office 365 pour collecter et traiter les enregistrements d’audit ne pas autorisent définitive ou contenu d’enregistrement ou la commande de l’heure d’audit de modifications irréversibles d’origine.

Les équipes du service utilisent Cosmos comme un référentiel centralisé pour effectuer une analyse de l’utilisation d’applications, à mesurer les performances du système et opérationnelles et rechercher les anomalies et les modèles qui peuvent indiquer des problèmes de sécurité. Chaque équipe service télécharge une ligne de base des journaux dans Cosmos, selon qu’ils cherchent à analyser, qui comportent généralement :
- Journaux des événements
- Journaux AppLocker
- Données de performances
- Données de System Center
- Enregistrements des détails des appels
- Qualité de l’expérience de données
- Journaux de serveur Web IIS
- Journaux SQL Server
- Données du journal système
- Journaux d’audit de sécurité

Avant le téléchargement de données dans Cosmos, l’application ODL utilise un service de nettoyage pour masquer tous les champs qui contiennent des données du client, telles que les informations de client et les informations d’identification pour l’utilisateur final et de remplacer les champs avec une valeur de hachage. Les journaux rendues et hachage sont réécrites et chargé dans Cosmos. Les équipes du service exécuter des requêtes sur lesquelles porte sur leurs données dans Cosmos corrélation, alertes et des rapports. La période de rétention des données journal d’audit dans Cosmos est déterminée par les équipes de service ; la plupart des données du journal d’audit sont conservées pendant 90 jours ou plus pour prendre en charge des enquêtes incident de sécurité et pour répondre aux exigences réglementaires de rétention.

Accès aux données d’Office 365 stockées dans Cosmos est limité aux personnes autorisées. Microsoft limite la gestion des fonctionnalités d’audit pour le sous-ensemble limité de membres de l’équipe service qui sont chargés de la fonctionnalité d’audit. Ces membres de l’équipe n’ont pas la possibilité de modifier ou supprimer des données dans Cosmos, et toutes les modifications apportées à des mécanismes d’enregistrement pour Cosmos sont enregistrées et auditées.

Chaque équipe service accède à ses données du journal d’analyse en autorisant certaines applications d’effectuer des analyses spécifiques. Par exemple, l’équipe de sécurité pour Microsoft Office 365 utilise des données à partir de Cosmos via un analyseur du journal des événements propriétaires pour mettre en corrélation, alerte et générer des rapports exploitables sur suspect possible dans l’environnement de production d’Office 365. Les rapports à partir de ces données sont utilisés pour corriger les vulnérabilités et pour améliorer les performances globales du service. Si un rapport ou une alerte spécifique requiert des investigations, le personnel de service peut demander que les données importées dans le service Office 365. Depuis le journal à importer à partir de Cosmos est dans chiffré et le personnel de service n’ont pas accès aux clés de déchiffrement, le journal de la cible est transmis par programme via un service de déchiffrement qui retourne les résultats sur lesquelles porte l’autorisé du personnel de service. Toutes les vulnérabilités de cet exercice sont signalées et transmis à l’aide des canaux de gestion des incidents de sécurité standard de Microsoft.
