---
title: Configuration des stratégies de pièces jointes approuvées ATP Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.date: 02/06/2019
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 078eb946-819a-4e13-8673-fe0c0ad3a775
ms.collection: M365-security-compliance
description: Définir des stratégies de pièces jointes approuvées pour protéger votre organisation contre les fichiers malveillants par courrier électronique.
ms.openlocfilehash: 782412cb39bf72676570c5a20344011449d878a8
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214564"
---
# <a name="set-up-office-365-atp-safe-attachments-policies"></a>Configuration des stratégies de pièces jointes approuvées ATP Office 365

Les personnes envoient, reçoivent et partagent régulièrement des pièces jointes, telles que des documents, des présentations, des feuilles de calcul, etc. Il n'est pas toujours facile de déterminer si une pièce jointe est fiable ou malveillante en regardant un message électronique. Et la dernière chose que vous souhaitez, c'est une pièce jointe malveillante à utiliser pour votre organisation. Heureusement, [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP) peut vous aider. Vous pouvez configurer des stratégies de [pièces jointEs approuvéEs ATP](atp-safe-attachments.md) pour vous assurer que votre organisation est protégée contre les attaques par des pièces jointes non sûres. 
  
## <a name="what-to-do"></a>Procédure 
  
1. [Vérifier les conditions préalables](#review-the-prerequisites)
    
2. [Configurer une stratégie de pièces jointes approuvées ATP](#set-up-an-atp-safe-attachments-policy)
    
3. [En savoir plus sur les options de stratégie de pièces jointes ATP](#learn-about-atp-safe-attachments-policy-options)
    
## <a name="step-1-review-the-prerequisites"></a>Étape 1: vérifier les conditions préalables

- Assurez-vous que votre organisation dispose de la [protection avancée contre les menaces d'Office 365](office-365-atp.md).
    
- Assurez-vous que vous disposez des autorisations nécessaires. Pour définir (ou modifier) des stratégies ATP, vous devez disposer d'un rôle approprié. Certains exemples sont décrits dans le tableau suivant: <br>

    |Rôle  |WHERE/How Assigned  |
    |---------|---------|
    |Administrateur général Office 365 |La personne qui s'inscrit pour acheter Office 365 est un administrateur global par défaut. (Pour en savoir plus, consultez la rubrique [à propos des rôles d'administrateur Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) .)         |
    |Administrateur de sécurité |Centre d'administration Azure Active Directory[https://aad.portal.azure.com](https://aad.portal.azure.com)()|
    |Gestion de l'organisation Exchange Online |Centre d'administration Exchange[https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)() <br>ou <br>  Applets de commande PowerShell (consultez la rubrique [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)) |
    
    Pour en savoir plus sur les rôles et les autorisations, consultez [la rubrique autorisations &amp; dans le centre de sécurité conformité Office 365](permissions-in-the-security-and-compliance-center.md).

- [En savoir plus sur les options de stratégie de pièces jointES ATP](#learn-about-atp-safe-attachments-policy-options) (dans cet article). Certaines options, telles que le moniteur ou les options de remplacement, peuvent entraîner un retard mineur du courrier électronique lors de l'analyse des pièces jointes. Pour éviter les retards de message, envisagez d'utiliser la [remise et l'aperçu dynamiques](dynamic-delivery-and-previewing.md).
    
- Attendez jusqu'à 30 minutes que votre stratégie nouvelle ou mise à jour se propage à tous les centres de mises à jour Office 365.
    
## <a name="step-2-set-up-or-edit-an-atp-safe-attachments-policy"></a>Étape 2: configurer (ou modifier) une stratégie de pièces jointes approuvées ATP
  
1. Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous avec votre compte professionnel ou scolaire. 
    
2. dans le centre de sécurité &amp; conformité Office 365, dans le volet de navigation de gauche, sous **gestion des menaces**, sélectionnez stratégie de **pièces jointes approuvées**par la **stratégie** \> .
    
3. Si vous voyez activer la protection avancée contre **les menaces pour SharePoint, OneDrive et Microsoft teams**, nous vous recommandons de sélectionner cette option. Cette opération active [office 365 protection avancée contre les menaces pour SharePoint, OneDrive et Microsoft teams](atp-for-spo-odb-and-teams.md) pour votre environnement Office 365. 
    
4. Sélectionnez **nouveau** (le nouveau bouton ressemble à un signe plus ( **+**)) pour commencer à créer votre stratégie.
    
5. Spécifiez le nom, la description et les paramètres de la stratégie.<br/><br/>**Exemple:** Pour configurer une stratégie appelée «pas de retard» qui remet immédiatement les messages de tout le monde, puis relie les pièces jointes après leur analyse, vous pouvez spécifier les paramètres suivants: 
    
      - Dans la zone **nom** , tapez aucun délai.
    
      - Dans la zone **Description** , tapez une description comme, remet immédiatement les messages et rattache les pièces jointes après l'analyse.
    
      - Dans la section réponse, sélectionnez l'option **remise dynamique** . ([En savoir plus sur la remise et l'aperçu dynamiques avec des pièces jointEs fiables ATP](dynamic-delivery-and-previewing.md).)
    
      - Dans la section **pièce jointe** de redirection, sélectionnez l'option permettant d'activer la redirection et tapez l'adresse de messagerie de votre administrateur général Office 365, administrateur de la sécurité ou analyste de sécurité qui analysera les pièces jointes malveillantes. 
    
      - Dans la section **appliqué à** , choisissez **le domaine du destinataire**, puis sélectionnez votre domaine. Choisissez **Ajouter**, puis choisissez **OK**.
    
6. Sélectionnez **Save (Enregistrer)**.
    
EnVisagez de configurer plusieurs stratégies de pièces jointes approuvées pour votre organisation. Ces stratégies seront appliquées dans l'ordre dans lequel elles apparaissent dans la page **pièces jointEs approuvéEs ATP** . Une fois qu'une stratégie a été définie ou modifiée, laissez au moins 30 minutes que les stratégies prennent effet dans tous les centres de connaissances Microsoft. 
  
## <a name="step-3-learn-about-atp-safe-attachments-policy-options"></a>Étape 3: découvrir les options de stratégie de pièces jointes approuvées ATP

Lorsque vous configurez vos stratégies de pièces jointes approuvées ATP, vous pouvez choisir parmi plusieurs options, notamment surveiller, bloquer, remplacer, remise dynamique, etc. Si vous vous posez des éventuelles précisions sur la signification de ces options, le tableau suivant résume chacun et ses effets.
  
|**Option**|**Effet**|**À utiliser lorsque vous souhaitez:**|
|:-----|:-----|:-----|
|**Off** <br/> |N'analyse pas les pièces jointes pour les programmes malveillants  <br/> Ne retarde pas la remise des messages  <br/> |Désactivation de l'analyse pour les expéditeurs internes, les scanneurs, les télécopies ou les hôtes actifs qui envoient uniquement des pièces jointes connues ou connues  <br/> Empêcher les retards inutiles dans le routage du courrier interne  <br/> **Cette option n'est pas recommandée pour la plupart des utilisateurs. Elle vous permet d'activer l'analyse des pièces jointes sûres ATP pour un petit groupe d'expéditeurs internes.**           |
|**Moniteur** <br/> |Remet les messages avec des pièces jointes, puis suit ce qui se produit avec des programmes malveillants détectés  <br/> |Afficher l'emplacement où les programmes malveillants sont détectés dans votre organisation  <br/> |
|**Bloc** <br/> |Empêche la poursuite des messages contenant des pièces jointes malveillantes détectées  <br/> Envoie des messages avec une mise en quarantaine aux programmes malveillants détectés [dans Office 365](manage-quarantined-messages-and-files.md) où un administrateur ou un analyste de la sécurité peut consulter et publier (ou supprimer) ces messages.  <br/> Bloque automatiquement les messages et pièces jointes futurs  <br/> |Protection de votre organisation contre les attaques répétées à l'aide des mêmes pièces jointes  <br/> |
|**Remplacement** <br/> |Supprime les pièces jointes de programmes malveillants détectées  <br/> Avertir les destinataires que des pièces jointes ont été supprimées  <br/> Envoie des messages avec une mise en quarantaine aux programmes malveillants détectés [dans Office 365](manage-quarantined-messages-and-files.md) où un administrateur ou un analyste de la sécurité peut consulter et publier (ou supprimer) ces messages.  <br/> |Augmenter la visibilité aux destinataires pour lesquels les pièces jointes ont été supprimées en raison d'un programme malveillant détecté  <br/> |
|**Remise dynamique** <br/> |Remet immédiatement les messages  <br/> Remplace les pièces jointes par un fichier d'espace réservé jusqu'à ce que l'analyse soit terminée, puis rattache les pièces jointes si aucun programme malveillant n'est détecté  <br/> Inclut les fonctionnalités d'aperçu des pièces jointes pour la plupart des fichiers PDF et Office lors de l'analyse  <br/> Envoie des messages avec des programmes malveillants détectés en quarantaine lorsqu'un administrateur ou un analyste de la sécurité peut consulter et libérer (ou supprimer) ces messages.  <br/> [En savoir plus sur la remise et l'aperçu dynamiques avec des pièces jointes fiables ATP](dynamic-delivery-and-previewing.md) <br/> |Éviter les retards de message tout en protégeant les destinataires des fichiers malveillants  <br/> Autoriser les destinataires à prévisualiser les pièces jointes en mode sans échec lors de l'analyse  <br/> |
|**Activer la redirection** <br/> |S'applique lorsque l'option surveiller, bloquer ou remplacer est sélectionnée  <br/> Envoie des pièces jointes à une adresse de messagerie spécifique que les administrateurs de sécurité ou les analystes peuvent examiner  <br/> |Activer les administrateurs de la sécurité et les analystes pour rechercher des pièces jointes suspectes  <br/> |
   
## <a name="next-steps"></a>Étapes suivantes

Une fois que vos stratégies de pièces jointes approuvées ATP sont en place, vous pouvez voir le fonctionnement de la fonctionnalité ATP pour votre organisation en affichant des rapports. Pour en savoir plus, consultez les ressources suivantes:
- [Afficher les rapports pour Office 365 protection avancée contre les menaces](view-reports-for-atp.md)
- [Utiliser l'Explorateur dans le &amp; Centre de sécurité conformité](use-explorer-in-security-and-compliance.md)

Restez au fait des nouvelles fonctionnalités disponibles dans la protection avancée contre les menaces. consultez la feuille de [route Microsoft 365](https://www.microsoft.com/microsoft-365/roadmap?filters=O365) et découvrez les [nouvelles fonctionnalités qui sont ajoutées à](office-365-atp.md#new-features-in-office-365-atp)la protection avancée contre les menaces.
 