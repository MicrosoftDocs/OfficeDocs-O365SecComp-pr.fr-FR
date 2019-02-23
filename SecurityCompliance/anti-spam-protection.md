---
title: Protection contre le courrier indésirable pour les courriers électroniques Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 6a601501-a6a8-4559-b2e7-56b59c96a586
ms.collection:
- M365-security-compliance
description: Découvrez les paramètres de blocage du courrier indésirable et les filtres qui vous permettront d'éviter le courrier indésirable dans Exchange Online et Office 365. Vous recevez trop de courrier indésirable dans Office 365? Vous pouvez personnaliser vos filtres de courrier indésirable et votre stratégie de blocage du courrier indésirable.
ms.openlocfilehash: 2d8f433cabda4408da2e29b7bc6570e09e6989dd
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30223423"
---
# <a name="office-365-email-anti-spam-protection"></a>Protection contre le courrier indésirable pour Office 365

Vous vous inquiétez de trop de courrier indésirable dans Office 365? Nous avons créé plusieurs filtres de courrier indésirable dans votre service Office 365 ou Exchange Online Protection (EOP), afin que votre courrier électronique soit protégé dès que vous recevez votre premier message. Afin d'éviter le courrier indésirable dans Office 365, vous pouvez modifier un paramètre de protection pour résoudre un problème spécifique dans votre organisation (par exemple, vous recevez un grand nombre de courriers indésirables d'un expéditeur particulier, par exemple) ou pour affiner vos paramètres de sorte qu'ils soient adapté pour répondre au mieux aux besoins de votre organisation. Pour ce faire, vous pouvez modifier les paramètres de blocage du courrier indésirable &amp; dans le centre de sécurité conformité Office 365.
  
