---
title: Services pour les non clients qui envoient des messages vers Office 365
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 5/2/2016
audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 19fd3e0f-8dbf-4049-a810-2c8ee6cefd48
ms.collection:
- M365-security-compliance
description: Pour préserver la confiance des utilisateurs dans l'utilisation de la messagerie électronique, Microsoft a mis en place diverses stratégies et technologies pour aider à protéger ses utilisateurs.
ms.openlocfilehash: 836beea966e4c944876d418fa88e8c4f6baaf770
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34156636"
---
# <a name="services-for-non-customers-sending-mail-to-office-365"></a>Services pour les non clients qui envoient des messages vers Office 365
  
L'utilisation abusive de la messagerie électronique, les courriers indésirables et les e-mails frauduleux (hameçonnage) continuent à peser sur l'ensemble de l'écosystème de la messagerie. Pour préserver la confiance des utilisateurs dans l'utilisation de la messagerie électronique, Microsoft a mis en place diverses stratégies et technologies pour aider à protéger ses utilisateurs. Cependant, Microsoft comprend que les e-mails légitimes ne doivent pas être affectés négativement. Par conséquent, nous avons établi une suite de services pour aider les expéditeurs à améliorer leur capacité à remettre des e-mails aux utilisateurs d'Office 365 en gérant de façon proactive leur réputation d'envoi.
  
Cette présentation fournit des informations sur les avantages que nous fournissons à votre organisation, même si vous n'êtes pas un client Office 365.
  
## <a name="sender-solutions"></a>Solutions de l'expéditeur
<a name="sectionSection0"> </a>

|**Service**|**Avantages**|
|:-----|:-----|
|Ce contenu d'aide en ligne  <br/> | Fournit :  <br/>  Un point de départ pour toutes les questions relatives à la mise à disposition de communications aux utilisateurs EOP  <br/>  Comprend un guide en ligne simple avec nos stratégies et exigences  <br/>  Une présentation des filtres de courrier indésirable et des technologies d'authentification utilisés par Microsoft  <br/> |
|[Support technique Microsoft](services-for-non-customers.md#AboutSupport) <br/> |Offre un support autonome et de transmission à une instance supérieure pour les problèmes de remise.  <br/> |
|[Portail de suppression d'adresse IP anti-courrier indésirable de la liste d'Office 365](services-for-non-customers.md#DelistPortal) <br/> |Un outil permettant d'envoyer une demande de suppression d'adresse IP de la liste. Avant d'envoyer cette demande, il incombe à l'expéditeur de s'assurer que tout autre courrier provenant de l'adresse IP en question n'est pas abusif ou malveillant.  <br/> |
|[Création de rapport de courrier indésirable et de mauvaise utilisation pour le courrier indésirable provenant d'Exchange Online](services-for-non-customers.md#ReportOurJunk) <br/> |Permet de ne pas envoyer le courrier indésirable à partir d'Exchange Online et de ne pas encombrer Internet et votre système de messagerie.  <br/> |
   
## <a name="microsoft-support"></a>Support technique Microsoft
<a name="AboutSupport"> </a>

Microsoft propose plusieurs options de support pour les personnes ayant des difficultés à envoyer du courrier vers des boîtes de réception Office 365. Nous vous recommandons d'effectuer les actions suivantes :
  
- Suivez les instructions fournies dans les rapports de non-remise que vous recevez.
    
- Consultez les problèmes les plus courants que rencontrent les non clients dans [Résolution des problèmes de messages envoyés à Office 365](troubleshooting-mail-sent-to-office-365.md).
    
- Utilisez le [Portail de suppression d'adresses IP de la liste anti-courrier indésirable Office 365](https://sender.office.com) pour envoyer une demande de suppression de votre adresse IP de la liste des expéditeurs bloqués. 
    
- Lisez les [forums de la communauté Microsoft](https://community.office365.com/en-us/f/).
    
- Contactez le client Office 365 auquel vous essayez d'envoyer un e-mail à l'aide d'une autre méthode et demandez-lui de contacter le support Microsoft et de demander un ticket d'assistance de votre part. Dans certains cas, pour des raisons juridiques, le support Microsoft doit communiquer directement avec l'expéditeur qui possède l'espace IP qui est bloqué. Toutefois, les personnes qui ne sont pas des clients ne peuvent généralement pas demander de tickets d'assistance.
    
     Pour plus d'informations sur le support technique de Microsoft pour Office 365, voir [Prise en charge](https://technet.microsoft.com/library/office-365-support.aspx).
    
## <a name="office-365-anti-spam-ip-delist-portal"></a>Portail de suppression d'adresse IP anti-courrier indésirable de la liste d'Office 365
<a name="DelistPortal"> </a>

Il s'agit d'un portail en libre-service que vous pouvez utiliser pour vous supprimer de la liste des expéditeurs bloqués Office 365. Utilisez ce portail si vous obtenez un message d'erreur lorsque vous tentez d'envoyer un courrier électronique à un destinataire dont l'adresse de messagerie est dans Office 365 alors que vous ne devriez pas. Pour plus d'informations, voir [Utilisation du portail Supprimer de la liste pour vous supprimer de la liste des expéditeurs bloqués Office 365](use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis.md).
  
## <a name="abuse-and-spam-reporting-for-junk-email-originating-from-exchange-online"></a>Création de rapport de courrier indésirable et de mauvaise utilisation pour le courrier indésirable provenant d'Exchange Online
<a name="ReportOurJunk"> </a>

Office 365 est parfois utilisé par des tiers pour envoyer du courrier indésirable, en violation de nos conditions d'utilisation et de notre stratégie. Si vous recevez un courrier indésirable provenant d'Office 365, vous pouvez signaler ces messages à [junk@office365.microsoft.com](mailto:junk@office365.microsoft.com). Veuillez joindre les messages posant problème, y compris l'en-tête complet du message au format RFC 5322 ou ARF. Outlook sur les utilisateurs web peut utiliser les outils intégrés pour signaler des messages de courrier indésirable. Pour plus d’informations, consultez [la rubrique signaler le courrier indésirable et les escroqueries par hameçonnage dans Outlook sur le Web ](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md).
  

