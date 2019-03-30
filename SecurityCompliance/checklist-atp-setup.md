---
title: 'Démarrage rapide: configurer Office 365 protection avancée contre les menaces'
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/19/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection:
- M365-security-compliance
description: Voici un guide de démarrage rapide que vous pouvez utiliser pour vous assurer que la protection avancée contre les menaces Office 365 (ATP) est configurée et configurée pour votre organisation.
ms.openlocfilehash: a071c626327aa7d0055df522e8fec5ebe41d6a83
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2019
ms.locfileid: "30999397"
---
# <a name="quick-start-guide-set-up-office-365-advanced-threat-protection"></a>Guide de démarrage rapide : configurer Office 365 - Protection avancée contre les menaces

Voici un guide de démarrage rapide que vous pouvez utiliser comme liste de vérification pour vous assurer que la protection avancée contre les menaces Office 365 est configurée pour votre organisation. Si vous ne connaissez pas la protection contre les menaces dans Office 365, ou si vous n'êtes pas sûr de savoir où commencer, utilisez les instructions suivantes comme point de départ. 

> [!IMPORTANT]
> Les **paramètres recommandés initiaux sont inclus pour chaque type de stratégie; Toutefois, de nombreuses options sont disponibles et vous pouvez ajuster vos paramètres afin de répondre aux besoins spécifiques de votre organisation**. Accordez environ 30 minutes à vos stratégies ou modifications pour qu'elles fonctionnent dans votre centre de centres de travail.

## <a name="prerequisites"></a>Conditions préalables

- Votre organisation doit disposer d'un abonnement qui inclut [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP).

