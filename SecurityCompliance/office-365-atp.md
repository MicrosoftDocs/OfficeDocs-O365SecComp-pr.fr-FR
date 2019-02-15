---
title: Office 365 - Protection avancée contre les menaces
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/08/2019
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e100fe7c-f2a1-4b7d-9e08-622330b83653
ms.collection:
- M365-security-compliance
description: Office 365 Advanced Threat Protection inclut des fonctionnalités d'usurpation d'identité, des liens fiables, des pièces jointes fiables, des fonctionnalités anti-hameçonnage avancées et une intelligence des menaces.
ms.openlocfilehash: d78b37ca048187a298b6e083b54ad68b949638ef
ms.sourcegitcommit: 2af6c3e8a74995294a67429530af8f085e6ca136
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/14/2019
ms.locfileid: "30051175"
---
# <a name="office-365-advanced-threat-protection"></a>Office 365 - Protection avancée contre les menaces

## <a name="overview-of-office-365-advanced-threat-protection"></a>Vue d'ensemble de la protection avancée contre les menaces Office 365

> [!IMPORTANT]
> Cet article est destiné aux clients professionnels. Si vous êtes un utilisateur à domicile et que vous recherchez des informations sur les liens fiables dans Outlook, consultez la rubrique [Advanced Outlook.com Security](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2).

Office 365 Advanced Threat Protection (ATP) contribue à protéger votre organisation contre les attaques malveillantes en:
  
- Analyse des pièces jointes de courrier électronique pour les programmes malveillants avec [pièces jointEs fiables](atp-safe-attachments.md)
    
- Analyse des adresses Web (URL) dans les messages électroniques et les documents Office à l'aide de [liens fiables ATP](atp-safe-links.md)
    
- Identification et blocage des fichiers malveillants dans les bibliothèques en ligne avec la protection avancée contre [les menaces pour SharePoint, OneDrive et Microsoft teams](atp-for-spo-odb-and-teams.md)
    
