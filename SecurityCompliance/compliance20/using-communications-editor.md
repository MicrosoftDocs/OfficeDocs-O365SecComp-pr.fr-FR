---
title: À l’aide de l’éditeur de communications
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
ms.openlocfilehash: 107f45510bcf70942c6f03bdfed0a9090f1d83c0
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607683"
---
# <a name="using-the-communications-editor"></a><span data-ttu-id="ea5ad-102">À l’aide de l’éditeur de Communications</span><span class="sxs-lookup"><span data-stu-id="ea5ad-102">Using the Communications Editor</span></span>
<span data-ttu-id="ea5ad-103">Lorsque vous définissez le contenu de votre contenu du portail, juridique maintenez notifications et rappels/escalades associés, vous pouvez tirer parti de l’éditeur de Communications pour mettre en forme et personnaliser votre contenu de manière dynamique.</span><span class="sxs-lookup"><span data-stu-id="ea5ad-103">As you define the content of your portal content, legal hold notifications, and related reminders/escalations, you can leverage the Communications Editor to format and dynamically customize your content.</span></span>

## <a name="rich-text-editor"></a><span data-ttu-id="ea5ad-104">Éditeur de texte enrichi</span><span class="sxs-lookup"><span data-stu-id="ea5ad-104">Rich-Text Editor</span></span> 

<span data-ttu-id="ea5ad-p101">L’éditeur de Communications permet à utilisateur de personnaliser le texte en utilisant les options de l’éditeur. Par exemple, les utilisateurs peuvent modifier les types de polices, créer des listes à puces et le contenu en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="ea5ad-p101">The Communications Editor allows user to customize the text using the editor options. For example, users can change font types, create bulleted lists, highlight content, and more.</span></span> 

<<include screenshot>>

## <a name="merge-field-variables"></a><span data-ttu-id="ea5ad-107">Variables de champs de fusion</span><span class="sxs-lookup"><span data-stu-id="ea5ad-107">Merge Field Variables</span></span>

<span data-ttu-id="ea5ad-p102">Vous pouvez tirer parti des variables de fusion e-mail à incorporer des attributs dépositaire personnalisé dans le corps du texte d’une communication à partir de l’éditeur de Communications. Lorsque envoyé vers le dépositaire, le champ de fusion est rempli avec le champ correspondant. Par exemple, lorsque envoyé au dépositaire John Smith, le champ de fusion [nom dépositaire] est traduit portant le nom correspondant.</span><span class="sxs-lookup"><span data-stu-id="ea5ad-p102">You can leverage email merge variables from the Communications Editor to embed customized custodian attributes into a communication's body text. When sent to the custodian, the merge field will be populated with the corresponding field. For example, when sent to custodian John Smith, the merge field [Custodian Name] would be translated with the corresponding name.</span></span> 

<span data-ttu-id="ea5ad-p103">Vous pouvez utiliser des champs de fusion de messagerie en sélectionnant les icônes de **Champ de fusion** en haut du contrôle d’éditeur de texte enrichi. L’espace réservé sera ajoutée en fonction de désactiver l’emplacement du curseur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ea5ad-p103">You can use email merge fields by selecting the **Merge Field** icons on the top of the rich-text editor control. The placeholder will be added based off the location of the users' cursor.</span></span> 

### <a name="list-of-merge-field-variables"></a><span data-ttu-id="ea5ad-113">Liste de Variables de champ de fusion</span><span class="sxs-lookup"><span data-stu-id="ea5ad-113">List of Merge Field Variables</span></span>
| <span data-ttu-id="ea5ad-114">Nom de champ</span><span class="sxs-lookup"><span data-stu-id="ea5ad-114">Field Name</span></span>                  | <span data-ttu-id="ea5ad-115">Détails du champ</span><span class="sxs-lookup"><span data-stu-id="ea5ad-115">Field Details</span></span> | 
| :------------------- | :-------------------: |
| <span data-ttu-id="ea5ad-116">Nom d'affichage</span><span class="sxs-lookup"><span data-stu-id="ea5ad-116">Display Name</span></span>  | <span data-ttu-id="ea5ad-117">Dépositaire le prénom et nom de famille</span><span class="sxs-lookup"><span data-stu-id="ea5ad-117">Custodian's first and last name</span></span> | 
| <span data-ttu-id="ea5ad-118">Lien d’un accusé de réception</span><span class="sxs-lookup"><span data-stu-id="ea5ad-118">Acknowledgement Link</span></span>                 | <span data-ttu-id="ea5ad-119">Lien personnalisé pour enregistrer un accusé de réception de chaque dépositaire</span><span class="sxs-lookup"><span data-stu-id="ea5ad-119">Customized link to record each custodian's acknowledgement</span></span>                 |
| <span data-ttu-id="ea5ad-120">Lien de portail</span><span class="sxs-lookup"><span data-stu-id="ea5ad-120">Portal Link</span></span>     | <span data-ttu-id="ea5ad-121">Lien personnalisé pour le portail de conformité de la dépositaire</span><span class="sxs-lookup"><span data-stu-id="ea5ad-121">Customized link for the custodian's Compliance Portal</span></span>                 |
| <span data-ttu-id="ea5ad-122">Responsable de délivrance</span><span class="sxs-lookup"><span data-stu-id="ea5ad-122">Issuing Officer</span></span>                   | <span data-ttu-id="ea5ad-123">Adresse de messagerie de l’agent de délivrance spécifié</span><span class="sxs-lookup"><span data-stu-id="ea5ad-123">Email address of the specified issuing officer</span></span>                   |
| <span data-ttu-id="ea5ad-124">Date d’émission</span><span class="sxs-lookup"><span data-stu-id="ea5ad-124">Issuing Date</span></span>                   | <span data-ttu-id="ea5ad-125">date à laquelle l’opération a été émise (UTC)</span><span class="sxs-lookup"><span data-stu-id="ea5ad-125">date that the notice was issued (UTC)</span></span>              |