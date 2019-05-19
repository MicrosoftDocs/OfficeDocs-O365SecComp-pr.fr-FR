---
title: Listes des expéditeurs autorisés et des expéditeurs bloqués dans Exchange Online
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 111ab6b0-2dd2-4a87-a928-4931df6b3c4d
ms.collection:
- M365-security-compliance
description: En tant qu'administrateur Exchange Online ou Exchange Online Protection (EOP), vous pouvez faire en sorte qu'un message électronique circulant via le service ne soit pas marqué comme courrier indésirable. Une manière de procéder consiste à créer des listes d'expéditeurs approuvés et d'expéditeurs bloqués pour les membres de votre organisation.
ms.openlocfilehash: a6e8f98d6cb5930f7eb6f2059c957112026dd5d8
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34156696"
---
# <a name="safe-sender-and-blocked-sender-lists-in-exchange-online"></a>Listes des expéditeurs autorisés et des expéditeurs bloqués dans Exchange Online

En tant qu'administrateur Exchange Online ou Exchange Online Protection (EOP), vous pouvez faire en sorte qu'un message électronique circulant via le service ne soit pas marqué comme courrier indésirable. Une manière de procéder consiste à créer des listes d'expéditeurs approuvés et d'expéditeurs bloqués pour les membres de votre organisation. 
  
 *Consultez la version mise à jour des conseils et procédures sur l'utilisation de ces listes comme administrateur dans la rubrique relative à la* [procédure visant à empêcher que des courriers électroniques faux positifs soient marqués comme courrier indésirable à l'aide d'une liste fiable ou d'autres techniques](https://go.microsoft.com/fwlink/p/?LinkID=534224). 
  
Si vous n'êtes pas administrateur et que vous souhaitez simplement gérer votre propre courrier indésirable dans Outlook en utilisant une liste d'expéditeurs approuvés, consultez les étapes décrites dans cette présentation du [filtre de courrier indésirable](https://go.microsoft.com/fwlink/?LinkId=817222). 
  
## <a name="what-is-the-safe-and-blocked-sender-limits-in-exchange-online"></a>Quelles sont les limites d’expéditeurs autorisés et d’expéditeurs bloqués dans Exchange Online ?

Les limites d’expéditeurs autorisés et d’expéditeurs bloqués dans Exchange Online diffèrent des limites d’Active Directory et d’Outlook. Ces limites sont :
  
- Limite d’expéditeurs autorisés: 1 024
    
- Limite des expéditeurs bloqués: 500
    
Remarque :
  
Vous pouvez observer l’erreur décrite dans [KB2590466](https://support.microsoft.com/help/2590466/you-receive-the-error-junk-e-mail-validation-error-in-outlook-web-app). Pour résoudre ce problème, désactivez la case à cocher «approuver les courriers électroniques en provenance de mes contacts». Vous pouvez également réduire le nombre d’adresses de messagerie figurant dans votre dossier de contacts par défaut afin de l’appliquer à la limite maximale autorisée de 1024 dans Exchange Online qui est définie pour l’attribut «Paramètres MaxSafeSenders». Pour plus d’informations sur cet attribut et sur la cmdlet Set-Mailbox, voirscript rubrique suivante:
  
[Set-Mailbox](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Set-Mailbox)
  
## <a name="see-also"></a>Voir aussi

[Sender filtering in Exchange 2016](http://technet.microsoft.com/library/b833f864-ff10-46a0-a653-28fb9ba30896.aspx)

