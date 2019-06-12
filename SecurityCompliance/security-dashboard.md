---
title: Vue d’ensemble du tableau de bord de sécurité
ms.author: deniseb
author: denisebmsft
manager: laurawi
audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: fe0b9b8f-faa9-44ff-8095-4d1b2f507b74
ms.collection:
- M365-security-compliance
description: Utilisez le nouveau tableau de bord de sécurité pour consulter l’état de protection contre les menaces d’Office 365, et afficher et agir sur les alertes de sécurité.
ms.openlocfilehash: 78e6a67ace757cca9d25086c601ab4b4437c7bf8
ms.sourcegitcommit: 5a93c2f3df35d06a59a7fbaff5c91f7afde11781
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2019
ms.locfileid: "34857664"
---
# <a name="security-dashboard"></a>Tableau de bord de sécurité

## <a name="overview"></a>Vue d’ensemble

Le [Centre &amp; de sécurité conformité](go-to-the-securitycompliance-center.md) permet à votre organisation de gérer la protection et la conformité des données. En supposant que vous disposez des autorisations nécessaires, le tableau de bord de sécurité vous permet d’examiner votre statut de protection contre les menaces, ainsi que d’afficher et d’agir sur les alertes de sécurité. 
  
Regardez la vidéo pour obtenir une vue d’ensemble, puis lisez cet article pour en savoir plus.
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE1VV3o]
  
En fonction de l’abonnement Office 365 de votre organisation, le tableau de bord de sécurité inclut plusieurs widgets, tels que le résumé de la gestion des menaces, le statut de protection contre les menaces, des détections de menaces globales hebdomadaires, des programmes malveillants, etc., comme décrit dans le sections suivantes.
  
Pour afficher le tableau de bord de sécurité, dans le [Centre de &amp; sécurité conformité Office 365](go-to-the-securitycompliance-center.md), accédez au **tableau de bord**gestion \> des **menaces** .
  
> [!NOTE]
> Vous devez être un administrateur général Office 365, un administrateur de sécurité ou un lecteur de sécurité pour afficher le tableau de bord de sécurité. Certains widgets nécessitent des autorisations supplémentaires pour être visualisées. Pour en savoir plus, consultez [la rubrique autorisations dans le &amp; Centre de sécurité conformité Office 365](permissions-in-the-security-and-compliance-center.md). 
  
## <a name="threat-management-summary"></a>Résumé de la gestion des menaces

Le widget gestion des menaces explique en un clin d’œil comment votre organisation a été protégée contre les menaces au cours des sept (7) derniers jours.

![Tableau de bord de sécurité-widget gestion des menaces-Résumé](media/SecDash-ThreatMgmtSummary.png)

Les informations que vous verrez dans le résumé de gestion des menaces dépendent de ce que comprend l’abonnement. Le tableau suivant décrit les informations incluses pour Office 365 E3 et Office 365 E5.


|Office 365 E3  |Office 365 E5  |
|---------|---------|
|Messages malveillants bloqués<br/>Messages d’hameçonnage bloqués<br>Messages signalés par les utilisateurs<br><br><br><br> |Messages malveillants bloqués<br>Messages d’hameçonnage bloqués<br>Messages signalés par les utilisateurs<br>Blocage des programmes malveillants de jour zéro<br>Messages d’hameçonnage avancés détectés<br>URL malveillantes bloquées |

