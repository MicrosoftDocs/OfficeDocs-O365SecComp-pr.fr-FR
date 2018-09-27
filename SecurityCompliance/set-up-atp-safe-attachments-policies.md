---
title: Définir des stratégies Office 365 DAV approuvés en pièce jointe
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 5/8/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 078eb946-819a-4e13-8673-fe0c0ad3a775
description: Définir des stratégies de pièces jointes fiables pour protéger votre organisation à partir des fichiers malveillants dans le message électronique.
ms.openlocfilehash: bc52522a45071776835efe20f57cf37c415d2436
ms.sourcegitcommit: 9826013c3e0532ae5d01b3d88a14691f8dd0f6b7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/27/2018
ms.locfileid: "25092940"
---
# <a name="set-up-office-365-atp-safe-attachments-policies"></a>Définir des stratégies Office 365 DAV approuvés en pièce jointe

Personnes régulièrement envoient, recevoir et partager des pièces jointes, telles que des documents, des présentations, des feuilles de calcul et plus. Il n’est pas toujours facile de savoir si une pièce jointe est fiable ou malveillante juste en regardant à un message électronique. Et la dernière chose que vous souhaitez passer, une pièce jointe qui peuvent faire les conséquences pour votre organisation. Heureusement, [Contre les menaces avancées Office 365](office-365-atp.md) (DAV) peut vous aider. Vous pouvez définir des stratégies de [Pièces jointes sûres DAV](atp-safe-attachments.md) pour vous assurer que votre organisation est protégée contre les attaques par les pièces jointes de courrier électronique non sécurisés. 
  
## <a name="what-to-do"></a>Procédure 
  
