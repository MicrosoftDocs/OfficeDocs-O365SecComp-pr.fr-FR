---
title: Suppression d'un utilisateur du portail utilisateurs restreints après l'envoi du courrier indésirable
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 03/12/2019
ms.audience: ITPro
ms.topic: article
f1_keywords:
- ms.exch.eac.ActionCenter.Restricted.Users.RestrictedUsers
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 712cfcc1-31e8-4e51-8561-b64258a8f1e5
ms.collection:
- M365-security-compliance
description: Si un utilisateur envoie continuellement des courriers électroniques à partir d'Office 365 classés comme courrier indésirable, il ne pourra pas envoyer d'autres messages.
ms.openlocfilehash: c775887ecfa136bd638d0b76050c7882a6219ae4
ms.sourcegitcommit: f86383dcb9c52352661d51b22617f1809445beaa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/14/2019
ms.locfileid: "30573518"
---
# <a name="removing-a-user-from-the-restricted-users-portal-after-sending-spam-email"></a>Suppression d'un utilisateur du portail utilisateurs restreints après l'envoi du courrier indésirable

Si un utilisateur envoie continuellement des courriers électroniques à partir d'Office 365 classés comme courrier indésirable, il ne sera pas autorisé à envoyer d'autres messages sortants. L'utilisateur est mentionné dans le service en tant qu'expéditeur sortant incorrect et reçoit une notification d'échec de remise qui indique:

- Votre message n'a pas pu être remis car vous n'avez pas été reconnu comme un expéditeur valide. La raison la plus fréquente de ce message est que votre adresse de courrier est suspecte d'envoyer du courrier indésirable et qu'elle n'est plus autorisée à envoyer des messages en dehors de votre organisation. Contactez votre administrateur de courrier électronique pour obtenir de l'aide. Le serveur distant a renvoyé' 550 5.1.8 accès refusé, expéditeur sortant incorrect "

## <a name="what-do-you-need-to-know-before-you-begin"></a>Ce qu'il faut savoir avant de commencer
<a name="sectionSection0"> </a>

Durée d'exécution estimée : 5 minutes
  
Des autorisations doivent vous être attribuées avant de pouvoir exécuter cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez la rubrique «entrée anti-courrier indésirable dans la rubrique [autorisations des fonctionnalités dans Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) .

La procédure suivante peut également être exécutée par le biais du service PowerShell à distance. Utilisez la cmdlet Get-BlockedSenderAddress pour obtenir la liste des utilisateurs avec accès restreint et Remove-BlockedSenderAddress pour supprimer la restriction. Pour apprendre à utiliser Windows PowerShell afin de vous connecter à Exchange Online, consultez la rubrique [Connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).

## <a name="remove-restrictions-for-a-blocked-office-365-email-account"></a>Supprimer les restrictions pour un compte de messagerie Office 365 bloqué

Vous effectuez cette tâche dans le centre de sécurité & conformité Office 365 (SCC). [Accédez au centre de sécurité & de sécurité Office 365](go-to-the-securitycompliance-center.md) pour plus d'informations sur SCC. Vous devez être dans le groupe de rôles gestion de l' **organisation** ou **administrateur de sécurité** pour effectuer ces fonctions. [Accédez à autorisations dans le centre de sécurité & de la sécurité Office 365](permissions-in-the-security-and-compliance-center.md) pour plus d'informations sur les groupes de rôles SCC.

1. À l'aide d'un compte professionnel ou scolaire disposant de privilèges d'administrateur général Office 365, connectez-vous au centre de sécurité et conformité Office 365 et, dans la liste de gauche, développez **gestion des menaces**, choisissez **examiner**, puis choisissez **restreint. Les utilisateurs**.
    
    > [!TIP]
    > Pour accéder directement à la page **utilisateurs restreints** (anciennement appelé centre de maintenance) dans le &amp; Centre de sécurité conformité, utilisez l'URL suivante: >[https://protection.office.com/#/restrictedusers](https://protection.office.com/?hash=/restrictedusers)

2. Cette page contient la liste des utilisateurs qui ont été bloqués pour l'envoi de messages à l'extérieur de votre organisation.  Recherchez l'utilisateur pour lequel vous souhaitez supprimer les restrictions, puis cliquez **** sur débloquer.

3. Un passage vers l'extérieur indiquera les détails du compte dont l'envoi est restreint. Vous devez passer en revue les recommandations pour vous assurer que vous prenez les mesures appropriées au cas où le compte est réellement compromis. Cliquez sur **suivant** lorsque vous avez fini.

4. L'écran suivant contient des recommandations pour vous aider à éviter toute compromission ultérieure. L'activation de l'authentification multifacteur (MFA) et la modification des mots de passe constituent une excellente défense. Cliquez sur déBloquer l' **utilisateur** lorsque vous avez fini.

5. Cliquez sur **Oui** pour confirmer la modification.

    > [!NOTE]
    > La suppression des restrictions peut prendre jusqu'à 30 minutes. 

## <a name="making-sure-admins-are-alerted-when-this-happens"></a>S'assurer que les administrateurs sont alertés lorsque cela se produit

Les administrateurs de client reçoivent également une alerte indiquant que l'utilisateur n'a pas été autorisé à envoyer des messages sortants supplémentaires. Il s'agit d'une alerte par défaut fournie pour tous les clients et est indiquée dans la page stratégies d'alerte SCC, intitulée «utilisateur restreint de l'envoi de courrier électronique». Pour plus d'informations sur l'alerte, accédez à [stratégies d'alerte dans le centre de sécurité _AMP_ Office 365](https://docs.microsoft.com/en-us/office365/securitycompliance/alert-policies) .

## <a name="for-more-information"></a>Pour plus d'informations

[Réponse à un compte de messagerie compromis](responding-to-a-compromised-email-account.md)

[Présentation de l'alerte utilisateur restreinte de l'envoi de messages électroniques](https://docs.microsoft.com/en-us/office365/securitycompliance/alert-policies)

[Pool de remise à risque élevé pour les messages sortants](high-risk-delivery-pool-for-outbound-messages.md)

[Autorisations dans le centre de sécurité & de sécurité Office 365](permissions-in-the-security-and-compliance-center.md)
