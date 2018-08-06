---
title: Forum Aux Questions d'ordre général concernant Exchange Online Protection (EOP)
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/2/2018
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 9dbff00a-474e-4452-aeb5-5be9a6b8c6d5
description: "Cette rubrique présente les réponses aux questions générales les plus fréquentes concernant le service de filtrage du courrier électronique hébergé dans le nuage Microsoft Exchange Online Protection (EOP). Pour d'autres rubriques du Forum Aux Questions (FAQ), suivez les liens suivants :"
ms.openlocfilehash: 9a8ac96678e33623803e95998780b4544dec5a78
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027381"
---
# <a name="eop-general-faq"></a>Forum Aux Questions d'ordre général concernant Exchange Online Protection (EOP)

Cette rubrique présente les réponses aux questions générales les plus fréquentes concernant le service de filtrage du courrier électronique hébergé dans le nuage Microsoft Exchange Online Protection (EOP). Pour d'autres rubriques du Forum Aux Questions (FAQ), suivez les liens suivants :
  
- [Questions fréquemment posées sur les messages mis en file d'attente, différés et retournés dans EOP](eop-queued-deferred-and-bounced-messages-faq.md)
    
- [FAQ sur l'administration déléguée](delegated-administration-faq.md)
    
- [Forum aux questions sur la protection anti-courrier indésirable](../anti-spam-protection-faq.md)
    
- [Listes des expéditeurs autorisés et des expéditeurs bloqués dans Exchange Online](../safe-sender-and-blocked-sender-lists-faq.md)
    
- [FAQ sur la mise en quarantaine](../quarantine-faq.md)
    
- [Forum aux questions sur la protection anti-programme malveillant](../anti-malware-protection-faq-eop.md)
    
- [Message Trace FAQ](http://technet.microsoft.com/library/aa49e3f9-a5b1-4410-aac2-ddbbf3f5bfb2.aspx)
    
- [Forum Aux Questions relatif à la transition de FOPE vers EOP](http://technet.microsoft.com/library/e0e76b89-b0d3-4c0a-bfc8-137b579e983b.aspx)
    
 **Q. Qu'est-ce qu'EOP ?**
  
R. EOP est un service de filtrage de courrier électronique hébergé dans le nuage, conçu pour protéger les clients contre le courrier indésirable et les logiciels malveillants, et pour implémenter des règles de stratégie personnalisées.
  
 **Q. Comment m'inscrire pour un essai d'EOP ou acheter EOP ?**
  
R. Pour vous inscrire pour un essai d'EOP ou pour l'acheter sur le web, visitez la page [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?LinkId=279912). Notez que les fonctionnalités du produit lors de l'achat d'une version d'essai sont identiques à celles du produit avec un abonnement payant, mais que des fonctionnalités supplémentaires fournies avec le plan d'abonnement [Licence d'accès client Exchange Enterprise avec services](https://go.microsoft.com/fwlink/p/?LinkId=320619) sont également comprises. 
  
 **Q. Que coûte EOP ?**
  
R. EOP fait l'objet d'une licence par utilisateur. Pour obtenir les derniers tarifs, consultez la page [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?LinkId=279912).
  
 **Q. Combien de temps faut-il pour qu'EOP soit opérationnel ?**
  
R. Le filtrage commence dès que vous modifiez votre enregistrement MX, conformément aux étapes décrites dans la rubrique [Configurer votre service EOP](set-up-your-eop-service.md), et que votre courrier électronique circule dans EOP. La propagation de l'enregistrement MX via DNS peut prendre entre 24 et 48 heures. Vous pouvez affiner vos paramètres de protection dans le Centre d'administration Exchange (CAE) à tout moment au cours de ce processus.
  
 **Q : dois-je utiliser toutes les fonctionnalités de Microsoft Office 365 pour utiliser EOP ? Que se passe-t-il si je veux protection EOP et c’est tout ?**
  
R. Vous pouvez utiliser EOP pour protéger vos boîtes aux lettres locales sans utiliser aucune autre fonctionnalité d'Office 365. C'est ce qu'on appelle un abonnement autonome. Une liste des fonctionnalités d'EOP est disponible dans la rubrique [Description du service de protection Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=320619).
  
 **Q. Pourquoi ai-je besoin d'un client Office 365 lors de l'inscription pour le filtrage des messages électroniques par EOP ?**
  
R. Office 365 est le nom donné à un ensemble de produits et de services qui sont accessibles via un client Office 365. Envisagez le client Office 365 comme le point de départ auquel vous pouvez ajouter des licences pour le filtrage des messages électroniques.
  
 **Q : EOP a-t-il un portail de communication où puis-je savoir à propos des problèmes connus et les résolutions attendues Qu’advient-il des nouvelles fonctionnalités ?**
  
R. Le Centre d'administration Office 365 disposera de certaines de ces informations. Si vous êtes concerné par un événement de niveau de service, vous devriez voir une alerte de communication (généralement accompagnée d'une icône en forme de cloche) lorsque vous vous connectez au Centre d'administration Office 365. Nous vous recommandons de lire ces informations et d'effectuer les actions appropriées.
  
Pour les nouvelles fonctionnalités EOP, la [feuille de route d'Office 365 pour les entreprises](https://office.microsoft.com/en-us/products/office-365-roadmap-FX104343353.aspx) est une excellente ressource pour trouver des informations sur les nouvelles fonctionnalités à venir. Nous publierons également des articles de blog concernant les nouvelles fonctionnalités sur le site des [blogs Office](https://go.microsoft.com/fwlink/p/?LinkId=392724). 
  
 **Q. Le service fonctionne-t-il avec des versions d'Exchange héritées (par exemple, Exchange Server 2010) et les environnements non Exchange ?**
  
A. Oui. Le service est indépendant du type de serveur et peut être utilisé avec tout agent de transfert du courrier SMTP.
  
 **Q. Quelle doit être la taille de l'organisation pour pouvoir utiliser le service ?**
  
A. N'importe quelle taille. Le réseau EOP offre une capacité suffisante pour s'adapter à la croissance de votre organisation, quelle qu'en soit la vitesse.
  
 **De quelles autorisations ai-je besoin pour configurer EOP ?**
  
Pour configurer EOP, vous devez être un administrateur global Office 365 ou un administrateur d'entreprise Exchange (groupe de rôles Gestion de l'organisation).
  
 **Q. Comment savoir si mes données et informations sont en sûreté ?**
  
R. Pour en savoir plus sur les mesures que nous avons prises pour assurer la sécurité de vos données et informations privées, y compris sur les contrats de niveau de service (SLA), visitez le [Centre de gestion de la protection des données d'Office 365](https://go.microsoft.com/fwlink/p/?LinkId=285405).
  
 **Q. Existe-t-il des limites que je devrais connaître, telles que les limites de taille pour les messages ?**
  
R. Oui. Pour plus d'informations sur les limites dans EOP, voir [Limites d'Exchange Online Protection](https://go.microsoft.com/fwlink/p/?LinkId=402617). 
  
 **Q. EOP prend-il en charge Windows PowerShell à distance ?**
  
R. Oui, toutes les fonctionnalités d'EOP sont disponibles via Windows PowerShell à distance. Pour plus d'informations, voir [PowerShell dans Exchange Online Protection](http://technet.microsoft.com/library/f7918a88-774a-405e-945b-bc2f5ee9f748.aspx).
  

