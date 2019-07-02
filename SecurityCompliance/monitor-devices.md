---
title: Surveillance et création de rapports sur les appareils dans le centre de sécurité Microsoft 365
description: Décrit comment maintenir vos appareils sécurisés, mis à jour et détecter les menaces potentielles au sein de votre organisation
keywords: sécurité, programmes malveillants, Microsoft 365, M365, centre de sécurité, moniteur, rapport, appareils
ms.prod: w10
ms.mktglfcycl: deploy
ms.localizationpriority: medium
ms.author: ellevin
author: levinec
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
search.appverid: met150
ms.openlocfilehash: 44fd28a0ba2ec72d999c89d183d85ccb496903ec
ms.sourcegitcommit: b9d8a43cb3afcdc8820bc9470c5707eff8fc6616
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2019
ms.locfileid: "34852868"
---
# <a name="device-monitoring-and-reporting-in-microsoft-365-security-center"></a>Surveillance et création de rapports sur les appareils dans le centre de sécurité Microsoft 365

Maintenez vos appareils sécurisés, mis à jour, et présentez les menaces potentielles dans le centre de sécurité Microsoft 365.

## <a name="view-device-alerts"></a>Afficher les alertes de l’appareil

Obtenez des alertes à jour sur l’activité de violation et d’autres menaces sur vos appareils à partir de Microsoft Defender ATP (disponible avec une licence E5). Le centre de sécurité Microsoft 365 contrôle efficacement ces alertes à un niveau élevé à l’aide de votre flux de travail préféré.

### <a name="monitor-high-impact-alerts"></a>Surveiller les alertes à fort impact

Chaque alerte Microsoft Defender ATP a un niveau de gravité correspondant (élevé, moyen, faible ou informatif) qui indique son impact potentiel sur votre réseau si vous ne l’avez pas fait.  

Utilisez la carte de **gravité des alertes de périphérique** pour vous concentrer spécifiquement sur les alertes plus sévères et susceptibles de nécessiter une réponse immédiate. À partir de cette carte, vous pouvez consulter plus d’informations sur le portail du centre de sécurité Microsoft Defender.

![Carte de gravité des alertes d’appareil](./media/security-docs/device-alerts-severity.png)

### <a name="understand-sources-of-alerts"></a>Comprendre les sources d’alertes

Microsoft Defender ATP exploite les données d’une large gamme de capteurs de sécurité et de sources d’intelligence pour générer des alertes. Par exemple, il peut utiliser les informations de détection de l’antivirus Windows Defender et des logiciels malveillants tiers, ainsi que votre propre intelligence de menace personnalisée fournie via l’API de service Web.

La carte sources de détection des alertes de **périphérique** affiche la répartition des alertes par source. Cette carte peut vous aider à suivre l’activité liée à certaines sources, en particulier vos sources personnalisées. Vous pouvez également l’utiliser pour vous concentrer sur les alertes provenant de capteurs qui ne sont pas configurés pour bloquer automatiquement les activités ou les composants malveillants.

![Carte sources de détection des alertes de périphérique](./media/security-docs/device-alert-detection-sources.png)

À partir de cette carte, vous pouvez consulter plus d’informations sur le portail du centre de sécurité Microsoft Defender.

### <a name="understand-the-types-of-threats-that-trigger-alerts"></a>Comprendre les types de menaces déclenchant des alertes

Microsoft Defender ATP trie chaque alerte dans une catégorie représentant une certaine étape de la chaîne d’attaque ou d’un type de composant de menace. Par exemple, l’activité de menace détectée peut être classée en «mouvement latéral» pour indiquer que l’activité impliquait une tentative d’accès à d’autres appareils sur le réseau et qu’elle a vraisemblablement eu lieu après le départ initial des pirates. Lorsqu’il est détecté, un composant de menace peut être classé globalement comme «Malware» ou plus spécifiquement comme «ransomware», «dérober les informations d’identification» ou d’autres types de logiciels malveillants ou indésirables.

La carte des **catégories de menaces du périphérique** affiche la répartition des alertes dans ces catégories. Vous pouvez utiliser ces informations pour identifier les activités de menace, telles que les tentatives de vol d’informations d’identification, ce qui peut avoir un impact plus significatif par rapport aux tentatives d’ingénierie sociale, par exemple. Vous pouvez également l’utiliser pour surveiller les menaces pouvant être destructrices telles que les ransomware.

![Carte des catégories de menaces de périphérique](./media/security-docs/device-threat-categories.png)

### <a name="monitor-active-alerts"></a>Surveiller les alertes actives

