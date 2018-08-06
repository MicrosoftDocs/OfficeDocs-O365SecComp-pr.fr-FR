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
# <a name="safe-sender-and-blocked-sender-lists-in-exchange-online"></a>Listes des expéditeurs autorisés et des expéditeurs bloqués dans Exchange Online

En tant qu'administrateur Exchange Online ou Exchange Online Protection (EOP), vous pouvez faire en sorte qu'un message électronique circulant via le service ne soit pas marqué comme courrier indésirable. Une manière de procéder consiste à créer des listes d'expéditeurs approuvés et d'expéditeurs bloqués pour les membres de votre organisation. 
  
 *Consultez la version mise à jour des conseils et procédures sur l'utilisation de ces listes comme administrateur dans la rubrique relative à la* [procédure visant à empêcher que des courriers électroniques faux positifs soient marqués comme courrier indésirable à l'aide d'une liste fiable ou d'autres techniques](https://go.microsoft.com/fwlink/p/?LinkID=534224). 
  
Si vous n'êtes pas administrateur et que vous souhaitez simplement gérer votre propre courrier indésirable dans Outlook en utilisant une liste d'expéditeurs approuvés, consultez les étapes décrites dans cette présentation du [filtre de courrier indésirable](https://go.microsoft.com/fwlink/?LinkId=817222). 
  
## <a name="what-is-the-safe-and-blocked-sender-limits-in-exchange-online"></a>Quelles sont les limites d'expéditeurs autorisés et d'expéditeurs bloqués dans Exchange Online ?

Les limites d'expéditeurs autorisés et d'expéditeurs bloqués dans Exchange Online diffèrent des limites d'Active Directory et d'Outlook. Ces limites sont :
  
- Limite d’expéditeurs autorisés : 1 024
    
- Limite d’expéditeurs bloqués : 500
    
Remarque :
  
Vous pouvez rencontrer l’erreur qui est décrite dans KB 2590466 (« vous recevez l’erreur « Erreur de validation de courrier indésirable » dans Outlook Web App pour Exchange Server 2010 »). Pour résoudre ce problème, désactivez la case à cocher « Approuver les messages électroniques à partir de mes contacts ». Vous pouvez également réduire la quantité d’adresses de messagerie qui sont dans votre dossier de Contacts par défaut afin qu’elle le nombre maximal autorisé de limite de 1 024 dans Exchange Online est définie pour l’attribut « MaxSafeSenders ». Pour plus d’informations sur cet attribut et l’applet de commande Set-Mailbox, reportez-vous à la suite de rubrique :
  
[Set-Mailbox](https://docs.microsoft.com/en-us/powershell/module/exchange/mailboxes/Set-Mailbox?view=exchange-ps)
  
## <a name="see-also"></a>See also

[Sender filtering in Exchange 2016](http://technet.microsoft.com/library/b833f864-ff10-46a0-a653-28fb9ba30896.aspx)

