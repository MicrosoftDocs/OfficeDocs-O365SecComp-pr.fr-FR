---
title: Afficher les rapports pour Office 365 protection avancée contre les menaces
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 05/21/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e47e838c-d99e-4c0b-b9aa-e66c4fae902f
ms.collection:
- M365-security-compliance
description: Découvrez comment trouver et utiliser des rapports pour Office 365 protection avancée contre les menaces dans &amp; le centre de sécurité conformité.
ms.openlocfilehash: 6bf8c3222b0ce4cecd1b14f407f7e9ee42783a75
ms.sourcegitcommit: 2b46fba650df8d252b1dd2b3c3f080a383183a06
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/23/2019
ms.locfileid: "34408399"
---
# <a name="view-reports-for-office-365-advanced-threat-protection"></a>Afficher les rapports pour Office 365 protection avancée contre les menaces

Si votre organisation dispose d' [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP) et que vous disposez des [autorisations nécessaires](#what-permissions-are-needed-to-view-the-atp-reports), vous pouvez utiliser plusieurs rapports ATP dans &amp; le centre de sécurité conformité. (Accédez au **** \> **tableau de bord**rapports.)
  
![Le tableau &amp; de bord du centre de sécurité conformité peut vous aider à déterminer le fonctionnement de la protection avancée contre les menaces](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)
  
