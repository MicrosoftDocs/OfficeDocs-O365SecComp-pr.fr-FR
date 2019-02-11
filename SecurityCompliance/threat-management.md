---
title: Threat management in the Office 365 Security &amp; Compliance Center
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 9/24/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 0a73d5fa-b2c8-43e7-9ed4-61f0552b1c98
description: Gestion des menaces permet de contrôler et de gérer l’accès d’appareil mobile aux données de votre organisation, de protéger votre organisation contre la perte de données et protéger les messages entrants et sortants à partir du courrier indésirable et les logiciels malveillants. Vous utilisez également threat management pour protéger la réputation de votre domaine et pour déterminer si les expéditeurs sont à des fins malveillantes usurpation de comptes à partir de votre domaine.
ms.openlocfilehash: fc7d0a3fd73c03e6eec6cfd265edbf3c47ce1803
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29652249"
---
# <a name="threat-management-in-the-office-365-security-amp-compliance-center"></a>Threat management in the Office 365 Security &amp; Compliance Center

Gestion des menaces permet de contrôler et de gérer l’accès d’appareil mobile aux données de votre organisation, de protéger votre organisation contre la perte de données et protéger les messages entrants et sortants à partir du courrier indésirable et les logiciels malveillants. Vous utilisez également threat management pour protéger la réputation de votre domaine et pour déterminer si les expéditeurs sont à des fins malveillantes usurpation de comptes à partir de votre domaine.
  
## <a name="how-to-view-and-use-threat-management-in-the-security-amp-compliance-center"></a>Comment afficher et utiliser la gestion des menaces de sécurité &amp; centre de conformité

Dans Office 365, utilisez la sécurité &amp; centre de conformité pour gérer les menaces au sein de votre organisation.
  
 **Pour accéder directement à la sécurité &amp; centre de conformité :**
  
