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
# <a name="use-the-communications-editor"></a>Utiliser l’éditeur de communications

Lorsque vous définissez le contenu de votre contenu du portail, juridique maintenez notifications et rappels/escalades associés, vous pouvez tirer parti de l’éditeur de Communications pour mettre en forme et personnaliser votre contenu de manière dynamique.

## <a name="rich-text-editor"></a>Éditeur de texte enrichi 

L’éditeur de Communications permet à utilisateur de personnaliser le texte en utilisant les options de l’éditeur. Par exemple, les utilisateurs peuvent modifier les types de polices, créer des listes à puces et le contenu en surbrillance. 

## <a name="merge-field-variables"></a>Variables de champs de fusion

Vous pouvez tirer parti des variables de fusion e-mail à incorporer des attributs dépositaire personnalisé dans le corps du texte d’une communication à partir de l’éditeur de Communications. Lorsque envoyé vers le dépositaire, le champ de fusion est rempli avec le champ correspondant. Par exemple, lorsque envoyé au dépositaire John Smith, le champ de fusion [nom dépositaire] est traduit portant le nom correspondant. 

Vous pouvez utiliser des champs de fusion de messagerie en sélectionnant les icônes de **champ de fusion** en haut du contrôle d’éditeur de texte enrichi. L’espace réservé sera ajoutée en fonction de désactiver l’emplacement du curseur de l’utilisateur. 

### <a name="list-of-merge-field-variables"></a>Liste de variables de champ de fusion

| Nom du champ                  | Détails du champ | 
| :------------------- | :------------------- |
| Nom d'affichage  | Le dépositaire prénom et nom. | 
| Lien d’un accusé de réception | Lien personnalisé pour enregistrer un accusé de réception de chaque dépositaire.|                 |
| Lien de portail     | Lien personnalisé pour le portail de conformité de la dépositaire.|                |
| Responsable de délivrance                   | L’adresse de messagerie de l’agent de délivrance spécifié.|                   |
| Date d’émission                   | La date à laquelle l’opération a été émise (UTC).              |