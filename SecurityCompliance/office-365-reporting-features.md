---
title: Fonctionnalités de création de rapports Office 365
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
description: Explication des fonctionnalités dans Office 365.
ms.openlocfilehash: 5a448089de5d517b81551269416c4a6f91599725
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528689"
---
# <a name="office-365-reporting-features"></a>Fonctionnalités de création de rapports Office 365 

## <a name="introduction"></a>Présentation
La fonctionnalité de rapports dans Office 365 offre une série de rapports d’audit pour Azure Active Directory (AD), Exchange Online, gestion des périphériques, supervision et protection contre la perte de données (DLP). Il s’agit différent et distinct dans les rapports d’activité Office 365.

## <a name="office-365-reports-dashboard"></a>Tableau de bord de rapports Office 365
Le tableau de bord des rapports dans l’aperçu du centre d’administration Office 365 affiche les activités d’utilisation dans Office 365. Les administrateurs globaux Office 365, ou un Exchange Online, SharePoint Online ou Skype pour l’administrateur d’entreprise, peut obtenir insight précise de l’utilisation de ce service. Rapports peuvent fournir des informations telles que le nombre d’utilisateurs de consommer un service particulier d’Office 365, le nombre d’utilisateurs qui ont activé Office Professionnel Plus, nombre de messages sont transitant par l’organisation. Les rapports sont disponibles pour les dernière 7, 30, 90 et 180 jours.

