---
title: Remise dynamique et l’aperçu avec Office 365 DAV approuvés en pièce jointe
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/08/2019
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: f16c9928-8e3d-4219-b994-271dc9a16272
description: Lorsque vous configurez vos stratégies de pièces jointes sûres DAV, vous choisissez remise dynamique afin d’éviter les retards de message et permettent aux utilisateurs d’afficher un aperçu des pièces jointes qui sont analysés.
ms.openlocfilehash: fe1b8fd2e26c683735f64de6b5b195e3bc351c8e
ms.sourcegitcommit: b936a2fd4b7f7a7099b96cc29580ed55bdb8bf2b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/10/2019
ms.locfileid: "27789462"
---
# <a name="dynamic-delivery-and-previewing-with-office-365-atp-safe-attachments"></a>Remise dynamique et l’aperçu avec Office 365 DAV approuvés en pièce jointe

**Résumé**: remise dynamique est une option qui peut être sélectionnée pour les [Pièces jointes fiables DAV](atp-safe-attachments.md). Lisez cet article pour en savoir plus sur remise dynamique et les fonctionnalités d’aperçu de pièce jointe dans les [Pièces jointes fiables de DAV dans Office 365](atp-safe-attachments.md).

Lorsque [les stratégies de pièces jointes sûres DAV sont configurés](set-up-atp-safe-attachments-policies.md) pour votre organisation, il existe plusieurs options pour la gestion des pièces jointes. Cela inclut les **Bloquer**, **Remplacer**et **Remise dynamique**. Selon la configuration des stratégies de pièces jointes sûres DAV, destinataires de courriers électroniques peuvent rencontrer un délai d’attente secondaire dans la remise du courrier électronique tandis que les pièces jointes sont analysés. Pour éviter les retards de message, choisissez **Remise dynamique**.
  
## <a name="how-dynamic-delivery-works"></a>Fonctionnement de distribution dynamique
  
Remise dynamique élimine les retards de courrier électronique en envoyant le corps d’un message électronique par le biais d’au destinataire avec un espace réservé pour chaque pièce jointe. L’espace réservé reste jusqu'à ce qu’une copie de la pièce jointe est analysée et déterminée sûrs par les [Pièces jointes sûres DAV](atp-safe-attachments.md). 

- Comme chaque pièce jointe est désactivée, il est disponible pour ouvrir ou télécharger. 

- Si une pièce jointe est déterminée malveillants, il est envoyé à la mise en quarantaine, où une personne dans l’équipe de sécurité de votre organisation (comme un administrateur général Office 365 ou un administrateur de sécurité) peut [Gérer les messages mis en quarantaine dans Office 365](manage-quarantined-messages-and-files.md).

La plupart des fichiers PDF et Office documents peuvent être affichés en mode sans échec pendant l’analyse DAV. Si une pièce jointe n’est pas compatible avec le Générateur d’aperçu de distribution dynamique, destinataires de courriers électroniques voient un espace réservé de pièce jointe jusqu'à ce que l’analyse des pièces jointes sûres DAV est terminée.

> [!TIP]
> Si vous utilisez un appareil mobile et un fichier PDF ne s’affichent pas dans le Générateur d’aperçu de distribution dynamique dans un premier temps, essayez de vous connecter à Office 365 à l’aide de votre navigateur mobile.

Avec remise dynamique, les personnes pouvant lire et répondre à leurs messages électroniques immédiatement, tandis que les pièces jointes sont en cours d’analyse. 

Pièces jointes sûres DAV analyse prend place dans la même zone où résident vos données d’Office 365. Pour plus d’informations sur la zone géographique de centre de données, voir [où se trouvent vos données situées ?](https://products.office.com/where-is-your-data-located?geo=All) 
  
## <a name="what-happens-when-someone-forwards-an-email-that-contains-an-attachment"></a>Que se passe-t-il lorsqu’une personne envoie un message électronique qui contient une pièce jointe ?

Supposons qu’une organisation de leur [stratégie de pièces jointes sûres DAV](set-up-atp-safe-attachments-policies.md)est à l’aide de remise dynamique et un utilisateur reçoit un message électronique contenant une pièce jointe. Maintenant Supposons que cette personne transfère le message électronique à une autre personne. Que se passe-t-il ? Cela dépend si les destinataires supplémentaires sont inclus dans les stratégies de pièces jointes sûres DAV.
  
- Si un destinataire est couverte par une stratégie de pièces jointes sûres DAV à l’aide de l’option de distribution dynamique, le destinataire voit l’espace réservé, avec la possibilité d’afficher un aperçu des fichiers compatibles.
    
- Si un destinataire n’est pas couvert par une stratégie de pièces jointes sûres DAV, puis le courrier électronique et la pièce jointe passeront, sans pièces jointes sûres DAV analyse ou des espaces réservés de la pièce jointe.
    
## <a name="whats-required-for-dynamic-delivery-to-work"></a>Les tâches requises pour la remise dynamique fonctionne ?

- Votre organisation doit avoir [Contre les menaces avancées Office 365](office-365-atp.md)
    
- Stratégies doivent être définis pour les pièces jointes sûres DAV à l’aide de l’option de distribution dynamique (voir [l’ensemble des stratégies de pièces jointes sûres DAV dans Office 365](set-up-atp-safe-attachments-policies.md))
    
- Courrier électronique de votre organisation doit être hébergé dans Office 365
    
## <a name="are-there-scenarios-for-which-dynamic-delivery-is-not-available"></a>Y a-t-il des scénarios pour lesquels la remise dynamique n’est pas disponible ?

Il existe certains scénarios dans lesquels remise dynamique n’est pas pris en charge. Ce sont les suivants :
  
- Messages électroniques stockés dans des dossiers publics
    
- Messages électroniques qui sont routés d’absence du bureau, puis de nouveau dans la boîte aux lettres de l’utilisateur à l’aide de règles personnalisées
    
- Messages électroniques qui sont déplacés (automatiquement ou manuellement) en dehors de la boîte aux lettres hébergée dans d’autres emplacements, y compris les dossiers d’archivage
    
- Messages électroniques supprimés
    
- Dossier de recherche de boîte aux lettres d’un utilisateur qui se trouve dans un état d’erreur
    
- Environnements dans lesquels un administrateur Exchange Online a activé Exclaimer. Pour résoudre ce problème, voir [les Messages avec pièces jointes ne sont pas remis lors de la remise dynamique DAV et Exclaimer sont utilisées](https://support.microsoft.com/help/4014438/messages-with-attachments-are-not-delivered-when-atp-dynamic-delivery)

- Messages chiffrés avec [Secure/Multipurpose Internet Mail Extensions (S/MIME)](s-mime-for-message-signing-and-encryption.md))

