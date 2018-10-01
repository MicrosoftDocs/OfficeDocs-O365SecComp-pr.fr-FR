---
title: Office 365 - Protection avancée contre les menaces
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/1/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e100fe7c-f2a1-4b7d-9e08-622330b83653
description: Protection contre les menaces avancées Office 365 inclut usurpation d’identité aide à la décision, liens fiables, pièces jointes fiables et des fonctionnalités anti-hameçonnage avancées. Protection contre les menaces avancées est également étendu aux fichiers dans SharePoint Online, OneDrive pour les entreprises et Teams Microsoft.
ms.openlocfilehash: 53488534d3a74f9e026142ed053dfcff5db6cbf9
ms.sourcegitcommit: 7032830867eb3fc71760e04b8342aff174c5d757
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/01/2018
ms.locfileid: "25353270"
---
# <a name="office-365-advanced-threat-protection"></a>Office 365 - Protection avancée contre les menaces

Office 365 Advanced Threat Protection (DAV) vous aide à protéger votre organisation contre les attaques par :
  
- Analyse des pièces jointes avec les [Pièces jointes fiables DAV](atp-safe-attachments.md)
    
- Analyse web adresses (URL) dans les messages électroniques et des documents Office avec [Des liens fiables DAV](atp-safe-links.md)
    
- Identification et le blocage des fichiers dans des bibliothèques en ligne avec [DAV pour SharePoint, OneDrive et les équipes Microsoft](atp-for-spo-odb-and-teams.md) malveillants
    
- Vérification des messages électroniques pour l’usurpation d’identité non autorisé avec [usurpation d’identité aide à la décision](learn-about-spoof-intelligence.md)
    
- Détecter lorsqu’un utilisateur tente d’emprunter l’identité de vos utilisateurs et les domaines personnalisés de votre organisation grâce à des [fonctionnalités anti-hameçonnage de DAV dans Office 365](atp-anti-phishing.md)
    
