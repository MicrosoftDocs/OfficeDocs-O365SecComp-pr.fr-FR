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
ms.openlocfilehash: 3ffd8b65d6994699093237e9f9a0a3aaa802f5e2
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30223083"
---
# <a name="removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email"></a>Suppression d’un utilisateur, d’un domaine ou d’une adresse IP d’une liste rouge après l’envoi de courrier indésirable

Si un utilisateur envoie continuellement des messages électroniques à partir d'Office 365 classé comme courrier indésirable, ils ne pourront plus envoyer d'autres messages. L'utilisateur est mentionné dans le service en tant qu'expéditeur sortant incorrect et reçoit une notification d'échec de remise qui indique:

- Votre message n'a pas pu être remis car vous n'avez pas été reconnu comme un expéditeur valide. La raison la plus fréquente de ce message est que votre adresse de courrier est suspecte d'envoyer du courrier indésirable et qu'elle n'est plus autorisée à envoyer des messages en dehors de votre organisation. Contactez votre administrateur de courrier électronique pour obtenir de l'aide.  Le serveur distant a renvoyé' 550 5.1.8 accès refusé, expéditeur sortant incorrect "

Les administrateurs de client reçoivent également une alerte indiquant que l'utilisateur n'a pas été autorisé à envoyer des messages sortants supplémentaires.

## <a name="what-do-you-need-to-know-before-you-begin"></a>Ce qu'il faut savoir avant de commencer
<a name="sectionSection0"> </a>

Durée d’exécution estimée : 5 minutes
  
Des autorisations doivent vous être attribuées avant de pouvoir effectuer cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez la rubrique «entrée anti-courrier indésirable dans la rubrique [autorisations des fonctionnalités dans Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) .

La procédure suivante peut également être effectuée via PowerShell à distance. Utilisez la cmdlet Get-BlockedSenderAddress pour obtenir la liste des utilisateurs avec accès restreint et Remove-BlockedSenderAddress pour supprimer la restriction. Pour savoir comment utiliser Windows PowerShell pour se connecter à Exchange Online, consultez la rubrique [connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).

## <a name="remove-restrictions-for-a-blocked-office-365-email-account"></a>Supprimer les restrictions pour un compte de messagerie Office 365 bloqué

Vous effectuez cette tâche dans le centre de sécurité & conformité Office 365 (SCC). [Accédez au centre de sécurité & de sécurité Office 365](go-to-the-securitycompliance-center.md) pour plus d'informations sur SCC. Vous devez être dans le groupe de rôles gestion de l' **organisation** ou **administrateur de sécurité** pour effectuer ces fonctions. [Accédez à autorisations dans le centre de sécurité & de la sécurité Office 365](permissions-in-the-security-and-compliance-center.md) pour plus d'informations sur les groupes de rôles SCC.

1. À l'aide d'un compte professionnel ou scolaire disposant de privilèges d'administrateur général Office 365, connectez-vous au centre de sécurité et conformité Office 365 et, dans la liste de gauche, développez **gestion des menaces**, choisissez **examiner**, puis choisissez **restreint. Les utilisateurs**.
    
    > [!TIP]
    > Pour accéder directement à la page **utilisateurs restreints** (anciennement appelé centre de maintenance) dans le &amp; Centre de sécurité conformité, utilisez l'URL suivante: >[https://protection.office.com/?hash=/restrictedusers](https://protection.office.com/?hash=/restrictedusers)

2. Cette page contient la liste des utilisateurs qui ont été bloqués pour l'envoi de messages à l'extérieur de votre organisation.  Recherchez l'utilisateur pour lequel vous souhaitez supprimer les restrictions, puis cliquez **** sur débloquer.

3. Cliquez sur **Oui** pour confirmer la modification. 
    
> [!NOTE]
> Le nombre de fois qu'un compte peut être débloqué par l'administrateur client est limité. Si la limite pour un utilisateur a été dépassée, un message d'erreur s'affiche. Vous devrez ensuite contacter le support technique pour débloquer l'utilisateur.<br/><br/> La déblocage de l'utilisateur peut prendre jusqu'à 1 heure.
  
## <a name="third-party-block-lists"></a>Listes rouges tierces

Exchange Online Protection utilise également des listes rouges tierces pour vous aider à prendre des décisions en matière de filtrage du courrier indésirable. Les utilisateurs, les sites Web, les domaines et les adresses IP peuvent être ajoutés aux listes bloquées uniquement pour apparaître dans un message de courrier indésirable. En tant qu'administrateur Office 365, vous devez essayer d'obtenir ces objets supprimés des fournisseurs de liste tiers s'ils vous appartiennent.

> [!NOTE]
> Si une personne extérieure à Office 365 ne peut pas envoyer de messages à votre compte Office 365, il se peut que son compte figure dans la liste des expéditeurs bloqués externes. Les utilisateurs externes à Office 365 peuvent essayer de se supprimer eux-mêmes à l'aide du portail de retrait [libre-service](https://docs.microsoft.com/en-us/office365/SecurityCompliance/use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis). 

## <a name="for-more-information"></a>Pour plus d’informations

[Réponse à un compte de messagerie compromis](responding-to-a-compromised-email-account.md)

[Configurer la stratégie anti-courrier indésirable sortant](configure-the-outbound-spam-policy.md)
  
[Pool de remise à risque élevé pour les messages sortants](high-risk-delivery-pool-for-outbound-messages.md)

[Autorisations dans le centre de sécurité & de sécurité Office 365](permissions-in-the-security-and-compliance-center.md)

  

