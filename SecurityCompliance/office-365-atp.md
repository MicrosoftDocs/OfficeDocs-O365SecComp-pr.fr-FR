---
title: Office 365 - Protection avancée contre les menaces
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/04/2019
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e100fe7c-f2a1-4b7d-9e08-622330b83653
description: Protection contre les menaces avancées Office 365 inclut usurpation d’identité aide à la décision, liens fiables, pièces jointes fiables et des fonctionnalités anti-hameçonnage avancées. Protection contre les menaces avancées est également étendu aux fichiers dans SharePoint Online, OneDrive pour les entreprises et Teams Microsoft.
ms.openlocfilehash: 7d60ac9bff108a6746a5e89d05d70bba23d2671d
ms.sourcegitcommit: a64af0ebd0b03e4a5e60a33e9108c44c7d74f356
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2019
ms.locfileid: "29741037"
---
# <a name="office-365-advanced-threat-protection"></a>Office 365 - Protection avancée contre les menaces

## <a name="overview-of-office-365-advanced-threat-protection"></a>Vue d’ensemble de la Protection de Microsoft Office 365 menace avancées

Office 365 Advanced Threat Protection (DAV) vous aide à protéger votre organisation contre les attaques par :
  
- Analyse les pièces jointes des programmes malveillants avec les [Pièces jointes fiables DAV](atp-safe-attachments.md)
    
- Analyse web adresses (URL) dans les messages électroniques et des documents Office avec [Des liens fiables DAV](atp-safe-links.md)
    
- Identification et le blocage des fichiers dans des bibliothèques en ligne avec [DAV pour SharePoint, OneDrive et les équipes Microsoft](atp-for-spo-odb-and-teams.md) malveillants
    
- Vérification des messages électroniques pour l’usurpation d’identité non autorisé avec [usurpation d’identité aide à la décision](learn-about-spoof-intelligence.md)
    
- Détecter lorsqu’un utilisateur tente d’emprunter l’identité de vos utilisateurs et les domaines personnalisés de votre organisation grâce à des [fonctionnalités anti-hameçonnage de DAV dans Office 365](atp-anti-phishing.md)
    
**Protection via Office 365 DAV est déterminée par les stratégies de l’équipe de sécurité de votre organisation définit pour les liens fiables, pièces jointes fiables et Anti-hameçonnage**. Il est important de définir des stratégies, ainsi que de régulièrement passer en revue et modifier les stratégies pour les mettre à jour et de tirer parti des nouvelles fonctionnalités qui sont ajoutées au service. 