1. Accédez à la page [https://protection.office.com](https://protection.office.com).

2. Connectez-vous à Office 365 à l'aide de votre compte scolaire ou professionnel.

3. Dans le volet gauche, sélectionnez **Gestion des menaces**.

    ![Sécurité Office 365 &amp; menu Gestion de menace de centre de conformité](media/dca29ff2-ad6d-4c27-becb-b5947268d55a.png)
  
 **Pour accéder à la sécurité &amp; centre de conformité à l’aide du lancement d’application Office 365 :**
  
1. Connectez-vous à Office 365 à l'aide de votre compte scolaire ou professionnel.

2. Sélectionnez le lancement d’application ![l’icône de lancement d’application dans Office 365](media/7502f4ec-3c9a-435d-a7b4-b9cda85189a7.png) dans le coin supérieur gauche d’angle, puis sélectionnez le **sécurité &amp; conformité** mosaïque. 

3. Dans le volet gauche, sélectionnez **Gestion des menaces**.

## <a name="about-threat-management-in-office-365"></a>La gestion des menaces dans Office 365

Ces options sont disponibles sous **Gestion des menaces** de sécurité &amp; centre de conformité.
  
Nous sommes toujours présentant gestion des menaces pour la sécurité &amp; centre de conformité, afin que vous ne voyez pas tous ces encore, ou vous pouvez voir que plusieurs options répertoriés ici. Au cours du déploiement, certains d'entre eux, par exemple anti-programme malveillant, Dkim et autres, continuera à être disponible via le centre d’administration Exchange (EAC) pour une durée limitée.

Dans certains cas, il existe des différences mineures entre la sécurité et le CAE &amp; implémentations de centre de conformité. Par exemple, les caractères pris en charge pour les filtres de courrier indésirable sont différents entre les deux plateformes. Les articles sont autant qui fournissent des informations supplémentaires sur les différences spécifiques lorsqu’elles se produisent.
  
|**Outil**|**Description**|
|:-----|:-----|
|**Tableau de bord, Threat explorer et Incidents** <br/> |Une fois activée, ces volets permettent de gérer Office 365 Analytique et menace aide à la décision. Pour plus d’informations, voir [vue d’ensemble des menaces Office 365](office-365-ti.md).<br/> |
|**Filtrage du courrier** <br/> |Ajuster et contrôler les paramètres qui permettent d’éviter le courrier indésirable dans Office 365. Créer autoriser et bloquer des listes, déterminer qui est l’usurpation d’identité votre domaine et pourquoi et la configuration et afficher les stratégies de filtrage du courrier indésirable. Pour plus d’informations, consultez la rubrique [protection contre le courrier indésirable de messagerie Office 365](anti-spam-protection.md).<br/> Vous pouvez également définir une stratégie pour vérifier que vos utilisateurs n’envoient du courrier indésirable. Cela peut se produire, par exemple, si l’ordinateur d’un utilisateur obtient infecté par programme malveillant est programmé pour envoyer des messages électroniques. Pour savoir comment vous pouvez empêcher le courrier indésirable sortant, voir [configurer la stratégie anti-courrier indésirable sortant](https://technet.microsoft.com/library/jj200737%28v=exchg.150%29.aspx).<br/> Si vous rencontrez un problème avec le courrier indésirable, vous pouvez utiliser la [résolution des problèmes de courrier indésirable et les programmes malveillants](https://configure.office.com/Scenario.aspx?sid=73).           |
|**Ant-programme malveillant** <br/> |Protège contre les virus et logiciels espions envoyés vers ou à partir de votre organisation dans Office 365. Virus sont malveillants logiciel de programmes qui, lorsqu’elle est exécutée, se répliquer et modifier d’autres programmes et des données sur l’ordinateur. Virus répartis dans votre ordinateur que vous recherchez des programmes d’infection et sont également partagés d’un ordinateur à un autre, souvent par courrier électronique. Les logiciels espions rassemble des informations personnelles, telles que les informations de connexion et l’envoie à son auteur. Pour commencer la configuration de stratégies anti-programme malveillant, consultez [configurer les stratégies anti-programme malveillant](https://technet.microsoft.com/library/jj200745%28v=exchg.150%29.aspx).<br/> Si vous rencontrez un problème avec les programmes malveillants, vous pouvez utiliser la [résolution des problèmes de courrier indésirable et les programmes malveillants](https://configure.office.com/Scenario.aspx?sid=73).           |
|**DKIM** <br/> |Prévu pour les administrateurs Office 365 plus avancées, mais disponibles pour tous les clients Office 365, DomainKeys DKIM (Identified Mail) permet de garantir que les autres systèmes de messagerie électronique approuvent les messages envoyés à partir d’Office 365. DKIM effectue cette action en ajoutant une signature numérique unique pour les messages électroniques envoyés à partir de votre organisation. Systèmes de messagerie recevoir du courrier électronique vous pouvant utiliser cette signature numérique pour aider à déterminer si le message est légitime.<br/> Ne vous inquiétez pas si les détails de fonctionnement semblent complexes, car la valeur par défaut qui est configuré pour vous dans Office 365 doit utiliser pour la plupart des organisations. Si vous ne définissez pas les DKIM vous-même, Office 365 utilise sa stratégie par défaut et les clés qu’il crée afin d’activer DKIM pour votre domaine. En outre, si vous désactivez la signature DKIM, après un certain temps, Office 365 active automatiquement la stratégie par défaut de Office 365 pour votre domaine.<br/> Si vous le souhaitez, vous pouvez afficher cette page dans la sécurité &amp; centre de conformité et de voir ou non des signatures DKIM sont actuellement activés pour votre domaine et que vous pouvant afficher la dernière fois que les clés de chiffrement utilisés par Office 365 ont été paysage. Vous pouvez également faire pivoter manuellement les clés de vous-même.<br/> **IMPORTANT !** DKIM est la technique d’authentification de courrier électronique qu’un seul utilisé par Office 365. Pour être plus efficace, DKIM est utilisé conjointement avec d’autres techniques pris en charge comme Framework SPF (Sender Policy) et d’authentification basé sur le domaine, création de rapports et conformité (DMARC). Ensemble, ces technologies de l’authentification basée sur le domaine éviter le courrier indésirable et l’usurpation d’identité indésirables.<br/>  Avant d’apporter des modifications à DKIM à l’aide de la sécurité &amp; centre de conformité, maîtrisez la technologie et son fonctionnement. Pour commencer, consultez la rubrique [Aller : plusieurs manières afin d’éviter le courrier indésirable dans Office 365](anti-spam-protection.md#beyond-the-basics-more-ways-to-prevent-spam-in-office-365).           |
|**Pièces jointes fiables**<br/>|[Pièces jointes sûres](atp-safe-attachments.md) fait partie de la protection contre les menaces avancées. Lorsqu’il est activé, les pièces jointes sont ouverts dans un environnement isolé spécial qui est distinct de Office 365 avant de les envoyer à la boîte de réception des destinataires. Pièces jointes sûres est conçu pour détecter les pièces jointes malveillants avant même que les signatures de virus sont disponibles. Pour plus d’informations, voir [Les pièces jointes fiables dans Office 365](atp-safe-attachments.md).<br/> |
|**Liens fiables** <br/> |[Liens approuvés](atp-safe-links.md) fait partie de protection contre les menaces avancées. Liens approuvés d’empêcher les utilisateurs à partir des URL suivantes dans le message électronique ou dans les documents Office qui pointent vers les sites web qui sont reconnus comme malveillants. Pour plus d’informations, voir [Les liens sécurisés dans Office 365](atp-safe-links.md).<br/> |
|**Mise en quarantaine**<br/>|Configurer la [mise en quarantaine](http://go.microsoft.com/fwlink/p/?LinkID=809005) pour les messages électroniques entrants dans Office 365 dans lequel les messages qui ont été filtrés comme courrier indésirable, en bloc, phishing, et programmes malveillants messagerie peut être conservée pour consultation ultérieure. Utilisateurs et administrateurs peuvent travailler avec des messages mis en quarantaine. Les utilisateurs peuvent utiliser uniquement leurs propres messages filtrés en quarantaine. Administrateurs peuvent rechercher et gérer les messages mis en quarantaine pour tous les utilisateurs.<br/> |
|**Menaces avancées** <br/> |Afficher le [rapport d’état de Protection de menace](https://support.office.com/article/View-the-reports-for-Advanced-Threat-Protection-E47E838C-D99E-4C0B-B9AA-E66C4FAE902F#advancedthreats) pour afficher des informations sur le contenu malveillant trouvé et bloqués par Exchange Online Protection et de protection contre les menaces avancées.  <br/> |
