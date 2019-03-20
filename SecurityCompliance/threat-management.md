---
title: Threat management in the Office 365 Security &amp; Compliance Center
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 9/24/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 0a73d5fa-b2c8-43e7-9ed4-61f0552b1c98
ms.collection:
- M365-security-compliance
description: Utilisez la gestion des menaces pour contrôler et gérer l'accès des appareils mobiles aux données de votre organisation, protéger votre organisation contre la perte de données et protéger les messages entrants et sortants contre les logiciels malveillants et le courrier indésirable. Vous pouvez également utiliser la gestion des menaces pour protéger la réputation de votre domaine et déterminer si les expéditeurs sont ou non usurpés de manière malveillante les comptes de votre domaine.
ms.openlocfilehash: 9c6c39b7edc008c4a44146fac8076897e705b5f5
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693173"
---
# <a name="threat-management-in-the-office-365-security-amp-compliance-center"></a>Threat management in the Office 365 Security &amp; Compliance Center

Utilisez la gestion des menaces pour contrôler et gérer l'accès des appareils mobiles aux données de votre organisation, protéger votre organisation contre la perte de données et protéger les messages entrants et sortants contre les logiciels malveillants et le courrier indésirable. Vous pouvez également utiliser la gestion des menaces pour protéger la réputation de votre domaine et déterminer si les expéditeurs sont ou non usurpés de manière malveillante les comptes de votre domaine.
  
## <a name="how-to-view-and-use-threat-management-in-the-security-amp-compliance-center"></a>Procédure d'affichage et d'utilisation de la gestion des &amp; menaces dans le centre de sécurité conformité

Dans Office 365, utilisez le centre &amp; de sécurité conformité pour gérer les menaces au sein de votre organisation.
  
 **Pour accéder directement au centre de &amp; sécurité conformité, procédez comme suit:**
  
