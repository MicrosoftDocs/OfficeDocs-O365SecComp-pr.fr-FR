---
title: Vue d’ensemble du tableau de bord de sécurité
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/07/2019
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: fe0b9b8f-faa9-44ff-8095-4d1b2f507b74
ms.collection: M365-security-compliance
description: Utilisez le nouveau tableau de bord de sécurité pour Office 365 Threat Protection état, de révision et d’afficher et agir sur les alertes de sécurité.
ms.openlocfilehash: 403c47ed09e9652a66abeafb93be02589c9b1702
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995125"
---
# <a name="security-dashboard"></a>Tableau de bord de sécurité

## <a name="overview"></a>Vue d'ensemble

Le [sécurité &amp; centre de conformité](go-to-the-securitycompliance-center.md) permet à votre organisation gérer la protection des données et conformité. En supposant que vous disposez des autorisations nécessaires, le tableau de bord de sécurité vous permet de consulter votre état de Protection de menace, ainsi que d’afficher et d’agir sur les alertes de sécurité. 
  
Regarder la vidéo pour obtenir une vue d’ensemble, puis lisez cet article pour en savoir plus.
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/3540b1f8-62d2-47fa-a07d-d7ad76f55b0f?autoplay=false]
  
Selon ce que l’abonnement de votre organisation Office 365 comprend le tableau de bord de sécurité comprend plusieurs widgets, telles que Threat Management Summary, Threat Protection état, Global détections de menace hebdomadaire, logiciels malveillants et plus d’informations, comme décrit dans le sections suivantes.
  
Pour afficher le tableau de bord de sécurité, dans le [Office 365 sécurité &amp; centre de conformité](go-to-the-securitycompliance-center.md), accédez à **gestion de menace** \> **tableau de bord**.
  
> [!NOTE]
> Vous devez être un administrateur global d’Office 365, un administrateur de sécurité ou un lecteur de sécurité pour afficher le tableau de bord de sécurité. Certains widgets nécessitent des autorisations supplémentaires à afficher. Pour plus d’informations, voir [des autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md). 
  
## <a name="threat-management-summary"></a>Résumé de la gestion des menaces

Le widget Threat Management Summary indique un coup de œil comment votre organisation a été protégée contre les menaces sur les sept (7) derniers jours.

![Tableau de bord de sécurité - widget Threat Management Summary](media/SecDash-ThreatMgmtSummary.png)

Les informations que vous verrez dans le résumé de la gestion des menaces dépendent de ce que vous abonnement comprend. Le tableau suivant décrit les informations sont incluses pour Office 365 entreprise E3 et Office 365 entreprise E5.


|Office 365 Entreprise E3  |Office 365 Entreprise E5  |
|---------|---------|
|Messages de programmes malveillants bloqués<br/>Messages de phishing bloqués<br>Messages signalés par les utilisateurs<br><br><br><br> |Messages de programmes malveillants bloqués<br>Messages de phishing bloqués<br>Messages signalés par les utilisateurs<br>Logiciels malveillants zéro jour bloqués<br>Hameçonnage avancées détecté<br>URL malveillantes bloqués |