**Protection via Office 365 DAV est déterminée par les stratégies de l’équipe de sécurité de votre organisation définit pour les liens fiables, pièces jointes fiables et Anti-hameçonnage**. Il est important de consulter régulièrement et de modifier vos stratégies pour les mettre à jour et de tirer parti des nouvelles fonctionnalités qui sont ajoutées au service. [Les rapports sont disponibles](view-reports-for-atp.md) pour afficher le fonctionne DAV pour votre organisation. Ces rapports peuvent également vous montrer les domaines où vous devrez peut-être passer en revue et mettre à jour vos stratégies. Et, si vous disposez des fichiers qui sont marqués comme les logiciels malveillants qui ne doivent pas être ou fichiers que vous souhaitez que Microsoft pour examiner, vous pouvez [Envoyer des fichiers à Microsoft pour analyse](office-365-atp.md#submitlalware).
  
> [!IMPORTANT]
> Office 365 DAV est inclus dans les abonnements, telles que Office 365 entreprise E5 et Office 365 éducation A5 et, depuis le 30 avril 2018, également les [fonctionnalités de sécurité Microsoft 365 Business](https://support.office.com/article/c123694a-1efb-459e-a8d5-2187975373dc). Si votre organisation a un abonnement à Office 365 qui n’inclut pas d’Office 365 DAV, vous pouvez acheter potentiellement DAV comme module complémentaire. Pour plus d’informations, voir [Office 365 Advanced Threat Protection Service Description](https://technet.microsoft.com/library/exchange-online-advanced-threat-protection-service-description.aspx). 
      
## <a name="get-office-365-atp"></a>Obtenir DAV Office 365

1. En tant qu’un administrateur global ou de sécurité, accédez à [https://portal.office.com](https://portal.office.com) et connectez-vous avec votre compte professionnel ou de l’école pour Office 365. 
    
2. Choisissez **Admin** \> **facturation** pour voir ce que comprend votre abonnement actuel. 
    
    ![En tant qu’un administrateur global, se connecter à portal.office.com et accédez à Admin \> de facturation](media/18a3546c-bd1f-4f49-82ec-0184909b42c2.png)
  
3. Si vous voyez **Office 365 entreprise E5**, **Office 365 éducation A5**ou **Microsoft 365 Business**, votre organisation a DAV. 
    
    Si vous voyez un autre abonnement, telles que **Office 365 entreprise E3** ou **Office 365 entreprise E1**, envisagez d’ajouter DAV. Pour ce faire, cliquez sur **+ Ajouter abonnement**.
    
Une fois que vous avez DAV, l’étape suivante consiste à votre équipe de sécurité définir des stratégies de protection [Fiable liens](atp-safe-links.md), les [Pièces jointes sûres](atp-safe-attachments.md)et [Anti-hameçonnage](set-up-atp-anti-phishing-policies.md) . 
  
[Que souhaitez-vous faire ?](office-365-atp.md#TOC)
  
## <a name="define-policies-for-atp"></a>Définir des stratégies pour DAV

- **[Définir des stratégies de liens fiables DAV dans Office 365](set-up-atp-safe-links-policies.md)** , y compris la [liste URL bloqué personnalisée](set-up-a-custom-blocked-urls-list-wtih-atp.md) et [liste des URL personnalisée « Pas de rewrite »](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) de votre organisation
    
- **[Configurer les pièces jointes sûres DAV stratégies dans Office 365](set-up-atp-safe-attachments-policies.md)** comprenant [remise dynamique et l’aperçu](dynamic-delivery-and-previewing.md)
    
- **[Configurer des stratégies anti-hameçonnage de DAV dans Office 365](set-up-atp-anti-phishing-policies.md)** , y compris les attaques de l’emprunt d’identité pour protéger contre les attaques qui envoient des messages électroniques qui semblent à partir de domaines ou des personnes de confiance 
  
## <a name="see-how-atp-is-working-by-viewing-reports"></a>Voir comment fonctionne DAV en affichant des rapports

Une fois vos stratégies DAV sont mis en place, les rapports sont disponibles pour afficher la façon dont le service fonctionne.

[![La sécurité &amp; tableau de bord de centre de conformité peut vous aider à voir où travaille protection contre les menaces avancées](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)](view-reports-for-atp.md)
  
1. Assurez-vous que vous êtes un administrateur global, administrateur de sécurité ou lecteur de sécurité Office 365. (Voir [les autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md).)
    
2. [Afficher les rapports de protection contre les menaces avancées et Exchange Online Protection](view-reports-for-atp.md).
    
3. Si nécessaire, ajuster vos stratégies de sécurité. Voir les ressources suivantes :
    
  - [Stratégies de liens fiables DAV dans Office 365](set-up-atp-safe-links-policies.md)
    
  - [Stratégies de pièces jointes sûres DAV dans Office 365](set-up-atp-safe-attachments-policies.md)
    
  - [Stratégies anti-hameçonnage DAV dans Office 365](set-up-atp-anti-phishing-policies.md)
    
[Que souhaitez-vous faire ?](office-365-atp.md)
  
## <a name="submit-a-suspicious-file-to-microsoft-for-analysis"></a>Envoyer un fichier suspect à Microsoft pour analyse

Si vous obtenez un fichier que vous pensez que possible des programmes malveillants, vous pouvez envoyer ce fichier à Microsoft pour analyse. Visitez le [portail d’aide à la décision de Windows Defender sécurité envoi](https://go.microsoft.com/fwlink/?linkid=857185).
  
## <a name="related-topics"></a>Voir aussi

[Vue d’ensemble de la sécurité Office 365 &amp; centre de conformité](https://support.office.com/article/a5f2fd18-b029-4257-b5a8-ae83e7768c85)
  
[Afficher les rapports de protection contre les menaces avancées](view-reports-for-atp.md)
  
[Menaces de sécurité Office 365 la gestion &amp; centre de conformité](threat-management.md)
  

