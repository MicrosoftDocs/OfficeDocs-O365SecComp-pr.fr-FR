---
title: Rétention des données, la suppression et Destruction dans Office 365
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
description: Vue d’ensemble des stratégies de Microsoft pour Office 365 concernant la rétention des données, la suppression et destruction.
ms.openlocfilehash: 4d952058df8d0efb664f23e5495796fdb9e006f2
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527861"
---
# <a name="data-retention-deletion-and-destruction-in-office-365"></a>Rétention des données, la suppression et Destruction dans Office 365

## <a name="introduction"></a>Présentation
Microsoft dispose d’une stratégie de gestion de données Standard pour Office 365 qui spécifie la durée de conservation des données client après avoir supprimé. En règle générale, dans Office 365, il existe deux scénarios dans lesquels les données de client sont supprimées :
- **Suppression active** - un utilisateur supprime les données ou les données personnelles d’un utilisateur sont supprimées après que l’utilisateur est supprimé par l’administrateur d’un client actif.
- **Suppression passive** - l’abonnement de client se termine.

Stratégie de gestion de données Standard de Microsoft pour Office 365 spécifie la durée de conservation des données dans chacun de ces scénarios. Les sections suivantes décrivent les catégories de données (en fonction Office 365 biens Classification Standard de Microsoft) et les périodes de rétention pour les scénarios de suppression actives et passives.

## <a name="active-deletion-retention"></a>Rétention de suppression Active

| Catégorie de données | Conserver au moins | Conserver au maximum |
|---------------------------------------|:-----------------:|:-----------------:|:----------------------------------:|:-------------------------------:|
| Données de contrôle d’accès | N/D | S/O |
| Contenu de client | 7 jours | 30 jours |
| Informations d’identification personnelle utilisateur final | 90 jours | 180 jours |
| Données de compte | 1 an | 3 ans |
| Organisation des informations identifiables | 90 jours | 180 jours |
| Métadonnées du système | Afficher les journaux de sécurité | Afficher les journaux de sécurité |
| Journaux de sécurité | Min 1 an | Max 1 an |
| Journaux d’archivage Exchange Online | Min 3 ans | Max 3 ans |

## <a name="passive-deletion-retention"></a>Rétention de suppression passive

| Catégorie de données | Conserver au moins | Conserver au maximum |
|---------------------------------------|:-----------------:|:-----------------:|:----------------------------------:|:-------------------------------:|
| Données de contrôle d’accès | 90 jours (pour la récupération de contenu) | 180 jours (pour la récupération de contenu) |
| Contenu de client | 90 jours (fonctions limitées compte) | 180 jours |
| Informations d’identification personnelle utilisateur final | 90 jours | 180 jours |
| Données de compte | 1 an | 3 ans |
| Organisation des informations identifiables | 90 jours | 180 jours |
| Métadonnées du système | Afficher les journaux de sécurité | Afficher les journaux de sécurité |
| Journaux de sécurité | Min 1 an | Max 1 an |
| Journaux d’archivage Exchange Online | Min 3 ans | Max 3 ans |

## <a name="subscription-rentention"></a>Fixation de l’abonnement

Contenu de client est défini en tant que contenu de boîte aux lettres Exchange Online (corps, des entrées de calendrier et le contenu des pièces jointes de courrier électronique, de messagerie et le cas échéant, Skype contenus d’entreprise), contenu de site SharePoint Online et les fichiers stockés dans des sites et téléchargé vers OneDrive pour les professionnels ou Skype pour les entreprises.

À tout moment pendant la durée d’un abonnement, un abonné peut accéder et extraire les données du client stockées dans Office 365. À l’exception des versions d’évaluation gratuites et services LinkedIn, Microsoft conserve les données stockées dans Office 365 dans un compte de fonctions limitées pendant 90 jours après l’expiration ou la résiliation de l’abonnement pour activer l’abonné extraire les données du client. (Dans le cas d’une version d’évaluation gratuite, lorsque la version d’évaluation arrive à expiration, il se déplace dans une période de grâce, en donnant des 30 derniers jours (pour la plupart des tirages, dans la plupart des pays et régions) d’acheter Office 365. Si vous décidez de ne pas acheter Office 365, vous pouvez laisser votre version d’évaluation expire ou annuler. Après la période de grâce de 30 jours, vos informations de compte d’évaluation et les données sont définitivement effacées.)

Après la fin de la période de rétention de 90 jours, Microsoft désactive le compte et supprime les données du client. Pas plus de 180 jours après expiration ou résiliation d’un abonnement à Office 365, Microsoft désactiver le compte et supprimer toutes les données du client à partir du compte. Une fois la période de rétention maximale pour toutes les données écoulée, les données sont rendues irrécupérables sur le marché.

Microsoft a également une stratégie Standard de gestion des données qui résout le recyclage et l’élimination des disques durs et des serveurs de retraite ou ayant échoués. Avant de réutiliser les disques dans Office 365, Microsoft effectue un processus de nettoyage physique est compatible avec SP NIST 800-88. Les disques ne peut pas être réutilisés à l’aide d’un processus de destruction physique est effectué sur le site dans le centre de données contenant les destruction des disques sont supprimés. Ces procédures sont exécutées par l’Infrastructure de nuage Microsoft & opérations (MCIO). Pour plus d’informations, voir la MCIO des rapports sur le [Service de gestion de la confidentialité aperçu](https://aka.ms/STP)d’audit.

## <a name="expedited-deletion"></a>Suppression prioritaire
À tout moment pendant la durée d’un abonnement, un abonné peut contacter demande EF mise hors service par abonnement et Support de Microsoft. Dans ce processus, toutes les données utilisateur, y compris les données dans SharePoint Online, Exchange Online peut se trouver sous blocage ou stockés dans des boîtes aux lettres inactives, est supprimée de trois jours après l’administrateur entre le code de verrouillage fourni par Microsoft. Pour plus d’informations sur la mise hors service prioritaire, voir [Annuler Office 365](https://support.office.com/article/Cancel-Office-365-for-business-b1bc0bef-4608-4601-813a-cdd9f746709a).

## <a name="related-links"></a>Liens connexes
- [Suppression de données en ligne Exchange](/office365/enterprise/office-365-exchange-online-data-deletion)
- [Suppression des données en ligne de SharePoint](/office365/enterprise/office-365-sharepoint-online-data-deletion)
- [Skype pour la suppression des données métiers](/office365/enterprise/office-365-skype-data-deletion)
- [Immuabilité dans Office 365](/office365/enterprise/office-365-data-immutability)
- [Destruction des données](/office365/enterprise/office-365-data-destruction)