[Les rapports sont disponibles](view-reports-for-atp.md) pour afficher le fonctionne DAV pour votre organisation. Ces rapports peuvent également vous montrer les domaines où vous devrez peut-être passer en revue et mettre à jour vos stratégies. Et, si vous disposez des fichiers qui sont marqués comme les logiciels malveillants qui ne doivent pas être ou fichiers que vous souhaitez que Microsoft pour examiner, vous pouvez [Envoyer un fichier à Microsoft pour analyse](#submit-a-suspicious-file-to-microsoft-for-analysis).

## <a name="new-features-are-continually-being-added-to-atp"></a>Nouvelles fonctionnalités sont continuellement ajoutées au DAV

Nous poursuivons ajouter de nouvelles fonctionnalités à Office 365, et qui inclut DAV. Vous trouverez ci-dessous une liste des nouvelles fonctionnalités, dont certains appels d’une stratégie de vente être révisé et mis à jour. Pour plus d’informations sur les nouvelles fonctionnalités bientôt DAV (ou Microsoft 365 en général), visitez le site de la [Feuille de route Microsoft 365](https://www.microsoft.com/microsoft-365/roadmap?filters=O365).


|Mises à jour de fonctionnalité  |Points d’action  |
|---------|---------|
|À partir de 2018 octobre et présentant plusieurs mois suivant, lors de personnes utilisent Outlook ou Outlook Web Application (OWA), les liens sécurisés DAV affiche les URL d’origine, pas réécrites URL. (Nous appelons ce rendu lien native).<br>Lorsque le rendu de lien natif est disponible pour votre organisation, cette fonctionnalité fonctionne dans Outlook 365 (Click-to-Run) et OWA.|Aucun         |
|Début de septembre 2018, [pages d’avertissement Office 365 DAV](atp-safe-links-warning-pages.md) fonctionnalité un jeu de couleurs, plus de détails et la possibilité de passer à un site en dépit de donné avertissements et des recommandations. |Aucun         |
|À partir du deuxième semestre 2018, protection liens fiables DAV est étendue pour appliquer aux URL dans Office Online (Word en ligne, Online Excel, PowerPoint en ligne et OneNote en ligne) et Office 365 ProPlus sur Mac.   |[Revoir et modifier vos stratégies de liens fiables DAV](set-up-atp-safe-links-policies.md)  |
|À partir de fin mai 2018, les fonctionnalités de [mise en quarantaine](quarantine-email-messages.md) dans la sécurité &amp; centre de conformité sont accordées à [DAV pour SharePoint Online, OneDrive entreprise et les équipes Microsoft](atp-for-spo-odb-and-teams.md). |[Revoir et modifier vos stratégies de pièces jointes sûres DAV](set-up-atp-safe-attachments-policies.md) |
|Au début de mars 2018, protection liens fiables DAV est étendue s’appliquent aux messages envoyés entre les personnes dans votre organisation. |[Revoir et modifier vos stratégies de liens fiables DAV](set-up-atp-safe-links-policies.md) |
|Au début de la liaison tardive 2017 octobre, protection liens fiables DAV est étendue pour appliquer aux URL dans un e-mail ainsi que les URL dans les documents Office 365 ProPlus, telles que Word, Excel, PowerPoint et Visio sur Windows, ainsi que Office applications sur les périphériques iOS ou Android.  |Assurez-vous que vous utilisez [l’Authentification moderne pour Office](https://docs.microsoft.com/office365/enterprise/modern-auth-for-office-2013-and-2016) |
  
## <a name="get-office-365-atp"></a>Obtenir DAV Office 365

Office 365 DAV est inclus dans les abonnements, tels que [Microsoft 365 pour entreprises](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), Office 365 entreprise E5 et Office 365 éducation A5. Si votre organisation a un abonnement à Office 365 qui n’inclut pas d’Office 365 DAV, vous pouvez acheter potentiellement DAV comme module complémentaire. Pour plus d’informations, voir [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description). 

## <a name="define-policies-for-atp"></a>Définir des stratégies pour DAV

Pour définir (ou modifier) les stratégies de vente, vous devez posséder un des rôles décrits dans le tableau suivant :

|Rôle  |Où/procédure affecté  |
|---------|---------|
|Administrateur Global d’Office 365 |La personne qui s’inscrit à acheter Office 365 est un administrateur global par défaut. (Voir [les rôles d’administration sur Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) pour en savoir plus).         |
|Administrateur de sécurité Office 365 |Centre d’administration ([https://aka.ms/admincenter](https://aka.ms/admincenter))|
|Gestion de l’organisation en ligne Exchange |Centre d’administration Exchange ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) <br>ou <br>  Applets de commande PowerShell (voir [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)) |

Il existe plusieurs types de stratégies DAV pour définir et consulter régulièrement.

1. **[Configurer des stratégies anti-hameçonnage de DAV dans Office 365](set-up-anti-phishing-policies.md)** , y compris les attaques de l’emprunt d’identité pour protéger contre les attaques qui envoient des messages électroniques qui semblent à partir de domaines ou des personnes de confiance. 

2. **[Définir des stratégies de liens fiables DAV dans Office 365](set-up-atp-safe-links-policies.md)** , y compris la [liste URL bloqué personnalisée](set-up-a-custom-blocked-urls-list-wtih-atp.md) et [liste des URL personnalisée « Pas de rewrite »](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md)de votre organisation.
    
3. **[Définir des stratégies de pièces jointes sûres DAV dans Office 365](set-up-atp-safe-attachments-policies.md)** et choisir parmi plusieurs options, telles que la [remise dynamique et l’aperçu](dynamic-delivery-and-previewing.md).
  
## <a name="see-how-atp-is-working-by-viewing-reports"></a>Voir comment fonctionne DAV en affichant des rapports

Une fois vos stratégies DAV sont mis en place, les rapports sont disponibles pour afficher la façon dont le service fonctionne. (Dans le centre de conformité & Office 365 sécurité, accédez aux **rapports** > **tableau de bord**.)

[![La sécurité &amp; tableau de bord de centre de conformité peut vous aider à voir où travaille protection contre les menaces avancées](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)](view-reports-for-atp.md)
  
1. En tant qu’un administrateur global d’Office 365, un administrateur de sécurité ou un lecteur de sécurité, accédez à [https://protection.office.com](https://protection.office.com) et se connecter.
    
2. Accédez aux **rapports** > **tableau de bord**. (Pour obtenir de l’aide avec ces rapports, voir [Afficher les rapports de protection contre les menaces avancées](view-reports-for-atp.md)).
    
3. Si nécessaire, ajuster vos stratégies de sécurité. Pour obtenir l’aide à ce sujet, voir les ressources suivantes :
      - [Stratégies anti-hameçonnage DAV dans Office 365](set-up-anti-phishing-policies.md)
      - [Stratégies de liens fiables DAV dans Office 365](set-up-atp-safe-links-policies.md)
      - [Stratégies de pièces jointes sûres DAV dans Office 365](set-up-atp-safe-attachments-policies.md)
    
    
## <a name="submit-a-suspicious-file-to-microsoft-for-analysis"></a>Envoyer un fichier suspect à Microsoft pour analyse

- Si vous obtenez un fichier que vous pensez que possible des programmes malveillants, vous pouvez envoyer ce fichier à Microsoft pour analyse. Visitez le [portail d’aide à la décision de Windows Defender sécurité envoi](https://go.microsoft.com/fwlink/?linkid=857185).

- Si vous recevez un message électronique (avec ou sans pièce jointe) que vous souhaitez envoyer à Microsoft pour analyse, utilisez le [complément de Message de rapport](enable-the-report-message-add-in.md). 
  

