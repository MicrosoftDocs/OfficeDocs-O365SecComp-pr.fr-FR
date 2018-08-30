---
title: Référence  Stratégies, pratiques et conseils
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: ff3f140b-b005-445f-bfe0-7bc3f328aaf0
description: Microsoft a développé diverses stratégies, procédures et adopté plusieurs meilleures pratiques du secteur pour aider à protéger nos utilisateurs contre les messages électroniques choquant, indésirables ou malveillants.
ms.openlocfilehash: e552128a06ce942383e7c5410508df61331fb874
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23003083"
---
# <a name="reference-policies-practices-and-guidelines"></a>Référence : Stratégies, pratiques et conseils
  
Microsoft s'engage à vous fournir l'expérience utilisateur la plus fiable sur le web. Par conséquent, Microsoft a développé diverses stratégies, procédures et adopté plusieurs meilleures pratiques du secteur pour aider à protéger ses utilisateurs contre les messages abusifs, indésirables ou malveillants. Les expéditeurs qui tentent d'envoyer des messages à des utilisateurs d'Office 365 doivent s'assurer qu'ils ont pris entièrement connaissance des conseils de cet article et qu'ils les suivent afin de poursuivre ces efforts et éviter d'éventuels problèmes de remise.
  
Si vous ne respectez pas ces instructions et stratégies, il se peut que notre équipe de support ne puisse pas vous assister. Si les problèmes de livraison basés sur votre adresse IP d'envoi persistent bien que vous suiviez les instructions, pratiques et stratégies présentées dans cet article, suivez la procédure d'envoi d'une demande de retrait de la liste. Pour plus d'informations, voir [Utilisation du portail Supprimer de la liste pour vous supprimer de la liste des expéditeurs bloqués Office 365](use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis.md).
  
## <a name="general-microsoft-policies"></a>Stratégies générales Microsoft
<a name="GenMsftPolicies"> </a>

Les messages envoyés à des utilisateurs d'Office 365 doivent être conformes à toutes les stratégies Microsoft qui régissent la transmission de messagerie et l'utilisation d'Office 365.
  
- Conditions d'utilisation d'Office 365, en particulier, interdiction d'utiliser le service pour distribuer des courriers indésirables ou des programmes malveillants
    
- [Contrat de Services Microsoft](https://www.microsoft.com/servicesagreement/)
    
## <a name="governmental-regulations"></a>Réglementations gouvernementales
<a name="GovtRegulations"> </a>

Les messages envoyés aux utilisateurs d'Office 365 doivent respecter toutes les lois et réglementations en matière de communications par courrier électronique dans la juridiction applicable.
  
- [CAN-SPAM Act: A Compliance Guide for Business](https://www.ftc.gov/tips-advice/business-center/guidance/can-spam-act-compliance-guide-business)
    
- ["Remove Me" Responses and Responsibilities: Email Marketers Must Honor "Unsubscribe" Claims](https://www.lawpublish.com/ftc-emai-marketers-unsubscribe-claims.mdl)
    
## <a name="technical-guidelines"></a>Instructions techniques
<a name="TechGuidelines"> </a>

Les e-mails envoyés à Office 365 doivent être conformes aux recommandations applicables répertoriées dans les documents ci-dessous (certains liens sont disponibles uniquement en anglais).
  
- [RFC 2505: Anti-Spam Recommendations for SMTP MTAs](https://www.ietf.org/rfc/rfc2505.txt)
    
- [RFC 2920: SMTP Service Extension for Command Pipelining](https://www.ietf.org/rfc/rfc2920.txt)
    
En outre, les serveurs de messagerie qui se connectent à Office 365 doivent respecter les conditions suivantes :
  
- L'expéditeur doit être conforme à toutes les normes techniques en matière de transmission de messages Internet, tel que publié par The Internet Society's Internet Engineering Task Force (IETF), y compris RFC 5321, RFC 5322, entre autres. 
    
- Une fois qu'un expéditeur a reçu un code de réponse d'erreur SMTP numérique compris entre 500 et 599 (également appelé notification d'échec de remise ou NDR), il ne doit pas essayer de retransmettre ce message à ce destinataire.
    
- Après plusieurs notifications d'échec de remise, l'expéditeur ne doit plus effectuer de tentatives d'envoi de messages à ce destinataire.
    
- Les messages ne doivent pas être transmis au moyen de serveurs proxy ou de relais de messagerie non sécurisés.
    
- Le mécanisme de désabonnement (de listes individuelles ou de toutes les listes hébergées par l'expéditeur) doit être clairement documenté et simple à trouver et à utiliser pour les destinataires.
    
- Il se peut que les connexions à partir de l'espace IP dynamique ne soient pas acceptées.
    
- Les serveurs de messagerie doivent avoir des enregistrements DNS inverses valides.
    
## <a name="reputation-management"></a>Gestion de la réputation
<a name="RepManagement"> </a>

Les expéditeurs, les fournisseurs de services Internet et autres fournisseurs de services doivent gérer activement la réputation de vos adresses IP sortantes.
  
## <a name="office-365-limits"></a>Limites d'Office 365
<a name="sectionSection4"> </a>

Les expéditeurs doivent adhérer aux limites d'Office 365 répertoriées dans [Limites d'Exchange Online Protection](https://technet.microsoft.com/library/exchange-online-protection-limits.aspx).
  
## <a name="email-delivery-resources-and-organizations"></a>Organisations et ressources de remise de courrier électronique
<a name="sectionSection5"> </a>

Microsoft collabore activement avec des organismes et fournisseurs de services du secteur afin d'améliorer l'écosystème de la messagerie et d'Internet. Ces organisations ont publié des documents relatifs aux meilleures pratiques que nous soutenons et que nous recommandons aux expéditeurs d'utiliser. Cela améliore votre capacité à remettre des courriers électroniques parmi plusieurs fournisseurs de services de messagerie dans le monde entier.
  
- [Messaging Malware Mobile Anti-Abuse Working Group](https://www.m3aawg.org/)
    
- [Alliance de la gestion de la confidentialité en ligne](https://www.otalliance.org/resources)
    
- [Email Sender &amp; Provider Coalition](http://www.espcoalition.org/)
    
## <a name="abuse-and-spam-reporting"></a>Création de rapport de courrier indésirable et de mauvaise utilisation
<a name="AbuseSpamReports"> </a>

Pour signaler un e-mail illicite, choquant, indésirable ou malveillant, veuillez [rapport indésirable escroqueries par hameçonnage et de messagerie dans Outlook sur le web ](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md). Envoyer ces types de communications constitue une violation de la stratégie de Microsoft et l’action appropriée sera appliquée sur les rapports confirmées.
  
## <a name="law-enforcement"></a>Application des lois
<a name="sectionSection7"> </a>

Si vous êtes un service chargé de l'application des lois et que vous souhaitez fournir à Microsoft Corporation une documentation juridique concernant Office 365, ou si vous avez des questions concernant une documentation juridique que vous avez envoyée à Microsoft, appelez le (1) (425) 722-1299.
  

