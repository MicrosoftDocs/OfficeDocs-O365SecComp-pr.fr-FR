---
title: Explorateur de menaces (et détections en temps réel)
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 05/22/2019
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
description: Découvrez l’Explorateur (et les détections en temps réel) dans le &amp; Centre de sécurité conformité.
ms.openlocfilehash: 030f866c5e86daa3dc543bddae7152e19f377d3b
ms.sourcegitcommit: 6c0fcb82178a4ac26375545f328389a6852a81be
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2019
ms.locfileid: "34490530"
---
# <a name="threat-explorer-and-real-time-detections"></a>Explorateur de menaces (et détections en temps réel)

Si votre organisation dispose d' [office 365 Advanced Threat Protection](office-365-atp.md) (Office 365 ATP) et que vous disposez [des autorisations nécessaires](#required-licenses-and-permissions), vous disposez de l' **Explorateur** ou des détections **en temps réel** (précédemment des *rapports en temps réel* ) [Voir ](#new-features-in-real-time-detections)nouveautés!). Dans le centre de sécurité & Compliance Center, accédez à **gestion des menaces**, puis choisissez **Explorateur** ou détections **en temps réel**. 

|Avec le plan ATP 2, vous pouvez voir:  |Avec le plan ATP 1, vous pouvez voir:  |
|---------|---------|
|![Explorateur de menaces](media/threatmgmt-explorer.png)      |![Détections en temps réel](media/threatmgmt-realtimedetections.png)         |

Avec l’Explorateur (ou les détections en temps réel), vous disposez d’un puissant rapport qui permet à votre équipe des opérations de sécurité d’examiner et de répondre efficacement aux menaces, et elle ressemble à l’image suivante: 

![Accéder à l’Explorateur \> de gestion des menaces](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)

Ce rapport vous permet d’utiliser les actions suivantes:
- [Voir programmes malveillants détectés par les fonctionnalités de sécurité d’Office 365](#see-malware-detected-in-email-by-technology)
- [Afficher les données sur les URL d’hameçonnage et cliquez sur verdict](#view-data-about-phishing-urls-and-click-verdict)
- [Démarrer un processus d’enquête et de réponse automatisés à partir d’une vue dans l’Explorateur](#start-automated-investigation-and-response) (Plan DAV 2 uniquement)
- ... [Examinez le courrier électronique malveillant, et bien plus encore](#more-ways-to-use-explorer-or-real-time-detections)!

## <a name="new-features-in-real-time-detections"></a>Nouvelles fonctionnalités dans les détections en temps réel

Pour les clients Office 365 DAV plan 1, le rapport de *détection en temps réel* était auparavant appelé *rapports en temps réel*. Outre le changement de nom, plusieurs nouvelles fonctionnalités et améliorations sont déployées:

- Dans la vue hameçonnage, vous pouvez voir plus de détails sur les URL détectées via les [liens fiables ATP](atp-safe-links.md). Les nouveaux détails et fonctionnalités sont les suivants:
  - URL dans les messages électroniques
  - Filtrage basé sur les informations d’URL
  - Informations d’URL affichées dans les graphiques de données
  - Données de temps de clic sur les clics dans les messages

- Chaque fois qu’une modification est apportée à une URL, cliquez sur verdict, une alerte s’affiche. URL cliquez sur les verdicts peuvent changer lorsque la réputation d’une URL modifie la détonation ou lorsqu’un utilisateur protégé par les liens fiables ATP remplace un [avertissement de liens fiables ATP](atp-safe-links-warning-pages.md).  
 
Ces améliorations permettent aux administrateurs de sécurité de votre organisation d’afficher plus de détails qu’avant. Les administrateurs de la sécurité peuvent afficher des informations sur les domaines d’URL, les URL manquées, les verdicts, et bien plus encore, et ajuster les stratégies Office 365 ATP de manière appropriée.

> [!NOTE]
> Bien que ces fonctionnalités soient en aperçu, les données URL seront disponibles pendant un nombre limité de jours. 

## <a name="see-malware-detected-in-email-by-technology"></a>Voir programmes malveillants détectés dans le courrier électronique par technologie

Supposons que vous souhaitez voir les programmes malveillants détectés par les messages électroniques, par la technologie Office 365. Pour ce faire, utilisez la vue [programmes malveillants de messagerie >](threat-explorer-views.md#email--malware) de l’Explorateur (ou détections en temps réel).

1. Dans le centre de sécurité & conformité[https://protection.office.com](https://protection.office.com)(), sélectionnez**Explorateur** de **gestion** > des menaces (ou **détections en temps réel**). (Cet exemple utilise Explorer.)

2. Dans le menu **affichage** , choisissez **** > **programmes malveillants**de messagerie.<br/>![Menu Affichage de l’Explorateur](media/ExplorerViewEmailMalwareMenu.png)<br/>

3. Cliquez sur **expéditeur**, puis choisissez**technologie de détection**de **base** > .<br/>Vos technologies de détection sont désormais disponibles en tant que filtres pour le rapport.<br/>![Technologies de détection des programmes malveillants](media/ExplorerEmailMalwareDetectionTech.png)<br/> 

4. Sélectionnez une option, puis cliquez sur le **** bouton Actualiser pour appliquer ce filtre.<br/>![Technologie de détection sélectionnée](media/ExplorerEmailMalwareDetectionTechATP.png)<br/> 

Le rapport est actualisé pour afficher les résultats de programmes malveillants détectés par courrier électronique, à l’aide de l’option de technologie que vous avez sélectionnée. À partir de là, vous pouvez effectuer une analyse plus poussée.

## <a name="view-data-about-phishing-urls-and-click-verdict"></a>Afficher les données sur les URL d’hameçonnage et cliquez sur verdict

Supposons que vous vouliez voir les tentatives de hameçonnage via des URL dans des e-mails, y compris une liste des URL qui ont été autorisées, bloquées et remplacées. L’identification des URL sur lesquelles l’utilisateur a cliqué requiert la configuration de [liens fiables ATP](atp-safe-links.md) . Assurez-vous que vous avez configuré les [stratégies de liens fiables ATP](set-up-atp-safe-links-policies.md) pour la protection du temps de clic et la journalisation des «verdict de clic» par les liens fiables ATP. 

Pour consulter les URL de hameçonnage dans les messages et les clics sur les URL dans les messages hameçons, utilisez la vue [E-mail _GT_ hameçonnage](threat-explorer-views.md#email--phish) de l’Explorateur (ou détections en temps réel).

1. Dans le centre de sécurité & conformité[https://protection.office.com](https://protection.office.com)(), sélectionnez**Explorateur** de **gestion** > des menaces (ou **détections en temps réel**). (Cet exemple utilise Explorer.)

2. Dans le menu **affichage** , choisissez **courrier** > **hameçon**.<br/>![Menu Affichage de l’Explorateur](media/ExplorerViewEmailPhishMenu.png)<br/>

3. Cliquez sur **expéditeur**, puis sur **URL** > , puis**cliquez sur verdict**.

4. Sélectionnez une ou plusieurs options, telles que **bloquées** et **bloquer le remplacement**, puis cliquez sur le bouton **Actualiser** qui se trouve sur la même ligne que les options pour appliquer le filtre. (Ne pas actualiser la fenêtre de votre navigateur.)<br/>![URL et cliquez sur verdicts](media/ThreatExplorerEmailPhishClickVerdictOptions.png)<br/>

    Le rapport est actualisé pour afficher deux tables d’URL différentes sous l’onglet URL sous le rapport:

   1. Les **URL principales** sont les URL contenues dans les messages que vous avez filtrés vers et l’action de remise de courrier électronique compte pour chaque URL. Dans l’affichage e-mail de hameçonnage, cette liste contient généralement des URL légitimes. Les agresseurs incluent un mélange d’URL correctes et incorrectes dans leurs messages pour essayer de les remettre, mais ils rendent les liens malveillants plus intéressants pour l’utilisateur. Le tableau des URL est trié par nombre total d’e-mails (Remarque: cette colonne n’est pas affichée pour simplifier l’affichage).

   2. Les **clics en haut** sont les liens fiables les URL sur lesquelles l’utilisateur a cliqué, triées par nombre total de clics (cette colonne ne montre pas non plus comment simplifier l’affichage). Nombre total par colonne indique le nombre de liens approuvés cliquez sur nombre de verdicts pour chaque URL sur laquelle vous avez cliqué. Dans la vue e-mail de hameçonnage, il s’agit plus souvent d’URL suspectes ou malveillantes, mais peut inclure des URL propres qui se trouvent dans des messages hameçons. Les clics d’URL sur les liens non justifiés ne s’afficheront pas ici.
   
   Les deux tableaux d’URL affichent les URL les plus fréquentes dans les messages d’hameçonnage par action de remise et par emplacement, et ils affichent des clics d’URL bloqués (ou visités malgré un avertissement) afin que vous puissiez comprendre quels liens incorrects potentiels ont été reçus par les utilisateurs et interagis avec les utilisateurs. À partir de là, vous pouvez effectuer une analyse plus poussée. Par exemple, sous le graphique, vous pouvez voir les URL principales dans les messages électroniques qui ont été bloqués dans l’environnement de votre organisation.
   
   ![URL de l’Explorateur bloquées](media/ExplorerPhishClickVerdictURLs.png)
   
   Sélectionnez une URL pour afficher des informations plus détaillées. Notez que dans la boîte de dialogue de menu volant d’URL, le filtrage des courriers électroniques est supprimé pour vous montrer l’affichage complet de l’exposition de l’URL dans votre environnement. Cela vous permet de filtrer les e-mails de l’Explorateur vers ceux qui vous intéressent, de rechercher des URL spécifiques qui constituent des menaces potentielles, puis de mieux comprendre l’exposition de l’URL dans votre environnement (via la boîte de dialogue détails de l’URL) sans avoir à ajouter de filtres d’URL au Affichage de l’Explorateur lui-même.

## <a name="review-email-messages-reported-by-users"></a>Examiner les messages électroniques signalés par les utilisateurs

Supposons que vous voulez afficher les messages électroniques que les utilisateurs de votre organisation ont signalés comme courriers indésirables, non légitimes ou le hameçonnage à l’aide du [complément de message de rapport pour Outlook et Outlook sur le Web](enable-the-report-message-add-in.md). Pour ce faire, utilisez l’affichage de [messagerie >](threat-explorer-views.md#email--user-reported) de l’Explorateur (ou des détections en temps réel).

1. Dans le centre de sécurité & conformité[https://protection.office.com](https://protection.office.com)(), sélectionnez**Explorateur** de **gestion** > des menaces (ou **détections en temps réel**). (Cet exemple utilise Explorer.)

2. Dans le menu **affichage** , choisissez **e-mail** > **-signalé**par l’utilisateur.<br/>![Menu Affichage de l’Explorateur](media/ExplorerViewMenuEmailUserReported.png)<br/>

3. Cliquez sur **expéditeur**, puis sur**type de rapport**de **base** > .

4. Sélectionnez une option, par exemple **hameçonnage**, puis cliquez sur le **** bouton Actualiser. <br/>![Hameçonnage signalé par l’utilisateur](media/EmailUserReportedReportType.png)<br/> 

Le rapport est actualisé pour afficher les données relatives aux messages électroniques que les personnes de votre organisation ont signalées comme tentatives de hameçonnage. Vous pouvez utiliser ces informations pour effectuer une analyse plus poussée et, si nécessaire, ajuster vos [stratégies anti-hameçonnage ATP](set-up-anti-phishing-policies.md).

## <a name="start-automated-investigation-and-response"></a>Démarrer une enquête et une réponse automatisées

> [!NOTE]
> Les fonctionnalités d’analyse et de réponse automatisées sont disponibles dans **office 365 ATP plan 2** et **Office 365 E5**.

(Nouveau!) L’analyse [et la réponse automatisées](automated-investigation-response-office.md) peuvent permettre à l’équipe de votre équipe de sécurité de gagner du temps et de faire des efforts pour examiner et atténuer les attaques informatiques. En plus de configurer des alertes pouvant déclencher un manuel de sécurité, vous pouvez démarrer un processus d’enquête et de réponse automatisés à partir d’une vue dans l’Explorateur. 

Pour plus d’informations, reportez-vous à l' [exemple: un administrateur de sécurité déclenche une enquête à partir de l’Explorateur](automated-investigation-response-office.md#example-a-security-administrator-triggers-an-investigation-from-threat-explorer).

## <a name="more-ways-to-use-explorer-or-real-time-detections"></a>Autres méthodes d’utilisation de l’Explorateur (ou des détections en temps réel)

Outre les scénarios décrits dans cet article, vous disposez de nombreuses autres options de création de rapports dans l’Explorateur (ou des détections en temps réel). 
- [Rechercher et d’examiner le courrier électronique malveillant qui a été distribué](investigate-malicious-email-that-was-delivered.md)
- [Affichage de fichiers malveillants détectés dans SharePoint Online, OneDrive et Microsoft teams](malicious-files-detected-in-spo-odb-or-teams.md)
- [Obtenir une vue d’ensemble des affichages dans l’Explorateur de menaces (et des détections en temps réel)](threat-explorer-views.md)

## <a name="required-licenses-and-permissions"></a>Licences et autorisations requises

Vous devez disposer de la protection avancée contre les menaces [Office 365](office-365-atp.md) pour obtenir des détections de l’Explorateur ou en temps réel.
- L’Explorateur est inclus dans Office 365 DAV plan 2. 
- Le rapport de détections en temps réel est inclus dans Office 365 DAV plan 1.

Pour afficher et utiliser l’Explorateur ou les détections en temps réel, vous devez disposer des autorisations appropriées, telles que celles accordées à un administrateur de sécurité ou à un lecteur de sécurité. 

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
  
