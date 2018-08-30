---
title: Activer le complément de Message de rapport
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/28/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 4250c4bc-6102-420b-9e0a-a95064837676
description: Découvrez comment activer le complément de Message de rapport pour Outlook et Outlook sur le web, pour des utilisateurs individuels ou la totalité de votre organisation.
ms.openlocfilehash: 2260f8823132d23e0e1f57a421fd223ea3ab14bd
ms.sourcegitcommit: edf5db9357c0d34573f8cc406314525ef10d1eb9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/28/2018
ms.locfileid: "23229996"
---
# <a name="enable-the-report-message-add-in"></a>Activer le complément de Message de rapport

Le complément de Message de rapport pour Outlook permet aux utilisateurs de créer facilement des rapports e-mail mal classé, fiables ou malveillantes, Microsoft et ses filiales pour l’analyse. Microsoft utilise ces envois pour améliorer l’efficacité des technologies de protection de courrier électronique.
  
Si vous êtes un utilisateur individuel, vous pouvez activer le complément de Message de rapport par vous-même. 
  
Si vous êtes un administrateur Exchange Online, vous pouvez activer le complément de Message de rapport pour votre organisation.
    
## <a name="get-the-report-message-add-in-for-yourself"></a>Obtenez le Message de rapport de complément pour vous-même

1. Accédez à [https://store.office.com](https://store.office.com)et la recherche pour le complément de Message de rapport.
    
2. Choisissez **obtenir maintenant** (ou **Ajouter** ). 
    
3. Passez en revue les termes du contrat de stratégie de confidentialité et d’utilisation. Puis cliquez sur **Continuer**. 
    
4. Connectez-vous à votre messagerie électronique Office 365 à l’aide de votre travail compte école (pour une utilisation professionnelle) ou votre compte Microsoft (pour une utilisation personnelle).
    
Une fois que le complément est installé et activé, vous verrez les icônes suivantes : 

- Dans Outlook, l’icône ressemble à ceci : </br> ![Icône Message Add-in rapport pour Outlook](media/OutlookReportMessageIcon.png)</br>
- Dans Outlook Web App, l’icône ressemble à ceci :</br>![Outlook sur l’icône Ajouter dans un Message de rapport Web](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)</br>

  
Étape suivante, découvrez comment [utiliser le complément de Message de rapport](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).
  
## <a name="get-and-enable-the-report-message-add-in-for-your-organization"></a>Obtenir et activer le complément de Message de rapport pour votre organisation

> [!IMPORTANT]
> Vous devez être administrateur Exchange Online pour effectuer cette tâche.
  
1. Accédez à [https://portal.office.com](https://portal.office.com) et connectez-vous à l’aide de votre compte professionnel ou de l’école. 
    
2. Choisissez **Admin** pour accéder au centre d’administration. 
    
3. Choisissez **Centre d’administration** \> **Exchange** pour accéder au centre d’administration Exchange (CAE). 
    
4. Cliquez sur **organisation** \> **des compléments**. 
    
5. Choisissez **+** \> **Ajouter à partir de l’Office Store**. 
    
6. Rechercher les messages d’état.
    
7. Dans la liste des **résultats de l’application** , rechercher **Un Message de rapport**, puis cliquez sur **obtenir maintenant** (ou **Ajouter** ). 
    
8. Passez en revue les termes du contrat de stratégie de confidentialité et d’utilisation. Puis cliquez sur **Continuer**. 
    
    ![Cliquez sur Continuer pour accepter les termes et la politique de confidentialité](media/3c813cd6-1601-4791-97dc-f8edbbd3fb6b.png)
  
9. Dans l’écran de confirmation, cliquez sur **Oui**. 
    
10. Après avoir installé le complément de Message de rapport, vous devez l’activer. Pour cela, procédez comme suit :
    
1. Revenez au CAE et actualiser la fenêtre du navigateur.
    
2. Cliquez sur **organisation** \> **des compléments**. 
    
3. Dans la liste des compléments, sélectionnez **Rapport de Message**. 
    
    ![Dans le centre d’administration Exchange, vous pouvez activer le complément de Message de rapport pour Outlook](media/b496743c-55fa-4cdb-aa06-0b2a7aec6dab.png)
  
4. Choisissez **Modifier**et sélectionnez une option pour activer le complément. 
    
    ![Activer le complément de Message de rapport dans le CAE](media/578b1b66-3620-4a8a-9819-1c9cc6836f37.png)
  
5. Sélectionnez **Enregistrer**. 
    
> [!TIP]
> Une fois que le complément est installé et activé, les personnes dans votre organisation voyez seront afficher les icônes suivantes : 
  
Ensuite, découvrez comment [utiliser le complément de Message de rapport](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)et configurer une règle pour voir les messages électroniques signalés.
  
### <a name="set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users"></a>Définir une règle pour obtenir une copie des messages électroniques signalés par vos utilisateurs

> [!IMPORTANT]
> Vous devez être administrateur Exchange Online pour effectuer cette tâche.
  
Vous pouvez configurer une règle pour obtenir une copie des messages électroniques signalés par les utilisateurs de votre organisation. Cela après avoir téléchargé et activé le complément de Message de rapport pour votre organisation.
  
1. Dans le centre d’administration Exchange, choisissez **flux de messagerie** \> **règles**. 
    
2. Choisissez **+** \> **créer une nouvelle règle**. 
    
3. Dans la zone **nom** , tapez un nom, tel que des envois.
    
4. Dans la liste **appliquer cette règle si** , sélectionnez **l’adresse du destinataire inclut...**. 
    
5. Dans l’écran **spécifier les mots ou expressions** , ajoutez junk@office365.microsoft.com et phish@office365.microsoft.com, puis cliquez sur **OK**. 
    
    ![Spécifier les adresses de courrier indésirable et de phishing pour la règle](media/018c1833-f336-4333-a45c-f2e8b75cd698.png)
  
6. Dans la liste **effectuer les opérations suivantes** , choisissez **Cci du message pour...**. 
    
7. Ajouter un administrateur global, un administrateur de sécurité et/ou lecteur de sécurité qui doit recevoir une copie de chaque message électronique qui signalent à Microsoft les personnes, puis cliquez sur **OK**. 
    
    ![Ajouter un administrateur global ou de sécurité pour recevoir une copie de chaque message signalé](media/a91ab9d1-66f2-4a2e-9dc1-f9f81a2298ad.png)
  
8. Sélectionnez **Auditer cette règle avec le niveau de gravité**, puis choisissez **moyenne**. 
    
9. Sous **Choisir un mode de cette règle**, cliquez sur **Appliquer**. 
    
    ![Définir une règle pour obtenir une copie de chaque message signalé](media/f1cd95ce-e40d-4a8a-8f48-893469eba691.png)
  
10. Sélectionnez **Enregistrer**. 
    
À cette règle en place, chaque fois qu’une personne de votre organisation signale un message électronique à l’aide du complément Message de rapport, votre administrateur général, administrateur de sécurité et/ou lecteur sécurité reçoit une copie de ce message. Ces informations permettent de vous permet de définir ou ajuster les stratégies, telles que les stratégies de [Liaisons sans échec de Office 365 DAV](atp-safe-links.md) . 
  
## <a name="related-topics"></a>Voir aussi

[Utiliser le complément de Message de rapport](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)
  
[Protection de Microsoft Office 365 menace avancées](office-365-atp.md)
  

