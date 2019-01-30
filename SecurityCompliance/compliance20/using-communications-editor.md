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
# <a name="using-the-communications-editor"></a>À l’aide de l’éditeur de Communications
Lorsque vous définissez le contenu de votre contenu du portail, juridique maintenez notifications et rappels/escalades associés, vous pouvez tirer parti de l’éditeur de Communications pour mettre en forme et personnaliser votre contenu de manière dynamique.

## <a name="rich-text-editor"></a>Éditeur de texte enrichi 

L’éditeur de Communications permet à utilisateur de personnaliser le texte en utilisant les options de l’éditeur. Par exemple, les utilisateurs peuvent modifier les types de polices, créer des listes à puces et le contenu en surbrillance. 

<<include screenshot>>

## <a name="merge-field-variables"></a>Variables de champs de fusion

Vous pouvez tirer parti des variables de fusion e-mail à incorporer des attributs dépositaire personnalisé dans le corps du texte d’une communication à partir de l’éditeur de Communications. Lorsque envoyé vers le dépositaire, le champ de fusion est rempli avec le champ correspondant. Par exemple, lorsque envoyé au dépositaire John Smith, le champ de fusion [nom dépositaire] est traduit portant le nom correspondant. 

Vous pouvez utiliser des champs de fusion de messagerie en sélectionnant les icônes de **Champ de fusion** en haut du contrôle d’éditeur de texte enrichi. L’espace réservé sera ajoutée en fonction de désactiver l’emplacement du curseur de l’utilisateur. 

### <a name="list-of-merge-field-variables"></a>Liste de Variables de champ de fusion
| Nom de champ                  | Détails du champ | 
| :------------------- | :-------------------: |
| Nom d'affichage  | Dépositaire le prénom et nom de famille | 
| Lien d’un accusé de réception                 | Lien personnalisé pour enregistrer un accusé de réception de chaque dépositaire                 |
| Lien de portail     | Lien personnalisé pour le portail de conformité de la dépositaire                 |
| Responsable de délivrance                   | Adresse de messagerie de l’agent de délivrance spécifié                   |
| Date d’émission                   | date à laquelle l’opération a été émise (UTC)              |