Les rapports ATP sont les suivants:
- [Rapport d’état de protection contre les menaces](#threat-protection-status-report)
- [Rapport de types de fichiers ATP](#atp-file-types-report)
- [Rapport de disposition des messages ATP](#atp-message-disposition-report)
- [détections en temps réel ou Explorateur](threat-explorer.md) (selon que vous disposez d’Office 365 DAV plan 1 ou 2)
- ... [et bien plus encore](#additional-reports-to-view). 

Lisez cet article pour obtenir une vue d’ensemble des rapports ATP et comment les utiliser.
  
## <a name="threat-protection-status-report"></a>Rapport d’état de protection contre les menaces

Le rapport d' **État de protection contre les menaces** est une vue unique qui rassemble des informations sur le contenu malveillant et les e-mails malveillants détectés et bloqués par [Exchange Online Protection](eop/exchange-online-protection-overview.md) (EOP) et [Office 365 ATP](office-365-atp.md). Ce rapport est utile pour afficher les détections au fil du temps (jusqu’à 90 jours) et permet aux administrateurs de sécurité d’identifier les tendances ou de déterminer si les stratégies ont besoin d’être ajustées. 

Le rapport d’état de protection contre les menaces fournit un nombre agrégé de messages électroniques uniques avec du contenu malveillant, tels que des fichiers ou des adresses de sites Web (URL) bloqués par le moteur anti-programme malveillant, la [purge automatique des heures zéro heure](zero-hour-auto-purge.md)et des fonctionnalités ATP telles que Les [liens approuvés ATP](atp-safe-links.md), [les pièces jointes sûres ATP](atp-safe-attachments.md)et les [fonctionnalités anti-hameçonnage ATP](atp-anti-phishing.md). 

> [!NOTE]
> Un rapport d’état de protection contre les menaces est disponible pour les clients qui ont [Office 365 ATP](office-365-atp.md) ou [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EoP); Toutefois, les informations affichées dans le rapport d’état de protection contre les menaces pour les clients ATP contiennent probablement des données différentes de celles que peuvent afficher les clients EOP. Par exemple, le rapport d’état de protection contre les menaces pour les clients ATP contient des informations sur les [fichiers malveillants détectés dans SharePoint Online, OneDrive ou Microsoft teams](atp-for-spo-odb-and-teams.md). Ces informations sont spécifiques à la protection avancée contre les menaces, de sorte que les clients qui disposent d’EOP mais pas de la fonctionnalité ATP ne verront pas ces détails dans le rapport d’état de protection contre les menaces.
  
Pour afficher le rapport d’état de protection contre les menaces, dans le [Centre de sécurité &amp; conformité](https://protection.office.com), accédez à **rapports** \> **tableau de bord** \> de **protection contre les menaces**.
  
![Rapport d’état de protection contre les menaces ATP](media/6bdd41eb-62e0-423b-9fd4-d1d5baf0cbd5.png)
  
Pour obtenir l’état détaillé d’une journée, pointez sur le graphique.
  
![Données d’état de protection contre les menaces ATP pendant une journée](media/d5c2c6ad-c002-4985-a032-c866e46fdea8.png)
  
Par défaut, le rapport d’état de protection contre les menaces affiche les données des sept derniers jours. Toutefois, vous pouvez choisir **filtres** et modifier la plage de dates pour afficher les données pour 90 jours maximum. (Si vous utilisez un abonnement d’évaluation, vous pouvez être limité à 30 jours de données.)
  
![Filtres d’état de protection contre les menaces ATP](media/4f703369-642b-402b-9758-b9c828283410.png)
  
Vous pouvez également utiliser le menu **afficher les données par** pour modifier les informations affichées dans le rapport. 
  
![Affichage des options pour le rapport d’état de protection contre les menaces ATP](media/4959bf8c-d192-4542-b00b-184e101e7513.png)
  
## <a name="atp-file-types-report"></a>Rapport de types de fichiers ATP

Le rapport **types de fichiers ATP** indique le type de fichiers détectés comme malveillants par des [pièces jointes sûres ATP](atp-safe-attachments.md).
  
Pour afficher ce rapport, dans le [Centre &amp; de sécurité conformité](https://protection.office.com), accédez à **types de fichiers DAV**du **tableau de bord** \> des **rapports** \> .
  
![Rapport de types de fichiers ATP](media/6e3f5d33-79aa-4b2d-938c-6ef135d9e54c.png)
  
Lorsque vous placez le curseur de la souris sur un jour particulier, vous pouvez voir la répartition des types de fichiers malveillants détectés par les [pièces jointes fiables ATP](atp-safe-attachments.md) et la protection contre les [programmes malveillants contre le courrier indésirable &amp; dans Office 365](anti-spam-and-anti-malware-protection.md).
  
![Données de rapport sur les types de fichiers ATP pendant une journée](media/10d18428-699a-41d2-a73e-be3a8214ada1.png)
  
## <a name="atp-message-disposition-report"></a>Rapport de disposition des messages ATP

Le rapport de **disposition des messages ATP** indique les actions qui ont été effectuées pour les messages électroniques détectés comme présentant du contenu malveillant. 
  
Pour afficher ce rapport, dans le [Centre &amp; de sécurité conformité](https://protection.office.com), accédez à rapports **tableau de bord** \> des **rapports** \> **ATP**.
  
![Rapport de disposition des messages ATP](media/b0ff65c4-53d3-496d-bafa-8937a5eb69e5.png)
  
Lorsque vous placez le curseur de la souris sur une barre du graphique, vous pouvez voir les actions effectuées pour les messages électroniques détectés pour ce jour.
  
![Données de rapport de disposition de messages ATP pendant une journée](media/68d2beb8-4b30-48c4-8ba6-5e8ab88ae456.png)
  
## <a name="additional-reports-to-view"></a>Rapports supplémentaires à afficher

Outre les rapports ATP décrits dans cet article, plusieurs autres rapports sont disponibles, comme décrit dans le tableau suivant:

|Rapport (s)  |Détails  |
|---------|---------|
|L' **Explorateur** ou les **détections en temps réel** (Office 365 DAV ATP plan 2 Customers) ont un Explorateur; Office 365 DAV plan 1 les clients ont des détections en temps réel.)| [Explorateur de menaces (et détections en temps réel)](threat-explorer.md)       |
|**Rapports de sécurité de messagerie**, tels que le rapport des expéditeurs et des destinataires, un rapport de courrier indésirable et un rapport de détection du courrier indésirable. | [Afficher les rapports de sécurité de messagerie &amp; dans le centre de sécurité conformité](view-email-security-reports.md)        |
|**Suivi des URL de liens fiables ATP** (Il s’agit d’un rapport que vous générez à l’aide de PowerShell.) Ce rapport affiche les résultats des actions de liens approuvés ATP au cours des sept (7) derniers jours. |[Référence de l’applet de commande Get-UrlTrace](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/get-urltrace?view=exchange-ps) |
|**Résultats EOP et ATP** (Il s’agit d’un rapport personnalisé que vous générez à l’aide de PowerShell). Ce rapport contient des informations, telles que le domaine, la date, le type d’événement, la direction, l’action et le nombre de messages.  | [Référence de l’applet de commande Get-MailTrafficATPReport](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/get-mailtrafficatpreport?view=exchange-ps) |
|**Détections EOP et ATP** (Il s’agit d’un rapport personnalisé que vous générez à l’aide de PowerShell). Ce rapport contient des détails sur les URL ou les fichiers malveillants, les tentatives de hameçonnage, l’emprunt d’identité et d’autres menaces potentielles dans les messages électroniques ou les fichiers.   | [Référence de l’applet de commande Get-MailDetailATPReport](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/get-maildetailatpreport?view=exchange-ps)        |

  
## <a name="what-permissions-are-needed-to-view-the-atp-reports"></a>Quelles sont les autorisations nécessaires pour afficher les rapports ATP?

Pour afficher et utiliser les rapports décrits dans cet article, **vous devez disposer d’un rôle approprié pour le centre de sécurité &amp; et le centre d’administration Exchange**.

- Pour le centre &amp; de sécurité conformité, vous devez disposer de l’un des rôles suivants:
    - Gestion de l’organisation
    - Administrateur de la sécurité (qui peut être affecté dans le centre d’administration Azure[https://aad.portal.azure.com](https://aad.portal.azure.com)Active Directory ())
    - Lecteur de sécurité

- Pour Exchange Online, vous devez disposer de l’un des rôles suivants, qui est affecté dans le centre[https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)d’administration Exchange () ou avec des applets de commande PowerShell (consultez la rubrique [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)):
    - Gestion de l’organisation
    - Gestion de l’organisation en affichage seul
    - Rôle Destinataires en affichage uniquement
    - Gestion de la conformité

Pour en savoir plus, consultez les ressources suivantes:

- [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md)

- [Autorisations des fonctionnalités dans Exchange Online](https://docs.microsoft.com/exchange/permissions-exo/feature-permissions)
   
## <a name="what-if-the-reports-arent-showing-data"></a>Qu’en est-il si les rapports n’affichent pas de données?

Si vous ne voyez pas de données dans vos rapports ATP, vérifiez que vos stratégies sont correctement configurées. Votre organisation doit avoir des [stratégies de liens fiables ATP](set-up-atp-safe-links-policies.md) et des [stratégies de pièces jointes approuvées ATP](set-up-atp-safe-attachments-policies.md) définies afin que la protection ATP soit mise en place. Consultez également la rubrique protection contre le [courrier indésirable et les programmes malveillants dans Office 365](anti-spam-and-anti-malware-protection.md).
  
## <a name="related-topics"></a>Sujets associés

[Rapports et informations dans le centre de sécurité &amp; conformité Office 365](reports-and-insights-in-security-and-compliance.md)
  
[Créer une planification pour un rapport dans le centre &amp; de sécurité conformité](create-a-schedule-for-a-report.md)
  
[Configurer et télécharger un rapport personnalisé dans le centre de &amp; sécurité conformité](set-up-and-download-a-custom-report.md)
  

