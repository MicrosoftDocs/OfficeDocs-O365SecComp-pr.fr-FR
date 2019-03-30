---
title: Surveillance des appareils dans Sécurité Microsoft 365
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
ms.openlocfilehash: fea3f35e0fca3ccc8148d93b7a535c98dd2d32b9
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2019
ms.locfileid: "31000527"
---
# <a name="monitor-devices-in-microsoft-365-security"></a><span data-ttu-id="1c166-104">Surveillance des appareils dans Sécurité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="1c166-104">Monitor devices in Microsoft 365 security</span></span>

<span data-ttu-id="1c166-105">Maintenez vos appareils sécurisés, mis à jour, et présentez les menaces potentielles dans le centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="1c166-105">Keep your devices secure, up-to-date, and spot potential threats in the Microsoft 365 security center.</span></span>

## <a name="view-device-alerts"></a><span data-ttu-id="1c166-106">Afficher les alertes de l'appareil</span><span class="sxs-lookup"><span data-stu-id="1c166-106">View device alerts</span></span>

<span data-ttu-id="1c166-107">Obtenez des alertes à jour sur l'activité de violation et d'autres menaces sur vos appareils à partir de Windows Defender ATP (disponible avec une licence E5).</span><span class="sxs-lookup"><span data-stu-id="1c166-107">Get up-to-date alerts about breach activity and other threats on your devices from Windows Defender ATP (available with an E5 license).</span></span> <span data-ttu-id="1c166-108">Le centre de sécurité Microsoft 365 dispose de plusieurs cartes qui vous permettent de surveiller efficacement ces alertes à un niveau supérieur, en fonction de votre flux de travail préféré.</span><span class="sxs-lookup"><span data-stu-id="1c166-108">Microsoft 365 security center has several cards that allow you to effectively monitor these alerts at a high-level, depending on your preferred workflow.</span></span>

### <a name="monitor-high-impact-alerts"></a><span data-ttu-id="1c166-109">Surveiller les alertes à fort impact</span><span class="sxs-lookup"><span data-stu-id="1c166-109">Monitor high-impact alerts</span></span>

<span data-ttu-id="1c166-110">Chaque alerte Windows Defender ATP a un niveau de gravité correspondant (élevé, moyen, faible ou informatif) qui indique son impact potentiel sur votre réseau si vous ne l'avez pas fait.</span><span class="sxs-lookup"><span data-stu-id="1c166-110">Each Windows Defender ATP alert has a corresponding severity—high, medium, low, or informational—that indicates its potential impact to your network if left unattended.</span></span>  

<span data-ttu-id="1c166-111">Utilisez la carte de **gravité des alertes de périphérique** pour vous concentrer spécifiquement sur les alertes plus sévères et susceptibles de nécessiter une réponse immédiate.</span><span class="sxs-lookup"><span data-stu-id="1c166-111">Use the **Device alert severity** card to focus specifically on alerts that are more severe and might require immediate response.</span></span> <span data-ttu-id="1c166-112">À partir de cette carte, vous pouvez consulter plus d'informations sur le portail du centre de sécurité Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="1c166-112">From this card, you can view more information on the Windows Defender Security Center portal.</span></span>

