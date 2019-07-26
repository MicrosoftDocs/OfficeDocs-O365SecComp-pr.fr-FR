---
title: Suppression d’un utilisateur du portail Utilisateurs restreints après l’envoi d’un courrier indésirable
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 07/10/2019
audience: ITPro
ms.topic: article
f1_keywords:
- ms.exch.eac.ActionCenter.Restricted.Users.RestrictedUsers
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.assetid: 712cfcc1-31e8-4e51-8561-b64258a8f1e5
ms.collection:
- M365-security-compliance
description: 'Si un utilisateur envoie en continu des messages électroniques classés comme courriers indésirables depuis Office 365, ses envois seront bloqués. '
ms.openlocfilehash: 56f1a34fe4b47a722ff1dace73dd001f0c4812a2
ms.sourcegitcommit: 33c8e9c16143650ca443d73e91631f9180a9268e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35854718"
---
# <a name="removing-a-user-from-the-restricted-users-portal-after-sending-spam-email"></a>Suppression d’un utilisateur du portail Utilisateurs restreints après l’envoi d’un courrier indésirable

Si un utilisateur envoie continuellement des courriers électroniques qui sont classés comme courrier indésirable d’Office 365, il ne pourra pas envoyer de courriers électroniques, mais pourra toujours en recevoir. L’utilisateur est répertorié dans le service comme expéditeur sortant incorrect et reçoit une notification d’échec de remise (NDR) qui indique :

> «Votre message n’a pas pu être remis parce que vous n’avez pas été reconnu comme expéditeur valide. Le plus souvent, il est possible que votre adresse de messagerie soit susceptible d’envoyer du courrier indésirable et qu’elle ne soit plus autorisée à envoyer du courrier électronique.  Contactez votre administrateur pour obtenir de l’aide. Le serveur distant a renvoyé' 550 5.1.8 accès refusé, expéditeur sortant incorrect».

## <a name="what-do-you-need-to-know-before-you-begin"></a>Ce qu'il faut savoir avant de commencer
<a name="sectionSection0"> </a>

Durée d’exécution estimée : 5 minutes
  
Des autorisations doivent vous être attribuées avant de pouvoir exécuter cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez l'entrée « Anti-spam » dans la rubrique [Autorisations des fonctionnalités dans Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx).

La procédure suivante peut également être exécutée via le service PowerShell à distance. Utilisez l’applet de commande Get-BlockedSenderAddress pour obtenir la liste des utilisateurs avec accès restreint et Remove-BlockedSenderAddress pour supprimer la restriction. Pour apprendre à utiliser Windows PowerShell afin de vous connecter à Exchange Online, consultez la rubrique [Connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).

## <a name="remove-restrictions-for-a-blocked-office-365-email-account"></a>Supprimer les restrictions pour un compte de courrier Office 365 bloqué

Vous devez effectuer cette tâche dans le centre de sécurité & conformité (SCC). Pour plus d’informations sur SCC,[accédez au centre de sécurité & conformité](go-to-the-securitycompliance-center.md). Vous devez être dans le groupe de rôles **Gestion de l’organisation** ou **administrateur de la sécurité** pour effectuer ces fonctions. Pour plus d’informations sur les groupes de rôles SCC,[accédez au centre de sécurité & conformité](permissions-in-the-security-and-compliance-center.md).

