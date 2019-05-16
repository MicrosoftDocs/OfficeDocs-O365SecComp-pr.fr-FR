---
title: Utiliser Threat Explorer dans le centre &amp; de sécurité conformité
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/31/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 82ac9922-939c-41be-9c8a-7c75b0a4e27d
ms.collection:
- M365-security-compliance
description: Découvrez l’Explorateur (également appelé Explorateur de menaces) dans le &amp; Centre de sécurité conformité.
ms.openlocfilehash: 30f3759b6eb35508a9de8c03abb72562417aa04f
ms.sourcegitcommit: 0d5a863f48914eeaaf29f7d2a2022618de186247
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "34077330"
---
# <a name="use-threat-explorer-in-the-security-amp-compliance-center"></a>Utiliser Threat Explorer dans le centre &amp; de sécurité conformité

Si votre organisation dispose d' [Office 365 Advanced Threat Protection Plan 2](office-365-ti.md) (ATP) et que vous disposez des autorisations nécessaires, vous pouvez utiliser l’Explorateur de menaces (également appelé Explorateur) pour identifier et analyser les menaces. (Pour utiliser l’Explorateur, dans le &amp; Centre de sécurité conformité, accédez à l' **Explorateur**de **gestion** \> des menaces.)

![Accéder à l’Explorateur \> de gestion des menaces](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)