Pour afficher ou accéder le widget Threat Management Summary, vous devez disposer des autorisations pour afficher les rapports de protection contre les menaces avancées. Pour plus d’informations, voir [les autorisations requises pour afficher les rapports DAV ?](view-reports-for-atp.md#what-permissions-are-needed-to-view-the-atp-reports). 

## <a name="threat-protection-status"></a>État de Protection de menace

Le widget Threat Protection état montre l’efficacité de protection de menace avec une vue détaillée des tendances de hameçonnage et les programmes malveillants. 

![Utilisation du widget Threat protection état](media/tpswidget.png)

Les détails dépendent si votre abonnement Office 365 inclut [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EOP) avec ou sans [Contre les menaces avancées Office 365](office-365-atp.md) (DAV).


|Si votre abonnement comprend... |Vous pouvez voir les détails |
|---------|---------|
|EOP mais pas Office 365 DAV     |Messagerie qui a été détecté et bloqué par EOP<br> Voir le [rapport d’état de Protection de menace (EOP)](view-email-security-reports.md#threat-protection-status-report).| |
|Office 365 DAV |Messagerie contenu et malveillant détecté et bloqué par EOP et Office 365 DAV<br>Nombre d’agrégée de messages unique avec du contenu malveillant bloqués par le moteur anti-programme malveillant, [purge automatique heures zéro](zero-hour-auto-purge.md)et fonctionnalités DAV (y compris les [Liens fiables](atp-safe-links.md), les [Pièces jointes sûres](atp-safe-attachments.md)et [DAV anti-hameçonnage](atp-anti-phishing.md)).<br>Voir le [rapport d’état de Protection de menace (DAV)](view-reports-for-atp.md#threat-protection-status-report). | 

Pour afficher ou accéder le widget d’état de Protection de menace, vous devez disposer des autorisations pour afficher les rapports de protection contre les menaces avancées. Pour plus d’informations, voir [les autorisations requises pour afficher les rapports DAV ?](view-reports-for-atp.md#what-permissions-are-needed-to-view-the-atp-reports). 

## <a name="global-weekly-threat-detections"></a>Détections de menaces hebdomadaire globale
 
Le widget globale détections de menace hebdomadaire indique combien les menaces ont été détectés dans les messages électroniques sur les sept (7) derniers jours.

![Utilisation du widget hebdomadaire détections de menace global](media/globalweeklythreatdetections.png)

Les mesures sont calculées comme indiqué dans le tableau suivant :

|Métrique  |Mode de calcul  |
|---------|---------|
|Messages analysés |Nombre de messages électroniques analysés multiplié par le nombre de destinataires |
|Menaces arrêtés  |Nombre de messages identifiés comme contenant des programmes malveillants multiplié par le nombre de destinataires |
|Bloqué par [DAV](office-365-atp.md) |Nombre de messages bloqués par DAV multiplié par le nombre de destinataires |
|Supprimés après la remise |Nombre de messages supprimés par [purge automatique zéro heures](zero-hour-auto-purge.md) multiplié par le nombre de destinataires |

## <a name="malware"></a>Malware : 

Widgets de programmes malveillants afficher plus d’informations sur les types de logiciels malveillants famille et les tendances de programmes malveillants sur les sept (7) derniers jours.

![Famille de types et les tendances de programmes malveillants](media/malwarewidgetatpe5.png)
 
## <a name="insights"></a>Informations

Insights surface non seulement les principaux problèmes, que vous devez consulter, elles incluent également des recommandations et les actions à prendre en compte. 

![Analyses actives](media/smartinsights.png)

Par exemple, vous pouvez voir que les messages électroniques d’hameçonnage sont remis, car certains utilisateurs ont désactivé les options de courrier indésirable. Pour plus d’informations sur le fonctionnement de détails, consultez la rubrique [des rapports et des vues d’ensemble de sécurité Office 365 &amp; centre de conformité](reports-and-insights-in-security-and-compliance.md).
  
## <a name="threat-intelligence"></a>Informations sur les menaces

Si l’abonnement de votre organisation comprend des [fonctionnalités sur les menaces](office-365-ti.md), votre tableau de bord de sécurité comprend une section **Sur les menaces** qui inclut des outils avancés. L’équipe de sécurité de votre organisation permet les informations de cette section comprendre les nouvelles campagnes, d’étudier les menaces et de gérer les incidents. 
  
![Informations sur les menaces permet de comprendre les attaques ciblées vers votre organisation](media/threatintelwidget.png)
  
  
## <a name="trends"></a>Tendances

Au bas du tableau de bord de sécurité est une section **tendances** , qui résume les tendances de flux de messagerie pour votre organisation. Rapports fournissent des informations sur la messagerie classé comme du courrier indésirable, les logiciels malveillants, les tentatives de hameçonnage et messagerie électronique. Cliquez sur une vignette pour afficher des informations plus détaillées dans le rapport. 
  
![La section tendances résume les tendances de flux de messagerie de l’organisation](media/trends.png)
  
Et, si l’abonnement à Office 365 de votre organisation comprend des [fonctionnalités sur les menaces](office-365-ti.md), vous devez également un rapport **récent gestion des alertes** dans cette section qui permet à votre équipe de sécurité afficher et effectuer une action alertes de haute priorité. 

Pour afficher ou accéder le widget d’envoi et réception de courrier électronique, vous devez disposer des autorisations pour afficher les rapports de protection contre les menaces avancées. Pour plus d’informations, voir [les autorisations requises pour afficher les rapports DAV ?](view-reports-for-atp.md#what-permissions-are-needed-to-view-the-atp-reports). 

Pour afficher ou accéder le widget récents gestion des alertes, vous devez disposer des autorisations permettant d’afficher des alertes. Pour plus d’informations, voir [autorisations RBAC requises pour afficher les alertes](alert-policies.md#rbac-permissions-required-to-view-alerts).
  
## <a name="related-topics"></a>Voir aussi

[Afficher les rapports de sécurité de messagerie de la sécurité &amp; centre de conformité](view-email-security-reports.md)
  
[Afficher les rapports de Protection de menace avancées d’Office 365](view-reports-for-atp.md)
  
[Protection avancée contre les menaces dans Office 365](office-365-atp.md)
  
[Intelligence des menaces d’Office 365](office-365-ti.md)
  