- Vérification des messages électroniques pour l'usurpation d'identité non autorisée avec l'aide à l' [usurpation d'identité](learn-about-spoof-intelligence.md)
    
- Détection des personnes qui tentent d'emprunter l'identité de vos utilisateurs et des domaines personnalisés de votre organisation à l'aide [de fonctionnalités anti-hameçonnage ATP dans Office 365](atp-anti-phishing.md)
    
**La protection par le biais de la protection avancée contre les menaces Office 365 est déterminée par les stratégies définies par l'équipe de sécurité de votre organisation pour les liens fiables, les pièces jointEs fiables et la protection anti-hameçonnage**. Il est important de définir des stratégies, de vérifier et de réviser régulièrement ces stratégies afin de les maintenir à jour et de tirer parti des nouvelles fonctionnalités ajoutées au service. 

Les [rapports sont disponibles](view-reports-for-atp.md) pour illustrer l'utilisation de la fonctionnalité ATP pour votre organisation. Ces rapports peuvent également vous indiquer des zones où vous devrez peut-être revoir et mettre à jour vos stratégies. De plus, si vous avez des fichiers marqués comme programmes malveillants qui ne devraient pas être ou des fichiers que Microsoft doit examiner, vous pouvez [soumettre un fichier à Microsoft pour analyse](#submit-a-suspicious-file-to-microsoft-for-analysis).

## <a name="new-features-are-continually-being-added-to-atp"></a>De nouvelles fonctionnalités sont continuellement ajoutées à la protection avancée contre les menaces

Nous continuons à ajouter de nouvelles fonctionnalités à Office 365 et cela inclut la protection avancée contre les menaces. Vous trouverez ci-dessous une liste de plusieurs nouvelles fonctionnalités, dont certaines appellent une stratégie de protection avancée contre les menaces à examiner et à mettre à jour. Pour en savoir plus sur les nouvelles fonctionnalités disponibles pour la protection avancée contre les menaces (ou Microsoft 365 en général), consultez la feuille de [route microsoft 365](https://www.microsoft.com/microsoft-365/roadmap?filters=O365).


|Mises à jour de fonctionnalité  |Éléments d'action  |
|---------|---------|
|Depuis le mois de février 2019 et le déploiement sur les prochains mois, des capacités d'aide à la décision sont ajoutées à la protection avancée contre les menaces. En outre, si votre organisation ne dispose actuellement pas de la protection avancée contre les menaces, vous aurez de nouvelles options à prendre en compte, notamment les plans ATP 1 et DAV 2. Pour en savoir plus, consultez les [offres et tarifs office 365 Advanced Threat Protection](https://products.office.com/exchange/advance-threat-protection) et la [Description du service Office 365 Advanced Threat Protection](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description). |Vérifiez l'abonnement de votre organisation et, si nécessaire, [achetez ou modifiez un module complémentaire](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/buy-or-edit-an-add-on).  |
|Depuis le mois d'octobre 2018 et le déploiement sur les prochains mois, lorsque des personnes utilisent Outlook ou Outlook Web App (OWA), les liens fiables ATP affichent les URL d'origine, et non les URL réécrites. (Nous appelons ce rendu de liaison native.)<br>Lorsque le rendu de liens natif est disponible pour votre organisation, cette fonctionnalité fonctionne dans Outlook 365 (démarrer en un clic) et OWA.|Aucun         |
|À partir du 2018 septembre, les [pages d'avertissement ATP Office 365](atp-safe-links-warning-pages.md) comportent un nouveau jeu de couleurs, des détails supplémentaires, ainsi que la possibilité de continuer sur un site malgré des avertissements et des recommandations. |Aucun         |
|Depuis la deuxième moitié de 2018, la protection des liens fiables ATP est étendue pour s'appliquer aux URL dans Office Online (Word Online, Excel Online, PowerPoint Online et OneNote Online) et Office 365 proPlus sur Mac.   |[Vérifier et modifier vos stratégies de liens fiables ATP](set-up-atp-safe-links-policies.md)  |
|À compter du 2018 mai, les fonctionnalités de [mise](quarantine-email-messages.md) en quarantaine &amp; dans le centre de sécurité conformité sont étendues à la protection avancée contre les menaces [pour SharePoint Online, OneDrive entreprise et Microsoft teams](atp-for-spo-odb-and-teams.md). |[Vérifier et modifier vos stratégies de pièces jointes approuvées ATP](set-up-atp-safe-attachments-policies.md) |
|Depuis le 2018 mars, la protection des liens fiables ATP est étendue pour s'appliquer aux courriers électroniques envoyés entre les personnes au sein d'une organisation. |[Vérifier et modifier vos stratégies de liens fiables ATP](set-up-atp-safe-links-policies.md) |
|À compter de la fin du 1er octobre 2017, la protection des liens fiables ATP est étendue aux URL de messagerie électronique ainsi qu'aux URL des documents Office 365 proPlus, comme Word, Excel, PowerPoint et Visio sous Windows, ainsi qu'aux applications Office sur les appareils iOS et Android.  |Assurez-vous que vous utilisez l' [authentification moderne pour Office](https://docs.microsoft.com/office365/enterprise/modern-auth-for-office-2013-and-2016) |

## <a name="get-office-365-atp"></a>Obtenir l'ATP Office 365

La protection avancée contre les menaces Office 365 est incluse dans les abonnements, tels que [microsoft 365 entreprise](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365](https://www.microsoft.com/microsoft-365/business)entreprise, Office 365 entreprise E5 et Office 365 éducation a5. Si votre organisation dispose d'un abonnement Office 365 qui n'inclut pas Office 365 ATP, vous pouvez acheter l'ATP en tant que module complémentaire. Pour plus d'informations, consultez la rubrique [offres et tarifs de protection avancée contre les menaces office 365](https://products.office.com/exchange/advance-threat-protection) , ainsi que la [Description du service Office 365 Advanced Threat Protection](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description). 

## <a name="define-policies-for-atp"></a>Définir des stratégies pour la protection avancée contre les menaces

Pour définir (ou modifier) des stratégies ATP, vous devez disposer de l'un des rôles décrits dans le tableau suivant:

|Rôle  |WHERE/How Assigned  |
|---------|---------|
|Administrateur général Office 365 |La personne qui s'inscrit pour acheter Office 365 est un administrateur global par défaut. (Pour en savoir plus, consultez la rubrique [à propos des rôles d'administrateur Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) .)         |
|Administrateur de sécurité |Centre d'administration Azure Active Directory[https://aad.portal.azure.com](https://aad.portal.azure.com)()|
|Gestion de l'organisation Exchange Online |Centre d'administration Exchange[https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)() <br>ou <br>  Applets de commande PowerShell (consultez la rubrique [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)) |

> [!TIP]
> Pour en savoir plus sur les rôles et les autorisations, consultez [la rubrique autorisations &amp; dans le centre de sécurité conformité Office 365](permissions-in-the-security-and-compliance-center.md).

Il existe plusieurs types de stratégies ATP à définir et à vérifier régulièrement.

1. **[Configurez des stratégies anti-hameçonnage ATP dans Office 365](set-up-anti-phishing-policies.md)** , notamment des attaques basées sur l'emprunt d'identité pour empêcher les attaquants qui envoient des messages électroniques qui semblent provenir de personnes ou de domaines approuvés. 

2. ConFigurez des **[stratégies de liens fiables ATP dans Office 365](set-up-atp-safe-links-policies.md)** y compris la [liste des URL bloquées personnalisées](set-up-a-custom-blocked-urls-list-wtih-atp.md) de votre organisation et une [liste d'URL «ne pas réécrire» personnalisée](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).
    
3. **[Configurez les stratégies de pièces jointEs approuvéES ATP dans Office 365](set-up-atp-safe-attachments-policies.md)** et choisissez parmi plusieurs options, telles que [remise et aperçu dynamiques](dynamic-delivery-and-previewing.md).
  
## <a name="see-how-atp-is-working-by-viewing-reports"></a>Découvrez le fonctionnement de la fonctionnalité ATP en affichant des rapports

Une fois les stratégies ATP en place, des rapports sont disponibles pour illustrer le fonctionnement du service. (dans le centre de sécurité & de sécurité Office 365, accédez à **rapports** > **Dashboard**.)

[![Le tableau &amp; de bord du centre de sécurité conformité peut vous aider à déterminer le fonctionnement de la protection avancée contre les menaces](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)](view-reports-for-atp.md)
  
1. En tant qu'administrateur général Office 365, administrateur de sécurité ou lecteur de sécurité, accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous.
    
2. Accédez au **** > **tableau de bord**rapports. (Pour obtenir de l'aide sur ces rapports, consultez la rubrique [afficher les rapports pour une protection avancée contre les menaces](view-reports-for-atp.md).)
    
3. Si nécessaire, effectuez des ajustements aux stratégies de sécurité. Pour obtenir de l'aide, consultez les ressources suivantes:
    - [Stratégies anti-hameçonnage ATP](set-up-anti-phishing-policies.md)
    - [Stratégies de liens fiables ATP](set-up-atp-safe-links-policies.md)
    - [Stratégies de pièces jointes approuvées ATP](set-up-atp-safe-attachments-policies.md)
    
    
## <a name="submit-a-suspicious-file-to-microsoft-for-analysis"></a>Envoyer un fichier suspect à Microsoft pour analyse

- Si vous obtenez un fichier dont vous pensez qu'il peut s'agir de programmes malveillants, vous pouvez soumettre ce fichier à Microsoft pour analyse. Visitez le [portail de soumission Windows Defender Security Intelligence](https://go.microsoft.com/fwlink/?linkid=857185).

- Si vous recevez un message électronique (avec ou sans pièce jointe) que vous souhaitez envoyer à Microsoft pour analyse, utilisez le [complément Report message](enable-the-report-message-add-in.md). 
  