La carte d' **État des alertes de périphérique** indique le nombre d’alertes qui n’ont pas été résolues et peuvent nécessiter votre attention. À partir de cette carte, vous pouvez consulter plus d’informations sur le portail du centre de sécurité Microsoft Defender.

![Carte d’état d’alerte de périphérique](./media/security-docs/device-alert-status.png)

### <a name="monitor-classification-of-resolved-alerts"></a>Surveiller la classification des alertes résolues

Lors de la résolution d’une alerte Microsoft Defender ATP, votre équipe de sécurité peut spécifier si une alerte a été vérifiée comme suit:

* Alerte vraie qui identifie les composants de menace ou d’activité de violation réels
* Alerte erronée ayant détecté une activité normale de manière incorrecte

La fiche classification des alertes de **périphérique** indique si les alertes résolues ont été classées comme vrai ou faux. À partir de cette carte, vous pouvez consulter plus d’informations sur le portail du centre de sécurité Microsoft Defender.

Remarque: dans certains cas, les informations de classification ne sont pas disponibles pour certaines alertes.

![Carte de classification des alertes de périphérique](./media/security-docs/device-alert-classification.png)

### <a name="monitor-determination-of-resolved-alerts"></a>Surveiller la détermination des alertes résolues

En plus de déterminer si une alerte est true ou false au cours de la résolution, votre équipe de sécurité peut fournir une détermination indiquant le type d’activité normale ou malveillante détectée lors de la validation de l’alerte.

La carte de **détermination des alertes de périphérique** indique la détermination fournie pour chaque alerte, en particulier:

* **Apt** – Advanced persistent Threat, indiquant que le composant de menace ou d’activité détecté fait partie d’une violation sophistiquée conçue pour se faire une brèche dans le réseau affecté  
* **Programme malveillant** : fichier ou code malveillant
* **Personnel de sécurité** : activité normale effectuée par le personnel de sécurité
* **Test de sécurité** : activité ou composants conçus pour simuler les menaces réelles et devant déclencher des alertes de sécurité et générer des alertes.
* **Logiciels** indésirables: applications et autres logiciels qui ne sont pas considérés comme malveillants, mais enfreignent une stratégie ou des normes d’utilisation acceptables.
* **Autres** : toute autre détermination qui ne relève pas des types fournis

À partir de cette carte, vous pouvez consulter plus d’informations dans le centre de sécurité Microsoft Defender.

![Carte de détermination d’alerte de périphérique](./media/security-docs/device-alert-determination.png)

### <a name="understand-which-devices-are-at-risk"></a>Comprendre quels périphériques sont exposés

**Device protection** indique le niveau de risque pour les appareils. Le niveau de risque est basé sur des facteurs tels que le type et la gravité des alertes sur l’appareil.

![Carte de protection des appareils](./media/security-docs/device-protection.png)

## <a name="monitor-and-report-status-of-intune-managed-devices"></a>Surveillance et signalement de l’état des appareils gérés par Intune

Les rapports suivants contiennent des données provenant d’appareils intégrés dans Intune. Les données provenant d’appareils non inscrits ne sont pas incluses. Seuls les administrateurs globaux peuvent afficher ces cartes.

Les données d’appareil apportées Intune incluent:

* Conformité des appareils
* Appareils avec programme malveillant actif
* Types de programmes malveillants sur les appareils
* Programmes malveillants sur les appareils
* Appareils avec des détections de programmes malveillants
* Utilisateurs avec des détections de programmes malveillants

### <a name="monitor-device-compliance"></a>Surveiller la conformité des appareils

**La conformité des appareils** indique le nombre de périphériques qui sont intégrés dans Intune conformément aux stratégies de configuration.

![Carte de conformité des appareils](./media/security-docs/device-compliance.png)

### <a name="discover-devices-with-malware-detections"></a>Détecter les appareils avec des détections de programmes malveillants

**Périphériques** les détections de programmes malveillants d’appareils fournissent le nombre d’appareils apportés Intune avec des programmes malveillants qui n’ont pas été entièrement résolus en raison d’actions en attente (un redémarrage, une analyse complète ou des actions utilisateur manuelles) ou si l’action de correction ne s’est pas correctement terminée.

![Carte de détection des programmes malveillants d’appareils](./media/security-docs/device-malware-detections.png)

### <a name="understand-the-types-of-malware-detected"></a>Comprendre les types de programmes malveillants détectés

