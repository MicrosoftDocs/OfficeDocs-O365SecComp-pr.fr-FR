---
title: Office 365 - Protection avancée contre les menaces
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 11/27/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e100fe7c-f2a1-4b7d-9e08-622330b83653
description: Protection contre les menaces avancées Office 365 inclut usurpation d’identité aide à la décision, liens fiables, pièces jointes fiables et des fonctionnalités anti-hameçonnage avancées. Protection contre les menaces avancées est également étendu aux fichiers dans SharePoint Online, OneDrive pour les entreprises et Teams Microsoft.
ms.openlocfilehash: c147fde4e470b998a66a2cb456be71f635db25d7
ms.sourcegitcommit: 2cf7f5bb282c971d33e00f65d9982a3f14aec74e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/27/2018
ms.locfileid: "26706308"
---
# <a name="office-365-advanced-threat-protection"></a>Office 365 - Protection avancée contre les menaces

## <a name="overview"></a>Vue d’ensemble

Office 365 Advanced Threat Protection (DAV) vous aide à protéger votre organisation contre les attaques par :
  
- Analyse les pièces jointes des programmes malveillants avec les [Pièces jointes fiables DAV](atp-safe-attachments.md)
    
- Analyse web adresses (URL) dans les messages électroniques et des documents Office avec [Des liens fiables DAV](atp-safe-links.md)
    
- Identification et le blocage des fichiers dans des bibliothèques en ligne avec [DAV pour SharePoint, OneDrive et les équipes Microsoft](atp-for-spo-odb-and-teams.md) malveillants
    
- Vérification des messages électroniques pour l’usurpation d’identité non autorisé avec [usurpation d’identité aide à la décision](learn-about-spoof-intelligence.md)
    
- Détecter lorsqu’un utilisateur tente d’emprunter l’identité de vos utilisateurs et les domaines personnalisés de votre organisation grâce à des [fonctionnalités anti-hameçonnage de DAV dans Office 365](atp-anti-phishing.md)
    