1. À l’aide d’un compte professionnel ou scolaire disposant de privilèges d’administrateur général Office 365, connectez-vous au centre de sécurité et conformité Office 365, puis dans la liste à gauche, développez **Gestion des menaces**, choisir** révision**, puis sélectionnez **utilisateurs avec accès restreint**.
    
    > [!TIP]
    > Pour accéder directement à la page **utilisateurs avec accès restreint** (autrefois appelée Centre d’actions) dans le centre de conformité&amp; et de sécurité, utilisez l’URL suivante: > [https://protection.office.com/#/restrictedusers](https://protection.office.com/?hash=/restrictedusers)

2. Cette page contient la liste des utilisateurs qui ont été bloqués pour l’envoi de messages électroniques.  Recherchez l’utilisateur dont vous voulez supprimer les restrictions, puis sélectionnez **débloquer**.

3. Une fenêtre permet d’accéder aux informations relatives au compte dont l’envoi est restreint. Nous vous conseillons de suivre les recommandations afin de vous assurer que vous effectuez les actions appropriées au cas où le compte serait réellement compromis. Sélectionnez **Suivant** lorsque vous avez terminé.

4. L’écran suivant comporte des recommandations pour empêcher toute compromission ultérieure. L’activation de l’authentification multifacteur (MFA) et la modification des mots de passe constituent une bonne défense. Lorsque vous avez terminé, cliquez sur **débloquer l’utilisateur**.

5. Cliquez sur **Oui** pour confirmer la modification.

    > [!NOTE]
    > L’opération peut prendre jusqu’à 30 minutes avant la suppression des restrictions. 

## <a name="making-sure-admins-are-alerted-when-this-happens"></a>Vérifier que les administrateurs sont avertis lorsque cela se produit

Une alerte «utilisateur restreint à l’envoi de courrier électronique» est disponible sous la forme d’une stratégie sous la page de stratégies d’alertes de conformité & sécurité d’Office 365. Il s’agissait autrefois de la stratégie anti-courrier indésirable sortant, qui est désormais native pour la plateforme d’alertes Office 365. Pour plus d’informations sur les alertes, accédez à[stratégies d’alertes dans le centre de sécurité & conformité](alert-policies.md).

> [!IMPORTANT]
> Pour que les alertes fonctionnent, la recherche dans le journal d’audit doit être activée. Pour plus d'informations, voir [Activer ou désactiver la recherche dans le journal d’audit Office 365](turn-audit-log-search-on-or-off.md).

La stratégie pour cette alerte est une stratégie par défaut et est fournie avec tous les clients Office 365 et n’a pas besoin d’être configurée. C’est une alerte de gravité élevée et sera envoyée par courrier électronique au groupe TenantAdmins configuré lorsque l’alerte est déclenchée chaque fois qu’un utilisateur a été empêché d’envoyer des messages. Les administrateurs peuvent mettre à jour le groupe averti lorsque cette alerte se produit en accédant à l’alerte sous le portail SCC > Alertes > les stratégies d’alerte > utilisateurs qui ne sont pas autorisés à envoyer des messages électroniques.

Vous pourrez modifier l’alerte en effectuant les actions suivantes :
- Activer/désactiver les notifications par courrier électronique
- Envoyer un courrier électronique aux destinataires requis
- Limiter les notifications que vous obtenez par jour

## <a name="checking-for-and-removing-restrictions-using-powershell"></a>Vérification et suppression des restrictions à l’aide de PowerShell
Les commandes PowerShell pour les utilisateurs avec accès restreint sont les suivantes :
- `Get-BlockedSenderAddress`: Exécuter pour récupérer la liste des utilisateurs qui ne sont pas autorisés à envoyer des messages électroniques
- `Remove-BlockedSenderAddress`: Exécuter pour supprimer des utilisateurs d’un accès restreint

## <a name="for-more-information"></a>Pour plus d'informations

[Réponse à un compte de messagerie compromis](responding-to-a-compromised-email-account.md)


  [Présentation de l’alerte l’utilisateur n’est pas autorisé à envoyer des messages](https://docs.microsoft.com/fr-FR/office365/securitycompliance/alert-policies)

[Pool de remise à haut risque pour les messages sortants](high-risk-delivery-pool-for-outbound-messages.md)

[Autorisations dans le centre de conformité et de sécurité](permissions-in-the-security-and-compliance-center.md)


  [Stratégies d’alerte dans le Centre de sécurité et de conformité](https://docs.microsoft.com/fr-FR/office365/securitycompliance/alert-policies)