**Types de programmes malveillants sur les appareils** affiche différents types de programmes malveillants qui ont été détectés sur les appareils intégrés dans Intune. Vous pouvez examiner chaque type dans le centre de sécurité Microsoft 365.

![Types de programmes malveillants sur la carte des appareils](./media/security-docs/types-of-malware-on-devices.png)

### <a name="understand-the-specific-malware-detected-on-your-devices"></a>Comprendre le programme malveillant spécifique détecté sur vos appareils

**Programmes malveillants sur les appareils** fournit une liste des programmes malveillants spécifiques détectés sur vos appareils.

![Carte de programmes malveillants sur les appareils](./media/security-docs/malware-on-devices.png)

### <a name="understand-which-devices-have-the-most-malware"></a>Comprendre quels appareils ont le plus de programmes malveillants

**Périphériques avec des détections de programmes malveillants** indique quels périphériques ont le plus de détections de programmes malveillants. Dans le centre de sécurité Microsoft 365, vous pouvez rechercher si un programme malveillant est actif, qui utilise l’appareil et son statut de gestion dans Intune.

![Carte périphériques avec des détections de programmes malveillants](./media/security-docs/devices-with-malware-detections.png)

### <a name="understand-which-users-have-devices-with-the-most-malware"></a>Comprendre quels sont les utilisateurs ayant des appareils avec le plus de programmes malveillants

**Les utilisateurs disposant de détections de programmes malveillants** affichent les utilisateurs avec des appareils qui avaient le plus de détections de programmes malveillants. Dans le centre de sécurité Microsoft 365, vous pouvez voir le nombre de périphériques affectés à chaque utilisateur et obtenir plus d’informations sur chaque appareil et le type de programmes malveillants.

![Utilisateurs avec carte de détection des programmes malveillants](./media/security-docs/users-with-malware-detections.png)

## <a name="monitor-and-manage-asr-rule-deployment-and-detections"></a>Surveillance et gestion du déploiement et des détections de règles ASR

Les règles de réduction de la [surface d’attaque (ASR)](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-exploit-guard/attack-surface-reduction-exploit-guard) permettent d’empêcher les actions et les applications généralement utilisées par un programme malveillant de recherche sur les ordinateurs. Ces règles contrôlent quand et comment les fichiers exécutables peuvent s’exécuter. Par exemple, vous pouvez empêcher JavaScript ou VBScript de lancer un exécutable téléchargé, bloquer les appels d’API Win32 à partir de macros Office ou bloquer les processus qui s’exécutent à partir de lecteurs USB.

![Carte de réduction de surface d’attaque](./media/security-docs/attack-surface-reduction-rules.png)

La carte de règles de réduction de la **surface d’attaque** offre une vue d’ensemble du déploiement des règles sur vos appareils.

La barre supérieure sur la carte indique le nombre total d’appareils qui sont dans les modes de déploiement suivants:

* **Mode de blocage** – appareils avec au moins une règle configurée pour bloquer l’activité détectée
* **Mode audit** : appareils sans règle définie pour bloquer les activités détectées, mais avec au moins un ensemble de règles pour auditer les activités détectées  
* **Off** : les appareils dont toutes les règles de récupération automatique sont désactivées

La partie inférieure de cette carte indique les paramètres par règle sur vos appareils. Chaque barre indique le nombre d’appareils configurés pour bloquer ou auditer la détection ou la désactivation de la règle.

### <a name="view-asr-detections"></a>Afficher les détections ASR

Pour afficher des informations détaillées sur les détections de règles ASR sur votre réseau, sélectionnez **Afficher** les détections sur la carte des règles de réduction de la **surface d’attaque** . L' **** onglet détections de la page rapport détaillé s’ouvre.

![Onglet détections](./media/security-docs/detections-tab.png)

Le graphique en haut de la page affiche les détections dans le temps de détections de pile qui ont été bloquées ou auditées. Le tableau en bas répertorie les détections les plus récentes. Utilisez les informations suivantes sur le tableau pour comprendre la nature des détections:

* **Fichier détecté** : fichier, généralement un script ou un document, dont le contenu a déclenché l’activité d’attaque suspecte.
* **Règle** – nom décrivant les activités d’attaque que la règle est conçue pour intercepter. En savoir plus sur les règles ASR existantes
* Application **source** : application qui a chargé ou exécuté du contenu qui déclenche l’activité d’attaque présumée. Il peut s’agir d’une application légitime, telle qu’un navigateur Web, une application Office ou un outil système tel que PowerShell
* **Publisher** : fournisseur qui a publié l’application source

### <a name="review-device-asr-rule-settings"></a>Vérifier les paramètres de règle ASR de l’appareil