1. Accédez à la page [https://protection.office.com](https://protection.office.com).

2. Connectez-vous à Office 365 à l'aide de votre compte scolaire ou professionnel.

3. Dans le volet gauche, sélectionnez **gestion des menaces**.

    ![Menu de gestion &amp; des menaces du centre de sécurité conformité Office 365](media/dca29ff2-ad6d-4c27-becb-b5947268d55a.png)
  
 **Pour accéder au centre de &amp; sécurité conformité à l'aide du lanceur d'applications Office 365:**
  
1. Connectez-vous à Office 365 à l'aide de votre compte scolaire ou professionnel.

2. Sélectionnez le lanceur ![d'applications icône du lanceur d'](media/7502f4ec-3c9a-435d-a7b4-b9cda85189a7.png) applications dans Office 365 dans le coin supérieur gauche, puis sélectionnez la vignette **conformité de sécurité &amp; ** . 

3. Dans le volet gauche, sélectionnez **gestion des menaces**.

## <a name="about-threat-management-in-office-365"></a>À propos de la gestion des menaces dans Office 365

Ces options sont disponibles sous **gestion des menaces** dans le &amp; Centre de sécurité et de conformité.
  
Nous déployons toujours la gestion des menaces pour le &amp; Centre de sécurité conformité, donc vous ne les verrez peut-être pas encore, ou vous pouvez voir d'autres options que celles répertoriées ici. Pendant le déploiement, certains de ces éléments, tels que les logiciels anti-programme malveillant, DKIM et autres, continueront à être disponibles via le centre d'administration Exchange pour une durée limitée.

Dans certains cas, il existe des différences mineures entre le centre d' &amp; administration Exchange et les implémentations du centre de sécurité conformité. Par exemple, les caractères pris en charge pour les filtres de courrier indésirable sont différents entre les deux plateformes. Les articles fournis fournissent des informations supplémentaires sur les différences spécifiques lorsqu'elles se produisent.
  
|**Outil**|**Description**|
|:-----|:-----|
|**Tableau de bord, Explorateur de menaces et incidents** <br/> |Une fois activés, ces volets vous permettent de gérer l'analyse et l'analyse des menaces Office 365 Analytics, ainsi que la réponse. Pour plus d'informations, consultez la rubrique [Office 365 Advanced Threat Protection Plan 2](office-365-ti.md).  <br/> |
|**Filtrage du courrier** <br/> |Affiner et surveiller les paramètres permettant d'éviter le courrier indésirable dans Office 365. Créez des listes verte et rouge, déterminez les personnes qui usurpent votre domaine et pourquoi, et configurez et affichez les stratégies de filtrage du courrier indésirable. Pour plus d'informations, consultez la rubrique protection contre le courrier indésirable pour les [courriers électroniques Office 365](anti-spam-protection.md).  <br/> Vous pouvez également configurer une stratégie pour vérifier que vos utilisateurs n'envoient pas de courrier indésirable. Cela peut se produire, par exemple, si l'ordinateur d'un utilisateur est infecté par un programme malveillant programmé pour envoyer des messages électroniques. Pour savoir comment empêcher le courrier indésirable sortant, consultez [la rubrique Configurer la stratégie anti-courrier indésirable sortant](https://technet.microsoft.com/library/jj200737%28v=exchg.150%29.aspx).  <br/> Si vous rencontrez actuellement un problème avec le courrier indésirable, vous pouvez utiliser l' [utilitaire de résolution des problèmes de courrier indésirable et de programmes malveillants](https://configure.office.com/Scenario.aspx?sid=73).           |
|**Anti-programme malveillant** <br/> |Protège contre les virus et les logiciels espions circulant vers ou à partir de votre organisation dans Office 365. Les virus sont des programmes logiciels malveillants qui, lorsqu'ils sont exécutés, se répliquent et modifient d'autres programmes et données sur l'ordinateur. Les virus se répandent sur votre ordinateur à la recherche de programmes à infecter et sont également partagés d'un ordinateur à un autre, souvent par courrier électronique. Les logiciels espions recueillent vos informations personnelles, telles que les informations de connexion, et les renvoient à son auteur. Pour commencer à configurer les stratégies anti-programme malveillant, consultez la rubrique [configure anti-malware Policies](https://technet.microsoft.com/library/jj200745%28v=exchg.150%29.aspx).  <br/> Si vous rencontrez actuellement un problème avec un programme malveillant, vous pouvez utiliser l' [utilitaire de résolution des problèmes de courrier indésirable et de programmes malveillants](https://configure.office.com/Scenario.aspx?sid=73).           |
|**DKIM** <br/> |Destiné aux administrateurs Office 365 plus avancés, mais disponible pour tous les clients Office 365, DomainKeys Identified Identified Mail (DKIM) garantit que les autres systèmes de messagerie approuvent les messages que vous envoyez à partir d'Office 365. DKIM effectue cette opération en ajoutant une signature numérique unique aux messages électroniques que vous envoyez à partir de votre organisation. Les systèmes de courrier électronique provenant de vous pouvez utiliser cette signature numérique pour vous aider à déterminer si le courrier électronique est légitime.  <br/> Ne vous inquiétez pas si les détails de cette procédure semblent compliqués, car la valeur par défaut configurée pour vous dans Office 365 doit fonctionner pour la plupart des organisations. Si vous ne configurez pas DKIM vous-même, Office 365 utilise sa stratégie et ses clés par défaut qu'il crée afin d'activer DKIM pour votre domaine. De plus, si vous désactivez la signature DKIM, après un certain temps, Office 365 active automatiquement la stratégie par défaut d'Office 365 pour votre domaine.  <br/> Si vous le souhaitez, vous pouvez afficher cette page dans le &amp; Centre de sécurité et voir si les signatures DKIM sont actuellement activées pour votre domaine et que vous pouvez afficher la dernière fois que les clés de chiffrement utilisées par Office 365 ont été pivotées. Vous pouvez également faire pivoter manuellement les touches vous-même.  <br/> **INDISPENSABLES!** DKIM n'est qu'une technique d'authentification de messagerie utilisée par Office 365. Pour être plus efficace, DKIM est utilisé avec d'autres techniques prises en charge, telles que l'authentification SPF (Sender Policy Framework) et l'authentification, la création de rapports et la conformité des messages basés sur un domaine (DMARC). Ensemble, ces technologies d'authentification basée sur le domaine permettent d'éviter le courrier indésirable et l'usurpation indésirable.<br/>  Avant d'apporter des modifications à DKIM à &amp; l'aide du centre de sécurité conformité, familiarisez-vous avec la technologie et son fonctionnement. Pour commencer, reportez-vous à [la section notions de base: autres méthodes pour empêcher le courrier indésirable dans Office 365](anti-spam-protection.md#beyond-the-basics-more-ways-to-prevent-spam-in-office-365).           |
|**Pièces jointes fiables**<br/>|[Les pièces jointEs fiables](atp-safe-attachments.md) font partie de la protection avancée contre les menaces. Lorsque cette option est activée, les pièces jointes de courrier électronique sont ouvertes dans un environnement isolé et isolé distinct d'Office 365 avant d'être envoyés aux boîtes de réception des destinataires. Les pièces jointes fiables permettent de détecter les pièces jointes malveillantes avant même que les signatures antivirus ne soient disponibles. Pour en savoir plus, consultez la rubrique [pièces jointEs fiables dans Office 365](atp-safe-attachments.md).<br/> |
|**Liens fiables** <br/> |Les [liens fiables](atp-safe-links.md) font partie de la protection avancée contre les menaces. Les liens fiables permettent d'empêcher les utilisateurs de suivre des URL dans des courriers électroniques ou dans des documents Office qui pointent vers des sites Web reconnus comme malveillants. Pour en savoir plus, consultez la rubrique [liens approuvés dans Office 365](atp-safe-links.md).<br/> |
|**Mise en quarantaine**<br/>|ConFigurez la [mise en quarantaine](http://go.microsoft.com/fwlink/p/?LinkID=809005) pour les messages électroniques entrants dans Office 365 où les messages qui ont été filtrés en tant que courrier indésirable, en bloc, de hameçonnage et de programmes malveillants peuvent être conservés à des fins de révision ultérieure. Les utilisateurs et les administrateurs peuvent travailler avec des messages mis en quarantaine. Les utilisateurs peuvent utiliser uniquement leurs propres messages filtrés en quarantaine. Les administrateurs peuvent rechercher et gérer les messages mis en quarantaine pour tous les utilisateurs.  <br/> |
|**Menaces avancées** <br/> |Consultez le [rapport d'état de protection contre les menaces](https://support.office.com/article/View-the-reports-for-Advanced-Threat-Protection-E47E838C-D99E-4C0B-B9AA-E66C4FAE902F#advancedthreats) pour afficher des informations sur le contenu malveillant détecté et bloqué par Exchange Online Protection et la protection avancée contre les menaces.  <br/> |
