---
title: Utilisation du portail Supprimer de la liste pour vous supprimer de la liste des expéditeurs bloqués Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/18/2016
ms.audience: ITPro
ms.topic: troubleshooting
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 0bcecdd4-3343-4cc0-9e58-e19d4de515e8
description: Obtenez-vous un message d'erreur lorsque vous tentez d'envoyer un courrier électronique à un destinataire dont l'adresse de messagerie est dans Office 365 ? Si vous pensez que vous ne devriez pas recevoir de message d'erreur, vous pouvez utiliser le portail Supprimer de la liste pour vous supprimer de la liste des expéditeurs bloqués Office 365.
ms.openlocfilehash: 127b305cdb27cffadc7ad6a43a5d2db2440365ca
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026231"
---
# <a name="use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-list"></a>Utilisation du portail Supprimer de la liste pour vous supprimer de la liste des expéditeurs bloqués Office 365

Obtenez-vous un message d'erreur lorsque vous tentez d'envoyer un courrier électronique à un destinataire dont l'adresse de messagerie est dans Office 365 ? Si vous pensez que vous ne devriez pas recevoir de message d'erreur, vous pouvez utiliser le portail Supprimer de la liste pour vous supprimer de la liste des expéditeurs bloqués Office 365.
  
## <a name="what-is-the-office-365-blocked-senders-list"></a>Qu'est-ce que la liste des expéditeurs bloqués Office 365 ?

Microsoft utilise la liste des expéditeurs bloqués pour protéger ses clients contre le courrier indésirable, l'usurpation d'identité et les attaques par hameçonnage. L'adresse IP de votre serveur messagerie, c'est-à-dire l'adresse que votre serveur de messagerie utilise pour s'identifier sur Internet, a été identifiée comme une menace potentielle envers Office 365 pour une raison quelconque. Quand Office 365 ajoute l'adresse IP à la liste, cela empêche toute autre communication entre l'adresse IP et l'un de nos clients par le biais de nos centres de données.
  
Vous savez que vous avez été ajouté à la liste si vous recevez une réponse à un courrier électronique incluant une erreur ressemblant à ce qui suit :
  
550 5.7.606-649 accès refusé, interdit l’envoi IP [ _adresse IP_] ; Pour demander la suppression de cette liste, consultez https://sender.office.com/ et suivez les instructions affichées. Pour plus d’informations, voir [les rapports de non-remise messagerie dans Office 365](http://go.microsoft.com/fwlink/?LinkID=526653).
  
où  _IP address_ est l'adresse IP de l'ordinateur sur lequel s'exécute le serveur de messagerie. 
  
### <a name="to-use-the-office-365-delist-portal-to-remove-yourself-from-the-blocked-senders-list"></a>Utilisation du portail Supprimer de la liste Office 365 pour vous supprimer de la liste des expéditeurs bloqués

1. Dans un navigateur web, accédez à [https://sender.office.com](https://sender.office.com).
    
2. Suivez les instructions de la page. Assurez-vous que vous utilisez l'adresse de messagerie à laquelle le message d'erreur a été envoyé et l'adresse IP qui est spécifiée dans le message d'erreur. Vous ne pouvez entrer qu'une adresse de messagerie et une adresse IP par visite.
    
3. Cliquez sur **Envoyer**.
    
    Le portail envoie un courrier électronique à l’adresse de messagerie que vous fournissez. Le courrier électronique doit ressembler à ce qui suit : ![capture d’écran de courrier électronique reçu lorsque vous soumettez une demande via le portail delist](media/bf13e4f7-f68c-4e46-baa7-b6ab4cfc13f3.png)
  
4. Cliquez sur le lien de confirmation dans le courrier électronique envoyé par le portail de suppression de la liste.
    
    Vous revenez au portail Supprimer de la liste.
    
5. Dans le portail Supprimer de la liste, cliquez sur **Supprimer l'adresse IP de la liste**.
    
    Une fois que l'adresse IP est supprimée de la liste des expéditeurs bloqués, les messages électroniques provenant de cette adresse IP seront remis aux destinataires utilisant Office 365. Par conséquent, assurez-vous que les messages envoyés à partir de cette adresse IP ne sont pas abusifs ou malveillants. Dans le cas contraire, il est possible que l'adresse IP soit bloquée à nouveau.
    

