---
title: Listes des expéditeurs autorisés et des expéditeurs bloqués dans Exchange Online
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/22/2018
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 111ab6b0-2dd2-4a87-a928-4931df6b3c4d
description: En tant qu'administrateur Exchange Online ou Exchange Online Protection (EOP), vous pouvez faire en sorte qu'un message électronique circulant via le service ne soit pas marqué comme courrier indésirable. Une manière de procéder consiste à créer des listes d'expéditeurs approuvés et d'expéditeurs bloqués pour les membres de votre organisation.
ms.openlocfilehash: fcb43f990750782788dc6f459dd5c7d296146a38
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22028081"
---
# <a name="safe-sender-and-blocked-sender-lists-in-exchange-online"></a><span data-ttu-id="8db3a-104">Listes des expéditeurs autorisés et des expéditeurs bloqués dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="8db3a-104">Safe sender and blocked sender lists in Exchange Online</span></span>

<span data-ttu-id="8db3a-p102">En tant qu'administrateur Exchange Online ou Exchange Online Protection (EOP), vous pouvez faire en sorte qu'un message électronique circulant via le service ne soit pas marqué comme courrier indésirable. Une manière de procéder consiste à créer des listes d'expéditeurs approuvés et d'expéditeurs bloqués pour les membres de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8db3a-p102">As an Exchange Online or Exchange Online Protection (EOP) administrator, you can help ensure that an email message traveling through the service isn't marked as spam. One way to do this is to create safe sender and blocked sender lists for the people in your organization.</span></span> 
  
 <span data-ttu-id="8db3a-107">*Consultez la version mise à jour des conseils et procédures sur l'utilisation de ces listes comme administrateur dans la rubrique relative à la* [procédure visant à empêcher que des courriers électroniques faux positifs soient marqués comme courrier indésirable à l'aide d'une liste fiable ou d'autres techniques](https://go.microsoft.com/fwlink/p/?LinkID=534224).</span><span class="sxs-lookup"><span data-stu-id="8db3a-107">*See the updated version of the tips and procedures for how to work with these lists as an admin in* [Prevent false positive email marked as spam with a safelist or other techniques](https://go.microsoft.com/fwlink/p/?LinkID=534224).</span></span> 
  
<span data-ttu-id="8db3a-108">Si vous n'êtes pas administrateur et que vous souhaitez simplement gérer votre propre courrier indésirable dans Outlook en utilisant une liste d'expéditeurs approuvés, consultez les étapes décrites dans cette présentation du [filtre de courrier indésirable](https://go.microsoft.com/fwlink/?LinkId=817222).</span><span class="sxs-lookup"><span data-stu-id="8db3a-108">If you're not an admin, and you just want to manage your own junk email in Outlook by using a safe sender list, check out the steps in this overview of [the Junk Email Filter](https://go.microsoft.com/fwlink/?LinkId=817222).</span></span> 
  
## <a name="what-is-the-safe-and-blocked-sender-limits-in-exchange-online"></a><span data-ttu-id="8db3a-109">Quelles sont les limites d'expéditeurs autorisés et d'expéditeurs bloqués dans Exchange Online ?</span><span class="sxs-lookup"><span data-stu-id="8db3a-109">What is the safe and blocked sender limits in Exchange Online?</span></span>

<span data-ttu-id="8db3a-p103">Les limites d'expéditeurs autorisés et d'expéditeurs bloqués dans Exchange Online diffèrent des limites d'Active Directory et d'Outlook. Ces limites sont :</span><span class="sxs-lookup"><span data-stu-id="8db3a-p103">The safe and blocked sender limits in Exchange Online differ from the Active Directory and Outlook limits. They are:</span></span>
  
- <span data-ttu-id="8db3a-112">Limite d’expéditeurs autorisés : 1 024</span><span class="sxs-lookup"><span data-stu-id="8db3a-112">Safe sender limit: 1,024</span></span>
    
- <span data-ttu-id="8db3a-113">Limite d’expéditeurs bloqués : 500</span><span class="sxs-lookup"><span data-stu-id="8db3a-113">Blocked sender limit: 500</span></span>
    
<span data-ttu-id="8db3a-114">Remarque :</span><span class="sxs-lookup"><span data-stu-id="8db3a-114">Note:</span></span>
  
<span data-ttu-id="8db3a-p104">Vous pouvez rencontrer l’erreur qui est décrite dans KB 2590466 (« vous recevez l’erreur « Erreur de validation de courrier indésirable » dans Outlook Web App pour Exchange Server 2010 »). Pour résoudre ce problème, désactivez la case à cocher « Approuver les messages électroniques à partir de mes contacts ». Vous pouvez également réduire la quantité d’adresses de messagerie qui sont dans votre dossier de Contacts par défaut afin qu’elle le nombre maximal autorisé de limite de 1 024 dans Exchange Online est définie pour l’attribut « MaxSafeSenders ». Pour plus d’informations sur cet attribut et l’applet de commande Set-Mailbox, reportez-vous à la suite de rubrique :</span><span class="sxs-lookup"><span data-stu-id="8db3a-p104">You may experience the error that is described in KB 2590466 ("You receive the error "Junk e-mail validation error" in Outlook Web App for Exchange Server 2010"). To resolve this issue, clear the "Trust emails from my contacts" check box. Alternatively, decrease the amount of email addresses that are in your default Contacts folder to bring it within the maximum allowed limit of 1,024 in Exchange Online that is set for "MaxSafeSenders" attribute. For more information about this attribute and the Set-Mailbox cmdlet, seethe following topic:</span></span>
  
[<span data-ttu-id="8db3a-119">Set-Mailbox</span><span class="sxs-lookup"><span data-stu-id="8db3a-119">Set-Mailbox</span></span>](https://docs.microsoft.com/en-us/powershell/module/exchange/mailboxes/Set-Mailbox?view=exchange-ps)
  
## <a name="see-also"></a><span data-ttu-id="8db3a-120">See also</span><span class="sxs-lookup"><span data-stu-id="8db3a-120">See also</span></span>

[<span data-ttu-id="8db3a-121">Sender filtering in Exchange 2016</span><span class="sxs-lookup"><span data-stu-id="8db3a-121">Sender filtering in Exchange 2016</span></span>](http://technet.microsoft.com/library/b833f864-ff10-46a0-a653-28fb9ba30896.aspx)