**Protection via Office 365 DAV est déterminée par les stratégies de l’équipe de sécurité de votre organisation définit pour les liens fiables, pièces jointes fiables et Anti-hameçonnage**. Il est important de consulter régulièrement et de modifier vos stratégies pour les mettre à jour et de tirer parti des nouvelles fonctionnalités qui sont ajoutées au service. [Les rapports sont disponibles](view-reports-for-atp.md) pour afficher le fonctionne DAV pour votre organisation. Ces rapports peuvent également vous montrer les domaines où vous devrez peut-être passer en revue et mettre à jour vos stratégies. Et, si vous disposez des fichiers qui sont marqués comme les logiciels malveillants qui ne doivent pas être ou fichiers que vous souhaitez que Microsoft pour examiner, vous pouvez [Envoyer un fichier à Microsoft pour analyse](#submit-a-suspicious-file-to-microsoft-for-analysis).

## <a name="new-features-are-continually-being-added-to-atp"></a>Nouvelles fonctionnalités sont continuellement ajoutées au DAV

Nous poursuivons ajouter de nouvelles fonctionnalités à Office 365, et qui inclut DAV. Vous trouverez ci-dessous une liste des nouvelles fonctionnalités, dont certains appels d’une stratégie de vente être révisé et mis à jour. Pour plus d’informations sur les nouvelles fonctionnalités bientôt DAV (ou Microsoft 365 en général), visitez le site de la [Feuille de route Microsoft 365](https://www.microsoft.com/microsoft-365/roadmap?filters=O365).
  
- Au début de la liaison tardive 2017 octobre, protection liens fiables DAV est étendue pour appliquer aux URL dans un e-mail ainsi que les URL dans les documents Office 365 ProPlus, telles que Word, Excel, PowerPoint et Visio sur Windows, ainsi que Office applications sur les périphériques iOS ou Android. (Assurez-vous que vous utilisez [l’Authentification moderne pour Office](https://docs.microsoft.com/office365/enterprise/modern-auth-for-office-2013-and-2016)).
    
- Au début de mars 2018, protection liens fiables DAV est étendue s’appliquent aux messages envoyés entre les personnes dans votre organisation. (Assurez-vous [d’examiner et modifier vos stratégies de liens fiables DAV](set-up-atp-safe-links-policies.md).)

- À partir de fin mai 2018, les fonctionnalités de [mise en quarantaine](quarantine-email-messages.md) dans la sécurité &amp; centre de conformité sont accordées à [DAV pour SharePoint Online, OneDrive entreprise et les équipes Microsoft](atp-for-spo-odb-and-teams.md).
 
- À partir du deuxième semestre 2018, protection liens fiables DAV est étendue pour appliquer aux URL dans Office Online (Word en ligne, Online Excel, PowerPoint en ligne et OneNote en ligne) et Office 365 ProPlus sur Mac. (Assurez-vous [d’examiner et modifier vos stratégies de liens fiables DAV](set-up-atp-safe-links-policies.md).)

- Début de septembre 2018, [pages d’avertissement Office 365 DAV](atp-safe-links-warning-pages.md) fonctionnalité un jeu de couleurs, plus de détails et la possibilité de passer à un site en dépit de donné avertissements et des recommandations. 
 
- À partir de 2018 octobre et présentant les prochains mois plusieurs, lorsque personnes utilisent Outlook Web Application (OWA) ou Outlook, les liens sécurisés DAV n'affiche pas les URL d’origine, réécrit URL. (Nous appelons cette visibilité lien native).

      
## <a name="get-office-365-atp"></a>Obtenir DAV Office 365

> [!IMPORTANT]
> DAV Office 365 est inclus dans les abonnements, tels que Microsoft 365 entreprise, Office 365 entreprise E5, Office 365 éducation A5 et [Microsoft 365 Business](https://docs.microsoft.com/en-us/microsoft-365/business/security-features). Si votre organisation a un abonnement à Office 365 qui n’inclut pas d’Office 365 DAV, vous pouvez acheter potentiellement DAV comme module complémentaire. Pour plus d’informations, voir [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description). 

1. En tant qu’un administrateur global ou de sécurité, accédez à [https://portal.office.com](https://portal.office.com) et connectez-vous avec votre compte professionnel ou de l’école pour Office 365. 
    
2. Choisissez **Admin** \> **facturation** pour voir ce que comprend votre abonnement actuel. <br/>![En tant qu’un administrateur global, se connecter à portal.office.com et accédez à Admin \> de facturation](media/18a3546c-bd1f-4f49-82ec-0184909b42c2.png)
  
3. Si vous voyez **Office 365 entreprise E5**, **Office 365 éducation A5**ou **Microsoft 365 Business**, votre organisation a DAV. <br/>Si vous voyez un autre abonnement, telles que **Office 365 entreprise E3** ou **Office 365 entreprise E1**, envisagez d’ajouter DAV. Pour ce faire, cliquez sur **+ Ajouter abonnement**.
    
Une fois que vous avez DAV, l’étape suivante consiste à votre équipe de sécurité définir des stratégies. 
  
## <a name="define-policies-for-atp"></a>Définir des stratégies pour DAV

- **[Configurer des stratégies anti-hameçonnage de DAV dans Office 365](set-up-anti-phishing-policies.md)** , y compris les attaques de l’emprunt d’identité pour protéger contre les attaques qui envoient des messages électroniques qui semblent à partir de domaines ou des personnes de confiance 

- **[Définir des stratégies de liens fiables DAV dans Office 365](set-up-atp-safe-links-policies.md)** , y compris la [liste URL bloqué personnalisée](set-up-a-custom-blocked-urls-list-wtih-atp.md) et [liste des URL personnalisée « Pas de rewrite »](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) de votre organisation
    
- **[Définir des stratégies de pièces jointes sûres DAV dans Office 365](set-up-atp-safe-attachments-policies.md)** comprenant [remise dynamique et l’aperçu](dynamic-delivery-and-previewing.md)
  
## <a name="see-how-atp-is-working-by-viewing-reports"></a>Voir comment fonctionne DAV en affichant des rapports

Une fois vos stratégies DAV sont mis en place, les rapports sont disponibles pour afficher la façon dont le service fonctionne.

[![La sécurité &amp; tableau de bord de centre de conformité peut vous aider à voir où travaille protection contre les menaces avancées](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)](view-reports-for-atp.md)
  
1. Assurez-vous que vous êtes un administrateur global, administrateur de sécurité ou lecteur de sécurité Office 365. (Voir [les autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md).)
    
2. [Afficher les rapports de protection contre les menaces avancées](view-reports-for-atp.md).
    
3. Si nécessaire, ajuster vos stratégies de sécurité. Voir les ressources suivantes :

  - [Stratégies anti-hameçonnage DAV dans Office 365](set-up-anti-phishing-policies.md)
    
  - [Stratégies de liens fiables DAV dans Office 365](set-up-atp-safe-links-policies.md)
    
  - [Stratégies de pièces jointes sûres DAV dans Office 365](set-up-atp-safe-attachments-policies.md)
    
    
## <a name="submit-a-suspicious-file-to-microsoft-for-analysis"></a>Envoyer un fichier suspect à Microsoft pour analyse

- Si vous obtenez un fichier que vous pensez que possible des programmes malveillants, vous pouvez envoyer ce fichier à Microsoft pour analyse. Visitez le [portail d’aide à la décision de Windows Defender sécurité envoi](https://go.microsoft.com/fwlink/?linkid=857185).

- Si vous recevez un message électronique (avec ou sans pièce jointe) que vous souhaitez envoyer à Microsoft pour analyse, utilisez le [complément de Message de rapport](enable-the-report-message-add-in.md). 
  

