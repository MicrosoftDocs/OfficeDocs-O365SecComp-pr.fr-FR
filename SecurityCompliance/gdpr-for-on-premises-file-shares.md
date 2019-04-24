---
title: RGPD pour les partages de fichiers en local
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
description: Découvrez comment satisfaire aux exigences du RGPD dans le cadre des partages de fichier Windows Server en local.
ms.openlocfilehash: 14af73a2ff2a162f2f3e621c2efeb5d9050c069a
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32255222"
---
# <a name="gdpr-for-on-premises-windows-server-file-shares"></a><span data-ttu-id="6a528-103">RGPD pour les partages de fichiers Windows Server en local</span><span class="sxs-lookup"><span data-stu-id="6a528-103">GDPR for on-premises Windows Server file shares</span></span>

<span data-ttu-id="6a528-104">L’approche principale recommandée pour les partages de fichiers est la suivante :</span><span class="sxs-lookup"><span data-stu-id="6a528-104">The basic recommended approach for file shares is:</span></span>

-   <span data-ttu-id="6a528-105">Vous pouvez attribuer des étiquettes aux données sensibles à l’aide d’Azure Information Protection.</span><span class="sxs-lookup"><span data-stu-id="6a528-105">Use Azure Information Protection to label sensitive data.</span></span>

-   <span data-ttu-id="6a528-106">Vous pouvez rechercher des données à l’aide du scanneur Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="6a528-106">Use Azure Information Protection scanner to find data.</span></span>

<span data-ttu-id="6a528-107">L’approche recommandée pour les partages de fichiers est la suivante :</span><span class="sxs-lookup"><span data-stu-id="6a528-107">The recommended approach for files shares includes these steps:</span></span>

1.  <span data-ttu-id="6a528-108">**Installez et configurez le scanneur Azure Information Protection.**</span><span class="sxs-lookup"><span data-stu-id="6a528-108">**Install and configure Azure Information Protection scanner.**</span></span>

    -   <span data-ttu-id="6a528-109">Déterminez les types de données sensibles à utiliser.</span><span class="sxs-lookup"><span data-stu-id="6a528-109">Decide which sensitive data types to use.</span></span>

    -   <span data-ttu-id="6a528-110">Indiquez les dossiers locaux et les partages réseau à utiliser.</span><span class="sxs-lookup"><span data-stu-id="6a528-110">Specify local folders and network shares to use.</span></span>

2.  <span data-ttu-id="6a528-111">**Effectuez un cycle de détection.**</span><span class="sxs-lookup"><span data-stu-id="6a528-111">**Complete a discovery cycle.**</span></span>

    -   <span data-ttu-id="6a528-112">Exécutez le scanneur en mode de détection et validez les résultats.</span><span class="sxs-lookup"><span data-stu-id="6a528-112">Run the scanner in discovery mode and validate the findings.</span></span>

    -   <span data-ttu-id="6a528-113">Si nécessaire, optimisez les conditions et les types d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="6a528-113">If needed, optimize the conditions and sensitive information types.</span></span>

    -   <span data-ttu-id="6a528-114">Évaluez l’incidence que peut avoir l’application automatique d’étiquettes.</span><span class="sxs-lookup"><span data-stu-id="6a528-114">Assess the expected impact of automatically applying labels.</span></span>

3.  <span data-ttu-id="6a528-115">**Exécutez le scanneur Azure Information Protection pour appliquer des étiquettes aux documents correspondants**.</span><span class="sxs-lookup"><span data-stu-id="6a528-115">**Run the Azure Information Protection scanner to apply labels to qualifying documents**.</span></span>

4.  <span data-ttu-id="6a528-116">**Pour une meilleure protection :**</span><span class="sxs-lookup"><span data-stu-id="6a528-116">**For protection:**</span></span>

    -   <span data-ttu-id="6a528-117">Configurez des règles de protection contre la perte de données Exchange pour protéger les documents avec l’étiquette souhaitée.</span><span class="sxs-lookup"><span data-stu-id="6a528-117">Configure Exchange data loss prevention rules to protect documents with the desired label.</span></span>

    -   <span data-ttu-id="6a528-118">Veillez à déterminer des autorisations pour restreindre les personnes pouvant accéder aux fichiers.</span><span class="sxs-lookup"><span data-stu-id="6a528-118">Be sure to use permissions to limit who can access files.</span></span>

5.  <span data-ttu-id="6a528-119">**Pour la surveillance, intégrez un outil SIEM aux journaux Windows Server.**</span><span class="sxs-lookup"><span data-stu-id="6a528-119">**For monitoring, integrate Windows Server logs with a SIEM tool.**</span></span>

    -   <span data-ttu-id="6a528-p101">Pour rechercher des données personnelles dans le cadre de demandes de personnes concernées, utilisez le scanneur Azure Information Protection. Vous pouvez également configurer la recherche SharePoint Server pour analyser les partages de fichiers.</span><span class="sxs-lookup"><span data-stu-id="6a528-p101">To find personal data for data subject requests, use Azure Information Protection scanner. You can also configure SharePoint Server search to crawl file shares.</span></span>

<span data-ttu-id="6a528-122">Pour plus d’informations sur l’utilisation du scanneur Azure Information Protection pour la recherche et l’étiquetage des données personnelles, reportez-vous au Kit de détection de données du RGPD Microsoft à l’adresse [http://aka.ms/gdprpartners](<http://aka.ms/gdprpartners>).</span><span class="sxs-lookup"><span data-stu-id="6a528-122">For more information on using Azure Information Protection scanner to find and label personal data, see the Microsoft GDPR Data Discovery Toolkit at [http://aka.ms/gdprpartners](<http://aka.ms/gdprpartners>).</span></span>

<span data-ttu-id="6a528-p102">Pour plus d’informations sur la configuration du scanneur pour diverses conditions et sur l’utilisation des types d’informations sensibles Office 365 dans le cadre de la protection contre la perte de données, reportez-vous à l’article [Comment configurer des conditions pour la classification automatique et recommandée pour Azure Information Protection](https://docs.microsoft.com/fr-FR/information-protection/deploy-use/configure-policy-classification). Notez que les nouveaux types d’informations sensibles Office 365 ne pourront pas immédiatement être utilisés avec le scanneur et que les types d’informations sensibles personnalisés ne peuvent pas être utilisés avec le scanneur.</span><span class="sxs-lookup"><span data-stu-id="6a528-p102">For information on configuring the scanner for conditions and using the Office 365 data loss prevention (DLP) sensitive information types, see [How to configure conditions for automatic and recommended classification for Azure Information Protection](https://docs.microsoft.com/fr-FR/information-protection/deploy-use/configure-policy-classification). Note that new Office 365 sensitive information types will not be immediately available to use with the scanner and custom sensitive information types cannot be used with the scanner.</span></span>