Dans la page rapport sur les règles de réduction de la **surface d’attaque** , accédez à l’onglet **configuration** pour vérifier les paramètres de règle pour les appareils individuels. Sélectionnez un appareil pour obtenir des informations détaillées sur la façon dont chaque règle est en mode bloquer, mode audit ou désactivé entièrement.

![Onglet Configuration](./media/security-docs/configuration-tab.png)

Microsoft Intune offre des fonctionnalités de gestion pour vos règles de récupération automatique du système. Si vous souhaitez mettre à jour vos paramètres, sélectionnez **prise en main** sous configurer les **appareils** sous l’onglet pour ouvrir gestion des appareils sur Intune.

### <a name="exclude-files-from-asr-rules"></a>Exclure les fichiers des règles ASR

Le centre de sécurité Microsoft 365 recueille les noms des [fichiers que vous pouvez exclure](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-exploit-guard/troubleshoot-asr#add-exclusions-for-a-false-positive) des détections par des règles de réduction de la surface d’attaque. En excluant des fichiers, vous pouvez réduire les faux positifs et déployer en toute confiance les règles de réduction de la surface d’attaque en mode bloc.

Les exclusions sont gérées sur Microsoft Intune, mais le centre de sécurité Microsoft 365 fournit un outil d’analyse pour vous aider à comprendre les fichiers. Pour commencer à collecter des fichiers pour exclusion, accédez à l’onglet **Ajouter** des exclusions dans la page rapport des règles de réduction de la **surface d’attaque** .

>[!NOTE]  
>L’outil analyse les détections par toutes les règles de réduction de la surface d’attaque, mais [seules certaines règles prennent en charge](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-exploit-guard/attack-surface-reduction-exploit-guard#attack-surface-reduction-rules)les exclusions.

![Onglet ajouter des exclusions](./media/security-docs/add-exclusions-tab.png)

Le tableau répertorie tous les noms de fichiers détectés par les règles de réduction de la surface d’attaque. Vous pouvez sélectionner des fichiers pour vérifier l’impact de leur exclusion:

* Nombre de détections moins nombreuses
* Nombre d’appareils qui signalent les menaces détectées

Pour obtenir la liste des fichiers sélectionnés avec leur chemin d’accès complet pour l’exclusion, sélectionnez **obtenir les chemins d’exclusion**.

Journaux pour les informations d’identification de blocage de la règle ASR dérobent du sous **-système Windows local Security Authority (lsass. exe)** Capturez l’application source **lsass. exe**, un fichier système normal, comme fichier détecté. Par conséquent, la liste générée des chemins d’exclusion inclut ce fichier. Pour exclure le fichier qui a déclenché cette règle au lieu de **lsass. exe**, utilisez le chemin d’accès à l’application source au lieu du fichier détecté.

Pour localiser l’application source, exécutez la [requête de recherche avancée](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting) suivante pour cette règle spécifique (identifiée par l’ID de règle 9e6c4e1f-7d60-472f-bA1a-a39ef669e4b2):

```MiscEvents
| where EventTime > ago(7d)
| where ActionType startswith "Asr"
| where AdditionalFields contains "9e6c4e1f-7d60-472f-ba1a-a39ef669e4b2"
| project InitiatingProcessFolderPath, InitiatingProcessFileName
```

#### <a name="check-files-for-exclusion"></a>Vérifier les fichiers pour exclusion
Avant d’exclure un fichier de la récupération automatique du système, nous vous recommandons d’inspecter le fichier afin de déterminer s’il n’est pas malveillant.

Pour passer en revue un fichier, utilisez la [page informations](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/investigate-files) sur le fichier sur le centre de sécurité Microsoft Defender. La page fournit des informations de récurrence ainsi que le ratio de détection antivirus VirusTotal. Vous pouvez également utiliser la page pour envoyer le fichier pour une analyse approfondie.

Pour rechercher un fichier détecté dans le centre de sécurité Microsoft Defender, recherchez toutes les détections de récupération automatique du système à l’aide de la requête de chasse avancée suivante:

```MiscEvents
| where EventTime > ago(7d)
| where ActionType startswith "Asr"
| project FolderPath, FileName, SHA1, InitiatingProcessFolderPath, InitiatingProcessFileName, InitiatingProcessSHA1
```

Utilisez **SHA1** ou le **InitiatingProcessSHA1** dans les résultats pour rechercher le fichier à l’aide de la barre de recherche universelle dans le centre de sécurité Microsoft Defender.
