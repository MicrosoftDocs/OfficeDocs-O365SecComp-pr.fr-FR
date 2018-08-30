---
title: Suspendre ou restaurer un compte d’utilisateur dans Office 365 Cloud Application Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/26/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 5f02d20f-b9aa-4b2f-ad2d-506a4a3c4540
description: 'Avec Office 365 de sécurité application Cloud, les gouvernance actions possibles sont de suspendre ou reprendre un compte d’utilisateur. '
ms.openlocfilehash: a5c75edefc6ddb87b5676c4253aafe04817f6a1d
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527695"
---
# <a name="suspend-or-restore-a-user-account-in-office-365-cloud-app-security"></a>Suspendre ou restaurer un compte d’utilisateur dans Office 365 Cloud Application Security

Gestion de la sécurité Office 365 avancée est désormais sécurité d’application Office 365 dans le nuage.
  
|Évaluation **\>**|Planification **\>**|Déploiement **\>**|Utilisation du ***|
|:-----|:-----|:-----|:-----|
|[Commencer à évaluer](office-365-cas-overview.md) <br/> |[Commencer à planifier](get-ready-for-office-365-cas.md) <br/> |[Commencer à déployer](turn-on-office-365-cas.md) <br/> |Vous êtes ici !  <br/> [Étapes suivantes](suspend-or-restore-an-account-in-ocas.md#nextsteps) <br/> |
   
Supposons que vous recevez une alerte qu’un des comptes d’utilisateurs de votre organisation pour Office 365 a été compromis. Ou bien, supposez que vous avez reçu une alerte indiquant un que problème avec un compte d’utilisateur. Avec Office 365 de sécurité App dans le nuage, vous pouvez suspendre un compte d’utilisateur et restaurer ultérieurement une fois que vous avez examiné les alertes que vous recevez.
  
> [!NOTE]
> Sécurité d’application Office 365 dans le nuage est disponible dans Office 365 entreprise E5. Si votre organisation utilise un autre abonnement Office 365 pour entreprises, Office 365 Cloud application sécurité peut être achetée comme module complémentaire. (En tant qu’administrateur global, dans le centre d’administration Office 365, choisissez **facturation** \> **abonnements Add**.) Pour plus d’informations, voir [Office 365 Platform Service Description : Office 365 sécurité &amp; centre de conformité](https://technet.microsoft.com/en-us/library/dn933793.aspx) et [acheter ou modifier un module complémentaire pour Office 365 pour entreprises](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6). 
  
## <a name="to-suspend-a-user-account-in-office-365-cloud-app-security"></a>Pour suspendre un compte d’utilisateur dans Office 365 Cloud Application Security

Lorsque vous interrompez un compte d’utilisateur, vous empêchez l’utilisateur de se connecter à nouveau. Il est identique à la modification directement dans Office 365 pour définir le statut de connexion pour la **connexion bloqué**le compte d’utilisateur.
  
> [!NOTE]
> Si vous bloquez un utilisateur de se connecter à Office 365, en leur suspension ou en modifiant son statut de connexion, sachez que peut prendre une heure ou afin de prendre effet sur tous les clients ([Modifier un utilisateur dans Office 365](https://support.office.com/article/42BB3F17-8F9D-4182-B434-5F1C8024E614#SingleUserPreview)) et les périphériques de l’utilisateur. Si l’utilisateur est connecté à Office 365, le bloc prendra effet chaque fois qu’Office 365 tenus de se reconnecter. 
  
1. En tant qu’un [administrateur global ou administrateur de sécurité](permissions-in-the-security-and-compliance-center.md), accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous à l’aide de votre compte professionnel ou de l’école. (Cela vous amène à la sécurité &amp; centre de conformité.) 
    
2. Dans la sécurité &amp; centre de conformité, sélectionnez **alertes** \> **Gestion avancée des alertes**.
    
3. Cliquez sur **Aller à la sécurité d’application Office 365 dans le nuage**.
    
    ![Dans la sécurité &amp; centre de conformité, cliquez sur Gérer les alertes avancées pour accéder à la sécurité d’application dans le nuage Office 365](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)
  
4. Dans la barre de navigation dans la partie supérieure de l’écran, cliquez sur **alertes**.
    
5. Dans la colonne **alerte** , double-cliquez sur une alerte qui se rapporte à un compte d’utilisateur spécifique. 
    
6. Sous **comptes**, dans la colonne **état** , choisissez paramètres ![icône paramètres](media/e01b75cc-b28f-4b83-8f86-b1b13dc27ab2.png) \> **utilisateur Suspend**.
    
## <a name="to-restore-a-user-account"></a>Pour restaurer un compte d’utilisateur

Reportez-vous à la section [restaurer un utilisateur dans Office 365](https://support.office.com/article/2c261e42-5dd1-48b0-845f-2a016d29cfc1)
  
## <a name="next-steps"></a>Étapes suivantes

- [Passez en revue et effectuer une action sur les alertes de sécurité pour application Cloud Microsoft Office 365](review-office-365-cas-alerts.md)
    
- [Gérer les autorisations d’application à l’aide de la sécurité d’application Office 365 dans le nuage](manage-app-permissions-in-ocas.md)
    
- Passez en revue vos [activités utilisation Office 365 nuage sécurité des applications](utilization-activities-for-ocas.md)
    

