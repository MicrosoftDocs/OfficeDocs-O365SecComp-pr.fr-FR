---
title: Utilisation du portail Supprimer de la liste pour vous supprimer de la liste des expéditeurs bloqués Office 365
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 04/18/2016
audience: ITPro
ms.topic: troubleshooting
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 0bcecdd4-3343-4cc0-9e58-e19d4de515e8
ms.collection:
- M365-security-compliance
description: Obtenez-vous un message d'erreur lorsque vous tentez d'envoyer un courrier électronique à un destinataire dont l'adresse de messagerie est dans Office 365 ? Si vous pensez que vous ne devriez pas recevoir de message d'erreur, vous pouvez utiliser le portail Supprimer de la liste pour vous supprimer de la liste des expéditeurs bloqués Office 365.
ms.openlocfilehash: 18ec4956b8d37308e7ec35c8fc28f24d36cd2763
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35598430"
---
# <a name="use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-list"></a>Utilisation du portail Supprimer de la liste pour vous supprimer de la liste des expéditeurs bloqués Office 365

Obtenez-vous un message d'erreur lorsque vous tentez d'envoyer un courrier électronique à un destinataire dont l'adresse de messagerie est dans Office 365 ? Si vous pensez que vous ne devriez pas recevoir de message d'erreur, vous pouvez utiliser le portail Supprimer de la liste pour vous supprimer de la liste des expéditeurs bloqués Office 365.
  
## <a name="what-is-the-office-365-blocked-senders-list"></a>Qu’est-ce que la liste des expéditeurs bloqués Office 365 ?

Microsoft utilise la liste des expéditeurs bloqués pour protéger ses clients contre le courrier indésirable, l'usurpation d'identité et les attaques par hameçonnage. L'adresse IP de votre serveur messagerie, c'est-à-dire l'adresse que votre serveur de messagerie utilise pour s'identifier sur Internet, a été identifiée comme une menace potentielle envers Office 365 pour une raison quelconque. Quand Office 365 ajoute l'adresse IP à la liste, cela empêche toute autre communication entre l'adresse IP et l'un de nos clients par le biais de nos centres de données.
  
Vous savez que vous avez été ajouté à la liste si vous recevez une réponse à un courrier électronique incluant une erreur ressemblant à ce qui suit :
  
> 550 5.7.606-649 accès refusé, IP d’envoi interdit [_adresse IP_]; Pour demander la suppression de cette liste, https://sender.office.com/ visitez le site et suivez les instructions. Pour plus d’informations, consultez la rubrique notifications de [non-remise aux courriers électroniques dans Office 365](http://go.microsoft.com/fwlink/?LinkID=526653).
  
où  _IP address_ est l'adresse IP de l'ordinateur sur lequel s'exécute le serveur de messagerie. 
  
### <a name="to-use-the-office-365-delist-portal-to-remove-yourself-from-the-blocked-senders-list"></a>Utilisation du portail Supprimer de la liste Office 365 pour vous supprimer de la liste des expéditeurs bloqués

1. Dans un navigateur web, accédez à [https://sender.office.com](https://sender.office.com).
    
2. Suivez les instructions de la page. Assurez-vous que vous utilisez l'adresse de messagerie à laquelle le message d'erreur a été envoyé et l'adresse IP qui est spécifiée dans le message d'erreur. Vous ne pouvez entrer qu'une adresse de messagerie et une adresse IP par visite.
    
3. Cliquez sur **Envoyer**.
    
    Le portail envoie un courrier électronique à l'adresse de messagerie que vous indiquez. Le message électronique se présente comme suit: ![capture d’écran du courrier électronique reçu lorsque vous envoyez une demande via le portail supprimer de la liste](media/bf13e4f7-f68c-4e46-baa7-b6ab4cfc13f3.png)
  
4. Cliquez sur le lien de confirmation dans le courrier électronique envoyé par le portail de suppression de la liste.
    
    Vous revenez au portail Supprimer de la liste.
    
5. Dans le portail Supprimer de la liste, cliquez sur **Supprimer l'adresse IP de la liste**.
    
    Une fois que l'adresse IP est supprimée de la liste des expéditeurs bloqués, les messages électroniques provenant de cette adresse IP seront remis aux destinataires utilisant Office 365. Par conséquent, assurez-vous que les messages envoyés à partir de cette adresse IP ne sont pas abusifs ou malveillants. Dans le cas contraire, il est possible que l'adresse IP soit bloquée à nouveau.
    
    > [!NOTE]
    > Cette opération peut prendre jusqu’à 24 heures ou les résultats peuvent varier considérablement avant la suppression des restrictions.
    
Découvrez [Comment empêcher le courrier électronique réel d’être marqué comme courrier indésirable dans office 365](prevent-email-from-being-marked-as-spam.md ) et de [contrôler le courrier indésirable sortant dans Office 365](outbound-spam-controls.md) afin d’empêcher IP d’être en liste de blocage.