Explorer est un outil puissant, quasiment en temps réel, qui permet aux équipes des opérations de sécurité d’examiner et de &amp; répondre aux menaces dans le centre de sécurité conformité. Voici quelques-unes des actions que vous pouvez effectuer:
- [Voir programmes malveillants détectés par les fonctionnalités de sécurité d’Office 365](#see-malware-detected-in-email-by-technology)
- [Afficher les données sur les URL d’hameçonnage et cliquez sur verdict](#view-data-about-phishing-urls-and-click-verdict)
- [Démarrer un processus d’enquête et de réponse automatisés à partir d’une vue dans l’Explorateur](#start-automated-investigation-and-response)
- ... [et bien plus encore](#more-ways-to-use-explorer)!

## <a name="see-malware-detected-in-email-by-technology"></a>Voir programmes malveillants détectés dans le courrier électronique par technologie

Supposons que vous vouliez voir les programmes malveillants détectés dans les messages électroniques et la technologie dans Office 365. Pour ce faire, utilisez la vue [programmes malveillants de messagerie >](threat-explorer-views.md#email--malware) de l’Explorateur.

1. Dans le centre de sécurité & Compliance[https://protection.office.com](https://protection.office.com)Center (), sélectionnez **Threat Management** > **Explorer**.
2. Dans le menu **affichage** , choisissez **** > **programmes malveillants**de messagerie.<br/>![Menu Affichage de l’Explorateur](media/ExplorerViewEmailMalwareMenu.png)<br/>
3. Cliquez sur **expéditeur**, puis choisissez**technologie de détection**de **base** > .<br/>Vos technologies de détection sont désormais disponibles en tant que filtres pour le rapport.<br/>![Technologies de détection des programmes malveillants](media/ExplorerEmailMalwareDetectionTech.png)<br/> 
4. Sélectionnez une option, puis cliquez sur le bouton Actualiser pour appliquer ce filtre.<br/>![Technologie de détection sélectionnée](media/ExplorerEmailMalwareDetectionTechATP.png)<br/> 

Le rapport est actualisé pour afficher les résultats de programmes malveillants détectés par courrier électronique, à l’aide de l’option de technologie que vous avez sélectionnée. À partir de là, vous pouvez effectuer une analyse plus poussée.

## <a name="view-data-about-phishing-urls-and-click-verdict"></a>Afficher les données sur les URL d’hameçonnage et cliquez sur verdict

Supposons que vous vouliez voir les tentatives de hameçonnage via des URL dans des courriers électroniques, y compris une liste des URL qui ont été autorisées, bloquées et remplacées.  L’identification des URL sur lesquelles l’utilisateur a cliqué requiert [des liens fiables ATP](atp-safe-links.md). (Assurez-vous que vous avez configuré et appliqué des [stratégies de liens fiables ATP](set-up-atp-safe-links-policies.md) à vos utilisateurs pour la protection de la période de clic et la journalisation des verdicts de clic par des liens fiables ATP.) Pour consulter les URL de hameçonnage dans les messages et les clics sur les URL dans les messages hameçons, utilisez la vue [E-mail _GT_ hameçonnage](threat-explorer-views.md#email--phish) de l’Explorateur.

1. Dans le centre de sécurité & Compliance[https://protection.office.com](https://protection.office.com)Center (), sélectionnez **Threat Management** > **Explorer**.
2. Dans le menu **affichage** , choisissez **courrier** > **hameçon**.<br/>![Menu Affichage de l’Explorateur](media/ExplorerViewEmailPhishMenu.png)<br/>
3. Cliquez sur **expéditeur**, puis sur **URL** > , puis**cliquez sur verdict**.
4. Sélectionnez une ou plusieurs options, telles que **bloquée** et **bloquer le remplacement**, puis cliquez sur le bouton **Actualiser** pour appliquer ce filtre.<br/>![URL et cliquez sur verdicts](media/ThreatExplorerEmailPhishClickVerdictOptions.png)<br/>

Le rapport est actualisé pour afficher deux tables d’URL différentes sous l’onglet URL ci-dessous:
1. Les **URL principales** sont les URL contenues dans les messages que vous avez filtrés vers et l’action de remise de courrier électronique compte pour chaque URL. Dans l’affichage e-mail de hameçonnage, cette liste contient généralement des URL légitimes. Les agresseurs incluent un mélange d’URL correctes et incorrectes dans leurs messages pour essayer de les remettre, mais ils rendent les liens malveillants plus intéressants pour l’utilisateur. Le tableau des URL est trié par nombre total d’e-mails (Remarque: cette colonne n’est pas affichée pour simplifier l’affichage).
2. Les **clics en haut** sont les liens fiables les URL sur lesquelles l’utilisateur a cliqué, triées par nombre total de clics (cette colonne ne montre pas non plus comment simplifier l’affichage). Nombre total par colonne indique le nombre de liens approuvés cliquez sur nombre de verdicts pour chaque URL sur laquelle vous avez cliqué. Dans la vue e-mail de hameçonnage, il s’agit plus souvent de liens suspects ou malveillants, mais peut inclure des URL propres qui se trouvent dans des messages hameçons. Les clics d’URL sur les liens non justifiés ne s’afficheront pas ici.

Les deux tableaux d’URL affichent les URL les plus populaires dans les messages d’hameçonnage par État de remise et ils affichent des clics d’URL bloqués (ou visités malgré un avertissement) afin que vous puissiez comprendre quels liens incorrects potentiels ont été reçus par les utilisateurs et interagis avec les utilisateurs. À partir de là, vous pouvez effectuer une analyse plus poussée. Par exemple, sous le graphique, vous pouvez voir les URL principales dans les messages électroniques qui ont été bloqués dans l’environnement de votre organisation. 

![URL de l’Explorateur bloquées](media/ExplorerPhishClickVerdictURLs.png) 

Sélectionnez une URL pour afficher des informations plus détaillées. Notez que dans la boîte de dialogue de menu volant d’URL, le filtrage des courriers électroniques est supprimé afin de vous montrer l’affichage complet de l’exposition de l’URL dans votre environnement. Cela vous permet de filtrer les e-mails de l’Explorateur vers ceux qui vous intéressent, de rechercher des URL spécifiques qui constituent des menaces potentielles, puis de mieux comprendre l’exposition de l’URL dans votre environnement (via la boîte de dialogue détails de l’URL) sans avoir à ajouter de filtres d’URL au Affichage de l’Explorateur lui-même.

## <a name="review-email-messages-reported-by-users"></a>Examiner les messages électroniques signalés par les utilisateurs

Supposons que vous voulez voir les messages électroniques que les utilisateurs de votre organisation ont signalés comme courriers indésirables, non légitimes ou le hameçonnage à l’aide du [complément de message de rapport pour Outlook et Outlook sur le Web](enable-the-report-message-add-in.md). Pour ce faire, utilisez la vue de [messagerie >](threat-explorer-views.md#email--user-reported) de l’Explorateur signalée par l’utilisateur.

1. Dans le centre de sécurité & Compliance[https://protection.office.com](https://protection.office.com)Center (), sélectionnez **Threat Management** > **Explorer**.
2. Dans le menu **affichage** , choisissez **e-mail** > **-signalé**par l’utilisateur.<br/>![Menu Affichage de l’Explorateur](media/ExplorerViewMenuEmailUserReported.png)<br/>
3. Cliquez sur **expéditeur**, puis sur**type de rapport**de **base** > .
4. Sélectionnez une option, par exemple **hameçonnage**, puis cliquez sur le **** bouton Actualiser. <br/>![Hameçonnage signalé par l’utilisateur](media/EmailUserReportedReportType.png)<br/> 

Le rapport est actualisé pour afficher les données relatives aux messages électroniques que les personnes de votre organisation ont signalées comme tentatives de hameçonnage. Vous pouvez utiliser ces informations pour effectuer une analyse plus poussée et, si nécessaire, ajuster vos [stratégies anti-hameçonnage ATP](set-up-anti-phishing-policies.md).

## <a name="start-automated-investigation-and-response"></a>Démarrer une enquête et une réponse automatisées

(Nouveau!) L’analyse [et la réponse automatisées](automated-investigation-response-office.md), récemment ajoutées au plan ATP 2, permettent d’enregistrer votre équipe de gestion des opérations de sécurité beaucoup de temps et d’efforts pour examiner et atténuer les attaques informatiques. En plus de configurer des alertes pouvant déclencher un manuel de sécurité, vous pouvez démarrer un processus d’enquête et de réponse automatisés à partir d’une vue dans l’Explorateur. 

Pour plus d’informations, reportez-vous à l' [exemple: un administrateur de sécurité déclenche une enquête à partir de l’Explorateur de menaces](automated-investigation-response-office.md#example-a-security-administrator-triggers-an-investigation-from-threat-explorer).

## <a name="more-ways-to-use-explorer"></a>Autres méthodes d’utilisation de l’Explorateur

Outre les scénarios décrits dans cet article, vous disposez de nombreuses autres options de création de rapports disponibles dans l’Explorateur. 
- [Rechercher et d’examiner le courrier électronique malveillant qui a été distribué](investigate-malicious-email-that-was-delivered.md)
- [Affichage de fichiers malveillants détectés dans SharePoint Online, OneDrive et Microsoft teams](malicious-files-detected-in-spo-odb-or-teams.md)
- [Obtenir une vue d’ensemble des affichages dans l’Explorateur de menaces](threat-explorer-views.md)

## <a name="required-licenses-and-permissions"></a>Licences et autorisations requises

L’Explorateur est inclus dans [Office 365 Advanced Threat Protection Plan 2](office-365-ti.md). 

Pour afficher et utiliser l’Explorateur, vous devez disposer des autorisations appropriées, telles que celles accordées à un administrateur de sécurité ou à un lecteur de sécurité. 

- Pour le centre &amp; de sécurité conformité, vous devez disposer de l’un des rôles suivants:
    - Gestion de l’organisation
    - Administrateur de la sécurité (qui peut être affecté dans le centre d’administration Azure[https://aad.portal.azure.com](https://aad.portal.azure.com)Active Directory ())
    - Lecteur de sécurité

- Pour Exchange Online, vous devez disposer de l’un des rôles suivants, qui est affecté dans le centre[https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)d’administration Exchange () ou avec des applets de commande PowerShell (consultez la rubrique [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)):
    - Gestion de l’organisation
    - Gestion de l’organisation en affichage seul
    - Rôle Destinataires en affichage uniquement
    - Gestion de la conformité

Pour en savoir plus sur les rôles et les autorisations, consultez les ressources suivantes:

- [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md)

- [Autorisations des fonctionnalités dans Exchange Online](https://docs.microsoft.com/exchange/permissions-exo/feature-permissions)
  
