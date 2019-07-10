---
title: Remise et aperçu dynamiques avec les pièces jointes sécurisées ATP Office 365
ms.author: deniseb
author: denisebmsft
manager: dansimp
ms.date: 04/19/2019
audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: f16c9928-8e3d-4219-b994-271dc9a16272
ms.collection:
- M365-security-compliance
description: Lorsque vous configurez vos stratégies de pièces jointes approuvées ATP, vous choisissez la remise dynamique pour éviter les retards de message et permettre aux utilisateurs de prévisualiser les pièces jointes en cours d’analyse.
ms.openlocfilehash: 2f965c119e9c4fca15e43d281dfc2d00d2c79c23
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35599900"
---
# <a name="dynamic-delivery-and-previewing-with-office-365-atp-safe-attachments"></a>Remise et aperçu dynamiques avec les pièces jointes sécurisées ATP Office 365

## <a name="overview"></a>Vue d’ensemble

La remise dynamique est une option qui peut être sélectionnée pour [les pièces jointes sûres ATP](atp-safe-attachments.md). Lisez cet article pour en savoir plus sur la remise dynamique et les fonctionnalités d’aperçu des pièces jointes dans [les pièces jointes approuvées ATP dans Office 365](atp-safe-attachments.md).

Lorsque des [stratégies de pièces jointes approuvées ATP sont configurées](set-up-atp-safe-attachments-policies.md) pour votre organisation, il existe plusieurs options pour la gestion des pièces jointes. Ces éléments incluent le **blocage**, le **remplacement**et la **remise dynamique**. En fonction de la configuration des stratégies de pièces jointes approuvées ATP, les destinataires peuvent observer un retard mineur lors de la remise du courrier électronique pendant l’analyse de leurs pièces jointes. Pour éviter les retards de message, choisissez **remise dynamique**.
  
## <a name="how-dynamic-delivery-works"></a>Fonctionnement de la remise dynamique
  
La remise dynamique élimine les retards de messagerie en envoyant le corps d’un message électronique au destinataire avec un espace réservé pour chaque pièce jointe de courrier électronique. L’espace réservé reste jusqu’à ce qu’une copie de la pièce jointe soit analysée et considérée comme fiable par [les pièces jointes sûres ATP](atp-safe-attachments.md). 

- À mesure que chaque pièce jointe est effacée, elle est disponible pour l’ouverture ou le téléchargement. 

- Si une pièce jointe est considérée comme malveillante, elle est envoyée en quarantaine, où une personne de l’équipe de sécurité de votre organisation (par exemple, un administrateur général ou un administrateur de sécurité d’Office 365) peut [gérer les messages mis en quarantaine dans Office 365](manage-quarantined-messages-and-files.md).

La plupart des documents PDF et Office peuvent être prévisualisés en mode sans échec pendant l’analyse de l’ATP. Si une pièce jointe n’est pas compatible avec le prévisualisation dynamique de remise, les destinataires de courrier voient une balise d’emplacement de pièce jointe jusqu’à la fin de l’analyse des pièces jointes.

> [!TIP]
> Si vous utilisez un appareil mobile et que les fichiers PDF ne sont pas rendus dans le prévisualiseur de remise dynamique, essayez de vous connecter à Office 365 à l’aide de votre navigateur mobile.

Avec la remise dynamique, les utilisateurs peuvent lire et répondre immédiatement à leurs messages électroniques, tandis que leurs pièces jointes sont en cours d’analyse. 