1. [Passez en revue les conditions préalables](#review-the-prerequisites)
    
2. [Configurer une stratégie de pièces jointes sûres DAV](#set-up-an-atp-safe-attachments-policy)
    
3. [En savoir plus sur les options de stratégie de pièces jointes sûres DAV](#learn-about-atp-safe-attachments-policy-options)
    
## <a name="step-1-review-the-prerequisites"></a>Étape 1 : Vérifier les conditions préalables

- Assurez-vous que votre organisation dispose [d’Office 365 avancée protection contre les menaces](office-365-atp.md).
    
- Assurez-vous que vous avez nécessaires [autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md).
    
- [Découvrez les options de stratégie de pièces jointes sûres DAV](#learn-about-atp-safe-attachments-policy-options) (dans cet article). Certaines options, telles que les options de surveiller ou de remplacement, peuvent entraîner un délai d’attente secondaire des courriers électroniques tandis que les pièces jointes sont analysés. Pour éviter les retards de message, envisagez d’utiliser [une remise dynamique et l’aperçu](dynamic-delivery-and-previewing.md).
    
- Autoriser jusqu'à 30 minutes pour votre stratégie de nouveau ou mis à jour pour se propager sur tous les centres de données Office 365.
    
## <a name="step-2-set-up-or-edit-an-atp-safe-attachments-policy"></a>Étape 2 : Configurer une stratégie de pièces jointes sûres DAV (ou en modifier)

> [!TIP]
> Vous pouvez configurer une stratégie de pièces jointes sûres DAV en utilisant le Office 365 Security &amp; centre de conformité ou le centre d’administration Exchange (CAE). **Nous recommandons l’utilisation de la sécurité de 365 Office &amp; centre de conformité**. 
  
1. En tant qu’un administrateur global ou administrateur de sécurité, accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous avec votre compte professionnel ou de l’école. 
    
2. De sécurité Office 365 &amp; centre de conformité, dans le volet de navigation de gauche, sous **Gestion des menaces**, choisissez **stratégie** \> **Pièces jointes fiables**.
    
3. Si vous voyez **Activer DAV pour SharePoint, OneDrive et les équipes Microsoft**, nous vous recommandons de sélectionner cette option. Cela permettra [d’Office 365 avancée protection contre les menaces pour SharePoint, OneDrive et les équipes Microsoft](atp-for-spo-odb-and-teams.md) pour votre environnement Office 365. 
    
4. Choisissez **Nouveau** (nouveau bouton ressemble à un signe plus ( **+**)) pour commencer à créer votre stratégie.
    
5. Spécifiez le nom, description et paramètres de la stratégie.
    
    **Exemple :** Pour configurer une stratégie appelée « sans retard » qui offre des messages de tout le monde immédiatement et puis rattache les pièces jointes une fois qu’ils sont analysés, vous pouvez spécifier les paramètres suivants : 
    
      - Dans la zone **nom** , tapez sans retard.
    
      - Dans la zone **Description** , tapez une description comme remet immédiatement les messages et les pièces jointes rattache après l’analyse.
    
      - Dans la section réponse, choisissez l’option de **Distribution dynamique** . ([En savoir plus sur la remise dynamique et aperçu des pièces jointes sûres DAV](dynamic-delivery-and-previewing.md)).
    
      - Dans la section **Rediriger la pièce jointe** , sélectionnez l’option pour activer la redirection et tapez l’adresse de messagerie de votre administrateur général, administrateur de sécurité ou analyste de sécurité qui va étudier les pièces jointes malveillants Office 365. 
    
      - Dans la section **Appliquée à** , choisissez **le domaine du destinataire est**, puis sélectionnez votre domaine. Cliquez sur **Ajouter**, puis cliquez sur **OK**.
    
6. Sélectionnez **Enregistrer**.
    
Pensez à configurer plusieurs stratégies de pièces jointes sûres DAV pour votre organisation. Ces stratégies seront appliquées dans l’ordre, qu'elles apparaissent dans la page **Pièces jointes sûres DAV** . Une fois une stratégie a été définie ou modifiée, permettre au moins 30 minutes pour les stratégies en vigueur au sein de centres de données Microsoft. 
  
## <a name="step-3-learn-about-atp-safe-attachments-policy-options"></a>Étape 3 : En savoir plus sur les options de stratégie de pièces jointes sûres DAV

Lorsque vous définissez vos stratégies de pièces jointes sûres DAV, vous choisissez parmi plusieurs options, notamment le moniteur, bloquer, remplacer, remise dynamique et ainsi de suite. Si vous vous demandez que faire ces options, le tableau suivant résume chacun et son effet.
  
|**Option**|**Effet**|**À utiliser lorsque vous souhaitez :**|
|:-----|:-----|:-----|
|**Off** <br/> |N’analyse pas les pièces jointes des programmes malveillants  <br/> Ne retarde pas la remise du message  <br/> |Désactiver l’analyse pour des expéditeurs internes, scanneurs, télécopies ou hôtes actifs qui permet uniquement d’envoyer des pièces jointes connus et en bonnes  <br/> Empêcher des retards de routage des messages internes  <br/> **Cette option n’est pas recommandée pour la plupart des utilisateurs. Elle vous permet de désactiver l’analyse des pièces jointes sûres DAV pour un petit groupe d’expéditeurs internes.**           |
|**Moniteur** <br/> |Remet les messages contenant des pièces jointes et puis suit ce qui se passe par un programme malveillant détecté  <br/> |Voir où vont de détection de programmes malveillants dans votre organisation  <br/> |
|**Bloc** <br/> |Empêche les messages contenant des pièces jointes de logiciel malveillant détecté de procédure  <br/> Envoie des messages par un programme malveillant détecté à la [mise en quarantaine dans Office 365](manage-quarantined-messages-and-files.md) où un administrateur ou un analyste peut consulter et version (ou supprimer) des messages  <br/> Bloque automatiquement les pièces jointes et les messages à venir  <br/> |Protéger votre organisation contre les attaques répétées à l’aide des même pièces jointes de programmes malveillants  <br/> |
|**Remplacement** <br/> |Supprime détecté des pièces jointes de programmes malveillants  <br/> Avertit les destinataires que les pièces jointes ont été supprimées.  <br/> Envoie des messages par un programme malveillant détecté à la [mise en quarantaine dans Office 365](manage-quarantined-messages-and-files.md) où un administrateur ou un analyste peut consulter et version (ou supprimer) des messages  <br/> |Augmenter la visibilité aux destinataires que les pièces jointes ont été supprimées en raison de logiciel malveillant détecté  <br/> |
|**Remise dynamique** <br/> |Remet les messages immédiatement  <br/> Remplace les pièces jointes avec un fichier d’espace réservé jusqu'à ce que l’analyse est terminée, puis rattache les pièces jointes si aucun programme malveillant n’est détecté  <br/> Inclut les pièces jointes afficher un aperçu des fonctionnalités pour la plupart des fichiers PDF et Office fichiers lors de l’analyse  <br/> Envoie des messages par un programme malveillant détecté à la mise en quarantaine où un administrateur ou un analyste peut consulter et version (ou supprimer) des messages  <br/> [En savoir plus sur la remise dynamique et aperçu des pièces jointes sûres DAV](dynamic-delivery-and-previewing.md) <br/> |Éviter les retards de message lors de la protection des destinataires à partir des fichiers malveillants  <br/> Activer l’aperçu des pièces jointes en mode sans échec pendant l’analyse des destinataires  <br/> |
|**Activer la redirection** <br/> |S’applique lorsque vous choisissez l’option moniteur, bloquer ou remplacer  <br/> Envoie les pièces jointes à une adresse de messagerie spécifiée où les administrateurs de sécurité ou analystes peuvent étudier  <br/> |Permettre aux administrateurs de sécurité et les analystes à la recherche de pièces jointes suspectes  <br/> |
   
## <a name="related-topics"></a>Voir aussi

[Office 365 - Protection avancée contre les menaces](office-365-atp.md)
  
[Pièces jointes DAV Safe dans Office 365](atp-safe-attachments.md)
  
[Liens DAV Safe dans Office 365](atp-safe-links.md)
  
[Définir des stratégies de liens fiables DAV dans Office 365](set-up-atp-safe-links-policies.md)
  
[Afficher les rapports de protection contre les menaces avancées](view-reports-for-atp.md)

[Autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md)
  

