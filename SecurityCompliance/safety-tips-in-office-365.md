---
title: Conseils de sécurité dans les messages électroniques dans Office 365
ms.author: tracyp
author: MSFTTracyP
manager: scotv
ms.date: 10/6/2016
audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- BCS160
ms.assetid: fb4f8e49-0468-4be2-8fa6-99501f1ad9d5
ms.collection:
- M365-security-compliance
description: Présente des conseils de sécurité pour les messages électroniques filtrés par le filtre de courrier indésirable EOP et Office 365.
ms.openlocfilehash: b5501459a56dcff322dfdfa05d019d7fb626f369
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34156986"
---
# <a name="safety-tips-in-email-messages-in-office-365"></a>Conseils de sécurité dans les messages électroniques dans Office 365

Exchange Online Protection (EOP) et Office 365 vous protègent contre le courrier indésirable, le hameçonnage et la protection contre les programmes malveillants. À l’heure actuelle, certaines de ces attaques sont tellement bien conçues qu’elles semblent légitimes. L’envoi de messages vers le dossier courrier indésirable n’est pas toujours suffisant. À présent, lorsque vous vérifiez votre courrier électronique dans Outlook ou Outlook sur le Web, EOP vérifie automatiquement l’expéditeur et ajoute un Conseil de sécurité en haut du message. 
  
Le Conseil de sécurité, un message codé en couleur, vous avertit des messages potentiellement dangereux. La plupart des messages de votre boîte de réception n’ont pas de Conseil de sécurité. Vous ne les verrez que lorsque EOP et Office 365 dispose des informations dont vous avez besoin pour éviter le courrier indésirable, le hameçonnage et les programmes malveillants. Si les conseils de sécurité s’affichent dans votre boîte de réception, vous pouvez utiliser les exemples suivants pour en savoir plus sur chaque type de Conseil de sécurité.
  
- Courrier suspect (Conseil de sécurité rouge).
    
    ![Capture d’écran illustrant un Conseil de sécurité rouge.](media/5078a0be-e556-44a1-b169-09d780d26898.png)
  
    Un Conseil de sécurité rouge dans un message électronique signifie que le message que vous avez reçu contient un message suspect, tel qu’une escroquerie de type hameçonnage. Nous vous recommandons de supprimer ce type de message électronique de votre boîte de réception sans l’ouvrir.
    
- Courrier indésirable (Conseil de sécurité jaune).
    
    ![Capture d’écran illustrant un Conseil de sécurité jaune.](media/793c9265-ea44-48fd-a98f-804fadd4163b.png)
  
    Un Conseil de sécurité jaune dans un message électronique signifie que le message a été marqué comme courrier indésirable. Si vous ne reconnaissez pas et ne faites pas confiance à l’expéditeur du message, ne téléchargez pas de pièces jointes ou d’images et ne cliquez sur aucun lien dans le message. Dans Outlook sur le Web, vous pouvez cliquer sur **ce message n’est pas un courrier** indésirable dans la barre jaune d’un élément de courrier indésirable pour déplacer le message vers votre boîte de réception. Si le Conseil de sécurité jaune apparaît sur un message qui a été remis dans votre boîte de réception, c’est probablement parce que vous avez désactivé le mouvement du courrier indésirable dans votre dossier courrier indésirable. 
    
- Courrier fiable (Conseil de sécurité vert).
    
    ![Capture d’écran illustrant un Conseil de sécurité vert.](media/acbc11d0-f626-4848-9fbf-66eeeda3f803.png)
  
    En plus des messages non sécurisés, nous vous informerons également sur les messages valides provenant d’expéditeurs que nous approuvons avec un Conseil de sécurité vert. Un Conseil de sécurité vert dans un message électronique signifie que nous avons vérifié l’expéditeur du message et vérifié qu’il était sûr. Microsoft conserve cette liste d’expéditeurs approuvés qui inclut des organisations financières et d’autres personnes fréquemment usurpées ou empruntées d’identité.
    
- Courrier non filtré (Conseil de sécurité gris).
    
    ![Capture d’écran illustrant un Conseil de sécurité gris.](media/c4d0cf8f-08e9-4c84-beee-1d9e0b022e0a.png)
  
    Nous vous indiquerons également quand nous avons ignoré la vérification d’un message, car il provient d’un expéditeur que vous approuvez sur votre liste des expéditeurs approuvés ou si une règle de flux de messagerie existe pour contourner le filtrage. 
    
    Le Conseil de sécurité gris s’affiche également lorsque les images externes sont bloquées, c’est-à-dire que le message se trouve dans votre boîte de réception et qu’il ne semble pas être un courrier indésirable, mais il contient des images externes que vous n’avez pas choisi de télécharger.
    
## <a name="working-with-safety-tips"></a>Utilisation des conseils de sécurité

Les conseils de sécurité sont toujours activés pour Outlook sur le Web, même si tous les messages ne recevront pas tous les messages. Les administrateurs d’Office 365 peuvent désactiver les conseils de sécurité pour d’autres clients de messagerie, tels qu’Outlook. Pour plus d’informations, consultez la rubrique [activation ou désactivation des conseils de sécurité dans Office 365](enable-or-disable-safety-tips.md).
  
Si vous n’êtes pas d’accord avec la façon dont Office 365 et EOP ont catégorisé un message (c’est-à-dire qu’il ne s’agit pas d’un courrier indésirable ou qu’il n’est pas légitime), vous pouvez envoyer les messages pour analyse afin de faciliter votre expérience. Pour plus d’informations, voir [Report junk email and phishing scams in Outlook on the web](https://technet.microsoft.com/library/dn594557.aspx). Vous pouvez également cliquer sur le lien Commentaires dans le Conseil de sécurité pour envoyer des commentaires directement à Microsoft afin de nous aider à améliorer.
  
## <a name="see-also"></a>Voir aussi

[Activer ou désactiver les conseils de sécurité dans Office 365](enable-or-disable-safety-tips.md)

