---
title: Utiliser l’éditeur de communications
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: c2957c88217bce4c9a34f8d3f9a9e291f1223cc9
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32241241"
---
# <a name="use-the-communications-editor"></a>Utiliser l’éditeur de communications

Lorsque vous définissez le contenu de votre contenu de portail, des notifications de conservation légale et des rappels associés, vous pouvez utiliser l'éditeur de communications pour formater et personnaliser dynamiquement votre contenu.

## <a name="rich-text-editor"></a>Éditeur de texte enrichi 

L'éditeur de communications permet à l'utilisateur de personnaliser le texte à l'aide des options de l'éditeur. Par exemple, les utilisateurs peuvent modifier les types de police, créer des listes à puces, mettre en surbrillance le contenu, etc. 

## <a name="merge-field-variables"></a>Fusionner des variables de champ

Vous pouvez utiliser des variables de fusion et publipostage à partir de l'éditeur de communications pour incorporer des attributs de dépositaire personnalisés dans le corps d'une communication. Lors de l'envoi au dépositaire, le champ de fusion est renseigné avec le champ correspondant. Par exemple, lorsqu'il est envoyé au dépositaire John Smith, le champ de fusion [nom du dépositaire] est traduit par le nom correspondant. 

Vous pouvez utiliser les champs de fusion de messagerie en sélectionnant les icônes de **champ de fusion** en haut du contrôle d'éditeur de texte enrichi. L'espace réservé est ajouté en fonction de l'emplacement du curseur de l'utilisateur. 

### <a name="list-of-merge-field-variables"></a>Liste des variables de champ de fusion

| Nom du champ                  | Détails du champ | 
| :------------------- | :------------------- |
| Nom complet  | Prénom et nom du dépositaire. | 
| Lien d'accusé de réception | Lien personnalisé permettant d'enregistrer l'accusé de réception de chaque dépositaire.|                 |
| Lien du portail     | Un lien personnalisé pour le portail de conformité du dépositaire.|                |
| Officier émetteur                   | Adresse de messagerie du responsable émetteur spécifié.|                   |
| Date d'émission                   | Date à laquelle l'avis a été émis (UTC).              |