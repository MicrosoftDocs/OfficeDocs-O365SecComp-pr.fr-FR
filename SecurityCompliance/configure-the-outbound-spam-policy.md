---
title: Configurer la stratégie anti-courrier indésirable sortant
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 11/10/2016
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: a44764e9-a5d2-4c67-8888-e7fb871c17c7
ms.collection:
- M365-security-compliance
description: Le filtrage du courrier indésirable sortant est toujours activé si vous utilisez le service pour l’envoi de messages sortants, ce qui permet de protéger les organisations utilisant le service ainsi que leurs destinataires.
ms.openlocfilehash: 2bf2f8c7292bee4d1e89249bcec5c74a4b5d38c9
ms.sourcegitcommit: bc25ea19c0b6d318751eadc4f27902b0054d5e2b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/01/2019
ms.locfileid: "36054652"
---
# <a name="configure-the-outbound-spam-policy"></a>Configurer la stratégie anti-courrier indésirable sortant

Le filtrage du courrier indésirable sortant est toujours activé si vous utilisez le service pour l'envoi de messages sortants, ce qui permet de protéger les organisations utilisant le service ainsi que leurs destinataires. Comme pour le filtrage entrant, le filtrage de courrier indésirable sortant comprend le filtrage de connexion et le filtrage de contenu. Toutefois, les paramètres de filtrage sortant ne peuvent pas être configurés. Si un message sortant est déterminé comme étant du courrier indésirable, il est routé via le pool de remise à risque plus élevé, ce qui réduit la probabilité d'ajout du pool d'IP sortantes normales à une liste rouge. Si un client continue à envoyer du courrier indésirable sortant au service, ses messages sont bloqués. Bien que le filtrage de courrier indésirable sortant ne puisse pas être désactivé ou modifié, vous pouvez configurer plusieurs paramètres de courrier indésirable à l'échelle de l'entreprise via la stratégie de courrier indésirable sortant par défaut. 
  
La vidéo suivante illustre la configuration de la stratégie de courrier indésirable sortant :
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/1f20d655-0d3d-4141-9cae-e57f5a6cffe8?autoplay=false]
  
> [!NOTE]
> Pour obtenir les meilleurs résultats de filtrage, le contenu de la vidéo ci-dessus doit être utilisé avec une configuration correcte et une connaissance des [contrôles de courrier indésirable sortants dans Office 365](https://docs.microsoft.com/office365/securitycompliance/outbound-spam-controls).

## <a name="what-do-you-need-to-know-before-you-begin"></a>Ce qu’il faut savoir avant de commencer
<a name="sectionSection0"> </a>

Durée d'exécution estimée : 5 minutes
  
Des autorisations doivent vous être attribuées avant de pouvoir exécuter cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez la rubrique «entrée anti-courrier indésirable dans la rubrique [autorisations des fonctionnalités dans Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) . 
  
Pour des informations sur les raccourcis clavier applicables aux procédures de cette rubrique, voir Raccourcis clavier dans Exchange 2013 **Keyboard shortcuts in Exchange 2013**.
  
La procédure suivante peut également être exécutée par le biais du service PowerShell à distance. Utilisez la cmdlet [Get-HostedOutboundSpamFilterPolicy](http://technet.microsoft.com/library/8f15c83c-c10a-4d9d-b135-35321430bdc2.aspx) pour vérifier vos paramètres et la cmdlet [Set-HostedOutboundSpamFilterPolicy](http://technet.microsoft.com/library/665d1b04-d4b5-4a0e-811a-4e37096ccbfd.aspx) pour modifier les paramètres de votre stratégie anti-courrier indésirable sortant. Pour apprendre à utiliser Windows PowerShell afin de vous connecter à Exchange Online Protection, consultez la rubrique [Connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627290). Pour apprendre à utiliser Windows PowerShell afin de vous connecter à Exchange Online, consultez la rubrique [Connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).
  
## <a name="use-the-eac-to-edit-the-default-outbound-spam-policy"></a>Utiliser le Centre d'administration Exchange (CAE) pour modifier la stratégie de courrier indésirable sortant par défaut
<a name="sectionSection1"> </a>

La procédure suivante vous permet de modifier la stratégie de courrier indésirable sortant par défaut :
  
### <a name="to-configure-the-default-outbound-spam-policy"></a>Pour configurer la stratégie de courrier indésirable sortant par défaut

1. Dans le CAE, accédez à **Protection**\> **Courrier indésirable sortant**, puis double-cliquez sur la stratégie par défaut.
    
2. Sélectionnez l'option de menu **Préférences de courrier indésirable sortant**. 
    
3. Cochez les cases suivantes relatives aux messages sortants, puis spécifiez une ou plusieurs adresses de messagerie associées dans la zone de texte connexe (il peut s'agir de listes de distribution si elles se résolvent en tant que destinations SMTP valides) :
    
1. **Envoyer une copie de tous les messages électroniques sortants suspects à l'adresse ou aux adresses de messagerie suivantes**. Il s'agit de messages marqués comme étant courriers indésirables par le filtre (quelle que soit la valeur SCL). Le filtre ne les rejette pas, mais ils sont routés via le pool de remise à risque plus élevé. S'il y a plusieurs adresses, utilisez un point-virgule pour les séparer. Notez que les destinataires spécifiés recevront les messages en tant qu'adresse Cci (les champs De et À correspondent à l'expéditeur et au destinataire initiaux).
    
2. **Envoyer une notification à l'adresse de messagerie suivante quand un utilisateur est bloqué en relation avec l'envoi de courrier indésirable sortant**. S'il y a plusieurs adresses, utilisez un point-virgule pour les séparer.
    
    Quand une quantité importante de courriers indésirables provenant d'un utilisateur en particulier est détectée, cet utilisateur est désactivé et ne peut plus envoyer de messages électroniques. L'administrateur du domaine, spécifié à l'aide de ce paramètre, est informé que l'envoi de messages sortants est bloqué pour cet utilisateur. Pour savoir à quoi ressemble cette notification, voir [Exemple de notification lorsqu'un expéditeur est bloqué en raison de l'envoi de courrier indésirable sortant](sample-notification-when-a-sender-is-blocked-sending-outbound-spam.md). Pour plus d'informations sur le mode de réactivaction, consultez la rubrique [Removing a user, domain, or IP address from a block list after sending spam email](http://technet.microsoft.com/library/712cfcc1-31e8-4e51-8561-b64258a8f1e5.aspx).
    
4. Cliquez sur **Enregistrer**. Un résumé de vos paramètres de stratégie par défaut s'affiche dans le volet droit.
    
## <a name="for-more-information"></a>Pour plus d'informations
<a name="sectionSection2"> </a>

[Pool de remise à risque élevé pour les messages sortants](high-risk-delivery-pool-for-outbound-messages.md)
  
[FAQ sur la protection contre le courrier indésirable](anti-spam-protection-faq.md)
  

