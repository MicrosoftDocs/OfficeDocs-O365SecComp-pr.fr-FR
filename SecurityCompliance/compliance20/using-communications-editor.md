---
title: Utiliser l’éditeur de communications
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 78865efc5c10ebcff9742f922f675b637bb9b2b0
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34151466"
---
# <a name="use-the-communications-editor"></a><span data-ttu-id="487e6-102">Utiliser l’éditeur de communications</span><span class="sxs-lookup"><span data-stu-id="487e6-102">Use the communications editor</span></span>

<span data-ttu-id="487e6-103">Lorsque vous définissez le contenu de votre contenu de portail, des notifications de conservation légale et des rappels associés, vous pouvez utiliser l’éditeur de communications pour formater et personnaliser dynamiquement votre contenu.</span><span class="sxs-lookup"><span data-stu-id="487e6-103">As you define the content of your portal content, legal hold notifications, and related reminders/escalations, you can leverage the Communications Editor to format and dynamically customize your content.</span></span>

## <a name="rich-text-editor"></a><span data-ttu-id="487e6-104">Éditeur de texte enrichi</span><span class="sxs-lookup"><span data-stu-id="487e6-104">Rich text editor</span></span> 

<span data-ttu-id="487e6-105">L’éditeur de communications permet à l’utilisateur de personnaliser le texte à l’aide des options de l’éditeur.</span><span class="sxs-lookup"><span data-stu-id="487e6-105">The Communications Editor allows user to customize the text using the editor options.</span></span> <span data-ttu-id="487e6-106">Par exemple, les utilisateurs peuvent modifier les types de police, créer des listes à puces, mettre en surbrillance le contenu, etc.</span><span class="sxs-lookup"><span data-stu-id="487e6-106">For example, users can change font types, create bulleted lists, highlight content, and more.</span></span> 

## <a name="merge-field-variables"></a><span data-ttu-id="487e6-107">Fusionner des variables de champ</span><span class="sxs-lookup"><span data-stu-id="487e6-107">Merge field variables</span></span>

<span data-ttu-id="487e6-108">Vous pouvez utiliser des variables de fusion et publipostage à partir de l’éditeur de communications pour incorporer des attributs de dépositaire personnalisés dans le corps d’une communication.</span><span class="sxs-lookup"><span data-stu-id="487e6-108">You can leverage email merge variables from the Communications Editor to embed customized custodian attributes into a communication's body text.</span></span> <span data-ttu-id="487e6-109">Lors de l’envoi au dépositaire, le champ de fusion est renseigné avec le champ correspondant.</span><span class="sxs-lookup"><span data-stu-id="487e6-109">When sent to the custodian, the merge field will be populated with the corresponding field.</span></span> <span data-ttu-id="487e6-110">Par exemple, lorsqu’il est envoyé au dépositaire John Smith, le champ de fusion [nom du dépositaire] est traduit par le nom correspondant.</span><span class="sxs-lookup"><span data-stu-id="487e6-110">For example, when sent to custodian John Smith, the merge field [Custodian Name] would be translated with the corresponding name.</span></span> 

<span data-ttu-id="487e6-111">Vous pouvez utiliser les champs de fusion de messagerie en sélectionnant les icônes de **champ de fusion** en haut du contrôle d’éditeur de texte enrichi.</span><span class="sxs-lookup"><span data-stu-id="487e6-111">You can use email merge fields by selecting the **Merge field** icons on the top of the rich-text editor control.</span></span> <span data-ttu-id="487e6-112">L’espace réservé est ajouté en fonction de l’emplacement du curseur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="487e6-112">The placeholder will be added based off the location of the users' cursor.</span></span> 

### <a name="list-of-merge-field-variables"></a><span data-ttu-id="487e6-113">Liste des variables de champ de fusion</span><span class="sxs-lookup"><span data-stu-id="487e6-113">List of merge field variables</span></span>

| <span data-ttu-id="487e6-114">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="487e6-114">Field name</span></span>                  | <span data-ttu-id="487e6-115">Détails du champ</span><span class="sxs-lookup"><span data-stu-id="487e6-115">Field details</span></span> | 
| :------------------- | :------------------- |
| <span data-ttu-id="487e6-116">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="487e6-116">Display Name</span></span>  | <span data-ttu-id="487e6-117">Prénom et nom du dépositaire.</span><span class="sxs-lookup"><span data-stu-id="487e6-117">The custodian's first and last name.</span></span> | 
| <span data-ttu-id="487e6-118">Lien d’accusé de réception</span><span class="sxs-lookup"><span data-stu-id="487e6-118">Acknowledgement Link</span></span> | <span data-ttu-id="487e6-119">Lien personnalisé permettant d’enregistrer l’accusé de réception de chaque dépositaire.</span><span class="sxs-lookup"><span data-stu-id="487e6-119">A customized link to record each custodian's acknowledgement.</span></span>|                 |
| <span data-ttu-id="487e6-120">Lien du portail</span><span class="sxs-lookup"><span data-stu-id="487e6-120">Portal Link</span></span>     | <span data-ttu-id="487e6-121">Un lien personnalisé pour le portail de conformité du dépositaire.</span><span class="sxs-lookup"><span data-stu-id="487e6-121">A customized link for the custodian's Compliance Portal.</span></span>|                |
| <span data-ttu-id="487e6-122">Officier émetteur</span><span class="sxs-lookup"><span data-stu-id="487e6-122">Issuing Officer</span></span>                   | <span data-ttu-id="487e6-123">Adresse de messagerie du responsable émetteur spécifié.</span><span class="sxs-lookup"><span data-stu-id="487e6-123">The email address of the specified issuing officer.</span></span>|                   |
| <span data-ttu-id="487e6-124">Date d’émission</span><span class="sxs-lookup"><span data-stu-id="487e6-124">Issuing Date</span></span>                   | <span data-ttu-id="487e6-125">Date à laquelle l’avis a été émis (UTC).</span><span class="sxs-lookup"><span data-stu-id="487e6-125">The date that the notice was issued (UTC).</span></span>              |