![Carte de gravité des alertes d'appareil](./media/security-docs/device-alerts-severity.png)

### <a name="understand-sources-of-alerts"></a><span data-ttu-id="1c166-114">Comprendre les sources d'alertes</span><span class="sxs-lookup"><span data-stu-id="1c166-114">Understand sources of alerts</span></span>

<span data-ttu-id="1c166-115">Windows Defender ATP exploite les données d'une large gamme de capteurs de sécurité et de sources d'intelligence pour générer des alertes.</span><span class="sxs-lookup"><span data-stu-id="1c166-115">Windows Defender ATP leverages data from a broad range of security sensors and intelligence sources to generate alerts.</span></span> <span data-ttu-id="1c166-116">Par exemple, il peut utiliser les informations de détection de l'antivirus Windows Defender et des logiciels malveillants tiers, ainsi que votre propre intelligence de menace personnalisée fournie via l'API de service Web.</span><span class="sxs-lookup"><span data-stu-id="1c166-116">For example, it can use detection information from Windows Defender Antivirus and third-party antimalware, as well as your own custom threat intelligence provided through the web service API.</span></span>

<span data-ttu-id="1c166-117">La carte sources de détection des alertes de **périphérique** affiche la répartition des alertes par source.</span><span class="sxs-lookup"><span data-stu-id="1c166-117">The **Device alert detection** sources card shows the distribution of alerts by source.</span></span> <span data-ttu-id="1c166-118">Cette carte peut vous aider à suivre l'activité liée à certaines sources, en particulier vos sources personnalisées.</span><span class="sxs-lookup"><span data-stu-id="1c166-118">This card can help you track activity related to certain sources, particularly your custom sources.</span></span> <span data-ttu-id="1c166-119">Vous pouvez également l'utiliser pour vous concentrer sur les alertes provenant de capteurs qui ne sont pas configurés pour bloquer automatiquement les activités ou les composants malveillants.</span><span class="sxs-lookup"><span data-stu-id="1c166-119">You can also use this to focus on alerts coming from sensors that are not configured to automatically block malicious activity or components.</span></span>

![Carte sources de détection des alertes de périphérique](./media/security-docs/device-alert-detection-sources.png)

<span data-ttu-id="1c166-121">À partir de cette carte, vous pouvez consulter plus d'informations sur le portail du centre de sécurité Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="1c166-121">From this card, you can view more information on the Windows Defender Security Center portal.</span></span>

### <a name="understand-the-types-of-threats-that-trigger-alerts"></a><span data-ttu-id="1c166-122">Comprendre les types de menaces déclenchant des alertes</span><span class="sxs-lookup"><span data-stu-id="1c166-122">Understand the types of threats that trigger alerts</span></span>

<span data-ttu-id="1c166-123">Windows Defender ATP trie chaque alerte dans une catégorie représentant une certaine étape de la chaîne d'attaque ou d'un type de composant de menace.</span><span class="sxs-lookup"><span data-stu-id="1c166-123">Windows Defender ATP sorts each alert into a category representing a certain stage in the attack chain or a type of threat component.</span></span> <span data-ttu-id="1c166-124">Par exemple, l'activité de menace détectée peut être classée en «mouvement latéral» pour indiquer que l'activité impliquait une tentative d'accès à d'autres appareils sur le réseau et qu'elle a vraisemblablement eu lieu après le départ initial des pirates.</span><span class="sxs-lookup"><span data-stu-id="1c166-124">For example, detected threat activity might be categorized into “lateral movement” to indicate that the activity involved an attempt to reach other devices on the network and has likely occurred after attackers have gained an initial foothold.</span></span> <span data-ttu-id="1c166-125">Lorsqu'il est détecté, un composant de menace peut être classé globalement comme «Malware» ou plus spécifiquement comme «ransomware», «dérober les informations d'identification» ou d'autres types de logiciels malveillants ou indésirables.</span><span class="sxs-lookup"><span data-stu-id="1c166-125">When detected, a threat component might either be classified broadly as “malware” or more specifically as “ransomware”, “credential stealing” or other types of malicious or unwanted software.</span></span>

<span data-ttu-id="1c166-126">La carte des **catégories de menaces du périphérique** affiche la répartition des alertes dans ces catégories.</span><span class="sxs-lookup"><span data-stu-id="1c166-126">The **Device threat categories** card shows the distribution of alerts into these categories.</span></span> <span data-ttu-id="1c166-127">Vous pouvez utiliser ces informations pour identifier les activités de menace, telles que les tentatives de vol d'informations d'identification, ce qui peut avoir un impact plus significatif par rapport aux tentatives d'ingénierie sociale, par exemple.</span><span class="sxs-lookup"><span data-stu-id="1c166-127">You can use this information to identify threat activity, such as attempts at credential theft, which can have more significant impact compared to attempts at social engineering, for example.</span></span> <span data-ttu-id="1c166-128">Vous pouvez également l'utiliser pour surveiller les menaces pouvant être destructrices telles que les ransomware.</span><span class="sxs-lookup"><span data-stu-id="1c166-128">You can also use this to monitor for potentially destructive threats like ransomware.</span></span>

![Carte des catégories de menaces de périphérique](./media/security-docs/device-threat-categories.png)

### <a name="monitor-active-alerts"></a><span data-ttu-id="1c166-130">Surveiller les alertes actives</span><span class="sxs-lookup"><span data-stu-id="1c166-130">Monitor active alerts</span></span>

<span data-ttu-id="1c166-131">La carte d' **État des alertes de périphérique** indique le nombre d'alertes qui n'ont pas été résolues et peuvent nécessiter votre attention.</span><span class="sxs-lookup"><span data-stu-id="1c166-131">The **Device alert status** card indicates the number of alerts that have not been resolved and might require attention.</span></span> <span data-ttu-id="1c166-132">À partir de cette carte, vous pouvez consulter plus d'informations sur le portail du centre de sécurité Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="1c166-132">From this card, you can view more information on the Windows Defender Security Center portal.</span></span>

![Carte d'état d'alerte de périphérique](./media/security-docs/device-alert-status.png)

### <a name="monitor-classification-of-resolved-alerts"></a><span data-ttu-id="1c166-134">Surveiller la classification des alertes résolues</span><span class="sxs-lookup"><span data-stu-id="1c166-134">Monitor classification of resolved alerts</span></span>

<span data-ttu-id="1c166-135">Lors de la résolution d'une alerte Windows Defender ATP, votre équipe de sécurité peut spécifier si une alerte a été vérifiée comme suit:</span><span class="sxs-lookup"><span data-stu-id="1c166-135">When resolving a Window Defender ATP alert, your security staff can specify whether an alert has been verified as:</span></span>

* <span data-ttu-id="1c166-136">Alerte vraie qui identifie les composants de menace ou d'activité de violation réels</span><span class="sxs-lookup"><span data-stu-id="1c166-136">A true alert that identifies actual breach activity or threat components</span></span>
* <span data-ttu-id="1c166-137">Alerte erronée ayant détecté une activité normale de manière incorrecte</span><span class="sxs-lookup"><span data-stu-id="1c166-137">A false alert that has incorrectly detected normal activity</span></span>

<span data-ttu-id="1c166-138">La fiche classification des alertes de **périphérique** indique si les alertes résolues ont été classées comme vrai ou faux.</span><span class="sxs-lookup"><span data-stu-id="1c166-138">The **Device alert classification** card shows whether your resolved alerts have been classified as true or false alerts.</span></span> <span data-ttu-id="1c166-139">À partir de cette carte, vous pouvez consulter plus d'informations sur le portail du centre de sécurité Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="1c166-139">From this card, you can view more information on the Windows Defender Security Center portal.</span></span>

<span data-ttu-id="1c166-140">Remarque: dans certains cas, les informations de classification ne sont pas disponibles pour certaines alertes.</span><span class="sxs-lookup"><span data-stu-id="1c166-140">Note: In some cases, classification information is unavailable for certain alerts.</span></span>

![Carte de classification des alertes de périphérique](./media/security-docs/device-alert-classification.png)

### <a name="monitor-determination-of-resolved-alerts"></a><span data-ttu-id="1c166-142">Surveiller la détermination des alertes résolues</span><span class="sxs-lookup"><span data-stu-id="1c166-142">Monitor determination of resolved alerts</span></span>

<span data-ttu-id="1c166-143">En plus de déterminer si une alerte est true ou false au cours de la résolution, votre équipe de sécurité peut fournir une détermination indiquant le type d'activité normale ou malveillante détectée lors de la validation de l'alerte.</span><span class="sxs-lookup"><span data-stu-id="1c166-143">In addition to classifying whether an alert is true or false during resolution, your security staff can provide a determination, indicating the type of normal or malicious activity that was found while validating the alert.</span></span>

<span data-ttu-id="1c166-144">La carte de **détermination des alertes de périphérique** indique la détermination fournie pour chaque alerte, en particulier:</span><span class="sxs-lookup"><span data-stu-id="1c166-144">The **Device alert determination** card shows the determination provided for each alert, specifically:</span></span>

* <span data-ttu-id="1c166-145">**Apt** – Advanced persistent Threat, indiquant que le composant de menace ou d'activité détecté fait partie d'une violation sophistiquée conçue pour se faire une brèche dans le réseau affecté</span><span class="sxs-lookup"><span data-stu-id="1c166-145">**APT** – advanced persistent threat, indicating that the detected activity or threat component is part of a sophisticated breach designed to gain a foothold in the affected network</span></span>  
* <span data-ttu-id="1c166-146">**Programme malveillant** : fichier ou code malveillant</span><span class="sxs-lookup"><span data-stu-id="1c166-146">**Malware** – malicious file or code</span></span>
* <span data-ttu-id="1c166-147">**Personnel de sécurité** : activité normale effectuée par le personnel de sécurité</span><span class="sxs-lookup"><span data-stu-id="1c166-147">**Security personnel** – normal activity performed by security staff</span></span>
* <span data-ttu-id="1c166-148">**Test de sécurité** : activité ou composants conçus pour simuler les menaces réelles et devant déclencher des alertes de sécurité et générer des alertes.</span><span class="sxs-lookup"><span data-stu-id="1c166-148">**Security testing** – activity or components designed to simulate actual threats and expected to trigger security sensors and generate alerts</span></span>
* <span data-ttu-id="1c166-149">**Logiciels** indésirables: applications et autres logiciels qui ne sont pas considérés comme malveillants, mais enfreignent une stratégie ou des normes d'utilisation acceptables.</span><span class="sxs-lookup"><span data-stu-id="1c166-149">**Unwanted software** – apps and other software that are not considered malicious, but otherwise violate policy or acceptable use standards</span></span>
* <span data-ttu-id="1c166-150">**Autres** : toute autre détermination qui ne relève pas des types fournis</span><span class="sxs-lookup"><span data-stu-id="1c166-150">**Others** – any other determination that does not fall under the provided types</span></span>

<span data-ttu-id="1c166-151">À partir de cette carte, vous pouvez afficher plus d'informations dans le centre de sécurité Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="1c166-151">From this card, you can view more information in Windows Defender security center.</span></span>

![Carte de détermination d'alerte de périphérique](./media/security-docs/device-alert-determination.png)

### <a name="understand-which-devices-are-at-risk"></a><span data-ttu-id="1c166-153">Comprendre quels périphériques sont exposés</span><span class="sxs-lookup"><span data-stu-id="1c166-153">Understand which devices are at risk</span></span>

<span data-ttu-id="1c166-154">**Device protection** indique le niveau de risque pour les appareils.</span><span class="sxs-lookup"><span data-stu-id="1c166-154">**Device protection** shows the risk level for devices.</span></span> <span data-ttu-id="1c166-155">Le niveau de risque est basé sur des facteurs tels que le type et la gravité des alertes sur l'appareil.</span><span class="sxs-lookup"><span data-stu-id="1c166-155">The risk level is based on factors such as the type and severity of alerts on the device.</span></span>

![Carte de protection des appareils](./media/security-docs/device-protection.png)

## <a name="monitor-and-report-status-of-intune-managed-devices"></a><span data-ttu-id="1c166-157">Surveillance et signalement de l'état des appareils gérés par Intune</span><span class="sxs-lookup"><span data-stu-id="1c166-157">Monitor and report status of Intune-managed devices</span></span>

<span data-ttu-id="1c166-158">La surveillance et les rapports suivants contiennent des données provenant d'appareils intégrés dans Intune.</span><span class="sxs-lookup"><span data-stu-id="1c166-158">The following monitoring and reports contain data from devices enrolled in Intune.</span></span> <span data-ttu-id="1c166-159">Les données provenant d'appareils non inscrits ne sont pas incluses.</span><span class="sxs-lookup"><span data-stu-id="1c166-159">Data from unenrolled devices is not included.</span></span> <span data-ttu-id="1c166-160">Seuls les administrateurs globaux peuvent afficher ces cartes.</span><span class="sxs-lookup"><span data-stu-id="1c166-160">Only Global Administrators can view these cards.</span></span>

<span data-ttu-id="1c166-161">Les données d'appareil apportées Intune incluent:</span><span class="sxs-lookup"><span data-stu-id="1c166-161">Intune enrolled device data includes:</span></span>

* <span data-ttu-id="1c166-162">Conformité des appareils</span><span class="sxs-lookup"><span data-stu-id="1c166-162">Device compliance</span></span>
* <span data-ttu-id="1c166-163">Appareils avec programme malveillant actif</span><span class="sxs-lookup"><span data-stu-id="1c166-163">Devices with active malware</span></span>
* <span data-ttu-id="1c166-164">Types de programmes malveillants sur les appareils</span><span class="sxs-lookup"><span data-stu-id="1c166-164">Types of malware on devices</span></span>
* <span data-ttu-id="1c166-165">Programmes malveillants sur les appareils</span><span class="sxs-lookup"><span data-stu-id="1c166-165">Malware on devices</span></span>
* <span data-ttu-id="1c166-166">Appareils avec des détections de programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="1c166-166">Devices with malware detections</span></span>
* <span data-ttu-id="1c166-167">Utilisateurs avec des détections de programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="1c166-167">Users with malware detections</span></span>

### <a name="monitor-device-compliance"></a><span data-ttu-id="1c166-168">Surveiller la conformité des appareils</span><span class="sxs-lookup"><span data-stu-id="1c166-168">Monitor device compliance</span></span>

<span data-ttu-id="1c166-169">**La conformité des appareils** indique le nombre de périphériques qui sont intégrés dans Intune conformément aux stratégies de configuration.</span><span class="sxs-lookup"><span data-stu-id="1c166-169">**Device compliance** shows how many devices that are enrolled in Intune comply with configuration policies.</span></span>

![Carte de conformité des appareils](./media/security-docs/device-compliance.png)

### <a name="discover-devices-with-malware-detections"></a><span data-ttu-id="1c166-171">Détecter les appareils avec des détections de programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="1c166-171">Discover devices with malware detections</span></span>

<span data-ttu-id="1c166-172">**Périphériques** les détections de programmes malveillants d'appareils fournissent le nombre d'appareils apportés Intune avec des programmes malveillants qui n'ont pas été entièrement résolus en raison d'actions en attente (un redémarrage, une analyse complète ou des actions utilisateur manuelles) ou si l'action de correction ne s'est pas correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="1c166-172">**Device malware detections** provides the number of Intune enrolled devices with malware that have not been fully resolved due to pending actions—a restart, a full scan or manual user actions—or if the remediation action did not complete successfully.</span></span>

![Carte de détection des programmes malveillants d'appareils](./media/security-docs/device-malware-detections.png)

### <a name="understand-the-types-of-malware-detected"></a><span data-ttu-id="1c166-174">Comprendre les types de programmes malveillants détectés</span><span class="sxs-lookup"><span data-stu-id="1c166-174">Understand the types of malware detected</span></span>

<span data-ttu-id="1c166-175">**Types de programmes malveillants sur les appareils** affiche différents types de programmes malveillants qui ont été détectés sur les appareils intégrés dans Intune.</span><span class="sxs-lookup"><span data-stu-id="1c166-175">**Types of malware on devices** shows different kinds of malware that have been detected on devices enrolled in Intune.</span></span> <span data-ttu-id="1c166-176">Vous pouvez examiner chaque type dans le centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="1c166-176">You can investigate each type in Microsoft 365 security center.</span></span>

![Types de programmes malveillants sur la carte des appareils](./media/security-docs/types-of-malware-on-devices.png)

### <a name="understand-the-specific-malware-detected-on-your-devices"></a><span data-ttu-id="1c166-178">Comprendre le programme malveillant spécifique détecté sur vos appareils</span><span class="sxs-lookup"><span data-stu-id="1c166-178">Understand the specific malware detected on your devices</span></span>

<span data-ttu-id="1c166-179">**Programmes malveillants sur les appareils** fournit une liste des programmes malveillants spécifiques détectés sur vos appareils.</span><span class="sxs-lookup"><span data-stu-id="1c166-179">**Malware on devices** provides a list of the specific malware detected on your devices.</span></span>

![Carte de programmes malveillants sur les appareils](./media/security-docs/malware-on-devices.png)

### <a name="understand-which-devices-have-the-most-malware"></a><span data-ttu-id="1c166-181">Comprendre quels appareils ont le plus de programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="1c166-181">Understand which devices have the most malware</span></span>

<span data-ttu-id="1c166-182">**Périphériques avec des détections de programmes malveillants** indique quels périphériques ont le plus de détections de programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="1c166-182">**Devices with malware detections** shows which devices have the most malware detections.</span></span> <span data-ttu-id="1c166-183">Dans le centre de sécurité Microsoft 365, vous pouvez rechercher si un programme malveillant est actif, qui utilise l'appareil et son statut de gestion dans Intune.</span><span class="sxs-lookup"><span data-stu-id="1c166-183">In Microsoft 365 security center, you can investigate whether malware is active, who uses the device, and its management status in Intune.</span></span>

![Carte périphériques avec des détections de programmes malveillants](./media/security-docs/devices-with-malware-detections.png)

### <a name="understand-which-users-have-devices-with-the-most-malware"></a><span data-ttu-id="1c166-185">Comprendre quels sont les utilisateurs ayant des appareils avec le plus de programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="1c166-185">Understand which users have devices with the most malware</span></span>

<span data-ttu-id="1c166-186">**Les utilisateurs disposant de détections de programmes malveillants** affichent les utilisateurs avec des appareils qui avaient le plus de détections de programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="1c166-186">**Users with malware detections** shows users with devices that had the most malware detections.</span></span> <span data-ttu-id="1c166-187">Dans le centre de sécurité Microsoft 365, vous pouvez voir le nombre de périphériques affectés à chaque utilisateur et obtenir plus d'informations sur chaque appareil et le type de programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="1c166-187">In Microsoft 365 security center, you can see how many devices are assigned to each user and more information about each device and the type of malware.</span></span>

![Utilisateurs avec carte de détection des programmes malveillants](./media/security-docs/users-with-malware-detections.png)

## <a name="monitor-and-manage-asr-rule-deployment-and-detections"></a><span data-ttu-id="1c166-189">Surveillance et gestion du déploiement et des détections de règles ASR</span><span class="sxs-lookup"><span data-stu-id="1c166-189">Monitor and manage ASR rule deployment and detections</span></span>

<span data-ttu-id="1c166-190">Les règles de réduction de la [surface d'attaque (ASR)](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-exploit-guard/attack-surface-reduction-exploit-guard) permettent d'empêcher les actions et les applications généralement utilisées par un programme malveillant de recherche sur les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="1c166-190">[Attack Surface Reduction (ASR) rules](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-exploit-guard/attack-surface-reduction-exploit-guard) help prevent actions and apps that are typically used by exploit-seeking malware to infect machines.</span></span> <span data-ttu-id="1c166-191">Ces règles contrôlent quand et comment les fichiers exécutables peuvent s'exécuter.</span><span class="sxs-lookup"><span data-stu-id="1c166-191">These rules control when and how executables can run.</span></span> <span data-ttu-id="1c166-192">Par exemple, vous pouvez empêcher JavaScript ou VBScript de lancer un exécutable téléchargé, bloquer les appels d'API Win32 à partir de macros Office ou bloquer les processus qui s'exécutent à partir de lecteurs USB.</span><span class="sxs-lookup"><span data-stu-id="1c166-192">For example, you can prevent JavaScript or VBScript from launching a downloaded executable, block Win32 API calls from Office macros, or block processes that run from USB drives.</span></span>

![Carte de réduction de surface d'attaque](./media/security-docs/attack-surface-reduction-rules.png)

<span data-ttu-id="1c166-194">La carte de règles de réduction de la **surface d'attaque** offre une vue d'ensemble du déploiement des règles sur vos appareils.</span><span class="sxs-lookup"><span data-stu-id="1c166-194">The **Attack surface reduction rules** card provides an overview of the deployment of rules across your devices.</span></span>

<span data-ttu-id="1c166-195">La barre supérieure sur la carte indique le nombre total d'appareils qui sont dans les modes de déploiement suivants:</span><span class="sxs-lookup"><span data-stu-id="1c166-195">The top bar on the card shows the total number of devices that are in the following deployment modes:</span></span>

* <span data-ttu-id="1c166-196">**Mode de blocage** – appareils avec au moins une règle configurée pour bloquer l'activité détectée</span><span class="sxs-lookup"><span data-stu-id="1c166-196">**Block mode** – devices with at least one rule configured to block detected activity</span></span>
* <span data-ttu-id="1c166-197">**Mode audit** : appareils sans règle définie pour bloquer les activités détectées, mais avec au moins un ensemble de règles pour auditer les activités détectées</span><span class="sxs-lookup"><span data-stu-id="1c166-197">**Audit mode** – devices with no rules set to block detected activity, but has at least one rule set to audit detected activity</span></span>  
* <span data-ttu-id="1c166-198">**Off** : les appareils dont toutes les règles de récupération automatique sont désactivées</span><span class="sxs-lookup"><span data-stu-id="1c166-198">**Off** – devices with all ASR rules turned off</span></span>

<span data-ttu-id="1c166-199">La partie inférieure de cette carte indique les paramètres par règle sur vos appareils.</span><span class="sxs-lookup"><span data-stu-id="1c166-199">The lower part of this card shows settings by rule across your devices.</span></span> <span data-ttu-id="1c166-200">Chaque barre indique le nombre d'appareils configurés pour bloquer ou auditer la détection ou la désactivation de la règle.</span><span class="sxs-lookup"><span data-stu-id="1c166-200">Each bar indicates the number of devices that are set to block or audit detection or have the rule completely turned off.</span></span>

### <a name="view-asr-detections"></a><span data-ttu-id="1c166-201">Afficher les détections ASR</span><span class="sxs-lookup"><span data-stu-id="1c166-201">View ASR detections</span></span>

<span data-ttu-id="1c166-202">Pour afficher des informations détaillées sur les détections de règles ASR sur votre réseau, sélectionnez **Afficher** les détections sur la carte des règles de réduction de la **surface d'attaque** .</span><span class="sxs-lookup"><span data-stu-id="1c166-202">To view detailed information about ASR rule detections in your network, select **View detections** on the **Attack surface reduction rules** card.</span></span> <span data-ttu-id="1c166-203">L' \*\*\*\* onglet détections de la page rapport détaillé s'ouvre.</span><span class="sxs-lookup"><span data-stu-id="1c166-203">The **Detections** tab in the detailed report page will open.</span></span>

![Onglet détections](./media/security-docs/detections-tab.png)

<span data-ttu-id="1c166-205">Le graphique en haut de la page affiche les détections dans le temps de détections de pile qui ont été bloquées ou auditées.</span><span class="sxs-lookup"><span data-stu-id="1c166-205">The chart at the top of the page shows detections over time stacking detections that were either blocked or audited.</span></span> <span data-ttu-id="1c166-206">Le tableau en bas répertorie les détections les plus récentes.</span><span class="sxs-lookup"><span data-stu-id="1c166-206">The table at the bottom lists the most recent detections.</span></span> <span data-ttu-id="1c166-207">Utilisez les informations suivantes sur le tableau pour comprendre la nature des détections:</span><span class="sxs-lookup"><span data-stu-id="1c166-207">Use the following information on the table to understand the nature of the detections:</span></span>

* <span data-ttu-id="1c166-208">**Fichier détecté** : fichier, généralement un script ou un document, dont le contenu a déclenché l'activité d'attaque suspecte.</span><span class="sxs-lookup"><span data-stu-id="1c166-208">**Detected file** – the file, typically a script or a document, whose contents triggered the suspected attack activity</span></span>
* <span data-ttu-id="1c166-209">**Règle** – nom décrivant les activités d'attaque que la règle est conçue pour intercepter.</span><span class="sxs-lookup"><span data-stu-id="1c166-209">**Rule** – name describing the attack activities the rule is designed to catch.</span></span> <span data-ttu-id="1c166-210">En savoir plus sur les règles ASR existantes</span><span class="sxs-lookup"><span data-stu-id="1c166-210">Read about existing ASR rules</span></span>
* <span data-ttu-id="1c166-211">Application **source** : application qui a chargé ou exécuté du contenu qui déclenche l'activité d'attaque présumée.</span><span class="sxs-lookup"><span data-stu-id="1c166-211">**Source app** – the application that loaded or executed content triggering the suspected attack activity.</span></span> <span data-ttu-id="1c166-212">Il peut s'agir d'une application légitime, telle qu'un navigateur Web, une application Office ou un outil système tel que PowerShell</span><span class="sxs-lookup"><span data-stu-id="1c166-212">This could be a legitimate application, such as web browser, an Office application, or a system tool like PowerShell</span></span>
* <span data-ttu-id="1c166-213">**Publisher** : fournisseur qui a publié l'application source</span><span class="sxs-lookup"><span data-stu-id="1c166-213">**Publisher** – the vendor that released the source app</span></span>

### <a name="review-device-asr-rule-settings"></a><span data-ttu-id="1c166-214">Vérifier les paramètres de règle ASR de l'appareil</span><span class="sxs-lookup"><span data-stu-id="1c166-214">Review device ASR rule settings</span></span>

<span data-ttu-id="1c166-215">Dans la page rapport sur les règles de réduction de la **surface d'attaque** , accédez à l'onglet **configuration** pour vérifier les paramètres de règle pour les appareils individuels.</span><span class="sxs-lookup"><span data-stu-id="1c166-215">In the **Attack surface reduction rules** report page, go to the **Configuration** tab to review rule settings for individual devices.</span></span> <span data-ttu-id="1c166-216">Sélectionnez un appareil pour obtenir des informations détaillées sur la façon dont chaque règle est en mode bloquer, mode audit ou désactivé entièrement.</span><span class="sxs-lookup"><span data-stu-id="1c166-216">Select a device to get detailed information about whether each rule is in block mode, audit mode, or turned off entirely.</span></span>

![Onglet Configuration](./media/security-docs/configuration-tab.png)

<span data-ttu-id="1c166-218">Microsoft Intune offre des fonctionnalités de gestion pour vos règles de récupération automatique du système.</span><span class="sxs-lookup"><span data-stu-id="1c166-218">Microsoft Intune provides management functionality for your ASR rules.</span></span> <span data-ttu-id="1c166-219">Si vous souhaitez mettre à jour vos paramètres, sélectionnez **prise en main** sous configurer les **appareils** sous l'onglet pour ouvrir gestion des appareils sur Intune.</span><span class="sxs-lookup"><span data-stu-id="1c166-219">If you want to update your settings, select **Get started** under **Configure devices** in the tab to open device management on Intune.</span></span>

### <a name="exclude-files-from-asr-rules"></a><span data-ttu-id="1c166-220">Exclure les fichiers des règles ASR</span><span class="sxs-lookup"><span data-stu-id="1c166-220">Exclude files from ASR rules</span></span>

<span data-ttu-id="1c166-221">En excluant des fichiers des détections, vous pouvez empêcher les détections fausses indésirables et déployer en toute confiance les règles de réduction de la surface d'attaque en mode bloc.</span><span class="sxs-lookup"><span data-stu-id="1c166-221">By excluding files from detections, you can prevent unwanted false positive detections and more confidently deploy attack surface reduction rules in block mode.</span></span>

<span data-ttu-id="1c166-222">Tandis que les exclusions de fichiers pour les règles de réduction de la surface d'attaque sont gérées sur Microsoft Intune, le centre de sécurité Microsoft 365 fournit un outil d'analyse pour vous aider à comprendre les fichiers qui déclenchent des détections.</span><span class="sxs-lookup"><span data-stu-id="1c166-222">While file exclusions for attack surface reduction rules are managed on Microsoft Intune, Microsoft 365 security center provides an analysis tool to help you understand the files that are triggering detections.</span></span> <span data-ttu-id="1c166-223">Il permet également de collecter les noms des fichiers que vous pouvez exclure.</span><span class="sxs-lookup"><span data-stu-id="1c166-223">It also helps collect the names of the files you might want to exclude.</span></span>

<span data-ttu-id="1c166-224">Pour démarrer l'analyse des détections et la collecte des fichiers pour exclusion, accédez à l'onglet **Ajouter** des exclusions dans la page rapport des règles de réduction de la **surface d'attaque** .</span><span class="sxs-lookup"><span data-stu-id="1c166-224">To start analyzing detections and collecting files for exclusion, go to the **Add exclusions** tab in the **Attack surface reduction rules** report page.</span></span>

![Onglet ajouter des exclusions](./media/security-docs/add-exclusions-tab.png)

<span data-ttu-id="1c166-226">Le tableau répertorie tous les noms de fichiers détectés par les règles de réduction de la surface d'attaque.</span><span class="sxs-lookup"><span data-stu-id="1c166-226">The table lists all the file names detected by your attack surface reduction rules.</span></span> <span data-ttu-id="1c166-227">Une fois que vous avez sélectionné un ou plusieurs fichiers, vous pouvez examiner l'impact de l'ajout de ces fichiers à vos exceptions:</span><span class="sxs-lookup"><span data-stu-id="1c166-227">Once you select a file or multiple files, you can review the impact of adding those files to your exceptions:</span></span>

* <span data-ttu-id="1c166-228">Réduction du nombre total de détections</span><span class="sxs-lookup"><span data-stu-id="1c166-228">The reduction in the total number of detections</span></span>
* <span data-ttu-id="1c166-229">Réduction du nombre total d'appareils affectés par les détections</span><span class="sxs-lookup"><span data-stu-id="1c166-229">The reduction in the total number of devices affected by the detections</span></span>

<span data-ttu-id="1c166-230">Pour obtenir la liste des fichiers sélectionnés avec leur chemin d'accès complet pour l'exclusion, sélectionnez **obtenir les chemins d'exclusion**.</span><span class="sxs-lookup"><span data-stu-id="1c166-230">To get a list of the selected files with their full paths for exclusion, select **Get exclusion paths**.</span></span>

<span data-ttu-id="1c166-231">Pour plus d'informations sur les exclusions et des instructions détaillées sur la façon de les ajouter, consultez la [rubrique Troubleshoot the Attack surface Reduction Rules](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-exploit-guard/troubleshoot-asr).</span><span class="sxs-lookup"><span data-stu-id="1c166-231">For more information about exclusions and detailed instructions about how to add them, read [troubleshoot attack surface reduction rules](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-exploit-guard/troubleshoot-asr).</span></span>
