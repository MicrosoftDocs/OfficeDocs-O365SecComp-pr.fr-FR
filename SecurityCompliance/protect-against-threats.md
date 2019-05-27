---
title: Se protéger contre les menaces dans Office 365
ms.author: tracyp
author: msfttracyp
manager: laurawi
audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Normal
ms.date: 05/09/2019
search.appverid:
- MOE150
- MET150
ms.assetid: b10023f6-f30f-45d3-b3ad-b71aa4aa0d58
ms.collection:
- M365-security-compliance
description: Utilisez cet article pour configurer vos fonctionnalités de protection contre les menaces dès maintenant.
ms.openlocfilehash: a9a2baccb4709b3e8d77f620281458d51ed0583a
ms.sourcegitcommit: 2b46fba650df8d252b1dd2b3c3f080a383183a06
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/23/2019
ms.locfileid: "34408389"
---
# <a name="protect-against-threats-in-office-365"></a>Se protéger contre les menaces dans Office 365

Office 365 inclut diverses fonctionnalités de protection contre les menaces. Voici un guide de démarrage rapide que vous pouvez utiliser comme liste de vérification pour vous assurer que les fonctionnalités de protection contre les menaces sont configurées pour votre organisation. Si vous ne connaissez pas les fonctionnalités de protection contre les menaces dans Office 365, ou si vous n’êtes pas sûr de savoir où commencer, utilisez les instructions suivantes comme point de départ. 

> [!IMPORTANT]
> Les **paramètres recommandés initiaux sont inclus pour chaque type de stratégie; Toutefois, de nombreuses options sont disponibles et vous pouvez ajuster vos paramètres afin de répondre aux besoins spécifiques de votre organisation**. Accordez environ 30 minutes à vos stratégies ou modifications pour qu’elles fonctionnent dans votre centre de centres de travail.

## <a name="requirements"></a>Configuration requise

### <a name="subscriptions"></a>Abonnements

Les fonctionnalités de protection contre les menaces sont incluses dans tous les abonnements Office 365; Toutefois, certains abonnements incluent des fonctionnalités plus avancées. Le tableau suivant répertorie les fonctionnalités de protection incluses dans cet article, ainsi que les conditions minimales requises en matière d’abonnement.<br/>

|Type de protection  |Conditions requises en matière d’abonnement  |
|---------|---------|
|Protection anti-programme malveillant    | [Exchange Online Protection](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description) EOP        |
|Protection contre les URL et les fichiers malveillants dans les e-mails et les documents Office    | [Office 365 protection avancée contre les menaces](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description) CUMULÉ       |
|Protection anti-hameçonnage    | [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description)      |
|Protection avancée contre le hameçonnage    | [Office 365 ATP](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)   |
|Protection anti-courrier indésirable     | [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description)       |
|Purge automatique avec zéro heure (pour la messagerie électronique)    | [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description) EOP        |
|Journalisation d’audit (utilisé à des fins de création de rapports)    | [Exchange Online](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description)        |

### <a name="roles-and-permissions"></a>Rôles et autorisations

Vous devez disposer d’un rôle approprié pour configurer les stratégies dans le [Centre de sécurité _AMP_ Compliance Center](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center). Le tableau suivant contient des exemples: 