- Vous devez disposer d'un rôle approprié pour accéder aux fonctionnalités ATP. Le tableau suivant contient des exemples: 

    |Rôle ou groupe de rôles  |Où en savoir plus  |
    |---------|---------|
    |Administrateur général Office 365 |[À propos des rôles d'administrateur Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles)|
    |Administrateur de sécurité |[Autorisations de rôle d'administrateur dans Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/directory-assign-admin-roles)|
    |Gestion de l'organisation Exchange Online |[Autorisations dans Exchange Online](https://docs.microsoft.com/en-us/exchange/permissions-exo/permissions-exo) <br>et<br> [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)|

    (Consultez [la rubrique autorisations dans le centre &amp; de sécurité conformité Office 365](permissions-in-the-security-and-compliance-center.md).)

## <a name="part-1---anti-malware"></a>Partie 1: anti-programme malveillant

1. Dans le [Centre de sécurité & conformité](https://protection.office.com), choisissez**protection contre les programmes malveillants**pour la**stratégie** > de **gestion** > des menaces.
2. Double-cliquez sur la stratégie **par défaut** , puis sélectionnez **paramètres**.
3. Spécifiez les paramètres suivants:
    - Dans la section réponse à la **détection de programmes malveillants** , conservez le paramètre par défaut **non**.
    - Dans la section **filtre de types de pièces jointEs courantes** , choisissez **activé**.
4. Cliquez sur **Enregistrer**.

Pour en savoir plus sur les options de stratégie anti-programme malveillant, consultez la rubrique [configure anti-malware Policies](configure-anti-malware-policies.md).

## <a name="part-2---zero-day-protection"></a>Partie 2-protection Zero-Day

La protection «Zero-Day» est configurée par le biais de stratégies, telles que les stratégies de liens fiables et de pièces jointes fiables.

### <a name="atp-safe-attachments-policies"></a>Stratégies de pièces jointes approuvées ATP

1. Dans le [Centre de sécurité & Compliance Center](https://protection.office.com), choisissez protection**** > **contre les** **menaces** > pièces jointes ATP.
2. Sélectionnez l'option Activer la protection avancée contre **les menaces pour SharePoint, OneDrive et Microsoft teams**.
3. Dans la section **protéger les pièces jointes** , cliquez sur le**+** signe plus ().
4. Spécifiez les paramètres suivants:
    - Dans la zone **nom** , tapez `Block malware`.
    - Dans la section réponse, sélectionnez **bloquer**.
    - Dans la section **pièce jointe** de redirection, sélectionnez l'option Activer la redirection, puis spécifiez l'adresse de messagerie de l'administrateur ou de l'opérateur de sécurité de votre organisation qui analysera les fichiers détectés. ****
    - Dans la section **appliqué à** , choisissez **le domaine du destinataire**. Sélectionnez votre domaine, choisissez **Ajouter**, puis cliquez sur **OK**.
5. Cliquez sur **Enregistrer**.
6. (Étape supplémentaire recommandée) En tant qu'administrateur général ou administrateur SharePoint Online, exécutez la cmdlet **[Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** avec le paramètre **DisallowInfectedFileDownload** défini sur *true* pour votre environnement Office 365. (Cela empêche les personnes d'ouvrir, de transférer, de copier ou de partager des fichiers détectés comme malveillants.)  

Pour en savoir plus, consultez la rubrique [configurer des stratégies de pièces jointEs approuvéES ATP office 365](set-up-atp-safe-attachments-policies.md) et [activer Office 365 ATP pour SharePoint, OneDrive et Microsoft teams](turn-on-atp-for-spo-odb-and-teams.md).

### <a name="atp-safe-links-policies"></a>Stratégies de liens fiables ATP

Pour configurer des liens approuvés ATP, vérifiez votre stratégie par défaut et ajoutez une stratégie.

1. Dans le [Centre de sécurité & conformité](https://protection.office.com), **sélectionnez gestion** > **** > **des menaces-liens fiables ATP**.
2. Double-cliquez sur la stratégie **par défaut** .
3. Dans la section **utiliser les liens approuvés dans** , sélectionnez l'option **Office 365 ProPlus, Office pour iOS et Android**, puis cliquez sur **Enregistrer**.
4. Dans la section **stratégies qui s'appliquent à des destinataires spécifiques** , cliquez**+** sur le signe plus ().
5. Spécifiez les paramètres suivants:
    - Dans la zone **nom** , tapez un nom, tel que `Safe Links`.
    - Dans la section **Sélectionnez l'action** , choisissez **activé**.
    - Sélectionnez les options suivantes:
        - **Utiliser les pièces jointes fiables pour analyser le contenu téléchargeable** 
        - **Appliquer des liens fiables aux messages électroniques envoyés au sein de l'Organisation**
        - **Ne pas autoriser les utilisateurs à cliquer sur les liens fiables vers l'URL d'origine**
    - Dans la section **appliqué à** , choisissez **le domaine du destinataire**. Sélectionnez votre domaine, choisissez **Ajouter**, puis cliquez sur **OK**.
6. Cliquez sur **Enregistrer**.

Pour plus d'informations, reportez-vous à la rubrique [set up Office 365 ATP Safe Links Policies](set-up-atp-safe-links-policies.md). 

## <a name="part-3---anti-phishing"></a>Partie 3: anti-hameçonnage 

1. Dans le [Centre de sécurité & Compliance Center](https://protection.office.com), sélectionnez **Threat Management** > **Policy** > **protection contre le hameçonnage**.
2. Cliquez sur **stratégie par défaut**.
3. Dans la section **emprunt d'identité** , cliquez sur **modifier**, puis spécifiez les paramètres suivants:
    -  Sous l'onglet **Ajouter des utilisateurs à protéger** , activez la protection. Ajoutez ensuite des utilisateurs, tels que les membres du tableau de bord de votre organisation, votre directeur général, votre directeur financier et d'autres dirigeants. (Vous pouvez taper une adresse de messagerie individuelle ou cliquer pour afficher une liste.)
    - Dans l'onglet **Ajouter des domaines à protéger** , activez **la fonction inclure automatiquement les domaines dont je suis propriétaire**. Si vous avez des domaines personnalisés, ajoutez-les également.
    - Sous l'onglet **actions** , sélectionnez **déplacer le message vers les dossiers** de courrier indésirable des destinataires pour les utilisateurs empruntés et les domaines empruntés, puis activez les conseils de sécurité.
    - Sous l'onglet **intelligence des boîtes aux lettres** , assurez-vous que l'intelligence des boîtes aux lettres est activée.
    - Dans l'onglet **vérifier vos paramètres** , une fois que vous avez vérifié vos paramètres, cliquez sur **Enregistrer**.
4. Dans la section **usurpation** , cliquez sur **modifier**, puis spécifiez les paramètres suivants:
    - Dans l'onglet **paramètres du filtre d'usurpation d'identité** , assurez-vous que la protection contre l'usurpation d'identité est activée.
    - Sous l'onglet **actions** , choisissez déplacer le message vers les dossiers de courrier indésirable des destinataires.
    - Dans l'onglet **vérifier vos paramètres** , une fois que vous avez vérifié vos paramètres, cliquez sur **Enregistrer**. (Si vous n'avez apporté aucune modification, cliquez sur **Annuler**.)
5. Fermez la page Paramètres de stratégie par défaut.

Pour en savoir plus sur les options de stratégie anti-hameçonnage, consultez la rubrique [set up Office 365 ATP anti-phishing and anti-](set-up-anti-phishing-policies.md)phishing Policies.

## <a name="part-4---anti-spam"></a>Partie 4: blocage du courrier indésirable

1. Dans le [Centre de sécurité & conformité](https://protection.office.com), choisissez**protection contre le courrier**indésirable pour la**stratégie** > de **gestion** > des menaces.
2. Sous l'onglet **personnalisé** , activez les **paramètres personnalisés** .
3. Développez **stratégie de filtrage du courrier indésirAble par défaut**, cliquez sur **modifier la stratégie**, puis spécifiez les paramètres suivants:
    - Dans la section **actions de courrier indésirable et en bloc** , définissez le seuil sur une valeur de 5 ou 6.
    - Dans la section **autoriser les listes** , vérifiez (et si nécessaire, modifiez) vos expéditeurs et domaines autorisés.
4. Cliquez sur **Enregistrer**.

Pour en savoir plus sur les options de votre stratégie de blocage du courrier indésirable, consultez [la rubrique Configurer les stratégies anti-courrier](configure-the-anti-spam-policies.md)indésirable.

## <a name="part-5---service-wide-settings"></a>Partie 5-paramètres à l'échelle du service

### <a name="zero-hour-auto-purge"></a>Purge automatique avec zéro heure

La purge automatique à zéro heure (ZAP) est activée par défaut; Toutefois, les conditions suivantes doivent être remplies:
- Les actions de courrier indésirable sont définies pour **déplacer le message vers le dossier** courrier indésirable des stratégies de blocage du courrier indésirable.
- Les utilisateurs ont conservé leurs paramètres de courrier indésirable par défaut et n'ont pas désactivé la protection contre le courrier indésirable.

Pour en savoir plus, consultez la rubrique [Zero-Hour auto-protection-protection contre le courrier indésirable et les programmes malveillants](zero-hour-auto-purge.md).

### <a name="audit-logging"></a>Journalisation d'audit

Pour afficher les données des rapports de protection contre les menaces, tels que le [tableau de bord de sécurité](security-dashboard.md) et l' [Explorateur](use-explorer-in-security-and-compliance.md), la journalisation d'audit doit être activée pour votre organisation.

Voir [activer ou désactiver la recherche dans le journal d'audit Office 365](turn-audit-log-search-on-or-off.md).

## <a name="post-setup-tasks"></a>Tâches consécutives à l'installation

### <a name="watch-for-new-features-and-service-updates"></a>SurVeillez les nouvelles fonctionnalités et les mises à jour de service

- [Consultez la feuille de route Microsoft 365](https://www.microsoft.com/microsoft-365/roadmap?filters=&searchterms=advanced%2Cthreat%2Cprotection)

- [Consultez la description du service Office 365 Advanced Threat Protection](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp)

### <a name="see-how-atp-is-working-for-your-organization"></a>Découvrez le fonctionnement de la fonctionnalité ATP pour votre organisation

- [Afficher les rapports pour Office 365 protection avancée contre les menaces](view-reports-for-atp.md)

- [Utiliser l'Explorateur dans le &amp; Centre de sécurité conformité](use-explorer-in-security-and-compliance.md)

### <a name="periodically-review-and-revise-your-atp-policies"></a>Vérifier et réviser régulièrement vos stratégies ATP

- [Assurer la sécurité de vos utilisateurs Office 365 avec l'enquête et la réponse aux menaces Office 365](keep-users-safe-with-office-365-ti.md) 

- [Utilisation des rapports intelligents et des informations dans le centre de sécurité &amp; conformité Office 365](reports-and-insights-in-security-and-compliance.md) 