---
title: Utilisation du portail Supprimer de la liste pour vous supprimer de la liste des expéditeurs bloqués Office 365
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 4/18/2016
ms.audience: ITPro
ms.topic: troubleshooting
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 0bcecdd4-3343-4cc0-9e58-e19d4de515e8
ms.collection:
- M365-security-compliance
description: Obtenez-vous un message d'erreur lorsque vous tentez d'envoyer un courrier électronique à un destinataire dont l'adresse de messagerie est dans Office 365 ? Si vous pensez que vous ne devriez pas recevoir de message d'erreur, vous pouvez utiliser le portail Supprimer de la liste pour vous supprimer de la liste des expéditeurs bloqués Office 365.
ms.openlocfilehash: 9b4834ae474d781497043bd8800879c57f36d785
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30276180"
---
# <a name="use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-list"></a><span data-ttu-id="77457-104">Utilisation du portail Supprimer de la liste pour vous supprimer de la liste des expéditeurs bloqués Office 365</span><span class="sxs-lookup"><span data-stu-id="77457-104">Use the delist portal to remove yourself from the Office 365 blocked senders list</span></span>

<span data-ttu-id="77457-p102">Obtenez-vous un message d'erreur lorsque vous tentez d'envoyer un courrier électronique à un destinataire dont l'adresse de messagerie est dans Office 365 ? Si vous pensez que vous ne devriez pas recevoir de message d'erreur, vous pouvez utiliser le portail Supprimer de la liste pour vous supprimer de la liste des expéditeurs bloqués Office 365.</span><span class="sxs-lookup"><span data-stu-id="77457-p102">Are you getting an error message when you try to send an email to a recipient whose email address is in Office 365? If you think you should not be receiving the error message, you can use the delist portal to remove yourself from the Office 365 blocked senders list.</span></span>
  
## <a name="what-is-the-office-365-blocked-senders-list"></a><span data-ttu-id="77457-107">Qu'est-ce que la liste des expéditeurs bloqués Office 365 ?</span><span class="sxs-lookup"><span data-stu-id="77457-107">What is the Office 365 blocked senders list?</span></span>

<span data-ttu-id="77457-p103">Microsoft utilise la liste des expéditeurs bloqués pour protéger ses clients contre le courrier indésirable, l'usurpation d'identité et les attaques par hameçonnage. L'adresse IP de votre serveur messagerie, c'est-à-dire l'adresse que votre serveur de messagerie utilise pour s'identifier sur Internet, a été identifiée comme une menace potentielle envers Office 365 pour une raison quelconque. Quand Office 365 ajoute l'adresse IP à la liste, cela empêche toute autre communication entre l'adresse IP et l'un de nos clients par le biais de nos centres de données.</span><span class="sxs-lookup"><span data-stu-id="77457-p103">Microsoft uses the blocked senders list to protect its customers from spam, spoofing, and phishing attacks. Your mail server's IP address, that is, the address your mail server uses to identify itself on the Internet, was tagged as a potential threat to Office 365 for one of a variety of reasons. When Office 365 adds the IP address to the list, it prevents all further communication between the IP address and any of our customers through our datacenters.</span></span>
  
<span data-ttu-id="77457-111">Vous savez que vous avez été ajouté à la liste si vous recevez une réponse à un courrier électronique incluant une erreur ressemblant à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="77457-111">You will know you have been added to the list when you receive a response to a mail message that includes an error that looks something like this:</span></span>
  
