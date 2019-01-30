---
title: Suppression d’un utilisateur, d’un domaine ou d’une adresse IP d’une liste rouge après l’envoi de courrier indésirable
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/01/2018
ms.audience: ITPro
ms.topic: article
f1_keywords:
- ms.exch.eac.ActionCenter
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 712cfcc1-31e8-4e51-8561-b64258a8f1e5
description: 'Si un utilisateur envoie en continu des messages électroniques classés comme courriers indésirables depuis Office 365, ses envois seront bloqués. '
ms.openlocfilehash: 6f6f4504a9c79463aadc21f2eaeadcd769e8b151
ms.sourcegitcommit: 03b9221d9885bcde1cdb5df2c2dc5d835802d299
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29614398"
---
# <a name="removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email"></a>Suppression d’un utilisateur, d’un domaine ou d’une adresse IP d’une liste rouge après l’envoi de courrier indésirable

Si un utilisateur envoie des messages électroniques en continu d’Office 365 qui est considéré comme du courrier indésirable, ils seront bloquées d’envoyer plus de messages. L’utilisateur est répertorié dans le service en tant qu’incorrect sortant expéditeur et reçoit un rapport de remise (NDR) indique :

- Votre message n’a pas pu être remis car vous n’ont pas été reconnue comme un expéditeur valide. La raison la plus courante est que votre adresse de messagerie est soupçonné d’envoyer du courrier indésirable et qu’il a n’est plus autorisé à envoyer des messages à l’extérieur de votre organisation. Contactez votre administrateur de messagerie.  Serveur distant a retourné « 550 5.1.8 accès refusé, expéditeur sortant incorrecte »

Les administrateurs de client reçoit également une alerte indiquant que l’utilisateur a été restreint d’envoyer des messages sortants plus.

## <a name="what-do-you-need-to-know-before-you-begin"></a>Ce qu'il faut savoir avant de commencer
<a name="sectionSection0"> </a>

Durée d’exécution estimée : 5 minutes
  
Vous devez avoir les autorisations avant de pouvoir effectuer cette procédure, ou procédures. Pour voir les autorisations dont vous avez besoin, consultez la rubrique « entrée anti-spam dans la rubrique [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) .

La procédure suivante peut également être effectuée par le biais de PowerShell à distance. Utilisez l’applet de commande Get-BlockedSenderAddress pour obtenir la liste des utilisateurs restreints et Remove-BlockedSenderAddress permet de supprimer la restriction. Pour savoir comment utiliser Windows PowerShell pour se connecter à Exchange Online, voir [se connecter à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).

## <a name="remove-restrictions-for-a-blocked-office-365-email-account"></a>Supprimer les restrictions pour un compte de messagerie Office 365 bloqué

Vous effectuez cette tâche dans le & de sécurité pour Microsoft Office 365 centre de conformité (SCC). Pour plus d’informations sur le contrôle de code source, [accédez à la & Office 365 sécurité Centre de conformité](go-to-the-securitycompliance-center.md) . Vous devez être dans la **Gestion de l’organisation** ou le groupe de rôles **d’Administrateur de sécurité** pour pouvoir exécuter ces fonctions. Pour plus d’informations sur les groupes de rôles de contrôle de code source, [accédez à autorisations dans le centre de conformité de & Office 365 sécurité](permissions-in-the-security-and-compliance-center.md) .

1. À l’aide d’un compte disposant de privilèges d’administrateur général Office 365, vous connecter dans le centre de conformité et de sécurité pour Microsoft Office 365 et dans la liste de gauche, développez **Threat Management**, sélectionnez **passer en revue les**, puis **Restricted Professionnel ou de l’école Les utilisateurs**.
    
    > [!TIP]
    > Pour accéder directement à la page **Utilisateurs restreints** (anciennement appelé le centre d’Action) de la sécurité &amp; centre de conformité, utilisez l’URL suivante : >[https://protection.office.com/?hash=/restrictedusers](https://protection.office.com/?hash=/restrictedusers)

2. Cette page contient la liste des utilisateurs qui ont été bloqués à partir de l’envoi de courrier à l’extérieur de votre organisation.  Recherchez l’utilisateur que vous souhaitez supprimer les restrictions sur, puis cliquez sur **Débloquer**.

3. Cliquez sur **Oui** pour confirmer la modification. 
    
> [!NOTE]
> Il existe une limite au nombre de fois qu’un compte peut être non bloquée par l’administrateur du client. Si la limite d’un utilisateur a été dépassée, un message d’erreur s’affiche. Vous devrez contacter le Support pour débloquer l’utilisateur.</br></br> Il peut prendre jusqu'à 1 heure avant que l’utilisateur soit débloquer.
  
## <a name="third-party-block-lists"></a>Listes rouges tierces

Exchange Online Protection utilise également des listes rouges tiers pour aider à prendre des décisions de filtrage du courrier indésirable. Les utilisateurs, des sites Web, des domaines et des adresses IP peuvent être ajoutés pour bloquer des listes figurant dans un message de courrier indésirable pour. En tant que l’administrateur Office 365, vous devriez obtenir ces objets supprimés des fournisseurs de listes de tiers si elles vous appartient.

> [!NOTE]
> Si une personne extérieure à Office 365 ne peuvent pas envoyer des messages à votre compte Office 365, leur compte peut se trouver sur la liste des expéditeurs bloqués externe. Les utilisateurs en dehors d’Office 365 peuvent tenter de se supprimer à l’aide du [portail libre-service de retrait de la liste](https://docs.microsoft.com/en-us/office365/SecurityCompliance/use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis). 

## <a name="for-more-information"></a>Pour plus d’informations

[Répondre à un compte de messagerie compromis](responding-to-a-compromised-email-account.md)

[Configurer la stratégie anti-courrier indésirable sortant](configure-the-outbound-spam-policy.md)
  
[Pool de remise à risque élevé pour les messages sortants](high-risk-delivery-pool-for-outbound-messages.md)

[Autorisations dans le centre de conformité de & de sécurité Office 365](permissions-in-the-security-and-compliance-center.md)

  