Les rapports suivants sont disponibles :
- [Rapport d’activité de courrier électronique](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--Email-activity-1cbe2c00-ca65-4fb9-9663-1bbfa58ebe44)
- [Rapport des activations de Microsoft Office](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--Microsoft-Office-activations-87c24ae2-82e0-4d1e-be01-c3bcc3f18c60)
- [Rapport d’utilisation du Site SharePoint Online](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--SharePoint-site-usage-4ecfb843-e5d5-464d-8bf6-7ed512a9b213)
- [OneDrive pour le rapport d’utilisation entreprise](https://support.office.com/article/Office-365-Reports-in-the-Admin-Center-Preview--OneDrive-for-Business-usage-0de3b312-c4e8-4e4b-a02d-32b2f726a680)
- [Rapport d’activité de Yammer](https://support.office.com/article/View-the-Yammer-Activity-report-in-the-Office-365-admin-center-preview-c7c9f938-5b8e-4d52-b1a2-c7c32cb2312a)
- [Skype pour le rapport des activités](https://docs.microsoft.com/SkypeForBusiness/skype-for-business-online-reporting/activity-report)
- [Skype pour le rapport d’activité Business pair à pair](https://docs.microsoft.com/SkypeForBusiness/skype-for-business-online-reporting/peer-to-peer-activity-report)
- [Skype pour le rapport de l’organisateur de la conférence](https://docs.microsoft.com/SkypeForBusiness/skype-for-business-online-reporting/conference-organizer-activity-report)
- [Skype pour le rapport d’activité entreprise Participant à la conférence](https://docs.microsoft.com/SkypeForBusiness/skype-for-business-online-reporting/conference-participant-activity-report)

Pour plus d’informations, consultez la rubrique [Rapports sur les activités dans le centre d’administration d’Office 365](https://support.office.com/article/activity-reports-in-the-office-365-admin-center-0d6dfb17-8582-4172-a9a9-aed798150263).


## <a name="azure-active-directory-reports"></a>Rapports d’Azure Active Directory
Office 365 utilise Azure AD pour l’authentification et la gestion des identités. Les administrateurs de Office 365 peuvent utiliser les rapports générés par Azure Rechercher tout accès non autorisé à leurs données et de l’activité inhabituelle. Vous pouvez utiliser les rapports d’accès et d’utilisation dans Azure AD visibilité sur l’intégrité et la sécurité du répertoire de votre organisation. Ces informations, un administrateur peut mieux déterminer où des risques de sécurité peut être afin qu’ils peuvent planifier atténuer ces risques.

Azure AD rapports peuvent être exportés vers Microsoft Excel et en corrélation avec d’autres données à partir d’Office 365, tels que les résultats d’une recherche de journal d’audit, pour fournir un aperçu dans access, l’authentification et les activités de niveau application. Les rapports d’utilisation des anomalies et des ressources avancées sont disponibles lorsque Azure AD Premium est activé. Ces rapports visant à améliorer les organisations de position et de l’aide de la sécurité d’une organisation répond à des menaces potentielles en exploitant analytique sur l’utilisation des accès et application de périphérique avancés. Pour plus d’informations, voir [Création de rapports Azure Active Directory](https://docs.microsoft.com/azure/active-directory/reports-monitoring/overview-reports/).

## <a name="exchange-online-audit-reports"></a>Rapports d’Audit en ligne Exchange
Rapports d’audit Exchange Online incluent plus d’informations sur les boîtes aux lettres et les modifications effectuées par les administrateurs au client d’une organisation Exchange Online. Une fois l’audit de boîte aux lettres est activé, vous pouvez utiliser les tâches dans le tableau suivant pour exécuter des rapports et exporter des journaux d’audit Exchange Online.

>**Remarque**: vous devez activer la boîte aux lettres enregistrement d’audit pour chaque boîte aux lettres afin que les événements audités sont enregistrés dans le journal d’audit pour cette boîte aux lettres. Si l’audit de boîte aux lettres de journalisation n’est pas activée pour une boîte aux lettres, les événements pour cette boîte aux lettres ne seront pas enregistrées dans le journal d’audit n’apparaissent pas dans les rapports d’audit de boîte aux lettres. Pour plus d’informations, voir [Activer l’audit de boîte aux lettres](https://support.office.com/article/Enable-mailbox-auditing-in-Office-365-aaca8987-5b62-458b-9882-c28476a66918).

| Tâche | Description |
|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Exécuter un rapport d'accès aux boîtes aux lettres par des non-propriétaires](https://docs.microsoft.com/exchange/security-and-compliance/exchange-auditing-reports/non-owner-mailbox-access-report) | Affiche la liste des boîtes aux lettres qui ont accédé à une personne autre que le propriétaire de la boîte aux lettres. Le rapport contient des informations qui a accédé à la boîte aux lettres, les actions nécessité dans la boîte aux lettres, et si les actions ont réussi. |
| [Exporter les journaux d’audit de boîte aux lettres](https://docs.microsoft.com/exchange/security-and-compliance/exchange-auditing-reports/export-mailbox-audit-logs) | Journaux d’audit de boîte aux lettres contiennent des informations sur l’accès et les actions dans une boîte aux lettres effectuées par un utilisateur autre que le propriétaire de la boîte aux lettres. Les administrateurs peuvent spécifier des boîtes aux lettres avec une plage de dates pour générer des rapports. Les journaux sont exportés dans le XML, joint à un message et envoyés à des utilisateurs spécifiques tels que définis par l’administrateur. |
| [Exécuter un rapport de groupe de rôles d'administrateur](https://docs.microsoft.com/Office365/SecurityCompliance/eop/run-an-administrator-role-group-report-in-eop-eop) | Le groupe de rôles d’administrateur est utilisé pour affecter des privilèges d’administrateur aux utilisateurs. Ces privilèges permettent aux utilisateurs d’effectuer des tâches d’administration telles que la réinitialisation des mots de passe, créer ou modifier des boîtes aux lettres et affecter des privilèges d’administrateur à d’autres utilisateurs. Le rapport de groupe de rôles d’administration affiche les modifications pour les groupes de rôles, y compris l’ajout ou la suppression de membres. |
| [Afficher le journal d’audit d’administration](https://docs.microsoft.com/exchange/security-and-compliance/exchange-auditing-reports/view-administrator-audit-log) | Les listes de rapport d’administration d’audit journal toutes les créent, mettre à jour et supprimer les fonctions exécutées par les administrateurs dans Exchange Online. Les entrées du journal fournissent des informations sur les applets de commande a été exécutée, les paramètres ont été utilisés, qui a exécuté l’applet de commande et les objets qui ont été affectées. |
| [Mise en attente et la recherche de contenu de boîtes aux lettres](https://docs.microsoft.com/exchange/security-and-compliance/in-place-ediscovery/in-place-ediscovery) | Fournit des détails de toute modification apportée à la découverte électronique locale ou les paramètres de blocage sur Place sur les boîtes aux lettres. |
| [Exporter le journal d’audit d’administration](https://docs.microsoft.com/exchange/security-and-compliance/exchange-auditing-reports/search-role-group-changes) | Les enregistrements du journal d’audit d’administration des actions d’administration spécifiques telles que la création, mise à jour et supprimer dans Exchange Online. Les résultats du journal sont exportés au format XML et les administrateurs peuvent choisir d’envoyer ce journal à un ensemble d’utilisateurs. |
| [Exécuter un rapport de suspension pour litige par boîte aux lettres](https://docs.microsoft.com/exchange/security-and-compliance/exchange-auditing-reports/per-mailbox-litigation-hold-report) | Fournit des détails de toute modification apportée aux litiges tenir compte des paramètres de boîtes aux lettres. |
| [Afficher et exporter le journal d'audit de l'administrateur externe](https://docs.microsoft.com/exchange/security-and-compliance/exchange-auditing-reports/view-external-admin-audit-log) | Contient des détails des actions effectuées par les administrateurs externes. Les entrées fournissent des informations sur les applets de commande a été exécuter, les paramètres ont été utilisés et toutes les actions créer, modifient ou supprimer des objets dans Exchange Online. |

## <a name="device-compliance-reports"></a>Rapports de conformité de périphérique
Vous pouvez gérer et sécuriser les périphériques mobiles s’ils étaient connectés à votre organisation Office 365 à l’aide d’Office 365 Mobile Device Management (MDM). Les appareils mobiles tels que les smartphones et tablettes qui servent à accéder aux travail courrier, calendrier, contacts et documents lire une grande partie de s’assurer que les employés sont en mesure d’utiliser à tout moment et depuis n’importe où. Par conséquent, il est essentiel de protéger les informations de votre organisation. Vous pouvez utiliser Office 365 MDM pour définir des règles d’accès et les stratégies de sécurité des appareils et pour réinitialiser les appareils mobiles s’ils sont perdus ou volés.

Rapports de conformité de Mobile Device Manager fournissent une vue d’ensemble des stratégies configurées par une organisation pour sécuriser les périphériques mobiles qui accèdent à des données d’Office 365. Le rapport permet le filtrage des périphériques par état de conformité, des violations signalées, bloqués et combien d’appareils ont été effacée à la suite de stratégies de sécurité. Pour plus d’informations, voir [Vue d’ensemble de gestion des périphériques mobiles pour Office 365](https://support.office.com/article/Overview-of-Mobile-Device-Management-for-Office-365-faa7d8e5-645d-4d59-839c-c8d4c1869e4a).

## <a name="data-loss-prevention"></a>Prévention contre la perte de données
Les stratégies DLP aident à gérer la sécurité et les flux d’informations dans une organisation. Vous pouvez définir des stratégies pour bloquer l’accès au contenu, chiffrer des données ou avertir les utilisateurs de la stratégie et les violations de stratégie à l’aide des conseils de stratégie DLP dans l’application. Rapports DLP indiquent le nombre de faux positifs, de remplacements et correspond à la stratégie et une règle.

Vous pouvez utiliser le centre d’administration Office 365 pour afficher des informations sur le nombre de messages qui sont détectés par vos stratégies DLP dans le graphique ou le format de tableau. Plus précisément, les correspondances de stratégies DLP pour envoi et la réception de courrier et établit une correspondance avec des règles DLP pour les messages entrants et sortants. Vous pouvez également afficher le nombre de correspondances, de remplacements et faux positifs pour chaque stratégie dans les dernières 24 heures à l’aide du centre d’administration Exchange. Toutefois, ces données ne sont pas disponibles sous forme de graphique. Si vous téléchargez un rapport à utiliser dans Excel, vous pouvez afficher encore plus de détails, tels que qui a envoyé le message, le jour, et établit une correspondance avec les stratégies ont été déclenché. Pour plus d’informations, voir [Afficher les rapports sur les détections de stratégie DLP](https://technet.microsoft.com/en-us/library/jj889415(v=exchg.150).aspx).

## <a name="auditing-in-yammer-enterprise"></a>L’audit dans Yammer Enterprise
Yammer Qu'enterprise offre aux administrateurs la possibilité pour exporter les données de l’activité utilisateur à partir de leurs réseaux Yammer via l' [API d’exporter des données d’Yammer](https://support.office.com/article/export-data-from-yammer-enterprise-b303d8f3-007d-4ad4-81f8-54fb1ecfb3f2), ou manuellement via la page d’administration du réseau Yammer. La possibilité d’exporter des journaux est limitée aux administrateurs réseau dans Yammer. (Tous les administrateurs globaux Office 365 sont les administrateurs réseau Yammer.)

Les données suivantes peuvent être exportées :

| Filename | Description |
|----------------------------|-------------------------------------------------------------------------|
| Users.csv | Tous les utilisateurs de nouveau, en attente et suspendus dans le réseau |
| Messages.csv | Tous les messages dans le réseau |
| Files.csv (métadonnées) | Métadonnées telles que le nom de fichier du fichier URL API, ID de l’outil de chargement, téléchargée à, etc.. |
| Files.csv (fichiers d’origine) | Fichier zip des fichiers d’origine qui ont été téléchargés par les utilisateurs dans Yammer |
| Topics.csv | Rubriques créés sur le réseau |
| Pages.csv | Créés par les utilisateurs dans le réseau de pages (notes) |
| Admins.csv | Tous les vérifiés administrateurs sur le réseau |
| Networks.csv | Tous les réseaux externes Yammer |

*Tableau 3 - Yammer réseau fichiers de données disponibles pour l’exportation par les clients*

Données d’entreprise Yammer sont également disponibles via les rapports d’activité Office 365. En outre, Yammer est activement sur l’exposition de journalisation supplémentaires par le biais de l’API d’activité de gestion Office 365 et de la capacité à raison des données à l’aide de Power BI. Voir la [Feuille de route Office](https://fasttrack.microsoft.com/roadmap?filters=yammer) pour plus d’informations sur ces fonctionnalités.