Cet article est destiné aux administrateurs Office 365. Si vous n'êtes pas administrateur, mais que vous êtes un utilisateur d'Office 365 et que vous souhaitez savoir comment gérer le courrier indésirable que vous recevez, il ne s'agit pas de l'article que vous recherchez. Au lieu de cela, si vous utilisez Outlook pour PC ou Outlook pour Mac, commencez avec [Présentation du filtre de](https://support.office.com/article/5ae3ea8e-cf41-4fa0-b02a-3b96e21de089)courrier indésirable. Si vous utilisez Outlook sur le Web, commencez par [en savoir plus sur](https://support.office.com/article/86c1d76f-4d5a-4967-9647-35665dc17c31)le courrier indésirable et le hameçonnage.
  
## <a name="these-options-help-you-prevent-spam-in-office-365"></a>Ces options vous aident à empêcher le courrier indésirable dans Office 365

 **Filtrage des connexions.** Lorsque vous utilisez le filtrage des connexions, Office 365 vérifie la réputation de l'expéditeur avant d'autoriser l'accès à un message. Vous pouvez créer une liste verte, ou liste des expéditeurs approuvés, pour vous assurer que vous recevez tous les messages qui vous sont envoyés à partir d'une adresse IP spécifique ou d'une plage d'adresses IP. Vous pouvez également créer une liste d'adresses IP à partir de laquelle bloquer les messages, appelée liste rouge. Pour plus d'informations, consultez [la rubrique Configure the connection filter Policy](https://technet.microsoft.com/library/jj200718%28v=exchg.150%29.aspx). Si vous êtes préoccupé par le courrier indésirable dans Office 365, utilisez le filtrage des connexions pour éviter le courrier indésirable.
  
Pour les clients qui ont Office 365 entreprise E5 ou qui ont acheté des licences protection avancée contre les menaces (ATP), le filtrage des connexions est utilisé par l'aide à l'usurpation pour créer des listes d'expéditeurs autorisés et bloqués qui usurpent votre domaine. Pour plus d'informations, consultez la rubrique [en savoir plus sur](https://go.microsoft.com/fwlink/?LinkID=735009)les informations d'usurpation d'identité.
  
 **Filtrage du courrier indésirable.** Office 365 recherche les caractéristiques de message cohérentes avec le courrier indésirable à l'aide du filtrage du courrier indésirable. Vous pouvez modifier les actions à effectuer sur les messages identifiés comme courrier indésirable et choisir de filtrer les messages rédigés dans des langues spécifiques ou à partir de pays ou régions spécifiques. Vous pouvez également activer les options avancées de filtrage du courrier indésirable si vous souhaitez adopter une approche agressive en matière de filtrage du courrier indésirable. De plus, vous pouvez configurer les notifications de courrier indésirable de l'utilisateur final pour informer les utilisateurs lorsque des messages destinés à leur mise en quarantaine ont été envoyés. (L'envoi de messages vers la quarantaine est l'une des actions configurables.) À partir de ces notifications, les utilisateurs finaux peuvent lancer des faux positifs et les signaler à Microsoft pour analyse. Pour plus d'informations, consultez [la rubrique Configuration de vos stratégies de filtrage du courrier](https://go.microsoft.com/fwlink/p/?LinkId=617147)indésirable. Afin d'éviter le courrier indésirable dans Office 365, utilisez le filtrage du courrier indésirable, si vous craignez le courrier indésirable dans Office 365, utilisez le filtrage des connexions pour éviter le courrier indésirable.
  
> [!NOTE]
> Pour les clients autonomes EOP: par défaut, les filtres de courrier indésirable EOP envoient des messages détectés par courrier indésirable dans le dossier courrier inDésirable des destinataires. Toutefois, pour vous assurer que l'action **déplacer le message vers le dossier** courrier indésirable fonctionnera avec des boîtes aux lettres locales, vous devez configurer deux règles de transport Exchange sur vos serveurs locaux pour détecter les en-têtes de courrier indésirable ajoutés par EOP. Pour plus d'informations, consultez [la rubrique s'assurer que le courrier indésirable est acheminé vers le dossier de courrier indésirable de chaque utilisateur](https://technet.microsoft.com/library/jj837173%28v=exchg.150%29.aspx). 
  
## <a name="extra-information-if-you-receive-too-much-spam-in-office-365"></a>Informations supplémentaires si vous recevez trop de courrier indésirable dans Office 365

La vidéo suivante fournit une vue d'ensemble de la configuration du filtrage du courrier indésirable dans EOP.
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/608be94c-d763-4c47-af94-99e7cb277713?autoplay=false]
  
Pour plus d'informations, consultez la rubrique [configurer les stratégies de filtrage du courrier](https://go.microsoft.com/fwlink/p/?LinkId=617147) indésirable.
  
## <a name="check-your-outgoing-messages-to-prevent-spam-in-office-365"></a>Vérifier les messages sortants pour éviter le courrier indésirable dans Office 365

 **Filtrage sortant.** Office 365 vérifie également que les utilisateurs n'envoient pas de courrier indésirable. Par exemple, l'ordinateur d'un utilisateur peut être infecté par un programme malveillant qui lui envoie des messages de courrier indésirable, nous créons ainsi une protection contre ce qui a été appelé *filtrage sortant* . Vous ne pouvez pas désactiver le filtrage sortant, mais vous pouvez configurer les paramètres décrits dans [configurer la stratégie anti-courrier indésirable sortant](https://technet.microsoft.com/library/jj200737%28v=exchg.150%29.aspx). Si vous craignez de trop de courrier indésirable dans Office 365, utilisez le filtrage sortant pour éviter le courrier indésirable dans Exchange Online.
  
## <a name="beyond-the-basics-more-ways-to-prevent-spam-in-office-365"></a>Au-delà des notions de base: autres méthodes pour empêcher le courrier indésirable dans Office 365

 **Règles de flux de messagerie.** Si vous souhaitez aller au-delà du filtrage de courrier indésirable intégré et créer des règles personnalisées basées sur vos stratégies professionnelles, les *[règles de flux de messagerie](https://technet.microsoft.com/library/jj919238%28v=exchg.150%29.aspx)*, également appelées règles de *transport*, sont un autre filtre qui vous permet d'éviter le courrier indésirable dans Office 365. Par exemple, vous pouvez utiliser des règles de flux de messagerie pour définir la valeur de seuil de probabilité de courrier indésirable (SCL) pour les messages qui répondent à des conditions spécifiques, comme décrit dans [use mail Flow Rules to Set the Spam Confidence Level (SCL) dans les messages](https://technet.microsoft.com/library/dn798345%28v=exchg.150%29.aspx).
  
 **Authentification de messagerie.** Les techniques qui utilisent le système DNS (Domain Name System) pour ajouter des informations vérifiables aux messages électroniques concernant l'expéditeur d'un message électronique sont appelées authentification de messagerie. Les administrateurs Office 365 plus avancés peuvent utiliser ces méthodes d'authentification de messagerie:
  
- **SPF (Sender Policy Framework).** SPF valide l'origine des messages électroniques en vérifiant l'adresse IP de l'expéditeur par rapport au propriétaire allégué du domaine d'envoi. Pour une présentation rapide de SPF et pour qu'il soit configuré rapidement, reportez-vous à la rubrique [set up SPF in Office 365 pour éviter l'usurpation](https://technet.microsoft.com/library/dn789058%28v=exchg.150%29.aspx). Pour mieux comprendre comment Office 365 utilise SPF, ou pour résoudre des problèmes ou des déploiements non standard tels que des déploiements hybrides, commencez par [Comment office 365 utilise SPF (Sender Policy Framework) pour éviter l'usurpation](https://technet.microsoft.com/library/mt712724%28v=exchg.150%29.aspx).

- **DomainKeys Identified Identified Mail (DKIM).** DKIM vous permet de joindre une signature numérique aux messages électroniques dans l'en-tête des messages électroniques que vous envoyez. Les systèmes de messagerie qui reçoivent le courrier de votre domaine utilisent cette signature numérique pour déterminer si le courrier entrant qu'ils reçoivent est légitime. Pour plus d'informations sur DKIM et Office 365, voir [use DKIM pour valider les messages sortants envoyés à partir de votre domaine dans Office 365](https://technet.microsoft.com/library/mt695945%28v=exchg.150%29.aspx).

- **Authentification de message basée sur un domaine, création de rapports et conformité (DMARC).** DMARC permet de recevoir des systèmes de messagerie de déterminer la marche à suivre pour les messages qui échouent aux contrôles SPF ou DKIM et qui procure un autre niveau de confiance pour vos partenaires de messagerie. Pour plus d'informations sur la configuration de DMARC, consultez la rubrique [utiliser DMARC pour valider le courrier électronique dans Office 365](https://technet.microsoft.com/library/mt734386%28v=exchg.150%29.aspx).

Si vous êtes préoccupé par le courrier indésirable, le hameçonnage et l'usurpation d'identité dans Office 365, utilisez SPF, DKIM et DMARC pour éviter le courrier indésirable et l'usurpation indésirable.
  
 **Paramètres gérés par l'utilisateur final.** Si vous recherchez des informations sur la façon dont les utilisateurs finaux peuvent gérer leurs propres paramètres de courrier indésirable, consultez [la rubrique Présentation du filtre de](https://go.microsoft.com/fwlink/?LinkId=270065) courrier indésirable (pour les utilisateurs de Microsoft Outlook) ou le [courrier](https://go.microsoft.com/fwlink/?LinkId=270068) indésirable (pour les utilisateurs d'Outlook sur le Web). Si vous utilisez EOP pour protéger les boîtes aux lettres locales, veillez à utiliser la synchronisation d'annuaires pour vous assurer que ces paramètres sont synchronisés avec le service. Pour plus d'informations sur la configuration de la synchronisation d'annuaires, voir «utiliser la synchronisation d'annuaires pour gérer les utilisateurs de messagerie» dans [Manage mail users in EOP](https://technet.microsoft.com/library/dn636911%28v=exchg.150%29.aspx).
  
## <a name="for-more-information"></a>Pour plus d’informations

[Blog: pourquoi le courrier indésirable et le hameçonnage sont-ils transmis via Office 365?](https://go.microsoft.com/fwlink/?LinkId=528179 )
  
[Forum Aux Questions sur la protection anti-courrier indésirable](https://technet.microsoft.com/library/jj937231%28v=exchg.150%29.aspx)
  
[Empêcher le marquage des faux positifs comme courrier indésirable à l’aide d’une liste fiable ou d’autres techniques](prevent-email-from-being-marked-as-spam-0.md)
  
[Procédure de configuration du filtrage du courrier indésirable Office 365 pour bloquer les messages indésirables](block-email-spam-to-prevent-false-negatives.md)
  
[Quelle est la différence entre courrier inDésirable et courrier électronique en masse?](https://technet.microsoft.com/library/dn720441%28v=exchg.150%29.aspx)
  
[En-têtes de messages anti-courrier indésirable](https://technet.microsoft.com/library/dn205071%28v=exchg.150%29.aspx)
  
[Messages rétrodiffusion et EOP](https://technet.microsoft.com/library/dn499795%28v=exchg.150%29.aspx)

## <a name="more-resources"></a>Ressources complémentaires

[Obtenir de l'aide dans les forums de la Communauté Office 365](https://go.microsoft.com/fwlink/p/?LinkId=518605)
  
[Administrateurs : Se connecter et créer une demande de service](https://go.microsoft.com/fwlink/p/?LinkId=519124)
  
[Administrateurs : appeler le support](https://go.microsoft.com/fwlink/p/?LinkID=518322)