Pour afficher ou accéder au widget Résumé de la gestion des menaces, vous devez disposer des autorisations permettant d’afficher les rapports de protection avancée contre les menaces. Pour en savoir plus, consultez [la rubrique Quelles autorisations sont requises pour afficher les rapports ATP?](view-reports-for-atp.md#what-permissions-are-needed-to-view-the-atp-reports). 

## <a name="threat-protection-status"></a>Statut de protection contre les menaces

Le widget état de protection contre les menaces indique l’efficacité de la protection contre les menaces avec une vue d’ensemble des tendances et programmes malveillants. 

![Widget d’état de protection contre les menaces](media/tpswidget.png)

Les détails varient selon que votre abonnement Office 365 inclut ou non [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EoP) avec ou sans [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP).


|Si votre abonnement inclut... |Ces détails s’affichent. |
|---------|---------|
|EOP mais pas Office 365 ATP     |Courrier électronique malveillant détecté et bloqué par EOP<br> Consultez la rubrique [Threat Protection Status Report (EoP)](view-email-security-reports.md#threat-protection-status-report).| |
|Office 365 ATP |Contenu malveillant et courrier involontaire détecté et bloqué par EOP et Office 365 ATP<br>Nombre agrégé de messages électroniques uniques dont le contenu malveillant est bloqué par le moteur anti-programme malveillant, la [purge automatique avec suppression automatique des heures d’heure](zero-hour-auto-purge.md)et les fonctionnalités ATP (y compris les [liens fiables](atp-safe-links.md), [les pièces jointes fiables](atp-safe-attachments.md)et l' [anti-hameçonnage ATP](atp-anti-phishing.md)).<br>Consultez la rubrique [Threat Protection Status Report (ATP)](view-reports-for-atp.md#threat-protection-status-report). | 

Pour afficher ou accéder au widget d’État protection contre les menaces, vous devez disposer des autorisations permettant d’afficher les rapports de protection avancée contre les menaces. Pour en savoir plus, consultez [la rubrique Quelles autorisations sont requises pour afficher les rapports ATP?](view-reports-for-atp.md#what-permissions-are-needed-to-view-the-atp-reports). 

## <a name="global-weekly-threat-detections"></a>Détections de menaces hebdomadaires globales
 
Le widget détections de menaces globales hebdomadaires indique le nombre de menaces détectées dans les messages électroniques au cours des sept (7) derniers jours.

![Widget de détections de menaces hebdomadaires globales](media/globalweeklythreatdetections.png)

Les mesures sont calculées de la manière décrite dans le tableau suivant:

|Liées  |Mode de calcul  |
|---------|---------|
|Messages analysés |Nombre de messages électroniques analysés multiplié par le nombre de destinataires |
|Menaces arrêtées  |Nombre de messages électroniques identifiés comme contenant des programmes malveillants multiplié par le nombre de destinataires |
|Bloqué par [](office-365-atp.md) la protection avancée contre les menaces |Nombre de messages électroniques bloqués par la protection avancée contre les menaces multiplié par le nombre de destinataires |
|Supprimés après la remise |Nombre de messages supprimés par [purge automatique 0 heure](zero-hour-auto-purge.md) multiplié par le nombre de destinataires |

## <a name="malware"></a>Programme malveillant

Les widgets de programmes malveillants affichent des informations sur les tendances des programmes malveillants et les types de familles de programmes malveillants au cours des sept derniers jours.

![Tendances des programmes malveillants et types de famille](media/malwarewidgetatpe5.png)
 
## <a name="insights"></a>Informations

Insights non seulement les problèmes de clés de surface que vous devez examiner, ils incluent également des recommandations et des actions à prendre en considération. 

![Informations intelligentes](media/smartinsights.png)

Par exemple, vous pouvez constater que les messages électroniques de hameçonnage sont remis car certains utilisateurs ont désactivé leurs options de courrier indésirable. Pour en savoir plus sur le fonctionnement des informations, voir [rapports et Insights dans le centre de sécurité &amp; conformité Office 365](reports-and-insights-in-security-and-compliance.md).
  
## <a name="threat-investigation-and-response"></a>Examen et réponse contre les menaces

Si l’abonnement de votre organisation comprend [Office 365 Advanced Threat Protection Plan 2](office-365-ti.md), votre tableau de bord de sécurité comporte une section qui inclut des outils d’enquête et de réponse de menace avancés. L’équipe de sécurité de votre organisation peut utiliser les informations de cette section pour comprendre les nouvelles campagnes, examiner les menaces et gérer les incidents. 
  
![Threat Intelligence vous permet de comprendre les attaques ciblées au sein de votre organisation](media/threatintelwidget.png)
  
  
## <a name="trends"></a>Tendances

Dans la partie inférieure du tableau de bord de sécurité se trouve une section **tendances** , qui récapitule les tendances de flux de messagerie pour votre organisation. Les rapports fournissent des informations sur les e-mails catégorisés comme courrier indésirable, programmes malveillants, tentatives de hameçonnage et courrier électronique. Cliquez sur une vignette pour afficher des informations plus détaillées dans le rapport. 
  
![La section tendances récapitule les tendances de flux de messagerie de l’organisation.](media/trends.png)
  
De plus, si l’abonnement Office 365 de votre organisation inclut [office 365 Advanced Threat Protection Plan 2](office-365-ti.md), vous aurez également un rapport **alertes de gestion des menaces récentes** dans cette section qui permet à votre équipe de sécurité d’afficher et de prendre des mesures sur alertes de sécurité à priorité élevée. 

Pour afficher ou accéder au widget courrier électronique envoyé et reçu, vous devez disposer des autorisations permettant d’afficher les rapports de protection avancée contre les menaces. Pour en savoir plus, consultez [la rubrique Quelles autorisations sont requises pour afficher les rapports ATP?](view-reports-for-atp.md#what-permissions-are-needed-to-view-the-atp-reports). 

Pour afficher ou accéder au widget alertes de gestion des menaces récentes, vous devez disposer des autorisations pour afficher les alertes. Pour en savoir plus, consultez la rubrique [autorisations RBAC requises pour afficher les alertes](alert-policies.md#rbac-permissions-required-to-view-alerts).
  
## <a name="related-topics"></a>Sujets associés

[Afficher les rapports de sécurité de messagerie &amp; dans le centre de sécurité conformité](view-email-security-reports.md)
  
[Afficher les rapports pour Office 365 protection avancée contre les menaces](view-reports-for-atp.md)
  
[Office 365 protection avancée contre les menaces](office-365-atp.md)
  
[Enquête et réponse aux menaces Office 365](office-365-ti.md)
  