<span data-ttu-id="77457-p104">550 5.7.606-649 accès refusé, IP d'envoi interdit [_adresse IP_]; Pour demander la suppression de cette liste, https://sender.office.com/ visitez le site et suivez les instructions. Pour plus d'informations, consultez la rubrique notifications de [non-remise aux courriers électroniques dans Office 365](http://go.microsoft.com/fwlink/?LinkID=526653).</span><span class="sxs-lookup"><span data-stu-id="77457-p104">550 5.7.606-649 Access denied, banned sending IP [_IP address_]; To request removal from this list please visit https://sender.office.com/ and follow the directions. For more information please see [Email non-delivery reports in Office 365](http://go.microsoft.com/fwlink/?LinkID=526653).</span></span>
  
<span data-ttu-id="77457-114">où  _IP address_ est l'adresse IP de l'ordinateur sur lequel s'exécute le serveur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="77457-114">where  _IP address_ is the IP address of the computer on which the mail server runs.</span></span> 
  
### <a name="to-use-the-office-365-delist-portal-to-remove-yourself-from-the-blocked-senders-list"></a><span data-ttu-id="77457-115">Utilisation du portail Supprimer de la liste Office 365 pour vous supprimer de la liste des expéditeurs bloqués</span><span class="sxs-lookup"><span data-stu-id="77457-115">To use the Office 365 delist portal to remove yourself from the blocked senders list</span></span>

1. <span data-ttu-id="77457-116">Dans un navigateur web, accédez à [https://sender.office.com](https://sender.office.com).</span><span class="sxs-lookup"><span data-stu-id="77457-116">In a web browser, go to [https://sender.office.com](https://sender.office.com).</span></span>
    
2. <span data-ttu-id="77457-p105">Suivez les instructions de la page. Assurez-vous que vous utilisez l'adresse de messagerie à laquelle le message d'erreur a été envoyé et l'adresse IP qui est spécifiée dans le message d'erreur. Vous ne pouvez entrer qu'une adresse de messagerie et une adresse IP par visite.</span><span class="sxs-lookup"><span data-stu-id="77457-p105">Follow the instructions on the page. Ensure that you use the email address to which the error message was sent, and the IP address that is specified in the error message. You can only enter one email address and one IP address per visit.</span></span>
    
3. <span data-ttu-id="77457-120">Cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="77457-120">Click **Submit**.</span></span>
    
    <span data-ttu-id="77457-p106">Le portail envoie un courrier électronique à l'adresse de messagerie que vous indiquez. Le message électronique se présente comme suit: ![capture d'écran du courrier électronique reçu lorsque vous envoyez une demande via le portail supprimer de la liste](media/bf13e4f7-f68c-4e46-baa7-b6ab4cfc13f3.png)</span><span class="sxs-lookup"><span data-stu-id="77457-p106">The portal sends an email to the email address that you supply. The email will look something like the following:  ![Screenshot of email received when you submit a request through the delist portal](media/bf13e4f7-f68c-4e46-baa7-b6ab4cfc13f3.png)</span></span>
  
4. <span data-ttu-id="77457-123">Cliquez sur le lien de confirmation dans le courrier électronique envoyé par le portail de suppression de la liste.</span><span class="sxs-lookup"><span data-stu-id="77457-123">Click the confirmation link in the email sent to you by the delisting portal.</span></span>
    
    <span data-ttu-id="77457-124">Vous revenez au portail Supprimer de la liste.</span><span class="sxs-lookup"><span data-stu-id="77457-124">This brings you back to the delist portal.</span></span>
    
5. <span data-ttu-id="77457-125">Dans le portail Supprimer de la liste, cliquez sur **Supprimer l'adresse IP de la liste**.</span><span class="sxs-lookup"><span data-stu-id="77457-125">In the delist portal, click **Delist IP**.</span></span>
    
    <span data-ttu-id="77457-p107">Une fois que l'adresse IP est supprimée de la liste des expéditeurs bloqués, les messages électroniques provenant de cette adresse IP seront remis aux destinataires utilisant Office 365. Par conséquent, assurez-vous que les messages envoyés à partir de cette adresse IP ne sont pas abusifs ou malveillants. Dans le cas contraire, il est possible que l'adresse IP soit bloquée à nouveau.</span><span class="sxs-lookup"><span data-stu-id="77457-p107">After the IP address is removed from the blocked senders list, email messages from that IP address will be delivered to recipients who use Office 365. So, make sure you're confident that email sent from that IP address won't be abusive or malicious; otherwise, the IP address might be blocked again.</span></span>
    

