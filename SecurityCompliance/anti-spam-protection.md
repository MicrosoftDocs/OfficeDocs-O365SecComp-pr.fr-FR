---
title: Protection contre le courrier indésirable de messagerie Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 6a601501-a6a8-4559-b2e7-56b59c96a586
description: En savoir plus sur les paramètres de blocage du courrier indésirable et les filtres qui vous aideront à que vous éviter le courrier indésirable dans Exchange Online et Office 365. Obtention d’un volume trop important du courrier indésirable dans Office 365 ? Vous pouvez personnaliser vos filtres de courrier indésirable et les paramètres de stratégie de blocage du courrier indésirable.
ms.openlocfilehash: 0a23ddd0610599bbd6478781c61e5e32b06726bc
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29652269"
---
# <a name="office-365-email-anti-spam-protection"></a>Protection contre le courrier indésirable pour Office 365

Sont concernés trop courrier indésirable dans Office 365 ? Nous avons intégré plusieurs filtres anti-spam dans votre service Office 365 ou Exchange Online Protection (EOP), afin que vos courriers électroniques depuis le moment où que votre premier message. Afin d’éviter le courrier indésirable dans Office 365, vous souhaiterez peut-être modifier un paramètre de protection pour traiter un problème spécifique dans votre organisation, dites que vous recevez beaucoup de courrier indésirable d’un expéditeur particulier, par exemple, ou pour simplement fine régler vos paramètres afin qu’ils soient adaptées selon les besoins de votre organisation. Pour ce faire, vous pouvez modifier les paramètres de blocage du courrier indésirable de sécurité Office 365 &amp; centre de conformité.
  
