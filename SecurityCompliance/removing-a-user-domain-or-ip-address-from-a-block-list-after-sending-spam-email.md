---
title: Suppression d’un utilisateur, d’un domaine ou d’une adresse IP d’une liste rouge après l’envoi de courrier indésirable
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 09/05/2018
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
ms.openlocfilehash: 3f3130bec3cde4cdc1343a0140a9013deacfc519
ms.sourcegitcommit: d85fc77cba3a17d5ddf215e2f506f61b499e0cda
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "23839108"
---
# <a name="removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email"></a>Suppression d’un utilisateur, d’un domaine ou d’une adresse IP d’une liste rouge après l’envoi de courrier indésirable

Si un utilisateur envoie en continu des messages électroniques classés comme courriers indésirables depuis Office 365, ses envois seront bloqués.  
  

Lorsque les messages électroniques d’un expéditeur sont bloqués, ce dernier une notification d’échec de remise (impossible d’envoyer le message) qui fournit des informations spécifiques sur les étapes à suivre pour débloquer les messages.
  
Non seulement des utilisateurs individuels peuvent être bloquées par les domaines de service, mais les sites Web spécifiques, et adresses IP peuvent aussi être bloquées. Dans certains cas, des domaines ou des sites Web peuvent être ajoutés à une liste d’adresses bloquées seulement car ils apparaissent dans un message de courrier indésirable. En tant que l’administrateur Office 365, vous pouvez essayer d’obtenir des utilisateurs, sites Web, des domaines et supprimées à partir de listes d’interdiction tiers des adresses IP. Utilisez les liens de la table en bas de cette rubrique pour contacter chaque tiers, puis suivez les instructions. Si une personne extérieure à Office 365 ne peuvent pas envoyer des messages à votre compte Office 365, leur compte peut se trouver sur la liste des expéditeurs bloqués externe. Les utilisateurs en dehors d’Office 365 peuvent tenter de se supprimer de la liste des expéditeurs bloqués à l’aide du [portail libre-service de retrait de la liste](https://technet.microsoft.com/library/mt661881%28v=exchg.150%29.aspx).
  
Vous pouvez configurer des paramètres de courrier indésirable sortant afin de recevoir une notification lorsque les messages d’un utilisateur Office 365 sont classés comme courrier indésirable. Une fois que le problème lié à la boîte aux lettres de l’utilisateur est résolu, vous pouvez le retirer de la liste rouge.
  
## <a name="unblock-a-blocked-office-365-email-account"></a>Retirer un compte de messagerie Office 365 de la liste rouge

Vous effectuez cette tâche dans la sécurité pour Microsoft Office 365 & centre de conformité (SCC). Pour plus d’informations sur le contrôle de code source, [accédez au portail Office 365 sécurité & centre de conformité](go-to-the-securitycompliance-center.md) .

1. À l’aide d’un compte disposant de privilèges d’administrateur général Office 365, vous connecter dans le centre de conformité et de sécurité pour Microsoft Office 365 et dans la liste de gauche, développez **Threat Management**, sélectionnez **passer en revue les**, puis **Restricted Professionnel ou de l’école Les utilisateurs**.
    
    > [!TIP]
    > Pour accéder directement à la page **Utilisateurs restreints** dans la sécurité &amp; centre de conformité, utilisez l’URL suivante : >[https://protection.office.com/?hash=/restrictedusers](https://protection.office.com/?hash=/restrictedusers)

2. Cette page contient la liste des utilisateurs qui ont été bloqués à partir de l’envoi de courrier à l’extérieur de votre organisation.  Recherchez les utilisateurs que vous souhaitez supprimer les restrictions, puis cliquez sur **Débloquer**.

3. Cliquez sur **Oui** pour confirmer la modification. 
    
> [!NOTE]
> Il existe une limite au nombre de fois qu’un compte peut être non bloquée par l’administrateur du client. Si la limite d’un utilisateur a été dépassée, un message d’erreur s’affiche. Vous devrez contacter le Support pour débloquer l’utilisateur. 
  
## <a name="third-party-block-lists"></a>Listes rouges tierces

|**Nom de la liste**|**Portail de retrait de la liste**|**Pour plus d'informations**|
|:-----|:-----|:-----|
|URIBL  <br/> |[https://admin.uribl.com/?section=lookup](https://admin.uribl.com/?section=lookup) <br/> |[Site Web URIBL](https://uribl.com/) <br/> |
|SURBL  <br/> |[http://www.surbl.org/surbl-analysis](http://www.surbl.org/surbl-analysis) <br/> |[Présentation de données de réputation d’URI SURBL](http://www.surbl.org/) <br/> |
|Spamhaus   <br/> |[https://www.spamhaus.org/lookup/](https://www.spamhaus.org/lookup/) <br/> |[Présentation du filtrage DNSBL](https://www.spamhaus.org/whitepapers/dnsbl_function/) <br/> |
|invaluement  <br/> |[http://dnsbl.invaluement.com/lookup/](http://dnsbl.invaluement.com/lookup/) <br/> |[liste de blocage du courrier indésirable de liste](http://dnsbl.invaluement.com/) <br/> |
|Phishtank  <br/> |[https://www.phishtank.com/](https://www.phishtank.com/) <br/> |[PhishTank Forum aux questions](https://www.phishtank.com/faq.php) <br/> |
   
> [!NOTE]
> Exchange Online Protection utilise également des listes rouges tiers pour le filtrage du courrier indésirable. 
   
## <a name="for-more-information"></a>Pour plus d'informations

[Configurer la stratégie anti-courrier indésirable sortant](configure-the-outbound-spam-policy.md)
  
[Pool de remise à risque élevé pour les messages sortants](high-risk-delivery-pool-for-outbound-messages.md)

[Utilisation du portail Supprimer de la liste pour vous supprimer de la liste des expéditeurs bloqués Office 365](use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis.md)
  

  

