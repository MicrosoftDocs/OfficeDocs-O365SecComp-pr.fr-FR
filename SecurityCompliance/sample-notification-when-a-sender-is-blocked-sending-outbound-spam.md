---
title: Exemple de notification lorsqu'un expéditeur est bloqué en raison de l'envoi de courrier indésirable sortant
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/2/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: c33fd406-a4c8-4ac8-ad85-123996c5cded
description: "Lorsqu'un expéditeur est bloqué du service en raison de l'envoi de courrier indésirable sortant, l'administrateur de domaine spécifié dans Configurer la stratégie anti-courrier indésirable sortant reçoit un courrier électronique de notification semblable à celui-ci :"
ms.openlocfilehash: c9954d3ea16582a66185d574bcb5fc8a1aeebbf9
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027461"
---
# <a name="sample-notification-when-a-sender-is-blocked-sending-outbound-spam"></a>Exemple de notification lorsqu'un expéditeur est bloqué en raison de l'envoi de courrier indésirable sortant

Lorsqu'un expéditeur est bloqué du service en raison de l'envoi de courrier indésirable sortant, l'administrateur de domaine spécifié dans [Configurer la stratégie anti-courrier indésirable sortant](configure-the-outbound-spam-policy.md) reçoit un courrier électronique de notification semblable à celui-ci : 
  
 **Adresse de l'expéditeur :** spamalerts@microsoft.com 
  
 **Objet :** Notification de courrier indésirable sortant : \<  *nom du compte*  \> a été bloqué du service d'envoi de courriers électroniques sortants 
  
 **Corps :** Il s'agit d'une réponse automatique du système d'analyse du courrier indésirable d'Exchange Online Protection. 
  
Vous êtes contacté car nous avons détecté de grandes quantités de courriers électroniques marqués comme courriers indésirables, ou tout autre comportement suspect, en provenance de votre organisation. L'envoi de courriers électroniques a été désactivé pour les comptes de messagerie suivants (ils peuvent toujours recevoir des courriers électroniques) :
  
\< *nom du compte*  \> 
  
Il est probable que ce compte de messagerie ait été compromis. Suivez les étapes ci-après :
  
1. Essayez de résoudre ce problème de votre côté en :
    
  - modifiant le mot de passe du compte ;
    
  - déterminant comment le compte a été compromis ;
    
  - prenant des précautions pour vous assurer que cette vulnérabilité ne sera pas exploitée à nouveau ;
    
  - confirmant que tous les messages posant problème ont été supprimés de votre file d'attente des messages.
    
2. Contactez le support Microsoft via le canal de contact que vous avez l'habitude d'utiliser.
    
3. Expliquez qu'un utilisateur ne peut pas envoyer de courriers électroniques et que le problème a été traité.
    
4. L'agent crée un ticket de support avec les informations que vous fournissez et le transfère afin de débloquer l'adresse de messagerie ou le domaine.
    
5. Une fois que l'adresse a été débloquée et qu'aucun autre problème n'est en attente, vous serez contacté et averti du déblocage.
    
Merci de nous aider dans la lutte contre le courrier indésirable.
  
Exchange Online Protection.
  
\*\*REMARQUE : ne répondez pas à ce courrier électronique car il est envoyé à partir d'une adresse non contrôlée\*\*
  
> [!TIP]
> Vous pouvez également contacter le support technique via les options décrite à [l’aide et support pour EOP](eop/help-and-support-for-eop.md). 
  

