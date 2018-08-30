---
title: Rejetant l’application visionneuse Office 365 Message Encryption
ms.author: krowley
author: kccross
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 6336cabb-b06e-402f-9e85-8bb9eb4ce68f
description: Sur 15 août 2018, vous allez supprimer l’application mobile Visionneuse Office 365 Message Encryption (OME) à partir de magasins Android et Apple. L’application mobile visionneuse de chiffrement Office 365 Message a été nécessaire pour lire les messages électroniques et les pièces jointes qui ont été chiffrées avec la version précédente d’OME sur Apple et téléphones Android. En dehors de la suppression de l’application Observateur OME, nous n'effectuons pas apporté les modifications à la version précédente d’OME.
ms.openlocfilehash: 43e514bd8336d283aaf774ffa4f49565f86e7102
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527504"
---
# <a name="deprecating-office-365-message-encryption-viewer-app"></a>Rejetant l’application visionneuse Office 365 Message Encryption

Sur 15 août 2018, vous allez supprimer l’application mobile Visionneuse Office 365 Message Encryption (OME) à partir de magasins Android et Apple. L’application mobile visionneuse de chiffrement Office 365 Message a été nécessaire pour lire les messages électroniques et les pièces jointes qui ont été chiffrées avec la version précédente d’OME sur Apple et téléphones Android. En dehors de la suppression de l’application Observateur OME, nous n'effectuons pas apporté les modifications à la version précédente d’OME.
  
## <a name="changes-beginning-august-2018"></a>Modifications début août 2018

Comme annoncé septembre dernier, nous avons publié une nouvelle version [d’Office 365 Message Encryption](https://aka.ms/ome2017) afin que les utilisateurs peuvent envoyer chiffré et protégé des messages à la personne à l’intérieur ou à l’extérieur de l’organisation sans l’exigence de l’application mobile. Depuis, nous avons ajouté des fonctionnalités supplémentaires : 
  
- [Modèle de chiffrer uniquement](https://aka.ms/encryptonly)
    
- [Contrôle à déchiffrer les pièces jointes](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Admin-control-for-attachments-now-available-in-Office-365/ba-p/204007)
    
Avec cette modification, les utilisateurs ne pourront télécharger l’application mobile visionneuse de chiffrement Office 365 Message commence au 1er août. Par conséquent, destinataires de messagerie ne peuvent pas être capables de lire des messages chiffrés avec la version précédente d’OME sur certains appareils mobiles Android et Apple. Toutefois, ils seront toujours en mesure de lire ces messages sur des ordinateurs personnels (via les navigateurs de bureau). Les utilisateurs qui ont déjà téléchargé l’application continuera à être en mesure de l’utiliser.
  
## <a name="why-this-change-was-made"></a>Pourquoi cette modification a été apportée.

La nouvelle version de OME n’a plus besoin d’une application mobile pour lire des messages électroniques protégé et les pièces jointes. Les clients Office 365 à l’aide de la nouvelle OME fonctionnalités peuvent afficher le message protégé dans Outlook mobile et les clients Office 365 peuvent afficher des messages dans un navigateur protégés.
  
Obliger les utilisateurs à télécharger une application mobile est également possible pour les clients afficher les messages protégés. Les nouvelles fonctionnalités d’Office 365 Message Encryption fournissent une meilleure expérience mobile.
  
## <a name="can-i-still-use-the-previous-version-of-office-365-message-encryption"></a>Puis-je toujours utiliser la version précédente d’Office 365 Message Encryption

La version précédente d’Office 365 Message Encryption ne sera pas déconseillée à ce stade, toutefois, nous avons apporté des améliorations importantes sur la nouvelle version de chiffrement de messages Office 365, qui rendent plus faciles à chiffrer et protéger les données sensibles à tout le monde des droits et sur n’importe quel appareil - y compris la possibilité pour les utilisateurs Office 365 lire des messages protégés directement dans Outlook (bureau, mobile et web). 
  
## <a name="what-do-i-need-to-do-to-prepare-for-this-change"></a>Que dois-je faire pour préparer pour que cette modification

Si votre organisation envoie actuellement chiffrés pièces jointes aux destinataires qui nécessitent l’application Observateur OME, vous devez mettre à jour votre documentation et des ressources de formation.
  
Nous vous recommandons de mettre à jour les règles de flux de messagerie existantes Exchange pour utiliser la version actuelle de OME afin que votre organisation peut tirer parti des fonctionnalités nouvelles et améliorées. Une fois que vous avez configuré les nouvelles fonctionnalités OME, destinataires n’est pas nécessaire de l’application Observateur OME pour lire les messages chiffrés sur des appareils mobiles.
  
Microsoft vous recommande de vous un plan pour la déplacer vers les nouvelles fonctionnalités OME dès que possible pour votre organisation. Pour plus d’informations, voir [configurer les nouvelles fonctionnalités d’Office 365 Message Encryption](set-up-new-message-encryption-capabilities.md). Si vous souhaitez en savoir plus sur le fonctionnement tout d’abord les nouvelles fonctionnalités, voir [Office 365 Message Encryption](ome.md).
  

