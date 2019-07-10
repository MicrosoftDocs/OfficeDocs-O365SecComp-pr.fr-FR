---
title: Suppression d’un utilisateur du portail Utilisateurs restreints après l’envoi d’un courrier indésirable
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 03/12/2019
audience: ITPro
ms.topic: article
f1_keywords:
- ms.exch.eac.ActionCenter.Restricted.Users.RestrictedUsers
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 712cfcc1-31e8-4e51-8561-b64258a8f1e5
ms.collection:
- M365-security-compliance
description: Si un utilisateur envoie continuellement des courriers électroniques à partir d’Office 365 classés comme courrier indésirable, il ne pourra pas envoyer d’autres messages.
ms.openlocfilehash: 80eb03ccb96f2178f168139234de8700b9b97e29
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35601151"
---
# <a name="removing-a-user-from-the-restricted-users-portal-after-sending-spam-email"></a>Suppression d’un utilisateur du portail Utilisateurs restreints après l’envoi d’un courrier indésirable

Si un utilisateur envoie continuellement des courriers électroniques classés comme courrier indésirable à partir d’Office 365, ils ne seront pas autorisés à envoyer des messages électroniques, mais ils pourront toujours le recevoir. L’utilisateur est mentionné dans le service en tant qu’expéditeur sortant incorrect et reçoit une notification d’échec de remise qui indique:

> «Votre message n’a pas pu être remis car vous n’avez pas été reconnu comme un expéditeur valide. La raison la plus fréquente de ce message est que votre adresse e-mail est suspecte d’envoyer du courrier indésirable et qu’elle n’est plus autorisée à envoyer des courriers électroniques.  Contactez votre administrateur de courrier électronique pour obtenir de l’aide. Le serveur distant a renvoyé' 550 5.1.8 accès refusé, expéditeur sortant incorrect. "

## <a name="what-do-you-need-to-know-before-you-begin"></a>Ce qu’il faut savoir avant de commencer
<a name="sectionSection0"> </a>

Durée d'exécution estimée : 5 minutes
  
Des autorisations doivent vous être attribuées avant de pouvoir exécuter cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez la rubrique «entrée anti-courrier indésirable dans la rubrique [autorisations des fonctionnalités dans Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) .

La procédure suivante peut également être exécutée par le biais du service PowerShell à distance. Utilisez la cmdlet Get-BlockedSenderAddress pour obtenir la liste des utilisateurs avec accès restreint et Remove-BlockedSenderAddress pour supprimer la restriction. Pour apprendre à utiliser Windows PowerShell afin de vous connecter à Exchange Online, consultez la rubrique [Connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).

## <a name="remove-restrictions-for-a-blocked-office-365-email-account"></a>Supprimer les restrictions pour un compte de messagerie Office 365 bloqué

Vous effectuez cette tâche dans le centre de sécurité & conformité (SCC). Pour plus d’informations sur SCC, [accédez au centre de sécurité & Compliance Center](go-to-the-securitycompliance-center.md) . Vous devez être dans le groupe de rôles gestion de l' **organisation** ou **administrateur de sécurité** pour effectuer ces fonctions. Pour plus d’informations sur les groupes de rôles SCC, [accédez à autorisations dans le centre de sécurité & conformité](permissions-in-the-security-and-compliance-center.md) .

1. À l’aide d’un compte professionnel ou scolaire disposant de privilèges d’administrateur général Office 365, connectez-vous au centre de sécurité et conformité Office 365 et, dans la liste de gauche, développez **gestion des menaces**, choisissez **examiner**, puis choisissez **restreint. Les utilisateurs**.
    
    > [!TIP]
    > Pour accéder directement à la page **utilisateurs restreints** (anciennement appelé centre de maintenance) dans le &amp; Centre de sécurité conformité, utilisez l’URL suivante: >[https://protection.office.com/#/restrictedusers](https://protection.office.com/?hash=/restrictedusers)

2. Cette page contient la liste des utilisateurs qui ont été bloqués pour l’envoi de messages électroniques.  Recherchez l’utilisateur dont vous souhaitez supprimer les restrictions, puis sélectionnez **débloquer**.

3. Un passage vers l’extérieur indiquera les détails du compte dont l’envoi est restreint. Vous devez passer en revue les recommandations pour vous assurer que vous prenez les mesures appropriées au cas où le compte est réellement compromis. Cliquez sur **suivant** lorsque vous avez fini.

4. L’écran suivant contient des recommandations pour vous aider à éviter toute compromission ultérieure. L’activation de l’authentification multifacteur (MFA) et la modification des mots de passe constituent une excellente défense. Cliquez sur débloquer l' **utilisateur** lorsque vous avez fini.

5. Cliquez sur **Oui** pour confirmer la modification.

    > [!NOTE]
    > Cette opération peut prendre 30 minutes ou plus avant la suppression des restrictions. 

## <a name="making-sure-admins-are-alerted-when-this-happens"></a>S’assurer que les administrateurs sont alertés lorsque cela se produit

Une alerte «utilisateur restreint à l’envoi de courrier électronique» est disponible sous forme de stratégie sous la page stratégies d’alerte de conformité d’Office 365 Security &. Il s’agissait précédemment de la stratégie de courrier indésirable sortant, qui est désormais native à la plateforme d’alerte Office 365. Pour plus d’informations sur les alertes, accédez à [stratégies d’alerte dans le centre de sécurité & conformité](alert-policies.md) .

> [!IMPORTANT]
> Pour que les alertes fonctionnent, la recherche dans le journal d’audit doit être activée. Pour plus d’informations, reportez-vous à la rubrique [activation ou désactivation de la recherche du journal d’audit Office 365](turn-audit-log-search-on-or-off.md) .

La stratégie pour cette alerte est une stratégie par défaut et est fournie avec tous les clients Office 365 et n’a pas besoin d’être configurée. Elle est considérée comme une alerte de gravité élevée et enverra un courrier électronique au groupe TenantAdmins configuré lorsque l’alerte est déclenchée chaque fois qu’un utilisateur ne peut pas envoyer de courrier. Les administrateurs peuvent mettre à jour le groupe informé lorsque cette alerte se produit en accédant à l’alerte sous le portail SCC > les alertes > les stratégies d’alerte > les utilisateurs ne sont pas autorisés à envoyer des courriers électroniques.

Vous serez en mesure de modifier l’alerte de la façon suivante:
- Activer/désactiver les notifications par courrier électronique
- Envoyer un message électronique aux destinataires requis
- Limiter les notifications que vous recevez par jour

## <a name="for-more-information"></a>Pour plus d’informations

[Réponse à un compte de messagerie compromis](responding-to-a-compromised-email-account.md)

[Présentation de l’alerte utilisateur restreinte de l’envoi de messages électroniques](https://docs.microsoft.com/en-us/office365/securitycompliance/alert-policies)

[Pool de remise à risque élevé pour les messages sortants](high-risk-delivery-pool-for-outbound-messages.md)

[Autorisations dans le centre de conformité et de sécurité](permissions-in-the-security-and-compliance-center.md)

[Stratégies d’alerte dans le centre de sécurité & conformité](https://docs.microsoft.com/en-us/office365/securitycompliance/alert-policies)
