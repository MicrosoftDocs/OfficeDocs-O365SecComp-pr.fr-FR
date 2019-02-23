---
title: Suspendre ou restaurer un compte d’utilisateur dans la sécurité des applications cloud Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 12/03/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 5f02d20f-b9aa-4b2f-ad2d-506a4a3c4540
description: "Avec la sécurité des applications Cloud d'Office 365, les actions de gouvernance que vous pouvez effectuer sont la suspension ou l'annulation de l'interruption d'un compte d'utilisateur. "
ms.openlocfilehash: 3650a5304af0440dc537610994c4bd827f599989
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215094"
---
# <a name="suspend-or-restore-a-user-account-in-office-365-cloud-app-security"></a>Suspendre ou restaurer un compte d’utilisateur dans la sécurité des applications cloud Office 365

|Évaluation * *\>**|Planification * *\>**|Déploiement * *\>**|Utilisation * * * *|
|:-----|:-----|:-----|:-----|
|[Commencer l'évaluation](office-365-cas-overview.md) <br/> |[Commencer la planification](get-ready-for-office-365-cas.md) <br/> |[Démarrer le déploiement](turn-on-office-365-cas.md) <br/> |Vous êtes là!  <br/> [Étapes suivantes](suspend-or-restore-an-account-in-ocas.md#nextsteps) <br/> |
   
Supposons que vous recevez une alerte indiquant qu'un des comptes d'utilisateur de votre organisation pour Office 365 a été compromis. Supposons que vous ayez reçu une alerte indiquant un problème lié à un compte d'utilisateur. Avec la sécurité des applications Cloud d'Office 365, vous pouvez suspendre un compte d'utilisateur et le restaurer ultérieurement après avoir étudié les alertes que vous recevez.
  
> [!NOTE]
> Office 365 Cloud App Security est disponible dans Office 365 entreprise E5. Si votre organisation utilise un autre abonnement entreprise 365 Enterprise, Office 365 Cloud App Security peut être acheté en tant que module complémentaire. (en tant qu'administrateur général, dans le centre d'administration Office 365, sélectionnez **facturation** \> : **ajouter**des abonnements.) Pour plus d'informations, reportez-vous à [la rubrique office &amp; 365 Platform Service Description: Office 365 Security Compliance Center](https://technet.microsoft.com/en-us/library/dn933793.aspx) et [acheter ou modifier un composant additionnel pour Office 365 pour les entreprises](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6). 
  
## <a name="to-suspend-a-user-account-in-office-365-cloud-app-security"></a>Pour suspendre un compte d'utilisateur dans Office 365 Cloud App Security

Lorsque vous suspendez un compte d'utilisateur, vous empêchez l'utilisateur de se reconnecter. Il s'agit de la modification du compte d'utilisateur directement dans Office 365 pour définir l'état de connexion **bloqué**.
  
> [!NOTE]
> Si vous empêchez un utilisateur de se connecter à Office 365, soit en le suspendant, soit en modifiant son statut de connexion, sachez qu'il peut prendre une heure ou pour prendre effet sur tous les appareils et clients de l'utilisateur ([modifier ou modifier un utilisateur dans Office 365](https://support.office.com/article/42BB3F17-8F9D-4182-B434-5F1C8024E614#SingleUserPreview)). Si l'utilisateur est connecté à Office 365, le blocage prend effet dès qu'Office 365 le demande de se reconnecter. 
  
1. En tant qu' [administrateur général ou administrateur de sécurité](permissions-in-the-security-and-compliance-center.md), [https://protection.office.com](https://protection.office.com) accédez à et connectez-vous à l'aide de votre compte professionnel ou scolaire. (Vous accédez au centre de sécurité &amp; conformité.) 
    
2. Dans le centre &amp; de sécurité conformité, sélectionnez **alertes** \> **gérer les alertes avancées**.
    
3. Sélectionnez **accéder à la sécurité des applications Cloud Office 365**.<br>![Dans le centre &amp; de sécurité conformité, choisissez gérer les alertes avancées pour accéder à la sécurité des applications Cloud Office 365](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)<br>
  
4. Dans la barre de navigation en haut de l'écran, sélectionnez **alertes**.
    
5. Dans la colonne **alerte** , double-cliquez sur une alerte qui se rapporte à un compte d'utilisateur spécifique. 
    
6. Sous **comptes**, dans la colonne **État** , sélectionnez icône ![](media/e01b75cc-b28f-4b83-8f86-b1b13dc27ab2.png) \> paramètres des paramètres de l' **utilisateur**.
    
## <a name="to-restore-a-user-account"></a>Pour restaurer un compte d'utilisateur

Voir [restaurer un utilisateur dans Office 365](https://support.office.com/article/2c261e42-5dd1-48b0-845f-2a016d29cfc1)
  
## <a name="next-steps"></a>Étapes suivantes

- [Passer en revue et effectuer une action sur les alertes dans la sécurité des applications cloud Office 365](review-office-365-cas-alerts.md)
    
- [Gérer les applications OAuth à l’aide de la sécurité des applications cloud Office 365](manage-app-permissions-in-ocas.md)
    
- Examiner vos [activités d'utilisation pour Office 365 Cloud App Security](utilization-activities-for-ocas.md)
    