Cet article est destiné aux administrateurs Office 365. Si vous n’êtes pas un administrateur, mais vous êtes un utilisateur d’Office 365 et que vous souhaitez apprendre à gérer le courrier indésirable que vous recevez, ce n’est pas l’article que vous recherchez. Au lieu de cela, si vous utilisez Outlook pour PC ou Outlook pour Mac, démarrez avec une [vue d’ensemble du filtre de courrier indésirable](https://support.office.com/article/5ae3ea8e-cf41-4fa0-b02a-3b96e21de089). Si vous utilisez Outlook sur le web, démarrez avec [obtenir des informations sur le courrier indésirable et l’hameçonnage](https://support.office.com/article/86c1d76f-4d5a-4967-9647-35665dc17c31).
  
## <a name="these-options-help-you-prevent-spam-in-office-365"></a>Ces options de vous aider à éviter le courrier indésirable dans Office 365

 **Le filtrage des connexions.** Lorsque vous utilisez le filtrage des connexions, Office 365 vérifie la réputation de l’expéditeur avant de passer d’un message. Vous pouvez créer une liste verte ou la liste des expéditeurs approuvés, pour vous assurer que vous recevez tous les messages envoyés à partir d’une adresse IP spécifique ou une plage d’adresses IP. Vous pouvez également créer une liste d’adresses IP à partir de laquelle bloquer des messages, appelés une liste rouge. Pour plus d’informations, voir [configurer la stratégie de filtrage de connexion](https://technet.microsoft.com/library/jj200718%28v=exchg.150%29.aspx). Si vous craignez du courrier indésirable dans Office 365, utilisez le filtrage des connexions pour éviter le courrier indésirable.
  
Pour les clients qui ont Office 365 entreprise E5 ou ont acheté des licences Advanced Threat Protection (DAV), le filtrage des connexions est utilisé par l’aide à la décision usurpation d’identité pour créer de liste verte et la liste des expéditeurs qui sont l’usurpation de votre domaine. Pour plus d’informations, voir [en savoir plus sur l’aide à la décision usurpation d’identité](https://go.microsoft.com/fwlink/?LinkID=735009).
  
 **Filtrage du courrier indésirable.** Office 365 vérifie les caractéristiques des messages compatibles avec le courrier indésirable à l’aide de filtrage du courrier indésirable. Vous pouvez modifier les actions prennent sur les messages identifiés comme courrier indésirable, et indiquez si vous souhaitez filtrer les messages enregistrés dans des langues spécifiques, ou envoyés à partir de certains pays ou régions. Vous pouvez également activer avancé du courrier indésirable options de filtrage si vous souhaitez adopter une approche agressive pour le filtrage du courrier indésirable. En outre, vous pouvez configurer les notifications de courrier indésirable de l’utilisateur final pour informer les utilisateurs lorsque les messages pour qu’ils ont été mis en quarantaine à la place. (L’envoi de messages en quarantaine est une des actions configurables.) À partir de ces notifications, les utilisateurs finaux peuvent version faux positifs et les signaler à Microsoft pour analyse. Pour plus d’informations, voir [configurer vos stratégies de filtrage du courrier indésirable](https://go.microsoft.com/fwlink/p/?LinkId=617147). Afin de vous aider à éviter le courrier indésirable dans Office 365, utilisez le filtrage, du courrier indésirable si vous craignez trop du courrier indésirable dans Office 365, utilisez le filtrage des connexions pour éviter le courrier indésirable.
  
> [!NOTE]
> Pour les clients autonomes EOP : par défaut, les filtres anti-spam EOP envoient des messages de courrier indésirable détectés au dossier courrier indésirable de chaque destinataire. Toutefois, afin de vous assurer que l’action **déplacer le message vers le dossier courrier indésirable** fonctionne avec les boîtes aux lettres locales, vous devez configurer deux règles de transport Exchange sur vos serveurs sur site pour détecter les en-têtes de spam ajoutés par EOP. Pour plus d’informations, voir [vous assurer que le courrier indésirable est routé vers le dossier courrier indésirable de chaque utilisateur](https://technet.microsoft.com/library/jj837173%28v=exchg.150%29.aspx). 
  
## <a name="extra-information-if-you-receive-too-much-spam-in-office-365"></a>Informations supplémentaires si vous recevez trop du courrier indésirable dans Office 365

La vidéo suivante fournit une vue d’ensemble de la configuration du filtrage dans EOP du courrier indésirable.
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/608be94c-d763-4c47-af94-99e7cb277713?autoplay=false]
  
Pour plus d’informations, consultez la rubrique [configuration de stratégies de filtrage de courrier indésirable](https://go.microsoft.com/fwlink/p/?LinkId=617147) .
  
## <a name="check-your-outgoing-messages-to-prevent-spam-in-office-365"></a>Vérifier vos messages sortants afin d’éviter le courrier indésirable dans Office 365

 **Filtrage sortant.** Office 365 vérifie également pour vous assurer que vos utilisateurs n’envoient du courrier indésirable. Par exemple, ordinateur d’un utilisateur peut obtenir infecté par un programme malveillant qui entraîne sa envoyer des messages de courrier indésirable, nous créons une protection contre qui a appelé le *filtrage sortant* . Vous ne pouvez pas désactiver le filtrage sortant, mais vous pouvez configurer les paramètres indiqués dans [Configure la stratégie anti-courrier indésirable sortant](https://technet.microsoft.com/library/jj200737%28v=exchg.150%29.aspx). Si vous craignez trop du courrier indésirable dans Office 365, utilisez le filtrage sortant pour éviter le courrier indésirable dans Exchange Online.
  
## <a name="beyond-the-basics-more-ways-to-prevent-spam-in-office-365"></a>Aller : plusieurs manières afin d’éviter le courrier indésirable dans Office 365

 **Règles de flux de messagerie.** Si vous voulez aller au-delà de filtrage du courrier indésirable intégré et créer des règles personnalisées qui sont basés sur les stratégies de votre entreprise, *[les règles de flux de messagerie](https://technet.microsoft.com/library/jj919238%28v=exchg.150%29.aspx)*, également appelées *règles de transport*, sont un autre filtre qui vous aident à éviter le courrier indésirable dans Office 365. Par exemple, vous pouvez utiliser les règles de flux de messagerie pour définir la valeur au niveau de (SCL) spam confidence pour les messages qui correspondent aux conditions spécifiques, comme décrit dans [utiliser des règles de flux de messagerie pour définir le niveau de confiance du courrier indésirable (SCL) dans les messages](https://technet.microsoft.com/library/dn798345%28v=exchg.150%29.aspx).
  
 **L’authentification du courrier électronique.** Les techniques qui utilisent le système de nom de domaine (DNS) pour ajouter des informations vérifiables pour les messages électroniques à propos de l’expéditeur d’un message électronique sont appelées l’authentification du courrier électronique. Plus avancées Office 365 administrateurs peut-il utiliser de ces méthodes d’authentification électronique :
  
- **Sender Policy Framework (SPF).** SPF valide l’origine de messages électroniques en vérifiant l’adresse IP de l’expéditeur contre le propriétaire du domaine présumé. Pour une présentation rapide pour SPF et pour obtenir une configuration rapidement, voir [Set up SPF dans Office 365 afin d’empêcher l’usurpation d’identité](https://technet.microsoft.com/library/dn789058%28v=exchg.150%29.aspx). Pour une présentation plus approfondie de la façon dont Office 365 utilise SPF, ou pour les déploiements de résolution des problèmes ou non standard telles que les déploiements hybrides, démarrez avec la [façon dont Office 365 utilise Framework SPF (Sender Policy) pour empêcher l’usurpation d’identité](https://technet.microsoft.com/library/mt712724%28v=exchg.150%29.aspx).

- **DomainKeys identifié Mail (DKIM).** DKIM permet d’associer une signature numérique aux messages électroniques dans l’en-tête du message de messages électroniques que vous envoyez. Systèmes de messagerie recevoir du courrier électronique à partir de votre domaine permet de déterminer si le courrier électronique entrant qu’ils reçoivent est légitime cette signature numérique. Pour plus d’informations sur Office 365 et DKIM, voir [DKIM utilisés pour valider le courrier sortant envoyé à partir de votre domaine dans Office 365](https://technet.microsoft.com/library/mt695945%28v=exchg.150%29.aspx).

- **L’authentification basée sur le domaine de Message, création de rapports et de conformité (DMARC).** Permet DMARC recevoir des systèmes de messagerie de déterminer comment traiter les messages qui échouent lors des vérifications SPF ou DKIM et fournit un niveau de confiance pour les partenaires de votre courrier électronique. Pour plus d’informations sur la configuration DMARC, voir [Utiliser DMARC pour valider le courrier dans Office 365](https://technet.microsoft.com/library/mt734386%28v=exchg.150%29.aspx).

Si vous êtes concerné sur le courrier indésirable, l’hameçonnage et l’usurpation d’identité dans Office 365, utiliser SPF, DKIM et DMARC pour éviter le courrier indésirable et l’usurpation d’identité indésirables.
  
 **Paramètres de l’utilisateur final géré.** Si vous recherchez des informations sur comment les utilisateurs finaux peuvent gérer leurs propres paramètres du courrier indésirable, consultez la rubrique [vue d’ensemble du filtre de courrier indésirable](https://go.microsoft.com/fwlink/?LinkId=270065) (pour les utilisateurs de Microsoft Outlook) ou d' [obtenir des informations sur le courrier indésirable et l’hameçonnage](https://go.microsoft.com/fwlink/?LinkId=270068) (pour Outlook sur les utilisateurs web). Si vous utilisez EOP pour protéger les boîtes aux lettres locales, veillez à utiliser la synchronisation d’annuaires pour vous assurer que ces paramètres sont synchronisées sur le service. Pour plus d’informations sur la configuration de la synchronisation d’annuaires, voir « Utiliser la synchronisation d’annuaires pour gérer les utilisateurs de messagerie » dans [Gérer les utilisateurs de messagerie dans EOP](https://technet.microsoft.com/library/dn636911%28v=exchg.150%29.aspx).
  
## <a name="for-more-information"></a>Pour plus d’informations

[Blog : Pourquoi le courrier indésirable et l’hameçonnage obtenir via Office 365 ?](https://go.microsoft.com/fwlink/?LinkId=528179 )
  
[Forum Aux Questions sur la protection anti-courrier indésirable](https://technet.microsoft.com/library/jj937231%28v=exchg.150%29.aspx)
  
[Empêcher le marquage des faux positifs comme courrier indésirable à l’aide d’une liste fiable ou d’autres techniques](prevent-email-from-being-marked-as-spam-0.md)
  
[Comment configurer le filtrage d’Office 365 pour vous aider à bloquer les messages indésirables](block-email-spam-to-prevent-false-negatives.md)
  
[Quelle est la différence entre courrier indésirable et les messages électroniques en masse ?](https://technet.microsoft.com/library/dn720441%28v=exchg.150%29.aspx)
  
[En-têtes de messages anti-courrier indésirable](https://technet.microsoft.com/library/dn205071%28v=exchg.150%29.aspx)
  
[Messages de RÉTRODIFFUSION et EOP](https://technet.microsoft.com/library/dn499795%28v=exchg.150%29.aspx)

## <a name="more-resources"></a>Ressources complémentaires

[Obtenir de l'aide dans les forums de la Communauté Office 365](https://go.microsoft.com/fwlink/p/?LinkId=518605)
  
[Administrateurs : Se connecter et créer une demande de service](https://go.microsoft.com/fwlink/p/?LinkId=519124)
  
[Administrateurs : appeler le support](https://go.microsoft.com/fwlink/p/?LinkID=518322)