L’analyse des pièces jointes approuvées ATP a lieu dans la région où se trouvent vos données Office 365. Pour plus d’informations sur la géographie du centre de données, voir [où se trouvent vos données?](https://products.office.com/where-is-your-data-located?geo=All) 
  
## <a name="what-happens-when-someone-forwards-an-email-that-contains-an-attachment"></a>Que se passe-t-il lorsque quelqu’un transfère un courrier électronique qui contient une pièce jointe?

Supposons qu’une organisation utilise une remise dynamique pour sa [stratégie de pièces jointes approuvées ATP](set-up-atp-safe-attachments-policies.md), et qu’une personne reçoit un e-mail contenant une pièce jointe. Supposons maintenant que cette personne transfère le message électronique à une autre personne. Que se passe-t-il? Cela dépend du fait que les destinataires supplémentaires sont inclus dans les stratégies de pièces jointes approuvées ATP.
  
- Si un destinataire est couvert par une stratégie de pièces jointes approuvées ATP à l’aide de l’option de remise dynamique, le destinataire voit alors l’espace réservé, avec la possibilité de prévisualiser les fichiers compatibles.
    
- Si un destinataire n’est pas couvert par une stratégie de pièces jointes approuvées pour la protection avancée contre les menaces, le courrier électronique et la pièce jointe sont transmis, sans aucune analyse des pièces jointes et espaces réservés de pièces jointes ATP.
    
## <a name="whats-required-for-dynamic-delivery-to-work"></a>Qu’est-ce qui est requis pour que la remise dynamique fonctionne?

- Votre organisation doit disposer d' [Office 365 protection avancée contre les menaces](office-365-atp.md)
    
- Les stratégies doivent être définies pour les pièces jointes de niveau de sécurité ATP à l’aide de l’option de remise dynamique (voir [configurer des stratégies de pièces jointes de sécurité ATP dans Office 365](set-up-atp-safe-attachments-policies.md))
    
- Les messages électroniques de votre organisation doivent être hébergés dans Office 365. Bien que la [protection avancée contre les menaces Office 365 puisse être utilisée avec n’importe quel agent de transfert de courrier SMTP](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#requirements-for-office-365-advanced-threat-protection-atp) (par exemple, Exchange Server), l’option de remise dynamique des pièces jointes approuvées à l’aide de la protection avancée requiert que le courrier électronique de votre organisation soit hébergé dans Office 365. Si votre courrier électronique n’est pas hébergé dans Office 365, choisissez une autre [option de stratégie de pièces jointes approuvées ATP](set-up-atp-safe-attachments-policies.md#step-3-learn-about-atp-safe-attachments-policy-options), telle que **bloquer**.
    
## <a name="additional-considerations"></a>Considérations supplémentaires

Il existe certains scénarios dans lesquels la remise dynamique n’est pas prise en charge. Elles incluent notamment les éléments suivants :
  
- Messages électroniques figurant dans des dossiers publics
    
- Messages électroniques qui sont acheminés vers la boîte aux lettres de l’utilisateur, puis reversez-les à l’aide de règles personnalisées
    
- Messages électroniques déplacés (automatiquement ou manuellement) en dehors de la boîte aux lettres hébergée et à d’autres emplacements, y compris les dossiers d’archivage
    
- Messages électroniques supprimés
    
- Dossier de recherche de boîte aux lettres d’un utilisateur en état d’erreur
    
- Environnements dans lesquels un administrateur Exchange Online a activé Exclaimer. Pour résoudre ce message, consultez la rubrique [les messages avec des pièces jointes ne sont pas remis lorsque la remise et l’exclaimement dynamiques ATP sont utilisés](https://support.microsoft.com/help/4014438/messages-with-attachments-are-not-delivered-when-atp-dynamic-delivery)

- Messages chiffrés à l’aide de [S/MIME (Secure/Multipurpose Internet Mail Extensions)](s-mime-for-message-signing-and-encryption.md))

- Dans les cas où la remise dynamique n’est pas prise en charge, les pièces jointes fiables ATP n’analysent pas les messages électroniques. Toutefois, la remise des messages électroniques contenant des pièces jointes contenant des URL est vérifiée, en fonction de la configuration de vos [stratégies de liens fiables ATP](set-up-atp-safe-links-policies.md) . Dans ce cas, les URL dans les messages électroniques et les fichiers Office sont vérifiées.
