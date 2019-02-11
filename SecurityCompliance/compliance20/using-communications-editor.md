---
title: Utiliser l’éditeur de communications
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
ms.openlocfilehash: b148ff1a77cd9225a26f98e7612e9fb5b57331e3
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29706055"
---
# <a name="use-the-communications-editor"></a><span data-ttu-id="1c726-102">Utiliser l’éditeur de communications</span><span class="sxs-lookup"><span data-stu-id="1c726-102">Use the communications editor</span></span>

<span data-ttu-id="1c726-103">Lorsque vous définissez le contenu de votre contenu du portail, juridique maintenez notifications et rappels/escalades associés, vous pouvez tirer parti de l’éditeur de Communications pour mettre en forme et personnaliser votre contenu de manière dynamique.</span><span class="sxs-lookup"><span data-stu-id="1c726-103">As you define the content of your portal content, legal hold notifications, and related reminders/escalations, you can leverage the Communications Editor to format and dynamically customize your content.</span></span>

## <a name="rich-text-editor"></a><span data-ttu-id="1c726-104">Éditeur de texte enrichi</span><span class="sxs-lookup"><span data-stu-id="1c726-104">Rich text editor</span></span> 

<span data-ttu-id="1c726-p101">L’éditeur de Communications permet à utilisateur de personnaliser le texte en utilisant les options de l’éditeur. Par exemple, les utilisateurs peuvent modifier les types de polices, créer des listes à puces et le contenu en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="1c726-p101">The Communications Editor allows user to customize the text using the editor options. For example, users can change font types, create bulleted lists, highlight content, and more.</span></span> 

## <a name="merge-field-variables"></a><span data-ttu-id="1c726-107">Variables de champs de fusion</span><span class="sxs-lookup"><span data-stu-id="1c726-107">Merge field variables</span></span>

<span data-ttu-id="1c726-p102">Vous pouvez tirer parti des variables de fusion e-mail à incorporer des attributs dépositaire personnalisé dans le corps du texte d’une communication à partir de l’éditeur de Communications. Lorsque envoyé vers le dépositaire, le champ de fusion est rempli avec le champ correspondant. Par exemple, lorsque envoyé au dépositaire John Smith, le champ de fusion [nom dépositaire] est traduit portant le nom correspondant.</span><span class="sxs-lookup"><span data-stu-id="1c726-p102">You can leverage email merge variables from the Communications Editor to embed customized custodian attributes into a communication's body text. When sent to the custodian, the merge field will be populated with the corresponding field. For example, when sent to custodian John Smith, the merge field [Custodian Name] would be translated with the corresponding name.</span></span> 

<span data-ttu-id="1c726-p103">Vous pouvez utiliser des champs de fusion de messagerie en sélectionnant les icônes de **champ de fusion** en haut du contrôle d’éditeur de texte enrichi. L’espace réservé sera ajoutée en fonction de désactiver l’emplacement du curseur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1c726-p103">You can use email merge fields by selecting the **Merge field** icons on the top of the rich-text editor control. The placeholder will be added based off the location of the users' cursor.</span></span> 

### <a name="list-of-merge-field-variables"></a><span data-ttu-id="1c726-113">Liste de variables de champ de fusion</span><span class="sxs-lookup"><span data-stu-id="1c726-113">List of merge field variables</span></span>

| <span data-ttu-id="1c726-114">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="1c726-114">Field name</span></span>                  | <span data-ttu-id="1c726-115">Détails du champ</span><span class="sxs-lookup"><span data-stu-id="1c726-115">Field details</span></span> | 
| :------------------- | :------------------- |
| <span data-ttu-id="1c726-116">Nom d'affichage</span><span class="sxs-lookup"><span data-stu-id="1c726-116">Display Name</span></span>  | <span data-ttu-id="1c726-117">Le dépositaire prénom et nom.</span><span class="sxs-lookup"><span data-stu-id="1c726-117">The custodian's first and last name.</span></span> | 
| <span data-ttu-id="1c726-118">Lien d’un accusé de réception</span><span class="sxs-lookup"><span data-stu-id="1c726-118">Acknowledgement Link</span></span> | <span data-ttu-id="1c726-119">Lien personnalisé pour enregistrer un accusé de réception de chaque dépositaire.</span><span class="sxs-lookup"><span data-stu-id="1c726-119">A customized link to record each custodian's acknowledgement.</span></span>|                 |
| <span data-ttu-id="1c726-120">Lien de portail</span><span class="sxs-lookup"><span data-stu-id="1c726-120">Portal Link</span></span>     | <span data-ttu-id="1c726-121">Lien personnalisé pour le portail de conformité de la dépositaire.</span><span class="sxs-lookup"><span data-stu-id="1c726-121">A customized link for the custodian's Compliance Portal.</span></span>|                |
| <span data-ttu-id="1c726-122">Responsable de délivrance</span><span class="sxs-lookup"><span data-stu-id="1c726-122">Issuing Officer</span></span>                   | <span data-ttu-id="1c726-123">L’adresse de messagerie de l’agent de délivrance spécifié.</span><span class="sxs-lookup"><span data-stu-id="1c726-123">The email address of the specified issuing officer.</span></span>|                   |
| <span data-ttu-id="1c726-124">Date d’émission</span><span class="sxs-lookup"><span data-stu-id="1c726-124">Issuing Date</span></span>                   | <span data-ttu-id="1c726-125">La date à laquelle l’opération a été émise (UTC).</span><span class="sxs-lookup"><span data-stu-id="1c726-125">The date that the notice was issued (UTC).</span></span>              |