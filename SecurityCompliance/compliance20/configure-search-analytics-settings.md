---
title: Configurer les paramètres de recherche et analytique
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: d9528a4bcfaa77f2e232b25d03eda46cce42ebb9
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607673"
---
# <a name="configure-search-and-analytics-settings"></a><span data-ttu-id="b776a-102">Configurer les paramètres de recherche et analytique</span><span class="sxs-lookup"><span data-stu-id="b776a-102">Configure search and analytics settings</span></span>


## <a name="near-duplicates-and-email-threading"></a><span data-ttu-id="b776a-103">Proximité des doublons et messagerie threading</span><span class="sxs-lookup"><span data-stu-id="b776a-103">Near duplicates and email threading</span></span>

<span data-ttu-id="b776a-104">Dans cette section, vous pouvez définir des paramètres pour la détection des doublons, près de la détection des doublons et des threads de messagerie.</span><span class="sxs-lookup"><span data-stu-id="b776a-104">In this section, you can set parameters for duplicate detection, near duplicate detection, and email threading.</span></span>

- <span data-ttu-id="b776a-p101">Activer/désactiver : inclure la détection des doublons, près de la détection des doublons et messagerie threading dans le cadre du flux analytique si activé. Car ils reposent sur l’autre, vous devez tous les activer ou désactiver tous les.</span><span class="sxs-lookup"><span data-stu-id="b776a-p101">Enable/disable: include duplicate detection, near duplicate detection, and email threading as part of analytics flow if enabled. Because they build on top of each other, you must enable all of them or disable all of them.</span></span>

- <span data-ttu-id="b776a-107">Seuil : si le niveau de similarité de deux documents est dépasse le seuil, ils seront placés dans le même près de jeu en double.</span><span class="sxs-lookup"><span data-stu-id="b776a-107">Threshold: if the similarity level of two documents are above the threshold, they will be put in the same near duplicate set.</span></span>

- <span data-ttu-id="b776a-p102">Masquer les doublons par défaut : Si ce paramètre est activé, un filtre pour masquer les documents en double sera appliqué dans le jeu par défaut de travail. Le filtre peut être supprimé manuellement dans le jeu si nécessaire de travail.</span><span class="sxs-lookup"><span data-stu-id="b776a-p102">Hide duplicates by default: if this setting is on, a filter to hide duplicate documents will be applied in the working set by default. The filter can be removed manually in the working set if necessary.</span></span>

- <span data-ttu-id="b776a-p103">Nombre minimum/maximum de mots : près de messagerie et les doublons threading s’exécute uniquement sur les documents qui ont au moins le nombre minimal de mots et au plus le nombre maximal de mots. Pour plus d’informations, voir [près de détection des doublons](near-duplicates.md) et les [threads de courrier électronique](email-threading.md).</span><span class="sxs-lookup"><span data-stu-id="b776a-p103">Minimum/maximum number of words: near duplicates and email threading will run only on documents that have at least the minimum number of words and at most the maximum number of words. For more information, see [Near duplicate detection](near-duplicates.md) and [Email threading](email-threading.md).</span></span>

## <a name="themes"></a><span data-ttu-id="b776a-112">Thèmes</span><span class="sxs-lookup"><span data-stu-id="b776a-112">Themes</span></span>

<span data-ttu-id="b776a-113">Dans cette section, vous pouvez définir les paramètres des thèmes.</span><span class="sxs-lookup"><span data-stu-id="b776a-113">In this section, you can set parameters for themes.</span></span>

- <span data-ttu-id="b776a-114">Activer/désactiver : inclure des thèmes clusters dans le cadre du flux analytique si activé.</span><span class="sxs-lookup"><span data-stu-id="b776a-114">Enable/disable: include themes clustering as part of analytics flow if enabled.</span></span>
- <span data-ttu-id="b776a-p104">Ajuster le nombre maximal de thèmes dynamiquement dynamiquement : dans certains cas, il n’existe pas suffisamment de documents pour générer le nombre de thèmes souhaité. Si ce paramètre est activé, puis plutôt que vous essayez de forcer le nombre maximal de votre choix de thèmes, le système ajuste nombre maximal de thèmes dynamique.</span><span class="sxs-lookup"><span data-stu-id="b776a-p104">Adjust maximum number of themes dynamically dynamically: in certain cases, there are not enough documents to produce the desired number of themes. If this setting is turned on, then rather than trying to force the desired maximum number of themes, the system adjusts maximum number of themes dynamically.</span></span>
- <span data-ttu-id="b776a-117">Nombre maximal de thèmes : nombre souhaité de thèmes</span><span class="sxs-lookup"><span data-stu-id="b776a-117">Maximum number of themes: desired number of themes</span></span>
- <span data-ttu-id="b776a-118">Inclure les numéros de thèmes : lorsqu’il est activé, il inclut les numéros dans lors de la génération des thèmes.</span><span class="sxs-lookup"><span data-stu-id="b776a-118">Include numbers in themes: When enabled, it will include numbers in when generating themes.</span></span>  

## <a name="optical-character-recognition-ocr"></a><span data-ttu-id="b776a-119">Reconnaissance optique de caractères (OCR)</span><span class="sxs-lookup"><span data-stu-id="b776a-119">Optical character recognition (OCR)</span></span>

<span data-ttu-id="b776a-120">Lorsque ce paramètre est activé, OCR doit s’exécuter sur les images qui sont ingérés dans des groupes de travail afin qu’elles puissent être utilisables dans une requête.</span><span class="sxs-lookup"><span data-stu-id="b776a-120">When this setting is turned on, OCR will be run on images that are ingested into working sets so that they can be searchable.</span></span>

## <a name="ignore-text"></a><span data-ttu-id="b776a-121">Ignorer le texte</span><span class="sxs-lookup"><span data-stu-id="b776a-121">Ignore text</span></span>

<span data-ttu-id="b776a-p105">Il existe des instances où certains textes peuvent diminuer la qualité d’analytique, tels que des exclusions longues qui sont ajoutées à certains messages électroniques indépendamment du contenu du courrier électronique. Si vous avez pris connaissance de ces cas, vous pouvez exclure ce texte analytique en spécifiant le texte (RegEx est pris en charge) et qui doit être exclu de texte pour les modules.</span><span class="sxs-lookup"><span data-stu-id="b776a-p105">There are instances where certain texts will diminish the quality of analytics, such as lengthy disclaimers that get added to certain emails regardless of the content of the email. If you are aware of such cases, you can exclude this text from analytics by specifying the text (RegEx is supported) and which modules that text should be excluded for.</span></span>