|Rôle ou groupe de rôles  |Où en savoir plus  |
|---------|---------|
|Administrateur général Office 365 |[À propos des rôles d'administrateur Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles)|
|Administrateur de sécurité |[Autorisations de rôle d’administrateur dans Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/directory-assign-admin-roles)|
|Gestion de l’organisation Exchange Online |[Autorisations dans Exchange Online](https://docs.microsoft.com/en-us/exchange/permissions-exo/permissions-exo) <br>et<br> [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)|

Pour en savoir plus, consultez [la rubrique autorisations dans le &amp; Centre de sécurité conformité Office 365](permissions-in-the-security-and-compliance-center.md).

## <a name="part-1---anti-malware-protection"></a>Partie 1: protection anti-programme malveillant

La [protection contre les programmes malveillants](anti-malware-protection.md) est disponible dans les abonnements incluant [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description). 

1. Dans le [Centre de sécurité & conformité](https://protection.office.com), choisissez**protection contre les programmes malveillants**pour la**stratégie** > de **gestion** > des menaces.

2. Double-cliquez sur la stratégie **par défaut** , puis sélectionnez **paramètres**.

3. Spécifiez les paramètres suivants:

    - Dans la section réponse à la **détection de programmes malveillants** , conservez le paramètre par défaut **non**.

    - Dans la section **filtre de types de pièces jointes courantes** , choisissez **activé**.

4. Cliquez sur **Enregistrer**.

Pour en savoir plus sur les options de stratégie anti-programme malveillant, consultez la rubrique [configure anti-malware Policies](configure-anti-malware-policies.md).

## <a name="part-2---protection-from-malicious-urls-and-files"></a>Partie 2-protection contre les URL et fichiers malveillants

La protection du temps de clic à partir d’URL et de fichiers malveillants est disponible dans les abonnements incluant [Office 365 ATP](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description) (ATP) et configurés par le biais de [pièces jointes approuvées ATP](atp-safe-attachments.md) et des stratégies de [liens fiables ATP](atp-safe-links.md) .

### <a name="atp-safe-attachments-policies"></a>Stratégies de pièces jointes approuvées ATP

Pour configurer des [pièces jointes sûres ATP](atp-safe-attachments.md), vous devez définir au moins une stratégie de pièces jointes approuvées ATP. 

1. Dans le [Centre de sécurité & Compliance Center](https://protection.office.com), choisissez protection**** > **contre les** **menaces** > pièces jointes ATP.

2. Sélectionnez l’option Activer la protection avancée contre **les menaces pour SharePoint, OneDrive et Microsoft teams**.

3. Dans la section **protéger les pièces jointes** , cliquez sur le**+** signe plus ().

4. Spécifiez les paramètres suivants:

    - Dans la zone **nom** , tapez `Block malware`.

    - Dans la section réponse, sélectionnez **bloquer**.

    - Dans la section **pièce jointe** de redirection, sélectionnez l’option Activer la redirection, puis spécifiez l’adresse de messagerie de l’administrateur ou de l’opérateur de sécurité de votre organisation qui analysera les fichiers détectés. ****

    - Dans la section **appliqué à** , choisissez **le domaine du destinataire**. Sélectionnez votre domaine, choisissez **Ajouter**, puis cliquez sur **OK**.

5. Cliquez sur **Enregistrer**.

6. (**Étape supplémentaire recommandée**) En tant qu’administrateur général ou administrateur SharePoint Online, exécutez la cmdlet **[Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** avec le paramètre **DisallowInfectedFileDownload** défini sur *true* pour votre environnement Office 365. (Cela empêche les personnes d’ouvrir, de transférer, de copier ou de partager des fichiers détectés comme malveillants.)  

Pour en savoir plus, consultez la rubrique [configurer des stratégies de pièces jointes approuvées ATP office 365](set-up-atp-safe-attachments-policies.md) et [activer Office 365 ATP pour SharePoint, OneDrive et Microsoft teams](turn-on-atp-for-spo-odb-and-teams.md).

### <a name="atp-safe-links-policies"></a>Stratégies de liens fiables ATP

Pour configurer [des liens approuvés ATP](atp-safe-links.md), vérifiez et modifiez votre stratégie par défaut, puis ajoutez une stratégie pour des utilisateurs spécifiques.

1. Dans le [Centre de sécurité & conformité](https://protection.office.com), **sélectionnez gestion** > **** > **des menaces-liens fiables ATP**.

2. Double-cliquez sur la stratégie **par défaut** .

3. Dans la section **utiliser les liens approuvés dans** , sélectionnez l’option **Office 365 ProPlus, Office pour iOS et Android**, puis cliquez sur **Enregistrer**.

4. Dans la section **stratégies qui s’appliquent à des destinataires spécifiques** , cliquez**+** sur le signe plus ().

5. Spécifiez les paramètres suivants:

    - Dans la zone **nom** , tapez un nom, tel que `Safe Links`.

    - Dans la section **Sélectionnez l’action** , choisissez **activé**.

    - Sélectionnez les options suivantes:

        - **Utiliser les pièces jointes fiables pour analyser le contenu téléchargeable** 

        - **Appliquer des liens fiables aux messages électroniques envoyés au sein de l’Organisation**

        - **Ne pas autoriser les utilisateurs à cliquer sur les liens fiables vers l’URL d’origine**

    - Dans la section **appliqué à** , choisissez **le domaine du destinataire**. Sélectionnez votre domaine, choisissez **Ajouter**, puis cliquez sur **OK**.

6. Cliquez sur **Enregistrer**.

Pour plus d’informations, reportez-vous à la rubrique [set up Office 365 ATP Safe Links Policies](set-up-atp-safe-links-policies.md). 

## <a name="part-3---anti-phishing-protection"></a>Partie 3: protection anti-hameçonnage

La [protection anti-hameçonnage](anti-phishing-protection.md) est disponible dans les abonnements incluant [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description). La protection avancée contre le hameçonnage est disponible dans [](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)la protection avancée contre les menaces. La procédure suivante décrit comment configurer une stratégie anti-hameçonnage ATP. Les étapes sont similaires pour la configuration d’une stratégie anti-hameçonnage (sans ATP).

1. Dans le [Centre de sécurité & Compliance Center](https://protection.office.com), sélectionnez **Threat Management** > **Policy** > **protection contre le hameçonnage**.

2. Cliquez sur **stratégie par défaut**.

3. Dans la section **emprunt d’identité** , cliquez sur **modifier**, puis spécifiez les paramètres suivants:

    - Sous l’onglet **Ajouter des utilisateurs à protéger** , activez la protection. Ajoutez ensuite des utilisateurs, tels que les membres du tableau de bord de votre organisation, votre directeur général, votre directeur financier et d’autres dirigeants. (Vous pouvez taper une adresse de messagerie individuelle ou cliquer pour afficher une liste.)

    - Dans l’onglet **Ajouter des domaines à protéger** , activez **la fonction inclure automatiquement les domaines dont je suis propriétaire**. Si vous avez des domaines personnalisés, ajoutez-les également.

    - Sous l’onglet **actions** , sélectionnez **déplacer le message vers les dossiers** de courrier indésirable des destinataires pour les utilisateurs empruntés et les domaines empruntés, puis activez les conseils de sécurité.

    - Sous l’onglet **intelligence des boîtes aux lettres** , assurez-vous que l’intelligence des boîtes aux lettres est activée.

    - Dans l’onglet **vérifier vos paramètres** , une fois que vous avez vérifié vos paramètres, cliquez sur **Enregistrer**.

4. Dans la section **usurpation** , cliquez sur **modifier**, puis spécifiez les paramètres suivants:

    - Dans l’onglet **paramètres du filtre d’usurpation d’identité** , assurez-vous que la protection contre l’usurpation d’identité est activée.

    - Sous l’onglet **actions** , choisissez déplacer le message vers les dossiers de courrier indésirable des destinataires.

    - Dans l’onglet **vérifier vos paramètres** , une fois que vous avez vérifié vos paramètres, cliquez sur **Enregistrer**. (Si vous n’avez apporté aucune modification, cliquez sur **Annuler**.)

5. Fermez la page Paramètres de stratégie par défaut.

Pour en savoir plus sur les options de stratégie anti-hameçonnage, consultez la rubrique [configurer des stratégies anti-hameçonnage](set-up-anti-phishing-policies.md).

## <a name="part-4---anti-spam-protection"></a>Partie 4: protection contre le courrier indésirable

La [protection contre le courrier](anti-spam-protection.md) indésirable est disponible dans les abonnements incluant [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description).

1. Dans le [Centre de sécurité & conformité](https://protection.office.com), choisissez**protection contre le courrier**indésirable pour la**stratégie** > de **gestion** > des menaces.

2. Sous l’onglet **personnalisé** , activez les **paramètres personnalisés** .

3. Développez **stratégie de filtrage du courrier indésirable par défaut**, cliquez sur **modifier la stratégie**, puis spécifiez les paramètres suivants:

    - Dans la section **actions de courrier indésirable et en bloc** , définissez le seuil sur une valeur de 5 ou 6.

    - Dans la section **autoriser les listes** , vérifiez (et si nécessaire, modifiez) vos expéditeurs et domaines autorisés.

4. Cliquez sur **Enregistrer**.

Pour en savoir plus sur les options de votre stratégie de blocage du courrier indésirable, consultez [la rubrique Configurer les stratégies anti-courrier](configure-the-anti-spam-policies.md)indésirable.

## <a name="part-5---additional-settings-to-configure"></a>Partie 5: paramètres supplémentaires à configurer

En plus de la configuration de la protection contre les programmes malveillants, les URL et les fichiers malveillants, le hameçonnage et le courrier indésirable, nous vous recommandons de configurer vos paramètres de purge automatique et de journalisation de l’heure zéro.

### <a name="zero-hour-auto-purge-for-email"></a>Purge automatique à zéro heure pour le courrier électronique

[Purge automatique avec zéro heure](zero-hour-auto-purge.md) (ZAP) est disponible dans les abonnements qui incluent [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description). Cette protection est activée par défaut; Toutefois, les conditions suivantes doivent être remplies pour que la protection soit appliquée:

- Les actions de courrier indésirable sont définies pour **déplacer le message vers le dossier** courrier indésirable des [stratégies de blocage du courrier](anti-spam-protection.md)indésirable.

- Les utilisateurs ont conservé leurs [paramètres](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md)de courrier indésirable par défaut et n’ont pas désactivé la protection contre le courrier indésirable.

Pour en savoir plus, consultez la rubrique [Zero-Hour auto-protection-protection contre le courrier indésirable et les programmes malveillants](zero-hour-auto-purge.md).

### <a name="audit-logging-for-reporting-and-investigation"></a>Journalisation d’audit pour la création de rapports et l’enquête

La journalisation d’audit est disponible dans les abonnements qui incluent [Exchange Online](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description). Pour afficher les données des rapports de protection contre les menaces, tels que le [tableau de bord de sécurité](security-dashboard.md), les rapports de sécurité de [messagerie](view-email-security-reports.md)et l' [Explorateur](use-explorer-in-security-and-compliance.md), la journalisation d’audit doit être activée pour votre organisation. Pour en savoir plus, consultez la rubrique [activer ou désactiver la recherche dans le journal d’audit Office 365](turn-audit-log-search-on-or-off.md).

## <a name="post-setup-tasks"></a>Tâches consécutives à l’installation

Une fois que vous avez configuré vos fonctionnalités de protection contre les menaces, veillez à surveiller le fonctionnement de ces fonctionnalités, examiner et réviser vos stratégies en fonction de vos besoins, et surveiller les nouvelles fonctionnalités et les mises à jour de services.

|Procédure  |Ressources pour en savoir plus  |
|---------|---------|
|Découvrez comment les fonctionnalités de protection contre les menaces fonctionnent pour votre organisation en affichant des rapports    |[Tableau de bord de sécurité](security-dashboard.md)<br/>[Rapports de sécurité de messagerie](view-email-security-reports.md)<br/>[Rapports pour la protection avancée contre les menaces Office 365](view-reports-for-atp.md)<br/>[Threat Explorer](use-explorer-in-security-and-compliance.md)    |
|Vérifier et réviser régulièrement vos stratégies de protection contre les menaces selon vos besoins    |[Degré de sécurisation](microsoft-secure-score.md)<br/>[Rapports intelligents et Insights](reports-and-insights-in-security-and-compliance.md)<br/>[Fonctionnalités d’enquête et de réponse aux menaces pour Office 365](keep-users-safe-with-office-365-ti.md)          |
|Surveillez les nouvelles fonctionnalités et les mises à jour de service     |[Options de publication standard et ciblées](https://docs.microsoft.com/office365/admin/manage/release-options-in-office-365?view=o365-worldwide)<br/>[Centre de messages](https://docs.microsoft.com/office365/admin/manage/message-center?view=o365-worldwide)<br/>[Feuille de route Microsoft 365](https://www.microsoft.com/microsoft-365/roadmap?filters=&searchterms=advanced%2Cthreat%2Cprotection)<br/>[Descriptions des services](https://docs.microsoft.com/office365/servicedescriptions/office-365-service-descriptions-technet-library)         |
